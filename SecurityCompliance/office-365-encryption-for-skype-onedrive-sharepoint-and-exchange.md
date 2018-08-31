---
title: Criptografia do Office 365 para Exchange, SharePoint, OneDrive e Skype
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Resumo: Uma descrição da criptografia do Skype, OneDrive, SharePoint e o Exchange Online.'
ms.openlocfilehash: 5b839b8d290306f2334d3ca3278d0d5dac20a56f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524067"
---
# <a name="office-365-encryption-for-skype-for-business-onedrive-for-business-sharepoint-online-and-exchange-online"></a>Criptografia do Office 365 para Skype for Business, OneDrive para negócios, SharePoint Online e Exchange Online

O Office 365 é um ambiente altamente seguro que oferece proteção extensiva em várias camadas: físico Datacenter segurança, segurança de rede, segurança de acesso, a segurança do aplicativo e a segurança dos dados.

## <a name="skype-for-business"></a>Skype for Business
Skype para dados de negócios do cliente pode ser armazenado em repouso na forma de arquivos ou apresentações que são carregadas pelos participantes da reunião. O servidor de webconferência criptografa os dados do cliente usando o AES com uma chave de 256 bits. Os dados do cliente criptografada são armazenados em um compartilhamento de arquivo. Cada parte dos dados do cliente é criptografado usando uma chave de 256 bits gerada aleatoriamente diferente. Quando uma parte dos dados do cliente é compartilhada em uma conferência, o servidor de webconferência instrui os clientes de conferência para baixar os dados criptografados do cliente via HTTPS. Ele envia a chave correspondente aos clientes de forma que os dados do cliente podem ser descriptografados. O servidor de webconferência também autentica clientes de conferência antes que ele permita que os clientes do acesso aos dados do cliente de conferência. Ao ingressar em uma conferência via Web, cada cliente de conferência estabelece uma caixa de diálogo SIP com o componente de foco de conferência executando dentro do servidor front-end via TLS primeiro. O foco de conferência passa para o cliente de conferência, um cookie de autenticação gerado pelo servidor de webconferência. O cliente de conferência se conecta ao servidor de webconferência apresentando o cookie de autenticação sejam autenticados pelo servidor.

## <a name="sharepoint-online-and-onedrive-for-business"></a>SharePoint Online e OneDrive for Business
Todos os arquivos de cliente no SharePoint Online são protegidos por chaves por arquivo exclusivo, que sempre são exclusivas para um único locatário. As chaves são tanto criado e gerenciado pelo serviço Online do SharePoint ou quando o cliente chave for usada, criado e gerenciado pelos clientes. Quando um arquivo for carregado, a criptografia é realizada pelo SharePoint Online dentro do contexto da solicitação de carregamento, antes de serem enviados para o armazenamento do Azure. Quando um arquivo é baixado, o SharePoint Online recupera o cliente criptografado dados do armazenamento do Azure com base no identificador exclusivo do documento e os criptografa os dados do cliente antes de enviá-lo ao usuário. Armazenamento do Azure não tem nenhuma capacidade para descriptografar, ou até mesmo identificar ou compreender os dados do cliente. Toda a criptografia e descriptografia acontecer nos sistemas mesmos que impõe o isolamento de locatário, que são o Azure Active Directory e no SharePoint Online.

Várias cargas de trabalho no Office 365 armazenam dados no SharePoint Online, incluindo Teams da Microsoft, que armazena todos os arquivos no SharePoint Online e o OneDrive for Business, que utilizará o SharePoint Online para seu armazenamento. Todos os dados do cliente armazenados no SharePoint Online é criptografado (com uma ou mais chaves AES 256 bits) e distribuídos em data centers da seguinte maneira. (Cada etapa deste processo de criptografia é FIPS 140-2 nível 2 validado. Para obter informações adicionais sobre a conformidade FIPS 140-2, consulte [a conformidade FIPS 140-2](https://docs.microsoft.com/previous-versions/sql/sql-server-2008-r2/bb326611(v=sql.105))).
- Cada arquivo é dividido em partes de um ou mais, dependendo do tamanho do arquivo. Cada bloco é criptografado usando sua própria chave AES 256 bits exclusiva.
- Quando um arquivo for atualizado, a atualização é tratada da mesma maneira: a alteração é dividida em um ou mais blocos e cada bloco é criptografado com uma chave exclusiva separada.
- Esses blocos – arquivos, partes de arquivos e atualização deltas – são armazenados como blobs no armazenamento do Azure aleatoriamente distribuídas em várias contas de armazenamento do Azure. 
- O conjunto de chaves de criptografia esses blocos de dados do cliente é criptografada.
   - As teclas usadas para criptografar os blobs são armazenadas no SharePoint Online conteúdo banco de dados.
   - O banco de dados de conteúdo é protegido por controles de acesso do banco de dados e a criptografia em repouso. Criptografia é realizada usando a [Criptografia de dados transparentes](https://docs.microsoft.com/sql/relational-databases/security/encryption/transparent-data-encryption-tde) (TDE) no [Banco de dados de SQL Azure](https://docs.microsoft.com/azure/sql-database/sql-database-technical-overview). (O banco de dados do SQL azure é um serviço de uso geral de banco de dados relacional in Microsoft Azure que suporta estruturas como dados relacionais, JSON, espacial e XML.) Esses segredos estão no nível de serviço para o SharePoint Online, não no nível do locatário. Esses segredos (às vezes referidos como as chaves mestre) são armazenados em um repositório seguro separado chamado repositório de chave. A TDE fornece segurança em repouso para o banco de dados ativo e os backups de banco de dados e logs de transações. 
   - Quando os clientes fornecer a chave opcional, a chave do cliente é armazenada no compartimento de chave do Windows Azure e o serviço usa a chave para criptografar uma chave de locatário, que é usada para criptografar uma chave de site, que é usada para criptografar as chaves de nível de arquivo. Essencialmente, uma nova hierarquia de chaves é introduzida quando o cliente fornece uma chave.
- O mapa usado para montar novamente o arquivo é armazenado no banco de dados de conteúdo, juntamente com as chaves criptografadas, separadamente da chave mestre necessária para descriptografá-los.
- Cada conta de armazenamento do Azure tem seus próprio credenciais exclusivas por tipo de acesso (leitura, gravação, enumerar e excluir). Cada conjunto de credenciais é mantido no repositório de chave segura e é atualizado regularmente. Conforme descrito acima, há três tipos diferentes de repositórios, cada um com uma função distinta:
- Dados de cliente são armazenados como blobs criptografadas no armazenamento do Azure. A tecla a cada bloco de dados do cliente é criptografada e armazenada separadamente do banco de dados de conteúdo. Os dados do cliente em si contém nenhuma indicação de como ele pode ser descriptografado.
- O banco de dados de conteúdo é um banco de dados do SQL Server. Ele contém o mapa necessário para localizar e monte os blobs de dados customer mantidos no armazenamento do Azure, bem como as chaves necessárias para criptografar os blobs. No entanto, o conjunto de chaves é próprio criptografadas (conforme explicado acima) e mantido em um repositório separado da chave.
- O armazenamento de chave é fisicamente separado do armazenamento de banco de dados de conteúdo e o Windows Azure. Ele contém as credenciais para cada contêiner de armazenamento do Azure e a chave mestra para o conjunto de chaves criptografadas mantidos no banco de dados de conteúdo.

Cada um desses três componentes de armazenamento – o Azure blob store, o banco de dados de conteúdo e o repositório de chave – é fisicamente separado. As informações contidas em qualquer um dos componentes não estão disponível por conta própria. Sem acesso a todos os três, é impossível recuperar as chaves para os fragmentos, descriptografar as chaves para torná-los utilizável, associar as chaves com seus fragmentos correspondentes, descriptografar cada bloco ou reconstruir um documento a partir de suas partes constituintes.

Certificados do BitLocker, o que proteger os volumes de disco físico em máquinas no datacenter, são armazenados em um repositório seguro (o armazenamento do SharePoint Online secreto) que estiver protegido pela chave do Farm.

As chaves TDE proteger as chaves por blob são armazenadas em dois locais:
- O repositório seguro, que hospeda os certificados BitLocker e estiver protegido pela chave do Farm; e
- Em um repositório seguro gerenciado por banco de dados de SQL Azure.

As credenciais usadas para acessar os contêineres do armazenamento do Azure também são mantidas no SharePoint Online segredo armazenar e delegados para cada farm do SharePoint Online, conforme necessário. Essas credenciais são assinaturas do armazenamento do Azure SAS, com credenciais separadas usadas para ler ou gravar dados e com a diretiva aplicada para que eles autoexpirarem a cada 60 dias. Credenciais diferentes são usadas para ler ou gravar dados (não ambos) e farms do SharePoint Online não são concedidas permissões para enumerar.

> Clientes de anotação para Office 365 governo dos Estados Unidos, blobs de dados são armazenados no armazenamento do Azure US governamentais. Além disso, o acesso às chaves do SharePoint Online no Office 365 US governo é limitado à equipe do Office 365 que tenha sido especificamente analisada. Equipe de operações do Azure governo dos EUA não têm acesso para o repositório de chave on-line do SharePoint que é usado para criptografar os blobs de dados.

Para obter mais informações sobre a criptografia de dados no SharePoint Online e o OneDrive for Business, consulte [Criptografia de dados no OneDrive for Business e no SharePoint Online](https://technet.microsoft.com/en-us/library/dn905447.aspx).

### <a name="list-items-in-sharepoint-online"></a>Itens de lista no SharePoint Online
Itens de lista são partes menores de dados que são criados ad hoc ou que podem residir mais dinamicamente em um site, como postagens individuais em um blog SharePoint Online ou entradas dentro de uma página de wiki do SharePoint Online, de linhas em uma lista criado pelo usuário do cliente. Itens de lista são armazenados no banco de dados (banco de dados de SQL Azure) conteúdo e protegidas com TDE.

## <a name="encryption-of-data-in-transit"></a>Criptografia de dados em trânsito
No OneDrive for Business e no SharePoint Online, há dois cenários em que os dados entram e saem dos data centers.
- **Comunicação do cliente com o servidor** - comunicação ao OneDrive for Business pela Internet usa conexões SSL/TLS. Todas as conexões SSL são estabelecidas usando chaves 2048 bits.
- **Movimentação de dados entre data centers** - o principal motivo para mover dados entre data centers destina-se a replicação geo habilitar a recuperação de desastres. Por exemplo, logs de transações do SQL Server e deltas de armazenamento de blob viajam junto este pipe. Enquanto este dados já são transmitidos por meio de uma rede privada, ela é ainda mais protegida com criptografia de ponta.


## <a name="exchange-online"></a>Exchange Online
O Exchange Online usa BitLocker para todos os dados de caixa de correio e a configuração de disco BitLocker é descrita no [BitLocker para criptografia](office-365-bitlocker-and-distributed-key-manager-for-encryption.md). A criptografia de nível de serviço criptografa todos os dados de caixa de correio no nível de caixa de correio. 

Além da criptografia de serviço, o Office 365 oferece suporte a chave de cliente, que baseia-se na parte superior de criptografia de serviço. Chave do cliente é uma opção de chave gerenciada Microsoft para a criptografia de serviço Exchange Online que também está no mapa da Microsoft. Esse método de criptografia fornece maior proteção não proporcionada pelo BitLocker porque ele fornece a separação dos administradores do servidor e as chaves criptográficas necessárias para a descriptografia de dados e a criptografia é aplicada diretamente aos dados (em contraste com BitLocker, que se aplica a criptografia de volume do disco lógico) quaisquer dados do cliente copiados de um servidor Exchange permanecerão criptografados.

O escopo para a criptografia do serviço Exchange Online é dados do cliente que estão armazenados em repouso no Exchange Online. (Skype para negócios armazena quase todas as conteúdo gerado pelo usuário dentro da caixa de correio Exchange Online do usuário e, portanto, herda o recurso de criptografia de serviço do Exchange Online.)

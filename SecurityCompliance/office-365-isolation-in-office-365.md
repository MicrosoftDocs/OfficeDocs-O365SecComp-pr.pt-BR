---
title: Controle de acesso e isolamento do Office 365 no Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: 'Resumo: uma explicação do isolamento e controle de acesso dentro dos vários aplicativos do Office 365.'
ms.openlocfilehash: 748da21f5b5048bb4ae4c14700ed482fd6d0058c
ms.sourcegitcommit: e23b84ef4eee9cccec7205826b71ddfe9aaac2f8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33402889"
---
# <a name="isolation-and-access-control-in-office-365"></a>Isolamento e controle de acesso no Office 365

O Azure Active Directory e o Office 365 usam um modelo de dados altamente complexo que inclui dezenas de serviços, centenas de entidades, milhares de relações e dezenas de milhares de atributos. Em um nível alto, o Azure Active Directory e os diretórios de serviço são os contêineres de locatários e destinatários mantidos em sincronia usando protocolos de replicação baseados em estado. Além das informações de diretório mantidas no Azure Active Directory, cada uma das cargas de trabalho de serviço tem sua própria infraestrutura de serviços de diretório.
 
![Sincronização de dados do locatário do Office 365](media/office-365-isolation-tenant-data-sync.png)

Dentro desse modelo, não há uma única fonte de dados de diretório. Sistemas específicos possuem partes individuais de dados, mas nenhum sistema único armazena todos os dados. Os serviços do Office 365 cooperar com o Azure Active Directory neste modelo de dados. O Azure Active Directory é o "sistema de verdade" para dados compartilhados, que normalmente são pequenos e estáticos usados por todos os serviços. O modelo federado usado no Office 365 e no Azure Active Directory fornece a exibição compartilhada dos dados.

O Office 365 usa o armazenamento físico e o armazenamento em nuvem do Azure. O Exchange Online (incluindo o Exchange Online Protection) e o Skype for Business usam seu próprio armazenamento para dados do cliente. O SharePoint Online usa o armazenamento do SQL Server e o armazenamento do Azure, portanto, a necessidade de isolamento adicional dos dados do cliente no nível de armazenamento.

## <a name="exchange-online"></a>Exchange Online

O Exchange Online armazena dados do cliente em caixas de correio. As caixas de correio são hospedadas em bancos de dados ESE (Extensible Storage Engine) chamados de bancos de dados de caixa de correio. Isso inclui caixas de correio de usuário, caixas de correio vinculadas, caixas de correio compartilhadas e caixas de correio de pasta pública. As caixas de correio de usuários incluem o conteúdo salvo do Skype for Business, como históricos de conversas.

O conteúdo da caixa de correio do usuário inclui:

- Emails e anexos de email
- Informações de calendário e disponibilidade
- Contatos
- Tarefas
- Observações
- Grupos
- Dados de inFerência

Cada banco de dados de caixa de correio no Exchange Online contém caixas de correio de vários locatários. Um código de autorização protege cada caixa de correio, incluindo dentro de uma locação. Por padrão, somente o usuário atribuído tem acesso a uma caixa de correio. A lista de controle de acesso (ACL) que protege uma caixa de correio contém uma identidade autenticada pelo Azure Active Directory no nível do locatário. As caixas de correio de cada locatário estão limitadas às identidades autenticadas no provedor de autenticação do locatário, que inclui apenas os usuários desse locatário. O conteúdo no locatário A não pode ser obtido por usuários no locatário B, a menos que explicitamente aprovado pelo locatário A.

## <a name="skype-for-business"></a>Skype for Business

O Skype for Business armazena dados em vários locais:

- As informações de usuário e conta, que incluem pontos de extremidade de conexão, IDs de locatário, planos de discagem, configurações de roaming, estado de presença, listas de contatos, etc., são armazenadas nos servidores do Active Directory do Skype for Business e em vários servidores de banco de dados do Skype for Business. As listas de contatos são armazenadas na caixa de correio do Exchange Online do usuário se o usuário estiver habilitado para ambos os produtos ou nos servidores do Skype for Business se o usuário não for. Os servidores de banco de dados do Skype for Business não são particionados por locatário, mas o isolamento de vários associados é imposto por meio do controle de acesso baseado em função (RBAC).
- O conteúdo da reunião e os dados carregados são armazenados em compartilhamentos do sistema de arquivos distribuídos (DFS). Esse conteúdo também pode ser arquivado no Exchange Online, se estiver habilitado. Os compartilhamentos DFS não são particionados por locatário. o conteúdo é protegido com ACLs e a multilocação é imposta por meio de RBAC.
- Os registros de detalhes da chamada, que são o histórico de atividades, como histórico de chamadas, sessões de IM, compartilhamento de aplicativos, histórico de IM, etc., também podem ser armazenados no Exchange Online, mas a maioria dos registros de detalhes das chamadas são temporariamente armazenados em servidores de CDR (registro de detalhes de chamadas). O conteúdo não é particionado por locatário, mas a multilocação é imposta por meio de RBAC.

## <a name="sharepoint-online"></a>SharePoint Online

O SharePoint Online tem vários mecanismos independentes que oferecem isolamento de dados. Ele armazena objetos como código abstrato em bancos de dados de aplicativo. Por exemplo, quando um usuário carrega um arquivo para o SharePoint Online, o arquivo é desmontado, convertido em código do aplicativo e armazenado em várias tabelas em vários bancos de dados.

Se um usuário puder obter acesso direto ao armazenamento que contém os dados, o conteúdo não poderá ser interpretado por um humano ou qualquer sistema que não seja o SharePoint Online. Esses mecanismos incluem controle de acesso de segurança e propriedades. Todos os recursos do SharePoint Online são protegidos pelo código de autorização e pela política RBAC, incluindo dentro de um locatário. A lista de controle de acesso (ACL) que protege um recurso contém uma identidade autenticada no nível do locatário. Os dados do SharePoint Online para um locatário são limitados às identidades autenticadas pelo provedor de autenticação para o locatário.

Além das ACLs, uma propriedade de nível de locatário que especifica o provedor de autenticação (que é o Azure Active Directory específico do locatário), é gravada uma vez e não pode ser alterada depois de definida. Depois que a propriedade locatário do provedor de autenticação tiver sido definida para um locatário, ela não poderá ser alterada usando as APIs expostas a um locatário.

Um *SubscriptionId* exclusivo é usado para cada locatário. Todos os sites de clientes pertencem a um locatário e recebem uma *assinatura* exclusiva para o locatário. A ** Propriedade SubscriptionId em um site é escrita uma vez e é permanente. Uma vez atribuída a um locatário, um site não pode ser movido para outro locatário. *SubscriptionId* é a chave usada para criar o escopo de segurança para o provedor de autenticação e está vinculada ao locatário.

O SharePoint Online usa o SQL Server e o armazenamento do Azure para armazenamento de metadados de conteúdo. A chave de partição para o repositório de ** conteúdo é SiteId no SQL. Ao executar uma consulta SQL, o SharePoint Online usa ** um SiteId verificado como parte de uma verificação de *SubscriptionId* no nível do locatário.

O SharePoint Online armazena conteúdo de arquivo criptografado em BLOBs do Microsoft Azure. Cada farm do SharePoint Online tem sua própria conta do Microsoft Azure e todos os BLOBs salvos no Azure são criptografados individualmente com uma chave armazenada no repositório de conteúdo do SQL. A chave de criptografia protegida no código pela camada de autorização e não exposta diretamente ao usuário final. O SharePoint Online tem monitoramento em tempo real para detectar quando uma solicitação HTTP lê ou grava dados para mais de um locatário. A identidade da ** solicitação SubscriptionId é controlada em relação à *SubscriptionId* do recurso acessado. As solicitações para acessar recursos de mais de um locatário nunca devem acontecer por usuários finais. As solicitações de serviço em um ambiente de vários locatários são a única exceção. Por exemplo, o rastreador de pesquisa recebe alterações de conteúdo para todo o banco de dados de uma só vez. Isso geralmente envolve a consulta de sites de mais de um locatário em uma única solicitação de serviço, que é feita por motivos de eficiência.

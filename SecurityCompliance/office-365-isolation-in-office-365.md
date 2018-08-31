---
title: Isolamento de Office 365 e o controle de acesso no Office 365
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
description: 'Resumo: Uma explicação dos isolamento e controle de acesso dentro dos vários aplicativos do Office 365.'
ms.openlocfilehash: c1989bc546df357740ea963a1a241dfa14557931
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524607"
---
# <a name="isolation-and-access-control-in-office-365"></a>Isolamento e controle de acesso no Office 365

Azure Active Directory e o Office 365 usam um modelo de dados altamente complexos que inclui dezenas de serviços, centenas de entidades, milhares de relações e dezenas de milhares de atributos (entidades, relações e atributos, geralmente, são específicas de aplicativos). Em um alto nível, Azure Active Directory e os diretórios de serviço são os contêineres de locatários e destinatários e elas são mantidas em sincronia usando os protocolos de replicação baseada em estado. Além das informações de diretório mantidas no Azure Active Directory, cada um dos serviços também têm seu próprios infraestrutura de serviços de diretório (por exemplo, serviços de diretório do Exchange Online, SharePoint Online Directory Services, etc.). 
 
![Sincronização de dados de Inquilino do Office 365](media/office-365-isolation-tenant-data-sync.png)

Dentro desse modelo, não há única fonte de dados de diretório. Cada item individual de dados é pertencentes a um sistema específico, mas nenhum sistema único contém todos os dados. Serviços do Office 365 cooperam com o Windows Azure Active Directory para concretizar o modelo de dados. Azure Active Directory é o "sistema veracidade" para dados compartilhados, que geralmente são pequenos e estáticos dados frequentemente usados por cada serviço. O modelo de federada usado dentro do Office 365 e Windows Azure Active Directory fornece a exibição compartilhada dos dados.

O Office 365 usa armazenamento físico e o armazenamento em nuvem do Windows Azure. O Exchange Online (incluindo o Exchange Online Protection) e Skype para negócios usam seu próprio armazenamento de dados do cliente. SharePoint Online aproveita seu armazenamento do SQL Server e o armazenamento do Azure, exigindo a necessidade de isolamento adicionais de dados do cliente no nível de armazenamento.

## <a name="exchange-online"></a>Exchange Online
O Exchange Online armazena dados de clientes dentro de caixas de correio hospedadas nos bancos de dados de mecanismo de armazenamento extensível (ESE) chamados bancos de dados de caixa de correio. Isso inclui caixas de correio do usuário, caixas de correio vinculadas, caixas de correio compartilhadas e caixas de correio de pasta pública. Caixas de correio de usuário também podem incluir salva Skype para conteúdo de negócios, como os históricos de conversa. O conteúdo de caixa de correio de usuário inclui emails e anexos de email, as informações de calendário e informações de disponibilidade, contatos, tarefas, anotações, grupos e dados inferência.

Cada banco de dados de caixa de correio no Exchange Online contém caixas de correio de vários locatários. Todas as caixas de correio são protegidas pelo código de autorização, incluindo dentro de um locatário. Como com uma implantação local do Exchange, por padrão apenas o usuário atribuído tem acesso a uma caixa de correio. A lista de controle de acesso (ACL) que protege uma caixa de correio contém uma identidade que é autenticada pelo Windows Azure Active Directory no nível do locatário. As caixas de correio para um determinado inquilino estão limitadas a identidades autenticadas em relação ao provedor de autenticação desse inquilino, que incluem somente os usuários de que locatário. Conteúdo pertencentes a TenantA não é possível de nenhuma maneira ser obtido por usuários em TenantB, a menos que explicitamente aprovadas pelos TenantA.

## <a name="skype-for-business"></a>Skype for Business
Skype para negócios armazena dados em vários locais:
- Conta de informações, que inclui os pontos de extremidade de conexão, locatário IDs, planos de discagem, roaming configurações, estado de presença, listas de contatos, etc. e o usuário está armazenado o Skype para servidores do Active Directory de negócios, bem como em vários Skype para o banco de dados corporativos servidores. Listas de contatos são armazenadas na caixa de correio Exchange Online do usuário se o usuário estiver habilitado para ambos os produtos, ou em Skype para servidores de negócios se o usuário não está. Skype para servidores de banco de dados corporativos não são particionados por locatário, mas a multilocação isolamento de dados é imposto por meio de RBAC.
- Conteúdo da reunião, como o conteúdo que os usuários carregar durante Skype para reuniões de negócios, é armazenado em compartilhamentos de sistema de arquivos distribuídos. Este conteúdo também pode ser arquivado no Exchange Online, desde que o arquivamento é habilitado. Os compartilhamentos DFS não são particionados por locatário, mas o conteúdo é protegido com ACLs e multilocação é imposta por meio de RBAC.
- Registros de detalhe de chamada, que é o histórico de atividade, como histórico de chamadas, sessões de IM, compartilhamento de aplicativos, histórico de mensagens Instantâneas, etc., também podem ser armazenados no Exchange Online, mas a maioria dos registros de detalhe de chamada são temporariamente armazenados nos servidores de registro (CDR) de detalhe de chamada. Conteúdo não é particionado por locatário, mas a multilocação é imposta por meio de RBAC.

## <a name="sharepoint-online"></a>SharePoint Online
Há vários mecanismos independentes exclusivos para o SharePoint Online que fornecem o isolamento de dados. SharePoint Online armazena objetos como código abstrata dentro de bancos de dados de aplicativo. Por exemplo, quando um usuário carrega um arquivo para o SharePoint Online, esse arquivo é desmontado e convertido no código do aplicativo e armazenado em várias tabelas entre vários bancos de dados.

Se um usuário poderá obter acesso direto ao armazenamento contendo os dados, o conteúdo não seria interpretable para uma pessoa ou qualquer sistema diferente do SharePoint Online. Esses mecanismos incluem propriedades e controle de acesso de segurança. Conforme descrito acima, todos os recursos do SharePoint Online são protegidos pela diretiva de RBAC, inclusive dentro de uma locação e do código de autorização. A lista de controle de acesso (ACL) que protege um recurso contém uma identidade que é autenticada no nível do locatário. Assim como acontece com o Exchange Online, no SharePoint Online, os dados para um determinado inquilino estão limitados a identidades autenticadas em relação ao provedor de autenticação desse inquilino, que incluem somente os usuários de que locatário.

As ACLs, além de uma propriedade de nível de locatário que especifica o provedor de autenticação (que é específica do locatário do Azure Active Directory), é gravada uma vez e não pode ser alterado depois de definido. Depois que a propriedade de locatário do provedor de autenticação tiver sido definida para um inquilino, ele não pode ser alterado usando qualquer APIs expostos para um inquilino.

Um único *SubscriptionId* também é usado para cada inquilino. Todos os locais de clientes pertencem a um locatário e que estão atribuídos a um *SubscriptionId* exclusivo para o inquilino. A propriedade *SubscriptionId* em um site é gravada uma vez e não pode ser alterada. Depois que um site é atribuído a um locatário, não podem ser movido para um locatário diferente posteriormente usando a API do repositório de conteúdo. A *SubscriptionId* também é a chave que é usada para criar o escopo de segurança para o provedor de autenticação e está vinculada ao inquilino.

SharePoint Online usa o armazenamento do SQL Server e Windows Azure para o armazenamento de conteúdo. No nível do SQL, a chave da partição do repositório de conteúdo é *SiteId*. Ao executar uma consulta SQL, SharePoint Online usa *SiteId* foi verificado como parte de uma verificação de nível de locatário *SubscriptionId* .

SharePoint Online armazena blobs de arquivo binário (por exemplo, os fluxos de arquivo) no Microsoft Azure. Cada farm do SharePoint Online tem sua própria conta Microsoft Azure e todos os blobs salvos no Azure são criptografados individualmente usando uma chave que é armazenada no repositório de conteúdo do SQL. A chave de criptografia não está exposta diretamente ao usuário final e é protegida em código pela camada de autorização. Finalmente, o SharePoint Online tem o monitoramento em tempo real em vigor para detectar quando uma solicitação HTTP lê ou grava dados para mais de um inquilino. Ele realiza isso mediante a *SubscriptionId* da identidade solicitação contra a *SubscriptionId* do recurso está sendo acessado de acompanhamento. Uma solicitação de acesso a recursos de mais de um inquilino nunca deve acontecer pelo usuário final. Ele pode acontecer para solicitações de serviço em um ambiente de multilocação, no entanto. Por exemplo, o rastreador de pesquisa extrai o conteúdo é alterado para um banco de dados inteiro todo ao mesmo tempo. Isso geralmente envolve consultando sites de mais de um inquilino em uma solicitação de serviço único, que é feito por motivos de eficiência.

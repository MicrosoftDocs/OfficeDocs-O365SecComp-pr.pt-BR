---
title: Controle de acesso e isolamento do Office 365 no Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: 'Resumo: uma explicação do isolamento e controle de acesso dentro dos vários aplicativos do Office 365.'
ms.openlocfilehash: 734c92a6f3185a25faf9aade1ba235444ed762da
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216851"
---
# <a name="isolation-and-access-control-in-office-365"></a>Isolamento e controle de acesso no Office 365

O Azure Active Directory e o Office 365 usam um modelo de dados altamente complexo que inclui dezenas de serviços, centenas de entidades, milhares de relações e dezenas de milhares de atributos (entidades, relações e atributos costumam ser específicos de aplicativos). Em um nível alto, o Azure Active Directory e os diretórios de serviço são contêineres de locatários e destinatários, e são mantidos em sincronização usando protocolos de replicação baseados em estado. Além das informações de diretório mantidas no Azure Active Directory, cada um dos serviços também tem sua própria infraestrutura de serviços de diretório (por exemplo, serviços de diretório do Exchange Online, serviços de diretório do SharePoint Online, etc.). 
 
![Sincronização de dados do locatário do Office 365](media/office-365-isolation-tenant-data-sync.png)

Dentro desse modelo, não há uma única fonte de dados de diretório. Cada parte de dados individual pertence a um sistema específico, mas nenhum sistema contém todos os dados. Os serviços do Office 365 cooperar com o Azure Active Directory para obter o modelo de dados. O Azure Active Directory é o "sistema de verdade" para dados compartilhados, que normalmente são pequenos e dados estáticos usados frequentemente por cada serviço. O modelo federado usado no Office 365 e no Azure Active Directory fornece a exibição compartilhada dos dados.

O Office 365 usa o armazenamento físico e o armazenamento em nuvem do Azure. O Exchange Online (incluindo o Exchange Online Protection) e o Skype for Business usam seu próprio armazenamento para dados do cliente. O SharePoint Online utiliza o armazenamento do SQL Server e o armazenamento do Azure, o que exige a necessidade de isolamento adicional dos dados do cliente no nível de armazenamento.

## <a name="exchange-online"></a>Exchange Online
O Exchange Online armazena dados do cliente em caixas de correio hospedadas em bancos de dados ESE (Extensible Storage Engine) chamados de bancos de dados de caixa de correio. Isso inclui caixas de correio de usuário, caixas de correio vinculadas, caixas de correio compartilhadas e caixas de correio de pasta pública. As caixas de correio do usuário também podem incluir conteúdo salvo do Skype for Business, como históricos de conversas. O conteúdo da caixa de correio do usuário inclui emails e anexos de email, informações de calendário e disponibilidade, contatos, tarefas, observações, grupos e dados de inferência.

Cada banco de dados de caixa de correio no Exchange Online contém caixas de correio de vários locatários. Todas as caixas de correio são protegidas por código de autorização, incluindo dentro de um locatário. Como em uma implantação local do Exchange, por padrão, apenas o usuário atribuído tem acesso a uma caixa de correio. A lista de controle de acesso (ACL) que protege uma caixa de correio contém uma identidade que é autenticada pelo Azure Active Directory no nível do locatário. As caixas de correio de um determinado locatário são limitadas às identidades autenticadas no provedor de autenticação do locatário, que incluem apenas usuários desse locatário. O conteúdo que pertence ao Locatárioa não pode ser obtido por usuários no TenantB, a menos que explicitamente aprovado pelo Locatárioa.

## <a name="skype-for-business"></a>Skype for Business
O Skype for Business armazena dados em vários lugares:
- As informações de usuário e conta, que incluem pontos de extremidade de conexão, IDs de locatário, planos de discagem, configurações de roaming, estado de presença, listas de contatos, etc., são armazenadas nos servidores do Active Directory do Skype for Business, bem como em vários bancos de dados do Skype for Business servidores. As listas de contatos são armazenadas na caixa de correio do Exchange Online do usuário se o usuário estiver habilitado para ambos os produtos ou nos servidores do Skype for Business se o usuário não for. Os servidores de banco de dados do Skype for Business não são particionados por locatário, mas o isolamento de vários associados é imposto por meio de RBAC.
- O conteúdo da reunião, como o carregamento de usuários de conteúdo durante as reuniões do Skype for Business, é armazenado em compartilhamentos do sistema de arquivos distribuídos. Esse conteúdo também pode ser arquivado no Exchange Online fornecido o arquivamento está habilitado. Os compartilhamentos DFS não são particionados por locatário, mas o conteúdo é protegido com ACLs e a multilocação é imposta por meio de RBAC.
- Os registros de detalhes da chamada, que é o histórico de atividades, como histórico de chamadas, sessões de IM, compartilhamento de aplicativos, histórico de mensagens INSTANTÂNEAs, etc., também podem ser armazenados no Exchange Online, mas a maioria dos registros de detalhes das chamadas são temporariamente armazenados em servidores de CDR (registro de detalhes de chamadas). O conteúdo não é particionado por locatário, mas a multilocação é imposta por meio de RBAC.

## <a name="sharepoint-online"></a>SharePoint Online
Há vários mecanismos independentes exclusivos do SharePoint Online que oferecem isolamento de dados. O SharePoint Online armazena objetos como código abstrato em bancos de dados de aplicativos. Por exemplo, quando um usuário carrega um arquivo para o SharePoint Online, esse arquivo é desmontado e convertido em código do aplicativo e armazenado em várias tabelas em vários bancos de dados.

Se um usuário puder obter acesso direto ao armazenamento contendo os dados, o conteúdo não poderá ser interpretado para um humano ou qualquer sistema que não seja o SharePoint Online. Esses mecanismos incluem controle de acesso de segurança e propriedades. Conforme descrito acima, todos os recursos do SharePoint Online são protegidos pelo código de autorização e pela política RBAC, incluindo dentro de um locatário. A lista de controle de acesso (ACL) que protege um recurso contém uma identidade que é autenticada no nível do locatário. Como no Exchange Online, no SharePoint Online, os dados de um determinado locatário são limitados às identidades autenticadas no provedor de autenticação do locatário, que incluem apenas os usuários desse locatário.

Além das ACLs, uma propriedade de nível de locatário que especifica o provedor de autenticação (que é o Azure Active Directory específico do locatário), é gravada uma vez e não pode ser alterada depois de definida. Depois que a propriedade locatário do provedor de autenticação tiver sido definida para um locatário, ela não poderá ser alterada usando as APIs expostas a um locatário.

Um *SubscriptionId* exclusivo também é usado para cada locatário. Todos os sites de clientes pertencem a um locatário e recebem uma *assinatura* exclusiva do locatário. A ** Propriedade SubscriptionId em um site é gravada uma vez e não pode ser alterada. Depois que um site é atribuído a um locatário, ele não pode ser movido para um locatário diferente mais tarde usando a API do repositório de conteúdo. *SubscriptionId* também é a chave usada para criar o escopo de segurança para o provedor de autenticação e está vinculada ao locatário.

O SharePoint Online usa o SQL Server e o armazenamento do Azure para o armazenamento de conteúdo. No nível SQL, a chave de partição para o repositório de conteúdo ** é SiteId. Ao executar uma consulta SQL, o SharePoint Online usa ** um SiteId que foi verificado como parte de uma verificação de *SubscriptionId* no nível do locatário.

O SharePoint Online armazena blobs binários de arquivos (por exemplo, os fluxos de arquivos) no Microsoft Azure. Cada farm do SharePoint Online tem sua própria conta do Microsoft Azure e todos os BLOBs salvos no Azure são criptografados individualmente usando uma chave que é armazenada no repositório de conteúdo do SQL. A chave de criptografia não é exposta diretamente ao usuário final e é protegida no código pela camada de autorização. Por fim, o SharePoint Online tem monitoramento em tempo real em vigor para detectar quando uma solicitação HTTP lê ou grava dados para mais de um locatário. Ele faz isso acompanhando *SubscriptionId* da identidade da solicitação em relação à *SubscriptionId* do recurso que está sendo acessado. Uma solicitação de acesso A recursos de mais de um locatário nunca deve acontecer pelo usuário final. Isso pode acontecer em solicitações de serviço em um ambiente de vários locatários, no entanto. Por exemplo, o rastreador de pesquisa recebe alterações de conteúdo para todo o banco de dados de uma só vez. Isso geralmente envolve a consulta de sites de mais de um locatário em uma única solicitação de serviço, que é feita por motivos de eficiência.

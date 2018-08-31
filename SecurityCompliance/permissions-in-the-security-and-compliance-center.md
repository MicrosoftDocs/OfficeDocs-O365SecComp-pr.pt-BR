---
title: Permissões de segurança do Office 365 &amp; Centro de conformidade
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: overview
f1_keywords:
- ms.o365.cc.AdminRoleGroups
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: d10608af-7934-490a-818e-e68f17d0e9c1
description: A segurança do Office 365 &amp; Centro de conformidade permite conceder permissões para as pessoas que executam tarefas de conformidade, como o gerenciamento de dispositivos, prevenção de perda de dados, eDiscovery, retenção e assim por diante. Essas pessoas podem executar somente as tarefas que você explicitamente concede acesso a eles para. Para acessar a segurança &amp; Centro de conformidade, os usuários precisam ter um administrador global do Office 365 ou um membro de um ou mais segurança &amp; grupos de função do Centro de conformidade.
ms.openlocfilehash: e393bad7c3a57b0734835e56fcd781cc31327c18
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "23013425"
---
# <a name="permissions-in-the-office-365-security-amp-compliance-center"></a>Permissões de segurança do Office 365 &amp; Centro de conformidade

A segurança do Office 365 &amp; Centro de conformidade permite conceder permissões para as pessoas que executam tarefas de conformidade, como o gerenciamento de dispositivos, prevenção de perda de dados, eDiscovery, retenção e assim por diante. Essas pessoas podem executar somente as tarefas que você explicitamente concede acesso a eles para. Para acessar a segurança &amp; Centro de conformidade, os usuários precisam ter um administrador global do Office 365 ou um membro de um ou mais segurança &amp; grupos de função do Centro de conformidade.
  
Permissões na segurança &amp; Centro de conformidade baseiam-se no modelo de permissões de controle de acesso com base da função (RBAC). Este é o mesmo modelo de permissões que é usado pelo Exchange, portanto se você estiver familiarizado com o Exchange, concedendo permissões na segurança &amp; Centro de conformidade será muito similar. É importante lembrar, no entanto, essa função Exchange grupos e segurança &amp; grupos de função do Centro de conformidade não compartilhem permissões ou associação. Embora os dois tenham um grupo de funções de gerenciamento da organização, eles não são os mesmos. As permissões que eles conceder e os membros dos grupos de função, são diferentes. Há uma lista de segurança &amp; abaixo grupos de função do Centro de conformidade.
  
![Permissões de página no Office 365 Security &amp; Centro de conformidade](media/992c20ca-e82e-497c-9c8d-6fab212deb80.png)
  
## <a name="relationship-of-members-roles-and-role-groups"></a>Relação de membros, funções e grupos de função

Uma **função** concede permissões para realizar um conjunto de tarefas; por exemplo, a função de Gerenciamento de Casos permite que as pessoas trabalhem em casos de Descoberta Eletrônica. 
  
Um **grupo de função** é um conjunto de funções que permite que as pessoas a realizar suas tarefas entre a segurança &amp; Centro de conformidade; Por exemplo, o grupo de funções de administrador de conformidade inclui as funções de gerenciamento de casos, pesquisa de conteúdo e configuração da organização (além de outras pessoas), porque alguém que seja um administrador de conformidade terá permissões para essas tarefas executar suas funções. 
  
A segurança &amp; Centro de conformidade inclui os grupos de função padrão para as tarefas mais comuns e a funções que você precisará atribuir pessoas. Recomendamos que você simplesmente adicionando usuários individuais como **membros** a grupos de funções a padrão. 
  
![Diagrama que mostra a relação de grupos de funções para membros e funções](media/2a16d200-968c-4755-98ec-f1862d58cb8b.png)
  
Você pode editar ou excluir os grupos de função existente, mas não recomendamos isso. Em vez de um grupo de funções padrão de edição, você pode copiá-lo, modificá-lo e depois salvá-lo com um nome diferente.
  
## <a name="permissions-needed-to-use-features-in-the-security-amp-compliance-center"></a>Permissões necessárias para usar os recursos na segurança &amp; Centro de conformidade

A tabela a seguir lista os grupos de função padrão que estão disponíveis na segurança &amp; Centro de conformidade. Para conceder permissões a um usuário para executar uma tarefa de conformidade, adicioná-los para a segurança adequada &amp; grupo de funções do Centro de conformidade.
  
Gerenciando permissões na segurança &amp; Centro de conformidade somente fornece aos usuários acesso os recursos de conformidade que estão disponíveis dentro de segurança &amp; Centro de conformidade em si. Se você deseja conceder permissões para outros recursos de conformidade que não estão na segurança &amp; Centro de conformidade, como regras de transporte do Exchange, você precisará usar o Centro de administração do Exchange.
  
Para ver como conceder acesso à segurança &amp; Centro de conformidade, check-out de [Conceder aos usuários acesso ao centro de administração de conformidade do Office 365](grant-access-to-the-security-and-compliance-center.md).
  
|**Grupo de função**|**Descrição**|
|:-----|:-----|
|**Administrador de conformidade** <sup>1</sup> <br/> |Os membros podem gerenciar configurações para o gerenciamento de dispositivos, prevenção de perda de dados, relatórios e preservação.  <br/> |
|**Gerente de Descoberta Eletrônica** <br/> | Os membros podem realizar pesquisas e colocar bloqueios em caixas de correio, sites do SharePoint Online e locais do OneDrive for Business. Os membros também podem criar e gerenciar ocorrências de Descoberta Eletrônica, adicionar e remover membros de uma ocorrência, criar e editar Pesquisas de Conteúdo associadas a uma ocorrência.<br/>  Um Administrador de Descoberta Eletrônica é um membro do grupo de função de Gerente de Descoberta Eletrônica que recebeu permissões adicionais. Um Administrador de Descoberta Eletrônica pode:<br/>  Visualizar todos os casos de Descoberta Eletrônica na sua organização.  <br/>  Gerenciar qualquer ocorrência de Descoberta Eletrônica após adicionarem a si mesmos como membro da ocorrência.  <br/>  Acesso avançadas do Office 365 eDiscovery. Isso ocorre porque os administradores de eDiscovery são automaticamente adicionados como administradores no eDiscovery avançado. Observe que você precisa ser um administrador na segurança do eDiscovery &amp; Centro de conformidade para acessar o eDiscovery avançado. Para obter mais informações sobre como tornar um usuário administrador de eDiscovery, consulte [casos de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade](https://go.microsoft.com/fwlink/p/?LinkId=780738).<br/> Se você deseja conceder a um usuário privilégios administrativos no eDiscovery avançado, mas não quer para torná-los uma administrador de descoberta eletrônica na segurança &amp; Centro de conformidade, você pode adicioná-los ao grupo de função de Gerenciador de descoberta eletrônica e adicioná-lo como um administrador no EDiscovery avançado. Para obter instruções, consulte [Configurar usuários e casos de eDiscovery avançadas do Office 365](https://go.microsoft.com/fwlink/p/?LinkId=780696).           |
|**Gerenciamento da organização** <sup>1</sup> <br/> |Os membros podem controlar permissões para acessar recursos na segurança &amp; Centro de conformidade e também gerenciar configurações para o gerenciamento de dispositivos, prevenção de perda de dados, relatórios e preservação.  <br/> Observe que, para que um usuário que não seja um administrador global para ver a lista de dispositivos gerenciados por MDM para o Office 365 e executar ações nesses dispositivos, como retirada de um dispositivo do MDM para o Office 365, o usuário deve ser um administrador do Exchange.  <br/> Administradores globais do Office 365 são automaticamente adicionados como membros desse grupo de função.           |
|**Gerenciamento de Registros** <br/> |Os membros podem gerenciar e dispor o conteúdo de registro.  <br/> |
|**Revisor** <br/> |Membros só podem exibir a lista de ocorrências na página de casos de eDiscovery na segurança &amp; Centro de conformidade. Eles não podem criar, abrir ou gerenciar um caso de eDiscovery. A principal finalidade deste grupo de função é permitir que os membros da exibição e acesso caso dados no eDiscovery avançado.  <br/> Esse grupo de função tem as permissões mais restritivas relacionadas a Descoberta Eletrônica.  <br/> |
|**Administrador de segurança** <br/> |A associação no grupo de função é sincronizada entre serviços e gerenciada centralmente. Este grupo de função não é gerenciável através dos portais de administrador. Os membros deste grupo de função podem incluir administradores cross-service, bem como grupos de parceiros externos e o Microsoft Support. Por padrão, esse grupo não é possível atribuir qualquer funções. No entanto, ela será um membro dos grupos de função de administradores de segurança e herdarão as capacidades desse grupo de função.  <br/> Todas as permissões de somente leitura de função de leitor de segurança, além de um número de permissões administrativas adicionais para os mesmos serviços: proteção de informações do Windows Azure, centro de proteção de identidade, gerenciamento de identidade privilegiada, Monitor Office 365 Service Integridade e segurança do Office 365 &amp; Centro de conformidade.  <br/> |
|**Leitor de segurança** <br/> |Os membros têm acesso somente leitura para um número de recursos de segurança do Centro de proteção de identidade, gerenciamento de identidade privilegiada, integridade do serviço do Monitor Office 365 e segurança do Office 365 &amp; Centro de conformidade.  <br/> A associação no grupo de função é sincronizada entre serviços e gerenciada centralmente. Este grupo de função não é gerenciável através dos portais de administrador. Os membros deste grupo de função podem incluir administradores cross-service, bem como grupos de parceiros externos e o Microsoft Support. Por padrão, esse grupo não é possível atribuir qualquer funções. No entanto, ela será um membro dos grupos de função Leitor de segurança e herdarão as capacidades desse grupo de função.  <br/> |
|**Usuário da Garantia do Serviço** <br/> |Os membros podem acessar a seção de garantia de serviço no Office 365 Security &amp; Centro de conformidade. Garantia de serviço fornece relatórios e documentos que descrevem práticas de segurança da Microsoft para os dados de cliente que estão armazenados no Office 365. Ele também fornece relatórios de auditoria de terceiros independente sobre o Office 365. Para obter mais informações, consulte [pessoal assurance no Office 365 Security &amp; Centro de conformidade](http://go.microsoft.com/fwlink/p/?LinkID=717765).<br/> |
|**Análise de supervisão** <br/> |Os membros podem criar e gerenciar as políticas que definem qual comunicações estão sujeitos a revisão em uma organização. Para obter mais informações, consulte [Configure supervisão analisar políticas para sua organização](configure-supervision-policies.md).<br/> |
   
> [!NOTE]
> <sup>1</sup> este grupo de função não atribuir membros as permissões necessárias para pesquisar o log de auditoria do Office 365 ou para usar todos os relatórios que podem incluir dados do Exchange, como os relatórios DLP ou ATP. Para pesquisar o log de auditoria ou exibir todos os relatórios, um usuário deve ter permissões no Exchange Online. Isso ocorre porque o cmdlet subjacente usado para pesquisar o log de auditoria é um cmdlet do Exchange Online. Os administradores globais do Office 365 podem pesquisar o log de auditoria e exibir todos os relatórios, pois são automaticamente adicionados como membros do grupo de funções de gerenciamento da organização no Exchange Online. Para obter mais informações, consulte [Pesquisar o log de auditoria de segurança do Office 365 &amp; Centro de conformidade](https://go.microsoft.com/fwlink/p/?LinkID=708432). 
  


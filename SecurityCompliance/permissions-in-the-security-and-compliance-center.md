---
title: Permissões no centro de conformidade de &amp; segurança do Office 365
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: overview
f1_keywords:
- ms.o365.cc.AdminRoleGroups
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: d10608af-7934-490a-818e-e68f17d0e9c1
description: O centro de conformidade &amp; de segurança do Office 365 permite que você conceda permissões a pessoas que executam tarefas de conformidade, como gerenciamento de dispositivos, prevenção de perda de dados, eDiscovery, retenção e assim por diante. Essas pessoas podem executar apenas as tarefas às quais você concede explicitamente o acesso. Para acessar o centro &amp; de conformidade de segurança, os usuários precisam ser um administrador global do Office 365 ou um membro de um &amp; ou mais grupos de funções do centro de conformidade de segurança.
ms.openlocfilehash: 3ff5583a0a4f9dcabcc1b7d676593b7c6eb0bbba
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30223500"
---
# <a name="permissions-in-the-office-365-security-amp-compliance-center"></a>Permissões no centro de conformidade de &amp; segurança do Office 365

O centro de conformidade &amp; de segurança do Office 365 permite que você conceda permissões a pessoas que executam tarefas de conformidade, como gerenciamento de dispositivos, prevenção de perda de dados, eDiscovery, retenção e assim por diante. Essas pessoas podem executar apenas as tarefas às quais você concede explicitamente o acesso. Para acessar o centro &amp; de conformidade de segurança, os usuários precisam ser um administrador global do Office 365 ou um membro de um &amp; ou mais grupos de funções do centro de conformidade de segurança.
  
As permissões no centro &amp; de conformidade de segurança baseiam-se no modelo de permissões RBAC (controle de acesso baseado em função). Este é o mesmo modelo de permissões usado pelo Exchange, portanto, se você estiver familiarizado com o Exchange, conceder permissões no centro de &amp; conformidade de segurança serão muito semelhantes. No entanto, é importante lembrar que os grupos de função do Exchange &amp; e os grupos de função do centro de conformidade de segurança não compartilham associações ou permissões. Embora ambos tenham um grupo de função de gerenciamento da organização, eles não são os mesmos. As permissões concedidas e os membros dos grupos de função são diferentes. Há uma lista de grupos de &amp; funções do centro de conformidade de segurança abaixo.
  
![Página de permissões no centro de conformidade &amp; de segurança do Office 365](media/992c20ca-e82e-497c-9c8d-6fab212deb80.png)
  
## <a name="relationship-of-members-roles-and-role-groups"></a>Relação de membros, funções e grupos de função

Uma **função** concede permissões para realizar um conjunto de tarefas; por exemplo, a função de Gerenciamento de Casos permite que as pessoas trabalhem em casos de Descoberta Eletrônica. 
  
Um **grupo de função** é um conjunto de funções que permite que as pessoas realizem seu &amp; trabalho no centro de conformidade de segurança; por exemplo, o grupo de funções de administrador de conformidade inclui as funções para gerenciamento de casos, pesquisa de conteúdo e configuração de organização (mais outros) porque alguém que é um administrador de conformidade precisará das permissões para que essas tarefas realizem seu trabalho. 
  
O centro &amp; de conformidade de segurança inclui grupos de função padrão para as tarefas e funções mais comuns às quais você precisará atribuir pessoas. Recomendamos simplesmente adicionar usuários individuais como **Membros** aos grupos de função padrão. 
  
![Diagrama que mostra a relação de grupos de funções para membros e funções](media/2a16d200-968c-4755-98ec-f1862d58cb8b.png)
  
Você pode editar ou excluir os grupos de função existentes, mas não recomendamos isso. Em vez de editar um grupo de função padrão, você pode copiá-lo, modificá-lo e salvá-lo com um nome diferente.
  
## <a name="permissions-needed-to-use-features-in-the-security-amp-compliance-center"></a>Permissões necessárias para usar recursos no centro de &amp; conformidade de segurança

A tabela a seguir lista os grupos de função padrão que estão disponíveis no &amp; centro de conformidade de segurança. Para conceder permissões a um usuário para executar uma tarefa de conformidade, adicione-os ao grupo &amp; de função centro de conformidade de segurança apropriado.
  
O gerenciamento de permissões no &amp; centro de conformidade de segurança fornece aos usuários acesso aos recursos de conformidade disponíveis no próprio &amp; centro de conformidade de segurança. Se quiser conceder permissões a outros recursos de conformidade que não estão no centro de &amp; conformidade de segurança, como regras de transporte do Exchange, você precisará usar o centro de administração do Exchange.
  
Para ver como conceder acesso ao centro de conformidade &amp; de segurança, confira [conceder aos usuários acesso ao centro de administração de conformidade do Office 365](grant-access-to-the-security-and-compliance-center.md).
  
|**Grupo de função**|**Descrição**|
|:-----|:-----|
|**Administrador de conformidade** <sup>1</sup> <br/> |Os membros podem gerenciar configurações de gerenciamento de dispositivos, prevenção contra perda de dados, relatórios e preservação.  <br/> |
|**Gerente de Descoberta Eletrônica** <br/> | Os membros podem executar pesquisas e colocar bloqueios em caixas de correio, sites do SharePoint Online e locais do OneDrive for Business. Os membros também podem criar e gerenciar ocorrências de descoberta eletrônica, adicionar e remover membros a uma ocorrência, criar e editar pesquisas de conteúdo associadas a uma ocorrência e acessar dados de ocorrências na descoberta eletrônica avançada do Office 365.<br/><br/>Um administrador de descoberta eletrônica é membro do grupo de funções Gerenciador de descoberta eletrônica que recebeu permissões adicionais. Além das tarefas que um gerente de descoberta eletrônica pode executar, um administrador de descoberta eletrônica pode:<br/><br/>  • Exibir todos os casos de descoberta eletrônica na organização.  <br/>  • Gerencie qualquer caso de descoberta eletrônica após eles se adicionarem como um membro do caso.  <br/><br/>A principal diferença entre um gerente de descoberta eletrônica e um administrador de descoberta eletrônica é que um admininstrator de descoberta eletrônica pode acessar todas as ocorrências listadas na &amp; página ocorrências de **descoberta eletrônica** no centro de conformidade de segurança. Um gerente de descoberta eletrônica só pode acessar os casos em que eles criaram ou em que eles são membros.  Para obter mais informações sobre como tornar um usuário administrador de descoberta eletrônica, confira [atribuir permissões de descoberta &amp; eletrônica no centro de conformidade de segurança do Office 365](assign-ediscovery-permissions.md).<br/>           |
|**Gerenciamento da organização** <sup>1</sup> <br/> |Os membros podem controlar as permissões para acessar recursos no &amp; centro de conformidade de segurança e também gerenciar configurações de gerenciamento de dispositivos, prevenção de perda de dados, relatórios e preservação.  <br/> Observe que, para um usuário que não seja um administrador global para ver a lista de dispositivos gerenciados pelo MDM para o Office 365 e realizar ações nesses dispositivos, como a desativação de um dispositivo de MDM para Office 365, o usuário deve ser um administrador do Exchange.  <br/> Os administradores globais do Office 365 são automaticamente adicionados como membros desse grupo de função.           |
|**Gerenciamento de Registros** <br/> |Os membros podem gerenciar e descartar o conteúdo do registro.  <br/> |
|**Revisor** <br/> |Os membros só podem exibir a lista de casos na página de ocorrências de descoberta &amp; eletrônica no centro de conformidade de segurança. Eles não podem criar, abrir ou gerenciar uma ocorrência de descoberta eletrônica. O principal objetivo desse grupo de função é permitir que os membros exibam e acessem os dados de caso na descoberta eletrônica avançada.  <br/> Esse grupo de função tem as permissões mais restritivas relacionadas a Descoberta Eletrônica.  <br/> |
|**Administrador de segurança** <br/> |Os membros desse grupo de função podem incluir administradores entre serviços, além de grupos de parceiros externos e suporte da Microsoft. Por padrão, não é possível atribuir nenhuma função a este grupo. No enTanto, ele será membro da função Administradores de segurança no Azure Active Directory e herdará os recursos dessa função. Para gerenciar permissões centralmente, faça alterações nessa função no centro de administração do Azure Active Directory-para obter mais informações, consulte [permissões de função de administrador no Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/directory-assign-admin-roles). Se você editar esse grupo de função no centro de conformidade do & de segurança, essas alterações só serão aplicadas ao centro de conformidade do & de segurança e não a nenhum outro serviço, enquanto as alterações feitas no centro de administração do Azure Active Directory afetarão todos os serviços.<br/> Todas as permissões somente leitura da função de leitor de segurança, além de várias permissões administrativas adicionais para os mesmos serviços: proteção de informações do Azure, centro de proteção de identidade, gerenciamento de identidade privilegiado, monitorar o serviço Office 365 Integridade e centro de conformidade de &amp; segurança do Office 365.  <br/> |
|**Leitor de segurança** <br/> |Os membros têm acesso somente leitura a vários recursos de segurança do centro de proteção de identidades, gerenciamento de identidade privilegiado, monitoramento da integridade do serviço do &amp; Office 365 e centro de conformidade de segurança do Office 365.  <br/> A associação a este grupo de funções é sincronizada de forma centralizada em serviços e gerenciada centralmente. Os membros desse grupo de função podem incluir administradores entre serviços, além de grupos de parceiros externos e suporte da Microsoft. Por padrão, não é possível atribuir nenhuma função a este grupo. No enTanto, ele será um membro da função de leitores de segurança no Azure Active Directory e herdará os recursos dessa função. Para gerenciar permissões centralmente, faça alterações nessa função no centro de administração do Azure Active Directory-para obter mais informações, consulte [permissões de função de administrador no Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/directory-assign-admin-roles). Se você editar esse grupo de função no centro de conformidade do & de segurança, essas alterações só serão aplicadas ao centro de conformidade do & de segurança e não a nenhum outro serviço, enquanto as alterações feitas no centro de administração do Azure Active Directory afetarão todos os serviços.<br/> |
|**Usuário da Garantia do Serviço** <br/> |Os membros podem acessar a seção de garantia de serviço no centro &amp; de conformidade de segurança do Office 365. O serviço Assurance fornece relatórios e documentos que descrevem as práticas de segurança da Microsoft para dados do cliente armazenados no Office 365. Ele também fornece relatórios de auditoria de terceiros independentes no Office 365. Para obter mais informações, consulte [Service Assurance no centro de conformidade &amp; de segurança do Office 365](http://go.microsoft.com/fwlink/p/?LinkID=717765).<br/> |
|**Análise de supervisão** <br/> |Os membros podem criar e gerenciar as políticas que definem quais comunicações estão sujeitas a revisar em uma organização. Para saber mais, confira [Configurar políticas de análise de supervisão para sua organização](configure-supervision-policies.md).<br/> |
   
> [!NOTE]
> <sup>1</sup> esse grupo de função não atribui aos membros as permissões necessárias para pesquisar o log de auditoria do Office 365 ou para usar qualquer relatório que possa incluir dados do Exchange, como os relatórios DLP ou ATP. Para pesquisar o log de auditoria ou exibir todos os relatórios, um usuário precisa receber permissões no Exchange Online. Isso ocorre porque o cmdlet subjacente usado para pesquisar o log de auditoria é um cmdlet do Exchange Online. Os administradores globais do Office 365 podem pesquisar o log de auditoria e exibir todos os relatórios, pois eles são automaticamente adicionados como membros do grupo de função gerenciamento da organização no Exchange Online. Para obter mais informações, consulte [Pesquisar o log de auditoria no centro de &amp; conformidade de segurança do Office 365](https://go.microsoft.com/fwlink/p/?LinkID=708432). 
  


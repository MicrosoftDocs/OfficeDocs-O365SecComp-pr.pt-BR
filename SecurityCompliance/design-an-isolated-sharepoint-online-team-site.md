---
title: Projetar um site de equipe do SharePoint Online isolado
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/15/2017
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Ent_O365
ms.custom: Ent_Solutions
ms.assetid: 775a4e9e-3135-4a48-b32f-bbdd9f2bd0aa
description: 'Resumo: Percorra o processo de design para sites de equipe isolados do SharePoint Online.'
ms.openlocfilehash: 19f030f5210fb6742098543ae91117a90d583242
ms.sourcegitcommit: 6122eb026c558a5126c40845e656fbb0c40cb32a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2019
ms.locfileid: "36053118"
---
# <a name="design-an-isolated-sharepoint-online-team-site"></a>Projetar um site de equipe do SharePoint Online isolado

 **Resumo:** Percorra o processo de design para sites de equipe isolados do SharePoint Online.
  
Este artigo orienta as principais decisões de design que você deve fazer antes de criar um site de equipe do SharePoint Online isolado.
  
## <a name="phase-1-determine-your-sharepoint-groups-and-permission-levels"></a>Fase 1: determinar seus grupos e níveis de permissão do SharePoint

Todos os sites de equipe do SharePoint Online por padrão são criados com os seguintes grupos do SharePoint:
  
- \<Membros do nome do site>
    
- \<nome do site> visitantes
    
- \<nome do site> proprietários
    
Esses grupos são separados dos grupos do Office 365 e do Azure Active Directory (AD) e são a base para atribuir permissões para os recursos do site.
  
O conjunto de permissões específicas que determina o que um membro de um grupo do SharePoint pode fazer em um site é um nível de permissão. Há três níveis de permissão por padrão para um site de equipe do SharePoint Online: editar, ler e controle total. A tabela a seguir mostra a correlação padrão de grupos do SharePoint e níveis de permissão atribuídos:
  
|**Grupo do SharePoint**|**Nível de permissão**|
|:-----|:-----|
|\<Membros do nome do site>  <br/> |Edit  <br/> |
|\<nome do site> visitantes  <br/> |Ler  <br/> |
|\<nome do site> proprietários  <br/> |Controle total  <br/> |
   
 Práticas **recomendadas:** Você pode criar grupos adicionais do SharePoint e níveis de permissão. No entanto, recomendamos o uso dos grupos e níveis de permissão padrão do SharePoint para seu site isolado do SharePoint Online.
  
Estes são os grupos e os níveis de permissão padrão do SharePoint.
  
![Os grupos e níveis de permissão padrão do SharePoint para um site do SharePoint Online.](media/3f892ab4-6479-42f0-a505-1ba0ef94b9c6.png)
  
## <a name="phase-2-assign-permissions-to-users-with-access-groups"></a>Fase 2: atribuir permissões a usuários com grupos de acesso

Você pode atribuir permissões aos usuários adicionando sua conta de usuário ou um grupo do Office 365 ou do Azure AD do qual a conta de usuário é membro, para os grupos do SharePoint. Depois de adicionada, as contas de usuário do Office 365, direta ou indiretamente, via Associação a um grupo do Office 365 ou do Azure AD, recebem o nível de permissão associado ao grupo do SharePoint.
  
Usando os grupos padrão do SharePoint como exemplo:
  
- Os membros do grupo ** \<nome do site> Membros** do SharePoint, que podem incluir contas de usuário e grupos, recebem o nível de permissão **Editar**
    
- Os membros do grupo ** \<nome do site> visitantes** do SharePoint, que podem incluir contas de usuário e grupos, recebem o nível de permissão de **leitura**
    
- Os membros do grupo ** \<nome do site> proprietários** do SharePoint, que podem incluir contas de usuário e grupos, recebem o nível de permissão **controle total**
    
 Práticas **recomendadas:** Embora você possa gerenciar permissões por meio de contas de usuário individuais, recomendamos usar um único grupo do Azure AD, conhecido como grupo de acesso, em vez disso. Isso simplifica o gerenciamento de permissões por meio da associação no grupo de acesso, em vez de gerenciar a lista de contas de usuário para cada grupo do SharePoint.
  
Os grupos do Azure AD para Office 365 são diferentes dos grupos do Office 365. Os grupos do Azure AD aparecem no centro de administração do Microsoft 365 com o **tipo** definido como **segurança** e não têm um endereço de email. Os grupos do Azure AD podem ser gerenciados em:
  
- Serviços de Domínio Active Directory (AD DS)
    
    Estes são grupos que foram criados em sua infraestrutura do AD DS local e sincronizados com a sua assinatura do Office 365. No centro de administração do Microsoft 365, esses grupos têm **** um status **sincronizado com o Active Directory**.
    
- Office 365
    
    Estes são os grupos que foram criados usando o centro de administração do Microsoft 365, o portal do Azure ou o Microsoft PowerShell. No centro de administração do Microsoft 365, esses grupos têm um **status** de **nuvem**.
    
 Práticas **recomendadas:** Se você estiver usando o AD DS no local e estiver sincronizando com sua assinatura do Office 365, realize o gerenciamento de usuário e de grupo com o AD DS.
  
Para sites de equipe isolados do SharePoint Online, a estrutura de grupo recomendada é semelhante a esta:
  
|**Grupo do SharePoint**|**Grupo de acesso baseado no AD do Azure**|**Nível de permissão**|
|:-----|:-----|:-----|
|\<Membros do nome do site>  <br/> |\<Membros do nome do site>  <br/> |Edit  <br/> |
|\<nome do site> visitantes  <br/> |\<Visualizadores de nome de site>  <br/> |Ler  <br/> |
|\<nome do site> proprietários  <br/> |\<nome do site> administradores  <br/> |Controle total  <br/> |
   
 Práticas **recomendadas:** Embora você possa usar os grupos do Office 365 ou do Azure AD como membros de grupos do SharePoint, recomendamos usar os grupos do Azure AD. Os grupos do Azure AD, gerenciados pelo AD DS ou pelo Office 365, oferecem mais flexibilidade para usar grupos aninhados para atribuir permissões.
  
Estes são os grupos padrão do SharePoint configurados para usar grupos de acesso baseados no Azure AD.
  
![Usando grupos do Access como membros de grupos de sites padrão do SharePoint Online.](media/50a76328-ae69-483e-9029-ac4e7357b5ef.png)
  
Ao projetar os três grupos de acesso, tenha em mente o seguinte:
  
- Deve haver apenas alguns membros no grupo nome do ** \<site> administradores** de acesso, correspondendo a um pequeno número de administradores do SharePoint Online que estão gerenciando o site de equipe.
    
- A maioria dos membros do site estão no ** \<nome do site> Membros** ou ** \<nome do site>** os grupos de acesso do visualizador. Como os membros do site no grupo ** \<nome do site> Members** Access têm a capacidade de excluir ou modificar recursos no site, considere cuidadosamente sua associação. Quando estiver em dúvida, adicione o membro do site ao grupo de acesso de ** \<nome do site> visualizadores** .
    
Veja um exemplo de grupos do SharePoint e grupos de acesso para um site isolado chamado projeto x.
  
![Um exemplo de uso de grupos de acesso para um site do SharePoint Online chamado projeto x.](media/13afe542-9ffd-4671-9f48-210a0e2a502a.png)
  
## <a name="phase-3-use-nested-azure-ad-groups"></a>Fase 3: usar grupos aninhados do Azure AD

Para um projeto confinado a um pequeno número de pessoas, um único nível de grupos de acesso baseado no AD do Azure adicionado aos grupos do SharePoint do site se ajustará à maioria dos cenários. No entanto, se você tiver um grande número de pessoas e essas pessoas já forem membros dos grupos do Azure AD estabelecidos, poderá atribuir permissões do SharePoint com mais facilidade usando grupos aninhados ou grupos que contenham outros grupos como membros.
  
Por exemplo, você deseja criar um site de equipe isolado do SharePoint Online para colaboração entre os executivos dos departamentos de vendas, marketing, engenharia, legal e de suporte e esses departamentos que já têm seus próprios grupos com conta de usuário executivo Academy. Em vez de criar um novo grupo para os novos membros do site e colocar todas as contas de usuário executivo individuais, coloque os grupos executivos existentes para cada departamento do novo grupo.
  
 Se você estiver compartilhando uma assinatura do Office 365 entre várias organizações, pode ser difícil gerenciar um único nível de associação de grupo para um site isolado para uma organização devido ao número enorme de contas de usuário. Nesse caso, você pode usar grupos aninhados do Azure AD para cada organização que contenha os grupos dentro de suas organizações para gerenciar as permissões.
  
Para usar grupos aninhados do Azure AD:
  
1. Identifique ou crie os grupos do Azure AD que conterá as contas de usuário e adicione as contas de usuário apropriadas como membros.
    
2. Crie o grupo de acesso baseado em AD do Azure de contêiner que conterá os outros grupos do Azure AD e adicione esses grupos como membros.
    
3.  Para o nível de acesso apropriado para o grupo de acesso de contêiner, identifique o grupo do SharePoint e o nível de permissão correspondente.
    
> [!NOTE]
> Não é possível usar grupos aninhados do Office 365. 
  
Veja um exemplo de grupos aninhados do Azure AD para o grupo de acesso de membros do projeto x.
  
![Um exemplo de uso de grupos de acesso aninhados para o grupo de acesso de membros do site do projeto x.](media/2abca710-bf9e-4ce8-9bcd-a8e128264fb1.png)
  
Como todas as contas de usuário nas equipes de pesquisa, engenharia e projetos líderes do projeto devem ser membros do site, é mais fácil adicionar seus grupos do Azure AD ao grupo de acesso de membros do projeto x.
  
## <a name="next-step"></a>Próxima etapa

Quando estiver pronto para criar e configurar um site isolado em produção, consulte [implantar um site de equipe isolado do SharePoint Online](deploy-an-isolated-sharepoint-online-team-site.md).
  
## <a name="see-also"></a>Confira também

[Sites de equipe do SharePoint Online isolados](isolated-sharepoint-online-team-sites.md)
  
[Gerenciar um site de equipe do SharePoint Online isolado](manage-an-isolated-sharepoint-online-team-site.md)

[Implantar um site de equipe do SharePoint Online isolado](deploy-an-isolated-sharepoint-online-team-site.md)




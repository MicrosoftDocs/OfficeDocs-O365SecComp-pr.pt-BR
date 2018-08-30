---
title: Configurar usuários e casos na Descoberta Eletrônica Avançada do Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 60ffd80b-4376-419d-b6e4-a72029b9907c
description: 'Saiba como configurar funções de usuário, crie casos e atribuir usuários a casos de eDiscovery avançadas do Office 365.  '
ms.openlocfilehash: 49f76b415d86035cecafc19c23b36c413f7576e5
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524312"
---
# <a name="set-up-users-and-cases-in-office-365-advanced-ediscovery"></a><span data-ttu-id="1a10a-103">Configurar usuários e casos na Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="1a10a-103">Set up users and cases in Office 365 Advanced eDiscovery</span></span>

<span data-ttu-id="1a10a-104">Este tópico descreve como configurar usuários e casos de eDiscovery avançadas do Office 365.</span><span class="sxs-lookup"><span data-stu-id="1a10a-104">This topic describes how to set up users and cases for Office 365 Advanced eDiscovery.</span></span>
  
> [!NOTE]
> <span data-ttu-id="1a10a-p101">EDiscovery Avançado requer um Office 365 E3 com o complemento de conformidade avançadas ou uma assinatura E5 para sua organização. Se você não tiver que plano e quiser tentar eDiscovery avançado, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="1a10a-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="prerequisites"></a><span data-ttu-id="1a10a-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="1a10a-107">Prerequisites</span></span>

<span data-ttu-id="1a10a-108">Antes de configurar os usuários no eDiscovery avançado e casos, é necessário o seguinte:</span><span class="sxs-lookup"><span data-stu-id="1a10a-108">Before setting up cases and users in Advanced eDiscovery, the following is required:</span></span>
  
- <span data-ttu-id="1a10a-p102">Para analisar dados de um usuário usando o eDiscovery avançado, o usuário (o de responsáveis dos dados) deve ser atribuído uma licença do Office 365 E5. Como alternativa, os usuários com uma licença do Office 365 E1 ou E3 podem ser atribuídos uma licença autônoma de eDiscovery avançado. Os administradores e oficiais de conformidade que estão atribuídos ao casos e usam o eDiscovery avançada para analisar dados não precisam de uma licença E5.</span><span class="sxs-lookup"><span data-stu-id="1a10a-p102">To analyze a user's data using Advanced eDiscovery, the user (the custodian of the data) must be assigned an Office 365 E5 license. Alternatively, users with an Office 365 E1 or E3 license can be assigned an Advanced eDiscovery standalone license. Administrators and compliance officers who are assigned to cases and use Advanced eDiscovery to analyze data don't need an E5 license.</span></span> 
    
- <span data-ttu-id="1a10a-p103">Você precisa ser membro do grupo de função do Gerenciador de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade para criar um caso de eDiscovery e adicionar membros a ela. Adicionar-se ao grupo de função de Gerenciador de descoberta eletrônica em Security &amp; Centro de conformidade, você precisa ser um administrador global na sua organização do Office 365. Se você não for um administrador global, você terá que pedir um administrador global para adicioná-lo ao grupo de função de Gerenciador de descoberta eletrônica. Para obter mais informações, consulte:</span><span class="sxs-lookup"><span data-stu-id="1a10a-p103">You have to be a member of the eDiscovery Manager role group in the Office 365 Security &amp; Compliance Center to create an eDiscovery case and add members to it. To add yourself to the eDiscovery Manager role group in Security &amp; Compliance Center, you have to be a global administrator in your Office 365 organization. If you're not a global administrator, you 'll have to ask a global administrator to add you to the eDiscovery Manager role group. For more information, see:</span></span>
    
  - [<span data-ttu-id="1a10a-116">Permissões de segurança do Office 365 &amp; Centro de conformidade</span><span class="sxs-lookup"><span data-stu-id="1a10a-116">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
    
  - [<span data-ttu-id="1a10a-117">Atribuir permissões de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade</span><span class="sxs-lookup"><span data-stu-id="1a10a-117">Assign eDiscovery permissions in the Office‍ 365 Security &amp; Compliance Center</span></span>](assign-ediscovery-permissions.md)
    
## <a name="step-1-assign-users-ediscovery-permissions"></a><span data-ttu-id="1a10a-118">Etapa 1: Atribuir aos usuários permissões de descoberta eletrônica</span><span class="sxs-lookup"><span data-stu-id="1a10a-118">Step 1: Assign users eDiscovery permissions</span></span>

<span data-ttu-id="1a10a-p104">A primeira etapa é atribuir as permissões de requisito na segurança de usuários &amp; Centro de conformidade para que eles possam me adicionada como um membro de um caso de eDiscovery. Depois que um usuário é adicionado como um membro de um caso na segurança &amp; Centro de conformidade, eles serão capazes de acessar o caso da eDiscovery avançado.</span><span class="sxs-lookup"><span data-stu-id="1a10a-p104">The first step is to assign users the requirement permissions in the Security &amp; Compliance Center so that they can me added as a member of an eDiscovery case. After a user is added as a member of a case in the Security &amp; Compliance Center, they'll be able to access the case in Advanced eDiscovery.</span></span>
  
<span data-ttu-id="1a10a-121">Para atribuir um usuário as permissões necessárias para que eles podem ser adicionados como um membro de um caso de eDiscovery, consulte a etapa 1 em [casos de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade](ediscovery-cases.md#step-1-assign-ediscovery-permissions-to-potential-case-members).</span><span class="sxs-lookup"><span data-stu-id="1a10a-121">To assign a user the necessary permissions so they can be added as a member of an eDiscovery case, see Step 1 in [eDiscovery cases in the Office 365 Security &amp; Compliance Center](ediscovery-cases.md#step-1-assign-ediscovery-permissions-to-potential-case-members).</span></span>
  
## <a name="step-2-create-an-ediscovery-case-and-add-members"></a><span data-ttu-id="1a10a-122">Etapa 2: Criar um caso de eDiscovery e adicionar membros</span><span class="sxs-lookup"><span data-stu-id="1a10a-122">Step 2: Create an eDiscovery case and add members</span></span>

<span data-ttu-id="1a10a-p105">A próxima etapa é criar um novo caso de descoberta eletrônica na segurança &amp; Centro de conformidade e adicionar membros. Membros do caso será capazes de acessar o caso da eDiscovery avançado.</span><span class="sxs-lookup"><span data-stu-id="1a10a-p105">The next step is to create a new eDiscovery case in the Security &amp; Compliance Center and add members. Members of the case will then be able to access the case in Advanced eDiscovery.</span></span>
  
1. <span data-ttu-id="1a10a-125">Para criar um novo caso de descoberta eletrônica, consulte a etapa 2 no [casos de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade](ediscovery-cases.md#step-2-create-a-new-case).</span><span class="sxs-lookup"><span data-stu-id="1a10a-125">To create a new eDiscovery case, see Step 2 in [eDiscovery cases in the Office 365 Security &amp; Compliance Center](ediscovery-cases.md#step-2-create-a-new-case).</span></span>
    
2. <span data-ttu-id="1a10a-126">Para adicionar membros a um caso de descoberta eletrônica, consulte a etapa 3 em [casos de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade](ediscovery-cases.md#step-3-add-members-to-a-case)</span><span class="sxs-lookup"><span data-stu-id="1a10a-126">To add members to an eDiscovery case, see Step 3 in [eDiscovery cases in the Office 365 Security &amp; Compliance Center](ediscovery-cases.md#step-3-add-members-to-a-case)</span></span>
    
## <a name="step-3-go-a-case-in-advanced-ediscovery"></a><span data-ttu-id="1a10a-127">Etapa 3: Ir um caso de eDiscovery avançado</span><span class="sxs-lookup"><span data-stu-id="1a10a-127">Step 3: Go a case in Advanced eDiscovery</span></span>

<span data-ttu-id="1a10a-p106">Depois de criar um caso de eDiscovery e adicionar membros, você (ou qualquer membro do caso) pode acessar o caso correspondente no eDiscovery avançado. Para acessar um caso de descoberta eletrônica avançada, consulte Step 8 em [casos de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade](ediscovery-cases.md#step-8-go-to-the-case-in-advanced-ediscovery).</span><span class="sxs-lookup"><span data-stu-id="1a10a-p106">After you create an eDiscovery case and add members, you (or any member of the case) can access the corresponding case in Advanced eDiscovery. To access a case in Advanced eDiscovery, see Step 8 in [eDiscovery cases in the Office 365 Security &amp; Compliance Center](ediscovery-cases.md#step-8-go-to-the-case-in-advanced-ediscovery).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1a10a-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a10a-130">See also</span></span>

[<span data-ttu-id="1a10a-131">Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="1a10a-131">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="1a10a-132">Preparar os dados</span><span class="sxs-lookup"><span data-stu-id="1a10a-132">Preparing data</span></span>](prepare-data-for-advanced-ediscovery.md)
  
[<span data-ttu-id="1a10a-133">Acesso e funções de usuário</span><span class="sxs-lookup"><span data-stu-id="1a10a-133">User roles and access</span></span>](user-roles-and-access-in-advanced-ediscovery.md)


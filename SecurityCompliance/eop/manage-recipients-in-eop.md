---
title: Gerenciar destinatários no EOP
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 2921f544-8257-4bae-8e3a-ce9250e9f162
description: O Microsoft Proteção do Exchange Online (EOP) oferece várias maneiras de gerenciar seus destinatários de email. Como administrador, você pode executar determinadas tarefas de gerenciamento no Centro de administração do Exchange (EAC) ou usando o Windows PowerShell remoto, e verificar outras tarefas de gerenciamento executadas no Centro de administração do Microsoft Office 365.
ms.openlocfilehash: 0159604eaa4e021d9ccef544306e8b274af11f18
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027568"
---
# <a name="manage-recipients-in-eop"></a><span data-ttu-id="082ac-104">Gerenciar destinatários no EOP</span><span class="sxs-lookup"><span data-stu-id="082ac-104">Manage recipients in EOP</span></span>

<span data-ttu-id="082ac-p102">O Microsoft Proteção do Exchange Online (EOP) oferece várias maneiras de gerenciar seus destinatários de email. Como administrador, você pode executar determinadas tarefas de gerenciamento no Centro de administração do Exchange (EAC) ou usando o Windows PowerShell remoto, e verificar outras tarefas de gerenciamento executadas no Centro de administração do Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="082ac-p102">Microsoft Exchange Online Protection (EOP) offers several ways to manage your mail recipients. As an administrator, you can perform certain management tasks within the Exchange admin center (EAC) or using remote Windows PowerShell, and verify other management tasks performed in the Microsoft Office 365 admin center.</span></span>
  
<span data-ttu-id="082ac-107">O EOP oferece suporte a estes três tipos de destinatários:</span><span class="sxs-lookup"><span data-stu-id="082ac-107">EOP supports the following types of recipients:</span></span>
  
- <span data-ttu-id="082ac-p103">**Usuários de email** Usuários de email são gerenciados de destinatários no seu EOP domínios. Esses destinatários tem credenciais de logon em sua organização do Office 365, mas eles têm endereços de email externo, que significa que suas caixas de correio do destinatários estão localizadas fora da sua organização em nuvem. Você pode adicionar usuários de email para que eles podem receber email e você também pode criar regras de transporte para usuários específicos. Você também pode atribuir funções a usuários de email em sua organização; os usuários com privilégios de grupo de função de gerenciamento podem acessar o Centro de administração do Exchange (EAC) e executar algumas tarefas de gerenciamento. Para saber mais sobre as funções de usuário e como atribuir funções de usuário no EOP, consulte [Gerenciar permissões de grupo de função administrador no EOP](manage-admin-role-group-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="082ac-p103">**Mail Users** Mail users are recipients in your EOP managed domains. These recipients have logon credentials in your Office 365 organization, but they have external email addresses, meaning that their recipient mailboxes are located outside of your cloud organization. You can add mail users so that they can receive mail and you can also create transport rules for specific users. You can also assign roles to mail users in your organization; users with management role group privileges can access the Exchange admin center (EAC) and perform certain management tasks. To learn more about user roles and how to assign user roles in EOP, see [Manage admin role group permissions in EOP](manage-admin-role-group-permissions-in-eop.md).</span></span>
    
    <span data-ttu-id="082ac-113">Para obter mais informações sobre o gerenciamento de usuários de email no EOP, consulte [Gerenciar usuários de email no EOP](manage-mail-users-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="082ac-113">For more information about managing mail users in EOP, see [Manage mail users in EOP](manage-mail-users-in-eop.md).</span></span>
    
- <span data-ttu-id="082ac-114">**Grupos** Os usuários de email podem ser agrupados em grupos de distribuição ou em grupos de segurança.</span><span class="sxs-lookup"><span data-stu-id="082ac-114">**Groups** Mail users can be grouped together into distribution groups or security groups.</span></span> 
    
    <span data-ttu-id="082ac-115">Para obter mais informações sobre o gerenciamento de grupos no EOP, consulte [Gerenciar grupos no EOP](manage-groups-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="082ac-115">For more information about managing groups in EOP, see [Manage groups in EOP](manage-groups-in-eop.md).</span></span>
    
<span data-ttu-id="082ac-p104">Procurando a versão do Exchange Online deste tópico? Consulte [Recipients in Exchange Online](http://technet.microsoft.com/library/50d16941-5cd7-435d-8715-e2b69f8410ab.aspx).</span><span class="sxs-lookup"><span data-stu-id="082ac-p104">Looking for the Exchange Online version of this topic? See [Recipients in Exchange Online](http://technet.microsoft.com/library/50d16941-5cd7-435d-8715-e2b69f8410ab.aspx).</span></span>
  
<span data-ttu-id="082ac-p105">Procurando a versão do Exchange Server deste tópico? Consulte [Recipients](http://technet.microsoft.com/library/40300ed4-85a5-463d-bb3a-cf787bd44e9d.aspx).</span><span class="sxs-lookup"><span data-stu-id="082ac-p105">Looking for the Exchange Server version of this topic? See [Recipients](http://technet.microsoft.com/library/40300ed4-85a5-463d-bb3a-cf787bd44e9d.aspx).</span></span>
  


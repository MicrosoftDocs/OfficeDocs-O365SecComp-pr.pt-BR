---
title: Gerenciar destinatários no EOP
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 2921f544-8257-4bae-8e3a-ce9250e9f162
description: O Microsoft Proteção do Exchange Online (EOP) oferece várias maneiras de gerenciar seus destinatários de email. Como administrador, você pode executar determinadas tarefas de gerenciamento no centro de administração do Exchange (Eat) ou usar o Windows PowerShell remoto e verificar outras tarefas de gerenciamento executadas no centro de administração do Microsoft 365.
ms.openlocfilehash: 1d9436cf02538ab5c69e0e68d20eda1af5b0a5cd
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32256609"
---
# <a name="manage-recipients-in-eop"></a><span data-ttu-id="b07fb-104">Gerenciar destinatários no EOP</span><span class="sxs-lookup"><span data-stu-id="b07fb-104">Manage recipients in EOP</span></span>

<span data-ttu-id="b07fb-105">O Microsoft Proteção do Exchange Online (EOP) oferece várias maneiras de gerenciar seus destinatários de email.</span><span class="sxs-lookup"><span data-stu-id="b07fb-105">Microsoft Exchange Online Protection (EOP) offers several ways to manage your mail recipients.</span></span> <span data-ttu-id="b07fb-106">Como administrador, você pode executar determinadas tarefas de gerenciamento no centro de administração do Exchange (Eat) ou usar o Windows PowerShell remoto e verificar outras tarefas de gerenciamento executadas no centro de administração do Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="b07fb-106">As an administrator, you can perform certain management tasks within the Exchange admin center (EAC) or using remote Windows PowerShell, and verify other management tasks performed in the Microsoft 365 admin center.</span></span>
  
<span data-ttu-id="b07fb-107">O EOP oferece suporte a estes três tipos de destinatários:</span><span class="sxs-lookup"><span data-stu-id="b07fb-107">EOP supports the following types of recipients:</span></span>
  
- <span data-ttu-id="b07fb-108">**Usuários de email** Os usuários de email são destinatários em seus domínios gerenciados do EOP.</span><span class="sxs-lookup"><span data-stu-id="b07fb-108">**Mail Users** Mail users are recipients in your EOP managed domains.</span></span> <span data-ttu-id="b07fb-109">Esses destinatários têm credenciais de logon na sua organização do Office 365, mas têm endereços de email externos, o que significa que suas caixas de correio de destinatário estão localizadas fora da sua organização em nuvem.</span><span class="sxs-lookup"><span data-stu-id="b07fb-109">These recipients have logon credentials in your Office 365 organization, but they have external email addresses, meaning that their recipient mailboxes are located outside of your cloud organization.</span></span> <span data-ttu-id="b07fb-110">Você pode adicionar usuários de email para que eles possam receber emails e também pode criar regras de fluxo de emails (também conhecidas como regras de transporte) para usuários específicos.</span><span class="sxs-lookup"><span data-stu-id="b07fb-110">You can add mail users so that they can receive mail and you can also create mail flow rules (also known as transport rules) for specific users.</span></span> <span data-ttu-id="b07fb-111">Você também pode atribuir funções aos usuários de email em sua organização; os usuários com privilégios de grupo de função de gerenciamento podem acessar o centro de administração do Exchange (Eat) e realizar determinadas tarefas de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="b07fb-111">You can also assign roles to mail users in your organization; users with management role group privileges can access the Exchange admin center (EAC) and perform certain management tasks.</span></span> <span data-ttu-id="b07fb-112">Para saber mais sobre as funções de usuário e como atribuir funções de usuário no EOP, confira [gerenciar permissões do grupo de funções de administrador no EOP](manage-admin-role-group-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="b07fb-112">To learn more about user roles and how to assign user roles in EOP, see [Manage admin role group permissions in EOP](manage-admin-role-group-permissions-in-eop.md).</span></span>
    
    <span data-ttu-id="b07fb-113">Para obter mais informações sobre o gerenciamento de usuários de email no EOP, consulte [Gerenciar usuários de email no EOP](manage-mail-users-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="b07fb-113">For more information about managing mail users in EOP, see [Manage mail users in EOP](manage-mail-users-in-eop.md).</span></span>
    
- <span data-ttu-id="b07fb-114">**Grupos** Os usuários de email podem ser agrupados em grupos de distribuição ou em grupos de segurança.</span><span class="sxs-lookup"><span data-stu-id="b07fb-114">**Groups** Mail users can be grouped together into distribution groups or security groups.</span></span> 
    
    <span data-ttu-id="b07fb-115">Para obter mais informações sobre o gerenciamento de grupos no EOP, consulte [Gerenciar grupos no EOP](manage-groups-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="b07fb-115">For more information about managing groups in EOP, see [Manage groups in EOP](manage-groups-in-eop.md).</span></span>
    
<span data-ttu-id="b07fb-p104">Procurando a versão do Exchange Online deste tópico? Consulte [Recipients in Exchange Online](http://technet.microsoft.com/library/50d16941-5cd7-435d-8715-e2b69f8410ab.aspx).</span><span class="sxs-lookup"><span data-stu-id="b07fb-p104">Looking for the Exchange Online version of this topic? See [Recipients in Exchange Online](http://technet.microsoft.com/library/50d16941-5cd7-435d-8715-e2b69f8410ab.aspx).</span></span>
  
<span data-ttu-id="b07fb-p105">Procurando a versão do Exchange Server deste tópico? Consulte [Recipients](http://technet.microsoft.com/library/40300ed4-85a5-463d-bb3a-cf787bd44e9d.aspx).</span><span class="sxs-lookup"><span data-stu-id="b07fb-p105">Looking for the Exchange Server version of this topic? See [Recipients](http://technet.microsoft.com/library/40300ed4-85a5-463d-bb3a-cf787bd44e9d.aspx).</span></span>
  


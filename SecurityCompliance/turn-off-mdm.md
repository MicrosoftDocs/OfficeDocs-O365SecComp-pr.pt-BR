---
title: Como desativar o gerenciamento de dispositivos móveis no Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/12/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- GPA150
- MET150
ms.assetid: 2709cafb-0a8b-44bc-8494-7e2fccfa2b19
description: Siga estas etapas para interromper as políticas MDM de sendo imposto para dispositivos móveis em sua organização do Office 365.
ms.openlocfilehash: 6b8f0036ed999b10263f5cc074df27175769e604
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272216"
---
# <a name="how-to-turn-off-mobile-device-management-in-office-365"></a><span data-ttu-id="45d8f-103">Como desativar o gerenciamento de dispositivos móveis no Office 365</span><span class="sxs-lookup"><span data-stu-id="45d8f-103">How to turn off Mobile Device Management in Office 365</span></span>

<span data-ttu-id="45d8f-104">Para desativar efetivamente MDM para o Office 365, você remove grupos de pessoas (definidos por grupos de segurança) através da política de gerenciamento de dispositivo ou remove as políticas em si.</span><span class="sxs-lookup"><span data-stu-id="45d8f-104">To effectively turn off MDM for Office 365, you remove groups of people (defined by security groups) from the device management policies, or remove the policies themselves.</span></span> 
  
- <span data-ttu-id="45d8f-105">Remova grupos de usuários, removendo os grupos de segurança do usuário através da política de dispositivo que você criou.</span><span class="sxs-lookup"><span data-stu-id="45d8f-105">Remove groups of users by removing user security groups from the device policies you've created.</span></span> 
    
- <span data-ttu-id="45d8f-106">Desabilite MDM para todas as pessoas, removendo todas as políticas de dispositivo MDM.</span><span class="sxs-lookup"><span data-stu-id="45d8f-106">Disable MDM for everyone by removing all MDM device policies.</span></span> 
    
<span data-ttu-id="45d8f-p101">Essas opções removerá imposição MDM para dispositivos em sua organização. Infelizmente, você não pode simplesmente "desprovisionar" MDM para o Office 365 depois de configurá-lo.</span><span class="sxs-lookup"><span data-stu-id="45d8f-p101">These options will remove MDM enforcement for devices in your organization. Unfortunately, you can't simply "unprovision" MDM for Office 365 after you've set it up.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="45d8f-p102">Lembre-se do impacto em dispositivos dos usuários quando você remove grupos de segurança do usuário de políticas ou remove as políticas em si. Por exemplo, email perfis e emails em cache podem ser removidos, dependendo do dispositivo. Consulte: [qual é o impacto das diretivas de segurança em tipos diferentes de dispositivos?](create-device-security-policies.md#what-is-the-impact-of-security-policies-on-different-device-types)</span><span class="sxs-lookup"><span data-stu-id="45d8f-p102">Be aware of the impact on users' devices when you remove user security groups from policies or remove the policies themselves. For example, email profiles and cached emails may be removed, depending on the device. See: [What is the impact of security policies on different device types?](create-device-security-policies.md#what-is-the-impact-of-security-policies-on-different-device-types)</span></span>
  
## <a name="remove-user-security-groups-from-mdm-device-policies"></a><span data-ttu-id="45d8f-112">Remover grupos de segurança do usuário de políticas de dispositivo do MDM</span><span class="sxs-lookup"><span data-stu-id="45d8f-112">Remove user security groups from MDM device policies</span></span>

1. <span data-ttu-id="45d8f-113">Vá para **segurança &amp; Centro de conformidade** \> **prevenção de perda de dados** \> **políticas de segurança de dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="45d8f-113">Go to **Security &amp; Compliance Center**\> **Data loss prevention** \> **Device security polices**.</span></span>
    
2. <span data-ttu-id="45d8f-114">Selecione uma política de dispositivo e, em seguida, clique em ![ícone Editar](media/O365-MDM-CreatePolicy-EditIcon.gif) **Editar política**.</span><span class="sxs-lookup"><span data-stu-id="45d8f-114">Select a device policy, and click ![Edit icon](media/O365-MDM-CreatePolicy-EditIcon.gif) **Edit policy**.</span></span>
    
3. <span data-ttu-id="45d8f-115">Em **implantação**, clique em **- Remove**.</span><span class="sxs-lookup"><span data-stu-id="45d8f-115">Under **Deployment**, click **- Remove**.</span></span>
    
    <span data-ttu-id="45d8f-116">Em **grupos**, selecione um grupo de segurança.</span><span class="sxs-lookup"><span data-stu-id="45d8f-116">Under **Groups**, select a security group.</span></span>
    
4.  <span data-ttu-id="45d8f-117">Clique em **Remover**.</span><span class="sxs-lookup"><span data-stu-id="45d8f-117">Click **Remove**.</span></span>
    
5. <span data-ttu-id="45d8f-118">Clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="45d8f-118">Click **Save**.</span></span>
    
## <a name="remove-mdm-device-policies"></a><span data-ttu-id="45d8f-119">Remover políticas de dispositivo do MDM</span><span class="sxs-lookup"><span data-stu-id="45d8f-119">Remove MDM device policies</span></span>

1. <span data-ttu-id="45d8f-120">Vá para **segurança &amp; Centro de conformidade** \> **diretivas de segurança** \> **diretivas de segurança de dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="45d8f-120">Go to **Security &amp; Compliance Center**\> **Security policies** \> **Device security policies**.</span></span>
    
2. <span data-ttu-id="45d8f-p103">Selecione uma política de dispositivo e clique em ![imagem da Lixeira pode ícone. ](media/b8bfa783-c0b5-46d9-9570-8a385088e8fe.png) **Excluir a política**.</span><span class="sxs-lookup"><span data-stu-id="45d8f-p103">Select a device policy, and then click ![Image of the trash can icon.](media/b8bfa783-c0b5-46d9-9570-8a385088e8fe.png) **Delete policy**.</span></span>
    
3. <span data-ttu-id="45d8f-123">Na caixa de diálogo de **Aviso** , clique em **Sim**.</span><span class="sxs-lookup"><span data-stu-id="45d8f-123">In the **Warning** dialog, click **Yes**.</span></span> 
    


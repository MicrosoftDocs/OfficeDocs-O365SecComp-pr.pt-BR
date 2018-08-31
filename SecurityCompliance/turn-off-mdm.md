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
# <a name="how-to-turn-off-mobile-device-management-in-office-365"></a>Como desativar o gerenciamento de dispositivos móveis no Office 365

Para desativar efetivamente MDM para o Office 365, você remove grupos de pessoas (definidos por grupos de segurança) através da política de gerenciamento de dispositivo ou remove as políticas em si. 
  
- Remova grupos de usuários, removendo os grupos de segurança do usuário através da política de dispositivo que você criou. 
    
- Desabilite MDM para todas as pessoas, removendo todas as políticas de dispositivo MDM. 
    
Essas opções removerá imposição MDM para dispositivos em sua organização. Infelizmente, você não pode simplesmente "desprovisionar" MDM para o Office 365 depois de configurá-lo.
  
> [!IMPORTANT]
> Lembre-se do impacto em dispositivos dos usuários quando você remove grupos de segurança do usuário de políticas ou remove as políticas em si. Por exemplo, email perfis e emails em cache podem ser removidos, dependendo do dispositivo. Consulte: [qual é o impacto das diretivas de segurança em tipos diferentes de dispositivos?](create-device-security-policies.md#what-is-the-impact-of-security-policies-on-different-device-types)
  
## <a name="remove-user-security-groups-from-mdm-device-policies"></a>Remover grupos de segurança do usuário de políticas de dispositivo do MDM

1. Vá para **segurança &amp; Centro de conformidade** \> **prevenção de perda de dados** \> **políticas de segurança de dispositivo**.
    
2. Selecione uma política de dispositivo e, em seguida, clique em ![ícone Editar](media/O365-MDM-CreatePolicy-EditIcon.gif) **Editar política**.
    
3. Em **implantação**, clique em **- Remove**.
    
    Em **grupos**, selecione um grupo de segurança.
    
4.  Clique em **Remover**.
    
5. Clique em **Salvar**.
    
## <a name="remove-mdm-device-policies"></a>Remover políticas de dispositivo do MDM

1. Vá para **segurança &amp; Centro de conformidade** \> **diretivas de segurança** \> **diretivas de segurança de dispositivo**.
    
2. Selecione uma política de dispositivo e clique em ![imagem da Lixeira pode ícone. ](media/b8bfa783-c0b5-46d9-9570-8a385088e8fe.png) **Excluir a política**.
    
3. Na caixa de diálogo de **Aviso** , clique em **Sim**. 
    


---
title: Gerenciar dispositivos inscritos no gerenciamento de dispositivos móveis no Office 365
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
- MBS150
- MET150
ms.assetid: 28dd276b-beeb-4c5b-8b22-7551186127fe
description: Siga estas etapas para definir o backup Mobile Device Management (MDM) no Office 365.
ms.openlocfilehash: 3a84b6904b866e07eb4efabe0f39041b282d0ba9
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272306"
---
# <a name="manage-devices-enrolled-in-mobile-device-management-in-office-365"></a>Gerenciar dispositivos inscritos no gerenciamento de dispositivos móveis no Office 365

O gerenciamento de dispositivos móveis internos para o Office 365 ajuda a proteger e gerenciar dispositivos móveis dos usuários, como iPhones, iPads, Androids, e telefones do Windows. A primeira etapa é entrar no Office 365 e [Configurar MDM para o Office 365](set-up-mobile-device-management.md). 
  
Depois que você tiver montá-lo, as pessoas na sua organização deve [registrar seus dispositivos](enroll-your-mobile-device.md) no serviço. Em seguida, você pode usar o MDM para o Office 365 para ajudar a gerenciar dispositivos em sua organização. Por exemplo, você pode usar as diretivas de segurança de dispositivo para ajudar a limitar o acesso de email ou outros serviços, exibir relatórios de dispositivos e limpar remotamente um dispositivo. Normalmente, você será levado para a [Ir para a segurança do Office 365 &amp; Centro de conformidade](https://support.office.com/article/7e696a40-b86b-4a20-afcc-559218b7b1b8) fazer essas tarefas. 
  
## <a name="device-management-tasks"></a>Tarefas de gerenciamento de dispositivo

Para obter o painel de gerenciamento de dispositivo, siga estas etapas. 
  
1. Vá para o centro de administração do Office 365.
    
2. Digite o gerenciamento de dispositivos móveis no campo de pesquisa e selecione **Gerenciamento de dispositivos móveis** da lista de resultados. 
    
    ![Tipo Mobile Device Manager no campo de pesquisa O365](media/e2e2f1c0-e543-431a-959b-e26c2ba328a7.png)
  
Depois que você acaba de criar MDM para o Office 365, configurar, aqui está como você pode gerenciar os dispositivos móveis em sua organização. 
  
|**Para fazer isso...**|**Faça isto**|
|:-----|:-----|
|Apagar um dispositivo  <br/> |No painel do gerenciamento de dispositivos, selecione o *nome do dispositivo* , **apagamento completo** para excluir todas as informações ou **seletiva apagar** para excluir somente as informações organizacionais no dispositivo.  <br/> Consulte [Apagar um dispositivo no Office 365](wipe-a-mobile-device.md).  <br/> |
|Bloquear o acesso de dispositivos sem suporte ao email do Exchange usando o Exchange ActiveSync  <br/> |No painel do gerenciamento de dispositivos, selecione **Bloquear**.  <br/> |
|Configurar políticas de dispositivo como requisitos de senha e configurações de segurança  <br/> |No painel do gerenciamento de dispositivo, clique em \> **diretivas de segurança de dispositivo** \> **Adicionar +**.  <br/> Consulte [criar e implantar diretivas de segurança de dispositivo](create-device-security-policies.md).  <br/> |
|Exibir a lista de dispositivos bloqueados  <br/> |No painel do gerenciamento de dispositivo, em **Selecione um modo de exibição** , selecione **bloqueado**.  <br/> ||
|Desbloquear um dispositivo incompatível ou sem suporte para um usuário ou para um grupo de usuários  <br/> | Você pode desbloquear dispositivos incompatíveis várias maneiras, dependendo da sua situação. Escolha um destes procedimentos:<br/>  Remova o grupo de segurança que foi aplicada a política para o usuário ou usuários. Vá para **o Centro de administração do Office 365** \> **grupos**e selecione * nome do grupo *. Clique em **Editar membros e administradores**.<br/>  Remova o grupo de segurança que os usuários serão um membro da política de dispositivo. Vá para **segurança &amp; Centro de conformidade** \> **diretivas de segurança** \> **diretivas de segurança de dispositivo**. Selecione * nome da política de dispositivo *, clique em **Editar** ![ícone Editar](media/O365_MDM_CreatePolicy_EditIcon.gif) \> **implantação**.<br/>  Desbloquear todos os dispositivos incompatíveis para uma política de dispositivo. Vá para **segurança &amp; Centro de conformidade** \> **diretivas de segurança** \> **diretivas de segurança de dispositivo**. Selecione o *nome da política de dispositivo* e clique em **Editar** ![ícone Editar](media/O365_MDM_CreatePolicy_EditIcon.gif) \> **requisitos de acesso**. Selecione **Permitir violação de acesso e o relatório**.<br/>  Para desbloquear um dispositivo incompatível ou não tem suporte para um usuário ou um grupo de usuários, consulte Go to **segurança &amp; Centro de conformidade** \> **diretivas de segurança** \> **Device management** \> configurações **Gerenciar o acesso de dispositivo **. Adicione um grupo de segurança com os membros que você deseja excluir sejam bloqueados acesso ao Office 365. Consulte [criar, editar ou excluir um grupo de segurança no Centro de administração do Office 365](https://support.office.com/article/55c96b32-e086-4c9e-948b-a018b44510cb).<br/> |
|Obter detalhes sobre os dispositivos em sua organização  <br/> |Para obter detalhes, como quais dispositivos estão registrados e em conformidade com as diretivas de segurança de dispositivo, siga as etapas descritas em [obter detalhes sobre os dispositivos gerenciados por MDM](get-details-about-mdm-managed-devices.md).  <br/> |
|Remover usuários para que seus dispositivos não são mais gerenciados pelo MDM  <br/> |Edite o grupo de segurança que tem políticas de gerenciamento de dispositivo para MDM remover o usuário. Consulte [criar, editar ou excluir um grupo de segurança no Centro de administração do Office 365](https://support.office.com/article/55c96b32-e086-4c9e-948b-a018b44510cb).<br/> Para remover o MDM todos os usuários do Office 365, consulte [desativar o gerenciamento de dispositivos móveis no Office 365](turn-off-mdm.md).  <br/> |
   


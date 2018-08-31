---
title: Solucionar problemas de inscrição de dispositivo com o MDM para Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 11/17/2015
ms.audience: Admin
ms.topic: get-started-article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: c863b2bf-45f3-483a-ba05-29fc7f4d6434
description: Se você estiver executando nestes problemas ao tentar registrar um dispositivo Mobile Device Management (MDM) para o Office 365, siga as etapas listadas aqui para rastrear o problema. Se as etapas gerais não corrigir o problema, consulte uma das seções posteriores com as etapas específicas para o seu tipo de dispositivo.
ms.openlocfilehash: 490259fc623b38ab5ad6cf8553c5074c77b77426
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272106"
---
# <a name="troubleshoot-device-enrollment-with-mdm-for-office-365"></a>Solucionar problemas de inscrição de dispositivo com o MDM para Office 365

Se você estiver executando nestes problemas ao tentar registrar um dispositivo Mobile Device Management (MDM) para o Office 365, siga as etapas listadas aqui para rastrear o problema. Se as etapas gerais não corrigir o problema, consulte uma das seções posteriores com as etapas específicas para o seu tipo de dispositivo.
  
## <a name="steps-to-try-first"></a>Etapas para tentar primeiro

Para começar, verifique o seguinte:
  
- Certifique-se de que o dispositivo não está inscrito já com outro provedor de gerenciamento de dispositivo móvel, como Intune.
    
- Certifique-se de que o dispositivo está definido como a data e hora correta.
    
- Alternar para um Wi-Fi diferente ou a rede celular no dispositivo.
    
- Para dispositivos Android ou iOS, desinstale e reinstale o aplicativo de Portal da empresa Intune no dispositivo.
    
## <a name="ios-phone-or-tablet"></a>iOS celular ou tablet

- Certifique-se de que você tiver que [Configurar um certificado APNs](https://support.office.com/article/522b43f4-a2ff-46f6-962a-dd4f47e546a7).
    
- Nas **configurações** \> **Geral** \> **perfil** (ou **Device Management**), certifique-se de que um **Perfil de gerenciamento** já não está instalado. Se estiver, removê-lo. 
    
- Se você vir a mensagem de erro "Falha de dispositivo que se inscrevam," entrar no Office 365 e certifique-se de que uma licença que inclui o Exchange Online tiver sido atribuída ao usuário que está conectado ao dispositivo.
    
- Se você vir a mensagem de erro "Falha de perfil instalar," Tente um destes procedimentos:
    
  - Certifique-se de que o Safari é o navegador padrão no dispositivo e que os cookies não estejam desabilitados.
    
  - Reinicializar o dispositivo, e em seguida, navegue até portal.manage.microsoft.com, entrar com sua ID de usuário do Office 365 e senha e tente instalar o perfil manualmente.
    
## <a name="windows-rt-tablet"></a>Tablet do Windows RT

- Certifique-se de que seu domínio é [configurado no Office 365 para funcionar com MDM](set-up-mobile-device-management.md).
    
- Certifique-se de que o usuário está escolhendo **Turn On** em vez de escolhendo **ingressar**.
    
## <a name="windows-phone"></a>Windows Phone

- Certifique-se de que seu domínio é [configurado no Office 365 para funcionar com MDM](set-up-mobile-device-management.md).
    
- Verifique se que o dispositivo está executando o Windows 8.1 ou posterior.
    
## <a name="android-phone-or-tablet"></a>Telefone Android ou tablet

- Verifique se que o dispositivo está executando o Android 4.0 ou posterior.
    
- Se você vir a mensagem de erro, "Nós não pôde registrar este dispositivo," entrar no Office 365 e certifique-se de que uma licença que inclui o Exchange Online tiver sido atribuída ao usuário que está conectado ao dispositivo.
    
- Verifique se a **Área de notificação** no dispositivo para ver se quaisquer ações do usuário final necessários estão pendentes e se eles forem, conclua as ações. 
    


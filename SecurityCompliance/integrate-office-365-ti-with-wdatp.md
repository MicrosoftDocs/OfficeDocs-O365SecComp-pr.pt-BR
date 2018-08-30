---
title: Integrar a Inteligência Contra Ameaças do Office 365 com a Proteção Avançada contra Ameaças do Windows Defender
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 3/21/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 414fa693-d7b7-4a1d-a387-ebc3b6a52889
description: Integre a proteção de ameaça avançadas do Office 365 Windows Defender avançada proteção contra ameaças para ver as informações mais detalhadas de gerenciamento de ameaça.
ms.openlocfilehash: 574594d5881853b268713e0bb74444ae80ffcf46
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523764"
---
# <a name="integrate-office-365-threat-intelligence-with-windows-defender-advanced-threat-protection"></a>Integrar a Inteligência Contra Ameaças do Office 365 com a Proteção Avançada contra Ameaças do Windows Defender

Se você fazem parte da equipe de segurança da sua organização, você poderá integrar o Office 365 com Windows Defender avançadas ameaça proteção (ATP). Isso pode ajudá-lo a entender rapidamente se máquinas dos usuários estão em risco quando estiver investigando ameaças no Office 365. Por exemplo, quando integração estiver habilitada, você poderá ver uma lista de computadores que são usadas pelos destinatários de uma mensagem de e-mail detectado, bem como a esses aparelhos de muitos alertas recentes têm no Windows Defender ATP.
  
A imagem a seguir mostra a guia **dispositivos** que você verá quando tem integração do Windows Defender ATP habilitada: 
  
![Quando o Windows Defender ATP estiver habilitado, você pode ver uma lista das máquinas com alertas.](media/fec928ea-8f0c-44d7-80b9-a2e0a8cd4e89.PNG)
  
Neste exemplo, você pode ver que os destinatários da mensagem de email têm quatro máquinas e um terá um alerta no Windows Defender ATP. Clicando no link para uma máquina abre a página de máquina no Windows Defender ATP em uma nova guia.
  
## <a name="requirements"></a>Requisitos

- Sua organização deve ter inteligência de ameaça do Office 365 e Windows Defender ATP.
    
- Você deve ser um administrador global do Office 365 ou ter uma função de administrador de segurança atribuída na segurança &amp; Centro de conformidade. (Consulte [Permissions in a segurança do Office 365 &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md))
    
- Você deve ter acesso ao Office 365 Threat Intelligence e o portal do Windows Defender ATP.
    
## <a name="to-integrate-office-365-threat-intelligence-with-windows-defender-atp"></a>Para integrar o Office 365 Threat Intelligence com Windows Defender ATP

Integrando o Office 365 Threat Intelligence com Windows Defender ATP é configurado no Office 365 e no portal do Windows Defender ATP.
  
1. Como um global do Office 365 ou um administrador de segurança, vá para [https://portal.office.com](https://portal.office.com) e entre com sua conta de trabalho ou da escola para o Office 365. 
    
2. Escolha **gerenciamento de ameaça** \> **explorer de ameaça**.
    
3. No menu **mais** , escolha **Configurações de WDATP**.
    
4. Selecione **conectar-se ao Windows ATP**.
    
Depois de alterar as configurações no Office 365, você deve habilitar a conexão do Windows Defender ATP. Para fazer isso, consulte [usar o portal de proteção de ameaça avançado do Windows Defender](https://go.microsoft.com/fwlink/?linkid=859690).
  
## <a name="related-topics"></a>Tópicos relacionados

[Inteligência Contra Ameaças do Office 365](office-365-ti.md)
  
[Proteção Avançada contra Ameaças do Office 365](office-365-atp.md) 
  


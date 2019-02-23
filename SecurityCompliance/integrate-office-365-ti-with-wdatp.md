---
title: Integrar a Inteligência Contra Ameaças do Office 365 com a Proteção Avançada contra Ameaças do Windows Defender
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/22/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 414fa693-d7b7-4a1d-a387-ebc3b6a52889
ms.collection: M365-security-compliance
description: Integre a proteção avançada contra ameaças do Office 365 com a proteção avançada contra ameaças do Windows Defender para ver informações mais detalhadas sobre o gerenciamento de ameaças.
ms.openlocfilehash: ec7c7f565a4a316085b586168512699bb13cad47
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220921"
---
# <a name="integrate-office-365-threat-intelligence-with-windows-defender-advanced-threat-protection"></a>Integrar a Inteligência Contra Ameaças do Office 365 com a Proteção Avançada contra Ameaças do Windows Defender

Se você fizer parte da equipe de segurança de sua organização, poderá integrar os recursos de proteção avançada contra ameaças e inteligência de ameaças do Office 365 com a proteção avançada contra ameaças do Windows Defender. Isso pode ajudá-lo a entender rapidamente se as máquinas dos usuários estão em risco quando você está investigando ameaças no Office 365. Por exemplo, depois que a integração estiver habilitada, você poderá ver uma lista de máquinas que são usadas pelos destinatários de uma mensagem de email detectada, bem como os alertas recentes que essas máquinas têm na proteção avançada contra ameaças do Windows Defender.
  
A imagem a seguir mostra a guia **dispositivos** que você verá quando tiver a integração de proteção avançada contra ameaças do Windows Defender habilitada: 
  
![Quando o Windows Defender ATP estiver habilitado, você poderá ver uma lista de computadores com alertas.](media/fec928ea-8f0c-44d7-80b9-a2e0a8cd4e89.PNG)
  
Neste exemplo, você pode ver que os destinatários da mensagem de email têm quatro dispositivos e um tem um alerta. Clicar no link de um dispositivo abre sua página no portal de proteção avançada contra ameaças do Windows Defender.
  
## <a name="requirements"></a>Requisitos

- Sua organização deve ter o Office 365 Threat Intelligence e o Windows Defender ATP.
    
- Você deve ser um administrador global do Office 365 ou ter uma função de administrador de segurança (como administrador de segurança) atribuída no [centro de conformidade de segurança &amp; ](https://protection.office.com). (Consulte [permissões no centro de conformidade de &amp; segurança do Office 365](permissions-in-the-security-and-compliance-center.md))
    
- Você deve ter acesso ao Office 365 Threat Intelligence e ao portal de proteção avançada contra ameaças do Windows Defender.
    
## <a name="to-integrate-office-365-threat-intelligence-with-windows-defender-atp"></a>Para integrar o Office 365 Threat Intelligence com o Windows Defender ATP

Integração do Office 365 Threat Intelligence com a proteção avançada contra ameaças do Windows Defender é configurada usando o centro de conformidade do Office 365 Security & e o portal de proteção avançada contra ameaças do Windows Defender.
  
1. Como um administrador global do Office 365 ou um administrador de segurança, [https://protection.office.com](https://protection.office.com) acesse e entre com sua conta corporativa ou de estudante para o Office 365. 
    
2. Escolha **** \> **Gerenciador**de gerenciamento de ameaças.<br>![Gerenciador no menu de gerenciamento de ameaças](media/ThreatMgmt-Explorer-nav.png)<br>
    
3. No canto superior direito da tela, escolha configurações de **WDATP**.
    
4. Na caixa de diálogo conexão ATP do Windows Defender, ative conectar ao Windows ATP.<br>![Conexão ATP do Windows Defender](media/Explorer-WDATPConnection-dialog.png)<br>
    
5. Habilitar a conexão na proteção avançada contra ameaças do Windows Defender. Consulte [usar o portal de proteção avançada contra ameaças do Windows Defender](https://go.microsoft.com/fwlink/?linkid=859690).

  
## <a name="related-topics"></a>Tópicos relacionados

[Inteligência Contra Ameaças do Office 365](office-365-ti.md)
  
[Proteção Avançada contra Ameaças do Office 365](office-365-atp.md) 
  


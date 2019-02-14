---
title: Integrar a Inteligência Contra Ameaças do Office 365 com a Proteção Avançada contra Ameaças do Windows Defender
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/22/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 414fa693-d7b7-4a1d-a387-ebc3b6a52889
ms.collection: M365-security-compliance
description: Integre a proteção de ameaça avançadas do Office 365 Windows Defender avançada proteção contra ameaças para ver as informações mais detalhadas de gerenciamento de ameaça.
ms.openlocfilehash: f8f5f50af10fb668aa67b68604e95e8dd19c9e69
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995202"
---
# <a name="integrate-office-365-threat-intelligence-with-windows-defender-advanced-threat-protection"></a>Integrar a Inteligência Contra Ameaças do Office 365 com a Proteção Avançada contra Ameaças do Windows Defender

Se você fizer parte da equipe de segurança da sua organização, você poderá integrar os recursos de proteção de ameaça avançadas do Office 365 e inteligência de ameaça com a proteção de ameaça avançado do Windows Defender. Isso pode ajudá-lo a entender rapidamente se máquinas dos usuários estão em risco quando estiver investigando ameaças no Office 365. Por exemplo, quando integração estiver habilitada, você poderá ver uma lista das máquinas que são usadas pelos destinatários de uma mensagem de e-mail detectado, assim como a esses aparelhos de muitos alertas recentes têm na proteção de ameaça avançado do Windows Defender.
  
A imagem a seguir mostra a guia **dispositivos** que você verá quando tem integração de proteção de ameaça avançado do Windows Defender habilitada: 
  
![Quando o Windows Defender ATP estiver habilitado, você pode ver uma lista das máquinas com alertas.](media/fec928ea-8f0c-44d7-80b9-a2e0a8cd4e89.PNG)
  
Neste exemplo, você pode ver que os destinatários da mensagem de email têm quatro dispositivos e um terá um alerta. Clicar no link para um dispositivo abre sua página no portal de proteção de ameaça avançado do Windows Defender.
  
## <a name="requirements"></a>Requisitos

- Sua organização deve ter inteligência de ameaça do Office 365 e Windows Defender ATP.
    
- Você deve ser um Administrador Global do Office 365 ou ter uma função de administrador de segurança (como administrador de segurança) atribuída no [segurança &amp; Centro de conformidade](https://protection.office.com). (Consulte [Permissions in a segurança do Office 365 &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md))
    
- Você deve ter acesso ao Office 365 Threat Intelligence e o portal de proteção de ameaça avançado do Windows Defender.
    
## <a name="to-integrate-office-365-threat-intelligence-with-windows-defender-atp"></a>Para integrar o Office 365 Threat Intelligence com Windows Defender ATP

Integrando o Office 365 Threat Intelligence com a proteção de ameaça avançado do Windows Defender é definida por meio de ambas as & de segurança do Office 365 Centro de conformidade e o portal de proteção de ameaça avançado do Windows Defender.
  
1. Como um administrador global do Office 365 ou um administrador de segurança, vá para [https://protection.office.com](https://protection.office.com) e entre com sua conta de trabalho ou da escola para o Office 365. 
    
2. Escolha **gerenciamento de ameaça** \> **Explorer**.<br>![Explorer no menu gerenciamento de ameaça](media/ThreatMgmt-Explorer-nav.png)<br>
    
3. No canto superior direito da tela, escolha **Configurações de WDATP**.
    
4. Na caixa de diálogo conexão do Windows Defender ATP, ative conectar ao Windows ATP.<br>![Conexão do Windows Defender ATP](media/Explorer-WDATPConnection-dialog.png)<br>
    
5. Habilite a conexão na proteção de ameaça avançado do Windows Defender. Consulte o [uso do portal de proteção de ameaça avançado do Windows Defender](https://go.microsoft.com/fwlink/?linkid=859690).

  
## <a name="related-topics"></a>Tópicos relacionados

[Inteligência Contra Ameaças do Office 365](office-365-ti.md)
  
[Proteção Avançada contra Ameaças do Office 365](office-365-atp.md) 
  


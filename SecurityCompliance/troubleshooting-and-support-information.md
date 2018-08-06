---
title: Solução de problemas e informações de suporte
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 5d9f75f5-bb7f-458c-ad30-5c8eae0b0e4e
description: Este tópico descreve as etapas de solução de problemas para os usuários finais e administradores e fornece informações sobre como contatar o suporte técnico para obter assistência.
ms.openlocfilehash: d6168be0580175b172616b3274f2a13f36de5d57
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027628"
---
# <a name="troubleshooting-and-support-information"></a>Solução de problemas e informações de suporte

Este tópico descreve as etapas de solução de problemas para os usuários finais e administradores e fornece informações sobre como contatar o suporte técnico para obter assistência.
  
## <a name="troubleshooting-for-users"></a>Solução de problemas para os usuários

Ocasionalmente, você pode enfrentar problemas com o Microsoft Office Outlook depois de adicionar o Suplemento de Relatório de Lixo Eletrônico. Veja a seguir os problemas que você pode encontrar, juntamente com dicas para resolvê-los. 
  
- Nada acontece quando você clica em **Relatar Lixo Eletrônico**
    
- O Outlook para de responder depois que você selecionar uma mensagem de email
    
- O lixo eletrônico relatado não pode ser entregue devido a uma resposta "não entregue"
    
### <a name="troubleshooting-tip"></a>Dica de solução de problemas

1. Feche e reinicie o Microsoft Office Outlook.
    
2. Verifique se você é capaz de criar e enviar uma mensagem de teste. Para fazer isso, você pode enviar uma mensagem de teste para outra conta de email pela qual é responsável e, em seguida, verificar se a mensagem é recebida.
    
Se o problema persistir, entre em contato com o administrador de TI.
  
> [!TIP]
> Você também pode enviar mensagens de spam diretamente à Microsoft usando o endereço de email [junk@office365.microsoft.com](mailto:junk@office365.microsoft.com) e mensagens de falso positivo usando o endereço de email [not_junk@office365.microsoft.com](mailto: not_junk@office365.microsoft.com) . Para obter mais informações, consulte o [envio de spam, não spam e mensagens de golpes de phishing à Microsoft para análise](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md). 
  
## <a name="troubleshooting-for-administrators"></a>Solução de problemas para os administradores

Como administrador, você pode perceber problemas com usuários que utilizam o Suplemento de Relatório de Lixo Eletrônico do Microsoft Office Outlook. A seguir. apresentamos algumas dicas para solucionar problemas que você possa vir a encontrar. 
  
 **Problema:** Aparece uma mensagem de erro continuamente pedindo para os usuários entrarem em contato com o administrador do sistema. 
  
### <a name="troubleshooting-tip"></a>Dica de solução de problemas

1. Defina o seguinte valor de chave do Registro como "Verbose":
    
  - **Outlook de 32 bits instalado em um sistema operacional de 32 bits:**
    
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Junk Email Reporting\Addins\LoggingLevel
    
  - **Outlook de 32 bits instalado em um sistema operacional de 64 bits:**
    
    HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Junk Email Reporting\Addins\LoggingLevel
    
  - **Outlook de 64 bits (sempre instalado em um sistema operacional de 64 bits):**
    
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Junk Email Reporting\Addins\LoggingLevel
    
2. Reinicie o Microsoft Office Outlook e peça aos usuários para relatar quando virem a mensagem de erro.
    
3. Colete as informações de log encontradas no seguinte local: 
    
    %LOCALAPPDATA%\Microsoft\Junk Email Reporting Add-in\SpamReporterAddinLog.txt
    
4. Entre em contato com o suporte técnico do Exchange Online Protection e forneça as informações de log. 
    
 **Problema:** Os usuários optam por não receber uma confirmação quando eles enviam um email como lixo eletrônico e agora eles querem a opção de volta. 
  
### <a name="troubleshooting-tip"></a>Dica de solução de problemas

1. Defina o seguinte valor de chave do Registro como "True": HKEY_CURRENT_USER\Software\Microsoft\Junk E-mail Reporting\Preferences\ConfirmReportJunk
    
2. Reinicie o Microsoft Office Outlook.
    
## <a name="support-information"></a>Informações de suporte

Se você precisar de ajuda com a instalação, configuração ou desinstalação do add-in, entre em contato com suporte técnico usando o novo link de solicitação de serviço da página de suporte no Centro de administração do Office 365. Para obter outras opções, incluindo enviando uma solicitação de serviço através das opções de telefone e auto-suporte, consulte a [Ajuda e suporte para EOP](eop/help-and-support-for-eop.md).
  
## <a name="for-more-information"></a>Para saber mais

[Habilitar o suplemento de mensagem de relatório](https://support.office.com/article/4250c4bc-6102-420b-9e0a-a95064837676)
  
[Relatar mensagens de lixo eletrônico à Microsoft](report-junk-email-messages-to-microsoft.md)
  


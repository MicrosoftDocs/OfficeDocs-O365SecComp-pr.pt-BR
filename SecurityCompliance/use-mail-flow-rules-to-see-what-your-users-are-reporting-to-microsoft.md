---
title: Usar regras de fluxo de email para ver o que os usuários são relatórios à Microsoft
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 8/23/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 8401f520-8e7c-467b-9e06-4a9fdb2ba548
description: Você pode criar uma regra de transporte do Exchange para impedir que os usuários enviem mensagens de email à Microsoft para análise e usá-los em seus próprios processos de segurança
ms.openlocfilehash: f2376668e2a1a16eba9913178a100fc31763b227
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026768"
---
# <a name="use-mail-flow-rules-to-see-what-your-users-are-reporting-to-microsoft"></a>Usar regras de fluxo de email para ver o que os usuários são relatórios à Microsoft

Há várias maneiras que você pode enviar as mensagens negativas falsos positivas e falsos para a Microsoft para análise. Como administrador, você pode usar as regras de fluxo de correio para ver o que os usuários são relatórios para a Microsoft como spam, golpes de phishing e não spam. Para obter mais informações, consulte o [envio de spam, não spam e mensagens de golpes de phishing à Microsoft para análise](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md). Por outro lado, você pode criar uma regra de transporte do Exchange para impedir que os usuários enviem mensagens de email à Microsoft para análise e usá-los em seus próprios processos de segurança.
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>O que você precisa saber antes de começar?
<a name="sectionSection0"> </a>

Tempo estimado para conclusão: 5 minutos
  
Você precisa ter permissões antes de executar este procedimento ou procedimentos. Para ver quais permissões você precisa, consulte a entrada "Regras de transporte" no tópico [permissões de política e conformidade de mensagens](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) e a entrada "Políticas de caixa de correio do Outlook Web App" no tópico [permissões de dispositivos móveis e clientes](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx) . 
  
Para informações sobre atalhos de teclado que possam se aplicar aos procedimentos neste tópico, consulte **Atalhos de teclado no Centro de administração do Exchange**.
  
## <a name="use-the-eac-to-create-a-mail-flow-rule-to-view-users-manual-junk-phishing-and-not-junk-reports"></a>Usar o EAC para criar uma regra de fluxo de email para exibir lixo manual, phishing e relatórios não sendo lixo eletrônico dos usuários
<a name="sectionSection1"> </a>

1. No EAC, navegue até **Fluxo de email** \> **Regras**.
    
2. Clique em ![Ícone Adicionar](media/ITPro-EAC-AddIcon.png) e em seguida, selecione **Criar uma nova regra**.
    
3. Dê um nome à regra e então clique em **Mais opções**.
    
4. Em **Aplicar esta regra se**, selecione **O destinatário** e escolha **endereço inclui qualquer uma destas palavras**.
    
5. Na caixa **especificar palavras ou frases**, faça o seguinte: 
    - Digite **abuse@messaging.microsoft.com** e clique em ![Ícone Adicionar](media/ITPro-EAC-AddIcon.png); depois digite **junk@office365.microsoft.com** e clique em ![Ícone Adicionar](media/ITPro-EAC-AddIcon.png). Esses endereços de email são usados para enviar mensagens de falso negativo para a Microsoft.
    - Digite **phish@office365.microsoft.com** e, em seguida, clique em ![ícone Adicionar](media/ITPro-EAC-AddIcon.png). Esse endereço de email é usado para enviar mensagens de phishing perdidas à Microsoft.
    - Digite **false_positive@messaging.microsoft.com** e clique em ![Ícone Adicionar](media/ITPro-EAC-AddIcon.png); depois digite **not_junk@office365.microsoft.com** e clique em ![Ícone Adicionar](media/ITPro-EAC-AddIcon.png). Esses endereços de email são usados para enviar mensagens de falso positivo para a Microsoft.
    - Clique em **OK**.
    
6. Em **faça o seguinte**, selecione **Cco da mensagem para...** e, em seguida e, em seguida, selecione as caixas de correio em que você gostaria de recebem as mensagens. 
    
7. Se desejar, você pode optar por auditar a regra, testar a regra, ativar a regra durante um período de tempo específico e outras opções. Recomendamos testar a regra por um período antes de aplicá-la. O tópico [Manage Transport Rules](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx) contém mais informações sobre estas seleções. 
    
8. Clique no botão **salvar** para salvar a regra. Ela aparece na sua lista de regras. 
    
Depois de criar e aplicar a regra, todas as mensagens que são enviadas de sua organização para os endereços de email especificados serão copiadas para a caixa de correio especificada.
  


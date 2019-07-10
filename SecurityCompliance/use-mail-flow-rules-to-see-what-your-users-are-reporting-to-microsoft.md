---
title: Usar regras de fluxo de emails para ver o que seus usuários estão relatando à Microsoft
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 8401f520-8e7c-467b-9e06-4a9fdb2ba548
ms.collection:
- M365-security-compliance
description: Você pode criar uma regra de fluxo de email do Exchange para impedir que os usuários enviem mensagens de email para a Microsoft para análise e usá-las em seus próprios processos de segurança
ms.openlocfilehash: 7308de8e3f23a7c210d4d8a4e6ec5e322d40055f
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35600427"
---
# <a name="use-mail-flow-rules-to-see-what-your-users-are-reporting-to-microsoft"></a>Usar regras de fluxo de emails para ver o que seus usuários estão relatando à Microsoft

Existem várias maneiras de você poder enviar mensagens de falso positivo e de falso negativo para a Microsoft para análise. Como administrador, você pode usar regras de fluxo de email para ver o que seus usuários estão relatando à Microsoft como spam, não spam e golpes de phishing. Para obter mais informações, consulte [enviar mensagens de spam, não spam e golpes de phishing para a Microsoft para análise](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md). Por outro lado, você pode criar uma regra de fluxo de emails do Exchange (também conhecida como regra de transporte) para impedir que os usuários enviem mensagens de email para a Microsoft para análise e usá-las em seus próprios processos de segurança.
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>O que você precisa saber antes de começar?

Tempo estimado para conclusão: 5 minutos
  
Para executar este procedimento ou estes procedimentos, você precisa receber permissões. Para ver de que permissões você precisa, consulte o entrada "regras de fluxo de emails" no tópico [Messaging Policy and Compliance Permissions](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) e The "Outlook on the Web Mailbox Policies" no tópico [clients and Mobile](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx) Devices Permissions. 
  
Para informações sobre atalhos de teclado que possam se aplicar aos procedimentos neste tópico, confira **Atalhos de teclado no Centro de Administração do Exchange**.
  
## <a name="use-the-eac-to-create-a-mail-flow-rule-to-view-users-manual-junk-phishing-and-not-junk-reports"></a>Use o Eat para criar uma regra de fluxo de emails para exibir o lixo eletrônico, phishing e não os relatórios de lixo eletrônico

1. No EAC, navegue até **Fluxo de email** \> **Regras**.
    
2. Clique em ![Ícone Adicionar](media/ITPro-EAC-AddIcon.gif) e em seguida, selecione **Criar uma nova regra**.
    
3. Dê um nome à regra e então clique em **Mais opções**.
    
4. Em **Aplicar esta regra se**, selecione **O destinatário** e escolha **endereço inclui qualquer uma destas palavras**.
    
5. Na caixa **especificar palavras ou frases**, faça o seguinte: 
    - Digite `abuse@messaging.microsoft.com` e, em ![seguida,](media/ITPro-EAC-AddIcon.gif)clique em Adicionar ícone `junk@office365.microsoft.com` e digite e ![, em](media/ITPro-EAC-AddIcon.gif)seguida, clique em Adicionar ícone. Esses endereços de email são usados para enviar mensagens de falso negativo para a Microsoft.
    - Digite `phish@office365.microsoft.com` e clique em ![adicionar ícone](media/ITPro-EAC-AddIcon.gif). Esse endereço de email é usado para enviar mensagens de phishing perdidas para a Microsoft.
    - Digite `false_positive@messaging.microsoft.com` e, em ![seguida,](media/ITPro-EAC-AddIcon.gif)clique em Adicionar ícone `not_junk@office365.microsoft.com` e digite e ![, em](media/ITPro-EAC-AddIcon.gif)seguida, clique em Adicionar ícone. Esses endereços de email são usados para enviar mensagens de falso positivo para a Microsoft.
    - Clique em **OK**.
    
6. Em **faça o seguinte**, selecione **Cco a mensagem para...** e, em seguida, selecione as caixas de correio nas quais você gostaria de receber as mensagens. 
    
7. Se desejar, você pode optar por auditar a regra, testar a regra, ativar a regra durante um período de tempo específico e outras opções. Recomendamos testar a regra por um período antes de aplicá-la. Consulte [procedimentos para regras de fluxo de emails](https://docs.microsoft.com/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures). 
    
8. Clique no botão **salvar** para salvar a regra. Ela aparece na sua lista de regras. 
    
Depois de criar e impor a regra, todas as mensagens enviadas da sua organização para os endereços de email especificados serão copiadas para a caixa de correio especificada.
  


---
title: Desativar os relatórios de lixo eletrônico no Outlook na Web
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 8d57fe9e-57b8-4884-9317-80b380804b4a
ms.collection:
- M365-security-compliance
description: Como um administrador do Office 365, você pode desativar a capacidade de os usuários reportarem email como lixo eletrônico.
ms.openlocfilehash: f3e8a8cf837e7923d3c7241852ab2acd375492b8
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32264163"
---
# <a name="turn-off-junk-email-reporting-in-outlook-on-the-web"></a>Desativar os relatórios de lixo eletrônico no Outlook na Web

Você pode enviar mensagens de lixo eletrônico, phishing e não é lixo eletrônico para a Microsoft para análise usando as opções de relatório de lixo eletrônico do Outlook na Web (anteriormente conhecido como Outlook Web App), conforme descrito em [relatar lixo eletrônico e golpes de phishing no Outlook na Web ](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md). Se você não quiser usar essas opções, os administradores podem desativá-las por meio do cmdlet [Set-OwaMailboxPolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx) . 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>O que você precisa saber antes de começar?
<a name="sectionSection0"> </a>

- Tempo estimado para conclusão: 5 minutos
    
- Para executar este procedimento ou estes procedimentos, você precisa receber permissões. Para ver de que permissões você precisa, consulte o entrada "diretivas de caixa de correio do Outlook na Web" no tópico [Outlook na Web Permissions](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx#OutlookWebApp) . 

- Para se conectar ao Exchange Online PowerShell, confira [Conectar ao Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).

## <a name="turn-off-junk-phishing-and-not-junk-reporting-to-microsoft"></a>Desativar os relatórios de lixo eletrônico, phishing e não lixo eletrônico para a Microsoft
<a name="sectionSection1"> </a>

Primeiro, execute o seguinte comando para obter os nomes das políticas de caixa de correio do Outlook disponíveis na Web:
  
```
Get-OwaMailboxPolicy | Format-Table Name
```

Em seguida, use a seguinte sintaxe para habilitar ou desabilitar o lixo eletrônico e não os relatórios de lixo eletrônico para a Microsoft no Outlook na Web:
  
```
Set-OwaMailboxPolicy -Identity "<OWAMailboxPolicyName>" -ReportJunkEmailEnabled <$true | $false>
```

Este exemplo desativa o relatório na política de caixa de correio padrão do Outlook Web App:
  
```
Set-OwaMailboxPolicy -Identity "OwaMailboxPolicy-Default" -ReportJunkEmailEnabled $false
```

Para informações detalhadas de sintaxes e de parâmetros, consulte [Get-OwaMailboxPolicy](http://technet.microsoft.com/library/bdd580d3-8812-4b4a-93e8-c6401b0d2f0f.aspx) e [Set-OwaMailboxPolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx).

## <a name="how-do-you-know-this-worked"></a>Como saber se funcionou?
<a name="sectionSection2"> </a>

Execute **Get-OwaMailboxPolicy** para verificar os valores de parâmetro e, em seguida, abra o Outlook na Web para um usuário afetado (que tenha a política de caixa de correio do Outlook na Web aplicada a eles) e verifique se as opções de relatório de lixo eletrônico, phishing e não estão disponíveis. Você ainda poderá marcar mensagens como lixo eletrônico, phishing e não lixo eletrônico, mas não poderá relatá-las. 

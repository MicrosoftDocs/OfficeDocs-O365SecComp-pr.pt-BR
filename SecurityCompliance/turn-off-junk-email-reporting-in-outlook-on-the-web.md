---
title: Desativar relatório no Outlook na web de lixo eletrônico
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/9/2015
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 8d57fe9e-57b8-4884-9317-80b380804b4a
description: Como um administrador do Office 365, você pode desativar a capacidade de pessoas para email de relatório como lixo eletrônico.
ms.openlocfilehash: 8ee5ff87408b80c443e4cf950ce49f624096becb
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272036"
---
# <a name="turn-off-junk-email-reporting-in-outlook-on-the-web"></a>Desativar relatório no Outlook na web de lixo eletrônico

Você pode enviar mensagens não sendo lixo eletrônico, phishing e lixo eletrônico à Microsoft para análise usando o Outlook no web relatório de lixo eletrônico opções, conforme descrito no [relatório lixo eletrônico e golpes de phishing no Outlook na web ](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md). Se você não quiser usar essas opções, os administradores podem desativá-los por meio do cmdlet [Set-OwaMailboxPolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx) . 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>O que você precisa saber antes de começar?
<a name="sectionSection0"> </a>

- Tempo estimado para conclusão: 5 minutos
    
- Você precisa ter permissões antes de executar este procedimento ou procedimentos. Para ver quais permissões você precisa, consulte a entrada "Políticas de caixa de correio do Outlook Web App" no tópico [permissões do Outlook Web App](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx#OutlookWebApp) . 
    
- Antes de executar os cmdlets necessários para desativar o relatório de lixo eletrônico, pode ser útil revisar as informações de referência nos tópicos [Get-OwaMailboxPolicy](http://technet.microsoft.com/library/bdd580d3-8812-4b4a-93e8-c6401b0d2f0f.aspx) e [Set-OwaMailboxPolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx) . 
    
## <a name="turn-off-junk-phishing-and-not-junk-reporting-to-microsoft"></a>Desativar phishing lixo e não o relatório para a Microsoft de lixo
<a name="sectionSection1"> </a>

Primeiro, para obter os diretórios virtuais nos quais queira desativar os relatórios, execute o cmdlet abaixo:
  
```
Get-OwaMailboxPolicy -Identity <parameter>
```

Em seguida, para desativar o relatório para a Microsoft de lixo eletrônico e não lixo eletrônico execute este cmdlet:
  
```
Set-OwaMailboxPolicy -Identity <parameter> -ReportJunkEmailEnabled $false
```

O cmdlet abaixo, por exemplo, desativa os relatórios para o diretório virtual Contoso\owa:
  
```
Set-OwaMailboxPolicy -Identity Default -ReportJunkEmailEnabled $false
```

## <a name="how-do-you-know-this-worked"></a>Como saber se funcionou?
<a name="sectionSection2"> </a>

Execute o Get-OWAMailboxPolicy para verificar se os valores dos parâmetros e, em seguida, acessar o Outlook na web e verifique se as opções para relatar lixo eletrônico, phishing e não lixo eletrônico não estão disponíveis. Você ainda será capaz de marcar as mensagens como lixo eletrônico, phishing e não é lixo eletrônico, mas você não conseguirá indicá-las. 
  


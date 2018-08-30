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
# <a name="turn-off-junk-email-reporting-in-outlook-on-the-web"></a><span data-ttu-id="21261-103">Desativar relatório no Outlook na web de lixo eletrônico</span><span class="sxs-lookup"><span data-stu-id="21261-103">Turn off junk email reporting in Outlook on the web</span></span>

<span data-ttu-id="21261-p101">Você pode enviar mensagens não sendo lixo eletrônico, phishing e lixo eletrônico à Microsoft para análise usando o Outlook no web relatório de lixo eletrônico opções, conforme descrito no [relatório lixo eletrônico e golpes de phishing no Outlook na web ](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md). Se você não quiser usar essas opções, os administradores podem desativá-los por meio do cmdlet [Set-OwaMailboxPolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx) .</span><span class="sxs-lookup"><span data-stu-id="21261-p101">You can send junk, phishing, and not junk messages to Microsoft for analysis using the Outlook on the web junk email reporting options, as described in [Report junk email and phishing scams in Outlook on the web ](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md). If you don't want to use these options,admins can turn them off via the [Set-OwaMailboxPolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx) cmdlet.</span></span> 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="21261-106">O que você precisa saber antes de começar?</span><span class="sxs-lookup"><span data-stu-id="21261-106">What do you need to know before you begin?</span></span>
<span data-ttu-id="21261-107"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="21261-107"></span></span>

- <span data-ttu-id="21261-108">Tempo estimado para conclusão: 5 minutos</span><span class="sxs-lookup"><span data-stu-id="21261-108">Estimated time to complete: 5 minutes</span></span>
    
- <span data-ttu-id="21261-p102">Você precisa ter permissões antes de executar este procedimento ou procedimentos. Para ver quais permissões você precisa, consulte a entrada "Políticas de caixa de correio do Outlook Web App" no tópico [permissões do Outlook Web App](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx#OutlookWebApp) .</span><span class="sxs-lookup"><span data-stu-id="21261-p102">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Outlook Web App mailbox policies" entry in the [Outlook Web App permissions](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx#OutlookWebApp) topic.</span></span> 
    
- <span data-ttu-id="21261-111">Antes de executar os cmdlets necessários para desativar o relatório de lixo eletrônico, pode ser útil revisar as informações de referência nos tópicos [Get-OwaMailboxPolicy](http://technet.microsoft.com/library/bdd580d3-8812-4b4a-93e8-c6401b0d2f0f.aspx) e [Set-OwaMailboxPolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx) .</span><span class="sxs-lookup"><span data-stu-id="21261-111">Before you run the cmdlets required to turn off junk email reporting, it might be helpful to review the reference information in the [Get-OwaMailboxPolicy](http://technet.microsoft.com/library/bdd580d3-8812-4b4a-93e8-c6401b0d2f0f.aspx) and [Set-OwaMailboxPolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx) topics.</span></span> 
    
## <a name="turn-off-junk-phishing-and-not-junk-reporting-to-microsoft"></a><span data-ttu-id="21261-112">Desativar phishing lixo e não o relatório para a Microsoft de lixo</span><span class="sxs-lookup"><span data-stu-id="21261-112">Turn off junk, phishing, and not junk reporting to Microsoft</span></span>
<span data-ttu-id="21261-113"><a name="sectionSection1"> </a></span><span class="sxs-lookup"><span data-stu-id="21261-113"></span></span>

<span data-ttu-id="21261-114">Primeiro, para obter os diretórios virtuais nos quais queira desativar os relatórios, execute o cmdlet abaixo:</span><span class="sxs-lookup"><span data-stu-id="21261-114">First, run the following cmdlet to get the virtual directories for which you want to turn off reporting:</span></span>
  
```
Get-OwaMailboxPolicy -Identity <parameter>
```

<span data-ttu-id="21261-115">Em seguida, para desativar o relatório para a Microsoft de lixo eletrônico e não lixo eletrônico execute este cmdlet:</span><span class="sxs-lookup"><span data-stu-id="21261-115">Next, run the following cmdlet to turn off junk and not junk reporting to Microsoft:</span></span>
  
```
Set-OwaMailboxPolicy -Identity <parameter> -ReportJunkEmailEnabled $false
```

<span data-ttu-id="21261-116">O cmdlet abaixo, por exemplo, desativa os relatórios para o diretório virtual Contoso\owa:</span><span class="sxs-lookup"><span data-stu-id="21261-116">For example, the following cmdlet turns off reporting for virtual directory Contoso\owa:</span></span>
  
```
Set-OwaMailboxPolicy -Identity Default -ReportJunkEmailEnabled $false
```

## <a name="how-do-you-know-this-worked"></a><span data-ttu-id="21261-117">Como saber se funcionou?</span><span class="sxs-lookup"><span data-stu-id="21261-117">How do you know this worked?</span></span>
<span data-ttu-id="21261-118"><a name="sectionSection2"> </a></span><span class="sxs-lookup"><span data-stu-id="21261-118"></span></span>

<span data-ttu-id="21261-p103">Execute o Get-OWAMailboxPolicy para verificar se os valores dos parâmetros e, em seguida, acessar o Outlook na web e verifique se as opções para relatar lixo eletrônico, phishing e não lixo eletrônico não estão disponíveis. Você ainda será capaz de marcar as mensagens como lixo eletrônico, phishing e não é lixo eletrônico, mas você não conseguirá indicá-las.</span><span class="sxs-lookup"><span data-stu-id="21261-p103">Run Get-OWAMailboxPolicy to check the parameter values, and then access Outlook on the web and verify that the options to report junk, phishing, and not junk are not available. You'll still be able to mark messages as junk, phishing, and not junk, but you won't be able to report them.</span></span> 
  


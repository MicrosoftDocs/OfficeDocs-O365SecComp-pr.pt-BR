---
title: Remetentes seguros e bloqueados listas de remetentes no Exchange Online
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/22/2018
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 111ab6b0-2dd2-4a87-a928-4931df6b3c4d
description: Como um administrador do Exchange Online ou Exchange Online Protection (EOP), você pode ajudar a garantir que uma mensagem de email em viagem através do serviço não está marcada como spam. Uma maneira de fazer isso é criar remetente seguro e listas de remetentes bloqueados para as pessoas na sua organização.
ms.openlocfilehash: cbf886bdcc40044a31b285b6806aecbc95f0f97c
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23003100"
---
# <a name="safe-sender-and-blocked-sender-lists-in-exchange-online"></a><span data-ttu-id="9d2f5-104">Remetentes seguros e bloqueados listas de remetentes no Exchange Online</span><span class="sxs-lookup"><span data-stu-id="9d2f5-104">Safe sender and blocked sender lists in Exchange Online</span></span>

<span data-ttu-id="9d2f5-p102">Como um administrador do Exchange Online ou Exchange Online Protection (EOP), você pode ajudar a garantir que uma mensagem de email em viagem através do serviço não está marcada como spam. Uma maneira de fazer isso é criar remetente seguro e listas de remetentes bloqueados para as pessoas na sua organização.</span><span class="sxs-lookup"><span data-stu-id="9d2f5-p102">As an Exchange Online or Exchange Online Protection (EOP) administrator, you can help ensure that an email message traveling through the service isn't marked as spam. One way to do this is to create safe sender and blocked sender lists for the people in your organization.</span></span> 
  
 <span data-ttu-id="9d2f5-107">*Consulte a versão atualizada das dicas e procedimentos sobre como trabalhar com essas listas como um administrador no* [Impedir email positivo falso marcada como spam com uma lista segura ou outras técnicas](https://go.microsoft.com/fwlink/p/?LinkID=534224).</span><span class="sxs-lookup"><span data-stu-id="9d2f5-107">*See the updated version of the tips and procedures for how to work with these lists as an admin in* [Prevent false positive email marked as spam with a safelist or other techniques](https://go.microsoft.com/fwlink/p/?LinkID=534224).</span></span> 
  
<span data-ttu-id="9d2f5-108">Se você não for um administrador e desejar apenas gerenciar sua próprias lixo eletrônico no Outlook usando uma lista de remetentes seguros, confira as etapas nesta visão geral do [Filtro de lixo eletrônico](https://go.microsoft.com/fwlink/?LinkId=817222).</span><span class="sxs-lookup"><span data-stu-id="9d2f5-108">If you're not an admin, and you just want to manage your own junk email in Outlook by using a safe sender list, check out the steps in this overview of [the Junk Email Filter](https://go.microsoft.com/fwlink/?LinkId=817222).</span></span> 
  
## <a name="what-is-the-safe-and-blocked-sender-limits-in-exchange-online"></a><span data-ttu-id="9d2f5-109">O que é o remetente bloqueado e seguro limites no Exchange Online?</span><span class="sxs-lookup"><span data-stu-id="9d2f5-109">What is the safe and blocked sender limits in Exchange Online?</span></span>

<span data-ttu-id="9d2f5-p103">Os limites de remetentes bloqueados e seguros no Exchange Online são diferentes do Active Directory e limites do Outlook. Eles são:</span><span class="sxs-lookup"><span data-stu-id="9d2f5-p103">The safe and blocked sender limits in Exchange Online differ from the Active Directory and Outlook limits. They are:</span></span>
  
- <span data-ttu-id="9d2f5-112">Limite de remetente seguro: 1.024</span><span class="sxs-lookup"><span data-stu-id="9d2f5-112">Safe sender limit: 1,024</span></span>
    
- <span data-ttu-id="9d2f5-113">Limite de remetentes bloqueados: 500</span><span class="sxs-lookup"><span data-stu-id="9d2f5-113">Blocked sender limit: 500</span></span>
    
<span data-ttu-id="9d2f5-114">Observação:</span><span class="sxs-lookup"><span data-stu-id="9d2f5-114">Note:</span></span>
  
<span data-ttu-id="9d2f5-p104">Você pode enfrentar o erro descrita em KB 2590466 ("você recebe o erro"Erro de validação do lixo eletrônico"no Outlook Web App para Exchange Server 2010"). Para resolver esse problema, desmarque a caixa de seleção "Confiar em emails de Meus contatos". Como alternativa, diminua a quantidade de endereços de email que estão na pasta padrão Contatos de colocá-lo dentro o máximo permitido limitar 1.024 no Exchange Online que está definido para o atributo "MaxSafeSenders". Para obter mais informações sobre esse atributo e o cmdlet Set-Mailbox, seethe seguinte tópico:</span><span class="sxs-lookup"><span data-stu-id="9d2f5-p104">You may experience the error that is described in KB 2590466 ("You receive the error "Junk e-mail validation error" in Outlook Web App for Exchange Server 2010"). To resolve this issue, clear the "Trust emails from my contacts" check box. Alternatively, decrease the amount of email addresses that are in your default Contacts folder to bring it within the maximum allowed limit of 1,024 in Exchange Online that is set for "MaxSafeSenders" attribute. For more information about this attribute and the Set-Mailbox cmdlet, seethe following topic:</span></span>
  
[<span data-ttu-id="9d2f5-119">Set-Mailbox</span><span class="sxs-lookup"><span data-stu-id="9d2f5-119">Set-Mailbox</span></span>](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Set-Mailbox?view=exchange-ps)
  
## <a name="see-also"></a><span data-ttu-id="9d2f5-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="9d2f5-120">See also</span></span>

[<span data-ttu-id="9d2f5-121">No Exchange 2016 a filtragem por remetente</span><span class="sxs-lookup"><span data-stu-id="9d2f5-121">Sender filtering in Exchange 2016</span></span>](http://technet.microsoft.com/library/b833f864-ff10-46a0-a653-28fb9ba30896.aspx)


---
title: Usar o portal de remoção da lista para ser removido da lista de remetentes bloqueados do Office 365
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 4/18/2016
ms.audience: ITPro
ms.topic: troubleshooting
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 0bcecdd4-3343-4cc0-9e58-e19d4de515e8
ms.collection:
- M365-security-compliance
description: Você está recebendo uma mensagem de erro ao tentar enviar um email para um destinatário cujo endereço de email está no Office 365? Se acha que não deve estar recebendo a mensagem de erro, use o portal de remoção da lista para ser removido da lista de remetentes bloqueados do Office 365.
ms.openlocfilehash: 9b4834ae474d781497043bd8800879c57f36d785
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30276172"
---
# <a name="use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-list"></a><span data-ttu-id="74d19-104">Usar o portal de remoção da lista para ser removido da lista de remetentes bloqueados do Office 365</span><span class="sxs-lookup"><span data-stu-id="74d19-104">Use the delist portal to remove yourself from the Office 365 blocked senders list</span></span>

<span data-ttu-id="74d19-p102">Você está recebendo uma mensagem de erro ao tentar enviar um email para um destinatário cujo endereço de email está no Office 365? Se acha que não deve estar recebendo a mensagem de erro, use o portal de remoção da lista para ser removido da lista de remetentes bloqueados do Office 365.</span><span class="sxs-lookup"><span data-stu-id="74d19-p102">Are you getting an error message when you try to send an email to a recipient whose email address is in Office 365? If you think you should not be receiving the error message, you can use the delist portal to remove yourself from the Office 365 blocked senders list.</span></span>
  
## <a name="what-is-the-office-365-blocked-senders-list"></a><span data-ttu-id="74d19-107">O que é a lista de remetentes bloqueados do Office 365?</span><span class="sxs-lookup"><span data-stu-id="74d19-107">What is the Office 365 blocked senders list?</span></span>

<span data-ttu-id="74d19-p103">A Microsoft usa a lista de remetentes bloqueados para proteger seus clientes contra spam, falsificação e ataques de phishing. O endereço IP do seu servidor de email, ou seja, o endereço que o seu servidor de email usa para se identificar na Internet, foi marcado como uma possível ameaça para o Office 365 por um de diversos motivos. Quando o Office 365 adiciona o endereço IP à lista, impede toda a comunicação entre o endereço IP e qualquer um dos nossos clientes por meio de nossos data centers.</span><span class="sxs-lookup"><span data-stu-id="74d19-p103">Microsoft uses the blocked senders list to protect its customers from spam, spoofing, and phishing attacks. Your mail server's IP address, that is, the address your mail server uses to identify itself on the Internet, was tagged as a potential threat to Office 365 for one of a variety of reasons. When Office 365 adds the IP address to the list, it prevents all further communication between the IP address and any of our customers through our datacenters.</span></span>
  
<span data-ttu-id="74d19-111">Você saberá que foi adicionado à lista quando receber uma resposta a uma mensagem de email que inclui um erro parecido com o seguinte:</span><span class="sxs-lookup"><span data-stu-id="74d19-111">You will know you have been added to the list when you receive a response to a mail message that includes an error that looks something like this:</span></span>
  
<span data-ttu-id="74d19-p104">550 5.7.606-649 acesso negado, envio de IP proibido [_endereço IP_]; Para solicitar a remoção dessa lista, acesse https://sender.office.com/ e siga as instruções. Confira mais informações [em notificações de falha na entrega de email no Office 365](http://go.microsoft.com/fwlink/?LinkID=526653).</span><span class="sxs-lookup"><span data-stu-id="74d19-p104">550 5.7.606-649 Access denied, banned sending IP [_IP address_]; To request removal from this list please visit https://sender.office.com/ and follow the directions. For more information please see [Email non-delivery reports in Office 365](http://go.microsoft.com/fwlink/?LinkID=526653).</span></span>
  
<span data-ttu-id="74d19-114">em que  _IP address_ é o endereço IP do computador no qual o servidor de email é executado.</span><span class="sxs-lookup"><span data-stu-id="74d19-114">where  _IP address_ is the IP address of the computer on which the mail server runs.</span></span> 
  
### <a name="to-use-the-office-365-delist-portal-to-remove-yourself-from-the-blocked-senders-list"></a><span data-ttu-id="74d19-115">Para usar o portal de remoção da lista do Office 365 a fim de ser removido da lista de remetentes bloqueados</span><span class="sxs-lookup"><span data-stu-id="74d19-115">To use the Office 365 delist portal to remove yourself from the blocked senders list</span></span>

1. <span data-ttu-id="74d19-116">Em um navegador da Web, acesse [https://sender.office.com](https://sender.office.com).</span><span class="sxs-lookup"><span data-stu-id="74d19-116">In a web browser, go to [https://sender.office.com](https://sender.office.com).</span></span>
    
2. <span data-ttu-id="74d19-p105">Siga as instruções descritas na página. Certifique-se de usar o endereço de email ao qual a mensagem de erro foi enviada e o endereço IP que é especificado na mensagem de erro. Você só pode inserir um endereço de email e um endereço IP por visita.</span><span class="sxs-lookup"><span data-stu-id="74d19-p105">Follow the instructions on the page. Ensure that you use the email address to which the error message was sent, and the IP address that is specified in the error message. You can only enter one email address and one IP address per visit.</span></span>
    
3. <span data-ttu-id="74d19-120">Clique em **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="74d19-120">Click **Submit**.</span></span>
    
    <span data-ttu-id="74d19-p106">O portal envia um email para o endereço de email que você fornece. O email será parecido com o seguinte: ![captura de tela do email recebido ao enviar uma solicitação pelo portal de deslista](media/bf13e4f7-f68c-4e46-baa7-b6ab4cfc13f3.png)</span><span class="sxs-lookup"><span data-stu-id="74d19-p106">The portal sends an email to the email address that you supply. The email will look something like the following:  ![Screenshot of email received when you submit a request through the delist portal](media/bf13e4f7-f68c-4e46-baa7-b6ab4cfc13f3.png)</span></span>
  
4. <span data-ttu-id="74d19-123">Clique no link confirmação no email enviado a você pelo portal de remoção da lista.</span><span class="sxs-lookup"><span data-stu-id="74d19-123">Click the confirmation link in the email sent to you by the delisting portal.</span></span>
    
    <span data-ttu-id="74d19-124">Isso leva você de volta ao portal de remoção da lista.</span><span class="sxs-lookup"><span data-stu-id="74d19-124">This brings you back to the delist portal.</span></span>
    
5. <span data-ttu-id="74d19-125">No portal de remoção da lista, clique em **remover IP da lista**.</span><span class="sxs-lookup"><span data-stu-id="74d19-125">In the delist portal, click **Delist IP**.</span></span>
    
    <span data-ttu-id="74d19-p107">Depois que o endereço IP for removido da lista de remetentes bloqueados, as mensagens de email desse endereço IP serão entregues aos destinatários que usam o Office 365. Portanto, certifique-se de que os emails enviados a partir desse endereço IP não sejam ofensivos ou mal-intencionados; caso contrário, o endereço IP pode ser bloqueado novamente.</span><span class="sxs-lookup"><span data-stu-id="74d19-p107">After the IP address is removed from the blocked senders list, email messages from that IP address will be delivered to recipients who use Office 365. So, make sure you're confident that email sent from that IP address won't be abusive or malicious; otherwise, the IP address might be blocked again.</span></span>
    


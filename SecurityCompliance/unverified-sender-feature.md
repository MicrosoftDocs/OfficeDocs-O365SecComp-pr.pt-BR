---
title: Remetente não verificado
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 04/25/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: Para impedir que mensagens de phishing acessem sua caixa de correio, o Outlook.com e o Outlook na Web verificam se o remetente é quem dizem eles e marcam mensagens suspeitas como lixo eletrônico.
ms.openlocfilehash: 92458a93a4da3e449061e4d2a4ba312d635c42cc
ms.sourcegitcommit: 7f00f765e8fa674ce1c8c66f5b89b6bea45e13ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/22/2019
ms.locfileid: "34341619"
---
# <a name="unverified-sender"></a><span data-ttu-id="c4ca2-103">Remetente não verificado</span><span class="sxs-lookup"><span data-stu-id="c4ca2-103">Unverified Sender</span></span>

<span data-ttu-id="c4ca2-104">Para impedir que mensagens de phishing acessem sua caixa de correio, o Outlook.com e o Outlook na Web verificam se o remetente é quem dizem eles e marcam mensagens suspeitas como lixo eletrônico.</span><span class="sxs-lookup"><span data-stu-id="c4ca2-104">To prevent phishing messages from reaching your mailbox, Outlook.com and Outlook on the web verify that the sender is who they say they are and mark suspicious messages as junk email.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c4ca2-105">Quando uma mensagem é marcada como um golpe de phishing, o Outlook.com e o Outlook na Web exibem um aviso na parte superior da página, mas todos os links na mensagem ainda podem ser abertos.</span><span class="sxs-lookup"><span data-stu-id="c4ca2-105">When a message is marked as a phishing scam, Outlook.com and Outlook on the web display a warning at the top of the page, but any links in the message can still be opened.</span></span>

## <a name="how-can-i-identify-a-suspicious-message-in-my-inbox"></a><span data-ttu-id="c4ca2-106">Como identificar uma mensagem suspeita em minha caixa de entrada?</span><span class="sxs-lookup"><span data-stu-id="c4ca2-106">How can I identify a suspicious message in my inbox?</span></span>

<span data-ttu-id="c4ca2-107">O Outlook.com e o Outlook na Web mostram indicadores quando o remetente de uma mensagem não pode ser identificado ou sua identidade é diferente da que você vê no endereço do remetente.</span><span class="sxs-lookup"><span data-stu-id="c4ca2-107">Outlook.com and Outlook on the web show indicators when the sender of a message either can't be identified or their identity is different from what you see in the From address.</span></span>

## <a name="how-to-manage-which-messages-receive-the-unverified-sender-treatment"></a><span data-ttu-id="c4ca2-108">Como gerenciar quais mensagens recebem o tratamento de remetentes não verificados</span><span class="sxs-lookup"><span data-stu-id="c4ca2-108">How to manage which messages receive the unverified sender treatment</span></span> 

<span data-ttu-id="c4ca2-109">Se você for um cliente do Office 365, poderá gerenciar esse recurso através do centro de conformidade do & de segurança.</span><span class="sxs-lookup"><span data-stu-id="c4ca2-109">If you are an Office 365 customer you can manage this feature through the Security & Compliance Center.</span></span> 

- <span data-ttu-id="c4ca2-110">No centro de conformidade do & de segurança do Office 365, os administradores de locatários podem ativar ou desativar o recurso por meio da proteção contra falsificação na política de anti-phishing.</span><span class="sxs-lookup"><span data-stu-id="c4ca2-110">In the Office 365 Security & Compliance Center, tenant admins can turn the feature on, or off, through the Anti-spoofing protection under the Anti-Phish policy.</span></span> <span data-ttu-id="c4ca2-111">Além disso, ele pode ser gerenciado por meio do cmdlet "Set-AntiPhishPolicy".</span><span class="sxs-lookup"><span data-stu-id="c4ca2-111">Additionally, it can be managed through the ‘Set-AntiPhishPolicy’ cmdlet.</span></span> <span data-ttu-id="c4ca2-112">Para obter mais detalhes, consulte proteção contra phishing no Office 365 e Set-AntiPhishPolicy.</span><span class="sxs-lookup"><span data-stu-id="c4ca2-112">For more details, see Anti-phishing protection in Office 365 and Set-AntiPhishPolicy.</span></span>

    ![Edição de remetentes não autenticados na interface gráfica.](media/unverified-sender-article-editing-unauthenticated-senders.jpg)

- <span data-ttu-id="c4ca2-114">Se um administrador identificou um falso positivo e um remetente não deve receber o tratamento de remetente não verificado, eles podem executar uma das ações a seguir para adicionar o remetente à lista de permissões de falsificação de inteligência de falsificação:</span><span class="sxs-lookup"><span data-stu-id="c4ca2-114">If an admin has identified a false positive, and a sender should not be receiving the unverified sender treatment they can take one of the following actions to add the sender to the Spoof Intelligence spoof allow list:</span></span>
        
    - <span data-ttu-id="c4ca2-115">Adicionar o par de domínios por meio da compreensão de inteligência de falsificação.</span><span class="sxs-lookup"><span data-stu-id="c4ca2-115">Add the domain pair through the Spoof Intelligence Insight.</span></span> <span data-ttu-id="c4ca2-116">Para obter mais detalhes, consulte Walkthrough: spoof Intelligence percepção</span><span class="sxs-lookup"><span data-stu-id="c4ca2-116">For more details, see Walkthrough: spoof intelligence insight</span></span>
                
    - <span data-ttu-id="c4ca2-117">Adicione o par de domínios através do cmdlet PhishFilterPolicy.</span><span class="sxs-lookup"><span data-stu-id="c4ca2-117">Add the domain pair through the PhishFilterPolicy cmdlet.</span></span> <span data-ttu-id="c4ca2-118">Para obter mais detalhes, consulte Set-PhishFilterPolicy e anti-falsification Protection in Office 365</span><span class="sxs-lookup"><span data-stu-id="c4ca2-118">For more details, see Set-PhishFilterPolicy and Anti-spoofing protection in Office 365</span></span>

<span data-ttu-id="c4ca2-119">Além disso, não aplicamos o tratamento de remetente não verificado se ele foi entregue à caixa de entrada por meio de uma lista de permissões de administração, incluindo regras de transporte de email (ETRs), lista de domínios seguros (política antispam), lista de remetentes seguros ou um usuário tiver definido esse usuário como um "remetente seguro" em seu postal.</span><span class="sxs-lookup"><span data-stu-id="c4ca2-119">Additionally, we do not apply the unverified sender treatment if it was delivered to the inbox via an admin allow list, including Email Transport Rules (ETRs), Safe Domain List (Anti-Spam Policy), Safe Sender List or a user has set this user as a “Safe Sender” in their inbox.</span></span>

### <a name="you-see-a--in-the-sender-image"></a><span data-ttu-id="c4ca2-120">Você vê um '? ' na imagem do remetente</span><span class="sxs-lookup"><span data-stu-id="c4ca2-120">You see a '?' in the sender image</span></span>

<span data-ttu-id="c4ca2-121">Quando o Outlook.com e o Outlook na Web não conseguem verificar a identidade do remetente usando técnicas de autenticação de email, eles exibem um '? ' na foto do remetente.</span><span class="sxs-lookup"><span data-stu-id="c4ca2-121">When Outlook.com and Outlook on the web can't verify the identity of the sender using email authentication techniques, they display a '?' in the sender photo.</span></span> 

![A mensagem não passou na verificação](media/message-did-not-pass-verification.jpg)

<span data-ttu-id="c4ca2-123">Nem todas as mensagens que não são autenticadas são mal-intencionadas.</span><span class="sxs-lookup"><span data-stu-id="c4ca2-123">Not every message that fails to authenticate is malicious.</span></span> <span data-ttu-id="c4ca2-124">No entanto, você deve ter cuidado para interagir com mensagens que não são autenticadas se você não reconhece o remetente.</span><span class="sxs-lookup"><span data-stu-id="c4ca2-124">However, you should be careful about interacting with messages that don't authenticate if you don't recognize the sender.</span></span> <span data-ttu-id="c4ca2-125">Ou, se você reconhece um remetente que normalmente não tem um '? ' na imagem do remetente, mas, repentinamente, você começa a vê-lo, que pode ser um sinal de que o remetente está sendo falsificado.</span><span class="sxs-lookup"><span data-stu-id="c4ca2-125">Or, if you recognize a sender that normally doesn't have a '?' in the sender image, but you suddenly start seeing it, that could be a sign the sender is being spoofed.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="c4ca2-126">Perguntas frequentes</span><span class="sxs-lookup"><span data-stu-id="c4ca2-126">Frequently asked questions</span></span>

### <a name="what-criteria-does-outlookcom-and-outlook-on-the-web-use-to-add-the--and-the-via-properties"></a><span data-ttu-id="c4ca2-127">Que critérios o Outlook.com e o Outlook na Web usam para adicionar as propriedades '? ' e ' via '?</span><span class="sxs-lookup"><span data-stu-id="c4ca2-127">What criteria does Outlook.com and Outlook on the web use to add the '?' and the 'via' properties?</span></span>

<span data-ttu-id="c4ca2-128">Para o '? ' na imagem do remetente: Outlook.com requer que a mensagem passe o SPF ou a autenticação do DKIM.</span><span class="sxs-lookup"><span data-stu-id="c4ca2-128">For the '?' in the sender image:  Outlook.com requires that the message pass either SPF or DKIM authentication.</span></span> <span data-ttu-id="c4ca2-129">Para obter mais detalhes, consulte [set up SPF in Office 365 para ajudar a impedir](set-up-spf-in-office-365-to-help-prevent-spoofing.md) a falsificação e [uso do DKIM para validar emails de saída enviados do seu domínio personalizado no Office 365](use-dkim-to-validate-outbound-email.md).</span><span class="sxs-lookup"><span data-stu-id="c4ca2-129">For more details, see [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md) and [Use DKIM to validate outbound email sent from your custom domain in Office 365](use-dkim-to-validate-outbound-email.md).</span></span>

<span data-ttu-id="c4ca2-130">Para o via Tag: se o domínio no endereço de for diferente do domínio na assinatura do DKIM ou do email SMTP de, Outlook.com exibe o domínio em um desses dois campos (preferência à assinatura DKIM).</span><span class="sxs-lookup"><span data-stu-id="c4ca2-130">For the via tag: If the domain in the From address is different from the domain in the DKIM signature or the SMTP MAIL FROM, Outlook.com displays the domain in one of those two fields (preferring the DKIM signature).</span></span>

### <a name="how-do-i-remove-the-"></a><span data-ttu-id="c4ca2-131">Como remover o '? '</span><span class="sxs-lookup"><span data-stu-id="c4ca2-131">How do I remove the '?'</span></span>

<span data-ttu-id="c4ca2-132">Para o '? ' na imagem do remetente: como um remetente, você deve autenticar sua mensagem com o SPF ou o DKIM.</span><span class="sxs-lookup"><span data-stu-id="c4ca2-132">For the '?' in the sender image: As a sender, you should authenticate your message with either SPF or DKIM.</span></span>

<span data-ttu-id="c4ca2-133">Para o via Tag: como um remetente, você deve garantir que o domínio na assinatura DKIM ou o email SMTP de seja o mesmo que ou seja um subdomínio de, o domínio no endereço de.</span><span class="sxs-lookup"><span data-stu-id="c4ca2-133">For the via tag: As a sender, you should ensure that either the domain in the DKIM signature or the SMTP MAIL FROM is the same as, or is a subdomain of, the domain in the From address.</span></span>

### <a name="does-outlookcom-and-outlook-on-the-web-show-this-for-every-message-that-doesnt-pass-authentication"></a><span data-ttu-id="c4ca2-134">O Outlook.com e o Outlook na Web mostram isso para cada mensagem que não aprova a autenticação?</span><span class="sxs-lookup"><span data-stu-id="c4ca2-134">Does Outlook.com and Outlook on the web show this for every message that doesn’t pass authentication?</span></span>

<span data-ttu-id="c4ca2-135">Não necessariamente.</span><span class="sxs-lookup"><span data-stu-id="c4ca2-135">Not necessarily.</span></span> <span data-ttu-id="c4ca2-136">O Outlook.com e o Outlook na Web podem ter outras propriedades dentro da mensagem para autenticar o remetente.</span><span class="sxs-lookup"><span data-stu-id="c4ca2-136">Outlook.com and Outlook on the web may have other properties within the message to authenticate the sender.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4ca2-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c4ca2-137">Related topics</span></span>

[<span data-ttu-id="c4ca2-138">Ajudar a proteger sua conta de email do Outlook.com</span><span class="sxs-lookup"><span data-stu-id="c4ca2-138">Help protect your Outlook.com email account</span></span>](https://support.office.com/article/a4f20fc5-4307-4ece-8231-6d4d4bd8a9ba)

[<span data-ttu-id="c4ca2-139">Lidar com abuso, phishing ou falsificação no Outlook.com</span><span class="sxs-lookup"><span data-stu-id="c4ca2-139">Deal with abuse, phishing, or spoofing in Outlook.com</span></span>](https://support.office.com/article/0d882ea5-eedc-4bed-aebc-079ffa1105a3)

[<span data-ttu-id="c4ca2-140">Filtrar lixo eletrônico e spam no Outlook na Web</span><span class="sxs-lookup"><span data-stu-id="c4ca2-140">Filter junk email and spam in Outlook on the web</span></span>](https://support.office.com/article/db786e79-54e2-40cc-904f-d89d57b7f41d)

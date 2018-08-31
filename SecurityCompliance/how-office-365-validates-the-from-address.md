---
title: Como o Office 365 valida o endereço de para evitar phishing
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/11/2017
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- OWC150
- MET150
ms.assetid: eef8408b-54d3-4d7d-9cf7-ad2af10b2e0e
description: 'Para ajudar a impedir phishing, Office 365 e Outlook.com agora requerem conformidade RFC para do: endereços.'
ms.openlocfilehash: 562e08aa54cb6544beccb6f0e8760735f67b834b
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523495"
---
# <a name="how-office-365-validates-the-from-address-to-prevent-phishing"></a><span data-ttu-id="7d972-103">Como o Office 365 valida o endereço de para evitar phishing</span><span class="sxs-lookup"><span data-stu-id="7d972-103">How Office 365 validates the From address to prevent phishing</span></span>

<span data-ttu-id="7d972-p101">O Office 365 e contas de email do Outlook.com recebem um número cada vez maior de ataques de phishing. Uma técnica phishers usam é para enviar mensagens que têm valores para From: endereço que não são compatíveis com a [RFC 5322](https://tools.ietf.org/html/rfc5322). From: o endereço também é chamado de endereço de 5322.From. Para evitar esse tipo de phishing, Office 365 e Outlook.com exigem que as mensagens recebidas pelo serviço para incluir um compatível com RFC do: endereço, conforme descrito neste artigo.</span><span class="sxs-lookup"><span data-stu-id="7d972-p101">Office 365 and Outlook.com email accounts receive an increasingly large number of phishing attacks. One technique phishers use is to send messages that have values for the From: address that are not compliant with [RFC 5322](https://tools.ietf.org/html/rfc5322). The From: address is also called the 5322.From address. To help prevent this type of phishing, Office 365 and Outlook.com require messages received by the service to include an RFC-compliant From: address as described in this article.</span></span>
  
> [!NOTE]
> <span data-ttu-id="7d972-p102">As informações neste artigo exige que você tenha uma noção básica do formato geral dos endereços de email. Para obter mais informações, consulte [RFC 5322](https://tools.ietf.org/html/rfc5322) (particularmente seções 3.2.3, 3.4 e 3.4.1), [RFC 5321](https://tools.ietf.org/html/rfc5321), bem como [3696 RFC](https://tools.ietf.org/html/rfc3696). Este artigo fala sobre imposição de política para o endereço de 5322.From. Este artigo não é sobre o endereço de 5321.MailFrom.</span><span class="sxs-lookup"><span data-stu-id="7d972-p102">The information in this article requires you to have a basic understanding of the general format of email addresses. For more information, see [RFC 5322](https://tools.ietf.org/html/rfc5322) (particularly sections 3.2.3, 3.4, and 3.4.1), [RFC 5321](https://tools.ietf.org/html/rfc5321), as well as [RFC 3696](https://tools.ietf.org/html/rfc3696). This article is about policy enforcement for the 5322.From address. This article is not about the 5321.MailFrom address.</span></span> 
  
<span data-ttu-id="7d972-p103">Infelizmente, ainda há alguns servidores herdados de email na Internet que continuam a enviar mensagens que têm uma falta de email "legítimo" ou mal formados do: endereço. Se você receber o email regularmente de organizações que usam esses sistemas legados, incentive dessas organizações para atualizar seus servidores de email para cumprir os padrões de segurança moderno.</span><span class="sxs-lookup"><span data-stu-id="7d972-p103">Unfortunately, there are still some legacy email servers on the Internet that continue to send "legitimate" email messages that have a missing or malformed From: address. If you regularly receive email from organizations that use these legacy systems, encourage those organizations to update their mail servers to comply with modern security standards.</span></span>
  
<span data-ttu-id="7d972-114">Microsoft iniciará a aplicação do reforço das diretivas descrito neste artigo em 9 de novembro de 2017.</span><span class="sxs-lookup"><span data-stu-id="7d972-114">Microsoft will start rolling out enforcement of the policies described in this article on November 9, 2017.</span></span>
  
## <a name="how-office-365-enforces-the-use-of-a-valid-from-address-to-prevent-phishing-attacks"></a><span data-ttu-id="7d972-115">Como o Office 365 impõe o uso de um valor válido de: endereço a prevenir ataques de phishing</span><span class="sxs-lookup"><span data-stu-id="7d972-115">How Office 365 enforces the use of a valid From: address to prevent phishing attacks</span></span>

<span data-ttu-id="7d972-p104">O Office 365 está fazendo alterações à maneira como ele impõe o uso de From: endereço em mensagens recebidas para melhor protegê-lo contra ataques de phishing. Neste artigo:</span><span class="sxs-lookup"><span data-stu-id="7d972-p104">Office 365 is making changes to the way it enforces the use of the From: address in messages it receives in order to better protect you from phishing attacks. In this article:</span></span>
  
- [<span data-ttu-id="7d972-118">Todas as mensagens devem incluir um valor válido de: endereço</span><span class="sxs-lookup"><span data-stu-id="7d972-118">All messages must include a valid From: address</span></span>](how-office-365-validates-the-from-address.md#MustIncludeFromAddress)
    
- [<span data-ttu-id="7d972-119">Todas as mensagens devem incluir um valor válido de: endereço</span><span class="sxs-lookup"><span data-stu-id="7d972-119">All messages must include a valid From: address</span></span>](how-office-365-validates-the-from-address.md#MustIncludeFromAddress)
    
- [<span data-ttu-id="7d972-120">Formato de From: se você não incluir um nome de exibição de endereços</span><span class="sxs-lookup"><span data-stu-id="7d972-120">Format of the From: address if you don't include a display name</span></span>](how-office-365-validates-the-from-address.md#FormatNoDisplayName)
    
- [<span data-ttu-id="7d972-121">Formato de From: se você incluir um nome de exibição de endereços</span><span class="sxs-lookup"><span data-stu-id="7d972-121">Format of the From: address if you include a display name</span></span>](how-office-365-validates-the-from-address.md#FormatDisplayName)
    
- [<span data-ttu-id="7d972-122">Exemplos adicionais de válidas e inválidas de: endereços</span><span class="sxs-lookup"><span data-stu-id="7d972-122">Additional examples of valid and invalid From: addresses</span></span>](how-office-365-validates-the-from-address.md#Examples)
    
- [<span data-ttu-id="7d972-123">Suprimir as respostas automáticas para seu domínio personalizado sem quebrar From: política</span><span class="sxs-lookup"><span data-stu-id="7d972-123">Suppress auto-replies to your custom domain without breaking the From: policy</span></span>](how-office-365-validates-the-from-address.md#SuppressAutoReply)
    
- [<span data-ttu-id="7d972-124">Substituindo o Office 365 do: política de imposição de endereços</span><span class="sxs-lookup"><span data-stu-id="7d972-124">Overriding the Office 365 From: address enforcement policy</span></span>](how-office-365-validates-the-from-address.md#Override)
    
- [<span data-ttu-id="7d972-125">Outras maneiras de prevenir e proteger contra aos cybercrimes no Office 365</span><span class="sxs-lookup"><span data-stu-id="7d972-125">Other ways to prevent and protect against cybercrimes in Office 365</span></span>](how-office-365-validates-the-from-address.md#OtherProtection)
    
<span data-ttu-id="7d972-126">Enviar em nome de outro usuário não é afetado por essa alteração, para obter mais detalhes, leia o blog de Terry Zink "[que estamos falando quando nos referimos 'remetente' de um email?](https://blogs.msdn.microsoft.com/tzink/2017/06/22/what-do-we-mean-when-we-refer-to-the-sender-of-an-email/)".</span><span class="sxs-lookup"><span data-stu-id="7d972-126">Sending on behalf of another user is not affected by this change, for more details, read Terry Zink's blog "[What do we mean when we refer to the 'sender' of an email?](https://blogs.msdn.microsoft.com/tzink/2017/06/22/what-do-we-mean-when-we-refer-to-the-sender-of-an-email/)".</span></span>
  
### <a name="all-messages-must-include-a-valid-from-address"></a><span data-ttu-id="7d972-127">Todas as mensagens devem incluir um valor válido de: endereço</span><span class="sxs-lookup"><span data-stu-id="7d972-127">All messages must include a valid From: address</span></span>
<span data-ttu-id="7d972-128"><a name="MustIncludeFromAddress"> </a></span><span class="sxs-lookup"><span data-stu-id="7d972-128"></span></span>

<span data-ttu-id="7d972-p105">Algumas mensagens automatizadas não incluem um From: endereço quando eles forem enviados. No passado, quando o Office 365 ou Outlook.com recebeu uma mensagem sem um From: o serviço de endereço, adicionado o seguinte formato padrão do: endereço à mensagem para torná-lo o resultado final:</span><span class="sxs-lookup"><span data-stu-id="7d972-p105">Some automated messages don't include a From: address when they are sent. In the past, when Office 365 or Outlook.com received a message without a From: address, the service added the following default From: address to the message in order to make it deliverable:</span></span>
  
```
From: <>
```

<span data-ttu-id="7d972-p106">Iniciando 9 de novembro de 2017, Office 365 estarão disponíveis alterações aos seus servidores de email e data centers que imporá uma nova regra onde mensagens sem um From: endereço não será aceito pelo Office 365 ou Outlook.com. Em vez disso, todas as mensagens recebidas pelo Office 365 já deverá conter um valor válido de: endereço. Caso contrário, a mensagem será enviada para o lixo eletrônico ou itens excluídos pastas no Outlook.com e no Office 365.</span><span class="sxs-lookup"><span data-stu-id="7d972-p106">Starting November 9, 2017, Office 365 will be rolling out changes to its datacenters and mail servers which will enforce a new rule where messages without a From: address will no longer be accepted by Office 365 or Outlook.com. Instead, all messages received by Office 365 must already contain a valid From: address. Otherwise, the message will be sent to either the Junk Email or Deleted Items folders in Outlook.com and Office 365.</span></span> 
  
### <a name="syntax-overview-valid-format-for-the-from-address-for-office-365"></a><span data-ttu-id="7d972-134">Visão geral de sintaxe: formato válido para From: endereço para o Office 365</span><span class="sxs-lookup"><span data-stu-id="7d972-134">Syntax overview: Valid format for the From: address for Office 365</span></span>
<span data-ttu-id="7d972-135"><a name="SyntaxOverviewFromAddress"> </a></span><span class="sxs-lookup"><span data-stu-id="7d972-135"></span></span>

<span data-ttu-id="7d972-p107">O formato para o valor do campo From: endereço é definido detalhadamente nas várias RFCs. Há muitas variações endereçamento e o que podem ser considerado válidos ou inválidos. Para manter simples, a Microsoft recomenda que você use as definições e o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="7d972-p107">The format for the value of the From: address is defined in detail across several RFCs. There are many variations on addressing and what may be considered valid or invalid. To keep it simple, Microsoft recommends that you use the following format and definitions:</span></span>
  
```
From: "displayname " <emailaddress >
```

<span data-ttu-id="7d972-139">Onde:</span><span class="sxs-lookup"><span data-stu-id="7d972-139">Where:</span></span>
  
- <span data-ttu-id="7d972-p108">(Opcional)  *DisplayName* é uma frase que descreve o proprietário do endereço de email. Por exemplo, isso pode ser um nome mais intuitivo para descrever o remetente do nome da caixa de correio. Usando um nome de exibição é opcional. No entanto, se você optar por usar um nome para exibição, a Microsoft recomenda que você sempre coloque-o entre aspas conforme mostrado.</span><span class="sxs-lookup"><span data-stu-id="7d972-p108">(Optional)  *displayname*  is a phrase that describes the owner of the email address. For example, this might be a more user-friendly name to describe the sender than the name of the mailbox. Using a display name is optional. However, if you choose to use a display name, Microsoft recommends that you always enclose it within quotation marks as shown.</span></span> 
    
- <span data-ttu-id="7d972-144">(Necessário)  *EmailAddress* é formada pelo:</span><span class="sxs-lookup"><span data-stu-id="7d972-144">(Required)  *emailaddress*  is made up of:</span></span> 
    
  ```
  local-part @domain
  ```

    <span data-ttu-id="7d972-145">Onde:</span><span class="sxs-lookup"><span data-stu-id="7d972-145">Where:</span></span>
    
  - <span data-ttu-id="7d972-p109">(Necessário)  *parte de local* é uma cadeia de caracteres que identifica a caixa de correio associada ao endereço. Isso é exclusivo dentro do domínio. Muitas vezes, username ou o GUID do proprietário da caixa de correio é usado como o valor para a parte de local.</span><span class="sxs-lookup"><span data-stu-id="7d972-p109">(Required)  *local-part*  is a string that identifies the mailbox associated with the address. This is unique within the domain. Often, the mailbox owner's username or GUID is used as the value for the local-part.</span></span> 
    
  - <span data-ttu-id="7d972-149">(Necessário)  *domínio* é o nome de domínio totalmente qualificado (FQDN) do servidor de email que hospeda a caixa de correio identificada por parte local do endereço de email.</span><span class="sxs-lookup"><span data-stu-id="7d972-149">(Required)  *domain*  is the fully-qualified domain name (FQDN) of the mail server that hosts the mailbox identified by the local-part of the email address.</span></span> 
    
### <a name="format-of-the-from-address-if-you-dont-include-a-display-name"></a><span data-ttu-id="7d972-150">Formato de From: se você não incluir um nome de exibição de endereços</span><span class="sxs-lookup"><span data-stu-id="7d972-150">Format of the From: address if you don't include a display name</span></span>
<span data-ttu-id="7d972-151"><a name="FormatNoDisplayName"> </a></span><span class="sxs-lookup"><span data-stu-id="7d972-151"></span></span>

<span data-ttu-id="7d972-p110">Uma formatada corretamente do: endereço que não inclua um nome de exibição inclui apenas um único endereço de email com ou sem colchetes angulares. A Microsoft recomenda que você não separe os colchetes angulares com espaços. Além disso, não inclua qualquer coisa após o endereço de email.</span><span class="sxs-lookup"><span data-stu-id="7d972-p110">A properly formatted From: address that does not include a display name includes only a single email address with or without angle brackets. Microsoft recommends that you do not separate the angle brackets with spaces. In addition, don't include anything after the email address.</span></span>
  
<span data-ttu-id="7d972-155">Os exemplos a seguir são válidos:</span><span class="sxs-lookup"><span data-stu-id="7d972-155">The following examples are valid:</span></span>
  
```
From: sender@contoso.com
```

```
From: <sender@contoso.com>
```

<span data-ttu-id="7d972-156">O exemplo a seguir é válido, mas não é recomendado porque ele contém espaços entre os colchetes angulares e o endereço de email:</span><span class="sxs-lookup"><span data-stu-id="7d972-156">The following example is valid but not recommended because it contains spaces between the angle brackets and the email address:</span></span>
  
```
From: < sender@contoso.com >
```

<span data-ttu-id="7d972-157">O exemplo a seguir é inválido, pois ele contém texto após o endereço de email:</span><span class="sxs-lookup"><span data-stu-id="7d972-157">The following example is invalid because it contains text after the email address:</span></span>
  
```
From: "Office 365" <sender@contoso.com> (Sent by a process)
```

### <a name="format-of-the-from-address-if-you-include-a-display-name"></a><span data-ttu-id="7d972-158">Formato de From: se você incluir um nome de exibição de endereços</span><span class="sxs-lookup"><span data-stu-id="7d972-158">Format of the From: address if you include a display name</span></span>
<span data-ttu-id="7d972-159"><a name="FormatDisplayName"> </a></span><span class="sxs-lookup"><span data-stu-id="7d972-159"></span></span>

<span data-ttu-id="7d972-160">Para partir: endereços que incluem um valor para o nome para exibição, as seguintes regras se aplicam:</span><span class="sxs-lookup"><span data-stu-id="7d972-160">For From: addresses that include a value for the display name, the following rules apply:</span></span>
  
- <span data-ttu-id="7d972-p111">Se o endereço do remetente inclui um nome de exibição e o nome para exibição inclui uma vírgula, o nome para exibição deve estar entre aspas. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="7d972-p111">If the sender address includes a display name, and the display name includes a comma, then the display name must be enclosed within quotation marks. For example:</span></span>
    
    <span data-ttu-id="7d972-163">O exemplo a seguir é válido:</span><span class="sxs-lookup"><span data-stu-id="7d972-163">The following example is valid:</span></span>
    
  ```
  From: "Sender, Example" <sender.example@contoso.com>
  ```

    <span data-ttu-id="7d972-164">O exemplo a seguir não é válido:</span><span class="sxs-lookup"><span data-stu-id="7d972-164">The following example is not valid:</span></span>
    
  ```
  From: Sender, Example <sender.example@contoso.com>
  ```

    <span data-ttu-id="7d972-165">Não é válido de acordo com a RFC 5322 não colocar o nome de exibição aspas se esse nome de exibição inclui uma vírgula.</span><span class="sxs-lookup"><span data-stu-id="7d972-165">Not enclosing the display name in quotation marks if that display name includes a comma is invalid according to RFC 5322.</span></span>
    
    <span data-ttu-id="7d972-166">Como prática recomendada, colocar aspas em torno do nome de exibição, independentemente de se há ou não é uma vírgula entre o nome para exibição.</span><span class="sxs-lookup"><span data-stu-id="7d972-166">As a best practice, put quote marks around the display name regardless of whether or not there is a comma within the display name.</span></span>
    
- <span data-ttu-id="7d972-167">Se o endereço do remetente inclui um nome para exibição, o endereço de email deve ser colocado entre colchetes angulares.</span><span class="sxs-lookup"><span data-stu-id="7d972-167">If the sender address includes a display name, then the email address must be enclosed within angle brackets.</span></span>
    
    <span data-ttu-id="7d972-168">Como prática recomendada, a Microsoft recomenda que você inserir um espaço entre o nome para exibição e o endereço de email.</span><span class="sxs-lookup"><span data-stu-id="7d972-168">As a best practice, Microsoft strongly recommends that you insert a space between the display name and the email address.</span></span>
    
### <a name="additional-examples-of-valid-and-invalid-from-addresses"></a><span data-ttu-id="7d972-169">Exemplos adicionais de válidas e inválidas de: endereços</span><span class="sxs-lookup"><span data-stu-id="7d972-169">Additional examples of valid and invalid From: addresses</span></span>
<span data-ttu-id="7d972-170"><a name="Examples"> </a></span><span class="sxs-lookup"><span data-stu-id="7d972-170"></span></span>

- <span data-ttu-id="7d972-171">Válido:</span><span class="sxs-lookup"><span data-stu-id="7d972-171">Valid:</span></span>
    
  ```
  From: "Office 365" <sender@contoso.com>
  ```

- <span data-ttu-id="7d972-p112">Inválido. O endereço de email não está incluído nos colchetes angulares:</span><span class="sxs-lookup"><span data-stu-id="7d972-p112">Invalid. The email address is not enclosed with angle brackets:</span></span>
    
  ```
  From: Office 365 sender@contoso.com
  ```

- <span data-ttu-id="7d972-p113">Válido, mas não recomendado. O nome para exibição não está entre aspas. Como prática recomendada, sempre coloque o nome de exibição entre aspas:</span><span class="sxs-lookup"><span data-stu-id="7d972-p113">Valid, but not recommended. The display name is not in quotes. As a best practice, always put quotation marks around the display name:</span></span>
    
  ```
  From: Office 365 <sender@contoso.com>
  ```

- <span data-ttu-id="7d972-p114">Inválido. Tudo está entre aspas, não apenas o nome de exibição:</span><span class="sxs-lookup"><span data-stu-id="7d972-p114">Invalid. Everything is enclosed within quotation marks, not just the display name:</span></span>
    
  ```
  From: "Office 365 <sender@contoso.com>"
  ```

- <span data-ttu-id="7d972-p115">Inválido. Não há nenhum ângulo entre colchetes o endereço de email:</span><span class="sxs-lookup"><span data-stu-id="7d972-p115">Invalid. There are no angle brackets around the email address:</span></span>
    
  ```
  From: "Office 365 <sender@contoso.com>" sender@contoso.com
  ```

- <span data-ttu-id="7d972-p116">Inválido. Não há nenhum espaço entre o nome para exibição e colchetes esquerdo:</span><span class="sxs-lookup"><span data-stu-id="7d972-p116">Invalid. There is no space between the display name and left angle bracket:</span></span>
    
  ```
  From: Office 365<sender@contoso.com>
  ```

- <span data-ttu-id="7d972-p117">Inválido. Não há nenhum espaço entre o quotation mark fechamento em torno do nome de exibição e o colchete esquerdo de ângulo.</span><span class="sxs-lookup"><span data-stu-id="7d972-p117">Invalid. There is no space between the closing quotation mark around the display name and the left angle bracket.</span></span>
    
  ```
  From: "Office 365"<sender@contoso.com>
  ```

### <a name="suppress-auto-replies-to-your-custom-domain-without-breaking-the-from-policy"></a><span data-ttu-id="7d972-185">Suprimir as respostas automáticas para seu domínio personalizado sem quebrar From: política</span><span class="sxs-lookup"><span data-stu-id="7d972-185">Suppress auto-replies to your custom domain without breaking the From: policy</span></span>
<span data-ttu-id="7d972-186"><a name="SuppressAutoReply"> </a></span><span class="sxs-lookup"><span data-stu-id="7d972-186"></span></span>

<span data-ttu-id="7d972-p118">Com o novo com base em: aplicação de políticas, você não poderá mais usar do: \< \> para suprimir as respostas automáticas. Em vez disso, você precisará configurar um registro MX nulo para seu domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="7d972-p118">With the new From: policy enforcement, you can no longer use From: \<\> to suppress auto-replies. Instead, you need to set up a null MX record for your custom domain.</span></span>
  
<span data-ttu-id="7d972-p119">O registro do mail exchanger (MX) é um registro de recurso no DNS que identifica o servidor de email que recebe o email para seu domínio. As respostas automáticas (e todas as respostas) são suprimidas naturalmente porque não há nenhum endereço publicado para o qual o servidor de resposta pode enviar mensagens.</span><span class="sxs-lookup"><span data-stu-id="7d972-p119">The mail exchanger (MX) record is a resource record in DNS that identifies the mail server that receives mail for your domain. Auto-replies (and all replies) are naturally suppressed because there is no published address to which the responding server can send messages.</span></span>
  
<span data-ttu-id="7d972-191">Quando você configurar um nulo registro MX para seu domínio personalizado:</span><span class="sxs-lookup"><span data-stu-id="7d972-191">When you set up a null MX record for your custom domain:</span></span>
  
- <span data-ttu-id="7d972-p120">Escolha um domínio do qual deseja enviar mensagens que não aceita (receber) emails. Por exemplo, se o seu domínio primário for contoso.com, você pode escolher noreply.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="7d972-p120">Choose a domain from which to send messages that doesn't accept (receive) email. For example, if your primary domain is contoso.com, you might choose noreply.contoso.com.</span></span>
    
- <span data-ttu-id="7d972-p121">Configure o registro MX nulo para seu domínio. Um registro de MX nulo consiste em um único ponto, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="7d972-p121">Set up the null MX record for your domain. A null MX record consists of a single dot, for example:</span></span>
    
  ```
  noreply.contoso.com IN MX .
  ```

<span data-ttu-id="7d972-196">Para obter mais informações sobre como publicar um MX nulo, consulte [RFC 7505](https://tools.ietf.org/html/rfc7505).</span><span class="sxs-lookup"><span data-stu-id="7d972-196">For more information about publishing a null MX, see [RFC 7505](https://tools.ietf.org/html/rfc7505).</span></span>
  
### <a name="overriding-the-office-365-from-address-enforcement-policy"></a><span data-ttu-id="7d972-197">Substituindo o Office 365 do: política de imposição de endereços</span><span class="sxs-lookup"><span data-stu-id="7d972-197">Overriding the Office 365 From: address enforcement policy</span></span>
<span data-ttu-id="7d972-198"><a name="Override"> </a></span><span class="sxs-lookup"><span data-stu-id="7d972-198"></span></span>

<span data-ttu-id="7d972-199">Uma vez concluída roll a nova política, você somente poderá ignorar essa diretiva para emails de entrada, que você recebe do Office 365 usando um dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="7d972-199">Once roll out of the new policy is complete, you can only bypass this policy for inbound mail you receive from Office 365 by using one of the following methods:</span></span> 
  
- <span data-ttu-id="7d972-200">Listas de permissões de IP</span><span class="sxs-lookup"><span data-stu-id="7d972-200">IP allow lists</span></span>
    
- <span data-ttu-id="7d972-201">Regras de fluxo de correio Exchange Online</span><span class="sxs-lookup"><span data-stu-id="7d972-201">Exchange Online mail flow rules</span></span>
    
<span data-ttu-id="7d972-p122">A Microsoft recomenda contra substituir a imposição de From: política. Substituir essa diretiva pode aumentar o risco de sua organização de exposição a spam, phishing e aos outros cybercrimes.</span><span class="sxs-lookup"><span data-stu-id="7d972-p122">Microsoft strongly recommends against overriding the enforcement of the From: policy. Overriding this policy can increase your organization's risk of exposure to spam, phishing, and other cybercrimes.</span></span>
  
<span data-ttu-id="7d972-p123">Você não pode substituir essa diretiva para mensagens de saída, que você pode enviar no Office 365. Além disso, o Outlook.com não permitirá substituições de qualquer tipo, mesmo por meio de suporte.</span><span class="sxs-lookup"><span data-stu-id="7d972-p123">You cannot override this policy for outbound mail you send in Office 365. In addition, Outlook.com will not allow overrides of any kind, even through support.</span></span> 
  
### <a name="other-ways-to-prevent-and-protect-against-cybercrimes-in-office-365"></a><span data-ttu-id="7d972-206">Outras maneiras de prevenir e proteger contra aos cybercrimes no Office 365</span><span class="sxs-lookup"><span data-stu-id="7d972-206">Other ways to prevent and protect against cybercrimes in Office 365</span></span>
<span data-ttu-id="7d972-207"><a name="OtherProtection"> </a></span><span class="sxs-lookup"><span data-stu-id="7d972-207"></span></span>

<span data-ttu-id="7d972-208">Para obter mais informações sobre como você pode fortalecer a sua organização em relação aos cybercrimes como o phishing, spam, violações de dados e outras ameaças, consulte [práticas recomendadas de segurança para o Office 365](https://support.office.com/article/9295e396-e53d-49b9-ae9b-0b5828cdedc3).</span><span class="sxs-lookup"><span data-stu-id="7d972-208">For more information on how you can strengthen your organization against cybercrimes like phishing, spamming, data breaches, and other threats, see [Security best practices for Office 365](https://support.office.com/article/9295e396-e53d-49b9-ae9b-0b5828cdedc3).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="7d972-209">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7d972-209">Related Topics</span></span>

[<span data-ttu-id="7d972-210">Mnsagens backscatter e EOP</span><span class="sxs-lookup"><span data-stu-id="7d972-210">Backscatter messages and EOP</span></span>](https://technet.microsoft.com/en-us/library/dn499795%28v=exchg.150%29.aspx)
  


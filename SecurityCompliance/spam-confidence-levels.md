---
title: Níveis de confiança de spam
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 10/2/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 34681000-0022-4b92-b38a-e32b3ed96bf6
ms.collection:
- M365-security-compliance
description: Quando uma mensagem de email passa pela filtragem de spam, recebe uma pontuação de spam. Essa pontuação é mapeada para uma classificação individual de Nível de Confiança de Spam (SCL) em um cabeçalho X. O serviço executa ações nas mensagens, dependendo da interpretação da confiança do spam da classificação SCL. A tabela a seguir mostra como as diferentes classificações SCL são interpretadas pelos filtros e a ação padrão tomada em mensagens de entrada para cada classificação.
ms.openlocfilehash: 1822fa50f9815397513fddf7a2024a99277cbb28
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30275641"
---
# <a name="spam-confidence-levels"></a><span data-ttu-id="a98a7-106">Níveis de confiança de spam</span><span class="sxs-lookup"><span data-stu-id="a98a7-106">Spam confidence levels</span></span>

<span data-ttu-id="a98a7-p102">Quando uma mensagem de email passa pela filtragem de spam, recebe uma pontuação de spam. Essa pontuação é mapeada para uma classificação individual de Nível de Confiança de Spam (SCL) em um cabeçalho X. O serviço executa ações nas mensagens, dependendo da interpretação da confiança do spam da classificação SCL. A tabela a seguir mostra como as diferentes classificações SCL são interpretadas pelos filtros e a ação padrão tomada em mensagens de entrada para cada classificação.</span><span class="sxs-lookup"><span data-stu-id="a98a7-p102">When an email message goes through spam filtering it is assigned a spam score. That score is mapped to an individual Spam Confidence Level (SCL) rating and stamped in an X-header. The service takes actions upon the messages depending upon the spam confidence interpretation of the SCL rating. The following table shows how the different SCL ratings are interpreted by the filters and the default action that is taken on inbound messages for each rating.</span></span>
  
|<span data-ttu-id="a98a7-111">**Classificação SCL**</span><span class="sxs-lookup"><span data-stu-id="a98a7-111">**SCL Rating**</span></span>|<span data-ttu-id="a98a7-112">**Interpretação de confiança de spam**</span><span class="sxs-lookup"><span data-stu-id="a98a7-112">**Spam Confidence Interpretation**</span></span>|<span data-ttu-id="a98a7-113">**Ação padrão**</span><span class="sxs-lookup"><span data-stu-id="a98a7-113">**Default Action**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a98a7-114">-1</span><span class="sxs-lookup"><span data-stu-id="a98a7-114">-1</span></span>  <br/> |<span data-ttu-id="a98a7-115">Não spam vindo de um remetente seguro, destinatário seguro ou endereço IP listado seguro (parceiro confiável)</span><span class="sxs-lookup"><span data-stu-id="a98a7-115">Non-spam coming from a safe sender, safe recipient, or safe listed IP address (trusted partner)</span></span>  <br/> |<span data-ttu-id="a98a7-116">Entregar a mensagem para a caixa de entrada do destinatário.</span><span class="sxs-lookup"><span data-stu-id="a98a7-116">Deliver the message to the recipients' inbox.</span></span>  <br/> |
|<span data-ttu-id="a98a7-117">0, 1</span><span class="sxs-lookup"><span data-stu-id="a98a7-117">0, 1</span></span>  <br/> |<span data-ttu-id="a98a7-118">Não spam porque a mensagem foi verificada e considerada como limpa</span><span class="sxs-lookup"><span data-stu-id="a98a7-118">Non-spam because the message was scanned and determined to be clean</span></span>  <br/> |<span data-ttu-id="a98a7-119">Entregar a mensagem para a caixa de entrada do destinatário.</span><span class="sxs-lookup"><span data-stu-id="a98a7-119">Deliver the message to the recipients' inbox.</span></span>  <br/> |
|<span data-ttu-id="a98a7-120">5, 6</span><span class="sxs-lookup"><span data-stu-id="a98a7-120">5, 6</span></span>  <br/> | <span data-ttu-id="a98a7-121">Spam</span><span class="sxs-lookup"><span data-stu-id="a98a7-121">Spam</span></span>  <br/> |<span data-ttu-id="a98a7-122">Entregar a mensagem na pasta Lixo Eletrônico do destinatário.</span><span class="sxs-lookup"><span data-stu-id="a98a7-122">Deliver the message to the recipients' Junk Email folder.</span></span>  <br/> |
|<span data-ttu-id="a98a7-123">7, 8, 9</span><span class="sxs-lookup"><span data-stu-id="a98a7-123">7, 8, 9</span></span>  <br/> |<span data-ttu-id="a98a7-124">Spam de alta confiança</span><span class="sxs-lookup"><span data-stu-id="a98a7-124">High confidence spam</span></span>  <br/> |<span data-ttu-id="a98a7-125">Entregar a mensagem na pasta Lixo Eletrônico do destinatário.</span><span class="sxs-lookup"><span data-stu-id="a98a7-125">Deliver the message to the recipients' Junk Email folder.</span></span>  <br/> |
   
> [!TIP]
> <span data-ttu-id="a98a7-p103">As classificações de SCL de 2, 3, 4, 7 e 8 não são definidas pelo serviço. Uma classificação de SCL de 5 ou 6 é considerada um spam suspeito, que é menos certo de ser spam do que a classificação de SCL 9, que é considerada determinados spam. Ações diferentes para spam e spam de alta confiança podem ser configuradas por meio de políticas de filtro de conteúdo no centro de administração do Exchange. Para obter mais informações, consulte [Configure Your spam filter Policies](configure-your-spam-filter-policies.md). Você também pode definir a classificação de SCL para mensagens que correspondem a condições específicas usando regras de transporte, conforme descrito em [usar regras de fluxo de emails para definir o SCL (nível de confiança de spam) em mensagens](use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages.md). Se você usar uma regra de transporte para definir SCL de 7, 8 ou 9, a mensagem será tratada como spam de alta confiança.</span><span class="sxs-lookup"><span data-stu-id="a98a7-p103">SCL ratings of 2, 3, 4, 7, and 8 are not set by the service. An SCL rating of 5 or 6 is considered suspected spam, which is less certain to be spam than an SCL rating of 9, which is considered certain spam. Different actions for spam and high confidence spam can be configured via your content filter policies in the Exchange admin center. For more information, see [Configure your spam filter policies](configure-your-spam-filter-policies.md). You can also set the SCL rating for messages that match specific conditions by using Transport rules, as described in [Use mail flow rules to set the spam confidence level (SCL) in messages](use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages.md). If you use a transport rule to set SCL of 7, 8, or 9 the message will be treated as high confidence spam.</span></span> 
  
||
|:-----|
|<span data-ttu-id="a98a7-p104">![O ícone pequeno do LinkedIn Learning](media/eac8a413-9498-4220-8544-1e37d1aaea13.png) **Começando a usar o Office 365?**         Descubra cursos em vídeo gratuitos para **Office 365 admins and IT pros**, oferecidos pelo LinkedIn Learning.</span><span class="sxs-lookup"><span data-stu-id="a98a7-p104">![The short icon for LinkedIn Learning](media/eac8a413-9498-4220-8544-1e37d1aaea13.png) **New to Office 365?**         Discover free video courses for **Office 365 admins and IT pros**, brought to you by LinkedIn Learning.</span></span> |
   


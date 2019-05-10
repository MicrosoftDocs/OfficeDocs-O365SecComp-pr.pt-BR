---
title: Criptografia de mensagem avançada do Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.date: 4/30/2019
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
description: A criptografia de mensagem avançada no Office 365 ajuda as organizações a cumprir suas obrigações de conformidade, permitindo que os administradores expirem e revogassem o acesso por meio de um portal da Web do Office 365 para emails criptografados.
ms.openlocfilehash: a775803a8d2678441f319c0145e96e7d19c26f7e
ms.sourcegitcommit: 8eb3cb4ec45ae0bb75fde249e35c4bc3d263b84f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/30/2019
ms.locfileid: "33506703"
---
# <a name="office-365-advanced-message-encryption"></a><span data-ttu-id="7fe9e-103">Criptografia de mensagem avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="7fe9e-103">Office 365 Advanced Message Encryption</span></span>

<span data-ttu-id="7fe9e-104">A criptografia de mensagem avançada do Office 365 está disponível na parte superior da criptografia de mensagem do Office 365 em determinadas assinaturas.</span><span class="sxs-lookup"><span data-stu-id="7fe9e-104">Office 365 Advanced Message Encryption is available on top of Office 365 Message Encryption in certain subscriptions.</span></span> <span data-ttu-id="7fe9e-105">A criptografia avançada de mensagens está incluída no [Microsoft 365 Enterprise E5](https://www.microsoft.com/microsoft-365/enterprise/home), no Office 365 Enterprise E5 e no Office 365 Education a5.</span><span class="sxs-lookup"><span data-stu-id="7fe9e-105">Advanced Message Encryption is included in [Microsoft 365 Enterprise E5](https://www.microsoft.com/microsoft-365/enterprise/home), Office 365 Enterprise E5, and Office 365 Education A5.</span></span> <span data-ttu-id="7fe9e-106">Se sua organização tiver uma assinatura do Office 365 que não inclua a criptografia de mensagem avançada do Office 365, você poderá comprar a criptografia de mensagem avançada como um complemento com a conformidade E5 do SKU de conformidade avançada.</span><span class="sxs-lookup"><span data-stu-id="7fe9e-106">If your organization has an Office 365 subscription that does not include Office 365 Advanced Message Encryption, you can purchase Advanced Message Encryption as an add-on with E5 Compliance of the Advanced Compliance SKU.</span></span>

<span data-ttu-id="7fe9e-107">Este artigo faz parte de uma série maior de artigos sobre a [criptografia de mensagens do Office 365](ome.md).</span><span class="sxs-lookup"><span data-stu-id="7fe9e-107">This article is part of a larger series of articles about [Office 365 Message Encryption](ome.md).</span></span>

<span data-ttu-id="7fe9e-108">A criptografia de mensagem avançada no Office 365 ajuda os clientes a cumprir as obrigações de conformidade que exigem controles mais flexíveis sobre destinatários externos e seu acesso a emails criptografados.</span><span class="sxs-lookup"><span data-stu-id="7fe9e-108">Advanced Message Encryption in Office 365 helps customers meet compliance obligations that require more flexible controls over external recipients and their access to encrypted emails.</span></span> <span data-ttu-id="7fe9e-109">Com a criptografia de mensagem avançada no Office 365, você pode controlar emails confidenciais compartilhados fora da organização com políticas automáticas.</span><span class="sxs-lookup"><span data-stu-id="7fe9e-109">With Advanced Message Encryption in Office 365, you can control sensitive emails shared outside the organization with automatic policies.</span></span> <span data-ttu-id="7fe9e-110">Você configura essas políticas para identificar tipos de informações confidenciais, como PII, finanças ou IDs de integridade, ou pode usar palavras-chave para melhorar a proteção.</span><span class="sxs-lookup"><span data-stu-id="7fe9e-110">You configure these policies to identify sensitive information types such as PII, Financial, or Health IDs, or you can use keywords to enhance protection.</span></span> <span data-ttu-id="7fe9e-111">Depois de configurar as políticas, você emparelhará políticas com os modelos de email com identidade visual personalizada e, em seguida, adicionará uma data de expiração para obter controle adicional para emails que se encaixam na política.</span><span class="sxs-lookup"><span data-stu-id="7fe9e-111">Once you've configured the policies, you pair policies with a custom branded email templates and then add an expiration date for additional control for emails that fit the policy.</span></span> <span data-ttu-id="7fe9e-112">Além disso, os administradores podem controlar ainda mais os emails criptografados acessados externamente por meio de um portal da Web seguro revogando o acesso ao email a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="7fe9e-112">Additionally, admins can further control encrypted emails accessed externally through a secure web portal by revoking access to the mail at any time.</span></span>

<span data-ttu-id="7fe9e-113">Você só pode definir uma expiração para e revogar emails enviados para destinatários externos.</span><span class="sxs-lookup"><span data-stu-id="7fe9e-113">You can only set an expiration for and revoke emails  sent to external recipients.</span></span>

<span data-ttu-id="7fe9e-114">Com a criptografia de mensagem avançada do Office 365, sempre que você aplicar a identidade visual personalizada, o Office 365 aplica o wrapper a emails que se ajustam à regra de fluxo de emails para a qual você aplica o modelo.</span><span class="sxs-lookup"><span data-stu-id="7fe9e-114">With Office 365 Advanced Message Encryption, any time you apply custom branding, the Office 365 applies the wrapper to email that fits the mail flow rule to which you apply the template.</span></span> <span data-ttu-id="7fe9e-115">Além disso, a expiração só poderá ser usada se a identidade visual personalizada for usada.</span><span class="sxs-lookup"><span data-stu-id="7fe9e-115">In addition, expiration can only be used if custom branding is used.</span></span> <span data-ttu-id="7fe9e-116">Só é possível revogar mensagens recebidas pelo portal.</span><span class="sxs-lookup"><span data-stu-id="7fe9e-116">You can only revoke messages that are received through the portal.</span></span>

## <a name="get-started-with-office-365-advanced-message-encryption"></a><span data-ttu-id="7fe9e-117">Introdução à criptografia de mensagem avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="7fe9e-117">Get started with Office 365 Advanced Message Encryption</span></span>

<span data-ttu-id="7fe9e-118">Os tópicos a seguir descrevem como configurar e usar a criptografia de mensagem avançada.</span><span class="sxs-lookup"><span data-stu-id="7fe9e-118">The following topics describe how you set up and use Advanced Message Encryption.</span></span>

<span data-ttu-id="7fe9e-119">Sua organização deve ter uma assinatura que inclua a criptografia de mensagem avançada do Office 365.</span><span class="sxs-lookup"><span data-stu-id="7fe9e-119">Your organization must have a subscription that includes Office 365 Advanced Message Encryption.</span></span> <span data-ttu-id="7fe9e-120">Para obter informações detalhadas sobre assinaturas suportadas, consulte a [Descrição de política de mensagens e serviço de conformidade](https://docs.microsoft.com/en-us/office365/servicedescriptions/exchange-online-service-description/message-policy-and-compliance).</span><span class="sxs-lookup"><span data-stu-id="7fe9e-120">For detailed information about supported subscriptions, see the [Message policy and compliance service description](https://docs.microsoft.com/en-us/office365/servicedescriptions/exchange-online-service-description/message-policy-and-compliance).</span></span>

<span data-ttu-id="7fe9e-121">Configure os novos recursos de criptografia de mensagem do Office 365 se eles ainda não estiverem configurados para aproveitar os recursos avançados de criptografia de mensagens, que fornecem proteção adicional sobre as mensagens criptografadas compartilhadas externamente.</span><span class="sxs-lookup"><span data-stu-id="7fe9e-121">Set up the new Office 365 Message Encryption capabilities if they are not already set up to leverage Advanced Message Encryption capabilities which provide added protection on top of encrypted messages shared externally.</span></span> <span data-ttu-id="7fe9e-122">Se você não tiver a criptografia de mensagem do Office 365 configurada, confira [configurar novos recursos de criptografia de mensagens do office 365](set-up-new-message-encryption-capabilities.md).</span><span class="sxs-lookup"><span data-stu-id="7fe9e-122">If you do not have Office 365 Message Encryption set up, see [Set up new Office 365 Message Encryption capabilities](set-up-new-message-encryption-capabilities.md).</span></span>

<span data-ttu-id="7fe9e-123">[Definir uma data de expiração para email criptografado pela criptografia de mensagem avançada do Office 365](ome-advanced-expiration.md).</span><span class="sxs-lookup"><span data-stu-id="7fe9e-123">[Set an expiration date for email encrypted by Office 365 Advanced Message Encryption](ome-advanced-expiration.md).</span></span> <span data-ttu-id="7fe9e-124">Controlar emails confidenciais compartilhados fora da organização com políticas automáticas que aprimoram a proteção, expirando o acesso por meio de um portal da Web seguro para emails criptografados.</span><span class="sxs-lookup"><span data-stu-id="7fe9e-124">Control sensitive emails shared outside the organization with automatic policies that enhance protection by expiring access through a secure web portal to encrypted emails.</span></span>

<span data-ttu-id="7fe9e-125">[Revogar emails criptografados pela criptografia de mensagem avançada do Office 365](revoke-ome-encrypted-mail.md).</span><span class="sxs-lookup"><span data-stu-id="7fe9e-125">[Revoke email encrypted by Office 365 Advanced Message Encryption](revoke-ome-encrypted-mail.md).</span></span> <span data-ttu-id="7fe9e-126">Controle emails confidenciais compartilhados fora da organização e aprimore a proteção revogando o acesso por meio de um portal da Web seguro para emails criptografados.</span><span class="sxs-lookup"><span data-stu-id="7fe9e-126">Control sensitive emails shared outside the organization and enhance protection by revoking access through a secure web portal to encrypted emails.</span></span>  
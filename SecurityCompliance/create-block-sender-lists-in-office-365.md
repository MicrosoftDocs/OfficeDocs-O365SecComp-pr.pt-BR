---
title: Criar listas de remetentes bloqueados no Office 365
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 5/6/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150s
description: Bloquear as opções da lista de remetentes incluem remetentes bloqueados do Outlook, listas de bloqueios de remetente/domínio antispam, listas de bloqueio de IP e regras de transporte do Exchange (ETRs) também chamadas de fluxo de emails.
ms.openlocfilehash: dae5ffb7d4f2a8f8f3b675719e4f61f5c970dcaf
ms.sourcegitcommit: e834d4168f584f2efb22479aec108497eea267f6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2019
ms.locfileid: "34709119"
---
# <a name="create-block-sender-lists-in-office-365"></a><span data-ttu-id="8a08b-103">Criar listas de remetentes bloqueados no Office 365</span><span class="sxs-lookup"><span data-stu-id="8a08b-103">Create block sender lists in Office 365</span></span>

<span data-ttu-id="8a08b-104">Às vezes, é necessário bloquear emails indesejados de remetentes.</span><span class="sxs-lookup"><span data-stu-id="8a08b-104">Sometimes it’s necessary to block unwanted email from senders.</span></span> <span data-ttu-id="8a08b-105">Há vários métodos disponíveis para escolher.</span><span class="sxs-lookup"><span data-stu-id="8a08b-105">There are several methods available to choose from.</span></span> <span data-ttu-id="8a08b-106">Essas opções incluem remetentes bloqueados do Outlook, listas de bloqueios de remetente/domínio antispam, listas de bloqueio de IP e regras de transporte do Exchange (ETRs, que também são conhecidas como regras de fluxo de emails).</span><span class="sxs-lookup"><span data-stu-id="8a08b-106">These options include Outlook Blocked Senders, Anti-Spam Sender/Domain Block Lists, IP Block Lists, and Exchange Transport Rules (ETRs, which are also known as mail flow rules).</span></span>

> [!NOTE]
> <span data-ttu-id="8a08b-107">Enquanto as listas de bloqueio da organização podem ser usadas para tratar de falsos negativos (spam perdido), esses candidatos também devem ser enviados para a Microsoft para análise.</span><span class="sxs-lookup"><span data-stu-id="8a08b-107">While organization block lists can be used to address false negatives (missed spam), those candidates should also be submitted to Microsoft for analysis.</span></span> <span data-ttu-id="8a08b-108">O gerenciamento de falsos negativos usando listas de bloqueio aumenta significativamente a sobrecarga administrativa.</span><span class="sxs-lookup"><span data-stu-id="8a08b-108">Managing false negatives by using block lists significantly increases your administrative overhead.</span></span> <span data-ttu-id="8a08b-109">Se você usar uma lista de bloqueios para esse propósito, você também precisará manter o artigo para [enviar mensagens de spam, não spam e golpes de phishing para a Microsoft para análise](https://docs.microsoft.com/en-us/office365/SecurityCompliance/submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis), no Ready.</span><span class="sxs-lookup"><span data-stu-id="8a08b-109">If you will use a block list for this purpose, you will need to also keep the article for [submitting spam, non-spam, and phishing scam messages to Microsoft for analysis](https://docs.microsoft.com/en-us/office365/SecurityCompliance/submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis), at the ready.</span></span>

<span data-ttu-id="8a08b-110">O método apropriado para configurar listas de remetentes bloqueados varia dependendo do escopo do impacto.</span><span class="sxs-lookup"><span data-stu-id="8a08b-110">The proper method to configure blocked sender lists varies depending on the scope of the impact.</span></span> <span data-ttu-id="8a08b-111">Para o impacto de um único usuário, a solução certa pode ser usar remetentes bloqueados do Outlook, mas se vários usuários ou todos os usuários estiverem sendo afetados, uma das outras opções será mais apropriada.</span><span class="sxs-lookup"><span data-stu-id="8a08b-111">For single user impact, the right solution could be to use Outlook Blocked Senders, but if multiple users or all users are being impacted, one of the other options would be more appropriate.</span></span>

## <a name="options-from-least-to-broadest-scope"></a><span data-ttu-id="8a08b-112">Opções do menor para o maior escopo</span><span class="sxs-lookup"><span data-stu-id="8a08b-112">Options from least to broadest scope</span></span>

<span data-ttu-id="8a08b-113">Ao criar uma lista de bloqueios, é importante escolher o método adequado com base no escopo do impacto (quantas pessoas serão impactadas), para que ela coincida com a amplitude do método de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="8a08b-113">When creating a Block list it's important to pick the appropriate method based on the scope of the impact (how many people will be impacted), so that it matches the breadth of the blocking method.</span></span> <span data-ttu-id="8a08b-114">As opções listadas abaixo são classificadas por escopo e por amplitude.</span><span class="sxs-lookup"><span data-stu-id="8a08b-114">The options listed below are ranked by both scope and breadth.</span></span> <span data-ttu-id="8a08b-115">A lista vai de estreito a amplo, mas *Leia as especificações* de recomendações completas.</span><span class="sxs-lookup"><span data-stu-id="8a08b-115">The list goes from narrow to broad, but *read the specifics* for full recommendations.</span></span>

- <span data-ttu-id="8a08b-116">Remetentes bloqueados do Outlook</span><span class="sxs-lookup"><span data-stu-id="8a08b-116">Outlook Blocked Senders</span></span>
- <span data-ttu-id="8a08b-117">Política antispam: listas de bloqueios de remetente/domínio</span><span class="sxs-lookup"><span data-stu-id="8a08b-117">Anti-Spam policy: Sender/Domain Block lists</span></span>
- <span data-ttu-id="8a08b-118">Regras de transporte do Exchange (ETRs também chamadas de regras de fluxo de emails)</span><span class="sxs-lookup"><span data-stu-id="8a08b-118">Exchange Transport Rules (ETRs also called mail-flow rules)</span></span>
- <span data-ttu-id="8a08b-119">Política antispam: listas de bloqueios de IP</span><span class="sxs-lookup"><span data-stu-id="8a08b-119">Anti-Spam policy: IP Block Lists</span></span>

## <a name="use-outlook-blocked-senders"></a><span data-ttu-id="8a08b-120">Usar remetentes bloqueados do Outlook</span><span class="sxs-lookup"><span data-stu-id="8a08b-120">Use Outlook Blocked Senders</span></span>

<span data-ttu-id="8a08b-121">Quando somente um pequeno número de usuários é afetado, isso ocorre quando os remetentes bloqueados do Outlook devem ser usados, pois isso afetará apenas o envio de emails para eles.</span><span class="sxs-lookup"><span data-stu-id="8a08b-121">When only a small number of users are impacted, that's when Outlook Blocked Senders should be used, because this will only impact mail being sent to them.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8a08b-122">Se as mensagens indesejadas forem boletins informativos de uma fonte confiável e reconhecível, a cancelamento do email é outra opção para impedir que o usuário obtenha os emails no futuro.</span><span class="sxs-lookup"><span data-stu-id="8a08b-122">If the unwanted messages are newsletters from a reputable and recognizable source, unsubscribing from the email is another option to stop the user from getting the emails in the future.</span></span>

<span data-ttu-id="8a08b-123">As etapas para configurar isso são diferentes entre o [Outlook Web App](https://support.office.com/en-us/article/block-or-allow-junk-email-settings-48c9f6f7-2309-4f95-9a4d-de987e880e46) e o [cliente do Outlook](https://support.office.com/en-us/article/overview-of-the-junk-email-filter-5ae3ea8e-cf41-4fa0-b02a-3b96e21de089).</span><span class="sxs-lookup"><span data-stu-id="8a08b-123">The steps to set this up are different between [Outlook Web App](https://support.office.com/en-us/article/block-or-allow-junk-email-settings-48c9f6f7-2309-4f95-9a4d-de987e880e46) and the [Outlook client](https://support.office.com/en-us/article/overview-of-the-junk-email-filter-5ae3ea8e-cf41-4fa0-b02a-3b96e21de089).</span></span> <span data-ttu-id="8a08b-124">**Quando as mensagens são bloqueadas com êxito devido a remetentes bloqueados, você verá SFV: BLK no X-Forefront-antispam-Report** , que indica que a mensagem está sendo bloqueada.</span><span class="sxs-lookup"><span data-stu-id="8a08b-124">**When messages are successfully blocked due to Blocked Senders you will see SFV:BLK in the X-Forefront-Antispam-Report** which indicates that the message is being blocked.</span></span>

## <a name="use-anti-spam-policy-senderdomain-block-lists"></a><span data-ttu-id="8a08b-125">Usar listas de bloqueio de remetente/domínio de política antispam</span><span class="sxs-lookup"><span data-stu-id="8a08b-125">Use Anti-Spam Policy Sender/Domain Block lists</span></span>

<span data-ttu-id="8a08b-126">Quando vários usuários estão sendo afetados, o escopo é mais largo e você precisa usar uma política anti-spam de lista de remetente/domínio em toda a empresa.</span><span class="sxs-lookup"><span data-stu-id="8a08b-126">When multiple users are being impacted, the scope is wider, and you need to use a company-wide sender/domain block list Anti-Spam policy.</span></span> <span data-ttu-id="8a08b-127">As etapas detalhadas podem ser encontradas em [configurar seu documento de políticas de filtro de spam](https://docs.microsoft.com/en-us/office365/securitycompliance/configure-your-spam-filter-policies) .</span><span class="sxs-lookup"><span data-stu-id="8a08b-127">The detailed steps can be found in [Configure your spam filter policies](https://docs.microsoft.com/en-us/office365/securitycompliance/configure-your-spam-filter-policies) document.</span></span> <span data-ttu-id="8a08b-128">Qualquer mensagem bloqueada por esse método seguirá a ação de spam conforme configurada na política.</span><span class="sxs-lookup"><span data-stu-id="8a08b-128">Any messages blocked through this method will follow the spam action as configured in the policy.</span></span>

## <a name="use-exchange-transport-rules-etrs-to-block-specific-senders"></a><span data-ttu-id="8a08b-129">Usar regras de transporte do Exchange (ETRs) para bloquear remetentes específicos</span><span class="sxs-lookup"><span data-stu-id="8a08b-129">Use Exchange Transport Rules (ETRs) to Block specific senders</span></span>

<span data-ttu-id="8a08b-130">Se for necessário bloquear as mensagens enviadas para usuários específicos ou por toda a organização, o ETRs (também chamado de regras de fluxo de email) poderá ser usado.</span><span class="sxs-lookup"><span data-stu-id="8a08b-130">If it's necessary to block messages being sent to specific users or across the entire organization, ETRs (also called mail flow rules) can be used.</span></span> <span data-ttu-id="8a08b-131">ETRs são mais flexíveis porque podem disparar o endereço de email do remetente ou o domínio, bem como palavras-chave e outras propriedades da mensagem.</span><span class="sxs-lookup"><span data-stu-id="8a08b-131">ETRs are more flexible because they can trigger off the sender Email Address or Domain as well as key words and other properties  in the message.</span></span> <span data-ttu-id="8a08b-132">Essa flexibilidade permitirá a criação de blocos de conclusão parcial.</span><span class="sxs-lookup"><span data-stu-id="8a08b-132">This flexibility will let you create partial- to complete blocks.</span></span> <span data-ttu-id="8a08b-133">[Clique para obter as etapas para criar um ETR, também conhecido como regras de fluxo](https://docs.microsoft.com/en-us/office365/SecurityCompliance/use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages)de emails.</span><span class="sxs-lookup"><span data-stu-id="8a08b-133">[Please click for the steps to create an ETR, also known as a mail-flow rules](https://docs.microsoft.com/en-us/office365/SecurityCompliance/use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8a08b-134">É fácil criar regras que são muito agressivas, como resultado, é importante que o critério que está sendo usado seja o mais específico possível. \*\*</span><span class="sxs-lookup"><span data-stu-id="8a08b-134">It's easy to create rules that are *overly* aggressive, as a result it's important the criteria being used is as specific as possible.</span></span> <span data-ttu-id="8a08b-135">Além disso, certifique-se de habilitar a auditoria na regra que você criou e teste para garantir que tudo funcione conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="8a08b-135">Also, be sure that you enable auditing on the rule you create and do testing to ensure everything works as expected.</span></span>

## <a name="use-anti-spam-policy-ip-block-lists"></a><span data-ttu-id="8a08b-136">Usar listas de bloqueio de IP de política antispam</span><span class="sxs-lookup"><span data-stu-id="8a08b-136">Use Anti-Spam Policy IP Block lists</span></span>

<span data-ttu-id="8a08b-137">Quando não é possível usar uma das outras opções para bloquear um remetente, a lista de \*\* IPs bloqueados de política antispam pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="8a08b-137">When it’s not possible to use one of the other options to block a sender, *then* the Anti-Spam Policy IP Block List can be used.</span></span> <span data-ttu-id="8a08b-138">[As etapas detalhadas podem ser encontradas no artigo configurar a política de filtro de conexão](https://docs.microsoft.com/en-us/office365/securitycompliance/configure-the-connection-filter-policy).</span><span class="sxs-lookup"><span data-stu-id="8a08b-138">[Detailed steps can be found in the article Configure the connection filter policy](https://docs.microsoft.com/en-us/office365/securitycompliance/configure-the-connection-filter-policy).</span></span> <span data-ttu-id="8a08b-139">É importante manter a lista de IPs bloqueados para um *mínimo* e usar intervalos de endereços IP aqui *não* é recomendável.</span><span class="sxs-lookup"><span data-stu-id="8a08b-139">It's important to keep the list of blocked IPs to a *minimum* and using IP address ranges here is *not* recommended.</span></span>

<span data-ttu-id="8a08b-140">Você deve *especialmente* evitar a adição de intervalos de endereços IP que pertencem a serviços de consumidor ou infraestruturas compartilhadas, e também garantir que você revise a lista de endereços IP permitidos como parte da manutenção normal.</span><span class="sxs-lookup"><span data-stu-id="8a08b-140">You should *especially* avoid adding IP address ranges that belong to consumer services or shared infrastructures, and also ensure that you review the list of allowed IP addresses as part of regular maintenance.</span></span> <span data-ttu-id="8a08b-141">**Como o permite que as entradas possam abrir rotas para ataques, você deve gerenciar de forma mais detalhada essa lista e remover regularmente as entradas que não são mais necessárias.**</span><span class="sxs-lookup"><span data-stu-id="8a08b-141">**Because allows-entries can open up routes for attack, you must closely manage this list and regularly remove the allows-entries that are no longer needed.**</span></span> <span data-ttu-id="8a08b-142">Além disso, se você permitir, em uma lista de remetentes seguros, leia e entenda os riscos e precauções em *[criar listas de remetentes seguros no Office 365](create-safe-sender-lists-in-office-365.md)*.</span><span class="sxs-lookup"><span data-stu-id="8a08b-142">Also, if you will make allows in a Safe-Sender list be sure to read and understand the risks and precautions in *[Create Safe-Sender lists in Office 365](create-safe-sender-lists-in-office-365.md)*.</span></span>
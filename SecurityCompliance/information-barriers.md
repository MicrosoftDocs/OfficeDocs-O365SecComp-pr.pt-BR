---
title: Visão geral das barreiras de informações
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 05/31/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: Use as barreiras de informação para garantir a conformidade de comunicação usando o Microsoft Teams em sua organização.
ms.openlocfilehash: e52a62ca0b80aed577be1978b81c8a01ac2371b9
ms.sourcegitcommit: 4fedeb06a6e7796096fc6279cfb091c7b89d484d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/31/2019
ms.locfileid: "34668268"
---
# <a name="information-barriers-preview"></a><span data-ttu-id="b4da7-103">Barreiras de informação (visualização)</span><span class="sxs-lookup"><span data-stu-id="b4da7-103">Information barriers (Preview)</span></span>

<span data-ttu-id="b4da7-104">Os serviços de nuvem da Microsoft incluem recursos avançados de comunicação e colaboração.</span><span class="sxs-lookup"><span data-stu-id="b4da7-104">Microsoft cloud services include powerful communication and collaboration capabilities.</span></span> <span data-ttu-id="b4da7-105">Mas suponha que você deseja restringir as comunicações entre dois grupos para evitar um conflito de interesse de ocorrer em sua organização.</span><span class="sxs-lookup"><span data-stu-id="b4da7-105">But suppose that you want to restrict communications between two groups to avoid a conflict of interest from occurring in your organization.</span></span> <span data-ttu-id="b4da7-106">Ou, talvez você queira restringir as comunicações entre determinadas pessoas dentro da sua organização para proteger informações internas.</span><span class="sxs-lookup"><span data-stu-id="b4da7-106">Or, perhaps you want to restrict communications between certain people inside your organization in order to safeguard internal information.</span></span> <span data-ttu-id="b4da7-107">A Microsoft 365 permite a comunicação e a colaboração entre grupos e organizações, portanto, há uma maneira de restringir as comunicações entre grupos específicos de usuários quando necessário?</span><span class="sxs-lookup"><span data-stu-id="b4da7-107">Microsoft 365 enables communication and collaboration across groups and organizations, so is there a way to restrict communications among specific groups of users when necessary?</span></span> <span data-ttu-id="b4da7-108">Com as barreiras de informação, você pode!</span><span class="sxs-lookup"><span data-stu-id="b4da7-108">With information barriers, you can!</span></span> 

<span data-ttu-id="b4da7-109">As barreiras de informação estão em versão prévia agora, começando com o Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="b4da7-109">Information barriers are in preview now, beginning with Microsoft Teams.</span></span> <span data-ttu-id="b4da7-110">Quando esses recursos estão disponíveis para sua organização, um administrador de conformidade ou barreiras de informações pode definir políticas para permitir ou impedir a comunicação entre grupos de usuários no Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="b4da7-110">When these features are available for your organization, a compliance administrator or information barriers administrator can define policies to allow or prevent communications between groups of users in Microsoft Teams.</span></span> <span data-ttu-id="b4da7-111">As políticas de barreira de informações podem ser usadas para situações como estas:</span><span class="sxs-lookup"><span data-stu-id="b4da7-111">Information barrier policies can be used for situations like these:</span></span>

- <span data-ttu-id="b4da7-112">Um dia dos traders não pode ligar para alguém na equipe de marketing</span><span class="sxs-lookup"><span data-stu-id="b4da7-112">A day trader cannot call someone on the marketing team</span></span>
- <span data-ttu-id="b4da7-113">O pessoal financeiro que trabalha em informações confidenciais da empresa não pode receber chamadas de determinados grupos dentro de sua organização</span><span class="sxs-lookup"><span data-stu-id="b4da7-113">Finance personnel working on confidential company information cannot receive calls from certain groups within their organization</span></span>
- <span data-ttu-id="b4da7-114">Uma equipe interna com material secreto comercial não pode ligar ou bater papo com pessoas de determinados grupos de sua organização</span><span class="sxs-lookup"><span data-stu-id="b4da7-114">An internal team with trade secret material cannot call or chat online with people in certain groups within their organization</span></span>
- <span data-ttu-id="b4da7-115">Uma equipe de pesquisa pode apenas ligar ou conversar online com uma equipe de desenvolvimento de produtos</span><span class="sxs-lookup"><span data-stu-id="b4da7-115">A research team can only call or chat online with a product development team</span></span>

<span data-ttu-id="b4da7-116">Para todos esses cenários de exemplo (e mais), as políticas de barreira de informações podem ser definidas para impedir ou permitir comunicações no Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="b4da7-116">For all of these example scenarios (and more), information barrier policies can be defined to prevent or allow communications in Microsoft Teams.</span></span> <span data-ttu-id="b4da7-117">Essas políticas podem impedir que as pessoas chamem ou chat com as que elas não deveriam ou permitir que as pessoas se comuniquem somente com grupos específicos no Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="b4da7-117">Such policies can prevent people from calling or chatting with those they shouldn't, or enable people to communicate only with specific groups in Microsoft Teams.</span></span> <span data-ttu-id="b4da7-118">Com as políticas de barreira de informações em vigor, sempre que os usuários que estão cobertos por essas políticas tentarem se comunicar com outras pessoas no Microsoft Teams, as verificações são realizadas para impedir (ou permitir) a comunicação (conforme definido pelas políticas de barreira de informações).</span><span class="sxs-lookup"><span data-stu-id="b4da7-118">With information barrier policies in effect, whenever users who are covered by those policies attempt to communicate with others in Microsoft Teams, checks are done to prevent (or allow) communication (as defined by information barrier policies).</span></span> 

> [!NOTE]
> <span data-ttu-id="b4da7-119">As barreiras de informação não serão aplicadas às comunicações por email ou ao compartilhamento de arquivos por meio do SharePoint Online ou do OneDrive.</span><span class="sxs-lookup"><span data-stu-id="b4da7-119">Information barriers will not apply to email communications or to file sharing through SharePoint Online or OneDrive.</span></span>

<span data-ttu-id="b4da7-120">As políticas de barreira de informações se aplicam aos seguintes tipos de atividades de comunicação:</span><span class="sxs-lookup"><span data-stu-id="b4da7-120">Information barrier policies apply to the following kinds of communication activities:</span></span>

- <span data-ttu-id="b4da7-121">Pesquisando usuário</span><span class="sxs-lookup"><span data-stu-id="b4da7-121">Searching for user</span></span>
- <span data-ttu-id="b4da7-122">Adicionar um membro a uma equipe</span><span class="sxs-lookup"><span data-stu-id="b4da7-122">Adding a member to a team</span></span>
- <span data-ttu-id="b4da7-123">Iniciar uma sessão de chat com alguém</span><span class="sxs-lookup"><span data-stu-id="b4da7-123">Starting a chat session with someone</span></span>
- <span data-ttu-id="b4da7-124">Iniciar um chat de grupo</span><span class="sxs-lookup"><span data-stu-id="b4da7-124">Starting a group chat</span></span> 
- <span data-ttu-id="b4da7-125">Convidar alguém para participar de uma reunião</span><span class="sxs-lookup"><span data-stu-id="b4da7-125">Inviting someone to join a meeting</span></span>
- <span data-ttu-id="b4da7-126">Compartilhar uma tela</span><span class="sxs-lookup"><span data-stu-id="b4da7-126">Sharing a screen</span></span> 
- <span data-ttu-id="b4da7-127">Fazendo uma chamada</span><span class="sxs-lookup"><span data-stu-id="b4da7-127">Placing a call</span></span>

<span data-ttu-id="b4da7-128">Se as pessoas envolvidas estiverem incluídas em uma política de barreira de informações que impede a atividade, elas não poderão continuar.</span><span class="sxs-lookup"><span data-stu-id="b4da7-128">If the people involved are included in an information barrier policy that prevents the activity, they will not be able to proceed.</span></span> <span data-ttu-id="b4da7-129">Para saber mais sobre a experiência do usuário com barreiras de informações, confira [barreiras de informações no Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams).</span><span class="sxs-lookup"><span data-stu-id="b4da7-129">To learn more about the user experience with information barriers, see [information barriers in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams).</span></span>

<span data-ttu-id="b4da7-130">Atualmente, as políticas de barreira de informações são definidas e gerenciadas no Office 365 usando cmdlets do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b4da7-130">Currently, information barrier policies are defined and managed in Office 365 by using PowerShell cmdlets.</span></span> <span data-ttu-id="b4da7-131">Isso geralmente é feito por um administrador de conformidade ou um administrador global e requer familiaridade com cmdlets (e parâmetros) do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b4da7-131">This is typically done by a compliance administrator or a global administrator, and requires familiarity with PowerShell cmdlets (and parameters).</span></span> <span data-ttu-id="b4da7-132">Para saber mais, confira [PowerShell (para definir as barreiras de informação)](information-barriers-policies.md#powershell).</span><span class="sxs-lookup"><span data-stu-id="b4da7-132">To learn more, see [PowerShell (for defining information barriers)](information-barriers-policies.md#powershell).</span></span>

## <a name="required-licenses-and-permissions"></a><span data-ttu-id="b4da7-133">Licenças e permissões necessárias</span><span class="sxs-lookup"><span data-stu-id="b4da7-133">Required licenses and permissions</span></span>

<span data-ttu-id="b4da7-134">**No momento, o recurso de barreira de informações está em visualização privada**.</span><span class="sxs-lookup"><span data-stu-id="b4da7-134">**Currently, the information barrier feature is in private preview**.</span></span> <span data-ttu-id="b4da7-135">Quando esses recursos estão disponíveis em geral, eles serão incluídos em assinaturas, como:</span><span class="sxs-lookup"><span data-stu-id="b4da7-135">When these features are generally available, they'll be included in subscriptions, such as:</span></span>

- <span data-ttu-id="b4da7-136">Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="b4da7-136">Microsoft 365 E5</span></span>
- <span data-ttu-id="b4da7-137">Office 365 e5</span><span class="sxs-lookup"><span data-stu-id="b4da7-137">Office 365 E5</span></span>
- <span data-ttu-id="b4da7-138">Conformidade Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="b4da7-138">Office 365 Advanced Compliance</span></span>
- <span data-ttu-id="b4da7-139">Conformidade e proteção de informações do Microsoft 365 e5</span><span class="sxs-lookup"><span data-stu-id="b4da7-139">Microsoft 365 E5 Information Protection and Compliance</span></span>

<span data-ttu-id="b4da7-140">Para obter mais detalhes, consulte [soluções de conformidade](https://products.office.com/business/security-and-compliance/compliance-solutions).</span><span class="sxs-lookup"><span data-stu-id="b4da7-140">For more details, see [Compliance Solutions](https://products.office.com/business/security-and-compliance/compliance-solutions).</span></span>

<span data-ttu-id="b4da7-141">Para [definir ou editar as políticas de barreira de informações](information-barriers-policies.md), você deve ter uma das seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="b4da7-141">To [define or edit information barrier policies](information-barriers-policies.md), you must be assigned one of the following roles:</span></span>

- <span data-ttu-id="b4da7-142">Administrador global do Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="b4da7-142">Microsoft 365 global administrator</span></span>
- <span data-ttu-id="b4da7-143">Administrador global do Office 365</span><span class="sxs-lookup"><span data-stu-id="b4da7-143">Office 365 global administrator</span></span>
- <span data-ttu-id="b4da7-144">Administrador de conformidade</span><span class="sxs-lookup"><span data-stu-id="b4da7-144">Compliance administrator</span></span>
- <span data-ttu-id="b4da7-145">Administrador de barreiras de informações</span><span class="sxs-lookup"><span data-stu-id="b4da7-145">Information barriers administrator</span></span>

<span data-ttu-id="b4da7-146">Você deve estar familiarizado com os cmdlets do PowerShell para definir, validar ou editar as políticas de barreira de informações.</span><span class="sxs-lookup"><span data-stu-id="b4da7-146">You must be familiar with PowerShell cmdlets in order to define, validate, or edit information barrier policies.</span></span> <span data-ttu-id="b4da7-147">Embora forneçamos vários exemplos de cmdlets do PowerShell nas [informações de instruções](information-barriers-policies.md), você precisará saber detalhes adicionais, como parâmetros, para sua organização.</span><span class="sxs-lookup"><span data-stu-id="b4da7-147">Although we provide several examples of PowerShell cmdlets in the [how-to information](information-barriers-policies.md), you'll need to know additional details, such as parameters, for your organization.</span></span>

## <a name="next-steps"></a><span data-ttu-id="b4da7-148">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="b4da7-148">Next steps</span></span>

- [<span data-ttu-id="b4da7-149">Saiba mais sobre as barreiras de informação no Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="b4da7-149">Learn more about information barriers in Microsoft Teams</span></span>](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams)
- [<span data-ttu-id="b4da7-150">Ver os atributos que podem ser usados para políticas de barreira de informações</span><span class="sxs-lookup"><span data-stu-id="b4da7-150">See the attributes that can be used for information barrier policies</span></span>](information-barriers-attributes.md)
- [<span data-ttu-id="b4da7-151">Definir políticas para barreiras de informações</span><span class="sxs-lookup"><span data-stu-id="b4da7-151">Define policies for information barriers</span></span>](information-barriers-policies.md) 


---
title: Visão geral das barreiras de informações
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 06/13/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: Use as barreiras de informação para garantir a conformidade de comunicação usando o Microsoft Teams em sua organização.
ms.openlocfilehash: a2c202d08f1de60f92f13b2ac4c2b9d3c7f900e8
ms.sourcegitcommit: eeb51470d8996e93fac28d7f12c6117e2aeb0cf0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/14/2019
ms.locfileid: "34935933"
---
# <a name="information-barriers-preview"></a><span data-ttu-id="bc09a-103">Barreiras de informação (visualização)</span><span class="sxs-lookup"><span data-stu-id="bc09a-103">Information barriers (Preview)</span></span>

## <a name="overview"></a><span data-ttu-id="bc09a-104">Visão geral</span><span class="sxs-lookup"><span data-stu-id="bc09a-104">Overview</span></span>

<span data-ttu-id="bc09a-105">Os serviços de nuvem da Microsoft incluem recursos avançados de comunicação e colaboração.</span><span class="sxs-lookup"><span data-stu-id="bc09a-105">Microsoft cloud services include powerful communication and collaboration capabilities.</span></span> <span data-ttu-id="bc09a-106">Mas suponha que você deseja restringir as comunicações entre dois grupos para evitar um conflito de interesse de ocorrer em sua organização.</span><span class="sxs-lookup"><span data-stu-id="bc09a-106">But suppose that you want to restrict communications between two groups to avoid a conflict of interest from occurring in your organization.</span></span> <span data-ttu-id="bc09a-107">Ou, talvez você queira restringir as comunicações entre determinadas pessoas dentro da sua organização para proteger informações internas.</span><span class="sxs-lookup"><span data-stu-id="bc09a-107">Or, perhaps you want to restrict communications between certain people inside your organization in order to safeguard internal information.</span></span> <span data-ttu-id="bc09a-108">A Microsoft 365 permite a comunicação e a colaboração entre grupos e organizações, portanto, há uma maneira de restringir as comunicações entre grupos específicos de usuários quando necessário?</span><span class="sxs-lookup"><span data-stu-id="bc09a-108">Microsoft 365 enables communication and collaboration across groups and organizations, so is there a way to restrict communications among specific groups of users when necessary?</span></span> <span data-ttu-id="bc09a-109">Com as barreiras de informação, você pode!</span><span class="sxs-lookup"><span data-stu-id="bc09a-109">With information barriers, you can!</span></span> 

<span data-ttu-id="bc09a-110">As barreiras de informação estão em versão prévia agora, começando com o Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="bc09a-110">Information barriers are in preview now, beginning with Microsoft Teams.</span></span> <span data-ttu-id="bc09a-111">Quando esses recursos estão disponíveis para sua organização, um administrador de conformidade ou barreiras de informações pode definir políticas para permitir ou impedir a comunicação entre grupos de usuários no Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="bc09a-111">When these features are available for your organization, a compliance administrator or information barriers administrator can define policies to allow or prevent communications between groups of users in Microsoft Teams.</span></span> <span data-ttu-id="bc09a-112">As políticas de barreira de informações podem ser usadas para situações como estas:</span><span class="sxs-lookup"><span data-stu-id="bc09a-112">Information barrier policies can be used for situations like these:</span></span>

- <span data-ttu-id="bc09a-113">Um dia dos traders não pode ligar para alguém na equipe de marketing</span><span class="sxs-lookup"><span data-stu-id="bc09a-113">A day trader cannot call someone on the marketing team</span></span>
- <span data-ttu-id="bc09a-114">O pessoal financeiro que trabalha em informações confidenciais da empresa não pode receber chamadas de determinados grupos dentro de sua organização</span><span class="sxs-lookup"><span data-stu-id="bc09a-114">Finance personnel working on confidential company information cannot receive calls from certain groups within their organization</span></span>
- <span data-ttu-id="bc09a-115">Uma equipe interna com material secreto comercial não pode ligar ou bater papo com pessoas de determinados grupos de sua organização</span><span class="sxs-lookup"><span data-stu-id="bc09a-115">An internal team with trade secret material cannot call or chat online with people in certain groups within their organization</span></span>
- <span data-ttu-id="bc09a-116">Uma equipe de pesquisa pode apenas ligar ou conversar online com uma equipe de desenvolvimento de produtos</span><span class="sxs-lookup"><span data-stu-id="bc09a-116">A research team can only call or chat online with a product development team</span></span>

<span data-ttu-id="bc09a-117">Para todos esses cenários de exemplo (e mais), as políticas de barreira de informações podem ser definidas para impedir ou permitir comunicações no Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="bc09a-117">For all of these example scenarios (and more), information barrier policies can be defined to prevent or allow communications in Microsoft Teams.</span></span> <span data-ttu-id="bc09a-118">Essas políticas podem impedir que as pessoas chamem ou chat com as que elas não deveriam ou permitir que as pessoas se comuniquem somente com grupos específicos no Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="bc09a-118">Such policies can prevent people from calling or chatting with those they shouldn't, or enable people to communicate only with specific groups in Microsoft Teams.</span></span> <span data-ttu-id="bc09a-119">Com as políticas de barreira de informações em vigor, sempre que os usuários que estão cobertos por essas políticas tentarem se comunicar com outras pessoas no Microsoft Teams, as verificações são realizadas para impedir (ou permitir) a comunicação (conforme definido pelas políticas de barreira de informações).</span><span class="sxs-lookup"><span data-stu-id="bc09a-119">With information barrier policies in effect, whenever users who are covered by those policies attempt to communicate with others in Microsoft Teams, checks are done to prevent (or allow) communication (as defined by information barrier policies).</span></span> <span data-ttu-id="bc09a-120">Para saber mais sobre a experiência do usuário com barreiras de informações, confira [barreiras de informações no Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams).</span><span class="sxs-lookup"><span data-stu-id="bc09a-120">To learn more about the user experience with information barriers, see [information barriers in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams).</span></span>

> [!NOTE]
> <span data-ttu-id="bc09a-121">As barreiras de informação não serão aplicadas às comunicações por email ou ao compartilhamento de arquivos por meio do SharePoint Online ou do OneDrive.</span><span class="sxs-lookup"><span data-stu-id="bc09a-121">Information barriers will not apply to email communications or to file sharing through SharePoint Online or OneDrive.</span></span>

## <a name="required-licenses-and-permissions"></a><span data-ttu-id="bc09a-122">Licenças e permissões necessárias</span><span class="sxs-lookup"><span data-stu-id="bc09a-122">Required licenses and permissions</span></span>

<span data-ttu-id="bc09a-123">**No momento, o recurso de barreira de informações está em visualização privada**.</span><span class="sxs-lookup"><span data-stu-id="bc09a-123">**Currently, the information barrier feature is in private preview**.</span></span> <span data-ttu-id="bc09a-124">Quando esses recursos estão disponíveis em geral, eles serão incluídos em assinaturas, como:</span><span class="sxs-lookup"><span data-stu-id="bc09a-124">When these features are generally available, they'll be included in subscriptions, such as:</span></span>

- <span data-ttu-id="bc09a-125">Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="bc09a-125">Microsoft 365 E5</span></span>
- <span data-ttu-id="bc09a-126">Office 365 e5</span><span class="sxs-lookup"><span data-stu-id="bc09a-126">Office 365 E5</span></span>
- <span data-ttu-id="bc09a-127">Conformidade Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="bc09a-127">Office 365 Advanced Compliance</span></span>
- <span data-ttu-id="bc09a-128">Conformidade e proteção de informações do Microsoft 365 e5</span><span class="sxs-lookup"><span data-stu-id="bc09a-128">Microsoft 365 E5 Information Protection and Compliance</span></span>

<span data-ttu-id="bc09a-129">Para obter mais detalhes, consulte [soluções de conformidade](https://products.office.com/business/security-and-compliance/compliance-solutions).</span><span class="sxs-lookup"><span data-stu-id="bc09a-129">For more details, see [Compliance Solutions](https://products.office.com/business/security-and-compliance/compliance-solutions).</span></span>

<span data-ttu-id="bc09a-130">Para [definir ou editar as políticas de barreira de informações](information-barriers-policies.md), você deve ter uma das seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="bc09a-130">To [define or edit information barrier policies](information-barriers-policies.md), you must be assigned one of the following roles:</span></span>

- <span data-ttu-id="bc09a-131">Administrador global do Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="bc09a-131">Microsoft 365 global administrator</span></span>
- <span data-ttu-id="bc09a-132">Administrador global do Office 365</span><span class="sxs-lookup"><span data-stu-id="bc09a-132">Office 365 global administrator</span></span>
- <span data-ttu-id="bc09a-133">Administrador de conformidade</span><span class="sxs-lookup"><span data-stu-id="bc09a-133">Compliance administrator</span></span>
- <span data-ttu-id="bc09a-134">Administrador de barreiras de informações</span><span class="sxs-lookup"><span data-stu-id="bc09a-134">Information barriers administrator</span></span>

<span data-ttu-id="bc09a-135">Você deve estar familiarizado com os cmdlets do PowerShell para definir, validar ou editar as políticas de barreira de informações.</span><span class="sxs-lookup"><span data-stu-id="bc09a-135">You must be familiar with PowerShell cmdlets in order to define, validate, or edit information barrier policies.</span></span> <span data-ttu-id="bc09a-136">Embora forneçamos vários exemplos de cmdlets do PowerShell nas [informações de instruções](information-barriers-policies.md), você precisará saber detalhes adicionais, como parâmetros, para sua organização.</span><span class="sxs-lookup"><span data-stu-id="bc09a-136">Although we provide several examples of PowerShell cmdlets in the [how-to information](information-barriers-policies.md), you'll need to know additional details, such as parameters, for your organization.</span></span>

## <a name="next-steps"></a><span data-ttu-id="bc09a-137">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="bc09a-137">Next steps</span></span>

- [<span data-ttu-id="bc09a-138">Saiba mais sobre as barreiras de informação no Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="bc09a-138">Learn more about information barriers in Microsoft Teams</span></span>](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams)
- [<span data-ttu-id="bc09a-139">Ver os atributos que podem ser usados para políticas de barreira de informações</span><span class="sxs-lookup"><span data-stu-id="bc09a-139">See the attributes that can be used for information barrier policies</span></span>](information-barriers-attributes.md)
- [<span data-ttu-id="bc09a-140">Definir políticas para barreiras de informações</span><span class="sxs-lookup"><span data-stu-id="bc09a-140">Define policies for information barriers</span></span>](information-barriers-policies.md) 


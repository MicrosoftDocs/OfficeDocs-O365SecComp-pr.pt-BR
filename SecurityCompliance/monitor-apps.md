---
title: Monitorar e relatar o status do aplicativo no Microsoft 365 Security
description: Descreve como você pode obter mais informações sobre o uso do aplicativo na nuvem em sua organização
keywords: segurança, malware, Microsoft 365, M365, central de segurança, monitor, relatório, aplicativos
ms.prod: w10
ms.mktglfcycl: deploy
ms.localizationpriority: medium
ms.author: ellevin
author: levinec
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
search.appverid: met150
ms.openlocfilehash: 33a10996ceaf3023d5aee58aaabf3fef54372c30
ms.sourcegitcommit: 8213c353954b92f5c3979bee4aa049da0fd28a18
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/03/2019
ms.locfileid: "31043292"
---
# <a name="monitor-and-report-app-status-in-microsoft-365-security"></a><span data-ttu-id="9d06f-104">Monitorar e relatar o status do aplicativo no Microsoft 365 Security</span><span class="sxs-lookup"><span data-stu-id="9d06f-104">Monitor and report app status in Microsoft 365 security</span></span>


<span data-ttu-id="9d06f-105">Esses relatórios fornecem mais informações sobre como os aplicativos de nuvem estão sendo usados na sua organização, incluindo os tipos de aplicativos, seu nível de risco e alertas.</span><span class="sxs-lookup"><span data-stu-id="9d06f-105">These reports provide more insight into how cloud apps are being used in your organization, including what kinds of apps, their level of risk, and alerts.</span></span>

## <a name="monitor-email-accounts-at-risk"></a><span data-ttu-id="9d06f-106">Monitorar contas de email em risco</span><span class="sxs-lookup"><span data-stu-id="9d06f-106">Monitor email accounts at risk</span></span>

<span data-ttu-id="9d06f-107">A **proteção de email** mostra as contas de email em risco.</span><span class="sxs-lookup"><span data-stu-id="9d06f-107">**Email protection** shows email accounts at risk.</span></span> <span data-ttu-id="9d06f-108">Você pode clicar em uma conta para investigar mais a central de segurança do Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="9d06f-108">You can click an account to investigate further in Windows Defender Security Center.</span></span>

![Cartão de proteção de email](./media/security-docs/email-protection.png)

## <a name="monitor-app-permissions-granted-by-users"></a><span data-ttu-id="9d06f-110">Monitorar permissões de aplicativo concedidas por usuários</span><span class="sxs-lookup"><span data-stu-id="9d06f-110">Monitor app permissions granted by users</span></span>

<span data-ttu-id="9d06f-111">**Cloud app Security-aplicativos OAuth** lista aplicativos descobertos pela Cloud app Security que receberam permissões pelos usuários.</span><span class="sxs-lookup"><span data-stu-id="9d06f-111">**Cloud App Security - OAuth apps** lists apps discovered by Cloud App Security that have been granted permissions by users.</span></span> <span data-ttu-id="9d06f-112">O catálogo de riscos do Cloud app Security inclui mais de 16.000 aplicativos que são avaliados usando mais de 70 fatores de risco.</span><span class="sxs-lookup"><span data-stu-id="9d06f-112">Cloud App Security's risk catalog includes over 16,000 apps that are assessed using over 70 risk factors.</span></span>

<span data-ttu-id="9d06f-113">Os fatores de risco são iniciados a partir de informações gerais, como o editor de aplicativos, medidas de segurança e controles, como se o aplicativo dá suporte para criptografia em repouso ou fornece um log de auditoria da atividade do usuário.</span><span class="sxs-lookup"><span data-stu-id="9d06f-113">The risk factors start from general information, such as the app publisher, to security measures and controls, such as whether the app supports for encryption at rest or provides an audit log of user activity.</span></span>

![Cartão de aplicativos OAuth do Cloud app Security](./media/security-docs/cloud-app-security-oauth-apps.png)

## <a name="monitor-cloud-app-user-accounts"></a><span data-ttu-id="9d06f-115">Monitorar contas de usuário do aplicativo na nuvem</span><span class="sxs-lookup"><span data-stu-id="9d06f-115">Monitor cloud app user accounts</span></span>

<span data-ttu-id="9d06f-116">**Contas de aplicativo em nuvem para análise** lista contas que podem exigir atenção.</span><span class="sxs-lookup"><span data-stu-id="9d06f-116">**Cloud app accounts for review** lists accounts that may require attention.</span></span>

![Contas de aplicativo de nuvem para o cartão de revisão](./media/security-docs/cloud-app-accounts-for-review.png)

## <a name="understand-which-cloud-apps-are-used"></a><span data-ttu-id="9d06f-118">Entender quais aplicativos de nuvem são usados</span><span class="sxs-lookup"><span data-stu-id="9d06f-118">Understand which cloud apps are used</span></span>

<span data-ttu-id="9d06f-119">Os **aplicativos de nuvem descobertos (categorias)** mostram quais tipos de aplicativos estão sendo usados na sua organização e links para o painel de descoberta de nuvem no Cloud app Security.</span><span class="sxs-lookup"><span data-stu-id="9d06f-119">**Discovered cloud apps (categories)** show what kinds of apps are being used in your organization and links to the Cloud Discovery dashboard in Cloud App Security.</span></span> <span data-ttu-id="9d06f-120">Para obter mais informações, consulte [QuickStart: work with untected apps](https://docs.microsoft.com/cloud-app-security/discovered-apps).</span><span class="sxs-lookup"><span data-stu-id="9d06f-120">For more information, see [Quickstart: Work with discovered apps](https://docs.microsoft.com/cloud-app-security/discovered-apps).</span></span>  

![Cartão de categorias de aplicativos de nuvem descoberto](./media/security-docs/discovered-cloud-apps-categories.png)

## <a name="monitor-where-users-access-cloud-apps"></a><span data-ttu-id="9d06f-122">Monitorar onde os usuários acessam os aplicativos de nuvem</span><span class="sxs-lookup"><span data-stu-id="9d06f-122">Monitor where users access cloud apps</span></span>

<span data-ttu-id="9d06f-123">**Locais de atividade do aplicativo na nuvem** mostram onde os usuários estão acessando aplicativos em nuvem.</span><span class="sxs-lookup"><span data-stu-id="9d06f-123">**Cloud app activity locations** show where users are accessing cloud apps.</span></span>

![Cartão de locais de atividade do Cloud app](./media/security-docs/cloud-app-activity-locations.png)

## <a name="monitor-health-for-infrastructure-workloads"></a><span data-ttu-id="9d06f-125">Monitorar a integridade das cargas de trabalho da infraestrutura</span><span class="sxs-lookup"><span data-stu-id="9d06f-125">Monitor health for infrastructure workloads</span></span>

<span data-ttu-id="9d06f-126">**Infrastructure Health** mostra alertas de status de integridade para cargas de trabalho de infraestrutura na central de segurança do Azure.</span><span class="sxs-lookup"><span data-stu-id="9d06f-126">**Infrastructure health** shows health status alerts for infrastructure workloads in Azure Security Center.</span></span>

<span data-ttu-id="9d06f-127">A central de segurança do Azure oferece gerenciamento de segurança unificado e proteção avançada contra ameaças em cargas de trabalho locais e em nuvem.</span><span class="sxs-lookup"><span data-stu-id="9d06f-127">Azure Security Center provides unified security management and advanced threat protection across on-premises and cloud workloads.</span></span> <span data-ttu-id="9d06f-128">Você pode coletar, Pesquisar e analisar dados de segurança de várias fontes, incluindo firewalls e outras soluções de parceiros.</span><span class="sxs-lookup"><span data-stu-id="9d06f-128">You can collect, search, and analyze security data from a variety of sources, including firewalls and other partner solutions.</span></span>

<span data-ttu-id="9d06f-129">Para obter mais informações, consulte a [documentação da central de segurança do Azure](https://docs.microsoft.com/azure/security-center/).</span><span class="sxs-lookup"><span data-stu-id="9d06f-129">For more information, see [Azure Security Center Documentation](https://docs.microsoft.com/azure/security-center/).</span></span>

![Cartão de integridade de infraestrutura](./media/security-docs/infrastructure-health.png)

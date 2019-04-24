---
title: Analisar descobertas de aplicativos do Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: aac65513-e75e-4c82-a668-9a6604dd9f9d
description: ReVisando os relatórios de descoberta de aplicativos no Office 365 Cloud app Security pode ajudá-lo a saber mais sobre como as pessoas em sua organização usam aplicativos de nuvem. Depois de criar relatórios de descoberta de aplicativos usando arquivos de log de seus firewalls e proxies, revise os resultados no painel de descoberta de aplicativos.
ms.openlocfilehash: f50ad372450b2a1404829eeb6f6964c1d954dccd
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32264947"
---
# <a name="review-app-discovery-findings-in-office-365-cloud-app-security"></a><span data-ttu-id="0bd60-104">Analisar descobertas de aplicativos do Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="0bd60-104">Review app discovery findings in Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="0bd60-105">Avaliação \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="0bd60-105">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="0bd60-106">Planejamento \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="0bd60-106">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="0bd60-107">Implantação \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="0bd60-107">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="0bd60-108">Utilização \* \* \*</span><span class="sxs-lookup"><span data-stu-id="0bd60-108">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="0bd60-109">Iniciar avaliação</span><span class="sxs-lookup"><span data-stu-id="0bd60-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="0bd60-110">Iniciar planejamento</span><span class="sxs-lookup"><span data-stu-id="0bd60-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="0bd60-111">Iniciar implantação</span><span class="sxs-lookup"><span data-stu-id="0bd60-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="0bd60-112">Você está aqui!</span><span class="sxs-lookup"><span data-stu-id="0bd60-112">You are here!</span></span>  <br/> [<span data-ttu-id="0bd60-113">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="0bd60-113">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="0bd60-114">O painel de descoberta de nuvem funciona com os logs de tráfego da Web da sua organização para fornecer informações detalhadas sobre o uso do aplicativo na nuvem.</span><span class="sxs-lookup"><span data-stu-id="0bd60-114">The Cloud Discovery dashboard works with your organization's web traffic logs to provide detailed information about cloud app usage.</span></span> <span data-ttu-id="0bd60-115">Se você é um administrador global, administrador de segurança ou leitor de segurança e sua organização [criou relatórios de descoberta de aplicativos no Office 365 Cloud app Security](create-app-discovery-reports-in-ocas.md), você pode usar o painel de descoberta de nuvem para obter informações sobre como as pessoas em seu a organização está usando o Office 365 e outros aplicativos em nuvem.</span><span class="sxs-lookup"><span data-stu-id="0bd60-115">If you're a global administrator, security administrator, or security reader, and your organization has [created app discovery reports in Office 365 Cloud App Security](create-app-discovery-reports-in-ocas.md), you can use the Cloud Discovery dashboard to gain insight into how people in your organization are using Office 365 and other cloud apps.</span></span> <span data-ttu-id="0bd60-116">(O painel de descoberta de nuvem também é conhecido como descoberta de aplicativos de produtividade.)</span><span class="sxs-lookup"><span data-stu-id="0bd60-116">(The Cloud Discovery dashboard is also known as Productivity App Discovery.)</span></span>
  
 <span data-ttu-id="0bd60-117">O painel de descoberta de nuvem permite que você exiba informações detalhadas sobre como as pessoas em sua organização estão usando o Office 365 e outros aplicativos.</span><span class="sxs-lookup"><span data-stu-id="0bd60-117">The Cloud Discovery dashboard enables you to view detailed information about how people in your organization are using Office 365 and other apps.</span></span> 
  
![O painel de descoberta de nuvem foi atualizado](media/12712681-c0b3-4cb3-b7fd-2cf2ad4e825f.png)
     
## <a name="go-to-the-cloud-discovery-dashboard"></a><span data-ttu-id="0bd60-119">Vá para o painel de descoberta de nuvem</span><span class="sxs-lookup"><span data-stu-id="0bd60-119">Go to the Cloud Discovery dashboard</span></span>

1. <span data-ttu-id="0bd60-120">Vá para o portal do Cloud app Security[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)() e entre.</span><span class="sxs-lookup"><span data-stu-id="0bd60-120">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span>
    
2. <span data-ttu-id="0bd60-121">Vá para **descobrir** \> **painel de descoberta de nuvem**.</span><span class="sxs-lookup"><span data-stu-id="0bd60-121">Go to **Discover** \> **Cloud Discovery dashboard**.</span></span>
    
## <a name="see-your-top-users-ip-addresses-apps-and-risk-levels"></a><span data-ttu-id="0bd60-122">Ver seus principais usuários, endereços IP, aplicativos e níveis de risco</span><span class="sxs-lookup"><span data-stu-id="0bd60-122">See your top users, IP addresses, apps, and risk levels</span></span>

<span data-ttu-id="0bd60-123">O painel de descoberta de nuvem oferece uma visão geral dos aplicativos usados com o Office 365 em sua organização, quaisquer alertas abertos, principais usuários e níveis de risco.</span><span class="sxs-lookup"><span data-stu-id="0bd60-123">The Cloud Discovery dashboard gives you an at-a-glance overview of apps that are used with Office 365 in your organization, any open alerts, top users, and risk levels.</span></span>
  
![Dashboaard de descoberta de nuvem](media/06696946-fbdf-4781-b5b8-2ac074fcb2a1.png)
  
1. <span data-ttu-id="0bd60-125">Na guia **painel** , examine o uso geral do aplicativo na nuvem em sua organização na seção visão geral na parte superior da tela.</span><span class="sxs-lookup"><span data-stu-id="0bd60-125">On the **Dashboard** tab, look at the overall cloud app use in your organization in the overview section across the top of the screen.</span></span> 
    
2. <span data-ttu-id="0bd60-126">ConFira as **categorias do Office 365** para aplicativos usados em sua organização.</span><span class="sxs-lookup"><span data-stu-id="0bd60-126">See the **Office 365 categories** for apps that are used in your organization.</span></span> 
    
3. <span data-ttu-id="0bd60-127">Examine o widget **aplicativos** descobertos para ver o uso do Office 365 e outros aplicativos neste modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="0bd60-127">Look at the **Discovered apps** widget to see usage of Office 365 and other apps in this view.</span></span> 
    
4. <span data-ttu-id="0bd60-128">Examine o widget **principais usuários** e **endereços IP principais** para identificar aqueles que usam o Office 365 e os aplicativos de nuvem mais em sua organização.</span><span class="sxs-lookup"><span data-stu-id="0bd60-128">Look at the **Top users** and **Top IP addresses** widget to identify those who use Office 365 and cloud apps the most in your organization.</span></span> 
    
5. <span data-ttu-id="0bd60-129">Veja onde os aplicativos que as pessoas estão usando são por localização geográfica usando o mapa de **localização do centro de aplicativos** .</span><span class="sxs-lookup"><span data-stu-id="0bd60-129">See where the apps people are using are by geographical location by using the **Apps headquarters location** map.</span></span> 
    
6. <span data-ttu-id="0bd60-130">Acima da área mapas, confira a pontuação de risco dos aplicativos detectados na visão geral dos **níveis de risco** .</span><span class="sxs-lookup"><span data-stu-id="0bd60-130">Above the maps area, take a look at the risk score of the discovered apps in the **Risk levels** overview.</span></span> <span data-ttu-id="0bd60-131">Você pode examinar riscos pelos mesmos grupos e categorias usados na área **aplicativos** descobertos.</span><span class="sxs-lookup"><span data-stu-id="0bd60-131">You can look at risks by the same groups and categories that you used in the **Discovered apps** area.</span></span> <span data-ttu-id="0bd60-132">Por exemplo, você pode ver quanto tráfego em cada agrupamento é de aplicativos de alto, médio ou baixo risco.</span><span class="sxs-lookup"><span data-stu-id="0bd60-132">For example, you can see how much traffic in each grouping is from high, medium, or low risk apps.</span></span> 
    
## <a name="dive-deeper-into-the-information"></a><span data-ttu-id="0bd60-133">Mergulhe mais fundo nas informações</span><span class="sxs-lookup"><span data-stu-id="0bd60-133">Dive deeper into the information</span></span>

<span data-ttu-id="0bd60-134">Você pode usar a descoberta de nuvem para obter uma análise mais profunda de aplicativos, subdomínios, endereços IP e usuários.</span><span class="sxs-lookup"><span data-stu-id="0bd60-134">You can use Cloud Discovery to take a deeper look at apps, subdomains, IP addresses, and users.</span></span>
  
1. <span data-ttu-id="0bd60-135">No painel de descoberta de nuvem, escolha a guia **aplicativos** descobertos.</span><span class="sxs-lookup"><span data-stu-id="0bd60-135">In the Cloud Discovery dashboard, choose the **Discovered apps** tab.</span></span> 
    
2. <span data-ttu-id="0bd60-136">Use a seção filtros para exibir os aplicativos por nome, categoria, nível de uso ou data da última exibição.</span><span class="sxs-lookup"><span data-stu-id="0bd60-136">Use the filters section to view apps by name, category, usage level, or last seen date.</span></span>
    
3. <span data-ttu-id="0bd60-137">Na lista de resultados, passe o mouse por um nome de aplicativo para revelar o link de subdomínios de **exibição** .</span><span class="sxs-lookup"><span data-stu-id="0bd60-137">In the list of results, hover by an app name to reveal the **View sub-domains** link.</span></span><br/> <span data-ttu-id="0bd60-138">![Focalize ao lado de um aplicativo para mostrar um link para exibir os detalhes do subdomínio](media/4a212215-8a2c-46fd-9ef9-89e4064658a6.png)</span><span class="sxs-lookup"><span data-stu-id="0bd60-138">![Hover next to an app to reveal a link to view subdomain details](media/4a212215-8a2c-46fd-9ef9-89e4064658a6.png)</span></span><br/><span data-ttu-id="0bd60-139">Serão exibidas informações detalhadas sobre o aplicativo selecionado.</span><span class="sxs-lookup"><span data-stu-id="0bd60-139">Detailed information about the selected app will appear.</span></span>
    
4. <span data-ttu-id="0bd60-140">Para exibir detalhes sobre endereços IP, escolha a guia **endereços IP** .</span><span class="sxs-lookup"><span data-stu-id="0bd60-140">To view details about IP addresses, choose the **IP addresses** tab.</span></span><br/><span data-ttu-id="0bd60-141">![A descoberta de nuvem mostra informações detalhadas sobre endereços IP](media/0c742bf6-da9e-4d22-8656-a27a5007d5d5.png)</span><span class="sxs-lookup"><span data-stu-id="0bd60-141">![Cloud Discovery shows detailed information about IP addresses](media/0c742bf6-da9e-4d22-8656-a27a5007d5d5.png)</span></span><br/><span data-ttu-id="0bd60-142">Na lista de resultados, selecione um endereço IP individual para exibir informações mais detalhadas.</span><span class="sxs-lookup"><span data-stu-id="0bd60-142">In the list of results, select an individual IP address to view more detailed information.</span></span>
    
5. <span data-ttu-id="0bd60-143">Para exibir detalhes sobre os usuários do Office 365 dentro da sua organização, escolha a guia **usuários** .</span><span class="sxs-lookup"><span data-stu-id="0bd60-143">To view details about Office 365 users within your organization, choose the **Users** tab.</span></span><br/><span data-ttu-id="0bd60-144">![Descoberta de nuvem-informações de usuários](media/2d9c2d85-01e6-4057-8020-d9a68f26bbac.png)</span><span class="sxs-lookup"><span data-stu-id="0bd60-144">![Cloud Discovery - users info](media/2d9c2d85-01e6-4057-8020-d9a68f26bbac.png)</span></span>
  
## <a name="exclude-entities"></a><span data-ttu-id="0bd60-145">Excluir entidades</span><span class="sxs-lookup"><span data-stu-id="0bd60-145">Exclude entities</span></span>

<span data-ttu-id="0bd60-146">Você pode excluir determinados usuários do sistema ou endereços IP para se concentrar em informações mais específicas.</span><span class="sxs-lookup"><span data-stu-id="0bd60-146">You can exclude certain system users or IP addresses in order to focus on more specific information.</span></span>
  
1. <span data-ttu-id="0bd60-147">Escolha **configurações** \> **descoberta de nuvem**.</span><span class="sxs-lookup"><span data-stu-id="0bd60-147">Choose **Settings** \> **Cloud Discovery settings**.</span></span>
    
2. <span data-ttu-id="0bd60-148">Escolha **excluir entidades**.</span><span class="sxs-lookup"><span data-stu-id="0bd60-148">Choose **Exclude entities**.</span></span>
    
3. <span data-ttu-id="0bd60-149">Escolha **usuários excluídos** ou **endereços IP excluídos**.</span><span class="sxs-lookup"><span data-stu-id="0bd60-149">Choose either **Excluded users** or **Excluded IP addresses**.</span></span>
    
4. <span data-ttu-id="0bd60-150">Especifique os usuários ou endereços IP e, na caixa **comentários** , digite as informações sobre o motivo pelo qual você está excluindo os endereços IP ou usuários.</span><span class="sxs-lookup"><span data-stu-id="0bd60-150">Specify the users or IP addresses, and in the **Comments** box, type information about why you are excluding those users or IP addresses.</span></span> 
    
5. <span data-ttu-id="0bd60-151">Escolha **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="0bd60-151">Choose **Add**.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="0bd60-152">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="0bd60-152">Next steps</span></span>

- [<span data-ttu-id="0bd60-153">ReVisar e executar ação em alertas</span><span class="sxs-lookup"><span data-stu-id="0bd60-153">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="0bd60-154">Criar relatórios de descoberta de aplicativos</span><span class="sxs-lookup"><span data-stu-id="0bd60-154">Create app discovery reports</span></span>](create-app-discovery-reports-in-ocas.md)
    
- <span data-ttu-id="0bd60-155">ReVisar suas [atividades de utilização do Office 365 Cloud app Security](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="0bd60-155">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    


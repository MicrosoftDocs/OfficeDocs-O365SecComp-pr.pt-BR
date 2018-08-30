---
title: Analisar descobertas de aplicativos do Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 3/19/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: aac65513-e75e-4c82-a668-9a6604dd9f9d
description: Analisar relatórios de descoberta de aplicativo no gerenciamento de segurança avançadas pode ajudá-lo a saber mais sobre como as pessoas na sua organização usam aplicativos na nuvem. Depois de criar relatórios de descoberta de aplicativo usando os arquivos de log de seus firewalls e proxies, revise os resultados no painel de descoberta do aplicativo.
ms.openlocfilehash: 188ef87920b26069e7d99057662b3812be22e46c
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523461"
---
# <a name="review-app-discovery-findings-in-office-365-cloud-app-security"></a><span data-ttu-id="460b3-104">Analisar descobertas de aplicativos do Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="460b3-104">Review app discovery findings in Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="460b3-105">Avaliação * *\>**</span><span class="sxs-lookup"><span data-stu-id="460b3-105">****Evaluation** \>**</span></span>|<span data-ttu-id="460b3-106">Planejamento * *\>**</span><span class="sxs-lookup"><span data-stu-id="460b3-106">****Planning** \>**</span></span>|<span data-ttu-id="460b3-107">Implantação * *\>**</span><span class="sxs-lookup"><span data-stu-id="460b3-107">****Deployment** \>**</span></span>|<span data-ttu-id="460b3-108">Utilização \* \* \*</span><span class="sxs-lookup"><span data-stu-id="460b3-108">****Utilization****</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="460b3-109">Comece a avaliar</span><span class="sxs-lookup"><span data-stu-id="460b3-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="460b3-110">Começar a planejar</span><span class="sxs-lookup"><span data-stu-id="460b3-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="460b3-111">Começar a implantar</span><span class="sxs-lookup"><span data-stu-id="460b3-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="460b3-112">Você está aqui!</span><span class="sxs-lookup"><span data-stu-id="460b3-112">You are here!</span></span>  <br/> [<span data-ttu-id="460b3-113">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="460b3-113">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="460b3-p102">O painel de descoberta de nuvem trabalha com logs de tráfego da web para fornecer informações detalhadas sobre o uso do aplicativo de nuvem da sua organização. Se você for um administrador global, administrador de segurança ou leitor de segurança e sua organização tenha [criado os relatórios de descoberta de aplicativo na segurança de aplicativo de nuvem do Office 365](create-app-discovery-reports-in-ocas.md), você pode usar o painel de descoberta de nuvem para percepção como as pessoas na sua organização estiver usando o Office 365 e outros aplicativos de nuvem. (O painel de descoberta de nuvem é também conhecido como descoberta de aplicativos de produtividade.)</span><span class="sxs-lookup"><span data-stu-id="460b3-p102">The Cloud Discovery dashboard works with your organization's web traffic logs to provide detailed information about cloud app usage. If you're a global administrator, security administrator, or security reader, and your organization has [created app discovery reports in Office 365 Cloud App Security](create-app-discovery-reports-in-ocas.md), you can use the Cloud Discovery dashboard to gain insight into how people in your organization are using Office 365 and other cloud apps. (The Cloud Discovery dashboard is also known as Productivity App Discovery.)</span></span>
  
 <span data-ttu-id="460b3-117">**A partir de março 2018, o painel de descoberta de nuvem tem recursos novos** que facilitam exibir informações detalhadas sobre como as pessoas na sua organização estiver usando o Office 365 e outros aplicativos.</span><span class="sxs-lookup"><span data-stu-id="460b3-117">**As of March 2018, the Cloud Discovery dashboard has new features** that make it easier to view detailed information about how people in your organization are using Office 365 and other apps.</span></span> 
  
![O painel de descoberta de nuvem foi atualizado](media/12712681-c0b3-4cb3-b7fd-2cf2ad4e825f.png)
     
## <a name="go-to-the-cloud-discovery-dashboard"></a><span data-ttu-id="460b3-119">Vá para o painel de descoberta de nuvem</span><span class="sxs-lookup"><span data-stu-id="460b3-119">Go to the Cloud Discovery dashboard</span></span>

1. <span data-ttu-id="460b3-p103">Vá para [https://protection.office.com](https://protection.office.com) e entrar usando sua conta de trabalho ou da escola para o Office 365. (Isso leva você para a segurança &amp; Centro de conformidade.)</span><span class="sxs-lookup"><span data-stu-id="460b3-p103">Go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account for Office 365. (This takes you to the Security &amp; Compliance Center.)</span></span> 
    
2. <span data-ttu-id="460b3-122">Na segurança &amp; Centro de conformidade, escolha **alertas** \> **avançadas de gerenciar alertas**.</span><span class="sxs-lookup"><span data-stu-id="460b3-122">In the Security &amp; Compliance Center, choose **Alerts** \> **Manage advanced alerts**.</span></span>
    
    <span data-ttu-id="460b3-123">(Se a segurança de aplicativo de nuvem do Office 365 ainda não estiver habilitada, e você é um administrador global, [Ative a segurança de aplicativo do Office 365 nuvem](turn-on-office-365-cas.md).)</span><span class="sxs-lookup"><span data-stu-id="460b3-123">(If Office 365 Cloud App Security is not yet enabled, and you are a global administrator, [turn on Office 365 Cloud App Security](turn-on-office-365-cas.md).)</span></span>
    
3. <span data-ttu-id="460b3-124">Escolha **vá para segurança de aplicativo do Office 365 nuvem**.</span><span class="sxs-lookup"><span data-stu-id="460b3-124">Choose **Go to Office 365 Cloud App Security**.</span></span>
    
4. <span data-ttu-id="460b3-125">Vá para **descobrir** \> **Painel de descoberta de nuvem**.</span><span class="sxs-lookup"><span data-stu-id="460b3-125">Go to **Discover** \> **Cloud Discovery dashboard**.</span></span>
    
## <a name="see-your-top-users-ip-addresses-apps-and-risk-levels"></a><span data-ttu-id="460b3-126">Veja os principais usuários, endereços IP, aplicativos e níveis de risco</span><span class="sxs-lookup"><span data-stu-id="460b3-126">See your top users, IP addresses, apps, and risk levels</span></span>

<span data-ttu-id="460b3-127">O painel de descoberta de nuvem oferece uma visão geral de um resumo geral de aplicativos que são usados com o Office 365 em sua organização, qualquer open alertas, principais usuários e níveis de risco.</span><span class="sxs-lookup"><span data-stu-id="460b3-127">The Cloud Discovery dashboard gives you an at-a-glance overview of apps that are used with Office 365 in your organization, any open alerts, top users, and risk levels.</span></span>
  
![Dashboaard da descoberta de nuvem](media/06696946-fbdf-4781-b5b8-2ac074fcb2a1.png)
  
1. <span data-ttu-id="460b3-129">Na guia do **painel** , examine o uso geral de aplicativo de nuvem em sua organização, na seção Visão geral na parte superior da tela.</span><span class="sxs-lookup"><span data-stu-id="460b3-129">On the **Dashboard** tab, look at the overall cloud app use in your organization in the overview section across the top of the screen.</span></span> 
    
2. <span data-ttu-id="460b3-130">Consulte as **categorias do Office 365** para aplicativos que são usados em sua organização.</span><span class="sxs-lookup"><span data-stu-id="460b3-130">See the **Office 365 categories** for apps that are used in your organization.</span></span> 
    
3. <span data-ttu-id="460b3-131">Examinar o widget **Discovered apps** para ver o uso do Office 365 e outros aplicativos nesse modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="460b3-131">Look at the **Discovered apps** widget to see usage of Office 365 and other apps in this view.</span></span> 
    
4. <span data-ttu-id="460b3-132">Examinar o widget **principais usuários** e **endereços IP de cima** para identificar aqueles que usam o Office 365 e aplicativos o máximo em sua organização em nuvem.</span><span class="sxs-lookup"><span data-stu-id="460b3-132">Look at the **Top users** and **Top IP addresses** widget to identify those who use Office 365 and cloud apps the most in your organization.</span></span> 
    
5. <span data-ttu-id="460b3-133">Visualizar onde estão os aplicativos pessoas estão usando por localização geográfica, usando o mapa de **local de matrizes de aplicativos** .</span><span class="sxs-lookup"><span data-stu-id="460b3-133">See where the apps people are using are by geographical location by using the **Apps headquarters location** map.</span></span> 
    
6. <span data-ttu-id="460b3-p104">Acima da área de mapas, dê uma olhada na pontuação de risco dos aplicativos descobertos na visão geral de **níveis de risco** . Você pode examinar riscos pelo mesmo grupos e categorias que você usou na área **Discovered aplicativos** . Por exemplo, você pode ver a quantidade de tráfego em cada agrupamento é de aplicativos de risco baixa, média ou alta.</span><span class="sxs-lookup"><span data-stu-id="460b3-p104">Above the maps area, take a look at the risk score of the discovered apps in the **Risk levels** overview. You can look at risks by the same groups and categories that you used in the **Discovered apps** area. For example, you can see how much traffic in each grouping is from high, medium, or low risk apps.</span></span> 
    
## <a name="dive-deeper-into-the-information"></a><span data-ttu-id="460b3-137">Se aprofundam nas informações</span><span class="sxs-lookup"><span data-stu-id="460b3-137">Dive deeper into the information</span></span>

<span data-ttu-id="460b3-138">Você pode usar a descoberta de nuvem para dar uma olhada mais aprofundada em aplicativos, subdomínios, endereços IP e os usuários.</span><span class="sxs-lookup"><span data-stu-id="460b3-138">You can use Cloud Discovery to take a deeper look at apps, subdomains, IP addresses, and users.</span></span>
  
1. <span data-ttu-id="460b3-139">No painel descoberta de nuvem, escolha a guia de **Discovered aplicativos** .</span><span class="sxs-lookup"><span data-stu-id="460b3-139">In the Cloud Discovery dashboard, choose the **Discovered apps** tab.</span></span> 
    
2. <span data-ttu-id="460b3-140">Use a seção filtros para exibir aplicativos pelo nome, categoria, nível de uso ou data da última Vista.</span><span class="sxs-lookup"><span data-stu-id="460b3-140">Use the filters section to view apps by name, category, usage level, or last seen date.</span></span>
    
3. <span data-ttu-id="460b3-141">Na lista de resultados, passe o mouse por um nome de aplicativo para revelar o link **Exibir subdomínios** .</span><span class="sxs-lookup"><span data-stu-id="460b3-141">In the list of results, hover by an app name to reveal the **View sub-domains** link.</span></span> 
    
    ![Passe o mouse ao lado de um aplicativo para revelar um link para exibir detalhes do subdomínio](media/4a212215-8a2c-46fd-9ef9-89e4064658a6.png)
  
    <span data-ttu-id="460b3-143">Informações detalhadas sobre o aplicativo selecionado serão exibida.</span><span class="sxs-lookup"><span data-stu-id="460b3-143">Detailed information about the selected app will appear.</span></span>
    
4. <span data-ttu-id="460b3-144">Para exibir detalhes sobre os endereços IP, escolha a guia de **endereços IP** .</span><span class="sxs-lookup"><span data-stu-id="460b3-144">To view details about IP addresses, choose the **IP addresses** tab.</span></span> 
    
    ![Descoberta de nuvem mostra informações detalhadas sobre endereços IP](media/0c742bf6-da9e-4d22-8656-a27a5007d5d5.png)
  
    <span data-ttu-id="460b3-146">Na lista de resultados, selecione um endereço IP individual para exibir informações mais detalhadas.</span><span class="sxs-lookup"><span data-stu-id="460b3-146">In the list of results, select an individual IP address to view more detailed information.</span></span>
    
5. <span data-ttu-id="460b3-147">Para exibir detalhes sobre os usuários do Office 365 dentro da sua organização, escolha a guia de **usuários** .</span><span class="sxs-lookup"><span data-stu-id="460b3-147">To view details about Office 365 users within your organization, choose the **Users** tab.</span></span> 
    
    ![Descoberta de nuvem - info de usuários](media/2d9c2d85-01e6-4057-8020-d9a68f26bbac.png)
  
## <a name="exclude-entities"></a><span data-ttu-id="460b3-149">Excluir entidades</span><span class="sxs-lookup"><span data-stu-id="460b3-149">Exclude entities</span></span>

<span data-ttu-id="460b3-150">Você pode excluir determinados usuários do sistema ou endereços IP para focalizar em informações mais específicas.</span><span class="sxs-lookup"><span data-stu-id="460b3-150">You can exclude certain system users or IP addresses in order to focus on more specific information.</span></span>
  
1. <span data-ttu-id="460b3-151">Escolha **configurações** \> **configurações de descoberta de nuvem**.</span><span class="sxs-lookup"><span data-stu-id="460b3-151">Choose **Settings** \> **Cloud Discovery settings**.</span></span>
    
2. <span data-ttu-id="460b3-152">Escolha **Excluir entidades**.</span><span class="sxs-lookup"><span data-stu-id="460b3-152">Choose **Exclude entities**.</span></span>
    
3. <span data-ttu-id="460b3-153">Escolha **usuários excluídos** ou **endereços IP excluídos**.</span><span class="sxs-lookup"><span data-stu-id="460b3-153">Choose either **Excluded users** or **Excluded IP addresses**.</span></span>
    
4. <span data-ttu-id="460b3-154">Especificar os usuários ou os endereços IP e, na caixa **comentários** , digite as informações sobre por que você está excluindo a esses usuários ou endereços IP.</span><span class="sxs-lookup"><span data-stu-id="460b3-154">Specify the users or IP addresses, and in the **Comments** box, type information about why you are excluding those users or IP addresses.</span></span> 
    
5. <span data-ttu-id="460b3-155">Selecione **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="460b3-155">Choose **Add**.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="460b3-156">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="460b3-156">Next steps</span></span>

- [<span data-ttu-id="460b3-157">Revise e agir em alertas</span><span class="sxs-lookup"><span data-stu-id="460b3-157">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="460b3-158">Criar relatórios de descoberta de aplicativo</span><span class="sxs-lookup"><span data-stu-id="460b3-158">Create app discovery reports</span></span>](create-app-discovery-reports-in-ocas.md)
    
- <span data-ttu-id="460b3-159">Revise suas [atividades de utilização para segurança de aplicativo de nuvem do Office 365](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="460b3-159">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    


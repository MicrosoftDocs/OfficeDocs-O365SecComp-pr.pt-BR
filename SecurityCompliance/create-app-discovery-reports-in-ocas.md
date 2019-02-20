---
title: Criar relatórios de descoberta de aplicativo usando o Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 1/28/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 3e68e691-1fc4-4d3e-a2c0-d3134eb64055
description: Criar relatórios com o Office 365 Cloud app Security que permite que você entenda como as pessoas em sua organização estão usando o Office 365 e outros aplicativos.
ms.openlocfilehash: e0d515ddd9b08aa4a70276177060f273cc89949e
ms.sourcegitcommit: 8679937354c1d8870ecd41519a59d2d7468c23c4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2019
ms.locfileid: "30087290"
---
# <a name="create-app-discovery-reports-using-office-365-cloud-app-security"></a><span data-ttu-id="a312e-103">Criar relatórios de descoberta de aplicativo usando o Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="a312e-103">Create app discovery reports using Office 365 Cloud App Security</span></span>

|<span data-ttu-id="a312e-104">Avaliação \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="a312e-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="a312e-105">Planejamento \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="a312e-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="a312e-106">Implantação \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="a312e-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="a312e-107">Utilização \* \* \*</span><span class="sxs-lookup"><span data-stu-id="a312e-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="a312e-108">Iniciar avaliação</span><span class="sxs-lookup"><span data-stu-id="a312e-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="a312e-109">Iniciar planejamento</span><span class="sxs-lookup"><span data-stu-id="a312e-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="a312e-110">Iniciar implantação</span><span class="sxs-lookup"><span data-stu-id="a312e-110">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="a312e-111">Você está aqui!</span><span class="sxs-lookup"><span data-stu-id="a312e-111">You are here!</span></span>  <br/> [<span data-ttu-id="a312e-112">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="a312e-112">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="a312e-p101">O Office 365 Cloud app Security ajuda administradores globais, administradores de segurança e leitores de segurança a obter informações sobre os serviços de nuvem que as pessoas de uma organização estão usando. Por exemplo, você pode ver onde os usuários estão armazenando e colaborando em documentos e quantos dados estão sendo carregados para aplicativos ou serviços que estão fora do Office 365.</span><span class="sxs-lookup"><span data-stu-id="a312e-p101">Office 365 Cloud App Security helps global administrators, security administrators, and security readers gain insight into the cloud services people in an organization are using. For example, you can see where users are storing and collaborating on documents and how much data is being uploaded to apps or services that are outside of Office 365.</span></span>
  
<span data-ttu-id="a312e-115">Para gerar um relatório de descoberta de aplicativos, você carrega manualmente seus arquivos de log de tráfego da Web de seus firewalls e proxies e, em seguida, o Office 365 Cloud app Security analisa e analisa esses arquivos para o seu relatório.</span><span class="sxs-lookup"><span data-stu-id="a312e-115">To generate an app discovery report, you manually upload your web traffic log files from your firewalls and proxies, and then Office 365 Cloud App Security parses and analyzes those files for your report.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a312e-p102">Você deve ser um administrador global, administrador de segurança ou leitor de segurança para executar as tarefas descritas neste artigo. Para saber mais, confira [permissões no centro de conformidade &amp; de segurança do Office 365](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="a312e-p102">You must be a global administrator, security administrator, or security reader to perform the tasks described in this article. To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
## <a name="create-a-report-with-app-discovery"></a><span data-ttu-id="a312e-118">Criar um relatório com descoberta de aplicativos</span><span class="sxs-lookup"><span data-stu-id="a312e-118">Create a report with app discovery</span></span>

<span data-ttu-id="a312e-119">Para criar um relatório de descoberta de aplicativos, identifique a fonte de dados do fornecedor para os arquivos de log que você deseja que sejam analisados, selecione os arquivos de log e solicite o relatório.</span><span class="sxs-lookup"><span data-stu-id="a312e-119">To create an app discovery report, you identify the vendor data source for the log files that you want to have analyzed, select the log files, and then request the report.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a312e-120">Use arquivos de log de tráfego da Web que incluem períodos de pico de tráfego para obter a melhor representação de uso em sua organização.</span><span class="sxs-lookup"><span data-stu-id="a312e-120">Use web traffic log files that include peak traffic periods to get the best representation of usage in your organization.</span></span> 
  
1. <span data-ttu-id="a312e-121">Coletar seus [logs de tráfego da Web e fontes de dados para o Office 365 Cloud app Security](web-traffic-logs-and-data-sources-for-ocas.md).</span><span class="sxs-lookup"><span data-stu-id="a312e-121">Collect your [web traffic logs and data sources for Office 365 Cloud App Security](web-traffic-logs-and-data-sources-for-ocas.md).</span></span>
    
2. <span data-ttu-id="a312e-122">Vá para o portal do Cloud app Security[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)() e entre.</span><span class="sxs-lookup"><span data-stu-id="a312e-122">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span> 
       
3. <span data-ttu-id="a312e-123">Escolha **descobrir** \> **criar novo relatório**.</span><span class="sxs-lookup"><span data-stu-id="a312e-123">Choose **Discover** \> **Create new report**.</span></span> <br><span data-ttu-id="a312e-124">![No portal CAS do Office 365, escolha descobrir](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)</span><span class="sxs-lookup"><span data-stu-id="a312e-124">![In the Office 365 CAS portal, choose Discover](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)</span></span><br>
  
4. <span data-ttu-id="a312e-125">Especifique um nome e uma descrição para o seu relatório e, em seguida, selecione a fonte de dados para os logs de tráfego da Web na lista de **fontes de dados** .</span><span class="sxs-lookup"><span data-stu-id="a312e-125">Specify a name and description for your report, and then select the data source for your web traffic logs in the **Data source** list.</span></span> <br><span data-ttu-id="a312e-126">![Em CAS do O365, escolha \> descobrir criar novo relatório](media/22e660f0-5eb2-49fa-9fea-f88a5809a07b.png)</span><span class="sxs-lookup"><span data-stu-id="a312e-126">![In O365 CAS, choose Discover \> Create new report](media/22e660f0-5eb2-49fa-9fea-f88a5809a07b.png)</span></span><br><span data-ttu-id="a312e-p103">Se uma fonte de dados que você gostaria de usar não estiver listada, você poderá solicitar que ela seja adicionada. Selecione **outro** para a **fonte de dados**e, em seguida, digite o nome da fonte de dados que você está tentando carregar. Examinaremos o log e informaremos se Adicionamos suporte para a fonte de dados que a gerou.</span><span class="sxs-lookup"><span data-stu-id="a312e-p103">If a data source that you'd like to use is not listed, you can request that it be added. Select **Other** for **Data source**, and then type the name of the data source that you're trying to upload. We'll review the log, and let you know if we add support for the data source that generated it.</span></span> 
  
5. <span data-ttu-id="a312e-p104">Navegue até o local dos arquivos de log coletados e selecione os arquivos. Os arquivos de log devem ter sido gerados pela fonte de dados que você escolheu para o relatório.</span><span class="sxs-lookup"><span data-stu-id="a312e-p104">Browse to the location of the log files you collected and select the files. The log files must have been generated by the data source that you chose for the report.</span></span>
    
6. <span data-ttu-id="a312e-132">Clique em **criar** para iniciar o processo de criação de relatórios.</span><span class="sxs-lookup"><span data-stu-id="a312e-132">Click **Create** to start the report creation process.</span></span> 
    
7. <span data-ttu-id="a312e-p105">Para ver o status do relatório, clique em **Gerenciar relatórios de instantâneo**. Quando um relatório estiver pronto, você verá a opção **Exibir relatório** .</span><span class="sxs-lookup"><span data-stu-id="a312e-p105">To see the status of the report, click **Manage snapshot reports**. When a report is ready, you'll see the **View report** option.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="a312e-135">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="a312e-135">Next steps</span></span>

- [<span data-ttu-id="a312e-136">ReVisar e executar ação em alertas</span><span class="sxs-lookup"><span data-stu-id="a312e-136">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="a312e-137">Analisar descobertas de aplicativos do Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="a312e-137">Review app discovery findings in Office 365 Cloud App Security</span></span>](review-app-discovery-findings-in-ocas.md)
    
- <span data-ttu-id="a312e-138">ReVisar suas [atividades de utilização do Office 365 Cloud app Security](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="a312e-138">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    


---
title: Criar relatórios de descoberta de aplicativo usando o Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/26/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 3e68e691-1fc4-4d3e-a2c0-d3134eb64055
description: Crie relatórios com o Office 365 App segurança na nuvem que permitem que você entenda como pessoas da sua organização estiver usando o Office 365 e outros aplicativos.
ms.openlocfilehash: 6842912f42072e21608955bde5250f0774c7bba4
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523474"
---
# <a name="create-app-discovery-reports-using-office-365-cloud-app-security"></a><span data-ttu-id="07a13-103">Criar relatórios de descoberta de aplicativo usando o Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="07a13-103">Create app discovery reports using Office 365 Cloud App Security</span></span>

<span data-ttu-id="07a13-104">Gerenciamento de segurança avançada do Office 365 agora é segurança de aplicativo de nuvem do Office 365.</span><span class="sxs-lookup"><span data-stu-id="07a13-104">Office 365 Advanced Security Management is now Office 365 Cloud App Security.</span></span>
  
|<span data-ttu-id="07a13-105">Avaliação * *\>**</span><span class="sxs-lookup"><span data-stu-id="07a13-105">****Evaluation** \>**</span></span>|<span data-ttu-id="07a13-106">Planejamento * *\>**</span><span class="sxs-lookup"><span data-stu-id="07a13-106">****Planning** \>**</span></span>|<span data-ttu-id="07a13-107">Implantação * *\>**</span><span class="sxs-lookup"><span data-stu-id="07a13-107">****Deployment** \>**</span></span>|<span data-ttu-id="07a13-108">Utilização \* \* \*</span><span class="sxs-lookup"><span data-stu-id="07a13-108">****Utilization****</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="07a13-109">Comece a avaliar</span><span class="sxs-lookup"><span data-stu-id="07a13-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="07a13-110">Começar a planejar</span><span class="sxs-lookup"><span data-stu-id="07a13-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="07a13-111">Começar a implantar</span><span class="sxs-lookup"><span data-stu-id="07a13-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="07a13-112">Você está aqui!</span><span class="sxs-lookup"><span data-stu-id="07a13-112">You are here!</span></span>  <br/> [<span data-ttu-id="07a13-113">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="07a13-113">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="07a13-p101">Segurança de aplicativo de nuvem do Office 365 ajuda administradores globais, os administradores de segurança e leitores de segurança percepção pessoas em uma organização estiver usando os serviços de nuvem. Por exemplo, você pode ver onde os usuários estão armazenando e colaborando em documentos e a quantidade de dados está sendo carregado para aplicativos ou serviços que estão fora do Office 365.</span><span class="sxs-lookup"><span data-stu-id="07a13-p101">Office 365 Cloud App Security helps global administrators, security administrators, and security readers gain insight into the cloud services people in an organization are using. For example, you can see where users are storing and collaborating on documents and how much data is being uploaded to apps or services that are outside of Office 365.</span></span>
  
<span data-ttu-id="07a13-116">Para gerar um relatório de descoberta de aplicativo, você carregar seus arquivos de log do tráfego da web a partir de seus firewalls e proxies manualmente e, em seguida, a segurança de aplicativo de nuvem do Office 365 analisa e analisa esses arquivos para o seu relatório.</span><span class="sxs-lookup"><span data-stu-id="07a13-116">To generate an app discovery report, you manually upload your web traffic log files from your firewalls and proxies, and then Office 365 Cloud App Security parses and analyzes those files for your report.</span></span>
  
> [!NOTE]
> <span data-ttu-id="07a13-p102">Você deve ser um administrador global, administrador de segurança ou leitor de segurança para executar as tarefas descritas neste artigo. Para saber mais, consulte [permissões no Office 365 Security &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="07a13-p102">You must be a global administrator, security administrator, or security reader to perform the tasks described in this article. To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
## <a name="create-a-report-with-app-discovery"></a><span data-ttu-id="07a13-119">Criar um relatório com a descoberta de aplicativo</span><span class="sxs-lookup"><span data-stu-id="07a13-119">Create a report with app discovery</span></span>

<span data-ttu-id="07a13-120">Para criar um relatório de descoberta de aplicativo, você deve identificar a fonte de dados de fornecedor para os arquivos de log que você deseja ter analisado, selecione os arquivos de log e, em seguida, solicitar o relatório.</span><span class="sxs-lookup"><span data-stu-id="07a13-120">To create an app discovery report, you identify the vendor data source for the log files that you want to have analyzed, select the log files, and then request the report.</span></span>
  
> [!NOTE]
> <span data-ttu-id="07a13-121">Use os arquivos de log do tráfego da web que incluem os períodos de tráfego para obter a melhor representação de uso em sua organização.</span><span class="sxs-lookup"><span data-stu-id="07a13-121">Use web traffic log files that include peak traffic periods to get the best representation of usage in your organization.</span></span> 
  
1. <span data-ttu-id="07a13-122">Colete [logs de tráfego da web e fontes de dados para segurança de aplicativo de nuvem do Office 365](web-traffic-logs-and-data-sources-for-ocas.md).</span><span class="sxs-lookup"><span data-stu-id="07a13-122">Collect your [web traffic logs and data sources for Office 365 Cloud App Security](web-traffic-logs-and-data-sources-for-ocas.md).</span></span>
    
2. <span data-ttu-id="07a13-123">Vá para [https://protection.office.com](https://protection.office.com) e entrar usando sua conta do trabalho ou da escola.</span><span class="sxs-lookup"><span data-stu-id="07a13-123">Go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account.</span></span> 
    
3. <span data-ttu-id="07a13-124">Na segurança &amp; Centro de conformidade, escolha **alertas** \> **avançadas de gerenciar alertas**.</span><span class="sxs-lookup"><span data-stu-id="07a13-124">In the Security &amp; Compliance Center, choose **Alerts** \> **Manage advanced alerts**.</span></span>
    
4. <span data-ttu-id="07a13-125">Escolha **vá para segurança de aplicativo do Office 365 nuvem**.</span><span class="sxs-lookup"><span data-stu-id="07a13-125">Choose **Go to Office 365 Cloud App Security**.</span></span>
    
5. <span data-ttu-id="07a13-126">Escolha **descobrir** \> **Criar novo relatório**.</span><span class="sxs-lookup"><span data-stu-id="07a13-126">Choose **Discover** \> **Create new report**.</span></span>
    
    ![No portal do Office 365 CAS, escolha Discover](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)
  
6. <span data-ttu-id="07a13-128">Especifique um nome e uma descrição para o seu relatório e, em seguida, selecione a fonte de dados de logs de tráfego da web na lista **fonte de dados** .</span><span class="sxs-lookup"><span data-stu-id="07a13-128">Specify a name and description for your report, and then select the data source for your web traffic logs in the **Data source** list.</span></span> 
    
    ![O CAS O365, escolha descobrir \> criar novo relatório](media/22e660f0-5eb2-49fa-9fea-f88a5809a07b.png)
  
    > [!NOTE]
    > <span data-ttu-id="07a13-p103">Se uma fonte de dados que você deseja usar não estiver listada, você poderá solicitar a ser adicionado. Selecione **outra** **fonte**de dados e, em seguida, digite o nome da fonte de dados que você está tentando carregar. Vamos examinar o log e permitem que você saiba se podemos adicionar suporte para a fonte de dados que geraram a ele.</span><span class="sxs-lookup"><span data-stu-id="07a13-p103">If a data source that you'd like to use is not listed, you can request that it be added. Select **Other** for **Data source**, and then type the name of the data source that you're trying to upload. We'll review the log, and let you know if we add support for the data source that generated it.</span></span> 
  
7. <span data-ttu-id="07a13-p104">Navegue até o local dos arquivos de log que você coletou e selecione os arquivos. Os arquivos de log devem ter sido gerados por fonte de dados que você escolheu para o relatório.</span><span class="sxs-lookup"><span data-stu-id="07a13-p104">Browse to the location of the log files you collected and select the files. The log files must have been generated by the data source that you chose for the report.</span></span>
    
8. <span data-ttu-id="07a13-135">Clique em **criar** para iniciar o processo de criação do relatório.</span><span class="sxs-lookup"><span data-stu-id="07a13-135">Click **Create** to start the report creation process.</span></span> 
    
9. <span data-ttu-id="07a13-p105">Para ver o status do relatório, clique em **Gerenciar relatórios de instantâneo**. Quando um relatório estiver pronto, você verá a opção **Exibir relatório** .</span><span class="sxs-lookup"><span data-stu-id="07a13-p105">To see the status of the report, click **Manage snapshot reports**. When a report is ready, you'll see the **View report** option.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="07a13-138">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="07a13-138">Next steps</span></span>

- [<span data-ttu-id="07a13-139">Revise e agir em alertas</span><span class="sxs-lookup"><span data-stu-id="07a13-139">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="07a13-140">Analisar descobertas de aplicativos do Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="07a13-140">Review app discovery findings in Office 365 Cloud App Security</span></span>](review-app-discovery-findings-in-ocas.md)
    
- <span data-ttu-id="07a13-141">Revise suas [atividades de utilização para segurança de aplicativo de nuvem do Office 365](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="07a13-141">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    


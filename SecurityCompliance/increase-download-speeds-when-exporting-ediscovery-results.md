---
title: Aumentar a velocidade de download ao exportar resultados de pesquisa de descoberta eletrônica do Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/14/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: MOE150
ms.assetid: c4c8f689-9d52-4e80-ae4b-1411ee9efc43
description: Saiba como configurar o registro do Windows para aumentar a taxa de transferência de dados ao baixar os resultados da pesquisa e pesquisar dados &amp; do centro de conformidade de segurança do Office 365 e da descoberta eletrônica avançada do Office 365.
ms.openlocfilehash: bafe9eda98b411472098770e4178748eb84f8afd
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216241"
---
# <a name="increase-the-download-speed-when-exporting-ediscovery-search-results-from-office-365"></a><span data-ttu-id="fbad1-103">Aumentar a velocidade de download ao exportar resultados de pesquisa de descoberta eletrônica do Office 365</span><span class="sxs-lookup"><span data-stu-id="fbad1-103">Increase the download speed when exporting eDiscovery search results from Office 365</span></span>

<span data-ttu-id="fbad1-p101">Ao usar a ferramenta de exportação de descoberta eletrônica do Office 365 para baixar os resultados de uma pesquisa de conteúdo no &amp; centro de conformidade de segurança do Office 365 ou baixar dados da descoberta eletrônica avançada do Office 365, a ferramenta inicia um determinado número de exportação simultânea operações para baixar os dados para o computador local. Por padrão, o número de operações simultâneas é definido como 8 vezes o número de núcleos no computador que você está usando para baixar os dados. Por exemplo, se você tiver um computador dual core (ou seja, duas unidades de processamento central em um único chip), o número padrão de operações de exportação simultâneas será 16. Para aumentar a taxa de transferência e acelerar o processo de download, é possível aumentar o número de operações simultâneas Configurando uma configuração do registro do Windows no computador que você usa para baixar os resultados da pesquisa. Para acelerar o processo de download, recomendamos que você comece com uma configuração de 24 operações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="fbad1-p101">When you use the Office 365 eDiscovery Export tool to download the results of a Content Search in the Office 365 Security &amp; Compliance Center or download data from Office 365 Advanced eDiscovery, the tool starts a certain number of concurrent export operations to download the data to your local computer. By default, the number of concurrent operations is set to 8 times the number of cores in the computer you're using to download the data. For example, if you have a dual core computer (meaning two central processing units on one chip), the default number of concurrent export operations is 16. To increase the data transfer throughput and speed-up the download process, you can increase the number of concurrent operations by configuring a Windows Registry setting on the computer that you use to download the search results. To speed-up the download process, we recommend that you start with a setting of 24 concurrent operations.</span></span>
  
<span data-ttu-id="fbad1-p102">Se você baixar os resultados da pesquisa por uma rede de baixa largura de banda, aumentar essa configuração poderá ter um impacto negativo. Como alternativa, é possível aumentar a configuração para mais de 24 operações simultâneas em uma rede de alta largura de banda (o número máximo de operações simultâneas é 512). Depois de definir essa configuração do registro, talvez seja necessário alterá-la para encontrar o número ideal de operações simultâneas para seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="fbad1-p102">If you download search results over a low-bandwidth network, increasing this setting might have a negative impact. Alternatively, you might be able to increase the setting to more than 24 concurrent operations in a high-bandwidth network (the maximum number of concurrent operations is 512). After you configure this registry setting, you might have to change it to find the optimal number of concurrent operations for your environment.</span></span>
  
## <a name="create-a-registry-setting-to-change-the-number-of-concurrent-operations-when-exporting-data"></a><span data-ttu-id="fbad1-112">Criar uma configuração de registro para alterar o número de operações simultâneas ao exportar dados</span><span class="sxs-lookup"><span data-stu-id="fbad1-112">Create a registry setting to change the number of concurrent operations when exporting data</span></span>

<span data-ttu-id="fbad1-113">Execute o procedimento a seguir no computador que você usará para baixar os resultados da pesquisa do &amp; centro de conformidade de segurança ou dos dados da descoberta eletrônica avançada.</span><span class="sxs-lookup"><span data-stu-id="fbad1-113">Perform the following procedure on the computer that you'll use to download search results from the Security &amp; Compliance Center or data from Advanced eDiscovery.</span></span>
  
1. <span data-ttu-id="fbad1-114">Feche a ferramenta de exportação de descoberta eletrônica do Office 365 se ela estiver aberta.</span><span class="sxs-lookup"><span data-stu-id="fbad1-114">Close the Office 365 eDiscovery Export tool if it's open.</span></span> 
    
2. <span data-ttu-id="fbad1-115">Salve o seguinte texto em um arquivo de registro de janela usando um sufixo de nome de arquivo. reg; por exemplo, ConcurrentOperations. reg.</span><span class="sxs-lookup"><span data-stu-id="fbad1-115">Save the following text to a Window registry file by using a filename suffix of .reg; for example, ConcurrentOperations.reg.</span></span> 
    
    ```
    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool]
    "DownloadConcurrency"="24"
    ```

    <span data-ttu-id="fbad1-116">Como explicado anteriormente, recomendamos que você comece com 24 operações simultâneas e, em seguida, altere essa configuração conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="fbad1-116">As previous explained, we recommend that you start with 24 concurrent operations, and then change this setting as appropriate.</span></span>
    
3. <span data-ttu-id="fbad1-117">No Windows Explorer, clique ou clique duas vezes no arquivo. reg que você criou na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="fbad1-117">In Windows Explorer, click or double-click the .reg file that you created in the previous step.</span></span>
    
4. <span data-ttu-id="fbad1-118">Na janela controle de acesso do usuário, clique em **Sim** para permitir que o editor do Registro faça a alteração.</span><span class="sxs-lookup"><span data-stu-id="fbad1-118">In the User Access Control window, click **Yes** to let the Registry Editor make the change.</span></span> 
    
5. <span data-ttu-id="fbad1-119">Quando for solicitado a continuar, clique em **Sim**.</span><span class="sxs-lookup"><span data-stu-id="fbad1-119">When prompted to continue, click **Yes**.</span></span>
    
    <span data-ttu-id="fbad1-120">O editor do registro exibe uma mensagem dizendo que a configuração foi adicionada com êxito ao registro.</span><span class="sxs-lookup"><span data-stu-id="fbad1-120">The Registry Editor displays a message saying that the setting was successfully added to the registry.</span></span>
    
6. <span data-ttu-id="fbad1-121">Você pode repetir as etapas 2-5 para alterar o valor da `DownloadConcurrency` configuração do registro.</span><span class="sxs-lookup"><span data-stu-id="fbad1-121">You can repeat steps 2 - 5 to change the value for the  `DownloadConcurrency` registry setting.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="fbad1-p103">Após criar ou alterar a `DownloadConcurrency` configuração do registro, certifique-se de criar um novo trabalho de exportação ou reinicie um trabalho de exportação existente para os resultados de pesquisa ou os dados que você deseja baixar. Consulte a seção [mais informações](increase-download-speeds-when-exporting-ediscovery-results.md#moreinfo) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="fbad1-p103">After you create or change the  `DownloadConcurrency` registry setting, be sure to create a new export job or restart an existing export job for the search results or data that you want to download. See the [More information](increase-download-speeds-when-exporting-ediscovery-results.md#moreinfo) section for more details.</span></span> 
  
## <a name="more-information"></a><span data-ttu-id="fbad1-124">Mais informações</span><span class="sxs-lookup"><span data-stu-id="fbad1-124">More information</span></span>

- <span data-ttu-id="fbad1-p104">Uma nova chave de registro é criada na primeira vez que você executa o arquivo. reg que você criou neste procedimento. Em seguida `DownloadConcurrency` , a configuração do registro será editada sempre que você alterar e executar novamente o arquivo. reg Edit.</span><span class="sxs-lookup"><span data-stu-id="fbad1-p104">A new registry key is created the first time you run the .reg file that you created in this procedure. Then the  `DownloadConcurrency` registry setting is edited each time you change and re-run the .reg edit file.</span></span> 
    
- <span data-ttu-id="fbad1-p105">A ferramenta de exportação de descoberta eletrônica do Office 365 usa o [utilitário AzCopy do Azure](https://go.microsoft.com/fwlink/?linkid=849949) para baixar &amp; dados de pesquisa do centro de conformidade de segurança ou da descoberta eletrônica avançada. Definir a `DownloadConcurrency` configuração do registro é semelhante a usar o parâmetro **/NC** ao executar o utilitário AzCopy. Portanto, a configuração do `"DownloadConcurrency=24"` registro de teria o mesmo efeito que usar o valor do `/NC:24` parâmetro de com o utilitário AzCopy.</span><span class="sxs-lookup"><span data-stu-id="fbad1-p105">The Office 365 eDiscovery Export tool uses the [Azure AzCopy utility](https://go.microsoft.com/fwlink/?linkid=849949) to download search data from the Security &amp; Compliance Center or from Advanced eDiscovery. Configuring the  `DownloadConcurrency` registry setting is similar to using the **/NC** parameter when running the AzCopy utility. So the registry setting of  `"DownloadConcurrency=24"` would have the same effect as using the parameter value of  `/NC:24` with the AzCopy utility.</span></span> 
    
- <span data-ttu-id="fbad1-p106">Se você interromper um download de exportação atualmente em andamento e reiniciá-lo (tentando baixar os resultados da pesquisa novamente), a ferramenta de exportação de descoberta eletrônica do Office 365 tentará continuar o mesmo download. Portanto, se você iniciar um download, interrompa-o e, em seguida `DownloadConcurrency` , altere a configuração do registro, o download provavelmente falhará se você reiniciá-lo (clicando em **baixar resultados**exportados). Isso ocorre porque a ferramenta de exportação tentará retomar o download anterior usando configurações que não são válidas, pois você alterou a configuração do registro.</span><span class="sxs-lookup"><span data-stu-id="fbad1-p106">If you stop an export download that's currently in progress and then restart it (by trying to download the search results again), the Office 365 eDiscovery Export tool will attempt to resume the same download. So, if you start a download, stop it, and then change the  `DownloadConcurrency` registry setting, the download will probably fail if you restart it (by clicking **Download exported results**). This is because the export tool will attempt to resume the previous download using settings that aren't valid because you changed the registry setting.</span></span>
    
    <span data-ttu-id="fbad1-p107">Portanto, depois de alterar a `DownloadConcurrency` configuração do registro, certifique-se de reiniciar o trabalho de exportação (clicando em **reiniciar exportação**) &amp; no centro de conformidade de segurança. Em seguida, você pode baixar os resultados exportados. Para obter mais informações sobre como exportar dados e resultados de pesquisa, consulte:</span><span class="sxs-lookup"><span data-stu-id="fbad1-p107">Therefore, after you change the  `DownloadConcurrency` registry setting, be sure to restart the export job (by clicking **Restart export**) in the Security &amp; Compliance Center. Then you can download the exported results. For more information about exporting search results and data, see:</span></span>
    
  - [<span data-ttu-id="fbad1-136">Exportar resultados de pesquisa de conteúdo do centro de &amp; conformidade de segurança do Office 365</span><span class="sxs-lookup"><span data-stu-id="fbad1-136">Export Content Search results from the Office 365 Security &amp; Compliance Center</span></span>](export-search-results.md)
    
  - [<span data-ttu-id="fbad1-137">Exportar resultados na Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="fbad1-137">Export results in Office 365 Advanced eDiscovery</span></span>](export-results-in-advanced-ediscovery.md)
    

---
title: Aumentar a velocidade de download ao exportar os resultados da pesquisa de descoberta eletrônica do Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/14/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c4c8f689-9d52-4e80-ae4b-1411ee9efc43
description: Saiba como configurar o registro do Windows para aumentar a taxa de transferência de dados ao fazer o download de resultados da pesquisa e pesquisa de dados a partir de segurança do Office 365 &amp; descoberta eletrônica do Centro de conformidade e avançadas do Office 365.
ms.openlocfilehash: 3f456f5ee0312d4d4d7b95f868520e6756a90fd1
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524714"
---
# <a name="increase-the-download-speed-when-exporting-ediscovery-search-results-from-office-365"></a><span data-ttu-id="6a4b5-103">Aumentar a velocidade de download ao exportar os resultados da pesquisa de descoberta eletrônica do Office 365</span><span class="sxs-lookup"><span data-stu-id="6a4b5-103">Increase the download speed when exporting eDiscovery search results from Office 365</span></span>

<span data-ttu-id="6a4b5-p101">Quando você usar a ferramenta de exportação de descoberta eletrônica do Office 365 para baixar os resultados de uma pesquisa de conteúdo no Office 365 Security &amp; dados Centro de conformidade ou fazer download de eDiscovery avançadas do Office 365, a ferramenta inicia um determinado número de exportação simultânea operações para baixar os dados em seu computador local. Por padrão, o número de operações simultâneas é definido como 8 vezes o número de núcleos no computador que você está usando para baixar os dados. Por exemplo, se você tiver um computador de núcleo duplo (ou seja, duas unidades de processamento central em um chip), o número padrão de operações de exportação simultâneas é 16. Para aumentar a taxa de transferência de transferência de dados e a velocidade do processo de download, você pode aumentar o número de operações simultâneas, definindo uma configuração de registro do Windows no computador que você pode usar para baixar os resultados da pesquisa. Para o processo de download de velocidade, recomendamos que você inicie com uma configuração de 24 operações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="6a4b5-p101">When you use the Office 365 eDiscovery Export tool to download the results of a Content Search in the Office 365 Security &amp; Compliance Center or download data from Office 365 Advanced eDiscovery, the tool starts a certain number of concurrent export operations to download the data to your local computer. By default, the number of concurrent operations is set to 8 times the number of cores in the computer you're using to download the data. For example, if you have a dual core computer (meaning two central processing units on one chip), the default number of concurrent export operations is 16. To increase the data transfer throughput and speed-up the download process, you can increase the number of concurrent operations by configuring a Windows Registry setting on the computer that you use to download the search results. To speed-up the download process, we recommend that you start with a setting of 24 concurrent operations.</span></span>
  
<span data-ttu-id="6a4b5-p102">Se você pode baixar os resultados da pesquisa através de uma rede de pouca largura de banda, aumentando a essa configuração pode ter um impacto negativo. Como alternativa, você poderá aumentar a configuração para mais de 24 operações simultâneas em uma rede de alta largura de banda (o número máximo de operações simultâneas é 512). Depois de configurar essa configuração de registro, você pode precisar alterá-lo para localizar o número ideal de operações simultâneas para seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="6a4b5-p102">If you download search results over a low-bandwidth network, increasing this setting might have a negative impact. Alternatively, you might be able to increase the setting to more than 24 concurrent operations in a high-bandwidth network (the maximum number of concurrent operations is 512). After you configure this registry setting, you might have to change it to find the optimal number of concurrent operations for your environment.</span></span>
  
## <a name="create-a-registry-setting-to-change-the-number-of-concurrent-operations-when-exporting-data"></a><span data-ttu-id="6a4b5-112">Criar uma configuração para alterar o número de operações simultâneas na exportação de dados de registro</span><span class="sxs-lookup"><span data-stu-id="6a4b5-112">Create a registry setting to change the number of concurrent operations when exporting data</span></span>

<span data-ttu-id="6a4b5-113">Execute o procedimento a seguir no computador que você usará para baixar os resultados da pesquisa a partir de segurança &amp; dados do eDiscovery avançado ou centro de conformidade.</span><span class="sxs-lookup"><span data-stu-id="6a4b5-113">Perform the following procedure on the computer that you'll use to download search results from the Security &amp; Compliance Center or data from Advanced eDiscovery.</span></span>
  
1. <span data-ttu-id="6a4b5-114">Feche a ferramenta de exportação de descoberta eletrônica do Office 365 se ele estiver aberto.</span><span class="sxs-lookup"><span data-stu-id="6a4b5-114">Close the Office 365 eDiscovery Export tool if it's open.</span></span> 
    
2. <span data-ttu-id="6a4b5-115">Salve o seguinte texto em um arquivo de registro da janela usando um sufixo de nome de arquivo de. reg; Por exemplo, ConcurrentOperations.reg.</span><span class="sxs-lookup"><span data-stu-id="6a4b5-115">Save the following text to a Window registry file by using a filename suffix of .reg; for example, ConcurrentOperations.reg.</span></span> 
    
    ```
    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool]
    "DownloadConcurrency"="24"
    ```

    <span data-ttu-id="6a4b5-116">Anterior conforme explicado, recomendamos que você inicie com 24 operações simultâneas e, em seguida, altere esta definição conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="6a4b5-116">As previous explained, we recommend that you start with 24 concurrent operations, and then change this setting as appropriate.</span></span>
    
3. <span data-ttu-id="6a4b5-117">No Windows Explorer, clique em ou duas vezes no arquivo. reg que você criou na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="6a4b5-117">In Windows Explorer, click or double-click the .reg file that you created in the previous step.</span></span>
    
4. <span data-ttu-id="6a4b5-118">Na janela de controle de acesso de usuário, clique em **Sim** para permitir que o Editor do registro faça a alteração.</span><span class="sxs-lookup"><span data-stu-id="6a4b5-118">In the User Access Control window, click **Yes** to let the Registry Editor make the change.</span></span> 
    
5. <span data-ttu-id="6a4b5-119">Quando solicitado a continuar, clique em **Sim**.</span><span class="sxs-lookup"><span data-stu-id="6a4b5-119">When prompted to continue, click **Yes**.</span></span>
    
    <span data-ttu-id="6a4b5-120">O Editor do registro exibe uma mensagem informando que a configuração foi adicionada com êxito ao registro.</span><span class="sxs-lookup"><span data-stu-id="6a4b5-120">The Registry Editor displays a message saying that the setting was successfully added to the registry.</span></span>
    
6. <span data-ttu-id="6a4b5-121">Você pode repetir as etapas 2 a 5 para alterar o valor para o `DownloadConcurrency` configuração do registro.</span><span class="sxs-lookup"><span data-stu-id="6a4b5-121">You can repeat steps 2 - 5 to change the value for the  `DownloadConcurrency` registry setting.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="6a4b5-p103">Depois que você criar ou alterar o `DownloadConcurrency` registro de configuração, certifique-se criar um novo trabalho de exportação ou reiniciar um trabalho de exportação existente para os resultados de pesquisa ou os dados que você deseja baixar. Consulte a seção de [informações adicionais](increase-download-speeds-when-exporting-ediscovery-results.md#moreinfo) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="6a4b5-p103">After you create or change the  `DownloadConcurrency` registry setting, be sure to create a new export job or restart an existing export job for the search results or data that you want to download. See the [More information](increase-download-speeds-when-exporting-ediscovery-results.md#moreinfo) section for more details.</span></span> 
  
## <a name="more-information"></a><span data-ttu-id="6a4b5-124">Mais informações</span><span class="sxs-lookup"><span data-stu-id="6a4b5-124">More information</span></span>

- <span data-ttu-id="6a4b5-p104">Uma nova chave de registro é criada na primeira vez que você executar o arquivo. reg que você criou neste procedimento. Em seguida, a `DownloadConcurrency` configuração do registro é editada sempre que você alterar e execute novamente o arquivo. reg editar.</span><span class="sxs-lookup"><span data-stu-id="6a4b5-p104">A new registry key is created the first time you run the .reg file that you created in this procedure. Then the  `DownloadConcurrency` registry setting is edited each time you change and re-run the .reg edit file.</span></span> 
    
- <span data-ttu-id="6a4b5-p105">A ferramenta de exportação de descoberta eletrônica do Office 365 usa o [utilitário AzCopy do Windows Azure](https://go.microsoft.com/fwlink/?linkid=849949) para baixar os dados de pesquisa a partir de segurança &amp; Centro de conformidade ou de descoberta eletrônica avançada. Configurando o `DownloadConcurrency` configuração do registro é semelhante a usar o parâmetro **/NC** ao executar o utilitário AzCopy. Então a configuração de registro de `"DownloadConcurrency=24"` teria o mesmo efeito que usar o valor do parâmetro da `/NC:24` com o utilitário AzCopy.</span><span class="sxs-lookup"><span data-stu-id="6a4b5-p105">The Office 365 eDiscovery Export tool uses the [Azure AzCopy utility](https://go.microsoft.com/fwlink/?linkid=849949) to download search data from the Security &amp; Compliance Center or from Advanced eDiscovery. Configuring the  `DownloadConcurrency` registry setting is similar to using the **/NC** parameter when running the AzCopy utility. So the registry setting of  `"DownloadConcurrency=24"` would have the same effect as using the parameter value of  `/NC:24` with the AzCopy utility.</span></span> 
    
- <span data-ttu-id="6a4b5-p106">Se você interromper um download de exportação em andamento e, em seguida, reiniciá-lo (por tentando baixar os resultados da pesquisa novamente), a ferramenta de exportação de descoberta eletrônica do Office 365 tentará reiniciar o download do mesmo. Assim, se você iniciar um download, pará-lo e, em seguida, alterar o `DownloadConcurrency` registro definição, o download provavelmente falhará se você reiniciá-lo (clicando **Download exportou resultados**). Isso ocorre porque a ferramenta de exportação tentará reiniciar o download anterior usando as configurações que não são válidas, pois você alterou a configuração do registro.</span><span class="sxs-lookup"><span data-stu-id="6a4b5-p106">If you stop an export download that's currently in progress and then restart it (by trying to download the search results again), the Office 365 eDiscovery Export tool will attempt to resume the same download. So, if you start a download, stop it, and then change the  `DownloadConcurrency` registry setting, the download will probably fail if you restart it (by clicking **Download exported results**). This is because the export tool will attempt to resume the previous download using settings that aren't valid because you changed the registry setting.</span></span>
    
    <span data-ttu-id="6a4b5-p107">Portanto, após você alterar o `DownloadConcurrency` registro configuração, certifique-se de reiniciar o trabalho de exportação (clicando **Reiniciar exportação**) na segurança &amp; Centro de conformidade. Em seguida, você pode baixar os resultados exportados. Para obter mais informações sobre como exportar dados e resultados de pesquisa, consulte:</span><span class="sxs-lookup"><span data-stu-id="6a4b5-p107">Therefore, after you change the  `DownloadConcurrency` registry setting, be sure to restart the export job (by clicking **Restart export**) in the Security &amp; Compliance Center. Then you can download the exported results. For more information about exporting search results and data, see:</span></span>
    
  - [<span data-ttu-id="6a4b5-136">Exportar resultados de pesquisa de conteúdo da segurança do Office 365 &amp; Centro de conformidade</span><span class="sxs-lookup"><span data-stu-id="6a4b5-136">Export Content Search results from the Office 365 Security &amp; Compliance Center</span></span>](export-search-results.md)
    
  - [<span data-ttu-id="6a4b5-137">Exportar resultados na Descoberta Eletrônica Avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="6a4b5-137">Export results in Office 365 Advanced eDiscovery</span></span>](export-results-in-advanced-ediscovery.md)
    

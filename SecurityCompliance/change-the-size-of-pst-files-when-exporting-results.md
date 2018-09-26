---
title: Alterar o tamanho dos arquivos PST ao exportar os resultados da pesquisa de descoberta eletrônica
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 11/30/2016
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 04e9de2d-765b-457b-a98a-d0f60bfb13f2
description: Você pode alterar o tamanho padrão dos arquivos PST que são dowloaded ao seu computador ao exportar os resultados da pesquisa de descoberta eletrônica.
ms.openlocfilehash: 1479db72117729d2e5cfa6feec1d9a0d9a60ffb5
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25037984"
---
# <a name="change-the-size-of-pst-files-when-exporting-ediscovery-search-results"></a><span data-ttu-id="9f6e0-103">Alterar o tamanho dos arquivos PST ao exportar os resultados da pesquisa de descoberta eletrônica</span><span class="sxs-lookup"><span data-stu-id="9f6e0-103">Change the size of PST files when exporting eDiscovery search results</span></span>

<span data-ttu-id="9f6e0-p101">Quando você usar a ferramenta de exportação de descoberta eletrônica do Office 365 para exportar os resultados de email de uma pesquisa de descoberta eletrônica das diferentes ferramentas de descoberta eletrônica da Microsoft, o tamanho padrão de um arquivo PST que pode ser exportado é 10 GB. Se você quiser alterar esse tamanho padrão, você pode editar o registro do Windows no computador que você usa para exportar os resultados da pesquisa. Um motivo para fazer isso é para que um arquivo PST pode caibam em mídia removível, tal um DVD, uma unidade USB ou um CD.</span><span class="sxs-lookup"><span data-stu-id="9f6e0-p101">When you use the Office 365 eDiscovery Export tool to export the email results of an eDiscovery search from the different Microsoft eDiscovery tools, the default size of a PST file that can be exported is 10 GB. If you want to change this default size, you can edit the Windows Registry on the computer that you use to export the search results. One reason to do this is so a PST file can fit on removable media, such a DVD, a compact disc, or a USB drive.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="9f6e0-107">A ferramenta de exportação de descoberta eletrônica do Office 365 é usada para exportar os resultados da pesquisa ao usar a pesquisa de conteúdo no Office 365 Security &amp; Centro de conformidade, In-Place eDiscovery no Exchange Online e o Centro de descoberta eletrônica no SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="9f6e0-107">The Office 365 eDiscovery Export tool is used to export the search results when using Content Search in the Office 365 Security &amp; Compliance Center, In-Place eDiscovery in Exchange Online, and the eDiscovery Center in SharePoint Online.</span></span> 
  
## <a name="create-a-registry-setting-to-change-the-size-of-pst-files-when-you-export-ediscovery-search-results"></a><span data-ttu-id="9f6e0-108">Criar uma configuração de registro para alterar o tamanho dos arquivos PST ao exportar os resultados da pesquisa de descoberta eletrônica</span><span class="sxs-lookup"><span data-stu-id="9f6e0-108">Create a registry setting to change the size of PST files when you export eDiscovery search results</span></span>

<span data-ttu-id="9f6e0-109">Execute o procedimento a seguir no computador que você usará para exportar os resultados de uma pesquisa de descoberta eletrônica.</span><span class="sxs-lookup"><span data-stu-id="9f6e0-109">Perform the following procedure on the computer that you'll use to export the results of an eDiscovery search.</span></span>
  
1. <span data-ttu-id="9f6e0-110">Feche a ferramenta de exportação de descoberta eletrônica do Office 365 se ele estiver aberto.</span><span class="sxs-lookup"><span data-stu-id="9f6e0-110">Close the Office 365 eDiscovery Export tool if it's open.</span></span> 
    
2. <span data-ttu-id="9f6e0-111">Salve o seguinte texto em um arquivo de registro da janela usando um sufixo de nome de arquivo de. reg; Por exemplo, PstExportSize.reg.</span><span class="sxs-lookup"><span data-stu-id="9f6e0-111">Save the following text to a Window registry file by using a filename suffix of .reg; for example, PstExportSize.reg.</span></span> 
    
    ```
    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool]
    "PstSizeLimitInBytes"="1073741824"
    ```

    <span data-ttu-id="9f6e0-p102">No exemplo acima, o `PstSizeLimitInBytes` valor for definido como 1.073.741.824 bytes ou aproximadamente 1 GB. Aqui estão alguns outros valores de amostra para o `PstSizeLimitInBytes` configuração.</span><span class="sxs-lookup"><span data-stu-id="9f6e0-p102">In the example above, the  `PstSizeLimitInBytes` value is set to 1,073,741,824 bytes or approximately 1 GB. Here are some other sample values for the  `PstSizeLimitInBytes` setting.</span></span> 
    
    |<span data-ttu-id="9f6e0-114">**Tamanho em GB (aproximadamente)**</span><span class="sxs-lookup"><span data-stu-id="9f6e0-114">**Size in GB (approx.)**</span></span>|<span data-ttu-id="9f6e0-115">**Tamanho em bytes**</span><span class="sxs-lookup"><span data-stu-id="9f6e0-115">**Size in bytes**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="9f6e0-116">.7 GB (700 MB)</span><span class="sxs-lookup"><span data-stu-id="9f6e0-116">.7 GB (700 MB)</span></span>  <br/> |<span data-ttu-id="9f6e0-117">751619277</span><span class="sxs-lookup"><span data-stu-id="9f6e0-117">751619277</span></span>  <br/> |
    |<span data-ttu-id="9f6e0-118">2 GB</span><span class="sxs-lookup"><span data-stu-id="9f6e0-118">2 GB</span></span>  <br/> |<span data-ttu-id="9f6e0-119">2147483648</span><span class="sxs-lookup"><span data-stu-id="9f6e0-119">2147483648</span></span>  <br/> |
    |<span data-ttu-id="9f6e0-120">4 GB</span><span class="sxs-lookup"><span data-stu-id="9f6e0-120">4 GB</span></span>  <br/> |<span data-ttu-id="9f6e0-121">4294967296</span><span class="sxs-lookup"><span data-stu-id="9f6e0-121">4294967296</span></span>  <br/> |
    |<span data-ttu-id="9f6e0-122">8 GB</span><span class="sxs-lookup"><span data-stu-id="9f6e0-122">8 GB</span></span>  <br/> |<span data-ttu-id="9f6e0-123">8589934592</span><span class="sxs-lookup"><span data-stu-id="9f6e0-123">8589934592</span></span>  <br/> |
   
3. <span data-ttu-id="9f6e0-124">Alterar o `PstSizeLimitInBytes` valor ao tamanho máximo de um arquivo PST ao exportar os resultados da pesquisa e salve o arquivo desejado.</span><span class="sxs-lookup"><span data-stu-id="9f6e0-124">Change the `PstSizeLimitInBytes` value to the desired maximum size of a PST file when you export search results, and then save the file.</span></span> 
    
4. <span data-ttu-id="9f6e0-125">No Windows Explorer, clique em ou duas vezes no arquivo. reg que você criou nas etapas anteriores.</span><span class="sxs-lookup"><span data-stu-id="9f6e0-125">In Windows Explorer, click or double-click the .reg file that you created in the previous steps.</span></span>
    
5. <span data-ttu-id="9f6e0-126">Na janela de controle de acesso de usuário, clique em **Sim** para permitir que o Editor do registro faça a alteração.</span><span class="sxs-lookup"><span data-stu-id="9f6e0-126">In the User Access Control window, click **Yes** to let the Registry Editor make the change.</span></span> 
    
6. <span data-ttu-id="9f6e0-127">Quando solicitado a continuar, clique em **Sim**.</span><span class="sxs-lookup"><span data-stu-id="9f6e0-127">When prompted to continue, click **Yes**.</span></span>
    
    <span data-ttu-id="9f6e0-128">O Editor do registro exibe uma mensagem informando que a configuração foi adicionada com êxito ao registro.</span><span class="sxs-lookup"><span data-stu-id="9f6e0-128">The Registry Editor displays a message saying that the setting was successfully added to the registry.</span></span>
    
7. <span data-ttu-id="9f6e0-129">Você pode repetir as etapas 3 a 6 para alterar o valor para o `PstSizeLimitInBytes` configuração do registro.</span><span class="sxs-lookup"><span data-stu-id="9f6e0-129">You can repeat steps 3 - 6 to change the value for the  `PstSizeLimitInBytes` registry setting.</span></span> 
  
## <a name="frequently-asked-questions-about-changing-the-default-size-of-pst-files-when-you-export-ediscovery-search-results"></a><span data-ttu-id="9f6e0-130">Perguntas frequentes sobre como alterar o tamanho padrão dos arquivos PST ao exportar os resultados da pesquisa de descoberta eletrônica</span><span class="sxs-lookup"><span data-stu-id="9f6e0-130">Frequently asked questions about changing the default size of PST files when you export eDiscovery search results</span></span>

 <span data-ttu-id="9f6e0-131">**Por que é o padrão de tamanho de 10 GB?**</span><span class="sxs-lookup"><span data-stu-id="9f6e0-131">**Why is the default size 10 GB?**</span></span>
  
<span data-ttu-id="9f6e0-132">O tamanho padrão de 10 GB foi com base nos comentários do cliente; 10 GB é um bom equilíbrio entre a quantidade ideal de conteúdo em um único PST e com uma mínima chance de corrupção de arquivo.</span><span class="sxs-lookup"><span data-stu-id="9f6e0-132">The default size of 10 GB was based on customer feedback; 10 GB is a good balance between the optimal amount of content in a single PST and with a minimum chance of file corruption.</span></span>
  
 <span data-ttu-id="9f6e0-133">**Deve aumentar ou diminuir o tamanho padrão dos arquivos PST?**</span><span class="sxs-lookup"><span data-stu-id="9f6e0-133">**Should I increase or decrease the default size of PST files?**</span></span>
  
<span data-ttu-id="9f6e0-p103">Os clientes tendem a diminuir o limite de tamanho, para que os resultados da pesquisa irá caber em mídia removível que eles podem enviar fisicamente outros locais em suas organizações. Não recomendamos que você aumentar o tamanho padrão porque os arquivos maior do que 10 GB podem ter problemas de corrupção de PST.</span><span class="sxs-lookup"><span data-stu-id="9f6e0-p103">Customers tend to decrease the size limit so that the search results will fit on removable media that they can physically ship other locations in their organization. We don't recommend that you increase the default size because PST files larger than 10 GB might have corruption issues.</span></span>
  
 <span data-ttu-id="9f6e0-136">**Computador em que é necessário fazer isso em?**</span><span class="sxs-lookup"><span data-stu-id="9f6e0-136">**What computer do I have to do this on?**</span></span>
  
<span data-ttu-id="9f6e0-137">Você precisará alterar a configuração de registro em qualquer computador local que você execute a ferramenta de exportação de descoberta eletrônica do Office 365 em.</span><span class="sxs-lookup"><span data-stu-id="9f6e0-137">You need to change the registry setting on any local computer that you run the Office 365 eDiscovery Export tool on.</span></span>
  
 <span data-ttu-id="9f6e0-138">**Após alterar essa configuração, preciso reinicializar o computador?**</span><span class="sxs-lookup"><span data-stu-id="9f6e0-138">**After I change this setting, do I have to reboot the computer?**</span></span>
  
<span data-ttu-id="9f6e0-p104">Não, você não precisa reinicializar o computador. Mas, se estiver executando a ferramenta de exportação de descoberta eletrônica do Office 365, você terá que fechá-lo e o reinício-lo depois que você alterar essa configuração.</span><span class="sxs-lookup"><span data-stu-id="9f6e0-p104">No, you don't have to reboot the computer. But, if the Office 365 eDiscovery Export tool is running, you'll have to close it and the restart it after you change this setting.</span></span>
  
 <span data-ttu-id="9f6e0-141">**Uma chave do registro existente fazer editada ou fazer uma nova chave criada?**</span><span class="sxs-lookup"><span data-stu-id="9f6e0-141">**Does an existing registry key get edited or does a new key get created?**</span></span>
  
<span data-ttu-id="9f6e0-p105">Uma nova chave de registro é criada na primeira vez que você executar o arquivo. reg que você criou neste procedimento. Em seguida, a configuração é editada sempre que você alterar e execute novamente o arquivo. reg editar.</span><span class="sxs-lookup"><span data-stu-id="9f6e0-p105">A new registry key is created the first time you run the .reg file that you created in this procedure. Then the setting is edited each time you change and re-run the .reg edit file.</span></span>

---
title: Exclusão de dados Online do Office 365 SharePoint
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: Obter uma explicação sobre a exclusão de dados no SharePoint Online.
ms.openlocfilehash: 8a84859ce170a4c3ca713c751aef2b6d5b911c55
ms.sourcegitcommit: 29ba4c36af8e90ddc8d885863ef25bac2cffbe94
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/22/2018
ms.locfileid: "27411157"
---
# <a name="sharepoint-online-data-deletion-in-office-365"></a><span data-ttu-id="05ac3-103">Exclusão de dados Online do SharePoint no Office 365</span><span class="sxs-lookup"><span data-stu-id="05ac3-103">SharePoint Online Data Deletion in Office 365</span></span>

<span data-ttu-id="05ac3-p101">SharePoint Online armazena objetos como código abstrata dentro de bancos de dados de aplicativo. Quando um usuário carrega um arquivo para o SharePoint Online, esse arquivo é desmontado e traduzido em código do aplicativo e armazenado em várias tabelas entre vários bancos de dados. No SharePoint Online, todo o conteúdo que carrega um cliente é dividido em partes, criptografadas (potencialmente com várias chaves de AES 256 bits) e distribuído no datacenter. Para obter detalhes específicos sobre o processo de criptografia e agrupamento, consulte [criptografia em nuvem da Microsoft](office-365-encryption-in-the-microsoft-cloud-overview.md).</span><span class="sxs-lookup"><span data-stu-id="05ac3-p101">SharePoint Online stores objects as abstracted code within application databases. When a user uploads a file to SharePoint Online, that file is disassembled and translated into application code and stored in multiple tables across multiple databases. In SharePoint Online, all content that a customer uploads is broken into chunks, encrypted (potentially with multiple AES 256-bit keys), and distributed across the datacenter. For specific details about the chunking and encryption process, see [Encryption in the Microsoft Cloud](office-365-encryption-in-the-microsoft-cloud-overview.md).</span></span> 

<span data-ttu-id="05ac3-p102">No SharePoint Online, os itens são mantidos por 93 dias desde o momento em que você pode excluí-los a partir de seu local original. Eles permanecem na Lixeira do site todo o tempo, a menos que alguém exclui-los a partir daí, ou esvazia que Lixeira. Nesse caso, os itens vá para o Lixeira, onde eles mantenha-se para o restante dos dias 93 do conjunto de sites. Para informações sobre como restaurar itens excluídos, consulte [restaurar itens da Lixeira de um site do SharePoint](https://support.office.com/en-us/article/6df466b6-55f2-4898-8d6e-c0dff851a0be#ID0EAADAAA=Online
) e [restaurar itens excluídos da Lixeira do conjunto de sites](https://support.office.com/article/5fa924ee-16d7-487b-9a0a-021b9062d14b). O tempo de retenção da Lixeira não é configurável no SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="05ac3-p102">In SharePoint Online, items are retained for 93 days from the time you delete them from their original location. They stay in the site Recycle Bin the entire time, unless someone deletes them from there or empties that Recycle Bin. In that case, the items go to the site collection Recycle Bin, where they stay for the remainder of the 93 days. For info about restoring deleted items, see [Restore items in the Recycle Bin of a SharePoint site](https://support.office.com/en-us/article/6df466b6-55f2-4898-8d6e-c0dff851a0be#ID0EAADAAA=Online
) and [Restore deleted items from the site collection recycle bin](https://support.office.com/article/5fa924ee-16d7-487b-9a0a-021b9062d14b). The Recycle Bin retention time is not configurable in SharePoint Online.</span></span>

<span data-ttu-id="05ac3-113">Quando você exclui um conjunto de sites, você também estiver excluindo a hierarquia dos sites na coleção e todo o conteúdo delas:</span><span class="sxs-lookup"><span data-stu-id="05ac3-113">When you delete a site collection, you're also deleting the hierarchy of sites in the collection, and all content within them:</span></span>
- <span data-ttu-id="05ac3-114">Documentos e bibliotecas de documentos</span><span class="sxs-lookup"><span data-stu-id="05ac3-114">Documents and document libraries</span></span>
- <span data-ttu-id="05ac3-115">Listas e dados de lista</span><span class="sxs-lookup"><span data-stu-id="05ac3-115">Lists and list data</span></span>
- <span data-ttu-id="05ac3-116">Definições de configuração de site</span><span class="sxs-lookup"><span data-stu-id="05ac3-116">Site configuration settings</span></span>
- <span data-ttu-id="05ac3-117">Informações de segurança e funções relacionadas para o site ou seus subsites</span><span class="sxs-lookup"><span data-stu-id="05ac3-117">Role and security information that is related to the site or its subsites</span></span>
- <span data-ttu-id="05ac3-118">Subsites das informações do site, seus conteúdos e usuário nível superior</span><span class="sxs-lookup"><span data-stu-id="05ac3-118">Subsites of the top-level website, their contents, and user information</span></span>

<span data-ttu-id="05ac3-119">Se você acidentalmente excluir um conjunto de sites, ele pode ser restaurado por um global ou SharePoint admin usando o Centro de administração do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="05ac3-119">If you accidentally delete a site collection, it can be restored by a global or SharePoint admin using the SharePoint admin center.</span></span> 

<span data-ttu-id="05ac3-p103">Disco rígido exclusão ocorre quando um usuário limpa os itens excluídos da Lixeira, do conjunto de sites quando os períodos de retenção e backup expirarem, ou quando um administrador exclui permanentemente um conjunto de sites usando o [cmdlet Remove-SPODeletedSite](/powershell/module/sharepoint-online/Remove-SPODeletedSite?view=sharepoint-ps). Quando o usuário rígido exclui (exclui permanentemente ou limpa) conteúdo do SharePoint Online, todas as chaves de criptografia para os blocos excluídos serão excluídas também. Os blocos nos discos que anteriormente armazenados os blocos excluídos são marcados como não utilizado e disponível para usar novamente.</span><span class="sxs-lookup"><span data-stu-id="05ac3-p103">Hard deletion occurs when a user purges deleted items from the site collection Recycle Bin, when the retention and backup periods expire, or when an administrator permanently deletes a site collection using the [Remove-SPODeletedSite cmdlet](/powershell/module/sharepoint-online/Remove-SPODeletedSite?view=sharepoint-ps). When a user hard deletes (permanently deletes, or purges) content from SharePoint Online, all encryption keys for the deleted chunks are also deleted. The blocks on the disks that previously stored the deleted chunks are marked as unused and available for re-use.</span></span>

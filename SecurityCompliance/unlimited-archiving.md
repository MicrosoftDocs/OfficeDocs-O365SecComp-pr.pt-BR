---
title: Visão geral do arquivamento ilimitado no Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 37cdbb02-a24a-4093-8bdb-2a7f0b3a19ee
description: Saiba mais sobre a expansão automática arquivamento no Office 365, que fornece armazenamento de arquivamento ilimitado para caixas de correio Exchange Online.
ms.openlocfilehash: 83eb49b3f2a7da418b61e509f44023809ed396c3
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29740813"
---
# <a name="overview-of-unlimited-archiving-in-office-365"></a><span data-ttu-id="7f049-103">Visão geral do arquivamento ilimitado no Office 365</span><span class="sxs-lookup"><span data-stu-id="7f049-103">Overview of unlimited archiving in Office 365</span></span>

<span data-ttu-id="7f049-p101">No Office 365, caixas de correio de arquivo morto oferecem aos usuários espaço de armazenamento de caixa de correio adicional. Depois de correio de arquivo morto de um usuário estiver habilitado, até 100 GB de armazenamento adicional está disponível. Quando a cota de armazenamento de 100 GB é atingida, as organizações tinham entrar em contato com a Microsoft para o espaço de armazenamento adicional de solicitação para uma caixa de correio de arquivo morto. Não há mais, que é o caso. O novo recurso de arquivamento ilimitado no Office 365 (chamados de *expansão automática arquivamento*) fornece uma quantidade ilimitada de armazenamento em caixas de correio de arquivo morto. Agora, quando a cota de armazenamento na caixa de correio de arquivo morto é atingida, o Office 365 aumenta automaticamente o tamanho do arquivamento, que significa que os usuários não serão executados sem espaço de armazenamento de caixa de correio e os administradores não devem solicitar o armazenamento adicional para caixas de correio de arquivo morto .</span><span class="sxs-lookup"><span data-stu-id="7f049-p101">In Office 365, archive mailboxes provide users with additional mailbox storage space. After a user's archive mailbox is enabled, up to 100 GB of additional storage is available. When the 100 GB storage quota is reached, organizations had to contact Microsoft to request additional storage space for an archive mailbox. That's no longer the case. The new unlimited archiving feature in Office 365 (called *auto-expanding archiving*) provides an unlimited amount of storage in archive mailboxes. Now, when the storage quota in the archive mailbox is reached, Office 365 automatically increases the size of the archive, which means that users won't run out of mailbox storage space and administrators won't have to request additional storage for archive mailboxes.</span></span>
  
<span data-ttu-id="7f049-110">Para obter instruções passo a passo para ativem expansão automática arquivamento, consulte [Habilitar o arquivamento ilimitado no Office 365](enable-unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="7f049-110">For step-by-step instructions for turning on auto-expanding archiving, see [Enable unlimited archiving in Office 365](enable-unlimited-archiving.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="7f049-p102">Expansão automática arquivamento também oferece suporte a caixas de correio compartilhadas. Para habilitar o arquivamento para uma caixa de correio compartilhada, é necessária uma licença do Exchange Online plano 2 ou uma licença do Exchange Online plano 1 com uma licença de arquivamento do Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="7f049-p102">Auto-expanding archiving also supports shared mailboxes. To enable the archive for a shared mailbox, an Exchange Online Plan 2 license or an Exchange Online Plan 1 license with an Exchange Online Archiving license is required.</span></span> 
  
## <a name="how-auto-expanding-archiving-works"></a><span data-ttu-id="7f049-113">Como expansão automática arquivamento funciona</span><span class="sxs-lookup"><span data-stu-id="7f049-113">How auto-expanding archiving works</span></span>

<span data-ttu-id="7f049-p103">Como explicada anteriormente, adicional para caixa de correio espaço de armazenamento é criado quando o correio de arquivo morto de um usuário está habilitado. Quando o arquivamento de expansão automática estiver habilitada, o Office 365 verifica periodicamente o tamanho da caixa de correio de arquivo morto. Quando uma caixa de correio de arquivo morto obtém e está perto do limite de armazenamento, o Office 365 cria automaticamente o espaço de armazenamento adicional para o arquivo morto. Se o usuário executa sem esse espaço de armazenamento adicional, o Office 365 adiciona mais espaço de armazenamento para o arquivo do usuário. Esse processo ocorre automaticamente, o que significa que os administradores não devem solicitar o armazenamento de arquivo morto adicionais ou gerenciar o arquivamento de expansão automática.</span><span class="sxs-lookup"><span data-stu-id="7f049-p103">As previously explained, additional mailbox storage space is created when a user's archive mailbox is enabled. When auto-expanding archiving is enabled, Office 365 periodically checks the size of the archive mailbox. When an archive mailbox gets close to its storage limit, Office 365 automatically creates additional storage space for the archive. If the user runs out of this additional storage space, Office 365 adds more storage space to the user's archive. This process happens automatically, which means administrators don't have to request additional archive storage or manage auto-expanding archiving.</span></span> 
  
<span data-ttu-id="7f049-119">Eis uma rápida visão geral do processo.</span><span class="sxs-lookup"><span data-stu-id="7f049-119">Here's a quick overview of the process.</span></span>
  
![Visão geral do processo de arquivamento expansão automática](media/74355385-d990-44fe-8a87-6c3639d1f63f.png)
  
1. <span data-ttu-id="7f049-p104">Arquivamento está habilitado para uma caixa de correio do usuário ou uma caixa de correio compartilhada. Uma caixa de correio de arquivamento com 100 GB de espaço de armazenamento é criada e a cota de aviso para a caixa de correio de arquivo morto estiver definida como 90 GB.</span><span class="sxs-lookup"><span data-stu-id="7f049-p104">Archiving is enabled for a user mailbox or a shared mailbox. An archive mailbox with 100 GB of storage space is created, and the warning quota for the archive mailbox is set to 90 GB.</span></span>
    
2. <span data-ttu-id="7f049-p105">Um administrador permite a expansão automática arquivamento da caixa de correio. Em seguida, quando a caixa de correio de arquivo morto (incluindo a pasta itens recuperáveis) atinge 90 GB, ele é convertido em um arquivo morto expansão automática e Office 365 adiciona espaço de armazenamento para o arquivo morto. Observe que pode demorar até 30 dias para o espaço de armazenamento adicional a ser provisionado.</span><span class="sxs-lookup"><span data-stu-id="7f049-p105">An administrator enables auto-expanding archiving for the mailbox. Then, when the archive mailbox (including the Recoverable Items folder) reaches 90 GB, it's converted to an auto-expanding archive, and Office 365 adds storage space to the archive. Note that it can take up to 30 days for the additional storage space to be provisioned.</span></span>
    
3. <span data-ttu-id="7f049-126">O Office 365 adiciona automaticamente mais espaço de armazenamento para o arquivo morto quando necessário.</span><span class="sxs-lookup"><span data-stu-id="7f049-126">Office 365 automatically adds more storage space to the archive when necessary.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="7f049-p106">Se uma caixa de correio é colocada em espera ou atribuída a uma política de retenção do Office 365, a cota de armazenamento para o arquivamento de maibox é aumentada para 110 GB quando o arquivamento de expansão automática está habilitada. Da mesma forma, a cota de aviso de arquivo morto é aumentada para 100 GB.</span><span class="sxs-lookup"><span data-stu-id="7f049-p106">If a mailbox is placed on hold or assigned to an Office 365 retention policy, the storage quota for the archive maibox is increased to 110 GB when auto-expanding archiving is enabled. Similarly, the archive warning quota is increased to 100 GB.</span></span>

## <a name="what-gets-moved-to-the-additional-archive-storage-space"></a><span data-ttu-id="7f049-129">O que foi movido para o espaço de armazenamento de arquivo morto adicionais?</span><span class="sxs-lookup"><span data-stu-id="7f049-129">What gets moved to the additional archive storage space?</span></span>

<span data-ttu-id="7f049-p107">Para fazer um uso eficiente do armazenamento de arquivo morto de expansão automática, pastas podem obter movidas. O Office 365 determina quais pastas são movidas quando armazenamento adicional é adicionado para o arquivo morto. Quando uma pasta é movida, uma subpasta é criada automaticamente sob a pasta original na parte de arquivo morto da lista de pastas no Outlook. Essa nova subpasta aponta para os itens que foram movidos. A convenção de nomenclatura que usa Office 365 para nomear essa pasta é \*\* \<nome da pasta\>_yyyy (criados na mmm dd, yyyy h_mm)\*\*, onde:</span><span class="sxs-lookup"><span data-stu-id="7f049-p107">To make efficient use of auto-expanding archive storage, folders might get moved. Office 365 determines which folders get moved when additional storage is added to the archive. When a folder is moved, a subfolder is automatically created under the original folder in the archive portion of the folder list in Outlook. This new subfolder points to the items that were moved. The naming convention that Office 365 uses to name this folder is **\<folder name\>_yyyy (Created on mmm dd, yyyy h_mm)**, where:</span></span> 
  
- <span data-ttu-id="7f049-135">**AAAA** é o ano que as mensagens na pasta foram recebidas.</span><span class="sxs-lookup"><span data-stu-id="7f049-135">**yyyy** is the year the messages in the folder were received.</span></span> 
    
- <span data-ttu-id="7f049-136">**mmm dd, yyyy h_m** é a data e hora em que a subpasta foi criada pelo Office 365, no formato UTC, com base no fuso horário do usuário e as configurações regionais no Outlook.</span><span class="sxs-lookup"><span data-stu-id="7f049-136">**mmm dd, yyyy h_m** is the date and time that the subfolder was created by Office 365, in UTC format, based on the user's time zone and regional settings in Outlook.</span></span> 
    
<span data-ttu-id="7f049-137">As capturas de tela a seguir mostram uma lista de pasta antes e depois que as mensagens são movidas em um arquivo morto expandido para automático.</span><span class="sxs-lookup"><span data-stu-id="7f049-137">The following screen shots show a folder list before and after messages are moved in an auto-expanded archive.</span></span>
  
 <span data-ttu-id="7f049-138">**Antes de é adicionado a armazenamento adicional**</span><span class="sxs-lookup"><span data-stu-id="7f049-138">**Before additional storage is added**</span></span>
  
![Lista de pastas da caixa de correio de arquivamento antes de arquivo morto de expansão automática está provisionado](media/5d6d6420-e562-4912-aaab-1c111762b3f6.png)
  
 <span data-ttu-id="7f049-140">**Depois que o armazenamento adicional é adicionado**</span><span class="sxs-lookup"><span data-stu-id="7f049-140">**After additional storage is added**</span></span>
  
![Lista de pastas de correio de arquivo morto após a expansão automática de arquivamento é provisionado](media/c03c5f51-23fa-4fc2-b887-7e7e5cce30da.png)
  
## <a name="outlook-requirements-for-accessing-items-in-an-auto-expanded-archive"></a><span data-ttu-id="7f049-142">Requisitos do Outlook para acessar os itens em um arquivo morto autoexpandida</span><span class="sxs-lookup"><span data-stu-id="7f049-142">Outlook requirements for accessing items in an auto-expanded archive</span></span>

<span data-ttu-id="7f049-143">Para acessar as mensagens que são armazenadas em um arquivo morto expandido para automático, os usuários precisam usar um dos seguintes clientes do Outlook:</span><span class="sxs-lookup"><span data-stu-id="7f049-143">To access messages that are stored in an auto-expanded archive, users have to use one of the following Outlook clients:</span></span>
  
- <span data-ttu-id="7f049-144">Outlook 2016 ou 2019 do Outlook para Windows</span><span class="sxs-lookup"><span data-stu-id="7f049-144">Outlook 2016 or Outlook 2019 for Windows</span></span>
    
- <span data-ttu-id="7f049-145">Outlook na Web</span><span class="sxs-lookup"><span data-stu-id="7f049-145">Outlook on the web</span></span> 
    
- <span data-ttu-id="7f049-146">Outlook 2016 ou 2019 do Outlook para Mac</span><span class="sxs-lookup"><span data-stu-id="7f049-146">Outlook 2016 or Outlook 2019 for Mac</span></span> 
    
> [!NOTE]
> <span data-ttu-id="7f049-p108">Usuários do Outlook 2013 podem acessar apenas os itens que estavam originalmente armazenados em suas caixas de correio de arquivo morto. Eles não poderão acessar os itens que são movidos para o armazenamento de arquivamento adicionais.</span><span class="sxs-lookup"><span data-stu-id="7f049-p108">Outlook 2013 users can only access items that were originally stored in their archive mailbox. They won't be able to access items that are moved to additional archive storage.</span></span> 
  
<span data-ttu-id="7f049-149">Aqui estão algumas coisas a considerar ao usar o Outlook ou o Outlook na web para acessar mensagens armazenados em um arquivo morto expandido para automático.</span><span class="sxs-lookup"><span data-stu-id="7f049-149">Here are some things to consider when using Outlook or Outlook on the web to access messages stored in an auto-expanded archive.</span></span>
  
- <span data-ttu-id="7f049-150">Você pode acessar qualquer pasta na sua caixa de correio de arquivo morto, incluindo aquelas que foram movidos para a área de armazenamento de autoexpandida.</span><span class="sxs-lookup"><span data-stu-id="7f049-150">You can access any folder in your archive mailbox, including ones that were moved to the auto-expanded storage area.</span></span>
    
- <span data-ttu-id="7f049-p109">Você pode pesquisar para itens que foram movidos para uma área de armazenamento adicional pesquisando na pasta propriamente dita. Isso significa que você deve selecionar a pasta de arquivamento na lista de pastas para selecionar a opção de **Pasta atual** como o escopo da pesquisa. Da mesma forma, se uma pasta em uma área de armazenamento de autoexpandida contiver subpastas, você precisará pesquisar cada subpasta separadamente.</span><span class="sxs-lookup"><span data-stu-id="7f049-p109">You can search for items that were moved to an additional storage area only by searching the folder itself. This means you have to select the archive folder in the folder list to select the **Current Folder** option as the search scope. Similarly, if a folder in an auto-expanded storage area contains subfolders, you have to search each subfolder separately.</span></span> 
    
- <span data-ttu-id="7f049-154">Contagens de item do Outlook e contagens de leitura/não lida (no Outlook e Outlook na web) em um arquivo morto autoexpandida talvez não sejam precisas.</span><span class="sxs-lookup"><span data-stu-id="7f049-154">Item counts in Outlook and Read/Unread counts (in Outlook and Outlook on the web ) in an auto-expanded archive might not be accurate.</span></span>
    
- <span data-ttu-id="7f049-155">Você pode excluir itens em uma subpasta que aponta para uma área de armazenamento de autochave expandidas, mas na pasta propriamente dita não pode ser excluída.</span><span class="sxs-lookup"><span data-stu-id="7f049-155">You can delete items in a subfolder that points to an auto-expanded storage area, but the folder itself can't be deleted.</span></span>
    
- <span data-ttu-id="7f049-156">Você não pode usar o recurso de recuperar itens excluídos para recuperar um item que foi excluído de uma área de armazenamento de autoexpandida.</span><span class="sxs-lookup"><span data-stu-id="7f049-156">You can't use the Recover Deleted Items feature to recover an item that was deleted from an auto-expanded storage area.</span></span>
  
## <a name="auto-expanding-archiving-and-other-office-365-compliance-features"></a><span data-ttu-id="7f049-157">Expansão automática de arquivamento e outros recursos de conformidade do Office 365</span><span class="sxs-lookup"><span data-stu-id="7f049-157">Auto-expanding archiving and other Office 365 compliance features</span></span>

<span data-ttu-id="7f049-158">Esta seção explica a funcionalidade entre a expansão automática de arquivamento e outros conformidade do Office 365 e os recursos de governança de dados.</span><span class="sxs-lookup"><span data-stu-id="7f049-158">This section explains the functionality between auto-expanding archiving and other Office 365 compliance and data governance features.</span></span>
  
- <span data-ttu-id="7f049-159">**Descoberta eletrônica** - quando você usar uma ferramenta de descoberta eletrônica do Office 365, como pesquisa de conteúdo ou In-Place eDiscovery, as áreas de armazenamento adicional em um arquivo morto expandido para automático também são pesquisados.</span><span class="sxs-lookup"><span data-stu-id="7f049-159">**eDiscovery** - When you use an Office 365 eDiscovery tool, such as Content Search or In-Place eDiscovery, the additional storage areas in an auto-expanded archive are also searched.</span></span>
    
- <span data-ttu-id="7f049-160">**Retenção** - quando você colocar uma caixa de correio em espera usando ferramentas como litígio no Exchange Online ou eDiscovery caso retenções e políticas de retenção no & de segurança do Office 365 Centro de conformidade, o conteúdo localizadas em um arquivo morto expandido para automático é também colocada em espera.</span><span class="sxs-lookup"><span data-stu-id="7f049-160">**Retention** - When you put a mailbox on hold by using tools such as Litigation Hold in Exchange Online or eDiscovery case holds and retention policies in the Office 365 Security & Compliance Center, content located in an auto-expanded archive is also placed on hold.</span></span>
    
- <span data-ttu-id="7f049-161">**Mensagens (MRM) de gerenciamento de registros** - se você usar políticas de exclusão de MRM no Exchange Online para excluir permanentemente os itens expirados de caixa de correio, itens expirados localizados no arquivamento automático-expandida também serão excluídas.</span><span class="sxs-lookup"><span data-stu-id="7f049-161">**Messaging records management (MRM)** - If you use MRM deletion policies in Exchange Online to permanently delete expired mailbox items, expired items located in the auto-expanded archive will also be deleted.</span></span>
    
- <span data-ttu-id="7f049-p110">**Importar serviço** - você pode usar o serviço Office 365 importar para importar arquivos PST para o arquivo morto expandido para automático de um usuário. Você pode importar até 100 GB de dados de arquivos PST à caixa de correio de arquivo morto do usuário.</span><span class="sxs-lookup"><span data-stu-id="7f049-p110">**Import service** - You can use the Office 365 Import service to import PST files to a user's auto-expanded archive. You can import up to 100 GB of data from PST files to the user's archive mailbox.</span></span> 

## <a name="more-information"></a><span data-ttu-id="7f049-164">Mais informações</span><span class="sxs-lookup"><span data-stu-id="7f049-164">More information</span></span>

<span data-ttu-id="7f049-165">Para obter mais detalhes técnicos sobre expansão automática, arquivamento, consulte [Office 365: perguntas Frequentes expansão automática de arquivos mortos](https://blogs.technet.microsoft.com/exchange/2018/04/09/office-365-auto-expanding-archives-faq/).</span><span class="sxs-lookup"><span data-stu-id="7f049-165">For more technical details about auto-expanding archiving, see [Office 365: Auto-Expanding Archives FAQ](https://blogs.technet.microsoft.com/exchange/2018/04/09/office-365-auto-expanding-archives-faq/).</span></span>
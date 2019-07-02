---
title: Migrações de caixas de correio do Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Um breve resumo dos cmdlets usados para migrações de caixa de correio do Office 365.
ms.openlocfilehash: 3858af0c246cdef07164b6414a87cf110cf65055
ms.sourcegitcommit: aa60a6cdf83c67576e858668d1182cd4fffeb5e0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/06/2019
ms.locfileid: "33622421"
---
# <a name="office-365-mailbox-migrations"></a><span data-ttu-id="91e32-103">Migrações de caixas de correio do Office 365</span><span class="sxs-lookup"><span data-stu-id="91e32-103">Office 365 Mailbox Migrations</span></span>
<span data-ttu-id="91e32-104">Com uma implantação híbrida baseada no Exchange, os clientes podem optar por mover caixas de correio locais do Exchange para uma organização do [Exchange Online](https://docs.microsoft.com/Exchange/exchange-online) ou mover caixas de correio do Exchange Online para uma organização [local do Exchange](https://docs.microsoft.com/Exchange/exchange-server) .</span><span class="sxs-lookup"><span data-stu-id="91e32-104">With an Exchange-based hybrid deployment, customers can choose to either move on-premises Exchange mailboxes to an [Exchange Online](https://docs.microsoft.com/Exchange/exchange-online) organization or move Exchange Online mailboxes to an [Exchange on-premises](https://docs.microsoft.com/Exchange/exchange-server) organization.</span></span> <span data-ttu-id="91e32-105">Os lotes de migração são usados ao mover caixas de correio entre as organizações locais e do Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="91e32-105">Migration batches are used when moving mailboxes between on-premises and Exchange Online organizations.</span></span>

<span data-ttu-id="91e32-106">Os clientes podem rever as estatísticas e outras informações sobre as migrações de caixa de correio com os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="91e32-106">Customers can review statistics and other information about mailbox migrations with the following cmdlets:</span></span>

- <span data-ttu-id="91e32-107">[Get-MoveRequestStatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequestStatistics?view=exchange-ps): fornece estatísticas padrão para uma caixa de correio de usuário, que inclui o status, tamanho da caixa de correio, tamanho da caixa de correio de arquivo morto e porcentagem concluída.</span><span class="sxs-lookup"><span data-stu-id="91e32-107">[Get-MoveRequestStatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequestStatistics?view=exchange-ps): Provides default statistics for a user mailbox, which includes the status, mailbox size, archive mailbox size, and percentage complete.</span></span>
- <span data-ttu-id="91e32-108">[Get-Mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-Mailbox?view=exchange-ps
): fornece uma lista resumida de objetos e atributos de caixa de correio na organização.</span><span class="sxs-lookup"><span data-stu-id="91e32-108">[Get-Mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-Mailbox?view=exchange-ps
): Provides a summary list of mailbox objects and attributes in the organization.</span></span>
- <span data-ttu-id="91e32-109">[Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/Get-Recipient?view=exchange-ps): fornece uma lista de objetos habilitados para email existentes, como caixas de correio, usuários de email, contatos e grupos de distribuição.</span><span class="sxs-lookup"><span data-stu-id="91e32-109">[Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/Get-Recipient?view=exchange-ps): Provides a list of existing mail-enabled objects such as mailboxes, mail users, contacts, and distribution groups.</span></span>
- <span data-ttu-id="91e32-110">[Get-MoveRequest](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequest?view=exchange-ps): fornece um status detalhado de uma migração de caixa de correio em andamento.</span><span class="sxs-lookup"><span data-stu-id="91e32-110">[Get-MoveRequest](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequest?view=exchange-ps): Provides a detailed status of an ongoing mailbox migration.</span></span>
- <span data-ttu-id="91e32-111">[Get-MigrationUser](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUser?view=exchange-ps): fornece informações sobre os usuários de movimentação e migração de caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="91e32-111">[Get-MigrationUser](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUser?view=exchange-ps): Provides information about the mailbox move and migration users.</span></span>
- <span data-ttu-id="91e32-112">[Get-MigrationBatch](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationBatch?view=exchange-ps): fornece informações sobre o status do lote de migração atual.</span><span class="sxs-lookup"><span data-stu-id="91e32-112">[Get-MigrationBatch](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationBatch?view=exchange-ps): Provides information on the status of current migration batch.</span></span>
- <span data-ttu-id="91e32-113">[Get-MigrationUserStatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUserStatistics?view=exchange-ps): fornece informações detalhadas sobre o status de migração para um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="91e32-113">[Get-MigrationUserStatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUserStatistics?view=exchange-ps): Provides detailed information about the migration status for a specific user.</span></span>
- <span data-ttu-id="91e32-114">[Get-MailboxStatistics](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-MailboxStatistics?view=exchange-ps): fornece informações sobre caixas de correio, como tamanho, o número de mensagens e a hora do último acesso.</span><span class="sxs-lookup"><span data-stu-id="91e32-114">[Get-MailboxStatistics](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-MailboxStatistics?view=exchange-ps): Provides information about mailboxes, such as size, the number of messages, and the last accessed time.</span></span>

<span data-ttu-id="91e32-115">Para obter mais informações sobre cmdlets, consulte os cmdlets de [movimentação e migração no Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="91e32-115">For more information about cmdlets, see [Move and Migration cmdlets in Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).</span></span>

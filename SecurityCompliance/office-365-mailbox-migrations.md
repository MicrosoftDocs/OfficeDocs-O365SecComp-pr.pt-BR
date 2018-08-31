---
title: Migrações de caixas de correio do Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: Um breve resumo dos cmdlets usados para migrações de caixa de correio do Office 365.
ms.openlocfilehash: 86896d956072b5c11e3b3292363bb32312ff1187
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524309"
---
# <a name="office-365-mailbox-migrations"></a><span data-ttu-id="80bfc-103">Migrações de caixas de correio do Office 365</span><span class="sxs-lookup"><span data-stu-id="80bfc-103">Office 365 Mailbox Migrations</span></span>
<span data-ttu-id="80bfc-p101">Com uma implantação híbrida baseada no Exchange, os clientes podem escolher mover caixas de correio do Exchange local para uma organização do [Exchange Online](https://docs.microsoft.com/Exchange/exchange-online) ou mover caixas de correio do Exchange Online para uma organização do [Exchange local](https://docs.microsoft.com/Exchange/exchange-server) . Lotes de migração são usados ao mover caixas de correio entre organizações Exchange Online e no local. Os clientes podem ler estatísticas e outras informações sobre migrações de caixa de correio usando os cmdlets a seguir:</span><span class="sxs-lookup"><span data-stu-id="80bfc-p101">With an Exchange-based hybrid deployment, customers can choose to either move on-premises Exchange mailboxes to an [Exchange Online](https://docs.microsoft.com/Exchange/exchange-online) organization or move Exchange Online mailboxes to an [Exchange on-premises](https://docs.microsoft.com/Exchange/exchange-server) organization. Migration batches are used when moving mailboxes between on-premises and Exchange Online organizations. Customers can review statistics and other information about mailbox migrations using the following cmdlets:</span></span>

- <span data-ttu-id="80bfc-107">[Get-MoveRequestStatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequestStatistics?view=exchange-ps) - fornece as estatísticas padrão de uma caixa de correio do usuário, que inclui o status, o tamanho da caixa de correio, arquivar o tamanho da caixa de correio e a porcentagem de conclusão.</span><span class="sxs-lookup"><span data-stu-id="80bfc-107">[Get-MoveRequestStatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequestStatistics?view=exchange-ps) - Provides default statistics for a user mailbox, which includes the status, mailbox size, archive mailbox size and percentage complete.</span></span>
- <span data-ttu-id="80bfc-108">[Get-Mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-Mailbox?view=exchange-ps
) - fornece uma lista resumida de objetos de caixa de correio e atributos na organização.</span><span class="sxs-lookup"><span data-stu-id="80bfc-108">[Get-Mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-Mailbox?view=exchange-ps
) - Provides a summary list of mailbox objects and attributes in the organization.</span></span>
- <span data-ttu-id="80bfc-109">[Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/Get-Recipient?view=exchange-ps) - fornece uma lista dos objetos existentes habilitados para email, como caixas de correio, usuários de email, contatos e grupos de distribuição.</span><span class="sxs-lookup"><span data-stu-id="80bfc-109">[Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/Get-Recipient?view=exchange-ps) - Provides a list of existing mail-enabled objects such as mailboxes, mail users, contacts and distribution groups.</span></span>
- <span data-ttu-id="80bfc-110">[Get-MoveRequest](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequest?view=exchange-ps) - fornece um status detalhado de uma migração de caixa de correio em andamento.</span><span class="sxs-lookup"><span data-stu-id="80bfc-110">[Get-MoveRequest](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequest?view=exchange-ps) - Provides a detailed status of an ongoing mailbox migration.</span></span>
- <span data-ttu-id="80bfc-111">[Get-MigrationUser](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUser?view=exchange-ps) - fornece informações sobre a caixa de correio movimentação e migração de usuários.</span><span class="sxs-lookup"><span data-stu-id="80bfc-111">[Get-MigrationUser](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUser?view=exchange-ps) - Provides information about the mailbox move and migration users.</span></span>
- <span data-ttu-id="80bfc-112">[Get-MigrationBatch](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationBatch?view=exchange-ps) - fornece informações sobre o status do lote de migração atual.</span><span class="sxs-lookup"><span data-stu-id="80bfc-112">[Get-MigrationBatch](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationBatch?view=exchange-ps) - Provides information on the status of current migration batch.</span></span>
- <span data-ttu-id="80bfc-113">[Get-MigrationUserStatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUserStatistics?view=exchange-ps) - fornece informações detalhadas sobre o status de migração para um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="80bfc-113">[Get-MigrationUserStatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUserStatistics?view=exchange-ps) - Provides detailed information about the migration status for a specific user.</span></span>
- <span data-ttu-id="80bfc-114">[Get-MailboxStatistics](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-MailboxStatistics?view=exchange-ps) - fornece informações sobre caixas de correio, como tamanho, o número de mensagens e a hora do último acesso.</span><span class="sxs-lookup"><span data-stu-id="80bfc-114">[Get-MailboxStatistics](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-MailboxStatistics?view=exchange-ps) - Provides information about mailboxes, such as size, the number of messages, and the last accessed time.</span></span>

<span data-ttu-id="80bfc-115">Para obter mais informações sobre os cmdlets adicionais, consulte [cmdlets de movimentação e migração no Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="80bfc-115">For more information on additional cmdlets, see [Move and Migration cmdlets in Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).</span></span>

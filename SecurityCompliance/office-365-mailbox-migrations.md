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
# <a name="office-365-mailbox-migrations"></a>Migrações de caixas de correio do Office 365
Com uma implantação híbrida baseada no Exchange, os clientes podem escolher mover caixas de correio do Exchange local para uma organização do [Exchange Online](https://docs.microsoft.com/Exchange/exchange-online) ou mover caixas de correio do Exchange Online para uma organização do [Exchange local](https://docs.microsoft.com/Exchange/exchange-server) . Lotes de migração são usados ao mover caixas de correio entre organizações Exchange Online e no local. Os clientes podem ler estatísticas e outras informações sobre migrações de caixa de correio usando os cmdlets a seguir:

- [Get-MoveRequestStatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequestStatistics?view=exchange-ps) - fornece as estatísticas padrão de uma caixa de correio do usuário, que inclui o status, o tamanho da caixa de correio, arquivar o tamanho da caixa de correio e a porcentagem de conclusão.
- [Get-Mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-Mailbox?view=exchange-ps
) - fornece uma lista resumida de objetos de caixa de correio e atributos na organização.
- [Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/Get-Recipient?view=exchange-ps) - fornece uma lista dos objetos existentes habilitados para email, como caixas de correio, usuários de email, contatos e grupos de distribuição.
- [Get-MoveRequest](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequest?view=exchange-ps) - fornece um status detalhado de uma migração de caixa de correio em andamento.
- [Get-MigrationUser](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUser?view=exchange-ps) - fornece informações sobre a caixa de correio movimentação e migração de usuários.
- [Get-MigrationBatch](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationBatch?view=exchange-ps) - fornece informações sobre o status do lote de migração atual.
- [Get-MigrationUserStatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUserStatistics?view=exchange-ps) - fornece informações detalhadas sobre o status de migração para um usuário específico.
- [Get-MailboxStatistics](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-MailboxStatistics?view=exchange-ps) - fornece informações sobre caixas de correio, como tamanho, o número de mensagens e a hora do último acesso.

Para obter mais informações sobre os cmdlets adicionais, consulte [cmdlets de movimentação e migração no Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).

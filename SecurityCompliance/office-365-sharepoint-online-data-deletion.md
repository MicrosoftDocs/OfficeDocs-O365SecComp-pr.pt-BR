---
title: Exclusão de dados Online do Office 365 SharePoint
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
description: Obter uma explicação sobre a exclusão de dados no SharePoint Online.
ms.openlocfilehash: c281f6de9cd9e4978ac4a6997333d71d8835420f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523652"
---
# <a name="sharepoint-online-data-deletion-in-office-365"></a>Exclusão de dados Online do SharePoint no Office 365

SharePoint Online armazena objetos como código abstrata dentro de bancos de dados de aplicativo. Quando um usuário carrega um arquivo para o SharePoint Online, esse arquivo é desmontado e traduzido em código do aplicativo e armazenado em várias tabelas entre vários bancos de dados. No SharePoint Online, todo o conteúdo que carrega um cliente é dividido em partes, criptografadas (potencialmente com várias chaves de AES 256 bits) e distribuído no datacenter. Para obter detalhes específicos sobre o processo de criptografia e agrupamento, consulte [criptografia em nuvem da Microsoft](office-365-encryption-in-the-microsoft-cloud-overview.md). São fornecidos serviços de proteção de dados para evitar a perda de dados do SharePoint Online. Especificamente, os backups são executados a cada 12 horas e mantidos para 14 dias.

Quando você exclui o conteúdo de um site do SharePoint Online, ele não é excluído imediatamente. Ele é enviado a um Site Recycle Bin, onde ele possa ser restaurado, se necessário. (Consulte [restaurar itens excluídos da Lixeira do conjunto de sites](https://support.office.com/article/Restore-deleted-items-from-the-site-collection-recycle-bin-5fa924ee-16d7-487b-9a0a-021b9062d14b) para as etapas de restauração). O tempo de retenção de Lixeira do Site padrão é de cerca de 90 dias. Se você excluir o conteúdo de um Site Recycle Bin, ele é enviado para o Site Lixeira do conjunto, que tem um tempo de retenção de 30 dias. O período de tempo para manter as coisas na Lixeira pode ser configurado por um administrador, mas na ausência dessa, o período de retenção padrão é de cerca de 90 dias. O armazenamento do site recycle bin conta contra o [Limite de exibição de lista](https://support.office.com/article/List-View-Threshold-b8588dae-9387-48c2-9248-c24122f07c59)e de cota de armazenamento do conjunto de sites.

Quando você exclui um conjunto de sites, você também estiver excluindo a hierarquia dos sites na coleção, incluindo todas as informações de conteúdo e de usuário:
- Documentos e bibliotecas de documentos
- Listas e dados de lista
- Definições de configuração de site
- Informações de segurança e funções relacionadas para o site ou seus subsites
- Subsites das informações do site, seus conteúdos e usuário nível superior

Antes de excluir um conjunto de sites, é recomendável que você revise a descrição do serviço SharePoint Online para o seu plano, que descreve a agenda de backup de dados mantida pela Microsoft para sites do SharePoint Online. Também Observe que podem restaurações de backups são apenas para conjuntos de sites ou subsites, não para arquivos, listas ou bibliotecas. Se você precisar recuperar aqueles, uso da Lixeira.

Se você acidentalmente excluir um conjunto de sites, ele pode ser restaurado da Site coleção Lixeira por um administrador de conjunto de sites dentro de 30 dias. Se precisar de um conjunto de sites restaurado após 30 dias, ele pode ser restaurado pela Microsoft em 14 dias entre a expiração de 30 dias contatando a Microsoft por meio de uma solicitação de serviço.

Disco rígido exclusão ocorre quando um usuário limpa os itens excluídos do Site Recycle Bin, e a retenção e os períodos de backup expiram, ou quando um administrador exclui permanentemente um conjunto de sites usando o [cmdlet Remove-SPODeletedSite](https://docs.microsoft.com/powershell/module/sharepoint-online/Remove-SPODeletedSite?view=sharepoint-ps). Quando o usuário rígido exclui (exclui permanentemente ou limpa) conteúdo do SharePoint Online, todas as chaves de criptografia para os blocos excluídos serão excluídas também. Os blocos nos discos que anteriormente armazenados os blocos excluídos são marcados como não utilizado e disponível para usar novamente.

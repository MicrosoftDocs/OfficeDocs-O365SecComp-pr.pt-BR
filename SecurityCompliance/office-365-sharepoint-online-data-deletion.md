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
# <a name="sharepoint-online-data-deletion-in-office-365"></a>Exclusão de dados Online do SharePoint no Office 365

SharePoint Online armazena objetos como código abstrata dentro de bancos de dados de aplicativo. Quando um usuário carrega um arquivo para o SharePoint Online, esse arquivo é desmontado e traduzido em código do aplicativo e armazenado em várias tabelas entre vários bancos de dados. No SharePoint Online, todo o conteúdo que carrega um cliente é dividido em partes, criptografadas (potencialmente com várias chaves de AES 256 bits) e distribuído no datacenter. Para obter detalhes específicos sobre o processo de criptografia e agrupamento, consulte [criptografia em nuvem da Microsoft](office-365-encryption-in-the-microsoft-cloud-overview.md). 

No SharePoint Online, os itens são mantidos por 93 dias desde o momento em que você pode excluí-los a partir de seu local original. Eles permanecem na Lixeira do site todo o tempo, a menos que alguém exclui-los a partir daí, ou esvazia que Lixeira. Nesse caso, os itens vá para o Lixeira, onde eles mantenha-se para o restante dos dias 93 do conjunto de sites. Para informações sobre como restaurar itens excluídos, consulte [restaurar itens da Lixeira de um site do SharePoint](https://support.office.com/en-us/article/6df466b6-55f2-4898-8d6e-c0dff851a0be#ID0EAADAAA=Online
) e [restaurar itens excluídos da Lixeira do conjunto de sites](https://support.office.com/article/5fa924ee-16d7-487b-9a0a-021b9062d14b). O tempo de retenção da Lixeira não é configurável no SharePoint Online.

Quando você exclui um conjunto de sites, você também estiver excluindo a hierarquia dos sites na coleção e todo o conteúdo delas:
- Documentos e bibliotecas de documentos
- Listas e dados de lista
- Definições de configuração de site
- Informações de segurança e funções relacionadas para o site ou seus subsites
- Subsites das informações do site, seus conteúdos e usuário nível superior

Se você acidentalmente excluir um conjunto de sites, ele pode ser restaurado por um global ou SharePoint admin usando o Centro de administração do SharePoint. 

Disco rígido exclusão ocorre quando um usuário limpa os itens excluídos da Lixeira, do conjunto de sites quando os períodos de retenção e backup expirarem, ou quando um administrador exclui permanentemente um conjunto de sites usando o [cmdlet Remove-SPODeletedSite](/powershell/module/sharepoint-online/Remove-SPODeletedSite?view=sharepoint-ps). Quando o usuário rígido exclui (exclui permanentemente ou limpa) conteúdo do SharePoint Online, todas as chaves de criptografia para os blocos excluídos serão excluídas também. Os blocos nos discos que anteriormente armazenados os blocos excluídos são marcados como não utilizado e disponível para usar novamente.

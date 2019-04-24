---
title: API da Atividade de Gerenciamento do Office 365
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
- M365-analytics
description: Um breve resumo sobre a API da atividade de gerenciamento do Office 365.
ms.openlocfilehash: 3405eaac000111fb5d5f054edcbe6816aa9af9e7
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262553"
---
# <a name="office-365-management-activity-api"></a>API da Atividade de Gerenciamento do Office 365
A Microsoft fornece o Reporting Services que permite que os administradores obtenham informações transacionais agregadas sobre o locatário do Office 365. A [API de atividade de gerenciamento do Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview) usa um design RESTful padrão da indústria e o OAuth v2 para autenticação, o que facilita o início da experimentação com a recuperação de dados e sua inclusão em ferramentas e aplicativos de visualização. A API fornece um feed de dados que inclui informações sobre o usuário, administrador, operações e atividade de segurança no Office 365. Os dados podem ser mantidos por razões regulamentares ou combinados com os dados de log adquiridos de uma infraestrutura local ou de outras fontes para criar uma solução de monitoramento para operações, segurança e conformidade em toda a empresa.

A API da Atividade de Gerenciamento do Office 365 fornece informações sobre várias ações e eventos de usuário, administração, sistema e políticas dos logs de atividades do Office 365 e do Azure Active Directory. A API fornece um esquema de auditoria consistente com mais de 10 campos que são comuns em todos os serviços. Isso permite que as organizações façam conexões fáceis entre eventos e permite que as novas maneiras de se deparam com os dados. Dezenas de ISVs (fornecedores de software independentes) fizeram parceria com a Microsoft e criaram soluções com base na API. Algumas soluções estão concentradas exclusivamente nos dados do Office 365, enquanto outras oferecem a capacidade de incluir dados de vários provedores de nuvem e sistemas locais para criar uma visão unificada de todas as operações, segurança e atividade relacionada à conformidade. Para obter mais informações, consulte a [referência da API da atividade de gerenciamento do Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).

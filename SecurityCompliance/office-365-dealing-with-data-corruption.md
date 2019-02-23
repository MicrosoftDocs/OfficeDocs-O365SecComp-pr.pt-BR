---
title: Office 365 lidando com corrupção de dados
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Uma explicação sobre corrupção de dados no Office 365 e esforços de prevenção e recuperação da Microsoft.
ms.openlocfilehash: d33cb298c432db45d560e4c2876d9ac34ab9d6f4
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216541"
---
# <a name="dealing-with-data-corruption-in-office-365"></a>Lidando com corrupção de dados no Office 365

Um dos aspectos desafiadores de execução de um serviço de nuvem em larga escala é como lidar com a corrupção de dados, considerando o grande volume de dados e sistemas independentes. A corrupção dos dados pode ser causada por:
- Erros de infraestrutura ou aplicativo, corrompendo parte ou todo o estado do aplicativo 
- Problemas de hardware que resultam em perda de dados ou incapacidade de ler dados 
- Erros operacionais humanos 
- Hackers mal-intencionados e funcionários descontentes 
- Incidentes em serviços externos que resultam em alguma perda de dados 

Como a maior resiliência na integridade dos dados significa menos incidentes de corrupção de dados, a Microsoft incorporou os mecanismos de proteção do Office 365 para evitar que os danos ocorram, bem como sistemas e processos que nos permitam recuperar dados, se houver. Os cheques e processos existem dentro dos vários estágios do processo de lançamento da engenharia para aumentar a resiliência contra corrupção de dados, incluindo:
- Design de sistema
- Organização e estrutura de código 
- Revisão de código 
- Testes de unidade, testes de integração e testes de sistema
- Testes/Gates dos fios de viagem 

Nos ambientes de produção do Office 365, a replicação de mesmo nível entre data centers garante que sempre haja várias cópias ao vivo de qualquer dado. Imagens e scripts padrão são usados para recuperar servidores perdidos e dados replicados são usados para restaurar dados do cliente. Devido às verificações e processos de resiliência de dados internos, a Microsoft mantém backups somente da documentação do sistema de informações do Office 365 (incluindo documentação relacionada à segurança), usando a replicação interna no SharePoint Online e nosso código interno ferramenta de repositório, depósito de origem. A documentação do sistema está armazenada no SharePoint Online e o depósito de origem contém imagens de sistema e de aplicativo. O SharePoint Online e o Source Depot usam o controle de versão e são replicados quase em tempo real. 
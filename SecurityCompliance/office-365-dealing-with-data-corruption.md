---
title: O Office 365 lidando com corrupção de dados
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
description: Uma explicação dos corrupção de dados no Office 365 e esforços da Microsoft de prevenção e recuperação.
ms.openlocfilehash: 087be23ce5dad1daf62357cb08e27c0a15962792
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524147"
---
# <a name="dealing-with-data-corruption-in-office-365"></a>Lidando com corrupção de dados no Office 365

Um dos aspectos desafiadoras da execução de um serviço em nuvem em larga escala é como lidar com a corrupção de dados, recebe um grande volume de dados e sistemas independentes. Corrupção de dados pode ser causada por:
- Aplicativo ou infraestrutura bugs, corromper parte ou todo o estado do aplicativo 
- Problemas de hardware que resultam em perda de dados ou incapacidade de ler dados 
- Erros operacionais humanos 
- Hackers mal-intencionados e funcionários insatisfeitos 
- Em serviços externos que resultar em alguma perda de dados de incidentes 

Como maior resiliência em integridade dos dados significa menos incidentes de corrupção de dados, o Microsoft incorporou em mecanismos de proteção do Office 365 para evitar corrupção de aconteça, bem como sistemas e processos que permitem conosco recuperar dados, se existir. Verificações e processos existirem dentro aos vários estágios do processo de lançamento de engenharia para aumentar a resiliência contra corrupção de dados, incluindo:
- Design do sistema
- Código de organização e estrutura 
- Revisão de código 
- Testes de unidade, testes de integração e testes do sistema
- Viagem conecta/entradas de testes 

Em ambientes de produção do Office 365, a replicação de ponto entre data centers garante que sempre existem várias cópias ao vivo de todos os dados. Scripts e arquivos de imagens padrão são usados para recuperar servidores perdidos e dados replicados são usados para restaurar dados do cliente. Devido às verificações de resiliência de dados interno e processos, a Microsoft mantém backups apenas de documentação do Office 365 informações sistema (incluindo documentação relacionada à segurança), usando a replicação interna no SharePoint Online e o nosso código interno ferramenta do repositório, depósito de origem. Documentação do sistema é armazenada no SharePoint Online e depósito de origem contém as imagens de sistema e de aplicativo. SharePoint Online e depósito de origem usam o controle de versão e são replicados em praticamente em tempo real. 
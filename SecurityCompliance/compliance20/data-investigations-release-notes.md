---
title: Notas de versão do investigações de dados (Preview) no Microsoft 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Este artigo descreve a nova versão do eDiscovery avançado (Preview) no Microsoft 365.
ms.openlocfilehash: 90bcbd4cae1e410e1544352a776ba4cbbedfa429
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29695057"
---
# <a name="release-notes-for-data-investigations-preview-in-microsoft-365"></a>Notas de versão do investigações de dados (Preview) no Microsoft 365

Você pode usar a nova ferramenta investigações de dados (Preview) no Microsoft 365 triagem, investigar e corrigir os dados relacionados incidentes, como uma investigação interna ou de um incidente de algum derramamento de dados. As investigações de visualização de dados públicos oferece acesso antecipado à funcionalidade futura e atualizações. Para obter acesso antecipado para os recursos mais recentes, crie uma nova investigação em investigações de dados (Preview) no Centro de conformidade do & de segurança do Office 365. Para saber como fazer isso, consulte [Manage um incidente de algum derramamento de dados no Microsoft 365](manage-data-spillage-incidents.md).

## <a name="whats-new"></a>Novidades 

- **Investigações** - você pode agrupar pesquisas e incidentes criando uma investigação. Gerencie quem pode acessar a investigação adicionando ou removendo membros.  Você também pode selecionar e marcar suas investigações favoritas. Controlar e monitorar a atividade dentro e entre investigações usando novos painéis. Depois de concluir sua investigação, você pode fechar ou excluí-lo.

- **Pessoas de interesse** – quando você adiciona usuários para investigações como pessoas de interesse, você pode ver suas caixas de correio, OneDrive para negócios conta e sites de Teams da Microsoft. Você pode usá-los à suas investigação pesquisas de conteúdo de escopo. Para obter mais investigar uma pessoa de interesse, também é possível exibir auditar registros relacionados a suas atividades no Office 365 e outros serviços da Microsoft.

- **Pesquisas** – criar uma pesquisa de toda a organização usando diversas condição de pesquisa. Se você souber a usuários ou sites que você deseja pesquisar, você pode fazer isso, esses usuários adicionando pessoas de interesse ou especificação locais de site no Assistente para criação de pesquisa. 

- **Incidentes** – criar um novo incidente e adicionar os resultados de pesquisa que você deseja analisar. Você pode analisar documentos individuais, anotar para deixar investigação anotações e exportar os resultados para mover para um ambiente diferente. 

- **Revise** – Use uma nativo, texto e modo de exibição de quase nativos para analisar documentos adicionados a um incidente. Você também pode aplicar analytics aos documentos agrupar itens, duplicatas, threads de email e temas, que podem ajudar a ajudar sua revisão do incidente. 

- **Redact, marcar e anotar** – redigir texto, aplicar marcas e fazer anotações à medida que você examine os documentos.
  
- **Indexação minuciosa** – se houver itens indexados parcialmente, eles serão indexados novamente sob demanda para que todos os dados estarão disponíveis para pesquisa.

- **Correção de erro** – corrigir ou erros de processamento de download. Isso inclui o suporte de remediação para tipos de arquivos grandes, arquivos e outros problemas relacionados à indexação erros protegido por senha. 

- **Trabalhos** – controlar o status dos processos de longa execução.

- **Itens de caixa de correio rígido-delete** - urgente situações, você talvez seja necessário excluir permanentemente os itens no local errado. Para fazer isso, você pode executar o **New-ComplianceSearchAction-limpar - PurgeType HardDelete** command na segurança & PowerShell do Centro de conformidade para remover permanentemente os itens de caixas de correio. Para obter mais informações, consulte [New-ComplianceSearchAction](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/new-compliancesearchaction).

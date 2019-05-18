---
title: Notas de versão para investigações de dados (visualização) no Microsoft 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Este artigo descreve a nova ferramenta de investigações de dados (visualização) no Microsoft 365.
ms.openlocfilehash: 200b1c6c08d0fdb1c4af5da59fa75836b4b1fab3
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34150893"
---
# <a name="release-notes-for-data-investigations-preview-in-microsoft-365"></a>Notas de versão para investigações de dados (visualização) no Microsoft 365

Você pode usar a ferramenta novas investigações de dados (visualização) no Microsoft 365 para fazer a triagem, investigar e corrigir incidentes relacionados a dados, como um incidente de derramamento de dados ou uma investigação interna. A visualização pública de investigações de dados fornece acesso antecipado às futuras funcionalidades e atualizações. Para obter acesso antecipado aos recursos mais recentes, crie uma nova investigação em investigações de dados (visualização) no centro de conformidade do & de segurança. Para saber como, confira [gerenciar um incidente de derramamento de dados no Microsoft 365](manage-data-spillage-incidents.md).

## <a name="whats-new"></a>Novidades 

- **Investigações** – você pode agrupar pesquisas e incidentes criando uma investigação. Gerenciar quem pode acessar a investigação adicionando ou removendo membros.  Você também pode selecionar e marcar suas investigações favoritas. Controlar e monitorar a atividade dentro e nas investigações usando novos painéis. Depois de concluir sua investigação, você pode fechá-la ou excluí-la.

- **Pessoas de interesse** – ao adicionar usuários a investigações como pessoas de interesse, você pode ver a caixa de correio, a conta do onedrive for Business e os sites do Microsoft Teams. Você pode usá-los para fazer o escopo das pesquisas de conteúdo investigativas. Para investigar ainda mais uma pessoa de interesse, você também pode exibir registros de auditoria relacionados às suas atividades no Office 365 e outros serviços da Microsoft.

- **Pesquisas** – crie uma pesquisa em toda a organização usando várias condições de pesquisa. Se você souber os usuários ou sites que deseja pesquisar, poderá fazê-lo adicionando-os como pessoas de interesse ou especificando locais de site no assistente de criação de pesquisa. 

- **Evidência** – crie um novo conjunto de evidências e adicione resultados de pesquisa que você deseja revisar. Você pode revisar documentos individuais, anotar para sair de notas de investigação e exportar resultados para mover para um ambiente diferente. 

- **Revisão** – use um modo de exibição nativo, de texto e quase nativo para revisar os documentos adicionados a um incidente. Você também pode aplicar a análise a documentos para agrupar itens por duplicatas, threads de email e temas, que podem ajudar a analisar o incidente. 

- **Redigir, marcar e anotar** – redigir texto, aplicar marcas e fazer anotações à medida que você revisar documentos.
  
- **Indexação avançada** – se houver algum item parcialmente indexado, eles serão novamente reindexados por demanda, de forma que todos os dados estarão disponíveis para pesquisa.

- **Correção de erro** : corrigir ou baixar erros de processamento. Isso inclui suporte de correção para tipos de arquivo grandes, arquivos protegidos por senha e outros problemas relacionados a erros de indexação. 

- **Jobs** – rastreie o status de processos de execução longa.

- **Itens de caixa de correio de exclusão de hardware** -em situações urgentes, talvez seja necessário excluir permanentemente os itens no local errado. Para fazer isso, você pode executar o comando **New-ComplianceSearchAction-purga-PurgeType HardDelete** no Security & centro de conformidade do PowerShell para remover itens permanentemente das caixas de correio. Para obter mais informações, consulte [New-ComplianceSearchAction](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/new-compliancesearchaction).

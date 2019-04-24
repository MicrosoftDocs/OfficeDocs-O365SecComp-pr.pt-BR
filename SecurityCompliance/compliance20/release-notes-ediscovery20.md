---
title: Notas de versão para descoberta eletrônica avançada (versão prévia)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Este artigo contém as notas de versão da descoberta eletrônica avançada (versão prévia).
ms.openlocfilehash: 32a02c16fd30e740fcc6e1c99b46775b97590a28
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32240936"
---
# <a name="release-notes-for-advanced-ediscovery-preview"></a>Notas de versão para descoberta eletrônica avançada (versão prévia)

O programa de visualização pública para descoberta eletrônica avançada é a maneira de obter acesso antecipado à funcionalidade e às atualizações futuras. Para obter acesso antecipado aos recursos mais recentes, basta criar e usar um caso de descoberta eletrônica avançada (visualização) no centro de conformidade do & de segurança do Office 365. ConFira [criar um novo caso](create-new-ediscovery-case.md).

## <a name="known-issues"></a>Problemas conhecidos

**Microsoft Forms**

- Os dados correspondentes a um formulário criado antes de 31 de janeiro de 2019 não poderão ser pesquisados ao usar a ferramenta de pesquisa na descoberta eletrônica avançada (visualização) para pesquisar caixas de correio. Formulários criados após essa data estarão disponíveis para pesquisa.

- Um formulário criado por um usuário ainda pode receber respostas, mesmo depois que o usuário que criou o formulário é excluído. No enTanto, os dados correspondentes para essas respostas (que ocorreram depois da exclusão da caixa de correio) não poderão ser pesquisados ao usar a ferramenta de pesquisa na descoberta eletrônica avançada (visualização) para pesquisar caixas de correio de responsáveis.
 
**Microsoft Sway**

- Se um usuário editar um Sway imediatamente antes da exclusão da conta de usuário para o proprietário desse Sway, essas alterações poderão não ser pesquisadas ao usar a ferramenta de pesquisa na descoberta eletrônica avançada (visualização) para pesquisar caixas de correio de responsáveis. O Sway bloqueia alterações em um Sway assim que recebe um sinal de que a conta foi excluída. No enTanto, há uma pequena chance de que um Sway possa ser editado antes que esse sinal seja recebido.

## <a name="issues-fixed-in-this-release"></a>Problemas corrigidos nesta versão

- DCR: manipulação de exceção para itens não indexados e itens órfãos
- DCR: notificações de bloqueio
- DCR: responsáveis pela descoberta eletrônica

## <a name="whats-new"></a>Novidades

- **Navegação reprojetada no centro de conformidade do & de segurança** – a descoberta eletrônica avançada (visualização) tem uma nova aparência. Use a descoberta eletrônica avançada (versão prévia) para gerenciar mais de seu fluxo de trabalho de caso.

- **Gerenciamento de casos** – há suporte adicional para novos tipos de caso. Você também pode selecionar e salvar seus casos recentes e favoritos. Controlar e monitorar a atividade em e entre casos usando novos painéis.

- **Gerenciamento de responsáveis** – adicione e remova usuários como responsáveis por dados em um caso.

- **Integração com o Exchange, o onedrive e** o Teams – adicione automaticamente a caixa de correio de um usuário, a conta do onedrive for Business e os sites do Microsoft Teams a uma ocorrência. 

- **Comunicações de responsáveis** – envie e gerencie notificações de retenção legal em nome da sua organização.

- **Portal de responsáveis** – novo portal para que os responsáveis acessem seus avisos de isenção ativos.

- **IndexAção profunda** – Rastreie novamente os itens parcialmente indexados sob demanda.

- **Correção de erro** : corrigir ou baixar erros de processamento; Isso inclui suporte de correção para tipos de arquivo grandes, arquivos protegidos por senha e muito mais. 

- **Melhorias na pesquisa** – crie uma pesquisa identificando os responsáveis e/ou locais.

- **Conjuntos de trabalho** – gerencie, rastreie e faça auditoria de conjuntos estáticos de documentos.

- **Revisão** – use um modo de exibição nativo, de texto e quase nativo para revisar os documentos adicionados ao seu conjunto de trabalho.

- **Redigir, marcar e anotar** – redigir texto, aplicar marcas e fazer anotações à medida que você revisar documentos.
  
- **Análise com capacidade para análise**– Aproveite a análise de descoberta eletrônica para localizar, Pesquisar e examinar os resultados em um conjunto de trabalho.

- **Jobs** – rastreie o status de processos de execução longa.

- **Novas atividades de auditoria** – rastrear e exibir novas atividades de auditoria para descoberta eletrônica avançada.

---
title: Visão geral do gerenciador de planos de arquivo
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 9/25/2018
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Priority
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: af398293-c69d-465e-a249-d74561552d30
description: O gerenciador de planos de arquivo fornece recursos avançados de gerenciamento de políticas e rótulos de retenção, e oferece uma maneira integrada de percorrer a atividade de rótulos e de rótulo para conteúdo para todo o seu ciclo de vida de conteúdo, desde a criação à colaboração, à declaração de registros, à retenção e por fim a disposição.
ms.openlocfilehash: 792729d55f7096114694a59d7202b36fc130e48c
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30221181"
---
# <a name="overview-of-file-plan-manager"></a>Visão geral do gerenciador de planos de arquivo

O gerenciador de planos de arquivo fornece recursos avançados de gerenciamento de políticas e rótulos de retenção, e oferece uma maneira integrada de percorrer a atividade de rótulos e de rótulo para conteúdo para todo o seu ciclo de vida de conteúdo, desde a criação à colaboração, à declaração de registros, à retenção e por fim a disposição.

![Página de plano de arquivo](media/file-plan-page.png)

## <a name="important-this-feature-is-currently-available-only-as-part-of-the-office-365-preview-program"></a>Importante: este recurso está atualmente disponível somente como parte do programa Office 365 Preview

Você verá esse recurso no seu locatário apenas se sua organização estiver inscrita no programa Office 365 Preview.

## <a name="accessing-file-plan-manager"></a>Acessar o gerenciador de planos de arquivo

Há dois requisitos para acessar o gerenciador de planos de arquivo, que são:
- Uma assinatura do Office 365 Enterprise E5.
- O usuário ter recebido uma das seguintes funções do Centro de Conformidade e Segurança: 
    - Gerenciador de Retenção
    - Gerenciador de Retenção somente exibição

## <a name="navigating-your-file-plan"></a>Navegar pelo plano de arquivo

O gerente de plano de arquivo torna mais fácil ver todas as configurações dos seus rótulos e políticas de retenção no mesmo modo de exibição.

Observe que os rótulos de retenção criados fora do plano de arquivamento estarão disponíveis no plano de arquivamento e vice-versa.

Na guia **rótulos de plano de arquivo**, as seguintes informações e recursos adicionais estão disponíveis:

### <a name="label-settings-columns"></a>Colunas de configurações de rótulo
 
- **Com base em** identifica o tipo de gatilho que iniciará o período de retenção. Os valores válidos estão: 
    - Evento
    - Data de criação
    - Data da última modificação
    - Data do rótulo
- **Registro** identifica se o item se tornará um registro declarado quando o rótulo for aplicado. Os valores válidos são:
    - Não
    - Sim
    - Sim (Regulatório)
- **Retenção** identifica o tipo de retenção. Os valores válidos são:
    - Manter
    - Manter e excluir
    - Excluir
- **Descarte** identifica o que acontecerá com o conteúdo no final do período de retenção. Os valores válidos são: 
    - null
    - Nenhuma ação
    - Excluir automaticamente
    - Revisão obrigatória (também conhecida como revisão de descarte)

![Configurações de rótulos no plano de arquivo](media/file-plan-label-columns.png)

### <a name="label-file-plan-descriptors-columns"></a>Etiqueta plano de arquivo descritores colunas

Agora você pode incluir mais informações na configuração das suas etiquetas de retenção. Inserir descritores de plano de arquivo em rótulos melhora o gerenciamento e a organização do seu plano de arquivamento.

Para começar, o gerenciador de planos de arquivo fornece alguns valores prontos de origem para: Função/departamento, Categoria, Tipo de autoridade e Provisão/citação. Você pode adicionar novos valores descritores de planos de arquivo ao criar ou editar um rótulo de retenção.

Aqui está uma visão geral da etapa de descritores de plano de arquivo ao criar ou editar um rótulo de retenção.

![Descritores de plano de arquivo](media/file-plan-descriptors.png)

Aqui está um modo de exibição das colunas de descritores de plano de arquivo na guia Rótulos do gerenciador de planos de arquivo.

![file-plan-descriptors-on-labels-tab.png](media/file-plan-descriptors-on-labels-tab.png)

## <a name="export-labels-out-of-your-file-plan"></a>Exportar rótulos do seu plano de arquivo

No gerenciador de planos de arquivo, você pode exportar os detalhes de todos os rótulos de retenção para um arquivo .csv, para ajudá-lo a facilitar as avaliações de conformidade periódicas com os participantes de governança de dados na sua organização.

Para exportar todos os rótulos de retenção, acesse **gerenciador de planos de arquivo** \> **ações de plano de arquivo** \> **exportar rótulos**.

![Opção para exportar o plano de arquivo](media/file-plan-export-labels-option.png)

Um arquivo *.csv que contém todos os rótulos de retenção existentes será aberto.

![Arquivo CSV mostrando todas as etiquetas de retenção](media/file-plan-csv-file.png)

## <a name="import-labels-into-your-file-plan"></a>Importar rótulos para seu plano de arquivo

No gerenciador de planos de arquivo, você pode importar em massa novos rótulos, bem como modificar rótulos de retenção existentes.

Para importar novos rótulos de retenção e fazer atualizações aos rótulos de retenção existentes, acesse **gerenciador de planos de arquivo** \> **ações de plano de arquivo** \> **importar rótulos**.

![Opção para importar plano de arquivo](media/file-plan-import-labels-option.png)

![Opção para baixar um modelo de plano de arquivo em branco](media/file-plan-blank-template-option.png)

Baixar um modelo em branco (ou começar com base em uma exportação do seu plano de arquivo atual).

![Modelo de plano de arquivo em branco aberto no Excel](media/file-plan-blank-template.png)

Preencha o modelo de discagem (em breve, estarão disponíveis informações de referência sobre os valores válidos para entradas).

![Modelo de plano de arquivo com as informações preenchidas](media/file-plan-filled-out-template.png)

Carregue o modelo preenchido, e o gerenciador de plano de arquivo validará as entradas e exibirá as estatísticas de importação.

![Estatísticas de importação de plano de arquivo](media/file-plan-import-statistics.png)

Quando a instalação for concluída, volte para o gerenciador de planos de arquivo e atribua novos rótulos às políticas novas ou existentes.

![Opção para publicar rótulos](media/file-plan-publish-labels-option.png)


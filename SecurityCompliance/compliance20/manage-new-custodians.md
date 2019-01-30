---
title: Gerenciando responsáveis em um caso de eDiscovery avançado (Preview)
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
description: ''
ms.openlocfilehash: 742f6bc35b67071fba528e6a0ce543ecc6915762
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607375"
---
# <a name="managing-custodians-in-an-advanced-ediscovery-preview-case"></a>Gerenciando responsáveis em um caso de eDiscovery avançado (Preview)

Na guia responsáveis contém uma lista classificada de todos os responsáveis no caso. Depois de adicionar responsáveis a um caso, detalhes sobre cada responsável automaticamente serão coletadas do Azure Active Directory.

## <a name="viewing-custodian-details"></a>Exibir os detalhes dos responsáveis

A página de submenu que contém detalhes dos responsáveis é exibida depois de adicionar um funcionário encarregado a um caso e selecione-os da lista na guia **responsáveis** . A partir daqui, você pode exibir todos os detalhes relacionados a dos responsáveis. A página de submenu contém os seguintes campos:

- Informações de contato

  - **Nome de exibição**: O nome exibido no catálogo de endereços para dos responsáveis. Isso geralmente é a combinação entre nome das dos responsáveis, nome intermediário de inicial e o sobrenome.
  - **Mail/SMTP**: endereço SMTP o dos responsáveis, por exemplo, jeff@contoso.onmicrosoft.com.  
  - **Título**: o cargo de responsáveis.
  - **Departamento**: O nome para o departamento no qual dos responsáveis funciona.
  - **Gerente**: gerente de responsáveis. O gerente designado receberá qualquer comunicações de escalonamento para dos responsáveis.
  
- Informações sobre o local

  - **Cidade**: A cidade na qual dos responsáveis está localizado.
  - **Estado**: O estado ou província no endereço de responsáveis.
  - **País/região**: O país/região no qual dos responsáveis está localizado; Por exemplo, "EUA" ou "UK".
  - **Office**: O local do escritório no lugar de responsáveis dos negócios.

- Informações do caso

  - **Status de isenção**: indica se dos responsáveis foi colocado em espera. 
  - **Status de comunicação**: indica se dos responsáveis tem sido emitido um aviso de isenção. Se dos responsáveis tem sido emitido um aviso, em seguida, isso será marcado como *publicado*. Se dos responsáveis não tem sido emitido um aviso, então esse status será *cancelada*. 
  - **Status**: O status do dos responsáveis dentro o caso. Isso estará *ativo* se dos responsáveis estiver ainda em espera para o caso. Se um funcionário encarregado for removido de um caso, seu status será alterado para *liberado*. 

- Status do processamento

  - **Status da indexação**: indica o status do trabalho de indexação aprofundado.  
  - **Indexação última vez atualizados**: indica a datestamp de quando o trabalho de indexação minuciosa última foi disparado.
  - **Fontes de dados**: mostra a contagem de caixas de correio, sites e equipes que foram selecionadas para dos responsáveis.

## <a name="updating-a-custodian"></a>Atualizando um funcionário encarregado

Como suas maiusculas em andamento, você pode descobrir que podem haver fontes de dados adicionais relevantes para uma & dos responsáveis específico seu caso. Em outros cenários, convém remover determinadas fontes de dados que foram revisadas e considerados como não relevantes.

Para atualizar dos responsáveis e as fontes de dados selecionado:

1. Selecione uma ocorrência existente a **eDiscovery avançado do eDiscovery gt _ (Preview)**.
  
2. No caso, clique na guia **responsáveis** .
  
3. Selecione o custodian(s) na lista e clique em **Editar fontes**.
  
4. Atualize seleções para locais do Exchange e OneDrive clicando em **fontes de dados de escolha**.
  
5. Adicionar ou remover o Exchange, SharePoint ou equipes caixas de correio mapeado o usuário clicando para **Selecionar as fontes de dados adicionais**. Para obter mais informações sobre como mapear dados fontes para dos responsáveis, consulte [Adicionar responsáveis a um eDiscovery avançado (Preview) caso](add-custodians-to-case.md).
  
6. Para atualizar o status de retenção dos responsáveis, clique em **retenções locais custódia**e habilitar ou desabilitar a isenção para os responsáveis.

> [!TIP]
> Você pode selecionar vários responsáveis para realizar ações em massa, como reindexação, liberando ou editando um conjunto dos responsáveis.

## <a name="resolving-custodian-processing-errors"></a>Resolvendo erros de processamento dos responsáveis

Na maioria dos fluxos de trabalho Legal, depois responsáveis são adicionados para uma investigação específica, um subconjunto de dados dos usuários será pesquisado. Devido aos tamanhos de arquivos grandes ou corrupção possível, alguns itens dentro de fontes de dados dos responsáveis podem ser indexadas parcialmente. Usando o recurso de indexação minuciosa eDiscovery avançado (Preview), esses itens indexados parcialmente podem ser remediadas de automaticamente pelo novamente rastrear e indexar novamente esses itens sob demanda. 

Quando um funcionário encarregado é adicionado a um caso, os dados serão automaticamente "profundidade indexados", permitindo que os usuários deixar estas parcialmente indexados itens locais em vez de informarem baixar, remediar e execute novamente a pesquisas fora do Office 365. Durante o ciclo de vida de um caso, um usuário pode remediar itens ou adicionar novas fontes de dados para dos responsáveis determinado. Isso pode exigir o índice dos responsáveis a ser atualizado. 

Para disparar um processo de indexação novamente para endereço parcialmente itens indexados:

1. Vá para **eDiscovery avançado do eDiscovery gt _ (Preview)** e selecione uma ocorrência existente.

2. No caso, clique em à **guia responsáveis**. 

3. Selecione o custodian(s) que precisa ser indexado novamente e, em seguida, clique em **Atualizar índice** da página de submenu.

4. Verificar o status do índice dos responsáveis clicando no link na coluna **Status do trabalho de indexação** na guia **responsáveis** .  

5. O status para o processo de indexação novamente também podem ser rastreado na guia **Jobs** .

Para obter mais informações sobre os itens indexados parcialmente indexação novamente e remediando, consulte [Corrigindo erros no eDiscovery avançado (Preview) de processamento](processing-data-for-case.md).

## <a name="releasing-a-custodian-from-a-case"></a>Liberação de um funcionário encarregado de um caso

Dos responsáveis for lançado em situações onde um caso for fechado, um funcionário encarregado não está mais sendo obrigação de preservar o conteúdo de um caso ou quando um funcionário encarregado é considerado nenhum mais ser relevantes para uma determinada caso. 

Se você solta um funcionário encarregado após um aviso de isenção foi publicado, um aviso de versão será enviado para dos responsáveis. Além disso, qualquer isenções custódia atribuídas aos responsáveis lançadas também serão removidas.

Se dos responsáveis foi colocado em uma espera silenciosa, onde eles não foram emitidos qualquer notificações de retenção legal, qualquer isenções custódia atribuídas aos responsáveis lançadas serão removidas.  

Para liberar um funcionário encarregado: 

1.  Vá para a guia **responsáveis** .

2.  Selecione dos responsáveis da lista e clique **responsáveis versão** na página submenu.

    O status do dos responsáveis na guia **responsáveis** é definido para a **Outubrolançada** e o **status de retenção** na página submenu é alterado para **inativo**. 

> [!TIP]
> Dos responsáveis podem ser simultaneamente estar envolvido nos vários assuntos de retenção legal. Quando um funcionário encarregado é liberado de um caso, as isenções e notificações em outros assuntos não serão afetadas.

## <a name="related-information"></a>Informações relacionadas

 - Atributos de usuário no Active Directory 
 - [Correção de erro durante o processamento de dados](error-remediation.md) 
 - [Trabalhando com a comunicação](managing-custodian-communications.md)

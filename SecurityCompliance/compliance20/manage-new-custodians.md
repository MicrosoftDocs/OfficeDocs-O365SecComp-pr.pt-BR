---
title: Gerenciar os responsáveis em um caso de descoberta eletrônica avançada (visualização)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 0c33335ecc103a97090dacaa769315ad9413b3c6
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214971"
---
# <a name="manage-custodians-in-an-advanced-ediscovery-preview-case"></a>Gerenciar os responsáveis em um caso de descoberta eletrônica avançada (visualização)

A guia responsáveis contém uma lista classificável de todos os responsáveis da ocorrência. Após adicionar os responsáveis a um caso, os detalhes sobre cada um serão automaticamente coletados do Azure Active Directory.

## <a name="viewing-custodian-details"></a>Exibindo detalhes do responsáveis

A página de menu que contém os detalhes dos responsáveis é exibida após você adicionar um dos responsáveis a um caso e selecioná-los na lista da guia **responsáveis** . A partir daqui, você pode exibir todos os detalhes relacionados a esses responsáveis. A página de submenu contém os seguintes campos:

- Informações de contato

  - **Nome para exibição**: o nome exibido no catálogo de endereços para os responsáveis. Geralmente, é a combinação do nome do responsáveis, inicial e sobrenome do meio.
  - **Mail/SMTP**: o endereço SMTP para os responsáveis, por exemplo, Jeff@contoso.onmicrosoft.com.  
  - **Título**: o cargo do profissional.
  - **Departamento**: o nome do departamento no qual os responsáveis funciona.
  - **Gerente**: gerente do responsáveis. O gerente designado receberá qualquer comunicação de escalonamento para este responsáveis.
  
- Informações sobre o local

  - **Cidade**: a cidade na qual o responsáveis está localizado.
  - **Estado**: o estado ou província no endereço do responsáveis.
  - **País/região**: o país/região no qual o responsáveis está localizado; por exemplo, "US" ou "ru".
  - **Office**: o local do escritório no local de trabalho do responsáveis.

- Informações sobre o caso

  - **Status de espera**: indica se os responsáveis foram colocados em espera. 
  - **Status de Comunicação**: indica se os responsáveis foram emitidos um aviso de espera. Se o objecttiver sido emitido um aviso, ele será marcado como *publicado*. Se não tiver sido emitido um aviso para os responsáveis, este status será canCelado. ** 
  - **Status**: o status dos responsáveis dentro do caso. Isso estará *ativo* se os responsáveis ainda estiverem em espera para o caso. Se um responsáveis for removido de uma ocorrência, seu status será alterado para *liberado*. 

- Status de processamento

  - **Status**de indexação: indica o status do trabalho de indexação profunda.  
  - **Hora da última atualização**da indexação: indica o dateStamp de quando o trabalho de indexação profunda foi disparado pela última vez.
  - **Fontes de dados**: mostra a contagem de caixas de correio, sites e equipes que foram selecionadas para os responsáveis.

## <a name="updating-a-custodian"></a>Atualizando um responsáveis

À medida que seu caso avança, você pode descobrir que pode haver fontes de dados adicionais relevantes para um determinado & de seu caso. Em outros cenários, talvez você queira remover determinadas fontes de dados que foram revisadas e consideradas não relevantes.

Para atualizar um Objecte as fontes de dados selecionadas:

1. Selecione um caso existente na **descoberta eletrônica avançada do > de descoberta eletrônica (visualização)**.
  
2. No caso, clique na guia **responsáveis** .
  
3. Selecione os responsáveis (s) na lista e clique em **Editar fontes**.
  
4. Atualize as seleções para os locais do Exchange e do OneDrive clicando em **escolher fontes de dados**.
  
5. Adicione ou remova as caixas de correio do Teams, SharePoint ou Exchange mapeadas ao usuário clicando para **selecionar outras fontes de dados**. Para obter mais informações sobre como mapear fontes de dados para um dos responsáveis, confira [Adicionar responsáveis a um caso](add-custodians-to-case.md).
  
6. Para atualizar o status de retenção de responsáveis, clique em **colocar custodial isenções**e habilite ou desabilite a retenção para os responsáveis.

> [!TIP]
> Você pode selecionar vários responsáveis para executar ações em massa, como reindexação, liberação ou edição de um conjunto de responsáveis.

## <a name="resolving-custodian-processing-errors"></a>Resolvendo erros de processamento de responsáveis

Na maioria dos fluxos de trabalho jurídicos, após a adição de responsáveis por uma investigação específica, um subconjunto dos dados dos usuários será pesquisado. Devido a grandes tamanhos de arquivo ou possíveis danos, alguns itens dentro das fontes de dados dos responsáveis podem ser parcialmente indexados. Usando o recurso de indexação avançada de descoberta eletrônica avançada (visualização), esses itens parcialmente indexados podem ser corrigidos automaticamente por meio de um novo rastreamento e re-indexação desses itens sob demanda. 

Quando um usuário é adicionado a uma ocorrência, seus dados serão automaticamente "indexados em profundidade", permitindo que os usuários deixem esses itens parcialmente indexados em vez de terem que baixar, corrigir e executar novamente as pesquisas fora do Office 365. Durante o ciclo de vida de um caso, um usuário pode corrigir itens ou adicionar novas fontes de dados para um determinado usuário. Isso pode exigir que o índice de responsáveis seja atualizado. 

Para acionar um processo de reindexação para lidar com itens parcialmente indexados:

1. Vá para descoberta eletrônica **_GT_ avançada de descoberta eletrônica (visualização)** e selecione uma ocorrência existente.

2. No caso, clique em para a **guia responsáveis**. 

3. Selecione os responsáveis que precisam ser indexados novamente e clique em **Atualizar índice** na página do menu suspenso.

4. Verifique o status do índice de responsáveis clicando no link na coluna **status do trabalho** de indexação na guia **responsáveis** .  

5. O status do processo de reindexação também pode ser acompanhado na guia **trabalhos** .

Para obter mais informações sobre a reindexação e a correção de itens parcialmente indexados, consulte [corrigir erros de processamento](processing-data-for-case.md).

## <a name="releasing-a-custodian-from-a-case"></a>Liberar um dos responsáveis por um caso

Um dos responsáveis é lançado em situações em que um caso é fechado, um não está mais sob obrigação de preservar o conteúdo de um caso ou quando um Objecté considerado não mais relevante para um caso específico. 

Se você liberar um dos responsáveis após um aviso de isenção ter sido publicado, um aviso de lançamento será enviado para o seu. Além disso, qualquer custodial que tenha sido atribuído aos responsáveis liberados também será removido.

Se o objecttiver sido colocado em um bloqueio silencioso, onde não foram emitidos notificações de bloqueio legal, qualquer custodial será atribuído aos responsáveis liberados serão removidos.  

Para liberar um responsáveis: 

1.  Vá para a guia **responsáveis** .

2.  Selecione os responsáveis na lista e clique em **liberar responsáveis** na página do menu suspenso.

    O status do responsáveis na guia **responsáveis** é definido como **liberado** e o **status de retenção** na página do submenu é alterado para inativo. **** 

> [!TIP]
> Os responsáveis podem estar simultaneamente envolvidos em várias questões legais. Quando um dos responsáveis é liberado de uma ocorrência, as isenções e notificações entre outras coisas não serão afetadas.

## <a name="related-information"></a>Informações relacionadas

 - [Correção de erro ao processar dados](error-remediation.md) 
- [Trabalhar com comunicações](managing-custodian-communications.md)

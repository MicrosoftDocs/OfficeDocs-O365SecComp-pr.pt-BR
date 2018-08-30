---
title: Aplicar ou remover uma política de exclusão de documentos de um site
ms.author: stephow
author: stephow-msft
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- MET150
ms.assetid: e3e92668-f9b2-46ee-8e5e-c623870588b6
description: Com frequência, as organizações estão sujeitas a regulamentações de conformidade, legais ou outras que exigem que elas retenham documentos por um determinado período. No entanto, reter os documentos por mais tempo do que o necessário poderá expor a organização a riscos legais. Por esse motivo, sua organização pode ter criado uma política de exclusão de documentos para seu site. Por exemplo, pode ser necessário que documentos comerciais gerais sejam excluídos cinco anos após sua criação.
ms.openlocfilehash: abee0da7adfba6f653743d503f8b30770ee93c40
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524466"
---
# <a name="apply-or-remove-a-document-deletion-policy-for-a-site"></a>Aplicar ou remover uma política de exclusão de documentos de um site

Com frequência, as organizações estão sujeitas a regulamentações de conformidade, legais ou outras que exigem que elas retenham documentos por um determinado período. No entanto, reter os documentos por mais tempo do que o necessário poderá expor a organização a riscos legais. Por esse motivo, sua organização pode ter criado uma política de exclusão de documentos para seu site. Por exemplo, pode ser necessário que documentos comerciais gerais sejam excluídos cinco anos após sua criação.
  
Dependendo da sua organização, uma política de exclusão de documentos pode ser:
  
- **Obrigatório** Um proprietário de site não pode recusar uma política obrigatória, que é automaticamente aplicada ao site. 
    
- **Padrão** Uma política padrão é automaticamente aplicada a um site, mas o proprietário do site pode: 
    
  - Escolher outra política, se disponível.
    
  - Recusar totalmente a política caso ela não seja relevante ao conteúdo do site.
    
- **Nem obrigatória nem padrão** Neste caso, nenhuma política será automaticamente aplicada ao site, e o proprietário do site precisará tomar ação para aplicar uma. 
    
Uma política de exclusão de documentos pode conter mais de uma regra — por exemplo, uma regra poderia dizer para excluir documentos um ano após sua criação, mas outra regra poderia dizer para excluir documentos um ano após a última modificação. Se uma política contiver mais de uma regra, você poderá selecionar a regra que melhor se aplique ao seu site. A regra de exclusão será aplicada a todas as bibliotecas no site. Somente uma política e uma regra poderão estar ativas em um site ao mesmo tempo. Como uma política, uma regra pode ser definida como padrão, de forma a ser automaticamente aplicada quando a política for aplicada.
  
Por fim, as políticas de exclusão de documentos são herdadas. Quando você seleciona uma política ou uma regra para seu site, essa seleção é herdada por todos os subsites, embora o proprietário de um subsite possa interromper a herança ao selecionar uma política ou regra diferente. Quando você selecionar uma política ou uma regra, considere o conteúdo de qualquer subsite abaixo de seu site.
  
## <a name="view-the-document-deletion-policies-available-in-a-site-collection"></a>Exibir as políticas de exclusão de documentos disponíveis em um conjunto de sites

Sua organização pode atribuir políticas diferentes a conjuntos de sites diferentes. No nível do conjunto de sites, o proprietário de um conjunto de sites pode exibir todas as políticas de exclusão de documentos disponíveis para aquele conjunto de sites. As políticas pode ter sido disponibilizadas para o modelo de conjunto de sites (e, portanto, para todos os conjuntos de sites criados a partir desse modelo) ou para este conjunto de sites específico.
  
1. No site de nível superior no conjunto de sites, no canto superior direito, escolha **configurações** [ícone de engrenagem] \> **Configurações do Site**.
    
2. Em **Administração do conjunto de sites** \> **políticas de exclusão de documentos**.
    
    > [!NOTE]
    > O link **Políticas de exclusão de documentos** não aparecerá, a menos que as políticas foram atribuídas ao conjunto de sites. Além disso, o link não aparece imediatamente após a políticas que tiverem sido atribuídas a site — pode demorar até 24 horas de quando as políticas são atribuídas para quando o link **Políticas de exclusão de documento** é exibido. 
  
3. Nesta página, você pode exibir:
    
  - As políticas atribuídas no momento e as regras associadas. Selecione uma política para exibir as regras no painel direito.
    
  - A política padrão, se houver, exibe **Sim** na coluna **Padrão**. 
    
  - Uma mensagem será exibida abaixo da lista caso a política tenha sido atribuída como **Obrigatória**.
    
Essa lista é somente para exibição, para que o proprietário de conjunto de sites veja todas as políticas e regras disponíveis. Para aplicar uma política, consulte a próxima seção.
  
![Exibição das políticas de exclusão de documentos atribuídas a um conjunto de sites](media/f2c0433b-2bb5-407d-a364-ae07c9627176.png)
  
## <a name="apply-or-remove-a-document-deletion-policy-for-a-site"></a>Aplicar ou remover uma política de exclusão de documentos de um site

Como proprietário do site ou proprietário de conjunto de sites, sua organização pode ter criado políticas que você poderá aplicar a seu site ou recusar inteiramente.
  
1. No canto superior direito, escolha **configurações** [ícone de engrenagem] \> **Configurações do Site**.
    
2. Em **Administração do Site** \> **políticas de exclusão de documentos**.
    
    > [!NOTE]
    > O link **Políticas de exclusão de documentos** não aparecerá, a menos que as políticas foram atribuídas ao conjunto de sites. Além disso, o link não aparece imediatamente após a políticas que tiverem sido atribuídas a site — pode demorar até 24 horas de quando as políticas são atribuídas para quando o link **Políticas de exclusão de documento** é exibido. 
  
3. Siga um destes procedimentos:
    
  - **Para aplicar uma política** Selecione uma política \> selecionar uma regra nessa política \> **Salvar**.
    
    Somente uma política e uma regra poderão estar ativas em um site ao mesmo tempo. Sua organização pode oferecer várias opções de políticas e de regras ou somente uma política ou uma regra.
    
    ![Selecione a opção de política](media/f7c7c055-fca7-4a4f-bb97-63e35a65beac.png)
  
  - **Para recusar uma política** Escolha **Recusar: Observe Delete** \> **Salvar**.
    
    Como proprietário do site, você poderá recusar uma política de exclusão de documentos se determinar que a política não é aplicável ao conteúdo de seu site. No entanto, você não poderá recusar uma política que tenha sido marcada como **Obrigatória**.
    
    ![Opção opt-Out](media/efac709c-bef7-4a02-a09d-5bc7d2b4ec63.png)
  
## <a name="document-deletion-policies-override-other-policies"></a>As políticas de exclusão de documentos substituem outras políticas

Um site pode usar outras políticas de retenção e exclusão de conteúdo:
  
- Políticas de tipo de conteúdo para o conjunto de sites.
    
- Políticas de gerenciamento de informações para uma lista ou biblioteca.
    
Se você aplicar uma política de exclusão de documentos para um site que já usa políticas de tipo de conteúdo ou políticas de gerenciamento de informações para uma lista ou biblioteca, essas diretivas são ignoradas, enquanto a política de exclusão de documentos está em vigor. Se forem ignoradas outras políticas, você verá a mensagem "O conteúdo deste site usa políticas de exclusão de documentos".
  
Isso significa que você deve planejar para que um site use somente políticas destinadas a conteúdo estruturado (políticas de gerenciamento de informações e políticas de tipo de conteúdo) ou a conteúdo não estruturado (políticas de exclusão de documentos), e não ambas. Caso você recuse uma política de exclusão de documentos, o aviso não será exibido e outros tipos de políticas continuarão a funcionar.
  
As políticas de site não são afetadas por políticas de exclusão de documentos.
  
### <a name="determine-if-content-type-policies-are-being-ignored"></a>Determinar se as políticas de tipo de conteúdo estão sendo ignoradas

Se seu site estava usando políticas de tipo de conteúdo e você verá esta mensagem agora, essas políticas não estão mais em vigor. Para restaurar as políticas de tipo de conteúdo, você pode remover a política de exclusão de documentos do site, conforme descrito anteriormente, se houver uma opção de recusar. Se não houver nenhuma opção para rejeitar, a política de exclusão de documentos é obrigatória e você precisa contatar o responsável pela conformidade em sua organização.
  
1. No canto superior direito, escolha **configurações** [ícone de engrenagem] \> **Configurações do Site**.
    
2. Em **Administração do Site** \> **modelos de política de tipo de conteúdo**.
    
    ![Aviso no site que as políticas de exclusão de documentos que estão sendo usadas](media/4cc3d703-9aff-4695-9670-f78c291c0010.png)
  
### <a name="determine-if-information-management-policies-are-being-ignored"></a>Determinar se as políticas de gerenciamento de informações estão sendo ignoradas

Se seu site estava usando políticas de gerenciamento de informações e agora você ver essa mensagem, essas políticas não estão mais em vigor. Para restaurar as políticas de gerenciamento de informações, você pode remover a política de exclusão de documentos do site, conforme descrito anteriormente, se houver uma opção de recusar. Se não houver nenhuma opção para rejeitar, a política de exclusão de documentos é obrigatória e você precisa contatar o responsável pela conformidade em sua organização.
  
- Para uma lista ou biblioteca, na faixa de opções \> guia **biblioteca** \> **Definições da biblioteca** \> em **permissões e gerenciamento** \> **Configurações de política de gerenciamento de informações**.
    
    ![Aviso no site que as políticas de exclusão de documentos que estão sendo usadas](media/3f043057-a741-4cd8-a165-6d139b986064.png)
  
## <a name="see-also"></a>Confira também

[Visão geral das políticas de exclusão de documentos](document-deletion-policies.md)
  
[Criar uma política de exclusão de documentos](create-a-document-deletion-policy.md)


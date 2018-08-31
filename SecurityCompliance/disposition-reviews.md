---
title: Visão geral das revisões de disposição
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: d0c6095b-bfee-4906-a2c7-89c2d7f411c1
description: Quando você cria um rótulo que retém o conteúdo no Office 365, você pode optar por acionar uma análise de disposição no final do período de retenção.
ms.openlocfilehash: c0a2933f597c9b314ac4ce2e72de9619fac90082
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "23013715"
---
# <a name="overview-of-disposition-reviews"></a>Visão geral das revisões de disposição

Quando o conteúdo atinge o final do período de retenção, há vários motivos por que talvez você queira revisar o conteúdo para decidir se ele pode ser excluído com segurança ("descartados"). Por exemplo, você pode precisar:
  
- Suspenda a exclusão ("descarte") de conteúdo relevante em caso de litígio ou auditoria.
    
- Remova o conteúdo da lista disposição para armazenar em um arquivo morto, se esse conteúdo tiver research ou um valor de histórico.
    
- Atribua um período de retenção diferente para o conteúdo, se a diretiva original foi uma solução temporária ou provisional.
    
- Retornar o conteúdo aos clientes ou transferi-la para outra organização.
    
Quando você cria um rótulo que retém o conteúdo no Office 365, você pode optar por acionar uma análise de disposição no final do período de retenção. Em uma revisão de disposição:
  
- As pessoas que você escolher recebem uma notificação de e-mail que têm conteúdo para analisar. Esses revisores podem ser usuários individuais, distribuição ou grupos de segurança ou grupos do Office 365. Observe que as notificações são enviadas semanalmente.
    
- Os revisores ir para a página de **disposição** na segurança &amp; Centro de conformidade para analisar o conteúdo. 
    
- Para cada documento, o revisor pode:
    
  - Aplica um rótulo diferente.
    
  - Estenda seu período de retenção.
    
  - Excluí-lo permanentemente.
    
- Revisores podem exibir descartes pendentes ou históricos e exportar essa lista como um arquivo. csv.
    
Observe que disposição revisões requerem uma assinatura do Office 365 Enterprise E5.
  
Uma análise de disposição pode incluir o conteúdo em caixas de correio do Exchange, sites do SharePoint, OneDrive contas e grupos do Office 365. Aguardando uma análise de disposição nesses locais de conteúdo é excluído somente depois que um revisor escolhe excluir permanentemente o conteúdo.
  
![Página de disposição](media/b7436fb2-1f35-4146-8ca2-32c9d10f7e09.png)
  
## <a name="setting-up-the-disposition-review-by-creating-a-label"></a>Configurando a revisão de disposição criando um rótulo

Este é o fluxo de trabalho básico para configurar uma análise de disposição. Observe que esse fluxo mostra um rótulo que está sendo publicado e aplicada manualmente por um usuário; Como alternativa, um rótulo que dispara uma análise de disposição pode ser autoaplicado ao conteúdo.
  
![Gráfico mostrando o fluxo de como funciona a disposição](media/5fb3f33a-cb53-468c-becc-6dda0ec52778.png)
  
Uma análise de disposição é uma opção quando você cria um rótulo no Office 365. Observe que essa opção não está disponível em uma política de retenção, mas somente em um rótulo com as configurações de retenção.
  
Para obter mais informações sobre rótulos, consulte [Overview of rótulos](labels.md).
  
![Configurações de retenção para um rótulo](media/a16dd202-8862-40ac-80ff-6fee974de5da.png)
  
## <a name="disposing-content"></a>Disposição de conteúdo

Quando um revisor será notificado por email que o conteúdo está pronto para analisar, eles podem ir para a página de **disposição** na segurança &amp; Centro de conformidade e selecione um ou mais itens. O revisor pode então: 
  
- Aplica um rótulo diferente.
    
- Estenda o período de retenção.
    
- Exclua permanentemente o item.
    
Um revisor pode usar o link para exibir o documento em seu local original, se o revisor tiver permissões para esse local. Durante uma revisão de disposição, nunca move o conteúdo de seu local original e ele é excluído nunca até que o revisor decide fazê-lo.
  
Observe que as notificações de email são enviadas automaticamente aos revisores semanalmente. Portanto, quando o conteúdo atinge o final do período de retenção, pode levar até sete dias para revisores receber email de notificação que o conteúdo está aguardando disposição.
  
Observe também que todas as ações de disposição sejam auditadas. Para garantir isso, você deve ativar a auditoria de pelo menos um dia antes da primeira ação de disposição - para obter mais informações, consulte [Pesquisar o log de auditoria de segurança do Office 365 &amp; Centro de conformidade](search-the-audit-log-in-security-and-compliance.md). 
  
![Opções de disposição para um documento](media/771630fd-a9b0-47cf-983b-fe85eb4cdafd.png)
  
## <a name="permissions-for-disposition"></a>Permissões de disposição

Para obter acesso à página de **disposição** , revisores devem ser membros da função de **Gerenciamento de disposição** e a função **Logs de auditoria somente para exibição** . Recomendamos a criação de um novo grupo de função chamado revisores de disposição, adicionando essas duas funções a esse grupo de função e, em seguida, adicionar membros ao grupo de funções. 
  
Para obter mais informações, consulte [Conceder aos usuários acesso para a segurança do Office 365 &amp; Centro de conformidade](grant-access-to-the-security-and-compliance-center.md)
  
## <a name="how-long-until-disposed-content-is-permanently-deleted"></a>Quanto tempo até que o conteúdo descartado é permanentemente excluído

Aguardando uma análise de disposição de conteúdo é excluído somente depois que um revisor escolhe excluir permanentemente o conteúdo. Quando o revisor escolhe essa opção, o conteúdo no site do SharePoint ou conta de OneDrive se torna qualificado para o processo de limpeza standard descrito nesta seção: [funcionamento de uma política de retenção com conteúdo in-loco](retention-policies.md#how-a-retention-policy-works-with-content-in-place).
  
Isso significa que:
  
- Conteúdo em uma biblioteca de documentos será movido para o primeiro estágio Recycle Bin **dentro de 7 dias** de disposição e excluídos permanentemente **93 dias** depois disso. A Lixeira não é indexada pela pesquisa e, portanto, não está disponível a uma isenção de descoberta eletrônica de seu conteúdo. 
    
- Conteúdo na preservação, mantenha biblioteca serão permanentemente excluídos **dentro de 7 dias** de disposição. 
    
## <a name="view-pending-and-completed-dispositions"></a>Modo de exibição pendentes e concluídas de vendas

Na página **disposição** da segurança &amp; Centro de conformidade, você pode exibir descartes pendentes e concluídas: 
  
- **Pendente** descartes atingiu o final do seu período de retenção e exigem uma análise de disposição. Após revisar cada item, decida se deseja aplicar um rótulo diferente a ele, estender seu período de retenção ou excluí-lo permanentemente. 
    
- **Concluído** descartes foram aprovadas para exclusão durante uma revisão de disposição e agora estão no processo sejam excluídos permanentemente. Itens que tinham um rótulo diferente aplicado ou seu período de retenção estendido como parte de uma análise não aparecerá aqui. 
    
### <a name="filter-the-disposition-views"></a>Filtrar os modos de exibição de disposição

Você pode filtrar esses modos de exibição pelo intervalo de rótulo ou hora. Para pendentes descartes, o intervalo de tempo se baseia na data de vencimento. Para descartes históricas, o intervalo de tempo baseia-se na data de exclusão.
  
![Opções de filtro na página de disposição](media/8682a9f5-a77d-45ae-b902-8418a3ebbea1.png)
  
### <a name="export-the-disposition-items"></a>Exportar os itens de disposição

Além disso, você pode exportar os itens em qualquer modo de exibição como um arquivo. csv que pode ser aberta no Excel.
  
![Dados de disposição exportado no Excel](media/08e3bc09-b132-47b4-a051-a590b697e725.png)
  


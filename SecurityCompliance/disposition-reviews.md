---
title: Visão geral das revisões de disposição
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Ao criar um rótulo que mantém o conteúdo no Office 365, você pode optar por acionar uma análise de disposição no final do período de retenção.
ms.openlocfilehash: a3125ee3f0ae388fce71968f25a68d5ccf3fc652
ms.sourcegitcommit: ed822a776d3419853453583e882f3c61ca26d4b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2019
ms.locfileid: "30410756"
---
# <a name="overview-of-disposition-reviews"></a>Visão geral das revisões de disposição

Quando o conteúdo atinge o final do período de retenção, há vários motivos para que você possa querer revisar o conteúdo para decidir se ele pode ser excluído com segurança ("descartado"). Por exemplo, você pode precisar:
  
- Suspender a exclusão ("disposição") de conteúdo relevante no caso de litígio ou auditoria.
    
- Remova o conteúdo da lista de descarte para armazenar em um arquivo morto, se esse conteúdo tiver um valor de pesquisa ou histórico.
    
- Atribua um período de retenção diferente ao conteúdo, se a política original era uma solução temporária ou provisionada.
    
- Retornar o conteúdo aos clientes ou transferi-lo para outra organização.
    
Ao criar um rótulo que mantém o conteúdo no Office 365, você pode optar por acionar uma análise de disposição no final do período de retenção. Em uma revisão de disposição:
  
- As pessoas escolhidas recebem uma notificação por email de que o conteúdo deve ser revisado. Esses revisores podem ser usuários individuais, grupos de distribuição ou segurança ou grupos do Office 365. Observe que as notificações são enviadas semanalmente.
    
- Os revisores vão para a página de **disposição** no centro &amp; de conformidade de segurança para analisar o conteúdo. 
    
- Para cada documento, o revisor pode:
    
  - Aplicar um rótulo diferente.
    
  - Estenda seu período de retenção.
    
  - Excluí-la permanentemente.
    
- Os revisores podem exibir as desposições de histórico ou pendentes e exportar essa lista como um arquivo. csv.
    
Observe que as revisões de disposição exigem uma assinatura do Office 365 Enterprise e5.
  
Uma análise de disposição pode incluir conteúdo em caixas de correio do Exchange, sites do SharePoint, contas do OneDrive e grupos do Office 365. O conteúdo que está aguardando uma revisão de disposição nesses locais é excluído somente depois que um revisor escolhe excluir permanentemente o conteúdo.
  
![Página de disposição](media/b7436fb2-1f35-4146-8ca2-32c9d10f7e09.png)
  
## <a name="setting-up-the-disposition-review-by-creating-a-label"></a>ConFigurando a revisão de disposição criando um rótulo

Este é o fluxo de trabalho básico para configurar uma revisão de disposição. Observe que esse fluxo mostra um rótulo que está sendo publicado e, em seguida, aplicado manualmente por um usuário; Como alternativa, um rótulo que dispara uma revisão de disposição pode ser aplicado automaticamente ao conteúdo.
  
![Gráfico mostrando o fluxo de como o descarte funciona](media/5fb3f33a-cb53-468c-becc-6dda0ec52778.png)
  
Uma revisão de disposição é uma opção quando você cria um rótulo no Office 365. Observe que essa opção não está disponível em uma política de retenção, mas somente em um rótulo com configurações de retenção.
  
Para saber mais sobre rótulos, confira [Visão geral dos rótulos](labels.md).
  
![Configurações de retenção para um rótulo](media/a16dd202-8862-40ac-80ff-6fee974de5da.png)
  
## <a name="disposing-content"></a>DesCartando conteúdo

Quando um revisor é notificado por email que o conteúdo está pronto para revisão, eles podem ir até a página de **disposição** no &amp; centro de conformidade de segurança e selecionar um ou mais itens. O revisor pode então: 
  
- Aplicar um rótulo diferente.
    
- Estenda o período de retenção.
    
- Excluir permanentemente o item.
    
Um revisor pode usar o link para exibir o documento em seu local original, se o revisor tiver permissões para esse local. Durante uma revisão de disposição, o conteúdo nunca se move do local original e nunca é excluído até que o revisor opte por fazê-lo.
  
Observe que as notificações por email são enviadas automaticamente aos revisores de forma semanal. Portanto, quando o conteúdo atinge o final do período de retenção, pode levar até sete dias para que os revisores recebam a notificação por email de que o conteúdo está aguardando disposição.
  
Observe também que todas as ações de disposição são auditadas. Para garantir isso, você deve ativar a auditoria pelo menos um dia antes da primeira ação de disposição: para saber mais, confira [Pesquisar o log de auditoria no centro de conformidade &amp; de segurança do Office 365](search-the-audit-log-in-security-and-compliance.md). 
  
![Opções de disposição para um documento](media/771630fd-a9b0-47cf-983b-fe85eb4cdafd.png)
  
## <a name="permissions-for-disposition"></a>Permissões para descarte

Para obter acesso à página de **disposição** , os revisores devem ser membros da função de **Gerenciamento de descarte** e da função de logs de **auditoria somente para exibição** . Recomendamos a criação de um novo grupo de função chamado revisores de disposição, adição dessas duas funções a esse grupo de função e adição de membros ao grupo de funções. 
  
Para obter mais informações, consulte [conceder aos usuários acesso ao centro de &amp; conformidade de segurança do Office 365](grant-access-to-the-security-and-compliance-center.md)
  
## <a name="how-long-until-disposed-content-is-permanently-deleted"></a>Quanto tempo até o conteúdo Descartado é excluído permanentemente

O conteúdo que está aguardando uma análise de disposição é excluído somente depois que um revisor escolhe excluir permanentemente o conteúdo. Quando o revisor escolhe essa opção, o conteúdo do site do SharePoint ou da conta do OneDrive fica qualificado para o processo de limpeza padrão descrito nesta seção: [como funciona uma política de retenção com conteúdo in-loco](retention-policies.md#how-a-retention-policy-works-with-content-in-place).
  
Isso significa que:
  
- O conteúdo de uma biblioteca de documentos será movido para a lixeira de primeiro estágio **dentro de sete dias** de disposição e, em seguida, excluído permanentemente **93 dias** após isso. A lixeira não é indexada pela pesquisa e, portanto, seu conteúdo não está disponível para um bloqueio de descoberta eletrônica. 
    
- O conteúdo da biblioteca de retenção de preservação será excluído permanentemente **dentro de 7 dias** após o descarte. 
    
## <a name="view-pending-and-completed-dispositions"></a>Exibir as desposições pendentes e concluídas

Na página **disposição** do centro de conformidade &amp; de segurança, você pode exibir as desposições pendentes e concluídas: 
  
- **** As disposições pendentes atingiram o final do período de retenção e exigem uma análise de disposição. Após a revisão de cada item, decida se deseja aplicar um rótulo diferente a ele, estenda o período de retenção ou exclua-o permanentemente. 
    
- **** As desposições concluídas foram aprovadas para exclusão durante uma revisão de disposição e agora estão em processo de exclusão permanente. Os itens que tinham um rótulo diferente aplicado ou seu período de retenção estendido como parte de uma revisão não aparecerão aqui. 
    
### <a name="filter-the-disposition-views"></a>Filtrar as exibições de disposição

Você pode filtrar esses modos de exibição por rótulo ou intervalo de tempo. Para desposições pendentes, o intervalo de tempo é baseado na data de expiração. Para desposições históricas, o intervalo de tempo é baseado na data de exclusão.
  
![Opções de filtro na página de disposição](media/8682a9f5-a77d-45ae-b902-8418a3ebbea1.png)
  
### <a name="export-the-disposition-items"></a>Exportar os itens de disposição

Além disso, você pode exportar os itens em um modo de exibição como um arquivo. csv que pode ser aberto no Excel.
  
![Dados de disposição exPortados no Excel](media/08e3bc09-b132-47b4-a051-a590b697e725.png)
  


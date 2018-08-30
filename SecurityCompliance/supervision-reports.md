---
title: Relatórios de supervisão
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: 5/12/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2a762db5-e1c9-4c09-aa8e-bef49ce97209
description: Usar relatórios de supervisão para ver quais e-mails conformidade precisa revisar e quem ele deve executar.
ms.openlocfilehash: e18d083c0aad8be945c628516e593462da8e3898
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523653"
---
# <a name="supervision-reports"></a>Relatórios de supervisão

As diretivas de supervisão definem qual communications em sua organização precisam revisão para fins de conformidade e quem executará as revisões. Use os relatórios de supervisão para ver a atividade de revisão no nível de política e revisor. Para cada diretiva, você também pode exibir live estatísticas sobre o estado atual da atividade de revisão. [Saiba mais sobre as diretivas de supervisão](configure-supervision-policies.md) . 
  
> [!NOTE]
> Usando diretivas de supervisão requer uma assinatura do Office 365 E5 para sua organização. Se você não tiver que plano e quiser tentar supervisão, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Você pode usar os relatórios de supervisão para:
  
- Verificar se as suas políticas estão funcionando conforme pretendido. 
    
- Descubra quantos emails estão sendo identificados para revisão.
    
- Descubra quantos emails não são compatíveis com e quais estão passando a revisão. Essas informações podem ajudá-lo a decidir se deseja ajustar suas políticas ou alterar o número de revisores.
    
## <a name="view-the-supervision-report"></a>Exibir o relatório de supervisão

1. Entrar no [segurança &amp; Centro de conformidade](https://protection.office.com/) usando as credenciais de uma conta de administrador em sua organização do Office 365 que tenha permissões para exibir relatórios de supervisão.. 
    
2. Vá para **relatórios** \> **painel**. Você verá um relatório widget para supervisão e outros relatórios, você tem acesso ao.
    
3. Clique em widget **supervisão** para abrir a página de relatório detalhado. 
    
> [!NOTE]
> Se você não conseguir acessar a página de **relatórios** , verifique se você for um membro do grupo de função de análise de supervisão, conforme descrito em [tornar supervisão disponível na sua organização](configure-supervision-policies.md#SRavailable). Sejam incluídos na função grupo permite que você criar e gerenciar supervisão políticas e executar o relatório. 
  
## <a name="how-to-use-the-report"></a>Como usar o relatório

Quando uma diretiva de supervisão identifica um email para revisão, o email é entregue a pasta de supervisão do revisor no Outlook e Outlook web app. Este relatório lista o nome da política de cada e o número de comunicações em cada estágio no processo de revisão.
  
Use o relatório para:
  
- Exibir dados para todos ou políticas específicas.
    
- Exibir dados agrupados por tipo de marca (por exemplo, compatível, Questionable, etc.), revisor ou tipo de mensagem.
    
- Exporte dados para um arquivo CSV.
    
- Filtre dados com base na data de revisão da atividade, tipo de marca, revisor, tipo de mensagem.
    
Aqui está uma divisão dos valores que talvez você veja na coluna **tipo de marca** . 
  
|**Tipo de marca**|**O que significa**|
|:-----|:-----|
|Não examinado  <br/> |O número de emails que ainda não foram revisadas. Esses emails são Aguardando revisão na pasta de supervisão do revisor no Outlook.  <br/> |
|Compatível com  <br/> |O número de emails revisado e marcado como compatível. Nenhuma ação adicional será necessária.  <br/> |
|Questionáveis  <br/> |O número de emails analisado e marcado questionável. Isso funciona como um sinalizador; outros revisores podem ajudar a verificar se um email precisa investigação para fins de conformidade.  <br/> |
|Incompatíveis (ativo)  <br/> |O número de emails não compatíveis que revisores estão atualmente investigando.  <br/> |
|Incompatíveis (resolvido)  <br/> |O número de emails não compatíveis que revisores investigados e resolvido.  <br/> |
   
## <a name="more-details"></a>Mais detalhes

- Diretivas de supervisão primeiro devem ser provisionadas antes que eles serão exibidos nesse relatório.
    
- Se as diretivas forem excluídas, dados históricos ainda são mostrados. No entanto, eles estiver indicados como "política inexistente" e a função **Exportar** não está disponível. 
    
- Se o relatório não mostrar todos os dados por padrão, talvez seja porque o intervalo de datas atual não tem quaisquer dados para mostrar. Nesses casos, use o controle de **filtros** para alterar o intervalo de datas. 
    


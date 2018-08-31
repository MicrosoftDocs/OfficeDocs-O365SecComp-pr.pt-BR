---
title: Definir a opção Ignorar Texto para análise na Descoberta Eletrônica Avançada do Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 44055727-56e8-42d7-9dc3-fb942f3901cc
description: 'Aprenda a definir a regra para ignorar o texto específico ao usar os módulos de analisar e processar no eDiscovery avançadas do Office 365.  '
ms.openlocfilehash: eb7e7052979087b7dba98aac3b0c9ab75ec0d02a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524098"
---
# <a name="set-ignore-text-option-for-analyze-in-office-365-advanced-ediscovery"></a>Definir a opção Ignorar Texto para análise na Descoberta Eletrônica Avançada do Office 365

> [!NOTE]
> EDiscovery Avançado requer um Office 365 E3 com o complemento de conformidade avançadas ou uma assinatura E5 para sua organização. Se você não tiver que plano e quiser tentar eDiscovery avançado, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
O recurso Ignorar texto pode ser aplicado a todos ou qualquer um dos seguintes módulos avançados eDiscovery: analisar (temas de Threads de Email, perto de duplicatas) e a relevância. Texto ignorado não aparecerá na arquivos exibidos em relevância e os cálculos de análise/descartará o texto ignorado.
  
Se o recurso Ignorar texto foi definido anteriormente para módulos que já foi executado, a configuração Ignorar texto agora estará protegida contra modificação. No entanto, o recurso de ignorar o texto para o módulo de relevância ainda pode ser alterado a qualquer momento.
  
## <a name="how-ignore-text-filters-are-applied"></a>Como Ignorar texto filtros são aplicados

Vários filtros Ignorar texto são aplicados na ordem em que foram inseridos. Para alterar a ordem na qual elas serão aplicadas, eles devem ser excluídos e entrado novamente na ordem desejada.
  
Por exemplo, se o conteúdo de texto é: "DAVE BOB ALICE CAROL noite", a seguir estão exemplos de entradas de ignorar o texto e os resultados:
  
||||
|:-----|:-----|:-----|
|**Ignorar as entradas de texto** <br/> |**==\>** <br/> |**Resultados** <br/> |
|"ALICE", "BOB CAROL"  <br/> |==\>  <br/> |"DAVE NOITE"  <br/> |
|"ALICE", "BOB ALICE CAROL"  <br/> |==\>  <br/> |"DAVE BOB CAROL NOITE"  <br/> |
   
A segunda entrada de texto ignorar não está implementada porque a cadeia de caracteres não for encontrada como tal, após o primeiro texto ignorar tiver sido aplicado.
  
## <a name="use-regular-expressions-when-defining-ignore-text"></a>Usar expressões regulares ao definir Ignorar texto

Expressões regulares são compatíveis para uso ao definir Ignorar texto. A seguir está exemplos de uso e a sintaxe de expressão regular:
  
- Para remover (ignorar) o texto de Begin até o final de uma linha:
    
     `Begin(.*)$`
    
    onde "Begin" é a ocorrência inicial dessa cadeia de caracteres na linha.
    
    Por exemplo, para o seguinte texto:
    
    **"Este é primeira frase e a primeira linha**
    
    **Esta é a segunda frase e a segunda linha"**
    
    a expressão Regular first(.\*) $ resultará em:
    
    **"Este é**
    
    **Esta é a segunda frase e a segunda linha"**
    
- Para remover os avisos de isenção e declarações jurídicas automaticamente inseridas no fim de threads de email:
    
     `Begin(.|\s)*End`
    
    onde "Begin" e "End" são cadeias de caracteres exclusivas no início e no final de um parágrafo do texto quebrado automaticamente. 
    
    Por exemplo, a seguinte expressão regular e serão removidos avisos de isenção legais instruções que estavam no segmento de email entre as cadeias de caracteres Begin e End:
    
    **Esta mensagem contém informações confidenciais (. | \s)\*se é necessária uma verificação solicite uma versão impresso**
    
- Para remover um aviso de isenção (incluindo caracteres especiais): 
    
    Por exemplo, para o seguinte texto (com a isenção de responsabilidade representado aqui por xx): 
    
    **/\*\ Esta mensagem contém informações confidenciais. xxxx xxxx**
    
    **xxxx xxxx xxxx xxxx xxxx xxxx xxxx**
    
    **xxxx xxxx se verificação for necessária, solicite uma versão impresso. /\*\**
    
    a expressão regular para remover a isenção de responsabilidade acima deve ser: 
    
    **\/\\*\\Esta mensagem contém informações confidenciais\.(. | \s)\* se é necessária uma verificação solicite uma versão impresso\.\/\\*\\**
    
- Regras de expressão regular:
    
  - Quaisquer caracteres que não fazem parte do alfabeto, com exceção de espaço (s), "_" e "-" deve ser precedido por "\".
    
  - O campo eExpression regular pode ser comprimento ilimitado.
    
> [!TIP]
> Para obter uma explicação e detalhadas sobre sintaxe das expressões regulares, consulte: [Linguagem de expressão Regular - referência rápida](https://msdn.microsoft.com/en-us/library/az24scfc%28v=vs.110%29.aspx). 
  
## <a name="define-ignore-text-rule"></a>Definir texto Ignorar regra

1. No **Gerenciar \> analisar \> analisar opções** guia, na seção **Ignorar texto** , clique no **+** ícone para adicionar uma regra. 
    
2. Na caixa de diálogo **Adicionar texto ignorar** , no campo **nome** , digite um nome para a regra Ignorar texto. 
    
    ![Adicionar texto ignorado](media/98e5129b-2667-4692-86fa-2d0117187a7f.png)
  
3. Na caixa de **texto** , digite o texto a ser ignorado. O campo texto permite que um número ilimitado de caracteres. 
    
    > [!TIP]
    > Conforme mostrado na janela acima, clique em **lâmpada** para ver as diretrizes de sintaxe comuns para a regra Ignorar texto. 
  
4. Marque a caixa de seleção **Diferenciar maiusculas de minúsculas** , se desejado. 
    
5. Na lista **Aplicar a** , selecione os módulos de descoberta eletrônica avançada na qual aplicar a definição. 
    
6. Se você quiser um execução de teste em texto de exemplo, digite o texto de exemplo na caixa de texto de **entrada** e clique em **Testar**. Os resultados são exibidos na caixa de texto de **saída** . 
    
7. Clique em **Okey** para salvar a regra Ignorar texto. A regra de Ignorar texto definida é exibida. 
    
    ![Definir nome de texto ignorado](media/3a788ac3-4a1c-46c9-89bd-7ff32d68ce23.png)
  
## <a name="see-also"></a>Confira também

[Descoberta Eletrônica Avançada do Office 365](office-365-advanced-ediscovery.md)
  
[Noções básicas sobre semelhança de documento](understand-document-similarity-in-advanced-ediscovery.md)
  
[Definindo opções de analisar](set-analyze-options-in-advanced-ediscovery.md)
  
[Analisar configuração configurações avançada](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[Exibindo os resultados da análise](view-analyze-results-in-advanced-ediscovery.md)


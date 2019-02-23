---
title: Entender similaridade de documentos na Descoberta Eletrônica Avançada do Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 4d4cb381-4c9a-4165-a455-609d525c7a88
description: 'Revise como o valor de similaridade do documento, o nível mínimo de aparência de dois arquivos a serem considerados próximos duplicados, funciona na descoberta eletrônica avançada do Office 365. '
ms.openlocfilehash: eb8f07ceedb10bd0152693dd1e82a28797d86a5a
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220421"
---
# <a name="understand-document-similarity-in-office-365-advanced-ediscovery"></a>Entender similaridade de documentos na Descoberta Eletrônica Avançada do Office 365

> [!NOTE]
> A Descoberta Eletrônica Avançada exige um Office 365 E3, com um complemento de Conformidade Avançada ou uma assinatura do E5 para sua organização. Se você não tiver esse plano e quiser tentar a Descoberta Eletrônica Avançada, poderá [Inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Na descoberta eletrônica avançada, a similaridade de documentos é o nível mínimo de aparência necessária para dois documentos a serem considerados como duplicatas.
  
> [!TIP]
> Para a maioria dos aplicativos de negócios, é recomendável usar um valor de similaridade de 60% a 75%. Para material de reconhecimento óptico de caracteres (OCR) de qualidade muito ruim, valores de similaridade menores podem ser aplicados. 
  
> [!NOTE]
> Após a definição e a execução de um determinado caso, o valor de similaridade não pode ser alterado. 
  
Dentro de um conjunto Near-Duplicate (ND), pode haver documentos com um nível de aparência abaixo do limite de similaridade. Para que um documento ingresse em um conjunto de ND, deve haver pelo menos um documento no conjunto de ND com um nível de semelhante. 
  
Por exemplo, suponha que a similaridade seja definida como 80%, o documento F1 se parece com o documento F2 em um nível de 85%, e o documento F2 é parecido com o documento F3 em um nível de 90%. 
  
No enTanto, o documento F1 pode se parecer com o documento F3 em um nível de apenas 70%, o que está abaixo do limite. No enTanto, neste exemplo, os documentos F1, F2 e F3 aparecem no conjunto de um. Da mesma forma, usando um valor de similaridade de 80%, podemos criar dois conjuntos, EquiSet-1 e EquiSet-2. EquiSet-1 contém documentos E1 e E2. Equiset-2 contém documentos F1, F2 e F3. 
  
Os níveis de semelhança são ilustrados da seguinte maneira:
  
![Similaridade de documentos](media/3907ea7d-e28a-4027-8fc3-be090dd39144.gif)
  
Suponha que outro documento, x1, agora seja inserido. A semelhança entre X1 e E3 é de 87%. Da mesma forma, a semelhança entre X1 e F1 é de 92%. Como resultado, EquiSet-1, EquiSet-2 e X1 agora são combinados em um conjunto de ND.
  
![Similaridade de documentos](media/d140d347-33d5-475a-af04-594a0f2ab13d.gif)
  
> [!NOTE]
> Se houver dois documentos atribuídos a um conjunto de ND, eles permanecerão juntos no mesmo conjunto de ND, mesmo se os documentos adicionais forem adicionados ao conjunto ou se os conjuntos forem mesclados. 
  
Após a mesclagem dos conjuntos, o documento dinâmico pode ser alterado quando novos documentos são adicionados a um conjunto. 
  
## <a name="see-also"></a>Confira também

[Descoberta Eletrônica Avançada do Office 365](office-365-advanced-ediscovery.md)
  
[Configuração das opções de análise](set-analyze-options-in-advanced-ediscovery.md)
  
[Configuração ignorar texto](set-ignore-text-in-advanced-ediscovery.md)
  
[Configuração analisar configurações avançadas](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[Exibindo resultados de análise](view-analyze-results-in-advanced-ediscovery.md)


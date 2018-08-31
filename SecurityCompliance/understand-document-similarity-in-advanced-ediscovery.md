---
title: Entender similaridade de documentos na Descoberta Eletrônica Avançada do Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 4d4cb381-4c9a-4165-a455-609d525c7a88
description: 'Revise o funcionamento do documento semelhança valor, o nível mínimo de semelhança para dois arquivos a serem considerados perto duplicatas no eDiscovery avançadas do Office 365. '
ms.openlocfilehash: 39cd8c31204f0164f6b52c71fa707253cb22758a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523885"
---
# <a name="understand-document-similarity-in-office-365-advanced-ediscovery"></a>Entender similaridade de documentos na Descoberta Eletrônica Avançada do Office 365

> [!NOTE]
> EDiscovery Avançado requer um Office 365 E3 com o complemento de conformidade avançadas ou uma assinatura E5 para sua organização. Se você não tiver que plano e quiser tentar eDiscovery avançado, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
No eDiscovery avançado, semelhança de documento é o nível mínimo de semelhança necessário para dois documentos a serem considerados como perto duplicatas.
  
> [!TIP]
> Para a maioria dos aplicativos de negócios, é recomendável usar um valor de semelhança de 60% - 75%. Para material de reconhecimento óptico de caracteres (OCR) de péssima qualidade, valores de semelhança menores podem ser aplicados. 
  
> [!NOTE]
> Depois que ele tiver sido definida e executar para um determinado caso, o valor de semelhança não pode ser alterado. 
  
Em um conjunto de duplicados Near (fim), pode haver documentos com um nível de semelhança abaixo do limiar de semelhança. Para um documento ingressar em um conjunto de término, deve haver pelo menos um documento no término definidas com um nível de semelhança excedendo a semelhança. 
  
Por exemplo, suponha a semelhança estiver definida como 80%, F1 do documento se parece com o documento F2 em um nível de 85% e documento F2 se parece com o documento F3 em um nível de 90%. 
  
No entanto, documento F1 pode se parecer com o documento F3 em um nível de apenas 70%, que está abaixo do limiar. No entanto, neste exemplo, documentos F1, F2 e F3 todos serão exibidos no término de um definido. Da mesma forma, usando um valor de semelhança de 80%, talvez criamos dois conjuntos, EquiSet-1 e EquiSet-2. EquiSet-1 contém documentos E1 e E2. Equiset-2 contém documentos F1, F2 e F3. 
  
Os níveis de semelhança são ilustrados da seguinte maneira:
  
![Similaridade de documentos](media/3907ea7d-e28a-4027-8fc3-be090dd39144.gif)
  
Suponha que a outro documento, X1, agora é inserido. A semelhança entre X1 e E3 é 87%. Da mesma forma, a semelhança entre X1 e F1 é 92%. Como resultado, o EquiSet -1, EquiSet -2 e X1 agora são combinados em um término definido.
  
![Similaridade de documentos](media/d140d347-33d5-475a-af04-594a0f2ab13d.gif)
  
> [!NOTE]
> Se qualquer dois documentos são atribuídos a um conjunto de término, eles permanecerão juntos no mesmo conjunto de término, mesmo se adicionais os documentos são adicionados ao conjunto ou se os conjuntos são mesclados. 
  
Depois que forem mesclados conjuntos, o documento Pivot pode alterar quando novos documentos forem adicionados a um conjunto. 
  
## <a name="see-also"></a>Confira também

[Descoberta Eletrônica Avançada do Office 365](office-365-advanced-ediscovery.md)
  
[Definindo opções de analisar](set-analyze-options-in-advanced-ediscovery.md)
  
[Configuração Ignorar texto](set-ignore-text-in-advanced-ediscovery.md)
  
[Analisar configuração configurações avançada](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[Exibindo os resultados da análise](view-analyze-results-in-advanced-ediscovery.md)


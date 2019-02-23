---
title: Definir configurações avançadas de análise na Descoberta Eletrônica Avançada do Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a797682f-ad85-4c08-a354-3850ba2237ee
description: 'Saiba como definir configurações avançadas, incluindo duplicatas, threads de email e temas, para o processo de análise na descoberta eletrônica avançada do Office 365. '
ms.openlocfilehash: d8dfb9f3ecfcda0f267dfccdc716eda40fe450b2
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220081"
---
# <a name="set-analyze-advanced-settings-in-office-365-advanced-ediscovery"></a>Definir configurações avançadas de análise na Descoberta Eletrônica Avançada do Office 365

> [!NOTE]
> A Descoberta Eletrônica Avançada exige um Office 365 E3, com um complemento de Conformidade Avançada ou uma assinatura do E5 para sua organização. Se você não tiver esse plano e quiser tentar a Descoberta Eletrônica Avançada, poderá [Inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
A descoberta eletrônica avançada fornece parâmetros avançados padrão para analisar configurações de módulo. O procedimento a seguir descreve as configurações que podem ser especificadas.
  
1. Na guia **preparar \> configuração \> de análise** , clique em **Configurações avançadas** (na parte inferior da página). O painel a seguir é exibido. 
    
    ![Definir as configurações avançadas de análise](media/c9ea3017-e19a-456b-a742-c3d07121a3f6.png)
  
2. Em **parâmetros Near-Duplicate e threads de email**, selecione valores para os seguintes, conforme necessário:
    
  - **Número mínimo de palavras**: o número mínimo de palavras, abaixo do qual um arquivo não é enviado para análise quase duplicada. 
    
  - **Número máximo de palavras**: número máximo de palavras, acima do qual um arquivo não é enviado para análise quase duplicada.
    
  - **Similaridade de email**: nível mínimo de aparência de dois emails a serem considerados semelhantes. O valor é sempre igual ou maior que a similaridade de documentos. O padrão é 90%.
    
3. Em **parâmetros de temas**, marque a caixa de seleção **incluir números na análise de temas** para incluir números no processamento de temas durante a análise. 
    
4. Clique em **Salvar**. 
    
## <a name="see-also"></a>Confira também

[Descoberta Eletrônica Avançada do Office 365](office-365-advanced-ediscovery.md)
  
[Noções básicas sobre a similaridade de documentos](understand-document-similarity-in-advanced-ediscovery.md)
  
[Configuração das opções de análise](set-analyze-options-in-advanced-ediscovery.md)
  
[Configuração ignorar texto](set-ignore-text-in-advanced-ediscovery.md)
  
[Exibindo resultados de análise](view-analyze-results-in-advanced-ediscovery.md)


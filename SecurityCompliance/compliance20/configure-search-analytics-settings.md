---
title: Definir as configurações de pesquisa e análise
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
ms.openlocfilehash: d9528a4bcfaa77f2e232b25d03eda46cce42ebb9
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607331"
---
# <a name="configure-search-and-analytics-settings"></a>Definir as configurações de pesquisa e análise


## <a name="near-duplicates-and-email-threading"></a>Quase duplicatas e email threading

Nesta seção, você pode definir parâmetros para detecção de duplicatas, perto de detecção de duplicatas e threading de email.

- Habilitar/desabilitar: inclua a detecção de duplicatas, perto de detecção de duplicatas e email threading como parte do fluxo de análise se habilitado. Porque eles criarem na parte superior de umas às outras, você deve habilitar todos eles ou desabilitar todos eles.

- Limite: se o nível de semelhança de dois documentos acima do limite, eles serão colocados no mesmo perto conjunto duplicado.

- Ocultar duplicatas por padrão: se essa configuração estiver ligado, um filtro para ocultar documentos duplicados será aplicado em trabalhar definido por padrão. O filtro pode ser removido manualmente no trabalho definido, se necessário.

- Número mínimo/máximo de palavras: perto duplicatas e email threading será executado somente em documentos que tenham pelo menos o número mínimo de palavras e no máximo o número máximo de palavras. Para obter mais informações, consulte [perto de detecção de duplicatas](near-duplicates.md) e [threading de Email](email-threading.md).

## <a name="themes"></a>Temas

Nesta seção, você pode definir parâmetros para temas.

- Habilitar/desabilitar: incluem temas clustering como parte do fluxo de análise se habilitado.
- Ajustar o número máximo de temas dinamicamente dinamicamente: em certos casos, não há documentos suficiente para produzir o número desejado de temas. Se essa configuração estiver ativada, em seguida, em vez de tentar forçar o número máximo desejado de temas, o sistema ajusta o número máximo de temas dinamicamente.
- Número máximo de temas: desejado o número de temas
- Incluir números em temas: Quando habilitada, ela incluirá números em ao gerar temas.  

## <a name="optical-character-recognition-ocr"></a>Reconhecimento óptico de caracteres (OCR)

Quando essa configuração é ativada, OCR será executada em imagens que são incluídas em conjuntos de trabalho para que eles possam ser pesquisáveis.

## <a name="ignore-text"></a>Ignorar texto

Há instâncias onde determinados textos reduzirá a qualidade da análise, como avisos de isenção longos que obtém adicionados a determinados emails independentemente do conteúdo do email. Se você estiver ciente nesses casos, você pode excluir esse texto do analytics especificando-se o texto (RegEx é suportada) e qual módulos de texto deve ser excluído para.
---
title: Definir configurações de pesquisa e análise
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 5aa83f4f736c239b1cdfe940f27cfaa4b981ff64
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155113"
---
# <a name="configure-search-and-analytics-settings"></a>Definir configurações de pesquisa e análise


## <a name="near-duplicates-and-email-threading"></a>Duplicados próximos e threads de email

Nesta seção, você pode definir parâmetros para detecção de duplicidades, detecção de duplicidade próxima e thread de email.

- Enable/disable: incluir a detecção de duplicidades, a detecção de duplicidade próxima e o encadeamento de email como parte do fluxo de análise, se habilitado. Como eles se baseiam uns dos outros, você deve habilitar todos eles ou desabilitá-los.

- Limite: se o nível de similaridade de dois documentos estiver acima do limite, ele será colocado no mesmo conjunto próximo duplicado.

- Ocultar duplicatas por padrão: se essa configuração estiver ativada, um filtro para ocultar documentos duplicados será aplicado na análise definida por padrão. O filtro pode ser removido manualmente no conjunto de revisão, se necessário.

- Número mínimo/máximo de palavras: próximas duplicatas e o encadeamento de emails será executado somente em documentos que tenham pelo menos o número mínimo de palavras e, no máximo, o número máximo de palavras.
Para obter mais informações, consulte [Near Duplicate](near-duplicates.md) Detection and [e-mail Threading](email-threading.md).

## <a name="themes"></a>Temas

Nesta seção, você pode definir parâmetros para temas.

- Enable/disable: incluir agrupamento de temas como parte do fluxo de análise, se habilitado.
- Ajustar o número máximo de temas dinamicamente dinamicamente: em certos casos, não há documentos suficientes para produzir o número desejado de temas. Se essa configuração estiver ativada, em vez de tentar forçar o número máximo de temas desejado, o sistema ajustará o número máximo de temas dinamicamente.
- Número máximo de temas: número desejado de temas
- Incluir números em temas: quando habilitado, ele incluirá números ao gerar temas.  

## <a name="optical-character-recognition-ocr"></a>Reconhecimento óptico de caracteres (OCR)

Quando essa configuração estiver ativada, o OCR será executado em imagens que são incluídas nos conjuntos de revisão para que possam ser pesquisadas.

## <a name="ignore-text"></a>Ignorar texto

Há situações em que determinados textos reduzirão a qualidade da análise, como avisos de isenção de responsabilidade longos que são adicionados a certos emails, independentemente do conteúdo do email. Se você estiver ciente desses casos, poderá excluir esse texto da análise especificando o texto (RegEx é suportado) e de quais módulos o texto deve ser excluído.
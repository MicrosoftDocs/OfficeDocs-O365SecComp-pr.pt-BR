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
# <a name="configure-search-and-analytics-settings"></a><span data-ttu-id="49582-102">Definir as configurações de pesquisa e análise</span><span class="sxs-lookup"><span data-stu-id="49582-102">Configure search and analytics settings</span></span>


## <a name="near-duplicates-and-email-threading"></a><span data-ttu-id="49582-103">Quase duplicatas e email threading</span><span class="sxs-lookup"><span data-stu-id="49582-103">Near duplicates and email threading</span></span>

<span data-ttu-id="49582-104">Nesta seção, você pode definir parâmetros para detecção de duplicatas, perto de detecção de duplicatas e threading de email.</span><span class="sxs-lookup"><span data-stu-id="49582-104">In this section, you can set parameters for duplicate detection, near duplicate detection, and email threading.</span></span>

- <span data-ttu-id="49582-p101">Habilitar/desabilitar: inclua a detecção de duplicatas, perto de detecção de duplicatas e email threading como parte do fluxo de análise se habilitado. Porque eles criarem na parte superior de umas às outras, você deve habilitar todos eles ou desabilitar todos eles.</span><span class="sxs-lookup"><span data-stu-id="49582-p101">Enable/disable: include duplicate detection, near duplicate detection, and email threading as part of analytics flow if enabled. Because they build on top of each other, you must enable all of them or disable all of them.</span></span>

- <span data-ttu-id="49582-107">Limite: se o nível de semelhança de dois documentos acima do limite, eles serão colocados no mesmo perto conjunto duplicado.</span><span class="sxs-lookup"><span data-stu-id="49582-107">Threshold: if the similarity level of two documents are above the threshold, they will be put in the same near duplicate set.</span></span>

- <span data-ttu-id="49582-p102">Ocultar duplicatas por padrão: se essa configuração estiver ligado, um filtro para ocultar documentos duplicados será aplicado em trabalhar definido por padrão. O filtro pode ser removido manualmente no trabalho definido, se necessário.</span><span class="sxs-lookup"><span data-stu-id="49582-p102">Hide duplicates by default: if this setting is on, a filter to hide duplicate documents will be applied in the working set by default. The filter can be removed manually in the working set if necessary.</span></span>

- <span data-ttu-id="49582-p103">Número mínimo/máximo de palavras: perto duplicatas e email threading será executado somente em documentos que tenham pelo menos o número mínimo de palavras e no máximo o número máximo de palavras. Para obter mais informações, consulte [perto de detecção de duplicatas](near-duplicates.md) e [threading de Email](email-threading.md).</span><span class="sxs-lookup"><span data-stu-id="49582-p103">Minimum/maximum number of words: near duplicates and email threading will run only on documents that have at least the minimum number of words and at most the maximum number of words. For more information, see [Near duplicate detection](near-duplicates.md) and [Email threading](email-threading.md).</span></span>

## <a name="themes"></a><span data-ttu-id="49582-112">Temas</span><span class="sxs-lookup"><span data-stu-id="49582-112">Themes</span></span>

<span data-ttu-id="49582-113">Nesta seção, você pode definir parâmetros para temas.</span><span class="sxs-lookup"><span data-stu-id="49582-113">In this section, you can set parameters for themes.</span></span>

- <span data-ttu-id="49582-114">Habilitar/desabilitar: incluem temas clustering como parte do fluxo de análise se habilitado.</span><span class="sxs-lookup"><span data-stu-id="49582-114">Enable/disable: include themes clustering as part of analytics flow if enabled.</span></span>
- <span data-ttu-id="49582-p104">Ajustar o número máximo de temas dinamicamente dinamicamente: em certos casos, não há documentos suficiente para produzir o número desejado de temas. Se essa configuração estiver ativada, em seguida, em vez de tentar forçar o número máximo desejado de temas, o sistema ajusta o número máximo de temas dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="49582-p104">Adjust maximum number of themes dynamically dynamically: in certain cases, there are not enough documents to produce the desired number of themes. If this setting is turned on, then rather than trying to force the desired maximum number of themes, the system adjusts maximum number of themes dynamically.</span></span>
- <span data-ttu-id="49582-117">Número máximo de temas: desejado o número de temas</span><span class="sxs-lookup"><span data-stu-id="49582-117">Maximum number of themes: desired number of themes</span></span>
- <span data-ttu-id="49582-118">Incluir números em temas: Quando habilitada, ela incluirá números em ao gerar temas.</span><span class="sxs-lookup"><span data-stu-id="49582-118">Include numbers in themes: When enabled, it will include numbers in when generating themes.</span></span>  

## <a name="optical-character-recognition-ocr"></a><span data-ttu-id="49582-119">Reconhecimento óptico de caracteres (OCR)</span><span class="sxs-lookup"><span data-stu-id="49582-119">Optical character recognition (OCR)</span></span>

<span data-ttu-id="49582-120">Quando essa configuração é ativada, OCR será executada em imagens que são incluídas em conjuntos de trabalho para que eles possam ser pesquisáveis.</span><span class="sxs-lookup"><span data-stu-id="49582-120">When this setting is turned on, OCR will be run on images that are ingested into working sets so that they can be searchable.</span></span>

## <a name="ignore-text"></a><span data-ttu-id="49582-121">Ignorar texto</span><span class="sxs-lookup"><span data-stu-id="49582-121">Ignore text</span></span>

<span data-ttu-id="49582-p105">Há instâncias onde determinados textos reduzirá a qualidade da análise, como avisos de isenção longos que obtém adicionados a determinados emails independentemente do conteúdo do email. Se você estiver ciente nesses casos, você pode excluir esse texto do analytics especificando-se o texto (RegEx é suportada) e qual módulos de texto deve ser excluído para.</span><span class="sxs-lookup"><span data-stu-id="49582-p105">There are instances where certain texts will diminish the quality of analytics, such as lengthy disclaimers that get added to certain emails regardless of the content of the email. If you are aware of such cases, you can exclude this text from analytics by specifying the text (RegEx is supported) and which modules that text should be excluded for.</span></span>
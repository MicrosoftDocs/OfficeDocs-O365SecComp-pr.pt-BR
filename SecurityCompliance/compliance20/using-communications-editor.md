---
title: Use o editor de comunicações
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
ms.openlocfilehash: b148ff1a77cd9225a26f98e7612e9fb5b57331e3
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29706052"
---
# <a name="use-the-communications-editor"></a><span data-ttu-id="752dd-102">Use o editor de comunicações</span><span class="sxs-lookup"><span data-stu-id="752dd-102">Use the communications editor</span></span>

<span data-ttu-id="752dd-103">Conforme você define o conteúdo de seu conteúdo de portal, legais segure notificações e lembretes/escalonamentos relacionados, você pode aproveitar o Editor de comunicações para formatar e personalizar dinamicamente seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="752dd-103">As you define the content of your portal content, legal hold notifications, and related reminders/escalations, you can leverage the Communications Editor to format and dynamically customize your content.</span></span>

## <a name="rich-text-editor"></a><span data-ttu-id="752dd-104">Editor de rich text</span><span class="sxs-lookup"><span data-stu-id="752dd-104">Rich text editor</span></span> 

<span data-ttu-id="752dd-p101">O Editor de comunicações permite que o usuário personalize o texto usando as opções de editor. Por exemplo, os usuários podem alterar os tipos de fonte, criar listas com marcadores, realce conteúdo e mais.</span><span class="sxs-lookup"><span data-stu-id="752dd-p101">The Communications Editor allows user to customize the text using the editor options. For example, users can change font types, create bulleted lists, highlight content, and more.</span></span> 

## <a name="merge-field-variables"></a><span data-ttu-id="752dd-107">Variáveis de campo de mesclagem</span><span class="sxs-lookup"><span data-stu-id="752dd-107">Merge field variables</span></span>

<span data-ttu-id="752dd-p102">Você pode aproveitar as variáveis de mesclagem email no Editor de comunicações para incorporar os atributos dos responsáveis personalizada no corpo de texto de uma comunicação. Quando enviado para dos responsáveis, o campo de mesclagem será preenchido com o campo correspondente. Por exemplo, quando enviado para dos responsáveis John Smith, o campo de mesclagem [nome dos responsáveis] seria convertido com o nome correspondente.</span><span class="sxs-lookup"><span data-stu-id="752dd-p102">You can leverage email merge variables from the Communications Editor to embed customized custodian attributes into a communication's body text. When sent to the custodian, the merge field will be populated with the corresponding field. For example, when sent to custodian John Smith, the merge field [Custodian Name] would be translated with the corresponding name.</span></span> 

<span data-ttu-id="752dd-p103">Você pode usar os campos de mesclagem email selecionando os ícones de **campo de mala direta** na parte superior do controle de editor de rich text. O espaço reservado será adicionado com base desativa a localização do cursor dos usuários.</span><span class="sxs-lookup"><span data-stu-id="752dd-p103">You can use email merge fields by selecting the **Merge field** icons on the top of the rich-text editor control. The placeholder will be added based off the location of the users' cursor.</span></span> 

### <a name="list-of-merge-field-variables"></a><span data-ttu-id="752dd-113">Lista de variáveis de campo de mala direta</span><span class="sxs-lookup"><span data-stu-id="752dd-113">List of merge field variables</span></span>

| <span data-ttu-id="752dd-114">Nome do campo</span><span class="sxs-lookup"><span data-stu-id="752dd-114">Field name</span></span>                  | <span data-ttu-id="752dd-115">Detalhes do campo</span><span class="sxs-lookup"><span data-stu-id="752dd-115">Field details</span></span> | 
| :------------------- | :------------------- |
| <span data-ttu-id="752dd-116">Nome para Exibição</span><span class="sxs-lookup"><span data-stu-id="752dd-116">Display Name</span></span>  | <span data-ttu-id="752dd-117">Dos responsáveis pela primeira vez e o último nome.</span><span class="sxs-lookup"><span data-stu-id="752dd-117">The custodian's first and last name.</span></span> | 
| <span data-ttu-id="752dd-118">Link de confirmação</span><span class="sxs-lookup"><span data-stu-id="752dd-118">Acknowledgement Link</span></span> | <span data-ttu-id="752dd-119">Um link personalizado para registrar a confirmação da cada responsável.</span><span class="sxs-lookup"><span data-stu-id="752dd-119">A customized link to record each custodian's acknowledgement.</span></span>|                 |
| <span data-ttu-id="752dd-120">Link de portal</span><span class="sxs-lookup"><span data-stu-id="752dd-120">Portal Link</span></span>     | <span data-ttu-id="752dd-121">Um link personalizado para Portal do dos responsáveis de conformidade.</span><span class="sxs-lookup"><span data-stu-id="752dd-121">A customized link for the custodian's Compliance Portal.</span></span>|                |
| <span data-ttu-id="752dd-122">Responsável pela emissora</span><span class="sxs-lookup"><span data-stu-id="752dd-122">Issuing Officer</span></span>                   | <span data-ttu-id="752dd-123">O endereço de email do responsável pela emissora especificado.</span><span class="sxs-lookup"><span data-stu-id="752dd-123">The email address of the specified issuing officer.</span></span>|                   |
| <span data-ttu-id="752dd-124">Data de emissão</span><span class="sxs-lookup"><span data-stu-id="752dd-124">Issuing Date</span></span>                   | <span data-ttu-id="752dd-125">A data em que o aviso foi emitido (UTC).</span><span class="sxs-lookup"><span data-stu-id="752dd-125">The date that the notice was issued (UTC).</span></span>              |
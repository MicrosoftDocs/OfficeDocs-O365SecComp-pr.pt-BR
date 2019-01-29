---
title: Usando o editor de comunicações
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
ms.openlocfilehash: 107f45510bcf70942c6f03bdfed0a9090f1d83c0
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607341"
---
# <a name="using-the-communications-editor"></a><span data-ttu-id="da966-102">Usando o Editor de comunicações</span><span class="sxs-lookup"><span data-stu-id="da966-102">Using the Communications Editor</span></span>
<span data-ttu-id="da966-103">Conforme você define o conteúdo de seu conteúdo de portal, legais segure notificações e lembretes/escalonamentos relacionados, você pode aproveitar o Editor de comunicações para formatar e personalizar dinamicamente seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="da966-103">As you define the content of your portal content, legal hold notifications, and related reminders/escalations, you can leverage the Communications Editor to format and dynamically customize your content.</span></span>

## <a name="rich-text-editor"></a><span data-ttu-id="da966-104">Editor de Rich Text</span><span class="sxs-lookup"><span data-stu-id="da966-104">Rich-Text Editor</span></span> 

<span data-ttu-id="da966-p101">O Editor de comunicações permite que o usuário personalize o texto usando as opções de editor. Por exemplo, os usuários podem alterar os tipos de fonte, criar listas com marcadores, realce conteúdo e mais.</span><span class="sxs-lookup"><span data-stu-id="da966-p101">The Communications Editor allows user to customize the text using the editor options. For example, users can change font types, create bulleted lists, highlight content, and more.</span></span> 

<<include screenshot>>

## <a name="merge-field-variables"></a><span data-ttu-id="da966-107">Variáveis de campo de mesclagem</span><span class="sxs-lookup"><span data-stu-id="da966-107">Merge Field Variables</span></span>

<span data-ttu-id="da966-p102">Você pode aproveitar as variáveis de mesclagem email no Editor de comunicações para incorporar os atributos dos responsáveis personalizada no corpo de texto de uma comunicação. Quando enviado para dos responsáveis, o campo de mesclagem será preenchido com o campo correspondente. Por exemplo, quando enviado para dos responsáveis John Smith, o campo de mesclagem [nome dos responsáveis] seria convertido com o nome correspondente.</span><span class="sxs-lookup"><span data-stu-id="da966-p102">You can leverage email merge variables from the Communications Editor to embed customized custodian attributes into a communication's body text. When sent to the custodian, the merge field will be populated with the corresponding field. For example, when sent to custodian John Smith, the merge field [Custodian Name] would be translated with the corresponding name.</span></span> 

<span data-ttu-id="da966-p103">Você pode usar os campos de mesclagem email selecionando os ícones de **Campo de mala direta** na parte superior do controle de editor de rich text. O espaço reservado será adicionado com base desativa a localização do cursor dos usuários.</span><span class="sxs-lookup"><span data-stu-id="da966-p103">You can use email merge fields by selecting the **Merge Field** icons on the top of the rich-text editor control. The placeholder will be added based off the location of the users' cursor.</span></span> 

### <a name="list-of-merge-field-variables"></a><span data-ttu-id="da966-113">Lista de variáveis de campo de mala direta</span><span class="sxs-lookup"><span data-stu-id="da966-113">List of Merge Field Variables</span></span>
| <span data-ttu-id="da966-114">Nome do campo</span><span class="sxs-lookup"><span data-stu-id="da966-114">Field Name</span></span>                  | <span data-ttu-id="da966-115">Detalhes do campo</span><span class="sxs-lookup"><span data-stu-id="da966-115">Field Details</span></span> | 
| :------------------- | :-------------------: |
| <span data-ttu-id="da966-116">Nome para Exibição</span><span class="sxs-lookup"><span data-stu-id="da966-116">Display Name</span></span>  | <span data-ttu-id="da966-117">Dos responsáveis e sobrenome nome</span><span class="sxs-lookup"><span data-stu-id="da966-117">Custodian's first and last name</span></span> | 
| <span data-ttu-id="da966-118">Link de confirmação</span><span class="sxs-lookup"><span data-stu-id="da966-118">Acknowledgement Link</span></span>                 | <span data-ttu-id="da966-119">Link personalizado para registrar a confirmação da cada responsável</span><span class="sxs-lookup"><span data-stu-id="da966-119">Customized link to record each custodian's acknowledgement</span></span>                 |
| <span data-ttu-id="da966-120">Link de portal</span><span class="sxs-lookup"><span data-stu-id="da966-120">Portal Link</span></span>     | <span data-ttu-id="da966-121">Link personalizado para Portal do dos responsáveis de conformidade</span><span class="sxs-lookup"><span data-stu-id="da966-121">Customized link for the custodian's Compliance Portal</span></span>                 |
| <span data-ttu-id="da966-122">Responsável pela emissora</span><span class="sxs-lookup"><span data-stu-id="da966-122">Issuing Officer</span></span>                   | <span data-ttu-id="da966-123">Endereço de email do responsável pela emissora especificado</span><span class="sxs-lookup"><span data-stu-id="da966-123">Email address of the specified issuing officer</span></span>                   |
| <span data-ttu-id="da966-124">Data de emissão</span><span class="sxs-lookup"><span data-stu-id="da966-124">Issuing Date</span></span>                   | <span data-ttu-id="da966-125">Data em que o aviso foi emitido (UTC)</span><span class="sxs-lookup"><span data-stu-id="da966-125">date that the notice was issued (UTC)</span></span>              |
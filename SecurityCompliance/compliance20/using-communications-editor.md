---
title: Usar o editor de comunicações
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: c2957c88217bce4c9a34f8d3f9a9e291f1223cc9
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30294964"
---
# <a name="use-the-communications-editor"></a><span data-ttu-id="8e1b2-102">Usar o editor de comunicações</span><span class="sxs-lookup"><span data-stu-id="8e1b2-102">Use the communications editor</span></span>

<span data-ttu-id="8e1b2-103">À medida que você define o conteúdo do seu conteúdo de portal, as notificações de retenção legal e lembretes/rementeções relacionados, você pode aproveitar o editor de comunicações para formatar e personalizar dinamicamente o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="8e1b2-103">As you define the content of your portal content, legal hold notifications, and related reminders/escalations, you can leverage the Communications Editor to format and dynamically customize your content.</span></span>

## <a name="rich-text-editor"></a><span data-ttu-id="8e1b2-104">Editor de Rich Text</span><span class="sxs-lookup"><span data-stu-id="8e1b2-104">Rich text editor</span></span> 

<span data-ttu-id="8e1b2-p101">O editor de comunicações permite que o usuário personalize o texto usando as opções do editor. Por exemplo, os usuários podem alterar os tipos de fonte, criar listas com marcadores, destacar conteúdo e muito mais.</span><span class="sxs-lookup"><span data-stu-id="8e1b2-p101">The Communications Editor allows user to customize the text using the editor options. For example, users can change font types, create bulleted lists, highlight content, and more.</span></span> 

## <a name="merge-field-variables"></a><span data-ttu-id="8e1b2-107">Mesclar variáveis de campo</span><span class="sxs-lookup"><span data-stu-id="8e1b2-107">Merge field variables</span></span>

<span data-ttu-id="8e1b2-p102">Você pode aproveitar as variáveis de mala direta por email do editor de comunicações para inserir atributos de responsáveis personalizados no corpo de texto de uma comunicação. Quando enviado para os responsáveis, o campo de mesclagem será preenchido com o campo correspondente. Por exemplo, quando enviado para os responsáveis John Smith, o campo de mesclagem [nome do responsáveis] seria convertido com o nome correspondente.</span><span class="sxs-lookup"><span data-stu-id="8e1b2-p102">You can leverage email merge variables from the Communications Editor to embed customized custodian attributes into a communication's body text. When sent to the custodian, the merge field will be populated with the corresponding field. For example, when sent to custodian John Smith, the merge field [Custodian Name] would be translated with the corresponding name.</span></span> 

<span data-ttu-id="8e1b2-p103">Você pode usar campos de mala direta por email selecionando os ícones do **campo** de mesclagem na parte superior do controle do editor de Rich Text. O espaço reservado será adicionado com base no local do cursor dos usuários.</span><span class="sxs-lookup"><span data-stu-id="8e1b2-p103">You can use email merge fields by selecting the **Merge field** icons on the top of the rich-text editor control. The placeholder will be added based off the location of the users' cursor.</span></span> 

### <a name="list-of-merge-field-variables"></a><span data-ttu-id="8e1b2-113">Lista de variáveis de campo de mesclagem</span><span class="sxs-lookup"><span data-stu-id="8e1b2-113">List of merge field variables</span></span>

| <span data-ttu-id="8e1b2-114">Nome do campo</span><span class="sxs-lookup"><span data-stu-id="8e1b2-114">Field name</span></span>                  | <span data-ttu-id="8e1b2-115">Detalhes do campo</span><span class="sxs-lookup"><span data-stu-id="8e1b2-115">Field details</span></span> | 
| :------------------- | :------------------- |
| <span data-ttu-id="8e1b2-116">Nome para Exibição</span><span class="sxs-lookup"><span data-stu-id="8e1b2-116">Display Name</span></span>  | <span data-ttu-id="8e1b2-117">O nome e o sobrenome do responsáveis.</span><span class="sxs-lookup"><span data-stu-id="8e1b2-117">The custodian's first and last name.</span></span> | 
| <span data-ttu-id="8e1b2-118">Link de confirmação</span><span class="sxs-lookup"><span data-stu-id="8e1b2-118">Acknowledgement Link</span></span> | <span data-ttu-id="8e1b2-119">Um link personalizado para registrar a confirmação de cada um dos responsáveis.</span><span class="sxs-lookup"><span data-stu-id="8e1b2-119">A customized link to record each custodian's acknowledgement.</span></span>|                 |
| <span data-ttu-id="8e1b2-120">Link do portal</span><span class="sxs-lookup"><span data-stu-id="8e1b2-120">Portal Link</span></span>     | <span data-ttu-id="8e1b2-121">Um link personalizado para o portal de conformidade do responsáveis.</span><span class="sxs-lookup"><span data-stu-id="8e1b2-121">A customized link for the custodian's Compliance Portal.</span></span>|                |
| <span data-ttu-id="8e1b2-122">Responsável pela emissão</span><span class="sxs-lookup"><span data-stu-id="8e1b2-122">Issuing Officer</span></span>                   | <span data-ttu-id="8e1b2-123">O endereço de email do responsável pela emissão especificado.</span><span class="sxs-lookup"><span data-stu-id="8e1b2-123">The email address of the specified issuing officer.</span></span>|                   |
| <span data-ttu-id="8e1b2-124">Data de emissão</span><span class="sxs-lookup"><span data-stu-id="8e1b2-124">Issuing Date</span></span>                   | <span data-ttu-id="8e1b2-125">A data em que o aviso foi emitido (UTC).</span><span class="sxs-lookup"><span data-stu-id="8e1b2-125">The date that the notice was issued (UTC).</span></span>              |
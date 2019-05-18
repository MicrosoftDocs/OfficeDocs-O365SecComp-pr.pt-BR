---
title: Usar o editor de comunicações
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
ms.openlocfilehash: 78865efc5c10ebcff9742f922f675b637bb9b2b0
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34151463"
---
# <a name="use-the-communications-editor"></a><span data-ttu-id="c8bd4-102">Usar o editor de comunicações</span><span class="sxs-lookup"><span data-stu-id="c8bd4-102">Use the communications editor</span></span>

<span data-ttu-id="c8bd4-103">À medida que você define o conteúdo do seu conteúdo de portal, as notificações de retenção legal e lembretes/rementeções relacionados, você pode aproveitar o editor de comunicações para formatar e personalizar dinamicamente o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="c8bd4-103">As you define the content of your portal content, legal hold notifications, and related reminders/escalations, you can leverage the Communications Editor to format and dynamically customize your content.</span></span>

## <a name="rich-text-editor"></a><span data-ttu-id="c8bd4-104">Editor de Rich Text</span><span class="sxs-lookup"><span data-stu-id="c8bd4-104">Rich text editor</span></span> 

<span data-ttu-id="c8bd4-105">O editor de comunicações permite que o usuário personalize o texto usando as opções do editor.</span><span class="sxs-lookup"><span data-stu-id="c8bd4-105">The Communications Editor allows user to customize the text using the editor options.</span></span> <span data-ttu-id="c8bd4-106">Por exemplo, os usuários podem alterar os tipos de fonte, criar listas com marcadores, destacar conteúdo e muito mais.</span><span class="sxs-lookup"><span data-stu-id="c8bd4-106">For example, users can change font types, create bulleted lists, highlight content, and more.</span></span> 

## <a name="merge-field-variables"></a><span data-ttu-id="c8bd4-107">Mesclar variáveis de campo</span><span class="sxs-lookup"><span data-stu-id="c8bd4-107">Merge field variables</span></span>

<span data-ttu-id="c8bd4-108">Você pode aproveitar as variáveis de mala direta por email do editor de comunicações para inserir atributos de responsáveis personalizados no corpo de texto de uma comunicação.</span><span class="sxs-lookup"><span data-stu-id="c8bd4-108">You can leverage email merge variables from the Communications Editor to embed customized custodian attributes into a communication's body text.</span></span> <span data-ttu-id="c8bd4-109">Quando enviado para os responsáveis, o campo de mesclagem será preenchido com o campo correspondente.</span><span class="sxs-lookup"><span data-stu-id="c8bd4-109">When sent to the custodian, the merge field will be populated with the corresponding field.</span></span> <span data-ttu-id="c8bd4-110">Por exemplo, quando enviado para os responsáveis John Smith, o campo de mesclagem [nome do responsáveis] seria convertido com o nome correspondente.</span><span class="sxs-lookup"><span data-stu-id="c8bd4-110">For example, when sent to custodian John Smith, the merge field [Custodian Name] would be translated with the corresponding name.</span></span> 

<span data-ttu-id="c8bd4-111">Você pode usar campos de mala direta por email selecionando os ícones do **campo** de mesclagem na parte superior do controle do editor de Rich Text.</span><span class="sxs-lookup"><span data-stu-id="c8bd4-111">You can use email merge fields by selecting the **Merge field** icons on the top of the rich-text editor control.</span></span> <span data-ttu-id="c8bd4-112">O espaço reservado será adicionado com base no local do cursor dos usuários.</span><span class="sxs-lookup"><span data-stu-id="c8bd4-112">The placeholder will be added based off the location of the users' cursor.</span></span> 

### <a name="list-of-merge-field-variables"></a><span data-ttu-id="c8bd4-113">Lista de variáveis de campo de mesclagem</span><span class="sxs-lookup"><span data-stu-id="c8bd4-113">List of merge field variables</span></span>

| <span data-ttu-id="c8bd4-114">Nome do campo</span><span class="sxs-lookup"><span data-stu-id="c8bd4-114">Field name</span></span>                  | <span data-ttu-id="c8bd4-115">Detalhes do campo</span><span class="sxs-lookup"><span data-stu-id="c8bd4-115">Field details</span></span> | 
| :------------------- | :------------------- |
| <span data-ttu-id="c8bd4-116">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="c8bd4-116">Display Name</span></span>  | <span data-ttu-id="c8bd4-117">O nome e o sobrenome do responsáveis.</span><span class="sxs-lookup"><span data-stu-id="c8bd4-117">The custodian's first and last name.</span></span> | 
| <span data-ttu-id="c8bd4-118">Link de confirmação</span><span class="sxs-lookup"><span data-stu-id="c8bd4-118">Acknowledgement Link</span></span> | <span data-ttu-id="c8bd4-119">Um link personalizado para registrar a confirmação de cada um dos responsáveis.</span><span class="sxs-lookup"><span data-stu-id="c8bd4-119">A customized link to record each custodian's acknowledgement.</span></span>|                 |
| <span data-ttu-id="c8bd4-120">Link do portal</span><span class="sxs-lookup"><span data-stu-id="c8bd4-120">Portal Link</span></span>     | <span data-ttu-id="c8bd4-121">Um link personalizado para o portal de conformidade do responsáveis.</span><span class="sxs-lookup"><span data-stu-id="c8bd4-121">A customized link for the custodian's Compliance Portal.</span></span>|                |
| <span data-ttu-id="c8bd4-122">Responsável pela emissão</span><span class="sxs-lookup"><span data-stu-id="c8bd4-122">Issuing Officer</span></span>                   | <span data-ttu-id="c8bd4-123">O endereço de email do responsável pela emissão especificado.</span><span class="sxs-lookup"><span data-stu-id="c8bd4-123">The email address of the specified issuing officer.</span></span>|                   |
| <span data-ttu-id="c8bd4-124">Data de emissão</span><span class="sxs-lookup"><span data-stu-id="c8bd4-124">Issuing Date</span></span>                   | <span data-ttu-id="c8bd4-125">A data em que o aviso foi emitido (UTC).</span><span class="sxs-lookup"><span data-stu-id="c8bd4-125">The date that the notice was issued (UTC).</span></span>              |
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
# <a name="use-the-communications-editor"></a>Usar o editor de comunicações

À medida que você define o conteúdo do seu conteúdo de portal, as notificações de retenção legal e lembretes/rementeções relacionados, você pode aproveitar o editor de comunicações para formatar e personalizar dinamicamente o conteúdo.

## <a name="rich-text-editor"></a>Editor de Rich Text 

O editor de comunicações permite que o usuário personalize o texto usando as opções do editor. Por exemplo, os usuários podem alterar os tipos de fonte, criar listas com marcadores, destacar conteúdo e muito mais. 

## <a name="merge-field-variables"></a>Mesclar variáveis de campo

Você pode aproveitar as variáveis de mala direta por email do editor de comunicações para inserir atributos de responsáveis personalizados no corpo de texto de uma comunicação. Quando enviado para os responsáveis, o campo de mesclagem será preenchido com o campo correspondente. Por exemplo, quando enviado para os responsáveis John Smith, o campo de mesclagem [nome do responsáveis] seria convertido com o nome correspondente. 

Você pode usar campos de mala direta por email selecionando os ícones do **campo** de mesclagem na parte superior do controle do editor de Rich Text. O espaço reservado será adicionado com base no local do cursor dos usuários. 

### <a name="list-of-merge-field-variables"></a>Lista de variáveis de campo de mesclagem

| Nome do campo                  | Detalhes do campo | 
| :------------------- | :------------------- |
| Nome de exibição  | O nome e o sobrenome do responsáveis. | 
| Link de confirmação | Um link personalizado para registrar a confirmação de cada um dos responsáveis.|                 |
| Link do portal     | Um link personalizado para o portal de conformidade do responsáveis.|                |
| Responsável pela emissão                   | O endereço de email do responsável pela emissão especificado.|                   |
| Data de emissão                   | A data em que o aviso foi emitido (UTC).              |
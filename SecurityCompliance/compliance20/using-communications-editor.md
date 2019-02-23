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
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 967320aeb960258d77d90cca4e3b681849f9952e
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215801"
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
| Nome para Exibição  | O nome e o sobrenome do responsáveis. | 
| Link de confirmação | Um link personalizado para registrar a confirmação de cada um dos responsáveis.|                 |
| Link do portal     | Um link personalizado para o portal de conformidade do responsáveis.|                |
| Responsável pela emissão                   | O endereço de email do responsável pela emissão especificado.|                   |
| Data de emissão                   | A data em que o aviso foi emitido (UTC).              |
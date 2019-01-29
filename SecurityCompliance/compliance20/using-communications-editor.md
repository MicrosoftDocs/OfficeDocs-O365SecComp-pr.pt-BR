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
# <a name="using-the-communications-editor"></a>Usando o Editor de comunicações
Conforme você define o conteúdo de seu conteúdo de portal, legais segure notificações e lembretes/escalonamentos relacionados, você pode aproveitar o Editor de comunicações para formatar e personalizar dinamicamente seu conteúdo.

## <a name="rich-text-editor"></a>Editor de Rich Text 

O Editor de comunicações permite que o usuário personalize o texto usando as opções de editor. Por exemplo, os usuários podem alterar os tipos de fonte, criar listas com marcadores, realce conteúdo e mais. 

<<include screenshot>>

## <a name="merge-field-variables"></a>Variáveis de campo de mesclagem

Você pode aproveitar as variáveis de mesclagem email no Editor de comunicações para incorporar os atributos dos responsáveis personalizada no corpo de texto de uma comunicação. Quando enviado para dos responsáveis, o campo de mesclagem será preenchido com o campo correspondente. Por exemplo, quando enviado para dos responsáveis John Smith, o campo de mesclagem [nome dos responsáveis] seria convertido com o nome correspondente. 

Você pode usar os campos de mesclagem email selecionando os ícones de **Campo de mala direta** na parte superior do controle de editor de rich text. O espaço reservado será adicionado com base desativa a localização do cursor dos usuários. 

### <a name="list-of-merge-field-variables"></a>Lista de variáveis de campo de mala direta
| Nome do campo                  | Detalhes do campo | 
| :------------------- | :-------------------: |
| Nome para Exibição  | Dos responsáveis e sobrenome nome | 
| Link de confirmação                 | Link personalizado para registrar a confirmação da cada responsável                 |
| Link de portal     | Link personalizado para Portal do dos responsáveis de conformidade                 |
| Responsável pela emissora                   | Endereço de email do responsável pela emissora especificado                   |
| Data de emissão                   | Data em que o aviso foi emitido (UTC)              |
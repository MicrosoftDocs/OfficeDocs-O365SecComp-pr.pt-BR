---
title: Isolamento de Inquilino do Office 365 na pesquisa do Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Resumo: Uma explicação dos isolamento de locatário na pesquisa do Office 365.'
ms.openlocfilehash: cc73f3c157ffd20b3891a6b7c58e7d0b2adf4e55
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523453"
---
# <a name="tenant-isolation-in-office-365-search"></a>Isolamento de locatário na pesquisa do Office 365
Pesquisa do SharePoint Online usa um modelo de separação de locatário que equilibra a eficiência de estruturas de dados compartilhadas com proteção contra vazamento de entre locatários de informações. Com esse modelo, podemos evitar que os recursos de pesquisa de:
- Retornar resultados de consulta que contêm os documentos a partir de outros tenants
- Expondo informações suficientes nos resultados da consulta que um usuário seu nível de habilidade poderia interpretar informações sobre outros tenants
- Mostrando o esquema ou configurações do outro locatário
- Combinação de informações entre locatários ou resultados de repositório no locatário errado de processamento de análise
- Usando as entradas de dicionário de outro locatário

Para cada tipo de dados de inquilinos, usamos uma ou mais camadas de proteção no código para evitar acidental de vazamento de informações. Os dados mais importantes tem as maioria das camadas de proteção para certificar-se de que um único defeito não resulta em vazamento de informações real ou percebida.

## <a name="tenant-separation-for-the-search-index"></a>Separação de locatário para o índice de pesquisa
O índice de pesquisa é armazenado em disco em servidores que hospedam os componentes de índice e os locatários compartilham os arquivos de índice. Documentos indexados de um inquilino são visíveis apenas para consultas para desse inquilino. Três mecanismos independentes evitar vazamento de informações:
- A filtragem de ID do inquilino
- Termos de ID de Inquilino prefixação
- Verificações ACL

Todos os três mecanismos teria falhar por pesquisa retornar os documentos ao inquilino errado.

## <a name="tenant-id-filtering-and-tenant-id-term-prefixing"></a>Termo de ID de Inquilino colocação de um prefixo e a filtragem de ID do inquilino
Prefixos de pesquisa cada termo que é indexada no índice de texto completo com o ID do inquilino. Por exemplo, quando o termo "*foo*" é indexado para um inquilino com uma ID de "*123*", a entrada no índice de texto completo é "*123foo.*"

Cada consulta é convertida para incluir a ID do inquilino usando um processo chamado filtragem por ID do inquilino. Por exemplo, a consulta "*foo*" é convertida em "<*guid*>. *foo* E a *tenantID*: <*guid*> ", onde <*guid*> representa o inquilino executando a consulta. Esta conversão de consulta ocorre em cada nó do índice e processamento nem consulta nem conteúdo pode influenciar a ele. Como a ID do inquilino é adicionada a cada consulta, a frequência de um termo em outros tenants não pode ser inferida observando na melhor das hipóteses em um locatário de classificação de correspondência.

Termos de ID de Inquilino prefixação ocorre apenas no índice de texto completo. Pesquisas por campo, como "*título: foo*", vá para um índice de pesquisa sintética onde termos não prefixados por ID de Inquilino. Em vez disso, as pesquisas por campo são prefixadas com o nome do campo. Por exemplo, a consulta "*título: foo*" é convertida em "*fields.title:foo AND fields.tenantID*: <*guid*>." Porque a frequência de um termo não influenciar a classificação de visitas no índice de pesquisa sintética, não é necessário para a separação de locatário for precedido dos termos. Para uma pesquisa por campo como "*título: foo*", separação de conteúdo de locatário depende da ID do inquilino filtragem por meio da conversão de consulta.

## <a name="document-access-control-list-checks"></a>Verificações de lista de controle de acesso de documento
Pesquisa controla o acesso a documentos por meio de ACLs que são salvas no índice de pesquisa. Cada item é indexada com um conjunto de termos em um campo ACL especial. O campo ACL contém um termo por grupo ou usuário que pode exibir o documento. Cada consulta é aumentada com uma lista de termos ACE (entrada) controle de acesso, um para cada grupo ao qual pertence o usuário autenticado.

Por exemplo, uma consulta como "<*guid*>. *foo AND tenantID*: <*guid*> "se torna:" <*guid*>. *foo AND tenantID*: <*guid*> *AND* (*docACL:*<*ace1*> *OR docACL*: <*ace2*> *OR docACL*: <*ace3*> *… *)"

Porque o usuário e os identificadores de grupo e daí ACEs são exclusivas, esse procedimento oferecerá um nível adicional de segurança entre locatários para documentos que são visíveis apenas para alguns usuários. O mesmo é o caso do especial "todos exceto os usuários externos" ACE que concede acesso aos usuários regulares no inquilino. Mas como ACEs para "Todos" são as mesmas para todos os locatários, separação de Inquilino para documentos públicos depende a filtragem de ID do inquilino. Nega que ACEs também são suportadas. O aumento da consulta adiciona uma cláusula que remove um documento a partir do resultado quando houver uma correspondência com uma ACE de negação.

Na pesquisa do Exchange Online, o índice é particionado na ID da caixa de correio para caixas de correio de usuário individual, em vez de ID do inquilino (ID de assinatura) como no SharePoint Online. O mecanismo de particionamento é igual ao SharePoint Online, mas não há nenhuma ACL filtragem.

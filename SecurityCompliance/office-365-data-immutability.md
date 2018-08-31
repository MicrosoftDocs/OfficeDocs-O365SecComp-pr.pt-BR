---
title: Imutabilidade de dados do Office 365
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
description: Define e explica imutabilidade de dados ou os dados que devem ser detectáveis e não podem ser destruídos ou alterado.
ms.openlocfilehash: 3a9e897734c1805e25a2e2dd5e0c5f8a3e3de3fd
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524329"
---
# <a name="immutability-in-office-365"></a>Imutabilidade no Office 365
Para algumas organizações, conformidade a normas, requisitos de controle interno ou o risco de litígio exigem a preservação de email e os dados associados em um formulário detectável. Todos os dados no sistema devem ser detectáveis e nenhuma parte dela podem ser destruídas ou alterada. O termo padrão do setor para que isso é "imutabilidade." 

Os métodos tradicionais de obter imutabilidade geralmente tem trabalhado movendo mensagens de email para um local de armazenamento separado, somente leitura. Enquanto tais sistemas têm a finalidade de preservar itens de caixa de correio de descoberta, elas geralmente afetam a experiência do usuário significativas maneiras, removendo preservadas itens de fluxo de trabalho diário usuais. Para profissionais de TI, essa abordagem para imutabilidade requer a implantação e a manutenção contínua de uma infra-estrutura de servidor e armazenamento separada. Descoberta propriamente dito é executada com ferramentas externas para o sistema de email, com os custos de manutenção e de implantação associada.

Por meio da configuração dos recursos de política de preservação de arquivamento no Office 365 e em conjunto com os serviços no conjunto do Office 365, como Exchange Online, SharePoint Online, OneDrive for Business e Skype para os negócios e retenção in-loco arquivamento no Office 365 pode preservar e reter várias classes de dados de entrada, internos e de saída, incluindo:
- Comunicações de email de entrada e saída
- Livros e registros contidos no formulário de email ou no compartilhados documentos online
- Solicitações de reunião
- Aparelhos de fax
- Mensagens instantâneas
- Documentos compartilhados durante reuniões online
- Caixas postais

Além disso, a Microsoft desenvolveu recursos de complementos para permitir o [arquivamento de dados](https://support.office.com/article/Archiving-third-party-data-in-Office-365-0ce338d5-3666-4a18-86ab-c6910ff408cc) de outras fontes através da integração com soluções de gerenciamento e a captura de dados de terceiros. Após a importação de dados de terceiros, você pode aplicar recursos de conformidade do Office 365 para os dados, incluindo litígio, descoberta eletrônica In-loco e retenção, pesquisa de conformidade, arquivamento In-loco, auditoria e políticas de retenção. Por exemplo, quando uma caixa de correio for colocada em retenção de litígio, dados de terceiros serão preservados. Você pode pesquisar dados de terceiros usando a descoberta eletrônica In-loco ou pesquisa de conformidade. Ou você pode aplicar o arquivamento e políticas de retenção para dados de terceiros exatamente como você pode usar para dados da Microsoft. Em resumo, o arquivamento de dados de terceiros no Office 365 pode ajudar sua organização permanecer em conformidade com normas políticas e governamentais.

Arquivamento no Office 365 fornece armazenamento de regra de títulos and Exchange comissão (s) compatíveis com 17a-4 e preserva os arquivos permanentes de todos os dados coletados em um formato regravado nem apagado usando diretivas de retenção in-loco e preservação , incluindo o bloqueio de preservação. Especificamente:
- Todos os registros que são armazenados usando as políticas de retenção observadas acima são mantidos em uma área de armazenamento dedicado fora do alcance do usuário comum. Além disso, somente os usuários autorizados podem acessar e pesquisar esses registros, mas não é possível alter ou apagá-los.
- Metadados para cada item incluem um carimbo de hora que é usado no cálculo da duração da retenção. Carimbos de hora são aplicados quando um novo item é recebido ou criado e não pode ser subsequentemente modificados ou removidos dos metadados.
- Arquivamento no Office 365 permite que os usuários para combinar diferentes políticas de retenção e reter ações para criar políticas de retenção granulares para definir o tipo ou o local dos itens imutavelmente seja preservado e a duração de tal preservação.
- O recurso de bloqueio de preservação permite que os usuários escolham se desejam fazer a política de uma diretiva restritiva. Uma política restritiva proíbe que qualquer pessoa com a capacidade de remover, desabilitar ou fazer alterações em uma diretiva de retenção. Isso significa que depois que o bloqueio de preservação está habilitado, ele não pode ser desativado e nenhum mecanismo existirá sob quais quaisquer dados da responsáveis existentes que foram coletados pela retenção políticas em vigor podem ser substituídas, modificado, apagados ou excluídos durante a período de preservação. Além disso, os isenção período definido por preservação de bloqueio não pode ser reduzida ou diminuiu. No entanto, talvez, seja estendidos, no caso de um requisito legal para continuar a retenção dos dados armazenados, conforme indicado acima. Bloqueio preservação garante que ninguém, nem mesmo os administradores ou aqueles com determinados controle de acesso, poderá alterar as configurações ou substituir ou apagar dados que foram armazenados, trazendo o arquivamento no Office 365 alinhado com as diretrizes estabelecida a versão 2003 do s Regra 17a-4.

Para os clientes compreender melhor como o Office 365 pode ser utilizada para atender suas obrigações normativas, especificamente em relação aos requisitos do Regra 17a-4, podemos ter lançado um [white paper](https://go.microsoft.com/fwlink/?linkid=830440) que cobre o arquivamento do Exchange Online, SharePoint Online, OneDrive para negócios e Skype para negócios. O white paper também fornece uma análise detalhada dos recursos de arquivamento do Office 365 e funcionalidades em relação a cada um dos requisitos em s Regra 17a-4 e demonstra aos clientes regulamentados como arquivamento do Office 365 pode permitir que eles atender a essas requisitos.
---
title: Imutabilidade dos dados do Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Define e explica a imutabilidade dos dados ou os dados que devem ser detectáveis e não podem ser destruídos ou alterados.
ms.openlocfilehash: b23a62dd95ec2ca554997fc667d89e6979e5b747
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262863"
---
# <a name="immutability-in-office-365"></a>Imutabilidade no Office 365
Para algumas organizações, conformidade normativa, requisitos de governança interna ou risco de litígio exigem a preservação de email e dados associados em um formulário detectável. Todos os dados no sistema devem ser detectáveis e nenhum deles pode ser destruído ou alterado. O termo padrão do setor para isso é "imutabilidade". 

Os métodos tradicionais de obtenção de imutabilidade normalmente funcionavam movendo mensagens de email para um local de armazenamento separado e somente leitura. Embora esses sistemas atendam à finalidade de preservar itens de caixa de correio para descoberta, eles geralmente afetam a experiência do usuário de maneiras significativas, removendo itens preservados do fluxo de trabalho diário personalizado. Para profissionais de ti, essa abordagem para a imutabilidade requer a implantação e a manutenção contínua de um servidor separado e uma infraestrutura de armazenamento. A descoberta em si é realizada com ferramentas externas ao sistema de email, com custos associados de implantação e manutenção.

Por meio da configuração dos recursos de política de retenção e preservação in-loco do arquivamento no Office 365 e em conjunto com os serviços do Office 365 Suite, como o Exchange Online, o SharePoint Online, o OneDrive for Business e o Skype for Business, o arquivamento no Office 365 pode preservar e reter várias classes de dados de entrada, internos e de saída, incluindo:
- Comunicações de email de entrada e saída
- Manuais e registros contidos no formulário de email ou em documentos online compartilhados
- Solicitações de reunião
- Fax
- Mensagens instantâneas
- Documentos compartilhados durante reuniões online
- Caixa postal

Além disso, a Microsoft desenvolveu recursos complementares para permitir o [arquivamento de dados](https://support.office.com/article/Archiving-third-party-data-in-Office-365-0ce338d5-3666-4a18-86ab-c6910ff408cc) de outras fontes por meio da integração com soluções de captura e gerenciamento de dados de terceiros. Após a importação dos dados de terceiros, você pode aplicar recursos de conformidade do Office 365 aos dados, incluindo retenção de litígio, descoberta eletrônica in-loco e bloqueio, pesquisa de conformidade, arquivamento in-loco, auditoria e políticas de retenção. Por exemplo, quando uma caixa de correio é colocada em Retenção de Litígio, os dados de terceiros são preservados. Você pode pesquisar dados de terceiros usando a Descoberta Eletrônica In-loco ou a Pesquisa de Conformidade. Se preferir, você pode aplicar políticas de arquivamento e de retenção aos dados de terceiros, assim como faz com os dados da Microsoft. Em suma, o arquivamento de dados de terceiros no Office 365 pode ajudar sua organização a se manter em conformidade com as políticas governamentais e regulamentares.

O arquivamento no Office 365 oferece um armazenamento em conformidade com a regra de Securities-4 de títulos e de comissões do Exchange (seg) e preserva arquivos permanentes de todos os dados coletados em um formato não-regravável e não apagável usando políticas de retenção in-loco e políticas de preservação , incluindo bloqueio de preservação. Especificamente:
- Todos os registros armazenados usando as políticas de retenção indicadas acima são mantidos em uma área de armazenamento dedicada fora do âmbito do usuário comum. Além disso, somente os usuários autorizados podem acessar e Pesquisar esses registros, mas não podem alterá-los ou apagá-los.
- Os metadados de cada item incluem um carimbo de data/hora que é usado no cálculo da duração da retenção. Os carimbos de data/hora são aplicados quando um novo item é recebido ou criado e não pode ser modificado ou removido dos metadados.
- O arquivamento no Office 365 permite aos usuários combinar diferentes políticas de retenção e ações de bloqueio para criar políticas de retenção granulares para definir o tipo ou o local dos itens a serem imutavelmente preservados e a duração da preservação.
- O recurso de bloqueio de preservação permite que os usuários escolham se desejam tornar a política uma política restritiva. Uma política restritiva proíbe que qualquer pessoa tenha a capacidade de remover, desabilitar ou fazer qualquer alteração na política de retenção. Isso significa que, quando o bloqueio de preservação estiver habilitado, ele não poderá ser desabilitado, e nenhum mecanismo existirá sob o qual qualquer dado dos responsáveis existentes que foram coletados pelas políticas de retenção em vigor poderá ser substituído, modificado, apagado ou excluído durante o período de preservação. Além disso, o período de retenção definido pelo bloqueio de preservação não pode ser reduzido ou reduzido. No entanto, ele pode ser estendido, no caso de um requisito legal para continuar a retenção dos dados armazenados, conforme observado acima. O bloqueio de preservação garante que ninguém, nem mesmo administradores ou aqueles com certos controles de acesso, possam alterar as configurações ou substituir ou apagar os dados que foram armazenados, disponibilizar o arquivamento no Office 365 em linha com as orientações definidas na versão 2003 de seg Regra 17a-4.

Para os clientes entender melhor como o Office 365 pode ser utilizado para atender às obrigações regulamentares, especificamente em relação aos requisitos da regra 17a-4, lançamos um [White Paper](https://go.microsoft.com/fwlink/?linkid=830440) que abrange o arquivamento do Exchange Online, o SharePoint Online, o onedrive para empresas e Skype for Business. O White Paper também fornece uma análise detalhada dos recursos de arquivamento e funcionalidades do Office 365 em relação a cada um dos requisitos na regra 17a-4 da SEC e demonstra aos clientes regulamentados como o arquivamento do Office 365 pode permitir que eles atendam a esses atende.
---
title: Isolamento de Inquilino no Office 365
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
description: Um resumo de como o Microsoft impõe o isolamento de Inquilino do Office 365.
ms.openlocfilehash: fcf66ee65c2a4cfdf73ae0eac77f54bd555d059d
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524118"
---
# <a name="tenant-isolation-in-office-365"></a>Isolamento de Inquilino no Office 365

Um dos principais benefícios da nuvem computação é o conceito de uma infraestrutura compartilhada, comum entre vários clientes simultaneamente, levando a economia de escala. Esse conceito é chamado de *multilocação*. A Microsoft trabalha continuamente para garantir que as arquiteturas de multilocatários de nossos serviços de nuvem oferecem suporte aos padrões de segurança, confidencialidade, privacidade, integridade e disponibilidade de nível empresarial.

Com base nos investimentos significativos e experiência obtidas do [Trustworthy Computing](https://www.microsoft.com/en-us/twc/default.aspx) e o [Security Development Lifecycle](http://www.microsoft.com/security/sdl/default.aspx), serviços de nuvem da Microsoft foram projetados com a pressuposição de que todos os locatários são potencialmente hostis a todos outros tenants e podemos implementou as medidas de segurança para impedir que as ações de um inquilino afetar a segurança ou o serviço de outro locatário, ou acessem o conteúdo de outro locatário.

Os dois objetivos principais de manter o isolamento de locatário em um ambiente de multilocação são:
1.  Impedindo o vazamento de ou acesso não autorizado a, conteúdo de cliente entre locatários; e
2.  Impedindo que as ações de um inquilino afetar adversamente o serviço para outro locatário

Vários formulários de proteção foram implementados ao longo do Office 365 para impedir que os clientes de serviços do Office 365 comprometer ou aplicativos ou que tenha acesso não autorizado às informações de outros tenants ou o sistema do Office 365 propriamente dito, incluindo:
- Isolamento lógico do conteúdo de cliente dentro de cada locatário para serviços do Office 365 é obtido por meio de autorização do Azure Active Directory e controle de acesso baseado em função.
- SharePoint Online oferece mecanismos de isolamento no nível de armazenamento de dados.
- A Microsoft usa rigorosa segurança física, triagem de plano de fundo e uma estratégia de várias camadas de criptografia para proteger a confidencialidade e a integridade do conteúdo de cliente. Todos os centros de dados do Office 365 têm controles de acesso biométrica, com mais exigir imprime palm para obter acesso físico. Além disso, os funcionários da Microsoft todas baseadas em US são necessárias para concluir com êxito uma verificação de plano de fundo padrão como parte do processo de contratação. Para obter mais informações sobre os controles usados para acesso administrativo no Office 365, consulte [Controles de acesso administrativo do Office 365](office-365-administrative-access-controls-overview.md).
- O Office 365 usa tecnologias no lado do serviço que criptografar conteúdo de cliente em repouso e em trânsito, incluindo o BitLocker, criptografia por arquivo, segurança de camada de transporte (TLS) e Internet Protocol Security (IPsec). Para obter detalhes específicos sobre a criptografia no Office 365, consulte [Tecnologias de criptografia de dados no Office 365](office-365-encryption-in-the-microsoft-cloud-overview.md).

Juntos, as proteções listados acima fornecem controles de isolamento lógico robusta que oferecem proteção contra ameaças e redução de risco equivalente à fornecida por isolamento físico sozinho.

## <a name="related-links"></a>Links relacionados
- [Isolamento e controle de acesso do Azure Active Directory](office-365-isolation-in-azure-active-directory.md)
- [Isolamento de locatário no Office Graph e Delve](office-365-isolation-in-graph-and-delve.md)
- [Isolamento de locatário na pesquisa do Office 365](office-365-isolation-in-office-365-search.md)
- [Isolamento de locatário no Vídeo do Office 365](office-365-isolation-in-office-365-video.md)
- [Limites de recurso](office-365-resource-limits.md)
- [Monitorando e testando limites do locatário](office-365-monitoring-and-testing.md)
- [Isolamento e controle de acesso no Office 365](office-365-isolation-in-office-365.md)
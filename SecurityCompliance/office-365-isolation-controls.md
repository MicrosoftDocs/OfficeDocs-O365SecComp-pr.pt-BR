---
title: Controles de isolamento do Office 365
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
description: 'Resumo: Uma explicação dos controles de isolamento dentro do Office 365.'
ms.openlocfilehash: 3a5c06d0675a4503d9f5e5edd58535688fb9180a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524715"
---
# <a name="office-365-isolation-controls"></a>Controles de isolamento do Office 365 

A Microsoft continuamente trabalha para garantir que a arquitetura de multilocação do Office 365 oferece suporte a segurança de nível empresarial, confidencialidade, [padrões](https://www.microsoft.com/TrustCenter/Compliance?service=Office#Icons)de privacidade, integridade e disponibilidade, bem como padrões internacionais e locais. Devido a escala e o escopo dos serviços fornecidos pela Microsoft, seria difícil e não econômicas para gerenciar o Office 365 se significativo interação humana eram necessária. Serviços do Office 365 são fornecidos em vários datacenters distribuídas globalmente, de maneira altamente automatizado, onde extremamente poucas operações de datacenter exigem um toque humano e até mesmo menos operações exigem acesso ao conteúdo do cliente. Nossa equipe oferece suporte a esses serviços e centros de dados usando ferramentas automatizadas e altamente seguros acesso remoto. Para alguns dos detalhes sobre como os serviços em larga escala são operados no Office 365, consulte [um behind olhada nos bastidores do Office 365 para profissionais de TI](https://channel9.msdn.com/Events/SharePoint-Conference/2014/SPC202).

O Office 365 é composto de vários serviços que fornecem funcionalidade comercial importante e contribuem para toda a experiência do Office 365. Cada um desses serviços é projetado para ser autônomos e integrar umas com as outras. O Office 365 destina-se com os princípios de uma [Arquitetura orientada a serviços](https://msdn.microsoft.com/library/aa480021.aspx), que é definido como a criação e desenvolvimento de software na forma de serviços interoperáveis fornecendo a funcionalidade de negócios bem definidas e [segurança operacional Garantia](http://www.microsoft.com/download/details.aspx?id=40872), uma estrutura que incorpora o conhecimento obtidas por meio de uma variedade de recursos que são exclusivos para a Microsoft, incluindo o Microsoft [Security Development Lifecycle](https://www.microsoft.com/sdl/default.aspx), o [Microsoft Security Response Center](https://technet.microsoft.com/library/dn440717.aspx)e profunda divulgação do cenário de ameaças cybersecurity.

Serviços do Office 365 interoperam uns com os outros, mas estão projetados e implementados para que possa ser implantados e operados como serviços autônomos independentes umas das outras. Microsoft separa obrigações e áreas de responsabilidade para o Office 365 reduzir as grandes oportunidades de modificação não intencional ou não autorizada ou uso indevido dos ativos da organização. As equipes do Office 365 tenham definido funções como parte de um mecanismo de controle de acesso baseado em função abrangente.

## <a name="customer-content-isolation"></a>Isolamento de conteúdo do cliente
Todo o conteúdo do cliente que pertencem a um locatário é isolado de outros tenants e dos dados de operações e sistemas usados no gerenciamento do Office 365. Vários formulários de proteção foram implementados ao longo do Office 365 para minimizar o risco de comprometimento de qualquer serviço do Office 365 ou um aplicativo ou qualquer obtenção de acesso não autorizado às informações de locatários ou o próprio sistema do Office 365. Para obter informações sobre como o Microsoft implementa o isolamento lógico de dados de inquilinos dentro do Office 365, consulte o [Isolamento de Inquilino no Office 365](office-365-tenant-isolation-overview.md).

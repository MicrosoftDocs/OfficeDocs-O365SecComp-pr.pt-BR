---
title: Controles de isolamento do Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: 'Resumo: uma explicação dos controles de isolamento no Office 365.'
ms.openlocfilehash: a6ff2b11ea02334a6c47317cbb77b8d47207b552
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217311"
---
# <a name="office-365-isolation-controls"></a>Controles de isolamento do Office 365 

A Microsoft funciona continuamente para garantir que a arquitetura de vários locatários do Office 365 suporte a segurança de nível empresarial, confidencialidade, privacidade, integridade e [padrões](https://www.microsoft.com/TrustCenter/Compliance?service=Office#Icons)de disponibilidade, bem como padrões locais e internacionais. Dada a escala e o escopo de serviços fornecidos pela Microsoft, seria difícil e não mais econômico gerenciar o Office 365 se for necessária uma interação humana significativa. Os serviços do Office 365 são fornecidos por meio de vários datacenters distribuídos globalmente, em um modo altamente automatizado, onde extremamente poucas operações de datacenter exigem um toque humano, e até menos operações precisam de acesso ao conteúdo do cliente. Nossa equipe oferece suporte a esses serviços e datacenters usando ferramentas automatizadas e acesso remoto altamente seguro. Para ver alguns dos detalhes sobre como os serviços em grande escala são operados no Office 365, confira [a bastidores, examine o Office 365 para profissionais de ti](https://channel9.msdn.com/Events/SharePoint-Conference/2014/SPC202).

O Office 365 é composto por vários serviços que fornecem funcionalidade comercial importante e contribuem para toda a experiência do Office 365. Cada um desses serviços é projetado para ser autônomo e para integração entre si. O Office 365 foi projetado com os princípios de uma [arquitetura orientada a serviços](https://msdn.microsoft.com/library/aa480021.aspx), que é definido como design e desenvolvimento de software na forma de serviços de interoperabilidade que fornecem funcionalidade de negócios bem definida e [segurança operacional Assurance](http://www.microsoft.com/download/details.aspx?id=40872), uma estrutura que incorpora o conhecimento obtido por meio de uma variedade de recursos exclusivos da Microsoft, incluindo o [ciclo de vida de desenvolvimento de segurança](https://www.microsoft.com/sdl/default.aspx)da Microsoft, o [Microsoft Security Response Center](https://technet.microsoft.com/library/dn440717.aspx)e profundo conhecimento do panorama de ameaças do cybersecurity.

Os serviços do Office 365 interoperam entre si, mas foram projetados e implementados para que eles possam ser implantados e operados como serviços autônomos, independentemente uns dos outros. A Microsoft segregou as obrigações e áreas de responsabilidade do Office 365 para reduzir as oportunidades de modificação não autorizada ou incorreta ou uso indevido dos ativos da organização. O Office 365 Teams tem funções definidas como parte de um mecanismo abrangente de controle de acesso baseado em função.

## <a name="customer-content-isolation"></a>Isolamento de conteúdo do cliente
Todo o conteúdo do cliente pertencente a um locatário é isolado de outros locatários e dos dados de operações e sistemas usados no gerenciamento do Office 365. Várias formas de proteção foram implementadas em todo o Office 365 para minimizar o risco de comprometimento de qualquer serviço ou aplicativo do Office 365 ou qualquer obtenção de acesso não autorizado às informações de locatários ou ao próprio sistema do Office 365. Para obter informações sobre como a Microsoft implementa o isolamento lógico de dados de locatário no Office 365, consulte [isolamento de locatário no office 365](office-365-tenant-isolation-overview.md).

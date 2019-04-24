---
title: Controles de acesso administrativo no Office 365
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
description: 'Resumo: uma visão geral dos controles de acesso administrativo e categorização de dados do Office 365.'
ms.openlocfilehash: 90dd00049e7e3a9b9548530c42b1c21534cfd7fd
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262973"
---
# <a name="administrative-access-controls-in-office-365"></a>Controles de acesso administrativo no Office 365 

## <a name="introduction"></a>Introdução
A Microsoft investiu de forma intensa e adequada em sistemas e controles que automatizam a maioria das operações do Office 365 enquanto limitava intencionalmente o acesso da Microsoft ao conteúdo do cliente. Os seres humanos governam o serviço e o software opera o serviço. Isso permite que a Microsoft gerencie o Office 365 em escala, além de gerenciar os riscos de ameaças internas ao conteúdo do cliente, como atores mal-intencionados, o spear-phishing de um engenheiro da Microsoft e assim por diante.

Por padrão, os engenheiros da Microsoft têm nenhum privilégio administrativo de pé e zero acesso de pé ao conteúdo do cliente no Office 365. Um engenheiro da Microsoft pode ter acesso limitado, auditado e protegido ao conteúdo de um cliente por um período limitado, mas apenas quando necessário para operações de serviço, e apenas quando aprovado por um membro do gerenciamento sênior da Microsoft (e para clientes que estão licenciado para o recurso de lockbox do cliente, o cliente).

A Microsoft fornece serviços online, incluindo o Office 365, usando várias formas de entrega na nuvem:

- **Nuvens públicas** : inclui versões de vários locatários do Office 365, Azure e outros serviços hospedados na América do Norte, América do Sul, Europa, Ásia, Austrália, etc.
- **Nuvens nacionais** : inclui todas as nuvens soberana e operadas por terceiros, fora dos Estados Unidos (exceto as citadas acima), como o Office 365 na China (que é operado pela 21vianet) e o Office 365 na Alemanha (que é operado pela Microsoft, mas em um modelo no qual um confiável de dados em alemão, o alemão Telekom, controla e monitora o acesso da Microsoft aos dados e sistemas de clientes que contêm dados do cliente).
- **Nuvens governamentais** : inclui o Office 365 e os serviços do Azure que estão disponíveis para os clientes do governo dos Estados Unidos.

Para os fins deste artigo, os serviços do Office 365 incluem o [Exchange Online](https://docs.microsoft.com/Exchange/exchange-online), o [Exchange Online Protection](https://docs.microsoft.com/Office365/SecurityCompliance/eop/exchange-online-protection-overview), o [SharePoint Online](https://docs.microsoft.com/sharepoint/sharepoint-online) (incluindo o [onedrive for Business](https://docs.microsoft.com/OneDrive/onedrive)) e o [Skype for Business](https://docs.microsoft.com/SkypeForBusiness/skype-for-business-online), com informações adicionais sobre alguns controles de acesso [corporativo do Yammer](https://support.office.com/article/yammer-–-admin-help-e1464355-1f97-49ac-b2aa-dd320b179dbe?ui=en-US&rs=en-US&ad=US) . Outros serviços do Office 365 estão fora do escopo deste artigo.

## <a name="office-365-access-controls"></a>Controles de acesso do Office 365
Para fins de controle de acesso, os dados do Office 365 são categorizados como dados do cliente ou outros tipos de dados. Os dados do cliente são todos os dados fornecidos por ou em nome de um cliente por meio do uso do cliente de serviços do Office 365, como conteúdo do cliente (conteúdo criado diretamente ou carregado por usuários do Office 365, incluindo emails, conteúdo do SharePoint Online, mensagens instantâneas, itens de calendário, documentos e contatos armazenados no Office 365) e informações de identificação do usuário final (EUII) (dados exclusivos de um usuário ou que são vinculados a um usuário individual, mas não inclui conteúdo do cliente). 

Outros tipos de dados incluem dados de conta (inclui dados administrativos, que são as informações fornecidas por administradores quando eles se conectam ou compram serviços, e dados de pagamento, que são informações sobre instrumentos de pagamento, como detalhes do cartão de crédito), informações de identificação organizacional (dados que podem ser usadas para identificar um locatário ou dados de uso; não é vinculável a um usuário individual e não inclui conteúdo do cliente) e metadados do sistema (inclui logs de serviço que contêm definições de configuração, status do sistema, endereços IP da Microsoft e informações técnicas sobre inscrições e locatários).

A Microsoft estabeleceu mecanismos de controle de acesso para garantir que ninguém tenha acesso não aprovado aos dados do cliente ou aos dados de controle de acesso (usado para gerenciar o acesso a outros tipos de dados ou funções dentro do ambiente, incluindo acesso ao conteúdo do cliente ou ao EUII; inclui senhas da Microsoft, certificados de segurança e outros dados relacionados à autenticação) ou acesso físico, lógico ou remoto não aprovado ao ambiente de produção do Office 365.

Os controles de acesso usados pela Microsoft para o Office 365 operacional podem ser agrupados em três categorias:
- Controles de isolamento
- Controles de pessoal
- Controles de tecnologia

Quando combinadas, esses controles ajudam a evitar e detectar ações mal-intencionadas no Office 365. Além dos controles de isolamento, pessoal e tecnologia usados pela Microsoft, há uma quarta categoria de controles: as implementadas por clientes.

O Office 365 permite que você gerencie seus dados da mesma forma que os dados são gerenciados em ambientes locais. A pessoa que assina uma organização para o Office 365 se torna automaticamente um administrador global (administrador). O administrador global tem acesso a todos os recursos nos portais de gerenciamento (por exemplo, centros de administração e PowerShell remoto) e pode criar ou editar usuários, atribuir funções de administrador a outros, redefinir senhas de usuário, gerenciar licenças de usuário, gerenciar domínios e aprovar o Lockbox do cliente solicitações, entre outras coisas. Recomendamos que cada organização designe pelo menos duas contas de administrador e, dependendo do tamanho da sua organização, você talvez queira designar vários administradores que atendem a diferentes funções. Para obter informações sobre como atribuir permissões e funções de administrador, consulte [atribuindo funções de administrador no office 365](https://support.office.com/article/Assigning-admin-roles-in-Office-365-eac4d046-1afd-4f1a-85fc-8219c79e1504) e [sobre as funções de administrador do Office 365](https://support.office.com/article/Permissions-in-Office-365-DA585EEA-F576-4F55-A1E0-87090B6AAA9D).


## <a name="related-links"></a>Links relacionados

- [Controles de isolamento](office-365-isolation-controls.md)
- [Controles de pessoal](office-365-personnel-controls.md)
- [Controles de tecnologia](office-365-technology-controls.md)
- [Monitorando e auditando controles de acesso ](office-365-monitoring-and-auditing-access-controls.md)
- [Controles de acesso do Yammer Enterprise](office-365-yammer-enterprise-access-controls.md)
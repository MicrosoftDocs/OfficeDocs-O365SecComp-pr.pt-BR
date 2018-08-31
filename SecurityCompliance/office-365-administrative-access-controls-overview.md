---
title: Controles de acesso administrativo no Office 365
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
description: 'Resumo: Uma visão geral de categorização de dados e controles de acesso administrativo do Office 365.'
ms.openlocfilehash: afa15d37aa8542985c59dbd9e3d82368421530e8
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524062"
---
# <a name="administrative-access-controls-in-office-365"></a>Controles de acesso administrativo no Office 365 

## <a name="introduction"></a>Introdução
A Microsoft investiu pesadamente e adequadamente em sistemas e controles que automatizam a maioria das operações do Office 365 enquanto limita intencionalmente access do Microsoft para conteúdo de cliente. Os humanos regem o serviço e o serviço opera de software. Isso permite que a Microsoft para gerenciar o Office 365 em escala, bem como gerenciar os riscos de ameaças internas para conteúdo de cliente, como atores mal-intencionado, o phishing lança um engenheiro da Microsoft, e assim por diante.

Por padrão, o engenheiros Microsoft tem zero privilégios administrativos de posição e zero acesso de posição ao conteúdo de cliente no Office 365. Engenheiro da Microsoft pode ter limitado, auditadas e acesso a um cliente de conteúdo para uma quantidade limitada de tempo, mas somente quando necessário para operações de serviço e somente quando aprovado por um membro de gerenciamento sênior da Microsoft (e para clientes que estejam seguro licenciados para o recurso de Lockbox do cliente, o "cliente").

A Microsoft fornece serviços online, incluindo o Office 365, usando vários formulários de entrega de nuvem:

- **Nuvens públicas** - inclui as versões de multilocação do Office 365, Windows Azure e outros serviços hospedados na América do Norte, América do Sul, Europa, Ásia, Austrália, etc.
- **Nuvens nacional** - inclui todas as nuvens soberana e operado por terceiros fora dos Estados Unidos (exceto aqueles observado acima), como o Office 365 na China (que é operado pela 21Vianet) e Office 365 na Alemanha (que é operado pela Microsoft, mas em um modelo no qual um objeto de confiança dados alemão, Deutsche Telekom, controla e monitora access do Microsoft para dados de clientes e os sistemas que contêm dados do cliente).
- **Nuvens governamentais** - inclui os serviços do Office 365 e o Azure que estão disponíveis para clientes do governo dos Estados Unidos.

Para fins deste artigo, serviços do Office 365 incluem [O Exchange Online](https://docs.microsoft.com/Exchange/exchange-online), [Exchange Online Protection](https://docs.microsoft.com/Office365/SecurityCompliance/eop/exchange-online-protection-overview), [SharePoint Online](https://docs.microsoft.com/sharepoint/sharepoint-online) (incluindo o [OneDrive for Business](https://docs.microsoft.com/OneDrive/onedrive)) e [Skype para os negócios](https://docs.microsoft.com/SkypeForBusiness/skype-for-business-online), com informações adicionais Alguns controles de acesso do [Yammer Enterprise](https://support.office.com/article/yammer-–-admin-help-e1464355-1f97-49ac-b2aa-dd320b179dbe?ui=en-US&rs=en-US&ad=US) . Outros serviços do Office 365 estão fora do escopo deste artigo.

## <a name="office-365-access-controls"></a>Controles de acesso do Office 365
Para fins de controle de acesso, os dados do Office 365 são categorizados como dados de clientes ou outros tipos de dados. Dados do cliente serão fornecidos pela ou em nome de um cliente por meio do uso do cliente de serviços do Office 365, como o conteúdo do cliente (conteúdo diretamente criadas ou carregadas por usuários do Office 365 incluindo e-mails, SharePoint Online conteúdos, mensagens instantâneas, de todos os dados contatos armazenados no Office 365, documentos e itens de calendário) e informações de identificação do usuário final (EUII) (dados exclusivo para um usuário ou a um usuário individual linkable mas não incluir o conteúdo de cliente). 

Outros tipos de dados incluem dados de conta (inclui dados administrativos, que é a informação oferecida pelos administradores quando eles inscrição ou serviços de compra e dados de pagamento, informações sobre instrumentos de pagamento, como crédito detalhes de cartão), informações de identificação empresariais (dados que podem ser usados para identificar um locatário; ou dados de uso; ele não é linkable a um usuário individual e não incluem conteúdo do cliente) e metadados do sistema (inclui os logs de serviço que contêm as definições de configuração status do sistema, endereços IP da Microsoft e informações técnicas sobre assinaturas e locatários).

Mecanismos de controle de acesso para garantir que ninguém tenha estabelecido pela Microsoft não aprovado acesso aos dados de controle de acesso ou dados do cliente (usado para gerenciar o acesso a outros tipos de dados ou funções dentro do ambiente, incluindo o acesso a conteúdo cliente ou EUII; ele inclui o Microsoft senhas, certificados de segurança e outros dados relacionados à autenticação) ou não aprovadas de acesso remoto, físico ou lógico para o ambiente de produção do Office 365.

Os controles de acesso usados pela Microsoft para Office 365 de operacionais podem ser agrupados em três categorias:
- Controles de isolamento
- Controles de pessoal
- Controles de tecnologia

Quando combinados, esses controles ajudam a prevenir e detectar ações mal-intencionadas no Office 365. Além do isolamento, pessoal e controles de tecnologia usados pela Microsoft, há uma quarta categoria dos controles: aqueles implementada por clientes.

O Office 365 permite que você gerencie seus dados que tanto nos mesmos dados de maneira é gerenciado em ambientes locais. A pessoa que aprova automaticamente o backup de uma organização para o Office 365 se torna um administrador global (admin). O administrador global tem acesso a todos os recursos nos portais de gerenciamento (por exemplo, centros de administração e o PowerShell remoto) e pode criar ou editar usuários, atribuir funções de administrador para outras pessoas, redefinir senhas de usuário, gerenciar licenças de usuário, gerenciar domínios e aprovar Lockbox do cliente solicitações, entre outras coisas. É recomendável que cada organização designar pelo menos duas contas de administrador e, dependendo do tamanho da sua organização, talvez você queira designar vários administradores que atendem a diferentes funções. Para obter informações sobre como atribuir permissões e funções de administrador, consulte [a atribuição de funções de administrador no Office 365](https://support.office.com/article/Assigning-admin-roles-in-Office-365-eac4d046-1afd-4f1a-85fc-8219c79e1504) e [funções de administrador do Office 365](https://support.office.com/article/Permissions-in-Office-365-DA585EEA-F576-4F55-A1E0-87090B6AAA9D).


## <a name="related-links"></a>Links relacionados

- [Controles de isolamento](office-365-isolation-controls.md)
- [Controles de pessoal](office-365-personnel-controls.md)
- [Controles de tecnologia](office-365-technology-controls.md)
- [Monitorando e auditando controles de acesso ](office-365-monitoring-and-auditing-access-controls.md)
- [Controles de acesso do Yammer Enterprise](office-365-yammer-enterprise-access-controls.md)
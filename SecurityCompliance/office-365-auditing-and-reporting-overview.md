---
title: Auditoria e relatórios nos serviços em nuvem da Microsoft
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
- M365-analytics
description: Uma visão geral dos recursos de auditoria e relatórios no Office 365, no Microsoft 365 e no serviço Assurance.
ms.openlocfilehash: a5df0dcb6f762723c6ec0102b2c39f1bc157720c
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262963"
---
# <a name="auditing-and-reporting-in-microsoft-cloud-services"></a>Auditoria e relatórios nos serviços em nuvem da Microsoft

## <a name="introduction"></a>Introdução
Os serviços de nuvem da Microsoft incluem vários recursos de auditoria e relatórios que os clientes podem usar para rastrear as atividades de usuário e administrativas dentro de seus locatários, como as alterações feitas em suas configurações de locatário do Exchange Online e do SharePoint Online, e alterações feitas por usuários em documentos e outros itens. Os clientes podem usar as informações e os relatórios de auditoria disponíveis em nossos serviços de nuvem para gerenciar com mais eficácia a experiência do usuário, reduzir o risco e cumprir as obrigações de conformidade.

## <a name="security--compliance-centers"></a>Centros de conformidade do & de segurança
O [centro de conformidade do & de segurança do Office 365](https://protection.office.com), o [centro de segurança do Microsoft 365](https://security.microsoft.com)e o [centro de conformidade da Microsoft 365](https://compliance.microsoft.com) são portais de um único ponto para proteger os dados em sua organização e incluem vários relatórios e auditorias recursos. Esses centros foram projetados para organizações com proteção de dados ou necessidades de conformidade, ou que desejam auditar as atividades do usuário e do administrador. Você pode acessar esses centros usando sua conta de administrador de assinatura.

Esses centros incluem painéis de navegação que fornecem acesso a vários recursos:
- **Alertas** : permite gerenciar alertas, exibir alertas relacionados à segurança e gerenciar alertas avançados usando o [Office 365 Cloud app Security](https://docs.microsoft.com/en-us/Office365/SecurityCompliance/office-365-cas-overview). 
- **Permissions** – permite que você [atribua permissões](https://support.office.com/article/Give-users-access-to-the-Office-365-Security-Compliance-Center-2cfce2c8-20c5-47f9-afc4-24b059c1bd76) como administrador de conformidade, Gerenciador de descoberta eletrônica e outros a pessoas em sua organização para que eles possam executar tarefas nesses centros. Você pode atribuir permissões para a maioria dos recursos em cada centro, mas outras permissões devem ser configuradas usando o centro de administração do Exchange e o centro de administração do SharePoint.
- **Gerenciamento de ameaças** – permite que você crie e aplique políticas de gerenciamento de dispositivos usando o [Gerenciamento de dispositivo móvel do Office 365](https://support.office.com/article/Overview-of-Mobile-Device-Management-for-Office-365-faa7d8e5-645d-4d59-839c-c8d4c1869e4a), para configurar políticas de [prevenção de perda de dados](https://support.office.com/article/Overview-of-data-loss-prevention-policies-1966b2a7-d1e2-4d92-ab61-42efbb137f5e) (DLP) para sua organização, para configurar a filtragem de emails anti-malware, DomainKeys identificadas por email (DKIM), anexos seguros, links seguros e aplicativos OAuth.
- **Governança de dados** – permite que [você importe emails ou dados do SharePoint de outros sistemas para o Office 365](https://support.office.com/article/Import-PST-files-or-SharePoint-data-to-Office-365-ba688e0a-0fcb-4bd7-8e57-2b669564ea84), [Configure caixas de correio de arquivo morto](https://support.office.com/article/Enable-archive-mailboxes-in-the-Office-365-Security-Compliance-Center-268a109e-7843-405b-bb3d-b9393b2342ce)e defina [as políticas de retenção](https://support.office.com/article/Retention-in-the-Office-365-Security-Compliance-Center-2a0fc432-f18c-45aa-a539-30ab035c608c) para email e outros conteúdos dentro da sua organização.
- **Search & Investigation** – fornece ferramentas de gerenciamento de casos de [pesquisa de conteúdo](https://support.office.com/article/Run-a-Content-Search-in-the-Office-365-Security-Compliance-Center-61852fd9-fe8a-4880-a339-cb19ed3bff4a), [log de auditoria](https://support.office.com/article/Search-the-audit-log-in-the-Office-365-Security-Compliance-Center-0d4d0f35-390b-4518-800e-0c7ec95e946c), quarentena e [descoberta eletrônica](https://support.office.com/article/Manage-eDiscovery-cases-in-the-Office-365-Security-Compliance-Center-edea80d6-20a7-40fb-b8c4-5e8c8395f6da) para fazer rapidamente Drill-in nas caixas de correio do Exchange Online, grupos e pastas públicas, SharePoint Online e OneDrive for Business.
- **Relatórios** – permite que você acesse [relatórios](https://support.office.com/article/Reports-in-the-Office-365-Security-Compliance-Center-7acd33ce-1ec8-49fb-b625-43bac7b58c5a) rapidamente para o SharePoint Online, o onedrive for Business, o Exchange Online e o Azure AD.
- **Garantia de serviço** : fornece informações sobre como a Microsoft mantém segurança, privacidade e conformidade com padrões globais para o Office 365, Azure, Microsoft Dynamics CRM Online, Microsoft Intune e outros serviços de nuvem. O também inclui acesso a aplicativos ISO, SOC e outros relatórios de auditoria de terceiros, além de controles auditados, que fornece detalhes sobre os vários controles que foram testados e verificados por auditores de terceiros do Office 365.

## <a name="service-assurance"></a>Garantia de serviço
Muitos de nossos clientes em setores regulamentados estão sujeitos a grandes requisitos de conformidade. Para realizar suas próprias avaliações de risco, os clientes normalmente precisam de informações detalhadas sobre como o Office 365 mantém a segurança e a privacidade de seus dados. A Microsoft está comprometida com a segurança e a privacidade dos dados do cliente em seus serviços de nuvem e para obter a confiança do cliente fornecendo uma visão transparente de suas operações e acesso fácil a relatórios e avaliações de conformidade independentes.

A garantia de serviço oferece transparência de operações e informações sobre como a Microsoft mantém a segurança, a privacidade e a conformidade dos dados do cliente no Office 365. Ele inclui relatórios de auditoria de terceiros junto com uma biblioteca de White papers, perguntas frequentes e outros materiais sobre os tópicos do Office 365, como criptografia de dados, resiliência de dados, gerenciamento de incidentes de segurança e muito mais. Os clientes podem usar essas informações para realizar suas próprias avaliações de riscos regulamentares. Os gerentes de conformidade podem atribuir a função "usuário de garantia de serviço" para conceder aos usuários acesso à garantia de serviço. O administrador de locatários também pode fornecer usuários externos, como auditores independentes, com acesso a informações no painel de garantia de serviço por meio do [Microsoft Cloud Service Trust portal](http://aka.ms/STP) (STP). Para obter detalhes sobre como acessar o STP, visite [introdução ao portal de confiança do serviço para o Office 365 for Business, Azure e Dynamics CRM Online subscriptions](http://aka.ms/STPHelp).

## <a name="onedrive-for-business-admin-center"></a>Centro de administração do OneDrive for Business
O novo centro de administração do Microsoft OneDrive ajuda você a gerenciar de forma rápida e fácil as configurações do OneDrive for Business de sua organização em um só lugar. Para usar o centro de administração do OneDrive, você deve permitir o acesso ao onedrive.com. Você também deve ser um administrador global para sua organização ou um administrador personalizado com a função de administrador do SharePoint. Acessar a visualização do centro de administração do OneDrive [https://admin.onedrive.com](https://admin.onedrive.com/)for Business em.

Os principais recursos incluem uma área de conformidade que oferece aos administradores links para o centro de gerenciamento apropriado para cenários principais, como pesquisar o log de auditoria, trabalhar com DLP, retenção, eDiscovery e alertas.

## <a name="related-links"></a>Links relacionados
- [Recursos de pesquisa e descoberta eletrônica](office-365-ediscovery-and-search-features.md)
- [Recursos de relatório do Office 365](office-365-reporting-features.md)
- [API da Atividade de Gerenciamento do Office 365](office-365-management-activity-api.md)
- [Migrações de caixas de correio do Office 365](office-365-mailbox-migrations.md)
- [Log interno de engenharia do Office 365](office-365-internal-logging.md)
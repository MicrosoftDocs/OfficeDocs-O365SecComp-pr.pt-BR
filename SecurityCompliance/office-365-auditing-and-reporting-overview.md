---
title: Auditoria e relatórios no Office 365
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
description: Visão geral de auditoria e recursos no Office 365, bem como garantia de serviço de relatório.
ms.openlocfilehash: 055a24523260bf14220d5436dcdd010f31f5d8cd
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524333"
---
# <a name="auditing-and-reporting-in-office-365"></a>Auditoria e relatórios no Office 365

## <a name="introduction"></a>Introdução
Serviços de nuvem da Microsoft inclui vários auditoria e relatórios de recursos que os clientes podem usar para rastrear atividades administrativas em seus locatários, como as alterações feitas em suas definições de configuração do inquilino do SharePoint Online e o Exchange Online e usuário e as alterações feitas pelos usuários para documentos e outros itens. Os clientes podem usar as informações de auditoria e os relatórios disponíveis no nossos serviços de nuvem para gerenciar a experiência do usuário, reduzir riscos e cumprir as obrigações de conformidade com mais eficiência.

## <a name="office-365-security--compliance-center"></a>Centro de Conformidade e Segurança do Office 365
O [Centro de conformidade e segurança do Office 365](https://support.office.com/article/Go-to-the-Office-365-Security-Compliance-Center-7e696a40-b86b-4a20-afcc-559218b7b1b8) é um portal de um único para proteger os dados no Office 365 e inclui muitas auditoria e recursos de relatório. É uma evolução do Centro de conformidade do Office 365. O Centro de conformidade & segurança foi projetado para organizações que tenham dados proteção ou necessidades de conformidade ou que deseja auditar a atividade de administrador e usuário. Você pode usar o Centro de conformidade e segurança para gerenciar a conformidade para todos os dados do Office 365 da sua organização. Você pode acessar o Centro de conformidade em & segurança [http://protection.office.com](http://protection.office.com/) usando sua conta de administração do Office 365.

O Centro de conformidade & segurança inclui painéis de navegação que fornecem acesso a vários recursos:
- **Alertas** - permite que você gerencie alertas, exibir alertas relacionados à segurança e gerenciar alertas avançadas usando o [Gerenciamento de segurança avançada](https://support.office.com/article/overview-of-office-365-cloud-app-security-81f0ee9a-9645-45ab-ba56-de9cbccab475). 
- **Permissões** - permite que você [atribua permissões](https://support.office.com/article/Give-users-access-to-the-Office-365-Security-Compliance-Center-2cfce2c8-20c5-47f9-afc4-24b059c1bd76) como administrador de conformidade, gerente de descoberta eletrônica e outras pessoas para as pessoas da sua organização para que eles podem executar tarefas no Centro de conformidade & segurança. Você pode atribuir permissões para a maioria dos recursos no Centro de conformidade & segurança, mas outras permissões devem ser configurados usando o Centro de administração do Exchange e o Centro de administração do SharePoint.
- **Gerenciamento de ameaça** - permite que você criar e aplicar políticas de gerenciamento de dispositivo usando o [Gerenciamento de dispositivos do Office 365 móveis](https://support.office.com/article/Overview-of-Mobile-Device-Management-for-Office-365-faa7d8e5-645d-4d59-839c-c8d4c1869e4a), para configurar políticas de [Prevenção de perda de dados](https://support.office.com/article/Overview-of-data-loss-prevention-policies-1966b2a7-d1e2-4d92-ab61-42efbb137f5e) (DLP) da sua organização, configurar o email filtragem, antimalware, email de identificado DomainKeys (DKIM), anexos seguros, links confiáveis e permissões do aplicativo.
- **Governança de dados** - permite [Importar dados do SharePoint de outros sistemas ao Office 365 ou de email](https://support.office.com/article/Import-PST-files-or-SharePoint-data-to-Office-365-ba688e0a-0fcb-4bd7-8e57-2b669564ea84), [Configurar caixas de correio de arquivo morto](https://support.office.com/article/Enable-archive-mailboxes-in-the-Office-365-Security-Compliance-Center-268a109e-7843-405b-bb3d-b9393b2342ce)e definir [políticas de retenção](https://support.office.com/article/Retention-in-the-Office-365-Security-Compliance-Center-2a0fc432-f18c-45aa-a539-30ab035c608c) para email e outros conteúdos dentro da sua organização.
- **Pesquisa & investigação** - fornece ferramentas de [pesquisa de conteúdo](https://support.office.com/article/Run-a-Content-Search-in-the-Office-365-Security-Compliance-Center-61852fd9-fe8a-4880-a339-cb19ed3bff4a), [o log de auditoria](https://support.office.com/article/Search-the-audit-log-in-the-Office-365-Security-Compliance-Center-0d4d0f35-390b-4518-800e-0c7ec95e946c), quarentena e [gerenciamento de casos de eDiscovery](https://support.office.com/article/Manage-eDiscovery-cases-in-the-Office-365-Security-Compliance-Center-edea80d6-20a7-40fb-b8c4-5e8c8395f6da) rapidamente detalhem atividade nas caixas de correio, grupos e pastas públicas, SharePoint Online do Exchange Online e o OneDrive for Business.
- **Relatórios** - permite acessar rapidamente [relatórios](https://support.office.com/article/Reports-in-the-Office-365-Security-Compliance-Center-7acd33ce-1ec8-49fb-b625-43bac7b58c5a) para o SharePoint Online, o OneDrive for Business, o Exchange Online e Azure AD.
- **Garantia de serviço** - fornece informações sobre como a Microsoft mantém a conformidade com padrões globais para o Office 365, Windows Azure, Microsoft Dynamics CRM Online, Microsoft Intune e outros serviços em nuvem, privacidade e segurança. Também inclui o acesso a ISO de terceiros, SOC e outros relatórios de auditoria, bem como controles auditadas, que fornece detalhes sobre os vários controles que foram testados e verificados por terceiros auditores do Office 365.

## <a name="service-assurance"></a>Garantia de serviço
Vários de nossos clientes em setores regulamentados estão sujeitos a requisitos de conformidade mais abrangentes. Para executar suas próprias avaliações de riscos, os clientes frequentemente precisam informações mais detalhadas sobre como o Office 365 mantém a segurança e privacidade dos seus dados. Microsoft tem o compromisso para a segurança e a privacidade de dados do cliente em seus serviços de nuvem e para a obtenção de confiança do cliente, fornecendo uma exibição transparente de suas operações e fácil acesso aos relatórios independente de conformidade e avaliações.

Serviço Assurance fornece transparência de operações e informações sobre como a Microsoft mantém a segurança, privacidade e conformidade de dados do cliente no Office 365. Ela inclui relatórios de auditoria de terceiros, juntamente com uma biblioteca de white papers, perguntas frequentes e outros materiais sobre tópicos do Office 365, como criptografia de dados, resiliência de dados, gerenciamento de incidentes de segurança e muito mais. Os clientes podem usar essas informações para executar suas próprias avaliações de riscos normativos. Oficiais de conformidade podem atribuir a função de "Usuário de garantia de serviço" conceder aos usuários acesso ao serviço de garantia. O administrador de locatário também pode fornecer a usuários externos, como auditores independentes, com o acesso às informações no painel garantia de serviço por meio do [Microsoft Cloud Service confiar Portal](http://aka.ms/STP) (STP). Para obter detalhes sobre como acessar o STP, visite [começar com o Portal de confiabilidade de serviço para o Office 365 para negócios, Windows Azure e Dynamics CRM Online assinaturas](http://aka.ms/STPHelp).

## <a name="onedrive-for-business-admin-center"></a>OneDrive para Business Admin Center
O novo centro de administração do Microsoft OneDrive ajuda rapidamente e facilita o gerenciamento OneDrive da sua organização para configurações de negócios em um único local. Para usar o Centro de administração do OneDrive, você deve permitir acesso a onedrive.com. Você também deve ser um administrador global para a sua organização ou um administrador personalizado com a função de administrador do SharePoint. Acessar o OneDrive for demonstração do Business admin center em [https://admin.onedrive.com](https://admin.onedrive.com/).

Os principais recursos incluem uma área de conformidade que permite aos administradores links ao centro de conformidade de segurança do Office 365 e para os principais cenários, como pesquisar o log de auditoria, trabalhando com DLP, retenção, eDiscovery e alertas.

## <a name="related-links"></a>Links relacionados
- [Recursos de pesquisa e descoberta eletrônica](office-365-ediscovery-and-search-features.md)
- [Recursos de relatório do Office 365](office-365-reporting-features.md)
- [API da Atividade de Gestão do Office 365](office-365-management-activity-api.md)
- [Migrações de caixas de correio do Office 365](office-365-mailbox-migrations.md)
- [Log interno de engenharia do Office 365](office-365-internal-logging.md)
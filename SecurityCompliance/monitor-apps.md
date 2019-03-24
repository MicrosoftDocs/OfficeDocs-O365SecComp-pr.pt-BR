---
title: Monitorar e relatar o status do aplicativo no Microsoft 365 Security
description: Descreve como você pode obter mais informações sobre o uso do aplicativo na nuvem em sua organização
keywords: segurança, malware, Microsoft 365, M365, central de segurança, monitor, relatório, aplicativos
ms.prod: w10
ms.mktglfcycl: deploy
ms.localizationpriority: medium
ms.author: ellevin
author: levinec
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.openlocfilehash: 02cc511532f65172aba2c0f98cdf594776f586a5
ms.sourcegitcommit: ef27da3ea5340d6e7a2eaa1288e2e005ef8e4788
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/23/2019
ms.locfileid: "30791532"
---
# <a name="monitor-and-report-app-status-in-microsoft-365-security"></a>Monitorar e relatar o status do aplicativo no Microsoft 365 Security

[!include[Prerelease�information](prerelease.md)]

Esses relatórios fornecem mais informações sobre como os aplicativos de nuvem estão sendo usados na sua organização, incluindo os tipos de aplicativos, seu nível de risco e alertas.

## <a name="monitor-email-accounts-at-risk"></a>Monitorar contas de email em risco

A **proteção de email** mostra as contas de email em risco. Você pode clicar em uma conta para investigar mais a central de segurança do Windows Defender.

![Cartão de proteção de email](./media/security-docs/email-protection.png)

## <a name="monitor-app-permissions-granted-by-users"></a>Monitorar permissões de aplicativo concedidas por usuários

**Cloud app Security-aplicativos OAuth** lista aplicativos descobertos pela Cloud app Security que receberam permissões pelos usuários. O catálogo de riscos do Cloud app Security inclui mais de 16.000 aplicativos que são avaliados usando mais de 70 fatores de risco.

Os fatores de risco são iniciados a partir de informações gerais, como o editor de aplicativos, medidas de segurança e controles, como se o aplicativo dá suporte para criptografia em repouso ou fornece um log de auditoria da atividade do usuário.

![Cartão de aplicativos OAuth do Cloud app Security](./media/security-docs/cloud-app-security-oauth-apps.png)

## <a name="monitor-cloud-app-user-accounts"></a>Monitorar contas de usuário do aplicativo na nuvem

**Contas de aplicativo em nuvem para análise** lista contas que podem exigir atenção.

![Contas de aplicativo de nuvem para o cartão de revisão](./media/security-docs/cloud-app-accounts-for-review.png)

## <a name="understand-which-cloud-apps-are-used"></a>Entender quais aplicativos de nuvem são usados

Os **aplicativos de nuvem descobertos (categorias)** mostram quais tipos de aplicativos estão sendo usados na sua organização e links para o painel de descoberta de nuvem no Cloud app Security. Para obter mais informações, consulte [QuickStart: work with untected apps](https://docs.microsoft.com/cloud-app-security/discovered-apps).  

![Cartão de categorias de aplicativos de nuvem descoberto](./media/security-docs/discovered-cloud-apps-categories.png)

## <a name="monitor-where-users-access-cloud-apps"></a>Monitorar onde os usuários acessam os aplicativos de nuvem

**Locais de atividade do aplicativo na nuvem** mostram onde os usuários estão acessando aplicativos em nuvem.

![Cartão de locais de atividade do Cloud app](./media/security-docs/cloud-app-activity-locations.png)

## <a name="monitor-health-for-infrastructure-workloads"></a>Monitorar a integridade das cargas de trabalho da infraestrutura

**Infrastructure Health** mostra alertas de status de integridade para cargas de trabalho de infraestrutura na central de segurança do Azure.

A central de segurança do Azure oferece gerenciamento de segurança unificado e proteção avançada contra ameaças em cargas de trabalho locais e em nuvem. Você pode coletar, Pesquisar e analisar dados de segurança de várias fontes, incluindo firewalls e outras soluções de parceiros.

Para obter mais informações, consulte a [documentação da central de segurança do Azure](https://docs.microsoft.com/azure/security-center/).

![Cartão de integridade de infraestrutura](./media/security-docs/infrastructure-health.png)

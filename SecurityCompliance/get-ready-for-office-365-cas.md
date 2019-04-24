---
title: Introdução ao Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.date: 02/15/2019
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: d9ee4d67-f2b3-42b4-9c9e-c4529904990a
description: Introdução ao uso do Office 365 Cloud app Security
ms.openlocfilehash: 89718adcbb7c77735db3009937d887e88d4a8bc3
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32254002"
---
# <a name="get-ready-for-office-365-cloud-app-security"></a>Introdução ao Office 365 Cloud App Security
  
|Avaliação * *\>**|Planejamento * *\>**|Implantação * *\>**|Utilização * * *|
|:-----|:-----|:-----|:-----|
|[Iniciar avaliação](office-365-cas-overview.md) <br/> |Você está aqui!  <br/> [Próxima etapa](turn-on-office-365-cas.md) <br/> |[Iniciar implantação](turn-on-office-365-cas.md) <br/> |[Começar a usar](utilization-activities-for-ocas.md) <br/> |
   
À medida que você se prepara para ativar e implementar o Office 365 Cloud app Security para sua organização, há algumas coisas a considerar. Use este artigo como guia para planejar o Office 365 Cloud app Security.
    
## <a name="step-1-identify-and-protect-your-global-and-security-administrator-accounts"></a>Etapa 1: identificar e proteger suas contas de administrador global e de segurança

Administradores globais, administradores de segurança e leitores de segurança podem acessar o portal de segurança do aplicativo Cloud do Office 365 para exibir políticas, revisar alertas e usar relatórios. Administradores globais e administradores de segurança podem definir políticas e realizar outras ações para proteger sua organização. (Para obter mais informações, consulte [permissões no centro de conformidade &amp; de segurança do Office 365](permissions-in-the-security-and-compliance-center.md).) Revise as contas de usuário da sua organização com permissões elevadas como precaução. 
  
 **[Proteja suas contas de administrador global do Office 365](https://docs.microsoft.com/office365/enterprise/protect-your-global-administrator-accounts)**. 
  
## <a name="step-2-turn-on-audit-logging-for-your-organization"></a>Etapa 2: ativar o log de auditoria para sua organização

Para que o Office 365 Cloud app Security funcione corretamente, o log de auditoria deve estar ativado. Isso geralmente é feito por um administrador do Exchange Online ou administrador global.
  
 **[Ativar ou desativar a pesquisa de log de auditoria do Office 365](turn-audit-log-search-on-or-off.md)**. 
  
## <a name="step-3-go-to-the-office-365-cloud-app-security-portal"></a>Etapa 3: Vá para o portal do Office 365 Cloud app Security

Você pode acessar o portal do Office 365 Cloud app Security entrando no [https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com) e entrando. 

Você também pode chegar lá no centro de conformidade de &amp; segurança do Office 365. Veja uma boa maneira de fazer isso:

1. AcEsse [https://protection.office.com](https://protection.office.com) e entre. (Isso leva você para o centro &amp; de conformidade de segurança.)
    
2. Vá até **alertas** \> **Gerenciar alertas avançados**.
    
3. Escolha **ir para o office 365 Cloud app Security** para ir para o portal do Office 365 Cloud app Security.<br> ![Escolha Gerenciar alertas avançados para ir para o Office 365 Cloud app Security](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)<br>Quando você vai para o portal do Office 365 Cloud app Security, a primeira página que você vê é a página de políticas, que se assemelha à seguinte imagem:<br>![Ao acessar o portal do Office 365 Cloud app Security, comece com a página políticas](media/5cb8833c-4e08-438c-bab3-91b5106f6f3f.png)<br>
  
## <a name="step-4-define-policies-and-set-up-alerts-amp-actions"></a>Etapa 4: definir políticas e configurar ações de &amp; alerta

Administradores globais e administradores de segurança definem políticas no Office 365 Cloud app Security. Durante o processo de definição de políticas, alertas e ações também são definidos. Um alerta é uma notificação baseada em critérios que aparece em um modo de exibição ou enviado por email. 
  
Há dois tipos de alertas no Office 365 Cloud app Security: alertas de detecção de anomalias que detectam atividades suspeitas e alertas de atividade, que são definidos para atividades que podem ser atypical para sua organização. Alertas notificam administradores globais e administradores de segurança quando há uma atividade no seu ambiente do Office 365 que é incomum para sua organização.
  
ConFira os seguintes recursos para saber mais:
  
- [Políticas de atividades e alertas no Office 365 Cloud App Security](activity-policies-and-alerts.md)
    
- [Políticas de detecção de anomalias no Office 365 Cloud App Security](anomaly-detection-policies-in-ocas.md)
    
- [Examinar e adotar medidas nos alertas do Office 365 Cloud app Security](review-office-365-cas-alerts.md)
    

## <a name="step-5-set-up-conditional-access-app-control"></a>Etapa 5: configurar o controle de aplicativo de acesso condicional

Configurar e impor controles nos aplicativos da sua organização, com base em determinadas condições, como quais usuários podem usar quais aplicativos e onde. Defina as políticas de acesso de aplicativo de usuário e de sessão para determinar se os documentos confidenciais podem ser baixados e criptografados, bloquear o acesso a determinados aplicativos, definir o modo somente leitura para determinados aplicativos e restringir sessões de usuário de redes não corporativas.

ConFira os seguintes recursos para saber mais:

- [Proteger os aplicativos com o Controle de Aplicativos de Acesso Condicional do Office 365 Cloud App Security](ocas-conditional-access-app-control.md)

- [Implantar o Controle de Aplicativos de Acesso Condicional nos aplicativos do Office 365](ocas-deploy-conditional-access-app-control.md)

## <a name="step-6-learn-about-your-organizations-cloud-usage"></a>Etapa 6: Saiba mais sobre o uso da nuvem da sua organização

Como administrador global, administrador de segurança ou leitor de segurança, você pode aprender sobre o uso da nuvem da sua organização por meio de relatórios e um painel de descoberta de nuvem (também chamado de descoberta de aplicativos de produtividade). Este painel mostra informações sobre usuários, aplicativos, tráfego da Web e níveis de risco.
  
![No portal CAS do Office 365, escolha descobrir \> painel de descoberta de nuvem](media/61269290-fd82-4d4b-8045-aea1ebc82287.png)
  
para ir para o painel de descoberta de aplicativos de produtividade, no portal do Office 365 Cloud app Security, escolha **descobrir** \> **painel de descoberta de nuvem**.
  
![No portal CAS do Office 365, escolha descobrir](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)
  
Para preencher relatórios com as informações de que você precisa, carregue seus arquivos de log dos firewalls e proxies da sua organização. Para saber mais, confira os seguintes recursos:
  
- [Criar relatórios de descoberta de aplicativos no Office 365 Cloud app Security](create-app-discovery-reports-in-ocas.md)
    
- [Analisar descobertas de aplicativos do Office 365 Cloud App Security](review-app-discovery-findings-in-ocas.md)
    
## <a name="step-7-manage-apps-that-your-organization-is-using-to-access-office-365"></a>Etapa 7: gerenciar aplicativos que sua organização está usando para acessar o Office 365

Como administrador global ou administrador de segurança, você pode gerenciar aplicativos, como aplicativos personalizados ou aplicativos de terceiros, que as pessoas em sua organização estão usando em seus dispositivos com o Office 365. Por exemplo, suponha que alguém tenha baixado um aplicativo personalizado que deseja usar com o Office 365. Você pode revisar os aplicativos que as pessoas estão usando, proibir aplicativos não confiáveis ou marcar aplicativos como aprovados para seus fins de controle. [Gerenciar aplicativos OAuth usando o Office 365 Cloud app Security](manage-app-permissions-in-ocas.md).
  
## <a name="step-8-create-a-maintenance-plan"></a>Etapa 8: criar um plano de manutenção

Depois de configurar e configurar o Office 365 Cloud app Security, convém executar determinadas tarefas de utilização como um administrador global do Office 365 ou administrador de segurança para sua organização.
Ao executar essas tarefas, você ajudará a garantir que o Office 365 Cloud app Security esteja configurado corretamente, suas políticas estejam atualizadas e sua organização perceba o valor do Office 365. Use este artigo como um guia para ajudá-lo a planejar essas tarefas. Veja [as atividades de utilização após a implantação do Office 365 Cloud app Security](utilization-activities-for-ocas.md).

## <a name="optional-step-9-use-your-siem-server-with-office-365-cloud-app-security"></a>Opcion Etapa 9: usar seu servidor SIEM com o Office 365 Cloud app Security

A sua organização está usando um servidor de gerenciamento de eventos e informações de segurança (SIEM)? O Office 365 Cloud app Security agora pode se integrar ao seu servidor SIEM para habilitar o monitoramento centralizado de alertas. A integração com um serviço SIEM permite que você proteja melhor seus aplicativos de nuvem enquanto mantém seu fluxo de trabalho de segurança normal, automação de procedimentos de segurança e correlação entre eventos locais e baseados em nuvem. O agente SIEM é executado em seu servidor, recebe alertas do Office 365 Cloud app Security e os transfere para seu servidor SIEM. Consulte [integração do Siem com o Office 365 Cloud app Security](integrate-your-siem-server-with-office-365-cas.md).
  
## <a name="next-steps"></a>Próximas etapas

- [Ativar o Office 365 Cloud app Security](turn-on-office-365-cas.md)
    
- Experimente nosso [Guia de laboratório de teste](https://docs.microsoft.com/office365/enterprise/cloud-app-security-for-your-office-365-dev-test-environment) para obter uma experiência prática onde você pode demonstrar os recursos avançados do Office 365 Cloud app Security e criar uma prova de conceito. 
    


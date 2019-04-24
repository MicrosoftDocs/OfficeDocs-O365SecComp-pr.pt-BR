---
title: Políticas de atividades e alertas no Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/28/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 367f25d3-10a0-4a91-bdae-70ebb7a79c98
description: Definir políticas de atividade com o Office 365 Cloud app Security para configurar alertas a serem acionados quando atividades específicas acontecem ou acontecem com muita frequência. Configurando políticas para acionar alertas, você pode ser notificado sobre e monitorar atividades específicas.
ms.openlocfilehash: cfa58182ea35551ca3a3807c23e09c9f87c7be82
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32242700"
---
# <a name="activity-policies-and-alerts-in-office-365-cloud-app-security"></a>Políticas de atividades e alertas no Office 365 Cloud App Security

|Avaliação * *\>**|Planejamento * *\>**|Implantação * *\>**|Utilização * * *|
|:-----|:-----|:-----|:-----|
|[Iniciar avaliação](office-365-cas-overview.md) <br/> |[Iniciar planejamento](get-ready-for-office-365-cas.md) <br/> |Você está aqui!  <br/> [Próxima etapa](anomaly-detection-policies-in-ocas.md) <br/> |[Começar a usar](utilization-activities-for-ocas.md) <br/> |
   
Com o Office 365 Cloud app Security, as políticas avançadas de gerenciamento de nuvem disparam alertas para atividades específicas que acontecem ou acontecem com muito frequência. Por exemplo, suponha que um usuário tente entrar no Office 365 e falhe 70 vezes em um minuto. Suponha que outro usuário Baixe 7.000 arquivos ou que esteja conectado do Canadá, quando esse usuário deve estar em outro local. Ou pior, suponha que a conta de alguém tenha sido comprometida e um invasor esteja usando essa conta para acessar os aplicativos de nuvem e dados confidenciais da sua organização.
  
Se você for um [administrador global ou administrador de segurança](permissions-in-the-security-and-compliance-center.md), os alertas de atividade o notificarão quando eventos como esses ocorrerem. Você pode então tomar ações específicas, como suspender uma conta de usuário até que você possa investigar o que aconteceu.
  
> [!NOTE]
> As políticas de segurança do aplicativo Cloud do Office 365 são diferentes das [políticas de alerta &amp; no centro de conformidade de segurança do Office 365](alert-policies.md). As políticas de atividade descritas neste artigo são definidas no portal do Office 365 Cloud app Security e podem ajudá-lo a gerenciar melhor o ambiente de nuvem da sua organização. 
  
## <a name="before-you-begin"></a>Antes de começar

Verifique se:
  
- Sua organização tem o [Office 365 Cloud app Security](office-365-cas-overview.md)e o serviço está [ativado](turn-on-office-365-cas.md).
    
- O [registro em log de auditoria](turn-audit-log-search-on-or-off.md) está ativado para seu ambiente do Office 365. 
    
- Você é um administrador global ou administrador de segurança do Office 365.
    
## <a name="create-a-new-activity-policy"></a>Criar uma nova política de atividade

1. Como administrador global ou administrador de segurança, vá para o portal do Cloud app Security[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)() e entre. <br>Isso leva você à página de políticas de segurança do aplicativo nuvem do Office 365.<br>![Ao acessar o portal do Office 365 Cloud app Security, comece com a página políticas](media/5cb8833c-4e08-438c-bab3-91b5106f6f3f.png)
  
2. Clique em **criar política**e selecione **política de atividade**.<br>![Ao criar uma política no O365 CAS, você pode escolher entre políticas de atividade e políticas de detecção de anomalias.](media/79f34535-ddf9-4a5b-a0a3-8766bf9c174c.png)
  
3. Na página **criar política de atividade** , especifique o **nome** e a **Descrição**da política. Para basear sua política em um modelo padrão, escolha uma na lista **modelo de política** ou crie sua própria política sem usar um modelo.<br>![Você pode criar políticas de atividade com o Office 365 Cloud app Security.](media/4083a76f-7074-4d6a-8200-6d76d49259d7.png)
  
4. Escolha uma **severidade de política** (baixa, média ou alta) que mede o grau de seriedade para você se essa política disparar um alerta. Isso ajudará você a filtrar alertas quando estiver examinando mais tarde. 
    
5. Escolha uma **categoria** para esta política. Isso ajudará você a filtrar e classificar alertas que foram disparados ou a políticas de grupo quando estiver revisando a fazer alterações. 
    
6. Escolha **filtros de atividade** para configurar outras ações ou métricas que irão disparar um alerta baseado nessa política. 
    
7. Em **parâmetros de correspondência de atividade**, especifique se uma violação de política será disparada quando uma única atividade corresponder aos filtros ou se um número especificado de atividades repetidas for necessário antes de os gatilhos de alerta.<br>Se você selecionar **atividade repetida**, especifique o número de atividades, o período de tempo e se uma violação será contabilizada para um usuário dentro de um aplicativo específico ou para o mesmo usuário com qualquer aplicativo.
    
8. Opcionalmente, você pode selecionar **criar alerta** para criar alertas adicionais para receber notificações dessa política (por email, mensagem de texto ou ambos).<br>**Certifique-se de que seu provedor de email não bloqueie `no-reply@cloudappsecurity.com`emails enviados **. 
  
9. Escolha as **ações** que devem ser executadas quando um alerta é disparado para suspender o usuário ou solicitar que o usuário entre novamente nos aplicativos do Office 365. 
    
10. Escolha **criar** para concluir a criação da política. 
    
## <a name="next-steps"></a>Próximas etapas

- [Políticas de detecção de anomalias](anomaly-detection-policies-in-ocas.md)
    
- [Integrar seu servidor SIEM](integrate-your-siem-server-with-office-365-cas.md)
    
- [ReVisar e executar ação em alertas](review-office-365-cas-alerts.md)
    
- [Agrupar seus endereços IP para simplificar o gerenciamento](group-your-ip-addresses-in-ocas.md)
    


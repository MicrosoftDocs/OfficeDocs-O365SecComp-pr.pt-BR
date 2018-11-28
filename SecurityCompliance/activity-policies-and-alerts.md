---
title: Políticas de atividades e alertas no Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/26/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 367f25d3-10a0-4a91-bdae-70ebb7a79c98
description: Defina políticas de atividade com segurança de aplicativo do Office 365 nuvem para configurar alertas para disparar quando atividades específicas acontecem ou acontecer muito frequentemente. Configurando políticas para acionar os alertas, você pode ser notificado sobre e monitora atividades específicas.
ms.openlocfilehash: 87173b5551a41b700728efff25aedeafa93188ee
ms.sourcegitcommit: 2cf7f5bb282c971d33e00f65d9982a3f14aec74e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/27/2018
ms.locfileid: "26706355"
---
# <a name="activity-policies-and-alerts-in-office-365-cloud-app-security"></a>Políticas de atividades e alertas no Office 365 Cloud App Security

Gerenciamento de segurança avançada do Office 365 agora é segurança de aplicativo de nuvem do Office 365.
  
|Avaliação * *\>**|Planejamento * *\>**|Implantação * *\>**|Utilização * * *|
|:-----|:-----|:-----|:-----|
|[Comece a avaliar](office-365-cas-overview.md) <br/> |[Começar a planejar](get-ready-for-office-365-cas.md) <br/> |Você está aqui!  <br/> [Próxima etapa](anomaly-detection-policies-in-ocas.md) <br/> |[Iniciar a utilização](utilization-activities-for-ocas.md) <br/> |
   
Com a segurança de aplicativo de nuvem do Office 365, políticas de gerenciamento avançado de nuvem disparam alertas para atividades específicas que acontecesse ou acontecer muito frequentemente. Por exemplo, suponha que um usuário tenta entrar no Office 365 e falha 70 vezes em um minuto. Suponha que outro usuário baixa 7.000 arquivos ou parece estar conectado no Canadá, quando o usuário deve para estar em outro local. Ou pior, suponha que a conta de alguém foi comprometida e um invasor esteja usando essa conta para acessar dados confidenciais e aplicativos de nuvem da sua organização.
  
Se você for um [administrador global ou administrador de segurança](permissions-in-the-security-and-compliance-center.md), os alertas de atividade notificam quando eventos, como estas ocorre. Em seguida, você pode tirar ações específicas, como suspendendo uma conta de usuário até que você possa investigar o que aconteceu.
  
> [!NOTE]
> Diretivas de segurança de aplicativo de nuvem do Office 365 são diferentes dos [políticas de segurança do Office 365 de alerta &amp; Centro de conformidade](alert-policies.md). A atividade políticas descritas neste artigo são definidas no portal de segurança de aplicativo de nuvem do Office 365 e poderá ajudá-lo gerenciar o ambiente de nuvem da sua organização. 
  
## <a name="before-you-begin"></a>Antes de começar

Verifique se:
  
- Sua organização tem [Segurança de aplicativo de nuvem do Office 365](office-365-cas-overview.md)e o serviço está [ativado](turn-on-office-365-cas.md).
    
- [Log de auditoria](turn-audit-log-search-on-or-off.md) está ativado para o seu ambiente do Office 365. 
    
- Você é um administrador global ou administrador de segurança para o Office 365.
    
## <a name="create-a-new-activity-policy"></a>Criar uma nova política de atividade

1. Como administrador global ou administrador de segurança, vá para [https://security.microsoft.com](https://security.microsoft.com) e entrar usando sua conta do trabalho ou da escola. 
    
2. Na segurança &amp; Centro de conformidade, escolha **alertas** \> **avançadas de gerenciar alertas**.
    
3. Escolha **vá para segurança de aplicativo do Office 365 nuvem**.
    
    Isso leva você para a página de diretivas de segurança de aplicativo de nuvem do Office 365.
    
    ![Quando você vai para o portal de segurança de aplicativo de nuvem do Office 365, você iniciar com a página de políticas](media/5cb8833c-4e08-438c-bab3-91b5106f6f3f.png)
  
4. Clique em **Criar política**e selecione **a política de atividade**.
    
    ![Quando você cria uma política no O365 CAS, você pode escolher entre as políticas de atividade e detecção de anomalias.](media/79f34535-ddf9-4a5b-a0a3-8766bf9c174c.png)
  
5. Na página **criar a política de atividade** , especifique o **nome da diretiva** e a **Descrição**. Para basear sua política em um modelo padrão, escolha uma opção na lista **modelo de política** ou criar sua própria política sem usar um modelo. 
    
    ![Você pode criar políticas de atividade com segurança de aplicativo de nuvem do Office 365.](media/4083a76f-7074-4d6a-8200-6d76d49259d7.png)
  
6. Escolha a **gravidade da política** (baixa, média ou alta) que mede como sérios é a você se essa diretiva dispara um alerta. Isso ajudará você filtrar alertas quando você estiver revisá-las mais tarde. 
    
7. Escolha uma **categoria** para esta diretiva. Isso ajudará você filtrar e classificar alertas que tiverem sido disparadas, ou quando você estiver revisá-las para fazer alterações de diretivas de grupo. 
    
8. Escolha **os filtros de atividade** para configurar outras ações ou métricas que acionarão um alerta com base nesta diretiva. 
    
9. Em **atividade correspondem a parâmetros**, especifique se uma violação de política será acionada quando os filtros corresponde a uma única atividade, ou se um número especificado de atividades repetidas for necessária antes do alerta dispara.
    
    Se você selecionar **repetida atividade**, especifique o número de atividades, o intervalo de tempo, e se uma violação contará para um usuário em um aplicativo específico ou para o mesmo usuário com qualquer aplicativo.
    
10. Opcionalmente, você pode selecionar **criar alerta** para criar alertas adicionais para receber notificações dessa diretiva (via email, mensagem de texto ou ambos). 
    
    > [!IMPORTANT]
    > Certifique-se de que o seu provedor de email não bloqueie emails enviados a partir de no-reply@cloudappsecurity.com. 
  
11. Escolha as **ações** que devem ser tomadas quando um alerta é acionado para suspender o usuário ou exigem que o usuário entrar novamente para aplicativos do Office 365. 
    
12. Escolha **criar** para concluir a criação de sua política. 
    
## <a name="next-steps"></a>Próximas etapas

- [Políticas de detecção de anomalia](anomaly-detection-policies-in-ocas.md)
    
- [Integrar seu servidor SIEM](integrate-your-siem-server-with-office-365-cas.md)
    
- [Revise e agir em alertas](review-office-365-cas-alerts.md)
    
- [Seus endereços IP para simplificar o gerenciamento de grupo](group-your-ip-addresses-in-ocas.md)
    


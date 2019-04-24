---
title: Revisar e tomar atitudes sobre alertas no Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 97e9c3d9-df89-458e-924b-369becee5532
description: Use a página alertas no Office 365 Cloud app Security para exibir possíveis problemas e tomar ações. Você pode descartar ou resolver alertas e, se necessário, suspender uma conta de usuário.
ms.openlocfilehash: ddef10293fca7b722a13babdca5c05bbe2398cb3
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32261470"
---
# <a name="review-and-take-action-on-alerts-in-office-365-cloud-app-security"></a>Revisar e tomar atitudes sobre alertas no Office 365 Cloud App Security
  
|Avaliação * *\>**|Planejamento * *\>**|Implantação * *\>**|Utilização * * *|
|:-----|:-----|:-----|:-----|
|[Iniciar avaliação](office-365-cas-overview.md) <br/> |[Iniciar planejamento](get-ready-for-office-365-cas.md) <br/> |[Iniciar implantação](turn-on-office-365-cas.md) <br/> |Você está aqui!  <br/> [Próximas etapas](#next-steps) <br/> |
   
Você pode usar a página alertas no Office 365 Cloud app Security para exibir possíveis problemas e, se necessário, tomar medidas.
  
> [!NOTE]
> Você deve ser um administrador global ou administrador de segurança para executar as tarefas neste artigo. Consulte [permissões no centro de conformidade de &amp; segurança do Office 365](permissions-in-the-security-and-compliance-center.md). 
  
## <a name="how-to-get-to-the-alerts-page"></a>Como acessar a página alertas

1. Vá para o portal do Cloud app Security[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)() e entre.
  
2. Na barra de navegação na parte superior da tela, escolha **alertas**.<br/>![Na página alertas, você pode ver os alertas que foram disparados e as ações realizadas.](media/3b53d4c9-4b13-435d-8547-8c0f9ae6b914.png)
 
> [!NOTE]
> Os alertas de segurança do Cloud app também estão visíveis no centro de conformidade do & de segurança (vá para **alertas** > ,**exibir alertas**. No momento, no entanto, você deve resolver esses alertas no portal do Cloud app Security e no centro de conformidade do & de segurança. Para saber mais, consulte [viewIng Cloud app Security Alerts](alert-policies.md#viewing-cloud-app-security-alerts).) 
 
## <a name="review-and-handle-alerts"></a>Examinar e lidar com alertas

Os alertas ajudam a identificar atividades no seu ambiente de nuvem do Office 365 que você pode querer investigar. Você também pode optar por criar novas políticas ou editar políticas existentes com base nos alertas exibidos. Por exemplo, se você vir um administrador fazendo logon a partir de um local estranho, poderá decidir configurar uma política que impede que os administradores entrem no Office 365 de determinados locais.
  
> [!TIP]
> Você pode filtrar os alertas por **categoria** ou por **gravidade** para que possa gerenciar o mais importante primeiro. 
  
Para cada alerta, examine o que causou o resultado para que você possa decidir qual ação executar. Para ver mais detalhes sobre um alerta e realizar ações, como resolver o alerta ou suspender uma conta de usuário, escolha o alerta para abrir uma página de detalhes. Na página detalhes, você pode revisar o log de atividades, contas e usuários relacionados ao alerta e realizar ações como as seguintes:
  
- **Ignorar** Se o alerta for falso positivo, ignore-o. Opcionalmente, você pode adicionar um comentário explicando por que você o descartau. 
    
- **Resolver alerta** Se o alerta foi disparado por uma atividade que você sabe que não é uma ameaça, resolva-o. Opcionalmente, você pode adicionar um comentário explicando por que você o resolveu. 
    
- **Suspender** Se você suspeitar de entradas não autorizadas em uma conta, por exemplo, alguém entrando de outro país quando você sabe que a pessoa está fisicamente em um escritório local, você pode [suspender a conta](suspend-or-restore-an-account-in-ocas.md) enquanto investiga o que está acontecendo. 
    
## <a name="next-steps"></a>Próximas etapas

- [Investigar uma atividade](investigate-an-activity-in-office-365-cas.md)
    
- [Suspender ou restaurar uma conta de usuário](suspend-or-restore-an-account-in-ocas.md)
    
- Exibir uma lista de [logs de tráfego da Web e fontes de dados](web-traffic-logs-and-data-sources-for-ocas.md) suportados
    
- ReVisar suas [atividades de utilização do Office 365 Cloud app Security](utilization-activities-for-ocas.md)
    


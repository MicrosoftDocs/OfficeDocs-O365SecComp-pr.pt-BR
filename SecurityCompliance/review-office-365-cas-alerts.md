---
title: Revisar e tomar atitudes sobre alertas no Office 365 Cloud App Security
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
ms.assetid: 97e9c3d9-df89-458e-924b-369becee5532
description: Use a página alertas na segurança de aplicativo de nuvem do Office 365 para exibir possíveis problemas e executar ação. Você pode descartar ou resolver alertas e, se necessário, suspender uma conta de usuário.
ms.openlocfilehash: 62431adc73354e573978781f120a11746aef08d9
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523443"
---
# <a name="review-and-take-action-on-alerts-in-office-365-cloud-app-security"></a>Revisar e tomar atitudes sobre alertas no Office 365 Cloud App Security
  
|Avaliação * *\>**|Planejamento * *\>**|Implantação * *\>**|Utilização * * *|
|:-----|:-----|:-----|:-----|
|[Comece a avaliar](office-365-cas-overview.md) <br/> |[Começar a planejar](get-ready-for-office-365-cas.md) <br/> |[Começar a implantar](turn-on-office-365-cas.md) <br/> |Você está aqui!  <br/> [Próximas etapas](#next-steps) <br/> |
   
Você pode usar a página alertas na segurança de aplicativo de nuvem do Office 365 para exibir possíveis problemas e, se necessário, executar a ação.
  
> [!NOTE]
> Você deve ser um administrador global ou administrador de segurança para executar as tarefas neste artigo. Consulte [Permissions in a segurança do Office 365 &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md). 
  
## <a name="how-to-get-to-the-alerts-page"></a>Como chegar à página de alertas

1. Como administrador global ou administrador de segurança, vá para [https://protection.office.com](https://protection.office.com) e entrar usando sua conta do trabalho ou da escola. 
    
2. Na segurança &amp; Centro de conformidade, escolha **alertas** \> **avançadas de gerenciar alertas**.
    
3. Escolha **vá para segurança de aplicativo do Office 365 nuvem**.
    
    ![Na segurança &amp; Centro de conformidade, escolha gerenciar alertas avançadas para ir à segurança de aplicativo de nuvem do Office 365](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)
  
4. Na barra de navegação na parte superior da tela, escolha **alertas**.
    
    ![Na página alertas, você pode ver os alertas que foram acionados e quaisquer ações tomadas.](media/3b53d4c9-4b13-435d-8547-8c0f9ae6b914.png)
  
## <a name="review-and-handle-alerts"></a>Revisão e a alça de alertas

Alertas ajudarão-lo a identificar atividades no seu ambiente de nuvem do Office 365 que você talvez queira investigar melhor. Você também pode decidir criar novas políticas ou editar políticas existentes, com base nos alertas que você vê. Por exemplo, se você vir um administrador de logon de um local estranho, você decidir definir uma política que impede que os administradores entrando para o Office 365 de determinados locais.
  
> [!TIP]
> Você pode filtrar os alertas por **categoria** ou por **gravidade** para que você possa gerenciar os mais importantes primeiro. 
  
Para cada tipo de alerta, considere o que causou para decidir qual ação a ser executada. Para obter mais detalhes sobre um alerta e ações, como resolver o alerta ou suspendendo uma conta de usuários, escolha o alerta para abrir uma página de detalhes. Na página de detalhes, você pode examinar o log da atividade, contas e usuários que estão relacionados ao alerta e realizar ações como o seguinte:
  
- **Descartar** Se o alerta era um falso positivo, descartá-lo. Opcionalmente, você pode adicionar um comentário que explica por que você descartado. 
    
- **Resolver alerta** Se o alerta tiver sido disparado por uma atividade que você sabe que não é uma ameaça, resolvê-lo. Opcionalmente, você pode adicionar um comentário que explica por que você resolvido. 
    
- **Suspender** Se você suspeitar de entrada não autorizada ins em uma conta, por exemplo, alguém entrando de outro país quando você sabe que a pessoa está fisicamente em um escritório local, é possível [suspender a conta](suspend-or-restore-an-account-in-ocas.md) enquanto você investigar o que está acontecendo. 
    
## <a name="next-steps"></a>Próximas etapas

- [Investigar uma atividade](investigate-an-activity-in-office-365-cas.md)
    
- [Suspender ou restaurar uma conta de usuário](suspend-or-restore-an-account-in-ocas.md)
    
- Exibir uma lista de suportadas [fontes de dados e logs de tráfego da Web](web-traffic-logs-and-data-sources-for-ocas.md)
    
- Revise suas [atividades de utilização para segurança de aplicativo de nuvem do Office 365](utilization-activities-for-ocas.md)
    


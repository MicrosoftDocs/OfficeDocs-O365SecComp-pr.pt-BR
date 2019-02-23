---
title: Ativar o Office 365 Cloud App Security
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
ms.assetid: ba919c73-d021-404d-9850-eec57e78678c
description: Leia este artigo para saber como ativar o Office 365 Cloud app Security, ativado pela Cloud app Security no Microsoft Azure.
ms.openlocfilehash: 1227545b1e4d1521dc1820342f09aabdf16ec2c6
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220361"
---
# <a name="turn-on-office-365-cloud-app-security"></a>Ativar o Office 365 Cloud App Security
  
|Avaliação * *\>**|Planejamento * *\>**|Implantação * *\>**|Utilização * * *|
|:-----|:-----|:-----|:-----|
|[Iniciar avaliação](office-365-cas-overview.md) <br/> |[Iniciar planejamento](get-ready-for-office-365-cas.md) <br/> |Você está aqui!  <br/> [Próxima etapa](activity-policies-and-alerts.md) <br/> |[Começar a usar](utilization-activities-for-ocas.md) <br/> |
  
## <a name="turn-on-office-365-cloud-app-security"></a>Ativar o Office 365 Cloud App Security

> [!IMPORTANT]
> Você deve ser um administrador global ou administrador de segurança para executar a tarefa a seguir. Para saber mais, confira [permissões no centro de conformidade &amp; de segurança do Office 365](permissions-in-the-security-and-compliance-center.md). Para que o Office 365 Cloud app Security funcione corretamente, o **log de auditoria deve estar ativado** para o seu ambiente do Office 365. Para obter mais informações, consulte [Ativar ou desativar a pesquisa de log de auditoria do Office 365](turn-audit-log-search-on-or-off.md). 
  
1. Como administrador global ou administrador de segurança, acesse [https://protection.office.com](https://security.microsoft.com) e entre usando sua conta corporativa ou de estudante para o Office 365. (Isso leva você para o centro &amp; de conformidade de segurança.) 
    
2. Vá até **alertas** \> **Gerenciar alertas avançados**.
    
3. Selecione **ativar o Office 365 Cloud app Security**.
    
4. Escolha **ir para o Office 365 Cloud app Security**.<br/>![No centro de &amp; conformidade de segurança, escolha Gerenciar alertas avançados para acessar o Office 365 Cloud app Security](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)<br/>Isso leva você para o portal do Office 365 Cloud app Security, onde você pode exibir relatórios e criar ou editar suas políticas.

Depois de ter ativado o Office 365 Cloud app Security, você pode ir para o portal do Cloud app Security visitando [https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com) e entrando.
    
> [!NOTE]
> Quando você ativa o Office 365 Cloud app Security, as informações de auditoria sobre suas contas de usuário e as atividades do usuário do Office 365 são transferidas para o [Microsoft Cloud app Security](https://aka.ms/whatiscas). Isso permite que o Office 365 forneça alertas avançados, filtragem e outros recursos para que você possa obter informações e tomar medidas sobre atividades suspeitas. 
  
## <a name="next-steps"></a>Próximas etapas

- [Políticas de atividade](activity-policies-and-alerts.md)
    
- [Políticas de detecção de anomalias](anomaly-detection-policies-in-ocas.md)
    
- [Integrar seu servidor SIEM](integrate-your-siem-server-with-office-365-cas.md)
    
- [Agrupar seus endereços IP para simplificar o gerenciamento](group-your-ip-addresses-in-ocas.md)
    


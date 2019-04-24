---
title: Suspender ou restaurar uma conta de usuário no Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 12/03/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 5f02d20f-b9aa-4b2f-ad2d-506a4a3c4540
description: 'Com o Office 365 Cloud app Security, as ações de governança que você pode executar são suspender ou cancelar a suspensão de uma conta de usuário. '
ms.openlocfilehash: d162be9d4e5382c6c03c63ae1b30043edbf0295b
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32260300"
---
# <a name="suspend-or-restore-a-user-account-in-office-365-cloud-app-security"></a>Suspender ou restaurar uma conta de usuário no Office 365 Cloud App Security

|Avaliação * *\>**|Planejamento * *\>**|Implantação * *\>**|Utilização * * *|
|:-----|:-----|:-----|:-----|
|[Iniciar avaliação](office-365-cas-overview.md) <br/> |[Iniciar planejamento](get-ready-for-office-365-cas.md) <br/> |[Iniciar implantação](turn-on-office-365-cas.md) <br/> |Você está aqui!  <br/> [Próximas etapas](#next-steps)<br/> |
   
Suponha que você receba um alerta de que uma das contas de usuário da sua organização para o Office 365 foi comprometida. Ou, suponha que você recebeu um alerta que indica que algo está errado com uma conta de usuário. Com o Office 365 Cloud app Security, você pode suspender uma conta de usuário e restaurá-la posteriormente após investigar os alertas recebidos.
  
> [!NOTE]
> O Office 365 Cloud app Security está disponível no Office 365 Enterprise e5. Se sua organização estiver usando outra assinatura do Office 365 Enterprise, o Office 365 Cloud app Security pode ser adquirido como um complemento. (como administrador global, no centro de administração do Microsoft 365, escolha **cobrança** \> **adicionar assinaturas**.) Para obter mais informações, consulte [Descrição do serviço da plataforma do office 365 &amp; : centro de conformidade de segurança](https://technet.microsoft.com/en-us/library/dn933793.aspx) do Office 365 e [comprar ou editar um complemento para o Office 365 for Business](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6). 
  
## <a name="to-suspend-a-user-account-in-office-365-cloud-app-security"></a>Para suspender uma conta de usuário no Office 365 Cloud app Security

Ao suspender uma conta de usuário, você impede o usuário de entrar novamente. É o mesmo que editar a conta de usuário diretamente no Office 365 para definir o status de entrada para **entrar em bloqueio**.
  
> [!NOTE]
> Se você impedir que um usuário entre no Office 365, suspenda-o ou editando seu status de entrada, lembre-se de que pode levar uma hora ou, assim, entrar em todos os dispositivos e clientes do usuário ([Editar ou alterar um usuário no Office 365](https://support.office.com/article/42BB3F17-8F9D-4182-B434-5F1C8024E614#SingleUserPreview)). Se o usuário estiver conectado ao Office 365, o bloco entrará em vigor sempre que o Office 365 exigir que eles entrem novamente. 
  
1. Como [administrador global ou administrador de segurança](permissions-in-the-security-and-compliance-center.md), acesse [https://protection.office.com](https://protection.office.com) e entre usando sua conta corporativa ou de estudante. (Isso leva você para o centro &amp; de conformidade de segurança.) 
    
2. No centro de &amp; conformidade de segurança, escolha **alertas** \> **Gerenciar alertas avançados**.
    
3. Escolha **ir para o Office 365 Cloud app Security**.<br>![No centro de &amp; conformidade de segurança, escolha Gerenciar alertas avançados para acessar o Office 365 Cloud app Security](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)<br>
  
4. Na barra de navegação na parte superior da tela, escolha **alertas**.
    
5. Na coluna **alerta** , clique duas vezes em um alerta que pertença a uma conta de usuário específica. 
    
6. Em **contas**, na coluna **status** , escolha o ícone ![](media/e01b75cc-b28f-4b83-8f86-b1b13dc27ab2.png) \> de configurações de **suspensão do usuário**.
    
## <a name="to-restore-a-user-account"></a>Para restaurar uma conta de usuário

Consulte [restaurar um usuário no Office 365](https://support.office.com/article/2c261e42-5dd1-48b0-845f-2a016d29cfc1)
  
## <a name="next-steps"></a>Próximas etapas

- [Revisar e tomar atitudes sobre alertas no Office 365 Cloud App Security](review-office-365-cas-alerts.md)
    
- [Gerenciar aplicativos do OAuth usando o Office 365 Cloud App Security](manage-app-permissions-in-ocas.md)
    
- ReVisar suas [atividades de utilização do Office 365 Cloud app Security](utilization-activities-for-ocas.md)
    


---
title: Suspender ou restaurar uma conta de usuário no Office 365 Cloud App Security
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
ms.assetid: 5f02d20f-b9aa-4b2f-ad2d-506a4a3c4540
description: 'Com segurança de aplicativo de nuvem do Office 365, as ações de governança que podem ser realizadas são suspender ou cancelar a suspensão de uma conta de usuário. '
ms.openlocfilehash: a5c75edefc6ddb87b5676c4253aafe04817f6a1d
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523648"
---
# <a name="suspend-or-restore-a-user-account-in-office-365-cloud-app-security"></a>Suspender ou restaurar uma conta de usuário no Office 365 Cloud App Security

Gerenciamento de segurança avançada do Office 365 agora é segurança de aplicativo de nuvem do Office 365.
  
|Avaliação * *\>**|Planejamento * *\>**|Implantação * *\>**|Utilização * * *|
|:-----|:-----|:-----|:-----|
|[Comece a avaliar](office-365-cas-overview.md) <br/> |[Começar a planejar](get-ready-for-office-365-cas.md) <br/> |[Começar a implantar](turn-on-office-365-cas.md) <br/> |Você está aqui!  <br/> [Próximas etapas](suspend-or-restore-an-account-in-ocas.md#nextsteps) <br/> |
   
Suponha que você recebe um alerta que uma das contas de usuário da sua organização para o Office 365 foi comprometida. Ou então, suponha que você tiver recebido um alerta indicando que algo está errado com uma conta de usuário. Com a segurança de aplicativo de nuvem do Office 365, você pode suspender uma conta de usuário e restaurá-lo mais tarde após você ter investigados os alertas que você recebe.
  
> [!NOTE]
> Segurança de aplicativo de nuvem do Office 365 está disponível no Office 365 Enterprise E5. Se sua organização estiver usando outra assinatura do Office 365 Enterprise, a segurança de aplicativo de nuvem do Office 365 pode ser adquirida como um complemento. (Como um administrador global, no Centro de administração do Office 365, escolha **faturamento** \> **Adicionar assinaturas**.) Para obter mais informações, consulte [Descrição do serviço de plataforma do Office 365: segurança do Office 365 &amp; Centro de conformidade](https://technet.microsoft.com/en-us/library/dn933793.aspx) e [comprar ou editar um complemento para o Office 365 para empresas](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6). 
  
## <a name="to-suspend-a-user-account-in-office-365-cloud-app-security"></a>Para suspender uma conta de usuário na segurança de aplicativo de nuvem do Office 365

Quando você suspende uma conta de usuário, você impede que o usuário entrar novamente. É o mesmo editando a conta de usuário diretamente no Office 365 para definir o status de entrada para **entrar bloqueados**.
  
> [!NOTE]
> Se você bloquear um usuário entrar no Office 365, suspendendo-los ou editando seus status de entrada, lembre-se de que ele pode levar uma hora ou isso entre em vigor em todos os dispositivos e clientes ([Editar ou alterar um usuário no Office 365](https://support.office.com/article/42BB3F17-8F9D-4182-B434-5F1C8024E614#SingleUserPreview)) do usuário. Se o usuário está conectado ao Office 365, o bloco entrará em vigor sempre que o Office 365 exige que eles entrar novamente. 
  
1. Como um [administrador global ou administrador de segurança](permissions-in-the-security-and-compliance-center.md), vá para [https://protection.office.com](https://protection.office.com) e entrar usando sua conta do trabalho ou da escola. (Isso leva você para a segurança &amp; Centro de conformidade.) 
    
2. Na segurança &amp; Centro de conformidade, escolha **alertas** \> **avançadas de gerenciar alertas**.
    
3. Escolha **vá para segurança de aplicativo do Office 365 nuvem**.
    
    ![Na segurança &amp; Centro de conformidade, escolha gerenciar alertas avançadas para ir à segurança de aplicativo de nuvem do Office 365](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)
  
4. Na barra de navegação na parte superior da tela, escolha **alertas**.
    
5. Na coluna de **alerta** , clique duas vezes em um alerta que pertence a uma conta de usuário específico. 
    
6. Em **contas**, na coluna **Status** , escolha configurações ![ícone configurações](media/e01b75cc-b28f-4b83-8f86-b1b13dc27ab2.png) \> **usuário Suspend**.
    
## <a name="to-restore-a-user-account"></a>Para restaurar uma conta de usuário

Consulte a [restauração de um usuário no Office 365](https://support.office.com/article/2c261e42-5dd1-48b0-845f-2a016d29cfc1)
  
## <a name="next-steps"></a>Próximas etapas

- [Revisar e tomar atitudes sobre alertas no Office 365 Cloud App Security](review-office-365-cas-alerts.md)
    
- [Gerenciar permissões de aplicativo usando o Office 365 Cloud App Security](manage-app-permissions-in-ocas.md)
    
- Revise suas [atividades de utilização para segurança de aplicativo de nuvem do Office 365](utilization-activities-for-ocas.md)
    


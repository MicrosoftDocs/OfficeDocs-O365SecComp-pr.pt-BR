---
title: Políticas de acesso no Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.reviewer: alesibov
ms.audience: Admin
ms.topic: reference
ms.date: 02/27/2019
ms.service: O365-seccomp
localization_priority: Normal
description: As políticas de acesso do Office 365 Cloud app Security permitem o monitoramento em tempo real e o controle sobre o acesso a aplicativos em nuvem com base no usuário, local, dispositivo e aplicativo. Você pode criar políticas de acesso para qualquer dispositivo, incluindo dispositivos que não são associados ao domínio, e não gerenciados pelo Windows Intune, distribuindo certificados de cliente para dispositivos gerenciados ou usando certificados existentes, como certificados MDM de terceiros. Por exemplo, você pode implantar certificados de cliente em dispositivos gerenciados e, em seguida, bloquear o acesso de dispositivos sem um certificado.
ms.openlocfilehash: 5e8b8fa293420bc9ff3616daf288b8e02a2eb768
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262994"
---
# <a name="access-policies-in-office-365-cloud-app-security"></a>Políticas de acesso no Office 365 Cloud App Security

|Avaliação * *\>**|Planejamento * *\>**|Implantação * *\>**|Utilização * * *|
|:-----|:-----|:-----|:-----|
|[Iniciar avaliação](office-365-cas-overview.md) <br/> |[Iniciar planejamento](get-ready-for-office-365-cas.md) <br/> |Você está aqui!  <br/> [Próxima etapa](group-your-ip-addresses-in-ocas.md) <br/> |[Começar a usar](utilization-activities-for-ocas.md) <br/> |

As políticas de acesso do Office 365 Cloud app Security permitem o monitoramento em tempo real e o controle sobre o acesso a aplicativos em nuvem com base no usuário, local, dispositivo e aplicativo. Você pode criar políticas de acesso para qualquer dispositivo, incluindo dispositivos que não são associados ao domínio, e não gerenciados pelo Windows Intune, distribuindo certificados de cliente para dispositivos gerenciados ou usando certificados existentes, como certificados MDM de terceiros. Por exemplo, você pode implantar certificados de cliente em dispositivos gerenciados e, em seguida, bloquear o acesso de dispositivos sem um certificado.

Em vez de permitir ou bloquear totalmente o acesso, com [políticas](ocas-session-policies.md) de sessão, você pode permitir o acesso enquanto monitora a sessão e/ou limita as atividades específicas da sessão.

## <a name="prerequisites-to-using-access-policies"></a>Pré-requisitos para usar políticas de acesso

- Licença do Azure AD Premium P1

- Os aplicativos relevantes devem ser [implantados com o controle de aplicativo de acesso condicional](https://docs.microsoft.com/en-us/cloud-app-security/proxy-deployment-aad)

-  uma [política de acesso condicional do Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal)deve estar no lugar que redireciona os usuários para o Office 365 Cloud App Security, conforme descrito abaixo.

## <a name="create-an-azure-ad-conditional-access-policy"></a>Criar uma política de acesso condicional do Azure AD

As políticas de acesso condicional do Azure Active Directory e diretivas de sessão de segurança do Cloud app funcionam em tandem para examinar cada sessão de usuário e tomar decisões sobre a política para cada aplicativo. Para configurar uma política de acesso condicional no Azure AD, siga este procedimento:

1. Configure uma [política de acesso condicional do Azure ad](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal)com atribuições para o usuário ou grupo de usuários e o aplicativo que você deseja controlar com o controle de aplicativo de acesso condicional.<br>Observação: somente os aplicativos que foram implantados com o  [controle de aplicativo de acesso condicional](https://docs.microsoft.com/cloud-app-security/proxy-deployment-aad)serão afetados por essa política.

2. encaminhe os usuários para o Office 365 Cloud App Security selecionando as  **restrições de usar o controle de aplicativo de acesso condicional**em **sessão**.

## <a name="create-a-cloud-app-security-access-policy"></a>Criar uma política de acesso de segurança do Cloud app

Para criar uma nova política de acesso, siga este procedimento:

1. No portal, selecione **controle** seguido por **políticas**.

2. Na página **políticas** , clique em **criar política** e selecione **política de acesso**.

3. Na janela **política** de acesso, atribua um nome para a política, como *bloquear o acesso de dispositivos não gerenciados*.

4. Nas **atividades correspondentes a todas as seguintes** seções, em **origem da atividade**, selecione filtros de atividade adicionais a serem aplicados à política. Os filtros incluem as seguintes opções:
    
    - **Marcas de dispositivo**: Use este filtro para identificar dispositivos não gerenciados.
    
    - **Local**: Use este filtro para identificar locais desconhecidos (e, portanto, arriscados).
    
    - **Endereço IP**: Use este filtro para filtrar por endereços IP ou usar marcas de endereço IP previamente atribuídas.
    
    - **Marca de agente do usuário**: Use este filtro para habilitar o heurístico para identificar aplicativos móveis e de área de trabalho. Esse filtro pode ser definido como igual ou diferente de. Os valores devem ser testados em relação aos aplicativos móveis e de área de trabalho para cada aplicativo de nuvem.

5. Em **ações**, selecione uma das seguintes opções:
    
    - **Permitir**: defina esta ação para permitir explicitamente o acesso de acordo com os filtros de política definidos.
    
    - **Bloquear**: defina esta ação para bloquear explicitamente o acesso de acordo com os filtros de política definidos.

6. Você pode **criar um alerta para cada evento coincidente com a severidade da política**e definir um limite de alerta e selecionar se deseja que o alerta seja um email, uma mensagem de texto ou ambos.

## <a name="next-steps"></a>Próximas etapas

- [Agrupar seus endereços IP para simplificar o gerenciamento do Office 365 Cloud App Security](group-your-ip-addresses-in-ocas.md)
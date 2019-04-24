---
title: Implantar o Controle de Aplicativos de Acesso Condicional nos aplicativos do Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.reviewer: alesibov
ms.audience: Admin
ms.topic: reference
ms.date: 02/27/2019
ms.service: O365-seccomp
localization_priority: Normal
description: Siga estas etapas para configurar os aplicativos do Azure AD Office 365 para serem controlados pelo controle de aplicativo de acesso condicional do Office 365 Cloud app Security.
ms.openlocfilehash: 72be95b3213b90cfe60d851d0852d465cdbe6ef9
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32263095"
---
# <a name="deploy-conditional-access-app-control-for-office-365-apps"></a>Implantar o Controle de Aplicativos de Acesso Condicional nos aplicativos do Office 365

|Avaliação * *\>**|Planejamento * *\>**|Implantação * *\>**|Utilização * * *|
|:-----|:-----|:-----|:-----|
|[Iniciar avaliação](office-365-cas-overview.md) <br/> |[Iniciar planejamento](get-ready-for-office-365-cas.md) <br/> |Você está aqui!  <br/> [Próxima etapa](ocas-session-policies.md) <br/> |[Começar a usar](utilization-activities-for-ocas.md) <br/> |

Siga estas etapas para configurar os aplicativos do Azure AD Office 365 para serem controlados pelo controle de aplicativo de acesso condicional do Office 365 Cloud app Security.

**Etapa 1: [criar uma política de teste de acesso condicional do Azure ad](#step-1-create-an-azure-ad-conditional-access-test-policy)**

**Etapa 2: [entrar com um usuário com escopo de política nos aplicativos](#step-2-sign-in-with-a-user-scoped-to-the-policy-in-the-apps)**

**Etapa 3: se você não tiver selecionado uma política de segurança do aplicativo de nuvem interna no Azure AD ou se quiser aplicar a política a um aplicativo não-----------------no [portal, configure os controles avançados no portal do Cloud app Security](#step-3-configure-advanced-controls-in-the-cloud-app-security-portal)**

**Etapa 4: [testar a implantação](#step-4-test-the-deployment)**

> [!IMPORTANT]
> para implantar o controle de aplicativo de acesso condicional para aplicativos do Office 365, você precisa de uma [licença válida para o Azure AD Premium P1](https://docs.microsoft.com/azure/active-directory/license-users-groups) , bem como uma licença de segurança do aplicativo na nuvem do Office 365.

## <a name="step-1-create-an-azure-ad-conditional-access-test-policy"></a>Etapa 1: criar uma política de teste de acesso condicional do Azure AD 

1. No Azure Active Directory, em **segurança**, clique em **acesso condicional**.

2. Clique em **nova política** e crie uma nova política.

3. Na política de teste, em **usuários**, atribua um usuário de teste ou usuário que possa ser usado para logon inicial e verificação.

4. Na política de teste, em **Cloud app**, atribua os aplicativos que você deseja controlar com o controle de aplicativo de acesso condicional.

5. Em **sessão**, defina a política para usar uma das políticas internas, **monitorar somente** ou **bloquear downloads**. Ou selecione **usar política** personalizada para definir uma política avançada no portal do Cloud app Security.

6. Adicione qualquer **atribuição** de condição ou **controle** de concessão aplicáveis (opcional).

> ![Acesso condicional do Azure AD](media/image1.png)

## <a name="step-2-sign-in-with-a-user-scoped-to-the-policy-in-the-apps"></a>Etapa 2: entrar com um usuário com escopo de política nos aplicativos 

Após criar a política, entre em cada aplicativo configurado nessa política. Certifique-se de entrar usando um usuário configurado na política. Certifique-se de sair primeiro das sessões existentes.

O Cloud app Security sincronizará seus detalhes de política com seus servidores para cada aplicativo novo no qual você fizer logon. Isso pode levar até um minuto.

## <a name="step-3-configure-advanced-controls-in-the-cloud-app-security-portal"></a>Etapa 3: configurar controles avançados no portal do Cloud app Security 

As instruções acima ajudaram você a criar uma política interna de segurança do aplicativo na nuvem para aplicativos em destaque diretamente no Azure AD.

para configurar uma política avançada, crie uma política de [acesso](ocas-access-policies.md) ou uma [política](ocas-session-policies.md) de sessão no portal do Office 365 Cloud App Security.

### <a name="to-identify-devices-using-client-certificates-this-is-optional"></a>Para identificar dispositivos usando certificados de cliente (isso é opcional):

1. Vá para as configurações COG e escolha **identificação de dispositivo**.

2. Carregar um ou mais certificados raiz ou intermediários.

3. Após o carregamento do certificado, você pode criar políticas de acesso e políticas de sessão com base na **marca de dispositivo** e **certificado de cliente válido**.

![ID do dispositivo de controle de aplicativo de acesso condicional](media/image2.png)

> [!NOTE]
> Um certificado só é solicitado a partir de um usuário se a sessão corresponder a uma política que use o filtro de certificado de cliente válido.
> 
## <a name="step-4-test-the-deployment"></a>Etapa 4: testar a implantação 

1. Primeiro saia de qualquer sessão existente. Em seguida, tente entrar em cada aplicativo que foi implantado com êxito. Entre usando um usuário que coincida com a política configurada no Azure AD.

2. No portal do Cloud app Security, em **Investigate**, selecione **log de atividades**e certifique-se de que as atividades de logon sejam capturadas para cada aplicativo.

3. Você pode filtrar clicando em **avançado**e, em seguida, filtragem usando **controle de acesso de origem igual a**.

4. É recomendável que você entre em aplicativos móveis e de área de trabalho de dispositivos gerenciados e não gerenciados. Isso é para garantir que as atividades sejam capturadas corretamente no log de atividades. Para verificar se a atividade foi capturada corretamente, clique em uma atividade de logon de logon único para que ela abra a gaveta de atividade. Certifique-se de que a **marca** de agente do usuário reflita corretamente se o dispositivo é um cliente nativo (ou seja, um aplicativo móvel ou de área de trabalho) ou se o dispositivo é um dispositivo gerenciado (compatível, domínio associado ou certificado de cliente válido).

> [!NOTE]
> Depois de implantado, você não pode remover um aplicativo da página de controle de aplicativo de acesso condicional. Contanto que você não defina uma sessão ou política de acesso no aplicativo, o controle de aplicativo de acesso condicional não alterará qualquer comportamento para o aplicativo.

## <a name="next-steps"></a>Próximas etapas

- [Saiba mais sobre as políticas de sessão no Office 365 Cloud app Security](ocas-session-policies.md)

- [Saiba mais sobre as políticas de acesso no Office 365 Cloud app Security](ocas-access-policies.md) 

- [Agrupar seus endereços IP para simplificar o gerenciamento do Office 365 Cloud App Security](group-your-ip-addresses-in-ocas.md)
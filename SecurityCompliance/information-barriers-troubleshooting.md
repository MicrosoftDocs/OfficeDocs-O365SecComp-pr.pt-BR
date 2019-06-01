---
title: Solucionando problemas de barreiras de informações
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 05/31/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: Use este artigo como um guia para solucionar problemas de barreiras de informações.
ms.openlocfilehash: b37585469ec8bb299b7976f8a330f4c6b29e3f95
ms.sourcegitcommit: 4fedeb06a6e7796096fc6279cfb091c7b89d484d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/31/2019
ms.locfileid: "34668269"
---
# <a name="troubleshooting-information-barriers-preview"></a>Solucionando problemas de barreiras de informações (versão prévia)

As barreiras de informação podem ajudar sua organização a permanecer em conformidade com requisitos legais e regulamentações do setor. Por exemplo, com barreiras de informações, você pode restringir a comunicação entre grupos específicos de usuários para evitar um conflito de interesses ou outros problemas. Para saber mais, confira [barreiras de informação (versão prévia)](information-barriers.md).

Este artigo fornece orientações que podem ser usadas para obter respostas a perguntas ou resolver problemas que podem surgir com as barreiras de informação.  

## <a name="before-you-begin"></a>Antes de começar...

Para executar as tarefas descritas neste artigo, você deve receber uma função apropriada, como uma das seguintes:
- Administrador global do Microsoft 365 Enterprise
- Administrador global do Office 365
- Administrador de Conformidade
- Gerenciamento de conformidade IB (esta é uma nova função!)

Para saber mais sobre funções e permissões, consulte [permissões no centro de conformidade & segurança do Office 365](permissions-in-the-security-and-compliance-center.md).

Para saber mais sobre os pré-requisitos para barreiras de informações, consulte [pré-requisitos (para políticas de barreira de informações)](information-barriers-policies.md#prerequisites).

Além disso, certifique [-se de se conectar ao PowerShell do centro de conformidade & segurança do Office 365](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).

## <a name="issue-people-are-unexpectedly-blocked-from-communicating-in-microsoft-teams"></a>Problema: as pessoas estão inesperadamente impedidas de se comunicar no Microsoft Teams 

Nesse caso, as pessoas estão relatando problemas inesperados ao se comunicar no Microsoft Teams. Exemplos:
- Um usuário não consegue encontrar ou se comunicar com outro usuário no Microsoft Teams.
- Um usuário não pode ver ou selecionar outro usuário no Microsoft Teams.
- Um usuário pode ver, mas não pode enviar mensagens para outro usuário no Microsoft Teams.

### <a name="what-to-do"></a>O que fazer

1. Determinar se os usuários são afetados por uma política de barreira de informações. Para fazer isso, use o cmdlet **Get-InformationBarrierRecipientStatus** com o parâmetro Identity. 

    A sintaxe é`Get-InformationBarrierRecipientStatus -Identity`

    Você pode usar qualquer valor de identidade que identifique exclusivamente cada destinatário, como nome, alias, nome diferenciado (DN), DN canônica, endereço de email ou GUID.

    Exemplo: `Get-InformationBarrierRecipientStatus -Identity meganb`

    Neste exemplo, estamos usando um alias (*meganb*) para o parâmetro Identity. Este cmdlet retornará informações que indicam se o usuário é afetado por uma política de barreira de informações. (Procure * ExoPolicyId: \<GUID>.)

    Se os usuários não estiverem incluídos nas políticas de barreira de informações, entre em contato com o suporte. Caso contrário, prossiga para a próxima etapa.

2. Descubra quais segmentos estão incluídos em uma política de barreira de informações. Para fazer isso, use o `Get-InformationBarrierPolicy` cmdlet com o parâmetro Identity. Use detalhes, como o GUID da política (ExoPolicyId) que você recebeu durante a etapa anterior, como um valor de identidade.

    Exemplo: `Get-InformationBarrierPolicy -Identity b42c3d0f-49e9-4506-a0a5-bf2853b5df6f`

    Neste exemplo, estamos obtendo informações detalhadas sobre a política de barreira de informações que tem o ExoPolicyId *b42c3d0f-49E9-4506-a0a5-bf2853b5df6f*.
    
    Depois de executar o cmdlet, nos resultados, procure os valores **AssignedSegment**, **SegmentsAllowed**e **SegmentsBlocked** .

    Exemplo: depois de executar `Get-InformationBarrierPolicy` o cmdlet, vimos o seguinte na lista de resultados:

    ```powershell
        AssignedSegment      : Sales
        SegmentsAllowed      : {}
        SegmentsBlocked      : {Research}
    ```
    Nesse caso, podemos ver que uma política de barreira de informações afeta as pessoas que estão nos segmentos de vendas e de pesquisa. Nesse caso, as pessoas em vendas são impedidas de se comunicar com pessoas em pesquisa. Se isso parecer correto, as barreiras de informação estão funcionando conforme o esperado. Caso contrário, vá para a próxima etapa.

4. Certifique-se de que seus segmentos estejam definidos corretamente. Para fazer isso, use o `Get-OrganizationSegment` cmdlet e revise a lista de resultados. 

    Para exibir detalhes de um segmento específico, use o `Get-OrganizationSegment` cmdlet com um parâmetro Identity. 

    Exemplo: `Get-OrganizationSegment -Identity c96e0837-c232-4a8a-841e-ef45787d8fcd`

    Neste exemplo, estamos obtendo informações sobre o segmento que tem GUID *c96e0837-c232-4a8a-841e-ef45787d8fcd*.

    Revise os detalhes do segmento. Se necessário, [edite um segmento](information-barriers-policies.md#edit-a-segment)e, em seguida, use `Start-InformationBarrierPoliciesApplication` o cmdlet novamente.

    Se você ainda estiver tendo problemas com a política de barreira de informações, entre em contato com o suporte.
    
## <a name="issue-the-information-barrier-application-process-is-taking-too-long"></a>Problema: o processo do aplicativo de barreira de informações está demorando muito

Depois de executar o cmdlet **Start-InformationBarrierPoliciesApplication** , o processo está demorando muito tempo para terminar.

### <a name="what-to-do"></a>O que fazer

1. Tenha em mente que quando você executa o cmdlet aplicativo de política, as políticas de barreira de informações são aplicadas (ou removidas), usuário por usuário para todas as contas da sua organização. Se você tiver muitos usuários, levará algum tempo para ser processado. (Como uma diretriz geral, leva cerca de uma hora para processar as contas de usuário 5.000.) 

2. Use o cmdlet **Get-InformationBarrierPoliciesApplicationStatus** para verificar o status.

    Possuem`Get-InformationBarrierPoliciesApplicationStatus`

    Para exibir o status de todos os aplicativos de política de barreira de informações, use`Get-InformationBarrierPoliciesApplicationStatus -All $true`

    Isso exibirá informações sobre se o aplicativo de política foi concluído, falhou ou está em andamento..

3. Dependendo dos resultados da etapa 2, execute uma das seguintes etapas:

    - Se o aplicativo não tiver sido iniciado e tiver sido mais de 45 minutos desde que o cmdlet **Start-InformationBarrierPoliciesApplication** foi executado, revise o log de auditoria para ver se há algum erro nas definições de política ou algum outro motivo pelo qual o o aplicativo não foi iniciado.

    - Se o aplicativo falhou, revise seus segmentos e políticas. Se necessário, [edite segmentos](information-barriers-policies.md#edit-a-segment) e/ou [edite políticas](information-barriers-policies.md#edit-a-policy)e, em seguida, execute o cmdlet **Start-InformationBarrierPoliciesApplication** novamente.

    - Se o aplicativo ainda estiver em andamento, permita que mais tempo seja concluído. Se houver vários dias, entre em contato com o suporte.

## <a name="related-topics"></a>Tópicos relacionados

[Definir políticas para barreiras de informações no Microsoft Teams (visualização)](information-barriers-policies.md)

[Barreiras de informação (visualização)](information-barriers.md)




---
title: Solucionando problemas de barreiras de informações
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 06/21/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: Use este artigo como um guia para solucionar problemas de barreiras de informações.
ms.openlocfilehash: b88f97cd872d4ea3b95bfac049f47cd71dfb2cb2
ms.sourcegitcommit: c603a07d24c4c764bdcf13f9354b3b4b7a76f656
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/21/2019
ms.locfileid: "35131345"
---
# <a name="troubleshooting-information-barriers-preview"></a>Solucionando problemas de barreiras de informações (versão prévia)

[As barreiras de informação (visualização)](information-barriers.md) podem ajudar sua organização a permanecer em conformidade com requisitos legais e regulamentações do setor. Por exemplo, com barreiras de informações, você pode restringir a comunicação entre grupos específicos de usuários para evitar um conflito de interesses ou outros problemas. (Para saber mais sobre como configurar as barreiras de informações, confira [definir políticas para barreiras de informação (versão prévia)](information-barriers-policies.md).

No caso de as pessoas funcionarem em problemas inesperados depois que as barreiras de informações estiverem vigentes, há algumas etapas que você pode executar para resolver esses problemas. Use este artigo como uma guia.


## <a name="before-you-begin"></a>Antes de começar...

Para executar as tarefas descritas neste artigo, você deve receber uma função apropriada, como uma das seguintes:
- Administrador global do Microsoft 365 Enterprise
- Administrador global do Office 365
- Administrador de Conformidade
- Gerenciamento de conformidade IB (esta é uma nova função!)

Para saber mais sobre os pré-requisitos para barreiras de informações, consulte [pré-requisitos (para políticas de barreira de informações)](information-barriers-policies.md#prerequisites).

Certifique-se de [se conectar ao PowerShell do centro de conformidade & segurança do Office 365](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).

## <a name="issue-communications-are-still-allowed-between-users-who-should-be-blocked-in-microsoft-teams"></a>Problema: as comunicações ainda são permitidas entre usuários que devem ser bloqueados no Microsoft Teams

Nesse caso, embora as barreiras de informação sejam definidas, ativas e aplicadas, as pessoas que devem ser impedidas de se comunicar umas com as outras ainda podem no Microsoft Teams.

### <a name="what-to-do"></a>O que fazer

Verifique se os usuários em questão estão incluídos em uma política de barreira de informações. Use o cmdlet **Get-InformationBarrierRecipientStatus** com parâmetros de identidade.

Possuem`Get-InformationBarrierRecipientStatus -Identity <value> -Identity2 <value>` 

Você pode usar qualquer valor que identifique exclusivamente cada usuário, como nome, alias, nome diferenciado, nome de domínio canônico, endereço de email ou GUID. 

Exemplo: `Get-InformationBarrierRecipientStatus -Identity meganb -Identity2 alexw` 

Neste exemplo, nos referimos a duas contas de usuário no Office 365: *meganb* para *Megan*e *alexw* para *Alex*. 

(Você também pode usar esse cmdlet para um único usuário: `Get-InformationBarrierRecipientStatus -Identity <value>`) esse cmdlet retorna informações sobre os usuários, como valores de atributo e quaisquer políticas de barreira de informação aplicadas.


|Resultados  |Próximas etapas  |
|---------|---------|
|Nenhum segmento está listado para os usuários selecionados     |Siga um destes procedimentos:<br/>-Atribuir usuários a um segmento existente editando seus perfis de usuário no Azure Active Directory<br/>-Definir um segmento usando um [atributo com suporte para barreiras de informação](information-barriers-attributes.md)         |
|Os segmentos estão listados, mas nenhuma política de barreira de informações é atribuída a esses segmentos     |Siga um destes procedimentos:<br/>- [Definir uma política de barreira de informações](information-barriers-policies.md#part-2-define-information-barrier-policies) para cada segmento em questão<br/>- [Editar uma política de barreira de informações](information-barriers-policies.md#edit-a-policy) e atribuí-la ao segmento correto         |
|Os segmentos são listados e cada um é incluído em uma política de barreira de informações     |– Execute o `Get-InformationBarrierPolicy` cmdlet para verificar se as políticas de barreira de informações estão ativas<br/>– Execute o `Get-InformationBarrierPoliciesApplicationStatus` cmdlet para confirmar que as políticas foram aplicadas<br/>– Execute o `Start-InformationBarrierPoliciesApplication` cmdlet para aplicar todas as políticas de barreira de informações ativas          |


## <a name="issue-people-are-unexpectedly-blocked-from-communicating-in-microsoft-teams"></a>Problema: as pessoas estão inesperadamente impedidas de se comunicar no Microsoft Teams 

Nesse caso, as pessoas estão relatando problemas inesperados ao se comunicar no Microsoft Teams. Exemplos:
- Um usuário não consegue encontrar ou se comunicar com outro usuário no Microsoft Teams.
- Um usuário não pode ver ou selecionar outro usuário no Microsoft Teams.
- Um usuário pode ver outro usuário, mas não pode selecionar ou enviar mensagens para esse outro usuário no Microsoft Teams.

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

Tenha em mente que quando você executa o cmdlet aplicativo de política, as políticas de barreira de informações são aplicadas (ou removidas), usuário por usuário para todas as contas da sua organização. Se você tiver muitos usuários, levará algum tempo para ser processado. (Como uma diretriz geral, leva cerca de uma hora para processar as contas de usuário 5.000.)

1. Use o cmdlet **Get-InformationBarrierPoliciesApplicationStatus** para verificar o status do aplicativo de política mais recente.

    Possuem`Get-InformationBarrierPoliciesApplicationStatus`

    (Para exibir o status de *todos os* aplicativos de política de barreira de informações, use este cmdlet:<br/>
    `Get-InformationBarrierPoliciesApplicationStatus -All $true`)

    Isso exibirá informações sobre se o aplicativo de política foi concluído, falhou ou está em andamento..

2. Dependendo dos resultados da etapa anterior, execute uma das seguintes etapas:
  
    |Status  |Próxima etapa  |
    |---------|---------|
    |**Não iniciado**     |Se tiver sido mais de 45 minutos desde que o cmdlet **Start-InformationBarrierPoliciesApplication** foi executado, revise o log de auditoria para ver se há algum erro nas definições de política ou outro motivo pelo qual o aplicativo não foi iniciado. |
    |**Falhou**     |Se o aplicativo falhou, revise o log de auditoria. Além disso, revise seus segmentos e políticas. Há usuários atribuídos a mais de um segmento? Há segmentos atribuídos a mais de um poliicy? Se necessário, [edite segmentos](information-barriers-policies.md#edit-a-segment) e/ou [edite políticas](information-barriers-policies.md#edit-a-policy)e, em seguida, execute o cmdlet **Start-InformationBarrierPoliciesApplication** novamente.  |
    |**Em andamento**     |Se o aplicativo ainda estiver em andamento, permita que mais tempo seja concluído. Se houver vários dias, reúna seus logs de auditoria e entre em contato com o suporte. |

## <a name="related-topics"></a>Tópicos relacionados

[Definir políticas para barreiras de informações no Microsoft Teams (visualização)](information-barriers-policies.md)

[Barreiras de informação (visualização)](information-barriers.md)




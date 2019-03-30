---
title: 'Início rápido: configurar a proteção avançada contra ameaças do Office 365'
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/19/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection:
- M365-security-compliance
description: Aqui está um guia de início rápido que você pode usar para garantir que o Office 365 Advanced Threat Protection (ATP) esteja configurado e configurado para sua organização.
ms.openlocfilehash: a071c626327aa7d0055df522e8fec5ebe41d6a83
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/29/2019
ms.locfileid: "30999394"
---
# <a name="quick-start-guide-set-up-office-365-advanced-threat-protection"></a>Guia de início rápido: configurar a proteção avançada contra ameaças do Office 365

Aqui está um guia de início rápido que você pode usar como uma lista de verificação para garantir que a proteção avançada contra ameaças do Office 365 (ATP) esteja configurada para sua organização. Se você for novo na proteção contra ameaças no Office 365, ou se não tiver certeza de onde começar, use a seguinte orientação como ponto de partida. 

> [!IMPORTANT]
> **As configurações iniciais recomendadas são incluídas para cada tipo de política; no entanto, muitas opções estão disponíveis e você pode ajustar suas configurações para atender às necessidades específicas da sua organização**. Aguarde aproximadamente 30 minutos para que as políticas ou as alterações funcionem da mesma forma por meio do datacenter.

## <a name="prerequisites"></a>Pré-requisitos

- Sua organização deve ter uma assinatura que inclua a [proteção avançada contra ameaças do Office 365](office-365-atp.md) (ATP).

- Você deve receber uma função apropriada para acessar os recursos de ATP. A tabela a seguir inclui alguns exemplos: 

    |Função ou grupo de função  |Onde saber mais  |
    |---------|---------|
    |Administrador global do Office 365 |[Tudo sobre as funções de administrador do Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles)|
    |Administrador de segurança |[Permissões de função de administrador no Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/directory-assign-admin-roles)|
    |Gerenciamento da organização do Exchange Online |[Permissões no Exchange Online](https://docs.microsoft.com/en-us/exchange/permissions-exo/permissions-exo) <br>and<br> [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)|

    (Consulte [permissões no centro de conformidade de &amp; segurança do Office 365](permissions-in-the-security-and-compliance-center.md).)

## <a name="part-1---anti-malware"></a>Parte 1-anti-malware

1. No [centro de conformidade do & de segurança](https://protection.office.com), escolha**anti-malware**de**política** > de **Gerenciamento** > de ameaças.
2. Clique duas vezes na política **padrão** e, em seguida, escolha **configurações**.
3. Especifique as seguintes configurações:
    - Na seção **resposta de detecção de malware** , mantenha a configuração padrão **no**.
    - Na seção **filtro de tipos de anexo comuns** , escolha **ativado**.
4. Clique em **Salvar**.

Para saber mais sobre opções de política Antimalware, consulte [Configure anti-malware Policies](configure-anti-malware-policies.md).

## <a name="part-2---zero-day-protection"></a>Parte 2-proteção de dia zero

A proteção de dia zero é configurada por meio de políticas, como links seguros de ATP e políticas de anexos seguros.

### <a name="atp-safe-attachments-policies"></a>Políticas de anexos seguros de ATP

1. No [centro de conformidade do & de segurança](https://protection.office.com), escolha a**política** > de **Gerenciamento** > de ameaça**anexos seguros de ATP**.
2. Selecione a opção **ativar a ATP para SharePoint, onedrive e Microsoft Teams**.
3. Na seção **proteger anexos de email** , clique no sinal de mais**+**().
4. Especifique as seguintes configurações:
    - Na caixa **nome** , digite `Block malware`.
    - Na seção resposta, escolha **Bloquear**.
    - Na seção **redirecionar anexo** , selecione a opção **habilitar**redirecionamento e, em seguida, especifique o endereço de email para o administrador ou operador de segurança da sua organização que examinará os arquivos detectados.
    - Na seção **aplica-se** a, escolha **o domínio do destinatário**. Em seguida, selecione o seu domínio, escolha **Adicionar**e clique em **OK**.
5. Clique em **Salvar**.
6. (Etapa adicional recomendada) Como um administrador global ou um administrador do SharePoint Online, execute o cmdlet **[set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** com o parâmetro **DisallowInfectedFileDownload** definido como *true* para o seu ambiente do Office 365. (Isso impede que as pessoas abram, movam, copiem ou compartilhem arquivos detectados como mal-intencionados.)  

Para saber mais, confira [configurar as políticas de anexos seguros do Microsoft office 365 ATP](set-up-atp-safe-attachments-policies.md) e [ativar o Office 365 ATP para SharePoint, onedrive e Microsoft Teams](turn-on-atp-for-spo-odb-and-teams.md).

### <a name="atp-safe-links-policies"></a>Políticas de links seguros de ATP

Para configurar links de ATP seguros, revise a política padrão e adicione uma política.

1. No [centro de conformidade do & de segurança](https://protection.office.com), escolha links de segurança**ATP**da**política** > de **Gerenciamento** > de ameaças.
2. Clique duas vezes na política **padrão** .
3. Na seção **usar links seguros em** , selecione a opção **Office 365 ProPlus, Office para IOS e Android**e clique em **salvar**.
4. Na seção **políticas que se aplicam a destinatários específicos** , clique no sinal de**+** mais ().
5. Especifique as seguintes configurações:
    - Na caixa **nome** , digite um nome, como `Safe Links`.
    - Na seção **Selecionar ação** , escolha **ativado**.
    - Selecione estas opções:
        - **Usar anexos seguros para examinar Conteúdo baixável** 
        - **Aplicar links seguros a mensagens de email enviadas dentro da organização**
        - **Não permitir que os usuários cliquem por meio de links seguros para a URL original**
    - Na seção **aplica-se** a, escolha **o domínio do destinatário**. Em seguida, selecione o seu domínio, escolha **Adicionar**e clique em **OK**.
6. Clique em **Salvar**.

Para saber mais, confira [configurar as políticas de links seguros de ATP do Office 365](set-up-atp-safe-links-policies.md). 

## <a name="part-3---anti-phishing"></a>Parte 3-anti-phishing 

1. No [centro de conformidade do & de segurança](https://protection.office.com), escolha**anti-phishing**da**política** > de **Gerenciamento** > de ameaças.
2. Clique em **política padrão**.
3. Na seção **representação** , clique em **Editar**e especifique as seguintes configurações:
    -  Na guia **Adicionar usuários para proteger** , ative a proteção. Em seguida, adicione usuários, como os membros da diretoria da sua organização, seu CEO, CFO e outros líderes seniores. (Você pode digitar um endereço de email individual ou clicar para exibir uma lista.)
    - Na guia **adicionar domínios para proteger** , ative **automaticamente os domínios que eu sou proprietário**. Se você tiver domínios personalizados, adicione-os também.
    - Na guia **ações** , selecione **mover mensagem para as pastas de lixo eletrônico dos destinatários para o** usuário representado e o domínio representado e ative as dicas de segurança.
    - Na guia **inteligência de caixa de correio** , verifique se a inteligência de caixa de correio está ativada.
    - Na guia **revise Your Settings** , depois de revisar as configurações, clique em **salvar**.
4. Na seção **spoof** , clique em **Editar**e especifique as seguintes configurações:
    - Na guia **configurações de filtro** de falsificação, verifique se a proteção contra falsificação está ativada.
    - Na guia **ações** , escolha mover mensagem para as pastas de lixo eletrônico dos destinatários.
    - Na guia **revise Your Settings** , depois de revisar as configurações, clique em **salvar**. Se não fizer alterações, clique em **Cancelar**.
5. Feche a página de configurações de política padrão.

Para saber mais sobre suas opções de política anti-phishing, confira [Configurar políticas de anti-phishing e anti-phishing do Office 365 ATP](set-up-anti-phishing-policies.md).

## <a name="part-4---anti-spam"></a>Parte 4-antispam

1. No [centro de conformidade do & de segurança](https://protection.office.com), escolha**anti-spam**de**política** > de **Gerenciamento** > de ameaças.
2. Na guia **Personalizar** , ative **as configurações personalizadas** .
3. Expanda **política de filtro de spam padrão**, clique em **Editar política**e especifique as seguintes configurações:
    - Na seção **ações de spam e em massa** , defina o limite para um valor de 5 ou 6.
    - Na seção **permitir listas** , revise (e, se necessário, edite) seus remetentes e domínios permitidos.
4. Clique em **Salvar**.

Para saber mais sobre suas opções de política antispam, consulte [Configure the anti-spam Policies](configure-the-anti-spam-policies.md).

## <a name="part-5---service-wide-settings"></a>Parte 5 – configurações de nível de serviço

### <a name="zero-hour-auto-purge"></a>Limpeza automática de zero horas

A limpeza automática de zero horas (ZAP) é ativada por padrão; no entanto, as seguintes condições devem ser atendidas:
- As ações de spam são definidas para **mover mensagens para a pasta lixo eletrônico** em políticas antispam.
- Os usuários mantiveram suas configurações de lixo eletrônico padrão e não desativaram a proteção de lixo eletrônico.

Para saber mais, confira [exclusão automática de zero horas-proteção contra spam e malware](zero-hour-auto-purge.md).

### <a name="audit-logging"></a>Registro em log de auditoria

Para exibir dados em relatórios de proteção contra ameaças, como o [painel de segurança](security-dashboard.md) e o [Explorer](use-explorer-in-security-and-compliance.md), o log de auditoria deve estar ativado para sua organização.

Consulte [Ativar ou desativar a pesquisa de log de auditoria do Office 365](turn-audit-log-search-on-or-off.md).

## <a name="post-setup-tasks"></a>Tarefas pós-instalação

### <a name="watch-for-new-features-and-service-updates"></a>Assista a novos recursos e atualizações de serviço

- [Visite o mapa do Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap?filters=&searchterms=advanced%2Cthreat%2Cprotection)

- [Consulte a descrição do serviço de proteção avançada contra ameaças do Office 365](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp)

### <a name="see-how-atp-is-working-for-your-organization"></a>Veja como a ATP está funcionando para sua organização

- [Exibir relatórios para a proteção avançada contra ameaças do Office 365](view-reports-for-atp.md)

- [Usar o Explorer no centro &amp; de conformidade de segurança](use-explorer-in-security-and-compliance.md)

### <a name="periodically-review-and-revise-your-atp-policies"></a>Revisar e revisar periodicamente suas políticas ATP

- [Mantenha os usuários do Office 365 seguros com o Office 365 investigação de ameaças e resposta](keep-users-safe-with-office-365-ti.md) 

- [Use os relatórios inteligentes e as ideias no centro de conformidade de segurança &amp; do Office 365](reports-and-insights-in-security-and-compliance.md) 
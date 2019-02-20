---
title: Diretivas de sessão no Office 365 Cloud app Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.reviewer: alesibov
ms.audience: Admin
ms.topic: reference
ms.date: 02/14/2019
ms.service: o365-administration
localization_priority: Normal
description: As políticas de sessão do Office 365 Cloud app Security permitem o monitoramento em tempo real em nível de sessão, o que proporciona visibilidade detalhada dos aplicativos do Office 365 e a capacidade de realizar ações diferentes dependendo da política definida para uma sessão de usuário. Em vez de permitir ou bloquear totalmente o acesso, com o controle de sessão, você pode permitir o acesso enquanto monitora a sessão e/ou limita as atividades específicas da sessão usando as funcionalidades de proxy reverso do controle de aplicativo de acesso condicional.
ms.openlocfilehash: 0dbfb3e5827fb76e52f0262333d372860f0cb58a
ms.sourcegitcommit: 8679937354c1d8870ecd41519a59d2d7468c23c4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2019
ms.locfileid: "30103336"
---
# <a name="session-policies-in-office-365-cloud-app-security"></a>Diretivas de sessão no Office 365 Cloud app Security

|Avaliação * *\>**|Planejamento * *\>**|Implantação * *\>**|Utilização * * *|
|:-----|:-----|:-----|:-----|
|[Iniciar avaliação](office-365-cas-overview.md) <br/> |[Iniciar planejamento](get-ready-for-office-365-cas.md) <br/> |Você está aqui!  <br/> [Próxima etapa](ocas-access-policies.md) <br/> |[Começar a usar](utilization-activities-for-ocas.md) <br/> |

As políticas de sessão do Office 365 Cloud app Security permitem o monitoramento em tempo real em nível de sessão, o que proporciona visibilidade detalhada dos aplicativos do Office 365 e a capacidade de realizar ações diferentes dependendo da política definida para uma sessão de usuário. Em vez de permitir ou bloquear totalmente o acesso, com o controle de sessão, você pode permitir o acesso enquanto monitora a sessão e/ou limita as atividades específicas da sessão usando as funcionalidades de proxy reverso do controle de aplicativo de acesso condicional.

Por exemplo, você pode decidir que de dispositivos não gerenciados ou de sessões vindas de locais específicos, você deseja permitir que o usuário acesse o aplicativo, mas também limitar o download de arquivos confidenciais ou exigir que determinados documentos estejam protegidos no download. As políticas de sessão permitem definir esses controles de sessão de usuário e permitir o acesso e permite que você:

- [Monitorar todas as atividades](#monitor-all-activities)

- [Bloquear todos os downloads](#block-all-downloads)

- [Bloquear atividades específicas](#block-specific-activities)

- [Proteger arquivos ao baixar](#protect-files-on-download)

## <a name="prerequisites-to-using-session-policies"></a>Pré-requisitos para usar políticas de sessão

- Licença do Azure AD Premium P1

- Os aplicativos relevantes do Office 365 devem ser implantados [com o controle de aplicativo de acesso condicional](ocas-deploy-conditional-access-app-control.md)

-  uma [política de acesso condicional do Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal)deve estar no lugar que redireciona os usuários para o Office 365 Cloud App Security

## <a name="create-an-azure-ad-conditional-access-policy"></a>Criar uma política de acesso condicional do Azure AD

As políticas de acesso condicional do Azure Active Directory e diretivas de sessão de segurança do Cloud app funcionam em tandem para examinar cada sessão de usuário e tomar decisões sobre a política para cada aplicativo. Para configurar uma política de acesso condicional no Azure AD, siga este procedimento:

1. Configure uma [política de acesso condicional do Azure ad](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal)com atribuições para um usuário ou grupo de usuários e o aplicativo que você deseja controlar com o controle de aplicativo de acesso condicional. Observação: somente os aplicativos que foram implantados com o  [controle de aplicativo de acesso condicional](ocas-deploy-conditional-access-app-control.md)serão afetados por essa política.

2. encaminhe os usuários para o Office 365 Cloud App Security, selecionando a **** página **usar o controle** de aplicativo de acesso condicional.

## <a name="create-a-cloud-app-security-session-policy"></a>Criar uma política de sessão de segurança do Cloud app

Para criar uma nova política de sessão, siga este procedimento:

1. No portal, selecione **controle** seguido por **políticas**.

2. Na página **políticas** , clique em **criar política** e selecione **política de sessão**.

3. Na janela **política** de sessão, atribua um nome para a política

4. No campo **tipo** de controle da sessão:
    
    - Selecione **monitorar somente** se você quiser monitorar apenas as atividades pelos usuários. Essa seleção criará uma política de monitor somente para os aplicativos que você selecionou onde todos os logins, downloads heurísticos e tipos de atividade serão baixados.
    
    - Selecione **controle download de arquivo (com DLP)** se você quiser monitorar as atividades do usuário. Você pode executar ações adicionais, como bloquear ou proteger downloads para usuários.
    
    - Selecione **bloquear atividades** para bloquear atividades específicas, que você pode selecionar usando o filtro de **tipo** de atividade. Todas as atividades de aplicativos selecionados serão monitoradas (e relatadas no log de atividades). As atividades específicas selecionadas serão bloqueadas se você selecionar a ação **Bloquear** . As atividades específicas selecionadas irão gerar alertas se você selecionar a ação de **teste** e tiver alertas ativados.

5. Em **origem** da atividade nas **atividades que correspondem a todas as seguintes** seções, selecione filtros de atividade adicionais a serem aplicados à política. Esses filtros podem incluir as seguintes opções:
    
    - **Marcas de dispositivo**: Use este filtro para identificar dispositivos não gerenciados.
    
    - **Local**: Use este filtro para identificar locais desconhecidos (e, portanto, arriscados).
    
    - **Endereço IP**: Use este filtro para filtrar por endereços IP ou usar marcas de endereço IP previamente atribuídas.
    
    - **Marca de agente do usuário**: Use este filtro para habilitar o heurístico para identificar aplicativos móveis e de área de trabalho. Esse filtro pode ser definido como igual ou não igual ao **cliente nativo**. Este filtro deve ser testado em relação aos aplicativos móveis e de área de trabalho para cada aplicativo de nuvem.<br>Observação: as políticas de sessão não dão suporte a aplicativos móveis e de área de trabalho. Aplicativos móveis e aplicativos de área de trabalho também podem ser bloqueados ou permitidos pela criação de uma política de acesso.

6. Se você selecionou a opção para **controlar o download de arquivo (com DLP)**, em **origem** da atividade nos **arquivos correspondentes a todas as seções a seguir** , selecione filtros de arquivo adicionais a serem aplicados à política. Esses filtros podem incluir as seguintes opções:
        
    - **Rótulo de classificação** : Use este filtro se sua organização usa a proteção de informações do Azure e seus dados foram protegidos por seus rótulos de classificação. Você pode filtrar arquivos com base no rótulo de classificação que você aplicou a eles. Para obter mais informações sobre a integração com a proteção de informações do Azure, consulte [Azure Information Protection Integration](https://docs.microsoft.com/cloud-app-security/azip-integration).
        
    - **Nome do arquivo** : Use este filtro para aplicar a política a arquivos específicos.
        
    - **Tipo de arquivo** : Use este filtro para aplicar a política a tipos de arquivo específicos, por exemplo, bloquear download para todos os arquivos. xls.
    
    - Na seção **inspeção** de conteúdo, defina se você deseja habilitar o mecanismo DLP para verificar documentos e conteúdo de arquivo.
    
    - Em **ações**, selecione um dos seguintes itens:
        
        - **Testar (monitorar todas as atividades)**: defina esta ação para permitir o download explicitamente de acordo com os filtros de política definidos.
        
        - **Bloquear (bloquear arquivo baixar e monitorar todas as atividades)**: defina esta ação para bloquear o download explicitamente de acordo com os filtros de política definidos. Para obter mais informações, consulte [How Block download Works](https://docs.microsoft.com/en-us/cloud-app-security/session-policy-aad#block-download).
        
        - **Proteger (Aplicar rótulo de classificação para baixar e monitorar todas as atividades)**: essa opção só estará disponível se você tiver selecionado **controle de download de arquivo (com DLP)** em **política de sessão**. Se sua organização usa a proteção de informações do Azure, você pode definir uma **ação** para aplicar um conjunto de rótulos de classificação na proteção de informações do Azure para o arquivo. Para obter mais informações, consulte [como proteger o download funciona](https://docs.microsoft.com/en-us/cloud-app-security/session-policy-aad#protect-download).

7. Você pode **criar um alerta para cada evento coincidente com a severidade da política**e definir um limite de alerta. Selecione se você deseja que o alerta seja um email, uma mensagem de texto ou ambos.

## <a name="monitor-all-activities"></a>Monitorar todas as atividades

Quando você cria uma política de sessão, cada sessão de usuário que corresponde à política é redirecionada para o controle de sessão em vez de diretamente para o aplicativo. O usuário verá um aviso de monitoramento para que eles saibam que suas sessões estão sendo monitoradas.

Se não quiser notificar o usuário de que ele está sendo monitorado, você poderá desabilitar a mensagem de notificação.

1. Na COG configurações, selecione **configurações gerais**.

2. Em seguida, em **controle** de aplicativo de acesso condicional, selecione monitoramento de **usuário**e desmarque a caixa de seleção **notificar usuários** .

Para manter o usuário dentro da sessão, o controle de aplicativo de acesso condicional substitui todas as URLs, scripts Java e cookies relevantes dentro da sessão de aplicativo com as URLs do Office 365 Cloud app Security. Por exemplo, se o aplicativo retornar uma página com links cujos domínios terminam `myapp.com`com, o controle de aplicativo Conditional Access substituirá os links com domínios `myapp.com.us.cas.ms`terminados por algo semelhante. Dessa forma, toda a sessão é monitorada pelo Office 365 Cloud app Security.

O controle de aplicativos de acesso condicional registra os logs de tráfego de cada sessão de usuário que é roteada através dele. Os logs de tráfego incluem hora, IP, agente do usuário, URLs visitadas e o número de bytes carregados e baixados. Esses logs são analisados e um relatório contínuo, **controle de aplicativo de acesso condicional do Cloud app Security**, é adicionado à lista de relatórios de descoberta de nuvem no painel de descoberta de nuvem.

### <a name="to-export-these-logs"></a>Para exportar esses logs:

1. Vá para a COG configurações e clique em **controle de aplicativo de acesso condicional**.

2. No lado direito da tabela, clique no botão Exportar.<br>![botão Exportar](media/image3.png)<br>

3. Selecione o intervalo do relatório e clique em **Exportar**. Esse processo pode levar algum tempo.

### <a name="to-download-the-exported-log"></a>Para baixar o log exportado:

1. Depois que o relatório estiver pronto, vá para **configurações** e, em seguida, **relatórios**exportados.

2. Na tabela, selecione o relatório relevante na lista de logs de **tráfego de controle de aplicativo de acesso condicional**e clique em baixar.<br>![botão baixar](media/image4.png)<br>

## <a name="block-all-downloads"></a>Bloquear todos os downloads

Quando o **bloco** é definido como a **ação** que você deseja realizar na política de sessão de segurança do aplicativo em nuvem, o controle de aplicativo de acesso condicional impede que o usuário Baixe um arquivo de acordo com os filtros de arquivo da política. Um evento de download é reconhecido pelo Office 365 Cloud app Security para cada aplicativo quando um usuário inicia um download. O controle de aplicativo condicional do Access interveniente em tempo real para impedir que ele seja executado. Quando o sinal é recebido de que um usuário iniciou um download, o controle de aplicativo Conditional Access retorna uma mensagem de **Download restrito** ao usuário e substitui o arquivo baixado por um arquivo de texto. A mensagem do arquivo de texto para o usuário pode ser configurada e personalizada na política de sessão.

## <a name="block-specific-activities"></a>Bloquear atividades específicas

Quando **atividades** de bloqueio são definidas como o **tipo de atividade**, você pode selecionar atividades específicas para bloquear em aplicativos específicos. Todas as atividades de aplicativos selecionados serão monitoradas e relatadas no log de atividades. As atividades específicas selecionadas serão bloqueadas se você selecionar a ação **Bloquear** . As atividades específicas selecionadas irão gerar alertas se você selecionar a ação de **teste** e tiver alertas ativados.

**Bloquear atividades** específicas e aplicá-las a grupos específicos para criar um modo somente leitura abrangente para sua organização.

## <a name="protect-files-on-download"></a>Proteger arquivos ao baixar

Selecione **bloquear atividades** para bloquear atividades específicas, que você pode encontrar usando o filtro de **tipo** de atividade. Todas as atividades de aplicativos selecionados serão monitoradas (e relatadas no log de atividades). As atividades específicas selecionadas serão bloqueadas se você selecionar a ação **Bloquear** . As atividades específicas selecionadas irão gerar alertas se você selecionar a ação de **teste** e tiver alertas ativados.

Quando a **proteção** é definida como a **ação** a ser realizada na política de sessão de segurança do aplicativo de nuvem, o controle de aplicativo de acesso condicional impõe o rotulamento e a proteção subsequente de um arquivo por filtros de arquivo da política. Os rótulos são configurados no console de proteção de informações do Azure e a **proteção** deve ser selecionada dentro do rótulo para que ele apareça como uma opção na política de segurança do aplicativo em nuvem. Quando um rótulo é selecionado, e um arquivo é baixado que atende aos critérios da política de segurança do aplicativo na nuvem, o rótulo e a proteção correspondente (com permissões) é aplicada ao arquivo no download. O arquivo original permanece como está no aplicativo na nuvem enquanto o arquivo baixado agora está protegido. Os usuários que tentam acessar o arquivo devem atender aos requisitos de permissão determinados pela proteção aplicada.

## <a name="next-steps"></a>Próximas etapas

- [Saiba mais sobre as políticas de acesso no Office 365 Cloud app Security](ocas-access-policies.md)

- [Bloqueando downloads em dispositivos não gerenciados usando recursos de controle de aplicativos de acesso condicional do Azure AD](https://docs.microsoft.com/en-us/cloud-app-security/use-case-proxy-block-session-aad)


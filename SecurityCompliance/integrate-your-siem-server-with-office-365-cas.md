---
title: Integrar seu servidor SIEM ao Office 365 Cloud App Security
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
ms.assetid: dd6d2417-49c4-4de6-9294-67fdabbf8532
description: Você pode integrar seu servidor SIEM com o Office 365 Cloud app Security. Leia este artigo para obter uma visão geral de como ele funciona e como configurá-lo.
ms.openlocfilehash: b4baeda3cb836c0b1aa528d29176bbf4321d1fe2
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215869"
---
# <a name="integrate-your-siem-server-with-office-365-cloud-app-security"></a>Integrar seu servidor SIEM ao Office 365 Cloud App Security
  
|Avaliação * *\>**|Planejamento * *\>**|Implantação * *\>**|Utilização * * *|
|:-----|:-----|:-----|:-----|
|[Iniciar avaliação](office-365-cas-overview.md) <br/> |[Iniciar planejamento](get-ready-for-office-365-cas.md) <br/> |Você está aqui!  <br/> [Próxima etapa](utilization-activities-for-ocas.md) <br/> |[Começar a usar](utilization-activities-for-ocas.md) <br/> |
   
## <a name="overview-and-prerequisites"></a>Visão geral e pré-requisitos

Você pode integrar o [Office 365 Cloud app Security](get-ready-for-office-365-cas.md) ao seu servidor de gerenciamento de eventos e informações de segurança (Siem) para habilitar o monitoramento centralizado de alertas. Isso é especialmente vantajoso para organizações que usam serviços de nuvem e aplicativos de servidor local. A integração com um servidor SIEM permite que sua equipe de segurança melhor proteja seus aplicativos do Office 365 enquanto mantém seu fluxo de trabalho de segurança usual, automatizando determinados procedimentos de segurança e correlacionando entre eventos baseados em nuvem e locais.  
  
Quando você integra pela primeira vez o seu servidor SIEM com o Office 365 Cloud app Security, os alertas dos últimos dois dias são encaminhados para o servidor SIEM, bem como todos os alertas de depois (com base nos filtros selecionados). Além disso, se você desabilitar esse recurso por um período estendido, ao habilitá-lo novamente, ele encaminhará os últimos dois dias de alertas e todos os alertas de então em diante.

### <a name="siem-integration-architecture"></a>Arquitetura de integração do SIEM

Um agente SIEM é configurado na rede da sua organização. Quando implantado e configurado, o agente SIEM Obtém os tipos de dados que foram configurados (alertas) usando as APIs do Office 365 Cloud app Security RESTful. O tráfego é enviado por um canal HTTPS criptografado na porta 443.
  
Quando um agente SIEM recupera dados do Office 365 Cloud app Security, ele envia as mensagens de syslog para seu servidor SIEM local usando as configurações de rede fornecidas durante a instalação (TCP ou UDP com uma porta personalizada).

![Arquitetura do SIEM e do Cloud app Security](media/siem-architecture.png)

### <a name="supported-siem-servers"></a>Servidores SIEM com suporte

O Office 365 Cloud app Security atualmente oferece suporte aos seguintes servidores SIEM:
- Micro Focus ArcSight
- CEF genérico

### <a name="prerequisites"></a>Pré-requisitos

- Você deve ser um administrador global ou administrador de segurança para executar as tarefas descritas neste artigo. Consulte [permissões no centro de conformidade de &amp; segurança do Office 365](permissions-in-the-security-and-compliance-center.md)

- Você deve ter o [Office 365 Cloud app Security habilitado](turn-on-office-365-cas.md) para sua organização.

- O [log de auditoria](turn-audit-log-search-on-or-off.md) deve estar ativado para o Office 365

- Você deve ter um servidor padrão que atenda aos seguintes requisitos para configurar a integração do SIEM Server:
    - OS: Windows ou Linux (pode ser uma máquina virtual)
    - CPU: 2
    - Espaço em disco: 20 GB
    - RAM: 2 GB
    - [Oracle Java 8](http://www.oracle.com/technetwork/java/javase/downloads/index.html) instalado
    - Firewall configurado conforme descrito nos [requisitos de rede](https://docs.microsoft.com/cloud-app-security/network-requirements)

- Você deve ter detalhes sobre o **host de syslog remoto** e o **número da porta Syslot**. Um administrador de rede ou administrador de segurança deve ser capaz de ajudá-lo a localizar essas informações. 

- Você deve concordar com os [termos de licença de software](https://go.microsoft.com/fwlink/?linkid=862491) para baixar o [arquivo JAR](https://go.microsoft.com/fwlink/?linkid=838596) , você precisará integrar seu servidor Siem.
 
## <a name="step-1-set-it-up-a-siem-agent-in-office-365-cloud-app-security"></a>Etapa 1: configurar um agente SIEM no Office 365 Cloud app Security

1. Vá para o portal do Cloud app Security[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)() e entre.
  
2. Clique em **configurações** \> de **extensões de segurança**e, em seguida, escolha agentes Siem.<br/>
![Escolher configurações extensões de segurança >](media/Settings-SecurityExtensions.png)

3. Escolha **Adicionar agente Siem**.<br/>![Escolha Adicionar agente SIEM.](media/SIEMAgents.png)
    
4. Escolha **Iniciar assistente**.<br/>![Obter ajuda ou iniciar o assistente](media/HelpOrWizard.png) 
    
5. Na etapa **geral** , especifique um nome e **Selecione seu formato Siem** e defina **as configurações avançadas** que sejam relevantes para esse formato. Em seguida, escolha **Avançar**.<br/>![Especifique um nome e tipo](media/ChooseAgentTypeAndName.png)
    
6. Na etapa **syslog remoto** , especifique o endereço IP ou o nome de host do **host syslog remoto** e o **número da porta de syslog**. Selecione TCP ou UDP como o protocolo de syslog remoto. (Você pode trabalhar com seu administrador de rede ou administrador de segurança para obter esses detalhes, caso não os tenha.) Em seguida, escolha **Avançar**.<br/>![Especificar detalhes do syslog remoto](media/ArcSightS1Syslog.png)
  
7. Na etapa **tipos de dados** , execute um dos seguintes procedimentos e clique em **Avançar**:
    - Manter a configuração padrão de **todos os alertas**<br/>OU
    - Clique em **todos os alertas**e, em seguida, escolha **filtros específicos**. Defina filtros para selecionar os tipos de alertas que você deseja enviar ao seu servidor SIEM.<br/>![Etapa tipos de dados do assistente](media/ArcSightS1ExportOptions.png)
  
8. Na tela Parabéns, copie o token e salve-o para mais tarde.<br/>![Tela criada pelo agente SIEM](media/SIEMAgentFinished.png) 

> [!IMPORTANT]
> Neste ponto, você configurou um agente SIEM no Office 365 Cloud app Security, mas sua integração com o servidor do SIEM ainda não foi concluída. Vá para a próxima etapa para continuar sua integração com o servidor SIEM.

Depois de clicar em fechar e sair do assistente, na tela extensões de segurança, você poderá ver o agente SIEM adicionado na tabela. Ele mostrará um status de **criado** até que seja conectado mais tarde.

![Agente SIEM criado](media/SIEMAgentCreated.png)
    
## <a name="step-2-download-a-jar-file-and-run-it-on-your-siem-server"></a>Etapa 2: baixar um arquivo JAR e executá-lo em seu servidor SIEM

1. Baixe o [agente Siem do Microsoft Cloud app Security](https://go.microsoft.com/fwlink/?linkid=838596) e descompacte a pasta. (Você deve concordar com os [termos de licença de software](https://go.microsoft.com/fwlink/?linkid=862491) para continuar.) 
    
2. Extraia o arquivo. jar da pasta zipada e execute-o em seu servidor SIEM.
    
3. Depois de executar o arquivo, execute o seguinte comando:<br/>
  ```
  java -jar mcas-siemagent-0.87.20-signed.jar [--logsDirectory DIRNAME] [--proxy ADDRESS[:PORT]] --token TOKEN
  ```
### <a name="important-notes"></a>Observações importantes

- O nome do arquivo pode ser diferente, dependendo da versão do agente SIEM. 

- Recomendamos que você execute o arquivo JAR no seu servidor SIEM durante a configuração do servidor.

    - **Windows**: executar como uma tarefa agendada, certifique-se de configurar a tarefa para **executar se o usuário está conectado ou não** e desmarque a **tarefa parar se ela for executada por mais de** uma opção.

    - **Linux**: Adicione o comando executar com um **&** para o `rc.local` arquivo. <br/>Exemplo:<br/> 
    ```
    java -jar mcas-siemagent-0.87.20-signed.jar [--logsDirectory DIRNAME] [--proxy ADDRESS[:PORT]] --token TOKEN &
    ```

- Os parâmetros entre colchetes [] são opcionais e devem ser usados apenas se relevante. Use as seguintes variáveis:

    - **DIRNAME** é o caminho para o diretório que você deseja usar para logs de depuração do agente local.

    - **Endereço [:P ORT]** é o endereço do servidor proxy e a porta que o servidor usa para se conectar à Internet.

    - **Token** é o token do agente Siem que você copiou no primeiro procedimento.

    - Para obter ajuda, digite `-h`. 
  
## <a name="step-3-validate-that-the-siem-agent-is-working"></a>Etapa 3: validar que o agente SIEM está funcionando

1. Certifique-se de que o status do agente SIEM no portal do Office 365 Cloud app Security não seja exibido como **erro de conexão** ou desconectado e que não haja nenhuma notificação de agente. ****<br/>Por exemplo, é possível ver aqui que o servidor SIEM está conectado:<br/>![Servidor SIEM conectado](media/siem-connected.png)<br/>E aqui, podemos ver que o servidor SIEM está desconectado:<br/>![Servidor SIEM não conectado](media/siem-not-connected.png) 
  
2. Em seu servidor de syslog/SIEM, verifique se os alertas chegaram no Office 365 Cloud app Security.
  
## <a name="what-the-logfiles-look-like"></a>Como os logfiles se parecem

Veja um exemplo de Logfile de alerta que pode ser enviado para um servidor SIEM:

```
2017-07-15T20:42:30.531Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|myPolicy|3|externalId=596a7e360c204203a335a3fb start=1500151350531 end=1500151350531 msg=Activity policy ''myPolicy'' was triggered by ''admin@box-contoso.com'' suser=admin@box-contoso.com destinationServiceName=Box cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596a7e360c204203a335a3fb cs2Label=uniqueServiceAppIds cs2=APPID_BOX cs3Label=relatedAudits cs3=1500151288183_acc891bf-33e1-424b-a021-0d4370789660 cs4Label=policyIDs cs4=59f0ab82f797fa0681e9b1c7

2017-07-16T09:36:26.550Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy|3|externalId=596b339b0c204203a33a51ae start=1500197786550 end=1500197786550 msg=Activity policy ''test-activity-policy'' was triggered by ''user@contoso.com'' suser=user@contoso.com destinationServiceName=Salesforce cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b339b0c204203a33a51ae cs2Label=uniqueServiceAppIds cs2=APPID_SALESFORCE cs3Label=relatedAudits cs3=1500197720691_b7f6317c-b8de-476a-bc8f-dfa570e00349 cs4Label=policyIDs cs4=

2017-07-16T09:17:03.361Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy3|3|externalId=596b2fd70c204203a33a3eeb start=1500196623361 end=1500196623361 msg=Activity policy ''test-activity-policy3'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Office 365 cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b2fd70c204203a33a3eeb cs2Label=uniqueServiceAppIds cs2=APPID_O365 cs3Label=relatedAudits cs3=1500196549157_a0e01f8a-e29a-43ae-8599-783c1c11597d cs4Label=policyIDs cs4=

2017-07-16T09:17:15.426Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy|3|externalId=596b2fd70c204203a33a3eec start=1500196635426 end=1500196635426 msg=Activity policy ''test-activity-policy'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Microsoft Office 365 admin center cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b2fd70c204203a33a3eec cs2Label=uniqueServiceAppIds cs2=APPID_O365_PORTAL cs3Label=relatedAudits cs3=1500196557398_3e102b20-d9fa-4f66-b550-8c7a403bb4d8 cs4Label=policyIDs cs4=59f0ab35f797fa9811e9b1c7

2017-07-16T09:17:46.290Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy4|3|externalId=596b30200c204203a33a4765 start=1500196666290 end=1500196666290 msg=Activity policy ''test-activity-policy4'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Microsoft Exchange Online cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b30200c204203a33a4765 cs2Label=uniqueServiceAppIds cs2=APPID_OUTLOOK cs3Label=relatedAudits cs3=1500196587034_a8673602-7e95-46d6-a1fe-c156c4709c5d cs4Label=policyIDs cs4=

2017-07-16T09:41:04.369Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy2|3|externalId=596b34b10c204203a33a5240 start=1500198064369 end=1500198064369 msg=Activity policy ''test-activity-policy2'' was triggered by ''user2@test15-adallom.com'' suser=user2@test15-adallom.com destinationServiceName=Google cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b34b10c204203a33a5240 cs2Label=uniqueServiceAppIds cs2=APPID_33626 cs3Label=relatedAudits cs3=1500197996117_fd71f265-1e46-4f04-b372-2e32ec874cd3 cs4Label=policyIDs cs4=
```

E aqui está outro exemplo, desta vez no formato CEF:


|Nome do campo CEF  | Descrição  |
|---------|---------|
|inicialização     | carimbo de hora do alerta        |
|ponto     | carimbo de hora do alerta        |
|RT     | carimbo de hora do alerta        |
|msg     | Descrição de alerta conforme mostrado no portal do Office 365 Cloud app Security        |
|suser     | alerta de usuário de requerente        |
|destinationServiceName     | alerta o aplicativo de origem, como o Office 365, SharePoint ou OneDrive        |
|csLabel     | Varia (os rótulos têm significados diferentes). Normalmente, os rótulos são auto-explicativos, como targetObjects.        |
|cs     | Informações correspondentes a um rótulo (como o usuário de destino de um alerta, conforme o exemplo de rótulo)        |

## <a name="additional-tasks-as-needed"></a>Tarefas adicionais (conforme necessário)

Depois de configurar seu servidor SIEM e integrado ao Office 365 Cloud app Security, talvez seja necessário gerar um token novamente, editar um agente SIEM ou excluir um agente SIEM. As seções a seguir descrevem como realizar essas tarefas.

### <a name="regenerate-a-token"></a>Regenerar um token

Se você perder o token, poderá regenerar um. 

1. no portal do Office 365 Cloud App security ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)), escolha **configurações** > e**extensões de segurança**.

2. Na tabela, localize a linha do agente SIEM. 

3. Clique nas reticências e, em seguida, escolha **regenerar token**.<br/>![Regenerar um token clicando nas reticências do seu agente do SIEM](media/04de368a-b88e-4a9c-a830-58025cb98db6.png)
  
### <a name="edit-a-siem-agent"></a>Editar um agente SIEM

1. no portal do Office 365 Cloud App security ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)), escolha **configurações** > e**extensões de segurança**.

2. Localize a linha do agente SIEM. 

3. Clique nas reticências e, em seguida, escolha **Editar**. (Se você editar o agente SIEM, não será necessário executar novamente o arquivo. jar; ele é atualizado automaticamente.)<br/>![Para editar seu agente SIEM, escolha as reticências e, em seguida, escolha Editar.](media/96d0b362-3e0c-4dff-b2b4-d7af5b1bfb91.png)
  
### <a name="delete-a-siem-agent"></a>Excluir um agente SIEM

1. no portal do Office 365 Cloud App security ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)), escolha **configurações** > e**extensões de segurança**.

2. Localize a linha do agente SIEM. 

3. Clique nas reticências e escolha **excluir**.<br/>![Para excluir um agente SIEM, escolha as reticências e, em seguida, escolha Excluir.](media/540b5bdf-5574-4ecc-a7b0-92a499a387d7.png)

  
## <a name="next-steps"></a>Próximas etapas

- [Atividades de utilização após a implantação do Office 365 Cloud App Security](utilization-activities-for-ocas.md)
    
- [ReVisar e executar ação em alertas](review-office-365-cas-alerts.md)
    
- [Agrupar seus endereços IP para simplificar o gerenciamento](group-your-ip-addresses-in-ocas.md)
    


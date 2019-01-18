---
title: Integrar seu servidor SIEM ao Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: dd6d2417-49c4-4de6-9294-67fdabbf8532
description: É possível integrar seu servidor SIEM com segurança de aplicativo de nuvem do Office 365. Leia este artigo para obter uma visão geral de como ele funciona e como configurá-lo.
ms.openlocfilehash: 3cdae0389065b18da090139528eceefb007363fa
ms.sourcegitcommit: b0b0b716718c22779c7c04775b8010d65cd6656b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28723258"
---
# <a name="integrate-your-siem-server-with-office-365-cloud-app-security"></a><span data-ttu-id="93a6c-104">Integrar seu servidor SIEM ao Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="93a6c-104">Integrate your SIEM server with Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="93a6c-105">Avaliação \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="93a6c-105">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="93a6c-106">Planejamento \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="93a6c-106">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="93a6c-107">Implantação \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="93a6c-107">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="93a6c-108">Utilização \* \* \*</span><span class="sxs-lookup"><span data-stu-id="93a6c-108">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="93a6c-109">Comece a avaliar</span><span class="sxs-lookup"><span data-stu-id="93a6c-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="93a6c-110">Começar a planejar</span><span class="sxs-lookup"><span data-stu-id="93a6c-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="93a6c-111">Você está aqui!</span><span class="sxs-lookup"><span data-stu-id="93a6c-111">You are here!</span></span>  <br/> [<span data-ttu-id="93a6c-112">Próxima etapa</span><span class="sxs-lookup"><span data-stu-id="93a6c-112">Next step</span></span>](utilization-activities-for-ocas.md) <br/> |[<span data-ttu-id="93a6c-113">Iniciar a utilização</span><span class="sxs-lookup"><span data-stu-id="93a6c-113">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |
   
## <a name="overview-and-prerequisites"></a><span data-ttu-id="93a6c-114">Visão geral e pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="93a6c-114">Overview and prerequisites</span></span>

<span data-ttu-id="93a6c-p102">É possível integrar a [Segurança de aplicativo de nuvem do Office 365](get-ready-for-office-365-cas.md) com sua segurança eventos e informações management (SIEM) server para habilitar o monitoramento centralizado de alertas. Isso é especialmente vantajoso para organizações que estejam usando os serviços em nuvem e aplicativos do servidor local. Integrando com um servidor SIEM permite que sua equipe de segurança proteger melhor seus aplicativos do Office 365 enquanto mantém o seu fluxo de trabalho de segurança usual, automatizando determinados procedimentos de segurança e correlacionando entre baseado em nuvem e eventos no local.</span><span class="sxs-lookup"><span data-stu-id="93a6c-p102">You can integrate [Office 365 Cloud App Security](get-ready-for-office-365-cas.md) with your security information and event management (SIEM) server to enable centralized monitoring of alerts. This is especially beneficial for organizations who are using cloud services and on-premises server applications. Integrating with a SIEM server allows your security team to better protect your Office 365 applications while maintaining your usual security workflow, by automating certain security procedures and correlating between cloud-based and on-premises events.</span></span>  
  
<span data-ttu-id="93a6c-p103">Ao integrar seu servidor SIEM primeiro com segurança de aplicativo de nuvem do Office 365, alertas dos últimos dois dias são encaminhados para o servidor SIEM, bem como todos os alertas do então em (com base em quaisquer filtros que você selecionar). Além disso, se você desativar esse recurso por um longo período, quando você ativá-lo novamente, ele encaminhará últimos dois dias de alertas e, em seguida, todos os alertas a partir.</span><span class="sxs-lookup"><span data-stu-id="93a6c-p103">When you first integrate your SIEM server with Office 365 Cloud App Security, alerts from the last two days are forwarded to the SIEM server, as well as all alerts from then on (based on any filters you select). Additionally, if you disable this feature for an extended period, when you enable it again, it will forward the past two days of alerts and then all alerts from then on.</span></span>

### <a name="siem-integration-architecture"></a><span data-ttu-id="93a6c-120">Arquitetura de integração de SIEM</span><span class="sxs-lookup"><span data-stu-id="93a6c-120">SIEM integration architecture</span></span>

<span data-ttu-id="93a6c-p104">Um agente SIEM é configurado na rede da sua organização. Quando implantada e configurada, o agente SIEM extrai os tipos de dados que foram configurados (alertas) usando o Office 365 nuvem App segurança APIs por REST. O tráfego é enviado por um canal HTTPS criptografado na porta 443.</span><span class="sxs-lookup"><span data-stu-id="93a6c-p104">A SIEM agent is set up in your organization's network. When deployed and configured, the SIEM agent pulls the data types that were configured (alerts) using Office 365 Cloud App Security RESTful APIs. The traffic is then sent over an encrypted HTTPS channel on port 443.</span></span>
  
<span data-ttu-id="93a6c-124">Quando um agente SIEM recupera dados de segurança de aplicativo de nuvem do Office 365, ele envia as mensagens de Syslog para seu servidor SIEM local, usando as configurações de rede que são fornecidas durante a instalação (TCP ou UDP com uma porta personalizada).</span><span class="sxs-lookup"><span data-stu-id="93a6c-124">When a SIEM agent retrieves data from Office 365 Cloud App Security, it sends the Syslog messages to your local SIEM server using the network configurations that are provided during setup (TCP or UDP with a custom port).</span></span>

![Arquitetura de segurança de aplicativo de nuvem e SIEM](media/siem-architecture.png)

### <a name="supported-siem-servers"></a><span data-ttu-id="93a6c-126">Servidores SIEM suportados</span><span class="sxs-lookup"><span data-stu-id="93a6c-126">Supported SIEM servers</span></span>

<span data-ttu-id="93a6c-127">Atualmente, a segurança de aplicativo de nuvem do Office 365 suporta os seguintes servidores SIEM:</span><span class="sxs-lookup"><span data-stu-id="93a6c-127">Office 365 Cloud App Security currently supports the following SIEM servers:</span></span>
- <span data-ttu-id="93a6c-128">Foco Micro ArcSight</span><span class="sxs-lookup"><span data-stu-id="93a6c-128">Micro Focus ArcSight</span></span>
- <span data-ttu-id="93a6c-129">CEF genérico</span><span class="sxs-lookup"><span data-stu-id="93a6c-129">Generic CEF</span></span>

### <a name="prerequisites"></a><span data-ttu-id="93a6c-130">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="93a6c-130">Prerequisites</span></span>

- <span data-ttu-id="93a6c-p105">Você deve ser um administrador global ou administrador de segurança para executar as tarefas descritas neste artigo. Consulte [Permissions in a segurança do Office 365 &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md)</span><span class="sxs-lookup"><span data-stu-id="93a6c-p105">You must be a global administrator or security administrator to perform the tasks described in this article. See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md)</span></span>

- <span data-ttu-id="93a6c-133">Você deve ter a [segurança de aplicativo de nuvem do Office 365 habilitada](turn-on-office-365-cas.md) para sua organização.</span><span class="sxs-lookup"><span data-stu-id="93a6c-133">You must have [Office 365 Cloud App Security enabled](turn-on-office-365-cas.md) for your organization.</span></span>

- <span data-ttu-id="93a6c-134">[Log de auditoria](turn-audit-log-search-on-or-off.md) deve ser ativado para o Office 365</span><span class="sxs-lookup"><span data-stu-id="93a6c-134">[Audit logging](turn-audit-log-search-on-or-off.md) must be turned on for Office 365</span></span>

- <span data-ttu-id="93a6c-135">Você deve ter um servidor standard que atende aos seguintes requisitos para configurar a integração do servidor SIEM:</span><span class="sxs-lookup"><span data-stu-id="93a6c-135">You must have a standard server that meets the following requirements in order to configure SIEM server integration:</span></span>
    - <span data-ttu-id="93a6c-136">Sistema operacional: Windows ou Linux (pode ser uma máquina virtual)</span><span class="sxs-lookup"><span data-stu-id="93a6c-136">OS: Windows or Linux (this can be a virtual machine)</span></span>
    - <span data-ttu-id="93a6c-137">CPU: 2</span><span class="sxs-lookup"><span data-stu-id="93a6c-137">CPU: 2</span></span>
    - <span data-ttu-id="93a6c-138">Espaço em disco: 20 GB</span><span class="sxs-lookup"><span data-stu-id="93a6c-138">Disk space: 20 GB</span></span>
    - <span data-ttu-id="93a6c-139">RAM: 2 GB</span><span class="sxs-lookup"><span data-stu-id="93a6c-139">RAM: 2 GB</span></span>
    - <span data-ttu-id="93a6c-140">[Oracle Java 8](http://www.oracle.com/technetwork/java/javase/downloads/index.html) instalado</span><span class="sxs-lookup"><span data-stu-id="93a6c-140">[Oracle Java 8](http://www.oracle.com/technetwork/java/javase/downloads/index.html) installed</span></span>
    - <span data-ttu-id="93a6c-141">Firewall configurado conforme descrito em [requisitos de rede](https://docs.microsoft.com/cloud-app-security/network-requirements)</span><span class="sxs-lookup"><span data-stu-id="93a6c-141">Firewall configured as described in [Network requirements](https://docs.microsoft.com/cloud-app-security/network-requirements)</span></span>

- <span data-ttu-id="93a6c-p106">Você deve ter os detalhes sobre o seu **host remoto syslog** e o **número da porta Syslot**. Um administrador da rede ou o administrador de segurança deve ser capaz de ajudar você a encontrar essas informações.</span><span class="sxs-lookup"><span data-stu-id="93a6c-p106">You must have details about your **Remote syslog host** and **Syslot port number**. A network administrator or security administrator should be able to help you locate that information.</span></span> 

- <span data-ttu-id="93a6c-144">Você deve concordar com [os termos de licença de software](https://go.microsoft.com/fwlink/?linkid=862491) baixar o [arquivo JAR](https://go.microsoft.com/fwlink/?linkid=838596) será necessário para integrar o seu servidor SIEM.</span><span class="sxs-lookup"><span data-stu-id="93a6c-144">You must agree to [software license terms](https://go.microsoft.com/fwlink/?linkid=862491) to download the [JAR file](https://go.microsoft.com/fwlink/?linkid=838596) you'll need to integrate your SIEM server.</span></span>
 
## <a name="step-1-set-it-up-a-siem-agent-in-office-365-cloud-app-security"></a><span data-ttu-id="93a6c-145">Etapa 1: Montá-lo um agente SIEM na segurança de aplicativo de nuvem do Office 365</span><span class="sxs-lookup"><span data-stu-id="93a6c-145">Step 1: Set it up a SIEM agent in Office 365 Cloud App Security</span></span>

1. <span data-ttu-id="93a6c-p107">Vá para [https://protection.office.com](https://protection.office.com) e entrar usando sua conta de trabalho ou da escola para o Office 365. (Isso leva você para a segurança &amp; Centro de conformidade.)</span><span class="sxs-lookup"><span data-stu-id="93a6c-p107">Go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account for Office 365. (This takes you to the Security &amp; Compliance Center.)</span></span> 
    
2. <span data-ttu-id="93a6c-148">Vá para **alertas** \> **avançadas de gerenciar alertas**.</span><span class="sxs-lookup"><span data-stu-id="93a6c-148">Go to **Alerts** \> **Manage advanced alerts**.</span></span>
    
3. <span data-ttu-id="93a6c-p108">Escolha **vá para segurança de aplicativo do Office 365 nuvem**.</span><span class="sxs-lookup"><span data-stu-id="93a6c-p108">Choose **Go to Office 365 Cloud App Security**. </span></span><br/>
    <span data-ttu-id="93a6c-150">![Na segurança &amp; Centro de conformidade, escolha gerenciar alertas avançadas para ir à segurança de aplicativo de nuvem do Office 365](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span><span class="sxs-lookup"><span data-stu-id="93a6c-150">![In the Security &amp; Compliance Center, choose Manage Advanced Alerts to go to Office 365 Cloud App Security](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span></span>
  
4. <span data-ttu-id="93a6c-151">Clique em **configurações** \> **extensões de segurança**e escolha agentes SIEM.</span><span class="sxs-lookup"><span data-stu-id="93a6c-151">Click **Settings** \> **Security extensions**, and then choose SIEM agents.</span></span><br/>
<span data-ttu-id="93a6c-152">![Escolha gt _ de configurações de extensões de segurança](media/Settings-SecurityExtensions.png)</span><span class="sxs-lookup"><span data-stu-id="93a6c-152">![Choose Settings > Security extensions](media/Settings-SecurityExtensions.png)</span></span>

5. <span data-ttu-id="93a6c-153">Escolha **Adicionar SIEM agente**.</span><span class="sxs-lookup"><span data-stu-id="93a6c-153">Choose **Add SIEM agent**.</span></span><br/><span data-ttu-id="93a6c-154">![Escolha o agente de adicionar SIEM.](media/SIEMAgents.png)</span><span class="sxs-lookup"><span data-stu-id="93a6c-154">![Choose Add SIEM agent.](media/SIEMAgents.png)</span></span>
    
6. <span data-ttu-id="93a6c-155">Clique em **Iniciar o assistente**.</span><span class="sxs-lookup"><span data-stu-id="93a6c-155">Choose **Start wizard**.</span></span><br/><span data-ttu-id="93a6c-156">![Obtenha ajuda ou iniciar o Assistente](media/HelpOrWizard.png)</span><span class="sxs-lookup"><span data-stu-id="93a6c-156">![Get help or start the wizard](media/HelpOrWizard.png)</span></span> 
    
7. <span data-ttu-id="93a6c-p109">Na etapa **Geral** , especifique um nome e **Selecione o seu formato de SIEM** e defina qualquer **Configurações avançadas** que são relevantes para esse formato. Escolha **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="93a6c-p109">In the **General** step, specify a name, and **Select your SIEM format** and set any **Advanced settings** that are relevant to that format. Then choose **Next**.</span></span><br/><span data-ttu-id="93a6c-159">![Especifique um nome e tipo](media/ChooseAgentTypeAndName.png)</span><span class="sxs-lookup"><span data-stu-id="93a6c-159">![Specify a name and type](media/ChooseAgentTypeAndName.png)</span></span>
    
8. <span data-ttu-id="93a6c-p110">Na etapa **Syslog remoto** , especifique o endereço IP ou o nome de host do **host remoto syslog** e o **número da porta Syslog**. Selecione TCP ou UDP como o protocolo de Syslog remoto. (Você pode trabalhar com o administrador de segurança ou o administrador da rede para obter esses detalhes se você não tivê-los). Escolha **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="93a6c-p110">In the **Remote Syslog** step, specify the IP address or hostname of the **Remote syslog host** and the **Syslog port number**. Select TCP or UDP as the Remote Syslog protocol. (You can work with your network administrator or security administrator to get these details if you don't have them.) Then choose **Next**.</span></span><br/><span data-ttu-id="93a6c-163">![Especificar detalhes de Syslog remoto](media/ArcSightS1Syslog.png)</span><span class="sxs-lookup"><span data-stu-id="93a6c-163">![Specify Remote Syslog details](media/ArcSightS1Syslog.png)</span></span>
  
9. <span data-ttu-id="93a6c-164">Na etapa **Tipos de dados** , siga um destes procedimentos e clique em **Avançar**:</span><span class="sxs-lookup"><span data-stu-id="93a6c-164">In the **Data Types** step, do one of the following, and then click **Next**:</span></span>
    - <span data-ttu-id="93a6c-165">Mantenha a configuração padrão de **Todos os alertas**</span><span class="sxs-lookup"><span data-stu-id="93a6c-165">Keep the default setting of **All Alerts**</span></span><br/><span data-ttu-id="93a6c-166">OU</span><span class="sxs-lookup"><span data-stu-id="93a6c-166">OR</span></span>
    - <span data-ttu-id="93a6c-p111">Clique em **todos os alertas**e escolha **filtros específicos**. Defina filtros para selecionar os tipos de alertas que você deseja enviar ao seu servidor SIEM.</span><span class="sxs-lookup"><span data-stu-id="93a6c-p111">Click **All alerts**, and then choose **Specific filters**. Define filters to select the kinds of alerts you want to send to your SIEM server. </span></span><br/><span data-ttu-id="93a6c-169">![Etapa de tipos de dados do Assistente](media/ArcSightS1ExportOptions.png)</span><span class="sxs-lookup"><span data-stu-id="93a6c-169">![Data Types step of the wizard](media/ArcSightS1ExportOptions.png)</span></span>
  
10. <span data-ttu-id="93a6c-170">Na tela Parabéns, copie o token e salvá-lo para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="93a6c-170">On the Congratulations screen, copy the token and save it for later.</span></span><br/>![Tela de agente criado SIEM](media/SIEMAgentFinished.png) 

> [!IMPORTANT]
> <span data-ttu-id="93a6c-p112">Neste ponto, você configurou um agente SIEM na segurança de aplicativo de nuvem do Office 365, mas sua integração do servidor SIEM ainda não estiver concluída. Vá para a próxima etapa para continuar sua integração do servidor SIEM.</span><span class="sxs-lookup"><span data-stu-id="93a6c-p112">At this point, you have set up a SIEM agent in Office 365 Cloud App Security, but your SIEM server integration is not yet finished. Proceed to the next step to continue your SIEM server integration.</span></span>

<span data-ttu-id="93a6c-p113">Depois que você clique em Fechar e sair do assistente, na tela de extensões de segurança, você pode ver o agente SIEM adicionada na tabela. Ela mostrará o status **criado** até que ele esteja conectado posteriormente.</span><span class="sxs-lookup"><span data-stu-id="93a6c-p113">After you click Close and leave the wizard, on the Security extensions screen, you can see the SIEM agent you added in the table. It will show a status of **Created** until it's connected later.</span></span>

![Agente SIEM criado](media/SIEMAgentCreated.png)
    
## <a name="step-2-download-a-jar-file-and-run-it-on-your-siem-server"></a><span data-ttu-id="93a6c-177">Etapa 2: Baixar um arquivo JAR e executá-lo em seu servidor SIEM</span><span class="sxs-lookup"><span data-stu-id="93a6c-177">Step 2: Download a JAR file and run it on your SIEM server</span></span>

1. <span data-ttu-id="93a6c-p114">Baixe o [Microsoft Cloud App segurança SIEM Agent](https://go.microsoft.com/fwlink/?linkid=838596) e descompacte a pasta. (Você deve concordar com [os termos de licença de software](https://go.microsoft.com/fwlink/?linkid=862491) para continuar.)</span><span class="sxs-lookup"><span data-stu-id="93a6c-p114">Download the [Microsoft Cloud App Security SIEM Agent](https://go.microsoft.com/fwlink/?linkid=838596) and unzip the folder. (You must agree to [software license terms](https://go.microsoft.com/fwlink/?linkid=862491) in order to proceed.)</span></span> 
    
2. <span data-ttu-id="93a6c-180">Extraia o arquivo. jar da pasta compactada e executá-lo em seu servidor SIEM.</span><span class="sxs-lookup"><span data-stu-id="93a6c-180">Extract the .jar file from the zipped folder and run it on your SIEM server.</span></span>
    
3. <span data-ttu-id="93a6c-181">Depois de executar o arquivo, execute o seguinte: comando:</span><span class="sxs-lookup"><span data-stu-id="93a6c-181">After running the file, run the following: command:</span></span><br/>
  ```
  java -jar mcas-siemagent-0.87.20-signed.jar [--logsDirectory DIRNAME] [--proxy ADDRESS[:PORT]] --token TOKEN
  ```
### <a name="important-notes"></a><span data-ttu-id="93a6c-182">Observações importantes</span><span class="sxs-lookup"><span data-stu-id="93a6c-182">Important notes</span></span>

- <span data-ttu-id="93a6c-183">O nome do arquivo pode diferir, dependendo da versão do agente SIEM.</span><span class="sxs-lookup"><span data-stu-id="93a6c-183">The file name may differ depending on the version of the SIEM agent.</span></span> 

- <span data-ttu-id="93a6c-184">Recomendamos que você execute o arquivo JAR no seu servidor SIEM durante a instalação do servidor.</span><span class="sxs-lookup"><span data-stu-id="93a6c-184">We recommend that you run the JAR file on your SIEM server during server setup.</span></span>

    - <span data-ttu-id="93a6c-185">**Windows**: executar como uma tarefa agendada, certificando-se de configurar a tarefa seja **executada se o usuário está conectado ou não** e desmarque a opção de **interromper a tarefa caso ela seja executada superiores** .</span><span class="sxs-lookup"><span data-stu-id="93a6c-185">**Windows**: Run as a scheduled task, making sure to configure the task to **Run whether the user is logged on or not** and clear the **Stop the task if it runs longer than** option.</span></span>

    - <span data-ttu-id="93a6c-186">**Linux**: adicionar o comando de execução com um **&** para o `rc.local` arquivo.</span><span class="sxs-lookup"><span data-stu-id="93a6c-186">**Linux**: Add the run command with an **&** to the `rc.local` file.</span></span> <br/><span data-ttu-id="93a6c-187">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="93a6c-187">Example:</span></span><br/> 
    ```
    java -jar mcas-siemagent-0.87.20-signed.jar [--logsDirectory DIRNAME] [--proxy ADDRESS[:PORT]] --token TOKEN &
    ```

- <span data-ttu-id="93a6c-p115">Parâmetros entre colchetes [] são opcionais e devem ser usados somente se relevantes. Use as seguintes variáveis:</span><span class="sxs-lookup"><span data-stu-id="93a6c-p115">Parameters in brackets [] are optional, and should be used only if relevant. Use the following variables:</span></span>

    - <span data-ttu-id="93a6c-190">**DIRNAME** é o caminho até o diretório que você deseja usar para logs de depuração do agente local.</span><span class="sxs-lookup"><span data-stu-id="93a6c-190">**DIRNAME** is the path to the directory you want to use for local agent debug logs.</span></span>

    - <span data-ttu-id="93a6c-191">**Endereço [: porta]** é o endereço do servidor proxy e a porta que o servidor usa para se conectar à Internet.</span><span class="sxs-lookup"><span data-stu-id="93a6c-191">**ADDRESS[:PORT]** is the proxy server address and port that the server uses to connect to the Internet.</span></span>

    - <span data-ttu-id="93a6c-192">**TOKEN** é o token de agente SIEM copiados no primeiro procedimento.</span><span class="sxs-lookup"><span data-stu-id="93a6c-192">**TOKEN** is the SIEM agent token you copied in the first procedure.</span></span>

    - <span data-ttu-id="93a6c-193">Para obter ajuda, digite `-h`.</span><span class="sxs-lookup"><span data-stu-id="93a6c-193">To get help, type `-h`.</span></span> 
  
## <a name="step-3-validate-that-the-siem-agent-is-working"></a><span data-ttu-id="93a6c-194">Etapa 3: Validar se o agente SIEM está funcionando</span><span class="sxs-lookup"><span data-stu-id="93a6c-194">Step 3: Validate that the SIEM agent is working</span></span>

1. <span data-ttu-id="93a6c-195">Verifique se o status do agente SIEM no portal de segurança de aplicativo de nuvem do Office 365 não é exibido como **erro de Conexão** ou **desconectada** e que não há nenhuma notificação de agente.</span><span class="sxs-lookup"><span data-stu-id="93a6c-195">Make sure the status of the SIEM agent in the Office 365 Cloud App Security portal is not displayed as **Connection error** or **Disconnected** and that there are no agent notifications.</span></span><br/><span data-ttu-id="93a6c-196">Por exemplo, aqui podemos ver que o servidor SIEM está conectado:</span><span class="sxs-lookup"><span data-stu-id="93a6c-196">For example, here we can see the SIEM server is connected:</span></span><br/><span data-ttu-id="93a6c-197">![Servidor SIEM conectado](media/siem-connected.png)</span><span class="sxs-lookup"><span data-stu-id="93a6c-197">![SIEM server connected](media/siem-connected.png)</span></span><br/><span data-ttu-id="93a6c-198">E aqui, podemos ver que o servidor SIEM é desconectado:</span><span class="sxs-lookup"><span data-stu-id="93a6c-198">And here, we can see the SIEM server is disconnected:</span></span><br/><span data-ttu-id="93a6c-199">![Servidor SIEM não conectado](media/siem-not-connected.png)</span><span class="sxs-lookup"><span data-stu-id="93a6c-199">![SIEM server not connected](media/siem-not-connected.png)</span></span> 
  
2. <span data-ttu-id="93a6c-200">No seu servidor Syslog/SIEM, verifique se que você vê que os alertas foram recebidos de segurança de aplicativo de nuvem do Office 365.</span><span class="sxs-lookup"><span data-stu-id="93a6c-200">In your Syslog/SIEM server, make sure you see that alerts have arrived from Office 365 Cloud App Security.</span></span>
  
## <a name="what-the-logfiles-look-like"></a><span data-ttu-id="93a6c-201">Aparência dos arquivos de log</span><span class="sxs-lookup"><span data-stu-id="93a6c-201">What the logfiles look like</span></span>

<span data-ttu-id="93a6c-202">Aqui está um exemplo de arquivo de log de alertas que pode ser enviado para um servidor SIEM:</span><span class="sxs-lookup"><span data-stu-id="93a6c-202">Here's an alerts logfile example that might be sent to a SIEM server:</span></span>

```
2017-07-15T20:42:30.531Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|myPolicy|3|externalId=596a7e360c204203a335a3fb start=1500151350531 end=1500151350531 msg=Activity policy ''myPolicy'' was triggered by ''admin@box-contoso.com'' suser=admin@box-contoso.com destinationServiceName=Box cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596a7e360c204203a335a3fb cs2Label=uniqueServiceAppIds cs2=APPID_BOX cs3Label=relatedAudits cs3=1500151288183_acc891bf-33e1-424b-a021-0d4370789660 cs4Label=policyIDs cs4=59f0ab82f797fa0681e9b1c7

2017-07-16T09:36:26.550Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy|3|externalId=596b339b0c204203a33a51ae start=1500197786550 end=1500197786550 msg=Activity policy ''test-activity-policy'' was triggered by ''user@contoso.com'' suser=user@contoso.com destinationServiceName=Salesforce cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b339b0c204203a33a51ae cs2Label=uniqueServiceAppIds cs2=APPID_SALESFORCE cs3Label=relatedAudits cs3=1500197720691_b7f6317c-b8de-476a-bc8f-dfa570e00349 cs4Label=policyIDs cs4=

2017-07-16T09:17:03.361Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy3|3|externalId=596b2fd70c204203a33a3eeb start=1500196623361 end=1500196623361 msg=Activity policy ''test-activity-policy3'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Office 365 cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b2fd70c204203a33a3eeb cs2Label=uniqueServiceAppIds cs2=APPID_O365 cs3Label=relatedAudits cs3=1500196549157_a0e01f8a-e29a-43ae-8599-783c1c11597d cs4Label=policyIDs cs4=

2017-07-16T09:17:15.426Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy|3|externalId=596b2fd70c204203a33a3eec start=1500196635426 end=1500196635426 msg=Activity policy ''test-activity-policy'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Microsoft Office 365 admin center cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b2fd70c204203a33a3eec cs2Label=uniqueServiceAppIds cs2=APPID_O365_PORTAL cs3Label=relatedAudits cs3=1500196557398_3e102b20-d9fa-4f66-b550-8c7a403bb4d8 cs4Label=policyIDs cs4=59f0ab35f797fa9811e9b1c7

2017-07-16T09:17:46.290Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy4|3|externalId=596b30200c204203a33a4765 start=1500196666290 end=1500196666290 msg=Activity policy ''test-activity-policy4'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Microsoft Exchange Online cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b30200c204203a33a4765 cs2Label=uniqueServiceAppIds cs2=APPID_OUTLOOK cs3Label=relatedAudits cs3=1500196587034_a8673602-7e95-46d6-a1fe-c156c4709c5d cs4Label=policyIDs cs4=

2017-07-16T09:41:04.369Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy2|3|externalId=596b34b10c204203a33a5240 start=1500198064369 end=1500198064369 msg=Activity policy ''test-activity-policy2'' was triggered by ''user2@test15-adallom.com'' suser=user2@test15-adallom.com destinationServiceName=Google cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b34b10c204203a33a5240 cs2Label=uniqueServiceAppIds cs2=APPID_33626 cs3Label=relatedAudits cs3=1500197996117_fd71f265-1e46-4f04-b372-2e32ec874cd3 cs4Label=policyIDs cs4=
```

<span data-ttu-id="93a6c-203">E aqui está outro exemplo, desta vez, no formato CEF:</span><span class="sxs-lookup"><span data-stu-id="93a6c-203">And here's another sample, this time in CEF format:</span></span>


|<span data-ttu-id="93a6c-204">Nome do campo CEF</span><span class="sxs-lookup"><span data-stu-id="93a6c-204">CEF field name</span></span>  | <span data-ttu-id="93a6c-205">Descrição</span><span class="sxs-lookup"><span data-stu-id="93a6c-205">Description</span></span>  |
|---------|---------|
|<span data-ttu-id="93a6c-206">Iniciar</span><span class="sxs-lookup"><span data-stu-id="93a6c-206">start</span></span>     | <span data-ttu-id="93a6c-207">carimbo de hora de alerta</span><span class="sxs-lookup"><span data-stu-id="93a6c-207">alert timestamp</span></span>        |
|<span data-ttu-id="93a6c-208">end</span><span class="sxs-lookup"><span data-stu-id="93a6c-208">end</span></span>     | <span data-ttu-id="93a6c-209">carimbo de hora de alerta</span><span class="sxs-lookup"><span data-stu-id="93a6c-209">alert timestamp</span></span>        |
|<span data-ttu-id="93a6c-210">RT</span><span class="sxs-lookup"><span data-stu-id="93a6c-210">rt</span></span>     | <span data-ttu-id="93a6c-211">carimbo de hora de alerta</span><span class="sxs-lookup"><span data-stu-id="93a6c-211">alert timestamp</span></span>        |
|<span data-ttu-id="93a6c-212">msg</span><span class="sxs-lookup"><span data-stu-id="93a6c-212">msg</span></span>     | <span data-ttu-id="93a6c-213">Descrição de alerta, conforme mostrado no portal de segurança de aplicativo de nuvem do Office 365</span><span class="sxs-lookup"><span data-stu-id="93a6c-213">alert description as shown in the Office 365 Cloud App Security portal</span></span>        |
|<span data-ttu-id="93a6c-214">suser</span><span class="sxs-lookup"><span data-stu-id="93a6c-214">suser</span></span>     | <span data-ttu-id="93a6c-215">usuário de assunto de alerta</span><span class="sxs-lookup"><span data-stu-id="93a6c-215">alert subject user</span></span>        |
|<span data-ttu-id="93a6c-216">destinationServiceName</span><span class="sxs-lookup"><span data-stu-id="93a6c-216">destinationServiceName</span></span>     | <span data-ttu-id="93a6c-217">alerta provenientes de aplicativo, como o Office 365, SharePoint ou OneDrive</span><span class="sxs-lookup"><span data-stu-id="93a6c-217">alert originating app, such as Office 365, SharePoint, or OneDrive</span></span>        |
|<span data-ttu-id="93a6c-218">csLabel</span><span class="sxs-lookup"><span data-stu-id="93a6c-218">csLabel</span></span>     | <span data-ttu-id="93a6c-p116">Varia (rótulos tem significados diferentes). Normalmente, os rótulos são auto-explicativos, como targetObjects.</span><span class="sxs-lookup"><span data-stu-id="93a6c-p116">Varies (labels have different meanings). Typically, labels are self-explanatory, like targetObjects.</span></span>        |
|<span data-ttu-id="93a6c-221">cs</span><span class="sxs-lookup"><span data-stu-id="93a6c-221">cs</span></span>     | <span data-ttu-id="93a6c-222">Informações correspondendo a um rótulo (por exemplo, o usuário de destino de um alerta conforme o exemplo de rótulo)</span><span class="sxs-lookup"><span data-stu-id="93a6c-222">Information corresponding to a label (such as the target user of an alert as per the label example)</span></span>        |

## <a name="additional-tasks-as-needed"></a><span data-ttu-id="93a6c-223">Tarefas adicionais (conforme necessário)</span><span class="sxs-lookup"><span data-stu-id="93a6c-223">Additional tasks (as needed)</span></span>

<span data-ttu-id="93a6c-p117">Depois que você configurou seu servidor SIEM e integrou com segurança de aplicativo de nuvem do Office 365, talvez seja necessário regenerar um token, um agente SIEM de editar ou excluir um operador SIEM. As seções a seguir descrevem como executar essas tarefas.</span><span class="sxs-lookup"><span data-stu-id="93a6c-p117">After you have configured your SIEM server and have integrated it with Office 365 Cloud App Security, you might need to regenerate a token, edit a SIEM agent, or delete a SIEM agent. The following sections describe how to perform these tasks.</span></span>

### <a name="regenerate-a-token"></a><span data-ttu-id="93a6c-226">Regenere um token</span><span class="sxs-lookup"><span data-stu-id="93a6c-226">Regenerate a token</span></span>

<span data-ttu-id="93a6c-227">Se você perder o token de seu, você poderá regenerar uma.</span><span class="sxs-lookup"><span data-stu-id="93a6c-227">If you lose your token, you can regenerate one.</span></span> 

1. <span data-ttu-id="93a6c-228">No portal de segurança de aplicativo de nuvem do Office 365, escolha **configurações** > **extensões de segurança**.</span><span class="sxs-lookup"><span data-stu-id="93a6c-228">In the Office 365 Cloud App Security portal, choose **Settings** > **Security extensions**.</span></span>

2. <span data-ttu-id="93a6c-229">Na tabela, localize a linha para o agente de SIEM.</span><span class="sxs-lookup"><span data-stu-id="93a6c-229">In the table, locate the row for the SIEM agent.</span></span> 

3. <span data-ttu-id="93a6c-230">Clique nas reticências e escolha **regenerar token**.</span><span class="sxs-lookup"><span data-stu-id="93a6c-230">Click the ellipses, and then choose **Regenerate token**.</span></span><br/><span data-ttu-id="93a6c-231">![Regenere um token clicando nas reticências para seu agente SIEM](media/04de368a-b88e-4a9c-a830-58025cb98db6.png)</span><span class="sxs-lookup"><span data-stu-id="93a6c-231">![Regenerate a token by clicking the ellipsis for your SIEM agent](media/04de368a-b88e-4a9c-a830-58025cb98db6.png)</span></span>
  
### <a name="edit-a-siem-agent"></a><span data-ttu-id="93a6c-232">Editar um agente SIEM</span><span class="sxs-lookup"><span data-stu-id="93a6c-232">Edit a SIEM agent</span></span>

1. <span data-ttu-id="93a6c-233">No portal de segurança de aplicativo de nuvem do Office 365, escolha **configurações** > **extensões de segurança**.</span><span class="sxs-lookup"><span data-stu-id="93a6c-233">In the Office 365 Cloud App Security portal, choose **Settings** > **Security extensions**.</span></span>

2. <span data-ttu-id="93a6c-234">Localize a linha para o agente de SIEM.</span><span class="sxs-lookup"><span data-stu-id="93a6c-234">Locate the row for the SIEM agent.</span></span> 

3. <span data-ttu-id="93a6c-p118">Clique nas reticências e escolha **Editar**. (Se você editar o agente SIEM, você não precisará executar novamente o arquivo. jar; ele atualiza automaticamente.)</span><span class="sxs-lookup"><span data-stu-id="93a6c-p118">Click the ellipses, and then choose **Edit**. (If you edit the SIEM agent, you do not need to re-run the .jar file; it updates automatically.) </span></span><br/><span data-ttu-id="93a6c-237">![Para editar seu agente SIEM, escolha as elipses e escolha Editar.](media/96d0b362-3e0c-4dff-b2b4-d7af5b1bfb91.png)</span><span class="sxs-lookup"><span data-stu-id="93a6c-237">![To edit your SIEM agent, choose the ellipses, and then choose Edit.](media/96d0b362-3e0c-4dff-b2b4-d7af5b1bfb91.png)</span></span>
  
### <a name="delete-a-siem-agent"></a><span data-ttu-id="93a6c-238">Excluir um operador SIEM</span><span class="sxs-lookup"><span data-stu-id="93a6c-238">Delete a SIEM agent</span></span>

1. <span data-ttu-id="93a6c-239">No portal de segurança de aplicativo de nuvem do Office 365, escolha **configurações** > **extensões de segurança**.</span><span class="sxs-lookup"><span data-stu-id="93a6c-239">In the Office 365 Cloud App Security portal, choose **Settings** > **Security extensions**.</span></span>

2. <span data-ttu-id="93a6c-240">Localize a linha para o agente de SIEM.</span><span class="sxs-lookup"><span data-stu-id="93a6c-240">Locate the row for the SIEM agent.</span></span> 

3. <span data-ttu-id="93a6c-241">Clique nas reticências e escolha **Excluir**.</span><span class="sxs-lookup"><span data-stu-id="93a6c-241">Click the ellipses, and then choose **Delete**.</span></span><br/><span data-ttu-id="93a6c-242">![Para excluir um agente SIEM, escolha as elipses e escolha Excluir.](media/540b5bdf-5574-4ecc-a7b0-92a499a387d7.png)</span><span class="sxs-lookup"><span data-stu-id="93a6c-242">![To delete a SIEM agent, choose the ellipses, and then choose Delete.](media/540b5bdf-5574-4ecc-a7b0-92a499a387d7.png)</span></span>

  
## <a name="next-steps"></a><span data-ttu-id="93a6c-243">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="93a6c-243">Next steps</span></span>

- [<span data-ttu-id="93a6c-244">Atividades de utilização após a implantação do Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="93a6c-244">Utilization activities after rolling out Office 365 Cloud App Security</span></span>](utilization-activities-for-ocas.md)
    
- [<span data-ttu-id="93a6c-245">Revise e agir em alertas</span><span class="sxs-lookup"><span data-stu-id="93a6c-245">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="93a6c-246">Seus endereços IP para simplificar o gerenciamento de grupo</span><span class="sxs-lookup"><span data-stu-id="93a6c-246">Group your IP addresses to simplify management</span></span>](group-your-ip-addresses-in-ocas.md)
    


---
title: Integrar seu servidor SIEM com o Office 365 Cloud app Security
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
ms.openlocfilehash: 82b5e0e6467bd42acba3c40d67e4e0363a7e0f72
ms.sourcegitcommit: 4abcc03497478abf1ae7fc84792f44360d8e59c1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/12/2019
ms.locfileid: "30548581"
---
# <a name="integrate-your-siem-server-with-office-365-cloud-app-security"></a><span data-ttu-id="58e8f-104">Integrar seu servidor SIEM com o Office 365 Cloud app Security</span><span class="sxs-lookup"><span data-stu-id="58e8f-104">Integrate your SIEM server with Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="58e8f-105">Avaliação \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="58e8f-105">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="58e8f-106">Planejamento \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="58e8f-106">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="58e8f-107">Implantação \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="58e8f-107">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="58e8f-108">Utilização \* \* \*</span><span class="sxs-lookup"><span data-stu-id="58e8f-108">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="58e8f-109">Iniciar avaliação</span><span class="sxs-lookup"><span data-stu-id="58e8f-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="58e8f-110">Iniciar planejamento</span><span class="sxs-lookup"><span data-stu-id="58e8f-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="58e8f-111">Você está aqui!</span><span class="sxs-lookup"><span data-stu-id="58e8f-111">You are here!</span></span>  <br/> [<span data-ttu-id="58e8f-112">Próxima etapa</span><span class="sxs-lookup"><span data-stu-id="58e8f-112">Next step</span></span>](utilization-activities-for-ocas.md) <br/> |[<span data-ttu-id="58e8f-113">Começar a usar</span><span class="sxs-lookup"><span data-stu-id="58e8f-113">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |
   
## <a name="overview-and-prerequisites"></a><span data-ttu-id="58e8f-114">Visão geral e pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="58e8f-114">Overview and prerequisites</span></span>

<span data-ttu-id="58e8f-115">Você pode integrar o [Office 365 Cloud app Security](get-ready-for-office-365-cas.md) ao seu servidor de gerenciamento de eventos e informações de segurança (Siem) para habilitar o monitoramento centralizado de alertas.</span><span class="sxs-lookup"><span data-stu-id="58e8f-115">You can integrate [Office 365 Cloud App Security](get-ready-for-office-365-cas.md) with your security information and event management (SIEM) server to enable centralized monitoring of alerts.</span></span> <span data-ttu-id="58e8f-116">Isso é especialmente vantajoso para organizações que usam serviços de nuvem e aplicativos de servidor local.</span><span class="sxs-lookup"><span data-stu-id="58e8f-116">This is especially beneficial for organizations who are using cloud services and on-premises server applications.</span></span> <span data-ttu-id="58e8f-117">Você pode integrar seu servidor SIEM para receber alertas e atividades do Office 365 Cloud app Security no seu servidor SIEM.</span><span class="sxs-lookup"><span data-stu-id="58e8f-117">You can integrate your SIEM server to pull alerts and activities from Office 365 Cloud App Security into your SIEM server.</span></span> <span data-ttu-id="58e8f-118">A integração com um servidor SIEM permite que sua equipe de segurança melhor proteja seus aplicativos do Office 365 enquanto mantém seu fluxo de trabalho de segurança usual, automatizando determinados procedimentos de segurança e correlacionando entre eventos baseados em nuvem e locais.</span><span class="sxs-lookup"><span data-stu-id="58e8f-118">Integrating with a SIEM server allows your security team to better protect your Office 365 applications while maintaining your usual security workflow, by automating certain security procedures and correlating between cloud-based and on-premises events.</span></span>  
  
<span data-ttu-id="58e8f-119">Quando você integra pela primeira vez o seu servidor SIEM com o Office 365 Cloud app Security, os alertas dos últimos dois dias são encaminhados para o servidor SIEM, bem como todos os alertas de depois (com base nos filtros selecionados).</span><span class="sxs-lookup"><span data-stu-id="58e8f-119">When you first integrate your SIEM server with Office 365 Cloud App Security, alerts from the last two days are forwarded to the SIEM server, as well as all alerts from then on (based on any filters you select).</span></span> <span data-ttu-id="58e8f-120">Além disso, se você desabilitar esse recurso por um período estendido, ao habilitá-lo novamente, ele encaminhará os últimos dois dias de alertas e todos os alertas de então em diante.</span><span class="sxs-lookup"><span data-stu-id="58e8f-120">Additionally, if you disable this feature for an extended period, when you enable it again, it will forward the past two days of alerts and then all alerts from then on.</span></span>

### <a name="siem-integration-architecture"></a><span data-ttu-id="58e8f-121">Arquitetura de integração do SIEM</span><span class="sxs-lookup"><span data-stu-id="58e8f-121">SIEM integration architecture</span></span>

<span data-ttu-id="58e8f-122">Um agente SIEM é configurado na rede da sua organização.</span><span class="sxs-lookup"><span data-stu-id="58e8f-122">A SIEM agent is set up in your organization's network.</span></span> <span data-ttu-id="58e8f-123">Quando implantado e configurado, o agente SIEM Obtém os tipos de dados que foram configurados (alertas) usando as APIs do Office 365 Cloud app Security RESTful.</span><span class="sxs-lookup"><span data-stu-id="58e8f-123">When deployed and configured, the SIEM agent pulls the data types that were configured (alerts) using Office 365 Cloud App Security RESTful APIs.</span></span> <span data-ttu-id="58e8f-124">O tráfego é enviado por um canal HTTPS criptografado na porta 443.</span><span class="sxs-lookup"><span data-stu-id="58e8f-124">The traffic is then sent over an encrypted HTTPS channel on port 443.</span></span>
  
<span data-ttu-id="58e8f-125">Quando um agente SIEM recupera dados do Office 365 Cloud app Security, ele envia as mensagens de syslog para seu servidor SIEM local usando as configurações de rede fornecidas durante a instalação (TCP ou UDP com uma porta personalizada).</span><span class="sxs-lookup"><span data-stu-id="58e8f-125">When a SIEM agent retrieves data from Office 365 Cloud App Security, it sends the Syslog messages to your local SIEM server using the network configurations that are provided during setup (TCP or UDP with a custom port).</span></span>

![Arquitetura do SIEM e do Cloud app Security](media/siem-architecture.png)

### <a name="supported-siem-servers"></a><span data-ttu-id="58e8f-127">Servidores SIEM com suporte</span><span class="sxs-lookup"><span data-stu-id="58e8f-127">Supported SIEM servers</span></span>

<span data-ttu-id="58e8f-128">O Office 365 Cloud app Security atualmente oferece suporte aos seguintes servidores SIEM:</span><span class="sxs-lookup"><span data-stu-id="58e8f-128">Office 365 Cloud App Security currently supports the following SIEM servers:</span></span>
- <span data-ttu-id="58e8f-129">Micro Focus ArcSight</span><span class="sxs-lookup"><span data-stu-id="58e8f-129">Micro Focus ArcSight</span></span>
- <span data-ttu-id="58e8f-130">CEF genérico</span><span class="sxs-lookup"><span data-stu-id="58e8f-130">Generic CEF</span></span>

### <a name="prerequisites"></a><span data-ttu-id="58e8f-131">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="58e8f-131">Prerequisites</span></span>

- <span data-ttu-id="58e8f-132">Você deve ser um administrador global ou administrador de segurança para executar as tarefas descritas neste artigo.</span><span class="sxs-lookup"><span data-stu-id="58e8f-132">You must be a global administrator or security administrator to perform the tasks described in this article.</span></span> <span data-ttu-id="58e8f-133">Consulte [permissões no centro de conformidade de &amp; segurança do Office 365](permissions-in-the-security-and-compliance-center.md)</span><span class="sxs-lookup"><span data-stu-id="58e8f-133">See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md)</span></span>

- <span data-ttu-id="58e8f-134">Você deve ter o [Office 365 Cloud app Security habilitado](turn-on-office-365-cas.md) para sua organização.</span><span class="sxs-lookup"><span data-stu-id="58e8f-134">You must have [Office 365 Cloud App Security enabled](turn-on-office-365-cas.md) for your organization.</span></span>

- <span data-ttu-id="58e8f-135">O [log de auditoria](turn-audit-log-search-on-or-off.md) deve estar ativado para o Office 365</span><span class="sxs-lookup"><span data-stu-id="58e8f-135">[Audit logging](turn-audit-log-search-on-or-off.md) must be turned on for Office 365</span></span>

- <span data-ttu-id="58e8f-136">Você deve ter um servidor padrão que atenda aos seguintes requisitos para configurar a integração do SIEM Server:</span><span class="sxs-lookup"><span data-stu-id="58e8f-136">You must have a standard server that meets the following requirements in order to configure SIEM server integration:</span></span>
    - <span data-ttu-id="58e8f-137">OS: Windows ou Linux (pode ser uma máquina virtual)</span><span class="sxs-lookup"><span data-stu-id="58e8f-137">OS: Windows or Linux (this can be a virtual machine)</span></span>
    - <span data-ttu-id="58e8f-138">CPU: 2</span><span class="sxs-lookup"><span data-stu-id="58e8f-138">CPU: 2</span></span>
    - <span data-ttu-id="58e8f-139">Espaço em disco: 20 GB</span><span class="sxs-lookup"><span data-stu-id="58e8f-139">Disk space: 20 GB</span></span>
    - <span data-ttu-id="58e8f-140">RAM: 2 GB</span><span class="sxs-lookup"><span data-stu-id="58e8f-140">RAM: 2 GB</span></span>
    - <span data-ttu-id="58e8f-141">[Oracle Java 8](http://www.oracle.com/technetwork/java/javase/downloads/index.html) instalado</span><span class="sxs-lookup"><span data-stu-id="58e8f-141">[Oracle Java 8](http://www.oracle.com/technetwork/java/javase/downloads/index.html) installed</span></span>
    - <span data-ttu-id="58e8f-142">Firewall configurado conforme descrito nos [requisitos de rede](https://docs.microsoft.com/cloud-app-security/network-requirements)</span><span class="sxs-lookup"><span data-stu-id="58e8f-142">Firewall configured as described in [Network requirements](https://docs.microsoft.com/cloud-app-security/network-requirements)</span></span>

- <span data-ttu-id="58e8f-143">Você deve ter detalhes sobre o **host de syslog remoto** e o **número da porta Syslot**.</span><span class="sxs-lookup"><span data-stu-id="58e8f-143">You must have details about your **Remote syslog host** and **Syslot port number**.</span></span> <span data-ttu-id="58e8f-144">Um administrador de rede ou administrador de segurança deve ser capaz de ajudá-lo a localizar essas informações.</span><span class="sxs-lookup"><span data-stu-id="58e8f-144">A network administrator or security administrator should be able to help you locate that information.</span></span> 

- <span data-ttu-id="58e8f-145">Você deve concordar com os [termos de licença de software](https://go.microsoft.com/fwlink/?linkid=862491) para baixar o [arquivo JAR](https://go.microsoft.com/fwlink/?linkid=838596) , você precisará integrar seu servidor Siem.</span><span class="sxs-lookup"><span data-stu-id="58e8f-145">You must agree to [software license terms](https://go.microsoft.com/fwlink/?linkid=862491) to download the [JAR file](https://go.microsoft.com/fwlink/?linkid=838596) you'll need to integrate your SIEM server.</span></span>
 
## <a name="step-1-set-it-up-a-siem-agent-in-office-365-cloud-app-security"></a><span data-ttu-id="58e8f-146">Etapa 1: configurar um agente SIEM no Office 365 Cloud app Security</span><span class="sxs-lookup"><span data-stu-id="58e8f-146">Step 1: Set it up a SIEM agent in Office 365 Cloud App Security</span></span>

1. <span data-ttu-id="58e8f-147">Vá para o portal do Cloud app Security[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)() e entre.</span><span class="sxs-lookup"><span data-stu-id="58e8f-147">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span>
  
2. <span data-ttu-id="58e8f-148">Clique em **configurações** \> de **extensões de segurança**e, em seguida, escolha agentes Siem.</span><span class="sxs-lookup"><span data-stu-id="58e8f-148">Click **Settings** \> **Security extensions**, and then choose SIEM agents.</span></span><br/>
<span data-ttu-id="58e8f-149">![Escolher configurações extensões de segurança >](media/Settings-SecurityExtensions.png)</span><span class="sxs-lookup"><span data-stu-id="58e8f-149">![Choose Settings > Security extensions](media/Settings-SecurityExtensions.png)</span></span>

3. <span data-ttu-id="58e8f-150">Escolha **Adicionar agente Siem**.</span><span class="sxs-lookup"><span data-stu-id="58e8f-150">Choose **Add SIEM agent**.</span></span><br/><span data-ttu-id="58e8f-151">![Escolha Adicionar agente SIEM.](media/SIEMAgents.png)</span><span class="sxs-lookup"><span data-stu-id="58e8f-151">![Choose Add SIEM agent.](media/SIEMAgents.png)</span></span>
    
4. <span data-ttu-id="58e8f-152">Escolha **Iniciar assistente**.</span><span class="sxs-lookup"><span data-stu-id="58e8f-152">Choose **Start wizard**.</span></span><br/><span data-ttu-id="58e8f-153">![Obter ajuda ou iniciar o assistente](media/HelpOrWizard.png)</span><span class="sxs-lookup"><span data-stu-id="58e8f-153">![Get help or start the wizard](media/HelpOrWizard.png)</span></span> 
    
5. <span data-ttu-id="58e8f-154">Na etapa **geral** , especifique um nome e **Selecione seu formato Siem** e defina **as configurações avançadas** que sejam relevantes para esse formato.</span><span class="sxs-lookup"><span data-stu-id="58e8f-154">In the **General** step, specify a name, and **Select your SIEM format** and set any **Advanced settings** that are relevant to that format.</span></span> <span data-ttu-id="58e8f-155">Em seguida, escolha **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="58e8f-155">Then choose **Next**.</span></span><br/><span data-ttu-id="58e8f-156">![Especifique um nome e tipo](media/ChooseAgentTypeAndName.png)</span><span class="sxs-lookup"><span data-stu-id="58e8f-156">![Specify a name and type](media/ChooseAgentTypeAndName.png)</span></span>
    
6. <span data-ttu-id="58e8f-157">Na etapa **syslog remoto** , especifique o endereço IP ou o nome de host do **host syslog remoto** e o **número da porta de syslog**.</span><span class="sxs-lookup"><span data-stu-id="58e8f-157">In the **Remote Syslog** step, specify the IP address or hostname of the **Remote syslog host** and the **Syslog port number**.</span></span> <span data-ttu-id="58e8f-158">Selecione TCP ou UDP como o protocolo de syslog remoto.</span><span class="sxs-lookup"><span data-stu-id="58e8f-158">Select TCP or UDP as the Remote Syslog protocol.</span></span> <span data-ttu-id="58e8f-159">(Você pode trabalhar com seu administrador de rede ou administrador de segurança para obter esses detalhes, caso não os tenha.) Em seguida, escolha **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="58e8f-159">(You can work with your network administrator or security administrator to get these details if you don't have them.) Then choose **Next**.</span></span><br/><span data-ttu-id="58e8f-160">![Especificar detalhes do syslog remoto](media/ArcSightS1Syslog.png)</span><span class="sxs-lookup"><span data-stu-id="58e8f-160">![Specify Remote Syslog details](media/ArcSightS1Syslog.png)</span></span>
  
7. <span data-ttu-id="58e8f-161">Na etapa **tipos de dados** , execute um dos seguintes procedimentos e clique em **Avançar**:</span><span class="sxs-lookup"><span data-stu-id="58e8f-161">In the **Data Types** step, do one of the following, and then click **Next**:</span></span>
    - <span data-ttu-id="58e8f-162">Manter a configuração padrão de **todos os alertas**</span><span class="sxs-lookup"><span data-stu-id="58e8f-162">Keep the default setting of **All Alerts**</span></span><br/><span data-ttu-id="58e8f-163">OU</span><span class="sxs-lookup"><span data-stu-id="58e8f-163">OR</span></span>
    - <span data-ttu-id="58e8f-164">Clique em **todos os alertas**e, em seguida, escolha **filtros específicos**.</span><span class="sxs-lookup"><span data-stu-id="58e8f-164">Click **All alerts**, and then choose **Specific filters**.</span></span> <span data-ttu-id="58e8f-165">Defina filtros para selecionar os tipos de alertas que você deseja enviar ao seu servidor SIEM.</span><span class="sxs-lookup"><span data-stu-id="58e8f-165">Define filters to select the kinds of alerts you want to send to your SIEM server.</span></span>
<br/><span data-ttu-id="58e8f-166">![Etapa tipos de dados do assistente](media/ArcSightS1ExportOptions.png)</span><span class="sxs-lookup"><span data-stu-id="58e8f-166">![Data Types step of the wizard](media/ArcSightS1ExportOptions.png)</span></span>
  
8. <span data-ttu-id="58e8f-167">Na tela Parabéns, copie o token e salve-o para mais tarde.</span><span class="sxs-lookup"><span data-stu-id="58e8f-167">On the Congratulations screen, copy the token and save it for later.</span></span><br/>![Tela criada pelo agente SIEM](media/SIEMAgentFinished.png) 

> [!IMPORTANT]
> <span data-ttu-id="58e8f-169">Neste ponto, você configurou um agente SIEM no Office 365 Cloud app Security, mas sua integração com o servidor do SIEM ainda não foi concluída.</span><span class="sxs-lookup"><span data-stu-id="58e8f-169">At this point, you have set up a SIEM agent in Office 365 Cloud App Security, but your SIEM server integration is not yet finished.</span></span> <span data-ttu-id="58e8f-170">Vá para a próxima etapa para continuar sua integração com o servidor SIEM.</span><span class="sxs-lookup"><span data-stu-id="58e8f-170">Proceed to the next step to continue your SIEM server integration.</span></span>

<span data-ttu-id="58e8f-171">Depois de clicar em fechar e sair do assistente, na tela extensões de segurança, você poderá ver o agente SIEM adicionado na tabela.</span><span class="sxs-lookup"><span data-stu-id="58e8f-171">After you click Close and leave the wizard, on the Security extensions screen, you can see the SIEM agent you added in the table.</span></span> <span data-ttu-id="58e8f-172">Ele mostrará um status de **criado** até que seja conectado mais tarde.</span><span class="sxs-lookup"><span data-stu-id="58e8f-172">It will show a status of **Created** until it's connected later.</span></span>

![Agente SIEM criado](media/SIEMAgentCreated.png)
    
## <a name="step-2-download-a-jar-file-and-run-it-on-your-siem-server"></a><span data-ttu-id="58e8f-174">Etapa 2: baixar um arquivo JAR e executá-lo em seu servidor SIEM</span><span class="sxs-lookup"><span data-stu-id="58e8f-174">Step 2: Download a JAR file and run it on your SIEM server</span></span>

1. <span data-ttu-id="58e8f-175">Baixe o [agente Siem do Microsoft Cloud app Security](https://go.microsoft.com/fwlink/?linkid=838596) e descompacte a pasta.</span><span class="sxs-lookup"><span data-stu-id="58e8f-175">Download the [Microsoft Cloud App Security SIEM Agent](https://go.microsoft.com/fwlink/?linkid=838596) and unzip the folder.</span></span> <span data-ttu-id="58e8f-176">(Você deve concordar com os [termos de licença de software](https://go.microsoft.com/fwlink/?linkid=862491) para continuar.)</span><span class="sxs-lookup"><span data-stu-id="58e8f-176">(You must agree to [software license terms](https://go.microsoft.com/fwlink/?linkid=862491) in order to proceed.)</span></span> 
    
2. <span data-ttu-id="58e8f-177">Extraia o arquivo. jar da pasta zipada e execute-o em seu servidor SIEM.</span><span class="sxs-lookup"><span data-stu-id="58e8f-177">Extract the .jar file from the zipped folder and run it on your SIEM server.</span></span>
    
3. <span data-ttu-id="58e8f-178">Depois de executar o arquivo, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="58e8f-178">After running the file, run the following: command:</span></span><br/>
  ```
  java -jar mcas-siemagent-0.87.20-signed.jar [--logsDirectory DIRNAME] [--proxy ADDRESS[:PORT]] --token TOKEN
  ```
### <a name="important-notes"></a><span data-ttu-id="58e8f-179">Observações importantes</span><span class="sxs-lookup"><span data-stu-id="58e8f-179">Important notes</span></span>

- <span data-ttu-id="58e8f-180">O nome do arquivo pode ser diferente, dependendo da versão do agente SIEM.</span><span class="sxs-lookup"><span data-stu-id="58e8f-180">The file name may differ depending on the version of the SIEM agent.</span></span> 

- <span data-ttu-id="58e8f-181">Recomendamos que você execute o arquivo JAR no seu servidor SIEM durante a configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="58e8f-181">We recommend that you run the JAR file on your SIEM server during server setup.</span></span>

    - <span data-ttu-id="58e8f-182">**Windows**: executar como uma tarefa agendada, certifique-se de configurar a tarefa para **executar se o usuário está conectado ou não** e desmarque a **tarefa parar se ela for executada por mais de** uma opção.</span><span class="sxs-lookup"><span data-stu-id="58e8f-182">**Windows**: Run as a scheduled task, making sure to configure the task to **Run whether the user is logged on or not** and clear the **Stop the task if it runs longer than** option.</span></span>

    - <span data-ttu-id="58e8f-183">**Linux**: Adicione o comando executar com um **&** para o `rc.local` arquivo.</span><span class="sxs-lookup"><span data-stu-id="58e8f-183">**Linux**: Add the run command with an **&** to the `rc.local` file.</span></span> <br/><span data-ttu-id="58e8f-184">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="58e8f-184">Example:</span></span><br/> 
    ```
    java -jar mcas-siemagent-0.87.20-signed.jar [--logsDirectory DIRNAME] [--proxy ADDRESS[:PORT]] --token TOKEN &
    ```

- <span data-ttu-id="58e8f-185">Os parâmetros entre colchetes [] são opcionais e devem ser usados apenas se relevante.</span><span class="sxs-lookup"><span data-stu-id="58e8f-185">Parameters in brackets [] are optional, and should be used only if relevant.</span></span> <span data-ttu-id="58e8f-186">Use as seguintes variáveis:</span><span class="sxs-lookup"><span data-stu-id="58e8f-186">Use the following variables:</span></span>

    - <span data-ttu-id="58e8f-187">**DIRNAME** é o caminho para o diretório que você deseja usar para logs de depuração do agente local.</span><span class="sxs-lookup"><span data-stu-id="58e8f-187">**DIRNAME** is the path to the directory you want to use for local agent debug logs.</span></span>

    - <span data-ttu-id="58e8f-188">**Endereço [:P ORT]** é o endereço do servidor proxy e a porta que o servidor usa para se conectar à Internet.</span><span class="sxs-lookup"><span data-stu-id="58e8f-188">**ADDRESS[:PORT]** is the proxy server address and port that the server uses to connect to the Internet.</span></span>

    - <span data-ttu-id="58e8f-189">**Token** é o token do agente Siem que você copiou no primeiro procedimento.</span><span class="sxs-lookup"><span data-stu-id="58e8f-189">**TOKEN** is the SIEM agent token you copied in the first procedure.</span></span>

    - <span data-ttu-id="58e8f-190">Para obter ajuda, digite `-h`.</span><span class="sxs-lookup"><span data-stu-id="58e8f-190">To get help, type `-h`.</span></span> 
  
## <a name="step-3-validate-that-the-siem-agent-is-working"></a><span data-ttu-id="58e8f-191">Etapa 3: validar que o agente SIEM está funcionando</span><span class="sxs-lookup"><span data-stu-id="58e8f-191">Step 3: Validate that the SIEM agent is working</span></span>

1. <span data-ttu-id="58e8f-192">Certifique-se de que o status do agente SIEM no portal do Office 365 Cloud app Security não seja exibido como **erro de conexão** ou desconectado e que não haja nenhuma notificação de agente. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="58e8f-192">Make sure the status of the SIEM agent in the Office 365 Cloud App Security portal is not displayed as **Connection error** or **Disconnected** and that there are no agent notifications.</span></span><br/><span data-ttu-id="58e8f-193">Por exemplo, é possível ver aqui que o servidor SIEM está conectado:</span><span class="sxs-lookup"><span data-stu-id="58e8f-193">For example, here we can see the SIEM server is connected:</span></span><br/><span data-ttu-id="58e8f-194">![Servidor SIEM conectado](media/siem-connected.png)</span><span class="sxs-lookup"><span data-stu-id="58e8f-194">![SIEM server connected](media/siem-connected.png)</span></span><br/><span data-ttu-id="58e8f-195">E aqui, podemos ver que o servidor SIEM está desconectado:</span><span class="sxs-lookup"><span data-stu-id="58e8f-195">And here, we can see the SIEM server is disconnected:</span></span><br/><span data-ttu-id="58e8f-196">![Servidor SIEM não conectado](media/siem-not-connected.png)</span><span class="sxs-lookup"><span data-stu-id="58e8f-196">![SIEM server not connected](media/siem-not-connected.png)</span></span> 
  
2. <span data-ttu-id="58e8f-197">Em seu servidor de syslog/SIEM, verifique se os alertas chegaram no Office 365 Cloud app Security.</span><span class="sxs-lookup"><span data-stu-id="58e8f-197">In your Syslog/SIEM server, make sure you see that alerts have arrived from Office 365 Cloud App Security.</span></span>
  
## <a name="what-the-logfiles-look-like"></a><span data-ttu-id="58e8f-198">Como os logfiles se parecem</span><span class="sxs-lookup"><span data-stu-id="58e8f-198">What the logfiles look like</span></span>

<span data-ttu-id="58e8f-199">Veja um exemplo de Logfile de alerta que pode ser enviado para um servidor SIEM:</span><span class="sxs-lookup"><span data-stu-id="58e8f-199">Here's an alerts logfile example that might be sent to a SIEM server:</span></span>

```
2017-07-15T20:42:30.531Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|myPolicy|3|externalId=596a7e360c204203a335a3fb start=1500151350531 end=1500151350531 msg=Activity policy ''myPolicy'' was triggered by ''admin@box-contoso.com'' suser=admin@box-contoso.com destinationServiceName=Box cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596a7e360c204203a335a3fb cs2Label=uniqueServiceAppIds cs2=APPID_BOX cs3Label=relatedAudits cs3=1500151288183_acc891bf-33e1-424b-a021-0d4370789660 cs4Label=policyIDs cs4=59f0ab82f797fa0681e9b1c7

2017-07-16T09:36:26.550Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy|3|externalId=596b339b0c204203a33a51ae start=1500197786550 end=1500197786550 msg=Activity policy ''test-activity-policy'' was triggered by ''user@contoso.com'' suser=user@contoso.com destinationServiceName=Salesforce cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b339b0c204203a33a51ae cs2Label=uniqueServiceAppIds cs2=APPID_SALESFORCE cs3Label=relatedAudits cs3=1500197720691_b7f6317c-b8de-476a-bc8f-dfa570e00349 cs4Label=policyIDs cs4=

2017-07-16T09:17:03.361Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy3|3|externalId=596b2fd70c204203a33a3eeb start=1500196623361 end=1500196623361 msg=Activity policy ''test-activity-policy3'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Office 365 cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b2fd70c204203a33a3eeb cs2Label=uniqueServiceAppIds cs2=APPID_O365 cs3Label=relatedAudits cs3=1500196549157_a0e01f8a-e29a-43ae-8599-783c1c11597d cs4Label=policyIDs cs4=

2017-07-16T09:17:15.426Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy|3|externalId=596b2fd70c204203a33a3eec start=1500196635426 end=1500196635426 msg=Activity policy ''test-activity-policy'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Microsoft Office 365 admin center cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b2fd70c204203a33a3eec cs2Label=uniqueServiceAppIds cs2=APPID_O365_PORTAL cs3Label=relatedAudits cs3=1500196557398_3e102b20-d9fa-4f66-b550-8c7a403bb4d8 cs4Label=policyIDs cs4=59f0ab35f797fa9811e9b1c7

2017-07-16T09:17:46.290Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy4|3|externalId=596b30200c204203a33a4765 start=1500196666290 end=1500196666290 msg=Activity policy ''test-activity-policy4'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Microsoft Exchange Online cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b30200c204203a33a4765 cs2Label=uniqueServiceAppIds cs2=APPID_OUTLOOK cs3Label=relatedAudits cs3=1500196587034_a8673602-7e95-46d6-a1fe-c156c4709c5d cs4Label=policyIDs cs4=

2017-07-16T09:41:04.369Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy2|3|externalId=596b34b10c204203a33a5240 start=1500198064369 end=1500198064369 msg=Activity policy ''test-activity-policy2'' was triggered by ''user2@test15-adallom.com'' suser=user2@test15-adallom.com destinationServiceName=Google cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b34b10c204203a33a5240 cs2Label=uniqueServiceAppIds cs2=APPID_33626 cs3Label=relatedAudits cs3=1500197996117_fd71f265-1e46-4f04-b372-2e32ec874cd3 cs4Label=policyIDs cs4=
```

<span data-ttu-id="58e8f-200">E aqui está outro exemplo, desta vez no formato CEF:</span><span class="sxs-lookup"><span data-stu-id="58e8f-200">And here's another sample, this time in CEF format:</span></span>


|<span data-ttu-id="58e8f-201">Nome do campo CEF</span><span class="sxs-lookup"><span data-stu-id="58e8f-201">CEF field name</span></span>  | <span data-ttu-id="58e8f-202">Descrição</span><span class="sxs-lookup"><span data-stu-id="58e8f-202">Description</span></span>  |
|---------|---------|
|<span data-ttu-id="58e8f-203">iniciar</span><span class="sxs-lookup"><span data-stu-id="58e8f-203">start</span></span>     | <span data-ttu-id="58e8f-204">carimbo de hora do alerta</span><span class="sxs-lookup"><span data-stu-id="58e8f-204">alert timestamp</span></span>        |
|<span data-ttu-id="58e8f-205">end</span><span class="sxs-lookup"><span data-stu-id="58e8f-205">end</span></span>     | <span data-ttu-id="58e8f-206">carimbo de hora do alerta</span><span class="sxs-lookup"><span data-stu-id="58e8f-206">alert timestamp</span></span>        |
|<span data-ttu-id="58e8f-207">RT</span><span class="sxs-lookup"><span data-stu-id="58e8f-207">rt</span></span>     | <span data-ttu-id="58e8f-208">carimbo de hora do alerta</span><span class="sxs-lookup"><span data-stu-id="58e8f-208">alert timestamp</span></span>        |
|<span data-ttu-id="58e8f-209">MSG</span><span class="sxs-lookup"><span data-stu-id="58e8f-209">msg</span></span>     | <span data-ttu-id="58e8f-210">Descrição de alerta conforme mostrado no portal do Office 365 Cloud app Security</span><span class="sxs-lookup"><span data-stu-id="58e8f-210">alert description as shown in the Office 365 Cloud App Security portal</span></span>        |
|<span data-ttu-id="58e8f-211">suser</span><span class="sxs-lookup"><span data-stu-id="58e8f-211">suser</span></span>     | <span data-ttu-id="58e8f-212">alerta de usuário de requerente</span><span class="sxs-lookup"><span data-stu-id="58e8f-212">alert subject user</span></span>        |
|<span data-ttu-id="58e8f-213">destinationServiceName</span><span class="sxs-lookup"><span data-stu-id="58e8f-213">destinationServiceName</span></span>     | <span data-ttu-id="58e8f-214">alerta o aplicativo de origem, como o Office 365, SharePoint ou OneDrive</span><span class="sxs-lookup"><span data-stu-id="58e8f-214">alert originating app, such as Office 365, SharePoint, or OneDrive</span></span>        |
|<span data-ttu-id="58e8f-215">csLabel</span><span class="sxs-lookup"><span data-stu-id="58e8f-215">csLabel</span></span>     | <span data-ttu-id="58e8f-216">Varia (os rótulos têm significados diferentes).</span><span class="sxs-lookup"><span data-stu-id="58e8f-216">Varies (labels have different meanings).</span></span> <span data-ttu-id="58e8f-217">Normalmente, os rótulos são auto-explicativos, como targetObjects.</span><span class="sxs-lookup"><span data-stu-id="58e8f-217">Typically, labels are self-explanatory, like targetObjects.</span></span>        |
|<span data-ttu-id="58e8f-218">cs</span><span class="sxs-lookup"><span data-stu-id="58e8f-218">cs</span></span>     | <span data-ttu-id="58e8f-219">Informações correspondentes a um rótulo (como o usuário de destino de um alerta, conforme o exemplo de rótulo)</span><span class="sxs-lookup"><span data-stu-id="58e8f-219">Information corresponding to a label (such as the target user of an alert as per the label example)</span></span>        |

## <a name="additional-tasks-as-needed"></a><span data-ttu-id="58e8f-220">Tarefas adicionais (conforme necessário)</span><span class="sxs-lookup"><span data-stu-id="58e8f-220">Additional tasks (as needed)</span></span>

<span data-ttu-id="58e8f-221">Depois de configurar seu servidor SIEM e integrado ao Office 365 Cloud app Security, talvez seja necessário gerar um token novamente, editar um agente SIEM ou excluir um agente SIEM.</span><span class="sxs-lookup"><span data-stu-id="58e8f-221">After you have configured your SIEM server and have integrated it with Office 365 Cloud App Security, you might need to regenerate a token, edit a SIEM agent, or delete a SIEM agent.</span></span> <span data-ttu-id="58e8f-222">As seções a seguir descrevem como realizar essas tarefas.</span><span class="sxs-lookup"><span data-stu-id="58e8f-222">The following sections describe how to perform these tasks.</span></span>

### <a name="regenerate-a-token"></a><span data-ttu-id="58e8f-223">Regenerar um token</span><span class="sxs-lookup"><span data-stu-id="58e8f-223">Regenerate a token</span></span>

<span data-ttu-id="58e8f-224">Se você perder o token, poderá regenerar um.</span><span class="sxs-lookup"><span data-stu-id="58e8f-224">If you lose your token, you can regenerate one.</span></span> 

1. <span data-ttu-id="58e8f-225">no portal do Office 365 Cloud App security ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)), escolha **configurações** > e**extensões de segurança**.</span><span class="sxs-lookup"><span data-stu-id="58e8f-225">In the Office 365 Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)), choose **Settings** > **Security extensions**.</span></span>

2. <span data-ttu-id="58e8f-226">Na tabela, localize a linha do agente SIEM.</span><span class="sxs-lookup"><span data-stu-id="58e8f-226">In the table, locate the row for the SIEM agent.</span></span> 

3. <span data-ttu-id="58e8f-227">Clique nas reticências e, em seguida, escolha **regenerar token**.</span><span class="sxs-lookup"><span data-stu-id="58e8f-227">Click the ellipses, and then choose **Regenerate token**.</span></span><br/><span data-ttu-id="58e8f-228">![Regenerar um token clicando nas reticências do seu agente do SIEM](media/04de368a-b88e-4a9c-a830-58025cb98db6.png)</span><span class="sxs-lookup"><span data-stu-id="58e8f-228">![Regenerate a token by clicking the ellipsis for your SIEM agent](media/04de368a-b88e-4a9c-a830-58025cb98db6.png)</span></span>
  
### <a name="edit-a-siem-agent"></a><span data-ttu-id="58e8f-229">Editar um agente SIEM</span><span class="sxs-lookup"><span data-stu-id="58e8f-229">Edit a SIEM agent</span></span>

1. <span data-ttu-id="58e8f-230">no portal do Office 365 Cloud App security ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)), escolha **configurações** > e**extensões de segurança**.</span><span class="sxs-lookup"><span data-stu-id="58e8f-230">In the Office 365 Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)), choose **Settings** > **Security extensions**.</span></span>

2. <span data-ttu-id="58e8f-231">Localize a linha do agente SIEM.</span><span class="sxs-lookup"><span data-stu-id="58e8f-231">Locate the row for the SIEM agent.</span></span> 

3. <span data-ttu-id="58e8f-232">Clique nas reticências e, em seguida, escolha **Editar**.</span><span class="sxs-lookup"><span data-stu-id="58e8f-232">Click the ellipses, and then choose **Edit**.</span></span> <span data-ttu-id="58e8f-233">(Se você editar o agente SIEM, não será necessário executar novamente o arquivo. jar; ele é atualizado automaticamente.)</span><span class="sxs-lookup"><span data-stu-id="58e8f-233">(If you edit the SIEM agent, you do not need to re-run the .jar file; it updates automatically.)</span></span> <br/><span data-ttu-id="58e8f-234">![Para editar seu agente SIEM, escolha as reticências e, em seguida, escolha Editar.](media/96d0b362-3e0c-4dff-b2b4-d7af5b1bfb91.png)</span><span class="sxs-lookup"><span data-stu-id="58e8f-234">![To edit your SIEM agent, choose the ellipses, and then choose Edit.](media/96d0b362-3e0c-4dff-b2b4-d7af5b1bfb91.png)</span></span>
  
### <a name="delete-a-siem-agent"></a><span data-ttu-id="58e8f-235">Excluir um agente SIEM</span><span class="sxs-lookup"><span data-stu-id="58e8f-235">Delete a SIEM agent</span></span>

1. <span data-ttu-id="58e8f-236">no portal do Office 365 Cloud App security ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)), escolha **configurações** > e**extensões de segurança**.</span><span class="sxs-lookup"><span data-stu-id="58e8f-236">In the Office 365 Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)), choose **Settings** > **Security extensions**.</span></span>

2. <span data-ttu-id="58e8f-237">Localize a linha do agente SIEM.</span><span class="sxs-lookup"><span data-stu-id="58e8f-237">Locate the row for the SIEM agent.</span></span> 

3. <span data-ttu-id="58e8f-238">Clique nas reticências e escolha **excluir**.</span><span class="sxs-lookup"><span data-stu-id="58e8f-238">Click the ellipses, and then choose **Delete**.</span></span><br/><span data-ttu-id="58e8f-239">![Para excluir um agente SIEM, escolha as reticências e, em seguida, escolha Excluir.](media/540b5bdf-5574-4ecc-a7b0-92a499a387d7.png)</span><span class="sxs-lookup"><span data-stu-id="58e8f-239">![To delete a SIEM agent, choose the ellipses, and then choose Delete.](media/540b5bdf-5574-4ecc-a7b0-92a499a387d7.png)</span></span>

  
## <a name="next-steps"></a><span data-ttu-id="58e8f-240">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="58e8f-240">Next steps</span></span>

- [<span data-ttu-id="58e8f-241">Atividades de utilização após a implantação do Office 365 Cloud app Security</span><span class="sxs-lookup"><span data-stu-id="58e8f-241">Utilization activities after rolling out Office 365 Cloud App Security</span></span>](utilization-activities-for-ocas.md)
    
- [<span data-ttu-id="58e8f-242">ReVisar e executar ação em alertas</span><span class="sxs-lookup"><span data-stu-id="58e8f-242">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="58e8f-243">Agrupar seus endereços IP para simplificar o gerenciamento</span><span class="sxs-lookup"><span data-stu-id="58e8f-243">Group your IP addresses to simplify management</span></span>](group-your-ip-addresses-in-ocas.md)
    


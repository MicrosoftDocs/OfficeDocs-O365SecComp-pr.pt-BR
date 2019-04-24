---
title: Configurar o IRM para usar um servidor RMS do AD local
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 12/13/2017
ms.audience: End User
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 3ecde857-4b7c-451d-b4aa-9eeffc8a8c61
ms.collection:
- M365-security-compliance
description: Este tópico mostra como configurar o IRM para usar um servidor AD RMS.
ms.openlocfilehash: 1da66c5afa37c96c061a4bf25c0858e4e71e2313
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32259569"
---
# <a name="configure-irm-to-use-an-on-premises-ad-rms-server"></a><span data-ttu-id="aaa2a-103">Configurar o IRM para usar um servidor RMS do AD local</span><span class="sxs-lookup"><span data-stu-id="aaa2a-103">Configure IRM to use an on-premises AD RMS server</span></span>
  
<span data-ttu-id="aaa2a-104">Para uso com implantações locais, o gerenciamento de direitos de informação (IRM) no Exchange Online usa o Active Directory Rights Management Services (AD RMS), uma tecnologia de proteção de informações no Windows Server 2008 e posteriores.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-104">For use with on-premises deployments, Information Rights Management (IRM) in Exchange Online uses Active Directory Rights Management Services (AD RMS), an information protection technology in Windows Server 2008 and later.</span></span> <span data-ttu-id="aaa2a-105">A proteção do IRM é aplicada ao email por meio da aplicação de um modelo de política de direitos do AD RMS a uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-105">IRM protection is applied to email by applying an AD RMS rights policy template to an email message.</span></span> <span data-ttu-id="aaa2a-106">Os direitos são anexados à própria mensagem para que a proteção ocorra online e offline e dentro e fora do firewall da sua organização.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-106">Rights are attached to the message itself so that protection occurs online and offline and inside and outside of your organization's firewall.</span></span>
  
<span data-ttu-id="aaa2a-107">Este tópico mostra como configurar o IRM para usar um servidor AD RMS.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-107">This topic shows you how to configure IRM to use an AD RMS server.</span></span> <span data-ttu-id="aaa2a-108">Para obter informações sobre como usar os novos recursos para a criptografia de mensagem do Office 365 com o Azure Active Directory e o Azure Rights Management, consulte as [perguntas frequentes sobre a criptografia de mensagens do office 365](https://support.office.com/article/0432dce9-d9b6-4e73-8a13-4a932eb0081e).</span><span class="sxs-lookup"><span data-stu-id="aaa2a-108">For information about using the new capabilities for Office 365 Message Encryption with Azure Active Directory and Azure Rights Management, see the [Office 365 Message Encryption FAQ](https://support.office.com/article/0432dce9-d9b6-4e73-8a13-4a932eb0081e).</span></span>
  
<span data-ttu-id="aaa2a-109">Para saber mais sobre IRM no Exchange Online, consulte [Gerenciamento de Direitos de Informação no Exchange Online](information-rights-management-in-exchange-online.md).</span><span class="sxs-lookup"><span data-stu-id="aaa2a-109">To learn more about IRM in Exchange Online, see [Information Rights Management in Exchange Online](information-rights-management-in-exchange-online.md).</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="aaa2a-110">O que você precisa saber antes de começar?</span><span class="sxs-lookup"><span data-stu-id="aaa2a-110">What do you need to know before you begin?</span></span>
<span data-ttu-id="aaa2a-111"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="aaa2a-111"></span></span>

- <span data-ttu-id="aaa2a-112">Tempo estimado para a conclusão da tarefa: 30 minutos</span><span class="sxs-lookup"><span data-stu-id="aaa2a-112">Estimated time to complete this task: 30 minutes</span></span>
    
- <span data-ttu-id="aaa2a-p103">Para executar este procedimento ou estes procedimentos, você precisa receber permissões. Para ver de que permissões você precisa, consulte o Entrada "Gerenciamento de Direitos de Informação " no tópico [Messaging policy and compliance permissions](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx).</span><span class="sxs-lookup"><span data-stu-id="aaa2a-p103">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Information Rights Management" entry in the [Messaging policy and compliance permissions](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) topic.</span></span> 
    
- <span data-ttu-id="aaa2a-p104">O servidor AD RMS deve estar executando o Windows Server 2008 ou posterior. Para obter informações sobre como implantar o AD RMS, consulte [Instalando um cluster do AD RMS](https://go.microsoft.com/fwlink/?LinkId=210873).</span><span class="sxs-lookup"><span data-stu-id="aaa2a-p104">The AD RMS server must be running Windows Server 2008 or later. For details about how to deploy AD RMS, see [Installing an AD RMS Cluster](https://go.microsoft.com/fwlink/?LinkId=210873).</span></span>
    
- <span data-ttu-id="aaa2a-117">Para obter detalhes sobre como instalar e configurar o Windows PowerShell e se conectar ao serviço, consulte [Conectar-se ao Exchange Online usando o PowerShell Remoto](http://technet.microsoft.com/library/c8bea338-6c1a-4bdf-8de0-7895d427ee5b.aspx).</span><span class="sxs-lookup"><span data-stu-id="aaa2a-117">For details about how to install and configure Windows PowerShell and connect to the service, see [Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/c8bea338-6c1a-4bdf-8de0-7895d427ee5b.aspx).</span></span>
    
- <span data-ttu-id="aaa2a-118">Para informações sobre atalhos de teclado que possam se aplicar aos procedimentos neste tópico, consulte **Keyboard shortcuts in Exchange 2013**.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-118">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
    
> [!TIP]
> <span data-ttu-id="aaa2a-p105">Está enfrentando problemas? Peça ajuda nos fóruns do Exchange. Visite os fóruns em: [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), ou [Proteção do Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=285351).</span><span class="sxs-lookup"><span data-stu-id="aaa2a-p105">Having problems? Ask for help in the Exchange forums. Visit the forums at [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), or [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351).</span></span> 
  
## <a name="how-do-you-do-this"></a><span data-ttu-id="aaa2a-122">Como fazer isso?</span><span class="sxs-lookup"><span data-stu-id="aaa2a-122">How do you do this?</span></span>
<span data-ttu-id="aaa2a-123"><a name="sectionSection1"> </a></span><span class="sxs-lookup"><span data-stu-id="aaa2a-123"></span></span>

### <a name="step-1-use-the-ad-rms-console-to-export-a-trusted-publishing-domain-tpd-from-an-ad-rms-server"></a><span data-ttu-id="aaa2a-124">Etapa 1: Use o console do AD RMS para exportar um domínio de publicação confiável (TPD) de um servidor AD RMS</span><span class="sxs-lookup"><span data-stu-id="aaa2a-124">Step 1: Use the AD RMS console to export a trusted publishing domain (TPD) from an AD RMS server</span></span>

<span data-ttu-id="aaa2a-p106">A primeira etapa é exportar um TPD (domínio de publicação confiável) do servidor AD RMS local para um arquivo XML. O TPD contém as seguintes configurações necessárias para usar recursos do RMS:</span><span class="sxs-lookup"><span data-stu-id="aaa2a-p106">The first step is to export a trusted publishing domain (TPD) from the on-premises AD RMS server to an XML file. The TPD contains the following settings needed to use RMS features:</span></span> 
  
- <span data-ttu-id="aaa2a-127">O certificado de licenciador de servidor (SLC) usado para assinatura e criptografia de certificados e licenças</span><span class="sxs-lookup"><span data-stu-id="aaa2a-127">The server licensor certificate (SLC) used for signing and encrypting certificates and licenses</span></span>
    
- <span data-ttu-id="aaa2a-128">As URLs usadas para licenciamento e publicação</span><span class="sxs-lookup"><span data-stu-id="aaa2a-128">The URLs used for licensing and publishing</span></span>
    
- <span data-ttu-id="aaa2a-129">Os modelos de política de direitos do AD RMS que foram criados com o SLC específico para esse TPD</span><span class="sxs-lookup"><span data-stu-id="aaa2a-129">The AD RMS rights policy templates that were created with the specific SLC for that TPD</span></span>
    
<span data-ttu-id="aaa2a-130">Ao importar o TPD, ele é armazenado e protegido no Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-130">When you import the TPD, it's stored and protected in Exchange Online.</span></span>
  
1. <span data-ttu-id="aaa2a-131">Abra o console do Active Directory Rights Management Services e expanda o cluster do AD RMS.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-131">Open the Active Directory Rights Management Services console, and then expand the AD RMS cluster.</span></span>
    
2. <span data-ttu-id="aaa2a-132">Na árvore de console, expanda **Políticas de Confiança** e clique em **Domínios de Publicação Confiáveis**.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-132">In the console tree, expand **Trust Policies**, and then click **Trusted Publishing Domains**.</span></span>
    
3. <span data-ttu-id="aaa2a-133">No painel de resultados, selecione o certificado para o domínio que você deseja exportar.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-133">In the results pane, select the certificate for the domain you want to export.</span></span>
    
4. <span data-ttu-id="aaa2a-134">No painel **Ações**, clique em **Exportar Domínio de Publicação Confiável**.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-134">In the **Actions** pane, click **Export Trusted Publishing Domain**.</span></span>
    
5. <span data-ttu-id="aaa2a-p107">Na caixa **Arquivo de domínio de publicação**, clique em **Salvar como** para salvar o arquivo em um local específico no computador local. Digite um nome de arquivo e certifique-se de especificar a extensão do nome de arquivo  `.xml` e clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-p107">In the **Publishing domain file** box, click **Save As** to save the file to a specific location on the local computer. Type a file name, making sure to specify the  `.xml` file name extension, and then click **Save**.</span></span>
    
6. <span data-ttu-id="aaa2a-p108">Nas caixas **Senha** e **Confirmar Senha**, digite uma senha segura que será usada para criptografar o arquivo de domínio de publicação confiável. Você terá de especificar essa senha quando importar o TPD para a sua organização de email baseada em nuvem.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-p108">In the **Password** and **Confirm Password** boxes, type a strong password that will be used to encrypt the trusted publishing domain file. You will have to specify this password when you import the TPD to your cloud-based email organization.</span></span> 
    
### <a name="step-2-use-the-exchange-management-shell-to-import-the-tpd-to-exchange-online"></a><span data-ttu-id="aaa2a-139">Etapa 2: usar o Shell de gerenciamento do Exchange para importar o TPD para o Exchange Online</span><span class="sxs-lookup"><span data-stu-id="aaa2a-139">Step 2: Use the Exchange Management Shell to import the TPD to Exchange Online</span></span>

<span data-ttu-id="aaa2a-p109">Depois de exportar o TPD para um arquivo XML, você terá de importá-lo para o Exchange Online. Quando um TPD é importado, os modelos do AD RMS da sua organização também são importados. Quando o primeiro TPD é importado, ele se torna o TPD padrão para sua organização baseada em nuvem. Se você importar outro TPD, poderá usar o botão **Padrão** para torná-lo o TPD padrão que está disponível para os usuários.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-p109">After the TPD is exported to an XML file, you have to import it to Exchange Online. When a TPD is imported, your organization's AD RMS templates are also imported. When the first TPD is imported, it becomes the default TPD for your cloud-based organization. If you import another TPD, you can use the **Default** switch to make it the default TPD that is available to users.</span></span> 
  
<span data-ttu-id="aaa2a-144">Para importar o TPD, execute o seguinte comando no Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="aaa2a-144">To import the TPD, run the following command in Windows PowerShell:</span></span>
  
```
Import-RMSTrustedPublishingDomain -FileData $([byte[]](Get-Content -Encoding byte -Path <path to exported TPD file> -ReadCount 0)) -Name "<name of TPD>" -ExtranetLicensingUrl <URL> -IntranetLicensingUrl <URL>
```

<span data-ttu-id="aaa2a-p110">Você pode obter os valores para os parâmetros  _ExtranetLicensingUrl_ e  _IntranetLicensingUrl_ no console do Active Directory Rights Management Services. Selecione o cluster do AD RMS na árvore do console. As URLs de licenciamento são exibidas no painel de resultados. Essas URLs são usadas por clientes de email quando o conteúdo deve ser descriptografado e quando o Exchange Online precisa determinar qual TPD usar.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-p110">You can obtain the values for the  _ExtranetLicensingUrl_ and  _IntranetLicensingUrl_ parameters in the Active Directory Rights Management Services console. Select the AD RMS cluster in the console tree. The licensing URLs are displayed in the results pane. These URLs are used by email clients when content has to be decrypted and when Exchange Online needs to determine which TPD to use.</span></span> 
  
<span data-ttu-id="aaa2a-p111">Ao executar esse comando, será solicitado que você insira uma senha. Digite a senha especificada quando você exportou o TPD do seu servidor AD RMS.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-p111">When you run this command, you'll be prompted for a password. Enter the password that you specified when you exported the TPD from your AD RMS server.</span></span>
  
<span data-ttu-id="aaa2a-p112">Por exemplo, o comando a seguir importa o TPD, denominado TPD exportado, usando o arquivo XML exportado do seu servidor AD RMS e salvo na área de trabalho da conta Administrador. O parâmetro Name é usado para especificar um nome para o TPD.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-p112">For example, the following command imports the TPD named Exported TPD using the XML file that you exported from your AD RMS server and saved to the desktop of the Administrator account. The Name parameter is used to specify a name to the TPD.</span></span>
  
```
Import-RMSTrustedPublishingDomain -FileData $([byte[]](Get-Content -Encoding byte -Path C:\Users\Administrator\Desktop\ExportTPD.xml -ReadCount 0)) -Name "Exported TPD" -ExtranetLicensingUrl https://corp.contoso.com/_wmcs/licensing -IntranetLicensingUrl https://rmsserver/_wmcs/licensing
```

<span data-ttu-id="aaa2a-153">Para obter informações detalhadas de sintaxes e parâmetros, consulte [Import-RMSTrustedPublishingDomain](http://technet.microsoft.com/library/7c5e7a0f-9c9d-4863-bab8-bcc729cc16a6.aspx).</span><span class="sxs-lookup"><span data-stu-id="aaa2a-153">For detailed syntax and parameter information, see [Import-RMSTrustedPublishingDomain](http://technet.microsoft.com/library/7c5e7a0f-9c9d-4863-bab8-bcc729cc16a6.aspx).</span></span>
  
#### <a name="how-do-you-know-this-step-worked"></a><span data-ttu-id="aaa2a-154">Como saber se esta etapa funcionou?</span><span class="sxs-lookup"><span data-stu-id="aaa2a-154">How do you know this step worked?</span></span>

<span data-ttu-id="aaa2a-p113">Para verificar se você importou com êxito o TPD, execute o cmdlet **Get-RMSTrustedPublishingDomain** para recuperar TPDs em sua organização do Exchange Online. Para obter detalhes, consulte os exemplos no [Get-RMSTrustedPublishingDomain](http://technet.microsoft.com/library/69499195-f08f-41bd-b0ed-443688410b12.aspx).</span><span class="sxs-lookup"><span data-stu-id="aaa2a-p113">To verify that you have successfully imported the TPD, run the **Get-RMSTrustedPublishingDomain** cmdlet to retrieve TPDs in your Exchange Online organization. For details, see the examples in [Get-RMSTrustedPublishingDomain](http://technet.microsoft.com/library/69499195-f08f-41bd-b0ed-443688410b12.aspx).</span></span>
  
### <a name="step-3-use-the-exchange-management-shell-to-distribute-an-ad-rms-rights-policy-template"></a><span data-ttu-id="aaa2a-157">Etapa 3: usar o Shell de gerenciamento do Exchange para distribuir um modelo de política de direitos do AD RMS</span><span class="sxs-lookup"><span data-stu-id="aaa2a-157">Step 3: Use the Exchange Management Shell to distribute an AD RMS rights policy template</span></span>

<span data-ttu-id="aaa2a-158">Depois de importar o TPD, você deverá garantir que um modelo de política de direitos do AD RMS seja distribuído.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-158">After you import the TPD, you must make sure an AD RMS rights policy template is distributed.</span></span> <span data-ttu-id="aaa2a-159">Um modelo distribuído é visível para os usuários do Outlook na Web (anteriormente conhecido como Outlook Web App), que podem aplicar os modelos a uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-159">A distributed template is visible to Outlook on the web (formerly known as Outlook Web App) users, who can then apply the templates to an email message.</span></span>
  
<span data-ttu-id="aaa2a-160">Para retornar uma lista de todos os modelos contidos no TPD padrão, execute este comando:</span><span class="sxs-lookup"><span data-stu-id="aaa2a-160">To return a list of all templates contained in the default TPD, run the following command:</span></span>
  
```
Get-RMSTemplate -Type All | fl
```

<span data-ttu-id="aaa2a-161">Se o valor do parâmetro  _Type_ for  `Archived`, o modelo não ficará visível para os usuários.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-161">If the value of the  _Type_ parameter is  `Archived`, the template isn't visible to users.</span></span> <span data-ttu-id="aaa2a-162">Somente os modelos distribuídos no TPD padrão estão disponíveis no Outlook na Web.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-162">Only distributed templates in the default TPD are available in Outlook on the web.</span></span>
  
<span data-ttu-id="aaa2a-163">Para distribuir um modelo, execute este comando:</span><span class="sxs-lookup"><span data-stu-id="aaa2a-163">To distribute a template, run the following command:</span></span>
  
```
Set-RMSTemplate -Identity "<name of the template>" -Type Distributed
```

<span data-ttu-id="aaa2a-164">Por exemplo, o comando a seguir importa o modelo Confidencial da Empresa.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-164">For example, the following command imports the Company Confidential template.</span></span>
  
```
Set-RMSTemplate -Identity "Company Confidential" -Type Distributed
```

<span data-ttu-id="aaa2a-165">Para obter informações detalhadas sobre sintaxe e parâmetros, consulte [Get-RMSTemplate](http://technet.microsoft.com/library/4a5066e8-b770-4aa2-b464-0d2190914f71.aspx) e [Set-RMSTemplate](http://technet.microsoft.com/library/4637f6b8-751a-4f5e-8869-428250230382.aspx).</span><span class="sxs-lookup"><span data-stu-id="aaa2a-165">For detailed syntax and parameter information, see [Get-RMSTemplate](http://technet.microsoft.com/library/4a5066e8-b770-4aa2-b464-0d2190914f71.aspx) and [Set-RMSTemplate](http://technet.microsoft.com/library/4637f6b8-751a-4f5e-8869-428250230382.aspx).</span></span>
  
 <span data-ttu-id="aaa2a-166">**O modelo Não Encaminhar**</span><span class="sxs-lookup"><span data-stu-id="aaa2a-166">**The Do Not Forward template**</span></span>
  
<span data-ttu-id="aaa2a-p116">Ao importar o TPD padrão da sua organização local para o Exchange Online, um modelo de política de direitos do AD RMS chamado **Não Encaminhar** será importado. Por padrão, esse modelo é distribuído quando você importa o TPD padrão. Não é possível usar o cmdlet **Set-RMSTemplate** para modificar o modelo **Não Encaminhar**.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-p116">When you import the default TPD from your on-premises organization into Exchange Online, one AD RMS rights policy template named **Do Not Forward** is imported. By default, this template is distributed when you import the default TPD. You can't use the **Set-RMSTemplate** cmdlet to modify the **Do Not Forward** template.</span></span> 
  
<span data-ttu-id="aaa2a-p117">Quando o modelo **Não Encaminhar** é aplicado a uma mensagem, somente os destinatários da mensagem podem ler a mensagem. Além disso, os destinatários não podem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="aaa2a-p117">When the **Do Not Forward** template is applied to a message, only the recipients addressed in the message can read the message. Additionally, recipients can't do the following:</span></span> 
  
- <span data-ttu-id="aaa2a-172">Encaminhar a mensagem para outra pessoa.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-172">Forward the message to another person.</span></span>
    
- <span data-ttu-id="aaa2a-173">Copiar o conteúdo da mensagem.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-173">Copy content from the message.</span></span>
    
- <span data-ttu-id="aaa2a-174">Imprimir a mensagem.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-174">Print the message.</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="aaa2a-175">O modelo **Não Encaminhar** não pode evitar que as informações de uma mensagem sejam copiadas com produtos de captura de tela de terceiros, câmeras ou transcrição manual por usuários.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-175">The **Do Not Forward** template can't prevent information in a message from being copied with third-party screen capture programs, cameras, or users manually transcribing the information</span></span> 
  
<span data-ttu-id="aaa2a-p118">Você pode criar mais modelos de política de direitos do AD RMS no servidor AD RMS, na sua organização local, para atender aos requisitos de proteção de IRM. Se você criar modelos de política de direitos do AD RMS adicionais, terá de exportar o TPD do servidor AD RMS local novamente e atualizar o TPD na organização de email baseada em nuvem.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-p118">You can create additional AD RMS rights policy templates on the AD RMS server in your on-premises organization to meet your IRM protection requirements. If you create additional AD RMS rights policy templates, you have to export the TPD from the on-premises AD RMS server again and refresh the TPD in the cloud-based email organization.</span></span> 
  
#### <a name="how-do-you-know-this-step-worked"></a><span data-ttu-id="aaa2a-178">Como saber se esta etapa funcionou?</span><span class="sxs-lookup"><span data-stu-id="aaa2a-178">How do you know this step worked?</span></span>

<span data-ttu-id="aaa2a-p119">Para verificar se você distribuiu com êxito um modelo de política de direitos do AD RMS, execute o cmdlet **Get-RMSTemplate** para verificar as propriedades do modelo. Para obter detalhes, consulte os exemplos no [Get-RMSTemplate](http://technet.microsoft.com/library/4a5066e8-b770-4aa2-b464-0d2190914f71.aspx).</span><span class="sxs-lookup"><span data-stu-id="aaa2a-p119">To verify that you have successfully distributed and AD RMS rights policy template, run the **Get-RMSTemplate** cmdlet to check the template's properties. For details, see the examples in [Get-RMSTemplate](http://technet.microsoft.com/library/4a5066e8-b770-4aa2-b464-0d2190914f71.aspx).</span></span>
  
### <a name="step-4-use-the-exchange-management-shell-to-enable-irm"></a><span data-ttu-id="aaa2a-181">Etapa 4: usar o Shell de gerenciamento do Exchange para habilitar o IRM</span><span class="sxs-lookup"><span data-stu-id="aaa2a-181">Step 4: Use the Exchange Management Shell to enable IRM</span></span>

<span data-ttu-id="aaa2a-182">Depois de importar o TPD e distribuir um modelo de política de direitos do AD RMS, execute o comando a seguir para habilitar o IRM para sua organização de email baseada em nuvem.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-182">After you import the TPD and distribute an AD RMS rights policy template, run the following command to enable IRM for your cloud-based email organization.</span></span>
  
```
Set-IRMConfiguration -InternalLicensingEnabled $true
```

<span data-ttu-id="aaa2a-183">Para obter informações detalhadas de sintaxes e parâmetros, consulte [Set-IRMConfiguration](http://technet.microsoft.com/library/5df0b56a-7bcc-4be2-b4b8-4de16720476c.aspx).</span><span class="sxs-lookup"><span data-stu-id="aaa2a-183">For detailed syntax and parameter information, see [Set-IRMConfiguration](http://technet.microsoft.com/library/5df0b56a-7bcc-4be2-b4b8-4de16720476c.aspx).</span></span>
  
#### <a name="how-do-you-know-this-step-worked"></a><span data-ttu-id="aaa2a-184">Como saber se esta etapa funcionou?</span><span class="sxs-lookup"><span data-stu-id="aaa2a-184">How do you know this step worked?</span></span>

<span data-ttu-id="aaa2a-185">Para verificar se você habilitou com êxito o IRM, execute o cmdlet [Get-IRMConfiguration](http://technet.microsoft.com/library/e1821219-fe18-4642-a9c2-58eb0aadd61a.aspx) para verificar a configuração do IRM na organização do Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-185">To verify that you have successfully enabled IRM, run the [Get-IRMConfiguration](http://technet.microsoft.com/library/e1821219-fe18-4642-a9c2-58eb0aadd61a.aspx) cmdlet to check IRM configuration in the Exchange Online organization.</span></span> 
  
## <a name="how-do-you-know-this-task-worked"></a><span data-ttu-id="aaa2a-186">Como saber se essa tarefa funcionou?</span><span class="sxs-lookup"><span data-stu-id="aaa2a-186">How do you know this task worked?</span></span>
<span data-ttu-id="aaa2a-187"><a name="sectionSection2"> </a></span><span class="sxs-lookup"><span data-stu-id="aaa2a-187"></span></span>

<span data-ttu-id="aaa2a-188">Para verificar se você importou com êxito o TPD e se habilitou o IRM, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="aaa2a-188">To verify that you have successfully imported the TPD and enabled IRM, do the following:</span></span>
  
- <span data-ttu-id="aaa2a-p120">Use o cmdlet do **Test-IRMConfiguration** para testar a funcionalidade do IRM. Para obter detalhes, confira "Exemplo 1" em [Test-IRMConfiguration](http://technet.microsoft.com/library/a730e7ff-a67f-4360-b5ff-70d171bb5e1d.aspx).</span><span class="sxs-lookup"><span data-stu-id="aaa2a-p120">Use the **Test-IRMConfiguration** cmdlet to test IRM functionality. For details, see "Example 1" in [Test-IRMConfiguration](http://technet.microsoft.com/library/a730e7ff-a67f-4360-b5ff-70d171bb5e1d.aspx).</span></span>
    
- <span data-ttu-id="aaa2a-191">Redija uma nova mensagem no Outlook na Web e proteja-a com o IRM ao selecionar a opção **definir permissões** no menu estendido ![(ícone](media/ITPro-EAC-MoreOptionsIcon.gif)mais opções).</span><span class="sxs-lookup"><span data-stu-id="aaa2a-191">Compose a new message in Outlook on the web and IRM-protect it by selecting **Set permissions** option from the extended menu ( ![More Options Icon](media/ITPro-EAC-MoreOptionsIcon.gif)).</span></span>
    


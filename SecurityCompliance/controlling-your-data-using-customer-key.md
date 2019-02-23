---
title: Controlar seus dados no Office 365 usando a Chave do cliente
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 8/1/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f2cd475a-e592-46cf-80a3-1bfb0fa17697
ms.collection:
- M365-security-compliance
description: Saiba como configurar a chave do cliente para o Office 365 para Exchange Online, Skype for Business, SharePoint Online e OneDrive for Business. Com a chave do cliente, você controla as chaves de criptografia da sua organização e, em seguida, configura o Office 365 para usá-las para criptografar seus dados em repouso nos datacenters da Microsoft.
ms.openlocfilehash: a14a213951bc87e4106e150c88c6b1461a5e685e
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218751"
---
# <a name="controlling-your-data-in-office-365-using-customer-key"></a><span data-ttu-id="a7de5-104">Controlar seus dados no Office 365 usando a Chave do cliente</span><span class="sxs-lookup"><span data-stu-id="a7de5-104">Controlling your data in Office 365 using Customer Key</span></span>

<span data-ttu-id="a7de5-p102">Com a chave do cliente, você controla as chaves de criptografia da sua organização e, em seguida, configura o Office 365 para usá-las para criptografar seus dados em repouso nos data centers da Microsoft. Os dados em repouso incluem dados do Exchange Online e do Skype for Business que são armazenados em caixas de correio e arquivos armazenados no SharePoint Online e no OneDrive for Business.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p102">With Customer Key, you control your organization's encryption keys and then configure Office 365 to use them to encrypt your data at rest in Microsoft's data centers. Data at rest includes data from Exchange Online and Skype for Business that is stored in mailboxes and files that are stored in SharePoint Online and OneDrive for Business.</span></span>
  
<span data-ttu-id="a7de5-p103">Você deve configurar o Azure antes de poder usar a chave do cliente para o Office 365. Este tópico descreve as etapas que você precisa seguir para criar e configurar os recursos do Azure necessários e, em seguida, fornece as etapas para configurar a chave do cliente no Office 365. Depois de concluir a instalação do Azure, determine a política e, portanto, quais teclas serão atribuídas a caixas de correio e arquivos em sua organização. Caixas de correio e arquivos para os quais você não atribui uma política usarão políticas de criptografia controladas e gerenciadas pela Microsoft. Para obter mais informações sobre a chave do cliente ou para uma visão geral, consulte a [chave do cliente para perguntas frequentes sobre o Office 365](service-encryption-with-customer-key-faq.md).</span><span class="sxs-lookup"><span data-stu-id="a7de5-p103">You must set up Azure before you can use Customer Key for Office 365. This topic describes the steps you need to follow to create and configure the required Azure resources and then provides the steps for setting up Customer Key in Office 365. After you have completed Azure setup, you determine which policy, and therefore, which keys, to assign to mailboxes and files in your organization. Mailboxes and files for which you don't assign a policy will use encryption policies that are controlled and managed by Microsoft. For more information about Customer Key, or for a general overview, see the [Customer Key for Office 365 FAQ](service-encryption-with-customer-key-faq.md).</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="a7de5-p104">É altamente recomendável seguir as práticas recomendadas neste tópico. Eles são chamados de **Tip** e **importante**. A chave do cliente dá controle sobre as chaves de criptografia raiz cujo escopo pode ser tão grande quanto sua organização inteira. Isso significa que os erros feitos com essas chaves podem ter um impacto amplo e podem resultar em interrupções de serviço ou perda irrevogável dos dados.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p104">We strongly recommend that you follow the best practices in this topic. These are called out as **TIP** and **IMPORTANT**. Customer Key gives you control over root encryption keys whose scope can be as large as your entire organization. This means that mistakes made with these keys can have a broad impact and may result in service interruptions or irrevocable loss of your data.</span></span> 
  
## <a name="before-you-begin-setting-up-customer-key"></a><span data-ttu-id="a7de5-116">Antes de começar a configurar a chave do cliente</span><span class="sxs-lookup"><span data-stu-id="a7de5-116">Before you begin setting up Customer Key</span></span>
<span data-ttu-id="a7de5-117"><a name="Beforeyoustart"> </a></span><span class="sxs-lookup"><span data-stu-id="a7de5-117"></span></span>

<span data-ttu-id="a7de5-p105">Antes de começar, verifique se você tem o licenciamento apropriado para sua organização. A chave do cliente no Office 365 é oferecida no Office 365 E5 ou no SKU de conformidade avançada.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p105">Before you get started, be sure you have the appropriate licensing for your organization. Customer Key in Office 365 is offered in Office 365 E5 or the Advanced Compliance SKU.</span></span>
  
<span data-ttu-id="a7de5-p106">Em seguida, para entender os conceitos e procedimentos deste tópico, você deve revisar a documentação do [Azure Key Vault](https://azure.microsoft.com/en-us/documentation/services/key-vault/) . Além disso, familiarize-se com os termos usados no Azure, por exemplo, [locatário](https://msdn.microsoft.com/library/azure/jj573650.aspx#BKMK_WhatIsAnAzureADTenant).</span><span class="sxs-lookup"><span data-stu-id="a7de5-p106">Then, to understand the concepts and procedures in this topic, you should review the [Azure Key Vault](https://azure.microsoft.com/en-us/documentation/services/key-vault/) documentation. Also, become familiar with the terms used in Azure, for example, [tenant](https://msdn.microsoft.com/library/azure/jj573650.aspx#BKMK_WhatIsAnAzureADTenant).</span></span>
  
<span data-ttu-id="a7de5-122">Para fornecer comentários sobre a chave do cliente, incluindo a documentação, envie suas ideias, sugestões e perspectivas para o customerkeyfeedback@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="a7de5-122">To provide feedback on Customer Key, including the documentation, send your ideas, suggestions and perspectives to customerkeyfeedback@microsoft.com.</span></span>
  
## <a name="overview-of-setting-up-customer-key-for-office-365"></a><span data-ttu-id="a7de5-123">Visão geral da configuração da chave do cliente para o Office 365</span><span class="sxs-lookup"><span data-stu-id="a7de5-123">Overview of setting up Customer Key for Office 365</span></span>
<span data-ttu-id="a7de5-124"><a name="Overview"> </a></span><span class="sxs-lookup"><span data-stu-id="a7de5-124"></span></span>

<span data-ttu-id="a7de5-p107">Para configurar a chave do cliente, você concluirá essas tarefas. O restante deste tópico fornece instruções detalhadas para cada tarefa ou links para mais informações de cada etapa do processo.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p107">To set up Customer Key you will complete these tasks. The rest of this topic provides detailed instructions for each task, or links out to more information for each step in the process.</span></span>
  
<span data-ttu-id="a7de5-127">**No Azure e no Microsoft FastTrack:**</span><span class="sxs-lookup"><span data-stu-id="a7de5-127">**In Azure and Microsoft FastTrack:**</span></span>
  
<span data-ttu-id="a7de5-p108">Você concluirá a maioria dessas tarefas, conectando-se remotamente ao Azure PowerShell. Para obter melhores resultados, use a versão 4.4.0 ou posterior do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p108">You will complete most of these tasks by remotely connecting to Azure PowerShell. For best results, use version 4.4.0 or later of Azure PowerShell.</span></span>
  
- [<span data-ttu-id="a7de5-130">Criar duas novas assinaturas do Azure</span><span class="sxs-lookup"><span data-stu-id="a7de5-130">Create two new Azure subscriptions</span></span>](controlling-your-data-using-customer-key.md#Create2newsubs)
    
- [<span data-ttu-id="a7de5-131">Registrar assinaturas do Azure para usar um período de retenção obrigatório</span><span class="sxs-lookup"><span data-stu-id="a7de5-131">Register Azure subscriptions to use a mandatory retention period</span></span>](controlling-your-data-using-customer-key.md#RegisterSubsforMRP)
    
    <span data-ttu-id="a7de5-132">O registro pode levar de um a cinco dias úteis.</span><span class="sxs-lookup"><span data-stu-id="a7de5-132">Registration can take from one to five business days.</span></span>
    
- [<span data-ttu-id="a7de5-133">Enviar uma solicitação para ativar a chave do cliente para o Office 365</span><span class="sxs-lookup"><span data-stu-id="a7de5-133">Submit a request to activate Customer Key for Office 365</span></span>](controlling-your-data-using-customer-key.md#FastTrack)
    
    <span data-ttu-id="a7de5-p109">Depois de criar as duas novas assinaturas do Azure, você precisará enviar a solicitação de oferta de chave do cliente apropriada, concluindo um formulário da Web hospedado no portal Microsoft FastTrack. **A equipe do FastTrack não fornece assistência com a chave do cliente. O Office simplesmente usa o portal do FastTrack para permitir que você envie o formulário e ajude-nos a acompanhar as ofertas relevantes para a chave do cliente**.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p109">Once you've created the two new Azure subscriptions, you'll need to submit the appropriate Customer Key offer request by completing a web form that is hosted in the Microsoft FastTrack portal. **The FastTrack team doesn't provide assistance with Customer Key. Office simply uses the FastTrack portal to allow you to submit the form and to help us track the relevant offers for Customer Key**.</span></span>
  
<span data-ttu-id="a7de5-p110">Depois de enviar uma oferta de chave do cliente, a Microsoft revisa sua solicitação e notifica você quando você pode prosseguir com o restante das tarefas de configuração. Esse processo pode levar até cinco dias úteis.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p110">Once you have submitted a Customer Key offer, Microsoft reviews your request and notifies you when you can proceed with the rest of the setup tasks. This process can take up to five business days.</span></span>
    
- [<span data-ttu-id="a7de5-138">Criar um cofre de chaves Premium do Azure em cada assinatura</span><span class="sxs-lookup"><span data-stu-id="a7de5-138">Create a premium Azure Key Vault in each subscription</span></span>](controlling-your-data-using-customer-key.md#CreateKeyVault)
    
- [<span data-ttu-id="a7de5-139">Atribuir permissões a cada cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="a7de5-139">Assign permissions to each key vault</span></span>](controlling-your-data-using-customer-key.md#KeyVaultPerms)
    
- [<span data-ttu-id="a7de5-140">Habilitar e confirmar a exclusão reversível nos seus principais cofres</span><span class="sxs-lookup"><span data-stu-id="a7de5-140">Enable and then confirm soft delete on your key vaults</span></span>](controlling-your-data-using-customer-key.md#SoftDelete)
    
- [<span data-ttu-id="a7de5-141">Adicionar uma chave a cada cofre de chaves criando ou importando uma chave</span><span class="sxs-lookup"><span data-stu-id="a7de5-141">Add a key to each key vault either by creating or importing a key</span></span>](controlling-your-data-using-customer-key.md#AddKeystoKeyVault)
    
- [<span data-ttu-id="a7de5-142">Verificar o nível de recuperação de suas chaves</span><span class="sxs-lookup"><span data-stu-id="a7de5-142">Check the recovery level of your keys</span></span>](controlling-your-data-using-customer-key.md#CheckKeyRecoveryLevel)
    
- [<span data-ttu-id="a7de5-143">Backup do Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="a7de5-143">Backup Azure Key Vault</span></span>](controlling-your-data-using-customer-key.md#BackupAzureKeyVaultkeys)
    
- [<span data-ttu-id="a7de5-144">Validar definições de configuração do Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="a7de5-144">Validate Azure Key Vault configuration settings</span></span>](controlling-your-data-using-customer-key.md#Validateconfiguration)
    
- [<span data-ttu-id="a7de5-145">Obter o URI para cada chave do Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="a7de5-145">Obtain the URI for each Azure Key Vault key</span></span>](controlling-your-data-using-customer-key.md#GetKeyURI)
    
<span data-ttu-id="a7de5-146">**No Office 365:**</span><span class="sxs-lookup"><span data-stu-id="a7de5-146">**In Office 365:**</span></span>
  
<span data-ttu-id="a7de5-147">Exchange Online e Skype for Business:</span><span class="sxs-lookup"><span data-stu-id="a7de5-147">Exchange Online and Skype for Business:</span></span>
  
- [<span data-ttu-id="a7de5-148">Criar uma DEP (política de criptografia de dados) para uso com o Exchange Online e o Skype for Business</span><span class="sxs-lookup"><span data-stu-id="a7de5-148">Create a data encryption policy (DEP) for use with Exchange Online and Skype for Business</span></span>](controlling-your-data-using-customer-key.md#CreateDEP4EXOSkype)
    
- [<span data-ttu-id="a7de5-149">Atribuir uma DEP a uma caixa de correio</span><span class="sxs-lookup"><span data-stu-id="a7de5-149">Assign a DEP to a mailbox</span></span>](controlling-your-data-using-customer-key.md#assignDEPtomailbox)
    
- [<span data-ttu-id="a7de5-150">Validar criptografia de caixa de correio</span><span class="sxs-lookup"><span data-stu-id="a7de5-150">Validate mailbox encryption</span></span>](controlling-your-data-using-customer-key.md#validatemailboxencryption)
    
<span data-ttu-id="a7de5-151">SharePoint Online e OneDrive for Business:</span><span class="sxs-lookup"><span data-stu-id="a7de5-151">SharePoint Online and OneDrive for Business:</span></span>
  
- [<span data-ttu-id="a7de5-152">Criar uma DEP (política de criptografia de dados) para cada Geografia do SharePoint Online e do OneDrive for Business</span><span class="sxs-lookup"><span data-stu-id="a7de5-152">Create a data encryption policy (DEP) for each SharePoint Online and OneDrive for Business geo</span></span>](controlling-your-data-using-customer-key.md#CreateDEP4SPOODfB)
    
- [<span data-ttu-id="a7de5-153">Validar a criptografia de sites de grupo, sites de equipe e o OneDrive for Business</span><span class="sxs-lookup"><span data-stu-id="a7de5-153">Validate encryption of Group Sites, Team Sites, and OneDrive for Business</span></span>](controlling-your-data-using-customer-key.md#validateencryptionSPO)
    
## <a name="complete-tasks-in-azure-key-vault-and-microsoft-fasttrack-for-customer-key"></a><span data-ttu-id="a7de5-154">Concluir tarefas no Azure Key Vault e no Microsoft FastTrack para chave do cliente</span><span class="sxs-lookup"><span data-stu-id="a7de5-154">Complete tasks in Azure Key Vault and Microsoft FastTrack for Customer Key</span></span>
<span data-ttu-id="a7de5-155"><a name="AzureSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="a7de5-155"></span></span>

<span data-ttu-id="a7de5-p111">Conclua essas tarefas no Azure Key Vault para configurar a chave do cliente para o Office 365. Você precisará concluir essas etapas, independentemente se pretende configurar a chave do cliente para o Exchange Online e o Skype for Business ou o SharePoint Online e o OneDrive for Business ou para todos os serviços com suporte no Office 365.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p111">Complete these tasks in Azure Key Vault in order to set up Customer Key for Office 365. You will need to complete these steps regardless of whether you intend to set up Customer Key for Exchange Online and Skype for Business or SharePoint Online and OneDrive for Business or for all supported services in Office 365.</span></span>
  
### <a name="create-two-new-azure-subscriptions"></a><span data-ttu-id="a7de5-158">Criar duas novas assinaturas do Azure</span><span class="sxs-lookup"><span data-stu-id="a7de5-158">Create two new Azure subscriptions</span></span>
<span data-ttu-id="a7de5-159"><a name="Create2newsubs"> </a></span><span class="sxs-lookup"><span data-stu-id="a7de5-159"></span></span>

<span data-ttu-id="a7de5-p112">Duas assinaturas do Azure são necessárias para a chave do cliente. Como prática recomendada, a Microsoft recomenda que você crie novas assinaturas do Azure para uso com a chave do cliente. Chaves do Azure Key Vault só podem ser autorizadas para aplicativos no mesmo locatário do Azure Active Directory (AAD), você deve criar as novas assinaturas usando o mesmo locatário do Azure AD usado com sua organização do Office 365, onde o DEPs será atribuído. Por exemplo, usando sua conta corporativa ou de estudante que tenha privilégios de administrador global em sua organização do Office 365. Para obter etapas detalhadas, consulte [inscrever-se no Azure como uma organização](https://azure.microsoft.com/en-us/documentation/articles/sign-up-organization/).</span><span class="sxs-lookup"><span data-stu-id="a7de5-p112">Two Azure subscriptions are required for Customer Key. As a best practice, Microsoft recommends that you create new Azure subscriptions for use with Customer Key. Azure Key Vault keys can only be authorized for applications in the same Azure Active Directory (AAD) tenant, you must create the new subscriptions using the same Azure AD tenant used with your Office 365 organization where the DEPs will be assigned. For example, using your work or school account that has global administrator privileges in your Office 365 organization. For detailed steps, see [Sign up for Azure as an organization](https://azure.microsoft.com/en-us/documentation/articles/sign-up-organization/).</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="a7de5-p113">A chave do cliente requer duas chaves para cada DEP (política de criptografia de dados). Para conseguir isso, você deve criar duas assinaturas do Azure. Como prática recomendada, a Microsoft recomenda que você tenha Membros separados da sua organização para configurar uma chave em cada assinatura. Além disso, essas assinaturas do Azure devem ser usadas apenas para administrar chaves de criptografia para o Office 365. Isso protegerá a sua organização caso um de seus operadores acidentalmente, intencionalmente ou exclua inadvertidamente as chaves para as quais são responsáveis.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p113">Customer Key requires two keys for each data encryption policy (DEP). In order to achieve this, you must create two Azure subscriptions. As a best practice, Microsoft recommends that you have separate members of your organization configure one key in each subscription. In addition, these Azure subscriptions should only be used to administer encryption keys for Office 365. This protects your organization in case one of your operators accidentally, intentionally, or maliciously deletes or otherwise mismanages the keys for which they are responsible. </span></span><br/> <span data-ttu-id="a7de5-p114">Recomendamos que você configure novas assinaturas do Azure que são usadas unicamente para o gerenciamento de recursos do Azure Key Vault para uso com a chave do cliente. Não há um limite prático para o número de assinaturas do Azure que você pode criar para sua organização. Seguir estas práticas recomendadas minimizará o impacto do erro humano enquanto ajuda a gerenciar os recursos usados pela chave do cliente.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p114">We recommend that you set up new Azure subscriptions that are solely used for managing Azure Key Vault resources for use with Customer Key. There is no practical limit to the number of Azure subscriptions that you can create for your organization. Following these best practices will minimize the impact of human error while helping to manage the resources used by Customer Key.</span></span> 
  
### <a name="submit-a-request-to-activate-customer-key-for-office-365"></a><span data-ttu-id="a7de5-173">Enviar uma solicitação para ativar a chave do cliente para o Office 365</span><span class="sxs-lookup"><span data-stu-id="a7de5-173">Submit a request to activate Customer Key for Office 365</span></span>
<span data-ttu-id="a7de5-174"><a name="FastTrack"> </a></span><span class="sxs-lookup"><span data-stu-id="a7de5-174"></span></span>

<span data-ttu-id="a7de5-p115">Depois de concluir as etapas do Azure, você precisará enviar uma solicitação de oferta no [portal Microsoft FastTrack](https://fasttrack.microsoft.com/). Depois de enviar uma solicitação pelo portal da Web do FastTrack, a Microsoft verifica os dados de configuração e informações de contato do Azure Key Vault que você forneceu. As seleções feitas no formulário de oferta em relação aos responsáveis autorizados da sua organização são fundamentais e necessárias para a conclusão do registro de chave do cliente. Os gerentes da sua organização selecionados no formulário serão usados para garantir a autenticidade de qualquer solicitação de revogação e destruição de todas as chaves usadas com uma política de criptografia de dados de chave do cliente. Você precisará fazer esta etapa uma vez para ativar a chave do cliente para o Exchange Online e a cobertura do Skype for Business e uma segunda vez para ativar a chave do cliente para o SharePoint Online e o OneDrive for Business.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p115">Once you've completed the Azure steps, you'll need to submit an offer request in the [Microsoft FastTrack portal](https://fasttrack.microsoft.com/). Once you have submitted a request through the FastTrack web portal, Microsoft verifies the Azure Key Vault configuration data and contact information you provided. The selections that you make in the offer form regarding the authorized officers of your organization is critical and necessary for completion of Customer Key registration. The officers of your organization that you select in the form will be the used to ensure the authenticity of any request to revoke and destroy all keys used with a Customer Key data encryption policy. You'll need to do this step once to activate Customer Key for Exchange Online and Skype for Business coverage and a second time to activate Customer Key for SharePoint Online and OneDrive for Business.</span></span>
  
<span data-ttu-id="a7de5-180">Para enviar uma oferta para ativar a chave do cliente, conclua estas etapas:</span><span class="sxs-lookup"><span data-stu-id="a7de5-180">To submit an offer to activate Customer Key, complete these steps:</span></span>
  
1. <span data-ttu-id="a7de5-181">Usando uma conta corporativa ou de estudante que tenha permissões de administrador global em sua organização do Office 365, faça logon no [portal do Microsoft FastTrack](https://fasttrack.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="a7de5-181">Using a work or school account that has global administrator permissions in your Office 365 organization, log in to the [Microsoft FastTrack portal](https://fasttrack.microsoft.com/).</span></span>
    
2. <span data-ttu-id="a7de5-182">Quando estiver conectado, navegue até o **painel**.</span><span class="sxs-lookup"><span data-stu-id="a7de5-182">Once you're logged in, browse to the **Dashboard**.</span></span>
    
3. <span data-ttu-id="a7de5-183">Escolha **ofertas**e revise a lista de ofertas atuais.</span><span class="sxs-lookup"><span data-stu-id="a7de5-183">Choose **Offers**, and review the list of current offers.</span></span>
    
4. <span data-ttu-id="a7de5-184">Escolha **saiba mais** para a oferta que se aplica a você:</span><span class="sxs-lookup"><span data-stu-id="a7de5-184">Choose **Learn More** for the offer that applies to you:</span></span> 
    
  - <span data-ttu-id="a7de5-185">**Exchange Online e Skype for Business:** Escolha **saiba mais** sobre a **chave do cliente para a oferta do Exchange** .</span><span class="sxs-lookup"><span data-stu-id="a7de5-185">**Exchange Online and Skype for Business:** Choose **Learn More** on the **Customer Key for Exchange** offer.</span></span> 
    
  - <span data-ttu-id="a7de5-186">**SharePoint Online e onedrive for Business:** Escolhido **saiba mais** sobre a **chave do cliente para o SharePoint e o onedrive for Business** offer.</span><span class="sxs-lookup"><span data-stu-id="a7de5-186">**SharePoint Online and OneDrive for Business:** Chose **Learn More** on the **Customer Key for SharePoint and OneDrive for Business** offer.</span></span> 
    
5. <span data-ttu-id="a7de5-187">Na página **detalhes da oferta** , escolha **criar solicitação**.</span><span class="sxs-lookup"><span data-stu-id="a7de5-187">On the **Offer details** page, choose **Create Request**.</span></span>
    
6. <span data-ttu-id="a7de5-p116">Preencha todos os detalhes aplicáveis e as informações solicitadas sobre o formulário de oferta. Preste bastante atenção às suas seleções para quais responsáveis da sua organização você deseja autorizar a aprovar a destruição permanente e irreversível de chaves e dados de criptografia. Depois de concluir o formulário, escolha **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p116">Fill out all applicable details and requested information on the offer form. Pay particular attention to your selections for which officers of your organization you want to authorize to approve the permanent and irreversible destruction of encryption keys and data. Once you've completed the form, choose **Submit**.</span></span>
    
    <span data-ttu-id="a7de5-191">Esse processo pode levar até cinco dias úteis quando a Microsoft for notificada de sua solicitação.</span><span class="sxs-lookup"><span data-stu-id="a7de5-191">This process can take up to five business days once Microsoft has been notified of your request.</span></span>
    
7. <span data-ttu-id="a7de5-192">Continue na seção período de retenção obrigatório abaixo.</span><span class="sxs-lookup"><span data-stu-id="a7de5-192">Continue on to the mandatory retention period section below.</span></span>
    
### <a name="register-azure-subscriptions-to-use-a-mandatory-retention-period"></a><span data-ttu-id="a7de5-193">Registrar assinaturas do Azure para usar um período de retenção obrigatório</span><span class="sxs-lookup"><span data-stu-id="a7de5-193">Register Azure subscriptions to use a mandatory retention period</span></span>
<span data-ttu-id="a7de5-194"><a name="RegisterSubsforMRP"> </a></span><span class="sxs-lookup"><span data-stu-id="a7de5-194"></span></span>

<span data-ttu-id="a7de5-p117">A perda temporária ou permanente das chaves de criptografia raiz pode ser muito prejudicial ou até mesmo uma operação de serviço e pode resultar em perda de dados. Por esse motivo, os recursos usados com a chave do cliente exigem uma forte proteção. Todos os recursos do Azure usados com os mecanismos de proteção da oferta de chave do cliente além da configuração padrão. As assinaturas do Azure podem ser marcadas ou registradas de uma maneira que impedirá o cancelamento imediato e irrevogável. Isso é conhecido como registro em um período de retenção obrigatório. As etapas necessárias para registrar assinaturas do Azure para um período de retenção obrigatório exigem colaboração com a equipe do Office 365. Esse processo pode levar de um a cinco dias úteis. Anteriormente, isso também era conhecido como "não cancelar".</span><span class="sxs-lookup"><span data-stu-id="a7de5-p117">The temporary or permanent loss of root encryption keys can be very disruptive or even catastrophic to service operation and can result in data loss. For this reason, the resources used with Customer Key require strong protection. All the Azure resources that are used with Customer Key offer protection mechanisms beyond the default configuration. Azure subscriptions can be tagged or registered in a way that will prevent immediate and irrevocable cancellation. This is referred to as registering for a mandatory retention period. The steps required to register Azure subscriptions for a mandatory retention period require collaboration with the Office 365 team. This process can take from one to five business days. Previously, this was sometimes referred to as "Do Not Cancel".</span></span>
  
<span data-ttu-id="a7de5-203">Antes de entrar em contato com a equipe do Office 365, você deve executar as seguintes etapas para cada assinatura do Azure que você usa com a chave do cliente:</span><span class="sxs-lookup"><span data-stu-id="a7de5-203">Before contacting the Office 365 team, you must perform the following steps for each Azure subscription that you use with Customer Key:</span></span>
  
1. <span data-ttu-id="a7de5-p118">Faça logon em sua assinatura do Azure com o Azure PowerShell. Para obter instruções, consulte [fazer logon com o Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).</span><span class="sxs-lookup"><span data-stu-id="a7de5-p118">Log in to your Azure subscription with Azure PowerShell. For instructions, see [Log in with Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).</span></span>
    
2. <span data-ttu-id="a7de5-206">Execute o cmdlet Register-AzureRmProviderFeature para registrar suas assinaturas para usar um período de retenção obrigatório.</span><span class="sxs-lookup"><span data-stu-id="a7de5-206">Run the Register-AzureRmProviderFeature cmdlet to register your subscriptions to use a mandatory retention period.</span></span>
    
  ```
  Register-AzureRmProviderFeature -FeatureName mandatoryRetentionPeriodEnabled -ProviderNamespace Microsoft.Resources
  ```

3. <span data-ttu-id="a7de5-p119">Entre em contato com a Microsoft para finalizar o processo. Para a equipe do SharePoint e do OneDrive for Business, entre em contato com [Spock@microsoft.com](mailto:spock@microsoft.com). Para o Exchange Online e o Skype for Business, entre em contato com a [exock@microsoft.com](mailto:exock@microsoft.com). O contrato de nível de serviço (SLA) para a conclusão desse processo é de cinco dias úteis quando a Microsoft é notificada (e verificada) que você registrou suas assinaturas para usar um período de retenção obrigatório. Inclua o seguinte em seu email:</span><span class="sxs-lookup"><span data-stu-id="a7de5-p119">Contact Microsoft to have the process finalized. For the SharePoint and OneDrive for Business team, contact [spock@microsoft.com](mailto:spock@microsoft.com). For Exchange Online and Skype for Business, contact [exock@microsoft.com](mailto:exock@microsoft.com). The Service Level Agreement (SLA) for completion of this process is five business days once Microsoft has been notified (and verified) that you have registered your subscriptions to use a mandatory retention period. Include the following in your email:</span></span>
    
    <span data-ttu-id="a7de5-212">**Subject**: chave de cliente \<para *o nome de domínio totalmente qualificado do seu locatário*\></span><span class="sxs-lookup"><span data-stu-id="a7de5-212">**Subject**: Customer Key for \<*Your tenant's fully-qualified domain name*\></span></span> 
    
    <span data-ttu-id="a7de5-213">**Corpo**: IDs de assinatura para as quais você deseja que o período de retenção obrigatório seja concluído.</span><span class="sxs-lookup"><span data-stu-id="a7de5-213">**Body**: Subscription IDs for which you want to have the mandatory retention period finalized.</span></span> 
    
4. <span data-ttu-id="a7de5-214">Depois que você receber uma notificação da Microsoft de que o registro foi concluído, verifique o status do seu registro executando o cmdlet Get-AzureRmProviderFeature da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="a7de5-214">Once you receive notification from Microsoft that registration is complete, verify the status of your registration by running the Get-AzureRmProviderFeature cmdlet as follows:</span></span>
    
  ```
  Get-AzureRmProviderFeature -ProviderNamespace Microsoft.Resources -FeatureName mandatoryRetentionPeriodEnabled
  ```

5. <span data-ttu-id="a7de5-215">Depois de verificar se a propriedade de **estado de registro** do cmdlet Get-AzureRmProviderFeature retorna um valor de **Registered**, execute o seguinte comando para concluir o processo:</span><span class="sxs-lookup"><span data-stu-id="a7de5-215">After verifying that the **Registration State** property from the Get-AzureRmProviderFeature cmdlet returns a value of **Registered**, run the following command to complete the process:</span></span>
    
  ```
  Register-AzureRmResourceProvider -ProviderNamespace "Microsoft.KeyVault"
  ```

### <a name="create-a-premium-azure-key-vault-in-each-subscription"></a><span data-ttu-id="a7de5-216">Criar um cofre de chaves Premium do Azure em cada assinatura</span><span class="sxs-lookup"><span data-stu-id="a7de5-216">Create a premium Azure Key Vault in each subscription</span></span>
<span data-ttu-id="a7de5-217"><a name="CreateKeyVault"> </a></span><span class="sxs-lookup"><span data-stu-id="a7de5-217"></span></span>

<span data-ttu-id="a7de5-218">As etapas para criar um cofre de chaves são documentadas na [introdução ao Azure Key Vault](https://azure.microsoft.com/documentation/articles/key-vault-get-started/), que orienta você durante a instalação e o lançamento do Azure PowerShell, a conexão com sua assinatura do Azure, a criação de um grupo de recursos e a criação de um cofre de chaves nesse grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a7de5-218">The steps to create a key vault are documented in [Getting Started with Azure Key Vault](https://azure.microsoft.com/documentation/articles/key-vault-get-started/), which guides you through installing and launching Azure PowerShell, connecting to your Azure subscription, creating a resource group, and creating a key vault in that resource group.</span></span>
  
<span data-ttu-id="a7de5-p120">Ao criar um cofre de chaves, você deve escolher um SKU: Standard ou Premium. A SKU padrão permite que as chaves do Azure Key Vault sejam protegidas por software – não há nenhuma proteção de chave do módulo de segurança de hardware (HSM), e a SKU Premium permite o uso de HSMs para proteção de chaves de compartimento de chaves. A chave do cliente aceita os principais cofres que usam SKU, embora a Microsoft recomende enfaticamente que você use apenas o SKU Premium. O custo das operações com chaves de qualquer tipo é o mesmo, portanto, a única diferença no custo é o custo por mês para cada chave protegida por HSM. ConFira os [preços do Key Vault](https://azure.microsoft.com/pricing/details/key-vault/) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p120">When you create a key vault, you must choose a SKU: either Standard or Premium. The Standard SKU allows Azure Key Vault keys to be protected with software - there is no Hardware Security Module (HSM) key protection - and the Premium SKU allows the use of HSMs for protection of Key Vault keys. Customer Key accepts key vaults that use either SKU, though Microsoft strongly recommends that you use only the Premium SKU. The cost of operations with keys of either type is the same, so the only difference in cost is the cost per month for each HSM-protected key. See [Key Vault pricing](https://azure.microsoft.com/pricing/details/key-vault/) for details.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="a7de5-224">Use os compartimentos de chave de SKU Premium e chaves protegidas por HSM para dados de produção e use somente os compartimentos de chave de SKU padrão e chaves para fins de teste e validação.</span><span class="sxs-lookup"><span data-stu-id="a7de5-224">Use the Premium SKU key vaults and HSM-protected keys for production data, and only use Standard SKU key vaults and keys for testing and validation purposes.</span></span> 
  
<span data-ttu-id="a7de5-p121">Para cada serviço do Office 365 com o qual você usará a chave do cliente, crie um cofre de chaves em cada uma das duas assinaturas do Azure que você criou. Por exemplo, apenas para o Exchange Online e o Skype for Business, somente para o SharePoint Online e o OneDrive for Business, você irá criar apenas um par de cofres. Para habilitar a chave do cliente para o Exchange Online e o SharePoint Online, você irá criar dois pares de cofres de chaves.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p121">For each Office 365 service with which you will use Customer Key, create a key vault in each of the two Azure subscriptions that you created. For example, for Exchange Online and Skype for Business only or SharePoint Online and OneDrive for Business only, you will create only one pair of vaults. To enable Customer Key for both Exchange Online and SharePoint Online, you will create two pairs of key vaults.</span></span>
  
<span data-ttu-id="a7de5-p122">Use uma Convenção de nomenclatura para os principais cofres que reflitam o uso pretendido da DEP com a qual você irá associar os cofres. Consulte a seção práticas recomendadas abaixo para obter recomendações de Convenção de nomenclatura.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p122">Use a naming convention for key vaults that reflects the intended use of the DEP with which you will associate the vaults. See the Best Practices section below for naming convention recommendations.</span></span>
  
<span data-ttu-id="a7de5-p123">Crie um conjunto separado e emparelhado de cofres para cada política de criptografia de dados. Para o Exchange Online, o escopo de uma política de criptografia de dados é escolhido quando você atribui a política à caixa de correio. Uma caixa de correio pode ter apenas uma política atribuída, e você pode criar até 50 políticas. Para o SharePoint Online, o escopo de uma política é todos os dados dentro de uma organização em um local geográfico ou Geo.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p123">Create a separate, paired set of vaults for each data encryption policy. For Exchange Online, the scope of a data encryption policy is chosen by you when you assign the policy to mailbox. A mailbox can have only one policy assigned, and you can create up to fifty policies. For SharePoint Online the scope of a policy is all of the data within an organization in a geographic location, or geo.</span></span>
  
<span data-ttu-id="a7de5-p124">A criação de compartimentos de chave também requer a criação de grupos de recursos do Azure, pois os principais cofres precisam de capacidade de armazenamento (embora muito pequeno) e do registro em log de compartimento de chaves, se habilitado, também gera dados armazenados. Como prática recomendada, a Microsoft recomenda o uso de administradores separados para gerenciar cada grupo de recursos, com a administração centralizada com o conjunto de administradores que gerenciará todos os recursos de chave do cliente relacionados.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p124">The creation of key vaults also requires the creation of Azure resource groups, since key vaults need storage capacity (though very small) and Key Vault logging, if enabled, also generates stored data. As a best practice Microsoft recommends using separate administrators to manage each resource group, with the administration aligned with the set of administrators that will manage all related Customer Key resources.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="a7de5-p125">Para maximizar a disponibilidade, seus cofres de chaves devem estar próximos às regiões do serviço do Office 365. Por exemplo, se sua organização do Exchange Online estiver na América do Norte, coloque seus principais cofres na América do Norte. Se sua organização do Exchange Online estiver na Europa, coloque seus principais cofres na Europa.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p125">To maximize availability, your key vaults should be in regions close to your Office 365 service. For example, if your Exchange Online organization is in North America, place your key vaults in North America. If your Exchange Online organization is in Europe, place your key vaults in Europe.</span></span><br/><span data-ttu-id="a7de5-p126">Use um prefixo comum para os principais compartimentos e inclua uma abreviação do uso e do escopo do compartimento de chaves e chaves (por exemplo, para o serviço do SharePoint da Contoso onde os cofres estarão localizados na América do Norte, um possível par de nomes é contoso-O365SP-NÃODISP-VaultA1 e Contoso-O365SP-NA-VaultA2. Os nomes de cofre são cadeias de caracteres globalmente exclusivas no Azure, portanto, talvez você precise tentar variações dos nomes desejados, caso os nomes desejados já sejam reivindicados por outros clientes do Azure. Os nomes de cofre de julho de 2017 não podem ser alterados, portanto, uma prática recomendada é ter um plano escrito para configuração e usar uma segunda pessoa para verificar se o plano foi executado corretamente.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p126">Use a common prefix for key vaults, and include an abbreviation of the use and scope of the key vault and keys (e.g., for the Contoso SharePoint service where the vaults will be located in North America, a possible pair of names is Contoso-O365SP-NA-VaultA1 and Contoso-O365SP-NA-VaultA2. Vault names are globally unique strings within Azure, so you may need to try variations of your desired names in case the desired names are already claimed by other Azure customers. As of July 2017 vault names cannot be changed, so a best practice is to have a written plan for setup and use a second person to verify the plan is executed correctly.</span></span><br/><span data-ttu-id="a7de5-p127">Se possível, crie seus cofres em regiões não emparelhadas. As regiões emparelhadas do Azure fornecem alta disponibilidade entre domínios de falha de serviço. Portanto, os pares regionais podem ser considerados como a região de backup uns dos outros. Isso significa que um recurso do Azure colocado em uma região é automaticamente obter tolerância a falhas por meio da região emparelhada. Por esse motivo, escolher regiões para dois cofres usados em uma DEP onde as regiões estão emparelhadas significa que apenas um total de duas regiões de disponibilidade está em uso. A maioria dos geografias tem apenas duas regiões, portanto, ainda não é possível selecionar regiões não emparelhadas. Se possível, escolha duas regiões não emparelhadas para os dois cofres usados com uma DEP. Isso beneficia de um total de quatro regiões de disponibilidade. Para obter mais informações, consulte [continuidade de negócios e recuperação de desastres (BCDR): regiões emparelhaDas do Azure](https://docs.microsoft.com/azure/best-practices-availability-paired-regions) para uma lista atual de pares regionais.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p127">If possible, create your vaults in non-paired regions. Paired Azure regions provide high availability across service failure domains. Therefore, regional pairs can be thought of as each other's backup region. This means that an Azure resource that is placed in one region is automatically gaining fault tolerance through the paired region. For this reason, choosing regions for two vaults used in a DEP where the regions are paired means that only a total of two regions of availability are in use. Most geographies only have two regions, so it's not yet possible to select non-paired regions. If possible, choose two non-paired regions for the two vaults used with a DEP. This benefits from a total of four regions of availability. For more information, see [Business continuity and disaster recovery (BCDR): Azure Paired Regions](https://docs.microsoft.com/azure/best-practices-availability-paired-regions) for a current list of regional pairs.</span></span> 
  
### <a name="assign-permissions-to-each-key-vault"></a><span data-ttu-id="a7de5-251">Atribuir permissões a cada cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="a7de5-251">Assign permissions to each key vault</span></span>
<span data-ttu-id="a7de5-252"><a name="KeyVaultPerms"> </a></span><span class="sxs-lookup"><span data-stu-id="a7de5-252"></span></span>

<span data-ttu-id="a7de5-p128">Para cada cofre de chave, você precisará definir três conjuntos separados de permissões para a chave do cliente, dependendo da sua implementação. Por exemplo, você precisará definir um conjunto de permissões para cada um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="a7de5-p128">For each key vault, you will need to define three separate sets of permissions for Customer Key, depending on your implementation. For example, you will need to define one set of permissions for each of the following:</span></span>
  
- <span data-ttu-id="a7de5-p129">**Administradores** de compartimentos de chaves que realizarão o gerenciamento diário de seu cofre de chaves para sua organização. Essas tarefas incluem backup, criar, obter, importar, listar e restaurar.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p129">**Key vault administrators** that will perform day-to-day management of your key vault for your organization. These tasks include backup, create, get, import, list, and restore.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="a7de5-p130">O conjunto de permissões atribuídas aos administradores de compartimento de chaves não inclui a permissão para excluir chaves. Isso é intencional e uma prática importante. Excluir chaves de criptografia normalmente não é feito, pois fazer isso permanentemente destrói os dados. Como prática recomendada, não conceda essa permissão a administradores de compartimento de chave por padrão. Em vez disso, Reserve-a para os colaboradores de Key Vault e apenas atribua-o a um administrador a curto prazo quando uma compreensão clara das conseqüências é entendida.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p130">The set of permissions assigned to key vault administrators does not include the permission to delete keys. This is intentional and an important practice. Deleting encryption keys is not typically done, since doing so permanently destroys data. As a best practice, do not grant this permission to key vault administrators by default. Instead, reserve this for key vault contributors and only assign it to an administrator on a short term basis once a clear understanding of the consequences is understood.</span></span> 
  
    <span data-ttu-id="a7de5-p131">Para atribuir essas permissões a um usuário na sua organização do Office 365, faça logon em sua assinatura do Azure com o Azure PowerShell. Para obter instruções, consulte [fazer logon com o Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).</span><span class="sxs-lookup"><span data-stu-id="a7de5-p131">To assign these permissions to a user in your Office 365 organization, log in to your Azure subscription with Azure PowerShell. For instructions, see [Log in with Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).</span></span>
    
- <span data-ttu-id="a7de5-264">Execute o cmdlet Set-AzureRmKeyVaultAccessPolicy para atribuir as permissões necessárias.</span><span class="sxs-lookup"><span data-stu-id="a7de5-264">Run the Set-AzureRmKeyVaultAccessPolicy cmdlet to assign the necessary permissions.</span></span>
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> 
  -UserPrincipalName <UPN of user> -PermissionsToKeys create,import,list,get,backup,restore
  ```

  <span data-ttu-id="a7de5-265">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="a7de5-265">For example:</span></span>
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
  -UserPrincipalName alice@contoso.com -PermissionsToKeys create,import,list,get,backup,restore
  ```

- <span data-ttu-id="a7de5-p132">Os **principais colaboradores do cofre** que podem alterar as permissões no próprio Azure Key Vault. Você precisará alterar essas permissões à medida que os funcionários saírem ou ingressarem em sua equipe ou na situação extremamente rara que os administradores de cofre de chaves precisam de permissão legítima para excluir ou restaurar uma chave. Esse conjunto de colaboradores de compartimento de chave precisa ter a função de **colaborador** no seu cofre de chaves. Você pode atribuir essa função usando o Azure Resource Manager. Para obter etapas detalhadas, consulte [use Role-Based Access Control para gerenciar o acesso aos seus recursos de assinatura do Azure](https://docs.microsoft.com/azure/active-directory/role-based-access-control-configure). O administrador que cria uma assinatura tem esse acesso implicitamente, bem como a capacidade de atribuir outros administradores à função colaborador.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p132">**Key vault contributors** that can change permissions on the Azure Key Vault itself. You'll need to change these permissions as employees leave or join your team, or in the extremely rare situation that the key vault administrators legitimately need permission to delete or restore a key. This set of key vault contributors needs to be granted the **Contributor** role on your key vault. You can assign this role by using Azure Resource Manager. For detailed steps, see [Use Role-Based Access Control to manage access to your Azure subscription resources](https://docs.microsoft.com/azure/active-directory/role-based-access-control-configure). The administrator who creates a subscription has this access implicitly, as well as the ability to assign other administrators to the Contributor role.</span></span>
    
- <span data-ttu-id="a7de5-p133">Se você pretende usar a chave do cliente com o Exchange Online e o Skype for Business, precisará conceder permissão ao Office 365 para usar o cofre de chaves em nome do Exchange Online e do Skype for Business. Da mesma forma, se você pretende usar a chave do cliente com o SharePoint Online e o OneDrive for Business, precisará adicionar permissão para o Office 365 para usar o cofre de chaves em nome do SharePoint Online e do OneDrive for Business. Para dar permissão ao Office 365, execute o cmdlet **set-AzureRmKeyVaultAccessPolicy** usando a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="a7de5-p133">If you intend to use Customer Key with Exchange Online and Skype for Business, you need to give permission to Office 365 to use the key vault on behalf of Exchange Online and Skype for Business. Likewise, if you intend to use Customer Key with SharePoint Online and OneDrive for Business, you need to add permission for the Office 365 to use the key vault on behalf of SharePoint Online and OneDrive for Business. To give permission to Office 365, run the **Set-AzureRmKeyVaultAccessPolicy** cmdlet using the following syntax:</span></span> 
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName <Office 365 appID>
  ```

    <span data-ttu-id="a7de5-275">Em que:</span><span class="sxs-lookup"><span data-stu-id="a7de5-275">Where:</span></span>
    
  - <span data-ttu-id="a7de5-276">*vaultname* é o nome do cofre de chaves que você criou.</span><span class="sxs-lookup"><span data-stu-id="a7de5-276">*vaultname* is the name of the key vault you created.</span></span> 
    
  - <span data-ttu-id="a7de5-277">Para o Exchange Online e o Skype for Business, substitua o *Office 365 AppID* por`00000002-0000-0ff1-ce00-000000000000`</span><span class="sxs-lookup"><span data-stu-id="a7de5-277">For Exchange Online and Skype for Business, replace  *Office 365 appID* with `00000002-0000-0ff1-ce00-000000000000`</span></span>
    
  - <span data-ttu-id="a7de5-278">Para o SharePoint Online e o OneDrive for Business, substitua o *Office 365 AppID* por`00000003-0000-0ff1-ce00-000000000000`</span><span class="sxs-lookup"><span data-stu-id="a7de5-278">For SharePoint Online and OneDrive for Business, replace  *Office 365 appID* with `00000003-0000-0ff1-ce00-000000000000`</span></span>
    
  <span data-ttu-id="a7de5-279">Exemplo: definir permissões para o Exchange Online e o Skype for Business:</span><span class="sxs-lookup"><span data-stu-id="a7de5-279">Example: Setting permissions for Exchange Online and Skype for Business:</span></span>
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
  -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000002-0000-0ff1-ce00-000000000000
  ```

  <span data-ttu-id="a7de5-280">Exemplo: definindo permissões para o SharePoint Online e o OneDrive for Business</span><span class="sxs-lookup"><span data-stu-id="a7de5-280">Example: Setting permissions for SharePoint Online and OneDrive for Business</span></span>
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365SP-NA-VaultA1 
  -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000003-0000-0ff1-ce00-000000000000
  ```

### <a name="enable-and-then-confirm-soft-delete-on-your-key-vaults"></a><span data-ttu-id="a7de5-281">Habilitar e confirmar a exclusão reversível nos seus principais cofres</span><span class="sxs-lookup"><span data-stu-id="a7de5-281">Enable and then confirm soft delete on your key vaults</span></span>
<span data-ttu-id="a7de5-282"><a name="SoftDelete"> </a></span><span class="sxs-lookup"><span data-stu-id="a7de5-282"></span></span>

<span data-ttu-id="a7de5-p134">Quando você pode recuperar rapidamente suas chaves, é menos provável que haja uma interrupção de serviço estendido devido a chaves acidentalmente ou excluídas de forma mal-intencionada. Você precisa habilitar essa configuração, conhecida como exclusão reVersível, antes de poder usar suas chaves com a chave do cliente. Habilitar a exclusão reVersível permite recuperar chaves ou cofres dentro de 90 dias de exclusão sem precisar restaurá-los do backup.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p134">When you can quickly recover your keys, you are less likely to experience an extended service outage due to accidentally or maliciously deleted keys. You need to enable this configuration, referred to as Soft Delete, before you can use your keys with Customer Key. Enabling Soft Delete allows you to recover keys or vaults within 90 days of deletion without having to restore them from backup.</span></span>
  
<span data-ttu-id="a7de5-286">Para habilitar a exclusão reVersível nos seus cofres de chaves, conclua estas etapas:</span><span class="sxs-lookup"><span data-stu-id="a7de5-286">To enable Soft Delete on your key vaults, complete these steps:</span></span>
  
1. <span data-ttu-id="a7de5-p135">Faça logon em sua assinatura do Azure com o Windows PowerShell. Para obter instruções, consulte [fazer logon com o Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps).</span><span class="sxs-lookup"><span data-stu-id="a7de5-p135">Log in to your Azure subscription with Windows Powershell. For instructions, see [Log in with Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps).</span></span>
    
2. <span data-ttu-id="a7de5-p136">Execute o cmdlet [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/azurerm.keyvault/get-azurermkeyvault) . Neste exemplo, o *cofre* é o nome do cofre de chaves para o qual você está habilitando a exclusão reversível:</span><span class="sxs-lookup"><span data-stu-id="a7de5-p136">Run the [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/azurerm.keyvault/get-azurermkeyvault) cmdlet. In this example, *vaultname* is the name of the key vault for which you are enabling soft delete:</span></span> 
    
   ```
   $v = Get-AzureRmKeyVault -VaultName <vaultname>
   $r = Get-AzureRmResource -ResourceId $v.ResourceId
   $r.Properties | Add-Member -MemberType NoteProperty -Name enableSoftDelete -Value 'True'
   Set-AzureRmResource -ResourceId $r.ResourceId -Properties $r.Properties
   ``` 
    
3. <span data-ttu-id="a7de5-p137">Confirmar se a exclusão reversível está configurada para o cofre de chaves executando o cmdlet **Get-AzureRmKeyVault** . Se a exclusão reversível estiver configurada corretamente para o cofre de chaves, a exclusão reVersível será habilitada? Propriedade retorna um valor **true**:</span><span class="sxs-lookup"><span data-stu-id="a7de5-p137">Confirm soft delete is configured for the key vault by running the **Get-AzureRmKeyVault** cmdlet. If soft delete is configured properly for the key vault, then the  Soft Delete Enabled? property returns a value of **True**:</span></span> 
    
   ```
   Get-AzureRmKeyVault -VaultName <vaultname> | fl
   ```

   
    
### <a name="add-a-key-to-each-key-vault-either-by-creating-or-importing-a-key"></a><span data-ttu-id="a7de5-293">Adicionar uma chave a cada cofre de chaves criando ou importando uma chave</span><span class="sxs-lookup"><span data-stu-id="a7de5-293">Add a key to each key vault either by creating or importing a key</span></span>
<span data-ttu-id="a7de5-294"><a name="AddKeystoKeyVault"> </a></span><span class="sxs-lookup"><span data-stu-id="a7de5-294"></span></span>

<span data-ttu-id="a7de5-p138">Há duas maneiras de adicionar chaves a um Azure Key Vault; Você pode criar uma chave diretamente no compartimento de chaves ou pode importar uma chave. A criação de uma chave diretamente no cofre de chaves é o método menos complicado, enquanto a importação de uma chave fornece total controle sobre como a chave é gerada.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p138">There are two ways to add keys to an Azure Key Vault; you can create a key directly in Key Vault, or you can import a key. Creating a key directly in Key Vault is the less complicated method, while importing a key provides total control over how the key is generated.</span></span>
  
<span data-ttu-id="a7de5-297">Para criar uma chave diretamente no seu cofre de chaves, execute o cmdlet [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="a7de5-297">To create a key directly in your key vault, run the [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey) cmdlet as follows:</span></span> 
  
```
Add-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname> -Destination <HSM|Software> -KeyOps wrapKey,unwrapKey
```

<span data-ttu-id="a7de5-298">Em que:</span><span class="sxs-lookup"><span data-stu-id="a7de5-298">Where:</span></span>
  
-  <span data-ttu-id="a7de5-299">*compartimentalizaname* é o nome do cofre de chaves em que você deseja criar a chave.</span><span class="sxs-lookup"><span data-stu-id="a7de5-299">*vaultname*  is the name of the key vault in which you want to create the key.</span></span> 
    
-  <span data-ttu-id="a7de5-300">*KeyName* é o nome que você deseja dar à nova chave.</span><span class="sxs-lookup"><span data-stu-id="a7de5-300">*keyname*  is the name you want to give the new key.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="a7de5-p139">Chaves de nome usando uma Convenção de nomenclatura semelhante, conforme descrito acima para os principais cofres. Dessa forma, em ferramentas que mostram apenas o nome da chave, a cadeia de caracteres é autodescritivo.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p139">Name keys using a similar naming convention as described above for key vaults. This way, in tools that show only the key name, the string is self-describing.</span></span> 
  
- <span data-ttu-id="a7de5-303">Se você pretende proteger a chave com um HSM, certifique-se de especificar o **HSM** como o valor do parâmetro _Destination_ , caso contrário, especifique **software**.</span><span class="sxs-lookup"><span data-stu-id="a7de5-303">If you intend to protect the key with an HSM, ensure that you specify **HSM** as the value of the  _Destination_ parameter, otherwise, specify **Software**.</span></span>
    
<span data-ttu-id="a7de5-304">Por exemplo,</span><span class="sxs-lookup"><span data-stu-id="a7de5-304">For example,</span></span>
  
```
Add-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -Destination Software -KeyOps wrapKey,unwrapKey
```

<span data-ttu-id="a7de5-305">Para importar uma chave diretamente para o seu cofre de chaves, você precisa ter um módulo de segurança de hardware do Thales nShield.</span><span class="sxs-lookup"><span data-stu-id="a7de5-305">To import a key directly into your key vault, you need to have a Thales nShield Hardware Security Module.</span></span>
  
<span data-ttu-id="a7de5-306">Algumas organizações preferem essa abordagem para estabelecer o comprovante de suas chaves, e o método também fornece o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a7de5-306">Some organizations prefer this approach to establish the provenance of their keys, and the this method also provides the following:</span></span>
  
- <span data-ttu-id="a7de5-307">O conjunto de ferramentas usado para importação inclui atestado de Thales que a chave de troca de chave (KEK) que é usada para criptografar a chave gerada não é exportável e é gerada dentro de um HSM autêntico que foi fabricado pela Thales.</span><span class="sxs-lookup"><span data-stu-id="a7de5-307">The toolset used for import includes attestation from Thales that the Key Exchange Key (KEK) that is used to encrypt the key you generate is not exportable and is generated inside a genuine HSM that was manufactured by Thales.</span></span>
    
- <span data-ttu-id="a7de5-p140">O conjunto de ferramentas inclui atestado do Thales que o mundo de segurança do Azure Key Vault também foi gerado em um HSM autêntico fabricado pela Thales. Esse atestado comprova que a Microsoft também está usando o hardware genuíno Thales.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p140">The toolset includes attestation from Thales that the Azure Key Vault security world was also generated on a genuine HSM manufactured by Thales. This attestation proves to you that Microsoft is also using genuine Thales hardware.</span></span>
    
<span data-ttu-id="a7de5-p141">Verifique com o grupo de segurança para determinar se os atestado acima são necessários. Para obter etapas detalhadas para criar uma chave no local e importá-la para o seu cofre de chaves, consulte [como gerar e transferir chaves protegidas por HSM para o Azure Key Vault](https://azure.microsoft.com/documentation/articles/key-vault-hsm-protected-keys/). Use as instruções do Azure para criar uma chave em cada cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p141">Check with your security group to determine if the above attestations are required. For detailed steps to create a key on-premises and import it into your key vault, see [How to generate and transfer HSM-protected keys for Azure Key Vault](https://azure.microsoft.com/documentation/articles/key-vault-hsm-protected-keys/). Use the Azure instructions to create a key in each key vault.</span></span>
  
### <a name="check-the-recovery-level-of-your-keys"></a><span data-ttu-id="a7de5-313">Verificar o nível de recuperação de suas chaves</span><span class="sxs-lookup"><span data-stu-id="a7de5-313">Check the recovery level of your keys</span></span>
<span data-ttu-id="a7de5-314"><a name="CheckKeyRecoveryLevel"> </a></span><span class="sxs-lookup"><span data-stu-id="a7de5-314"></span></span>

<span data-ttu-id="a7de5-p142">O Office 365 requer que a assinatura do Azure Key Vault esteja definida como não cancelar e que as chaves usadas pela chave do cliente tenham a exclusão reversível habilitada. Você pode confirmar isso examinando o nível de recuperação nas chaves.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p142">Office 365 requires that the Azure Key Vault subscription is set to Do Not Cancel and that the keys used by Customer Key have soft delete enabled. You can confirm this by looking at the recovery level on your keys.</span></span>
  
<span data-ttu-id="a7de5-317">Para verificar o nível de recuperação de uma chave, no PowerShell do Azure, execute o cmdlet Get-AzureKeyVaultKey da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="a7de5-317">To check the recovery level of a key, in Azure PowerShell, run the Get-AzureKeyVaultKey cmdlet as follows:</span></span>
  
```
(Get-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname>).Attributes 
```

<span data-ttu-id="a7de5-318">Se a propriedade de _nível de recuperação_ retornar algo diferente de um valor de **recuperável + ProtectedSubscription**, será necessário revisar este tópico e verificar se você seguiu todas as etapas para colocar a assinatura na lista não cancelar e que você tem a exclusão reversível habilitada em cada um dos seus compartimentos de chave.</span><span class="sxs-lookup"><span data-stu-id="a7de5-318">If the  _Recovery Level_ property returns anything other than a value of **Recoverable+ProtectedSubscription**, you will need to review this topic and ensure that you have followed all of the steps to put the subscription on the Do Not Cancel list and that you have soft delete enabled on each of your key vaults.</span></span>
  
### <a name="backup-azure-key-vault"></a><span data-ttu-id="a7de5-319">Backup do Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="a7de5-319">Backup Azure Key Vault</span></span>
<span data-ttu-id="a7de5-320"><a name="BackupAzureKeyVaultkeys"> </a></span><span class="sxs-lookup"><span data-stu-id="a7de5-320"></span></span>

<span data-ttu-id="a7de5-p143">Imediatamente após a criação ou qualquer alteração em uma chave, execute um backup e armazene cópias do backup, tanto online quanto offline. As cópias offline não devem ser conectadas a qualquer rede, como em uma instalação física segura ou de armazenamento comercial. Pelo menos uma cópia do backup deve ser armazenada em um local que será acessível em caso de desastre. Os blobs de backup são o único meio de restaurar o material chave caso uma chave de compartimento de chave seja permanentemente destruída ou não seja processada. As chaves que são externas para o Azure Key Vault e foram importadas para o Azure Key Vault não se qualificam como um backup porque os metadados necessários para a chave do cliente usar a chave não existem com a chave externa. Somente um backup obtido do Azure Key Vault pode ser usado para operações de restauração com a chave do cliente. Portanto, é essencial que um backup do Azure Key Vault seja feito depois que uma chave é carregada ou criada.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p143">Immediately following creation or any change to a key, perform a backup and store copies of the backup, both online and offline. Offline copies should not be connected to any network, such as in a physical safe or commercial storage facility. At least one copy of the backup should be stored in a location that will be accessible in the event of a disaster. The backup blobs are the sole means of restoring key material should a Key Vault key be permanently destroyed or otherwise rendered inoperable. Keys that are external to Azure Key Vault and were imported to Azure Key Vault do not qualify as a backup because the metadata necessary for Customer Key to use the key does not exist with the external key. Only a backup taken from Azure Key Vault can be used for restore operations with Customer Key. Therefore, it is essential that a backup of Azure Key Vault be made once a key is uploaded or created.</span></span>
  
<span data-ttu-id="a7de5-328">Para criar um backup de uma chave do Azure Key Vault, execute o cmdlet [backup-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Backup-AzureKeyVaultKey) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="a7de5-328">To create a backup of an Azure Key Vault key, run the [Backup-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Backup-AzureKeyVaultKey) cmdlet as follows:</span></span>
```
Backup-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname> 
-OutputFile <filename .backup>

```

<span data-ttu-id="a7de5-329">Verifique se o arquivo de saída usa o `.backup`sufixo.</span><span class="sxs-lookup"><span data-stu-id="a7de5-329">Ensure that your output file uses the suffix  `.backup`.</span></span>
  
<span data-ttu-id="a7de5-p144">O arquivo de saída resultante deste cmdlet é criptografado e não pode ser usado fora do Azure Key Vault. O backup pode ser restaurado somente para a assinatura do Azure a partir da qual o backup foi feito.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p144">The output file resulting from this cmdlet is encrypted and cannot be used outside of Azure Key Vault. The backup can be restored only to the Azure subscription from which the backup was taken.</span></span>
  
> [!TIP]
> <span data-ttu-id="a7de5-p145">Para o arquivo de saída, escolha uma combinação de nome de cofre e nome de chave. Isso fará com que o nome do arquivo seja autodescritivo. Também garantirá que os nomes de arquivo de backup não colidem.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p145">For the output file, choose a combination of your vault name and key name. This will make the file name self-describing. It will also ensure that backup file names do not collide.</span></span> 
  
<span data-ttu-id="a7de5-335">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="a7de5-335">For example:</span></span>
  
```
Backup-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -OutputFile Contoso-O365EX-NA-VaultA1-Key001-Backup-20170802.backup
```

### <a name="validate-azure-key-vault-configuration-settings"></a><span data-ttu-id="a7de5-336">Validar definições de configuração do Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="a7de5-336">Validate Azure Key Vault configuration settings</span></span>
<span data-ttu-id="a7de5-337"><a name="Validateconfiguration"> </a></span><span class="sxs-lookup"><span data-stu-id="a7de5-337"></span></span>

<span data-ttu-id="a7de5-p146">Executar a validação antes de usar chaves em uma DEP é opcional, mas altamente recomendado. Em particular, se você usar as etapas para configurar suas chaves e cofres diferentes dos descritos neste tópico, você deve validar a integridade dos recursos do Azure Key Vault antes de configurar a chave do cliente.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p146">Performing validation before using keys in a DEP is optional, but highly recommended. In particular, if you use steps to set up your keys and vaults other than the ones described in this topic, you should validate the health of your Azure Key Vault resources before you configure Customer Key.</span></span>
  
<span data-ttu-id="a7de5-340">Para verificar se as chaves têm as operações Get, wrapKey e unwrapKey habilitadas:</span><span class="sxs-lookup"><span data-stu-id="a7de5-340">To verify that your keys have get, wrapKey, and unwrapKey operations enabled:</span></span>
  
<span data-ttu-id="a7de5-341">Execute o cmdlet [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureRmKeyVault) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="a7de5-341">Run the [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureRmKeyVault) cmdlet as follows:</span></span> 
  
```
Get-AzureRMKeyVault -VaultName <vaultname>
```

<span data-ttu-id="a7de5-p147">Na saída, procure a política de acesso e a identidade do Exchange Online (GUID) ou a identidade do SharePoint Online (GUID), conforme apropriado. Todas as três das permissões acima devem ser mostradas em permissões para chaves.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p147">In the output, look for the Access Policy and for the Exchange Online identity (GUID) or the SharePoint Online identity (GUID) as appropriate. All three of the above permissions must be shown under Permissions to Keys.</span></span>
  
<span data-ttu-id="a7de5-344">Se a configuração da política de acesso estiver incorreta, execute o cmdlet Set-AzureRmKeyVaultAccessPolicy da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="a7de5-344">If the access policy configuration is incorrect, run the Set-AzureRmKeyVaultAccessPolicy cmdlet as follows:</span></span>
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName <Office 365 appID>
```

<span data-ttu-id="a7de5-345">Por exemplo, para o Exchange Online e o Skype for Business:</span><span class="sxs-lookup"><span data-stu-id="a7de5-345">For example, for Exchange Online and Skype for Business:</span></span>
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
-PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000002-0000-0ff1-ce00-000000000000
```

<span data-ttu-id="a7de5-346">Por exemplo, para o SharePoint Online e o OneDrive for Business:</span><span class="sxs-lookup"><span data-stu-id="a7de5-346">For example, for SharePoint Online and OneDrive for Business:</span></span>
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365SP-NA-VaultA1 
-PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName TBD
```

<span data-ttu-id="a7de5-347">Para verificar se uma data de vencimento não está definida para suas chaves, execute o cmdlet [Get-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureKeyVaultKey) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="a7de5-347">To verify that an expiration date is not set for your keys run the [Get-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureKeyVaultKey) cmdlet as follows:</span></span> 
  
```
Get-AzureKeyVaultKey -VaultName <vaultname> 
```

<span data-ttu-id="a7de5-p148">Uma chave expirada não pode ser usada pela chave do cliente e as operações tentadas com uma chave expirada falharão e possivelmente resultarão em uma interrupção de serviço. É altamente recomendável que as teclas usadas com a chave do cliente não tenham uma data de validade. Uma data de vencimento, uma vez definida, não pode ser removida, mas pode ser alterada para uma data diferente. Se for necessário usar uma chave que tenha uma data de expiração definida, altere o valor de expiração para 12/31/9999. As chaves com uma data de expiração definida para uma data diferente de 12/31/9999 não passarão pela validação do Office 365.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p148">An expired key cannot be used by Customer Key and operations attempted with an expired key will fail, and possibly result in a service outage. We strongly recommend that keys used with Customer Key do not have an expiration date. An expiration date, once set, cannot be removed, but can be changed to a different date. If a key must be used that has an expiration date set, change the expiration value to 12/31/9999. Keys with an expiration date set to a date other than 12/31/9999 will not pass Office 365 validation.</span></span>
  
<span data-ttu-id="a7de5-353">Para alterar uma data de expiração que tenha sido definida para qualquer valor diferente de 12/31/9999, execute o cmdlet [set-AzureKeyVaultKeyAttribute](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Set-AzureKeyVaultKeyAttribute) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="a7de5-353">To change an expiration date that has been set to any value other than 12/31/9999, run the [Set-AzureKeyVaultKeyAttribute](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Set-AzureKeyVaultKeyAttribute) cmdlet as follows:</span></span> 
  
```
Set-AzureKeyVaultKeyAttribute -VaultName <vaultname> -Name <keyname> 
-Expires (Get-Date -Date "12/31/9999")
```

> [!CAUTION]
> <span data-ttu-id="a7de5-354">Não defina datas de expiração em chaves de criptografia usadas com a chave do cliente.</span><span class="sxs-lookup"><span data-stu-id="a7de5-354">Don't set expiration dates on encryption keys you use with Customer Key.</span></span> 
  
### <a name="obtain-the-uri-for-each-azure-key-vault-key"></a><span data-ttu-id="a7de5-355">Obter o URI para cada chave do Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="a7de5-355">Obtain the URI for each Azure Key Vault key</span></span>
<span data-ttu-id="a7de5-356"><a name="GetKeyURI"> </a></span><span class="sxs-lookup"><span data-stu-id="a7de5-356"></span></span>

<span data-ttu-id="a7de5-p149">Após concluir todas as etapas no Azure para configurar seus principais cofres e adicionar suas chaves, execute o comando a seguir para obter o URI da chave em cada cofre de chaves. Você precisará usar esses URIs ao criar e atribuir cada DEP mais tarde, portanto, salve essas informações em um local seguro. Lembre-se de executar este comando uma vez para cada cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p149">Once you have completed all the steps in Azure to set up your key vaults and added your keys, run the following command to get the URI for the key in each key vault. You will need to use these URIs when you create and assign each DEP later, so save this information in a safe place. Remember to run this command once for each key vault.</span></span>
  
<span data-ttu-id="a7de5-360">No Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="a7de5-360">In Azure PowerShell:</span></span>
  
```
(Get-AzureKeyVaultKey -VaultName <vaultname>).Id
```

## <a name="office-365-setting-up-customer-key-for-exchange-online-and-skype-for-business"></a><span data-ttu-id="a7de5-361">Office 365: configuração da chave do cliente para o Exchange Online e o Skype for Business</span><span class="sxs-lookup"><span data-stu-id="a7de5-361">Office 365: Setting up Customer Key for Exchange Online and Skype for Business</span></span>
<span data-ttu-id="a7de5-362"><a name="AzureSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="a7de5-362"></span></span>

<span data-ttu-id="a7de5-p150">Antes de começar, verifique se você concluiu as tarefas necessárias para configurar o Azure Key Vault. Veja [tarefas completas no Azure Key Vault e Microsoft FastTrack para](controlling-your-data-using-customer-key.md#AzureSteps) obter informações sobre a chave do cliente.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p150">Before you begin, ensure that you have completed the tasks required to set up Azure Key Vault. See [Complete tasks in Azure Key Vault and Microsoft FastTrack for Customer Key](controlling-your-data-using-customer-key.md#AzureSteps) for information.</span></span> 
  
<span data-ttu-id="a7de5-365">Para configurar a chave do cliente para o Exchange Online e o Skype for Business, você precisará executar estas etapas conectando-se remotamente ao Exchange Online com o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a7de5-365">To set up Customer Key for Exchange Online and Skype for Business, you will need to perform these steps by remotely connecting to Exchange Online with Windows PowerShell.</span></span>
  
### <a name="create-a-data-encryption-policy-dep-for-use-with-exchange-online-and-skype-for-business"></a><span data-ttu-id="a7de5-366">Criar uma DEP (política de criptografia de dados) para uso com o Exchange Online e o Skype for Business</span><span class="sxs-lookup"><span data-stu-id="a7de5-366">Create a data encryption policy (DEP) for use with Exchange Online and Skype for Business</span></span>
<span data-ttu-id="a7de5-367"><a name="CreateDEP4EXOSkype"> </a></span><span class="sxs-lookup"><span data-stu-id="a7de5-367"></span></span>

<span data-ttu-id="a7de5-p151">Uma DEP é associada a um conjunto de chaves armazenadas no Azure Key Vault. Você atribui uma DEP a uma caixa de correio no Office 365. O Office 365 usará as chaves identificadas na política para criptografar a caixa de correio. Para criar a DEP, você precisará dos URIs de compartimento de chave obtidos anteriormente. Consulte [obter o URI de cada chave do Azure Key Vault](controlling-your-data-using-customer-key.md#GetKeyURI) para obter instruções.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p151">A DEP is associated with a set of keys stored in Azure Key Vault. You assign a DEP to a mailbox in Office 365. Office 365 will then use the keys identified in the policy to encrypt the mailbox. To create the DEP, you need the Key Vault URIs you obtained earlier. See [Obtain the URI for each Azure Key Vault key](controlling-your-data-using-customer-key.md#GetKeyURI) for instructions.</span></span> 
  
<span data-ttu-id="a7de5-p152">Esquecer! Ao criar uma DEP, você especifica duas chaves que residem em dois cofres de chaves diferentes do Azure. Verifique se essas chaves estão localizadas em duas regiões separadas do Azure para garantir a redundância geográfica.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p152">Remember! When you create a DEP, you specify two keys that reside in two different Azure Key Vaults. Ensure that these keys are located in two separate Azure regions to ensure geo-redundancy.</span></span>
  
<span data-ttu-id="a7de5-376">Para criar a DEP, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="a7de5-376">To create the DEP, follow these steps:</span></span>
  
1. <span data-ttu-id="a7de5-377">No computador local, usando uma conta corporativa ou de estudante que tenha permissões de administrador global em sua organização do Office 365, [Conecte-se ao PowerShell do Exchange Online](https://technet.microsoft.com/en-us/library/jj984289%28v=exchg.160%29.aspx) abrindo o Windows PowerShell e executando o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="a7de5-377">On your local computer, using a work or school account that has global administrator permissions in your Office 365 organization, [connect to Exchange Online PowerShell](https://technet.microsoft.com/en-us/library/jj984289%28v=exchg.160%29.aspx) by opening Windows PowerShell and running the following command.</span></span> 
    
   ```
   $UserCredential = Get-Credential
   ```

2. <span data-ttu-id="a7de5-378">Na caixa de diálogo solicitação de credencial do Windows PowerShell, insira as informações da conta corporativa ou de estudante, clique em **OK**e, em seguida, insira o comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="a7de5-378">In the Windows PowerShell Credential Request dialog box, enter your work or school account information, click **OK**, and then enter the following command.</span></span> 
    
   ```
   $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://outlook.office365.com/powershell-liveid/ -Credential $UserCredential -Authentication Basic -AllowRedirection
   ```

3. <span data-ttu-id="a7de5-379">Execute o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="a7de5-379">Run the following command.</span></span>
    
   ```
   Import-PSSession $Session
   ```

4. <span data-ttu-id="a7de5-380">Para criar uma DEP, use o cmdlet New-DataEncryptionPolicy digitando o comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="a7de5-380">To create a DEP, use the New-DataEncryptionPolicy cmdlet by typing the following command.</span></span>
    
   ```
   New-DataEncryptionPolicy -Name <PolicyName> -Description "PolicyDescription " -AzureKeyIDs <KeyVaultURI1>, <KeyVaultURI2>
   ```

   <span data-ttu-id="a7de5-381">Em que:</span><span class="sxs-lookup"><span data-stu-id="a7de5-381">Where:</span></span>
    
   -  <span data-ttu-id="a7de5-p153">*PolicyName* é o nome que você deseja usar para a política. Os nomes não podem conter espaços. Por exemplo, USA_mailboxes.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p153">*PolicyName*  is the name you want to use for the policy. Names cannot contain spaces. For example, USA_mailboxes.</span></span> 
    
   -  <span data-ttu-id="a7de5-p154">*PolicyDescription* é uma descrição amigável da política que ajudará você a se lembrar do que a política é para o. Você pode incluir espaços na descrição. Por exemplo, chave raiz para caixas de correio nos EUA e seus territórios.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p154">*PolicyDescription*  is a user friendly description of the policy that will help you remember what the policy is for. You can include spaces in the description. For example, Root key for mailboxes in USA and its territories.</span></span> 
    
   -  <span data-ttu-id="a7de5-p155">*KeyVaultURI1* é o URI da primeira chave na política. Por exemplo, https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p155">*KeyVaultURI1*  is the URI for the first key in the policy. For example, https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01.</span></span> 
    
   -  <span data-ttu-id="a7de5-p156">*KeyVaultURI2* é o URI da segunda chave na política. Por exemplo, https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02. Separe os dois URIs por uma vírgula e um espaço.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p156">*KeyVaultURI2*  is the URI for the second key in the policy. For example, https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02. Separate the two URIs by a comma and a space.</span></span> 
    
   <span data-ttu-id="a7de5-393">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="a7de5-393">Example:</span></span>
  
   ```
   New-DataEncryptionPolicy -Name USA_mailboxes -Description "Root key for mailboxes in USA and its territories" -AzureKeyIDs https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01, https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02
   ```

### <a name="assign-a-dep-to-a-mailbox"></a><span data-ttu-id="a7de5-394">Atribuir uma DEP a uma caixa de correio</span><span class="sxs-lookup"><span data-stu-id="a7de5-394">Assign a DEP to a mailbox</span></span>
<span data-ttu-id="a7de5-395"><a name="assignDEPtomailbox"> </a></span><span class="sxs-lookup"><span data-stu-id="a7de5-395"></span></span>

<span data-ttu-id="a7de5-p157">Atribua a DEP a uma caixa de correio usando o cmdlet Set-Mailbox. Depois de atribuir a política, o Office 365 pode criptografar a caixa de correio com a chave designada no DEP.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p157">Assign the DEP to a mailbox by using the Set-Mailbox cmdlet. Once you assign the policy, Office 365 can encrypt the mailbox with the key designated in the DEP.</span></span>
  
```
Set-Mailbox -Identity <MailboxIdParameter> -DataEncryptionPolicy <PolicyName>
```

<span data-ttu-id="a7de5-p158">Onde *MailboxIdParameter* especifica uma caixa de correio. Para obter mais informações sobre o cmdlet Set-Mailbox, consulte [Set-Mailbox](https://technet.microsoft.com/library/bb123981%28v=exchg.160%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="a7de5-p158">Where *MailboxIdParameter* specifies a mailbox. For more information about the Set-Mailbox cmdlet, see [Set-Mailbox](https://technet.microsoft.com/library/bb123981%28v=exchg.160%29.aspx).</span></span>
  
### <a name="validate-mailbox-encryption"></a><span data-ttu-id="a7de5-400">Validar criptografia de caixa de correio</span><span class="sxs-lookup"><span data-stu-id="a7de5-400">Validate mailbox encryption</span></span>
<span data-ttu-id="a7de5-401"><a name="validatemailboxencryption"> </a></span><span class="sxs-lookup"><span data-stu-id="a7de5-401"></span></span>

<span data-ttu-id="a7de5-p159">Criptografar uma caixa de correio pode levar algum tempo. Para a primeira atribuição de política de tempo, a caixa de correio também deve concluir a movimentação de um banco de dados para outro antes que o serviço possa criptografar a caixa de correio. Recomendamos que você aguarde 72 horas antes de tentar validar a criptografia após alterar uma DEP ou a primeira vez em que você atribui uma DEP a uma caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p159">Encrypting a mailbox can take some time. For first time policy assignment, the mailbox must also complete the move from one database to another before the service can encrypt the mailbox. We recommend that you wait 72 hours before you attempt to validate encryption after you change a DEP or the first time you assign a DEP to a mailbox.</span></span>
  
<span data-ttu-id="a7de5-405">Use o cmdlet Get-MailboxStatistics para determinar se uma caixa de correio está criptografada.</span><span class="sxs-lookup"><span data-stu-id="a7de5-405">Use the Get-MailboxStatistics cmdlet to determine if a mailbox is encrypted.</span></span>
  
```
Get-MailboxStatistics -Identity <GeneralMailboxOrMailUserIdParameter> | fl IsEncrypted
```

<span data-ttu-id="a7de5-406">A propriedade isEncrypted retornará um valor **true** se a caixa de correio for criptografada e um valor **false** se a caixa de correio não estiver criptografada.</span><span class="sxs-lookup"><span data-stu-id="a7de5-406">The IsEncrypted property returns a value of **true** if the mailbox is encrypted and a value of **false** if the mailbox is not encrypted.</span></span> 

<span data-ttu-id="a7de5-p160">O tempo para concluir movimentações de caixa de correio depende do número de caixas de correio às quais você atribui uma DEP pela primeira vez, bem como o tamanho das caixas de correio. Se as caixas de correio não foram criptografadas após uma semana a partir do momento em que você atribuiu a DEP, inicie uma movimentação de caixa de correio para as caixas de correio não criptografadas usando o cmdlet New-MoveRequest.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p160">The time to complete mailbox moves depends on the number of mailboxes to which you assign a DEP for the first time, as well as the size of the mailboxes. If the mailboxes have not been encrypted after a week from the time you assigned the DEP, initiate a mailbox move for the unencrypted mailboxes by using the New-MoveRequest cmdlet.</span></span>

```
New-MoveRequest <mailbox alias>
``` 

## <a name="office-365-setting-up-customer-key-for-sharepoint-online-and-onedrive-for-business"></a><span data-ttu-id="a7de5-409">Office 365: configuração da chave do cliente para o SharePoint Online e o OneDrive for Business</span><span class="sxs-lookup"><span data-stu-id="a7de5-409">Office 365: Setting up Customer Key for SharePoint Online and OneDrive for Business</span></span>
<span data-ttu-id="a7de5-410"><a name="AzureSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="a7de5-410"></span></span>

<span data-ttu-id="a7de5-p161">Antes de começar, verifique se você concluiu as tarefas necessárias para configurar o Azure Key Vault. Veja [tarefas completas no Azure Key Vault e Microsoft FastTrack para](controlling-your-data-using-customer-key.md#AzureSteps) obter informações sobre a chave do cliente.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p161">Before you begin, ensure that you have completed the tasks required to set up Azure Key Vault. See [Complete tasks in Azure Key Vault and Microsoft FastTrack for Customer Key](controlling-your-data-using-customer-key.md#AzureSteps) for information.</span></span> 
  
<span data-ttu-id="a7de5-413">Para configurar a chave do cliente para o SharePoint Online e o OneDrive for Business, você precisará executar estas etapas conectando-se remotamente ao SharePoint Online com o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a7de5-413">To set up Customer Key for SharePoint Online and OneDrive for Business, you will need to perform these steps by remotely connecting to SharePoint Online with Windows PowerShell.</span></span>
  
### <a name="create-a-data-encryption-policy-dep-for-each-sharepoint-online-and-onedrive-for-business-geo"></a><span data-ttu-id="a7de5-414">Criar uma DEP (política de criptografia de dados) para cada Geografia do SharePoint Online e do OneDrive for Business</span><span class="sxs-lookup"><span data-stu-id="a7de5-414">Create a data encryption policy (DEP) for each SharePoint Online and OneDrive for Business geo</span></span>
<span data-ttu-id="a7de5-415"><a name="CreateDEP4SPOODfB"> </a></span><span class="sxs-lookup"><span data-stu-id="a7de5-415"></span></span>

<span data-ttu-id="a7de5-p162">Uma DEP é associada a um conjunto de chaves armazenadas no Azure Key Vault. Você aplica uma DEP a todos os seus dados em um local geográfico, também chamado de uma geografia. Se você usar o recurso multigeográfico do Office 365 (atualmente em visualização), você pode criar uma DEP por geografia. Se você não estiver usando a geografia, é possível criar uma DEP no Office 365 para uso com o SharePoint Online e o OneDrive for Business. O Office 365 usará as chaves identificadas na DEP para criptografar seus dados nessa geografia. Para criar a DEP, você precisará dos URIs de compartimento de chave obtidos anteriormente. Consulte [obter o URI de cada chave do Azure Key Vault](controlling-your-data-using-customer-key.md#GetKeyURI) para obter instruções.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p162">A DEP is associated with a set of keys stored in Azure Key Vault. You apply a DEP to all of your data in one geographic location, also called a geo. If you use the multi-geo feature of Office 365 (currently in Preview), you can create one DEP per geo. If you are not using multi-geo, you can create one DEP in Office 365 for use with SharePoint Online and OneDrive for Business. Office 365 will then use the keys identified in the DEP to encrypt your data in that geo. To create the DEP, you need the Key Vault URIs you obtained earlier. See [Obtain the URI for each Azure Key Vault key](controlling-your-data-using-customer-key.md#GetKeyURI) for instructions.</span></span> 
  
<span data-ttu-id="a7de5-p163">Esquecer! Ao criar uma DEP, você especifica duas chaves que residem em dois cofres de chaves diferentes do Azure. Verifique se essas chaves estão localizadas em duas regiões separadas do Azure para garantir a redundância geográfica.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p163">Remember! When you create a DEP, you specify two keys that reside in two different Azure Key Vaults. Ensure that these keys are located in two separate Azure regions to ensure geo-redundancy.</span></span>
  
<span data-ttu-id="a7de5-426">Para criar uma DEP, você precisa se conectar remotamente ao SharePoint online usando o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a7de5-426">To create a DEP, you need to remotely connect to SharePoint Online by using Windows PowerShell.</span></span>
  
1. <span data-ttu-id="a7de5-427">No computador local, usando uma conta corporativa ou de estudante que tenha permissões de administrador global em sua organização do Office 365, [Conecte-se ao PowerShell do SharePoint Online](https://technet.microsoft.com/library/fp161372.aspx).</span><span class="sxs-lookup"><span data-stu-id="a7de5-427">On your local computer, using a work or school account that has global administrator permissions in your Office 365 organization, [Connect to SharePoint Online Powershell](https://technet.microsoft.com/library/fp161372.aspx).</span></span>
    
2. <span data-ttu-id="a7de5-428">No Shell de gerenciamento do Microsoft SharePoint Online, execute o cmdlet [Register-SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843950.aspx) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="a7de5-428">In the Microsoft SharePoint Online Management Shell, run the [Register-SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843950.aspx) cmdlet as follows:</span></span> 
    
   ```
   Register-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl> -PrimaryKeyVaultName <PrimaryKeyVaultName> -PrimaryKeyName <PrimaryKeyName> -PrimaryKeyVersion <PrimaryKeyVersion> -SecondaryKeyVaultName <SecondaryKeyVaultName> -SecondaryKeyName <SecondaryKeyName> -SecondaryKeyVersion <SecondaryKeyVersion>
   ```

   <span data-ttu-id="a7de5-p164">Quando você registra a DEP, a criptografia começa nos dados na geografia. Isso pode levar algum tempo.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p164">When you register the DEP, encryption begins on the data in the geo. This can take some time.</span></span>
    
### <a name="validate-encryption-of-group-sites-team-sites-and-onedrive-for-business"></a><span data-ttu-id="a7de5-431">Validar a criptografia de sites de grupo, sites de equipe e o OneDrive for Business</span><span class="sxs-lookup"><span data-stu-id="a7de5-431">Validate encryption of Group Sites, Team Sites, and OneDrive for Business</span></span>
<span data-ttu-id="a7de5-432"><a name="validateencryptionSPO"> </a></span><span class="sxs-lookup"><span data-stu-id="a7de5-432"></span></span>

<span data-ttu-id="a7de5-433">Você pode verificar o status da criptografia executando o cmdlet Get-SPODataEncryptionPolicy da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="a7de5-433">You can check on the status of encryption by running the Get-SPODataEncryptionPolicy cmdlet as follows:</span></span>
  
```
Get-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl>
```

<span data-ttu-id="a7de5-434">A saída deste cmdlet inclui:</span><span class="sxs-lookup"><span data-stu-id="a7de5-434">The output from this cmdlet includes:</span></span>
  
- <span data-ttu-id="a7de5-435">O URI da chave primária.</span><span class="sxs-lookup"><span data-stu-id="a7de5-435">The URI of the primary key.</span></span>
    
- <span data-ttu-id="a7de5-436">O URI da chave secundária.</span><span class="sxs-lookup"><span data-stu-id="a7de5-436">The URI of the secondary key.</span></span>
    
- <span data-ttu-id="a7de5-p165">O status de criptografia para a geografia. Os Estados possíveis incluem:</span><span class="sxs-lookup"><span data-stu-id="a7de5-p165">The encryption status for the geo. Possible states include:</span></span>
    
  - <span data-ttu-id="a7de5-439">Não **registrado:** A criptografia de chave do cliente ainda não foi aplicada.</span><span class="sxs-lookup"><span data-stu-id="a7de5-439">**Unregistered:** Customer Key encryption has not yet been applied.</span></span> 
    
  - <span data-ttu-id="a7de5-p166">**Registro:** A criptografia da chave do cliente foi aplicada e seus arquivos estão em processo de criptografia. Se sua geografia estiver nesse estado, você também verá informações sobre a porcentagem de sites na geografia que podem ser concluídas para que você possa monitorar o andamento da criptografia.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p166">**Registering:** Customer Key encryption has been applied and your files are in the process of being encrypted. If your geo is in this state, you'll also be shown information on what percentage of sites in the geo are complete so that you can monitor encryption progress.</span></span> 
    
  - <span data-ttu-id="a7de5-442">**Registrado:** A criptografia da chave do cliente foi aplicada e todos os arquivos em todos os sites foram criptografados.</span><span class="sxs-lookup"><span data-stu-id="a7de5-442">**Registered:** Customer Key encryption has been applied, and all files in all sites have been encrypted.</span></span> 
    
  - <span data-ttu-id="a7de5-p167">**Sem interrupção:** Um rolo de chave está em andamento. Se sua geografia estiver nesse estado, você também verá informações sobre a porcentagem de sites que concluíram a operação do registro principal para que você possa monitorar o progresso.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p167">**Rolling:** A key roll is in progress. If your geo is in this state, you'll also be shown information on what percentage of sites have completed the key roll operation so that you can monitor progress.</span></span> 
    
## <a name="managing-customer-key-for-office-365"></a><span data-ttu-id="a7de5-445">Gerenciando a chave do cliente para o Office 365</span><span class="sxs-lookup"><span data-stu-id="a7de5-445">Managing Customer Key for Office 365</span></span>
<span data-ttu-id="a7de5-446"><a name="ManageCustomerKey"> </a></span><span class="sxs-lookup"><span data-stu-id="a7de5-446"></span></span>

<span data-ttu-id="a7de5-447">Depois de configurar a chave do cliente para o Office 365, você pode executar essas tarefas de gerenciamento adicionais.</span><span class="sxs-lookup"><span data-stu-id="a7de5-447">After you've set up Customer Key for Office 365, you can perform these additional management tasks.</span></span>
  
- [<span data-ttu-id="a7de5-448">Restaurar chaves do Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="a7de5-448">Restore Azure Key Vault keys</span></span>](controlling-your-data-using-customer-key.md#RestoreAzureKeyVaultKeys)
    
- [<span data-ttu-id="a7de5-449">Reverter ou girar uma chave no Azure Key Vault que você usa com a chave do cliente</span><span class="sxs-lookup"><span data-stu-id="a7de5-449">Rolling or rotating a key in Azure Key Vault that you use with Customer Key</span></span>](controlling-your-data-using-customer-key.md#RollCKkey)
    
- [<span data-ttu-id="a7de5-450">Gerenciar permissões do Key Vault</span><span class="sxs-lookup"><span data-stu-id="a7de5-450">Manage key vault permissions</span></span>](controlling-your-data-using-customer-key.md#Managekeyvaultperms)
    
- [<span data-ttu-id="a7de5-451">Determinar a DEP atribuída a uma caixa de correio</span><span class="sxs-lookup"><span data-stu-id="a7de5-451">Determine the DEP assigned to a mailbox</span></span>](controlling-your-data-using-customer-key.md#DeterminemailboxDEP)
    
### <a name="restore-azure-key-vault-keys"></a><span data-ttu-id="a7de5-452">Restaurar chaves do Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="a7de5-452">Restore Azure Key Vault keys</span></span>
<span data-ttu-id="a7de5-453"><a name="RestoreAzureKeyVaultKeys"> </a></span><span class="sxs-lookup"><span data-stu-id="a7de5-453"></span></span>

<span data-ttu-id="a7de5-p168">Antes de executar uma restauração, use os recursos de recuperação fornecidos pela exclusão reversível. Todas as chaves usadas com a chave do cliente são necessárias para que a exclusão reversível seja habilitada. A exclusão reVersível funciona como uma lixeira e permite a recuperação de até 90 dias sem a necessidade de restauração. A restauração deve ser necessária somente em circunstâncias extremas ou incomuns, por exemplo, se a chave ou o cofre de chaves for perdido. Se for necessário restaurar uma chave para uso com a chave do cliente, no PowerShell do Azure, execute o cmdlet Restore-AzureKeyVaultKey da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="a7de5-p168">Before performing a restore, use the recovery capabilities provided by soft delete. All keys that are used with Customer Key are required to have soft delete enabled. Soft delete acts like a recycle bin and allows recovery for up to 90 days without the need to restore. Restore should only be required in extreme or unusual circumstances, for example if the key or key vault is lost. If you must restore a key for use with Customer Key, in Azure PowerShell, run the Restore-AzureKeyVaultKey cmdlet as follows:</span></span>
  
```
Restore-AzureKeyVaultKey -VaultName <vaultname> -InputFile <filename>
```

<span data-ttu-id="a7de5-459">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="a7de5-459">For example:</span></span>
  
```
Restore-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -InputFile Contoso-O365EX-NA-VaultA1-Key001-Backup-20170802.backup
```

<span data-ttu-id="a7de5-p169">Se já existir uma chave com o mesmo nome no cofre de chaves, a operação de restauração falhará. Restore-AzureKeyVaultKey restaura todas as versões de chave e todos os metadados da chave, incluindo o nome da chave.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p169">If a key with the same name already exists in the key vault, the restore operation will fail. Restore-AzureKeyVaultKey restores all key versions and all metadata for the key including the key name.</span></span>
  
### <a name="rolling-or-rotating-a-key-in-azure-key-vault-that-you-use-with-customer-key"></a><span data-ttu-id="a7de5-462">Reverter ou girar uma chave no Azure Key Vault que você usa com a chave do cliente</span><span class="sxs-lookup"><span data-stu-id="a7de5-462">Rolling or rotating a key in Azure Key Vault that you use with Customer Key</span></span>
<span data-ttu-id="a7de5-463"><a name="RollCKkey"> </a></span><span class="sxs-lookup"><span data-stu-id="a7de5-463"></span></span>

<span data-ttu-id="a7de5-p170">As chaves sem interrupção não são exigidas pelo Azure Key Vault ou pela chave do cliente. Além disso, as chaves protegidas com um HSM são praticamente impossíveis de ser comprometidas. Mesmo que uma chave raiz estivesse na posse de um ator mal-intencionado, não há meios viáveis de usá-lo para descriptografar dados, já que apenas o código do Office 365 sabe como usá-lo. No enTanto, a chave do cliente oferece suporte à substituição de uma chave.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p170">Rolling keys is not required by either Azure Key Vault or by Customer Key. In addition, keys that are protected with an HSM are virtually impossible to compromise. Even if a root key were in the possession of a malicious actor there is no feasible means of using it to decrypt data, since only Office 365 code knows how to use it. However, rolling a key is supported by Customer Key.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="a7de5-p171">Apenas rolo uma chave de criptografia que você usa com a chave do cliente quando existe uma razão técnica clara ou um requisito de conformidade determina que você precisa rolar a chave. Além disso, não exclua chaves que estejam associadas a políticas. Ao rolar suas chaves, haverá conteúdo criptografado com as teclas anteriores. Por exemplo, enquanto as caixas de correio ativas forem criptografadas freqüentemente, inativas, desconectadas e desativadas, as caixas de correio ainda poderão ser criptografadas com as teclas anteriores. O SharePoint Online realiza o backup de conteúdo para fins de restauração e recuperação, para que ainda possa haver conteúdo arquivado usando chaves antigas.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p171">Only roll an encryption key that you use with Customer Key when a clear technical reason exists or a compliance requirement dictates that you have to roll the key. In addition, do not delete any keys that are or were associated with policies. When you roll your keys, there will be content encrypted with the previous keys. For example, while active mailboxes will be re-encrypted frequently, inactive, disconnected, and disabled mailboxes may still be encrypted with the previous keys. SharePoint Online performs backup of content for restore and recovery purposes, so there may still be archived content using older keys. </span></span><br/> <span data-ttu-id="a7de5-p172">Para garantir a segurança de seus dados, o SharePoint Online permitirá que não haja mais de uma operação de registro de chave em andamento por vez. Se quiser rolar as duas chaves em um cofre de chaves, você precisará aguardar a conclusão completa da primeira operação do rolo de chave. Nossa recomendação é escalonar as operações de seu rolo principal em intervalos diferentes, para que isso não seja um problema.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p172">To ensure the safety of your data, SharePoint Online will allow no more than one Key Roll operation to be in progress at a time. If you want to roll both of the keys in a key vault, you'll need to wait for the first key roll operation to fully complete. Our recommendation is to stagger your key roll operations at different intervals, so that this is not an issue.</span></span> 
  
<span data-ttu-id="a7de5-p173">Ao lançar uma chave, você está solicitando uma nova versão de uma chave existente. Para solicitar uma nova versão de uma chave existente, use o mesmo cmdlet, [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey), com a mesma sintaxe que você usou para criar a chave no primeiro lugar.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p173">When you roll a key, you are requesting a new version of an existing key. In order to request a new version of an existing key, you use the same cmdlet, [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey), with the same syntax that you used to create the key in the first place.</span></span>
  
<span data-ttu-id="a7de5-478">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="a7de5-478">For example:</span></span>
  
```
Add-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -Destination HSM -KeyOps @('wrapKey','unwrapKey') -NotBefore (Get-Date -Date "12/27/2016 12:01 AM")
```

<span data-ttu-id="a7de5-p174">Neste exemplo, como uma chave chamada **contoso-O365EX-nd-VaultA1-Key001** já existe no cofre **contoso-O365EX-na-VaultA1** , uma nova versão de chave será criada. A operação adiciona uma nova versão de chave. Essa operação preserva as versões de chave anteriores no histórico de versão da chave, para que os dados anteriormente criptografados com essa chave ainda possam ser descriptografados. Depois de concluir a transferência de qualquer chave associada a uma DEP, você deve executar um cmdlet adicional para garantir que a chave do cliente comece a usar a nova chave.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p174">In this example, since a key named **Contoso-O365EX-NA-VaultA1-Key001** already exists in the **Contoso-O365EX-NA-VaultA1** vault, a new key version will be created. The operation adds a new key version. This operation preserves the previous key versions in the key's version history, so that data previously encrypted with that key can still be decrypted. Once you have completed rolling any key that is associated with a DEP, you must then run an additional cmdlet to ensure Customer Key begins using the new key.</span></span> 
  
#### <a name="enable-exchange-online-and-skype-for-business-to-use-a-new-key-after-you-roll-or-rotate-keys-in-azure-key-vault"></a><span data-ttu-id="a7de5-483">Habilitar o Exchange Online e o Skype for Business usar uma nova chave após rolar ou girar as teclas no Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="a7de5-483">Enable Exchange Online and Skype for Business to use a new key after you roll or rotate keys in Azure Key Vault</span></span>

<span data-ttu-id="a7de5-484">Ao lançar uma das chaves do Azure Key Vault associadas a uma DEP usada com o Exchange Online e o Skype for Business, você deve executar o seguinte comando para atualizar a DEP e habilitar o Office 365 para começar a usar a nova chave.</span><span class="sxs-lookup"><span data-stu-id="a7de5-484">When you roll either of the Azure Key Vault keys associated with a DEP used with Exchange Online and Skype for Business, you must run the following command to update the DEP and enable Office 365 to start using the new key.</span></span>
  
<span data-ttu-id="a7de5-485">Para instruir a chave do cliente a usar a nova chave para criptografar caixas de correio no Office 365, execute o cmdlet Set-DataEncryptionPolicy da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="a7de5-485">To instruct Customer Key to use the new key to encrypt mailboxes in Office 365 run the Set-DataEncryptionPolicy cmdlet as follows:</span></span>
  
```
Set-DataEncryptionPolicy <policyname> -Refresh 
```

<span data-ttu-id="a7de5-p175">Em 48 horas, as caixas de correio ativas criptografadas usando essa política serão associadas à chave atualizada. Use as etapas em [determinar a DEP atribuída a uma caixa de correio](controlling-your-data-using-customer-key.md#DeterminemailboxDEP) para verificar o valor da propriedade DataEncryptionPolicyID da caixa de correio. O valor dessa propriedade será alterado após a aplicação da chave atualizada.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p175">Within 48 hours, the active mailboxes encrypted using this policy will become associated with the updated key. Use the steps in [Determine the DEP assigned to a mailbox](controlling-your-data-using-customer-key.md#DeterminemailboxDEP) to check the value for the DataEncryptionPolicyID property for the mailbox. The value for this property will change once the updated key has been applied.</span></span> 
  
#### <a name="enable-sharepoint-online-and-onedrive-for-business-to-use-a-new-key-after-you-roll-or-rotate-keys-in-azure-key-vault"></a><span data-ttu-id="a7de5-489">Habilitar o SharePoint Online e o OneDrive for Business para usar uma nova chave após rolar ou girar as teclas no Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="a7de5-489">Enable SharePoint Online and OneDrive for Business to use a new key after you roll or rotate keys in Azure Key Vault</span></span>

<span data-ttu-id="a7de5-490">Ao lançar uma das chaves do Azure Key Vault associadas a uma DEP usada com o SharePoint Online e o OneDrive for Business, você deve executar o cmdlet [Update-SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843948.aspx) para atualizar a DEP e habilitar o Office 365 para começar a usar a nova chave.</span><span class="sxs-lookup"><span data-stu-id="a7de5-490">When you roll either of the Azure Key Vault keys associated with a DEP used with SharePoint Online and OneDrive for Business, you must run the [Update-SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843948.aspx) cmdlet to update the DEP and enable Office 365 to start using the new key.</span></span> 
  
```
Update-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl> -KeyVaultName <ReplacementKeyVaultName> -KeyName <ReplacementKeyName> -KeyVersion <ReplacementKeyVersion> -KeyType <Primary | Secondary>
```

<span data-ttu-id="a7de5-p176">Isso iniciará a operação do rolo principal para o SharePoint Online e o OneDrive for Business. Esta ação não é imediata. Para ver o andamento da operação do registro principal, execute o cmdlet Get-SPODataEncryptionPolicy da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="a7de5-p176">This will start the key roll operation for SharePoint Online and OneDrive for Business. This action is not immediate. To see the progress of the key roll operation, run the Get-SPODataEncryptionPolicy cmdlet as follows:</span></span>
  
```
Get-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl>
```

### <a name="manage-key-vault-permissions"></a><span data-ttu-id="a7de5-494">Gerenciar permissões do Key Vault</span><span class="sxs-lookup"><span data-stu-id="a7de5-494">Manage key vault permissions</span></span>
<span data-ttu-id="a7de5-495"><a name="Managekeyvaultperms"> </a></span><span class="sxs-lookup"><span data-stu-id="a7de5-495"></span></span>

<span data-ttu-id="a7de5-p177">Há vários cmdlets disponíveis que permitem que você visualize e, se necessário, remova as permissões do Key Vault. Talvez seja necessário remover permissões, por exemplo, quando um funcionário sair da equipe.</span><span class="sxs-lookup"><span data-stu-id="a7de5-p177">Several cmdlets are available that enable you to view and, if necessary, remove key vault permissions. You might need to remove permissions, for example, when an employee leaves the team.</span></span>
  
<span data-ttu-id="a7de5-498">Para exibir as permissões do compartimento de chaves, execute o cmdlet Get-AzureRmKeyVault:</span><span class="sxs-lookup"><span data-stu-id="a7de5-498">To view key vault permissions, run the Get-AzureRmKeyVault cmdlet:</span></span>
  
```
Get-AzureRmKeyVault -VaultName <vaultname>
```

<span data-ttu-id="a7de5-499">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="a7de5-499">For example:</span></span>
  
```
Get-AzureRmKeyVault -VaultName Contoso-O365EX-NA-VaultA1
```

<span data-ttu-id="a7de5-500">Para remover as permissões de um administrador, execute o cmdlet Remove-AzureRmKeyVaultAccessPolicy:</span><span class="sxs-lookup"><span data-stu-id="a7de5-500">To remove an administrator's permissions, run the Remove-AzureRmKeyVaultAccessPolicy cmdlet:</span></span>
  
```
Remove-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> 
-UserPrincipalName <UPN of user>
```

<span data-ttu-id="a7de5-501">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="a7de5-501">For example:</span></span>
  
```
Remove-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
-UserPrincipalName alice@contoso.com
```

### <a name="determine-the-dep-assigned-to-a-mailbox"></a><span data-ttu-id="a7de5-502">Determinar a DEP atribuída a uma caixa de correio</span><span class="sxs-lookup"><span data-stu-id="a7de5-502">Determine the DEP assigned to a mailbox</span></span>
<span data-ttu-id="a7de5-503"><a name="DeterminemailboxDEP"> </a></span><span class="sxs-lookup"><span data-stu-id="a7de5-503"></span></span>

<span data-ttu-id="a7de5-p178">Para determinar a DEP atribuída a uma caixa de correio, use o cmdlet Get-MailboxStatistics. O cmdlet retorna um identificador exclusivo (GUID).</span><span class="sxs-lookup"><span data-stu-id="a7de5-p178">To determine the DEP assigned to a mailbox, use the Get-MailboxStatistics cmdlet. The cmdlet returns a unique identifier (GUID).</span></span>
  
```
Get-MailboxStatistics -Identity <GeneralMailboxOrMailUserIdParameter> | fl DataEncryptionPolicyID
```

<span data-ttu-id="a7de5-p179">Onde *GeneralMailboxOrMailUserIdParameter* especifica uma caixa de correio. Para obter mais informações sobre o cmdlet Get-MailboxStatistics, consulte [Get-MailboxStatistics](https://technet.microsoft.com/library/bb124612%28v=exchg.160%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="a7de5-p179">Where *GeneralMailboxOrMailUserIdParameter* specifies a mailbox. For more information about the Get-MailboxStatistics cmdlet, see [Get-MailboxStatistics](https://technet.microsoft.com/library/bb124612%28v=exchg.160%29.aspx).</span></span>
  
<span data-ttu-id="a7de5-508">Use o GUID para descobrir o nome amigável da DEP à qual a caixa de correio é atribuída executando o cmdlet a seguir.</span><span class="sxs-lookup"><span data-stu-id="a7de5-508">Use the GUID to find out the friendly name of the DEP to which the mailbox is assigned by running the following cmdlet.</span></span>
  
```
Get-DataEncryptionPolicy <GUID>
```

<span data-ttu-id="a7de5-509">Onde *GUID* é o GUID retornado pelo cmdlet Get-MailboxStatistics na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="a7de5-509">Where *GUID* is the GUID returned by the Get-MailboxStatistics cmdlet in the previous step.</span></span> 
  


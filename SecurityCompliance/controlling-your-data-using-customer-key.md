---
title: Controlar seus dados no Office 365 usando a Chave do cliente
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 8/1/2018
ms.audience: ITPro
ms.topic: get-started-article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f2cd475a-e592-46cf-80a3-1bfb0fa17697
description: Saiba como configurar o chave de cliente para o Office 365 para Exchange Online, Skype para negócios, SharePoint Online e OneDrive for Business. Com a chave do cliente, você controlar as chaves de criptografia da sua organização e configurar o Office 365 para usá-los para criptografar dados em repouso em centros de dados da Microsoft.
ms.openlocfilehash: 3eeccd03b89aa5a79ceba536d3f13c7a881b6ca7
ms.sourcegitcommit: ef0bb05a0cf7974ae5083c7551ce3fe4ab7a9544
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/13/2018
ms.locfileid: "23965605"
---
# <a name="controlling-your-data-in-office-365-using-customer-key"></a><span data-ttu-id="e7e12-104">Controlar seus dados no Office 365 usando a Chave do cliente</span><span class="sxs-lookup"><span data-stu-id="e7e12-104">Controlling your data in Office 365 using Customer Key</span></span>

<span data-ttu-id="e7e12-p102">Com a chave do cliente, você controlar as chaves de criptografia da sua organização e configurar o Office 365 para usá-los para criptografar dados em repouso em centros de dados da Microsoft. Dados em repouso incluem os dados do Exchange Online e do Skype for Business que é armazenado em caixas de correio e arquivos que são armazenados no SharePoint Online e o OneDrive for Business.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p102">With Customer Key, you control your organization's encryption keys and then configure Office 365 to use them to encrypt your data at rest in Microsoft's data centers. Data at rest includes data from Exchange Online and Skype for Business that is stored in mailboxes and files that are stored in SharePoint Online and OneDrive for Business.</span></span>
  
<span data-ttu-id="e7e12-p103">Você deve configurar o Azure antes de poder usar chave do cliente para o Office 365. Este tópico descreve as etapas que precisam ser seguidas para criar e configurar os recursos necessários do Windows Azure e então fornece as etapas para configurar a chave do cliente no Office 365. Após concluir a instalação do Azure, você deve determinar qual política e, portanto, quais teclas, para atribuir a caixas de correio e arquivos na sua organização. Caixas de correio e de arquivos para os quais você não atribuir uma política usará as diretivas de criptografia que são controladas e gerenciadas pela Microsoft. Para obter mais informações sobre a chave do cliente, ou para obter uma visão geral, consulte a [Chave do cliente para perguntas Frequentes do Office 365](service-encryption-with-customer-key-faq.md).</span><span class="sxs-lookup"><span data-stu-id="e7e12-p103">You must set up Azure before you can use Customer Key for Office 365. This topic describes the steps you need to follow to create and configure the required Azure resources and then provides the steps for setting up Customer Key in Office 365. After you have completed Azure setup, you determine which policy, and therefore, which keys, to assign to mailboxes and files in your organization. Mailboxes and files for which you don't assign a policy will use encryption policies that are controlled and managed by Microsoft. For more information about Customer Key, or for a general overview, see the [Customer Key for Office 365 FAQ](service-encryption-with-customer-key-faq.md).</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="e7e12-p104">É altamente recomendável que você siga as práticas recomendadas descritas neste tópico. Estes são chamados check-out como **Dica** e **importante**. Dá de chave do cliente controle sobre as chaves de criptografia de raiz cujo escopo pode ser tão grande quanto toda sua organização. Isso significa que cometidos com essas chaves podem ter um impacto amplo e podem resultar em interrupções do serviço ou perda irreversível dos seus dados.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p104">We strongly recommend that you follow the best practices in this topic. These are called out as **TIP** and **IMPORTANT**. Customer Key gives you control over root encryption keys whose scope can be as large as your entire organization. This means that mistakes made with these keys can have a broad impact and may result in service interruptions or irrevocable loss of your data.</span></span> 
  
## <a name="before-you-begin-setting-up-customer-key"></a><span data-ttu-id="e7e12-116">Antes de começar a configurar a chave do cliente</span><span class="sxs-lookup"><span data-stu-id="e7e12-116">Before you begin setting up Customer Key</span></span>
<span data-ttu-id="e7e12-117"><a name="Beforeyoustart"> </a></span><span class="sxs-lookup"><span data-stu-id="e7e12-117"></span></span>

<span data-ttu-id="e7e12-p105">Antes de começar, certifique-se de que você tem o licenciamento apropriado para sua organização. Chave do cliente no Office 365 é oferecida no Office 365 E5 ou a SKU de conformidade avançadas.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p105">Before you get started, be sure you have the appropriate licensing for your organization. Customer Key in Office 365 is offered in Office 365 E5 or the Advanced Compliance SKU.</span></span>
  
<span data-ttu-id="e7e12-p106">Em seguida, para entender os conceitos e procedimentos neste tópico, você deve consultar a documentação do [Windows Azure chave Vault](https://azure.microsoft.com/en-us/documentation/services/key-vault/) . Além disso, familiarize-se com os termos usados no Windows Azure, por exemplo, o [inquilino](https://msdn.microsoft.com/library/azure/jj573650.aspx#BKMK_WhatIsAnAzureADTenant).</span><span class="sxs-lookup"><span data-stu-id="e7e12-p106">Then, to understand the concepts and procedures in this topic, you should review the [Azure Key Vault](https://azure.microsoft.com/en-us/documentation/services/key-vault/) documentation. Also, become familiar with the terms used in Azure, for example, [tenant](https://msdn.microsoft.com/library/azure/jj573650.aspx#BKMK_WhatIsAnAzureADTenant).</span></span>
  
<span data-ttu-id="e7e12-122">Para fornecer comentários sobre a chave do cliente, incluindo a documentação, envie suas ideias, sugestões e perspectivas para customerkeyfeedback@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="e7e12-122">To provide feedback on Customer Key, including the documentation, send your ideas, suggestions and perspectives to customerkeyfeedback@microsoft.com.</span></span>
  
## <a name="overview-of-setting-up-customer-key-for-office-365"></a><span data-ttu-id="e7e12-123">Visão geral da configuração de chave de cliente para o Office 365</span><span class="sxs-lookup"><span data-stu-id="e7e12-123">Overview of setting up Customer Key for Office 365</span></span>
<span data-ttu-id="e7e12-124"><a name="Overview"> </a></span><span class="sxs-lookup"><span data-stu-id="e7e12-124"></span></span>

<span data-ttu-id="e7e12-p107">Para configurar a chave do cliente, você concluirá essas tarefas. O restante deste tópico fornece instruções detalhadas para cada tarefa ou links check-out para obter mais informações para cada etapa do processo.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p107">To set up Customer Key you will complete these tasks. The rest of this topic provides detailed instructions for each task, or links out to more information for each step in the process.</span></span>
  
<span data-ttu-id="e7e12-127">**No Windows Azure e FastTrack da Microsoft:**</span><span class="sxs-lookup"><span data-stu-id="e7e12-127">**In Azure and Microsoft FastTrack:**</span></span>
  
<span data-ttu-id="e7e12-p108">Você concluirá maioria dessas tarefas conectando remotamente ao PowerShell do Windows Azure. Para obter melhores resultados, use versão 4.4.0 ou posterior do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p108">You will complete most of these tasks by remotely connecting to Azure PowerShell. For best results, use version 4.4.0 or later of Azure PowerShell.</span></span>
  
- [<span data-ttu-id="e7e12-130">Criar duas novas inscrições Azure</span><span class="sxs-lookup"><span data-stu-id="e7e12-130">Create two new Azure subscriptions</span></span>](controlling-your-data-using-customer-key.md#Create2newsubs)
    
- [<span data-ttu-id="e7e12-131">Registrar o Azure inscrições para usar um período de retenção obrigatória</span><span class="sxs-lookup"><span data-stu-id="e7e12-131">Register Azure subscriptions to use a mandatory retention period</span></span>](controlling-your-data-using-customer-key.md#RegisterSubsforMRP)
    
    <span data-ttu-id="e7e12-132">Registro pode levar de um a cinco dias úteis.</span><span class="sxs-lookup"><span data-stu-id="e7e12-132">Registration can take from one to five business days.</span></span>
    
- [<span data-ttu-id="e7e12-133">Enviar uma solicitação para ativar a chave do cliente para o Office 365</span><span class="sxs-lookup"><span data-stu-id="e7e12-133">Submit a request to activate Customer Key for Office 365</span></span>](controlling-your-data-using-customer-key.md#FastTrack)
    
    <span data-ttu-id="e7e12-p109">Depois que você criou as duas novas inscrições Azure, você precisará enviar a solicitação de oferta de chave de cliente apropriada, completando um formulário da web que é hospedado no portal do Microsoft FastTrack. A equipe de FastTrack não prestar assistência com chave de cliente. Office simplesmente usa o portal de FastTrack para permitir que você envie o formulário e nos ajudar a controlar as ofertas relevantes para a chave do cliente.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p109">Once you've created the two new Azure subscriptions, you'll need to submit the appropriate Customer Key offer request by completing a web form that is hosted in the Microsoft FastTrack portal. The FastTrack team doesn't provide assistance with Customer Key. Office simply uses the FastTrack portal to allow you to submit the form and to help us track the relevant offers for Customer Key.</span></span>
  
<span data-ttu-id="e7e12-p110">Depois que você enviou uma oferta de chave de cliente, o Microsoft analisa sua solicitação e notifica você quando você pode continuar com o restante das tarefas de instalação. Esse processo pode levar até cinco dias úteis.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p110">Once you have submitted a Customer Key offer, Microsoft reviews your request and notifies you when you can proceed with the rest of the setup tasks. This process can take up to five business days.</span></span>
    
- [<span data-ttu-id="e7e12-139">Criar um premium Azure chave Vault em cada uma assinatura</span><span class="sxs-lookup"><span data-stu-id="e7e12-139">Create a premium Azure Key Vault in each subscription</span></span>](controlling-your-data-using-customer-key.md#CreateKeyVault)
    
- [<span data-ttu-id="e7e12-140">Atribuir permissões a cada vault principal</span><span class="sxs-lookup"><span data-stu-id="e7e12-140">Assign permissions to each key vault</span></span>](controlling-your-data-using-customer-key.md#KeyVaultPerms)
    
- [<span data-ttu-id="e7e12-141">Habilitar e Confirmar exclusão reversível na suas chaves compartimentos</span><span class="sxs-lookup"><span data-stu-id="e7e12-141">Enable and then confirm soft delete on your key vaults</span></span>](controlling-your-data-using-customer-key.md#SoftDelete)
    
- [<span data-ttu-id="e7e12-142">Adicionar uma chave para cada chave vault tanto criando ou importando uma chave</span><span class="sxs-lookup"><span data-stu-id="e7e12-142">Add a key to each key vault either by creating or importing a key</span></span>](controlling-your-data-using-customer-key.md#AddKeystoKeyVault)
    
- [<span data-ttu-id="e7e12-143">Marque o nível de recuperação de suas chaves</span><span class="sxs-lookup"><span data-stu-id="e7e12-143">Check the recovery level of your keys</span></span>](controlling-your-data-using-customer-key.md#CheckKeyRecoveryLevel)
    
- [<span data-ttu-id="e7e12-144">Backup Vault Azure de chave</span><span class="sxs-lookup"><span data-stu-id="e7e12-144">Backup Azure Key Vault</span></span>](controlling-your-data-using-customer-key.md#BackupAzureKeyVaultkeys)
    
- [<span data-ttu-id="e7e12-145">Validar as definições de configuração de armazenamento de chave do Windows Azure</span><span class="sxs-lookup"><span data-stu-id="e7e12-145">Validate Azure Key Vault configuration settings</span></span>](controlling-your-data-using-customer-key.md#Validateconfiguration)
    
- [<span data-ttu-id="e7e12-146">Obter o URI para cada chave Vault de chave do Windows Azure</span><span class="sxs-lookup"><span data-stu-id="e7e12-146">Obtain the URI for each Azure Key Vault key</span></span>](controlling-your-data-using-customer-key.md#GetKeyURI)
    
<span data-ttu-id="e7e12-147">**No Office 365:**</span><span class="sxs-lookup"><span data-stu-id="e7e12-147">**In Office 365:**</span></span>
  
<span data-ttu-id="e7e12-148">Exchange Online e Skype para negócios:</span><span class="sxs-lookup"><span data-stu-id="e7e12-148">Exchange Online and Skype for Business:</span></span>
  
- [<span data-ttu-id="e7e12-149">Criar uma política de criptografia de dados (DEP) para uso com o Exchange Online e Skype para negócios</span><span class="sxs-lookup"><span data-stu-id="e7e12-149">Create a data encryption policy (DEP) for use with Exchange Online and Skype for Business</span></span>](controlling-your-data-using-customer-key.md#CreateDEP4EXOSkype)
    
- [<span data-ttu-id="e7e12-150">Atribuir um DEP a uma caixa de correio</span><span class="sxs-lookup"><span data-stu-id="e7e12-150">Assign a DEP to a mailbox</span></span>](controlling-your-data-using-customer-key.md#assignDEPtomailbox)
    
- [<span data-ttu-id="e7e12-151">Validar a criptografia de caixa de correio</span><span class="sxs-lookup"><span data-stu-id="e7e12-151">Validate mailbox encryption</span></span>](controlling-your-data-using-customer-key.md#validatemailboxencryption)
    
<span data-ttu-id="e7e12-152">SharePoint Online e o OneDrive for Business:</span><span class="sxs-lookup"><span data-stu-id="e7e12-152">SharePoint Online and OneDrive for Business:</span></span>
  
- [<span data-ttu-id="e7e12-153">Criar uma diretiva de criptografia de dados (DEP) para cada SharePoint Online e o OneDrive for Business geo</span><span class="sxs-lookup"><span data-stu-id="e7e12-153">Create a data encryption policy (DEP) for each SharePoint Online and OneDrive for Business geo</span></span>](controlling-your-data-using-customer-key.md#CreateDEP4SPOODfB)
    
- [<span data-ttu-id="e7e12-154">Validar a criptografia do grupo de Sites, Sites de equipe e OneDrive for Business</span><span class="sxs-lookup"><span data-stu-id="e7e12-154">Validate encryption of Group Sites, Team Sites, and OneDrive for Business</span></span>](controlling-your-data-using-customer-key.md#validateencryptionSPO)
    
## <a name="complete-tasks-in-azure-key-vault-and-microsoft-fasttrack-for-customer-key"></a><span data-ttu-id="e7e12-155">Concluir tarefas no Azure chave Vault e Microsoft FastTrack para a chave do cliente</span><span class="sxs-lookup"><span data-stu-id="e7e12-155">Complete tasks in Azure Key Vault and Microsoft FastTrack for Customer Key</span></span>
<span data-ttu-id="e7e12-156"><a name="AzureSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="e7e12-156"></span></span>

<span data-ttu-id="e7e12-p111">Conclua essas tarefas no Azure chave Vault para configurar a chave de cliente para o Office 365. Você precisará concluir essas etapas, independentemente se você pretende configurar chave do cliente para o Exchange Online e Skype para negócios ou SharePoint Online e OneDrive for Business ou para todos os serviços com suporte no Office 365.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p111">Complete these tasks in Azure Key Vault in order to set up Customer Key for Office 365. You will need to complete these steps regardless of whether you intend to set up Customer Key for Exchange Online and Skype for Business or SharePoint Online and OneDrive for Business or for all supported services in Office 365.</span></span>
  
### <a name="create-two-new-azure-subscriptions"></a><span data-ttu-id="e7e12-159">Criar duas novas inscrições Azure</span><span class="sxs-lookup"><span data-stu-id="e7e12-159">Create two new Azure subscriptions</span></span>
<span data-ttu-id="e7e12-160"><a name="Create2newsubs"> </a></span><span class="sxs-lookup"><span data-stu-id="e7e12-160"></span></span>

<span data-ttu-id="e7e12-p112">Duas assinaturas Azure são necessárias para a chave do cliente. Como prática recomendada, a Microsoft recomenda que você crie novas inscrições Azure para uso com a chave do cliente. Chaves de chave Vault Azure só podem ser autorizadas para aplicativos no mesmo inquilino do Azure Active Directory (AAD), você deve criar as novas inscrições usando o mesmo inquilino Azure AD usado com a sua organização do Office 365 onde os DEPs serão atribuídos. Por exemplo, usando sua conta de trabalho ou da escola que tenha privilégios de administrador global na sua organização do Office 365. Para obter etapas detalhadas, consulte [inscrever-se no Azure como uma organização](https://azure.microsoft.com/en-us/documentation/articles/sign-up-organization/).</span><span class="sxs-lookup"><span data-stu-id="e7e12-p112">Two Azure subscriptions are required for Customer Key. As a best practice, Microsoft recommends that you create new Azure subscriptions for use with Customer Key. Azure Key Vault keys can only be authorized for applications in the same Azure Active Directory (AAD) tenant, you must create the new subscriptions using the same Azure AD tenant used with your Office 365 organization where the DEPs will be assigned. For example, using your work or school account that has global administrator privileges in your Office 365 organization. For detailed steps, see [Sign up for Azure as an organization](https://azure.microsoft.com/en-us/documentation/articles/sign-up-organization/).</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="e7e12-p113">Chave de cliente exige duas chaves para cada política de criptografia de dados (DEP). Para conseguir isso, você deve criar dois assinaturas do Azure. Como prática recomendada, a Microsoft recomenda que você tenha separados membros da sua organização configurar uma chave em cada uma assinatura. Além disso, essas assinaturas Azure só devem ser usadas para administrar as chaves de criptografia para o Office 365. Isso protege a sua organização no caso de um dos seus operadores acidentalmente, intencionalmente ou modo mal-intencionado exclui ou mismanages caso contrário, as chaves para os quais eles são responsáveis.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p113">Customer Key requires two keys for each data encryption policy (DEP). In order to achieve this, you must create two Azure subscriptions. As a best practice, Microsoft recommends that you have separate members of your organization configure one key in each subscription. In addition, these Azure subscriptions should only be used to administer encryption keys for Office 365. This protects your organization in case one of your operators accidentally, intentionally, or maliciously deletes or otherwise mismanages the keys for which they are responsible. </span></span><br/> <span data-ttu-id="e7e12-p114">Recomendamos que você configure novas inscrições Azure que são usadas exclusivamente para gerenciar recursos de armazenamento de chave do Windows Azure para uso com chave de cliente. Não há nenhum limite prático para o número de inscrições Azure que podem ser criados para sua organização. Estas práticas recomendadas minimizará o impacto de erro humano e ajudar a gerenciar os recursos usados pela chave do cliente.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p114">We recommend that you set up new Azure subscriptions that are solely used for managing Azure Key Vault resources for use with Customer Key. There is no practical limit to the number of Azure subscriptions that you can create for your organization. Following these best practices will minimize the impact of human error while helping to manage the resources used by Customer Key.</span></span> 
  
### <a name="submit-a-request-to-activate-customer-key-for-office-365"></a><span data-ttu-id="e7e12-174">Enviar uma solicitação para ativar a chave do cliente para o Office 365</span><span class="sxs-lookup"><span data-stu-id="e7e12-174">Submit a request to activate Customer Key for Office 365</span></span>
<span data-ttu-id="e7e12-175"><a name="FastTrack"> </a></span><span class="sxs-lookup"><span data-stu-id="e7e12-175"></span></span>

<span data-ttu-id="e7e12-p115">Depois de ter concluído as etapas do Azure, você precisará enviar uma solicitação de oferta no [portal do Microsoft FastTrack](https://fasttrack.microsoft.com/). Depois que você enviou uma solicitação por meio do portal da web FastTrack, Microsoft verifica as informações Azure chave Vault de dados e o contato configuração fornecidas por você. As seleções feitas no formato oferta relacionadas as oficiais autorizados da sua organização é necessário para a conclusão do registro da chave de cliente e não críticas. Os oficiais da sua organização que você seleciona no formulário será o valor usado para assegurar a autenticidade de qualquer solicitação revogar e destruir todas as chaves usadas com uma diretiva de criptografia de dados de chave do cliente. Você precisará executar esta etapa uma vez para ativar a chave de cliente do Exchange Online e Skype para cobertura de negócios e uma segunda vez ativar a chave do cliente para o SharePoint Online e o OneDrive for Business.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p115">Once you've completed the Azure steps, you'll need to submit an offer request in the [Microsoft FastTrack portal](https://fasttrack.microsoft.com/). Once you have submitted a request through the FastTrack web portal, Microsoft verifies the Azure Key Vault configuration data and contact information you provided. The selections that you make in the offer form regarding the authorized officers of your organization is critical and necessary for completion of Customer Key registration. The officers of your organization that you select in the form will be the used to ensure the authenticity of any request to revoke and destroy all keys used with a Customer Key data encryption policy. You'll need to do this step once to activate Customer Key for Exchange Online and Skype for Business coverage and a second time to activate Customer Key for SharePoint Online and OneDrive for Business.</span></span>
  
<span data-ttu-id="e7e12-181">Para enviar uma oferta para ativar a chave do cliente, conclua estas etapas:</span><span class="sxs-lookup"><span data-stu-id="e7e12-181">To submit an offer to activate Customer Key, complete these steps:</span></span>
  
1. <span data-ttu-id="e7e12-182">Usando uma conta de trabalho ou da escola que tenha permissões de administrador global na sua organização do Office 365, faça logon no [portal do Microsoft FastTrack](https://fasttrack.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="e7e12-182">Using a work or school account that has global administrator permissions in your Office 365 organization, log in to the [Microsoft FastTrack portal](https://fasttrack.microsoft.com/).</span></span>
    
2. <span data-ttu-id="e7e12-183">Depois que você está logado, navegue até o **painel**.</span><span class="sxs-lookup"><span data-stu-id="e7e12-183">Once you're logged in, browse to the **Dashboard**.</span></span>
    
3. <span data-ttu-id="e7e12-184">Escolha **oferece**e examine a lista de ofertas atuais.</span><span class="sxs-lookup"><span data-stu-id="e7e12-184">Choose **Offers**, and review the list of current offers.</span></span>
    
4. <span data-ttu-id="e7e12-185">Escolha **Saiba mais** oferta do que se aplica a você:</span><span class="sxs-lookup"><span data-stu-id="e7e12-185">Choose **Learn More** for the offer that applies to you:</span></span> 
    
  - <span data-ttu-id="e7e12-186">**Exchange Online e Skype for Business:** Escolha **Saiba mais** sobre a oferta de **Chave de cliente do Exchange** .</span><span class="sxs-lookup"><span data-stu-id="e7e12-186">**Exchange Online and Skype for Business:** Choose **Learn More** on the **Customer Key for Exchange** offer.</span></span> 
    
  - <span data-ttu-id="e7e12-187">**SharePoint Online e o OneDrive for Business:** Escolher **Saiba mais** sobre a oferta de **Chave de cliente para SharePoint e o OneDrive for Business** .</span><span class="sxs-lookup"><span data-stu-id="e7e12-187">**SharePoint Online and OneDrive for Business:** Chose **Learn More** on the **Customer Key for SharePoint and OneDrive for Business** offer.</span></span> 
    
5. <span data-ttu-id="e7e12-188">Na página **detalhes da oferta** , escolha **Criar a solicitação**.</span><span class="sxs-lookup"><span data-stu-id="e7e12-188">On the **Offer details** page, choose **Create Request**.</span></span>
    
6. <span data-ttu-id="e7e12-p116">Preencha todos os detalhes aplicáveis e as informações solicitadas no formulário oferta. Preste atenção para suas seleções para quais oficiais da sua organização para o qual você deseja autorizar para aprovar a destruição permanente e irreversível de chaves de criptografia e dados. Depois de ter concluído o formulário, escolha **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p116">Fill out all applicable details and requested information on the offer form. Pay particular attention to your selections for which officers of your organization you want to authorize to approve the permanent and irreversible destruction of encryption keys and data. Once you've completed the form, choose **Submit**.</span></span>
    
    <span data-ttu-id="e7e12-192">Esse processo pode levar até cinco dias de negócios depois que a Microsoft foi notificado da sua solicitação.</span><span class="sxs-lookup"><span data-stu-id="e7e12-192">This process can take up to five business days once Microsoft has been notified of your request.</span></span>
    
7. <span data-ttu-id="e7e12-193">Prosseguir para a seção de período de retenção obrigatória abaixo.</span><span class="sxs-lookup"><span data-stu-id="e7e12-193">Continue on to the mandatory retention period section below.</span></span>
    
### <a name="register-azure-subscriptions-to-use-a-mandatory-retention-period"></a><span data-ttu-id="e7e12-194">Registrar o Azure inscrições para usar um período de retenção obrigatória</span><span class="sxs-lookup"><span data-stu-id="e7e12-194">Register Azure subscriptions to use a mandatory retention period</span></span>
<span data-ttu-id="e7e12-195"><a name="RegisterSubsforMRP"> </a></span><span class="sxs-lookup"><span data-stu-id="e7e12-195"></span></span>

<span data-ttu-id="e7e12-p117">A perda temporária ou permanente de chaves de criptografia de raiz pode ser muito destrutivos ou até mesmo catastrófica a operação de serviço e pode resultar em perda de dados. Por esse motivo, os recursos usados com a chave de cliente exigem proteção de alta segurança. Todos os recursos do Azure que são usados com a chave de cliente oferecem mecanismos de proteção além da configuração padrão. Assinaturas do Azure podem ser marcadas ou registradas de forma que impedirá o cancelamento imediato e irrevogável. Isso é conhecido como registrando por um período de retenção obrigatória. As etapas necessárias para registrar o Azure inscrições por um período de retenção obrigatória exigem colaboração com a equipe do Office 365. Esse processo pode levar de um a cinco dias úteis. Anteriormente, isso era às vezes conhecido como "Não cancelar".</span><span class="sxs-lookup"><span data-stu-id="e7e12-p117">The temporary or permanent loss of root encryption keys can be very disruptive or even catastrophic to service operation and can result in data loss. For this reason, the resources used with Customer Key require strong protection. All the Azure resources that are used with Customer Key offer protection mechanisms beyond the default configuration. Azure subscriptions can be tagged or registered in a way that will prevent immediate and irrevocable cancellation. This is referred to as registering for a mandatory retention period. The steps required to register Azure subscriptions for a mandatory retention period require collaboration with the Office 365 team. This process can take from one to five business days. Previously, this was sometimes referred to as "Do Not Cancel".</span></span>
  
<span data-ttu-id="e7e12-204">Antes de contatar a equipe do Office 365, você deve executar as seguintes etapas para cada assinatura Azure que você pode usar com a chave de cliente:</span><span class="sxs-lookup"><span data-stu-id="e7e12-204">Before contacting the Office 365 team, you must perform the following steps for each Azure subscription that you use with Customer Key:</span></span>
  
1. <span data-ttu-id="e7e12-p118">Faça logon em sua assinatura do Windows Azure com o Azure PowerShell. Para obter instruções, consulte [entrar nas Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).</span><span class="sxs-lookup"><span data-stu-id="e7e12-p118">Log in to your Azure subscription with Azure PowerShell. For instructions, see [Log in with Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).</span></span>
    
2. <span data-ttu-id="e7e12-207">Execute o cmdlet Register-AzureRmProviderFeature para registrar suas assinaturas para usar um período de retenção obrigatória.</span><span class="sxs-lookup"><span data-stu-id="e7e12-207">Run the Register-AzureRmProviderFeature cmdlet to register your subscriptions to use a mandatory retention period.</span></span>
    
  ```
  Register-AzureRmProviderFeature -FeatureName mandatoryRetentionPeriodEnabled -ProviderNamespace Microsoft.Resources
  ```

3. <span data-ttu-id="e7e12-p119">Contate a Microsoft para que o processo finalizado. Para o SharePoint e o OneDrive para a equipe de negócios, contate [spock@microsoft.com](mailto:spock@microsoft.com). Para o Exchange Online e Skype para a empresa, contate [exock@microsoft.com](mailto:exock@microsoft.com). O contrato de nível de serviço (SLA) para a conclusão desse processo é cinco dias úteis depois que a Microsoft foi notificado (e verificou) que você registrou suas assinaturas para usar um período de retenção obrigatória. Inclua o seguinte no seu email:</span><span class="sxs-lookup"><span data-stu-id="e7e12-p119">Contact Microsoft to have the process finalized. For the SharePoint and OneDrive for Business team, contact [spock@microsoft.com](mailto:spock@microsoft.com). For Exchange Online and Skype for Business, contact [exock@microsoft.com](mailto:exock@microsoft.com). The Service Level Agreement (SLA) for completion of this process is five business days once Microsoft has been notified (and verified) that you have registered your subscriptions to use a mandatory retention period. Include the following in your email:</span></span>
    
    <span data-ttu-id="e7e12-213">**Assunto**: chave do cliente para \< *nome de domínio totalmente qualificado de seu locatário*\></span><span class="sxs-lookup"><span data-stu-id="e7e12-213">**Subject**: Customer Key for \<*Your tenant's fully-qualified domain name*\></span></span> 
    
    <span data-ttu-id="e7e12-214">**Corpo**: IDs de assinatura para o qual você deseja ter o obrigatória finalizada período de retenção.</span><span class="sxs-lookup"><span data-stu-id="e7e12-214">**Body**: Subscription IDs for which you want to have the mandatory retention period finalized.</span></span> 
    
4. <span data-ttu-id="e7e12-215">Depois de receber a notificação da Microsoft que registro está concluído, verifique o status do seu registro executando o cmdlet Get-AzureRmProviderFeature da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e7e12-215">Once you receive notification from Microsoft that registration is complete, verify the status of your registration by running the Get-AzureRmProviderFeature cmdlet as follows:</span></span>
    
  ```
  Get-AzureRmProviderFeature -ProviderNamespace Microsoft.Resources -FeatureName mandatoryRetentionPeriodEnabled
  ```

5. <span data-ttu-id="e7e12-216">Depois de verificar se a propriedade **Estado do registro** do cmdlet Get-AzureRmProviderFeature retorna um valor de **Registered**, execute o seguinte comando para concluir o processo:</span><span class="sxs-lookup"><span data-stu-id="e7e12-216">After verifying that the **Registration State** property from the Get-AzureRmProviderFeature cmdlet returns a value of **Registered**, run the following command to complete the process:</span></span>
    
  ```
  Register-AzureRmResourceProvider -ProviderNamespace "Microsoft.KeyVault"
  ```

### <a name="create-a-premium-azure-key-vault-in-each-subscription"></a><span data-ttu-id="e7e12-217">Criar um premium Azure chave Vault em cada uma assinatura</span><span class="sxs-lookup"><span data-stu-id="e7e12-217">Create a premium Azure Key Vault in each subscription</span></span>
<span data-ttu-id="e7e12-218"><a name="CreateKeyVault"> </a></span><span class="sxs-lookup"><span data-stu-id="e7e12-218"></span></span>

<span data-ttu-id="e7e12-219">As etapas para criar um armazenamento de chave estão documentadas no [Guia de Introdução ao Windows Azure chave Vault](https://azure.microsoft.com/documentation/articles/key-vault-get-started/), que lhe orienta durante a instalação e lançar o Azure PowerShell, conectando-se a sua assinatura do Windows Azure, criando um grupo de recursos e criando um armazenamento de chave em que grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e7e12-219">The steps to create a key vault are documented in [Getting Started with Azure Key Vault](https://azure.microsoft.com/documentation/articles/key-vault-get-started/), which guides you through installing and launching Azure PowerShell, connecting to your Azure subscription, creating a resource group, and creating a key vault in that resource group.</span></span>
  
<span data-ttu-id="e7e12-p120">Quando você cria um armazenamento de chave, você deve escolher uma SKU: Standard ou Premium. A SKU Standard permite que as chaves do Azure chave Vault devem ser protegidos com o software - não há nenhuma proteção de chave do módulo de segurança de Hardware (HSM) - e a SKU Premium permite o uso de HSMs para proteção de chave Vault chaves. Chave de cliente aceita compartimentos principais que usam qualquer SKU, embora a Microsoft recomenda que você use apenas a SKU Premium. O custo das operações com chaves de qualquer tipo é o mesmo, portanto, a única diferença no custo é o custo por mês para cada chave HSM protegidas. Para obter detalhes, consulte [chave Vault preços](https://azure.microsoft.com/pricing/details/key-vault/) .</span><span class="sxs-lookup"><span data-stu-id="e7e12-p120">When you create a key vault, you must choose a SKU: either Standard or Premium. The Standard SKU allows Azure Key Vault keys to be protected with software - there is no Hardware Security Module (HSM) key protection - and the Premium SKU allows the use of HSMs for protection of Key Vault keys. Customer Key accepts key vaults that use either SKU, though Microsoft strongly recommends that you use only the Premium SKU. The cost of operations with keys of either type is the same, so the only difference in cost is the cost per month for each HSM-protected key. See [Key Vault pricing](https://azure.microsoft.com/pricing/details/key-vault/) for details.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="e7e12-225">Use os compartimentos de chave Premium SKU e protegidos HSM as chaves para dados de produção e use apenas compartimentos principais de SKU Standard e chaves para fins de teste e validação.</span><span class="sxs-lookup"><span data-stu-id="e7e12-225">Use the Premium SKU key vaults and HSM-protected keys for production data, and only use Standard SKU key vaults and keys for testing and validation purposes.</span></span> 
  
<span data-ttu-id="e7e12-p121">Para cada serviço do Office 365 com os quais você usará a chave de cliente, crie um armazenamento de chave em cada uma das duas inscrições Azure que você criou. Por exemplo, para o Exchange Online e Skype para negócios apenas ou SharePoint Online e o OneDrive for Business apenas, você criará somente um par de compartimentos. Para habilitar a chave de cliente para o Exchange Online e SharePoint Online, você irá criar dois pares de chaves compartimentos.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p121">For each Office 365 service with which you will use Customer Key, create a key vault in each of the two Azure subscriptions that you created. For example, for Exchange Online and Skype for Business only or SharePoint Online and OneDrive for Business only, you will create only one pair of vaults. To enable Customer Key for both Exchange Online and SharePoint Online, you will create two pairs of key vaults.</span></span>
  
<span data-ttu-id="e7e12-p122">Use uma convenção de nomenclatura para compartimentos principais que reflete o uso pretendido da DEP com os quais você irá associar os compartimentos. Consulte a seção de práticas recomendadas abaixo recomendações da convenção de nomenclatura.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p122">Use a naming convention for key vaults that reflects the intended use of the DEP with which you will associate the vaults. See the Best Practices section below for naming convention recommendations.</span></span>
  
<span data-ttu-id="e7e12-p123">Crie um conjunto de compartimentos para cada política de criptografia de dados separado e emparelhado. Para o Exchange Online, o escopo de uma diretiva de criptografia de dados é escolhido por você ao atribuir a diretiva de caixa de correio. Uma caixa de correio pode ter apenas uma política atribuída e você pode criar até cinquenta diretivas. Para o SharePoint Online, o escopo de uma diretiva é todos os dados em uma organização em uma localização geográfica ou geo.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p123">Create a separate, paired set of vaults for each data encryption policy. For Exchange Online, the scope of a data encryption policy is chosen by you when you assign the policy to mailbox. A mailbox can have only one policy assigned, and you can create up to fifty policies. For SharePoint Online the scope of a policy is all of the data within an organization in a geographic location, or geo.</span></span>
  
<span data-ttu-id="e7e12-p124">A criação de chaves compartimentos também requer a criação de grupos de recursos do Windows Azure, desde que compartimentos principais precisam de capacidade de armazenamento (embora muito pequeno) e Vault da chave de registro em log, se for habilitada, também gera dados armazenados. Como prática recomendada a Microsoft recomenda usar o administradores separados para gerenciar cada grupo de recursos, com a administração alinhada com o conjunto de administradores que irá gerenciar todos os recursos relacionados da chave de cliente.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p124">The creation of key vaults also requires the creation of Azure resource groups, since key vaults need storage capacity (though very small) and Key Vault logging, if enabled, also generates stored data. As a best practice Microsoft recommends using separate administrators to manage each resource group, with the administration aligned with the set of administrators that will manage all related Customer Key resources.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="e7e12-p125">Para maximizar a disponibilidade, a suas chaves compartimentos devem ficar em regiões e está perto do seu serviço do Office 365. Por exemplo, se sua organização do Exchange Online for na América do Norte, coloque a suas chaves compartimentos na América do Norte. Se sua organização do Exchange Online for na Europa, coloque a suas chaves compartimentos na Europa.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p125">To maximize availability, your key vaults should be in regions close to your Office 365 service. For example, if your Exchange Online organization is in North America, place your key vaults in North America. If your Exchange Online organization is in Europe, place your key vaults in Europe.</span></span><br/><span data-ttu-id="e7e12-p126">Use um prefixo comum para compartimentos chaves e incluir o escopo das principal vault e chaves e uma abreviação do uso (por exemplo, para o serviço de Contoso SharePoint onde os compartimentos estará localizados na América do Norte, um par de possível de nomes é Contoso-O365SP-NA-VaultA1 e Contoso-O365SP-NA-VaultA2. Nomes Vault são cadeias de caracteres globalmente exclusivas dentro do Azure, portanto, talvez você precise tente variações de seus nomes desejados, caso os nomes desejados já estão solicitados por outros clientes do Azure. A partir de julho de 2017 vault nomes não podem ser alterados, portanto, uma prática recomendada é ter um plano por escrito para a instalação e usar uma segunda pessoa para verificar que o plano é executado corretamente.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p126">Use a common prefix for key vaults, and include an abbreviation of the use and scope of the key vault and keys (e.g., for the Contoso SharePoint service where the vaults will be located in North America, a possible pair of names is Contoso-O365SP-NA-VaultA1 and Contoso-O365SP-NA-VaultA2. Vault names are globally unique strings within Azure, so you may need to try variations of your desired names in case the desired names are already claimed by other Azure customers. As of July 2017 vault names cannot be changed, so a best practice is to have a written plan for setup and use a second person to verify the plan is executed correctly.</span></span><br/><span data-ttu-id="e7e12-p127">Se possível, crie seus compartimentos em regiões não emparelhada. Emparelhados regiões Azure fornecem alta disponibilidade entre domínios de falha de serviço. Portanto, pares regionais podem ser considerados região backup uns dos outros. Isso significa que um recurso Azure que é colocado em uma região está ganhando automaticamente a tolerância a falhas por meio da região emparelhada. Por esse motivo, escolhendo áreas para dois compartimentos usados em um DEP onde as regiões são emparelhadas significa que apenas um total de duas regiões de disponibilidade estão em uso. Maioria das regiões têm apenas duas regiões, portanto, ele ainda não é possível selecionar regiões não emparelhada. Se possível, escolha duas regiões não emparelhada para os dois compartimentos usados com um DEP. Isso se beneficia de um total de quatro áreas de disponibilidade. Para obter mais informações, consulte [Business continuity e recuperação de desastres (BCDR): Azure emparelhada regiões](https://docs.microsoft.com/azure/best-practices-availability-paired-regions) para obter uma lista atual de pares regionais.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p127">If possible, create your vaults in non-paired regions. Paired Azure regions provide high availability across service failure domains. Therefore, regional pairs can be thought of as each other's backup region. This means that an Azure resource that is placed in one region is automatically gaining fault tolerance through the paired region. For this reason, choosing regions for two vaults used in a DEP where the regions are paired means that only a total of two regions of availability are in use. Most geographies only have two regions, so it's not yet possible to select non-paired regions. If possible, choose two non-paired regions for the two vaults used with a DEP. This benefits from a total of four regions of availability. For more information, see [Business continuity and disaster recovery (BCDR): Azure Paired Regions](https://docs.microsoft.com/azure/best-practices-availability-paired-regions) for a current list of regional pairs.</span></span> 
  
### <a name="assign-permissions-to-each-key-vault"></a><span data-ttu-id="e7e12-252">Atribuir permissões a cada vault principal</span><span class="sxs-lookup"><span data-stu-id="e7e12-252">Assign permissions to each key vault</span></span>
<span data-ttu-id="e7e12-253"><a name="KeyVaultPerms"> </a></span><span class="sxs-lookup"><span data-stu-id="e7e12-253"></span></span>

<span data-ttu-id="e7e12-p128">Para cada chave vault, você precisará definir três conjuntos de permissões para a chave do cliente, dependendo da sua implementação separados. Por exemplo, você precisará definir um conjunto de permissões para cada um dos seguintes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="e7e12-p128">For each key vault, you will need to define three separate sets of permissions for Customer Key, depending on your implementation. For example, you will need to define one set of permissions for each of the following:</span></span>
  
- <span data-ttu-id="e7e12-p129">**Os administradores de armazenamento de chave** que executará o gerenciamento diário da sua chave vault para sua organização. Essas tarefas incluem o backup, criar, obtém, importar, lista e restaurar.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p129">**Key vault administrators** that will perform day-to-day management of your key vault for your organization. These tasks include backup, create, get, import, list, and restore.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="e7e12-p130">O conjunto de permissões atribuídas aos administradores vault chave não inclui a permissão para excluir chaves. Isso é intencional e uma prática importante. Excluindo as chaves de criptografia não é geralmente feito, desde que fazer então permanentemente destruir dados. Como prática recomendada, não conceda essa permissão aos administradores vault principais por padrão. Em vez disso, reservar isso para colaboradores da chave vault e apenas atribuí-la a um administrador em uma base de curto prazo depois que uma compreensão clara das consequências é compreendida.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p130">The set of permissions assigned to key vault administrators does not include the permission to delete keys. This is intentional and an important practice. Deleting encryption keys is not typically done, since doing so permanently destroys data. As a best practice, do not grant this permission to key vault administrators by default. Instead, reserve this for key vault contributors and only assign it to an administrator on a short term basis once a clear understanding of the consequences is understood.</span></span> 
  
    <span data-ttu-id="e7e12-p131">Para atribuir essas permissões a um usuário em sua organização do Office 365, faça logon em sua assinatura do Windows Azure com o Azure PowerShell. Para obter instruções, consulte [entrar nas Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).</span><span class="sxs-lookup"><span data-stu-id="e7e12-p131">To assign these permissions to a user in your Office 365 organization, log in to your Azure subscription with Azure PowerShell. For instructions, see [Log in with Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).</span></span>
    
- <span data-ttu-id="e7e12-265">Execute o cmdlet Set-AzureRmKeyVaultAccessPolicy para atribuir as permissões necessárias.</span><span class="sxs-lookup"><span data-stu-id="e7e12-265">Run the Set-AzureRmKeyVaultAccessPolicy cmdlet to assign the necessary permissions.</span></span>
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> 
  -UserPrincipalName <UPN of user> -PermissionsToKeys create,import,list,get,backup,restore
  ```

  <span data-ttu-id="e7e12-266">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="e7e12-266">For example:</span></span>
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
  -UserPrincipalName alice@contoso.com -PermissionsToKeys create,import,list,get,backup,restore
  ```

- <span data-ttu-id="e7e12-p132">**Os colaboradores vault chave** que pode alterar permissões no compartimento de chave do Windows Azure em si. Você precisará alterar essas permissões, como funcionários saírem ou entrarem sua equipe ou na situação extremamente rara que a tecla compartimentalizar administradores legitimamente precisam de permissão para excluir ou restaurar uma chave. Este conjunto de colaboradores da chave vault precisa ser concedido a função de **Colaborador** em sua chave vault. Você pode atribuir essa função usando o Gerenciador de recursos do Windows Azure. Para obter etapas detalhadas, consulte [Use Role-Based de controle de acesso para gerenciar o acesso aos seus recursos de assinatura do Windows Azure](https://docs.microsoft.com/azure/active-directory/role-based-access-control-configure). O administrador que cria uma assinatura tem esse acesso implicitamente, bem como a capacidade de atribuir a outros administradores à função de Colaborador.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p132">**Key vault contributors** that can change permissions on the Azure Key Vault itself. You'll need to change these permissions as employees leave or join your team, or in the extremely rare situation that the key vault administrators legitimately need permission to delete or restore a key. This set of key vault contributors needs to be granted the **Contributor** role on your key vault. You can assign this role by using Azure Resource Manager. For detailed steps, see [Use Role-Based Access Control to manage access to your Azure subscription resources](https://docs.microsoft.com/azure/active-directory/role-based-access-control-configure). The administrator who creates a subscription has this access implicitly, as well as the ability to assign other administrators to the Contributor role.</span></span>
    
- <span data-ttu-id="e7e12-p133">Se você pretende usar chave do cliente com o Exchange Online e Skype for Business, você precisa conceder permissão para o Office 365 para usar o chave vault em nome do Exchange Online e Skype para negócios. Da mesma forma, se você pretende usar a chave de cliente com o SharePoint Online e o OneDrive for Business, você precisará adicionar a permissão para o Office 365 usar o chave vault em nome do SharePoint Online e o OneDrive for Business. Para conceder permissão para o Office 365, execute o cmdlet **Set-AzureRmKeyVaultAccessPolicy** usando a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="e7e12-p133">If you intend to use Customer Key with Exchange Online and Skype for Business, you need to give permission to Office 365 to use the key vault on behalf of Exchange Online and Skype for Business. Likewise, if you intend to use Customer Key with SharePoint Online and OneDrive for Business, you need to add permission for the Office 365 to use the key vault on behalf of SharePoint Online and OneDrive for Business. To give permission to Office 365, run the **Set-AzureRmKeyVaultAccessPolicy** cmdlet using the following syntax:</span></span> 
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName <Office 365 appID>
  ```

    <span data-ttu-id="e7e12-276">Onde:</span><span class="sxs-lookup"><span data-stu-id="e7e12-276">Where:</span></span>
    
  - <span data-ttu-id="e7e12-277">*vaultname* é o nome do chave vault que você criou.</span><span class="sxs-lookup"><span data-stu-id="e7e12-277">*vaultname* is the name of the key vault you created.</span></span> 
    
  - <span data-ttu-id="e7e12-278">Para o Exchange Online e Skype para os negócios, substitua *appID do Office 365* com`00000002-0000-0ff1-ce00-000000000000`</span><span class="sxs-lookup"><span data-stu-id="e7e12-278">For Exchange Online and Skype for Business, replace  *Office 365 appID* with `00000002-0000-0ff1-ce00-000000000000`</span></span>
    
  - <span data-ttu-id="e7e12-279">Para o SharePoint Online e OneDrive for Business, substitua *appID do Office 365* com`00000003-0000-0ff1-ce00-000000000000`</span><span class="sxs-lookup"><span data-stu-id="e7e12-279">For SharePoint Online and OneDrive for Business, replace  *Office 365 appID* with `00000003-0000-0ff1-ce00-000000000000`</span></span>
    
  <span data-ttu-id="e7e12-280">Exemplo: Definindo permissões para o Exchange Online e Skype para negócios:</span><span class="sxs-lookup"><span data-stu-id="e7e12-280">Example: Setting permissions for Exchange Online and Skype for Business:</span></span>
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
  -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000002-0000-0ff1-ce00-000000000000
  ```

  <span data-ttu-id="e7e12-281">Exemplo: Definindo permissões para o SharePoint Online e o OneDrive for Business</span><span class="sxs-lookup"><span data-stu-id="e7e12-281">Example: Setting permissions for SharePoint Online and OneDrive for Business</span></span>
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365SP-NA-VaultA1 
  -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000003-0000-0ff1-ce00-000000000000
  ```

### <a name="enable-and-then-confirm-soft-delete-on-your-key-vaults"></a><span data-ttu-id="e7e12-282">Habilitar e Confirmar exclusão reversível na suas chaves compartimentos</span><span class="sxs-lookup"><span data-stu-id="e7e12-282">Enable and then confirm soft delete on your key vaults</span></span>
<span data-ttu-id="e7e12-283"><a name="SoftDelete"> </a></span><span class="sxs-lookup"><span data-stu-id="e7e12-283"></span></span>

<span data-ttu-id="e7e12-p134">Quando você pode recuperar rapidamente suas chaves, são menos suscetíveis a experiência de uma interrupção de serviço estendido devido às teclas de modo mal-intencionado ou acidentalmente excluídas. Você precisará habilitar essa configuração, conhecida como excluir suave, antes de poder usar as chaves com chave de cliente. Habilitando a excluir suave permite que você recupere compartimentos ou chaves dentro de 90 dias da exclusão sem precisar restaurá-los a partir do backup.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p134">When you can quickly recover your keys, you are less likely to experience an extended service outage due to accidentally or maliciously deleted keys. You need to enable this configuration, referred to as Soft Delete, before you can use your keys with Customer Key. Enabling Soft Delete allows you to recover keys or vaults within 90 days of deletion without having to restore them from backup.</span></span>
  
<span data-ttu-id="e7e12-287">Para habilitar a excluir suave na suas chaves compartimentos, conclua estas etapas:</span><span class="sxs-lookup"><span data-stu-id="e7e12-287">To enable Soft Delete on your key vaults, complete these steps:</span></span>
  
1. <span data-ttu-id="e7e12-p135">Faça logon em sua assinatura do Windows Azure com o Windows Powershell. Para obter instruções, consulte [entrar nas Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps).</span><span class="sxs-lookup"><span data-stu-id="e7e12-p135">Log in to your Azure subscription with Windows Powershell. For instructions, see [Log in with Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps).</span></span>
    
2. <span data-ttu-id="e7e12-p136">Execute o cmdlet [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/azurerm.keyvault/get-azurermkeyvault) . Neste exemplo, *vaultname* é o nome do chave vault para o qual você está habilitando exclusão reversível:</span><span class="sxs-lookup"><span data-stu-id="e7e12-p136">Run the [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/azurerm.keyvault/get-azurermkeyvault) cmdlet. In this example, *vaultname* is the name of the key vault for which you are enabling soft delete:</span></span> 
    
   ```
   $v = Get-AzureRmKeyVault -VaultName <vaultname>
   $r = Get-AzureRmResource -ResourceId $v.ResourceId
   $r.Properties | Add-Member -MemberType NoteProperty -Name enableSoftDelete -Value 'True'
   Set-AzureRmResource -ResourceId $r.ResourceId -Properties $r.Properties
   ``` 
    
3. <span data-ttu-id="e7e12-p137">Confirme a exclusão reversível está configurado para o chave vault executando o cmdlet **Get-AzureRmKeyVault** . Se a exclusão reversível está configurada corretamente para o armazenamento de chave, o Soft excluir habilitado? propriedade retorna um valor **True**:</span><span class="sxs-lookup"><span data-stu-id="e7e12-p137">Confirm soft delete is configured for the key vault by running the **Get-AzureRmKeyVault** cmdlet. If soft delete is configured properly for the key vault, then the  Soft Delete Enabled? property returns a value of **True**:</span></span> 
    
   ```
   Get-AzureRmKeyVault -VaultName <vaultname> | fl
   ```

   
    
### <a name="add-a-key-to-each-key-vault-either-by-creating-or-importing-a-key"></a><span data-ttu-id="e7e12-294">Adicionar uma chave para cada chave vault tanto criando ou importando uma chave</span><span class="sxs-lookup"><span data-stu-id="e7e12-294">Add a key to each key vault either by creating or importing a key</span></span>
<span data-ttu-id="e7e12-295"><a name="AddKeystoKeyVault"> </a></span><span class="sxs-lookup"><span data-stu-id="e7e12-295"></span></span>

<span data-ttu-id="e7e12-p138">Existem duas maneiras de adicionar chaves para um armazenamento de chave do Azure; Você pode criar uma chave diretamente no compartimento de chave, ou você pode importar uma chave. Criando uma chave diretamente no compartimento de chave é o método menos complicado, enquanto importando uma chave fornece um controle total sobre como a chave é gerada.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p138">There are two ways to add keys to an Azure Key Vault; you can create a key directly in Key Vault, or you can import a key. Creating a key directly in Key Vault is the less complicated method, while importing a key provides total control over how the key is generated.</span></span>
  
<span data-ttu-id="e7e12-298">Para criar uma chave diretamente no seu vault principal, execute o cmdlet [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e7e12-298">To create a key directly in your key vault, run the [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey) cmdlet as follows:</span></span> 
  
```
Add-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname> -Destination <HSM|Software> -KeyOps wrapKey,unwrapKey
```

<span data-ttu-id="e7e12-299">Onde:</span><span class="sxs-lookup"><span data-stu-id="e7e12-299">Where:</span></span>
  
-  <span data-ttu-id="e7e12-300">*vaultname* é o nome do chave vault no qual você deseja criar a chave.</span><span class="sxs-lookup"><span data-stu-id="e7e12-300">*vaultname*  is the name of the key vault in which you want to create the key.</span></span> 
    
-  <span data-ttu-id="e7e12-301">*nome chave* é o nome que você deseja conceder a nova chave.</span><span class="sxs-lookup"><span data-stu-id="e7e12-301">*keyname*  is the name you want to give the new key.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="e7e12-p139">Chaves de nome usando uma convenção de nomenclatura semelhante, conforme descrito acima para compartimentos principais. Dessa forma, nas ferramentas que mostram apenas o nome da chave, a cadeia de caracteres é Self descrevendo.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p139">Name keys using a similar naming convention as described above for key vaults. This way, in tools that show only the key name, the string is self-describing.</span></span> 
  
- <span data-ttu-id="e7e12-304">Se você pretende proteger a chave com um HSM, certifique-se de que você especifique **HSM** como o valor do parâmetro de _destino_ , caso contrário, especifique a **Software**.</span><span class="sxs-lookup"><span data-stu-id="e7e12-304">If you intend to protect the key with an HSM, ensure that you specify **HSM** as the value of the  _Destination_ parameter, otherwise, specify **Software**.</span></span>
    
<span data-ttu-id="e7e12-305">Por exemplo,</span><span class="sxs-lookup"><span data-stu-id="e7e12-305">For example,</span></span>
  
```
Add-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -Destination Software -KeyOps wrapKey,unwrapKey
```

<span data-ttu-id="e7e12-306">Para importar uma chave diretamente para sua chave vault, você precisa ter um nShield Thales módulo de segurança de Hardware.</span><span class="sxs-lookup"><span data-stu-id="e7e12-306">To import a key directly into your key vault, you need to have a Thales nShield Hardware Security Module.</span></span>
  
<span data-ttu-id="e7e12-307">Algumas organizações preferem essa abordagem para estabelecer o provenance de suas chaves e este método também fornece os seguintes:</span><span class="sxs-lookup"><span data-stu-id="e7e12-307">Some organizations prefer this approach to establish the provenance of their keys, and the this method also provides the following:</span></span>
  
- <span data-ttu-id="e7e12-308">O conjunto de ferramentas usado para importação inclui certificação de Thales não é exportável a chave Exchange chave KEK que é usado para criptografar a chave que é gerar e é gerado dentro de um genuíno HSM que foi fabricado pela Thales.</span><span class="sxs-lookup"><span data-stu-id="e7e12-308">The toolset used for import includes attestation from Thales that the Key Exchange Key (KEK) that is used to encrypt the key you generate is not exportable and is generated inside a genuine HSM that was manufactured by Thales.</span></span>
    
- <span data-ttu-id="e7e12-p140">O conjunto de ferramentas inclui certificação de Thales que o mundo da segurança do Windows Azure chave Vault também foi gerado em um genuíno HSM fabricado pela Thales. Essa certificação prova a você que Microsoft também está usando hardware de Thales autêntico.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p140">The toolset includes attestation from Thales that the Azure Key Vault security world was also generated on a genuine HSM manufactured by Thales. This attestation proves to you that Microsoft is also using genuine Thales hardware.</span></span>
    
<span data-ttu-id="e7e12-p141">Verifique com seu grupo de segurança para determinar se o attestations acima são necessárias. Para obter etapas detalhadas criar uma chave local e importá-lo para a sua chave vault, consulte [como gerar e transferir chaves protegidas HSM para armazenamento de chave do Windows Azure](https://azure.microsoft.com/documentation/articles/key-vault-hsm-protected-keys/). Use as instruções Azure para criar uma chave em cada compartimento principal.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p141">Check with your security group to determine if the above attestations are required. For detailed steps to create a key on-premises and import it into your key vault, see [How to generate and transfer HSM-protected keys for Azure Key Vault](https://azure.microsoft.com/documentation/articles/key-vault-hsm-protected-keys/). Use the Azure instructions to create a key in each key vault.</span></span>
  
### <a name="check-the-recovery-level-of-your-keys"></a><span data-ttu-id="e7e12-314">Marque o nível de recuperação de suas chaves</span><span class="sxs-lookup"><span data-stu-id="e7e12-314">Check the recovery level of your keys</span></span>
<span data-ttu-id="e7e12-315"><a name="CheckKeyRecoveryLevel"> </a></span><span class="sxs-lookup"><span data-stu-id="e7e12-315"></span></span>

<span data-ttu-id="e7e12-p142">O Office 365 exige que a assinatura do Windows Azure chave Vault está definida como não cancelar e se as teclas usadas pela chave cliente tem como exclusão reversível habilitado. Você pode confirmar isso examinando o nível de recuperação em suas chaves.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p142">Office 365 requires that the Azure Key Vault subscription is set to Do Not Cancel and that the keys used by Customer Key have soft delete enabled. You can confirm this by looking at the recovery level on your keys.</span></span>
  
<span data-ttu-id="e7e12-318">Para verificar o nível de recuperação de uma chave, no Azure PowerShell, execute o cmdlet Get-AzureKeyVaultKey da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e7e12-318">To check the recovery level of a key, in Azure PowerShell, run the Get-AzureKeyVaultKey cmdlet as follows:</span></span>
  
```
(Get-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname>).Attributes 
```

<span data-ttu-id="e7e12-319">Se a propriedade de _Nível de recuperação_ retornar qualquer coisa diferente de um valor de **Recuperável + ProtectedSubscription**, você precisará analisar este tópico e certifique-se de ter seguido todas as etapas para colocar a assinatura na lista não cancelar e que você tenha habilitado em cada um dos seus principais compartimentos como exclusão reversível.</span><span class="sxs-lookup"><span data-stu-id="e7e12-319">If the  _Recovery Level_ property returns anything other than a value of **Recoverable+ProtectedSubscription**, you will need to review this topic and ensure that you have followed all of the steps to put the subscription on the Do Not Cancel list and that you have soft delete enabled on each of your key vaults.</span></span>
  
### <a name="backup-azure-key-vault"></a><span data-ttu-id="e7e12-320">Backup Vault Azure de chave</span><span class="sxs-lookup"><span data-stu-id="e7e12-320">Backup Azure Key Vault</span></span>
<span data-ttu-id="e7e12-321"><a name="BackupAzureKeyVaultkeys"> </a></span><span class="sxs-lookup"><span data-stu-id="e7e12-321"></span></span>

<span data-ttu-id="e7e12-p143">Imediatamente após a criação ou qualquer alteração a uma chave, execute um backup e armazenar cópias do backup, online e offline. Cópias offline não devem estar conectadas para qualquer rede, como em um recurso de armazenamento físico de seguros ou comerciais. Pelo menos uma cópia de backup deve ser armazenada em um local que será acessível em caso de desastre. Os blobs backup são os meios exclusivo de restaurar o material da chave deve uma chave de chave Vault ser destruída permanentemente ou caso contrário, inoperante. Chaves que são externos para armazenamento de chave do Windows Azure e foram importadas para armazenamento de chave do Windows Azure não qualificados como um backup porque os metadados necessários para a chave do cliente usar a chave não existe com a chave externa. Somente um backup extraído do Azure chave Vault pode ser usado para operações de restauração com chave de cliente. Portanto, é essencial que um backup do Windows Azure chave Vault sejam feitas depois que uma chave é carregada ou criada.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p143">Immediately following creation or any change to a key, perform a backup and store copies of the backup, both online and offline. Offline copies should not be connected to any network, such as in a physical safe or commercial storage facility. At least one copy of the backup should be stored in a location that will be accessible in the event of a disaster. The backup blobs are the sole means of restoring key material should a Key Vault key be permanently destroyed or otherwise rendered inoperable. Keys that are external to Azure Key Vault and were imported to Azure Key Vault do not qualify as a backup because the metadata necessary for Customer Key to use the key does not exist with the external key. Only a backup taken from Azure Key Vault can be used for restore operations with Customer Key. Therefore, it is essential that a backup of Azure Key Vault be made once a key is uploaded or created.</span></span>
  
<span data-ttu-id="e7e12-329">Para criar um backup de uma chave de armazenamento de chave do Windows Azure, execute o cmdlet [Backup-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Backup-AzureKeyVaultKey) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e7e12-329">To create a backup of an Azure Key Vault key, run the [Backup-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Backup-AzureKeyVaultKey) cmdlet as follows:</span></span>
```
Backup-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname> 
-OutputFile <filename .backup>

```

<span data-ttu-id="e7e12-330">Certifique-se de que o seu arquivo de saída usa o sufixo `.backup`.</span><span class="sxs-lookup"><span data-stu-id="e7e12-330">Ensure that your output file uses the suffix  `.backup`.</span></span>
  
<span data-ttu-id="e7e12-p144">O arquivo de saída resultante desse cmdlet é criptografado e não pode ser usado fora do Azure chave Vault. O backup pode ser restaurado somente a partir do qual foi feito o backup de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p144">The output file resulting from this cmdlet is encrypted and cannot be used outside of Azure Key Vault. The backup can be restored only to the Azure subscription from which the backup was taken.</span></span>
  
> [!TIP]
> <span data-ttu-id="e7e12-p145">Para o arquivo de saída, escolha uma combinação de seu nome de armazenamento e o nome da chave. Isso fará com que o arquivo nome definido de forma automática. Ele também assegurará que os nomes de arquivo de backup não coincidem.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p145">For the output file, choose a combination of your vault name and key name. This will make the file name self-describing. It will also ensure that backup file names do not collide.</span></span> 
  
<span data-ttu-id="e7e12-336">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="e7e12-336">For example:</span></span>
  
```
Backup-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -OutputFile Contoso-O365EX-NA-VaultA1-Key001-Backup-20170802.backup
```

### <a name="validate-azure-key-vault-configuration-settings"></a><span data-ttu-id="e7e12-337">Validar as definições de configuração de armazenamento de chave do Windows Azure</span><span class="sxs-lookup"><span data-stu-id="e7e12-337">Validate Azure Key Vault configuration settings</span></span>
<span data-ttu-id="e7e12-338"><a name="Validateconfiguration"> </a></span><span class="sxs-lookup"><span data-stu-id="e7e12-338"></span></span>

<span data-ttu-id="e7e12-p146">Executar a validação antes de usar um DEP chaves é opcional, mas altamente recomendado. Em particular, se você usar as etapas para configurar chaves e compartimentos que seja diferente dos descritos neste tópico, você deve validar a integridade de seus recursos do Windows Azure chave Vault antes de configurar a chave do cliente.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p146">Performing validation before using keys in a DEP is optional, but highly recommended. In particular, if you use steps to set up your keys and vaults other than the ones described in this topic, you should validate the health of your Azure Key Vault resources before you configure Customer Key.</span></span>
  
<span data-ttu-id="e7e12-341">Para verificar que sua chaves têm operações get, wrapKey e unwrapKey habilitadas:</span><span class="sxs-lookup"><span data-stu-id="e7e12-341">To verify that your keys have get, wrapKey, and unwrapKey operations enabled:</span></span>
  
<span data-ttu-id="e7e12-342">Execute o cmdlet [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureRmKeyVault) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e7e12-342">Run the [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureRmKeyVault) cmdlet as follows:</span></span> 
  
```
Get-AzureRMKeyVault -VaultName <vaultname>
```

<span data-ttu-id="e7e12-p147">Na saída, procure para a política de acesso e para a identidade (GUID) do Exchange Online ou a identidade do SharePoint Online (GUID), conforme apropriado. Todos os três das permissões acima devem ser mostrados em permissões às chaves.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p147">In the output, look for the Access Policy and for the Exchange Online identity (GUID) or the SharePoint Online identity (GUID) as appropriate. All three of the above permissions must be shown under Permissions to Keys.</span></span>
  
<span data-ttu-id="e7e12-345">Se a configuração de política de acesso estiver incorreta, execute o cmdlet Set-AzureRmKeyVaultAccessPolicy da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e7e12-345">If the access policy configuration is incorrect, run the Set-AzureRmKeyVaultAccessPolicy cmdlet as follows:</span></span>
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName <Office 365 appID>
```

<span data-ttu-id="e7e12-346">Por exemplo, para o Exchange Online e Skype para negócios:</span><span class="sxs-lookup"><span data-stu-id="e7e12-346">For example, for Exchange Online and Skype for Business:</span></span>
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
-PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000002-0000-0ff1-ce00-000000000000
```

<span data-ttu-id="e7e12-347">Por exemplo, para o SharePoint Online e OneDrive for Business:</span><span class="sxs-lookup"><span data-stu-id="e7e12-347">For example, for SharePoint Online and OneDrive for Business:</span></span>
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365SP-NA-VaultA1 
-PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName TBD
```

<span data-ttu-id="e7e12-348">Para verificar se uma data de validade não está definida para essas chaves, executados o cmdlet [Get-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureKeyVaultKey) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e7e12-348">To verify that an expiration date is not set for your keys run the [Get-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureKeyVaultKey) cmdlet as follows:</span></span> 
  
```
Get-AzureKeyVaultKey -VaultName <vaultname> 
```

<span data-ttu-id="e7e12-p148">Uma chave expirada não pode ser usada pela chave cliente e operações tentadas com uma chave expirada irá falhar e possivelmente resultar em uma interrupção de serviço. É altamente recomendável que chaves usadas com a chave do cliente não têm uma data de validade. Uma data de expiração, depois que set, não podem ser removidas, mas pode ser alterada para uma data diferente. Se uma chave deve ser usada com uma data de validade definido, altere o valor de expiração para 31/12/9999. Chaves com uma data de validade é definido como uma data diferente de 31/12/9999 não passará a validação do Office 365.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p148">An expired key cannot be used by Customer Key and operations attempted with an expired key will fail, and possibly result in a service outage. We strongly recommend that keys used with Customer Key do not have an expiration date. An expiration date, once set, cannot be removed, but can be changed to a different date. If a key must be used that has an expiration date set, change the expiration value to 12/31/9999. Keys with an expiration date set to a date other than 12/31/9999 will not pass Office 365 validation.</span></span>
  
<span data-ttu-id="e7e12-354">Para alterar uma data de validade tiver sido definida como qualquer valor diferente de 31/12/9999, execute o cmdlet [Set-AzureKeyVaultKeyAttribute](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Set-AzureKeyVaultKeyAttribute) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e7e12-354">To change an expiration date that has been set to any value other than 12/31/9999, run the [Set-AzureKeyVaultKeyAttribute](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Set-AzureKeyVaultKeyAttribute) cmdlet as follows:</span></span> 
  
```
Set-AzureKeyVaultKeyAttribute -VaultName <vaultname> -Name <keyname> 
-Expires (Get-Date -Date "12/31/9999")
```

> [!CAUTION]
> <span data-ttu-id="e7e12-355">Não defina datas de expiração sobre chaves de criptografia, que você pode usar com a chave do cliente.</span><span class="sxs-lookup"><span data-stu-id="e7e12-355">Don't set expiration dates on encryption keys you use with Customer Key.</span></span> 
  
### <a name="obtain-the-uri-for-each-azure-key-vault-key"></a><span data-ttu-id="e7e12-356">Obter o URI para cada chave Vault de chave do Windows Azure</span><span class="sxs-lookup"><span data-stu-id="e7e12-356">Obtain the URI for each Azure Key Vault key</span></span>
<span data-ttu-id="e7e12-357"><a name="GetKeyURI"> </a></span><span class="sxs-lookup"><span data-stu-id="e7e12-357"></span></span>

<span data-ttu-id="e7e12-p149">Depois de ter concluído todas as etapas no Windows Azure para configurar suas chaves compartimentos e adicionou seus chaves, execute o seguinte comando para obter o URI para a chave em cada compartimento principal. Você precisará usar esses URIs quando você cria e atribuir cada DEP posteriormente, portanto, salve essas informações em um local seguro. Lembre-se de executar esse comando uma vez para cada chave vault.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p149">Once you have completed all the steps in Azure to set up your key vaults and added your keys, run the following command to get the URI for the key in each key vault. You will need to use these URIs when you create and assign each DEP later, so save this information in a safe place. Remember to run this command once for each key vault.</span></span>
  
<span data-ttu-id="e7e12-361">No PowerShell do Azure:</span><span class="sxs-lookup"><span data-stu-id="e7e12-361">In Azure PowerShell:</span></span>
  
```
(Get-AzureKeyVaultKey -VaultName <vaultname>).Id
```

## <a name="office-365-setting-up-customer-key-for-exchange-online-and-skype-for-business"></a><span data-ttu-id="e7e12-362">Office 365: Configurando a chave do cliente para o Exchange Online e Skype para negócios</span><span class="sxs-lookup"><span data-stu-id="e7e12-362">Office 365: Setting up Customer Key for Exchange Online and Skype for Business</span></span>
<span data-ttu-id="e7e12-363"><a name="AzureSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="e7e12-363"></span></span>

<span data-ttu-id="e7e12-p150">Antes de começar, certifique-se de que você concluiu as tarefas necessárias para configurar o armazenamento de chave do Windows Azure. Consulte [Concluir tarefas no Azure chave Vault e Microsoft FastTrack para a chave do cliente](controlling-your-data-using-customer-key.md#AzureSteps) para obter informações.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p150">Before you begin, ensure that you have completed the tasks required to set up Azure Key Vault. See [Complete tasks in Azure Key Vault and Microsoft FastTrack for Customer Key](controlling-your-data-using-customer-key.md#AzureSteps) for information.</span></span> 
  
<span data-ttu-id="e7e12-366">Para configurar a chave do cliente para o Exchange Online e Skype for Business, você precisará executar estas etapas conectando remotamente ao Exchange Online com o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e7e12-366">To set up Customer Key for Exchange Online and Skype for Business, you will need to perform these steps by remotely connecting to Exchange Online with Windows PowerShell.</span></span>
  
### <a name="create-a-data-encryption-policy-dep-for-use-with-exchange-online-and-skype-for-business"></a><span data-ttu-id="e7e12-367">Criar uma política de criptografia de dados (DEP) para uso com o Exchange Online e Skype para negócios</span><span class="sxs-lookup"><span data-stu-id="e7e12-367">Create a data encryption policy (DEP) for use with Exchange Online and Skype for Business</span></span>
<span data-ttu-id="e7e12-368"><a name="CreateDEP4EXOSkype"> </a></span><span class="sxs-lookup"><span data-stu-id="e7e12-368"></span></span>

<span data-ttu-id="e7e12-p151">Um DEP é associado um conjunto de chaves armazenadas no compartimento de chave do Windows Azure. Você pode atribuir um DEP uma caixa de correio no Office 365. O Office 365, em seguida, usará as teclas identificadas na política para criptografar a caixa de correio. Para criar a DEP, você precisa ter os URIs de Vault chave tiver obtido anteriormente. Consulte [obter o URI para cada chave Azure chave Vault](controlling-your-data-using-customer-key.md#GetKeyURI) para obter instruções.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p151">A DEP is associated with a set of keys stored in Azure Key Vault. You assign a DEP to a mailbox in Office 365. Office 365 will then use the keys identified in the policy to encrypt the mailbox. To create the DEP, you need the Key Vault URIs you obtained earlier. See [Obtain the URI for each Azure Key Vault key](controlling-your-data-using-customer-key.md#GetKeyURI) for instructions.</span></span> 
  
<span data-ttu-id="e7e12-p152">Lembre-se! Quando você cria um DEP, você pode especificar duas chaves que residem em dois compartimentos diferentes de chave do Azure. Certifique-se de que essas chaves estão localizados em duas regiões Azure separados para garantir a redundância de geo.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p152">Remember! When you create a DEP, you specify two keys that reside in two different Azure Key Vaults. Ensure that these keys are located in two separate Azure regions to ensure geo-redundancy.</span></span>
  
<span data-ttu-id="e7e12-377">Para criar a DEP, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="e7e12-377">To create the DEP, follow these steps:</span></span>
  
1. <span data-ttu-id="e7e12-378">No computador local, usando uma conta de trabalho ou da escola que tenha permissões de administrador global na sua organização do Office 365, [se conectar ao Exchange Online PowerShell](https://technet.microsoft.com/en-us/library/jj984289%28v=exchg.160%29.aspx) abrindo o Windows PowerShell e executando o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="e7e12-378">On your local computer, using a work or school account that has global administrator permissions in your Office 365 organization, [connect to Exchange Online PowerShell](https://technet.microsoft.com/en-us/library/jj984289%28v=exchg.160%29.aspx) by opening Windows PowerShell and running the following command.</span></span> 
    
   ```
   $UserCredential = Get-Credential
   ```

2. <span data-ttu-id="e7e12-379">Na caixa de diálogo solicitação de credencial do Windows PowerShell, insira seu trabalho ou escola informações da conta, clique **Okey**e, em seguida, insira o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="e7e12-379">In the Windows PowerShell Credential Request dialog box, enter your work or school account information, click **OK**, and then enter the following command.</span></span> 
    
   ```
   $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://outlook.office365.com/powershell-liveid/ -Credential $UserCredential -Authentication Basic -AllowRedirection
   ```

3. <span data-ttu-id="e7e12-380">Execute o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="e7e12-380">Run the following command.</span></span>
    
   ```
   Import-PSSession $Session
   ```

4. <span data-ttu-id="e7e12-381">Para criar um DEP, use o cmdlet New-DataEncryptionPolicy digitando o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="e7e12-381">To create a DEP, use the New-DataEncryptionPolicy cmdlet by typing the following command.</span></span>
    
   ```
   New-DataEncryptionPolicy -Name <PolicyName> -Description "PolicyDescription " -AzureKeyIDs <KeyVaultURI1>, <KeyVaultURI2>
   ```

   <span data-ttu-id="e7e12-382">Onde:</span><span class="sxs-lookup"><span data-stu-id="e7e12-382">Where:</span></span>
    
   -  <span data-ttu-id="e7e12-p153">*PolicyName* é o nome que você deseja usar para a política. Nomes não podem conter espaços. Por exemplo, USA_mailboxes.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p153">*PolicyName*  is the name you want to use for the policy. Names cannot contain spaces. For example, USA_mailboxes.</span></span> 
    
   -  <span data-ttu-id="e7e12-p154">*PolicyDescription* é uma descrição amigável da política que o ajudará a se lembrar o que é a política por. Você pode incluir espaços na descrição. Por exemplo, raiz chave para caixas de correio nos Estados Unidos e seus territórios.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p154">*PolicyDescription*  is a user friendly description of the policy that will help you remember what the policy is for. You can include spaces in the description. For example, Root key for mailboxes in USA and its territories.</span></span> 
    
   -  <span data-ttu-id="e7e12-p155">*KeyVaultURI1* é o URI para a primeira chave na política. Por exemplo, https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p155">*KeyVaultURI1*  is the URI for the first key in the policy. For example, https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01.</span></span> 
    
   -  <span data-ttu-id="e7e12-p156">*KeyVaultURI2* é o URI para a segunda chave na política. Por exemplo, https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02. Separe os URIs de dois por uma vírgula e um espaço.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p156">*KeyVaultURI2*  is the URI for the second key in the policy. For example, https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02. Separate the two URIs by a comma and a space.</span></span> 
    
   <span data-ttu-id="e7e12-394">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="e7e12-394">Example:</span></span>
  
   ```
   New-DataEncryptionPolicy -Name USA_mailboxes -Description "Root key for mailboxes in USA and its territories" -AzureKeyIDs https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01, https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02
   ```

### <a name="assign-a-dep-to-a-mailbox"></a><span data-ttu-id="e7e12-395">Atribuir um DEP a uma caixa de correio</span><span class="sxs-lookup"><span data-stu-id="e7e12-395">Assign a DEP to a mailbox</span></span>
<span data-ttu-id="e7e12-396"><a name="assignDEPtomailbox"> </a></span><span class="sxs-lookup"><span data-stu-id="e7e12-396"></span></span>

<span data-ttu-id="e7e12-p157">Atribua a DEP a uma caixa de correio usando o cmdlet Set-Mailbox. Depois de atribuir a política, o Office 365 pode criptografar a caixa de correio com a chave designada na DEP.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p157">Assign the DEP to a mailbox by using the Set-Mailbox cmdlet. Once you assign the policy, Office 365 can encrypt the mailbox with the key designated in the DEP.</span></span>
  
```
Set-Mailbox -Identity <MailboxIdParameter> -DataEncryptionPolicy <PolicyName>
```

<span data-ttu-id="e7e12-p158">Onde *MailboxIdParameter* Especifica uma caixa de correio. Para obter mais informações sobre o cmdlet Set-Mailbox, consulte [Set-Mailbox](https://technet.microsoft.com/library/bb123981%28v=exchg.160%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="e7e12-p158">Where *MailboxIdParameter* specifies a mailbox. For more information about the Set-Mailbox cmdlet, see [Set-Mailbox](https://technet.microsoft.com/library/bb123981%28v=exchg.160%29.aspx).</span></span>
  
### <a name="validate-mailbox-encryption"></a><span data-ttu-id="e7e12-401">Validar a criptografia de caixa de correio</span><span class="sxs-lookup"><span data-stu-id="e7e12-401">Validate mailbox encryption</span></span>
<span data-ttu-id="e7e12-402"><a name="validatemailboxencryption"> </a></span><span class="sxs-lookup"><span data-stu-id="e7e12-402"></span></span>

<span data-ttu-id="e7e12-p159">Criptografar uma caixa de correio pode levar algum tempo. Para atribuição de política de tempo primeira, a caixa de correio também deverá concluir a movimentação de um banco de dados para outro antes que o serviço pode criptografar a caixa de correio. Recomendamos que você aguardar 72 horas antes de tentar validar criptografia depois que você alterar um DEP ou na primeira vez que você atribua um DEP uma caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p159">Encrypting a mailbox can take some time. For first time policy assignment, the mailbox must also complete the move from one database to another before the service can encrypt the mailbox. We recommend that you wait 72 hours before you attempt to validate encryption after you change a DEP or the first time you assign a DEP to a mailbox.</span></span>
  
<span data-ttu-id="e7e12-406">Use o cmdlet Get-MailboxStatistics para determinar se uma caixa de correio é criptografada.</span><span class="sxs-lookup"><span data-stu-id="e7e12-406">Use the Get-MailboxStatistics cmdlet to determine if a mailbox is encrypted.</span></span>
  
```
Get-MailboxStatistics -Identity <GeneralMailboxOrMailUserIdParameter> | fl IsEncrypted
```

<span data-ttu-id="e7e12-407">A propriedade IsEncrypted retorna um valor de **true** se a caixa de correio é criptografada e um valor **false** se a caixa de correio não é criptografada.</span><span class="sxs-lookup"><span data-stu-id="e7e12-407">The IsEncrypted property returns a value of **true** if the mailbox is encrypted and a value of **false** if the mailbox is not encrypted.</span></span> 

<span data-ttu-id="e7e12-p160">O tempo para concluir as movimentações de caixa de correio depende do número de caixas de correio à qual você atribui um DEP pela primeira vez, bem como o tamanho das caixas de correio. Se as caixas de correio não foram criptografadas depois de uma semana desde o momento em que você atribuiu a DEP, inicie uma movimentação de caixa de correio para as caixas de correio não criptografadas usando o cmdlet New-MoveRequest.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p160">The time to complete mailbox moves depends on the number of mailboxes to which you assign a DEP for the first time, as well as the size of the mailboxes. If the mailboxes have not been encrypted after a week from the time you assigned the DEP, initiate a mailbox move for the unencrypted mailboxes by using the New-MoveRequest cmdlet.</span></span>

```
New-MoveRequest <mailbox alias>
``` 

## <a name="office-365-setting-up-customer-key-for-sharepoint-online-and-onedrive-for-business"></a><span data-ttu-id="e7e12-410">Office 365: Configurando a chave do cliente para o SharePoint Online e o OneDrive for Business</span><span class="sxs-lookup"><span data-stu-id="e7e12-410">Office 365: Setting up Customer Key for SharePoint Online and OneDrive for Business</span></span>
<span data-ttu-id="e7e12-411"><a name="AzureSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="e7e12-411"></span></span>

<span data-ttu-id="e7e12-p161">Antes de começar, certifique-se de que você concluiu as tarefas necessárias para configurar o armazenamento de chave do Windows Azure. Consulte [Concluir tarefas no Azure chave Vault e Microsoft FastTrack para a chave do cliente](controlling-your-data-using-customer-key.md#AzureSteps) para obter informações.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p161">Before you begin, ensure that you have completed the tasks required to set up Azure Key Vault. See [Complete tasks in Azure Key Vault and Microsoft FastTrack for Customer Key](controlling-your-data-using-customer-key.md#AzureSteps) for information.</span></span> 
  
<span data-ttu-id="e7e12-414">Para configurar a chave do cliente para o SharePoint Online e o OneDrive for Business, você precisará executar estas etapas conectando remotamente ao SharePoint Online com o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e7e12-414">To set up Customer Key for SharePoint Online and OneDrive for Business, you will need to perform these steps by remotely connecting to SharePoint Online with Windows PowerShell.</span></span>
  
### <a name="create-a-data-encryption-policy-dep-for-each-sharepoint-online-and-onedrive-for-business-geo"></a><span data-ttu-id="e7e12-415">Criar uma diretiva de criptografia de dados (DEP) para cada SharePoint Online e o OneDrive for Business geo</span><span class="sxs-lookup"><span data-stu-id="e7e12-415">Create a data encryption policy (DEP) for each SharePoint Online and OneDrive for Business geo</span></span>
<span data-ttu-id="e7e12-416"><a name="CreateDEP4SPOODfB"> </a></span><span class="sxs-lookup"><span data-stu-id="e7e12-416"></span></span>

<span data-ttu-id="e7e12-p162">Um DEP é associado um conjunto de chaves armazenadas no compartimento de chave do Windows Azure. Você pode aplicar um DEP para todos os seus dados em uma localidade geográfica, também chamada de um geo. Se você usar o recurso de multi-geo do Office 365 (atualmente na visualização), você pode criar um DEP por geo. Se você não estiver usando multi-geo, você pode criar um DEP no Office 365 para uso com o SharePoint Online e o OneDrive for Business. O Office 365, em seguida, usará as teclas identificadas na DEP para criptografar dados em que geo. Para criar a DEP, você precisa ter os URIs de Vault chave tiver obtido anteriormente. Consulte [obter o URI para cada chave Azure chave Vault](controlling-your-data-using-customer-key.md#GetKeyURI) para obter instruções.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p162">A DEP is associated with a set of keys stored in Azure Key Vault. You apply a DEP to all of your data in one geographic location, also called a geo. If you use the multi-geo feature of Office 365 (currently in Preview), you can create one DEP per geo. If you are not using multi-geo, you can create one DEP in Office 365 for use with SharePoint Online and OneDrive for Business. Office 365 will then use the keys identified in the DEP to encrypt your data in that geo. To create the DEP, you need the Key Vault URIs you obtained earlier. See [Obtain the URI for each Azure Key Vault key](controlling-your-data-using-customer-key.md#GetKeyURI) for instructions.</span></span> 
  
<span data-ttu-id="e7e12-p163">Lembre-se! Quando você cria um DEP, você pode especificar duas chaves que residem em dois compartimentos diferentes de chave do Azure. Certifique-se de que essas chaves estão localizados em duas regiões Azure separados para garantir a redundância de geo.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p163">Remember! When you create a DEP, you specify two keys that reside in two different Azure Key Vaults. Ensure that these keys are located in two separate Azure regions to ensure geo-redundancy.</span></span>
  
<span data-ttu-id="e7e12-427">Para criar um DEP, você precisará conectar-se remotamente ao SharePoint Online usando o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e7e12-427">To create a DEP, you need to remotely connect to SharePoint Online by using Windows PowerShell.</span></span>
  
1. <span data-ttu-id="e7e12-428">No computador local, usando uma conta de trabalho ou da escola que tenha permissões de administrador global na sua organização do Office 365, [se conectar ao Powershell do SharePoint Online](https://technet.microsoft.com/library/fp161372.aspx).</span><span class="sxs-lookup"><span data-stu-id="e7e12-428">On your local computer, using a work or school account that has global administrator permissions in your Office 365 organization, [Connect to SharePoint Online Powershell](https://technet.microsoft.com/library/fp161372.aspx).</span></span>
    
2. <span data-ttu-id="e7e12-429">No Microsoft SharePoint Online Management Shell, execute o cmdlet [Register-SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843950.aspx) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e7e12-429">In the Microsoft SharePoint Online Management Shell, run the [Register-SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843950.aspx) cmdlet as follows:</span></span> 
    
   ```
   Register-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl> -PrimaryKeyVaultName <PrimaryKeyVaultName> -PrimaryKeyName <PrimaryKeyName> -PrimaryKeyVersion <PrimaryKeyVersion> -SecondaryKeyVaultName <SecondaryKeyVaultName> -SecondaryKeyName <SecondaryKeyName> -SecondaryKeyVersion <SecondaryKeyVersion>
   ```

   <span data-ttu-id="e7e12-p164">Ao registrar a DEP, criptografia começa nos dados do geo. Isso pode levar algum tempo.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p164">When you register the DEP, encryption begins on the data in the geo. This can take some time.</span></span>
    
### <a name="validate-encryption-of-group-sites-team-sites-and-onedrive-for-business"></a><span data-ttu-id="e7e12-432">Validar a criptografia do grupo de Sites, Sites de equipe e OneDrive for Business</span><span class="sxs-lookup"><span data-stu-id="e7e12-432">Validate encryption of Group Sites, Team Sites, and OneDrive for Business</span></span>
<span data-ttu-id="e7e12-433"><a name="validateencryptionSPO"> </a></span><span class="sxs-lookup"><span data-stu-id="e7e12-433"></span></span>

<span data-ttu-id="e7e12-434">Você pode verificar o status de criptografia, executando o cmdlet Get-SPODataEncryptionPolicy da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e7e12-434">You can check on the status of encryption by running the Get-SPODataEncryptionPolicy cmdlet as follows:</span></span>
  
```
Get-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl>
```

<span data-ttu-id="e7e12-435">A saída desse cmdlet inclui:</span><span class="sxs-lookup"><span data-stu-id="e7e12-435">The output from this cmdlet includes:</span></span>
  
- <span data-ttu-id="e7e12-436">O URI da chave primária.</span><span class="sxs-lookup"><span data-stu-id="e7e12-436">The URI of the primary key.</span></span>
    
- <span data-ttu-id="e7e12-437">O URI da chave secundário.</span><span class="sxs-lookup"><span data-stu-id="e7e12-437">The URI of the secondary key.</span></span>
    
- <span data-ttu-id="e7e12-p165">O status de criptografia para o geo. Estados possíveis incluem:</span><span class="sxs-lookup"><span data-stu-id="e7e12-p165">The encryption status for the geo. Possible states include:</span></span>
    
  - <span data-ttu-id="e7e12-440">**Não registrados:** Criptografia de chave do cliente ainda não tiver sido aplicada.</span><span class="sxs-lookup"><span data-stu-id="e7e12-440">**Unregistered:** Customer Key encryption has not yet been applied.</span></span> 
    
  - <span data-ttu-id="e7e12-p166">**Registrando:** Criptografia de chave do cliente tiver sido aplicada e seus arquivos estiverem sendo criptografado. Se seu geo estiver nesse estado, você vai também ser mostradas informações na qual o percentual de sites no geo forem concluídas, para que você pode monitorar o progresso de criptografia.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p166">**Registering:** Customer Key encryption has been applied and your files are in the process of being encrypted. If your geo is in this state, you'll also be shown information on what percentage of sites in the geo are complete so that you can monitor encryption progress.</span></span> 
    
  - <span data-ttu-id="e7e12-443">**Registrado:** Criptografia de chave do cliente tiver sido aplicada e todos os arquivos em todos os sites foram criptografados.</span><span class="sxs-lookup"><span data-stu-id="e7e12-443">**Registered:** Customer Key encryption has been applied, and all files in all sites have been encrypted.</span></span> 
    
  - <span data-ttu-id="e7e12-p167">**Aplicação:** Uma chave roll está em andamento. Se seu geo estiver nesse estado, você vai também ser mostradas informações na qual o percentual de sites concluiu a operação roll principais para que você pode monitorar o andamento.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p167">**Rolling:** A key roll is in progress. If your geo is in this state, you'll also be shown information on what percentage of sites have completed the key roll operation so that you can monitor progress.</span></span> 
    
## <a name="managing-customer-key-for-office-365"></a><span data-ttu-id="e7e12-446">Gerenciando a chave do cliente para o Office 365</span><span class="sxs-lookup"><span data-stu-id="e7e12-446">Managing Customer Key for Office 365</span></span>
<span data-ttu-id="e7e12-447"><a name="ManageCustomerKey"> </a></span><span class="sxs-lookup"><span data-stu-id="e7e12-447"></span></span>

<span data-ttu-id="e7e12-448">Depois que você definiu o backup da chave de cliente para o Office 365, você pode executar essas tarefas de gerenciamento adicionais.</span><span class="sxs-lookup"><span data-stu-id="e7e12-448">After you've set up Customer Key for Office 365, you can perform these additional management tasks.</span></span>
  
- [<span data-ttu-id="e7e12-449">Restaurar as chaves do Azure chave Vault</span><span class="sxs-lookup"><span data-stu-id="e7e12-449">Restore Azure Key Vault keys</span></span>](controlling-your-data-using-customer-key.md#RestoreAzureKeyVaultKeys)
    
- [<span data-ttu-id="e7e12-450">Sem interrupção ou girando uma chave no Azure chave Vault que você pode usar com a chave do cliente</span><span class="sxs-lookup"><span data-stu-id="e7e12-450">Rolling or rotating a key in Azure Key Vault that you use with Customer Key</span></span>](controlling-your-data-using-customer-key.md#RollCKkey)
    
- [<span data-ttu-id="e7e12-451">Gerenciar permissões de chave vault</span><span class="sxs-lookup"><span data-stu-id="e7e12-451">Manage key vault permissions</span></span>](controlling-your-data-using-customer-key.md#Managekeyvaultperms)
    
- [<span data-ttu-id="e7e12-452">Determinar a DEP atribuída a uma caixa de correio</span><span class="sxs-lookup"><span data-stu-id="e7e12-452">Determine the DEP assigned to a mailbox</span></span>](controlling-your-data-using-customer-key.md#DeterminemailboxDEP)
    
### <a name="restore-azure-key-vault-keys"></a><span data-ttu-id="e7e12-453">Restaurar as chaves do Azure chave Vault</span><span class="sxs-lookup"><span data-stu-id="e7e12-453">Restore Azure Key Vault keys</span></span>
<span data-ttu-id="e7e12-454"><a name="RestoreAzureKeyVaultKeys"> </a></span><span class="sxs-lookup"><span data-stu-id="e7e12-454"></span></span>

<span data-ttu-id="e7e12-p168">Antes de executar uma restauração, use os recursos de recuperação fornecidos pela exclusão reversível. Todas as chaves que são usadas com a chave do cliente serão necessárias ter habilitada como exclusão reversível. Exclusão reversível funciona como uma Lixeira e permite a recuperação por até 90 dias sem a necessidade de restauração. Restore só deve ser necessário em circunstâncias extremas ou incomuns, por exemplo, se a tecla ou vault chave for perdido. Se precisar restaurar uma chave para uso com a chave do cliente no Azure PowerShell, execute o cmdlet Restore-AzureKeyVaultKey da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e7e12-p168">Before performing a restore, use the recovery capabilities provided by soft delete. All keys that are used with Customer Key are required to have soft delete enabled. Soft delete acts like a recycle bin and allows recovery for up to 90 days without the need to restore. Restore should only be required in extreme or unusual circumstances, for example if the key or key vault is lost. If you must restore a key for use with Customer Key, in Azure PowerShell, run the Restore-AzureKeyVaultKey cmdlet as follows:</span></span>
  
```
Restore-AzureKeyVaultKey -VaultName <vaultname> -InputFile <filename>
```

<span data-ttu-id="e7e12-460">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="e7e12-460">For example:</span></span>
  
```
Restore-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -InputFile Contoso-O365EX-NA-VaultA1-Key001-Backup-20170802.backup
```

<span data-ttu-id="e7e12-p169">Se uma chave com o mesmo nome já existir no compartimento principal, haverá falha na operação de restauração. Restore-AzureKeyVaultKey restaura todas as versões principais e todos os metadados para a chave, incluindo o nome da chave.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p169">If a key with the same name already exists in the key vault, the restore operation will fail. Restore-AzureKeyVaultKey restores all key versions and all metadata for the key including the key name.</span></span>
  
### <a name="rolling-or-rotating-a-key-in-azure-key-vault-that-you-use-with-customer-key"></a><span data-ttu-id="e7e12-463">Sem interrupção ou girando uma chave no Azure chave Vault que você pode usar com a chave do cliente</span><span class="sxs-lookup"><span data-stu-id="e7e12-463">Rolling or rotating a key in Azure Key Vault that you use with Customer Key</span></span>
<span data-ttu-id="e7e12-464"><a name="RollCKkey"> </a></span><span class="sxs-lookup"><span data-stu-id="e7e12-464"></span></span>

<span data-ttu-id="e7e12-p170">Aplicação de chaves não é necessário por qualquer um dos Vault de chave do Windows Azure ou por chave de cliente. Além disso, as chaves são protegidas com um HSM são praticamente impossíveis comprometer. Mesmo se uma chave raiz estavam em posse de um ator mal-intencionado não há nenhum significa viável de usá-lo para descriptografar os dados, desde que apenas o Office 365 código sabe como usá-lo. No entanto, a aplicação de uma chave é suportado pela chave do cliente.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p170">Rolling keys is not required by either Azure Key Vault or by Customer Key. In addition, keys that are protected with an HSM are virtually impossible to compromise. Even if a root key were in the possession of a malicious actor there is no feasible means of using it to decrypt data, since only Office 365 code knows how to use it. However, rolling a key is supported by Customer Key.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="e7e12-p171">Rolo apenas uma chave de criptografia que usados com a chave do cliente quando existe um motivo desmarque técnico ou um requisito de conformidade dita que você precisa aplicar a chave. Além disso, não exclua todas as chaves que estão ou estavam associadas a políticas. Quando você distribuir seu chaves, haverá a ser conteúdo criptografado com as chaves anteriores. Por exemplo, enquanto caixas de correio ativas serão novamente criptografadas com frequência, inativa, caixas de correio desconectadas e desabilitadas ainda podem ser criptografadas com as chaves anteriores. SharePoint Online executa backup de conteúdo para fins de restauração e recuperação, portanto talvez ainda haja conteúdo arquivado usando as teclas mais antigas.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p171">Only roll an encryption key that you use with Customer Key when a clear technical reason exists or a compliance requirement dictates that you have to roll the key. In addition, do not delete any keys that are or were associated with policies. When you roll your keys, there will be content encrypted with the previous keys. For example, while active mailboxes will be re-encrypted frequently, inactive, disconnected, and disabled mailboxes may still be encrypted with the previous keys. SharePoint Online performs backup of content for restore and recovery purposes, so there may still be archived content using older keys. </span></span><br/> <span data-ttu-id="e7e12-p172">Para garantir a segurança dos seus dados, SharePoint Online permitirá que não mais de uma operação de chave rolo estejam em andamento por vez. Se você deseja implantar ambas as chaves de um armazenamento de chave, você precisará aguardar a primeira operação chave roll totalmente concluída. Nossa recomendação é escalonar suas operações roll principais em intervalos diferentes, para que isso não é um problema.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p172">To ensure the safety of your data, SharePoint Online will allow no more than one Key Roll operation to be in progress at a time. If you want to roll both of the keys in a key vault, you'll need to wait for the first key roll operation to fully complete. Our recommendation is to stagger your key roll operations at different intervals, so that this is not an issue.</span></span> 
  
<span data-ttu-id="e7e12-p173">Quando você lançar uma chave, você está solicitando uma nova versão de uma chave existente. Para solicitar uma nova versão de uma chave existente, você pode usar o mesmo cmdlet, [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey), com a mesma sintaxe que você usou para criar a chave em primeiro lugar.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p173">When you roll a key, you are requesting a new version of an existing key. In order to request a new version of an existing key, you use the same cmdlet, [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey), with the same syntax that you used to create the key in the first place.</span></span>
  
<span data-ttu-id="e7e12-479">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="e7e12-479">For example:</span></span>
  
```
Add-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -Destination HSM -KeyOps @('wrapKey','unwrapKey') -NotBefore (Get-Date -Date "12/27/2016 12:01 AM")
```

<span data-ttu-id="e7e12-p174">Neste exemplo, desde que uma chave chamada **Contoso-O365EX-NA-VaultA1-Key001** já existe no compartimento **Contoso-O365EX-NA-VaultA1** , uma nova versão chave será criada. A operação adiciona uma nova versão principal. Essa operação preserva as versões anteriores de chave no histórico de versão da chave, para que os dados criptografados anteriormente com essa chave ainda podem ser descriptografados. Depois de ter concluído sem interrupção qualquer tecla que está associada um DEP, você deve executar um cmdlet adicional para garantir a que chave de cliente começa usando a nova chave.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p174">In this example, since a key named **Contoso-O365EX-NA-VaultA1-Key001** already exists in the **Contoso-O365EX-NA-VaultA1** vault, a new key version will be created. The operation adds a new key version. This operation preserves the previous key versions in the key's version history, so that data previously encrypted with that key can still be decrypted. Once you have completed rolling any key that is associated with a DEP, you must then run an additional cmdlet to ensure Customer Key begins using the new key.</span></span> 
  
#### <a name="enable-exchange-online-and-skype-for-business-to-use-a-new-key-after-you-roll-or-rotate-keys-in-azure-key-vault"></a><span data-ttu-id="e7e12-484">Habilitar o Exchange Online e Skype for Business para usar uma nova chave após reverter ou girar chaves no Azure chave Vault</span><span class="sxs-lookup"><span data-stu-id="e7e12-484">Enable Exchange Online and Skype for Business to use a new key after you roll or rotate keys in Azure Key Vault</span></span>

<span data-ttu-id="e7e12-485">Quando você distribuir um das chaves de Azure chave Vault associadas a um DEP usadas com o Exchange Online e Skype for Business, você deve executar o seguinte comando para atualizar a DEP e ativar o Office 365 começar a usar a nova chave.</span><span class="sxs-lookup"><span data-stu-id="e7e12-485">When you roll either of the Azure Key Vault keys associated with a DEP used with Exchange Online and Skype for Business, you must run the following command to update the DEP and enable Office 365 to start using the new key.</span></span>
  
<span data-ttu-id="e7e12-486">Para instruir o chave do cliente para usar a nova chave para criptografar as caixas de correio no Office 365, execute o cmdlet Set-DataEncryptionPolicy da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e7e12-486">To instruct Customer Key to use the new key to encrypt mailboxes in Office 365 run the Set-DataEncryptionPolicy cmdlet as follows:</span></span>
  
```
Set-DataEncryptionPolicy <policyname> -Refresh 
```

<span data-ttu-id="e7e12-p175">Em 48 horas, as caixas de correio ativas criptografadas usando esta diretiva se tornará associadas com a chave atualizada. Use as etapas em [Determine a DEP atribuída a uma caixa de correio](controlling-your-data-using-customer-key.md#DeterminemailboxDEP) para verificar o valor da propriedade DataEncryptionPolicyID da caixa de correio. O valor dessa propriedade será alterado depois que a chave atualizada tiver sido aplicada.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p175">Within 48 hours, the active mailboxes encrypted using this policy will become associated with the updated key. Use the steps in [Determine the DEP assigned to a mailbox](controlling-your-data-using-customer-key.md#DeterminemailboxDEP) to check the value for the DataEncryptionPolicyID property for the mailbox. The value for this property will change once the updated key has been applied.</span></span> 
  
#### <a name="enable-sharepoint-online-and-onedrive-for-business-to-use-a-new-key-after-you-roll-or-rotate-keys-in-azure-key-vault"></a><span data-ttu-id="e7e12-490">Habilitar o SharePoint Online e OneDrive for Business para usar uma nova chave após reverter ou girar chaves no Azure chave Vault</span><span class="sxs-lookup"><span data-stu-id="e7e12-490">Enable SharePoint Online and OneDrive for Business to use a new key after you roll or rotate keys in Azure Key Vault</span></span>

<span data-ttu-id="e7e12-491">Quando você distribuir um das chaves de Azure chave Vault associadas a um DEP usadas com o SharePoint Online e o OneDrive for Business, você deve executar o cmdlet [Update-SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843948.aspx) para atualizar a DEP e ativar o Office 365 começar a usar a nova chave.</span><span class="sxs-lookup"><span data-stu-id="e7e12-491">When you roll either of the Azure Key Vault keys associated with a DEP used with SharePoint Online and OneDrive for Business, you must run the [Update-SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843948.aspx) cmdlet to update the DEP and enable Office 365 to start using the new key.</span></span> 
  
```
Update-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl> -KeyVaultName <ReplacementKeyVaultName> -KeyName <ReplacementKeyName> -KeyVersion <ReplacementKeyVersion> -KeyType <Primary | Secondary>
```

<span data-ttu-id="e7e12-p176">Isso iniciará a operação roll principais para o SharePoint Online e o OneDrive for Business. Esta ação não é imediata. Para ver o progresso da chave rolo operation, execute o cmdlet Get-SPODataEncryptionPolicy da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e7e12-p176">This will start the key roll operation for SharePoint Online and OneDrive for Business. This action is not immediate. To see the progress of the key roll operation, run the Get-SPODataEncryptionPolicy cmdlet as follows:</span></span>
  
```
Get-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl>
```

### <a name="manage-key-vault-permissions"></a><span data-ttu-id="e7e12-495">Gerenciar permissões de chave vault</span><span class="sxs-lookup"><span data-stu-id="e7e12-495">Manage key vault permissions</span></span>
<span data-ttu-id="e7e12-496"><a name="Managekeyvaultperms"> </a></span><span class="sxs-lookup"><span data-stu-id="e7e12-496"></span></span>

<span data-ttu-id="e7e12-p177">Vários cmdlets estão disponíveis que permitem que você exiba e, se necessário, remover permissões de chave vault. Talvez seja necessário remover permissões, por exemplo, quando um funcionário deixa a equipe.</span><span class="sxs-lookup"><span data-stu-id="e7e12-p177">Several cmdlets are available that enable you to view and, if necessary, remove key vault permissions. You might need to remove permissions, for example, when an employee leaves the team.</span></span>
  
<span data-ttu-id="e7e12-499">Para exibir as permissões de chave vault, execute o cmdlet Get-AzureRmKeyVault:</span><span class="sxs-lookup"><span data-stu-id="e7e12-499">To view key vault permissions, run the Get-AzureRmKeyVault cmdlet:</span></span>
  
```
Get-AzureRmKeyVault -VaultName <vaultname>
```

<span data-ttu-id="e7e12-500">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="e7e12-500">For example:</span></span>
  
```
Get-AzureRmKeyVault -VaultName Contoso-O365EX-NA-VaultA1
```

<span data-ttu-id="e7e12-501">Para remover permissões de administrador, execute o cmdlet Remove-AzureRmKeyVaultAccessPolicy:</span><span class="sxs-lookup"><span data-stu-id="e7e12-501">To remove an administrator's permissions, run the Remove-AzureRmKeyVaultAccessPolicy cmdlet:</span></span>
  
```
Remove-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> 
-UserPrincipalName <UPN of user>
```

<span data-ttu-id="e7e12-502">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="e7e12-502">For example:</span></span>
  
```
Remove-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
-UserPrincipalName alice@contoso.com
```

### <a name="determine-the-dep-assigned-to-a-mailbox"></a><span data-ttu-id="e7e12-503">Determinar a DEP atribuída a uma caixa de correio</span><span class="sxs-lookup"><span data-stu-id="e7e12-503">Determine the DEP assigned to a mailbox</span></span>
<span data-ttu-id="e7e12-504"><a name="DeterminemailboxDEP"> </a></span><span class="sxs-lookup"><span data-stu-id="e7e12-504"></span></span>

<span data-ttu-id="e7e12-p178">Para determinar a DEP atribuída a uma caixa de correio, use o cmdlet Get-MailboxStatistics. O cmdlet retorna um identificador exclusivo (GUID).</span><span class="sxs-lookup"><span data-stu-id="e7e12-p178">To determine the DEP assigned to a mailbox, use the Get-MailboxStatistics cmdlet. The cmdlet returns a unique identifier (GUID).</span></span>
  
```
Get-MailboxStatistics -Identity <GeneralMailboxOrMailUserIdParameter> | fl DataEncryptionPolicyID
```

<span data-ttu-id="e7e12-p179">Onde *GeneralMailboxOrMailUserIdParameter* Especifica uma caixa de correio. Para obter mais informações sobre o cmdlet Get-MailboxStatistics, consulte [Get-MailboxStatistics](https://technet.microsoft.com/library/bb124612%28v=exchg.160%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="e7e12-p179">Where *GeneralMailboxOrMailUserIdParameter* specifies a mailbox. For more information about the Get-MailboxStatistics cmdlet, see [Get-MailboxStatistics](https://technet.microsoft.com/library/bb124612%28v=exchg.160%29.aspx).</span></span>
  
<span data-ttu-id="e7e12-509">Use o GUID para descobrir o nome amigável da DEP ao qual a caixa de correio foi atribuída, executando o seguinte cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7e12-509">Use the GUID to find out the friendly name of the DEP to which the mailbox is assigned by running the following cmdlet.</span></span>
  
```
Get-DataEncryptionPolicy <GUID>
```

<span data-ttu-id="e7e12-510">Onde *GUID* é o GUID retornado pelo cmdlet Get-MailboxStatistics na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="e7e12-510">Where *GUID* is the GUID returned by the Get-MailboxStatistics cmdlet in the previous step.</span></span> 
  


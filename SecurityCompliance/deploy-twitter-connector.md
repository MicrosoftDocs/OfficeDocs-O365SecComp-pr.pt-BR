---
title: Implantar um conector para arquivar dados do Twitter no Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
ROBOTS: NOINDEX, NOFOLLOW
description: Os administradores podem configurar um conector nativo para importar e arquivar dados do Twitter para o Office 365. Depois que esses dados são importados para o Office 365, você pode usar recursos de conformidade, como retenção legal, pesquisa de conteúdo e políticas de retenção para gerenciar a governança dos dados do Twitter da sua organização.
ms.openlocfilehash: 2f9d4842a834858b40e1d788f34f4fb8b2d5b9fd
ms.sourcegitcommit: 5bd7a97aeab1c89e0a3660ba7bdb3200224107a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/16/2019
ms.locfileid: "34103713"
---
# <a name="deploy-a-connector-to-archive-twitter-data-in-office-365"></a><span data-ttu-id="0b412-104">Implantar um conector para arquivar dados do Twitter no Office 365</span><span class="sxs-lookup"><span data-stu-id="0b412-104">Deploy a connector to archive Twitter data in Office 365</span></span>

<span data-ttu-id="0b412-105">Este artigo contém o processo passo a passo para implantar um conector que usa o serviço de importação do Office 365 para importar dados da conta do Twitter da sua organização para o Office 365.</span><span class="sxs-lookup"><span data-stu-id="0b412-105">This article contains the step-by-step process to deploy a connector that uses the Office 365 Import service to import data from your organization's Twitter account to Office 365.</span></span> <span data-ttu-id="0b412-106">Para obter uma visão geral de alto nível desse processo e uma lista de pré-requisitos necessários para implantar um conector do Twitter, consulte [usar um conector de exemplo para arquivar dados do Twitter no Office 365 (versão prévia)](archive-twitter-data-with-sample-connector.md).</span><span class="sxs-lookup"><span data-stu-id="0b412-106">For a high-level overview of this process and a list of prerequisites required to deploy a Twitter connector, see [Use a sample connector to archive Twitter data in Office 365 (Preview)](archive-twitter-data-with-sample-connector.md).</span></span> 

## <a name="step-1-download-the-package"></a><span data-ttu-id="0b412-107">Etapa 1: baixar o pacote</span><span class="sxs-lookup"><span data-stu-id="0b412-107">Step 1: Download the package</span></span>

<span data-ttu-id="0b412-108">Baixe o pacote pré-criado da seção liberar no repositório do GitHub em [https://github.com/microsoft/m365-sample-twitter-connector-csharp-aspnet/releases](https://github.com/microsoft/m365-sample-twitter-connector-csharp-aspnet/releases).</span><span class="sxs-lookup"><span data-stu-id="0b412-108">Download the prebuilt package from the Release section in the GitHub repository at [https://github.com/microsoft/m365-sample-twitter-connector-csharp-aspnet/releases](https://github.com/microsoft/m365-sample-twitter-connector-csharp-aspnet/releases).</span></span> <span data-ttu-id="0b412-109">Na versão mais recente, baixe o arquivo zip chamado **SampleConnector. zip**.</span><span class="sxs-lookup"><span data-stu-id="0b412-109">Under the latest release, download the zip file named **SampleConnector.zip**.</span></span> <span data-ttu-id="0b412-110">Você carregará este arquivo zip no Azure na etapa 4.</span><span class="sxs-lookup"><span data-stu-id="0b412-110">You will upload this zip file to Azure in Step 4.</span></span>

## <a name="step-2-create-an-app-in-azure-active-directory"></a><span data-ttu-id="0b412-111">Etapa 2: criar um aplicativo no Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="0b412-111">Step 2: Create an app in Azure Active Directory</span></span>

1. <span data-ttu-id="0b412-112">Vá para <https://portal.azure.com> e entre usando as credenciais de uma conta de administrador global do Office 365.</span><span class="sxs-lookup"><span data-stu-id="0b412-112">Go to <https://portal.azure.com> and sign in using the credentials of an Office 365 global admin account.</span></span>

   ![](media/TCimage01.png)

2. <span data-ttu-id="0b412-113">No painel de navegação esquerdo, clique em **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="0b412-113">In the left navigation pane, click **Azure Active Directory**.</span></span>

   ![](media/TCimage02.png)

3. <span data-ttu-id="0b412-114">No painel de navegação esquerdo, clique em **registros de aplicativo (visualização)** e clique em **novo registro**.</span><span class="sxs-lookup"><span data-stu-id="0b412-114">In the left navigation pane, click **App registrations (Preview)** and then click **New registration**.</span></span>

   ![](media/TCimage03.png)

4. <span data-ttu-id="0b412-115">Registre o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0b412-115">Register the application.</span></span> <span data-ttu-id="0b412-116">Em **URI de redirecionamento (opcional)**, selecione Web na lista suspensa tipo de aplicativo <https://portal.azure.com> e digite a caixa para o URI.</span><span class="sxs-lookup"><span data-stu-id="0b412-116">Under **Redirect URI (optional)**, select Web in the application type dropdown list and then type <https://portal.azure.com> in the box for the URI.</span></span>

   ![](media/TCimage04.png)

5. <span data-ttu-id="0b412-117">Copie a ID de **aplicativo (cliente)** e a ID de **diretório (locatário)** e salve-as em um arquivo de texto ou outro local seguro.</span><span class="sxs-lookup"><span data-stu-id="0b412-117">Copy the **Application (client) ID** and **Directory (tenant) ID** and save them to a text file or other safe location.</span></span> <span data-ttu-id="0b412-118">Você usará essas IDs nas etapas posteriores.</span><span class="sxs-lookup"><span data-stu-id="0b412-118">You’ll use these IDs in later steps.</span></span>

    ![](media/TCimage05.png)

6. <span data-ttu-id="0b412-119">Vá até **certificados & segredos do novo aplicativo** e, em **segredos do cliente** , clique em **novo segredo do cliente**.</span><span class="sxs-lookup"><span data-stu-id="0b412-119">Go to **Certificates & secrets for the new app** and under **Client secrets** click **New client secret**.</span></span>

   ![](media/TCimage06.png)

7. <span data-ttu-id="0b412-120">Criar um novo segredo.</span><span class="sxs-lookup"><span data-stu-id="0b412-120">Create a new secret.</span></span> <span data-ttu-id="0b412-121">Na caixa Descrição, digite o segredo e, em seguida, escolha um período de expiração.</span><span class="sxs-lookup"><span data-stu-id="0b412-121">In the description box, type the secret and then choose an expiration period.</span></span> 

   ![](media/TCimage08.png)

8. <span data-ttu-id="0b412-122">Copie o valor do segredo e salve-o em um arquivo de texto ou outro local de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0b412-122">Copy the value of the secret and save it to a text file or other storage location.</span></span> <span data-ttu-id="0b412-123">Este é o segredo do aplicativo AAD que você vai usar nas etapas posteriores.</span><span class="sxs-lookup"><span data-stu-id="0b412-123">This is the AAD application secret that you will use in later steps.</span></span>

   ![](media/TCimage09.png)

9. <span data-ttu-id="0b412-124">Vá para **manifesto** e copie o identifieruris agora (que também é chamado de URI do aplicativo AAD) como realçado na captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0b412-124">Go to **Manifest** and copy the identifierUris (which is also called the AAD application Uri) as highlighted in the following screenshot.</span></span> <span data-ttu-id="0b412-125">Copie o URI do aplicativo AAD para um arquivo de texto ou outro local de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0b412-125">Copy the AAD application Uri to a text file or other storage location.</span></span> <span data-ttu-id="0b412-126">Você o usará na etapa 6.</span><span class="sxs-lookup"><span data-stu-id="0b412-126">You’ll use it in Step 6.</span></span>

    ![](media/TCimage10.png)

## <a name="step-3-create-an-azure-storage-account"></a><span data-ttu-id="0b412-127">Etapa 3: criar uma conta de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="0b412-127">Step 3: Create an Azure storage account</span></span>

1.  <span data-ttu-id="0b412-128">Vá para a home page do Azure para sua organização.</span><span class="sxs-lookup"><span data-stu-id="0b412-128">Go to the Azure home page for your organization.</span></span>

    ![](media/TCimage11.png)

2. <span data-ttu-id="0b412-129">Clique em **criar um recurso** e digite a **conta de armazenamento** na caixa de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="0b412-129">Click **Create a resource** and they type **storage account** in the search box.</span></span>

   ![](media/TCimage12.png)

3. <span data-ttu-id="0b412-130">Clique em **armazenamento**e, em seguida, clique em **conta de armazenamento**.</span><span class="sxs-lookup"><span data-stu-id="0b412-130">Click **Storage**, and then click **Storage account**.</span></span>

   ![](media/TCimage13.png)

4. <span data-ttu-id="0b412-131">Na página **criar conta de armazenamento** , na caixa assinatura, selecione **pagar como você** ou **avaliação gratuita** , dependendo do tipo de assinatura do Azure que você tem.</span><span class="sxs-lookup"><span data-stu-id="0b412-131">On the **Create storage account** page, in the Subscription box, select **Pay-As-You-Go** or **Free Trial** depending on which type of Azure subscription you have.</span></span> 

   ![](media/TCimage14.png)

5. <span data-ttu-id="0b412-132">Selecione ou crie um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0b412-132">Select or create a resource group.</span></span>

   ![](media/TCimage15.png)

6. <span data-ttu-id="0b412-133">Digite um nome para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0b412-133">Type a name for the storage account.</span></span>

   ![](media/TCimage16.png)

7. <span data-ttu-id="0b412-134">Revise e clique em **criar** para criar a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0b412-134">Review and then click **Create** to create the storage account.</span></span>

   ![](media/TCimage17.png)

8. <span data-ttu-id="0b412-135">Após alguns momentos, clique em **Atualizar** e clique em **ir para recurso** para navegar até a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0b412-135">After a few moments, click **Refresh** and then click **Go to resource** to navigate to the storage account.</span></span>

   ![](media/TCimage18.png)

9. <span data-ttu-id="0b412-136">Clique em **teclas de acesso** no painel de navegação esquerdo.</span><span class="sxs-lookup"><span data-stu-id="0b412-136">Click **Access keys** in the left navigation pane.</span></span>

   ![](media/TCimage19.png)

10. <span data-ttu-id="0b412-137">Copie uma **cadeia de caracteres de conexão** e salve-a em um arquivo de texto ou outro local de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0b412-137">Copy a **Connection string** and save it to a text file or other storage location.</span></span> <span data-ttu-id="0b412-138">Você o usará ao criar um recurso do aplicativo Web na etapa 4.</span><span class="sxs-lookup"><span data-stu-id="0b412-138">You’ll use this when creating a web app resource in Step 4.</span></span>

    ![](media/TCimage20.png)

## <a name="step-4-create-a-new-web-app-resource-in-azure"></a><span data-ttu-id="0b412-139">Etapa 4: criar um novo recurso do aplicativo Web no Azure</span><span class="sxs-lookup"><span data-stu-id="0b412-139">Step 4: Create a new web app resource in Azure</span></span>

1. <span data-ttu-id="0b412-140">Na **Home** Page do portal do Azure, clique em **criar um recurso \> para \> todos os aplicativos Web**.</span><span class="sxs-lookup"><span data-stu-id="0b412-140">On the **Home** page in the Azure portal, click **Create a resource \> Everything \> Web app**.</span></span> <span data-ttu-id="0b412-141">Na página **Web App** , clique em **criar**.</span><span class="sxs-lookup"><span data-stu-id="0b412-141">On the **Web app** page, click **Create**.</span></span>

   ![](media/TCimage21.png)

2. <span data-ttu-id="0b412-142">Preencha os detalhes (conforme mostrado abaixo) e, em seguida, crie o aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="0b412-142">Fill in the details (as shown below) and then create the Web app.</span></span> <span data-ttu-id="0b412-143">Observe que o nome inserido na caixa nome do **aplicativo** será usado para criar a URL do serviço de aplicativo do Azure; por exemplo twitterconnector.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="0b412-143">Note that the name that you enter in the **App name** box will be used to create the Azure app service URL; for example twitterconnector.azurewebsites.net.</span></span>

   ![](media/TCimage22.png)

3. <span data-ttu-id="0b412-144">Vá para o recurso aplicativo Web recém-criado, clique em **configurações do aplicativo** no painel de navegação esquerdo.</span><span class="sxs-lookup"><span data-stu-id="0b412-144">Go to the newly created web app resource, click **Application Settings** in the left navigation pane.</span></span> <span data-ttu-id="0b412-145">Em **configurações do aplicativo**, clique em **Adicionar nova configuração** e adicione as três configurações a seguir.</span><span class="sxs-lookup"><span data-stu-id="0b412-145">Under **Application settings**, click **Add new setting** and add the following three settings.</span></span> <span data-ttu-id="0b412-146">Use os valores (que você copiou para o arquivo de texto das etapas anteriores):</span><span class="sxs-lookup"><span data-stu-id="0b412-146">Use the values (that you copied to the text file from the previous steps):</span></span> 

    - <span data-ttu-id="0b412-147">**APISecretKey** – você pode digitar qualquer valor como o segredo.</span><span class="sxs-lookup"><span data-stu-id="0b412-147">**APISecretKey** – You can type any value as the secret.</span></span> <span data-ttu-id="0b412-148">Isso será usado para acessar o aplicativo Web do conector na etapa 7.</span><span class="sxs-lookup"><span data-stu-id="0b412-148">This will be used to access the connector web app in Step 7.</span></span>

    - <span data-ttu-id="0b412-149">**StorageAccountConnectionString** – o URI da cadeia de caracteres de conexão que você copiou após a criação da conta de armazenamento do Azure na etapa 3.</span><span class="sxs-lookup"><span data-stu-id="0b412-149">**StorageAccountConnectionString** – The connection string Uri that you copied after creating the Azure storage account in Step 3.</span></span>

    - <span data-ttu-id="0b412-150">**tenantid** – a ID do locatário de sua organização do Office 365 que você copiou depois de criar o aplicativo do conector do Twitter no Azure Active Directory na etapa 2.</span><span class="sxs-lookup"><span data-stu-id="0b412-150">**tenantId** – The tenant ID of your Office 365 organization that you copied after creating the Twitter connector app in Azure Active Directory in Step 2.</span></span>

    ![](media/TCimage23.png)

4. <span data-ttu-id="0b412-151">Em **configurações gerais**, clique **em** ao lado de **sempre ligado**.</span><span class="sxs-lookup"><span data-stu-id="0b412-151">Under **General settings**, click **On** next to the **Always On**.</span></span> <span data-ttu-id="0b412-152">Clique em **salvar** na parte superior da página para salvar as configurações do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0b412-152">Click **Save** at the top of the page to save the application settings.</span></span>

   ![](media/TCimage24.png)

5. <span data-ttu-id="0b412-153">A etapa final é carregar o código-fonte do aplicativo conector para o Azure que você baixou na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="0b412-153">The final step is to upload the connector app source code to Azure that you downloaded in Step 1.</span></span> <span data-ttu-id="0b412-154">Em um navegador da Web, vá para<AzureAppResourceName>https://. SCM.azurewebsites.net/ZipDeployUi.</span><span class="sxs-lookup"><span data-stu-id="0b412-154">In a web browser, go to https://<AzureAppResourceName>.scm.azurewebsites.net/ZipDeployUi.</span></span> <span data-ttu-id="0b412-155">Por exemplo, se o nome do seu recurso de aplicativo do Azure (que você nomeou na etapa 2 nesta seção) for **twitterconnector**, vá para https://twitterconnector.scm.azurewebsites.net/ZipDeployUi.</span><span class="sxs-lookup"><span data-stu-id="0b412-155">For example, if the name of your Azure app resource (which you named in step 2 in this section) is **twitterconnector**, then you would go to https://twitterconnector.scm.azurewebsites.net/ZipDeployUi.</span></span>

6. <span data-ttu-id="0b412-156">Arraste e solte o SampleConnector. zip (que você baixou na etapa 1) para esta página.</span><span class="sxs-lookup"><span data-stu-id="0b412-156">Drag and drop the SampleConnector.zip (that you downloaded in Step 1) to this page.</span></span> <span data-ttu-id="0b412-157">Após o carregamento dos arquivos e a implantação ter êxito, a página será semelhante à captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0b412-157">After the files are uploaded and the deployment is successful, the page will look similar to the following screenshot.</span></span>

   ![](media/TCimage25.png)

## <a name="step-5-create-the-twitter-app"></a><span data-ttu-id="0b412-158">Etapa 5: criar o aplicativo Twitter</span><span class="sxs-lookup"><span data-stu-id="0b412-158">Step 5: Create the Twitter app</span></span>

1. <span data-ttu-id="0b412-159">Vá para https://developer.twitter.com, faça logon usando as credenciais da conta de desenvolvedor da sua organização e clique em **aplicativos**.</span><span class="sxs-lookup"><span data-stu-id="0b412-159">Go to https://developer.twitter.com, log in using the credentials for the developer account for your organization, and then click **Apps**.</span></span>

   ![TCimage25-5. png](media/TCimage25-5.png)
2. <span data-ttu-id="0b412-161">Clique em **criar um aplicativo**.</span><span class="sxs-lookup"><span data-stu-id="0b412-161">Click **Create an app**.</span></span>
   
   ![](media/TCimage26.png)

3. <span data-ttu-id="0b412-162">Em **detalhes do aplicativo**, adicione informações sobre o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0b412-162">Under **App details**, add information about the application.</span></span>

   ![](media/TCimage27.png)

4. <span data-ttu-id="0b412-163">No painel de desenvolvedor do Twitter, selecione o aplicativo que você acabou de criar e copie a ID do aplicativo que é exibida e salve-a em um arquivo de texto ou outro local de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0b412-163">On the Twitter developer dashboard, select the app that you just created and copy the App ID that's displayed  and save it to a text file or other storage location.</span></span> <span data-ttu-id="0b412-164">Em seguida, clique em **detalhes**.</span><span class="sxs-lookup"><span data-stu-id="0b412-164">Then click **Details**.</span></span>
   
   ![](media/TCimage28.png)

5. <span data-ttu-id="0b412-165">Na guia **chaves e tokens** , em **chaves da API do consumidor** , copie a chave secreta da API e salve-a em um arquivo de texto ou outro local de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0b412-165">On the **Keys and tokens** tab, under **Consumer API keys** copy the API secret key and save it to a text file or other storage location.</span></span> <span data-ttu-id="0b412-166">Em seguida, clique em **criar** para gerar um token de acesso e um segredo de token de acesso e copie-os para um arquivo de texto ou outro local de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0b412-166">Then click **Create** to generate an access token and an access token secret, and copy these to a text file or other storage location.</span></span>
   
   ![](media/TCimage29.png)

   <span data-ttu-id="0b412-167">Em seguida, clique em **criar** para gerar um token de acesso e um segredo de token de acesso e copie-os para um arquivo de texto ou outro local de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0b412-167">Then click **Create** to generate an access token and an access token secret, and copy these to a text file or other storage location.</span></span>

6. <span data-ttu-id="0b412-168">Clique na guia **permissões** e configure as permissões conforme mostrado na captura de tela a seguir:</span><span class="sxs-lookup"><span data-stu-id="0b412-168">Click the **Permissions** tab and configure the permissions as shown in the following screenshot:</span></span>

   ![](media/TCimage30.png)

7. <span data-ttu-id="0b412-169">Após salvar as configurações de permissão, clique na guia **detalhes do aplicativo** e, em seguida, clique em **Editar > editar detalhes**.</span><span class="sxs-lookup"><span data-stu-id="0b412-169">After you save the permission settings, click the **App details** tab, and then click **Edit > Edit details**.</span></span>

   ![](media/TCimage31.png)

8. <span data-ttu-id="0b412-170">Execute as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="0b412-170">Do the following tasks:</span></span>

   - <span data-ttu-id="0b412-171">Marque a caixa de seleção para permitir que o aplicativo conector entre no Twitter.</span><span class="sxs-lookup"><span data-stu-id="0b412-171">Select the checkbox to allow the connector app to sign in to Twitter.</span></span>
   
   - <span data-ttu-id="0b412-172">Adicione o URI de redirecionamento OAuth usando o seguinte formato: \*\* \<connectorserviceuri>/views/TwitterOAuth\*\*, onde o valor de *connectorserviceuri* é a URL do serviço de aplicativo do Azure para sua organização; por exemplo https://twitterconnector.azurewebsites.net/Views/TwitterOAuth.</span><span class="sxs-lookup"><span data-stu-id="0b412-172">Add the OAuth redirect Uri using the following format: **\<connectorserviceuri>/Views/TwitterOAuth**, where the value of *connectorserviceuri* is the Azure app service URL for your organization; for example https://twitterconnector.azurewebsites.net/Views/TwitterOAuth.</span></span>

   ![](media/TCimage32.png)

<span data-ttu-id="0b412-173">O aplicativo de desenvolvedor do Twitter agora está pronto para uso.</span><span class="sxs-lookup"><span data-stu-id="0b412-173">The Twitter developer app is now ready to use.</span></span>

## <a name="step-6-configure-the-connector-web-app"></a><span data-ttu-id="0b412-174">Etapa 6: configurar o aplicativo Web do conector</span><span class="sxs-lookup"><span data-stu-id="0b412-174">Step 6: Configure the connector web app</span></span> 

1. <span data-ttu-id="0b412-175">Vá para https://\<AzureAppResourceName>. azurewebsites. net (onde **AzureAppResourceName** é o nome do seu recurso do aplicativo do Azure que você nomeou na etapa 4) por exemplo, se o nome for **twitterconnector**, vá para https://twitterconnector.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="0b412-175">Go to https://\<AzureAppResourceName>.azurewebsites.net (where **AzureAppResourceName** is the name of your Azure app resource that you named in Step 4) For example, if the name is **twitterconnector**, go to https://twitterconnector.azurewebsites.net.</span></span> <span data-ttu-id="0b412-176">A home page do aplicativo se parecerá com a captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0b412-176">The home page of the app will look like the following screenshot.</span></span>

   ![](media/FBCimage41.png)

2. <span data-ttu-id="0b412-177">Clique em **Configurar** para exibir uma página de entrada.</span><span class="sxs-lookup"><span data-stu-id="0b412-177">Click **Configure** to display a sign in page.</span></span>

   ![](media/FBCimage42.png)

3. <span data-ttu-id="0b412-178">Na caixa ID do locatário, digite ou cole sua ID de locatário (que você obteve na etapa 2).</span><span class="sxs-lookup"><span data-stu-id="0b412-178">In the Tenant Id box, type or paste your tenant Id (that you obtained in Step 2).</span></span> <span data-ttu-id="0b412-179">Na caixa senha, digite ou cole o APISecretKey (que você obteve na etapa 2) e clique em **definir definições de configuração** para exibir a página **detalhes da configuração** .</span><span class="sxs-lookup"><span data-stu-id="0b412-179">In the password box, type or paste the APISecretKey (that you obtained in Step 2), and then click **Set Configuration Settings** to display the **Configuration Details** page.</span></span>

   ![](media/TCimage35.png)

4. <span data-ttu-id="0b412-180">Em **detalhes da configuração**, insira as seguintes definições de configuração</span><span class="sxs-lookup"><span data-stu-id="0b412-180">Under **Configuration Details**, enter the following configuration settings</span></span> 

   - <span data-ttu-id="0b412-181">**ID do aplicativo Twitter** -a ID do aplicativo do aplicativo Twitter que você criou na etapa 5.</span><span class="sxs-lookup"><span data-stu-id="0b412-181">**Twitter application ID** - The app ID for the Twitter application that you created in Step 5.</span></span>
   - <span data-ttu-id="0b412-182">**Segredo do aplicativo Twitter** -a chave secreta da API para o aplicativo Twitter que você criou na etapa 5.</span><span class="sxs-lookup"><span data-stu-id="0b412-182">**Twitter application secret** - The API secret key for the Twitter application that you created in Step 5.</span></span>
   - <span data-ttu-id="0b412-183">**Token de cliente do Twitter** -o token de acesso que você criou na etapa 5.</span><span class="sxs-lookup"><span data-stu-id="0b412-183">**Twitter client token** - The access token that you created in Step 5.</span></span>
   - <span data-ttu-id="0b412-184">**Segredo do token de cliente do Twitter** -o segredo do token de acesso que você criou na etapa 5.</span><span class="sxs-lookup"><span data-stu-id="0b412-184">**Twitter client token secret** - The access token secret that you created in Step 5.</span></span>
   - <span data-ttu-id="0b412-185">**ID do aplicativo AAD** -a ID do aplicativo para o aplicativo do Azure Active Directory que você criou na etapa 2</span><span class="sxs-lookup"><span data-stu-id="0b412-185">**AAD application ID** - The application ID for the Azure Active Directory app that you created in Step 2</span></span>
   - <span data-ttu-id="0b412-186">**Sigilo de aplicativo do AAD** -o valor para o segredo APISecretKey que você criou na etapa 4.</span><span class="sxs-lookup"><span data-stu-id="0b412-186">**AAD application secret** - The value for the APISecretKey secret that you created in Step 4.</span></span>
   - <span data-ttu-id="0b412-187">**URI do aplicativo AAD** -o URI do aplicativo AAD obtido na etapa 2; por exemplo, https://microsoft.onmicrosoft.com/2688yu6n-12q3-23we-e3ee-121111123213.</span><span class="sxs-lookup"><span data-stu-id="0b412-187">**AAD application Uri** - The AAD application Uri obtained in Step 2; for example, https://microsoft.onmicrosoft.com/2688yu6n-12q3-23we-e3ee-121111123213.</span></span>
   - <span data-ttu-id="0b412-188">**Chave** de instrumentação do App insights-deixe esta caixa em branco.</span><span class="sxs-lookup"><span data-stu-id="0b412-188">**App insights instrumentation key** - Leave this box blank.</span></span>

5. <span data-ttu-id="0b412-189">Clique em **salvar** para salvar as configurações do conector.</span><span class="sxs-lookup"><span data-stu-id="0b412-189">Click **Save** to save the connector settings.</span></span>

## <a name="step-7-set-up-a-custom-connector-in-the-security-and-compliance-center"></a><span data-ttu-id="0b412-190">Etapa 7: configurar um conector personalizado no centro de conformidade e segurança</span><span class="sxs-lookup"><span data-stu-id="0b412-190">Step 7: Set up a custom connector in the security and compliance center</span></span>

1.  <span data-ttu-id="0b412-191">Vá para <https://protection.office.com> e, em seguida, clique em **arquivar importação \> \> de governança de dados dados de terceiros**.</span><span class="sxs-lookup"><span data-stu-id="0b412-191">Go to <https://protection.office.com> and then click **Data governance \> Import \> Archive third-party data**.</span></span>

    ![](media/TCimage36.png)

2. <span data-ttu-id="0b412-192">Clique em **Adicionar um conector** e, em seguida, clique em **Twitter**.</span><span class="sxs-lookup"><span data-stu-id="0b412-192">Click **Add a connector** and then click **Twitter**.</span></span>

   ![](media/TCimage37.png)

3. <span data-ttu-id="0b412-193">Na página **Adicionar aplicativo do conector** , digite as informações a seguir e clique em **validar conector**.</span><span class="sxs-lookup"><span data-stu-id="0b412-193">On the **Add Connector App** page, enter the following information and then click **Validate connector**.</span></span>

    - <span data-ttu-id="0b412-194">Na primeira caixa, digite um nome para o conector, como **Twitter**.</span><span class="sxs-lookup"><span data-stu-id="0b412-194">In the first box, type a name for the connector, such as **Twitter**.</span></span>
    - <span data-ttu-id="0b412-195">Na segunda caixa, digite ou cole o valor do APISecretKey que você adicionou na etapa 4.</span><span class="sxs-lookup"><span data-stu-id="0b412-195">In the second box, type or paste the value of the APISecretKey that you added in Step 4.</span></span>
    - <span data-ttu-id="0b412-196">Na terceira caixa, digite ou cole a URL do serviço de aplicativo do Azure; por exemplo **https://twitterconnector.azurewebsites.net**.</span><span class="sxs-lookup"><span data-stu-id="0b412-196">In the third box, type or paste the Azure app service URL; for example **https://twitterconnector.azurewebsites.net**.</span></span>

   <span data-ttu-id="0b412-197">Depois que o conector for validado com êxito, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="0b412-197">After the connector is successfully validated, click **Next**.</span></span>

   ![](media/TCimage38.png)

4. <span data-ttu-id="0b412-198">Clique em **login com o aplicativo do conector**.</span><span class="sxs-lookup"><span data-stu-id="0b412-198">Click **Login with Connector App**.</span></span>

   ![](media/TCimage39.png)

5. <span data-ttu-id="0b412-199">Digite ou cole o APISecretKey novamente e, em seguida, clique em **login to Connector Service**.</span><span class="sxs-lookup"><span data-stu-id="0b412-199">Type or paste the APISecretKey again and then click  **Login to Connector Service**.</span></span>

   ![](media/TCimage40.png)


6. <span data-ttu-id="0b412-200">Clique em **continuar com o Twitter**.</span><span class="sxs-lookup"><span data-stu-id="0b412-200">Click **Continue with Twitter**.</span></span>

7. <span data-ttu-id="0b412-201">Na página de entrada do Twitter, entre usando as credenciais da conta da conta do Twitter da sua organização.</span><span class="sxs-lookup"><span data-stu-id="0b412-201">On the Twitter sign in page, sign in using the credentials for the account for your organization’s Twitter account.</span></span>

   ![](media/TCimage42.png)

   <span data-ttu-id="0b412-202">Depois que você entrar, a página do Twitter exibirá a seguinte mensagem, "trabalho do conector do Twitter configurado com êxito".</span><span class="sxs-lookup"><span data-stu-id="0b412-202">After you sign in, the Twitter page will display the following message, "Twitter Connector Job Successfully set up."</span></span>

8. <span data-ttu-id="0b412-203">Clique em **concluir** para concluir a configuração do conector do Twitter.</span><span class="sxs-lookup"><span data-stu-id="0b412-203">Click **Finish** to complete setting up the Twitter connector.</span></span>

9. <span data-ttu-id="0b412-204">Na página **definir filtros** , você pode aplicar um filtro para importar (e arquivar) itens que são uma determinada idade.</span><span class="sxs-lookup"><span data-stu-id="0b412-204">On the **Set Filters** page, you can apply a filter to import (and archive) items that are a certain age.</span></span> <span data-ttu-id="0b412-205">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="0b412-205">Click **Next**.</span></span>

   ![](media/TCimage44.png)

10. <span data-ttu-id="0b412-206">Na página **definir conta de armazenamento** , selecione a caixa de correio do Office 365 para a qual os itens do Twitter serão importados.</span><span class="sxs-lookup"><span data-stu-id="0b412-206">On the **Set Storage Account** page, select the Office 365 mailbox that the Twitter items will be imported to.</span></span>

    ![](media/TCimage45.png)

11. <span data-ttu-id="0b412-207">Revise suas configurações e clique em **concluir** para concluir a instalação do conector no centro de conformidade do _AMP_ de segurança.</span><span class="sxs-lookup"><span data-stu-id="0b412-207">Review your settings and then click **Finish** to complete the connector setup in the Security & Compliance Center.</span></span>

    ![](media/TCimage46.png)

    ![](media/TCimage47.png)

12. <span data-ttu-id="0b412-208">Vá para a página **arquivar dados** de terceiros para ver o andamento do processo de importação.</span><span class="sxs-lookup"><span data-stu-id="0b412-208">Go to the **Archive third-party data** page to see the progress of the import process.</span></span>

    ![](media/TCimage48.png)

---
title: Configurar um conector para arquivar dados do LinkedIn no Office 365 (versão prévia)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
description: Os administradores podem configurar um conector nativo para importar dados de uma página da empresa do LinkedIn para o Office 365. Isso permite que você arquive dados de fontes de dados de terceiros no Office 365 para que possa usar recursos de conformidade, como retenção legal, pesquisa de conteúdo e políticas de retenção para gerenciar a conformidade dos dados de terceiros da sua organização.
ms.openlocfilehash: 2b89f990f18ae13ad15015f240ea4c4b0ec434b0
ms.sourcegitcommit: f2798d46acfbd56314e809cd3fe0350be807e420
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2019
ms.locfileid: "35017942"
---
# <a name="set-up-a-connector-to-archive-linkedin-data-in-office-365-preview"></a><span data-ttu-id="57352-104">Configurar um conector para arquivar dados do LinkedIn no Office 365 (versão prévia)</span><span class="sxs-lookup"><span data-stu-id="57352-104">Set up a connector to archive LinkedIn data in Office 365 (Preview)</span></span>

<span data-ttu-id="57352-105">O recurso conector para arquivar dados das páginas da empresa do LinkedIn no Office 365 está em visualização.</span><span class="sxs-lookup"><span data-stu-id="57352-105">The connector feature to archive data from LinkedIn Company pages in Office 365 is in Preview.</span></span>

<span data-ttu-id="57352-106">Use um conector nativo no centro de conformidade & segurança no Office 365 para importar e arquivar dados das páginas da empresa do LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="57352-106">Use a native connector in the Security & Compliance Center in Office 365 to import and archive data from LinkedIn Company pages.</span></span> <span data-ttu-id="57352-107">Depois de configurar e configurar um conector, ele se conecta à conta da página específica da empresa do LinkedIn uma vez a cada 24 horas.</span><span class="sxs-lookup"><span data-stu-id="57352-107">After you set up and configure a connector, it connects to the account for the specific LinkedIn Company page once every 24 hours.</span></span> <span data-ttu-id="57352-108">O conector converte as mensagens postadas na página da empresa em uma mensagem de email e, em seguida, importa esses itens para uma caixa de correio no Office 365.</span><span class="sxs-lookup"><span data-stu-id="57352-108">The connector converts the messages posted to the Company page to an email message, and then imports those items to a mailbox in Office 365.</span></span>

<span data-ttu-id="57352-109">Depois que os dados da página da empresa do LinkedIn são armazenados em uma caixa de correio, você pode aplicar recursos de conformidade do Office 365, como retenção de litígio, pesquisa de conteúdo, arquivamento in-loco, auditoria e políticas de retenção do Office 365 a dados do LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="57352-109">After the LinkedIn Company page data is stored in a mailbox, you can apply Office 365 compliance features such as Litigation Hold, Content Search, In-Place Archiving, Auditing, and Office 365 retention policies to LinkedIn data.</span></span> <span data-ttu-id="57352-110">Por exemplo, você pode pesquisar esses itens usando a pesquisa de conteúdo ou associar a caixa de correio de armazenamento a um funcionário em uma caixa de descoberta eletrônica avançada.</span><span class="sxs-lookup"><span data-stu-id="57352-110">For example, you can search for these items using Content Search or associate the storage mailbox with a custodian in an Advanced eDiscovery case.</span></span> <span data-ttu-id="57352-111">A criação de um conector para importar e arquivar dados do LinkedIn no Office 365 pode ajudar sua organização a se manter em conformidade com as políticas governamentais e regulamentares.</span><span class="sxs-lookup"><span data-stu-id="57352-111">Creating a connector to import and archive LinkedIn data in Office 365 can help your organization stay compliant with government and regulatory policies.</span></span>

## <a name="before-you--begin"></a><span data-ttu-id="57352-112">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="57352-112">Before you  begin</span></span>

- <span data-ttu-id="57352-113">Você deve ter as credenciais de entrada (endereço de email ou número de telefone e senha) de uma conta de usuário do LinkedIn que seja um administrador para a página da empresa do LinkedIn que você deseja arquivar.</span><span class="sxs-lookup"><span data-stu-id="57352-113">You must have the sign-in credentials (email address or phone number and password) of a LinkedIn user account that is an admin for the LinkedIn Company Page that you want to archive.</span></span> <span data-ttu-id="57352-114">Use essas credenciais para entrar no LinkedIn ao configurar o conector.</span><span class="sxs-lookup"><span data-stu-id="57352-114">You use these credentials to sign in to LinkedIn when setting up the connector.</span></span>

- <span data-ttu-id="57352-115">O usuário que cria um conector de página da empresa do LinkedIn deve receber a função de exportação de importação de caixa de correio no Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="57352-115">The user who creates an LinkedIn Company Page connector must be assigned the Mailbox Import Export role in Exchange Online.</span></span> <span data-ttu-id="57352-116">Isso é necessário para acessar a página **arquivar dados** de terceiros no centro de conformidade de & de segurança.</span><span class="sxs-lookup"><span data-stu-id="57352-116">This is required to access the **Archive third-party data** page in the Security & Compliance Center.</span></span> <span data-ttu-id="57352-117">Por padrão, essa função não é atribuída a nenhum grupo de função no Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="57352-117">By default, this role isn't assigned to any role group in Exchange Online.</span></span> <span data-ttu-id="57352-118">Você pode adicionar a função de exportação de importação de caixa de correio ao grupo de funções Gerenciamento da organização no Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="57352-118">You can add the Mailbox Import Export role to the Organization Management role group in Exchange Online.</span></span> <span data-ttu-id="57352-119">Ou você pode criar um grupo de função, atribua a função de exportação de importação de caixa de correio e, em seguida, adicione os usuários apropriados como membros.</span><span class="sxs-lookup"><span data-stu-id="57352-119">Or you can create a role group, assign the Mailbox Import Export role, and then add the appropriate users as members.</span></span> <span data-ttu-id="57352-120">Para obter mais informações, consulte as seções [criar grupos de função](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#create-role-groups) ou [modificar grupos de função](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#modify-role-groups) no artigo "gerenciar grupos de função no Exchange Online".</span><span class="sxs-lookup"><span data-stu-id="57352-120">For more information, see the  [Create role groups](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#create-role-groups) or [Modify role groups](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#modify-role-groups) sections in the article "Manage role groups in Exchange Online".</span></span>

## <a name="create-a-linkedin-connector"></a><span data-ttu-id="57352-121">Criar um conector do LinkedIn</span><span class="sxs-lookup"><span data-stu-id="57352-121">Create a LinkedIn connector</span></span>

1. <span data-ttu-id="57352-122">Vá para <https://protection.office.com> e clique em **importação de \> governança de dados** e clique em **arquivar dados de terceiros**.</span><span class="sxs-lookup"><span data-stu-id="57352-122">Go to <https://protection.office.com> and then click **Data governance \> Import** and then click **Archive third-party data**.</span></span>

2. <span data-ttu-id="57352-123">Na página **arquivar dados de terceiros** , clique em **Adicionar um conector**e, em seguida, clique em **LinkedIn**.</span><span class="sxs-lookup"><span data-stu-id="57352-123">On the **Archive third-party data** page, click **Add a connector**, and then click **LinkedIn**.</span></span>

3. <span data-ttu-id="57352-124">Na página **termos de serviço** , clique em **aceitar**.</span><span class="sxs-lookup"><span data-stu-id="57352-124">On the **Terms of service** page, click **Accept**.</span></span>

4. <span data-ttu-id="57352-125">Na página **entrar com o LinkedIn** , clique em **entrar com LinkedIn**.</span><span class="sxs-lookup"><span data-stu-id="57352-125">On the **Sign in with LinkedIn** page, click **Sign in with LinkedIn**.</span></span>

   <span data-ttu-id="57352-126">A página de entrada do LinkedIn é exibida.</span><span class="sxs-lookup"><span data-stu-id="57352-126">The LinkedIn sign in page is displayed.</span></span>

   ![Página de entrada do LinkedIn](media/LinkedInSigninPage.png)

5. <span data-ttu-id="57352-128">Na página de entrada do LinkedIn, insira o endereço de email (ou número de telefone) e a senha da conta do LinkedIn associada à página da empresa que você deseja arquivar e clique em **entrar**.</span><span class="sxs-lookup"><span data-stu-id="57352-128">On the LinkedIn sign in page, enter the email address (or phone number) and password for the LinkedIn account that associated with the company page that you want to archive, and then click **Sign in**.</span></span>

   <span data-ttu-id="57352-129">Uma página de assistente é exibida com uma lista de todas as páginas da empresa do LinkedIn associadas à conta na qual você entrou no.</span><span class="sxs-lookup"><span data-stu-id="57352-129">A wizard page is displayed with a list of all LinkedIn Company Pages associated with the account that you signed in to.</span></span> <span data-ttu-id="57352-130">Um conector só pode ser configurado para uma página da empresa.</span><span class="sxs-lookup"><span data-stu-id="57352-130">A connector can only be configured for one company page.</span></span> <span data-ttu-id="57352-131">Se sua organização tiver várias páginas da empresa do LinkedIn, você precisará criar um conector para cada uma delas.</span><span class="sxs-lookup"><span data-stu-id="57352-131">If your organization has multiple LinkedIn Company Pages, you have to create a connector for each one.</span></span>

   ![Uma página com uma lista de páginas da empresa do LinkedIn é exibida](media/LinkedInSelectCompanyPage.png)


6. <span data-ttu-id="57352-133">Selecione a página da empresa da qual você deseja arquivar itens e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="57352-133">Select the company page that you want to archive items from, and then click **Next**.</span></span>

7. <span data-ttu-id="57352-134">Na página **definir filtros** , você pode aplicar um filtro para importar inicialmente os itens que tenham uma determinada idade.</span><span class="sxs-lookup"><span data-stu-id="57352-134">On the **Set filters** page, you can apply a filter to initially import items that are a certain age.</span></span> <span data-ttu-id="57352-135">Selecione uma idade e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="57352-135">Select an age, and then click **Next**.</span></span>

8. <span data-ttu-id="57352-136">Na página **definir conta de armazenamento** , digite o endereço de email de uma caixa de correio do Office 365 à qual os itens do LinkedIn serão importados e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="57352-136">On the **Set storage account** page, type the email address of an Office 365 mailbox that the LinkedIn items will be imported to, and then click **Next**.</span></span> <span data-ttu-id="57352-137">Os itens são importados para a pasta caixa de entrada nesta caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="57352-137">Items are imported to the Inbox folder in this mailbox.</span></span>

9. <span data-ttu-id="57352-138">Revise as configurações do conector e clique em **salvar** para concluir a configuração do conector.</span><span class="sxs-lookup"><span data-stu-id="57352-138">Review the connector settings and then click **Save** to complete the connector setup.</span></span>

<span data-ttu-id="57352-139">Depois de criar o conector, você pode voltar para a página **arquivar dados** de terceiros (clique em **Atualizar** se necessário para atualizar a lista de conectores) um modo de exibição do novo conector.</span><span class="sxs-lookup"><span data-stu-id="57352-139">After you create the connector, you can go back to the **Archive third-party data** page (click **Refresh** if necessary to update the list of connectors) a view the new connector.</span></span> <span data-ttu-id="57352-140">O valor na coluna **status** está **aguardando para iniciar**.</span><span class="sxs-lookup"><span data-stu-id="57352-140">The value in the **Status** column is **Waiting to start**.</span></span> <span data-ttu-id="57352-141">É necessário ter até 24 horas para que o processo inicial de importação seja iniciado.</span><span class="sxs-lookup"><span data-stu-id="57352-141">It takes up to 24 hours for the initial import process to be started.</span></span> <span data-ttu-id="57352-142">Após a primeira vez que o conector é executado e importa os itens do LinkedIn, o conector é executado uma vez a cada 24 horas e importa os novos itens que são criados na página da empresa do LinkedIn nas últimas 24 horas.</span><span class="sxs-lookup"><span data-stu-id="57352-142">After the first time the connector runs and imports the LinkedIn items, the connector will run once every 24 hours and import any new items that are created on the LinkedIn Company Page in the previous 24 hours.</span></span>

<span data-ttu-id="57352-143">Para exibir mais detalhes, clique no conector na lista na página de **dados** de terceiros de arquivamento para exibir a página de menu.</span><span class="sxs-lookup"><span data-stu-id="57352-143">To view more details, click the connector in the list on the **Archive third-party data** page to display the flyout page.</span></span> <span data-ttu-id="57352-144">Em **status**, o intervalo de datas exibido indica o filtro de idade que foi selecionado quando o conector foi criado.</span><span class="sxs-lookup"><span data-stu-id="57352-144">Under **Status**, the date range that's displayed indicates the age filter that was selected when the connector was created.</span></span> 

## <a name="more-information"></a><span data-ttu-id="57352-145">Mais informações</span><span class="sxs-lookup"><span data-stu-id="57352-145">More information</span></span>

- <span data-ttu-id="57352-146">Os itens do LinkedIn são importados para a pasta caixa de entrada na caixa de correio de armazenamento no Office 365.</span><span class="sxs-lookup"><span data-stu-id="57352-146">LinkedIn items are imported to the Inbox folder in the storage mailbox in Office 365.</span></span> <span data-ttu-id="57352-147">Eles aparecem como mensagens de email.</span><span class="sxs-lookup"><span data-stu-id="57352-147">They appear as email messages.</span></span> <span data-ttu-id="57352-148">O nome de exibição do remetente da mensagem é o nome da página da empresa do LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="57352-148">The display name of the sender of the message is the name of the LinkedIn Company Page.</span></span> <span data-ttu-id="57352-149">O endereço de email real do remetente é o endereço de email da caixa de correio de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="57352-149">The actual email address of the sender is the email address of the storage mailbox.</span></span> <span data-ttu-id="57352-150">O nome da página da empresa também é acrescentado à linha de assunto.</span><span class="sxs-lookup"><span data-stu-id="57352-150">The name of the company page is also pre-appended to the subject line.</span></span> 

- <span data-ttu-id="57352-151">Devido ao comportamento anterior, você pode pesquisar as propriedades `from` ou `subject` email ao usar uma ferramenta de descoberta eletrônica da Microsoft para pesquisar itens do LinkedIn que são arquivados no Office 365.</span><span class="sxs-lookup"><span data-stu-id="57352-151">Because of the previous behavior, you can search the `from` or `subject` email properties when using a Microsoft eDiscovery tool to search LinkedIn items that are archived in Office 365.</span></span> <span data-ttu-id="57352-152">Por exemplo, se o nome da página da empresa for "página da empresa contoso", então você poderá usar uma das seguintes *Propriedades:* pares de valores na consulta de pesquisa de palavra-chave:</span><span class="sxs-lookup"><span data-stu-id="57352-152">For example if the name of the company page is "Contoso Company Page", then you can use one of the following *property:value* pairs in the keyword search query:</span></span>
   
   ```
   from:"Contoso Company Page"
   ```

    <span data-ttu-id="57352-153">Ou</span><span class="sxs-lookup"><span data-stu-id="57352-153">Or</span></span>

   ```
   subject:"Contoso Company Page"
   ```

- <span data-ttu-id="57352-154">Para facilitar a localização ou o gerenciamento de itens do LinkedIn importados para o Office 365, o proprietário da caixa de correio de armazenamento (ou qualquer pessoa que tenha atribuído a permissão FullAccess) pode configurar uma regra de caixa de entrada para mover os itens de uma página específica da empresa do LinkedIn para uma pasta específica.</span><span class="sxs-lookup"><span data-stu-id="57352-154">To make it easier to locate or manage LinkedIn items imported to Office 365, the owner of the storage mailbox (or anyone assigned the FullAccess permission) can set up an inbox rule to move the items from a specific LinkedIn Company page to a specific folder.</span></span> <span data-ttu-id="57352-155">Isso é útil se a caixa de correio de armazenamento é usada para arquivar itens importados de diferentes fontes de dados de terceiros.</span><span class="sxs-lookup"><span data-stu-id="57352-155">This is helpful if the storage mailbox is used to archive items that are imported from different third-party data sources.</span></span> <span data-ttu-id="57352-156">Por exemplo, você pode criar uma regra de caixa de entrada que move todos os itens que contêm o nome de uma página específica da empresa do LinkedIn no campo assunto para uma pasta específica.</span><span class="sxs-lookup"><span data-stu-id="57352-156">For example, you can create an inbox rule that moves all items that contain the name of a specific LinkedIn Company page in the subject field to a specific folder.</span></span>
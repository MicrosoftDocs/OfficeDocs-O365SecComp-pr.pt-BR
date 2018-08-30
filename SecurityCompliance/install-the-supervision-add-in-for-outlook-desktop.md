---
title: Instalar o suplemento de supervisão da área de trabalho do Outlook
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: 6/19/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
- ZOL160
ms.assetid: 6c5620e6-aba3-4910-8f3a-b55451656ff7
description: Instalar o suplemento do Office 365 supervisão para a versão da área de trabalho do Outlook
ms.openlocfilehash: 0bddf305087bf0d9552c7671da5306db8352143f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523567"
---
# <a name="install-the-supervision-add-in-for-outlook-desktop"></a><span data-ttu-id="e7c78-103">Instalar o suplemento de supervisão da área de trabalho do Outlook</span><span class="sxs-lookup"><span data-stu-id="e7c78-103">Install the Supervision add-in for Outlook desktop</span></span>

<span data-ttu-id="e7c78-p101">Para revisar identificadas por uma política de supervisão de comunicações, o uso de revisores o suplemento de supervisão para o Outlook e Outlook web app. O suplemento é instalado automaticamente no Outlook web app para todos os revisores que você especificou na política. No entanto, os revisores devem executar algumas etapas para instalá-lo na versão para desktop do Outlook.</span><span class="sxs-lookup"><span data-stu-id="e7c78-p101">To review communications identified by a supervision policy, reviewers use the Supervision add-in for Outlook and Outlook web app. The add-in is installed automatically in Outlook web app for all reviewers you specified in the policy. However, reviewers must run through some steps to install it in the desktop version of Outlook.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e7c78-p102">Usando diretivas de supervisão requer uma assinatura do Office 365 E5 para sua organização. Se você não tiver que plano e quiser tentar supervisão, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="e7c78-p102">Using supervision policies requires an Office 365 E5 subscription for your organization. If you don't have that plan and want to try supervision, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="step-1-copy-the-address-for-the-supervision-mailbox"></a><span data-ttu-id="e7c78-109">Etapa 1: Copie o endereço da caixa de correio de supervisão</span><span class="sxs-lookup"><span data-stu-id="e7c78-109">Step 1: Copy the address for the supervision mailbox</span></span>

<span data-ttu-id="e7c78-110">Para instalar o suplemento para desktop do Outlook, você precisará o endereço para a caixa de correio de supervisão que foi criada como parte da configuração da diretiva de supervisão.</span><span class="sxs-lookup"><span data-stu-id="e7c78-110">To install the add-in for Outlook desktop, you'll need the address for the supervision mailbox that was created as part of the supervision policy setup.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e7c78-111">Se alguém criou a política, você precisará obter esse endereço a partir deles para instalar o suplemento.</span><span class="sxs-lookup"><span data-stu-id="e7c78-111">If someone else created the policy, you'll need to get this address from them to install the add-in.</span></span> 
  
 <span data-ttu-id="e7c78-112">**Para localizar o endereço da caixa de correio de supervisão**</span><span class="sxs-lookup"><span data-stu-id="e7c78-112">**To find the supervision mailbox address**</span></span>
  
1. <span data-ttu-id="e7c78-113">Entrar no [segurança &amp; Centro de conformidade](https://protection.office.com) usando credenciais de uma conta de administrador em sua organização do Office 365.</span><span class="sxs-lookup"><span data-stu-id="e7c78-113">Sign into the [Security &amp; Compliance Center](https://protection.office.com) using credentials for an admin account in your Office 365 organization.</span></span> 
    
2. <span data-ttu-id="e7c78-114">Vá até a **governança de dados** \> **supervisão**.</span><span class="sxs-lookup"><span data-stu-id="e7c78-114">Go to **Data governance** \> **Supervision**.</span></span>
    
3. <span data-ttu-id="e7c78-115">Clique na política de supervisão que está juntando as comunicações que você deseja analisar.</span><span class="sxs-lookup"><span data-stu-id="e7c78-115">Click the supervision policy that's gathering the communications you want to review.</span></span>
    
4. <span data-ttu-id="e7c78-116">Na política detalha submenu, em * * caixa de correio de supervisão * *, copie o endereço.</span><span class="sxs-lookup"><span data-stu-id="e7c78-116">In the policy details flyout, under ** Supervision mailbox **, copy the address.</span></span> 
    
    ![A seção de 'Caixa de correio de supervisão' do submenu de detalhes de uma diretiva de supervisão mostrando o endereço da caixa de correio de supervisão realçado](media/71779d0e-4f01-4dd3-8234-5f9c30eeb067.jpg)
  
## <a name="step-2-configure-the-supervision-mailbox-for-outlook-desktop-access"></a><span data-ttu-id="e7c78-118">Etapa 2: Configurar a caixa de correio de supervisão para acesso de área de trabalho do Outlook</span><span class="sxs-lookup"><span data-stu-id="e7c78-118">Step 2: Configure the supervision mailbox for Outlook desktop access</span></span>

<span data-ttu-id="e7c78-119">Em seguida, os revisores precisará executar alguns comandos do PowerShell do Exchange Online para que eles possam se conectar à caixa de correio de supervisão.</span><span class="sxs-lookup"><span data-stu-id="e7c78-119">Next, reviewers will need to run a couple Exchange Online PowerShell commands so they can connect Outlook to the supervision mailbox.</span></span>
  
1. <span data-ttu-id="e7c78-p103">Conecte-se para o Exchange Online PowerShell. [Como fazer isso?](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)</span><span class="sxs-lookup"><span data-stu-id="e7c78-p103">Connect to Exchange Online PowerShell. [How do I do this?](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)</span></span>
    
2. <span data-ttu-id="e7c78-122">Execute os seguintes comandos.</span><span class="sxs-lookup"><span data-stu-id="e7c78-122">Run the following commands.</span></span>
    
  ```
  Add-MailboxPermission "SupervisoryReview{GUID}@domain.onmicrosoft.com" -User <alias or email address of the account that has reviewer permissions to the supervision mailbox> -AccessRights FullAccessSet-Mailbox "<SupervisoryReview{GUID}@domain.onmicrosoft.com>" -HiddenFromAddressListsEnabled: $false
  ```

    <span data-ttu-id="e7c78-123">Onde *SupervisoryReview{GUID}@domain.onmicrosoft.com* é o endereço que você copiou na etapa 1 acima, e o *usuário* é o nome do revisor que se conectarão à caixa de correio de supervisão na próxima etapa.</span><span class="sxs-lookup"><span data-stu-id="e7c78-123">Where  *SupervisoryReview{GUID}@domain.onmicrosoft.com*  is the address you copied in Step 1 above, and  *User*  is the name of the reviewer who will be connecting to the supervision mailbox in the next step.</span></span> 
    
3. <span data-ttu-id="e7c78-124">Aguarde pelo menos uma hora antes de prosseguir para a etapa 3 abaixo.</span><span class="sxs-lookup"><span data-stu-id="e7c78-124">Wait at least an hour before moving on to Step 3 below.</span></span>
    
## <a name="step-3-create-an-outlook-profile-to-connect-to-the-supervision-mailbox"></a><span data-ttu-id="e7c78-125">Etapa 3: Criar um perfil do Outlook para se conectar à caixa de correio de supervisão</span><span class="sxs-lookup"><span data-stu-id="e7c78-125">Step 3: Create an Outlook profile to connect to the supervision mailbox</span></span>

<span data-ttu-id="e7c78-126">Para a etapa final, serão necessário criar um perfil do Outlook para se conectar à caixa de correio de supervisão revisores.</span><span class="sxs-lookup"><span data-stu-id="e7c78-126">For the final step, reviewers will need to create an Outlook profile to connect to the supervision mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e7c78-p104">Para criar um novo perfil do Outlook, você usará as configurações de email no painel de controle do Windows. O caminho que você tomar para chegar a essas configurações pode dependem de qual sistema operacional do Windows (Windows 7, Windows 8 ou Windows 10) que você está usando e qual versão do Outlook está instalada.</span><span class="sxs-lookup"><span data-stu-id="e7c78-p104">To create a new Outlook profile, you'll use the Mail settings in the Windows Control Panel. The path you take to get to these settings might depend on which Windows operating system (Windows 7, Windows 8, or Windows 10) you're using and which version of Outlook is installed.</span></span> 
  
1. <span data-ttu-id="e7c78-129">Abra o painel de controle e, na caixa **Pesquisar** na parte superior da janela, digite o **email**.</span><span class="sxs-lookup"><span data-stu-id="e7c78-129">Open the Control Panel, and in the **Search** box at the top of the window, type **Mail**.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="e7c78-p105">Não tem certeza como chegar ao painel de controle? Consulte [onde está o painel de controle?](https://support.microsoft.com/help/13764/windows-where-is-control-panel)</span><span class="sxs-lookup"><span data-stu-id="e7c78-p105">Not sure how to get to the Control Panel? See [Where is Control Panel?](https://support.microsoft.com/help/13764/windows-where-is-control-panel)</span></span>
  
2. <span data-ttu-id="e7c78-132">Abra o aplicativo de **email** .</span><span class="sxs-lookup"><span data-stu-id="e7c78-132">Open the **Mail** app.</span></span> 
    
3. <span data-ttu-id="e7c78-133">Em **Configurar email - Outlook**, clique em **Mostrar perfis**.</span><span class="sxs-lookup"><span data-stu-id="e7c78-133">In **Mail Setup - Outlook**, click **Show Profiles**.</span></span>
    
    !['Configurar email - Outlook' caixa de diálogo com o botão Mostrar perfis realçado](media/28b5dae9-d10c-4f2b-926a-294c857d555c.jpg)
  
4. <span data-ttu-id="e7c78-p106">No **email**, clique em **Adicionar**. Em seguida, em **Novo perfil**, digite um nome para a caixa de correio de supervisão (por exemplo, **supervisão**).</span><span class="sxs-lookup"><span data-stu-id="e7c78-p106">In **Mail**, click **Add**. Then, in **New Profile**, enter a name for the supervision mailbox (such as **Supervision**).</span></span>
    
    ![A caixa de diálogo 'Novo perfil' Mostrar o nome 'Supervisão' na caixa Nome do perfil](media/d02ae181-b541-4ec6-8f51-698f30033204.jpg)
  
5. <span data-ttu-id="e7c78-138">No **Outlook se conectar ao Office 365**, clique em **Conectar para uma conta diferente**.</span><span class="sxs-lookup"><span data-stu-id="e7c78-138">In **Connect Outlook to Office 365**, click **Connect to a different account**.</span></span>
    
    ![A mensagem 'Conectar o Outlook para o Office 365' com o link 'Conectar-se para uma conta diferente' realçado](media/fac49ff8-a7f0-4e82-a271-9ec045a95de1.jpg)
  
6. <span data-ttu-id="e7c78-140">Na **Configuração automática de conta**, escolha a **instalação Manual ou tipos de servidor adicionais**e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="e7c78-140">In **Auto Account Setup**, choose **Manual setup or additional server types**, and then click **Next**.</span></span>
    
7. <span data-ttu-id="e7c78-p107">Em **Escolha seu tipo de conta**, escolha o **Office 365**. Em seguida, na caixa **Endereço de Email** , digite o endereço da caixa de correio de supervisão que você copiou anteriormente.</span><span class="sxs-lookup"><span data-stu-id="e7c78-p107">In **Choose Your Account Type**, choose **Office 365**. Then, in the **Email Address** box, enter the address of the supervision mailbox you copied previously.</span></span> 
    
    ![A página 'Escolher o tipo de conta' da caixa de diálogo Adicionar conta no Outlook, mostrando a caixa de 'endereço de Email ' realçada.](media/4f601236-9f69-4cf6-a58c-0b91204aa8cb.jpg)
  
8. <span data-ttu-id="e7c78-144">Quando solicitado, insira suas credenciais do Office 365.</span><span class="sxs-lookup"><span data-stu-id="e7c78-144">When prompted, enter your Office 365 credentials.</span></span>
    
9. <span data-ttu-id="e7c78-145">Se tiver êxito, você verá o **supervisão - \<nome da política\> ** pasta listada no modo de exibição lista de pastas no Outlook.</span><span class="sxs-lookup"><span data-stu-id="e7c78-145">If successful, you'll see the **Supervision - \<policy name\>** folder listed in the Folder List view in Outlook.</span></span> 
    


---
title: Instalar o suplemento de supervisão da área de trabalho do Outlook
ms.author: robmazz
author: robmazz
manager: laurawi
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
ms.openlocfilehash: b0cb0d78ab5f8887628528dd53b49fb15de44126
ms.sourcegitcommit: 204fb0269b5c10b63941055824e863d77e3e9b02
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/06/2018
ms.locfileid: "27180861"
---
# <a name="install-the-supervision-add-in-for-outlook-desktop"></a><span data-ttu-id="2d769-103">Instalar o suplemento de supervisão da área de trabalho do Outlook</span><span class="sxs-lookup"><span data-stu-id="2d769-103">Install the Supervision add-in for Outlook desktop</span></span>

<span data-ttu-id="2d769-p101">Para revisar identificadas por uma política de supervisão de comunicações, o uso de revisores o suplemento de supervisão para o Outlook e Outlook web app. O suplemento é instalado automaticamente no Outlook web app para todos os revisores que você especificou na política. No entanto, os revisores devem executar algumas etapas para instalá-lo na versão para desktop do Outlook.</span><span class="sxs-lookup"><span data-stu-id="2d769-p101">To review communications identified by a supervision policy, reviewers use the Supervision add-in for Outlook and Outlook web app. The add-in is installed automatically in Outlook web app for all reviewers you specified in the policy. However, reviewers must run through some steps to install it in the desktop version of Outlook.</span></span>
  
> [!NOTE]
> <span data-ttu-id="2d769-p102">Usuários monitorados pelo diretivas de supervisão devem ter uma licença de Office 365 Enterprise E3 com o complemento de conformidade avançadas ou ser incluídos em uma assinatura do Office 365 Enterprise E5. Se você não tiver um plano de Enterprise E5 existente e quiser tentar supervisão, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="2d769-p102">Users monitored by supervision policies must have either an Office 365 Enterprise E3 license with the Advanced Compliance add-on or be included in an Office 365 Enterprise E5 subscription. If you don't have an existing Enterprise E5 plan and want to try supervision, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span>
  
## <a name="step-1-copy-the-address-for-the-supervision-mailbox"></a><span data-ttu-id="2d769-109">Etapa 1: Copie o endereço da caixa de correio de supervisão</span><span class="sxs-lookup"><span data-stu-id="2d769-109">Step 1: Copy the address for the supervision mailbox</span></span>

<span data-ttu-id="2d769-110">Para instalar o suplemento para desktop do Outlook, você precisará o endereço para a caixa de correio de supervisão que foi criada como parte da configuração da diretiva de supervisão.</span><span class="sxs-lookup"><span data-stu-id="2d769-110">To install the add-in for Outlook desktop, you'll need the address for the supervision mailbox that was created as part of the supervision policy setup.</span></span>
  
> [!NOTE]
> <span data-ttu-id="2d769-111">Se alguém criou a política, você precisará obter esse endereço a partir deles para instalar o suplemento.</span><span class="sxs-lookup"><span data-stu-id="2d769-111">If someone else created the policy, you'll need to get this address from them to install the add-in.</span></span>
 
 <span data-ttu-id="2d769-112">**Para localizar o endereço da caixa de correio de supervisão**</span><span class="sxs-lookup"><span data-stu-id="2d769-112">**To find the supervision mailbox address**</span></span>
  
1. <span data-ttu-id="2d769-113">Entrar no [segurança &amp; Centro de conformidade](https://protection.office.com) usando credenciais de uma conta de administrador em sua organização do Office 365.</span><span class="sxs-lookup"><span data-stu-id="2d769-113">Sign into the [Security &amp; Compliance Center](https://protection.office.com) using credentials for an admin account in your Office 365 organization.</span></span>
    
2. <span data-ttu-id="2d769-114">Vá até a **governança de dados** \> **supervisão**.</span><span class="sxs-lookup"><span data-stu-id="2d769-114">Go to **Data governance** \> **Supervision**.</span></span>
    
3. <span data-ttu-id="2d769-115">Clique na política de supervisão que está juntando as comunicações que você deseja analisar.</span><span class="sxs-lookup"><span data-stu-id="2d769-115">Click the supervision policy that's gathering the communications you want to review.</span></span>
    
4. <span data-ttu-id="2d769-116">Na política detalha submenu, em \* \* caixa de correio de supervisão \* \*, copie o endereço.</span><span class="sxs-lookup"><span data-stu-id="2d769-116">In the policy details flyout, under \*\* Supervision mailbox \*\*, copy the address.</span></span><br/>![A seção de 'Caixa de correio de supervisão' do submenu de detalhes de uma diretiva de supervisão mostrando o endereço da caixa de correio de supervisão realçado](media/71779d0e-4f01-4dd3-8234-5f9c30eeb067.jpg)
  
## <a name="step-2-configure-the-supervision-mailbox-for-outlook-desktop-access"></a><span data-ttu-id="2d769-118">Etapa 2: Configurar a caixa de correio de supervisão para acesso de área de trabalho do Outlook</span><span class="sxs-lookup"><span data-stu-id="2d769-118">Step 2: Configure the supervision mailbox for Outlook desktop access</span></span>

<span data-ttu-id="2d769-119">Em seguida, os revisores precisará executar alguns comandos do PowerShell do Exchange Online para que eles possam se conectar à caixa de correio de supervisão.</span><span class="sxs-lookup"><span data-stu-id="2d769-119">Next, reviewers will need to run a couple Exchange Online PowerShell commands so they can connect Outlook to the supervision mailbox.</span></span>
  
1. <span data-ttu-id="2d769-p103">Conecte-se para o Exchange Online PowerShell. [Como fazer isso?](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)</span><span class="sxs-lookup"><span data-stu-id="2d769-p103">Connect to Exchange Online PowerShell. [How do I do this?](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)</span></span>
    
2. <span data-ttu-id="2d769-122">Execute os seguintes comandos, onde *SupervisoryReview{GUID}@domain.onmicrosoft.com* é o endereço que você copiou na etapa 1 acima, e o *usuário* é o nome do revisor que se conectarão à caixa de correio de supervisão na etapa 3.</span><span class="sxs-lookup"><span data-stu-id="2d769-122">Run the following commands, where  *SupervisoryReview{GUID}@domain.onmicrosoft.com*  is the address you copied in Step 1 above, and  *User*  is the name of the reviewer who will be connecting to the supervision mailbox in Step 3.</span></span>
    - ```Add-MailboxPermission "SupervisoryReview{GUID}@domain.onmicrosoft.com" -User <alias or email address of the account that has reviewer permissions to the supervision mailbox> -AccessRights FullAccess```<br/>
    - ```Set-Mailbox "<SupervisoryReview{GUID}@domain.onmicrosoft.com>" -HiddenFromAddressListsEnabled: $false```
    
3. <span data-ttu-id="2d769-123">Aguarde pelo menos uma hora antes de prosseguir para a etapa 3 abaixo.</span><span class="sxs-lookup"><span data-stu-id="2d769-123">Wait at least an hour before moving on to Step 3 below.</span></span>
    
## <a name="step-3-create-an-outlook-profile-to-connect-to-the-supervision-mailbox"></a><span data-ttu-id="2d769-124">Etapa 3: Criar um perfil do Outlook para se conectar à caixa de correio de supervisão</span><span class="sxs-lookup"><span data-stu-id="2d769-124">Step 3: Create an Outlook profile to connect to the supervision mailbox</span></span>

<span data-ttu-id="2d769-125">Para a etapa final, serão necessário criar um perfil do Outlook para se conectar à caixa de correio de supervisão revisores.</span><span class="sxs-lookup"><span data-stu-id="2d769-125">For the final step, reviewers will need to create an Outlook profile to connect to the supervision mailbox.</span></span>
 
> [!NOTE]
> <span data-ttu-id="2d769-p104">Para criar um novo perfil do Outlook, você usará as configurações de email no painel de controle do Windows. O caminho que você tomar para chegar a essas configurações pode dependem de qual sistema operacional do Windows (Windows 7, Windows 8 ou Windows 10) que você está usando e qual versão do Outlook está instalada.</span><span class="sxs-lookup"><span data-stu-id="2d769-p104">To create a new Outlook profile, you'll use the Mail settings in the Windows Control Panel. The path you take to get to these settings might depend on which Windows operating system (Windows 7, Windows 8, or Windows 10) you're using and which version of Outlook is installed.</span></span>
  
1. <span data-ttu-id="2d769-128">Abra o painel de controle e, na caixa **Pesquisar** na parte superior da janela, digite o **email**.</span><span class="sxs-lookup"><span data-stu-id="2d769-128">Open the Control Panel, and in the **Search** box at the top of the window, type **Mail**.</span></span><br/><span data-ttu-id="2d769-p105">(Não tem certeza como chegar ao painel de controle? Consulte [onde está o painel de controle?](https://support.microsoft.com/help/13764/windows-where-is-control-panel))</span><span class="sxs-lookup"><span data-stu-id="2d769-p105">(Not sure how to get to the Control Panel? See [Where is Control Panel?](https://support.microsoft.com/help/13764/windows-where-is-control-panel))</span></span>
  
2. <span data-ttu-id="2d769-131">Abra o aplicativo de **email** .</span><span class="sxs-lookup"><span data-stu-id="2d769-131">Open the **Mail** app.</span></span>
    
3. <span data-ttu-id="2d769-132">Em **Configurar email - Outlook**, clique em **Mostrar perfis**.</span><span class="sxs-lookup"><span data-stu-id="2d769-132">In **Mail Setup - Outlook**, click **Show Profiles**.</span></span><br/><span data-ttu-id="2d769-133">!['Configurar email - Outlook' caixa de diálogo com o botão Mostrar perfis realçado](media/28b5dae9-d10c-4f2b-926a-294c857d555c.jpg)</span><span class="sxs-lookup"><span data-stu-id="2d769-133">![The 'Mail Setup - Outlook' dialog box with the 'Show Profiles' button highlighted](media/28b5dae9-d10c-4f2b-926a-294c857d555c.jpg)</span></span>
  
4. <span data-ttu-id="2d769-p106">No **email**, clique em **Adicionar**. Em seguida, em **Novo perfil**, digite um nome para a caixa de correio de supervisão (por exemplo, **supervisão**).</span><span class="sxs-lookup"><span data-stu-id="2d769-p106">In **Mail**, click **Add**. Then, in **New Profile**, enter a name for the supervision mailbox (such as **Supervision**).</span></span><br/><span data-ttu-id="2d769-136">![A caixa de diálogo 'Novo perfil' Mostrar o nome 'Supervisão' na caixa Nome do perfil](media/d02ae181-b541-4ec6-8f51-698f30033204.jpg)</span><span class="sxs-lookup"><span data-stu-id="2d769-136">![The 'New Profile' dialog showing the name 'Supervision' in the 'Profile Name' box](media/d02ae181-b541-4ec6-8f51-698f30033204.jpg)</span></span>
  
5. <span data-ttu-id="2d769-137">No **Outlook se conectar ao Office 365**, clique em **Conectar para uma conta diferente**.</span><span class="sxs-lookup"><span data-stu-id="2d769-137">In **Connect Outlook to Office 365**, click **Connect to a different account**.</span></span><br/><span data-ttu-id="2d769-138">![A mensagem 'Conectar o Outlook para o Office 365' com o link 'Conectar-se para uma conta diferente' realçado](media/fac49ff8-a7f0-4e82-a271-9ec045a95de1.jpg)</span><span class="sxs-lookup"><span data-stu-id="2d769-138">![The 'Connect Outlook to Office 365' message with the 'Connect to a different account' link highlighted](media/fac49ff8-a7f0-4e82-a271-9ec045a95de1.jpg)</span></span>
  
6. <span data-ttu-id="2d769-139">Na **Configuração automática de conta**, escolha a **instalação Manual ou tipos de servidor adicionais**e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="2d769-139">In **Auto Account Setup**, choose **Manual setup or additional server types**, and then click **Next**.</span></span>
    
7. <span data-ttu-id="2d769-p107">Em **Escolha seu tipo de conta**, escolha o **Office 365**. Em seguida, na caixa **Endereço de Email** , digite o endereço da caixa de correio de supervisão que você copiou anteriormente.</span><span class="sxs-lookup"><span data-stu-id="2d769-p107">In **Choose Your Account Type**, choose **Office 365**. Then, in the **Email Address** box, enter the address of the supervision mailbox you copied previously.</span></span><br/><span data-ttu-id="2d769-142">![A página 'Escolher o tipo de conta' da caixa de diálogo Adicionar conta no Outlook, mostrando a caixa de 'endereço de Email ' realçada.](media/4f601236-9f69-4cf6-a58c-0b91204aa8cb.jpg)</span><span class="sxs-lookup"><span data-stu-id="2d769-142">![The 'Choose Your Account Type' page of the 'Add Account' dialog in Outlook showing the 'Email Address' box highlighted.](media/4f601236-9f69-4cf6-a58c-0b91204aa8cb.jpg)</span></span>
  
8. <span data-ttu-id="2d769-143">Quando solicitado, insira suas credenciais do Office 365.</span><span class="sxs-lookup"><span data-stu-id="2d769-143">When prompted, enter your Office 365 credentials.</span></span>
    
9. <span data-ttu-id="2d769-144">Se tiver êxito, você verá o \*\*supervisão - \<nome da política\> \*\* pasta listada no modo de exibição lista de pastas no Outlook.</span><span class="sxs-lookup"><span data-stu-id="2d769-144">If successful, you'll see the **Supervision - \<policy name\>** folder listed in the Folder List view in Outlook.</span></span>
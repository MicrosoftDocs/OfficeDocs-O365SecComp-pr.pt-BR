---
title: Configurar uma lista de URLs bloqueadas personalizada usando os links seguros de ATP do Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
audience: Admin
ms.topic: article
ms.date: 02/06/2019
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 896a7efb-1683-465e-a394-261349e5d866
ms.collection:
- M365-security-compliance
description: Saiba como configurar uma lista de URLs bloqueadas para sua organização usando a proteção avançada contra ameaças do Office 365. As URLs bloqueadas serão aplicadas a mensagens de email e documentos do Office de acordo com as políticas de links seguros de ATP.
ms.openlocfilehash: 4856d0ae76318c99a9c9c2404ef8a4cd700e4953
ms.sourcegitcommit: 4fedeb06a6e7796096fc6279cfb091c7b89d484d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/31/2019
ms.locfileid: "34652714"
---
# <a name="set-up-a-custom-blocked-urls-list-using-office-365-atp-safe-links"></a><span data-ttu-id="843c1-104">Configurar uma lista de URLs bloqueadas personalizada usando os links seguros de ATP do Office 365</span><span class="sxs-lookup"><span data-stu-id="843c1-104">Set up a custom blocked URLs list using Office 365 ATP Safe Links</span></span>

> [!IMPORTANT]
> <span data-ttu-id="843c1-105">Este artigo destina-se a clientes corporativos com [proteção avançada contra ameaças do Office 365](office-365-atp.md).</span><span class="sxs-lookup"><span data-stu-id="843c1-105">This article is intended for business customers who have [Office 365 Advanced Threat Protection](office-365-atp.md).</span></span> <span data-ttu-id="843c1-106">Se você for um usuário doméstico que procura informações sobre links seguros no Outlook, consulte [Advanced Outlook.com Security](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2).</span><span class="sxs-lookup"><span data-stu-id="843c1-106">If you are a home user looking for information about Safe Links in Outlook, see [Advanced Outlook.com security](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2).</span></span>

<span data-ttu-id="843c1-107">Com a [proteção avançada contra ameaças do Office 365](office-365-atp.md) (ATP), sua organização pode ter uma lista personalizada de endereços de sites (URLs) bloqueadas.</span><span class="sxs-lookup"><span data-stu-id="843c1-107">With [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP), your organization can have a custom list of website addresses (URLs) that are blocked.</span></span> <span data-ttu-id="843c1-108">Quando uma URL é bloqueada, as pessoas que clicam em links para a URL bloqueada são levadas para uma [página de aviso](atp-safe-links-warning-pages.md) que se assemelha à seguinte imagem:</span><span class="sxs-lookup"><span data-stu-id="843c1-108">When a URL is blocked, people who click on links to the blocked URL are taken to a [warning page](atp-safe-links-warning-pages.md) that resembles the following image:</span></span> 
  
![Este site é bloqueado](media/6b4bda2d-a1e6-419e-8b10-588e83c3af3f.png)
  
<span data-ttu-id="843c1-110">A lista de URLs bloqueadas é definida pela equipe de segurança do Office 365 da sua organização e essa lista se aplica a todos na organização que estão cobertos por políticas de links seguros do Office 365 ATP.</span><span class="sxs-lookup"><span data-stu-id="843c1-110">The blocked URLs list is defined by your organization's Office 365 security team, and that list applies to everyone in the organization who is covered by Office 365 ATP Safe Links policies.</span></span> 
  
<span data-ttu-id="843c1-111">Leia este artigo para saber como configurar a lista de URLs bloqueadas personalizadas da sua organização para [links seguros de ATP no Office 365](atp-safe-links.md).</span><span class="sxs-lookup"><span data-stu-id="843c1-111">Read this article to learn how to set up your organization's custom blocked URLs list for [ATP Safe Links in Office 365](atp-safe-links.md).</span></span>
  
## <a name="view-or-edit-a-custom-list-of-blocked-urls"></a><span data-ttu-id="843c1-112">Exibir ou editar uma lista personalizada de URLs bloqueadas</span><span class="sxs-lookup"><span data-stu-id="843c1-112">View or edit a custom list of blocked URLs</span></span>

<span data-ttu-id="843c1-113">Os [links seguros de ATP no Office 365](atp-safe-links.md) usam várias listas, incluindo a lista de URLs bloqueadas da sua organização.</span><span class="sxs-lookup"><span data-stu-id="843c1-113">[ATP Safe Links in Office 365](atp-safe-links.md) uses several lists, including your organization's custom blocked URLs list.</span></span> <span data-ttu-id="843c1-114">Se tiver as permissões necessárias, você poderá configurar a lista personalizada da sua organização.</span><span class="sxs-lookup"><span data-stu-id="843c1-114">If you have the necessary permissions, you can set up your organization's custom list.</span></span> <span data-ttu-id="843c1-115">Para fazer isso, edite a política de links seguros padrão da sua organização.</span><span class="sxs-lookup"><span data-stu-id="843c1-115">You do this by editing your organization's default Safe Links policy.</span></span>

<span data-ttu-id="843c1-116">Para editar (ou definir) políticas ATP, você deve receber uma das funções descritas na tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="843c1-116">To edit (or define) ATP policies, you must be assigned one of the roles described in the following table:</span></span> 

|<span data-ttu-id="843c1-117">Role</span><span class="sxs-lookup"><span data-stu-id="843c1-117">Role</span></span>  |<span data-ttu-id="843c1-118">Onde/como a atribuição</span><span class="sxs-lookup"><span data-stu-id="843c1-118">Where/how assigned</span></span>  |
|---------|---------|
|<span data-ttu-id="843c1-119">Administrador global do Office 365</span><span class="sxs-lookup"><span data-stu-id="843c1-119">Office 365 Global Administrator</span></span> |<span data-ttu-id="843c1-120">Por padrão, a pessoa que se inscreve para comprar o Office 365 é um administrador global.</span><span class="sxs-lookup"><span data-stu-id="843c1-120">The person who signs up to buy Office 365 is a global admin by default.</span></span> <span data-ttu-id="843c1-121">(Confira [sobre as funções de administrador do Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) para saber mais.)</span><span class="sxs-lookup"><span data-stu-id="843c1-121">(See [About Office 365 admin roles](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) to learn more.)</span></span>         |
|<span data-ttu-id="843c1-122">Administrador de segurança</span><span class="sxs-lookup"><span data-stu-id="843c1-122">Security Administrator</span></span> |<span data-ttu-id="843c1-123">Centro de administração do Azure Active[https://aad.portal.azure.com](https://aad.portal.azure.com)Directory ()</span><span class="sxs-lookup"><span data-stu-id="843c1-123">Azure Active Directory admin center ([https://aad.portal.azure.com](https://aad.portal.azure.com))</span></span>|
|<span data-ttu-id="843c1-124">Gerenciamento da organização do Exchange Online</span><span class="sxs-lookup"><span data-stu-id="843c1-124">Exchange Online Organization Management</span></span> |<span data-ttu-id="843c1-125">Centro de administração do[https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)Exchange ()</span><span class="sxs-lookup"><span data-stu-id="843c1-125">Exchange admin center ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp))</span></span> <br><span data-ttu-id="843c1-126">ou</span><span class="sxs-lookup"><span data-stu-id="843c1-126">or</span></span> <br>  <span data-ttu-id="843c1-127">Cmdlets do PowerShell (consulte [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps))</span><span class="sxs-lookup"><span data-stu-id="843c1-127">PowerShell cmdlets (See [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps))</span></span> |

> [!TIP]
> <span data-ttu-id="843c1-128">Para saber mais sobre funções e permissões, confira [permissões no centro de conformidade &amp; de segurança do Office 365](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="843c1-128">To learn more about roles and permissions, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

### <a name="to-view-or-edit-a-custom-blocked-urls-list"></a><span data-ttu-id="843c1-129">Para exibir ou editar uma lista de URLs bloqueadas personalizada</span><span class="sxs-lookup"><span data-stu-id="843c1-129">To view or edit a custom blocked URLs list</span></span>
  
1. <span data-ttu-id="843c1-130">Acesse [https://protection.office.com](https://protection.office.com) e entre com sua conta corporativa ou de estudante.</span><span class="sxs-lookup"><span data-stu-id="843c1-130">Go to [https://protection.office.com](https://protection.office.com) and sign in with your work or school account.</span></span> 
    
2. <span data-ttu-id="843c1-131">Na navegação à esquerda, em **Gerenciamento de ameaças**, escolha **links seguros**de **política** \> .</span><span class="sxs-lookup"><span data-stu-id="843c1-131">In the left navigation, under **Threat management**, choose **Policy** \> **Safe Links**.</span></span>
    
3. <span data-ttu-id="843c1-132">Na seção **políticas que se aplicam a toda a organização** , selecione **padrão**e, em seguida, escolha **Editar** (o botão Editar parece um lápis).</span><span class="sxs-lookup"><span data-stu-id="843c1-132">In the **Policies that apply to the entire organization** section, select **Default**, and then choose **Edit** (the Edit button resembles a pencil).</span></span><br/><span data-ttu-id="843c1-133">![Clique em Editar para editar a política padrão para proteção de links seguros](media/d08f9615-d947-4033-813a-d310ec2c8cca.png)</span><span class="sxs-lookup"><span data-stu-id="843c1-133">![Click Edit to edit your default policy for Safe Links protection](media/d08f9615-d947-4033-813a-d310ec2c8cca.png)</span></span><br/><span data-ttu-id="843c1-134">Isso permite que você exiba a lista de URLs bloqueadas.</span><span class="sxs-lookup"><span data-stu-id="843c1-134">This enables you to view your list of blocked URLs.</span></span> <span data-ttu-id="843c1-135">Em primeiro lugar, talvez você não tenha URLs listadas aqui.</span><span class="sxs-lookup"><span data-stu-id="843c1-135">At first, you might not have any URLs listed here.</span></span><br/><span data-ttu-id="843c1-136">![Lista de URLs bloqueadas na política de links seguros padrão](media/575e1449-6191-40ac-b626-030a2fd3fb11.png)</span><span class="sxs-lookup"><span data-stu-id="843c1-136">![Blocked URLs list in the default Safe Links policy](media/575e1449-6191-40ac-b626-030a2fd3fb11.png)</span></span>
  
4. <span data-ttu-id="843c1-137">Selecione a caixa **Insira uma URL válida** , digite uma URL e, em seguida, escolha o sinal**+** de mais ().</span><span class="sxs-lookup"><span data-stu-id="843c1-137">Select the **Enter a valid URL** box, type a URL, and then choose the plus sign (**+**).</span></span> 

5. <span data-ttu-id="843c1-138">Quando terminar de adicionar URLs, no canto inferior direito da tela, escolha **salvar**.</span><span class="sxs-lookup"><span data-stu-id="843c1-138">When you are finished adding URLs, in the lower right corner of the screen, choose **Save**.</span></span>
    
## <a name="a-few-things-to-keep-in-mind"></a><span data-ttu-id="843c1-139">Há algumas coisas que você deve ter em mente</span><span class="sxs-lookup"><span data-stu-id="843c1-139">A few things to keep in mind</span></span>

<span data-ttu-id="843c1-140">Ao adicionar URLs à sua lista, tenha em mente os seguintes pontos:</span><span class="sxs-lookup"><span data-stu-id="843c1-140">While you add URLs to your list, keep the following points in mind:</span></span> 

- <span data-ttu-id="843c1-141">Não inclua uma barra ( **/**) no final da URL.</span><span class="sxs-lookup"><span data-stu-id="843c1-141">Do not include a forward slash ( **/**) at the end of the URL.</span></span> <span data-ttu-id="843c1-142">Por exemplo, em vez de `http://www.contoso.com/`inserir, `http://www.contoso.com`insira.</span><span class="sxs-lookup"><span data-stu-id="843c1-142">For example, instead of entering `http://www.contoso.com/`, enter `http://www.contoso.com`.</span></span>
    
- <span data-ttu-id="843c1-143">Você pode especificar uma URL somente de domínio (como `contoso.com` ou `tailspintoys.com`).</span><span class="sxs-lookup"><span data-stu-id="843c1-143">You can specify a domain-only URL (like `contoso.com` or `tailspintoys.com`).</span></span> <span data-ttu-id="843c1-144">Isso bloqueará cliques em qualquer URL que contenha o domínio.</span><span class="sxs-lookup"><span data-stu-id="843c1-144">This will block clicks on any URL that contains the domain.</span></span>

- <span data-ttu-id="843c1-145">Você pode especificar um subdomínio (como `toys.contoso.com*`) sem bloquear um domínio completo (como `contoso.com`).</span><span class="sxs-lookup"><span data-stu-id="843c1-145">You can specify a subdomain (like `toys.contoso.com*`) without blocking a full domain (like `contoso.com`).</span></span> <span data-ttu-id="843c1-146">Isso bloqueará cliques em qualquer URL que contenha o subdomínio, mas não bloqueará cliques para uma URL que contenha o domínio completo.</span><span class="sxs-lookup"><span data-stu-id="843c1-146">This will block clicks any URL that contains the subdomain, but it won't block clicks to a URL that contains the full domain.</span></span>  
    
- <span data-ttu-id="843c1-147">Você pode incluir até três asteriscos curinga (\*) por URL.</span><span class="sxs-lookup"><span data-stu-id="843c1-147">You can include up to three wildcard asterisks (\*) per URL.</span></span> <span data-ttu-id="843c1-148">A tabela a seguir lista alguns exemplos do que você pode inserir e o efeito que essas entradas têm.</span><span class="sxs-lookup"><span data-stu-id="843c1-148">The following table lists some examples of what you can enter and what effect those entries have.</span></span>
    
|<span data-ttu-id="843c1-149">**Entrada de exemplo**</span><span class="sxs-lookup"><span data-stu-id="843c1-149">**Example Entry**</span></span>|<span data-ttu-id="843c1-150">**O que ele faz**</span><span class="sxs-lookup"><span data-stu-id="843c1-150">**What It Does**</span></span>|
|:-----|:-----|
|<span data-ttu-id="843c1-151">`contoso.com` ou `*contoso.com*`</span><span class="sxs-lookup"><span data-stu-id="843c1-151">`contoso.com` or `*contoso.com*`</span></span>  <br/> |<span data-ttu-id="843c1-152">Bloqueia o domínio, subdomínios e caminhos, como `https://www.contoso.com`, e `http://sub.contoso.com``http://contoso.com/abc`</span><span class="sxs-lookup"><span data-stu-id="843c1-152">Blocks the domain, subdomains, and paths, such as `https://www.contoso.com`, `http://sub.contoso.com`, and `http://contoso.com/abc`</span></span>  <br/> |
|`http://contoso.com/a`  <br/> |<span data-ttu-id="843c1-153">Bloqueia um site `http://contoso.com/a` , mas não outros subcaminhos como`http://contoso.com/a/b`</span><span class="sxs-lookup"><span data-stu-id="843c1-153">Blocks a site `http://contoso.com/a` but not additional subpaths like `http://contoso.com/a/b`</span></span>  <br/> |
|`http://contoso.com/a*`  <br/> |<span data-ttu-id="843c1-154">Bloqueia um site `http://contoso.com/a` e subcaminhos adicionais, como`http://contoso.com/a/b`</span><span class="sxs-lookup"><span data-stu-id="843c1-154">Blocks a site `http://contoso.com/a` and additional subpaths like `http://contoso.com/a/b`</span></span>  <br/> |
|`http://toys.contoso.com*`  <br/> |<span data-ttu-id="843c1-155">Bloqueia um subdomínio ("Toys" nesse caso), mas permite cliques para outras URLs de domínio ( `http://contoso.com` como `http://home.contoso.com`ou).</span><span class="sxs-lookup"><span data-stu-id="843c1-155">Blocks a subdomain ("toys" in this case) but allow clicks to other domain URLs (like `http://contoso.com` or `http://home.contoso.com`).</span></span>  <br/> |
   

## <a name="how-to-define-exceptions-for-certain-users-in-an-organization"></a><span data-ttu-id="843c1-156">Como definir exceções para determinados usuários em uma organização</span><span class="sxs-lookup"><span data-stu-id="843c1-156">How to define exceptions for certain users in an organization</span></span>

<span data-ttu-id="843c1-157">Se quiser que certos grupos possam exibir URLs que podem ser bloqueadas para outras pessoas, você pode especificar uma política de links seguros de ATP que se aplica a destinatários específicos.</span><span class="sxs-lookup"><span data-stu-id="843c1-157">If you want certain groups to be able to view URLs that might be blocked for others, you can specify an ATP Safe Links policy that applies to specific recipients.</span></span> <span data-ttu-id="843c1-158">Confira [Configurar uma lista de URLs "não reconfigurar" personalizada usando os links seguros de ATP](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).</span><span class="sxs-lookup"><span data-stu-id="843c1-158">See [Set up a custom "do not rewrite" URLs list using ATP Safe Links](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).</span></span>
  


---
title: Configurar uma lista de URLs bloqueada personalizada usando o Office 365 ATP seguros Links
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 896a7efb-1683-465e-a394-261349e5d866
description: Leia este artigo para saber como configurar uma lista das URLs bloqueados para sua organização usando a proteção de ameaça avançadas do Office 365. As URLs bloqueadas serão aplicados a mensagens de email e documentos do Office de acordo com suas políticas de links seguros ATP.
ms.openlocfilehash: 36d295e6924d2e9972c185657885fa25bd96bf08
ms.sourcegitcommit: 7032830867eb3fc71760e04b8342aff174c5d757
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/01/2018
ms.locfileid: "25353247"
---
# <a name="set-up-a-custom-blocked-urls-list-using-office-365-atp-safe-links"></a><span data-ttu-id="98075-104">Configurar uma lista de URLs bloqueada personalizada usando o Office 365 ATP seguros Links</span><span class="sxs-lookup"><span data-stu-id="98075-104">Set up a custom blocked URLs list using Office 365 ATP Safe Links</span></span>

<span data-ttu-id="98075-p102">Com [A proteção de ameaça avançadas do Office 365](office-365-atp.md) (ATP), sua organização pode ter uma lista personalizada de endereços de site (URLs) que são bloqueados. Quando uma URL for bloqueada, as pessoas que clique nos links para a URL bloqueada são seguidas para uma [página de aviso](atp-safe-links-warning-pages.md) semelhante à seguinte imagem:</span><span class="sxs-lookup"><span data-stu-id="98075-p102">With [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP), your organization can have a custom list of website addresses (URLs) that are blocked. When a URL is blocked, people who click on links to the blocked URL are taken to a [warning page](atp-safe-links-warning-pages.md) that resembles the following image:</span></span> 
  
![Este site está bloqueado](media/6b4bda2d-a1e6-419e-8b10-588e83c3af3f.png)
  
<span data-ttu-id="98075-108">A lista de URLs bloqueada é definida pela equipe de segurança do Office 365 da sua organização e essa lista se aplica a todas as pessoas da organização que é coberto por políticas de vínculos do Office 365 ATP seguros.</span><span class="sxs-lookup"><span data-stu-id="98075-108">The blocked URLs list is defined by your organization's Office 365 security team, and that list applies to everyone in the organization who is covered by Office 365 ATP Safe Links policies.</span></span> 
  
<span data-ttu-id="98075-109">Leia este artigo para saber como configurar personalizada lista de URLs bloqueios da sua organização para [Links de ATP seguros no Office 365](atp-safe-links.md).</span><span class="sxs-lookup"><span data-stu-id="98075-109">Read this article to learn how to set up your organization's custom blocked URLs list for [ATP Safe Links in Office 365](atp-safe-links.md).</span></span>
  
## <a name="view-or-edit-a-custom-list-of-blocked-urls"></a><span data-ttu-id="98075-110">Exibir ou editar uma lista personalizada de URLs bloqueados</span><span class="sxs-lookup"><span data-stu-id="98075-110">View or edit a custom list of blocked URLs</span></span>

<span data-ttu-id="98075-p103">[Links de ATP seguros no Office 365](atp-safe-links.md) usa várias listas, incluindo personalizado bloqueada lista de URLs da sua organização. Se você tiver as permissões necessárias, você pode configurar a lista personalizada de sua organização. Você pode fazer isso editando a política de seguros Links padrão da sua organização.</span><span class="sxs-lookup"><span data-stu-id="98075-p103">[ATP Safe Links in Office 365](atp-safe-links.md) uses several lists, including your organization's custom blocked URLs list. If you have the necessary permissions, you can set up your organization's custom list. You do this by editing your organization's default Safe Links policy.</span></span>
  
1. <span data-ttu-id="98075-114">Vá para [https://protection.office.com](https://protection.office.com) e entre com sua conta do trabalho ou da escola.</span><span class="sxs-lookup"><span data-stu-id="98075-114">Go to [https://protection.office.com](https://protection.office.com) and sign in with your work or school account.</span></span> 
    
2. <span data-ttu-id="98075-115">No painel de navegação esquerdo, em **gerenciamento de ameaça**, escolha **política** \> **Links seguros**.</span><span class="sxs-lookup"><span data-stu-id="98075-115">In the left navigation, under **Threat management**, choose **Policy** \> **Safe Links**.</span></span>
    
3. <span data-ttu-id="98075-116">Na seção **políticas que se aplicam a toda a organização** , selecione **padrão**e, em seguida, escolha **Editar** (no botão Editar se parece com um lápis).</span><span class="sxs-lookup"><span data-stu-id="98075-116">In the **Policies that apply to the entire organization** section, select **Default**, and then choose **Edit** (the Edit button resembles a pencil).</span></span> 
    
    ![Clique em Editar para editar sua política padrão para a proteção de Links de seguros](media/d08f9615-d947-4033-813a-d310ec2c8cca.png)
  
    <span data-ttu-id="98075-p104">Isso é onde você vai para exibir sua lista de URLs bloqueados. Observe que, inicialmente, você não terá nenhum URL listado.</span><span class="sxs-lookup"><span data-stu-id="98075-p104">This is where you go to view your list of blocked URLs. Note that at first, you won't have any URLs listed.</span></span>
    
    ![A lista de URLs bloqueado é no padrão política de seguros Links que se aplica a toda sua organização.](media/575e1449-6191-40ac-b626-030a2fd3fb11.png)
  
4. <span data-ttu-id="98075-p105">Selecione caixa **Digite uma URL válida** e, em seguida, digite uma URL e clique no sinal de adição (+). Aqui estão algumas coisas em mente:</span><span class="sxs-lookup"><span data-stu-id="98075-p105">Select the **Enter a valid URL** box, and then type a URL, and then choose the plus sign (+). Here are a few things to keep in mind:</span></span> 
    
  - <span data-ttu-id="98075-p106">Você pode especificar uma URL de domínio somente (como `contoso.com` ou `tailspintoys.com`). Isso irá bloquear cliques em qualquer URL que contém o domínio.</span><span class="sxs-lookup"><span data-stu-id="98075-p106">You can specify a domain-only URL (like `contoso.com` or `tailspintoys.com`). This will block clicks on any URL that contains the domain.</span></span>
    
  - <span data-ttu-id="98075-p107">Não inclua uma barra invertida ( **/**) no final da URL. Por exemplo, em vez de inserir `http://www.contoso.com/`, insira `http://www.contoso.com`.</span><span class="sxs-lookup"><span data-stu-id="98075-p107">Do not include a forward slash ( **/**) at the end of the URL. For example, instead of entering `http://www.contoso.com/`, enter `http://www.contoso.com`.</span></span>
    
  - <span data-ttu-id="98075-p108">Você pode incluir até três asteriscos de caractere curinga (\*) por URL. A tabela a seguir lista alguns exemplos de como você pode inserir e o que essas entradas de efeito tem.</span><span class="sxs-lookup"><span data-stu-id="98075-p108">You can include up to three wildcard asterisks (\*) per URL. The following table lists some examples of what you can enter and what effect those entries have.</span></span>
    
|<span data-ttu-id="98075-129">**Entrada de exemplo**</span><span class="sxs-lookup"><span data-stu-id="98075-129">**Example Entry**</span></span>|<span data-ttu-id="98075-130">**O que ele faz**</span><span class="sxs-lookup"><span data-stu-id="98075-130">**What It Does**</span></span>|
|:-----|:-----|
|<span data-ttu-id="98075-131">`contoso.com`ou`*contoso.com*`</span><span class="sxs-lookup"><span data-stu-id="98075-131">`contoso.com` or `*contoso.com*`</span></span>  <br/> |<span data-ttu-id="98075-132">Bloqueia o domínio, subdomínios e caminhos, tais como `https://www.contoso.com`, `http://sub.contoso.com`, e`http://contoso.com/abc`</span><span class="sxs-lookup"><span data-stu-id="98075-132">Blocks the domain, subdomains, and paths, such as `https://www.contoso.com`, `http://sub.contoso.com`, and `http://contoso.com/abc`</span></span>  <br/> |
|`http://contoso.com/a`  <br/> |<span data-ttu-id="98075-133">Bloqueia um site `http://contoso.com/a` mas subcaminhos não adicionais, como`http://contoso.com/a/b`</span><span class="sxs-lookup"><span data-stu-id="98075-133">Blocks a site `http://contoso.com/a` but not additional subpaths like `http://contoso.com/a/b`</span></span>  <br/> |
|`http://contoso.com/a*`  <br/> |<span data-ttu-id="98075-134">Bloqueia um site `http://contoso.com/a` e subcaminhos adicionais, como`http://contoso.com/a/b`</span><span class="sxs-lookup"><span data-stu-id="98075-134">Blocks a site `http://contoso.com/a` and additional subpaths like `http://contoso.com/a/b`</span></span>  <br/> |
   
5. <span data-ttu-id="98075-135">Quando terminar de adicionar URLs, no canto inferior direito da tela, escolha **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="98075-135">When you are finished adding URLs, in the lower right corner of the screen, choose **Save**.</span></span>
    
## <a name="what-if-i-want-to-define-exceptions-for-certain-users-in-my-organization"></a><span data-ttu-id="98075-136">O que ocorre se eu quiser definir exceções para determinados usuários na minha organização?</span><span class="sxs-lookup"><span data-stu-id="98075-136">What if I want to define exceptions for certain users in my organization?</span></span>

<span data-ttu-id="98075-p109">Se você quiser determinados grupos possam exibir URLs que poderá ser bloqueadas para outras pessoas, você pode especificar uma política de Links de seguros ATP que se aplica a destinatários específicos. Consulte [Configurar uma lista de URLs "não regravação" personalizada usando Links de ATP seguros](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).</span><span class="sxs-lookup"><span data-stu-id="98075-p109">If you want certain groups to be able to view URLs that might be blocked for others, you can specify an ATP Safe Links policy that applies to specific recipients. See [Set up a custom "do not rewrite" URLs list using ATP Safe Links](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="98075-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="98075-139">Related topics</span></span>

<span data-ttu-id="98075-140">[Proteção Avançada contra Ameaças do Office 365](office-365-atp.md) </span><span class="sxs-lookup"><span data-stu-id="98075-140">[Office 365 Advanced Threat Protection](office-365-atp.md)</span></span>
  
[<span data-ttu-id="98075-141">Links de ATP seguros no Office 365</span><span class="sxs-lookup"><span data-stu-id="98075-141">ATP Safe Links in Office 365</span></span>](atp-safe-links.md)
  
[<span data-ttu-id="98075-142">Configurar políticas de Links de ATP seguros no Office 365</span><span class="sxs-lookup"><span data-stu-id="98075-142">Set up ATP Safe Links policies in Office 365</span></span>](set-up-atp-safe-links-policies.md)
  
[<span data-ttu-id="98075-143">Anexos de ATP seguros no Office 365</span><span class="sxs-lookup"><span data-stu-id="98075-143">ATP Safe Attachments in Office 365</span></span>](atp-safe-attachments.md)

[<span data-ttu-id="98075-144">Permissões de segurança do Office 365 &amp; Centro de conformidade</span><span class="sxs-lookup"><span data-stu-id="98075-144">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
  


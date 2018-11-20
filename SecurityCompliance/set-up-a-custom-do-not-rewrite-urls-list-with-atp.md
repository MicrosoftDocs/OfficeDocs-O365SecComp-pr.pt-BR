---
title: Configurar uma lista de URLs execute-não-reconfiguração personalizada usando o Office 365 ATP seguros Links
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
ms.assetid: 35dbfd99-da5a-422b-9b0e-c6caf3b645fa
description: Ao configurar suas políticas de links seguros ATP, você pode incluir reconfiguração execute-não é ' lista de URLs para permitir que algumas pessoas na sua organização visitar sites que você pode incluir em sua lista.
ms.openlocfilehash: c954c12785659f9c025046bf3773cfec2d5dd5f9
ms.sourcegitcommit: 147768bbe44c8c98c02fa29ae9d882cee4ec2d6b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/09/2018
ms.locfileid: "26238383"
---
# <a name="set-up-a-custom-do-not-rewrite-urls-list-using-office-365-atp-safe-links"></a><span data-ttu-id="598c5-103">Configurar uma lista de URLs execute-não-reconfiguração personalizada usando o Office 365 ATP seguros Links</span><span class="sxs-lookup"><span data-stu-id="598c5-103">Set up a custom do-not-rewrite URLs list using Office 365 ATP Safe Links</span></span>

<span data-ttu-id="598c5-p101">Com [A proteção de ameaça avançadas do Office 365](office-365-atp.md) (ATP), sua organização pode ter um [URLs bloqueados personalizados](set-up-a-custom-blocked-urls-list-wtih-atp.md), de forma que, quando as pessoas clicarem na web endereços (URLs) em mensagens de email ou certos documentos do Office, eles são impedidos de pretende dessas URLs. Sua organização também pode ter listas personalizadas "não regravação" para grupos específicos na sua organização. Uma lista de "não regravação" permite que algumas pessoas visite URLs que são bloqueados contrário por [Links de ATP seguros no Office 365](atp-safe-links.md).</span><span class="sxs-lookup"><span data-stu-id="598c5-p101">With [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP), your organization can have a [custom blocked URLs](set-up-a-custom-blocked-urls-list-wtih-atp.md), such that when people click on web addresses (URLs) in email messages or certain Office documents, they are prevented from going to those URLs. Your organization can also have custom "do not rewrite" lists for specific groups in your organization. A "do not rewrite" list enables some people to visit URLs that are otherwise blocked by [ATP Safe Links in Office 365](atp-safe-links.md).</span></span> 
  
<span data-ttu-id="598c5-107">Este artigo descreve como especificar uma lista das URLs que são excluídos da verificação de Links de ATP seguros e alguns pontos importantes a serem tenha em mente.</span><span class="sxs-lookup"><span data-stu-id="598c5-107">This article describes how to specify a list of URLs that are excluded from ATP Safe Links scanning, and a few important points to keep in mind.</span></span>

## <a name="set-up-a-do-not-rewrite-list"></a><span data-ttu-id="598c5-108">Configurar uma lista de "não regravação"</span><span class="sxs-lookup"><span data-stu-id="598c5-108">Set up a "do not rewrite" list</span></span>

<span data-ttu-id="598c5-p102">Proteção de Links de seguros ATP usa várias listas, incluindo a lista de URLs bloqueios da sua organização e as listas de "não regravação" para exceções. Se você tiver as permissões necessárias, você pode configurar suas listas de "não regravação" personalizado. Você fazer isso quando você adicionar ou editar políticas de seguros Links que se aplicam a destinatários específicos na sua organização.</span><span class="sxs-lookup"><span data-stu-id="598c5-p102">ATP Safe Links protection uses several lists, including your organization's blocked URLs list and the "do not rewrite" lists for exceptions. If you have the necessary permissions, you can set up your custom "do not rewrite" lists. You do this when you add or edit Safe Links policies that apply to specific recipients in your organization.</span></span> 
  
1. <span data-ttu-id="598c5-112">Vá para [https://protection.office.com](https://protection.office.com) e entre com sua conta do trabalho ou da escola.</span><span class="sxs-lookup"><span data-stu-id="598c5-112">Go to [https://protection.office.com](https://protection.office.com) and sign in with your work or school account.</span></span> 
    
2. <span data-ttu-id="598c5-113">No painel de navegação esquerdo, em **gerenciamento de ameaça** \> **política** \> **Links seguros**.</span><span class="sxs-lookup"><span data-stu-id="598c5-113">In the left navigation, under **Threat management** \> **Policy** \> **Safe Links**.</span></span>
    
3. <span data-ttu-id="598c5-p103">Na seção **políticas que se aplicam a destinatários específicos** , escolha **novo** (botão novo se parece com um sinal de adição ( **+**)) para criar uma nova política. (Como alternativa, você pode editar uma política existente).</span><span class="sxs-lookup"><span data-stu-id="598c5-p103">In the **Policies that apply to specific recipients** section, choose **New** (the New button resembles a plus sign ( **+**)) to create a new policy. (Alternatively, you can edit an existing policy.)</span></span>
    
    ![Escolha Novo para adicionar uma diretiva de segurança Links para os destinatários de email específicos](media/01073f42-3cec-4ddb-8c10-4d33ec434676.png)
  
4. <span data-ttu-id="598c5-117">Especifique um nome e descrição para a diretiva.</span><span class="sxs-lookup"><span data-stu-id="598c5-117">Specify a name and description for your policy.</span></span>
    
5. <span data-ttu-id="598c5-118">Na seção **não reescrever as seguintes URLs** , marque a caixa **Digite uma URL válida** , digite uma URL e clique no sinal de adição (+).</span><span class="sxs-lookup"><span data-stu-id="598c5-118">In the **Do not rewrite the following URLs** section, select the **Enter a valid URL** box, and then type a URL, and then choose the plus sign (+).</span></span> 
    
6. <span data-ttu-id="598c5-p104">Na seção **Aplicada** , escolha **o destinatário é um membro da**e escolha o grupo (s) que você deseja incluir na sua política. Escolha **Adicionar**e escolha **Okey**.</span><span class="sxs-lookup"><span data-stu-id="598c5-p104">In the **Applied To** section, choose **The recipient is a member of**, and then choose the group(s) you want to include in your policy. Choose **Add**, and then choose **OK**.</span></span>
    
7. <span data-ttu-id="598c5-121">Quando terminar de adicionar URLs, no canto inferior direito da tela, escolha **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="598c5-121">When you are finished adding URLs, in the lower right corner of the screen, choose **Save**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="598c5-p105">Certifique-se de revisar a lista de bloqueados URLs personalizada da sua organização. Consulte [Configurar uma lista de URLs bloqueada personalizada usando Links de ATP seguros](set-up-a-custom-blocked-urls-list-wtih-atp.md).</span><span class="sxs-lookup"><span data-stu-id="598c5-p105">Make sure to review your organization's custom list of blocked URLs. See [Set up a custom blocked URLs list using ATP Safe Links](set-up-a-custom-blocked-urls-list-wtih-atp.md).</span></span> 
  
## <a name="important-points-to-keep-in-mind"></a><span data-ttu-id="598c5-124">Pontos importantes a serem tenha em mente</span><span class="sxs-lookup"><span data-stu-id="598c5-124">Important points to keep in mind</span></span>

- <span data-ttu-id="598c5-125">Nenhum URL que você especificar na lista "não regravação" é excluída dos Links de seguros ATP varredura para os destinatários que você especificar.</span><span class="sxs-lookup"><span data-stu-id="598c5-125">Any URLs that you specify in the "do not rewrite" list are excluded from ATP Safe Links scanning for the recipients that you specify.</span></span>
 
- <span data-ttu-id="598c5-p106">Quando você especifica uma lista de "não regravação" para uma política de ATP Links de seguros, você pode incluir até três asteriscos de caractere curinga (\*). Caracteres curinga (\*) são considerados como entradas de `contoso.com`, que não explicitamente incluir prefixos ou subdomínios, como `http://` ou `https://`. Isso significa que uma entrada, tais como `contoso.com` é semelhante ao `*contoso.com*` para sua lista de "não regravação".</span><span class="sxs-lookup"><span data-stu-id="598c5-p106">When you specify a "do not rewrite" list for an ATP Safe Links policy, you can include up to three wildcard asterisks (\*). Wildcards (\*) are assumed for entries such as `contoso.com`, which do not explicitly include prefixes or subdomains, like `http://` or `https://`. This means an entry, such as `contoso.com` is similar to `*contoso.com*` for your "do not rewrite" list.</span></span>

- <span data-ttu-id="598c5-p107">Se você já tiver uma lista das URLs em sua lista de "não regravação", certifique-se revisar essa lista e adicionar caracteres curinga, conforme apropriado. Por exemplo, se sua lista existente tiver uma entrada como `http://contoso.com/a` e você deseja incluir subcaminhos como `http://contoso.com/a/b` em sua política, adicione um caractere curinga para a entrada para que ele se parece com `http://contoso.com/a*`.</span><span class="sxs-lookup"><span data-stu-id="598c5-p107">If you already have a list of URLs in your "do not rewrite" list, make sure to review that list and add wildcards as appropriate. For example, if your existing list has an entry like `http://contoso.com/a` and you want to include subpaths like `http://contoso.com/a/b` in your policy, add a wildcard to your entry so it looks like `http://contoso.com/a*`.</span></span>
    
- <span data-ttu-id="598c5-p108">Não inclua uma barra (/) nas URLs que você especificar em sua lista de "não regravação". Por exemplo, em vez de inserir `contoso.com/` na sua lista de "não regravação", digite `contoso.com`.</span><span class="sxs-lookup"><span data-stu-id="598c5-p108">Do not include a forward slash (/) in the URLs that you specify in your "do not rewrite" list. For example, rather than enter `contoso.com/` in your "do not rewrite" list, enter `contoso.com`.</span></span>
    
<span data-ttu-id="598c5-133">Os seguintes exemplos de listas de tabela de que você pode digitar e o que essas entradas de efeito tem.</span><span class="sxs-lookup"><span data-stu-id="598c5-133">The following table lists examples of what you can enter and what effect those entries have.</span></span>
    
|<span data-ttu-id="598c5-134">**Entrada de exemplo**</span><span class="sxs-lookup"><span data-stu-id="598c5-134">**Example Entry**</span></span>|<span data-ttu-id="598c5-135">**O que ele faz**</span><span class="sxs-lookup"><span data-stu-id="598c5-135">**What It Does**</span></span>|
|:-----|:-----|
|`*contoso.com*`  <br/> |<span data-ttu-id="598c5-136">Permite que os destinatários específicos a visitar um domínio, subdomínios e caminhos, tais como `http://www.contoso.com`, `https://www.contoso.com`, `https://maps.contoso.com`, ou`http://www.contoso.com/a`</span><span class="sxs-lookup"><span data-stu-id="598c5-136">Allows specific recipients to visit a domain, subdomains, and paths, such as `http://www.contoso.com`, `https://www.contoso.com`, `https://maps.contoso.com`, or `http://www.contoso.com/a`</span></span>  <br/> |
|`http://contoso.com/a`  <br/> |<span data-ttu-id="598c5-137">Permite que os destinatários específicos visitar um site como `http://contoso.com/a`, mas não subcaminhos, como`http://contoso.com/a/b`</span><span class="sxs-lookup"><span data-stu-id="598c5-137">Allows specific recipients to visit a site like `http://contoso.com/a`, but not subpaths like `http://contoso.com/a/b`</span></span>  <br/> |
|`http://contoso.com/a*`  <br/> |<span data-ttu-id="598c5-138">Permite que os destinatários específicos visitar um site como `http://contoso.com/a` e subcaminhos like`http://contoso.com/a/b`</span><span class="sxs-lookup"><span data-stu-id="598c5-138">Allows specific recipients to visit a site like `http://contoso.com/a` and subpaths like `http://contoso.com/a/b`</span></span>  <br/> |
   
 
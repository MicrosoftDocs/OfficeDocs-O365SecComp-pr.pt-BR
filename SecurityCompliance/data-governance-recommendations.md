---
title: Como o conteúdo é identificado para recomendações de governança de dados
ms.author: brendonb
author: stephow-MSFT
manager: laurawi
ms.date: 1/15/2019
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Priority
search.appverid:
- MOE150
- MET150
ROBOTS: NOINDEX, NOFOLLOW
description: O Centro de Segurança e Conformidade do Office 365 fornece recomendações para governança de dados com base na configuração atual da sua organização e permite que você configure as coisas com apenas alguns cliques. Algumas dessas recomendações detectam conteúdo específico em sua organização e, em seguida, fornecem etapas recomendadas para gerenciar esse conteúdo. Por exemplo, uma recomendação pode detectar itens que contenham conteúdo essencial para os negócios (como privilégio advogado-cliente ou informações do NDA) e permitir que você aplique automaticamente um rótulo de retenção a esses itens para garantir que eles sejam classificados e retidos conforme necessário. Este tópico lista as recomendações de controle de dados que você pode ver e descreve qual conteúdo é detectado para acionar cada um deles.
ms.openlocfilehash: a3f803105ea5c2626c8c2a26ad898df5f45af2f0
ms.sourcegitcommit: c7737903ff2e1d047682ee61f7ac21b0bdd1c6fd
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/16/2019
ms.locfileid: "28263934"
---
# <a name="how-content-is-identified-for-data-governance-recommendations"></a><span data-ttu-id="14670-106">Como o conteúdo é identificado para recomendações de governança de dados</span><span class="sxs-lookup"><span data-stu-id="14670-106">How content is identified for data-governance recommendations</span></span>

<span data-ttu-id="14670-p102">O Centro de Segurança e Conformidade do Office 365 fornece recomendações para governança de dados com base na configuração atual da sua organização e permite que você configure as coisas com apenas alguns cliques. Algumas dessas recomendações detectam conteúdo específico em sua organização e, em seguida, fornecem etapas recomendadas para gerenciar esse conteúdo. Por exemplo, uma recomendação pode detectar itens que contenham conteúdo essencial para os negócios (como privilégio advogado-cliente ou informações do NDA) e permitir que você aplique automaticamente um rótulo de retenção a esses itens para garantir que eles sejam classificados e retidos conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="14670-p102">The Office 365 Security & Compliance Center provides recommendations for data governance based on your org's current setup and lets you set things up in a couple clicks. Some of these recommendations detect specific content in your organization and then provide recommended steps for managing that content. For example, a recommendation might detect items that contain business-critical content (such as attorney-client privilege or NDA info), and then let you automatically apply a retention label to those items to ensure that they’re classified and retained as needed.</span></span>

<span data-ttu-id="14670-110">Este tópico lista as recomendações de controle de dados que você pode ver e descreve qual conteúdo é detectado para acionar cada um deles.</span><span class="sxs-lookup"><span data-stu-id="14670-110">This topic lists the data-governance recommendations you might see and describes what content is detected to trigger each one.</span></span>

## <a name="clean-up-voicemail"></a><span data-ttu-id="14670-111">Limpar a caixa postal</span><span class="sxs-lookup"><span data-stu-id="14670-111">Clean up voicemail</span></span>

<span data-ttu-id="14670-p103">Essa recomendação é exibida quando as mensagens de e-mail identificadas como o tipo de mensagem "correio de voz" são detectadas nas caixas de correio dos usuários. Saiba mais sobre em [propriedades de mensagem do Exchange](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/ediscovery/message-properties-and-search-operators?view=exchserver-2019#searchable-properties-in-exchange).</span><span class="sxs-lookup"><span data-stu-id="14670-p103">This recommendation appears when email messages identified as the message type ‘voicemail’ are detected in users’ mailboxes. Learn more about [message properties in Exchange](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/ediscovery/message-properties-and-search-operators?view=exchserver-2019#searchable-properties-in-exchange).</span></span>

## <a name="label-attorney-client-privilege-content"></a><span data-ttu-id="14670-114">Etiquetar conteúdo de privilégio advogado-cliente</span><span class="sxs-lookup"><span data-stu-id="14670-114">Label attorney-client privilege content</span></span> 

<span data-ttu-id="14670-115">Este recomendação é exibida quando os seguintes critérios são atendidos.</span><span class="sxs-lookup"><span data-stu-id="14670-115">This recommendation appears when either of the following criteria are met.</span></span>

- <span data-ttu-id="14670-116">Qualquer combinação dessas palavras-chave for detectada no corpo da mensagem de email:</span><span class="sxs-lookup"><span data-stu-id="14670-116">Any of combination of these keywords is detected in the body of an email message:</span></span>
    - <span data-ttu-id="14670-117">ACP</span><span class="sxs-lookup"><span data-stu-id="14670-117">ACP</span></span>
    - <span data-ttu-id="14670-118">Privilégio advogado cliente</span><span class="sxs-lookup"><span data-stu-id="14670-118">Attorney Client Privilege</span></span>
    - <span data-ttu-id="14670-119">Privilégio advogado-cliente</span><span class="sxs-lookup"><span data-stu-id="14670-119">Attorney-Client Privilege</span></span>
    - <span data-ttu-id="14670-120">Advogado-cliente privilegiados</span><span class="sxs-lookup"><span data-stu-id="14670-120">Attorney-Client Privileged</span></span>

- <span data-ttu-id="14670-121">Qualquer combinação dessas palavras-chave é detectada em arquivos do SharePoint ou no OneDrive:</span><span class="sxs-lookup"><span data-stu-id="14670-121">Any combination of these keywords are detected in SharePoint or OneDrive files:</span></span>
    - <span data-ttu-id="14670-122">ACP</span><span class="sxs-lookup"><span data-stu-id="14670-122">ACP</span></span>
    - <span data-ttu-id="14670-123">Advogado cliente privilégio \*</span><span class="sxs-lookup"><span data-stu-id="14670-123">Attorney Client Privilege\*</span></span>
    - <span data-ttu-id="14670-124">Privilégio AC</span><span class="sxs-lookup"><span data-stu-id="14670-124">AC Privilege</span></span>

## <a name="retain-audio-files"></a><span data-ttu-id="14670-125">Manter os arquivos de áudio</span><span class="sxs-lookup"><span data-stu-id="14670-125">Retain audio files</span></span>

<span data-ttu-id="14670-126">Este recomendação é exibida quando qualquer um dos seguintes tipos de arquivo é detectado no SharePoint ou OneDrive.</span><span class="sxs-lookup"><span data-stu-id="14670-126">This recommendation appears when any of the following file types are detected in SharePoint or OneDrive.</span></span>

- <span data-ttu-id="14670-127">.MP3</span><span class="sxs-lookup"><span data-stu-id="14670-127">MP3 (default)</span></span>
- <span data-ttu-id="14670-128">.WMA</span><span class="sxs-lookup"><span data-stu-id="14670-128">WMA</span></span>
- <span data-ttu-id="14670-129">.WAV</span><span class="sxs-lookup"><span data-stu-id="14670-129">WAV</span></span>
- <span data-ttu-id="14670-130">.RA</span><span class="sxs-lookup"><span data-stu-id="14670-130">.RA</span></span>
- <span data-ttu-id="14670-131">.RAM</span><span class="sxs-lookup"><span data-stu-id="14670-131">RAM</span></span>
- <span data-ttu-id="14670-132">.RM</span><span class="sxs-lookup"><span data-stu-id="14670-132">rm</span></span>
- <span data-ttu-id="14670-133">.MID</span><span class="sxs-lookup"><span data-stu-id="14670-133">.MID</span></span>
- <span data-ttu-id="14670-134">.OGG</span><span class="sxs-lookup"><span data-stu-id="14670-134">.OGG</span></span>
- <span data-ttu-id="14670-135">.AIFF</span><span class="sxs-lookup"><span data-stu-id="14670-135">.AIFF</span></span>
- <span data-ttu-id="14670-136">.PCM</span><span class="sxs-lookup"><span data-stu-id="14670-136">.PCM</span></span>
- <span data-ttu-id="14670-137">.AAC</span><span class="sxs-lookup"><span data-stu-id="14670-137">.AAC</span></span>
- <span data-ttu-id="14670-138">.FLAC</span><span class="sxs-lookup"><span data-stu-id="14670-138">.FLAC</span></span>
- <span data-ttu-id="14670-139">.ALAC</span><span class="sxs-lookup"><span data-stu-id="14670-139">.ALAC</span></span>

## <a name="retain-cad-files"></a><span data-ttu-id="14670-140">Manter os arquivos do CAD</span><span class="sxs-lookup"><span data-stu-id="14670-140">Retain CAD files</span></span>

<span data-ttu-id="14670-141">Este recomendação é exibida quando qualquer um dos seguintes tipos de arquivo é detectado no SharePoint ou OneDrive.</span><span class="sxs-lookup"><span data-stu-id="14670-141">This recommendation appears when any of the following file types are detected in SharePoint or OneDrive.</span></span>

- <span data-ttu-id="14670-142">.3DXML</span><span class="sxs-lookup"><span data-stu-id="14670-142">.3DXML</span></span>
- <span data-ttu-id="14670-143">.ACIS</span><span class="sxs-lookup"><span data-stu-id="14670-143">.ACIS</span></span>
- <span data-ttu-id="14670-144">.ARC</span><span class="sxs-lookup"><span data-stu-id="14670-144">ARC
</span></span>
- <span data-ttu-id="14670-145">.ASM</span><span class="sxs-lookup"><span data-stu-id="14670-145">asm</span></span>
- <span data-ttu-id="14670-146">.CAT\*</span><span class="sxs-lookup"><span data-stu-id="14670-146">cat\*</span></span>
- <span data-ttu-id="14670-147">.CGR</span><span class="sxs-lookup"><span data-stu-id="14670-147">.CGR</span></span>
- <span data-ttu-id="14670-148">.DW</span><span class="sxs-lookup"><span data-stu-id="14670-148">DW</span></span>
- <span data-ttu-id="14670-149">.DX</span><span class="sxs-lookup"><span data-stu-id="14670-149">Dx</span></span>
- <span data-ttu-id="14670-150">.EDRW</span><span class="sxs-lookup"><span data-stu-id="14670-150">.EDRW</span></span>
- <span data-ttu-id="14670-151">.IAM</span><span class="sxs-lookup"><span data-stu-id="14670-151">.IAM</span></span>
- <span data-ttu-id="14670-152">.IGES</span><span class="sxs-lookup"><span data-stu-id="14670-152">.IGES</span></span>
- <span data-ttu-id="14670-153">.IGS</span><span class="sxs-lookup"><span data-stu-id="14670-153">.IGS</span></span>
- <span data-ttu-id="14670-154">.IPT</span><span class="sxs-lookup"><span data-stu-id="14670-154">.IPT</span></span>
- <span data-ttu-id="14670-155">.JT</span><span class="sxs-lookup"><span data-stu-id="14670-155">.JT</span></span>
- <span data-ttu-id="14670-156">.MF1</span><span class="sxs-lookup"><span data-stu-id="14670-156">.MF1</span></span>
- <span data-ttu-id="14670-157">.NEU</span><span class="sxs-lookup"><span data-stu-id="14670-157">.NEU</span></span>
- <span data-ttu-id="14670-158">.NOMINAL</span><span class="sxs-lookup"><span data-stu-id="14670-158">.PAR</span></span>
- <span data-ttu-id="14670-159">.PKG</span><span class="sxs-lookup"><span data-stu-id="14670-159">.PKG</span></span>
- <span data-ttu-id="14670-160">.PRC</span><span class="sxs-lookup"><span data-stu-id="14670-160">PRC
</span></span>
- <span data-ttu-id="14670-161">.PRT</span><span class="sxs-lookup"><span data-stu-id="14670-161">.PRT</span></span>
- <span data-ttu-id="14670-162">.PSM</span><span class="sxs-lookup"><span data-stu-id="14670-162">.PSM</span></span>
- <span data-ttu-id="14670-163">.PWD</span><span class="sxs-lookup"><span data-stu-id="14670-163">.PWD</span></span>
- <span data-ttu-id="14670-164">.SLD\*</span><span class="sxs-lookup"><span data-stu-id="14670-164">.SLD\*</span></span>
- <span data-ttu-id="14670-165">.STEP</span><span class="sxs-lookup"><span data-stu-id="14670-165">Step</span></span>
- <span data-ttu-id="14670-166">.STL</span><span class="sxs-lookup"><span data-stu-id="14670-166">.STL</span></span>
- <span data-ttu-id="14670-167">.STP</span><span class="sxs-lookup"><span data-stu-id="14670-167">.STP</span></span>
- <span data-ttu-id="14670-168">.U3D</span><span class="sxs-lookup"><span data-stu-id="14670-168">.U3D</span></span>
- <span data-ttu-id="14670-169">.UNV</span><span class="sxs-lookup"><span data-stu-id="14670-169">.UNV</span></span>
- <span data-ttu-id="14670-170">.VRML</span><span class="sxs-lookup"><span data-stu-id="14670-170">.VRML</span></span>
- <span data-ttu-id="14670-171">.WRL</span><span class="sxs-lookup"><span data-stu-id="14670-171">.WRL</span></span>
- <span data-ttu-id="14670-172">.X_\*</span><span class="sxs-lookup"><span data-stu-id="14670-172">X</span></span>
- <span data-ttu-id="14670-173">.XAS</span><span class="sxs-lookup"><span data-stu-id="14670-173">.XAS</span></span>
- <span data-ttu-id="14670-174">.XMT\*</span><span class="sxs-lookup"><span data-stu-id="14670-174">.XMT\*</span></span>
- <span data-ttu-id="14670-175">.XPR</span><span class="sxs-lookup"><span data-stu-id="14670-175">.XPR</span></span>

## <a name="retain-image-files"></a><span data-ttu-id="14670-176">Manter os arquivos de imagem</span><span class="sxs-lookup"><span data-stu-id="14670-176">Retain image files</span></span>

<span data-ttu-id="14670-177">Este recomendação é exibida quando qualquer um dos seguintes tipos de arquivo é detectado no SharePoint ou OneDrive.</span><span class="sxs-lookup"><span data-stu-id="14670-177">This recommendation appears when any of the following file types are detected in SharePoint or OneDrive.</span></span>

- <span data-ttu-id="14670-178">.JPEG</span><span class="sxs-lookup"><span data-stu-id="14670-178">JPEG</span></span>
- <span data-ttu-id="14670-179">.GIF</span><span class="sxs-lookup"><span data-stu-id="14670-179">GIF</span></span>
- <span data-ttu-id="14670-180">.TIF\*</span><span class="sxs-lookup"><span data-stu-id="14670-180">tif</span></span>
- <span data-ttu-id="14670-181">.BMP</span><span class="sxs-lookup"><span data-stu-id="14670-181">.bmp</span></span>
- <span data-ttu-id="14670-182">.PNG</span><span class="sxs-lookup"><span data-stu-id="14670-182">PNG</span></span>
- <span data-ttu-id="14670-183">.RAW</span><span class="sxs-lookup"><span data-stu-id="14670-183">.RAW</span></span>
- <span data-ttu-id="14670-184">.PSD</span><span class="sxs-lookup"><span data-stu-id="14670-184">.PSD</span></span>
- <span data-ttu-id="14670-185">.PSP</span><span class="sxs-lookup"><span data-stu-id="14670-185">PSP
</span></span>
- <span data-ttu-id="14670-186">.JPG</span><span class="sxs-lookup"><span data-stu-id="14670-186">.jpg</span></span>
- <span data-ttu-id="14670-187">.EXIF</span><span class="sxs-lookup"><span data-stu-id="14670-187">.EXIF</span></span>
- <span data-ttu-id="14670-188">.PPM</span><span class="sxs-lookup"><span data-stu-id="14670-188">PPM capabilities</span></span>
- <span data-ttu-id="14670-189">.PGM</span><span class="sxs-lookup"><span data-stu-id="14670-189">.PGM</span></span>
- <span data-ttu-id="14670-190">.PBM</span><span class="sxs-lookup"><span data-stu-id="14670-190">.PBM</span></span>
- <span data-ttu-id="14670-191">.PNM</span><span class="sxs-lookup"><span data-stu-id="14670-191">.PNM</span></span>
- <span data-ttu-id="14670-192">.WEBP</span><span class="sxs-lookup"><span data-stu-id="14670-192">.WEBP</span></span>

## <a name="retain-nda-content"></a><span data-ttu-id="14670-193">Reter o conteúdo NDA</span><span class="sxs-lookup"><span data-stu-id="14670-193">Retain NDA content</span></span> 

<span data-ttu-id="14670-194">Este recomendação é exibida quando os seguintes critérios são atendidos.</span><span class="sxs-lookup"><span data-stu-id="14670-194">This recommendation appears when either of the following criteria are met.</span></span>

- <span data-ttu-id="14670-195">Qualquer combinação dessas palavras-chave for detectada no corpo da mensagem de email:</span><span class="sxs-lookup"><span data-stu-id="14670-195">Any of combination of these keywords is detected in the body of an email message:</span></span>
    - <span data-ttu-id="14670-196">NDA</span><span class="sxs-lookup"><span data-stu-id="14670-196">NDA</span></span>
    - <span data-ttu-id="14670-197">"Contrato de não-divulgação"</span><span class="sxs-lookup"><span data-stu-id="14670-197">“Non-Disclosure Agreement”</span></span>
    - <span data-ttu-id="14670-198">"Contrato de não divulgação"</span><span class="sxs-lookup"><span data-stu-id="14670-198">“Non Disclosure Agreement”</span></span>

- <span data-ttu-id="14670-199">Qualquer combinação dessas palavras-chave é detectada em arquivos .PDF ou .DOC no SharePoint ou no OneDrive:</span><span class="sxs-lookup"><span data-stu-id="14670-199">Any combination of these keywords are detected in .PDF or .DOC files in SharePoint or OneDrive:</span></span>
    - <span data-ttu-id="14670-200">NDA</span><span class="sxs-lookup"><span data-stu-id="14670-200">NDA</span></span>
    - <span data-ttu-id="14670-201">Contrato de não divulgação</span><span class="sxs-lookup"><span data-stu-id="14670-201">Non Disclosure Agreement</span></span>

## <a name="retain-software-development-files"></a><span data-ttu-id="14670-202">Manter os arquivos de desenvolvimento de software</span><span class="sxs-lookup"><span data-stu-id="14670-202">Retain software development files</span></span>

<span data-ttu-id="14670-203">Este recomendação é exibida quando qualquer um dos seguintes tipos de arquivo é detectado no SharePoint ou OneDrive.</span><span class="sxs-lookup"><span data-stu-id="14670-203">This recommendation appears when any of the following file types are detected in SharePoint or OneDrive.</span></span>

- <span data-ttu-id="14670-204">.ASAX</span><span class="sxs-lookup"><span data-stu-id="14670-204">.ASAX</span></span>
- <span data-ttu-id="14670-205">.ASM</span><span class="sxs-lookup"><span data-stu-id="14670-205">asm</span></span>
- <span data-ttu-id="14670-206">.ASP\*</span><span class="sxs-lookup"><span data-stu-id="14670-206">asp</span></span>
- <span data-ttu-id="14670-207">.BAT</span><span class="sxs-lookup"><span data-stu-id="14670-207">bat</span></span>
- <span data-ttu-id="14670-208">.CONFIG</span><span class="sxs-lookup"><span data-stu-id="14670-208">.config</span></span>
- <span data-ttu-id="14670-209">.CS</span><span class="sxs-lookup"><span data-stu-id="14670-209">cs</span></span>
- <span data-ttu-id="14670-210">.CSS</span><span class="sxs-lookup"><span data-stu-id="14670-210">CSS</span></span>
- <span data-ttu-id="14670-211">.DISCO</span><span class="sxs-lookup"><span data-stu-id="14670-211">.DISCO</span></span>
- <span data-ttu-id="14670-212">.HTM\*</span><span class="sxs-lookup"><span data-stu-id="14670-212">htm</span></span>
- <span data-ttu-id="14670-213">.INC</span><span class="sxs-lookup"><span data-stu-id="14670-213">.INC</span></span>
- <span data-ttu-id="14670-214">.JAD</span><span class="sxs-lookup"><span data-stu-id="14670-214">.JAD</span></span>
- <span data-ttu-id="14670-215">.JAVA</span><span class="sxs-lookup"><span data-stu-id="14670-215">Java</span></span>
- <span data-ttu-id="14670-216">.JS\*</span><span class="sxs-lookup"><span data-stu-id="14670-216">.js</span></span>
- <span data-ttu-id="14670-217">.LIB</span><span class="sxs-lookup"><span data-stu-id="14670-217">.LIB</span></span>
- <span data-ttu-id="14670-218">.O</span><span class="sxs-lookup"><span data-stu-id="14670-218">O</span></span>
- <span data-ttu-id="14670-219">.PHP</span><span class="sxs-lookup"><span data-stu-id="14670-219">PHP</span></span>
- <span data-ttu-id="14670-220">.RC</span><span class="sxs-lookup"><span data-stu-id="14670-220">.RC</span></span>
- <span data-ttu-id="14670-221">.RESX</span><span class="sxs-lookup"><span data-stu-id="14670-221">\*.resx</span></span>
- <span data-ttu-id="14670-222">.RPT</span><span class="sxs-lookup"><span data-stu-id="14670-222">.RPT</span></span>
- <span data-ttu-id="14670-223">.RSS</span><span class="sxs-lookup"><span data-stu-id="14670-223">RSS</span></span>
- <span data-ttu-id="14670-224">.SCPT</span><span class="sxs-lookup"><span data-stu-id="14670-224">.SCPT</span></span>
- <span data-ttu-id="14670-225">.SRC</span><span class="sxs-lookup"><span data-stu-id="14670-225">.SRC</span></span>
- <span data-ttu-id="14670-226">.VB\*</span><span class="sxs-lookup"><span data-stu-id="14670-226">.vb</span></span>
- <span data-ttu-id="14670-227">.WSF</span><span class="sxs-lookup"><span data-stu-id="14670-227">.wsf</span></span>
- <span data-ttu-id="14670-228">. XCODEPROJ</span><span class="sxs-lookup"><span data-stu-id="14670-228">.XCODEPROJ</span></span>
- <span data-ttu-id="14670-229">.XML</span><span class="sxs-lookup"><span data-stu-id="14670-229">XML</span></span>
- <span data-ttu-id="14670-230">.XSD</span><span class="sxs-lookup"><span data-stu-id="14670-230">.XSD</span></span>
- <span data-ttu-id="14670-231">.XSL\*</span><span class="sxs-lookup"><span data-stu-id="14670-231">XSL</span></span>

## <a name="retain-video-files"></a><span data-ttu-id="14670-232">Manter os arquivos de vídeo</span><span class="sxs-lookup"><span data-stu-id="14670-232">Retain video files</span></span>

<span data-ttu-id="14670-233">Este recomendação é exibida quando qualquer um dos seguintes tipos de arquivo é detectado no SharePoint ou OneDrive.</span><span class="sxs-lookup"><span data-stu-id="14670-233">This recommendation appears when any of the following file types are detected in SharePoint or OneDrive.</span></span>

- <span data-ttu-id="14670-234">.AVCHD</span><span class="sxs-lookup"><span data-stu-id="14670-234">.AVCHD</span></span>
- <span data-ttu-id="14670-235">.AVI</span><span class="sxs-lookup"><span data-stu-id="14670-235">avi</span></span>
- <span data-ttu-id="14670-236">.FLV</span><span class="sxs-lookup"><span data-stu-id="14670-236">.FLV</span></span>
- <span data-ttu-id="14670-237">.MOV</span><span class="sxs-lookup"><span data-stu-id="14670-237">.MOV</span></span>
- <span data-ttu-id="14670-238">.MP2V</span><span class="sxs-lookup"><span data-stu-id="14670-238">.MP2V</span></span>
- <span data-ttu-id="14670-239">.MP4</span><span class="sxs-lookup"><span data-stu-id="14670-239">.MP4</span></span>
- <span data-ttu-id="14670-240">.MP4V</span><span class="sxs-lookup"><span data-stu-id="14670-240">.MP4V</span></span>
- <span data-ttu-id="14670-241">.MPE</span><span class="sxs-lookup"><span data-stu-id="14670-241">.MPE</span></span>
- <span data-ttu-id="14670-242">.MPEG</span><span class="sxs-lookup"><span data-stu-id="14670-242">MPEG</span></span>
- <span data-ttu-id="14670-243">.MPEG1</span><span class="sxs-lookup"><span data-stu-id="14670-243">.MPEG1</span></span>
- <span data-ttu-id="14670-244">.MPEG2</span><span class="sxs-lookup"><span data-stu-id="14670-244">.MPEG2</span></span>
- <span data-ttu-id="14670-245">.MPEG4</span><span class="sxs-lookup"><span data-stu-id="14670-245">.MPEG4</span></span>
- <span data-ttu-id="14670-246">.MPG</span><span class="sxs-lookup"><span data-stu-id="14670-246">.MPG</span></span>
- <span data-ttu-id="14670-247">.MPG2</span><span class="sxs-lookup"><span data-stu-id="14670-247">.MPG2</span></span>
- <span data-ttu-id="14670-248">.MPG4</span><span class="sxs-lookup"><span data-stu-id="14670-248">.MPG4</span></span>
- <span data-ttu-id="14670-249">.WMV</span><span class="sxs-lookup"><span data-stu-id="14670-249">.WMV</span></span>
- <span data-ttu-id="14670-250">.XMV</span><span class="sxs-lookup"><span data-stu-id="14670-250">.XMV</span></span>

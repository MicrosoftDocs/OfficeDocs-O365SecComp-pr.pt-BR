---
title: Pesquisar e localizar dados pessoais
ms.author: bcarter
author: brendacarter
manager: laurawi
ms.date: 2/7/2018
ms.audience: ITPro
ms.topic: overview
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
- GDPR
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
description: Saiba como pesquisar e localizar dados pessoais no Office 365.
ms.openlocfilehash: 8b9359c6daf3817b4da73d6be5a652d17d19549b
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30223550"
---
# <a name="search-for-and-find-personal-data"></a><span data-ttu-id="c5f1c-103">Pesquisar e localizar dados pessoais</span><span class="sxs-lookup"><span data-stu-id="c5f1c-103">Search for and find personal data</span></span>

<span data-ttu-id="c5f1c-104">A grosso modo, o RGPD define dados pessoais como qualquer dado relativo a uma pessoa física identificada ou identificável que seja residente da União Europeia (UE).</span><span class="sxs-lookup"><span data-stu-id="c5f1c-104">Personal data is defined very broadly under the GDPR as any data that relates to an identified or identifiable natural person that is a resident of the European Union (EU).</span></span>

<span data-ttu-id="c5f1c-105">Artigo 4 – Definições</span><span class="sxs-lookup"><span data-stu-id="c5f1c-105">Article 4 – Definitions</span></span>

> <span data-ttu-id="c5f1c-106">"dados pessoais" são todas as informações relativas a uma pessoa física identificada ou identificável ("titular dos dados"); uma pessoa física identificável é alguém que pode ser identificado, direta ou indiretamente, em especial por referência a um identificador como um nome, um número de identificação, dados de localização, um identificador online ou por um ou mais elementos específicos da identidade física, fisiológica, genética, mental, econômica, cultural ou social dessa pessoa física;</span><span class="sxs-lookup"><span data-stu-id="c5f1c-106">‘personal data’ means any information relating to an identified or identifiable natural person (‘data subject’); an identifiable natural person is one who can be identified, directly or indirectly, in particular by reference to an identifier such as a name, an identification number, location data, an online identifier or to one or more factors specific to the physical, physiological, genetic, mental, economic, cultural or social identity of that natural person;</span></span>

<span data-ttu-id="c5f1c-107">Este artigo demonstra como localizar dados pessoais armazenados no SharePoint Online e no OneDrive for Business (que inclui os sites de todos os grupos do Office 365 e Microsoft Teams).</span><span class="sxs-lookup"><span data-stu-id="c5f1c-107">This article demonstrates how to find personal data stored in SharePoint Online and OneDrive for Business (which includes the sites for all Office 365 groups and Microsoft Teams).</span></span>

<span data-ttu-id="c5f1c-p101">A localização dos dados pessoais sujeitos ao RGPD depende do uso dos tipos de informações confidenciais no Office 365. Eles definem como o processo automatizado reconhecerá os tipos de informações específicas, como números de serviço de saúde e de cartões de crédito. No momento, não é possível usá-los para localizar dados em repouso nas caixas de correio do Exchange. Porém, os tipos de informações confidenciais podem ser usados com as políticas de prevenção contra perda de dados para localizar dados pessoais no email em trânsito.</span><span class="sxs-lookup"><span data-stu-id="c5f1c-p101">Finding personal data subject to GDPR relies on using sensitive information types in Office 365. These define how the automated process recognizes specific information types such as health service numbers and credit card numbers. At this time these cannot be used to find data in Exchange mailboxes at rest. However, sensitive information types can be used with data loss prevention policies to find personal data in mail while in transit.</span></span>

<span data-ttu-id="c5f1c-112">Portanto, mesmo que ainda não seja possível usar a Pesquisa de Conteúdo para localizar dados pessoais em repouso nas caixas de correio do Exchange Online, você pode usar os tipos de informações confidenciais que selecionar para o RGPD e localizar e proteger informações pessoais ao serem enviadas por email.</span><span class="sxs-lookup"><span data-stu-id="c5f1c-112">So, while you can’t currently use Content Search to find personal data at rest in Exchange Online mailboxes, you can use the sensitive information types you curate for GDPR to find and protect personal information as it is sent through email.</span></span>

## <a name="use-content-search-to-find-personal-data"></a><span data-ttu-id="c5f1c-113">Usar a Pesquisa de Conteúdo para localizar dados pessoais</span><span class="sxs-lookup"><span data-stu-id="c5f1c-113">Use Content Search to find personal data</span></span>

<span data-ttu-id="c5f1c-p102">A Microsoft recomenda uma abordagem em três etapas para localizar dados pessoais no Office 365. O restante deste tópico orienta sobre cada uma dessas etapas.</span><span class="sxs-lookup"><span data-stu-id="c5f1c-p102">Microsoft recommends a three-stage approach to finding personal data in Office 365. The rest of this topic provides guidance for each of these stages.</span></span>

<table>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c5f1c-116"><strong>Etapa</strong></span><span class="sxs-lookup"><span data-stu-id="c5f1c-116"><strong>Step</strong></span></span></th>
<th align="left"><span data-ttu-id="c5f1c-117"><strong>Descrição</strong></span><span class="sxs-lookup"><span data-stu-id="c5f1c-117"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c5f1c-118">1. Pesquisar tipos de informações confidenciais</span><span class="sxs-lookup"><span data-stu-id="c5f1c-118">1. Search for sensitive information types</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5f1c-p103">Inicie usando os tipos de informações confidenciais para localizar dados pessoais. Crie uma consulta de Pesquisa de Conteúdo para cada tipo de informação confidencial. Execute a consulta e analise os resultados.</span><span class="sxs-lookup"><span data-stu-id="c5f1c-p103">Start by using sensitive information types to find personal data. Create a Content Search query for each sensitive information type. Run the query and analyze the results.</span></span></p>
<span data-ttu-id="c5f1c-122">Se necessário, adicione parâmetros às consultas para reduzir os falsos positivos:</span><span class="sxs-lookup"><span data-stu-id="c5f1c-122">If needed, add parameters to the query to reduce false positives:</span></span> <li><span data-ttu-id="c5f1c-123">Intervalo de contagem</span><span class="sxs-lookup"><span data-stu-id="c5f1c-123">Count range</span></span></li>
    <li><span data-ttu-id="c5f1c-124">Intervalo de confiança</span><span class="sxs-lookup"><span data-stu-id="c5f1c-124">Confidence range</span></span></li>
    <li><span data-ttu-id="c5f1c-125">Outras propriedades ou operadores para consultas mais complexas</span><span class="sxs-lookup"><span data-stu-id="c5f1c-125">Other properties or operators for more complex queries</span></span></li>
<p><span data-ttu-id="c5f1c-126">Se necessário, modifique um tipo de informação confidencial para aprimorar o refinamento para a sua organização:</span><span class="sxs-lookup"><span data-stu-id="c5f1c-126">If necessary, modify a sensitive information type to improve accuracy for your organization:</span></span></p>
<p><li><span data-ttu-id="c5f1c-127">Ajuste o nível de confiança diretamente no XML.</span><span class="sxs-lookup"><span data-stu-id="c5f1c-127">Adjust the confidence level directly in the XML.</span></span></li></p>
<p><li><span data-ttu-id="c5f1c-128">Adicione palavras-chave.</span><span class="sxs-lookup"><span data-stu-id="c5f1c-128">Add key words.</span></span></li></p>
<p><li><span data-ttu-id="c5f1c-129">Ajuste os requisitos de proximidade das palavras-chave.</span><span class="sxs-lookup"><span data-stu-id="c5f1c-129">Adjust the proximity requirements for keywords.</span></span></li></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c5f1c-130">2. Usar a Keyword Query Language (KQL) para localizar dados pessoais adicionais em seu ambiente</span><span class="sxs-lookup"><span data-stu-id="c5f1c-130">2. Use Keyword Query Language (KQL) to find additional personal data in your environment</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5f1c-131">Para localizar dados não incluídos nos tipos de informações confidenciais, use a linguagem de consulta KQL para desenvolver consultas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="c5f1c-131">To find data not included in sensitive information types, use the KQL query language to develop custom queries.</span></span></p>
<p><span data-ttu-id="c5f1c-132">Teste os resultados da pesquisa e ajuste a cadeia de caracteres de consulta da KQL até atingir o resultado esperado.</span><span class="sxs-lookup"><span data-stu-id="c5f1c-132">Test the results of these searches and adjust the KQL query string until you achieve the expected result.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c5f1c-133">3. Criar novos tipos de informações confidenciais personalizados usando consultas KQL</span><span class="sxs-lookup"><span data-stu-id="c5f1c-133">3. Create new custom sensitive information types using the KQL queries</span></span></p></td>
<td align="left"><span data-ttu-id="c5f1c-p104">Após otimizar as consultas KQL para localizar os dados de destino, crie novos tipos de informações confidenciais personalizados usando essas consultas. Em seguida, você pode usar esses tipos de informações confidenciais personalizados com a Pesquisa de Conteúdo, com as políticas DLP e outras ferramentas e em outras consultas KQL.</span><span class="sxs-lookup"><span data-stu-id="c5f1c-p104">After optimizing KQL queries to find target data, create new custom sensitive information types using these queries. You can then use these custom sensitive information types with Content Search, in DLP policies and other tools, and within other KQL queries.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c5f1c-p105">Em breve será possível criar e modificar os tipos de informações confidenciais em uma nova interface do usuário no Centro de Conformidade e Segurança. Veja resultados correspondentes dinamicamente e ajuste os tipos de informações confidenciais para atender às suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="c5f1c-p105">Coming soon — You'll be able to create and modify sensitive information types in a new user interface in the Security and Compliance Center. You can dynamically see matching results and tune sensitive information types to meet your needs.</span></span>

## <a name="search-for-sensitive-information-types-using-content-search"></a><span data-ttu-id="c5f1c-138">Buscar tipos de informações confidenciais usando a Pesquisa de Conteúdo</span><span class="sxs-lookup"><span data-stu-id="c5f1c-138">Search for sensitive information types using Content Search</span></span>

<span data-ttu-id="c5f1c-p106">Comece a pesquisa de dados pessoais usando os tipos de informações confidenciais incluídos no Office 365. Eles estão relacionados no Centro de Conformidade e Segurança, em Classificação.</span><span class="sxs-lookup"><span data-stu-id="c5f1c-p106">Begin searching for personal data by using the sensitive information types that are included with Office 365. These are listed in the Security and Compliance Center under Classification.</span></span>

<span data-ttu-id="c5f1c-p107">Este tópico inclui uma lista atual dos tipos de informações confidenciais que se aplicam a cidadãos da União Europeia. Use-os como ponto de partida. Consulte regularmente o Centro de Conformidade e Segurança para ver as novas inclusões que podem ajudar a ficar em conformidade com o RGPD.</span><span class="sxs-lookup"><span data-stu-id="c5f1c-p107">This topic includes a list of current sensitive information types that apply to citizens in the European Union. Use these as a starting point. Check Security and Compliance Center frequently for new additions that can help with GDPR compliance.</span></span>

<span data-ttu-id="c5f1c-144">Confira também este artigo: [Lista de tipos de informações confidenciais e para que serve cada um](https://support.office.com/pt-BR/article/What-the-sensitive-information-types-look-for-fd505979-76be-4d9f-b459-abef3fc9e86b).</span><span class="sxs-lookup"><span data-stu-id="c5f1c-144">Also see this article: [List of sensitive information types and what each one looks for](https://support.office.com/pt-BR/article/What-the-sensitive-information-types-look-for-fd505979-76be-4d9f-b459-abef3fc9e86b).</span></span>

<span data-ttu-id="c5f1c-p108">Os tipos de informações confidenciais definem como o processo automatizado reconhecerá tipos específicos de informação, como números de contas bancárias, números de serviços de saúde e de cartões de crédito. Os tipos de informações confidenciais também são conhecidos como condições. Um tipo de informação confidencial se define por um padrão que pode ser identificado por uma expressão regular ou uma função. Além disso, podem-se usar evidências de comprovação como palavras-chave e somas de verificação para identificar um tipo de informação confidencial. Também se usa o nível de confiança e de proximidade no processo de avaliação.</span><span class="sxs-lookup"><span data-stu-id="c5f1c-p108">Sensitive information types define how the automated process recognizes specific information types such as bank account numbers, health service numbers, and credit card numbers. Sensitive information types are also referred to as conditions. A sensitive information type is defined by a pattern that can be identified by a regular expression or a function. In addition, corroborative evidence such as keywords and checksums can be used to identify a sensitive information type. Confidence level and proximity are also used in the evaluation process.</span></span>

<span data-ttu-id="c5f1c-150">No momento, os tipos de informações confidenciais não podem ser usados para localizar dados em repouso nas caixas de correio.</span><span class="sxs-lookup"><span data-stu-id="c5f1c-150">At this time sensitive information types cannot be used to find data at rest in mailboxes.</span></span>

### <a name="using-content-search-with-sensitive-information-types"></a><span data-ttu-id="c5f1c-151">Usar a Pesquisa de Conteúdo com os tipos de informações confidenciais</span><span class="sxs-lookup"><span data-stu-id="c5f1c-151">Using Content Search with sensitive information types</span></span>

<table>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c5f1c-152"><strong>Etapa</strong></span><span class="sxs-lookup"><span data-stu-id="c5f1c-152"><strong>Step</strong></span></span></th>
<th align="left"><span data-ttu-id="c5f1c-153"><strong>Mais informações</strong></span><span class="sxs-lookup"><span data-stu-id="c5f1c-153"><strong>More information</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd"><td align="left"><p><span data-ttu-id="c5f1c-154">Acessar a Pesquisa de Conteúdo no Centro de Conformidade e Segurança</span><span class="sxs-lookup"><span data-stu-id="c5f1c-154">Go to Content Search in the Security and Compliance Center</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5f1c-155">No painel esquerdo do Centro de Conformidade e Segurança, clique em **Pesquisa&amp; investigação** &gt; **Pesquisa de Conteúdo**.</span><span class="sxs-lookup"><span data-stu-id="c5f1c-155">In the left pane of the Security &amp; Compliance Center, click **Search &amp; investigation** &gt; **Content search**.</span></span></p>
<p><span data-ttu-id="c5f1c-156">Confira <a href="https://support.office.com/en-us/article/Run-a-Content-Search-in-the-Office-365-Security-Compliance-Center-61852fd9-fe8a-4880-a339-cb19ed3bff4a">Executar uma Pesquisa de Conteúdo no Centro de Conformidade e Segurança do Office 365</a>.</span><span class="sxs-lookup"><span data-stu-id="c5f1c-156">See <a href="https://support.office.com/en-us/article/Run-a-Content-Search-in-the-Office-365-Security-Compliance-Center-61852fd9-fe8a-4880-a339-cb19ed3bff4a">Run a Content Search in the Office 365 Security &amp; Compliance Center</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c5f1c-157">Criar um novo item de pesquisa para cada tipo de informação confidencial</span><span class="sxs-lookup"><span data-stu-id="c5f1c-157">Create a new search item for each sensitive information type</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5f1c-158">Use a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="c5f1c-158">Use the following syntax:</span></span></p>
<blockquote>
<p><span data-ttu-id="c5f1c-159">SensitiveType:"&lt;type&gt;"</span><span class="sxs-lookup"><span data-stu-id="c5f1c-159">SensitiveType:”&lt;type&gt;”</span></span></p>
</blockquote>
<p><span data-ttu-id="c5f1c-160">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="c5f1c-160">For example:</span></span></p>
<blockquote>
<p><span data-ttu-id="c5f1c-161">SensitiveType:&quot;Número de passaporte francês&quot;</span><span class="sxs-lookup"><span data-stu-id="c5f1c-161">SensitiveType:&quot;France Passport Number&quot;</span></span></p>
</blockquote>
<p><span data-ttu-id="c5f1c-p109">Amplie a pesquisa para o SharePoint (inclui o OneDrive for Business). A sintaxe deve ser exata e não deve haver erros de digitação ou espaços extras.</span><span class="sxs-lookup"><span data-stu-id="c5f1c-p109">Scope the search to SharePoint (includes OneDrive for Business). Make sure the syntax is exact and there are no extra spaces or typos.</span></span></p>
<p><span data-ttu-id="c5f1c-164">Confira <a href="https://support.office.com/pt-BR/article/Form-a-query-to-find-sensitive-data-stored-on-sites-3019fbc5-7f15-4972-8d0e-dc182dc7f836">Criar uma consulta para localizar dados confidenciais armazenados em sites</a>.</span><span class="sxs-lookup"><span data-stu-id="c5f1c-164">See <a href="https://support.office.com/pt-BR/article/Form-a-query-to-find-sensitive-data-stored-on-sites-3019fbc5-7f15-4972-8d0e-dc182dc7f836">Form a query to find sensitive data stored on sites</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c5f1c-165">Examinar os resultados de cada pesquisa</span><span class="sxs-lookup"><span data-stu-id="c5f1c-165">Review the results for each search</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5f1c-166">Identifique esses tipos de problemas para determinar se a precisão da consulta está adequada:</span><span class="sxs-lookup"><span data-stu-id="c5f1c-166">Look for these types of issues to determine if the query accuracy is on target:</span></span></p>
<p><li><span data-ttu-id="c5f1c-167">Muitos falsos positivos</span><span class="sxs-lookup"><span data-stu-id="c5f1c-167">Many false positives</span></span></li></p>
<p><li><span data-ttu-id="c5f1c-168">Falta de instâncias de dados conhecidos</span><span class="sxs-lookup"><span data-stu-id="c5f1c-168">Missing known instances of data</span></span></li></p>
<p><span data-ttu-id="c5f1c-169">Confira <a href="https://support.office.com/en-us/article/Export-Content-Search-results-from-the-Office-365-Security-Compliance-Center-ed48d448-3714-4c42-85f5-10f75f6a4278">Exportar os resultados da Pesquisa de Conteúdo do Centro de Conformidade e Segurança do Office 365</a>.</span><span class="sxs-lookup"><span data-stu-id="c5f1c-169">See <a href="https://support.office.com/en-us/article/Export-Content-Search-results-from-the-Office-365-Security-Compliance-Center-ed48d448-3714-4c42-85f5-10f75f6a4278">Export Content Search results from the Office 365 Security &amp; Compliance Center</a>.</span></span></p>
<p><span data-ttu-id="c5f1c-170">Observação: se estiver usando o Mozilla Firefox ou o Chrome, pode ser preciso baixar antes os relatórios usando o Internet Explorer ou o Microsoft Edge para instalar o suplemento necessário.</span><span class="sxs-lookup"><span data-stu-id="c5f1c-170">Note: if you’re using Mozilla Firefox or Chrome, you might need to first download reports using Internet Explorer or Edge in order to install the required add-in.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="sensitive-information-types-for-eu-citizen-data"></a><span data-ttu-id="c5f1c-171">Tipos de informações confidenciais para os dados de cidadãos da União Europeia</span><span class="sxs-lookup"><span data-stu-id="c5f1c-171">Sensitive information types for EU citizen data</span></span>

<span data-ttu-id="c5f1c-p110">Comece com esses tipos de informações confidenciais, muitos outros chegarão em breve para os dados pessoais na União Europeia.</span><span class="sxs-lookup"><span data-stu-id="c5f1c-p110">Start with these sensitive information types. Many more sensitive information types are coming soon for personal data in EU countries.</span></span>

> <span data-ttu-id="c5f1c-174">Número nacional belga</span><span class="sxs-lookup"><span data-stu-id="c5f1c-174">Belgium National Number</span></span>
>
> <span data-ttu-id="c5f1c-175">Número de Cartão de Crédito</span><span class="sxs-lookup"><span data-stu-id="c5f1c-175">Credit Card Number</span></span>
>
> <span data-ttu-id="c5f1c-176">Número da carteira de identidade croata</span><span class="sxs-lookup"><span data-stu-id="c5f1c-176">Croatia Identity Card Number</span></span>
>
> <span data-ttu-id="c5f1c-177">Número de identificação pessoal (NIB) croata</span><span class="sxs-lookup"><span data-stu-id="c5f1c-177">Croatia Personal Identification (OIB) Number</span></span>
>
> <span data-ttu-id="c5f1c-178">Número da carteira nacional de identidade tcheca</span><span class="sxs-lookup"><span data-stu-id="c5f1c-178">Czech National Identity Card Number</span></span>
>
> <span data-ttu-id="c5f1c-179">Número de identificação pessoal dinamarquês</span><span class="sxs-lookup"><span data-stu-id="c5f1c-179">Denmark Personal Identification Number</span></span>
>
> <span data-ttu-id="c5f1c-180">Número de cartão de débito da UE</span><span class="sxs-lookup"><span data-stu-id="c5f1c-180">EU Debit Card Number</span></span>
>
> <span data-ttu-id="c5f1c-181">RG nacional finlandês</span><span class="sxs-lookup"><span data-stu-id="c5f1c-181">Finland National ID</span></span>
>
> <span data-ttu-id="c5f1c-182">Número de passaporte finlandês</span><span class="sxs-lookup"><span data-stu-id="c5f1c-182">Finland Passport Number</span></span>
>
> <span data-ttu-id="c5f1c-183">Número da carteira de motorista francesa</span><span class="sxs-lookup"><span data-stu-id="c5f1c-183">France Driver's License Number</span></span>
>
> <span data-ttu-id="c5f1c-184">Carteira nacional de identidade francesa (CNI)</span><span class="sxs-lookup"><span data-stu-id="c5f1c-184">France National ID Card (CNI)</span></span>
>
> <span data-ttu-id="c5f1c-185">Número de passaporte francês</span><span class="sxs-lookup"><span data-stu-id="c5f1c-185">France Passport Number</span></span>
>
> <span data-ttu-id="c5f1c-186">Número da segurança social francesa (INSEE)</span><span class="sxs-lookup"><span data-stu-id="c5f1c-186">France Social Security Number (INSEE)</span></span>
>
> <span data-ttu-id="c5f1c-187">Número da carteira de motorista alemã</span><span class="sxs-lookup"><span data-stu-id="c5f1c-187">German Driver’s License Number</span></span>
>
> <span data-ttu-id="c5f1c-188">Número da carteira de identidade alemã</span><span class="sxs-lookup"><span data-stu-id="c5f1c-188">Germany Identity Card Number</span></span>
>
> <span data-ttu-id="c5f1c-189">Número de passaporte alemão</span><span class="sxs-lookup"><span data-stu-id="c5f1c-189">German Passport Number</span></span>
>
> <span data-ttu-id="c5f1c-190">Carteira nacional de identidade grega</span><span class="sxs-lookup"><span data-stu-id="c5f1c-190">Greece National ID Card</span></span>
>
> <span data-ttu-id="c5f1c-191">Número internacional de conta bancária (IBAN)</span><span class="sxs-lookup"><span data-stu-id="c5f1c-191">International Banking Account Number (IBAN)</span></span>
>
> <span data-ttu-id="c5f1c-192">Endereço IP</span><span class="sxs-lookup"><span data-stu-id="c5f1c-192">IP Address</span></span>
>
> <span data-ttu-id="c5f1c-193">Número de serviço público pessoal (PPS) irlandês</span><span class="sxs-lookup"><span data-stu-id="c5f1c-193">Ireland Personal Public Service (PPS) Number</span></span>
>
> <span data-ttu-id="c5f1c-194">Número de carteira de motorista italiana</span><span class="sxs-lookup"><span data-stu-id="c5f1c-194">Italy’s Driver’s License Number</span></span>
>
> <span data-ttu-id="c5f1c-195">Número do serviço do cidadão (BSN) holandês</span><span class="sxs-lookup"><span data-stu-id="c5f1c-195">Netherlands Citizen’s Service (BSN) Number</span></span>
>
> <span data-ttu-id="c5f1c-196">Número de identidade norueguesa</span><span class="sxs-lookup"><span data-stu-id="c5f1c-196">Norway Identity Number</span></span>
>
> <span data-ttu-id="c5f1c-197">Carteira de identidade polonesa</span><span class="sxs-lookup"><span data-stu-id="c5f1c-197">Poland Identity Card</span></span>
>
> <span data-ttu-id="c5f1c-198">RG nacional polonês (PESEL)</span><span class="sxs-lookup"><span data-stu-id="c5f1c-198">Poland National ID (PESEL)</span></span>
>
> <span data-ttu-id="c5f1c-199">Passaporte polonês</span><span class="sxs-lookup"><span data-stu-id="c5f1c-199">Poland Passport</span></span>
>
> <span data-ttu-id="c5f1c-200">Número do cartão do cidadão português</span><span class="sxs-lookup"><span data-stu-id="c5f1c-200">Portugal Citizen Card Number</span></span>
>
> <span data-ttu-id="c5f1c-201">Número da segurança social espanhola (SSN)</span><span class="sxs-lookup"><span data-stu-id="c5f1c-201">Spain Social Security Number (SSN)</span></span>
>
> <span data-ttu-id="c5f1c-202">RG nacional sueco</span><span class="sxs-lookup"><span data-stu-id="c5f1c-202">Sweden National ID</span></span>
>
> <span data-ttu-id="c5f1c-203">Número de passaporte sueco</span><span class="sxs-lookup"><span data-stu-id="c5f1c-203">Sweden Passport Number</span></span>
>
> <span data-ttu-id="c5f1c-p111">Número da carteira de motorista britânica</span><span class="sxs-lookup"><span data-stu-id="c5f1c-p111">U.K. Driver’s License Number</span></span>
>
> <span data-ttu-id="c5f1c-p112">Número do título de eleitor britânico</span><span class="sxs-lookup"><span data-stu-id="c5f1c-p112">U.K. Electoral Roll Number</span></span>
>
> <span data-ttu-id="c5f1c-p113">Número do serviço nacional de saúde britânico</span><span class="sxs-lookup"><span data-stu-id="c5f1c-p113">U.K. National Health Service Number</span></span>
>
> <span data-ttu-id="c5f1c-p114">Número do seguro nacional britânico (NINO)</span><span class="sxs-lookup"><span data-stu-id="c5f1c-p114">U.K. National Insurance Number (NINO)</span></span>
>
> <span data-ttu-id="c5f1c-p115">Número de passaporte americano/britânico</span><span class="sxs-lookup"><span data-stu-id="c5f1c-p115">U.S./U.K. Passport Number</span></span>

## <a name="add-parameters-to-a-sensitive-information-type-query-to-hone-the-results"></a><span data-ttu-id="c5f1c-214">Adicionar parâmetros a uma consulta de tipo de informação confidencial para refinar os resultados</span><span class="sxs-lookup"><span data-stu-id="c5f1c-214">Add parameters to a sensitive information type query to hone the results</span></span>

<span data-ttu-id="c5f1c-215">É possível adicionar esses parâmetros a uma consulta de tipo de informação confidencial:</span><span class="sxs-lookup"><span data-stu-id="c5f1c-215">You can add these parameters to a sensitive information type query:</span></span>

-   <span data-ttu-id="c5f1c-216">Intervalo de contagem: define o número de ocorrências de informações confidenciais que um documento precisa conter para ser incluído nos resultados da consulta.</span><span class="sxs-lookup"><span data-stu-id="c5f1c-216">Count range — define the number of occurrences of sensitive information a document needs to contain before it’s included in the query results.</span></span>

-   <span data-ttu-id="c5f1c-217">Intervalo de confiança: o nível de confiança a que o tipo confidencial detectado realmente corresponde, como 85% (85%).</span><span class="sxs-lookup"><span data-stu-id="c5f1c-217">Confidence range — the level of confidence that the detected sensitive type is actually a match, such as 85 (85%).</span></span>

<span data-ttu-id="c5f1c-218">Sintaxe:</span><span class="sxs-lookup"><span data-stu-id="c5f1c-218">Syntax:</span></span>

-   <span data-ttu-id="c5f1c-219">SensitiveType:"\<tipo\>|\<intervalo de contagem\>|\<intervalo de confiança\>"</span><span class="sxs-lookup"><span data-stu-id="c5f1c-219">SensitiveType:”\<type\>|\<count range\>|\<confidence range\>”</span></span>

<span data-ttu-id="c5f1c-220">Exemplos:</span><span class="sxs-lookup"><span data-stu-id="c5f1c-220">Examples:</span></span>

-   <span data-ttu-id="c5f1c-221">SensitiveType:"Número de cartão de crédito|5" (retornará apenas os documentos que contenham exatamente cinco números de cartão de crédito)</span><span class="sxs-lookup"><span data-stu-id="c5f1c-221">SensitiveType:“Credit Card Number|5” (return only documents that contain exactly five credit card numbers)</span></span>

-   <span data-ttu-id="c5f1c-p116">SensitiveType:"Número de cartão de crédito|\*|85.." (o intervalo de confiança é 85% ou mais)</span><span class="sxs-lookup"><span data-stu-id="c5f1c-p116">SensitiveType:“Credit Card Number|\*|85..” (confidence range is 85 percent or higher)</span></span>

<span data-ttu-id="c5f1c-224">Observação: "SensitiveType" diferencia maiúsculas e minúsculas, mas o restante da consulta não.</span><span class="sxs-lookup"><span data-stu-id="c5f1c-224">Note: “SensitiveType” is case sensitive, but the rest of the query is not.</span></span>

<span data-ttu-id="c5f1c-p117">Também é possível usar operadores e propriedades para ilustrar como você pode refinar suas consultas. Para obter mais informações e exemplos, confira [Criar uma consulta para localizar dados confidenciais armazenados em sites](https://support.office.com/pt-BR/article/Form-a-query-to-find-sensitive-data-stored-on-sites-3019fbc5-7f15-4972-8d0e-dc182dc7f836).</span><span class="sxs-lookup"><span data-stu-id="c5f1c-p117">You can also use properties, and operators to illustrate how you can refine your queries. For more information and examples, see [Form a query to find sensitive data stored on sites](https://support.office.com/pt-BR/article/Form-a-query-to-find-sensitive-data-stored-on-sites-3019fbc5-7f15-4972-8d0e-dc182dc7f836).</span></span>

---
title: Número de identificação do imposto da UE
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: Este tópico mostra o que uma política de prevenção de perda de dados (DLP) procura quando detecta o tipo de informação confidencial do número de identificação de imposto da UE. Esse tipo de informação confidencial define diferentes padrões, palavras-chave e outras evidências para cada país.
ms.openlocfilehash: 4914ff078695519c2a298190d82c86a6abebceb9
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32255519"
---
# <a name="eu-tax-identification-number"></a><span data-ttu-id="3bf79-104">Número de identificação do imposto da UE</span><span class="sxs-lookup"><span data-stu-id="3bf79-104">EU Tax Identification Number</span></span>

<span data-ttu-id="3bf79-105">Este tópico mostra o que uma política de prevenção de perda de dados (DLP) procura quando detecta o tipo de informação confidencial do número de identificação de imposto (TIN) da UE.</span><span class="sxs-lookup"><span data-stu-id="3bf79-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Tax Identification Number (TIN) sensitive information type.</span></span> <span data-ttu-id="3bf79-106">Esse tipo de informação confidencial define diferentes padrões, palavras-chave e outras evidências para cada país.</span><span class="sxs-lookup"><span data-stu-id="3bf79-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="3bf79-107">Áustria </span><span class="sxs-lookup"><span data-stu-id="3bf79-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="3bf79-108">Formatar</span><span class="sxs-lookup"><span data-stu-id="3bf79-108">Format</span></span>

<span data-ttu-id="3bf79-109">Nove dígitos com hífen opcional e barra para frente</span><span class="sxs-lookup"><span data-stu-id="3bf79-109">Nine digits with optional hyphen and forward slash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3bf79-110">Padrão</span><span class="sxs-lookup"><span data-stu-id="3bf79-110">Pattern</span></span>

<span data-ttu-id="3bf79-111">Nove dígitos com hífen opcional e barra para frente:</span><span class="sxs-lookup"><span data-stu-id="3bf79-111">Nine digits with optional hyphen and forward slash:</span></span>
  
-  <span data-ttu-id="3bf79-112">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="3bf79-112">Two digits</span></span> 
    
- <span data-ttu-id="3bf79-113">Um hífen (opcional)</span><span class="sxs-lookup"><span data-stu-id="3bf79-113">A hyphen (optional)</span></span>
    
- <span data-ttu-id="3bf79-114">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="3bf79-114">Three digits</span></span>
    
- <span data-ttu-id="3bf79-115">Uma barra (opcional)</span><span class="sxs-lookup"><span data-stu-id="3bf79-115">A forward slash (optional)</span></span>
    
- <span data-ttu-id="3bf79-116">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="3bf79-116">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="3bf79-117">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3bf79-117">Checksum</span></span>

<span data-ttu-id="3bf79-118">Sim</span><span class="sxs-lookup"><span data-stu-id="3bf79-118">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="3bf79-119">Definição</span><span class="sxs-lookup"><span data-stu-id="3bf79-119">Definition</span></span>

<span data-ttu-id="3bf79-120">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-120">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-121">A função `Func_austria_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-121">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3bf79-122">Uma palavra- `Keywords_austria_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="3bf79-122">A keyword from  `Keywords_austria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3bf79-123">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-123">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-124">A função `Func_austria_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-124">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_austria_eu_tax_file_number" />
          <Match idRef="Keywords_austria_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_austria_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3bf79-125">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3bf79-125">Keywords</span></span>

#### <a name="keywordsaustriaeutaxfilenumber"></a><span data-ttu-id="3bf79-126">Keywords_austria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3bf79-126">Keywords_austria_eu_tax_file_number</span></span>

<span data-ttu-id="3bf79-127">número do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-127">tax number</span></span>
  
<span data-ttu-id="3bf79-128">number</span><span class="sxs-lookup"><span data-stu-id="3bf79-128">number</span></span>
  
<span data-ttu-id="3bf79-129">número de registro de imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-129">tax registration number</span></span>
  
<span data-ttu-id="3bf79-130">tax id</span><span class="sxs-lookup"><span data-stu-id="3bf79-130">tax id</span></span>
  
<span data-ttu-id="3bf79-131">St.Nr.</span><span class="sxs-lookup"><span data-stu-id="3bf79-131">st.nr.</span></span>
  
<span data-ttu-id="3bf79-132">steuernummer</span><span class="sxs-lookup"><span data-stu-id="3bf79-132">steuernummer</span></span>
  
## <a name="belgium"></a><span data-ttu-id="3bf79-133">Bélgica </span><span class="sxs-lookup"><span data-stu-id="3bf79-133">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="3bf79-134">Formatar</span><span class="sxs-lookup"><span data-stu-id="3bf79-134">Format</span></span>

<span data-ttu-id="3bf79-135">11 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="3bf79-135">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3bf79-136">Padrão</span><span class="sxs-lookup"><span data-stu-id="3bf79-136">Pattern</span></span>

<span data-ttu-id="3bf79-137">11 dígitos:</span><span class="sxs-lookup"><span data-stu-id="3bf79-137">11 digits:</span></span>
  
- <span data-ttu-id="3bf79-138">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="3bf79-138">Two digits</span></span>
    
- <span data-ttu-id="3bf79-139">Um "0" ou "1"</span><span class="sxs-lookup"><span data-stu-id="3bf79-139">A "0" or "1"</span></span>
    
- <span data-ttu-id="3bf79-140">Um dígito</span><span class="sxs-lookup"><span data-stu-id="3bf79-140">One digit</span></span>
    
- <span data-ttu-id="3bf79-141">"0" ou "1" ou "2" ou "3"</span><span class="sxs-lookup"><span data-stu-id="3bf79-141">A "0" or "1" or "2" or "3"</span></span> 
    
- <span data-ttu-id="3bf79-142">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="3bf79-142">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="3bf79-143">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3bf79-143">Checksum</span></span>

<span data-ttu-id="3bf79-144">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="3bf79-144">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="3bf79-145">Definição</span><span class="sxs-lookup"><span data-stu-id="3bf79-145">Definition</span></span>

<span data-ttu-id="3bf79-146">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-146">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-147">A expressão `Regex_belgium_eu_tax_file_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-147">The regular expression  `Regex_belgium_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3bf79-148">Uma palavra- `Keywords_belgium_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="3bf79-148">A keyword from  `Keywords_belgium_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_tax_file_number" />
          <Match idRef="Keywords_belgium_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3bf79-149">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3bf79-149">Keywords</span></span>

#### <a name="keywordsbelgiumeutaxfilenumber"></a><span data-ttu-id="3bf79-150">Keywords_belgium_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3bf79-150">Keywords_belgium_eu_tax_file_number</span></span>

<span data-ttu-id="3bf79-151">número do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-151">tax number</span></span>
  
<span data-ttu-id="3bf79-152">número de Registro Nacional</span><span class="sxs-lookup"><span data-stu-id="3bf79-152">national registration number</span></span>
  
<span data-ttu-id="3bf79-153">número de registro de imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-153">tax registration number</span></span>
  
<span data-ttu-id="3bf79-154">tax id</span><span class="sxs-lookup"><span data-stu-id="3bf79-154">tax id</span></span>
  
<span data-ttu-id="3bf79-155">nse</span><span class="sxs-lookup"><span data-stu-id="3bf79-155">nif</span></span>
  
<span data-ttu-id="3bf79-156">nse</span><span class="sxs-lookup"><span data-stu-id="3bf79-156">nif#</span></span>
  
<span data-ttu-id="3bf79-157">Numéro de Registro Nacional</span><span class="sxs-lookup"><span data-stu-id="3bf79-157">numéro de registre national</span></span>
  
<span data-ttu-id="3bf79-158">Numéro d'identification fiscal</span><span class="sxs-lookup"><span data-stu-id="3bf79-158">numéro d'identification fiscale</span></span>
  
## <a name="bulgaria"></a><span data-ttu-id="3bf79-159">Bulgária</span><span class="sxs-lookup"><span data-stu-id="3bf79-159">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="3bf79-160">Formatar</span><span class="sxs-lookup"><span data-stu-id="3bf79-160">Format</span></span>

<span data-ttu-id="3bf79-161">Dez dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="3bf79-161">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3bf79-162">Padrão</span><span class="sxs-lookup"><span data-stu-id="3bf79-162">Pattern</span></span>

<span data-ttu-id="3bf79-163">10 dígitos</span><span class="sxs-lookup"><span data-stu-id="3bf79-163">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="3bf79-164">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3bf79-164">Checksum</span></span>

<span data-ttu-id="3bf79-165">Sim</span><span class="sxs-lookup"><span data-stu-id="3bf79-165">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="3bf79-166">Definição</span><span class="sxs-lookup"><span data-stu-id="3bf79-166">Definition</span></span>

<span data-ttu-id="3bf79-167">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-167">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-168">A função `Func_bulgaria_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-168">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3bf79-169">Uma palavra- `Keywords_bulgaria_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="3bf79-169">A keyword from  `Keywords_bulgaria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3bf79-170">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-170">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-171">A função `Func_bulgaria_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-171">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_bulgaria_eu_tax_file_number" />
          <Match idRef="Keywords_bulgaria_eu_tax_file_number" />
        </Pattern>
 <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_bulgaria_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3bf79-172">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3bf79-172">Keywords</span></span>

#### <a name="keywordsbulgariaeutaxfilenumber"></a><span data-ttu-id="3bf79-173">Keywords_bulgaria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3bf79-173">Keywords_bulgaria_eu_tax_file_number</span></span>

<span data-ttu-id="3bf79-174">bucn</span><span class="sxs-lookup"><span data-stu-id="3bf79-174">bucn</span></span>
  
<span data-ttu-id="3bf79-175">número civil uniforme</span><span class="sxs-lookup"><span data-stu-id="3bf79-175">uniform civil number</span></span>
  
<span data-ttu-id="3bf79-176">bucn #</span><span class="sxs-lookup"><span data-stu-id="3bf79-176">bucn#</span></span>
  
<span data-ttu-id="3bf79-177">uniformcivilnumber #</span><span class="sxs-lookup"><span data-stu-id="3bf79-177">uniformcivilnumber#</span></span>
  
<span data-ttu-id="3bf79-178">ID civil uniforme</span><span class="sxs-lookup"><span data-stu-id="3bf79-178">uniform civil id</span></span>
  
<span data-ttu-id="3bf79-179">Nenhum civil uniforme</span><span class="sxs-lookup"><span data-stu-id="3bf79-179">uniform civil no</span></span>
  
<span data-ttu-id="3bf79-180">Egn</span><span class="sxs-lookup"><span data-stu-id="3bf79-180">egn</span></span>
  
<span data-ttu-id="3bf79-181">número civil uniforme búlgaro</span><span class="sxs-lookup"><span data-stu-id="3bf79-181">bulgarian uniform civil number</span></span>
  
<span data-ttu-id="3bf79-182">uniformcivilno #</span><span class="sxs-lookup"><span data-stu-id="3bf79-182">uniformcivilno#</span></span>
  
<span data-ttu-id="3bf79-183">Egn #</span><span class="sxs-lookup"><span data-stu-id="3bf79-183">egn#</span></span>
  
<span data-ttu-id="3bf79-184">униформ граждански номер</span><span class="sxs-lookup"><span data-stu-id="3bf79-184">униформ граждански номер</span></span>
  
<span data-ttu-id="3bf79-185">ID униформ</span><span class="sxs-lookup"><span data-stu-id="3bf79-185">униформ id</span></span>
  
<span data-ttu-id="3bf79-186">ID de граждански униформ</span><span class="sxs-lookup"><span data-stu-id="3bf79-186">униформ граждански id</span></span>
  
<span data-ttu-id="3bf79-187">униформ граждански не</span><span class="sxs-lookup"><span data-stu-id="3bf79-187">униформ граждански не</span></span>
  
## <a name="croatia"></a><span data-ttu-id="3bf79-188">Croácia</span><span class="sxs-lookup"><span data-stu-id="3bf79-188">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="3bf79-189">Formatar</span><span class="sxs-lookup"><span data-stu-id="3bf79-189">Format</span></span>

<span data-ttu-id="3bf79-190">11 dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="3bf79-190">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3bf79-191">Padrão</span><span class="sxs-lookup"><span data-stu-id="3bf79-191">Pattern</span></span>

<span data-ttu-id="3bf79-192">11 dígitos:</span><span class="sxs-lookup"><span data-stu-id="3bf79-192">11 digits:</span></span>
  
- <span data-ttu-id="3bf79-193">Dez dígitos, escolhidos aleatoriamente</span><span class="sxs-lookup"><span data-stu-id="3bf79-193">Ten digits, randomly chosen</span></span>
    
- <span data-ttu-id="3bf79-194">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="3bf79-194">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="3bf79-195">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3bf79-195">Checksum</span></span>

<span data-ttu-id="3bf79-196">Sim</span><span class="sxs-lookup"><span data-stu-id="3bf79-196">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="3bf79-197">Definição</span><span class="sxs-lookup"><span data-stu-id="3bf79-197">Definition</span></span>

<span data-ttu-id="3bf79-198">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-198">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-199">A função `Func_croatia_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-199">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3bf79-200">Uma palavra- `Keywords_croatia_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="3bf79-200">A keyword from  `Keywords_croatia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3bf79-201">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-201">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-202">A função `Func_croatia_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-202">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_croatia_eu_tax_file_number" />
          <Match idRef="Keywords_croatia_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_croatia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3bf79-203">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3bf79-203">Keywords</span></span>

#### <a name="keywordscroatiaeutaxfilenumber"></a><span data-ttu-id="3bf79-204">Keywords_croatia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3bf79-204">Keywords_croatia_eu_tax_file_number</span></span>

<span data-ttu-id="3bf79-205">número do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-205">tax number</span></span>
  
<span data-ttu-id="3bf79-206">imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-206">tax</span></span>
  
<span data-ttu-id="3bf79-207">tax id</span><span class="sxs-lookup"><span data-stu-id="3bf79-207">tax id</span></span>
  
<span data-ttu-id="3bf79-208">OID</span><span class="sxs-lookup"><span data-stu-id="3bf79-208">oid</span></span>
  
<span data-ttu-id="3bf79-209">OID</span><span class="sxs-lookup"><span data-stu-id="3bf79-209">oid#</span></span>
  
<span data-ttu-id="3bf79-210">porezni broj</span><span class="sxs-lookup"><span data-stu-id="3bf79-210">porezni broj</span></span>
  
## <a name="cyprus"></a><span data-ttu-id="3bf79-211">Chipre</span><span class="sxs-lookup"><span data-stu-id="3bf79-211">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="3bf79-212">Formatar</span><span class="sxs-lookup"><span data-stu-id="3bf79-212">Format</span></span>

<span data-ttu-id="3bf79-213">Oito dígitos e uma letra no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="3bf79-213">Eight digits and one letter in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3bf79-214">Padrão</span><span class="sxs-lookup"><span data-stu-id="3bf79-214">Pattern</span></span>

<span data-ttu-id="3bf79-215">Oito dígitos e uma letra:</span><span class="sxs-lookup"><span data-stu-id="3bf79-215">Eight digits and one letter:</span></span>
  
-  <span data-ttu-id="3bf79-216">Um "0"</span><span class="sxs-lookup"><span data-stu-id="3bf79-216">A "0"</span></span> 
    
- <span data-ttu-id="3bf79-217">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="3bf79-217">Seven digits</span></span>
    
- <span data-ttu-id="3bf79-218">Uma letra (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="3bf79-218">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="3bf79-219">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3bf79-219">Checksum</span></span>

<span data-ttu-id="3bf79-220">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="3bf79-220">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="3bf79-221">Definição</span><span class="sxs-lookup"><span data-stu-id="3bf79-221">Definition</span></span>

<span data-ttu-id="3bf79-222">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-222">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-223">A função `Func_cyprus_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-223">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3bf79-224">Uma palavra- `Keywords_cyprus_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="3bf79-224">A keyword from  `Keywords_cyprus_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3bf79-225">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-225">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-226">A função `Func_cyprus_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-226">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_cyprus_eu_tax_file_number" />
          <Match idRef="Keywords_cyprus_eu_tax_file_number" />
        </Pattern>
Pattern confidenceLevel="75">
          <IdMatch idRef="Func_cyprus_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3bf79-227">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3bf79-227">Keywords</span></span>

#### <a name="keywordscypruseutaxfilenumber"></a><span data-ttu-id="3bf79-228">Keywords_cyprus_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3bf79-228">Keywords_cyprus_eu_tax_file_number</span></span>

<span data-ttu-id="3bf79-229">número do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-229">tax number</span></span>
  
<span data-ttu-id="3bf79-230">imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-230">tax</span></span>
  
<span data-ttu-id="3bf79-231">tax id</span><span class="sxs-lookup"><span data-stu-id="3bf79-231">tax id</span></span>
  
<span data-ttu-id="3bf79-232">código de identificação de imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-232">tax identification code</span></span>
  
<span data-ttu-id="3bf79-233">TIC</span><span class="sxs-lookup"><span data-stu-id="3bf79-233">tic</span></span>
  
<span data-ttu-id="3bf79-234">TIC #</span><span class="sxs-lookup"><span data-stu-id="3bf79-234">tic#</span></span>
  
<span data-ttu-id="3bf79-235">αριθμός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="3bf79-235">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="3bf79-236">φορολογική ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="3bf79-236">φορολογική ταυτότητα</span></span>
  
<span data-ttu-id="3bf79-237">κωδικός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="3bf79-237">κωδικός φορολογικού μητρώου</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="3bf79-238">República Tcheca</span><span class="sxs-lookup"><span data-stu-id="3bf79-238">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="3bf79-239">Formatar</span><span class="sxs-lookup"><span data-stu-id="3bf79-239">Format</span></span>

<span data-ttu-id="3bf79-240">Nove ou dez dígitos com uma barra invertida opcional</span><span class="sxs-lookup"><span data-stu-id="3bf79-240">Nine or ten digits with an optional backslash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3bf79-241">Padrão</span><span class="sxs-lookup"><span data-stu-id="3bf79-241">Pattern</span></span>

<span data-ttu-id="3bf79-242">Nove ou dez dígitos com uma barra invertida opcional:</span><span class="sxs-lookup"><span data-stu-id="3bf79-242">Nine or ten digits with an optional backslashl:</span></span>
  
- <span data-ttu-id="3bf79-243">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="3bf79-243">Six digits</span></span> 
    
- <span data-ttu-id="3bf79-244">Uma barra invertida (opcional)</span><span class="sxs-lookup"><span data-stu-id="3bf79-244">A backslash (optional)</span></span>
    
- <span data-ttu-id="3bf79-245">Três ou quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="3bf79-245">Three or four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="3bf79-246">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3bf79-246">Checksum</span></span>

<span data-ttu-id="3bf79-247">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="3bf79-247">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="3bf79-248">Definição</span><span class="sxs-lookup"><span data-stu-id="3bf79-248">Definition</span></span>

<span data-ttu-id="3bf79-249">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-249">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-250">A expressão `Regex_czech_republic_eu_tax_file_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-250">The regular expression  `Regex_czech_republic_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3bf79-251">Uma palavra- `Keywords_czech_republic_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="3bf79-251">A keyword from  `Keywords_czech_republic_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_tax_file_number" />
          <Match idRef="Keywords_czech_republic_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3bf79-252">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3bf79-252">Keywords</span></span>

#### <a name="keywordsczechrepubliceutaxfilenumber"></a><span data-ttu-id="3bf79-253">Keywords_czech_republic_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3bf79-253">Keywords_czech_republic_eu_tax_file_number</span></span>

<span data-ttu-id="3bf79-254">número do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-254">tax number</span></span>
  
<span data-ttu-id="3bf79-255">imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-255">tax</span></span>
  
<span data-ttu-id="3bf79-256">tax id</span><span class="sxs-lookup"><span data-stu-id="3bf79-256">tax id</span></span>
  
<span data-ttu-id="3bf79-257">número pessoal</span><span class="sxs-lookup"><span data-stu-id="3bf79-257">personal number</span></span>
  
<span data-ttu-id="3bf79-258">daňové číslo</span><span class="sxs-lookup"><span data-stu-id="3bf79-258">daňové číslo</span></span>
  
<span data-ttu-id="3bf79-259">osobní číslo</span><span class="sxs-lookup"><span data-stu-id="3bf79-259">osobní číslo</span></span>
  
## <a name="denmark"></a><span data-ttu-id="3bf79-260">Dinamarca</span><span class="sxs-lookup"><span data-stu-id="3bf79-260">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="3bf79-261">Formatar</span><span class="sxs-lookup"><span data-stu-id="3bf79-261">Format</span></span>

<span data-ttu-id="3bf79-262">Dez dígitos contendo um hífen</span><span class="sxs-lookup"><span data-stu-id="3bf79-262">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3bf79-263">Padrão</span><span class="sxs-lookup"><span data-stu-id="3bf79-263">Pattern</span></span>

<span data-ttu-id="3bf79-264">Dez dígitos contendo um hífen:</span><span class="sxs-lookup"><span data-stu-id="3bf79-264">Ten digits containing a hyphenl:</span></span>
  
-  <span data-ttu-id="3bf79-265">Seis dígitos que correspondem à data de nascimento (DDMMAA)</span><span class="sxs-lookup"><span data-stu-id="3bf79-265">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="3bf79-266">Um hífen</span><span class="sxs-lookup"><span data-stu-id="3bf79-266">A hyphen</span></span>
    
- <span data-ttu-id="3bf79-267">Quatro dígitos que correspondem a um número de sequência onde o primeiro dígito corresponde ao século do nascimento e o último dígito corresponde ao sexo da pessoa (ímpar para macho e par para fêmea)</span><span class="sxs-lookup"><span data-stu-id="3bf79-267">Four digits that correspond to a sequence number where the first digit corresponds to the century of birth and the last digit corresponds to the individual's gender (odd for male and even for female)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="3bf79-268">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3bf79-268">Checksum</span></span>

<span data-ttu-id="3bf79-269">Sim</span><span class="sxs-lookup"><span data-stu-id="3bf79-269">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="3bf79-270">Definição</span><span class="sxs-lookup"><span data-stu-id="3bf79-270">Definition</span></span>

<span data-ttu-id="3bf79-271">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-271">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-272">A função `Func_denmark_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-272">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3bf79-273">Uma palavra- `Keywords_denmark_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="3bf79-273">A keyword from  `Keywords_denmark_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3bf79-274">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-275">A função `Func_denmark_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-275">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_denmark_eu_tax_file_number" />
          <Match idRef="Keywords_denmark_eu_tax_file_number" />
        </Pattern> 
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_denmark_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3bf79-276">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3bf79-276">Keywords</span></span>

#### <a name="keywordsdenmarkeutaxfilenumber"></a><span data-ttu-id="3bf79-277">Keywords_denmark_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3bf79-277">Keywords_denmark_eu_tax_file_number</span></span>

<span data-ttu-id="3bf79-278">número do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-278">tax number</span></span>
  
<span data-ttu-id="3bf79-279">imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-279">tax</span></span>
  
<span data-ttu-id="3bf79-280">tax id</span><span class="sxs-lookup"><span data-stu-id="3bf79-280">tax id</span></span>
  
<span data-ttu-id="3bf79-281">número de CPR</span><span class="sxs-lookup"><span data-stu-id="3bf79-281">cpr number</span></span>
  
<span data-ttu-id="3bf79-282">pedir</span><span class="sxs-lookup"><span data-stu-id="3bf79-282">cpr#</span></span>
  
<span data-ttu-id="3bf79-283">Skat Nummer</span><span class="sxs-lookup"><span data-stu-id="3bf79-283">skat nummer</span></span>
  
<span data-ttu-id="3bf79-284">ID Skat</span><span class="sxs-lookup"><span data-stu-id="3bf79-284">skat id</span></span>
  
## <a name="estonia"></a><span data-ttu-id="3bf79-285">Estônia</span><span class="sxs-lookup"><span data-stu-id="3bf79-285">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="3bf79-286">Formatar</span><span class="sxs-lookup"><span data-stu-id="3bf79-286">Format</span></span>

<span data-ttu-id="3bf79-287">11 dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="3bf79-287">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3bf79-288">Padrão</span><span class="sxs-lookup"><span data-stu-id="3bf79-288">Pattern</span></span>

<span data-ttu-id="3bf79-289">11 dígitos:</span><span class="sxs-lookup"><span data-stu-id="3bf79-289">11 digits:</span></span>
  
-  <span data-ttu-id="3bf79-290">Um dígito que corresponde ao gênero e ao século de nascimento onde um número ímpar indica macho e o número par indica fêmea da seguinte maneira: 1, 2 para o século 19; 3, 4 para o século 20; e 5, 6 para o século 21</span><span class="sxs-lookup"><span data-stu-id="3bf79-290">One digit that corresponds to gender and century of birth where an odd number indicates male and the even number indicates female as follows: 1, 2 for the 19th century; 3, 4 for the 20th century; and 5, 6 for the 21st century</span></span> 
    
- <span data-ttu-id="3bf79-291">Seis dígitos que correspondem à data de nascimento (AAMMDD)</span><span class="sxs-lookup"><span data-stu-id="3bf79-291">Six digits that correspond to birth date (YYMMDD)</span></span>
    
- <span data-ttu-id="3bf79-292">Três dígitos que correspondem a um número de série separando as pessoas que nasceu na mesma data</span><span class="sxs-lookup"><span data-stu-id="3bf79-292">Three digits that correspond to a serial number separating persons born on the same date</span></span>
    
- <span data-ttu-id="3bf79-293">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="3bf79-293">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="3bf79-294">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3bf79-294">Checksum</span></span>

<span data-ttu-id="3bf79-295">Sim</span><span class="sxs-lookup"><span data-stu-id="3bf79-295">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="3bf79-296">Definição</span><span class="sxs-lookup"><span data-stu-id="3bf79-296">Definition</span></span>

<span data-ttu-id="3bf79-297">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-297">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-298">A função `Func_estonia_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-298">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3bf79-299">Uma palavra- `Keywords_estonia_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="3bf79-299">A keyword from  `Keywords_estonia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3bf79-300">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-300">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-301">A função `Func_estonia_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-301">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_estonia_eu_tax_file_number" />
          <Match idRef="Keywords_estonia_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_estonia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3bf79-302">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3bf79-302">Keywords</span></span>

#### <a name="keywordsestoniaeutaxfilenumber"></a><span data-ttu-id="3bf79-303">Keywords_estonia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3bf79-303">Keywords_estonia_eu_tax_file_number</span></span>

<span data-ttu-id="3bf79-304">número do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-304">tax number</span></span>
  
<span data-ttu-id="3bf79-305">imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-305">tax</span></span>
  
<span data-ttu-id="3bf79-306">tax id</span><span class="sxs-lookup"><span data-stu-id="3bf79-306">tax id</span></span>
  
<span data-ttu-id="3bf79-307">código pessoal</span><span class="sxs-lookup"><span data-stu-id="3bf79-307">personal code</span></span>
  
<span data-ttu-id="3bf79-308">maksunumber</span><span class="sxs-lookup"><span data-stu-id="3bf79-308">maksunumber</span></span>
  
<span data-ttu-id="3bf79-309">ID maksu</span><span class="sxs-lookup"><span data-stu-id="3bf79-309">maksu id</span></span>
  
<span data-ttu-id="3bf79-310">isikukood</span><span class="sxs-lookup"><span data-stu-id="3bf79-310">isikukood</span></span>
  
## <a name="finland"></a><span data-ttu-id="3bf79-311">Finlândia</span><span class="sxs-lookup"><span data-stu-id="3bf79-311">Finland</span></span>

### <a name="format"></a><span data-ttu-id="3bf79-312">Formatar</span><span class="sxs-lookup"><span data-stu-id="3bf79-312">Format</span></span>

<span data-ttu-id="3bf79-313">Uma combinação de 11 caracteres de dígitos, letras e sinal de mais e de menos</span><span class="sxs-lookup"><span data-stu-id="3bf79-313">An 11-character combination of digits, letters, and plus and minus sign</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3bf79-314">Padrão</span><span class="sxs-lookup"><span data-stu-id="3bf79-314">Pattern</span></span>

<span data-ttu-id="3bf79-315">Uma combinação de 11 caracteres de dígitos, letras e sinal de mais e menos:</span><span class="sxs-lookup"><span data-stu-id="3bf79-315">An 11-character combination of digits, letters, and plus and minus sign:</span></span>
  
- <span data-ttu-id="3bf79-316">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="3bf79-316">Six digits</span></span>
    
- <span data-ttu-id="3bf79-317">Uma das seguintes opções: um sinal de adição, um sinal de menos ou a letra "A" (não diferencia maiúsculas de minúsculas) onde o sinal de mais significa que nasceu entre 1800-1899, o sinal de menos significa que nasceu entre 1900-1999 e "A" significa que nasceu 2000 e depois</span><span class="sxs-lookup"><span data-stu-id="3bf79-317">One of the following: a plus sign, a minus sign, or the letter "A" (not case sensitive) where the plus sign means born between 1800-1899, the minus sign means born between 1900-1999, and "A" means born 2000 and after</span></span>
    
- <span data-ttu-id="3bf79-318">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="3bf79-318">Three digits</span></span>
    
- <span data-ttu-id="3bf79-319">Uma letra ou um número</span><span class="sxs-lookup"><span data-stu-id="3bf79-319">One letter or one number</span></span>
    
### <a name="checksum"></a><span data-ttu-id="3bf79-320">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3bf79-320">Checksum</span></span>

<span data-ttu-id="3bf79-321">Sim</span><span class="sxs-lookup"><span data-stu-id="3bf79-321">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="3bf79-322">Definição</span><span class="sxs-lookup"><span data-stu-id="3bf79-322">Definition</span></span>

<span data-ttu-id="3bf79-323">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-323">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-324">A função `Func_finland_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-324">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3bf79-325">Uma palavra- `Keywords_finland_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="3bf79-325">A keyword from  `Keywords_finland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3bf79-326">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-326">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-327">A função `Func_finland_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-327">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finland_eu_tax_file_number" />
          <Match idRef="Keywords_finland_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_finland_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3bf79-328">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3bf79-328">Keywords</span></span>

#### <a name="keywordsfinlandeutaxfilenumber"></a><span data-ttu-id="3bf79-329">Keywords_finland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3bf79-329">Keywords_finland_eu_tax_file_number</span></span>

<span data-ttu-id="3bf79-330">identification number</span><span class="sxs-lookup"><span data-stu-id="3bf79-330">identification number</span></span>
  
<span data-ttu-id="3bf79-331">ID pessoal</span><span class="sxs-lookup"><span data-stu-id="3bf79-331">personal id</span></span>
  
<span data-ttu-id="3bf79-332">número de identidade</span><span class="sxs-lookup"><span data-stu-id="3bf79-332">identity number</span></span>
  
<span data-ttu-id="3bf79-333">número de ID nacional da finlandês</span><span class="sxs-lookup"><span data-stu-id="3bf79-333">finnish national id number</span></span>
  
<span data-ttu-id="3bf79-334">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="3bf79-334">personalidnumber#</span></span>
  
<span data-ttu-id="3bf79-335">national identification number</span><span class="sxs-lookup"><span data-stu-id="3bf79-335">national identification number</span></span>
  
<span data-ttu-id="3bf79-336">número de identificação</span><span class="sxs-lookup"><span data-stu-id="3bf79-336">id number</span></span>
  
<span data-ttu-id="3bf79-337">n º de ID nacional</span><span class="sxs-lookup"><span data-stu-id="3bf79-337">national id no.</span></span>
  
<span data-ttu-id="3bf79-338">número de ID nacional</span><span class="sxs-lookup"><span data-stu-id="3bf79-338">national id number</span></span>
  
<span data-ttu-id="3bf79-339">ID não</span><span class="sxs-lookup"><span data-stu-id="3bf79-339">id no</span></span>
  
<span data-ttu-id="3bf79-340">tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="3bf79-340">tunnistenumero</span></span>
  
<span data-ttu-id="3bf79-341">henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="3bf79-341">henkilötunnus</span></span>
  
<span data-ttu-id="3bf79-342">yksilöllinen henkilökohtainen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="3bf79-342">yksilöllinen henkilökohtainen tunnistenumero</span></span>
  
<span data-ttu-id="3bf79-343">ainutlaatuinen henkilökohtainen Tunnus</span><span class="sxs-lookup"><span data-stu-id="3bf79-343">ainutlaatuinen henkilökohtainen tunnus</span></span>
  
<span data-ttu-id="3bf79-344">identiteetti numero</span><span class="sxs-lookup"><span data-stu-id="3bf79-344">identiteetti numero</span></span>
  
<span data-ttu-id="3bf79-345">Suomen Kansallinen henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="3bf79-345">suomen kansallinen henkilötunnus</span></span>
  
<span data-ttu-id="3bf79-346">henkilötunnusnumero #</span><span class="sxs-lookup"><span data-stu-id="3bf79-346">henkilötunnusnumero#</span></span>
  
<span data-ttu-id="3bf79-347">kansallisen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="3bf79-347">kansallisen tunnistenumero</span></span>
  
<span data-ttu-id="3bf79-348">tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="3bf79-348">tunnusnumero</span></span>
  
<span data-ttu-id="3bf79-349">Kansallinen Tunnus numero</span><span class="sxs-lookup"><span data-stu-id="3bf79-349">kansallinen tunnus numero</span></span>
  
## <a name="france"></a><span data-ttu-id="3bf79-350">França</span><span class="sxs-lookup"><span data-stu-id="3bf79-350">France</span></span>

### <a name="format"></a><span data-ttu-id="3bf79-351">Formatar</span><span class="sxs-lookup"><span data-stu-id="3bf79-351">Format</span></span>

<span data-ttu-id="3bf79-352">13 dígitos para pessoas e nove dígitos para entidades</span><span class="sxs-lookup"><span data-stu-id="3bf79-352">13 digits for individuals and nine digits for entities</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3bf79-353">Padrão</span><span class="sxs-lookup"><span data-stu-id="3bf79-353">Pattern</span></span>

<span data-ttu-id="3bf79-354">13 dígitos para pessoas:</span><span class="sxs-lookup"><span data-stu-id="3bf79-354">13 digits for individuals:</span></span>
  
- <span data-ttu-id="3bf79-355">Um dígito que deve ser 0, 1, 2 ou 3</span><span class="sxs-lookup"><span data-stu-id="3bf79-355">One digit that must be 0, 1, 2, or 3</span></span>
    
- <span data-ttu-id="3bf79-356">12 dígitos</span><span class="sxs-lookup"><span data-stu-id="3bf79-356">12 digits</span></span>
    
<span data-ttu-id="3bf79-357">Nove dígitos para entidades</span><span class="sxs-lookup"><span data-stu-id="3bf79-357">Nine digits for entities</span></span>
  
### <a name="checksum"></a><span data-ttu-id="3bf79-358">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3bf79-358">Checksum</span></span>

<span data-ttu-id="3bf79-359">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="3bf79-359">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="3bf79-360">Definição</span><span class="sxs-lookup"><span data-stu-id="3bf79-360">Definition</span></span>

<span data-ttu-id="3bf79-361">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-361">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-362">A função `Func_france_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-362">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3bf79-363">Uma palavra- `Keywords_france_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="3bf79-363">A keyword from  `Keywords_france_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3bf79-364">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-365">A função `Func_france_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-365">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_france_eu_tax_file_number" />
          <Match idRef="Keywords_france_eu_tax_file_number" />
        </Pattern>
 <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_france_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3bf79-366">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3bf79-366">Keywords</span></span>

#### <a name="keywordsfranceeutaxfilenumber"></a><span data-ttu-id="3bf79-367">Keywords_france_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3bf79-367">Keywords_france_eu_tax_file_number</span></span>

<span data-ttu-id="3bf79-368">número de identificação do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-368">tax identification number</span></span>
  
<span data-ttu-id="3bf79-369">número do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-369">tax number</span></span>
  
<span data-ttu-id="3bf79-370">tax id</span><span class="sxs-lookup"><span data-stu-id="3bf79-370">tax id</span></span>
  
<span data-ttu-id="3bf79-371">Numéro d'identification fiscal</span><span class="sxs-lookup"><span data-stu-id="3bf79-371">numéro d'identification fiscale</span></span>
  
## <a name="germany"></a><span data-ttu-id="3bf79-372">Alemanha</span><span class="sxs-lookup"><span data-stu-id="3bf79-372">Germany</span></span>

### <a name="format"></a><span data-ttu-id="3bf79-373">Formatar</span><span class="sxs-lookup"><span data-stu-id="3bf79-373">Format</span></span>

<span data-ttu-id="3bf79-374">11 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="3bf79-374">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3bf79-375">Padrão</span><span class="sxs-lookup"><span data-stu-id="3bf79-375">Pattern</span></span>

<span data-ttu-id="3bf79-376">11 dígitos:</span><span class="sxs-lookup"><span data-stu-id="3bf79-376">11 digits :</span></span>
  
-  <span data-ttu-id="3bf79-377">Dez dígitos</span><span class="sxs-lookup"><span data-stu-id="3bf79-377">Ten digits</span></span> 
    
- <span data-ttu-id="3bf79-378">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="3bf79-378">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="3bf79-379">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3bf79-379">Checksum</span></span>

<span data-ttu-id="3bf79-380">Sim</span><span class="sxs-lookup"><span data-stu-id="3bf79-380">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="3bf79-381">Definição</span><span class="sxs-lookup"><span data-stu-id="3bf79-381">Definition</span></span>

<span data-ttu-id="3bf79-382">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-382">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-383">A função `Func_germany_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-383">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3bf79-384">Uma palavra- `Keywords_germany_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="3bf79-384">A keyword from  `Keywords_germany_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3bf79-385">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-385">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-386">A função `Func_germany_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-386">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_germany_eu_tax_file_number" />
          <Match idRef="Keywords_germany_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_germany_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3bf79-387">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3bf79-387">Keywords</span></span>

#### <a name="keywordsgermanyeutaxfilenumber"></a><span data-ttu-id="3bf79-388">Keywords_germany_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3bf79-388">Keywords_germany_eu_tax_file_number</span></span>

<span data-ttu-id="3bf79-389">número do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-389">tax number</span></span>
  
<span data-ttu-id="3bf79-390">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-390">tax no.</span></span>
  
<span data-ttu-id="3bf79-391">taxno #</span><span class="sxs-lookup"><span data-stu-id="3bf79-391">taxno#</span></span>
  
<span data-ttu-id="3bf79-392">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="3bf79-392">taxnumber#</span></span>
  
<span data-ttu-id="3bf79-393">taxnumber</span><span class="sxs-lookup"><span data-stu-id="3bf79-393">taxnumber</span></span>
  
<span data-ttu-id="3bf79-394">tax id</span><span class="sxs-lookup"><span data-stu-id="3bf79-394">tax id</span></span>
  
<span data-ttu-id="3bf79-395">táxi #</span><span class="sxs-lookup"><span data-stu-id="3bf79-395">taxid#</span></span>
  
<span data-ttu-id="3bf79-396">número de identificação do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-396">tax identification number</span></span>
  
<span data-ttu-id="3bf79-397">n º de identificação de imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-397">tax identification no.</span></span>
  
<span data-ttu-id="3bf79-398">steuernummer</span><span class="sxs-lookup"><span data-stu-id="3bf79-398">steuernummer</span></span>
  
<span data-ttu-id="3bf79-399">ID Steuer</span><span class="sxs-lookup"><span data-stu-id="3bf79-399">steuer id</span></span>
  
<span data-ttu-id="3bf79-400">steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="3bf79-400">steueridentifikationsnummer</span></span>
  
## <a name="greece"></a><span data-ttu-id="3bf79-401">Grécia</span><span class="sxs-lookup"><span data-stu-id="3bf79-401">Greece</span></span>

### <a name="format"></a><span data-ttu-id="3bf79-402">Formatar</span><span class="sxs-lookup"><span data-stu-id="3bf79-402">Format</span></span>

<span data-ttu-id="3bf79-403">Nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="3bf79-403">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3bf79-404">Padrão</span><span class="sxs-lookup"><span data-stu-id="3bf79-404">Pattern</span></span>

<span data-ttu-id="3bf79-405">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="3bf79-405">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="3bf79-406">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3bf79-406">Checksum</span></span>

<span data-ttu-id="3bf79-407">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="3bf79-407">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="3bf79-408">Definição</span><span class="sxs-lookup"><span data-stu-id="3bf79-408">Definition</span></span>

<span data-ttu-id="3bf79-409">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-409">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-410">A expressão `Regex_greece_eu_tax_file_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-410">The regular expression  `Regex_greece_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3bf79-411">Uma palavra- `Keywords_greece_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="3bf79-411">A keyword from  `Keywords_greece_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_tax_file_number" />
          <Match idRef="Keywords_greece_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3bf79-412">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3bf79-412">Keywords</span></span>

#### <a name="keywordsgreeceeutaxfilenumber"></a><span data-ttu-id="3bf79-413">Keywords_greece_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3bf79-413">Keywords_greece_eu_tax_file_number</span></span>

<span data-ttu-id="3bf79-414">AFM</span><span class="sxs-lookup"><span data-stu-id="3bf79-414">afm</span></span>
  
<span data-ttu-id="3bf79-415">Tin</span><span class="sxs-lookup"><span data-stu-id="3bf79-415">tin</span></span>
  
<span data-ttu-id="3bf79-416">n º de ID de imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-416">tax id no.</span></span>
  
<span data-ttu-id="3bf79-417">ID de imposto não</span><span class="sxs-lookup"><span data-stu-id="3bf79-417">tax id no</span></span>
  
<span data-ttu-id="3bf79-418">número de identificação do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-418">tax identification number</span></span>
  
<span data-ttu-id="3bf79-419">número do registro de imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-419">tax registry number</span></span>
  
<span data-ttu-id="3bf79-420">n º do registro de impostos</span><span class="sxs-lookup"><span data-stu-id="3bf79-420">tax registry no.</span></span>
  
<span data-ttu-id="3bf79-421">AFM</span><span class="sxs-lookup"><span data-stu-id="3bf79-421">afm#</span></span>
  
<span data-ttu-id="3bf79-422">Tin</span><span class="sxs-lookup"><span data-stu-id="3bf79-422">tin#</span></span>
  
<span data-ttu-id="3bf79-423">taxidno #</span><span class="sxs-lookup"><span data-stu-id="3bf79-423">taxidno#</span></span>
  
<span data-ttu-id="3bf79-424">taxregistryno #</span><span class="sxs-lookup"><span data-stu-id="3bf79-424">taxregistryno#</span></span>
  
<span data-ttu-id="3bf79-425">αριθμός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="3bf79-425">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="3bf79-426">aφμ</span><span class="sxs-lookup"><span data-stu-id="3bf79-426">aφμ</span></span>
  
<span data-ttu-id="3bf79-427">aφμ αριθμός</span><span class="sxs-lookup"><span data-stu-id="3bf79-427">aφμ αριθμός</span></span>
  
<span data-ttu-id="3bf79-428">φορολογικού μητρώου νο.</span><span class="sxs-lookup"><span data-stu-id="3bf79-428">φορολογικού μητρώου νο.</span></span>
  
<span data-ttu-id="3bf79-429">τον αριθμό φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="3bf79-429">τον αριθμό φορολογικού μητρώου</span></span>
  
## <a name="hungary"></a><span data-ttu-id="3bf79-430">Hungria</span><span class="sxs-lookup"><span data-stu-id="3bf79-430">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="3bf79-431">Formatar</span><span class="sxs-lookup"><span data-stu-id="3bf79-431">Format</span></span>

<span data-ttu-id="3bf79-432">Dez dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="3bf79-432">Ten digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3bf79-433">Padrão</span><span class="sxs-lookup"><span data-stu-id="3bf79-433">Pattern</span></span>

<span data-ttu-id="3bf79-434">Dez dígitos:</span><span class="sxs-lookup"><span data-stu-id="3bf79-434">Ten digits:</span></span>
  
-  <span data-ttu-id="3bf79-435">Um dígito que deve ser "8"</span><span class="sxs-lookup"><span data-stu-id="3bf79-435">One digit that must be "8"</span></span> 
    
- <span data-ttu-id="3bf79-436">Cinco dígitos que correspondem ao número de dias entre a data 01/01/1867 e a data do nascimento da pessoa</span><span class="sxs-lookup"><span data-stu-id="3bf79-436">Five digits that correspond to the number of days between the date 01/01/1867 and the date of the birth of the individual</span></span>
    
- <span data-ttu-id="3bf79-437">Três dígitos que correspondem ao número gerado pela chance de diferenciar as pessoas nasceu no mesmo dia</span><span class="sxs-lookup"><span data-stu-id="3bf79-437">Three digits that correspond to the number generated by chance to differentiate individuals born on the same day</span></span>
    
- <span data-ttu-id="3bf79-438">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="3bf79-438">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="3bf79-439">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3bf79-439">Checksum</span></span>

<span data-ttu-id="3bf79-440">Sim</span><span class="sxs-lookup"><span data-stu-id="3bf79-440">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="3bf79-441">Definição</span><span class="sxs-lookup"><span data-stu-id="3bf79-441">Definition</span></span>

<span data-ttu-id="3bf79-442">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-442">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-443">A função `Func_hungary_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-443">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3bf79-444">Uma palavra- `Keywords_hungary_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="3bf79-444">A keyword from  `Keywords_hungary_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3bf79-445">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-445">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-446">A função `Func_hungary_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-446">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_hungary_eu_tax_file_number" />
          <Match idRef="Keywords_hungary_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_hungary_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3bf79-447">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3bf79-447">Keywords</span></span>

#### <a name="keywordshungaryeutaxfilenumber"></a><span data-ttu-id="3bf79-448">Keywords_hungary_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3bf79-448">Keywords_hungary_eu_tax_file_number</span></span>

<span data-ttu-id="3bf79-449">número de identificação do imposto húngaro</span><span class="sxs-lookup"><span data-stu-id="3bf79-449">hungarian tax identification number</span></span>
  
<span data-ttu-id="3bf79-450">Tin húngaro</span><span class="sxs-lookup"><span data-stu-id="3bf79-450">hungarian tin</span></span>
  
<span data-ttu-id="3bf79-451">número de ID do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-451">tax id number</span></span>
  
<span data-ttu-id="3bf79-452">número de IVA</span><span class="sxs-lookup"><span data-stu-id="3bf79-452">vat number</span></span>
  
<span data-ttu-id="3bf79-453">autoridade de imposto não</span><span class="sxs-lookup"><span data-stu-id="3bf79-453">tax authority no</span></span>
  
<span data-ttu-id="3bf79-454">número de identidade do imposto ID do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-454">tax id tax identity number</span></span>
  
<span data-ttu-id="3bf79-455">taxidnumber #</span><span class="sxs-lookup"><span data-stu-id="3bf79-455">taxidnumber#</span></span>
  
<span data-ttu-id="3bf79-456">Tin</span><span class="sxs-lookup"><span data-stu-id="3bf79-456">tin#</span></span>
  
<span data-ttu-id="3bf79-457">hungatiantin #</span><span class="sxs-lookup"><span data-stu-id="3bf79-457">hungatiantin#</span></span>
  
<span data-ttu-id="3bf79-458">identificação de imposto não</span><span class="sxs-lookup"><span data-stu-id="3bf79-458">tax identification no</span></span>
  
<span data-ttu-id="3bf79-459">taxidno #</span><span class="sxs-lookup"><span data-stu-id="3bf79-459">taxidno#</span></span>
  
<span data-ttu-id="3bf79-460">adóazonosító szám</span><span class="sxs-lookup"><span data-stu-id="3bf79-460">adóazonosító szám</span></span>
  
<span data-ttu-id="3bf79-461">adószám</span><span class="sxs-lookup"><span data-stu-id="3bf79-461">adószám</span></span>
  
<span data-ttu-id="3bf79-462">adóhatóság szám</span><span class="sxs-lookup"><span data-stu-id="3bf79-462">adóhatóság szám</span></span>
  
## <a name="ireland"></a><span data-ttu-id="3bf79-463">Irlanda</span><span class="sxs-lookup"><span data-stu-id="3bf79-463">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="3bf79-464">Formatar</span><span class="sxs-lookup"><span data-stu-id="3bf79-464">Format</span></span>

<span data-ttu-id="3bf79-465">Sete dígitos seguidos de uma letra sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="3bf79-465">Seven digits followed by a letter with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3bf79-466">Padrão</span><span class="sxs-lookup"><span data-stu-id="3bf79-466">Pattern</span></span>

<span data-ttu-id="3bf79-467">Sete dígitos seguidos de uma letra:</span><span class="sxs-lookup"><span data-stu-id="3bf79-467">Seven digits followed by a letter:</span></span>
  
-  <span data-ttu-id="3bf79-468">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="3bf79-468">Seven digits</span></span> 
    
- <span data-ttu-id="3bf79-469">Uma letra (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="3bf79-469">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="3bf79-470">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3bf79-470">Checksum</span></span>

<span data-ttu-id="3bf79-471">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="3bf79-471">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="3bf79-472">Definição</span><span class="sxs-lookup"><span data-stu-id="3bf79-472">Definition</span></span>

<span data-ttu-id="3bf79-473">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-473">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-474">A função `Func_ireland_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-474">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3bf79-475">Uma palavra- `Keywords_ireland_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="3bf79-475">A keyword from  `Keywords_ireland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3bf79-476">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-476">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-477">A função `Func_ireland_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-477">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_ireland_eu_tax_file_number" />
          <Match idRef="Keywords_ireland_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_ireland_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3bf79-478">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3bf79-478">Keywords</span></span>

#### <a name="keywordsirelandeutaxfilenumber"></a><span data-ttu-id="3bf79-479">Keywords_ireland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3bf79-479">Keywords_ireland_eu_tax_file_number</span></span>

<span data-ttu-id="3bf79-480">serviço público não</span><span class="sxs-lookup"><span data-stu-id="3bf79-480">public service no</span></span>
  
<span data-ttu-id="3bf79-481">serviço público pessoal não</span><span class="sxs-lookup"><span data-stu-id="3bf79-481">personal public service no</span></span>
  
<span data-ttu-id="3bf79-482">PPS não</span><span class="sxs-lookup"><span data-stu-id="3bf79-482">pps no</span></span>
  
<span data-ttu-id="3bf79-483">serviço pessoal não</span><span class="sxs-lookup"><span data-stu-id="3bf79-483">personal service no</span></span>
  
<span data-ttu-id="3bf79-484">serviço PPS não</span><span class="sxs-lookup"><span data-stu-id="3bf79-484">pps service no</span></span>
  
<span data-ttu-id="3bf79-485">ppsno #</span><span class="sxs-lookup"><span data-stu-id="3bf79-485">ppsno#</span></span>
  
<span data-ttu-id="3bf79-486">número do PPS do irlandês</span><span class="sxs-lookup"><span data-stu-id="3bf79-486">irish pps no</span></span>
  
<span data-ttu-id="3bf79-487">publicserviceno #</span><span class="sxs-lookup"><span data-stu-id="3bf79-487">publicserviceno#</span></span>
  
<span data-ttu-id="3bf79-488">número de serviço público pessoal</span><span class="sxs-lookup"><span data-stu-id="3bf79-488">personal public service number</span></span>
  
<span data-ttu-id="3bf79-489">uimhir phearsanta seirbhíse poiblí</span><span class="sxs-lookup"><span data-stu-id="3bf79-489">uimhir phearsanta seirbhíse poiblí</span></span>
  
<span data-ttu-id="3bf79-490">PPS uimh</span><span class="sxs-lookup"><span data-stu-id="3bf79-490">pps uimh</span></span>
  
<span data-ttu-id="3bf79-491">uimhir aitheantais phearsanta</span><span class="sxs-lookup"><span data-stu-id="3bf79-491">uimhir aitheantais phearsanta</span></span>
  
## <a name="italy"></a><span data-ttu-id="3bf79-492">Itália</span><span class="sxs-lookup"><span data-stu-id="3bf79-492">Italy</span></span>

### <a name="format"></a><span data-ttu-id="3bf79-493">Formatar</span><span class="sxs-lookup"><span data-stu-id="3bf79-493">Format</span></span>

<span data-ttu-id="3bf79-494">16 letras e dígitos no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="3bf79-494">16 letters and digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3bf79-495">Padrão</span><span class="sxs-lookup"><span data-stu-id="3bf79-495">Pattern</span></span>

<span data-ttu-id="3bf79-496">16 letras e dígitos:</span><span class="sxs-lookup"><span data-stu-id="3bf79-496">16 letters and digits:</span></span>
  
-  <span data-ttu-id="3bf79-497">Três letras que correspondem às três primeiras consoantes no nome da família</span><span class="sxs-lookup"><span data-stu-id="3bf79-497">Three letters that correspond to the first three consonants in the family name</span></span> 
    
- <span data-ttu-id="3bf79-498">Três letras que correspondem à primeira, terceira e quarta consoantes no primeiro nome</span><span class="sxs-lookup"><span data-stu-id="3bf79-498">Three letters that correspond to the first, third, and fourth consonants in the first name</span></span>
    
- <span data-ttu-id="3bf79-499">Dois dígitos que correspondem aos últimos dígitos do ano de nascimento</span><span class="sxs-lookup"><span data-stu-id="3bf79-499">Two digits that correspond to the last digits of the birth year</span></span>
    
- <span data-ttu-id="3bf79-500">Um dígito que corresponde ao mês de nascimento-as letras são usadas em ordem alfabética, mas apenas as letras de a a E, H, L, M, P, R a T são usadas (portanto, Janeiro é A e outubro é R)</span><span class="sxs-lookup"><span data-stu-id="3bf79-500">One digit that corresponds to the month of birth—letters are used in alphabetical order, but only the letters A to E, H, L, M, P, R to T are used (thus, January is A and October is R)</span></span>
    
- <span data-ttu-id="3bf79-501">Dois dígitos que correspondem ao dia do mês de nascimento, onde 40 é adicionado ao dia de nascimento de mulheres para diferenciar da homens</span><span class="sxs-lookup"><span data-stu-id="3bf79-501">Two digits that correspond to the day of the month of birth where 40 is added to the day of birth for females to differentiate from males</span></span>
    
- <span data-ttu-id="3bf79-502">Quatro dígitos que correspondem a um código de área específico para o município onde a pessoa nasceu — códigos em todo o país são usados para países estrangeiros</span><span class="sxs-lookup"><span data-stu-id="3bf79-502">Four digits that correspond to an area code specific to the municipality where the person was born—country-wide codes are used for foreign countries</span></span>
    
- <span data-ttu-id="3bf79-503">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="3bf79-503">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="3bf79-504">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3bf79-504">Checksum</span></span>

<span data-ttu-id="3bf79-505">Sim</span><span class="sxs-lookup"><span data-stu-id="3bf79-505">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="3bf79-506">Definição</span><span class="sxs-lookup"><span data-stu-id="3bf79-506">Definition</span></span>

<span data-ttu-id="3bf79-507">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-507">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-508">A função `Func_italy_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-508">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3bf79-509">Uma palavra- `Keywords_italy_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="3bf79-509">A keyword from  `Keywords_italy_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3bf79-510">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-510">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-511">A função `Func_italy_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-511">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_italy_eu_tax_file_number" />
          <Match idRef="Keywords_italy_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_italy_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3bf79-512">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3bf79-512">Keywords</span></span>

#### <a name="keywordsitalyeutaxfilenumber"></a><span data-ttu-id="3bf79-513">Keywords_italy_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3bf79-513">Keywords_italy_eu_tax_file_number</span></span>

<span data-ttu-id="3bf79-514">número do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-514">tax number</span></span>
  
<span data-ttu-id="3bf79-515">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-515">tax no.</span></span>
  
<span data-ttu-id="3bf79-516">taxno #</span><span class="sxs-lookup"><span data-stu-id="3bf79-516">taxno#</span></span>
  
<span data-ttu-id="3bf79-517">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="3bf79-517">taxnumber#</span></span>
  
<span data-ttu-id="3bf79-518">taxnumber</span><span class="sxs-lookup"><span data-stu-id="3bf79-518">taxnumber</span></span>
  
<span data-ttu-id="3bf79-519">tax id</span><span class="sxs-lookup"><span data-stu-id="3bf79-519">tax id</span></span>
  
<span data-ttu-id="3bf79-520">táxi #</span><span class="sxs-lookup"><span data-stu-id="3bf79-520">taxid#</span></span>
  
<span data-ttu-id="3bf79-521">código fiscal</span><span class="sxs-lookup"><span data-stu-id="3bf79-521">fiscal code</span></span>
  
<span data-ttu-id="3bf79-522">fiscalização codice</span><span class="sxs-lookup"><span data-stu-id="3bf79-522">codice fiscale</span></span>
  
## <a name="latvia"></a><span data-ttu-id="3bf79-523">Letônia</span><span class="sxs-lookup"><span data-stu-id="3bf79-523">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="3bf79-524">Formatar</span><span class="sxs-lookup"><span data-stu-id="3bf79-524">Format</span></span>

<span data-ttu-id="3bf79-525">11 dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="3bf79-525">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3bf79-526">Padrão</span><span class="sxs-lookup"><span data-stu-id="3bf79-526">Pattern</span></span>

<span data-ttu-id="3bf79-527">11 dígitos no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="3bf79-527">11 digits in the specified pattern</span></span>
  
-  <span data-ttu-id="3bf79-528">Seis dígitos que correspondem à data de nascimento (DDMMAA)</span><span class="sxs-lookup"><span data-stu-id="3bf79-528">Six digits that correspond to the date of birth (DDMMYY)</span></span> 
    
- <span data-ttu-id="3bf79-529">Um dígito que corresponde ao século de nascimento onde "0" corresponde ao século 19, "1" corresponde a 20 Century e "2" corresponde ao século 21</span><span class="sxs-lookup"><span data-stu-id="3bf79-529">One digit that corresponds to the century of birth where "0" corresponds to 19th century, "1" corresponds to 20th century, and "2"corresponds to 21st century</span></span>
    
- <span data-ttu-id="3bf79-530">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="3bf79-530">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="3bf79-531">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3bf79-531">Checksum</span></span>

<span data-ttu-id="3bf79-532">Sim</span><span class="sxs-lookup"><span data-stu-id="3bf79-532">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="3bf79-533">Definição</span><span class="sxs-lookup"><span data-stu-id="3bf79-533">Definition</span></span>

<span data-ttu-id="3bf79-534">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-534">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-535">A função `Func_latvia_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-535">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3bf79-536">Uma palavra- `Keywords_latvia_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="3bf79-536">A keyword from  `Keywords_latvia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3bf79-537">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-537">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-538">A função `Func_latvia_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-538">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_latvia_eu_tax_file_number" />
          <Match idRef="Keywords_latvia_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_latvia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3bf79-539">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3bf79-539">Keywords</span></span>

#### <a name="keywordslatviaeutaxfilenumber"></a><span data-ttu-id="3bf79-540">Keywords_latvia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3bf79-540">Keywords_latvia_eu_tax_file_number</span></span>

<span data-ttu-id="3bf79-541">número do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-541">tax number</span></span>
  
<span data-ttu-id="3bf79-542">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-542">tax no.</span></span>
  
<span data-ttu-id="3bf79-543">taxno #</span><span class="sxs-lookup"><span data-stu-id="3bf79-543">taxno#</span></span>
  
<span data-ttu-id="3bf79-544">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="3bf79-544">taxnumber#</span></span>
  
<span data-ttu-id="3bf79-545">taxnumber</span><span class="sxs-lookup"><span data-stu-id="3bf79-545">taxnumber</span></span>
  
<span data-ttu-id="3bf79-546">tax id</span><span class="sxs-lookup"><span data-stu-id="3bf79-546">tax id</span></span>
  
<span data-ttu-id="3bf79-547">táxi #</span><span class="sxs-lookup"><span data-stu-id="3bf79-547">taxid#</span></span>
  
<span data-ttu-id="3bf79-548">número de identificação do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-548">tax identification number</span></span>
  
<span data-ttu-id="3bf79-549">n º de identificação de imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-549">tax identification no.</span></span>
  
<span data-ttu-id="3bf79-550">nodokļa numurs</span><span class="sxs-lookup"><span data-stu-id="3bf79-550">nodokļa numurs</span></span>
  
<span data-ttu-id="3bf79-551">nodokļu identifikācijas numurs</span><span class="sxs-lookup"><span data-stu-id="3bf79-551">nodokļu identifikācijas numurs</span></span>
  
<span data-ttu-id="3bf79-552">nodokļu identifikācija numurs</span><span class="sxs-lookup"><span data-stu-id="3bf79-552">nodokļu identifikācija numurs</span></span>
  
## <a name="lithuania"></a><span data-ttu-id="3bf79-553">Lituânia</span><span class="sxs-lookup"><span data-stu-id="3bf79-553">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="3bf79-554">Formatar</span><span class="sxs-lookup"><span data-stu-id="3bf79-554">Format</span></span>

<span data-ttu-id="3bf79-555">11 dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="3bf79-555">11 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3bf79-556">Padrão</span><span class="sxs-lookup"><span data-stu-id="3bf79-556">Pattern</span></span>

<span data-ttu-id="3bf79-557">11 dígitos</span><span class="sxs-lookup"><span data-stu-id="3bf79-557">11 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="3bf79-558">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3bf79-558">Checksum</span></span>

<span data-ttu-id="3bf79-559">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="3bf79-559">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="3bf79-560">Definição</span><span class="sxs-lookup"><span data-stu-id="3bf79-560">Definition</span></span>

<span data-ttu-id="3bf79-561">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-561">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-562">A função `Func_lithuania_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-562">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3bf79-563">Uma palavra- `Keywords_lithuania_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="3bf79-563">A keyword from  `Keywords_lithuania_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3bf79-564">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-564">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-565">A função `Func_lithuania_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-565">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_lithuania_eu_tax_file_number" />
          <Match idRef="Keywords_lithuania_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_lithuania_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3bf79-566">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3bf79-566">Keywords</span></span>

#### <a name="keywordslithuaniaeutaxfilenumber"></a><span data-ttu-id="3bf79-567">Keywords_lithuania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3bf79-567">Keywords_lithuania_eu_tax_file_number</span></span>

<span data-ttu-id="3bf79-568">número do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-568">tax number</span></span>
  
<span data-ttu-id="3bf79-569">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-569">tax no.</span></span>
  
<span data-ttu-id="3bf79-570">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-570">tax no#</span></span>
  
<span data-ttu-id="3bf79-571">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="3bf79-571">taxnumber#</span></span>
  
<span data-ttu-id="3bf79-572">taxnumber</span><span class="sxs-lookup"><span data-stu-id="3bf79-572">taxnumber</span></span>
  
<span data-ttu-id="3bf79-573">tax id</span><span class="sxs-lookup"><span data-stu-id="3bf79-573">tax id</span></span>
  
<span data-ttu-id="3bf79-574">táxi #</span><span class="sxs-lookup"><span data-stu-id="3bf79-574">taxid#</span></span>
  
<span data-ttu-id="3bf79-575">número de identificação do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-575">tax identification number</span></span>
  
<span data-ttu-id="3bf79-576">n º de identificação de imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-576">tax identification no.</span></span>
  
<span data-ttu-id="3bf79-577">ID mokesčių</span><span class="sxs-lookup"><span data-stu-id="3bf79-577">mokesčių id</span></span>
  
<span data-ttu-id="3bf79-578">mokesčių Numeris</span><span class="sxs-lookup"><span data-stu-id="3bf79-578">mokesčių numeris</span></span>
  
<span data-ttu-id="3bf79-579">mokesčių identifikavimas Numeris</span><span class="sxs-lookup"><span data-stu-id="3bf79-579">mokesčių identifikavimas numeris</span></span>
  
## <a name="luxemburg"></a><span data-ttu-id="3bf79-580">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="3bf79-580">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="3bf79-581">Formatar</span><span class="sxs-lookup"><span data-stu-id="3bf79-581">Format</span></span>

<span data-ttu-id="3bf79-582">13 dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="3bf79-582">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3bf79-583">Padrão</span><span class="sxs-lookup"><span data-stu-id="3bf79-583">Pattern</span></span>

<span data-ttu-id="3bf79-584">13 dígitos:</span><span class="sxs-lookup"><span data-stu-id="3bf79-584">13 digits:</span></span>
  
-  <span data-ttu-id="3bf79-585">11 dígitos</span><span class="sxs-lookup"><span data-stu-id="3bf79-585">11 digits</span></span> 
    
- <span data-ttu-id="3bf79-586">Dois dígitos de verificação</span><span class="sxs-lookup"><span data-stu-id="3bf79-586">Two check digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="3bf79-587">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3bf79-587">Checksum</span></span>

<span data-ttu-id="3bf79-588">Sim</span><span class="sxs-lookup"><span data-stu-id="3bf79-588">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="3bf79-589">Definição</span><span class="sxs-lookup"><span data-stu-id="3bf79-589">Definition</span></span>

<span data-ttu-id="3bf79-590">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-590">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-591">A função `Func_luxemburg_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-591">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3bf79-592">Uma palavra- `Keywords_luxemburg_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="3bf79-592">A keyword from  `Keywords_luxemburg_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3bf79-593">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-593">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-594">A função `Func_luxemburg_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-594">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_luxemburg_eu_tax_file_number" />
          <Match idRef="Keywords_luxemburg_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_luxemburg_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3bf79-595">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3bf79-595">Keywords</span></span>

#### <a name="keywordsluxemburgeutaxfilenumber"></a><span data-ttu-id="3bf79-596">Keywords_luxemburg_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3bf79-596">Keywords_luxemburg_eu_tax_file_number</span></span>

<span data-ttu-id="3bf79-597">número do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-597">tax number</span></span>
  
<span data-ttu-id="3bf79-598">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-598">tax no.</span></span>
  
<span data-ttu-id="3bf79-599">taxno #</span><span class="sxs-lookup"><span data-stu-id="3bf79-599">taxno#</span></span>
  
<span data-ttu-id="3bf79-600">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="3bf79-600">taxnumber#</span></span>
  
<span data-ttu-id="3bf79-601">taxnumber</span><span class="sxs-lookup"><span data-stu-id="3bf79-601">taxnumber</span></span>
  
<span data-ttu-id="3bf79-602">tax id</span><span class="sxs-lookup"><span data-stu-id="3bf79-602">tax id</span></span>
  
<span data-ttu-id="3bf79-603">táxi #</span><span class="sxs-lookup"><span data-stu-id="3bf79-603">taxid#</span></span>
  
<span data-ttu-id="3bf79-604">número de identificação do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-604">tax identification number</span></span>
  
<span data-ttu-id="3bf79-605">n º de identificação de imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-605">tax identification no.</span></span>
  
<span data-ttu-id="3bf79-606">steuernummer</span><span class="sxs-lookup"><span data-stu-id="3bf79-606">steuernummer</span></span>
  
<span data-ttu-id="3bf79-607">ID Steuer</span><span class="sxs-lookup"><span data-stu-id="3bf79-607">steuer id</span></span>
  
<span data-ttu-id="3bf79-608">steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="3bf79-608">steueridentifikationsnummer</span></span>
  
## <a name="malta"></a><span data-ttu-id="3bf79-609">Malta</span><span class="sxs-lookup"><span data-stu-id="3bf79-609">Malta</span></span>

### <a name="format"></a><span data-ttu-id="3bf79-610">Formatar</span><span class="sxs-lookup"><span data-stu-id="3bf79-610">Format</span></span>

<span data-ttu-id="3bf79-611">Para as nacionalidades maltês: 7 dígitos e uma letra no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="3bf79-611">For Maltese nationals: 7 digits and one letter in the specified pattern</span></span>
  
<span data-ttu-id="3bf79-612">Entidades nacionais e Maltês não-maltês: 9 dígitos</span><span class="sxs-lookup"><span data-stu-id="3bf79-612">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3bf79-613">Padrão</span><span class="sxs-lookup"><span data-stu-id="3bf79-613">Pattern</span></span>

<span data-ttu-id="3bf79-614">Nacionalidades maltês: 7 dígitos e uma letra</span><span class="sxs-lookup"><span data-stu-id="3bf79-614">Maltese nationals: 7 digits and one letter</span></span>
  
-  <span data-ttu-id="3bf79-615">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="3bf79-615">Seven digits</span></span> 
    
- <span data-ttu-id="3bf79-616">Uma letra (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="3bf79-616">One letter (not case-sensitive)</span></span>
    
<span data-ttu-id="3bf79-617">Entidades nacionais e Maltês não-maltês: 9 dígitos</span><span class="sxs-lookup"><span data-stu-id="3bf79-617">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
-  <span data-ttu-id="3bf79-618">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="3bf79-618">Nine digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="3bf79-619">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3bf79-619">Checksum</span></span>

<span data-ttu-id="3bf79-620">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="3bf79-620">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="3bf79-621">Definição</span><span class="sxs-lookup"><span data-stu-id="3bf79-621">Definition</span></span>

<span data-ttu-id="3bf79-622">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-622">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-623">A função `Func_malta_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-623">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3bf79-624">Uma palavra- `Keywords_malta_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="3bf79-624">A keyword from  `Keywords_malta_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3bf79-625">Uma política de DLP tem 65% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-625">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-626">A função `Func_malta_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-626">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_malta_eu_tax_file_number" />
          <Match idRef="Keywords_malta_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_malta_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3bf79-627">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3bf79-627">Keywords</span></span>

#### <a name="keywordsmaltaeutaxfilenumber"></a><span data-ttu-id="3bf79-628">Keywords_malta_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3bf79-628">Keywords_malta_eu_tax_file_number</span></span>

<span data-ttu-id="3bf79-629">número do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-629">tax number</span></span>
  
<span data-ttu-id="3bf79-630">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-630">tax no.</span></span>
  
<span data-ttu-id="3bf79-631">taxno #</span><span class="sxs-lookup"><span data-stu-id="3bf79-631">taxno#</span></span>
  
<span data-ttu-id="3bf79-632">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="3bf79-632">taxnumber#</span></span>
  
<span data-ttu-id="3bf79-633">taxnumber</span><span class="sxs-lookup"><span data-stu-id="3bf79-633">taxnumber</span></span>
  
<span data-ttu-id="3bf79-634">tax id</span><span class="sxs-lookup"><span data-stu-id="3bf79-634">tax id</span></span>
  
<span data-ttu-id="3bf79-635">táxi #</span><span class="sxs-lookup"><span data-stu-id="3bf79-635">taxid#</span></span>
  
<span data-ttu-id="3bf79-636">número de identificação do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-636">tax identification number</span></span>
  
<span data-ttu-id="3bf79-637">n º de identificação de imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-637">tax identification no.</span></span>
  
<span data-ttu-id="3bf79-638">numru tat-taxxa</span><span class="sxs-lookup"><span data-stu-id="3bf79-638">numru tat-taxxa</span></span>
  
<span data-ttu-id="3bf79-639">ID tat-taxxa</span><span class="sxs-lookup"><span data-stu-id="3bf79-639">id tat-taxxa</span></span>
  
<span data-ttu-id="3bf79-640">numru ta ' identifikazzjoni tat-taxxa</span><span class="sxs-lookup"><span data-stu-id="3bf79-640">numru ta 'identifikazzjoni tat-taxxa</span></span>
  
## <a name="netherlands"></a><span data-ttu-id="3bf79-641">Países Baixos</span><span class="sxs-lookup"><span data-stu-id="3bf79-641">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="3bf79-642">Formatar</span><span class="sxs-lookup"><span data-stu-id="3bf79-642">Format</span></span>

<span data-ttu-id="3bf79-643">Nove dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="3bf79-643">Nine digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3bf79-644">Padrão</span><span class="sxs-lookup"><span data-stu-id="3bf79-644">Pattern</span></span>

<span data-ttu-id="3bf79-645">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="3bf79-645">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="3bf79-646">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3bf79-646">Checksum</span></span>

<span data-ttu-id="3bf79-647">Sim</span><span class="sxs-lookup"><span data-stu-id="3bf79-647">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="3bf79-648">Definição</span><span class="sxs-lookup"><span data-stu-id="3bf79-648">Definition</span></span>

<span data-ttu-id="3bf79-649">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-649">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-650">A função `Func_netherlands_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-650">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3bf79-651">Uma palavra- `Keywords_netherlands_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="3bf79-651">A keyword from  `Keywords_netherlands_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3bf79-652">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-652">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-653">A função `Func_netherlands_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-653">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_netherlands_eu_tax_file_number" />
          <Match idRef="Keywords_netherlands_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_netherlands_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3bf79-654">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3bf79-654">Keywords</span></span>

#### <a name="keywordsnetherlandseutaxfilenumber"></a><span data-ttu-id="3bf79-655">Keywords_netherlands_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3bf79-655">Keywords_netherlands_eu_tax_file_number</span></span>

<span data-ttu-id="3bf79-656">número de identificação do imposto Holanda</span><span class="sxs-lookup"><span data-stu-id="3bf79-656">netherlands tax identification number</span></span>
  
<span data-ttu-id="3bf79-657">identificação de imposto Holanda</span><span class="sxs-lookup"><span data-stu-id="3bf79-657">netherlands tax identification</span></span>
  
<span data-ttu-id="3bf79-658">número de identificação de imposto do Netherland</span><span class="sxs-lookup"><span data-stu-id="3bf79-658">netherland's tax identification number</span></span>
  
<span data-ttu-id="3bf79-659">identificação de imposto do Netherland</span><span class="sxs-lookup"><span data-stu-id="3bf79-659">netherland's tax identification</span></span>
  
<span data-ttu-id="3bf79-660">número de identificação do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-660">tax identification number</span></span>
  
<span data-ttu-id="3bf79-661">ID de imposto holandês</span><span class="sxs-lookup"><span data-stu-id="3bf79-661">dutch tax id</span></span>
  
<span data-ttu-id="3bf79-662">número de identificação do imposto holandês</span><span class="sxs-lookup"><span data-stu-id="3bf79-662">dutch tax identification number</span></span>
  
<span data-ttu-id="3bf79-663">tax id</span><span class="sxs-lookup"><span data-stu-id="3bf79-663">tax id</span></span>
  
<span data-ttu-id="3bf79-664">ID de imposto #</span><span class="sxs-lookup"><span data-stu-id="3bf79-664">tax id#</span></span>
  
<span data-ttu-id="3bf79-665">número do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-665">tax number</span></span>
  
<span data-ttu-id="3bf79-666">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-666">tax no#</span></span>
  
<span data-ttu-id="3bf79-667">imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-667">tax#</span></span>
  
<span data-ttu-id="3bf79-668">Tin</span><span class="sxs-lookup"><span data-stu-id="3bf79-668">tin</span></span>
  
<span data-ttu-id="3bf79-669">Tin</span><span class="sxs-lookup"><span data-stu-id="3bf79-669">tin#</span></span>
  
<span data-ttu-id="3bf79-670">Tin Holanda</span><span class="sxs-lookup"><span data-stu-id="3bf79-670">netherlands tin</span></span>
  
<span data-ttu-id="3bf79-671">Tin do Netherland</span><span class="sxs-lookup"><span data-stu-id="3bf79-671">netherland's tin</span></span>
  
<span data-ttu-id="3bf79-672">Países Baixos identificatienummer</span><span class="sxs-lookup"><span data-stu-id="3bf79-672">nederlands belasting identificatienummer</span></span>
  
<span data-ttu-id="3bf79-673">identificatienummer Van é última</span><span class="sxs-lookup"><span data-stu-id="3bf79-673">identificatienummer van belasting</span></span>
  
<span data-ttu-id="3bf79-674">identificatienummer a última</span><span class="sxs-lookup"><span data-stu-id="3bf79-674">identificatienummer belasting</span></span>
  
<span data-ttu-id="3bf79-675">Países Baixos identificatie</span><span class="sxs-lookup"><span data-stu-id="3bf79-675">nederlands belasting identificatie</span></span>
  
<span data-ttu-id="3bf79-676">Países Baixos Nummer ID da última vez</span><span class="sxs-lookup"><span data-stu-id="3bf79-676">nederlands belasting id nummer</span></span>
  
<span data-ttu-id="3bf79-677">Países Baixos belastingnummer</span><span class="sxs-lookup"><span data-stu-id="3bf79-677">nederlands belastingnummer</span></span>
  
<span data-ttu-id="3bf79-678">BTW Nummer</span><span class="sxs-lookup"><span data-stu-id="3bf79-678">btw nummer</span></span>
  
<span data-ttu-id="3bf79-679">Nederlandse identificatie</span><span class="sxs-lookup"><span data-stu-id="3bf79-679">nederlandse belasting identificatie</span></span>
  
## <a name="poland"></a><span data-ttu-id="3bf79-680">Polônia</span><span class="sxs-lookup"><span data-stu-id="3bf79-680">Poland</span></span>

### <a name="format"></a><span data-ttu-id="3bf79-681">Formatar</span><span class="sxs-lookup"><span data-stu-id="3bf79-681">Format</span></span>

<span data-ttu-id="3bf79-682">Onze dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="3bf79-682">Eleven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3bf79-683">Padrão</span><span class="sxs-lookup"><span data-stu-id="3bf79-683">Pattern</span></span>

<span data-ttu-id="3bf79-684">Onze dígitos</span><span class="sxs-lookup"><span data-stu-id="3bf79-684">Eleven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="3bf79-685">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3bf79-685">Checksum</span></span>

<span data-ttu-id="3bf79-686">Sim</span><span class="sxs-lookup"><span data-stu-id="3bf79-686">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="3bf79-687">Definição</span><span class="sxs-lookup"><span data-stu-id="3bf79-687">Definition</span></span>

<span data-ttu-id="3bf79-688">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-688">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-689">A função `Func_poland_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-689">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3bf79-690">Uma palavra- `Keywords_poland_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="3bf79-690">A keyword from  `Keywords_poland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3bf79-691">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-691">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-692">A função `Func_poland_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-692">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_poland_eu_tax_file_number" />
          <Match idRef="Keywords_poland_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_poland_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3bf79-693">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3bf79-693">Keywords</span></span>

#### <a name="keywordspolandeutaxfilenumber"></a><span data-ttu-id="3bf79-694">Keywords_poland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3bf79-694">Keywords_poland_eu_tax_file_number</span></span>

<span data-ttu-id="3bf79-695">número do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-695">tax number</span></span>
  
<span data-ttu-id="3bf79-696">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-696">tax no.</span></span>
  
<span data-ttu-id="3bf79-697">taxno #</span><span class="sxs-lookup"><span data-stu-id="3bf79-697">taxno#</span></span>
  
<span data-ttu-id="3bf79-698">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="3bf79-698">taxnumber#</span></span>
  
<span data-ttu-id="3bf79-699">taxnumber</span><span class="sxs-lookup"><span data-stu-id="3bf79-699">taxnumber</span></span>
  
<span data-ttu-id="3bf79-700">Nip</span><span class="sxs-lookup"><span data-stu-id="3bf79-700">nip</span></span>
  
<span data-ttu-id="3bf79-701">Nip #</span><span class="sxs-lookup"><span data-stu-id="3bf79-701">nip#</span></span>
  
<span data-ttu-id="3bf79-702">tax id</span><span class="sxs-lookup"><span data-stu-id="3bf79-702">tax id</span></span>
  
<span data-ttu-id="3bf79-703">ID de imposto #</span><span class="sxs-lookup"><span data-stu-id="3bf79-703">tax id#</span></span>
  
<span data-ttu-id="3bf79-704">ID Nip</span><span class="sxs-lookup"><span data-stu-id="3bf79-704">nip id</span></span>
  
<span data-ttu-id="3bf79-705">NIP ID #</span><span class="sxs-lookup"><span data-stu-id="3bf79-705">nip id#</span></span>
  
<span data-ttu-id="3bf79-706">número de identificação do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-706">tax identification number</span></span>
  
<span data-ttu-id="3bf79-707">n º de identificação de imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-707">tax identification no.</span></span>
  
<span data-ttu-id="3bf79-708">número de IVA</span><span class="sxs-lookup"><span data-stu-id="3bf79-708">vat number</span></span>
  
<span data-ttu-id="3bf79-709">IVA não.</span><span class="sxs-lookup"><span data-stu-id="3bf79-709">vat no.</span></span>
  
<span data-ttu-id="3bf79-710">vatno #</span><span class="sxs-lookup"><span data-stu-id="3bf79-710">vatno#</span></span>
  
<span data-ttu-id="3bf79-711">ID de IVA</span><span class="sxs-lookup"><span data-stu-id="3bf79-711">vat id</span></span>
  
<span data-ttu-id="3bf79-712">ID de IVA #</span><span class="sxs-lookup"><span data-stu-id="3bf79-712">vat id#</span></span>
  
<span data-ttu-id="3bf79-713">numer identyfikacji podatkowej</span><span class="sxs-lookup"><span data-stu-id="3bf79-713">numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="3bf79-714">Polski numer identyfikacji podatkowej</span><span class="sxs-lookup"><span data-stu-id="3bf79-714">polski numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="3bf79-715">numeridentyfikacjipodatkowej #</span><span class="sxs-lookup"><span data-stu-id="3bf79-715">numeridentyfikacjipodatkowej#</span></span>
  
## <a name="portugal"></a><span data-ttu-id="3bf79-716">Portugal</span><span class="sxs-lookup"><span data-stu-id="3bf79-716">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="3bf79-717">Formatar</span><span class="sxs-lookup"><span data-stu-id="3bf79-717">Format</span></span>

<span data-ttu-id="3bf79-718">Nove dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="3bf79-718">Nine digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3bf79-719">Padrão</span><span class="sxs-lookup"><span data-stu-id="3bf79-719">Pattern</span></span>

<span data-ttu-id="3bf79-720">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="3bf79-720">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="3bf79-721">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3bf79-721">Checksum</span></span>

<span data-ttu-id="3bf79-722">Sim</span><span class="sxs-lookup"><span data-stu-id="3bf79-722">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="3bf79-723">Definição</span><span class="sxs-lookup"><span data-stu-id="3bf79-723">Definition</span></span>

<span data-ttu-id="3bf79-724">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-724">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-725">A função `Func_portugal_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-725">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3bf79-726">Uma palavra- `Keywords_portugal_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="3bf79-726">A keyword from  `Keywords_portugal_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3bf79-727">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-727">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-728">A função `Func_portugal_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-728">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_portugal_eu_tax_file_number" />
          <Match idRef="Keywords_portugal_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_portugal_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3bf79-729">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3bf79-729">Keywords</span></span>

#### <a name="keywordsportugaleutaxfilenumber"></a><span data-ttu-id="3bf79-730">Keywords_portugal_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3bf79-730">Keywords_portugal_eu_tax_file_number</span></span>

<span data-ttu-id="3bf79-731">número do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-731">tax number</span></span>
  
<span data-ttu-id="3bf79-732">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-732">tax no.</span></span>
  
<span data-ttu-id="3bf79-733">taxno #</span><span class="sxs-lookup"><span data-stu-id="3bf79-733">taxno#</span></span>
  
<span data-ttu-id="3bf79-734">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="3bf79-734">taxnumber#</span></span>
  
<span data-ttu-id="3bf79-735">taxnumber</span><span class="sxs-lookup"><span data-stu-id="3bf79-735">taxnumber</span></span>
  
<span data-ttu-id="3bf79-736">nse</span><span class="sxs-lookup"><span data-stu-id="3bf79-736">nif</span></span>
  
<span data-ttu-id="3bf79-737">nse</span><span class="sxs-lookup"><span data-stu-id="3bf79-737">nif#</span></span>
  
<span data-ttu-id="3bf79-738">fiscal numero</span><span class="sxs-lookup"><span data-stu-id="3bf79-738">numero fiscal</span></span>
  
<span data-ttu-id="3bf79-739">número de identificação fiscal</span><span class="sxs-lookup"><span data-stu-id="3bf79-739">número de identificação fiscal</span></span>
  
## <a name="romania"></a><span data-ttu-id="3bf79-740">Romênia</span><span class="sxs-lookup"><span data-stu-id="3bf79-740">Romania</span></span>

### <a name="format"></a><span data-ttu-id="3bf79-741">Formatar</span><span class="sxs-lookup"><span data-stu-id="3bf79-741">Format</span></span>

<span data-ttu-id="3bf79-742">13 dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="3bf79-742">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3bf79-743">Padrão</span><span class="sxs-lookup"><span data-stu-id="3bf79-743">Pattern</span></span>

<span data-ttu-id="3bf79-744">13 dígitos</span><span class="sxs-lookup"><span data-stu-id="3bf79-744">13 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="3bf79-745">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3bf79-745">Checksum</span></span>

<span data-ttu-id="3bf79-746">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="3bf79-746">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="3bf79-747">Definição</span><span class="sxs-lookup"><span data-stu-id="3bf79-747">Definition</span></span>

<span data-ttu-id="3bf79-748">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-748">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-749">A expressão `Regex_romania_eu_tax_file_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-749">The regular expression  `Regex_romania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3bf79-750">Uma palavra- `Keywords_romania_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="3bf79-750">A keyword from  `Keywords_romania_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_tax_file_number" />
          <Match idRef="Keywords_romania_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3bf79-751">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3bf79-751">Keywords</span></span>

#### <a name="keywordsromaniaeutaxfilenumber"></a><span data-ttu-id="3bf79-752">Keywords_romania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3bf79-752">Keywords_romania_eu_tax_file_number</span></span>

<span data-ttu-id="3bf79-753">tax id</span><span class="sxs-lookup"><span data-stu-id="3bf79-753">tax id</span></span>
  
<span data-ttu-id="3bf79-754">número de ID do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-754">tax id number</span></span>
  
<span data-ttu-id="3bf79-755">arquivo de imposto não</span><span class="sxs-lookup"><span data-stu-id="3bf79-755">tax file no</span></span>
  
<span data-ttu-id="3bf79-756">tax file number</span><span class="sxs-lookup"><span data-stu-id="3bf79-756">tax file number</span></span>
  
<span data-ttu-id="3bf79-757">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-757">tax no</span></span>
  
<span data-ttu-id="3bf79-758">número do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-758">tax number</span></span>
  
<span data-ttu-id="3bf79-759">táxi #</span><span class="sxs-lookup"><span data-stu-id="3bf79-759">taxid#</span></span>
  
<span data-ttu-id="3bf79-760">taxno #</span><span class="sxs-lookup"><span data-stu-id="3bf79-760">taxno#</span></span>
  
<span data-ttu-id="3bf79-761">ID-UL Taxei</span><span class="sxs-lookup"><span data-stu-id="3bf79-761">id-ul taxei</span></span>
  
<span data-ttu-id="3bf79-762">numărul de identificare Fiscală</span><span class="sxs-lookup"><span data-stu-id="3bf79-762">numărul de identificare fiscală</span></span>
  
## <a name="slovakia"></a><span data-ttu-id="3bf79-763">Eslováquia</span><span class="sxs-lookup"><span data-stu-id="3bf79-763">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="3bf79-764">Formatar</span><span class="sxs-lookup"><span data-stu-id="3bf79-764">Format</span></span>

<span data-ttu-id="3bf79-765">10 dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="3bf79-765">10 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3bf79-766">Padrão</span><span class="sxs-lookup"><span data-stu-id="3bf79-766">Pattern</span></span>

<span data-ttu-id="3bf79-767">10 dígitos</span><span class="sxs-lookup"><span data-stu-id="3bf79-767">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="3bf79-768">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3bf79-768">Checksum</span></span>

<span data-ttu-id="3bf79-769">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="3bf79-769">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="3bf79-770">Definição</span><span class="sxs-lookup"><span data-stu-id="3bf79-770">Definition</span></span>

<span data-ttu-id="3bf79-771">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-771">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-772">A expressão `Regex_slovakia_eu_tax_file_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-772">The regular expression  `Regex_slovakia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3bf79-773">Uma palavra- `Keywords_slovakia_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="3bf79-773">A keyword from  `Keywords_slovakia_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_tax_file_number" />
          <Match idRef="Keywords_slovakia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3bf79-774">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3bf79-774">Keywords</span></span>

#### <a name="keywordsslovakiaeutaxfilenumber"></a><span data-ttu-id="3bf79-775">Keywords_slovakia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3bf79-775">Keywords_slovakia_eu_tax_file_number</span></span>

<span data-ttu-id="3bf79-776">tax id</span><span class="sxs-lookup"><span data-stu-id="3bf79-776">tax id</span></span>
  
<span data-ttu-id="3bf79-777">número de ID do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-777">tax id number</span></span>
  
<span data-ttu-id="3bf79-778">ID do Tin</span><span class="sxs-lookup"><span data-stu-id="3bf79-778">tin id</span></span>
  
<span data-ttu-id="3bf79-779">Tin não</span><span class="sxs-lookup"><span data-stu-id="3bf79-779">tin no</span></span>
  
<span data-ttu-id="3bf79-780">ID de Tin de eslovaco</span><span class="sxs-lookup"><span data-stu-id="3bf79-780">slovakian tin id</span></span>
  
<span data-ttu-id="3bf79-781">Tin</span><span class="sxs-lookup"><span data-stu-id="3bf79-781">tin</span></span>
  
<span data-ttu-id="3bf79-782">arquivo de imposto não</span><span class="sxs-lookup"><span data-stu-id="3bf79-782">tax file no</span></span>
  
<span data-ttu-id="3bf79-783">tax file number</span><span class="sxs-lookup"><span data-stu-id="3bf79-783">tax file number</span></span>
  
<span data-ttu-id="3bf79-784">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-784">tax no</span></span>
  
<span data-ttu-id="3bf79-785">número do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-785">tax number</span></span>
  
<span data-ttu-id="3bf79-786">táxi #</span><span class="sxs-lookup"><span data-stu-id="3bf79-786">taxid#</span></span>
  
<span data-ttu-id="3bf79-787">taxno #</span><span class="sxs-lookup"><span data-stu-id="3bf79-787">taxno#</span></span>
  
<span data-ttu-id="3bf79-788">daňové identifikačné číslo</span><span class="sxs-lookup"><span data-stu-id="3bf79-788">daňové identifikačné číslo</span></span>
  
<span data-ttu-id="3bf79-789">daňové číslo</span><span class="sxs-lookup"><span data-stu-id="3bf79-789">daňové číslo</span></span>
  
<span data-ttu-id="3bf79-790">daňové číslo súboru</span><span class="sxs-lookup"><span data-stu-id="3bf79-790">daňové číslo súboru</span></span>
  
## <a name="slovenia"></a><span data-ttu-id="3bf79-791">Eslovênia</span><span class="sxs-lookup"><span data-stu-id="3bf79-791">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="3bf79-792">Formatar</span><span class="sxs-lookup"><span data-stu-id="3bf79-792">Format</span></span>

<span data-ttu-id="3bf79-793">Oito dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="3bf79-793">Eight digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3bf79-794">Padrão</span><span class="sxs-lookup"><span data-stu-id="3bf79-794">Pattern</span></span>

<span data-ttu-id="3bf79-795">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="3bf79-795">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="3bf79-796">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3bf79-796">Checksum</span></span>

<span data-ttu-id="3bf79-797">Sim</span><span class="sxs-lookup"><span data-stu-id="3bf79-797">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="3bf79-798">Definição</span><span class="sxs-lookup"><span data-stu-id="3bf79-798">Definition</span></span>

<span data-ttu-id="3bf79-799">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-799">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-800">A função `Func_slovenia_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-800">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3bf79-801">Uma palavra- `Keywords_slovenia_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="3bf79-801">A keyword from  `Keywords_slovenia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3bf79-802">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-802">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-803">A função `Func_slovenia_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-803">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_nation_eu_tax_file_number" />
          <Match idRef="Keywords_nation_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_slovenia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3bf79-804">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3bf79-804">Keywords</span></span>

#### <a name="keywordssloveniaeutaxfilenumber"></a><span data-ttu-id="3bf79-805">Keywords_slovenia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3bf79-805">Keywords_slovenia_eu_tax_file_number</span></span>

<span data-ttu-id="3bf79-806">tax id</span><span class="sxs-lookup"><span data-stu-id="3bf79-806">tax id</span></span>
  
<span data-ttu-id="3bf79-807">número de ID do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-807">tax id number</span></span>
  
<span data-ttu-id="3bf79-808">ID do Tin</span><span class="sxs-lookup"><span data-stu-id="3bf79-808">tin id</span></span>
  
<span data-ttu-id="3bf79-809">Tin não</span><span class="sxs-lookup"><span data-stu-id="3bf79-809">tin no</span></span>
  
<span data-ttu-id="3bf79-810">ID de Tin esloveno</span><span class="sxs-lookup"><span data-stu-id="3bf79-810">slovenian tin id</span></span>
  
<span data-ttu-id="3bf79-811">Tin</span><span class="sxs-lookup"><span data-stu-id="3bf79-811">tin</span></span>
  
<span data-ttu-id="3bf79-812">arquivo de imposto não</span><span class="sxs-lookup"><span data-stu-id="3bf79-812">tax file no</span></span>
  
<span data-ttu-id="3bf79-813">tax file number</span><span class="sxs-lookup"><span data-stu-id="3bf79-813">tax file number</span></span>
  
<span data-ttu-id="3bf79-814">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-814">tax no</span></span>
  
<span data-ttu-id="3bf79-815">número do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-815">tax number</span></span>
  
<span data-ttu-id="3bf79-816">táxi #</span><span class="sxs-lookup"><span data-stu-id="3bf79-816">taxid#</span></span>
  
<span data-ttu-id="3bf79-817">taxno #</span><span class="sxs-lookup"><span data-stu-id="3bf79-817">taxno#</span></span>
  
<span data-ttu-id="3bf79-818">identifikacijska številka davka</span><span class="sxs-lookup"><span data-stu-id="3bf79-818">identifikacijska številka davka</span></span>
  
<span data-ttu-id="3bf79-819">davčna številka</span><span class="sxs-lookup"><span data-stu-id="3bf79-819">davčna številka</span></span>
  
<span data-ttu-id="3bf79-820">številka davčne datoteke</span><span class="sxs-lookup"><span data-stu-id="3bf79-820">številka davčne datoteke</span></span>
  
## <a name="spain"></a><span data-ttu-id="3bf79-821">Espanha</span><span class="sxs-lookup"><span data-stu-id="3bf79-821">Spain</span></span>

### <a name="format"></a><span data-ttu-id="3bf79-822">Formatar</span><span class="sxs-lookup"><span data-stu-id="3bf79-822">Format</span></span>

<span data-ttu-id="3bf79-823">Sete ou oito dígitos e uma ou duas letras no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="3bf79-823">Seven or eight digits and one or two letters in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3bf79-824">Padrão</span><span class="sxs-lookup"><span data-stu-id="3bf79-824">Pattern</span></span>

<span data-ttu-id="3bf79-825">Pessoas naturais do espanhol com um cartão de identidade nacional da Espanha:</span><span class="sxs-lookup"><span data-stu-id="3bf79-825">Spanish Natural Persons with a Spain National Identity Card:</span></span>
  
-  <span data-ttu-id="3bf79-826">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="3bf79-826">Eight digits</span></span> 
    
- <span data-ttu-id="3bf79-827">Uma letra maiúscula (diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="3bf79-827">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="3bf79-828">Spaniards não residente sem um cartão de identidade nacional da Espanha</span><span class="sxs-lookup"><span data-stu-id="3bf79-828">Non-resident Spaniards without a Spain National Identity Card</span></span>
  
- <span data-ttu-id="3bf79-829">Uma letra maiúscula "L" (diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="3bf79-829">One uppercase letter "L" (case-sensitive)</span></span>
    
- <span data-ttu-id="3bf79-830">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="3bf79-830">Seven digits</span></span>
    
- <span data-ttu-id="3bf79-831">Uma letra maiúscula (diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="3bf79-831">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="3bf79-832">Spaniards residentes sob a idade de 14 anos sem um cartão de identidade nacional da Espanha:</span><span class="sxs-lookup"><span data-stu-id="3bf79-832">Resident Spaniards under the age of 14 years without a Spain National Identity Card :</span></span>
  
- <span data-ttu-id="3bf79-833">Uma letra maiúscula "K" (diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="3bf79-833">One uppercase letter"K" (case-sensitive)</span></span>
    
-  <span data-ttu-id="3bf79-834">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="3bf79-834">Seven digits</span></span> 
    
- <span data-ttu-id="3bf79-835">Uma letra maiúscula (diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="3bf79-835">One uppercase letter (case-sensitive)</span></span>
    
<span data-ttu-id="3bf79-836">Foreigners com o número de identificação do estrangeiro</span><span class="sxs-lookup"><span data-stu-id="3bf79-836">Foreigners with a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="3bf79-837">Uma letra maiúscula que é "X", "Y" ou "Z" (diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="3bf79-837">One uppercase letter that is "X", "Y", or "Z" (case-sensitive)</span></span> 
    
- <span data-ttu-id="3bf79-838">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="3bf79-838">Seven digits</span></span>
    
- <span data-ttu-id="3bf79-839">Uma letra maiúscula (diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="3bf79-839">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="3bf79-840">Foreigners sem um número de identificação do estrangeiro</span><span class="sxs-lookup"><span data-stu-id="3bf79-840">Foreigners without a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="3bf79-841">Uma letra maiúscula que é "M" (diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="3bf79-841">One uppercase letter that is "M" (case-sensitive)</span></span> 
    
- <span data-ttu-id="3bf79-842">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="3bf79-842">Seven digits</span></span>
    
- <span data-ttu-id="3bf79-843">Uma letra maiúscula (diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="3bf79-843">One uppercase letter (case-sensitive)</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="3bf79-844">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3bf79-844">Checksum</span></span>

<span data-ttu-id="3bf79-845">Sim</span><span class="sxs-lookup"><span data-stu-id="3bf79-845">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="3bf79-846">Definição</span><span class="sxs-lookup"><span data-stu-id="3bf79-846">Definition</span></span>

<span data-ttu-id="3bf79-847">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-847">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-848">A função `Func_spain_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-848">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3bf79-849">Uma palavra- `Keywords_spain_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="3bf79-849">A keyword from  `Keywords_spain_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3bf79-850">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-850">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-851">A função `Func_spain_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-851">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_spain_eu_tax_file_number" />
          <Match idRef="Keywords_spain_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3bf79-852">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3bf79-852">Keywords</span></span>

#### <a name="keywordsspaineutaxfilenumber"></a><span data-ttu-id="3bf79-853">Keywords_spain_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3bf79-853">Keywords_spain_eu_tax_file_number</span></span>

<span data-ttu-id="3bf79-854">tax id</span><span class="sxs-lookup"><span data-stu-id="3bf79-854">tax id</span></span>
  
<span data-ttu-id="3bf79-855">número de ID do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-855">tax id number</span></span>
  
<span data-ttu-id="3bf79-856">ID de CIF</span><span class="sxs-lookup"><span data-stu-id="3bf79-856">cif id</span></span>
  
<span data-ttu-id="3bf79-857">Não CIF</span><span class="sxs-lookup"><span data-stu-id="3bf79-857">cif no</span></span>
  
<span data-ttu-id="3bf79-858">ID de CIF espanhol</span><span class="sxs-lookup"><span data-stu-id="3bf79-858">spanish cif id</span></span>
  
<span data-ttu-id="3bf79-859">CIF</span><span class="sxs-lookup"><span data-stu-id="3bf79-859">cif</span></span>
  
<span data-ttu-id="3bf79-860">arquivo de imposto não</span><span class="sxs-lookup"><span data-stu-id="3bf79-860">tax file no</span></span>
  
<span data-ttu-id="3bf79-861">número de CIF espanhol</span><span class="sxs-lookup"><span data-stu-id="3bf79-861">spanish cif number</span></span>
  
<span data-ttu-id="3bf79-862">tax file number</span><span class="sxs-lookup"><span data-stu-id="3bf79-862">tax file number</span></span>
  
<span data-ttu-id="3bf79-863">Não CIF espanhol</span><span class="sxs-lookup"><span data-stu-id="3bf79-863">spanish cif no</span></span>
  
<span data-ttu-id="3bf79-864">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-864">tax no</span></span>
  
<span data-ttu-id="3bf79-865">número do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-865">tax number</span></span>
  
<span data-ttu-id="3bf79-866">táxi #</span><span class="sxs-lookup"><span data-stu-id="3bf79-866">taxid#</span></span>
  
<span data-ttu-id="3bf79-867">taxno #</span><span class="sxs-lookup"><span data-stu-id="3bf79-867">taxno#</span></span>
  
<span data-ttu-id="3bf79-868">cifid #</span><span class="sxs-lookup"><span data-stu-id="3bf79-868">cifid#</span></span>
  
<span data-ttu-id="3bf79-869">spanishcifid #</span><span class="sxs-lookup"><span data-stu-id="3bf79-869">spanishcifid#</span></span>
  
<span data-ttu-id="3bf79-870">spanishcifno #</span><span class="sxs-lookup"><span data-stu-id="3bf79-870">spanishcifno#</span></span>
  
<span data-ttu-id="3bf79-871">número de contribuyente</span><span class="sxs-lookup"><span data-stu-id="3bf79-871">número de contribuyente</span></span>
  
<span data-ttu-id="3bf79-872">número de impuesto corporativo</span><span class="sxs-lookup"><span data-stu-id="3bf79-872">número de impuesto corporativo</span></span>
  
<span data-ttu-id="3bf79-873">número de Identificación fiscal</span><span class="sxs-lookup"><span data-stu-id="3bf79-873">número de identificación fiscal</span></span>
  
<span data-ttu-id="3bf79-874">número CIF</span><span class="sxs-lookup"><span data-stu-id="3bf79-874">cif número</span></span>
  
<span data-ttu-id="3bf79-875">cifnúmero #</span><span class="sxs-lookup"><span data-stu-id="3bf79-875">cifnúmero#</span></span>
  
## <a name="sweden"></a><span data-ttu-id="3bf79-876">Suécia</span><span class="sxs-lookup"><span data-stu-id="3bf79-876">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="3bf79-877">Formatar</span><span class="sxs-lookup"><span data-stu-id="3bf79-877">Format</span></span>

<span data-ttu-id="3bf79-878">Dez dígitos e um símbolo no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="3bf79-878">Ten digits and a symbol in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3bf79-879">Padrão</span><span class="sxs-lookup"><span data-stu-id="3bf79-879">Pattern</span></span>

<span data-ttu-id="3bf79-880">Dez dígitos e um símbolo:</span><span class="sxs-lookup"><span data-stu-id="3bf79-880">Ten digits and a symbol:</span></span>
  
-  <span data-ttu-id="3bf79-881">Seis dígitos que correspondem à data de nascimento (AAMMDD)</span><span class="sxs-lookup"><span data-stu-id="3bf79-881">Six digits that correspond to the birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="3bf79-882">Um sinal de adição, sinal de menos ou barra invertida</span><span class="sxs-lookup"><span data-stu-id="3bf79-882">A plus sign, minus sign, or backslash</span></span>
    
- <span data-ttu-id="3bf79-883">Três dígitos que tornam o número de identificação exclusivo, onde:</span><span class="sxs-lookup"><span data-stu-id="3bf79-883">Three digits that make the identification number unique where:</span></span> 
    
  - <span data-ttu-id="3bf79-884">Para números emitidos antes de 1990, o sétimo e oitavo dígito identificam o Condado de nascimento ou pessoas de nasceu</span><span class="sxs-lookup"><span data-stu-id="3bf79-884">For numbers issued before 1990, the seventh and eighth digit identify the county of birth or foreign-born people</span></span>
    
  - <span data-ttu-id="3bf79-885">O dígito na nona posição indica sexo por tanto ímpar para masculino ou par para fêmea</span><span class="sxs-lookup"><span data-stu-id="3bf79-885">The digit in the ninth position indicates gender by either odd for male or even for female</span></span>
    
- <span data-ttu-id="3bf79-886">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="3bf79-886">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="3bf79-887">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3bf79-887">Checksum</span></span>

<span data-ttu-id="3bf79-888">Sim</span><span class="sxs-lookup"><span data-stu-id="3bf79-888">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="3bf79-889">Definição</span><span class="sxs-lookup"><span data-stu-id="3bf79-889">Definition</span></span>

<span data-ttu-id="3bf79-890">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-890">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-891">A função `Func_sweden_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-891">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3bf79-892">Uma palavra- `Keywords_sweden_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="3bf79-892">A keyword from  `Keywords_sweden_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3bf79-893">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-893">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-894">A função `Func_sweden_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-894">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_sweden_eu_tax_file_number" />
          <Match idRef="Keywords_sweden_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_sweden_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3bf79-895">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3bf79-895">Keywords</span></span>

#### <a name="keywordsswedeneutaxfilenumber"></a><span data-ttu-id="3bf79-896">Keywords_sweden_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3bf79-896">Keywords_sweden_eu_tax_file_number</span></span>

<span data-ttu-id="3bf79-897">tax id</span><span class="sxs-lookup"><span data-stu-id="3bf79-897">tax id</span></span>
  
<span data-ttu-id="3bf79-898">n º de ID de imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-898">tax id no.</span></span>
  
<span data-ttu-id="3bf79-899">número de ID do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-899">tax id number</span></span>
  
<span data-ttu-id="3bf79-900">tax identification</span><span class="sxs-lookup"><span data-stu-id="3bf79-900">tax identification</span></span>
  
<span data-ttu-id="3bf79-901">identificação de imposto #</span><span class="sxs-lookup"><span data-stu-id="3bf79-901">tax identification#</span></span>
  
<span data-ttu-id="3bf79-902">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-902">tax no.</span></span>
  
<span data-ttu-id="3bf79-903">imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-903">tax#</span></span>
  
<span data-ttu-id="3bf79-904">táxi #</span><span class="sxs-lookup"><span data-stu-id="3bf79-904">taxid#</span></span>
  
<span data-ttu-id="3bf79-905">arquivo de imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-905">tax file</span></span>
  
<span data-ttu-id="3bf79-906">arquivo de impostos não.</span><span class="sxs-lookup"><span data-stu-id="3bf79-906">tax file no.</span></span>
  
<span data-ttu-id="3bf79-907">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="3bf79-907">personal id number</span></span>
  
<span data-ttu-id="3bf79-908">skatt ID Nummer</span><span class="sxs-lookup"><span data-stu-id="3bf79-908">skatt id nummer</span></span>
  
<span data-ttu-id="3bf79-909">skatt identifikation</span><span class="sxs-lookup"><span data-stu-id="3bf79-909">skatt identifikation</span></span>
  
<span data-ttu-id="3bf79-910">personnummer</span><span class="sxs-lookup"><span data-stu-id="3bf79-910">personnummer</span></span>
  
## <a name="uk"></a><span data-ttu-id="3bf79-911">Reino Unido</span><span class="sxs-lookup"><span data-stu-id="3bf79-911">UK</span></span>

### <a name="format"></a><span data-ttu-id="3bf79-912">Formatar</span><span class="sxs-lookup"><span data-stu-id="3bf79-912">Format</span></span>

<span data-ttu-id="3bf79-913">Referência de contribuidor exclusivo (UTR): 10 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="3bf79-913">Unique Taxpayer Reference (UTR): 10 digits without spaces and delimiters</span></span>
  
<span data-ttu-id="3bf79-914">Número de seguro nacional (NINO): para obter detalhes, consulte a seção "Reino Unido</span><span class="sxs-lookup"><span data-stu-id="3bf79-914">National Insurance Number (NINO): For details, see the section "U.K.</span></span> <span data-ttu-id="3bf79-915">Número de seguro nacional (NINO) "em [o que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="3bf79-915">National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3bf79-916">Padrão</span><span class="sxs-lookup"><span data-stu-id="3bf79-916">Pattern</span></span>

<span data-ttu-id="3bf79-917">Referência de contribuidor exclusivo (UTR): 10 dígitos</span><span class="sxs-lookup"><span data-stu-id="3bf79-917">Unique Taxpayer Reference (UTR): 10 digits</span></span>
  
<span data-ttu-id="3bf79-918">Número de seguro nacional (NINO): para obter detalhes, consulte a seção "Reino Unido</span><span class="sxs-lookup"><span data-stu-id="3bf79-918">National Insurance Number (NINO): For details, see the section "U.K.</span></span> <span data-ttu-id="3bf79-919">Número de seguro nacional (NINO) "em [o que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="3bf79-919">National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="checksum"></a><span data-ttu-id="3bf79-920">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3bf79-920">Checksum</span></span>

<span data-ttu-id="3bf79-921">Sim</span><span class="sxs-lookup"><span data-stu-id="3bf79-921">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="3bf79-922">Definição</span><span class="sxs-lookup"><span data-stu-id="3bf79-922">Definition</span></span>

<span data-ttu-id="3bf79-923">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3bf79-923">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3bf79-924">A função `Func_uk_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3bf79-924">The function  `Func_uk_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3bf79-925">Uma palavra- `Keywords_uk_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="3bf79-925">A keyword from  `Keywords_uk_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_uk_eu_tax_file_number" />
          <Match idRef="Keywords_uk_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3bf79-926">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3bf79-926">Keywords</span></span>

#### <a name="keywordsukeutaxfilenumber"></a><span data-ttu-id="3bf79-927">Keywords_uk_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3bf79-927">Keywords_uk_eu_tax_file_number</span></span>

<span data-ttu-id="3bf79-928">tax id</span><span class="sxs-lookup"><span data-stu-id="3bf79-928">tax id</span></span>
  
<span data-ttu-id="3bf79-929">n º de ID de imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-929">tax id no.</span></span>
  
<span data-ttu-id="3bf79-930">número de ID do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-930">tax id number</span></span>
  
<span data-ttu-id="3bf79-931">tax identification</span><span class="sxs-lookup"><span data-stu-id="3bf79-931">tax identification</span></span>
  
<span data-ttu-id="3bf79-932">identificação de imposto #</span><span class="sxs-lookup"><span data-stu-id="3bf79-932">tax identification#</span></span>
  
<span data-ttu-id="3bf79-933">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-933">tax no.</span></span>
  
<span data-ttu-id="3bf79-934">imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-934">tax#</span></span>
  
<span data-ttu-id="3bf79-935">táxi #</span><span class="sxs-lookup"><span data-stu-id="3bf79-935">taxid#</span></span>
  
<span data-ttu-id="3bf79-936">arquivo de imposto</span><span class="sxs-lookup"><span data-stu-id="3bf79-936">tax file</span></span>
  
<span data-ttu-id="3bf79-937">arquivo de impostos não.</span><span class="sxs-lookup"><span data-stu-id="3bf79-937">tax file no.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3bf79-938">Confira também</span><span class="sxs-lookup"><span data-stu-id="3bf79-938">See also</span></span>

[<span data-ttu-id="3bf79-939">O que os tipos de informações confidenciais procuram</span><span class="sxs-lookup"><span data-stu-id="3bf79-939">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)


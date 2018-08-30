---
title: Número de identificação de imposto da UE
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: f04919c8-2356-4de2-bb2a-b9f67f339726
description: Este tópico mostra o que uma política de prevenção (DLP) de perda de dados procura por quando detecta o tipo de informações confidenciais de número de identificação de imposto da UE. Esse tipo de informações confidenciais define diferentes padrões, palavras-chave e outras evidências para cada país.
ms.openlocfilehash: 5192496b393d15fd6d063e09c9bfe1cb3dd7e2dd
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524029"
---
# <a name="eu-tax-identification-number"></a><span data-ttu-id="3ec72-104">Número de identificação de imposto da UE</span><span class="sxs-lookup"><span data-stu-id="3ec72-104">EU Tax Identification Number</span></span>

<span data-ttu-id="3ec72-p102">Este tópico mostra o que uma política de prevenção (DLP) de perda de dados procura por quando detecta o tipo de informações confidenciais de número de identificação da UE imposto (TIN). Esse tipo de informações confidenciais define diferentes padrões, palavras-chave e outras evidências para cada país.</span><span class="sxs-lookup"><span data-stu-id="3ec72-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Tax Identification Number (TIN) sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="3ec72-107">Áustria</span><span class="sxs-lookup"><span data-stu-id="3ec72-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="3ec72-108">Formato</span><span class="sxs-lookup"><span data-stu-id="3ec72-108">Format</span></span>

<span data-ttu-id="3ec72-109">Nove dígitos com hífen opcional e barra invertida</span><span class="sxs-lookup"><span data-stu-id="3ec72-109">Nine digits with optional hyphen and forward slash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ec72-110">Padrão</span><span class="sxs-lookup"><span data-stu-id="3ec72-110">Pattern</span></span>

<span data-ttu-id="3ec72-111">Nove dígitos com hífen opcional e barra invertida:</span><span class="sxs-lookup"><span data-stu-id="3ec72-111">Nine digits with optional hyphen and forward slash:</span></span>
  
-  <span data-ttu-id="3ec72-112">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="3ec72-112">Two digits</span></span> 
    
- <span data-ttu-id="3ec72-113">Um hífen (opcional)</span><span class="sxs-lookup"><span data-stu-id="3ec72-113">A hyphen (optional)</span></span>
    
- <span data-ttu-id="3ec72-114">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="3ec72-114">Three digits</span></span>
    
- <span data-ttu-id="3ec72-115">Uma barra (opcional)</span><span class="sxs-lookup"><span data-stu-id="3ec72-115">A forward slash (optional)</span></span>
    
- <span data-ttu-id="3ec72-116">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="3ec72-116">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="3ec72-117">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3ec72-117">Checksum</span></span>

<span data-ttu-id="3ec72-118">Sim</span><span class="sxs-lookup"><span data-stu-id="3ec72-118">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ec72-119">Definição</span><span class="sxs-lookup"><span data-stu-id="3ec72-119">Definition</span></span>

<span data-ttu-id="3ec72-120">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-120">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-121">A função `Func_austria_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-121">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ec72-122">Uma palavra-chave da `Keywords_austria_eu_tax_file_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="3ec72-122">A keyword from  `Keywords_austria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3ec72-123">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-123">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-124">A função `Func_austria_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-124">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="3ec72-125">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3ec72-125">Keywords</span></span>

#### <a name="keywordsaustriaeutaxfilenumber"></a><span data-ttu-id="3ec72-126">Keywords_austria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3ec72-126">Keywords_austria_eu_tax_file_number</span></span>

<span data-ttu-id="3ec72-127">número de imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-127">tax number</span></span>
  
<span data-ttu-id="3ec72-128">número</span><span class="sxs-lookup"><span data-stu-id="3ec72-128">number</span></span>
  
<span data-ttu-id="3ec72-129">número de inscrição</span><span class="sxs-lookup"><span data-stu-id="3ec72-129">tax registration number</span></span>
  
<span data-ttu-id="3ec72-130">tax id
</span><span class="sxs-lookup"><span data-stu-id="3ec72-130">tax id</span></span>
  
<span data-ttu-id="3ec72-131">St.nr.</span><span class="sxs-lookup"><span data-stu-id="3ec72-131">st.nr.</span></span>
  
<span data-ttu-id="3ec72-132">steuernummer</span><span class="sxs-lookup"><span data-stu-id="3ec72-132">steuernummer</span></span>
  
## <a name="belgium"></a><span data-ttu-id="3ec72-133">Bélgica</span><span class="sxs-lookup"><span data-stu-id="3ec72-133">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="3ec72-134">Formato</span><span class="sxs-lookup"><span data-stu-id="3ec72-134">Format</span></span>

<span data-ttu-id="3ec72-135">11 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="3ec72-135">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ec72-136">Padrão</span><span class="sxs-lookup"><span data-stu-id="3ec72-136">Pattern</span></span>

<span data-ttu-id="3ec72-137">11 dígitos:</span><span class="sxs-lookup"><span data-stu-id="3ec72-137">11 digits:</span></span>
  
- <span data-ttu-id="3ec72-138">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="3ec72-138">Two digits</span></span>
    
- <span data-ttu-id="3ec72-139">"0" ou "1"</span><span class="sxs-lookup"><span data-stu-id="3ec72-139">A "0" or "1"</span></span>
    
- <span data-ttu-id="3ec72-140">Um dígito</span><span class="sxs-lookup"><span data-stu-id="3ec72-140">One digit</span></span>
    
- <span data-ttu-id="3ec72-141">"0" ou "1" ou "2" ou "3"</span><span class="sxs-lookup"><span data-stu-id="3ec72-141">A "0" or "1" or "2" or "3"</span></span> 
    
- <span data-ttu-id="3ec72-142">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="3ec72-142">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="3ec72-143">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3ec72-143">Checksum</span></span>

<span data-ttu-id="3ec72-144">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="3ec72-144">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ec72-145">Definição</span><span class="sxs-lookup"><span data-stu-id="3ec72-145">Definition</span></span>

<span data-ttu-id="3ec72-146">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-146">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-147">A expressão regular `Regex_belgium_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-147">The regular expression  `Regex_belgium_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ec72-148">Uma palavra-chave da `Keywords_belgium_eu_tax_file_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="3ec72-148">A keyword from  `Keywords_belgium_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_tax_file_number" />
          <Match idRef="Keywords_belgium_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3ec72-149">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3ec72-149">Keywords</span></span>

#### <a name="keywordsbelgiumeutaxfilenumber"></a><span data-ttu-id="3ec72-150">Keywords_belgium_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3ec72-150">Keywords_belgium_eu_tax_file_number</span></span>

<span data-ttu-id="3ec72-151">número de imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-151">tax number</span></span>
  
<span data-ttu-id="3ec72-152">número de registro nacional</span><span class="sxs-lookup"><span data-stu-id="3ec72-152">national registration number</span></span>
  
<span data-ttu-id="3ec72-153">número de inscrição</span><span class="sxs-lookup"><span data-stu-id="3ec72-153">tax registration number</span></span>
  
<span data-ttu-id="3ec72-154">tax id
</span><span class="sxs-lookup"><span data-stu-id="3ec72-154">tax id</span></span>
  
<span data-ttu-id="3ec72-155">NIF</span><span class="sxs-lookup"><span data-stu-id="3ec72-155">nif</span></span>
  
<span data-ttu-id="3ec72-156">NIF #</span><span class="sxs-lookup"><span data-stu-id="3ec72-156">nif#</span></span>
  
<span data-ttu-id="3ec72-157">numéro de registre nacional</span><span class="sxs-lookup"><span data-stu-id="3ec72-157">numéro de registre national</span></span>
  
<span data-ttu-id="3ec72-158">numéro d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="3ec72-158">numéro d'identification fiscale</span></span>
  
## <a name="bulgaria"></a><span data-ttu-id="3ec72-159">Bulgária</span><span class="sxs-lookup"><span data-stu-id="3ec72-159">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="3ec72-160">Formato</span><span class="sxs-lookup"><span data-stu-id="3ec72-160">Format</span></span>

<span data-ttu-id="3ec72-161">Dez dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="3ec72-161">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ec72-162">Padrão</span><span class="sxs-lookup"><span data-stu-id="3ec72-162">Pattern</span></span>

<span data-ttu-id="3ec72-163">10 dígitos</span><span class="sxs-lookup"><span data-stu-id="3ec72-163">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="3ec72-164">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3ec72-164">Checksum</span></span>

<span data-ttu-id="3ec72-165">Sim</span><span class="sxs-lookup"><span data-stu-id="3ec72-165">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ec72-166">Definição</span><span class="sxs-lookup"><span data-stu-id="3ec72-166">Definition</span></span>

<span data-ttu-id="3ec72-167">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-167">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-168">A função `Func_bulgaria_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-168">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ec72-169">Uma palavra-chave da `Keywords_bulgaria_eu_tax_file_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="3ec72-169">A keyword from  `Keywords_bulgaria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3ec72-170">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-170">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-171">A função `Func_bulgaria_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-171">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="3ec72-172">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3ec72-172">Keywords</span></span>

#### <a name="keywordsbulgariaeutaxfilenumber"></a><span data-ttu-id="3ec72-173">Keywords_bulgaria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3ec72-173">Keywords_bulgaria_eu_tax_file_number</span></span>

<span data-ttu-id="3ec72-174">bucn</span><span class="sxs-lookup"><span data-stu-id="3ec72-174">bucn</span></span>
  
<span data-ttu-id="3ec72-175">número de civil Uniform</span><span class="sxs-lookup"><span data-stu-id="3ec72-175">uniform civil number</span></span>
  
<span data-ttu-id="3ec72-176">bucn #</span><span class="sxs-lookup"><span data-stu-id="3ec72-176">bucn#</span></span>
  
<span data-ttu-id="3ec72-177">uniformcivilnumber #</span><span class="sxs-lookup"><span data-stu-id="3ec72-177">uniformcivilnumber#</span></span>
  
<span data-ttu-id="3ec72-178">id de civil Uniform</span><span class="sxs-lookup"><span data-stu-id="3ec72-178">uniform civil id</span></span>
  
<span data-ttu-id="3ec72-179">Uniform não civil</span><span class="sxs-lookup"><span data-stu-id="3ec72-179">uniform civil no</span></span>
  
<span data-ttu-id="3ec72-180">egn</span><span class="sxs-lookup"><span data-stu-id="3ec72-180">egn</span></span>
  
<span data-ttu-id="3ec72-181">número de civil uniform búlgaro</span><span class="sxs-lookup"><span data-stu-id="3ec72-181">bulgarian uniform civil number</span></span>
  
<span data-ttu-id="3ec72-182">uniformcivilno #</span><span class="sxs-lookup"><span data-stu-id="3ec72-182">uniformcivilno#</span></span>
  
<span data-ttu-id="3ec72-183">egn #</span><span class="sxs-lookup"><span data-stu-id="3ec72-183">egn#</span></span>
  
<span data-ttu-id="3ec72-184">УНИФОРМ ГРАЖДАНСКИ НОМЕР</span><span class="sxs-lookup"><span data-stu-id="3ec72-184">униформ граждански номер</span></span>
  
<span data-ttu-id="3ec72-185">Id униформ</span><span class="sxs-lookup"><span data-stu-id="3ec72-185">униформ id</span></span>
  
<span data-ttu-id="3ec72-186">Id граждански униформ</span><span class="sxs-lookup"><span data-stu-id="3ec72-186">униформ граждански id</span></span>
  
<span data-ttu-id="3ec72-187">УНИФОРМ ГРАЖДАНСКИ НЕ</span><span class="sxs-lookup"><span data-stu-id="3ec72-187">униформ граждански не</span></span>
  
## <a name="croatia"></a><span data-ttu-id="3ec72-188">Croácia</span><span class="sxs-lookup"><span data-stu-id="3ec72-188">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="3ec72-189">Formato</span><span class="sxs-lookup"><span data-stu-id="3ec72-189">Format</span></span>

<span data-ttu-id="3ec72-190">11 dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="3ec72-190">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ec72-191">Padrão</span><span class="sxs-lookup"><span data-stu-id="3ec72-191">Pattern</span></span>

<span data-ttu-id="3ec72-192">11 dígitos:</span><span class="sxs-lookup"><span data-stu-id="3ec72-192">11 digits:</span></span>
  
- <span data-ttu-id="3ec72-193">Dez dígitos, escolhidos aleatoriamente</span><span class="sxs-lookup"><span data-stu-id="3ec72-193">Ten digits, randomly chosen</span></span>
    
- <span data-ttu-id="3ec72-194">Seleção de um dígito</span><span class="sxs-lookup"><span data-stu-id="3ec72-194">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="3ec72-195">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3ec72-195">Checksum</span></span>

<span data-ttu-id="3ec72-196">Sim</span><span class="sxs-lookup"><span data-stu-id="3ec72-196">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ec72-197">Definição</span><span class="sxs-lookup"><span data-stu-id="3ec72-197">Definition</span></span>

<span data-ttu-id="3ec72-198">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-198">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-199">A função `Func_croatia_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-199">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ec72-200">Uma palavra-chave da `Keywords_croatia_eu_tax_file_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="3ec72-200">A keyword from  `Keywords_croatia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3ec72-201">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-201">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-202">A função `Func_croatia_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-202">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="3ec72-203">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3ec72-203">Keywords</span></span>

#### <a name="keywordscroatiaeutaxfilenumber"></a><span data-ttu-id="3ec72-204">Keywords_croatia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3ec72-204">Keywords_croatia_eu_tax_file_number</span></span>

<span data-ttu-id="3ec72-205">número de imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-205">tax number</span></span>
  
<span data-ttu-id="3ec72-206">imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-206">tax</span></span>
  
<span data-ttu-id="3ec72-207">tax id
</span><span class="sxs-lookup"><span data-stu-id="3ec72-207">tax id</span></span>
  
<span data-ttu-id="3ec72-208">identificação de objeto</span><span class="sxs-lookup"><span data-stu-id="3ec72-208">oid</span></span>
  
<span data-ttu-id="3ec72-209">identificação de objeto #</span><span class="sxs-lookup"><span data-stu-id="3ec72-209">oid#</span></span>
  
<span data-ttu-id="3ec72-210">porezni broj</span><span class="sxs-lookup"><span data-stu-id="3ec72-210">porezni broj</span></span>
  
## <a name="cyprus"></a><span data-ttu-id="3ec72-211">Chipre</span><span class="sxs-lookup"><span data-stu-id="3ec72-211">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="3ec72-212">Formato</span><span class="sxs-lookup"><span data-stu-id="3ec72-212">Format</span></span>

<span data-ttu-id="3ec72-213">Oito dígitos e uma letra no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="3ec72-213">Eight digits and one letter in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ec72-214">Padrão</span><span class="sxs-lookup"><span data-stu-id="3ec72-214">Pattern</span></span>

<span data-ttu-id="3ec72-215">Oito dígitos e uma letra:</span><span class="sxs-lookup"><span data-stu-id="3ec72-215">Eight digits and one letter:</span></span>
  
-  <span data-ttu-id="3ec72-216">"0"</span><span class="sxs-lookup"><span data-stu-id="3ec72-216">A "0"</span></span> 
    
- <span data-ttu-id="3ec72-217">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="3ec72-217">Seven digits</span></span>
    
- <span data-ttu-id="3ec72-218">Uma letra (não diferencia maiusculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="3ec72-218">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="3ec72-219">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3ec72-219">Checksum</span></span>

<span data-ttu-id="3ec72-220">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="3ec72-220">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ec72-221">Definição</span><span class="sxs-lookup"><span data-stu-id="3ec72-221">Definition</span></span>

<span data-ttu-id="3ec72-222">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-222">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-223">A função `Func_cyprus_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-223">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ec72-224">Uma palavra-chave da `Keywords_cyprus_eu_tax_file_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="3ec72-224">A keyword from  `Keywords_cyprus_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3ec72-225">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-225">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-226">A função `Func_cyprus_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-226">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="3ec72-227">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3ec72-227">Keywords</span></span>

#### <a name="keywordscypruseutaxfilenumber"></a><span data-ttu-id="3ec72-228">Keywords_cyprus_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3ec72-228">Keywords_cyprus_eu_tax_file_number</span></span>

<span data-ttu-id="3ec72-229">número de imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-229">tax number</span></span>
  
<span data-ttu-id="3ec72-230">imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-230">tax</span></span>
  
<span data-ttu-id="3ec72-231">tax id
</span><span class="sxs-lookup"><span data-stu-id="3ec72-231">tax id</span></span>
  
<span data-ttu-id="3ec72-232">código de identificação de imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-232">tax identification code</span></span>
  
<span data-ttu-id="3ec72-233">velha</span><span class="sxs-lookup"><span data-stu-id="3ec72-233">tic</span></span>
  
<span data-ttu-id="3ec72-234">velha #</span><span class="sxs-lookup"><span data-stu-id="3ec72-234">tic#</span></span>
  
<span data-ttu-id="3ec72-235">ΑΡΙΘΜΌΣ ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ</span><span class="sxs-lookup"><span data-stu-id="3ec72-235">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="3ec72-236">ΦΟΡΟΛΟΓΙΚΉ ΤΑΥΤΌΤΗΤΑ</span><span class="sxs-lookup"><span data-stu-id="3ec72-236">φορολογική ταυτότητα</span></span>
  
<span data-ttu-id="3ec72-237">ΚΩΔΙΚΌΣ ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ</span><span class="sxs-lookup"><span data-stu-id="3ec72-237">κωδικός φορολογικού μητρώου</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="3ec72-238">República Tcheca</span><span class="sxs-lookup"><span data-stu-id="3ec72-238">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="3ec72-239">Formato</span><span class="sxs-lookup"><span data-stu-id="3ec72-239">Format</span></span>

<span data-ttu-id="3ec72-240">Nove ou dez dígitos com uma barra invertida a opcional</span><span class="sxs-lookup"><span data-stu-id="3ec72-240">Nine or ten digits with an optional backslash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ec72-241">Padrão</span><span class="sxs-lookup"><span data-stu-id="3ec72-241">Pattern</span></span>

<span data-ttu-id="3ec72-242">Nove ou dez dígitos com um backslashl opcional:</span><span class="sxs-lookup"><span data-stu-id="3ec72-242">Nine or ten digits with an optional backslashl:</span></span>
  
- <span data-ttu-id="3ec72-243">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="3ec72-243">Six digits</span></span> 
    
- <span data-ttu-id="3ec72-244">Uma barra invertida (opcional)</span><span class="sxs-lookup"><span data-stu-id="3ec72-244">A backslash (optional)</span></span>
    
- <span data-ttu-id="3ec72-245">Três ou quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="3ec72-245">Three or four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="3ec72-246">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3ec72-246">Checksum</span></span>

<span data-ttu-id="3ec72-247">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="3ec72-247">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ec72-248">Definição</span><span class="sxs-lookup"><span data-stu-id="3ec72-248">Definition</span></span>

<span data-ttu-id="3ec72-249">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-249">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-250">A expressão regular `Regex_czech_republic_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-250">The regular expression  `Regex_czech_republic_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ec72-251">Uma palavra-chave da `Keywords_czech_republic_eu_tax_file_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="3ec72-251">A keyword from  `Keywords_czech_republic_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_tax_file_number" />
          <Match idRef="Keywords_czech_republic_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3ec72-252">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3ec72-252">Keywords</span></span>

#### <a name="keywordsczechrepubliceutaxfilenumber"></a><span data-ttu-id="3ec72-253">Keywords_czech_republic_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3ec72-253">Keywords_czech_republic_eu_tax_file_number</span></span>

<span data-ttu-id="3ec72-254">número de imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-254">tax number</span></span>
  
<span data-ttu-id="3ec72-255">imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-255">tax</span></span>
  
<span data-ttu-id="3ec72-256">tax id
</span><span class="sxs-lookup"><span data-stu-id="3ec72-256">tax id</span></span>
  
<span data-ttu-id="3ec72-257">número de pessoal</span><span class="sxs-lookup"><span data-stu-id="3ec72-257">personal number</span></span>
  
<span data-ttu-id="3ec72-258">daňové číslo</span><span class="sxs-lookup"><span data-stu-id="3ec72-258">daňové číslo</span></span>
  
<span data-ttu-id="3ec72-259">osobní číslo</span><span class="sxs-lookup"><span data-stu-id="3ec72-259">osobní číslo</span></span>
  
## <a name="denmark"></a><span data-ttu-id="3ec72-260">Dinamarca</span><span class="sxs-lookup"><span data-stu-id="3ec72-260">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="3ec72-261">Formato</span><span class="sxs-lookup"><span data-stu-id="3ec72-261">Format</span></span>

<span data-ttu-id="3ec72-262">Dez dígitos que contém um hífen</span><span class="sxs-lookup"><span data-stu-id="3ec72-262">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ec72-263">Padrão</span><span class="sxs-lookup"><span data-stu-id="3ec72-263">Pattern</span></span>

<span data-ttu-id="3ec72-264">Dez dígitos que contém um hyphenl:</span><span class="sxs-lookup"><span data-stu-id="3ec72-264">Ten digits containing a hyphenl:</span></span>
  
-  <span data-ttu-id="3ec72-265">Seis dígitos que correspondem à data de nascimento (DDMMYY)</span><span class="sxs-lookup"><span data-stu-id="3ec72-265">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="3ec72-266">Um hífen</span><span class="sxs-lookup"><span data-stu-id="3ec72-266">A hyphen</span></span>
    
- <span data-ttu-id="3ec72-267">Quatro dígitos que correspondem a um número de sequência em que o primeiro dígito corresponde como o century de nascimento e o último dígito corresponde ao gênero do indivíduo (ímpar para masculino e até mesmo fêmea)</span><span class="sxs-lookup"><span data-stu-id="3ec72-267">Four digits that correspond to a sequence number where the first digit corresponds to the century of birth and the last digit corresponds to the individual's gender (odd for male and even for female)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="3ec72-268">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3ec72-268">Checksum</span></span>

<span data-ttu-id="3ec72-269">Sim</span><span class="sxs-lookup"><span data-stu-id="3ec72-269">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ec72-270">Definição</span><span class="sxs-lookup"><span data-stu-id="3ec72-270">Definition</span></span>

<span data-ttu-id="3ec72-271">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-271">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-272">A função `Func_denmark_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-272">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ec72-273">Uma palavra-chave da `Keywords_denmark_eu_tax_file_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="3ec72-273">A keyword from  `Keywords_denmark_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3ec72-274">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-275">A função `Func_denmark_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-275">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="3ec72-276">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3ec72-276">Keywords</span></span>

#### <a name="keywordsdenmarkeutaxfilenumber"></a><span data-ttu-id="3ec72-277">Keywords_denmark_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3ec72-277">Keywords_denmark_eu_tax_file_number</span></span>

<span data-ttu-id="3ec72-278">número de imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-278">tax number</span></span>
  
<span data-ttu-id="3ec72-279">imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-279">tax</span></span>
  
<span data-ttu-id="3ec72-280">tax id
</span><span class="sxs-lookup"><span data-stu-id="3ec72-280">tax id</span></span>
  
<span data-ttu-id="3ec72-281">número de CPR</span><span class="sxs-lookup"><span data-stu-id="3ec72-281">cpr number</span></span>
  
<span data-ttu-id="3ec72-282">CPR #</span><span class="sxs-lookup"><span data-stu-id="3ec72-282">cpr#</span></span>
  
<span data-ttu-id="3ec72-283">skat nummer</span><span class="sxs-lookup"><span data-stu-id="3ec72-283">skat nummer</span></span>
  
<span data-ttu-id="3ec72-284">id de skat</span><span class="sxs-lookup"><span data-stu-id="3ec72-284">skat id</span></span>
  
## <a name="estonia"></a><span data-ttu-id="3ec72-285">Estônia</span><span class="sxs-lookup"><span data-stu-id="3ec72-285">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="3ec72-286">Formato</span><span class="sxs-lookup"><span data-stu-id="3ec72-286">Format</span></span>

<span data-ttu-id="3ec72-287">11 dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="3ec72-287">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ec72-288">Padrão</span><span class="sxs-lookup"><span data-stu-id="3ec72-288">Pattern</span></span>

<span data-ttu-id="3ec72-289">11 dígitos:</span><span class="sxs-lookup"><span data-stu-id="3ec72-289">11 digits:</span></span>
  
-  <span data-ttu-id="3ec72-290">Um dígito que corresponde ao gênero e century de nascimento onde um número ímpar indica masculino e o número par fêmea da seguinte maneira: 1, 2 para o décimo nono century; 3, 4 para o century 20; e 5, 6 para o century 21</span><span class="sxs-lookup"><span data-stu-id="3ec72-290">One digit that corresponds to gender and century of birth where an odd number indicates male and the even number indicates female as follows: 1, 2 for the 19th century; 3, 4 for the 20th century; and 5, 6 for the 21st century</span></span> 
    
- <span data-ttu-id="3ec72-291">Seis dígitos que correspondem à data de nascimento (aammdd)</span><span class="sxs-lookup"><span data-stu-id="3ec72-291">Six digits that correspond to birth date (YYMMDD)</span></span>
    
- <span data-ttu-id="3ec72-292">Três dígitos que correspondem a um número de série separando pessoas nascidas na mesma data</span><span class="sxs-lookup"><span data-stu-id="3ec72-292">Three digits that correspond to a serial number separating persons born on the same date</span></span>
    
- <span data-ttu-id="3ec72-293">Seleção de um dígito</span><span class="sxs-lookup"><span data-stu-id="3ec72-293">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="3ec72-294">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3ec72-294">Checksum</span></span>

<span data-ttu-id="3ec72-295">Sim</span><span class="sxs-lookup"><span data-stu-id="3ec72-295">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ec72-296">Definição</span><span class="sxs-lookup"><span data-stu-id="3ec72-296">Definition</span></span>

<span data-ttu-id="3ec72-297">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-297">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-298">A função `Func_estonia_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-298">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ec72-299">Uma palavra-chave da `Keywords_estonia_eu_tax_file_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="3ec72-299">A keyword from  `Keywords_estonia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3ec72-300">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-300">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-301">A função `Func_estonia_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-301">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="3ec72-302">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3ec72-302">Keywords</span></span>

#### <a name="keywordsestoniaeutaxfilenumber"></a><span data-ttu-id="3ec72-303">Keywords_estonia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3ec72-303">Keywords_estonia_eu_tax_file_number</span></span>

<span data-ttu-id="3ec72-304">número de imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-304">tax number</span></span>
  
<span data-ttu-id="3ec72-305">imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-305">tax</span></span>
  
<span data-ttu-id="3ec72-306">tax id
</span><span class="sxs-lookup"><span data-stu-id="3ec72-306">tax id</span></span>
  
<span data-ttu-id="3ec72-307">código pessoal</span><span class="sxs-lookup"><span data-stu-id="3ec72-307">personal code</span></span>
  
<span data-ttu-id="3ec72-308">maksunumber</span><span class="sxs-lookup"><span data-stu-id="3ec72-308">maksunumber</span></span>
  
<span data-ttu-id="3ec72-309">id de maksu</span><span class="sxs-lookup"><span data-stu-id="3ec72-309">maksu id</span></span>
  
<span data-ttu-id="3ec72-310">isikukood</span><span class="sxs-lookup"><span data-stu-id="3ec72-310">isikukood</span></span>
  
## <a name="finland"></a><span data-ttu-id="3ec72-311">Finlândia</span><span class="sxs-lookup"><span data-stu-id="3ec72-311">Finland</span></span>

### <a name="format"></a><span data-ttu-id="3ec72-312">Formato</span><span class="sxs-lookup"><span data-stu-id="3ec72-312">Format</span></span>

<span data-ttu-id="3ec72-313">Uma combinação de 11 caracteres de dígitos, letras, e mais e menos de entrada</span><span class="sxs-lookup"><span data-stu-id="3ec72-313">An 11-character combination of digits, letters, and plus and minus sign</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ec72-314">Padrão</span><span class="sxs-lookup"><span data-stu-id="3ec72-314">Pattern</span></span>

<span data-ttu-id="3ec72-315">Uma combinação de 11 caracteres de dígitos, letras, e mais e menos entrada:</span><span class="sxs-lookup"><span data-stu-id="3ec72-315">An 11-character combination of digits, letters, and plus and minus sign:</span></span>
  
- <span data-ttu-id="3ec72-316">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="3ec72-316">Six digits</span></span>
    
- <span data-ttu-id="3ec72-317">Um dos seguintes: um sinal de adição, um sinal de subtração ou a letra "A" (não diferenciar maiusculas de minúsculas) onde o sinal de adição significa nascer entre 1800-1899, o sinal de menos assinar significa nascer entre 1900-1999 e "A" significa Nascida 2000 e depois</span><span class="sxs-lookup"><span data-stu-id="3ec72-317">One of the following: a plus sign, a minus sign, or the letter "A" (not case sensitive) where the plus sign means born between 1800-1899, the minus sign means born between 1900-1999, and "A" means born 2000 and after</span></span>
    
- <span data-ttu-id="3ec72-318">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="3ec72-318">Three digits</span></span>
    
- <span data-ttu-id="3ec72-319">Uma letra ou um número</span><span class="sxs-lookup"><span data-stu-id="3ec72-319">One letter or one number</span></span>
    
### <a name="checksum"></a><span data-ttu-id="3ec72-320">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3ec72-320">Checksum</span></span>

<span data-ttu-id="3ec72-321">Sim</span><span class="sxs-lookup"><span data-stu-id="3ec72-321">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ec72-322">Definição</span><span class="sxs-lookup"><span data-stu-id="3ec72-322">Definition</span></span>

<span data-ttu-id="3ec72-323">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-323">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-324">A função `Func_finland_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-324">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ec72-325">Uma palavra-chave da `Keywords_finland_eu_tax_file_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="3ec72-325">A keyword from  `Keywords_finland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3ec72-326">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-326">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-327">A função `Func_finland_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-327">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="3ec72-328">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3ec72-328">Keywords</span></span>

#### <a name="keywordsfinlandeutaxfilenumber"></a><span data-ttu-id="3ec72-329">Keywords_finland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3ec72-329">Keywords_finland_eu_tax_file_number</span></span>

<span data-ttu-id="3ec72-330">identification number
</span><span class="sxs-lookup"><span data-stu-id="3ec72-330">identification number</span></span>
  
<span data-ttu-id="3ec72-331">identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="3ec72-331">personal id</span></span>
  
<span data-ttu-id="3ec72-332">número de identidade</span><span class="sxs-lookup"><span data-stu-id="3ec72-332">identity number</span></span>
  
<span data-ttu-id="3ec72-333">número de identificação nacional finlandês</span><span class="sxs-lookup"><span data-stu-id="3ec72-333">finnish national id number</span></span>
  
<span data-ttu-id="3ec72-334">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="3ec72-334">personalidnumber#</span></span>
  
<span data-ttu-id="3ec72-335">número de identificação nacional</span><span class="sxs-lookup"><span data-stu-id="3ec72-335">national identification number</span></span>
  
<span data-ttu-id="3ec72-336">número de identificação</span><span class="sxs-lookup"><span data-stu-id="3ec72-336">id number</span></span>
  
<span data-ttu-id="3ec72-337">id nacional nenhum.</span><span class="sxs-lookup"><span data-stu-id="3ec72-337">national id no.</span></span>
  
<span data-ttu-id="3ec72-338">número de identificação nacional</span><span class="sxs-lookup"><span data-stu-id="3ec72-338">national id number</span></span>
  
<span data-ttu-id="3ec72-339">ID nenhum</span><span class="sxs-lookup"><span data-stu-id="3ec72-339">id no</span></span>
  
<span data-ttu-id="3ec72-340">tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="3ec72-340">tunnistenumero</span></span>
  
<span data-ttu-id="3ec72-341">henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="3ec72-341">henkilötunnus</span></span>
  
<span data-ttu-id="3ec72-342">yksilöllinen henkilökohtainen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="3ec72-342">yksilöllinen henkilökohtainen tunnistenumero</span></span>
  
<span data-ttu-id="3ec72-343">ainutlaatuinen henkilökohtainen tunnus</span><span class="sxs-lookup"><span data-stu-id="3ec72-343">ainutlaatuinen henkilökohtainen tunnus</span></span>
  
<span data-ttu-id="3ec72-344">numero identiteetti</span><span class="sxs-lookup"><span data-stu-id="3ec72-344">identiteetti numero</span></span>
  
<span data-ttu-id="3ec72-345">suomen kansallinen henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="3ec72-345">suomen kansallinen henkilötunnus</span></span>
  
<span data-ttu-id="3ec72-346">henkilötunnusnumero #</span><span class="sxs-lookup"><span data-stu-id="3ec72-346">henkilötunnusnumero#</span></span>
  
<span data-ttu-id="3ec72-347">kansallisen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="3ec72-347">kansallisen tunnistenumero</span></span>
  
<span data-ttu-id="3ec72-348">tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="3ec72-348">tunnusnumero</span></span>
  
<span data-ttu-id="3ec72-349">kansallinen tunnus numero</span><span class="sxs-lookup"><span data-stu-id="3ec72-349">kansallinen tunnus numero</span></span>
  
## <a name="france"></a><span data-ttu-id="3ec72-350">França</span><span class="sxs-lookup"><span data-stu-id="3ec72-350">France</span></span>

### <a name="format"></a><span data-ttu-id="3ec72-351">Formato</span><span class="sxs-lookup"><span data-stu-id="3ec72-351">Format</span></span>

<span data-ttu-id="3ec72-352">13 dígitos dos indivíduos e nove dígitos para entidades</span><span class="sxs-lookup"><span data-stu-id="3ec72-352">13 digits for individuals and nine digits for entities</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ec72-353">Padrão</span><span class="sxs-lookup"><span data-stu-id="3ec72-353">Pattern</span></span>

<span data-ttu-id="3ec72-354">13 dígitos para as pessoas:</span><span class="sxs-lookup"><span data-stu-id="3ec72-354">13 digits for individuals:</span></span>
  
- <span data-ttu-id="3ec72-355">Um dígito que deve ser 0, 1, 2 ou 3</span><span class="sxs-lookup"><span data-stu-id="3ec72-355">One digit that must be 0, 1, 2, or 3</span></span>
    
- <span data-ttu-id="3ec72-356">12 dígitos</span><span class="sxs-lookup"><span data-stu-id="3ec72-356">12 digits</span></span>
    
<span data-ttu-id="3ec72-357">Nove dígitos para entidades</span><span class="sxs-lookup"><span data-stu-id="3ec72-357">Nine digits for entities</span></span>
  
### <a name="checksum"></a><span data-ttu-id="3ec72-358">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3ec72-358">Checksum</span></span>

<span data-ttu-id="3ec72-359">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="3ec72-359">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ec72-360">Definição</span><span class="sxs-lookup"><span data-stu-id="3ec72-360">Definition</span></span>

<span data-ttu-id="3ec72-361">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-361">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-362">A função `Func_france_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-362">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ec72-363">Uma palavra-chave da `Keywords_france_eu_tax_file_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="3ec72-363">A keyword from  `Keywords_france_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3ec72-364">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-365">A função `Func_france_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-365">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="3ec72-366">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3ec72-366">Keywords</span></span>

#### <a name="keywordsfranceeutaxfilenumber"></a><span data-ttu-id="3ec72-367">Keywords_france_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3ec72-367">Keywords_france_eu_tax_file_number</span></span>

<span data-ttu-id="3ec72-368">número de identificação de imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-368">tax identification number</span></span>
  
<span data-ttu-id="3ec72-369">número de imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-369">tax number</span></span>
  
<span data-ttu-id="3ec72-370">tax id
</span><span class="sxs-lookup"><span data-stu-id="3ec72-370">tax id</span></span>
  
<span data-ttu-id="3ec72-371">numéro d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="3ec72-371">numéro d'identification fiscale</span></span>
  
## <a name="germany"></a><span data-ttu-id="3ec72-372">Alemanha</span><span class="sxs-lookup"><span data-stu-id="3ec72-372">Germany</span></span>

### <a name="format"></a><span data-ttu-id="3ec72-373">Formato</span><span class="sxs-lookup"><span data-stu-id="3ec72-373">Format</span></span>

<span data-ttu-id="3ec72-374">11 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="3ec72-374">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ec72-375">Padrão</span><span class="sxs-lookup"><span data-stu-id="3ec72-375">Pattern</span></span>

<span data-ttu-id="3ec72-376">11 dígitos:</span><span class="sxs-lookup"><span data-stu-id="3ec72-376">11 digits :</span></span>
  
-  <span data-ttu-id="3ec72-377">Dez dígitos</span><span class="sxs-lookup"><span data-stu-id="3ec72-377">Ten digits</span></span> 
    
- <span data-ttu-id="3ec72-378">Seleção de um dígito</span><span class="sxs-lookup"><span data-stu-id="3ec72-378">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="3ec72-379">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3ec72-379">Checksum</span></span>

<span data-ttu-id="3ec72-380">Sim</span><span class="sxs-lookup"><span data-stu-id="3ec72-380">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ec72-381">Definição</span><span class="sxs-lookup"><span data-stu-id="3ec72-381">Definition</span></span>

<span data-ttu-id="3ec72-382">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-382">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-383">A função `Func_germany_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-383">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ec72-384">Uma palavra-chave da `Keywords_germany_eu_tax_file_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="3ec72-384">A keyword from  `Keywords_germany_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3ec72-385">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-385">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-386">A função `Func_germany_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-386">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="3ec72-387">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3ec72-387">Keywords</span></span>

#### <a name="keywordsgermanyeutaxfilenumber"></a><span data-ttu-id="3ec72-388">Keywords_germany_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3ec72-388">Keywords_germany_eu_tax_file_number</span></span>

<span data-ttu-id="3ec72-389">número de imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-389">tax number</span></span>
  
<span data-ttu-id="3ec72-390">imposto não.</span><span class="sxs-lookup"><span data-stu-id="3ec72-390">tax no.</span></span>
  
<span data-ttu-id="3ec72-391">taxno #</span><span class="sxs-lookup"><span data-stu-id="3ec72-391">taxno#</span></span>
  
<span data-ttu-id="3ec72-392">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="3ec72-392">taxnumber#</span></span>
  
<span data-ttu-id="3ec72-393">taxnumber</span><span class="sxs-lookup"><span data-stu-id="3ec72-393">taxnumber</span></span>
  
<span data-ttu-id="3ec72-394">tax id
</span><span class="sxs-lookup"><span data-stu-id="3ec72-394">tax id</span></span>
  
<span data-ttu-id="3ec72-395">taxid #</span><span class="sxs-lookup"><span data-stu-id="3ec72-395">taxid#</span></span>
  
<span data-ttu-id="3ec72-396">número de identificação de imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-396">tax identification number</span></span>
  
<span data-ttu-id="3ec72-397">identificação de imposto não.</span><span class="sxs-lookup"><span data-stu-id="3ec72-397">tax identification no.</span></span>
  
<span data-ttu-id="3ec72-398">steuernummer</span><span class="sxs-lookup"><span data-stu-id="3ec72-398">steuernummer</span></span>
  
<span data-ttu-id="3ec72-399">id de steuer</span><span class="sxs-lookup"><span data-stu-id="3ec72-399">steuer id</span></span>
  
<span data-ttu-id="3ec72-400">steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="3ec72-400">steueridentifikationsnummer</span></span>
  
## <a name="greece"></a><span data-ttu-id="3ec72-401">Grécia</span><span class="sxs-lookup"><span data-stu-id="3ec72-401">Greece</span></span>

### <a name="format"></a><span data-ttu-id="3ec72-402">Formato</span><span class="sxs-lookup"><span data-stu-id="3ec72-402">Format</span></span>

<span data-ttu-id="3ec72-403">Nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="3ec72-403">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ec72-404">Padrão</span><span class="sxs-lookup"><span data-stu-id="3ec72-404">Pattern</span></span>

<span data-ttu-id="3ec72-405">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="3ec72-405">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="3ec72-406">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3ec72-406">Checksum</span></span>

<span data-ttu-id="3ec72-407">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="3ec72-407">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ec72-408">Definição</span><span class="sxs-lookup"><span data-stu-id="3ec72-408">Definition</span></span>

<span data-ttu-id="3ec72-409">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-409">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-410">A expressão regular `Regex_greece_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-410">The regular expression  `Regex_greece_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ec72-411">Uma palavra-chave da `Keywords_greece_eu_tax_file_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="3ec72-411">A keyword from  `Keywords_greece_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_tax_file_number" />
          <Match idRef="Keywords_greece_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3ec72-412">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3ec72-412">Keywords</span></span>

#### <a name="keywordsgreeceeutaxfilenumber"></a><span data-ttu-id="3ec72-413">Keywords_greece_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3ec72-413">Keywords_greece_eu_tax_file_number</span></span>

<span data-ttu-id="3ec72-414">AFM</span><span class="sxs-lookup"><span data-stu-id="3ec72-414">afm</span></span>
  
<span data-ttu-id="3ec72-415">tin
</span><span class="sxs-lookup"><span data-stu-id="3ec72-415">tin</span></span>
  
<span data-ttu-id="3ec72-416">id de imposto não.</span><span class="sxs-lookup"><span data-stu-id="3ec72-416">tax id no.</span></span>
  
<span data-ttu-id="3ec72-417">id de imposto não</span><span class="sxs-lookup"><span data-stu-id="3ec72-417">tax id no</span></span>
  
<span data-ttu-id="3ec72-418">número de identificação de imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-418">tax identification number</span></span>
  
<span data-ttu-id="3ec72-419">número de registro de imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-419">tax registry number</span></span>
  
<span data-ttu-id="3ec72-420">imposto do registro não.</span><span class="sxs-lookup"><span data-stu-id="3ec72-420">tax registry no.</span></span>
  
<span data-ttu-id="3ec72-421">AFM #</span><span class="sxs-lookup"><span data-stu-id="3ec72-421">afm#</span></span>
  
<span data-ttu-id="3ec72-422">TIN #</span><span class="sxs-lookup"><span data-stu-id="3ec72-422">tin#</span></span>
  
<span data-ttu-id="3ec72-423">taxidno #</span><span class="sxs-lookup"><span data-stu-id="3ec72-423">taxidno#</span></span>
  
<span data-ttu-id="3ec72-424">taxregistryno #</span><span class="sxs-lookup"><span data-stu-id="3ec72-424">taxregistryno#</span></span>
  
<span data-ttu-id="3ec72-425">ΑΡΙΘΜΌΣ ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ</span><span class="sxs-lookup"><span data-stu-id="3ec72-425">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="3ec72-426">aφμ</span><span class="sxs-lookup"><span data-stu-id="3ec72-426">aφμ</span></span>
  
<span data-ttu-id="3ec72-427">aφμ αριθμός</span><span class="sxs-lookup"><span data-stu-id="3ec72-427">aφμ αριθμός</span></span>
  
<span data-ttu-id="3ec72-428">ΝΟ DE ΜΗΤΡΏΟΥ ΦΟΡΟΛΟΓΙΚΟΎ.</span><span class="sxs-lookup"><span data-stu-id="3ec72-428">φορολογικού μητρώου νο.</span></span>
  
<span data-ttu-id="3ec72-429">ΤΟΝ ΑΡΙΘΜΌ ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ</span><span class="sxs-lookup"><span data-stu-id="3ec72-429">τον αριθμό φορολογικού μητρώου</span></span>
  
## <a name="hungary"></a><span data-ttu-id="3ec72-430">Hungria</span><span class="sxs-lookup"><span data-stu-id="3ec72-430">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="3ec72-431">Formato</span><span class="sxs-lookup"><span data-stu-id="3ec72-431">Format</span></span>

<span data-ttu-id="3ec72-432">Dez dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="3ec72-432">Ten digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ec72-433">Padrão</span><span class="sxs-lookup"><span data-stu-id="3ec72-433">Pattern</span></span>

<span data-ttu-id="3ec72-434">Dez dígitos:</span><span class="sxs-lookup"><span data-stu-id="3ec72-434">Ten digits:</span></span>
  
-  <span data-ttu-id="3ec72-435">Um dígito que deve estar "8"</span><span class="sxs-lookup"><span data-stu-id="3ec72-435">One digit that must be "8"</span></span> 
    
- <span data-ttu-id="3ec72-436">Cinco dígitos que corresponde ao número de dias entre a data 01/01/1867 e a data do nascimento do indivíduo</span><span class="sxs-lookup"><span data-stu-id="3ec72-436">Five digits that correspond to the number of days between the date 01/01/1867 and the date of the birth of the individual</span></span>
    
- <span data-ttu-id="3ec72-437">Três dígitos que corresponde ao número gerado por acaso para diferenciar indivíduos nascidos no mesmo dia</span><span class="sxs-lookup"><span data-stu-id="3ec72-437">Three digits that correspond to the number generated by chance to differentiate individuals born on the same day</span></span>
    
- <span data-ttu-id="3ec72-438">Seleção de um dígito</span><span class="sxs-lookup"><span data-stu-id="3ec72-438">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="3ec72-439">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3ec72-439">Checksum</span></span>

<span data-ttu-id="3ec72-440">Sim</span><span class="sxs-lookup"><span data-stu-id="3ec72-440">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ec72-441">Definição</span><span class="sxs-lookup"><span data-stu-id="3ec72-441">Definition</span></span>

<span data-ttu-id="3ec72-442">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-442">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-443">A função `Func_hungary_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-443">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ec72-444">Uma palavra-chave da `Keywords_hungary_eu_tax_file_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="3ec72-444">A keyword from  `Keywords_hungary_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3ec72-445">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-445">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-446">A função `Func_hungary_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-446">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="3ec72-447">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3ec72-447">Keywords</span></span>

#### <a name="keywordshungaryeutaxfilenumber"></a><span data-ttu-id="3ec72-448">Keywords_hungary_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3ec72-448">Keywords_hungary_eu_tax_file_number</span></span>

<span data-ttu-id="3ec72-449">número de identificação de imposto húngaro</span><span class="sxs-lookup"><span data-stu-id="3ec72-449">hungarian tax identification number</span></span>
  
<span data-ttu-id="3ec72-450">tin húngaro</span><span class="sxs-lookup"><span data-stu-id="3ec72-450">hungarian tin</span></span>
  
<span data-ttu-id="3ec72-451">número de identificação de imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-451">tax id number</span></span>
  
<span data-ttu-id="3ec72-452">número VAT</span><span class="sxs-lookup"><span data-stu-id="3ec72-452">vat number</span></span>
  
<span data-ttu-id="3ec72-453">autoridade de fiscal não</span><span class="sxs-lookup"><span data-stu-id="3ec72-453">tax authority no</span></span>
  
<span data-ttu-id="3ec72-454">número de identidade de imposto de id de imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-454">tax id tax identity number</span></span>
  
<span data-ttu-id="3ec72-455">taxidnumber #</span><span class="sxs-lookup"><span data-stu-id="3ec72-455">taxidnumber#</span></span>
  
<span data-ttu-id="3ec72-456">TIN #</span><span class="sxs-lookup"><span data-stu-id="3ec72-456">tin#</span></span>
  
<span data-ttu-id="3ec72-457">hungatiantin #</span><span class="sxs-lookup"><span data-stu-id="3ec72-457">hungatiantin#</span></span>
  
<span data-ttu-id="3ec72-458">identificação de imposto não</span><span class="sxs-lookup"><span data-stu-id="3ec72-458">tax identification no</span></span>
  
<span data-ttu-id="3ec72-459">taxidno #</span><span class="sxs-lookup"><span data-stu-id="3ec72-459">taxidno#</span></span>
  
<span data-ttu-id="3ec72-460">adóazonosító szám</span><span class="sxs-lookup"><span data-stu-id="3ec72-460">adóazonosító szám</span></span>
  
<span data-ttu-id="3ec72-461">adószám</span><span class="sxs-lookup"><span data-stu-id="3ec72-461">adószám</span></span>
  
<span data-ttu-id="3ec72-462">adóhatóság szám</span><span class="sxs-lookup"><span data-stu-id="3ec72-462">adóhatóság szám</span></span>
  
## <a name="ireland"></a><span data-ttu-id="3ec72-463">Irlanda</span><span class="sxs-lookup"><span data-stu-id="3ec72-463">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="3ec72-464">Formato</span><span class="sxs-lookup"><span data-stu-id="3ec72-464">Format</span></span>

<span data-ttu-id="3ec72-465">Sete dígitos, seguidos por uma letra sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="3ec72-465">Seven digits followed by a letter with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ec72-466">Padrão</span><span class="sxs-lookup"><span data-stu-id="3ec72-466">Pattern</span></span>

<span data-ttu-id="3ec72-467">Sete dígitos seguidos por uma letra:</span><span class="sxs-lookup"><span data-stu-id="3ec72-467">Seven digits followed by a letter:</span></span>
  
-  <span data-ttu-id="3ec72-468">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="3ec72-468">Seven digits</span></span> 
    
- <span data-ttu-id="3ec72-469">Uma letra (não diferencia maiusculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="3ec72-469">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="3ec72-470">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3ec72-470">Checksum</span></span>

<span data-ttu-id="3ec72-471">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="3ec72-471">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ec72-472">Definição</span><span class="sxs-lookup"><span data-stu-id="3ec72-472">Definition</span></span>

<span data-ttu-id="3ec72-473">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-473">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-474">A função `Func_ireland_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-474">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ec72-475">Uma palavra-chave da `Keywords_ireland_eu_tax_file_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="3ec72-475">A keyword from  `Keywords_ireland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3ec72-476">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-476">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-477">A função `Func_ireland_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-477">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="3ec72-478">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3ec72-478">Keywords</span></span>

#### <a name="keywordsirelandeutaxfilenumber"></a><span data-ttu-id="3ec72-479">Keywords_ireland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3ec72-479">Keywords_ireland_eu_tax_file_number</span></span>

<span data-ttu-id="3ec72-480">serviço público nenhum</span><span class="sxs-lookup"><span data-stu-id="3ec72-480">public service no</span></span>
  
<span data-ttu-id="3ec72-481">serviço de público pessoal nenhum</span><span class="sxs-lookup"><span data-stu-id="3ec72-481">personal public service no</span></span>
  
<span data-ttu-id="3ec72-482">PPS nenhum</span><span class="sxs-lookup"><span data-stu-id="3ec72-482">pps no</span></span>
  
<span data-ttu-id="3ec72-483">pessoal de serviço não</span><span class="sxs-lookup"><span data-stu-id="3ec72-483">personal service no</span></span>
  
<span data-ttu-id="3ec72-484">PPS pessoal não</span><span class="sxs-lookup"><span data-stu-id="3ec72-484">pps service no</span></span>
  
<span data-ttu-id="3ec72-485">ppsno #</span><span class="sxs-lookup"><span data-stu-id="3ec72-485">ppsno#</span></span>
  
<span data-ttu-id="3ec72-486">Irlandês pps nenhum</span><span class="sxs-lookup"><span data-stu-id="3ec72-486">irish pps no</span></span>
  
<span data-ttu-id="3ec72-487">publicserviceno #</span><span class="sxs-lookup"><span data-stu-id="3ec72-487">publicserviceno#</span></span>
  
<span data-ttu-id="3ec72-488">número de serviço pessoal de público</span><span class="sxs-lookup"><span data-stu-id="3ec72-488">personal public service number</span></span>
  
<span data-ttu-id="3ec72-489">uimhir phearsanta seirbhíse poiblí</span><span class="sxs-lookup"><span data-stu-id="3ec72-489">uimhir phearsanta seirbhíse poiblí</span></span>
  
<span data-ttu-id="3ec72-490">uimh PPS</span><span class="sxs-lookup"><span data-stu-id="3ec72-490">pps uimh</span></span>
  
<span data-ttu-id="3ec72-491">uimhir aitheantais phearsanta</span><span class="sxs-lookup"><span data-stu-id="3ec72-491">uimhir aitheantais phearsanta</span></span>
  
## <a name="italy"></a><span data-ttu-id="3ec72-492">Itália</span><span class="sxs-lookup"><span data-stu-id="3ec72-492">Italy</span></span>

### <a name="format"></a><span data-ttu-id="3ec72-493">Formato</span><span class="sxs-lookup"><span data-stu-id="3ec72-493">Format</span></span>

<span data-ttu-id="3ec72-494">16 letras e dígitos no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="3ec72-494">16 letters and digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ec72-495">Padrão</span><span class="sxs-lookup"><span data-stu-id="3ec72-495">Pattern</span></span>

<span data-ttu-id="3ec72-496">16 letras e dígitos:</span><span class="sxs-lookup"><span data-stu-id="3ec72-496">16 letters and digits:</span></span>
  
-  <span data-ttu-id="3ec72-497">Três letras que correspondem às três primeiros consoantes no nome da família</span><span class="sxs-lookup"><span data-stu-id="3ec72-497">Three letters that correspond to the first three consonants in the family name</span></span> 
    
- <span data-ttu-id="3ec72-498">Três letras que correspondem à primeira, terceira e quarta consoantes no primeiro nome de usuário</span><span class="sxs-lookup"><span data-stu-id="3ec72-498">Three letters that correspond to the first, third, and fourth consonants in the first name</span></span>
    
- <span data-ttu-id="3ec72-499">Dois dígitos que correspondem à última dígitos do ano nascimento</span><span class="sxs-lookup"><span data-stu-id="3ec72-499">Two digits that correspond to the last digits of the birth year</span></span>
    
- <span data-ttu-id="3ec72-500">Um dígito que corresponde ao mês de nascimento — letras são usadas em ordem alfabética, mas apenas as letras de a F, R, L, M, P, R para T são usadas (assim, janeiro é uma e outubro é R)</span><span class="sxs-lookup"><span data-stu-id="3ec72-500">One digit that corresponds to the month of birth—letters are used in alphabetical order, but only the letters A to E, H, L, M, P, R to T are used (thus, January is A and October is R)</span></span>
    
- <span data-ttu-id="3ec72-501">Dois dígitos que correspondem ao dia do mês de nascimento onde 40 é adicionado ao dia de nascimento para mulheres diferenciar dos homens</span><span class="sxs-lookup"><span data-stu-id="3ec72-501">Two digits that correspond to the day of the month of birth where 40 is added to the day of birth for females to differentiate from males</span></span>
    
- <span data-ttu-id="3ec72-502">Quatro dígitos que correspondem a um código de área específico para o município onde a pessoa surgiu — códigos de todo o país são usados para países estrangeiros</span><span class="sxs-lookup"><span data-stu-id="3ec72-502">Four digits that correspond to an area code specific to the municipality where the person was born—country-wide codes are used for foreign countries</span></span>
    
- <span data-ttu-id="3ec72-503">Seleção de um dígito</span><span class="sxs-lookup"><span data-stu-id="3ec72-503">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="3ec72-504">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3ec72-504">Checksum</span></span>

<span data-ttu-id="3ec72-505">Sim</span><span class="sxs-lookup"><span data-stu-id="3ec72-505">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ec72-506">Definição</span><span class="sxs-lookup"><span data-stu-id="3ec72-506">Definition</span></span>

<span data-ttu-id="3ec72-507">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-507">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-508">A função `Func_italy_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-508">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ec72-509">Uma palavra-chave da `Keywords_italy_eu_tax_file_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="3ec72-509">A keyword from  `Keywords_italy_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3ec72-510">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-510">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-511">A função `Func_italy_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-511">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="3ec72-512">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3ec72-512">Keywords</span></span>

#### <a name="keywordsitalyeutaxfilenumber"></a><span data-ttu-id="3ec72-513">Keywords_italy_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3ec72-513">Keywords_italy_eu_tax_file_number</span></span>

<span data-ttu-id="3ec72-514">número de imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-514">tax number</span></span>
  
<span data-ttu-id="3ec72-515">imposto não.</span><span class="sxs-lookup"><span data-stu-id="3ec72-515">tax no.</span></span>
  
<span data-ttu-id="3ec72-516">taxno #</span><span class="sxs-lookup"><span data-stu-id="3ec72-516">taxno#</span></span>
  
<span data-ttu-id="3ec72-517">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="3ec72-517">taxnumber#</span></span>
  
<span data-ttu-id="3ec72-518">taxnumber</span><span class="sxs-lookup"><span data-stu-id="3ec72-518">taxnumber</span></span>
  
<span data-ttu-id="3ec72-519">tax id
</span><span class="sxs-lookup"><span data-stu-id="3ec72-519">tax id</span></span>
  
<span data-ttu-id="3ec72-520">taxid #</span><span class="sxs-lookup"><span data-stu-id="3ec72-520">taxid#</span></span>
  
<span data-ttu-id="3ec72-521">código fiscal</span><span class="sxs-lookup"><span data-stu-id="3ec72-521">fiscal code</span></span>
  
<span data-ttu-id="3ec72-522">codice fiscale</span><span class="sxs-lookup"><span data-stu-id="3ec72-522">codice fiscale</span></span>
  
## <a name="latvia"></a><span data-ttu-id="3ec72-523">Letônia</span><span class="sxs-lookup"><span data-stu-id="3ec72-523">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="3ec72-524">Formato</span><span class="sxs-lookup"><span data-stu-id="3ec72-524">Format</span></span>

<span data-ttu-id="3ec72-525">11 dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="3ec72-525">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ec72-526">Padrão</span><span class="sxs-lookup"><span data-stu-id="3ec72-526">Pattern</span></span>

<span data-ttu-id="3ec72-527">11 dígitos no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="3ec72-527">11 digits in the specified pattern</span></span>
  
-  <span data-ttu-id="3ec72-528">Seis dígitos que correspondem à data de nascimento (DDMMYY)</span><span class="sxs-lookup"><span data-stu-id="3ec72-528">Six digits that correspond to the date of birth (DDMMYY)</span></span> 
    
- <span data-ttu-id="3ec72-529">Um dígito que corresponde do century de nascimento onde "0" corresponde ao décimo nono century, corresponde "1" como century 20 e "2" corresponde a century 21</span><span class="sxs-lookup"><span data-stu-id="3ec72-529">One digit that corresponds to the century of birth where "0" corresponds to 19th century, "1" corresponds to 20th century, and "2"corresponds to 21st century</span></span>
    
- <span data-ttu-id="3ec72-530">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="3ec72-530">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="3ec72-531">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3ec72-531">Checksum</span></span>

<span data-ttu-id="3ec72-532">Sim</span><span class="sxs-lookup"><span data-stu-id="3ec72-532">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ec72-533">Definição</span><span class="sxs-lookup"><span data-stu-id="3ec72-533">Definition</span></span>

<span data-ttu-id="3ec72-534">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-534">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-535">A função `Func_latvia_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-535">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ec72-536">Uma palavra-chave da `Keywords_latvia_eu_tax_file_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="3ec72-536">A keyword from  `Keywords_latvia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3ec72-537">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-537">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-538">A função `Func_latvia_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-538">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="3ec72-539">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3ec72-539">Keywords</span></span>

#### <a name="keywordslatviaeutaxfilenumber"></a><span data-ttu-id="3ec72-540">Keywords_latvia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3ec72-540">Keywords_latvia_eu_tax_file_number</span></span>

<span data-ttu-id="3ec72-541">número de imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-541">tax number</span></span>
  
<span data-ttu-id="3ec72-542">imposto não.</span><span class="sxs-lookup"><span data-stu-id="3ec72-542">tax no.</span></span>
  
<span data-ttu-id="3ec72-543">taxno #</span><span class="sxs-lookup"><span data-stu-id="3ec72-543">taxno#</span></span>
  
<span data-ttu-id="3ec72-544">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="3ec72-544">taxnumber#</span></span>
  
<span data-ttu-id="3ec72-545">taxnumber</span><span class="sxs-lookup"><span data-stu-id="3ec72-545">taxnumber</span></span>
  
<span data-ttu-id="3ec72-546">tax id
</span><span class="sxs-lookup"><span data-stu-id="3ec72-546">tax id</span></span>
  
<span data-ttu-id="3ec72-547">taxid #</span><span class="sxs-lookup"><span data-stu-id="3ec72-547">taxid#</span></span>
  
<span data-ttu-id="3ec72-548">número de identificação de imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-548">tax identification number</span></span>
  
<span data-ttu-id="3ec72-549">identificação de imposto não.</span><span class="sxs-lookup"><span data-stu-id="3ec72-549">tax identification no.</span></span>
  
<span data-ttu-id="3ec72-550">nodokļa numurs</span><span class="sxs-lookup"><span data-stu-id="3ec72-550">nodokļa numurs</span></span>
  
<span data-ttu-id="3ec72-551">nodokļu identifikācijas numurs</span><span class="sxs-lookup"><span data-stu-id="3ec72-551">nodokļu identifikācijas numurs</span></span>
  
<span data-ttu-id="3ec72-552">nodokļu identifikācija numurs</span><span class="sxs-lookup"><span data-stu-id="3ec72-552">nodokļu identifikācija numurs</span></span>
  
## <a name="lithuania"></a><span data-ttu-id="3ec72-553">Lituânia</span><span class="sxs-lookup"><span data-stu-id="3ec72-553">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="3ec72-554">Formato</span><span class="sxs-lookup"><span data-stu-id="3ec72-554">Format</span></span>

<span data-ttu-id="3ec72-555">11 dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="3ec72-555">11 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ec72-556">Padrão</span><span class="sxs-lookup"><span data-stu-id="3ec72-556">Pattern</span></span>

<span data-ttu-id="3ec72-557">11 dígitos</span><span class="sxs-lookup"><span data-stu-id="3ec72-557">11 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="3ec72-558">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3ec72-558">Checksum</span></span>

<span data-ttu-id="3ec72-559">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="3ec72-559">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ec72-560">Definição</span><span class="sxs-lookup"><span data-stu-id="3ec72-560">Definition</span></span>

<span data-ttu-id="3ec72-561">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-561">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-562">A função `Func_lithuania_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-562">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ec72-563">Uma palavra-chave da `Keywords_lithuania_eu_tax_file_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="3ec72-563">A keyword from  `Keywords_lithuania_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3ec72-564">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-564">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-565">A função `Func_lithuania_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-565">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="3ec72-566">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3ec72-566">Keywords</span></span>

#### <a name="keywordslithuaniaeutaxfilenumber"></a><span data-ttu-id="3ec72-567">Keywords_lithuania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3ec72-567">Keywords_lithuania_eu_tax_file_number</span></span>

<span data-ttu-id="3ec72-568">número de imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-568">tax number</span></span>
  
<span data-ttu-id="3ec72-569">imposto não.</span><span class="sxs-lookup"><span data-stu-id="3ec72-569">tax no.</span></span>
  
<span data-ttu-id="3ec72-570">imposto não #</span><span class="sxs-lookup"><span data-stu-id="3ec72-570">tax no#</span></span>
  
<span data-ttu-id="3ec72-571">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="3ec72-571">taxnumber#</span></span>
  
<span data-ttu-id="3ec72-572">taxnumber</span><span class="sxs-lookup"><span data-stu-id="3ec72-572">taxnumber</span></span>
  
<span data-ttu-id="3ec72-573">tax id
</span><span class="sxs-lookup"><span data-stu-id="3ec72-573">tax id</span></span>
  
<span data-ttu-id="3ec72-574">taxid #</span><span class="sxs-lookup"><span data-stu-id="3ec72-574">taxid#</span></span>
  
<span data-ttu-id="3ec72-575">número de identificação de imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-575">tax identification number</span></span>
  
<span data-ttu-id="3ec72-576">identificação de imposto não.</span><span class="sxs-lookup"><span data-stu-id="3ec72-576">tax identification no.</span></span>
  
<span data-ttu-id="3ec72-577">id de mokesčių</span><span class="sxs-lookup"><span data-stu-id="3ec72-577">mokesčių id</span></span>
  
<span data-ttu-id="3ec72-578">mokesčių numeris</span><span class="sxs-lookup"><span data-stu-id="3ec72-578">mokesčių numeris</span></span>
  
<span data-ttu-id="3ec72-579">mokesčių identifikavimas numeris</span><span class="sxs-lookup"><span data-stu-id="3ec72-579">mokesčių identifikavimas numeris</span></span>
  
## <a name="luxemburg"></a><span data-ttu-id="3ec72-580">Luxemburgo</span><span class="sxs-lookup"><span data-stu-id="3ec72-580">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="3ec72-581">Formato</span><span class="sxs-lookup"><span data-stu-id="3ec72-581">Format</span></span>

<span data-ttu-id="3ec72-582">13 dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="3ec72-582">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ec72-583">Padrão</span><span class="sxs-lookup"><span data-stu-id="3ec72-583">Pattern</span></span>

<span data-ttu-id="3ec72-584">13 dígitos:</span><span class="sxs-lookup"><span data-stu-id="3ec72-584">13 digits:</span></span>
  
-  <span data-ttu-id="3ec72-585">11 dígitos</span><span class="sxs-lookup"><span data-stu-id="3ec72-585">11 digits</span></span> 
    
- <span data-ttu-id="3ec72-586">Dois dígitos de verificação</span><span class="sxs-lookup"><span data-stu-id="3ec72-586">Two check digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="3ec72-587">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3ec72-587">Checksum</span></span>

<span data-ttu-id="3ec72-588">Sim</span><span class="sxs-lookup"><span data-stu-id="3ec72-588">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ec72-589">Definição</span><span class="sxs-lookup"><span data-stu-id="3ec72-589">Definition</span></span>

<span data-ttu-id="3ec72-590">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-590">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-591">A função `Func_luxemburg_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-591">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ec72-592">Uma palavra-chave da `Keywords_luxemburg_eu_tax_file_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="3ec72-592">A keyword from  `Keywords_luxemburg_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3ec72-593">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-593">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-594">A função `Func_luxemburg_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-594">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="3ec72-595">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3ec72-595">Keywords</span></span>

#### <a name="keywordsluxemburgeutaxfilenumber"></a><span data-ttu-id="3ec72-596">Keywords_luxemburg_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3ec72-596">Keywords_luxemburg_eu_tax_file_number</span></span>

<span data-ttu-id="3ec72-597">número de imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-597">tax number</span></span>
  
<span data-ttu-id="3ec72-598">imposto não.</span><span class="sxs-lookup"><span data-stu-id="3ec72-598">tax no.</span></span>
  
<span data-ttu-id="3ec72-599">taxno #</span><span class="sxs-lookup"><span data-stu-id="3ec72-599">taxno#</span></span>
  
<span data-ttu-id="3ec72-600">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="3ec72-600">taxnumber#</span></span>
  
<span data-ttu-id="3ec72-601">taxnumber</span><span class="sxs-lookup"><span data-stu-id="3ec72-601">taxnumber</span></span>
  
<span data-ttu-id="3ec72-602">tax id
</span><span class="sxs-lookup"><span data-stu-id="3ec72-602">tax id</span></span>
  
<span data-ttu-id="3ec72-603">taxid #</span><span class="sxs-lookup"><span data-stu-id="3ec72-603">taxid#</span></span>
  
<span data-ttu-id="3ec72-604">número de identificação de imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-604">tax identification number</span></span>
  
<span data-ttu-id="3ec72-605">identificação de imposto não.</span><span class="sxs-lookup"><span data-stu-id="3ec72-605">tax identification no.</span></span>
  
<span data-ttu-id="3ec72-606">steuernummer</span><span class="sxs-lookup"><span data-stu-id="3ec72-606">steuernummer</span></span>
  
<span data-ttu-id="3ec72-607">id de steuer</span><span class="sxs-lookup"><span data-stu-id="3ec72-607">steuer id</span></span>
  
<span data-ttu-id="3ec72-608">steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="3ec72-608">steueridentifikationsnummer</span></span>
  
## <a name="malta"></a><span data-ttu-id="3ec72-609">Malta</span><span class="sxs-lookup"><span data-stu-id="3ec72-609">Malta</span></span>

### <a name="format"></a><span data-ttu-id="3ec72-610">Formato</span><span class="sxs-lookup"><span data-stu-id="3ec72-610">Format</span></span>

<span data-ttu-id="3ec72-611">Para cidadãos Maltês: 7 dígitos e uma letra no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="3ec72-611">For Maltese nationals: 7 digits and one letter in the specified pattern</span></span>
  
<span data-ttu-id="3ec72-612">Não-Maltês cidadãos e entidades Maltês: 9 dígitos</span><span class="sxs-lookup"><span data-stu-id="3ec72-612">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ec72-613">Padrão</span><span class="sxs-lookup"><span data-stu-id="3ec72-613">Pattern</span></span>

<span data-ttu-id="3ec72-614">Maltês cidadãos: 7 dígitos e uma letra</span><span class="sxs-lookup"><span data-stu-id="3ec72-614">Maltese nationals: 7 digits and one letter</span></span>
  
-  <span data-ttu-id="3ec72-615">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="3ec72-615">Seven digits</span></span> 
    
- <span data-ttu-id="3ec72-616">Uma letra (não diferencia maiusculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="3ec72-616">One letter (not case-sensitive)</span></span>
    
<span data-ttu-id="3ec72-617">Não-Maltês cidadãos e entidades Maltês: 9 dígitos</span><span class="sxs-lookup"><span data-stu-id="3ec72-617">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
-  <span data-ttu-id="3ec72-618">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="3ec72-618">Nine digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="3ec72-619">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3ec72-619">Checksum</span></span>

<span data-ttu-id="3ec72-620">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="3ec72-620">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ec72-621">Definição</span><span class="sxs-lookup"><span data-stu-id="3ec72-621">Definition</span></span>

<span data-ttu-id="3ec72-622">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-622">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-623">A função `Func_malta_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-623">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ec72-624">Uma palavra-chave da `Keywords_malta_eu_tax_file_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="3ec72-624">A keyword from  `Keywords_malta_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3ec72-625">Uma política de DLP tem 65% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-625">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-626">A função `Func_malta_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-626">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="3ec72-627">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3ec72-627">Keywords</span></span>

#### <a name="keywordsmaltaeutaxfilenumber"></a><span data-ttu-id="3ec72-628">Keywords_malta_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3ec72-628">Keywords_malta_eu_tax_file_number</span></span>

<span data-ttu-id="3ec72-629">número de imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-629">tax number</span></span>
  
<span data-ttu-id="3ec72-630">imposto não.</span><span class="sxs-lookup"><span data-stu-id="3ec72-630">tax no.</span></span>
  
<span data-ttu-id="3ec72-631">taxno #</span><span class="sxs-lookup"><span data-stu-id="3ec72-631">taxno#</span></span>
  
<span data-ttu-id="3ec72-632">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="3ec72-632">taxnumber#</span></span>
  
<span data-ttu-id="3ec72-633">taxnumber</span><span class="sxs-lookup"><span data-stu-id="3ec72-633">taxnumber</span></span>
  
<span data-ttu-id="3ec72-634">tax id
</span><span class="sxs-lookup"><span data-stu-id="3ec72-634">tax id</span></span>
  
<span data-ttu-id="3ec72-635">taxid #</span><span class="sxs-lookup"><span data-stu-id="3ec72-635">taxid#</span></span>
  
<span data-ttu-id="3ec72-636">número de identificação de imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-636">tax identification number</span></span>
  
<span data-ttu-id="3ec72-637">identificação de imposto não.</span><span class="sxs-lookup"><span data-stu-id="3ec72-637">tax identification no.</span></span>
  
<span data-ttu-id="3ec72-638">numru tat-taxxa</span><span class="sxs-lookup"><span data-stu-id="3ec72-638">numru tat-taxxa</span></span>
  
<span data-ttu-id="3ec72-639">ID tat-taxxa</span><span class="sxs-lookup"><span data-stu-id="3ec72-639">id tat-taxxa</span></span>
  
<span data-ttu-id="3ec72-640">numru guias ' identifikazzjoni tat-taxxa</span><span class="sxs-lookup"><span data-stu-id="3ec72-640">numru ta 'identifikazzjoni tat-taxxa</span></span>
  
## <a name="netherlands"></a><span data-ttu-id="3ec72-641">Países Baixos</span><span class="sxs-lookup"><span data-stu-id="3ec72-641">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="3ec72-642">Formato</span><span class="sxs-lookup"><span data-stu-id="3ec72-642">Format</span></span>

<span data-ttu-id="3ec72-643">Nove dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="3ec72-643">Nine digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ec72-644">Padrão</span><span class="sxs-lookup"><span data-stu-id="3ec72-644">Pattern</span></span>

<span data-ttu-id="3ec72-645">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="3ec72-645">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="3ec72-646">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3ec72-646">Checksum</span></span>

<span data-ttu-id="3ec72-647">Sim</span><span class="sxs-lookup"><span data-stu-id="3ec72-647">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ec72-648">Definição</span><span class="sxs-lookup"><span data-stu-id="3ec72-648">Definition</span></span>

<span data-ttu-id="3ec72-649">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-649">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-650">A função `Func_netherlands_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-650">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ec72-651">Uma palavra-chave da `Keywords_netherlands_eu_tax_file_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="3ec72-651">A keyword from  `Keywords_netherlands_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3ec72-652">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-652">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-653">A função `Func_netherlands_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-653">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="3ec72-654">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3ec72-654">Keywords</span></span>

#### <a name="keywordsnetherlandseutaxfilenumber"></a><span data-ttu-id="3ec72-655">Keywords_netherlands_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3ec72-655">Keywords_netherlands_eu_tax_file_number</span></span>

<span data-ttu-id="3ec72-656">número de identificação de imposto países baixos</span><span class="sxs-lookup"><span data-stu-id="3ec72-656">netherlands tax identification number</span></span>
  
<span data-ttu-id="3ec72-657">identificação de imposto países baixos</span><span class="sxs-lookup"><span data-stu-id="3ec72-657">netherlands tax identification</span></span>
  
<span data-ttu-id="3ec72-658">número de identificação do Antilhas imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-658">netherland's tax identification number</span></span>
  
<span data-ttu-id="3ec72-659">identificação de imposto do Antilhas</span><span class="sxs-lookup"><span data-stu-id="3ec72-659">netherland's tax identification</span></span>
  
<span data-ttu-id="3ec72-660">número de identificação de imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-660">tax identification number</span></span>
  
<span data-ttu-id="3ec72-661">id de imposto holandês</span><span class="sxs-lookup"><span data-stu-id="3ec72-661">dutch tax id</span></span>
  
<span data-ttu-id="3ec72-662">número de identificação de imposto holandês</span><span class="sxs-lookup"><span data-stu-id="3ec72-662">dutch tax identification number</span></span>
  
<span data-ttu-id="3ec72-663">tax id
</span><span class="sxs-lookup"><span data-stu-id="3ec72-663">tax id</span></span>
  
<span data-ttu-id="3ec72-664">n º fiscal</span><span class="sxs-lookup"><span data-stu-id="3ec72-664">tax id#</span></span>
  
<span data-ttu-id="3ec72-665">número de imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-665">tax number</span></span>
  
<span data-ttu-id="3ec72-666">imposto não #</span><span class="sxs-lookup"><span data-stu-id="3ec72-666">tax no#</span></span>
  
<span data-ttu-id="3ec72-667">imposto #</span><span class="sxs-lookup"><span data-stu-id="3ec72-667">tax#</span></span>
  
<span data-ttu-id="3ec72-668">tin
</span><span class="sxs-lookup"><span data-stu-id="3ec72-668">tin</span></span>
  
<span data-ttu-id="3ec72-669">TIN #</span><span class="sxs-lookup"><span data-stu-id="3ec72-669">tin#</span></span>
  
<span data-ttu-id="3ec72-670">tin países baixos</span><span class="sxs-lookup"><span data-stu-id="3ec72-670">netherlands tin</span></span>
  
<span data-ttu-id="3ec72-671">tin do Antilhas</span><span class="sxs-lookup"><span data-stu-id="3ec72-671">netherland's tin</span></span>
  
<span data-ttu-id="3ec72-672">Holanda belasting identificatienummer</span><span class="sxs-lookup"><span data-stu-id="3ec72-672">nederlands belasting identificatienummer</span></span>
  
<span data-ttu-id="3ec72-673">identificatienummer van belasting</span><span class="sxs-lookup"><span data-stu-id="3ec72-673">identificatienummer van belasting</span></span>
  
<span data-ttu-id="3ec72-674">identificatienummer belasting</span><span class="sxs-lookup"><span data-stu-id="3ec72-674">identificatienummer belasting</span></span>
  
<span data-ttu-id="3ec72-675">Holanda belasting identificatie</span><span class="sxs-lookup"><span data-stu-id="3ec72-675">nederlands belasting identificatie</span></span>
  
<span data-ttu-id="3ec72-676">Holanda belasting id nummer</span><span class="sxs-lookup"><span data-stu-id="3ec72-676">nederlands belasting id nummer</span></span>
  
<span data-ttu-id="3ec72-677">Holanda belastingnummer</span><span class="sxs-lookup"><span data-stu-id="3ec72-677">nederlands belastingnummer</span></span>
  
<span data-ttu-id="3ec72-678">btw nummer</span><span class="sxs-lookup"><span data-stu-id="3ec72-678">btw nummer</span></span>
  
<span data-ttu-id="3ec72-679">nederlandse belasting identificatie</span><span class="sxs-lookup"><span data-stu-id="3ec72-679">nederlandse belasting identificatie</span></span>
  
## <a name="poland"></a><span data-ttu-id="3ec72-680">Polônia</span><span class="sxs-lookup"><span data-stu-id="3ec72-680">Poland</span></span>

### <a name="format"></a><span data-ttu-id="3ec72-681">Formato</span><span class="sxs-lookup"><span data-stu-id="3ec72-681">Format</span></span>

<span data-ttu-id="3ec72-682">Onze dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="3ec72-682">Eleven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ec72-683">Padrão</span><span class="sxs-lookup"><span data-stu-id="3ec72-683">Pattern</span></span>

<span data-ttu-id="3ec72-684">Onze dígitos</span><span class="sxs-lookup"><span data-stu-id="3ec72-684">Eleven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="3ec72-685">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3ec72-685">Checksum</span></span>

<span data-ttu-id="3ec72-686">Sim</span><span class="sxs-lookup"><span data-stu-id="3ec72-686">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ec72-687">Definição</span><span class="sxs-lookup"><span data-stu-id="3ec72-687">Definition</span></span>

<span data-ttu-id="3ec72-688">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-688">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-689">A função `Func_poland_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-689">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ec72-690">Uma palavra-chave da `Keywords_poland_eu_tax_file_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="3ec72-690">A keyword from  `Keywords_poland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3ec72-691">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-691">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-692">A função `Func_poland_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-692">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="3ec72-693">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3ec72-693">Keywords</span></span>

#### <a name="keywordspolandeutaxfilenumber"></a><span data-ttu-id="3ec72-694">Keywords_poland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3ec72-694">Keywords_poland_eu_tax_file_number</span></span>

<span data-ttu-id="3ec72-695">número de imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-695">tax number</span></span>
  
<span data-ttu-id="3ec72-696">imposto não.</span><span class="sxs-lookup"><span data-stu-id="3ec72-696">tax no.</span></span>
  
<span data-ttu-id="3ec72-697">taxno #</span><span class="sxs-lookup"><span data-stu-id="3ec72-697">taxno#</span></span>
  
<span data-ttu-id="3ec72-698">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="3ec72-698">taxnumber#</span></span>
  
<span data-ttu-id="3ec72-699">taxnumber</span><span class="sxs-lookup"><span data-stu-id="3ec72-699">taxnumber</span></span>
  
<span data-ttu-id="3ec72-700">NIP</span><span class="sxs-lookup"><span data-stu-id="3ec72-700">nip</span></span>
  
<span data-ttu-id="3ec72-701">NIP #</span><span class="sxs-lookup"><span data-stu-id="3ec72-701">nip#</span></span>
  
<span data-ttu-id="3ec72-702">tax id
</span><span class="sxs-lookup"><span data-stu-id="3ec72-702">tax id</span></span>
  
<span data-ttu-id="3ec72-703">n º fiscal</span><span class="sxs-lookup"><span data-stu-id="3ec72-703">tax id#</span></span>
  
<span data-ttu-id="3ec72-704">id de NIP</span><span class="sxs-lookup"><span data-stu-id="3ec72-704">nip id</span></span>
  
<span data-ttu-id="3ec72-705">id de NIP #</span><span class="sxs-lookup"><span data-stu-id="3ec72-705">nip id#</span></span>
  
<span data-ttu-id="3ec72-706">número de identificação de imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-706">tax identification number</span></span>
  
<span data-ttu-id="3ec72-707">identificação de imposto não.</span><span class="sxs-lookup"><span data-stu-id="3ec72-707">tax identification no.</span></span>
  
<span data-ttu-id="3ec72-708">número VAT</span><span class="sxs-lookup"><span data-stu-id="3ec72-708">vat number</span></span>
  
<span data-ttu-id="3ec72-709">IVA não.</span><span class="sxs-lookup"><span data-stu-id="3ec72-709">vat no.</span></span>
  
<span data-ttu-id="3ec72-710">vatno #</span><span class="sxs-lookup"><span data-stu-id="3ec72-710">vatno#</span></span>
  
<span data-ttu-id="3ec72-711">id de VAT</span><span class="sxs-lookup"><span data-stu-id="3ec72-711">vat id</span></span>
  
<span data-ttu-id="3ec72-712">id de VAT #</span><span class="sxs-lookup"><span data-stu-id="3ec72-712">vat id#</span></span>
  
<span data-ttu-id="3ec72-713">número identyfikacji podatkowej</span><span class="sxs-lookup"><span data-stu-id="3ec72-713">numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="3ec72-714">Polski número identyfikacji podatkowej</span><span class="sxs-lookup"><span data-stu-id="3ec72-714">polski numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="3ec72-715">numeridentyfikacjipodatkowej #</span><span class="sxs-lookup"><span data-stu-id="3ec72-715">numeridentyfikacjipodatkowej#</span></span>
  
## <a name="portugal"></a><span data-ttu-id="3ec72-716">Portugal</span><span class="sxs-lookup"><span data-stu-id="3ec72-716">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="3ec72-717">Formato</span><span class="sxs-lookup"><span data-stu-id="3ec72-717">Format</span></span>

<span data-ttu-id="3ec72-718">Nove dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="3ec72-718">Nine digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ec72-719">Padrão</span><span class="sxs-lookup"><span data-stu-id="3ec72-719">Pattern</span></span>

<span data-ttu-id="3ec72-720">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="3ec72-720">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="3ec72-721">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3ec72-721">Checksum</span></span>

<span data-ttu-id="3ec72-722">Sim</span><span class="sxs-lookup"><span data-stu-id="3ec72-722">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ec72-723">Definição</span><span class="sxs-lookup"><span data-stu-id="3ec72-723">Definition</span></span>

<span data-ttu-id="3ec72-724">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-724">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-725">A função `Func_portugal_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-725">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ec72-726">Uma palavra-chave da `Keywords_portugal_eu_tax_file_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="3ec72-726">A keyword from  `Keywords_portugal_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3ec72-727">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-727">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-728">A função `Func_portugal_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-728">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="3ec72-729">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3ec72-729">Keywords</span></span>

#### <a name="keywordsportugaleutaxfilenumber"></a><span data-ttu-id="3ec72-730">Keywords_portugal_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3ec72-730">Keywords_portugal_eu_tax_file_number</span></span>

<span data-ttu-id="3ec72-731">número de imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-731">tax number</span></span>
  
<span data-ttu-id="3ec72-732">imposto não.</span><span class="sxs-lookup"><span data-stu-id="3ec72-732">tax no.</span></span>
  
<span data-ttu-id="3ec72-733">taxno #</span><span class="sxs-lookup"><span data-stu-id="3ec72-733">taxno#</span></span>
  
<span data-ttu-id="3ec72-734">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="3ec72-734">taxnumber#</span></span>
  
<span data-ttu-id="3ec72-735">taxnumber</span><span class="sxs-lookup"><span data-stu-id="3ec72-735">taxnumber</span></span>
  
<span data-ttu-id="3ec72-736">NIF</span><span class="sxs-lookup"><span data-stu-id="3ec72-736">nif</span></span>
  
<span data-ttu-id="3ec72-737">NIF #</span><span class="sxs-lookup"><span data-stu-id="3ec72-737">nif#</span></span>
  
<span data-ttu-id="3ec72-738">numero fiscal</span><span class="sxs-lookup"><span data-stu-id="3ec72-738">numero fiscal</span></span>
  
<span data-ttu-id="3ec72-739">número de identificação fiscal</span><span class="sxs-lookup"><span data-stu-id="3ec72-739">número de identificação fiscal</span></span>
  
## <a name="romania"></a><span data-ttu-id="3ec72-740">Romênia</span><span class="sxs-lookup"><span data-stu-id="3ec72-740">Romania</span></span>

### <a name="format"></a><span data-ttu-id="3ec72-741">Formato</span><span class="sxs-lookup"><span data-stu-id="3ec72-741">Format</span></span>

<span data-ttu-id="3ec72-742">13 dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="3ec72-742">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ec72-743">Padrão</span><span class="sxs-lookup"><span data-stu-id="3ec72-743">Pattern</span></span>

<span data-ttu-id="3ec72-744">13 dígitos</span><span class="sxs-lookup"><span data-stu-id="3ec72-744">13 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="3ec72-745">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3ec72-745">Checksum</span></span>

<span data-ttu-id="3ec72-746">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="3ec72-746">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ec72-747">Definição</span><span class="sxs-lookup"><span data-stu-id="3ec72-747">Definition</span></span>

<span data-ttu-id="3ec72-748">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-748">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-749">A expressão regular `Regex_romania_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-749">The regular expression  `Regex_romania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ec72-750">Uma palavra-chave da `Keywords_romania_eu_tax_file_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="3ec72-750">A keyword from  `Keywords_romania_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_tax_file_number" />
          <Match idRef="Keywords_romania_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3ec72-751">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3ec72-751">Keywords</span></span>

#### <a name="keywordsromaniaeutaxfilenumber"></a><span data-ttu-id="3ec72-752">Keywords_romania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3ec72-752">Keywords_romania_eu_tax_file_number</span></span>

<span data-ttu-id="3ec72-753">tax id
</span><span class="sxs-lookup"><span data-stu-id="3ec72-753">tax id</span></span>
  
<span data-ttu-id="3ec72-754">número de identificação de imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-754">tax id number</span></span>
  
<span data-ttu-id="3ec72-755">arquivo do imposto não</span><span class="sxs-lookup"><span data-stu-id="3ec72-755">tax file no</span></span>
  
<span data-ttu-id="3ec72-756">

tax file number</span><span class="sxs-lookup"><span data-stu-id="3ec72-756">tax file number</span></span>
  
<span data-ttu-id="3ec72-757">imposto não</span><span class="sxs-lookup"><span data-stu-id="3ec72-757">tax no</span></span>
  
<span data-ttu-id="3ec72-758">número de imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-758">tax number</span></span>
  
<span data-ttu-id="3ec72-759">taxid #</span><span class="sxs-lookup"><span data-stu-id="3ec72-759">taxid#</span></span>
  
<span data-ttu-id="3ec72-760">taxno #</span><span class="sxs-lookup"><span data-stu-id="3ec72-760">taxno#</span></span>
  
<span data-ttu-id="3ec72-761">ID-ul taxei</span><span class="sxs-lookup"><span data-stu-id="3ec72-761">id-ul taxei</span></span>
  
<span data-ttu-id="3ec72-762">numărul de identificare fiscală</span><span class="sxs-lookup"><span data-stu-id="3ec72-762">numărul de identificare fiscală</span></span>
  
## <a name="slovakia"></a><span data-ttu-id="3ec72-763">Eslováquia</span><span class="sxs-lookup"><span data-stu-id="3ec72-763">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="3ec72-764">Formato</span><span class="sxs-lookup"><span data-stu-id="3ec72-764">Format</span></span>

<span data-ttu-id="3ec72-765">10 dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="3ec72-765">10 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ec72-766">Padrão</span><span class="sxs-lookup"><span data-stu-id="3ec72-766">Pattern</span></span>

<span data-ttu-id="3ec72-767">10 dígitos</span><span class="sxs-lookup"><span data-stu-id="3ec72-767">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="3ec72-768">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3ec72-768">Checksum</span></span>

<span data-ttu-id="3ec72-769">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="3ec72-769">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ec72-770">Definição</span><span class="sxs-lookup"><span data-stu-id="3ec72-770">Definition</span></span>

<span data-ttu-id="3ec72-771">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-771">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-772">A expressão regular `Regex_slovakia_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-772">The regular expression  `Regex_slovakia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ec72-773">Uma palavra-chave da `Keywords_slovakia_eu_tax_file_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="3ec72-773">A keyword from  `Keywords_slovakia_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_tax_file_number" />
          <Match idRef="Keywords_slovakia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3ec72-774">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3ec72-774">Keywords</span></span>

#### <a name="keywordsslovakiaeutaxfilenumber"></a><span data-ttu-id="3ec72-775">Keywords_slovakia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3ec72-775">Keywords_slovakia_eu_tax_file_number</span></span>

<span data-ttu-id="3ec72-776">tax id
</span><span class="sxs-lookup"><span data-stu-id="3ec72-776">tax id</span></span>
  
<span data-ttu-id="3ec72-777">número de identificação de imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-777">tax id number</span></span>
  
<span data-ttu-id="3ec72-778">id de estanho</span><span class="sxs-lookup"><span data-stu-id="3ec72-778">tin id</span></span>
  
<span data-ttu-id="3ec72-779">não estanho</span><span class="sxs-lookup"><span data-stu-id="3ec72-779">tin no</span></span>
  
<span data-ttu-id="3ec72-780">id de estanho eslovaco</span><span class="sxs-lookup"><span data-stu-id="3ec72-780">slovakian tin id</span></span>
  
<span data-ttu-id="3ec72-781">tin
</span><span class="sxs-lookup"><span data-stu-id="3ec72-781">tin</span></span>
  
<span data-ttu-id="3ec72-782">arquivo do imposto não</span><span class="sxs-lookup"><span data-stu-id="3ec72-782">tax file no</span></span>
  
<span data-ttu-id="3ec72-783">

tax file number</span><span class="sxs-lookup"><span data-stu-id="3ec72-783">tax file number</span></span>
  
<span data-ttu-id="3ec72-784">imposto não</span><span class="sxs-lookup"><span data-stu-id="3ec72-784">tax no</span></span>
  
<span data-ttu-id="3ec72-785">número de imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-785">tax number</span></span>
  
<span data-ttu-id="3ec72-786">taxid #</span><span class="sxs-lookup"><span data-stu-id="3ec72-786">taxid#</span></span>
  
<span data-ttu-id="3ec72-787">taxno #</span><span class="sxs-lookup"><span data-stu-id="3ec72-787">taxno#</span></span>
  
<span data-ttu-id="3ec72-788">daňové identifikačné číslo</span><span class="sxs-lookup"><span data-stu-id="3ec72-788">daňové identifikačné číslo</span></span>
  
<span data-ttu-id="3ec72-789">daňové číslo</span><span class="sxs-lookup"><span data-stu-id="3ec72-789">daňové číslo</span></span>
  
<span data-ttu-id="3ec72-790">daňové číslo súboru</span><span class="sxs-lookup"><span data-stu-id="3ec72-790">daňové číslo súboru</span></span>
  
## <a name="slovenia"></a><span data-ttu-id="3ec72-791">Eslovênia</span><span class="sxs-lookup"><span data-stu-id="3ec72-791">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="3ec72-792">Formato</span><span class="sxs-lookup"><span data-stu-id="3ec72-792">Format</span></span>

<span data-ttu-id="3ec72-793">Oito dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="3ec72-793">Eight digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ec72-794">Padrão</span><span class="sxs-lookup"><span data-stu-id="3ec72-794">Pattern</span></span>

<span data-ttu-id="3ec72-795">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="3ec72-795">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="3ec72-796">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3ec72-796">Checksum</span></span>

<span data-ttu-id="3ec72-797">Sim</span><span class="sxs-lookup"><span data-stu-id="3ec72-797">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ec72-798">Definição</span><span class="sxs-lookup"><span data-stu-id="3ec72-798">Definition</span></span>

<span data-ttu-id="3ec72-799">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-799">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-800">A função `Func_slovenia_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-800">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ec72-801">Uma palavra-chave da `Keywords_slovenia_eu_tax_file_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="3ec72-801">A keyword from  `Keywords_slovenia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3ec72-802">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-802">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-803">A função `Func_slovenia_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-803">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="3ec72-804">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3ec72-804">Keywords</span></span>

#### <a name="keywordssloveniaeutaxfilenumber"></a><span data-ttu-id="3ec72-805">Keywords_slovenia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3ec72-805">Keywords_slovenia_eu_tax_file_number</span></span>

<span data-ttu-id="3ec72-806">tax id
</span><span class="sxs-lookup"><span data-stu-id="3ec72-806">tax id</span></span>
  
<span data-ttu-id="3ec72-807">número de identificação de imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-807">tax id number</span></span>
  
<span data-ttu-id="3ec72-808">id de estanho</span><span class="sxs-lookup"><span data-stu-id="3ec72-808">tin id</span></span>
  
<span data-ttu-id="3ec72-809">não estanho</span><span class="sxs-lookup"><span data-stu-id="3ec72-809">tin no</span></span>
  
<span data-ttu-id="3ec72-810">id de estanho esloveno</span><span class="sxs-lookup"><span data-stu-id="3ec72-810">slovenian tin id</span></span>
  
<span data-ttu-id="3ec72-811">tin
</span><span class="sxs-lookup"><span data-stu-id="3ec72-811">tin</span></span>
  
<span data-ttu-id="3ec72-812">arquivo do imposto não</span><span class="sxs-lookup"><span data-stu-id="3ec72-812">tax file no</span></span>
  
<span data-ttu-id="3ec72-813">

tax file number</span><span class="sxs-lookup"><span data-stu-id="3ec72-813">tax file number</span></span>
  
<span data-ttu-id="3ec72-814">imposto não</span><span class="sxs-lookup"><span data-stu-id="3ec72-814">tax no</span></span>
  
<span data-ttu-id="3ec72-815">número de imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-815">tax number</span></span>
  
<span data-ttu-id="3ec72-816">taxid #</span><span class="sxs-lookup"><span data-stu-id="3ec72-816">taxid#</span></span>
  
<span data-ttu-id="3ec72-817">taxno #</span><span class="sxs-lookup"><span data-stu-id="3ec72-817">taxno#</span></span>
  
<span data-ttu-id="3ec72-818">identifikacijska številka davka</span><span class="sxs-lookup"><span data-stu-id="3ec72-818">identifikacijska številka davka</span></span>
  
<span data-ttu-id="3ec72-819">davčna številka</span><span class="sxs-lookup"><span data-stu-id="3ec72-819">davčna številka</span></span>
  
<span data-ttu-id="3ec72-820">Številka davčne datoteke</span><span class="sxs-lookup"><span data-stu-id="3ec72-820">številka davčne datoteke</span></span>
  
## <a name="spain"></a><span data-ttu-id="3ec72-821">Espanha</span><span class="sxs-lookup"><span data-stu-id="3ec72-821">Spain</span></span>

### <a name="format"></a><span data-ttu-id="3ec72-822">Formato</span><span class="sxs-lookup"><span data-stu-id="3ec72-822">Format</span></span>

<span data-ttu-id="3ec72-823">Sete ou oito dígitos e uma ou duas letras no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="3ec72-823">Seven or eight digits and one or two letters in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ec72-824">Padrão</span><span class="sxs-lookup"><span data-stu-id="3ec72-824">Pattern</span></span>

<span data-ttu-id="3ec72-825">Espanholas Natural as pessoas com um cartão de identificação nacional da Espanha:</span><span class="sxs-lookup"><span data-stu-id="3ec72-825">Spanish Natural Persons with a Spain National Identity Card:</span></span>
  
-  <span data-ttu-id="3ec72-826">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="3ec72-826">Eight digits</span></span> 
    
- <span data-ttu-id="3ec72-827">Uma letra maiuscula (diferencia maiusculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="3ec72-827">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="3ec72-828">Não residente Spaniards sem um cartão de identificação nacional da Espanha</span><span class="sxs-lookup"><span data-stu-id="3ec72-828">Non-resident Spaniards without a Spain National Identity Card</span></span>
  
- <span data-ttu-id="3ec72-829">Uma letra maiuscula "L" (diferencia maiusculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="3ec72-829">One uppercase letter "L" (case-sensitive)</span></span>
    
- <span data-ttu-id="3ec72-830">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="3ec72-830">Seven digits</span></span>
    
- <span data-ttu-id="3ec72-831">Uma letra maiuscula (diferencia maiusculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="3ec72-831">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="3ec72-832">Spaniards residente sob a idade dos 14 anos sem um Espanha nacional identidade cartão:</span><span class="sxs-lookup"><span data-stu-id="3ec72-832">Resident Spaniards under the age of 14 years without a Spain National Identity Card :</span></span>
  
- <span data-ttu-id="3ec72-833">Uma letra maiuscula "K" (diferencia maiusculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="3ec72-833">One uppercase letter"K" (case-sensitive)</span></span>
    
-  <span data-ttu-id="3ec72-834">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="3ec72-834">Seven digits</span></span> 
    
- <span data-ttu-id="3ec72-835">Uma letra maiuscula (diferencia maiusculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="3ec72-835">One uppercase letter (case-sensitive)</span></span>
    
<span data-ttu-id="3ec72-836">Estrangeiros com número de identificação de um Foreigner</span><span class="sxs-lookup"><span data-stu-id="3ec72-836">Foreigners with a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="3ec72-837">Letras maiusculas uma letra ou seja "X", "Y" ou "Z" (diferencia maiusculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="3ec72-837">One uppercase letter that is "X", "Y", or "Z" (case-sensitive)</span></span> 
    
- <span data-ttu-id="3ec72-838">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="3ec72-838">Seven digits</span></span>
    
- <span data-ttu-id="3ec72-839">Uma letra maiuscula (diferencia maiusculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="3ec72-839">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="3ec72-840">Estrangeiros sem número de identificação de um Foreigner</span><span class="sxs-lookup"><span data-stu-id="3ec72-840">Foreigners without a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="3ec72-841">Uma letra maiuscula que é "M" (diferencia maiusculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="3ec72-841">One uppercase letter that is "M" (case-sensitive)</span></span> 
    
- <span data-ttu-id="3ec72-842">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="3ec72-842">Seven digits</span></span>
    
- <span data-ttu-id="3ec72-843">Uma letra maiuscula (diferencia maiusculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="3ec72-843">One uppercase letter (case-sensitive)</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="3ec72-844">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3ec72-844">Checksum</span></span>

<span data-ttu-id="3ec72-845">Sim</span><span class="sxs-lookup"><span data-stu-id="3ec72-845">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ec72-846">Definição</span><span class="sxs-lookup"><span data-stu-id="3ec72-846">Definition</span></span>

<span data-ttu-id="3ec72-847">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-847">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-848">A função `Func_spain_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-848">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ec72-849">Uma palavra-chave da `Keywords_spain_eu_tax_file_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="3ec72-849">A keyword from  `Keywords_spain_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3ec72-850">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-850">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-851">A função `Func_spain_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-851">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="3ec72-852">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3ec72-852">Keywords</span></span>

#### <a name="keywordsspaineutaxfilenumber"></a><span data-ttu-id="3ec72-853">Keywords_spain_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3ec72-853">Keywords_spain_eu_tax_file_number</span></span>

<span data-ttu-id="3ec72-854">tax id
</span><span class="sxs-lookup"><span data-stu-id="3ec72-854">tax id</span></span>
  
<span data-ttu-id="3ec72-855">número de identificação de imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-855">tax id number</span></span>
  
<span data-ttu-id="3ec72-856">id de CIF</span><span class="sxs-lookup"><span data-stu-id="3ec72-856">cif id</span></span>
  
<span data-ttu-id="3ec72-857">CIF nenhum</span><span class="sxs-lookup"><span data-stu-id="3ec72-857">cif no</span></span>
  
<span data-ttu-id="3ec72-858">id do espanhol cif</span><span class="sxs-lookup"><span data-stu-id="3ec72-858">spanish cif id</span></span>
  
<span data-ttu-id="3ec72-859">CIF</span><span class="sxs-lookup"><span data-stu-id="3ec72-859">cif</span></span>
  
<span data-ttu-id="3ec72-860">arquivo do imposto não</span><span class="sxs-lookup"><span data-stu-id="3ec72-860">tax file no</span></span>
  
<span data-ttu-id="3ec72-861">número de cif espanhol</span><span class="sxs-lookup"><span data-stu-id="3ec72-861">spanish cif number</span></span>
  
<span data-ttu-id="3ec72-862">

tax file number</span><span class="sxs-lookup"><span data-stu-id="3ec72-862">tax file number</span></span>
  
<span data-ttu-id="3ec72-863">Espanhol cif nenhum</span><span class="sxs-lookup"><span data-stu-id="3ec72-863">spanish cif no</span></span>
  
<span data-ttu-id="3ec72-864">imposto não</span><span class="sxs-lookup"><span data-stu-id="3ec72-864">tax no</span></span>
  
<span data-ttu-id="3ec72-865">número de imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-865">tax number</span></span>
  
<span data-ttu-id="3ec72-866">taxid #</span><span class="sxs-lookup"><span data-stu-id="3ec72-866">taxid#</span></span>
  
<span data-ttu-id="3ec72-867">taxno #</span><span class="sxs-lookup"><span data-stu-id="3ec72-867">taxno#</span></span>
  
<span data-ttu-id="3ec72-868">cifid #</span><span class="sxs-lookup"><span data-stu-id="3ec72-868">cifid#</span></span>
  
<span data-ttu-id="3ec72-869">spanishcifid #</span><span class="sxs-lookup"><span data-stu-id="3ec72-869">spanishcifid#</span></span>
  
<span data-ttu-id="3ec72-870">spanishcifno #</span><span class="sxs-lookup"><span data-stu-id="3ec72-870">spanishcifno#</span></span>
  
<span data-ttu-id="3ec72-871">número de contribuyente</span><span class="sxs-lookup"><span data-stu-id="3ec72-871">número de contribuyente</span></span>
  
<span data-ttu-id="3ec72-872">número de impuesto corporativo</span><span class="sxs-lookup"><span data-stu-id="3ec72-872">número de impuesto corporativo</span></span>
  
<span data-ttu-id="3ec72-873">número de identificación fiscal</span><span class="sxs-lookup"><span data-stu-id="3ec72-873">número de identificación fiscal</span></span>
  
<span data-ttu-id="3ec72-874">número de CIF</span><span class="sxs-lookup"><span data-stu-id="3ec72-874">cif número</span></span>
  
<span data-ttu-id="3ec72-875">cifnúmero #</span><span class="sxs-lookup"><span data-stu-id="3ec72-875">cifnúmero#</span></span>
  
## <a name="sweden"></a><span data-ttu-id="3ec72-876">Suécia</span><span class="sxs-lookup"><span data-stu-id="3ec72-876">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="3ec72-877">Formato</span><span class="sxs-lookup"><span data-stu-id="3ec72-877">Format</span></span>

<span data-ttu-id="3ec72-878">Dez dígitos e um símbolo no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="3ec72-878">Ten digits and a symbol in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ec72-879">Padrão</span><span class="sxs-lookup"><span data-stu-id="3ec72-879">Pattern</span></span>

<span data-ttu-id="3ec72-880">Dez dígitos e um símbolo:</span><span class="sxs-lookup"><span data-stu-id="3ec72-880">Ten digits and a symbol:</span></span>
  
-  <span data-ttu-id="3ec72-881">Seis dígitos que correspondem à data de nascimento (aammdd)</span><span class="sxs-lookup"><span data-stu-id="3ec72-881">Six digits that correspond to the birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="3ec72-882">Um sinal de adição, sinal de subtração ou barra invertida</span><span class="sxs-lookup"><span data-stu-id="3ec72-882">A plus sign, minus sign, or backslash</span></span>
    
- <span data-ttu-id="3ec72-883">Três dígitos que tornam a identificação do número exclusivo where:</span><span class="sxs-lookup"><span data-stu-id="3ec72-883">Three digits that make the identification number unique where:</span></span> 
    
  - <span data-ttu-id="3ec72-884">Para números emitidos antes de 1990, o sétimo e oitavo dígito identificar a região de nascimento ou foreign-born pessoas</span><span class="sxs-lookup"><span data-stu-id="3ec72-884">For numbers issued before 1990, the seventh and eighth digit identify the county of birth or foreign-born people</span></span>
    
  - <span data-ttu-id="3ec72-885">O dígito na posição mais à nono indica gênero por qualquer um dos ímpares para Masculino ou até mesmo fêmea</span><span class="sxs-lookup"><span data-stu-id="3ec72-885">The digit in the ninth position indicates gender by either odd for male or even for female</span></span>
    
- <span data-ttu-id="3ec72-886">Seleção de um dígito</span><span class="sxs-lookup"><span data-stu-id="3ec72-886">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="3ec72-887">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3ec72-887">Checksum</span></span>

<span data-ttu-id="3ec72-888">Sim</span><span class="sxs-lookup"><span data-stu-id="3ec72-888">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ec72-889">Definição</span><span class="sxs-lookup"><span data-stu-id="3ec72-889">Definition</span></span>

<span data-ttu-id="3ec72-890">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-890">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-891">A função `Func_sweden_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-891">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ec72-892">Uma palavra-chave da `Keywords_sweden_eu_tax_file_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="3ec72-892">A keyword from  `Keywords_sweden_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="3ec72-893">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-893">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-894">A função `Func_sweden_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-894">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="3ec72-895">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3ec72-895">Keywords</span></span>

#### <a name="keywordsswedeneutaxfilenumber"></a><span data-ttu-id="3ec72-896">Keywords_sweden_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3ec72-896">Keywords_sweden_eu_tax_file_number</span></span>

<span data-ttu-id="3ec72-897">tax id
</span><span class="sxs-lookup"><span data-stu-id="3ec72-897">tax id</span></span>
  
<span data-ttu-id="3ec72-898">id de imposto não.</span><span class="sxs-lookup"><span data-stu-id="3ec72-898">tax id no.</span></span>
  
<span data-ttu-id="3ec72-899">número de identificação de imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-899">tax id number</span></span>
  
<span data-ttu-id="3ec72-900">tax identification
</span><span class="sxs-lookup"><span data-stu-id="3ec72-900">tax identification</span></span>
  
<span data-ttu-id="3ec72-901">identificação de imposto #</span><span class="sxs-lookup"><span data-stu-id="3ec72-901">tax identification#</span></span>
  
<span data-ttu-id="3ec72-902">imposto não.</span><span class="sxs-lookup"><span data-stu-id="3ec72-902">tax no.</span></span>
  
<span data-ttu-id="3ec72-903">imposto #</span><span class="sxs-lookup"><span data-stu-id="3ec72-903">tax#</span></span>
  
<span data-ttu-id="3ec72-904">taxid #</span><span class="sxs-lookup"><span data-stu-id="3ec72-904">taxid#</span></span>
  
<span data-ttu-id="3ec72-905">arquivo impostos</span><span class="sxs-lookup"><span data-stu-id="3ec72-905">tax file</span></span>
  
<span data-ttu-id="3ec72-906">imposto não o arquivo.</span><span class="sxs-lookup"><span data-stu-id="3ec72-906">tax file no.</span></span>
  
<span data-ttu-id="3ec72-907">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="3ec72-907">personal id number</span></span>
  
<span data-ttu-id="3ec72-908">skatt id nummer</span><span class="sxs-lookup"><span data-stu-id="3ec72-908">skatt id nummer</span></span>
  
<span data-ttu-id="3ec72-909">skatt identifikation</span><span class="sxs-lookup"><span data-stu-id="3ec72-909">skatt identifikation</span></span>
  
<span data-ttu-id="3ec72-910">personnummer</span><span class="sxs-lookup"><span data-stu-id="3ec72-910">personnummer</span></span>
  
## <a name="uk"></a><span data-ttu-id="3ec72-911">REINO UNIDO</span><span class="sxs-lookup"><span data-stu-id="3ec72-911">UK</span></span>

### <a name="format"></a><span data-ttu-id="3ec72-912">Formato</span><span class="sxs-lookup"><span data-stu-id="3ec72-912">Format</span></span>

<span data-ttu-id="3ec72-913">Referência de contribuinte exclusivo (UTR): 10 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="3ec72-913">Unique Taxpayer Reference (UTR): 10 digits without spaces and delimiters</span></span>
  
<span data-ttu-id="3ec72-p103">Número de seguro de Nacional (NINO): Para obter detalhes, consulte a seção "número de Insurance nacional da Reino Unido (NINO)" em [quais tipos de informações confidenciais a procurar](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="3ec72-p103">National Insurance Number (NINO): For details, see the section "U.K. National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ec72-916">Padrão</span><span class="sxs-lookup"><span data-stu-id="3ec72-916">Pattern</span></span>

<span data-ttu-id="3ec72-917">Referência de contribuinte exclusivo (UTR): 10 dígitos</span><span class="sxs-lookup"><span data-stu-id="3ec72-917">Unique Taxpayer Reference (UTR): 10 digits</span></span>
  
<span data-ttu-id="3ec72-p104">Número de seguro de Nacional (NINO): Para obter detalhes, consulte a seção "número de Insurance nacional da Reino Unido (NINO)" em [quais tipos de informações confidenciais a procurar](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="3ec72-p104">National Insurance Number (NINO): For details, see the section "U.K. National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="checksum"></a><span data-ttu-id="3ec72-920">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3ec72-920">Checksum</span></span>

<span data-ttu-id="3ec72-921">Sim</span><span class="sxs-lookup"><span data-stu-id="3ec72-921">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ec72-922">Definição</span><span class="sxs-lookup"><span data-stu-id="3ec72-922">Definition</span></span>

<span data-ttu-id="3ec72-923">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="3ec72-923">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ec72-924">A função `Func_uk_eu_tax_file_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec72-924">The function  `Func_uk_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ec72-925">Uma palavra-chave da `Keywords_uk_eu_tax_file_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="3ec72-925">A keyword from  `Keywords_uk_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_uk_eu_tax_file_number" />
          <Match idRef="Keywords_uk_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3ec72-926">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="3ec72-926">Keywords</span></span>

#### <a name="keywordsukeutaxfilenumber"></a><span data-ttu-id="3ec72-927">Keywords_uk_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="3ec72-927">Keywords_uk_eu_tax_file_number</span></span>

<span data-ttu-id="3ec72-928">tax id
</span><span class="sxs-lookup"><span data-stu-id="3ec72-928">tax id</span></span>
  
<span data-ttu-id="3ec72-929">id de imposto não.</span><span class="sxs-lookup"><span data-stu-id="3ec72-929">tax id no.</span></span>
  
<span data-ttu-id="3ec72-930">número de identificação de imposto</span><span class="sxs-lookup"><span data-stu-id="3ec72-930">tax id number</span></span>
  
<span data-ttu-id="3ec72-931">tax identification
</span><span class="sxs-lookup"><span data-stu-id="3ec72-931">tax identification</span></span>
  
<span data-ttu-id="3ec72-932">identificação de imposto #</span><span class="sxs-lookup"><span data-stu-id="3ec72-932">tax identification#</span></span>
  
<span data-ttu-id="3ec72-933">imposto não.</span><span class="sxs-lookup"><span data-stu-id="3ec72-933">tax no.</span></span>
  
<span data-ttu-id="3ec72-934">imposto #</span><span class="sxs-lookup"><span data-stu-id="3ec72-934">tax#</span></span>
  
<span data-ttu-id="3ec72-935">taxid #</span><span class="sxs-lookup"><span data-stu-id="3ec72-935">taxid#</span></span>
  
<span data-ttu-id="3ec72-936">arquivo impostos</span><span class="sxs-lookup"><span data-stu-id="3ec72-936">tax file</span></span>
  
<span data-ttu-id="3ec72-937">imposto não o arquivo.</span><span class="sxs-lookup"><span data-stu-id="3ec72-937">tax file no.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3ec72-938">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ec72-938">See also</span></span>

[<span data-ttu-id="3ec72-939">O que os tipos de informações confidenciais procuram</span><span class="sxs-lookup"><span data-stu-id="3ec72-939">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)


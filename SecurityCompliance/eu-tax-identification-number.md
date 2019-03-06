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
ms.sourcegitcommit: ed822a776d3419853453583e882f3c61ca26d4b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2019
ms.locfileid: "30410906"
---
# <a name="eu-tax-identification-number"></a><span data-ttu-id="33911-104">Número de identificação do imposto da UE</span><span class="sxs-lookup"><span data-stu-id="33911-104">EU Tax Identification Number</span></span>

<span data-ttu-id="33911-105">Este tópico mostra o que uma política de prevenção de perda de dados (DLP) procura quando detecta o tipo de informação confidencial do número de identificação de imposto (TIN) da UE.</span><span class="sxs-lookup"><span data-stu-id="33911-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Tax Identification Number (TIN) sensitive information type.</span></span> <span data-ttu-id="33911-106">Esse tipo de informação confidencial define diferentes padrões, palavras-chave e outras evidências para cada país.</span><span class="sxs-lookup"><span data-stu-id="33911-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="33911-107">Áustria </span><span class="sxs-lookup"><span data-stu-id="33911-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="33911-108">Format</span><span class="sxs-lookup"><span data-stu-id="33911-108">Format</span></span>

<span data-ttu-id="33911-109">Nove dígitos com hífen opcional e barra para frente</span><span class="sxs-lookup"><span data-stu-id="33911-109">Nine digits with optional hyphen and forward slash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="33911-110">Padrão</span><span class="sxs-lookup"><span data-stu-id="33911-110">Pattern</span></span>

<span data-ttu-id="33911-111">Nove dígitos com hífen opcional e barra para frente:</span><span class="sxs-lookup"><span data-stu-id="33911-111">Nine digits with optional hyphen and forward slash:</span></span>
  
-  <span data-ttu-id="33911-112">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="33911-112">Two digits</span></span> 
    
- <span data-ttu-id="33911-113">Um hífen (opcional)</span><span class="sxs-lookup"><span data-stu-id="33911-113">A hyphen (optional)</span></span>
    
- <span data-ttu-id="33911-114">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="33911-114">Three digits</span></span>
    
- <span data-ttu-id="33911-115">Uma barra (opcional)</span><span class="sxs-lookup"><span data-stu-id="33911-115">A forward slash (optional)</span></span>
    
- <span data-ttu-id="33911-116">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="33911-116">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="33911-117">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="33911-117">Checksum</span></span>

<span data-ttu-id="33911-118">Sim</span><span class="sxs-lookup"><span data-stu-id="33911-118">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="33911-119">Definição</span><span class="sxs-lookup"><span data-stu-id="33911-119">Definition</span></span>

<span data-ttu-id="33911-120">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-120">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-121">A função `Func_austria_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-121">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="33911-122">Uma palavra- `Keywords_austria_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="33911-122">A keyword from  `Keywords_austria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="33911-123">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-123">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-124">A função `Func_austria_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-124">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="33911-125">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="33911-125">Keywords</span></span>

#### <a name="keywordsaustriaeutaxfilenumber"></a><span data-ttu-id="33911-126">Keywords_austria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="33911-126">Keywords_austria_eu_tax_file_number</span></span>

<span data-ttu-id="33911-127">número do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-127">tax number</span></span>
  
<span data-ttu-id="33911-128">number</span><span class="sxs-lookup"><span data-stu-id="33911-128">number</span></span>
  
<span data-ttu-id="33911-129">número de registro de imposto</span><span class="sxs-lookup"><span data-stu-id="33911-129">tax registration number</span></span>
  
<span data-ttu-id="33911-130">tax id</span><span class="sxs-lookup"><span data-stu-id="33911-130">tax id</span></span>
  
<span data-ttu-id="33911-131">St.Nr.</span><span class="sxs-lookup"><span data-stu-id="33911-131">st.nr.</span></span>
  
<span data-ttu-id="33911-132">steuernummer</span><span class="sxs-lookup"><span data-stu-id="33911-132">steuernummer</span></span>
  
## <a name="belgium"></a><span data-ttu-id="33911-133">Bélgica </span><span class="sxs-lookup"><span data-stu-id="33911-133">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="33911-134">Format</span><span class="sxs-lookup"><span data-stu-id="33911-134">Format</span></span>

<span data-ttu-id="33911-135">11 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="33911-135">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="33911-136">Padrão</span><span class="sxs-lookup"><span data-stu-id="33911-136">Pattern</span></span>

<span data-ttu-id="33911-137">11 dígitos:</span><span class="sxs-lookup"><span data-stu-id="33911-137">11 digits:</span></span>
  
- <span data-ttu-id="33911-138">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="33911-138">Two digits</span></span>
    
- <span data-ttu-id="33911-139">Um "0" ou "1"</span><span class="sxs-lookup"><span data-stu-id="33911-139">A "0" or "1"</span></span>
    
- <span data-ttu-id="33911-140">Um dígito</span><span class="sxs-lookup"><span data-stu-id="33911-140">One digit</span></span>
    
- <span data-ttu-id="33911-141">"0" ou "1" ou "2" ou "3"</span><span class="sxs-lookup"><span data-stu-id="33911-141">A "0" or "1" or "2" or "3"</span></span> 
    
- <span data-ttu-id="33911-142">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="33911-142">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="33911-143">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="33911-143">Checksum</span></span>

<span data-ttu-id="33911-144">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="33911-144">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="33911-145">Definição</span><span class="sxs-lookup"><span data-stu-id="33911-145">Definition</span></span>

<span data-ttu-id="33911-146">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-146">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-147">A expressão `Regex_belgium_eu_tax_file_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-147">The regular expression  `Regex_belgium_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="33911-148">Uma palavra- `Keywords_belgium_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="33911-148">A keyword from  `Keywords_belgium_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_tax_file_number" />
          <Match idRef="Keywords_belgium_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="33911-149">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="33911-149">Keywords</span></span>

#### <a name="keywordsbelgiumeutaxfilenumber"></a><span data-ttu-id="33911-150">Keywords_belgium_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="33911-150">Keywords_belgium_eu_tax_file_number</span></span>

<span data-ttu-id="33911-151">número do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-151">tax number</span></span>
  
<span data-ttu-id="33911-152">número de Registro Nacional</span><span class="sxs-lookup"><span data-stu-id="33911-152">national registration number</span></span>
  
<span data-ttu-id="33911-153">número de registro de imposto</span><span class="sxs-lookup"><span data-stu-id="33911-153">tax registration number</span></span>
  
<span data-ttu-id="33911-154">tax id</span><span class="sxs-lookup"><span data-stu-id="33911-154">tax id</span></span>
  
<span data-ttu-id="33911-155">nse</span><span class="sxs-lookup"><span data-stu-id="33911-155">nif</span></span>
  
<span data-ttu-id="33911-156">nse</span><span class="sxs-lookup"><span data-stu-id="33911-156">nif#</span></span>
  
<span data-ttu-id="33911-157">Numéro de Registro Nacional</span><span class="sxs-lookup"><span data-stu-id="33911-157">numéro de registre national</span></span>
  
<span data-ttu-id="33911-158">Numéro d'identification fiscal</span><span class="sxs-lookup"><span data-stu-id="33911-158">numéro d'identification fiscale</span></span>
  
## <a name="bulgaria"></a><span data-ttu-id="33911-159">Bulgária</span><span class="sxs-lookup"><span data-stu-id="33911-159">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="33911-160">Format</span><span class="sxs-lookup"><span data-stu-id="33911-160">Format</span></span>

<span data-ttu-id="33911-161">Dez dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="33911-161">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="33911-162">Padrão</span><span class="sxs-lookup"><span data-stu-id="33911-162">Pattern</span></span>

<span data-ttu-id="33911-163">10 dígitos</span><span class="sxs-lookup"><span data-stu-id="33911-163">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="33911-164">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="33911-164">Checksum</span></span>

<span data-ttu-id="33911-165">Sim</span><span class="sxs-lookup"><span data-stu-id="33911-165">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="33911-166">Definição</span><span class="sxs-lookup"><span data-stu-id="33911-166">Definition</span></span>

<span data-ttu-id="33911-167">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-167">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-168">A função `Func_bulgaria_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-168">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="33911-169">Uma palavra- `Keywords_bulgaria_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="33911-169">A keyword from  `Keywords_bulgaria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="33911-170">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-170">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-171">A função `Func_bulgaria_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-171">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="33911-172">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="33911-172">Keywords</span></span>

#### <a name="keywordsbulgariaeutaxfilenumber"></a><span data-ttu-id="33911-173">Keywords_bulgaria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="33911-173">Keywords_bulgaria_eu_tax_file_number</span></span>

<span data-ttu-id="33911-174">bucn</span><span class="sxs-lookup"><span data-stu-id="33911-174">bucn</span></span>
  
<span data-ttu-id="33911-175">número civil uniforme</span><span class="sxs-lookup"><span data-stu-id="33911-175">uniform civil number</span></span>
  
<span data-ttu-id="33911-176">bucn #</span><span class="sxs-lookup"><span data-stu-id="33911-176">bucn#</span></span>
  
<span data-ttu-id="33911-177">uniformcivilnumber #</span><span class="sxs-lookup"><span data-stu-id="33911-177">uniformcivilnumber#</span></span>
  
<span data-ttu-id="33911-178">ID civil uniforme</span><span class="sxs-lookup"><span data-stu-id="33911-178">uniform civil id</span></span>
  
<span data-ttu-id="33911-179">Nenhum civil uniforme</span><span class="sxs-lookup"><span data-stu-id="33911-179">uniform civil no</span></span>
  
<span data-ttu-id="33911-180">Egn</span><span class="sxs-lookup"><span data-stu-id="33911-180">egn</span></span>
  
<span data-ttu-id="33911-181">número civil uniforme búlgaro</span><span class="sxs-lookup"><span data-stu-id="33911-181">bulgarian uniform civil number</span></span>
  
<span data-ttu-id="33911-182">uniformcivilno #</span><span class="sxs-lookup"><span data-stu-id="33911-182">uniformcivilno#</span></span>
  
<span data-ttu-id="33911-183">Egn #</span><span class="sxs-lookup"><span data-stu-id="33911-183">egn#</span></span>
  
<span data-ttu-id="33911-184">униформ граждански номер</span><span class="sxs-lookup"><span data-stu-id="33911-184">униформ граждански номер</span></span>
  
<span data-ttu-id="33911-185">ID униформ</span><span class="sxs-lookup"><span data-stu-id="33911-185">униформ id</span></span>
  
<span data-ttu-id="33911-186">ID de граждански униформ</span><span class="sxs-lookup"><span data-stu-id="33911-186">униформ граждански id</span></span>
  
<span data-ttu-id="33911-187">униформ граждански не</span><span class="sxs-lookup"><span data-stu-id="33911-187">униформ граждански не</span></span>
  
## <a name="croatia"></a><span data-ttu-id="33911-188">Croácia</span><span class="sxs-lookup"><span data-stu-id="33911-188">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="33911-189">Format</span><span class="sxs-lookup"><span data-stu-id="33911-189">Format</span></span>

<span data-ttu-id="33911-190">11 dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="33911-190">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="33911-191">Padrão</span><span class="sxs-lookup"><span data-stu-id="33911-191">Pattern</span></span>

<span data-ttu-id="33911-192">11 dígitos:</span><span class="sxs-lookup"><span data-stu-id="33911-192">11 digits:</span></span>
  
- <span data-ttu-id="33911-193">Dez dígitos, escolhidos aleatoriamente</span><span class="sxs-lookup"><span data-stu-id="33911-193">Ten digits, randomly chosen</span></span>
    
- <span data-ttu-id="33911-194">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="33911-194">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="33911-195">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="33911-195">Checksum</span></span>

<span data-ttu-id="33911-196">Sim</span><span class="sxs-lookup"><span data-stu-id="33911-196">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="33911-197">Definição</span><span class="sxs-lookup"><span data-stu-id="33911-197">Definition</span></span>

<span data-ttu-id="33911-198">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-198">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-199">A função `Func_croatia_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-199">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="33911-200">Uma palavra- `Keywords_croatia_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="33911-200">A keyword from  `Keywords_croatia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="33911-201">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-201">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-202">A função `Func_croatia_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-202">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="33911-203">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="33911-203">Keywords</span></span>

#### <a name="keywordscroatiaeutaxfilenumber"></a><span data-ttu-id="33911-204">Keywords_croatia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="33911-204">Keywords_croatia_eu_tax_file_number</span></span>

<span data-ttu-id="33911-205">número do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-205">tax number</span></span>
  
<span data-ttu-id="33911-206">imposto</span><span class="sxs-lookup"><span data-stu-id="33911-206">tax</span></span>
  
<span data-ttu-id="33911-207">tax id</span><span class="sxs-lookup"><span data-stu-id="33911-207">tax id</span></span>
  
<span data-ttu-id="33911-208">OID</span><span class="sxs-lookup"><span data-stu-id="33911-208">oid</span></span>
  
<span data-ttu-id="33911-209">OID</span><span class="sxs-lookup"><span data-stu-id="33911-209">oid#</span></span>
  
<span data-ttu-id="33911-210">porezni broj</span><span class="sxs-lookup"><span data-stu-id="33911-210">porezni broj</span></span>
  
## <a name="cyprus"></a><span data-ttu-id="33911-211">Chipre</span><span class="sxs-lookup"><span data-stu-id="33911-211">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="33911-212">Format</span><span class="sxs-lookup"><span data-stu-id="33911-212">Format</span></span>

<span data-ttu-id="33911-213">Oito dígitos e uma letra no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="33911-213">Eight digits and one letter in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="33911-214">Padrão</span><span class="sxs-lookup"><span data-stu-id="33911-214">Pattern</span></span>

<span data-ttu-id="33911-215">Oito dígitos e uma letra:</span><span class="sxs-lookup"><span data-stu-id="33911-215">Eight digits and one letter:</span></span>
  
-  <span data-ttu-id="33911-216">Um "0"</span><span class="sxs-lookup"><span data-stu-id="33911-216">A "0"</span></span> 
    
- <span data-ttu-id="33911-217">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="33911-217">Seven digits</span></span>
    
- <span data-ttu-id="33911-218">Uma letra (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="33911-218">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="33911-219">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="33911-219">Checksum</span></span>

<span data-ttu-id="33911-220">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="33911-220">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="33911-221">Definição</span><span class="sxs-lookup"><span data-stu-id="33911-221">Definition</span></span>

<span data-ttu-id="33911-222">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-222">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-223">A função `Func_cyprus_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-223">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="33911-224">Uma palavra- `Keywords_cyprus_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="33911-224">A keyword from  `Keywords_cyprus_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="33911-225">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-225">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-226">A função `Func_cyprus_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-226">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="33911-227">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="33911-227">Keywords</span></span>

#### <a name="keywordscypruseutaxfilenumber"></a><span data-ttu-id="33911-228">Keywords_cyprus_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="33911-228">Keywords_cyprus_eu_tax_file_number</span></span>

<span data-ttu-id="33911-229">número do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-229">tax number</span></span>
  
<span data-ttu-id="33911-230">imposto</span><span class="sxs-lookup"><span data-stu-id="33911-230">tax</span></span>
  
<span data-ttu-id="33911-231">tax id</span><span class="sxs-lookup"><span data-stu-id="33911-231">tax id</span></span>
  
<span data-ttu-id="33911-232">código de identificação de imposto</span><span class="sxs-lookup"><span data-stu-id="33911-232">tax identification code</span></span>
  
<span data-ttu-id="33911-233">TIC</span><span class="sxs-lookup"><span data-stu-id="33911-233">tic</span></span>
  
<span data-ttu-id="33911-234">TIC #</span><span class="sxs-lookup"><span data-stu-id="33911-234">tic#</span></span>
  
<span data-ttu-id="33911-235">αριθμός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="33911-235">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="33911-236">φορολογική ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="33911-236">φορολογική ταυτότητα</span></span>
  
<span data-ttu-id="33911-237">κωδικός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="33911-237">κωδικός φορολογικού μητρώου</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="33911-238">República Tcheca</span><span class="sxs-lookup"><span data-stu-id="33911-238">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="33911-239">Format</span><span class="sxs-lookup"><span data-stu-id="33911-239">Format</span></span>

<span data-ttu-id="33911-240">Nove ou dez dígitos com uma barra invertida opcional</span><span class="sxs-lookup"><span data-stu-id="33911-240">Nine or ten digits with an optional backslash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="33911-241">Padrão</span><span class="sxs-lookup"><span data-stu-id="33911-241">Pattern</span></span>

<span data-ttu-id="33911-242">Nove ou dez dígitos com uma barra invertida opcional:</span><span class="sxs-lookup"><span data-stu-id="33911-242">Nine or ten digits with an optional backslashl:</span></span>
  
- <span data-ttu-id="33911-243">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="33911-243">Six digits</span></span> 
    
- <span data-ttu-id="33911-244">Uma barra invertida (opcional)</span><span class="sxs-lookup"><span data-stu-id="33911-244">A backslash (optional)</span></span>
    
- <span data-ttu-id="33911-245">Três ou quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="33911-245">Three or four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="33911-246">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="33911-246">Checksum</span></span>

<span data-ttu-id="33911-247">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="33911-247">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="33911-248">Definição</span><span class="sxs-lookup"><span data-stu-id="33911-248">Definition</span></span>

<span data-ttu-id="33911-249">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-249">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-250">A expressão `Regex_czech_republic_eu_tax_file_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-250">The regular expression  `Regex_czech_republic_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="33911-251">Uma palavra- `Keywords_czech_republic_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="33911-251">A keyword from  `Keywords_czech_republic_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_tax_file_number" />
          <Match idRef="Keywords_czech_republic_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="33911-252">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="33911-252">Keywords</span></span>

#### <a name="keywordsczechrepubliceutaxfilenumber"></a><span data-ttu-id="33911-253">Keywords_czech_republic_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="33911-253">Keywords_czech_republic_eu_tax_file_number</span></span>

<span data-ttu-id="33911-254">número do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-254">tax number</span></span>
  
<span data-ttu-id="33911-255">imposto</span><span class="sxs-lookup"><span data-stu-id="33911-255">tax</span></span>
  
<span data-ttu-id="33911-256">tax id</span><span class="sxs-lookup"><span data-stu-id="33911-256">tax id</span></span>
  
<span data-ttu-id="33911-257">número pessoal</span><span class="sxs-lookup"><span data-stu-id="33911-257">personal number</span></span>
  
<span data-ttu-id="33911-258">daňové číslo</span><span class="sxs-lookup"><span data-stu-id="33911-258">daňové číslo</span></span>
  
<span data-ttu-id="33911-259">osobní číslo</span><span class="sxs-lookup"><span data-stu-id="33911-259">osobní číslo</span></span>
  
## <a name="denmark"></a><span data-ttu-id="33911-260">Dinamarca</span><span class="sxs-lookup"><span data-stu-id="33911-260">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="33911-261">Format</span><span class="sxs-lookup"><span data-stu-id="33911-261">Format</span></span>

<span data-ttu-id="33911-262">Dez dígitos contendo um hífen</span><span class="sxs-lookup"><span data-stu-id="33911-262">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="33911-263">Padrão</span><span class="sxs-lookup"><span data-stu-id="33911-263">Pattern</span></span>

<span data-ttu-id="33911-264">Dez dígitos contendo um hífen:</span><span class="sxs-lookup"><span data-stu-id="33911-264">Ten digits containing a hyphenl:</span></span>
  
-  <span data-ttu-id="33911-265">Seis dígitos que correspondem à data de nascimento (DDMMAA)</span><span class="sxs-lookup"><span data-stu-id="33911-265">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="33911-266">Um hífen</span><span class="sxs-lookup"><span data-stu-id="33911-266">A hyphen</span></span>
    
- <span data-ttu-id="33911-267">Quatro dígitos que correspondem a um número de sequência onde o primeiro dígito corresponde ao século do nascimento e o último dígito corresponde ao sexo da pessoa (ímpar para macho e par para fêmea)</span><span class="sxs-lookup"><span data-stu-id="33911-267">Four digits that correspond to a sequence number where the first digit corresponds to the century of birth and the last digit corresponds to the individual's gender (odd for male and even for female)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="33911-268">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="33911-268">Checksum</span></span>

<span data-ttu-id="33911-269">Sim</span><span class="sxs-lookup"><span data-stu-id="33911-269">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="33911-270">Definição</span><span class="sxs-lookup"><span data-stu-id="33911-270">Definition</span></span>

<span data-ttu-id="33911-271">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-271">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-272">A função `Func_denmark_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-272">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="33911-273">Uma palavra- `Keywords_denmark_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="33911-273">A keyword from  `Keywords_denmark_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="33911-274">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-275">A função `Func_denmark_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-275">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="33911-276">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="33911-276">Keywords</span></span>

#### <a name="keywordsdenmarkeutaxfilenumber"></a><span data-ttu-id="33911-277">Keywords_denmark_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="33911-277">Keywords_denmark_eu_tax_file_number</span></span>

<span data-ttu-id="33911-278">número do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-278">tax number</span></span>
  
<span data-ttu-id="33911-279">imposto</span><span class="sxs-lookup"><span data-stu-id="33911-279">tax</span></span>
  
<span data-ttu-id="33911-280">tax id</span><span class="sxs-lookup"><span data-stu-id="33911-280">tax id</span></span>
  
<span data-ttu-id="33911-281">número de CPR</span><span class="sxs-lookup"><span data-stu-id="33911-281">cpr number</span></span>
  
<span data-ttu-id="33911-282">pedir</span><span class="sxs-lookup"><span data-stu-id="33911-282">cpr#</span></span>
  
<span data-ttu-id="33911-283">Skat Nummer</span><span class="sxs-lookup"><span data-stu-id="33911-283">skat nummer</span></span>
  
<span data-ttu-id="33911-284">ID Skat</span><span class="sxs-lookup"><span data-stu-id="33911-284">skat id</span></span>
  
## <a name="estonia"></a><span data-ttu-id="33911-285">Estônia</span><span class="sxs-lookup"><span data-stu-id="33911-285">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="33911-286">Format</span><span class="sxs-lookup"><span data-stu-id="33911-286">Format</span></span>

<span data-ttu-id="33911-287">11 dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="33911-287">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="33911-288">Padrão</span><span class="sxs-lookup"><span data-stu-id="33911-288">Pattern</span></span>

<span data-ttu-id="33911-289">11 dígitos:</span><span class="sxs-lookup"><span data-stu-id="33911-289">11 digits:</span></span>
  
-  <span data-ttu-id="33911-290">Um dígito que corresponde ao gênero e ao século de nascimento onde um número ímpar indica macho e o número par indica fêmea da seguinte maneira: 1, 2 para o século 19; 3, 4 para o século 20; e 5, 6 para o século 21</span><span class="sxs-lookup"><span data-stu-id="33911-290">One digit that corresponds to gender and century of birth where an odd number indicates male and the even number indicates female as follows: 1, 2 for the 19th century; 3, 4 for the 20th century; and 5, 6 for the 21st century</span></span> 
    
- <span data-ttu-id="33911-291">Seis dígitos que correspondem à data de nascimento (AAMMDD)</span><span class="sxs-lookup"><span data-stu-id="33911-291">Six digits that correspond to birth date (YYMMDD)</span></span>
    
- <span data-ttu-id="33911-292">Três dígitos que correspondem a um número de série separando as pessoas que nasceu na mesma data</span><span class="sxs-lookup"><span data-stu-id="33911-292">Three digits that correspond to a serial number separating persons born on the same date</span></span>
    
- <span data-ttu-id="33911-293">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="33911-293">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="33911-294">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="33911-294">Checksum</span></span>

<span data-ttu-id="33911-295">Sim</span><span class="sxs-lookup"><span data-stu-id="33911-295">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="33911-296">Definição</span><span class="sxs-lookup"><span data-stu-id="33911-296">Definition</span></span>

<span data-ttu-id="33911-297">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-297">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-298">A função `Func_estonia_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-298">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="33911-299">Uma palavra- `Keywords_estonia_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="33911-299">A keyword from  `Keywords_estonia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="33911-300">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-300">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-301">A função `Func_estonia_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-301">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="33911-302">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="33911-302">Keywords</span></span>

#### <a name="keywordsestoniaeutaxfilenumber"></a><span data-ttu-id="33911-303">Keywords_estonia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="33911-303">Keywords_estonia_eu_tax_file_number</span></span>

<span data-ttu-id="33911-304">número do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-304">tax number</span></span>
  
<span data-ttu-id="33911-305">imposto</span><span class="sxs-lookup"><span data-stu-id="33911-305">tax</span></span>
  
<span data-ttu-id="33911-306">tax id</span><span class="sxs-lookup"><span data-stu-id="33911-306">tax id</span></span>
  
<span data-ttu-id="33911-307">código pessoal</span><span class="sxs-lookup"><span data-stu-id="33911-307">personal code</span></span>
  
<span data-ttu-id="33911-308">maksunumber</span><span class="sxs-lookup"><span data-stu-id="33911-308">maksunumber</span></span>
  
<span data-ttu-id="33911-309">ID maksu</span><span class="sxs-lookup"><span data-stu-id="33911-309">maksu id</span></span>
  
<span data-ttu-id="33911-310">isikukood</span><span class="sxs-lookup"><span data-stu-id="33911-310">isikukood</span></span>
  
## <a name="finland"></a><span data-ttu-id="33911-311">Finlândia</span><span class="sxs-lookup"><span data-stu-id="33911-311">Finland</span></span>

### <a name="format"></a><span data-ttu-id="33911-312">Format</span><span class="sxs-lookup"><span data-stu-id="33911-312">Format</span></span>

<span data-ttu-id="33911-313">Uma combinação de 11 caracteres de dígitos, letras e sinal de mais e de menos</span><span class="sxs-lookup"><span data-stu-id="33911-313">An 11-character combination of digits, letters, and plus and minus sign</span></span>
  
### <a name="pattern"></a><span data-ttu-id="33911-314">Padrão</span><span class="sxs-lookup"><span data-stu-id="33911-314">Pattern</span></span>

<span data-ttu-id="33911-315">Uma combinação de 11 caracteres de dígitos, letras e sinal de mais e menos:</span><span class="sxs-lookup"><span data-stu-id="33911-315">An 11-character combination of digits, letters, and plus and minus sign:</span></span>
  
- <span data-ttu-id="33911-316">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="33911-316">Six digits</span></span>
    
- <span data-ttu-id="33911-317">Uma das seguintes opções: um sinal de adição, um sinal de menos ou a letra "A" (não diferencia maiúsculas de minúsculas) onde o sinal de mais significa que nasceu entre 1800-1899, o sinal de menos significa que nasceu entre 1900-1999 e "A" significa que nasceu 2000 e depois</span><span class="sxs-lookup"><span data-stu-id="33911-317">One of the following: a plus sign, a minus sign, or the letter "A" (not case sensitive) where the plus sign means born between 1800-1899, the minus sign means born between 1900-1999, and "A" means born 2000 and after</span></span>
    
- <span data-ttu-id="33911-318">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="33911-318">Three digits</span></span>
    
- <span data-ttu-id="33911-319">Uma letra ou um número</span><span class="sxs-lookup"><span data-stu-id="33911-319">One letter or one number</span></span>
    
### <a name="checksum"></a><span data-ttu-id="33911-320">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="33911-320">Checksum</span></span>

<span data-ttu-id="33911-321">Sim</span><span class="sxs-lookup"><span data-stu-id="33911-321">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="33911-322">Definição</span><span class="sxs-lookup"><span data-stu-id="33911-322">Definition</span></span>

<span data-ttu-id="33911-323">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-323">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-324">A função `Func_finland_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-324">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="33911-325">Uma palavra- `Keywords_finland_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="33911-325">A keyword from  `Keywords_finland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="33911-326">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-326">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-327">A função `Func_finland_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-327">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="33911-328">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="33911-328">Keywords</span></span>

#### <a name="keywordsfinlandeutaxfilenumber"></a><span data-ttu-id="33911-329">Keywords_finland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="33911-329">Keywords_finland_eu_tax_file_number</span></span>

<span data-ttu-id="33911-330">identification number</span><span class="sxs-lookup"><span data-stu-id="33911-330">identification number</span></span>
  
<span data-ttu-id="33911-331">ID pessoal</span><span class="sxs-lookup"><span data-stu-id="33911-331">personal id</span></span>
  
<span data-ttu-id="33911-332">número de identidade</span><span class="sxs-lookup"><span data-stu-id="33911-332">identity number</span></span>
  
<span data-ttu-id="33911-333">número de ID nacional da finlandês</span><span class="sxs-lookup"><span data-stu-id="33911-333">finnish national id number</span></span>
  
<span data-ttu-id="33911-334">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="33911-334">personalidnumber#</span></span>
  
<span data-ttu-id="33911-335">national identification number</span><span class="sxs-lookup"><span data-stu-id="33911-335">national identification number</span></span>
  
<span data-ttu-id="33911-336">número de identificação</span><span class="sxs-lookup"><span data-stu-id="33911-336">id number</span></span>
  
<span data-ttu-id="33911-337">n º de ID nacional</span><span class="sxs-lookup"><span data-stu-id="33911-337">national id no.</span></span>
  
<span data-ttu-id="33911-338">número de ID nacional</span><span class="sxs-lookup"><span data-stu-id="33911-338">national id number</span></span>
  
<span data-ttu-id="33911-339">ID não</span><span class="sxs-lookup"><span data-stu-id="33911-339">id no</span></span>
  
<span data-ttu-id="33911-340">tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="33911-340">tunnistenumero</span></span>
  
<span data-ttu-id="33911-341">henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="33911-341">henkilötunnus</span></span>
  
<span data-ttu-id="33911-342">yksilöllinen henkilökohtainen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="33911-342">yksilöllinen henkilökohtainen tunnistenumero</span></span>
  
<span data-ttu-id="33911-343">ainutlaatuinen henkilökohtainen Tunnus</span><span class="sxs-lookup"><span data-stu-id="33911-343">ainutlaatuinen henkilökohtainen tunnus</span></span>
  
<span data-ttu-id="33911-344">identiteetti numero</span><span class="sxs-lookup"><span data-stu-id="33911-344">identiteetti numero</span></span>
  
<span data-ttu-id="33911-345">Suomen Kansallinen henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="33911-345">suomen kansallinen henkilötunnus</span></span>
  
<span data-ttu-id="33911-346">henkilötunnusnumero #</span><span class="sxs-lookup"><span data-stu-id="33911-346">henkilötunnusnumero#</span></span>
  
<span data-ttu-id="33911-347">kansallisen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="33911-347">kansallisen tunnistenumero</span></span>
  
<span data-ttu-id="33911-348">tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="33911-348">tunnusnumero</span></span>
  
<span data-ttu-id="33911-349">Kansallinen Tunnus numero</span><span class="sxs-lookup"><span data-stu-id="33911-349">kansallinen tunnus numero</span></span>
  
## <a name="france"></a><span data-ttu-id="33911-350">França</span><span class="sxs-lookup"><span data-stu-id="33911-350">France</span></span>

### <a name="format"></a><span data-ttu-id="33911-351">Format</span><span class="sxs-lookup"><span data-stu-id="33911-351">Format</span></span>

<span data-ttu-id="33911-352">13 dígitos para pessoas e nove dígitos para entidades</span><span class="sxs-lookup"><span data-stu-id="33911-352">13 digits for individuals and nine digits for entities</span></span>
  
### <a name="pattern"></a><span data-ttu-id="33911-353">Padrão</span><span class="sxs-lookup"><span data-stu-id="33911-353">Pattern</span></span>

<span data-ttu-id="33911-354">13 dígitos para pessoas:</span><span class="sxs-lookup"><span data-stu-id="33911-354">13 digits for individuals:</span></span>
  
- <span data-ttu-id="33911-355">Um dígito que deve ser 0, 1, 2 ou 3</span><span class="sxs-lookup"><span data-stu-id="33911-355">One digit that must be 0, 1, 2, or 3</span></span>
    
- <span data-ttu-id="33911-356">12 dígitos</span><span class="sxs-lookup"><span data-stu-id="33911-356">12 digits</span></span>
    
<span data-ttu-id="33911-357">Nove dígitos para entidades</span><span class="sxs-lookup"><span data-stu-id="33911-357">Nine digits for entities</span></span>
  
### <a name="checksum"></a><span data-ttu-id="33911-358">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="33911-358">Checksum</span></span>

<span data-ttu-id="33911-359">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="33911-359">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="33911-360">Definição</span><span class="sxs-lookup"><span data-stu-id="33911-360">Definition</span></span>

<span data-ttu-id="33911-361">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-361">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-362">A função `Func_france_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-362">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="33911-363">Uma palavra- `Keywords_france_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="33911-363">A keyword from  `Keywords_france_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="33911-364">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-365">A função `Func_france_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-365">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="33911-366">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="33911-366">Keywords</span></span>

#### <a name="keywordsfranceeutaxfilenumber"></a><span data-ttu-id="33911-367">Keywords_france_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="33911-367">Keywords_france_eu_tax_file_number</span></span>

<span data-ttu-id="33911-368">número de identificação do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-368">tax identification number</span></span>
  
<span data-ttu-id="33911-369">número do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-369">tax number</span></span>
  
<span data-ttu-id="33911-370">tax id</span><span class="sxs-lookup"><span data-stu-id="33911-370">tax id</span></span>
  
<span data-ttu-id="33911-371">Numéro d'identification fiscal</span><span class="sxs-lookup"><span data-stu-id="33911-371">numéro d'identification fiscale</span></span>
  
## <a name="germany"></a><span data-ttu-id="33911-372">Alemanha</span><span class="sxs-lookup"><span data-stu-id="33911-372">Germany</span></span>

### <a name="format"></a><span data-ttu-id="33911-373">Format</span><span class="sxs-lookup"><span data-stu-id="33911-373">Format</span></span>

<span data-ttu-id="33911-374">11 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="33911-374">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="33911-375">Padrão</span><span class="sxs-lookup"><span data-stu-id="33911-375">Pattern</span></span>

<span data-ttu-id="33911-376">11 dígitos:</span><span class="sxs-lookup"><span data-stu-id="33911-376">11 digits :</span></span>
  
-  <span data-ttu-id="33911-377">Dez dígitos</span><span class="sxs-lookup"><span data-stu-id="33911-377">Ten digits</span></span> 
    
- <span data-ttu-id="33911-378">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="33911-378">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="33911-379">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="33911-379">Checksum</span></span>

<span data-ttu-id="33911-380">Sim</span><span class="sxs-lookup"><span data-stu-id="33911-380">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="33911-381">Definição</span><span class="sxs-lookup"><span data-stu-id="33911-381">Definition</span></span>

<span data-ttu-id="33911-382">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-382">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-383">A função `Func_germany_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-383">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="33911-384">Uma palavra- `Keywords_germany_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="33911-384">A keyword from  `Keywords_germany_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="33911-385">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-385">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-386">A função `Func_germany_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-386">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="33911-387">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="33911-387">Keywords</span></span>

#### <a name="keywordsgermanyeutaxfilenumber"></a><span data-ttu-id="33911-388">Keywords_germany_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="33911-388">Keywords_germany_eu_tax_file_number</span></span>

<span data-ttu-id="33911-389">número do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-389">tax number</span></span>
  
<span data-ttu-id="33911-390">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-390">tax no.</span></span>
  
<span data-ttu-id="33911-391">taxno #</span><span class="sxs-lookup"><span data-stu-id="33911-391">taxno#</span></span>
  
<span data-ttu-id="33911-392">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="33911-392">taxnumber#</span></span>
  
<span data-ttu-id="33911-393">taxnumber</span><span class="sxs-lookup"><span data-stu-id="33911-393">taxnumber</span></span>
  
<span data-ttu-id="33911-394">tax id</span><span class="sxs-lookup"><span data-stu-id="33911-394">tax id</span></span>
  
<span data-ttu-id="33911-395">táxi #</span><span class="sxs-lookup"><span data-stu-id="33911-395">taxid#</span></span>
  
<span data-ttu-id="33911-396">número de identificação do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-396">tax identification number</span></span>
  
<span data-ttu-id="33911-397">n º de identificação de imposto</span><span class="sxs-lookup"><span data-stu-id="33911-397">tax identification no.</span></span>
  
<span data-ttu-id="33911-398">steuernummer</span><span class="sxs-lookup"><span data-stu-id="33911-398">steuernummer</span></span>
  
<span data-ttu-id="33911-399">ID Steuer</span><span class="sxs-lookup"><span data-stu-id="33911-399">steuer id</span></span>
  
<span data-ttu-id="33911-400">steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="33911-400">steueridentifikationsnummer</span></span>
  
## <a name="greece"></a><span data-ttu-id="33911-401">Grécia</span><span class="sxs-lookup"><span data-stu-id="33911-401">Greece</span></span>

### <a name="format"></a><span data-ttu-id="33911-402">Format</span><span class="sxs-lookup"><span data-stu-id="33911-402">Format</span></span>

<span data-ttu-id="33911-403">Nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="33911-403">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="33911-404">Padrão</span><span class="sxs-lookup"><span data-stu-id="33911-404">Pattern</span></span>

<span data-ttu-id="33911-405">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="33911-405">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="33911-406">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="33911-406">Checksum</span></span>

<span data-ttu-id="33911-407">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="33911-407">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="33911-408">Definição</span><span class="sxs-lookup"><span data-stu-id="33911-408">Definition</span></span>

<span data-ttu-id="33911-409">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-409">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-410">A expressão `Regex_greece_eu_tax_file_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-410">The regular expression  `Regex_greece_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="33911-411">Uma palavra- `Keywords_greece_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="33911-411">A keyword from  `Keywords_greece_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_tax_file_number" />
          <Match idRef="Keywords_greece_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="33911-412">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="33911-412">Keywords</span></span>

#### <a name="keywordsgreeceeutaxfilenumber"></a><span data-ttu-id="33911-413">Keywords_greece_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="33911-413">Keywords_greece_eu_tax_file_number</span></span>

<span data-ttu-id="33911-414">AFM</span><span class="sxs-lookup"><span data-stu-id="33911-414">afm</span></span>
  
<span data-ttu-id="33911-415">Tin</span><span class="sxs-lookup"><span data-stu-id="33911-415">tin</span></span>
  
<span data-ttu-id="33911-416">n º de ID de imposto</span><span class="sxs-lookup"><span data-stu-id="33911-416">tax id no.</span></span>
  
<span data-ttu-id="33911-417">ID de imposto não</span><span class="sxs-lookup"><span data-stu-id="33911-417">tax id no</span></span>
  
<span data-ttu-id="33911-418">número de identificação do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-418">tax identification number</span></span>
  
<span data-ttu-id="33911-419">número do registro de imposto</span><span class="sxs-lookup"><span data-stu-id="33911-419">tax registry number</span></span>
  
<span data-ttu-id="33911-420">n º do registro de impostos</span><span class="sxs-lookup"><span data-stu-id="33911-420">tax registry no.</span></span>
  
<span data-ttu-id="33911-421">AFM</span><span class="sxs-lookup"><span data-stu-id="33911-421">afm#</span></span>
  
<span data-ttu-id="33911-422">Tin</span><span class="sxs-lookup"><span data-stu-id="33911-422">tin#</span></span>
  
<span data-ttu-id="33911-423">taxidno #</span><span class="sxs-lookup"><span data-stu-id="33911-423">taxidno#</span></span>
  
<span data-ttu-id="33911-424">taxregistryno #</span><span class="sxs-lookup"><span data-stu-id="33911-424">taxregistryno#</span></span>
  
<span data-ttu-id="33911-425">αριθμός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="33911-425">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="33911-426">aφμ</span><span class="sxs-lookup"><span data-stu-id="33911-426">aφμ</span></span>
  
<span data-ttu-id="33911-427">aφμ αριθμός</span><span class="sxs-lookup"><span data-stu-id="33911-427">aφμ αριθμός</span></span>
  
<span data-ttu-id="33911-428">φορολογικού μητρώου νο.</span><span class="sxs-lookup"><span data-stu-id="33911-428">φορολογικού μητρώου νο.</span></span>
  
<span data-ttu-id="33911-429">τον αριθμό φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="33911-429">τον αριθμό φορολογικού μητρώου</span></span>
  
## <a name="hungary"></a><span data-ttu-id="33911-430">Hungria</span><span class="sxs-lookup"><span data-stu-id="33911-430">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="33911-431">Format</span><span class="sxs-lookup"><span data-stu-id="33911-431">Format</span></span>

<span data-ttu-id="33911-432">Dez dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="33911-432">Ten digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="33911-433">Padrão</span><span class="sxs-lookup"><span data-stu-id="33911-433">Pattern</span></span>

<span data-ttu-id="33911-434">Dez dígitos:</span><span class="sxs-lookup"><span data-stu-id="33911-434">Ten digits:</span></span>
  
-  <span data-ttu-id="33911-435">Um dígito que deve ser "8"</span><span class="sxs-lookup"><span data-stu-id="33911-435">One digit that must be "8"</span></span> 
    
- <span data-ttu-id="33911-436">Cinco dígitos que correspondem ao número de dias entre a data 01/01/1867 e a data do nascimento da pessoa</span><span class="sxs-lookup"><span data-stu-id="33911-436">Five digits that correspond to the number of days between the date 01/01/1867 and the date of the birth of the individual</span></span>
    
- <span data-ttu-id="33911-437">Três dígitos que correspondem ao número gerado pela chance de diferenciar as pessoas nasceu no mesmo dia</span><span class="sxs-lookup"><span data-stu-id="33911-437">Three digits that correspond to the number generated by chance to differentiate individuals born on the same day</span></span>
    
- <span data-ttu-id="33911-438">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="33911-438">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="33911-439">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="33911-439">Checksum</span></span>

<span data-ttu-id="33911-440">Sim</span><span class="sxs-lookup"><span data-stu-id="33911-440">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="33911-441">Definição</span><span class="sxs-lookup"><span data-stu-id="33911-441">Definition</span></span>

<span data-ttu-id="33911-442">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-442">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-443">A função `Func_hungary_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-443">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="33911-444">Uma palavra- `Keywords_hungary_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="33911-444">A keyword from  `Keywords_hungary_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="33911-445">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-445">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-446">A função `Func_hungary_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-446">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="33911-447">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="33911-447">Keywords</span></span>

#### <a name="keywordshungaryeutaxfilenumber"></a><span data-ttu-id="33911-448">Keywords_hungary_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="33911-448">Keywords_hungary_eu_tax_file_number</span></span>

<span data-ttu-id="33911-449">número de identificação do imposto húngaro</span><span class="sxs-lookup"><span data-stu-id="33911-449">hungarian tax identification number</span></span>
  
<span data-ttu-id="33911-450">Tin húngaro</span><span class="sxs-lookup"><span data-stu-id="33911-450">hungarian tin</span></span>
  
<span data-ttu-id="33911-451">número de ID do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-451">tax id number</span></span>
  
<span data-ttu-id="33911-452">número de IVA</span><span class="sxs-lookup"><span data-stu-id="33911-452">vat number</span></span>
  
<span data-ttu-id="33911-453">autoridade de imposto não</span><span class="sxs-lookup"><span data-stu-id="33911-453">tax authority no</span></span>
  
<span data-ttu-id="33911-454">número de identidade do imposto ID do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-454">tax id tax identity number</span></span>
  
<span data-ttu-id="33911-455">taxidnumber #</span><span class="sxs-lookup"><span data-stu-id="33911-455">taxidnumber#</span></span>
  
<span data-ttu-id="33911-456">Tin</span><span class="sxs-lookup"><span data-stu-id="33911-456">tin#</span></span>
  
<span data-ttu-id="33911-457">hungatiantin #</span><span class="sxs-lookup"><span data-stu-id="33911-457">hungatiantin#</span></span>
  
<span data-ttu-id="33911-458">identificação de imposto não</span><span class="sxs-lookup"><span data-stu-id="33911-458">tax identification no</span></span>
  
<span data-ttu-id="33911-459">taxidno #</span><span class="sxs-lookup"><span data-stu-id="33911-459">taxidno#</span></span>
  
<span data-ttu-id="33911-460">adóazonosító szám</span><span class="sxs-lookup"><span data-stu-id="33911-460">adóazonosító szám</span></span>
  
<span data-ttu-id="33911-461">adószám</span><span class="sxs-lookup"><span data-stu-id="33911-461">adószám</span></span>
  
<span data-ttu-id="33911-462">adóhatóság szám</span><span class="sxs-lookup"><span data-stu-id="33911-462">adóhatóság szám</span></span>
  
## <a name="ireland"></a><span data-ttu-id="33911-463">Irlanda</span><span class="sxs-lookup"><span data-stu-id="33911-463">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="33911-464">Format</span><span class="sxs-lookup"><span data-stu-id="33911-464">Format</span></span>

<span data-ttu-id="33911-465">Sete dígitos seguidos de uma letra sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="33911-465">Seven digits followed by a letter with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="33911-466">Padrão</span><span class="sxs-lookup"><span data-stu-id="33911-466">Pattern</span></span>

<span data-ttu-id="33911-467">Sete dígitos seguidos de uma letra:</span><span class="sxs-lookup"><span data-stu-id="33911-467">Seven digits followed by a letter:</span></span>
  
-  <span data-ttu-id="33911-468">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="33911-468">Seven digits</span></span> 
    
- <span data-ttu-id="33911-469">Uma letra (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="33911-469">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="33911-470">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="33911-470">Checksum</span></span>

<span data-ttu-id="33911-471">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="33911-471">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="33911-472">Definição</span><span class="sxs-lookup"><span data-stu-id="33911-472">Definition</span></span>

<span data-ttu-id="33911-473">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-473">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-474">A função `Func_ireland_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-474">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="33911-475">Uma palavra- `Keywords_ireland_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="33911-475">A keyword from  `Keywords_ireland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="33911-476">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-476">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-477">A função `Func_ireland_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-477">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="33911-478">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="33911-478">Keywords</span></span>

#### <a name="keywordsirelandeutaxfilenumber"></a><span data-ttu-id="33911-479">Keywords_ireland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="33911-479">Keywords_ireland_eu_tax_file_number</span></span>

<span data-ttu-id="33911-480">serviço público não</span><span class="sxs-lookup"><span data-stu-id="33911-480">public service no</span></span>
  
<span data-ttu-id="33911-481">serviço público pessoal não</span><span class="sxs-lookup"><span data-stu-id="33911-481">personal public service no</span></span>
  
<span data-ttu-id="33911-482">PPS não</span><span class="sxs-lookup"><span data-stu-id="33911-482">pps no</span></span>
  
<span data-ttu-id="33911-483">serviço pessoal não</span><span class="sxs-lookup"><span data-stu-id="33911-483">personal service no</span></span>
  
<span data-ttu-id="33911-484">serviço PPS não</span><span class="sxs-lookup"><span data-stu-id="33911-484">pps service no</span></span>
  
<span data-ttu-id="33911-485">ppsno #</span><span class="sxs-lookup"><span data-stu-id="33911-485">ppsno#</span></span>
  
<span data-ttu-id="33911-486">número do PPS do irlandês</span><span class="sxs-lookup"><span data-stu-id="33911-486">irish pps no</span></span>
  
<span data-ttu-id="33911-487">publicserviceno #</span><span class="sxs-lookup"><span data-stu-id="33911-487">publicserviceno#</span></span>
  
<span data-ttu-id="33911-488">número de serviço público pessoal</span><span class="sxs-lookup"><span data-stu-id="33911-488">personal public service number</span></span>
  
<span data-ttu-id="33911-489">uimhir phearsanta seirbhíse poiblí</span><span class="sxs-lookup"><span data-stu-id="33911-489">uimhir phearsanta seirbhíse poiblí</span></span>
  
<span data-ttu-id="33911-490">PPS uimh</span><span class="sxs-lookup"><span data-stu-id="33911-490">pps uimh</span></span>
  
<span data-ttu-id="33911-491">uimhir aitheantais phearsanta</span><span class="sxs-lookup"><span data-stu-id="33911-491">uimhir aitheantais phearsanta</span></span>
  
## <a name="italy"></a><span data-ttu-id="33911-492">Itália</span><span class="sxs-lookup"><span data-stu-id="33911-492">Italy</span></span>

### <a name="format"></a><span data-ttu-id="33911-493">Format</span><span class="sxs-lookup"><span data-stu-id="33911-493">Format</span></span>

<span data-ttu-id="33911-494">16 letras e dígitos no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="33911-494">16 letters and digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="33911-495">Padrão</span><span class="sxs-lookup"><span data-stu-id="33911-495">Pattern</span></span>

<span data-ttu-id="33911-496">16 letras e dígitos:</span><span class="sxs-lookup"><span data-stu-id="33911-496">16 letters and digits:</span></span>
  
-  <span data-ttu-id="33911-497">Três letras que correspondem às três primeiras consoantes no nome da família</span><span class="sxs-lookup"><span data-stu-id="33911-497">Three letters that correspond to the first three consonants in the family name</span></span> 
    
- <span data-ttu-id="33911-498">Três letras que correspondem à primeira, terceira e quarta consoantes no primeiro nome</span><span class="sxs-lookup"><span data-stu-id="33911-498">Three letters that correspond to the first, third, and fourth consonants in the first name</span></span>
    
- <span data-ttu-id="33911-499">Dois dígitos que correspondem aos últimos dígitos do ano de nascimento</span><span class="sxs-lookup"><span data-stu-id="33911-499">Two digits that correspond to the last digits of the birth year</span></span>
    
- <span data-ttu-id="33911-500">Um dígito que corresponde ao mês de nascimento-as letras são usadas em ordem alfabética, mas apenas as letras de a a E, H, L, M, P, R a T são usadas (portanto, Janeiro é A e outubro é R)</span><span class="sxs-lookup"><span data-stu-id="33911-500">One digit that corresponds to the month of birth—letters are used in alphabetical order, but only the letters A to E, H, L, M, P, R to T are used (thus, January is A and October is R)</span></span>
    
- <span data-ttu-id="33911-501">Dois dígitos que correspondem ao dia do mês de nascimento, onde 40 é adicionado ao dia de nascimento de mulheres para diferenciar da homens</span><span class="sxs-lookup"><span data-stu-id="33911-501">Two digits that correspond to the day of the month of birth where 40 is added to the day of birth for females to differentiate from males</span></span>
    
- <span data-ttu-id="33911-502">Quatro dígitos que correspondem a um código de área específico para o município onde a pessoa nasceu — códigos em todo o país são usados para países estrangeiros</span><span class="sxs-lookup"><span data-stu-id="33911-502">Four digits that correspond to an area code specific to the municipality where the person was born—country-wide codes are used for foreign countries</span></span>
    
- <span data-ttu-id="33911-503">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="33911-503">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="33911-504">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="33911-504">Checksum</span></span>

<span data-ttu-id="33911-505">Sim</span><span class="sxs-lookup"><span data-stu-id="33911-505">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="33911-506">Definição</span><span class="sxs-lookup"><span data-stu-id="33911-506">Definition</span></span>

<span data-ttu-id="33911-507">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-507">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-508">A função `Func_italy_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-508">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="33911-509">Uma palavra- `Keywords_italy_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="33911-509">A keyword from  `Keywords_italy_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="33911-510">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-510">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-511">A função `Func_italy_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-511">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="33911-512">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="33911-512">Keywords</span></span>

#### <a name="keywordsitalyeutaxfilenumber"></a><span data-ttu-id="33911-513">Keywords_italy_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="33911-513">Keywords_italy_eu_tax_file_number</span></span>

<span data-ttu-id="33911-514">número do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-514">tax number</span></span>
  
<span data-ttu-id="33911-515">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-515">tax no.</span></span>
  
<span data-ttu-id="33911-516">taxno #</span><span class="sxs-lookup"><span data-stu-id="33911-516">taxno#</span></span>
  
<span data-ttu-id="33911-517">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="33911-517">taxnumber#</span></span>
  
<span data-ttu-id="33911-518">taxnumber</span><span class="sxs-lookup"><span data-stu-id="33911-518">taxnumber</span></span>
  
<span data-ttu-id="33911-519">tax id</span><span class="sxs-lookup"><span data-stu-id="33911-519">tax id</span></span>
  
<span data-ttu-id="33911-520">táxi #</span><span class="sxs-lookup"><span data-stu-id="33911-520">taxid#</span></span>
  
<span data-ttu-id="33911-521">código fiscal</span><span class="sxs-lookup"><span data-stu-id="33911-521">fiscal code</span></span>
  
<span data-ttu-id="33911-522">fiscalização codice</span><span class="sxs-lookup"><span data-stu-id="33911-522">codice fiscale</span></span>
  
## <a name="latvia"></a><span data-ttu-id="33911-523">Letônia</span><span class="sxs-lookup"><span data-stu-id="33911-523">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="33911-524">Format</span><span class="sxs-lookup"><span data-stu-id="33911-524">Format</span></span>

<span data-ttu-id="33911-525">11 dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="33911-525">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="33911-526">Padrão</span><span class="sxs-lookup"><span data-stu-id="33911-526">Pattern</span></span>

<span data-ttu-id="33911-527">11 dígitos no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="33911-527">11 digits in the specified pattern</span></span>
  
-  <span data-ttu-id="33911-528">Seis dígitos que correspondem à data de nascimento (DDMMAA)</span><span class="sxs-lookup"><span data-stu-id="33911-528">Six digits that correspond to the date of birth (DDMMYY)</span></span> 
    
- <span data-ttu-id="33911-529">Um dígito que corresponde ao século de nascimento onde "0" corresponde ao século 19, "1" corresponde a 20 Century e "2" corresponde ao século 21</span><span class="sxs-lookup"><span data-stu-id="33911-529">One digit that corresponds to the century of birth where "0" corresponds to 19th century, "1" corresponds to 20th century, and "2"corresponds to 21st century</span></span>
    
- <span data-ttu-id="33911-530">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="33911-530">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="33911-531">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="33911-531">Checksum</span></span>

<span data-ttu-id="33911-532">Sim</span><span class="sxs-lookup"><span data-stu-id="33911-532">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="33911-533">Definição</span><span class="sxs-lookup"><span data-stu-id="33911-533">Definition</span></span>

<span data-ttu-id="33911-534">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-534">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-535">A função `Func_latvia_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-535">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="33911-536">Uma palavra- `Keywords_latvia_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="33911-536">A keyword from  `Keywords_latvia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="33911-537">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-537">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-538">A função `Func_latvia_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-538">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="33911-539">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="33911-539">Keywords</span></span>

#### <a name="keywordslatviaeutaxfilenumber"></a><span data-ttu-id="33911-540">Keywords_latvia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="33911-540">Keywords_latvia_eu_tax_file_number</span></span>

<span data-ttu-id="33911-541">número do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-541">tax number</span></span>
  
<span data-ttu-id="33911-542">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-542">tax no.</span></span>
  
<span data-ttu-id="33911-543">taxno #</span><span class="sxs-lookup"><span data-stu-id="33911-543">taxno#</span></span>
  
<span data-ttu-id="33911-544">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="33911-544">taxnumber#</span></span>
  
<span data-ttu-id="33911-545">taxnumber</span><span class="sxs-lookup"><span data-stu-id="33911-545">taxnumber</span></span>
  
<span data-ttu-id="33911-546">tax id</span><span class="sxs-lookup"><span data-stu-id="33911-546">tax id</span></span>
  
<span data-ttu-id="33911-547">táxi #</span><span class="sxs-lookup"><span data-stu-id="33911-547">taxid#</span></span>
  
<span data-ttu-id="33911-548">número de identificação do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-548">tax identification number</span></span>
  
<span data-ttu-id="33911-549">n º de identificação de imposto</span><span class="sxs-lookup"><span data-stu-id="33911-549">tax identification no.</span></span>
  
<span data-ttu-id="33911-550">nodokļa numurs</span><span class="sxs-lookup"><span data-stu-id="33911-550">nodokļa numurs</span></span>
  
<span data-ttu-id="33911-551">nodokļu identifikācijas numurs</span><span class="sxs-lookup"><span data-stu-id="33911-551">nodokļu identifikācijas numurs</span></span>
  
<span data-ttu-id="33911-552">nodokļu identifikācija numurs</span><span class="sxs-lookup"><span data-stu-id="33911-552">nodokļu identifikācija numurs</span></span>
  
## <a name="lithuania"></a><span data-ttu-id="33911-553">Lituânia</span><span class="sxs-lookup"><span data-stu-id="33911-553">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="33911-554">Format</span><span class="sxs-lookup"><span data-stu-id="33911-554">Format</span></span>

<span data-ttu-id="33911-555">11 dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="33911-555">11 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="33911-556">Padrão</span><span class="sxs-lookup"><span data-stu-id="33911-556">Pattern</span></span>

<span data-ttu-id="33911-557">11 dígitos</span><span class="sxs-lookup"><span data-stu-id="33911-557">11 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="33911-558">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="33911-558">Checksum</span></span>

<span data-ttu-id="33911-559">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="33911-559">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="33911-560">Definição</span><span class="sxs-lookup"><span data-stu-id="33911-560">Definition</span></span>

<span data-ttu-id="33911-561">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-561">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-562">A função `Func_lithuania_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-562">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="33911-563">Uma palavra- `Keywords_lithuania_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="33911-563">A keyword from  `Keywords_lithuania_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="33911-564">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-564">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-565">A função `Func_lithuania_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-565">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="33911-566">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="33911-566">Keywords</span></span>

#### <a name="keywordslithuaniaeutaxfilenumber"></a><span data-ttu-id="33911-567">Keywords_lithuania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="33911-567">Keywords_lithuania_eu_tax_file_number</span></span>

<span data-ttu-id="33911-568">número do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-568">tax number</span></span>
  
<span data-ttu-id="33911-569">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-569">tax no.</span></span>
  
<span data-ttu-id="33911-570">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-570">tax no#</span></span>
  
<span data-ttu-id="33911-571">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="33911-571">taxnumber#</span></span>
  
<span data-ttu-id="33911-572">taxnumber</span><span class="sxs-lookup"><span data-stu-id="33911-572">taxnumber</span></span>
  
<span data-ttu-id="33911-573">tax id</span><span class="sxs-lookup"><span data-stu-id="33911-573">tax id</span></span>
  
<span data-ttu-id="33911-574">táxi #</span><span class="sxs-lookup"><span data-stu-id="33911-574">taxid#</span></span>
  
<span data-ttu-id="33911-575">número de identificação do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-575">tax identification number</span></span>
  
<span data-ttu-id="33911-576">n º de identificação de imposto</span><span class="sxs-lookup"><span data-stu-id="33911-576">tax identification no.</span></span>
  
<span data-ttu-id="33911-577">ID mokesčių</span><span class="sxs-lookup"><span data-stu-id="33911-577">mokesčių id</span></span>
  
<span data-ttu-id="33911-578">mokesčių Numeris</span><span class="sxs-lookup"><span data-stu-id="33911-578">mokesčių numeris</span></span>
  
<span data-ttu-id="33911-579">mokesčių identifikavimas Numeris</span><span class="sxs-lookup"><span data-stu-id="33911-579">mokesčių identifikavimas numeris</span></span>
  
## <a name="luxemburg"></a><span data-ttu-id="33911-580">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="33911-580">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="33911-581">Format</span><span class="sxs-lookup"><span data-stu-id="33911-581">Format</span></span>

<span data-ttu-id="33911-582">13 dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="33911-582">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="33911-583">Padrão</span><span class="sxs-lookup"><span data-stu-id="33911-583">Pattern</span></span>

<span data-ttu-id="33911-584">13 dígitos:</span><span class="sxs-lookup"><span data-stu-id="33911-584">13 digits:</span></span>
  
-  <span data-ttu-id="33911-585">11 dígitos</span><span class="sxs-lookup"><span data-stu-id="33911-585">11 digits</span></span> 
    
- <span data-ttu-id="33911-586">Dois dígitos de verificação</span><span class="sxs-lookup"><span data-stu-id="33911-586">Two check digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="33911-587">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="33911-587">Checksum</span></span>

<span data-ttu-id="33911-588">Sim</span><span class="sxs-lookup"><span data-stu-id="33911-588">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="33911-589">Definição</span><span class="sxs-lookup"><span data-stu-id="33911-589">Definition</span></span>

<span data-ttu-id="33911-590">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-590">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-591">A função `Func_luxemburg_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-591">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="33911-592">Uma palavra- `Keywords_luxemburg_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="33911-592">A keyword from  `Keywords_luxemburg_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="33911-593">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-593">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-594">A função `Func_luxemburg_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-594">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="33911-595">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="33911-595">Keywords</span></span>

#### <a name="keywordsluxemburgeutaxfilenumber"></a><span data-ttu-id="33911-596">Keywords_luxemburg_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="33911-596">Keywords_luxemburg_eu_tax_file_number</span></span>

<span data-ttu-id="33911-597">número do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-597">tax number</span></span>
  
<span data-ttu-id="33911-598">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-598">tax no.</span></span>
  
<span data-ttu-id="33911-599">taxno #</span><span class="sxs-lookup"><span data-stu-id="33911-599">taxno#</span></span>
  
<span data-ttu-id="33911-600">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="33911-600">taxnumber#</span></span>
  
<span data-ttu-id="33911-601">taxnumber</span><span class="sxs-lookup"><span data-stu-id="33911-601">taxnumber</span></span>
  
<span data-ttu-id="33911-602">tax id</span><span class="sxs-lookup"><span data-stu-id="33911-602">tax id</span></span>
  
<span data-ttu-id="33911-603">táxi #</span><span class="sxs-lookup"><span data-stu-id="33911-603">taxid#</span></span>
  
<span data-ttu-id="33911-604">número de identificação do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-604">tax identification number</span></span>
  
<span data-ttu-id="33911-605">n º de identificação de imposto</span><span class="sxs-lookup"><span data-stu-id="33911-605">tax identification no.</span></span>
  
<span data-ttu-id="33911-606">steuernummer</span><span class="sxs-lookup"><span data-stu-id="33911-606">steuernummer</span></span>
  
<span data-ttu-id="33911-607">ID Steuer</span><span class="sxs-lookup"><span data-stu-id="33911-607">steuer id</span></span>
  
<span data-ttu-id="33911-608">steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="33911-608">steueridentifikationsnummer</span></span>
  
## <a name="malta"></a><span data-ttu-id="33911-609">Malta</span><span class="sxs-lookup"><span data-stu-id="33911-609">Malta</span></span>

### <a name="format"></a><span data-ttu-id="33911-610">Format</span><span class="sxs-lookup"><span data-stu-id="33911-610">Format</span></span>

<span data-ttu-id="33911-611">Para as nacionalidades maltês: 7 dígitos e uma letra no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="33911-611">For Maltese nationals: 7 digits and one letter in the specified pattern</span></span>
  
<span data-ttu-id="33911-612">Entidades nacionais e Maltês não-maltês: 9 dígitos</span><span class="sxs-lookup"><span data-stu-id="33911-612">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="33911-613">Padrão</span><span class="sxs-lookup"><span data-stu-id="33911-613">Pattern</span></span>

<span data-ttu-id="33911-614">Nacionalidades maltês: 7 dígitos e uma letra</span><span class="sxs-lookup"><span data-stu-id="33911-614">Maltese nationals: 7 digits and one letter</span></span>
  
-  <span data-ttu-id="33911-615">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="33911-615">Seven digits</span></span> 
    
- <span data-ttu-id="33911-616">Uma letra (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="33911-616">One letter (not case-sensitive)</span></span>
    
<span data-ttu-id="33911-617">Entidades nacionais e Maltês não-maltês: 9 dígitos</span><span class="sxs-lookup"><span data-stu-id="33911-617">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
-  <span data-ttu-id="33911-618">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="33911-618">Nine digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="33911-619">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="33911-619">Checksum</span></span>

<span data-ttu-id="33911-620">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="33911-620">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="33911-621">Definição</span><span class="sxs-lookup"><span data-stu-id="33911-621">Definition</span></span>

<span data-ttu-id="33911-622">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-622">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-623">A função `Func_malta_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-623">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="33911-624">Uma palavra- `Keywords_malta_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="33911-624">A keyword from  `Keywords_malta_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="33911-625">Uma política de DLP tem 65% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-625">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-626">A função `Func_malta_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-626">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="33911-627">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="33911-627">Keywords</span></span>

#### <a name="keywordsmaltaeutaxfilenumber"></a><span data-ttu-id="33911-628">Keywords_malta_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="33911-628">Keywords_malta_eu_tax_file_number</span></span>

<span data-ttu-id="33911-629">número do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-629">tax number</span></span>
  
<span data-ttu-id="33911-630">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-630">tax no.</span></span>
  
<span data-ttu-id="33911-631">taxno #</span><span class="sxs-lookup"><span data-stu-id="33911-631">taxno#</span></span>
  
<span data-ttu-id="33911-632">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="33911-632">taxnumber#</span></span>
  
<span data-ttu-id="33911-633">taxnumber</span><span class="sxs-lookup"><span data-stu-id="33911-633">taxnumber</span></span>
  
<span data-ttu-id="33911-634">tax id</span><span class="sxs-lookup"><span data-stu-id="33911-634">tax id</span></span>
  
<span data-ttu-id="33911-635">táxi #</span><span class="sxs-lookup"><span data-stu-id="33911-635">taxid#</span></span>
  
<span data-ttu-id="33911-636">número de identificação do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-636">tax identification number</span></span>
  
<span data-ttu-id="33911-637">n º de identificação de imposto</span><span class="sxs-lookup"><span data-stu-id="33911-637">tax identification no.</span></span>
  
<span data-ttu-id="33911-638">numru tat-taxxa</span><span class="sxs-lookup"><span data-stu-id="33911-638">numru tat-taxxa</span></span>
  
<span data-ttu-id="33911-639">ID tat-taxxa</span><span class="sxs-lookup"><span data-stu-id="33911-639">id tat-taxxa</span></span>
  
<span data-ttu-id="33911-640">numru ta ' identifikazzjoni tat-taxxa</span><span class="sxs-lookup"><span data-stu-id="33911-640">numru ta 'identifikazzjoni tat-taxxa</span></span>
  
## <a name="netherlands"></a><span data-ttu-id="33911-641">Países Baixos</span><span class="sxs-lookup"><span data-stu-id="33911-641">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="33911-642">Format</span><span class="sxs-lookup"><span data-stu-id="33911-642">Format</span></span>

<span data-ttu-id="33911-643">Nove dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="33911-643">Nine digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="33911-644">Padrão</span><span class="sxs-lookup"><span data-stu-id="33911-644">Pattern</span></span>

<span data-ttu-id="33911-645">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="33911-645">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="33911-646">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="33911-646">Checksum</span></span>

<span data-ttu-id="33911-647">Sim</span><span class="sxs-lookup"><span data-stu-id="33911-647">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="33911-648">Definição</span><span class="sxs-lookup"><span data-stu-id="33911-648">Definition</span></span>

<span data-ttu-id="33911-649">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-649">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-650">A função `Func_netherlands_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-650">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="33911-651">Uma palavra- `Keywords_netherlands_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="33911-651">A keyword from  `Keywords_netherlands_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="33911-652">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-652">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-653">A função `Func_netherlands_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-653">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="33911-654">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="33911-654">Keywords</span></span>

#### <a name="keywordsnetherlandseutaxfilenumber"></a><span data-ttu-id="33911-655">Keywords_netherlands_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="33911-655">Keywords_netherlands_eu_tax_file_number</span></span>

<span data-ttu-id="33911-656">número de identificação do imposto Holanda</span><span class="sxs-lookup"><span data-stu-id="33911-656">netherlands tax identification number</span></span>
  
<span data-ttu-id="33911-657">identificação de imposto Holanda</span><span class="sxs-lookup"><span data-stu-id="33911-657">netherlands tax identification</span></span>
  
<span data-ttu-id="33911-658">número de identificação de imposto do Netherland</span><span class="sxs-lookup"><span data-stu-id="33911-658">netherland's tax identification number</span></span>
  
<span data-ttu-id="33911-659">identificação de imposto do Netherland</span><span class="sxs-lookup"><span data-stu-id="33911-659">netherland's tax identification</span></span>
  
<span data-ttu-id="33911-660">número de identificação do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-660">tax identification number</span></span>
  
<span data-ttu-id="33911-661">ID de imposto holandês</span><span class="sxs-lookup"><span data-stu-id="33911-661">dutch tax id</span></span>
  
<span data-ttu-id="33911-662">número de identificação do imposto holandês</span><span class="sxs-lookup"><span data-stu-id="33911-662">dutch tax identification number</span></span>
  
<span data-ttu-id="33911-663">tax id</span><span class="sxs-lookup"><span data-stu-id="33911-663">tax id</span></span>
  
<span data-ttu-id="33911-664">ID de imposto #</span><span class="sxs-lookup"><span data-stu-id="33911-664">tax id#</span></span>
  
<span data-ttu-id="33911-665">número do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-665">tax number</span></span>
  
<span data-ttu-id="33911-666">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-666">tax no#</span></span>
  
<span data-ttu-id="33911-667">imposto</span><span class="sxs-lookup"><span data-stu-id="33911-667">tax#</span></span>
  
<span data-ttu-id="33911-668">Tin</span><span class="sxs-lookup"><span data-stu-id="33911-668">tin</span></span>
  
<span data-ttu-id="33911-669">Tin</span><span class="sxs-lookup"><span data-stu-id="33911-669">tin#</span></span>
  
<span data-ttu-id="33911-670">Tin Holanda</span><span class="sxs-lookup"><span data-stu-id="33911-670">netherlands tin</span></span>
  
<span data-ttu-id="33911-671">Tin do Netherland</span><span class="sxs-lookup"><span data-stu-id="33911-671">netherland's tin</span></span>
  
<span data-ttu-id="33911-672">Países Baixos identificatienummer</span><span class="sxs-lookup"><span data-stu-id="33911-672">nederlands belasting identificatienummer</span></span>
  
<span data-ttu-id="33911-673">identificatienummer Van é última</span><span class="sxs-lookup"><span data-stu-id="33911-673">identificatienummer van belasting</span></span>
  
<span data-ttu-id="33911-674">identificatienummer a última</span><span class="sxs-lookup"><span data-stu-id="33911-674">identificatienummer belasting</span></span>
  
<span data-ttu-id="33911-675">Países Baixos identificatie</span><span class="sxs-lookup"><span data-stu-id="33911-675">nederlands belasting identificatie</span></span>
  
<span data-ttu-id="33911-676">Países Baixos Nummer ID da última vez</span><span class="sxs-lookup"><span data-stu-id="33911-676">nederlands belasting id nummer</span></span>
  
<span data-ttu-id="33911-677">Países Baixos belastingnummer</span><span class="sxs-lookup"><span data-stu-id="33911-677">nederlands belastingnummer</span></span>
  
<span data-ttu-id="33911-678">BTW Nummer</span><span class="sxs-lookup"><span data-stu-id="33911-678">btw nummer</span></span>
  
<span data-ttu-id="33911-679">Nederlandse identificatie</span><span class="sxs-lookup"><span data-stu-id="33911-679">nederlandse belasting identificatie</span></span>
  
## <a name="poland"></a><span data-ttu-id="33911-680">Polônia</span><span class="sxs-lookup"><span data-stu-id="33911-680">Poland</span></span>

### <a name="format"></a><span data-ttu-id="33911-681">Format</span><span class="sxs-lookup"><span data-stu-id="33911-681">Format</span></span>

<span data-ttu-id="33911-682">Onze dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="33911-682">Eleven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="33911-683">Padrão</span><span class="sxs-lookup"><span data-stu-id="33911-683">Pattern</span></span>

<span data-ttu-id="33911-684">Onze dígitos</span><span class="sxs-lookup"><span data-stu-id="33911-684">Eleven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="33911-685">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="33911-685">Checksum</span></span>

<span data-ttu-id="33911-686">Sim</span><span class="sxs-lookup"><span data-stu-id="33911-686">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="33911-687">Definição</span><span class="sxs-lookup"><span data-stu-id="33911-687">Definition</span></span>

<span data-ttu-id="33911-688">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-688">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-689">A função `Func_poland_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-689">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="33911-690">Uma palavra- `Keywords_poland_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="33911-690">A keyword from  `Keywords_poland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="33911-691">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-691">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-692">A função `Func_poland_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-692">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="33911-693">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="33911-693">Keywords</span></span>

#### <a name="keywordspolandeutaxfilenumber"></a><span data-ttu-id="33911-694">Keywords_poland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="33911-694">Keywords_poland_eu_tax_file_number</span></span>

<span data-ttu-id="33911-695">número do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-695">tax number</span></span>
  
<span data-ttu-id="33911-696">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-696">tax no.</span></span>
  
<span data-ttu-id="33911-697">taxno #</span><span class="sxs-lookup"><span data-stu-id="33911-697">taxno#</span></span>
  
<span data-ttu-id="33911-698">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="33911-698">taxnumber#</span></span>
  
<span data-ttu-id="33911-699">taxnumber</span><span class="sxs-lookup"><span data-stu-id="33911-699">taxnumber</span></span>
  
<span data-ttu-id="33911-700">Nip</span><span class="sxs-lookup"><span data-stu-id="33911-700">nip</span></span>
  
<span data-ttu-id="33911-701">Nip #</span><span class="sxs-lookup"><span data-stu-id="33911-701">nip#</span></span>
  
<span data-ttu-id="33911-702">tax id</span><span class="sxs-lookup"><span data-stu-id="33911-702">tax id</span></span>
  
<span data-ttu-id="33911-703">ID de imposto #</span><span class="sxs-lookup"><span data-stu-id="33911-703">tax id#</span></span>
  
<span data-ttu-id="33911-704">ID Nip</span><span class="sxs-lookup"><span data-stu-id="33911-704">nip id</span></span>
  
<span data-ttu-id="33911-705">NIP ID #</span><span class="sxs-lookup"><span data-stu-id="33911-705">nip id#</span></span>
  
<span data-ttu-id="33911-706">número de identificação do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-706">tax identification number</span></span>
  
<span data-ttu-id="33911-707">n º de identificação de imposto</span><span class="sxs-lookup"><span data-stu-id="33911-707">tax identification no.</span></span>
  
<span data-ttu-id="33911-708">número de IVA</span><span class="sxs-lookup"><span data-stu-id="33911-708">vat number</span></span>
  
<span data-ttu-id="33911-709">IVA não.</span><span class="sxs-lookup"><span data-stu-id="33911-709">vat no.</span></span>
  
<span data-ttu-id="33911-710">vatno #</span><span class="sxs-lookup"><span data-stu-id="33911-710">vatno#</span></span>
  
<span data-ttu-id="33911-711">ID de IVA</span><span class="sxs-lookup"><span data-stu-id="33911-711">vat id</span></span>
  
<span data-ttu-id="33911-712">ID de IVA #</span><span class="sxs-lookup"><span data-stu-id="33911-712">vat id#</span></span>
  
<span data-ttu-id="33911-713">numer identyfikacji podatkowej</span><span class="sxs-lookup"><span data-stu-id="33911-713">numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="33911-714">Polski numer identyfikacji podatkowej</span><span class="sxs-lookup"><span data-stu-id="33911-714">polski numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="33911-715">numeridentyfikacjipodatkowej #</span><span class="sxs-lookup"><span data-stu-id="33911-715">numeridentyfikacjipodatkowej#</span></span>
  
## <a name="portugal"></a><span data-ttu-id="33911-716">Portugal</span><span class="sxs-lookup"><span data-stu-id="33911-716">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="33911-717">Format</span><span class="sxs-lookup"><span data-stu-id="33911-717">Format</span></span>

<span data-ttu-id="33911-718">Nove dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="33911-718">Nine digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="33911-719">Padrão</span><span class="sxs-lookup"><span data-stu-id="33911-719">Pattern</span></span>

<span data-ttu-id="33911-720">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="33911-720">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="33911-721">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="33911-721">Checksum</span></span>

<span data-ttu-id="33911-722">Sim</span><span class="sxs-lookup"><span data-stu-id="33911-722">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="33911-723">Definição</span><span class="sxs-lookup"><span data-stu-id="33911-723">Definition</span></span>

<span data-ttu-id="33911-724">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-724">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-725">A função `Func_portugal_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-725">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="33911-726">Uma palavra- `Keywords_portugal_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="33911-726">A keyword from  `Keywords_portugal_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="33911-727">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-727">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-728">A função `Func_portugal_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-728">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="33911-729">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="33911-729">Keywords</span></span>

#### <a name="keywordsportugaleutaxfilenumber"></a><span data-ttu-id="33911-730">Keywords_portugal_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="33911-730">Keywords_portugal_eu_tax_file_number</span></span>

<span data-ttu-id="33911-731">número do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-731">tax number</span></span>
  
<span data-ttu-id="33911-732">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-732">tax no.</span></span>
  
<span data-ttu-id="33911-733">taxno #</span><span class="sxs-lookup"><span data-stu-id="33911-733">taxno#</span></span>
  
<span data-ttu-id="33911-734">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="33911-734">taxnumber#</span></span>
  
<span data-ttu-id="33911-735">taxnumber</span><span class="sxs-lookup"><span data-stu-id="33911-735">taxnumber</span></span>
  
<span data-ttu-id="33911-736">nse</span><span class="sxs-lookup"><span data-stu-id="33911-736">nif</span></span>
  
<span data-ttu-id="33911-737">nse</span><span class="sxs-lookup"><span data-stu-id="33911-737">nif#</span></span>
  
<span data-ttu-id="33911-738">fiscal numero</span><span class="sxs-lookup"><span data-stu-id="33911-738">numero fiscal</span></span>
  
<span data-ttu-id="33911-739">número de identificação fiscal</span><span class="sxs-lookup"><span data-stu-id="33911-739">número de identificação fiscal</span></span>
  
## <a name="romania"></a><span data-ttu-id="33911-740">Romênia</span><span class="sxs-lookup"><span data-stu-id="33911-740">Romania</span></span>

### <a name="format"></a><span data-ttu-id="33911-741">Format</span><span class="sxs-lookup"><span data-stu-id="33911-741">Format</span></span>

<span data-ttu-id="33911-742">13 dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="33911-742">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="33911-743">Padrão</span><span class="sxs-lookup"><span data-stu-id="33911-743">Pattern</span></span>

<span data-ttu-id="33911-744">13 dígitos</span><span class="sxs-lookup"><span data-stu-id="33911-744">13 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="33911-745">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="33911-745">Checksum</span></span>

<span data-ttu-id="33911-746">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="33911-746">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="33911-747">Definição</span><span class="sxs-lookup"><span data-stu-id="33911-747">Definition</span></span>

<span data-ttu-id="33911-748">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-748">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-749">A expressão `Regex_romania_eu_tax_file_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-749">The regular expression  `Regex_romania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="33911-750">Uma palavra- `Keywords_romania_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="33911-750">A keyword from  `Keywords_romania_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_tax_file_number" />
          <Match idRef="Keywords_romania_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="33911-751">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="33911-751">Keywords</span></span>

#### <a name="keywordsromaniaeutaxfilenumber"></a><span data-ttu-id="33911-752">Keywords_romania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="33911-752">Keywords_romania_eu_tax_file_number</span></span>

<span data-ttu-id="33911-753">tax id</span><span class="sxs-lookup"><span data-stu-id="33911-753">tax id</span></span>
  
<span data-ttu-id="33911-754">número de ID do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-754">tax id number</span></span>
  
<span data-ttu-id="33911-755">arquivo de imposto não</span><span class="sxs-lookup"><span data-stu-id="33911-755">tax file no</span></span>
  
<span data-ttu-id="33911-756">tax file number</span><span class="sxs-lookup"><span data-stu-id="33911-756">tax file number</span></span>
  
<span data-ttu-id="33911-757">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-757">tax no</span></span>
  
<span data-ttu-id="33911-758">número do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-758">tax number</span></span>
  
<span data-ttu-id="33911-759">táxi #</span><span class="sxs-lookup"><span data-stu-id="33911-759">taxid#</span></span>
  
<span data-ttu-id="33911-760">taxno #</span><span class="sxs-lookup"><span data-stu-id="33911-760">taxno#</span></span>
  
<span data-ttu-id="33911-761">ID-UL Taxei</span><span class="sxs-lookup"><span data-stu-id="33911-761">id-ul taxei</span></span>
  
<span data-ttu-id="33911-762">numărul de identificare Fiscală</span><span class="sxs-lookup"><span data-stu-id="33911-762">numărul de identificare fiscală</span></span>
  
## <a name="slovakia"></a><span data-ttu-id="33911-763">Eslováquia</span><span class="sxs-lookup"><span data-stu-id="33911-763">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="33911-764">Format</span><span class="sxs-lookup"><span data-stu-id="33911-764">Format</span></span>

<span data-ttu-id="33911-765">10 dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="33911-765">10 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="33911-766">Padrão</span><span class="sxs-lookup"><span data-stu-id="33911-766">Pattern</span></span>

<span data-ttu-id="33911-767">10 dígitos</span><span class="sxs-lookup"><span data-stu-id="33911-767">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="33911-768">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="33911-768">Checksum</span></span>

<span data-ttu-id="33911-769">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="33911-769">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="33911-770">Definição</span><span class="sxs-lookup"><span data-stu-id="33911-770">Definition</span></span>

<span data-ttu-id="33911-771">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-771">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-772">A expressão `Regex_slovakia_eu_tax_file_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-772">The regular expression  `Regex_slovakia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="33911-773">Uma palavra- `Keywords_slovakia_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="33911-773">A keyword from  `Keywords_slovakia_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_tax_file_number" />
          <Match idRef="Keywords_slovakia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="33911-774">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="33911-774">Keywords</span></span>

#### <a name="keywordsslovakiaeutaxfilenumber"></a><span data-ttu-id="33911-775">Keywords_slovakia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="33911-775">Keywords_slovakia_eu_tax_file_number</span></span>

<span data-ttu-id="33911-776">tax id</span><span class="sxs-lookup"><span data-stu-id="33911-776">tax id</span></span>
  
<span data-ttu-id="33911-777">número de ID do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-777">tax id number</span></span>
  
<span data-ttu-id="33911-778">ID do Tin</span><span class="sxs-lookup"><span data-stu-id="33911-778">tin id</span></span>
  
<span data-ttu-id="33911-779">Tin não</span><span class="sxs-lookup"><span data-stu-id="33911-779">tin no</span></span>
  
<span data-ttu-id="33911-780">ID de Tin de eslovaco</span><span class="sxs-lookup"><span data-stu-id="33911-780">slovakian tin id</span></span>
  
<span data-ttu-id="33911-781">Tin</span><span class="sxs-lookup"><span data-stu-id="33911-781">tin</span></span>
  
<span data-ttu-id="33911-782">arquivo de imposto não</span><span class="sxs-lookup"><span data-stu-id="33911-782">tax file no</span></span>
  
<span data-ttu-id="33911-783">tax file number</span><span class="sxs-lookup"><span data-stu-id="33911-783">tax file number</span></span>
  
<span data-ttu-id="33911-784">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-784">tax no</span></span>
  
<span data-ttu-id="33911-785">número do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-785">tax number</span></span>
  
<span data-ttu-id="33911-786">táxi #</span><span class="sxs-lookup"><span data-stu-id="33911-786">taxid#</span></span>
  
<span data-ttu-id="33911-787">taxno #</span><span class="sxs-lookup"><span data-stu-id="33911-787">taxno#</span></span>
  
<span data-ttu-id="33911-788">daňové identifikačné číslo</span><span class="sxs-lookup"><span data-stu-id="33911-788">daňové identifikačné číslo</span></span>
  
<span data-ttu-id="33911-789">daňové číslo</span><span class="sxs-lookup"><span data-stu-id="33911-789">daňové číslo</span></span>
  
<span data-ttu-id="33911-790">daňové číslo súboru</span><span class="sxs-lookup"><span data-stu-id="33911-790">daňové číslo súboru</span></span>
  
## <a name="slovenia"></a><span data-ttu-id="33911-791">Eslovênia</span><span class="sxs-lookup"><span data-stu-id="33911-791">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="33911-792">Format</span><span class="sxs-lookup"><span data-stu-id="33911-792">Format</span></span>

<span data-ttu-id="33911-793">Oito dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="33911-793">Eight digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="33911-794">Padrão</span><span class="sxs-lookup"><span data-stu-id="33911-794">Pattern</span></span>

<span data-ttu-id="33911-795">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="33911-795">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="33911-796">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="33911-796">Checksum</span></span>

<span data-ttu-id="33911-797">Sim</span><span class="sxs-lookup"><span data-stu-id="33911-797">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="33911-798">Definição</span><span class="sxs-lookup"><span data-stu-id="33911-798">Definition</span></span>

<span data-ttu-id="33911-799">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-799">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-800">A função `Func_slovenia_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-800">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="33911-801">Uma palavra- `Keywords_slovenia_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="33911-801">A keyword from  `Keywords_slovenia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="33911-802">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-802">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-803">A função `Func_slovenia_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-803">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="33911-804">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="33911-804">Keywords</span></span>

#### <a name="keywordssloveniaeutaxfilenumber"></a><span data-ttu-id="33911-805">Keywords_slovenia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="33911-805">Keywords_slovenia_eu_tax_file_number</span></span>

<span data-ttu-id="33911-806">tax id</span><span class="sxs-lookup"><span data-stu-id="33911-806">tax id</span></span>
  
<span data-ttu-id="33911-807">número de ID do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-807">tax id number</span></span>
  
<span data-ttu-id="33911-808">ID do Tin</span><span class="sxs-lookup"><span data-stu-id="33911-808">tin id</span></span>
  
<span data-ttu-id="33911-809">Tin não</span><span class="sxs-lookup"><span data-stu-id="33911-809">tin no</span></span>
  
<span data-ttu-id="33911-810">ID de Tin esloveno</span><span class="sxs-lookup"><span data-stu-id="33911-810">slovenian tin id</span></span>
  
<span data-ttu-id="33911-811">Tin</span><span class="sxs-lookup"><span data-stu-id="33911-811">tin</span></span>
  
<span data-ttu-id="33911-812">arquivo de imposto não</span><span class="sxs-lookup"><span data-stu-id="33911-812">tax file no</span></span>
  
<span data-ttu-id="33911-813">tax file number</span><span class="sxs-lookup"><span data-stu-id="33911-813">tax file number</span></span>
  
<span data-ttu-id="33911-814">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-814">tax no</span></span>
  
<span data-ttu-id="33911-815">número do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-815">tax number</span></span>
  
<span data-ttu-id="33911-816">táxi #</span><span class="sxs-lookup"><span data-stu-id="33911-816">taxid#</span></span>
  
<span data-ttu-id="33911-817">taxno #</span><span class="sxs-lookup"><span data-stu-id="33911-817">taxno#</span></span>
  
<span data-ttu-id="33911-818">identifikacijska številka davka</span><span class="sxs-lookup"><span data-stu-id="33911-818">identifikacijska številka davka</span></span>
  
<span data-ttu-id="33911-819">davčna številka</span><span class="sxs-lookup"><span data-stu-id="33911-819">davčna številka</span></span>
  
<span data-ttu-id="33911-820">številka davčne datoteke</span><span class="sxs-lookup"><span data-stu-id="33911-820">številka davčne datoteke</span></span>
  
## <a name="spain"></a><span data-ttu-id="33911-821">Espanha</span><span class="sxs-lookup"><span data-stu-id="33911-821">Spain</span></span>

### <a name="format"></a><span data-ttu-id="33911-822">Format</span><span class="sxs-lookup"><span data-stu-id="33911-822">Format</span></span>

<span data-ttu-id="33911-823">Sete ou oito dígitos e uma ou duas letras no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="33911-823">Seven or eight digits and one or two letters in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="33911-824">Padrão</span><span class="sxs-lookup"><span data-stu-id="33911-824">Pattern</span></span>

<span data-ttu-id="33911-825">Pessoas naturais do espanhol com um cartão de identidade nacional da Espanha:</span><span class="sxs-lookup"><span data-stu-id="33911-825">Spanish Natural Persons with a Spain National Identity Card:</span></span>
  
-  <span data-ttu-id="33911-826">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="33911-826">Eight digits</span></span> 
    
- <span data-ttu-id="33911-827">Uma letra maiúscula (diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="33911-827">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="33911-828">Spaniards não residente sem um cartão de identidade nacional da Espanha</span><span class="sxs-lookup"><span data-stu-id="33911-828">Non-resident Spaniards without a Spain National Identity Card</span></span>
  
- <span data-ttu-id="33911-829">Uma letra maiúscula "L" (diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="33911-829">One uppercase letter "L" (case-sensitive)</span></span>
    
- <span data-ttu-id="33911-830">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="33911-830">Seven digits</span></span>
    
- <span data-ttu-id="33911-831">Uma letra maiúscula (diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="33911-831">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="33911-832">Spaniards residentes sob a idade de 14 anos sem um cartão de identidade nacional da Espanha:</span><span class="sxs-lookup"><span data-stu-id="33911-832">Resident Spaniards under the age of 14 years without a Spain National Identity Card :</span></span>
  
- <span data-ttu-id="33911-833">Uma letra maiúscula "K" (diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="33911-833">One uppercase letter"K" (case-sensitive)</span></span>
    
-  <span data-ttu-id="33911-834">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="33911-834">Seven digits</span></span> 
    
- <span data-ttu-id="33911-835">Uma letra maiúscula (diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="33911-835">One uppercase letter (case-sensitive)</span></span>
    
<span data-ttu-id="33911-836">Foreigners com o número de identificação do estrangeiro</span><span class="sxs-lookup"><span data-stu-id="33911-836">Foreigners with a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="33911-837">Uma letra maiúscula que é "X", "Y" ou "Z" (diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="33911-837">One uppercase letter that is "X", "Y", or "Z" (case-sensitive)</span></span> 
    
- <span data-ttu-id="33911-838">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="33911-838">Seven digits</span></span>
    
- <span data-ttu-id="33911-839">Uma letra maiúscula (diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="33911-839">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="33911-840">Foreigners sem um número de identificação do estrangeiro</span><span class="sxs-lookup"><span data-stu-id="33911-840">Foreigners without a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="33911-841">Uma letra maiúscula que é "M" (diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="33911-841">One uppercase letter that is "M" (case-sensitive)</span></span> 
    
- <span data-ttu-id="33911-842">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="33911-842">Seven digits</span></span>
    
- <span data-ttu-id="33911-843">Uma letra maiúscula (diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="33911-843">One uppercase letter (case-sensitive)</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="33911-844">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="33911-844">Checksum</span></span>

<span data-ttu-id="33911-845">Sim</span><span class="sxs-lookup"><span data-stu-id="33911-845">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="33911-846">Definição</span><span class="sxs-lookup"><span data-stu-id="33911-846">Definition</span></span>

<span data-ttu-id="33911-847">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-847">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-848">A função `Func_spain_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-848">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="33911-849">Uma palavra- `Keywords_spain_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="33911-849">A keyword from  `Keywords_spain_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="33911-850">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-850">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-851">A função `Func_spain_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-851">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="33911-852">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="33911-852">Keywords</span></span>

#### <a name="keywordsspaineutaxfilenumber"></a><span data-ttu-id="33911-853">Keywords_spain_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="33911-853">Keywords_spain_eu_tax_file_number</span></span>

<span data-ttu-id="33911-854">tax id</span><span class="sxs-lookup"><span data-stu-id="33911-854">tax id</span></span>
  
<span data-ttu-id="33911-855">número de ID do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-855">tax id number</span></span>
  
<span data-ttu-id="33911-856">ID de CIF</span><span class="sxs-lookup"><span data-stu-id="33911-856">cif id</span></span>
  
<span data-ttu-id="33911-857">Não CIF</span><span class="sxs-lookup"><span data-stu-id="33911-857">cif no</span></span>
  
<span data-ttu-id="33911-858">ID de CIF espanhol</span><span class="sxs-lookup"><span data-stu-id="33911-858">spanish cif id</span></span>
  
<span data-ttu-id="33911-859">CIF</span><span class="sxs-lookup"><span data-stu-id="33911-859">cif</span></span>
  
<span data-ttu-id="33911-860">arquivo de imposto não</span><span class="sxs-lookup"><span data-stu-id="33911-860">tax file no</span></span>
  
<span data-ttu-id="33911-861">número de CIF espanhol</span><span class="sxs-lookup"><span data-stu-id="33911-861">spanish cif number</span></span>
  
<span data-ttu-id="33911-862">tax file number</span><span class="sxs-lookup"><span data-stu-id="33911-862">tax file number</span></span>
  
<span data-ttu-id="33911-863">Não CIF espanhol</span><span class="sxs-lookup"><span data-stu-id="33911-863">spanish cif no</span></span>
  
<span data-ttu-id="33911-864">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-864">tax no</span></span>
  
<span data-ttu-id="33911-865">número do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-865">tax number</span></span>
  
<span data-ttu-id="33911-866">táxi #</span><span class="sxs-lookup"><span data-stu-id="33911-866">taxid#</span></span>
  
<span data-ttu-id="33911-867">taxno #</span><span class="sxs-lookup"><span data-stu-id="33911-867">taxno#</span></span>
  
<span data-ttu-id="33911-868">cifid #</span><span class="sxs-lookup"><span data-stu-id="33911-868">cifid#</span></span>
  
<span data-ttu-id="33911-869">spanishcifid #</span><span class="sxs-lookup"><span data-stu-id="33911-869">spanishcifid#</span></span>
  
<span data-ttu-id="33911-870">spanishcifno #</span><span class="sxs-lookup"><span data-stu-id="33911-870">spanishcifno#</span></span>
  
<span data-ttu-id="33911-871">número de contribuyente</span><span class="sxs-lookup"><span data-stu-id="33911-871">número de contribuyente</span></span>
  
<span data-ttu-id="33911-872">número de impuesto corporativo</span><span class="sxs-lookup"><span data-stu-id="33911-872">número de impuesto corporativo</span></span>
  
<span data-ttu-id="33911-873">número de Identificación fiscal</span><span class="sxs-lookup"><span data-stu-id="33911-873">número de identificación fiscal</span></span>
  
<span data-ttu-id="33911-874">número CIF</span><span class="sxs-lookup"><span data-stu-id="33911-874">cif número</span></span>
  
<span data-ttu-id="33911-875">cifnúmero #</span><span class="sxs-lookup"><span data-stu-id="33911-875">cifnúmero#</span></span>
  
## <a name="sweden"></a><span data-ttu-id="33911-876">Suécia</span><span class="sxs-lookup"><span data-stu-id="33911-876">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="33911-877">Format</span><span class="sxs-lookup"><span data-stu-id="33911-877">Format</span></span>

<span data-ttu-id="33911-878">Dez dígitos e um símbolo no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="33911-878">Ten digits and a symbol in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="33911-879">Padrão</span><span class="sxs-lookup"><span data-stu-id="33911-879">Pattern</span></span>

<span data-ttu-id="33911-880">Dez dígitos e um símbolo:</span><span class="sxs-lookup"><span data-stu-id="33911-880">Ten digits and a symbol:</span></span>
  
-  <span data-ttu-id="33911-881">Seis dígitos que correspondem à data de nascimento (AAMMDD)</span><span class="sxs-lookup"><span data-stu-id="33911-881">Six digits that correspond to the birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="33911-882">Um sinal de adição, sinal de menos ou barra invertida</span><span class="sxs-lookup"><span data-stu-id="33911-882">A plus sign, minus sign, or backslash</span></span>
    
- <span data-ttu-id="33911-883">Três dígitos que tornam o número de identificação exclusivo, onde:</span><span class="sxs-lookup"><span data-stu-id="33911-883">Three digits that make the identification number unique where:</span></span> 
    
  - <span data-ttu-id="33911-884">Para números emitidos antes de 1990, o sétimo e oitavo dígito identificam o Condado de nascimento ou pessoas de nasceu</span><span class="sxs-lookup"><span data-stu-id="33911-884">For numbers issued before 1990, the seventh and eighth digit identify the county of birth or foreign-born people</span></span>
    
  - <span data-ttu-id="33911-885">O dígito na nona posição indica sexo por tanto ímpar para masculino ou par para fêmea</span><span class="sxs-lookup"><span data-stu-id="33911-885">The digit in the ninth position indicates gender by either odd for male or even for female</span></span>
    
- <span data-ttu-id="33911-886">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="33911-886">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="33911-887">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="33911-887">Checksum</span></span>

<span data-ttu-id="33911-888">Sim</span><span class="sxs-lookup"><span data-stu-id="33911-888">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="33911-889">Definição</span><span class="sxs-lookup"><span data-stu-id="33911-889">Definition</span></span>

<span data-ttu-id="33911-890">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-890">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-891">A função `Func_sweden_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-891">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="33911-892">Uma palavra- `Keywords_sweden_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="33911-892">A keyword from  `Keywords_sweden_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="33911-893">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-893">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-894">A função `Func_sweden_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-894">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="33911-895">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="33911-895">Keywords</span></span>

#### <a name="keywordsswedeneutaxfilenumber"></a><span data-ttu-id="33911-896">Keywords_sweden_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="33911-896">Keywords_sweden_eu_tax_file_number</span></span>

<span data-ttu-id="33911-897">tax id</span><span class="sxs-lookup"><span data-stu-id="33911-897">tax id</span></span>
  
<span data-ttu-id="33911-898">n º de ID de imposto</span><span class="sxs-lookup"><span data-stu-id="33911-898">tax id no.</span></span>
  
<span data-ttu-id="33911-899">número de ID do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-899">tax id number</span></span>
  
<span data-ttu-id="33911-900">tax identification</span><span class="sxs-lookup"><span data-stu-id="33911-900">tax identification</span></span>
  
<span data-ttu-id="33911-901">identificação de imposto #</span><span class="sxs-lookup"><span data-stu-id="33911-901">tax identification#</span></span>
  
<span data-ttu-id="33911-902">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-902">tax no.</span></span>
  
<span data-ttu-id="33911-903">imposto</span><span class="sxs-lookup"><span data-stu-id="33911-903">tax#</span></span>
  
<span data-ttu-id="33911-904">táxi #</span><span class="sxs-lookup"><span data-stu-id="33911-904">taxid#</span></span>
  
<span data-ttu-id="33911-905">arquivo de imposto</span><span class="sxs-lookup"><span data-stu-id="33911-905">tax file</span></span>
  
<span data-ttu-id="33911-906">arquivo de impostos não.</span><span class="sxs-lookup"><span data-stu-id="33911-906">tax file no.</span></span>
  
<span data-ttu-id="33911-907">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="33911-907">personal id number</span></span>
  
<span data-ttu-id="33911-908">skatt ID Nummer</span><span class="sxs-lookup"><span data-stu-id="33911-908">skatt id nummer</span></span>
  
<span data-ttu-id="33911-909">skatt identifikation</span><span class="sxs-lookup"><span data-stu-id="33911-909">skatt identifikation</span></span>
  
<span data-ttu-id="33911-910">personnummer</span><span class="sxs-lookup"><span data-stu-id="33911-910">personnummer</span></span>
  
## <a name="uk"></a><span data-ttu-id="33911-911">Reino Unido</span><span class="sxs-lookup"><span data-stu-id="33911-911">UK</span></span>

### <a name="format"></a><span data-ttu-id="33911-912">Format</span><span class="sxs-lookup"><span data-stu-id="33911-912">Format</span></span>

<span data-ttu-id="33911-913">Referência de contribuidor exclusivo (UTR): 10 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="33911-913">Unique Taxpayer Reference (UTR): 10 digits without spaces and delimiters</span></span>
  
<span data-ttu-id="33911-914">Número de seguro nacional (NINO): para obter detalhes, consulte a seção "Reino Unido</span><span class="sxs-lookup"><span data-stu-id="33911-914">National Insurance Number (NINO): For details, see the section "U.K.</span></span> <span data-ttu-id="33911-915">Número de seguro nacional (NINO) "em [o que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="33911-915">National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="pattern"></a><span data-ttu-id="33911-916">Padrão</span><span class="sxs-lookup"><span data-stu-id="33911-916">Pattern</span></span>

<span data-ttu-id="33911-917">Referência de contribuidor exclusivo (UTR): 10 dígitos</span><span class="sxs-lookup"><span data-stu-id="33911-917">Unique Taxpayer Reference (UTR): 10 digits</span></span>
  
<span data-ttu-id="33911-918">Número de seguro nacional (NINO): para obter detalhes, consulte a seção "Reino Unido</span><span class="sxs-lookup"><span data-stu-id="33911-918">National Insurance Number (NINO): For details, see the section "U.K.</span></span> <span data-ttu-id="33911-919">Número de seguro nacional (NINO) "em [o que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="33911-919">National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="checksum"></a><span data-ttu-id="33911-920">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="33911-920">Checksum</span></span>

<span data-ttu-id="33911-921">Sim</span><span class="sxs-lookup"><span data-stu-id="33911-921">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="33911-922">Definição</span><span class="sxs-lookup"><span data-stu-id="33911-922">Definition</span></span>

<span data-ttu-id="33911-923">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="33911-923">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="33911-924">A função `Func_uk_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="33911-924">The function  `Func_uk_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="33911-925">Uma palavra- `Keywords_uk_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="33911-925">A keyword from  `Keywords_uk_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_uk_eu_tax_file_number" />
          <Match idRef="Keywords_uk_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="33911-926">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="33911-926">Keywords</span></span>

#### <a name="keywordsukeutaxfilenumber"></a><span data-ttu-id="33911-927">Keywords_uk_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="33911-927">Keywords_uk_eu_tax_file_number</span></span>

<span data-ttu-id="33911-928">tax id</span><span class="sxs-lookup"><span data-stu-id="33911-928">tax id</span></span>
  
<span data-ttu-id="33911-929">n º de ID de imposto</span><span class="sxs-lookup"><span data-stu-id="33911-929">tax id no.</span></span>
  
<span data-ttu-id="33911-930">número de ID do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-930">tax id number</span></span>
  
<span data-ttu-id="33911-931">tax identification</span><span class="sxs-lookup"><span data-stu-id="33911-931">tax identification</span></span>
  
<span data-ttu-id="33911-932">identificação de imposto #</span><span class="sxs-lookup"><span data-stu-id="33911-932">tax identification#</span></span>
  
<span data-ttu-id="33911-933">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="33911-933">tax no.</span></span>
  
<span data-ttu-id="33911-934">imposto</span><span class="sxs-lookup"><span data-stu-id="33911-934">tax#</span></span>
  
<span data-ttu-id="33911-935">táxi #</span><span class="sxs-lookup"><span data-stu-id="33911-935">taxid#</span></span>
  
<span data-ttu-id="33911-936">arquivo de imposto</span><span class="sxs-lookup"><span data-stu-id="33911-936">tax file</span></span>
  
<span data-ttu-id="33911-937">arquivo de impostos não.</span><span class="sxs-lookup"><span data-stu-id="33911-937">tax file no.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="33911-938">Confira também</span><span class="sxs-lookup"><span data-stu-id="33911-938">See also</span></span>

[<span data-ttu-id="33911-939">O que os tipos de informações confidenciais procuram</span><span class="sxs-lookup"><span data-stu-id="33911-939">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)


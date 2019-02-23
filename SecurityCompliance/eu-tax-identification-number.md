---
title: Número de identificação do imposto da UE
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: f04919c8-2356-4de2-bb2a-b9f67f339726
description: Este tópico mostra o que uma política de prevenção de perda de dados (DLP) procura quando detecta o tipo de informação confidencial do número de identificação de imposto da UE. Esse tipo de informação confidencial define diferentes padrões, palavras-chave e outras evidências para cada país.
ms.openlocfilehash: f851cce4be70fd41c24a7876d97c452f0a738eda
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30213821"
---
# <a name="eu-tax-identification-number"></a><span data-ttu-id="fe0d7-104">Número de identificação do imposto da UE</span><span class="sxs-lookup"><span data-stu-id="fe0d7-104">EU Tax Identification Number</span></span>

<span data-ttu-id="fe0d7-p102">Este tópico mostra o que uma política de prevenção de perda de dados (DLP) procura quando detecta o tipo de informação confidencial do número de identificação de imposto (TIN) da UE. Esse tipo de informação confidencial define diferentes padrões, palavras-chave e outras evidências para cada país.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Tax Identification Number (TIN) sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="fe0d7-107">Áustria</span><span class="sxs-lookup"><span data-stu-id="fe0d7-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="fe0d7-108">Formato</span><span class="sxs-lookup"><span data-stu-id="fe0d7-108">Format</span></span>

<span data-ttu-id="fe0d7-109">Nove dígitos com hífen opcional e barra para frente</span><span class="sxs-lookup"><span data-stu-id="fe0d7-109">Nine digits with optional hyphen and forward slash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fe0d7-110">Padrão</span><span class="sxs-lookup"><span data-stu-id="fe0d7-110">Pattern</span></span>

<span data-ttu-id="fe0d7-111">Nove dígitos com hífen opcional e barra para frente:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-111">Nine digits with optional hyphen and forward slash:</span></span>
  
-  <span data-ttu-id="fe0d7-112">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="fe0d7-112">Two digits</span></span> 
    
- <span data-ttu-id="fe0d7-113">Um hífen (opcional)</span><span class="sxs-lookup"><span data-stu-id="fe0d7-113">A hyphen (optional)</span></span>
    
- <span data-ttu-id="fe0d7-114">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="fe0d7-114">Three digits</span></span>
    
- <span data-ttu-id="fe0d7-115">Uma barra (opcional)</span><span class="sxs-lookup"><span data-stu-id="fe0d7-115">A forward slash (optional)</span></span>
    
- <span data-ttu-id="fe0d7-116">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="fe0d7-116">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="fe0d7-117">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fe0d7-117">Checksum</span></span>

<span data-ttu-id="fe0d7-118">Sim</span><span class="sxs-lookup"><span data-stu-id="fe0d7-118">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="fe0d7-119">Definição</span><span class="sxs-lookup"><span data-stu-id="fe0d7-119">Definition</span></span>

<span data-ttu-id="fe0d7-120">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-120">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-121">A função `Func_austria_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-121">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fe0d7-122">Uma palavra- `Keywords_austria_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-122">A keyword from  `Keywords_austria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="fe0d7-123">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-123">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-124">A função `Func_austria_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-124">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="fe0d7-125">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fe0d7-125">Keywords</span></span>

#### <a name="keywordsaustriaeutaxfilenumber"></a><span data-ttu-id="fe0d7-126">Keywords_austria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="fe0d7-126">Keywords_austria_eu_tax_file_number</span></span>

<span data-ttu-id="fe0d7-127">número do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-127">tax number</span></span>
  
<span data-ttu-id="fe0d7-128">série</span><span class="sxs-lookup"><span data-stu-id="fe0d7-128">number</span></span>
  
<span data-ttu-id="fe0d7-129">número de registro de imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-129">tax registration number</span></span>
  
<span data-ttu-id="fe0d7-130">tax id
</span><span class="sxs-lookup"><span data-stu-id="fe0d7-130">tax id</span></span>
  
<span data-ttu-id="fe0d7-131">St.Nr.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-131">st.nr.</span></span>
  
<span data-ttu-id="fe0d7-132">steuernummer</span><span class="sxs-lookup"><span data-stu-id="fe0d7-132">steuernummer</span></span>
  
## <a name="belgium"></a><span data-ttu-id="fe0d7-133">Bélgica</span><span class="sxs-lookup"><span data-stu-id="fe0d7-133">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="fe0d7-134">Formato</span><span class="sxs-lookup"><span data-stu-id="fe0d7-134">Format</span></span>

<span data-ttu-id="fe0d7-135">11 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="fe0d7-135">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fe0d7-136">Padrão</span><span class="sxs-lookup"><span data-stu-id="fe0d7-136">Pattern</span></span>

<span data-ttu-id="fe0d7-137">11 dígitos:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-137">11 digits:</span></span>
  
- <span data-ttu-id="fe0d7-138">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="fe0d7-138">Two digits</span></span>
    
- <span data-ttu-id="fe0d7-139">Um "0" ou "1"</span><span class="sxs-lookup"><span data-stu-id="fe0d7-139">A "0" or "1"</span></span>
    
- <span data-ttu-id="fe0d7-140">Um dígito</span><span class="sxs-lookup"><span data-stu-id="fe0d7-140">One digit</span></span>
    
- <span data-ttu-id="fe0d7-141">"0" ou "1" ou "2" ou "3"</span><span class="sxs-lookup"><span data-stu-id="fe0d7-141">A "0" or "1" or "2" or "3"</span></span> 
    
- <span data-ttu-id="fe0d7-142">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="fe0d7-142">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="fe0d7-143">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fe0d7-143">Checksum</span></span>

<span data-ttu-id="fe0d7-144">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="fe0d7-144">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="fe0d7-145">Definição</span><span class="sxs-lookup"><span data-stu-id="fe0d7-145">Definition</span></span>

<span data-ttu-id="fe0d7-146">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-146">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-147">A expressão `Regex_belgium_eu_tax_file_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-147">The regular expression  `Regex_belgium_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fe0d7-148">Uma palavra- `Keywords_belgium_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-148">A keyword from  `Keywords_belgium_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_tax_file_number" />
          <Match idRef="Keywords_belgium_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fe0d7-149">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fe0d7-149">Keywords</span></span>

#### <a name="keywordsbelgiumeutaxfilenumber"></a><span data-ttu-id="fe0d7-150">Keywords_belgium_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="fe0d7-150">Keywords_belgium_eu_tax_file_number</span></span>

<span data-ttu-id="fe0d7-151">número do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-151">tax number</span></span>
  
<span data-ttu-id="fe0d7-152">número de Registro Nacional</span><span class="sxs-lookup"><span data-stu-id="fe0d7-152">national registration number</span></span>
  
<span data-ttu-id="fe0d7-153">número de registro de imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-153">tax registration number</span></span>
  
<span data-ttu-id="fe0d7-154">tax id
</span><span class="sxs-lookup"><span data-stu-id="fe0d7-154">tax id</span></span>
  
<span data-ttu-id="fe0d7-155">nse</span><span class="sxs-lookup"><span data-stu-id="fe0d7-155">nif</span></span>
  
<span data-ttu-id="fe0d7-156">nse</span><span class="sxs-lookup"><span data-stu-id="fe0d7-156">nif#</span></span>
  
<span data-ttu-id="fe0d7-157">Numéro de Registro Nacional</span><span class="sxs-lookup"><span data-stu-id="fe0d7-157">numéro de registre national</span></span>
  
<span data-ttu-id="fe0d7-158">Numéro d'identification fiscal</span><span class="sxs-lookup"><span data-stu-id="fe0d7-158">numéro d'identification fiscale</span></span>
  
## <a name="bulgaria"></a><span data-ttu-id="fe0d7-159">Bulgária</span><span class="sxs-lookup"><span data-stu-id="fe0d7-159">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="fe0d7-160">Formato</span><span class="sxs-lookup"><span data-stu-id="fe0d7-160">Format</span></span>

<span data-ttu-id="fe0d7-161">Dez dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="fe0d7-161">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fe0d7-162">Padrão</span><span class="sxs-lookup"><span data-stu-id="fe0d7-162">Pattern</span></span>

<span data-ttu-id="fe0d7-163">10 dígitos</span><span class="sxs-lookup"><span data-stu-id="fe0d7-163">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="fe0d7-164">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fe0d7-164">Checksum</span></span>

<span data-ttu-id="fe0d7-165">Sim</span><span class="sxs-lookup"><span data-stu-id="fe0d7-165">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="fe0d7-166">Definição</span><span class="sxs-lookup"><span data-stu-id="fe0d7-166">Definition</span></span>

<span data-ttu-id="fe0d7-167">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-167">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-168">A função `Func_bulgaria_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-168">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fe0d7-169">Uma palavra- `Keywords_bulgaria_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-169">A keyword from  `Keywords_bulgaria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="fe0d7-170">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-170">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-171">A função `Func_bulgaria_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-171">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="fe0d7-172">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fe0d7-172">Keywords</span></span>

#### <a name="keywordsbulgariaeutaxfilenumber"></a><span data-ttu-id="fe0d7-173">Keywords_bulgaria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="fe0d7-173">Keywords_bulgaria_eu_tax_file_number</span></span>

<span data-ttu-id="fe0d7-174">bucn</span><span class="sxs-lookup"><span data-stu-id="fe0d7-174">bucn</span></span>
  
<span data-ttu-id="fe0d7-175">número civil uniforme</span><span class="sxs-lookup"><span data-stu-id="fe0d7-175">uniform civil number</span></span>
  
<span data-ttu-id="fe0d7-176">bucn #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-176">bucn#</span></span>
  
<span data-ttu-id="fe0d7-177">uniformcivilnumber #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-177">uniformcivilnumber#</span></span>
  
<span data-ttu-id="fe0d7-178">ID civil uniforme</span><span class="sxs-lookup"><span data-stu-id="fe0d7-178">uniform civil id</span></span>
  
<span data-ttu-id="fe0d7-179">Nenhum civil uniforme</span><span class="sxs-lookup"><span data-stu-id="fe0d7-179">uniform civil no</span></span>
  
<span data-ttu-id="fe0d7-180">Egn</span><span class="sxs-lookup"><span data-stu-id="fe0d7-180">egn</span></span>
  
<span data-ttu-id="fe0d7-181">número civil uniforme búlgaro</span><span class="sxs-lookup"><span data-stu-id="fe0d7-181">bulgarian uniform civil number</span></span>
  
<span data-ttu-id="fe0d7-182">uniformcivilno #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-182">uniformcivilno#</span></span>
  
<span data-ttu-id="fe0d7-183">Egn #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-183">egn#</span></span>
  
<span data-ttu-id="fe0d7-184">униформ граждански номер</span><span class="sxs-lookup"><span data-stu-id="fe0d7-184">униформ граждански номер</span></span>
  
<span data-ttu-id="fe0d7-185">ID униформ</span><span class="sxs-lookup"><span data-stu-id="fe0d7-185">униформ id</span></span>
  
<span data-ttu-id="fe0d7-186">ID de граждански униформ</span><span class="sxs-lookup"><span data-stu-id="fe0d7-186">униформ граждански id</span></span>
  
<span data-ttu-id="fe0d7-187">униформ граждански не</span><span class="sxs-lookup"><span data-stu-id="fe0d7-187">униформ граждански не</span></span>
  
## <a name="croatia"></a><span data-ttu-id="fe0d7-188">Croácia</span><span class="sxs-lookup"><span data-stu-id="fe0d7-188">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="fe0d7-189">Formato</span><span class="sxs-lookup"><span data-stu-id="fe0d7-189">Format</span></span>

<span data-ttu-id="fe0d7-190">11 dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="fe0d7-190">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fe0d7-191">Padrão</span><span class="sxs-lookup"><span data-stu-id="fe0d7-191">Pattern</span></span>

<span data-ttu-id="fe0d7-192">11 dígitos:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-192">11 digits:</span></span>
  
- <span data-ttu-id="fe0d7-193">Dez dígitos, escolhidos aleatoriamente</span><span class="sxs-lookup"><span data-stu-id="fe0d7-193">Ten digits, randomly chosen</span></span>
    
- <span data-ttu-id="fe0d7-194">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="fe0d7-194">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="fe0d7-195">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fe0d7-195">Checksum</span></span>

<span data-ttu-id="fe0d7-196">Sim</span><span class="sxs-lookup"><span data-stu-id="fe0d7-196">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="fe0d7-197">Definição</span><span class="sxs-lookup"><span data-stu-id="fe0d7-197">Definition</span></span>

<span data-ttu-id="fe0d7-198">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-198">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-199">A função `Func_croatia_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-199">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fe0d7-200">Uma palavra- `Keywords_croatia_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-200">A keyword from  `Keywords_croatia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="fe0d7-201">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-201">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-202">A função `Func_croatia_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-202">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="fe0d7-203">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fe0d7-203">Keywords</span></span>

#### <a name="keywordscroatiaeutaxfilenumber"></a><span data-ttu-id="fe0d7-204">Keywords_croatia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="fe0d7-204">Keywords_croatia_eu_tax_file_number</span></span>

<span data-ttu-id="fe0d7-205">número do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-205">tax number</span></span>
  
<span data-ttu-id="fe0d7-206">imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-206">tax</span></span>
  
<span data-ttu-id="fe0d7-207">tax id
</span><span class="sxs-lookup"><span data-stu-id="fe0d7-207">tax id</span></span>
  
<span data-ttu-id="fe0d7-208">OID</span><span class="sxs-lookup"><span data-stu-id="fe0d7-208">oid</span></span>
  
<span data-ttu-id="fe0d7-209">OID</span><span class="sxs-lookup"><span data-stu-id="fe0d7-209">oid#</span></span>
  
<span data-ttu-id="fe0d7-210">porezni broj</span><span class="sxs-lookup"><span data-stu-id="fe0d7-210">porezni broj</span></span>
  
## <a name="cyprus"></a><span data-ttu-id="fe0d7-211">Chipre</span><span class="sxs-lookup"><span data-stu-id="fe0d7-211">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="fe0d7-212">Formato</span><span class="sxs-lookup"><span data-stu-id="fe0d7-212">Format</span></span>

<span data-ttu-id="fe0d7-213">Oito dígitos e uma letra no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="fe0d7-213">Eight digits and one letter in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fe0d7-214">Padrão</span><span class="sxs-lookup"><span data-stu-id="fe0d7-214">Pattern</span></span>

<span data-ttu-id="fe0d7-215">Oito dígitos e uma letra:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-215">Eight digits and one letter:</span></span>
  
-  <span data-ttu-id="fe0d7-216">Um "0"</span><span class="sxs-lookup"><span data-stu-id="fe0d7-216">A "0"</span></span> 
    
- <span data-ttu-id="fe0d7-217">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="fe0d7-217">Seven digits</span></span>
    
- <span data-ttu-id="fe0d7-218">Uma letra (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="fe0d7-218">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="fe0d7-219">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fe0d7-219">Checksum</span></span>

<span data-ttu-id="fe0d7-220">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="fe0d7-220">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="fe0d7-221">Definição</span><span class="sxs-lookup"><span data-stu-id="fe0d7-221">Definition</span></span>

<span data-ttu-id="fe0d7-222">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-222">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-223">A função `Func_cyprus_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-223">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fe0d7-224">Uma palavra- `Keywords_cyprus_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-224">A keyword from  `Keywords_cyprus_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="fe0d7-225">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-225">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-226">A função `Func_cyprus_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-226">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="fe0d7-227">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fe0d7-227">Keywords</span></span>

#### <a name="keywordscypruseutaxfilenumber"></a><span data-ttu-id="fe0d7-228">Keywords_cyprus_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="fe0d7-228">Keywords_cyprus_eu_tax_file_number</span></span>

<span data-ttu-id="fe0d7-229">número do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-229">tax number</span></span>
  
<span data-ttu-id="fe0d7-230">imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-230">tax</span></span>
  
<span data-ttu-id="fe0d7-231">tax id
</span><span class="sxs-lookup"><span data-stu-id="fe0d7-231">tax id</span></span>
  
<span data-ttu-id="fe0d7-232">código de identificação de imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-232">tax identification code</span></span>
  
<span data-ttu-id="fe0d7-233">TIC</span><span class="sxs-lookup"><span data-stu-id="fe0d7-233">tic</span></span>
  
<span data-ttu-id="fe0d7-234">TIC #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-234">tic#</span></span>
  
<span data-ttu-id="fe0d7-235">αριθμός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="fe0d7-235">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="fe0d7-236">φορολογική ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="fe0d7-236">φορολογική ταυτότητα</span></span>
  
<span data-ttu-id="fe0d7-237">κωδικός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="fe0d7-237">κωδικός φορολογικού μητρώου</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="fe0d7-238">República Tcheca</span><span class="sxs-lookup"><span data-stu-id="fe0d7-238">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="fe0d7-239">Formato</span><span class="sxs-lookup"><span data-stu-id="fe0d7-239">Format</span></span>

<span data-ttu-id="fe0d7-240">Nove ou dez dígitos com uma barra invertida opcional</span><span class="sxs-lookup"><span data-stu-id="fe0d7-240">Nine or ten digits with an optional backslash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fe0d7-241">Padrão</span><span class="sxs-lookup"><span data-stu-id="fe0d7-241">Pattern</span></span>

<span data-ttu-id="fe0d7-242">Nove ou dez dígitos com uma barra invertida opcional:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-242">Nine or ten digits with an optional backslashl:</span></span>
  
- <span data-ttu-id="fe0d7-243">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="fe0d7-243">Six digits</span></span> 
    
- <span data-ttu-id="fe0d7-244">Uma barra invertida (opcional)</span><span class="sxs-lookup"><span data-stu-id="fe0d7-244">A backslash (optional)</span></span>
    
- <span data-ttu-id="fe0d7-245">Três ou quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="fe0d7-245">Three or four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="fe0d7-246">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fe0d7-246">Checksum</span></span>

<span data-ttu-id="fe0d7-247">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="fe0d7-247">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="fe0d7-248">Definição</span><span class="sxs-lookup"><span data-stu-id="fe0d7-248">Definition</span></span>

<span data-ttu-id="fe0d7-249">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-249">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-250">A expressão `Regex_czech_republic_eu_tax_file_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-250">The regular expression  `Regex_czech_republic_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fe0d7-251">Uma palavra- `Keywords_czech_republic_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-251">A keyword from  `Keywords_czech_republic_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_tax_file_number" />
          <Match idRef="Keywords_czech_republic_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fe0d7-252">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fe0d7-252">Keywords</span></span>

#### <a name="keywordsczechrepubliceutaxfilenumber"></a><span data-ttu-id="fe0d7-253">Keywords_czech_republic_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="fe0d7-253">Keywords_czech_republic_eu_tax_file_number</span></span>

<span data-ttu-id="fe0d7-254">número do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-254">tax number</span></span>
  
<span data-ttu-id="fe0d7-255">imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-255">tax</span></span>
  
<span data-ttu-id="fe0d7-256">tax id
</span><span class="sxs-lookup"><span data-stu-id="fe0d7-256">tax id</span></span>
  
<span data-ttu-id="fe0d7-257">número pessoal</span><span class="sxs-lookup"><span data-stu-id="fe0d7-257">personal number</span></span>
  
<span data-ttu-id="fe0d7-258">daňové číslo</span><span class="sxs-lookup"><span data-stu-id="fe0d7-258">daňové číslo</span></span>
  
<span data-ttu-id="fe0d7-259">osobní číslo</span><span class="sxs-lookup"><span data-stu-id="fe0d7-259">osobní číslo</span></span>
  
## <a name="denmark"></a><span data-ttu-id="fe0d7-260">Dinamarca</span><span class="sxs-lookup"><span data-stu-id="fe0d7-260">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="fe0d7-261">Formato</span><span class="sxs-lookup"><span data-stu-id="fe0d7-261">Format</span></span>

<span data-ttu-id="fe0d7-262">Dez dígitos contendo um hífen</span><span class="sxs-lookup"><span data-stu-id="fe0d7-262">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fe0d7-263">Padrão</span><span class="sxs-lookup"><span data-stu-id="fe0d7-263">Pattern</span></span>

<span data-ttu-id="fe0d7-264">Dez dígitos contendo um hífen:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-264">Ten digits containing a hyphenl:</span></span>
  
-  <span data-ttu-id="fe0d7-265">Seis dígitos que correspondem à data de nascimento (DDMMAA)</span><span class="sxs-lookup"><span data-stu-id="fe0d7-265">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="fe0d7-266">Um hífen</span><span class="sxs-lookup"><span data-stu-id="fe0d7-266">A hyphen</span></span>
    
- <span data-ttu-id="fe0d7-267">Quatro dígitos que correspondem a um número de sequência onde o primeiro dígito corresponde ao século do nascimento e o último dígito corresponde ao sexo da pessoa (ímpar para macho e par para fêmea)</span><span class="sxs-lookup"><span data-stu-id="fe0d7-267">Four digits that correspond to a sequence number where the first digit corresponds to the century of birth and the last digit corresponds to the individual's gender (odd for male and even for female)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="fe0d7-268">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fe0d7-268">Checksum</span></span>

<span data-ttu-id="fe0d7-269">Sim</span><span class="sxs-lookup"><span data-stu-id="fe0d7-269">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="fe0d7-270">Definição</span><span class="sxs-lookup"><span data-stu-id="fe0d7-270">Definition</span></span>

<span data-ttu-id="fe0d7-271">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-271">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-272">A função `Func_denmark_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-272">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fe0d7-273">Uma palavra- `Keywords_denmark_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-273">A keyword from  `Keywords_denmark_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="fe0d7-274">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-275">A função `Func_denmark_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-275">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="fe0d7-276">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fe0d7-276">Keywords</span></span>

#### <a name="keywordsdenmarkeutaxfilenumber"></a><span data-ttu-id="fe0d7-277">Keywords_denmark_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="fe0d7-277">Keywords_denmark_eu_tax_file_number</span></span>

<span data-ttu-id="fe0d7-278">número do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-278">tax number</span></span>
  
<span data-ttu-id="fe0d7-279">imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-279">tax</span></span>
  
<span data-ttu-id="fe0d7-280">tax id
</span><span class="sxs-lookup"><span data-stu-id="fe0d7-280">tax id</span></span>
  
<span data-ttu-id="fe0d7-281">número de CPR</span><span class="sxs-lookup"><span data-stu-id="fe0d7-281">cpr number</span></span>
  
<span data-ttu-id="fe0d7-282">pedir</span><span class="sxs-lookup"><span data-stu-id="fe0d7-282">cpr#</span></span>
  
<span data-ttu-id="fe0d7-283">Skat Nummer</span><span class="sxs-lookup"><span data-stu-id="fe0d7-283">skat nummer</span></span>
  
<span data-ttu-id="fe0d7-284">ID Skat</span><span class="sxs-lookup"><span data-stu-id="fe0d7-284">skat id</span></span>
  
## <a name="estonia"></a><span data-ttu-id="fe0d7-285">Estônia</span><span class="sxs-lookup"><span data-stu-id="fe0d7-285">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="fe0d7-286">Formato</span><span class="sxs-lookup"><span data-stu-id="fe0d7-286">Format</span></span>

<span data-ttu-id="fe0d7-287">11 dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="fe0d7-287">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fe0d7-288">Padrão</span><span class="sxs-lookup"><span data-stu-id="fe0d7-288">Pattern</span></span>

<span data-ttu-id="fe0d7-289">11 dígitos:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-289">11 digits:</span></span>
  
-  <span data-ttu-id="fe0d7-290">Um dígito que corresponde ao gênero e ao século de nascimento onde um número ímpar indica macho e o número par indica fêmea da seguinte maneira: 1, 2 para o século 19; 3, 4 para o século 20; e 5, 6 para o século 21</span><span class="sxs-lookup"><span data-stu-id="fe0d7-290">One digit that corresponds to gender and century of birth where an odd number indicates male and the even number indicates female as follows: 1, 2 for the 19th century; 3, 4 for the 20th century; and 5, 6 for the 21st century</span></span> 
    
- <span data-ttu-id="fe0d7-291">Seis dígitos que correspondem à data de nascimento (AAMMDD)</span><span class="sxs-lookup"><span data-stu-id="fe0d7-291">Six digits that correspond to birth date (YYMMDD)</span></span>
    
- <span data-ttu-id="fe0d7-292">Três dígitos que correspondem a um número de série separando as pessoas que nasceu na mesma data</span><span class="sxs-lookup"><span data-stu-id="fe0d7-292">Three digits that correspond to a serial number separating persons born on the same date</span></span>
    
- <span data-ttu-id="fe0d7-293">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="fe0d7-293">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="fe0d7-294">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fe0d7-294">Checksum</span></span>

<span data-ttu-id="fe0d7-295">Sim</span><span class="sxs-lookup"><span data-stu-id="fe0d7-295">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="fe0d7-296">Definição</span><span class="sxs-lookup"><span data-stu-id="fe0d7-296">Definition</span></span>

<span data-ttu-id="fe0d7-297">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-297">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-298">A função `Func_estonia_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-298">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fe0d7-299">Uma palavra- `Keywords_estonia_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-299">A keyword from  `Keywords_estonia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="fe0d7-300">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-300">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-301">A função `Func_estonia_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-301">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="fe0d7-302">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fe0d7-302">Keywords</span></span>

#### <a name="keywordsestoniaeutaxfilenumber"></a><span data-ttu-id="fe0d7-303">Keywords_estonia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="fe0d7-303">Keywords_estonia_eu_tax_file_number</span></span>

<span data-ttu-id="fe0d7-304">número do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-304">tax number</span></span>
  
<span data-ttu-id="fe0d7-305">imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-305">tax</span></span>
  
<span data-ttu-id="fe0d7-306">tax id
</span><span class="sxs-lookup"><span data-stu-id="fe0d7-306">tax id</span></span>
  
<span data-ttu-id="fe0d7-307">código pessoal</span><span class="sxs-lookup"><span data-stu-id="fe0d7-307">personal code</span></span>
  
<span data-ttu-id="fe0d7-308">maksunumber</span><span class="sxs-lookup"><span data-stu-id="fe0d7-308">maksunumber</span></span>
  
<span data-ttu-id="fe0d7-309">ID maksu</span><span class="sxs-lookup"><span data-stu-id="fe0d7-309">maksu id</span></span>
  
<span data-ttu-id="fe0d7-310">isikukood</span><span class="sxs-lookup"><span data-stu-id="fe0d7-310">isikukood</span></span>
  
## <a name="finland"></a><span data-ttu-id="fe0d7-311">Finlândia</span><span class="sxs-lookup"><span data-stu-id="fe0d7-311">Finland</span></span>

### <a name="format"></a><span data-ttu-id="fe0d7-312">Formato</span><span class="sxs-lookup"><span data-stu-id="fe0d7-312">Format</span></span>

<span data-ttu-id="fe0d7-313">Uma combinação de 11 caracteres de dígitos, letras e sinal de mais e de menos</span><span class="sxs-lookup"><span data-stu-id="fe0d7-313">An 11-character combination of digits, letters, and plus and minus sign</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fe0d7-314">Padrão</span><span class="sxs-lookup"><span data-stu-id="fe0d7-314">Pattern</span></span>

<span data-ttu-id="fe0d7-315">Uma combinação de 11 caracteres de dígitos, letras e sinal de mais e menos:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-315">An 11-character combination of digits, letters, and plus and minus sign:</span></span>
  
- <span data-ttu-id="fe0d7-316">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="fe0d7-316">Six digits</span></span>
    
- <span data-ttu-id="fe0d7-317">Uma das seguintes opções: um sinal de adição, um sinal de menos ou a letra "A" (não diferencia maiúsculas de minúsculas) onde o sinal de mais significa que nasceu entre 1800-1899, o sinal de menos significa que nasceu entre 1900-1999 e "A" significa que nasceu 2000 e depois</span><span class="sxs-lookup"><span data-stu-id="fe0d7-317">One of the following: a plus sign, a minus sign, or the letter "A" (not case sensitive) where the plus sign means born between 1800-1899, the minus sign means born between 1900-1999, and "A" means born 2000 and after</span></span>
    
- <span data-ttu-id="fe0d7-318">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="fe0d7-318">Three digits</span></span>
    
- <span data-ttu-id="fe0d7-319">Uma letra ou um número</span><span class="sxs-lookup"><span data-stu-id="fe0d7-319">One letter or one number</span></span>
    
### <a name="checksum"></a><span data-ttu-id="fe0d7-320">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fe0d7-320">Checksum</span></span>

<span data-ttu-id="fe0d7-321">Sim</span><span class="sxs-lookup"><span data-stu-id="fe0d7-321">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="fe0d7-322">Definição</span><span class="sxs-lookup"><span data-stu-id="fe0d7-322">Definition</span></span>

<span data-ttu-id="fe0d7-323">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-323">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-324">A função `Func_finland_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-324">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fe0d7-325">Uma palavra- `Keywords_finland_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-325">A keyword from  `Keywords_finland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="fe0d7-326">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-326">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-327">A função `Func_finland_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-327">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="fe0d7-328">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fe0d7-328">Keywords</span></span>

#### <a name="keywordsfinlandeutaxfilenumber"></a><span data-ttu-id="fe0d7-329">Keywords_finland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="fe0d7-329">Keywords_finland_eu_tax_file_number</span></span>

<span data-ttu-id="fe0d7-330">identification number
</span><span class="sxs-lookup"><span data-stu-id="fe0d7-330">identification number</span></span>
  
<span data-ttu-id="fe0d7-331">ID pessoal</span><span class="sxs-lookup"><span data-stu-id="fe0d7-331">personal id</span></span>
  
<span data-ttu-id="fe0d7-332">número de identidade</span><span class="sxs-lookup"><span data-stu-id="fe0d7-332">identity number</span></span>
  
<span data-ttu-id="fe0d7-333">número de ID nacional da finlandês</span><span class="sxs-lookup"><span data-stu-id="fe0d7-333">finnish national id number</span></span>
  
<span data-ttu-id="fe0d7-334">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-334">personalidnumber#</span></span>
  
<span data-ttu-id="fe0d7-335">número de identificação nacional</span><span class="sxs-lookup"><span data-stu-id="fe0d7-335">national identification number</span></span>
  
<span data-ttu-id="fe0d7-336">número de identificação</span><span class="sxs-lookup"><span data-stu-id="fe0d7-336">id number</span></span>
  
<span data-ttu-id="fe0d7-337">n º de ID nacional</span><span class="sxs-lookup"><span data-stu-id="fe0d7-337">national id no.</span></span>
  
<span data-ttu-id="fe0d7-338">número de ID nacional</span><span class="sxs-lookup"><span data-stu-id="fe0d7-338">national id number</span></span>
  
<span data-ttu-id="fe0d7-339">ID não</span><span class="sxs-lookup"><span data-stu-id="fe0d7-339">id no</span></span>
  
<span data-ttu-id="fe0d7-340">tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="fe0d7-340">tunnistenumero</span></span>
  
<span data-ttu-id="fe0d7-341">henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="fe0d7-341">henkilötunnus</span></span>
  
<span data-ttu-id="fe0d7-342">yksilöllinen henkilökohtainen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="fe0d7-342">yksilöllinen henkilökohtainen tunnistenumero</span></span>
  
<span data-ttu-id="fe0d7-343">ainutlaatuinen henkilökohtainen Tunnus</span><span class="sxs-lookup"><span data-stu-id="fe0d7-343">ainutlaatuinen henkilökohtainen tunnus</span></span>
  
<span data-ttu-id="fe0d7-344">identiteetti numero</span><span class="sxs-lookup"><span data-stu-id="fe0d7-344">identiteetti numero</span></span>
  
<span data-ttu-id="fe0d7-345">Suomen Kansallinen henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="fe0d7-345">suomen kansallinen henkilötunnus</span></span>
  
<span data-ttu-id="fe0d7-346">henkilötunnusnumero #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-346">henkilötunnusnumero#</span></span>
  
<span data-ttu-id="fe0d7-347">kansallisen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="fe0d7-347">kansallisen tunnistenumero</span></span>
  
<span data-ttu-id="fe0d7-348">tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="fe0d7-348">tunnusnumero</span></span>
  
<span data-ttu-id="fe0d7-349">Kansallinen Tunnus numero</span><span class="sxs-lookup"><span data-stu-id="fe0d7-349">kansallinen tunnus numero</span></span>
  
## <a name="france"></a><span data-ttu-id="fe0d7-350">França</span><span class="sxs-lookup"><span data-stu-id="fe0d7-350">France</span></span>

### <a name="format"></a><span data-ttu-id="fe0d7-351">Formato</span><span class="sxs-lookup"><span data-stu-id="fe0d7-351">Format</span></span>

<span data-ttu-id="fe0d7-352">13 dígitos para pessoas e nove dígitos para entidades</span><span class="sxs-lookup"><span data-stu-id="fe0d7-352">13 digits for individuals and nine digits for entities</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fe0d7-353">Padrão</span><span class="sxs-lookup"><span data-stu-id="fe0d7-353">Pattern</span></span>

<span data-ttu-id="fe0d7-354">13 dígitos para pessoas:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-354">13 digits for individuals:</span></span>
  
- <span data-ttu-id="fe0d7-355">Um dígito que deve ser 0, 1, 2 ou 3</span><span class="sxs-lookup"><span data-stu-id="fe0d7-355">One digit that must be 0, 1, 2, or 3</span></span>
    
- <span data-ttu-id="fe0d7-356">12 dígitos</span><span class="sxs-lookup"><span data-stu-id="fe0d7-356">12 digits</span></span>
    
<span data-ttu-id="fe0d7-357">Nove dígitos para entidades</span><span class="sxs-lookup"><span data-stu-id="fe0d7-357">Nine digits for entities</span></span>
  
### <a name="checksum"></a><span data-ttu-id="fe0d7-358">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fe0d7-358">Checksum</span></span>

<span data-ttu-id="fe0d7-359">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="fe0d7-359">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="fe0d7-360">Definição</span><span class="sxs-lookup"><span data-stu-id="fe0d7-360">Definition</span></span>

<span data-ttu-id="fe0d7-361">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-361">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-362">A função `Func_france_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-362">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fe0d7-363">Uma palavra- `Keywords_france_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-363">A keyword from  `Keywords_france_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="fe0d7-364">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-365">A função `Func_france_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-365">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="fe0d7-366">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fe0d7-366">Keywords</span></span>

#### <a name="keywordsfranceeutaxfilenumber"></a><span data-ttu-id="fe0d7-367">Keywords_france_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="fe0d7-367">Keywords_france_eu_tax_file_number</span></span>

<span data-ttu-id="fe0d7-368">número de identificação do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-368">tax identification number</span></span>
  
<span data-ttu-id="fe0d7-369">número do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-369">tax number</span></span>
  
<span data-ttu-id="fe0d7-370">tax id
</span><span class="sxs-lookup"><span data-stu-id="fe0d7-370">tax id</span></span>
  
<span data-ttu-id="fe0d7-371">Numéro d'identification fiscal</span><span class="sxs-lookup"><span data-stu-id="fe0d7-371">numéro d'identification fiscale</span></span>
  
## <a name="germany"></a><span data-ttu-id="fe0d7-372">Alemanha</span><span class="sxs-lookup"><span data-stu-id="fe0d7-372">Germany</span></span>

### <a name="format"></a><span data-ttu-id="fe0d7-373">Formato</span><span class="sxs-lookup"><span data-stu-id="fe0d7-373">Format</span></span>

<span data-ttu-id="fe0d7-374">11 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="fe0d7-374">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fe0d7-375">Padrão</span><span class="sxs-lookup"><span data-stu-id="fe0d7-375">Pattern</span></span>

<span data-ttu-id="fe0d7-376">11 dígitos:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-376">11 digits :</span></span>
  
-  <span data-ttu-id="fe0d7-377">Dez dígitos</span><span class="sxs-lookup"><span data-stu-id="fe0d7-377">Ten digits</span></span> 
    
- <span data-ttu-id="fe0d7-378">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="fe0d7-378">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="fe0d7-379">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fe0d7-379">Checksum</span></span>

<span data-ttu-id="fe0d7-380">Sim</span><span class="sxs-lookup"><span data-stu-id="fe0d7-380">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="fe0d7-381">Definição</span><span class="sxs-lookup"><span data-stu-id="fe0d7-381">Definition</span></span>

<span data-ttu-id="fe0d7-382">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-382">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-383">A função `Func_germany_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-383">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fe0d7-384">Uma palavra- `Keywords_germany_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-384">A keyword from  `Keywords_germany_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="fe0d7-385">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-385">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-386">A função `Func_germany_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-386">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="fe0d7-387">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fe0d7-387">Keywords</span></span>

#### <a name="keywordsgermanyeutaxfilenumber"></a><span data-ttu-id="fe0d7-388">Keywords_germany_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="fe0d7-388">Keywords_germany_eu_tax_file_number</span></span>

<span data-ttu-id="fe0d7-389">número do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-389">tax number</span></span>
  
<span data-ttu-id="fe0d7-390">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-390">tax no.</span></span>
  
<span data-ttu-id="fe0d7-391">taxno #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-391">taxno#</span></span>
  
<span data-ttu-id="fe0d7-392">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-392">taxnumber#</span></span>
  
<span data-ttu-id="fe0d7-393">taxnumber</span><span class="sxs-lookup"><span data-stu-id="fe0d7-393">taxnumber</span></span>
  
<span data-ttu-id="fe0d7-394">tax id
</span><span class="sxs-lookup"><span data-stu-id="fe0d7-394">tax id</span></span>
  
<span data-ttu-id="fe0d7-395">táxi #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-395">taxid#</span></span>
  
<span data-ttu-id="fe0d7-396">número de identificação do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-396">tax identification number</span></span>
  
<span data-ttu-id="fe0d7-397">n º de identificação de imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-397">tax identification no.</span></span>
  
<span data-ttu-id="fe0d7-398">steuernummer</span><span class="sxs-lookup"><span data-stu-id="fe0d7-398">steuernummer</span></span>
  
<span data-ttu-id="fe0d7-399">ID Steuer</span><span class="sxs-lookup"><span data-stu-id="fe0d7-399">steuer id</span></span>
  
<span data-ttu-id="fe0d7-400">steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="fe0d7-400">steueridentifikationsnummer</span></span>
  
## <a name="greece"></a><span data-ttu-id="fe0d7-401">Grécia</span><span class="sxs-lookup"><span data-stu-id="fe0d7-401">Greece</span></span>

### <a name="format"></a><span data-ttu-id="fe0d7-402">Formato</span><span class="sxs-lookup"><span data-stu-id="fe0d7-402">Format</span></span>

<span data-ttu-id="fe0d7-403">Nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="fe0d7-403">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fe0d7-404">Padrão</span><span class="sxs-lookup"><span data-stu-id="fe0d7-404">Pattern</span></span>

<span data-ttu-id="fe0d7-405">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="fe0d7-405">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="fe0d7-406">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fe0d7-406">Checksum</span></span>

<span data-ttu-id="fe0d7-407">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="fe0d7-407">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="fe0d7-408">Definição</span><span class="sxs-lookup"><span data-stu-id="fe0d7-408">Definition</span></span>

<span data-ttu-id="fe0d7-409">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-409">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-410">A expressão `Regex_greece_eu_tax_file_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-410">The regular expression  `Regex_greece_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fe0d7-411">Uma palavra- `Keywords_greece_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-411">A keyword from  `Keywords_greece_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_tax_file_number" />
          <Match idRef="Keywords_greece_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fe0d7-412">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fe0d7-412">Keywords</span></span>

#### <a name="keywordsgreeceeutaxfilenumber"></a><span data-ttu-id="fe0d7-413">Keywords_greece_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="fe0d7-413">Keywords_greece_eu_tax_file_number</span></span>

<span data-ttu-id="fe0d7-414">AFM</span><span class="sxs-lookup"><span data-stu-id="fe0d7-414">afm</span></span>
  
<span data-ttu-id="fe0d7-415">tin
</span><span class="sxs-lookup"><span data-stu-id="fe0d7-415">tin</span></span>
  
<span data-ttu-id="fe0d7-416">n º de ID de imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-416">tax id no.</span></span>
  
<span data-ttu-id="fe0d7-417">ID de imposto não</span><span class="sxs-lookup"><span data-stu-id="fe0d7-417">tax id no</span></span>
  
<span data-ttu-id="fe0d7-418">número de identificação do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-418">tax identification number</span></span>
  
<span data-ttu-id="fe0d7-419">número do registro de imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-419">tax registry number</span></span>
  
<span data-ttu-id="fe0d7-420">n º do registro de impostos</span><span class="sxs-lookup"><span data-stu-id="fe0d7-420">tax registry no.</span></span>
  
<span data-ttu-id="fe0d7-421">AFM</span><span class="sxs-lookup"><span data-stu-id="fe0d7-421">afm#</span></span>
  
<span data-ttu-id="fe0d7-422">Tin</span><span class="sxs-lookup"><span data-stu-id="fe0d7-422">tin#</span></span>
  
<span data-ttu-id="fe0d7-423">taxidno #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-423">taxidno#</span></span>
  
<span data-ttu-id="fe0d7-424">taxregistryno #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-424">taxregistryno#</span></span>
  
<span data-ttu-id="fe0d7-425">αριθμός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="fe0d7-425">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="fe0d7-426">aφμ</span><span class="sxs-lookup"><span data-stu-id="fe0d7-426">aφμ</span></span>
  
<span data-ttu-id="fe0d7-427">aφμ αριθμός</span><span class="sxs-lookup"><span data-stu-id="fe0d7-427">aφμ αριθμός</span></span>
  
<span data-ttu-id="fe0d7-428">φορολογικού μητρώου νο.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-428">φορολογικού μητρώου νο.</span></span>
  
<span data-ttu-id="fe0d7-429">τον αριθμό φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="fe0d7-429">τον αριθμό φορολογικού μητρώου</span></span>
  
## <a name="hungary"></a><span data-ttu-id="fe0d7-430">Hungria</span><span class="sxs-lookup"><span data-stu-id="fe0d7-430">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="fe0d7-431">Formato</span><span class="sxs-lookup"><span data-stu-id="fe0d7-431">Format</span></span>

<span data-ttu-id="fe0d7-432">Dez dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="fe0d7-432">Ten digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fe0d7-433">Padrão</span><span class="sxs-lookup"><span data-stu-id="fe0d7-433">Pattern</span></span>

<span data-ttu-id="fe0d7-434">Dez dígitos:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-434">Ten digits:</span></span>
  
-  <span data-ttu-id="fe0d7-435">Um dígito que deve ser "8"</span><span class="sxs-lookup"><span data-stu-id="fe0d7-435">One digit that must be "8"</span></span> 
    
- <span data-ttu-id="fe0d7-436">Cinco dígitos que correspondem ao número de dias entre a data 01/01/1867 e a data do nascimento da pessoa</span><span class="sxs-lookup"><span data-stu-id="fe0d7-436">Five digits that correspond to the number of days between the date 01/01/1867 and the date of the birth of the individual</span></span>
    
- <span data-ttu-id="fe0d7-437">Três dígitos que correspondem ao número gerado pela chance de diferenciar as pessoas nasceu no mesmo dia</span><span class="sxs-lookup"><span data-stu-id="fe0d7-437">Three digits that correspond to the number generated by chance to differentiate individuals born on the same day</span></span>
    
- <span data-ttu-id="fe0d7-438">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="fe0d7-438">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="fe0d7-439">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fe0d7-439">Checksum</span></span>

<span data-ttu-id="fe0d7-440">Sim</span><span class="sxs-lookup"><span data-stu-id="fe0d7-440">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="fe0d7-441">Definição</span><span class="sxs-lookup"><span data-stu-id="fe0d7-441">Definition</span></span>

<span data-ttu-id="fe0d7-442">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-442">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-443">A função `Func_hungary_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-443">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fe0d7-444">Uma palavra- `Keywords_hungary_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-444">A keyword from  `Keywords_hungary_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="fe0d7-445">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-445">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-446">A função `Func_hungary_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-446">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="fe0d7-447">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fe0d7-447">Keywords</span></span>

#### <a name="keywordshungaryeutaxfilenumber"></a><span data-ttu-id="fe0d7-448">Keywords_hungary_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="fe0d7-448">Keywords_hungary_eu_tax_file_number</span></span>

<span data-ttu-id="fe0d7-449">número de identificação do imposto húngaro</span><span class="sxs-lookup"><span data-stu-id="fe0d7-449">hungarian tax identification number</span></span>
  
<span data-ttu-id="fe0d7-450">Tin húngaro</span><span class="sxs-lookup"><span data-stu-id="fe0d7-450">hungarian tin</span></span>
  
<span data-ttu-id="fe0d7-451">número de ID do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-451">tax id number</span></span>
  
<span data-ttu-id="fe0d7-452">número de IVA</span><span class="sxs-lookup"><span data-stu-id="fe0d7-452">vat number</span></span>
  
<span data-ttu-id="fe0d7-453">autoridade de imposto não</span><span class="sxs-lookup"><span data-stu-id="fe0d7-453">tax authority no</span></span>
  
<span data-ttu-id="fe0d7-454">número de identidade do imposto ID do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-454">tax id tax identity number</span></span>
  
<span data-ttu-id="fe0d7-455">taxidnumber #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-455">taxidnumber#</span></span>
  
<span data-ttu-id="fe0d7-456">Tin</span><span class="sxs-lookup"><span data-stu-id="fe0d7-456">tin#</span></span>
  
<span data-ttu-id="fe0d7-457">hungatiantin #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-457">hungatiantin#</span></span>
  
<span data-ttu-id="fe0d7-458">identificação de imposto não</span><span class="sxs-lookup"><span data-stu-id="fe0d7-458">tax identification no</span></span>
  
<span data-ttu-id="fe0d7-459">taxidno #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-459">taxidno#</span></span>
  
<span data-ttu-id="fe0d7-460">adóazonosító szám</span><span class="sxs-lookup"><span data-stu-id="fe0d7-460">adóazonosító szám</span></span>
  
<span data-ttu-id="fe0d7-461">adószám</span><span class="sxs-lookup"><span data-stu-id="fe0d7-461">adószám</span></span>
  
<span data-ttu-id="fe0d7-462">adóhatóság szám</span><span class="sxs-lookup"><span data-stu-id="fe0d7-462">adóhatóság szám</span></span>
  
## <a name="ireland"></a><span data-ttu-id="fe0d7-463">Irlanda</span><span class="sxs-lookup"><span data-stu-id="fe0d7-463">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="fe0d7-464">Formato</span><span class="sxs-lookup"><span data-stu-id="fe0d7-464">Format</span></span>

<span data-ttu-id="fe0d7-465">Sete dígitos seguidos de uma letra sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="fe0d7-465">Seven digits followed by a letter with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fe0d7-466">Padrão</span><span class="sxs-lookup"><span data-stu-id="fe0d7-466">Pattern</span></span>

<span data-ttu-id="fe0d7-467">Sete dígitos seguidos de uma letra:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-467">Seven digits followed by a letter:</span></span>
  
-  <span data-ttu-id="fe0d7-468">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="fe0d7-468">Seven digits</span></span> 
    
- <span data-ttu-id="fe0d7-469">Uma letra (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="fe0d7-469">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="fe0d7-470">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fe0d7-470">Checksum</span></span>

<span data-ttu-id="fe0d7-471">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="fe0d7-471">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="fe0d7-472">Definição</span><span class="sxs-lookup"><span data-stu-id="fe0d7-472">Definition</span></span>

<span data-ttu-id="fe0d7-473">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-473">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-474">A função `Func_ireland_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-474">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fe0d7-475">Uma palavra- `Keywords_ireland_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-475">A keyword from  `Keywords_ireland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="fe0d7-476">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-476">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-477">A função `Func_ireland_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-477">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="fe0d7-478">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fe0d7-478">Keywords</span></span>

#### <a name="keywordsirelandeutaxfilenumber"></a><span data-ttu-id="fe0d7-479">Keywords_ireland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="fe0d7-479">Keywords_ireland_eu_tax_file_number</span></span>

<span data-ttu-id="fe0d7-480">serviço público não</span><span class="sxs-lookup"><span data-stu-id="fe0d7-480">public service no</span></span>
  
<span data-ttu-id="fe0d7-481">serviço público pessoal não</span><span class="sxs-lookup"><span data-stu-id="fe0d7-481">personal public service no</span></span>
  
<span data-ttu-id="fe0d7-482">PPS não</span><span class="sxs-lookup"><span data-stu-id="fe0d7-482">pps no</span></span>
  
<span data-ttu-id="fe0d7-483">serviço pessoal não</span><span class="sxs-lookup"><span data-stu-id="fe0d7-483">personal service no</span></span>
  
<span data-ttu-id="fe0d7-484">serviço PPS não</span><span class="sxs-lookup"><span data-stu-id="fe0d7-484">pps service no</span></span>
  
<span data-ttu-id="fe0d7-485">ppsno #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-485">ppsno#</span></span>
  
<span data-ttu-id="fe0d7-486">número do PPS do irlandês</span><span class="sxs-lookup"><span data-stu-id="fe0d7-486">irish pps no</span></span>
  
<span data-ttu-id="fe0d7-487">publicserviceno #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-487">publicserviceno#</span></span>
  
<span data-ttu-id="fe0d7-488">número de serviço público pessoal</span><span class="sxs-lookup"><span data-stu-id="fe0d7-488">personal public service number</span></span>
  
<span data-ttu-id="fe0d7-489">uimhir phearsanta seirbhíse poiblí</span><span class="sxs-lookup"><span data-stu-id="fe0d7-489">uimhir phearsanta seirbhíse poiblí</span></span>
  
<span data-ttu-id="fe0d7-490">PPS uimh</span><span class="sxs-lookup"><span data-stu-id="fe0d7-490">pps uimh</span></span>
  
<span data-ttu-id="fe0d7-491">uimhir aitheantais phearsanta</span><span class="sxs-lookup"><span data-stu-id="fe0d7-491">uimhir aitheantais phearsanta</span></span>
  
## <a name="italy"></a><span data-ttu-id="fe0d7-492">Itália</span><span class="sxs-lookup"><span data-stu-id="fe0d7-492">Italy</span></span>

### <a name="format"></a><span data-ttu-id="fe0d7-493">Formato</span><span class="sxs-lookup"><span data-stu-id="fe0d7-493">Format</span></span>

<span data-ttu-id="fe0d7-494">16 letras e dígitos no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="fe0d7-494">16 letters and digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fe0d7-495">Padrão</span><span class="sxs-lookup"><span data-stu-id="fe0d7-495">Pattern</span></span>

<span data-ttu-id="fe0d7-496">16 letras e dígitos:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-496">16 letters and digits:</span></span>
  
-  <span data-ttu-id="fe0d7-497">Três letras que correspondem às três primeiras consoantes no nome da família</span><span class="sxs-lookup"><span data-stu-id="fe0d7-497">Three letters that correspond to the first three consonants in the family name</span></span> 
    
- <span data-ttu-id="fe0d7-498">Três letras que correspondem à primeira, terceira e quarta consoantes no primeiro nome</span><span class="sxs-lookup"><span data-stu-id="fe0d7-498">Three letters that correspond to the first, third, and fourth consonants in the first name</span></span>
    
- <span data-ttu-id="fe0d7-499">Dois dígitos que correspondem aos últimos dígitos do ano de nascimento</span><span class="sxs-lookup"><span data-stu-id="fe0d7-499">Two digits that correspond to the last digits of the birth year</span></span>
    
- <span data-ttu-id="fe0d7-500">Um dígito que corresponde ao mês de nascimento-as letras são usadas em ordem alfabética, mas apenas as letras de a a E, H, L, M, P, R a T são usadas (portanto, Janeiro é A e outubro é R)</span><span class="sxs-lookup"><span data-stu-id="fe0d7-500">One digit that corresponds to the month of birth—letters are used in alphabetical order, but only the letters A to E, H, L, M, P, R to T are used (thus, January is A and October is R)</span></span>
    
- <span data-ttu-id="fe0d7-501">Dois dígitos que correspondem ao dia do mês de nascimento, onde 40 é adicionado ao dia de nascimento de mulheres para diferenciar da homens</span><span class="sxs-lookup"><span data-stu-id="fe0d7-501">Two digits that correspond to the day of the month of birth where 40 is added to the day of birth for females to differentiate from males</span></span>
    
- <span data-ttu-id="fe0d7-502">Quatro dígitos que correspondem a um código de área específico para o município onde a pessoa nasceu — códigos em todo o país são usados para países estrangeiros</span><span class="sxs-lookup"><span data-stu-id="fe0d7-502">Four digits that correspond to an area code specific to the municipality where the person was born—country-wide codes are used for foreign countries</span></span>
    
- <span data-ttu-id="fe0d7-503">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="fe0d7-503">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="fe0d7-504">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fe0d7-504">Checksum</span></span>

<span data-ttu-id="fe0d7-505">Sim</span><span class="sxs-lookup"><span data-stu-id="fe0d7-505">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="fe0d7-506">Definição</span><span class="sxs-lookup"><span data-stu-id="fe0d7-506">Definition</span></span>

<span data-ttu-id="fe0d7-507">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-507">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-508">A função `Func_italy_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-508">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fe0d7-509">Uma palavra- `Keywords_italy_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-509">A keyword from  `Keywords_italy_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="fe0d7-510">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-510">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-511">A função `Func_italy_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-511">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="fe0d7-512">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fe0d7-512">Keywords</span></span>

#### <a name="keywordsitalyeutaxfilenumber"></a><span data-ttu-id="fe0d7-513">Keywords_italy_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="fe0d7-513">Keywords_italy_eu_tax_file_number</span></span>

<span data-ttu-id="fe0d7-514">número do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-514">tax number</span></span>
  
<span data-ttu-id="fe0d7-515">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-515">tax no.</span></span>
  
<span data-ttu-id="fe0d7-516">taxno #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-516">taxno#</span></span>
  
<span data-ttu-id="fe0d7-517">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-517">taxnumber#</span></span>
  
<span data-ttu-id="fe0d7-518">taxnumber</span><span class="sxs-lookup"><span data-stu-id="fe0d7-518">taxnumber</span></span>
  
<span data-ttu-id="fe0d7-519">tax id
</span><span class="sxs-lookup"><span data-stu-id="fe0d7-519">tax id</span></span>
  
<span data-ttu-id="fe0d7-520">táxi #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-520">taxid#</span></span>
  
<span data-ttu-id="fe0d7-521">código fiscal</span><span class="sxs-lookup"><span data-stu-id="fe0d7-521">fiscal code</span></span>
  
<span data-ttu-id="fe0d7-522">fiscalização codice</span><span class="sxs-lookup"><span data-stu-id="fe0d7-522">codice fiscale</span></span>
  
## <a name="latvia"></a><span data-ttu-id="fe0d7-523">Letônia</span><span class="sxs-lookup"><span data-stu-id="fe0d7-523">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="fe0d7-524">Formato</span><span class="sxs-lookup"><span data-stu-id="fe0d7-524">Format</span></span>

<span data-ttu-id="fe0d7-525">11 dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="fe0d7-525">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fe0d7-526">Padrão</span><span class="sxs-lookup"><span data-stu-id="fe0d7-526">Pattern</span></span>

<span data-ttu-id="fe0d7-527">11 dígitos no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="fe0d7-527">11 digits in the specified pattern</span></span>
  
-  <span data-ttu-id="fe0d7-528">Seis dígitos que correspondem à data de nascimento (DDMMAA)</span><span class="sxs-lookup"><span data-stu-id="fe0d7-528">Six digits that correspond to the date of birth (DDMMYY)</span></span> 
    
- <span data-ttu-id="fe0d7-529">Um dígito que corresponde ao século de nascimento onde "0" corresponde ao século 19, "1" corresponde a 20 Century e "2" corresponde ao século 21</span><span class="sxs-lookup"><span data-stu-id="fe0d7-529">One digit that corresponds to the century of birth where "0" corresponds to 19th century, "1" corresponds to 20th century, and "2"corresponds to 21st century</span></span>
    
- <span data-ttu-id="fe0d7-530">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="fe0d7-530">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="fe0d7-531">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fe0d7-531">Checksum</span></span>

<span data-ttu-id="fe0d7-532">Sim</span><span class="sxs-lookup"><span data-stu-id="fe0d7-532">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="fe0d7-533">Definição</span><span class="sxs-lookup"><span data-stu-id="fe0d7-533">Definition</span></span>

<span data-ttu-id="fe0d7-534">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-534">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-535">A função `Func_latvia_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-535">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fe0d7-536">Uma palavra- `Keywords_latvia_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-536">A keyword from  `Keywords_latvia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="fe0d7-537">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-537">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-538">A função `Func_latvia_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-538">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="fe0d7-539">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fe0d7-539">Keywords</span></span>

#### <a name="keywordslatviaeutaxfilenumber"></a><span data-ttu-id="fe0d7-540">Keywords_latvia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="fe0d7-540">Keywords_latvia_eu_tax_file_number</span></span>

<span data-ttu-id="fe0d7-541">número do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-541">tax number</span></span>
  
<span data-ttu-id="fe0d7-542">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-542">tax no.</span></span>
  
<span data-ttu-id="fe0d7-543">taxno #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-543">taxno#</span></span>
  
<span data-ttu-id="fe0d7-544">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-544">taxnumber#</span></span>
  
<span data-ttu-id="fe0d7-545">taxnumber</span><span class="sxs-lookup"><span data-stu-id="fe0d7-545">taxnumber</span></span>
  
<span data-ttu-id="fe0d7-546">tax id
</span><span class="sxs-lookup"><span data-stu-id="fe0d7-546">tax id</span></span>
  
<span data-ttu-id="fe0d7-547">táxi #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-547">taxid#</span></span>
  
<span data-ttu-id="fe0d7-548">número de identificação do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-548">tax identification number</span></span>
  
<span data-ttu-id="fe0d7-549">n º de identificação de imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-549">tax identification no.</span></span>
  
<span data-ttu-id="fe0d7-550">nodokļa numurs</span><span class="sxs-lookup"><span data-stu-id="fe0d7-550">nodokļa numurs</span></span>
  
<span data-ttu-id="fe0d7-551">nodokļu identifikācijas numurs</span><span class="sxs-lookup"><span data-stu-id="fe0d7-551">nodokļu identifikācijas numurs</span></span>
  
<span data-ttu-id="fe0d7-552">nodokļu identifikācija numurs</span><span class="sxs-lookup"><span data-stu-id="fe0d7-552">nodokļu identifikācija numurs</span></span>
  
## <a name="lithuania"></a><span data-ttu-id="fe0d7-553">Lituânia</span><span class="sxs-lookup"><span data-stu-id="fe0d7-553">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="fe0d7-554">Formato</span><span class="sxs-lookup"><span data-stu-id="fe0d7-554">Format</span></span>

<span data-ttu-id="fe0d7-555">11 dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="fe0d7-555">11 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fe0d7-556">Padrão</span><span class="sxs-lookup"><span data-stu-id="fe0d7-556">Pattern</span></span>

<span data-ttu-id="fe0d7-557">11 dígitos</span><span class="sxs-lookup"><span data-stu-id="fe0d7-557">11 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="fe0d7-558">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fe0d7-558">Checksum</span></span>

<span data-ttu-id="fe0d7-559">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="fe0d7-559">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="fe0d7-560">Definição</span><span class="sxs-lookup"><span data-stu-id="fe0d7-560">Definition</span></span>

<span data-ttu-id="fe0d7-561">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-561">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-562">A função `Func_lithuania_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-562">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fe0d7-563">Uma palavra- `Keywords_lithuania_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-563">A keyword from  `Keywords_lithuania_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="fe0d7-564">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-564">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-565">A função `Func_lithuania_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-565">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="fe0d7-566">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fe0d7-566">Keywords</span></span>

#### <a name="keywordslithuaniaeutaxfilenumber"></a><span data-ttu-id="fe0d7-567">Keywords_lithuania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="fe0d7-567">Keywords_lithuania_eu_tax_file_number</span></span>

<span data-ttu-id="fe0d7-568">número do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-568">tax number</span></span>
  
<span data-ttu-id="fe0d7-569">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-569">tax no.</span></span>
  
<span data-ttu-id="fe0d7-570">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-570">tax no#</span></span>
  
<span data-ttu-id="fe0d7-571">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-571">taxnumber#</span></span>
  
<span data-ttu-id="fe0d7-572">taxnumber</span><span class="sxs-lookup"><span data-stu-id="fe0d7-572">taxnumber</span></span>
  
<span data-ttu-id="fe0d7-573">tax id
</span><span class="sxs-lookup"><span data-stu-id="fe0d7-573">tax id</span></span>
  
<span data-ttu-id="fe0d7-574">táxi #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-574">taxid#</span></span>
  
<span data-ttu-id="fe0d7-575">número de identificação do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-575">tax identification number</span></span>
  
<span data-ttu-id="fe0d7-576">n º de identificação de imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-576">tax identification no.</span></span>
  
<span data-ttu-id="fe0d7-577">ID mokesčių</span><span class="sxs-lookup"><span data-stu-id="fe0d7-577">mokesčių id</span></span>
  
<span data-ttu-id="fe0d7-578">mokesčių Numeris</span><span class="sxs-lookup"><span data-stu-id="fe0d7-578">mokesčių numeris</span></span>
  
<span data-ttu-id="fe0d7-579">mokesčių identifikavimas Numeris</span><span class="sxs-lookup"><span data-stu-id="fe0d7-579">mokesčių identifikavimas numeris</span></span>
  
## <a name="luxemburg"></a><span data-ttu-id="fe0d7-580">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="fe0d7-580">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="fe0d7-581">Formato</span><span class="sxs-lookup"><span data-stu-id="fe0d7-581">Format</span></span>

<span data-ttu-id="fe0d7-582">13 dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="fe0d7-582">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fe0d7-583">Padrão</span><span class="sxs-lookup"><span data-stu-id="fe0d7-583">Pattern</span></span>

<span data-ttu-id="fe0d7-584">13 dígitos:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-584">13 digits:</span></span>
  
-  <span data-ttu-id="fe0d7-585">11 dígitos</span><span class="sxs-lookup"><span data-stu-id="fe0d7-585">11 digits</span></span> 
    
- <span data-ttu-id="fe0d7-586">Dois dígitos de verificação</span><span class="sxs-lookup"><span data-stu-id="fe0d7-586">Two check digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="fe0d7-587">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fe0d7-587">Checksum</span></span>

<span data-ttu-id="fe0d7-588">Sim</span><span class="sxs-lookup"><span data-stu-id="fe0d7-588">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="fe0d7-589">Definição</span><span class="sxs-lookup"><span data-stu-id="fe0d7-589">Definition</span></span>

<span data-ttu-id="fe0d7-590">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-590">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-591">A função `Func_luxemburg_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-591">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fe0d7-592">Uma palavra- `Keywords_luxemburg_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-592">A keyword from  `Keywords_luxemburg_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="fe0d7-593">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-593">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-594">A função `Func_luxemburg_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-594">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="fe0d7-595">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fe0d7-595">Keywords</span></span>

#### <a name="keywordsluxemburgeutaxfilenumber"></a><span data-ttu-id="fe0d7-596">Keywords_luxemburg_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="fe0d7-596">Keywords_luxemburg_eu_tax_file_number</span></span>

<span data-ttu-id="fe0d7-597">número do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-597">tax number</span></span>
  
<span data-ttu-id="fe0d7-598">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-598">tax no.</span></span>
  
<span data-ttu-id="fe0d7-599">taxno #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-599">taxno#</span></span>
  
<span data-ttu-id="fe0d7-600">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-600">taxnumber#</span></span>
  
<span data-ttu-id="fe0d7-601">taxnumber</span><span class="sxs-lookup"><span data-stu-id="fe0d7-601">taxnumber</span></span>
  
<span data-ttu-id="fe0d7-602">tax id
</span><span class="sxs-lookup"><span data-stu-id="fe0d7-602">tax id</span></span>
  
<span data-ttu-id="fe0d7-603">táxi #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-603">taxid#</span></span>
  
<span data-ttu-id="fe0d7-604">número de identificação do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-604">tax identification number</span></span>
  
<span data-ttu-id="fe0d7-605">n º de identificação de imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-605">tax identification no.</span></span>
  
<span data-ttu-id="fe0d7-606">steuernummer</span><span class="sxs-lookup"><span data-stu-id="fe0d7-606">steuernummer</span></span>
  
<span data-ttu-id="fe0d7-607">ID Steuer</span><span class="sxs-lookup"><span data-stu-id="fe0d7-607">steuer id</span></span>
  
<span data-ttu-id="fe0d7-608">steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="fe0d7-608">steueridentifikationsnummer</span></span>
  
## <a name="malta"></a><span data-ttu-id="fe0d7-609">Malta</span><span class="sxs-lookup"><span data-stu-id="fe0d7-609">Malta</span></span>

### <a name="format"></a><span data-ttu-id="fe0d7-610">Formato</span><span class="sxs-lookup"><span data-stu-id="fe0d7-610">Format</span></span>

<span data-ttu-id="fe0d7-611">Para as nacionalidades maltês: 7 dígitos e uma letra no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="fe0d7-611">For Maltese nationals: 7 digits and one letter in the specified pattern</span></span>
  
<span data-ttu-id="fe0d7-612">Entidades nacionais e Maltês não-maltês: 9 dígitos</span><span class="sxs-lookup"><span data-stu-id="fe0d7-612">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fe0d7-613">Padrão</span><span class="sxs-lookup"><span data-stu-id="fe0d7-613">Pattern</span></span>

<span data-ttu-id="fe0d7-614">Nacionalidades maltês: 7 dígitos e uma letra</span><span class="sxs-lookup"><span data-stu-id="fe0d7-614">Maltese nationals: 7 digits and one letter</span></span>
  
-  <span data-ttu-id="fe0d7-615">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="fe0d7-615">Seven digits</span></span> 
    
- <span data-ttu-id="fe0d7-616">Uma letra (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="fe0d7-616">One letter (not case-sensitive)</span></span>
    
<span data-ttu-id="fe0d7-617">Entidades nacionais e Maltês não-maltês: 9 dígitos</span><span class="sxs-lookup"><span data-stu-id="fe0d7-617">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
-  <span data-ttu-id="fe0d7-618">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="fe0d7-618">Nine digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="fe0d7-619">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fe0d7-619">Checksum</span></span>

<span data-ttu-id="fe0d7-620">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="fe0d7-620">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="fe0d7-621">Definição</span><span class="sxs-lookup"><span data-stu-id="fe0d7-621">Definition</span></span>

<span data-ttu-id="fe0d7-622">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-622">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-623">A função `Func_malta_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-623">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fe0d7-624">Uma palavra- `Keywords_malta_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-624">A keyword from  `Keywords_malta_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="fe0d7-625">Uma política de DLP tem 65% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-625">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-626">A função `Func_malta_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-626">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="fe0d7-627">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fe0d7-627">Keywords</span></span>

#### <a name="keywordsmaltaeutaxfilenumber"></a><span data-ttu-id="fe0d7-628">Keywords_malta_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="fe0d7-628">Keywords_malta_eu_tax_file_number</span></span>

<span data-ttu-id="fe0d7-629">número do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-629">tax number</span></span>
  
<span data-ttu-id="fe0d7-630">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-630">tax no.</span></span>
  
<span data-ttu-id="fe0d7-631">taxno #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-631">taxno#</span></span>
  
<span data-ttu-id="fe0d7-632">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-632">taxnumber#</span></span>
  
<span data-ttu-id="fe0d7-633">taxnumber</span><span class="sxs-lookup"><span data-stu-id="fe0d7-633">taxnumber</span></span>
  
<span data-ttu-id="fe0d7-634">tax id
</span><span class="sxs-lookup"><span data-stu-id="fe0d7-634">tax id</span></span>
  
<span data-ttu-id="fe0d7-635">táxi #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-635">taxid#</span></span>
  
<span data-ttu-id="fe0d7-636">número de identificação do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-636">tax identification number</span></span>
  
<span data-ttu-id="fe0d7-637">n º de identificação de imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-637">tax identification no.</span></span>
  
<span data-ttu-id="fe0d7-638">numru tat-taxxa</span><span class="sxs-lookup"><span data-stu-id="fe0d7-638">numru tat-taxxa</span></span>
  
<span data-ttu-id="fe0d7-639">ID tat-taxxa</span><span class="sxs-lookup"><span data-stu-id="fe0d7-639">id tat-taxxa</span></span>
  
<span data-ttu-id="fe0d7-640">numru ta ' identifikazzjoni tat-taxxa</span><span class="sxs-lookup"><span data-stu-id="fe0d7-640">numru ta 'identifikazzjoni tat-taxxa</span></span>
  
## <a name="netherlands"></a><span data-ttu-id="fe0d7-641">Países Baixos</span><span class="sxs-lookup"><span data-stu-id="fe0d7-641">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="fe0d7-642">Formato</span><span class="sxs-lookup"><span data-stu-id="fe0d7-642">Format</span></span>

<span data-ttu-id="fe0d7-643">Nove dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="fe0d7-643">Nine digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fe0d7-644">Padrão</span><span class="sxs-lookup"><span data-stu-id="fe0d7-644">Pattern</span></span>

<span data-ttu-id="fe0d7-645">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="fe0d7-645">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="fe0d7-646">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fe0d7-646">Checksum</span></span>

<span data-ttu-id="fe0d7-647">Sim</span><span class="sxs-lookup"><span data-stu-id="fe0d7-647">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="fe0d7-648">Definição</span><span class="sxs-lookup"><span data-stu-id="fe0d7-648">Definition</span></span>

<span data-ttu-id="fe0d7-649">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-649">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-650">A função `Func_netherlands_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-650">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fe0d7-651">Uma palavra- `Keywords_netherlands_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-651">A keyword from  `Keywords_netherlands_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="fe0d7-652">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-652">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-653">A função `Func_netherlands_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-653">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="fe0d7-654">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fe0d7-654">Keywords</span></span>

#### <a name="keywordsnetherlandseutaxfilenumber"></a><span data-ttu-id="fe0d7-655">Keywords_netherlands_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="fe0d7-655">Keywords_netherlands_eu_tax_file_number</span></span>

<span data-ttu-id="fe0d7-656">número de identificação do imposto Holanda</span><span class="sxs-lookup"><span data-stu-id="fe0d7-656">netherlands tax identification number</span></span>
  
<span data-ttu-id="fe0d7-657">identificação de imposto Holanda</span><span class="sxs-lookup"><span data-stu-id="fe0d7-657">netherlands tax identification</span></span>
  
<span data-ttu-id="fe0d7-658">número de identificação de imposto do Netherland</span><span class="sxs-lookup"><span data-stu-id="fe0d7-658">netherland's tax identification number</span></span>
  
<span data-ttu-id="fe0d7-659">identificação de imposto do Netherland</span><span class="sxs-lookup"><span data-stu-id="fe0d7-659">netherland's tax identification</span></span>
  
<span data-ttu-id="fe0d7-660">número de identificação do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-660">tax identification number</span></span>
  
<span data-ttu-id="fe0d7-661">ID de imposto holandês</span><span class="sxs-lookup"><span data-stu-id="fe0d7-661">dutch tax id</span></span>
  
<span data-ttu-id="fe0d7-662">número de identificação do imposto holandês</span><span class="sxs-lookup"><span data-stu-id="fe0d7-662">dutch tax identification number</span></span>
  
<span data-ttu-id="fe0d7-663">tax id
</span><span class="sxs-lookup"><span data-stu-id="fe0d7-663">tax id</span></span>
  
<span data-ttu-id="fe0d7-664">ID de imposto #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-664">tax id#</span></span>
  
<span data-ttu-id="fe0d7-665">número do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-665">tax number</span></span>
  
<span data-ttu-id="fe0d7-666">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-666">tax no#</span></span>
  
<span data-ttu-id="fe0d7-667">imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-667">tax#</span></span>
  
<span data-ttu-id="fe0d7-668">tin
</span><span class="sxs-lookup"><span data-stu-id="fe0d7-668">tin</span></span>
  
<span data-ttu-id="fe0d7-669">Tin</span><span class="sxs-lookup"><span data-stu-id="fe0d7-669">tin#</span></span>
  
<span data-ttu-id="fe0d7-670">Tin Holanda</span><span class="sxs-lookup"><span data-stu-id="fe0d7-670">netherlands tin</span></span>
  
<span data-ttu-id="fe0d7-671">Tin do Netherland</span><span class="sxs-lookup"><span data-stu-id="fe0d7-671">netherland's tin</span></span>
  
<span data-ttu-id="fe0d7-672">Países Baixos identificatienummer</span><span class="sxs-lookup"><span data-stu-id="fe0d7-672">nederlands belasting identificatienummer</span></span>
  
<span data-ttu-id="fe0d7-673">identificatienummer Van é última</span><span class="sxs-lookup"><span data-stu-id="fe0d7-673">identificatienummer van belasting</span></span>
  
<span data-ttu-id="fe0d7-674">identificatienummer a última</span><span class="sxs-lookup"><span data-stu-id="fe0d7-674">identificatienummer belasting</span></span>
  
<span data-ttu-id="fe0d7-675">Países Baixos identificatie</span><span class="sxs-lookup"><span data-stu-id="fe0d7-675">nederlands belasting identificatie</span></span>
  
<span data-ttu-id="fe0d7-676">Países Baixos Nummer ID da última vez</span><span class="sxs-lookup"><span data-stu-id="fe0d7-676">nederlands belasting id nummer</span></span>
  
<span data-ttu-id="fe0d7-677">Países Baixos belastingnummer</span><span class="sxs-lookup"><span data-stu-id="fe0d7-677">nederlands belastingnummer</span></span>
  
<span data-ttu-id="fe0d7-678">BTW Nummer</span><span class="sxs-lookup"><span data-stu-id="fe0d7-678">btw nummer</span></span>
  
<span data-ttu-id="fe0d7-679">Nederlandse identificatie</span><span class="sxs-lookup"><span data-stu-id="fe0d7-679">nederlandse belasting identificatie</span></span>
  
## <a name="poland"></a><span data-ttu-id="fe0d7-680">Polônia</span><span class="sxs-lookup"><span data-stu-id="fe0d7-680">Poland</span></span>

### <a name="format"></a><span data-ttu-id="fe0d7-681">Formato</span><span class="sxs-lookup"><span data-stu-id="fe0d7-681">Format</span></span>

<span data-ttu-id="fe0d7-682">Onze dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="fe0d7-682">Eleven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fe0d7-683">Padrão</span><span class="sxs-lookup"><span data-stu-id="fe0d7-683">Pattern</span></span>

<span data-ttu-id="fe0d7-684">Onze dígitos</span><span class="sxs-lookup"><span data-stu-id="fe0d7-684">Eleven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="fe0d7-685">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fe0d7-685">Checksum</span></span>

<span data-ttu-id="fe0d7-686">Sim</span><span class="sxs-lookup"><span data-stu-id="fe0d7-686">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="fe0d7-687">Definição</span><span class="sxs-lookup"><span data-stu-id="fe0d7-687">Definition</span></span>

<span data-ttu-id="fe0d7-688">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-688">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-689">A função `Func_poland_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-689">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fe0d7-690">Uma palavra- `Keywords_poland_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-690">A keyword from  `Keywords_poland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="fe0d7-691">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-691">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-692">A função `Func_poland_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-692">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="fe0d7-693">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fe0d7-693">Keywords</span></span>

#### <a name="keywordspolandeutaxfilenumber"></a><span data-ttu-id="fe0d7-694">Keywords_poland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="fe0d7-694">Keywords_poland_eu_tax_file_number</span></span>

<span data-ttu-id="fe0d7-695">número do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-695">tax number</span></span>
  
<span data-ttu-id="fe0d7-696">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-696">tax no.</span></span>
  
<span data-ttu-id="fe0d7-697">taxno #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-697">taxno#</span></span>
  
<span data-ttu-id="fe0d7-698">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-698">taxnumber#</span></span>
  
<span data-ttu-id="fe0d7-699">taxnumber</span><span class="sxs-lookup"><span data-stu-id="fe0d7-699">taxnumber</span></span>
  
<span data-ttu-id="fe0d7-700">Nip</span><span class="sxs-lookup"><span data-stu-id="fe0d7-700">nip</span></span>
  
<span data-ttu-id="fe0d7-701">Nip #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-701">nip#</span></span>
  
<span data-ttu-id="fe0d7-702">tax id
</span><span class="sxs-lookup"><span data-stu-id="fe0d7-702">tax id</span></span>
  
<span data-ttu-id="fe0d7-703">ID de imposto #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-703">tax id#</span></span>
  
<span data-ttu-id="fe0d7-704">ID Nip</span><span class="sxs-lookup"><span data-stu-id="fe0d7-704">nip id</span></span>
  
<span data-ttu-id="fe0d7-705">NIP ID #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-705">nip id#</span></span>
  
<span data-ttu-id="fe0d7-706">número de identificação do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-706">tax identification number</span></span>
  
<span data-ttu-id="fe0d7-707">n º de identificação de imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-707">tax identification no.</span></span>
  
<span data-ttu-id="fe0d7-708">número de IVA</span><span class="sxs-lookup"><span data-stu-id="fe0d7-708">vat number</span></span>
  
<span data-ttu-id="fe0d7-709">IVA não.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-709">vat no.</span></span>
  
<span data-ttu-id="fe0d7-710">vatno #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-710">vatno#</span></span>
  
<span data-ttu-id="fe0d7-711">ID de IVA</span><span class="sxs-lookup"><span data-stu-id="fe0d7-711">vat id</span></span>
  
<span data-ttu-id="fe0d7-712">ID de IVA #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-712">vat id#</span></span>
  
<span data-ttu-id="fe0d7-713">numer identyfikacji podatkowej</span><span class="sxs-lookup"><span data-stu-id="fe0d7-713">numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="fe0d7-714">Polski numer identyfikacji podatkowej</span><span class="sxs-lookup"><span data-stu-id="fe0d7-714">polski numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="fe0d7-715">numeridentyfikacjipodatkowej #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-715">numeridentyfikacjipodatkowej#</span></span>
  
## <a name="portugal"></a><span data-ttu-id="fe0d7-716">Portugal</span><span class="sxs-lookup"><span data-stu-id="fe0d7-716">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="fe0d7-717">Formato</span><span class="sxs-lookup"><span data-stu-id="fe0d7-717">Format</span></span>

<span data-ttu-id="fe0d7-718">Nove dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="fe0d7-718">Nine digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fe0d7-719">Padrão</span><span class="sxs-lookup"><span data-stu-id="fe0d7-719">Pattern</span></span>

<span data-ttu-id="fe0d7-720">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="fe0d7-720">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="fe0d7-721">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fe0d7-721">Checksum</span></span>

<span data-ttu-id="fe0d7-722">Sim</span><span class="sxs-lookup"><span data-stu-id="fe0d7-722">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="fe0d7-723">Definição</span><span class="sxs-lookup"><span data-stu-id="fe0d7-723">Definition</span></span>

<span data-ttu-id="fe0d7-724">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-724">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-725">A função `Func_portugal_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-725">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fe0d7-726">Uma palavra- `Keywords_portugal_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-726">A keyword from  `Keywords_portugal_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="fe0d7-727">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-727">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-728">A função `Func_portugal_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-728">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="fe0d7-729">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fe0d7-729">Keywords</span></span>

#### <a name="keywordsportugaleutaxfilenumber"></a><span data-ttu-id="fe0d7-730">Keywords_portugal_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="fe0d7-730">Keywords_portugal_eu_tax_file_number</span></span>

<span data-ttu-id="fe0d7-731">número do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-731">tax number</span></span>
  
<span data-ttu-id="fe0d7-732">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-732">tax no.</span></span>
  
<span data-ttu-id="fe0d7-733">taxno #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-733">taxno#</span></span>
  
<span data-ttu-id="fe0d7-734">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-734">taxnumber#</span></span>
  
<span data-ttu-id="fe0d7-735">taxnumber</span><span class="sxs-lookup"><span data-stu-id="fe0d7-735">taxnumber</span></span>
  
<span data-ttu-id="fe0d7-736">nse</span><span class="sxs-lookup"><span data-stu-id="fe0d7-736">nif</span></span>
  
<span data-ttu-id="fe0d7-737">nse</span><span class="sxs-lookup"><span data-stu-id="fe0d7-737">nif#</span></span>
  
<span data-ttu-id="fe0d7-738">fiscal numero</span><span class="sxs-lookup"><span data-stu-id="fe0d7-738">numero fiscal</span></span>
  
<span data-ttu-id="fe0d7-739">número de identificação fiscal</span><span class="sxs-lookup"><span data-stu-id="fe0d7-739">número de identificação fiscal</span></span>
  
## <a name="romania"></a><span data-ttu-id="fe0d7-740">Romênia</span><span class="sxs-lookup"><span data-stu-id="fe0d7-740">Romania</span></span>

### <a name="format"></a><span data-ttu-id="fe0d7-741">Formato</span><span class="sxs-lookup"><span data-stu-id="fe0d7-741">Format</span></span>

<span data-ttu-id="fe0d7-742">13 dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="fe0d7-742">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fe0d7-743">Padrão</span><span class="sxs-lookup"><span data-stu-id="fe0d7-743">Pattern</span></span>

<span data-ttu-id="fe0d7-744">13 dígitos</span><span class="sxs-lookup"><span data-stu-id="fe0d7-744">13 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="fe0d7-745">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fe0d7-745">Checksum</span></span>

<span data-ttu-id="fe0d7-746">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="fe0d7-746">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="fe0d7-747">Definição</span><span class="sxs-lookup"><span data-stu-id="fe0d7-747">Definition</span></span>

<span data-ttu-id="fe0d7-748">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-748">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-749">A expressão `Regex_romania_eu_tax_file_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-749">The regular expression  `Regex_romania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fe0d7-750">Uma palavra- `Keywords_romania_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-750">A keyword from  `Keywords_romania_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_tax_file_number" />
          <Match idRef="Keywords_romania_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fe0d7-751">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fe0d7-751">Keywords</span></span>

#### <a name="keywordsromaniaeutaxfilenumber"></a><span data-ttu-id="fe0d7-752">Keywords_romania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="fe0d7-752">Keywords_romania_eu_tax_file_number</span></span>

<span data-ttu-id="fe0d7-753">tax id
</span><span class="sxs-lookup"><span data-stu-id="fe0d7-753">tax id</span></span>
  
<span data-ttu-id="fe0d7-754">número de ID do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-754">tax id number</span></span>
  
<span data-ttu-id="fe0d7-755">arquivo de imposto não</span><span class="sxs-lookup"><span data-stu-id="fe0d7-755">tax file no</span></span>
  
<span data-ttu-id="fe0d7-756">

tax file number</span><span class="sxs-lookup"><span data-stu-id="fe0d7-756">tax file number</span></span>
  
<span data-ttu-id="fe0d7-757">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-757">tax no</span></span>
  
<span data-ttu-id="fe0d7-758">número do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-758">tax number</span></span>
  
<span data-ttu-id="fe0d7-759">táxi #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-759">taxid#</span></span>
  
<span data-ttu-id="fe0d7-760">taxno #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-760">taxno#</span></span>
  
<span data-ttu-id="fe0d7-761">ID-UL Taxei</span><span class="sxs-lookup"><span data-stu-id="fe0d7-761">id-ul taxei</span></span>
  
<span data-ttu-id="fe0d7-762">numărul de identificare Fiscală</span><span class="sxs-lookup"><span data-stu-id="fe0d7-762">numărul de identificare fiscală</span></span>
  
## <a name="slovakia"></a><span data-ttu-id="fe0d7-763">Eslováquia</span><span class="sxs-lookup"><span data-stu-id="fe0d7-763">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="fe0d7-764">Formato</span><span class="sxs-lookup"><span data-stu-id="fe0d7-764">Format</span></span>

<span data-ttu-id="fe0d7-765">10 dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="fe0d7-765">10 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fe0d7-766">Padrão</span><span class="sxs-lookup"><span data-stu-id="fe0d7-766">Pattern</span></span>

<span data-ttu-id="fe0d7-767">10 dígitos</span><span class="sxs-lookup"><span data-stu-id="fe0d7-767">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="fe0d7-768">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fe0d7-768">Checksum</span></span>

<span data-ttu-id="fe0d7-769">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="fe0d7-769">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="fe0d7-770">Definição</span><span class="sxs-lookup"><span data-stu-id="fe0d7-770">Definition</span></span>

<span data-ttu-id="fe0d7-771">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-771">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-772">A expressão `Regex_slovakia_eu_tax_file_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-772">The regular expression  `Regex_slovakia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fe0d7-773">Uma palavra- `Keywords_slovakia_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-773">A keyword from  `Keywords_slovakia_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_tax_file_number" />
          <Match idRef="Keywords_slovakia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fe0d7-774">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fe0d7-774">Keywords</span></span>

#### <a name="keywordsslovakiaeutaxfilenumber"></a><span data-ttu-id="fe0d7-775">Keywords_slovakia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="fe0d7-775">Keywords_slovakia_eu_tax_file_number</span></span>

<span data-ttu-id="fe0d7-776">tax id
</span><span class="sxs-lookup"><span data-stu-id="fe0d7-776">tax id</span></span>
  
<span data-ttu-id="fe0d7-777">número de ID do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-777">tax id number</span></span>
  
<span data-ttu-id="fe0d7-778">ID do Tin</span><span class="sxs-lookup"><span data-stu-id="fe0d7-778">tin id</span></span>
  
<span data-ttu-id="fe0d7-779">Tin não</span><span class="sxs-lookup"><span data-stu-id="fe0d7-779">tin no</span></span>
  
<span data-ttu-id="fe0d7-780">ID de Tin de eslovaco</span><span class="sxs-lookup"><span data-stu-id="fe0d7-780">slovakian tin id</span></span>
  
<span data-ttu-id="fe0d7-781">tin
</span><span class="sxs-lookup"><span data-stu-id="fe0d7-781">tin</span></span>
  
<span data-ttu-id="fe0d7-782">arquivo de imposto não</span><span class="sxs-lookup"><span data-stu-id="fe0d7-782">tax file no</span></span>
  
<span data-ttu-id="fe0d7-783">

tax file number</span><span class="sxs-lookup"><span data-stu-id="fe0d7-783">tax file number</span></span>
  
<span data-ttu-id="fe0d7-784">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-784">tax no</span></span>
  
<span data-ttu-id="fe0d7-785">número do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-785">tax number</span></span>
  
<span data-ttu-id="fe0d7-786">táxi #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-786">taxid#</span></span>
  
<span data-ttu-id="fe0d7-787">taxno #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-787">taxno#</span></span>
  
<span data-ttu-id="fe0d7-788">daňové identifikačné číslo</span><span class="sxs-lookup"><span data-stu-id="fe0d7-788">daňové identifikačné číslo</span></span>
  
<span data-ttu-id="fe0d7-789">daňové číslo</span><span class="sxs-lookup"><span data-stu-id="fe0d7-789">daňové číslo</span></span>
  
<span data-ttu-id="fe0d7-790">daňové číslo súboru</span><span class="sxs-lookup"><span data-stu-id="fe0d7-790">daňové číslo súboru</span></span>
  
## <a name="slovenia"></a><span data-ttu-id="fe0d7-791">Eslovênia</span><span class="sxs-lookup"><span data-stu-id="fe0d7-791">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="fe0d7-792">Formato</span><span class="sxs-lookup"><span data-stu-id="fe0d7-792">Format</span></span>

<span data-ttu-id="fe0d7-793">Oito dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="fe0d7-793">Eight digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fe0d7-794">Padrão</span><span class="sxs-lookup"><span data-stu-id="fe0d7-794">Pattern</span></span>

<span data-ttu-id="fe0d7-795">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="fe0d7-795">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="fe0d7-796">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fe0d7-796">Checksum</span></span>

<span data-ttu-id="fe0d7-797">Sim</span><span class="sxs-lookup"><span data-stu-id="fe0d7-797">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="fe0d7-798">Definição</span><span class="sxs-lookup"><span data-stu-id="fe0d7-798">Definition</span></span>

<span data-ttu-id="fe0d7-799">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-799">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-800">A função `Func_slovenia_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-800">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fe0d7-801">Uma palavra- `Keywords_slovenia_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-801">A keyword from  `Keywords_slovenia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="fe0d7-802">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-802">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-803">A função `Func_slovenia_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-803">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="fe0d7-804">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fe0d7-804">Keywords</span></span>

#### <a name="keywordssloveniaeutaxfilenumber"></a><span data-ttu-id="fe0d7-805">Keywords_slovenia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="fe0d7-805">Keywords_slovenia_eu_tax_file_number</span></span>

<span data-ttu-id="fe0d7-806">tax id
</span><span class="sxs-lookup"><span data-stu-id="fe0d7-806">tax id</span></span>
  
<span data-ttu-id="fe0d7-807">número de ID do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-807">tax id number</span></span>
  
<span data-ttu-id="fe0d7-808">ID do Tin</span><span class="sxs-lookup"><span data-stu-id="fe0d7-808">tin id</span></span>
  
<span data-ttu-id="fe0d7-809">Tin não</span><span class="sxs-lookup"><span data-stu-id="fe0d7-809">tin no</span></span>
  
<span data-ttu-id="fe0d7-810">ID de Tin esloveno</span><span class="sxs-lookup"><span data-stu-id="fe0d7-810">slovenian tin id</span></span>
  
<span data-ttu-id="fe0d7-811">tin
</span><span class="sxs-lookup"><span data-stu-id="fe0d7-811">tin</span></span>
  
<span data-ttu-id="fe0d7-812">arquivo de imposto não</span><span class="sxs-lookup"><span data-stu-id="fe0d7-812">tax file no</span></span>
  
<span data-ttu-id="fe0d7-813">

tax file number</span><span class="sxs-lookup"><span data-stu-id="fe0d7-813">tax file number</span></span>
  
<span data-ttu-id="fe0d7-814">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-814">tax no</span></span>
  
<span data-ttu-id="fe0d7-815">número do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-815">tax number</span></span>
  
<span data-ttu-id="fe0d7-816">táxi #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-816">taxid#</span></span>
  
<span data-ttu-id="fe0d7-817">taxno #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-817">taxno#</span></span>
  
<span data-ttu-id="fe0d7-818">identifikacijska številka davka</span><span class="sxs-lookup"><span data-stu-id="fe0d7-818">identifikacijska številka davka</span></span>
  
<span data-ttu-id="fe0d7-819">davčna številka</span><span class="sxs-lookup"><span data-stu-id="fe0d7-819">davčna številka</span></span>
  
<span data-ttu-id="fe0d7-820">številka davčne datoteke</span><span class="sxs-lookup"><span data-stu-id="fe0d7-820">številka davčne datoteke</span></span>
  
## <a name="spain"></a><span data-ttu-id="fe0d7-821">Espanha</span><span class="sxs-lookup"><span data-stu-id="fe0d7-821">Spain</span></span>

### <a name="format"></a><span data-ttu-id="fe0d7-822">Formato</span><span class="sxs-lookup"><span data-stu-id="fe0d7-822">Format</span></span>

<span data-ttu-id="fe0d7-823">Sete ou oito dígitos e uma ou duas letras no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="fe0d7-823">Seven or eight digits and one or two letters in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fe0d7-824">Padrão</span><span class="sxs-lookup"><span data-stu-id="fe0d7-824">Pattern</span></span>

<span data-ttu-id="fe0d7-825">Pessoas naturais do espanhol com um cartão de identidade nacional da Espanha:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-825">Spanish Natural Persons with a Spain National Identity Card:</span></span>
  
-  <span data-ttu-id="fe0d7-826">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="fe0d7-826">Eight digits</span></span> 
    
- <span data-ttu-id="fe0d7-827">Uma letra maiúscula (diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="fe0d7-827">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="fe0d7-828">Spaniards não residente sem um cartão de identidade nacional da Espanha</span><span class="sxs-lookup"><span data-stu-id="fe0d7-828">Non-resident Spaniards without a Spain National Identity Card</span></span>
  
- <span data-ttu-id="fe0d7-829">Uma letra maiúscula "L" (diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="fe0d7-829">One uppercase letter "L" (case-sensitive)</span></span>
    
- <span data-ttu-id="fe0d7-830">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="fe0d7-830">Seven digits</span></span>
    
- <span data-ttu-id="fe0d7-831">Uma letra maiúscula (diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="fe0d7-831">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="fe0d7-832">Spaniards residentes sob a idade de 14 anos sem um cartão de identidade nacional da Espanha:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-832">Resident Spaniards under the age of 14 years without a Spain National Identity Card :</span></span>
  
- <span data-ttu-id="fe0d7-833">Uma letra maiúscula "K" (diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="fe0d7-833">One uppercase letter"K" (case-sensitive)</span></span>
    
-  <span data-ttu-id="fe0d7-834">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="fe0d7-834">Seven digits</span></span> 
    
- <span data-ttu-id="fe0d7-835">Uma letra maiúscula (diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="fe0d7-835">One uppercase letter (case-sensitive)</span></span>
    
<span data-ttu-id="fe0d7-836">Foreigners com o número de identificação do estrangeiro</span><span class="sxs-lookup"><span data-stu-id="fe0d7-836">Foreigners with a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="fe0d7-837">Uma letra maiúscula que é "X", "Y" ou "Z" (diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="fe0d7-837">One uppercase letter that is "X", "Y", or "Z" (case-sensitive)</span></span> 
    
- <span data-ttu-id="fe0d7-838">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="fe0d7-838">Seven digits</span></span>
    
- <span data-ttu-id="fe0d7-839">Uma letra maiúscula (diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="fe0d7-839">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="fe0d7-840">Foreigners sem um número de identificação do estrangeiro</span><span class="sxs-lookup"><span data-stu-id="fe0d7-840">Foreigners without a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="fe0d7-841">Uma letra maiúscula que é "M" (diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="fe0d7-841">One uppercase letter that is "M" (case-sensitive)</span></span> 
    
- <span data-ttu-id="fe0d7-842">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="fe0d7-842">Seven digits</span></span>
    
- <span data-ttu-id="fe0d7-843">Uma letra maiúscula (diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="fe0d7-843">One uppercase letter (case-sensitive)</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="fe0d7-844">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fe0d7-844">Checksum</span></span>

<span data-ttu-id="fe0d7-845">Sim</span><span class="sxs-lookup"><span data-stu-id="fe0d7-845">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="fe0d7-846">Definição</span><span class="sxs-lookup"><span data-stu-id="fe0d7-846">Definition</span></span>

<span data-ttu-id="fe0d7-847">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-847">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-848">A função `Func_spain_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-848">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fe0d7-849">Uma palavra- `Keywords_spain_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-849">A keyword from  `Keywords_spain_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="fe0d7-850">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-850">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-851">A função `Func_spain_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-851">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="fe0d7-852">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fe0d7-852">Keywords</span></span>

#### <a name="keywordsspaineutaxfilenumber"></a><span data-ttu-id="fe0d7-853">Keywords_spain_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="fe0d7-853">Keywords_spain_eu_tax_file_number</span></span>

<span data-ttu-id="fe0d7-854">tax id
</span><span class="sxs-lookup"><span data-stu-id="fe0d7-854">tax id</span></span>
  
<span data-ttu-id="fe0d7-855">número de ID do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-855">tax id number</span></span>
  
<span data-ttu-id="fe0d7-856">ID de CIF</span><span class="sxs-lookup"><span data-stu-id="fe0d7-856">cif id</span></span>
  
<span data-ttu-id="fe0d7-857">Não CIF</span><span class="sxs-lookup"><span data-stu-id="fe0d7-857">cif no</span></span>
  
<span data-ttu-id="fe0d7-858">ID de CIF espanhol</span><span class="sxs-lookup"><span data-stu-id="fe0d7-858">spanish cif id</span></span>
  
<span data-ttu-id="fe0d7-859">CIF</span><span class="sxs-lookup"><span data-stu-id="fe0d7-859">cif</span></span>
  
<span data-ttu-id="fe0d7-860">arquivo de imposto não</span><span class="sxs-lookup"><span data-stu-id="fe0d7-860">tax file no</span></span>
  
<span data-ttu-id="fe0d7-861">número de CIF espanhol</span><span class="sxs-lookup"><span data-stu-id="fe0d7-861">spanish cif number</span></span>
  
<span data-ttu-id="fe0d7-862">

tax file number</span><span class="sxs-lookup"><span data-stu-id="fe0d7-862">tax file number</span></span>
  
<span data-ttu-id="fe0d7-863">Não CIF espanhol</span><span class="sxs-lookup"><span data-stu-id="fe0d7-863">spanish cif no</span></span>
  
<span data-ttu-id="fe0d7-864">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-864">tax no</span></span>
  
<span data-ttu-id="fe0d7-865">número do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-865">tax number</span></span>
  
<span data-ttu-id="fe0d7-866">táxi #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-866">taxid#</span></span>
  
<span data-ttu-id="fe0d7-867">taxno #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-867">taxno#</span></span>
  
<span data-ttu-id="fe0d7-868">cifid #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-868">cifid#</span></span>
  
<span data-ttu-id="fe0d7-869">spanishcifid #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-869">spanishcifid#</span></span>
  
<span data-ttu-id="fe0d7-870">spanishcifno #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-870">spanishcifno#</span></span>
  
<span data-ttu-id="fe0d7-871">número de contribuyente</span><span class="sxs-lookup"><span data-stu-id="fe0d7-871">número de contribuyente</span></span>
  
<span data-ttu-id="fe0d7-872">número de impuesto corporativo</span><span class="sxs-lookup"><span data-stu-id="fe0d7-872">número de impuesto corporativo</span></span>
  
<span data-ttu-id="fe0d7-873">número de Identificación fiscal</span><span class="sxs-lookup"><span data-stu-id="fe0d7-873">número de identificación fiscal</span></span>
  
<span data-ttu-id="fe0d7-874">número CIF</span><span class="sxs-lookup"><span data-stu-id="fe0d7-874">cif número</span></span>
  
<span data-ttu-id="fe0d7-875">cifnúmero #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-875">cifnúmero#</span></span>
  
## <a name="sweden"></a><span data-ttu-id="fe0d7-876">Suécia</span><span class="sxs-lookup"><span data-stu-id="fe0d7-876">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="fe0d7-877">Formato</span><span class="sxs-lookup"><span data-stu-id="fe0d7-877">Format</span></span>

<span data-ttu-id="fe0d7-878">Dez dígitos e um símbolo no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="fe0d7-878">Ten digits and a symbol in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fe0d7-879">Padrão</span><span class="sxs-lookup"><span data-stu-id="fe0d7-879">Pattern</span></span>

<span data-ttu-id="fe0d7-880">Dez dígitos e um símbolo:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-880">Ten digits and a symbol:</span></span>
  
-  <span data-ttu-id="fe0d7-881">Seis dígitos que correspondem à data de nascimento (AAMMDD)</span><span class="sxs-lookup"><span data-stu-id="fe0d7-881">Six digits that correspond to the birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="fe0d7-882">Um sinal de adição, sinal de menos ou barra invertida</span><span class="sxs-lookup"><span data-stu-id="fe0d7-882">A plus sign, minus sign, or backslash</span></span>
    
- <span data-ttu-id="fe0d7-883">Três dígitos que tornam o número de identificação exclusivo, onde:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-883">Three digits that make the identification number unique where:</span></span> 
    
  - <span data-ttu-id="fe0d7-884">Para números emitidos antes de 1990, o sétimo e oitavo dígito identificam o Condado de nascimento ou pessoas de nasceu</span><span class="sxs-lookup"><span data-stu-id="fe0d7-884">For numbers issued before 1990, the seventh and eighth digit identify the county of birth or foreign-born people</span></span>
    
  - <span data-ttu-id="fe0d7-885">O dígito na nona posição indica sexo por tanto ímpar para masculino ou par para fêmea</span><span class="sxs-lookup"><span data-stu-id="fe0d7-885">The digit in the ninth position indicates gender by either odd for male or even for female</span></span>
    
- <span data-ttu-id="fe0d7-886">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="fe0d7-886">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="fe0d7-887">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fe0d7-887">Checksum</span></span>

<span data-ttu-id="fe0d7-888">Sim</span><span class="sxs-lookup"><span data-stu-id="fe0d7-888">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="fe0d7-889">Definição</span><span class="sxs-lookup"><span data-stu-id="fe0d7-889">Definition</span></span>

<span data-ttu-id="fe0d7-890">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-890">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-891">A função `Func_sweden_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-891">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fe0d7-892">Uma palavra- `Keywords_sweden_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-892">A keyword from  `Keywords_sweden_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="fe0d7-893">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-893">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-894">A função `Func_sweden_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-894">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="fe0d7-895">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fe0d7-895">Keywords</span></span>

#### <a name="keywordsswedeneutaxfilenumber"></a><span data-ttu-id="fe0d7-896">Keywords_sweden_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="fe0d7-896">Keywords_sweden_eu_tax_file_number</span></span>

<span data-ttu-id="fe0d7-897">tax id
</span><span class="sxs-lookup"><span data-stu-id="fe0d7-897">tax id</span></span>
  
<span data-ttu-id="fe0d7-898">n º de ID de imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-898">tax id no.</span></span>
  
<span data-ttu-id="fe0d7-899">número de ID do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-899">tax id number</span></span>
  
<span data-ttu-id="fe0d7-900">tax identification
</span><span class="sxs-lookup"><span data-stu-id="fe0d7-900">tax identification</span></span>
  
<span data-ttu-id="fe0d7-901">identificação de imposto #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-901">tax identification#</span></span>
  
<span data-ttu-id="fe0d7-902">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-902">tax no.</span></span>
  
<span data-ttu-id="fe0d7-903">imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-903">tax#</span></span>
  
<span data-ttu-id="fe0d7-904">táxi #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-904">taxid#</span></span>
  
<span data-ttu-id="fe0d7-905">arquivo de imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-905">tax file</span></span>
  
<span data-ttu-id="fe0d7-906">arquivo de impostos não.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-906">tax file no.</span></span>
  
<span data-ttu-id="fe0d7-907">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="fe0d7-907">personal id number</span></span>
  
<span data-ttu-id="fe0d7-908">skatt ID Nummer</span><span class="sxs-lookup"><span data-stu-id="fe0d7-908">skatt id nummer</span></span>
  
<span data-ttu-id="fe0d7-909">skatt identifikation</span><span class="sxs-lookup"><span data-stu-id="fe0d7-909">skatt identifikation</span></span>
  
<span data-ttu-id="fe0d7-910">personnummer</span><span class="sxs-lookup"><span data-stu-id="fe0d7-910">personnummer</span></span>
  
## <a name="uk"></a><span data-ttu-id="fe0d7-911">Reino Unido</span><span class="sxs-lookup"><span data-stu-id="fe0d7-911">UK</span></span>

### <a name="format"></a><span data-ttu-id="fe0d7-912">Formato</span><span class="sxs-lookup"><span data-stu-id="fe0d7-912">Format</span></span>

<span data-ttu-id="fe0d7-913">Referência de contribuidor exclusivo (UTR): 10 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="fe0d7-913">Unique Taxpayer Reference (UTR): 10 digits without spaces and delimiters</span></span>
  
<span data-ttu-id="fe0d7-p103">Número de seguro nacional (NINO): para obter detalhes, consulte a seção "número de seguro nacional do Reino Unido (NINO)" em [o que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="fe0d7-p103">National Insurance Number (NINO): For details, see the section "U.K. National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fe0d7-916">Padrão</span><span class="sxs-lookup"><span data-stu-id="fe0d7-916">Pattern</span></span>

<span data-ttu-id="fe0d7-917">Referência de contribuidor exclusivo (UTR): 10 dígitos</span><span class="sxs-lookup"><span data-stu-id="fe0d7-917">Unique Taxpayer Reference (UTR): 10 digits</span></span>
  
<span data-ttu-id="fe0d7-p104">Número de seguro nacional (NINO): para obter detalhes, consulte a seção "número de seguro nacional do Reino Unido (NINO)" em [o que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="fe0d7-p104">National Insurance Number (NINO): For details, see the section "U.K. National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="checksum"></a><span data-ttu-id="fe0d7-920">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fe0d7-920">Checksum</span></span>

<span data-ttu-id="fe0d7-921">Sim</span><span class="sxs-lookup"><span data-stu-id="fe0d7-921">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="fe0d7-922">Definição</span><span class="sxs-lookup"><span data-stu-id="fe0d7-922">Definition</span></span>

<span data-ttu-id="fe0d7-923">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fe0d7-923">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fe0d7-924">A função `Func_uk_eu_tax_file_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-924">The function  `Func_uk_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fe0d7-925">Uma palavra- `Keywords_uk_eu_tax_file_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-925">A keyword from  `Keywords_uk_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_uk_eu_tax_file_number" />
          <Match idRef="Keywords_uk_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fe0d7-926">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fe0d7-926">Keywords</span></span>

#### <a name="keywordsukeutaxfilenumber"></a><span data-ttu-id="fe0d7-927">Keywords_uk_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="fe0d7-927">Keywords_uk_eu_tax_file_number</span></span>

<span data-ttu-id="fe0d7-928">tax id
</span><span class="sxs-lookup"><span data-stu-id="fe0d7-928">tax id</span></span>
  
<span data-ttu-id="fe0d7-929">n º de ID de imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-929">tax id no.</span></span>
  
<span data-ttu-id="fe0d7-930">número de ID do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-930">tax id number</span></span>
  
<span data-ttu-id="fe0d7-931">tax identification
</span><span class="sxs-lookup"><span data-stu-id="fe0d7-931">tax identification</span></span>
  
<span data-ttu-id="fe0d7-932">identificação de imposto #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-932">tax identification#</span></span>
  
<span data-ttu-id="fe0d7-933">n º do imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-933">tax no.</span></span>
  
<span data-ttu-id="fe0d7-934">imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-934">tax#</span></span>
  
<span data-ttu-id="fe0d7-935">táxi #</span><span class="sxs-lookup"><span data-stu-id="fe0d7-935">taxid#</span></span>
  
<span data-ttu-id="fe0d7-936">arquivo de imposto</span><span class="sxs-lookup"><span data-stu-id="fe0d7-936">tax file</span></span>
  
<span data-ttu-id="fe0d7-937">arquivo de impostos não.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-937">tax file no.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fe0d7-938">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe0d7-938">See also</span></span>

[<span data-ttu-id="fe0d7-939">O que os tipos de informação confidencial procuram</span><span class="sxs-lookup"><span data-stu-id="fe0d7-939">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)


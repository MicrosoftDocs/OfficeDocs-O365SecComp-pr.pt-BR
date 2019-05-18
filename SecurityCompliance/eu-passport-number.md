---
title: Número do Passport da UE
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/16/2018
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: Este tópico mostra o que uma política de prevenção de perda de dados (DLP) procura quando detecta o tipo de informação confidencial do número do Passport da UE. Esse tipo de informação confidencial define diferentes padrões, palavras-chave e outras evidências para cada país.
ms.openlocfilehash: fa3be04dec0f71a2568e046abd6b0af3e20181c5
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34152963"
---
# <a name="eu-passport-number"></a><span data-ttu-id="bb0c5-104">Número do Passport da UE</span><span class="sxs-lookup"><span data-stu-id="bb0c5-104">EU Passport Number</span></span>

<span data-ttu-id="bb0c5-105">Este tópico mostra o que uma política de prevenção de perda de dados (DLP) procura quando detecta o tipo de informação confidencial do número do Passport da UE.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Passport Number sensitive information type.</span></span> <span data-ttu-id="bb0c5-106">Esse tipo de informação confidencial define diferentes padrões, palavras-chave e outras evidências para cada país.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="bb0c5-107">Áustria </span><span class="sxs-lookup"><span data-stu-id="bb0c5-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="bb0c5-108">Formatar</span><span class="sxs-lookup"><span data-stu-id="bb0c5-108">Format</span></span>

<span data-ttu-id="bb0c5-109">Uma letra seguida de um espaço opcional e sete dígitos</span><span class="sxs-lookup"><span data-stu-id="bb0c5-109">One letter followed by an optional space and seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bb0c5-110">Padrão</span><span class="sxs-lookup"><span data-stu-id="bb0c5-110">Pattern</span></span>

<span data-ttu-id="bb0c5-111">Uma combinação de uma letra, sete dígitos e um espaço:</span><span class="sxs-lookup"><span data-stu-id="bb0c5-111">A combination of one letter, seven digits, and one space:</span></span>
  
- <span data-ttu-id="bb0c5-112">Uma letra (não diferencia maiúscula de minúscula)</span><span class="sxs-lookup"><span data-stu-id="bb0c5-112">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="bb0c5-113">Um espaço (opcional)</span><span class="sxs-lookup"><span data-stu-id="bb0c5-113">One space (optional)</span></span>
    
- <span data-ttu-id="bb0c5-114">Sete dígitos</span><span class="sxs-lookup"><span data-stu-id="bb0c5-114">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="bb0c5-115">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="bb0c5-115">Checksum</span></span>

<span data-ttu-id="bb0c5-116">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="bb0c5-116">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="bb0c5-117">Definição</span><span class="sxs-lookup"><span data-stu-id="bb0c5-117">Definition</span></span>

<span data-ttu-id="bb0c5-118">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="bb0c5-118">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bb0c5-119">A expressão `Regex_austria_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-119">The regular expression  `Regex_austria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bb0c5-120">Uma palavra- `Keywords_austria_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-120">A keyword from  `Keywords_austria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_passport_number" />
          <Match idRef="Keywords_austria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bb0c5-121">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="bb0c5-121">Keywords</span></span>

<span data-ttu-id="bb0c5-122">| |</span><span class="sxs-lookup"><span data-stu-id="bb0c5-122"></span></span>
|<span data-ttu-id="bb0c5-123">**Keywords_austria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="bb0c5-123">**Keywords_austria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="bb0c5-124">passport number</span><span class="sxs-lookup"><span data-stu-id="bb0c5-124">passport number</span></span>  <br/> <span data-ttu-id="bb0c5-125">número de passaporte austríaco</span><span class="sxs-lookup"><span data-stu-id="bb0c5-125">austrian passport number</span></span>  <br/> <span data-ttu-id="bb0c5-126">Passport não</span><span class="sxs-lookup"><span data-stu-id="bb0c5-126">passport no</span></span>  <br/> <span data-ttu-id="bb0c5-127">reisepass</span><span class="sxs-lookup"><span data-stu-id="bb0c5-127">reisepass</span></span>  <br/> <span data-ttu-id="bb0c5-128">österreichisch reisepass</span><span class="sxs-lookup"><span data-stu-id="bb0c5-128">österreichisch reisepass</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="bb0c5-129">Bélgica </span><span class="sxs-lookup"><span data-stu-id="bb0c5-129">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="bb0c5-130">Formatar</span><span class="sxs-lookup"><span data-stu-id="bb0c5-130">Format</span></span>

<span data-ttu-id="bb0c5-131">Duas letras seguidas por seis dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="bb0c5-131">Two letters followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bb0c5-132">Padrão</span><span class="sxs-lookup"><span data-stu-id="bb0c5-132">Pattern</span></span>

<span data-ttu-id="bb0c5-133">Duas letras e seguidas por seis dígitos</span><span class="sxs-lookup"><span data-stu-id="bb0c5-133">Two letters and followed by six digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="bb0c5-134">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="bb0c5-134">Checksum</span></span>

<span data-ttu-id="bb0c5-135">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="bb0c5-135">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="bb0c5-136">Definição</span><span class="sxs-lookup"><span data-stu-id="bb0c5-136">Definition</span></span>

<span data-ttu-id="bb0c5-137">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="bb0c5-137">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bb0c5-138">A expressão `Regex_belgium_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-138">The regular expression  `Regex_belgium_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bb0c5-139">Uma palavra- `Keywords_belgium_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-139">A keyword from  `Keywords_belgium_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium__eu_passport_number" />
          <Match idRef="Keywords_belgium_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bb0c5-140">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="bb0c5-140">Keywords</span></span>

<span data-ttu-id="bb0c5-141">| |</span><span class="sxs-lookup"><span data-stu-id="bb0c5-141"></span></span>
|<span data-ttu-id="bb0c5-142">**Keywords_belgium_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="bb0c5-142">**Keywords_belgium_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="bb0c5-143">passport number</span><span class="sxs-lookup"><span data-stu-id="bb0c5-143">passport number</span></span>  <br/> <span data-ttu-id="bb0c5-144">número de passaporte belga</span><span class="sxs-lookup"><span data-stu-id="bb0c5-144">belgian passport number</span></span>  <br/> <span data-ttu-id="bb0c5-145">Passport não</span><span class="sxs-lookup"><span data-stu-id="bb0c5-145">passport no</span></span>  <br/> <span data-ttu-id="bb0c5-146">paspoort</span><span class="sxs-lookup"><span data-stu-id="bb0c5-146">paspoort</span></span>  <br/> <span data-ttu-id="bb0c5-147">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="bb0c5-147">paspoortnummer</span></span>  <br/> <span data-ttu-id="bb0c5-148">reisepass kein</span><span class="sxs-lookup"><span data-stu-id="bb0c5-148">reisepass kein</span></span>  <br/> <span data-ttu-id="bb0c5-149">reisepass</span><span class="sxs-lookup"><span data-stu-id="bb0c5-149">reisepass</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="bb0c5-150">Bulgária</span><span class="sxs-lookup"><span data-stu-id="bb0c5-150">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="bb0c5-151">Formatar</span><span class="sxs-lookup"><span data-stu-id="bb0c5-151">Format</span></span>

<span data-ttu-id="bb0c5-152">Nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="bb0c5-152">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bb0c5-153">Padrão</span><span class="sxs-lookup"><span data-stu-id="bb0c5-153">Pattern</span></span>

 <span data-ttu-id="bb0c5-154">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="bb0c5-154">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="bb0c5-155">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="bb0c5-155">Checksum</span></span>

<span data-ttu-id="bb0c5-156">Não</span><span class="sxs-lookup"><span data-stu-id="bb0c5-156">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="bb0c5-157">Definição</span><span class="sxs-lookup"><span data-stu-id="bb0c5-157">Definition</span></span>

<span data-ttu-id="bb0c5-158">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="bb0c5-158">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bb0c5-159">A expressão `Regex_bulgaria_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-159">The regular expression  `Regex_bulgaria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bb0c5-160">Uma palavra- `Keywords_bulgaria_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-160">A keyword from  `Keywords_bulgaria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_passport_number" />
          <Match idRef="Keywords_bulgaria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bb0c5-161">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="bb0c5-161">Keywords</span></span>

<span data-ttu-id="bb0c5-162">| |</span><span class="sxs-lookup"><span data-stu-id="bb0c5-162"></span></span>
|<span data-ttu-id="bb0c5-163">**Keywords_bulgaria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="bb0c5-163">**Keywords_bulgaria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="bb0c5-164">passport number</span><span class="sxs-lookup"><span data-stu-id="bb0c5-164">passport number</span></span>  <br/> <span data-ttu-id="bb0c5-165">número de passaporte búlgaro</span><span class="sxs-lookup"><span data-stu-id="bb0c5-165">bulgarian passport number</span></span>  <br/> <span data-ttu-id="bb0c5-166">Passport não</span><span class="sxs-lookup"><span data-stu-id="bb0c5-166">passport no</span></span>  <br/> <span data-ttu-id="bb0c5-167">номер на паспорта</span><span class="sxs-lookup"><span data-stu-id="bb0c5-167">номер на паспорта</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="bb0c5-168">Croácia</span><span class="sxs-lookup"><span data-stu-id="bb0c5-168">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="bb0c5-169">Formatar</span><span class="sxs-lookup"><span data-stu-id="bb0c5-169">Format</span></span>

<span data-ttu-id="bb0c5-170">Nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="bb0c5-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bb0c5-171">Padrão</span><span class="sxs-lookup"><span data-stu-id="bb0c5-171">Pattern</span></span>

 <span data-ttu-id="bb0c5-172">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="bb0c5-172">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="bb0c5-173">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="bb0c5-173">Checksum</span></span>

<span data-ttu-id="bb0c5-174">Não</span><span class="sxs-lookup"><span data-stu-id="bb0c5-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="bb0c5-175">Definição</span><span class="sxs-lookup"><span data-stu-id="bb0c5-175">Definition</span></span>

<span data-ttu-id="bb0c5-176">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="bb0c5-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bb0c5-177">A expressão `Regex_croatia_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-177">The regular expression  `Regex_croatia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bb0c5-178">Uma palavra- `Keywords_croatia_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-178">A keyword from  `Keywords_croatia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_passport_number" />
          <Match idRef="Keywords_croatia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bb0c5-179">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="bb0c5-179">Keywords</span></span>

<span data-ttu-id="bb0c5-180">| |</span><span class="sxs-lookup"><span data-stu-id="bb0c5-180"></span></span>
|<span data-ttu-id="bb0c5-181">**Keywords_croatia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="bb0c5-181">**Keywords_croatia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="bb0c5-182">passport number</span><span class="sxs-lookup"><span data-stu-id="bb0c5-182">passport number</span></span>  <br/> <span data-ttu-id="bb0c5-183">número de passaporte Croata</span><span class="sxs-lookup"><span data-stu-id="bb0c5-183">croatian passport number</span></span>  <br/> <span data-ttu-id="bb0c5-184">Passport não</span><span class="sxs-lookup"><span data-stu-id="bb0c5-184">passport no</span></span>  <br/> <span data-ttu-id="bb0c5-185">broj putovnice</span><span class="sxs-lookup"><span data-stu-id="bb0c5-185">broj putovnice</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="bb0c5-186">Chipre</span><span class="sxs-lookup"><span data-stu-id="bb0c5-186">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="bb0c5-187">Formatar</span><span class="sxs-lookup"><span data-stu-id="bb0c5-187">Format</span></span>

<span data-ttu-id="bb0c5-188">Uma letra seguida de 6-8 dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="bb0c5-188">One letter followed by 6-8 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bb0c5-189">Padrão</span><span class="sxs-lookup"><span data-stu-id="bb0c5-189">Pattern</span></span>

<span data-ttu-id="bb0c5-190">Uma letra seguida de seis a oito dígitos</span><span class="sxs-lookup"><span data-stu-id="bb0c5-190">One letter followed by six to eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="bb0c5-191">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="bb0c5-191">Checksum</span></span>

<span data-ttu-id="bb0c5-192">Não</span><span class="sxs-lookup"><span data-stu-id="bb0c5-192">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="bb0c5-193">Definição</span><span class="sxs-lookup"><span data-stu-id="bb0c5-193">Definition</span></span>

<span data-ttu-id="bb0c5-194">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="bb0c5-194">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bb0c5-195">A expressão `Regex_cyprus_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-195">The regular expression  `Regex_cyprus_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bb0c5-196">Uma palavra- `Keywords_cyprus_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-196">A keyword from  `Keywords_cyprus_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_passport_number" />
          <Match idRef="Keywords_cyprus_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bb0c5-197">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="bb0c5-197">Keywords</span></span>

<span data-ttu-id="bb0c5-198">| |</span><span class="sxs-lookup"><span data-stu-id="bb0c5-198"></span></span>
|<span data-ttu-id="bb0c5-199">**Keywords_cyprus_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="bb0c5-199">**Keywords_cyprus_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="bb0c5-200">passport number</span><span class="sxs-lookup"><span data-stu-id="bb0c5-200">passport number</span></span>  <br/> <span data-ttu-id="bb0c5-201">número de passaporte do Chipre</span><span class="sxs-lookup"><span data-stu-id="bb0c5-201">cyprus passport number</span></span>  <br/> <span data-ttu-id="bb0c5-202">Passport não</span><span class="sxs-lookup"><span data-stu-id="bb0c5-202">passport no</span></span>  <br/> <span data-ttu-id="bb0c5-203">αριθμό διαβατηρίου</span><span class="sxs-lookup"><span data-stu-id="bb0c5-203">αριθμό διαβατηρίου</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="bb0c5-204">República Tcheca</span><span class="sxs-lookup"><span data-stu-id="bb0c5-204">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="bb0c5-205">Formatar</span><span class="sxs-lookup"><span data-stu-id="bb0c5-205">Format</span></span>

<span data-ttu-id="bb0c5-206">Oito dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="bb0c5-206">Eight digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bb0c5-207">Padrão</span><span class="sxs-lookup"><span data-stu-id="bb0c5-207">Pattern</span></span>

<span data-ttu-id="bb0c5-208">Oito dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="bb0c5-208">Eight digits without spaces or delimiters</span></span>
  
### <a name="checksum"></a><span data-ttu-id="bb0c5-209">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="bb0c5-209">Checksum</span></span>

<span data-ttu-id="bb0c5-210">Não</span><span class="sxs-lookup"><span data-stu-id="bb0c5-210">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="bb0c5-211">Definição</span><span class="sxs-lookup"><span data-stu-id="bb0c5-211">Definition</span></span>

<span data-ttu-id="bb0c5-212">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="bb0c5-212">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bb0c5-213">A expressão `Regex_czech_republic_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-213">The regular expression  `Regex_czech_republic_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bb0c5-214">Uma palavra- `Keywords_czech_republic_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-214">A keyword from  `Keywords_czech_republic_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_passport_number" />
          <Match idRef="Keywords_czech_republic_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bb0c5-215">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="bb0c5-215">Keywords</span></span>

<span data-ttu-id="bb0c5-216">| |</span><span class="sxs-lookup"><span data-stu-id="bb0c5-216"></span></span>
|<span data-ttu-id="bb0c5-217">**Keywords_czech_republic_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="bb0c5-217">**Keywords_czech_republic_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="bb0c5-218">passport number</span><span class="sxs-lookup"><span data-stu-id="bb0c5-218">passport number</span></span>  <br/> <span data-ttu-id="bb0c5-219">número de passaporte tcheco</span><span class="sxs-lookup"><span data-stu-id="bb0c5-219">czech passport number</span></span>  <br/> <span data-ttu-id="bb0c5-220">Passport não</span><span class="sxs-lookup"><span data-stu-id="bb0c5-220">passport no</span></span>  <br/> <span data-ttu-id="bb0c5-221">Pas cestovní</span><span class="sxs-lookup"><span data-stu-id="bb0c5-221">cestovní pas</span></span>  <br/> <span data-ttu-id="bb0c5-222">Pas</span><span class="sxs-lookup"><span data-stu-id="bb0c5-222">pas</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="bb0c5-223">Dinamarca</span><span class="sxs-lookup"><span data-stu-id="bb0c5-223">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="bb0c5-224">Formatar</span><span class="sxs-lookup"><span data-stu-id="bb0c5-224">Format</span></span>

<span data-ttu-id="bb0c5-225">Nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="bb0c5-225">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bb0c5-226">Padrão</span><span class="sxs-lookup"><span data-stu-id="bb0c5-226">Pattern</span></span>

 <span data-ttu-id="bb0c5-227">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="bb0c5-227">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="bb0c5-228">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="bb0c5-228">Checksum</span></span>

<span data-ttu-id="bb0c5-229">Não</span><span class="sxs-lookup"><span data-stu-id="bb0c5-229">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="bb0c5-230">Definição</span><span class="sxs-lookup"><span data-stu-id="bb0c5-230">Definition</span></span>

<span data-ttu-id="bb0c5-231">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="bb0c5-231">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bb0c5-232">A expressão `Regex_denmark_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-232">The regular expression  `Regex_denmark_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bb0c5-233">Uma palavra- `Keywords_denmark_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-233">A keyword from  `Keywords_denmark_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_passport_number" />
          <Match idRef="Keywords_denmark_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bb0c5-234">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="bb0c5-234">Keywords</span></span>

<span data-ttu-id="bb0c5-235">| |</span><span class="sxs-lookup"><span data-stu-id="bb0c5-235"></span></span>
|<span data-ttu-id="bb0c5-236">**Keywords_denmark_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="bb0c5-236">**Keywords_denmark_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="bb0c5-237">passport number</span><span class="sxs-lookup"><span data-stu-id="bb0c5-237">passport number</span></span>  <br/> <span data-ttu-id="bb0c5-238">número de passaporte dinamarquês</span><span class="sxs-lookup"><span data-stu-id="bb0c5-238">danish passport number</span></span>  <br/> <span data-ttu-id="bb0c5-239">Passport não</span><span class="sxs-lookup"><span data-stu-id="bb0c5-239">passport no</span></span>  <br/> <span data-ttu-id="bb0c5-240">Pas</span><span class="sxs-lookup"><span data-stu-id="bb0c5-240">pas</span></span>  <br/> <span data-ttu-id="bb0c5-241">pasnummer</span><span class="sxs-lookup"><span data-stu-id="bb0c5-241">pasnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="bb0c5-242">Estônia</span><span class="sxs-lookup"><span data-stu-id="bb0c5-242">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="bb0c5-243">Formatar</span><span class="sxs-lookup"><span data-stu-id="bb0c5-243">Format</span></span>

<span data-ttu-id="bb0c5-244">Uma letra seguida por sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="bb0c5-244">One letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bb0c5-245">Padrão</span><span class="sxs-lookup"><span data-stu-id="bb0c5-245">Pattern</span></span>

<span data-ttu-id="bb0c5-246">Uma letra seguida por sete dígitos</span><span class="sxs-lookup"><span data-stu-id="bb0c5-246">One letter followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="bb0c5-247">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="bb0c5-247">Checksum</span></span>

<span data-ttu-id="bb0c5-248">Não</span><span class="sxs-lookup"><span data-stu-id="bb0c5-248">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="bb0c5-249">Definição</span><span class="sxs-lookup"><span data-stu-id="bb0c5-249">Definition</span></span>

<span data-ttu-id="bb0c5-250">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="bb0c5-250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bb0c5-251">A expressão `Regex_estonia_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-251">The regular expression  `Regex_estonia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bb0c5-252">Uma palavra- `Keywords_estonia_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-252">A keyword from  `Keywords_estonia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_passport_number" />
          <Match idRef="Keywords_estonia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bb0c5-253">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="bb0c5-253">Keywords</span></span>

<span data-ttu-id="bb0c5-254">| |</span><span class="sxs-lookup"><span data-stu-id="bb0c5-254"></span></span>
|<span data-ttu-id="bb0c5-255">**Keywords_estonia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="bb0c5-255">**Keywords_estonia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="bb0c5-256">passport number</span><span class="sxs-lookup"><span data-stu-id="bb0c5-256">passport number</span></span>  <br/> <span data-ttu-id="bb0c5-257">número de passaporte estoniano</span><span class="sxs-lookup"><span data-stu-id="bb0c5-257">estonian passport number</span></span>  <br/> <span data-ttu-id="bb0c5-258">Passport não</span><span class="sxs-lookup"><span data-stu-id="bb0c5-258">passport no</span></span>  <br/> <span data-ttu-id="bb0c5-259">Eesti kodaniku</span><span class="sxs-lookup"><span data-stu-id="bb0c5-259">eesti kodaniku pass</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="bb0c5-260">Finlândia</span><span class="sxs-lookup"><span data-stu-id="bb0c5-260">Finland</span></span>

<span data-ttu-id="bb0c5-261">Para obter detalhes, consulte a seção "número de passaporte da Finlândia" em [o que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="bb0c5-261">For details, see the section "Finland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="bb0c5-262">França</span><span class="sxs-lookup"><span data-stu-id="bb0c5-262">France</span></span>

<span data-ttu-id="bb0c5-263">Para obter detalhes, consulte a seção "número do passaporte da França" em [o que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="bb0c5-263">For details, see the section "France Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="bb0c5-264">Alemanha</span><span class="sxs-lookup"><span data-stu-id="bb0c5-264">Germany</span></span>

<span data-ttu-id="bb0c5-265">Para obter detalhes, consulte a seção "número de passaporte da Alemanha" em [o que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="bb0c5-265">For details, see the section "Germany Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="bb0c5-266">Grécia</span><span class="sxs-lookup"><span data-stu-id="bb0c5-266">Greece</span></span>

### <a name="format"></a><span data-ttu-id="bb0c5-267">Formatar</span><span class="sxs-lookup"><span data-stu-id="bb0c5-267">Format</span></span>

<span data-ttu-id="bb0c5-268">Duas letras seguidas por sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="bb0c5-268">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bb0c5-269">Padrão</span><span class="sxs-lookup"><span data-stu-id="bb0c5-269">Pattern</span></span>

<span data-ttu-id="bb0c5-270">Duas letras seguidas por sete dígitos</span><span class="sxs-lookup"><span data-stu-id="bb0c5-270">Two letters followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="bb0c5-271">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="bb0c5-271">Checksum</span></span>

<span data-ttu-id="bb0c5-272">Não</span><span class="sxs-lookup"><span data-stu-id="bb0c5-272">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="bb0c5-273">Definição</span><span class="sxs-lookup"><span data-stu-id="bb0c5-273">Definition</span></span>

<span data-ttu-id="bb0c5-274">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="bb0c5-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bb0c5-275">A expressão `Regex_greece_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-275">The regular expression  `Regex_greece_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bb0c5-276">Uma palavra- `Keywords_greece_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-276">A keyword from  `Keywords_greece_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_passport_number" />
          <Match idRef="Keywords_greece_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bb0c5-277">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="bb0c5-277">Keywords</span></span>

<span data-ttu-id="bb0c5-278">| |</span><span class="sxs-lookup"><span data-stu-id="bb0c5-278"></span></span>
|<span data-ttu-id="bb0c5-279">**Keywords_greece_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="bb0c5-279">**Keywords_greece_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="bb0c5-280">passport number</span><span class="sxs-lookup"><span data-stu-id="bb0c5-280">passport number</span></span>  <br/> <span data-ttu-id="bb0c5-281">número de passaporte grego</span><span class="sxs-lookup"><span data-stu-id="bb0c5-281">greek passport number</span></span>  <br/> <span data-ttu-id="bb0c5-282">Passport não</span><span class="sxs-lookup"><span data-stu-id="bb0c5-282">passport no</span></span>  <br/> <span data-ttu-id="bb0c5-283">διαβατηριο</span><span class="sxs-lookup"><span data-stu-id="bb0c5-283">διαβατηριο</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="bb0c5-284">Hungria</span><span class="sxs-lookup"><span data-stu-id="bb0c5-284">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="bb0c5-285">Formatar</span><span class="sxs-lookup"><span data-stu-id="bb0c5-285">Format</span></span>

<span data-ttu-id="bb0c5-286">Duas letras seguidas por seis ou sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="bb0c5-286">Two letters followed by six or seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bb0c5-287">Padrão</span><span class="sxs-lookup"><span data-stu-id="bb0c5-287">Pattern</span></span>

<span data-ttu-id="bb0c5-288">Duas letras seguidas por seis ou sete dígitos</span><span class="sxs-lookup"><span data-stu-id="bb0c5-288">Two letters followed by six or seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="bb0c5-289">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="bb0c5-289">Checksum</span></span>

<span data-ttu-id="bb0c5-290">Não</span><span class="sxs-lookup"><span data-stu-id="bb0c5-290">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="bb0c5-291">Definição</span><span class="sxs-lookup"><span data-stu-id="bb0c5-291">Definition</span></span>

<span data-ttu-id="bb0c5-292">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="bb0c5-292">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bb0c5-293">A expressão `Regex_hungary_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-293">The regular expression  `Regex_hungary_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bb0c5-294">Uma palavra- `Keywords_hungary_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-294">A keyword from  `Keywords_hungary_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_passport_number" />
          <Match idRef="Keywords_hungary_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bb0c5-295">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="bb0c5-295">Keywords</span></span>

<span data-ttu-id="bb0c5-296">| |</span><span class="sxs-lookup"><span data-stu-id="bb0c5-296"></span></span>
|<span data-ttu-id="bb0c5-297">**Keywords_hungary_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="bb0c5-297">**Keywords_hungary_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="bb0c5-298">passport number</span><span class="sxs-lookup"><span data-stu-id="bb0c5-298">passport number</span></span>  <br/> <span data-ttu-id="bb0c5-299">número de passaporte húngaro</span><span class="sxs-lookup"><span data-stu-id="bb0c5-299">hungarian passport number</span></span>  <br/> <span data-ttu-id="bb0c5-300">Passport não</span><span class="sxs-lookup"><span data-stu-id="bb0c5-300">passport no</span></span>  <br/> <span data-ttu-id="bb0c5-301">útlevél száma</span><span class="sxs-lookup"><span data-stu-id="bb0c5-301">útlevél száma</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="bb0c5-302">Irlanda</span><span class="sxs-lookup"><span data-stu-id="bb0c5-302">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="bb0c5-303">Formatar</span><span class="sxs-lookup"><span data-stu-id="bb0c5-303">Format</span></span>

<span data-ttu-id="bb0c5-304">Duas letras ou dígitos seguidos de sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="bb0c5-304">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bb0c5-305">Padrão</span><span class="sxs-lookup"><span data-stu-id="bb0c5-305">Pattern</span></span>

<span data-ttu-id="bb0c5-306">Duas letras ou dígitos seguidos por sete dígitos:</span><span class="sxs-lookup"><span data-stu-id="bb0c5-306">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="bb0c5-307">Dois dígitos ou letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="bb0c5-307">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="bb0c5-308">Sete dígitos</span><span class="sxs-lookup"><span data-stu-id="bb0c5-308">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="bb0c5-309">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="bb0c5-309">Checksum</span></span>

<span data-ttu-id="bb0c5-310">Não</span><span class="sxs-lookup"><span data-stu-id="bb0c5-310">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="bb0c5-311">Definição</span><span class="sxs-lookup"><span data-stu-id="bb0c5-311">Definition</span></span>

<span data-ttu-id="bb0c5-312">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="bb0c5-312">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bb0c5-313">A expressão `Regex_ireland_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-313">The regular expression  `Regex_ireland_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bb0c5-314">Uma palavra- `Keywords_ireland_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-314">A keyword from  `Keywords_ireland_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_passport_number" />
          <Match idRef="Keywords_ireland_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bb0c5-315">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="bb0c5-315">Keywords</span></span>

<span data-ttu-id="bb0c5-316">| |</span><span class="sxs-lookup"><span data-stu-id="bb0c5-316"></span></span>
|<span data-ttu-id="bb0c5-317">**Keywords_ireland_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="bb0c5-317">**Keywords_ireland_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="bb0c5-318">passport number</span><span class="sxs-lookup"><span data-stu-id="bb0c5-318">passport number</span></span>  <br/> <span data-ttu-id="bb0c5-319">número de passaporte do irlandês</span><span class="sxs-lookup"><span data-stu-id="bb0c5-319">irish passport number</span></span>  <br/> <span data-ttu-id="bb0c5-320">Passport não</span><span class="sxs-lookup"><span data-stu-id="bb0c5-320">passport no</span></span>  <br/> <span data-ttu-id="bb0c5-321">Pas</span><span class="sxs-lookup"><span data-stu-id="bb0c5-321">pas</span></span>  <br/> <span data-ttu-id="bb0c5-322">Passaport</span><span class="sxs-lookup"><span data-stu-id="bb0c5-322">passport</span></span>  <br/> <span data-ttu-id="bb0c5-323">passeport</span><span class="sxs-lookup"><span data-stu-id="bb0c5-323">passeport</span></span>  <br/> <span data-ttu-id="bb0c5-324">passeport numero</span><span class="sxs-lookup"><span data-stu-id="bb0c5-324">passeport numero</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="bb0c5-325">Itália</span><span class="sxs-lookup"><span data-stu-id="bb0c5-325">Italy</span></span>

### <a name="format"></a><span data-ttu-id="bb0c5-326">Formatar</span><span class="sxs-lookup"><span data-stu-id="bb0c5-326">Format</span></span>

<span data-ttu-id="bb0c5-327">Duas letras ou dígitos seguidos de sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="bb0c5-327">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bb0c5-328">Padrão</span><span class="sxs-lookup"><span data-stu-id="bb0c5-328">Pattern</span></span>

<span data-ttu-id="bb0c5-329">Duas letras ou dígitos seguidos por sete dígitos:</span><span class="sxs-lookup"><span data-stu-id="bb0c5-329">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="bb0c5-330">Dois dígitos ou letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="bb0c5-330">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="bb0c5-331">Sete dígitos</span><span class="sxs-lookup"><span data-stu-id="bb0c5-331">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="bb0c5-332">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="bb0c5-332">Checksum</span></span>

<span data-ttu-id="bb0c5-333">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="bb0c5-333">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="bb0c5-334">Definição</span><span class="sxs-lookup"><span data-stu-id="bb0c5-334">Definition</span></span>

<span data-ttu-id="bb0c5-335">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="bb0c5-335">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bb0c5-336">A expressão `Regex_italy_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-336">The regular expression  `Regex_italy_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bb0c5-337">Uma palavra- `Keywords_italy_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-337">A keyword from  `Keywords_italy_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_passport_number" />
          <Match idRef="Keywords_italy_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bb0c5-338">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="bb0c5-338">Keywords</span></span>

<span data-ttu-id="bb0c5-339">| |</span><span class="sxs-lookup"><span data-stu-id="bb0c5-339"></span></span>
|<span data-ttu-id="bb0c5-340">**Keywords_italy_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="bb0c5-340">**Keywords_italy_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="bb0c5-341">número de passaporte italiano</span><span class="sxs-lookup"><span data-stu-id="bb0c5-341">italian passport number</span></span>  <br/> <span data-ttu-id="bb0c5-342">repubblica italiana passaporto</span><span class="sxs-lookup"><span data-stu-id="bb0c5-342">repubblica italiana passaporto</span></span>  <br/> <span data-ttu-id="bb0c5-343">passaporto</span><span class="sxs-lookup"><span data-stu-id="bb0c5-343">passaporto</span></span>  <br/> <span data-ttu-id="bb0c5-344">passaporto italiana</span><span class="sxs-lookup"><span data-stu-id="bb0c5-344">passaporto italiana</span></span>  <br/> <span data-ttu-id="bb0c5-345">passport number</span><span class="sxs-lookup"><span data-stu-id="bb0c5-345">passport number</span></span>  <br/> <span data-ttu-id="bb0c5-346">italiana passaporto numero</span><span class="sxs-lookup"><span data-stu-id="bb0c5-346">italiana passaporto numero</span></span>  <br/> <span data-ttu-id="bb0c5-347">passaporto numero</span><span class="sxs-lookup"><span data-stu-id="bb0c5-347">passaporto numero</span></span>  <br/> <span data-ttu-id="bb0c5-348">numéro passeport italien</span><span class="sxs-lookup"><span data-stu-id="bb0c5-348">numéro passeport italien</span></span>  <br/> <span data-ttu-id="bb0c5-349">numéro passeport</span><span class="sxs-lookup"><span data-stu-id="bb0c5-349">numéro passeport</span></span>  <br/> |
   
## <a name="latvia"></a><span data-ttu-id="bb0c5-350">Letônia</span><span class="sxs-lookup"><span data-stu-id="bb0c5-350">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="bb0c5-351">Formatar</span><span class="sxs-lookup"><span data-stu-id="bb0c5-351">Format</span></span>

<span data-ttu-id="bb0c5-352">Duas letras ou dígitos seguidos de sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="bb0c5-352">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bb0c5-353">Padrão</span><span class="sxs-lookup"><span data-stu-id="bb0c5-353">Pattern</span></span>

<span data-ttu-id="bb0c5-354">Duas letras ou dígitos seguidos por sete dígitos:</span><span class="sxs-lookup"><span data-stu-id="bb0c5-354">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="bb0c5-355">Dois dígitos ou letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="bb0c5-355">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="bb0c5-356">Sete dígitos</span><span class="sxs-lookup"><span data-stu-id="bb0c5-356">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="bb0c5-357">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="bb0c5-357">Checksum</span></span>

<span data-ttu-id="bb0c5-358">Não</span><span class="sxs-lookup"><span data-stu-id="bb0c5-358">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="bb0c5-359">Definição</span><span class="sxs-lookup"><span data-stu-id="bb0c5-359">Definition</span></span>

<span data-ttu-id="bb0c5-360">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="bb0c5-360">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bb0c5-361">A expressão `Regex_latvia_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-361">The regular expression  `Regex_latvia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bb0c5-362">Uma palavra- `Keywords_latvia_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-362">A keyword from  `Keywords_latvia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_passport_number" />
          <Match idRef="Keywords_latvia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bb0c5-363">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="bb0c5-363">Keywords</span></span>

<span data-ttu-id="bb0c5-364">| |</span><span class="sxs-lookup"><span data-stu-id="bb0c5-364"></span></span>
|<span data-ttu-id="bb0c5-365">**Keywords_latvia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="bb0c5-365">**Keywords_latvia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="bb0c5-366">passport number</span><span class="sxs-lookup"><span data-stu-id="bb0c5-366">passport number</span></span>  <br/> <span data-ttu-id="bb0c5-367">número de passaporte da Letão</span><span class="sxs-lookup"><span data-stu-id="bb0c5-367">latvian passport number</span></span>  <br/> <span data-ttu-id="bb0c5-368">Passport não</span><span class="sxs-lookup"><span data-stu-id="bb0c5-368">passport no</span></span>  <br/> <span data-ttu-id="bb0c5-369">pase numurs</span><span class="sxs-lookup"><span data-stu-id="bb0c5-369">pase numurs</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="bb0c5-370">Lituânia</span><span class="sxs-lookup"><span data-stu-id="bb0c5-370">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="bb0c5-371">Formatar</span><span class="sxs-lookup"><span data-stu-id="bb0c5-371">Format</span></span>

<span data-ttu-id="bb0c5-372">Oito dígitos ou letras sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="bb0c5-372">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bb0c5-373">Padrão</span><span class="sxs-lookup"><span data-stu-id="bb0c5-373">Pattern</span></span>

<span data-ttu-id="bb0c5-374">Oito dígitos ou letras (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="bb0c5-374">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="bb0c5-375">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="bb0c5-375">Checksum</span></span>

<span data-ttu-id="bb0c5-376">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="bb0c5-376">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="bb0c5-377">Definição</span><span class="sxs-lookup"><span data-stu-id="bb0c5-377">Definition</span></span>

<span data-ttu-id="bb0c5-378">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="bb0c5-378">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bb0c5-379">A expressão `Regex_lithuania_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-379">The regular expression  `Regex_lithuania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bb0c5-380">Uma palavra- `Keywords_lithuania_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-380">A keyword from  `Keywords_lithuania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_passport_number" />
          <Match idRef="Keywords_lithuania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bb0c5-381">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="bb0c5-381">Keywords</span></span>

<span data-ttu-id="bb0c5-382">| |</span><span class="sxs-lookup"><span data-stu-id="bb0c5-382"></span></span>
|<span data-ttu-id="bb0c5-383">**Keywords_lithuania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="bb0c5-383">**Keywords_lithuania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="bb0c5-384">passport number</span><span class="sxs-lookup"><span data-stu-id="bb0c5-384">passport number</span></span>  <br/> <span data-ttu-id="bb0c5-385">número de passaporte lithunian</span><span class="sxs-lookup"><span data-stu-id="bb0c5-385">lithunian passport number</span></span>  <br/> <span data-ttu-id="bb0c5-386">Passport não</span><span class="sxs-lookup"><span data-stu-id="bb0c5-386">passport no</span></span>  <br/> <span data-ttu-id="bb0c5-387">paso numeris</span><span class="sxs-lookup"><span data-stu-id="bb0c5-387">paso numeris</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="bb0c5-388">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="bb0c5-388">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="bb0c5-389">Formatar</span><span class="sxs-lookup"><span data-stu-id="bb0c5-389">Format</span></span>

<span data-ttu-id="bb0c5-390">Oito dígitos ou letras sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="bb0c5-390">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bb0c5-391">Padrão</span><span class="sxs-lookup"><span data-stu-id="bb0c5-391">Pattern</span></span>

<span data-ttu-id="bb0c5-392">Oito dígitos ou letras (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="bb0c5-392">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="bb0c5-393">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="bb0c5-393">Checksum</span></span>

<span data-ttu-id="bb0c5-394">Não</span><span class="sxs-lookup"><span data-stu-id="bb0c5-394">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="bb0c5-395">Definição</span><span class="sxs-lookup"><span data-stu-id="bb0c5-395">Definition</span></span>

<span data-ttu-id="bb0c5-396">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="bb0c5-396">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bb0c5-397">A expressão `Regex_nation_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-397">The regular expression  `Regex_nation_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bb0c5-398">Uma palavra- `Keywords_nation_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-398">A keyword from  `Keywords_nation_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_nation_eu_passport_number" />
          <Match idRef="Keywords_nation_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bb0c5-399">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="bb0c5-399">Keywords</span></span>

<span data-ttu-id="bb0c5-400">| |</span><span class="sxs-lookup"><span data-stu-id="bb0c5-400"></span></span>
|<span data-ttu-id="bb0c5-401">**Keywords_nation_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="bb0c5-401">**Keywords_nation_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="bb0c5-402">passport number</span><span class="sxs-lookup"><span data-stu-id="bb0c5-402">passport number</span></span>  <br/> <span data-ttu-id="bb0c5-403">número de passaporte da Letão</span><span class="sxs-lookup"><span data-stu-id="bb0c5-403">latvian passport number</span></span>  <br/> <span data-ttu-id="bb0c5-404">Passport não</span><span class="sxs-lookup"><span data-stu-id="bb0c5-404">passport no</span></span>  <br/> <span data-ttu-id="bb0c5-405">passnummer</span><span class="sxs-lookup"><span data-stu-id="bb0c5-405">passnummer</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="bb0c5-406">Malta</span><span class="sxs-lookup"><span data-stu-id="bb0c5-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="bb0c5-407">Formatar</span><span class="sxs-lookup"><span data-stu-id="bb0c5-407">Format</span></span>

<span data-ttu-id="bb0c5-408">Sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="bb0c5-408">Seven digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bb0c5-409">Padrão</span><span class="sxs-lookup"><span data-stu-id="bb0c5-409">Pattern</span></span>

 <span data-ttu-id="bb0c5-410">Sete dígitos</span><span class="sxs-lookup"><span data-stu-id="bb0c5-410">Seven digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="bb0c5-411">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="bb0c5-411">Checksum</span></span>

<span data-ttu-id="bb0c5-412">Não</span><span class="sxs-lookup"><span data-stu-id="bb0c5-412">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="bb0c5-413">Definição</span><span class="sxs-lookup"><span data-stu-id="bb0c5-413">Definition</span></span>

<span data-ttu-id="bb0c5-414">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="bb0c5-414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bb0c5-415">A expressão `Regex_malta_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-415">The regular expression  `Regex_malta_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bb0c5-416">Uma palavra- `Keywords_malta_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-416">A keyword from  `Keywords_malta_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_passport_number" />
          <Match idRef="Keywords_malta_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bb0c5-417">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="bb0c5-417">Keywords</span></span>

<span data-ttu-id="bb0c5-418">| |</span><span class="sxs-lookup"><span data-stu-id="bb0c5-418"></span></span>
|<span data-ttu-id="bb0c5-419">**Keywords_malta_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="bb0c5-419">**Keywords_malta_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="bb0c5-420">passport number</span><span class="sxs-lookup"><span data-stu-id="bb0c5-420">passport number</span></span>  <br/> <span data-ttu-id="bb0c5-421">número de passaporte Maltês</span><span class="sxs-lookup"><span data-stu-id="bb0c5-421">maltese passport number</span></span>  <br/> <span data-ttu-id="bb0c5-422">Passport não</span><span class="sxs-lookup"><span data-stu-id="bb0c5-422">passport no</span></span>  <br/> <span data-ttu-id="bb0c5-423">numru tal-passaport</span><span class="sxs-lookup"><span data-stu-id="bb0c5-423">numru tal-passaport</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="bb0c5-424">Países Baixos</span><span class="sxs-lookup"><span data-stu-id="bb0c5-424">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="bb0c5-425">Formatar</span><span class="sxs-lookup"><span data-stu-id="bb0c5-425">Format</span></span>

<span data-ttu-id="bb0c5-426">Nove letras ou dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="bb0c5-426">Nine letters or digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bb0c5-427">Padrão</span><span class="sxs-lookup"><span data-stu-id="bb0c5-427">Pattern</span></span>

<span data-ttu-id="bb0c5-428">Nove letras ou dígitos</span><span class="sxs-lookup"><span data-stu-id="bb0c5-428">Nine letters or digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="bb0c5-429">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="bb0c5-429">Checksum</span></span>

<span data-ttu-id="bb0c5-430">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="bb0c5-430">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="bb0c5-431">Definição</span><span class="sxs-lookup"><span data-stu-id="bb0c5-431">Definition</span></span>

<span data-ttu-id="bb0c5-432">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="bb0c5-432">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bb0c5-433">A expressão `Regex_netherlands_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-433">The regular expression  `Regex_netherlands_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bb0c5-434">Uma palavra- `Keywords_netherlands_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-434">A keyword from  `Keywords_netherlands_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_passport_number" />
          <Match idRef="Keywords_netherlands_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bb0c5-435">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="bb0c5-435">Keywords</span></span>

<span data-ttu-id="bb0c5-436">| |</span><span class="sxs-lookup"><span data-stu-id="bb0c5-436"></span></span>
|<span data-ttu-id="bb0c5-437">**Keywords_netherlands_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="bb0c5-437">**Keywords_netherlands_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="bb0c5-438">número de passaporte holandês</span><span class="sxs-lookup"><span data-stu-id="bb0c5-438">dutch passport number</span></span>  <br/> <span data-ttu-id="bb0c5-439">passport number</span><span class="sxs-lookup"><span data-stu-id="bb0c5-439">passport number</span></span>  <br/> <span data-ttu-id="bb0c5-440">número de passaporte Holanda</span><span class="sxs-lookup"><span data-stu-id="bb0c5-440">netherlands passport number</span></span>  <br/> <span data-ttu-id="bb0c5-441">nederlanden paspoort nummer</span><span class="sxs-lookup"><span data-stu-id="bb0c5-441">nederlanden paspoort nummer</span></span>  <br/> <span data-ttu-id="bb0c5-442">paspoort</span><span class="sxs-lookup"><span data-stu-id="bb0c5-442">paspoort</span></span>  <br/> <span data-ttu-id="bb0c5-443">nederlanden paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="bb0c5-443">nederlanden paspoortnummer</span></span>  <br/> <span data-ttu-id="bb0c5-444">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="bb0c5-444">paspoortnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="bb0c5-445">Polônia</span><span class="sxs-lookup"><span data-stu-id="bb0c5-445">Poland</span></span>

<span data-ttu-id="bb0c5-446">Para obter detalhes, consulte a seção "número de passaporte da Polônia" em [o que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="bb0c5-446">For details, see the section "Poland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="bb0c5-447">Portugal</span><span class="sxs-lookup"><span data-stu-id="bb0c5-447">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="bb0c5-448">Formatar</span><span class="sxs-lookup"><span data-stu-id="bb0c5-448">Format</span></span>

<span data-ttu-id="bb0c5-449">Uma letra seguida de seis dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="bb0c5-449">One letter followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bb0c5-450">Padrão</span><span class="sxs-lookup"><span data-stu-id="bb0c5-450">Pattern</span></span>

<span data-ttu-id="bb0c5-451">Uma letra seguida por seis dígitos:</span><span class="sxs-lookup"><span data-stu-id="bb0c5-451">One letter followed by six digits:</span></span>
  
- <span data-ttu-id="bb0c5-452">Uma letra (não diferencia maiúscula de minúscula)</span><span class="sxs-lookup"><span data-stu-id="bb0c5-452">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="bb0c5-453">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="bb0c5-453">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="bb0c5-454">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="bb0c5-454">Checksum</span></span>

<span data-ttu-id="bb0c5-455">Não</span><span class="sxs-lookup"><span data-stu-id="bb0c5-455">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="bb0c5-456">Definição</span><span class="sxs-lookup"><span data-stu-id="bb0c5-456">Definition</span></span>

<span data-ttu-id="bb0c5-457">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="bb0c5-457">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bb0c5-458">A expressão `Regex_portugal_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-458">The regular expression  `Regex_portugal_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bb0c5-459">Uma palavra- `Keywords_portugal_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-459">A keyword from  `Keywords_portugal_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_passport_number" />
          <Match idRef="Keywords_portugal_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bb0c5-460">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="bb0c5-460">Keywords</span></span>

<span data-ttu-id="bb0c5-461">| |</span><span class="sxs-lookup"><span data-stu-id="bb0c5-461"></span></span>
|<span data-ttu-id="bb0c5-462">**Keywords_portugal_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="bb0c5-462">**Keywords_portugal_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="bb0c5-463">passport number</span><span class="sxs-lookup"><span data-stu-id="bb0c5-463">passport number</span></span>  <br/> <span data-ttu-id="bb0c5-464">número de passaporte Português</span><span class="sxs-lookup"><span data-stu-id="bb0c5-464">portuguese passport number</span></span>  <br/> <span data-ttu-id="bb0c5-465">Passport não</span><span class="sxs-lookup"><span data-stu-id="bb0c5-465">passport no</span></span>  <br/> <span data-ttu-id="bb0c5-466">número do passaporte</span><span class="sxs-lookup"><span data-stu-id="bb0c5-466">número do passaporte</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="bb0c5-467">Romênia</span><span class="sxs-lookup"><span data-stu-id="bb0c5-467">Romania</span></span>

### <a name="format"></a><span data-ttu-id="bb0c5-468">Formatar</span><span class="sxs-lookup"><span data-stu-id="bb0c5-468">Format</span></span>

<span data-ttu-id="bb0c5-469">Oito ou nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="bb0c5-469">Eight or nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bb0c5-470">Padrão</span><span class="sxs-lookup"><span data-stu-id="bb0c5-470">Pattern</span></span>

<span data-ttu-id="bb0c5-471">Oito ou nove dígitos</span><span class="sxs-lookup"><span data-stu-id="bb0c5-471">Eight or nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="bb0c5-472">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="bb0c5-472">Checksum</span></span>

<span data-ttu-id="bb0c5-473">Não</span><span class="sxs-lookup"><span data-stu-id="bb0c5-473">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="bb0c5-474">Definição</span><span class="sxs-lookup"><span data-stu-id="bb0c5-474">Definition</span></span>

<span data-ttu-id="bb0c5-475">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="bb0c5-475">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bb0c5-476">A expressão `Regex_romania_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-476">The regular expression  `Regex_romania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bb0c5-477">Uma palavra- `Keywords_romania_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-477">A keyword from  `Keywords_romania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_passport_number" />
          <Match idRef="Keywords_romania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bb0c5-478">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="bb0c5-478">Keywords</span></span>

<span data-ttu-id="bb0c5-479">| |</span><span class="sxs-lookup"><span data-stu-id="bb0c5-479"></span></span>
|<span data-ttu-id="bb0c5-480">**Keywords_romania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="bb0c5-480">**Keywords_romania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="bb0c5-481">passport number</span><span class="sxs-lookup"><span data-stu-id="bb0c5-481">passport number</span></span>  <br/> <span data-ttu-id="bb0c5-482">número de passaporte romeno</span><span class="sxs-lookup"><span data-stu-id="bb0c5-482">romanian passport number</span></span>  <br/> <span data-ttu-id="bb0c5-483">Passport não</span><span class="sxs-lookup"><span data-stu-id="bb0c5-483">passport no</span></span>  <br/> <span data-ttu-id="bb0c5-484">numărul pașaportului</span><span class="sxs-lookup"><span data-stu-id="bb0c5-484">numărul pașaportului</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="bb0c5-485">Eslováquia</span><span class="sxs-lookup"><span data-stu-id="bb0c5-485">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="bb0c5-486">Formatar</span><span class="sxs-lookup"><span data-stu-id="bb0c5-486">Format</span></span>

<span data-ttu-id="bb0c5-487">Um dígito ou letra seguido por sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="bb0c5-487">One digit or letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bb0c5-488">Padrão</span><span class="sxs-lookup"><span data-stu-id="bb0c5-488">Pattern</span></span>

<span data-ttu-id="bb0c5-489">Um dígito ou letra (não diferencia maiúsculas de minúsculas) seguido por sete dígitos</span><span class="sxs-lookup"><span data-stu-id="bb0c5-489">One digit or letter (not case sensitive) followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="bb0c5-490">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="bb0c5-490">Checksum</span></span>

<span data-ttu-id="bb0c5-491">Não</span><span class="sxs-lookup"><span data-stu-id="bb0c5-491">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="bb0c5-492">Definição</span><span class="sxs-lookup"><span data-stu-id="bb0c5-492">Definition</span></span>

<span data-ttu-id="bb0c5-493">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="bb0c5-493">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bb0c5-494">A expressão `Regex_slovakia_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-494">The regular expression  `Regex_slovakia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bb0c5-495">Uma palavra- `Keywords_slovakia_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-495">A keyword from  `Keywords_slovakia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_passport_number" />
          <Match idRef="Keywords_slovakia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bb0c5-496">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="bb0c5-496">Keywords</span></span>

<span data-ttu-id="bb0c5-497">| |</span><span class="sxs-lookup"><span data-stu-id="bb0c5-497"></span></span>
|<span data-ttu-id="bb0c5-498">**Keywords_slovakia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="bb0c5-498">**Keywords_slovakia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="bb0c5-499">passport number</span><span class="sxs-lookup"><span data-stu-id="bb0c5-499">passport number</span></span>  <br/> <span data-ttu-id="bb0c5-500">número de passaporte eslovaco</span><span class="sxs-lookup"><span data-stu-id="bb0c5-500">slovakian passport number</span></span>  <br/> <span data-ttu-id="bb0c5-501">Passport não</span><span class="sxs-lookup"><span data-stu-id="bb0c5-501">passport no</span></span>  <br/> <span data-ttu-id="bb0c5-502">číslo pasu</span><span class="sxs-lookup"><span data-stu-id="bb0c5-502">číslo pasu</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="bb0c5-503">Eslovênia</span><span class="sxs-lookup"><span data-stu-id="bb0c5-503">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="bb0c5-504">Formatar</span><span class="sxs-lookup"><span data-stu-id="bb0c5-504">Format</span></span>

<span data-ttu-id="bb0c5-505">Duas letras seguidas por sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="bb0c5-505">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bb0c5-506">Padrão</span><span class="sxs-lookup"><span data-stu-id="bb0c5-506">Pattern</span></span>

<span data-ttu-id="bb0c5-507">Duas letras seguidas por sete dígitos:</span><span class="sxs-lookup"><span data-stu-id="bb0c5-507">Two letters followed by seven digits:</span></span>
  
- <span data-ttu-id="bb0c5-508">A letra "P"</span><span class="sxs-lookup"><span data-stu-id="bb0c5-508">The letter "P"</span></span>
    
- <span data-ttu-id="bb0c5-509">Uma letra maiúscula</span><span class="sxs-lookup"><span data-stu-id="bb0c5-509">One uppercase letter</span></span>
    
- <span data-ttu-id="bb0c5-510">Sete dígitos</span><span class="sxs-lookup"><span data-stu-id="bb0c5-510">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="bb0c5-511">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="bb0c5-511">Checksum</span></span>

<span data-ttu-id="bb0c5-512">Não</span><span class="sxs-lookup"><span data-stu-id="bb0c5-512">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="bb0c5-513">Definição</span><span class="sxs-lookup"><span data-stu-id="bb0c5-513">Definition</span></span>

<span data-ttu-id="bb0c5-514">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="bb0c5-514">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bb0c5-515">A expressão `Regex_slovenia_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-515">The regular expression  `Regex_slovenia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bb0c5-516">Uma palavra- `Keywords_slovenia_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-516">A keyword from  `Keywords_slovenia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_passport_number" />
          <Match idRef="Keywords_slovenia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bb0c5-517">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="bb0c5-517">Keywords</span></span>

<span data-ttu-id="bb0c5-518">| |</span><span class="sxs-lookup"><span data-stu-id="bb0c5-518"></span></span>
|<span data-ttu-id="bb0c5-519">**Keywords_slovenia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="bb0c5-519">**Keywords_slovenia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="bb0c5-520">passport number</span><span class="sxs-lookup"><span data-stu-id="bb0c5-520">passport number</span></span>  <br/> <span data-ttu-id="bb0c5-521">número de passaporte esloveno</span><span class="sxs-lookup"><span data-stu-id="bb0c5-521">slovenian passport number</span></span>  <br/> <span data-ttu-id="bb0c5-522">Passport não</span><span class="sxs-lookup"><span data-stu-id="bb0c5-522">passport no</span></span>  <br/> <span data-ttu-id="bb0c5-523">lista de številka potnega</span><span class="sxs-lookup"><span data-stu-id="bb0c5-523">številka potnega lista</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="bb0c5-524">Espanha</span><span class="sxs-lookup"><span data-stu-id="bb0c5-524">Spain</span></span>

### <a name="format"></a><span data-ttu-id="bb0c5-525">Formatar</span><span class="sxs-lookup"><span data-stu-id="bb0c5-525">Format</span></span>

<span data-ttu-id="bb0c5-526">Uma combinação de letras e números de oito ou nove caracteres sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="bb0c5-526">An eight- or nine-character combination of letters and numbers with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bb0c5-527">Padrão</span><span class="sxs-lookup"><span data-stu-id="bb0c5-527">Pattern</span></span>

<span data-ttu-id="bb0c5-528">Uma combinação de letras e números de oito ou nove caracteres:</span><span class="sxs-lookup"><span data-stu-id="bb0c5-528">An eight- or nine-character combination of letters and numbers:</span></span>
  
-  <span data-ttu-id="bb0c5-529">Dois dígitos ou letras</span><span class="sxs-lookup"><span data-stu-id="bb0c5-529">Two digits or letters</span></span> 
    
- <span data-ttu-id="bb0c5-530">Um dígito ou letra (opcional)</span><span class="sxs-lookup"><span data-stu-id="bb0c5-530">One digit or letter (optional)</span></span>
    
- <span data-ttu-id="bb0c5-531">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="bb0c5-531">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="bb0c5-532">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="bb0c5-532">Checksum</span></span>

<span data-ttu-id="bb0c5-533">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="bb0c5-533">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="bb0c5-534">Definição</span><span class="sxs-lookup"><span data-stu-id="bb0c5-534">Definition</span></span>

<span data-ttu-id="bb0c5-535">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="bb0c5-535">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bb0c5-536">A expressão `Regex_spain_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-536">The regular expression  `Regex_spain_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bb0c5-537">Uma palavra- `Keywords_spain_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="bb0c5-537">A keyword from  `Keywords_spain_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_passport_number" />
          <Match idRef="Keywords_spain_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bb0c5-538">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="bb0c5-538">Keywords</span></span>

<span data-ttu-id="bb0c5-539">| |</span><span class="sxs-lookup"><span data-stu-id="bb0c5-539"></span></span>
|<span data-ttu-id="bb0c5-540">**Keywords_spain_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="bb0c5-540">**Keywords_spain_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="bb0c5-541">Passaport</span><span class="sxs-lookup"><span data-stu-id="bb0c5-541">passport</span></span>  <br/> <span data-ttu-id="bb0c5-542">o Passport da Espanha</span><span class="sxs-lookup"><span data-stu-id="bb0c5-542">spain passport</span></span>  <br/> <span data-ttu-id="bb0c5-543">Catálogo do Passport</span><span class="sxs-lookup"><span data-stu-id="bb0c5-543">passport book</span></span>  <br/> <span data-ttu-id="bb0c5-544">passport number</span><span class="sxs-lookup"><span data-stu-id="bb0c5-544">passport number</span></span>  <br/> <span data-ttu-id="bb0c5-545">Passport não</span><span class="sxs-lookup"><span data-stu-id="bb0c5-545">passport no</span></span>  <br/> <span data-ttu-id="bb0c5-546">libreta pasaporte</span><span class="sxs-lookup"><span data-stu-id="bb0c5-546">libreta pasaporte</span></span>  <br/> <span data-ttu-id="bb0c5-547">número pasaporte</span><span class="sxs-lookup"><span data-stu-id="bb0c5-547">número pasaporte</span></span>  <br/> <span data-ttu-id="bb0c5-548">españa pasaporte</span><span class="sxs-lookup"><span data-stu-id="bb0c5-548">españa pasaporte</span></span>  <br/> <span data-ttu-id="bb0c5-549">pasaporte</span><span class="sxs-lookup"><span data-stu-id="bb0c5-549">pasaporte</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="bb0c5-550">Suécia</span><span class="sxs-lookup"><span data-stu-id="bb0c5-550">Sweden</span></span>

<span data-ttu-id="bb0c5-551">Para obter detalhes, consulte a seção "número de passaporte da Suécia" em [o que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="bb0c5-551">For details, see the section "Sweden Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="uk"></a><span data-ttu-id="bb0c5-552">Reino Unido</span><span class="sxs-lookup"><span data-stu-id="bb0c5-552">UK</span></span>

<span data-ttu-id="bb0c5-553">Para obter detalhes, consulte a seção "U.S./Reino Unido</span><span class="sxs-lookup"><span data-stu-id="bb0c5-553">For details, see the section "U.S. / U.K.</span></span> <span data-ttu-id="bb0c5-554">Número do Passport "no [que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="bb0c5-554">Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bb0c5-555">Confira também</span><span class="sxs-lookup"><span data-stu-id="bb0c5-555">See also</span></span>

[<span data-ttu-id="bb0c5-556">O que os tipos de informações confidenciais procuram</span><span class="sxs-lookup"><span data-stu-id="bb0c5-556">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)


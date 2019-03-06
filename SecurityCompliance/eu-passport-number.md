---
title: Número do Passport da UE
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/16/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: Este tópico mostra o que uma política de prevenção de perda de dados (DLP) procura quando detecta o tipo de informação confidencial do número do Passport da UE. Esse tipo de informação confidencial define diferentes padrões, palavras-chave e outras evidências para cada país.
ms.openlocfilehash: 3ab92e87607f41cffa8c15f1179a4eef5369cb29
ms.sourcegitcommit: ed822a776d3419853453583e882f3c61ca26d4b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2019
ms.locfileid: "30410926"
---
# <a name="eu-passport-number"></a><span data-ttu-id="acd4f-104">Número do Passport da UE</span><span class="sxs-lookup"><span data-stu-id="acd4f-104">EU Passport Number</span></span>

<span data-ttu-id="acd4f-105">Este tópico mostra o que uma política de prevenção de perda de dados (DLP) procura quando detecta o tipo de informação confidencial do número do Passport da UE.</span><span class="sxs-lookup"><span data-stu-id="acd4f-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Passport Number sensitive information type.</span></span> <span data-ttu-id="acd4f-106">Esse tipo de informação confidencial define diferentes padrões, palavras-chave e outras evidências para cada país.</span><span class="sxs-lookup"><span data-stu-id="acd4f-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="acd4f-107">Áustria </span><span class="sxs-lookup"><span data-stu-id="acd4f-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="acd4f-108">Format</span><span class="sxs-lookup"><span data-stu-id="acd4f-108">Format</span></span>

<span data-ttu-id="acd4f-109">Uma letra seguida de um espaço opcional e sete dígitos</span><span class="sxs-lookup"><span data-stu-id="acd4f-109">One letter followed by an optional space and seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="acd4f-110">Padrão</span><span class="sxs-lookup"><span data-stu-id="acd4f-110">Pattern</span></span>

<span data-ttu-id="acd4f-111">Uma combinação de uma letra, sete dígitos e um espaço:</span><span class="sxs-lookup"><span data-stu-id="acd4f-111">A combination of one letter, seven digits, and one space:</span></span>
  
- <span data-ttu-id="acd4f-112">Uma letra (não diferencia maiúscula de minúscula)</span><span class="sxs-lookup"><span data-stu-id="acd4f-112">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="acd4f-113">Um espaço (opcional)</span><span class="sxs-lookup"><span data-stu-id="acd4f-113">One space (optional)</span></span>
    
- <span data-ttu-id="acd4f-114">Sete dígitos</span><span class="sxs-lookup"><span data-stu-id="acd4f-114">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="acd4f-115">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="acd4f-115">Checksum</span></span>

<span data-ttu-id="acd4f-116">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="acd4f-116">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="acd4f-117">Definição</span><span class="sxs-lookup"><span data-stu-id="acd4f-117">Definition</span></span>

<span data-ttu-id="acd4f-118">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="acd4f-118">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="acd4f-119">A expressão `Regex_austria_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="acd4f-119">The regular expression  `Regex_austria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="acd4f-120">Uma palavra- `Keywords_austria_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="acd4f-120">A keyword from  `Keywords_austria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_passport_number" />
          <Match idRef="Keywords_austria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="acd4f-121">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="acd4f-121">Keywords</span></span>

<span data-ttu-id="acd4f-122">| |</span><span class="sxs-lookup"><span data-stu-id="acd4f-122"></span></span>
|<span data-ttu-id="acd4f-123">**Keywords_austria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="acd4f-123">**Keywords_austria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="acd4f-124">passport number</span><span class="sxs-lookup"><span data-stu-id="acd4f-124">passport number</span></span>  <br/> <span data-ttu-id="acd4f-125">número de passaporte austríaco</span><span class="sxs-lookup"><span data-stu-id="acd4f-125">austrian passport number</span></span>  <br/> <span data-ttu-id="acd4f-126">Passport não</span><span class="sxs-lookup"><span data-stu-id="acd4f-126">passport no</span></span>  <br/> <span data-ttu-id="acd4f-127">reisepass</span><span class="sxs-lookup"><span data-stu-id="acd4f-127">reisepass</span></span>  <br/> <span data-ttu-id="acd4f-128">österreichisch reisepass</span><span class="sxs-lookup"><span data-stu-id="acd4f-128">österreichisch reisepass</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="acd4f-129">Bélgica </span><span class="sxs-lookup"><span data-stu-id="acd4f-129">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="acd4f-130">Format</span><span class="sxs-lookup"><span data-stu-id="acd4f-130">Format</span></span>

<span data-ttu-id="acd4f-131">Duas letras seguidas por seis dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="acd4f-131">Two letters followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="acd4f-132">Padrão</span><span class="sxs-lookup"><span data-stu-id="acd4f-132">Pattern</span></span>

<span data-ttu-id="acd4f-133">Duas letras e seguidas por seis dígitos</span><span class="sxs-lookup"><span data-stu-id="acd4f-133">Two letters and followed by six digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="acd4f-134">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="acd4f-134">Checksum</span></span>

<span data-ttu-id="acd4f-135">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="acd4f-135">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="acd4f-136">Definição</span><span class="sxs-lookup"><span data-stu-id="acd4f-136">Definition</span></span>

<span data-ttu-id="acd4f-137">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="acd4f-137">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="acd4f-138">A expressão `Regex_belgium_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="acd4f-138">The regular expression  `Regex_belgium_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="acd4f-139">Uma palavra- `Keywords_belgium_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="acd4f-139">A keyword from  `Keywords_belgium_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium__eu_passport_number" />
          <Match idRef="Keywords_belgium_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="acd4f-140">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="acd4f-140">Keywords</span></span>

<span data-ttu-id="acd4f-141">| |</span><span class="sxs-lookup"><span data-stu-id="acd4f-141"></span></span>
|<span data-ttu-id="acd4f-142">**Keywords_belgium_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="acd4f-142">**Keywords_belgium_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="acd4f-143">passport number</span><span class="sxs-lookup"><span data-stu-id="acd4f-143">passport number</span></span>  <br/> <span data-ttu-id="acd4f-144">número de passaporte belga</span><span class="sxs-lookup"><span data-stu-id="acd4f-144">belgian passport number</span></span>  <br/> <span data-ttu-id="acd4f-145">Passport não</span><span class="sxs-lookup"><span data-stu-id="acd4f-145">passport no</span></span>  <br/> <span data-ttu-id="acd4f-146">paspoort</span><span class="sxs-lookup"><span data-stu-id="acd4f-146">paspoort</span></span>  <br/> <span data-ttu-id="acd4f-147">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="acd4f-147">paspoortnummer</span></span>  <br/> <span data-ttu-id="acd4f-148">reisepass Kein</span><span class="sxs-lookup"><span data-stu-id="acd4f-148">reisepass kein</span></span>  <br/> <span data-ttu-id="acd4f-149">reisepass</span><span class="sxs-lookup"><span data-stu-id="acd4f-149">reisepass</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="acd4f-150">Bulgária</span><span class="sxs-lookup"><span data-stu-id="acd4f-150">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="acd4f-151">Format</span><span class="sxs-lookup"><span data-stu-id="acd4f-151">Format</span></span>

<span data-ttu-id="acd4f-152">Nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="acd4f-152">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="acd4f-153">Padrão</span><span class="sxs-lookup"><span data-stu-id="acd4f-153">Pattern</span></span>

 <span data-ttu-id="acd4f-154">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="acd4f-154">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="acd4f-155">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="acd4f-155">Checksum</span></span>

<span data-ttu-id="acd4f-156">Não</span><span class="sxs-lookup"><span data-stu-id="acd4f-156">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="acd4f-157">Definição</span><span class="sxs-lookup"><span data-stu-id="acd4f-157">Definition</span></span>

<span data-ttu-id="acd4f-158">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="acd4f-158">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="acd4f-159">A expressão `Regex_bulgaria_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="acd4f-159">The regular expression  `Regex_bulgaria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="acd4f-160">Uma palavra- `Keywords_bulgaria_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="acd4f-160">A keyword from  `Keywords_bulgaria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_passport_number" />
          <Match idRef="Keywords_bulgaria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="acd4f-161">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="acd4f-161">Keywords</span></span>

<span data-ttu-id="acd4f-162">| |</span><span class="sxs-lookup"><span data-stu-id="acd4f-162"></span></span>
|<span data-ttu-id="acd4f-163">**Keywords_bulgaria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="acd4f-163">**Keywords_bulgaria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="acd4f-164">passport number</span><span class="sxs-lookup"><span data-stu-id="acd4f-164">passport number</span></span>  <br/> <span data-ttu-id="acd4f-165">número de passaporte búlgaro</span><span class="sxs-lookup"><span data-stu-id="acd4f-165">bulgarian passport number</span></span>  <br/> <span data-ttu-id="acd4f-166">Passport não</span><span class="sxs-lookup"><span data-stu-id="acd4f-166">passport no</span></span>  <br/> <span data-ttu-id="acd4f-167">номер на паспорта</span><span class="sxs-lookup"><span data-stu-id="acd4f-167">номер на паспорта</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="acd4f-168">Croácia</span><span class="sxs-lookup"><span data-stu-id="acd4f-168">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="acd4f-169">Format</span><span class="sxs-lookup"><span data-stu-id="acd4f-169">Format</span></span>

<span data-ttu-id="acd4f-170">Nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="acd4f-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="acd4f-171">Padrão</span><span class="sxs-lookup"><span data-stu-id="acd4f-171">Pattern</span></span>

 <span data-ttu-id="acd4f-172">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="acd4f-172">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="acd4f-173">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="acd4f-173">Checksum</span></span>

<span data-ttu-id="acd4f-174">Não</span><span class="sxs-lookup"><span data-stu-id="acd4f-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="acd4f-175">Definição</span><span class="sxs-lookup"><span data-stu-id="acd4f-175">Definition</span></span>

<span data-ttu-id="acd4f-176">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="acd4f-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="acd4f-177">A expressão `Regex_croatia_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="acd4f-177">The regular expression  `Regex_croatia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="acd4f-178">Uma palavra- `Keywords_croatia_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="acd4f-178">A keyword from  `Keywords_croatia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_passport_number" />
          <Match idRef="Keywords_croatia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="acd4f-179">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="acd4f-179">Keywords</span></span>

<span data-ttu-id="acd4f-180">| |</span><span class="sxs-lookup"><span data-stu-id="acd4f-180"></span></span>
|<span data-ttu-id="acd4f-181">**Keywords_croatia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="acd4f-181">**Keywords_croatia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="acd4f-182">passport number</span><span class="sxs-lookup"><span data-stu-id="acd4f-182">passport number</span></span>  <br/> <span data-ttu-id="acd4f-183">número de passaporte Croata</span><span class="sxs-lookup"><span data-stu-id="acd4f-183">croatian passport number</span></span>  <br/> <span data-ttu-id="acd4f-184">Passport não</span><span class="sxs-lookup"><span data-stu-id="acd4f-184">passport no</span></span>  <br/> <span data-ttu-id="acd4f-185">broj putovnice</span><span class="sxs-lookup"><span data-stu-id="acd4f-185">broj putovnice</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="acd4f-186">Chipre</span><span class="sxs-lookup"><span data-stu-id="acd4f-186">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="acd4f-187">Format</span><span class="sxs-lookup"><span data-stu-id="acd4f-187">Format</span></span>

<span data-ttu-id="acd4f-188">Uma letra seguida de 6-8 dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="acd4f-188">One letter followed by 6-8 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="acd4f-189">Padrão</span><span class="sxs-lookup"><span data-stu-id="acd4f-189">Pattern</span></span>

<span data-ttu-id="acd4f-190">Uma letra seguida de seis a oito dígitos</span><span class="sxs-lookup"><span data-stu-id="acd4f-190">One letter followed by six to eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="acd4f-191">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="acd4f-191">Checksum</span></span>

<span data-ttu-id="acd4f-192">Não</span><span class="sxs-lookup"><span data-stu-id="acd4f-192">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="acd4f-193">Definição</span><span class="sxs-lookup"><span data-stu-id="acd4f-193">Definition</span></span>

<span data-ttu-id="acd4f-194">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="acd4f-194">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="acd4f-195">A expressão `Regex_cyprus_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="acd4f-195">The regular expression  `Regex_cyprus_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="acd4f-196">Uma palavra- `Keywords_cyprus_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="acd4f-196">A keyword from  `Keywords_cyprus_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_passport_number" />
          <Match idRef="Keywords_cyprus_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="acd4f-197">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="acd4f-197">Keywords</span></span>

<span data-ttu-id="acd4f-198">| |</span><span class="sxs-lookup"><span data-stu-id="acd4f-198"></span></span>
|<span data-ttu-id="acd4f-199">**Keywords_cyprus_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="acd4f-199">**Keywords_cyprus_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="acd4f-200">passport number</span><span class="sxs-lookup"><span data-stu-id="acd4f-200">passport number</span></span>  <br/> <span data-ttu-id="acd4f-201">número de passaporte do Chipre</span><span class="sxs-lookup"><span data-stu-id="acd4f-201">cyprus passport number</span></span>  <br/> <span data-ttu-id="acd4f-202">Passport não</span><span class="sxs-lookup"><span data-stu-id="acd4f-202">passport no</span></span>  <br/> <span data-ttu-id="acd4f-203">αριθμό διαβατηρίου</span><span class="sxs-lookup"><span data-stu-id="acd4f-203">αριθμό διαβατηρίου</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="acd4f-204">República Tcheca</span><span class="sxs-lookup"><span data-stu-id="acd4f-204">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="acd4f-205">Format</span><span class="sxs-lookup"><span data-stu-id="acd4f-205">Format</span></span>

<span data-ttu-id="acd4f-206">Oito dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="acd4f-206">Eight digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="acd4f-207">Padrão</span><span class="sxs-lookup"><span data-stu-id="acd4f-207">Pattern</span></span>

<span data-ttu-id="acd4f-208">Oito dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="acd4f-208">Eight digits without spaces or delimiters</span></span>
  
### <a name="checksum"></a><span data-ttu-id="acd4f-209">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="acd4f-209">Checksum</span></span>

<span data-ttu-id="acd4f-210">Não</span><span class="sxs-lookup"><span data-stu-id="acd4f-210">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="acd4f-211">Definição</span><span class="sxs-lookup"><span data-stu-id="acd4f-211">Definition</span></span>

<span data-ttu-id="acd4f-212">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="acd4f-212">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="acd4f-213">A expressão `Regex_czech_republic_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="acd4f-213">The regular expression  `Regex_czech_republic_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="acd4f-214">Uma palavra- `Keywords_czech_republic_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="acd4f-214">A keyword from  `Keywords_czech_republic_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_passport_number" />
          <Match idRef="Keywords_czech_republic_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="acd4f-215">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="acd4f-215">Keywords</span></span>

<span data-ttu-id="acd4f-216">| |</span><span class="sxs-lookup"><span data-stu-id="acd4f-216"></span></span>
|<span data-ttu-id="acd4f-217">**Keywords_czech_republic_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="acd4f-217">**Keywords_czech_republic_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="acd4f-218">passport number</span><span class="sxs-lookup"><span data-stu-id="acd4f-218">passport number</span></span>  <br/> <span data-ttu-id="acd4f-219">número de passaporte tcheco</span><span class="sxs-lookup"><span data-stu-id="acd4f-219">czech passport number</span></span>  <br/> <span data-ttu-id="acd4f-220">Passport não</span><span class="sxs-lookup"><span data-stu-id="acd4f-220">passport no</span></span>  <br/> <span data-ttu-id="acd4f-221">Pas cestovní</span><span class="sxs-lookup"><span data-stu-id="acd4f-221">cestovní pas</span></span>  <br/> <span data-ttu-id="acd4f-222">Pas</span><span class="sxs-lookup"><span data-stu-id="acd4f-222">pas</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="acd4f-223">Dinamarca</span><span class="sxs-lookup"><span data-stu-id="acd4f-223">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="acd4f-224">Format</span><span class="sxs-lookup"><span data-stu-id="acd4f-224">Format</span></span>

<span data-ttu-id="acd4f-225">Nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="acd4f-225">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="acd4f-226">Padrão</span><span class="sxs-lookup"><span data-stu-id="acd4f-226">Pattern</span></span>

 <span data-ttu-id="acd4f-227">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="acd4f-227">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="acd4f-228">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="acd4f-228">Checksum</span></span>

<span data-ttu-id="acd4f-229">Não</span><span class="sxs-lookup"><span data-stu-id="acd4f-229">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="acd4f-230">Definição</span><span class="sxs-lookup"><span data-stu-id="acd4f-230">Definition</span></span>

<span data-ttu-id="acd4f-231">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="acd4f-231">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="acd4f-232">A expressão `Regex_denmark_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="acd4f-232">The regular expression  `Regex_denmark_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="acd4f-233">Uma palavra- `Keywords_denmark_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="acd4f-233">A keyword from  `Keywords_denmark_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_passport_number" />
          <Match idRef="Keywords_denmark_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="acd4f-234">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="acd4f-234">Keywords</span></span>

<span data-ttu-id="acd4f-235">| |</span><span class="sxs-lookup"><span data-stu-id="acd4f-235"></span></span>
|<span data-ttu-id="acd4f-236">**Keywords_denmark_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="acd4f-236">**Keywords_denmark_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="acd4f-237">passport number</span><span class="sxs-lookup"><span data-stu-id="acd4f-237">passport number</span></span>  <br/> <span data-ttu-id="acd4f-238">número de passaporte dinamarquês</span><span class="sxs-lookup"><span data-stu-id="acd4f-238">danish passport number</span></span>  <br/> <span data-ttu-id="acd4f-239">Passport não</span><span class="sxs-lookup"><span data-stu-id="acd4f-239">passport no</span></span>  <br/> <span data-ttu-id="acd4f-240">Pas</span><span class="sxs-lookup"><span data-stu-id="acd4f-240">pas</span></span>  <br/> <span data-ttu-id="acd4f-241">pasnummer</span><span class="sxs-lookup"><span data-stu-id="acd4f-241">pasnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="acd4f-242">Estônia</span><span class="sxs-lookup"><span data-stu-id="acd4f-242">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="acd4f-243">Format</span><span class="sxs-lookup"><span data-stu-id="acd4f-243">Format</span></span>

<span data-ttu-id="acd4f-244">Uma letra seguida por sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="acd4f-244">One letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="acd4f-245">Padrão</span><span class="sxs-lookup"><span data-stu-id="acd4f-245">Pattern</span></span>

<span data-ttu-id="acd4f-246">Uma letra seguida por sete dígitos</span><span class="sxs-lookup"><span data-stu-id="acd4f-246">One letter followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="acd4f-247">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="acd4f-247">Checksum</span></span>

<span data-ttu-id="acd4f-248">Não</span><span class="sxs-lookup"><span data-stu-id="acd4f-248">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="acd4f-249">Definição</span><span class="sxs-lookup"><span data-stu-id="acd4f-249">Definition</span></span>

<span data-ttu-id="acd4f-250">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="acd4f-250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="acd4f-251">A expressão `Regex_estonia_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="acd4f-251">The regular expression  `Regex_estonia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="acd4f-252">Uma palavra- `Keywords_estonia_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="acd4f-252">A keyword from  `Keywords_estonia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_passport_number" />
          <Match idRef="Keywords_estonia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="acd4f-253">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="acd4f-253">Keywords</span></span>

<span data-ttu-id="acd4f-254">| |</span><span class="sxs-lookup"><span data-stu-id="acd4f-254"></span></span>
|<span data-ttu-id="acd4f-255">**Keywords_estonia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="acd4f-255">**Keywords_estonia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="acd4f-256">passport number</span><span class="sxs-lookup"><span data-stu-id="acd4f-256">passport number</span></span>  <br/> <span data-ttu-id="acd4f-257">número de passaporte estoniano</span><span class="sxs-lookup"><span data-stu-id="acd4f-257">estonian passport number</span></span>  <br/> <span data-ttu-id="acd4f-258">Passport não</span><span class="sxs-lookup"><span data-stu-id="acd4f-258">passport no</span></span>  <br/> <span data-ttu-id="acd4f-259">Eesti kodaniku</span><span class="sxs-lookup"><span data-stu-id="acd4f-259">eesti kodaniku pass</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="acd4f-260">Finlândia</span><span class="sxs-lookup"><span data-stu-id="acd4f-260">Finland</span></span>

<span data-ttu-id="acd4f-261">Para obter detalhes, consulte a seção "número de passaporte da Finlândia" em [o que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="acd4f-261">For details, see the section "Finland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="acd4f-262">França</span><span class="sxs-lookup"><span data-stu-id="acd4f-262">France</span></span>

<span data-ttu-id="acd4f-263">Para obter detalhes, consulte a seção "número do passaporte da França" em [o que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="acd4f-263">For details, see the section "France Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="acd4f-264">Alemanha</span><span class="sxs-lookup"><span data-stu-id="acd4f-264">Germany</span></span>

<span data-ttu-id="acd4f-265">Para obter detalhes, consulte a seção "número de passaporte da Alemanha" em [o que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="acd4f-265">For details, see the section "Germany Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="acd4f-266">Grécia</span><span class="sxs-lookup"><span data-stu-id="acd4f-266">Greece</span></span>

### <a name="format"></a><span data-ttu-id="acd4f-267">Format</span><span class="sxs-lookup"><span data-stu-id="acd4f-267">Format</span></span>

<span data-ttu-id="acd4f-268">Duas letras seguidas por sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="acd4f-268">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="acd4f-269">Padrão</span><span class="sxs-lookup"><span data-stu-id="acd4f-269">Pattern</span></span>

<span data-ttu-id="acd4f-270">Duas letras seguidas por sete dígitos</span><span class="sxs-lookup"><span data-stu-id="acd4f-270">Two letters followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="acd4f-271">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="acd4f-271">Checksum</span></span>

<span data-ttu-id="acd4f-272">Não</span><span class="sxs-lookup"><span data-stu-id="acd4f-272">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="acd4f-273">Definição</span><span class="sxs-lookup"><span data-stu-id="acd4f-273">Definition</span></span>

<span data-ttu-id="acd4f-274">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="acd4f-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="acd4f-275">A expressão `Regex_greece_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="acd4f-275">The regular expression  `Regex_greece_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="acd4f-276">Uma palavra- `Keywords_greece_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="acd4f-276">A keyword from  `Keywords_greece_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_passport_number" />
          <Match idRef="Keywords_greece_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="acd4f-277">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="acd4f-277">Keywords</span></span>

<span data-ttu-id="acd4f-278">| |</span><span class="sxs-lookup"><span data-stu-id="acd4f-278"></span></span>
|<span data-ttu-id="acd4f-279">**Keywords_greece_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="acd4f-279">**Keywords_greece_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="acd4f-280">passport number</span><span class="sxs-lookup"><span data-stu-id="acd4f-280">passport number</span></span>  <br/> <span data-ttu-id="acd4f-281">número de passaporte grego</span><span class="sxs-lookup"><span data-stu-id="acd4f-281">greek passport number</span></span>  <br/> <span data-ttu-id="acd4f-282">Passport não</span><span class="sxs-lookup"><span data-stu-id="acd4f-282">passport no</span></span>  <br/> <span data-ttu-id="acd4f-283">διαβατηριο</span><span class="sxs-lookup"><span data-stu-id="acd4f-283">διαβατηριο</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="acd4f-284">Hungria</span><span class="sxs-lookup"><span data-stu-id="acd4f-284">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="acd4f-285">Format</span><span class="sxs-lookup"><span data-stu-id="acd4f-285">Format</span></span>

<span data-ttu-id="acd4f-286">Duas letras seguidas por seis ou sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="acd4f-286">Two letters followed by six or seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="acd4f-287">Padrão</span><span class="sxs-lookup"><span data-stu-id="acd4f-287">Pattern</span></span>

<span data-ttu-id="acd4f-288">Duas letras seguidas por seis ou sete dígitos</span><span class="sxs-lookup"><span data-stu-id="acd4f-288">Two letters followed by six or seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="acd4f-289">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="acd4f-289">Checksum</span></span>

<span data-ttu-id="acd4f-290">Não</span><span class="sxs-lookup"><span data-stu-id="acd4f-290">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="acd4f-291">Definição</span><span class="sxs-lookup"><span data-stu-id="acd4f-291">Definition</span></span>

<span data-ttu-id="acd4f-292">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="acd4f-292">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="acd4f-293">A expressão `Regex_hungary_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="acd4f-293">The regular expression  `Regex_hungary_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="acd4f-294">Uma palavra- `Keywords_hungary_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="acd4f-294">A keyword from  `Keywords_hungary_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_passport_number" />
          <Match idRef="Keywords_hungary_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="acd4f-295">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="acd4f-295">Keywords</span></span>

<span data-ttu-id="acd4f-296">| |</span><span class="sxs-lookup"><span data-stu-id="acd4f-296"></span></span>
|<span data-ttu-id="acd4f-297">**Keywords_hungary_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="acd4f-297">**Keywords_hungary_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="acd4f-298">passport number</span><span class="sxs-lookup"><span data-stu-id="acd4f-298">passport number</span></span>  <br/> <span data-ttu-id="acd4f-299">número de passaporte húngaro</span><span class="sxs-lookup"><span data-stu-id="acd4f-299">hungarian passport number</span></span>  <br/> <span data-ttu-id="acd4f-300">Passport não</span><span class="sxs-lookup"><span data-stu-id="acd4f-300">passport no</span></span>  <br/> <span data-ttu-id="acd4f-301">útlevél száma</span><span class="sxs-lookup"><span data-stu-id="acd4f-301">útlevél száma</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="acd4f-302">Irlanda</span><span class="sxs-lookup"><span data-stu-id="acd4f-302">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="acd4f-303">Format</span><span class="sxs-lookup"><span data-stu-id="acd4f-303">Format</span></span>

<span data-ttu-id="acd4f-304">Duas letras ou dígitos seguidos de sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="acd4f-304">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="acd4f-305">Padrão</span><span class="sxs-lookup"><span data-stu-id="acd4f-305">Pattern</span></span>

<span data-ttu-id="acd4f-306">Duas letras ou dígitos seguidos por sete dígitos:</span><span class="sxs-lookup"><span data-stu-id="acd4f-306">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="acd4f-307">Dois dígitos ou letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="acd4f-307">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="acd4f-308">Sete dígitos</span><span class="sxs-lookup"><span data-stu-id="acd4f-308">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="acd4f-309">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="acd4f-309">Checksum</span></span>

<span data-ttu-id="acd4f-310">Não</span><span class="sxs-lookup"><span data-stu-id="acd4f-310">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="acd4f-311">Definição</span><span class="sxs-lookup"><span data-stu-id="acd4f-311">Definition</span></span>

<span data-ttu-id="acd4f-312">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="acd4f-312">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="acd4f-313">A expressão `Regex_ireland_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="acd4f-313">The regular expression  `Regex_ireland_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="acd4f-314">Uma palavra- `Keywords_ireland_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="acd4f-314">A keyword from  `Keywords_ireland_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_passport_number" />
          <Match idRef="Keywords_ireland_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="acd4f-315">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="acd4f-315">Keywords</span></span>

<span data-ttu-id="acd4f-316">| |</span><span class="sxs-lookup"><span data-stu-id="acd4f-316"></span></span>
|<span data-ttu-id="acd4f-317">**Keywords_ireland_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="acd4f-317">**Keywords_ireland_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="acd4f-318">passport number</span><span class="sxs-lookup"><span data-stu-id="acd4f-318">passport number</span></span>  <br/> <span data-ttu-id="acd4f-319">número de passaporte do irlandês</span><span class="sxs-lookup"><span data-stu-id="acd4f-319">irish passport number</span></span>  <br/> <span data-ttu-id="acd4f-320">Passport não</span><span class="sxs-lookup"><span data-stu-id="acd4f-320">passport no</span></span>  <br/> <span data-ttu-id="acd4f-321">Pas</span><span class="sxs-lookup"><span data-stu-id="acd4f-321">pas</span></span>  <br/> <span data-ttu-id="acd4f-322">Passaport</span><span class="sxs-lookup"><span data-stu-id="acd4f-322">passport</span></span>  <br/> <span data-ttu-id="acd4f-323">passeport</span><span class="sxs-lookup"><span data-stu-id="acd4f-323">passeport</span></span>  <br/> <span data-ttu-id="acd4f-324">passeport numero</span><span class="sxs-lookup"><span data-stu-id="acd4f-324">passeport numero</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="acd4f-325">Itália</span><span class="sxs-lookup"><span data-stu-id="acd4f-325">Italy</span></span>

### <a name="format"></a><span data-ttu-id="acd4f-326">Format</span><span class="sxs-lookup"><span data-stu-id="acd4f-326">Format</span></span>

<span data-ttu-id="acd4f-327">Duas letras ou dígitos seguidos de sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="acd4f-327">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="acd4f-328">Padrão</span><span class="sxs-lookup"><span data-stu-id="acd4f-328">Pattern</span></span>

<span data-ttu-id="acd4f-329">Duas letras ou dígitos seguidos por sete dígitos:</span><span class="sxs-lookup"><span data-stu-id="acd4f-329">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="acd4f-330">Dois dígitos ou letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="acd4f-330">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="acd4f-331">Sete dígitos</span><span class="sxs-lookup"><span data-stu-id="acd4f-331">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="acd4f-332">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="acd4f-332">Checksum</span></span>

<span data-ttu-id="acd4f-333">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="acd4f-333">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="acd4f-334">Definição</span><span class="sxs-lookup"><span data-stu-id="acd4f-334">Definition</span></span>

<span data-ttu-id="acd4f-335">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="acd4f-335">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="acd4f-336">A expressão `Regex_italy_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="acd4f-336">The regular expression  `Regex_italy_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="acd4f-337">Uma palavra- `Keywords_italy_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="acd4f-337">A keyword from  `Keywords_italy_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_passport_number" />
          <Match idRef="Keywords_italy_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="acd4f-338">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="acd4f-338">Keywords</span></span>

<span data-ttu-id="acd4f-339">| |</span><span class="sxs-lookup"><span data-stu-id="acd4f-339"></span></span>
|<span data-ttu-id="acd4f-340">**Keywords_italy_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="acd4f-340">**Keywords_italy_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="acd4f-341">número de passaporte italiano</span><span class="sxs-lookup"><span data-stu-id="acd4f-341">italian passport number</span></span>  <br/> <span data-ttu-id="acd4f-342">Repubblica Italiana PASSAPORTO</span><span class="sxs-lookup"><span data-stu-id="acd4f-342">repubblica italiana passaporto</span></span>  <br/> <span data-ttu-id="acd4f-343">PASSAPORTO</span><span class="sxs-lookup"><span data-stu-id="acd4f-343">passaporto</span></span>  <br/> <span data-ttu-id="acd4f-344">PASSAPORTO italiana</span><span class="sxs-lookup"><span data-stu-id="acd4f-344">passaporto italiana</span></span>  <br/> <span data-ttu-id="acd4f-345">passport number</span><span class="sxs-lookup"><span data-stu-id="acd4f-345">passport number</span></span>  <br/> <span data-ttu-id="acd4f-346">italiana PASSAPORTO numero</span><span class="sxs-lookup"><span data-stu-id="acd4f-346">italiana passaporto numero</span></span>  <br/> <span data-ttu-id="acd4f-347">PASSAPORTO numero</span><span class="sxs-lookup"><span data-stu-id="acd4f-347">passaporto numero</span></span>  <br/> <span data-ttu-id="acd4f-348">Numéro passeport Italien</span><span class="sxs-lookup"><span data-stu-id="acd4f-348">numéro passeport italien</span></span>  <br/> <span data-ttu-id="acd4f-349">Numéro passeport</span><span class="sxs-lookup"><span data-stu-id="acd4f-349">numéro passeport</span></span>  <br/> |
   
## <a name="latvia"></a><span data-ttu-id="acd4f-350">Letônia</span><span class="sxs-lookup"><span data-stu-id="acd4f-350">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="acd4f-351">Format</span><span class="sxs-lookup"><span data-stu-id="acd4f-351">Format</span></span>

<span data-ttu-id="acd4f-352">Duas letras ou dígitos seguidos de sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="acd4f-352">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="acd4f-353">Padrão</span><span class="sxs-lookup"><span data-stu-id="acd4f-353">Pattern</span></span>

<span data-ttu-id="acd4f-354">Duas letras ou dígitos seguidos por sete dígitos:</span><span class="sxs-lookup"><span data-stu-id="acd4f-354">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="acd4f-355">Dois dígitos ou letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="acd4f-355">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="acd4f-356">Sete dígitos</span><span class="sxs-lookup"><span data-stu-id="acd4f-356">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="acd4f-357">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="acd4f-357">Checksum</span></span>

<span data-ttu-id="acd4f-358">Não</span><span class="sxs-lookup"><span data-stu-id="acd4f-358">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="acd4f-359">Definição</span><span class="sxs-lookup"><span data-stu-id="acd4f-359">Definition</span></span>

<span data-ttu-id="acd4f-360">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="acd4f-360">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="acd4f-361">A expressão `Regex_latvia_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="acd4f-361">The regular expression  `Regex_latvia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="acd4f-362">Uma palavra- `Keywords_latvia_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="acd4f-362">A keyword from  `Keywords_latvia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_passport_number" />
          <Match idRef="Keywords_latvia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="acd4f-363">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="acd4f-363">Keywords</span></span>

<span data-ttu-id="acd4f-364">| |</span><span class="sxs-lookup"><span data-stu-id="acd4f-364"></span></span>
|<span data-ttu-id="acd4f-365">**Keywords_latvia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="acd4f-365">**Keywords_latvia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="acd4f-366">passport number</span><span class="sxs-lookup"><span data-stu-id="acd4f-366">passport number</span></span>  <br/> <span data-ttu-id="acd4f-367">número de passaporte da Letão</span><span class="sxs-lookup"><span data-stu-id="acd4f-367">latvian passport number</span></span>  <br/> <span data-ttu-id="acd4f-368">Passport não</span><span class="sxs-lookup"><span data-stu-id="acd4f-368">passport no</span></span>  <br/> <span data-ttu-id="acd4f-369">pase numurs</span><span class="sxs-lookup"><span data-stu-id="acd4f-369">pase numurs</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="acd4f-370">Lituânia</span><span class="sxs-lookup"><span data-stu-id="acd4f-370">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="acd4f-371">Format</span><span class="sxs-lookup"><span data-stu-id="acd4f-371">Format</span></span>

<span data-ttu-id="acd4f-372">Oito dígitos ou letras sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="acd4f-372">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="acd4f-373">Padrão</span><span class="sxs-lookup"><span data-stu-id="acd4f-373">Pattern</span></span>

<span data-ttu-id="acd4f-374">Oito dígitos ou letras (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="acd4f-374">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="acd4f-375">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="acd4f-375">Checksum</span></span>

<span data-ttu-id="acd4f-376">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="acd4f-376">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="acd4f-377">Definição</span><span class="sxs-lookup"><span data-stu-id="acd4f-377">Definition</span></span>

<span data-ttu-id="acd4f-378">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="acd4f-378">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="acd4f-379">A expressão `Regex_lithuania_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="acd4f-379">The regular expression  `Regex_lithuania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="acd4f-380">Uma palavra- `Keywords_lithuania_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="acd4f-380">A keyword from  `Keywords_lithuania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_passport_number" />
          <Match idRef="Keywords_lithuania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="acd4f-381">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="acd4f-381">Keywords</span></span>

<span data-ttu-id="acd4f-382">| |</span><span class="sxs-lookup"><span data-stu-id="acd4f-382"></span></span>
|<span data-ttu-id="acd4f-383">**Keywords_lithuania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="acd4f-383">**Keywords_lithuania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="acd4f-384">passport number</span><span class="sxs-lookup"><span data-stu-id="acd4f-384">passport number</span></span>  <br/> <span data-ttu-id="acd4f-385">número de passaporte lithunian</span><span class="sxs-lookup"><span data-stu-id="acd4f-385">lithunian passport number</span></span>  <br/> <span data-ttu-id="acd4f-386">Passport não</span><span class="sxs-lookup"><span data-stu-id="acd4f-386">passport no</span></span>  <br/> <span data-ttu-id="acd4f-387">Paso Numeris</span><span class="sxs-lookup"><span data-stu-id="acd4f-387">paso numeris</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="acd4f-388">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="acd4f-388">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="acd4f-389">Format</span><span class="sxs-lookup"><span data-stu-id="acd4f-389">Format</span></span>

<span data-ttu-id="acd4f-390">Oito dígitos ou letras sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="acd4f-390">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="acd4f-391">Padrão</span><span class="sxs-lookup"><span data-stu-id="acd4f-391">Pattern</span></span>

<span data-ttu-id="acd4f-392">Oito dígitos ou letras (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="acd4f-392">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="acd4f-393">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="acd4f-393">Checksum</span></span>

<span data-ttu-id="acd4f-394">Não</span><span class="sxs-lookup"><span data-stu-id="acd4f-394">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="acd4f-395">Definição</span><span class="sxs-lookup"><span data-stu-id="acd4f-395">Definition</span></span>

<span data-ttu-id="acd4f-396">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="acd4f-396">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="acd4f-397">A expressão `Regex_nation_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="acd4f-397">The regular expression  `Regex_nation_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="acd4f-398">Uma palavra- `Keywords_nation_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="acd4f-398">A keyword from  `Keywords_nation_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_nation_eu_passport_number" />
          <Match idRef="Keywords_nation_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="acd4f-399">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="acd4f-399">Keywords</span></span>

<span data-ttu-id="acd4f-400">| |</span><span class="sxs-lookup"><span data-stu-id="acd4f-400"></span></span>
|<span data-ttu-id="acd4f-401">**Keywords_nation_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="acd4f-401">**Keywords_nation_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="acd4f-402">passport number</span><span class="sxs-lookup"><span data-stu-id="acd4f-402">passport number</span></span>  <br/> <span data-ttu-id="acd4f-403">número de passaporte da Letão</span><span class="sxs-lookup"><span data-stu-id="acd4f-403">latvian passport number</span></span>  <br/> <span data-ttu-id="acd4f-404">Passport não</span><span class="sxs-lookup"><span data-stu-id="acd4f-404">passport no</span></span>  <br/> <span data-ttu-id="acd4f-405">passnummer</span><span class="sxs-lookup"><span data-stu-id="acd4f-405">passnummer</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="acd4f-406">Malta</span><span class="sxs-lookup"><span data-stu-id="acd4f-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="acd4f-407">Format</span><span class="sxs-lookup"><span data-stu-id="acd4f-407">Format</span></span>

<span data-ttu-id="acd4f-408">Sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="acd4f-408">Seven digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="acd4f-409">Padrão</span><span class="sxs-lookup"><span data-stu-id="acd4f-409">Pattern</span></span>

 <span data-ttu-id="acd4f-410">Sete dígitos</span><span class="sxs-lookup"><span data-stu-id="acd4f-410">Seven digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="acd4f-411">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="acd4f-411">Checksum</span></span>

<span data-ttu-id="acd4f-412">Não</span><span class="sxs-lookup"><span data-stu-id="acd4f-412">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="acd4f-413">Definição</span><span class="sxs-lookup"><span data-stu-id="acd4f-413">Definition</span></span>

<span data-ttu-id="acd4f-414">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="acd4f-414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="acd4f-415">A expressão `Regex_malta_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="acd4f-415">The regular expression  `Regex_malta_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="acd4f-416">Uma palavra- `Keywords_malta_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="acd4f-416">A keyword from  `Keywords_malta_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_passport_number" />
          <Match idRef="Keywords_malta_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="acd4f-417">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="acd4f-417">Keywords</span></span>

<span data-ttu-id="acd4f-418">| |</span><span class="sxs-lookup"><span data-stu-id="acd4f-418"></span></span>
|<span data-ttu-id="acd4f-419">**Keywords_malta_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="acd4f-419">**Keywords_malta_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="acd4f-420">passport number</span><span class="sxs-lookup"><span data-stu-id="acd4f-420">passport number</span></span>  <br/> <span data-ttu-id="acd4f-421">número de passaporte Maltês</span><span class="sxs-lookup"><span data-stu-id="acd4f-421">maltese passport number</span></span>  <br/> <span data-ttu-id="acd4f-422">Passport não</span><span class="sxs-lookup"><span data-stu-id="acd4f-422">passport no</span></span>  <br/> <span data-ttu-id="acd4f-423">numru tal-Passaport</span><span class="sxs-lookup"><span data-stu-id="acd4f-423">numru tal-passaport</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="acd4f-424">Países Baixos</span><span class="sxs-lookup"><span data-stu-id="acd4f-424">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="acd4f-425">Format</span><span class="sxs-lookup"><span data-stu-id="acd4f-425">Format</span></span>

<span data-ttu-id="acd4f-426">Nove letras ou dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="acd4f-426">Nine letters or digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="acd4f-427">Padrão</span><span class="sxs-lookup"><span data-stu-id="acd4f-427">Pattern</span></span>

<span data-ttu-id="acd4f-428">Nove letras ou dígitos</span><span class="sxs-lookup"><span data-stu-id="acd4f-428">Nine letters or digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="acd4f-429">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="acd4f-429">Checksum</span></span>

<span data-ttu-id="acd4f-430">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="acd4f-430">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="acd4f-431">Definição</span><span class="sxs-lookup"><span data-stu-id="acd4f-431">Definition</span></span>

<span data-ttu-id="acd4f-432">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="acd4f-432">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="acd4f-433">A expressão `Regex_netherlands_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="acd4f-433">The regular expression  `Regex_netherlands_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="acd4f-434">Uma palavra- `Keywords_netherlands_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="acd4f-434">A keyword from  `Keywords_netherlands_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_passport_number" />
          <Match idRef="Keywords_netherlands_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="acd4f-435">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="acd4f-435">Keywords</span></span>

<span data-ttu-id="acd4f-436">| |</span><span class="sxs-lookup"><span data-stu-id="acd4f-436"></span></span>
|<span data-ttu-id="acd4f-437">**Keywords_netherlands_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="acd4f-437">**Keywords_netherlands_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="acd4f-438">número de passaporte holandês</span><span class="sxs-lookup"><span data-stu-id="acd4f-438">dutch passport number</span></span>  <br/> <span data-ttu-id="acd4f-439">passport number</span><span class="sxs-lookup"><span data-stu-id="acd4f-439">passport number</span></span>  <br/> <span data-ttu-id="acd4f-440">número de passaporte Holanda</span><span class="sxs-lookup"><span data-stu-id="acd4f-440">netherlands passport number</span></span>  <br/> <span data-ttu-id="acd4f-441">Nederlanden paspoort Nummer</span><span class="sxs-lookup"><span data-stu-id="acd4f-441">nederlanden paspoort nummer</span></span>  <br/> <span data-ttu-id="acd4f-442">paspoort</span><span class="sxs-lookup"><span data-stu-id="acd4f-442">paspoort</span></span>  <br/> <span data-ttu-id="acd4f-443">Nederlanden paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="acd4f-443">nederlanden paspoortnummer</span></span>  <br/> <span data-ttu-id="acd4f-444">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="acd4f-444">paspoortnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="acd4f-445">Polônia</span><span class="sxs-lookup"><span data-stu-id="acd4f-445">Poland</span></span>

<span data-ttu-id="acd4f-446">Para obter detalhes, consulte a seção "número de passaporte da Polônia" em [o que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="acd4f-446">For details, see the section "Poland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="acd4f-447">Portugal</span><span class="sxs-lookup"><span data-stu-id="acd4f-447">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="acd4f-448">Format</span><span class="sxs-lookup"><span data-stu-id="acd4f-448">Format</span></span>

<span data-ttu-id="acd4f-449">Uma letra seguida de seis dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="acd4f-449">One letter followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="acd4f-450">Padrão</span><span class="sxs-lookup"><span data-stu-id="acd4f-450">Pattern</span></span>

<span data-ttu-id="acd4f-451">Uma letra seguida por seis dígitos:</span><span class="sxs-lookup"><span data-stu-id="acd4f-451">One letter followed by six digits:</span></span>
  
- <span data-ttu-id="acd4f-452">Uma letra (não diferencia maiúscula de minúscula)</span><span class="sxs-lookup"><span data-stu-id="acd4f-452">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="acd4f-453">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="acd4f-453">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="acd4f-454">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="acd4f-454">Checksum</span></span>

<span data-ttu-id="acd4f-455">Não</span><span class="sxs-lookup"><span data-stu-id="acd4f-455">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="acd4f-456">Definição</span><span class="sxs-lookup"><span data-stu-id="acd4f-456">Definition</span></span>

<span data-ttu-id="acd4f-457">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="acd4f-457">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="acd4f-458">A expressão `Regex_portugal_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="acd4f-458">The regular expression  `Regex_portugal_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="acd4f-459">Uma palavra- `Keywords_portugal_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="acd4f-459">A keyword from  `Keywords_portugal_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_passport_number" />
          <Match idRef="Keywords_portugal_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="acd4f-460">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="acd4f-460">Keywords</span></span>

<span data-ttu-id="acd4f-461">| |</span><span class="sxs-lookup"><span data-stu-id="acd4f-461"></span></span>
|<span data-ttu-id="acd4f-462">**Keywords_portugal_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="acd4f-462">**Keywords_portugal_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="acd4f-463">passport number</span><span class="sxs-lookup"><span data-stu-id="acd4f-463">passport number</span></span>  <br/> <span data-ttu-id="acd4f-464">número de passaporte Português</span><span class="sxs-lookup"><span data-stu-id="acd4f-464">portuguese passport number</span></span>  <br/> <span data-ttu-id="acd4f-465">Passport não</span><span class="sxs-lookup"><span data-stu-id="acd4f-465">passport no</span></span>  <br/> <span data-ttu-id="acd4f-466">número do passaporte</span><span class="sxs-lookup"><span data-stu-id="acd4f-466">número do passaporte</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="acd4f-467">Romênia</span><span class="sxs-lookup"><span data-stu-id="acd4f-467">Romania</span></span>

### <a name="format"></a><span data-ttu-id="acd4f-468">Format</span><span class="sxs-lookup"><span data-stu-id="acd4f-468">Format</span></span>

<span data-ttu-id="acd4f-469">Oito ou nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="acd4f-469">Eight or nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="acd4f-470">Padrão</span><span class="sxs-lookup"><span data-stu-id="acd4f-470">Pattern</span></span>

<span data-ttu-id="acd4f-471">Oito ou nove dígitos</span><span class="sxs-lookup"><span data-stu-id="acd4f-471">Eight or nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="acd4f-472">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="acd4f-472">Checksum</span></span>

<span data-ttu-id="acd4f-473">Não</span><span class="sxs-lookup"><span data-stu-id="acd4f-473">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="acd4f-474">Definição</span><span class="sxs-lookup"><span data-stu-id="acd4f-474">Definition</span></span>

<span data-ttu-id="acd4f-475">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="acd4f-475">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="acd4f-476">A expressão `Regex_romania_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="acd4f-476">The regular expression  `Regex_romania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="acd4f-477">Uma palavra- `Keywords_romania_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="acd4f-477">A keyword from  `Keywords_romania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_passport_number" />
          <Match idRef="Keywords_romania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="acd4f-478">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="acd4f-478">Keywords</span></span>

<span data-ttu-id="acd4f-479">| |</span><span class="sxs-lookup"><span data-stu-id="acd4f-479"></span></span>
|<span data-ttu-id="acd4f-480">**Keywords_romania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="acd4f-480">**Keywords_romania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="acd4f-481">passport number</span><span class="sxs-lookup"><span data-stu-id="acd4f-481">passport number</span></span>  <br/> <span data-ttu-id="acd4f-482">número de passaporte romeno</span><span class="sxs-lookup"><span data-stu-id="acd4f-482">romanian passport number</span></span>  <br/> <span data-ttu-id="acd4f-483">Passport não</span><span class="sxs-lookup"><span data-stu-id="acd4f-483">passport no</span></span>  <br/> <span data-ttu-id="acd4f-484">numărul pașaportului</span><span class="sxs-lookup"><span data-stu-id="acd4f-484">numărul pașaportului</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="acd4f-485">Eslováquia</span><span class="sxs-lookup"><span data-stu-id="acd4f-485">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="acd4f-486">Format</span><span class="sxs-lookup"><span data-stu-id="acd4f-486">Format</span></span>

<span data-ttu-id="acd4f-487">Um dígito ou letra seguido por sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="acd4f-487">One digit or letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="acd4f-488">Padrão</span><span class="sxs-lookup"><span data-stu-id="acd4f-488">Pattern</span></span>

<span data-ttu-id="acd4f-489">Um dígito ou letra (não diferencia maiúsculas de minúsculas) seguido por sete dígitos</span><span class="sxs-lookup"><span data-stu-id="acd4f-489">One digit or letter (not case sensitive) followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="acd4f-490">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="acd4f-490">Checksum</span></span>

<span data-ttu-id="acd4f-491">Não</span><span class="sxs-lookup"><span data-stu-id="acd4f-491">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="acd4f-492">Definição</span><span class="sxs-lookup"><span data-stu-id="acd4f-492">Definition</span></span>

<span data-ttu-id="acd4f-493">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="acd4f-493">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="acd4f-494">A expressão `Regex_slovakia_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="acd4f-494">The regular expression  `Regex_slovakia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="acd4f-495">Uma palavra- `Keywords_slovakia_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="acd4f-495">A keyword from  `Keywords_slovakia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_passport_number" />
          <Match idRef="Keywords_slovakia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="acd4f-496">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="acd4f-496">Keywords</span></span>

<span data-ttu-id="acd4f-497">| |</span><span class="sxs-lookup"><span data-stu-id="acd4f-497"></span></span>
|<span data-ttu-id="acd4f-498">**Keywords_slovakia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="acd4f-498">**Keywords_slovakia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="acd4f-499">passport number</span><span class="sxs-lookup"><span data-stu-id="acd4f-499">passport number</span></span>  <br/> <span data-ttu-id="acd4f-500">número de passaporte eslovaco</span><span class="sxs-lookup"><span data-stu-id="acd4f-500">slovakian passport number</span></span>  <br/> <span data-ttu-id="acd4f-501">Passport não</span><span class="sxs-lookup"><span data-stu-id="acd4f-501">passport no</span></span>  <br/> <span data-ttu-id="acd4f-502">číslo Pasu</span><span class="sxs-lookup"><span data-stu-id="acd4f-502">číslo pasu</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="acd4f-503">Eslovênia</span><span class="sxs-lookup"><span data-stu-id="acd4f-503">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="acd4f-504">Format</span><span class="sxs-lookup"><span data-stu-id="acd4f-504">Format</span></span>

<span data-ttu-id="acd4f-505">Duas letras seguidas por sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="acd4f-505">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="acd4f-506">Padrão</span><span class="sxs-lookup"><span data-stu-id="acd4f-506">Pattern</span></span>

<span data-ttu-id="acd4f-507">Duas letras seguidas por sete dígitos:</span><span class="sxs-lookup"><span data-stu-id="acd4f-507">Two letters followed by seven digits:</span></span>
  
- <span data-ttu-id="acd4f-508">A letra "P"</span><span class="sxs-lookup"><span data-stu-id="acd4f-508">The letter "P"</span></span>
    
- <span data-ttu-id="acd4f-509">Uma letra maiúscula</span><span class="sxs-lookup"><span data-stu-id="acd4f-509">One uppercase letter</span></span>
    
- <span data-ttu-id="acd4f-510">Sete dígitos</span><span class="sxs-lookup"><span data-stu-id="acd4f-510">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="acd4f-511">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="acd4f-511">Checksum</span></span>

<span data-ttu-id="acd4f-512">Não</span><span class="sxs-lookup"><span data-stu-id="acd4f-512">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="acd4f-513">Definição</span><span class="sxs-lookup"><span data-stu-id="acd4f-513">Definition</span></span>

<span data-ttu-id="acd4f-514">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="acd4f-514">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="acd4f-515">A expressão `Regex_slovenia_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="acd4f-515">The regular expression  `Regex_slovenia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="acd4f-516">Uma palavra- `Keywords_slovenia_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="acd4f-516">A keyword from  `Keywords_slovenia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_passport_number" />
          <Match idRef="Keywords_slovenia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="acd4f-517">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="acd4f-517">Keywords</span></span>

<span data-ttu-id="acd4f-518">| |</span><span class="sxs-lookup"><span data-stu-id="acd4f-518"></span></span>
|<span data-ttu-id="acd4f-519">**Keywords_slovenia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="acd4f-519">**Keywords_slovenia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="acd4f-520">passport number</span><span class="sxs-lookup"><span data-stu-id="acd4f-520">passport number</span></span>  <br/> <span data-ttu-id="acd4f-521">número de passaporte esloveno</span><span class="sxs-lookup"><span data-stu-id="acd4f-521">slovenian passport number</span></span>  <br/> <span data-ttu-id="acd4f-522">Passport não</span><span class="sxs-lookup"><span data-stu-id="acd4f-522">passport no</span></span>  <br/> <span data-ttu-id="acd4f-523">lista de številka potnega</span><span class="sxs-lookup"><span data-stu-id="acd4f-523">številka potnega lista</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="acd4f-524">Espanha</span><span class="sxs-lookup"><span data-stu-id="acd4f-524">Spain</span></span>

### <a name="format"></a><span data-ttu-id="acd4f-525">Format</span><span class="sxs-lookup"><span data-stu-id="acd4f-525">Format</span></span>

<span data-ttu-id="acd4f-526">Uma combinação de letras e números de oito ou nove caracteres sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="acd4f-526">An eight- or nine-character combination of letters and numbers with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="acd4f-527">Padrão</span><span class="sxs-lookup"><span data-stu-id="acd4f-527">Pattern</span></span>

<span data-ttu-id="acd4f-528">Uma combinação de letras e números de oito ou nove caracteres:</span><span class="sxs-lookup"><span data-stu-id="acd4f-528">An eight- or nine-character combination of letters and numbers:</span></span>
  
-  <span data-ttu-id="acd4f-529">Dois dígitos ou letras</span><span class="sxs-lookup"><span data-stu-id="acd4f-529">Two digits or letters</span></span> 
    
- <span data-ttu-id="acd4f-530">Um dígito ou letra (opcional)</span><span class="sxs-lookup"><span data-stu-id="acd4f-530">One digit or letter (optional)</span></span>
    
- <span data-ttu-id="acd4f-531">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="acd4f-531">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="acd4f-532">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="acd4f-532">Checksum</span></span>

<span data-ttu-id="acd4f-533">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="acd4f-533">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="acd4f-534">Definição</span><span class="sxs-lookup"><span data-stu-id="acd4f-534">Definition</span></span>

<span data-ttu-id="acd4f-535">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="acd4f-535">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="acd4f-536">A expressão `Regex_spain_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="acd4f-536">The regular expression  `Regex_spain_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="acd4f-537">Uma palavra- `Keywords_spain_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="acd4f-537">A keyword from  `Keywords_spain_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_passport_number" />
          <Match idRef="Keywords_spain_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="acd4f-538">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="acd4f-538">Keywords</span></span>

<span data-ttu-id="acd4f-539">| |</span><span class="sxs-lookup"><span data-stu-id="acd4f-539"></span></span>
|<span data-ttu-id="acd4f-540">**Keywords_spain_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="acd4f-540">**Keywords_spain_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="acd4f-541">Passaport</span><span class="sxs-lookup"><span data-stu-id="acd4f-541">passport</span></span>  <br/> <span data-ttu-id="acd4f-542">o Passport da Espanha</span><span class="sxs-lookup"><span data-stu-id="acd4f-542">spain passport</span></span>  <br/> <span data-ttu-id="acd4f-543">Catálogo do Passport</span><span class="sxs-lookup"><span data-stu-id="acd4f-543">passport book</span></span>  <br/> <span data-ttu-id="acd4f-544">passport number</span><span class="sxs-lookup"><span data-stu-id="acd4f-544">passport number</span></span>  <br/> <span data-ttu-id="acd4f-545">Passport não</span><span class="sxs-lookup"><span data-stu-id="acd4f-545">passport no</span></span>  <br/> <span data-ttu-id="acd4f-546">Libreta pasaporte</span><span class="sxs-lookup"><span data-stu-id="acd4f-546">libreta pasaporte</span></span>  <br/> <span data-ttu-id="acd4f-547">número pasaporte</span><span class="sxs-lookup"><span data-stu-id="acd4f-547">número pasaporte</span></span>  <br/> <span data-ttu-id="acd4f-548">España pasaporte</span><span class="sxs-lookup"><span data-stu-id="acd4f-548">españa pasaporte</span></span>  <br/> <span data-ttu-id="acd4f-549">pasaporte</span><span class="sxs-lookup"><span data-stu-id="acd4f-549">pasaporte</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="acd4f-550">Suécia</span><span class="sxs-lookup"><span data-stu-id="acd4f-550">Sweden</span></span>

<span data-ttu-id="acd4f-551">Para obter detalhes, consulte a seção "número de passaporte da Suécia" em [o que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="acd4f-551">For details, see the section "Sweden Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="uk"></a><span data-ttu-id="acd4f-552">Reino Unido</span><span class="sxs-lookup"><span data-stu-id="acd4f-552">UK</span></span>

<span data-ttu-id="acd4f-553">Para obter detalhes, consulte a seção "U.S./Reino Unido</span><span class="sxs-lookup"><span data-stu-id="acd4f-553">For details, see the section "U.S. / U.K.</span></span> <span data-ttu-id="acd4f-554">Número do Passport "no [que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="acd4f-554">Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="acd4f-555">Confira também</span><span class="sxs-lookup"><span data-stu-id="acd4f-555">See also</span></span>

[<span data-ttu-id="acd4f-556">O que os tipos de informações confidenciais procuram</span><span class="sxs-lookup"><span data-stu-id="acd4f-556">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)


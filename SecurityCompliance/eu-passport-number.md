---
title: Número do Passport da UE
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/16/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 8c00df57-9fb3-459c-ba87-40480c87bd55
description: Este tópico mostra o que uma política de prevenção de perda de dados (DLP) procura quando detecta o tipo de informação confidencial do número do Passport da UE. Esse tipo de informação confidencial define diferentes padrões, palavras-chave e outras evidências para cada país.
ms.openlocfilehash: c46f683bd1baf651bcf13c1766dfff3cb953b341
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218261"
---
# <a name="eu-passport-number"></a><span data-ttu-id="0285a-104">Número do Passport da UE</span><span class="sxs-lookup"><span data-stu-id="0285a-104">EU Passport Number</span></span>

<span data-ttu-id="0285a-p102">Este tópico mostra o que uma política de prevenção de perda de dados (DLP) procura quando detecta o tipo de informação confidencial do número do Passport da UE. Esse tipo de informação confidencial define diferentes padrões, palavras-chave e outras evidências para cada país.</span><span class="sxs-lookup"><span data-stu-id="0285a-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Passport Number sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="0285a-107">Áustria</span><span class="sxs-lookup"><span data-stu-id="0285a-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="0285a-108">Formato</span><span class="sxs-lookup"><span data-stu-id="0285a-108">Format</span></span>

<span data-ttu-id="0285a-109">Uma letra seguida de um espaço opcional e sete dígitos</span><span class="sxs-lookup"><span data-stu-id="0285a-109">One letter followed by an optional space and seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0285a-110">Padrão</span><span class="sxs-lookup"><span data-stu-id="0285a-110">Pattern</span></span>

<span data-ttu-id="0285a-111">Uma combinação de uma letra, sete dígitos e um espaço:</span><span class="sxs-lookup"><span data-stu-id="0285a-111">A combination of one letter, seven digits, and one space:</span></span>
  
- <span data-ttu-id="0285a-112">Uma letra (não diferencia maiúscula de minúscula)</span><span class="sxs-lookup"><span data-stu-id="0285a-112">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="0285a-113">Um espaço (opcional)</span><span class="sxs-lookup"><span data-stu-id="0285a-113">One space (optional)</span></span>
    
- <span data-ttu-id="0285a-114">Sete dígitos</span><span class="sxs-lookup"><span data-stu-id="0285a-114">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0285a-115">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="0285a-115">Checksum</span></span>

<span data-ttu-id="0285a-116">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="0285a-116">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="0285a-117">Definição</span><span class="sxs-lookup"><span data-stu-id="0285a-117">Definition</span></span>

<span data-ttu-id="0285a-118">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="0285a-118">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0285a-119">A expressão `Regex_austria_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="0285a-119">The regular expression  `Regex_austria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0285a-120">Uma palavra- `Keywords_austria_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="0285a-120">A keyword from  `Keywords_austria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_passport_number" />
          <Match idRef="Keywords_austria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0285a-121">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="0285a-121">Keywords</span></span>

<span data-ttu-id="0285a-122">| |</span><span class="sxs-lookup"><span data-stu-id="0285a-122"></span></span>
|<span data-ttu-id="0285a-123">**Keywords_austria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="0285a-123">**Keywords_austria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="0285a-124">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="0285a-124">passport number</span></span>  <br/> <span data-ttu-id="0285a-125">número de passaporte austríaco</span><span class="sxs-lookup"><span data-stu-id="0285a-125">austrian passport number</span></span>  <br/> <span data-ttu-id="0285a-126">Passport não</span><span class="sxs-lookup"><span data-stu-id="0285a-126">passport no</span></span>  <br/> <span data-ttu-id="0285a-127">reisepass</span><span class="sxs-lookup"><span data-stu-id="0285a-127">reisepass</span></span>  <br/> <span data-ttu-id="0285a-128">österreichisch reisepass</span><span class="sxs-lookup"><span data-stu-id="0285a-128">österreichisch reisepass</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="0285a-129">Bélgica</span><span class="sxs-lookup"><span data-stu-id="0285a-129">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="0285a-130">Formato</span><span class="sxs-lookup"><span data-stu-id="0285a-130">Format</span></span>

<span data-ttu-id="0285a-131">Duas letras seguidas por seis dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="0285a-131">Two letters followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0285a-132">Padrão</span><span class="sxs-lookup"><span data-stu-id="0285a-132">Pattern</span></span>

<span data-ttu-id="0285a-133">Duas letras e seguidas por seis dígitos</span><span class="sxs-lookup"><span data-stu-id="0285a-133">Two letters and followed by six digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0285a-134">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="0285a-134">Checksum</span></span>

<span data-ttu-id="0285a-135">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="0285a-135">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="0285a-136">Definição</span><span class="sxs-lookup"><span data-stu-id="0285a-136">Definition</span></span>

<span data-ttu-id="0285a-137">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="0285a-137">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0285a-138">A expressão `Regex_belgium_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="0285a-138">The regular expression  `Regex_belgium_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0285a-139">Uma palavra- `Keywords_belgium_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="0285a-139">A keyword from  `Keywords_belgium_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium__eu_passport_number" />
          <Match idRef="Keywords_belgium_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0285a-140">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="0285a-140">Keywords</span></span>

<span data-ttu-id="0285a-141">| |</span><span class="sxs-lookup"><span data-stu-id="0285a-141"></span></span>
|<span data-ttu-id="0285a-142">**Keywords_belgium_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="0285a-142">**Keywords_belgium_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="0285a-143">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="0285a-143">passport number</span></span>  <br/> <span data-ttu-id="0285a-144">número de passaporte belga</span><span class="sxs-lookup"><span data-stu-id="0285a-144">belgian passport number</span></span>  <br/> <span data-ttu-id="0285a-145">Passport não</span><span class="sxs-lookup"><span data-stu-id="0285a-145">passport no</span></span>  <br/> <span data-ttu-id="0285a-146">paspoort</span><span class="sxs-lookup"><span data-stu-id="0285a-146">paspoort</span></span>  <br/> <span data-ttu-id="0285a-147">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="0285a-147">paspoortnummer</span></span>  <br/> <span data-ttu-id="0285a-148">reisepass Kein</span><span class="sxs-lookup"><span data-stu-id="0285a-148">reisepass kein</span></span>  <br/> <span data-ttu-id="0285a-149">reisepass</span><span class="sxs-lookup"><span data-stu-id="0285a-149">reisepass</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="0285a-150">Bulgária</span><span class="sxs-lookup"><span data-stu-id="0285a-150">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="0285a-151">Formato</span><span class="sxs-lookup"><span data-stu-id="0285a-151">Format</span></span>

<span data-ttu-id="0285a-152">Nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="0285a-152">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0285a-153">Padrão</span><span class="sxs-lookup"><span data-stu-id="0285a-153">Pattern</span></span>

 <span data-ttu-id="0285a-154">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="0285a-154">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="0285a-155">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="0285a-155">Checksum</span></span>

<span data-ttu-id="0285a-156">Não</span><span class="sxs-lookup"><span data-stu-id="0285a-156">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="0285a-157">Definição</span><span class="sxs-lookup"><span data-stu-id="0285a-157">Definition</span></span>

<span data-ttu-id="0285a-158">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="0285a-158">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0285a-159">A expressão `Regex_bulgaria_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="0285a-159">The regular expression  `Regex_bulgaria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0285a-160">Uma palavra- `Keywords_bulgaria_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="0285a-160">A keyword from  `Keywords_bulgaria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_passport_number" />
          <Match idRef="Keywords_bulgaria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0285a-161">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="0285a-161">Keywords</span></span>

<span data-ttu-id="0285a-162">| |</span><span class="sxs-lookup"><span data-stu-id="0285a-162"></span></span>
|<span data-ttu-id="0285a-163">**Keywords_bulgaria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="0285a-163">**Keywords_bulgaria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="0285a-164">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="0285a-164">passport number</span></span>  <br/> <span data-ttu-id="0285a-165">número de passaporte búlgaro</span><span class="sxs-lookup"><span data-stu-id="0285a-165">bulgarian passport number</span></span>  <br/> <span data-ttu-id="0285a-166">Passport não</span><span class="sxs-lookup"><span data-stu-id="0285a-166">passport no</span></span>  <br/> <span data-ttu-id="0285a-167">номер на паспорта</span><span class="sxs-lookup"><span data-stu-id="0285a-167">номер на паспорта</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="0285a-168">Croácia</span><span class="sxs-lookup"><span data-stu-id="0285a-168">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="0285a-169">Formato</span><span class="sxs-lookup"><span data-stu-id="0285a-169">Format</span></span>

<span data-ttu-id="0285a-170">Nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="0285a-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0285a-171">Padrão</span><span class="sxs-lookup"><span data-stu-id="0285a-171">Pattern</span></span>

 <span data-ttu-id="0285a-172">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="0285a-172">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="0285a-173">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="0285a-173">Checksum</span></span>

<span data-ttu-id="0285a-174">Não</span><span class="sxs-lookup"><span data-stu-id="0285a-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="0285a-175">Definição</span><span class="sxs-lookup"><span data-stu-id="0285a-175">Definition</span></span>

<span data-ttu-id="0285a-176">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="0285a-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0285a-177">A expressão `Regex_croatia_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="0285a-177">The regular expression  `Regex_croatia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0285a-178">Uma palavra- `Keywords_croatia_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="0285a-178">A keyword from  `Keywords_croatia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_passport_number" />
          <Match idRef="Keywords_croatia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0285a-179">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="0285a-179">Keywords</span></span>

<span data-ttu-id="0285a-180">| |</span><span class="sxs-lookup"><span data-stu-id="0285a-180"></span></span>
|<span data-ttu-id="0285a-181">**Keywords_croatia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="0285a-181">**Keywords_croatia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="0285a-182">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="0285a-182">passport number</span></span>  <br/> <span data-ttu-id="0285a-183">número de passaporte Croata</span><span class="sxs-lookup"><span data-stu-id="0285a-183">croatian passport number</span></span>  <br/> <span data-ttu-id="0285a-184">Passport não</span><span class="sxs-lookup"><span data-stu-id="0285a-184">passport no</span></span>  <br/> <span data-ttu-id="0285a-185">broj putovnice</span><span class="sxs-lookup"><span data-stu-id="0285a-185">broj putovnice</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="0285a-186">Chipre</span><span class="sxs-lookup"><span data-stu-id="0285a-186">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="0285a-187">Formato</span><span class="sxs-lookup"><span data-stu-id="0285a-187">Format</span></span>

<span data-ttu-id="0285a-188">Uma letra seguida de 6-8 dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="0285a-188">One letter followed by 6-8 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0285a-189">Padrão</span><span class="sxs-lookup"><span data-stu-id="0285a-189">Pattern</span></span>

<span data-ttu-id="0285a-190">Uma letra seguida de seis a oito dígitos</span><span class="sxs-lookup"><span data-stu-id="0285a-190">One letter followed by six to eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0285a-191">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="0285a-191">Checksum</span></span>

<span data-ttu-id="0285a-192">Não</span><span class="sxs-lookup"><span data-stu-id="0285a-192">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="0285a-193">Definição</span><span class="sxs-lookup"><span data-stu-id="0285a-193">Definition</span></span>

<span data-ttu-id="0285a-194">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="0285a-194">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0285a-195">A expressão `Regex_cyprus_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="0285a-195">The regular expression  `Regex_cyprus_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0285a-196">Uma palavra- `Keywords_cyprus_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="0285a-196">A keyword from  `Keywords_cyprus_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_passport_number" />
          <Match idRef="Keywords_cyprus_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0285a-197">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="0285a-197">Keywords</span></span>

<span data-ttu-id="0285a-198">| |</span><span class="sxs-lookup"><span data-stu-id="0285a-198"></span></span>
|<span data-ttu-id="0285a-199">**Keywords_cyprus_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="0285a-199">**Keywords_cyprus_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="0285a-200">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="0285a-200">passport number</span></span>  <br/> <span data-ttu-id="0285a-201">número de passaporte do Chipre</span><span class="sxs-lookup"><span data-stu-id="0285a-201">cyprus passport number</span></span>  <br/> <span data-ttu-id="0285a-202">Passport não</span><span class="sxs-lookup"><span data-stu-id="0285a-202">passport no</span></span>  <br/> <span data-ttu-id="0285a-203">αριθμό διαβατηρίου</span><span class="sxs-lookup"><span data-stu-id="0285a-203">αριθμό διαβατηρίου</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="0285a-204">República Tcheca</span><span class="sxs-lookup"><span data-stu-id="0285a-204">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="0285a-205">Formato</span><span class="sxs-lookup"><span data-stu-id="0285a-205">Format</span></span>

<span data-ttu-id="0285a-206">Oito dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="0285a-206">Eight digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0285a-207">Padrão</span><span class="sxs-lookup"><span data-stu-id="0285a-207">Pattern</span></span>

<span data-ttu-id="0285a-208">Oito dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="0285a-208">Eight digits without spaces or delimiters</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0285a-209">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="0285a-209">Checksum</span></span>

<span data-ttu-id="0285a-210">Não</span><span class="sxs-lookup"><span data-stu-id="0285a-210">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="0285a-211">Definição</span><span class="sxs-lookup"><span data-stu-id="0285a-211">Definition</span></span>

<span data-ttu-id="0285a-212">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="0285a-212">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0285a-213">A expressão `Regex_czech_republic_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="0285a-213">The regular expression  `Regex_czech_republic_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0285a-214">Uma palavra- `Keywords_czech_republic_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="0285a-214">A keyword from  `Keywords_czech_republic_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_passport_number" />
          <Match idRef="Keywords_czech_republic_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0285a-215">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="0285a-215">Keywords</span></span>

<span data-ttu-id="0285a-216">| |</span><span class="sxs-lookup"><span data-stu-id="0285a-216"></span></span>
|<span data-ttu-id="0285a-217">**Keywords_czech_republic_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="0285a-217">**Keywords_czech_republic_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="0285a-218">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="0285a-218">passport number</span></span>  <br/> <span data-ttu-id="0285a-219">número de passaporte tcheco</span><span class="sxs-lookup"><span data-stu-id="0285a-219">czech passport number</span></span>  <br/> <span data-ttu-id="0285a-220">Passport não</span><span class="sxs-lookup"><span data-stu-id="0285a-220">passport no</span></span>  <br/> <span data-ttu-id="0285a-221">Pas cestovní</span><span class="sxs-lookup"><span data-stu-id="0285a-221">cestovní pas</span></span>  <br/> <span data-ttu-id="0285a-222">Pas</span><span class="sxs-lookup"><span data-stu-id="0285a-222">pas</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="0285a-223">Dinamarca</span><span class="sxs-lookup"><span data-stu-id="0285a-223">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="0285a-224">Formato</span><span class="sxs-lookup"><span data-stu-id="0285a-224">Format</span></span>

<span data-ttu-id="0285a-225">Nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="0285a-225">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0285a-226">Padrão</span><span class="sxs-lookup"><span data-stu-id="0285a-226">Pattern</span></span>

 <span data-ttu-id="0285a-227">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="0285a-227">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="0285a-228">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="0285a-228">Checksum</span></span>

<span data-ttu-id="0285a-229">Não</span><span class="sxs-lookup"><span data-stu-id="0285a-229">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="0285a-230">Definição</span><span class="sxs-lookup"><span data-stu-id="0285a-230">Definition</span></span>

<span data-ttu-id="0285a-231">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="0285a-231">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0285a-232">A expressão `Regex_denmark_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="0285a-232">The regular expression  `Regex_denmark_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0285a-233">Uma palavra- `Keywords_denmark_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="0285a-233">A keyword from  `Keywords_denmark_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_passport_number" />
          <Match idRef="Keywords_denmark_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0285a-234">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="0285a-234">Keywords</span></span>

<span data-ttu-id="0285a-235">| |</span><span class="sxs-lookup"><span data-stu-id="0285a-235"></span></span>
|<span data-ttu-id="0285a-236">**Keywords_denmark_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="0285a-236">**Keywords_denmark_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="0285a-237">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="0285a-237">passport number</span></span>  <br/> <span data-ttu-id="0285a-238">número de passaporte dinamarquês</span><span class="sxs-lookup"><span data-stu-id="0285a-238">danish passport number</span></span>  <br/> <span data-ttu-id="0285a-239">Passport não</span><span class="sxs-lookup"><span data-stu-id="0285a-239">passport no</span></span>  <br/> <span data-ttu-id="0285a-240">Pas</span><span class="sxs-lookup"><span data-stu-id="0285a-240">pas</span></span>  <br/> <span data-ttu-id="0285a-241">pasnummer</span><span class="sxs-lookup"><span data-stu-id="0285a-241">pasnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="0285a-242">Estônia</span><span class="sxs-lookup"><span data-stu-id="0285a-242">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="0285a-243">Formato</span><span class="sxs-lookup"><span data-stu-id="0285a-243">Format</span></span>

<span data-ttu-id="0285a-244">Uma letra seguida por sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="0285a-244">One letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0285a-245">Padrão</span><span class="sxs-lookup"><span data-stu-id="0285a-245">Pattern</span></span>

<span data-ttu-id="0285a-246">Uma letra seguida por sete dígitos</span><span class="sxs-lookup"><span data-stu-id="0285a-246">One letter followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0285a-247">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="0285a-247">Checksum</span></span>

<span data-ttu-id="0285a-248">Não</span><span class="sxs-lookup"><span data-stu-id="0285a-248">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="0285a-249">Definição</span><span class="sxs-lookup"><span data-stu-id="0285a-249">Definition</span></span>

<span data-ttu-id="0285a-250">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="0285a-250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0285a-251">A expressão `Regex_estonia_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="0285a-251">The regular expression  `Regex_estonia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0285a-252">Uma palavra- `Keywords_estonia_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="0285a-252">A keyword from  `Keywords_estonia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_passport_number" />
          <Match idRef="Keywords_estonia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0285a-253">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="0285a-253">Keywords</span></span>

<span data-ttu-id="0285a-254">| |</span><span class="sxs-lookup"><span data-stu-id="0285a-254"></span></span>
|<span data-ttu-id="0285a-255">**Keywords_estonia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="0285a-255">**Keywords_estonia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="0285a-256">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="0285a-256">passport number</span></span>  <br/> <span data-ttu-id="0285a-257">número de passaporte estoniano</span><span class="sxs-lookup"><span data-stu-id="0285a-257">estonian passport number</span></span>  <br/> <span data-ttu-id="0285a-258">Passport não</span><span class="sxs-lookup"><span data-stu-id="0285a-258">passport no</span></span>  <br/> <span data-ttu-id="0285a-259">Eesti kodaniku</span><span class="sxs-lookup"><span data-stu-id="0285a-259">eesti kodaniku pass</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="0285a-260">Finlândia</span><span class="sxs-lookup"><span data-stu-id="0285a-260">Finland</span></span>

<span data-ttu-id="0285a-261">Para obter detalhes, consulte a seção "número de passaporte da Finlândia" em [o que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="0285a-261">For details, see the section "Finland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="0285a-262">França</span><span class="sxs-lookup"><span data-stu-id="0285a-262">France</span></span>

<span data-ttu-id="0285a-263">Para obter detalhes, consulte a seção "número do passaporte da França" em [o que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="0285a-263">For details, see the section "France Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="0285a-264">Alemanha</span><span class="sxs-lookup"><span data-stu-id="0285a-264">Germany</span></span>

<span data-ttu-id="0285a-265">Para obter detalhes, consulte a seção "número de passaporte da Alemanha" em [o que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="0285a-265">For details, see the section "Germany Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="0285a-266">Grécia</span><span class="sxs-lookup"><span data-stu-id="0285a-266">Greece</span></span>

### <a name="format"></a><span data-ttu-id="0285a-267">Formato</span><span class="sxs-lookup"><span data-stu-id="0285a-267">Format</span></span>

<span data-ttu-id="0285a-268">Duas letras seguidas por sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="0285a-268">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0285a-269">Padrão</span><span class="sxs-lookup"><span data-stu-id="0285a-269">Pattern</span></span>

<span data-ttu-id="0285a-270">Duas letras seguidas por sete dígitos</span><span class="sxs-lookup"><span data-stu-id="0285a-270">Two letters followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0285a-271">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="0285a-271">Checksum</span></span>

<span data-ttu-id="0285a-272">Não</span><span class="sxs-lookup"><span data-stu-id="0285a-272">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="0285a-273">Definição</span><span class="sxs-lookup"><span data-stu-id="0285a-273">Definition</span></span>

<span data-ttu-id="0285a-274">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="0285a-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0285a-275">A expressão `Regex_greece_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="0285a-275">The regular expression  `Regex_greece_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0285a-276">Uma palavra- `Keywords_greece_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="0285a-276">A keyword from  `Keywords_greece_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_passport_number" />
          <Match idRef="Keywords_greece_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0285a-277">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="0285a-277">Keywords</span></span>

<span data-ttu-id="0285a-278">| |</span><span class="sxs-lookup"><span data-stu-id="0285a-278"></span></span>
|<span data-ttu-id="0285a-279">**Keywords_greece_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="0285a-279">**Keywords_greece_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="0285a-280">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="0285a-280">passport number</span></span>  <br/> <span data-ttu-id="0285a-281">número de passaporte grego</span><span class="sxs-lookup"><span data-stu-id="0285a-281">greek passport number</span></span>  <br/> <span data-ttu-id="0285a-282">Passport não</span><span class="sxs-lookup"><span data-stu-id="0285a-282">passport no</span></span>  <br/> <span data-ttu-id="0285a-283">διαβατηριο</span><span class="sxs-lookup"><span data-stu-id="0285a-283">διαβατηριο</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="0285a-284">Hungria</span><span class="sxs-lookup"><span data-stu-id="0285a-284">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="0285a-285">Formato</span><span class="sxs-lookup"><span data-stu-id="0285a-285">Format</span></span>

<span data-ttu-id="0285a-286">Duas letras seguidas por seis ou sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="0285a-286">Two letters followed by six or seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0285a-287">Padrão</span><span class="sxs-lookup"><span data-stu-id="0285a-287">Pattern</span></span>

<span data-ttu-id="0285a-288">Duas letras seguidas por seis ou sete dígitos</span><span class="sxs-lookup"><span data-stu-id="0285a-288">Two letters followed by six or seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0285a-289">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="0285a-289">Checksum</span></span>

<span data-ttu-id="0285a-290">Não</span><span class="sxs-lookup"><span data-stu-id="0285a-290">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="0285a-291">Definição</span><span class="sxs-lookup"><span data-stu-id="0285a-291">Definition</span></span>

<span data-ttu-id="0285a-292">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="0285a-292">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0285a-293">A expressão `Regex_hungary_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="0285a-293">The regular expression  `Regex_hungary_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0285a-294">Uma palavra- `Keywords_hungary_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="0285a-294">A keyword from  `Keywords_hungary_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_passport_number" />
          <Match idRef="Keywords_hungary_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0285a-295">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="0285a-295">Keywords</span></span>

<span data-ttu-id="0285a-296">| |</span><span class="sxs-lookup"><span data-stu-id="0285a-296"></span></span>
|<span data-ttu-id="0285a-297">**Keywords_hungary_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="0285a-297">**Keywords_hungary_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="0285a-298">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="0285a-298">passport number</span></span>  <br/> <span data-ttu-id="0285a-299">número de passaporte húngaro</span><span class="sxs-lookup"><span data-stu-id="0285a-299">hungarian passport number</span></span>  <br/> <span data-ttu-id="0285a-300">Passport não</span><span class="sxs-lookup"><span data-stu-id="0285a-300">passport no</span></span>  <br/> <span data-ttu-id="0285a-301">útlevél száma</span><span class="sxs-lookup"><span data-stu-id="0285a-301">útlevél száma</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="0285a-302">Irlanda</span><span class="sxs-lookup"><span data-stu-id="0285a-302">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="0285a-303">Formato</span><span class="sxs-lookup"><span data-stu-id="0285a-303">Format</span></span>

<span data-ttu-id="0285a-304">Duas letras ou dígitos seguidos de sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="0285a-304">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0285a-305">Padrão</span><span class="sxs-lookup"><span data-stu-id="0285a-305">Pattern</span></span>

<span data-ttu-id="0285a-306">Duas letras ou dígitos seguidos por sete dígitos:</span><span class="sxs-lookup"><span data-stu-id="0285a-306">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="0285a-307">Dois dígitos ou letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="0285a-307">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="0285a-308">Sete dígitos</span><span class="sxs-lookup"><span data-stu-id="0285a-308">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0285a-309">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="0285a-309">Checksum</span></span>

<span data-ttu-id="0285a-310">Não</span><span class="sxs-lookup"><span data-stu-id="0285a-310">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="0285a-311">Definição</span><span class="sxs-lookup"><span data-stu-id="0285a-311">Definition</span></span>

<span data-ttu-id="0285a-312">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="0285a-312">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0285a-313">A expressão `Regex_ireland_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="0285a-313">The regular expression  `Regex_ireland_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0285a-314">Uma palavra- `Keywords_ireland_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="0285a-314">A keyword from  `Keywords_ireland_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_passport_number" />
          <Match idRef="Keywords_ireland_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0285a-315">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="0285a-315">Keywords</span></span>

<span data-ttu-id="0285a-316">| |</span><span class="sxs-lookup"><span data-stu-id="0285a-316"></span></span>
|<span data-ttu-id="0285a-317">**Keywords_ireland_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="0285a-317">**Keywords_ireland_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="0285a-318">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="0285a-318">passport number</span></span>  <br/> <span data-ttu-id="0285a-319">número de passaporte do irlandês</span><span class="sxs-lookup"><span data-stu-id="0285a-319">irish passport number</span></span>  <br/> <span data-ttu-id="0285a-320">Passport não</span><span class="sxs-lookup"><span data-stu-id="0285a-320">passport no</span></span>  <br/> <span data-ttu-id="0285a-321">Pas</span><span class="sxs-lookup"><span data-stu-id="0285a-321">pas</span></span>  <br/> <span data-ttu-id="0285a-322">passport</span><span class="sxs-lookup"><span data-stu-id="0285a-322">passport</span></span>  <br/> <span data-ttu-id="0285a-323">passeport</span><span class="sxs-lookup"><span data-stu-id="0285a-323">passeport</span></span>  <br/> <span data-ttu-id="0285a-324">passeport numero</span><span class="sxs-lookup"><span data-stu-id="0285a-324">passeport numero</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="0285a-325">Itália</span><span class="sxs-lookup"><span data-stu-id="0285a-325">Italy</span></span>

### <a name="format"></a><span data-ttu-id="0285a-326">Formato</span><span class="sxs-lookup"><span data-stu-id="0285a-326">Format</span></span>

<span data-ttu-id="0285a-327">Duas letras ou dígitos seguidos de sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="0285a-327">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0285a-328">Padrão</span><span class="sxs-lookup"><span data-stu-id="0285a-328">Pattern</span></span>

<span data-ttu-id="0285a-329">Duas letras ou dígitos seguidos por sete dígitos:</span><span class="sxs-lookup"><span data-stu-id="0285a-329">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="0285a-330">Dois dígitos ou letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="0285a-330">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="0285a-331">Sete dígitos</span><span class="sxs-lookup"><span data-stu-id="0285a-331">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0285a-332">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="0285a-332">Checksum</span></span>

<span data-ttu-id="0285a-333">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="0285a-333">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="0285a-334">Definição</span><span class="sxs-lookup"><span data-stu-id="0285a-334">Definition</span></span>

<span data-ttu-id="0285a-335">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="0285a-335">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0285a-336">A expressão `Regex_italy_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="0285a-336">The regular expression  `Regex_italy_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0285a-337">Uma palavra- `Keywords_italy_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="0285a-337">A keyword from  `Keywords_italy_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_passport_number" />
          <Match idRef="Keywords_italy_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0285a-338">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="0285a-338">Keywords</span></span>

<span data-ttu-id="0285a-339">| |</span><span class="sxs-lookup"><span data-stu-id="0285a-339"></span></span>
|<span data-ttu-id="0285a-340">**Keywords_italy_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="0285a-340">**Keywords_italy_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="0285a-341">número de passaporte italiano</span><span class="sxs-lookup"><span data-stu-id="0285a-341">italian passport number</span></span>  <br/> <span data-ttu-id="0285a-342">Repubblica Italiana PASSAPORTO</span><span class="sxs-lookup"><span data-stu-id="0285a-342">repubblica italiana passaporto</span></span>  <br/> <span data-ttu-id="0285a-343">PASSAPORTO</span><span class="sxs-lookup"><span data-stu-id="0285a-343">passaporto</span></span>  <br/> <span data-ttu-id="0285a-344">PASSAPORTO italiana</span><span class="sxs-lookup"><span data-stu-id="0285a-344">passaporto italiana</span></span>  <br/> <span data-ttu-id="0285a-345">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="0285a-345">passport number</span></span>  <br/> <span data-ttu-id="0285a-346">italiana PASSAPORTO numero</span><span class="sxs-lookup"><span data-stu-id="0285a-346">italiana passaporto numero</span></span>  <br/> <span data-ttu-id="0285a-347">PASSAPORTO numero</span><span class="sxs-lookup"><span data-stu-id="0285a-347">passaporto numero</span></span>  <br/> <span data-ttu-id="0285a-348">Numéro passeport Italien</span><span class="sxs-lookup"><span data-stu-id="0285a-348">numéro passeport italien</span></span>  <br/> <span data-ttu-id="0285a-349">Numéro passeport</span><span class="sxs-lookup"><span data-stu-id="0285a-349">numéro passeport</span></span>  <br/> |
   
## <a name="latvia"></a><span data-ttu-id="0285a-350">Letônia</span><span class="sxs-lookup"><span data-stu-id="0285a-350">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="0285a-351">Formato</span><span class="sxs-lookup"><span data-stu-id="0285a-351">Format</span></span>

<span data-ttu-id="0285a-352">Duas letras ou dígitos seguidos de sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="0285a-352">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0285a-353">Padrão</span><span class="sxs-lookup"><span data-stu-id="0285a-353">Pattern</span></span>

<span data-ttu-id="0285a-354">Duas letras ou dígitos seguidos por sete dígitos:</span><span class="sxs-lookup"><span data-stu-id="0285a-354">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="0285a-355">Dois dígitos ou letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="0285a-355">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="0285a-356">Sete dígitos</span><span class="sxs-lookup"><span data-stu-id="0285a-356">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0285a-357">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="0285a-357">Checksum</span></span>

<span data-ttu-id="0285a-358">Não</span><span class="sxs-lookup"><span data-stu-id="0285a-358">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="0285a-359">Definição</span><span class="sxs-lookup"><span data-stu-id="0285a-359">Definition</span></span>

<span data-ttu-id="0285a-360">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="0285a-360">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0285a-361">A expressão `Regex_latvia_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="0285a-361">The regular expression  `Regex_latvia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0285a-362">Uma palavra- `Keywords_latvia_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="0285a-362">A keyword from  `Keywords_latvia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_passport_number" />
          <Match idRef="Keywords_latvia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0285a-363">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="0285a-363">Keywords</span></span>

<span data-ttu-id="0285a-364">| |</span><span class="sxs-lookup"><span data-stu-id="0285a-364"></span></span>
|<span data-ttu-id="0285a-365">**Keywords_latvia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="0285a-365">**Keywords_latvia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="0285a-366">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="0285a-366">passport number</span></span>  <br/> <span data-ttu-id="0285a-367">número de passaporte da Letão</span><span class="sxs-lookup"><span data-stu-id="0285a-367">latvian passport number</span></span>  <br/> <span data-ttu-id="0285a-368">Passport não</span><span class="sxs-lookup"><span data-stu-id="0285a-368">passport no</span></span>  <br/> <span data-ttu-id="0285a-369">pase numurs</span><span class="sxs-lookup"><span data-stu-id="0285a-369">pase numurs</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="0285a-370">Lituânia</span><span class="sxs-lookup"><span data-stu-id="0285a-370">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="0285a-371">Formato</span><span class="sxs-lookup"><span data-stu-id="0285a-371">Format</span></span>

<span data-ttu-id="0285a-372">Oito dígitos ou letras sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="0285a-372">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0285a-373">Padrão</span><span class="sxs-lookup"><span data-stu-id="0285a-373">Pattern</span></span>

<span data-ttu-id="0285a-374">Oito dígitos ou letras (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="0285a-374">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0285a-375">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="0285a-375">Checksum</span></span>

<span data-ttu-id="0285a-376">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="0285a-376">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="0285a-377">Definição</span><span class="sxs-lookup"><span data-stu-id="0285a-377">Definition</span></span>

<span data-ttu-id="0285a-378">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="0285a-378">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0285a-379">A expressão `Regex_lithuania_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="0285a-379">The regular expression  `Regex_lithuania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0285a-380">Uma palavra- `Keywords_lithuania_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="0285a-380">A keyword from  `Keywords_lithuania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_passport_number" />
          <Match idRef="Keywords_lithuania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0285a-381">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="0285a-381">Keywords</span></span>

<span data-ttu-id="0285a-382">| |</span><span class="sxs-lookup"><span data-stu-id="0285a-382"></span></span>
|<span data-ttu-id="0285a-383">**Keywords_lithuania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="0285a-383">**Keywords_lithuania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="0285a-384">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="0285a-384">passport number</span></span>  <br/> <span data-ttu-id="0285a-385">número de passaporte lithunian</span><span class="sxs-lookup"><span data-stu-id="0285a-385">lithunian passport number</span></span>  <br/> <span data-ttu-id="0285a-386">Passport não</span><span class="sxs-lookup"><span data-stu-id="0285a-386">passport no</span></span>  <br/> <span data-ttu-id="0285a-387">Paso Numeris</span><span class="sxs-lookup"><span data-stu-id="0285a-387">paso numeris</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="0285a-388">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="0285a-388">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="0285a-389">Formato</span><span class="sxs-lookup"><span data-stu-id="0285a-389">Format</span></span>

<span data-ttu-id="0285a-390">Oito dígitos ou letras sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="0285a-390">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0285a-391">Padrão</span><span class="sxs-lookup"><span data-stu-id="0285a-391">Pattern</span></span>

<span data-ttu-id="0285a-392">Oito dígitos ou letras (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="0285a-392">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0285a-393">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="0285a-393">Checksum</span></span>

<span data-ttu-id="0285a-394">Não</span><span class="sxs-lookup"><span data-stu-id="0285a-394">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="0285a-395">Definição</span><span class="sxs-lookup"><span data-stu-id="0285a-395">Definition</span></span>

<span data-ttu-id="0285a-396">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="0285a-396">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0285a-397">A expressão `Regex_nation_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="0285a-397">The regular expression  `Regex_nation_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0285a-398">Uma palavra- `Keywords_nation_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="0285a-398">A keyword from  `Keywords_nation_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_nation_eu_passport_number" />
          <Match idRef="Keywords_nation_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0285a-399">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="0285a-399">Keywords</span></span>

<span data-ttu-id="0285a-400">| |</span><span class="sxs-lookup"><span data-stu-id="0285a-400"></span></span>
|<span data-ttu-id="0285a-401">**Keywords_nation_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="0285a-401">**Keywords_nation_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="0285a-402">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="0285a-402">passport number</span></span>  <br/> <span data-ttu-id="0285a-403">número de passaporte da Letão</span><span class="sxs-lookup"><span data-stu-id="0285a-403">latvian passport number</span></span>  <br/> <span data-ttu-id="0285a-404">Passport não</span><span class="sxs-lookup"><span data-stu-id="0285a-404">passport no</span></span>  <br/> <span data-ttu-id="0285a-405">passnummer</span><span class="sxs-lookup"><span data-stu-id="0285a-405">passnummer</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="0285a-406">Malta</span><span class="sxs-lookup"><span data-stu-id="0285a-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="0285a-407">Formato</span><span class="sxs-lookup"><span data-stu-id="0285a-407">Format</span></span>

<span data-ttu-id="0285a-408">Sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="0285a-408">Seven digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0285a-409">Padrão</span><span class="sxs-lookup"><span data-stu-id="0285a-409">Pattern</span></span>

 <span data-ttu-id="0285a-410">Sete dígitos</span><span class="sxs-lookup"><span data-stu-id="0285a-410">Seven digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="0285a-411">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="0285a-411">Checksum</span></span>

<span data-ttu-id="0285a-412">Não</span><span class="sxs-lookup"><span data-stu-id="0285a-412">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="0285a-413">Definição</span><span class="sxs-lookup"><span data-stu-id="0285a-413">Definition</span></span>

<span data-ttu-id="0285a-414">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="0285a-414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0285a-415">A expressão `Regex_malta_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="0285a-415">The regular expression  `Regex_malta_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0285a-416">Uma palavra- `Keywords_malta_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="0285a-416">A keyword from  `Keywords_malta_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_passport_number" />
          <Match idRef="Keywords_malta_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0285a-417">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="0285a-417">Keywords</span></span>

<span data-ttu-id="0285a-418">| |</span><span class="sxs-lookup"><span data-stu-id="0285a-418"></span></span>
|<span data-ttu-id="0285a-419">**Keywords_malta_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="0285a-419">**Keywords_malta_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="0285a-420">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="0285a-420">passport number</span></span>  <br/> <span data-ttu-id="0285a-421">número de passaporte Maltês</span><span class="sxs-lookup"><span data-stu-id="0285a-421">maltese passport number</span></span>  <br/> <span data-ttu-id="0285a-422">Passport não</span><span class="sxs-lookup"><span data-stu-id="0285a-422">passport no</span></span>  <br/> <span data-ttu-id="0285a-423">numru tal-Passaport</span><span class="sxs-lookup"><span data-stu-id="0285a-423">numru tal-passaport</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="0285a-424">Países Baixos</span><span class="sxs-lookup"><span data-stu-id="0285a-424">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="0285a-425">Formato</span><span class="sxs-lookup"><span data-stu-id="0285a-425">Format</span></span>

<span data-ttu-id="0285a-426">Nove letras ou dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="0285a-426">Nine letters or digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0285a-427">Padrão</span><span class="sxs-lookup"><span data-stu-id="0285a-427">Pattern</span></span>

<span data-ttu-id="0285a-428">Nove letras ou dígitos</span><span class="sxs-lookup"><span data-stu-id="0285a-428">Nine letters or digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0285a-429">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="0285a-429">Checksum</span></span>

<span data-ttu-id="0285a-430">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="0285a-430">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="0285a-431">Definição</span><span class="sxs-lookup"><span data-stu-id="0285a-431">Definition</span></span>

<span data-ttu-id="0285a-432">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="0285a-432">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0285a-433">A expressão `Regex_netherlands_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="0285a-433">The regular expression  `Regex_netherlands_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0285a-434">Uma palavra- `Keywords_netherlands_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="0285a-434">A keyword from  `Keywords_netherlands_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_passport_number" />
          <Match idRef="Keywords_netherlands_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0285a-435">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="0285a-435">Keywords</span></span>

<span data-ttu-id="0285a-436">| |</span><span class="sxs-lookup"><span data-stu-id="0285a-436"></span></span>
|<span data-ttu-id="0285a-437">**Keywords_netherlands_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="0285a-437">**Keywords_netherlands_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="0285a-438">número de passaporte holandês</span><span class="sxs-lookup"><span data-stu-id="0285a-438">dutch passport number</span></span>  <br/> <span data-ttu-id="0285a-439">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="0285a-439">passport number</span></span>  <br/> <span data-ttu-id="0285a-440">número de passaporte Holanda</span><span class="sxs-lookup"><span data-stu-id="0285a-440">netherlands passport number</span></span>  <br/> <span data-ttu-id="0285a-441">Nederlanden paspoort Nummer</span><span class="sxs-lookup"><span data-stu-id="0285a-441">nederlanden paspoort nummer</span></span>  <br/> <span data-ttu-id="0285a-442">paspoort</span><span class="sxs-lookup"><span data-stu-id="0285a-442">paspoort</span></span>  <br/> <span data-ttu-id="0285a-443">Nederlanden paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="0285a-443">nederlanden paspoortnummer</span></span>  <br/> <span data-ttu-id="0285a-444">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="0285a-444">paspoortnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="0285a-445">Polônia</span><span class="sxs-lookup"><span data-stu-id="0285a-445">Poland</span></span>

<span data-ttu-id="0285a-446">Para obter detalhes, consulte a seção "número de passaporte da Polônia" em [o que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="0285a-446">For details, see the section "Poland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="0285a-447">Portugal</span><span class="sxs-lookup"><span data-stu-id="0285a-447">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="0285a-448">Formato</span><span class="sxs-lookup"><span data-stu-id="0285a-448">Format</span></span>

<span data-ttu-id="0285a-449">Uma letra seguida de seis dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="0285a-449">One letter followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0285a-450">Padrão</span><span class="sxs-lookup"><span data-stu-id="0285a-450">Pattern</span></span>

<span data-ttu-id="0285a-451">Uma letra seguida por seis dígitos:</span><span class="sxs-lookup"><span data-stu-id="0285a-451">One letter followed by six digits:</span></span>
  
- <span data-ttu-id="0285a-452">Uma letra (não diferencia maiúscula de minúscula)</span><span class="sxs-lookup"><span data-stu-id="0285a-452">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="0285a-453">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="0285a-453">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0285a-454">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="0285a-454">Checksum</span></span>

<span data-ttu-id="0285a-455">Não</span><span class="sxs-lookup"><span data-stu-id="0285a-455">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="0285a-456">Definição</span><span class="sxs-lookup"><span data-stu-id="0285a-456">Definition</span></span>

<span data-ttu-id="0285a-457">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="0285a-457">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0285a-458">A expressão `Regex_portugal_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="0285a-458">The regular expression  `Regex_portugal_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0285a-459">Uma palavra- `Keywords_portugal_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="0285a-459">A keyword from  `Keywords_portugal_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_passport_number" />
          <Match idRef="Keywords_portugal_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0285a-460">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="0285a-460">Keywords</span></span>

<span data-ttu-id="0285a-461">| |</span><span class="sxs-lookup"><span data-stu-id="0285a-461"></span></span>
|<span data-ttu-id="0285a-462">**Keywords_portugal_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="0285a-462">**Keywords_portugal_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="0285a-463">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="0285a-463">passport number</span></span>  <br/> <span data-ttu-id="0285a-464">número de passaporte Português</span><span class="sxs-lookup"><span data-stu-id="0285a-464">portuguese passport number</span></span>  <br/> <span data-ttu-id="0285a-465">Passport não</span><span class="sxs-lookup"><span data-stu-id="0285a-465">passport no</span></span>  <br/> <span data-ttu-id="0285a-466">número do passaporte</span><span class="sxs-lookup"><span data-stu-id="0285a-466">número do passaporte</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="0285a-467">Romênia</span><span class="sxs-lookup"><span data-stu-id="0285a-467">Romania</span></span>

### <a name="format"></a><span data-ttu-id="0285a-468">Formato</span><span class="sxs-lookup"><span data-stu-id="0285a-468">Format</span></span>

<span data-ttu-id="0285a-469">Oito ou nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="0285a-469">Eight or nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0285a-470">Padrão</span><span class="sxs-lookup"><span data-stu-id="0285a-470">Pattern</span></span>

<span data-ttu-id="0285a-471">Oito ou nove dígitos</span><span class="sxs-lookup"><span data-stu-id="0285a-471">Eight or nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0285a-472">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="0285a-472">Checksum</span></span>

<span data-ttu-id="0285a-473">Não</span><span class="sxs-lookup"><span data-stu-id="0285a-473">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="0285a-474">Definição</span><span class="sxs-lookup"><span data-stu-id="0285a-474">Definition</span></span>

<span data-ttu-id="0285a-475">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="0285a-475">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0285a-476">A expressão `Regex_romania_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="0285a-476">The regular expression  `Regex_romania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0285a-477">Uma palavra- `Keywords_romania_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="0285a-477">A keyword from  `Keywords_romania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_passport_number" />
          <Match idRef="Keywords_romania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0285a-478">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="0285a-478">Keywords</span></span>

<span data-ttu-id="0285a-479">| |</span><span class="sxs-lookup"><span data-stu-id="0285a-479"></span></span>
|<span data-ttu-id="0285a-480">**Keywords_romania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="0285a-480">**Keywords_romania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="0285a-481">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="0285a-481">passport number</span></span>  <br/> <span data-ttu-id="0285a-482">número de passaporte romeno</span><span class="sxs-lookup"><span data-stu-id="0285a-482">romanian passport number</span></span>  <br/> <span data-ttu-id="0285a-483">Passport não</span><span class="sxs-lookup"><span data-stu-id="0285a-483">passport no</span></span>  <br/> <span data-ttu-id="0285a-484">numărul pașaportului</span><span class="sxs-lookup"><span data-stu-id="0285a-484">numărul pașaportului</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="0285a-485">Eslováquia</span><span class="sxs-lookup"><span data-stu-id="0285a-485">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="0285a-486">Formato</span><span class="sxs-lookup"><span data-stu-id="0285a-486">Format</span></span>

<span data-ttu-id="0285a-487">Um dígito ou letra seguido por sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="0285a-487">One digit or letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0285a-488">Padrão</span><span class="sxs-lookup"><span data-stu-id="0285a-488">Pattern</span></span>

<span data-ttu-id="0285a-489">Um dígito ou letra (não diferencia maiúsculas de minúsculas) seguido por sete dígitos</span><span class="sxs-lookup"><span data-stu-id="0285a-489">One digit or letter (not case sensitive) followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0285a-490">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="0285a-490">Checksum</span></span>

<span data-ttu-id="0285a-491">Não</span><span class="sxs-lookup"><span data-stu-id="0285a-491">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="0285a-492">Definição</span><span class="sxs-lookup"><span data-stu-id="0285a-492">Definition</span></span>

<span data-ttu-id="0285a-493">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="0285a-493">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0285a-494">A expressão `Regex_slovakia_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="0285a-494">The regular expression  `Regex_slovakia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0285a-495">Uma palavra- `Keywords_slovakia_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="0285a-495">A keyword from  `Keywords_slovakia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_passport_number" />
          <Match idRef="Keywords_slovakia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0285a-496">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="0285a-496">Keywords</span></span>

<span data-ttu-id="0285a-497">| |</span><span class="sxs-lookup"><span data-stu-id="0285a-497"></span></span>
|<span data-ttu-id="0285a-498">**Keywords_slovakia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="0285a-498">**Keywords_slovakia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="0285a-499">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="0285a-499">passport number</span></span>  <br/> <span data-ttu-id="0285a-500">número de passaporte eslovaco</span><span class="sxs-lookup"><span data-stu-id="0285a-500">slovakian passport number</span></span>  <br/> <span data-ttu-id="0285a-501">Passport não</span><span class="sxs-lookup"><span data-stu-id="0285a-501">passport no</span></span>  <br/> <span data-ttu-id="0285a-502">číslo Pasu</span><span class="sxs-lookup"><span data-stu-id="0285a-502">číslo pasu</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="0285a-503">Eslovênia</span><span class="sxs-lookup"><span data-stu-id="0285a-503">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="0285a-504">Formato</span><span class="sxs-lookup"><span data-stu-id="0285a-504">Format</span></span>

<span data-ttu-id="0285a-505">Duas letras seguidas por sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="0285a-505">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0285a-506">Padrão</span><span class="sxs-lookup"><span data-stu-id="0285a-506">Pattern</span></span>

<span data-ttu-id="0285a-507">Duas letras seguidas por sete dígitos:</span><span class="sxs-lookup"><span data-stu-id="0285a-507">Two letters followed by seven digits:</span></span>
  
- <span data-ttu-id="0285a-508">A letra "P"</span><span class="sxs-lookup"><span data-stu-id="0285a-508">The letter "P"</span></span>
    
- <span data-ttu-id="0285a-509">Uma letra maiúscula</span><span class="sxs-lookup"><span data-stu-id="0285a-509">One uppercase letter</span></span>
    
- <span data-ttu-id="0285a-510">Sete dígitos</span><span class="sxs-lookup"><span data-stu-id="0285a-510">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0285a-511">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="0285a-511">Checksum</span></span>

<span data-ttu-id="0285a-512">Não</span><span class="sxs-lookup"><span data-stu-id="0285a-512">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="0285a-513">Definição</span><span class="sxs-lookup"><span data-stu-id="0285a-513">Definition</span></span>

<span data-ttu-id="0285a-514">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="0285a-514">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0285a-515">A expressão `Regex_slovenia_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="0285a-515">The regular expression  `Regex_slovenia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0285a-516">Uma palavra- `Keywords_slovenia_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="0285a-516">A keyword from  `Keywords_slovenia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_passport_number" />
          <Match idRef="Keywords_slovenia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0285a-517">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="0285a-517">Keywords</span></span>

<span data-ttu-id="0285a-518">| |</span><span class="sxs-lookup"><span data-stu-id="0285a-518"></span></span>
|<span data-ttu-id="0285a-519">**Keywords_slovenia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="0285a-519">**Keywords_slovenia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="0285a-520">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="0285a-520">passport number</span></span>  <br/> <span data-ttu-id="0285a-521">número de passaporte esloveno</span><span class="sxs-lookup"><span data-stu-id="0285a-521">slovenian passport number</span></span>  <br/> <span data-ttu-id="0285a-522">Passport não</span><span class="sxs-lookup"><span data-stu-id="0285a-522">passport no</span></span>  <br/> <span data-ttu-id="0285a-523">lista de številka potnega</span><span class="sxs-lookup"><span data-stu-id="0285a-523">številka potnega lista</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="0285a-524">Espanha</span><span class="sxs-lookup"><span data-stu-id="0285a-524">Spain</span></span>

### <a name="format"></a><span data-ttu-id="0285a-525">Formato</span><span class="sxs-lookup"><span data-stu-id="0285a-525">Format</span></span>

<span data-ttu-id="0285a-526">Uma combinação de letras e números de oito ou nove caracteres sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="0285a-526">An eight- or nine-character combination of letters and numbers with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0285a-527">Padrão</span><span class="sxs-lookup"><span data-stu-id="0285a-527">Pattern</span></span>

<span data-ttu-id="0285a-528">Uma combinação de letras e números de oito ou nove caracteres:</span><span class="sxs-lookup"><span data-stu-id="0285a-528">An eight- or nine-character combination of letters and numbers:</span></span>
  
-  <span data-ttu-id="0285a-529">Dois dígitos ou letras</span><span class="sxs-lookup"><span data-stu-id="0285a-529">Two digits or letters</span></span> 
    
- <span data-ttu-id="0285a-530">Um dígito ou letra (opcional)</span><span class="sxs-lookup"><span data-stu-id="0285a-530">One digit or letter (optional)</span></span>
    
- <span data-ttu-id="0285a-531">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="0285a-531">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0285a-532">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="0285a-532">Checksum</span></span>

<span data-ttu-id="0285a-533">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="0285a-533">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="0285a-534">Definição</span><span class="sxs-lookup"><span data-stu-id="0285a-534">Definition</span></span>

<span data-ttu-id="0285a-535">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="0285a-535">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0285a-536">A expressão `Regex_spain_eu_passport_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="0285a-536">The regular expression  `Regex_spain_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0285a-537">Uma palavra- `Keywords_spain_eu_passport_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="0285a-537">A keyword from  `Keywords_spain_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_passport_number" />
          <Match idRef="Keywords_spain_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0285a-538">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="0285a-538">Keywords</span></span>

<span data-ttu-id="0285a-539">| |</span><span class="sxs-lookup"><span data-stu-id="0285a-539"></span></span>
|<span data-ttu-id="0285a-540">**Keywords_spain_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="0285a-540">**Keywords_spain_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="0285a-541">passport</span><span class="sxs-lookup"><span data-stu-id="0285a-541">passport</span></span>  <br/> <span data-ttu-id="0285a-542">o Passport da Espanha</span><span class="sxs-lookup"><span data-stu-id="0285a-542">spain passport</span></span>  <br/> <span data-ttu-id="0285a-543">Catálogo do Passport</span><span class="sxs-lookup"><span data-stu-id="0285a-543">passport book</span></span>  <br/> <span data-ttu-id="0285a-544">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="0285a-544">passport number</span></span>  <br/> <span data-ttu-id="0285a-545">Passport não</span><span class="sxs-lookup"><span data-stu-id="0285a-545">passport no</span></span>  <br/> <span data-ttu-id="0285a-546">Libreta pasaporte</span><span class="sxs-lookup"><span data-stu-id="0285a-546">libreta pasaporte</span></span>  <br/> <span data-ttu-id="0285a-547">número pasaporte</span><span class="sxs-lookup"><span data-stu-id="0285a-547">número pasaporte</span></span>  <br/> <span data-ttu-id="0285a-548">España pasaporte</span><span class="sxs-lookup"><span data-stu-id="0285a-548">españa pasaporte</span></span>  <br/> <span data-ttu-id="0285a-549">pasaporte</span><span class="sxs-lookup"><span data-stu-id="0285a-549">pasaporte</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="0285a-550">Suécia</span><span class="sxs-lookup"><span data-stu-id="0285a-550">Sweden</span></span>

<span data-ttu-id="0285a-551">Para obter detalhes, consulte a seção "número de passaporte da Suécia" em [o que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="0285a-551">For details, see the section "Sweden Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="uk"></a><span data-ttu-id="0285a-552">Reino Unido</span><span class="sxs-lookup"><span data-stu-id="0285a-552">UK</span></span>

<span data-ttu-id="0285a-p103">Para obter detalhes, consulte a seção "número de passaporte americano/Reino Unido" em [o que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="0285a-p103">For details, see the section "U.S. / U.K. Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0285a-555">Confira também</span><span class="sxs-lookup"><span data-stu-id="0285a-555">See also</span></span>

[<span data-ttu-id="0285a-556">O que os tipos de informação confidencial procuram</span><span class="sxs-lookup"><span data-stu-id="0285a-556">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)


---
title: Número de passaporte da UE
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/16/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 8c00df57-9fb3-459c-ba87-40480c87bd55
description: Este tópico mostra o que uma política de prevenção (DLP) de perda de dados procura por quando detecta o tipo de informações confidenciais de número de passaporte da UE. Esse tipo de informações confidenciais define diferentes padrões, palavras-chave e outras evidências para cada país.
ms.openlocfilehash: 71acc39b885c057e1771ec13b2f3c25017ac1bb6
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524139"
---
# <a name="eu-passport-number"></a><span data-ttu-id="2ffe7-104">Número de passaporte da UE</span><span class="sxs-lookup"><span data-stu-id="2ffe7-104">EU Passport Number</span></span>

<span data-ttu-id="2ffe7-p102">Este tópico mostra o que uma política de prevenção (DLP) de perda de dados procura por quando detecta o tipo de informações confidenciais de número de passaporte da UE. Esse tipo de informações confidenciais define diferentes padrões, palavras-chave e outras evidências para cada país.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Passport Number sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="2ffe7-107">Áustria</span><span class="sxs-lookup"><span data-stu-id="2ffe7-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="2ffe7-108">Formato</span><span class="sxs-lookup"><span data-stu-id="2ffe7-108">Format</span></span>

<span data-ttu-id="2ffe7-109">Uma letra seguida por um espaço opcional e sete dígitos</span><span class="sxs-lookup"><span data-stu-id="2ffe7-109">One letter followed by an optional space and seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ffe7-110">Padrão</span><span class="sxs-lookup"><span data-stu-id="2ffe7-110">Pattern</span></span>

<span data-ttu-id="2ffe7-111">Uma combinação de uma letra, um espaço e sete dígitos:</span><span class="sxs-lookup"><span data-stu-id="2ffe7-111">A combination of one letter, seven digits, and one space:</span></span>
  
- <span data-ttu-id="2ffe7-112">Uma letra (não diferencia maiúscula de minúscula)</span><span class="sxs-lookup"><span data-stu-id="2ffe7-112">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="2ffe7-113">Um espaço (opcional)</span><span class="sxs-lookup"><span data-stu-id="2ffe7-113">One space (optional)</span></span>
    
- <span data-ttu-id="2ffe7-114">Sete dígitos</span><span class="sxs-lookup"><span data-stu-id="2ffe7-114">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="2ffe7-115">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="2ffe7-115">Checksum</span></span>

<span data-ttu-id="2ffe7-116">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="2ffe7-116">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ffe7-117">Definição</span><span class="sxs-lookup"><span data-stu-id="2ffe7-117">Definition</span></span>

<span data-ttu-id="2ffe7-118">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="2ffe7-118">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ffe7-119">A expressão regular `Regex_austria_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-119">The regular expression  `Regex_austria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ffe7-120">Uma palavra-chave da `Keywords_austria_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-120">A keyword from  `Keywords_austria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_passport_number" />
          <Match idRef="Keywords_austria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ffe7-121">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="2ffe7-121">Keywords</span></span>

<span data-ttu-id="2ffe7-122">| |</span><span class="sxs-lookup"><span data-stu-id="2ffe7-122"></span></span>
|<span data-ttu-id="2ffe7-123">**Keywords_austria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="2ffe7-123">**Keywords_austria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="2ffe7-124">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="2ffe7-124">passport number</span></span>  <br/> <span data-ttu-id="2ffe7-125">número de passaporte austríaco</span><span class="sxs-lookup"><span data-stu-id="2ffe7-125">austrian passport number</span></span>  <br/> <span data-ttu-id="2ffe7-126">Passport nenhum</span><span class="sxs-lookup"><span data-stu-id="2ffe7-126">passport no</span></span>  <br/> <span data-ttu-id="2ffe7-127">reisepass</span><span class="sxs-lookup"><span data-stu-id="2ffe7-127">reisepass</span></span>  <br/> <span data-ttu-id="2ffe7-128">österreichisch reisepass</span><span class="sxs-lookup"><span data-stu-id="2ffe7-128">österreichisch reisepass</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="2ffe7-129">Bélgica</span><span class="sxs-lookup"><span data-stu-id="2ffe7-129">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="2ffe7-130">Formato</span><span class="sxs-lookup"><span data-stu-id="2ffe7-130">Format</span></span>

<span data-ttu-id="2ffe7-131">Duas letras seguidas de seis dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="2ffe7-131">Two letters followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ffe7-132">Padrão</span><span class="sxs-lookup"><span data-stu-id="2ffe7-132">Pattern</span></span>

<span data-ttu-id="2ffe7-133">Duas letras e seguido de seis dígitos</span><span class="sxs-lookup"><span data-stu-id="2ffe7-133">Two letters and followed by six digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="2ffe7-134">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="2ffe7-134">Checksum</span></span>

<span data-ttu-id="2ffe7-135">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="2ffe7-135">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ffe7-136">Definição</span><span class="sxs-lookup"><span data-stu-id="2ffe7-136">Definition</span></span>

<span data-ttu-id="2ffe7-137">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="2ffe7-137">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ffe7-138">A expressão regular `Regex_belgium_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-138">The regular expression  `Regex_belgium_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ffe7-139">Uma palavra-chave da `Keywords_belgium_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-139">A keyword from  `Keywords_belgium_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium__eu_passport_number" />
          <Match idRef="Keywords_belgium_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ffe7-140">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="2ffe7-140">Keywords</span></span>

<span data-ttu-id="2ffe7-141">| |</span><span class="sxs-lookup"><span data-stu-id="2ffe7-141"></span></span>
|<span data-ttu-id="2ffe7-142">**Keywords_belgium_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="2ffe7-142">**Keywords_belgium_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="2ffe7-143">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="2ffe7-143">passport number</span></span>  <br/> <span data-ttu-id="2ffe7-144">número de passaporte belga</span><span class="sxs-lookup"><span data-stu-id="2ffe7-144">belgian passport number</span></span>  <br/> <span data-ttu-id="2ffe7-145">Passport nenhum</span><span class="sxs-lookup"><span data-stu-id="2ffe7-145">passport no</span></span>  <br/> <span data-ttu-id="2ffe7-146">paspoort</span><span class="sxs-lookup"><span data-stu-id="2ffe7-146">paspoort</span></span>  <br/> <span data-ttu-id="2ffe7-147">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="2ffe7-147">paspoortnummer</span></span>  <br/> <span data-ttu-id="2ffe7-148">reisepass kein</span><span class="sxs-lookup"><span data-stu-id="2ffe7-148">reisepass kein</span></span>  <br/> <span data-ttu-id="2ffe7-149">reisepass</span><span class="sxs-lookup"><span data-stu-id="2ffe7-149">reisepass</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="2ffe7-150">Bulgária</span><span class="sxs-lookup"><span data-stu-id="2ffe7-150">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="2ffe7-151">Formato</span><span class="sxs-lookup"><span data-stu-id="2ffe7-151">Format</span></span>

<span data-ttu-id="2ffe7-152">Nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="2ffe7-152">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ffe7-153">Padrão</span><span class="sxs-lookup"><span data-stu-id="2ffe7-153">Pattern</span></span>

 <span data-ttu-id="2ffe7-154">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="2ffe7-154">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="2ffe7-155">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="2ffe7-155">Checksum</span></span>

<span data-ttu-id="2ffe7-156">Não</span><span class="sxs-lookup"><span data-stu-id="2ffe7-156">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ffe7-157">Definição</span><span class="sxs-lookup"><span data-stu-id="2ffe7-157">Definition</span></span>

<span data-ttu-id="2ffe7-158">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="2ffe7-158">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ffe7-159">A expressão regular `Regex_bulgaria_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-159">The regular expression  `Regex_bulgaria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ffe7-160">Uma palavra-chave da `Keywords_bulgaria_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-160">A keyword from  `Keywords_bulgaria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_passport_number" />
          <Match idRef="Keywords_bulgaria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ffe7-161">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="2ffe7-161">Keywords</span></span>

<span data-ttu-id="2ffe7-162">| |</span><span class="sxs-lookup"><span data-stu-id="2ffe7-162"></span></span>
|<span data-ttu-id="2ffe7-163">**Keywords_bulgaria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="2ffe7-163">**Keywords_bulgaria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="2ffe7-164">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="2ffe7-164">passport number</span></span>  <br/> <span data-ttu-id="2ffe7-165">número de passaporte búlgaro</span><span class="sxs-lookup"><span data-stu-id="2ffe7-165">bulgarian passport number</span></span>  <br/> <span data-ttu-id="2ffe7-166">Passport nenhum</span><span class="sxs-lookup"><span data-stu-id="2ffe7-166">passport no</span></span>  <br/> <span data-ttu-id="2ffe7-167">НОМЕР НА ПАСПОРТА</span><span class="sxs-lookup"><span data-stu-id="2ffe7-167">номер на паспорта</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="2ffe7-168">Croácia</span><span class="sxs-lookup"><span data-stu-id="2ffe7-168">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="2ffe7-169">Formato</span><span class="sxs-lookup"><span data-stu-id="2ffe7-169">Format</span></span>

<span data-ttu-id="2ffe7-170">Nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="2ffe7-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ffe7-171">Padrão</span><span class="sxs-lookup"><span data-stu-id="2ffe7-171">Pattern</span></span>

 <span data-ttu-id="2ffe7-172">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="2ffe7-172">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="2ffe7-173">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="2ffe7-173">Checksum</span></span>

<span data-ttu-id="2ffe7-174">Não</span><span class="sxs-lookup"><span data-stu-id="2ffe7-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ffe7-175">Definição</span><span class="sxs-lookup"><span data-stu-id="2ffe7-175">Definition</span></span>

<span data-ttu-id="2ffe7-176">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="2ffe7-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ffe7-177">A expressão regular `Regex_croatia_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-177">The regular expression  `Regex_croatia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ffe7-178">Uma palavra-chave da `Keywords_croatia_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-178">A keyword from  `Keywords_croatia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_passport_number" />
          <Match idRef="Keywords_croatia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ffe7-179">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="2ffe7-179">Keywords</span></span>

<span data-ttu-id="2ffe7-180">| |</span><span class="sxs-lookup"><span data-stu-id="2ffe7-180"></span></span>
|<span data-ttu-id="2ffe7-181">**Keywords_croatia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="2ffe7-181">**Keywords_croatia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="2ffe7-182">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="2ffe7-182">passport number</span></span>  <br/> <span data-ttu-id="2ffe7-183">número de passaporte croata</span><span class="sxs-lookup"><span data-stu-id="2ffe7-183">croatian passport number</span></span>  <br/> <span data-ttu-id="2ffe7-184">Passport nenhum</span><span class="sxs-lookup"><span data-stu-id="2ffe7-184">passport no</span></span>  <br/> <span data-ttu-id="2ffe7-185">broj putovnice</span><span class="sxs-lookup"><span data-stu-id="2ffe7-185">broj putovnice</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="2ffe7-186">Chipre</span><span class="sxs-lookup"><span data-stu-id="2ffe7-186">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="2ffe7-187">Formato</span><span class="sxs-lookup"><span data-stu-id="2ffe7-187">Format</span></span>

<span data-ttu-id="2ffe7-188">Uma letra seguida de 6 a 8 dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="2ffe7-188">One letter followed by 6-8 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ffe7-189">Padrão</span><span class="sxs-lookup"><span data-stu-id="2ffe7-189">Pattern</span></span>

<span data-ttu-id="2ffe7-190">Uma letra seguida de seis a oito dígitos</span><span class="sxs-lookup"><span data-stu-id="2ffe7-190">One letter followed by six to eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="2ffe7-191">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="2ffe7-191">Checksum</span></span>

<span data-ttu-id="2ffe7-192">Não</span><span class="sxs-lookup"><span data-stu-id="2ffe7-192">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ffe7-193">Definição</span><span class="sxs-lookup"><span data-stu-id="2ffe7-193">Definition</span></span>

<span data-ttu-id="2ffe7-194">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="2ffe7-194">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ffe7-195">A expressão regular `Regex_cyprus_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-195">The regular expression  `Regex_cyprus_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ffe7-196">Uma palavra-chave da `Keywords_cyprus_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-196">A keyword from  `Keywords_cyprus_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_passport_number" />
          <Match idRef="Keywords_cyprus_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ffe7-197">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="2ffe7-197">Keywords</span></span>

<span data-ttu-id="2ffe7-198">| |</span><span class="sxs-lookup"><span data-stu-id="2ffe7-198"></span></span>
|<span data-ttu-id="2ffe7-199">**Keywords_cyprus_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="2ffe7-199">**Keywords_cyprus_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="2ffe7-200">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="2ffe7-200">passport number</span></span>  <br/> <span data-ttu-id="2ffe7-201">número de passaporte Chipre</span><span class="sxs-lookup"><span data-stu-id="2ffe7-201">cyprus passport number</span></span>  <br/> <span data-ttu-id="2ffe7-202">Passport nenhum</span><span class="sxs-lookup"><span data-stu-id="2ffe7-202">passport no</span></span>  <br/> <span data-ttu-id="2ffe7-203">ΑΡΙΘΜΌ ΔΙΑΒΑΤΗΡΊΟΥ</span><span class="sxs-lookup"><span data-stu-id="2ffe7-203">αριθμό διαβατηρίου</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="2ffe7-204">República Tcheca</span><span class="sxs-lookup"><span data-stu-id="2ffe7-204">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="2ffe7-205">Formato</span><span class="sxs-lookup"><span data-stu-id="2ffe7-205">Format</span></span>

<span data-ttu-id="2ffe7-206">Oito dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="2ffe7-206">Eight digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ffe7-207">Padrão</span><span class="sxs-lookup"><span data-stu-id="2ffe7-207">Pattern</span></span>

<span data-ttu-id="2ffe7-208">Oito dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="2ffe7-208">Eight digits without spaces or delimiters</span></span>
  
### <a name="checksum"></a><span data-ttu-id="2ffe7-209">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="2ffe7-209">Checksum</span></span>

<span data-ttu-id="2ffe7-210">Não</span><span class="sxs-lookup"><span data-stu-id="2ffe7-210">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ffe7-211">Definição</span><span class="sxs-lookup"><span data-stu-id="2ffe7-211">Definition</span></span>

<span data-ttu-id="2ffe7-212">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="2ffe7-212">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ffe7-213">A expressão regular `Regex_czech_republic_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-213">The regular expression  `Regex_czech_republic_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ffe7-214">Uma palavra-chave da `Keywords_czech_republic_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-214">A keyword from  `Keywords_czech_republic_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_passport_number" />
          <Match idRef="Keywords_czech_republic_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ffe7-215">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="2ffe7-215">Keywords</span></span>

<span data-ttu-id="2ffe7-216">| |</span><span class="sxs-lookup"><span data-stu-id="2ffe7-216"></span></span>
|<span data-ttu-id="2ffe7-217">**Keywords_czech_republic_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="2ffe7-217">**Keywords_czech_republic_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="2ffe7-218">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="2ffe7-218">passport number</span></span>  <br/> <span data-ttu-id="2ffe7-219">número de passaporte tcheco</span><span class="sxs-lookup"><span data-stu-id="2ffe7-219">czech passport number</span></span>  <br/> <span data-ttu-id="2ffe7-220">Passport nenhum</span><span class="sxs-lookup"><span data-stu-id="2ffe7-220">passport no</span></span>  <br/> <span data-ttu-id="2ffe7-221">cestovní pas</span><span class="sxs-lookup"><span data-stu-id="2ffe7-221">cestovní pas</span></span>  <br/> <span data-ttu-id="2ffe7-222">PAS</span><span class="sxs-lookup"><span data-stu-id="2ffe7-222">pas</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="2ffe7-223">Dinamarca</span><span class="sxs-lookup"><span data-stu-id="2ffe7-223">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="2ffe7-224">Formato</span><span class="sxs-lookup"><span data-stu-id="2ffe7-224">Format</span></span>

<span data-ttu-id="2ffe7-225">Nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="2ffe7-225">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ffe7-226">Padrão</span><span class="sxs-lookup"><span data-stu-id="2ffe7-226">Pattern</span></span>

 <span data-ttu-id="2ffe7-227">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="2ffe7-227">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="2ffe7-228">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="2ffe7-228">Checksum</span></span>

<span data-ttu-id="2ffe7-229">Não</span><span class="sxs-lookup"><span data-stu-id="2ffe7-229">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ffe7-230">Definição</span><span class="sxs-lookup"><span data-stu-id="2ffe7-230">Definition</span></span>

<span data-ttu-id="2ffe7-231">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="2ffe7-231">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ffe7-232">A expressão regular `Regex_denmark_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-232">The regular expression  `Regex_denmark_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ffe7-233">Uma palavra-chave da `Keywords_denmark_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-233">A keyword from  `Keywords_denmark_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_passport_number" />
          <Match idRef="Keywords_denmark_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ffe7-234">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="2ffe7-234">Keywords</span></span>

<span data-ttu-id="2ffe7-235">| |</span><span class="sxs-lookup"><span data-stu-id="2ffe7-235"></span></span>
|<span data-ttu-id="2ffe7-236">**Keywords_denmark_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="2ffe7-236">**Keywords_denmark_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="2ffe7-237">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="2ffe7-237">passport number</span></span>  <br/> <span data-ttu-id="2ffe7-238">número de passaporte dinamarquês</span><span class="sxs-lookup"><span data-stu-id="2ffe7-238">danish passport number</span></span>  <br/> <span data-ttu-id="2ffe7-239">Passport nenhum</span><span class="sxs-lookup"><span data-stu-id="2ffe7-239">passport no</span></span>  <br/> <span data-ttu-id="2ffe7-240">PAS</span><span class="sxs-lookup"><span data-stu-id="2ffe7-240">pas</span></span>  <br/> <span data-ttu-id="2ffe7-241">pasnummer</span><span class="sxs-lookup"><span data-stu-id="2ffe7-241">pasnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="2ffe7-242">Estônia</span><span class="sxs-lookup"><span data-stu-id="2ffe7-242">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="2ffe7-243">Formato</span><span class="sxs-lookup"><span data-stu-id="2ffe7-243">Format</span></span>

<span data-ttu-id="2ffe7-244">Uma letra seguida por sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="2ffe7-244">One letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ffe7-245">Padrão</span><span class="sxs-lookup"><span data-stu-id="2ffe7-245">Pattern</span></span>

<span data-ttu-id="2ffe7-246">Uma letra seguida por sete dígitos</span><span class="sxs-lookup"><span data-stu-id="2ffe7-246">One letter followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="2ffe7-247">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="2ffe7-247">Checksum</span></span>

<span data-ttu-id="2ffe7-248">Não</span><span class="sxs-lookup"><span data-stu-id="2ffe7-248">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ffe7-249">Definição</span><span class="sxs-lookup"><span data-stu-id="2ffe7-249">Definition</span></span>

<span data-ttu-id="2ffe7-250">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="2ffe7-250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ffe7-251">A expressão regular `Regex_estonia_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-251">The regular expression  `Regex_estonia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ffe7-252">Uma palavra-chave da `Keywords_estonia_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-252">A keyword from  `Keywords_estonia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_passport_number" />
          <Match idRef="Keywords_estonia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ffe7-253">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="2ffe7-253">Keywords</span></span>

<span data-ttu-id="2ffe7-254">| |</span><span class="sxs-lookup"><span data-stu-id="2ffe7-254"></span></span>
|<span data-ttu-id="2ffe7-255">**Keywords_estonia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="2ffe7-255">**Keywords_estonia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="2ffe7-256">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="2ffe7-256">passport number</span></span>  <br/> <span data-ttu-id="2ffe7-257">número de passaporte estoniano</span><span class="sxs-lookup"><span data-stu-id="2ffe7-257">estonian passport number</span></span>  <br/> <span data-ttu-id="2ffe7-258">Passport nenhum</span><span class="sxs-lookup"><span data-stu-id="2ffe7-258">passport no</span></span>  <br/> <span data-ttu-id="2ffe7-259">eesti kodaniku secreta</span><span class="sxs-lookup"><span data-stu-id="2ffe7-259">eesti kodaniku pass</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="2ffe7-260">Finlândia</span><span class="sxs-lookup"><span data-stu-id="2ffe7-260">Finland</span></span>

<span data-ttu-id="2ffe7-261">Para obter detalhes, consulte a seção "Número de passaporte da Finlândia" nos [quais os tipos de informações confidenciais procurar](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="2ffe7-261">For details, see the section "Finland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="2ffe7-262">França</span><span class="sxs-lookup"><span data-stu-id="2ffe7-262">France</span></span>

<span data-ttu-id="2ffe7-263">Para obter detalhes, consulte a seção "Número de passaporte da França" nos [quais os tipos de informações confidenciais procurar](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="2ffe7-263">For details, see the section "France Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="2ffe7-264">Alemanha</span><span class="sxs-lookup"><span data-stu-id="2ffe7-264">Germany</span></span>

<span data-ttu-id="2ffe7-265">Para obter detalhes, consulte a seção "Número de passaporte da Alemanha" em [quais tipos de informações confidenciais a procurar](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="2ffe7-265">For details, see the section "Germany Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="2ffe7-266">Grécia</span><span class="sxs-lookup"><span data-stu-id="2ffe7-266">Greece</span></span>

### <a name="format"></a><span data-ttu-id="2ffe7-267">Formato</span><span class="sxs-lookup"><span data-stu-id="2ffe7-267">Format</span></span>

<span data-ttu-id="2ffe7-268">Duas letras seguidas por sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="2ffe7-268">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ffe7-269">Padrão</span><span class="sxs-lookup"><span data-stu-id="2ffe7-269">Pattern</span></span>

<span data-ttu-id="2ffe7-270">Duas letras seguidas por sete dígitos</span><span class="sxs-lookup"><span data-stu-id="2ffe7-270">Two letters followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="2ffe7-271">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="2ffe7-271">Checksum</span></span>

<span data-ttu-id="2ffe7-272">Não</span><span class="sxs-lookup"><span data-stu-id="2ffe7-272">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ffe7-273">Definição</span><span class="sxs-lookup"><span data-stu-id="2ffe7-273">Definition</span></span>

<span data-ttu-id="2ffe7-274">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="2ffe7-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ffe7-275">A expressão regular `Regex_greece_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-275">The regular expression  `Regex_greece_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ffe7-276">Uma palavra-chave da `Keywords_greece_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-276">A keyword from  `Keywords_greece_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_passport_number" />
          <Match idRef="Keywords_greece_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ffe7-277">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="2ffe7-277">Keywords</span></span>

<span data-ttu-id="2ffe7-278">| |</span><span class="sxs-lookup"><span data-stu-id="2ffe7-278"></span></span>
|<span data-ttu-id="2ffe7-279">**Keywords_greece_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="2ffe7-279">**Keywords_greece_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="2ffe7-280">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="2ffe7-280">passport number</span></span>  <br/> <span data-ttu-id="2ffe7-281">número de passaporte grego</span><span class="sxs-lookup"><span data-stu-id="2ffe7-281">greek passport number</span></span>  <br/> <span data-ttu-id="2ffe7-282">Passport nenhum</span><span class="sxs-lookup"><span data-stu-id="2ffe7-282">passport no</span></span>  <br/> <span data-ttu-id="2ffe7-283">ΔΙΑΒΑΤΗΡΙΟ</span><span class="sxs-lookup"><span data-stu-id="2ffe7-283">διαβατηριο</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="2ffe7-284">Hungria</span><span class="sxs-lookup"><span data-stu-id="2ffe7-284">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="2ffe7-285">Formato</span><span class="sxs-lookup"><span data-stu-id="2ffe7-285">Format</span></span>

<span data-ttu-id="2ffe7-286">Duas letras seguidas por seis ou sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="2ffe7-286">Two letters followed by six or seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ffe7-287">Padrão</span><span class="sxs-lookup"><span data-stu-id="2ffe7-287">Pattern</span></span>

<span data-ttu-id="2ffe7-288">Duas letras seguidas por seis ou sete dígitos</span><span class="sxs-lookup"><span data-stu-id="2ffe7-288">Two letters followed by six or seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="2ffe7-289">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="2ffe7-289">Checksum</span></span>

<span data-ttu-id="2ffe7-290">Não</span><span class="sxs-lookup"><span data-stu-id="2ffe7-290">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ffe7-291">Definição</span><span class="sxs-lookup"><span data-stu-id="2ffe7-291">Definition</span></span>

<span data-ttu-id="2ffe7-292">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="2ffe7-292">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ffe7-293">A expressão regular `Regex_hungary_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-293">The regular expression  `Regex_hungary_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ffe7-294">Uma palavra-chave da `Keywords_hungary_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-294">A keyword from  `Keywords_hungary_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_passport_number" />
          <Match idRef="Keywords_hungary_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ffe7-295">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="2ffe7-295">Keywords</span></span>

<span data-ttu-id="2ffe7-296">| |</span><span class="sxs-lookup"><span data-stu-id="2ffe7-296"></span></span>
|<span data-ttu-id="2ffe7-297">**Keywords_hungary_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="2ffe7-297">**Keywords_hungary_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="2ffe7-298">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="2ffe7-298">passport number</span></span>  <br/> <span data-ttu-id="2ffe7-299">número de passaporte húngaro</span><span class="sxs-lookup"><span data-stu-id="2ffe7-299">hungarian passport number</span></span>  <br/> <span data-ttu-id="2ffe7-300">Passport nenhum</span><span class="sxs-lookup"><span data-stu-id="2ffe7-300">passport no</span></span>  <br/> <span data-ttu-id="2ffe7-301">útlevél száma</span><span class="sxs-lookup"><span data-stu-id="2ffe7-301">útlevél száma</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="2ffe7-302">Irlanda</span><span class="sxs-lookup"><span data-stu-id="2ffe7-302">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="2ffe7-303">Formato</span><span class="sxs-lookup"><span data-stu-id="2ffe7-303">Format</span></span>

<span data-ttu-id="2ffe7-304">Duas letras ou dígitos seguidos por sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="2ffe7-304">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ffe7-305">Padrão</span><span class="sxs-lookup"><span data-stu-id="2ffe7-305">Pattern</span></span>

<span data-ttu-id="2ffe7-306">Duas letras ou dígitos seguidos por sete dígitos:</span><span class="sxs-lookup"><span data-stu-id="2ffe7-306">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="2ffe7-307">Dois dígitos ou letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="2ffe7-307">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="2ffe7-308">Sete dígitos</span><span class="sxs-lookup"><span data-stu-id="2ffe7-308">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="2ffe7-309">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="2ffe7-309">Checksum</span></span>

<span data-ttu-id="2ffe7-310">Não</span><span class="sxs-lookup"><span data-stu-id="2ffe7-310">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ffe7-311">Definição</span><span class="sxs-lookup"><span data-stu-id="2ffe7-311">Definition</span></span>

<span data-ttu-id="2ffe7-312">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="2ffe7-312">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ffe7-313">A expressão regular `Regex_ireland_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-313">The regular expression  `Regex_ireland_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ffe7-314">Uma palavra-chave da `Keywords_ireland_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-314">A keyword from  `Keywords_ireland_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_passport_number" />
          <Match idRef="Keywords_ireland_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ffe7-315">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="2ffe7-315">Keywords</span></span>

<span data-ttu-id="2ffe7-316">| |</span><span class="sxs-lookup"><span data-stu-id="2ffe7-316"></span></span>
|<span data-ttu-id="2ffe7-317">**Keywords_ireland_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="2ffe7-317">**Keywords_ireland_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="2ffe7-318">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="2ffe7-318">passport number</span></span>  <br/> <span data-ttu-id="2ffe7-319">número de passaporte irlandês</span><span class="sxs-lookup"><span data-stu-id="2ffe7-319">irish passport number</span></span>  <br/> <span data-ttu-id="2ffe7-320">Passport nenhum</span><span class="sxs-lookup"><span data-stu-id="2ffe7-320">passport no</span></span>  <br/> <span data-ttu-id="2ffe7-321">PAS</span><span class="sxs-lookup"><span data-stu-id="2ffe7-321">pas</span></span>  <br/> <span data-ttu-id="2ffe7-322">passport</span><span class="sxs-lookup"><span data-stu-id="2ffe7-322">passport</span></span>  <br/> <span data-ttu-id="2ffe7-323">passeport</span><span class="sxs-lookup"><span data-stu-id="2ffe7-323">passeport</span></span>  <br/> <span data-ttu-id="2ffe7-324">numero passeport</span><span class="sxs-lookup"><span data-stu-id="2ffe7-324">passeport numero</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="2ffe7-325">Itália</span><span class="sxs-lookup"><span data-stu-id="2ffe7-325">Italy</span></span>

### <a name="format"></a><span data-ttu-id="2ffe7-326">Formato</span><span class="sxs-lookup"><span data-stu-id="2ffe7-326">Format</span></span>

<span data-ttu-id="2ffe7-327">Duas letras ou dígitos seguidos por sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="2ffe7-327">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ffe7-328">Padrão</span><span class="sxs-lookup"><span data-stu-id="2ffe7-328">Pattern</span></span>

<span data-ttu-id="2ffe7-329">Duas letras ou dígitos seguidos por sete dígitos:</span><span class="sxs-lookup"><span data-stu-id="2ffe7-329">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="2ffe7-330">Dois dígitos ou letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="2ffe7-330">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="2ffe7-331">Sete dígitos</span><span class="sxs-lookup"><span data-stu-id="2ffe7-331">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="2ffe7-332">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="2ffe7-332">Checksum</span></span>

<span data-ttu-id="2ffe7-333">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="2ffe7-333">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ffe7-334">Definição</span><span class="sxs-lookup"><span data-stu-id="2ffe7-334">Definition</span></span>

<span data-ttu-id="2ffe7-335">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="2ffe7-335">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ffe7-336">A expressão regular `Regex_italy_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-336">The regular expression  `Regex_italy_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ffe7-337">Uma palavra-chave da `Keywords_italy_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-337">A keyword from  `Keywords_italy_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_passport_number" />
          <Match idRef="Keywords_italy_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ffe7-338">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="2ffe7-338">Keywords</span></span>

<span data-ttu-id="2ffe7-339">| |</span><span class="sxs-lookup"><span data-stu-id="2ffe7-339"></span></span>
|<span data-ttu-id="2ffe7-340">**Keywords_italy_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="2ffe7-340">**Keywords_italy_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="2ffe7-341">número de passaporte italiano</span><span class="sxs-lookup"><span data-stu-id="2ffe7-341">italian passport number</span></span>  <br/> <span data-ttu-id="2ffe7-342">repubblica italiana passaporto</span><span class="sxs-lookup"><span data-stu-id="2ffe7-342">repubblica italiana passaporto</span></span>  <br/> <span data-ttu-id="2ffe7-343">passaporto</span><span class="sxs-lookup"><span data-stu-id="2ffe7-343">passaporto</span></span>  <br/> <span data-ttu-id="2ffe7-344">passaporto italiana</span><span class="sxs-lookup"><span data-stu-id="2ffe7-344">passaporto italiana</span></span>  <br/> <span data-ttu-id="2ffe7-345">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="2ffe7-345">passport number</span></span>  <br/> <span data-ttu-id="2ffe7-346">italiana passaporto numero</span><span class="sxs-lookup"><span data-stu-id="2ffe7-346">italiana passaporto numero</span></span>  <br/> <span data-ttu-id="2ffe7-347">numero passaporto</span><span class="sxs-lookup"><span data-stu-id="2ffe7-347">passaporto numero</span></span>  <br/> <span data-ttu-id="2ffe7-348">numéro passeport italien</span><span class="sxs-lookup"><span data-stu-id="2ffe7-348">numéro passeport italien</span></span>  <br/> <span data-ttu-id="2ffe7-349">numéro passeport</span><span class="sxs-lookup"><span data-stu-id="2ffe7-349">numéro passeport</span></span>  <br/> |
   
## <a name="latvia"></a><span data-ttu-id="2ffe7-350">Letônia</span><span class="sxs-lookup"><span data-stu-id="2ffe7-350">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="2ffe7-351">Formato</span><span class="sxs-lookup"><span data-stu-id="2ffe7-351">Format</span></span>

<span data-ttu-id="2ffe7-352">Duas letras ou dígitos seguidos por sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="2ffe7-352">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ffe7-353">Padrão</span><span class="sxs-lookup"><span data-stu-id="2ffe7-353">Pattern</span></span>

<span data-ttu-id="2ffe7-354">Duas letras ou dígitos seguidos por sete dígitos:</span><span class="sxs-lookup"><span data-stu-id="2ffe7-354">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="2ffe7-355">Dois dígitos ou letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="2ffe7-355">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="2ffe7-356">Sete dígitos</span><span class="sxs-lookup"><span data-stu-id="2ffe7-356">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="2ffe7-357">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="2ffe7-357">Checksum</span></span>

<span data-ttu-id="2ffe7-358">Não</span><span class="sxs-lookup"><span data-stu-id="2ffe7-358">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ffe7-359">Definição</span><span class="sxs-lookup"><span data-stu-id="2ffe7-359">Definition</span></span>

<span data-ttu-id="2ffe7-360">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="2ffe7-360">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ffe7-361">A expressão regular `Regex_latvia_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-361">The regular expression  `Regex_latvia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ffe7-362">Uma palavra-chave da `Keywords_latvia_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-362">A keyword from  `Keywords_latvia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_passport_number" />
          <Match idRef="Keywords_latvia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ffe7-363">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="2ffe7-363">Keywords</span></span>

<span data-ttu-id="2ffe7-364">| |</span><span class="sxs-lookup"><span data-stu-id="2ffe7-364"></span></span>
|<span data-ttu-id="2ffe7-365">**Keywords_latvia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="2ffe7-365">**Keywords_latvia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="2ffe7-366">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="2ffe7-366">passport number</span></span>  <br/> <span data-ttu-id="2ffe7-367">número de passaporte letão</span><span class="sxs-lookup"><span data-stu-id="2ffe7-367">latvian passport number</span></span>  <br/> <span data-ttu-id="2ffe7-368">Passport nenhum</span><span class="sxs-lookup"><span data-stu-id="2ffe7-368">passport no</span></span>  <br/> <span data-ttu-id="2ffe7-369">pase numurs</span><span class="sxs-lookup"><span data-stu-id="2ffe7-369">pase numurs</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="2ffe7-370">Lituânia</span><span class="sxs-lookup"><span data-stu-id="2ffe7-370">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="2ffe7-371">Formato</span><span class="sxs-lookup"><span data-stu-id="2ffe7-371">Format</span></span>

<span data-ttu-id="2ffe7-372">Oito dígitos ou letras sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="2ffe7-372">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ffe7-373">Padrão</span><span class="sxs-lookup"><span data-stu-id="2ffe7-373">Pattern</span></span>

<span data-ttu-id="2ffe7-374">Oito dígitos ou letras (não maiusculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="2ffe7-374">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="2ffe7-375">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="2ffe7-375">Checksum</span></span>

<span data-ttu-id="2ffe7-376">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="2ffe7-376">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ffe7-377">Definição</span><span class="sxs-lookup"><span data-stu-id="2ffe7-377">Definition</span></span>

<span data-ttu-id="2ffe7-378">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="2ffe7-378">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ffe7-379">A expressão regular `Regex_lithuania_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-379">The regular expression  `Regex_lithuania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ffe7-380">Uma palavra-chave da `Keywords_lithuania_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-380">A keyword from  `Keywords_lithuania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_passport_number" />
          <Match idRef="Keywords_lithuania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ffe7-381">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="2ffe7-381">Keywords</span></span>

<span data-ttu-id="2ffe7-382">| |</span><span class="sxs-lookup"><span data-stu-id="2ffe7-382"></span></span>
|<span data-ttu-id="2ffe7-383">**Keywords_lithuania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="2ffe7-383">**Keywords_lithuania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="2ffe7-384">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="2ffe7-384">passport number</span></span>  <br/> <span data-ttu-id="2ffe7-385">número de passaporte lithunian</span><span class="sxs-lookup"><span data-stu-id="2ffe7-385">lithunian passport number</span></span>  <br/> <span data-ttu-id="2ffe7-386">Passport nenhum</span><span class="sxs-lookup"><span data-stu-id="2ffe7-386">passport no</span></span>  <br/> <span data-ttu-id="2ffe7-387">Paso numeris</span><span class="sxs-lookup"><span data-stu-id="2ffe7-387">paso numeris</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="2ffe7-388">Luxemburgo</span><span class="sxs-lookup"><span data-stu-id="2ffe7-388">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="2ffe7-389">Formato</span><span class="sxs-lookup"><span data-stu-id="2ffe7-389">Format</span></span>

<span data-ttu-id="2ffe7-390">Oito dígitos ou letras sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="2ffe7-390">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ffe7-391">Padrão</span><span class="sxs-lookup"><span data-stu-id="2ffe7-391">Pattern</span></span>

<span data-ttu-id="2ffe7-392">Oito dígitos ou letras (não maiusculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="2ffe7-392">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="2ffe7-393">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="2ffe7-393">Checksum</span></span>

<span data-ttu-id="2ffe7-394">Não</span><span class="sxs-lookup"><span data-stu-id="2ffe7-394">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ffe7-395">Definição</span><span class="sxs-lookup"><span data-stu-id="2ffe7-395">Definition</span></span>

<span data-ttu-id="2ffe7-396">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="2ffe7-396">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ffe7-397">A expressão regular `Regex_nation_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-397">The regular expression  `Regex_nation_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ffe7-398">Uma palavra-chave da `Keywords_nation_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-398">A keyword from  `Keywords_nation_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_nation_eu_passport_number" />
          <Match idRef="Keywords_nation_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ffe7-399">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="2ffe7-399">Keywords</span></span>

<span data-ttu-id="2ffe7-400">| |</span><span class="sxs-lookup"><span data-stu-id="2ffe7-400"></span></span>
|<span data-ttu-id="2ffe7-401">**Keywords_nation_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="2ffe7-401">**Keywords_nation_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="2ffe7-402">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="2ffe7-402">passport number</span></span>  <br/> <span data-ttu-id="2ffe7-403">número de passaporte letão</span><span class="sxs-lookup"><span data-stu-id="2ffe7-403">latvian passport number</span></span>  <br/> <span data-ttu-id="2ffe7-404">Passport nenhum</span><span class="sxs-lookup"><span data-stu-id="2ffe7-404">passport no</span></span>  <br/> <span data-ttu-id="2ffe7-405">passnummer</span><span class="sxs-lookup"><span data-stu-id="2ffe7-405">passnummer</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="2ffe7-406">Malta</span><span class="sxs-lookup"><span data-stu-id="2ffe7-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="2ffe7-407">Formato</span><span class="sxs-lookup"><span data-stu-id="2ffe7-407">Format</span></span>

<span data-ttu-id="2ffe7-408">Sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="2ffe7-408">Seven digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ffe7-409">Padrão</span><span class="sxs-lookup"><span data-stu-id="2ffe7-409">Pattern</span></span>

 <span data-ttu-id="2ffe7-410">Sete dígitos</span><span class="sxs-lookup"><span data-stu-id="2ffe7-410">Seven digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="2ffe7-411">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="2ffe7-411">Checksum</span></span>

<span data-ttu-id="2ffe7-412">Não</span><span class="sxs-lookup"><span data-stu-id="2ffe7-412">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ffe7-413">Definição</span><span class="sxs-lookup"><span data-stu-id="2ffe7-413">Definition</span></span>

<span data-ttu-id="2ffe7-414">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="2ffe7-414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ffe7-415">A expressão regular `Regex_malta_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-415">The regular expression  `Regex_malta_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ffe7-416">Uma palavra-chave da `Keywords_malta_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-416">A keyword from  `Keywords_malta_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_passport_number" />
          <Match idRef="Keywords_malta_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ffe7-417">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="2ffe7-417">Keywords</span></span>

<span data-ttu-id="2ffe7-418">| |</span><span class="sxs-lookup"><span data-stu-id="2ffe7-418"></span></span>
|<span data-ttu-id="2ffe7-419">**Keywords_malta_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="2ffe7-419">**Keywords_malta_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="2ffe7-420">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="2ffe7-420">passport number</span></span>  <br/> <span data-ttu-id="2ffe7-421">número de passaporte Maltês</span><span class="sxs-lookup"><span data-stu-id="2ffe7-421">maltese passport number</span></span>  <br/> <span data-ttu-id="2ffe7-422">Passport nenhum</span><span class="sxs-lookup"><span data-stu-id="2ffe7-422">passport no</span></span>  <br/> <span data-ttu-id="2ffe7-423">horizontal-passaport numru</span><span class="sxs-lookup"><span data-stu-id="2ffe7-423">numru tal-passaport</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="2ffe7-424">Países Baixos</span><span class="sxs-lookup"><span data-stu-id="2ffe7-424">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="2ffe7-425">Formato</span><span class="sxs-lookup"><span data-stu-id="2ffe7-425">Format</span></span>

<span data-ttu-id="2ffe7-426">Nove letras ou dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="2ffe7-426">Nine letters or digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ffe7-427">Padrão</span><span class="sxs-lookup"><span data-stu-id="2ffe7-427">Pattern</span></span>

<span data-ttu-id="2ffe7-428">Nove letras ou dígitos</span><span class="sxs-lookup"><span data-stu-id="2ffe7-428">Nine letters or digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="2ffe7-429">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="2ffe7-429">Checksum</span></span>

<span data-ttu-id="2ffe7-430">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="2ffe7-430">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ffe7-431">Definição</span><span class="sxs-lookup"><span data-stu-id="2ffe7-431">Definition</span></span>

<span data-ttu-id="2ffe7-432">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="2ffe7-432">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ffe7-433">A expressão regular `Regex_netherlands_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-433">The regular expression  `Regex_netherlands_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ffe7-434">Uma palavra-chave da `Keywords_netherlands_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-434">A keyword from  `Keywords_netherlands_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_passport_number" />
          <Match idRef="Keywords_netherlands_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ffe7-435">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="2ffe7-435">Keywords</span></span>

<span data-ttu-id="2ffe7-436">| |</span><span class="sxs-lookup"><span data-stu-id="2ffe7-436"></span></span>
|<span data-ttu-id="2ffe7-437">**Keywords_netherlands_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="2ffe7-437">**Keywords_netherlands_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="2ffe7-438">número de passaporte holandês</span><span class="sxs-lookup"><span data-stu-id="2ffe7-438">dutch passport number</span></span>  <br/> <span data-ttu-id="2ffe7-439">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="2ffe7-439">passport number</span></span>  <br/> <span data-ttu-id="2ffe7-440">número de passaporte países baixos</span><span class="sxs-lookup"><span data-stu-id="2ffe7-440">netherlands passport number</span></span>  <br/> <span data-ttu-id="2ffe7-441">nederlanden paspoort nummer</span><span class="sxs-lookup"><span data-stu-id="2ffe7-441">nederlanden paspoort nummer</span></span>  <br/> <span data-ttu-id="2ffe7-442">paspoort</span><span class="sxs-lookup"><span data-stu-id="2ffe7-442">paspoort</span></span>  <br/> <span data-ttu-id="2ffe7-443">nederlanden paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="2ffe7-443">nederlanden paspoortnummer</span></span>  <br/> <span data-ttu-id="2ffe7-444">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="2ffe7-444">paspoortnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="2ffe7-445">Polônia</span><span class="sxs-lookup"><span data-stu-id="2ffe7-445">Poland</span></span>

<span data-ttu-id="2ffe7-446">Para obter detalhes, consulte a seção "Número de passaporte da Polônia" nos [quais os tipos de informações confidenciais procurar](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="2ffe7-446">For details, see the section "Poland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="2ffe7-447">Portugal</span><span class="sxs-lookup"><span data-stu-id="2ffe7-447">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="2ffe7-448">Formato</span><span class="sxs-lookup"><span data-stu-id="2ffe7-448">Format</span></span>

<span data-ttu-id="2ffe7-449">Uma letra seguida de seis dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="2ffe7-449">One letter followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ffe7-450">Padrão</span><span class="sxs-lookup"><span data-stu-id="2ffe7-450">Pattern</span></span>

<span data-ttu-id="2ffe7-451">Uma letra seguida de seis dígitos:</span><span class="sxs-lookup"><span data-stu-id="2ffe7-451">One letter followed by six digits:</span></span>
  
- <span data-ttu-id="2ffe7-452">Uma letra (não diferencia maiúscula de minúscula)</span><span class="sxs-lookup"><span data-stu-id="2ffe7-452">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="2ffe7-453">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="2ffe7-453">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="2ffe7-454">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="2ffe7-454">Checksum</span></span>

<span data-ttu-id="2ffe7-455">Não</span><span class="sxs-lookup"><span data-stu-id="2ffe7-455">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ffe7-456">Definição</span><span class="sxs-lookup"><span data-stu-id="2ffe7-456">Definition</span></span>

<span data-ttu-id="2ffe7-457">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="2ffe7-457">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ffe7-458">A expressão regular `Regex_portugal_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-458">The regular expression  `Regex_portugal_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ffe7-459">Uma palavra-chave da `Keywords_portugal_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-459">A keyword from  `Keywords_portugal_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_passport_number" />
          <Match idRef="Keywords_portugal_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ffe7-460">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="2ffe7-460">Keywords</span></span>

<span data-ttu-id="2ffe7-461">| |</span><span class="sxs-lookup"><span data-stu-id="2ffe7-461"></span></span>
|<span data-ttu-id="2ffe7-462">**Keywords_portugal_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="2ffe7-462">**Keywords_portugal_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="2ffe7-463">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="2ffe7-463">passport number</span></span>  <br/> <span data-ttu-id="2ffe7-464">número de passaporte português</span><span class="sxs-lookup"><span data-stu-id="2ffe7-464">portugese passport number</span></span>  <br/> <span data-ttu-id="2ffe7-465">Passport nenhum</span><span class="sxs-lookup"><span data-stu-id="2ffe7-465">passport no</span></span>  <br/> <span data-ttu-id="2ffe7-466">número passaporte</span><span class="sxs-lookup"><span data-stu-id="2ffe7-466">número do passaporte</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="2ffe7-467">Romênia</span><span class="sxs-lookup"><span data-stu-id="2ffe7-467">Romania</span></span>

### <a name="format"></a><span data-ttu-id="2ffe7-468">Formato</span><span class="sxs-lookup"><span data-stu-id="2ffe7-468">Format</span></span>

<span data-ttu-id="2ffe7-469">Oito ou nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="2ffe7-469">Eight or nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ffe7-470">Padrão</span><span class="sxs-lookup"><span data-stu-id="2ffe7-470">Pattern</span></span>

<span data-ttu-id="2ffe7-471">Oito ou nove dígitos</span><span class="sxs-lookup"><span data-stu-id="2ffe7-471">Eight or nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="2ffe7-472">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="2ffe7-472">Checksum</span></span>

<span data-ttu-id="2ffe7-473">Não</span><span class="sxs-lookup"><span data-stu-id="2ffe7-473">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ffe7-474">Definição</span><span class="sxs-lookup"><span data-stu-id="2ffe7-474">Definition</span></span>

<span data-ttu-id="2ffe7-475">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="2ffe7-475">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ffe7-476">A expressão regular `Regex_romania_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-476">The regular expression  `Regex_romania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ffe7-477">Uma palavra-chave da `Keywords_romania_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-477">A keyword from  `Keywords_romania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_passport_number" />
          <Match idRef="Keywords_romania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ffe7-478">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="2ffe7-478">Keywords</span></span>

<span data-ttu-id="2ffe7-479">| |</span><span class="sxs-lookup"><span data-stu-id="2ffe7-479"></span></span>
|<span data-ttu-id="2ffe7-480">**Keywords_romania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="2ffe7-480">**Keywords_romania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="2ffe7-481">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="2ffe7-481">passport number</span></span>  <br/> <span data-ttu-id="2ffe7-482">número de passaporte romeno</span><span class="sxs-lookup"><span data-stu-id="2ffe7-482">romanian passport number</span></span>  <br/> <span data-ttu-id="2ffe7-483">Passport nenhum</span><span class="sxs-lookup"><span data-stu-id="2ffe7-483">passport no</span></span>  <br/> <span data-ttu-id="2ffe7-484">numărul pașaportului</span><span class="sxs-lookup"><span data-stu-id="2ffe7-484">numărul pașaportului</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="2ffe7-485">Eslováquia</span><span class="sxs-lookup"><span data-stu-id="2ffe7-485">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="2ffe7-486">Formato</span><span class="sxs-lookup"><span data-stu-id="2ffe7-486">Format</span></span>

<span data-ttu-id="2ffe7-487">Um dígito ou letra seguido por sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="2ffe7-487">One digit or letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ffe7-488">Padrão</span><span class="sxs-lookup"><span data-stu-id="2ffe7-488">Pattern</span></span>

<span data-ttu-id="2ffe7-489">Um dígito ou carta (não maiusculas de minúsculas) seguido por sete dígitos</span><span class="sxs-lookup"><span data-stu-id="2ffe7-489">One digit or letter (not case sensitive) followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="2ffe7-490">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="2ffe7-490">Checksum</span></span>

<span data-ttu-id="2ffe7-491">Não</span><span class="sxs-lookup"><span data-stu-id="2ffe7-491">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ffe7-492">Definição</span><span class="sxs-lookup"><span data-stu-id="2ffe7-492">Definition</span></span>

<span data-ttu-id="2ffe7-493">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="2ffe7-493">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ffe7-494">A expressão regular `Regex_slovakia_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-494">The regular expression  `Regex_slovakia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ffe7-495">Uma palavra-chave da `Keywords_slovakia_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-495">A keyword from  `Keywords_slovakia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_passport_number" />
          <Match idRef="Keywords_slovakia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ffe7-496">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="2ffe7-496">Keywords</span></span>

<span data-ttu-id="2ffe7-497">| |</span><span class="sxs-lookup"><span data-stu-id="2ffe7-497"></span></span>
|<span data-ttu-id="2ffe7-498">**Keywords_slovakia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="2ffe7-498">**Keywords_slovakia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="2ffe7-499">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="2ffe7-499">passport number</span></span>  <br/> <span data-ttu-id="2ffe7-500">número de passaporte eslovaco</span><span class="sxs-lookup"><span data-stu-id="2ffe7-500">slovakian passport number</span></span>  <br/> <span data-ttu-id="2ffe7-501">Passport nenhum</span><span class="sxs-lookup"><span data-stu-id="2ffe7-501">passport no</span></span>  <br/> <span data-ttu-id="2ffe7-502">Číslo pasu</span><span class="sxs-lookup"><span data-stu-id="2ffe7-502">číslo pasu</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="2ffe7-503">Eslovênia</span><span class="sxs-lookup"><span data-stu-id="2ffe7-503">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="2ffe7-504">Formato</span><span class="sxs-lookup"><span data-stu-id="2ffe7-504">Format</span></span>

<span data-ttu-id="2ffe7-505">Duas letras seguidas por sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="2ffe7-505">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ffe7-506">Padrão</span><span class="sxs-lookup"><span data-stu-id="2ffe7-506">Pattern</span></span>

<span data-ttu-id="2ffe7-507">Duas letras seguidas por sete dígitos:</span><span class="sxs-lookup"><span data-stu-id="2ffe7-507">Two letters followed by seven digits:</span></span>
  
- <span data-ttu-id="2ffe7-508">A letra "P"</span><span class="sxs-lookup"><span data-stu-id="2ffe7-508">The letter "P"</span></span>
    
- <span data-ttu-id="2ffe7-509">Uma letra maiuscula</span><span class="sxs-lookup"><span data-stu-id="2ffe7-509">One uppercase letter</span></span>
    
- <span data-ttu-id="2ffe7-510">Sete dígitos</span><span class="sxs-lookup"><span data-stu-id="2ffe7-510">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="2ffe7-511">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="2ffe7-511">Checksum</span></span>

<span data-ttu-id="2ffe7-512">Não</span><span class="sxs-lookup"><span data-stu-id="2ffe7-512">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ffe7-513">Definição</span><span class="sxs-lookup"><span data-stu-id="2ffe7-513">Definition</span></span>

<span data-ttu-id="2ffe7-514">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="2ffe7-514">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ffe7-515">A expressão regular `Regex_slovenia_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-515">The regular expression  `Regex_slovenia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ffe7-516">Uma palavra-chave da `Keywords_slovenia_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-516">A keyword from  `Keywords_slovenia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_passport_number" />
          <Match idRef="Keywords_slovenia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ffe7-517">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="2ffe7-517">Keywords</span></span>

<span data-ttu-id="2ffe7-518">| |</span><span class="sxs-lookup"><span data-stu-id="2ffe7-518"></span></span>
|<span data-ttu-id="2ffe7-519">**Keywords_slovenia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="2ffe7-519">**Keywords_slovenia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="2ffe7-520">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="2ffe7-520">passport number</span></span>  <br/> <span data-ttu-id="2ffe7-521">número de passaporte esloveno</span><span class="sxs-lookup"><span data-stu-id="2ffe7-521">slovenian passport number</span></span>  <br/> <span data-ttu-id="2ffe7-522">Passport nenhum</span><span class="sxs-lookup"><span data-stu-id="2ffe7-522">passport no</span></span>  <br/> <span data-ttu-id="2ffe7-523">Lista de potnega številka</span><span class="sxs-lookup"><span data-stu-id="2ffe7-523">številka potnega lista</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="2ffe7-524">Espanha</span><span class="sxs-lookup"><span data-stu-id="2ffe7-524">Spain</span></span>

### <a name="format"></a><span data-ttu-id="2ffe7-525">Formato</span><span class="sxs-lookup"><span data-stu-id="2ffe7-525">Format</span></span>

<span data-ttu-id="2ffe7-526">Uma combinação de oito ou nove caracteres de letras e números sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="2ffe7-526">An eight- or nine-character combination of letters and numbers with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ffe7-527">Padrão</span><span class="sxs-lookup"><span data-stu-id="2ffe7-527">Pattern</span></span>

<span data-ttu-id="2ffe7-528">Uma combinação de oito ou nove caracteres de letras e números:</span><span class="sxs-lookup"><span data-stu-id="2ffe7-528">An eight- or nine-character combination of letters and numbers:</span></span>
  
-  <span data-ttu-id="2ffe7-529">Dois dígitos ou letras</span><span class="sxs-lookup"><span data-stu-id="2ffe7-529">Two digits or letters</span></span> 
    
- <span data-ttu-id="2ffe7-530">Um dígito ou carta (opcional)</span><span class="sxs-lookup"><span data-stu-id="2ffe7-530">One digit or letter (optional)</span></span>
    
- <span data-ttu-id="2ffe7-531">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="2ffe7-531">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="2ffe7-532">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="2ffe7-532">Checksum</span></span>

<span data-ttu-id="2ffe7-533">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="2ffe7-533">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ffe7-534">Definição</span><span class="sxs-lookup"><span data-stu-id="2ffe7-534">Definition</span></span>

<span data-ttu-id="2ffe7-535">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="2ffe7-535">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ffe7-536">A expressão regular `Regex_spain_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-536">The regular expression  `Regex_spain_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ffe7-537">Uma palavra-chave da `Keywords_spain_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="2ffe7-537">A keyword from  `Keywords_spain_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_passport_number" />
          <Match idRef="Keywords_spain_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ffe7-538">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="2ffe7-538">Keywords</span></span>

<span data-ttu-id="2ffe7-539">| |</span><span class="sxs-lookup"><span data-stu-id="2ffe7-539"></span></span>
|<span data-ttu-id="2ffe7-540">**Keywords_spain_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="2ffe7-540">**Keywords_spain_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="2ffe7-541">passport</span><span class="sxs-lookup"><span data-stu-id="2ffe7-541">passport</span></span>  <br/> <span data-ttu-id="2ffe7-542">passaporte da Espanha</span><span class="sxs-lookup"><span data-stu-id="2ffe7-542">spain passport</span></span>  <br/> <span data-ttu-id="2ffe7-543">Catálogo do Passport</span><span class="sxs-lookup"><span data-stu-id="2ffe7-543">passport book</span></span>  <br/> <span data-ttu-id="2ffe7-544">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="2ffe7-544">passport number</span></span>  <br/> <span data-ttu-id="2ffe7-545">Passport nenhum</span><span class="sxs-lookup"><span data-stu-id="2ffe7-545">passport no</span></span>  <br/> <span data-ttu-id="2ffe7-546">libreta pasaporte</span><span class="sxs-lookup"><span data-stu-id="2ffe7-546">libreta pasaporte</span></span>  <br/> <span data-ttu-id="2ffe7-547">número pasaporte</span><span class="sxs-lookup"><span data-stu-id="2ffe7-547">número pasaporte</span></span>  <br/> <span data-ttu-id="2ffe7-548">españa pasaporte</span><span class="sxs-lookup"><span data-stu-id="2ffe7-548">españa pasaporte</span></span>  <br/> <span data-ttu-id="2ffe7-549">pasaporte</span><span class="sxs-lookup"><span data-stu-id="2ffe7-549">pasaporte</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="2ffe7-550">Suécia</span><span class="sxs-lookup"><span data-stu-id="2ffe7-550">Sweden</span></span>

<span data-ttu-id="2ffe7-551">Para obter detalhes, consulte a seção "Número de passaporte da Suécia" nos [quais os tipos de informações confidenciais procurar](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="2ffe7-551">For details, see the section "Sweden Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="uk"></a><span data-ttu-id="2ffe7-552">REINO UNIDO</span><span class="sxs-lookup"><span data-stu-id="2ffe7-552">UK</span></span>

<span data-ttu-id="2ffe7-p103">Para obter detalhes, consulte a seção "Número de passaporte US / Reino Unido" nos [quais os tipos de informações confidenciais procurar](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="2ffe7-p103">For details, see the section "U.S. / U.K. Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2ffe7-555">Confira também</span><span class="sxs-lookup"><span data-stu-id="2ffe7-555">See also</span></span>

[<span data-ttu-id="2ffe7-556">O que os tipos de informações confidenciais procuram</span><span class="sxs-lookup"><span data-stu-id="2ffe7-556">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)


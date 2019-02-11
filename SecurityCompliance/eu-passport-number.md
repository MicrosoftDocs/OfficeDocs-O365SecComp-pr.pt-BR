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
ms.openlocfilehash: 7a7fc1ff826aab4096c46535686eb0fd68173c6f
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2019
ms.locfileid: "25840320"
---
# <a name="eu-passport-number"></a><span data-ttu-id="aaef6-104">Número de passaporte da UE</span><span class="sxs-lookup"><span data-stu-id="aaef6-104">EU Passport Number</span></span>

<span data-ttu-id="aaef6-p102">Este tópico mostra o que uma política de prevenção (DLP) de perda de dados procura por quando detecta o tipo de informações confidenciais de número de passaporte da UE. Esse tipo de informações confidenciais define diferentes padrões, palavras-chave e outras evidências para cada país.</span><span class="sxs-lookup"><span data-stu-id="aaef6-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Passport Number sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="aaef6-107">Áustria</span><span class="sxs-lookup"><span data-stu-id="aaef6-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="aaef6-108">Formato</span><span class="sxs-lookup"><span data-stu-id="aaef6-108">Format</span></span>

<span data-ttu-id="aaef6-109">Uma letra seguida por um espaço opcional e sete dígitos</span><span class="sxs-lookup"><span data-stu-id="aaef6-109">One letter followed by an optional space and seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="aaef6-110">Padrão</span><span class="sxs-lookup"><span data-stu-id="aaef6-110">Pattern</span></span>

<span data-ttu-id="aaef6-111">Uma combinação de uma letra, um espaço e sete dígitos:</span><span class="sxs-lookup"><span data-stu-id="aaef6-111">A combination of one letter, seven digits, and one space:</span></span>
  
- <span data-ttu-id="aaef6-112">Uma letra (não diferencia maiúscula de minúscula)</span><span class="sxs-lookup"><span data-stu-id="aaef6-112">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="aaef6-113">Um espaço (opcional)</span><span class="sxs-lookup"><span data-stu-id="aaef6-113">One space (optional)</span></span>
    
- <span data-ttu-id="aaef6-114">Sete dígitos</span><span class="sxs-lookup"><span data-stu-id="aaef6-114">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="aaef6-115">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="aaef6-115">Checksum</span></span>

<span data-ttu-id="aaef6-116">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="aaef6-116">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="aaef6-117">Definição</span><span class="sxs-lookup"><span data-stu-id="aaef6-117">Definition</span></span>

<span data-ttu-id="aaef6-118">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="aaef6-118">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="aaef6-119">A expressão regular `Regex_austria_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="aaef6-119">The regular expression  `Regex_austria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="aaef6-120">Uma palavra-chave da `Keywords_austria_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="aaef6-120">A keyword from  `Keywords_austria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_passport_number" />
          <Match idRef="Keywords_austria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="aaef6-121">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="aaef6-121">Keywords</span></span>

<span data-ttu-id="aaef6-122">| |</span><span class="sxs-lookup"><span data-stu-id="aaef6-122"></span></span>
|<span data-ttu-id="aaef6-123">**Keywords_austria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="aaef6-123">**Keywords_austria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="aaef6-124">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="aaef6-124">passport number</span></span>  <br/> <span data-ttu-id="aaef6-125">número de passaporte austríaco</span><span class="sxs-lookup"><span data-stu-id="aaef6-125">austrian passport number</span></span>  <br/> <span data-ttu-id="aaef6-126">Passport nenhum</span><span class="sxs-lookup"><span data-stu-id="aaef6-126">passport no</span></span>  <br/> <span data-ttu-id="aaef6-127">reisepass</span><span class="sxs-lookup"><span data-stu-id="aaef6-127">reisepass</span></span>  <br/> <span data-ttu-id="aaef6-128">österreichisch reisepass</span><span class="sxs-lookup"><span data-stu-id="aaef6-128">österreichisch reisepass</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="aaef6-129">Bélgica</span><span class="sxs-lookup"><span data-stu-id="aaef6-129">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="aaef6-130">Formato</span><span class="sxs-lookup"><span data-stu-id="aaef6-130">Format</span></span>

<span data-ttu-id="aaef6-131">Duas letras seguidas de seis dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="aaef6-131">Two letters followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="aaef6-132">Padrão</span><span class="sxs-lookup"><span data-stu-id="aaef6-132">Pattern</span></span>

<span data-ttu-id="aaef6-133">Duas letras e seguido de seis dígitos</span><span class="sxs-lookup"><span data-stu-id="aaef6-133">Two letters and followed by six digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="aaef6-134">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="aaef6-134">Checksum</span></span>

<span data-ttu-id="aaef6-135">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="aaef6-135">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="aaef6-136">Definição</span><span class="sxs-lookup"><span data-stu-id="aaef6-136">Definition</span></span>

<span data-ttu-id="aaef6-137">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="aaef6-137">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="aaef6-138">A expressão regular `Regex_belgium_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="aaef6-138">The regular expression  `Regex_belgium_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="aaef6-139">Uma palavra-chave da `Keywords_belgium_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="aaef6-139">A keyword from  `Keywords_belgium_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium__eu_passport_number" />
          <Match idRef="Keywords_belgium_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="aaef6-140">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="aaef6-140">Keywords</span></span>

<span data-ttu-id="aaef6-141">| |</span><span class="sxs-lookup"><span data-stu-id="aaef6-141"></span></span>
|<span data-ttu-id="aaef6-142">**Keywords_belgium_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="aaef6-142">**Keywords_belgium_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="aaef6-143">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="aaef6-143">passport number</span></span>  <br/> <span data-ttu-id="aaef6-144">número de passaporte belga</span><span class="sxs-lookup"><span data-stu-id="aaef6-144">belgian passport number</span></span>  <br/> <span data-ttu-id="aaef6-145">Passport nenhum</span><span class="sxs-lookup"><span data-stu-id="aaef6-145">passport no</span></span>  <br/> <span data-ttu-id="aaef6-146">paspoort</span><span class="sxs-lookup"><span data-stu-id="aaef6-146">paspoort</span></span>  <br/> <span data-ttu-id="aaef6-147">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="aaef6-147">paspoortnummer</span></span>  <br/> <span data-ttu-id="aaef6-148">reisepass kein</span><span class="sxs-lookup"><span data-stu-id="aaef6-148">reisepass kein</span></span>  <br/> <span data-ttu-id="aaef6-149">reisepass</span><span class="sxs-lookup"><span data-stu-id="aaef6-149">reisepass</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="aaef6-150">Bulgária</span><span class="sxs-lookup"><span data-stu-id="aaef6-150">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="aaef6-151">Formato</span><span class="sxs-lookup"><span data-stu-id="aaef6-151">Format</span></span>

<span data-ttu-id="aaef6-152">Nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="aaef6-152">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="aaef6-153">Padrão</span><span class="sxs-lookup"><span data-stu-id="aaef6-153">Pattern</span></span>

 <span data-ttu-id="aaef6-154">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="aaef6-154">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="aaef6-155">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="aaef6-155">Checksum</span></span>

<span data-ttu-id="aaef6-156">Não</span><span class="sxs-lookup"><span data-stu-id="aaef6-156">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="aaef6-157">Definição</span><span class="sxs-lookup"><span data-stu-id="aaef6-157">Definition</span></span>

<span data-ttu-id="aaef6-158">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="aaef6-158">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="aaef6-159">A expressão regular `Regex_bulgaria_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="aaef6-159">The regular expression  `Regex_bulgaria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="aaef6-160">Uma palavra-chave da `Keywords_bulgaria_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="aaef6-160">A keyword from  `Keywords_bulgaria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_passport_number" />
          <Match idRef="Keywords_bulgaria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="aaef6-161">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="aaef6-161">Keywords</span></span>

<span data-ttu-id="aaef6-162">| |</span><span class="sxs-lookup"><span data-stu-id="aaef6-162"></span></span>
|<span data-ttu-id="aaef6-163">**Keywords_bulgaria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="aaef6-163">**Keywords_bulgaria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="aaef6-164">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="aaef6-164">passport number</span></span>  <br/> <span data-ttu-id="aaef6-165">número de passaporte búlgaro</span><span class="sxs-lookup"><span data-stu-id="aaef6-165">bulgarian passport number</span></span>  <br/> <span data-ttu-id="aaef6-166">Passport nenhum</span><span class="sxs-lookup"><span data-stu-id="aaef6-166">passport no</span></span>  <br/> <span data-ttu-id="aaef6-167">НОМЕР НА ПАСПОРТА</span><span class="sxs-lookup"><span data-stu-id="aaef6-167">номер на паспорта</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="aaef6-168">Croácia</span><span class="sxs-lookup"><span data-stu-id="aaef6-168">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="aaef6-169">Formato</span><span class="sxs-lookup"><span data-stu-id="aaef6-169">Format</span></span>

<span data-ttu-id="aaef6-170">Nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="aaef6-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="aaef6-171">Padrão</span><span class="sxs-lookup"><span data-stu-id="aaef6-171">Pattern</span></span>

 <span data-ttu-id="aaef6-172">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="aaef6-172">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="aaef6-173">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="aaef6-173">Checksum</span></span>

<span data-ttu-id="aaef6-174">Não</span><span class="sxs-lookup"><span data-stu-id="aaef6-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="aaef6-175">Definição</span><span class="sxs-lookup"><span data-stu-id="aaef6-175">Definition</span></span>

<span data-ttu-id="aaef6-176">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="aaef6-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="aaef6-177">A expressão regular `Regex_croatia_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="aaef6-177">The regular expression  `Regex_croatia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="aaef6-178">Uma palavra-chave da `Keywords_croatia_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="aaef6-178">A keyword from  `Keywords_croatia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_passport_number" />
          <Match idRef="Keywords_croatia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="aaef6-179">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="aaef6-179">Keywords</span></span>

<span data-ttu-id="aaef6-180">| |</span><span class="sxs-lookup"><span data-stu-id="aaef6-180"></span></span>
|<span data-ttu-id="aaef6-181">**Keywords_croatia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="aaef6-181">**Keywords_croatia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="aaef6-182">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="aaef6-182">passport number</span></span>  <br/> <span data-ttu-id="aaef6-183">número de passaporte croata</span><span class="sxs-lookup"><span data-stu-id="aaef6-183">croatian passport number</span></span>  <br/> <span data-ttu-id="aaef6-184">Passport nenhum</span><span class="sxs-lookup"><span data-stu-id="aaef6-184">passport no</span></span>  <br/> <span data-ttu-id="aaef6-185">broj putovnice</span><span class="sxs-lookup"><span data-stu-id="aaef6-185">broj putovnice</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="aaef6-186">Chipre</span><span class="sxs-lookup"><span data-stu-id="aaef6-186">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="aaef6-187">Formato</span><span class="sxs-lookup"><span data-stu-id="aaef6-187">Format</span></span>

<span data-ttu-id="aaef6-188">Uma letra seguida de 6 a 8 dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="aaef6-188">One letter followed by 6-8 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="aaef6-189">Padrão</span><span class="sxs-lookup"><span data-stu-id="aaef6-189">Pattern</span></span>

<span data-ttu-id="aaef6-190">Uma letra seguida de seis a oito dígitos</span><span class="sxs-lookup"><span data-stu-id="aaef6-190">One letter followed by six to eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="aaef6-191">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="aaef6-191">Checksum</span></span>

<span data-ttu-id="aaef6-192">Não</span><span class="sxs-lookup"><span data-stu-id="aaef6-192">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="aaef6-193">Definição</span><span class="sxs-lookup"><span data-stu-id="aaef6-193">Definition</span></span>

<span data-ttu-id="aaef6-194">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="aaef6-194">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="aaef6-195">A expressão regular `Regex_cyprus_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="aaef6-195">The regular expression  `Regex_cyprus_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="aaef6-196">Uma palavra-chave da `Keywords_cyprus_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="aaef6-196">A keyword from  `Keywords_cyprus_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_passport_number" />
          <Match idRef="Keywords_cyprus_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="aaef6-197">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="aaef6-197">Keywords</span></span>

<span data-ttu-id="aaef6-198">| |</span><span class="sxs-lookup"><span data-stu-id="aaef6-198"></span></span>
|<span data-ttu-id="aaef6-199">**Keywords_cyprus_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="aaef6-199">**Keywords_cyprus_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="aaef6-200">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="aaef6-200">passport number</span></span>  <br/> <span data-ttu-id="aaef6-201">número de passaporte Chipre</span><span class="sxs-lookup"><span data-stu-id="aaef6-201">cyprus passport number</span></span>  <br/> <span data-ttu-id="aaef6-202">Passport nenhum</span><span class="sxs-lookup"><span data-stu-id="aaef6-202">passport no</span></span>  <br/> <span data-ttu-id="aaef6-203">ΑΡΙΘΜΌ ΔΙΑΒΑΤΗΡΊΟΥ</span><span class="sxs-lookup"><span data-stu-id="aaef6-203">αριθμό διαβατηρίου</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="aaef6-204">República Tcheca</span><span class="sxs-lookup"><span data-stu-id="aaef6-204">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="aaef6-205">Formato</span><span class="sxs-lookup"><span data-stu-id="aaef6-205">Format</span></span>

<span data-ttu-id="aaef6-206">Oito dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="aaef6-206">Eight digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="aaef6-207">Padrão</span><span class="sxs-lookup"><span data-stu-id="aaef6-207">Pattern</span></span>

<span data-ttu-id="aaef6-208">Oito dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="aaef6-208">Eight digits without spaces or delimiters</span></span>
  
### <a name="checksum"></a><span data-ttu-id="aaef6-209">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="aaef6-209">Checksum</span></span>

<span data-ttu-id="aaef6-210">Não</span><span class="sxs-lookup"><span data-stu-id="aaef6-210">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="aaef6-211">Definição</span><span class="sxs-lookup"><span data-stu-id="aaef6-211">Definition</span></span>

<span data-ttu-id="aaef6-212">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="aaef6-212">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="aaef6-213">A expressão regular `Regex_czech_republic_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="aaef6-213">The regular expression  `Regex_czech_republic_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="aaef6-214">Uma palavra-chave da `Keywords_czech_republic_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="aaef6-214">A keyword from  `Keywords_czech_republic_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_passport_number" />
          <Match idRef="Keywords_czech_republic_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="aaef6-215">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="aaef6-215">Keywords</span></span>

<span data-ttu-id="aaef6-216">| |</span><span class="sxs-lookup"><span data-stu-id="aaef6-216"></span></span>
|<span data-ttu-id="aaef6-217">**Keywords_czech_republic_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="aaef6-217">**Keywords_czech_republic_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="aaef6-218">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="aaef6-218">passport number</span></span>  <br/> <span data-ttu-id="aaef6-219">número de passaporte tcheco</span><span class="sxs-lookup"><span data-stu-id="aaef6-219">czech passport number</span></span>  <br/> <span data-ttu-id="aaef6-220">Passport nenhum</span><span class="sxs-lookup"><span data-stu-id="aaef6-220">passport no</span></span>  <br/> <span data-ttu-id="aaef6-221">cestovní pas</span><span class="sxs-lookup"><span data-stu-id="aaef6-221">cestovní pas</span></span>  <br/> <span data-ttu-id="aaef6-222">PAS</span><span class="sxs-lookup"><span data-stu-id="aaef6-222">pas</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="aaef6-223">Dinamarca</span><span class="sxs-lookup"><span data-stu-id="aaef6-223">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="aaef6-224">Formato</span><span class="sxs-lookup"><span data-stu-id="aaef6-224">Format</span></span>

<span data-ttu-id="aaef6-225">Nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="aaef6-225">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="aaef6-226">Padrão</span><span class="sxs-lookup"><span data-stu-id="aaef6-226">Pattern</span></span>

 <span data-ttu-id="aaef6-227">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="aaef6-227">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="aaef6-228">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="aaef6-228">Checksum</span></span>

<span data-ttu-id="aaef6-229">Não</span><span class="sxs-lookup"><span data-stu-id="aaef6-229">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="aaef6-230">Definição</span><span class="sxs-lookup"><span data-stu-id="aaef6-230">Definition</span></span>

<span data-ttu-id="aaef6-231">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="aaef6-231">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="aaef6-232">A expressão regular `Regex_denmark_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="aaef6-232">The regular expression  `Regex_denmark_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="aaef6-233">Uma palavra-chave da `Keywords_denmark_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="aaef6-233">A keyword from  `Keywords_denmark_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_passport_number" />
          <Match idRef="Keywords_denmark_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="aaef6-234">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="aaef6-234">Keywords</span></span>

<span data-ttu-id="aaef6-235">| |</span><span class="sxs-lookup"><span data-stu-id="aaef6-235"></span></span>
|<span data-ttu-id="aaef6-236">**Keywords_denmark_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="aaef6-236">**Keywords_denmark_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="aaef6-237">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="aaef6-237">passport number</span></span>  <br/> <span data-ttu-id="aaef6-238">número de passaporte dinamarquês</span><span class="sxs-lookup"><span data-stu-id="aaef6-238">danish passport number</span></span>  <br/> <span data-ttu-id="aaef6-239">Passport nenhum</span><span class="sxs-lookup"><span data-stu-id="aaef6-239">passport no</span></span>  <br/> <span data-ttu-id="aaef6-240">PAS</span><span class="sxs-lookup"><span data-stu-id="aaef6-240">pas</span></span>  <br/> <span data-ttu-id="aaef6-241">pasnummer</span><span class="sxs-lookup"><span data-stu-id="aaef6-241">pasnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="aaef6-242">Estônia</span><span class="sxs-lookup"><span data-stu-id="aaef6-242">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="aaef6-243">Formato</span><span class="sxs-lookup"><span data-stu-id="aaef6-243">Format</span></span>

<span data-ttu-id="aaef6-244">Uma letra seguida por sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="aaef6-244">One letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="aaef6-245">Padrão</span><span class="sxs-lookup"><span data-stu-id="aaef6-245">Pattern</span></span>

<span data-ttu-id="aaef6-246">Uma letra seguida por sete dígitos</span><span class="sxs-lookup"><span data-stu-id="aaef6-246">One letter followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="aaef6-247">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="aaef6-247">Checksum</span></span>

<span data-ttu-id="aaef6-248">Não</span><span class="sxs-lookup"><span data-stu-id="aaef6-248">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="aaef6-249">Definição</span><span class="sxs-lookup"><span data-stu-id="aaef6-249">Definition</span></span>

<span data-ttu-id="aaef6-250">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="aaef6-250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="aaef6-251">A expressão regular `Regex_estonia_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="aaef6-251">The regular expression  `Regex_estonia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="aaef6-252">Uma palavra-chave da `Keywords_estonia_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="aaef6-252">A keyword from  `Keywords_estonia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_passport_number" />
          <Match idRef="Keywords_estonia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="aaef6-253">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="aaef6-253">Keywords</span></span>

<span data-ttu-id="aaef6-254">| |</span><span class="sxs-lookup"><span data-stu-id="aaef6-254"></span></span>
|<span data-ttu-id="aaef6-255">**Keywords_estonia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="aaef6-255">**Keywords_estonia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="aaef6-256">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="aaef6-256">passport number</span></span>  <br/> <span data-ttu-id="aaef6-257">número de passaporte estoniano</span><span class="sxs-lookup"><span data-stu-id="aaef6-257">estonian passport number</span></span>  <br/> <span data-ttu-id="aaef6-258">Passport nenhum</span><span class="sxs-lookup"><span data-stu-id="aaef6-258">passport no</span></span>  <br/> <span data-ttu-id="aaef6-259">eesti kodaniku secreta</span><span class="sxs-lookup"><span data-stu-id="aaef6-259">eesti kodaniku pass</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="aaef6-260">Finlândia</span><span class="sxs-lookup"><span data-stu-id="aaef6-260">Finland</span></span>

<span data-ttu-id="aaef6-261">Para obter detalhes, consulte a seção "Número de passaporte da Finlândia" nos [quais os tipos de informações confidenciais procurar](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="aaef6-261">For details, see the section "Finland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="aaef6-262">França</span><span class="sxs-lookup"><span data-stu-id="aaef6-262">France</span></span>

<span data-ttu-id="aaef6-263">Para obter detalhes, consulte a seção "Número de passaporte da França" nos [quais os tipos de informações confidenciais procurar](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="aaef6-263">For details, see the section "France Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="aaef6-264">Alemanha</span><span class="sxs-lookup"><span data-stu-id="aaef6-264">Germany</span></span>

<span data-ttu-id="aaef6-265">Para obter detalhes, consulte a seção "Número de passaporte da Alemanha" em [quais tipos de informações confidenciais a procurar](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="aaef6-265">For details, see the section "Germany Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="aaef6-266">Grécia</span><span class="sxs-lookup"><span data-stu-id="aaef6-266">Greece</span></span>

### <a name="format"></a><span data-ttu-id="aaef6-267">Formato</span><span class="sxs-lookup"><span data-stu-id="aaef6-267">Format</span></span>

<span data-ttu-id="aaef6-268">Duas letras seguidas por sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="aaef6-268">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="aaef6-269">Padrão</span><span class="sxs-lookup"><span data-stu-id="aaef6-269">Pattern</span></span>

<span data-ttu-id="aaef6-270">Duas letras seguidas por sete dígitos</span><span class="sxs-lookup"><span data-stu-id="aaef6-270">Two letters followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="aaef6-271">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="aaef6-271">Checksum</span></span>

<span data-ttu-id="aaef6-272">Não</span><span class="sxs-lookup"><span data-stu-id="aaef6-272">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="aaef6-273">Definição</span><span class="sxs-lookup"><span data-stu-id="aaef6-273">Definition</span></span>

<span data-ttu-id="aaef6-274">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="aaef6-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="aaef6-275">A expressão regular `Regex_greece_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="aaef6-275">The regular expression  `Regex_greece_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="aaef6-276">Uma palavra-chave da `Keywords_greece_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="aaef6-276">A keyword from  `Keywords_greece_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_passport_number" />
          <Match idRef="Keywords_greece_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="aaef6-277">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="aaef6-277">Keywords</span></span>

<span data-ttu-id="aaef6-278">| |</span><span class="sxs-lookup"><span data-stu-id="aaef6-278"></span></span>
|<span data-ttu-id="aaef6-279">**Keywords_greece_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="aaef6-279">**Keywords_greece_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="aaef6-280">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="aaef6-280">passport number</span></span>  <br/> <span data-ttu-id="aaef6-281">número de passaporte grego</span><span class="sxs-lookup"><span data-stu-id="aaef6-281">greek passport number</span></span>  <br/> <span data-ttu-id="aaef6-282">Passport nenhum</span><span class="sxs-lookup"><span data-stu-id="aaef6-282">passport no</span></span>  <br/> <span data-ttu-id="aaef6-283">ΔΙΑΒΑΤΗΡΙΟ</span><span class="sxs-lookup"><span data-stu-id="aaef6-283">διαβατηριο</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="aaef6-284">Hungria</span><span class="sxs-lookup"><span data-stu-id="aaef6-284">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="aaef6-285">Formato</span><span class="sxs-lookup"><span data-stu-id="aaef6-285">Format</span></span>

<span data-ttu-id="aaef6-286">Duas letras seguidas por seis ou sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="aaef6-286">Two letters followed by six or seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="aaef6-287">Padrão</span><span class="sxs-lookup"><span data-stu-id="aaef6-287">Pattern</span></span>

<span data-ttu-id="aaef6-288">Duas letras seguidas por seis ou sete dígitos</span><span class="sxs-lookup"><span data-stu-id="aaef6-288">Two letters followed by six or seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="aaef6-289">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="aaef6-289">Checksum</span></span>

<span data-ttu-id="aaef6-290">Não</span><span class="sxs-lookup"><span data-stu-id="aaef6-290">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="aaef6-291">Definição</span><span class="sxs-lookup"><span data-stu-id="aaef6-291">Definition</span></span>

<span data-ttu-id="aaef6-292">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="aaef6-292">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="aaef6-293">A expressão regular `Regex_hungary_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="aaef6-293">The regular expression  `Regex_hungary_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="aaef6-294">Uma palavra-chave da `Keywords_hungary_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="aaef6-294">A keyword from  `Keywords_hungary_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_passport_number" />
          <Match idRef="Keywords_hungary_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="aaef6-295">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="aaef6-295">Keywords</span></span>

<span data-ttu-id="aaef6-296">| |</span><span class="sxs-lookup"><span data-stu-id="aaef6-296"></span></span>
|<span data-ttu-id="aaef6-297">**Keywords_hungary_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="aaef6-297">**Keywords_hungary_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="aaef6-298">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="aaef6-298">passport number</span></span>  <br/> <span data-ttu-id="aaef6-299">número de passaporte húngaro</span><span class="sxs-lookup"><span data-stu-id="aaef6-299">hungarian passport number</span></span>  <br/> <span data-ttu-id="aaef6-300">Passport nenhum</span><span class="sxs-lookup"><span data-stu-id="aaef6-300">passport no</span></span>  <br/> <span data-ttu-id="aaef6-301">útlevél száma</span><span class="sxs-lookup"><span data-stu-id="aaef6-301">útlevél száma</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="aaef6-302">Irlanda</span><span class="sxs-lookup"><span data-stu-id="aaef6-302">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="aaef6-303">Formato</span><span class="sxs-lookup"><span data-stu-id="aaef6-303">Format</span></span>

<span data-ttu-id="aaef6-304">Duas letras ou dígitos seguidos por sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="aaef6-304">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="aaef6-305">Padrão</span><span class="sxs-lookup"><span data-stu-id="aaef6-305">Pattern</span></span>

<span data-ttu-id="aaef6-306">Duas letras ou dígitos seguidos por sete dígitos:</span><span class="sxs-lookup"><span data-stu-id="aaef6-306">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="aaef6-307">Dois dígitos ou letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="aaef6-307">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="aaef6-308">Sete dígitos</span><span class="sxs-lookup"><span data-stu-id="aaef6-308">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="aaef6-309">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="aaef6-309">Checksum</span></span>

<span data-ttu-id="aaef6-310">Não</span><span class="sxs-lookup"><span data-stu-id="aaef6-310">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="aaef6-311">Definição</span><span class="sxs-lookup"><span data-stu-id="aaef6-311">Definition</span></span>

<span data-ttu-id="aaef6-312">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="aaef6-312">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="aaef6-313">A expressão regular `Regex_ireland_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="aaef6-313">The regular expression  `Regex_ireland_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="aaef6-314">Uma palavra-chave da `Keywords_ireland_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="aaef6-314">A keyword from  `Keywords_ireland_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_passport_number" />
          <Match idRef="Keywords_ireland_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="aaef6-315">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="aaef6-315">Keywords</span></span>

<span data-ttu-id="aaef6-316">| |</span><span class="sxs-lookup"><span data-stu-id="aaef6-316"></span></span>
|<span data-ttu-id="aaef6-317">**Keywords_ireland_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="aaef6-317">**Keywords_ireland_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="aaef6-318">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="aaef6-318">passport number</span></span>  <br/> <span data-ttu-id="aaef6-319">número de passaporte irlandês</span><span class="sxs-lookup"><span data-stu-id="aaef6-319">irish passport number</span></span>  <br/> <span data-ttu-id="aaef6-320">Passport nenhum</span><span class="sxs-lookup"><span data-stu-id="aaef6-320">passport no</span></span>  <br/> <span data-ttu-id="aaef6-321">PAS</span><span class="sxs-lookup"><span data-stu-id="aaef6-321">pas</span></span>  <br/> <span data-ttu-id="aaef6-322">passport</span><span class="sxs-lookup"><span data-stu-id="aaef6-322">passport</span></span>  <br/> <span data-ttu-id="aaef6-323">passeport</span><span class="sxs-lookup"><span data-stu-id="aaef6-323">passeport</span></span>  <br/> <span data-ttu-id="aaef6-324">numero passeport</span><span class="sxs-lookup"><span data-stu-id="aaef6-324">passeport numero</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="aaef6-325">Itália</span><span class="sxs-lookup"><span data-stu-id="aaef6-325">Italy</span></span>

### <a name="format"></a><span data-ttu-id="aaef6-326">Formato</span><span class="sxs-lookup"><span data-stu-id="aaef6-326">Format</span></span>

<span data-ttu-id="aaef6-327">Duas letras ou dígitos seguidos por sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="aaef6-327">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="aaef6-328">Padrão</span><span class="sxs-lookup"><span data-stu-id="aaef6-328">Pattern</span></span>

<span data-ttu-id="aaef6-329">Duas letras ou dígitos seguidos por sete dígitos:</span><span class="sxs-lookup"><span data-stu-id="aaef6-329">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="aaef6-330">Dois dígitos ou letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="aaef6-330">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="aaef6-331">Sete dígitos</span><span class="sxs-lookup"><span data-stu-id="aaef6-331">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="aaef6-332">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="aaef6-332">Checksum</span></span>

<span data-ttu-id="aaef6-333">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="aaef6-333">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="aaef6-334">Definição</span><span class="sxs-lookup"><span data-stu-id="aaef6-334">Definition</span></span>

<span data-ttu-id="aaef6-335">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="aaef6-335">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="aaef6-336">A expressão regular `Regex_italy_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="aaef6-336">The regular expression  `Regex_italy_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="aaef6-337">Uma palavra-chave da `Keywords_italy_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="aaef6-337">A keyword from  `Keywords_italy_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_passport_number" />
          <Match idRef="Keywords_italy_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="aaef6-338">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="aaef6-338">Keywords</span></span>

<span data-ttu-id="aaef6-339">| |</span><span class="sxs-lookup"><span data-stu-id="aaef6-339"></span></span>
|<span data-ttu-id="aaef6-340">**Keywords_italy_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="aaef6-340">**Keywords_italy_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="aaef6-341">número de passaporte italiano</span><span class="sxs-lookup"><span data-stu-id="aaef6-341">italian passport number</span></span>  <br/> <span data-ttu-id="aaef6-342">repubblica italiana passaporto</span><span class="sxs-lookup"><span data-stu-id="aaef6-342">repubblica italiana passaporto</span></span>  <br/> <span data-ttu-id="aaef6-343">passaporto</span><span class="sxs-lookup"><span data-stu-id="aaef6-343">passaporto</span></span>  <br/> <span data-ttu-id="aaef6-344">passaporto italiana</span><span class="sxs-lookup"><span data-stu-id="aaef6-344">passaporto italiana</span></span>  <br/> <span data-ttu-id="aaef6-345">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="aaef6-345">passport number</span></span>  <br/> <span data-ttu-id="aaef6-346">italiana passaporto numero</span><span class="sxs-lookup"><span data-stu-id="aaef6-346">italiana passaporto numero</span></span>  <br/> <span data-ttu-id="aaef6-347">numero passaporto</span><span class="sxs-lookup"><span data-stu-id="aaef6-347">passaporto numero</span></span>  <br/> <span data-ttu-id="aaef6-348">numéro passeport italien</span><span class="sxs-lookup"><span data-stu-id="aaef6-348">numéro passeport italien</span></span>  <br/> <span data-ttu-id="aaef6-349">numéro passeport</span><span class="sxs-lookup"><span data-stu-id="aaef6-349">numéro passeport</span></span>  <br/> |
   
## <a name="latvia"></a><span data-ttu-id="aaef6-350">Letônia</span><span class="sxs-lookup"><span data-stu-id="aaef6-350">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="aaef6-351">Formato</span><span class="sxs-lookup"><span data-stu-id="aaef6-351">Format</span></span>

<span data-ttu-id="aaef6-352">Duas letras ou dígitos seguidos por sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="aaef6-352">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="aaef6-353">Padrão</span><span class="sxs-lookup"><span data-stu-id="aaef6-353">Pattern</span></span>

<span data-ttu-id="aaef6-354">Duas letras ou dígitos seguidos por sete dígitos:</span><span class="sxs-lookup"><span data-stu-id="aaef6-354">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="aaef6-355">Dois dígitos ou letras (não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="aaef6-355">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="aaef6-356">Sete dígitos</span><span class="sxs-lookup"><span data-stu-id="aaef6-356">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="aaef6-357">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="aaef6-357">Checksum</span></span>

<span data-ttu-id="aaef6-358">Não</span><span class="sxs-lookup"><span data-stu-id="aaef6-358">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="aaef6-359">Definição</span><span class="sxs-lookup"><span data-stu-id="aaef6-359">Definition</span></span>

<span data-ttu-id="aaef6-360">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="aaef6-360">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="aaef6-361">A expressão regular `Regex_latvia_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="aaef6-361">The regular expression  `Regex_latvia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="aaef6-362">Uma palavra-chave da `Keywords_latvia_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="aaef6-362">A keyword from  `Keywords_latvia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_passport_number" />
          <Match idRef="Keywords_latvia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="aaef6-363">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="aaef6-363">Keywords</span></span>

<span data-ttu-id="aaef6-364">| |</span><span class="sxs-lookup"><span data-stu-id="aaef6-364"></span></span>
|<span data-ttu-id="aaef6-365">**Keywords_latvia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="aaef6-365">**Keywords_latvia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="aaef6-366">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="aaef6-366">passport number</span></span>  <br/> <span data-ttu-id="aaef6-367">número de passaporte letão</span><span class="sxs-lookup"><span data-stu-id="aaef6-367">latvian passport number</span></span>  <br/> <span data-ttu-id="aaef6-368">Passport nenhum</span><span class="sxs-lookup"><span data-stu-id="aaef6-368">passport no</span></span>  <br/> <span data-ttu-id="aaef6-369">pase numurs</span><span class="sxs-lookup"><span data-stu-id="aaef6-369">pase numurs</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="aaef6-370">Lituânia</span><span class="sxs-lookup"><span data-stu-id="aaef6-370">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="aaef6-371">Formato</span><span class="sxs-lookup"><span data-stu-id="aaef6-371">Format</span></span>

<span data-ttu-id="aaef6-372">Oito dígitos ou letras sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="aaef6-372">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="aaef6-373">Padrão</span><span class="sxs-lookup"><span data-stu-id="aaef6-373">Pattern</span></span>

<span data-ttu-id="aaef6-374">Oito dígitos ou letras (não maiusculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="aaef6-374">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="aaef6-375">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="aaef6-375">Checksum</span></span>

<span data-ttu-id="aaef6-376">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="aaef6-376">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="aaef6-377">Definição</span><span class="sxs-lookup"><span data-stu-id="aaef6-377">Definition</span></span>

<span data-ttu-id="aaef6-378">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="aaef6-378">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="aaef6-379">A expressão regular `Regex_lithuania_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="aaef6-379">The regular expression  `Regex_lithuania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="aaef6-380">Uma palavra-chave da `Keywords_lithuania_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="aaef6-380">A keyword from  `Keywords_lithuania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_passport_number" />
          <Match idRef="Keywords_lithuania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="aaef6-381">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="aaef6-381">Keywords</span></span>

<span data-ttu-id="aaef6-382">| |</span><span class="sxs-lookup"><span data-stu-id="aaef6-382"></span></span>
|<span data-ttu-id="aaef6-383">**Keywords_lithuania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="aaef6-383">**Keywords_lithuania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="aaef6-384">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="aaef6-384">passport number</span></span>  <br/> <span data-ttu-id="aaef6-385">número de passaporte lithunian</span><span class="sxs-lookup"><span data-stu-id="aaef6-385">lithunian passport number</span></span>  <br/> <span data-ttu-id="aaef6-386">Passport nenhum</span><span class="sxs-lookup"><span data-stu-id="aaef6-386">passport no</span></span>  <br/> <span data-ttu-id="aaef6-387">Paso numeris</span><span class="sxs-lookup"><span data-stu-id="aaef6-387">paso numeris</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="aaef6-388">Luxemburgo</span><span class="sxs-lookup"><span data-stu-id="aaef6-388">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="aaef6-389">Formato</span><span class="sxs-lookup"><span data-stu-id="aaef6-389">Format</span></span>

<span data-ttu-id="aaef6-390">Oito dígitos ou letras sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="aaef6-390">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="aaef6-391">Padrão</span><span class="sxs-lookup"><span data-stu-id="aaef6-391">Pattern</span></span>

<span data-ttu-id="aaef6-392">Oito dígitos ou letras (não maiusculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="aaef6-392">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="aaef6-393">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="aaef6-393">Checksum</span></span>

<span data-ttu-id="aaef6-394">Não</span><span class="sxs-lookup"><span data-stu-id="aaef6-394">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="aaef6-395">Definição</span><span class="sxs-lookup"><span data-stu-id="aaef6-395">Definition</span></span>

<span data-ttu-id="aaef6-396">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="aaef6-396">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="aaef6-397">A expressão regular `Regex_nation_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="aaef6-397">The regular expression  `Regex_nation_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="aaef6-398">Uma palavra-chave da `Keywords_nation_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="aaef6-398">A keyword from  `Keywords_nation_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_nation_eu_passport_number" />
          <Match idRef="Keywords_nation_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="aaef6-399">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="aaef6-399">Keywords</span></span>

<span data-ttu-id="aaef6-400">| |</span><span class="sxs-lookup"><span data-stu-id="aaef6-400"></span></span>
|<span data-ttu-id="aaef6-401">**Keywords_nation_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="aaef6-401">**Keywords_nation_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="aaef6-402">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="aaef6-402">passport number</span></span>  <br/> <span data-ttu-id="aaef6-403">número de passaporte letão</span><span class="sxs-lookup"><span data-stu-id="aaef6-403">latvian passport number</span></span>  <br/> <span data-ttu-id="aaef6-404">Passport nenhum</span><span class="sxs-lookup"><span data-stu-id="aaef6-404">passport no</span></span>  <br/> <span data-ttu-id="aaef6-405">passnummer</span><span class="sxs-lookup"><span data-stu-id="aaef6-405">passnummer</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="aaef6-406">Malta</span><span class="sxs-lookup"><span data-stu-id="aaef6-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="aaef6-407">Formato</span><span class="sxs-lookup"><span data-stu-id="aaef6-407">Format</span></span>

<span data-ttu-id="aaef6-408">Sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="aaef6-408">Seven digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="aaef6-409">Padrão</span><span class="sxs-lookup"><span data-stu-id="aaef6-409">Pattern</span></span>

 <span data-ttu-id="aaef6-410">Sete dígitos</span><span class="sxs-lookup"><span data-stu-id="aaef6-410">Seven digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="aaef6-411">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="aaef6-411">Checksum</span></span>

<span data-ttu-id="aaef6-412">Não</span><span class="sxs-lookup"><span data-stu-id="aaef6-412">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="aaef6-413">Definição</span><span class="sxs-lookup"><span data-stu-id="aaef6-413">Definition</span></span>

<span data-ttu-id="aaef6-414">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="aaef6-414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="aaef6-415">A expressão regular `Regex_malta_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="aaef6-415">The regular expression  `Regex_malta_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="aaef6-416">Uma palavra-chave da `Keywords_malta_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="aaef6-416">A keyword from  `Keywords_malta_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_passport_number" />
          <Match idRef="Keywords_malta_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="aaef6-417">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="aaef6-417">Keywords</span></span>

<span data-ttu-id="aaef6-418">| |</span><span class="sxs-lookup"><span data-stu-id="aaef6-418"></span></span>
|<span data-ttu-id="aaef6-419">**Keywords_malta_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="aaef6-419">**Keywords_malta_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="aaef6-420">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="aaef6-420">passport number</span></span>  <br/> <span data-ttu-id="aaef6-421">número de passaporte Maltês</span><span class="sxs-lookup"><span data-stu-id="aaef6-421">maltese passport number</span></span>  <br/> <span data-ttu-id="aaef6-422">Passport nenhum</span><span class="sxs-lookup"><span data-stu-id="aaef6-422">passport no</span></span>  <br/> <span data-ttu-id="aaef6-423">horizontal-passaport numru</span><span class="sxs-lookup"><span data-stu-id="aaef6-423">numru tal-passaport</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="aaef6-424">Países Baixos</span><span class="sxs-lookup"><span data-stu-id="aaef6-424">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="aaef6-425">Formato</span><span class="sxs-lookup"><span data-stu-id="aaef6-425">Format</span></span>

<span data-ttu-id="aaef6-426">Nove letras ou dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="aaef6-426">Nine letters or digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="aaef6-427">Padrão</span><span class="sxs-lookup"><span data-stu-id="aaef6-427">Pattern</span></span>

<span data-ttu-id="aaef6-428">Nove letras ou dígitos</span><span class="sxs-lookup"><span data-stu-id="aaef6-428">Nine letters or digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="aaef6-429">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="aaef6-429">Checksum</span></span>

<span data-ttu-id="aaef6-430">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="aaef6-430">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="aaef6-431">Definição</span><span class="sxs-lookup"><span data-stu-id="aaef6-431">Definition</span></span>

<span data-ttu-id="aaef6-432">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="aaef6-432">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="aaef6-433">A expressão regular `Regex_netherlands_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="aaef6-433">The regular expression  `Regex_netherlands_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="aaef6-434">Uma palavra-chave da `Keywords_netherlands_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="aaef6-434">A keyword from  `Keywords_netherlands_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_passport_number" />
          <Match idRef="Keywords_netherlands_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="aaef6-435">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="aaef6-435">Keywords</span></span>

<span data-ttu-id="aaef6-436">| |</span><span class="sxs-lookup"><span data-stu-id="aaef6-436"></span></span>
|<span data-ttu-id="aaef6-437">**Keywords_netherlands_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="aaef6-437">**Keywords_netherlands_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="aaef6-438">número de passaporte holandês</span><span class="sxs-lookup"><span data-stu-id="aaef6-438">dutch passport number</span></span>  <br/> <span data-ttu-id="aaef6-439">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="aaef6-439">passport number</span></span>  <br/> <span data-ttu-id="aaef6-440">número de passaporte países baixos</span><span class="sxs-lookup"><span data-stu-id="aaef6-440">netherlands passport number</span></span>  <br/> <span data-ttu-id="aaef6-441">nederlanden paspoort nummer</span><span class="sxs-lookup"><span data-stu-id="aaef6-441">nederlanden paspoort nummer</span></span>  <br/> <span data-ttu-id="aaef6-442">paspoort</span><span class="sxs-lookup"><span data-stu-id="aaef6-442">paspoort</span></span>  <br/> <span data-ttu-id="aaef6-443">nederlanden paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="aaef6-443">nederlanden paspoortnummer</span></span>  <br/> <span data-ttu-id="aaef6-444">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="aaef6-444">paspoortnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="aaef6-445">Polônia</span><span class="sxs-lookup"><span data-stu-id="aaef6-445">Poland</span></span>

<span data-ttu-id="aaef6-446">Para obter detalhes, consulte a seção "Número de passaporte da Polônia" nos [quais os tipos de informações confidenciais procurar](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="aaef6-446">For details, see the section "Poland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="aaef6-447">Portugal</span><span class="sxs-lookup"><span data-stu-id="aaef6-447">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="aaef6-448">Formato</span><span class="sxs-lookup"><span data-stu-id="aaef6-448">Format</span></span>

<span data-ttu-id="aaef6-449">Uma letra seguida de seis dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="aaef6-449">One letter followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="aaef6-450">Padrão</span><span class="sxs-lookup"><span data-stu-id="aaef6-450">Pattern</span></span>

<span data-ttu-id="aaef6-451">Uma letra seguida de seis dígitos:</span><span class="sxs-lookup"><span data-stu-id="aaef6-451">One letter followed by six digits:</span></span>
  
- <span data-ttu-id="aaef6-452">Uma letra (não diferencia maiúscula de minúscula)</span><span class="sxs-lookup"><span data-stu-id="aaef6-452">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="aaef6-453">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="aaef6-453">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="aaef6-454">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="aaef6-454">Checksum</span></span>

<span data-ttu-id="aaef6-455">Não</span><span class="sxs-lookup"><span data-stu-id="aaef6-455">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="aaef6-456">Definição</span><span class="sxs-lookup"><span data-stu-id="aaef6-456">Definition</span></span>

<span data-ttu-id="aaef6-457">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="aaef6-457">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="aaef6-458">A expressão regular `Regex_portugal_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="aaef6-458">The regular expression  `Regex_portugal_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="aaef6-459">Uma palavra-chave da `Keywords_portugal_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="aaef6-459">A keyword from  `Keywords_portugal_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_passport_number" />
          <Match idRef="Keywords_portugal_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="aaef6-460">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="aaef6-460">Keywords</span></span>

<span data-ttu-id="aaef6-461">| |</span><span class="sxs-lookup"><span data-stu-id="aaef6-461"></span></span>
|<span data-ttu-id="aaef6-462">**Keywords_portugal_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="aaef6-462">**Keywords_portugal_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="aaef6-463">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="aaef6-463">passport number</span></span>  <br/> <span data-ttu-id="aaef6-464">número de passaporte português</span><span class="sxs-lookup"><span data-stu-id="aaef6-464">portuguese passport number</span></span>  <br/> <span data-ttu-id="aaef6-465">Passport nenhum</span><span class="sxs-lookup"><span data-stu-id="aaef6-465">passport no</span></span>  <br/> <span data-ttu-id="aaef6-466">número passaporte</span><span class="sxs-lookup"><span data-stu-id="aaef6-466">número do passaporte</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="aaef6-467">Romênia</span><span class="sxs-lookup"><span data-stu-id="aaef6-467">Romania</span></span>

### <a name="format"></a><span data-ttu-id="aaef6-468">Formato</span><span class="sxs-lookup"><span data-stu-id="aaef6-468">Format</span></span>

<span data-ttu-id="aaef6-469">Oito ou nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="aaef6-469">Eight or nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="aaef6-470">Padrão</span><span class="sxs-lookup"><span data-stu-id="aaef6-470">Pattern</span></span>

<span data-ttu-id="aaef6-471">Oito ou nove dígitos</span><span class="sxs-lookup"><span data-stu-id="aaef6-471">Eight or nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="aaef6-472">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="aaef6-472">Checksum</span></span>

<span data-ttu-id="aaef6-473">Não</span><span class="sxs-lookup"><span data-stu-id="aaef6-473">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="aaef6-474">Definição</span><span class="sxs-lookup"><span data-stu-id="aaef6-474">Definition</span></span>

<span data-ttu-id="aaef6-475">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="aaef6-475">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="aaef6-476">A expressão regular `Regex_romania_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="aaef6-476">The regular expression  `Regex_romania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="aaef6-477">Uma palavra-chave da `Keywords_romania_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="aaef6-477">A keyword from  `Keywords_romania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_passport_number" />
          <Match idRef="Keywords_romania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="aaef6-478">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="aaef6-478">Keywords</span></span>

<span data-ttu-id="aaef6-479">| |</span><span class="sxs-lookup"><span data-stu-id="aaef6-479"></span></span>
|<span data-ttu-id="aaef6-480">**Keywords_romania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="aaef6-480">**Keywords_romania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="aaef6-481">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="aaef6-481">passport number</span></span>  <br/> <span data-ttu-id="aaef6-482">número de passaporte romeno</span><span class="sxs-lookup"><span data-stu-id="aaef6-482">romanian passport number</span></span>  <br/> <span data-ttu-id="aaef6-483">Passport nenhum</span><span class="sxs-lookup"><span data-stu-id="aaef6-483">passport no</span></span>  <br/> <span data-ttu-id="aaef6-484">numărul pașaportului</span><span class="sxs-lookup"><span data-stu-id="aaef6-484">numărul pașaportului</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="aaef6-485">Eslováquia</span><span class="sxs-lookup"><span data-stu-id="aaef6-485">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="aaef6-486">Formato</span><span class="sxs-lookup"><span data-stu-id="aaef6-486">Format</span></span>

<span data-ttu-id="aaef6-487">Um dígito ou letra seguido por sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="aaef6-487">One digit or letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="aaef6-488">Padrão</span><span class="sxs-lookup"><span data-stu-id="aaef6-488">Pattern</span></span>

<span data-ttu-id="aaef6-489">Um dígito ou carta (não maiusculas de minúsculas) seguido por sete dígitos</span><span class="sxs-lookup"><span data-stu-id="aaef6-489">One digit or letter (not case sensitive) followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="aaef6-490">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="aaef6-490">Checksum</span></span>

<span data-ttu-id="aaef6-491">Não</span><span class="sxs-lookup"><span data-stu-id="aaef6-491">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="aaef6-492">Definição</span><span class="sxs-lookup"><span data-stu-id="aaef6-492">Definition</span></span>

<span data-ttu-id="aaef6-493">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="aaef6-493">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="aaef6-494">A expressão regular `Regex_slovakia_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="aaef6-494">The regular expression  `Regex_slovakia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="aaef6-495">Uma palavra-chave da `Keywords_slovakia_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="aaef6-495">A keyword from  `Keywords_slovakia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_passport_number" />
          <Match idRef="Keywords_slovakia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="aaef6-496">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="aaef6-496">Keywords</span></span>

<span data-ttu-id="aaef6-497">| |</span><span class="sxs-lookup"><span data-stu-id="aaef6-497"></span></span>
|<span data-ttu-id="aaef6-498">**Keywords_slovakia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="aaef6-498">**Keywords_slovakia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="aaef6-499">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="aaef6-499">passport number</span></span>  <br/> <span data-ttu-id="aaef6-500">número de passaporte eslovaco</span><span class="sxs-lookup"><span data-stu-id="aaef6-500">slovakian passport number</span></span>  <br/> <span data-ttu-id="aaef6-501">Passport nenhum</span><span class="sxs-lookup"><span data-stu-id="aaef6-501">passport no</span></span>  <br/> <span data-ttu-id="aaef6-502">Číslo pasu</span><span class="sxs-lookup"><span data-stu-id="aaef6-502">číslo pasu</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="aaef6-503">Eslovênia</span><span class="sxs-lookup"><span data-stu-id="aaef6-503">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="aaef6-504">Formato</span><span class="sxs-lookup"><span data-stu-id="aaef6-504">Format</span></span>

<span data-ttu-id="aaef6-505">Duas letras seguidas por sete dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="aaef6-505">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="aaef6-506">Padrão</span><span class="sxs-lookup"><span data-stu-id="aaef6-506">Pattern</span></span>

<span data-ttu-id="aaef6-507">Duas letras seguidas por sete dígitos:</span><span class="sxs-lookup"><span data-stu-id="aaef6-507">Two letters followed by seven digits:</span></span>
  
- <span data-ttu-id="aaef6-508">A letra "P"</span><span class="sxs-lookup"><span data-stu-id="aaef6-508">The letter "P"</span></span>
    
- <span data-ttu-id="aaef6-509">Uma letra maiuscula</span><span class="sxs-lookup"><span data-stu-id="aaef6-509">One uppercase letter</span></span>
    
- <span data-ttu-id="aaef6-510">Sete dígitos</span><span class="sxs-lookup"><span data-stu-id="aaef6-510">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="aaef6-511">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="aaef6-511">Checksum</span></span>

<span data-ttu-id="aaef6-512">Não</span><span class="sxs-lookup"><span data-stu-id="aaef6-512">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="aaef6-513">Definição</span><span class="sxs-lookup"><span data-stu-id="aaef6-513">Definition</span></span>

<span data-ttu-id="aaef6-514">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="aaef6-514">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="aaef6-515">A expressão regular `Regex_slovenia_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="aaef6-515">The regular expression  `Regex_slovenia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="aaef6-516">Uma palavra-chave da `Keywords_slovenia_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="aaef6-516">A keyword from  `Keywords_slovenia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_passport_number" />
          <Match idRef="Keywords_slovenia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="aaef6-517">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="aaef6-517">Keywords</span></span>

<span data-ttu-id="aaef6-518">| |</span><span class="sxs-lookup"><span data-stu-id="aaef6-518"></span></span>
|<span data-ttu-id="aaef6-519">**Keywords_slovenia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="aaef6-519">**Keywords_slovenia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="aaef6-520">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="aaef6-520">passport number</span></span>  <br/> <span data-ttu-id="aaef6-521">número de passaporte esloveno</span><span class="sxs-lookup"><span data-stu-id="aaef6-521">slovenian passport number</span></span>  <br/> <span data-ttu-id="aaef6-522">Passport nenhum</span><span class="sxs-lookup"><span data-stu-id="aaef6-522">passport no</span></span>  <br/> <span data-ttu-id="aaef6-523">Lista de potnega številka</span><span class="sxs-lookup"><span data-stu-id="aaef6-523">številka potnega lista</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="aaef6-524">Espanha</span><span class="sxs-lookup"><span data-stu-id="aaef6-524">Spain</span></span>

### <a name="format"></a><span data-ttu-id="aaef6-525">Formato</span><span class="sxs-lookup"><span data-stu-id="aaef6-525">Format</span></span>

<span data-ttu-id="aaef6-526">Uma combinação de oito ou nove caracteres de letras e números sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="aaef6-526">An eight- or nine-character combination of letters and numbers with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="aaef6-527">Padrão</span><span class="sxs-lookup"><span data-stu-id="aaef6-527">Pattern</span></span>

<span data-ttu-id="aaef6-528">Uma combinação de oito ou nove caracteres de letras e números:</span><span class="sxs-lookup"><span data-stu-id="aaef6-528">An eight- or nine-character combination of letters and numbers:</span></span>
  
-  <span data-ttu-id="aaef6-529">Dois dígitos ou letras</span><span class="sxs-lookup"><span data-stu-id="aaef6-529">Two digits or letters</span></span> 
    
- <span data-ttu-id="aaef6-530">Um dígito ou carta (opcional)</span><span class="sxs-lookup"><span data-stu-id="aaef6-530">One digit or letter (optional)</span></span>
    
- <span data-ttu-id="aaef6-531">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="aaef6-531">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="aaef6-532">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="aaef6-532">Checksum</span></span>

<span data-ttu-id="aaef6-533">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="aaef6-533">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="aaef6-534">Definição</span><span class="sxs-lookup"><span data-stu-id="aaef6-534">Definition</span></span>

<span data-ttu-id="aaef6-535">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="aaef6-535">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="aaef6-536">A expressão regular `Regex_spain_eu_passport_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="aaef6-536">The regular expression  `Regex_spain_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="aaef6-537">Uma palavra-chave da `Keywords_spain_eu_passport_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="aaef6-537">A keyword from  `Keywords_spain_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_passport_number" />
          <Match idRef="Keywords_spain_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="aaef6-538">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="aaef6-538">Keywords</span></span>

<span data-ttu-id="aaef6-539">| |</span><span class="sxs-lookup"><span data-stu-id="aaef6-539"></span></span>
|<span data-ttu-id="aaef6-540">**Keywords_spain_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="aaef6-540">**Keywords_spain_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="aaef6-541">passport</span><span class="sxs-lookup"><span data-stu-id="aaef6-541">passport</span></span>  <br/> <span data-ttu-id="aaef6-542">passaporte da Espanha</span><span class="sxs-lookup"><span data-stu-id="aaef6-542">spain passport</span></span>  <br/> <span data-ttu-id="aaef6-543">Catálogo do Passport</span><span class="sxs-lookup"><span data-stu-id="aaef6-543">passport book</span></span>  <br/> <span data-ttu-id="aaef6-544">número de passaporte</span><span class="sxs-lookup"><span data-stu-id="aaef6-544">passport number</span></span>  <br/> <span data-ttu-id="aaef6-545">Passport nenhum</span><span class="sxs-lookup"><span data-stu-id="aaef6-545">passport no</span></span>  <br/> <span data-ttu-id="aaef6-546">libreta pasaporte</span><span class="sxs-lookup"><span data-stu-id="aaef6-546">libreta pasaporte</span></span>  <br/> <span data-ttu-id="aaef6-547">número pasaporte</span><span class="sxs-lookup"><span data-stu-id="aaef6-547">número pasaporte</span></span>  <br/> <span data-ttu-id="aaef6-548">españa pasaporte</span><span class="sxs-lookup"><span data-stu-id="aaef6-548">españa pasaporte</span></span>  <br/> <span data-ttu-id="aaef6-549">pasaporte</span><span class="sxs-lookup"><span data-stu-id="aaef6-549">pasaporte</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="aaef6-550">Suécia</span><span class="sxs-lookup"><span data-stu-id="aaef6-550">Sweden</span></span>

<span data-ttu-id="aaef6-551">Para obter detalhes, consulte a seção "Número de passaporte da Suécia" nos [quais os tipos de informações confidenciais procurar](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="aaef6-551">For details, see the section "Sweden Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="uk"></a><span data-ttu-id="aaef6-552">REINO UNIDO</span><span class="sxs-lookup"><span data-stu-id="aaef6-552">UK</span></span>

<span data-ttu-id="aaef6-p103">Para obter detalhes, consulte a seção "Número de passaporte US / Reino Unido" nos [quais os tipos de informações confidenciais procurar](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="aaef6-p103">For details, see the section "U.S. / U.K. Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="aaef6-555">Confira também</span><span class="sxs-lookup"><span data-stu-id="aaef6-555">See also</span></span>

[<span data-ttu-id="aaef6-556">O que os tipos de informação confidencial procuram</span><span class="sxs-lookup"><span data-stu-id="aaef6-556">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)


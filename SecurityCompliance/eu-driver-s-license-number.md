---
title: Número da carteira de motorista da UE
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: Este tópico mostra o que uma política de prevenção de perda de dados (DLP) procura quando detecta o tipo de informação confidencial do número de licença do driver da UE. Esse tipo de informação confidencial define diferentes padrões, palavras-chave e outras evidências para cada país.
ms.openlocfilehash: f1a95ecbaf6b6d1ac189290dd6d076cfd91ab30f
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34152973"
---
# <a name="eu-drivers-license-number"></a><span data-ttu-id="7ecfd-104">Número da carteira de motorista da UE</span><span class="sxs-lookup"><span data-stu-id="7ecfd-104">EU Driver's License Number</span></span>

<span data-ttu-id="7ecfd-105">Este tópico mostra o que uma política de prevenção de perda de dados (DLP) procura quando detecta o tipo de informação confidencial do número de licença do driver da UE.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Driver's License Number sensitive information type.</span></span> <span data-ttu-id="7ecfd-106">Esse tipo de informação confidencial define diferentes padrões, palavras-chave e outras evidências para cada país.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="7ecfd-107">Áustria </span><span class="sxs-lookup"><span data-stu-id="7ecfd-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="7ecfd-108">Formatar</span><span class="sxs-lookup"><span data-stu-id="7ecfd-108">Format</span></span>

<span data-ttu-id="7ecfd-109">Oito dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="7ecfd-109">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7ecfd-110">Padrão</span><span class="sxs-lookup"><span data-stu-id="7ecfd-110">Pattern</span></span>

<span data-ttu-id="7ecfd-111">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="7ecfd-111">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="7ecfd-112">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="7ecfd-112">Checksum</span></span>

<span data-ttu-id="7ecfd-113">Não</span><span class="sxs-lookup"><span data-stu-id="7ecfd-113">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7ecfd-114">Definição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-114">Definition</span></span>

<span data-ttu-id="7ecfd-115">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="7ecfd-115">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7ecfd-116">A expressão `Regex_austria_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-116">The regular expression  `Regex_austria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7ecfd-117">Uma palavra- `Keywords_austria_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-117">A keyword from  `Keywords_austria_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_driver's_license_number" />
          <Match idRef="Keywords_austria_eu_driver's_license_number" />
        </Pattern>
    </Entity>

```

### <a name="keywords"></a><span data-ttu-id="7ecfd-118">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="7ecfd-118">Keywords</span></span>

<span data-ttu-id="7ecfd-119">| |</span><span class="sxs-lookup"><span data-stu-id="7ecfd-119"></span></span>
|<span data-ttu-id="7ecfd-120">**Keywords_austria_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7ecfd-120">**Keywords_austria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7ecfd-121">distribuição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-121">dl#</span></span>  <br/> <span data-ttu-id="7ecfd-122">driver license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-122">driver license</span></span>  <br/> <span data-ttu-id="7ecfd-123">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-123">driver license number</span></span>  <br/> <span data-ttu-id="7ecfd-124">licença de driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-124">driver licence</span></span>  <br/> <span data-ttu-id="7ecfd-125">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-125">drivers lic.</span></span>  <br/> <span data-ttu-id="7ecfd-126">drivers license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-126">drivers license</span></span>  <br/> <span data-ttu-id="7ecfd-127">driver's licence</span><span class="sxs-lookup"><span data-stu-id="7ecfd-127">driver's licence</span></span>  <br/> <span data-ttu-id="7ecfd-128">driver's license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-128">driver's license</span></span>  <br/> <span data-ttu-id="7ecfd-129">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-129">driver's license number</span></span>  <br/> <span data-ttu-id="7ecfd-130">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-130">driver's licence number</span></span>  <br/>  <span data-ttu-id="7ecfd-131">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="7ecfd-131">driving license number</span></span>  <br/> <span data-ttu-id="7ecfd-132">dlno#</span><span class="sxs-lookup"><span data-stu-id="7ecfd-132">dlno#</span></span>  <br/> <span data-ttu-id="7ecfd-133">fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="7ecfd-133">fuhrerschein</span></span>  <br/> <span data-ttu-id="7ecfd-134">fuhrerschein republik osterreich</span><span class="sxs-lookup"><span data-stu-id="7ecfd-134">fuhrerschein republik osterreich</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="7ecfd-135">Bélgica </span><span class="sxs-lookup"><span data-stu-id="7ecfd-135">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="7ecfd-136">Formatar</span><span class="sxs-lookup"><span data-stu-id="7ecfd-136">Format</span></span>

<span data-ttu-id="7ecfd-137">10 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="7ecfd-137">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7ecfd-138">Padrão</span><span class="sxs-lookup"><span data-stu-id="7ecfd-138">Pattern</span></span>

<span data-ttu-id="7ecfd-139">10 dígitos</span><span class="sxs-lookup"><span data-stu-id="7ecfd-139">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="7ecfd-140">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="7ecfd-140">Checksum</span></span>

<span data-ttu-id="7ecfd-141">Não</span><span class="sxs-lookup"><span data-stu-id="7ecfd-141">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7ecfd-142">Definição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-142">Definition</span></span>

<span data-ttu-id="7ecfd-143">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="7ecfd-143">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7ecfd-144">A expressão `Regex_belgium_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-144">The regular expression  `Regex_belgium_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7ecfd-145">Uma palavra- `Keywords_belgium_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-145">A keyword from  `Keywords_belgium_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_driver's_license_number" />
          <Match idRef="Keywords_belgium_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="7ecfd-146">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="7ecfd-146">Keywords</span></span>

<span data-ttu-id="7ecfd-147">| |</span><span class="sxs-lookup"><span data-stu-id="7ecfd-147"></span></span>
|<span data-ttu-id="7ecfd-148">**Keywords__belgium_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7ecfd-148">**Keywords__belgium_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7ecfd-149">distribuição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-149">dl#</span></span>  <br/> <span data-ttu-id="7ecfd-150">driver license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-150">driver license</span></span>  <br/> <span data-ttu-id="7ecfd-151">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-151">driver license number</span></span>  <br/> <span data-ttu-id="7ecfd-152">licença de driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-152">driver licence</span></span>  <br/> <span data-ttu-id="7ecfd-153">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-153">drivers lic.</span></span>  <br/> <span data-ttu-id="7ecfd-154">drivers license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-154">drivers license</span></span>  <br/> <span data-ttu-id="7ecfd-155">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7ecfd-155">drivers licence</span></span>  <br/> <span data-ttu-id="7ecfd-156">driver's license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-156">driver's license</span></span>  <br/> <span data-ttu-id="7ecfd-157">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-157">driver's license number</span></span>  <br/> <span data-ttu-id="7ecfd-158">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-158">driver's licence number</span></span>  <br/> <span data-ttu-id="7ecfd-159">dlno#</span><span class="sxs-lookup"><span data-stu-id="7ecfd-159">dlno#</span></span>  <br/> <span data-ttu-id="7ecfd-160">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="7ecfd-160">rijbewijs</span></span>  <br/> <span data-ttu-id="7ecfd-161">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="7ecfd-161">rijbewijsnummer</span></span>  <br/> <span data-ttu-id="7ecfd-162">führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7ecfd-162">führerscheinnummer</span></span>  <br/> <span data-ttu-id="7ecfd-163">fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7ecfd-163">fuhrerscheinnummer</span></span>  <br/> <span data-ttu-id="7ecfd-164">fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7ecfd-164">fuehrerscheinnummer</span></span>  <br/> <span data-ttu-id="7ecfd-165">führerschein- nr</span><span class="sxs-lookup"><span data-stu-id="7ecfd-165">führerschein- nr</span></span>  <br/> <span data-ttu-id="7ecfd-166">fuehrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="7ecfd-166">fuehrerschein- Nr</span></span>  <br/> <span data-ttu-id="7ecfd-167">fuehrerschein- nr</span><span class="sxs-lookup"><span data-stu-id="7ecfd-167">fuehrerschein- nr</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="7ecfd-168">Bulgária</span><span class="sxs-lookup"><span data-stu-id="7ecfd-168">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="7ecfd-169">Formatar</span><span class="sxs-lookup"><span data-stu-id="7ecfd-169">Format</span></span>

<span data-ttu-id="7ecfd-170">Nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="7ecfd-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7ecfd-171">Padrão</span><span class="sxs-lookup"><span data-stu-id="7ecfd-171">Pattern</span></span>

<span data-ttu-id="7ecfd-172">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="7ecfd-172">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="7ecfd-173">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="7ecfd-173">Checksum</span></span>

<span data-ttu-id="7ecfd-174">Não</span><span class="sxs-lookup"><span data-stu-id="7ecfd-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7ecfd-175">Definição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-175">Definition</span></span>

<span data-ttu-id="7ecfd-176">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="7ecfd-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7ecfd-177">A expressão `Regex_bulgaria_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-177">The regular expression  `Regex_bulgaria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7ecfd-178">Uma palavra- `Keywords_bulgaria_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-178">A keyword from  `Keywords_bulgaria_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
             <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_driver's_license_number" />
          <Match idRef="Keywords_bulgaria_eu_driver's_license_number" />
        </Pattern> 
</Entity>    

```

### <a name="keywords"></a><span data-ttu-id="7ecfd-179">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="7ecfd-179">Keywords</span></span>

<span data-ttu-id="7ecfd-180">| |</span><span class="sxs-lookup"><span data-stu-id="7ecfd-180"></span></span>
|<span data-ttu-id="7ecfd-181">**Keywords_bulgaria_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7ecfd-181">**Keywords_bulgaria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7ecfd-182">distribuição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-182">dl#</span></span>  <br/> <span data-ttu-id="7ecfd-183">driver license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-183">driver license</span></span>  <br/> <span data-ttu-id="7ecfd-184">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-184">driver license number</span></span>  <br/> <span data-ttu-id="7ecfd-185">licença de driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-185">driver licence</span></span>  <br/> <span data-ttu-id="7ecfd-186">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-186">drivers lic.</span></span>  <br/> <span data-ttu-id="7ecfd-187">drivers license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-187">drivers license</span></span>  <br/> <span data-ttu-id="7ecfd-188">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7ecfd-188">drivers licence</span></span>  <br/> <span data-ttu-id="7ecfd-189">driver's license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-189">driver's license</span></span>  <br/> <span data-ttu-id="7ecfd-190">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-190">driver's license number</span></span>  <br/> <span data-ttu-id="7ecfd-191">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-191">driver's licence number</span></span>  <br/> <span data-ttu-id="7ecfd-192">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="7ecfd-192">driving license number</span></span>  <br/> <span data-ttu-id="7ecfd-193">dlno#</span><span class="sxs-lookup"><span data-stu-id="7ecfd-193">dlno#</span></span>  <br/> <span data-ttu-id="7ecfd-194">свидетелство за управление на мпс</span><span class="sxs-lookup"><span data-stu-id="7ecfd-194">свидетелство за управление на мпс</span></span>  <br/> <span data-ttu-id="7ecfd-195">свидетелство за управление на моторно превозно средство</span><span class="sxs-lookup"><span data-stu-id="7ecfd-195">свидетелство за управление на моторно превозно средство</span></span>  <br/> <span data-ttu-id="7ecfd-196">сумпс</span><span class="sxs-lookup"><span data-stu-id="7ecfd-196">сумпс</span></span>  <br/> <span data-ttu-id="7ecfd-197">шофьорска книжка</span><span class="sxs-lookup"><span data-stu-id="7ecfd-197">шофьорска книжка</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="7ecfd-198">Croácia</span><span class="sxs-lookup"><span data-stu-id="7ecfd-198">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="7ecfd-199">Formatar</span><span class="sxs-lookup"><span data-stu-id="7ecfd-199">Format</span></span>

<span data-ttu-id="7ecfd-200">Oito dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="7ecfd-200">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7ecfd-201">Padrão</span><span class="sxs-lookup"><span data-stu-id="7ecfd-201">Pattern</span></span>

<span data-ttu-id="7ecfd-202">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="7ecfd-202">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="7ecfd-203">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="7ecfd-203">Checksum</span></span>

<span data-ttu-id="7ecfd-204">Não</span><span class="sxs-lookup"><span data-stu-id="7ecfd-204">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7ecfd-205">Definição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-205">Definition</span></span>

<span data-ttu-id="7ecfd-206">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="7ecfd-206">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7ecfd-207">A expressão `Regex_croatia_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-207">The regular expression  `Regex_croatia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7ecfd-208">Uma palavra- `Keywords_croatia_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-208">A keyword from  `Keywords_croatia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_driver's_license_number" />
          <Match idRef="Keywords_croatia_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="7ecfd-209">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="7ecfd-209">Keywords</span></span>

<span data-ttu-id="7ecfd-210">| |</span><span class="sxs-lookup"><span data-stu-id="7ecfd-210"></span></span>
|<span data-ttu-id="7ecfd-211">**Keywords_croatia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7ecfd-211">**Keywords_croatia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7ecfd-212">distribuição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-212">dl#</span></span>  <br/> <span data-ttu-id="7ecfd-213">driver license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-213">driver license</span></span>  <br/> <span data-ttu-id="7ecfd-214">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-214">driver license number</span></span>  <br/> <span data-ttu-id="7ecfd-215">licença de driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-215">driver licence</span></span>  <br/> <span data-ttu-id="7ecfd-216">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-216">drivers lic.</span></span>  <br/> <span data-ttu-id="7ecfd-217">drivers license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-217">drivers license</span></span>  <br/> <span data-ttu-id="7ecfd-218">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7ecfd-218">drivers licence</span></span>  <br/> <span data-ttu-id="7ecfd-219">driver's license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-219">driver's license</span></span>  <br/> <span data-ttu-id="7ecfd-220">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-220">driver's license number</span></span>  <br/> <span data-ttu-id="7ecfd-221">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-221">driver's licence number</span></span>  <br/> <span data-ttu-id="7ecfd-222">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="7ecfd-222">driving license number</span></span>  <br/> <span data-ttu-id="7ecfd-223">dlno#</span><span class="sxs-lookup"><span data-stu-id="7ecfd-223">dlno#</span></span>  <br/> <span data-ttu-id="7ecfd-224">vozačka dozvola</span><span class="sxs-lookup"><span data-stu-id="7ecfd-224">vozačka dozvola</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="7ecfd-225">Chipre</span><span class="sxs-lookup"><span data-stu-id="7ecfd-225">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="7ecfd-226">Formatar</span><span class="sxs-lookup"><span data-stu-id="7ecfd-226">Format</span></span>

<span data-ttu-id="7ecfd-227">12 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="7ecfd-227">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7ecfd-228">Padrão</span><span class="sxs-lookup"><span data-stu-id="7ecfd-228">Pattern</span></span>

<span data-ttu-id="7ecfd-229">12 dígitos</span><span class="sxs-lookup"><span data-stu-id="7ecfd-229">12 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="7ecfd-230">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="7ecfd-230">Checksum</span></span>

<span data-ttu-id="7ecfd-231">Não</span><span class="sxs-lookup"><span data-stu-id="7ecfd-231">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7ecfd-232">Definição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-232">Definition</span></span>

<span data-ttu-id="7ecfd-233">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="7ecfd-233">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7ecfd-234">A expressão `Regex_cyprus_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-234">The regular expression  `Regex_cyprus_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7ecfd-235">Uma palavra- `Keywords_cyprus_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-235">A keyword from  `Keywords_cyprus_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_driver's_license_number" />
          <Match idRef="Keywords_cyprus_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7ecfd-236">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="7ecfd-236">Keywords</span></span>

<span data-ttu-id="7ecfd-237">| |</span><span class="sxs-lookup"><span data-stu-id="7ecfd-237"></span></span>
|<span data-ttu-id="7ecfd-238">**Keywords_cyprus_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7ecfd-238">**Keywords_cyprus_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7ecfd-239">distribuição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-239">dl#</span></span>  <br/> <span data-ttu-id="7ecfd-240">driver license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-240">driver license</span></span>  <br/> <span data-ttu-id="7ecfd-241">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-241">driver license number</span></span>  <br/> <span data-ttu-id="7ecfd-242">licença de driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-242">driver licence</span></span>  <br/> <span data-ttu-id="7ecfd-243">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-243">drivers lic.</span></span>  <br/> <span data-ttu-id="7ecfd-244">drivers license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-244">drivers license</span></span>  <br/> <span data-ttu-id="7ecfd-245">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7ecfd-245">drivers licence</span></span>  <br/> <span data-ttu-id="7ecfd-246">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-246">driver's license number</span></span>  <br/> <span data-ttu-id="7ecfd-247">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-247">driver's licence number</span></span>  <br/> <span data-ttu-id="7ecfd-248">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="7ecfd-248">driving license number</span></span>  <br/> <span data-ttu-id="7ecfd-249">dlno#</span><span class="sxs-lookup"><span data-stu-id="7ecfd-249">dlno#</span></span>  <br/> <span data-ttu-id="7ecfd-250">άδεια οδήγησης</span><span class="sxs-lookup"><span data-stu-id="7ecfd-250">άδεια οδήγησης</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="7ecfd-251">República Tcheca</span><span class="sxs-lookup"><span data-stu-id="7ecfd-251">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="7ecfd-252">Formatar</span><span class="sxs-lookup"><span data-stu-id="7ecfd-252">Format</span></span>

<span data-ttu-id="7ecfd-253">Duas letras seguidas por seis dígitos</span><span class="sxs-lookup"><span data-stu-id="7ecfd-253">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7ecfd-254">Padrão</span><span class="sxs-lookup"><span data-stu-id="7ecfd-254">Pattern</span></span>

<span data-ttu-id="7ecfd-255">Oito letras e dígitos:</span><span class="sxs-lookup"><span data-stu-id="7ecfd-255">Eight letters and digits:</span></span>
  
- <span data-ttu-id="7ecfd-256">Duas letras (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="7ecfd-256">Two letters (not case-sensitive)</span></span>
    
- <span data-ttu-id="7ecfd-257">Um espaço (opcional)</span><span class="sxs-lookup"><span data-stu-id="7ecfd-257">A space (optional)</span></span>
    
- <span data-ttu-id="7ecfd-258">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="7ecfd-258">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7ecfd-259">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="7ecfd-259">Checksum</span></span>

<span data-ttu-id="7ecfd-260">Não</span><span class="sxs-lookup"><span data-stu-id="7ecfd-260">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7ecfd-261">Definição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-261">Definition</span></span>

<span data-ttu-id="7ecfd-262">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="7ecfd-262">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7ecfd-263">A expressão `Regex_czech_republic_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-263">The regular expression  `Regex_czech_republic_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7ecfd-264">Uma palavra- `Keywords_czech_republic_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-264">A keyword from  `Keywords_czech_republic_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_driver's_license_number" />
          <Match idRef="Keywords_czech_republic_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="7ecfd-265">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="7ecfd-265">Keywords</span></span>

<span data-ttu-id="7ecfd-266">| |</span><span class="sxs-lookup"><span data-stu-id="7ecfd-266"></span></span>
|<span data-ttu-id="7ecfd-267">**Keywords_czech_republic_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7ecfd-267">**Keywords_czech_republic_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7ecfd-268">distribuição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-268">dl#</span></span>  <br/> <span data-ttu-id="7ecfd-269">driver license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-269">driver license</span></span>  <br/> <span data-ttu-id="7ecfd-270">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-270">driver license number</span></span>  <br/> <span data-ttu-id="7ecfd-271">licença de driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-271">driver licence</span></span>  <br/> <span data-ttu-id="7ecfd-272">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-272">drivers lic.</span></span>  <br/> <span data-ttu-id="7ecfd-273">drivers license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-273">drivers license</span></span>  <br/> <span data-ttu-id="7ecfd-274">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7ecfd-274">drivers licence</span></span>  <br/> <span data-ttu-id="7ecfd-275">driver's license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-275">driver's license</span></span>  <br/> <span data-ttu-id="7ecfd-276">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-276">driver's license number</span></span>  <br/> <span data-ttu-id="7ecfd-277">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-277">driver's license number</span></span>  <br/> <span data-ttu-id="7ecfd-278">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-278">driver's licence number</span></span>  <br/> <span data-ttu-id="7ecfd-279">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="7ecfd-279">driving license number</span></span>  <br/> <span data-ttu-id="7ecfd-280">dlno#</span><span class="sxs-lookup"><span data-stu-id="7ecfd-280">dlno#</span></span>  <br/> <span data-ttu-id="7ecfd-281">řidičský prúkaz</span><span class="sxs-lookup"><span data-stu-id="7ecfd-281">řidičský prúkaz</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="7ecfd-282">Dinamarca</span><span class="sxs-lookup"><span data-stu-id="7ecfd-282">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="7ecfd-283">Formatar</span><span class="sxs-lookup"><span data-stu-id="7ecfd-283">Format</span></span>

<span data-ttu-id="7ecfd-284">Oito dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="7ecfd-284">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7ecfd-285">Padrão</span><span class="sxs-lookup"><span data-stu-id="7ecfd-285">Pattern</span></span>

<span data-ttu-id="7ecfd-286">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="7ecfd-286">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="7ecfd-287">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="7ecfd-287">Checksum</span></span>

<span data-ttu-id="7ecfd-288">Sim</span><span class="sxs-lookup"><span data-stu-id="7ecfd-288">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="7ecfd-289">Definição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-289">Definition</span></span>

<span data-ttu-id="7ecfd-290">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="7ecfd-290">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7ecfd-291">A expressão `Regex_denmark_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-291">The regular expression  `Regex_denmark_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7ecfd-292">Uma palavra- `Keywords_denmark_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-292">A keyword from  `Keywords_denmark_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_driver's_license_number" />
          <Match idRef="Keywords_denmark_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="7ecfd-293">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="7ecfd-293">Keywords</span></span>

<span data-ttu-id="7ecfd-294">| |</span><span class="sxs-lookup"><span data-stu-id="7ecfd-294"></span></span>
|<span data-ttu-id="7ecfd-295">**Keywords_denmark_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7ecfd-295">**Keywords_denmark_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7ecfd-296">distribuição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-296">dl#</span></span>  <br/> <span data-ttu-id="7ecfd-297">driver license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-297">driver license</span></span>  <br/> <span data-ttu-id="7ecfd-298">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-298">driver license number</span></span>  <br/> <span data-ttu-id="7ecfd-299">licença de driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-299">driver licence</span></span>  <br/> <span data-ttu-id="7ecfd-300">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-300">drivers lic.</span></span>  <br/> <span data-ttu-id="7ecfd-301">drivers license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-301">drivers license</span></span>  <br/> <span data-ttu-id="7ecfd-302">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7ecfd-302">drivers licence</span></span>  <br/> <span data-ttu-id="7ecfd-303">driver's license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-303">driver's license</span></span>  <br/> <span data-ttu-id="7ecfd-304">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-304">driver's license number</span></span>  <br/> <span data-ttu-id="7ecfd-305">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-305">driver's licence number</span></span>  <br/> <span data-ttu-id="7ecfd-306">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="7ecfd-306">driving license number</span></span>  <br/> <span data-ttu-id="7ecfd-307">dlno#</span><span class="sxs-lookup"><span data-stu-id="7ecfd-307">dlno#</span></span>  <br/> <span data-ttu-id="7ecfd-308">kørekort</span><span class="sxs-lookup"><span data-stu-id="7ecfd-308">kørekort</span></span>  <br/> <span data-ttu-id="7ecfd-309">kørekortnummer</span><span class="sxs-lookup"><span data-stu-id="7ecfd-309">kørekortnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="7ecfd-310">Estônia</span><span class="sxs-lookup"><span data-stu-id="7ecfd-310">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="7ecfd-311">Formatar</span><span class="sxs-lookup"><span data-stu-id="7ecfd-311">Format</span></span>

<span data-ttu-id="7ecfd-312">Duas letras seguidas por seis dígitos</span><span class="sxs-lookup"><span data-stu-id="7ecfd-312">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7ecfd-313">Padrão</span><span class="sxs-lookup"><span data-stu-id="7ecfd-313">Pattern</span></span>

<span data-ttu-id="7ecfd-314">Duas letras e seis dígitos:</span><span class="sxs-lookup"><span data-stu-id="7ecfd-314">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="7ecfd-315">As letras "ET" (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="7ecfd-315">The letters "ET" (not case-sensitive)</span></span> 
    
- <span data-ttu-id="7ecfd-316">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="7ecfd-316">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7ecfd-317">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="7ecfd-317">Checksum</span></span>

<span data-ttu-id="7ecfd-318">Não</span><span class="sxs-lookup"><span data-stu-id="7ecfd-318">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7ecfd-319">Definição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-319">Definition</span></span>

<span data-ttu-id="7ecfd-320">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="7ecfd-320">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7ecfd-321">A expressão `Regex_estonia_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-321">The regular expression  `Regex_estonia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7ecfd-322">Uma palavra- `Keywords_estonia_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-322">A keyword from  `Keywords_estonia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_driver's_license_number" />
          <Match idRef="Keywords_estonia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7ecfd-323">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="7ecfd-323">Keywords</span></span>

<span data-ttu-id="7ecfd-324">| |</span><span class="sxs-lookup"><span data-stu-id="7ecfd-324"></span></span>
|<span data-ttu-id="7ecfd-325">**Keywords_estonia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7ecfd-325">**Keywords_estonia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7ecfd-326">distribuição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-326">dl#</span></span>  <br/> <span data-ttu-id="7ecfd-327">driver license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-327">driver license</span></span>  <br/> <span data-ttu-id="7ecfd-328">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-328">driver license number</span></span>  <br/> <span data-ttu-id="7ecfd-329">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-329">driver license number</span></span>  <br/> <span data-ttu-id="7ecfd-330">licença de driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-330">driver licence</span></span>  <br/> <span data-ttu-id="7ecfd-331">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-331">drivers lic.</span></span>  <br/> <span data-ttu-id="7ecfd-332">drivers license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-332">drivers license</span></span>  <br/> <span data-ttu-id="7ecfd-333">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7ecfd-333">drivers licence</span></span>  <br/> <span data-ttu-id="7ecfd-334">driver's license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-334">driver's license</span></span>  <br/> <span data-ttu-id="7ecfd-335">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-335">driver's license number</span></span>  <br/> <span data-ttu-id="7ecfd-336">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="7ecfd-336">driving license number</span></span>  <br/> <span data-ttu-id="7ecfd-337">dlno#</span><span class="sxs-lookup"><span data-stu-id="7ecfd-337">dlno#</span></span>  <br/> <span data-ttu-id="7ecfd-338">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="7ecfd-338">permis de conduire</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="7ecfd-339">Finlândia</span><span class="sxs-lookup"><span data-stu-id="7ecfd-339">Finland</span></span>

### <a name="format"></a><span data-ttu-id="7ecfd-340">Formatar</span><span class="sxs-lookup"><span data-stu-id="7ecfd-340">Format</span></span>

<span data-ttu-id="7ecfd-341">10 dígitos que contêm um hífen</span><span class="sxs-lookup"><span data-stu-id="7ecfd-341">10 digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7ecfd-342">Padrão</span><span class="sxs-lookup"><span data-stu-id="7ecfd-342">Pattern</span></span>

<span data-ttu-id="7ecfd-343">10 dígitos contendo um hífen:</span><span class="sxs-lookup"><span data-stu-id="7ecfd-343">10 digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="7ecfd-344">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="7ecfd-344">Six digits</span></span> 
    
- <span data-ttu-id="7ecfd-345">Um hífen</span><span class="sxs-lookup"><span data-stu-id="7ecfd-345">A hyphen</span></span>
    
-  <span data-ttu-id="7ecfd-346">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="7ecfd-346">Four digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="7ecfd-347">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="7ecfd-347">Checksum</span></span>

<span data-ttu-id="7ecfd-348">Não</span><span class="sxs-lookup"><span data-stu-id="7ecfd-348">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7ecfd-349">Definição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-349">Definition</span></span>

<span data-ttu-id="7ecfd-350">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="7ecfd-350">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7ecfd-351">A expressão `Regex_finland_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-351">The regular expression  `Regex_finland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7ecfd-352">Uma palavra- `Keywords_finland_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-352">A keyword from  `Keywords_finland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_driver's_license_number" />
          <Match idRef="Keywords_finland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7ecfd-353">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="7ecfd-353">Keywords</span></span>

<span data-ttu-id="7ecfd-354">| |</span><span class="sxs-lookup"><span data-stu-id="7ecfd-354"></span></span>
|<span data-ttu-id="7ecfd-355">**Keywords_finland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7ecfd-355">**Keywords_finland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7ecfd-356">distribuição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-356">dl#</span></span>  <br/> <span data-ttu-id="7ecfd-357">driver license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-357">driver license</span></span>  <br/> <span data-ttu-id="7ecfd-358">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-358">driver license number</span></span>  <br/> <span data-ttu-id="7ecfd-359">licença de driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-359">driver licence</span></span>  <br/> <span data-ttu-id="7ecfd-360">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-360">drivers lic.</span></span>  <br/> <span data-ttu-id="7ecfd-361">drivers license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-361">drivers license</span></span>  <br/> <span data-ttu-id="7ecfd-362">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7ecfd-362">drivers licence</span></span>  <br/> <span data-ttu-id="7ecfd-363">driver's license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-363">driver's license</span></span>  <br/> <span data-ttu-id="7ecfd-364">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-364">driver's license number</span></span>  <br/> <span data-ttu-id="7ecfd-365">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-365">driver's licence number</span></span>  <br/> <span data-ttu-id="7ecfd-366">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="7ecfd-366">driving license number</span></span>  <br/> <span data-ttu-id="7ecfd-367">dlno#</span><span class="sxs-lookup"><span data-stu-id="7ecfd-367">dlno#</span></span>  <br/> <span data-ttu-id="7ecfd-368">ajokortti</span><span class="sxs-lookup"><span data-stu-id="7ecfd-368">ajokortti</span></span>  <br/> |
   
## <a name="france"></a><span data-ttu-id="7ecfd-369">França</span><span class="sxs-lookup"><span data-stu-id="7ecfd-369">France</span></span>

<span data-ttu-id="7ecfd-370">Para obter detalhes, consulte a seção "número da carteira de motorista do driver da França" em [o que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="7ecfd-370">For details, see the section "France Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="7ecfd-371">Alemanha</span><span class="sxs-lookup"><span data-stu-id="7ecfd-371">Germany</span></span>

<span data-ttu-id="7ecfd-372">Para obter detalhes, consulte a seção "número da carteira de motorista do driver alemão" em [o que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="7ecfd-372">For details, see the section "German Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="7ecfd-373">Grécia</span><span class="sxs-lookup"><span data-stu-id="7ecfd-373">Greece</span></span>

### <a name="format"></a><span data-ttu-id="7ecfd-374">Formatar</span><span class="sxs-lookup"><span data-stu-id="7ecfd-374">Format</span></span>

<span data-ttu-id="7ecfd-375">Nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="7ecfd-375">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7ecfd-376">Padrão</span><span class="sxs-lookup"><span data-stu-id="7ecfd-376">Pattern</span></span>

 <span data-ttu-id="7ecfd-377">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="7ecfd-377">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="7ecfd-378">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="7ecfd-378">Checksum</span></span>

<span data-ttu-id="7ecfd-379">Não</span><span class="sxs-lookup"><span data-stu-id="7ecfd-379">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7ecfd-380">Definição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-380">Definition</span></span>

<span data-ttu-id="7ecfd-381">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="7ecfd-381">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7ecfd-382">A expressão `Regex_greece_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-382">The regular expression  `Regex_greece_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7ecfd-383">Uma palavra- `Keywords_greece_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-383">A keyword from  `Keywords_greece_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_driver's_license_number" />
          <Match idRef="Keywords_greece_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7ecfd-384">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="7ecfd-384">Keywords</span></span>

<span data-ttu-id="7ecfd-385">| |</span><span class="sxs-lookup"><span data-stu-id="7ecfd-385"></span></span>
|<span data-ttu-id="7ecfd-386">**Keywords_greece_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7ecfd-386">**Keywords_greece_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7ecfd-387">DlL</span><span class="sxs-lookup"><span data-stu-id="7ecfd-387">dlL#</span></span>  <br/> <span data-ttu-id="7ecfd-388">driver license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-388">driver license</span></span>  <br/> <span data-ttu-id="7ecfd-389">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-389">driver license number</span></span>  <br/> <span data-ttu-id="7ecfd-390">licença de driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-390">driver licence</span></span>  <br/> <span data-ttu-id="7ecfd-391">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-391">drivers lic.</span></span>  <br/> <span data-ttu-id="7ecfd-392">drivers license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-392">drivers license</span></span>  <br/> <span data-ttu-id="7ecfd-393">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7ecfd-393">drivers licence</span></span>  <br/> <span data-ttu-id="7ecfd-394">driver's license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-394">driver's license</span></span>  <br/> <span data-ttu-id="7ecfd-395">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-395">driver's license number</span></span>  <br/> <span data-ttu-id="7ecfd-396">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-396">driver's licence number</span></span>  <br/> <span data-ttu-id="7ecfd-397">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="7ecfd-397">driving license number</span></span>  <br/> <span data-ttu-id="7ecfd-398">dlno#</span><span class="sxs-lookup"><span data-stu-id="7ecfd-398">dlno#</span></span>  <br/> <span data-ttu-id="7ecfd-399">δεια οδήγησης</span><span class="sxs-lookup"><span data-stu-id="7ecfd-399">δεια οδήγησης</span></span>  <br/> <span data-ttu-id="7ecfd-400">Adeia odigisis</span><span class="sxs-lookup"><span data-stu-id="7ecfd-400">Adeia odigisis</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="7ecfd-401">Hungria</span><span class="sxs-lookup"><span data-stu-id="7ecfd-401">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="7ecfd-402">Formatar</span><span class="sxs-lookup"><span data-stu-id="7ecfd-402">Format</span></span>

<span data-ttu-id="7ecfd-403">Duas letras seguidas por seis dígitos</span><span class="sxs-lookup"><span data-stu-id="7ecfd-403">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7ecfd-404">Padrão</span><span class="sxs-lookup"><span data-stu-id="7ecfd-404">Pattern</span></span>

<span data-ttu-id="7ecfd-405">Duas letras e seis dígitos:</span><span class="sxs-lookup"><span data-stu-id="7ecfd-405">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="7ecfd-406">Duas letras (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="7ecfd-406">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="7ecfd-407">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="7ecfd-407">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7ecfd-408">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="7ecfd-408">Checksum</span></span>

<span data-ttu-id="7ecfd-409">Não</span><span class="sxs-lookup"><span data-stu-id="7ecfd-409">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7ecfd-410">Definição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-410">Definition</span></span>

<span data-ttu-id="7ecfd-411">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="7ecfd-411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7ecfd-412">A expressão `Regex_hungary_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-412">The regular expression  `Regex_hungary_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7ecfd-413">Uma palavra- `Keywords_hungary_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-413">A keyword from  `Keywords_hungary_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_driver's_license_number" />
          <Match idRef="Keywords_hungary_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7ecfd-414">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="7ecfd-414">Keywords</span></span>

<span data-ttu-id="7ecfd-415">| |</span><span class="sxs-lookup"><span data-stu-id="7ecfd-415"></span></span>
|<span data-ttu-id="7ecfd-416">**Keywords_hungary_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7ecfd-416">**Keywords_hungary_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7ecfd-417">distribuição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-417">dl#</span></span>  <br/> <span data-ttu-id="7ecfd-418">driver license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-418">driver license</span></span>  <br/> <span data-ttu-id="7ecfd-419">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-419">driver license number</span></span>  <br/> <span data-ttu-id="7ecfd-420">licença de driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-420">driver licence</span></span>  <br/> <span data-ttu-id="7ecfd-421">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-421">drivers lic.</span></span>  <br/> <span data-ttu-id="7ecfd-422">drivers license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-422">drivers license</span></span>  <br/> <span data-ttu-id="7ecfd-423">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7ecfd-423">drivers licence</span></span>  <br/> <span data-ttu-id="7ecfd-424">driver's license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-424">driver's license</span></span>  <br/> <span data-ttu-id="7ecfd-425">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-425">driver's license number</span></span>  <br/> <span data-ttu-id="7ecfd-426">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-426">driver's licence number</span></span>  <br/> <span data-ttu-id="7ecfd-427">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="7ecfd-427">driving license number</span></span>  <br/> <span data-ttu-id="7ecfd-428">dlno#</span><span class="sxs-lookup"><span data-stu-id="7ecfd-428">dlno#</span></span>  <br/> <span data-ttu-id="7ecfd-429">vezetoi engedely</span><span class="sxs-lookup"><span data-stu-id="7ecfd-429">vezetoi engedely</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="7ecfd-430">Irlanda</span><span class="sxs-lookup"><span data-stu-id="7ecfd-430">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="7ecfd-431">Formatar</span><span class="sxs-lookup"><span data-stu-id="7ecfd-431">Format</span></span>

<span data-ttu-id="7ecfd-432">Seis dígitos seguidos de quatro letras</span><span class="sxs-lookup"><span data-stu-id="7ecfd-432">Six digits followed by four letters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7ecfd-433">Padrão</span><span class="sxs-lookup"><span data-stu-id="7ecfd-433">Pattern</span></span>

<span data-ttu-id="7ecfd-434">Seis dígitos e quatro letras:</span><span class="sxs-lookup"><span data-stu-id="7ecfd-434">Six digits and four letters:</span></span>
  
- <span data-ttu-id="7ecfd-435">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="7ecfd-435">Six digits</span></span>
    
- <span data-ttu-id="7ecfd-436">Quatro letras (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="7ecfd-436">Four letters (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7ecfd-437">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="7ecfd-437">Checksum</span></span>

<span data-ttu-id="7ecfd-438">Não</span><span class="sxs-lookup"><span data-stu-id="7ecfd-438">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7ecfd-439">Definição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-439">Definition</span></span>

<span data-ttu-id="7ecfd-440">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="7ecfd-440">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7ecfd-441">A expressão `Regex_ireland_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-441">The regular expression  `Regex_ireland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7ecfd-442">Uma palavra- `Keywords_ireland_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-442">A keyword from  `Keywords_ireland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_driver's_license_number" />
          <Match idRef="Keywords_ireland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7ecfd-443">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="7ecfd-443">Keywords</span></span>

<span data-ttu-id="7ecfd-444">| |</span><span class="sxs-lookup"><span data-stu-id="7ecfd-444"></span></span>
|<span data-ttu-id="7ecfd-445">**Keywords_ireland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7ecfd-445">**Keywords_ireland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7ecfd-446">distribuição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-446">dl#</span></span>  <br/> <span data-ttu-id="7ecfd-447">driver license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-447">driver license</span></span>  <br/> <span data-ttu-id="7ecfd-448">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-448">driver license number</span></span>  <br/> <span data-ttu-id="7ecfd-449">licença de driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-449">driver licence</span></span>  <br/> <span data-ttu-id="7ecfd-450">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-450">drivers lic.</span></span>  <br/> <span data-ttu-id="7ecfd-451">drivers license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-451">drivers license</span></span>  <br/> <span data-ttu-id="7ecfd-452">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7ecfd-452">drivers licence</span></span>  <br/> <span data-ttu-id="7ecfd-453">driver's license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-453">driver's license</span></span>  <br/> <span data-ttu-id="7ecfd-454">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-454">driver's license number</span></span>  <br/> <span data-ttu-id="7ecfd-455">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-455">driver's licence number</span></span>  <br/> <span data-ttu-id="7ecfd-456">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="7ecfd-456">driving license number</span></span>  <br/> <span data-ttu-id="7ecfd-457">dlno#</span><span class="sxs-lookup"><span data-stu-id="7ecfd-457">dlno#</span></span>  <br/> <span data-ttu-id="7ecfd-458">ceadúnas tiomána</span><span class="sxs-lookup"><span data-stu-id="7ecfd-458">ceadúnas tiomána</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="7ecfd-459">Itália</span><span class="sxs-lookup"><span data-stu-id="7ecfd-459">Italy</span></span>

<span data-ttu-id="7ecfd-460">Para obter detalhes, consulte a seção "número da carteira de motorista do driver da Itália" em [o que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="7ecfd-460">For details, see the section "Italy Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="latvia"></a><span data-ttu-id="7ecfd-461">Letônia</span><span class="sxs-lookup"><span data-stu-id="7ecfd-461">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="7ecfd-462">Formatar</span><span class="sxs-lookup"><span data-stu-id="7ecfd-462">Format</span></span>

<span data-ttu-id="7ecfd-463">Três letras seguidas por seis dígitos</span><span class="sxs-lookup"><span data-stu-id="7ecfd-463">Three letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7ecfd-464">Padrão</span><span class="sxs-lookup"><span data-stu-id="7ecfd-464">Pattern</span></span>

<span data-ttu-id="7ecfd-465">Três letras e seis dígitos:</span><span class="sxs-lookup"><span data-stu-id="7ecfd-465">Three letters and six digits:</span></span>
  
-  <span data-ttu-id="7ecfd-466">Três letras (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="7ecfd-466">Three letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="7ecfd-467">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="7ecfd-467">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7ecfd-468">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="7ecfd-468">Checksum</span></span>

<span data-ttu-id="7ecfd-469">Não</span><span class="sxs-lookup"><span data-stu-id="7ecfd-469">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7ecfd-470">Definição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-470">Definition</span></span>

<span data-ttu-id="7ecfd-471">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="7ecfd-471">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7ecfd-472">A expressão `Regex_latvia_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-472">The regular expression  `Regex_latvia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7ecfd-473">Uma palavra- `Keywords_latvia_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-473">A keyword from  `Keywords_latvia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_driver's_license_number" />
          <Match idRef="Keywords_latvia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7ecfd-474">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="7ecfd-474">Keywords</span></span>

<span data-ttu-id="7ecfd-475">| |</span><span class="sxs-lookup"><span data-stu-id="7ecfd-475"></span></span>
|<span data-ttu-id="7ecfd-476">**Keywords_latvia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7ecfd-476">**Keywords_latvia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7ecfd-477">distribuição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-477">dl#</span></span>  <br/> <span data-ttu-id="7ecfd-478">driver license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-478">driver license</span></span>  <br/> <span data-ttu-id="7ecfd-479">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-479">driver license number</span></span>  <br/> <span data-ttu-id="7ecfd-480">licença de driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-480">driver licence</span></span>  <br/> <span data-ttu-id="7ecfd-481">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-481">drivers lic.</span></span>  <br/> <span data-ttu-id="7ecfd-482">drivers license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-482">drivers license</span></span>  <br/> <span data-ttu-id="7ecfd-483">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7ecfd-483">drivers licence</span></span>  <br/> <span data-ttu-id="7ecfd-484">driver's license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-484">driver's license</span></span>  <br/> <span data-ttu-id="7ecfd-485">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-485">driver's license number</span></span>  <br/> <span data-ttu-id="7ecfd-486">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-486">driver's licence number</span></span>  <br/> <span data-ttu-id="7ecfd-487">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="7ecfd-487">driving license number</span></span>  <br/> <span data-ttu-id="7ecfd-488">dlno#</span><span class="sxs-lookup"><span data-stu-id="7ecfd-488">dlno#</span></span>  <br/> <span data-ttu-id="7ecfd-489">autovadītāja apliecība</span><span class="sxs-lookup"><span data-stu-id="7ecfd-489">autovadītāja apliecība</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="7ecfd-490">Lituânia</span><span class="sxs-lookup"><span data-stu-id="7ecfd-490">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="7ecfd-491">Formatar</span><span class="sxs-lookup"><span data-stu-id="7ecfd-491">Format</span></span>

<span data-ttu-id="7ecfd-492">Oito dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="7ecfd-492">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7ecfd-493">Padrão</span><span class="sxs-lookup"><span data-stu-id="7ecfd-493">Pattern</span></span>

 <span data-ttu-id="7ecfd-494">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="7ecfd-494">Eight digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="7ecfd-495">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="7ecfd-495">Checksum</span></span>

<span data-ttu-id="7ecfd-496">Não</span><span class="sxs-lookup"><span data-stu-id="7ecfd-496">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7ecfd-497">Definição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-497">Definition</span></span>

<span data-ttu-id="7ecfd-498">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="7ecfd-498">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7ecfd-499">A expressão `Regex_lithuania_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-499">The regular expression  `Regex_lithuania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7ecfd-500">Uma palavra- `Keywords_lithuania_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-500">A keyword from  `Keywords_lithuania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_driver's_license_number" />
          <Match idRef="Keywords_lithuania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7ecfd-501">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="7ecfd-501">Keywords</span></span>

<span data-ttu-id="7ecfd-502">| |</span><span class="sxs-lookup"><span data-stu-id="7ecfd-502"></span></span>
|<span data-ttu-id="7ecfd-503">**Keywords_lithuania_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7ecfd-503">**Keywords_lithuania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7ecfd-504">distribuição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-504">dl#</span></span>  <br/> <span data-ttu-id="7ecfd-505">driver license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-505">driver license</span></span>  <br/> <span data-ttu-id="7ecfd-506">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-506">driver license number</span></span>  <br/> <span data-ttu-id="7ecfd-507">licença de driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-507">driver licence</span></span>  <br/> <span data-ttu-id="7ecfd-508">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-508">drivers lic.</span></span>  <br/> <span data-ttu-id="7ecfd-509">drivers license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-509">drivers license</span></span>  <br/> <span data-ttu-id="7ecfd-510">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7ecfd-510">drivers licence</span></span>  <br/> <span data-ttu-id="7ecfd-511">driver's license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-511">driver's license</span></span>  <br/> <span data-ttu-id="7ecfd-512">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-512">driver's license number</span></span>  <br/> <span data-ttu-id="7ecfd-513">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-513">driver's licence number</span></span>  <br/> <span data-ttu-id="7ecfd-514">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="7ecfd-514">driving license number</span></span>  <br/> <span data-ttu-id="7ecfd-515">dlno#</span><span class="sxs-lookup"><span data-stu-id="7ecfd-515">dlno#</span></span>  <br/> <span data-ttu-id="7ecfd-516">vairuotojo pažymėjimas</span><span class="sxs-lookup"><span data-stu-id="7ecfd-516">vairuotojo pažymėjimas</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="7ecfd-517">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="7ecfd-517">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="7ecfd-518">Formatar</span><span class="sxs-lookup"><span data-stu-id="7ecfd-518">Format</span></span>

<span data-ttu-id="7ecfd-519">Seis dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="7ecfd-519">Six digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7ecfd-520">Padrão</span><span class="sxs-lookup"><span data-stu-id="7ecfd-520">Pattern</span></span>

 <span data-ttu-id="7ecfd-521">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="7ecfd-521">Six digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="7ecfd-522">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="7ecfd-522">Checksum</span></span>

<span data-ttu-id="7ecfd-523">Não</span><span class="sxs-lookup"><span data-stu-id="7ecfd-523">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7ecfd-524">Definição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-524">Definition</span></span>

<span data-ttu-id="7ecfd-525">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="7ecfd-525">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7ecfd-526">A expressão `Regex_luxemburg_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-526">The regular expression  `Regex_luxemburg_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7ecfd-527">Uma palavra- `Keywords_luxemburg_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-527">A keyword from  `Keywords_luxemburg_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_driver's_license_number" />
          <Match idRef="Keywords_luxemburg_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7ecfd-528">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="7ecfd-528">Keywords</span></span>

<span data-ttu-id="7ecfd-529">| |</span><span class="sxs-lookup"><span data-stu-id="7ecfd-529"></span></span>
|<span data-ttu-id="7ecfd-530">**Keywords_luxemburg_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7ecfd-530">**Keywords_luxemburg_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7ecfd-531">distribuição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-531">dl#</span></span>  <br/> <span data-ttu-id="7ecfd-532">driver license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-532">driver license</span></span>  <br/> <span data-ttu-id="7ecfd-533">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-533">driver license number</span></span>  <br/> <span data-ttu-id="7ecfd-534">licença de driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-534">driver licence</span></span>  <br/> <span data-ttu-id="7ecfd-535">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-535">drivers lic.</span></span>  <br/> <span data-ttu-id="7ecfd-536">drivers license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-536">drivers license</span></span>  <br/> <span data-ttu-id="7ecfd-537">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7ecfd-537">drivers licence</span></span>  <br/> <span data-ttu-id="7ecfd-538">driver's license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-538">driver's license</span></span>  <br/> <span data-ttu-id="7ecfd-539">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-539">driver's license number</span></span>  <br/> <span data-ttu-id="7ecfd-540">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-540">driver's licence number</span></span>  <br/> <span data-ttu-id="7ecfd-541">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="7ecfd-541">driving license number</span></span>  <br/> <span data-ttu-id="7ecfd-542">dlno#</span><span class="sxs-lookup"><span data-stu-id="7ecfd-542">dlno#</span></span>  <br/> <span data-ttu-id="7ecfd-543">fahrerlaubnis</span><span class="sxs-lookup"><span data-stu-id="7ecfd-543">fahrerlaubnis</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="7ecfd-544">Malta</span><span class="sxs-lookup"><span data-stu-id="7ecfd-544">Malta</span></span>

### <a name="format"></a><span data-ttu-id="7ecfd-545">Formatar</span><span class="sxs-lookup"><span data-stu-id="7ecfd-545">Format</span></span>

<span data-ttu-id="7ecfd-546">Combinação de dois caracteres e seis dígitos no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="7ecfd-546">Combination of two characters and six digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7ecfd-547">Padrão</span><span class="sxs-lookup"><span data-stu-id="7ecfd-547">Pattern</span></span>

<span data-ttu-id="7ecfd-548">Combinação de dois caracteres e seis dígitos:</span><span class="sxs-lookup"><span data-stu-id="7ecfd-548">Combination of two characters and six digits:</span></span>
  
- <span data-ttu-id="7ecfd-549">Dois caracteres (dígitos ou letras, não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="7ecfd-549">Two characters (digits or letters, not case-sensitive)</span></span>
    
- <span data-ttu-id="7ecfd-550">Um espaço (opcional)</span><span class="sxs-lookup"><span data-stu-id="7ecfd-550">A space (optional)</span></span>
    
- <span data-ttu-id="7ecfd-551">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="7ecfd-551">Three digits</span></span>
    
- <span data-ttu-id="7ecfd-552">Um espaço (opcional)</span><span class="sxs-lookup"><span data-stu-id="7ecfd-552">A space (optional)</span></span>
    
- <span data-ttu-id="7ecfd-553">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="7ecfd-553">Three digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7ecfd-554">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="7ecfd-554">Checksum</span></span>

<span data-ttu-id="7ecfd-555">Não</span><span class="sxs-lookup"><span data-stu-id="7ecfd-555">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7ecfd-556">Definição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-556">Definition</span></span>

<span data-ttu-id="7ecfd-557">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="7ecfd-557">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7ecfd-558">A expressão `Regex_malta_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-558">The regular expression  `Regex_malta_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7ecfd-559">Uma palavra- `Keywords_malta_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-559">A keyword from  `Keywords_malta_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
 <Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_driver's_license_number" />
          <Match idRef="Keywords_malta_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7ecfd-560">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="7ecfd-560">Keywords</span></span>

<span data-ttu-id="7ecfd-561">| |</span><span class="sxs-lookup"><span data-stu-id="7ecfd-561"></span></span>
|<span data-ttu-id="7ecfd-562">**Keywords_malta_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7ecfd-562">**Keywords_malta_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7ecfd-563">distribuição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-563">dl#</span></span>  <br/> <span data-ttu-id="7ecfd-564">driver license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-564">driver license</span></span>  <br/> <span data-ttu-id="7ecfd-565">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-565">driver license number</span></span>  <br/> <span data-ttu-id="7ecfd-566">licença de driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-566">driver licence</span></span>  <br/> <span data-ttu-id="7ecfd-567">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-567">drivers lic.</span></span>  <br/> <span data-ttu-id="7ecfd-568">drivers license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-568">drivers license</span></span>  <br/> <span data-ttu-id="7ecfd-569">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7ecfd-569">drivers licence</span></span>  <br/> <span data-ttu-id="7ecfd-570">driver's license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-570">driver's license</span></span>  <br/> <span data-ttu-id="7ecfd-571">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-571">driver's license number</span></span>  <br/> <span data-ttu-id="7ecfd-572">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-572">driver's licence number</span></span>  <br/> <span data-ttu-id="7ecfd-573">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="7ecfd-573">driving license number</span></span>  <br/> <span data-ttu-id="7ecfd-574">dlno#</span><span class="sxs-lookup"><span data-stu-id="7ecfd-574">dlno#</span></span>  <br/> <span data-ttu-id="7ecfd-575">liċenzja tas-sewqan</span><span class="sxs-lookup"><span data-stu-id="7ecfd-575">liċenzja tas-sewqan</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="7ecfd-576">Países Baixos</span><span class="sxs-lookup"><span data-stu-id="7ecfd-576">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="7ecfd-577">Formatar</span><span class="sxs-lookup"><span data-stu-id="7ecfd-577">Format</span></span>

<span data-ttu-id="7ecfd-578">10 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="7ecfd-578">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7ecfd-579">Padrão</span><span class="sxs-lookup"><span data-stu-id="7ecfd-579">Pattern</span></span>

<span data-ttu-id="7ecfd-580">10 dígitos</span><span class="sxs-lookup"><span data-stu-id="7ecfd-580">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="7ecfd-581">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="7ecfd-581">Checksum</span></span>

<span data-ttu-id="7ecfd-582">Não</span><span class="sxs-lookup"><span data-stu-id="7ecfd-582">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7ecfd-583">Definição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-583">Definition</span></span>

<span data-ttu-id="7ecfd-584">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="7ecfd-584">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7ecfd-585">A expressão `Regex_netherlands_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-585">The regular expression  `Regex_netherlands_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7ecfd-586">Uma palavra- `Keywords_netherlands_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-586">A keyword from  `Keywords_netherlands_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_driver's_license_number" />
          <Match idRef="Keywords_netherlands_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7ecfd-587">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="7ecfd-587">Keywords</span></span>

<span data-ttu-id="7ecfd-588">| |</span><span class="sxs-lookup"><span data-stu-id="7ecfd-588"></span></span>
|<span data-ttu-id="7ecfd-589">**Keywords_netherlands_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7ecfd-589">**Keywords_netherlands_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7ecfd-590">distribuição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-590">dl#</span></span>  <br/> <span data-ttu-id="7ecfd-591">driver license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-591">driver license</span></span>  <br/> <span data-ttu-id="7ecfd-592">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-592">driver license number</span></span>  <br/> <span data-ttu-id="7ecfd-593">licença de driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-593">driver licence</span></span>  <br/> <span data-ttu-id="7ecfd-594">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-594">drivers lic.</span></span>  <br/> <span data-ttu-id="7ecfd-595">drivers license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-595">drivers license</span></span>  <br/> <span data-ttu-id="7ecfd-596">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7ecfd-596">drivers licence</span></span>  <br/> <span data-ttu-id="7ecfd-597">driver's license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-597">driver's license</span></span>  <br/> <span data-ttu-id="7ecfd-598">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-598">driver's license number</span></span>  <br/> <span data-ttu-id="7ecfd-599">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-599">driver's licence number</span></span>  <br/> <span data-ttu-id="7ecfd-600">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="7ecfd-600">driving license number</span></span>  <br/> <span data-ttu-id="7ecfd-601">dlno#</span><span class="sxs-lookup"><span data-stu-id="7ecfd-601">dlno#</span></span>  <br/> <span data-ttu-id="7ecfd-602">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="7ecfd-602">permis de conduire</span></span>  <br/> <span data-ttu-id="7ecfd-603">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="7ecfd-603">rijbewijs</span></span>  <br/> <span data-ttu-id="7ecfd-604">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="7ecfd-604">rijbewijsnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="7ecfd-605">Polônia</span><span class="sxs-lookup"><span data-stu-id="7ecfd-605">Poland</span></span>

### <a name="format"></a><span data-ttu-id="7ecfd-606">Formatar</span><span class="sxs-lookup"><span data-stu-id="7ecfd-606">Format</span></span>

<span data-ttu-id="7ecfd-607">14 dígitos contendo 2 barras</span><span class="sxs-lookup"><span data-stu-id="7ecfd-607">14 digits containing 2 forward slashes</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7ecfd-608">Padrão</span><span class="sxs-lookup"><span data-stu-id="7ecfd-608">Pattern</span></span>

<span data-ttu-id="7ecfd-609">14 dígitos e 2 barras de avanço:</span><span class="sxs-lookup"><span data-stu-id="7ecfd-609">14 digits and 2 forward slashes:</span></span>
  
-  <span data-ttu-id="7ecfd-610">Cinco dígitos</span><span class="sxs-lookup"><span data-stu-id="7ecfd-610">Five digits</span></span> 
    
- <span data-ttu-id="7ecfd-611">Uma barra</span><span class="sxs-lookup"><span data-stu-id="7ecfd-611">A forward slash</span></span>
    
- <span data-ttu-id="7ecfd-612">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="7ecfd-612">Two digits</span></span>
    
- <span data-ttu-id="7ecfd-613">Uma barra</span><span class="sxs-lookup"><span data-stu-id="7ecfd-613">A forward slash</span></span>
    
- <span data-ttu-id="7ecfd-614">Sete dígitos</span><span class="sxs-lookup"><span data-stu-id="7ecfd-614">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7ecfd-615">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="7ecfd-615">Checksum</span></span>

<span data-ttu-id="7ecfd-616">Não</span><span class="sxs-lookup"><span data-stu-id="7ecfd-616">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7ecfd-617">Definição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-617">Definition</span></span>

<span data-ttu-id="7ecfd-618">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="7ecfd-618">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7ecfd-619">A expressão `Regex_poland_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-619">The regular expression  `Regex_poland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7ecfd-620">Uma palavra- `Keywords_poland_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-620">A keyword from  `Keywords_poland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_driver's_license_number" />
          <Match idRef="Keywords_poland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7ecfd-621">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="7ecfd-621">Keywords</span></span>

<span data-ttu-id="7ecfd-622">| |</span><span class="sxs-lookup"><span data-stu-id="7ecfd-622"></span></span>
|<span data-ttu-id="7ecfd-623">**Keywords_poland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7ecfd-623">**Keywords_poland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7ecfd-624">distribuição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-624">dl#</span></span>  <br/> <span data-ttu-id="7ecfd-625">driver license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-625">driver license</span></span>  <br/> <span data-ttu-id="7ecfd-626">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-626">driver license number</span></span>  <br/> <span data-ttu-id="7ecfd-627">licença de driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-627">driver licence</span></span>  <br/> <span data-ttu-id="7ecfd-628">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-628">drivers lic.</span></span>  <br/> <span data-ttu-id="7ecfd-629">drivers license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-629">drivers license</span></span>  <br/> <span data-ttu-id="7ecfd-630">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7ecfd-630">drivers licence</span></span>  <br/> <span data-ttu-id="7ecfd-631">driver's license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-631">driver's license</span></span>  <br/> <span data-ttu-id="7ecfd-632">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-632">driver's license number</span></span>  <br/> <span data-ttu-id="7ecfd-633">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-633">driver's licence number</span></span>  <br/> <span data-ttu-id="7ecfd-634">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="7ecfd-634">driving license number</span></span>  <br/> <span data-ttu-id="7ecfd-635">dlno#</span><span class="sxs-lookup"><span data-stu-id="7ecfd-635">dlno#</span></span>  <br/> <span data-ttu-id="7ecfd-636">prawo jazdy</span><span class="sxs-lookup"><span data-stu-id="7ecfd-636">prawo jazdy</span></span>  <br/> |
   
## <a name="portugal"></a><span data-ttu-id="7ecfd-637">Portugal</span><span class="sxs-lookup"><span data-stu-id="7ecfd-637">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="7ecfd-638">Formatar</span><span class="sxs-lookup"><span data-stu-id="7ecfd-638">Format</span></span>

<span data-ttu-id="7ecfd-639">Duas letras seguidas por sete números no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="7ecfd-639">Two letters followed by a seven numbers in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7ecfd-640">Padrão</span><span class="sxs-lookup"><span data-stu-id="7ecfd-640">Pattern</span></span>

<span data-ttu-id="7ecfd-641">Duas letras seguidas por sete números com caracteres especiais:</span><span class="sxs-lookup"><span data-stu-id="7ecfd-641">Two letters followed by seven numbers with special characters:</span></span>
  
-  <span data-ttu-id="7ecfd-642">Duas letras (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="7ecfd-642">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="7ecfd-643">Um hífen</span><span class="sxs-lookup"><span data-stu-id="7ecfd-643">A hyphen</span></span>
    
- <span data-ttu-id="7ecfd-644">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="7ecfd-644">Six digits</span></span>
    
- <span data-ttu-id="7ecfd-645">Um espaço</span><span class="sxs-lookup"><span data-stu-id="7ecfd-645">A space</span></span>
    
- <span data-ttu-id="7ecfd-646">Um dígito</span><span class="sxs-lookup"><span data-stu-id="7ecfd-646">One digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7ecfd-647">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="7ecfd-647">Checksum</span></span>

<span data-ttu-id="7ecfd-648">Não</span><span class="sxs-lookup"><span data-stu-id="7ecfd-648">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7ecfd-649">Definição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-649">Definition</span></span>

<span data-ttu-id="7ecfd-650">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="7ecfd-650">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7ecfd-651">A expressão `Regex_portugal_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-651">The regular expression  `Regex_portugal_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7ecfd-652">Uma palavra- `Keywords_portugal_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-652">A keyword from  `Keywords_portugal_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_driver's_license_number" />
          <Match idRef="Keywords_portugal_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7ecfd-653">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="7ecfd-653">Keywords</span></span>

<span data-ttu-id="7ecfd-654">| |</span><span class="sxs-lookup"><span data-stu-id="7ecfd-654"></span></span>
|<span data-ttu-id="7ecfd-655">**Keywords_portugal_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7ecfd-655">**Keywords_portugal_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7ecfd-656">distribuição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-656">dl#</span></span>  <br/> <span data-ttu-id="7ecfd-657">driver license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-657">driver license</span></span>  <br/> <span data-ttu-id="7ecfd-658">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-658">driver license number</span></span>  <br/> <span data-ttu-id="7ecfd-659">licença de driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-659">driver licence</span></span>  <br/> <span data-ttu-id="7ecfd-660">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-660">drivers lic.</span></span>  <br/> <span data-ttu-id="7ecfd-661">drivers license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-661">drivers license</span></span>  <br/> <span data-ttu-id="7ecfd-662">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7ecfd-662">drivers licence</span></span>  <br/> <span data-ttu-id="7ecfd-663">driver's license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-663">driver's license</span></span>  <br/> <span data-ttu-id="7ecfd-664">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-664">driver's license number</span></span>  <br/> <span data-ttu-id="7ecfd-665">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-665">driver's licence number</span></span>  <br/> <span data-ttu-id="7ecfd-666">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="7ecfd-666">driving license number</span></span>  <br/> <span data-ttu-id="7ecfd-667">dlno#</span><span class="sxs-lookup"><span data-stu-id="7ecfd-667">dlno#</span></span>  <br/> <span data-ttu-id="7ecfd-668">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-668">carteira de motorista</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="7ecfd-669">Romênia</span><span class="sxs-lookup"><span data-stu-id="7ecfd-669">Romania</span></span>

### <a name="format"></a><span data-ttu-id="7ecfd-670">Formatar</span><span class="sxs-lookup"><span data-stu-id="7ecfd-670">Format</span></span>

<span data-ttu-id="7ecfd-671">Um caractere seguido por oito dígitos</span><span class="sxs-lookup"><span data-stu-id="7ecfd-671">One character followed by eight digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7ecfd-672">Padrão</span><span class="sxs-lookup"><span data-stu-id="7ecfd-672">Pattern</span></span>

<span data-ttu-id="7ecfd-673">Um caractere seguido por oito dígitos:</span><span class="sxs-lookup"><span data-stu-id="7ecfd-673">One character followed by eight digits:</span></span>
  
-  <span data-ttu-id="7ecfd-674">Uma letra (não diferencia maiúsculas de minúsculas) ou dígito</span><span class="sxs-lookup"><span data-stu-id="7ecfd-674">One letter (not case-sensitive) or digit</span></span> 
    
- <span data-ttu-id="7ecfd-675">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="7ecfd-675">Eight digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7ecfd-676">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="7ecfd-676">Checksum</span></span>

<span data-ttu-id="7ecfd-677">Não</span><span class="sxs-lookup"><span data-stu-id="7ecfd-677">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7ecfd-678">Definição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-678">Definition</span></span>

<span data-ttu-id="7ecfd-679">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="7ecfd-679">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7ecfd-680">A expressão `Regex_romania_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-680">The regular expression  `Regex_romania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7ecfd-681">Uma palavra- `Keywords_romania_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-681">A keyword from  `Keywords_romania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_driver's_license_number" />
          <Match idRef="Keywords_romania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7ecfd-682">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="7ecfd-682">Keywords</span></span>

<span data-ttu-id="7ecfd-683">| |</span><span class="sxs-lookup"><span data-stu-id="7ecfd-683"></span></span>
|<span data-ttu-id="7ecfd-684">**Keywords_romania_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7ecfd-684">**Keywords_romania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7ecfd-685">distribuição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-685">dl#</span></span>  <br/> <span data-ttu-id="7ecfd-686">driver license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-686">driver license</span></span>  <br/> <span data-ttu-id="7ecfd-687">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-687">driver license number</span></span>  <br/> <span data-ttu-id="7ecfd-688">licença de driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-688">driver licence</span></span>  <br/> <span data-ttu-id="7ecfd-689">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-689">drivers lic.</span></span>  <br/> <span data-ttu-id="7ecfd-690">drivers license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-690">drivers license</span></span>  <br/> <span data-ttu-id="7ecfd-691">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7ecfd-691">drivers licence</span></span>  <br/> <span data-ttu-id="7ecfd-692">driver's license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-692">driver's license</span></span>  <br/> <span data-ttu-id="7ecfd-693">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-693">driver's license number</span></span>  <br/> <span data-ttu-id="7ecfd-694">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-694">driver's licence number</span></span>  <br/> <span data-ttu-id="7ecfd-695">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="7ecfd-695">driving license number</span></span>  <br/> <span data-ttu-id="7ecfd-696">dlno#</span><span class="sxs-lookup"><span data-stu-id="7ecfd-696">dlno#</span></span>  <br/> <span data-ttu-id="7ecfd-697">permé de conducere</span><span class="sxs-lookup"><span data-stu-id="7ecfd-697">permis de conducere</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="7ecfd-698">Eslováquia</span><span class="sxs-lookup"><span data-stu-id="7ecfd-698">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="7ecfd-699">Formatar</span><span class="sxs-lookup"><span data-stu-id="7ecfd-699">Format</span></span>

<span data-ttu-id="7ecfd-700">Um caractere seguido por sete dígitos</span><span class="sxs-lookup"><span data-stu-id="7ecfd-700">One character followed by seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7ecfd-701">Padrão</span><span class="sxs-lookup"><span data-stu-id="7ecfd-701">Pattern</span></span>

<span data-ttu-id="7ecfd-702">Um caractere seguido por sete dígitos</span><span class="sxs-lookup"><span data-stu-id="7ecfd-702">One character followed by seven digits</span></span>
  
- <span data-ttu-id="7ecfd-703">Uma letra (não diferencia maiúsculas de minúsculas) ou dígito</span><span class="sxs-lookup"><span data-stu-id="7ecfd-703">One letter (not case-sensitive) or digit</span></span>
    
-  <span data-ttu-id="7ecfd-704">Sete dígitos</span><span class="sxs-lookup"><span data-stu-id="7ecfd-704">Seven digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="7ecfd-705">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="7ecfd-705">Checksum</span></span>

<span data-ttu-id="7ecfd-706">Não</span><span class="sxs-lookup"><span data-stu-id="7ecfd-706">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7ecfd-707">Definição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-707">Definition</span></span>

<span data-ttu-id="7ecfd-708">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="7ecfd-708">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7ecfd-709">A expressão `Regex_slovakia_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-709">The regular expression  `Regex_slovakia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7ecfd-710">Uma palavra- `Keywords_slovakia_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-710">A keyword from  `Keywords_slovakia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovaknia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovakia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7ecfd-711">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="7ecfd-711">Keywords</span></span>

<span data-ttu-id="7ecfd-712">| |</span><span class="sxs-lookup"><span data-stu-id="7ecfd-712"></span></span>
|<span data-ttu-id="7ecfd-713">**Keywords_slovakia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7ecfd-713">**Keywords_slovakia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7ecfd-714">distribuição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-714">dl#</span></span>  <br/> <span data-ttu-id="7ecfd-715">driver license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-715">driver license</span></span>  <br/> <span data-ttu-id="7ecfd-716">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-716">driver license number</span></span>  <br/> <span data-ttu-id="7ecfd-717">licença de driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-717">driver licence</span></span>  <br/> <span data-ttu-id="7ecfd-718">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-718">drivers lic.</span></span>  <br/> <span data-ttu-id="7ecfd-719">drivers license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-719">drivers license</span></span>  <br/> <span data-ttu-id="7ecfd-720">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7ecfd-720">drivers licence</span></span>  <br/> <span data-ttu-id="7ecfd-721">driver's license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-721">driver's license</span></span>  <br/> <span data-ttu-id="7ecfd-722">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-722">driver's license number</span></span>  <br/> <span data-ttu-id="7ecfd-723">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-723">driver's licence number</span></span>  <br/> <span data-ttu-id="7ecfd-724">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="7ecfd-724">driving license number</span></span>  <br/> <span data-ttu-id="7ecfd-725">dlno#</span><span class="sxs-lookup"><span data-stu-id="7ecfd-725">dlno#</span></span>  <br/> <span data-ttu-id="7ecfd-726">vodičský preukaz</span><span class="sxs-lookup"><span data-stu-id="7ecfd-726">vodičský preukaz</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="7ecfd-727">Eslovênia</span><span class="sxs-lookup"><span data-stu-id="7ecfd-727">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="7ecfd-728">Formatar</span><span class="sxs-lookup"><span data-stu-id="7ecfd-728">Format</span></span>

<span data-ttu-id="7ecfd-729">Nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="7ecfd-729">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7ecfd-730">Padrão</span><span class="sxs-lookup"><span data-stu-id="7ecfd-730">Pattern</span></span>

<span data-ttu-id="7ecfd-731">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="7ecfd-731">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="7ecfd-732">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="7ecfd-732">Checksum</span></span>

<span data-ttu-id="7ecfd-733">Não</span><span class="sxs-lookup"><span data-stu-id="7ecfd-733">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7ecfd-734">Definição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-734">Definition</span></span>

<span data-ttu-id="7ecfd-735">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="7ecfd-735">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7ecfd-736">A expressão `Regex_slovenia_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-736">The regular expression  `Regex_slovenia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7ecfd-737">Uma palavra- `Keywords_slovenia_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-737">A keyword from  `Keywords_slovenia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovenia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7ecfd-738">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="7ecfd-738">Keywords</span></span>

<span data-ttu-id="7ecfd-739">| |</span><span class="sxs-lookup"><span data-stu-id="7ecfd-739"></span></span>
|<span data-ttu-id="7ecfd-740">**Keywords_slovenia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7ecfd-740">**Keywords_slovenia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7ecfd-741">distribuição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-741">dl#</span></span>  <br/> <span data-ttu-id="7ecfd-742">driver license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-742">driver license</span></span>  <br/> <span data-ttu-id="7ecfd-743">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-743">driver license number</span></span>  <br/> <span data-ttu-id="7ecfd-744">licença de driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-744">driver licence</span></span>  <br/> <span data-ttu-id="7ecfd-745">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-745">drivers lic.</span></span>  <br/> <span data-ttu-id="7ecfd-746">drivers license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-746">drivers license</span></span>  <br/> <span data-ttu-id="7ecfd-747">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7ecfd-747">drivers licence</span></span>  <br/> <span data-ttu-id="7ecfd-748">driver's license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-748">driver's license</span></span>  <br/> <span data-ttu-id="7ecfd-749">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-749">driver's license number</span></span>  <br/> <span data-ttu-id="7ecfd-750">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-750">driver's licence number</span></span>  <br/> <span data-ttu-id="7ecfd-751">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="7ecfd-751">driving license number</span></span>  <br/> <span data-ttu-id="7ecfd-752">dlno#</span><span class="sxs-lookup"><span data-stu-id="7ecfd-752">dlno#</span></span>  <br/> <span data-ttu-id="7ecfd-753">vozniško dovoljenje</span><span class="sxs-lookup"><span data-stu-id="7ecfd-753">vozniško dovoljenje</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="7ecfd-754">Espanha</span><span class="sxs-lookup"><span data-stu-id="7ecfd-754">Spain</span></span>

### <a name="format"></a><span data-ttu-id="7ecfd-755">Formatar</span><span class="sxs-lookup"><span data-stu-id="7ecfd-755">Format</span></span>

<span data-ttu-id="7ecfd-756">Oito dígitos seguidos de um caractere</span><span class="sxs-lookup"><span data-stu-id="7ecfd-756">Eight digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7ecfd-757">Padrão</span><span class="sxs-lookup"><span data-stu-id="7ecfd-757">Pattern</span></span>

<span data-ttu-id="7ecfd-758">Oito dígitos seguidos de um caractere:</span><span class="sxs-lookup"><span data-stu-id="7ecfd-758">Eight digits followed by one character:</span></span>
  
-  <span data-ttu-id="7ecfd-759">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="7ecfd-759">Eight digits</span></span> 
    
- <span data-ttu-id="7ecfd-760">Um dígito ou letra (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="7ecfd-760">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7ecfd-761">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="7ecfd-761">Checksum</span></span>

<span data-ttu-id="7ecfd-762">Sim</span><span class="sxs-lookup"><span data-stu-id="7ecfd-762">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="7ecfd-763">Definição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-763">Definition</span></span>

<span data-ttu-id="7ecfd-764">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="7ecfd-764">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7ecfd-765">A função `Func_spain_eu_driver's_license_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-765">The function  `Func_spain_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7ecfd-766">Uma palavra- `Keywords_spain_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-766">A keyword from  `Keywords_spain_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_driver's_license_number" />
          <Match idRef="Keywords_spain_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7ecfd-767">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="7ecfd-767">Keywords</span></span>

<span data-ttu-id="7ecfd-768">| |</span><span class="sxs-lookup"><span data-stu-id="7ecfd-768"></span></span>
|<span data-ttu-id="7ecfd-769">**Keywords_spain_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7ecfd-769">**Keywords_spain_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7ecfd-770">dlno#</span><span class="sxs-lookup"><span data-stu-id="7ecfd-770">dlno#</span></span>  <br/> <span data-ttu-id="7ecfd-771">distribuição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-771">dl#</span></span>  <br/> <span data-ttu-id="7ecfd-772">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-772">drivers lic.</span></span>  <br/> <span data-ttu-id="7ecfd-773">licença de driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-773">driver licence</span></span>  <br/> <span data-ttu-id="7ecfd-774">driver license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-774">driver license</span></span>  <br/> <span data-ttu-id="7ecfd-775">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7ecfd-775">drivers licence</span></span>  <br/> <span data-ttu-id="7ecfd-776">drivers license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-776">drivers license</span></span>  <br/> <span data-ttu-id="7ecfd-777">driver's licence</span><span class="sxs-lookup"><span data-stu-id="7ecfd-777">driver's licence</span></span>  <br/> <span data-ttu-id="7ecfd-778">driver's license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-778">driver's license</span></span>  <br/> <span data-ttu-id="7ecfd-779">driving licence</span><span class="sxs-lookup"><span data-stu-id="7ecfd-779">driving licence</span></span>  <br/> <span data-ttu-id="7ecfd-780">driving licence</span><span class="sxs-lookup"><span data-stu-id="7ecfd-780">driving license</span></span>  <br/> <span data-ttu-id="7ecfd-781">número de licença de driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-781">driver licence number</span></span>  <br/> <span data-ttu-id="7ecfd-782">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-782">driver license number</span></span>  <br/> <span data-ttu-id="7ecfd-783">número de licença de drivers</span><span class="sxs-lookup"><span data-stu-id="7ecfd-783">drivers licence number</span></span>  <br/> <span data-ttu-id="7ecfd-784">número de licença de drivers</span><span class="sxs-lookup"><span data-stu-id="7ecfd-784">drivers license number</span></span>  <br/> <span data-ttu-id="7ecfd-785">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-785">driver's licence number</span></span>  <br/> <span data-ttu-id="7ecfd-786">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-786">driver's license number</span></span>  <br/> <span data-ttu-id="7ecfd-787">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="7ecfd-787">driving licence number</span></span>  <br/> <span data-ttu-id="7ecfd-788">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="7ecfd-788">driving license number</span></span>  <br/> <span data-ttu-id="7ecfd-789">permissão de condução</span><span class="sxs-lookup"><span data-stu-id="7ecfd-789">driving permit</span></span>  <br/> <span data-ttu-id="7ecfd-790">número de permissão de dirigir</span><span class="sxs-lookup"><span data-stu-id="7ecfd-790">driving permit number</span></span>  <br/> <span data-ttu-id="7ecfd-791">permiso de conducción</span><span class="sxs-lookup"><span data-stu-id="7ecfd-791">permiso de conducción</span></span>  <br/> <span data-ttu-id="7ecfd-792">permiso conducción</span><span class="sxs-lookup"><span data-stu-id="7ecfd-792">permiso conducción</span></span>  <br/> <span data-ttu-id="7ecfd-793">número licencia conducir</span><span class="sxs-lookup"><span data-stu-id="7ecfd-793">número licencia conducir</span></span>  <br/> <span data-ttu-id="7ecfd-794">número de Carnet de conducir</span><span class="sxs-lookup"><span data-stu-id="7ecfd-794">número de carnet de conducir</span></span>  <br/> <span data-ttu-id="7ecfd-795">número Carnet conducir</span><span class="sxs-lookup"><span data-stu-id="7ecfd-795">número carnet conducir</span></span>  <br/> <span data-ttu-id="7ecfd-796">licencia conducir</span><span class="sxs-lookup"><span data-stu-id="7ecfd-796">licencia conducir</span></span>  <br/> <span data-ttu-id="7ecfd-797">número de permiso de conducir</span><span class="sxs-lookup"><span data-stu-id="7ecfd-797">número de permiso de conducir</span></span>  <br/> <span data-ttu-id="7ecfd-798">número de permiso conducir</span><span class="sxs-lookup"><span data-stu-id="7ecfd-798">número de permiso conducir</span></span>  <br/> <span data-ttu-id="7ecfd-799">número permiso conducir</span><span class="sxs-lookup"><span data-stu-id="7ecfd-799">número permiso conducir</span></span>  <br/> <span data-ttu-id="7ecfd-800">permiso conducir</span><span class="sxs-lookup"><span data-stu-id="7ecfd-800">permiso conducir</span></span>  <br/> <span data-ttu-id="7ecfd-801">licencia de manejo</span><span class="sxs-lookup"><span data-stu-id="7ecfd-801">licencia de manejo</span></span>  <br/> <span data-ttu-id="7ecfd-802">El Carnet de conducir</span><span class="sxs-lookup"><span data-stu-id="7ecfd-802">el carnet de conducir</span></span>  <br/> <span data-ttu-id="7ecfd-803">carnet conducir</span><span class="sxs-lookup"><span data-stu-id="7ecfd-803">carnet conducir</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="7ecfd-804">Suécia</span><span class="sxs-lookup"><span data-stu-id="7ecfd-804">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="7ecfd-805">Formatar</span><span class="sxs-lookup"><span data-stu-id="7ecfd-805">Format</span></span>

<span data-ttu-id="7ecfd-806">Dez dígitos contendo um hífen</span><span class="sxs-lookup"><span data-stu-id="7ecfd-806">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7ecfd-807">Padrão</span><span class="sxs-lookup"><span data-stu-id="7ecfd-807">Pattern</span></span>

<span data-ttu-id="7ecfd-808">Dez dígitos contendo um hífen:</span><span class="sxs-lookup"><span data-stu-id="7ecfd-808">Ten digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="7ecfd-809">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="7ecfd-809">Six digits</span></span> 
    
- <span data-ttu-id="7ecfd-810">Um hífen</span><span class="sxs-lookup"><span data-stu-id="7ecfd-810">A hyphen</span></span>
    
- <span data-ttu-id="7ecfd-811">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="7ecfd-811">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7ecfd-812">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="7ecfd-812">Checksum</span></span>

<span data-ttu-id="7ecfd-813">Não</span><span class="sxs-lookup"><span data-stu-id="7ecfd-813">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7ecfd-814">Definição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-814">Definition</span></span>

<span data-ttu-id="7ecfd-815">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="7ecfd-815">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7ecfd-816">A expressão `Regex_sweden_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-816">The regular expression  `Regex_sweden_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7ecfd-817">Uma palavra- `Keywords_sweden_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-817">A keyword from  `Keywords_sweden_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_driver's_license_number" />
          <Match idRef="Keywords_sweden_eu_driver's_license_number" />
        </Pattern>
</Entity> 
```

### <a name="keywords"></a><span data-ttu-id="7ecfd-818">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="7ecfd-818">Keywords</span></span>

<span data-ttu-id="7ecfd-819">| |</span><span class="sxs-lookup"><span data-stu-id="7ecfd-819"></span></span>
|<span data-ttu-id="7ecfd-820">**Keywords_sweden_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7ecfd-820">**Keywords_sweden_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7ecfd-821">distribuição</span><span class="sxs-lookup"><span data-stu-id="7ecfd-821">dl#</span></span>  <br/> <span data-ttu-id="7ecfd-822">driver license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-822">driver license</span></span>  <br/> <span data-ttu-id="7ecfd-823">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-823">driver license number</span></span>  <br/> <span data-ttu-id="7ecfd-824">licença de driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-824">driver licence</span></span>  <br/> <span data-ttu-id="7ecfd-825">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="7ecfd-825">drivers lic.</span></span>  <br/> <span data-ttu-id="7ecfd-826">drivers license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-826">drivers license</span></span>  <br/> <span data-ttu-id="7ecfd-827">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7ecfd-827">drivers licence</span></span>  <br/> <span data-ttu-id="7ecfd-828">driver's license</span><span class="sxs-lookup"><span data-stu-id="7ecfd-828">driver's license</span></span>  <br/> <span data-ttu-id="7ecfd-829">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7ecfd-829">driver's license number</span></span>  <br/> <span data-ttu-id="7ecfd-830">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="7ecfd-830">driver's licence number</span></span>  <br/> <span data-ttu-id="7ecfd-831">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="7ecfd-831">driving license number</span></span>  <br/> <span data-ttu-id="7ecfd-832">dlno#</span><span class="sxs-lookup"><span data-stu-id="7ecfd-832">dlno#</span></span>  <br/> <span data-ttu-id="7ecfd-833">körkort</span><span class="sxs-lookup"><span data-stu-id="7ecfd-833">körkort</span></span>  <br/> |
   
## <a name="uk"></a><span data-ttu-id="7ecfd-834">Reino Unido</span><span class="sxs-lookup"><span data-stu-id="7ecfd-834">UK</span></span>

<span data-ttu-id="7ecfd-835">Para obter detalhes, consulte a seção "Reino Unido</span><span class="sxs-lookup"><span data-stu-id="7ecfd-835">For details, see the section "U.K.</span></span> <span data-ttu-id="7ecfd-836">Número da carteira de motorista "em [que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="7ecfd-836">Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7ecfd-837">Confira também</span><span class="sxs-lookup"><span data-stu-id="7ecfd-837">See also</span></span>

[<span data-ttu-id="7ecfd-838">O que os tipos de informações confidenciais procuram</span><span class="sxs-lookup"><span data-stu-id="7ecfd-838">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)


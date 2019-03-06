---
title: Número da carteira de motorista da UE
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: Este tópico mostra o que uma política de prevenção de perda de dados (DLP) procura quando detecta o tipo de informação confidencial do número de licença do driver da UE. Esse tipo de informação confidencial define diferentes padrões, palavras-chave e outras evidências para cada país.
ms.openlocfilehash: be9497c325866a670dff8d82b5170f4ca947c4ad
ms.sourcegitcommit: ed822a776d3419853453583e882f3c61ca26d4b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2019
ms.locfileid: "30410746"
---
# <a name="eu-drivers-license-number"></a><span data-ttu-id="540c7-104">Número da carteira de motorista da UE</span><span class="sxs-lookup"><span data-stu-id="540c7-104">EU Driver's License Number</span></span>

<span data-ttu-id="540c7-105">Este tópico mostra o que uma política de prevenção de perda de dados (DLP) procura quando detecta o tipo de informação confidencial do número de licença do driver da UE.</span><span class="sxs-lookup"><span data-stu-id="540c7-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Driver's License Number sensitive information type.</span></span> <span data-ttu-id="540c7-106">Esse tipo de informação confidencial define diferentes padrões, palavras-chave e outras evidências para cada país.</span><span class="sxs-lookup"><span data-stu-id="540c7-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="540c7-107">Áustria </span><span class="sxs-lookup"><span data-stu-id="540c7-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="540c7-108">Format</span><span class="sxs-lookup"><span data-stu-id="540c7-108">Format</span></span>

<span data-ttu-id="540c7-109">Oito dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="540c7-109">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="540c7-110">Padrão</span><span class="sxs-lookup"><span data-stu-id="540c7-110">Pattern</span></span>

<span data-ttu-id="540c7-111">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="540c7-111">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="540c7-112">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="540c7-112">Checksum</span></span>

<span data-ttu-id="540c7-113">Não</span><span class="sxs-lookup"><span data-stu-id="540c7-113">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="540c7-114">Definição</span><span class="sxs-lookup"><span data-stu-id="540c7-114">Definition</span></span>

<span data-ttu-id="540c7-115">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="540c7-115">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="540c7-116">A expressão `Regex_austria_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="540c7-116">The regular expression  `Regex_austria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="540c7-117">Uma palavra- `Keywords_austria_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="540c7-117">A keyword from  `Keywords_austria_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_driver's_license_number" />
          <Match idRef="Keywords_austria_eu_driver's_license_number" />
        </Pattern>
    </Entity>

```

### <a name="keywords"></a><span data-ttu-id="540c7-118">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="540c7-118">Keywords</span></span>

<span data-ttu-id="540c7-119">| |</span><span class="sxs-lookup"><span data-stu-id="540c7-119"></span></span>
|<span data-ttu-id="540c7-120">**Keywords_austria_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="540c7-120">**Keywords_austria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="540c7-121">distribuição</span><span class="sxs-lookup"><span data-stu-id="540c7-121">dl#</span></span>  <br/> <span data-ttu-id="540c7-122">driver license</span><span class="sxs-lookup"><span data-stu-id="540c7-122">driver license</span></span>  <br/> <span data-ttu-id="540c7-123">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-123">driver license number</span></span>  <br/> <span data-ttu-id="540c7-124">licença de driver</span><span class="sxs-lookup"><span data-stu-id="540c7-124">driver licence</span></span>  <br/> <span data-ttu-id="540c7-125">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="540c7-125">drivers lic.</span></span>  <br/> <span data-ttu-id="540c7-126">drivers license</span><span class="sxs-lookup"><span data-stu-id="540c7-126">drivers license</span></span>  <br/> <span data-ttu-id="540c7-127">driver's licence</span><span class="sxs-lookup"><span data-stu-id="540c7-127">driver's licence</span></span>  <br/> <span data-ttu-id="540c7-128">driver's license</span><span class="sxs-lookup"><span data-stu-id="540c7-128">driver's license</span></span>  <br/> <span data-ttu-id="540c7-129">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-129">driver's license number</span></span>  <br/> <span data-ttu-id="540c7-130">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="540c7-130">driver's licence number</span></span>  <br/>  <span data-ttu-id="540c7-131">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="540c7-131">driving license number</span></span>  <br/> <span data-ttu-id="540c7-132">dlno #</span><span class="sxs-lookup"><span data-stu-id="540c7-132">dlno#</span></span>  <br/> <span data-ttu-id="540c7-133">fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="540c7-133">fuhrerschein</span></span>  <br/> <span data-ttu-id="540c7-134">fuhrerschein Republik Osterreich</span><span class="sxs-lookup"><span data-stu-id="540c7-134">fuhrerschein republik osterreich</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="540c7-135">Bélgica </span><span class="sxs-lookup"><span data-stu-id="540c7-135">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="540c7-136">Format</span><span class="sxs-lookup"><span data-stu-id="540c7-136">Format</span></span>

<span data-ttu-id="540c7-137">10 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="540c7-137">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="540c7-138">Padrão</span><span class="sxs-lookup"><span data-stu-id="540c7-138">Pattern</span></span>

<span data-ttu-id="540c7-139">10 dígitos</span><span class="sxs-lookup"><span data-stu-id="540c7-139">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="540c7-140">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="540c7-140">Checksum</span></span>

<span data-ttu-id="540c7-141">Não</span><span class="sxs-lookup"><span data-stu-id="540c7-141">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="540c7-142">Definição</span><span class="sxs-lookup"><span data-stu-id="540c7-142">Definition</span></span>

<span data-ttu-id="540c7-143">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="540c7-143">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="540c7-144">A expressão `Regex_belgium_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="540c7-144">The regular expression  `Regex_belgium_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="540c7-145">Uma palavra- `Keywords_belgium_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="540c7-145">A keyword from  `Keywords_belgium_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_driver's_license_number" />
          <Match idRef="Keywords_belgium_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="540c7-146">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="540c7-146">Keywords</span></span>

<span data-ttu-id="540c7-147">| |</span><span class="sxs-lookup"><span data-stu-id="540c7-147"></span></span>
|<span data-ttu-id="540c7-148">**Keywords__belgium_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="540c7-148">**Keywords__belgium_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="540c7-149">distribuição</span><span class="sxs-lookup"><span data-stu-id="540c7-149">dl#</span></span>  <br/> <span data-ttu-id="540c7-150">driver license</span><span class="sxs-lookup"><span data-stu-id="540c7-150">driver license</span></span>  <br/> <span data-ttu-id="540c7-151">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-151">driver license number</span></span>  <br/> <span data-ttu-id="540c7-152">licença de driver</span><span class="sxs-lookup"><span data-stu-id="540c7-152">driver licence</span></span>  <br/> <span data-ttu-id="540c7-153">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="540c7-153">drivers lic.</span></span>  <br/> <span data-ttu-id="540c7-154">drivers license</span><span class="sxs-lookup"><span data-stu-id="540c7-154">drivers license</span></span>  <br/> <span data-ttu-id="540c7-155">drivers licence</span><span class="sxs-lookup"><span data-stu-id="540c7-155">drivers licence</span></span>  <br/> <span data-ttu-id="540c7-156">driver's license</span><span class="sxs-lookup"><span data-stu-id="540c7-156">driver's license</span></span>  <br/> <span data-ttu-id="540c7-157">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-157">driver's license number</span></span>  <br/> <span data-ttu-id="540c7-158">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="540c7-158">driver's licence number</span></span>  <br/> <span data-ttu-id="540c7-159">dlno #</span><span class="sxs-lookup"><span data-stu-id="540c7-159">dlno#</span></span>  <br/> <span data-ttu-id="540c7-160">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="540c7-160">rijbewijs</span></span>  <br/> <span data-ttu-id="540c7-161">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="540c7-161">rijbewijsnummer</span></span>  <br/> <span data-ttu-id="540c7-162">führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="540c7-162">führerscheinnummer</span></span>  <br/> <span data-ttu-id="540c7-163">fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="540c7-163">fuhrerscheinnummer</span></span>  <br/> <span data-ttu-id="540c7-164">fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="540c7-164">fuehrerscheinnummer</span></span>  <br/> <span data-ttu-id="540c7-165">führerschein-NR</span><span class="sxs-lookup"><span data-stu-id="540c7-165">führerschein- nr</span></span>  <br/> <span data-ttu-id="540c7-166">fuehrerschein-NR</span><span class="sxs-lookup"><span data-stu-id="540c7-166">fuehrerschein- Nr</span></span>  <br/> <span data-ttu-id="540c7-167">fuehrerschein-NR</span><span class="sxs-lookup"><span data-stu-id="540c7-167">fuehrerschein- nr</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="540c7-168">Bulgária</span><span class="sxs-lookup"><span data-stu-id="540c7-168">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="540c7-169">Format</span><span class="sxs-lookup"><span data-stu-id="540c7-169">Format</span></span>

<span data-ttu-id="540c7-170">Nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="540c7-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="540c7-171">Padrão</span><span class="sxs-lookup"><span data-stu-id="540c7-171">Pattern</span></span>

<span data-ttu-id="540c7-172">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="540c7-172">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="540c7-173">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="540c7-173">Checksum</span></span>

<span data-ttu-id="540c7-174">Não</span><span class="sxs-lookup"><span data-stu-id="540c7-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="540c7-175">Definição</span><span class="sxs-lookup"><span data-stu-id="540c7-175">Definition</span></span>

<span data-ttu-id="540c7-176">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="540c7-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="540c7-177">A expressão `Regex_bulgaria_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="540c7-177">The regular expression  `Regex_bulgaria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="540c7-178">Uma palavra- `Keywords_bulgaria_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="540c7-178">A keyword from  `Keywords_bulgaria_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
             <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_driver's_license_number" />
          <Match idRef="Keywords_bulgaria_eu_driver's_license_number" />
        </Pattern> 
</Entity>    

```

### <a name="keywords"></a><span data-ttu-id="540c7-179">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="540c7-179">Keywords</span></span>

<span data-ttu-id="540c7-180">| |</span><span class="sxs-lookup"><span data-stu-id="540c7-180"></span></span>
|<span data-ttu-id="540c7-181">**Keywords_bulgaria_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="540c7-181">**Keywords_bulgaria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="540c7-182">distribuição</span><span class="sxs-lookup"><span data-stu-id="540c7-182">dl#</span></span>  <br/> <span data-ttu-id="540c7-183">driver license</span><span class="sxs-lookup"><span data-stu-id="540c7-183">driver license</span></span>  <br/> <span data-ttu-id="540c7-184">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-184">driver license number</span></span>  <br/> <span data-ttu-id="540c7-185">licença de driver</span><span class="sxs-lookup"><span data-stu-id="540c7-185">driver licence</span></span>  <br/> <span data-ttu-id="540c7-186">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="540c7-186">drivers lic.</span></span>  <br/> <span data-ttu-id="540c7-187">drivers license</span><span class="sxs-lookup"><span data-stu-id="540c7-187">drivers license</span></span>  <br/> <span data-ttu-id="540c7-188">drivers licence</span><span class="sxs-lookup"><span data-stu-id="540c7-188">drivers licence</span></span>  <br/> <span data-ttu-id="540c7-189">driver's license</span><span class="sxs-lookup"><span data-stu-id="540c7-189">driver's license</span></span>  <br/> <span data-ttu-id="540c7-190">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-190">driver's license number</span></span>  <br/> <span data-ttu-id="540c7-191">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="540c7-191">driver's licence number</span></span>  <br/> <span data-ttu-id="540c7-192">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="540c7-192">driving license number</span></span>  <br/> <span data-ttu-id="540c7-193">dlno #</span><span class="sxs-lookup"><span data-stu-id="540c7-193">dlno#</span></span>  <br/> <span data-ttu-id="540c7-194">свидетелство за управление на мпс</span><span class="sxs-lookup"><span data-stu-id="540c7-194">свидетелство за управление на мпс</span></span>  <br/> <span data-ttu-id="540c7-195">свидетелство за управление на моторно превозно средство</span><span class="sxs-lookup"><span data-stu-id="540c7-195">свидетелство за управление на моторно превозно средство</span></span>  <br/> <span data-ttu-id="540c7-196">сумпс</span><span class="sxs-lookup"><span data-stu-id="540c7-196">сумпс</span></span>  <br/> <span data-ttu-id="540c7-197">шофьорска книжка</span><span class="sxs-lookup"><span data-stu-id="540c7-197">шофьорска книжка</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="540c7-198">Croácia</span><span class="sxs-lookup"><span data-stu-id="540c7-198">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="540c7-199">Format</span><span class="sxs-lookup"><span data-stu-id="540c7-199">Format</span></span>

<span data-ttu-id="540c7-200">Oito dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="540c7-200">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="540c7-201">Padrão</span><span class="sxs-lookup"><span data-stu-id="540c7-201">Pattern</span></span>

<span data-ttu-id="540c7-202">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="540c7-202">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="540c7-203">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="540c7-203">Checksum</span></span>

<span data-ttu-id="540c7-204">Não</span><span class="sxs-lookup"><span data-stu-id="540c7-204">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="540c7-205">Definição</span><span class="sxs-lookup"><span data-stu-id="540c7-205">Definition</span></span>

<span data-ttu-id="540c7-206">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="540c7-206">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="540c7-207">A expressão `Regex_croatia_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="540c7-207">The regular expression  `Regex_croatia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="540c7-208">Uma palavra- `Keywords_croatia_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="540c7-208">A keyword from  `Keywords_croatia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_driver's_license_number" />
          <Match idRef="Keywords_croatia_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="540c7-209">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="540c7-209">Keywords</span></span>

<span data-ttu-id="540c7-210">| |</span><span class="sxs-lookup"><span data-stu-id="540c7-210"></span></span>
|<span data-ttu-id="540c7-211">**Keywords_croatia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="540c7-211">**Keywords_croatia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="540c7-212">distribuição</span><span class="sxs-lookup"><span data-stu-id="540c7-212">dl#</span></span>  <br/> <span data-ttu-id="540c7-213">driver license</span><span class="sxs-lookup"><span data-stu-id="540c7-213">driver license</span></span>  <br/> <span data-ttu-id="540c7-214">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-214">driver license number</span></span>  <br/> <span data-ttu-id="540c7-215">licença de driver</span><span class="sxs-lookup"><span data-stu-id="540c7-215">driver licence</span></span>  <br/> <span data-ttu-id="540c7-216">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="540c7-216">drivers lic.</span></span>  <br/> <span data-ttu-id="540c7-217">drivers license</span><span class="sxs-lookup"><span data-stu-id="540c7-217">drivers license</span></span>  <br/> <span data-ttu-id="540c7-218">drivers licence</span><span class="sxs-lookup"><span data-stu-id="540c7-218">drivers licence</span></span>  <br/> <span data-ttu-id="540c7-219">driver's license</span><span class="sxs-lookup"><span data-stu-id="540c7-219">driver's license</span></span>  <br/> <span data-ttu-id="540c7-220">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-220">driver's license number</span></span>  <br/> <span data-ttu-id="540c7-221">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="540c7-221">driver's licence number</span></span>  <br/> <span data-ttu-id="540c7-222">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="540c7-222">driving license number</span></span>  <br/> <span data-ttu-id="540c7-223">dlno #</span><span class="sxs-lookup"><span data-stu-id="540c7-223">dlno#</span></span>  <br/> <span data-ttu-id="540c7-224">vozačka dozvola</span><span class="sxs-lookup"><span data-stu-id="540c7-224">vozačka dozvola</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="540c7-225">Chipre</span><span class="sxs-lookup"><span data-stu-id="540c7-225">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="540c7-226">Format</span><span class="sxs-lookup"><span data-stu-id="540c7-226">Format</span></span>

<span data-ttu-id="540c7-227">12 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="540c7-227">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="540c7-228">Padrão</span><span class="sxs-lookup"><span data-stu-id="540c7-228">Pattern</span></span>

<span data-ttu-id="540c7-229">12 dígitos</span><span class="sxs-lookup"><span data-stu-id="540c7-229">12 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="540c7-230">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="540c7-230">Checksum</span></span>

<span data-ttu-id="540c7-231">Não</span><span class="sxs-lookup"><span data-stu-id="540c7-231">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="540c7-232">Definição</span><span class="sxs-lookup"><span data-stu-id="540c7-232">Definition</span></span>

<span data-ttu-id="540c7-233">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="540c7-233">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="540c7-234">A expressão `Regex_cyprus_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="540c7-234">The regular expression  `Regex_cyprus_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="540c7-235">Uma palavra- `Keywords_cyprus_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="540c7-235">A keyword from  `Keywords_cyprus_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_driver's_license_number" />
          <Match idRef="Keywords_cyprus_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="540c7-236">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="540c7-236">Keywords</span></span>

<span data-ttu-id="540c7-237">| |</span><span class="sxs-lookup"><span data-stu-id="540c7-237"></span></span>
|<span data-ttu-id="540c7-238">**Keywords_cyprus_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="540c7-238">**Keywords_cyprus_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="540c7-239">distribuição</span><span class="sxs-lookup"><span data-stu-id="540c7-239">dl#</span></span>  <br/> <span data-ttu-id="540c7-240">driver license</span><span class="sxs-lookup"><span data-stu-id="540c7-240">driver license</span></span>  <br/> <span data-ttu-id="540c7-241">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-241">driver license number</span></span>  <br/> <span data-ttu-id="540c7-242">licença de driver</span><span class="sxs-lookup"><span data-stu-id="540c7-242">driver licence</span></span>  <br/> <span data-ttu-id="540c7-243">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="540c7-243">drivers lic.</span></span>  <br/> <span data-ttu-id="540c7-244">drivers license</span><span class="sxs-lookup"><span data-stu-id="540c7-244">drivers license</span></span>  <br/> <span data-ttu-id="540c7-245">drivers licence</span><span class="sxs-lookup"><span data-stu-id="540c7-245">drivers licence</span></span>  <br/> <span data-ttu-id="540c7-246">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-246">driver's license number</span></span>  <br/> <span data-ttu-id="540c7-247">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="540c7-247">driver's licence number</span></span>  <br/> <span data-ttu-id="540c7-248">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="540c7-248">driving license number</span></span>  <br/> <span data-ttu-id="540c7-249">dlno #</span><span class="sxs-lookup"><span data-stu-id="540c7-249">dlno#</span></span>  <br/> <span data-ttu-id="540c7-250">άδεια οδήγησης</span><span class="sxs-lookup"><span data-stu-id="540c7-250">άδεια οδήγησης</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="540c7-251">República Tcheca</span><span class="sxs-lookup"><span data-stu-id="540c7-251">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="540c7-252">Format</span><span class="sxs-lookup"><span data-stu-id="540c7-252">Format</span></span>

<span data-ttu-id="540c7-253">Duas letras seguidas por seis dígitos</span><span class="sxs-lookup"><span data-stu-id="540c7-253">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="540c7-254">Padrão</span><span class="sxs-lookup"><span data-stu-id="540c7-254">Pattern</span></span>

<span data-ttu-id="540c7-255">Oito letras e dígitos:</span><span class="sxs-lookup"><span data-stu-id="540c7-255">Eight letters and digits:</span></span>
  
- <span data-ttu-id="540c7-256">Duas letras (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="540c7-256">Two letters (not case-sensitive)</span></span>
    
- <span data-ttu-id="540c7-257">Um espaço (opcional)</span><span class="sxs-lookup"><span data-stu-id="540c7-257">A space (optional)</span></span>
    
- <span data-ttu-id="540c7-258">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="540c7-258">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="540c7-259">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="540c7-259">Checksum</span></span>

<span data-ttu-id="540c7-260">Não</span><span class="sxs-lookup"><span data-stu-id="540c7-260">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="540c7-261">Definição</span><span class="sxs-lookup"><span data-stu-id="540c7-261">Definition</span></span>

<span data-ttu-id="540c7-262">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="540c7-262">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="540c7-263">A expressão `Regex_czech_republic_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="540c7-263">The regular expression  `Regex_czech_republic_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="540c7-264">Uma palavra- `Keywords_czech_republic_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="540c7-264">A keyword from  `Keywords_czech_republic_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_driver's_license_number" />
          <Match idRef="Keywords_czech_republic_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="540c7-265">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="540c7-265">Keywords</span></span>

<span data-ttu-id="540c7-266">| |</span><span class="sxs-lookup"><span data-stu-id="540c7-266"></span></span>
|<span data-ttu-id="540c7-267">**Keywords_czech_republic_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="540c7-267">**Keywords_czech_republic_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="540c7-268">distribuição</span><span class="sxs-lookup"><span data-stu-id="540c7-268">dl#</span></span>  <br/> <span data-ttu-id="540c7-269">driver license</span><span class="sxs-lookup"><span data-stu-id="540c7-269">driver license</span></span>  <br/> <span data-ttu-id="540c7-270">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-270">driver license number</span></span>  <br/> <span data-ttu-id="540c7-271">licença de driver</span><span class="sxs-lookup"><span data-stu-id="540c7-271">driver licence</span></span>  <br/> <span data-ttu-id="540c7-272">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="540c7-272">drivers lic.</span></span>  <br/> <span data-ttu-id="540c7-273">drivers license</span><span class="sxs-lookup"><span data-stu-id="540c7-273">drivers license</span></span>  <br/> <span data-ttu-id="540c7-274">drivers licence</span><span class="sxs-lookup"><span data-stu-id="540c7-274">drivers licence</span></span>  <br/> <span data-ttu-id="540c7-275">driver's license</span><span class="sxs-lookup"><span data-stu-id="540c7-275">driver's license</span></span>  <br/> <span data-ttu-id="540c7-276">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-276">driver's license number</span></span>  <br/> <span data-ttu-id="540c7-277">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-277">driver's license number</span></span>  <br/> <span data-ttu-id="540c7-278">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="540c7-278">driver's licence number</span></span>  <br/> <span data-ttu-id="540c7-279">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="540c7-279">driving license number</span></span>  <br/> <span data-ttu-id="540c7-280">dlno #</span><span class="sxs-lookup"><span data-stu-id="540c7-280">dlno#</span></span>  <br/> <span data-ttu-id="540c7-281">řidičský prúkaz</span><span class="sxs-lookup"><span data-stu-id="540c7-281">řidičský prúkaz</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="540c7-282">Dinamarca</span><span class="sxs-lookup"><span data-stu-id="540c7-282">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="540c7-283">Format</span><span class="sxs-lookup"><span data-stu-id="540c7-283">Format</span></span>

<span data-ttu-id="540c7-284">Oito dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="540c7-284">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="540c7-285">Padrão</span><span class="sxs-lookup"><span data-stu-id="540c7-285">Pattern</span></span>

<span data-ttu-id="540c7-286">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="540c7-286">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="540c7-287">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="540c7-287">Checksum</span></span>

<span data-ttu-id="540c7-288">Sim</span><span class="sxs-lookup"><span data-stu-id="540c7-288">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="540c7-289">Definição</span><span class="sxs-lookup"><span data-stu-id="540c7-289">Definition</span></span>

<span data-ttu-id="540c7-290">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="540c7-290">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="540c7-291">A expressão `Regex_denmark_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="540c7-291">The regular expression  `Regex_denmark_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="540c7-292">Uma palavra- `Keywords_denmark_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="540c7-292">A keyword from  `Keywords_denmark_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_driver's_license_number" />
          <Match idRef="Keywords_denmark_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="540c7-293">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="540c7-293">Keywords</span></span>

<span data-ttu-id="540c7-294">| |</span><span class="sxs-lookup"><span data-stu-id="540c7-294"></span></span>
|<span data-ttu-id="540c7-295">**Keywords_denmark_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="540c7-295">**Keywords_denmark_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="540c7-296">distribuição</span><span class="sxs-lookup"><span data-stu-id="540c7-296">dl#</span></span>  <br/> <span data-ttu-id="540c7-297">driver license</span><span class="sxs-lookup"><span data-stu-id="540c7-297">driver license</span></span>  <br/> <span data-ttu-id="540c7-298">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-298">driver license number</span></span>  <br/> <span data-ttu-id="540c7-299">licença de driver</span><span class="sxs-lookup"><span data-stu-id="540c7-299">driver licence</span></span>  <br/> <span data-ttu-id="540c7-300">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="540c7-300">drivers lic.</span></span>  <br/> <span data-ttu-id="540c7-301">drivers license</span><span class="sxs-lookup"><span data-stu-id="540c7-301">drivers license</span></span>  <br/> <span data-ttu-id="540c7-302">drivers licence</span><span class="sxs-lookup"><span data-stu-id="540c7-302">drivers licence</span></span>  <br/> <span data-ttu-id="540c7-303">driver's license</span><span class="sxs-lookup"><span data-stu-id="540c7-303">driver's license</span></span>  <br/> <span data-ttu-id="540c7-304">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-304">driver's license number</span></span>  <br/> <span data-ttu-id="540c7-305">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="540c7-305">driver's licence number</span></span>  <br/> <span data-ttu-id="540c7-306">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="540c7-306">driving license number</span></span>  <br/> <span data-ttu-id="540c7-307">dlno #</span><span class="sxs-lookup"><span data-stu-id="540c7-307">dlno#</span></span>  <br/> <span data-ttu-id="540c7-308">kørekort</span><span class="sxs-lookup"><span data-stu-id="540c7-308">kørekort</span></span>  <br/> <span data-ttu-id="540c7-309">kørekortnummer</span><span class="sxs-lookup"><span data-stu-id="540c7-309">kørekortnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="540c7-310">Estônia</span><span class="sxs-lookup"><span data-stu-id="540c7-310">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="540c7-311">Format</span><span class="sxs-lookup"><span data-stu-id="540c7-311">Format</span></span>

<span data-ttu-id="540c7-312">Duas letras seguidas por seis dígitos</span><span class="sxs-lookup"><span data-stu-id="540c7-312">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="540c7-313">Padrão</span><span class="sxs-lookup"><span data-stu-id="540c7-313">Pattern</span></span>

<span data-ttu-id="540c7-314">Duas letras e seis dígitos:</span><span class="sxs-lookup"><span data-stu-id="540c7-314">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="540c7-315">As letras "ET" (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="540c7-315">The letters "ET" (not case-sensitive)</span></span> 
    
- <span data-ttu-id="540c7-316">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="540c7-316">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="540c7-317">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="540c7-317">Checksum</span></span>

<span data-ttu-id="540c7-318">Não</span><span class="sxs-lookup"><span data-stu-id="540c7-318">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="540c7-319">Definição</span><span class="sxs-lookup"><span data-stu-id="540c7-319">Definition</span></span>

<span data-ttu-id="540c7-320">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="540c7-320">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="540c7-321">A expressão `Regex_estonia_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="540c7-321">The regular expression  `Regex_estonia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="540c7-322">Uma palavra- `Keywords_estonia_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="540c7-322">A keyword from  `Keywords_estonia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_driver's_license_number" />
          <Match idRef="Keywords_estonia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="540c7-323">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="540c7-323">Keywords</span></span>

<span data-ttu-id="540c7-324">| |</span><span class="sxs-lookup"><span data-stu-id="540c7-324"></span></span>
|<span data-ttu-id="540c7-325">**Keywords_estonia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="540c7-325">**Keywords_estonia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="540c7-326">distribuição</span><span class="sxs-lookup"><span data-stu-id="540c7-326">dl#</span></span>  <br/> <span data-ttu-id="540c7-327">driver license</span><span class="sxs-lookup"><span data-stu-id="540c7-327">driver license</span></span>  <br/> <span data-ttu-id="540c7-328">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-328">driver license number</span></span>  <br/> <span data-ttu-id="540c7-329">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-329">driver license number</span></span>  <br/> <span data-ttu-id="540c7-330">licença de driver</span><span class="sxs-lookup"><span data-stu-id="540c7-330">driver licence</span></span>  <br/> <span data-ttu-id="540c7-331">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="540c7-331">drivers lic.</span></span>  <br/> <span data-ttu-id="540c7-332">drivers license</span><span class="sxs-lookup"><span data-stu-id="540c7-332">drivers license</span></span>  <br/> <span data-ttu-id="540c7-333">drivers licence</span><span class="sxs-lookup"><span data-stu-id="540c7-333">drivers licence</span></span>  <br/> <span data-ttu-id="540c7-334">driver's license</span><span class="sxs-lookup"><span data-stu-id="540c7-334">driver's license</span></span>  <br/> <span data-ttu-id="540c7-335">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-335">driver's license number</span></span>  <br/> <span data-ttu-id="540c7-336">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="540c7-336">driving license number</span></span>  <br/> <span data-ttu-id="540c7-337">dlno #</span><span class="sxs-lookup"><span data-stu-id="540c7-337">dlno#</span></span>  <br/> <span data-ttu-id="540c7-338">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="540c7-338">permis de conduire</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="540c7-339">Finlândia</span><span class="sxs-lookup"><span data-stu-id="540c7-339">Finland</span></span>

### <a name="format"></a><span data-ttu-id="540c7-340">Format</span><span class="sxs-lookup"><span data-stu-id="540c7-340">Format</span></span>

<span data-ttu-id="540c7-341">10 dígitos que contêm um hífen</span><span class="sxs-lookup"><span data-stu-id="540c7-341">10 digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="540c7-342">Padrão</span><span class="sxs-lookup"><span data-stu-id="540c7-342">Pattern</span></span>

<span data-ttu-id="540c7-343">10 dígitos contendo um hífen:</span><span class="sxs-lookup"><span data-stu-id="540c7-343">10 digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="540c7-344">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="540c7-344">Six digits</span></span> 
    
- <span data-ttu-id="540c7-345">Um hífen</span><span class="sxs-lookup"><span data-stu-id="540c7-345">A hyphen</span></span>
    
-  <span data-ttu-id="540c7-346">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="540c7-346">Four digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="540c7-347">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="540c7-347">Checksum</span></span>

<span data-ttu-id="540c7-348">Não</span><span class="sxs-lookup"><span data-stu-id="540c7-348">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="540c7-349">Definição</span><span class="sxs-lookup"><span data-stu-id="540c7-349">Definition</span></span>

<span data-ttu-id="540c7-350">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="540c7-350">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="540c7-351">A expressão `Regex_finland_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="540c7-351">The regular expression  `Regex_finland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="540c7-352">Uma palavra- `Keywords_finland_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="540c7-352">A keyword from  `Keywords_finland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_driver's_license_number" />
          <Match idRef="Keywords_finland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="540c7-353">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="540c7-353">Keywords</span></span>

<span data-ttu-id="540c7-354">| |</span><span class="sxs-lookup"><span data-stu-id="540c7-354"></span></span>
|<span data-ttu-id="540c7-355">**Keywords_finland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="540c7-355">**Keywords_finland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="540c7-356">distribuição</span><span class="sxs-lookup"><span data-stu-id="540c7-356">dl#</span></span>  <br/> <span data-ttu-id="540c7-357">driver license</span><span class="sxs-lookup"><span data-stu-id="540c7-357">driver license</span></span>  <br/> <span data-ttu-id="540c7-358">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-358">driver license number</span></span>  <br/> <span data-ttu-id="540c7-359">licença de driver</span><span class="sxs-lookup"><span data-stu-id="540c7-359">driver licence</span></span>  <br/> <span data-ttu-id="540c7-360">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="540c7-360">drivers lic.</span></span>  <br/> <span data-ttu-id="540c7-361">drivers license</span><span class="sxs-lookup"><span data-stu-id="540c7-361">drivers license</span></span>  <br/> <span data-ttu-id="540c7-362">drivers licence</span><span class="sxs-lookup"><span data-stu-id="540c7-362">drivers licence</span></span>  <br/> <span data-ttu-id="540c7-363">driver's license</span><span class="sxs-lookup"><span data-stu-id="540c7-363">driver's license</span></span>  <br/> <span data-ttu-id="540c7-364">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-364">driver's license number</span></span>  <br/> <span data-ttu-id="540c7-365">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="540c7-365">driver's licence number</span></span>  <br/> <span data-ttu-id="540c7-366">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="540c7-366">driving license number</span></span>  <br/> <span data-ttu-id="540c7-367">dlno #</span><span class="sxs-lookup"><span data-stu-id="540c7-367">dlno#</span></span>  <br/> <span data-ttu-id="540c7-368">ajokortti</span><span class="sxs-lookup"><span data-stu-id="540c7-368">ajokortti</span></span>  <br/> |
   
## <a name="france"></a><span data-ttu-id="540c7-369">França</span><span class="sxs-lookup"><span data-stu-id="540c7-369">France</span></span>

<span data-ttu-id="540c7-370">Para obter detalhes, consulte a seção "número da carteira de motorista do driver da França" em [o que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="540c7-370">For details, see the section "France Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="540c7-371">Alemanha</span><span class="sxs-lookup"><span data-stu-id="540c7-371">Germany</span></span>

<span data-ttu-id="540c7-372">Para obter detalhes, consulte a seção "número da carteira de motorista do driver alemão" em [o que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="540c7-372">For details, see the section "German Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="540c7-373">Grécia</span><span class="sxs-lookup"><span data-stu-id="540c7-373">Greece</span></span>

### <a name="format"></a><span data-ttu-id="540c7-374">Format</span><span class="sxs-lookup"><span data-stu-id="540c7-374">Format</span></span>

<span data-ttu-id="540c7-375">Nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="540c7-375">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="540c7-376">Padrão</span><span class="sxs-lookup"><span data-stu-id="540c7-376">Pattern</span></span>

 <span data-ttu-id="540c7-377">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="540c7-377">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="540c7-378">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="540c7-378">Checksum</span></span>

<span data-ttu-id="540c7-379">Não</span><span class="sxs-lookup"><span data-stu-id="540c7-379">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="540c7-380">Definição</span><span class="sxs-lookup"><span data-stu-id="540c7-380">Definition</span></span>

<span data-ttu-id="540c7-381">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="540c7-381">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="540c7-382">A expressão `Regex_greece_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="540c7-382">The regular expression  `Regex_greece_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="540c7-383">Uma palavra- `Keywords_greece_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="540c7-383">A keyword from  `Keywords_greece_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_driver's_license_number" />
          <Match idRef="Keywords_greece_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="540c7-384">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="540c7-384">Keywords</span></span>

<span data-ttu-id="540c7-385">| |</span><span class="sxs-lookup"><span data-stu-id="540c7-385"></span></span>
|<span data-ttu-id="540c7-386">**Keywords_greece_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="540c7-386">**Keywords_greece_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="540c7-387">DlL</span><span class="sxs-lookup"><span data-stu-id="540c7-387">dlL#</span></span>  <br/> <span data-ttu-id="540c7-388">driver license</span><span class="sxs-lookup"><span data-stu-id="540c7-388">driver license</span></span>  <br/> <span data-ttu-id="540c7-389">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-389">driver license number</span></span>  <br/> <span data-ttu-id="540c7-390">licença de driver</span><span class="sxs-lookup"><span data-stu-id="540c7-390">driver licence</span></span>  <br/> <span data-ttu-id="540c7-391">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="540c7-391">drivers lic.</span></span>  <br/> <span data-ttu-id="540c7-392">drivers license</span><span class="sxs-lookup"><span data-stu-id="540c7-392">drivers license</span></span>  <br/> <span data-ttu-id="540c7-393">drivers licence</span><span class="sxs-lookup"><span data-stu-id="540c7-393">drivers licence</span></span>  <br/> <span data-ttu-id="540c7-394">driver's license</span><span class="sxs-lookup"><span data-stu-id="540c7-394">driver's license</span></span>  <br/> <span data-ttu-id="540c7-395">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-395">driver's license number</span></span>  <br/> <span data-ttu-id="540c7-396">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="540c7-396">driver's licence number</span></span>  <br/> <span data-ttu-id="540c7-397">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="540c7-397">driving license number</span></span>  <br/> <span data-ttu-id="540c7-398">dlno #</span><span class="sxs-lookup"><span data-stu-id="540c7-398">dlno#</span></span>  <br/> <span data-ttu-id="540c7-399">δεια οδήγησης</span><span class="sxs-lookup"><span data-stu-id="540c7-399">δεια οδήγησης</span></span>  <br/> <span data-ttu-id="540c7-400">AdeIa odigisis</span><span class="sxs-lookup"><span data-stu-id="540c7-400">Adeia odigisis</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="540c7-401">Hungria</span><span class="sxs-lookup"><span data-stu-id="540c7-401">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="540c7-402">Format</span><span class="sxs-lookup"><span data-stu-id="540c7-402">Format</span></span>

<span data-ttu-id="540c7-403">Duas letras seguidas por seis dígitos</span><span class="sxs-lookup"><span data-stu-id="540c7-403">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="540c7-404">Padrão</span><span class="sxs-lookup"><span data-stu-id="540c7-404">Pattern</span></span>

<span data-ttu-id="540c7-405">Duas letras e seis dígitos:</span><span class="sxs-lookup"><span data-stu-id="540c7-405">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="540c7-406">Duas letras (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="540c7-406">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="540c7-407">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="540c7-407">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="540c7-408">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="540c7-408">Checksum</span></span>

<span data-ttu-id="540c7-409">Não</span><span class="sxs-lookup"><span data-stu-id="540c7-409">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="540c7-410">Definição</span><span class="sxs-lookup"><span data-stu-id="540c7-410">Definition</span></span>

<span data-ttu-id="540c7-411">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="540c7-411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="540c7-412">A expressão `Regex_hungary_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="540c7-412">The regular expression  `Regex_hungary_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="540c7-413">Uma palavra- `Keywords_hungary_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="540c7-413">A keyword from  `Keywords_hungary_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_driver's_license_number" />
          <Match idRef="Keywords_hungary_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="540c7-414">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="540c7-414">Keywords</span></span>

<span data-ttu-id="540c7-415">| |</span><span class="sxs-lookup"><span data-stu-id="540c7-415"></span></span>
|<span data-ttu-id="540c7-416">**Keywords_hungary_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="540c7-416">**Keywords_hungary_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="540c7-417">distribuição</span><span class="sxs-lookup"><span data-stu-id="540c7-417">dl#</span></span>  <br/> <span data-ttu-id="540c7-418">driver license</span><span class="sxs-lookup"><span data-stu-id="540c7-418">driver license</span></span>  <br/> <span data-ttu-id="540c7-419">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-419">driver license number</span></span>  <br/> <span data-ttu-id="540c7-420">licença de driver</span><span class="sxs-lookup"><span data-stu-id="540c7-420">driver licence</span></span>  <br/> <span data-ttu-id="540c7-421">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="540c7-421">drivers lic.</span></span>  <br/> <span data-ttu-id="540c7-422">drivers license</span><span class="sxs-lookup"><span data-stu-id="540c7-422">drivers license</span></span>  <br/> <span data-ttu-id="540c7-423">drivers licence</span><span class="sxs-lookup"><span data-stu-id="540c7-423">drivers licence</span></span>  <br/> <span data-ttu-id="540c7-424">driver's license</span><span class="sxs-lookup"><span data-stu-id="540c7-424">driver's license</span></span>  <br/> <span data-ttu-id="540c7-425">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-425">driver's license number</span></span>  <br/> <span data-ttu-id="540c7-426">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="540c7-426">driver's licence number</span></span>  <br/> <span data-ttu-id="540c7-427">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="540c7-427">driving license number</span></span>  <br/> <span data-ttu-id="540c7-428">dlno #</span><span class="sxs-lookup"><span data-stu-id="540c7-428">dlno#</span></span>  <br/> <span data-ttu-id="540c7-429">vezetoi engedely</span><span class="sxs-lookup"><span data-stu-id="540c7-429">vezetoi engedely</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="540c7-430">Irlanda</span><span class="sxs-lookup"><span data-stu-id="540c7-430">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="540c7-431">Format</span><span class="sxs-lookup"><span data-stu-id="540c7-431">Format</span></span>

<span data-ttu-id="540c7-432">Seis dígitos seguidos de quatro letras</span><span class="sxs-lookup"><span data-stu-id="540c7-432">Six digits followed by four letters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="540c7-433">Padrão</span><span class="sxs-lookup"><span data-stu-id="540c7-433">Pattern</span></span>

<span data-ttu-id="540c7-434">Seis dígitos e quatro letras:</span><span class="sxs-lookup"><span data-stu-id="540c7-434">Six digits and four letters:</span></span>
  
- <span data-ttu-id="540c7-435">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="540c7-435">Six digits</span></span>
    
- <span data-ttu-id="540c7-436">Quatro letras (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="540c7-436">Four letters (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="540c7-437">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="540c7-437">Checksum</span></span>

<span data-ttu-id="540c7-438">Não</span><span class="sxs-lookup"><span data-stu-id="540c7-438">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="540c7-439">Definição</span><span class="sxs-lookup"><span data-stu-id="540c7-439">Definition</span></span>

<span data-ttu-id="540c7-440">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="540c7-440">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="540c7-441">A expressão `Regex_ireland_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="540c7-441">The regular expression  `Regex_ireland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="540c7-442">Uma palavra- `Keywords_ireland_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="540c7-442">A keyword from  `Keywords_ireland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_driver's_license_number" />
          <Match idRef="Keywords_ireland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="540c7-443">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="540c7-443">Keywords</span></span>

<span data-ttu-id="540c7-444">| |</span><span class="sxs-lookup"><span data-stu-id="540c7-444"></span></span>
|<span data-ttu-id="540c7-445">**Keywords_ireland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="540c7-445">**Keywords_ireland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="540c7-446">distribuição</span><span class="sxs-lookup"><span data-stu-id="540c7-446">dl#</span></span>  <br/> <span data-ttu-id="540c7-447">driver license</span><span class="sxs-lookup"><span data-stu-id="540c7-447">driver license</span></span>  <br/> <span data-ttu-id="540c7-448">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-448">driver license number</span></span>  <br/> <span data-ttu-id="540c7-449">licença de driver</span><span class="sxs-lookup"><span data-stu-id="540c7-449">driver licence</span></span>  <br/> <span data-ttu-id="540c7-450">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="540c7-450">drivers lic.</span></span>  <br/> <span data-ttu-id="540c7-451">drivers license</span><span class="sxs-lookup"><span data-stu-id="540c7-451">drivers license</span></span>  <br/> <span data-ttu-id="540c7-452">drivers licence</span><span class="sxs-lookup"><span data-stu-id="540c7-452">drivers licence</span></span>  <br/> <span data-ttu-id="540c7-453">driver's license</span><span class="sxs-lookup"><span data-stu-id="540c7-453">driver's license</span></span>  <br/> <span data-ttu-id="540c7-454">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-454">driver's license number</span></span>  <br/> <span data-ttu-id="540c7-455">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="540c7-455">driver's licence number</span></span>  <br/> <span data-ttu-id="540c7-456">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="540c7-456">driving license number</span></span>  <br/> <span data-ttu-id="540c7-457">dlno #</span><span class="sxs-lookup"><span data-stu-id="540c7-457">dlno#</span></span>  <br/> <span data-ttu-id="540c7-458">ceadúnas tiomána</span><span class="sxs-lookup"><span data-stu-id="540c7-458">ceadúnas tiomána</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="540c7-459">Itália</span><span class="sxs-lookup"><span data-stu-id="540c7-459">Italy</span></span>

<span data-ttu-id="540c7-460">Para obter detalhes, consulte a seção "número da carteira de motorista do driver da Itália" em [o que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="540c7-460">For details, see the section "Italy Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="latvia"></a><span data-ttu-id="540c7-461">Letônia</span><span class="sxs-lookup"><span data-stu-id="540c7-461">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="540c7-462">Format</span><span class="sxs-lookup"><span data-stu-id="540c7-462">Format</span></span>

<span data-ttu-id="540c7-463">Três letras seguidas por seis dígitos</span><span class="sxs-lookup"><span data-stu-id="540c7-463">Three letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="540c7-464">Padrão</span><span class="sxs-lookup"><span data-stu-id="540c7-464">Pattern</span></span>

<span data-ttu-id="540c7-465">Três letras e seis dígitos:</span><span class="sxs-lookup"><span data-stu-id="540c7-465">Three letters and six digits:</span></span>
  
-  <span data-ttu-id="540c7-466">Três letras (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="540c7-466">Three letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="540c7-467">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="540c7-467">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="540c7-468">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="540c7-468">Checksum</span></span>

<span data-ttu-id="540c7-469">Não</span><span class="sxs-lookup"><span data-stu-id="540c7-469">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="540c7-470">Definição</span><span class="sxs-lookup"><span data-stu-id="540c7-470">Definition</span></span>

<span data-ttu-id="540c7-471">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="540c7-471">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="540c7-472">A expressão `Regex_latvia_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="540c7-472">The regular expression  `Regex_latvia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="540c7-473">Uma palavra- `Keywords_latvia_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="540c7-473">A keyword from  `Keywords_latvia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_driver's_license_number" />
          <Match idRef="Keywords_latvia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="540c7-474">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="540c7-474">Keywords</span></span>

<span data-ttu-id="540c7-475">| |</span><span class="sxs-lookup"><span data-stu-id="540c7-475"></span></span>
|<span data-ttu-id="540c7-476">**Keywords_latvia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="540c7-476">**Keywords_latvia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="540c7-477">distribuição</span><span class="sxs-lookup"><span data-stu-id="540c7-477">dl#</span></span>  <br/> <span data-ttu-id="540c7-478">driver license</span><span class="sxs-lookup"><span data-stu-id="540c7-478">driver license</span></span>  <br/> <span data-ttu-id="540c7-479">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-479">driver license number</span></span>  <br/> <span data-ttu-id="540c7-480">licença de driver</span><span class="sxs-lookup"><span data-stu-id="540c7-480">driver licence</span></span>  <br/> <span data-ttu-id="540c7-481">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="540c7-481">drivers lic.</span></span>  <br/> <span data-ttu-id="540c7-482">drivers license</span><span class="sxs-lookup"><span data-stu-id="540c7-482">drivers license</span></span>  <br/> <span data-ttu-id="540c7-483">drivers licence</span><span class="sxs-lookup"><span data-stu-id="540c7-483">drivers licence</span></span>  <br/> <span data-ttu-id="540c7-484">driver's license</span><span class="sxs-lookup"><span data-stu-id="540c7-484">driver's license</span></span>  <br/> <span data-ttu-id="540c7-485">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-485">driver's license number</span></span>  <br/> <span data-ttu-id="540c7-486">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="540c7-486">driver's licence number</span></span>  <br/> <span data-ttu-id="540c7-487">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="540c7-487">driving license number</span></span>  <br/> <span data-ttu-id="540c7-488">dlno #</span><span class="sxs-lookup"><span data-stu-id="540c7-488">dlno#</span></span>  <br/> <span data-ttu-id="540c7-489">autovadītāja apliecība</span><span class="sxs-lookup"><span data-stu-id="540c7-489">autovadītāja apliecība</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="540c7-490">Lituânia</span><span class="sxs-lookup"><span data-stu-id="540c7-490">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="540c7-491">Format</span><span class="sxs-lookup"><span data-stu-id="540c7-491">Format</span></span>

<span data-ttu-id="540c7-492">Oito dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="540c7-492">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="540c7-493">Padrão</span><span class="sxs-lookup"><span data-stu-id="540c7-493">Pattern</span></span>

 <span data-ttu-id="540c7-494">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="540c7-494">Eight digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="540c7-495">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="540c7-495">Checksum</span></span>

<span data-ttu-id="540c7-496">Não</span><span class="sxs-lookup"><span data-stu-id="540c7-496">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="540c7-497">Definição</span><span class="sxs-lookup"><span data-stu-id="540c7-497">Definition</span></span>

<span data-ttu-id="540c7-498">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="540c7-498">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="540c7-499">A expressão `Regex_lithuania_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="540c7-499">The regular expression  `Regex_lithuania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="540c7-500">Uma palavra- `Keywords_lithuania_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="540c7-500">A keyword from  `Keywords_lithuania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_driver's_license_number" />
          <Match idRef="Keywords_lithuania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="540c7-501">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="540c7-501">Keywords</span></span>

<span data-ttu-id="540c7-502">| |</span><span class="sxs-lookup"><span data-stu-id="540c7-502"></span></span>
|<span data-ttu-id="540c7-503">**Keywords_lithuania_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="540c7-503">**Keywords_lithuania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="540c7-504">distribuição</span><span class="sxs-lookup"><span data-stu-id="540c7-504">dl#</span></span>  <br/> <span data-ttu-id="540c7-505">driver license</span><span class="sxs-lookup"><span data-stu-id="540c7-505">driver license</span></span>  <br/> <span data-ttu-id="540c7-506">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-506">driver license number</span></span>  <br/> <span data-ttu-id="540c7-507">licença de driver</span><span class="sxs-lookup"><span data-stu-id="540c7-507">driver licence</span></span>  <br/> <span data-ttu-id="540c7-508">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="540c7-508">drivers lic.</span></span>  <br/> <span data-ttu-id="540c7-509">drivers license</span><span class="sxs-lookup"><span data-stu-id="540c7-509">drivers license</span></span>  <br/> <span data-ttu-id="540c7-510">drivers licence</span><span class="sxs-lookup"><span data-stu-id="540c7-510">drivers licence</span></span>  <br/> <span data-ttu-id="540c7-511">driver's license</span><span class="sxs-lookup"><span data-stu-id="540c7-511">driver's license</span></span>  <br/> <span data-ttu-id="540c7-512">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-512">driver's license number</span></span>  <br/> <span data-ttu-id="540c7-513">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="540c7-513">driver's licence number</span></span>  <br/> <span data-ttu-id="540c7-514">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="540c7-514">driving license number</span></span>  <br/> <span data-ttu-id="540c7-515">dlno #</span><span class="sxs-lookup"><span data-stu-id="540c7-515">dlno#</span></span>  <br/> <span data-ttu-id="540c7-516">vairuotojo pažymėjimas</span><span class="sxs-lookup"><span data-stu-id="540c7-516">vairuotojo pažymėjimas</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="540c7-517">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="540c7-517">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="540c7-518">Format</span><span class="sxs-lookup"><span data-stu-id="540c7-518">Format</span></span>

<span data-ttu-id="540c7-519">Seis dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="540c7-519">Six digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="540c7-520">Padrão</span><span class="sxs-lookup"><span data-stu-id="540c7-520">Pattern</span></span>

 <span data-ttu-id="540c7-521">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="540c7-521">Six digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="540c7-522">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="540c7-522">Checksum</span></span>

<span data-ttu-id="540c7-523">Não</span><span class="sxs-lookup"><span data-stu-id="540c7-523">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="540c7-524">Definição</span><span class="sxs-lookup"><span data-stu-id="540c7-524">Definition</span></span>

<span data-ttu-id="540c7-525">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="540c7-525">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="540c7-526">A expressão `Regex_luxemburg_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="540c7-526">The regular expression  `Regex_luxemburg_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="540c7-527">Uma palavra- `Keywords_luxemburg_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="540c7-527">A keyword from  `Keywords_luxemburg_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_driver's_license_number" />
          <Match idRef="Keywords_luxemburg_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="540c7-528">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="540c7-528">Keywords</span></span>

<span data-ttu-id="540c7-529">| |</span><span class="sxs-lookup"><span data-stu-id="540c7-529"></span></span>
|<span data-ttu-id="540c7-530">**Keywords_luxemburg_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="540c7-530">**Keywords_luxemburg_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="540c7-531">distribuição</span><span class="sxs-lookup"><span data-stu-id="540c7-531">dl#</span></span>  <br/> <span data-ttu-id="540c7-532">driver license</span><span class="sxs-lookup"><span data-stu-id="540c7-532">driver license</span></span>  <br/> <span data-ttu-id="540c7-533">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-533">driver license number</span></span>  <br/> <span data-ttu-id="540c7-534">licença de driver</span><span class="sxs-lookup"><span data-stu-id="540c7-534">driver licence</span></span>  <br/> <span data-ttu-id="540c7-535">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="540c7-535">drivers lic.</span></span>  <br/> <span data-ttu-id="540c7-536">drivers license</span><span class="sxs-lookup"><span data-stu-id="540c7-536">drivers license</span></span>  <br/> <span data-ttu-id="540c7-537">drivers licence</span><span class="sxs-lookup"><span data-stu-id="540c7-537">drivers licence</span></span>  <br/> <span data-ttu-id="540c7-538">driver's license</span><span class="sxs-lookup"><span data-stu-id="540c7-538">driver's license</span></span>  <br/> <span data-ttu-id="540c7-539">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-539">driver's license number</span></span>  <br/> <span data-ttu-id="540c7-540">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="540c7-540">driver's licence number</span></span>  <br/> <span data-ttu-id="540c7-541">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="540c7-541">driving license number</span></span>  <br/> <span data-ttu-id="540c7-542">dlno #</span><span class="sxs-lookup"><span data-stu-id="540c7-542">dlno#</span></span>  <br/> <span data-ttu-id="540c7-543">fahrerlaubnis</span><span class="sxs-lookup"><span data-stu-id="540c7-543">fahrerlaubnis</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="540c7-544">Malta</span><span class="sxs-lookup"><span data-stu-id="540c7-544">Malta</span></span>

### <a name="format"></a><span data-ttu-id="540c7-545">Format</span><span class="sxs-lookup"><span data-stu-id="540c7-545">Format</span></span>

<span data-ttu-id="540c7-546">Combinação de dois caracteres e seis dígitos no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="540c7-546">Combination of two characters and six digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="540c7-547">Padrão</span><span class="sxs-lookup"><span data-stu-id="540c7-547">Pattern</span></span>

<span data-ttu-id="540c7-548">Combinação de dois caracteres e seis dígitos:</span><span class="sxs-lookup"><span data-stu-id="540c7-548">Combination of two characters and six digits:</span></span>
  
- <span data-ttu-id="540c7-549">Dois caracteres (dígitos ou letras, não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="540c7-549">Two characters (digits or letters, not case-sensitive)</span></span>
    
- <span data-ttu-id="540c7-550">Um espaço (opcional)</span><span class="sxs-lookup"><span data-stu-id="540c7-550">A space (optional)</span></span>
    
- <span data-ttu-id="540c7-551">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="540c7-551">Three digits</span></span>
    
- <span data-ttu-id="540c7-552">Um espaço (opcional)</span><span class="sxs-lookup"><span data-stu-id="540c7-552">A space (optional)</span></span>
    
- <span data-ttu-id="540c7-553">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="540c7-553">Three digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="540c7-554">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="540c7-554">Checksum</span></span>

<span data-ttu-id="540c7-555">Não</span><span class="sxs-lookup"><span data-stu-id="540c7-555">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="540c7-556">Definição</span><span class="sxs-lookup"><span data-stu-id="540c7-556">Definition</span></span>

<span data-ttu-id="540c7-557">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="540c7-557">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="540c7-558">A expressão `Regex_malta_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="540c7-558">The regular expression  `Regex_malta_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="540c7-559">Uma palavra- `Keywords_malta_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="540c7-559">A keyword from  `Keywords_malta_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
 <Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_driver's_license_number" />
          <Match idRef="Keywords_malta_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="540c7-560">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="540c7-560">Keywords</span></span>

<span data-ttu-id="540c7-561">| |</span><span class="sxs-lookup"><span data-stu-id="540c7-561"></span></span>
|<span data-ttu-id="540c7-562">**Keywords_malta_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="540c7-562">**Keywords_malta_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="540c7-563">distribuição</span><span class="sxs-lookup"><span data-stu-id="540c7-563">dl#</span></span>  <br/> <span data-ttu-id="540c7-564">driver license</span><span class="sxs-lookup"><span data-stu-id="540c7-564">driver license</span></span>  <br/> <span data-ttu-id="540c7-565">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-565">driver license number</span></span>  <br/> <span data-ttu-id="540c7-566">licença de driver</span><span class="sxs-lookup"><span data-stu-id="540c7-566">driver licence</span></span>  <br/> <span data-ttu-id="540c7-567">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="540c7-567">drivers lic.</span></span>  <br/> <span data-ttu-id="540c7-568">drivers license</span><span class="sxs-lookup"><span data-stu-id="540c7-568">drivers license</span></span>  <br/> <span data-ttu-id="540c7-569">drivers licence</span><span class="sxs-lookup"><span data-stu-id="540c7-569">drivers licence</span></span>  <br/> <span data-ttu-id="540c7-570">driver's license</span><span class="sxs-lookup"><span data-stu-id="540c7-570">driver's license</span></span>  <br/> <span data-ttu-id="540c7-571">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-571">driver's license number</span></span>  <br/> <span data-ttu-id="540c7-572">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="540c7-572">driver's licence number</span></span>  <br/> <span data-ttu-id="540c7-573">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="540c7-573">driving license number</span></span>  <br/> <span data-ttu-id="540c7-574">dlno #</span><span class="sxs-lookup"><span data-stu-id="540c7-574">dlno#</span></span>  <br/> <span data-ttu-id="540c7-575">liċenzja tas-sewqan</span><span class="sxs-lookup"><span data-stu-id="540c7-575">liċenzja tas-sewqan</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="540c7-576">Países Baixos</span><span class="sxs-lookup"><span data-stu-id="540c7-576">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="540c7-577">Format</span><span class="sxs-lookup"><span data-stu-id="540c7-577">Format</span></span>

<span data-ttu-id="540c7-578">10 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="540c7-578">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="540c7-579">Padrão</span><span class="sxs-lookup"><span data-stu-id="540c7-579">Pattern</span></span>

<span data-ttu-id="540c7-580">10 dígitos</span><span class="sxs-lookup"><span data-stu-id="540c7-580">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="540c7-581">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="540c7-581">Checksum</span></span>

<span data-ttu-id="540c7-582">Não</span><span class="sxs-lookup"><span data-stu-id="540c7-582">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="540c7-583">Definição</span><span class="sxs-lookup"><span data-stu-id="540c7-583">Definition</span></span>

<span data-ttu-id="540c7-584">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="540c7-584">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="540c7-585">A expressão `Regex_netherlands_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="540c7-585">The regular expression  `Regex_netherlands_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="540c7-586">Uma palavra- `Keywords_netherlands_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="540c7-586">A keyword from  `Keywords_netherlands_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_driver's_license_number" />
          <Match idRef="Keywords_netherlands_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="540c7-587">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="540c7-587">Keywords</span></span>

<span data-ttu-id="540c7-588">| |</span><span class="sxs-lookup"><span data-stu-id="540c7-588"></span></span>
|<span data-ttu-id="540c7-589">**Keywords_netherlands_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="540c7-589">**Keywords_netherlands_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="540c7-590">distribuição</span><span class="sxs-lookup"><span data-stu-id="540c7-590">dl#</span></span>  <br/> <span data-ttu-id="540c7-591">driver license</span><span class="sxs-lookup"><span data-stu-id="540c7-591">driver license</span></span>  <br/> <span data-ttu-id="540c7-592">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-592">driver license number</span></span>  <br/> <span data-ttu-id="540c7-593">licença de driver</span><span class="sxs-lookup"><span data-stu-id="540c7-593">driver licence</span></span>  <br/> <span data-ttu-id="540c7-594">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="540c7-594">drivers lic.</span></span>  <br/> <span data-ttu-id="540c7-595">drivers license</span><span class="sxs-lookup"><span data-stu-id="540c7-595">drivers license</span></span>  <br/> <span data-ttu-id="540c7-596">drivers licence</span><span class="sxs-lookup"><span data-stu-id="540c7-596">drivers licence</span></span>  <br/> <span data-ttu-id="540c7-597">driver's license</span><span class="sxs-lookup"><span data-stu-id="540c7-597">driver's license</span></span>  <br/> <span data-ttu-id="540c7-598">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-598">driver's license number</span></span>  <br/> <span data-ttu-id="540c7-599">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="540c7-599">driver's licence number</span></span>  <br/> <span data-ttu-id="540c7-600">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="540c7-600">driving license number</span></span>  <br/> <span data-ttu-id="540c7-601">dlno #</span><span class="sxs-lookup"><span data-stu-id="540c7-601">dlno#</span></span>  <br/> <span data-ttu-id="540c7-602">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="540c7-602">permis de conduire</span></span>  <br/> <span data-ttu-id="540c7-603">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="540c7-603">rijbewijs</span></span>  <br/> <span data-ttu-id="540c7-604">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="540c7-604">rijbewijsnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="540c7-605">Polônia</span><span class="sxs-lookup"><span data-stu-id="540c7-605">Poland</span></span>

### <a name="format"></a><span data-ttu-id="540c7-606">Format</span><span class="sxs-lookup"><span data-stu-id="540c7-606">Format</span></span>

<span data-ttu-id="540c7-607">14 dígitos contendo 2 barras</span><span class="sxs-lookup"><span data-stu-id="540c7-607">14 digits containing 2 forward slashes</span></span>
  
### <a name="pattern"></a><span data-ttu-id="540c7-608">Padrão</span><span class="sxs-lookup"><span data-stu-id="540c7-608">Pattern</span></span>

<span data-ttu-id="540c7-609">14 dígitos e 2 barras de avanço:</span><span class="sxs-lookup"><span data-stu-id="540c7-609">14 digits and 2 forward slashes:</span></span>
  
-  <span data-ttu-id="540c7-610">Cinco dígitos</span><span class="sxs-lookup"><span data-stu-id="540c7-610">Five digits</span></span> 
    
- <span data-ttu-id="540c7-611">Uma barra</span><span class="sxs-lookup"><span data-stu-id="540c7-611">A forward slash</span></span>
    
- <span data-ttu-id="540c7-612">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="540c7-612">Two digits</span></span>
    
- <span data-ttu-id="540c7-613">Uma barra</span><span class="sxs-lookup"><span data-stu-id="540c7-613">A forward slash</span></span>
    
- <span data-ttu-id="540c7-614">Sete dígitos</span><span class="sxs-lookup"><span data-stu-id="540c7-614">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="540c7-615">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="540c7-615">Checksum</span></span>

<span data-ttu-id="540c7-616">Não</span><span class="sxs-lookup"><span data-stu-id="540c7-616">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="540c7-617">Definição</span><span class="sxs-lookup"><span data-stu-id="540c7-617">Definition</span></span>

<span data-ttu-id="540c7-618">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="540c7-618">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="540c7-619">A expressão `Regex_poland_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="540c7-619">The regular expression  `Regex_poland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="540c7-620">Uma palavra- `Keywords_poland_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="540c7-620">A keyword from  `Keywords_poland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_driver's_license_number" />
          <Match idRef="Keywords_poland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="540c7-621">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="540c7-621">Keywords</span></span>

<span data-ttu-id="540c7-622">| |</span><span class="sxs-lookup"><span data-stu-id="540c7-622"></span></span>
|<span data-ttu-id="540c7-623">**Keywords_poland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="540c7-623">**Keywords_poland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="540c7-624">distribuição</span><span class="sxs-lookup"><span data-stu-id="540c7-624">dl#</span></span>  <br/> <span data-ttu-id="540c7-625">driver license</span><span class="sxs-lookup"><span data-stu-id="540c7-625">driver license</span></span>  <br/> <span data-ttu-id="540c7-626">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-626">driver license number</span></span>  <br/> <span data-ttu-id="540c7-627">licença de driver</span><span class="sxs-lookup"><span data-stu-id="540c7-627">driver licence</span></span>  <br/> <span data-ttu-id="540c7-628">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="540c7-628">drivers lic.</span></span>  <br/> <span data-ttu-id="540c7-629">drivers license</span><span class="sxs-lookup"><span data-stu-id="540c7-629">drivers license</span></span>  <br/> <span data-ttu-id="540c7-630">drivers licence</span><span class="sxs-lookup"><span data-stu-id="540c7-630">drivers licence</span></span>  <br/> <span data-ttu-id="540c7-631">driver's license</span><span class="sxs-lookup"><span data-stu-id="540c7-631">driver's license</span></span>  <br/> <span data-ttu-id="540c7-632">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-632">driver's license number</span></span>  <br/> <span data-ttu-id="540c7-633">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="540c7-633">driver's licence number</span></span>  <br/> <span data-ttu-id="540c7-634">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="540c7-634">driving license number</span></span>  <br/> <span data-ttu-id="540c7-635">dlno #</span><span class="sxs-lookup"><span data-stu-id="540c7-635">dlno#</span></span>  <br/> <span data-ttu-id="540c7-636">Prawo jazdy</span><span class="sxs-lookup"><span data-stu-id="540c7-636">prawo jazdy</span></span>  <br/> |
   
## <a name="portugal"></a><span data-ttu-id="540c7-637">Portugal</span><span class="sxs-lookup"><span data-stu-id="540c7-637">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="540c7-638">Format</span><span class="sxs-lookup"><span data-stu-id="540c7-638">Format</span></span>

<span data-ttu-id="540c7-639">Duas letras seguidas por sete números no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="540c7-639">Two letters followed by a seven numbers in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="540c7-640">Padrão</span><span class="sxs-lookup"><span data-stu-id="540c7-640">Pattern</span></span>

<span data-ttu-id="540c7-641">Duas letras seguidas por sete números com caracteres especiais:</span><span class="sxs-lookup"><span data-stu-id="540c7-641">Two letters followed by seven numbers with special characters:</span></span>
  
-  <span data-ttu-id="540c7-642">Duas letras (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="540c7-642">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="540c7-643">Um hífen</span><span class="sxs-lookup"><span data-stu-id="540c7-643">A hyphen</span></span>
    
- <span data-ttu-id="540c7-644">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="540c7-644">Six digits</span></span>
    
- <span data-ttu-id="540c7-645">Um espaço</span><span class="sxs-lookup"><span data-stu-id="540c7-645">A space</span></span>
    
- <span data-ttu-id="540c7-646">Um dígito</span><span class="sxs-lookup"><span data-stu-id="540c7-646">One digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="540c7-647">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="540c7-647">Checksum</span></span>

<span data-ttu-id="540c7-648">Não</span><span class="sxs-lookup"><span data-stu-id="540c7-648">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="540c7-649">Definição</span><span class="sxs-lookup"><span data-stu-id="540c7-649">Definition</span></span>

<span data-ttu-id="540c7-650">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="540c7-650">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="540c7-651">A expressão `Regex_portugal_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="540c7-651">The regular expression  `Regex_portugal_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="540c7-652">Uma palavra- `Keywords_portugal_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="540c7-652">A keyword from  `Keywords_portugal_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_driver's_license_number" />
          <Match idRef="Keywords_portugal_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="540c7-653">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="540c7-653">Keywords</span></span>

<span data-ttu-id="540c7-654">| |</span><span class="sxs-lookup"><span data-stu-id="540c7-654"></span></span>
|<span data-ttu-id="540c7-655">**Keywords_portugal_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="540c7-655">**Keywords_portugal_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="540c7-656">distribuição</span><span class="sxs-lookup"><span data-stu-id="540c7-656">dl#</span></span>  <br/> <span data-ttu-id="540c7-657">driver license</span><span class="sxs-lookup"><span data-stu-id="540c7-657">driver license</span></span>  <br/> <span data-ttu-id="540c7-658">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-658">driver license number</span></span>  <br/> <span data-ttu-id="540c7-659">licença de driver</span><span class="sxs-lookup"><span data-stu-id="540c7-659">driver licence</span></span>  <br/> <span data-ttu-id="540c7-660">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="540c7-660">drivers lic.</span></span>  <br/> <span data-ttu-id="540c7-661">drivers license</span><span class="sxs-lookup"><span data-stu-id="540c7-661">drivers license</span></span>  <br/> <span data-ttu-id="540c7-662">drivers licence</span><span class="sxs-lookup"><span data-stu-id="540c7-662">drivers licence</span></span>  <br/> <span data-ttu-id="540c7-663">driver's license</span><span class="sxs-lookup"><span data-stu-id="540c7-663">driver's license</span></span>  <br/> <span data-ttu-id="540c7-664">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-664">driver's license number</span></span>  <br/> <span data-ttu-id="540c7-665">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="540c7-665">driver's licence number</span></span>  <br/> <span data-ttu-id="540c7-666">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="540c7-666">driving license number</span></span>  <br/> <span data-ttu-id="540c7-667">dlno #</span><span class="sxs-lookup"><span data-stu-id="540c7-667">dlno#</span></span>  <br/> <span data-ttu-id="540c7-668">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-668">carteira de motorista</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="540c7-669">Romênia</span><span class="sxs-lookup"><span data-stu-id="540c7-669">Romania</span></span>

### <a name="format"></a><span data-ttu-id="540c7-670">Format</span><span class="sxs-lookup"><span data-stu-id="540c7-670">Format</span></span>

<span data-ttu-id="540c7-671">Um caractere seguido por oito dígitos</span><span class="sxs-lookup"><span data-stu-id="540c7-671">One character followed by eight digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="540c7-672">Padrão</span><span class="sxs-lookup"><span data-stu-id="540c7-672">Pattern</span></span>

<span data-ttu-id="540c7-673">Um caractere seguido por oito dígitos:</span><span class="sxs-lookup"><span data-stu-id="540c7-673">One character followed by eight digits:</span></span>
  
-  <span data-ttu-id="540c7-674">Uma letra (não diferencia maiúsculas de minúsculas) ou dígito</span><span class="sxs-lookup"><span data-stu-id="540c7-674">One letter (not case-sensitive) or digit</span></span> 
    
- <span data-ttu-id="540c7-675">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="540c7-675">Eight digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="540c7-676">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="540c7-676">Checksum</span></span>

<span data-ttu-id="540c7-677">Não</span><span class="sxs-lookup"><span data-stu-id="540c7-677">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="540c7-678">Definição</span><span class="sxs-lookup"><span data-stu-id="540c7-678">Definition</span></span>

<span data-ttu-id="540c7-679">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="540c7-679">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="540c7-680">A expressão `Regex_romania_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="540c7-680">The regular expression  `Regex_romania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="540c7-681">Uma palavra- `Keywords_romania_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="540c7-681">A keyword from  `Keywords_romania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_driver's_license_number" />
          <Match idRef="Keywords_romania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="540c7-682">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="540c7-682">Keywords</span></span>

<span data-ttu-id="540c7-683">| |</span><span class="sxs-lookup"><span data-stu-id="540c7-683"></span></span>
|<span data-ttu-id="540c7-684">**Keywords_romania_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="540c7-684">**Keywords_romania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="540c7-685">distribuição</span><span class="sxs-lookup"><span data-stu-id="540c7-685">dl#</span></span>  <br/> <span data-ttu-id="540c7-686">driver license</span><span class="sxs-lookup"><span data-stu-id="540c7-686">driver license</span></span>  <br/> <span data-ttu-id="540c7-687">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-687">driver license number</span></span>  <br/> <span data-ttu-id="540c7-688">licença de driver</span><span class="sxs-lookup"><span data-stu-id="540c7-688">driver licence</span></span>  <br/> <span data-ttu-id="540c7-689">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="540c7-689">drivers lic.</span></span>  <br/> <span data-ttu-id="540c7-690">drivers license</span><span class="sxs-lookup"><span data-stu-id="540c7-690">drivers license</span></span>  <br/> <span data-ttu-id="540c7-691">drivers licence</span><span class="sxs-lookup"><span data-stu-id="540c7-691">drivers licence</span></span>  <br/> <span data-ttu-id="540c7-692">driver's license</span><span class="sxs-lookup"><span data-stu-id="540c7-692">driver's license</span></span>  <br/> <span data-ttu-id="540c7-693">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-693">driver's license number</span></span>  <br/> <span data-ttu-id="540c7-694">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="540c7-694">driver's licence number</span></span>  <br/> <span data-ttu-id="540c7-695">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="540c7-695">driving license number</span></span>  <br/> <span data-ttu-id="540c7-696">dlno #</span><span class="sxs-lookup"><span data-stu-id="540c7-696">dlno#</span></span>  <br/> <span data-ttu-id="540c7-697">permé de conducere</span><span class="sxs-lookup"><span data-stu-id="540c7-697">permis de conducere</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="540c7-698">Eslováquia</span><span class="sxs-lookup"><span data-stu-id="540c7-698">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="540c7-699">Format</span><span class="sxs-lookup"><span data-stu-id="540c7-699">Format</span></span>

<span data-ttu-id="540c7-700">Um caractere seguido por sete dígitos</span><span class="sxs-lookup"><span data-stu-id="540c7-700">One character followed by seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="540c7-701">Padrão</span><span class="sxs-lookup"><span data-stu-id="540c7-701">Pattern</span></span>

<span data-ttu-id="540c7-702">Um caractere seguido por sete dígitos</span><span class="sxs-lookup"><span data-stu-id="540c7-702">One character followed by seven digits</span></span>
  
- <span data-ttu-id="540c7-703">Uma letra (não diferencia maiúsculas de minúsculas) ou dígito</span><span class="sxs-lookup"><span data-stu-id="540c7-703">One letter (not case-sensitive) or digit</span></span>
    
-  <span data-ttu-id="540c7-704">Sete dígitos</span><span class="sxs-lookup"><span data-stu-id="540c7-704">Seven digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="540c7-705">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="540c7-705">Checksum</span></span>

<span data-ttu-id="540c7-706">Não</span><span class="sxs-lookup"><span data-stu-id="540c7-706">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="540c7-707">Definição</span><span class="sxs-lookup"><span data-stu-id="540c7-707">Definition</span></span>

<span data-ttu-id="540c7-708">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="540c7-708">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="540c7-709">A expressão `Regex_slovakia_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="540c7-709">The regular expression  `Regex_slovakia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="540c7-710">Uma palavra- `Keywords_slovakia_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="540c7-710">A keyword from  `Keywords_slovakia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovaknia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovakia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="540c7-711">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="540c7-711">Keywords</span></span>

<span data-ttu-id="540c7-712">| |</span><span class="sxs-lookup"><span data-stu-id="540c7-712"></span></span>
|<span data-ttu-id="540c7-713">**Keywords_slovakia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="540c7-713">**Keywords_slovakia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="540c7-714">distribuição</span><span class="sxs-lookup"><span data-stu-id="540c7-714">dl#</span></span>  <br/> <span data-ttu-id="540c7-715">driver license</span><span class="sxs-lookup"><span data-stu-id="540c7-715">driver license</span></span>  <br/> <span data-ttu-id="540c7-716">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-716">driver license number</span></span>  <br/> <span data-ttu-id="540c7-717">licença de driver</span><span class="sxs-lookup"><span data-stu-id="540c7-717">driver licence</span></span>  <br/> <span data-ttu-id="540c7-718">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="540c7-718">drivers lic.</span></span>  <br/> <span data-ttu-id="540c7-719">drivers license</span><span class="sxs-lookup"><span data-stu-id="540c7-719">drivers license</span></span>  <br/> <span data-ttu-id="540c7-720">drivers licence</span><span class="sxs-lookup"><span data-stu-id="540c7-720">drivers licence</span></span>  <br/> <span data-ttu-id="540c7-721">driver's license</span><span class="sxs-lookup"><span data-stu-id="540c7-721">driver's license</span></span>  <br/> <span data-ttu-id="540c7-722">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-722">driver's license number</span></span>  <br/> <span data-ttu-id="540c7-723">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="540c7-723">driver's licence number</span></span>  <br/> <span data-ttu-id="540c7-724">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="540c7-724">driving license number</span></span>  <br/> <span data-ttu-id="540c7-725">dlno #</span><span class="sxs-lookup"><span data-stu-id="540c7-725">dlno#</span></span>  <br/> <span data-ttu-id="540c7-726">vodičský preukaz</span><span class="sxs-lookup"><span data-stu-id="540c7-726">vodičský preukaz</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="540c7-727">Eslovênia</span><span class="sxs-lookup"><span data-stu-id="540c7-727">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="540c7-728">Format</span><span class="sxs-lookup"><span data-stu-id="540c7-728">Format</span></span>

<span data-ttu-id="540c7-729">Nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="540c7-729">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="540c7-730">Padrão</span><span class="sxs-lookup"><span data-stu-id="540c7-730">Pattern</span></span>

<span data-ttu-id="540c7-731">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="540c7-731">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="540c7-732">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="540c7-732">Checksum</span></span>

<span data-ttu-id="540c7-733">Não</span><span class="sxs-lookup"><span data-stu-id="540c7-733">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="540c7-734">Definição</span><span class="sxs-lookup"><span data-stu-id="540c7-734">Definition</span></span>

<span data-ttu-id="540c7-735">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="540c7-735">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="540c7-736">A expressão `Regex_slovenia_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="540c7-736">The regular expression  `Regex_slovenia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="540c7-737">Uma palavra- `Keywords_slovenia_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="540c7-737">A keyword from  `Keywords_slovenia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovenia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="540c7-738">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="540c7-738">Keywords</span></span>

<span data-ttu-id="540c7-739">| |</span><span class="sxs-lookup"><span data-stu-id="540c7-739"></span></span>
|<span data-ttu-id="540c7-740">**Keywords_slovenia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="540c7-740">**Keywords_slovenia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="540c7-741">distribuição</span><span class="sxs-lookup"><span data-stu-id="540c7-741">dl#</span></span>  <br/> <span data-ttu-id="540c7-742">driver license</span><span class="sxs-lookup"><span data-stu-id="540c7-742">driver license</span></span>  <br/> <span data-ttu-id="540c7-743">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-743">driver license number</span></span>  <br/> <span data-ttu-id="540c7-744">licença de driver</span><span class="sxs-lookup"><span data-stu-id="540c7-744">driver licence</span></span>  <br/> <span data-ttu-id="540c7-745">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="540c7-745">drivers lic.</span></span>  <br/> <span data-ttu-id="540c7-746">drivers license</span><span class="sxs-lookup"><span data-stu-id="540c7-746">drivers license</span></span>  <br/> <span data-ttu-id="540c7-747">drivers licence</span><span class="sxs-lookup"><span data-stu-id="540c7-747">drivers licence</span></span>  <br/> <span data-ttu-id="540c7-748">driver's license</span><span class="sxs-lookup"><span data-stu-id="540c7-748">driver's license</span></span>  <br/> <span data-ttu-id="540c7-749">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-749">driver's license number</span></span>  <br/> <span data-ttu-id="540c7-750">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="540c7-750">driver's licence number</span></span>  <br/> <span data-ttu-id="540c7-751">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="540c7-751">driving license number</span></span>  <br/> <span data-ttu-id="540c7-752">dlno #</span><span class="sxs-lookup"><span data-stu-id="540c7-752">dlno#</span></span>  <br/> <span data-ttu-id="540c7-753">vozniško dovoljenje</span><span class="sxs-lookup"><span data-stu-id="540c7-753">vozniško dovoljenje</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="540c7-754">Espanha</span><span class="sxs-lookup"><span data-stu-id="540c7-754">Spain</span></span>

### <a name="format"></a><span data-ttu-id="540c7-755">Format</span><span class="sxs-lookup"><span data-stu-id="540c7-755">Format</span></span>

<span data-ttu-id="540c7-756">Oito dígitos seguidos de um caractere</span><span class="sxs-lookup"><span data-stu-id="540c7-756">Eight digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="540c7-757">Padrão</span><span class="sxs-lookup"><span data-stu-id="540c7-757">Pattern</span></span>

<span data-ttu-id="540c7-758">Oito dígitos seguidos de um caractere:</span><span class="sxs-lookup"><span data-stu-id="540c7-758">Eight digits followed by one character:</span></span>
  
-  <span data-ttu-id="540c7-759">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="540c7-759">Eight digits</span></span> 
    
- <span data-ttu-id="540c7-760">Um dígito ou letra (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="540c7-760">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="540c7-761">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="540c7-761">Checksum</span></span>

<span data-ttu-id="540c7-762">Sim</span><span class="sxs-lookup"><span data-stu-id="540c7-762">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="540c7-763">Definição</span><span class="sxs-lookup"><span data-stu-id="540c7-763">Definition</span></span>

<span data-ttu-id="540c7-764">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="540c7-764">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="540c7-765">A função `Func_spain_eu_driver's_license_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="540c7-765">The function  `Func_spain_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="540c7-766">Uma palavra- `Keywords_spain_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="540c7-766">A keyword from  `Keywords_spain_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_driver's_license_number" />
          <Match idRef="Keywords_spain_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="540c7-767">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="540c7-767">Keywords</span></span>

<span data-ttu-id="540c7-768">| |</span><span class="sxs-lookup"><span data-stu-id="540c7-768"></span></span>
|<span data-ttu-id="540c7-769">**Keywords_spain_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="540c7-769">**Keywords_spain_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="540c7-770">dlno #</span><span class="sxs-lookup"><span data-stu-id="540c7-770">dlno#</span></span>  <br/> <span data-ttu-id="540c7-771">distribuição</span><span class="sxs-lookup"><span data-stu-id="540c7-771">dl#</span></span>  <br/> <span data-ttu-id="540c7-772">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="540c7-772">drivers lic.</span></span>  <br/> <span data-ttu-id="540c7-773">licença de driver</span><span class="sxs-lookup"><span data-stu-id="540c7-773">driver licence</span></span>  <br/> <span data-ttu-id="540c7-774">driver license</span><span class="sxs-lookup"><span data-stu-id="540c7-774">driver license</span></span>  <br/> <span data-ttu-id="540c7-775">drivers licence</span><span class="sxs-lookup"><span data-stu-id="540c7-775">drivers licence</span></span>  <br/> <span data-ttu-id="540c7-776">drivers license</span><span class="sxs-lookup"><span data-stu-id="540c7-776">drivers license</span></span>  <br/> <span data-ttu-id="540c7-777">driver's licence</span><span class="sxs-lookup"><span data-stu-id="540c7-777">driver's licence</span></span>  <br/> <span data-ttu-id="540c7-778">driver's license</span><span class="sxs-lookup"><span data-stu-id="540c7-778">driver's license</span></span>  <br/> <span data-ttu-id="540c7-779">driving licence</span><span class="sxs-lookup"><span data-stu-id="540c7-779">driving licence</span></span>  <br/> <span data-ttu-id="540c7-780">driving licence</span><span class="sxs-lookup"><span data-stu-id="540c7-780">driving license</span></span>  <br/> <span data-ttu-id="540c7-781">número de licença de driver</span><span class="sxs-lookup"><span data-stu-id="540c7-781">driver licence number</span></span>  <br/> <span data-ttu-id="540c7-782">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-782">driver license number</span></span>  <br/> <span data-ttu-id="540c7-783">número de licença de drivers</span><span class="sxs-lookup"><span data-stu-id="540c7-783">drivers licence number</span></span>  <br/> <span data-ttu-id="540c7-784">número de licença de drivers</span><span class="sxs-lookup"><span data-stu-id="540c7-784">drivers license number</span></span>  <br/> <span data-ttu-id="540c7-785">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="540c7-785">driver's licence number</span></span>  <br/> <span data-ttu-id="540c7-786">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-786">driver's license number</span></span>  <br/> <span data-ttu-id="540c7-787">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="540c7-787">driving licence number</span></span>  <br/> <span data-ttu-id="540c7-788">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="540c7-788">driving license number</span></span>  <br/> <span data-ttu-id="540c7-789">permissão de condução</span><span class="sxs-lookup"><span data-stu-id="540c7-789">driving permit</span></span>  <br/> <span data-ttu-id="540c7-790">número de permissão de dirigir</span><span class="sxs-lookup"><span data-stu-id="540c7-790">driving permit number</span></span>  <br/> <span data-ttu-id="540c7-791">permiso de conducción</span><span class="sxs-lookup"><span data-stu-id="540c7-791">permiso de conducción</span></span>  <br/> <span data-ttu-id="540c7-792">permiso conducción</span><span class="sxs-lookup"><span data-stu-id="540c7-792">permiso conducción</span></span>  <br/> <span data-ttu-id="540c7-793">número licencia conducir</span><span class="sxs-lookup"><span data-stu-id="540c7-793">número licencia conducir</span></span>  <br/> <span data-ttu-id="540c7-794">número de Carnet de conducir</span><span class="sxs-lookup"><span data-stu-id="540c7-794">número de carnet de conducir</span></span>  <br/> <span data-ttu-id="540c7-795">número Carnet conducir</span><span class="sxs-lookup"><span data-stu-id="540c7-795">número carnet conducir</span></span>  <br/> <span data-ttu-id="540c7-796">licencia conducir</span><span class="sxs-lookup"><span data-stu-id="540c7-796">licencia conducir</span></span>  <br/> <span data-ttu-id="540c7-797">número de permiso de conducir</span><span class="sxs-lookup"><span data-stu-id="540c7-797">número de permiso de conducir</span></span>  <br/> <span data-ttu-id="540c7-798">número de permiso conducir</span><span class="sxs-lookup"><span data-stu-id="540c7-798">número de permiso conducir</span></span>  <br/> <span data-ttu-id="540c7-799">número permiso conducir</span><span class="sxs-lookup"><span data-stu-id="540c7-799">número permiso conducir</span></span>  <br/> <span data-ttu-id="540c7-800">permiso conducir</span><span class="sxs-lookup"><span data-stu-id="540c7-800">permiso conducir</span></span>  <br/> <span data-ttu-id="540c7-801">licencia de manejo</span><span class="sxs-lookup"><span data-stu-id="540c7-801">licencia de manejo</span></span>  <br/> <span data-ttu-id="540c7-802">El Carnet de conducir</span><span class="sxs-lookup"><span data-stu-id="540c7-802">el carnet de conducir</span></span>  <br/> <span data-ttu-id="540c7-803">Carnet conducir</span><span class="sxs-lookup"><span data-stu-id="540c7-803">carnet conducir</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="540c7-804">Suécia</span><span class="sxs-lookup"><span data-stu-id="540c7-804">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="540c7-805">Format</span><span class="sxs-lookup"><span data-stu-id="540c7-805">Format</span></span>

<span data-ttu-id="540c7-806">Dez dígitos contendo um hífen</span><span class="sxs-lookup"><span data-stu-id="540c7-806">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="540c7-807">Padrão</span><span class="sxs-lookup"><span data-stu-id="540c7-807">Pattern</span></span>

<span data-ttu-id="540c7-808">Dez dígitos contendo um hífen:</span><span class="sxs-lookup"><span data-stu-id="540c7-808">Ten digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="540c7-809">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="540c7-809">Six digits</span></span> 
    
- <span data-ttu-id="540c7-810">Um hífen</span><span class="sxs-lookup"><span data-stu-id="540c7-810">A hyphen</span></span>
    
- <span data-ttu-id="540c7-811">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="540c7-811">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="540c7-812">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="540c7-812">Checksum</span></span>

<span data-ttu-id="540c7-813">Não</span><span class="sxs-lookup"><span data-stu-id="540c7-813">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="540c7-814">Definição</span><span class="sxs-lookup"><span data-stu-id="540c7-814">Definition</span></span>

<span data-ttu-id="540c7-815">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="540c7-815">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="540c7-816">A expressão `Regex_sweden_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="540c7-816">The regular expression  `Regex_sweden_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="540c7-817">Uma palavra- `Keywords_sweden_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="540c7-817">A keyword from  `Keywords_sweden_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_driver's_license_number" />
          <Match idRef="Keywords_sweden_eu_driver's_license_number" />
        </Pattern>
</Entity> 
```

### <a name="keywords"></a><span data-ttu-id="540c7-818">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="540c7-818">Keywords</span></span>

<span data-ttu-id="540c7-819">| |</span><span class="sxs-lookup"><span data-stu-id="540c7-819"></span></span>
|<span data-ttu-id="540c7-820">**Keywords_sweden_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="540c7-820">**Keywords_sweden_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="540c7-821">distribuição</span><span class="sxs-lookup"><span data-stu-id="540c7-821">dl#</span></span>  <br/> <span data-ttu-id="540c7-822">driver license</span><span class="sxs-lookup"><span data-stu-id="540c7-822">driver license</span></span>  <br/> <span data-ttu-id="540c7-823">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-823">driver license number</span></span>  <br/> <span data-ttu-id="540c7-824">licença de driver</span><span class="sxs-lookup"><span data-stu-id="540c7-824">driver licence</span></span>  <br/> <span data-ttu-id="540c7-825">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="540c7-825">drivers lic.</span></span>  <br/> <span data-ttu-id="540c7-826">drivers license</span><span class="sxs-lookup"><span data-stu-id="540c7-826">drivers license</span></span>  <br/> <span data-ttu-id="540c7-827">drivers licence</span><span class="sxs-lookup"><span data-stu-id="540c7-827">drivers licence</span></span>  <br/> <span data-ttu-id="540c7-828">driver's license</span><span class="sxs-lookup"><span data-stu-id="540c7-828">driver's license</span></span>  <br/> <span data-ttu-id="540c7-829">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="540c7-829">driver's license number</span></span>  <br/> <span data-ttu-id="540c7-830">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="540c7-830">driver's licence number</span></span>  <br/> <span data-ttu-id="540c7-831">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="540c7-831">driving license number</span></span>  <br/> <span data-ttu-id="540c7-832">dlno #</span><span class="sxs-lookup"><span data-stu-id="540c7-832">dlno#</span></span>  <br/> <span data-ttu-id="540c7-833">körkort</span><span class="sxs-lookup"><span data-stu-id="540c7-833">körkort</span></span>  <br/> |
   
## <a name="uk"></a><span data-ttu-id="540c7-834">Reino Unido</span><span class="sxs-lookup"><span data-stu-id="540c7-834">UK</span></span>

<span data-ttu-id="540c7-835">Para obter detalhes, consulte a seção "Reino Unido</span><span class="sxs-lookup"><span data-stu-id="540c7-835">For details, see the section "U.K.</span></span> <span data-ttu-id="540c7-836">Número da carteira de motorista "em [que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="540c7-836">Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="540c7-837">Confira também</span><span class="sxs-lookup"><span data-stu-id="540c7-837">See also</span></span>

[<span data-ttu-id="540c7-838">O que os tipos de informações confidenciais procuram</span><span class="sxs-lookup"><span data-stu-id="540c7-838">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)


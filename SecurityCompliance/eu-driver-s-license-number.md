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
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32255769"
---
# <a name="eu-drivers-license-number"></a><span data-ttu-id="fff16-104">Número da carteira de motorista da UE</span><span class="sxs-lookup"><span data-stu-id="fff16-104">EU Driver's License Number</span></span>

<span data-ttu-id="fff16-105">Este tópico mostra o que uma política de prevenção de perda de dados (DLP) procura quando detecta o tipo de informação confidencial do número de licença do driver da UE.</span><span class="sxs-lookup"><span data-stu-id="fff16-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Driver's License Number sensitive information type.</span></span> <span data-ttu-id="fff16-106">Esse tipo de informação confidencial define diferentes padrões, palavras-chave e outras evidências para cada país.</span><span class="sxs-lookup"><span data-stu-id="fff16-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="fff16-107">Áustria </span><span class="sxs-lookup"><span data-stu-id="fff16-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="fff16-108">Formatar</span><span class="sxs-lookup"><span data-stu-id="fff16-108">Format</span></span>

<span data-ttu-id="fff16-109">Oito dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="fff16-109">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fff16-110">Padrão</span><span class="sxs-lookup"><span data-stu-id="fff16-110">Pattern</span></span>

<span data-ttu-id="fff16-111">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="fff16-111">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="fff16-112">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fff16-112">Checksum</span></span>

<span data-ttu-id="fff16-113">Não</span><span class="sxs-lookup"><span data-stu-id="fff16-113">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="fff16-114">Definição</span><span class="sxs-lookup"><span data-stu-id="fff16-114">Definition</span></span>

<span data-ttu-id="fff16-115">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fff16-115">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fff16-116">A expressão `Regex_austria_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fff16-116">The regular expression  `Regex_austria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fff16-117">Uma palavra- `Keywords_austria_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fff16-117">A keyword from  `Keywords_austria_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_driver's_license_number" />
          <Match idRef="Keywords_austria_eu_driver's_license_number" />
        </Pattern>
    </Entity>

```

### <a name="keywords"></a><span data-ttu-id="fff16-118">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fff16-118">Keywords</span></span>

<span data-ttu-id="fff16-119">| |</span><span class="sxs-lookup"><span data-stu-id="fff16-119"></span></span>
|<span data-ttu-id="fff16-120">**Keywords_austria_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="fff16-120">**Keywords_austria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="fff16-121">distribuição</span><span class="sxs-lookup"><span data-stu-id="fff16-121">dl#</span></span>  <br/> <span data-ttu-id="fff16-122">driver license</span><span class="sxs-lookup"><span data-stu-id="fff16-122">driver license</span></span>  <br/> <span data-ttu-id="fff16-123">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-123">driver license number</span></span>  <br/> <span data-ttu-id="fff16-124">licença de driver</span><span class="sxs-lookup"><span data-stu-id="fff16-124">driver licence</span></span>  <br/> <span data-ttu-id="fff16-125">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="fff16-125">drivers lic.</span></span>  <br/> <span data-ttu-id="fff16-126">drivers license</span><span class="sxs-lookup"><span data-stu-id="fff16-126">drivers license</span></span>  <br/> <span data-ttu-id="fff16-127">driver's licence</span><span class="sxs-lookup"><span data-stu-id="fff16-127">driver's licence</span></span>  <br/> <span data-ttu-id="fff16-128">driver's license</span><span class="sxs-lookup"><span data-stu-id="fff16-128">driver's license</span></span>  <br/> <span data-ttu-id="fff16-129">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-129">driver's license number</span></span>  <br/> <span data-ttu-id="fff16-130">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="fff16-130">driver's licence number</span></span>  <br/>  <span data-ttu-id="fff16-131">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="fff16-131">driving license number</span></span>  <br/> <span data-ttu-id="fff16-132">dlno #</span><span class="sxs-lookup"><span data-stu-id="fff16-132">dlno#</span></span>  <br/> <span data-ttu-id="fff16-133">fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="fff16-133">fuhrerschein</span></span>  <br/> <span data-ttu-id="fff16-134">fuhrerschein Republik Osterreich</span><span class="sxs-lookup"><span data-stu-id="fff16-134">fuhrerschein republik osterreich</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="fff16-135">Bélgica </span><span class="sxs-lookup"><span data-stu-id="fff16-135">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="fff16-136">Formatar</span><span class="sxs-lookup"><span data-stu-id="fff16-136">Format</span></span>

<span data-ttu-id="fff16-137">10 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="fff16-137">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fff16-138">Padrão</span><span class="sxs-lookup"><span data-stu-id="fff16-138">Pattern</span></span>

<span data-ttu-id="fff16-139">10 dígitos</span><span class="sxs-lookup"><span data-stu-id="fff16-139">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="fff16-140">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fff16-140">Checksum</span></span>

<span data-ttu-id="fff16-141">Não</span><span class="sxs-lookup"><span data-stu-id="fff16-141">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="fff16-142">Definição</span><span class="sxs-lookup"><span data-stu-id="fff16-142">Definition</span></span>

<span data-ttu-id="fff16-143">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fff16-143">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fff16-144">A expressão `Regex_belgium_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fff16-144">The regular expression  `Regex_belgium_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fff16-145">Uma palavra- `Keywords_belgium_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fff16-145">A keyword from  `Keywords_belgium_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_driver's_license_number" />
          <Match idRef="Keywords_belgium_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="fff16-146">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fff16-146">Keywords</span></span>

<span data-ttu-id="fff16-147">| |</span><span class="sxs-lookup"><span data-stu-id="fff16-147"></span></span>
|<span data-ttu-id="fff16-148">**Keywords__belgium_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="fff16-148">**Keywords__belgium_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="fff16-149">distribuição</span><span class="sxs-lookup"><span data-stu-id="fff16-149">dl#</span></span>  <br/> <span data-ttu-id="fff16-150">driver license</span><span class="sxs-lookup"><span data-stu-id="fff16-150">driver license</span></span>  <br/> <span data-ttu-id="fff16-151">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-151">driver license number</span></span>  <br/> <span data-ttu-id="fff16-152">licença de driver</span><span class="sxs-lookup"><span data-stu-id="fff16-152">driver licence</span></span>  <br/> <span data-ttu-id="fff16-153">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="fff16-153">drivers lic.</span></span>  <br/> <span data-ttu-id="fff16-154">drivers license</span><span class="sxs-lookup"><span data-stu-id="fff16-154">drivers license</span></span>  <br/> <span data-ttu-id="fff16-155">drivers licence</span><span class="sxs-lookup"><span data-stu-id="fff16-155">drivers licence</span></span>  <br/> <span data-ttu-id="fff16-156">driver's license</span><span class="sxs-lookup"><span data-stu-id="fff16-156">driver's license</span></span>  <br/> <span data-ttu-id="fff16-157">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-157">driver's license number</span></span>  <br/> <span data-ttu-id="fff16-158">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="fff16-158">driver's licence number</span></span>  <br/> <span data-ttu-id="fff16-159">dlno #</span><span class="sxs-lookup"><span data-stu-id="fff16-159">dlno#</span></span>  <br/> <span data-ttu-id="fff16-160">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="fff16-160">rijbewijs</span></span>  <br/> <span data-ttu-id="fff16-161">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="fff16-161">rijbewijsnummer</span></span>  <br/> <span data-ttu-id="fff16-162">führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="fff16-162">führerscheinnummer</span></span>  <br/> <span data-ttu-id="fff16-163">fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="fff16-163">fuhrerscheinnummer</span></span>  <br/> <span data-ttu-id="fff16-164">fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="fff16-164">fuehrerscheinnummer</span></span>  <br/> <span data-ttu-id="fff16-165">führerschein-NR</span><span class="sxs-lookup"><span data-stu-id="fff16-165">führerschein- nr</span></span>  <br/> <span data-ttu-id="fff16-166">fuehrerschein-NR</span><span class="sxs-lookup"><span data-stu-id="fff16-166">fuehrerschein- Nr</span></span>  <br/> <span data-ttu-id="fff16-167">fuehrerschein-NR</span><span class="sxs-lookup"><span data-stu-id="fff16-167">fuehrerschein- nr</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="fff16-168">Bulgária</span><span class="sxs-lookup"><span data-stu-id="fff16-168">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="fff16-169">Formatar</span><span class="sxs-lookup"><span data-stu-id="fff16-169">Format</span></span>

<span data-ttu-id="fff16-170">Nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="fff16-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fff16-171">Padrão</span><span class="sxs-lookup"><span data-stu-id="fff16-171">Pattern</span></span>

<span data-ttu-id="fff16-172">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="fff16-172">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="fff16-173">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fff16-173">Checksum</span></span>

<span data-ttu-id="fff16-174">Não</span><span class="sxs-lookup"><span data-stu-id="fff16-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="fff16-175">Definição</span><span class="sxs-lookup"><span data-stu-id="fff16-175">Definition</span></span>

<span data-ttu-id="fff16-176">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fff16-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fff16-177">A expressão `Regex_bulgaria_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fff16-177">The regular expression  `Regex_bulgaria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fff16-178">Uma palavra- `Keywords_bulgaria_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fff16-178">A keyword from  `Keywords_bulgaria_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
             <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_driver's_license_number" />
          <Match idRef="Keywords_bulgaria_eu_driver's_license_number" />
        </Pattern> 
</Entity>    

```

### <a name="keywords"></a><span data-ttu-id="fff16-179">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fff16-179">Keywords</span></span>

<span data-ttu-id="fff16-180">| |</span><span class="sxs-lookup"><span data-stu-id="fff16-180"></span></span>
|<span data-ttu-id="fff16-181">**Keywords_bulgaria_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="fff16-181">**Keywords_bulgaria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="fff16-182">distribuição</span><span class="sxs-lookup"><span data-stu-id="fff16-182">dl#</span></span>  <br/> <span data-ttu-id="fff16-183">driver license</span><span class="sxs-lookup"><span data-stu-id="fff16-183">driver license</span></span>  <br/> <span data-ttu-id="fff16-184">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-184">driver license number</span></span>  <br/> <span data-ttu-id="fff16-185">licença de driver</span><span class="sxs-lookup"><span data-stu-id="fff16-185">driver licence</span></span>  <br/> <span data-ttu-id="fff16-186">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="fff16-186">drivers lic.</span></span>  <br/> <span data-ttu-id="fff16-187">drivers license</span><span class="sxs-lookup"><span data-stu-id="fff16-187">drivers license</span></span>  <br/> <span data-ttu-id="fff16-188">drivers licence</span><span class="sxs-lookup"><span data-stu-id="fff16-188">drivers licence</span></span>  <br/> <span data-ttu-id="fff16-189">driver's license</span><span class="sxs-lookup"><span data-stu-id="fff16-189">driver's license</span></span>  <br/> <span data-ttu-id="fff16-190">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-190">driver's license number</span></span>  <br/> <span data-ttu-id="fff16-191">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="fff16-191">driver's licence number</span></span>  <br/> <span data-ttu-id="fff16-192">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="fff16-192">driving license number</span></span>  <br/> <span data-ttu-id="fff16-193">dlno #</span><span class="sxs-lookup"><span data-stu-id="fff16-193">dlno#</span></span>  <br/> <span data-ttu-id="fff16-194">свидетелство за управление на мпс</span><span class="sxs-lookup"><span data-stu-id="fff16-194">свидетелство за управление на мпс</span></span>  <br/> <span data-ttu-id="fff16-195">свидетелство за управление на моторно превозно средство</span><span class="sxs-lookup"><span data-stu-id="fff16-195">свидетелство за управление на моторно превозно средство</span></span>  <br/> <span data-ttu-id="fff16-196">сумпс</span><span class="sxs-lookup"><span data-stu-id="fff16-196">сумпс</span></span>  <br/> <span data-ttu-id="fff16-197">шофьорска книжка</span><span class="sxs-lookup"><span data-stu-id="fff16-197">шофьорска книжка</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="fff16-198">Croácia</span><span class="sxs-lookup"><span data-stu-id="fff16-198">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="fff16-199">Formatar</span><span class="sxs-lookup"><span data-stu-id="fff16-199">Format</span></span>

<span data-ttu-id="fff16-200">Oito dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="fff16-200">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fff16-201">Padrão</span><span class="sxs-lookup"><span data-stu-id="fff16-201">Pattern</span></span>

<span data-ttu-id="fff16-202">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="fff16-202">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="fff16-203">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fff16-203">Checksum</span></span>

<span data-ttu-id="fff16-204">Não</span><span class="sxs-lookup"><span data-stu-id="fff16-204">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="fff16-205">Definição</span><span class="sxs-lookup"><span data-stu-id="fff16-205">Definition</span></span>

<span data-ttu-id="fff16-206">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fff16-206">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fff16-207">A expressão `Regex_croatia_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fff16-207">The regular expression  `Regex_croatia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fff16-208">Uma palavra- `Keywords_croatia_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fff16-208">A keyword from  `Keywords_croatia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_driver's_license_number" />
          <Match idRef="Keywords_croatia_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="fff16-209">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fff16-209">Keywords</span></span>

<span data-ttu-id="fff16-210">| |</span><span class="sxs-lookup"><span data-stu-id="fff16-210"></span></span>
|<span data-ttu-id="fff16-211">**Keywords_croatia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="fff16-211">**Keywords_croatia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="fff16-212">distribuição</span><span class="sxs-lookup"><span data-stu-id="fff16-212">dl#</span></span>  <br/> <span data-ttu-id="fff16-213">driver license</span><span class="sxs-lookup"><span data-stu-id="fff16-213">driver license</span></span>  <br/> <span data-ttu-id="fff16-214">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-214">driver license number</span></span>  <br/> <span data-ttu-id="fff16-215">licença de driver</span><span class="sxs-lookup"><span data-stu-id="fff16-215">driver licence</span></span>  <br/> <span data-ttu-id="fff16-216">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="fff16-216">drivers lic.</span></span>  <br/> <span data-ttu-id="fff16-217">drivers license</span><span class="sxs-lookup"><span data-stu-id="fff16-217">drivers license</span></span>  <br/> <span data-ttu-id="fff16-218">drivers licence</span><span class="sxs-lookup"><span data-stu-id="fff16-218">drivers licence</span></span>  <br/> <span data-ttu-id="fff16-219">driver's license</span><span class="sxs-lookup"><span data-stu-id="fff16-219">driver's license</span></span>  <br/> <span data-ttu-id="fff16-220">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-220">driver's license number</span></span>  <br/> <span data-ttu-id="fff16-221">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="fff16-221">driver's licence number</span></span>  <br/> <span data-ttu-id="fff16-222">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="fff16-222">driving license number</span></span>  <br/> <span data-ttu-id="fff16-223">dlno #</span><span class="sxs-lookup"><span data-stu-id="fff16-223">dlno#</span></span>  <br/> <span data-ttu-id="fff16-224">vozačka dozvola</span><span class="sxs-lookup"><span data-stu-id="fff16-224">vozačka dozvola</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="fff16-225">Chipre</span><span class="sxs-lookup"><span data-stu-id="fff16-225">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="fff16-226">Formatar</span><span class="sxs-lookup"><span data-stu-id="fff16-226">Format</span></span>

<span data-ttu-id="fff16-227">12 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="fff16-227">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fff16-228">Padrão</span><span class="sxs-lookup"><span data-stu-id="fff16-228">Pattern</span></span>

<span data-ttu-id="fff16-229">12 dígitos</span><span class="sxs-lookup"><span data-stu-id="fff16-229">12 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="fff16-230">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fff16-230">Checksum</span></span>

<span data-ttu-id="fff16-231">Não</span><span class="sxs-lookup"><span data-stu-id="fff16-231">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="fff16-232">Definição</span><span class="sxs-lookup"><span data-stu-id="fff16-232">Definition</span></span>

<span data-ttu-id="fff16-233">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fff16-233">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fff16-234">A expressão `Regex_cyprus_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fff16-234">The regular expression  `Regex_cyprus_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fff16-235">Uma palavra- `Keywords_cyprus_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fff16-235">A keyword from  `Keywords_cyprus_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_driver's_license_number" />
          <Match idRef="Keywords_cyprus_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fff16-236">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fff16-236">Keywords</span></span>

<span data-ttu-id="fff16-237">| |</span><span class="sxs-lookup"><span data-stu-id="fff16-237"></span></span>
|<span data-ttu-id="fff16-238">**Keywords_cyprus_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="fff16-238">**Keywords_cyprus_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="fff16-239">distribuição</span><span class="sxs-lookup"><span data-stu-id="fff16-239">dl#</span></span>  <br/> <span data-ttu-id="fff16-240">driver license</span><span class="sxs-lookup"><span data-stu-id="fff16-240">driver license</span></span>  <br/> <span data-ttu-id="fff16-241">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-241">driver license number</span></span>  <br/> <span data-ttu-id="fff16-242">licença de driver</span><span class="sxs-lookup"><span data-stu-id="fff16-242">driver licence</span></span>  <br/> <span data-ttu-id="fff16-243">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="fff16-243">drivers lic.</span></span>  <br/> <span data-ttu-id="fff16-244">drivers license</span><span class="sxs-lookup"><span data-stu-id="fff16-244">drivers license</span></span>  <br/> <span data-ttu-id="fff16-245">drivers licence</span><span class="sxs-lookup"><span data-stu-id="fff16-245">drivers licence</span></span>  <br/> <span data-ttu-id="fff16-246">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-246">driver's license number</span></span>  <br/> <span data-ttu-id="fff16-247">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="fff16-247">driver's licence number</span></span>  <br/> <span data-ttu-id="fff16-248">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="fff16-248">driving license number</span></span>  <br/> <span data-ttu-id="fff16-249">dlno #</span><span class="sxs-lookup"><span data-stu-id="fff16-249">dlno#</span></span>  <br/> <span data-ttu-id="fff16-250">άδεια οδήγησης</span><span class="sxs-lookup"><span data-stu-id="fff16-250">άδεια οδήγησης</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="fff16-251">República Tcheca</span><span class="sxs-lookup"><span data-stu-id="fff16-251">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="fff16-252">Formatar</span><span class="sxs-lookup"><span data-stu-id="fff16-252">Format</span></span>

<span data-ttu-id="fff16-253">Duas letras seguidas por seis dígitos</span><span class="sxs-lookup"><span data-stu-id="fff16-253">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fff16-254">Padrão</span><span class="sxs-lookup"><span data-stu-id="fff16-254">Pattern</span></span>

<span data-ttu-id="fff16-255">Oito letras e dígitos:</span><span class="sxs-lookup"><span data-stu-id="fff16-255">Eight letters and digits:</span></span>
  
- <span data-ttu-id="fff16-256">Duas letras (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="fff16-256">Two letters (not case-sensitive)</span></span>
    
- <span data-ttu-id="fff16-257">Um espaço (opcional)</span><span class="sxs-lookup"><span data-stu-id="fff16-257">A space (optional)</span></span>
    
- <span data-ttu-id="fff16-258">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="fff16-258">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="fff16-259">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fff16-259">Checksum</span></span>

<span data-ttu-id="fff16-260">Não</span><span class="sxs-lookup"><span data-stu-id="fff16-260">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="fff16-261">Definição</span><span class="sxs-lookup"><span data-stu-id="fff16-261">Definition</span></span>

<span data-ttu-id="fff16-262">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fff16-262">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fff16-263">A expressão `Regex_czech_republic_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fff16-263">The regular expression  `Regex_czech_republic_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fff16-264">Uma palavra- `Keywords_czech_republic_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fff16-264">A keyword from  `Keywords_czech_republic_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_driver's_license_number" />
          <Match idRef="Keywords_czech_republic_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="fff16-265">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fff16-265">Keywords</span></span>

<span data-ttu-id="fff16-266">| |</span><span class="sxs-lookup"><span data-stu-id="fff16-266"></span></span>
|<span data-ttu-id="fff16-267">**Keywords_czech_republic_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="fff16-267">**Keywords_czech_republic_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="fff16-268">distribuição</span><span class="sxs-lookup"><span data-stu-id="fff16-268">dl#</span></span>  <br/> <span data-ttu-id="fff16-269">driver license</span><span class="sxs-lookup"><span data-stu-id="fff16-269">driver license</span></span>  <br/> <span data-ttu-id="fff16-270">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-270">driver license number</span></span>  <br/> <span data-ttu-id="fff16-271">licença de driver</span><span class="sxs-lookup"><span data-stu-id="fff16-271">driver licence</span></span>  <br/> <span data-ttu-id="fff16-272">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="fff16-272">drivers lic.</span></span>  <br/> <span data-ttu-id="fff16-273">drivers license</span><span class="sxs-lookup"><span data-stu-id="fff16-273">drivers license</span></span>  <br/> <span data-ttu-id="fff16-274">drivers licence</span><span class="sxs-lookup"><span data-stu-id="fff16-274">drivers licence</span></span>  <br/> <span data-ttu-id="fff16-275">driver's license</span><span class="sxs-lookup"><span data-stu-id="fff16-275">driver's license</span></span>  <br/> <span data-ttu-id="fff16-276">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-276">driver's license number</span></span>  <br/> <span data-ttu-id="fff16-277">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-277">driver's license number</span></span>  <br/> <span data-ttu-id="fff16-278">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="fff16-278">driver's licence number</span></span>  <br/> <span data-ttu-id="fff16-279">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="fff16-279">driving license number</span></span>  <br/> <span data-ttu-id="fff16-280">dlno #</span><span class="sxs-lookup"><span data-stu-id="fff16-280">dlno#</span></span>  <br/> <span data-ttu-id="fff16-281">řidičský prúkaz</span><span class="sxs-lookup"><span data-stu-id="fff16-281">řidičský prúkaz</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="fff16-282">Dinamarca</span><span class="sxs-lookup"><span data-stu-id="fff16-282">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="fff16-283">Formatar</span><span class="sxs-lookup"><span data-stu-id="fff16-283">Format</span></span>

<span data-ttu-id="fff16-284">Oito dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="fff16-284">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fff16-285">Padrão</span><span class="sxs-lookup"><span data-stu-id="fff16-285">Pattern</span></span>

<span data-ttu-id="fff16-286">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="fff16-286">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="fff16-287">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fff16-287">Checksum</span></span>

<span data-ttu-id="fff16-288">Sim</span><span class="sxs-lookup"><span data-stu-id="fff16-288">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="fff16-289">Definição</span><span class="sxs-lookup"><span data-stu-id="fff16-289">Definition</span></span>

<span data-ttu-id="fff16-290">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fff16-290">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fff16-291">A expressão `Regex_denmark_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fff16-291">The regular expression  `Regex_denmark_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fff16-292">Uma palavra- `Keywords_denmark_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fff16-292">A keyword from  `Keywords_denmark_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_driver's_license_number" />
          <Match idRef="Keywords_denmark_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="fff16-293">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fff16-293">Keywords</span></span>

<span data-ttu-id="fff16-294">| |</span><span class="sxs-lookup"><span data-stu-id="fff16-294"></span></span>
|<span data-ttu-id="fff16-295">**Keywords_denmark_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="fff16-295">**Keywords_denmark_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="fff16-296">distribuição</span><span class="sxs-lookup"><span data-stu-id="fff16-296">dl#</span></span>  <br/> <span data-ttu-id="fff16-297">driver license</span><span class="sxs-lookup"><span data-stu-id="fff16-297">driver license</span></span>  <br/> <span data-ttu-id="fff16-298">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-298">driver license number</span></span>  <br/> <span data-ttu-id="fff16-299">licença de driver</span><span class="sxs-lookup"><span data-stu-id="fff16-299">driver licence</span></span>  <br/> <span data-ttu-id="fff16-300">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="fff16-300">drivers lic.</span></span>  <br/> <span data-ttu-id="fff16-301">drivers license</span><span class="sxs-lookup"><span data-stu-id="fff16-301">drivers license</span></span>  <br/> <span data-ttu-id="fff16-302">drivers licence</span><span class="sxs-lookup"><span data-stu-id="fff16-302">drivers licence</span></span>  <br/> <span data-ttu-id="fff16-303">driver's license</span><span class="sxs-lookup"><span data-stu-id="fff16-303">driver's license</span></span>  <br/> <span data-ttu-id="fff16-304">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-304">driver's license number</span></span>  <br/> <span data-ttu-id="fff16-305">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="fff16-305">driver's licence number</span></span>  <br/> <span data-ttu-id="fff16-306">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="fff16-306">driving license number</span></span>  <br/> <span data-ttu-id="fff16-307">dlno #</span><span class="sxs-lookup"><span data-stu-id="fff16-307">dlno#</span></span>  <br/> <span data-ttu-id="fff16-308">kørekort</span><span class="sxs-lookup"><span data-stu-id="fff16-308">kørekort</span></span>  <br/> <span data-ttu-id="fff16-309">kørekortnummer</span><span class="sxs-lookup"><span data-stu-id="fff16-309">kørekortnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="fff16-310">Estônia</span><span class="sxs-lookup"><span data-stu-id="fff16-310">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="fff16-311">Formatar</span><span class="sxs-lookup"><span data-stu-id="fff16-311">Format</span></span>

<span data-ttu-id="fff16-312">Duas letras seguidas por seis dígitos</span><span class="sxs-lookup"><span data-stu-id="fff16-312">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fff16-313">Padrão</span><span class="sxs-lookup"><span data-stu-id="fff16-313">Pattern</span></span>

<span data-ttu-id="fff16-314">Duas letras e seis dígitos:</span><span class="sxs-lookup"><span data-stu-id="fff16-314">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="fff16-315">As letras "ET" (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="fff16-315">The letters "ET" (not case-sensitive)</span></span> 
    
- <span data-ttu-id="fff16-316">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="fff16-316">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="fff16-317">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fff16-317">Checksum</span></span>

<span data-ttu-id="fff16-318">Não</span><span class="sxs-lookup"><span data-stu-id="fff16-318">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="fff16-319">Definição</span><span class="sxs-lookup"><span data-stu-id="fff16-319">Definition</span></span>

<span data-ttu-id="fff16-320">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fff16-320">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fff16-321">A expressão `Regex_estonia_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fff16-321">The regular expression  `Regex_estonia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fff16-322">Uma palavra- `Keywords_estonia_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fff16-322">A keyword from  `Keywords_estonia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_driver's_license_number" />
          <Match idRef="Keywords_estonia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fff16-323">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fff16-323">Keywords</span></span>

<span data-ttu-id="fff16-324">| |</span><span class="sxs-lookup"><span data-stu-id="fff16-324"></span></span>
|<span data-ttu-id="fff16-325">**Keywords_estonia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="fff16-325">**Keywords_estonia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="fff16-326">distribuição</span><span class="sxs-lookup"><span data-stu-id="fff16-326">dl#</span></span>  <br/> <span data-ttu-id="fff16-327">driver license</span><span class="sxs-lookup"><span data-stu-id="fff16-327">driver license</span></span>  <br/> <span data-ttu-id="fff16-328">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-328">driver license number</span></span>  <br/> <span data-ttu-id="fff16-329">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-329">driver license number</span></span>  <br/> <span data-ttu-id="fff16-330">licença de driver</span><span class="sxs-lookup"><span data-stu-id="fff16-330">driver licence</span></span>  <br/> <span data-ttu-id="fff16-331">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="fff16-331">drivers lic.</span></span>  <br/> <span data-ttu-id="fff16-332">drivers license</span><span class="sxs-lookup"><span data-stu-id="fff16-332">drivers license</span></span>  <br/> <span data-ttu-id="fff16-333">drivers licence</span><span class="sxs-lookup"><span data-stu-id="fff16-333">drivers licence</span></span>  <br/> <span data-ttu-id="fff16-334">driver's license</span><span class="sxs-lookup"><span data-stu-id="fff16-334">driver's license</span></span>  <br/> <span data-ttu-id="fff16-335">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-335">driver's license number</span></span>  <br/> <span data-ttu-id="fff16-336">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="fff16-336">driving license number</span></span>  <br/> <span data-ttu-id="fff16-337">dlno #</span><span class="sxs-lookup"><span data-stu-id="fff16-337">dlno#</span></span>  <br/> <span data-ttu-id="fff16-338">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fff16-338">permis de conduire</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="fff16-339">Finlândia</span><span class="sxs-lookup"><span data-stu-id="fff16-339">Finland</span></span>

### <a name="format"></a><span data-ttu-id="fff16-340">Formatar</span><span class="sxs-lookup"><span data-stu-id="fff16-340">Format</span></span>

<span data-ttu-id="fff16-341">10 dígitos que contêm um hífen</span><span class="sxs-lookup"><span data-stu-id="fff16-341">10 digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fff16-342">Padrão</span><span class="sxs-lookup"><span data-stu-id="fff16-342">Pattern</span></span>

<span data-ttu-id="fff16-343">10 dígitos contendo um hífen:</span><span class="sxs-lookup"><span data-stu-id="fff16-343">10 digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="fff16-344">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="fff16-344">Six digits</span></span> 
    
- <span data-ttu-id="fff16-345">Um hífen</span><span class="sxs-lookup"><span data-stu-id="fff16-345">A hyphen</span></span>
    
-  <span data-ttu-id="fff16-346">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="fff16-346">Four digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="fff16-347">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fff16-347">Checksum</span></span>

<span data-ttu-id="fff16-348">Não</span><span class="sxs-lookup"><span data-stu-id="fff16-348">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="fff16-349">Definição</span><span class="sxs-lookup"><span data-stu-id="fff16-349">Definition</span></span>

<span data-ttu-id="fff16-350">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fff16-350">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fff16-351">A expressão `Regex_finland_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fff16-351">The regular expression  `Regex_finland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fff16-352">Uma palavra- `Keywords_finland_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fff16-352">A keyword from  `Keywords_finland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_driver's_license_number" />
          <Match idRef="Keywords_finland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fff16-353">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fff16-353">Keywords</span></span>

<span data-ttu-id="fff16-354">| |</span><span class="sxs-lookup"><span data-stu-id="fff16-354"></span></span>
|<span data-ttu-id="fff16-355">**Keywords_finland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="fff16-355">**Keywords_finland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="fff16-356">distribuição</span><span class="sxs-lookup"><span data-stu-id="fff16-356">dl#</span></span>  <br/> <span data-ttu-id="fff16-357">driver license</span><span class="sxs-lookup"><span data-stu-id="fff16-357">driver license</span></span>  <br/> <span data-ttu-id="fff16-358">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-358">driver license number</span></span>  <br/> <span data-ttu-id="fff16-359">licença de driver</span><span class="sxs-lookup"><span data-stu-id="fff16-359">driver licence</span></span>  <br/> <span data-ttu-id="fff16-360">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="fff16-360">drivers lic.</span></span>  <br/> <span data-ttu-id="fff16-361">drivers license</span><span class="sxs-lookup"><span data-stu-id="fff16-361">drivers license</span></span>  <br/> <span data-ttu-id="fff16-362">drivers licence</span><span class="sxs-lookup"><span data-stu-id="fff16-362">drivers licence</span></span>  <br/> <span data-ttu-id="fff16-363">driver's license</span><span class="sxs-lookup"><span data-stu-id="fff16-363">driver's license</span></span>  <br/> <span data-ttu-id="fff16-364">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-364">driver's license number</span></span>  <br/> <span data-ttu-id="fff16-365">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="fff16-365">driver's licence number</span></span>  <br/> <span data-ttu-id="fff16-366">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="fff16-366">driving license number</span></span>  <br/> <span data-ttu-id="fff16-367">dlno #</span><span class="sxs-lookup"><span data-stu-id="fff16-367">dlno#</span></span>  <br/> <span data-ttu-id="fff16-368">ajokortti</span><span class="sxs-lookup"><span data-stu-id="fff16-368">ajokortti</span></span>  <br/> |
   
## <a name="france"></a><span data-ttu-id="fff16-369">França</span><span class="sxs-lookup"><span data-stu-id="fff16-369">France</span></span>

<span data-ttu-id="fff16-370">Para obter detalhes, consulte a seção "número da carteira de motorista do driver da França" em [o que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="fff16-370">For details, see the section "France Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="fff16-371">Alemanha</span><span class="sxs-lookup"><span data-stu-id="fff16-371">Germany</span></span>

<span data-ttu-id="fff16-372">Para obter detalhes, consulte a seção "número da carteira de motorista do driver alemão" em [o que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="fff16-372">For details, see the section "German Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="fff16-373">Grécia</span><span class="sxs-lookup"><span data-stu-id="fff16-373">Greece</span></span>

### <a name="format"></a><span data-ttu-id="fff16-374">Formatar</span><span class="sxs-lookup"><span data-stu-id="fff16-374">Format</span></span>

<span data-ttu-id="fff16-375">Nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="fff16-375">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fff16-376">Padrão</span><span class="sxs-lookup"><span data-stu-id="fff16-376">Pattern</span></span>

 <span data-ttu-id="fff16-377">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="fff16-377">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="fff16-378">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fff16-378">Checksum</span></span>

<span data-ttu-id="fff16-379">Não</span><span class="sxs-lookup"><span data-stu-id="fff16-379">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="fff16-380">Definição</span><span class="sxs-lookup"><span data-stu-id="fff16-380">Definition</span></span>

<span data-ttu-id="fff16-381">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fff16-381">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fff16-382">A expressão `Regex_greece_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fff16-382">The regular expression  `Regex_greece_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fff16-383">Uma palavra- `Keywords_greece_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fff16-383">A keyword from  `Keywords_greece_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_driver's_license_number" />
          <Match idRef="Keywords_greece_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fff16-384">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fff16-384">Keywords</span></span>

<span data-ttu-id="fff16-385">| |</span><span class="sxs-lookup"><span data-stu-id="fff16-385"></span></span>
|<span data-ttu-id="fff16-386">**Keywords_greece_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="fff16-386">**Keywords_greece_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="fff16-387">DlL</span><span class="sxs-lookup"><span data-stu-id="fff16-387">dlL#</span></span>  <br/> <span data-ttu-id="fff16-388">driver license</span><span class="sxs-lookup"><span data-stu-id="fff16-388">driver license</span></span>  <br/> <span data-ttu-id="fff16-389">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-389">driver license number</span></span>  <br/> <span data-ttu-id="fff16-390">licença de driver</span><span class="sxs-lookup"><span data-stu-id="fff16-390">driver licence</span></span>  <br/> <span data-ttu-id="fff16-391">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="fff16-391">drivers lic.</span></span>  <br/> <span data-ttu-id="fff16-392">drivers license</span><span class="sxs-lookup"><span data-stu-id="fff16-392">drivers license</span></span>  <br/> <span data-ttu-id="fff16-393">drivers licence</span><span class="sxs-lookup"><span data-stu-id="fff16-393">drivers licence</span></span>  <br/> <span data-ttu-id="fff16-394">driver's license</span><span class="sxs-lookup"><span data-stu-id="fff16-394">driver's license</span></span>  <br/> <span data-ttu-id="fff16-395">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-395">driver's license number</span></span>  <br/> <span data-ttu-id="fff16-396">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="fff16-396">driver's licence number</span></span>  <br/> <span data-ttu-id="fff16-397">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="fff16-397">driving license number</span></span>  <br/> <span data-ttu-id="fff16-398">dlno #</span><span class="sxs-lookup"><span data-stu-id="fff16-398">dlno#</span></span>  <br/> <span data-ttu-id="fff16-399">δεια οδήγησης</span><span class="sxs-lookup"><span data-stu-id="fff16-399">δεια οδήγησης</span></span>  <br/> <span data-ttu-id="fff16-400">AdeIa odigisis</span><span class="sxs-lookup"><span data-stu-id="fff16-400">Adeia odigisis</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="fff16-401">Hungria</span><span class="sxs-lookup"><span data-stu-id="fff16-401">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="fff16-402">Formatar</span><span class="sxs-lookup"><span data-stu-id="fff16-402">Format</span></span>

<span data-ttu-id="fff16-403">Duas letras seguidas por seis dígitos</span><span class="sxs-lookup"><span data-stu-id="fff16-403">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fff16-404">Padrão</span><span class="sxs-lookup"><span data-stu-id="fff16-404">Pattern</span></span>

<span data-ttu-id="fff16-405">Duas letras e seis dígitos:</span><span class="sxs-lookup"><span data-stu-id="fff16-405">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="fff16-406">Duas letras (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="fff16-406">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="fff16-407">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="fff16-407">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="fff16-408">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fff16-408">Checksum</span></span>

<span data-ttu-id="fff16-409">Não</span><span class="sxs-lookup"><span data-stu-id="fff16-409">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="fff16-410">Definição</span><span class="sxs-lookup"><span data-stu-id="fff16-410">Definition</span></span>

<span data-ttu-id="fff16-411">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fff16-411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fff16-412">A expressão `Regex_hungary_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fff16-412">The regular expression  `Regex_hungary_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fff16-413">Uma palavra- `Keywords_hungary_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fff16-413">A keyword from  `Keywords_hungary_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_driver's_license_number" />
          <Match idRef="Keywords_hungary_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fff16-414">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fff16-414">Keywords</span></span>

<span data-ttu-id="fff16-415">| |</span><span class="sxs-lookup"><span data-stu-id="fff16-415"></span></span>
|<span data-ttu-id="fff16-416">**Keywords_hungary_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="fff16-416">**Keywords_hungary_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="fff16-417">distribuição</span><span class="sxs-lookup"><span data-stu-id="fff16-417">dl#</span></span>  <br/> <span data-ttu-id="fff16-418">driver license</span><span class="sxs-lookup"><span data-stu-id="fff16-418">driver license</span></span>  <br/> <span data-ttu-id="fff16-419">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-419">driver license number</span></span>  <br/> <span data-ttu-id="fff16-420">licença de driver</span><span class="sxs-lookup"><span data-stu-id="fff16-420">driver licence</span></span>  <br/> <span data-ttu-id="fff16-421">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="fff16-421">drivers lic.</span></span>  <br/> <span data-ttu-id="fff16-422">drivers license</span><span class="sxs-lookup"><span data-stu-id="fff16-422">drivers license</span></span>  <br/> <span data-ttu-id="fff16-423">drivers licence</span><span class="sxs-lookup"><span data-stu-id="fff16-423">drivers licence</span></span>  <br/> <span data-ttu-id="fff16-424">driver's license</span><span class="sxs-lookup"><span data-stu-id="fff16-424">driver's license</span></span>  <br/> <span data-ttu-id="fff16-425">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-425">driver's license number</span></span>  <br/> <span data-ttu-id="fff16-426">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="fff16-426">driver's licence number</span></span>  <br/> <span data-ttu-id="fff16-427">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="fff16-427">driving license number</span></span>  <br/> <span data-ttu-id="fff16-428">dlno #</span><span class="sxs-lookup"><span data-stu-id="fff16-428">dlno#</span></span>  <br/> <span data-ttu-id="fff16-429">vezetoi engedely</span><span class="sxs-lookup"><span data-stu-id="fff16-429">vezetoi engedely</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="fff16-430">Irlanda</span><span class="sxs-lookup"><span data-stu-id="fff16-430">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="fff16-431">Formatar</span><span class="sxs-lookup"><span data-stu-id="fff16-431">Format</span></span>

<span data-ttu-id="fff16-432">Seis dígitos seguidos de quatro letras</span><span class="sxs-lookup"><span data-stu-id="fff16-432">Six digits followed by four letters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fff16-433">Padrão</span><span class="sxs-lookup"><span data-stu-id="fff16-433">Pattern</span></span>

<span data-ttu-id="fff16-434">Seis dígitos e quatro letras:</span><span class="sxs-lookup"><span data-stu-id="fff16-434">Six digits and four letters:</span></span>
  
- <span data-ttu-id="fff16-435">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="fff16-435">Six digits</span></span>
    
- <span data-ttu-id="fff16-436">Quatro letras (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="fff16-436">Four letters (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="fff16-437">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fff16-437">Checksum</span></span>

<span data-ttu-id="fff16-438">Não</span><span class="sxs-lookup"><span data-stu-id="fff16-438">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="fff16-439">Definição</span><span class="sxs-lookup"><span data-stu-id="fff16-439">Definition</span></span>

<span data-ttu-id="fff16-440">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fff16-440">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fff16-441">A expressão `Regex_ireland_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fff16-441">The regular expression  `Regex_ireland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fff16-442">Uma palavra- `Keywords_ireland_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fff16-442">A keyword from  `Keywords_ireland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_driver's_license_number" />
          <Match idRef="Keywords_ireland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fff16-443">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fff16-443">Keywords</span></span>

<span data-ttu-id="fff16-444">| |</span><span class="sxs-lookup"><span data-stu-id="fff16-444"></span></span>
|<span data-ttu-id="fff16-445">**Keywords_ireland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="fff16-445">**Keywords_ireland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="fff16-446">distribuição</span><span class="sxs-lookup"><span data-stu-id="fff16-446">dl#</span></span>  <br/> <span data-ttu-id="fff16-447">driver license</span><span class="sxs-lookup"><span data-stu-id="fff16-447">driver license</span></span>  <br/> <span data-ttu-id="fff16-448">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-448">driver license number</span></span>  <br/> <span data-ttu-id="fff16-449">licença de driver</span><span class="sxs-lookup"><span data-stu-id="fff16-449">driver licence</span></span>  <br/> <span data-ttu-id="fff16-450">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="fff16-450">drivers lic.</span></span>  <br/> <span data-ttu-id="fff16-451">drivers license</span><span class="sxs-lookup"><span data-stu-id="fff16-451">drivers license</span></span>  <br/> <span data-ttu-id="fff16-452">drivers licence</span><span class="sxs-lookup"><span data-stu-id="fff16-452">drivers licence</span></span>  <br/> <span data-ttu-id="fff16-453">driver's license</span><span class="sxs-lookup"><span data-stu-id="fff16-453">driver's license</span></span>  <br/> <span data-ttu-id="fff16-454">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-454">driver's license number</span></span>  <br/> <span data-ttu-id="fff16-455">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="fff16-455">driver's licence number</span></span>  <br/> <span data-ttu-id="fff16-456">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="fff16-456">driving license number</span></span>  <br/> <span data-ttu-id="fff16-457">dlno #</span><span class="sxs-lookup"><span data-stu-id="fff16-457">dlno#</span></span>  <br/> <span data-ttu-id="fff16-458">ceadúnas tiomána</span><span class="sxs-lookup"><span data-stu-id="fff16-458">ceadúnas tiomána</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="fff16-459">Itália</span><span class="sxs-lookup"><span data-stu-id="fff16-459">Italy</span></span>

<span data-ttu-id="fff16-460">Para obter detalhes, consulte a seção "número da carteira de motorista do driver da Itália" em [o que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="fff16-460">For details, see the section "Italy Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="latvia"></a><span data-ttu-id="fff16-461">Letônia</span><span class="sxs-lookup"><span data-stu-id="fff16-461">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="fff16-462">Formatar</span><span class="sxs-lookup"><span data-stu-id="fff16-462">Format</span></span>

<span data-ttu-id="fff16-463">Três letras seguidas por seis dígitos</span><span class="sxs-lookup"><span data-stu-id="fff16-463">Three letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fff16-464">Padrão</span><span class="sxs-lookup"><span data-stu-id="fff16-464">Pattern</span></span>

<span data-ttu-id="fff16-465">Três letras e seis dígitos:</span><span class="sxs-lookup"><span data-stu-id="fff16-465">Three letters and six digits:</span></span>
  
-  <span data-ttu-id="fff16-466">Três letras (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="fff16-466">Three letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="fff16-467">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="fff16-467">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="fff16-468">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fff16-468">Checksum</span></span>

<span data-ttu-id="fff16-469">Não</span><span class="sxs-lookup"><span data-stu-id="fff16-469">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="fff16-470">Definição</span><span class="sxs-lookup"><span data-stu-id="fff16-470">Definition</span></span>

<span data-ttu-id="fff16-471">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fff16-471">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fff16-472">A expressão `Regex_latvia_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fff16-472">The regular expression  `Regex_latvia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fff16-473">Uma palavra- `Keywords_latvia_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fff16-473">A keyword from  `Keywords_latvia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_driver's_license_number" />
          <Match idRef="Keywords_latvia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fff16-474">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fff16-474">Keywords</span></span>

<span data-ttu-id="fff16-475">| |</span><span class="sxs-lookup"><span data-stu-id="fff16-475"></span></span>
|<span data-ttu-id="fff16-476">**Keywords_latvia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="fff16-476">**Keywords_latvia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="fff16-477">distribuição</span><span class="sxs-lookup"><span data-stu-id="fff16-477">dl#</span></span>  <br/> <span data-ttu-id="fff16-478">driver license</span><span class="sxs-lookup"><span data-stu-id="fff16-478">driver license</span></span>  <br/> <span data-ttu-id="fff16-479">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-479">driver license number</span></span>  <br/> <span data-ttu-id="fff16-480">licença de driver</span><span class="sxs-lookup"><span data-stu-id="fff16-480">driver licence</span></span>  <br/> <span data-ttu-id="fff16-481">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="fff16-481">drivers lic.</span></span>  <br/> <span data-ttu-id="fff16-482">drivers license</span><span class="sxs-lookup"><span data-stu-id="fff16-482">drivers license</span></span>  <br/> <span data-ttu-id="fff16-483">drivers licence</span><span class="sxs-lookup"><span data-stu-id="fff16-483">drivers licence</span></span>  <br/> <span data-ttu-id="fff16-484">driver's license</span><span class="sxs-lookup"><span data-stu-id="fff16-484">driver's license</span></span>  <br/> <span data-ttu-id="fff16-485">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-485">driver's license number</span></span>  <br/> <span data-ttu-id="fff16-486">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="fff16-486">driver's licence number</span></span>  <br/> <span data-ttu-id="fff16-487">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="fff16-487">driving license number</span></span>  <br/> <span data-ttu-id="fff16-488">dlno #</span><span class="sxs-lookup"><span data-stu-id="fff16-488">dlno#</span></span>  <br/> <span data-ttu-id="fff16-489">autovadītāja apliecība</span><span class="sxs-lookup"><span data-stu-id="fff16-489">autovadītāja apliecība</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="fff16-490">Lituânia</span><span class="sxs-lookup"><span data-stu-id="fff16-490">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="fff16-491">Formatar</span><span class="sxs-lookup"><span data-stu-id="fff16-491">Format</span></span>

<span data-ttu-id="fff16-492">Oito dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="fff16-492">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fff16-493">Padrão</span><span class="sxs-lookup"><span data-stu-id="fff16-493">Pattern</span></span>

 <span data-ttu-id="fff16-494">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="fff16-494">Eight digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="fff16-495">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fff16-495">Checksum</span></span>

<span data-ttu-id="fff16-496">Não</span><span class="sxs-lookup"><span data-stu-id="fff16-496">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="fff16-497">Definição</span><span class="sxs-lookup"><span data-stu-id="fff16-497">Definition</span></span>

<span data-ttu-id="fff16-498">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fff16-498">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fff16-499">A expressão `Regex_lithuania_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fff16-499">The regular expression  `Regex_lithuania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fff16-500">Uma palavra- `Keywords_lithuania_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fff16-500">A keyword from  `Keywords_lithuania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_driver's_license_number" />
          <Match idRef="Keywords_lithuania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fff16-501">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fff16-501">Keywords</span></span>

<span data-ttu-id="fff16-502">| |</span><span class="sxs-lookup"><span data-stu-id="fff16-502"></span></span>
|<span data-ttu-id="fff16-503">**Keywords_lithuania_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="fff16-503">**Keywords_lithuania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="fff16-504">distribuição</span><span class="sxs-lookup"><span data-stu-id="fff16-504">dl#</span></span>  <br/> <span data-ttu-id="fff16-505">driver license</span><span class="sxs-lookup"><span data-stu-id="fff16-505">driver license</span></span>  <br/> <span data-ttu-id="fff16-506">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-506">driver license number</span></span>  <br/> <span data-ttu-id="fff16-507">licença de driver</span><span class="sxs-lookup"><span data-stu-id="fff16-507">driver licence</span></span>  <br/> <span data-ttu-id="fff16-508">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="fff16-508">drivers lic.</span></span>  <br/> <span data-ttu-id="fff16-509">drivers license</span><span class="sxs-lookup"><span data-stu-id="fff16-509">drivers license</span></span>  <br/> <span data-ttu-id="fff16-510">drivers licence</span><span class="sxs-lookup"><span data-stu-id="fff16-510">drivers licence</span></span>  <br/> <span data-ttu-id="fff16-511">driver's license</span><span class="sxs-lookup"><span data-stu-id="fff16-511">driver's license</span></span>  <br/> <span data-ttu-id="fff16-512">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-512">driver's license number</span></span>  <br/> <span data-ttu-id="fff16-513">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="fff16-513">driver's licence number</span></span>  <br/> <span data-ttu-id="fff16-514">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="fff16-514">driving license number</span></span>  <br/> <span data-ttu-id="fff16-515">dlno #</span><span class="sxs-lookup"><span data-stu-id="fff16-515">dlno#</span></span>  <br/> <span data-ttu-id="fff16-516">vairuotojo pažymėjimas</span><span class="sxs-lookup"><span data-stu-id="fff16-516">vairuotojo pažymėjimas</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="fff16-517">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="fff16-517">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="fff16-518">Formatar</span><span class="sxs-lookup"><span data-stu-id="fff16-518">Format</span></span>

<span data-ttu-id="fff16-519">Seis dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="fff16-519">Six digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fff16-520">Padrão</span><span class="sxs-lookup"><span data-stu-id="fff16-520">Pattern</span></span>

 <span data-ttu-id="fff16-521">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="fff16-521">Six digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="fff16-522">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fff16-522">Checksum</span></span>

<span data-ttu-id="fff16-523">Não</span><span class="sxs-lookup"><span data-stu-id="fff16-523">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="fff16-524">Definição</span><span class="sxs-lookup"><span data-stu-id="fff16-524">Definition</span></span>

<span data-ttu-id="fff16-525">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fff16-525">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fff16-526">A expressão `Regex_luxemburg_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fff16-526">The regular expression  `Regex_luxemburg_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fff16-527">Uma palavra- `Keywords_luxemburg_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fff16-527">A keyword from  `Keywords_luxemburg_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_driver's_license_number" />
          <Match idRef="Keywords_luxemburg_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fff16-528">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fff16-528">Keywords</span></span>

<span data-ttu-id="fff16-529">| |</span><span class="sxs-lookup"><span data-stu-id="fff16-529"></span></span>
|<span data-ttu-id="fff16-530">**Keywords_luxemburg_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="fff16-530">**Keywords_luxemburg_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="fff16-531">distribuição</span><span class="sxs-lookup"><span data-stu-id="fff16-531">dl#</span></span>  <br/> <span data-ttu-id="fff16-532">driver license</span><span class="sxs-lookup"><span data-stu-id="fff16-532">driver license</span></span>  <br/> <span data-ttu-id="fff16-533">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-533">driver license number</span></span>  <br/> <span data-ttu-id="fff16-534">licença de driver</span><span class="sxs-lookup"><span data-stu-id="fff16-534">driver licence</span></span>  <br/> <span data-ttu-id="fff16-535">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="fff16-535">drivers lic.</span></span>  <br/> <span data-ttu-id="fff16-536">drivers license</span><span class="sxs-lookup"><span data-stu-id="fff16-536">drivers license</span></span>  <br/> <span data-ttu-id="fff16-537">drivers licence</span><span class="sxs-lookup"><span data-stu-id="fff16-537">drivers licence</span></span>  <br/> <span data-ttu-id="fff16-538">driver's license</span><span class="sxs-lookup"><span data-stu-id="fff16-538">driver's license</span></span>  <br/> <span data-ttu-id="fff16-539">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-539">driver's license number</span></span>  <br/> <span data-ttu-id="fff16-540">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="fff16-540">driver's licence number</span></span>  <br/> <span data-ttu-id="fff16-541">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="fff16-541">driving license number</span></span>  <br/> <span data-ttu-id="fff16-542">dlno #</span><span class="sxs-lookup"><span data-stu-id="fff16-542">dlno#</span></span>  <br/> <span data-ttu-id="fff16-543">fahrerlaubnis</span><span class="sxs-lookup"><span data-stu-id="fff16-543">fahrerlaubnis</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="fff16-544">Malta</span><span class="sxs-lookup"><span data-stu-id="fff16-544">Malta</span></span>

### <a name="format"></a><span data-ttu-id="fff16-545">Formatar</span><span class="sxs-lookup"><span data-stu-id="fff16-545">Format</span></span>

<span data-ttu-id="fff16-546">Combinação de dois caracteres e seis dígitos no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="fff16-546">Combination of two characters and six digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fff16-547">Padrão</span><span class="sxs-lookup"><span data-stu-id="fff16-547">Pattern</span></span>

<span data-ttu-id="fff16-548">Combinação de dois caracteres e seis dígitos:</span><span class="sxs-lookup"><span data-stu-id="fff16-548">Combination of two characters and six digits:</span></span>
  
- <span data-ttu-id="fff16-549">Dois caracteres (dígitos ou letras, não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="fff16-549">Two characters (digits or letters, not case-sensitive)</span></span>
    
- <span data-ttu-id="fff16-550">Um espaço (opcional)</span><span class="sxs-lookup"><span data-stu-id="fff16-550">A space (optional)</span></span>
    
- <span data-ttu-id="fff16-551">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="fff16-551">Three digits</span></span>
    
- <span data-ttu-id="fff16-552">Um espaço (opcional)</span><span class="sxs-lookup"><span data-stu-id="fff16-552">A space (optional)</span></span>
    
- <span data-ttu-id="fff16-553">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="fff16-553">Three digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="fff16-554">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fff16-554">Checksum</span></span>

<span data-ttu-id="fff16-555">Não</span><span class="sxs-lookup"><span data-stu-id="fff16-555">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="fff16-556">Definição</span><span class="sxs-lookup"><span data-stu-id="fff16-556">Definition</span></span>

<span data-ttu-id="fff16-557">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fff16-557">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fff16-558">A expressão `Regex_malta_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fff16-558">The regular expression  `Regex_malta_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fff16-559">Uma palavra- `Keywords_malta_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fff16-559">A keyword from  `Keywords_malta_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
 <Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_driver's_license_number" />
          <Match idRef="Keywords_malta_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fff16-560">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fff16-560">Keywords</span></span>

<span data-ttu-id="fff16-561">| |</span><span class="sxs-lookup"><span data-stu-id="fff16-561"></span></span>
|<span data-ttu-id="fff16-562">**Keywords_malta_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="fff16-562">**Keywords_malta_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="fff16-563">distribuição</span><span class="sxs-lookup"><span data-stu-id="fff16-563">dl#</span></span>  <br/> <span data-ttu-id="fff16-564">driver license</span><span class="sxs-lookup"><span data-stu-id="fff16-564">driver license</span></span>  <br/> <span data-ttu-id="fff16-565">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-565">driver license number</span></span>  <br/> <span data-ttu-id="fff16-566">licença de driver</span><span class="sxs-lookup"><span data-stu-id="fff16-566">driver licence</span></span>  <br/> <span data-ttu-id="fff16-567">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="fff16-567">drivers lic.</span></span>  <br/> <span data-ttu-id="fff16-568">drivers license</span><span class="sxs-lookup"><span data-stu-id="fff16-568">drivers license</span></span>  <br/> <span data-ttu-id="fff16-569">drivers licence</span><span class="sxs-lookup"><span data-stu-id="fff16-569">drivers licence</span></span>  <br/> <span data-ttu-id="fff16-570">driver's license</span><span class="sxs-lookup"><span data-stu-id="fff16-570">driver's license</span></span>  <br/> <span data-ttu-id="fff16-571">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-571">driver's license number</span></span>  <br/> <span data-ttu-id="fff16-572">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="fff16-572">driver's licence number</span></span>  <br/> <span data-ttu-id="fff16-573">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="fff16-573">driving license number</span></span>  <br/> <span data-ttu-id="fff16-574">dlno #</span><span class="sxs-lookup"><span data-stu-id="fff16-574">dlno#</span></span>  <br/> <span data-ttu-id="fff16-575">liċenzja tas-sewqan</span><span class="sxs-lookup"><span data-stu-id="fff16-575">liċenzja tas-sewqan</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="fff16-576">Países Baixos</span><span class="sxs-lookup"><span data-stu-id="fff16-576">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="fff16-577">Formatar</span><span class="sxs-lookup"><span data-stu-id="fff16-577">Format</span></span>

<span data-ttu-id="fff16-578">10 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="fff16-578">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fff16-579">Padrão</span><span class="sxs-lookup"><span data-stu-id="fff16-579">Pattern</span></span>

<span data-ttu-id="fff16-580">10 dígitos</span><span class="sxs-lookup"><span data-stu-id="fff16-580">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="fff16-581">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fff16-581">Checksum</span></span>

<span data-ttu-id="fff16-582">Não</span><span class="sxs-lookup"><span data-stu-id="fff16-582">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="fff16-583">Definição</span><span class="sxs-lookup"><span data-stu-id="fff16-583">Definition</span></span>

<span data-ttu-id="fff16-584">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fff16-584">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fff16-585">A expressão `Regex_netherlands_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fff16-585">The regular expression  `Regex_netherlands_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fff16-586">Uma palavra- `Keywords_netherlands_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fff16-586">A keyword from  `Keywords_netherlands_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_driver's_license_number" />
          <Match idRef="Keywords_netherlands_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fff16-587">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fff16-587">Keywords</span></span>

<span data-ttu-id="fff16-588">| |</span><span class="sxs-lookup"><span data-stu-id="fff16-588"></span></span>
|<span data-ttu-id="fff16-589">**Keywords_netherlands_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="fff16-589">**Keywords_netherlands_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="fff16-590">distribuição</span><span class="sxs-lookup"><span data-stu-id="fff16-590">dl#</span></span>  <br/> <span data-ttu-id="fff16-591">driver license</span><span class="sxs-lookup"><span data-stu-id="fff16-591">driver license</span></span>  <br/> <span data-ttu-id="fff16-592">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-592">driver license number</span></span>  <br/> <span data-ttu-id="fff16-593">licença de driver</span><span class="sxs-lookup"><span data-stu-id="fff16-593">driver licence</span></span>  <br/> <span data-ttu-id="fff16-594">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="fff16-594">drivers lic.</span></span>  <br/> <span data-ttu-id="fff16-595">drivers license</span><span class="sxs-lookup"><span data-stu-id="fff16-595">drivers license</span></span>  <br/> <span data-ttu-id="fff16-596">drivers licence</span><span class="sxs-lookup"><span data-stu-id="fff16-596">drivers licence</span></span>  <br/> <span data-ttu-id="fff16-597">driver's license</span><span class="sxs-lookup"><span data-stu-id="fff16-597">driver's license</span></span>  <br/> <span data-ttu-id="fff16-598">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-598">driver's license number</span></span>  <br/> <span data-ttu-id="fff16-599">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="fff16-599">driver's licence number</span></span>  <br/> <span data-ttu-id="fff16-600">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="fff16-600">driving license number</span></span>  <br/> <span data-ttu-id="fff16-601">dlno #</span><span class="sxs-lookup"><span data-stu-id="fff16-601">dlno#</span></span>  <br/> <span data-ttu-id="fff16-602">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fff16-602">permis de conduire</span></span>  <br/> <span data-ttu-id="fff16-603">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="fff16-603">rijbewijs</span></span>  <br/> <span data-ttu-id="fff16-604">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="fff16-604">rijbewijsnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="fff16-605">Polônia</span><span class="sxs-lookup"><span data-stu-id="fff16-605">Poland</span></span>

### <a name="format"></a><span data-ttu-id="fff16-606">Formatar</span><span class="sxs-lookup"><span data-stu-id="fff16-606">Format</span></span>

<span data-ttu-id="fff16-607">14 dígitos contendo 2 barras</span><span class="sxs-lookup"><span data-stu-id="fff16-607">14 digits containing 2 forward slashes</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fff16-608">Padrão</span><span class="sxs-lookup"><span data-stu-id="fff16-608">Pattern</span></span>

<span data-ttu-id="fff16-609">14 dígitos e 2 barras de avanço:</span><span class="sxs-lookup"><span data-stu-id="fff16-609">14 digits and 2 forward slashes:</span></span>
  
-  <span data-ttu-id="fff16-610">Cinco dígitos</span><span class="sxs-lookup"><span data-stu-id="fff16-610">Five digits</span></span> 
    
- <span data-ttu-id="fff16-611">Uma barra</span><span class="sxs-lookup"><span data-stu-id="fff16-611">A forward slash</span></span>
    
- <span data-ttu-id="fff16-612">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="fff16-612">Two digits</span></span>
    
- <span data-ttu-id="fff16-613">Uma barra</span><span class="sxs-lookup"><span data-stu-id="fff16-613">A forward slash</span></span>
    
- <span data-ttu-id="fff16-614">Sete dígitos</span><span class="sxs-lookup"><span data-stu-id="fff16-614">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="fff16-615">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fff16-615">Checksum</span></span>

<span data-ttu-id="fff16-616">Não</span><span class="sxs-lookup"><span data-stu-id="fff16-616">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="fff16-617">Definição</span><span class="sxs-lookup"><span data-stu-id="fff16-617">Definition</span></span>

<span data-ttu-id="fff16-618">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fff16-618">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fff16-619">A expressão `Regex_poland_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fff16-619">The regular expression  `Regex_poland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fff16-620">Uma palavra- `Keywords_poland_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fff16-620">A keyword from  `Keywords_poland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_driver's_license_number" />
          <Match idRef="Keywords_poland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fff16-621">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fff16-621">Keywords</span></span>

<span data-ttu-id="fff16-622">| |</span><span class="sxs-lookup"><span data-stu-id="fff16-622"></span></span>
|<span data-ttu-id="fff16-623">**Keywords_poland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="fff16-623">**Keywords_poland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="fff16-624">distribuição</span><span class="sxs-lookup"><span data-stu-id="fff16-624">dl#</span></span>  <br/> <span data-ttu-id="fff16-625">driver license</span><span class="sxs-lookup"><span data-stu-id="fff16-625">driver license</span></span>  <br/> <span data-ttu-id="fff16-626">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-626">driver license number</span></span>  <br/> <span data-ttu-id="fff16-627">licença de driver</span><span class="sxs-lookup"><span data-stu-id="fff16-627">driver licence</span></span>  <br/> <span data-ttu-id="fff16-628">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="fff16-628">drivers lic.</span></span>  <br/> <span data-ttu-id="fff16-629">drivers license</span><span class="sxs-lookup"><span data-stu-id="fff16-629">drivers license</span></span>  <br/> <span data-ttu-id="fff16-630">drivers licence</span><span class="sxs-lookup"><span data-stu-id="fff16-630">drivers licence</span></span>  <br/> <span data-ttu-id="fff16-631">driver's license</span><span class="sxs-lookup"><span data-stu-id="fff16-631">driver's license</span></span>  <br/> <span data-ttu-id="fff16-632">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-632">driver's license number</span></span>  <br/> <span data-ttu-id="fff16-633">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="fff16-633">driver's licence number</span></span>  <br/> <span data-ttu-id="fff16-634">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="fff16-634">driving license number</span></span>  <br/> <span data-ttu-id="fff16-635">dlno #</span><span class="sxs-lookup"><span data-stu-id="fff16-635">dlno#</span></span>  <br/> <span data-ttu-id="fff16-636">Prawo jazdy</span><span class="sxs-lookup"><span data-stu-id="fff16-636">prawo jazdy</span></span>  <br/> |
   
## <a name="portugal"></a><span data-ttu-id="fff16-637">Portugal</span><span class="sxs-lookup"><span data-stu-id="fff16-637">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="fff16-638">Formatar</span><span class="sxs-lookup"><span data-stu-id="fff16-638">Format</span></span>

<span data-ttu-id="fff16-639">Duas letras seguidas por sete números no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="fff16-639">Two letters followed by a seven numbers in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fff16-640">Padrão</span><span class="sxs-lookup"><span data-stu-id="fff16-640">Pattern</span></span>

<span data-ttu-id="fff16-641">Duas letras seguidas por sete números com caracteres especiais:</span><span class="sxs-lookup"><span data-stu-id="fff16-641">Two letters followed by seven numbers with special characters:</span></span>
  
-  <span data-ttu-id="fff16-642">Duas letras (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="fff16-642">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="fff16-643">Um hífen</span><span class="sxs-lookup"><span data-stu-id="fff16-643">A hyphen</span></span>
    
- <span data-ttu-id="fff16-644">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="fff16-644">Six digits</span></span>
    
- <span data-ttu-id="fff16-645">Um espaço</span><span class="sxs-lookup"><span data-stu-id="fff16-645">A space</span></span>
    
- <span data-ttu-id="fff16-646">Um dígito</span><span class="sxs-lookup"><span data-stu-id="fff16-646">One digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="fff16-647">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fff16-647">Checksum</span></span>

<span data-ttu-id="fff16-648">Não</span><span class="sxs-lookup"><span data-stu-id="fff16-648">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="fff16-649">Definição</span><span class="sxs-lookup"><span data-stu-id="fff16-649">Definition</span></span>

<span data-ttu-id="fff16-650">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fff16-650">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fff16-651">A expressão `Regex_portugal_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fff16-651">The regular expression  `Regex_portugal_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fff16-652">Uma palavra- `Keywords_portugal_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fff16-652">A keyword from  `Keywords_portugal_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_driver's_license_number" />
          <Match idRef="Keywords_portugal_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fff16-653">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fff16-653">Keywords</span></span>

<span data-ttu-id="fff16-654">| |</span><span class="sxs-lookup"><span data-stu-id="fff16-654"></span></span>
|<span data-ttu-id="fff16-655">**Keywords_portugal_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="fff16-655">**Keywords_portugal_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="fff16-656">distribuição</span><span class="sxs-lookup"><span data-stu-id="fff16-656">dl#</span></span>  <br/> <span data-ttu-id="fff16-657">driver license</span><span class="sxs-lookup"><span data-stu-id="fff16-657">driver license</span></span>  <br/> <span data-ttu-id="fff16-658">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-658">driver license number</span></span>  <br/> <span data-ttu-id="fff16-659">licença de driver</span><span class="sxs-lookup"><span data-stu-id="fff16-659">driver licence</span></span>  <br/> <span data-ttu-id="fff16-660">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="fff16-660">drivers lic.</span></span>  <br/> <span data-ttu-id="fff16-661">drivers license</span><span class="sxs-lookup"><span data-stu-id="fff16-661">drivers license</span></span>  <br/> <span data-ttu-id="fff16-662">drivers licence</span><span class="sxs-lookup"><span data-stu-id="fff16-662">drivers licence</span></span>  <br/> <span data-ttu-id="fff16-663">driver's license</span><span class="sxs-lookup"><span data-stu-id="fff16-663">driver's license</span></span>  <br/> <span data-ttu-id="fff16-664">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-664">driver's license number</span></span>  <br/> <span data-ttu-id="fff16-665">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="fff16-665">driver's licence number</span></span>  <br/> <span data-ttu-id="fff16-666">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="fff16-666">driving license number</span></span>  <br/> <span data-ttu-id="fff16-667">dlno #</span><span class="sxs-lookup"><span data-stu-id="fff16-667">dlno#</span></span>  <br/> <span data-ttu-id="fff16-668">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-668">carteira de motorista</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="fff16-669">Romênia</span><span class="sxs-lookup"><span data-stu-id="fff16-669">Romania</span></span>

### <a name="format"></a><span data-ttu-id="fff16-670">Formatar</span><span class="sxs-lookup"><span data-stu-id="fff16-670">Format</span></span>

<span data-ttu-id="fff16-671">Um caractere seguido por oito dígitos</span><span class="sxs-lookup"><span data-stu-id="fff16-671">One character followed by eight digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fff16-672">Padrão</span><span class="sxs-lookup"><span data-stu-id="fff16-672">Pattern</span></span>

<span data-ttu-id="fff16-673">Um caractere seguido por oito dígitos:</span><span class="sxs-lookup"><span data-stu-id="fff16-673">One character followed by eight digits:</span></span>
  
-  <span data-ttu-id="fff16-674">Uma letra (não diferencia maiúsculas de minúsculas) ou dígito</span><span class="sxs-lookup"><span data-stu-id="fff16-674">One letter (not case-sensitive) or digit</span></span> 
    
- <span data-ttu-id="fff16-675">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="fff16-675">Eight digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="fff16-676">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fff16-676">Checksum</span></span>

<span data-ttu-id="fff16-677">Não</span><span class="sxs-lookup"><span data-stu-id="fff16-677">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="fff16-678">Definição</span><span class="sxs-lookup"><span data-stu-id="fff16-678">Definition</span></span>

<span data-ttu-id="fff16-679">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fff16-679">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fff16-680">A expressão `Regex_romania_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fff16-680">The regular expression  `Regex_romania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fff16-681">Uma palavra- `Keywords_romania_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fff16-681">A keyword from  `Keywords_romania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_driver's_license_number" />
          <Match idRef="Keywords_romania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fff16-682">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fff16-682">Keywords</span></span>

<span data-ttu-id="fff16-683">| |</span><span class="sxs-lookup"><span data-stu-id="fff16-683"></span></span>
|<span data-ttu-id="fff16-684">**Keywords_romania_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="fff16-684">**Keywords_romania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="fff16-685">distribuição</span><span class="sxs-lookup"><span data-stu-id="fff16-685">dl#</span></span>  <br/> <span data-ttu-id="fff16-686">driver license</span><span class="sxs-lookup"><span data-stu-id="fff16-686">driver license</span></span>  <br/> <span data-ttu-id="fff16-687">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-687">driver license number</span></span>  <br/> <span data-ttu-id="fff16-688">licença de driver</span><span class="sxs-lookup"><span data-stu-id="fff16-688">driver licence</span></span>  <br/> <span data-ttu-id="fff16-689">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="fff16-689">drivers lic.</span></span>  <br/> <span data-ttu-id="fff16-690">drivers license</span><span class="sxs-lookup"><span data-stu-id="fff16-690">drivers license</span></span>  <br/> <span data-ttu-id="fff16-691">drivers licence</span><span class="sxs-lookup"><span data-stu-id="fff16-691">drivers licence</span></span>  <br/> <span data-ttu-id="fff16-692">driver's license</span><span class="sxs-lookup"><span data-stu-id="fff16-692">driver's license</span></span>  <br/> <span data-ttu-id="fff16-693">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-693">driver's license number</span></span>  <br/> <span data-ttu-id="fff16-694">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="fff16-694">driver's licence number</span></span>  <br/> <span data-ttu-id="fff16-695">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="fff16-695">driving license number</span></span>  <br/> <span data-ttu-id="fff16-696">dlno #</span><span class="sxs-lookup"><span data-stu-id="fff16-696">dlno#</span></span>  <br/> <span data-ttu-id="fff16-697">permé de conducere</span><span class="sxs-lookup"><span data-stu-id="fff16-697">permis de conducere</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="fff16-698">Eslováquia</span><span class="sxs-lookup"><span data-stu-id="fff16-698">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="fff16-699">Formatar</span><span class="sxs-lookup"><span data-stu-id="fff16-699">Format</span></span>

<span data-ttu-id="fff16-700">Um caractere seguido por sete dígitos</span><span class="sxs-lookup"><span data-stu-id="fff16-700">One character followed by seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fff16-701">Padrão</span><span class="sxs-lookup"><span data-stu-id="fff16-701">Pattern</span></span>

<span data-ttu-id="fff16-702">Um caractere seguido por sete dígitos</span><span class="sxs-lookup"><span data-stu-id="fff16-702">One character followed by seven digits</span></span>
  
- <span data-ttu-id="fff16-703">Uma letra (não diferencia maiúsculas de minúsculas) ou dígito</span><span class="sxs-lookup"><span data-stu-id="fff16-703">One letter (not case-sensitive) or digit</span></span>
    
-  <span data-ttu-id="fff16-704">Sete dígitos</span><span class="sxs-lookup"><span data-stu-id="fff16-704">Seven digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="fff16-705">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fff16-705">Checksum</span></span>

<span data-ttu-id="fff16-706">Não</span><span class="sxs-lookup"><span data-stu-id="fff16-706">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="fff16-707">Definição</span><span class="sxs-lookup"><span data-stu-id="fff16-707">Definition</span></span>

<span data-ttu-id="fff16-708">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fff16-708">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fff16-709">A expressão `Regex_slovakia_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fff16-709">The regular expression  `Regex_slovakia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fff16-710">Uma palavra- `Keywords_slovakia_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fff16-710">A keyword from  `Keywords_slovakia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovaknia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovakia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fff16-711">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fff16-711">Keywords</span></span>

<span data-ttu-id="fff16-712">| |</span><span class="sxs-lookup"><span data-stu-id="fff16-712"></span></span>
|<span data-ttu-id="fff16-713">**Keywords_slovakia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="fff16-713">**Keywords_slovakia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="fff16-714">distribuição</span><span class="sxs-lookup"><span data-stu-id="fff16-714">dl#</span></span>  <br/> <span data-ttu-id="fff16-715">driver license</span><span class="sxs-lookup"><span data-stu-id="fff16-715">driver license</span></span>  <br/> <span data-ttu-id="fff16-716">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-716">driver license number</span></span>  <br/> <span data-ttu-id="fff16-717">licença de driver</span><span class="sxs-lookup"><span data-stu-id="fff16-717">driver licence</span></span>  <br/> <span data-ttu-id="fff16-718">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="fff16-718">drivers lic.</span></span>  <br/> <span data-ttu-id="fff16-719">drivers license</span><span class="sxs-lookup"><span data-stu-id="fff16-719">drivers license</span></span>  <br/> <span data-ttu-id="fff16-720">drivers licence</span><span class="sxs-lookup"><span data-stu-id="fff16-720">drivers licence</span></span>  <br/> <span data-ttu-id="fff16-721">driver's license</span><span class="sxs-lookup"><span data-stu-id="fff16-721">driver's license</span></span>  <br/> <span data-ttu-id="fff16-722">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-722">driver's license number</span></span>  <br/> <span data-ttu-id="fff16-723">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="fff16-723">driver's licence number</span></span>  <br/> <span data-ttu-id="fff16-724">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="fff16-724">driving license number</span></span>  <br/> <span data-ttu-id="fff16-725">dlno #</span><span class="sxs-lookup"><span data-stu-id="fff16-725">dlno#</span></span>  <br/> <span data-ttu-id="fff16-726">vodičský preukaz</span><span class="sxs-lookup"><span data-stu-id="fff16-726">vodičský preukaz</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="fff16-727">Eslovênia</span><span class="sxs-lookup"><span data-stu-id="fff16-727">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="fff16-728">Formatar</span><span class="sxs-lookup"><span data-stu-id="fff16-728">Format</span></span>

<span data-ttu-id="fff16-729">Nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="fff16-729">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fff16-730">Padrão</span><span class="sxs-lookup"><span data-stu-id="fff16-730">Pattern</span></span>

<span data-ttu-id="fff16-731">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="fff16-731">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="fff16-732">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fff16-732">Checksum</span></span>

<span data-ttu-id="fff16-733">Não</span><span class="sxs-lookup"><span data-stu-id="fff16-733">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="fff16-734">Definição</span><span class="sxs-lookup"><span data-stu-id="fff16-734">Definition</span></span>

<span data-ttu-id="fff16-735">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fff16-735">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fff16-736">A expressão `Regex_slovenia_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fff16-736">The regular expression  `Regex_slovenia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fff16-737">Uma palavra- `Keywords_slovenia_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fff16-737">A keyword from  `Keywords_slovenia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovenia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fff16-738">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fff16-738">Keywords</span></span>

<span data-ttu-id="fff16-739">| |</span><span class="sxs-lookup"><span data-stu-id="fff16-739"></span></span>
|<span data-ttu-id="fff16-740">**Keywords_slovenia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="fff16-740">**Keywords_slovenia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="fff16-741">distribuição</span><span class="sxs-lookup"><span data-stu-id="fff16-741">dl#</span></span>  <br/> <span data-ttu-id="fff16-742">driver license</span><span class="sxs-lookup"><span data-stu-id="fff16-742">driver license</span></span>  <br/> <span data-ttu-id="fff16-743">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-743">driver license number</span></span>  <br/> <span data-ttu-id="fff16-744">licença de driver</span><span class="sxs-lookup"><span data-stu-id="fff16-744">driver licence</span></span>  <br/> <span data-ttu-id="fff16-745">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="fff16-745">drivers lic.</span></span>  <br/> <span data-ttu-id="fff16-746">drivers license</span><span class="sxs-lookup"><span data-stu-id="fff16-746">drivers license</span></span>  <br/> <span data-ttu-id="fff16-747">drivers licence</span><span class="sxs-lookup"><span data-stu-id="fff16-747">drivers licence</span></span>  <br/> <span data-ttu-id="fff16-748">driver's license</span><span class="sxs-lookup"><span data-stu-id="fff16-748">driver's license</span></span>  <br/> <span data-ttu-id="fff16-749">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-749">driver's license number</span></span>  <br/> <span data-ttu-id="fff16-750">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="fff16-750">driver's licence number</span></span>  <br/> <span data-ttu-id="fff16-751">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="fff16-751">driving license number</span></span>  <br/> <span data-ttu-id="fff16-752">dlno #</span><span class="sxs-lookup"><span data-stu-id="fff16-752">dlno#</span></span>  <br/> <span data-ttu-id="fff16-753">vozniško dovoljenje</span><span class="sxs-lookup"><span data-stu-id="fff16-753">vozniško dovoljenje</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="fff16-754">Espanha</span><span class="sxs-lookup"><span data-stu-id="fff16-754">Spain</span></span>

### <a name="format"></a><span data-ttu-id="fff16-755">Formatar</span><span class="sxs-lookup"><span data-stu-id="fff16-755">Format</span></span>

<span data-ttu-id="fff16-756">Oito dígitos seguidos de um caractere</span><span class="sxs-lookup"><span data-stu-id="fff16-756">Eight digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fff16-757">Padrão</span><span class="sxs-lookup"><span data-stu-id="fff16-757">Pattern</span></span>

<span data-ttu-id="fff16-758">Oito dígitos seguidos de um caractere:</span><span class="sxs-lookup"><span data-stu-id="fff16-758">Eight digits followed by one character:</span></span>
  
-  <span data-ttu-id="fff16-759">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="fff16-759">Eight digits</span></span> 
    
- <span data-ttu-id="fff16-760">Um dígito ou letra (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="fff16-760">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="fff16-761">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fff16-761">Checksum</span></span>

<span data-ttu-id="fff16-762">Sim</span><span class="sxs-lookup"><span data-stu-id="fff16-762">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="fff16-763">Definição</span><span class="sxs-lookup"><span data-stu-id="fff16-763">Definition</span></span>

<span data-ttu-id="fff16-764">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fff16-764">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fff16-765">A função `Func_spain_eu_driver's_license_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fff16-765">The function  `Func_spain_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fff16-766">Uma palavra- `Keywords_spain_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fff16-766">A keyword from  `Keywords_spain_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_driver's_license_number" />
          <Match idRef="Keywords_spain_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fff16-767">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fff16-767">Keywords</span></span>

<span data-ttu-id="fff16-768">| |</span><span class="sxs-lookup"><span data-stu-id="fff16-768"></span></span>
|<span data-ttu-id="fff16-769">**Keywords_spain_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="fff16-769">**Keywords_spain_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="fff16-770">dlno #</span><span class="sxs-lookup"><span data-stu-id="fff16-770">dlno#</span></span>  <br/> <span data-ttu-id="fff16-771">distribuição</span><span class="sxs-lookup"><span data-stu-id="fff16-771">dl#</span></span>  <br/> <span data-ttu-id="fff16-772">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="fff16-772">drivers lic.</span></span>  <br/> <span data-ttu-id="fff16-773">licença de driver</span><span class="sxs-lookup"><span data-stu-id="fff16-773">driver licence</span></span>  <br/> <span data-ttu-id="fff16-774">driver license</span><span class="sxs-lookup"><span data-stu-id="fff16-774">driver license</span></span>  <br/> <span data-ttu-id="fff16-775">drivers licence</span><span class="sxs-lookup"><span data-stu-id="fff16-775">drivers licence</span></span>  <br/> <span data-ttu-id="fff16-776">drivers license</span><span class="sxs-lookup"><span data-stu-id="fff16-776">drivers license</span></span>  <br/> <span data-ttu-id="fff16-777">driver's licence</span><span class="sxs-lookup"><span data-stu-id="fff16-777">driver's licence</span></span>  <br/> <span data-ttu-id="fff16-778">driver's license</span><span class="sxs-lookup"><span data-stu-id="fff16-778">driver's license</span></span>  <br/> <span data-ttu-id="fff16-779">driving licence</span><span class="sxs-lookup"><span data-stu-id="fff16-779">driving licence</span></span>  <br/> <span data-ttu-id="fff16-780">driving licence</span><span class="sxs-lookup"><span data-stu-id="fff16-780">driving license</span></span>  <br/> <span data-ttu-id="fff16-781">número de licença de driver</span><span class="sxs-lookup"><span data-stu-id="fff16-781">driver licence number</span></span>  <br/> <span data-ttu-id="fff16-782">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-782">driver license number</span></span>  <br/> <span data-ttu-id="fff16-783">número de licença de drivers</span><span class="sxs-lookup"><span data-stu-id="fff16-783">drivers licence number</span></span>  <br/> <span data-ttu-id="fff16-784">número de licença de drivers</span><span class="sxs-lookup"><span data-stu-id="fff16-784">drivers license number</span></span>  <br/> <span data-ttu-id="fff16-785">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="fff16-785">driver's licence number</span></span>  <br/> <span data-ttu-id="fff16-786">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-786">driver's license number</span></span>  <br/> <span data-ttu-id="fff16-787">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="fff16-787">driving licence number</span></span>  <br/> <span data-ttu-id="fff16-788">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="fff16-788">driving license number</span></span>  <br/> <span data-ttu-id="fff16-789">permissão de condução</span><span class="sxs-lookup"><span data-stu-id="fff16-789">driving permit</span></span>  <br/> <span data-ttu-id="fff16-790">número de permissão de dirigir</span><span class="sxs-lookup"><span data-stu-id="fff16-790">driving permit number</span></span>  <br/> <span data-ttu-id="fff16-791">permiso de conducción</span><span class="sxs-lookup"><span data-stu-id="fff16-791">permiso de conducción</span></span>  <br/> <span data-ttu-id="fff16-792">permiso conducción</span><span class="sxs-lookup"><span data-stu-id="fff16-792">permiso conducción</span></span>  <br/> <span data-ttu-id="fff16-793">número licencia conducir</span><span class="sxs-lookup"><span data-stu-id="fff16-793">número licencia conducir</span></span>  <br/> <span data-ttu-id="fff16-794">número de Carnet de conducir</span><span class="sxs-lookup"><span data-stu-id="fff16-794">número de carnet de conducir</span></span>  <br/> <span data-ttu-id="fff16-795">número Carnet conducir</span><span class="sxs-lookup"><span data-stu-id="fff16-795">número carnet conducir</span></span>  <br/> <span data-ttu-id="fff16-796">licencia conducir</span><span class="sxs-lookup"><span data-stu-id="fff16-796">licencia conducir</span></span>  <br/> <span data-ttu-id="fff16-797">número de permiso de conducir</span><span class="sxs-lookup"><span data-stu-id="fff16-797">número de permiso de conducir</span></span>  <br/> <span data-ttu-id="fff16-798">número de permiso conducir</span><span class="sxs-lookup"><span data-stu-id="fff16-798">número de permiso conducir</span></span>  <br/> <span data-ttu-id="fff16-799">número permiso conducir</span><span class="sxs-lookup"><span data-stu-id="fff16-799">número permiso conducir</span></span>  <br/> <span data-ttu-id="fff16-800">permiso conducir</span><span class="sxs-lookup"><span data-stu-id="fff16-800">permiso conducir</span></span>  <br/> <span data-ttu-id="fff16-801">licencia de manejo</span><span class="sxs-lookup"><span data-stu-id="fff16-801">licencia de manejo</span></span>  <br/> <span data-ttu-id="fff16-802">El Carnet de conducir</span><span class="sxs-lookup"><span data-stu-id="fff16-802">el carnet de conducir</span></span>  <br/> <span data-ttu-id="fff16-803">Carnet conducir</span><span class="sxs-lookup"><span data-stu-id="fff16-803">carnet conducir</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="fff16-804">Suécia</span><span class="sxs-lookup"><span data-stu-id="fff16-804">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="fff16-805">Formatar</span><span class="sxs-lookup"><span data-stu-id="fff16-805">Format</span></span>

<span data-ttu-id="fff16-806">Dez dígitos contendo um hífen</span><span class="sxs-lookup"><span data-stu-id="fff16-806">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="fff16-807">Padrão</span><span class="sxs-lookup"><span data-stu-id="fff16-807">Pattern</span></span>

<span data-ttu-id="fff16-808">Dez dígitos contendo um hífen:</span><span class="sxs-lookup"><span data-stu-id="fff16-808">Ten digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="fff16-809">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="fff16-809">Six digits</span></span> 
    
- <span data-ttu-id="fff16-810">Um hífen</span><span class="sxs-lookup"><span data-stu-id="fff16-810">A hyphen</span></span>
    
- <span data-ttu-id="fff16-811">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="fff16-811">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="fff16-812">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="fff16-812">Checksum</span></span>

<span data-ttu-id="fff16-813">Não</span><span class="sxs-lookup"><span data-stu-id="fff16-813">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="fff16-814">Definição</span><span class="sxs-lookup"><span data-stu-id="fff16-814">Definition</span></span>

<span data-ttu-id="fff16-815">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="fff16-815">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="fff16-816">A expressão `Regex_sweden_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="fff16-816">The regular expression  `Regex_sweden_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="fff16-817">Uma palavra- `Keywords_sweden_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fff16-817">A keyword from  `Keywords_sweden_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_driver's_license_number" />
          <Match idRef="Keywords_sweden_eu_driver's_license_number" />
        </Pattern>
</Entity> 
```

### <a name="keywords"></a><span data-ttu-id="fff16-818">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="fff16-818">Keywords</span></span>

<span data-ttu-id="fff16-819">| |</span><span class="sxs-lookup"><span data-stu-id="fff16-819"></span></span>
|<span data-ttu-id="fff16-820">**Keywords_sweden_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="fff16-820">**Keywords_sweden_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="fff16-821">distribuição</span><span class="sxs-lookup"><span data-stu-id="fff16-821">dl#</span></span>  <br/> <span data-ttu-id="fff16-822">driver license</span><span class="sxs-lookup"><span data-stu-id="fff16-822">driver license</span></span>  <br/> <span data-ttu-id="fff16-823">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-823">driver license number</span></span>  <br/> <span data-ttu-id="fff16-824">licença de driver</span><span class="sxs-lookup"><span data-stu-id="fff16-824">driver licence</span></span>  <br/> <span data-ttu-id="fff16-825">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="fff16-825">drivers lic.</span></span>  <br/> <span data-ttu-id="fff16-826">drivers license</span><span class="sxs-lookup"><span data-stu-id="fff16-826">drivers license</span></span>  <br/> <span data-ttu-id="fff16-827">drivers licence</span><span class="sxs-lookup"><span data-stu-id="fff16-827">drivers licence</span></span>  <br/> <span data-ttu-id="fff16-828">driver's license</span><span class="sxs-lookup"><span data-stu-id="fff16-828">driver's license</span></span>  <br/> <span data-ttu-id="fff16-829">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="fff16-829">driver's license number</span></span>  <br/> <span data-ttu-id="fff16-830">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="fff16-830">driver's licence number</span></span>  <br/> <span data-ttu-id="fff16-831">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="fff16-831">driving license number</span></span>  <br/> <span data-ttu-id="fff16-832">dlno #</span><span class="sxs-lookup"><span data-stu-id="fff16-832">dlno#</span></span>  <br/> <span data-ttu-id="fff16-833">körkort</span><span class="sxs-lookup"><span data-stu-id="fff16-833">körkort</span></span>  <br/> |
   
## <a name="uk"></a><span data-ttu-id="fff16-834">Reino Unido</span><span class="sxs-lookup"><span data-stu-id="fff16-834">UK</span></span>

<span data-ttu-id="fff16-835">Para obter detalhes, consulte a seção "Reino Unido</span><span class="sxs-lookup"><span data-stu-id="fff16-835">For details, see the section "U.K.</span></span> <span data-ttu-id="fff16-836">Número da carteira de motorista "em [que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="fff16-836">Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fff16-837">Confira também</span><span class="sxs-lookup"><span data-stu-id="fff16-837">See also</span></span>

[<span data-ttu-id="fff16-838">O que os tipos de informações confidenciais procuram</span><span class="sxs-lookup"><span data-stu-id="fff16-838">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)


---
title: Número da carteira de motorista da UE
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: c3923cd3-ec84-435f-bf41-cadc37996a4b
description: Este tópico mostra o que uma política de prevenção de perda de dados (DLP) procura quando detecta o tipo de informação confidencial do número de licença do driver da UE. Esse tipo de informação confidencial define diferentes padrões, palavras-chave e outras evidências para cada país.
ms.openlocfilehash: 86be7b52aed7581fd62ab595ac2c4b63ab33aab3
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217741"
---
# <a name="eu-drivers-license-number"></a><span data-ttu-id="a2283-104">Número da carteira de motorista da UE</span><span class="sxs-lookup"><span data-stu-id="a2283-104">EU Driver's License Number</span></span>

<span data-ttu-id="a2283-p102">Este tópico mostra o que uma política de prevenção de perda de dados (DLP) procura quando detecta o tipo de informação confidencial do número de licença do driver da UE. Esse tipo de informação confidencial define diferentes padrões, palavras-chave e outras evidências para cada país.</span><span class="sxs-lookup"><span data-stu-id="a2283-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Driver's License Number sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="a2283-107">Áustria</span><span class="sxs-lookup"><span data-stu-id="a2283-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="a2283-108">Formato</span><span class="sxs-lookup"><span data-stu-id="a2283-108">Format</span></span>

<span data-ttu-id="a2283-109">Oito dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="a2283-109">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2283-110">Padrão</span><span class="sxs-lookup"><span data-stu-id="a2283-110">Pattern</span></span>

<span data-ttu-id="a2283-111">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="a2283-111">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a2283-112">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a2283-112">Checksum</span></span>

<span data-ttu-id="a2283-113">Não</span><span class="sxs-lookup"><span data-stu-id="a2283-113">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2283-114">Definição</span><span class="sxs-lookup"><span data-stu-id="a2283-114">Definition</span></span>

<span data-ttu-id="a2283-115">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a2283-115">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2283-116">A expressão `Regex_austria_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a2283-116">The regular expression  `Regex_austria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2283-117">Uma palavra- `Keywords_austria_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="a2283-117">A keyword from  `Keywords_austria_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_driver's_license_number" />
          <Match idRef="Keywords_austria_eu_driver's_license_number" />
        </Pattern>
    </Entity>

```

### <a name="keywords"></a><span data-ttu-id="a2283-118">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a2283-118">Keywords</span></span>

<span data-ttu-id="a2283-119">| |</span><span class="sxs-lookup"><span data-stu-id="a2283-119"></span></span>
|<span data-ttu-id="a2283-120">**Keywords_austria_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a2283-120">**Keywords_austria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2283-121">distribuição</span><span class="sxs-lookup"><span data-stu-id="a2283-121">dl#</span></span>  <br/> <span data-ttu-id="a2283-122">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-122">driver license</span></span>  <br/> <span data-ttu-id="a2283-123">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-123">driver license number</span></span>  <br/> <span data-ttu-id="a2283-124">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-124">driver licence</span></span>  <br/> <span data-ttu-id="a2283-125">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="a2283-125">drivers lic.</span></span>  <br/> <span data-ttu-id="a2283-126">licença de drivers</span><span class="sxs-lookup"><span data-stu-id="a2283-126">drivers license</span></span>  <br/> <span data-ttu-id="a2283-127">licença do driver</span><span class="sxs-lookup"><span data-stu-id="a2283-127">driver's licence</span></span>  <br/> <span data-ttu-id="a2283-128">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-128">driver's license</span></span>  <br/> <span data-ttu-id="a2283-129">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-129">driver's license number</span></span>  <br/> <span data-ttu-id="a2283-130">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="a2283-130">driver's licence number</span></span>  <br/>  <span data-ttu-id="a2283-131">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="a2283-131">driving license number</span></span>  <br/> <span data-ttu-id="a2283-132">dlno #</span><span class="sxs-lookup"><span data-stu-id="a2283-132">dlno#</span></span>  <br/> <span data-ttu-id="a2283-133">fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="a2283-133">fuhrerschein</span></span>  <br/> <span data-ttu-id="a2283-134">fuhrerschein Republik Osterreich</span><span class="sxs-lookup"><span data-stu-id="a2283-134">fuhrerschein republik osterreich</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="a2283-135">Bélgica</span><span class="sxs-lookup"><span data-stu-id="a2283-135">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="a2283-136">Formato</span><span class="sxs-lookup"><span data-stu-id="a2283-136">Format</span></span>

<span data-ttu-id="a2283-137">10 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="a2283-137">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2283-138">Padrão</span><span class="sxs-lookup"><span data-stu-id="a2283-138">Pattern</span></span>

<span data-ttu-id="a2283-139">10 dígitos</span><span class="sxs-lookup"><span data-stu-id="a2283-139">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a2283-140">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a2283-140">Checksum</span></span>

<span data-ttu-id="a2283-141">Não</span><span class="sxs-lookup"><span data-stu-id="a2283-141">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2283-142">Definição</span><span class="sxs-lookup"><span data-stu-id="a2283-142">Definition</span></span>

<span data-ttu-id="a2283-143">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a2283-143">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2283-144">A expressão `Regex_belgium_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a2283-144">The regular expression  `Regex_belgium_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2283-145">Uma palavra- `Keywords_belgium_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="a2283-145">A keyword from  `Keywords_belgium_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_driver's_license_number" />
          <Match idRef="Keywords_belgium_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="a2283-146">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a2283-146">Keywords</span></span>

<span data-ttu-id="a2283-147">| |</span><span class="sxs-lookup"><span data-stu-id="a2283-147"></span></span>
|<span data-ttu-id="a2283-148">**Keywords__belgium_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a2283-148">**Keywords__belgium_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2283-149">distribuição</span><span class="sxs-lookup"><span data-stu-id="a2283-149">dl#</span></span>  <br/> <span data-ttu-id="a2283-150">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-150">driver license</span></span>  <br/> <span data-ttu-id="a2283-151">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-151">driver license number</span></span>  <br/> <span data-ttu-id="a2283-152">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-152">driver licence</span></span>  <br/> <span data-ttu-id="a2283-153">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="a2283-153">drivers lic.</span></span>  <br/> <span data-ttu-id="a2283-154">licença de drivers</span><span class="sxs-lookup"><span data-stu-id="a2283-154">drivers license</span></span>  <br/> <span data-ttu-id="a2283-155">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2283-155">drivers licence</span></span>  <br/> <span data-ttu-id="a2283-156">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-156">driver's license</span></span>  <br/> <span data-ttu-id="a2283-157">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-157">driver's license number</span></span>  <br/> <span data-ttu-id="a2283-158">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="a2283-158">driver's licence number</span></span>  <br/> <span data-ttu-id="a2283-159">dlno #</span><span class="sxs-lookup"><span data-stu-id="a2283-159">dlno#</span></span>  <br/> <span data-ttu-id="a2283-160">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="a2283-160">rijbewijs</span></span>  <br/> <span data-ttu-id="a2283-161">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="a2283-161">rijbewijsnummer</span></span>  <br/> <span data-ttu-id="a2283-162">führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a2283-162">führerscheinnummer</span></span>  <br/> <span data-ttu-id="a2283-163">fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a2283-163">fuhrerscheinnummer</span></span>  <br/> <span data-ttu-id="a2283-164">fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a2283-164">fuehrerscheinnummer</span></span>  <br/> <span data-ttu-id="a2283-165">führerschein-NR</span><span class="sxs-lookup"><span data-stu-id="a2283-165">führerschein- nr</span></span>  <br/> <span data-ttu-id="a2283-166">fuehrerschein-NR</span><span class="sxs-lookup"><span data-stu-id="a2283-166">fuehrerschein- Nr</span></span>  <br/> <span data-ttu-id="a2283-167">fuehrerschein-NR</span><span class="sxs-lookup"><span data-stu-id="a2283-167">fuehrerschein- nr</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="a2283-168">Bulgária</span><span class="sxs-lookup"><span data-stu-id="a2283-168">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="a2283-169">Formato</span><span class="sxs-lookup"><span data-stu-id="a2283-169">Format</span></span>

<span data-ttu-id="a2283-170">Nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="a2283-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2283-171">Padrão</span><span class="sxs-lookup"><span data-stu-id="a2283-171">Pattern</span></span>

<span data-ttu-id="a2283-172">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="a2283-172">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a2283-173">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a2283-173">Checksum</span></span>

<span data-ttu-id="a2283-174">Não</span><span class="sxs-lookup"><span data-stu-id="a2283-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2283-175">Definição</span><span class="sxs-lookup"><span data-stu-id="a2283-175">Definition</span></span>

<span data-ttu-id="a2283-176">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a2283-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2283-177">A expressão `Regex_bulgaria_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a2283-177">The regular expression  `Regex_bulgaria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2283-178">Uma palavra- `Keywords_bulgaria_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="a2283-178">A keyword from  `Keywords_bulgaria_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
             <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_driver's_license_number" />
          <Match idRef="Keywords_bulgaria_eu_driver's_license_number" />
        </Pattern> 
</Entity>    

```

### <a name="keywords"></a><span data-ttu-id="a2283-179">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a2283-179">Keywords</span></span>

<span data-ttu-id="a2283-180">| |</span><span class="sxs-lookup"><span data-stu-id="a2283-180"></span></span>
|<span data-ttu-id="a2283-181">**Keywords_bulgaria_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a2283-181">**Keywords_bulgaria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2283-182">distribuição</span><span class="sxs-lookup"><span data-stu-id="a2283-182">dl#</span></span>  <br/> <span data-ttu-id="a2283-183">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-183">driver license</span></span>  <br/> <span data-ttu-id="a2283-184">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-184">driver license number</span></span>  <br/> <span data-ttu-id="a2283-185">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-185">driver licence</span></span>  <br/> <span data-ttu-id="a2283-186">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="a2283-186">drivers lic.</span></span>  <br/> <span data-ttu-id="a2283-187">licença de drivers</span><span class="sxs-lookup"><span data-stu-id="a2283-187">drivers license</span></span>  <br/> <span data-ttu-id="a2283-188">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2283-188">drivers licence</span></span>  <br/> <span data-ttu-id="a2283-189">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-189">driver's license</span></span>  <br/> <span data-ttu-id="a2283-190">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-190">driver's license number</span></span>  <br/> <span data-ttu-id="a2283-191">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="a2283-191">driver's licence number</span></span>  <br/> <span data-ttu-id="a2283-192">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="a2283-192">driving license number</span></span>  <br/> <span data-ttu-id="a2283-193">dlno #</span><span class="sxs-lookup"><span data-stu-id="a2283-193">dlno#</span></span>  <br/> <span data-ttu-id="a2283-194">свидетелство за управление на мпс</span><span class="sxs-lookup"><span data-stu-id="a2283-194">свидетелство за управление на мпс</span></span>  <br/> <span data-ttu-id="a2283-195">свидетелство за управление на моторно превозно средство</span><span class="sxs-lookup"><span data-stu-id="a2283-195">свидетелство за управление на моторно превозно средство</span></span>  <br/> <span data-ttu-id="a2283-196">сумпс</span><span class="sxs-lookup"><span data-stu-id="a2283-196">сумпс</span></span>  <br/> <span data-ttu-id="a2283-197">шофьорска книжка</span><span class="sxs-lookup"><span data-stu-id="a2283-197">шофьорска книжка</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="a2283-198">Croácia</span><span class="sxs-lookup"><span data-stu-id="a2283-198">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="a2283-199">Formato</span><span class="sxs-lookup"><span data-stu-id="a2283-199">Format</span></span>

<span data-ttu-id="a2283-200">Oito dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="a2283-200">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2283-201">Padrão</span><span class="sxs-lookup"><span data-stu-id="a2283-201">Pattern</span></span>

<span data-ttu-id="a2283-202">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="a2283-202">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a2283-203">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a2283-203">Checksum</span></span>

<span data-ttu-id="a2283-204">Não</span><span class="sxs-lookup"><span data-stu-id="a2283-204">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2283-205">Definição</span><span class="sxs-lookup"><span data-stu-id="a2283-205">Definition</span></span>

<span data-ttu-id="a2283-206">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a2283-206">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2283-207">A expressão `Regex_croatia_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a2283-207">The regular expression  `Regex_croatia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2283-208">Uma palavra- `Keywords_croatia_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="a2283-208">A keyword from  `Keywords_croatia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_driver's_license_number" />
          <Match idRef="Keywords_croatia_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="a2283-209">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a2283-209">Keywords</span></span>

<span data-ttu-id="a2283-210">| |</span><span class="sxs-lookup"><span data-stu-id="a2283-210"></span></span>
|<span data-ttu-id="a2283-211">**Keywords_croatia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a2283-211">**Keywords_croatia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2283-212">distribuição</span><span class="sxs-lookup"><span data-stu-id="a2283-212">dl#</span></span>  <br/> <span data-ttu-id="a2283-213">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-213">driver license</span></span>  <br/> <span data-ttu-id="a2283-214">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-214">driver license number</span></span>  <br/> <span data-ttu-id="a2283-215">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-215">driver licence</span></span>  <br/> <span data-ttu-id="a2283-216">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="a2283-216">drivers lic.</span></span>  <br/> <span data-ttu-id="a2283-217">licença de drivers</span><span class="sxs-lookup"><span data-stu-id="a2283-217">drivers license</span></span>  <br/> <span data-ttu-id="a2283-218">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2283-218">drivers licence</span></span>  <br/> <span data-ttu-id="a2283-219">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-219">driver's license</span></span>  <br/> <span data-ttu-id="a2283-220">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-220">driver's license number</span></span>  <br/> <span data-ttu-id="a2283-221">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="a2283-221">driver's licence number</span></span>  <br/> <span data-ttu-id="a2283-222">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="a2283-222">driving license number</span></span>  <br/> <span data-ttu-id="a2283-223">dlno #</span><span class="sxs-lookup"><span data-stu-id="a2283-223">dlno#</span></span>  <br/> <span data-ttu-id="a2283-224">vozačka dozvola</span><span class="sxs-lookup"><span data-stu-id="a2283-224">vozačka dozvola</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="a2283-225">Chipre</span><span class="sxs-lookup"><span data-stu-id="a2283-225">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="a2283-226">Formato</span><span class="sxs-lookup"><span data-stu-id="a2283-226">Format</span></span>

<span data-ttu-id="a2283-227">12 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="a2283-227">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2283-228">Padrão</span><span class="sxs-lookup"><span data-stu-id="a2283-228">Pattern</span></span>

<span data-ttu-id="a2283-229">12 dígitos</span><span class="sxs-lookup"><span data-stu-id="a2283-229">12 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a2283-230">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a2283-230">Checksum</span></span>

<span data-ttu-id="a2283-231">Não</span><span class="sxs-lookup"><span data-stu-id="a2283-231">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2283-232">Definição</span><span class="sxs-lookup"><span data-stu-id="a2283-232">Definition</span></span>

<span data-ttu-id="a2283-233">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a2283-233">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2283-234">A expressão `Regex_cyprus_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a2283-234">The regular expression  `Regex_cyprus_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2283-235">Uma palavra- `Keywords_cyprus_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="a2283-235">A keyword from  `Keywords_cyprus_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_driver's_license_number" />
          <Match idRef="Keywords_cyprus_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a2283-236">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a2283-236">Keywords</span></span>

<span data-ttu-id="a2283-237">| |</span><span class="sxs-lookup"><span data-stu-id="a2283-237"></span></span>
|<span data-ttu-id="a2283-238">**Keywords_cyprus_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a2283-238">**Keywords_cyprus_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2283-239">distribuição</span><span class="sxs-lookup"><span data-stu-id="a2283-239">dl#</span></span>  <br/> <span data-ttu-id="a2283-240">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-240">driver license</span></span>  <br/> <span data-ttu-id="a2283-241">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-241">driver license number</span></span>  <br/> <span data-ttu-id="a2283-242">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-242">driver licence</span></span>  <br/> <span data-ttu-id="a2283-243">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="a2283-243">drivers lic.</span></span>  <br/> <span data-ttu-id="a2283-244">licença de drivers</span><span class="sxs-lookup"><span data-stu-id="a2283-244">drivers license</span></span>  <br/> <span data-ttu-id="a2283-245">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2283-245">drivers licence</span></span>  <br/> <span data-ttu-id="a2283-246">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-246">driver's license number</span></span>  <br/> <span data-ttu-id="a2283-247">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="a2283-247">driver's licence number</span></span>  <br/> <span data-ttu-id="a2283-248">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="a2283-248">driving license number</span></span>  <br/> <span data-ttu-id="a2283-249">dlno #</span><span class="sxs-lookup"><span data-stu-id="a2283-249">dlno#</span></span>  <br/> <span data-ttu-id="a2283-250">άδεια οδήγησης</span><span class="sxs-lookup"><span data-stu-id="a2283-250">άδεια οδήγησης</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="a2283-251">República Tcheca</span><span class="sxs-lookup"><span data-stu-id="a2283-251">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="a2283-252">Formato</span><span class="sxs-lookup"><span data-stu-id="a2283-252">Format</span></span>

<span data-ttu-id="a2283-253">Duas letras seguidas por seis dígitos</span><span class="sxs-lookup"><span data-stu-id="a2283-253">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2283-254">Padrão</span><span class="sxs-lookup"><span data-stu-id="a2283-254">Pattern</span></span>

<span data-ttu-id="a2283-255">Oito letras e dígitos:</span><span class="sxs-lookup"><span data-stu-id="a2283-255">Eight letters and digits:</span></span>
  
- <span data-ttu-id="a2283-256">Duas letras (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="a2283-256">Two letters (not case-sensitive)</span></span>
    
- <span data-ttu-id="a2283-257">Um espaço (opcional)</span><span class="sxs-lookup"><span data-stu-id="a2283-257">A space (optional)</span></span>
    
- <span data-ttu-id="a2283-258">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="a2283-258">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a2283-259">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a2283-259">Checksum</span></span>

<span data-ttu-id="a2283-260">Não</span><span class="sxs-lookup"><span data-stu-id="a2283-260">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2283-261">Definição</span><span class="sxs-lookup"><span data-stu-id="a2283-261">Definition</span></span>

<span data-ttu-id="a2283-262">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a2283-262">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2283-263">A expressão `Regex_czech_republic_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a2283-263">The regular expression  `Regex_czech_republic_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2283-264">Uma palavra- `Keywords_czech_republic_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="a2283-264">A keyword from  `Keywords_czech_republic_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_driver's_license_number" />
          <Match idRef="Keywords_czech_republic_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="a2283-265">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a2283-265">Keywords</span></span>

<span data-ttu-id="a2283-266">| |</span><span class="sxs-lookup"><span data-stu-id="a2283-266"></span></span>
|<span data-ttu-id="a2283-267">**Keywords_czech_republic_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a2283-267">**Keywords_czech_republic_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2283-268">distribuição</span><span class="sxs-lookup"><span data-stu-id="a2283-268">dl#</span></span>  <br/> <span data-ttu-id="a2283-269">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-269">driver license</span></span>  <br/> <span data-ttu-id="a2283-270">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-270">driver license number</span></span>  <br/> <span data-ttu-id="a2283-271">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-271">driver licence</span></span>  <br/> <span data-ttu-id="a2283-272">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="a2283-272">drivers lic.</span></span>  <br/> <span data-ttu-id="a2283-273">licença de drivers</span><span class="sxs-lookup"><span data-stu-id="a2283-273">drivers license</span></span>  <br/> <span data-ttu-id="a2283-274">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2283-274">drivers licence</span></span>  <br/> <span data-ttu-id="a2283-275">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-275">driver's license</span></span>  <br/> <span data-ttu-id="a2283-276">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-276">driver's license number</span></span>  <br/> <span data-ttu-id="a2283-277">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-277">driver's license number</span></span>  <br/> <span data-ttu-id="a2283-278">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="a2283-278">driver's licence number</span></span>  <br/> <span data-ttu-id="a2283-279">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="a2283-279">driving license number</span></span>  <br/> <span data-ttu-id="a2283-280">dlno #</span><span class="sxs-lookup"><span data-stu-id="a2283-280">dlno#</span></span>  <br/> <span data-ttu-id="a2283-281">řidičský prúkaz</span><span class="sxs-lookup"><span data-stu-id="a2283-281">řidičský prúkaz</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="a2283-282">Dinamarca</span><span class="sxs-lookup"><span data-stu-id="a2283-282">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="a2283-283">Formato</span><span class="sxs-lookup"><span data-stu-id="a2283-283">Format</span></span>

<span data-ttu-id="a2283-284">Oito dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="a2283-284">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2283-285">Padrão</span><span class="sxs-lookup"><span data-stu-id="a2283-285">Pattern</span></span>

<span data-ttu-id="a2283-286">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="a2283-286">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a2283-287">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a2283-287">Checksum</span></span>

<span data-ttu-id="a2283-288">Sim</span><span class="sxs-lookup"><span data-stu-id="a2283-288">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2283-289">Definição</span><span class="sxs-lookup"><span data-stu-id="a2283-289">Definition</span></span>

<span data-ttu-id="a2283-290">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a2283-290">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2283-291">A expressão `Regex_denmark_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a2283-291">The regular expression  `Regex_denmark_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2283-292">Uma palavra- `Keywords_denmark_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="a2283-292">A keyword from  `Keywords_denmark_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_driver's_license_number" />
          <Match idRef="Keywords_denmark_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="a2283-293">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a2283-293">Keywords</span></span>

<span data-ttu-id="a2283-294">| |</span><span class="sxs-lookup"><span data-stu-id="a2283-294"></span></span>
|<span data-ttu-id="a2283-295">**Keywords_denmark_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a2283-295">**Keywords_denmark_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2283-296">distribuição</span><span class="sxs-lookup"><span data-stu-id="a2283-296">dl#</span></span>  <br/> <span data-ttu-id="a2283-297">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-297">driver license</span></span>  <br/> <span data-ttu-id="a2283-298">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-298">driver license number</span></span>  <br/> <span data-ttu-id="a2283-299">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-299">driver licence</span></span>  <br/> <span data-ttu-id="a2283-300">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="a2283-300">drivers lic.</span></span>  <br/> <span data-ttu-id="a2283-301">licença de drivers</span><span class="sxs-lookup"><span data-stu-id="a2283-301">drivers license</span></span>  <br/> <span data-ttu-id="a2283-302">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2283-302">drivers licence</span></span>  <br/> <span data-ttu-id="a2283-303">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-303">driver's license</span></span>  <br/> <span data-ttu-id="a2283-304">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-304">driver's license number</span></span>  <br/> <span data-ttu-id="a2283-305">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="a2283-305">driver's licence number</span></span>  <br/> <span data-ttu-id="a2283-306">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="a2283-306">driving license number</span></span>  <br/> <span data-ttu-id="a2283-307">dlno #</span><span class="sxs-lookup"><span data-stu-id="a2283-307">dlno#</span></span>  <br/> <span data-ttu-id="a2283-308">kørekort</span><span class="sxs-lookup"><span data-stu-id="a2283-308">kørekort</span></span>  <br/> <span data-ttu-id="a2283-309">kørekortnummer</span><span class="sxs-lookup"><span data-stu-id="a2283-309">kørekortnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="a2283-310">Estônia</span><span class="sxs-lookup"><span data-stu-id="a2283-310">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="a2283-311">Formato</span><span class="sxs-lookup"><span data-stu-id="a2283-311">Format</span></span>

<span data-ttu-id="a2283-312">Duas letras seguidas por seis dígitos</span><span class="sxs-lookup"><span data-stu-id="a2283-312">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2283-313">Padrão</span><span class="sxs-lookup"><span data-stu-id="a2283-313">Pattern</span></span>

<span data-ttu-id="a2283-314">Duas letras e seis dígitos:</span><span class="sxs-lookup"><span data-stu-id="a2283-314">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="a2283-315">As letras "ET" (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="a2283-315">The letters "ET" (not case-sensitive)</span></span> 
    
- <span data-ttu-id="a2283-316">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="a2283-316">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a2283-317">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a2283-317">Checksum</span></span>

<span data-ttu-id="a2283-318">Não</span><span class="sxs-lookup"><span data-stu-id="a2283-318">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2283-319">Definição</span><span class="sxs-lookup"><span data-stu-id="a2283-319">Definition</span></span>

<span data-ttu-id="a2283-320">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a2283-320">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2283-321">A expressão `Regex_estonia_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a2283-321">The regular expression  `Regex_estonia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2283-322">Uma palavra- `Keywords_estonia_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="a2283-322">A keyword from  `Keywords_estonia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_driver's_license_number" />
          <Match idRef="Keywords_estonia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a2283-323">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a2283-323">Keywords</span></span>

<span data-ttu-id="a2283-324">| |</span><span class="sxs-lookup"><span data-stu-id="a2283-324"></span></span>
|<span data-ttu-id="a2283-325">**Keywords_estonia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a2283-325">**Keywords_estonia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2283-326">distribuição</span><span class="sxs-lookup"><span data-stu-id="a2283-326">dl#</span></span>  <br/> <span data-ttu-id="a2283-327">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-327">driver license</span></span>  <br/> <span data-ttu-id="a2283-328">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-328">driver license number</span></span>  <br/> <span data-ttu-id="a2283-329">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-329">driver license number</span></span>  <br/> <span data-ttu-id="a2283-330">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-330">driver licence</span></span>  <br/> <span data-ttu-id="a2283-331">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="a2283-331">drivers lic.</span></span>  <br/> <span data-ttu-id="a2283-332">licença de drivers</span><span class="sxs-lookup"><span data-stu-id="a2283-332">drivers license</span></span>  <br/> <span data-ttu-id="a2283-333">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2283-333">drivers licence</span></span>  <br/> <span data-ttu-id="a2283-334">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-334">driver's license</span></span>  <br/> <span data-ttu-id="a2283-335">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-335">driver's license number</span></span>  <br/> <span data-ttu-id="a2283-336">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="a2283-336">driving license number</span></span>  <br/> <span data-ttu-id="a2283-337">dlno #</span><span class="sxs-lookup"><span data-stu-id="a2283-337">dlno#</span></span>  <br/> <span data-ttu-id="a2283-338">
permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a2283-338">permis de conduire</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="a2283-339">Finlândia</span><span class="sxs-lookup"><span data-stu-id="a2283-339">Finland</span></span>

### <a name="format"></a><span data-ttu-id="a2283-340">Formato</span><span class="sxs-lookup"><span data-stu-id="a2283-340">Format</span></span>

<span data-ttu-id="a2283-341">10 dígitos que contêm um hífen</span><span class="sxs-lookup"><span data-stu-id="a2283-341">10 digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2283-342">Padrão</span><span class="sxs-lookup"><span data-stu-id="a2283-342">Pattern</span></span>

<span data-ttu-id="a2283-343">10 dígitos contendo um hífen:</span><span class="sxs-lookup"><span data-stu-id="a2283-343">10 digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="a2283-344">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="a2283-344">Six digits</span></span> 
    
- <span data-ttu-id="a2283-345">Um hífen</span><span class="sxs-lookup"><span data-stu-id="a2283-345">A hyphen</span></span>
    
-  <span data-ttu-id="a2283-346">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="a2283-346">Four digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="a2283-347">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a2283-347">Checksum</span></span>

<span data-ttu-id="a2283-348">Não</span><span class="sxs-lookup"><span data-stu-id="a2283-348">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2283-349">Definição</span><span class="sxs-lookup"><span data-stu-id="a2283-349">Definition</span></span>

<span data-ttu-id="a2283-350">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a2283-350">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2283-351">A expressão `Regex_finland_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a2283-351">The regular expression  `Regex_finland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2283-352">Uma palavra- `Keywords_finland_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="a2283-352">A keyword from  `Keywords_finland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_driver's_license_number" />
          <Match idRef="Keywords_finland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a2283-353">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a2283-353">Keywords</span></span>

<span data-ttu-id="a2283-354">| |</span><span class="sxs-lookup"><span data-stu-id="a2283-354"></span></span>
|<span data-ttu-id="a2283-355">**Keywords_finland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a2283-355">**Keywords_finland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2283-356">distribuição</span><span class="sxs-lookup"><span data-stu-id="a2283-356">dl#</span></span>  <br/> <span data-ttu-id="a2283-357">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-357">driver license</span></span>  <br/> <span data-ttu-id="a2283-358">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-358">driver license number</span></span>  <br/> <span data-ttu-id="a2283-359">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-359">driver licence</span></span>  <br/> <span data-ttu-id="a2283-360">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="a2283-360">drivers lic.</span></span>  <br/> <span data-ttu-id="a2283-361">licença de drivers</span><span class="sxs-lookup"><span data-stu-id="a2283-361">drivers license</span></span>  <br/> <span data-ttu-id="a2283-362">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2283-362">drivers licence</span></span>  <br/> <span data-ttu-id="a2283-363">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-363">driver's license</span></span>  <br/> <span data-ttu-id="a2283-364">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-364">driver's license number</span></span>  <br/> <span data-ttu-id="a2283-365">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="a2283-365">driver's licence number</span></span>  <br/> <span data-ttu-id="a2283-366">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="a2283-366">driving license number</span></span>  <br/> <span data-ttu-id="a2283-367">dlno #</span><span class="sxs-lookup"><span data-stu-id="a2283-367">dlno#</span></span>  <br/> <span data-ttu-id="a2283-368">ajokortti</span><span class="sxs-lookup"><span data-stu-id="a2283-368">ajokortti</span></span>  <br/> |
   
## <a name="france"></a><span data-ttu-id="a2283-369">França</span><span class="sxs-lookup"><span data-stu-id="a2283-369">France</span></span>

<span data-ttu-id="a2283-370">Para obter detalhes, consulte a seção "número da carteira de motorista do driver da França" em [o que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="a2283-370">For details, see the section "France Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="a2283-371">Alemanha</span><span class="sxs-lookup"><span data-stu-id="a2283-371">Germany</span></span>

<span data-ttu-id="a2283-372">Para obter detalhes, consulte a seção "número da carteira de motorista do driver alemão" em [o que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="a2283-372">For details, see the section "German Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="a2283-373">Grécia</span><span class="sxs-lookup"><span data-stu-id="a2283-373">Greece</span></span>

### <a name="format"></a><span data-ttu-id="a2283-374">Formato</span><span class="sxs-lookup"><span data-stu-id="a2283-374">Format</span></span>

<span data-ttu-id="a2283-375">Nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="a2283-375">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2283-376">Padrão</span><span class="sxs-lookup"><span data-stu-id="a2283-376">Pattern</span></span>

 <span data-ttu-id="a2283-377">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="a2283-377">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="a2283-378">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a2283-378">Checksum</span></span>

<span data-ttu-id="a2283-379">Não</span><span class="sxs-lookup"><span data-stu-id="a2283-379">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2283-380">Definição</span><span class="sxs-lookup"><span data-stu-id="a2283-380">Definition</span></span>

<span data-ttu-id="a2283-381">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a2283-381">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2283-382">A expressão `Regex_greece_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a2283-382">The regular expression  `Regex_greece_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2283-383">Uma palavra- `Keywords_greece_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="a2283-383">A keyword from  `Keywords_greece_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_driver's_license_number" />
          <Match idRef="Keywords_greece_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a2283-384">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a2283-384">Keywords</span></span>

<span data-ttu-id="a2283-385">| |</span><span class="sxs-lookup"><span data-stu-id="a2283-385"></span></span>
|<span data-ttu-id="a2283-386">**Keywords_greece_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a2283-386">**Keywords_greece_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2283-387">DlL</span><span class="sxs-lookup"><span data-stu-id="a2283-387">dlL#</span></span>  <br/> <span data-ttu-id="a2283-388">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-388">driver license</span></span>  <br/> <span data-ttu-id="a2283-389">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-389">driver license number</span></span>  <br/> <span data-ttu-id="a2283-390">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-390">driver licence</span></span>  <br/> <span data-ttu-id="a2283-391">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="a2283-391">drivers lic.</span></span>  <br/> <span data-ttu-id="a2283-392">licença de drivers</span><span class="sxs-lookup"><span data-stu-id="a2283-392">drivers license</span></span>  <br/> <span data-ttu-id="a2283-393">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2283-393">drivers licence</span></span>  <br/> <span data-ttu-id="a2283-394">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-394">driver's license</span></span>  <br/> <span data-ttu-id="a2283-395">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-395">driver's license number</span></span>  <br/> <span data-ttu-id="a2283-396">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="a2283-396">driver's licence number</span></span>  <br/> <span data-ttu-id="a2283-397">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="a2283-397">driving license number</span></span>  <br/> <span data-ttu-id="a2283-398">dlno #</span><span class="sxs-lookup"><span data-stu-id="a2283-398">dlno#</span></span>  <br/> <span data-ttu-id="a2283-399">δεια οδήγησης</span><span class="sxs-lookup"><span data-stu-id="a2283-399">δεια οδήγησης</span></span>  <br/> <span data-ttu-id="a2283-400">AdeIa odigisis</span><span class="sxs-lookup"><span data-stu-id="a2283-400">Adeia odigisis</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="a2283-401">Hungria</span><span class="sxs-lookup"><span data-stu-id="a2283-401">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="a2283-402">Formato</span><span class="sxs-lookup"><span data-stu-id="a2283-402">Format</span></span>

<span data-ttu-id="a2283-403">Duas letras seguidas por seis dígitos</span><span class="sxs-lookup"><span data-stu-id="a2283-403">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2283-404">Padrão</span><span class="sxs-lookup"><span data-stu-id="a2283-404">Pattern</span></span>

<span data-ttu-id="a2283-405">Duas letras e seis dígitos:</span><span class="sxs-lookup"><span data-stu-id="a2283-405">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="a2283-406">Duas letras (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="a2283-406">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="a2283-407">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="a2283-407">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a2283-408">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a2283-408">Checksum</span></span>

<span data-ttu-id="a2283-409">Não</span><span class="sxs-lookup"><span data-stu-id="a2283-409">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2283-410">Definição</span><span class="sxs-lookup"><span data-stu-id="a2283-410">Definition</span></span>

<span data-ttu-id="a2283-411">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a2283-411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2283-412">A expressão `Regex_hungary_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a2283-412">The regular expression  `Regex_hungary_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2283-413">Uma palavra- `Keywords_hungary_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="a2283-413">A keyword from  `Keywords_hungary_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_driver's_license_number" />
          <Match idRef="Keywords_hungary_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a2283-414">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a2283-414">Keywords</span></span>

<span data-ttu-id="a2283-415">| |</span><span class="sxs-lookup"><span data-stu-id="a2283-415"></span></span>
|<span data-ttu-id="a2283-416">**Keywords_hungary_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a2283-416">**Keywords_hungary_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2283-417">distribuição</span><span class="sxs-lookup"><span data-stu-id="a2283-417">dl#</span></span>  <br/> <span data-ttu-id="a2283-418">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-418">driver license</span></span>  <br/> <span data-ttu-id="a2283-419">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-419">driver license number</span></span>  <br/> <span data-ttu-id="a2283-420">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-420">driver licence</span></span>  <br/> <span data-ttu-id="a2283-421">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="a2283-421">drivers lic.</span></span>  <br/> <span data-ttu-id="a2283-422">licença de drivers</span><span class="sxs-lookup"><span data-stu-id="a2283-422">drivers license</span></span>  <br/> <span data-ttu-id="a2283-423">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2283-423">drivers licence</span></span>  <br/> <span data-ttu-id="a2283-424">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-424">driver's license</span></span>  <br/> <span data-ttu-id="a2283-425">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-425">driver's license number</span></span>  <br/> <span data-ttu-id="a2283-426">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="a2283-426">driver's licence number</span></span>  <br/> <span data-ttu-id="a2283-427">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="a2283-427">driving license number</span></span>  <br/> <span data-ttu-id="a2283-428">dlno #</span><span class="sxs-lookup"><span data-stu-id="a2283-428">dlno#</span></span>  <br/> <span data-ttu-id="a2283-429">vezetoi engedely</span><span class="sxs-lookup"><span data-stu-id="a2283-429">vezetoi engedely</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="a2283-430">Irlanda</span><span class="sxs-lookup"><span data-stu-id="a2283-430">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="a2283-431">Formato</span><span class="sxs-lookup"><span data-stu-id="a2283-431">Format</span></span>

<span data-ttu-id="a2283-432">Seis dígitos seguidos de quatro letras</span><span class="sxs-lookup"><span data-stu-id="a2283-432">Six digits followed by four letters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2283-433">Padrão</span><span class="sxs-lookup"><span data-stu-id="a2283-433">Pattern</span></span>

<span data-ttu-id="a2283-434">Seis dígitos e quatro letras:</span><span class="sxs-lookup"><span data-stu-id="a2283-434">Six digits and four letters:</span></span>
  
- <span data-ttu-id="a2283-435">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="a2283-435">Six digits</span></span>
    
- <span data-ttu-id="a2283-436">Quatro letras (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="a2283-436">Four letters (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a2283-437">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a2283-437">Checksum</span></span>

<span data-ttu-id="a2283-438">Não</span><span class="sxs-lookup"><span data-stu-id="a2283-438">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2283-439">Definição</span><span class="sxs-lookup"><span data-stu-id="a2283-439">Definition</span></span>

<span data-ttu-id="a2283-440">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a2283-440">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2283-441">A expressão `Regex_ireland_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a2283-441">The regular expression  `Regex_ireland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2283-442">Uma palavra- `Keywords_ireland_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="a2283-442">A keyword from  `Keywords_ireland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_driver's_license_number" />
          <Match idRef="Keywords_ireland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a2283-443">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a2283-443">Keywords</span></span>

<span data-ttu-id="a2283-444">| |</span><span class="sxs-lookup"><span data-stu-id="a2283-444"></span></span>
|<span data-ttu-id="a2283-445">**Keywords_ireland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a2283-445">**Keywords_ireland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2283-446">distribuição</span><span class="sxs-lookup"><span data-stu-id="a2283-446">dl#</span></span>  <br/> <span data-ttu-id="a2283-447">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-447">driver license</span></span>  <br/> <span data-ttu-id="a2283-448">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-448">driver license number</span></span>  <br/> <span data-ttu-id="a2283-449">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-449">driver licence</span></span>  <br/> <span data-ttu-id="a2283-450">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="a2283-450">drivers lic.</span></span>  <br/> <span data-ttu-id="a2283-451">licença de drivers</span><span class="sxs-lookup"><span data-stu-id="a2283-451">drivers license</span></span>  <br/> <span data-ttu-id="a2283-452">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2283-452">drivers licence</span></span>  <br/> <span data-ttu-id="a2283-453">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-453">driver's license</span></span>  <br/> <span data-ttu-id="a2283-454">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-454">driver's license number</span></span>  <br/> <span data-ttu-id="a2283-455">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="a2283-455">driver's licence number</span></span>  <br/> <span data-ttu-id="a2283-456">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="a2283-456">driving license number</span></span>  <br/> <span data-ttu-id="a2283-457">dlno #</span><span class="sxs-lookup"><span data-stu-id="a2283-457">dlno#</span></span>  <br/> <span data-ttu-id="a2283-458">ceadúnas tiomána</span><span class="sxs-lookup"><span data-stu-id="a2283-458">ceadúnas tiomána</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="a2283-459">Itália</span><span class="sxs-lookup"><span data-stu-id="a2283-459">Italy</span></span>

<span data-ttu-id="a2283-460">Para obter detalhes, consulte a seção "número da carteira de motorista do driver da Itália" em [o que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="a2283-460">For details, see the section "Italy Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="latvia"></a><span data-ttu-id="a2283-461">Letônia</span><span class="sxs-lookup"><span data-stu-id="a2283-461">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="a2283-462">Formato</span><span class="sxs-lookup"><span data-stu-id="a2283-462">Format</span></span>

<span data-ttu-id="a2283-463">Três letras seguidas por seis dígitos</span><span class="sxs-lookup"><span data-stu-id="a2283-463">Three letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2283-464">Padrão</span><span class="sxs-lookup"><span data-stu-id="a2283-464">Pattern</span></span>

<span data-ttu-id="a2283-465">Três letras e seis dígitos:</span><span class="sxs-lookup"><span data-stu-id="a2283-465">Three letters and six digits:</span></span>
  
-  <span data-ttu-id="a2283-466">Três letras (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="a2283-466">Three letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="a2283-467">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="a2283-467">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a2283-468">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a2283-468">Checksum</span></span>

<span data-ttu-id="a2283-469">Não</span><span class="sxs-lookup"><span data-stu-id="a2283-469">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2283-470">Definição</span><span class="sxs-lookup"><span data-stu-id="a2283-470">Definition</span></span>

<span data-ttu-id="a2283-471">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a2283-471">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2283-472">A expressão `Regex_latvia_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a2283-472">The regular expression  `Regex_latvia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2283-473">Uma palavra- `Keywords_latvia_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="a2283-473">A keyword from  `Keywords_latvia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_driver's_license_number" />
          <Match idRef="Keywords_latvia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a2283-474">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a2283-474">Keywords</span></span>

<span data-ttu-id="a2283-475">| |</span><span class="sxs-lookup"><span data-stu-id="a2283-475"></span></span>
|<span data-ttu-id="a2283-476">**Keywords_latvia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a2283-476">**Keywords_latvia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2283-477">distribuição</span><span class="sxs-lookup"><span data-stu-id="a2283-477">dl#</span></span>  <br/> <span data-ttu-id="a2283-478">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-478">driver license</span></span>  <br/> <span data-ttu-id="a2283-479">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-479">driver license number</span></span>  <br/> <span data-ttu-id="a2283-480">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-480">driver licence</span></span>  <br/> <span data-ttu-id="a2283-481">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="a2283-481">drivers lic.</span></span>  <br/> <span data-ttu-id="a2283-482">licença de drivers</span><span class="sxs-lookup"><span data-stu-id="a2283-482">drivers license</span></span>  <br/> <span data-ttu-id="a2283-483">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2283-483">drivers licence</span></span>  <br/> <span data-ttu-id="a2283-484">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-484">driver's license</span></span>  <br/> <span data-ttu-id="a2283-485">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-485">driver's license number</span></span>  <br/> <span data-ttu-id="a2283-486">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="a2283-486">driver's licence number</span></span>  <br/> <span data-ttu-id="a2283-487">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="a2283-487">driving license number</span></span>  <br/> <span data-ttu-id="a2283-488">dlno #</span><span class="sxs-lookup"><span data-stu-id="a2283-488">dlno#</span></span>  <br/> <span data-ttu-id="a2283-489">autovadītāja apliecība</span><span class="sxs-lookup"><span data-stu-id="a2283-489">autovadītāja apliecība</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="a2283-490">Lituânia</span><span class="sxs-lookup"><span data-stu-id="a2283-490">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="a2283-491">Formato</span><span class="sxs-lookup"><span data-stu-id="a2283-491">Format</span></span>

<span data-ttu-id="a2283-492">Oito dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="a2283-492">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2283-493">Padrão</span><span class="sxs-lookup"><span data-stu-id="a2283-493">Pattern</span></span>

 <span data-ttu-id="a2283-494">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="a2283-494">Eight digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="a2283-495">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a2283-495">Checksum</span></span>

<span data-ttu-id="a2283-496">Não</span><span class="sxs-lookup"><span data-stu-id="a2283-496">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2283-497">Definição</span><span class="sxs-lookup"><span data-stu-id="a2283-497">Definition</span></span>

<span data-ttu-id="a2283-498">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a2283-498">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2283-499">A expressão `Regex_lithuania_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a2283-499">The regular expression  `Regex_lithuania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2283-500">Uma palavra- `Keywords_lithuania_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="a2283-500">A keyword from  `Keywords_lithuania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_driver's_license_number" />
          <Match idRef="Keywords_lithuania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a2283-501">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a2283-501">Keywords</span></span>

<span data-ttu-id="a2283-502">| |</span><span class="sxs-lookup"><span data-stu-id="a2283-502"></span></span>
|<span data-ttu-id="a2283-503">**Keywords_lithuania_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a2283-503">**Keywords_lithuania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2283-504">distribuição</span><span class="sxs-lookup"><span data-stu-id="a2283-504">dl#</span></span>  <br/> <span data-ttu-id="a2283-505">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-505">driver license</span></span>  <br/> <span data-ttu-id="a2283-506">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-506">driver license number</span></span>  <br/> <span data-ttu-id="a2283-507">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-507">driver licence</span></span>  <br/> <span data-ttu-id="a2283-508">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="a2283-508">drivers lic.</span></span>  <br/> <span data-ttu-id="a2283-509">licença de drivers</span><span class="sxs-lookup"><span data-stu-id="a2283-509">drivers license</span></span>  <br/> <span data-ttu-id="a2283-510">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2283-510">drivers licence</span></span>  <br/> <span data-ttu-id="a2283-511">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-511">driver's license</span></span>  <br/> <span data-ttu-id="a2283-512">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-512">driver's license number</span></span>  <br/> <span data-ttu-id="a2283-513">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="a2283-513">driver's licence number</span></span>  <br/> <span data-ttu-id="a2283-514">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="a2283-514">driving license number</span></span>  <br/> <span data-ttu-id="a2283-515">dlno #</span><span class="sxs-lookup"><span data-stu-id="a2283-515">dlno#</span></span>  <br/> <span data-ttu-id="a2283-516">vairuotojo pažymėjimas</span><span class="sxs-lookup"><span data-stu-id="a2283-516">vairuotojo pažymėjimas</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="a2283-517">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="a2283-517">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="a2283-518">Formato</span><span class="sxs-lookup"><span data-stu-id="a2283-518">Format</span></span>

<span data-ttu-id="a2283-519">Seis dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="a2283-519">Six digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2283-520">Padrão</span><span class="sxs-lookup"><span data-stu-id="a2283-520">Pattern</span></span>

 <span data-ttu-id="a2283-521">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="a2283-521">Six digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="a2283-522">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a2283-522">Checksum</span></span>

<span data-ttu-id="a2283-523">Não</span><span class="sxs-lookup"><span data-stu-id="a2283-523">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2283-524">Definição</span><span class="sxs-lookup"><span data-stu-id="a2283-524">Definition</span></span>

<span data-ttu-id="a2283-525">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a2283-525">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2283-526">A expressão `Regex_luxemburg_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a2283-526">The regular expression  `Regex_luxemburg_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2283-527">Uma palavra- `Keywords_luxemburg_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="a2283-527">A keyword from  `Keywords_luxemburg_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_driver's_license_number" />
          <Match idRef="Keywords_luxemburg_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a2283-528">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a2283-528">Keywords</span></span>

<span data-ttu-id="a2283-529">| |</span><span class="sxs-lookup"><span data-stu-id="a2283-529"></span></span>
|<span data-ttu-id="a2283-530">**Keywords_luxemburg_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a2283-530">**Keywords_luxemburg_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2283-531">distribuição</span><span class="sxs-lookup"><span data-stu-id="a2283-531">dl#</span></span>  <br/> <span data-ttu-id="a2283-532">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-532">driver license</span></span>  <br/> <span data-ttu-id="a2283-533">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-533">driver license number</span></span>  <br/> <span data-ttu-id="a2283-534">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-534">driver licence</span></span>  <br/> <span data-ttu-id="a2283-535">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="a2283-535">drivers lic.</span></span>  <br/> <span data-ttu-id="a2283-536">licença de drivers</span><span class="sxs-lookup"><span data-stu-id="a2283-536">drivers license</span></span>  <br/> <span data-ttu-id="a2283-537">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2283-537">drivers licence</span></span>  <br/> <span data-ttu-id="a2283-538">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-538">driver's license</span></span>  <br/> <span data-ttu-id="a2283-539">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-539">driver's license number</span></span>  <br/> <span data-ttu-id="a2283-540">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="a2283-540">driver's licence number</span></span>  <br/> <span data-ttu-id="a2283-541">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="a2283-541">driving license number</span></span>  <br/> <span data-ttu-id="a2283-542">dlno #</span><span class="sxs-lookup"><span data-stu-id="a2283-542">dlno#</span></span>  <br/> <span data-ttu-id="a2283-543">fahrerlaubnis</span><span class="sxs-lookup"><span data-stu-id="a2283-543">fahrerlaubnis</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="a2283-544">Malta</span><span class="sxs-lookup"><span data-stu-id="a2283-544">Malta</span></span>

### <a name="format"></a><span data-ttu-id="a2283-545">Formato</span><span class="sxs-lookup"><span data-stu-id="a2283-545">Format</span></span>

<span data-ttu-id="a2283-546">Combinação de dois caracteres e seis dígitos no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="a2283-546">Combination of two characters and six digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2283-547">Padrão</span><span class="sxs-lookup"><span data-stu-id="a2283-547">Pattern</span></span>

<span data-ttu-id="a2283-548">Combinação de dois caracteres e seis dígitos:</span><span class="sxs-lookup"><span data-stu-id="a2283-548">Combination of two characters and six digits:</span></span>
  
- <span data-ttu-id="a2283-549">Dois caracteres (dígitos ou letras, não diferenciam maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="a2283-549">Two characters (digits or letters, not case-sensitive)</span></span>
    
- <span data-ttu-id="a2283-550">Um espaço (opcional)</span><span class="sxs-lookup"><span data-stu-id="a2283-550">A space (optional)</span></span>
    
- <span data-ttu-id="a2283-551">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="a2283-551">Three digits</span></span>
    
- <span data-ttu-id="a2283-552">Um espaço (opcional)</span><span class="sxs-lookup"><span data-stu-id="a2283-552">A space (optional)</span></span>
    
- <span data-ttu-id="a2283-553">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="a2283-553">Three digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a2283-554">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a2283-554">Checksum</span></span>

<span data-ttu-id="a2283-555">Não</span><span class="sxs-lookup"><span data-stu-id="a2283-555">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2283-556">Definição</span><span class="sxs-lookup"><span data-stu-id="a2283-556">Definition</span></span>

<span data-ttu-id="a2283-557">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a2283-557">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2283-558">A expressão `Regex_malta_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a2283-558">The regular expression  `Regex_malta_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2283-559">Uma palavra- `Keywords_malta_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="a2283-559">A keyword from  `Keywords_malta_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
 <Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_driver's_license_number" />
          <Match idRef="Keywords_malta_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a2283-560">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a2283-560">Keywords</span></span>

<span data-ttu-id="a2283-561">| |</span><span class="sxs-lookup"><span data-stu-id="a2283-561"></span></span>
|<span data-ttu-id="a2283-562">**Keywords_malta_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a2283-562">**Keywords_malta_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2283-563">distribuição</span><span class="sxs-lookup"><span data-stu-id="a2283-563">dl#</span></span>  <br/> <span data-ttu-id="a2283-564">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-564">driver license</span></span>  <br/> <span data-ttu-id="a2283-565">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-565">driver license number</span></span>  <br/> <span data-ttu-id="a2283-566">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-566">driver licence</span></span>  <br/> <span data-ttu-id="a2283-567">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="a2283-567">drivers lic.</span></span>  <br/> <span data-ttu-id="a2283-568">licença de drivers</span><span class="sxs-lookup"><span data-stu-id="a2283-568">drivers license</span></span>  <br/> <span data-ttu-id="a2283-569">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2283-569">drivers licence</span></span>  <br/> <span data-ttu-id="a2283-570">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-570">driver's license</span></span>  <br/> <span data-ttu-id="a2283-571">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-571">driver's license number</span></span>  <br/> <span data-ttu-id="a2283-572">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="a2283-572">driver's licence number</span></span>  <br/> <span data-ttu-id="a2283-573">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="a2283-573">driving license number</span></span>  <br/> <span data-ttu-id="a2283-574">dlno #</span><span class="sxs-lookup"><span data-stu-id="a2283-574">dlno#</span></span>  <br/> <span data-ttu-id="a2283-575">liċenzja tas-sewqan</span><span class="sxs-lookup"><span data-stu-id="a2283-575">liċenzja tas-sewqan</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="a2283-576">Países Baixos</span><span class="sxs-lookup"><span data-stu-id="a2283-576">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="a2283-577">Formato</span><span class="sxs-lookup"><span data-stu-id="a2283-577">Format</span></span>

<span data-ttu-id="a2283-578">10 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="a2283-578">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2283-579">Padrão</span><span class="sxs-lookup"><span data-stu-id="a2283-579">Pattern</span></span>

<span data-ttu-id="a2283-580">10 dígitos</span><span class="sxs-lookup"><span data-stu-id="a2283-580">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a2283-581">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a2283-581">Checksum</span></span>

<span data-ttu-id="a2283-582">Não</span><span class="sxs-lookup"><span data-stu-id="a2283-582">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2283-583">Definição</span><span class="sxs-lookup"><span data-stu-id="a2283-583">Definition</span></span>

<span data-ttu-id="a2283-584">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a2283-584">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2283-585">A expressão `Regex_netherlands_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a2283-585">The regular expression  `Regex_netherlands_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2283-586">Uma palavra- `Keywords_netherlands_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="a2283-586">A keyword from  `Keywords_netherlands_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_driver's_license_number" />
          <Match idRef="Keywords_netherlands_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a2283-587">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a2283-587">Keywords</span></span>

<span data-ttu-id="a2283-588">| |</span><span class="sxs-lookup"><span data-stu-id="a2283-588"></span></span>
|<span data-ttu-id="a2283-589">**Keywords_netherlands_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a2283-589">**Keywords_netherlands_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2283-590">distribuição</span><span class="sxs-lookup"><span data-stu-id="a2283-590">dl#</span></span>  <br/> <span data-ttu-id="a2283-591">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-591">driver license</span></span>  <br/> <span data-ttu-id="a2283-592">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-592">driver license number</span></span>  <br/> <span data-ttu-id="a2283-593">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-593">driver licence</span></span>  <br/> <span data-ttu-id="a2283-594">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="a2283-594">drivers lic.</span></span>  <br/> <span data-ttu-id="a2283-595">licença de drivers</span><span class="sxs-lookup"><span data-stu-id="a2283-595">drivers license</span></span>  <br/> <span data-ttu-id="a2283-596">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2283-596">drivers licence</span></span>  <br/> <span data-ttu-id="a2283-597">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-597">driver's license</span></span>  <br/> <span data-ttu-id="a2283-598">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-598">driver's license number</span></span>  <br/> <span data-ttu-id="a2283-599">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="a2283-599">driver's licence number</span></span>  <br/> <span data-ttu-id="a2283-600">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="a2283-600">driving license number</span></span>  <br/> <span data-ttu-id="a2283-601">dlno #</span><span class="sxs-lookup"><span data-stu-id="a2283-601">dlno#</span></span>  <br/> <span data-ttu-id="a2283-602">
permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a2283-602">permis de conduire</span></span>  <br/> <span data-ttu-id="a2283-603">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="a2283-603">rijbewijs</span></span>  <br/> <span data-ttu-id="a2283-604">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="a2283-604">rijbewijsnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="a2283-605">Polônia</span><span class="sxs-lookup"><span data-stu-id="a2283-605">Poland</span></span>

### <a name="format"></a><span data-ttu-id="a2283-606">Formato</span><span class="sxs-lookup"><span data-stu-id="a2283-606">Format</span></span>

<span data-ttu-id="a2283-607">14 dígitos contendo 2 barras</span><span class="sxs-lookup"><span data-stu-id="a2283-607">14 digits containing 2 forward slashes</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2283-608">Padrão</span><span class="sxs-lookup"><span data-stu-id="a2283-608">Pattern</span></span>

<span data-ttu-id="a2283-609">14 dígitos e 2 barras de avanço:</span><span class="sxs-lookup"><span data-stu-id="a2283-609">14 digits and 2 forward slashes:</span></span>
  
-  <span data-ttu-id="a2283-610">Cinco dígitos</span><span class="sxs-lookup"><span data-stu-id="a2283-610">Five digits</span></span> 
    
- <span data-ttu-id="a2283-611">Uma barra</span><span class="sxs-lookup"><span data-stu-id="a2283-611">A forward slash</span></span>
    
- <span data-ttu-id="a2283-612">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="a2283-612">Two digits</span></span>
    
- <span data-ttu-id="a2283-613">Uma barra</span><span class="sxs-lookup"><span data-stu-id="a2283-613">A forward slash</span></span>
    
- <span data-ttu-id="a2283-614">Sete dígitos</span><span class="sxs-lookup"><span data-stu-id="a2283-614">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a2283-615">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a2283-615">Checksum</span></span>

<span data-ttu-id="a2283-616">Não</span><span class="sxs-lookup"><span data-stu-id="a2283-616">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2283-617">Definição</span><span class="sxs-lookup"><span data-stu-id="a2283-617">Definition</span></span>

<span data-ttu-id="a2283-618">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a2283-618">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2283-619">A expressão `Regex_poland_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a2283-619">The regular expression  `Regex_poland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2283-620">Uma palavra- `Keywords_poland_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="a2283-620">A keyword from  `Keywords_poland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_driver's_license_number" />
          <Match idRef="Keywords_poland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a2283-621">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a2283-621">Keywords</span></span>

<span data-ttu-id="a2283-622">| |</span><span class="sxs-lookup"><span data-stu-id="a2283-622"></span></span>
|<span data-ttu-id="a2283-623">**Keywords_poland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a2283-623">**Keywords_poland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2283-624">distribuição</span><span class="sxs-lookup"><span data-stu-id="a2283-624">dl#</span></span>  <br/> <span data-ttu-id="a2283-625">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-625">driver license</span></span>  <br/> <span data-ttu-id="a2283-626">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-626">driver license number</span></span>  <br/> <span data-ttu-id="a2283-627">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-627">driver licence</span></span>  <br/> <span data-ttu-id="a2283-628">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="a2283-628">drivers lic.</span></span>  <br/> <span data-ttu-id="a2283-629">licença de drivers</span><span class="sxs-lookup"><span data-stu-id="a2283-629">drivers license</span></span>  <br/> <span data-ttu-id="a2283-630">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2283-630">drivers licence</span></span>  <br/> <span data-ttu-id="a2283-631">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-631">driver's license</span></span>  <br/> <span data-ttu-id="a2283-632">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-632">driver's license number</span></span>  <br/> <span data-ttu-id="a2283-633">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="a2283-633">driver's licence number</span></span>  <br/> <span data-ttu-id="a2283-634">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="a2283-634">driving license number</span></span>  <br/> <span data-ttu-id="a2283-635">dlno #</span><span class="sxs-lookup"><span data-stu-id="a2283-635">dlno#</span></span>  <br/> <span data-ttu-id="a2283-636">Prawo jazdy</span><span class="sxs-lookup"><span data-stu-id="a2283-636">prawo jazdy</span></span>  <br/> |
   
## <a name="portugal"></a><span data-ttu-id="a2283-637">Portugal</span><span class="sxs-lookup"><span data-stu-id="a2283-637">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="a2283-638">Formato</span><span class="sxs-lookup"><span data-stu-id="a2283-638">Format</span></span>

<span data-ttu-id="a2283-639">Duas letras seguidas por sete números no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="a2283-639">Two letters followed by a seven numbers in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2283-640">Padrão</span><span class="sxs-lookup"><span data-stu-id="a2283-640">Pattern</span></span>

<span data-ttu-id="a2283-641">Duas letras seguidas por sete números com caracteres especiais:</span><span class="sxs-lookup"><span data-stu-id="a2283-641">Two letters followed by seven numbers with special characters:</span></span>
  
-  <span data-ttu-id="a2283-642">Duas letras (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="a2283-642">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="a2283-643">Um hífen</span><span class="sxs-lookup"><span data-stu-id="a2283-643">A hyphen</span></span>
    
- <span data-ttu-id="a2283-644">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="a2283-644">Six digits</span></span>
    
- <span data-ttu-id="a2283-645">Um espaço</span><span class="sxs-lookup"><span data-stu-id="a2283-645">A space</span></span>
    
- <span data-ttu-id="a2283-646">Um dígito</span><span class="sxs-lookup"><span data-stu-id="a2283-646">One digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a2283-647">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a2283-647">Checksum</span></span>

<span data-ttu-id="a2283-648">Não</span><span class="sxs-lookup"><span data-stu-id="a2283-648">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2283-649">Definição</span><span class="sxs-lookup"><span data-stu-id="a2283-649">Definition</span></span>

<span data-ttu-id="a2283-650">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a2283-650">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2283-651">A expressão `Regex_portugal_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a2283-651">The regular expression  `Regex_portugal_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2283-652">Uma palavra- `Keywords_portugal_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="a2283-652">A keyword from  `Keywords_portugal_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_driver's_license_number" />
          <Match idRef="Keywords_portugal_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a2283-653">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a2283-653">Keywords</span></span>

<span data-ttu-id="a2283-654">| |</span><span class="sxs-lookup"><span data-stu-id="a2283-654"></span></span>
|<span data-ttu-id="a2283-655">**Keywords_portugal_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a2283-655">**Keywords_portugal_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2283-656">distribuição</span><span class="sxs-lookup"><span data-stu-id="a2283-656">dl#</span></span>  <br/> <span data-ttu-id="a2283-657">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-657">driver license</span></span>  <br/> <span data-ttu-id="a2283-658">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-658">driver license number</span></span>  <br/> <span data-ttu-id="a2283-659">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-659">driver licence</span></span>  <br/> <span data-ttu-id="a2283-660">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="a2283-660">drivers lic.</span></span>  <br/> <span data-ttu-id="a2283-661">licença de drivers</span><span class="sxs-lookup"><span data-stu-id="a2283-661">drivers license</span></span>  <br/> <span data-ttu-id="a2283-662">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2283-662">drivers licence</span></span>  <br/> <span data-ttu-id="a2283-663">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-663">driver's license</span></span>  <br/> <span data-ttu-id="a2283-664">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-664">driver's license number</span></span>  <br/> <span data-ttu-id="a2283-665">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="a2283-665">driver's licence number</span></span>  <br/> <span data-ttu-id="a2283-666">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="a2283-666">driving license number</span></span>  <br/> <span data-ttu-id="a2283-667">dlno #</span><span class="sxs-lookup"><span data-stu-id="a2283-667">dlno#</span></span>  <br/> <span data-ttu-id="a2283-668">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-668">carteira de motorista</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="a2283-669">Romênia</span><span class="sxs-lookup"><span data-stu-id="a2283-669">Romania</span></span>

### <a name="format"></a><span data-ttu-id="a2283-670">Formato</span><span class="sxs-lookup"><span data-stu-id="a2283-670">Format</span></span>

<span data-ttu-id="a2283-671">Um caractere seguido por oito dígitos</span><span class="sxs-lookup"><span data-stu-id="a2283-671">One character followed by eight digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2283-672">Padrão</span><span class="sxs-lookup"><span data-stu-id="a2283-672">Pattern</span></span>

<span data-ttu-id="a2283-673">Um caractere seguido por oito dígitos:</span><span class="sxs-lookup"><span data-stu-id="a2283-673">One character followed by eight digits:</span></span>
  
-  <span data-ttu-id="a2283-674">Uma letra (não diferencia maiúsculas de minúsculas) ou dígito</span><span class="sxs-lookup"><span data-stu-id="a2283-674">One letter (not case-sensitive) or digit</span></span> 
    
- <span data-ttu-id="a2283-675">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="a2283-675">Eight digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a2283-676">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a2283-676">Checksum</span></span>

<span data-ttu-id="a2283-677">Não</span><span class="sxs-lookup"><span data-stu-id="a2283-677">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2283-678">Definição</span><span class="sxs-lookup"><span data-stu-id="a2283-678">Definition</span></span>

<span data-ttu-id="a2283-679">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a2283-679">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2283-680">A expressão `Regex_romania_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a2283-680">The regular expression  `Regex_romania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2283-681">Uma palavra- `Keywords_romania_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="a2283-681">A keyword from  `Keywords_romania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_driver's_license_number" />
          <Match idRef="Keywords_romania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a2283-682">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a2283-682">Keywords</span></span>

<span data-ttu-id="a2283-683">| |</span><span class="sxs-lookup"><span data-stu-id="a2283-683"></span></span>
|<span data-ttu-id="a2283-684">**Keywords_romania_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a2283-684">**Keywords_romania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2283-685">distribuição</span><span class="sxs-lookup"><span data-stu-id="a2283-685">dl#</span></span>  <br/> <span data-ttu-id="a2283-686">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-686">driver license</span></span>  <br/> <span data-ttu-id="a2283-687">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-687">driver license number</span></span>  <br/> <span data-ttu-id="a2283-688">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-688">driver licence</span></span>  <br/> <span data-ttu-id="a2283-689">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="a2283-689">drivers lic.</span></span>  <br/> <span data-ttu-id="a2283-690">licença de drivers</span><span class="sxs-lookup"><span data-stu-id="a2283-690">drivers license</span></span>  <br/> <span data-ttu-id="a2283-691">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2283-691">drivers licence</span></span>  <br/> <span data-ttu-id="a2283-692">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-692">driver's license</span></span>  <br/> <span data-ttu-id="a2283-693">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-693">driver's license number</span></span>  <br/> <span data-ttu-id="a2283-694">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="a2283-694">driver's licence number</span></span>  <br/> <span data-ttu-id="a2283-695">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="a2283-695">driving license number</span></span>  <br/> <span data-ttu-id="a2283-696">dlno #</span><span class="sxs-lookup"><span data-stu-id="a2283-696">dlno#</span></span>  <br/> <span data-ttu-id="a2283-697">permé de conducere</span><span class="sxs-lookup"><span data-stu-id="a2283-697">permis de conducere</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="a2283-698">Eslováquia</span><span class="sxs-lookup"><span data-stu-id="a2283-698">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="a2283-699">Formato</span><span class="sxs-lookup"><span data-stu-id="a2283-699">Format</span></span>

<span data-ttu-id="a2283-700">Um caractere seguido por sete dígitos</span><span class="sxs-lookup"><span data-stu-id="a2283-700">One character followed by seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2283-701">Padrão</span><span class="sxs-lookup"><span data-stu-id="a2283-701">Pattern</span></span>

<span data-ttu-id="a2283-702">Um caractere seguido por sete dígitos</span><span class="sxs-lookup"><span data-stu-id="a2283-702">One character followed by seven digits</span></span>
  
- <span data-ttu-id="a2283-703">Uma letra (não diferencia maiúsculas de minúsculas) ou dígito</span><span class="sxs-lookup"><span data-stu-id="a2283-703">One letter (not case-sensitive) or digit</span></span>
    
-  <span data-ttu-id="a2283-704">Sete dígitos</span><span class="sxs-lookup"><span data-stu-id="a2283-704">Seven digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="a2283-705">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a2283-705">Checksum</span></span>

<span data-ttu-id="a2283-706">Não</span><span class="sxs-lookup"><span data-stu-id="a2283-706">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2283-707">Definição</span><span class="sxs-lookup"><span data-stu-id="a2283-707">Definition</span></span>

<span data-ttu-id="a2283-708">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a2283-708">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2283-709">A expressão `Regex_slovakia_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a2283-709">The regular expression  `Regex_slovakia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2283-710">Uma palavra- `Keywords_slovakia_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="a2283-710">A keyword from  `Keywords_slovakia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovaknia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovakia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a2283-711">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a2283-711">Keywords</span></span>

<span data-ttu-id="a2283-712">| |</span><span class="sxs-lookup"><span data-stu-id="a2283-712"></span></span>
|<span data-ttu-id="a2283-713">**Keywords_slovakia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a2283-713">**Keywords_slovakia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2283-714">distribuição</span><span class="sxs-lookup"><span data-stu-id="a2283-714">dl#</span></span>  <br/> <span data-ttu-id="a2283-715">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-715">driver license</span></span>  <br/> <span data-ttu-id="a2283-716">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-716">driver license number</span></span>  <br/> <span data-ttu-id="a2283-717">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-717">driver licence</span></span>  <br/> <span data-ttu-id="a2283-718">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="a2283-718">drivers lic.</span></span>  <br/> <span data-ttu-id="a2283-719">licença de drivers</span><span class="sxs-lookup"><span data-stu-id="a2283-719">drivers license</span></span>  <br/> <span data-ttu-id="a2283-720">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2283-720">drivers licence</span></span>  <br/> <span data-ttu-id="a2283-721">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-721">driver's license</span></span>  <br/> <span data-ttu-id="a2283-722">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-722">driver's license number</span></span>  <br/> <span data-ttu-id="a2283-723">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="a2283-723">driver's licence number</span></span>  <br/> <span data-ttu-id="a2283-724">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="a2283-724">driving license number</span></span>  <br/> <span data-ttu-id="a2283-725">dlno #</span><span class="sxs-lookup"><span data-stu-id="a2283-725">dlno#</span></span>  <br/> <span data-ttu-id="a2283-726">vodičský preukaz</span><span class="sxs-lookup"><span data-stu-id="a2283-726">vodičský preukaz</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="a2283-727">Eslovênia</span><span class="sxs-lookup"><span data-stu-id="a2283-727">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="a2283-728">Formato</span><span class="sxs-lookup"><span data-stu-id="a2283-728">Format</span></span>

<span data-ttu-id="a2283-729">Nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="a2283-729">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2283-730">Padrão</span><span class="sxs-lookup"><span data-stu-id="a2283-730">Pattern</span></span>

<span data-ttu-id="a2283-731">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="a2283-731">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a2283-732">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a2283-732">Checksum</span></span>

<span data-ttu-id="a2283-733">Não</span><span class="sxs-lookup"><span data-stu-id="a2283-733">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2283-734">Definição</span><span class="sxs-lookup"><span data-stu-id="a2283-734">Definition</span></span>

<span data-ttu-id="a2283-735">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a2283-735">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2283-736">A expressão `Regex_slovenia_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a2283-736">The regular expression  `Regex_slovenia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2283-737">Uma palavra- `Keywords_slovenia_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="a2283-737">A keyword from  `Keywords_slovenia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovenia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a2283-738">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a2283-738">Keywords</span></span>

<span data-ttu-id="a2283-739">| |</span><span class="sxs-lookup"><span data-stu-id="a2283-739"></span></span>
|<span data-ttu-id="a2283-740">**Keywords_slovenia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a2283-740">**Keywords_slovenia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2283-741">distribuição</span><span class="sxs-lookup"><span data-stu-id="a2283-741">dl#</span></span>  <br/> <span data-ttu-id="a2283-742">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-742">driver license</span></span>  <br/> <span data-ttu-id="a2283-743">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-743">driver license number</span></span>  <br/> <span data-ttu-id="a2283-744">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-744">driver licence</span></span>  <br/> <span data-ttu-id="a2283-745">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="a2283-745">drivers lic.</span></span>  <br/> <span data-ttu-id="a2283-746">licença de drivers</span><span class="sxs-lookup"><span data-stu-id="a2283-746">drivers license</span></span>  <br/> <span data-ttu-id="a2283-747">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2283-747">drivers licence</span></span>  <br/> <span data-ttu-id="a2283-748">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-748">driver's license</span></span>  <br/> <span data-ttu-id="a2283-749">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-749">driver's license number</span></span>  <br/> <span data-ttu-id="a2283-750">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="a2283-750">driver's licence number</span></span>  <br/> <span data-ttu-id="a2283-751">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="a2283-751">driving license number</span></span>  <br/> <span data-ttu-id="a2283-752">dlno #</span><span class="sxs-lookup"><span data-stu-id="a2283-752">dlno#</span></span>  <br/> <span data-ttu-id="a2283-753">vozniško dovoljenje</span><span class="sxs-lookup"><span data-stu-id="a2283-753">vozniško dovoljenje</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="a2283-754">Espanha</span><span class="sxs-lookup"><span data-stu-id="a2283-754">Spain</span></span>

### <a name="format"></a><span data-ttu-id="a2283-755">Formato</span><span class="sxs-lookup"><span data-stu-id="a2283-755">Format</span></span>

<span data-ttu-id="a2283-756">Oito dígitos seguidos de um caractere</span><span class="sxs-lookup"><span data-stu-id="a2283-756">Eight digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2283-757">Padrão</span><span class="sxs-lookup"><span data-stu-id="a2283-757">Pattern</span></span>

<span data-ttu-id="a2283-758">Oito dígitos seguidos de um caractere:</span><span class="sxs-lookup"><span data-stu-id="a2283-758">Eight digits followed by one character:</span></span>
  
-  <span data-ttu-id="a2283-759">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="a2283-759">Eight digits</span></span> 
    
- <span data-ttu-id="a2283-760">Um dígito ou letra (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="a2283-760">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a2283-761">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a2283-761">Checksum</span></span>

<span data-ttu-id="a2283-762">Sim</span><span class="sxs-lookup"><span data-stu-id="a2283-762">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2283-763">Definição</span><span class="sxs-lookup"><span data-stu-id="a2283-763">Definition</span></span>

<span data-ttu-id="a2283-764">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a2283-764">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2283-765">A função `Func_spain_eu_driver's_license_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a2283-765">The function  `Func_spain_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2283-766">Uma palavra- `Keywords_spain_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="a2283-766">A keyword from  `Keywords_spain_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_driver's_license_number" />
          <Match idRef="Keywords_spain_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a2283-767">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a2283-767">Keywords</span></span>

<span data-ttu-id="a2283-768">| |</span><span class="sxs-lookup"><span data-stu-id="a2283-768"></span></span>
|<span data-ttu-id="a2283-769">**Keywords_spain_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a2283-769">**Keywords_spain_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2283-770">dlno #</span><span class="sxs-lookup"><span data-stu-id="a2283-770">dlno#</span></span>  <br/> <span data-ttu-id="a2283-771">distribuição</span><span class="sxs-lookup"><span data-stu-id="a2283-771">dl#</span></span>  <br/> <span data-ttu-id="a2283-772">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="a2283-772">drivers lic.</span></span>  <br/> <span data-ttu-id="a2283-773">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-773">driver licence</span></span>  <br/> <span data-ttu-id="a2283-774">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-774">driver license</span></span>  <br/> <span data-ttu-id="a2283-775">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2283-775">drivers licence</span></span>  <br/> <span data-ttu-id="a2283-776">
drivers license</span><span class="sxs-lookup"><span data-stu-id="a2283-776">drivers license</span></span>  <br/> <span data-ttu-id="a2283-777">licença do driver</span><span class="sxs-lookup"><span data-stu-id="a2283-777">driver's licence</span></span>  <br/> <span data-ttu-id="a2283-778">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-778">driver's license</span></span>  <br/> <span data-ttu-id="a2283-779">driving licence
</span><span class="sxs-lookup"><span data-stu-id="a2283-779">driving licence</span></span>  <br/> <span data-ttu-id="a2283-780">direcionando a licença</span><span class="sxs-lookup"><span data-stu-id="a2283-780">driving license</span></span>  <br/> <span data-ttu-id="a2283-781">número de licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-781">driver licence number</span></span>  <br/> <span data-ttu-id="a2283-782">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-782">driver license number</span></span>  <br/> <span data-ttu-id="a2283-783">número de licença de drivers</span><span class="sxs-lookup"><span data-stu-id="a2283-783">drivers licence number</span></span>  <br/> <span data-ttu-id="a2283-784">número de licença de drivers</span><span class="sxs-lookup"><span data-stu-id="a2283-784">drivers license number</span></span>  <br/> <span data-ttu-id="a2283-785">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="a2283-785">driver's licence number</span></span>  <br/> <span data-ttu-id="a2283-786">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-786">driver's license number</span></span>  <br/> <span data-ttu-id="a2283-787">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="a2283-787">driving licence number</span></span>  <br/> <span data-ttu-id="a2283-788">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="a2283-788">driving license number</span></span>  <br/> <span data-ttu-id="a2283-789">permissão de condução</span><span class="sxs-lookup"><span data-stu-id="a2283-789">driving permit</span></span>  <br/> <span data-ttu-id="a2283-790">número de permissão de dirigir</span><span class="sxs-lookup"><span data-stu-id="a2283-790">driving permit number</span></span>  <br/> <span data-ttu-id="a2283-791">permiso de conducción</span><span class="sxs-lookup"><span data-stu-id="a2283-791">permiso de conducción</span></span>  <br/> <span data-ttu-id="a2283-792">permiso conducción</span><span class="sxs-lookup"><span data-stu-id="a2283-792">permiso conducción</span></span>  <br/> <span data-ttu-id="a2283-793">número licencia conducir</span><span class="sxs-lookup"><span data-stu-id="a2283-793">número licencia conducir</span></span>  <br/> <span data-ttu-id="a2283-794">número de Carnet de conducir</span><span class="sxs-lookup"><span data-stu-id="a2283-794">número de carnet de conducir</span></span>  <br/> <span data-ttu-id="a2283-795">número Carnet conducir</span><span class="sxs-lookup"><span data-stu-id="a2283-795">número carnet conducir</span></span>  <br/> <span data-ttu-id="a2283-796">licencia conducir</span><span class="sxs-lookup"><span data-stu-id="a2283-796">licencia conducir</span></span>  <br/> <span data-ttu-id="a2283-797">número de permiso de conducir</span><span class="sxs-lookup"><span data-stu-id="a2283-797">número de permiso de conducir</span></span>  <br/> <span data-ttu-id="a2283-798">número de permiso conducir</span><span class="sxs-lookup"><span data-stu-id="a2283-798">número de permiso conducir</span></span>  <br/> <span data-ttu-id="a2283-799">número permiso conducir</span><span class="sxs-lookup"><span data-stu-id="a2283-799">número permiso conducir</span></span>  <br/> <span data-ttu-id="a2283-800">permiso conducir</span><span class="sxs-lookup"><span data-stu-id="a2283-800">permiso conducir</span></span>  <br/> <span data-ttu-id="a2283-801">licencia de manejo</span><span class="sxs-lookup"><span data-stu-id="a2283-801">licencia de manejo</span></span>  <br/> <span data-ttu-id="a2283-802">El Carnet de conducir</span><span class="sxs-lookup"><span data-stu-id="a2283-802">el carnet de conducir</span></span>  <br/> <span data-ttu-id="a2283-803">Carnet conducir</span><span class="sxs-lookup"><span data-stu-id="a2283-803">carnet conducir</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="a2283-804">Suécia</span><span class="sxs-lookup"><span data-stu-id="a2283-804">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="a2283-805">Formato</span><span class="sxs-lookup"><span data-stu-id="a2283-805">Format</span></span>

<span data-ttu-id="a2283-806">Dez dígitos contendo um hífen</span><span class="sxs-lookup"><span data-stu-id="a2283-806">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2283-807">Padrão</span><span class="sxs-lookup"><span data-stu-id="a2283-807">Pattern</span></span>

<span data-ttu-id="a2283-808">Dez dígitos contendo um hífen:</span><span class="sxs-lookup"><span data-stu-id="a2283-808">Ten digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="a2283-809">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="a2283-809">Six digits</span></span> 
    
- <span data-ttu-id="a2283-810">Um hífen</span><span class="sxs-lookup"><span data-stu-id="a2283-810">A hyphen</span></span>
    
- <span data-ttu-id="a2283-811">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="a2283-811">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a2283-812">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a2283-812">Checksum</span></span>

<span data-ttu-id="a2283-813">Não</span><span class="sxs-lookup"><span data-stu-id="a2283-813">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2283-814">Definição</span><span class="sxs-lookup"><span data-stu-id="a2283-814">Definition</span></span>

<span data-ttu-id="a2283-815">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a2283-815">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2283-816">A expressão `Regex_sweden_eu_driver's_license_number` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a2283-816">The regular expression  `Regex_sweden_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2283-817">Uma palavra- `Keywords_sweden_eu_driver's_license_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="a2283-817">A keyword from  `Keywords_sweden_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_driver's_license_number" />
          <Match idRef="Keywords_sweden_eu_driver's_license_number" />
        </Pattern>
</Entity> 
```

### <a name="keywords"></a><span data-ttu-id="a2283-818">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a2283-818">Keywords</span></span>

<span data-ttu-id="a2283-819">| |</span><span class="sxs-lookup"><span data-stu-id="a2283-819"></span></span>
|<span data-ttu-id="a2283-820">**Keywords_sweden_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a2283-820">**Keywords_sweden_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2283-821">distribuição</span><span class="sxs-lookup"><span data-stu-id="a2283-821">dl#</span></span>  <br/> <span data-ttu-id="a2283-822">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-822">driver license</span></span>  <br/> <span data-ttu-id="a2283-823">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-823">driver license number</span></span>  <br/> <span data-ttu-id="a2283-824">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a2283-824">driver licence</span></span>  <br/> <span data-ttu-id="a2283-825">drivers driver'lic.</span><span class="sxs-lookup"><span data-stu-id="a2283-825">drivers lic.</span></span>  <br/> <span data-ttu-id="a2283-826">licença de drivers</span><span class="sxs-lookup"><span data-stu-id="a2283-826">drivers license</span></span>  <br/> <span data-ttu-id="a2283-827">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2283-827">drivers licence</span></span>  <br/> <span data-ttu-id="a2283-828">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-828">driver's license</span></span>  <br/> <span data-ttu-id="a2283-829">número da carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a2283-829">driver's license number</span></span>  <br/> <span data-ttu-id="a2283-830">número de licença do driver</span><span class="sxs-lookup"><span data-stu-id="a2283-830">driver's licence number</span></span>  <br/> <span data-ttu-id="a2283-831">número da licença de dirigir</span><span class="sxs-lookup"><span data-stu-id="a2283-831">driving license number</span></span>  <br/> <span data-ttu-id="a2283-832">dlno #</span><span class="sxs-lookup"><span data-stu-id="a2283-832">dlno#</span></span>  <br/> <span data-ttu-id="a2283-833">körkort</span><span class="sxs-lookup"><span data-stu-id="a2283-833">körkort</span></span>  <br/> |
   
## <a name="uk"></a><span data-ttu-id="a2283-834">Reino Unido</span><span class="sxs-lookup"><span data-stu-id="a2283-834">UK</span></span>

<span data-ttu-id="a2283-p103">Para obter detalhes, consulte a seção "número da carteira de motorista do Reino Unido" em [o que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="a2283-p103">For details, see the section "U.K. Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a2283-837">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2283-837">See also</span></span>

[<span data-ttu-id="a2283-838">O que os tipos de informação confidencial procuram</span><span class="sxs-lookup"><span data-stu-id="a2283-838">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)


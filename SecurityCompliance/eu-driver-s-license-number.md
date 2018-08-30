---
title: Número de carteira de motorista da UE
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: c3923cd3-ec84-435f-bf41-cadc37996a4b
description: Este tópico mostra o que uma política de prevenção (DLP) de perda de dados procura por quando ele detectar o tipo de informação confidencial número de carteira de motorista da UE. Esse tipo de informações confidenciais define diferentes padrões, palavras-chave e outras evidências para cada país.
ms.openlocfilehash: 065684249f9766d567c63e6b8170d36f56692e45
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524018"
---
# <a name="eu-drivers-license-number"></a><span data-ttu-id="a70fe-104">Número de carteira de motorista da UE</span><span class="sxs-lookup"><span data-stu-id="a70fe-104">EU Driver's License Number</span></span>

<span data-ttu-id="a70fe-p102">Este tópico mostra o que uma política de prevenção (DLP) de perda de dados procura por quando ele detectar o tipo de informação confidencial número de carteira de motorista da UE. Esse tipo de informações confidenciais define diferentes padrões, palavras-chave e outras evidências para cada país.</span><span class="sxs-lookup"><span data-stu-id="a70fe-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Driver's License Number sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="a70fe-107">Áustria</span><span class="sxs-lookup"><span data-stu-id="a70fe-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="a70fe-108">Formato</span><span class="sxs-lookup"><span data-stu-id="a70fe-108">Format</span></span>

<span data-ttu-id="a70fe-109">Oito dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="a70fe-109">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a70fe-110">Padrão</span><span class="sxs-lookup"><span data-stu-id="a70fe-110">Pattern</span></span>

<span data-ttu-id="a70fe-111">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="a70fe-111">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a70fe-112">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a70fe-112">Checksum</span></span>

<span data-ttu-id="a70fe-113">Não</span><span class="sxs-lookup"><span data-stu-id="a70fe-113">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a70fe-114">Definição</span><span class="sxs-lookup"><span data-stu-id="a70fe-114">Definition</span></span>

<span data-ttu-id="a70fe-115">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a70fe-115">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a70fe-116">A expressão regular `Regex_austria_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a70fe-116">The regular expression  `Regex_austria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a70fe-117">Uma palavra-chave da `Keywords_austria_eu_driver's_license_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="a70fe-117">A keyword from  `Keywords_austria_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_driver's_license_number" />
          <Match idRef="Keywords_austria_eu_driver's_license_number" />
        </Pattern>
    </Entity>

```

### <a name="keywords"></a><span data-ttu-id="a70fe-118">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a70fe-118">Keywords</span></span>

<span data-ttu-id="a70fe-119">| |</span><span class="sxs-lookup"><span data-stu-id="a70fe-119"></span></span>
|<span data-ttu-id="a70fe-120">**Keywords_austria_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a70fe-120">**Keywords_austria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a70fe-121">DL #</span><span class="sxs-lookup"><span data-stu-id="a70fe-121">dl#</span></span>  <br/> <span data-ttu-id="a70fe-122">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-122">driver license</span></span>  <br/> <span data-ttu-id="a70fe-123">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-123">driver license number</span></span>  <br/> <span data-ttu-id="a70fe-124">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-124">driver licence</span></span>  <br/> <span data-ttu-id="a70fe-125">lic drivers.</span><span class="sxs-lookup"><span data-stu-id="a70fe-125">drivers lic.</span></span>  <br/> <span data-ttu-id="a70fe-126">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-126">drivers license</span></span>  <br/> <span data-ttu-id="a70fe-127">licença de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-127">driver's licence</span></span>  <br/> <span data-ttu-id="a70fe-128">de motorista carteira</span><span class="sxs-lookup"><span data-stu-id="a70fe-128">driver's license</span></span>  <br/> <span data-ttu-id="a70fe-129">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-129">driver's license number</span></span>  <br/> <span data-ttu-id="a70fe-130">número de licença de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-130">driver's licence number</span></span>  <br/>  <span data-ttu-id="a70fe-131">número de carteira de dirigir</span><span class="sxs-lookup"><span data-stu-id="a70fe-131">driving license number</span></span>  <br/> <span data-ttu-id="a70fe-132">dlno #</span><span class="sxs-lookup"><span data-stu-id="a70fe-132">dlno#</span></span>  <br/> <span data-ttu-id="a70fe-133">fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="a70fe-133">fuhrerschein</span></span>  <br/> <span data-ttu-id="a70fe-134">fuhrerschein republik osterreich</span><span class="sxs-lookup"><span data-stu-id="a70fe-134">fuhrerschein republik osterreich</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="a70fe-135">Bélgica</span><span class="sxs-lookup"><span data-stu-id="a70fe-135">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="a70fe-136">Formato</span><span class="sxs-lookup"><span data-stu-id="a70fe-136">Format</span></span>

<span data-ttu-id="a70fe-137">10 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="a70fe-137">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a70fe-138">Padrão</span><span class="sxs-lookup"><span data-stu-id="a70fe-138">Pattern</span></span>

<span data-ttu-id="a70fe-139">10 dígitos</span><span class="sxs-lookup"><span data-stu-id="a70fe-139">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a70fe-140">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a70fe-140">Checksum</span></span>

<span data-ttu-id="a70fe-141">Não</span><span class="sxs-lookup"><span data-stu-id="a70fe-141">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a70fe-142">Definição</span><span class="sxs-lookup"><span data-stu-id="a70fe-142">Definition</span></span>

<span data-ttu-id="a70fe-143">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a70fe-143">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a70fe-144">A expressão regular `Regex_belgium_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a70fe-144">The regular expression  `Regex_belgium_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a70fe-145">Uma palavra-chave da `Keywords_belgium_eu_driver's_license_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="a70fe-145">A keyword from  `Keywords_belgium_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_driver's_license_number" />
          <Match idRef="Keywords_belgium_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="a70fe-146">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a70fe-146">Keywords</span></span>

<span data-ttu-id="a70fe-147">| |</span><span class="sxs-lookup"><span data-stu-id="a70fe-147"></span></span>
|<span data-ttu-id="a70fe-148">**Keywords__belgium_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a70fe-148">**Keywords__belgium_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a70fe-149">DL #</span><span class="sxs-lookup"><span data-stu-id="a70fe-149">dl#</span></span>  <br/> <span data-ttu-id="a70fe-150">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-150">driver license</span></span>  <br/> <span data-ttu-id="a70fe-151">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-151">driver license number</span></span>  <br/> <span data-ttu-id="a70fe-152">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-152">driver licence</span></span>  <br/> <span data-ttu-id="a70fe-153">lic drivers.</span><span class="sxs-lookup"><span data-stu-id="a70fe-153">drivers lic.</span></span>  <br/> <span data-ttu-id="a70fe-154">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-154">drivers license</span></span>  <br/> <span data-ttu-id="a70fe-155">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a70fe-155">drivers licence</span></span>  <br/> <span data-ttu-id="a70fe-156">de motorista carteira</span><span class="sxs-lookup"><span data-stu-id="a70fe-156">driver's license</span></span>  <br/> <span data-ttu-id="a70fe-157">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-157">driver's license number</span></span>  <br/> <span data-ttu-id="a70fe-158">número de licença de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-158">driver's licence number</span></span>  <br/> <span data-ttu-id="a70fe-159">dlno #</span><span class="sxs-lookup"><span data-stu-id="a70fe-159">dlno#</span></span>  <br/> <span data-ttu-id="a70fe-160">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="a70fe-160">rijbewijs</span></span>  <br/> <span data-ttu-id="a70fe-161">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="a70fe-161">rijbewijsnummer</span></span>  <br/> <span data-ttu-id="a70fe-162">führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a70fe-162">führerscheinnummer</span></span>  <br/> <span data-ttu-id="a70fe-163">fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a70fe-163">fuhrerscheinnummer</span></span>  <br/> <span data-ttu-id="a70fe-164">fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a70fe-164">fuehrerscheinnummer</span></span>  <br/> <span data-ttu-id="a70fe-165">führerschein-nr</span><span class="sxs-lookup"><span data-stu-id="a70fe-165">führerschein- nr</span></span>  <br/> <span data-ttu-id="a70fe-166">fuehrerschein-Nr</span><span class="sxs-lookup"><span data-stu-id="a70fe-166">fuehrerschein- Nr</span></span>  <br/> <span data-ttu-id="a70fe-167">fuehrerschein-nr</span><span class="sxs-lookup"><span data-stu-id="a70fe-167">fuehrerschein- nr</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="a70fe-168">Bulgária</span><span class="sxs-lookup"><span data-stu-id="a70fe-168">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="a70fe-169">Formato</span><span class="sxs-lookup"><span data-stu-id="a70fe-169">Format</span></span>

<span data-ttu-id="a70fe-170">Nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="a70fe-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a70fe-171">Padrão</span><span class="sxs-lookup"><span data-stu-id="a70fe-171">Pattern</span></span>

<span data-ttu-id="a70fe-172">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="a70fe-172">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a70fe-173">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a70fe-173">Checksum</span></span>

<span data-ttu-id="a70fe-174">Não</span><span class="sxs-lookup"><span data-stu-id="a70fe-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a70fe-175">Definição</span><span class="sxs-lookup"><span data-stu-id="a70fe-175">Definition</span></span>

<span data-ttu-id="a70fe-176">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a70fe-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a70fe-177">A expressão regular `Regex_bulgaria_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a70fe-177">The regular expression  `Regex_bulgaria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a70fe-178">Uma palavra-chave da `Keywords_bulgaria_eu_driver's_license_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="a70fe-178">A keyword from  `Keywords_bulgaria_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
             <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_driver's_license_number" />
          <Match idRef="Keywords_bulgaria_eu_driver's_license_number" />
        </Pattern> 
</Entity>    

```

### <a name="keywords"></a><span data-ttu-id="a70fe-179">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a70fe-179">Keywords</span></span>

<span data-ttu-id="a70fe-180">| |</span><span class="sxs-lookup"><span data-stu-id="a70fe-180"></span></span>
|<span data-ttu-id="a70fe-181">**Keywords_bulgaria_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a70fe-181">**Keywords_bulgaria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a70fe-182">DL #</span><span class="sxs-lookup"><span data-stu-id="a70fe-182">dl#</span></span>  <br/> <span data-ttu-id="a70fe-183">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-183">driver license</span></span>  <br/> <span data-ttu-id="a70fe-184">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-184">driver license number</span></span>  <br/> <span data-ttu-id="a70fe-185">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-185">driver licence</span></span>  <br/> <span data-ttu-id="a70fe-186">lic drivers.</span><span class="sxs-lookup"><span data-stu-id="a70fe-186">drivers lic.</span></span>  <br/> <span data-ttu-id="a70fe-187">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-187">drivers license</span></span>  <br/> <span data-ttu-id="a70fe-188">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a70fe-188">drivers licence</span></span>  <br/> <span data-ttu-id="a70fe-189">de motorista carteira</span><span class="sxs-lookup"><span data-stu-id="a70fe-189">driver's license</span></span>  <br/> <span data-ttu-id="a70fe-190">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-190">driver's license number</span></span>  <br/> <span data-ttu-id="a70fe-191">número de licença de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-191">driver's licence number</span></span>  <br/> <span data-ttu-id="a70fe-192">número de carteira de dirigir</span><span class="sxs-lookup"><span data-stu-id="a70fe-192">driving license number</span></span>  <br/> <span data-ttu-id="a70fe-193">dlno #</span><span class="sxs-lookup"><span data-stu-id="a70fe-193">dlno#</span></span>  <br/> <span data-ttu-id="a70fe-194">СВИДЕТЕЛСТВО ЗА УПРАВЛЕНИЕ НА МПС</span><span class="sxs-lookup"><span data-stu-id="a70fe-194">свидетелство за управление на мпс</span></span>  <br/> <span data-ttu-id="a70fe-195">СВИДЕТЕЛСТВО ЗА УПРАВЛЕНИЕ НА МОТОРНО ПРЕВОЗНО СРЕДСТВО</span><span class="sxs-lookup"><span data-stu-id="a70fe-195">свидетелство за управление на моторно превозно средство</span></span>  <br/> <span data-ttu-id="a70fe-196">СУМПС</span><span class="sxs-lookup"><span data-stu-id="a70fe-196">сумпс</span></span>  <br/> <span data-ttu-id="a70fe-197">ШОФЬОРСКА КНИЖКА</span><span class="sxs-lookup"><span data-stu-id="a70fe-197">шофьорска книжка</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="a70fe-198">Croácia</span><span class="sxs-lookup"><span data-stu-id="a70fe-198">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="a70fe-199">Formato</span><span class="sxs-lookup"><span data-stu-id="a70fe-199">Format</span></span>

<span data-ttu-id="a70fe-200">Oito dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="a70fe-200">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a70fe-201">Padrão</span><span class="sxs-lookup"><span data-stu-id="a70fe-201">Pattern</span></span>

<span data-ttu-id="a70fe-202">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="a70fe-202">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a70fe-203">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a70fe-203">Checksum</span></span>

<span data-ttu-id="a70fe-204">Não</span><span class="sxs-lookup"><span data-stu-id="a70fe-204">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a70fe-205">Definição</span><span class="sxs-lookup"><span data-stu-id="a70fe-205">Definition</span></span>

<span data-ttu-id="a70fe-206">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a70fe-206">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a70fe-207">A expressão regular `Regex_croatia_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a70fe-207">The regular expression  `Regex_croatia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a70fe-208">Uma palavra-chave da `Keywords_croatia_eu_driver's_license_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="a70fe-208">A keyword from  `Keywords_croatia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_driver's_license_number" />
          <Match idRef="Keywords_croatia_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="a70fe-209">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a70fe-209">Keywords</span></span>

<span data-ttu-id="a70fe-210">| |</span><span class="sxs-lookup"><span data-stu-id="a70fe-210"></span></span>
|<span data-ttu-id="a70fe-211">**Keywords_croatia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a70fe-211">**Keywords_croatia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a70fe-212">DL #</span><span class="sxs-lookup"><span data-stu-id="a70fe-212">dl#</span></span>  <br/> <span data-ttu-id="a70fe-213">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-213">driver license</span></span>  <br/> <span data-ttu-id="a70fe-214">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-214">driver license number</span></span>  <br/> <span data-ttu-id="a70fe-215">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-215">driver licence</span></span>  <br/> <span data-ttu-id="a70fe-216">lic drivers.</span><span class="sxs-lookup"><span data-stu-id="a70fe-216">drivers lic.</span></span>  <br/> <span data-ttu-id="a70fe-217">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-217">drivers license</span></span>  <br/> <span data-ttu-id="a70fe-218">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a70fe-218">drivers licence</span></span>  <br/> <span data-ttu-id="a70fe-219">de motorista carteira</span><span class="sxs-lookup"><span data-stu-id="a70fe-219">driver's license</span></span>  <br/> <span data-ttu-id="a70fe-220">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-220">driver's license number</span></span>  <br/> <span data-ttu-id="a70fe-221">número de licença de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-221">driver's licence number</span></span>  <br/> <span data-ttu-id="a70fe-222">número de carteira de dirigir</span><span class="sxs-lookup"><span data-stu-id="a70fe-222">driving license number</span></span>  <br/> <span data-ttu-id="a70fe-223">dlno #</span><span class="sxs-lookup"><span data-stu-id="a70fe-223">dlno#</span></span>  <br/> <span data-ttu-id="a70fe-224">vozačka dozvola</span><span class="sxs-lookup"><span data-stu-id="a70fe-224">vozačka dozvola</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="a70fe-225">Chipre</span><span class="sxs-lookup"><span data-stu-id="a70fe-225">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="a70fe-226">Formato</span><span class="sxs-lookup"><span data-stu-id="a70fe-226">Format</span></span>

<span data-ttu-id="a70fe-227">12 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="a70fe-227">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a70fe-228">Padrão</span><span class="sxs-lookup"><span data-stu-id="a70fe-228">Pattern</span></span>

<span data-ttu-id="a70fe-229">12 dígitos</span><span class="sxs-lookup"><span data-stu-id="a70fe-229">12 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a70fe-230">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a70fe-230">Checksum</span></span>

<span data-ttu-id="a70fe-231">Não</span><span class="sxs-lookup"><span data-stu-id="a70fe-231">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a70fe-232">Definição</span><span class="sxs-lookup"><span data-stu-id="a70fe-232">Definition</span></span>

<span data-ttu-id="a70fe-233">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a70fe-233">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a70fe-234">A expressão regular `Regex_cyprus_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a70fe-234">The regular expression  `Regex_cyprus_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a70fe-235">Uma palavra-chave da `Keywords_cyprus_eu_driver's_license_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="a70fe-235">A keyword from  `Keywords_cyprus_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_driver's_license_number" />
          <Match idRef="Keywords_cyprus_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a70fe-236">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a70fe-236">Keywords</span></span>

<span data-ttu-id="a70fe-237">| |</span><span class="sxs-lookup"><span data-stu-id="a70fe-237"></span></span>
|<span data-ttu-id="a70fe-238">**Keywords_cyprus_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a70fe-238">**Keywords_cyprus_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a70fe-239">DL #</span><span class="sxs-lookup"><span data-stu-id="a70fe-239">dl#</span></span>  <br/> <span data-ttu-id="a70fe-240">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-240">driver license</span></span>  <br/> <span data-ttu-id="a70fe-241">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-241">driver license number</span></span>  <br/> <span data-ttu-id="a70fe-242">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-242">driver licence</span></span>  <br/> <span data-ttu-id="a70fe-243">lic drivers.</span><span class="sxs-lookup"><span data-stu-id="a70fe-243">drivers lic.</span></span>  <br/> <span data-ttu-id="a70fe-244">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-244">drivers license</span></span>  <br/> <span data-ttu-id="a70fe-245">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a70fe-245">drivers licence</span></span>  <br/> <span data-ttu-id="a70fe-246">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-246">driver's license number</span></span>  <br/> <span data-ttu-id="a70fe-247">número de licença de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-247">driver's licence number</span></span>  <br/> <span data-ttu-id="a70fe-248">número de carteira de dirigir</span><span class="sxs-lookup"><span data-stu-id="a70fe-248">driving license number</span></span>  <br/> <span data-ttu-id="a70fe-249">dlno #</span><span class="sxs-lookup"><span data-stu-id="a70fe-249">dlno#</span></span>  <br/> <span data-ttu-id="a70fe-250">ΆΔΕΙΑ ΟΔΉΓΗΣΗΣ</span><span class="sxs-lookup"><span data-stu-id="a70fe-250">άδεια οδήγησης</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="a70fe-251">República Tcheca</span><span class="sxs-lookup"><span data-stu-id="a70fe-251">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="a70fe-252">Formato</span><span class="sxs-lookup"><span data-stu-id="a70fe-252">Format</span></span>

<span data-ttu-id="a70fe-253">Duas letras seguidas de seis dígitos</span><span class="sxs-lookup"><span data-stu-id="a70fe-253">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a70fe-254">Padrão</span><span class="sxs-lookup"><span data-stu-id="a70fe-254">Pattern</span></span>

<span data-ttu-id="a70fe-255">Oito letras e dígitos:</span><span class="sxs-lookup"><span data-stu-id="a70fe-255">Eight letters and digits:</span></span>
  
- <span data-ttu-id="a70fe-256">Duas letras (não diferencia maiusculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="a70fe-256">Two letters (not case-sensitive)</span></span>
    
- <span data-ttu-id="a70fe-257">Um espaço (opcional)</span><span class="sxs-lookup"><span data-stu-id="a70fe-257">A space (optional)</span></span>
    
- <span data-ttu-id="a70fe-258">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="a70fe-258">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a70fe-259">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a70fe-259">Checksum</span></span>

<span data-ttu-id="a70fe-260">Não</span><span class="sxs-lookup"><span data-stu-id="a70fe-260">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a70fe-261">Definição</span><span class="sxs-lookup"><span data-stu-id="a70fe-261">Definition</span></span>

<span data-ttu-id="a70fe-262">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a70fe-262">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a70fe-263">A expressão regular `Regex_czech_republic_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a70fe-263">The regular expression  `Regex_czech_republic_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a70fe-264">Uma palavra-chave da `Keywords_czech_republic_eu_driver's_license_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="a70fe-264">A keyword from  `Keywords_czech_republic_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_driver's_license_number" />
          <Match idRef="Keywords_czech_republic_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="a70fe-265">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a70fe-265">Keywords</span></span>

<span data-ttu-id="a70fe-266">| |</span><span class="sxs-lookup"><span data-stu-id="a70fe-266"></span></span>
|<span data-ttu-id="a70fe-267">**Keywords_czech_republic_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a70fe-267">**Keywords_czech_republic_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a70fe-268">DL #</span><span class="sxs-lookup"><span data-stu-id="a70fe-268">dl#</span></span>  <br/> <span data-ttu-id="a70fe-269">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-269">driver license</span></span>  <br/> <span data-ttu-id="a70fe-270">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-270">driver license number</span></span>  <br/> <span data-ttu-id="a70fe-271">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-271">driver licence</span></span>  <br/> <span data-ttu-id="a70fe-272">lic drivers.</span><span class="sxs-lookup"><span data-stu-id="a70fe-272">drivers lic.</span></span>  <br/> <span data-ttu-id="a70fe-273">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-273">drivers license</span></span>  <br/> <span data-ttu-id="a70fe-274">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a70fe-274">drivers licence</span></span>  <br/> <span data-ttu-id="a70fe-275">de motorista carteira</span><span class="sxs-lookup"><span data-stu-id="a70fe-275">driver's license</span></span>  <br/> <span data-ttu-id="a70fe-276">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-276">driver's license number</span></span>  <br/> <span data-ttu-id="a70fe-277">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-277">driver's license number</span></span>  <br/> <span data-ttu-id="a70fe-278">número de licença de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-278">driver's licence number</span></span>  <br/> <span data-ttu-id="a70fe-279">número de carteira de dirigir</span><span class="sxs-lookup"><span data-stu-id="a70fe-279">driving license number</span></span>  <br/> <span data-ttu-id="a70fe-280">dlno #</span><span class="sxs-lookup"><span data-stu-id="a70fe-280">dlno#</span></span>  <br/> <span data-ttu-id="a70fe-281">Řidičský prúkaz</span><span class="sxs-lookup"><span data-stu-id="a70fe-281">řidičský prúkaz</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="a70fe-282">Dinamarca</span><span class="sxs-lookup"><span data-stu-id="a70fe-282">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="a70fe-283">Formato</span><span class="sxs-lookup"><span data-stu-id="a70fe-283">Format</span></span>

<span data-ttu-id="a70fe-284">Oito dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="a70fe-284">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a70fe-285">Padrão</span><span class="sxs-lookup"><span data-stu-id="a70fe-285">Pattern</span></span>

<span data-ttu-id="a70fe-286">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="a70fe-286">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a70fe-287">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a70fe-287">Checksum</span></span>

<span data-ttu-id="a70fe-288">Sim</span><span class="sxs-lookup"><span data-stu-id="a70fe-288">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="a70fe-289">Definição</span><span class="sxs-lookup"><span data-stu-id="a70fe-289">Definition</span></span>

<span data-ttu-id="a70fe-290">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a70fe-290">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a70fe-291">A expressão regular `Regex_denmark_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a70fe-291">The regular expression  `Regex_denmark_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a70fe-292">Uma palavra-chave da `Keywords_denmark_eu_driver's_license_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="a70fe-292">A keyword from  `Keywords_denmark_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_driver's_license_number" />
          <Match idRef="Keywords_denmark_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="a70fe-293">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a70fe-293">Keywords</span></span>

<span data-ttu-id="a70fe-294">| |</span><span class="sxs-lookup"><span data-stu-id="a70fe-294"></span></span>
|<span data-ttu-id="a70fe-295">**Keywords_denmark_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a70fe-295">**Keywords_denmark_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a70fe-296">DL #</span><span class="sxs-lookup"><span data-stu-id="a70fe-296">dl#</span></span>  <br/> <span data-ttu-id="a70fe-297">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-297">driver license</span></span>  <br/> <span data-ttu-id="a70fe-298">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-298">driver license number</span></span>  <br/> <span data-ttu-id="a70fe-299">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-299">driver licence</span></span>  <br/> <span data-ttu-id="a70fe-300">lic drivers.</span><span class="sxs-lookup"><span data-stu-id="a70fe-300">drivers lic.</span></span>  <br/> <span data-ttu-id="a70fe-301">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-301">drivers license</span></span>  <br/> <span data-ttu-id="a70fe-302">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a70fe-302">drivers licence</span></span>  <br/> <span data-ttu-id="a70fe-303">de motorista carteira</span><span class="sxs-lookup"><span data-stu-id="a70fe-303">driver's license</span></span>  <br/> <span data-ttu-id="a70fe-304">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-304">driver's license number</span></span>  <br/> <span data-ttu-id="a70fe-305">número de licença de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-305">driver's licence number</span></span>  <br/> <span data-ttu-id="a70fe-306">número de carteira de dirigir</span><span class="sxs-lookup"><span data-stu-id="a70fe-306">driving license number</span></span>  <br/> <span data-ttu-id="a70fe-307">dlno #</span><span class="sxs-lookup"><span data-stu-id="a70fe-307">dlno#</span></span>  <br/> <span data-ttu-id="a70fe-308">kørekort</span><span class="sxs-lookup"><span data-stu-id="a70fe-308">kørekort</span></span>  <br/> <span data-ttu-id="a70fe-309">kørekortnummer</span><span class="sxs-lookup"><span data-stu-id="a70fe-309">kørekortnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="a70fe-310">Estônia</span><span class="sxs-lookup"><span data-stu-id="a70fe-310">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="a70fe-311">Formato</span><span class="sxs-lookup"><span data-stu-id="a70fe-311">Format</span></span>

<span data-ttu-id="a70fe-312">Duas letras seguidas de seis dígitos</span><span class="sxs-lookup"><span data-stu-id="a70fe-312">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a70fe-313">Padrão</span><span class="sxs-lookup"><span data-stu-id="a70fe-313">Pattern</span></span>

<span data-ttu-id="a70fe-314">Duas letras e seis dígitos:</span><span class="sxs-lookup"><span data-stu-id="a70fe-314">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="a70fe-315">As letras "ET" (não diferencia maiusculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="a70fe-315">The letters "ET" (not case-sensitive)</span></span> 
    
- <span data-ttu-id="a70fe-316">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="a70fe-316">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a70fe-317">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a70fe-317">Checksum</span></span>

<span data-ttu-id="a70fe-318">Não</span><span class="sxs-lookup"><span data-stu-id="a70fe-318">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a70fe-319">Definição</span><span class="sxs-lookup"><span data-stu-id="a70fe-319">Definition</span></span>

<span data-ttu-id="a70fe-320">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a70fe-320">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a70fe-321">A expressão regular `Regex_estonia_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a70fe-321">The regular expression  `Regex_estonia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a70fe-322">Uma palavra-chave da `Keywords_estonia_eu_driver's_license_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="a70fe-322">A keyword from  `Keywords_estonia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_driver's_license_number" />
          <Match idRef="Keywords_estonia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a70fe-323">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a70fe-323">Keywords</span></span>

<span data-ttu-id="a70fe-324">| |</span><span class="sxs-lookup"><span data-stu-id="a70fe-324"></span></span>
|<span data-ttu-id="a70fe-325">**Keywords_estonia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a70fe-325">**Keywords_estonia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a70fe-326">DL #</span><span class="sxs-lookup"><span data-stu-id="a70fe-326">dl#</span></span>  <br/> <span data-ttu-id="a70fe-327">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-327">driver license</span></span>  <br/> <span data-ttu-id="a70fe-328">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-328">driver license number</span></span>  <br/> <span data-ttu-id="a70fe-329">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-329">driver license number</span></span>  <br/> <span data-ttu-id="a70fe-330">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-330">driver licence</span></span>  <br/> <span data-ttu-id="a70fe-331">lic drivers.</span><span class="sxs-lookup"><span data-stu-id="a70fe-331">drivers lic.</span></span>  <br/> <span data-ttu-id="a70fe-332">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-332">drivers license</span></span>  <br/> <span data-ttu-id="a70fe-333">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a70fe-333">drivers licence</span></span>  <br/> <span data-ttu-id="a70fe-334">de motorista carteira</span><span class="sxs-lookup"><span data-stu-id="a70fe-334">driver's license</span></span>  <br/> <span data-ttu-id="a70fe-335">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-335">driver's license number</span></span>  <br/> <span data-ttu-id="a70fe-336">número de carteira de dirigir</span><span class="sxs-lookup"><span data-stu-id="a70fe-336">driving license number</span></span>  <br/> <span data-ttu-id="a70fe-337">dlno #</span><span class="sxs-lookup"><span data-stu-id="a70fe-337">dlno#</span></span>  <br/> <span data-ttu-id="a70fe-338">
permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a70fe-338">permis de conduire</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="a70fe-339">Finlândia</span><span class="sxs-lookup"><span data-stu-id="a70fe-339">Finland</span></span>

### <a name="format"></a><span data-ttu-id="a70fe-340">Formato</span><span class="sxs-lookup"><span data-stu-id="a70fe-340">Format</span></span>

<span data-ttu-id="a70fe-341">10 dígitos que contêm um hífen</span><span class="sxs-lookup"><span data-stu-id="a70fe-341">10 digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a70fe-342">Padrão</span><span class="sxs-lookup"><span data-stu-id="a70fe-342">Pattern</span></span>

<span data-ttu-id="a70fe-343">10 dígitos que contém um hífen:</span><span class="sxs-lookup"><span data-stu-id="a70fe-343">10 digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="a70fe-344">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="a70fe-344">Six digits</span></span> 
    
- <span data-ttu-id="a70fe-345">Um hífen</span><span class="sxs-lookup"><span data-stu-id="a70fe-345">A hyphen</span></span>
    
-  <span data-ttu-id="a70fe-346">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="a70fe-346">Four digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="a70fe-347">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a70fe-347">Checksum</span></span>

<span data-ttu-id="a70fe-348">Não</span><span class="sxs-lookup"><span data-stu-id="a70fe-348">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a70fe-349">Definição</span><span class="sxs-lookup"><span data-stu-id="a70fe-349">Definition</span></span>

<span data-ttu-id="a70fe-350">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a70fe-350">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a70fe-351">A expressão regular `Regex_finland_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a70fe-351">The regular expression  `Regex_finland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a70fe-352">Uma palavra-chave da `Keywords_finland_eu_driver's_license_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="a70fe-352">A keyword from  `Keywords_finland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_driver's_license_number" />
          <Match idRef="Keywords_finland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a70fe-353">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a70fe-353">Keywords</span></span>

<span data-ttu-id="a70fe-354">| |</span><span class="sxs-lookup"><span data-stu-id="a70fe-354"></span></span>
|<span data-ttu-id="a70fe-355">**Keywords_finland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a70fe-355">**Keywords_finland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a70fe-356">DL #</span><span class="sxs-lookup"><span data-stu-id="a70fe-356">dl#</span></span>  <br/> <span data-ttu-id="a70fe-357">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-357">driver license</span></span>  <br/> <span data-ttu-id="a70fe-358">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-358">driver license number</span></span>  <br/> <span data-ttu-id="a70fe-359">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-359">driver licence</span></span>  <br/> <span data-ttu-id="a70fe-360">lic drivers.</span><span class="sxs-lookup"><span data-stu-id="a70fe-360">drivers lic.</span></span>  <br/> <span data-ttu-id="a70fe-361">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-361">drivers license</span></span>  <br/> <span data-ttu-id="a70fe-362">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a70fe-362">drivers licence</span></span>  <br/> <span data-ttu-id="a70fe-363">de motorista carteira</span><span class="sxs-lookup"><span data-stu-id="a70fe-363">driver's license</span></span>  <br/> <span data-ttu-id="a70fe-364">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-364">driver's license number</span></span>  <br/> <span data-ttu-id="a70fe-365">número de licença de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-365">driver's licence number</span></span>  <br/> <span data-ttu-id="a70fe-366">número de carteira de dirigir</span><span class="sxs-lookup"><span data-stu-id="a70fe-366">driving license number</span></span>  <br/> <span data-ttu-id="a70fe-367">dlno #</span><span class="sxs-lookup"><span data-stu-id="a70fe-367">dlno#</span></span>  <br/> <span data-ttu-id="a70fe-368">ajokortti</span><span class="sxs-lookup"><span data-stu-id="a70fe-368">ajokortti</span></span>  <br/> |
   
## <a name="france"></a><span data-ttu-id="a70fe-369">França</span><span class="sxs-lookup"><span data-stu-id="a70fe-369">France</span></span>

<span data-ttu-id="a70fe-370">Para obter detalhes, consulte a seção "Número de carteira de motorista da França" nos [quais os tipos de informações confidenciais procurar](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="a70fe-370">For details, see the section "France Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="a70fe-371">Alemanha</span><span class="sxs-lookup"><span data-stu-id="a70fe-371">Germany</span></span>

<span data-ttu-id="a70fe-372">Para obter detalhes, consulte a seção "Número de carteira de motorista da Alemanha" em [quais tipos de informações confidenciais a procurar](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="a70fe-372">For details, see the section "German Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="a70fe-373">Grécia</span><span class="sxs-lookup"><span data-stu-id="a70fe-373">Greece</span></span>

### <a name="format"></a><span data-ttu-id="a70fe-374">Formato</span><span class="sxs-lookup"><span data-stu-id="a70fe-374">Format</span></span>

<span data-ttu-id="a70fe-375">Nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="a70fe-375">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a70fe-376">Padrão</span><span class="sxs-lookup"><span data-stu-id="a70fe-376">Pattern</span></span>

 <span data-ttu-id="a70fe-377">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="a70fe-377">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="a70fe-378">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a70fe-378">Checksum</span></span>

<span data-ttu-id="a70fe-379">Não</span><span class="sxs-lookup"><span data-stu-id="a70fe-379">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a70fe-380">Definição</span><span class="sxs-lookup"><span data-stu-id="a70fe-380">Definition</span></span>

<span data-ttu-id="a70fe-381">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a70fe-381">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a70fe-382">A expressão regular `Regex_greece_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a70fe-382">The regular expression  `Regex_greece_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a70fe-383">Uma palavra-chave da `Keywords_greece_eu_driver's_license_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="a70fe-383">A keyword from  `Keywords_greece_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_driver's_license_number" />
          <Match idRef="Keywords_greece_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a70fe-384">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a70fe-384">Keywords</span></span>

<span data-ttu-id="a70fe-385">| |</span><span class="sxs-lookup"><span data-stu-id="a70fe-385"></span></span>
|<span data-ttu-id="a70fe-386">**Keywords_greece_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a70fe-386">**Keywords_greece_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a70fe-387">dlL #</span><span class="sxs-lookup"><span data-stu-id="a70fe-387">dlL#</span></span>  <br/> <span data-ttu-id="a70fe-388">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-388">driver license</span></span>  <br/> <span data-ttu-id="a70fe-389">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-389">driver license number</span></span>  <br/> <span data-ttu-id="a70fe-390">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-390">driver licence</span></span>  <br/> <span data-ttu-id="a70fe-391">lic drivers.</span><span class="sxs-lookup"><span data-stu-id="a70fe-391">drivers lic.</span></span>  <br/> <span data-ttu-id="a70fe-392">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-392">drivers license</span></span>  <br/> <span data-ttu-id="a70fe-393">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a70fe-393">drivers licence</span></span>  <br/> <span data-ttu-id="a70fe-394">de motorista carteira</span><span class="sxs-lookup"><span data-stu-id="a70fe-394">driver's license</span></span>  <br/> <span data-ttu-id="a70fe-395">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-395">driver's license number</span></span>  <br/> <span data-ttu-id="a70fe-396">número de licença de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-396">driver's licence number</span></span>  <br/> <span data-ttu-id="a70fe-397">número de carteira de dirigir</span><span class="sxs-lookup"><span data-stu-id="a70fe-397">driving license number</span></span>  <br/> <span data-ttu-id="a70fe-398">dlno #</span><span class="sxs-lookup"><span data-stu-id="a70fe-398">dlno#</span></span>  <br/> <span data-ttu-id="a70fe-399">ΔΕΙΑ ΟΔΉΓΗΣΗΣ</span><span class="sxs-lookup"><span data-stu-id="a70fe-399">δεια οδήγησης</span></span>  <br/> <span data-ttu-id="a70fe-400">Adeia odigisis</span><span class="sxs-lookup"><span data-stu-id="a70fe-400">Adeia odigisis</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="a70fe-401">Hungria</span><span class="sxs-lookup"><span data-stu-id="a70fe-401">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="a70fe-402">Formato</span><span class="sxs-lookup"><span data-stu-id="a70fe-402">Format</span></span>

<span data-ttu-id="a70fe-403">Duas letras seguidas de seis dígitos</span><span class="sxs-lookup"><span data-stu-id="a70fe-403">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a70fe-404">Padrão</span><span class="sxs-lookup"><span data-stu-id="a70fe-404">Pattern</span></span>

<span data-ttu-id="a70fe-405">Duas letras e seis dígitos:</span><span class="sxs-lookup"><span data-stu-id="a70fe-405">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="a70fe-406">Duas letras (não diferencia maiusculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="a70fe-406">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="a70fe-407">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="a70fe-407">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a70fe-408">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a70fe-408">Checksum</span></span>

<span data-ttu-id="a70fe-409">Não</span><span class="sxs-lookup"><span data-stu-id="a70fe-409">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a70fe-410">Definição</span><span class="sxs-lookup"><span data-stu-id="a70fe-410">Definition</span></span>

<span data-ttu-id="a70fe-411">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a70fe-411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a70fe-412">A expressão regular `Regex_hungary_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a70fe-412">The regular expression  `Regex_hungary_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a70fe-413">Uma palavra-chave da `Keywords_hungary_eu_driver's_license_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="a70fe-413">A keyword from  `Keywords_hungary_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_driver's_license_number" />
          <Match idRef="Keywords_hungary_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a70fe-414">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a70fe-414">Keywords</span></span>

<span data-ttu-id="a70fe-415">| |</span><span class="sxs-lookup"><span data-stu-id="a70fe-415"></span></span>
|<span data-ttu-id="a70fe-416">**Keywords_hungary_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a70fe-416">**Keywords_hungary_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a70fe-417">DL #</span><span class="sxs-lookup"><span data-stu-id="a70fe-417">dl#</span></span>  <br/> <span data-ttu-id="a70fe-418">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-418">driver license</span></span>  <br/> <span data-ttu-id="a70fe-419">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-419">driver license number</span></span>  <br/> <span data-ttu-id="a70fe-420">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-420">driver licence</span></span>  <br/> <span data-ttu-id="a70fe-421">lic drivers.</span><span class="sxs-lookup"><span data-stu-id="a70fe-421">drivers lic.</span></span>  <br/> <span data-ttu-id="a70fe-422">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-422">drivers license</span></span>  <br/> <span data-ttu-id="a70fe-423">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a70fe-423">drivers licence</span></span>  <br/> <span data-ttu-id="a70fe-424">de motorista carteira</span><span class="sxs-lookup"><span data-stu-id="a70fe-424">driver's license</span></span>  <br/> <span data-ttu-id="a70fe-425">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-425">driver's license number</span></span>  <br/> <span data-ttu-id="a70fe-426">número de licença de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-426">driver's licence number</span></span>  <br/> <span data-ttu-id="a70fe-427">número de carteira de dirigir</span><span class="sxs-lookup"><span data-stu-id="a70fe-427">driving license number</span></span>  <br/> <span data-ttu-id="a70fe-428">dlno #</span><span class="sxs-lookup"><span data-stu-id="a70fe-428">dlno#</span></span>  <br/> <span data-ttu-id="a70fe-429">vezetoi engedely</span><span class="sxs-lookup"><span data-stu-id="a70fe-429">vezetoi engedely</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="a70fe-430">Irlanda</span><span class="sxs-lookup"><span data-stu-id="a70fe-430">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="a70fe-431">Formato</span><span class="sxs-lookup"><span data-stu-id="a70fe-431">Format</span></span>

<span data-ttu-id="a70fe-432">Seis dígitos seguidos por quatro letras</span><span class="sxs-lookup"><span data-stu-id="a70fe-432">Six digits followed by four letters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a70fe-433">Padrão</span><span class="sxs-lookup"><span data-stu-id="a70fe-433">Pattern</span></span>

<span data-ttu-id="a70fe-434">Seis dígitos e quatro letras:</span><span class="sxs-lookup"><span data-stu-id="a70fe-434">Six digits and four letters:</span></span>
  
- <span data-ttu-id="a70fe-435">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="a70fe-435">Six digits</span></span>
    
- <span data-ttu-id="a70fe-436">Quatro letras (não diferencia maiusculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="a70fe-436">Four letters (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a70fe-437">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a70fe-437">Checksum</span></span>

<span data-ttu-id="a70fe-438">Não</span><span class="sxs-lookup"><span data-stu-id="a70fe-438">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a70fe-439">Definição</span><span class="sxs-lookup"><span data-stu-id="a70fe-439">Definition</span></span>

<span data-ttu-id="a70fe-440">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a70fe-440">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a70fe-441">A expressão regular `Regex_ireland_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a70fe-441">The regular expression  `Regex_ireland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a70fe-442">Uma palavra-chave da `Keywords_ireland_eu_driver's_license_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="a70fe-442">A keyword from  `Keywords_ireland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_driver's_license_number" />
          <Match idRef="Keywords_ireland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a70fe-443">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a70fe-443">Keywords</span></span>

<span data-ttu-id="a70fe-444">| |</span><span class="sxs-lookup"><span data-stu-id="a70fe-444"></span></span>
|<span data-ttu-id="a70fe-445">**Keywords_ireland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a70fe-445">**Keywords_ireland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a70fe-446">DL #</span><span class="sxs-lookup"><span data-stu-id="a70fe-446">dl#</span></span>  <br/> <span data-ttu-id="a70fe-447">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-447">driver license</span></span>  <br/> <span data-ttu-id="a70fe-448">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-448">driver license number</span></span>  <br/> <span data-ttu-id="a70fe-449">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-449">driver licence</span></span>  <br/> <span data-ttu-id="a70fe-450">lic drivers.</span><span class="sxs-lookup"><span data-stu-id="a70fe-450">drivers lic.</span></span>  <br/> <span data-ttu-id="a70fe-451">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-451">drivers license</span></span>  <br/> <span data-ttu-id="a70fe-452">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a70fe-452">drivers licence</span></span>  <br/> <span data-ttu-id="a70fe-453">de motorista carteira</span><span class="sxs-lookup"><span data-stu-id="a70fe-453">driver's license</span></span>  <br/> <span data-ttu-id="a70fe-454">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-454">driver's license number</span></span>  <br/> <span data-ttu-id="a70fe-455">número de licença de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-455">driver's licence number</span></span>  <br/> <span data-ttu-id="a70fe-456">número de carteira de dirigir</span><span class="sxs-lookup"><span data-stu-id="a70fe-456">driving license number</span></span>  <br/> <span data-ttu-id="a70fe-457">dlno #</span><span class="sxs-lookup"><span data-stu-id="a70fe-457">dlno#</span></span>  <br/> <span data-ttu-id="a70fe-458">ceadúnas tiomána</span><span class="sxs-lookup"><span data-stu-id="a70fe-458">ceadúnas tiomána</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="a70fe-459">Itália</span><span class="sxs-lookup"><span data-stu-id="a70fe-459">Italy</span></span>

<span data-ttu-id="a70fe-460">Para obter detalhes, consulte a seção "Número de carteira de motorista da Itália" nos [quais os tipos de informações confidenciais procurar](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="a70fe-460">For details, see the section "Italy Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="latvia"></a><span data-ttu-id="a70fe-461">Letônia</span><span class="sxs-lookup"><span data-stu-id="a70fe-461">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="a70fe-462">Formato</span><span class="sxs-lookup"><span data-stu-id="a70fe-462">Format</span></span>

<span data-ttu-id="a70fe-463">Três letras seguidas de seis dígitos</span><span class="sxs-lookup"><span data-stu-id="a70fe-463">Three letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a70fe-464">Padrão</span><span class="sxs-lookup"><span data-stu-id="a70fe-464">Pattern</span></span>

<span data-ttu-id="a70fe-465">Três letras e seis dígitos:</span><span class="sxs-lookup"><span data-stu-id="a70fe-465">Three letters and six digits:</span></span>
  
-  <span data-ttu-id="a70fe-466">Três letras (não diferencia maiusculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="a70fe-466">Three letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="a70fe-467">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="a70fe-467">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a70fe-468">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a70fe-468">Checksum</span></span>

<span data-ttu-id="a70fe-469">Não</span><span class="sxs-lookup"><span data-stu-id="a70fe-469">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a70fe-470">Definição</span><span class="sxs-lookup"><span data-stu-id="a70fe-470">Definition</span></span>

<span data-ttu-id="a70fe-471">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a70fe-471">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a70fe-472">A expressão regular `Regex_latvia_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a70fe-472">The regular expression  `Regex_latvia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a70fe-473">Uma palavra-chave da `Keywords_latvia_eu_driver's_license_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="a70fe-473">A keyword from  `Keywords_latvia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_driver's_license_number" />
          <Match idRef="Keywords_latvia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a70fe-474">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a70fe-474">Keywords</span></span>

<span data-ttu-id="a70fe-475">| |</span><span class="sxs-lookup"><span data-stu-id="a70fe-475"></span></span>
|<span data-ttu-id="a70fe-476">**Keywords_latvia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a70fe-476">**Keywords_latvia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a70fe-477">DL #</span><span class="sxs-lookup"><span data-stu-id="a70fe-477">dl#</span></span>  <br/> <span data-ttu-id="a70fe-478">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-478">driver license</span></span>  <br/> <span data-ttu-id="a70fe-479">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-479">driver license number</span></span>  <br/> <span data-ttu-id="a70fe-480">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-480">driver licence</span></span>  <br/> <span data-ttu-id="a70fe-481">lic drivers.</span><span class="sxs-lookup"><span data-stu-id="a70fe-481">drivers lic.</span></span>  <br/> <span data-ttu-id="a70fe-482">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-482">drivers license</span></span>  <br/> <span data-ttu-id="a70fe-483">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a70fe-483">drivers licence</span></span>  <br/> <span data-ttu-id="a70fe-484">de motorista carteira</span><span class="sxs-lookup"><span data-stu-id="a70fe-484">driver's license</span></span>  <br/> <span data-ttu-id="a70fe-485">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-485">driver's license number</span></span>  <br/> <span data-ttu-id="a70fe-486">número de licença de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-486">driver's licence number</span></span>  <br/> <span data-ttu-id="a70fe-487">número de carteira de dirigir</span><span class="sxs-lookup"><span data-stu-id="a70fe-487">driving license number</span></span>  <br/> <span data-ttu-id="a70fe-488">dlno #</span><span class="sxs-lookup"><span data-stu-id="a70fe-488">dlno#</span></span>  <br/> <span data-ttu-id="a70fe-489">autovadītāja apliecība</span><span class="sxs-lookup"><span data-stu-id="a70fe-489">autovadītāja apliecība</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="a70fe-490">Lituânia</span><span class="sxs-lookup"><span data-stu-id="a70fe-490">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="a70fe-491">Formato</span><span class="sxs-lookup"><span data-stu-id="a70fe-491">Format</span></span>

<span data-ttu-id="a70fe-492">Oito dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="a70fe-492">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a70fe-493">Padrão</span><span class="sxs-lookup"><span data-stu-id="a70fe-493">Pattern</span></span>

 <span data-ttu-id="a70fe-494">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="a70fe-494">Eight digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="a70fe-495">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a70fe-495">Checksum</span></span>

<span data-ttu-id="a70fe-496">Não</span><span class="sxs-lookup"><span data-stu-id="a70fe-496">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a70fe-497">Definição</span><span class="sxs-lookup"><span data-stu-id="a70fe-497">Definition</span></span>

<span data-ttu-id="a70fe-498">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a70fe-498">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a70fe-499">A expressão regular `Regex_lithuania_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a70fe-499">The regular expression  `Regex_lithuania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a70fe-500">Uma palavra-chave da `Keywords_lithuania_eu_driver's_license_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="a70fe-500">A keyword from  `Keywords_lithuania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_driver's_license_number" />
          <Match idRef="Keywords_lithuania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a70fe-501">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a70fe-501">Keywords</span></span>

<span data-ttu-id="a70fe-502">| |</span><span class="sxs-lookup"><span data-stu-id="a70fe-502"></span></span>
|<span data-ttu-id="a70fe-503">**Keywords_lithuania_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a70fe-503">**Keywords_lithuania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a70fe-504">DL #</span><span class="sxs-lookup"><span data-stu-id="a70fe-504">dl#</span></span>  <br/> <span data-ttu-id="a70fe-505">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-505">driver license</span></span>  <br/> <span data-ttu-id="a70fe-506">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-506">driver license number</span></span>  <br/> <span data-ttu-id="a70fe-507">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-507">driver licence</span></span>  <br/> <span data-ttu-id="a70fe-508">lic drivers.</span><span class="sxs-lookup"><span data-stu-id="a70fe-508">drivers lic.</span></span>  <br/> <span data-ttu-id="a70fe-509">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-509">drivers license</span></span>  <br/> <span data-ttu-id="a70fe-510">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a70fe-510">drivers licence</span></span>  <br/> <span data-ttu-id="a70fe-511">de motorista carteira</span><span class="sxs-lookup"><span data-stu-id="a70fe-511">driver's license</span></span>  <br/> <span data-ttu-id="a70fe-512">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-512">driver's license number</span></span>  <br/> <span data-ttu-id="a70fe-513">número de licença de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-513">driver's licence number</span></span>  <br/> <span data-ttu-id="a70fe-514">número de carteira de dirigir</span><span class="sxs-lookup"><span data-stu-id="a70fe-514">driving license number</span></span>  <br/> <span data-ttu-id="a70fe-515">dlno #</span><span class="sxs-lookup"><span data-stu-id="a70fe-515">dlno#</span></span>  <br/> <span data-ttu-id="a70fe-516">vairuotojo pažymėjimas</span><span class="sxs-lookup"><span data-stu-id="a70fe-516">vairuotojo pažymėjimas</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="a70fe-517">Luxemburgo</span><span class="sxs-lookup"><span data-stu-id="a70fe-517">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="a70fe-518">Formato</span><span class="sxs-lookup"><span data-stu-id="a70fe-518">Format</span></span>

<span data-ttu-id="a70fe-519">Seis dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="a70fe-519">Six digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a70fe-520">Padrão</span><span class="sxs-lookup"><span data-stu-id="a70fe-520">Pattern</span></span>

 <span data-ttu-id="a70fe-521">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="a70fe-521">Six digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="a70fe-522">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a70fe-522">Checksum</span></span>

<span data-ttu-id="a70fe-523">Não</span><span class="sxs-lookup"><span data-stu-id="a70fe-523">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a70fe-524">Definição</span><span class="sxs-lookup"><span data-stu-id="a70fe-524">Definition</span></span>

<span data-ttu-id="a70fe-525">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a70fe-525">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a70fe-526">A expressão regular `Regex_luxemburg_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a70fe-526">The regular expression  `Regex_luxemburg_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a70fe-527">Uma palavra-chave da `Keywords_luxemburg_eu_driver's_license_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="a70fe-527">A keyword from  `Keywords_luxemburg_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_driver's_license_number" />
          <Match idRef="Keywords_luxemburg_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a70fe-528">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a70fe-528">Keywords</span></span>

<span data-ttu-id="a70fe-529">| |</span><span class="sxs-lookup"><span data-stu-id="a70fe-529"></span></span>
|<span data-ttu-id="a70fe-530">**Keywords_luxemburg_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a70fe-530">**Keywords_luxemburg_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a70fe-531">DL #</span><span class="sxs-lookup"><span data-stu-id="a70fe-531">dl#</span></span>  <br/> <span data-ttu-id="a70fe-532">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-532">driver license</span></span>  <br/> <span data-ttu-id="a70fe-533">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-533">driver license number</span></span>  <br/> <span data-ttu-id="a70fe-534">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-534">driver licence</span></span>  <br/> <span data-ttu-id="a70fe-535">lic drivers.</span><span class="sxs-lookup"><span data-stu-id="a70fe-535">drivers lic.</span></span>  <br/> <span data-ttu-id="a70fe-536">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-536">drivers license</span></span>  <br/> <span data-ttu-id="a70fe-537">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a70fe-537">drivers licence</span></span>  <br/> <span data-ttu-id="a70fe-538">de motorista carteira</span><span class="sxs-lookup"><span data-stu-id="a70fe-538">driver's license</span></span>  <br/> <span data-ttu-id="a70fe-539">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-539">driver's license number</span></span>  <br/> <span data-ttu-id="a70fe-540">número de licença de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-540">driver's licence number</span></span>  <br/> <span data-ttu-id="a70fe-541">número de carteira de dirigir</span><span class="sxs-lookup"><span data-stu-id="a70fe-541">driving license number</span></span>  <br/> <span data-ttu-id="a70fe-542">dlno #</span><span class="sxs-lookup"><span data-stu-id="a70fe-542">dlno#</span></span>  <br/> <span data-ttu-id="a70fe-543">fahrerlaubnis</span><span class="sxs-lookup"><span data-stu-id="a70fe-543">fahrerlaubnis</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="a70fe-544">Malta</span><span class="sxs-lookup"><span data-stu-id="a70fe-544">Malta</span></span>

### <a name="format"></a><span data-ttu-id="a70fe-545">Formato</span><span class="sxs-lookup"><span data-stu-id="a70fe-545">Format</span></span>

<span data-ttu-id="a70fe-546">Combinação de dois caracteres e seis dígitos no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="a70fe-546">Combination of two characters and six digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a70fe-547">Padrão</span><span class="sxs-lookup"><span data-stu-id="a70fe-547">Pattern</span></span>

<span data-ttu-id="a70fe-548">Combinação de dois caracteres e seis dígitos:</span><span class="sxs-lookup"><span data-stu-id="a70fe-548">Combination of two characters and six digits:</span></span>
  
- <span data-ttu-id="a70fe-549">Dois caracteres (dígitos ou letras, não diferencia maiusculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="a70fe-549">Two characters (digits or letters, not case-sensitive)</span></span>
    
- <span data-ttu-id="a70fe-550">Um espaço (opcional)</span><span class="sxs-lookup"><span data-stu-id="a70fe-550">A space (optional)</span></span>
    
- <span data-ttu-id="a70fe-551">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="a70fe-551">Three digits</span></span>
    
- <span data-ttu-id="a70fe-552">Um espaço (opcional)</span><span class="sxs-lookup"><span data-stu-id="a70fe-552">A space (optional)</span></span>
    
- <span data-ttu-id="a70fe-553">Três dígitos</span><span class="sxs-lookup"><span data-stu-id="a70fe-553">Three digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a70fe-554">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a70fe-554">Checksum</span></span>

<span data-ttu-id="a70fe-555">Não</span><span class="sxs-lookup"><span data-stu-id="a70fe-555">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a70fe-556">Definição</span><span class="sxs-lookup"><span data-stu-id="a70fe-556">Definition</span></span>

<span data-ttu-id="a70fe-557">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a70fe-557">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a70fe-558">A expressão regular `Regex_malta_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a70fe-558">The regular expression  `Regex_malta_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a70fe-559">Uma palavra-chave da `Keywords_malta_eu_driver's_license_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="a70fe-559">A keyword from  `Keywords_malta_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
 <Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_driver's_license_number" />
          <Match idRef="Keywords_malta_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a70fe-560">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a70fe-560">Keywords</span></span>

<span data-ttu-id="a70fe-561">| |</span><span class="sxs-lookup"><span data-stu-id="a70fe-561"></span></span>
|<span data-ttu-id="a70fe-562">**Keywords_malta_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a70fe-562">**Keywords_malta_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a70fe-563">DL #</span><span class="sxs-lookup"><span data-stu-id="a70fe-563">dl#</span></span>  <br/> <span data-ttu-id="a70fe-564">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-564">driver license</span></span>  <br/> <span data-ttu-id="a70fe-565">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-565">driver license number</span></span>  <br/> <span data-ttu-id="a70fe-566">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-566">driver licence</span></span>  <br/> <span data-ttu-id="a70fe-567">lic drivers.</span><span class="sxs-lookup"><span data-stu-id="a70fe-567">drivers lic.</span></span>  <br/> <span data-ttu-id="a70fe-568">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-568">drivers license</span></span>  <br/> <span data-ttu-id="a70fe-569">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a70fe-569">drivers licence</span></span>  <br/> <span data-ttu-id="a70fe-570">de motorista carteira</span><span class="sxs-lookup"><span data-stu-id="a70fe-570">driver's license</span></span>  <br/> <span data-ttu-id="a70fe-571">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-571">driver's license number</span></span>  <br/> <span data-ttu-id="a70fe-572">número de licença de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-572">driver's licence number</span></span>  <br/> <span data-ttu-id="a70fe-573">número de carteira de dirigir</span><span class="sxs-lookup"><span data-stu-id="a70fe-573">driving license number</span></span>  <br/> <span data-ttu-id="a70fe-574">dlno #</span><span class="sxs-lookup"><span data-stu-id="a70fe-574">dlno#</span></span>  <br/> <span data-ttu-id="a70fe-575">tarefa liċenzja-sewqan</span><span class="sxs-lookup"><span data-stu-id="a70fe-575">liċenzja tas-sewqan</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="a70fe-576">Países Baixos</span><span class="sxs-lookup"><span data-stu-id="a70fe-576">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="a70fe-577">Formato</span><span class="sxs-lookup"><span data-stu-id="a70fe-577">Format</span></span>

<span data-ttu-id="a70fe-578">10 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="a70fe-578">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a70fe-579">Padrão</span><span class="sxs-lookup"><span data-stu-id="a70fe-579">Pattern</span></span>

<span data-ttu-id="a70fe-580">10 dígitos</span><span class="sxs-lookup"><span data-stu-id="a70fe-580">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a70fe-581">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a70fe-581">Checksum</span></span>

<span data-ttu-id="a70fe-582">Não</span><span class="sxs-lookup"><span data-stu-id="a70fe-582">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a70fe-583">Definição</span><span class="sxs-lookup"><span data-stu-id="a70fe-583">Definition</span></span>

<span data-ttu-id="a70fe-584">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a70fe-584">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a70fe-585">A expressão regular `Regex_netherlands_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a70fe-585">The regular expression  `Regex_netherlands_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a70fe-586">Uma palavra-chave da `Keywords_netherlands_eu_driver's_license_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="a70fe-586">A keyword from  `Keywords_netherlands_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_driver's_license_number" />
          <Match idRef="Keywords_netherlands_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a70fe-587">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a70fe-587">Keywords</span></span>

<span data-ttu-id="a70fe-588">| |</span><span class="sxs-lookup"><span data-stu-id="a70fe-588"></span></span>
|<span data-ttu-id="a70fe-589">**Keywords_netherlands_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a70fe-589">**Keywords_netherlands_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a70fe-590">DL #</span><span class="sxs-lookup"><span data-stu-id="a70fe-590">dl#</span></span>  <br/> <span data-ttu-id="a70fe-591">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-591">driver license</span></span>  <br/> <span data-ttu-id="a70fe-592">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-592">driver license number</span></span>  <br/> <span data-ttu-id="a70fe-593">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-593">driver licence</span></span>  <br/> <span data-ttu-id="a70fe-594">lic drivers.</span><span class="sxs-lookup"><span data-stu-id="a70fe-594">drivers lic.</span></span>  <br/> <span data-ttu-id="a70fe-595">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-595">drivers license</span></span>  <br/> <span data-ttu-id="a70fe-596">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a70fe-596">drivers licence</span></span>  <br/> <span data-ttu-id="a70fe-597">de motorista carteira</span><span class="sxs-lookup"><span data-stu-id="a70fe-597">driver's license</span></span>  <br/> <span data-ttu-id="a70fe-598">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-598">driver's license number</span></span>  <br/> <span data-ttu-id="a70fe-599">número de licença de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-599">driver's licence number</span></span>  <br/> <span data-ttu-id="a70fe-600">número de carteira de dirigir</span><span class="sxs-lookup"><span data-stu-id="a70fe-600">driving license number</span></span>  <br/> <span data-ttu-id="a70fe-601">dlno #</span><span class="sxs-lookup"><span data-stu-id="a70fe-601">dlno#</span></span>  <br/> <span data-ttu-id="a70fe-602">
permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a70fe-602">permis de conduire</span></span>  <br/> <span data-ttu-id="a70fe-603">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="a70fe-603">rijbewijs</span></span>  <br/> <span data-ttu-id="a70fe-604">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="a70fe-604">rijbewijsnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="a70fe-605">Polônia</span><span class="sxs-lookup"><span data-stu-id="a70fe-605">Poland</span></span>

### <a name="format"></a><span data-ttu-id="a70fe-606">Formato</span><span class="sxs-lookup"><span data-stu-id="a70fe-606">Format</span></span>

<span data-ttu-id="a70fe-607">14 dígitos contendo 2 barras</span><span class="sxs-lookup"><span data-stu-id="a70fe-607">14 digits containing 2 forward slashes</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a70fe-608">Padrão</span><span class="sxs-lookup"><span data-stu-id="a70fe-608">Pattern</span></span>

<span data-ttu-id="a70fe-609">14 dígitos e 2 barras:</span><span class="sxs-lookup"><span data-stu-id="a70fe-609">14 digits and 2 forward slashes:</span></span>
  
-  <span data-ttu-id="a70fe-610">Cinco dígitos</span><span class="sxs-lookup"><span data-stu-id="a70fe-610">Five digits</span></span> 
    
- <span data-ttu-id="a70fe-611">Uma barra</span><span class="sxs-lookup"><span data-stu-id="a70fe-611">A forward slash</span></span>
    
- <span data-ttu-id="a70fe-612">Dois dígitos</span><span class="sxs-lookup"><span data-stu-id="a70fe-612">Two digits</span></span>
    
- <span data-ttu-id="a70fe-613">Uma barra</span><span class="sxs-lookup"><span data-stu-id="a70fe-613">A forward slash</span></span>
    
- <span data-ttu-id="a70fe-614">Sete dígitos</span><span class="sxs-lookup"><span data-stu-id="a70fe-614">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a70fe-615">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a70fe-615">Checksum</span></span>

<span data-ttu-id="a70fe-616">Não</span><span class="sxs-lookup"><span data-stu-id="a70fe-616">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a70fe-617">Definição</span><span class="sxs-lookup"><span data-stu-id="a70fe-617">Definition</span></span>

<span data-ttu-id="a70fe-618">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a70fe-618">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a70fe-619">A expressão regular `Regex_poland_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a70fe-619">The regular expression  `Regex_poland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a70fe-620">Uma palavra-chave da `Keywords_poland_eu_driver's_license_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="a70fe-620">A keyword from  `Keywords_poland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_driver's_license_number" />
          <Match idRef="Keywords_poland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a70fe-621">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a70fe-621">Keywords</span></span>

<span data-ttu-id="a70fe-622">| |</span><span class="sxs-lookup"><span data-stu-id="a70fe-622"></span></span>
|<span data-ttu-id="a70fe-623">**Keywords_poland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a70fe-623">**Keywords_poland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a70fe-624">DL #</span><span class="sxs-lookup"><span data-stu-id="a70fe-624">dl#</span></span>  <br/> <span data-ttu-id="a70fe-625">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-625">driver license</span></span>  <br/> <span data-ttu-id="a70fe-626">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-626">driver license number</span></span>  <br/> <span data-ttu-id="a70fe-627">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-627">driver licence</span></span>  <br/> <span data-ttu-id="a70fe-628">lic drivers.</span><span class="sxs-lookup"><span data-stu-id="a70fe-628">drivers lic.</span></span>  <br/> <span data-ttu-id="a70fe-629">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-629">drivers license</span></span>  <br/> <span data-ttu-id="a70fe-630">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a70fe-630">drivers licence</span></span>  <br/> <span data-ttu-id="a70fe-631">de motorista carteira</span><span class="sxs-lookup"><span data-stu-id="a70fe-631">driver's license</span></span>  <br/> <span data-ttu-id="a70fe-632">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-632">driver's license number</span></span>  <br/> <span data-ttu-id="a70fe-633">número de licença de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-633">driver's licence number</span></span>  <br/> <span data-ttu-id="a70fe-634">número de carteira de dirigir</span><span class="sxs-lookup"><span data-stu-id="a70fe-634">driving license number</span></span>  <br/> <span data-ttu-id="a70fe-635">dlno #</span><span class="sxs-lookup"><span data-stu-id="a70fe-635">dlno#</span></span>  <br/> <span data-ttu-id="a70fe-636">prawo jazdy</span><span class="sxs-lookup"><span data-stu-id="a70fe-636">prawo jazdy</span></span>  <br/> |
   
## <a name="portugal"></a><span data-ttu-id="a70fe-637">Portugal</span><span class="sxs-lookup"><span data-stu-id="a70fe-637">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="a70fe-638">Formato</span><span class="sxs-lookup"><span data-stu-id="a70fe-638">Format</span></span>

<span data-ttu-id="a70fe-639">Duas letras seguidas por um sete números no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="a70fe-639">Two letters followed by a seven numbers in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a70fe-640">Padrão</span><span class="sxs-lookup"><span data-stu-id="a70fe-640">Pattern</span></span>

<span data-ttu-id="a70fe-641">Duas letras seguidas por sete números com caracteres especiais:</span><span class="sxs-lookup"><span data-stu-id="a70fe-641">Two letters followed by seven numbers with special characters:</span></span>
  
-  <span data-ttu-id="a70fe-642">Duas letras (não diferencia maiusculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="a70fe-642">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="a70fe-643">Um hífen</span><span class="sxs-lookup"><span data-stu-id="a70fe-643">A hyphen</span></span>
    
- <span data-ttu-id="a70fe-644">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="a70fe-644">Six digits</span></span>
    
- <span data-ttu-id="a70fe-645">Um espaço</span><span class="sxs-lookup"><span data-stu-id="a70fe-645">A space</span></span>
    
- <span data-ttu-id="a70fe-646">Um dígito</span><span class="sxs-lookup"><span data-stu-id="a70fe-646">One digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a70fe-647">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a70fe-647">Checksum</span></span>

<span data-ttu-id="a70fe-648">Não</span><span class="sxs-lookup"><span data-stu-id="a70fe-648">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a70fe-649">Definição</span><span class="sxs-lookup"><span data-stu-id="a70fe-649">Definition</span></span>

<span data-ttu-id="a70fe-650">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a70fe-650">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a70fe-651">A expressão regular `Regex_portugal_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a70fe-651">The regular expression  `Regex_portugal_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a70fe-652">Uma palavra-chave da `Keywords_portugal_eu_driver's_license_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="a70fe-652">A keyword from  `Keywords_portugal_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_driver's_license_number" />
          <Match idRef="Keywords_portugal_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a70fe-653">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a70fe-653">Keywords</span></span>

<span data-ttu-id="a70fe-654">| |</span><span class="sxs-lookup"><span data-stu-id="a70fe-654"></span></span>
|<span data-ttu-id="a70fe-655">**Keywords_portugal_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a70fe-655">**Keywords_portugal_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a70fe-656">DL #</span><span class="sxs-lookup"><span data-stu-id="a70fe-656">dl#</span></span>  <br/> <span data-ttu-id="a70fe-657">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-657">driver license</span></span>  <br/> <span data-ttu-id="a70fe-658">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-658">driver license number</span></span>  <br/> <span data-ttu-id="a70fe-659">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-659">driver licence</span></span>  <br/> <span data-ttu-id="a70fe-660">lic drivers.</span><span class="sxs-lookup"><span data-stu-id="a70fe-660">drivers lic.</span></span>  <br/> <span data-ttu-id="a70fe-661">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-661">drivers license</span></span>  <br/> <span data-ttu-id="a70fe-662">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a70fe-662">drivers licence</span></span>  <br/> <span data-ttu-id="a70fe-663">de motorista carteira</span><span class="sxs-lookup"><span data-stu-id="a70fe-663">driver's license</span></span>  <br/> <span data-ttu-id="a70fe-664">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-664">driver's license number</span></span>  <br/> <span data-ttu-id="a70fe-665">número de licença de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-665">driver's licence number</span></span>  <br/> <span data-ttu-id="a70fe-666">número de carteira de dirigir</span><span class="sxs-lookup"><span data-stu-id="a70fe-666">driving license number</span></span>  <br/> <span data-ttu-id="a70fe-667">dlno #</span><span class="sxs-lookup"><span data-stu-id="a70fe-667">dlno#</span></span>  <br/> <span data-ttu-id="a70fe-668">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-668">carteira de motorista</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="a70fe-669">Romênia</span><span class="sxs-lookup"><span data-stu-id="a70fe-669">Romania</span></span>

### <a name="format"></a><span data-ttu-id="a70fe-670">Formato</span><span class="sxs-lookup"><span data-stu-id="a70fe-670">Format</span></span>

<span data-ttu-id="a70fe-671">Um caractere seguido oito dígitos</span><span class="sxs-lookup"><span data-stu-id="a70fe-671">One character followed by eight digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a70fe-672">Padrão</span><span class="sxs-lookup"><span data-stu-id="a70fe-672">Pattern</span></span>

<span data-ttu-id="a70fe-673">Um caractere seguido oito dígitos:</span><span class="sxs-lookup"><span data-stu-id="a70fe-673">One character followed by eight digits:</span></span>
  
-  <span data-ttu-id="a70fe-674">Uma letra (não diferencia maiusculas de minúsculas) ou dígito</span><span class="sxs-lookup"><span data-stu-id="a70fe-674">One letter (not case-sensitive) or digit</span></span> 
    
- <span data-ttu-id="a70fe-675">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="a70fe-675">Eight digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a70fe-676">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a70fe-676">Checksum</span></span>

<span data-ttu-id="a70fe-677">Não</span><span class="sxs-lookup"><span data-stu-id="a70fe-677">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a70fe-678">Definição</span><span class="sxs-lookup"><span data-stu-id="a70fe-678">Definition</span></span>

<span data-ttu-id="a70fe-679">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a70fe-679">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a70fe-680">A expressão regular `Regex_romania_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a70fe-680">The regular expression  `Regex_romania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a70fe-681">Uma palavra-chave da `Keywords_romania_eu_driver's_license_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="a70fe-681">A keyword from  `Keywords_romania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_driver's_license_number" />
          <Match idRef="Keywords_romania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a70fe-682">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a70fe-682">Keywords</span></span>

<span data-ttu-id="a70fe-683">| |</span><span class="sxs-lookup"><span data-stu-id="a70fe-683"></span></span>
|<span data-ttu-id="a70fe-684">**Keywords_romania_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a70fe-684">**Keywords_romania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a70fe-685">DL #</span><span class="sxs-lookup"><span data-stu-id="a70fe-685">dl#</span></span>  <br/> <span data-ttu-id="a70fe-686">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-686">driver license</span></span>  <br/> <span data-ttu-id="a70fe-687">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-687">driver license number</span></span>  <br/> <span data-ttu-id="a70fe-688">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-688">driver licence</span></span>  <br/> <span data-ttu-id="a70fe-689">lic drivers.</span><span class="sxs-lookup"><span data-stu-id="a70fe-689">drivers lic.</span></span>  <br/> <span data-ttu-id="a70fe-690">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-690">drivers license</span></span>  <br/> <span data-ttu-id="a70fe-691">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a70fe-691">drivers licence</span></span>  <br/> <span data-ttu-id="a70fe-692">de motorista carteira</span><span class="sxs-lookup"><span data-stu-id="a70fe-692">driver's license</span></span>  <br/> <span data-ttu-id="a70fe-693">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-693">driver's license number</span></span>  <br/> <span data-ttu-id="a70fe-694">número de licença de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-694">driver's licence number</span></span>  <br/> <span data-ttu-id="a70fe-695">número de carteira de dirigir</span><span class="sxs-lookup"><span data-stu-id="a70fe-695">driving license number</span></span>  <br/> <span data-ttu-id="a70fe-696">dlno #</span><span class="sxs-lookup"><span data-stu-id="a70fe-696">dlno#</span></span>  <br/> <span data-ttu-id="a70fe-697">permis de conducere</span><span class="sxs-lookup"><span data-stu-id="a70fe-697">permis de conducere</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="a70fe-698">Eslováquia</span><span class="sxs-lookup"><span data-stu-id="a70fe-698">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="a70fe-699">Formato</span><span class="sxs-lookup"><span data-stu-id="a70fe-699">Format</span></span>

<span data-ttu-id="a70fe-700">Um caractere seguido por sete dígitos</span><span class="sxs-lookup"><span data-stu-id="a70fe-700">One character followed by seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a70fe-701">Padrão</span><span class="sxs-lookup"><span data-stu-id="a70fe-701">Pattern</span></span>

<span data-ttu-id="a70fe-702">Um caractere seguido por sete dígitos</span><span class="sxs-lookup"><span data-stu-id="a70fe-702">One character followed by seven digits</span></span>
  
- <span data-ttu-id="a70fe-703">Uma letra (não diferencia maiusculas de minúsculas) ou dígito</span><span class="sxs-lookup"><span data-stu-id="a70fe-703">One letter (not case-sensitive) or digit</span></span>
    
-  <span data-ttu-id="a70fe-704">Sete dígitos</span><span class="sxs-lookup"><span data-stu-id="a70fe-704">Seven digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="a70fe-705">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a70fe-705">Checksum</span></span>

<span data-ttu-id="a70fe-706">Não</span><span class="sxs-lookup"><span data-stu-id="a70fe-706">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a70fe-707">Definição</span><span class="sxs-lookup"><span data-stu-id="a70fe-707">Definition</span></span>

<span data-ttu-id="a70fe-708">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a70fe-708">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a70fe-709">A expressão regular `Regex_slovakia_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a70fe-709">The regular expression  `Regex_slovakia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a70fe-710">Uma palavra-chave da `Keywords_slovakia_eu_driver's_license_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="a70fe-710">A keyword from  `Keywords_slovakia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovaknia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovakia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a70fe-711">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a70fe-711">Keywords</span></span>

<span data-ttu-id="a70fe-712">| |</span><span class="sxs-lookup"><span data-stu-id="a70fe-712"></span></span>
|<span data-ttu-id="a70fe-713">**Keywords_slovakia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a70fe-713">**Keywords_slovakia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a70fe-714">DL #</span><span class="sxs-lookup"><span data-stu-id="a70fe-714">dl#</span></span>  <br/> <span data-ttu-id="a70fe-715">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-715">driver license</span></span>  <br/> <span data-ttu-id="a70fe-716">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-716">driver license number</span></span>  <br/> <span data-ttu-id="a70fe-717">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-717">driver licence</span></span>  <br/> <span data-ttu-id="a70fe-718">lic drivers.</span><span class="sxs-lookup"><span data-stu-id="a70fe-718">drivers lic.</span></span>  <br/> <span data-ttu-id="a70fe-719">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-719">drivers license</span></span>  <br/> <span data-ttu-id="a70fe-720">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a70fe-720">drivers licence</span></span>  <br/> <span data-ttu-id="a70fe-721">de motorista carteira</span><span class="sxs-lookup"><span data-stu-id="a70fe-721">driver's license</span></span>  <br/> <span data-ttu-id="a70fe-722">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-722">driver's license number</span></span>  <br/> <span data-ttu-id="a70fe-723">número de licença de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-723">driver's licence number</span></span>  <br/> <span data-ttu-id="a70fe-724">número de carteira de dirigir</span><span class="sxs-lookup"><span data-stu-id="a70fe-724">driving license number</span></span>  <br/> <span data-ttu-id="a70fe-725">dlno #</span><span class="sxs-lookup"><span data-stu-id="a70fe-725">dlno#</span></span>  <br/> <span data-ttu-id="a70fe-726">vodičský preukaz</span><span class="sxs-lookup"><span data-stu-id="a70fe-726">vodičský preukaz</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="a70fe-727">Eslovênia</span><span class="sxs-lookup"><span data-stu-id="a70fe-727">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="a70fe-728">Formato</span><span class="sxs-lookup"><span data-stu-id="a70fe-728">Format</span></span>

<span data-ttu-id="a70fe-729">Nove dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="a70fe-729">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a70fe-730">Padrão</span><span class="sxs-lookup"><span data-stu-id="a70fe-730">Pattern</span></span>

<span data-ttu-id="a70fe-731">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="a70fe-731">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a70fe-732">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a70fe-732">Checksum</span></span>

<span data-ttu-id="a70fe-733">Não</span><span class="sxs-lookup"><span data-stu-id="a70fe-733">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a70fe-734">Definição</span><span class="sxs-lookup"><span data-stu-id="a70fe-734">Definition</span></span>

<span data-ttu-id="a70fe-735">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a70fe-735">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a70fe-736">A expressão regular `Regex_slovenia_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a70fe-736">The regular expression  `Regex_slovenia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a70fe-737">Uma palavra-chave da `Keywords_slovenia_eu_driver's_license_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="a70fe-737">A keyword from  `Keywords_slovenia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovenia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a70fe-738">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a70fe-738">Keywords</span></span>

<span data-ttu-id="a70fe-739">| |</span><span class="sxs-lookup"><span data-stu-id="a70fe-739"></span></span>
|<span data-ttu-id="a70fe-740">**Keywords_slovenia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a70fe-740">**Keywords_slovenia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a70fe-741">DL #</span><span class="sxs-lookup"><span data-stu-id="a70fe-741">dl#</span></span>  <br/> <span data-ttu-id="a70fe-742">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-742">driver license</span></span>  <br/> <span data-ttu-id="a70fe-743">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-743">driver license number</span></span>  <br/> <span data-ttu-id="a70fe-744">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-744">driver licence</span></span>  <br/> <span data-ttu-id="a70fe-745">lic drivers.</span><span class="sxs-lookup"><span data-stu-id="a70fe-745">drivers lic.</span></span>  <br/> <span data-ttu-id="a70fe-746">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-746">drivers license</span></span>  <br/> <span data-ttu-id="a70fe-747">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a70fe-747">drivers licence</span></span>  <br/> <span data-ttu-id="a70fe-748">de motorista carteira</span><span class="sxs-lookup"><span data-stu-id="a70fe-748">driver's license</span></span>  <br/> <span data-ttu-id="a70fe-749">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-749">driver's license number</span></span>  <br/> <span data-ttu-id="a70fe-750">número de licença de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-750">driver's licence number</span></span>  <br/> <span data-ttu-id="a70fe-751">número de carteira de dirigir</span><span class="sxs-lookup"><span data-stu-id="a70fe-751">driving license number</span></span>  <br/> <span data-ttu-id="a70fe-752">dlno #</span><span class="sxs-lookup"><span data-stu-id="a70fe-752">dlno#</span></span>  <br/> <span data-ttu-id="a70fe-753">vozniško dovoljenje</span><span class="sxs-lookup"><span data-stu-id="a70fe-753">vozniško dovoljenje</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="a70fe-754">Espanha</span><span class="sxs-lookup"><span data-stu-id="a70fe-754">Spain</span></span>

### <a name="format"></a><span data-ttu-id="a70fe-755">Formato</span><span class="sxs-lookup"><span data-stu-id="a70fe-755">Format</span></span>

<span data-ttu-id="a70fe-756">Oito dígitos seguidos por um caractere</span><span class="sxs-lookup"><span data-stu-id="a70fe-756">Eight digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a70fe-757">Padrão</span><span class="sxs-lookup"><span data-stu-id="a70fe-757">Pattern</span></span>

<span data-ttu-id="a70fe-758">Oito dígitos seguidos por um caractere:</span><span class="sxs-lookup"><span data-stu-id="a70fe-758">Eight digits followed by one character:</span></span>
  
-  <span data-ttu-id="a70fe-759">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="a70fe-759">Eight digits</span></span> 
    
- <span data-ttu-id="a70fe-760">Um dígito ou carta (não diferencia maiusculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="a70fe-760">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a70fe-761">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a70fe-761">Checksum</span></span>

<span data-ttu-id="a70fe-762">Sim</span><span class="sxs-lookup"><span data-stu-id="a70fe-762">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="a70fe-763">Definição</span><span class="sxs-lookup"><span data-stu-id="a70fe-763">Definition</span></span>

<span data-ttu-id="a70fe-764">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a70fe-764">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a70fe-765">A função `Func_spain_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a70fe-765">The function  `Func_spain_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a70fe-766">Uma palavra-chave da `Keywords_spain_eu_driver's_license_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="a70fe-766">A keyword from  `Keywords_spain_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_driver's_license_number" />
          <Match idRef="Keywords_spain_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a70fe-767">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a70fe-767">Keywords</span></span>

<span data-ttu-id="a70fe-768">| |</span><span class="sxs-lookup"><span data-stu-id="a70fe-768"></span></span>
|<span data-ttu-id="a70fe-769">**Keywords_spain_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a70fe-769">**Keywords_spain_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a70fe-770">dlno #</span><span class="sxs-lookup"><span data-stu-id="a70fe-770">dlno#</span></span>  <br/> <span data-ttu-id="a70fe-771">DL #</span><span class="sxs-lookup"><span data-stu-id="a70fe-771">dl#</span></span>  <br/> <span data-ttu-id="a70fe-772">lic drivers.</span><span class="sxs-lookup"><span data-stu-id="a70fe-772">drivers lic.</span></span>  <br/> <span data-ttu-id="a70fe-773">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-773">driver licence</span></span>  <br/> <span data-ttu-id="a70fe-774">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-774">driver license</span></span>  <br/> <span data-ttu-id="a70fe-775">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a70fe-775">drivers licence</span></span>  <br/> <span data-ttu-id="a70fe-776">
drivers license</span><span class="sxs-lookup"><span data-stu-id="a70fe-776">drivers license</span></span>  <br/> <span data-ttu-id="a70fe-777">licença de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-777">driver's licence</span></span>  <br/> <span data-ttu-id="a70fe-778">de motorista carteira</span><span class="sxs-lookup"><span data-stu-id="a70fe-778">driver's license</span></span>  <br/> <span data-ttu-id="a70fe-779">driving licence
</span><span class="sxs-lookup"><span data-stu-id="a70fe-779">driving licence</span></span>  <br/> <span data-ttu-id="a70fe-780">orientando licença</span><span class="sxs-lookup"><span data-stu-id="a70fe-780">driving license</span></span>  <br/> <span data-ttu-id="a70fe-781">número de carteira de licença</span><span class="sxs-lookup"><span data-stu-id="a70fe-781">driver licence number</span></span>  <br/> <span data-ttu-id="a70fe-782">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-782">driver license number</span></span>  <br/> <span data-ttu-id="a70fe-783">número de licenciar drivers</span><span class="sxs-lookup"><span data-stu-id="a70fe-783">drivers licence number</span></span>  <br/> <span data-ttu-id="a70fe-784">número de carteira de drivers</span><span class="sxs-lookup"><span data-stu-id="a70fe-784">drivers license number</span></span>  <br/> <span data-ttu-id="a70fe-785">número de licença de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-785">driver's licence number</span></span>  <br/> <span data-ttu-id="a70fe-786">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-786">driver's license number</span></span>  <br/> <span data-ttu-id="a70fe-787">número de licença driving</span><span class="sxs-lookup"><span data-stu-id="a70fe-787">driving licence number</span></span>  <br/> <span data-ttu-id="a70fe-788">número de carteira de dirigir</span><span class="sxs-lookup"><span data-stu-id="a70fe-788">driving license number</span></span>  <br/> <span data-ttu-id="a70fe-789">orientando permitir</span><span class="sxs-lookup"><span data-stu-id="a70fe-789">driving permit</span></span>  <br/> <span data-ttu-id="a70fe-790">número de permitir que controla</span><span class="sxs-lookup"><span data-stu-id="a70fe-790">driving permit number</span></span>  <br/> <span data-ttu-id="a70fe-791">permiso de conducción</span><span class="sxs-lookup"><span data-stu-id="a70fe-791">permiso de conducción</span></span>  <br/> <span data-ttu-id="a70fe-792">permiso conducción</span><span class="sxs-lookup"><span data-stu-id="a70fe-792">permiso conducción</span></span>  <br/> <span data-ttu-id="a70fe-793">número licencia conducir</span><span class="sxs-lookup"><span data-stu-id="a70fe-793">número licencia conducir</span></span>  <br/> <span data-ttu-id="a70fe-794">número de carnet de conducir</span><span class="sxs-lookup"><span data-stu-id="a70fe-794">número de carnet de conducir</span></span>  <br/> <span data-ttu-id="a70fe-795">número carnet conducir</span><span class="sxs-lookup"><span data-stu-id="a70fe-795">número carnet conducir</span></span>  <br/> <span data-ttu-id="a70fe-796">licencia conducir</span><span class="sxs-lookup"><span data-stu-id="a70fe-796">licencia conducir</span></span>  <br/> <span data-ttu-id="a70fe-797">número de permiso de conducir</span><span class="sxs-lookup"><span data-stu-id="a70fe-797">número de permiso de conducir</span></span>  <br/> <span data-ttu-id="a70fe-798">número de permiso conducir</span><span class="sxs-lookup"><span data-stu-id="a70fe-798">número de permiso conducir</span></span>  <br/> <span data-ttu-id="a70fe-799">número permiso conducir</span><span class="sxs-lookup"><span data-stu-id="a70fe-799">número permiso conducir</span></span>  <br/> <span data-ttu-id="a70fe-800">permiso conducir</span><span class="sxs-lookup"><span data-stu-id="a70fe-800">permiso conducir</span></span>  <br/> <span data-ttu-id="a70fe-801">licencia de manejo</span><span class="sxs-lookup"><span data-stu-id="a70fe-801">licencia de manejo</span></span>  <br/> <span data-ttu-id="a70fe-802">el carnet de conducir</span><span class="sxs-lookup"><span data-stu-id="a70fe-802">el carnet de conducir</span></span>  <br/> <span data-ttu-id="a70fe-803">carnet conducir</span><span class="sxs-lookup"><span data-stu-id="a70fe-803">carnet conducir</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="a70fe-804">Suécia</span><span class="sxs-lookup"><span data-stu-id="a70fe-804">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="a70fe-805">Formato</span><span class="sxs-lookup"><span data-stu-id="a70fe-805">Format</span></span>

<span data-ttu-id="a70fe-806">Dez dígitos que contém um hífen</span><span class="sxs-lookup"><span data-stu-id="a70fe-806">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a70fe-807">Padrão</span><span class="sxs-lookup"><span data-stu-id="a70fe-807">Pattern</span></span>

<span data-ttu-id="a70fe-808">Dez dígitos que contém um hífen:</span><span class="sxs-lookup"><span data-stu-id="a70fe-808">Ten digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="a70fe-809">Seis dígitos</span><span class="sxs-lookup"><span data-stu-id="a70fe-809">Six digits</span></span> 
    
- <span data-ttu-id="a70fe-810">Um hífen</span><span class="sxs-lookup"><span data-stu-id="a70fe-810">A hyphen</span></span>
    
- <span data-ttu-id="a70fe-811">Quatro dígitos</span><span class="sxs-lookup"><span data-stu-id="a70fe-811">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a70fe-812">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="a70fe-812">Checksum</span></span>

<span data-ttu-id="a70fe-813">Não</span><span class="sxs-lookup"><span data-stu-id="a70fe-813">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a70fe-814">Definição</span><span class="sxs-lookup"><span data-stu-id="a70fe-814">Definition</span></span>

<span data-ttu-id="a70fe-815">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="a70fe-815">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a70fe-816">A expressão regular `Regex_sweden_eu_driver's_license_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="a70fe-816">The regular expression  `Regex_sweden_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a70fe-817">Uma palavra-chave da `Keywords_sweden_eu_driver's_license_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="a70fe-817">A keyword from  `Keywords_sweden_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_driver's_license_number" />
          <Match idRef="Keywords_sweden_eu_driver's_license_number" />
        </Pattern>
</Entity> 
```

### <a name="keywords"></a><span data-ttu-id="a70fe-818">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="a70fe-818">Keywords</span></span>

<span data-ttu-id="a70fe-819">| |</span><span class="sxs-lookup"><span data-stu-id="a70fe-819"></span></span>
|<span data-ttu-id="a70fe-820">**Keywords_sweden_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a70fe-820">**Keywords_sweden_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a70fe-821">DL #</span><span class="sxs-lookup"><span data-stu-id="a70fe-821">dl#</span></span>  <br/> <span data-ttu-id="a70fe-822">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-822">driver license</span></span>  <br/> <span data-ttu-id="a70fe-823">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-823">driver license number</span></span>  <br/> <span data-ttu-id="a70fe-824">licença de driver</span><span class="sxs-lookup"><span data-stu-id="a70fe-824">driver licence</span></span>  <br/> <span data-ttu-id="a70fe-825">lic drivers.</span><span class="sxs-lookup"><span data-stu-id="a70fe-825">drivers lic.</span></span>  <br/> <span data-ttu-id="a70fe-826">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-826">drivers license</span></span>  <br/> <span data-ttu-id="a70fe-827">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a70fe-827">drivers licence</span></span>  <br/> <span data-ttu-id="a70fe-828">de motorista carteira</span><span class="sxs-lookup"><span data-stu-id="a70fe-828">driver's license</span></span>  <br/> <span data-ttu-id="a70fe-829">número de carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-829">driver's license number</span></span>  <br/> <span data-ttu-id="a70fe-830">número de licença de motorista</span><span class="sxs-lookup"><span data-stu-id="a70fe-830">driver's licence number</span></span>  <br/> <span data-ttu-id="a70fe-831">número de carteira de dirigir</span><span class="sxs-lookup"><span data-stu-id="a70fe-831">driving license number</span></span>  <br/> <span data-ttu-id="a70fe-832">dlno #</span><span class="sxs-lookup"><span data-stu-id="a70fe-832">dlno#</span></span>  <br/> <span data-ttu-id="a70fe-833">körkort</span><span class="sxs-lookup"><span data-stu-id="a70fe-833">körkort</span></span>  <br/> |
   
## <a name="uk"></a><span data-ttu-id="a70fe-834">REINO UNIDO</span><span class="sxs-lookup"><span data-stu-id="a70fe-834">UK</span></span>

<span data-ttu-id="a70fe-p103">Para obter detalhes, consulte a seção "Número de carteira de motorista do Reino Unido" nos [quais os tipos de informações confidenciais procurar](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="a70fe-p103">For details, see the section "U.K. Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a70fe-837">Confira também</span><span class="sxs-lookup"><span data-stu-id="a70fe-837">See also</span></span>

[<span data-ttu-id="a70fe-838">O que os tipos de informações confidenciais procuram</span><span class="sxs-lookup"><span data-stu-id="a70fe-838">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)


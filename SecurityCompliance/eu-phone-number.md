---
title: Número de telefone da UE
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 1c90ca41-1681-46bf-8ad6-6bf4cec5c426
description: Prevenção de perda de dados (DLP) no Office 365 Security &amp; Centro de conformidade inclui muitos tipos de informações confidenciais que estão prontos para uso em suas políticas de DLP. Este tópico descreve o tipo de informações confidenciais de número de telefone da UE.
ms.openlocfilehash: 9dd878e3385312982f9f3a4927205e3ebb27aabb
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524128"
---
# <a name="eu-phone-number"></a><span data-ttu-id="24d37-104">Número de telefone da UE</span><span class="sxs-lookup"><span data-stu-id="24d37-104">EU Phone Number</span></span>

<span data-ttu-id="24d37-p102">Prevenção de perda de dados (DLP) no Office 365 Security &amp; Centro de conformidade inclui muitos tipos de informações confidenciais que estão prontos para uso em suas políticas de DLP. Este tópico descreve o tipo de informações confidenciais de número de telefone da UE.</span><span class="sxs-lookup"><span data-stu-id="24d37-p102">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies. This topic describes the EU Phone Number sensitive information type.</span></span> 
  
## <a name="austria"></a><span data-ttu-id="24d37-107">Áustria</span><span class="sxs-lookup"><span data-stu-id="24d37-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="24d37-108">Formato</span><span class="sxs-lookup"><span data-stu-id="24d37-108">Format</span></span>

<span data-ttu-id="24d37-109">Nenhum comprimento standard</span><span class="sxs-lookup"><span data-stu-id="24d37-109">No standard length</span></span>
  
### <a name="pattern"></a><span data-ttu-id="24d37-110">Padrão</span><span class="sxs-lookup"><span data-stu-id="24d37-110">Pattern</span></span>

- <span data-ttu-id="24d37-111">Dígitos</span><span class="sxs-lookup"><span data-stu-id="24d37-111">Digits</span></span> 
    
- <span data-ttu-id="24d37-112">Apenas os números de telefone celular começam com o dígito "6"</span><span class="sxs-lookup"><span data-stu-id="24d37-112">Only mobile phone numbers begin with the digit "6"</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="24d37-113">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="24d37-113">Checksum</span></span>

<span data-ttu-id="24d37-114">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="24d37-114">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="24d37-115">Definição</span><span class="sxs-lookup"><span data-stu-id="24d37-115">Definition</span></span>

<span data-ttu-id="24d37-116">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-116">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-117">A expressão regular `Regex_austria_eu_telephone_number_1` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-117">The regular expression  `Regex_austria_eu_telephone_number_1` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="24d37-118">Uma palavra-chave da `Keywords_austria_eu_telephone_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="24d37-118">A keyword from  `Keywords_austria_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="24d37-119">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-119">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-120">A expressão regular `Regex_austria_eu_telephone_number_2` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-120">The regular expression  `Regex_austria_eu_telephone_number_2` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="24d37-121">Uma palavra-chave da `Keywords_austria_eu_telephone_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="24d37-121">A keyword from  `Keywords_austria_eu_telephone_number` is found.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_telephone_number_1" />
          <Match idRef="Keywords_austria_eu_telephone_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_telephone_number_2" />
          <Match idRef="Keywords_austria_eu_telephone_number" />
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_austria_eu_formatted_telephone_number_1" />
          </Pattern>
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_austria_eu_formatted_telephone_number_2" />
          </Pattern>
</Entity>
```

## <a name="belgium"></a><span data-ttu-id="24d37-122">Bélgica</span><span class="sxs-lookup"><span data-stu-id="24d37-122">Belgium</span></span>

### <a name="definition"></a><span data-ttu-id="24d37-123">Definição</span><span class="sxs-lookup"><span data-stu-id="24d37-123">Definition</span></span>

<span data-ttu-id="24d37-124">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-124">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-125">A expressão regular `Regex_belgium_eu_telephone_number_1` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-125">The regular expression  `Regex_belgium_eu_telephone_number_1` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="24d37-126">Uma palavra-chave da `Keywords_belgium_eu_telephone_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="24d37-126">A keyword from  `Keywords_belgium_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="24d37-127">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-127">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-128">A expressão regular `Regex_belgium_eu_telephone_number_2` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-128">The regular expression  `Regex_belgium_eu_telephone_number_2` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="24d37-129">Uma palavra-chave da `Keywords_belgium_eu_telephone_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="24d37-129">A keyword from  `Keywords_belgium_eu_telephone_number` is found.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_telephone_number_1" />
          <Match idRef="Keywords_belgium_eu_telephone_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_telephone_number_2" />
          <Match idRef="Keywords_belgium_eu_telephone_number" />
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_belgium_eu_formatted_telephone_number_1" />
          </Pattern>
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_belgium_eu_formatted_telephone_number_2" />
          </Pattern></Entity>
```

## <a name="bulgaria"></a><span data-ttu-id="24d37-130">Bulgária</span><span class="sxs-lookup"><span data-stu-id="24d37-130">Bulgaria</span></span>

### <a name="pattern"></a><span data-ttu-id="24d37-131">Padrão</span><span class="sxs-lookup"><span data-stu-id="24d37-131">Pattern</span></span>

- <span data-ttu-id="24d37-132">Dígitos</span><span class="sxs-lookup"><span data-stu-id="24d37-132">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="24d37-133">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="24d37-133">Checksum</span></span>

<span data-ttu-id="24d37-134">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="24d37-134">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="24d37-135">Definição</span><span class="sxs-lookup"><span data-stu-id="24d37-135">Definition</span></span>

<span data-ttu-id="24d37-136">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-136">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-137">A expressão regular `Regex_bulgaria_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-137">The regular expression  `Regex_bulgaria_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="24d37-138">Uma palavra-chave da `Keywords_bulgaria_eu_telephone_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="24d37-138">A keyword from  `Keywords_bulgaria_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="24d37-139">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-139">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-140">A expressão regular `Regex_bulgaria_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-140">The regular expression  `Regex_bulgaria_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_telephone_number" />
          <Match idRef="Keywords_bulgaria_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_bulgaria_eu_formatted_telephone_number" />
          </Pattern>
          
</Entity>
```

## <a name="croatia"></a><span data-ttu-id="24d37-141">Croácia</span><span class="sxs-lookup"><span data-stu-id="24d37-141">Croatia</span></span>

### <a name="pattern"></a><span data-ttu-id="24d37-142">Padrão</span><span class="sxs-lookup"><span data-stu-id="24d37-142">Pattern</span></span>

- <span data-ttu-id="24d37-143">Dígitos</span><span class="sxs-lookup"><span data-stu-id="24d37-143">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="24d37-144">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="24d37-144">Checksum</span></span>

<span data-ttu-id="24d37-145">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="24d37-145">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="24d37-146">Definição</span><span class="sxs-lookup"><span data-stu-id="24d37-146">Definition</span></span>

<span data-ttu-id="24d37-147">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-147">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-148">A expressão regular `Regex_croatia_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-148">The regular expression  `Regex_croatia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="24d37-149">Uma palavra-chave da `Keywords_croatia_eu_telephone_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="24d37-149">A keyword from  `Keywords_croatia_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="24d37-150">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-150">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-151">A expressão regular `Regex_croatia_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-151">The regular expression  `Regex_croatia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_telephone_number" />
          <Match idRef="Keywords_croatia_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_croatia_eu_formatted_telephone_number" />
          </Pattern>
         </Entity>
```

## <a name="cyprus"></a><span data-ttu-id="24d37-152">Chipre</span><span class="sxs-lookup"><span data-stu-id="24d37-152">Cyprus</span></span>

### <a name="pattern"></a><span data-ttu-id="24d37-153">Padrão</span><span class="sxs-lookup"><span data-stu-id="24d37-153">Pattern</span></span>

- <span data-ttu-id="24d37-154">Dígitos</span><span class="sxs-lookup"><span data-stu-id="24d37-154">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="24d37-155">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="24d37-155">Checksum</span></span>

<span data-ttu-id="24d37-156">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="24d37-156">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="24d37-157">Definição</span><span class="sxs-lookup"><span data-stu-id="24d37-157">Definition</span></span>

<span data-ttu-id="24d37-158">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-158">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-159">A expressão regular `Regex_cyprus_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-159">The regular expression  `Regex_cyprus_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="24d37-160">Uma palavra-chave da `Keywords_cyprus_eu_telephone_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="24d37-160">A keyword from  `Keywords_cyprus_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="24d37-161">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-161">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-162">A expressão regular `Regex_cyprus_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-162">The regular expression  `Regex_cyprus_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_telephone_number" />
          <Match idRef="Keywords_cyprus_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_cyprus_eu_formatted_telephone_number" />
            </Pattern>
</Entity>
```

## <a name="czech-republic"></a><span data-ttu-id="24d37-163">República Tcheca</span><span class="sxs-lookup"><span data-stu-id="24d37-163">Czech Republic</span></span>

### <a name="pattern"></a><span data-ttu-id="24d37-164">Padrão</span><span class="sxs-lookup"><span data-stu-id="24d37-164">Pattern</span></span>

- <span data-ttu-id="24d37-165">Dígitos</span><span class="sxs-lookup"><span data-stu-id="24d37-165">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="24d37-166">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="24d37-166">Checksum</span></span>

<span data-ttu-id="24d37-167">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="24d37-167">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="24d37-168">Definição</span><span class="sxs-lookup"><span data-stu-id="24d37-168">Definition</span></span>

<span data-ttu-id="24d37-169">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-169">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-170">A expressão regular `Regex_czech_republic_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-170">The regular expression  `Regex_czech_republic_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="24d37-171">Uma palavra-chave da `Keywords_czech_republic_eu_telephone_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="24d37-171">A keyword from  `Keywords_czech_republic_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="24d37-172">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-172">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-173">A expressão regular `Regex_czech_republic_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-173">The regular expression  `Regex_czech_republic_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_telephone_number" />
          <Match idRef="Keywords_czech_republic_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_czech_republic_eu_formatted_telephone_number" />
          </Pattern>
        </Entity>
```

## <a name="denmark"></a><span data-ttu-id="24d37-174">Dinamarca</span><span class="sxs-lookup"><span data-stu-id="24d37-174">Denmark</span></span>

### <a name="pattern"></a><span data-ttu-id="24d37-175">Padrão</span><span class="sxs-lookup"><span data-stu-id="24d37-175">Pattern</span></span>

- <span data-ttu-id="24d37-176">Dígitos</span><span class="sxs-lookup"><span data-stu-id="24d37-176">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="24d37-177">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="24d37-177">Checksum</span></span>

<span data-ttu-id="24d37-178">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="24d37-178">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="24d37-179">Definição</span><span class="sxs-lookup"><span data-stu-id="24d37-179">Definition</span></span>

<span data-ttu-id="24d37-180">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-180">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-181">A expressão regular `Regex_denmark_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-181">The regular expression  `Regex_denmark_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="24d37-182">Uma palavra-chave da `Keywords_denmark_eu_telephone_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="24d37-182">A keyword from  `Keywords_denmark_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="24d37-183">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-183">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-184">A expressão regular `Regex_denmark_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-184">The regular expression  `Regex_denmark_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_telephone_number" />
          <Match idRef="Keywords_denmark_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_denmark_eu_formatted_telephone_number" />
          </Pattern>
          </Entity>
```

## <a name="estonia"></a><span data-ttu-id="24d37-185">Estônia</span><span class="sxs-lookup"><span data-stu-id="24d37-185">Estonia</span></span>

### <a name="pattern"></a><span data-ttu-id="24d37-186">Padrão</span><span class="sxs-lookup"><span data-stu-id="24d37-186">Pattern</span></span>

- <span data-ttu-id="24d37-187">Dígitos</span><span class="sxs-lookup"><span data-stu-id="24d37-187">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="24d37-188">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="24d37-188">Checksum</span></span>

<span data-ttu-id="24d37-189">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="24d37-189">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="24d37-190">Definição</span><span class="sxs-lookup"><span data-stu-id="24d37-190">Definition</span></span>

<span data-ttu-id="24d37-191">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-191">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-192">A expressão regular `Regex_estonia_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-192">The regular expression  `Regex_estonia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="24d37-193">Uma palavra-chave da `Keywords_estonia_eu_telephone_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="24d37-193">A keyword from  `Keywords_estonia_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="24d37-194">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-194">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-195">A expressão regular `Regex_estonia_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-195">The regular expression  `Regex_estonia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_telephone_number" />
          <Match idRef="Keywords_estonia_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_estonia_eu_formatted_telephone_number" />
          </Pattern>
       </Entity>
```

## <a name="finland"></a><span data-ttu-id="24d37-196">Finlândia</span><span class="sxs-lookup"><span data-stu-id="24d37-196">Finland</span></span>

### <a name="pattern"></a><span data-ttu-id="24d37-197">Padrão</span><span class="sxs-lookup"><span data-stu-id="24d37-197">Pattern</span></span>

- <span data-ttu-id="24d37-198">Dígitos</span><span class="sxs-lookup"><span data-stu-id="24d37-198">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="24d37-199">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="24d37-199">Checksum</span></span>

<span data-ttu-id="24d37-200">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="24d37-200">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="24d37-201">Definição</span><span class="sxs-lookup"><span data-stu-id="24d37-201">Definition</span></span>

<span data-ttu-id="24d37-202">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-202">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-203">A expressão regular `Regex_finland_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-203">The regular expression  `Regex_finland_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="24d37-204">Uma palavra-chave da `Keywords_finland_eu_telephone_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="24d37-204">A keyword from  `Keywords_finland_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="24d37-205">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-205">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-206">A expressão regular `Regex_finland_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-206">The regular expression  `Regex_finland_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_telephone_number" />
          <Match idRef="Keywords_finland_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_finland_eu_formatted_telephone_number" />
             </Pattern>
</Entity>
```

## <a name="france"></a><span data-ttu-id="24d37-207">França</span><span class="sxs-lookup"><span data-stu-id="24d37-207">France</span></span>

### <a name="pattern"></a><span data-ttu-id="24d37-208">Padrão</span><span class="sxs-lookup"><span data-stu-id="24d37-208">Pattern</span></span>

- <span data-ttu-id="24d37-209">Dígitos</span><span class="sxs-lookup"><span data-stu-id="24d37-209">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="24d37-210">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="24d37-210">Checksum</span></span>

<span data-ttu-id="24d37-211">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="24d37-211">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="24d37-212">Definição</span><span class="sxs-lookup"><span data-stu-id="24d37-212">Definition</span></span>

<span data-ttu-id="24d37-213">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-213">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-214">A expressão regular `Regex_france_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-214">The regular expression  `Regex_france_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="24d37-215">Uma palavra-chave da `Keywords_france_eu_telephone_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="24d37-215">A keyword from  `Keywords_france_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="24d37-216">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-216">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-217">A expressão regular `Regex_france_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-217">The regular expression  `Regex_france_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_france_eu_telephone_number" />
          <Match idRef="Keywords_france_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_france_eu_formatted_telephone_number" />
          </Pattern>
          </Entity>
```

## <a name="germany"></a><span data-ttu-id="24d37-218">Alemanha</span><span class="sxs-lookup"><span data-stu-id="24d37-218">Germany</span></span>

### <a name="pattern"></a><span data-ttu-id="24d37-219">Padrão</span><span class="sxs-lookup"><span data-stu-id="24d37-219">Pattern</span></span>

- <span data-ttu-id="24d37-220">Dígitos</span><span class="sxs-lookup"><span data-stu-id="24d37-220">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="24d37-221">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="24d37-221">Checksum</span></span>

<span data-ttu-id="24d37-222">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="24d37-222">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="24d37-223">Definição</span><span class="sxs-lookup"><span data-stu-id="24d37-223">Definition</span></span>

<span data-ttu-id="24d37-224">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-224">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-225">A expressão regular `Regex_germany_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-225">The regular expression  `Regex_germany_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="24d37-226">Uma palavra-chave da `Keywords_germany_eu_telephone_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="24d37-226">A keyword from  `Keywords_germany_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="24d37-227">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-227">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-228">A expressão regular `Regex_germany_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-228">The regular expression  `Regex_germany_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_germany_eu_telephone_number" />
          <Match idRef="Keywords_germany_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_germany_eu_formatted_telephone_number" />
          </Pattern>
        </Entity>
```

## <a name="greece"></a><span data-ttu-id="24d37-229">Grécia</span><span class="sxs-lookup"><span data-stu-id="24d37-229">Greece</span></span>

### <a name="pattern"></a><span data-ttu-id="24d37-230">Padrão</span><span class="sxs-lookup"><span data-stu-id="24d37-230">Pattern</span></span>

- <span data-ttu-id="24d37-231">Dígitos</span><span class="sxs-lookup"><span data-stu-id="24d37-231">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="24d37-232">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="24d37-232">Checksum</span></span>

<span data-ttu-id="24d37-233">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="24d37-233">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="24d37-234">Definição</span><span class="sxs-lookup"><span data-stu-id="24d37-234">Definition</span></span>

<span data-ttu-id="24d37-235">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-235">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-236">A expressão regular `Regex_greece_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-236">The regular expression  `Regex_greece_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="24d37-237">Uma palavra-chave da `Keywords_greece_eu_telephone_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="24d37-237">A keyword from  `Keywords_greece_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="24d37-238">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-238">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-239">A expressão regular `Regex_greece_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-239">The regular expression  `Regex_greece_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_telephone_number" />
          <Match idRef="Keywords_greece_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_greece_eu_formatted_telephone_number" />
          </Pattern>
        </Entity>
```

## <a name="hungary"></a><span data-ttu-id="24d37-240">Hungria</span><span class="sxs-lookup"><span data-stu-id="24d37-240">Hungary</span></span>

### <a name="pattern"></a><span data-ttu-id="24d37-241">Padrão</span><span class="sxs-lookup"><span data-stu-id="24d37-241">Pattern</span></span>

- <span data-ttu-id="24d37-242">Dígitos</span><span class="sxs-lookup"><span data-stu-id="24d37-242">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="24d37-243">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="24d37-243">Checksum</span></span>

<span data-ttu-id="24d37-244">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="24d37-244">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="24d37-245">Definição</span><span class="sxs-lookup"><span data-stu-id="24d37-245">Definition</span></span>

<span data-ttu-id="24d37-246">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-246">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-247">A expressão regular `Regex_hungary_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-247">The regular expression  `Regex_hungary_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="24d37-248">Uma palavra-chave da `Keywords_hungary_eu_telephone_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="24d37-248">A keyword from  `Keywords_hungary_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="24d37-249">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-249">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-250">A expressão regular `Regex_hungary_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-250">The regular expression  `Regex_hungary_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_telephone_number" />
          <Match idRef="Keywords_hungary_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_hungary_eu_formatted_telephone_number" />
          </Pattern>
       </Entity>
```

## <a name="ireland"></a><span data-ttu-id="24d37-251">Irlanda</span><span class="sxs-lookup"><span data-stu-id="24d37-251">Ireland</span></span>

### <a name="pattern"></a><span data-ttu-id="24d37-252">Padrão</span><span class="sxs-lookup"><span data-stu-id="24d37-252">Pattern</span></span>

- <span data-ttu-id="24d37-253">Dígitos</span><span class="sxs-lookup"><span data-stu-id="24d37-253">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="24d37-254">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="24d37-254">Checksum</span></span>

<span data-ttu-id="24d37-255">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="24d37-255">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="24d37-256">Definição</span><span class="sxs-lookup"><span data-stu-id="24d37-256">Definition</span></span>

<span data-ttu-id="24d37-257">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-257">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-258">A expressão regular `Regex_ireland_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-258">The regular expression  `Regex_ireland_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="24d37-259">Uma palavra-chave da `Keywords_ireland_eu_telephone_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="24d37-259">A keyword from  `Keywords_ireland_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="24d37-260">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-260">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-261">A expressão regular `Regex_ireland_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-261">The regular expression  `Regex_ireland_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_telephone_number" />
          <Match idRef="Keywords_ireland_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_ireland_eu_formatted_telephone_number" />
          </Pattern>
          </Entity>
```

## <a name="italy"></a><span data-ttu-id="24d37-262">Itália</span><span class="sxs-lookup"><span data-stu-id="24d37-262">Italy</span></span>

### <a name="pattern"></a><span data-ttu-id="24d37-263">Padrão</span><span class="sxs-lookup"><span data-stu-id="24d37-263">Pattern</span></span>

- <span data-ttu-id="24d37-264">Dígitos</span><span class="sxs-lookup"><span data-stu-id="24d37-264">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="24d37-265">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="24d37-265">Checksum</span></span>

<span data-ttu-id="24d37-266">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="24d37-266">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="24d37-267">Definição</span><span class="sxs-lookup"><span data-stu-id="24d37-267">Definition</span></span>

<span data-ttu-id="24d37-268">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-268">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-269">A expressão regular `Regex_italy_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-269">The regular expression  `Regex_italy_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="24d37-270">Uma palavra-chave da `Keywords_italy_eu_telephone_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="24d37-270">A keyword from  `Keywords_italy_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="24d37-271">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-271">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-272">A expressão regular `Regex_italy_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-272">The regular expression  `Regex_italy_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_telephone_number" />
          <Match idRef="Keywords_italy_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_italy_eu_formatted_telephone_number" />
          </Pattern>
         </Entity>
```

## <a name="latvia"></a><span data-ttu-id="24d37-273">Letônia</span><span class="sxs-lookup"><span data-stu-id="24d37-273">Latvia</span></span>

### <a name="pattern"></a><span data-ttu-id="24d37-274">Padrão</span><span class="sxs-lookup"><span data-stu-id="24d37-274">Pattern</span></span>

- <span data-ttu-id="24d37-275">Dígitos</span><span class="sxs-lookup"><span data-stu-id="24d37-275">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="24d37-276">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="24d37-276">Checksum</span></span>

<span data-ttu-id="24d37-277">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="24d37-277">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="24d37-278">Definição</span><span class="sxs-lookup"><span data-stu-id="24d37-278">Definition</span></span>

<span data-ttu-id="24d37-279">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-279">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-280">A expressão regular `Regex_latvia_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-280">The regular expression  `Regex_latvia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="24d37-281">Uma palavra-chave da `Keywords_latvia_eu_telephone_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="24d37-281">A keyword from  `Keywords_latvia_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="24d37-282">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-282">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-283">A expressão regular `Regex_latvia_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-283">The regular expression  `Regex_latvia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_telephone_number" />
          <Match idRef="Keywords_latvia_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_latvia_eu_formatted_telephone_number" />
          </Pattern>
          </Entity>
```

## <a name="lithuania"></a><span data-ttu-id="24d37-284">Lituânia</span><span class="sxs-lookup"><span data-stu-id="24d37-284">Lithuania</span></span>

### <a name="pattern"></a><span data-ttu-id="24d37-285">Padrão</span><span class="sxs-lookup"><span data-stu-id="24d37-285">Pattern</span></span>

- <span data-ttu-id="24d37-286">Dígitos</span><span class="sxs-lookup"><span data-stu-id="24d37-286">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="24d37-287">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="24d37-287">Checksum</span></span>

<span data-ttu-id="24d37-288">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="24d37-288">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="24d37-289">Definição</span><span class="sxs-lookup"><span data-stu-id="24d37-289">Definition</span></span>

<span data-ttu-id="24d37-290">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-290">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-291">A expressão regular `Regex_lithuania_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-291">The regular expression  `Regex_lithuania_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="24d37-292">Uma palavra-chave da `Keywords_lithuania_eu_telephone_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="24d37-292">A keyword from  `Keywords_lithuania_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="24d37-293">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-293">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-294">A expressão regular `Regex_lithuania_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-294">The regular expression  `Regex_lithuania_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_telephone_number" />
          <Match idRef="Keywords_lithuania_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_lithuania_eu_formatted_telephone_number" />
          </Pattern>
          </Entity>
```

## <a name="luxemburg"></a><span data-ttu-id="24d37-295">Luxemburgo</span><span class="sxs-lookup"><span data-stu-id="24d37-295">Luxemburg</span></span>

### <a name="pattern"></a><span data-ttu-id="24d37-296">Padrão</span><span class="sxs-lookup"><span data-stu-id="24d37-296">Pattern</span></span>

- <span data-ttu-id="24d37-297">Dígitos</span><span class="sxs-lookup"><span data-stu-id="24d37-297">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="24d37-298">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="24d37-298">Checksum</span></span>

<span data-ttu-id="24d37-299">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="24d37-299">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="24d37-300">Definição</span><span class="sxs-lookup"><span data-stu-id="24d37-300">Definition</span></span>

<span data-ttu-id="24d37-301">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-301">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-302">A expressão regular `Regex_luxemburg_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-302">The regular expression  `Regex_luxemburg_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="24d37-303">Uma palavra-chave da `Keywords_luxemburg_eu_telephone_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="24d37-303">A keyword from  `Keywords_luxemburg_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="24d37-304">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-304">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-305">A expressão regular `Regex_luxemburg_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-305">The regular expression  `Regex_luxemburg_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_telephone_number" />
          <Match idRef="Keywords_luxemburg_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_luxemburg_eu_formatted_telephone_number" />
                  </Pattern>
</Entity>
```

## <a name="malta"></a><span data-ttu-id="24d37-306">Malta</span><span class="sxs-lookup"><span data-stu-id="24d37-306">Malta</span></span>

### <a name="pattern"></a><span data-ttu-id="24d37-307">Padrão</span><span class="sxs-lookup"><span data-stu-id="24d37-307">Pattern</span></span>

- <span data-ttu-id="24d37-308">Dígitos</span><span class="sxs-lookup"><span data-stu-id="24d37-308">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="24d37-309">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="24d37-309">Checksum</span></span>

<span data-ttu-id="24d37-310">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="24d37-310">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="24d37-311">Definição</span><span class="sxs-lookup"><span data-stu-id="24d37-311">Definition</span></span>

<span data-ttu-id="24d37-312">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-312">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-313">A expressão regular `Regex_malta_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-313">The regular expression  `Regex_malta_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="24d37-314">Uma palavra-chave da `Keywords_malta_eu_telephone_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="24d37-314">A keyword from  `Keywords_malta_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="24d37-315">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-315">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-316">A expressão regular `Regex_malta_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-316">The regular expression  `Regex_malta_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_telephone_number" />
          <Match idRef="Keywords_malta_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_malta_eu_formatted_telephone_number" />
            </Pattern>
</Entity>
```

## <a name="netherlands"></a><span data-ttu-id="24d37-317">Países Baixos</span><span class="sxs-lookup"><span data-stu-id="24d37-317">Netherlands</span></span>

### <a name="pattern"></a><span data-ttu-id="24d37-318">Padrão</span><span class="sxs-lookup"><span data-stu-id="24d37-318">Pattern</span></span>

- <span data-ttu-id="24d37-319">Dígitos</span><span class="sxs-lookup"><span data-stu-id="24d37-319">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="24d37-320">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="24d37-320">Checksum</span></span>

<span data-ttu-id="24d37-321">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="24d37-321">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="24d37-322">Definição</span><span class="sxs-lookup"><span data-stu-id="24d37-322">Definition</span></span>

<span data-ttu-id="24d37-323">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-323">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-324">A expressão regular `Regex_netherlands_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-324">The regular expression  `Regex_netherlands_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="24d37-325">Uma palavra-chave da `Keywords_netherlands_eu_telephone_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="24d37-325">A keyword from  `Keywords_netherlands_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="24d37-326">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-326">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-327">A expressão regular `Regex_netherlands_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-327">The regular expression  `Regex_netherlands_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_telephone_number" />
          <Match idRef="Keywords_netherlands_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_netherlands_eu_formatted_telephone_number" />
            </Pattern>
</Entity>
```

## <a name="poland"></a><span data-ttu-id="24d37-328">Polônia</span><span class="sxs-lookup"><span data-stu-id="24d37-328">Poland</span></span>

### <a name="pattern"></a><span data-ttu-id="24d37-329">Padrão</span><span class="sxs-lookup"><span data-stu-id="24d37-329">Pattern</span></span>

- <span data-ttu-id="24d37-330">Dígitos</span><span class="sxs-lookup"><span data-stu-id="24d37-330">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="24d37-331">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="24d37-331">Checksum</span></span>

<span data-ttu-id="24d37-332">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="24d37-332">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="24d37-333">Definição</span><span class="sxs-lookup"><span data-stu-id="24d37-333">Definition</span></span>

<span data-ttu-id="24d37-334">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-334">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-335">A expressão regular `Regex_poland_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-335">The regular expression  `Regex_poland_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="24d37-336">Uma palavra-chave da `Keywords_poland_eu_telephone_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="24d37-336">A keyword from  `Keywords_poland_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="24d37-337">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-337">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-338">A expressão regular `Regex_poland_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-338">The regular expression  `Regex_poland_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_telephone_number" />
          <Match idRef="Keywords_poland_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_poland_eu_formatted_telephone_number" />
             </Pattern>
</Entity>
```

## <a name="portugal"></a><span data-ttu-id="24d37-339">Portugal</span><span class="sxs-lookup"><span data-stu-id="24d37-339">Portugal</span></span>

### <a name="pattern"></a><span data-ttu-id="24d37-340">Padrão</span><span class="sxs-lookup"><span data-stu-id="24d37-340">Pattern</span></span>

- <span data-ttu-id="24d37-341">Dígitos</span><span class="sxs-lookup"><span data-stu-id="24d37-341">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="24d37-342">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="24d37-342">Checksum</span></span>

<span data-ttu-id="24d37-343">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="24d37-343">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="24d37-344">Definição</span><span class="sxs-lookup"><span data-stu-id="24d37-344">Definition</span></span>

<span data-ttu-id="24d37-345">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-345">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-346">A expressão regular `Regex_portugal_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-346">The regular expression  `Regex_portugal_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="24d37-347">Uma palavra-chave da `Keywords_portugal_eu_telephone_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="24d37-347">A keyword from  `Keywords_portugal_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="24d37-348">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-348">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-349">A expressão regular `Regex_portugal_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-349">The regular expression  `Regex_portugal_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_telephone_number" />
          <Match idRef="Keywords_portugal_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_portugal_eu_formatted_telephone_number" />
          </Pattern>
        </Entity>
```

## <a name="romania"></a><span data-ttu-id="24d37-350">Romênia</span><span class="sxs-lookup"><span data-stu-id="24d37-350">Romania</span></span>

### <a name="pattern"></a><span data-ttu-id="24d37-351">Padrão</span><span class="sxs-lookup"><span data-stu-id="24d37-351">Pattern</span></span>

- <span data-ttu-id="24d37-352">Dígitos</span><span class="sxs-lookup"><span data-stu-id="24d37-352">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="24d37-353">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="24d37-353">Checksum</span></span>

<span data-ttu-id="24d37-354">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="24d37-354">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="24d37-355">Definição</span><span class="sxs-lookup"><span data-stu-id="24d37-355">Definition</span></span>

<span data-ttu-id="24d37-356">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-356">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-357">A expressão regular `Regex_romania_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-357">The regular expression  `Regex_romania_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="24d37-358">Uma palavra-chave da `Keywords_romania_eu_telephone_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="24d37-358">A keyword from  `Keywords_romania_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="24d37-359">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-359">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-360">A expressão regular `Regex_romania_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-360">The regular expression  `Regex_romania_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_telephone_number" />
          <Match idRef="Keywords_romania_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_romania_eu_formatted_telephone_number" />
            </Pattern>
</Entity>
```

## <a name="slovakia"></a><span data-ttu-id="24d37-361">Eslováquia</span><span class="sxs-lookup"><span data-stu-id="24d37-361">Slovakia</span></span>

### <a name="pattern"></a><span data-ttu-id="24d37-362">Padrão</span><span class="sxs-lookup"><span data-stu-id="24d37-362">Pattern</span></span>

- <span data-ttu-id="24d37-363">Dígitos</span><span class="sxs-lookup"><span data-stu-id="24d37-363">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="24d37-364">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="24d37-364">Checksum</span></span>

<span data-ttu-id="24d37-365">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="24d37-365">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="24d37-366">Definição</span><span class="sxs-lookup"><span data-stu-id="24d37-366">Definition</span></span>

<span data-ttu-id="24d37-367">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-367">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-368">A expressão regular `Regex_slovakia_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-368">The regular expression  `Regex_slovakia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="24d37-369">Uma palavra-chave da `Keywords_slovakia_eu_telephone_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="24d37-369">A keyword from  `Keywords_slovakia_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="24d37-370">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-370">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-371">A expressão regular `Regex_slovakia_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-371">The regular expression  `Regex_slovakia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_telephone_number" />
          <Match idRef="Keywords_slovakia_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_slovakia_eu_formatted_telephone_number" />
            </Pattern>
</Entity>
```

## <a name="slovenia"></a><span data-ttu-id="24d37-372">Eslovênia</span><span class="sxs-lookup"><span data-stu-id="24d37-372">Slovenia</span></span>

### <a name="pattern"></a><span data-ttu-id="24d37-373">Padrão</span><span class="sxs-lookup"><span data-stu-id="24d37-373">Pattern</span></span>

- <span data-ttu-id="24d37-374">Dígitos</span><span class="sxs-lookup"><span data-stu-id="24d37-374">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="24d37-375">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="24d37-375">Checksum</span></span>

<span data-ttu-id="24d37-376">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="24d37-376">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="24d37-377">Definição</span><span class="sxs-lookup"><span data-stu-id="24d37-377">Definition</span></span>

<span data-ttu-id="24d37-378">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-378">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-379">A expressão regular `Regex_slovenia_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-379">The regular expression  `Regex_slovenia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="24d37-380">Uma palavra-chave da `Keywords_slovenia_eu_telephone_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="24d37-380">A keyword from  `Keywords_slovenia_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="24d37-381">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-381">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-382">A expressão regular `Regex_slovenia_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-382">The regular expression  `Regex_slovenia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_telephone_number" />
          <Match idRef="Keywords_slovenia_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_slovenia_eu_formatted_telephone_number" />
          </Pattern>
          </Entity>
```

## <a name="spain"></a><span data-ttu-id="24d37-383">Espanha</span><span class="sxs-lookup"><span data-stu-id="24d37-383">Spain</span></span>

### <a name="pattern"></a><span data-ttu-id="24d37-384">Padrão</span><span class="sxs-lookup"><span data-stu-id="24d37-384">Pattern</span></span>

- <span data-ttu-id="24d37-385">Dígitos</span><span class="sxs-lookup"><span data-stu-id="24d37-385">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="24d37-386">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="24d37-386">Checksum</span></span>

<span data-ttu-id="24d37-387">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="24d37-387">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="24d37-388">Definição</span><span class="sxs-lookup"><span data-stu-id="24d37-388">Definition</span></span>

<span data-ttu-id="24d37-389">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-389">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-390">A expressão regular `Regex_spain_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-390">The regular expression  `Regex_spain_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="24d37-391">Uma palavra-chave da `Keywords_spain_eu_telephone_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="24d37-391">A keyword from  `Keywords_spain_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="24d37-392">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-392">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-393">A expressão regular `Regex_spain_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-393">The regular expression  `Regex_spain_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_telephone_number" />
          <Match idRef="Keywords_spain_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_spain_eu_formatted_telephone_number" />
          </Pattern>
          </Entity>
```

## <a name="sweden"></a><span data-ttu-id="24d37-394">Suécia</span><span class="sxs-lookup"><span data-stu-id="24d37-394">Sweden</span></span>

### <a name="pattern"></a><span data-ttu-id="24d37-395">Padrão</span><span class="sxs-lookup"><span data-stu-id="24d37-395">Pattern</span></span>

- <span data-ttu-id="24d37-396">Dígitos</span><span class="sxs-lookup"><span data-stu-id="24d37-396">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="24d37-397">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="24d37-397">Checksum</span></span>

<span data-ttu-id="24d37-398">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="24d37-398">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="24d37-399">Definição</span><span class="sxs-lookup"><span data-stu-id="24d37-399">Definition</span></span>

<span data-ttu-id="24d37-400">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-400">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-401">A expressão regular `Regex_sweden_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-401">The regular expression  `Regex_sweden_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="24d37-402">Uma palavra-chave da `Keywords_sweden_eu_telephone_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="24d37-402">A keyword from  `Keywords_sweden_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="24d37-403">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-403">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-404">A expressão regular `Regex_sweden_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-404">The regular expression  `Regex_sweden_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_telephone_number" />
          <Match idRef="Keywords_sweden_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_sweden_eu_formatted_telephone_number" />
          </Pattern>
          </Entity>
```

## <a name="uk"></a><span data-ttu-id="24d37-405">REINO UNIDO</span><span class="sxs-lookup"><span data-stu-id="24d37-405">UK</span></span>

### <a name="pattern"></a><span data-ttu-id="24d37-406">Padrão</span><span class="sxs-lookup"><span data-stu-id="24d37-406">Pattern</span></span>

- <span data-ttu-id="24d37-407">Dígitos</span><span class="sxs-lookup"><span data-stu-id="24d37-407">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="24d37-408">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="24d37-408">Checksum</span></span>

<span data-ttu-id="24d37-409">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="24d37-409">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="24d37-410">Definição</span><span class="sxs-lookup"><span data-stu-id="24d37-410">Definition</span></span>

<span data-ttu-id="24d37-411">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-412">A expressão regular `Regex_uk_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-412">The regular expression  `Regex_uk_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="24d37-413">Uma palavra-chave da `Keywords_uk_eu_telephone_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="24d37-413">A keyword from  `Keywords_uk_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="24d37-414">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="24d37-414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="24d37-415">A expressão regular `Regex_uk_eu_telephone_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="24d37-415">The regular expression  `Regex_uk_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_uk_eu_telephone_number" />
          <Match idRef="Keywords_uk_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_uk_eu_formatted_telephone_number" />
            </Pattern>
</Entity>
```

## <a name="see-also"></a><span data-ttu-id="24d37-416">Confira também</span><span class="sxs-lookup"><span data-stu-id="24d37-416">See also</span></span>

[<span data-ttu-id="24d37-417">O que os tipos de informações confidenciais procuram</span><span class="sxs-lookup"><span data-stu-id="24d37-417">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)


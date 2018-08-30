---
title: Número de telefone celular da UE
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/16/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 555e7675-2ae8-42d1-9b8e-2c8f8cd21337
description: Prevenção de perda de dados (DLP) no Office 365 Security &amp; Centro de conformidade inclui muitos tipos de informações confidenciais que estão prontos para uso em suas políticas de DLP. Este tópico descreve o tipo de informações confidenciais da UE número de telefone celular.
ms.openlocfilehash: d0818759dae8ed86cc9aef6f7fad48cbd2acf24f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523960"
---
# <a name="eu-mobile-phone-number"></a><span data-ttu-id="4975e-104">Número de telefone celular da UE</span><span class="sxs-lookup"><span data-stu-id="4975e-104">EU Mobile Phone Number</span></span>

<span data-ttu-id="4975e-p102">Prevenção de perda de dados (DLP) no Office 365 Security &amp; Centro de conformidade inclui muitos tipos de informações confidenciais que estão prontos para uso em suas políticas de DLP. Este tópico descreve o tipo de informações confidenciais da UE número de telefone celular.</span><span class="sxs-lookup"><span data-stu-id="4975e-p102">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies. This topic describes the EU Mobile Phone Number sensitive information type.</span></span> 
  
## <a name="austria"></a><span data-ttu-id="4975e-107">Áustria</span><span class="sxs-lookup"><span data-stu-id="4975e-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="4975e-108">Formato</span><span class="sxs-lookup"><span data-stu-id="4975e-108">Format</span></span>

<span data-ttu-id="4975e-109">Dígitos sem comprimentos standard</span><span class="sxs-lookup"><span data-stu-id="4975e-109">Digits without standard lengths</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4975e-110">Padrão</span><span class="sxs-lookup"><span data-stu-id="4975e-110">Pattern</span></span>

-  <span data-ttu-id="4975e-111">Dígitos</span><span class="sxs-lookup"><span data-stu-id="4975e-111">Digits</span></span> 
    
### <a name="definition"></a><span data-ttu-id="4975e-112">Definição</span><span class="sxs-lookup"><span data-stu-id="4975e-112">Definition</span></span>

<span data-ttu-id="4975e-113">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4975e-113">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4975e-114">A expressão regular `Regex_austria_eu_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-114">The regular expression  `Regex_austria_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-115">A expressão regular `Regex_austria_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-115">The regular expression  `Regex_austria_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-116">Uma palavra-chave da `Keywords_austria_eu_mobile_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="4975e-116">A keyword from  `Keywords_austria_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_mobile_number"/>
          <Match idRef="Keywords_austria_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_austria_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="belgium"></a><span data-ttu-id="4975e-117">Bélgica</span><span class="sxs-lookup"><span data-stu-id="4975e-117">Belgium</span></span>

### <a name="pattern"></a><span data-ttu-id="4975e-118">Padrão</span><span class="sxs-lookup"><span data-stu-id="4975e-118">Pattern</span></span>

-  <span data-ttu-id="4975e-119">Dígitos</span><span class="sxs-lookup"><span data-stu-id="4975e-119">Digits</span></span> 
    
### <a name="definition"></a><span data-ttu-id="4975e-120">Definição</span><span class="sxs-lookup"><span data-stu-id="4975e-120">Definition</span></span>

<span data-ttu-id="4975e-121">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4975e-121">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4975e-122">A expressão regular `Regex_belgium_eu_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-122">The regular expression  `Regex_belgium_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-123">A expressão regular `Regex_belgium_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-123">The regular expression  `Regex_belgium_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-124">Uma palavra-chave da `Keywords_belgium_eu_mobile_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="4975e-124">A keyword from  `Keywords_belgium_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_mobile_number"/>
          <Match idRef="Keywords_belgium_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_belgium_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="bulgaria"></a><span data-ttu-id="4975e-125">Bulgária</span><span class="sxs-lookup"><span data-stu-id="4975e-125">Bulgaria</span></span>

### <a name="pattern"></a><span data-ttu-id="4975e-126">Padrão</span><span class="sxs-lookup"><span data-stu-id="4975e-126">Pattern</span></span>

-  <span data-ttu-id="4975e-127">Dígitos</span><span class="sxs-lookup"><span data-stu-id="4975e-127">Digits</span></span> 
    
### <a name="definition"></a><span data-ttu-id="4975e-128">Definição</span><span class="sxs-lookup"><span data-stu-id="4975e-128">Definition</span></span>

<span data-ttu-id="4975e-129">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4975e-129">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4975e-130">A expressão regular `Regex_bulgaria_eu_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-130">The regular expression  `Regex_bulgaria_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-131">A expressão regular `Regex_bulgaria_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-131">The regular expression  `Regex_bulgaria_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-132">Uma palavra-chave da `Keywords_bulgaria_eu_mobile_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="4975e-132">A keyword from  `Keywords_bulgaria_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_mobile_number"/>
          <Match idRef="Keywords_bulgaria_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_bulgaria_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="croatia"></a><span data-ttu-id="4975e-133">Croácia</span><span class="sxs-lookup"><span data-stu-id="4975e-133">Croatia</span></span>

### <a name="pattern"></a><span data-ttu-id="4975e-134">Padrão</span><span class="sxs-lookup"><span data-stu-id="4975e-134">Pattern</span></span>

-  <span data-ttu-id="4975e-135">Dígitos</span><span class="sxs-lookup"><span data-stu-id="4975e-135">Digits</span></span> 
    
### <a name="definition"></a><span data-ttu-id="4975e-136">Definição</span><span class="sxs-lookup"><span data-stu-id="4975e-136">Definition</span></span>

<span data-ttu-id="4975e-137">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4975e-137">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4975e-138">A expressão regular `Regex_croatia_eu_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-138">The regular expression  `Regex_croatia_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-139">A expressão regular `Regex_croatia_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-139">The regular expression  `Regex_croatia_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-140">Uma palavra-chave da `Keywords_croatia_eu_mobile_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="4975e-140">A keyword from  `Keywords_croatia_eu_mobile_number` is found.</span></span> 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_mobile_number"/>
          <Match idRef="Keywords_croatia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_croatia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="cyprus"></a><span data-ttu-id="4975e-141">Chipre</span><span class="sxs-lookup"><span data-stu-id="4975e-141">Cyprus</span></span>

### <a name="pattern"></a><span data-ttu-id="4975e-142">Padrão</span><span class="sxs-lookup"><span data-stu-id="4975e-142">Pattern</span></span>

-  <span data-ttu-id="4975e-143">Dígitos</span><span class="sxs-lookup"><span data-stu-id="4975e-143">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="4975e-144">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="4975e-144">Checksum</span></span>

<span data-ttu-id="4975e-145">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="4975e-145">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="4975e-146">Definição</span><span class="sxs-lookup"><span data-stu-id="4975e-146">Definition</span></span>

<span data-ttu-id="4975e-147">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4975e-147">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4975e-148">A expressão regular `Regex_cyprus_eu_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-148">The regular expression  `Regex_cyprus_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-149">A expressão regular `Regex_cyprus_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-149">The regular expression  `Regex_cyprus_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-150">Uma palavra-chave da `Keywords_cyprus_eu_mobile_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="4975e-150">A keyword from  `Keywords_cyprus_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_mobile_number"/>
          <Match idRef="Keywords_cyprus_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_cyprus_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="czech-republic"></a><span data-ttu-id="4975e-151">República Tcheca</span><span class="sxs-lookup"><span data-stu-id="4975e-151">Czech Republic</span></span>

### <a name="pattern"></a><span data-ttu-id="4975e-152">Padrão</span><span class="sxs-lookup"><span data-stu-id="4975e-152">Pattern</span></span>

-  <span data-ttu-id="4975e-153">Dígitos</span><span class="sxs-lookup"><span data-stu-id="4975e-153">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="4975e-154">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="4975e-154">Checksum</span></span>

<span data-ttu-id="4975e-155">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="4975e-155">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="4975e-156">Definição</span><span class="sxs-lookup"><span data-stu-id="4975e-156">Definition</span></span>

<span data-ttu-id="4975e-157">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4975e-157">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4975e-158">A expressão regular `Regex_czech_republic_eu_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-158">The regular expression  `Regex_czech_republic_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-159">A expressão regular `Regex_czech_republic_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-159">The regular expression  `Regex_czech_republic_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-160">Uma palavra-chave da `Keywords_czech_republic_eu_mobile_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="4975e-160">A keyword from  `Keywords_czech_republic_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_mobile_number"/>
          <Match idRef="Keywords_czech_republic_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_czech_republic_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="denmark"></a><span data-ttu-id="4975e-161">Dinamarca</span><span class="sxs-lookup"><span data-stu-id="4975e-161">Denmark</span></span>

### <a name="pattern"></a><span data-ttu-id="4975e-162">Padrão</span><span class="sxs-lookup"><span data-stu-id="4975e-162">Pattern</span></span>

-  <span data-ttu-id="4975e-163">Dígitos</span><span class="sxs-lookup"><span data-stu-id="4975e-163">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="4975e-164">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="4975e-164">Checksum</span></span>

<span data-ttu-id="4975e-165">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="4975e-165">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="4975e-166">Definição</span><span class="sxs-lookup"><span data-stu-id="4975e-166">Definition</span></span>

<span data-ttu-id="4975e-167">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4975e-167">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4975e-168">A expressão regular `Regex_denmark_eu_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-168">The regular expression  `Regex_denmark_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-169">A expressão regular `Regex_denmark_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-169">The regular expression  `Regex_denmark_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-170">Uma palavra-chave da `Keywords_denmark_eu_mobile_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="4975e-170">A keyword from  `Keywords_denmark_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_mobile_number"/>
          <Match idRef="Keywords_denmark_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_denmark_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="estonia"></a><span data-ttu-id="4975e-171">Estônia</span><span class="sxs-lookup"><span data-stu-id="4975e-171">Estonia</span></span>

### <a name="pattern"></a><span data-ttu-id="4975e-172">Padrão</span><span class="sxs-lookup"><span data-stu-id="4975e-172">Pattern</span></span>

-  <span data-ttu-id="4975e-173">Dígitos</span><span class="sxs-lookup"><span data-stu-id="4975e-173">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="4975e-174">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="4975e-174">Checksum</span></span>

<span data-ttu-id="4975e-175">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="4975e-175">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="4975e-176">Definição</span><span class="sxs-lookup"><span data-stu-id="4975e-176">Definition</span></span>

<span data-ttu-id="4975e-177">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4975e-177">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4975e-178">A expressão regular `Regex_estonia_eu_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-178">The regular expression  `Regex_estonia_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-179">A expressão regular `Regex_estonia_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-179">The regular expression  `Regex_estonia_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-180">Uma palavra-chave da `Keywords_estonia_eu_mobile_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="4975e-180">A keyword from  `Keywords_estonia_eu_mobile_number` is found.</span></span> 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_mobile_number"/>
          <Match idRef="Keywords_estonia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_estonia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="finland"></a><span data-ttu-id="4975e-181">Finlândia</span><span class="sxs-lookup"><span data-stu-id="4975e-181">Finland</span></span>

### <a name="pattern"></a><span data-ttu-id="4975e-182">Padrão</span><span class="sxs-lookup"><span data-stu-id="4975e-182">Pattern</span></span>

-  <span data-ttu-id="4975e-183">Dígitos</span><span class="sxs-lookup"><span data-stu-id="4975e-183">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="4975e-184">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="4975e-184">Checksum</span></span>

<span data-ttu-id="4975e-185">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="4975e-185">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="4975e-186">Definição</span><span class="sxs-lookup"><span data-stu-id="4975e-186">Definition</span></span>

<span data-ttu-id="4975e-187">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4975e-187">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4975e-188">A expressão regular `Regex_finland_eu_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-188">The regular expression  `Regex_finland_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-189">A expressão regular `Regex_finland_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-189">The regular expression  `Regex_finland_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-190">Uma palavra-chave da `Keywords_finland_eu_mobile_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="4975e-190">A keyword from  `Keywords_finland_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_mobile_number"/>
          <Match idRef="Keywords_finland_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_finland_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="france"></a><span data-ttu-id="4975e-191">França</span><span class="sxs-lookup"><span data-stu-id="4975e-191">France</span></span>

### <a name="pattern"></a><span data-ttu-id="4975e-192">Padrão</span><span class="sxs-lookup"><span data-stu-id="4975e-192">Pattern</span></span>

-  <span data-ttu-id="4975e-193">Dígitos</span><span class="sxs-lookup"><span data-stu-id="4975e-193">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="4975e-194">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="4975e-194">Checksum</span></span>

<span data-ttu-id="4975e-195">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="4975e-195">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="4975e-196">Definição</span><span class="sxs-lookup"><span data-stu-id="4975e-196">Definition</span></span>

<span data-ttu-id="4975e-197">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4975e-197">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4975e-198">A expressão regular `Regex_france_eu_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-198">The regular expression  `Regex_france_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-199">A expressão regular `Regex_france_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-199">The regular expression  `Regex_france_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-200">Uma palavra-chave da `Keywords_france_eu_mobile_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="4975e-200">A keyword from  `Keywords_france_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_france_eu_mobile_number"/>
          <Match idRef="Keywords_france_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_france_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="germany"></a><span data-ttu-id="4975e-201">Alemanha</span><span class="sxs-lookup"><span data-stu-id="4975e-201">Germany</span></span>

### <a name="pattern"></a><span data-ttu-id="4975e-202">Padrão</span><span class="sxs-lookup"><span data-stu-id="4975e-202">Pattern</span></span>

-  <span data-ttu-id="4975e-203">Dígitos</span><span class="sxs-lookup"><span data-stu-id="4975e-203">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="4975e-204">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="4975e-204">Checksum</span></span>

<span data-ttu-id="4975e-205">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="4975e-205">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="4975e-206">Definição</span><span class="sxs-lookup"><span data-stu-id="4975e-206">Definition</span></span>

<span data-ttu-id="4975e-207">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4975e-207">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4975e-208">A expressão regular `Regex_germany_eu_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-208">The regular expression  `Regex_germany_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-209">A expressão regular `Regex_germany_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-209">The regular expression  `Regex_germany_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-210">Uma palavra-chave da `Keywords_germany_eu_mobile_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="4975e-210">A keyword from  `Keywords_germany_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_germany_eu_mobile_number"/>
          <Match idRef="Keywords_germany_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_germany_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="greece"></a><span data-ttu-id="4975e-211">Grécia</span><span class="sxs-lookup"><span data-stu-id="4975e-211">Greece</span></span>

### <a name="pattern"></a><span data-ttu-id="4975e-212">Padrão</span><span class="sxs-lookup"><span data-stu-id="4975e-212">Pattern</span></span>

-  <span data-ttu-id="4975e-213">Dígitos</span><span class="sxs-lookup"><span data-stu-id="4975e-213">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="4975e-214">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="4975e-214">Checksum</span></span>

<span data-ttu-id="4975e-215">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="4975e-215">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="4975e-216">Definição</span><span class="sxs-lookup"><span data-stu-id="4975e-216">Definition</span></span>

<span data-ttu-id="4975e-217">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4975e-217">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4975e-218">A expressão regular `Regex_greece_eu_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-218">The regular expression  `Regex_greece_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-219">A expressão regular `Regex_greece_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-219">The regular expression  `Regex_greece_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-220">Uma palavra-chave da `Keywords_greece_eu_mobile_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="4975e-220">A keyword from  `Keywords_greece_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_mobile_number"/>
          <Match idRef="Keywords_greece_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_greece_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="hungary"></a><span data-ttu-id="4975e-221">Hungria</span><span class="sxs-lookup"><span data-stu-id="4975e-221">Hungary</span></span>

### <a name="pattern"></a><span data-ttu-id="4975e-222">Padrão</span><span class="sxs-lookup"><span data-stu-id="4975e-222">Pattern</span></span>

-  <span data-ttu-id="4975e-223">Dígitos</span><span class="sxs-lookup"><span data-stu-id="4975e-223">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="4975e-224">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="4975e-224">Checksum</span></span>

<span data-ttu-id="4975e-225">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="4975e-225">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="4975e-226">Definição</span><span class="sxs-lookup"><span data-stu-id="4975e-226">Definition</span></span>

<span data-ttu-id="4975e-227">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4975e-227">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4975e-228">A expressão regular `Regex_hungary_eu_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-228">The regular expression  `Regex_hungary_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-229">A expressão regular `Regex_hungary_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-229">The regular expression  `Regex_hungary_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-230">Uma palavra-chave da `Keywords_hungary_eu_mobile_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="4975e-230">A keyword from  `Keywords_hungary_eu_mobile_number` is found.</span></span> 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_mobile_number"/>
          <Match idRef="Keywords_hungary_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_hungary_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="ireland"></a><span data-ttu-id="4975e-231">Irlanda</span><span class="sxs-lookup"><span data-stu-id="4975e-231">Ireland</span></span>

### <a name="pattern"></a><span data-ttu-id="4975e-232">Padrão</span><span class="sxs-lookup"><span data-stu-id="4975e-232">Pattern</span></span>

-  <span data-ttu-id="4975e-233">Dígitos</span><span class="sxs-lookup"><span data-stu-id="4975e-233">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="4975e-234">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="4975e-234">Checksum</span></span>

<span data-ttu-id="4975e-235">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="4975e-235">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="4975e-236">Definição</span><span class="sxs-lookup"><span data-stu-id="4975e-236">Definition</span></span>

<span data-ttu-id="4975e-237">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4975e-237">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4975e-238">A expressão regular `Regex_ireland_eu_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-238">The regular expression  `Regex_ireland_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-239">A expressão regular `Regex_ireland_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-239">The regular expression  `Regex_ireland_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-240">Uma palavra-chave da `Keywords_ireland_eu_mobile_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="4975e-240">A keyword from  `Keywords_ireland_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_mobile_number"/>
          <Match idRef="Keywords_ireland_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_ireland_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="italy"></a><span data-ttu-id="4975e-241">Itália</span><span class="sxs-lookup"><span data-stu-id="4975e-241">Italy</span></span>

### <a name="pattern"></a><span data-ttu-id="4975e-242">Padrão</span><span class="sxs-lookup"><span data-stu-id="4975e-242">Pattern</span></span>

-  <span data-ttu-id="4975e-243">Dígitos</span><span class="sxs-lookup"><span data-stu-id="4975e-243">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="4975e-244">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="4975e-244">Checksum</span></span>

<span data-ttu-id="4975e-245">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="4975e-245">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="4975e-246">Definição</span><span class="sxs-lookup"><span data-stu-id="4975e-246">Definition</span></span>

<span data-ttu-id="4975e-247">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4975e-247">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4975e-248">A expressão regular `Regex_italy_eu_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-248">The regular expression  `Regex_italy_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-249">A expressão regular `Regex_italy_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-249">The regular expression  `Regex_italy_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-250">Uma palavra-chave da `Keywords_italy_eu_mobile_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="4975e-250">A keyword from  `Keywords_italy_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_mobile_number"/>
          <Match idRef="Keywords_italy_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_italy_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="latvia"></a><span data-ttu-id="4975e-251">Letônia</span><span class="sxs-lookup"><span data-stu-id="4975e-251">Latvia</span></span>

### <a name="pattern"></a><span data-ttu-id="4975e-252">Padrão</span><span class="sxs-lookup"><span data-stu-id="4975e-252">Pattern</span></span>

-  <span data-ttu-id="4975e-253">Dígitos</span><span class="sxs-lookup"><span data-stu-id="4975e-253">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="4975e-254">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="4975e-254">Checksum</span></span>

<span data-ttu-id="4975e-255">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="4975e-255">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="4975e-256">Definição</span><span class="sxs-lookup"><span data-stu-id="4975e-256">Definition</span></span>

<span data-ttu-id="4975e-257">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4975e-257">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4975e-258">A expressão regular `Regex_latvia_eu_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-258">The regular expression  `Regex_latvia_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-259">A expressão regular `Regex_latvia_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-259">The regular expression  `Regex_latvia_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-260">Uma palavra-chave da `Keywords_latvia_eu_mobile_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="4975e-260">A keyword from  `Keywords_latvia_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_mobile_number"/>
          <Match idRef="Keywords_latvia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_latvia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="lithuania"></a><span data-ttu-id="4975e-261">Lituânia</span><span class="sxs-lookup"><span data-stu-id="4975e-261">Lithuania</span></span>

### <a name="pattern"></a><span data-ttu-id="4975e-262">Padrão</span><span class="sxs-lookup"><span data-stu-id="4975e-262">Pattern</span></span>

-  <span data-ttu-id="4975e-263">Dígitos</span><span class="sxs-lookup"><span data-stu-id="4975e-263">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="4975e-264">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="4975e-264">Checksum</span></span>

<span data-ttu-id="4975e-265">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="4975e-265">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="4975e-266">Definição</span><span class="sxs-lookup"><span data-stu-id="4975e-266">Definition</span></span>

<span data-ttu-id="4975e-267">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4975e-267">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4975e-268">A expressão regular `Regex_lithuania_eu_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-268">The regular expression  `Regex_lithuania_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-269">A expressão regular `Regex_lithuania_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-269">The regular expression  `Regex_lithuania_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-270">Uma palavra-chave da `Keywords_lithuania_eu_mobile_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="4975e-270">A keyword from  `Keywords_lithuania_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_mobile_number"/>
          <Match idRef="Keywords_lithuania_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_lithuania_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="luxemburg"></a><span data-ttu-id="4975e-271">Luxemburgo</span><span class="sxs-lookup"><span data-stu-id="4975e-271">Luxemburg</span></span>

### <a name="pattern"></a><span data-ttu-id="4975e-272">Padrão</span><span class="sxs-lookup"><span data-stu-id="4975e-272">Pattern</span></span>

-  <span data-ttu-id="4975e-273">Dígitos</span><span class="sxs-lookup"><span data-stu-id="4975e-273">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="4975e-274">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="4975e-274">Checksum</span></span>

<span data-ttu-id="4975e-275">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="4975e-275">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="4975e-276">Definição</span><span class="sxs-lookup"><span data-stu-id="4975e-276">Definition</span></span>

<span data-ttu-id="4975e-277">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4975e-277">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4975e-278">A expressão regular `Regex_luxumburg_eu_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-278">The regular expression  `Regex_luxumburg_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-279">A expressão regular `Regex_luxumburg_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-279">The regular expression  `Regex_luxumburg_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-280">Uma palavra-chave da `Keywords_luxumburg_eu_mobile_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="4975e-280">A keyword from  `Keywords_luxumburg_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxumburg_eu_mobile_number"/>
          <Match idRef="Keywords_luxumburg_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_luxumburg_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="malta"></a><span data-ttu-id="4975e-281">Malta</span><span class="sxs-lookup"><span data-stu-id="4975e-281">Malta</span></span>

### <a name="pattern"></a><span data-ttu-id="4975e-282">Padrão</span><span class="sxs-lookup"><span data-stu-id="4975e-282">Pattern</span></span>

-  <span data-ttu-id="4975e-283">Dígitos</span><span class="sxs-lookup"><span data-stu-id="4975e-283">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="4975e-284">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="4975e-284">Checksum</span></span>

<span data-ttu-id="4975e-285">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="4975e-285">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="4975e-286">Definição</span><span class="sxs-lookup"><span data-stu-id="4975e-286">Definition</span></span>

<span data-ttu-id="4975e-287">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4975e-287">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4975e-288">A expressão regular `Regex_malta_eu_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-288">The regular expression  `Regex_malta_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-289">A expressão regular `Regex_malta_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-289">The regular expression  `Regex_malta_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-290">Uma palavra-chave da `Keywords_malta_eu_mobile_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="4975e-290">A keyword from  `Keywords_malta_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_mobile_number"/>
          <Match idRef="Keywords_malta_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_malta_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="netherlands"></a><span data-ttu-id="4975e-291">Países Baixos</span><span class="sxs-lookup"><span data-stu-id="4975e-291">Netherlands</span></span>

### <a name="pattern"></a><span data-ttu-id="4975e-292">Padrão</span><span class="sxs-lookup"><span data-stu-id="4975e-292">Pattern</span></span>

-  <span data-ttu-id="4975e-293">Dígitos</span><span class="sxs-lookup"><span data-stu-id="4975e-293">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="4975e-294">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="4975e-294">Checksum</span></span>

<span data-ttu-id="4975e-295">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="4975e-295">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="4975e-296">Definição</span><span class="sxs-lookup"><span data-stu-id="4975e-296">Definition</span></span>

<span data-ttu-id="4975e-297">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4975e-297">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4975e-298">A expressão regular `Regex_netherlands_eu_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-298">The regular expression  `Regex_netherlands_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-299">A expressão regular `Regex_netherlands_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-299">The regular expression  `Regex_netherlands_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-300">Uma palavra-chave da `Keywords_netherlands_eu_mobile_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="4975e-300">A keyword from  `Keywords_netherlands_eu_mobile_number` is found.</span></span> 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_mobile_number"/>
          <Match idRef="Keywords_netherlands_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_netherlands_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="poland"></a><span data-ttu-id="4975e-301">Polônia</span><span class="sxs-lookup"><span data-stu-id="4975e-301">Poland</span></span>

### <a name="pattern"></a><span data-ttu-id="4975e-302">Padrão</span><span class="sxs-lookup"><span data-stu-id="4975e-302">Pattern</span></span>

-  <span data-ttu-id="4975e-303">Dígitos</span><span class="sxs-lookup"><span data-stu-id="4975e-303">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="4975e-304">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="4975e-304">Checksum</span></span>

<span data-ttu-id="4975e-305">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="4975e-305">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="4975e-306">Definição</span><span class="sxs-lookup"><span data-stu-id="4975e-306">Definition</span></span>

<span data-ttu-id="4975e-307">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4975e-307">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4975e-308">A expressão regular `Regex_poland_eu_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-308">The regular expression  `Regex_poland_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-309">A expressão regular `Regex_poland_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-309">The regular expression  `Regex_poland_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-310">Uma palavra-chave da `Keywords_poland_eu_mobile_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="4975e-310">A keyword from  `Keywords_poland_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_mobile_number"/>
          <Match idRef="Keywords_poland_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_poland_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="portugal"></a><span data-ttu-id="4975e-311">Portugal</span><span class="sxs-lookup"><span data-stu-id="4975e-311">Portugal</span></span>

### <a name="pattern"></a><span data-ttu-id="4975e-312">Padrão</span><span class="sxs-lookup"><span data-stu-id="4975e-312">Pattern</span></span>

-  <span data-ttu-id="4975e-313">Dígitos</span><span class="sxs-lookup"><span data-stu-id="4975e-313">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="4975e-314">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="4975e-314">Checksum</span></span>

<span data-ttu-id="4975e-315">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="4975e-315">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="4975e-316">Definição</span><span class="sxs-lookup"><span data-stu-id="4975e-316">Definition</span></span>

<span data-ttu-id="4975e-317">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4975e-317">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4975e-318">A expressão regular `Regex_portugal_eu_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-318">The regular expression  `Regex_portugal_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-319">A expressão regular `Regex_portugal_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-319">The regular expression  `Regex_portugal_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-320">Uma palavra-chave da `Keywords_portugal_eu_mobile_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="4975e-320">A keyword from  `Keywords_portugal_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_mobile_number"/>
          <Match idRef="Keywords_portugal_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_portugal_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="romania"></a><span data-ttu-id="4975e-321">Romênia</span><span class="sxs-lookup"><span data-stu-id="4975e-321">Romania</span></span>

### <a name="pattern"></a><span data-ttu-id="4975e-322">Padrão</span><span class="sxs-lookup"><span data-stu-id="4975e-322">Pattern</span></span>

-  <span data-ttu-id="4975e-323">Dígitos</span><span class="sxs-lookup"><span data-stu-id="4975e-323">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="4975e-324">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="4975e-324">Checksum</span></span>

<span data-ttu-id="4975e-325">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="4975e-325">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="4975e-326">Definição</span><span class="sxs-lookup"><span data-stu-id="4975e-326">Definition</span></span>

<span data-ttu-id="4975e-327">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4975e-327">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4975e-328">A expressão regular `Regex_romania_eu_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-328">The regular expression  `Regex_romania_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-329">A expressão regular `Regex_romania_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-329">The regular expression  `Regex_romania_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-330">Uma palavra-chave da `Keywords_romania_eu_mobile_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="4975e-330">A keyword from  `Keywords_romania_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_mobile_number"/>
          <Match idRef="Keywords_romania_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_romania_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="slovakia"></a><span data-ttu-id="4975e-331">Eslováquia</span><span class="sxs-lookup"><span data-stu-id="4975e-331">Slovakia</span></span>

### <a name="pattern"></a><span data-ttu-id="4975e-332">Padrão</span><span class="sxs-lookup"><span data-stu-id="4975e-332">Pattern</span></span>

-  <span data-ttu-id="4975e-333">Dígitos</span><span class="sxs-lookup"><span data-stu-id="4975e-333">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="4975e-334">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="4975e-334">Checksum</span></span>

<span data-ttu-id="4975e-335">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="4975e-335">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="4975e-336">Definição</span><span class="sxs-lookup"><span data-stu-id="4975e-336">Definition</span></span>

<span data-ttu-id="4975e-337">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4975e-337">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4975e-338">A expressão regular `Regex_slovakia_eu_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-338">The regular expression  `Regex_slovakia_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-339">A expressão regular `Regex_slovakia_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-339">The regular expression  `Regex_slovakia_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-340">Uma palavra-chave da `Keywords_slovakia_eu_mobile_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="4975e-340">A keyword from  `Keywords_slovakia_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_mobile_number"/>
          <Match idRef="Keywords_slovakia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_slovakia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="slovenia"></a><span data-ttu-id="4975e-341">Eslovênia</span><span class="sxs-lookup"><span data-stu-id="4975e-341">Slovenia</span></span>

### <a name="pattern"></a><span data-ttu-id="4975e-342">Padrão</span><span class="sxs-lookup"><span data-stu-id="4975e-342">Pattern</span></span>

-  <span data-ttu-id="4975e-343">Dígitos</span><span class="sxs-lookup"><span data-stu-id="4975e-343">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="4975e-344">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="4975e-344">Checksum</span></span>

<span data-ttu-id="4975e-345">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="4975e-345">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="4975e-346">Definição</span><span class="sxs-lookup"><span data-stu-id="4975e-346">Definition</span></span>

<span data-ttu-id="4975e-347">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4975e-347">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4975e-348">A expressão regular `Regex_slovenia_eu_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-348">The regular expression  `Regex_slovenia_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-349">A expressão regular `Regex_slovenia_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-349">The regular expression  `Regex_slovenia_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-350">Uma palavra-chave da `Keywords_slovenia_eu_mobile_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="4975e-350">A keyword from  `Keywords_slovenia_eu_mobile_number` is found.</span></span> 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_mobile_number"/>
          <Match idRef="Keywords_slovenia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_slovenia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="spain"></a><span data-ttu-id="4975e-351">Espanha</span><span class="sxs-lookup"><span data-stu-id="4975e-351">Spain</span></span>

### <a name="pattern"></a><span data-ttu-id="4975e-352">Padrão</span><span class="sxs-lookup"><span data-stu-id="4975e-352">Pattern</span></span>

-  <span data-ttu-id="4975e-353">Dígitos</span><span class="sxs-lookup"><span data-stu-id="4975e-353">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="4975e-354">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="4975e-354">Checksum</span></span>

<span data-ttu-id="4975e-355">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="4975e-355">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="4975e-356">Definição</span><span class="sxs-lookup"><span data-stu-id="4975e-356">Definition</span></span>

<span data-ttu-id="4975e-357">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4975e-357">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4975e-358">A expressão regular `Regex_spain_eu_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-358">The regular expression  `Regex_spain_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-359">A expressão regular `Regex_spain_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-359">The regular expression  `Regex_spain_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-360">Uma palavra-chave da `Keywords_spain_eu_mobile_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="4975e-360">A keyword from  `Keywords_spain_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_mobile_number"/>
          <Match idRef="Keywords_spain_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_spain_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="sweden"></a><span data-ttu-id="4975e-361">Suécia</span><span class="sxs-lookup"><span data-stu-id="4975e-361">Sweden</span></span>

### <a name="pattern"></a><span data-ttu-id="4975e-362">Padrão</span><span class="sxs-lookup"><span data-stu-id="4975e-362">Pattern</span></span>

-  <span data-ttu-id="4975e-363">Dígitos</span><span class="sxs-lookup"><span data-stu-id="4975e-363">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="4975e-364">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="4975e-364">Checksum</span></span>

<span data-ttu-id="4975e-365">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="4975e-365">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="4975e-366">Definição</span><span class="sxs-lookup"><span data-stu-id="4975e-366">Definition</span></span>

<span data-ttu-id="4975e-367">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4975e-367">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4975e-368">A expressão regular `Regex_sweden_eu_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-368">The regular expression  `Regex_sweden_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-369">A expressão regular `Regex_sweden_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-369">The regular expression  `Regex_sweden_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-370">Uma palavra-chave da `Keywords_sweden_eu_mobile_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="4975e-370">A keyword from  `Keywords_sweden_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_mobile_number"/>
          <Match idRef="Keywords_sweden_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_sweden_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="uk"></a><span data-ttu-id="4975e-371">REINO UNIDO</span><span class="sxs-lookup"><span data-stu-id="4975e-371">UK</span></span>

### <a name="pattern"></a><span data-ttu-id="4975e-372">Padrão</span><span class="sxs-lookup"><span data-stu-id="4975e-372">Pattern</span></span>

-  <span data-ttu-id="4975e-373">Dígitos</span><span class="sxs-lookup"><span data-stu-id="4975e-373">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="4975e-374">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="4975e-374">Checksum</span></span>

<span data-ttu-id="4975e-375">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="4975e-375">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="4975e-376">Definição</span><span class="sxs-lookup"><span data-stu-id="4975e-376">Definition</span></span>

<span data-ttu-id="4975e-377">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4975e-377">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4975e-378">A expressão regular `Regex_uk_eu_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-378">The regular expression  `Regex_uk_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-379">A expressão regular `Regex_uk_eu_formatted_mobile_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4975e-379">The regular expression  `Regex_uk_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4975e-380">Uma palavra-chave da `Keywords_uk_eu_mobile_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="4975e-380">A keyword from  `Keywords_uk_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_uk_eu_mobile_number"/>
          <Match idRef="Keywords_uk_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_uk_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="see-also"></a><span data-ttu-id="4975e-381">Confira também</span><span class="sxs-lookup"><span data-stu-id="4975e-381">See also</span></span>

[<span data-ttu-id="4975e-382">O que os tipos de informações confidenciais procuram</span><span class="sxs-lookup"><span data-stu-id="4975e-382">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)


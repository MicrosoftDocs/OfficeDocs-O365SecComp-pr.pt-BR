---
title: Coordenadas do GPS da UE
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/14/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: fdf2aebc-d5a4-4138-b10f-4a81dd70415a
description: Prevenção de perda de dados (DLP) no Office 365 Security &amp; Centro de conformidade inclui muitos tipos de informações confidenciais que estão prontos para uso em suas políticas de DLP. Este tópico descreve o tipo de informações confidenciais da UE coordena de GPS.
ms.openlocfilehash: 89fb8420e479b9f793fc2be9aa3a9a9fd5741691
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523973"
---
# <a name="eu-gps-coordinates"></a><span data-ttu-id="64916-104">Coordenadas do GPS da UE</span><span class="sxs-lookup"><span data-stu-id="64916-104">EU GPS Coordinates</span></span>

<span data-ttu-id="64916-p102">Prevenção de perda de dados (DLP) no Office 365 Security &amp; Centro de conformidade inclui muitos tipos de informações confidenciais que estão prontos para uso em suas políticas de DLP. Este tópico descreve o tipo de informações confidenciais da UE coordena de GPS.</span><span class="sxs-lookup"><span data-stu-id="64916-p102">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies. This topic describes the EU GPS Coordinates sensitive information type.</span></span>
  
## <a name="austria"></a><span data-ttu-id="64916-107">Áustria</span><span class="sxs-lookup"><span data-stu-id="64916-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="64916-108">Formato</span><span class="sxs-lookup"><span data-stu-id="64916-108">Format</span></span>

<span data-ttu-id="64916-109">Coordena para cidades na Áustria estão no intervalo: Latitude de 46.526 48.816 e longitude do 9.6 para 16.945.</span><span class="sxs-lookup"><span data-stu-id="64916-109">Coordinates for cities in Austria are in range: Latitude from 46.526 to 48.816 and longitude from 9.6 to 16.945.</span></span>
  
### <a name="pattern"></a><span data-ttu-id="64916-110">Padrão</span><span class="sxs-lookup"><span data-stu-id="64916-110">Pattern</span></span>

<span data-ttu-id="64916-111">Para cada coordenada, a combinação de até 6 dígitos e um separador decimal.</span><span class="sxs-lookup"><span data-stu-id="64916-111">For each coordinate, combination of up to 6 digits and a decimal point.</span></span>
  
- <span data-ttu-id="64916-112">Até 6 dígitos</span><span class="sxs-lookup"><span data-stu-id="64916-112">Up to 6 digits</span></span>
    
- <span data-ttu-id="64916-113">Um separador decimal após a primeiro ou segundo dígitos.</span><span class="sxs-lookup"><span data-stu-id="64916-113">A decimal point after first or second digit.</span></span>
    
### <a name="checksum"></a><span data-ttu-id="64916-114">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="64916-114">Checksum</span></span>

<span data-ttu-id="64916-115">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="64916-115">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64916-116">Definição</span><span class="sxs-lookup"><span data-stu-id="64916-116">Definition</span></span>

<span data-ttu-id="64916-117">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="64916-117">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64916-118">A expressão regular `Regex_austria_eu_gps_data_1` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="64916-118">The regular expression  `Regex_austria_eu_gps_data_1` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64916-119">Uma palavra-chave da `Keywords_austria_eu_gps_data` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="64916-119">A keyword from  `Keywords_austria_eu_gps_data` is found.</span></span> 
    
<span data-ttu-id="64916-120">Uma política de DLP tem 65% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="64916-120">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64916-121">A expressão regular `Regex_austria_eu_gps_data_1` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="64916-121">The regular expression  `Regex_austria_eu_gps_data_1` finds content that matches the pattern.</span></span> 
    
<span data-ttu-id="64916-122">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="64916-122">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64916-123">A expressão regular `Regex_austria_eu_gps_data_2` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="64916-123">The regular expression  `Regex_austria_eu_gps_data_2` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64916-124">Uma palavra-chave da `Keywords_austria_eu_gps_data` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="64916-124">A keyword from  `Keywords_austria_eu_gps_data` is found.</span></span> 
    
<span data-ttu-id="64916-125">Uma política de DLP tem 65% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="64916-125">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64916-126">A expressão regular `Regex_austria_eu_gps_data_2` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="64916-126">The regular expression  `Regex_austria_eu_gps_data_2` finds content that matches the pattern.</span></span> 
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_gps_data_1" />
          <Match idRef="Keywords_austria_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_austria_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_gps_data_2" />
          <Match idRef="Keywords_austria_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_austria_eu_gps_data_2" />
        </Pattern>

```

### <a name="keywords"></a><span data-ttu-id="64916-127">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="64916-127">Keywords</span></span>

#### <a name="keywordsaustriaeugpsdata"></a><span data-ttu-id="64916-128">Keywords_austria_eu_gps_data</span><span class="sxs-lookup"><span data-stu-id="64916-128">Keywords_austria_eu_gps_data</span></span>

<span data-ttu-id="64916-129">GPS tracker</span><span class="sxs-lookup"><span data-stu-id="64916-129">gps tracker</span></span>
  
<span data-ttu-id="64916-130">coordenadas de GPS</span><span class="sxs-lookup"><span data-stu-id="64916-130">gps coordinates</span></span>
  
<span data-ttu-id="64916-131">local</span><span class="sxs-lookup"><span data-stu-id="64916-131">location</span></span>
  
<span data-ttu-id="64916-132">mapa</span><span class="sxs-lookup"><span data-stu-id="64916-132">map</span></span>
  
<span data-ttu-id="64916-133">Latitude</span><span class="sxs-lookup"><span data-stu-id="64916-133">latitude</span></span>
  
<span data-ttu-id="64916-134">longitude</span><span class="sxs-lookup"><span data-stu-id="64916-134">longitude</span></span>
  
<span data-ttu-id="64916-135">Rastreador de GPS</span><span class="sxs-lookup"><span data-stu-id="64916-135">GPS-Tracker</span></span>
  
<span data-ttu-id="64916-136">GPS-Koordinaten</span><span class="sxs-lookup"><span data-stu-id="64916-136">GPS-Koordinaten</span></span>
  
<span data-ttu-id="64916-137">Standort Karte</span><span class="sxs-lookup"><span data-stu-id="64916-137">Standort Karte</span></span>
  
<span data-ttu-id="64916-138">Breitengrad</span><span class="sxs-lookup"><span data-stu-id="64916-138">Breitengrad</span></span>
  
<span data-ttu-id="64916-139">Längengrad</span><span class="sxs-lookup"><span data-stu-id="64916-139">Längengrad</span></span>
  
## <a name="belgium"></a><span data-ttu-id="64916-140">Bélgica</span><span class="sxs-lookup"><span data-stu-id="64916-140">Belgium</span></span>

### <a name="pattern"></a><span data-ttu-id="64916-141">Padrão</span><span class="sxs-lookup"><span data-stu-id="64916-141">Pattern</span></span>

-  <span data-ttu-id="64916-142">dígitos</span><span class="sxs-lookup"><span data-stu-id="64916-142">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64916-143">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="64916-143">Checksum</span></span>

<span data-ttu-id="64916-144">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="64916-144">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64916-145">Definição</span><span class="sxs-lookup"><span data-stu-id="64916-145">Definition</span></span>

<span data-ttu-id="64916-146">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="64916-146">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64916-147">A expressão regular encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="64916-147">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="64916-148">Uma palavra-chave da é encontrada.</span><span class="sxs-lookup"><span data-stu-id="64916-148">A keyword from is found.</span></span>
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75>">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_gps_data_1" />
          <Match idRef="Keywords_belgium_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_belgium_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_gps_data_2" />
          <Match idRef="Keywords_belgium_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_belgium_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="bulgaria"></a><span data-ttu-id="64916-149">Bulgária</span><span class="sxs-lookup"><span data-stu-id="64916-149">Bulgaria</span></span>

### <a name="pattern"></a><span data-ttu-id="64916-150">Padrão</span><span class="sxs-lookup"><span data-stu-id="64916-150">Pattern</span></span>

-  <span data-ttu-id="64916-151">dígitos</span><span class="sxs-lookup"><span data-stu-id="64916-151">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64916-152">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="64916-152">Checksum</span></span>

<span data-ttu-id="64916-153">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="64916-153">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64916-154">Definição</span><span class="sxs-lookup"><span data-stu-id="64916-154">Definition</span></span>

<span data-ttu-id="64916-155">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="64916-155">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64916-156">A expressão regular encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="64916-156">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="64916-157">Uma palavra-chave da é encontrada.</span><span class="sxs-lookup"><span data-stu-id="64916-157">A keyword from is found.</span></span>
    
```
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75>
</Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_belgium_eu_gps_data_2" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_gps_data_1" />
          <Match idRef="Keywords_bulgaria_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_bulgaria_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_gps_data_2" />
          <Match idRef="Keywords_bulgaria_eu_gps_data" />
        </Pattern>
</Entity>
```

## <a name="croatia"></a><span data-ttu-id="64916-158">Croácia</span><span class="sxs-lookup"><span data-stu-id="64916-158">Croatia</span></span>

### <a name="pattern"></a><span data-ttu-id="64916-159">Padrão</span><span class="sxs-lookup"><span data-stu-id="64916-159">Pattern</span></span>

-  <span data-ttu-id="64916-160">dígitos</span><span class="sxs-lookup"><span data-stu-id="64916-160">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64916-161">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="64916-161">Checksum</span></span>

<span data-ttu-id="64916-162">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="64916-162">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64916-163">Definição</span><span class="sxs-lookup"><span data-stu-id="64916-163">Definition</span></span>

<span data-ttu-id="64916-164">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="64916-164">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64916-165">A expressão regular encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="64916-165">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="64916-166">Uma palavra-chave da é encontrada.</span><span class="sxs-lookup"><span data-stu-id="64916-166">A keyword from is found.</span></span>
    
```
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_gps_data_1" />
          <Match idRef="Keywords_croatia_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_croatia_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_gps_data_2" />
          <Match idRef="Keywords_croatia_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_croatia_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="cyprus"></a><span data-ttu-id="64916-167">Chipre</span><span class="sxs-lookup"><span data-stu-id="64916-167">Cyprus</span></span>

### <a name="pattern"></a><span data-ttu-id="64916-168">Padrão</span><span class="sxs-lookup"><span data-stu-id="64916-168">Pattern</span></span>

-  <span data-ttu-id="64916-169">dígitos</span><span class="sxs-lookup"><span data-stu-id="64916-169">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64916-170">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="64916-170">Checksum</span></span>

<span data-ttu-id="64916-171">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="64916-171">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64916-172">Definição</span><span class="sxs-lookup"><span data-stu-id="64916-172">Definition</span></span>

<span data-ttu-id="64916-173">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="64916-173">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64916-174">A expressão regular encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="64916-174">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="64916-175">Uma palavra-chave da é encontrada.</span><span class="sxs-lookup"><span data-stu-id="64916-175">A keyword from is found.</span></span>
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_gps_data_1" />
          <Match idRef="Keywords_cyprus_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_cyprus_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_gps_data_2" />
          <Match idRef="Keywords_cyprus_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_cyprus_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="czech-republic"></a><span data-ttu-id="64916-176">República Tcheca</span><span class="sxs-lookup"><span data-stu-id="64916-176">Czech Republic</span></span>

### <a name="pattern"></a><span data-ttu-id="64916-177">Padrão</span><span class="sxs-lookup"><span data-stu-id="64916-177">Pattern</span></span>

-  <span data-ttu-id="64916-178">dígitos</span><span class="sxs-lookup"><span data-stu-id="64916-178">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64916-179">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="64916-179">Checksum</span></span>

<span data-ttu-id="64916-180">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="64916-180">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64916-181">Definição</span><span class="sxs-lookup"><span data-stu-id="64916-181">Definition</span></span>

<span data-ttu-id="64916-182">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="64916-182">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
<span data-ttu-id="64916-183">Uma política de DLP é % confiante de que detectou esse tipo de informações confidenciais if, dentro de uma proximidade de caracteres:</span><span class="sxs-lookup"><span data-stu-id="64916-183">A DLP policy is % confident that it's detected this type of sensitive information if, within a proximity of characters:</span></span>
  
- <span data-ttu-id="64916-184">A expressão regular encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="64916-184">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="64916-185">Uma palavra-chave da é encontrada.</span><span class="sxs-lookup"><span data-stu-id="64916-185">A keyword from is found.</span></span>
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_gps_data_1" />
          <Match idRef="Keywords_czech_republic_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_czech_republic_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_gps_data_2" />
          <Match idRef="Keywords_czech_republic_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_czech_republic_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="denmark"></a><span data-ttu-id="64916-186">Dinamarca</span><span class="sxs-lookup"><span data-stu-id="64916-186">Denmark</span></span>

### <a name="pattern"></a><span data-ttu-id="64916-187">Padrão</span><span class="sxs-lookup"><span data-stu-id="64916-187">Pattern</span></span>

-  <span data-ttu-id="64916-188">dígitos</span><span class="sxs-lookup"><span data-stu-id="64916-188">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64916-189">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="64916-189">Checksum</span></span>

<span data-ttu-id="64916-190">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="64916-190">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64916-191">Definição</span><span class="sxs-lookup"><span data-stu-id="64916-191">Definition</span></span>

<span data-ttu-id="64916-192">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="64916-192">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64916-193">A expressão regular encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="64916-193">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="64916-194">Uma palavra-chave da é encontrada.</span><span class="sxs-lookup"><span data-stu-id="64916-194">A keyword from is found.</span></span>
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_gps_data_1" />
          <Match idRef="Keywords_denmark_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_denmark_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_gps_data_2" />
          <Match idRef="Keywords_denmark_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_denmark_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="estonia"></a><span data-ttu-id="64916-195">Estônia</span><span class="sxs-lookup"><span data-stu-id="64916-195">Estonia</span></span>

### <a name="pattern"></a><span data-ttu-id="64916-196">Padrão</span><span class="sxs-lookup"><span data-stu-id="64916-196">Pattern</span></span>

-  <span data-ttu-id="64916-197">dígitos</span><span class="sxs-lookup"><span data-stu-id="64916-197">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64916-198">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="64916-198">Checksum</span></span>

<span data-ttu-id="64916-199">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="64916-199">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64916-200">Definição</span><span class="sxs-lookup"><span data-stu-id="64916-200">Definition</span></span>

<span data-ttu-id="64916-201">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="64916-201">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64916-202">A expressão regular encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="64916-202">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="64916-203">Uma palavra-chave da é encontrada.</span><span class="sxs-lookup"><span data-stu-id="64916-203">A keyword from is found.</span></span>
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_gps_data_1" />
          <Match idRef="Keywords_estonia_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_estonia_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_gps_data_2" />
          <Match idRef="Keywords_estonia_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_estonia_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="finland"></a><span data-ttu-id="64916-204">Finlândia</span><span class="sxs-lookup"><span data-stu-id="64916-204">Finland</span></span>

### <a name="pattern"></a><span data-ttu-id="64916-205">Padrão</span><span class="sxs-lookup"><span data-stu-id="64916-205">Pattern</span></span>

-  <span data-ttu-id="64916-206">dígitos</span><span class="sxs-lookup"><span data-stu-id="64916-206">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64916-207">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="64916-207">Checksum</span></span>

<span data-ttu-id="64916-208">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="64916-208">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64916-209">Definição</span><span class="sxs-lookup"><span data-stu-id="64916-209">Definition</span></span>

<span data-ttu-id="64916-210">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="64916-210">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64916-211">A expressão regular encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="64916-211">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="64916-212">Uma palavra-chave da é encontrada.</span><span class="sxs-lookup"><span data-stu-id="64916-212">A keyword from is found.</span></span>
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_gps_data_1" />
          <Match idRef="Keywords_finland_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_finland_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_gps_data_2" />
          <Match idRef="Keywords_finland_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_finland_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="france"></a><span data-ttu-id="64916-213">França</span><span class="sxs-lookup"><span data-stu-id="64916-213">France</span></span>

### <a name="pattern"></a><span data-ttu-id="64916-214">Padrão</span><span class="sxs-lookup"><span data-stu-id="64916-214">Pattern</span></span>

-  <span data-ttu-id="64916-215">dígitos</span><span class="sxs-lookup"><span data-stu-id="64916-215">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64916-216">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="64916-216">Checksum</span></span>

<span data-ttu-id="64916-217">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="64916-217">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64916-218">Definição</span><span class="sxs-lookup"><span data-stu-id="64916-218">Definition</span></span>

<span data-ttu-id="64916-219">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="64916-219">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64916-220">A expressão regular encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="64916-220">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="64916-221">Uma palavra-chave da é encontrada.</span><span class="sxs-lookup"><span data-stu-id="64916-221">A keyword from is found.</span></span>
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
 <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_france_eu_gps_data_1" />
          <Match idRef="Keywords_france_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_france_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_france_eu_gps_data_2" />
          <Match idRef="Keywords_france_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_france_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="germany"></a><span data-ttu-id="64916-222">Alemanha</span><span class="sxs-lookup"><span data-stu-id="64916-222">Germany</span></span>

### <a name="pattern"></a><span data-ttu-id="64916-223">Padrão</span><span class="sxs-lookup"><span data-stu-id="64916-223">Pattern</span></span>

-  <span data-ttu-id="64916-224">dígitos</span><span class="sxs-lookup"><span data-stu-id="64916-224">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64916-225">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="64916-225">Checksum</span></span>

<span data-ttu-id="64916-226">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="64916-226">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64916-227">Definição</span><span class="sxs-lookup"><span data-stu-id="64916-227">Definition</span></span>

<span data-ttu-id="64916-228">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="64916-228">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64916-229">A expressão regular encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="64916-229">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="64916-230">Uma palavra-chave da é encontrada.</span><span class="sxs-lookup"><span data-stu-id="64916-230">A keyword from is found.</span></span>
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_germany_eu_gps_data_1" />
          <Match idRef="Keywords_germany_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_germany_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_germany_eu_gps_data_2" />
          <Match idRef="Keywords_germany_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_germany_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="greece"></a><span data-ttu-id="64916-231">Grécia</span><span class="sxs-lookup"><span data-stu-id="64916-231">Greece</span></span>

### <a name="pattern"></a><span data-ttu-id="64916-232">Padrão</span><span class="sxs-lookup"><span data-stu-id="64916-232">Pattern</span></span>

-  <span data-ttu-id="64916-233">dígitos</span><span class="sxs-lookup"><span data-stu-id="64916-233">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64916-234">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="64916-234">Checksum</span></span>

<span data-ttu-id="64916-235">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="64916-235">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64916-236">Definição</span><span class="sxs-lookup"><span data-stu-id="64916-236">Definition</span></span>

<span data-ttu-id="64916-237">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="64916-237">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64916-238">A expressão regular encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="64916-238">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="64916-239">Uma palavra-chave da é encontrada.</span><span class="sxs-lookup"><span data-stu-id="64916-239">A keyword from is found.</span></span>
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_gps_data_1" />
          <Match idRef="Keywords_greece_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_greece_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_gps_data_2" />
          <Match idRef="Keywords_greece_eu_gps_data" />
        </Pattern>
</Entity>
```

## <a name="hungary"></a><span data-ttu-id="64916-240">Hungria</span><span class="sxs-lookup"><span data-stu-id="64916-240">Hungary</span></span>

### <a name="pattern"></a><span data-ttu-id="64916-241">Padrão</span><span class="sxs-lookup"><span data-stu-id="64916-241">Pattern</span></span>

-  <span data-ttu-id="64916-242">dígitos</span><span class="sxs-lookup"><span data-stu-id="64916-242">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64916-243">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="64916-243">Checksum</span></span>

<span data-ttu-id="64916-244">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="64916-244">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64916-245">Definição</span><span class="sxs-lookup"><span data-stu-id="64916-245">Definition</span></span>

<span data-ttu-id="64916-246">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="64916-246">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64916-247">A expressão regular encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="64916-247">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="64916-248">Uma palavra-chave da é encontrada.</span><span class="sxs-lookup"><span data-stu-id="64916-248">A keyword from is found.</span></span>
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_gps_data_1" />
          <Match idRef="Keywords_hungary_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_hungary_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_gps_data_2" />
          <Match idRef="Keywords_hungary_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_hungary_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="ireland"></a><span data-ttu-id="64916-249">Irlanda</span><span class="sxs-lookup"><span data-stu-id="64916-249">Ireland</span></span>

### <a name="pattern"></a><span data-ttu-id="64916-250">Padrão</span><span class="sxs-lookup"><span data-stu-id="64916-250">Pattern</span></span>

-  <span data-ttu-id="64916-251">dígitos</span><span class="sxs-lookup"><span data-stu-id="64916-251">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64916-252">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="64916-252">Checksum</span></span>

<span data-ttu-id="64916-253">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="64916-253">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64916-254">Definição</span><span class="sxs-lookup"><span data-stu-id="64916-254">Definition</span></span>

<span data-ttu-id="64916-255">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="64916-255">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64916-256">A expressão regular encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="64916-256">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="64916-257">Uma palavra-chave da é encontrada.</span><span class="sxs-lookup"><span data-stu-id="64916-257">A keyword from is found.</span></span>
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_gps_data_1" />
          <Match idRef="Keywords_ireland_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_ireland_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_gps_data_2" />
          <Match idRef="Keywords_ireland_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_ireland_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="italy"></a><span data-ttu-id="64916-258">Itália</span><span class="sxs-lookup"><span data-stu-id="64916-258">Italy</span></span>

### <a name="pattern"></a><span data-ttu-id="64916-259">Padrão</span><span class="sxs-lookup"><span data-stu-id="64916-259">Pattern</span></span>

-  <span data-ttu-id="64916-260">dígitos</span><span class="sxs-lookup"><span data-stu-id="64916-260">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64916-261">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="64916-261">Checksum</span></span>

<span data-ttu-id="64916-262">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="64916-262">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64916-263">Definição</span><span class="sxs-lookup"><span data-stu-id="64916-263">Definition</span></span>

<span data-ttu-id="64916-264">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="64916-264">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64916-265">A expressão regular encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="64916-265">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="64916-266">Uma palavra-chave da é encontrada.</span><span class="sxs-lookup"><span data-stu-id="64916-266">A keyword from is found.</span></span>
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_gps_data_1" />
          <Match idRef="Keywords_italy_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_italy_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_gps_data_2" />
          <Match idRef="Keywords_italy_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_italy_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="latvia"></a><span data-ttu-id="64916-267">Letônia</span><span class="sxs-lookup"><span data-stu-id="64916-267">Latvia</span></span>

### <a name="pattern"></a><span data-ttu-id="64916-268">Padrão</span><span class="sxs-lookup"><span data-stu-id="64916-268">Pattern</span></span>

-  <span data-ttu-id="64916-269">dígitos</span><span class="sxs-lookup"><span data-stu-id="64916-269">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64916-270">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="64916-270">Checksum</span></span>

<span data-ttu-id="64916-271">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="64916-271">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64916-272">Definição</span><span class="sxs-lookup"><span data-stu-id="64916-272">Definition</span></span>

<span data-ttu-id="64916-273">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="64916-273">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64916-274">A expressão regular encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="64916-274">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="64916-275">Uma palavra-chave da é encontrada.</span><span class="sxs-lookup"><span data-stu-id="64916-275">A keyword from is found.</span></span>
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_gps_data_1" />
          <Match idRef="Keywords_latvia_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_latvia_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_gps_data_2" />
          <Match idRef="Keywords_latvia_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_latvia_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="lithuania"></a><span data-ttu-id="64916-276">Lituânia</span><span class="sxs-lookup"><span data-stu-id="64916-276">Lithuania</span></span>

### <a name="pattern"></a><span data-ttu-id="64916-277">Padrão</span><span class="sxs-lookup"><span data-stu-id="64916-277">Pattern</span></span>

-  <span data-ttu-id="64916-278">dígitos</span><span class="sxs-lookup"><span data-stu-id="64916-278">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64916-279">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="64916-279">Checksum</span></span>

<span data-ttu-id="64916-280">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="64916-280">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64916-281">Definição</span><span class="sxs-lookup"><span data-stu-id="64916-281">Definition</span></span>

<span data-ttu-id="64916-282">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="64916-282">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64916-283">A expressão regular encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="64916-283">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="64916-284">Uma palavra-chave da é encontrada.</span><span class="sxs-lookup"><span data-stu-id="64916-284">A keyword from is found.</span></span>
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_gps_data_1" />
          <Match idRef="Keywords_lithuania_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_lithuania_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_gps_data_2" />
          <Match idRef="Keywords_lithuania_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_lithuania_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="luxemburg"></a><span data-ttu-id="64916-285">Luxemburgo</span><span class="sxs-lookup"><span data-stu-id="64916-285">Luxemburg</span></span>

### <a name="pattern"></a><span data-ttu-id="64916-286">Padrão</span><span class="sxs-lookup"><span data-stu-id="64916-286">Pattern</span></span>

-  <span data-ttu-id="64916-287">dígitos</span><span class="sxs-lookup"><span data-stu-id="64916-287">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64916-288">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="64916-288">Checksum</span></span>

<span data-ttu-id="64916-289">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="64916-289">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64916-290">Definição</span><span class="sxs-lookup"><span data-stu-id="64916-290">Definition</span></span>

<span data-ttu-id="64916-291">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="64916-291">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64916-292">A expressão regular encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="64916-292">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="64916-293">Uma palavra-chave da é encontrada.</span><span class="sxs-lookup"><span data-stu-id="64916-293">A keyword from is found.</span></span>
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_gps_data_1" />
          <Match idRef="Keywords_luxemburg_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_luxemburg_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_gps_data_2" />
          <Match idRef="Keywords_luxemburg_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_luxemburg_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="malta"></a><span data-ttu-id="64916-294">Malta</span><span class="sxs-lookup"><span data-stu-id="64916-294">Malta</span></span>

### <a name="pattern"></a><span data-ttu-id="64916-295">Padrão</span><span class="sxs-lookup"><span data-stu-id="64916-295">Pattern</span></span>

-  <span data-ttu-id="64916-296">dígitos</span><span class="sxs-lookup"><span data-stu-id="64916-296">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64916-297">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="64916-297">Checksum</span></span>

<span data-ttu-id="64916-298">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="64916-298">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64916-299">Definição</span><span class="sxs-lookup"><span data-stu-id="64916-299">Definition</span></span>

<span data-ttu-id="64916-300">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="64916-300">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64916-301">A expressão regular encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="64916-301">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="64916-302">Uma palavra-chave da é encontrada.</span><span class="sxs-lookup"><span data-stu-id="64916-302">A keyword from is found.</span></span>
    
```
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_gps_data_1" />
          <Match idRef="Keywords_malta_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_malta_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_gps_data_2" />
          <Match idRef="Keywords_malta_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_malta_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="netherlands"></a><span data-ttu-id="64916-303">Países Baixos</span><span class="sxs-lookup"><span data-stu-id="64916-303">Netherlands</span></span>

### <a name="pattern"></a><span data-ttu-id="64916-304">Padrão</span><span class="sxs-lookup"><span data-stu-id="64916-304">Pattern</span></span>

-  <span data-ttu-id="64916-305">dígitos</span><span class="sxs-lookup"><span data-stu-id="64916-305">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64916-306">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="64916-306">Checksum</span></span>

<span data-ttu-id="64916-307">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="64916-307">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64916-308">Definição</span><span class="sxs-lookup"><span data-stu-id="64916-308">Definition</span></span>

<span data-ttu-id="64916-309">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="64916-309">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64916-310">A expressão regular encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="64916-310">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="64916-311">Uma palavra-chave da é encontrada.</span><span class="sxs-lookup"><span data-stu-id="64916-311">A keyword from is found.</span></span>
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_gps_data_1" />
          <Match idRef="Keywords_netherlands_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_netherlands_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_gps_data_2" />
          <Match idRef="Keywords_netherlands_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_netherlands_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="poland"></a><span data-ttu-id="64916-312">Polônia</span><span class="sxs-lookup"><span data-stu-id="64916-312">Poland</span></span>

### <a name="pattern"></a><span data-ttu-id="64916-313">Padrão</span><span class="sxs-lookup"><span data-stu-id="64916-313">Pattern</span></span>

-  <span data-ttu-id="64916-314">dígitos</span><span class="sxs-lookup"><span data-stu-id="64916-314">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64916-315">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="64916-315">Checksum</span></span>

<span data-ttu-id="64916-316">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="64916-316">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64916-317">Definição</span><span class="sxs-lookup"><span data-stu-id="64916-317">Definition</span></span>

<span data-ttu-id="64916-318">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="64916-318">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64916-319">A expressão regular encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="64916-319">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="64916-320">Uma palavra-chave da é encontrada.</span><span class="sxs-lookup"><span data-stu-id="64916-320">A keyword from is found.</span></span>
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_gps_data_1" />
          <Match idRef="Keywords_poland_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_poland_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_gps_data_2" />
          <Match idRef="Keywords_poland_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_poland_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="portugal"></a><span data-ttu-id="64916-321">Portugal</span><span class="sxs-lookup"><span data-stu-id="64916-321">Portugal</span></span>

### <a name="pattern"></a><span data-ttu-id="64916-322">Padrão</span><span class="sxs-lookup"><span data-stu-id="64916-322">Pattern</span></span>

-  <span data-ttu-id="64916-323">dígitos</span><span class="sxs-lookup"><span data-stu-id="64916-323">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64916-324">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="64916-324">Checksum</span></span>

<span data-ttu-id="64916-325">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="64916-325">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64916-326">Definição</span><span class="sxs-lookup"><span data-stu-id="64916-326">Definition</span></span>

<span data-ttu-id="64916-327">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="64916-327">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64916-328">A expressão regular encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="64916-328">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="64916-329">Uma palavra-chave da é encontrada.</span><span class="sxs-lookup"><span data-stu-id="64916-329">A keyword from is found.</span></span>
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_gps_data_1" />
          <Match idRef="Keywords_portugal_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_portugal_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_gps_data_2" />
          <Match idRef="Keywords_portugal_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_portugal_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="romania"></a><span data-ttu-id="64916-330">Romênia</span><span class="sxs-lookup"><span data-stu-id="64916-330">Romania</span></span>

### <a name="pattern"></a><span data-ttu-id="64916-331">Padrão</span><span class="sxs-lookup"><span data-stu-id="64916-331">Pattern</span></span>

-  <span data-ttu-id="64916-332">dígitos</span><span class="sxs-lookup"><span data-stu-id="64916-332">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64916-333">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="64916-333">Checksum</span></span>

<span data-ttu-id="64916-334">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="64916-334">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64916-335">Definição</span><span class="sxs-lookup"><span data-stu-id="64916-335">Definition</span></span>

<span data-ttu-id="64916-336">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="64916-336">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64916-337">A expressão regular encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="64916-337">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="64916-338">Uma palavra-chave da é encontrada.</span><span class="sxs-lookup"><span data-stu-id="64916-338">A keyword from is found.</span></span>
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_gps_data_1" />
          <Match idRef="Keywords_romania_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_romania_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_gps_data_2" />
          <Match idRef="Keywords_romania_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_romania_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="slovakia"></a><span data-ttu-id="64916-339">Eslováquia</span><span class="sxs-lookup"><span data-stu-id="64916-339">Slovakia</span></span>

### <a name="pattern"></a><span data-ttu-id="64916-340">Padrão</span><span class="sxs-lookup"><span data-stu-id="64916-340">Pattern</span></span>

-  <span data-ttu-id="64916-341">dígitos</span><span class="sxs-lookup"><span data-stu-id="64916-341">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64916-342">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="64916-342">Checksum</span></span>

<span data-ttu-id="64916-343">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="64916-343">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64916-344">Definição</span><span class="sxs-lookup"><span data-stu-id="64916-344">Definition</span></span>

<span data-ttu-id="64916-345">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="64916-345">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64916-346">A expressão regular encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="64916-346">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="64916-347">Uma palavra-chave da é encontrada.</span><span class="sxs-lookup"><span data-stu-id="64916-347">A keyword from is found.</span></span>
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_gps_data_1" />
          <Match idRef="Keywords_slovakia_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_slovakia_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_gps_data_2" />
          <Match idRef="Keywords_slovakia_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_slovakia_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="slovenia"></a><span data-ttu-id="64916-348">Eslovênia</span><span class="sxs-lookup"><span data-stu-id="64916-348">Slovenia</span></span>

### <a name="pattern"></a><span data-ttu-id="64916-349">Padrão</span><span class="sxs-lookup"><span data-stu-id="64916-349">Pattern</span></span>

-  <span data-ttu-id="64916-350">dígitos</span><span class="sxs-lookup"><span data-stu-id="64916-350">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64916-351">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="64916-351">Checksum</span></span>

<span data-ttu-id="64916-352">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="64916-352">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64916-353">Definição</span><span class="sxs-lookup"><span data-stu-id="64916-353">Definition</span></span>

<span data-ttu-id="64916-354">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="64916-354">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64916-355">A expressão regular encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="64916-355">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="64916-356">Uma palavra-chave da é encontrada.</span><span class="sxs-lookup"><span data-stu-id="64916-356">A keyword from is found.</span></span>
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_gps_data_1" />
          <Match idRef="Keywords_slovenia_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_slovenia_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_gps_data_2" />
          <Match idRef="Keywords_slovenia_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_slovenia_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="spain"></a><span data-ttu-id="64916-357">Espanha</span><span class="sxs-lookup"><span data-stu-id="64916-357">Spain</span></span>

### <a name="pattern"></a><span data-ttu-id="64916-358">Padrão</span><span class="sxs-lookup"><span data-stu-id="64916-358">Pattern</span></span>

-  <span data-ttu-id="64916-359">dígitos</span><span class="sxs-lookup"><span data-stu-id="64916-359">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64916-360">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="64916-360">Checksum</span></span>

<span data-ttu-id="64916-361">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="64916-361">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64916-362">Definição</span><span class="sxs-lookup"><span data-stu-id="64916-362">Definition</span></span>

<span data-ttu-id="64916-363">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="64916-363">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64916-364">A expressão regular encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="64916-364">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="64916-365">Uma palavra-chave da é encontrada.</span><span class="sxs-lookup"><span data-stu-id="64916-365">A keyword from is found.</span></span>
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_gps_data_1" />
          <Match idRef="Keywords_spain_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_spain_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_gps_data_2" />
          <Match idRef="Keywords_spain_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_spain_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="sweden"></a><span data-ttu-id="64916-366">Suécia</span><span class="sxs-lookup"><span data-stu-id="64916-366">Sweden</span></span>

### <a name="pattern"></a><span data-ttu-id="64916-367">Padrão</span><span class="sxs-lookup"><span data-stu-id="64916-367">Pattern</span></span>

-  <span data-ttu-id="64916-368">dígitos</span><span class="sxs-lookup"><span data-stu-id="64916-368">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64916-369">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="64916-369">Checksum</span></span>

<span data-ttu-id="64916-370">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="64916-370">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64916-371">Definição</span><span class="sxs-lookup"><span data-stu-id="64916-371">Definition</span></span>

<span data-ttu-id="64916-372">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="64916-372">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64916-373">A expressão regular encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="64916-373">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="64916-374">Uma palavra-chave da é encontrada.</span><span class="sxs-lookup"><span data-stu-id="64916-374">A keyword from is found.</span></span>
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_gps_data_1" />
          <Match idRef="Keywords_sweden_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_sweden_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_gps_data_2" />
          <Match idRef="Keywords_sweden_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_sweden_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="uk"></a><span data-ttu-id="64916-375">REINO UNIDO</span><span class="sxs-lookup"><span data-stu-id="64916-375">UK</span></span>

### <a name="pattern"></a><span data-ttu-id="64916-376">Padrão</span><span class="sxs-lookup"><span data-stu-id="64916-376">Pattern</span></span>

-  <span data-ttu-id="64916-377">dígitos</span><span class="sxs-lookup"><span data-stu-id="64916-377">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64916-378">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="64916-378">Checksum</span></span>

<span data-ttu-id="64916-379">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="64916-379">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64916-380">Definição</span><span class="sxs-lookup"><span data-stu-id="64916-380">Definition</span></span>

<span data-ttu-id="64916-381">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="64916-381">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64916-382">A expressão regular encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="64916-382">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="64916-383">Uma palavra-chave da é encontrada.</span><span class="sxs-lookup"><span data-stu-id="64916-383">A keyword from is found.</span></span>
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_uk_eu_gps_data_1" />
          <Match idRef="Keywords_uk_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_uk_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_uk_eu_gps_data_2" />
          <Match idRef="Keywords_uk_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_uk_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="see-also"></a><span data-ttu-id="64916-384">Confira também</span><span class="sxs-lookup"><span data-stu-id="64916-384">See also</span></span>

[<span data-ttu-id="64916-385">O que os tipos de informações confidenciais procuram</span><span class="sxs-lookup"><span data-stu-id="64916-385">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)


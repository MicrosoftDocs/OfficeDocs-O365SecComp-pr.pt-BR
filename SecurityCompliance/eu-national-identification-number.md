---
title: Número de identificação nacional da UE
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 2ea971bf-9434-4b61-b825-2bbd28ae6064
description: Este tópico mostra o que uma política de prevenção (DLP) de perda de dados procura por quando detecta o tipo de informações confidenciais de número de identificação nacional da UE. Esse tipo de informações confidenciais define diferentes padrões, palavras-chave e outras evidências para cada país.
ms.openlocfilehash: 29d2126b937ff46039284a74eb2a84f2ebbacb41
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523996"
---
# <a name="eu-national-identification-number"></a><span data-ttu-id="05f15-104">Número de identificação nacional da UE</span><span class="sxs-lookup"><span data-stu-id="05f15-104">EU National Identification Number</span></span>

<span data-ttu-id="05f15-p102">Este tópico mostra o que uma política de prevenção (DLP) de perda de dados procura por quando detecta o tipo de informações confidenciais de número de identificação nacional da UE. Esse tipo de informações confidenciais define diferentes padrões, palavras-chave e outras evidências para cada país.</span><span class="sxs-lookup"><span data-stu-id="05f15-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU National Identification Number sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="05f15-107">Áustria</span><span class="sxs-lookup"><span data-stu-id="05f15-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="05f15-108">Formato</span><span class="sxs-lookup"><span data-stu-id="05f15-108">Format</span></span>

<span data-ttu-id="05f15-109">Uma combinação de 24 caracteres de letras, dígitos e caracteres especiais</span><span class="sxs-lookup"><span data-stu-id="05f15-109">A 24-character combination of letters, digits, and special characters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="05f15-110">Padrão</span><span class="sxs-lookup"><span data-stu-id="05f15-110">Pattern</span></span>

<span data-ttu-id="05f15-111">24 de caracteres:</span><span class="sxs-lookup"><span data-stu-id="05f15-111">24 characters:</span></span>
  
-  <span data-ttu-id="05f15-112">22 letras (não diferencia maiusculas de minúsculas), dígitos, barras invertidas, barras ou sinais de adição</span><span class="sxs-lookup"><span data-stu-id="05f15-112">22 letters (not case-sensitive), digits, backslashes, forward slashes, or plus signs</span></span> 
    
- <span data-ttu-id="05f15-113">(Não diferencia maiusculas de minúsculas) de duas letras, dígitos, barras invertidas, barras, sinais de adição ou sinais de igual</span><span class="sxs-lookup"><span data-stu-id="05f15-113">Two letters (not case-sensitive), digits, backslashes, forward slashes, plus signs, or equal signs</span></span>
    
### <a name="checksum"></a><span data-ttu-id="05f15-114">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="05f15-114">Checksum</span></span>

<span data-ttu-id="05f15-115">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="05f15-115">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="05f15-116">Definição</span><span class="sxs-lookup"><span data-stu-id="05f15-116">Definition</span></span>

<span data-ttu-id="05f15-117">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="05f15-117">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="05f15-118">A expressão regular `Regex_austria_eu_national_id_card` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="05f15-118">The regular expression  `Regex_austria_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="05f15-119">Uma palavra-chave da `Keywords_austria_eu_national_id_card` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="05f15-119">A keyword from  `Keywords_austria_eu_national_id_card` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_national_id_card" />
          <Match idRef="Keywords_austria_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="05f15-120">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="05f15-120">Keywords</span></span>

#### <a name="keywordsaustriaeunationalidcard"></a><span data-ttu-id="05f15-121">Keywords_austria_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="05f15-121">Keywords_austria_eu_national_id_card</span></span>

<span data-ttu-id="05f15-122">número de identidade austríaco</span><span class="sxs-lookup"><span data-stu-id="05f15-122">austrian identity number</span></span>
  
<span data-ttu-id="05f15-123">número de identidade nacional</span><span class="sxs-lookup"><span data-stu-id="05f15-123">national identity number</span></span>
  
<span data-ttu-id="05f15-124">número de identidade</span><span class="sxs-lookup"><span data-stu-id="05f15-124">identity number</span></span>
  
<span data-ttu-id="05f15-125">
national id</span><span class="sxs-lookup"><span data-stu-id="05f15-125">national id</span></span>
  
<span data-ttu-id="05f15-126">personalausweis republik österreich</span><span class="sxs-lookup"><span data-stu-id="05f15-126">personalausweis republik österreich</span></span>
  
## <a name="belgium"></a><span data-ttu-id="05f15-127">Bélgica</span><span class="sxs-lookup"><span data-stu-id="05f15-127">Belgium</span></span>

<span data-ttu-id="05f15-128">Para obter detalhes, consulte a seção "Bélgica nacional Number" em [quais tipos de informações confidenciais a procurar](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="05f15-128">For details, see the section "Belgium National Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="bulgaria"></a><span data-ttu-id="05f15-129">Bulgária</span><span class="sxs-lookup"><span data-stu-id="05f15-129">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="05f15-130">Formato</span><span class="sxs-lookup"><span data-stu-id="05f15-130">Format</span></span>

<span data-ttu-id="05f15-131">Dez dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="05f15-131">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="05f15-132">Padrão</span><span class="sxs-lookup"><span data-stu-id="05f15-132">Pattern</span></span>

<span data-ttu-id="05f15-133">Dez dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="05f15-133">Ten digits without spaces and delimiters</span></span>
  
-  <span data-ttu-id="05f15-134">Seis dígitos que correspondem à data de nascimento (aammdd)</span><span class="sxs-lookup"><span data-stu-id="05f15-134">Six digits that correspond to the birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="05f15-135">Dois dígitos correspondentes na ordem de nascimento</span><span class="sxs-lookup"><span data-stu-id="05f15-135">Two digits that correspond to the birth order</span></span>
    
- <span data-ttu-id="05f15-136">Um dígito que corresponde ao gênero: um dígito par de masculino e um dígito ímpar para fêmea</span><span class="sxs-lookup"><span data-stu-id="05f15-136">One digit that corresponds to gender: An even digit for male and an odd digit for female</span></span>
    
- <span data-ttu-id="05f15-137">Seleção de um dígito</span><span class="sxs-lookup"><span data-stu-id="05f15-137">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="05f15-138">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="05f15-138">Checksum</span></span>

<span data-ttu-id="05f15-139">Sim</span><span class="sxs-lookup"><span data-stu-id="05f15-139">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="05f15-140">Definição</span><span class="sxs-lookup"><span data-stu-id="05f15-140">Definition</span></span>

<span data-ttu-id="05f15-141">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="05f15-141">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="05f15-142">A função `Func_bulgaria_national_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="05f15-142">The function  `Func_bulgaria_national_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="05f15-143">Uma palavra-chave da `Keywords_bulgaria_national_number` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="05f15-143">A keyword from  `Keywords_bulgaria_national_number` is found.</span></span> 
    
<span data-ttu-id="05f15-144">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="05f15-144">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="05f15-145">A função `Func_bulgaria_national_number` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="05f15-145">The function  `Func_bulgaria_national_number` finds content that matches the pattern.</span></span> 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_bulgaria_national_number" />
          <Match idRef="Keywords_bulgaria_national_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_bulgaria_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="05f15-146">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="05f15-146">Keywords</span></span>

#### <a name="keywordsbulgarianationalnumber"></a><span data-ttu-id="05f15-147">Keywords_bulgaria_national_number</span><span class="sxs-lookup"><span data-stu-id="05f15-147">Keywords_bulgaria_national_number</span></span>

<span data-ttu-id="05f15-148">egn</span><span class="sxs-lookup"><span data-stu-id="05f15-148">egn</span></span>
  
<span data-ttu-id="05f15-149">egn #</span><span class="sxs-lookup"><span data-stu-id="05f15-149">egn#</span></span>
  
<span data-ttu-id="05f15-150">número nacional búlgaro</span><span class="sxs-lookup"><span data-stu-id="05f15-150">bulgarian national number</span></span>
  
<span data-ttu-id="05f15-151">número nacional</span><span class="sxs-lookup"><span data-stu-id="05f15-151">national number</span></span>
  
<span data-ttu-id="05f15-152">social security number
</span><span class="sxs-lookup"><span data-stu-id="05f15-152">social security number</span></span>
  
<span data-ttu-id="05f15-153">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="05f15-153">nationalnumber#</span></span>
  
<span data-ttu-id="05f15-154">SSN #</span><span class="sxs-lookup"><span data-stu-id="05f15-154">ssn#</span></span>
  
<span data-ttu-id="05f15-155">SSN</span><span class="sxs-lookup"><span data-stu-id="05f15-155">ssn</span></span>
  
<span data-ttu-id="05f15-156">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="05f15-156">nationalnumber</span></span>
  
<span data-ttu-id="05f15-157">bnn #</span><span class="sxs-lookup"><span data-stu-id="05f15-157">bnn#</span></span>
  
<span data-ttu-id="05f15-158">bnn</span><span class="sxs-lookup"><span data-stu-id="05f15-158">bnn</span></span>
  
<span data-ttu-id="05f15-159">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="05f15-159">personal id number</span></span>
  
<span data-ttu-id="05f15-160">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="05f15-160">personalidnumber#</span></span>
  
<span data-ttu-id="05f15-161">ЕДИНЕН ГРАЖДАНСКИ НОМЕР</span><span class="sxs-lookup"><span data-stu-id="05f15-161">единен граждански номер</span></span>
  
<span data-ttu-id="05f15-162">edinen grazhdanski nomer</span><span class="sxs-lookup"><span data-stu-id="05f15-162">edinen grazhdanski nomer</span></span>
  
<span data-ttu-id="05f15-163">ЕГН</span><span class="sxs-lookup"><span data-stu-id="05f15-163">егн</span></span>
  
<span data-ttu-id="05f15-164">ЕГН #</span><span class="sxs-lookup"><span data-stu-id="05f15-164">егн#</span></span>
  
## <a name="croatia"></a><span data-ttu-id="05f15-165">Croácia</span><span class="sxs-lookup"><span data-stu-id="05f15-165">Croatia</span></span>

<span data-ttu-id="05f15-166">Para obter detalhes, consulte a seção "Croácia identidade Number" em [quais tipos de informações confidenciais a procurar](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="05f15-166">For details, see the section "Croatia Identity Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="cyprus"></a><span data-ttu-id="05f15-167">Chipre</span><span class="sxs-lookup"><span data-stu-id="05f15-167">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="05f15-168">Formato</span><span class="sxs-lookup"><span data-stu-id="05f15-168">Format</span></span>

<span data-ttu-id="05f15-169">Dez dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="05f15-169">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="05f15-170">Padrão</span><span class="sxs-lookup"><span data-stu-id="05f15-170">Pattern</span></span>

 <span data-ttu-id="05f15-171">Dez dígitos</span><span class="sxs-lookup"><span data-stu-id="05f15-171">Ten digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="05f15-172">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="05f15-172">Checksum</span></span>

<span data-ttu-id="05f15-173">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="05f15-173">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="05f15-174">Definição</span><span class="sxs-lookup"><span data-stu-id="05f15-174">Definition</span></span>

<span data-ttu-id="05f15-175">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="05f15-175">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="05f15-176">A expressão regular `Regex_cyprus_eu_national_id_card` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="05f15-176">The regular expression  `Regex_cyprus_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="05f15-177">Uma palavra-chave da `Keywords_cyprus_eu_national_id_card` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="05f15-177">A keyword from  `Keywords_cyprus_eu_national_id_card` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_national_id_card" />
          <Match idRef="Keywords_cyprus_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="05f15-178">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="05f15-178">Keywords</span></span>

#### <a name="keywordscypruseunationalidcard"></a><span data-ttu-id="05f15-179">Keywords_cyprus_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="05f15-179">Keywords_cyprus_eu_national_id_card</span></span>

<span data-ttu-id="05f15-180">número de cartão de identificação</span><span class="sxs-lookup"><span data-stu-id="05f15-180">id card number</span></span>
  
<span data-ttu-id="05f15-181">número de identificação nacional</span><span class="sxs-lookup"><span data-stu-id="05f15-181">national identification number</span></span>
  
<span data-ttu-id="05f15-182">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="05f15-182">personal id number</span></span>
  
<span data-ttu-id="05f15-183">número de cartão de identificação</span><span class="sxs-lookup"><span data-stu-id="05f15-183">identity card number</span></span>
  
<span data-ttu-id="05f15-184">ΤΑΥΤΟΤΗΤΑΣ</span><span class="sxs-lookup"><span data-stu-id="05f15-184">ταυτοτητασ</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="05f15-185">República Tcheca</span><span class="sxs-lookup"><span data-stu-id="05f15-185">Czech Republic</span></span>

<span data-ttu-id="05f15-186">Para obter detalhes, consulte a seção "Tcheco nacional identidade Number" em [quais tipos de informações confidenciais a procurar](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="05f15-186">For details, see the section "Czech National Identity Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="denmark"></a><span data-ttu-id="05f15-187">Dinamarca</span><span class="sxs-lookup"><span data-stu-id="05f15-187">Denmark</span></span>

<span data-ttu-id="05f15-188">Para obter detalhes, consulte a seção "Dinamarca número de identificação pessoal" nos [quais os tipos de informações confidenciais procurar](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="05f15-188">For details, see the section "Denmark Personal Identification Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="estonia"></a><span data-ttu-id="05f15-189">Estônia</span><span class="sxs-lookup"><span data-stu-id="05f15-189">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="05f15-190">Formato</span><span class="sxs-lookup"><span data-stu-id="05f15-190">Format</span></span>

<span data-ttu-id="05f15-191">11 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="05f15-191">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="05f15-192">Padrão</span><span class="sxs-lookup"><span data-stu-id="05f15-192">Pattern</span></span>

<span data-ttu-id="05f15-193">11 dígitos:</span><span class="sxs-lookup"><span data-stu-id="05f15-193">11 digits:</span></span>
  
- <span data-ttu-id="05f15-194">Um dígito que corresponde ao sexo e century de nascimento (Masculino número ímpar, o número de par feminino; 1-2: 19 century; 3 e 4: 20 century; 5-6: 21 century)</span><span class="sxs-lookup"><span data-stu-id="05f15-194">One digit that corresponds to sex and century of birth (odd number male, even number female; 1-2: 19th century; 3-4: 20th century; 5-6: 21st century)</span></span>
    
- <span data-ttu-id="05f15-195">Seis dígitos que correspondem à data de nascimento (aammdd)</span><span class="sxs-lookup"><span data-stu-id="05f15-195">Six digits that correspond to date of birth (YYMMDD)</span></span>
    
- <span data-ttu-id="05f15-196">Três dígitos que correspondem a um número de série separando pessoas nascidas na mesma data</span><span class="sxs-lookup"><span data-stu-id="05f15-196">Three digits that correspond to a serial number separating persons born on the same date</span></span>
    
- <span data-ttu-id="05f15-197">Seleção de um dígito</span><span class="sxs-lookup"><span data-stu-id="05f15-197">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="05f15-198">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="05f15-198">Checksum</span></span>

<span data-ttu-id="05f15-199">Sim</span><span class="sxs-lookup"><span data-stu-id="05f15-199">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="05f15-200">Definição</span><span class="sxs-lookup"><span data-stu-id="05f15-200">Definition</span></span>

<span data-ttu-id="05f15-201">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="05f15-201">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="05f15-202">A função `Func_estonia_eu_national_id_card` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="05f15-202">The function  `Func_estonia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="05f15-203">Uma palavra-chave da `Keywords_estonia_eu_national_id_card` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="05f15-203">A keyword from  `Keywords_estonia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="05f15-204">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="05f15-204">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="05f15-205">A função `Func_estonia_eu_national_id_card` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="05f15-205">The function  `Func_estonia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_estonia_eu_national_id_card" />
          <Match idRef="Keywords_estonia_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_estonia_eu_national_id_card" />
</Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="05f15-206">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="05f15-206">Keywords</span></span>

#### <a name="keywordsestoniaeunationalidcard"></a><span data-ttu-id="05f15-207">Keywords_estonia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="05f15-207">Keywords_estonia_eu_national_id_card</span></span>

<span data-ttu-id="05f15-208">código de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="05f15-208">personal identification code</span></span>
  
<span data-ttu-id="05f15-209">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="05f15-209">personal identification number</span></span>
  
<span data-ttu-id="05f15-210">número de identificação nacional</span><span class="sxs-lookup"><span data-stu-id="05f15-210">national identification number</span></span>
  
<span data-ttu-id="05f15-211">número nacional</span><span class="sxs-lookup"><span data-stu-id="05f15-211">national number</span></span>
  
<span data-ttu-id="05f15-212">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="05f15-212">personal id number</span></span>
  
<span data-ttu-id="05f15-213">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="05f15-213">personalidnumber#</span></span>
  
<span data-ttu-id="05f15-214">IK</span><span class="sxs-lookup"><span data-stu-id="05f15-214">ik</span></span>
  
<span data-ttu-id="05f15-215">isikukood</span><span class="sxs-lookup"><span data-stu-id="05f15-215">isikukood</span></span>
  
<span data-ttu-id="05f15-216">ID-kaart</span><span class="sxs-lookup"><span data-stu-id="05f15-216">id-kaart</span></span>
  
## <a name="finland"></a><span data-ttu-id="05f15-217">Finlândia</span><span class="sxs-lookup"><span data-stu-id="05f15-217">Finland</span></span>

<span data-ttu-id="05f15-218">Para obter detalhes, consulte a seção "ID nacional da Finlândia" nos [quais os tipos de informações confidenciais procurar](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="05f15-218">For details, see the section "Finland National ID" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="05f15-219">França</span><span class="sxs-lookup"><span data-stu-id="05f15-219">France</span></span>

<span data-ttu-id="05f15-220">Para obter detalhes, consulte a seção "França nacional cartão de identificação (CNI)" em [quais tipos de informações confidenciais a procurar](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="05f15-220">For details, see the section "France National ID Card (CNI)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="05f15-221">Alemanha</span><span class="sxs-lookup"><span data-stu-id="05f15-221">Germany</span></span>

<span data-ttu-id="05f15-222">Para obter detalhes, consulte a seção "Número de cartão de identificação da Alemanha" em [quais tipos de informações confidenciais a procurar](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="05f15-222">For details, see the section "Germany Identity Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="05f15-223">Grécia</span><span class="sxs-lookup"><span data-stu-id="05f15-223">Greece</span></span>

<span data-ttu-id="05f15-224">Para obter detalhes, consulte a seção "Grécia cartão de identificação nacional" nos [quais os tipos de informações confidenciais procurar](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="05f15-224">For details, see the section "Greece National ID Card" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="hungary"></a><span data-ttu-id="05f15-225">Hungria</span><span class="sxs-lookup"><span data-stu-id="05f15-225">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="05f15-226">Formato</span><span class="sxs-lookup"><span data-stu-id="05f15-226">Format</span></span>

<span data-ttu-id="05f15-227">11 dígitos</span><span class="sxs-lookup"><span data-stu-id="05f15-227">11 digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="05f15-228">Padrão</span><span class="sxs-lookup"><span data-stu-id="05f15-228">Pattern</span></span>

<span data-ttu-id="05f15-229">11 dígitos:</span><span class="sxs-lookup"><span data-stu-id="05f15-229">11 digits:</span></span>
  
-  <span data-ttu-id="05f15-230">Um dígito que corresponde ao gênero (Masculino-1, 2-fêmea, outros números também são possíveis para cidadãos nascidos antes de 1900 ou cidadãos com ações sociais double)</span><span class="sxs-lookup"><span data-stu-id="05f15-230">One digit that corresponds to gender (1-male, 2-female, other numbers are also possible for citizens born before 1900 or citizens with double citizenship)</span></span> 
    
- <span data-ttu-id="05f15-231">Seis dígitos que correspondem à data de nascimento (aammdd)</span><span class="sxs-lookup"><span data-stu-id="05f15-231">Six digits that correspond to birth date (YYMMDD)</span></span>
    
- <span data-ttu-id="05f15-232">Três dígitos que correspondem a um número de série</span><span class="sxs-lookup"><span data-stu-id="05f15-232">Three digits that correspond to a serial number</span></span>
    
- <span data-ttu-id="05f15-233">Seleção de um dígito</span><span class="sxs-lookup"><span data-stu-id="05f15-233">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="05f15-234">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="05f15-234">Checksum</span></span>

<span data-ttu-id="05f15-235">Sim</span><span class="sxs-lookup"><span data-stu-id="05f15-235">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="05f15-236">Definição</span><span class="sxs-lookup"><span data-stu-id="05f15-236">Definition</span></span>

<span data-ttu-id="05f15-237">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="05f15-237">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="05f15-238">A função `Func_hungary_eu_national_id_card` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="05f15-238">The function  `Func_hungary_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="05f15-239">Uma palavra-chave da `Keywords_hungary_eu_national_id_card` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="05f15-239">A keyword from  `Keywords_hungary_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="05f15-240">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="05f15-240">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="05f15-241">A função `Func_hungary_eu_national_id_card` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="05f15-241">The function  `Func_hungary_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_hungary_eu_national_id_card" />
          <Match idRef="Keywords_hungary_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_hungary_eu_national_id_card" />
</Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="05f15-242">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="05f15-242">Keywords</span></span>

#### <a name="keywordshungaryeunationalidcard"></a><span data-ttu-id="05f15-243">Keywords_hungary_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="05f15-243">Keywords_hungary_eu_national_id_card</span></span>

<span data-ttu-id="05f15-244">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="05f15-244">personal identification number</span></span>
  
<span data-ttu-id="05f15-245">identification number
</span><span class="sxs-lookup"><span data-stu-id="05f15-245">identification number</span></span>
  
<span data-ttu-id="05f15-246">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="05f15-246">personal id number</span></span>
  
<span data-ttu-id="05f15-247">személyazonosító igazolvány</span><span class="sxs-lookup"><span data-stu-id="05f15-247">személyazonosító igazolvány</span></span>
  
## <a name="ireland"></a><span data-ttu-id="05f15-248">Irlanda</span><span class="sxs-lookup"><span data-stu-id="05f15-248">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="05f15-249">Formato</span><span class="sxs-lookup"><span data-stu-id="05f15-249">Format</span></span>

<span data-ttu-id="05f15-250">Uma combinação de nove caracteres de letras, dígitos e um espaço no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="05f15-250">A nine-character combination of letters, digits, and a space in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="05f15-251">Padrão</span><span class="sxs-lookup"><span data-stu-id="05f15-251">Pattern</span></span>

<span data-ttu-id="05f15-252">Uma combinação de nove caracteres de letras, dígitos e um espaço no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="05f15-252">A nine-character combination of letters, digits, and a space in the specified pattern</span></span>
  
<span data-ttu-id="05f15-253">A partir de 01 de janeiro de 2013 para now:</span><span class="sxs-lookup"><span data-stu-id="05f15-253">From 01 January 2013 to now:</span></span>
  
-  <span data-ttu-id="05f15-254">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="05f15-254">Seven digits</span></span> 
    
- <span data-ttu-id="05f15-255">Seleção de um dígito</span><span class="sxs-lookup"><span data-stu-id="05f15-255">One check digit</span></span>
    
- <span data-ttu-id="05f15-256">Um espaço ou a letra maiuscula "W" (com distinção entre maiusculas e minúsculas)</span><span class="sxs-lookup"><span data-stu-id="05f15-256">One space or the uppercase letter "W" (Case sensitive)</span></span>
    
<span data-ttu-id="05f15-257">Antes de 01 de janeiro de 2013:</span><span class="sxs-lookup"><span data-stu-id="05f15-257">Prior to 01 January 2013:</span></span>
  
-  <span data-ttu-id="05f15-258">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="05f15-258">Seven digits</span></span> 
    
- <span data-ttu-id="05f15-259">Seleção de um dígito</span><span class="sxs-lookup"><span data-stu-id="05f15-259">One check digit</span></span>
    
- <span data-ttu-id="05f15-260">Um espaço ou uma letra maiuscula (diferenciar maiusculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="05f15-260">One space or an uppercase letter (Case sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="05f15-261">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="05f15-261">Checksum</span></span>

<span data-ttu-id="05f15-262">Sim</span><span class="sxs-lookup"><span data-stu-id="05f15-262">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="05f15-263">Definição</span><span class="sxs-lookup"><span data-stu-id="05f15-263">Definition</span></span>

<span data-ttu-id="05f15-264">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="05f15-264">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="05f15-265">A função encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="05f15-265">The function finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="05f15-266">Uma palavra-chave da é encontrada.</span><span class="sxs-lookup"><span data-stu-id="05f15-266">A keyword from is found.</span></span>
    
<span data-ttu-id="05f15-267">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="05f15-267">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="05f15-268">A função encontra o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="05f15-268">The function finds content that matches the pattern.</span></span>
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_ireland_eu_national_id_card" />
          <Match idRef="Keywords_ireland_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_ireland_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="05f15-269">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="05f15-269">Keywords</span></span>

#### <a name="keywordsirelandeunationalidcard"></a><span data-ttu-id="05f15-270">Keywords_ireland_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="05f15-270">Keywords_ireland_eu_national_id_card</span></span>

<span data-ttu-id="05f15-271">número de serviço pessoal de público</span><span class="sxs-lookup"><span data-stu-id="05f15-271">personal public service number</span></span>
  
<span data-ttu-id="05f15-272">PPS nenhum</span><span class="sxs-lookup"><span data-stu-id="05f15-272">pps no</span></span>
  
<span data-ttu-id="05f15-273">número de seguro social e de receita</span><span class="sxs-lookup"><span data-stu-id="05f15-273">revenue and social insurance number</span></span>
  
<span data-ttu-id="05f15-274">rsi nenhum</span><span class="sxs-lookup"><span data-stu-id="05f15-274">rsi no</span></span>
  
<span data-ttu-id="05f15-275">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="05f15-275">personal identification number</span></span>
  
<span data-ttu-id="05f15-276">identification number
</span><span class="sxs-lookup"><span data-stu-id="05f15-276">identification number</span></span>
  
<span data-ttu-id="05f15-277">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="05f15-277">personal id number</span></span>
  
<span data-ttu-id="05f15-278">uimhir phearsanta seirbhíse poiblí</span><span class="sxs-lookup"><span data-stu-id="05f15-278">uimhir phearsanta seirbhíse poiblí</span></span>
  
<span data-ttu-id="05f15-p103">uimh. PSP</span><span class="sxs-lookup"><span data-stu-id="05f15-p103">uimh. psp</span></span>
  
## <a name="italy"></a><span data-ttu-id="05f15-281">Itália</span><span class="sxs-lookup"><span data-stu-id="05f15-281">Italy</span></span>

### <a name="format"></a><span data-ttu-id="05f15-282">Formato</span><span class="sxs-lookup"><span data-stu-id="05f15-282">Format</span></span>

<span data-ttu-id="05f15-283">Uma combinação de 16 caracteres de letras e dígitos no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="05f15-283">A 16-character combination of letters and digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="05f15-284">Padrão</span><span class="sxs-lookup"><span data-stu-id="05f15-284">Pattern</span></span>

<span data-ttu-id="05f15-285">Uma combinação de 16 caracteres de letras e dígitos:</span><span class="sxs-lookup"><span data-stu-id="05f15-285">A 16-character combination of letters and digits:</span></span>
  
- <span data-ttu-id="05f15-286">Três letras que correspondem às três primeiros consoantes no nome da família</span><span class="sxs-lookup"><span data-stu-id="05f15-286">Three letters that correspond to the first three consonants in the family name</span></span>
    
- <span data-ttu-id="05f15-287">Três letras que correspondem à primeira, terceira e quarta consoantes no primeiro nome de usuário</span><span class="sxs-lookup"><span data-stu-id="05f15-287">Three letters that correspond to the first, third, and fourth consonants in the first name</span></span>
    
- <span data-ttu-id="05f15-288">Dois dígitos que correspondem à última dígitos do ano nascimento</span><span class="sxs-lookup"><span data-stu-id="05f15-288">Two digits that correspond to the last digits of the birth year</span></span>
    
- <span data-ttu-id="05f15-289">Uma letra que corresponde à letra no mês de nascimento — letras são usadas em ordem alfabética, mas apenas as letras de a F, R, L, M, P, R para T são usadas (assim, janeiro é uma e outubro é R)</span><span class="sxs-lookup"><span data-stu-id="05f15-289">One letter that corresponds to the letter for the month of birth—letters are used in alphabetical order, but only the letters A to E, H, L, M, P, R to T are used (thus, January is A and October is R)</span></span>
    
- <span data-ttu-id="05f15-290">Dois dígitos que correspondem ao dia do mês de nascimento — para diferenciar entre sexos, 40 é adicionado ao dia de nascimento para feminino</span><span class="sxs-lookup"><span data-stu-id="05f15-290">Two digits that correspond to the day of the month of birth—in order to differentiate between genders, 40 is added to the day of birth for women</span></span>
    
- <span data-ttu-id="05f15-291">Quatro dígitos que corresponde ao código de área específico para o município onde a pessoa surgiu (códigos de país são usados para países estrangeiros)</span><span class="sxs-lookup"><span data-stu-id="05f15-291">Four digits that corresponds to the area code specific to the municipality where the person was born (country-wide codes are used for foreign countries)</span></span>
    
- <span data-ttu-id="05f15-292">Um dígito de paridade</span><span class="sxs-lookup"><span data-stu-id="05f15-292">One parity digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="05f15-293">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="05f15-293">Checksum</span></span>

<span data-ttu-id="05f15-294">Sim</span><span class="sxs-lookup"><span data-stu-id="05f15-294">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="05f15-295">Definição</span><span class="sxs-lookup"><span data-stu-id="05f15-295">Definition</span></span>

<span data-ttu-id="05f15-296">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="05f15-296">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="05f15-297">A função `Func_italy_eu_national_id_card` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="05f15-297">The function  `Func_italy_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="05f15-298">Uma palavra-chave da `Keywords_italy_eu_national_id_card` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="05f15-298">A keyword from  `Keywords_italy_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="05f15-299">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="05f15-299">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="05f15-300">A função `Func_italy_eu_national_id_card` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="05f15-300">The function  `Func_italy_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_italy_eu_national_id_card" />
          <Match idRef="Keywords_italy_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_italy_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="05f15-301">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="05f15-301">Keywords</span></span>

#### <a name="keywordsitalyeunationalidcard"></a><span data-ttu-id="05f15-302">Keywords_italy_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="05f15-302">Keywords_italy_eu_national_id_card</span></span>

<span data-ttu-id="05f15-303">código pessoal</span><span class="sxs-lookup"><span data-stu-id="05f15-303">personal code</span></span>
  
<span data-ttu-id="05f15-304">número de código pessoal</span><span class="sxs-lookup"><span data-stu-id="05f15-304">personal code number</span></span>
  
<span data-ttu-id="05f15-305">número de certificados pessoais</span><span class="sxs-lookup"><span data-stu-id="05f15-305">personal certificate number</span></span>
  
<span data-ttu-id="05f15-306">código fiscal</span><span class="sxs-lookup"><span data-stu-id="05f15-306">fiscal code</span></span>
  
<span data-ttu-id="05f15-307">personalcodeno #</span><span class="sxs-lookup"><span data-stu-id="05f15-307">personalcodeno#</span></span>
  
<span data-ttu-id="05f15-308">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="05f15-308">personal id number</span></span>
  
<span data-ttu-id="05f15-309">código de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="05f15-309">personal id code</span></span>
  
<span data-ttu-id="05f15-310">codice personale</span><span class="sxs-lookup"><span data-stu-id="05f15-310">codice personale</span></span>
  
<span data-ttu-id="05f15-311">numero certificato personale</span><span class="sxs-lookup"><span data-stu-id="05f15-311">numero certificato personale</span></span>
  
<span data-ttu-id="05f15-312">numero personale</span><span class="sxs-lookup"><span data-stu-id="05f15-312">numero personale</span></span>
  
<span data-ttu-id="05f15-313">numero id personale</span><span class="sxs-lookup"><span data-stu-id="05f15-313">numero id personale</span></span>
  
<span data-ttu-id="05f15-314">codice personale id</span><span class="sxs-lookup"><span data-stu-id="05f15-314">codice id personale</span></span>
  
<span data-ttu-id="05f15-315">codice fiscale</span><span class="sxs-lookup"><span data-stu-id="05f15-315">codice fiscale</span></span>
  
## <a name="italy"></a><span data-ttu-id="05f15-316">Itália</span><span class="sxs-lookup"><span data-stu-id="05f15-316">Italy</span></span>

### <a name="format"></a><span data-ttu-id="05f15-317">Formato</span><span class="sxs-lookup"><span data-stu-id="05f15-317">Format</span></span>

<span data-ttu-id="05f15-318">11 dígitos e um hífen no formato especificado</span><span class="sxs-lookup"><span data-stu-id="05f15-318">11 digits and a hyphen in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="05f15-319">Padrão</span><span class="sxs-lookup"><span data-stu-id="05f15-319">Pattern</span></span>

<span data-ttu-id="05f15-320">11 dígitos e um hífen:</span><span class="sxs-lookup"><span data-stu-id="05f15-320">11 digits and a hyphen:</span></span>
  
-  <span data-ttu-id="05f15-321">Seis dígitos que correspondem à data de nascimento (DDMMYY)</span><span class="sxs-lookup"><span data-stu-id="05f15-321">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="05f15-322">Um hífen</span><span class="sxs-lookup"><span data-stu-id="05f15-322">A hyphen</span></span>
    
- <span data-ttu-id="05f15-323">Um dígito que corresponde do century de nascimento ("0" para o décimo nono century, para 20 century "1" e "2" para century 21)</span><span class="sxs-lookup"><span data-stu-id="05f15-323">One digit that corresponds to the century of birth ("0" for 19th century, "1" for 20th century, and "2" for 21st century)</span></span>
    
- <span data-ttu-id="05f15-324">Quatro dígitos, gerados aleatoriamente</span><span class="sxs-lookup"><span data-stu-id="05f15-324">Four digits, randomly generated</span></span>
    
### <a name="checksum"></a><span data-ttu-id="05f15-325">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="05f15-325">Checksum</span></span>

<span data-ttu-id="05f15-326">Sim</span><span class="sxs-lookup"><span data-stu-id="05f15-326">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="05f15-327">Definição</span><span class="sxs-lookup"><span data-stu-id="05f15-327">Definition</span></span>

<span data-ttu-id="05f15-328">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="05f15-328">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="05f15-329">A função `Func_latvia_eu_national_id_card` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="05f15-329">The function  `Func_latvia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="05f15-330">Uma palavra-chave da `Keywords_latvia_eu_national_id_card` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="05f15-330">A keyword from  `Keywords_latvia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="05f15-331">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="05f15-331">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="05f15-332">A função `Func_latvia_eu_national_id_card` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="05f15-332">The function  `Func_latvia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_latvia_eu_national_id_card" />
          <Match idRef="Keywords_latvia_eu_national_id_card" />
        </Pattern>
 <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_latvia_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="05f15-333">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="05f15-333">Keywords</span></span>

#### <a name="keywordslatviaeunationalidcard"></a><span data-ttu-id="05f15-334">Keywords_latvia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="05f15-334">Keywords_latvia_eu_national_id_card</span></span>

<span data-ttu-id="05f15-335">código pessoal</span><span class="sxs-lookup"><span data-stu-id="05f15-335">personal code</span></span>
  
<span data-ttu-id="05f15-336">número de código pessoal</span><span class="sxs-lookup"><span data-stu-id="05f15-336">personal code number</span></span>
  
<span data-ttu-id="05f15-337">número de certificados pessoais</span><span class="sxs-lookup"><span data-stu-id="05f15-337">personal certificate number</span></span>
  
<span data-ttu-id="05f15-338">personalcodeno #</span><span class="sxs-lookup"><span data-stu-id="05f15-338">personalcodeno#</span></span>
  
<span data-ttu-id="05f15-339">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="05f15-339">personal id number</span></span>
  
<span data-ttu-id="05f15-340">código de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="05f15-340">personal id code</span></span>
  
<span data-ttu-id="05f15-341">kods personagens</span><span class="sxs-lookup"><span data-stu-id="05f15-341">personas kods</span></span>
  
## <a name="lithuania"></a><span data-ttu-id="05f15-342">Lituânia</span><span class="sxs-lookup"><span data-stu-id="05f15-342">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="05f15-343">Formato</span><span class="sxs-lookup"><span data-stu-id="05f15-343">Format</span></span>

<span data-ttu-id="05f15-344">11 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="05f15-344">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="05f15-345">Padrão</span><span class="sxs-lookup"><span data-stu-id="05f15-345">Pattern</span></span>

<span data-ttu-id="05f15-346">11 dígitos sem espaços e delimitadores:</span><span class="sxs-lookup"><span data-stu-id="05f15-346">11 digits without spaces and delimiters:</span></span>
  
- <span data-ttu-id="05f15-347">Um dígito que corresponde ao gênero da pessoa e o century de nascimento</span><span class="sxs-lookup"><span data-stu-id="05f15-347">One digit that corresponds to the person's gender and century of birth</span></span>
    
-  <span data-ttu-id="05f15-348">Seis dígitos que correspondem à data de nascimento (aammdd)</span><span class="sxs-lookup"><span data-stu-id="05f15-348">Six digits that correspond to birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="05f15-349">Três dígitos que correspondem ao número de série da data de nascimento</span><span class="sxs-lookup"><span data-stu-id="05f15-349">Three digits that correspond to the serial number of the date of birth</span></span>
    
- <span data-ttu-id="05f15-350">Seleção de um dígito</span><span class="sxs-lookup"><span data-stu-id="05f15-350">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="05f15-351">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="05f15-351">Checksum</span></span>

<span data-ttu-id="05f15-352">Sim</span><span class="sxs-lookup"><span data-stu-id="05f15-352">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="05f15-353">Definição</span><span class="sxs-lookup"><span data-stu-id="05f15-353">Definition</span></span>

<span data-ttu-id="05f15-354">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="05f15-354">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="05f15-355">A função `Func_lithuania_eu_national_id_card` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="05f15-355">The function  `Func_lithuania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="05f15-356">Uma palavra-chave da `Keywords_lithuania_eu_national_id_card` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="05f15-356">A keyword from  `Keywords_lithuania_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="05f15-357">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="05f15-357">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="05f15-358">A função `Func_lithuania_eu_national_id_card` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="05f15-358">The function  `Func_lithuania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_lithuania_eu_national_id_card" />
          <Match idRef="Keywords_lithuania_eu_national_id_card" />
        </Pattern> 
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_lithuania_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="05f15-359">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="05f15-359">Keywords</span></span>

#### <a name="keywordslithuaniaeunationalidcard"></a><span data-ttu-id="05f15-360">Keywords_lithuania_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="05f15-360">Keywords_lithuania_eu_national_id_card</span></span>

<span data-ttu-id="05f15-361">código numérico pessoal</span><span class="sxs-lookup"><span data-stu-id="05f15-361">personal numeric code</span></span>
  
<span data-ttu-id="05f15-362">número de identificação exclusivo</span><span class="sxs-lookup"><span data-stu-id="05f15-362">unique identification number</span></span>
  
<span data-ttu-id="05f15-363">número de serviços aos cidadãos</span><span class="sxs-lookup"><span data-stu-id="05f15-363">citizen service number</span></span>
  
<span data-ttu-id="05f15-364">número de identidade exclusiva</span><span class="sxs-lookup"><span data-stu-id="05f15-364">unique identity number</span></span>
  
<span data-ttu-id="05f15-365">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="05f15-365">uniqueidentityno#</span></span>
  
<span data-ttu-id="05f15-366">código de pessoal.</span><span class="sxs-lookup"><span data-stu-id="05f15-366">personal code.</span></span>
  
<span data-ttu-id="05f15-367">asmeninis skaitmeninis kodas</span><span class="sxs-lookup"><span data-stu-id="05f15-367">asmeninis skaitmeninis kodas</span></span>
  
<span data-ttu-id="05f15-368">unikalus identifikavimo numeris</span><span class="sxs-lookup"><span data-stu-id="05f15-368">unikalus identifikavimo numeris</span></span>
  
<span data-ttu-id="05f15-369">piliečio paslaugos numeris</span><span class="sxs-lookup"><span data-stu-id="05f15-369">piliečio paslaugos numeris</span></span>
  
<span data-ttu-id="05f15-370">unikalus identifikavimo kodas</span><span class="sxs-lookup"><span data-stu-id="05f15-370">unikalus identifikavimo kodas</span></span>
  
<span data-ttu-id="05f15-371">asmens kodas.</span><span class="sxs-lookup"><span data-stu-id="05f15-371">asmens kodas.</span></span>
  
## <a name="luxemburg"></a><span data-ttu-id="05f15-372">Luxemburgo</span><span class="sxs-lookup"><span data-stu-id="05f15-372">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="05f15-373">Formato</span><span class="sxs-lookup"><span data-stu-id="05f15-373">Format</span></span>

<span data-ttu-id="05f15-374">11 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="05f15-374">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="05f15-375">Padrão</span><span class="sxs-lookup"><span data-stu-id="05f15-375">Pattern</span></span>

<span data-ttu-id="05f15-376">11 dígitos</span><span class="sxs-lookup"><span data-stu-id="05f15-376">11 digits</span></span>
  
- <span data-ttu-id="05f15-377">Um dígito que corresponde ao gênero da pessoa e o century de nascimento</span><span class="sxs-lookup"><span data-stu-id="05f15-377">One digit that corresponds to the person's gender and century of birth</span></span>
    
-  <span data-ttu-id="05f15-378">Seis dígitos que correspondem à data de nascimento (aammdd)</span><span class="sxs-lookup"><span data-stu-id="05f15-378">Six digits that correspond to birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="05f15-379">Três dígitos que correspondem ao número de série da data de nascimento</span><span class="sxs-lookup"><span data-stu-id="05f15-379">Three digits that correspond to the serial number of the date of birth</span></span>
    
- <span data-ttu-id="05f15-380">Seleção de um dígito</span><span class="sxs-lookup"><span data-stu-id="05f15-380">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="05f15-381">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="05f15-381">Checksum</span></span>

<span data-ttu-id="05f15-382">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="05f15-382">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="05f15-383">Definição</span><span class="sxs-lookup"><span data-stu-id="05f15-383">Definition</span></span>

<span data-ttu-id="05f15-384">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="05f15-384">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="05f15-385">A expressão regular `Regex_luxemburg_eu_national_id_card` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="05f15-385">The regular expression  `Regex_luxemburg_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="05f15-386">Uma palavra-chave da `Keywords_luxemburg_eu_national_id_card` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="05f15-386">A keyword from  `Keywords_luxemburg_eu_national_id_card` is found.</span></span> 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_national_id_card" />
          <Match idRef="Keywords_luxemburg_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="05f15-387">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="05f15-387">Keywords</span></span>

#### <a name="keywordsluxemburgeunationalidcard"></a><span data-ttu-id="05f15-388">Keywords_luxemburg_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="05f15-388">Keywords_luxemburg_eu_national_id_card</span></span>

<span data-ttu-id="05f15-389">identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="05f15-389">personal id</span></span>
  
<span data-ttu-id="05f15-390">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="05f15-390">personal id number</span></span>
  
<span data-ttu-id="05f15-391">personalidno #</span><span class="sxs-lookup"><span data-stu-id="05f15-391">personalidno#</span></span>
  
<span data-ttu-id="05f15-392">número de identificação exclusiva</span><span class="sxs-lookup"><span data-stu-id="05f15-392">unique id number</span></span>
  
<span data-ttu-id="05f15-393">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="05f15-393">personalidnumber#</span></span>
  
<span data-ttu-id="05f15-394">chave de identificação exclusiva</span><span class="sxs-lookup"><span data-stu-id="05f15-394">unique id key</span></span>
  
<span data-ttu-id="05f15-395">código de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="05f15-395">personal id code</span></span>
  
<span data-ttu-id="05f15-396">uniqueidkey #</span><span class="sxs-lookup"><span data-stu-id="05f15-396">uniqueidkey#</span></span>
  
<span data-ttu-id="05f15-397">código individual</span><span class="sxs-lookup"><span data-stu-id="05f15-397">individual code</span></span>
  
<span data-ttu-id="05f15-398">id individual</span><span class="sxs-lookup"><span data-stu-id="05f15-398">individual id</span></span>
  
<span data-ttu-id="05f15-399">id de eindeutige-nummer</span><span class="sxs-lookup"><span data-stu-id="05f15-399">eindeutige id-nummer</span></span>
  
<span data-ttu-id="05f15-400">id de eindeutige</span><span class="sxs-lookup"><span data-stu-id="05f15-400">eindeutige id</span></span>
  
<span data-ttu-id="05f15-401">ID personnelle</span><span class="sxs-lookup"><span data-stu-id="05f15-401">id personnelle</span></span>
  
<span data-ttu-id="05f15-402">numéro d'identification pessoal</span><span class="sxs-lookup"><span data-stu-id="05f15-402">numéro d'identification personnel</span></span>
  
<span data-ttu-id="05f15-403">idpersonnelle #</span><span class="sxs-lookup"><span data-stu-id="05f15-403">idpersonnelle#</span></span>
  
<span data-ttu-id="05f15-404">persönliche identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="05f15-404">persönliche identifikationsnummer</span></span>
  
<span data-ttu-id="05f15-405">eindeutigeid #</span><span class="sxs-lookup"><span data-stu-id="05f15-405">eindeutigeid#</span></span>
  
## <a name="malta"></a><span data-ttu-id="05f15-406">Malta</span><span class="sxs-lookup"><span data-stu-id="05f15-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="05f15-407">Formato</span><span class="sxs-lookup"><span data-stu-id="05f15-407">Format</span></span>

<span data-ttu-id="05f15-408">Sete dígitos, seguidos por uma letra</span><span class="sxs-lookup"><span data-stu-id="05f15-408">Seven digits followed by one letter</span></span>
  
### <a name="pattern"></a><span data-ttu-id="05f15-409">Padrão</span><span class="sxs-lookup"><span data-stu-id="05f15-409">Pattern</span></span>

<span data-ttu-id="05f15-410">Sete dígitos seguidos por uma letra:</span><span class="sxs-lookup"><span data-stu-id="05f15-410">Seven digits followed by one letter:</span></span>
  
-  <span data-ttu-id="05f15-411">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="05f15-411">Seven digits</span></span> 
    
- <span data-ttu-id="05f15-412">Uma letra maiuscula (com distinção entre maiusculas e minúsculas)</span><span class="sxs-lookup"><span data-stu-id="05f15-412">One uppercase letter (case sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="05f15-413">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="05f15-413">Checksum</span></span>

<span data-ttu-id="05f15-414">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="05f15-414">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="05f15-415">Definição</span><span class="sxs-lookup"><span data-stu-id="05f15-415">Definition</span></span>

<span data-ttu-id="05f15-416">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="05f15-416">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="05f15-417">A expressão regular `Regex_malta_eu_national_id_card` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="05f15-417">The regular expression  `Regex_malta_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="05f15-418">Uma palavra-chave da `Keywords_malta_eu_national_id_card` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="05f15-418">A keyword from  `Keywords_malta_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="05f15-419">Uma política de DLP tem 65% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="05f15-419">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="05f15-420">A expressão regular `Regex_malta_eu_national_id_card` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="05f15-420">The regular expression  `Regex_malta_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_national_id_card" />
          <Match idRef="Keywords_malta_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_malta_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="05f15-421">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="05f15-421">Keywords</span></span>

#### <a name="keywordsmaltaeunationalidcard"></a><span data-ttu-id="05f15-422">Keywords_malta_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="05f15-422">Keywords_malta_eu_national_id_card</span></span>

<span data-ttu-id="05f15-423">código numérico pessoal</span><span class="sxs-lookup"><span data-stu-id="05f15-423">personal numeric code</span></span>
  
<span data-ttu-id="05f15-424">número de identificação exclusivo</span><span class="sxs-lookup"><span data-stu-id="05f15-424">unique identification number</span></span>
  
<span data-ttu-id="05f15-425">número de serviços aos cidadãos</span><span class="sxs-lookup"><span data-stu-id="05f15-425">citizen service number</span></span>
  
<span data-ttu-id="05f15-426">número de identidade exclusiva</span><span class="sxs-lookup"><span data-stu-id="05f15-426">unique identity number</span></span>
  
<span data-ttu-id="05f15-427">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="05f15-427">uniqueidentityno#</span></span>
  
<span data-ttu-id="05f15-428">kodiċi numerali personali</span><span class="sxs-lookup"><span data-stu-id="05f15-428">kodiċi numerali personali</span></span>
  
<span data-ttu-id="05f15-429">numru guias ' identifikazzjoni uniku</span><span class="sxs-lookup"><span data-stu-id="05f15-429">numru ta 'identifikazzjoni uniku</span></span>
  
<span data-ttu-id="05f15-430">numru servizz de tarefa taċ-ċittadin</span><span class="sxs-lookup"><span data-stu-id="05f15-430">numru tas-servizz taċ-ċittadin</span></span>
  
<span data-ttu-id="05f15-431">numru guias ' identità uniku</span><span class="sxs-lookup"><span data-stu-id="05f15-431">numru ta' identità uniku</span></span>
  
## <a name="netherlands"></a><span data-ttu-id="05f15-432">Países Baixos</span><span class="sxs-lookup"><span data-stu-id="05f15-432">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="05f15-433">Formato</span><span class="sxs-lookup"><span data-stu-id="05f15-433">Format</span></span>

<span data-ttu-id="05f15-434">Nove dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="05f15-434">Nine digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="05f15-435">Padrão</span><span class="sxs-lookup"><span data-stu-id="05f15-435">Pattern</span></span>

<span data-ttu-id="05f15-436">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="05f15-436">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="05f15-437">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="05f15-437">Checksum</span></span>

<span data-ttu-id="05f15-438">Sim</span><span class="sxs-lookup"><span data-stu-id="05f15-438">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="05f15-439">Definição</span><span class="sxs-lookup"><span data-stu-id="05f15-439">Definition</span></span>

<span data-ttu-id="05f15-440">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="05f15-440">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="05f15-441">A função `Func_netherlands_eu_national_id_card` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="05f15-441">The function  `Func_netherlands_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="05f15-442">Uma palavra-chave da é encontrada.</span><span class="sxs-lookup"><span data-stu-id="05f15-442">A keyword from is found.</span></span>
    
<span data-ttu-id="05f15-443">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="05f15-443">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="05f15-444">A função `Func_netherlands_eu_national_id_card` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="05f15-444">The function  `Func_netherlands_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_netherlands_eu_national_id_card" />
          <Match idRef="Keywords_netherlands_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_netherlands_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="05f15-445">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="05f15-445">Keywords</span></span>

#### <a name="keywordsnetherlandseunationalidcard"></a><span data-ttu-id="05f15-446">Keywords_netherlands_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="05f15-446">Keywords_netherlands_eu_national_id_card</span></span>

<span data-ttu-id="05f15-447">código numérico pessoal</span><span class="sxs-lookup"><span data-stu-id="05f15-447">personal numeric code</span></span>
  
<span data-ttu-id="05f15-448">número de identificação exclusivo</span><span class="sxs-lookup"><span data-stu-id="05f15-448">unique identification number</span></span>
  
<span data-ttu-id="05f15-449">número de serviços aos cidadãos</span><span class="sxs-lookup"><span data-stu-id="05f15-449">citizen service number</span></span>
  
<span data-ttu-id="05f15-450">número de identidade exclusiva</span><span class="sxs-lookup"><span data-stu-id="05f15-450">unique identity number</span></span>
  
<span data-ttu-id="05f15-451">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="05f15-451">uniqueidentityno#</span></span>
  
<span data-ttu-id="05f15-452">bsn</span><span class="sxs-lookup"><span data-stu-id="05f15-452">bsn</span></span>
  
<span data-ttu-id="05f15-453">bsn #</span><span class="sxs-lookup"><span data-stu-id="05f15-453">bsn#</span></span>
  
<span data-ttu-id="05f15-454">código de numerieke persoonlijke</span><span class="sxs-lookup"><span data-stu-id="05f15-454">persoonlijke numerieke code</span></span>
  
<span data-ttu-id="05f15-455">uniek identificatienummer</span><span class="sxs-lookup"><span data-stu-id="05f15-455">uniek identificatienummer</span></span>
  
<span data-ttu-id="05f15-456">burgerservicenummer</span><span class="sxs-lookup"><span data-stu-id="05f15-456">burgerservicenummer</span></span>
  
<span data-ttu-id="05f15-457">uniek identiteitsnummer</span><span class="sxs-lookup"><span data-stu-id="05f15-457">uniek identiteitsnummer</span></span>
  
## <a name="poland"></a><span data-ttu-id="05f15-458">Polônia</span><span class="sxs-lookup"><span data-stu-id="05f15-458">Poland</span></span>

<span data-ttu-id="05f15-459">Para obter detalhes, consulte a seção "Polônia nacional ID (PESEL)" em [quais tipos de informações confidenciais a procurar](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="05f15-459">For details, see the section "Poland National ID (PESEL)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="05f15-460">Portugal</span><span class="sxs-lookup"><span data-stu-id="05f15-460">Portugal</span></span>

<span data-ttu-id="05f15-461">Para obter detalhes, consulte a seção "Número de cartão de cidadãos Portugal" nos [quais os tipos de informações confidenciais procurar](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="05f15-461">For details, see the section "Portugal Citizen Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="romania"></a><span data-ttu-id="05f15-462">Romênia</span><span class="sxs-lookup"><span data-stu-id="05f15-462">Romania</span></span>

### <a name="format"></a><span data-ttu-id="05f15-463">Formato</span><span class="sxs-lookup"><span data-stu-id="05f15-463">Format</span></span>

<span data-ttu-id="05f15-464">13 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="05f15-464">13 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="05f15-465">Padrão</span><span class="sxs-lookup"><span data-stu-id="05f15-465">Pattern</span></span>

<span data-ttu-id="05f15-466">13 dígitos</span><span class="sxs-lookup"><span data-stu-id="05f15-466">13 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="05f15-467">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="05f15-467">Checksum</span></span>

<span data-ttu-id="05f15-468">Sim</span><span class="sxs-lookup"><span data-stu-id="05f15-468">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="05f15-469">Definição</span><span class="sxs-lookup"><span data-stu-id="05f15-469">Definition</span></span>

<span data-ttu-id="05f15-470">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="05f15-470">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="05f15-471">A função `Func_romania_eu_national_id_card` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="05f15-471">The function  `Func_romania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="05f15-472">Uma palavra-chave da `Keywords_romania_eu_national_id_card` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="05f15-472">A keyword from  `Keywords_romania_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="05f15-473">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="05f15-473">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="05f15-474">A função `Func_romania_eu_national_id_card` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="05f15-474">The function  `Func_romania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_romania_eu_national_id_card" />
          <Match idRef="Keywords_romania_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_romania_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="05f15-475">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="05f15-475">Keywords</span></span>

#### <a name="keywordsromaniaeunationalidcard"></a><span data-ttu-id="05f15-476">Keywords_romania_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="05f15-476">Keywords_romania_eu_national_id_card</span></span>

<span data-ttu-id="05f15-477">código numérico pessoal</span><span class="sxs-lookup"><span data-stu-id="05f15-477">personal numeric code</span></span>
  
<span data-ttu-id="05f15-478">número de identificação exclusivo</span><span class="sxs-lookup"><span data-stu-id="05f15-478">unique identification number</span></span>
  
<span data-ttu-id="05f15-479">cnp</span><span class="sxs-lookup"><span data-stu-id="05f15-479">cnp</span></span>
  
<span data-ttu-id="05f15-480">cnp #</span><span class="sxs-lookup"><span data-stu-id="05f15-480">cnp#</span></span>
  
<span data-ttu-id="05f15-481">fixar</span><span class="sxs-lookup"><span data-stu-id="05f15-481">pin</span></span>
  
<span data-ttu-id="05f15-482">PIN #</span><span class="sxs-lookup"><span data-stu-id="05f15-482">pin#</span></span>
  
<span data-ttu-id="05f15-483">número do seguro</span><span class="sxs-lookup"><span data-stu-id="05f15-483">insurance number</span></span>
  
<span data-ttu-id="05f15-484">insurancenumber #</span><span class="sxs-lookup"><span data-stu-id="05f15-484">insurancenumber#</span></span>
  
<span data-ttu-id="05f15-485">número de identidade exclusiva</span><span class="sxs-lookup"><span data-stu-id="05f15-485">unique identity number</span></span>
  
<span data-ttu-id="05f15-486">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="05f15-486">uniqueidentityno#</span></span>
  
<span data-ttu-id="05f15-487">pessoal de COD numéricos</span><span class="sxs-lookup"><span data-stu-id="05f15-487">cod numeric personal</span></span>
  
<span data-ttu-id="05f15-488">bacalhau identificare pessoal</span><span class="sxs-lookup"><span data-stu-id="05f15-488">cod identificare personal</span></span>
  
<span data-ttu-id="05f15-489">COD UNIX identificare</span><span class="sxs-lookup"><span data-stu-id="05f15-489">cod unic identificare</span></span>
  
<span data-ttu-id="05f15-490">număr UNIX de pessoal</span><span class="sxs-lookup"><span data-stu-id="05f15-490">număr personal unic</span></span>
  
<span data-ttu-id="05f15-491">număr identitate</span><span class="sxs-lookup"><span data-stu-id="05f15-491">număr identitate</span></span>
  
<span data-ttu-id="05f15-492">număr identificare pessoal</span><span class="sxs-lookup"><span data-stu-id="05f15-492">număr identificare personal</span></span>
  
<span data-ttu-id="05f15-493">număridentitate #</span><span class="sxs-lookup"><span data-stu-id="05f15-493">număridentitate#</span></span>
  
<span data-ttu-id="05f15-494">codnumericpersonal #</span><span class="sxs-lookup"><span data-stu-id="05f15-494">codnumericpersonal#</span></span>
  
<span data-ttu-id="05f15-495">numărpersonalunic #</span><span class="sxs-lookup"><span data-stu-id="05f15-495">numărpersonalunic#</span></span>
  
## <a name="slovakia"></a><span data-ttu-id="05f15-496">Eslováquia</span><span class="sxs-lookup"><span data-stu-id="05f15-496">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="05f15-497">Formato</span><span class="sxs-lookup"><span data-stu-id="05f15-497">Format</span></span>

<span data-ttu-id="05f15-498">Dez dígitos que contém a barra um invertida</span><span class="sxs-lookup"><span data-stu-id="05f15-498">Ten digits containing one backslash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="05f15-499">Padrão</span><span class="sxs-lookup"><span data-stu-id="05f15-499">Pattern</span></span>

<span data-ttu-id="05f15-500">Dez dígitos que contém a barra um invertida:</span><span class="sxs-lookup"><span data-stu-id="05f15-500">Ten digits containing one backslash:</span></span>
  
### <a name="checksum"></a><span data-ttu-id="05f15-501">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="05f15-501">Checksum</span></span>

<span data-ttu-id="05f15-502">Sim</span><span class="sxs-lookup"><span data-stu-id="05f15-502">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="05f15-503">Definição</span><span class="sxs-lookup"><span data-stu-id="05f15-503">Definition</span></span>

<span data-ttu-id="05f15-504">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="05f15-504">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="05f15-505">A função `Func_slovakia_eu_national_id_card` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="05f15-505">The function  `Func_slovakia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="05f15-506">Uma palavra-chave da `Keywords_slovakia_eu_national_id_card` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="05f15-506">A keyword from  `Keywords_slovakia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="05f15-507">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="05f15-507">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="05f15-508">A função `Func_slovakia_eu_national_id_card` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="05f15-508">The function  `Func_slovakia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_slovakia_eu_national_id_card" />
          <Match idRef="Keywords_slovakia_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_slovakia_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="05f15-509">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="05f15-509">Keywords</span></span>

#### <a name="keywordsslovakiaeunationalidcard"></a><span data-ttu-id="05f15-510">Keywords_slovakia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="05f15-510">Keywords_slovakia_eu_national_id_card</span></span>

<span data-ttu-id="05f15-511">número de nascimento</span><span class="sxs-lookup"><span data-stu-id="05f15-511">birth number</span></span>
  
<span data-ttu-id="05f15-512">número de identificação nacional</span><span class="sxs-lookup"><span data-stu-id="05f15-512">national identification number</span></span>
  
<span data-ttu-id="05f15-513">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="05f15-513">personal identification number</span></span>
  
<span data-ttu-id="05f15-514">social security number
</span><span class="sxs-lookup"><span data-stu-id="05f15-514">social security number</span></span>
  
<span data-ttu-id="05f15-515">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="05f15-515">nationalnumber#</span></span>
  
<span data-ttu-id="05f15-516">SSN #</span><span class="sxs-lookup"><span data-stu-id="05f15-516">ssn#</span></span>
  
<span data-ttu-id="05f15-517">SSN</span><span class="sxs-lookup"><span data-stu-id="05f15-517">ssn</span></span>
  
<span data-ttu-id="05f15-518">número nacional</span><span class="sxs-lookup"><span data-stu-id="05f15-518">national number</span></span>
  
<span data-ttu-id="05f15-519">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="05f15-519">personal id number</span></span>
  
<span data-ttu-id="05f15-520">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="05f15-520">personalidnumber#</span></span>
  
<span data-ttu-id="05f15-521">rč</span><span class="sxs-lookup"><span data-stu-id="05f15-521">rč</span></span>
  
<span data-ttu-id="05f15-522">rodné číslo</span><span class="sxs-lookup"><span data-stu-id="05f15-522">rodné číslo</span></span>
  
<span data-ttu-id="05f15-523">rodne cislo</span><span class="sxs-lookup"><span data-stu-id="05f15-523">rodne cislo</span></span>
  
## <a name="slovenia"></a><span data-ttu-id="05f15-524">Eslovênia</span><span class="sxs-lookup"><span data-stu-id="05f15-524">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="05f15-525">Formato</span><span class="sxs-lookup"><span data-stu-id="05f15-525">Format</span></span>

<span data-ttu-id="05f15-526">13 dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="05f15-526">13 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="05f15-527">Padrão</span><span class="sxs-lookup"><span data-stu-id="05f15-527">Pattern</span></span>

<span data-ttu-id="05f15-528">13 dígitos no padrão especificado:</span><span class="sxs-lookup"><span data-stu-id="05f15-528">13 digits in the specified pattern:</span></span>
  
-  <span data-ttu-id="05f15-529">Sete dígitos que correspondem à data de nascimento (DDMMLLL) onde "LLL" corresponde aos últimos três dígitos do ano nascimento</span><span class="sxs-lookup"><span data-stu-id="05f15-529">Seven digits that correspond to the birth date (DDMMLLL) where "LLL" corresponds to the last three digits of the birth year</span></span> 
    
- <span data-ttu-id="05f15-530">Dois dígitos que correspondem à área de nascimento</span><span class="sxs-lookup"><span data-stu-id="05f15-530">Two digits that correspond to the area of birth</span></span>
    
- <span data-ttu-id="05f15-531">Três dígitos que correspondem a uma combinação de gênero e número de série para as pessoas nascidas no mesmo dia (000-499 para Masculino) e 500 e 999 para fêmea</span><span class="sxs-lookup"><span data-stu-id="05f15-531">Three digits that correspond to a combination of gender and serial number for persons born on the same day (000-499 for male and 500-999 for female)</span></span>
    
- <span data-ttu-id="05f15-532">Seleção de um dígito</span><span class="sxs-lookup"><span data-stu-id="05f15-532">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="05f15-533">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="05f15-533">Checksum</span></span>

<span data-ttu-id="05f15-534">Sim</span><span class="sxs-lookup"><span data-stu-id="05f15-534">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="05f15-535">Definição</span><span class="sxs-lookup"><span data-stu-id="05f15-535">Definition</span></span>

<span data-ttu-id="05f15-536">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="05f15-536">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="05f15-537">A função `Func_slovenia_eu_national_id_card` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="05f15-537">The function  `Func_slovenia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="05f15-538">Uma palavra-chave da `Keywords_slovenia_eu_national_id_card` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="05f15-538">A keyword from  `Keywords_slovenia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="05f15-539">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="05f15-539">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="05f15-540">A função `Func_slovenia_eu_national_id_card` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="05f15-540">The function  `Func_slovenia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_slovenia_eu_national_id_card" />
          <Match idRef="Keywords_slovenia_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_slovenia_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="05f15-541">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="05f15-541">Keywords</span></span>

#### <a name="keywordssloveniaeunationalidcard"></a><span data-ttu-id="05f15-542">Keywords_slovenia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="05f15-542">Keywords_slovenia_eu_national_id_card</span></span>

<span data-ttu-id="05f15-543">código numérico pessoal</span><span class="sxs-lookup"><span data-stu-id="05f15-543">personal numeric code</span></span>
  
<span data-ttu-id="05f15-544">número de identificação exclusivo</span><span class="sxs-lookup"><span data-stu-id="05f15-544">unique identification number</span></span>
  
<span data-ttu-id="05f15-545">número exclusivo de registro</span><span class="sxs-lookup"><span data-stu-id="05f15-545">unique registration number</span></span>
  
<span data-ttu-id="05f15-546">número de identidade exclusiva</span><span class="sxs-lookup"><span data-stu-id="05f15-546">unique identity number</span></span>
  
<span data-ttu-id="05f15-547">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="05f15-547">uniqueidentityno#</span></span>
  
<span data-ttu-id="05f15-548">número exclusivo cidadãos mestre</span><span class="sxs-lookup"><span data-stu-id="05f15-548">unique master citizen number</span></span>
  
<span data-ttu-id="05f15-549">edinstvena identifikacijska številka</span><span class="sxs-lookup"><span data-stu-id="05f15-549">edinstvena identifikacijska številka</span></span>
  
<span data-ttu-id="05f15-550">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="05f15-550">uniqueidentityno #</span></span>
  
<span data-ttu-id="05f15-551">edinstvena številka glavnega državljana</span><span class="sxs-lookup"><span data-stu-id="05f15-551">edinstvena številka glavnega državljana</span></span>
  
<span data-ttu-id="05f15-552">emšo</span><span class="sxs-lookup"><span data-stu-id="05f15-552">emšo</span></span>
  
## <a name="spain"></a><span data-ttu-id="05f15-553">Espanha</span><span class="sxs-lookup"><span data-stu-id="05f15-553">Spain</span></span>

### <a name="format"></a><span data-ttu-id="05f15-554">Formato</span><span class="sxs-lookup"><span data-stu-id="05f15-554">Format</span></span>

<span data-ttu-id="05f15-555">Sete dígitos seguidos por um caractere</span><span class="sxs-lookup"><span data-stu-id="05f15-555">Seven digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="05f15-556">Padrão</span><span class="sxs-lookup"><span data-stu-id="05f15-556">Pattern</span></span>

<span data-ttu-id="05f15-557">Sete dígitos seguidos por um caractere</span><span class="sxs-lookup"><span data-stu-id="05f15-557">Seven digits followed by one character</span></span>
  
- <span data-ttu-id="05f15-558">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="05f15-558">Seven digits</span></span>
    
- <span data-ttu-id="05f15-559">Um dígito ou carta (não diferencia maiusculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="05f15-559">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="05f15-560">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="05f15-560">Checksum</span></span>

<span data-ttu-id="05f15-561">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="05f15-561">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="05f15-562">Definição</span><span class="sxs-lookup"><span data-stu-id="05f15-562">Definition</span></span>

<span data-ttu-id="05f15-563">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="05f15-563">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="05f15-564">A expressão regular `Regex_spain_eu_national_id_card` encontra conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="05f15-564">The regular expression  `Regex_spain_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="05f15-565">Uma palavra-chave da `Keywords_spain_eu_national_id_card"` for encontrado.</span><span class="sxs-lookup"><span data-stu-id="05f15-565">A keyword from  `Keywords_spain_eu_national_id_card"` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_national_id_card" />
          <Match idRef="Keywords_spain_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="05f15-566">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="05f15-566">Keywords</span></span>

#### <a name="keywordsspaineunationalidcard"></a><span data-ttu-id="05f15-567">Keywords_spain_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="05f15-567">Keywords_spain_eu_national_id_card</span></span>

<span data-ttu-id="05f15-568">dni</span><span class="sxs-lookup"><span data-stu-id="05f15-568">dni</span></span>
  
<span data-ttu-id="05f15-569">número de identificação nacional</span><span class="sxs-lookup"><span data-stu-id="05f15-569">national identification number</span></span>
  
<span data-ttu-id="05f15-570">número de identidade nacional</span><span class="sxs-lookup"><span data-stu-id="05f15-570">national identity number</span></span>
  
<span data-ttu-id="05f15-571">número do seguro</span><span class="sxs-lookup"><span data-stu-id="05f15-571">insurance number</span></span>
  
<span data-ttu-id="05f15-572">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="05f15-572">personal identification number</span></span>
  
<span data-ttu-id="05f15-573">identidade nacional</span><span class="sxs-lookup"><span data-stu-id="05f15-573">national identity</span></span>
  
<span data-ttu-id="05f15-574">identidade pessoal sem</span><span class="sxs-lookup"><span data-stu-id="05f15-574">personal identity no</span></span>
  
<span data-ttu-id="05f15-575">número de identidade exclusiva</span><span class="sxs-lookup"><span data-stu-id="05f15-575">unique identity number</span></span>
  
<span data-ttu-id="05f15-576">nationalidno #</span><span class="sxs-lookup"><span data-stu-id="05f15-576">nationalidno#</span></span>
  
<span data-ttu-id="05f15-577">UniqueID #</span><span class="sxs-lookup"><span data-stu-id="05f15-577">uniqueid#</span></span>
  
<span data-ttu-id="05f15-578">dni #</span><span class="sxs-lookup"><span data-stu-id="05f15-578">dni#</span></span>
  
<span data-ttu-id="05f15-579">nationalid #</span><span class="sxs-lookup"><span data-stu-id="05f15-579">nationalid#</span></span>
  
<span data-ttu-id="05f15-580">NIE #</span><span class="sxs-lookup"><span data-stu-id="05f15-580">nie#</span></span>
  
<span data-ttu-id="05f15-581">NIE</span><span class="sxs-lookup"><span data-stu-id="05f15-581">nie</span></span>
  
<span data-ttu-id="05f15-582">nienúmero #</span><span class="sxs-lookup"><span data-stu-id="05f15-582">nienúmero#</span></span>
  
<span data-ttu-id="05f15-583">número de NIE</span><span class="sxs-lookup"><span data-stu-id="05f15-583">nie número</span></span>
  
<span data-ttu-id="05f15-584">documento nacional de identidad</span><span class="sxs-lookup"><span data-stu-id="05f15-584">documento nacional de identidad</span></span>
  
<span data-ttu-id="05f15-585">identidad único</span><span class="sxs-lookup"><span data-stu-id="05f15-585">identidad único</span></span>
  
<span data-ttu-id="05f15-586">número nacional identidad</span><span class="sxs-lookup"><span data-stu-id="05f15-586">número nacional identidad</span></span>
  
<span data-ttu-id="05f15-587">número de dni</span><span class="sxs-lookup"><span data-stu-id="05f15-587">dni número</span></span>
  
<span data-ttu-id="05f15-588">dninúmero #</span><span class="sxs-lookup"><span data-stu-id="05f15-588">dninúmero#</span></span>
  
<span data-ttu-id="05f15-589">identidadúnico #</span><span class="sxs-lookup"><span data-stu-id="05f15-589">identidadúnico#</span></span>
  
## <a name="sweden"></a><span data-ttu-id="05f15-590">Suécia</span><span class="sxs-lookup"><span data-stu-id="05f15-590">Sweden</span></span>

<span data-ttu-id="05f15-591">Para obter detalhes, consulte a seção "ID nacional da Suécia" nos [quais os tipos de informações confidenciais procurar](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="05f15-591">For details, see the section "Sweden National ID" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="05f15-592">Confira também</span><span class="sxs-lookup"><span data-stu-id="05f15-592">See also</span></span>

[<span data-ttu-id="05f15-593">O que os tipos de informações confidenciais procuram</span><span class="sxs-lookup"><span data-stu-id="05f15-593">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)


---
title: Número de identificação nacional da UE
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: Este tópico mostra o que uma política de prevenção de perda de dados (DLP) procura quando detecta o tipo de informação confidencial do número de identificação nacional da UE. Esse tipo de informação confidencial define diferentes padrões, palavras-chave e outras evidências para cada país.
ms.openlocfilehash: afae2c3fa54fe5fcd93990cdf5797f5517c46202
ms.sourcegitcommit: ed822a776d3419853453583e882f3c61ca26d4b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2019
ms.locfileid: "30410966"
---
# <a name="eu-national-identification-number"></a><span data-ttu-id="46643-104">Número de identificação nacional da UE</span><span class="sxs-lookup"><span data-stu-id="46643-104">EU National Identification Number</span></span>

<span data-ttu-id="46643-105">Este tópico mostra o que uma política de prevenção de perda de dados (DLP) procura quando detecta o tipo de informação confidencial do número de identificação nacional da UE.</span><span class="sxs-lookup"><span data-stu-id="46643-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU National Identification Number sensitive information type.</span></span> <span data-ttu-id="46643-106">Esse tipo de informação confidencial define diferentes padrões, palavras-chave e outras evidências para cada país.</span><span class="sxs-lookup"><span data-stu-id="46643-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="46643-107">Áustria </span><span class="sxs-lookup"><span data-stu-id="46643-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="46643-108">Format</span><span class="sxs-lookup"><span data-stu-id="46643-108">Format</span></span>

<span data-ttu-id="46643-109">Uma combinação de 24 caracteres de letras, dígitos e caracteres especiais</span><span class="sxs-lookup"><span data-stu-id="46643-109">A 24-character combination of letters, digits, and special characters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="46643-110">Padrão</span><span class="sxs-lookup"><span data-stu-id="46643-110">Pattern</span></span>

<span data-ttu-id="46643-111">24 caracteres:</span><span class="sxs-lookup"><span data-stu-id="46643-111">24 characters:</span></span>
  
-  <span data-ttu-id="46643-112">22 letras (não diferencia maiúsculas de minúsculas), dígitos, barras invertidas, barras encaminhadas ou sinais de adição</span><span class="sxs-lookup"><span data-stu-id="46643-112">22 letters (not case-sensitive), digits, backslashes, forward slashes, or plus signs</span></span> 
    
- <span data-ttu-id="46643-113">Duas letras (não diferencia maiúsculas de minúsculas), dígitos, barras invertidas, barras invertidas, sinais de adição ou sinais de igual</span><span class="sxs-lookup"><span data-stu-id="46643-113">Two letters (not case-sensitive), digits, backslashes, forward slashes, plus signs, or equal signs</span></span>
    
### <a name="checksum"></a><span data-ttu-id="46643-114">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="46643-114">Checksum</span></span>

<span data-ttu-id="46643-115">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="46643-115">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="46643-116">Definição</span><span class="sxs-lookup"><span data-stu-id="46643-116">Definition</span></span>

<span data-ttu-id="46643-117">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="46643-117">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46643-118">A expressão `Regex_austria_eu_national_id_card` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="46643-118">The regular expression  `Regex_austria_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46643-119">Uma palavra- `Keywords_austria_eu_national_id_card` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="46643-119">A keyword from  `Keywords_austria_eu_national_id_card` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_national_id_card" />
          <Match idRef="Keywords_austria_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="46643-120">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="46643-120">Keywords</span></span>

#### <a name="keywordsaustriaeunationalidcard"></a><span data-ttu-id="46643-121">Keywords_austria_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="46643-121">Keywords_austria_eu_national_id_card</span></span>

<span data-ttu-id="46643-122">número de identidade austríaca</span><span class="sxs-lookup"><span data-stu-id="46643-122">austrian identity number</span></span>
  
<span data-ttu-id="46643-123">número de identidade nacional</span><span class="sxs-lookup"><span data-stu-id="46643-123">national identity number</span></span>
  
<span data-ttu-id="46643-124">número de identidade</span><span class="sxs-lookup"><span data-stu-id="46643-124">identity number</span></span>
  
<span data-ttu-id="46643-125">national id</span><span class="sxs-lookup"><span data-stu-id="46643-125">national id</span></span>
  
<span data-ttu-id="46643-126">Personalausweis REPUBLIK ÖSTERREICH</span><span class="sxs-lookup"><span data-stu-id="46643-126">personalausweis republik österreich</span></span>
  
## <a name="belgium"></a><span data-ttu-id="46643-127">Bélgica </span><span class="sxs-lookup"><span data-stu-id="46643-127">Belgium</span></span>

<span data-ttu-id="46643-128">Para obter detalhes, consulte a seção "número nacional da Bélgica" em o [que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="46643-128">For details, see the section "Belgium National Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="bulgaria"></a><span data-ttu-id="46643-129">Bulgária</span><span class="sxs-lookup"><span data-stu-id="46643-129">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="46643-130">Format</span><span class="sxs-lookup"><span data-stu-id="46643-130">Format</span></span>

<span data-ttu-id="46643-131">Dez dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="46643-131">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="46643-132">Padrão</span><span class="sxs-lookup"><span data-stu-id="46643-132">Pattern</span></span>

<span data-ttu-id="46643-133">Dez dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="46643-133">Ten digits without spaces and delimiters</span></span>
  
-  <span data-ttu-id="46643-134">Seis dígitos que correspondem à data de nascimento (AAMMDD)</span><span class="sxs-lookup"><span data-stu-id="46643-134">Six digits that correspond to the birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="46643-135">Dois dígitos que correspondem à ordem de nascimento</span><span class="sxs-lookup"><span data-stu-id="46643-135">Two digits that correspond to the birth order</span></span>
    
- <span data-ttu-id="46643-136">Um dígito que corresponde ao gênero: um dígito par para macho e um dígito estranho para o fêmea</span><span class="sxs-lookup"><span data-stu-id="46643-136">One digit that corresponds to gender: An even digit for male and an odd digit for female</span></span>
    
- <span data-ttu-id="46643-137">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="46643-137">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="46643-138">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="46643-138">Checksum</span></span>

<span data-ttu-id="46643-139">Sim</span><span class="sxs-lookup"><span data-stu-id="46643-139">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="46643-140">Definição</span><span class="sxs-lookup"><span data-stu-id="46643-140">Definition</span></span>

<span data-ttu-id="46643-141">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="46643-141">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46643-142">A função `Func_bulgaria_national_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="46643-142">The function  `Func_bulgaria_national_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46643-143">Uma palavra- `Keywords_bulgaria_national_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="46643-143">A keyword from  `Keywords_bulgaria_national_number` is found.</span></span> 
    
<span data-ttu-id="46643-144">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="46643-144">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46643-145">A função `Func_bulgaria_national_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="46643-145">The function  `Func_bulgaria_national_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="46643-146">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="46643-146">Keywords</span></span>

#### <a name="keywordsbulgarianationalnumber"></a><span data-ttu-id="46643-147">Keywords_bulgaria_national_number</span><span class="sxs-lookup"><span data-stu-id="46643-147">Keywords_bulgaria_national_number</span></span>

<span data-ttu-id="46643-148">Egn</span><span class="sxs-lookup"><span data-stu-id="46643-148">egn</span></span>
  
<span data-ttu-id="46643-149">Egn #</span><span class="sxs-lookup"><span data-stu-id="46643-149">egn#</span></span>
  
<span data-ttu-id="46643-150">número nacional búlgaro</span><span class="sxs-lookup"><span data-stu-id="46643-150">bulgarian national number</span></span>
  
<span data-ttu-id="46643-151">número nacional</span><span class="sxs-lookup"><span data-stu-id="46643-151">national number</span></span>
  
<span data-ttu-id="46643-152">social security number</span><span class="sxs-lookup"><span data-stu-id="46643-152">social security number</span></span>
  
<span data-ttu-id="46643-153">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="46643-153">nationalnumber#</span></span>
  
<span data-ttu-id="46643-154">es</span><span class="sxs-lookup"><span data-stu-id="46643-154">ssn#</span></span>
  
<span data-ttu-id="46643-155">es</span><span class="sxs-lookup"><span data-stu-id="46643-155">ssn</span></span>
  
<span data-ttu-id="46643-156">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="46643-156">nationalnumber</span></span>
  
<span data-ttu-id="46643-157">BNN #</span><span class="sxs-lookup"><span data-stu-id="46643-157">bnn#</span></span>
  
<span data-ttu-id="46643-158">BNN</span><span class="sxs-lookup"><span data-stu-id="46643-158">bnn</span></span>
  
<span data-ttu-id="46643-159">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="46643-159">personal id number</span></span>
  
<span data-ttu-id="46643-160">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="46643-160">personalidnumber#</span></span>
  
<span data-ttu-id="46643-161">единен граждански номер</span><span class="sxs-lookup"><span data-stu-id="46643-161">единен граждански номер</span></span>
  
<span data-ttu-id="46643-162">edinen grazhdanski de nome</span><span class="sxs-lookup"><span data-stu-id="46643-162">edinen grazhdanski nomer</span></span>
  
<span data-ttu-id="46643-163">егн</span><span class="sxs-lookup"><span data-stu-id="46643-163">егн</span></span>
  
<span data-ttu-id="46643-164">егн #</span><span class="sxs-lookup"><span data-stu-id="46643-164">егн#</span></span>
  
## <a name="croatia"></a><span data-ttu-id="46643-165">Croácia</span><span class="sxs-lookup"><span data-stu-id="46643-165">Croatia</span></span>

<span data-ttu-id="46643-166">Para obter detalhes, consulte a seção "número de identidade da Croácia" em o [que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="46643-166">For details, see the section "Croatia Identity Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="cyprus"></a><span data-ttu-id="46643-167">Chipre</span><span class="sxs-lookup"><span data-stu-id="46643-167">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="46643-168">Format</span><span class="sxs-lookup"><span data-stu-id="46643-168">Format</span></span>

<span data-ttu-id="46643-169">Dez dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="46643-169">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="46643-170">Padrão</span><span class="sxs-lookup"><span data-stu-id="46643-170">Pattern</span></span>

 <span data-ttu-id="46643-171">Dez dígitos</span><span class="sxs-lookup"><span data-stu-id="46643-171">Ten digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="46643-172">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="46643-172">Checksum</span></span>

<span data-ttu-id="46643-173">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="46643-173">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="46643-174">Definição</span><span class="sxs-lookup"><span data-stu-id="46643-174">Definition</span></span>

<span data-ttu-id="46643-175">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="46643-175">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46643-176">A expressão `Regex_cyprus_eu_national_id_card` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="46643-176">The regular expression  `Regex_cyprus_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46643-177">Uma palavra- `Keywords_cyprus_eu_national_id_card` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="46643-177">A keyword from  `Keywords_cyprus_eu_national_id_card` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_national_id_card" />
          <Match idRef="Keywords_cyprus_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="46643-178">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="46643-178">Keywords</span></span>

#### <a name="keywordscypruseunationalidcard"></a><span data-ttu-id="46643-179">Keywords_cyprus_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="46643-179">Keywords_cyprus_eu_national_id_card</span></span>

<span data-ttu-id="46643-180">número do cartão de identificação</span><span class="sxs-lookup"><span data-stu-id="46643-180">id card number</span></span>
  
<span data-ttu-id="46643-181">national identification number</span><span class="sxs-lookup"><span data-stu-id="46643-181">national identification number</span></span>
  
<span data-ttu-id="46643-182">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="46643-182">personal id number</span></span>
  
<span data-ttu-id="46643-183">número do cartão de identidade</span><span class="sxs-lookup"><span data-stu-id="46643-183">identity card number</span></span>
  
<span data-ttu-id="46643-184">ταυτοτητασ</span><span class="sxs-lookup"><span data-stu-id="46643-184">ταυτοτητασ</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="46643-185">República Tcheca</span><span class="sxs-lookup"><span data-stu-id="46643-185">Czech Republic</span></span>

<span data-ttu-id="46643-186">Para obter detalhes, consulte a seção "número de identidade nacional tcheco" em [que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="46643-186">For details, see the section "Czech National Identity Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="denmark"></a><span data-ttu-id="46643-187">Dinamarca</span><span class="sxs-lookup"><span data-stu-id="46643-187">Denmark</span></span>

<span data-ttu-id="46643-188">Para obter detalhes, consulte a seção "Dinamarca Personal Identification Number" em o [que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="46643-188">For details, see the section "Denmark Personal Identification Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="estonia"></a><span data-ttu-id="46643-189">Estônia</span><span class="sxs-lookup"><span data-stu-id="46643-189">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="46643-190">Format</span><span class="sxs-lookup"><span data-stu-id="46643-190">Format</span></span>

<span data-ttu-id="46643-191">11 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="46643-191">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="46643-192">Padrão</span><span class="sxs-lookup"><span data-stu-id="46643-192">Pattern</span></span>

<span data-ttu-id="46643-193">11 dígitos:</span><span class="sxs-lookup"><span data-stu-id="46643-193">11 digits:</span></span>
  
- <span data-ttu-id="46643-194">Um dígito que corresponde ao sexo e ao século de nascimento (número ímpar masculino, mesmo número fêmea; 1-2:19 Century; 3-4:20 Century; 5-6:21 século)</span><span class="sxs-lookup"><span data-stu-id="46643-194">One digit that corresponds to sex and century of birth (odd number male, even number female; 1-2: 19th century; 3-4: 20th century; 5-6: 21st century)</span></span>
    
- <span data-ttu-id="46643-195">Seis dígitos que correspondem à data de nascimento (AAMMDD)</span><span class="sxs-lookup"><span data-stu-id="46643-195">Six digits that correspond to date of birth (YYMMDD)</span></span>
    
- <span data-ttu-id="46643-196">Três dígitos que correspondem a um número de série separando as pessoas que nasceu na mesma data</span><span class="sxs-lookup"><span data-stu-id="46643-196">Three digits that correspond to a serial number separating persons born on the same date</span></span>
    
- <span data-ttu-id="46643-197">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="46643-197">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="46643-198">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="46643-198">Checksum</span></span>

<span data-ttu-id="46643-199">Sim</span><span class="sxs-lookup"><span data-stu-id="46643-199">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="46643-200">Definição</span><span class="sxs-lookup"><span data-stu-id="46643-200">Definition</span></span>

<span data-ttu-id="46643-201">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="46643-201">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46643-202">A função `Func_estonia_eu_national_id_card` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="46643-202">The function  `Func_estonia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46643-203">Uma palavra- `Keywords_estonia_eu_national_id_card` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="46643-203">A keyword from  `Keywords_estonia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="46643-204">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="46643-204">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46643-205">A função `Func_estonia_eu_national_id_card` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="46643-205">The function  `Func_estonia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="46643-206">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="46643-206">Keywords</span></span>

#### <a name="keywordsestoniaeunationalidcard"></a><span data-ttu-id="46643-207">Keywords_estonia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="46643-207">Keywords_estonia_eu_national_id_card</span></span>

<span data-ttu-id="46643-208">código de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="46643-208">personal identification code</span></span>
  
<span data-ttu-id="46643-209">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="46643-209">personal identification number</span></span>
  
<span data-ttu-id="46643-210">national identification number</span><span class="sxs-lookup"><span data-stu-id="46643-210">national identification number</span></span>
  
<span data-ttu-id="46643-211">número nacional</span><span class="sxs-lookup"><span data-stu-id="46643-211">national number</span></span>
  
<span data-ttu-id="46643-212">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="46643-212">personal id number</span></span>
  
<span data-ttu-id="46643-213">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="46643-213">personalidnumber#</span></span>
  
<span data-ttu-id="46643-214">IKMover</span><span class="sxs-lookup"><span data-stu-id="46643-214">ik</span></span>
  
<span data-ttu-id="46643-215">isikukood</span><span class="sxs-lookup"><span data-stu-id="46643-215">isikukood</span></span>
  
<span data-ttu-id="46643-216">ID-kaart</span><span class="sxs-lookup"><span data-stu-id="46643-216">id-kaart</span></span>
  
## <a name="finland"></a><span data-ttu-id="46643-217">Finlândia</span><span class="sxs-lookup"><span data-stu-id="46643-217">Finland</span></span>

<span data-ttu-id="46643-218">Para obter detalhes, consulte a seção "ID nacional da Finlândia" em o [que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="46643-218">For details, see the section "Finland National ID" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="46643-219">França</span><span class="sxs-lookup"><span data-stu-id="46643-219">France</span></span>

<span data-ttu-id="46643-220">Para obter detalhes, consulte a seção "CNI (cartão de ID nacional da França)" em [que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="46643-220">For details, see the section "France National ID Card (CNI)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="46643-221">Alemanha</span><span class="sxs-lookup"><span data-stu-id="46643-221">Germany</span></span>

<span data-ttu-id="46643-222">Para obter detalhes, consulte a seção "número do cartão de identidade da Alemanha" em [o que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="46643-222">For details, see the section "Germany Identity Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="46643-223">Grécia</span><span class="sxs-lookup"><span data-stu-id="46643-223">Greece</span></span>

<span data-ttu-id="46643-224">Para obter detalhes, consulte a seção "cartão de ID nacional da Grécia" em [que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="46643-224">For details, see the section "Greece National ID Card" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="hungary"></a><span data-ttu-id="46643-225">Hungria</span><span class="sxs-lookup"><span data-stu-id="46643-225">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="46643-226">Format</span><span class="sxs-lookup"><span data-stu-id="46643-226">Format</span></span>

<span data-ttu-id="46643-227">11 dígitos</span><span class="sxs-lookup"><span data-stu-id="46643-227">11 digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="46643-228">Padrão</span><span class="sxs-lookup"><span data-stu-id="46643-228">Pattern</span></span>

<span data-ttu-id="46643-229">11 dígitos:</span><span class="sxs-lookup"><span data-stu-id="46643-229">11 digits:</span></span>
  
-  <span data-ttu-id="46643-230">Um dígito que corresponde ao gênero (1-macho, 2-fêmea, outros números também são possíveis para o cidadãos nasceu antes 1900 ou cidadãos com cidadania dupla)</span><span class="sxs-lookup"><span data-stu-id="46643-230">One digit that corresponds to gender (1-male, 2-female, other numbers are also possible for citizens born before 1900 or citizens with double citizenship)</span></span> 
    
- <span data-ttu-id="46643-231">Seis dígitos que correspondem à data de nascimento (AAMMDD)</span><span class="sxs-lookup"><span data-stu-id="46643-231">Six digits that correspond to birth date (YYMMDD)</span></span>
    
- <span data-ttu-id="46643-232">Três dígitos que correspondem a um número de série</span><span class="sxs-lookup"><span data-stu-id="46643-232">Three digits that correspond to a serial number</span></span>
    
- <span data-ttu-id="46643-233">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="46643-233">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="46643-234">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="46643-234">Checksum</span></span>

<span data-ttu-id="46643-235">Sim</span><span class="sxs-lookup"><span data-stu-id="46643-235">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="46643-236">Definição</span><span class="sxs-lookup"><span data-stu-id="46643-236">Definition</span></span>

<span data-ttu-id="46643-237">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="46643-237">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46643-238">A função `Func_hungary_eu_national_id_card` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="46643-238">The function  `Func_hungary_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46643-239">Uma palavra- `Keywords_hungary_eu_national_id_card` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="46643-239">A keyword from  `Keywords_hungary_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="46643-240">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="46643-240">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46643-241">A função `Func_hungary_eu_national_id_card` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="46643-241">The function  `Func_hungary_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="46643-242">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="46643-242">Keywords</span></span>

#### <a name="keywordshungaryeunationalidcard"></a><span data-ttu-id="46643-243">Keywords_hungary_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="46643-243">Keywords_hungary_eu_national_id_card</span></span>

<span data-ttu-id="46643-244">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="46643-244">personal identification number</span></span>
  
<span data-ttu-id="46643-245">identification number</span><span class="sxs-lookup"><span data-stu-id="46643-245">identification number</span></span>
  
<span data-ttu-id="46643-246">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="46643-246">personal id number</span></span>
  
<span data-ttu-id="46643-247">személyazonosító igazolvány</span><span class="sxs-lookup"><span data-stu-id="46643-247">személyazonosító igazolvány</span></span>
  
## <a name="ireland"></a><span data-ttu-id="46643-248">Irlanda</span><span class="sxs-lookup"><span data-stu-id="46643-248">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="46643-249">Format</span><span class="sxs-lookup"><span data-stu-id="46643-249">Format</span></span>

<span data-ttu-id="46643-250">Uma combinação de letras, dígitos e um espaço no padrão especificado de nove caracteres</span><span class="sxs-lookup"><span data-stu-id="46643-250">A nine-character combination of letters, digits, and a space in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="46643-251">Padrão</span><span class="sxs-lookup"><span data-stu-id="46643-251">Pattern</span></span>

<span data-ttu-id="46643-252">Uma combinação de letras, dígitos e um espaço no padrão especificado de nove caracteres</span><span class="sxs-lookup"><span data-stu-id="46643-252">A nine-character combination of letters, digits, and a space in the specified pattern</span></span>
  
<span data-ttu-id="46643-253">De 1º de janeiro de 2013 até agora:</span><span class="sxs-lookup"><span data-stu-id="46643-253">From 01 January 2013 to now:</span></span>
  
-  <span data-ttu-id="46643-254">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="46643-254">Seven digits</span></span> 
    
- <span data-ttu-id="46643-255">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="46643-255">One check digit</span></span>
    
- <span data-ttu-id="46643-256">Um espaço ou a letra maiúscula "W" (diferencia maiúscula de minúscula)</span><span class="sxs-lookup"><span data-stu-id="46643-256">One space or the uppercase letter "W" (Case sensitive)</span></span>
    
<span data-ttu-id="46643-257">Antes de 1º de janeiro de 2013:</span><span class="sxs-lookup"><span data-stu-id="46643-257">Prior to 01 January 2013:</span></span>
  
-  <span data-ttu-id="46643-258">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="46643-258">Seven digits</span></span> 
    
- <span data-ttu-id="46643-259">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="46643-259">One check digit</span></span>
    
- <span data-ttu-id="46643-260">Um espaço ou uma letra maiúscula (diferencia maiúscula de minúscula)</span><span class="sxs-lookup"><span data-stu-id="46643-260">One space or an uppercase letter (Case sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="46643-261">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="46643-261">Checksum</span></span>

<span data-ttu-id="46643-262">Sim</span><span class="sxs-lookup"><span data-stu-id="46643-262">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="46643-263">Definição</span><span class="sxs-lookup"><span data-stu-id="46643-263">Definition</span></span>

<span data-ttu-id="46643-264">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="46643-264">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46643-265">A função localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="46643-265">The function finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="46643-266">Uma palavra-chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="46643-266">A keyword from is found.</span></span>
    
<span data-ttu-id="46643-267">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="46643-267">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46643-268">A função localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="46643-268">The function finds content that matches the pattern.</span></span>
    
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

### <a name="keywords"></a><span data-ttu-id="46643-269">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="46643-269">Keywords</span></span>

#### <a name="keywordsirelandeunationalidcard"></a><span data-ttu-id="46643-270">Keywords_ireland_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="46643-270">Keywords_ireland_eu_national_id_card</span></span>

<span data-ttu-id="46643-271">número de serviço público pessoal</span><span class="sxs-lookup"><span data-stu-id="46643-271">personal public service number</span></span>
  
<span data-ttu-id="46643-272">PPS não</span><span class="sxs-lookup"><span data-stu-id="46643-272">pps no</span></span>
  
<span data-ttu-id="46643-273">número da receita e do seguro social</span><span class="sxs-lookup"><span data-stu-id="46643-273">revenue and social insurance number</span></span>
  
<span data-ttu-id="46643-274">RSI não</span><span class="sxs-lookup"><span data-stu-id="46643-274">rsi no</span></span>
  
<span data-ttu-id="46643-275">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="46643-275">personal identification number</span></span>
  
<span data-ttu-id="46643-276">identification number</span><span class="sxs-lookup"><span data-stu-id="46643-276">identification number</span></span>
  
<span data-ttu-id="46643-277">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="46643-277">personal id number</span></span>
  
<span data-ttu-id="46643-278">uimhir phearsanta seirbhíse poiblí</span><span class="sxs-lookup"><span data-stu-id="46643-278">uimhir phearsanta seirbhíse poiblí</span></span>
  
<span data-ttu-id="46643-279">uimh.</span><span class="sxs-lookup"><span data-stu-id="46643-279">uimh.</span></span> <span data-ttu-id="46643-280">PSP</span><span class="sxs-lookup"><span data-stu-id="46643-280">psp</span></span>
  
## <a name="italy"></a><span data-ttu-id="46643-281">Itália</span><span class="sxs-lookup"><span data-stu-id="46643-281">Italy</span></span>

### <a name="format"></a><span data-ttu-id="46643-282">Format</span><span class="sxs-lookup"><span data-stu-id="46643-282">Format</span></span>

<span data-ttu-id="46643-283">Uma combinação de 16 caracteres de letras e dígitos no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="46643-283">A 16-character combination of letters and digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="46643-284">Padrão</span><span class="sxs-lookup"><span data-stu-id="46643-284">Pattern</span></span>

<span data-ttu-id="46643-285">Uma combinação de letras e dígitos de 16 caracteres:</span><span class="sxs-lookup"><span data-stu-id="46643-285">A 16-character combination of letters and digits:</span></span>
  
- <span data-ttu-id="46643-286">Três letras que correspondem às três primeiras consoantes no nome da família</span><span class="sxs-lookup"><span data-stu-id="46643-286">Three letters that correspond to the first three consonants in the family name</span></span>
    
- <span data-ttu-id="46643-287">Três letras que correspondem à primeira, terceira e quarta consoantes no primeiro nome</span><span class="sxs-lookup"><span data-stu-id="46643-287">Three letters that correspond to the first, third, and fourth consonants in the first name</span></span>
    
- <span data-ttu-id="46643-288">Dois dígitos que correspondem aos últimos dígitos do ano de nascimento</span><span class="sxs-lookup"><span data-stu-id="46643-288">Two digits that correspond to the last digits of the birth year</span></span>
    
- <span data-ttu-id="46643-289">Uma letra que corresponde à carta para o mês de nascimento-as letras são usadas em ordem alfabética, mas apenas as letras de a a E, H, L, M, P, R a T são usadas (dessa forma, Janeiro é A e outubro é R)</span><span class="sxs-lookup"><span data-stu-id="46643-289">One letter that corresponds to the letter for the month of birth—letters are used in alphabetical order, but only the letters A to E, H, L, M, P, R to T are used (thus, January is A and October is R)</span></span>
    
- <span data-ttu-id="46643-290">Dois dígitos que correspondem ao dia do mês de nascimento — para diferenciar entre sexos, 40 é adicionado ao dia de nascimento para mulheres</span><span class="sxs-lookup"><span data-stu-id="46643-290">Two digits that correspond to the day of the month of birth—in order to differentiate between genders, 40 is added to the day of birth for women</span></span>
    
- <span data-ttu-id="46643-291">Quatro dígitos que correspondem ao código de área específico do município onde a pessoa nasceu (códigos de todo o país são usados para países estrangeiros)</span><span class="sxs-lookup"><span data-stu-id="46643-291">Four digits that corresponds to the area code specific to the municipality where the person was born (country-wide codes are used for foreign countries)</span></span>
    
- <span data-ttu-id="46643-292">Um dígito de paridade</span><span class="sxs-lookup"><span data-stu-id="46643-292">One parity digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="46643-293">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="46643-293">Checksum</span></span>

<span data-ttu-id="46643-294">Sim</span><span class="sxs-lookup"><span data-stu-id="46643-294">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="46643-295">Definição</span><span class="sxs-lookup"><span data-stu-id="46643-295">Definition</span></span>

<span data-ttu-id="46643-296">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="46643-296">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46643-297">A função `Func_italy_eu_national_id_card` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="46643-297">The function  `Func_italy_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46643-298">Uma palavra- `Keywords_italy_eu_national_id_card` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="46643-298">A keyword from  `Keywords_italy_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="46643-299">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="46643-299">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46643-300">A função `Func_italy_eu_national_id_card` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="46643-300">The function  `Func_italy_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="46643-301">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="46643-301">Keywords</span></span>

#### <a name="keywordsitalyeunationalidcard"></a><span data-ttu-id="46643-302">Keywords_italy_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="46643-302">Keywords_italy_eu_national_id_card</span></span>

<span data-ttu-id="46643-303">código pessoal</span><span class="sxs-lookup"><span data-stu-id="46643-303">personal code</span></span>
  
<span data-ttu-id="46643-304">número de código pessoal</span><span class="sxs-lookup"><span data-stu-id="46643-304">personal code number</span></span>
  
<span data-ttu-id="46643-305">número do certificado pessoal</span><span class="sxs-lookup"><span data-stu-id="46643-305">personal certificate number</span></span>
  
<span data-ttu-id="46643-306">código fiscal</span><span class="sxs-lookup"><span data-stu-id="46643-306">fiscal code</span></span>
  
<span data-ttu-id="46643-307">personalcodeno #</span><span class="sxs-lookup"><span data-stu-id="46643-307">personalcodeno#</span></span>
  
<span data-ttu-id="46643-308">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="46643-308">personal id number</span></span>
  
<span data-ttu-id="46643-309">código de ID pessoal</span><span class="sxs-lookup"><span data-stu-id="46643-309">personal id code</span></span>
  
<span data-ttu-id="46643-310">pessoal do Codice</span><span class="sxs-lookup"><span data-stu-id="46643-310">codice personale</span></span>
  
<span data-ttu-id="46643-311">numero certificato pessoal</span><span class="sxs-lookup"><span data-stu-id="46643-311">numero certificato personale</span></span>
  
<span data-ttu-id="46643-312">pessoal do numero</span><span class="sxs-lookup"><span data-stu-id="46643-312">numero personale</span></span>
  
<span data-ttu-id="46643-313">pessoal da ID numero</span><span class="sxs-lookup"><span data-stu-id="46643-313">numero id personale</span></span>
  
<span data-ttu-id="46643-314">pessoal da ID codice</span><span class="sxs-lookup"><span data-stu-id="46643-314">codice id personale</span></span>
  
<span data-ttu-id="46643-315">fiscalização codice</span><span class="sxs-lookup"><span data-stu-id="46643-315">codice fiscale</span></span>
  
## <a name="italy"></a><span data-ttu-id="46643-316">Itália</span><span class="sxs-lookup"><span data-stu-id="46643-316">Italy</span></span>

### <a name="format"></a><span data-ttu-id="46643-317">Format</span><span class="sxs-lookup"><span data-stu-id="46643-317">Format</span></span>

<span data-ttu-id="46643-318">11 dígitos e um hífen no formato especificado</span><span class="sxs-lookup"><span data-stu-id="46643-318">11 digits and a hyphen in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="46643-319">Padrão</span><span class="sxs-lookup"><span data-stu-id="46643-319">Pattern</span></span>

<span data-ttu-id="46643-320">11 dígitos e um hífen:</span><span class="sxs-lookup"><span data-stu-id="46643-320">11 digits and a hyphen:</span></span>
  
-  <span data-ttu-id="46643-321">Seis dígitos que correspondem à data de nascimento (DDMMAA)</span><span class="sxs-lookup"><span data-stu-id="46643-321">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="46643-322">Um hífen</span><span class="sxs-lookup"><span data-stu-id="46643-322">A hyphen</span></span>
    
- <span data-ttu-id="46643-323">Um dígito que corresponde ao século de nascimento ("0" para o século 19, "1" para o século 20 e "2" para o século 21)</span><span class="sxs-lookup"><span data-stu-id="46643-323">One digit that corresponds to the century of birth ("0" for 19th century, "1" for 20th century, and "2" for 21st century)</span></span>
    
- <span data-ttu-id="46643-324">Quatro dígitos, gerados aleatoriamente</span><span class="sxs-lookup"><span data-stu-id="46643-324">Four digits, randomly generated</span></span>
    
### <a name="checksum"></a><span data-ttu-id="46643-325">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="46643-325">Checksum</span></span>

<span data-ttu-id="46643-326">Sim</span><span class="sxs-lookup"><span data-stu-id="46643-326">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="46643-327">Definição</span><span class="sxs-lookup"><span data-stu-id="46643-327">Definition</span></span>

<span data-ttu-id="46643-328">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="46643-328">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46643-329">A função `Func_latvia_eu_national_id_card` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="46643-329">The function  `Func_latvia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46643-330">Uma palavra- `Keywords_latvia_eu_national_id_card` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="46643-330">A keyword from  `Keywords_latvia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="46643-331">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="46643-331">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46643-332">A função `Func_latvia_eu_national_id_card` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="46643-332">The function  `Func_latvia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="46643-333">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="46643-333">Keywords</span></span>

#### <a name="keywordslatviaeunationalidcard"></a><span data-ttu-id="46643-334">Keywords_latvia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="46643-334">Keywords_latvia_eu_national_id_card</span></span>

<span data-ttu-id="46643-335">código pessoal</span><span class="sxs-lookup"><span data-stu-id="46643-335">personal code</span></span>
  
<span data-ttu-id="46643-336">número de código pessoal</span><span class="sxs-lookup"><span data-stu-id="46643-336">personal code number</span></span>
  
<span data-ttu-id="46643-337">número do certificado pessoal</span><span class="sxs-lookup"><span data-stu-id="46643-337">personal certificate number</span></span>
  
<span data-ttu-id="46643-338">personalcodeno #</span><span class="sxs-lookup"><span data-stu-id="46643-338">personalcodeno#</span></span>
  
<span data-ttu-id="46643-339">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="46643-339">personal id number</span></span>
  
<span data-ttu-id="46643-340">código de ID pessoal</span><span class="sxs-lookup"><span data-stu-id="46643-340">personal id code</span></span>
  
<span data-ttu-id="46643-341">Kods personas</span><span class="sxs-lookup"><span data-stu-id="46643-341">personas kods</span></span>
  
## <a name="lithuania"></a><span data-ttu-id="46643-342">Lituânia</span><span class="sxs-lookup"><span data-stu-id="46643-342">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="46643-343">Format</span><span class="sxs-lookup"><span data-stu-id="46643-343">Format</span></span>

<span data-ttu-id="46643-344">11 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="46643-344">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="46643-345">Padrão</span><span class="sxs-lookup"><span data-stu-id="46643-345">Pattern</span></span>

<span data-ttu-id="46643-346">11 dígitos sem espaços e delimitadores:</span><span class="sxs-lookup"><span data-stu-id="46643-346">11 digits without spaces and delimiters:</span></span>
  
- <span data-ttu-id="46643-347">Um dígito que corresponde ao sexo da pessoa e ao século de nascimento</span><span class="sxs-lookup"><span data-stu-id="46643-347">One digit that corresponds to the person's gender and century of birth</span></span>
    
-  <span data-ttu-id="46643-348">Seis dígitos que correspondem à data de nascimento (AAMMDD)</span><span class="sxs-lookup"><span data-stu-id="46643-348">Six digits that correspond to birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="46643-349">Três dígitos que correspondem ao número de série da data de nascimento</span><span class="sxs-lookup"><span data-stu-id="46643-349">Three digits that correspond to the serial number of the date of birth</span></span>
    
- <span data-ttu-id="46643-350">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="46643-350">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="46643-351">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="46643-351">Checksum</span></span>

<span data-ttu-id="46643-352">Sim</span><span class="sxs-lookup"><span data-stu-id="46643-352">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="46643-353">Definição</span><span class="sxs-lookup"><span data-stu-id="46643-353">Definition</span></span>

<span data-ttu-id="46643-354">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="46643-354">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46643-355">A função `Func_lithuania_eu_national_id_card` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="46643-355">The function  `Func_lithuania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46643-356">Uma palavra- `Keywords_lithuania_eu_national_id_card` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="46643-356">A keyword from  `Keywords_lithuania_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="46643-357">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="46643-357">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46643-358">A função `Func_lithuania_eu_national_id_card` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="46643-358">The function  `Func_lithuania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="46643-359">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="46643-359">Keywords</span></span>

#### <a name="keywordslithuaniaeunationalidcard"></a><span data-ttu-id="46643-360">Keywords_lithuania_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="46643-360">Keywords_lithuania_eu_national_id_card</span></span>

<span data-ttu-id="46643-361">código numérico pessoal</span><span class="sxs-lookup"><span data-stu-id="46643-361">personal numeric code</span></span>
  
<span data-ttu-id="46643-362">número de identificação exclusivo</span><span class="sxs-lookup"><span data-stu-id="46643-362">unique identification number</span></span>
  
<span data-ttu-id="46643-363">número do serviço do cidadão</span><span class="sxs-lookup"><span data-stu-id="46643-363">citizen service number</span></span>
  
<span data-ttu-id="46643-364">número de identidade exclusivo</span><span class="sxs-lookup"><span data-stu-id="46643-364">unique identity number</span></span>
  
<span data-ttu-id="46643-365">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="46643-365">uniqueidentityno#</span></span>
  
<span data-ttu-id="46643-366">código pessoal.</span><span class="sxs-lookup"><span data-stu-id="46643-366">personal code.</span></span>
  
<span data-ttu-id="46643-367">asmeninis skaitmeninis kodas</span><span class="sxs-lookup"><span data-stu-id="46643-367">asmeninis skaitmeninis kodas</span></span>
  
<span data-ttu-id="46643-368">unikalus identifikavimo Numeris</span><span class="sxs-lookup"><span data-stu-id="46643-368">unikalus identifikavimo numeris</span></span>
  
<span data-ttu-id="46643-369">piliečio paslaugos Numeris</span><span class="sxs-lookup"><span data-stu-id="46643-369">piliečio paslaugos numeris</span></span>
  
<span data-ttu-id="46643-370">unikalus identifikavimo kodas</span><span class="sxs-lookup"><span data-stu-id="46643-370">unikalus identifikavimo kodas</span></span>
  
<span data-ttu-id="46643-371">kodas.</span><span class="sxs-lookup"><span data-stu-id="46643-371">asmens kodas.</span></span>
  
## <a name="luxemburg"></a><span data-ttu-id="46643-372">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="46643-372">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="46643-373">Format</span><span class="sxs-lookup"><span data-stu-id="46643-373">Format</span></span>

<span data-ttu-id="46643-374">11 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="46643-374">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="46643-375">Padrão</span><span class="sxs-lookup"><span data-stu-id="46643-375">Pattern</span></span>

<span data-ttu-id="46643-376">11 dígitos</span><span class="sxs-lookup"><span data-stu-id="46643-376">11 digits</span></span>
  
- <span data-ttu-id="46643-377">Um dígito que corresponde ao sexo da pessoa e ao século de nascimento</span><span class="sxs-lookup"><span data-stu-id="46643-377">One digit that corresponds to the person's gender and century of birth</span></span>
    
-  <span data-ttu-id="46643-378">Seis dígitos que correspondem à data de nascimento (AAMMDD)</span><span class="sxs-lookup"><span data-stu-id="46643-378">Six digits that correspond to birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="46643-379">Três dígitos que correspondem ao número de série da data de nascimento</span><span class="sxs-lookup"><span data-stu-id="46643-379">Three digits that correspond to the serial number of the date of birth</span></span>
    
- <span data-ttu-id="46643-380">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="46643-380">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="46643-381">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="46643-381">Checksum</span></span>

<span data-ttu-id="46643-382">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="46643-382">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="46643-383">Definição</span><span class="sxs-lookup"><span data-stu-id="46643-383">Definition</span></span>

<span data-ttu-id="46643-384">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="46643-384">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46643-385">A expressão `Regex_luxemburg_eu_national_id_card` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="46643-385">The regular expression  `Regex_luxemburg_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46643-386">Uma palavra- `Keywords_luxemburg_eu_national_id_card` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="46643-386">A keyword from  `Keywords_luxemburg_eu_national_id_card` is found.</span></span> 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_national_id_card" />
          <Match idRef="Keywords_luxemburg_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="46643-387">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="46643-387">Keywords</span></span>

#### <a name="keywordsluxemburgeunationalidcard"></a><span data-ttu-id="46643-388">Keywords_luxemburg_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="46643-388">Keywords_luxemburg_eu_national_id_card</span></span>

<span data-ttu-id="46643-389">ID pessoal</span><span class="sxs-lookup"><span data-stu-id="46643-389">personal id</span></span>
  
<span data-ttu-id="46643-390">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="46643-390">personal id number</span></span>
  
<span data-ttu-id="46643-391">personalidno #</span><span class="sxs-lookup"><span data-stu-id="46643-391">personalidno#</span></span>
  
<span data-ttu-id="46643-392">número de identificação exclusivo</span><span class="sxs-lookup"><span data-stu-id="46643-392">unique id number</span></span>
  
<span data-ttu-id="46643-393">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="46643-393">personalidnumber#</span></span>
  
<span data-ttu-id="46643-394">chave de ID exclusiva</span><span class="sxs-lookup"><span data-stu-id="46643-394">unique id key</span></span>
  
<span data-ttu-id="46643-395">código de ID pessoal</span><span class="sxs-lookup"><span data-stu-id="46643-395">personal id code</span></span>
  
<span data-ttu-id="46643-396">uniqueidkey #</span><span class="sxs-lookup"><span data-stu-id="46643-396">uniqueidkey#</span></span>
  
<span data-ttu-id="46643-397">código individual</span><span class="sxs-lookup"><span data-stu-id="46643-397">individual code</span></span>
  
<span data-ttu-id="46643-398">ID individual</span><span class="sxs-lookup"><span data-stu-id="46643-398">individual id</span></span>
  
<span data-ttu-id="46643-399">ID eindeutige-Nummer</span><span class="sxs-lookup"><span data-stu-id="46643-399">eindeutige id-nummer</span></span>
  
<span data-ttu-id="46643-400">ID eindeutige</span><span class="sxs-lookup"><span data-stu-id="46643-400">eindeutige id</span></span>
  
<span data-ttu-id="46643-401">ID personnelle</span><span class="sxs-lookup"><span data-stu-id="46643-401">id personnelle</span></span>
  
<span data-ttu-id="46643-402">Numéro d'identification</span><span class="sxs-lookup"><span data-stu-id="46643-402">numéro d'identification personnel</span></span>
  
<span data-ttu-id="46643-403">idpersonnelle #</span><span class="sxs-lookup"><span data-stu-id="46643-403">idpersonnelle#</span></span>
  
<span data-ttu-id="46643-404">Persönliche identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="46643-404">persönliche identifikationsnummer</span></span>
  
<span data-ttu-id="46643-405">eindeutigeid #</span><span class="sxs-lookup"><span data-stu-id="46643-405">eindeutigeid#</span></span>
  
## <a name="malta"></a><span data-ttu-id="46643-406">Malta</span><span class="sxs-lookup"><span data-stu-id="46643-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="46643-407">Format</span><span class="sxs-lookup"><span data-stu-id="46643-407">Format</span></span>

<span data-ttu-id="46643-408">Sete dígitos seguidos de uma letra</span><span class="sxs-lookup"><span data-stu-id="46643-408">Seven digits followed by one letter</span></span>
  
### <a name="pattern"></a><span data-ttu-id="46643-409">Padrão</span><span class="sxs-lookup"><span data-stu-id="46643-409">Pattern</span></span>

<span data-ttu-id="46643-410">Sete dígitos seguidos de uma letra:</span><span class="sxs-lookup"><span data-stu-id="46643-410">Seven digits followed by one letter:</span></span>
  
-  <span data-ttu-id="46643-411">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="46643-411">Seven digits</span></span> 
    
- <span data-ttu-id="46643-412">Uma letra maiúscula (diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="46643-412">One uppercase letter (case sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="46643-413">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="46643-413">Checksum</span></span>

<span data-ttu-id="46643-414">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="46643-414">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="46643-415">Definição</span><span class="sxs-lookup"><span data-stu-id="46643-415">Definition</span></span>

<span data-ttu-id="46643-416">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="46643-416">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46643-417">A expressão `Regex_malta_eu_national_id_card` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="46643-417">The regular expression  `Regex_malta_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46643-418">Uma palavra- `Keywords_malta_eu_national_id_card` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="46643-418">A keyword from  `Keywords_malta_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="46643-419">Uma política de DLP tem 65% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="46643-419">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46643-420">A expressão `Regex_malta_eu_national_id_card` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="46643-420">The regular expression  `Regex_malta_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="46643-421">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="46643-421">Keywords</span></span>

#### <a name="keywordsmaltaeunationalidcard"></a><span data-ttu-id="46643-422">Keywords_malta_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="46643-422">Keywords_malta_eu_national_id_card</span></span>

<span data-ttu-id="46643-423">código numérico pessoal</span><span class="sxs-lookup"><span data-stu-id="46643-423">personal numeric code</span></span>
  
<span data-ttu-id="46643-424">número de identificação exclusivo</span><span class="sxs-lookup"><span data-stu-id="46643-424">unique identification number</span></span>
  
<span data-ttu-id="46643-425">número do serviço do cidadão</span><span class="sxs-lookup"><span data-stu-id="46643-425">citizen service number</span></span>
  
<span data-ttu-id="46643-426">número de identidade exclusivo</span><span class="sxs-lookup"><span data-stu-id="46643-426">unique identity number</span></span>
  
<span data-ttu-id="46643-427">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="46643-427">uniqueidentityno#</span></span>
  
<span data-ttu-id="46643-428">Kodiċi numerali pessoali</span><span class="sxs-lookup"><span data-stu-id="46643-428">kodiċi numerali personali</span></span>
  
<span data-ttu-id="46643-429">numru ta ' identifikazzjoni uniku</span><span class="sxs-lookup"><span data-stu-id="46643-429">numru ta 'identifikazzjoni uniku</span></span>
  
<span data-ttu-id="46643-430">numru tas-servizz taċ-ċittadin</span><span class="sxs-lookup"><span data-stu-id="46643-430">numru tas-servizz taċ-ċittadin</span></span>
  
<span data-ttu-id="46643-431">numru ta ' Identità uniku</span><span class="sxs-lookup"><span data-stu-id="46643-431">numru ta' identità uniku</span></span>
  
## <a name="netherlands"></a><span data-ttu-id="46643-432">Países Baixos</span><span class="sxs-lookup"><span data-stu-id="46643-432">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="46643-433">Format</span><span class="sxs-lookup"><span data-stu-id="46643-433">Format</span></span>

<span data-ttu-id="46643-434">Nove dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="46643-434">Nine digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="46643-435">Padrão</span><span class="sxs-lookup"><span data-stu-id="46643-435">Pattern</span></span>

<span data-ttu-id="46643-436">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="46643-436">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="46643-437">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="46643-437">Checksum</span></span>

<span data-ttu-id="46643-438">Sim</span><span class="sxs-lookup"><span data-stu-id="46643-438">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="46643-439">Definição</span><span class="sxs-lookup"><span data-stu-id="46643-439">Definition</span></span>

<span data-ttu-id="46643-440">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="46643-440">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46643-441">A função `Func_netherlands_eu_national_id_card` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="46643-441">The function  `Func_netherlands_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46643-442">Uma palavra-chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="46643-442">A keyword from is found.</span></span>
    
<span data-ttu-id="46643-443">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="46643-443">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46643-444">A função `Func_netherlands_eu_national_id_card` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="46643-444">The function  `Func_netherlands_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="46643-445">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="46643-445">Keywords</span></span>

#### <a name="keywordsnetherlandseunationalidcard"></a><span data-ttu-id="46643-446">Keywords_netherlands_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="46643-446">Keywords_netherlands_eu_national_id_card</span></span>

<span data-ttu-id="46643-447">código numérico pessoal</span><span class="sxs-lookup"><span data-stu-id="46643-447">personal numeric code</span></span>
  
<span data-ttu-id="46643-448">número de identificação exclusivo</span><span class="sxs-lookup"><span data-stu-id="46643-448">unique identification number</span></span>
  
<span data-ttu-id="46643-449">número do serviço do cidadão</span><span class="sxs-lookup"><span data-stu-id="46643-449">citizen service number</span></span>
  
<span data-ttu-id="46643-450">número de identidade exclusivo</span><span class="sxs-lookup"><span data-stu-id="46643-450">unique identity number</span></span>
  
<span data-ttu-id="46643-451">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="46643-451">uniqueidentityno#</span></span>
  
<span data-ttu-id="46643-452">BSN</span><span class="sxs-lookup"><span data-stu-id="46643-452">bsn</span></span>
  
<span data-ttu-id="46643-453">BSN</span><span class="sxs-lookup"><span data-stu-id="46643-453">bsn#</span></span>
  
<span data-ttu-id="46643-454">código de numerieke persoonlijke</span><span class="sxs-lookup"><span data-stu-id="46643-454">persoonlijke numerieke code</span></span>
  
<span data-ttu-id="46643-455">uniek identificatienummer</span><span class="sxs-lookup"><span data-stu-id="46643-455">uniek identificatienummer</span></span>
  
<span data-ttu-id="46643-456">burgerservicenummer</span><span class="sxs-lookup"><span data-stu-id="46643-456">burgerservicenummer</span></span>
  
<span data-ttu-id="46643-457">uniek identiteitsnummer</span><span class="sxs-lookup"><span data-stu-id="46643-457">uniek identiteitsnummer</span></span>
  
## <a name="poland"></a><span data-ttu-id="46643-458">Polônia</span><span class="sxs-lookup"><span data-stu-id="46643-458">Poland</span></span>

<span data-ttu-id="46643-459">Para obter detalhes, consulte a seção "ID nacional da Polônia (PESEL)" em [que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="46643-459">For details, see the section "Poland National ID (PESEL)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="46643-460">Portugal</span><span class="sxs-lookup"><span data-stu-id="46643-460">Portugal</span></span>

<span data-ttu-id="46643-461">Para obter detalhes, consulte a seção "número de cartão de cidadão da Portugal" em [o que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="46643-461">For details, see the section "Portugal Citizen Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="romania"></a><span data-ttu-id="46643-462">Romênia</span><span class="sxs-lookup"><span data-stu-id="46643-462">Romania</span></span>

### <a name="format"></a><span data-ttu-id="46643-463">Format</span><span class="sxs-lookup"><span data-stu-id="46643-463">Format</span></span>

<span data-ttu-id="46643-464">13 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="46643-464">13 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="46643-465">Padrão</span><span class="sxs-lookup"><span data-stu-id="46643-465">Pattern</span></span>

<span data-ttu-id="46643-466">13 dígitos</span><span class="sxs-lookup"><span data-stu-id="46643-466">13 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="46643-467">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="46643-467">Checksum</span></span>

<span data-ttu-id="46643-468">Sim</span><span class="sxs-lookup"><span data-stu-id="46643-468">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="46643-469">Definição</span><span class="sxs-lookup"><span data-stu-id="46643-469">Definition</span></span>

<span data-ttu-id="46643-470">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="46643-470">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46643-471">A função `Func_romania_eu_national_id_card` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="46643-471">The function  `Func_romania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46643-472">Uma palavra- `Keywords_romania_eu_national_id_card` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="46643-472">A keyword from  `Keywords_romania_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="46643-473">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="46643-473">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46643-474">A função `Func_romania_eu_national_id_card` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="46643-474">The function  `Func_romania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="46643-475">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="46643-475">Keywords</span></span>

#### <a name="keywordsromaniaeunationalidcard"></a><span data-ttu-id="46643-476">Keywords_romania_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="46643-476">Keywords_romania_eu_national_id_card</span></span>

<span data-ttu-id="46643-477">código numérico pessoal</span><span class="sxs-lookup"><span data-stu-id="46643-477">personal numeric code</span></span>
  
<span data-ttu-id="46643-478">número de identificação exclusivo</span><span class="sxs-lookup"><span data-stu-id="46643-478">unique identification number</span></span>
  
<span data-ttu-id="46643-479">CNP</span><span class="sxs-lookup"><span data-stu-id="46643-479">cnp</span></span>
  
<span data-ttu-id="46643-480">CNP #</span><span class="sxs-lookup"><span data-stu-id="46643-480">cnp#</span></span>
  
<span data-ttu-id="46643-481">pessoal</span><span class="sxs-lookup"><span data-stu-id="46643-481">pin</span></span>
  
<span data-ttu-id="46643-482">pessoal</span><span class="sxs-lookup"><span data-stu-id="46643-482">pin#</span></span>
  
<span data-ttu-id="46643-483">número de seguro</span><span class="sxs-lookup"><span data-stu-id="46643-483">insurance number</span></span>
  
<span data-ttu-id="46643-484">insurancenumber #</span><span class="sxs-lookup"><span data-stu-id="46643-484">insurancenumber#</span></span>
  
<span data-ttu-id="46643-485">número de identidade exclusivo</span><span class="sxs-lookup"><span data-stu-id="46643-485">unique identity number</span></span>
  
<span data-ttu-id="46643-486">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="46643-486">uniqueidentityno#</span></span>
  
<span data-ttu-id="46643-487">c.o.d. numérico pessoal</span><span class="sxs-lookup"><span data-stu-id="46643-487">cod numeric personal</span></span>
  
<span data-ttu-id="46643-488">identificare de c.o.d. pessoal</span><span class="sxs-lookup"><span data-stu-id="46643-488">cod identificare personal</span></span>
  
<span data-ttu-id="46643-489">UNIC de c.o.d. identificare</span><span class="sxs-lookup"><span data-stu-id="46643-489">cod unic identificare</span></span>
  
<span data-ttu-id="46643-490">număr pessoal do UNIC</span><span class="sxs-lookup"><span data-stu-id="46643-490">număr personal unic</span></span>
  
<span data-ttu-id="46643-491">număr identitate</span><span class="sxs-lookup"><span data-stu-id="46643-491">număr identitate</span></span>
  
<span data-ttu-id="46643-492">număr identificare pessoal</span><span class="sxs-lookup"><span data-stu-id="46643-492">număr identificare personal</span></span>
  
<span data-ttu-id="46643-493">număridentitate #</span><span class="sxs-lookup"><span data-stu-id="46643-493">număridentitate#</span></span>
  
<span data-ttu-id="46643-494">codnumericpersonal #</span><span class="sxs-lookup"><span data-stu-id="46643-494">codnumericpersonal#</span></span>
  
<span data-ttu-id="46643-495">numărpersonalunic #</span><span class="sxs-lookup"><span data-stu-id="46643-495">numărpersonalunic#</span></span>
  
## <a name="slovakia"></a><span data-ttu-id="46643-496">Eslováquia</span><span class="sxs-lookup"><span data-stu-id="46643-496">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="46643-497">Format</span><span class="sxs-lookup"><span data-stu-id="46643-497">Format</span></span>

<span data-ttu-id="46643-498">Dez dígitos contendo uma barra invertida</span><span class="sxs-lookup"><span data-stu-id="46643-498">Ten digits containing one backslash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="46643-499">Padrão</span><span class="sxs-lookup"><span data-stu-id="46643-499">Pattern</span></span>

<span data-ttu-id="46643-500">Dez dígitos contendo uma barra invertida:</span><span class="sxs-lookup"><span data-stu-id="46643-500">Ten digits containing one backslash:</span></span>
  
### <a name="checksum"></a><span data-ttu-id="46643-501">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="46643-501">Checksum</span></span>

<span data-ttu-id="46643-502">Sim</span><span class="sxs-lookup"><span data-stu-id="46643-502">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="46643-503">Definição</span><span class="sxs-lookup"><span data-stu-id="46643-503">Definition</span></span>

<span data-ttu-id="46643-504">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="46643-504">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46643-505">A função `Func_slovakia_eu_national_id_card` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="46643-505">The function  `Func_slovakia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46643-506">Uma palavra- `Keywords_slovakia_eu_national_id_card` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="46643-506">A keyword from  `Keywords_slovakia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="46643-507">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="46643-507">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46643-508">A função `Func_slovakia_eu_national_id_card` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="46643-508">The function  `Func_slovakia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="46643-509">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="46643-509">Keywords</span></span>

#### <a name="keywordsslovakiaeunationalidcard"></a><span data-ttu-id="46643-510">Keywords_slovakia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="46643-510">Keywords_slovakia_eu_national_id_card</span></span>

<span data-ttu-id="46643-511">número de nascimento</span><span class="sxs-lookup"><span data-stu-id="46643-511">birth number</span></span>
  
<span data-ttu-id="46643-512">national identification number</span><span class="sxs-lookup"><span data-stu-id="46643-512">national identification number</span></span>
  
<span data-ttu-id="46643-513">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="46643-513">personal identification number</span></span>
  
<span data-ttu-id="46643-514">social security number</span><span class="sxs-lookup"><span data-stu-id="46643-514">social security number</span></span>
  
<span data-ttu-id="46643-515">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="46643-515">nationalnumber#</span></span>
  
<span data-ttu-id="46643-516">es</span><span class="sxs-lookup"><span data-stu-id="46643-516">ssn#</span></span>
  
<span data-ttu-id="46643-517">es</span><span class="sxs-lookup"><span data-stu-id="46643-517">ssn</span></span>
  
<span data-ttu-id="46643-518">número nacional</span><span class="sxs-lookup"><span data-stu-id="46643-518">national number</span></span>
  
<span data-ttu-id="46643-519">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="46643-519">personal id number</span></span>
  
<span data-ttu-id="46643-520">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="46643-520">personalidnumber#</span></span>
  
<span data-ttu-id="46643-521">rč</span><span class="sxs-lookup"><span data-stu-id="46643-521">rč</span></span>
  
<span data-ttu-id="46643-522">rodné číslo</span><span class="sxs-lookup"><span data-stu-id="46643-522">rodné číslo</span></span>
  
<span data-ttu-id="46643-523">RODNE cislo</span><span class="sxs-lookup"><span data-stu-id="46643-523">rodne cislo</span></span>
  
## <a name="slovenia"></a><span data-ttu-id="46643-524">Eslovênia</span><span class="sxs-lookup"><span data-stu-id="46643-524">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="46643-525">Format</span><span class="sxs-lookup"><span data-stu-id="46643-525">Format</span></span>

<span data-ttu-id="46643-526">13 dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="46643-526">13 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="46643-527">Padrão</span><span class="sxs-lookup"><span data-stu-id="46643-527">Pattern</span></span>

<span data-ttu-id="46643-528">13 dígitos no padrão especificado:</span><span class="sxs-lookup"><span data-stu-id="46643-528">13 digits in the specified pattern:</span></span>
  
-  <span data-ttu-id="46643-529">Sete dígitos que correspondem à data de nascimento (DDMMLLL), onde "LLL" corresponde aos últimos três dígitos do ano de nascimento</span><span class="sxs-lookup"><span data-stu-id="46643-529">Seven digits that correspond to the birth date (DDMMLLL) where "LLL" corresponds to the last three digits of the birth year</span></span> 
    
- <span data-ttu-id="46643-530">Dois dígitos que correspondem à área de nascimento</span><span class="sxs-lookup"><span data-stu-id="46643-530">Two digits that correspond to the area of birth</span></span>
    
- <span data-ttu-id="46643-531">Três dígitos que correspondem a uma combinação de sexo e número de série para pessoas nasceu no mesmo dia (000-499 para macho e 500-999 para fêmea)</span><span class="sxs-lookup"><span data-stu-id="46643-531">Three digits that correspond to a combination of gender and serial number for persons born on the same day (000-499 for male and 500-999 for female)</span></span>
    
- <span data-ttu-id="46643-532">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="46643-532">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="46643-533">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="46643-533">Checksum</span></span>

<span data-ttu-id="46643-534">Sim</span><span class="sxs-lookup"><span data-stu-id="46643-534">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="46643-535">Definição</span><span class="sxs-lookup"><span data-stu-id="46643-535">Definition</span></span>

<span data-ttu-id="46643-536">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="46643-536">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46643-537">A função `Func_slovenia_eu_national_id_card` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="46643-537">The function  `Func_slovenia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46643-538">Uma palavra- `Keywords_slovenia_eu_national_id_card` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="46643-538">A keyword from  `Keywords_slovenia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="46643-539">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="46643-539">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46643-540">A função `Func_slovenia_eu_national_id_card` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="46643-540">The function  `Func_slovenia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="46643-541">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="46643-541">Keywords</span></span>

#### <a name="keywordssloveniaeunationalidcard"></a><span data-ttu-id="46643-542">Keywords_slovenia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="46643-542">Keywords_slovenia_eu_national_id_card</span></span>

<span data-ttu-id="46643-543">código numérico pessoal</span><span class="sxs-lookup"><span data-stu-id="46643-543">personal numeric code</span></span>
  
<span data-ttu-id="46643-544">número de identificação exclusivo</span><span class="sxs-lookup"><span data-stu-id="46643-544">unique identification number</span></span>
  
<span data-ttu-id="46643-545">número de registro exclusivo</span><span class="sxs-lookup"><span data-stu-id="46643-545">unique registration number</span></span>
  
<span data-ttu-id="46643-546">número de identidade exclusivo</span><span class="sxs-lookup"><span data-stu-id="46643-546">unique identity number</span></span>
  
<span data-ttu-id="46643-547">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="46643-547">uniqueidentityno#</span></span>
  
<span data-ttu-id="46643-548">número de cidadão mestre exclusivo</span><span class="sxs-lookup"><span data-stu-id="46643-548">unique master citizen number</span></span>
  
<span data-ttu-id="46643-549">edinstvena identifikacijska številka</span><span class="sxs-lookup"><span data-stu-id="46643-549">edinstvena identifikacijska številka</span></span>
  
<span data-ttu-id="46643-550">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="46643-550">uniqueidentityno #</span></span>
  
<span data-ttu-id="46643-551">edinstvena številka glavnega državljana</span><span class="sxs-lookup"><span data-stu-id="46643-551">edinstvena številka glavnega državljana</span></span>
  
<span data-ttu-id="46643-552">emšo</span><span class="sxs-lookup"><span data-stu-id="46643-552">emšo</span></span>
  
## <a name="spain"></a><span data-ttu-id="46643-553">Espanha</span><span class="sxs-lookup"><span data-stu-id="46643-553">Spain</span></span>

### <a name="format"></a><span data-ttu-id="46643-554">Format</span><span class="sxs-lookup"><span data-stu-id="46643-554">Format</span></span>

<span data-ttu-id="46643-555">Sete dígitos seguidos de um caractere</span><span class="sxs-lookup"><span data-stu-id="46643-555">Seven digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="46643-556">Padrão</span><span class="sxs-lookup"><span data-stu-id="46643-556">Pattern</span></span>

<span data-ttu-id="46643-557">Sete dígitos seguidos de um caractere</span><span class="sxs-lookup"><span data-stu-id="46643-557">Seven digits followed by one character</span></span>
  
- <span data-ttu-id="46643-558">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="46643-558">Seven digits</span></span>
    
- <span data-ttu-id="46643-559">Um dígito ou letra (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="46643-559">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="46643-560">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="46643-560">Checksum</span></span>

<span data-ttu-id="46643-561">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="46643-561">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="46643-562">Definição</span><span class="sxs-lookup"><span data-stu-id="46643-562">Definition</span></span>

<span data-ttu-id="46643-563">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="46643-563">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46643-564">A expressão `Regex_spain_eu_national_id_card` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="46643-564">The regular expression  `Regex_spain_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46643-565">Uma palavra- `Keywords_spain_eu_national_id_card"` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="46643-565">A keyword from  `Keywords_spain_eu_national_id_card"` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_national_id_card" />
          <Match idRef="Keywords_spain_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="46643-566">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="46643-566">Keywords</span></span>

#### <a name="keywordsspaineunationalidcard"></a><span data-ttu-id="46643-567">Keywords_spain_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="46643-567">Keywords_spain_eu_national_id_card</span></span>

<span data-ttu-id="46643-568">DNI</span><span class="sxs-lookup"><span data-stu-id="46643-568">dni</span></span>
  
<span data-ttu-id="46643-569">national identification number</span><span class="sxs-lookup"><span data-stu-id="46643-569">national identification number</span></span>
  
<span data-ttu-id="46643-570">número de identidade nacional</span><span class="sxs-lookup"><span data-stu-id="46643-570">national identity number</span></span>
  
<span data-ttu-id="46643-571">número de seguro</span><span class="sxs-lookup"><span data-stu-id="46643-571">insurance number</span></span>
  
<span data-ttu-id="46643-572">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="46643-572">personal identification number</span></span>
  
<span data-ttu-id="46643-573">identidade nacional</span><span class="sxs-lookup"><span data-stu-id="46643-573">national identity</span></span>
  
<span data-ttu-id="46643-574">identidade pessoal não</span><span class="sxs-lookup"><span data-stu-id="46643-574">personal identity no</span></span>
  
<span data-ttu-id="46643-575">número de identidade exclusivo</span><span class="sxs-lookup"><span data-stu-id="46643-575">unique identity number</span></span>
  
<span data-ttu-id="46643-576">nationalidno #</span><span class="sxs-lookup"><span data-stu-id="46643-576">nationalidno#</span></span>
  
<span data-ttu-id="46643-577">UniqueId</span><span class="sxs-lookup"><span data-stu-id="46643-577">uniqueid#</span></span>
  
<span data-ttu-id="46643-578">DNI #</span><span class="sxs-lookup"><span data-stu-id="46643-578">dni#</span></span>
  
<span data-ttu-id="46643-579">nationalid #</span><span class="sxs-lookup"><span data-stu-id="46643-579">nationalid#</span></span>
  
<span data-ttu-id="46643-580">Nie #</span><span class="sxs-lookup"><span data-stu-id="46643-580">nie#</span></span>
  
<span data-ttu-id="46643-581">Nie</span><span class="sxs-lookup"><span data-stu-id="46643-581">nie</span></span>
  
<span data-ttu-id="46643-582">nienúmero #</span><span class="sxs-lookup"><span data-stu-id="46643-582">nienúmero#</span></span>
  
<span data-ttu-id="46643-583">Nie número</span><span class="sxs-lookup"><span data-stu-id="46643-583">nie número</span></span>
  
<span data-ttu-id="46643-584">documento nacional de Identidad</span><span class="sxs-lookup"><span data-stu-id="46643-584">documento nacional de identidad</span></span>
  
<span data-ttu-id="46643-585">identidad único</span><span class="sxs-lookup"><span data-stu-id="46643-585">identidad único</span></span>
  
<span data-ttu-id="46643-586">número nacional identidad</span><span class="sxs-lookup"><span data-stu-id="46643-586">número nacional identidad</span></span>
  
<span data-ttu-id="46643-587">DNI número</span><span class="sxs-lookup"><span data-stu-id="46643-587">dni número</span></span>
  
<span data-ttu-id="46643-588">dninúmero #</span><span class="sxs-lookup"><span data-stu-id="46643-588">dninúmero#</span></span>
  
<span data-ttu-id="46643-589">identidadúnico #</span><span class="sxs-lookup"><span data-stu-id="46643-589">identidadúnico#</span></span>
  
## <a name="sweden"></a><span data-ttu-id="46643-590">Suécia</span><span class="sxs-lookup"><span data-stu-id="46643-590">Sweden</span></span>

<span data-ttu-id="46643-591">Para obter detalhes, consulte a seção "ID nacional da Suécia" em [o que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="46643-591">For details, see the section "Sweden National ID" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="46643-592">Confira também</span><span class="sxs-lookup"><span data-stu-id="46643-592">See also</span></span>

[<span data-ttu-id="46643-593">O que os tipos de informações confidenciais procuram</span><span class="sxs-lookup"><span data-stu-id="46643-593">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)


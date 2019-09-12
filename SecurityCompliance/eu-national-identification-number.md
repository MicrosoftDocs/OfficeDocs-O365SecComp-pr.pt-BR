---
title: Número de identificação nacional da UE
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: Este tópico mostra o que uma política de prevenção de perda de dados (DLP) procura quando detecta o tipo de informação confidencial do número de identificação nacional da UE. Esse tipo de informação confidencial define diferentes padrões, palavras-chave e outras evidências para cada país.
ms.openlocfilehash: b784b7509eed899f9f03db96ee5e827b9bf70d2e
ms.sourcegitcommit: ff370e93b792204547694139ef99bc0848304570
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/11/2019
ms.locfileid: "36852743"
---
# <a name="eu-national-identification-number"></a><span data-ttu-id="4dbb4-104">Número de identificação nacional da UE</span><span class="sxs-lookup"><span data-stu-id="4dbb4-104">EU National Identification Number</span></span>

<span data-ttu-id="4dbb4-105">Este tópico mostra o que uma política de prevenção de perda de dados (DLP) procura quando detecta o tipo de informação confidencial do número de identificação nacional da UE.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU National Identification Number sensitive information type.</span></span> <span data-ttu-id="4dbb4-106">Esse tipo de informação confidencial define diferentes padrões, palavras-chave e outras evidências para cada país.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="4dbb4-107">Áustria </span><span class="sxs-lookup"><span data-stu-id="4dbb4-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="4dbb4-108">Formatar</span><span class="sxs-lookup"><span data-stu-id="4dbb4-108">Format</span></span>

<span data-ttu-id="4dbb4-109">Uma combinação de 24 caracteres de letras, dígitos e caracteres especiais</span><span class="sxs-lookup"><span data-stu-id="4dbb4-109">A 24-character combination of letters, digits, and special characters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4dbb4-110">Padrão</span><span class="sxs-lookup"><span data-stu-id="4dbb4-110">Pattern</span></span>

<span data-ttu-id="4dbb4-111">24 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4dbb4-111">24 characters:</span></span>
  
-  <span data-ttu-id="4dbb4-112">22 letras (não diferencia maiúsculas de minúsculas), dígitos, barras invertidas, barras encaminhadas ou sinais de adição</span><span class="sxs-lookup"><span data-stu-id="4dbb4-112">22 letters (not case-sensitive), digits, backslashes, forward slashes, or plus signs</span></span> 
    
- <span data-ttu-id="4dbb4-113">Duas letras (não diferencia maiúsculas de minúsculas), dígitos, barras invertidas, barras invertidas, sinais de adição ou sinais de igual</span><span class="sxs-lookup"><span data-stu-id="4dbb4-113">Two letters (not case-sensitive), digits, backslashes, forward slashes, plus signs, or equal signs</span></span>
    
### <a name="checksum"></a><span data-ttu-id="4dbb4-114">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="4dbb4-114">Checksum</span></span>

<span data-ttu-id="4dbb4-115">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="4dbb4-115">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="4dbb4-116">Definição</span><span class="sxs-lookup"><span data-stu-id="4dbb4-116">Definition</span></span>

<span data-ttu-id="4dbb4-117">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4dbb4-117">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4dbb4-118">A expressão `Regex_austria_eu_national_id_card` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-118">The regular expression  `Regex_austria_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4dbb4-119">Uma palavra- `Keywords_austria_eu_national_id_card` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-119">A keyword from  `Keywords_austria_eu_national_id_card` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_national_id_card" />
          <Match idRef="Keywords_austria_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4dbb4-120">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="4dbb4-120">Keywords</span></span>

#### <a name="keywords_austria_eu_national_id_card"></a><span data-ttu-id="4dbb4-121">Keywords_austria_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="4dbb4-121">Keywords_austria_eu_national_id_card</span></span>

<span data-ttu-id="4dbb4-122">número de identidade austríaca</span><span class="sxs-lookup"><span data-stu-id="4dbb4-122">austrian identity number</span></span>
  
<span data-ttu-id="4dbb4-123">número de identidade nacional</span><span class="sxs-lookup"><span data-stu-id="4dbb4-123">national identity number</span></span>
  
<span data-ttu-id="4dbb4-124">número de identidade</span><span class="sxs-lookup"><span data-stu-id="4dbb4-124">identity number</span></span>
  
<span data-ttu-id="4dbb4-125">national id</span><span class="sxs-lookup"><span data-stu-id="4dbb4-125">national id</span></span>
  
<span data-ttu-id="4dbb4-126">personalausweis republik österreich</span><span class="sxs-lookup"><span data-stu-id="4dbb4-126">personalausweis republik österreich</span></span>
  
## <a name="belgium"></a><span data-ttu-id="4dbb4-127">Bélgica </span><span class="sxs-lookup"><span data-stu-id="4dbb4-127">Belgium</span></span>

<span data-ttu-id="4dbb4-128">Para obter detalhes, consulte a seção "número nacional da Bélgica" em o [que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="4dbb4-128">For details, see the section "Belgium National Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="bulgaria"></a><span data-ttu-id="4dbb4-129">Bulgária</span><span class="sxs-lookup"><span data-stu-id="4dbb4-129">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="4dbb4-130">Formatar</span><span class="sxs-lookup"><span data-stu-id="4dbb4-130">Format</span></span>

<span data-ttu-id="4dbb4-131">Dez dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="4dbb4-131">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4dbb4-132">Padrão</span><span class="sxs-lookup"><span data-stu-id="4dbb4-132">Pattern</span></span>

<span data-ttu-id="4dbb4-133">Dez dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="4dbb4-133">Ten digits without spaces and delimiters</span></span>
  
-  <span data-ttu-id="4dbb4-134">Seis dígitos que correspondem à data de nascimento (AAMMDD)</span><span class="sxs-lookup"><span data-stu-id="4dbb4-134">Six digits that correspond to the birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="4dbb4-135">Dois dígitos que correspondem à ordem de nascimento</span><span class="sxs-lookup"><span data-stu-id="4dbb4-135">Two digits that correspond to the birth order</span></span>
    
- <span data-ttu-id="4dbb4-136">Um dígito que corresponde ao gênero: um dígito par para macho e um dígito estranho para o fêmea</span><span class="sxs-lookup"><span data-stu-id="4dbb4-136">One digit that corresponds to gender: An even digit for male and an odd digit for female</span></span>
    
- <span data-ttu-id="4dbb4-137">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="4dbb4-137">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="4dbb4-138">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="4dbb4-138">Checksum</span></span>

<span data-ttu-id="4dbb4-139">Sim</span><span class="sxs-lookup"><span data-stu-id="4dbb4-139">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="4dbb4-140">Definição</span><span class="sxs-lookup"><span data-stu-id="4dbb4-140">Definition</span></span>

<span data-ttu-id="4dbb4-141">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4dbb4-141">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4dbb4-142">A função `Func_bulgaria_national_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-142">The function  `Func_bulgaria_national_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4dbb4-143">Uma palavra- `Keywords_bulgaria_national_number` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-143">A keyword from  `Keywords_bulgaria_national_number` is found.</span></span> 
    
<span data-ttu-id="4dbb4-144">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4dbb4-144">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4dbb4-145">A função `Func_bulgaria_national_number` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-145">The function  `Func_bulgaria_national_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="4dbb4-146">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="4dbb4-146">Keywords</span></span>

#### <a name="keywords_bulgaria_national_number"></a><span data-ttu-id="4dbb4-147">Keywords_bulgaria_national_number</span><span class="sxs-lookup"><span data-stu-id="4dbb4-147">Keywords_bulgaria_national_number</span></span>

<span data-ttu-id="4dbb4-148">egn</span><span class="sxs-lookup"><span data-stu-id="4dbb4-148">egn</span></span>
  
<span data-ttu-id="4dbb4-149">egn #</span><span class="sxs-lookup"><span data-stu-id="4dbb4-149">egn#</span></span>
  
<span data-ttu-id="4dbb4-150">número nacional búlgaro</span><span class="sxs-lookup"><span data-stu-id="4dbb4-150">bulgarian national number</span></span>
  
<span data-ttu-id="4dbb4-151">número nacional</span><span class="sxs-lookup"><span data-stu-id="4dbb4-151">national number</span></span>
  
<span data-ttu-id="4dbb4-152">social security number</span><span class="sxs-lookup"><span data-stu-id="4dbb4-152">social security number</span></span>
  
<span data-ttu-id="4dbb4-153">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="4dbb4-153">nationalnumber#</span></span>
  
<span data-ttu-id="4dbb4-154">es #</span><span class="sxs-lookup"><span data-stu-id="4dbb4-154">ssn#</span></span>
  
<span data-ttu-id="4dbb4-155">es</span><span class="sxs-lookup"><span data-stu-id="4dbb4-155">ssn</span></span>
  
<span data-ttu-id="4dbb4-156">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="4dbb4-156">nationalnumber</span></span>
  
<span data-ttu-id="4dbb4-157">bnn #</span><span class="sxs-lookup"><span data-stu-id="4dbb4-157">bnn#</span></span>
  
<span data-ttu-id="4dbb4-158">bnn</span><span class="sxs-lookup"><span data-stu-id="4dbb4-158">bnn</span></span>
  
<span data-ttu-id="4dbb4-159">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="4dbb4-159">personal id number</span></span>
  
<span data-ttu-id="4dbb4-160">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="4dbb4-160">personalidnumber#</span></span>
  
<span data-ttu-id="4dbb4-161">единен граждански номер</span><span class="sxs-lookup"><span data-stu-id="4dbb4-161">единен граждански номер</span></span>
  
<span data-ttu-id="4dbb4-162">edinen grazhdanski de nome</span><span class="sxs-lookup"><span data-stu-id="4dbb4-162">edinen grazhdanski nomer</span></span>
  
<span data-ttu-id="4dbb4-163">егн</span><span class="sxs-lookup"><span data-stu-id="4dbb4-163">егн</span></span>
  
<span data-ttu-id="4dbb4-164">егн #</span><span class="sxs-lookup"><span data-stu-id="4dbb4-164">егн#</span></span>
  
## <a name="croatia"></a><span data-ttu-id="4dbb4-165">Croácia</span><span class="sxs-lookup"><span data-stu-id="4dbb4-165">Croatia</span></span>

<span data-ttu-id="4dbb4-166">Para obter detalhes, consulte a seção "número de identidade da Croácia" em o [que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="4dbb4-166">For details, see the section "Croatia Identity Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="cyprus"></a><span data-ttu-id="4dbb4-167">Chipre</span><span class="sxs-lookup"><span data-stu-id="4dbb4-167">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="4dbb4-168">Formatar</span><span class="sxs-lookup"><span data-stu-id="4dbb4-168">Format</span></span>

<span data-ttu-id="4dbb4-169">Dez dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="4dbb4-169">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4dbb4-170">Padrão</span><span class="sxs-lookup"><span data-stu-id="4dbb4-170">Pattern</span></span>

 <span data-ttu-id="4dbb4-171">Dez dígitos</span><span class="sxs-lookup"><span data-stu-id="4dbb4-171">Ten digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="4dbb4-172">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="4dbb4-172">Checksum</span></span>

<span data-ttu-id="4dbb4-173">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="4dbb4-173">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="4dbb4-174">Definição</span><span class="sxs-lookup"><span data-stu-id="4dbb4-174">Definition</span></span>

<span data-ttu-id="4dbb4-175">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4dbb4-175">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4dbb4-176">A expressão `Regex_cyprus_eu_national_id_card` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-176">The regular expression  `Regex_cyprus_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4dbb4-177">Uma palavra- `Keywords_cyprus_eu_national_id_card` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-177">A keyword from  `Keywords_cyprus_eu_national_id_card` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_national_id_card" />
          <Match idRef="Keywords_cyprus_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4dbb4-178">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="4dbb4-178">Keywords</span></span>

#### <a name="keywords_cyprus_eu_national_id_card"></a><span data-ttu-id="4dbb4-179">Keywords_cyprus_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="4dbb4-179">Keywords_cyprus_eu_national_id_card</span></span>

<span data-ttu-id="4dbb4-180">número do cartão de identificação</span><span class="sxs-lookup"><span data-stu-id="4dbb4-180">id card number</span></span>
  
<span data-ttu-id="4dbb4-181">national identification number</span><span class="sxs-lookup"><span data-stu-id="4dbb4-181">national identification number</span></span>
  
<span data-ttu-id="4dbb4-182">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="4dbb4-182">personal id number</span></span>
  
<span data-ttu-id="4dbb4-183">número do cartão de identidade</span><span class="sxs-lookup"><span data-stu-id="4dbb4-183">identity card number</span></span>
  
<span data-ttu-id="4dbb4-184">ταυτοτητασ</span><span class="sxs-lookup"><span data-stu-id="4dbb4-184">ταυτοτητασ</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="4dbb4-185">República Tcheca</span><span class="sxs-lookup"><span data-stu-id="4dbb4-185">Czech Republic</span></span>

<span data-ttu-id="4dbb4-186">Para obter detalhes, consulte a seção "número de identidade nacional tcheco" em [que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="4dbb4-186">For details, see the section "Czech National Identity Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="denmark"></a><span data-ttu-id="4dbb4-187">Dinamarca</span><span class="sxs-lookup"><span data-stu-id="4dbb4-187">Denmark</span></span>

<span data-ttu-id="4dbb4-188">Para obter detalhes, consulte a seção "Dinamarca Personal Identification Number" em o [que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="4dbb4-188">For details, see the section "Denmark Personal Identification Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="estonia"></a><span data-ttu-id="4dbb4-189">Estônia</span><span class="sxs-lookup"><span data-stu-id="4dbb4-189">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="4dbb4-190">Formatar</span><span class="sxs-lookup"><span data-stu-id="4dbb4-190">Format</span></span>

<span data-ttu-id="4dbb4-191">11 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="4dbb4-191">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4dbb4-192">Padrão</span><span class="sxs-lookup"><span data-stu-id="4dbb4-192">Pattern</span></span>

<span data-ttu-id="4dbb4-193">11 dígitos:</span><span class="sxs-lookup"><span data-stu-id="4dbb4-193">11 digits:</span></span>
  
- <span data-ttu-id="4dbb4-194">Um dígito que corresponde ao sexo e ao século de nascimento (número ímpar masculino, mesmo número fêmea; 1-2:19 Century; 3-4:20 Century; 5-6:21 século)</span><span class="sxs-lookup"><span data-stu-id="4dbb4-194">One digit that corresponds to sex and century of birth (odd number male, even number female; 1-2: 19th century; 3-4: 20th century; 5-6: 21st century)</span></span>
    
- <span data-ttu-id="4dbb4-195">Seis dígitos que correspondem à data de nascimento (AAMMDD)</span><span class="sxs-lookup"><span data-stu-id="4dbb4-195">Six digits that correspond to date of birth (YYMMDD)</span></span>
    
- <span data-ttu-id="4dbb4-196">Três dígitos que correspondem a um número de série separando as pessoas que nasceu na mesma data</span><span class="sxs-lookup"><span data-stu-id="4dbb4-196">Three digits that correspond to a serial number separating persons born on the same date</span></span>
    
- <span data-ttu-id="4dbb4-197">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="4dbb4-197">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="4dbb4-198">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="4dbb4-198">Checksum</span></span>

<span data-ttu-id="4dbb4-199">Sim</span><span class="sxs-lookup"><span data-stu-id="4dbb4-199">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="4dbb4-200">Definição</span><span class="sxs-lookup"><span data-stu-id="4dbb4-200">Definition</span></span>

<span data-ttu-id="4dbb4-201">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4dbb4-201">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4dbb4-202">A função `Func_estonia_eu_national_id_card` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-202">The function  `Func_estonia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4dbb4-203">Uma palavra- `Keywords_estonia_eu_national_id_card` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-203">A keyword from  `Keywords_estonia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="4dbb4-204">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4dbb4-204">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4dbb4-205">A função `Func_estonia_eu_national_id_card` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-205">The function  `Func_estonia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="4dbb4-206">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="4dbb4-206">Keywords</span></span>

#### <a name="keywords_estonia_eu_national_id_card"></a><span data-ttu-id="4dbb4-207">Keywords_estonia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="4dbb4-207">Keywords_estonia_eu_national_id_card</span></span>

<span data-ttu-id="4dbb4-208">código de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="4dbb4-208">personal identification code</span></span>
  
<span data-ttu-id="4dbb4-209">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="4dbb4-209">personal identification number</span></span>
  
<span data-ttu-id="4dbb4-210">national identification number</span><span class="sxs-lookup"><span data-stu-id="4dbb4-210">national identification number</span></span>
  
<span data-ttu-id="4dbb4-211">número nacional</span><span class="sxs-lookup"><span data-stu-id="4dbb4-211">national number</span></span>
  
<span data-ttu-id="4dbb4-212">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="4dbb4-212">personal id number</span></span>
  
<span data-ttu-id="4dbb4-213">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="4dbb4-213">personalidnumber#</span></span>
  
<span data-ttu-id="4dbb4-214">IKMover</span><span class="sxs-lookup"><span data-stu-id="4dbb4-214">ik</span></span>
  
<span data-ttu-id="4dbb4-215">isikukood</span><span class="sxs-lookup"><span data-stu-id="4dbb4-215">isikukood</span></span>
  
<span data-ttu-id="4dbb4-216">ID-kaart</span><span class="sxs-lookup"><span data-stu-id="4dbb4-216">id-kaart</span></span>
  
## <a name="finland"></a><span data-ttu-id="4dbb4-217">Finlândia</span><span class="sxs-lookup"><span data-stu-id="4dbb4-217">Finland</span></span>

<span data-ttu-id="4dbb4-218">Para obter detalhes, consulte a seção "ID nacional da Finlândia" em o [que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="4dbb4-218">For details, see the section "Finland National ID" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="4dbb4-219">França</span><span class="sxs-lookup"><span data-stu-id="4dbb4-219">France</span></span>

<span data-ttu-id="4dbb4-220">Para obter detalhes, consulte a seção "CNI (cartão de ID nacional da França)" em [que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="4dbb4-220">For details, see the section "France National ID Card (CNI)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="4dbb4-221">Alemanha</span><span class="sxs-lookup"><span data-stu-id="4dbb4-221">Germany</span></span>

<span data-ttu-id="4dbb4-222">Para obter detalhes, consulte a seção "número do cartão de identidade da Alemanha" em [o que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="4dbb4-222">For details, see the section "Germany Identity Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="4dbb4-223">Grécia</span><span class="sxs-lookup"><span data-stu-id="4dbb4-223">Greece</span></span>

<span data-ttu-id="4dbb4-224">Para obter detalhes, consulte a seção "cartão de ID nacional da Grécia" em [que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="4dbb4-224">For details, see the section "Greece National ID Card" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="hungary"></a><span data-ttu-id="4dbb4-225">Hungria</span><span class="sxs-lookup"><span data-stu-id="4dbb4-225">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="4dbb4-226">Formatar</span><span class="sxs-lookup"><span data-stu-id="4dbb4-226">Format</span></span>

<span data-ttu-id="4dbb4-227">11 dígitos</span><span class="sxs-lookup"><span data-stu-id="4dbb4-227">11 digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4dbb4-228">Padrão</span><span class="sxs-lookup"><span data-stu-id="4dbb4-228">Pattern</span></span>

<span data-ttu-id="4dbb4-229">11 dígitos:</span><span class="sxs-lookup"><span data-stu-id="4dbb4-229">11 digits:</span></span>
  
-  <span data-ttu-id="4dbb4-230">Um dígito que corresponde ao gênero (1-macho, 2-fêmea, outros números também são possíveis para o cidadãos nasceu antes 1900 ou cidadãos com cidadania dupla)</span><span class="sxs-lookup"><span data-stu-id="4dbb4-230">One digit that corresponds to gender (1-male, 2-female, other numbers are also possible for citizens born before 1900 or citizens with double citizenship)</span></span> 
    
- <span data-ttu-id="4dbb4-231">Seis dígitos que correspondem à data de nascimento (AAMMDD)</span><span class="sxs-lookup"><span data-stu-id="4dbb4-231">Six digits that correspond to birth date (YYMMDD)</span></span>
    
- <span data-ttu-id="4dbb4-232">Três dígitos que correspondem a um número de série</span><span class="sxs-lookup"><span data-stu-id="4dbb4-232">Three digits that correspond to a serial number</span></span>
    
- <span data-ttu-id="4dbb4-233">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="4dbb4-233">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="4dbb4-234">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="4dbb4-234">Checksum</span></span>

<span data-ttu-id="4dbb4-235">Sim</span><span class="sxs-lookup"><span data-stu-id="4dbb4-235">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="4dbb4-236">Definição</span><span class="sxs-lookup"><span data-stu-id="4dbb4-236">Definition</span></span>

<span data-ttu-id="4dbb4-237">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4dbb4-237">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4dbb4-238">A função `Func_hungary_eu_national_id_card` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-238">The function  `Func_hungary_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4dbb4-239">Uma palavra- `Keywords_hungary_eu_national_id_card` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-239">A keyword from  `Keywords_hungary_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="4dbb4-240">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4dbb4-240">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4dbb4-241">A função `Func_hungary_eu_national_id_card` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-241">The function  `Func_hungary_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="4dbb4-242">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="4dbb4-242">Keywords</span></span>

#### <a name="keywords_hungary_eu_national_id_card"></a><span data-ttu-id="4dbb4-243">Keywords_hungary_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="4dbb4-243">Keywords_hungary_eu_national_id_card</span></span>

<span data-ttu-id="4dbb4-244">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="4dbb4-244">personal identification number</span></span>
  
<span data-ttu-id="4dbb4-245">identification number</span><span class="sxs-lookup"><span data-stu-id="4dbb4-245">identification number</span></span>
  
<span data-ttu-id="4dbb4-246">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="4dbb4-246">personal id number</span></span>
  
<span data-ttu-id="4dbb4-247">személyazonosító igazolvány</span><span class="sxs-lookup"><span data-stu-id="4dbb4-247">személyazonosító igazolvány</span></span>
  
## <a name="ireland"></a><span data-ttu-id="4dbb4-248">Irlanda</span><span class="sxs-lookup"><span data-stu-id="4dbb4-248">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="4dbb4-249">Formatar</span><span class="sxs-lookup"><span data-stu-id="4dbb4-249">Format</span></span>

<span data-ttu-id="4dbb4-250">Uma combinação de letras, dígitos e um espaço no padrão especificado de nove caracteres</span><span class="sxs-lookup"><span data-stu-id="4dbb4-250">A nine-character combination of letters, digits, and a space in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4dbb4-251">Padrão</span><span class="sxs-lookup"><span data-stu-id="4dbb4-251">Pattern</span></span>

<span data-ttu-id="4dbb4-252">Uma combinação de letras, dígitos e um espaço no padrão especificado de nove caracteres</span><span class="sxs-lookup"><span data-stu-id="4dbb4-252">A nine-character combination of letters, digits, and a space in the specified pattern</span></span>
  
<span data-ttu-id="4dbb4-253">De 1º de janeiro de 2013 até agora:</span><span class="sxs-lookup"><span data-stu-id="4dbb4-253">From 01 January 2013 to now:</span></span>
  
-  <span data-ttu-id="4dbb4-254">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="4dbb4-254">Seven digits</span></span> 
    
- <span data-ttu-id="4dbb4-255">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="4dbb4-255">One check digit</span></span>
    
- <span data-ttu-id="4dbb4-256">Um espaço ou a letra maiúscula "W" (diferencia maiúscula de minúscula)</span><span class="sxs-lookup"><span data-stu-id="4dbb4-256">One space or the uppercase letter "W" (Case sensitive)</span></span>
    
<span data-ttu-id="4dbb4-257">Antes de 1º de janeiro de 2013:</span><span class="sxs-lookup"><span data-stu-id="4dbb4-257">Prior to 01 January 2013:</span></span>
  
-  <span data-ttu-id="4dbb4-258">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="4dbb4-258">Seven digits</span></span> 
    
- <span data-ttu-id="4dbb4-259">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="4dbb4-259">One check digit</span></span>
    
- <span data-ttu-id="4dbb4-260">Um espaço ou uma letra maiúscula (diferencia maiúscula de minúscula)</span><span class="sxs-lookup"><span data-stu-id="4dbb4-260">One space or an uppercase letter (Case sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="4dbb4-261">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="4dbb4-261">Checksum</span></span>

<span data-ttu-id="4dbb4-262">Sim</span><span class="sxs-lookup"><span data-stu-id="4dbb4-262">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="4dbb4-263">Definição</span><span class="sxs-lookup"><span data-stu-id="4dbb4-263">Definition</span></span>

<span data-ttu-id="4dbb4-264">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4dbb4-264">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4dbb4-265">A função localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-265">The function finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="4dbb4-266">Uma palavra-chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-266">A keyword from is found.</span></span>
    
<span data-ttu-id="4dbb4-267">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4dbb4-267">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4dbb4-268">A função localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-268">The function finds content that matches the pattern.</span></span>
    
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

### <a name="keywords"></a><span data-ttu-id="4dbb4-269">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="4dbb4-269">Keywords</span></span>

#### <a name="keywords_ireland_eu_national_id_card"></a><span data-ttu-id="4dbb4-270">Keywords_ireland_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="4dbb4-270">Keywords_ireland_eu_national_id_card</span></span>

<span data-ttu-id="4dbb4-271">número de serviço público pessoal</span><span class="sxs-lookup"><span data-stu-id="4dbb4-271">personal public service number</span></span>
  
<span data-ttu-id="4dbb4-272">PPS não</span><span class="sxs-lookup"><span data-stu-id="4dbb4-272">pps no</span></span>
  
<span data-ttu-id="4dbb4-273">número da receita e do seguro social</span><span class="sxs-lookup"><span data-stu-id="4dbb4-273">revenue and social insurance number</span></span>
  
<span data-ttu-id="4dbb4-274">RSI não</span><span class="sxs-lookup"><span data-stu-id="4dbb4-274">rsi no</span></span>
  
<span data-ttu-id="4dbb4-275">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="4dbb4-275">personal identification number</span></span>
  
<span data-ttu-id="4dbb4-276">identification number</span><span class="sxs-lookup"><span data-stu-id="4dbb4-276">identification number</span></span>
  
<span data-ttu-id="4dbb4-277">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="4dbb4-277">personal id number</span></span>
  
<span data-ttu-id="4dbb4-278">uimhir phearsanta seirbhíse poiblí</span><span class="sxs-lookup"><span data-stu-id="4dbb4-278">uimhir phearsanta seirbhíse poiblí</span></span>
  
<span data-ttu-id="4dbb4-279">uimh.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-279">uimh.</span></span> <span data-ttu-id="4dbb4-280">PSP</span><span class="sxs-lookup"><span data-stu-id="4dbb4-280">psp</span></span>
  
## <a name="italy"></a><span data-ttu-id="4dbb4-281">Itália</span><span class="sxs-lookup"><span data-stu-id="4dbb4-281">Italy</span></span>

### <a name="format"></a><span data-ttu-id="4dbb4-282">Formatar</span><span class="sxs-lookup"><span data-stu-id="4dbb4-282">Format</span></span>

<span data-ttu-id="4dbb4-283">Uma combinação de 16 caracteres de letras e dígitos no padrão especificado</span><span class="sxs-lookup"><span data-stu-id="4dbb4-283">A 16-character combination of letters and digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4dbb4-284">Padrão</span><span class="sxs-lookup"><span data-stu-id="4dbb4-284">Pattern</span></span>

<span data-ttu-id="4dbb4-285">Uma combinação de letras e dígitos de 16 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4dbb4-285">A 16-character combination of letters and digits:</span></span>
  
- <span data-ttu-id="4dbb4-286">Três letras que correspondem às três primeiras consoantes no nome da família</span><span class="sxs-lookup"><span data-stu-id="4dbb4-286">Three letters that correspond to the first three consonants in the family name</span></span>
    
- <span data-ttu-id="4dbb4-287">Três letras que correspondem à primeira, terceira e quarta consoantes no primeiro nome</span><span class="sxs-lookup"><span data-stu-id="4dbb4-287">Three letters that correspond to the first, third, and fourth consonants in the first name</span></span>
    
- <span data-ttu-id="4dbb4-288">Dois dígitos que correspondem aos últimos dígitos do ano de nascimento</span><span class="sxs-lookup"><span data-stu-id="4dbb4-288">Two digits that correspond to the last digits of the birth year</span></span>
    
- <span data-ttu-id="4dbb4-289">Uma letra que corresponde à carta para o mês de nascimento-as letras são usadas em ordem alfabética, mas apenas as letras de a a E, H, L, M, P, R a T são usadas (dessa forma, Janeiro é A e outubro é R)</span><span class="sxs-lookup"><span data-stu-id="4dbb4-289">One letter that corresponds to the letter for the month of birth—letters are used in alphabetical order, but only the letters A to E, H, L, M, P, R to T are used (thus, January is A and October is R)</span></span>
    
- <span data-ttu-id="4dbb4-290">Dois dígitos que correspondem ao dia do mês de nascimento — para diferenciar entre sexos, 40 é adicionado ao dia de nascimento para mulheres</span><span class="sxs-lookup"><span data-stu-id="4dbb4-290">Two digits that correspond to the day of the month of birth—in order to differentiate between genders, 40 is added to the day of birth for women</span></span>
    
- <span data-ttu-id="4dbb4-291">Quatro dígitos que correspondem ao código de área específico do município onde a pessoa nasceu (códigos de todo o país são usados para países estrangeiros)</span><span class="sxs-lookup"><span data-stu-id="4dbb4-291">Four digits that corresponds to the area code specific to the municipality where the person was born (country-wide codes are used for foreign countries)</span></span>
    
- <span data-ttu-id="4dbb4-292">Um dígito de paridade</span><span class="sxs-lookup"><span data-stu-id="4dbb4-292">One parity digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="4dbb4-293">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="4dbb4-293">Checksum</span></span>

<span data-ttu-id="4dbb4-294">Sim</span><span class="sxs-lookup"><span data-stu-id="4dbb4-294">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="4dbb4-295">Definição</span><span class="sxs-lookup"><span data-stu-id="4dbb4-295">Definition</span></span>

<span data-ttu-id="4dbb4-296">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4dbb4-296">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4dbb4-297">A função `Func_italy_eu_national_id_card` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-297">The function  `Func_italy_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4dbb4-298">Uma palavra- `Keywords_italy_eu_national_id_card` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-298">A keyword from  `Keywords_italy_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="4dbb4-299">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4dbb4-299">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4dbb4-300">A função `Func_italy_eu_national_id_card` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-300">The function  `Func_italy_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="4dbb4-301">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="4dbb4-301">Keywords</span></span>

#### <a name="keywords_italy_eu_national_id_card"></a><span data-ttu-id="4dbb4-302">Keywords_italy_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="4dbb4-302">Keywords_italy_eu_national_id_card</span></span>

<span data-ttu-id="4dbb4-303">código pessoal</span><span class="sxs-lookup"><span data-stu-id="4dbb4-303">personal code</span></span>
  
<span data-ttu-id="4dbb4-304">número de código pessoal</span><span class="sxs-lookup"><span data-stu-id="4dbb4-304">personal code number</span></span>
  
<span data-ttu-id="4dbb4-305">número do certificado pessoal</span><span class="sxs-lookup"><span data-stu-id="4dbb4-305">personal certificate number</span></span>
  
<span data-ttu-id="4dbb4-306">código fiscal</span><span class="sxs-lookup"><span data-stu-id="4dbb4-306">fiscal code</span></span>
  
<span data-ttu-id="4dbb4-307">personalcodeno #</span><span class="sxs-lookup"><span data-stu-id="4dbb4-307">personalcodeno#</span></span>
  
<span data-ttu-id="4dbb4-308">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="4dbb4-308">personal id number</span></span>
  
<span data-ttu-id="4dbb4-309">código de ID pessoal</span><span class="sxs-lookup"><span data-stu-id="4dbb4-309">personal id code</span></span>
  
<span data-ttu-id="4dbb4-310">pessoal do Codice</span><span class="sxs-lookup"><span data-stu-id="4dbb4-310">codice personale</span></span>
  
<span data-ttu-id="4dbb4-311">numero certificato pessoal</span><span class="sxs-lookup"><span data-stu-id="4dbb4-311">numero certificato personale</span></span>
  
<span data-ttu-id="4dbb4-312">pessoal do numero</span><span class="sxs-lookup"><span data-stu-id="4dbb4-312">numero personale</span></span>
  
<span data-ttu-id="4dbb4-313">pessoal da ID numero</span><span class="sxs-lookup"><span data-stu-id="4dbb4-313">numero id personale</span></span>
  
<span data-ttu-id="4dbb4-314">pessoal da ID codice</span><span class="sxs-lookup"><span data-stu-id="4dbb4-314">codice id personale</span></span>
  
<span data-ttu-id="4dbb4-315">fiscalização codice</span><span class="sxs-lookup"><span data-stu-id="4dbb4-315">codice fiscale</span></span>
  
## <a name="latvia"></a><span data-ttu-id="4dbb4-316">Letônia</span><span class="sxs-lookup"><span data-stu-id="4dbb4-316">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="4dbb4-317">Formatar</span><span class="sxs-lookup"><span data-stu-id="4dbb4-317">Format</span></span>

<span data-ttu-id="4dbb4-318">11 dígitos e um hífen no formato especificado</span><span class="sxs-lookup"><span data-stu-id="4dbb4-318">11 digits and a hyphen in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4dbb4-319">Padrão</span><span class="sxs-lookup"><span data-stu-id="4dbb4-319">Pattern</span></span>

<span data-ttu-id="4dbb4-320">11 dígitos e um hífen:</span><span class="sxs-lookup"><span data-stu-id="4dbb4-320">11 digits and a hyphen:</span></span>
  
-  <span data-ttu-id="4dbb4-321">Seis dígitos que correspondem à data de nascimento (DDMMAA)</span><span class="sxs-lookup"><span data-stu-id="4dbb4-321">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="4dbb4-322">Um hífen</span><span class="sxs-lookup"><span data-stu-id="4dbb4-322">A hyphen</span></span>
    
- <span data-ttu-id="4dbb4-323">Um dígito que corresponde ao século de nascimento ("0" para o século 19, "1" para o século 20 e "2" para o século 21)</span><span class="sxs-lookup"><span data-stu-id="4dbb4-323">One digit that corresponds to the century of birth ("0" for 19th century, "1" for 20th century, and "2" for 21st century)</span></span>
    
- <span data-ttu-id="4dbb4-324">Quatro dígitos, gerados aleatoriamente</span><span class="sxs-lookup"><span data-stu-id="4dbb4-324">Four digits, randomly generated</span></span>
    
### <a name="checksum"></a><span data-ttu-id="4dbb4-325">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="4dbb4-325">Checksum</span></span>

<span data-ttu-id="4dbb4-326">Sim</span><span class="sxs-lookup"><span data-stu-id="4dbb4-326">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="4dbb4-327">Definição</span><span class="sxs-lookup"><span data-stu-id="4dbb4-327">Definition</span></span>

<span data-ttu-id="4dbb4-328">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4dbb4-328">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4dbb4-329">A função `Func_latvia_eu_national_id_card` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-329">The function  `Func_latvia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4dbb4-330">Uma palavra- `Keywords_latvia_eu_national_id_card` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-330">A keyword from  `Keywords_latvia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="4dbb4-331">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4dbb4-331">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4dbb4-332">A função `Func_latvia_eu_national_id_card` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-332">The function  `Func_latvia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="4dbb4-333">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="4dbb4-333">Keywords</span></span>

#### <a name="keywords_latvia_eu_national_id_card"></a><span data-ttu-id="4dbb4-334">Keywords_latvia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="4dbb4-334">Keywords_latvia_eu_national_id_card</span></span>

<span data-ttu-id="4dbb4-335">código pessoal</span><span class="sxs-lookup"><span data-stu-id="4dbb4-335">personal code</span></span>
  
<span data-ttu-id="4dbb4-336">número de código pessoal</span><span class="sxs-lookup"><span data-stu-id="4dbb4-336">personal code number</span></span>
  
<span data-ttu-id="4dbb4-337">número do certificado pessoal</span><span class="sxs-lookup"><span data-stu-id="4dbb4-337">personal certificate number</span></span>
  
<span data-ttu-id="4dbb4-338">personalcodeno #</span><span class="sxs-lookup"><span data-stu-id="4dbb4-338">personalcodeno#</span></span>
  
<span data-ttu-id="4dbb4-339">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="4dbb4-339">personal id number</span></span>
  
<span data-ttu-id="4dbb4-340">código de ID pessoal</span><span class="sxs-lookup"><span data-stu-id="4dbb4-340">personal id code</span></span>
  
<span data-ttu-id="4dbb4-341">Kods personas</span><span class="sxs-lookup"><span data-stu-id="4dbb4-341">personas kods</span></span>
  
## <a name="lithuania"></a><span data-ttu-id="4dbb4-342">Lituânia</span><span class="sxs-lookup"><span data-stu-id="4dbb4-342">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="4dbb4-343">Formatar</span><span class="sxs-lookup"><span data-stu-id="4dbb4-343">Format</span></span>

<span data-ttu-id="4dbb4-344">11 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="4dbb4-344">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4dbb4-345">Padrão</span><span class="sxs-lookup"><span data-stu-id="4dbb4-345">Pattern</span></span>

<span data-ttu-id="4dbb4-346">11 dígitos sem espaços e delimitadores:</span><span class="sxs-lookup"><span data-stu-id="4dbb4-346">11 digits without spaces and delimiters:</span></span>
  
- <span data-ttu-id="4dbb4-347">Um dígito que corresponde ao sexo da pessoa e ao século de nascimento</span><span class="sxs-lookup"><span data-stu-id="4dbb4-347">One digit that corresponds to the person's gender and century of birth</span></span>
    
-  <span data-ttu-id="4dbb4-348">Seis dígitos que correspondem à data de nascimento (AAMMDD)</span><span class="sxs-lookup"><span data-stu-id="4dbb4-348">Six digits that correspond to birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="4dbb4-349">Três dígitos que correspondem ao número de série da data de nascimento</span><span class="sxs-lookup"><span data-stu-id="4dbb4-349">Three digits that correspond to the serial number of the date of birth</span></span>
    
- <span data-ttu-id="4dbb4-350">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="4dbb4-350">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="4dbb4-351">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="4dbb4-351">Checksum</span></span>

<span data-ttu-id="4dbb4-352">Sim</span><span class="sxs-lookup"><span data-stu-id="4dbb4-352">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="4dbb4-353">Definição</span><span class="sxs-lookup"><span data-stu-id="4dbb4-353">Definition</span></span>

<span data-ttu-id="4dbb4-354">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4dbb4-354">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4dbb4-355">A função `Func_lithuania_eu_national_id_card` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-355">The function  `Func_lithuania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4dbb4-356">Uma palavra- `Keywords_lithuania_eu_national_id_card` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-356">A keyword from  `Keywords_lithuania_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="4dbb4-357">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4dbb4-357">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4dbb4-358">A função `Func_lithuania_eu_national_id_card` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-358">The function  `Func_lithuania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="4dbb4-359">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="4dbb4-359">Keywords</span></span>

#### <a name="keywords_lithuania_eu_national_id_card"></a><span data-ttu-id="4dbb4-360">Keywords_lithuania_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="4dbb4-360">Keywords_lithuania_eu_national_id_card</span></span>

<span data-ttu-id="4dbb4-361">código numérico pessoal</span><span class="sxs-lookup"><span data-stu-id="4dbb4-361">personal numeric code</span></span>
  
<span data-ttu-id="4dbb4-362">número de identificação exclusivo</span><span class="sxs-lookup"><span data-stu-id="4dbb4-362">unique identification number</span></span>
  
<span data-ttu-id="4dbb4-363">número do serviço do cidadão</span><span class="sxs-lookup"><span data-stu-id="4dbb4-363">citizen service number</span></span>
  
<span data-ttu-id="4dbb4-364">número de identidade exclusivo</span><span class="sxs-lookup"><span data-stu-id="4dbb4-364">unique identity number</span></span>
  
<span data-ttu-id="4dbb4-365">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="4dbb4-365">uniqueidentityno#</span></span>
  
<span data-ttu-id="4dbb4-366">código pessoal.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-366">personal code.</span></span>
  
<span data-ttu-id="4dbb4-367">asmeninis skaitmeninis kodas</span><span class="sxs-lookup"><span data-stu-id="4dbb4-367">asmeninis skaitmeninis kodas</span></span>
  
<span data-ttu-id="4dbb4-368">unikalus identifikavimo numeris</span><span class="sxs-lookup"><span data-stu-id="4dbb4-368">unikalus identifikavimo numeris</span></span>
  
<span data-ttu-id="4dbb4-369">piliečio paslaugos numeris</span><span class="sxs-lookup"><span data-stu-id="4dbb4-369">piliečio paslaugos numeris</span></span>
  
<span data-ttu-id="4dbb4-370">unikalus identifikavimo kodas</span><span class="sxs-lookup"><span data-stu-id="4dbb4-370">unikalus identifikavimo kodas</span></span>
  
<span data-ttu-id="4dbb4-371">kodas.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-371">asmens kodas.</span></span>
  
## <a name="luxemburg"></a><span data-ttu-id="4dbb4-372">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="4dbb4-372">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="4dbb4-373">Formatar</span><span class="sxs-lookup"><span data-stu-id="4dbb4-373">Format</span></span>

<span data-ttu-id="4dbb4-374">11 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="4dbb4-374">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4dbb4-375">Padrão</span><span class="sxs-lookup"><span data-stu-id="4dbb4-375">Pattern</span></span>

<span data-ttu-id="4dbb4-376">11 dígitos</span><span class="sxs-lookup"><span data-stu-id="4dbb4-376">11 digits</span></span>
  
- <span data-ttu-id="4dbb4-377">Um dígito que corresponde ao sexo da pessoa e ao século de nascimento</span><span class="sxs-lookup"><span data-stu-id="4dbb4-377">One digit that corresponds to the person's gender and century of birth</span></span>
    
-  <span data-ttu-id="4dbb4-378">Seis dígitos que correspondem à data de nascimento (AAMMDD)</span><span class="sxs-lookup"><span data-stu-id="4dbb4-378">Six digits that correspond to birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="4dbb4-379">Três dígitos que correspondem ao número de série da data de nascimento</span><span class="sxs-lookup"><span data-stu-id="4dbb4-379">Three digits that correspond to the serial number of the date of birth</span></span>
    
- <span data-ttu-id="4dbb4-380">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="4dbb4-380">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="4dbb4-381">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="4dbb4-381">Checksum</span></span>

<span data-ttu-id="4dbb4-382">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="4dbb4-382">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="4dbb4-383">Definição</span><span class="sxs-lookup"><span data-stu-id="4dbb4-383">Definition</span></span>

<span data-ttu-id="4dbb4-384">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4dbb4-384">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4dbb4-385">A expressão `Regex_luxemburg_eu_national_id_card` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-385">The regular expression  `Regex_luxemburg_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4dbb4-386">Uma palavra- `Keywords_luxemburg_eu_national_id_card` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-386">A keyword from  `Keywords_luxemburg_eu_national_id_card` is found.</span></span> 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_national_id_card" />
          <Match idRef="Keywords_luxemburg_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4dbb4-387">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="4dbb4-387">Keywords</span></span>

#### <a name="keywords_luxemburg_eu_national_id_card"></a><span data-ttu-id="4dbb4-388">Keywords_luxemburg_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="4dbb4-388">Keywords_luxemburg_eu_national_id_card</span></span>

<span data-ttu-id="4dbb4-389">ID pessoal</span><span class="sxs-lookup"><span data-stu-id="4dbb4-389">personal id</span></span>
  
<span data-ttu-id="4dbb4-390">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="4dbb4-390">personal id number</span></span>
  
<span data-ttu-id="4dbb4-391">personalidno #</span><span class="sxs-lookup"><span data-stu-id="4dbb4-391">personalidno#</span></span>
  
<span data-ttu-id="4dbb4-392">número de identificação exclusivo</span><span class="sxs-lookup"><span data-stu-id="4dbb4-392">unique id number</span></span>
  
<span data-ttu-id="4dbb4-393">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="4dbb4-393">personalidnumber#</span></span>
  
<span data-ttu-id="4dbb4-394">chave de ID exclusiva</span><span class="sxs-lookup"><span data-stu-id="4dbb4-394">unique id key</span></span>
  
<span data-ttu-id="4dbb4-395">código de ID pessoal</span><span class="sxs-lookup"><span data-stu-id="4dbb4-395">personal id code</span></span>
  
<span data-ttu-id="4dbb4-396">uniqueidkey #</span><span class="sxs-lookup"><span data-stu-id="4dbb4-396">uniqueidkey#</span></span>
  
<span data-ttu-id="4dbb4-397">código individual</span><span class="sxs-lookup"><span data-stu-id="4dbb4-397">individual code</span></span>
  
<span data-ttu-id="4dbb4-398">ID individual</span><span class="sxs-lookup"><span data-stu-id="4dbb4-398">individual id</span></span>
  
<span data-ttu-id="4dbb4-399">ID eindeutige-Nummer</span><span class="sxs-lookup"><span data-stu-id="4dbb4-399">eindeutige id-nummer</span></span>
  
<span data-ttu-id="4dbb4-400">ID eindeutige</span><span class="sxs-lookup"><span data-stu-id="4dbb4-400">eindeutige id</span></span>
  
<span data-ttu-id="4dbb4-401">ID personnelle</span><span class="sxs-lookup"><span data-stu-id="4dbb4-401">id personnelle</span></span>
  
<span data-ttu-id="4dbb4-402">Numéro d'identification</span><span class="sxs-lookup"><span data-stu-id="4dbb4-402">numéro d'identification personnel</span></span>
  
<span data-ttu-id="4dbb4-403">idpersonnelle #</span><span class="sxs-lookup"><span data-stu-id="4dbb4-403">idpersonnelle#</span></span>
  
<span data-ttu-id="4dbb4-404">persönliche identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="4dbb4-404">persönliche identifikationsnummer</span></span>
  
<span data-ttu-id="4dbb4-405">eindeutigeid #</span><span class="sxs-lookup"><span data-stu-id="4dbb4-405">eindeutigeid#</span></span>
  
## <a name="malta"></a><span data-ttu-id="4dbb4-406">Malta</span><span class="sxs-lookup"><span data-stu-id="4dbb4-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="4dbb4-407">Formatar</span><span class="sxs-lookup"><span data-stu-id="4dbb4-407">Format</span></span>

<span data-ttu-id="4dbb4-408">Sete dígitos seguidos de uma letra</span><span class="sxs-lookup"><span data-stu-id="4dbb4-408">Seven digits followed by one letter</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4dbb4-409">Padrão</span><span class="sxs-lookup"><span data-stu-id="4dbb4-409">Pattern</span></span>

<span data-ttu-id="4dbb4-410">Sete dígitos seguidos de uma letra:</span><span class="sxs-lookup"><span data-stu-id="4dbb4-410">Seven digits followed by one letter:</span></span>
  
-  <span data-ttu-id="4dbb4-411">Sete dígitos </span><span class="sxs-lookup"><span data-stu-id="4dbb4-411">Seven digits</span></span> 
    
- <span data-ttu-id="4dbb4-412">Uma letra maiúscula (diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="4dbb4-412">One uppercase letter (case sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="4dbb4-413">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="4dbb4-413">Checksum</span></span>

<span data-ttu-id="4dbb4-414">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="4dbb4-414">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="4dbb4-415">Definição</span><span class="sxs-lookup"><span data-stu-id="4dbb4-415">Definition</span></span>

<span data-ttu-id="4dbb4-416">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4dbb4-416">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4dbb4-417">A expressão `Regex_malta_eu_national_id_card` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-417">The regular expression  `Regex_malta_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4dbb4-418">Uma palavra- `Keywords_malta_eu_national_id_card` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-418">A keyword from  `Keywords_malta_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="4dbb4-419">Uma política de DLP tem 65% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4dbb4-419">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4dbb4-420">A expressão `Regex_malta_eu_national_id_card` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-420">The regular expression  `Regex_malta_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="4dbb4-421">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="4dbb4-421">Keywords</span></span>

#### <a name="keywords_malta_eu_national_id_card"></a><span data-ttu-id="4dbb4-422">Keywords_malta_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="4dbb4-422">Keywords_malta_eu_national_id_card</span></span>

<span data-ttu-id="4dbb4-423">código numérico pessoal</span><span class="sxs-lookup"><span data-stu-id="4dbb4-423">personal numeric code</span></span>
  
<span data-ttu-id="4dbb4-424">número de identificação exclusivo</span><span class="sxs-lookup"><span data-stu-id="4dbb4-424">unique identification number</span></span>
  
<span data-ttu-id="4dbb4-425">número do serviço do cidadão</span><span class="sxs-lookup"><span data-stu-id="4dbb4-425">citizen service number</span></span>
  
<span data-ttu-id="4dbb4-426">número de identidade exclusivo</span><span class="sxs-lookup"><span data-stu-id="4dbb4-426">unique identity number</span></span>
  
<span data-ttu-id="4dbb4-427">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="4dbb4-427">uniqueidentityno#</span></span>
  
<span data-ttu-id="4dbb4-428">Kodiċi numerali pessoali</span><span class="sxs-lookup"><span data-stu-id="4dbb4-428">kodiċi numerali personali</span></span>
  
<span data-ttu-id="4dbb4-429">numru ta ' identifikazzjoni uniku</span><span class="sxs-lookup"><span data-stu-id="4dbb4-429">numru ta 'identifikazzjoni uniku</span></span>
  
<span data-ttu-id="4dbb4-430">numru tas-servizz taċ-ċittadin</span><span class="sxs-lookup"><span data-stu-id="4dbb4-430">numru tas-servizz taċ-ċittadin</span></span>
  
<span data-ttu-id="4dbb4-431">numru ta ' Identità uniku</span><span class="sxs-lookup"><span data-stu-id="4dbb4-431">numru ta' identità uniku</span></span>
  
## <a name="netherlands"></a><span data-ttu-id="4dbb4-432">Países Baixos</span><span class="sxs-lookup"><span data-stu-id="4dbb4-432">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="4dbb4-433">Formatar</span><span class="sxs-lookup"><span data-stu-id="4dbb4-433">Format</span></span>

<span data-ttu-id="4dbb4-434">Nove dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="4dbb4-434">Nine digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4dbb4-435">Padrão</span><span class="sxs-lookup"><span data-stu-id="4dbb4-435">Pattern</span></span>

<span data-ttu-id="4dbb4-436">Nove dígitos</span><span class="sxs-lookup"><span data-stu-id="4dbb4-436">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="4dbb4-437">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="4dbb4-437">Checksum</span></span>

<span data-ttu-id="4dbb4-438">Sim</span><span class="sxs-lookup"><span data-stu-id="4dbb4-438">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="4dbb4-439">Definição</span><span class="sxs-lookup"><span data-stu-id="4dbb4-439">Definition</span></span>

<span data-ttu-id="4dbb4-440">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4dbb4-440">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4dbb4-441">A função `Func_netherlands_eu_national_id_card` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-441">The function  `Func_netherlands_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4dbb4-442">Uma palavra-chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-442">A keyword from is found.</span></span>
    
<span data-ttu-id="4dbb4-443">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4dbb4-443">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4dbb4-444">A função `Func_netherlands_eu_national_id_card` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-444">The function  `Func_netherlands_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="4dbb4-445">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="4dbb4-445">Keywords</span></span>

#### <a name="keywords_netherlands_eu_national_id_card"></a><span data-ttu-id="4dbb4-446">Keywords_netherlands_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="4dbb4-446">Keywords_netherlands_eu_national_id_card</span></span>

<span data-ttu-id="4dbb4-447">código numérico pessoal</span><span class="sxs-lookup"><span data-stu-id="4dbb4-447">personal numeric code</span></span>
  
<span data-ttu-id="4dbb4-448">número de identificação exclusivo</span><span class="sxs-lookup"><span data-stu-id="4dbb4-448">unique identification number</span></span>
  
<span data-ttu-id="4dbb4-449">número do serviço do cidadão</span><span class="sxs-lookup"><span data-stu-id="4dbb4-449">citizen service number</span></span>
  
<span data-ttu-id="4dbb4-450">número de identidade exclusivo</span><span class="sxs-lookup"><span data-stu-id="4dbb4-450">unique identity number</span></span>
  
<span data-ttu-id="4dbb4-451">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="4dbb4-451">uniqueidentityno#</span></span>
  
<span data-ttu-id="4dbb4-452">BSN</span><span class="sxs-lookup"><span data-stu-id="4dbb4-452">bsn</span></span>
  
<span data-ttu-id="4dbb4-453">BSN #</span><span class="sxs-lookup"><span data-stu-id="4dbb4-453">bsn#</span></span>
  
<span data-ttu-id="4dbb4-454">código de numerieke persoonlijke</span><span class="sxs-lookup"><span data-stu-id="4dbb4-454">persoonlijke numerieke code</span></span>
  
<span data-ttu-id="4dbb4-455">uniek identificatienummer</span><span class="sxs-lookup"><span data-stu-id="4dbb4-455">uniek identificatienummer</span></span>
  
<span data-ttu-id="4dbb4-456">burgerservicenummer</span><span class="sxs-lookup"><span data-stu-id="4dbb4-456">burgerservicenummer</span></span>
  
<span data-ttu-id="4dbb4-457">uniek identiteitsnummer</span><span class="sxs-lookup"><span data-stu-id="4dbb4-457">uniek identiteitsnummer</span></span>
  
## <a name="poland"></a><span data-ttu-id="4dbb4-458">Polônia</span><span class="sxs-lookup"><span data-stu-id="4dbb4-458">Poland</span></span>

<span data-ttu-id="4dbb4-459">Para obter detalhes, consulte a seção "ID nacional da Polônia (PESEL)" em [que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="4dbb4-459">For details, see the section "Poland National ID (PESEL)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="4dbb4-460">Portugal</span><span class="sxs-lookup"><span data-stu-id="4dbb4-460">Portugal</span></span>

<span data-ttu-id="4dbb4-461">Para obter detalhes, consulte a seção "número de cartão de cidadão da Portugal" em [o que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="4dbb4-461">For details, see the section "Portugal Citizen Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="romania"></a><span data-ttu-id="4dbb4-462">Romênia</span><span class="sxs-lookup"><span data-stu-id="4dbb4-462">Romania</span></span>

### <a name="format"></a><span data-ttu-id="4dbb4-463">Formatar</span><span class="sxs-lookup"><span data-stu-id="4dbb4-463">Format</span></span>

<span data-ttu-id="4dbb4-464">13 dígitos sem espaços e delimitadores</span><span class="sxs-lookup"><span data-stu-id="4dbb4-464">13 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4dbb4-465">Padrão</span><span class="sxs-lookup"><span data-stu-id="4dbb4-465">Pattern</span></span>

<span data-ttu-id="4dbb4-466">13 dígitos</span><span class="sxs-lookup"><span data-stu-id="4dbb4-466">13 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="4dbb4-467">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="4dbb4-467">Checksum</span></span>

<span data-ttu-id="4dbb4-468">Sim</span><span class="sxs-lookup"><span data-stu-id="4dbb4-468">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="4dbb4-469">Definição</span><span class="sxs-lookup"><span data-stu-id="4dbb4-469">Definition</span></span>

<span data-ttu-id="4dbb4-470">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4dbb4-470">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4dbb4-471">A função `Func_romania_eu_national_id_card` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-471">The function  `Func_romania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4dbb4-472">Uma palavra- `Keywords_romania_eu_national_id_card` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-472">A keyword from  `Keywords_romania_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="4dbb4-473">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4dbb4-473">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4dbb4-474">A função `Func_romania_eu_national_id_card` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-474">The function  `Func_romania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="4dbb4-475">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="4dbb4-475">Keywords</span></span>

#### <a name="keywords_romania_eu_national_id_card"></a><span data-ttu-id="4dbb4-476">Keywords_romania_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="4dbb4-476">Keywords_romania_eu_national_id_card</span></span>

<span data-ttu-id="4dbb4-477">código numérico pessoal</span><span class="sxs-lookup"><span data-stu-id="4dbb4-477">personal numeric code</span></span>
  
<span data-ttu-id="4dbb4-478">número de identificação exclusivo</span><span class="sxs-lookup"><span data-stu-id="4dbb4-478">unique identification number</span></span>
  
<span data-ttu-id="4dbb4-479">cnp</span><span class="sxs-lookup"><span data-stu-id="4dbb4-479">cnp</span></span>
  
<span data-ttu-id="4dbb4-480">cnp #</span><span class="sxs-lookup"><span data-stu-id="4dbb4-480">cnp#</span></span>
  
<span data-ttu-id="4dbb4-481">pessoal</span><span class="sxs-lookup"><span data-stu-id="4dbb4-481">pin</span></span>
  
<span data-ttu-id="4dbb4-482">pessoal #</span><span class="sxs-lookup"><span data-stu-id="4dbb4-482">pin#</span></span>
  
<span data-ttu-id="4dbb4-483">número de seguro</span><span class="sxs-lookup"><span data-stu-id="4dbb4-483">insurance number</span></span>
  
<span data-ttu-id="4dbb4-484">insurancenumber #</span><span class="sxs-lookup"><span data-stu-id="4dbb4-484">insurancenumber#</span></span>
  
<span data-ttu-id="4dbb4-485">número de identidade exclusivo</span><span class="sxs-lookup"><span data-stu-id="4dbb4-485">unique identity number</span></span>
  
<span data-ttu-id="4dbb4-486">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="4dbb4-486">uniqueidentityno#</span></span>
  
<span data-ttu-id="4dbb4-487">c.o.d. numérico pessoal</span><span class="sxs-lookup"><span data-stu-id="4dbb4-487">cod numeric personal</span></span>
  
<span data-ttu-id="4dbb4-488">identificare de c.o.d. pessoal</span><span class="sxs-lookup"><span data-stu-id="4dbb4-488">cod identificare personal</span></span>
  
<span data-ttu-id="4dbb4-489">UNIC de c.o.d. identificare</span><span class="sxs-lookup"><span data-stu-id="4dbb4-489">cod unic identificare</span></span>
  
<span data-ttu-id="4dbb4-490">număr pessoal do UNIC</span><span class="sxs-lookup"><span data-stu-id="4dbb4-490">număr personal unic</span></span>
  
<span data-ttu-id="4dbb4-491">număr identitate</span><span class="sxs-lookup"><span data-stu-id="4dbb4-491">număr identitate</span></span>
  
<span data-ttu-id="4dbb4-492">număr identificare pessoal</span><span class="sxs-lookup"><span data-stu-id="4dbb4-492">număr identificare personal</span></span>
  
<span data-ttu-id="4dbb4-493">număridentitate #</span><span class="sxs-lookup"><span data-stu-id="4dbb4-493">număridentitate#</span></span>
  
<span data-ttu-id="4dbb4-494">codnumericpersonal #</span><span class="sxs-lookup"><span data-stu-id="4dbb4-494">codnumericpersonal#</span></span>
  
<span data-ttu-id="4dbb4-495">numărpersonalunic #</span><span class="sxs-lookup"><span data-stu-id="4dbb4-495">numărpersonalunic#</span></span>
  
## <a name="slovakia"></a><span data-ttu-id="4dbb4-496">Eslováquia</span><span class="sxs-lookup"><span data-stu-id="4dbb4-496">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="4dbb4-497">Formatar</span><span class="sxs-lookup"><span data-stu-id="4dbb4-497">Format</span></span>

<span data-ttu-id="4dbb4-498">Dez dígitos contendo uma barra invertida</span><span class="sxs-lookup"><span data-stu-id="4dbb4-498">Ten digits containing one backslash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4dbb4-499">Padrão</span><span class="sxs-lookup"><span data-stu-id="4dbb4-499">Pattern</span></span>

<span data-ttu-id="4dbb4-500">Dez dígitos contendo uma barra invertida:</span><span class="sxs-lookup"><span data-stu-id="4dbb4-500">Ten digits containing one backslash:</span></span>
  
### <a name="checksum"></a><span data-ttu-id="4dbb4-501">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="4dbb4-501">Checksum</span></span>

<span data-ttu-id="4dbb4-502">Sim</span><span class="sxs-lookup"><span data-stu-id="4dbb4-502">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="4dbb4-503">Definição</span><span class="sxs-lookup"><span data-stu-id="4dbb4-503">Definition</span></span>

<span data-ttu-id="4dbb4-504">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4dbb4-504">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4dbb4-505">A função `Func_slovakia_eu_national_id_card` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-505">The function  `Func_slovakia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4dbb4-506">Uma palavra- `Keywords_slovakia_eu_national_id_card` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-506">A keyword from  `Keywords_slovakia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="4dbb4-507">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4dbb4-507">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4dbb4-508">A função `Func_slovakia_eu_national_id_card` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-508">The function  `Func_slovakia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="4dbb4-509">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="4dbb4-509">Keywords</span></span>

#### <a name="keywords_slovakia_eu_national_id_card"></a><span data-ttu-id="4dbb4-510">Keywords_slovakia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="4dbb4-510">Keywords_slovakia_eu_national_id_card</span></span>

<span data-ttu-id="4dbb4-511">número de nascimento</span><span class="sxs-lookup"><span data-stu-id="4dbb4-511">birth number</span></span>
  
<span data-ttu-id="4dbb4-512">national identification number</span><span class="sxs-lookup"><span data-stu-id="4dbb4-512">national identification number</span></span>
  
<span data-ttu-id="4dbb4-513">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="4dbb4-513">personal identification number</span></span>
  
<span data-ttu-id="4dbb4-514">social security number</span><span class="sxs-lookup"><span data-stu-id="4dbb4-514">social security number</span></span>
  
<span data-ttu-id="4dbb4-515">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="4dbb4-515">nationalnumber#</span></span>
  
<span data-ttu-id="4dbb4-516">es #</span><span class="sxs-lookup"><span data-stu-id="4dbb4-516">ssn#</span></span>
  
<span data-ttu-id="4dbb4-517">es</span><span class="sxs-lookup"><span data-stu-id="4dbb4-517">ssn</span></span>
  
<span data-ttu-id="4dbb4-518">número nacional</span><span class="sxs-lookup"><span data-stu-id="4dbb4-518">national number</span></span>
  
<span data-ttu-id="4dbb4-519">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="4dbb4-519">personal id number</span></span>
  
<span data-ttu-id="4dbb4-520">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="4dbb4-520">personalidnumber#</span></span>
  
<span data-ttu-id="4dbb4-521">rč</span><span class="sxs-lookup"><span data-stu-id="4dbb4-521">rč</span></span>
  
<span data-ttu-id="4dbb4-522">rodné číslo</span><span class="sxs-lookup"><span data-stu-id="4dbb4-522">rodné číslo</span></span>
  
<span data-ttu-id="4dbb4-523">rodne cislo</span><span class="sxs-lookup"><span data-stu-id="4dbb4-523">rodne cislo</span></span>
  
## <a name="slovenia"></a><span data-ttu-id="4dbb4-524">Eslovênia</span><span class="sxs-lookup"><span data-stu-id="4dbb4-524">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="4dbb4-525">Formatar</span><span class="sxs-lookup"><span data-stu-id="4dbb4-525">Format</span></span>

<span data-ttu-id="4dbb4-526">13 dígitos sem espaços ou delimitadores</span><span class="sxs-lookup"><span data-stu-id="4dbb4-526">13 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4dbb4-527">Padrão</span><span class="sxs-lookup"><span data-stu-id="4dbb4-527">Pattern</span></span>

<span data-ttu-id="4dbb4-528">13 dígitos no padrão especificado:</span><span class="sxs-lookup"><span data-stu-id="4dbb4-528">13 digits in the specified pattern:</span></span>
  
-  <span data-ttu-id="4dbb4-529">Sete dígitos que correspondem à data de nascimento (DDMMLLL), onde "LLL" corresponde aos últimos três dígitos do ano de nascimento</span><span class="sxs-lookup"><span data-stu-id="4dbb4-529">Seven digits that correspond to the birth date (DDMMLLL) where "LLL" corresponds to the last three digits of the birth year</span></span> 
    
- <span data-ttu-id="4dbb4-530">Dois dígitos que correspondem à área de nascimento</span><span class="sxs-lookup"><span data-stu-id="4dbb4-530">Two digits that correspond to the area of birth</span></span>
    
- <span data-ttu-id="4dbb4-531">Três dígitos que correspondem a uma combinação de sexo e número de série para pessoas nasceu no mesmo dia (000-499 para macho e 500-999 para fêmea)</span><span class="sxs-lookup"><span data-stu-id="4dbb4-531">Three digits that correspond to a combination of gender and serial number for persons born on the same day (000-499 for male and 500-999 for female)</span></span>
    
- <span data-ttu-id="4dbb4-532">Um dígito de verificação</span><span class="sxs-lookup"><span data-stu-id="4dbb4-532">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="4dbb4-533">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="4dbb4-533">Checksum</span></span>

<span data-ttu-id="4dbb4-534">Sim</span><span class="sxs-lookup"><span data-stu-id="4dbb4-534">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="4dbb4-535">Definição</span><span class="sxs-lookup"><span data-stu-id="4dbb4-535">Definition</span></span>

<span data-ttu-id="4dbb4-536">Uma política de DLP tem 85% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4dbb4-536">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4dbb4-537">A função `Func_slovenia_eu_national_id_card` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-537">The function  `Func_slovenia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4dbb4-538">Uma palavra- `Keywords_slovenia_eu_national_id_card` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-538">A keyword from  `Keywords_slovenia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="4dbb4-539">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4dbb4-539">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4dbb4-540">A função `Func_slovenia_eu_national_id_card` localiza conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-540">The function  `Func_slovenia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="4dbb4-541">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="4dbb4-541">Keywords</span></span>

#### <a name="keywords_slovenia_eu_national_id_card"></a><span data-ttu-id="4dbb4-542">Keywords_slovenia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="4dbb4-542">Keywords_slovenia_eu_national_id_card</span></span>

<span data-ttu-id="4dbb4-543">código numérico pessoal</span><span class="sxs-lookup"><span data-stu-id="4dbb4-543">personal numeric code</span></span>
  
<span data-ttu-id="4dbb4-544">número de identificação exclusivo</span><span class="sxs-lookup"><span data-stu-id="4dbb4-544">unique identification number</span></span>
  
<span data-ttu-id="4dbb4-545">número de registro exclusivo</span><span class="sxs-lookup"><span data-stu-id="4dbb4-545">unique registration number</span></span>
  
<span data-ttu-id="4dbb4-546">número de identidade exclusivo</span><span class="sxs-lookup"><span data-stu-id="4dbb4-546">unique identity number</span></span>
  
<span data-ttu-id="4dbb4-547">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="4dbb4-547">uniqueidentityno#</span></span>
  
<span data-ttu-id="4dbb4-548">número de cidadão mestre exclusivo</span><span class="sxs-lookup"><span data-stu-id="4dbb4-548">unique master citizen number</span></span>
  
<span data-ttu-id="4dbb4-549">edinstvena identifikacijska številka</span><span class="sxs-lookup"><span data-stu-id="4dbb4-549">edinstvena identifikacijska številka</span></span>
  
<span data-ttu-id="4dbb4-550">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="4dbb4-550">uniqueidentityno #</span></span>
  
<span data-ttu-id="4dbb4-551">edinstvena številka glavnega državljana</span><span class="sxs-lookup"><span data-stu-id="4dbb4-551">edinstvena številka glavnega državljana</span></span>
  
<span data-ttu-id="4dbb4-552">emšo</span><span class="sxs-lookup"><span data-stu-id="4dbb4-552">emšo</span></span>
  
## <a name="spain"></a><span data-ttu-id="4dbb4-553">Espanha</span><span class="sxs-lookup"><span data-stu-id="4dbb4-553">Spain</span></span>

### <a name="format"></a><span data-ttu-id="4dbb4-554">Formatar</span><span class="sxs-lookup"><span data-stu-id="4dbb4-554">Format</span></span>

<span data-ttu-id="4dbb4-555">Oito dígitos seguidos de um caractere</span><span class="sxs-lookup"><span data-stu-id="4dbb4-555">Eight digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="4dbb4-556">Padrão</span><span class="sxs-lookup"><span data-stu-id="4dbb4-556">Pattern</span></span>

<span data-ttu-id="4dbb4-557">Oito dígitos seguidos de um caractere</span><span class="sxs-lookup"><span data-stu-id="4dbb4-557">Eight digits followed by one character</span></span>
  
- <span data-ttu-id="4dbb4-558">Oito dígitos</span><span class="sxs-lookup"><span data-stu-id="4dbb4-558">Eight digits</span></span>
    
- <span data-ttu-id="4dbb4-559">Um dígito ou letra (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="4dbb4-559">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="4dbb4-560">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="4dbb4-560">Checksum</span></span>

<span data-ttu-id="4dbb4-561">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="4dbb4-561">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="4dbb4-562">Definição</span><span class="sxs-lookup"><span data-stu-id="4dbb4-562">Definition</span></span>

<span data-ttu-id="4dbb4-563">Uma política de DLP tem 75% de certeza de que ela detectou este tipo de informação confidencial se, dentro de uma proximidade de 300 caracteres:</span><span class="sxs-lookup"><span data-stu-id="4dbb4-563">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="4dbb4-564">A expressão `Regex_spain_eu_national_id_card` regular localiza o conteúdo que corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-564">The regular expression  `Regex_spain_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="4dbb4-565">Uma palavra- `Keywords_spain_eu_national_id_card"` chave de foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="4dbb4-565">A keyword from  `Keywords_spain_eu_national_id_card"` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_national_id_card" />
          <Match idRef="Keywords_spain_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="4dbb4-566">Palavras-chave</span><span class="sxs-lookup"><span data-stu-id="4dbb4-566">Keywords</span></span>

#### <a name="keywords_spain_eu_national_id_card"></a><span data-ttu-id="4dbb4-567">Keywords_spain_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="4dbb4-567">Keywords_spain_eu_national_id_card</span></span>

<span data-ttu-id="4dbb4-568">dni</span><span class="sxs-lookup"><span data-stu-id="4dbb4-568">dni</span></span>
  
<span data-ttu-id="4dbb4-569">national identification number</span><span class="sxs-lookup"><span data-stu-id="4dbb4-569">national identification number</span></span>
  
<span data-ttu-id="4dbb4-570">número de identidade nacional</span><span class="sxs-lookup"><span data-stu-id="4dbb4-570">national identity number</span></span>
  
<span data-ttu-id="4dbb4-571">número de seguro</span><span class="sxs-lookup"><span data-stu-id="4dbb4-571">insurance number</span></span>
  
<span data-ttu-id="4dbb4-572">número de identificação pessoal</span><span class="sxs-lookup"><span data-stu-id="4dbb4-572">personal identification number</span></span>
  
<span data-ttu-id="4dbb4-573">identidade nacional</span><span class="sxs-lookup"><span data-stu-id="4dbb4-573">national identity</span></span>
  
<span data-ttu-id="4dbb4-574">identidade pessoal não</span><span class="sxs-lookup"><span data-stu-id="4dbb4-574">personal identity no</span></span>
  
<span data-ttu-id="4dbb4-575">número de identidade exclusivo</span><span class="sxs-lookup"><span data-stu-id="4dbb4-575">unique identity number</span></span>
  
<span data-ttu-id="4dbb4-576">nationalidno #</span><span class="sxs-lookup"><span data-stu-id="4dbb4-576">nationalidno#</span></span>
  
<span data-ttu-id="4dbb4-577">UniqueId #</span><span class="sxs-lookup"><span data-stu-id="4dbb4-577">uniqueid#</span></span>
  
<span data-ttu-id="4dbb4-578">dni #</span><span class="sxs-lookup"><span data-stu-id="4dbb4-578">dni#</span></span>
  
<span data-ttu-id="4dbb4-579">nationalid #</span><span class="sxs-lookup"><span data-stu-id="4dbb4-579">nationalid#</span></span>
  
<span data-ttu-id="4dbb4-580">nie #</span><span class="sxs-lookup"><span data-stu-id="4dbb4-580">nie#</span></span>
  
<span data-ttu-id="4dbb4-581">nie</span><span class="sxs-lookup"><span data-stu-id="4dbb4-581">nie</span></span>
  
<span data-ttu-id="4dbb4-582">nienúmero #</span><span class="sxs-lookup"><span data-stu-id="4dbb4-582">nienúmero#</span></span>
  
<span data-ttu-id="4dbb4-583">Nie número</span><span class="sxs-lookup"><span data-stu-id="4dbb4-583">nie número</span></span>
  
<span data-ttu-id="4dbb4-584">documento nacional de Identidad</span><span class="sxs-lookup"><span data-stu-id="4dbb4-584">documento nacional de identidad</span></span>
  
<span data-ttu-id="4dbb4-585">identidad único</span><span class="sxs-lookup"><span data-stu-id="4dbb4-585">identidad único</span></span>
  
<span data-ttu-id="4dbb4-586">número nacional identidad</span><span class="sxs-lookup"><span data-stu-id="4dbb4-586">número nacional identidad</span></span>
  
<span data-ttu-id="4dbb4-587">DNI número</span><span class="sxs-lookup"><span data-stu-id="4dbb4-587">dni número</span></span>
  
<span data-ttu-id="4dbb4-588">dninúmero #</span><span class="sxs-lookup"><span data-stu-id="4dbb4-588">dninúmero#</span></span>
  
<span data-ttu-id="4dbb4-589">identidadúnico #</span><span class="sxs-lookup"><span data-stu-id="4dbb4-589">identidadúnico#</span></span>
  
## <a name="sweden"></a><span data-ttu-id="4dbb4-590">Suécia</span><span class="sxs-lookup"><span data-stu-id="4dbb4-590">Sweden</span></span>

<span data-ttu-id="4dbb4-591">Para obter detalhes, consulte a seção "ID nacional da Suécia" em [o que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="4dbb4-591">For details, see the section "Sweden National ID" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4dbb4-592">Confira também</span><span class="sxs-lookup"><span data-stu-id="4dbb4-592">See also</span></span>

[<span data-ttu-id="4dbb4-593">O que os tipos de informações confidenciais procuram</span><span class="sxs-lookup"><span data-stu-id="4dbb4-593">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)


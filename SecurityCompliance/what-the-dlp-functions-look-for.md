---
title: O que as funções DLP procuram
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/18/2016
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 94349ed4-5351-4ee2-bbda-70813c9ed693
description: Os tipos de informações confidenciais procure por um padrão específico e corroborá-lo assegurando formatação apropriada, aplicando somas de verificação e procurando por palavras-chave relevantes ou outras informações. Alguns dessa funcionalidade é realizada pelas funções internas. Este tópico explica o que essas funções procuram, para ajudá-lo a entender como os tipos de informações confidenciais predefinidos funcionam.
ms.openlocfilehash: 510f98e2b4e1d2480550f11026cf445be6ffc931
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "23013755"
---
# <a name="what-the-dlp-functions-look-for"></a><span data-ttu-id="40677-105">O que as funções DLP procuram</span><span class="sxs-lookup"><span data-stu-id="40677-105">What the DLP functions look for</span></span>

<span data-ttu-id="40677-p102">A política DLP inclui tipos de informação confidencial, como números de cartão de crédito e de cartão de débito da UE (União Europeia), que estão prontos para uso em suas políticas DLP. Esses tipos de informação confidencial procuram por um padrão específico e o confirmam, garantindo a formatação adequada, impondo as somas de verificação e procurando palavras-chave relevantes ou outras informações. Algumas dessas funcionalidades são realizadas por funções internas. Por exemplo, o tipo de informação confidencial de Número de Cartão de Crédito usa uma função para procurar datas formatadas como uma data de expiração, para ajudar a corroborar que um número é um número de cartão de crédito.</span><span class="sxs-lookup"><span data-stu-id="40677-p102">Data loss prevention (DLP) includes sensitive information types, such as Credit Card Number and EU Debit Card Number, which are ready for you to use in your DLP policies. These sensitive information types look for a specific pattern and corroborate it by ensuring proper formatting, enforcing checksums, and looking for relevant keywords or other information. Some of this functionality is performed by internal functions. For example, the Credit Card Number sensitive information type uses a function to look for dates formatted like an expiration date, to help corroborate that a number is a credit card number.</span></span>
  
<span data-ttu-id="40677-p103">Este tópico explica o que essas funções procuram, para ajudar você a entender como funcionam os tipos de informações confidenciais predefinidas. Para saber mais, consulte [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="40677-p103">This topic explains what these functions look for, to help you understand how the predefined sensitive information types work. For more information, see [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="funcusdate"></a><span data-ttu-id="40677-112">Func_us_date</span><span class="sxs-lookup"><span data-stu-id="40677-112">Func_us_date</span></span>

<span data-ttu-id="40677-p104">Essa função procura por uma data no formato comumente usada nos EUA Isso inclui os formatos de "mês/dia/ano", "mês-dia-ano," e "mês dia/ano". Os nomes ou abreviações de meses não diferenciam maiusculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="40677-p104">This function looks for a date in the format commonly used in the U.S. This includes the formats "month/day/year", "month-day-year", and "month day year ". The names or abbreviations of months are not case sensitive.</span></span> 
  
<span data-ttu-id="40677-115">Exemplos:</span><span class="sxs-lookup"><span data-stu-id="40677-115">Examples:</span></span>
  
- <span data-ttu-id="40677-116">2 de dezembro de 2016</span><span class="sxs-lookup"><span data-stu-id="40677-116">December 2, 2016</span></span>
    
- <span data-ttu-id="40677-117">2 de dezembro de 2016</span><span class="sxs-lookup"><span data-stu-id="40677-117">Dec 2, 2016</span></span>
    
- <span data-ttu-id="40677-118">dez 2016 02</span><span class="sxs-lookup"><span data-stu-id="40677-118">dec 02 2016</span></span>
    
- <span data-ttu-id="40677-119">12/2/2016</span><span class="sxs-lookup"><span data-stu-id="40677-119">12/2/2016</span></span>
    
- <span data-ttu-id="40677-120">12/02/16</span><span class="sxs-lookup"><span data-stu-id="40677-120">12/02/16</span></span>
    
- <span data-ttu-id="40677-121">Dez-2-2016</span><span class="sxs-lookup"><span data-stu-id="40677-121">Dec-2-2016</span></span>
    
- <span data-ttu-id="40677-122">2-12-16</span><span class="sxs-lookup"><span data-stu-id="40677-122">12-2-16</span></span>
    
<span data-ttu-id="40677-123">Nomes de meses aceitos:</span><span class="sxs-lookup"><span data-stu-id="40677-123">Accepted month names:</span></span>
  
- <span data-ttu-id="40677-124">Inglês</span><span class="sxs-lookup"><span data-stu-id="40677-124">English</span></span>
    
  - <span data-ttu-id="40677-125">Janeiro, fevereiro, março, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span><span class="sxs-lookup"><span data-stu-id="40677-125">January, February, march, April, may, June, July, August, September, October, November, December</span></span>
    
  - <span data-ttu-id="40677-126">Junho, julho ago Dec de novembro de outubro de setembro de maio de fevereiro de janeiro abr de março.</span><span class="sxs-lookup"><span data-stu-id="40677-126">Jan. Feb. Mar. Apr. May June July Aug. Sept. Oct. Nov. Dec.</span></span>
    
## <a name="funceudate"></a><span data-ttu-id="40677-127">Func_eu_date</span><span class="sxs-lookup"><span data-stu-id="40677-127">Func_eu_date</span></span>

<span data-ttu-id="40677-p105">Essa função procura uma data no formato comumente usado na UE (e na maioria dos lugares fora dos Estados Unidos). Isso inclui os formatos de "dia/mês/ano", "dia-mês-ano" e "dia mês ano". Os nomes ou as abreviações de meses não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="40677-p105">This function looks for a date in the format commonly used in the E.U. (and most places outside the U.S.). This includes the formats "day/month/year", "day-month-year", and "day month year". The names or abbreviations of months are not case sensitive.</span></span>
  
<span data-ttu-id="40677-132">Exemplos:</span><span class="sxs-lookup"><span data-stu-id="40677-132">Examples:</span></span>
  
- <span data-ttu-id="40677-133">De 2016 2 de dezembro</span><span class="sxs-lookup"><span data-stu-id="40677-133">2 Dec 2016</span></span>
    
- <span data-ttu-id="40677-134">dez 02 2016</span><span class="sxs-lookup"><span data-stu-id="40677-134">02 dec 2016</span></span>
    
- <span data-ttu-id="40677-135">16 de dezembro de 2</span><span class="sxs-lookup"><span data-stu-id="40677-135">2 Dec 16</span></span>
    
- <span data-ttu-id="40677-136">2/12/2016</span><span class="sxs-lookup"><span data-stu-id="40677-136">2/12/2016</span></span>
    
- <span data-ttu-id="40677-137">16/12/02</span><span class="sxs-lookup"><span data-stu-id="40677-137">02/12/16</span></span>
    
- <span data-ttu-id="40677-138">2-Dec-2016</span><span class="sxs-lookup"><span data-stu-id="40677-138">2-Dec-2016</span></span>
    
- <span data-ttu-id="40677-139">2-12-16</span><span class="sxs-lookup"><span data-stu-id="40677-139">2-12-16</span></span>
    
<span data-ttu-id="40677-140">Nomes de meses aceitos:</span><span class="sxs-lookup"><span data-stu-id="40677-140">Accepted month names:</span></span>
  
- <span data-ttu-id="40677-141">Inglês</span><span class="sxs-lookup"><span data-stu-id="40677-141">English</span></span>
    
  - <span data-ttu-id="40677-142">Janeiro, fevereiro, março, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span><span class="sxs-lookup"><span data-stu-id="40677-142">January, February, march, April, may, June, July, August, September, October, November, December</span></span>
    
  - <span data-ttu-id="40677-143">Junho, julho ago Dec de novembro de outubro de setembro de maio de fevereiro de janeiro abr de março.</span><span class="sxs-lookup"><span data-stu-id="40677-143">Jan. Feb. Mar. Apr. May June July Aug. Sept. Oct. Nov. Dec.</span></span>
    
- <span data-ttu-id="40677-144">Holandês</span><span class="sxs-lookup"><span data-stu-id="40677-144">Dutch</span></span>
    
  - <span data-ttu-id="40677-145">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span><span class="sxs-lookup"><span data-stu-id="40677-145">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span></span>
    
  - <span data-ttu-id="40677-146">Jan CTP de fevereiro maart abr mei junho, julho agosto Set setembro oct okt novembro dec</span><span class="sxs-lookup"><span data-stu-id="40677-146">jan feb maart apr mei jun jul aug sep sept oct okt nov dec</span></span>
    
- <span data-ttu-id="40677-147">Francês</span><span class="sxs-lookup"><span data-stu-id="40677-147">French</span></span>
    
  - <span data-ttu-id="40677-148">janvier, février, mars, avril, mai, juin juillet, août, septembre, octobre, novembre, décembre</span><span class="sxs-lookup"><span data-stu-id="40677-148">janvier, février, mars, avril, mai, juin juillet, août, septembre, octobre, novembre, décembre</span></span>
    
  - <span data-ttu-id="40677-p106">janv. févr. MARS avril mai juin juil. setembro de août outubro de novembro. déc.</span><span class="sxs-lookup"><span data-stu-id="40677-p106">janv. févr. mars avril mai juin juil. août sept. oct. nov. déc.</span></span>
    
- <span data-ttu-id="40677-156">Alemão</span><span class="sxs-lookup"><span data-stu-id="40677-156">German</span></span>
    
  - <span data-ttu-id="40677-157">jänuar, februar, märz, abril, mai, juni juli, agosto, setembro, oktober, novembro, dezember</span><span class="sxs-lookup"><span data-stu-id="40677-157">jänuar, februar, märz, April, mai, juni juli, August, September, oktober, November, dezember</span></span>
    
  - <span data-ttu-id="40677-p107">Jan. / Jän. Fevereiro März Mai abr Juni Juli ago setembro Okt. Dez de novembro.</span><span class="sxs-lookup"><span data-stu-id="40677-p107">Jan./Jän. Feb. März Apr. Mai Juni Juli Aug. Sept. Okt. Nov. Dez.</span></span>
    
- <span data-ttu-id="40677-161">Italiano</span><span class="sxs-lookup"><span data-stu-id="40677-161">Italian</span></span>
    
  - <span data-ttu-id="40677-162">gennaio, febbraio, marzo, aprile, maggio, giugno, luglio, agosto, settembre, ottobre, novembre, dicembre</span><span class="sxs-lookup"><span data-stu-id="40677-162">gennaio, febbraio, marzo, aprile, maggio, giugno, luglio, agosto, settembre, ottobre, novembre, dicembre</span></span>
    
  - <span data-ttu-id="40677-p108">genn. febbr. Mar. abr. magg. giugno luglio ag. definições. ott. novembro. dic.</span><span class="sxs-lookup"><span data-stu-id="40677-p108">genn. febbr. mar. apr. magg. giugno luglio ag. sett. ott. nov. dic.</span></span>
    
- <span data-ttu-id="40677-173">Português</span><span class="sxs-lookup"><span data-stu-id="40677-173">Portuguese</span></span>
    
  - <span data-ttu-id="40677-174">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span><span class="sxs-lookup"><span data-stu-id="40677-174">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span></span>
    
  - <span data-ttu-id="40677-175">Jan fev mar abr mai junho, julho atrás dispostos dez novembro</span><span class="sxs-lookup"><span data-stu-id="40677-175">jan fev mar abr mai jun jul ago set out nov dez</span></span>
    
- <span data-ttu-id="40677-176">Espanhol</span><span class="sxs-lookup"><span data-stu-id="40677-176">Spanish</span></span>
    
  - <span data-ttu-id="40677-177">enero, febrero, marzo, abril, mayo, junio, julio, agosto, septiembre, octubre, noviembre, diciembre</span><span class="sxs-lookup"><span data-stu-id="40677-177">enero, febrero, marzo, abril, mayo, junio, julio, agosto, septiembre, octubre, noviembre, diciembre</span></span>
    
  - <span data-ttu-id="40677-p109">enero CTP de fevereiro. marzo abr. mayo junho julho. setembro de agosto/conjunto. outubro de novembro. dic.</span><span class="sxs-lookup"><span data-stu-id="40677-p109">enero feb. marzo abr. mayo jun. jul. agosto sept./set. oct. nov. dic.</span></span>
    
## <a name="funceudate1-deprecated"></a><span data-ttu-id="40677-186">Func_eu_date1 (preterido)</span><span class="sxs-lookup"><span data-stu-id="40677-186">Func_eu_date1 (deprecated)</span></span>

> [!NOTE]
> <span data-ttu-id="40677-187">Essa função foi preterida porque ele oferece suporte a apenas nomes de mês português, que agora estão incluídos na `Func_eu_date` função acima.</span><span class="sxs-lookup"><span data-stu-id="40677-187">This function is deprecated because it supports only Portuguese month names, which are now included in the  `Func_eu_date` function above.</span></span> 
  
<span data-ttu-id="40677-p110">Essa função procura por uma data no formato normalmente usado em português. O formato para essa função é os mesmos `Func_eu_date`, diferentes apenas no idioma usado.</span><span class="sxs-lookup"><span data-stu-id="40677-p110">This function looks for a date in the format commonly used in Portuguese. The format for this function is the same as  `Func_eu_date`, differing only in the language used.</span></span>
  
<span data-ttu-id="40677-190">Exemplos:</span><span class="sxs-lookup"><span data-stu-id="40677-190">Examples:</span></span>
  
- <span data-ttu-id="40677-191">Dez 2 2016</span><span class="sxs-lookup"><span data-stu-id="40677-191">2 Dez 2016</span></span>
    
- <span data-ttu-id="40677-192">dez 02 2016</span><span class="sxs-lookup"><span data-stu-id="40677-192">02 dez 2016</span></span>
    
- <span data-ttu-id="40677-193">Dez 2 16</span><span class="sxs-lookup"><span data-stu-id="40677-193">2 Dez 16</span></span>
    
- <span data-ttu-id="40677-194">2/12/2016</span><span class="sxs-lookup"><span data-stu-id="40677-194">2/12/2016</span></span>
    
- <span data-ttu-id="40677-195">16/12/02</span><span class="sxs-lookup"><span data-stu-id="40677-195">02/12/16</span></span>
    
- <span data-ttu-id="40677-196">2-Dez-2016</span><span class="sxs-lookup"><span data-stu-id="40677-196">2-Dez-2016</span></span>
    
- <span data-ttu-id="40677-197">2-12-16</span><span class="sxs-lookup"><span data-stu-id="40677-197">2-12-16</span></span>
    
<span data-ttu-id="40677-198">Nomes de meses aceitos:</span><span class="sxs-lookup"><span data-stu-id="40677-198">Accepted month names:</span></span>
  
- <span data-ttu-id="40677-199">Português</span><span class="sxs-lookup"><span data-stu-id="40677-199">Portuguese</span></span>
    
  - <span data-ttu-id="40677-200">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span><span class="sxs-lookup"><span data-stu-id="40677-200">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span></span>
    
  - <span data-ttu-id="40677-201">Jan fev mar abr mai junho, julho atrás dispostos dez novembro</span><span class="sxs-lookup"><span data-stu-id="40677-201">jan fev mar abr mai jun jul ago set out nov dez</span></span>
    
## <a name="funceudate2-deprecated"></a><span data-ttu-id="40677-202">Func_eu_date2 (preterido)</span><span class="sxs-lookup"><span data-stu-id="40677-202">Func_eu_date2 (deprecated)</span></span>

> [!NOTE]
> <span data-ttu-id="40677-203">Essa função foi preterida porque ele oferece suporte a apenas nomes de mês holandês, que agora estão incluídos na `Func_eu_date` função acima.</span><span class="sxs-lookup"><span data-stu-id="40677-203">This function is deprecated because it supports only Dutch month names, which are now included in the  `Func_eu_date` function above.</span></span> 
  
<span data-ttu-id="40677-p111">Essa função procura por uma data no formato comumente usada em alemão. O formato para essa função é os mesmos `Func_eu_date`, diferentes apenas no idioma usado.</span><span class="sxs-lookup"><span data-stu-id="40677-p111">This function looks for a date in the format commonly used in Dutch. The format for this function is the same as  `Func_eu_date`, differing only in the language used.</span></span>
  
<span data-ttu-id="40677-206">Exemplos:</span><span class="sxs-lookup"><span data-stu-id="40677-206">Examples:</span></span>
  
- <span data-ttu-id="40677-207">2 Mei 2016</span><span class="sxs-lookup"><span data-stu-id="40677-207">2 Mei 2016</span></span>
    
- <span data-ttu-id="40677-208">02 mei 2016</span><span class="sxs-lookup"><span data-stu-id="40677-208">02 mei 2016</span></span>
    
- <span data-ttu-id="40677-209">2 Mei 16</span><span class="sxs-lookup"><span data-stu-id="40677-209">2 Mei 16</span></span>
    
- <span data-ttu-id="40677-210">2/12/2016</span><span class="sxs-lookup"><span data-stu-id="40677-210">2/12/2016</span></span>
    
- <span data-ttu-id="40677-211">16/12/02</span><span class="sxs-lookup"><span data-stu-id="40677-211">02/12/16</span></span>
    
- <span data-ttu-id="40677-212">2-Mei-2016</span><span class="sxs-lookup"><span data-stu-id="40677-212">2-Mei-2016</span></span>
    
- <span data-ttu-id="40677-213">2-12-16</span><span class="sxs-lookup"><span data-stu-id="40677-213">2-12-16</span></span>
    
<span data-ttu-id="40677-214">Nomes de meses aceitos:</span><span class="sxs-lookup"><span data-stu-id="40677-214">Accepted month names:</span></span>
  
- <span data-ttu-id="40677-215">Holandês</span><span class="sxs-lookup"><span data-stu-id="40677-215">Dutch</span></span>
    
  - <span data-ttu-id="40677-216">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span><span class="sxs-lookup"><span data-stu-id="40677-216">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span></span>
    
  - <span data-ttu-id="40677-217">Jan CTP de fevereiro maart abr mei junho, julho agosto Set setembro oct okt novembro dec</span><span class="sxs-lookup"><span data-stu-id="40677-217">jan feb maart apr mei jun jul aug sep sept oct okt nov dec</span></span>
    
## <a name="funcexpirationdate"></a><span data-ttu-id="40677-218">Func_expiration_date</span><span class="sxs-lookup"><span data-stu-id="40677-218">Func_expiration_date</span></span>

<span data-ttu-id="40677-p112">Essa função procura por uma data nos formatos costumam ser utilizados pelos cartões de crédito e débito, que excluir dias em favor meses. Essa função corresponderá datas no formato de "mês/ano", "mês-ano", "ano [nome do mês]" e "ano [abreviação mês]". Os nomes ou abreviações de meses não diferenciam maiusculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="40677-p112">This function looks for a date in the formats commonly used by credit and debit cards, which exclude days in favor of months. This function will match dates in format of "month/year", "month-year", "[month name] year", and "[month abbreviation] year". The names or abbreviations of months are not case sensitive.</span></span>
  
<span data-ttu-id="40677-222">Exemplos</span><span class="sxs-lookup"><span data-stu-id="40677-222">Examples:</span></span>
  
- <span data-ttu-id="40677-223">MM/AA -- por exemplo, 01/11 ou 1/11</span><span class="sxs-lookup"><span data-stu-id="40677-223">MM/YY -- for example, 01/11 or 1/11</span></span>
    
- <span data-ttu-id="40677-224">MM/AAAA -- por exemplo, 01/2011 ou 1/2011</span><span class="sxs-lookup"><span data-stu-id="40677-224">MM/YYYY -- for example, 01/2011 or 1/2011</span></span>
    
- <span data-ttu-id="40677-225">MM-AA -- por exemplo, 01-22 ou 1-11</span><span class="sxs-lookup"><span data-stu-id="40677-225">MM-YY -- for example, 01-22 or 1-11</span></span>
    
- <span data-ttu-id="40677-226">MM-AAAA -- por exemplo, 01-2000 ou 1-2000</span><span class="sxs-lookup"><span data-stu-id="40677-226">MM-YYYY -- for example, 01-2000 or 1-2000</span></span>
    
<span data-ttu-id="40677-227">Os seguintes formatos dão suporte a AA ou AAAA:</span><span class="sxs-lookup"><span data-stu-id="40677-227">The following formats support YY or YYYY:</span></span>
  
- <span data-ttu-id="40677-228">Mês-AAAA – por exemplo, jan-2010 ou janeiro-2010 ou jan-10 ou janeiro-10</span><span class="sxs-lookup"><span data-stu-id="40677-228">Month-YYYY -- for example, .Jan-2010 or january-2010 or Jan-10 or january-10</span></span>
    
- <span data-ttu-id="40677-229">Mês AAAA – por exemplo, 'janeiro 2010' ou 'jan 2010' ou 'janeiro 10' ou 'jan 10'</span><span class="sxs-lookup"><span data-stu-id="40677-229">Month YYYY -- for example, 'january 2010' or 'Jan 2010' or 'january 10' or 'Jan 10'</span></span>
    
- <span data-ttu-id="40677-230">MêsAAAA – por exemplo, 'janeiro2010' ou 'Jan2010' ou 'janeiro10' ou 'Jan10'</span><span class="sxs-lookup"><span data-stu-id="40677-230">MonthYYYY -- for example, 'january2010' or 'Jan2010' or 'january10' or 'Jan10'</span></span>
    
- <span data-ttu-id="40677-231">Mês aaaa – por exemplo, 'janeiro de 2010' ou ' Jan/2010' ou ' janeiro/10' ou ' Jan/10'</span><span class="sxs-lookup"><span data-stu-id="40677-231">Month/YYYY -- for example, 'january/2010' or 'Jan/2010' or 'january/10' or 'Jan/10'</span></span>
    
<span data-ttu-id="40677-232">Nomes de meses aceitos:</span><span class="sxs-lookup"><span data-stu-id="40677-232">Accepted month names:</span></span>
  
- <span data-ttu-id="40677-233">Inglês</span><span class="sxs-lookup"><span data-stu-id="40677-233">English</span></span>
    
  - <span data-ttu-id="40677-234">Janeiro, fevereiro, março, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span><span class="sxs-lookup"><span data-stu-id="40677-234">January, February, march, April, may, June, July, August, September, October, November, December</span></span>
    
  - <span data-ttu-id="40677-235">CTP de fevereiro de Jan Mar Abr talvez junho, julho agosto setembro Oct novembro Dec</span><span class="sxs-lookup"><span data-stu-id="40677-235">Jan Feb Mar Apr May June July Aug Sept Oct Nov Dec</span></span>
    
## <a name="funcusaddress"></a><span data-ttu-id="40677-236">Func_us_address</span><span class="sxs-lookup"><span data-stu-id="40677-236">Func_us_address</span></span>

<span data-ttu-id="40677-p113">Essa função procura por um nome ou sigla de estado dos EUA seguida de um CEP válido, como são usados em endereços postais. O CEP deve ser um dos CEPs corretos associados ao nome ou sigla do estado americano. O nome do estado americano e o CEP não podem ser separados por pontos ou letras.</span><span class="sxs-lookup"><span data-stu-id="40677-p113">This function looks for a U.S. state name or postal abbreviation followed by a valid zip code, just as they are used in postal addresses. The zip code must be one of the correct zip codes associated with the U.S. state name or abbreviation. The U.S. state name and zip code cannot be separated by punctuation or letters.</span></span>
  
<span data-ttu-id="40677-240">Exemplos:</span><span class="sxs-lookup"><span data-stu-id="40677-240">Examples:</span></span>
  
- <span data-ttu-id="40677-241">Washington 98052</span><span class="sxs-lookup"><span data-stu-id="40677-241">Washington 98052</span></span>
    
- <span data-ttu-id="40677-242">Washington 98052-9998</span><span class="sxs-lookup"><span data-stu-id="40677-242">Washington 98052-9998</span></span>
    
- <span data-ttu-id="40677-243">WA 98052</span><span class="sxs-lookup"><span data-stu-id="40677-243">WA 98052</span></span>
    
- <span data-ttu-id="40677-244">WA 98052-9998</span><span class="sxs-lookup"><span data-stu-id="40677-244">WA 98052-9998</span></span>
    


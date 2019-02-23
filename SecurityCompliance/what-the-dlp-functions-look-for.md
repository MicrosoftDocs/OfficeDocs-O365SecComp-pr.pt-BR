---
title: O que as funções DLP procuram
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/18/2016
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 94349ed4-5351-4ee2-bbda-70813c9ed693
description: Os tipos de informações confidenciais procuram um padrão específico e o corroboratem, garantindo a formatação adequada, aplicando as somas de verificação e procurando palavras-chave relevantes ou outras informações. Algumas dessas funcionalidades são executadas por funções internas. Este tópico explica o que essas funções procuram para ajudá-lo a entender como funcionam os tipos de informações confidenciais predefinidos.
ms.openlocfilehash: 55c740e892e92902b368b2dcf7b0999cbc60f3ed
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219351"
---
# <a name="what-the-dlp-functions-look-for"></a><span data-ttu-id="0c802-105">O que as funções DLP procuram</span><span class="sxs-lookup"><span data-stu-id="0c802-105">What the DLP functions look for</span></span>

<span data-ttu-id="0c802-p102">A política DLP inclui tipos de informação confidencial, como números de cartão de crédito e de cartão de débito da UE (União Europeia), que estão prontos para uso em suas políticas DLP. Esses tipos de informação confidencial procuram por um padrão específico e o confirmam, garantindo a formatação adequada, impondo as somas de verificação e procurando palavras-chave relevantes ou outras informações. Algumas dessas funcionalidades são realizadas por funções internas. Por exemplo, o tipo de informação confidencial de Número de Cartão de Crédito usa uma função para procurar datas formatadas como uma data de expiração, para ajudar a corroborar que um número é um número de cartão de crédito.</span><span class="sxs-lookup"><span data-stu-id="0c802-p102">Data loss prevention (DLP) includes sensitive information types, such as Credit Card Number and EU Debit Card Number, which are ready for you to use in your DLP policies. These sensitive information types look for a specific pattern and corroborate it by ensuring proper formatting, enforcing checksums, and looking for relevant keywords or other information. Some of this functionality is performed by internal functions. For example, the Credit Card Number sensitive information type uses a function to look for dates formatted like an expiration date, to help corroborate that a number is a credit card number.</span></span>
  
<span data-ttu-id="0c802-p103">Este tópico explica o que essas funções procuram, para ajudar você a entender como funcionam os tipos de informações confidenciais predefinidas. Para saber mais, consulte [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="0c802-p103">This topic explains what these functions look for, to help you understand how the predefined sensitive information types work. For more information, see [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="funcusdate"></a><span data-ttu-id="0c802-112">Func_us_date</span><span class="sxs-lookup"><span data-stu-id="0c802-112">Func_us_date</span></span>

<span data-ttu-id="0c802-p104">Essa função procura uma data no formato comumente usado nos EUA. Isso inclui os formatos "mês/dia/ano", "mês-dia-ano" e "ano dia do mês". Os nomes ou abreviações de meses não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="0c802-p104">This function looks for a date in the format commonly used in the U.S. This includes the formats "month/day/year", "month-day-year", and "month day year ". The names or abbreviations of months are not case sensitive.</span></span> 
  
<span data-ttu-id="0c802-115">Exemplos:</span><span class="sxs-lookup"><span data-stu-id="0c802-115">Examples:</span></span>
  
- <span data-ttu-id="0c802-116">2 de dezembro de 2016</span><span class="sxs-lookup"><span data-stu-id="0c802-116">December 2, 2016</span></span>
    
- <span data-ttu-id="0c802-117">2 de dezembro de 2016</span><span class="sxs-lookup"><span data-stu-id="0c802-117">Dec 2, 2016</span></span>
    
- <span data-ttu-id="0c802-118">Dec 02 2016</span><span class="sxs-lookup"><span data-stu-id="0c802-118">dec 02 2016</span></span>
    
- <span data-ttu-id="0c802-119">12/2/2016</span><span class="sxs-lookup"><span data-stu-id="0c802-119">12/2/2016</span></span>
    
- <span data-ttu-id="0c802-120">12/02/16</span><span class="sxs-lookup"><span data-stu-id="0c802-120">12/02/16</span></span>
    
- <span data-ttu-id="0c802-121">Dec-2-2016</span><span class="sxs-lookup"><span data-stu-id="0c802-121">Dec-2-2016</span></span>
    
- <span data-ttu-id="0c802-122">12-2-16</span><span class="sxs-lookup"><span data-stu-id="0c802-122">12-2-16</span></span>
    
<span data-ttu-id="0c802-123">Nomes de meses aceitos:</span><span class="sxs-lookup"><span data-stu-id="0c802-123">Accepted month names:</span></span>
  
- <span data-ttu-id="0c802-124">Inglês</span><span class="sxs-lookup"><span data-stu-id="0c802-124">English</span></span>
    
  - <span data-ttu-id="0c802-125">Janeiro, fevereiro, março, abril, maio, junho de julho, agosto, setembro, outubro, novembro de dezembro</span><span class="sxs-lookup"><span data-stu-id="0c802-125">January, February, march, April, may, June, July, August, September, October, November, December</span></span>
    
  - <span data-ttu-id="0c802-126">Jan. Fev. mar. abr. Maio de 1º de julho de agosto de setembro. Dec.</span><span class="sxs-lookup"><span data-stu-id="0c802-126">Jan. Feb. Mar. Apr. May June July Aug. Sept. Oct. Nov. Dec.</span></span>
    
## <a name="funceudate"></a><span data-ttu-id="0c802-127">Func_eu_date</span><span class="sxs-lookup"><span data-stu-id="0c802-127">Func_eu_date</span></span>

<span data-ttu-id="0c802-p105">Essa função procura uma data no formato comumente usado na UE (e na maioria dos lugares fora dos Estados Unidos). Isso inclui os formatos de "dia/mês/ano", "dia-mês-ano" e "dia mês ano". Os nomes ou as abreviações de meses não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="0c802-p105">This function looks for a date in the format commonly used in the E.U. (and most places outside the U.S.). This includes the formats "day/month/year", "day-month-year", and "day month year". The names or abbreviations of months are not case sensitive.</span></span>
  
<span data-ttu-id="0c802-132">Exemplos:</span><span class="sxs-lookup"><span data-stu-id="0c802-132">Examples:</span></span>
  
- <span data-ttu-id="0c802-133">2 Dec 2016</span><span class="sxs-lookup"><span data-stu-id="0c802-133">2 Dec 2016</span></span>
    
- <span data-ttu-id="0c802-134">02 de dezembro de 2016</span><span class="sxs-lookup"><span data-stu-id="0c802-134">02 dec 2016</span></span>
    
- <span data-ttu-id="0c802-135">2 de dezembro de 16</span><span class="sxs-lookup"><span data-stu-id="0c802-135">2 Dec 16</span></span>
    
- <span data-ttu-id="0c802-136">2/12/2016</span><span class="sxs-lookup"><span data-stu-id="0c802-136">2/12/2016</span></span>
    
- <span data-ttu-id="0c802-137">02/12/16</span><span class="sxs-lookup"><span data-stu-id="0c802-137">02/12/16</span></span>
    
- <span data-ttu-id="0c802-138">2-dez-2016</span><span class="sxs-lookup"><span data-stu-id="0c802-138">2-Dec-2016</span></span>
    
- <span data-ttu-id="0c802-139">2-12-16</span><span class="sxs-lookup"><span data-stu-id="0c802-139">2-12-16</span></span>
    
<span data-ttu-id="0c802-140">Nomes de meses aceitos:</span><span class="sxs-lookup"><span data-stu-id="0c802-140">Accepted month names:</span></span>
  
- <span data-ttu-id="0c802-141">Inglês</span><span class="sxs-lookup"><span data-stu-id="0c802-141">English</span></span>
    
  - <span data-ttu-id="0c802-142">Janeiro, fevereiro, março, abril, maio, junho de julho, agosto, setembro, outubro, novembro de dezembro</span><span class="sxs-lookup"><span data-stu-id="0c802-142">January, February, march, April, may, June, July, August, September, October, November, December</span></span>
    
  - <span data-ttu-id="0c802-143">Jan. Fev. mar. abr. Maio de 1º de julho de agosto de setembro. Dec.</span><span class="sxs-lookup"><span data-stu-id="0c802-143">Jan. Feb. Mar. Apr. May June July Aug. Sept. Oct. Nov. Dec.</span></span>
    
- <span data-ttu-id="0c802-144">Holandês</span><span class="sxs-lookup"><span data-stu-id="0c802-144">Dutch</span></span>
    
  - <span data-ttu-id="0c802-145">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span><span class="sxs-lookup"><span data-stu-id="0c802-145">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span></span>
    
  - <span data-ttu-id="0c802-146">Jan fevereiro de maart de abril de Mei jun jul setembro de agosto de dezembro de Okt de Nov</span><span class="sxs-lookup"><span data-stu-id="0c802-146">jan feb maart apr mei jun jul aug sep sept oct okt nov dec</span></span>
    
- <span data-ttu-id="0c802-147">Francês</span><span class="sxs-lookup"><span data-stu-id="0c802-147">French</span></span>
    
  - <span data-ttu-id="0c802-148">Janvier, Février, Mars, Avril, Mai, Juin Juillet, Août, Septembre, outubro, Novembre, décembre</span><span class="sxs-lookup"><span data-stu-id="0c802-148">janvier, février, mars, avril, mai, juin juillet, août, septembre, octobre, novembre, décembre</span></span>
    
  - <span data-ttu-id="0c802-p106">Janv. févr. Mars Avril Mai Juin Juil. Août set. Oct. nov. déc.</span><span class="sxs-lookup"><span data-stu-id="0c802-p106">janv. févr. mars avril mai juin juil. août sept. oct. nov. déc.</span></span>
    
- <span data-ttu-id="0c802-156">Alemão</span><span class="sxs-lookup"><span data-stu-id="0c802-156">German</span></span>
    
  - <span data-ttu-id="0c802-157">jänuar, februar, März, abril, Mai, Juni Juli, agosto, setembro, Oktober, novembro de Dezember</span><span class="sxs-lookup"><span data-stu-id="0c802-157">jänuar, februar, märz, April, mai, juni juli, August, September, oktober, November, dezember</span></span>
    
  - <span data-ttu-id="0c802-p107">Jan./Jän. Fev. März abr. Mai Juni Juli ago. set. Okt. Nov. dez.</span><span class="sxs-lookup"><span data-stu-id="0c802-p107">Jan./Jän. Feb. März Apr. Mai Juni Juli Aug. Sept. Okt. Nov. Dez.</span></span>
    
- <span data-ttu-id="0c802-161">Italiano</span><span class="sxs-lookup"><span data-stu-id="0c802-161">Italian</span></span>
    
  - <span data-ttu-id="0c802-162">gennaio, febbraio, Marzo, Aprile, Maggio, giugno, Luglio, agosto, Settembre, ottobre, Novembre, Dicembre</span><span class="sxs-lookup"><span data-stu-id="0c802-162">gennaio, febbraio, marzo, aprile, maggio, giugno, luglio, agosto, settembre, ottobre, novembre, dicembre</span></span>
    
  - <span data-ttu-id="0c802-p108">Genn. febbr. mar. abr. Magg. giugno Luglio AG. definida. Ott. Nov. DIC.</span><span class="sxs-lookup"><span data-stu-id="0c802-p108">genn. febbr. mar. apr. magg. giugno luglio ag. sett. ott. nov. dic.</span></span>
    
- <span data-ttu-id="0c802-173">Português</span><span class="sxs-lookup"><span data-stu-id="0c802-173">Portuguese</span></span>
    
  - <span data-ttu-id="0c802-174">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span><span class="sxs-lookup"><span data-stu-id="0c802-174">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span></span>
    
  - <span data-ttu-id="0c802-175">Jan fev mar abr mai jun jul atrás Set out nov dez</span><span class="sxs-lookup"><span data-stu-id="0c802-175">jan fev mar abr mai jun jul ago set out nov dez</span></span>
    
- <span data-ttu-id="0c802-176">Espanhol</span><span class="sxs-lookup"><span data-stu-id="0c802-176">Spanish</span></span>
    
  - <span data-ttu-id="0c802-177">Enero, Febrero, Marzo, abril, Mayo, junio, Julio, agosto, Septiembre, Octubre, Noviembre, Diciembre</span><span class="sxs-lookup"><span data-stu-id="0c802-177">enero, febrero, marzo, abril, mayo, junio, julio, agosto, septiembre, octubre, noviembre, diciembre</span></span>
    
  - <span data-ttu-id="0c802-p109">Enero Fev. Marzo abr. Mayo Jun. Jul. agosto set./set. Oct. nov. DIC.</span><span class="sxs-lookup"><span data-stu-id="0c802-p109">enero feb. marzo abr. mayo jun. jul. agosto sept./set. oct. nov. dic.</span></span>
    
## <a name="funceudate1-deprecated"></a><span data-ttu-id="0c802-186">Func_eu_date1 (preterido)</span><span class="sxs-lookup"><span data-stu-id="0c802-186">Func_eu_date1 (deprecated)</span></span>

> [!NOTE]
> <span data-ttu-id="0c802-187">Essa função foi preterida porque dá suporte apenas a `Func_eu_date` nomes de meses em Português, que agora estão incluídos na função acima.</span><span class="sxs-lookup"><span data-stu-id="0c802-187">This function is deprecated because it supports only Portuguese month names, which are now included in the  `Func_eu_date` function above.</span></span> 
  
<span data-ttu-id="0c802-p110">Essa função procura uma data no formato comumente usado em Português. O formato dessa função é o mesmo que `Func_eu_date`, diferente somente no idioma usado.</span><span class="sxs-lookup"><span data-stu-id="0c802-p110">This function looks for a date in the format commonly used in Portuguese. The format for this function is the same as  `Func_eu_date`, differing only in the language used.</span></span>
  
<span data-ttu-id="0c802-190">Exemplos:</span><span class="sxs-lookup"><span data-stu-id="0c802-190">Examples:</span></span>
  
- <span data-ttu-id="0c802-191">2 dez 2016</span><span class="sxs-lookup"><span data-stu-id="0c802-191">2 Dez 2016</span></span>
    
- <span data-ttu-id="0c802-192">02 dez 2016</span><span class="sxs-lookup"><span data-stu-id="0c802-192">02 dez 2016</span></span>
    
- <span data-ttu-id="0c802-193">2 dez 16</span><span class="sxs-lookup"><span data-stu-id="0c802-193">2 Dez 16</span></span>
    
- <span data-ttu-id="0c802-194">2/12/2016</span><span class="sxs-lookup"><span data-stu-id="0c802-194">2/12/2016</span></span>
    
- <span data-ttu-id="0c802-195">02/12/16</span><span class="sxs-lookup"><span data-stu-id="0c802-195">02/12/16</span></span>
    
- <span data-ttu-id="0c802-196">2-dez-2016</span><span class="sxs-lookup"><span data-stu-id="0c802-196">2-Dez-2016</span></span>
    
- <span data-ttu-id="0c802-197">2-12-16</span><span class="sxs-lookup"><span data-stu-id="0c802-197">2-12-16</span></span>
    
<span data-ttu-id="0c802-198">Nomes de meses aceitos:</span><span class="sxs-lookup"><span data-stu-id="0c802-198">Accepted month names:</span></span>
  
- <span data-ttu-id="0c802-199">Português</span><span class="sxs-lookup"><span data-stu-id="0c802-199">Portuguese</span></span>
    
  - <span data-ttu-id="0c802-200">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span><span class="sxs-lookup"><span data-stu-id="0c802-200">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span></span>
    
  - <span data-ttu-id="0c802-201">Jan fev mar abr mai jun jul atrás Set out nov dez</span><span class="sxs-lookup"><span data-stu-id="0c802-201">jan fev mar abr mai jun jul ago set out nov dez</span></span>
    
## <a name="funceudate2-deprecated"></a><span data-ttu-id="0c802-202">Func_eu_date2 (preterido)</span><span class="sxs-lookup"><span data-stu-id="0c802-202">Func_eu_date2 (deprecated)</span></span>

> [!NOTE]
> <span data-ttu-id="0c802-203">Essa função foi preterida porque dá suporte apenas a `Func_eu_date` nomes de meses em Holandês, que agora estão incluídos na função acima.</span><span class="sxs-lookup"><span data-stu-id="0c802-203">This function is deprecated because it supports only Dutch month names, which are now included in the  `Func_eu_date` function above.</span></span> 
  
<span data-ttu-id="0c802-p111">Essa função procura uma data no formato comumente usado em Holandês. O formato dessa função é o mesmo que `Func_eu_date`, diferente somente no idioma usado.</span><span class="sxs-lookup"><span data-stu-id="0c802-p111">This function looks for a date in the format commonly used in Dutch. The format for this function is the same as  `Func_eu_date`, differing only in the language used.</span></span>
  
<span data-ttu-id="0c802-206">Exemplos:</span><span class="sxs-lookup"><span data-stu-id="0c802-206">Examples:</span></span>
  
- <span data-ttu-id="0c802-207">2 Mei 2016</span><span class="sxs-lookup"><span data-stu-id="0c802-207">2 Mei 2016</span></span>
    
- <span data-ttu-id="0c802-208">02 Mei 2016</span><span class="sxs-lookup"><span data-stu-id="0c802-208">02 mei 2016</span></span>
    
- <span data-ttu-id="0c802-209">2 Mei 16</span><span class="sxs-lookup"><span data-stu-id="0c802-209">2 Mei 16</span></span>
    
- <span data-ttu-id="0c802-210">2/12/2016</span><span class="sxs-lookup"><span data-stu-id="0c802-210">2/12/2016</span></span>
    
- <span data-ttu-id="0c802-211">02/12/16</span><span class="sxs-lookup"><span data-stu-id="0c802-211">02/12/16</span></span>
    
- <span data-ttu-id="0c802-212">2-Mei-2016</span><span class="sxs-lookup"><span data-stu-id="0c802-212">2-Mei-2016</span></span>
    
- <span data-ttu-id="0c802-213">2-12-16</span><span class="sxs-lookup"><span data-stu-id="0c802-213">2-12-16</span></span>
    
<span data-ttu-id="0c802-214">Nomes de meses aceitos:</span><span class="sxs-lookup"><span data-stu-id="0c802-214">Accepted month names:</span></span>
  
- <span data-ttu-id="0c802-215">Holandês</span><span class="sxs-lookup"><span data-stu-id="0c802-215">Dutch</span></span>
    
  - <span data-ttu-id="0c802-216">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span><span class="sxs-lookup"><span data-stu-id="0c802-216">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span></span>
    
  - <span data-ttu-id="0c802-217">Jan fevereiro de maart de abril de Mei jun jul setembro de agosto de dezembro de Okt de Nov</span><span class="sxs-lookup"><span data-stu-id="0c802-217">jan feb maart apr mei jun jul aug sep sept oct okt nov dec</span></span>
    
## <a name="funcexpirationdate"></a><span data-ttu-id="0c802-218">Func_expiration_date</span><span class="sxs-lookup"><span data-stu-id="0c802-218">Func_expiration_date</span></span>

<span data-ttu-id="0c802-p112">Essa função procura uma data nos formatos comumente usados por cartões de crédito e débito, que excluem dias em favor de meses. Essa função coincidirá datas no formato de "mês/ano", "Mês-Year", "[month Name] Year" e "[month abreviation] Year". Os nomes ou abreviações de meses não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="0c802-p112">This function looks for a date in the formats commonly used by credit and debit cards, which exclude days in favor of months. This function will match dates in format of "month/year", "month-year", "[month name] year", and "[month abbreviation] year". The names or abbreviations of months are not case sensitive.</span></span>
  
<span data-ttu-id="0c802-222">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0c802-222">Examples:</span></span>
  
- <span data-ttu-id="0c802-223">MM/AA -- por exemplo, 01/11 ou 1/11</span><span class="sxs-lookup"><span data-stu-id="0c802-223">MM/YY -- for example, 01/11 or 1/11</span></span>
    
- <span data-ttu-id="0c802-224">MM/AAAA -- por exemplo, 01/2011 ou 1/2011</span><span class="sxs-lookup"><span data-stu-id="0c802-224">MM/YYYY -- for example, 01/2011 or 1/2011</span></span>
    
- <span data-ttu-id="0c802-225">MM-AA -- por exemplo, 01-22 ou 1-11</span><span class="sxs-lookup"><span data-stu-id="0c802-225">MM-YY -- for example, 01-22 or 1-11</span></span>
    
- <span data-ttu-id="0c802-226">MM-AAAA -- por exemplo, 01-2000 ou 1-2000</span><span class="sxs-lookup"><span data-stu-id="0c802-226">MM-YYYY -- for example, 01-2000 or 1-2000</span></span>
    
<span data-ttu-id="0c802-227">Os seguintes formatos dão suporte a AA ou AAAA:</span><span class="sxs-lookup"><span data-stu-id="0c802-227">The following formats support YY or YYYY:</span></span>
  
- <span data-ttu-id="0c802-228">Mês-AAAA – por exemplo, jan-2010 ou janeiro-2010 ou jan-10 ou janeiro-10</span><span class="sxs-lookup"><span data-stu-id="0c802-228">Month-YYYY -- for example, .Jan-2010 or january-2010 or Jan-10 or january-10</span></span>
    
- <span data-ttu-id="0c802-229">Mês AAAA – por exemplo, 'janeiro 2010' ou 'jan 2010' ou 'janeiro 10' ou 'jan 10'</span><span class="sxs-lookup"><span data-stu-id="0c802-229">Month YYYY -- for example, 'january 2010' or 'Jan 2010' or 'january 10' or 'Jan 10'</span></span>
    
- <span data-ttu-id="0c802-230">MêsAAAA – por exemplo, 'janeiro2010' ou 'Jan2010' ou 'janeiro10' ou 'Jan10'</span><span class="sxs-lookup"><span data-stu-id="0c802-230">MonthYYYY -- for example, 'january2010' or 'Jan2010' or 'january10' or 'Jan10'</span></span>
    
- <span data-ttu-id="0c802-231">Month/aaaa--por exemplo, ' Janeiro/2010 ' ou ' Jan/2010 ' ou ' janeiro/10 ' ou ' Jan/10 '</span><span class="sxs-lookup"><span data-stu-id="0c802-231">Month/YYYY -- for example, 'january/2010' or 'Jan/2010' or 'january/10' or 'Jan/10'</span></span>
    
<span data-ttu-id="0c802-232">Nomes de meses aceitos:</span><span class="sxs-lookup"><span data-stu-id="0c802-232">Accepted month names:</span></span>
  
- <span data-ttu-id="0c802-233">Inglês</span><span class="sxs-lookup"><span data-stu-id="0c802-233">English</span></span>
    
  - <span data-ttu-id="0c802-234">Janeiro, fevereiro, março, abril, maio, junho de julho, agosto, setembro, outubro, novembro de dezembro</span><span class="sxs-lookup"><span data-stu-id="0c802-234">January, February, march, April, may, June, July, August, September, October, November, December</span></span>
    
  - <span data-ttu-id="0c802-235">Jan fev mar de junho de julho de agosto de agosto de abril de dezembro</span><span class="sxs-lookup"><span data-stu-id="0c802-235">Jan Feb Mar Apr May June July Aug Sept Oct Nov Dec</span></span>
    
## <a name="funcusaddress"></a><span data-ttu-id="0c802-236">Func_us_address</span><span class="sxs-lookup"><span data-stu-id="0c802-236">Func_us_address</span></span>

<span data-ttu-id="0c802-p113">Essa função procura por um nome ou sigla de estado dos EUA seguida de um CEP válido, como são usados em endereços postais. O CEP deve ser um dos CEPs corretos associados ao nome ou sigla do estado americano. O nome do estado americano e o CEP não podem ser separados por pontos ou letras.</span><span class="sxs-lookup"><span data-stu-id="0c802-p113">This function looks for a U.S. state name or postal abbreviation followed by a valid zip code, just as they are used in postal addresses. The zip code must be one of the correct zip codes associated with the U.S. state name or abbreviation. The U.S. state name and zip code cannot be separated by punctuation or letters.</span></span>
  
<span data-ttu-id="0c802-240">Exemplos:</span><span class="sxs-lookup"><span data-stu-id="0c802-240">Examples:</span></span>
  
- <span data-ttu-id="0c802-241">Washington 98052</span><span class="sxs-lookup"><span data-stu-id="0c802-241">Washington 98052</span></span>
    
- <span data-ttu-id="0c802-242">Washington 98052-9998</span><span class="sxs-lookup"><span data-stu-id="0c802-242">Washington 98052-9998</span></span>
    
- <span data-ttu-id="0c802-243">WA 98052</span><span class="sxs-lookup"><span data-stu-id="0c802-243">WA 98052</span></span>
    
- <span data-ttu-id="0c802-244">WA 98052-9998</span><span class="sxs-lookup"><span data-stu-id="0c802-244">WA 98052-9998</span></span>
    


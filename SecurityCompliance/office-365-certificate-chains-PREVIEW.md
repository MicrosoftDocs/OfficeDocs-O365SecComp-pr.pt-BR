---
title: Cadeias de certificados do Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/26/2018
ms.audience: ITPro
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Ent_O365
ms.assetid: 0c03e6b3-e73f-4316-9e2b-bf4091ae96bb
description: O Office 365 utiliza um número de provedores de certificado diferente. O exemplo a seguir descreve a lista completa de certificados de raiz Office 365 conhecidos que os clientes podem encontrar ao acessar o Office 365. Para obter informações sobre os certificados que você talvez precise instalar em sua própria infra-estrutura, consulte Plan for certificados SSL de terceiros para o Office 365. As seguintes informações de certificado se aplica a todas as instâncias de nuvem em todo o mundo e Nacional do Office 365.
ms.openlocfilehash: 1dcc2dc38bb8e3239a3be3983791b0c60917dc5e
ms.sourcegitcommit: 13f40ff7c1799152bf45af2d8110f4f3235b770a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/12/2018
ms.locfileid: "25549737"
---
# <a name="office-365-certificate-chains"></a><span data-ttu-id="8fce5-106">Cadeias de certificados do Office 365</span><span class="sxs-lookup"><span data-stu-id="8fce5-106">Office 365 Certificate Chains</span></span>

<span data-ttu-id="8fce5-p102">O Office 365 utiliza um número de provedores de certificado diferente. O exemplo a seguir descreve a lista completa de certificados de raiz Office 365 conhecidos que os clientes podem encontrar ao acessar o Office 365. Para obter informações sobre os certificados que você talvez precise instalar em sua própria infra-estrutura, consulte [Planejar certificados SSL de terceiros para o Office 365](https://support.office.com/article/b48cdf63-07e0-4cda-8c12-4871590f59ce). As seguintes informações de certificado se aplica a todas as instâncias de nuvem em todo o mundo e Nacional do Office 365.</span><span class="sxs-lookup"><span data-stu-id="8fce5-p102">Office 365 leverages a number of different certificate providers. The following describes the complete list of known Office 365 root certificates that customers may encounter when accessing Office 365. For information on the certificates you may need to install in your own infrastructure, see [Plan for third-party SSL certificates for Office 365](https://support.office.com/article/b48cdf63-07e0-4cda-8c12-4871590f59ce). The following certificate information applies to all worldwide and national cloud instances of Office 365.</span></span>
  

|<span data-ttu-id="8fce5-111">**Tipo de certificado**</span><span class="sxs-lookup"><span data-stu-id="8fce5-111">**Certificate type**</span></span>|<span data-ttu-id="8fce5-112">**P7b download**</span><span class="sxs-lookup"><span data-stu-id="8fce5-112">**P7b download**</span></span>|<span data-ttu-id="8fce5-113">**Pontos de extremidade da lista de certificados Revogados**</span><span class="sxs-lookup"><span data-stu-id="8fce5-113">**CRL Endpoints**</span></span>|<span data-ttu-id="8fce5-114">**Pontos de extremidade OCSP**</span><span class="sxs-lookup"><span data-stu-id="8fce5-114">**OCSP Endpoints**</span></span>|<span data-ttu-id="8fce5-115">**Pontos de extremidade AIA**</span><span class="sxs-lookup"><span data-stu-id="8fce5-115">**AIA Endpoints**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="8fce5-116">Certificados raiz de publicamente confiáveis</span><span class="sxs-lookup"><span data-stu-id="8fce5-116">Publicly Trusted Root Certificates</span></span>](https://support.office.com/article/0c03e6b3-e73f-4316-9e2b-bf4091ae96bb#rootcerts) <br/> |[<span data-ttu-id="8fce5-117">Pacote de certificado raiz do Office 365 (P7B)</span><span class="sxs-lookup"><span data-stu-id="8fce5-117">Office 365 Root Certificate Bundle (P7B)</span></span>](http://download.microsoft.com/download/A/5/A/A5AE01F3-D19B-4A11-9407-801263CEF72C/O365_Root_Certs_20170321.p7b) <br/> |<span data-ttu-id="8fce5-118">CRL.GlobalSign.NET</span><span class="sxs-lookup"><span data-stu-id="8fce5-118">crl.globalsign.net</span></span>  <br/> <span data-ttu-id="8fce5-119">www.d-Trust.NET</span><span class="sxs-lookup"><span data-stu-id="8fce5-119">www.d-trust.net</span></span>  <br/> |<span data-ttu-id="8fce5-120">N/D</span><span class="sxs-lookup"><span data-stu-id="8fce5-120">N/A</span></span>  <br/> |<span data-ttu-id="8fce5-121">N/D</span><span class="sxs-lookup"><span data-stu-id="8fce5-121">N/A</span></span>  <br/> |
|[<span data-ttu-id="8fce5-122">Publicamente confiáveis certificados intermediários</span><span class="sxs-lookup"><span data-stu-id="8fce5-122">Publicly Trusted Intermediate Certificates</span></span>](https://support.office.com/article/0c03e6b3-e73f-4316-9e2b-bf4091ae96bb#IntermediateCerts) <br/> |[<span data-ttu-id="8fce5-123">Pacote do Office 365 intermediário de certificado (P7B)</span><span class="sxs-lookup"><span data-stu-id="8fce5-123">Office 365 Intermediate Certificate Bundle (P7B)</span></span>](http://download.microsoft.com/download/4/D/5/4D5339A4-0A4A-46AB-AE52-B179DEDA4BEC/O365_Intermediate_Certs_20170321.p7b)  <br/> |<span data-ttu-id="8fce5-124">cdp1.Public-trust.com</span><span class="sxs-lookup"><span data-stu-id="8fce5-124">cdp1.public-trust.com</span></span>  <br/> <span data-ttu-id="8fce5-125">CRL.cnnic.CN</span><span class="sxs-lookup"><span data-stu-id="8fce5-125">crl.cnnic.cn</span></span>  <br/> <span data-ttu-id="8fce5-126">CRL.Entrust.NET</span><span class="sxs-lookup"><span data-stu-id="8fce5-126">crl.entrust.net</span></span>  <br/> <span data-ttu-id="8fce5-127">CRL.GlobalSign.com</span><span class="sxs-lookup"><span data-stu-id="8fce5-127">crl.globalsign.com</span></span>  <br/> <span data-ttu-id="8fce5-128">CRL.GlobalSign.NET</span><span class="sxs-lookup"><span data-stu-id="8fce5-128">crl.globalsign.net</span></span>  <br/> <span data-ttu-id="8fce5-129">CRL.identrust.com</span><span class="sxs-lookup"><span data-stu-id="8fce5-129">crl.identrust.com</span></span>  <br/> <span data-ttu-id="8fce5-130">CRL.Thawte.com</span><span class="sxs-lookup"><span data-stu-id="8fce5-130">crl.thawte.com</span></span>  <br/> <span data-ttu-id="8fce5-131">crl3.digicert.com</span><span class="sxs-lookup"><span data-stu-id="8fce5-131">crl3.digicert.com</span></span>  <br/> <span data-ttu-id="8fce5-132">crl4.digicert.com</span><span class="sxs-lookup"><span data-stu-id="8fce5-132">crl4.digicert.com</span></span>  <br/> <span data-ttu-id="8fce5-133">S1.symcb.com</span><span class="sxs-lookup"><span data-stu-id="8fce5-133">s1.symcb.com</span></span>  <br/> <span data-ttu-id="8fce5-134">www.d-Trust.NET</span><span class="sxs-lookup"><span data-stu-id="8fce5-134">www.d-trust.net</span></span>  <br/> |<span data-ttu-id="8fce5-135">isrg.trustid.OCSP.identrust.com</span><span class="sxs-lookup"><span data-stu-id="8fce5-135">isrg.trustid.ocsp.identrust.com</span></span>  <br/> <span data-ttu-id="8fce5-136">OCSP.digicert.com</span><span class="sxs-lookup"><span data-stu-id="8fce5-136">ocsp.digicert.com</span></span>  <br/> <span data-ttu-id="8fce5-137">OCSP.Entrust.NET</span><span class="sxs-lookup"><span data-stu-id="8fce5-137">ocsp.entrust.net</span></span>  <br/> <span data-ttu-id="8fce5-138">OCSP.GlobalSign.com</span><span class="sxs-lookup"><span data-stu-id="8fce5-138">ocsp.globalsign.com</span></span>  <br/> <span data-ttu-id="8fce5-139">OCSP.omniroot.com</span><span class="sxs-lookup"><span data-stu-id="8fce5-139">ocsp.omniroot.com</span></span>  <br/> <span data-ttu-id="8fce5-140">OCSP.startssl.com</span><span class="sxs-lookup"><span data-stu-id="8fce5-140">ocsp.startssl.com</span></span>  <br/> <span data-ttu-id="8fce5-141">OCSP.Thawte.com</span><span class="sxs-lookup"><span data-stu-id="8fce5-141">ocsp.thawte.com</span></span>  <br/> <span data-ttu-id="8fce5-142">ocsp2.GlobalSign.com</span><span class="sxs-lookup"><span data-stu-id="8fce5-142">ocsp2.globalsign.com</span></span>  <br/> <span data-ttu-id="8fce5-143">ocspcnnicroot.cnnic.CN</span><span class="sxs-lookup"><span data-stu-id="8fce5-143">ocspcnnicroot.cnnic.cn</span></span>  <br/> <span data-ttu-id="8fce5-144">raiz-c3-ca2-2009.ocsp.d-trust.net</span><span class="sxs-lookup"><span data-stu-id="8fce5-144">root-c3-ca2-2009.ocsp.d-trust.net</span></span>  <br/> <span data-ttu-id="8fce5-145">root-C3-ca2-EV-2009.OCSP.d-Trust.NET</span><span class="sxs-lookup"><span data-stu-id="8fce5-145">root-c3-ca2-ev-2009.ocsp.d-trust.net</span></span>  <br/> <span data-ttu-id="8fce5-146">S2.symcb.com</span><span class="sxs-lookup"><span data-stu-id="8fce5-146">s2.symcb.com</span></span>  <br/> |<span data-ttu-id="8fce5-147">AIA.startssl.com</span><span class="sxs-lookup"><span data-stu-id="8fce5-147">aia.startssl.com</span></span>  <br/> <span data-ttu-id="8fce5-148">Apps.identrust.com</span><span class="sxs-lookup"><span data-stu-id="8fce5-148">apps.identrust.com</span></span>  <br/> <span data-ttu-id="8fce5-149">cacert.omniroot.com</span><span class="sxs-lookup"><span data-stu-id="8fce5-149">cacert.omniroot.com</span></span>  <br/> <span data-ttu-id="8fce5-150">www.cnnic.CN</span><span class="sxs-lookup"><span data-stu-id="8fce5-150">www.cnnic.cn</span></span>  <br/> |
   
<span data-ttu-id="8fce5-151">Expanda a raiz e intermediárias seções abaixo para ver detalhes adicionais sobre os provedores de certificado.</span><span class="sxs-lookup"><span data-stu-id="8fce5-151">Expand the root and intermediate sections below to see additional details about the certificate providers.</span></span>
  
## <a name="office-365-root-certificate-details"></a><span data-ttu-id="8fce5-152">O Office 365 detalhes do certificado raiz</span><span class="sxs-lookup"><span data-stu-id="8fce5-152">Office 365 Root Certificate Details</span></span>
<span data-ttu-id="8fce5-153"><a name="RootCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="8fce5-153"></span></span>

 <span data-ttu-id="8fce5-154">**Baltimore CyberTrust Root**</span><span class="sxs-lookup"><span data-stu-id="8fce5-154">**Baltimore CyberTrust Root**</span></span>
  
<span data-ttu-id="8fce5-155">|:-----|</span><span class="sxs-lookup"><span data-stu-id="8fce5-155">|:-----|</span></span>
|<span data-ttu-id="8fce5-156">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-156">**Subject**</span></span>|
|:-----|
|<span data-ttu-id="8fce5-157">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="8fce5-157">**Serial Number**</span></span>|
|<span data-ttu-id="8fce5-158">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-158"></span></span>|
|<span data-ttu-id="8fce5-159">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="8fce5-159">**Public Key Length**</span></span>|
|<span data-ttu-id="8fce5-160">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-160"></span></span>|
|<span data-ttu-id="8fce5-161">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="8fce5-161">**Signature Algorithm**</span></span>|
|<span data-ttu-id="8fce5-162">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-162"></span></span>|
|<span data-ttu-id="8fce5-163">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-163">**Validity Not Before**</span></span>|
|<span data-ttu-id="8fce5-164">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-164"></span></span>|
|<span data-ttu-id="8fce5-165">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="8fce5-165">**Validity Not After**</span></span>|
|<span data-ttu-id="8fce5-166">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-166"></span></span>|
|<span data-ttu-id="8fce5-167">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-167">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-168">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-168"></span></span>|
|<span data-ttu-id="8fce5-169">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-169">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="8fce5-170">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-170"></span></span>|
|<span data-ttu-id="8fce5-171">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-171">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-172">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-172"></span></span>|
|<span data-ttu-id="8fce5-173">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-173">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-174">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-174"></span></span>|
   
 <span data-ttu-id="8fce5-175">**RAIZ CNNIC**</span><span class="sxs-lookup"><span data-stu-id="8fce5-175">**CNNIC ROOT**</span></span>
  
||
|:-----|
|<span data-ttu-id="8fce5-176">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-176">**Subject**</span></span>|
|<span data-ttu-id="8fce5-177">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-177"></span></span>|
|<span data-ttu-id="8fce5-178">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="8fce5-178">**Serial Number**</span></span>|
|<span data-ttu-id="8fce5-179">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-179"></span></span>|
|<span data-ttu-id="8fce5-180">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="8fce5-180">**Public Key Length**</span></span>|
|<span data-ttu-id="8fce5-181">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-181"></span></span>|
|<span data-ttu-id="8fce5-182">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="8fce5-182">**Signature Algorithm**</span></span>|
|<span data-ttu-id="8fce5-183">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-183"></span></span>|
|<span data-ttu-id="8fce5-184">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-184">**Validity Not Before**</span></span>|
|<span data-ttu-id="8fce5-185">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-185"></span></span>|
|<span data-ttu-id="8fce5-186">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="8fce5-186">**Validity Not After**</span></span>|
|<span data-ttu-id="8fce5-187">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-187"></span></span>|
|<span data-ttu-id="8fce5-188">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-188">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-189">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-189"></span></span>|
|<span data-ttu-id="8fce5-190">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-190">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-191">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-191"></span></span>|
|<span data-ttu-id="8fce5-192">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-192">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="8fce5-193">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-193"></span></span>|
|<span data-ttu-id="8fce5-194">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-194">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-195">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-195"></span></span>|
|<span data-ttu-id="8fce5-196">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-196">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-197">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-197"></span></span>|
   
 <span data-ttu-id="8fce5-198">**CA de raiz Global DigiCert**</span><span class="sxs-lookup"><span data-stu-id="8fce5-198">**DigiCert Global Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="8fce5-199">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-199">**Subject**</span></span>|
|<span data-ttu-id="8fce5-200">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-200"></span></span>|
|<span data-ttu-id="8fce5-201">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="8fce5-201">**Serial Number**</span></span>|
|<span data-ttu-id="8fce5-202">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-202"></span></span>|
|<span data-ttu-id="8fce5-203">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="8fce5-203">**Public Key Length**</span></span>|
|<span data-ttu-id="8fce5-204">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-204"></span></span>|
|<span data-ttu-id="8fce5-205">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="8fce5-205">**Signature Algorithm**</span></span>|
|<span data-ttu-id="8fce5-206">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-206"></span></span>|
|<span data-ttu-id="8fce5-207">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-207">**Validity Not Before**</span></span>|
|<span data-ttu-id="8fce5-208">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-208"></span></span>|
|<span data-ttu-id="8fce5-209">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="8fce5-209">**Validity Not After**</span></span>|
|<span data-ttu-id="8fce5-210">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-210"></span></span>|
|<span data-ttu-id="8fce5-211">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-211">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-212">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-212"></span></span>|
|<span data-ttu-id="8fce5-213">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-213">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-214">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-214"></span></span>|
|<span data-ttu-id="8fce5-215">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-215">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="8fce5-216">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-216"></span></span>|
|<span data-ttu-id="8fce5-217">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-217">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-218">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-218"></span></span>|
|<span data-ttu-id="8fce5-219">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-219">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-220">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-220"></span></span>|
   
 <span data-ttu-id="8fce5-221">**Autoridade de certificação de raiz de garantia EV alta DigiCert**</span><span class="sxs-lookup"><span data-stu-id="8fce5-221">**DigiCert High Assurance EV Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="8fce5-222">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-222">**Subject**</span></span>|
|<span data-ttu-id="8fce5-223">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-223"></span></span>|
|<span data-ttu-id="8fce5-224">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="8fce5-224">**Serial Number**</span></span>|
|<span data-ttu-id="8fce5-225">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-225"></span></span>|
|<span data-ttu-id="8fce5-226">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="8fce5-226">**Public Key Length**</span></span>|
|<span data-ttu-id="8fce5-227">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-227"></span></span>|
|<span data-ttu-id="8fce5-228">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="8fce5-228">**Signature Algorithm**</span></span>|
|<span data-ttu-id="8fce5-229">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-229"></span></span>|
|<span data-ttu-id="8fce5-230">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-230">**Validity Not Before**</span></span>|
|<span data-ttu-id="8fce5-231">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-231"></span></span>|
|<span data-ttu-id="8fce5-232">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="8fce5-232">**Validity Not After**</span></span>|
|<span data-ttu-id="8fce5-233">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-233"></span></span>|
|<span data-ttu-id="8fce5-234">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-234">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-235">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-235"></span></span>|
|<span data-ttu-id="8fce5-236">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-236">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-237">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-237"></span></span>|
|<span data-ttu-id="8fce5-238">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-238">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="8fce5-239">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-239"></span></span>|
|<span data-ttu-id="8fce5-240">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-240">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-241">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-241"></span></span>|
|<span data-ttu-id="8fce5-242">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-242">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-243">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-243"></span></span>|
   
 <span data-ttu-id="8fce5-244">**Autoridade de certificação da classe 3 de raiz de confiança D 2 de 2009**</span><span class="sxs-lookup"><span data-stu-id="8fce5-244">**D-TRUST Root Class 3 CA 2 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="8fce5-245">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-245">**Subject**</span></span>|
|<span data-ttu-id="8fce5-246">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-246"></span></span>|
|<span data-ttu-id="8fce5-247">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="8fce5-247">**Serial Number**</span></span>|
|<span data-ttu-id="8fce5-248">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-248"></span></span>|
|<span data-ttu-id="8fce5-249">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="8fce5-249">**Public Key Length**</span></span>|
|<span data-ttu-id="8fce5-250">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-250"></span></span>|
|<span data-ttu-id="8fce5-251">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="8fce5-251">**Signature Algorithm**</span></span>|
|<span data-ttu-id="8fce5-252">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-252"></span></span>|
|<span data-ttu-id="8fce5-253">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-253">**Validity Not Before**</span></span>|
|<span data-ttu-id="8fce5-254">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-254"></span></span>|
|<span data-ttu-id="8fce5-255">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="8fce5-255">**Validity Not After**</span></span>|
|<span data-ttu-id="8fce5-256">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-256"></span></span>|
|<span data-ttu-id="8fce5-257">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-257">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-258">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-258"></span></span>|
|<span data-ttu-id="8fce5-259">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-259">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="8fce5-260">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-260"></span></span>|
|<span data-ttu-id="8fce5-261">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-261">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-262">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-262"></span></span>|
|<span data-ttu-id="8fce5-263">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-263">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-264">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-264"></span></span>|
|<span data-ttu-id="8fce5-265">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="8fce5-265">**CRL URLs**</span></span>|
|<span data-ttu-id="8fce5-266">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-266"></span></span>|
   
 <span data-ttu-id="8fce5-267">**Autoridade de certificação raiz confiável D classe 3 2 EV de 2009**</span><span class="sxs-lookup"><span data-stu-id="8fce5-267">**D-TRUST Root Class 3 CA 2 EV 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="8fce5-268">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-268">**Subject**</span></span>|
|<span data-ttu-id="8fce5-269">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-269"></span></span>|
|<span data-ttu-id="8fce5-270">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="8fce5-270">**Serial Number**</span></span>|
|<span data-ttu-id="8fce5-271">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-271"></span></span>|
|<span data-ttu-id="8fce5-272">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="8fce5-272">**Public Key Length**</span></span>|
|<span data-ttu-id="8fce5-273">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-273"></span></span>|
|<span data-ttu-id="8fce5-274">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="8fce5-274">**Signature Algorithm**</span></span>|
|<span data-ttu-id="8fce5-275">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-275"></span></span>|
|<span data-ttu-id="8fce5-276">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-276">**Validity Not Before**</span></span>|
|<span data-ttu-id="8fce5-277">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-277"></span></span>|
|<span data-ttu-id="8fce5-278">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="8fce5-278">**Validity Not After**</span></span>|
|<span data-ttu-id="8fce5-279">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-279"></span></span>|
|<span data-ttu-id="8fce5-280">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-280">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-281">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-281"></span></span>|
|<span data-ttu-id="8fce5-282">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-282">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="8fce5-283">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-283"></span></span>|
|<span data-ttu-id="8fce5-284">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-284">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-285">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-285"></span></span>|
|<span data-ttu-id="8fce5-286">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-286">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-287">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-287"></span></span>|
|<span data-ttu-id="8fce5-288">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="8fce5-288">**CRL URLs**</span></span>|
|<span data-ttu-id="8fce5-289">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-289"></span></span>|
   
 <span data-ttu-id="8fce5-290">**Horário de verão raiz da autoridade de certificação X3**</span><span class="sxs-lookup"><span data-stu-id="8fce5-290">**DST Root CA X3**</span></span>
  
||
|:-----|
|<span data-ttu-id="8fce5-291">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-291">**Subject**</span></span>|
|<span data-ttu-id="8fce5-292">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-292"></span></span>|
|<span data-ttu-id="8fce5-293">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="8fce5-293">**Serial Number**</span></span>|
|<span data-ttu-id="8fce5-294">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-294"></span></span>|
|<span data-ttu-id="8fce5-295">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="8fce5-295">**Public Key Length**</span></span>|
|<span data-ttu-id="8fce5-296">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-296"></span></span>|
|<span data-ttu-id="8fce5-297">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="8fce5-297">**Signature Algorithm**</span></span>|
|<span data-ttu-id="8fce5-298">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-298"></span></span>|
|<span data-ttu-id="8fce5-299">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-299">**Validity Not Before**</span></span>|
|<span data-ttu-id="8fce5-300">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-300"></span></span>|
|<span data-ttu-id="8fce5-301">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="8fce5-301">**Validity Not After**</span></span>|
|<span data-ttu-id="8fce5-302">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-302"></span></span>|
|<span data-ttu-id="8fce5-303">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-303">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-304">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-304"></span></span>|
|<span data-ttu-id="8fce5-305">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-305">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="8fce5-306">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-306"></span></span>|
|<span data-ttu-id="8fce5-307">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-307">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-308">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-308"></span></span>|
|<span data-ttu-id="8fce5-309">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-309">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-310">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-310"></span></span>|
   
 <span data-ttu-id="8fce5-311">**Entrust autoridade de certificação raiz - G2**</span><span class="sxs-lookup"><span data-stu-id="8fce5-311">**Entrust Root Certification Authority - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="8fce5-312">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-312">**Subject**</span></span>|
|<span data-ttu-id="8fce5-313">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-313"></span></span>|
|<span data-ttu-id="8fce5-314">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="8fce5-314">**Serial Number**</span></span>|
|<span data-ttu-id="8fce5-315">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-315"></span></span>|
|<span data-ttu-id="8fce5-316">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="8fce5-316">**Public Key Length**</span></span>|
|<span data-ttu-id="8fce5-317">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-317"></span></span>|
|<span data-ttu-id="8fce5-318">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="8fce5-318">**Signature Algorithm**</span></span>|
|<span data-ttu-id="8fce5-319">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-319"></span></span>|
|<span data-ttu-id="8fce5-320">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-320">**Validity Not Before**</span></span>|
|<span data-ttu-id="8fce5-321">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-321"></span></span>|
|<span data-ttu-id="8fce5-322">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="8fce5-322">**Validity Not After**</span></span>|
|<span data-ttu-id="8fce5-323">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-323"></span></span>|
|<span data-ttu-id="8fce5-324">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-324">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-325">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-325"></span></span>|
|<span data-ttu-id="8fce5-326">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-326">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="8fce5-327">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-327"></span></span>|
|<span data-ttu-id="8fce5-328">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-328">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-329">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-329"></span></span>|
|<span data-ttu-id="8fce5-330">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-330">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-331">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-331"></span></span>|
   
 <span data-ttu-id="8fce5-332">**Entrust.net Certification Authority (2048)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-332">**Entrust.net Certification Authority (2048)**</span></span>
  
||
|:-----|
|<span data-ttu-id="8fce5-333">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-333">**Subject**</span></span>|
|<span data-ttu-id="8fce5-334">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-334"></span></span>|
|<span data-ttu-id="8fce5-335">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="8fce5-335">**Serial Number**</span></span>|
|<span data-ttu-id="8fce5-336">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-336"></span></span>|
|<span data-ttu-id="8fce5-337">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="8fce5-337">**Public Key Length**</span></span>|
|<span data-ttu-id="8fce5-338">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-338"></span></span>|
|<span data-ttu-id="8fce5-339">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="8fce5-339">**Signature Algorithm**</span></span>|
|<span data-ttu-id="8fce5-340">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-340"></span></span>|
|<span data-ttu-id="8fce5-341">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-341">**Validity Not Before**</span></span>|
|<span data-ttu-id="8fce5-342">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-342"></span></span>|
|<span data-ttu-id="8fce5-343">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="8fce5-343">**Validity Not After**</span></span>|
|<span data-ttu-id="8fce5-344">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-344"></span></span>|
|<span data-ttu-id="8fce5-345">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-345">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-346">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-346"></span></span>|
|<span data-ttu-id="8fce5-347">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-347">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="8fce5-348">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-348"></span></span>|
|<span data-ttu-id="8fce5-349">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-349">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-350">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-350"></span></span>|
|<span data-ttu-id="8fce5-351">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-351">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-352">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-352"></span></span>|
   
 <span data-ttu-id="8fce5-353">**GlobalSign**</span><span class="sxs-lookup"><span data-stu-id="8fce5-353">**GlobalSign**</span></span>
  
||
|:-----|
|<span data-ttu-id="8fce5-354">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-354">**Subject**</span></span>|
|<span data-ttu-id="8fce5-355">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-355"></span></span>|
|<span data-ttu-id="8fce5-356">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="8fce5-356">**Serial Number**</span></span>|
|<span data-ttu-id="8fce5-357">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-357"></span></span>|
|<span data-ttu-id="8fce5-358">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="8fce5-358">**Public Key Length**</span></span>|
|<span data-ttu-id="8fce5-359">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-359"></span></span>|
|<span data-ttu-id="8fce5-360">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="8fce5-360">**Signature Algorithm**</span></span>|
|<span data-ttu-id="8fce5-361">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-361"></span></span>|
|<span data-ttu-id="8fce5-362">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-362">**Validity Not Before**</span></span>|
|<span data-ttu-id="8fce5-363">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-363"></span></span>|
|<span data-ttu-id="8fce5-364">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="8fce5-364">**Validity Not After**</span></span>|
|<span data-ttu-id="8fce5-365">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-365"></span></span>|
|<span data-ttu-id="8fce5-366">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-366">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-367">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-367"></span></span>|
|<span data-ttu-id="8fce5-368">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-368">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-369">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-369"></span></span>|
|<span data-ttu-id="8fce5-370">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-370">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="8fce5-371">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-371"></span></span>|
|<span data-ttu-id="8fce5-372">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-372">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-373">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-373"></span></span>|
|<span data-ttu-id="8fce5-374">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-374">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-375">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-375"></span></span>|
|<span data-ttu-id="8fce5-376">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="8fce5-376">**CRL URLs**</span></span>|
|<span data-ttu-id="8fce5-377">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-377"></span></span>|
   
 <span data-ttu-id="8fce5-378">**GlobalSign Root CA**</span><span class="sxs-lookup"><span data-stu-id="8fce5-378">**GlobalSign Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="8fce5-379">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-379">**Subject**</span></span>|
|<span data-ttu-id="8fce5-380">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-380"></span></span>|
|<span data-ttu-id="8fce5-381">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="8fce5-381">**Serial Number**</span></span>|
|<span data-ttu-id="8fce5-382">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-382"></span></span>|
|<span data-ttu-id="8fce5-383">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="8fce5-383">**Public Key Length**</span></span>|
|<span data-ttu-id="8fce5-384">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-384"></span></span>|
|<span data-ttu-id="8fce5-385">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="8fce5-385">**Signature Algorithm**</span></span>|
|<span data-ttu-id="8fce5-386">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-386"></span></span>|
|<span data-ttu-id="8fce5-387">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-387">**Validity Not Before**</span></span>|
|<span data-ttu-id="8fce5-388">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-388"></span></span>|
|<span data-ttu-id="8fce5-389">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="8fce5-389">**Validity Not After**</span></span>|
|<span data-ttu-id="8fce5-390">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-390"></span></span>|
|<span data-ttu-id="8fce5-391">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-391">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-392">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-392"></span></span>|
|<span data-ttu-id="8fce5-393">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-393">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="8fce5-394">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-394"></span></span>|
|<span data-ttu-id="8fce5-395">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-395">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-396">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-396"></span></span>|
|<span data-ttu-id="8fce5-397">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-397">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-398">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-398"></span></span>|
   
 <span data-ttu-id="8fce5-399">**Thawte autoridade de certificação raiz primária - G3**</span><span class="sxs-lookup"><span data-stu-id="8fce5-399">**thawte Primary Root CA - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="8fce5-400">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-400">**Subject**</span></span>|
|<span data-ttu-id="8fce5-401">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-401"></span></span>|
|<span data-ttu-id="8fce5-402">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="8fce5-402">**Serial Number**</span></span>|
|<span data-ttu-id="8fce5-403">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-403"></span></span>|
|<span data-ttu-id="8fce5-404">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="8fce5-404">**Public Key Length**</span></span>|
|<span data-ttu-id="8fce5-405">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-405"></span></span>|
|<span data-ttu-id="8fce5-406">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="8fce5-406">**Signature Algorithm**</span></span>|
|<span data-ttu-id="8fce5-407">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-407"></span></span>|
|<span data-ttu-id="8fce5-408">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-408">**Validity Not Before**</span></span>|
|<span data-ttu-id="8fce5-409">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-409"></span></span>|
|<span data-ttu-id="8fce5-410">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="8fce5-410">**Validity Not After**</span></span>|
|<span data-ttu-id="8fce5-411">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-411"></span></span>|
|<span data-ttu-id="8fce5-412">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-412">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-413">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-413"></span></span>|
|<span data-ttu-id="8fce5-414">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-414">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="8fce5-415">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-415"></span></span>|
|<span data-ttu-id="8fce5-416">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-416">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-417">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-417"></span></span>|
|<span data-ttu-id="8fce5-418">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-418">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-419">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-419"></span></span>|
   
 <span data-ttu-id="8fce5-420">**Autoridade de certificação principal pública classe VeriSign 3 - G5**</span><span class="sxs-lookup"><span data-stu-id="8fce5-420">**VeriSign Class 3 Public Primary Certification Authority - G5**</span></span>
  
||
|:-----|
|<span data-ttu-id="8fce5-421">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-421">**Subject**</span></span>|
|<span data-ttu-id="8fce5-422">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-422"></span></span>|
|<span data-ttu-id="8fce5-423">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="8fce5-423">**Serial Number**</span></span>|
|<span data-ttu-id="8fce5-424">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-424"></span></span>|
|<span data-ttu-id="8fce5-425">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="8fce5-425">**Public Key Length**</span></span>|
|<span data-ttu-id="8fce5-426">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-426"></span></span>|
|<span data-ttu-id="8fce5-427">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="8fce5-427">**Signature Algorithm**</span></span>|
|<span data-ttu-id="8fce5-428">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-428"></span></span>|
|<span data-ttu-id="8fce5-429">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-429">**Validity Not Before**</span></span>|
|<span data-ttu-id="8fce5-430">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-430"></span></span>|
|<span data-ttu-id="8fce5-431">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="8fce5-431">**Validity Not After**</span></span>|
|<span data-ttu-id="8fce5-432">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-432"></span></span>|
|<span data-ttu-id="8fce5-433">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-433">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-434">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-434"></span></span>|
|<span data-ttu-id="8fce5-435">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-435">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="8fce5-436">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-436"></span></span>|
|<span data-ttu-id="8fce5-437">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-437">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-438">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-438"></span></span>|
|<span data-ttu-id="8fce5-439">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-439">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-440">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-440"></span></span>|
   
## <a name="office-365-intermediate-certificate-details"></a><span data-ttu-id="8fce5-441">Detalhes do certificado intermediário de Office 365</span><span class="sxs-lookup"><span data-stu-id="8fce5-441">Office 365 Intermediate Certificate Details</span></span>
<span data-ttu-id="8fce5-442"><a name="IntermediateCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="8fce5-442"></span></span>

 <span data-ttu-id="8fce5-443">**CNNIC SHA256 SSL**</span><span class="sxs-lookup"><span data-stu-id="8fce5-443">**CNNIC SHA256 SSL**</span></span>
  
||
|:-----|
|<span data-ttu-id="8fce5-444">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-444">**Subject**</span></span>|
|<span data-ttu-id="8fce5-445">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-445"></span></span>|
|<span data-ttu-id="8fce5-446">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="8fce5-446">**Issuer**</span></span>|
|<span data-ttu-id="8fce5-447">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-447"></span></span>|
|<span data-ttu-id="8fce5-448">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="8fce5-448">**Serial Number**</span></span>|
|<span data-ttu-id="8fce5-449">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-449"></span></span>|
|<span data-ttu-id="8fce5-450">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="8fce5-450">**Public Key Length**</span></span>|
|<span data-ttu-id="8fce5-451">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-451"></span></span>|
|<span data-ttu-id="8fce5-452">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="8fce5-452">**Signature Algorithm**</span></span>|
|<span data-ttu-id="8fce5-453">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-453"></span></span>|
|<span data-ttu-id="8fce5-454">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-454">**Validity Not Before**</span></span>|
|<span data-ttu-id="8fce5-455">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-455"></span></span>|
|<span data-ttu-id="8fce5-456">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="8fce5-456">**Validity Not After**</span></span>|
|<span data-ttu-id="8fce5-457">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-457"></span></span>|
|<span data-ttu-id="8fce5-458">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-458">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-459">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-459"></span></span>|
|<span data-ttu-id="8fce5-460">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-460">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-461">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-461"></span></span>|
|<span data-ttu-id="8fce5-462">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-462">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="8fce5-463">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-463"></span></span>|
|<span data-ttu-id="8fce5-464">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-464">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-465">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-465"></span></span>|
|<span data-ttu-id="8fce5-466">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-466">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-467">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-467"></span></span>|
|<span data-ttu-id="8fce5-468">**URLs AIA**</span><span class="sxs-lookup"><span data-stu-id="8fce5-468">**AIA URLs**</span></span>|
|<span data-ttu-id="8fce5-469">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-469"></span></span>|
|<span data-ttu-id="8fce5-470">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="8fce5-470">**CRL URLs**</span></span>|
|<span data-ttu-id="8fce5-471">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-471"></span></span>|
|<span data-ttu-id="8fce5-472">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="8fce5-472">**OCSP URLs**</span></span>|
|<span data-ttu-id="8fce5-473">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-473"></span></span>|
   
 <span data-ttu-id="8fce5-474">**D-TRUST SSL classe 3 CA 1 2009**</span><span class="sxs-lookup"><span data-stu-id="8fce5-474">**D-TRUST SSL Class 3 CA 1 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="8fce5-475">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-475">**Subject**</span></span>|
|<span data-ttu-id="8fce5-476">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-476"></span></span>|
|<span data-ttu-id="8fce5-477">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="8fce5-477">**Issuer**</span></span>|
|<span data-ttu-id="8fce5-478">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-478"></span></span>|
|<span data-ttu-id="8fce5-479">**Nome alternativo da entidade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-479">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="8fce5-480">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-480"></span></span>|
|<span data-ttu-id="8fce5-481">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="8fce5-481">**Serial Number**</span></span>|
|<span data-ttu-id="8fce5-482">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-482"></span></span>|
|<span data-ttu-id="8fce5-483">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="8fce5-483">**Public Key Length**</span></span>|
|<span data-ttu-id="8fce5-484">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-484"></span></span>|
|<span data-ttu-id="8fce5-485">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="8fce5-485">**Signature Algorithm**</span></span>|
|<span data-ttu-id="8fce5-486">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-486"></span></span>|
|<span data-ttu-id="8fce5-487">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-487">**Validity Not Before**</span></span>|
|<span data-ttu-id="8fce5-488">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-488"></span></span>|
|<span data-ttu-id="8fce5-489">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="8fce5-489">**Validity Not After**</span></span>|
|<span data-ttu-id="8fce5-490">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-490"></span></span>|
|<span data-ttu-id="8fce5-491">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-491">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-492">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-492"></span></span>|
|<span data-ttu-id="8fce5-493">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-493">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-494">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-494"></span></span>|
|<span data-ttu-id="8fce5-495">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-495">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="8fce5-496">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-496"></span></span>|
|<span data-ttu-id="8fce5-497">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-497">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-498">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-498"></span></span>|
|<span data-ttu-id="8fce5-499">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-499">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-500">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-500"></span></span>|
|<span data-ttu-id="8fce5-501">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="8fce5-501">**CRL URLs**</span></span>|
|<span data-ttu-id="8fce5-502">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-502"></span></span>|
|<span data-ttu-id="8fce5-503">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="8fce5-503">**OCSP URLs**</span></span>|
|<span data-ttu-id="8fce5-504">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-504"></span></span>|
   
 <span data-ttu-id="8fce5-505">**Autoridade de certificação confiável D SSL classe 3 1 EV de 2009**</span><span class="sxs-lookup"><span data-stu-id="8fce5-505">**D-TRUST SSL Class 3 CA 1 EV 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="8fce5-506">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-506">**Subject**</span></span>|
|<span data-ttu-id="8fce5-507">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-507"></span></span>|
|<span data-ttu-id="8fce5-508">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="8fce5-508">**Issuer**</span></span>|
|<span data-ttu-id="8fce5-509">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-509"></span></span>|
|<span data-ttu-id="8fce5-510">**Nome alternativo da entidade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-510">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="8fce5-511">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-511"></span></span>|
|<span data-ttu-id="8fce5-512">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="8fce5-512">**Serial Number**</span></span>|
|<span data-ttu-id="8fce5-513">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-513"></span></span>|
|<span data-ttu-id="8fce5-514">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="8fce5-514">**Public Key Length**</span></span>|
|<span data-ttu-id="8fce5-515">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-515"></span></span>|
|<span data-ttu-id="8fce5-516">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="8fce5-516">**Signature Algorithm**</span></span>|
|<span data-ttu-id="8fce5-517">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-517"></span></span>|
|<span data-ttu-id="8fce5-518">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-518">**Validity Not Before**</span></span>|
|<span data-ttu-id="8fce5-519">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-519"></span></span>|
|<span data-ttu-id="8fce5-520">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="8fce5-520">**Validity Not After**</span></span>|
|<span data-ttu-id="8fce5-521">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-521"></span></span>|
|<span data-ttu-id="8fce5-522">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-522">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-523">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-523"></span></span>|
|<span data-ttu-id="8fce5-524">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-524">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-525">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-525"></span></span>|
|<span data-ttu-id="8fce5-526">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-526">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="8fce5-527">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-527"></span></span>|
|<span data-ttu-id="8fce5-528">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-528">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-529">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-529"></span></span>|
|<span data-ttu-id="8fce5-530">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-530">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-531">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-531"></span></span>|
|<span data-ttu-id="8fce5-532">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="8fce5-532">**CRL URLs**</span></span>|
|<span data-ttu-id="8fce5-533">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-533"></span></span>|
|<span data-ttu-id="8fce5-534">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="8fce5-534">**OCSP URLs**</span></span>|
|<span data-ttu-id="8fce5-535">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-535"></span></span>|
   
 <span data-ttu-id="8fce5-536">**Serviços em nuvem de DigiCert CA-1**</span><span class="sxs-lookup"><span data-stu-id="8fce5-536">**DigiCert Cloud Services CA-1**</span></span>
  
||
|:-----|
|<span data-ttu-id="8fce5-537">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-537">**Subject**</span></span>|
|<span data-ttu-id="8fce5-538">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-538"></span></span>|
|<span data-ttu-id="8fce5-539">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="8fce5-539">**Issuer**</span></span>|
|<span data-ttu-id="8fce5-540">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-540"></span></span>|
|<span data-ttu-id="8fce5-541">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="8fce5-541">**Serial Number**</span></span>|
|<span data-ttu-id="8fce5-542">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-542"></span></span>|
|<span data-ttu-id="8fce5-543">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="8fce5-543">**Public Key Length**</span></span>|
|<span data-ttu-id="8fce5-544">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-544"></span></span>|
|<span data-ttu-id="8fce5-545">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="8fce5-545">**Signature Algorithm**</span></span>|
|<span data-ttu-id="8fce5-546">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-546"></span></span>|
|<span data-ttu-id="8fce5-547">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-547">**Validity Not Before**</span></span>|
|<span data-ttu-id="8fce5-548">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-548"></span></span>|
|<span data-ttu-id="8fce5-549">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="8fce5-549">**Validity Not After**</span></span>|
|<span data-ttu-id="8fce5-550">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-550"></span></span>|
|<span data-ttu-id="8fce5-551">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-551">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-552">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-552"></span></span>|
|<span data-ttu-id="8fce5-553">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-553">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-554">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-554"></span></span>|
|<span data-ttu-id="8fce5-555">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-555">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="8fce5-556">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-556"></span></span>|
|<span data-ttu-id="8fce5-557">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-557">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-558">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-558"></span></span>|
|<span data-ttu-id="8fce5-559">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-559">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-560">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-560"></span></span>|
|<span data-ttu-id="8fce5-561">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="8fce5-561">**CRL URLs**</span></span>|
|<span data-ttu-id="8fce5-562">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-562"></span></span>|
|<span data-ttu-id="8fce5-563">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="8fce5-563">**OCSP URLs**</span></span>|
|<span data-ttu-id="8fce5-564">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-564"></span></span>|
   
 <span data-ttu-id="8fce5-565">**Servidor de alta garantia DigiCert SHA2 CA**</span><span class="sxs-lookup"><span data-stu-id="8fce5-565">**DigiCert SHA2 High Assurance Server CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="8fce5-566">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-566">**Subject**</span></span>|
|<span data-ttu-id="8fce5-567">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-567"></span></span>|
|<span data-ttu-id="8fce5-568">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="8fce5-568">**Issuer**</span></span>|
|<span data-ttu-id="8fce5-569">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-569"></span></span>|
|<span data-ttu-id="8fce5-570">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="8fce5-570">**Serial Number**</span></span>|
|<span data-ttu-id="8fce5-571">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-571"></span></span>|
|<span data-ttu-id="8fce5-572">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="8fce5-572">**Public Key Length**</span></span>|
|<span data-ttu-id="8fce5-573">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-573"></span></span>|
|<span data-ttu-id="8fce5-574">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="8fce5-574">**Signature Algorithm**</span></span>|
|<span data-ttu-id="8fce5-575">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-575"></span></span>|
|<span data-ttu-id="8fce5-576">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-576">**Validity Not Before**</span></span>|
|<span data-ttu-id="8fce5-577">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-577"></span></span>|
|<span data-ttu-id="8fce5-578">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="8fce5-578">**Validity Not After**</span></span>|
|<span data-ttu-id="8fce5-579">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-579"></span></span>|
|<span data-ttu-id="8fce5-580">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-580">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-581">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-581"></span></span>|
|<span data-ttu-id="8fce5-582">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-582">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-583">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-583"></span></span>|
|<span data-ttu-id="8fce5-584">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-584">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="8fce5-585">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-585"></span></span>|
|<span data-ttu-id="8fce5-586">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-586">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-587">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-587"></span></span>|
|<span data-ttu-id="8fce5-588">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-588">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-589">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-589"></span></span>|
|<span data-ttu-id="8fce5-590">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="8fce5-590">**CRL URLs**</span></span>|
|<span data-ttu-id="8fce5-591">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-591"></span></span>|
|<span data-ttu-id="8fce5-592">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="8fce5-592">**OCSP URLs**</span></span>|
|<span data-ttu-id="8fce5-593">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-593"></span></span>|
   
 <span data-ttu-id="8fce5-594">**Servidores de seguros DigiCert SHA2 CA**</span><span class="sxs-lookup"><span data-stu-id="8fce5-594">**DigiCert SHA2 Secure Server CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="8fce5-595">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-595">**Subject**</span></span>|
|<span data-ttu-id="8fce5-596">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-596"></span></span>|
|<span data-ttu-id="8fce5-597">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="8fce5-597">**Issuer**</span></span>|
|<span data-ttu-id="8fce5-598">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-598"></span></span>|
|<span data-ttu-id="8fce5-599">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="8fce5-599">**Serial Number**</span></span>|
|<span data-ttu-id="8fce5-600">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-600"></span></span>|
|<span data-ttu-id="8fce5-601">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="8fce5-601">**Public Key Length**</span></span>|
|<span data-ttu-id="8fce5-602">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-602"></span></span>|
|<span data-ttu-id="8fce5-603">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="8fce5-603">**Signature Algorithm**</span></span>|
|<span data-ttu-id="8fce5-604">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-604"></span></span>|
|<span data-ttu-id="8fce5-605">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-605">**Validity Not Before**</span></span>|
|<span data-ttu-id="8fce5-606">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-606"></span></span>|
|<span data-ttu-id="8fce5-607">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="8fce5-607">**Validity Not After**</span></span>|
|<span data-ttu-id="8fce5-608">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-608"></span></span>|
|<span data-ttu-id="8fce5-609">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-609">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-610">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-610"></span></span>|
|<span data-ttu-id="8fce5-611">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-611">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-612">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-612"></span></span>|
|<span data-ttu-id="8fce5-613">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-613">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="8fce5-614">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-614"></span></span>|
|<span data-ttu-id="8fce5-615">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-615">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-616">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-616"></span></span>|
|<span data-ttu-id="8fce5-617">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-617">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-618">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-618"></span></span>|
|<span data-ttu-id="8fce5-619">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="8fce5-619">**CRL URLs**</span></span>|
|<span data-ttu-id="8fce5-620">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-620"></span></span>|
|<span data-ttu-id="8fce5-621">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="8fce5-621">**OCSP URLs**</span></span>|
|<span data-ttu-id="8fce5-622">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-622"></span></span>|
   
 <span data-ttu-id="8fce5-623">**Entrust autoridade de certificação - L1C**</span><span class="sxs-lookup"><span data-stu-id="8fce5-623">**Entrust Certification Authority - L1C**</span></span>
  
||
|:-----|
|<span data-ttu-id="8fce5-624">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-624">**Subject**</span></span>|
|<span data-ttu-id="8fce5-625">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-625"></span></span>|
|<span data-ttu-id="8fce5-626">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="8fce5-626">**Issuer**</span></span>|
|<span data-ttu-id="8fce5-627">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-627"></span></span>|
|<span data-ttu-id="8fce5-628">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="8fce5-628">**Serial Number**</span></span>|
|<span data-ttu-id="8fce5-629">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-629"></span></span>|
|<span data-ttu-id="8fce5-630">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="8fce5-630">**Public Key Length**</span></span>|
|<span data-ttu-id="8fce5-631">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-631"></span></span>|
|<span data-ttu-id="8fce5-632">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="8fce5-632">**Signature Algorithm**</span></span>|
|<span data-ttu-id="8fce5-633">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-633"></span></span>|
|<span data-ttu-id="8fce5-634">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-634">**Validity Not Before**</span></span>|
|<span data-ttu-id="8fce5-635">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-635"></span></span>|
|<span data-ttu-id="8fce5-636">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="8fce5-636">**Validity Not After**</span></span>|
|<span data-ttu-id="8fce5-637">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-637"></span></span>|
|<span data-ttu-id="8fce5-638">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-638">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-639">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-639"></span></span>|
|<span data-ttu-id="8fce5-640">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-640">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-641">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-641"></span></span>|
|<span data-ttu-id="8fce5-642">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-642">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="8fce5-643">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-643"></span></span>|
|<span data-ttu-id="8fce5-644">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-644">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-645">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-645"></span></span>|
|<span data-ttu-id="8fce5-646">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-646">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-647">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-647"></span></span>|
|<span data-ttu-id="8fce5-648">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="8fce5-648">**CRL URLs**</span></span>|
|<span data-ttu-id="8fce5-649">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-649"></span></span>|
|<span data-ttu-id="8fce5-650">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="8fce5-650">**OCSP URLs**</span></span>|
|<span data-ttu-id="8fce5-651">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-651"></span></span>|
   
 <span data-ttu-id="8fce5-652">**Entrust autoridade de certificação - L1K**</span><span class="sxs-lookup"><span data-stu-id="8fce5-652">**Entrust Certification Authority - L1K**</span></span>
  
||
|:-----|
|<span data-ttu-id="8fce5-653">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-653">**Subject**</span></span>|
|<span data-ttu-id="8fce5-654">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-654"></span></span>|
|<span data-ttu-id="8fce5-655">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="8fce5-655">**Issuer**</span></span>|
|<span data-ttu-id="8fce5-656">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-656"></span></span>|
|<span data-ttu-id="8fce5-657">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="8fce5-657">**Serial Number**</span></span>|
|<span data-ttu-id="8fce5-658">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-658"></span></span>|
|<span data-ttu-id="8fce5-659">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="8fce5-659">**Public Key Length**</span></span>|
|<span data-ttu-id="8fce5-660">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-660"></span></span>|
|<span data-ttu-id="8fce5-661">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="8fce5-661">**Signature Algorithm**</span></span>|
|<span data-ttu-id="8fce5-662">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-662"></span></span>|
|<span data-ttu-id="8fce5-663">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-663">**Validity Not Before**</span></span>|
|<span data-ttu-id="8fce5-664">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-664"></span></span>|
|<span data-ttu-id="8fce5-665">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="8fce5-665">**Validity Not After**</span></span>|
|<span data-ttu-id="8fce5-666">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-666"></span></span>|
|<span data-ttu-id="8fce5-667">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-667">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-668">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-668"></span></span>|
|<span data-ttu-id="8fce5-669">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-669">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-670">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-670"></span></span>|
|<span data-ttu-id="8fce5-671">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-671">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="8fce5-672">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-672"></span></span>|
|<span data-ttu-id="8fce5-673">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-673">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-674">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-674"></span></span>|
|<span data-ttu-id="8fce5-675">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-675">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-676">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-676"></span></span>|
|<span data-ttu-id="8fce5-677">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="8fce5-677">**CRL URLs**</span></span>|
|<span data-ttu-id="8fce5-678">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-678"></span></span>|
|<span data-ttu-id="8fce5-679">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="8fce5-679">**OCSP URLs**</span></span>|
|<span data-ttu-id="8fce5-680">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-680"></span></span>|
   
 <span data-ttu-id="8fce5-681">**GlobalSign**</span><span class="sxs-lookup"><span data-stu-id="8fce5-681">**GlobalSign**</span></span>
  
||
|:-----|
|<span data-ttu-id="8fce5-682">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-682">**Subject**</span></span>|
|<span data-ttu-id="8fce5-683">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-683"></span></span>|
|<span data-ttu-id="8fce5-684">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="8fce5-684">**Issuer**</span></span>|
|<span data-ttu-id="8fce5-685">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-685"></span></span>|
|<span data-ttu-id="8fce5-686">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="8fce5-686">**Serial Number**</span></span>|
|<span data-ttu-id="8fce5-687">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-687"></span></span>|
|<span data-ttu-id="8fce5-688">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="8fce5-688">**Public Key Length**</span></span>|
|<span data-ttu-id="8fce5-689">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-689"></span></span>|
|<span data-ttu-id="8fce5-690">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="8fce5-690">**Signature Algorithm**</span></span>|
|<span data-ttu-id="8fce5-691">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-691"></span></span>|
|<span data-ttu-id="8fce5-692">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-692">**Validity Not Before**</span></span>|
|<span data-ttu-id="8fce5-693">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-693"></span></span>|
|<span data-ttu-id="8fce5-694">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="8fce5-694">**Validity Not After**</span></span>|
|<span data-ttu-id="8fce5-695">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-695"></span></span>|
|<span data-ttu-id="8fce5-696">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-696">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-697">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-697"></span></span>|
|<span data-ttu-id="8fce5-698">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-698">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-699">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-699"></span></span>|
|<span data-ttu-id="8fce5-700">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-700">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="8fce5-701">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-701"></span></span>|
|<span data-ttu-id="8fce5-702">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-702">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-703">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-703"></span></span>|
|<span data-ttu-id="8fce5-704">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-704">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-705">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-705"></span></span>|
|<span data-ttu-id="8fce5-706">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="8fce5-706">**CRL URLs**</span></span>|
|<span data-ttu-id="8fce5-707">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-707"></span></span>|
|<span data-ttu-id="8fce5-708">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="8fce5-708">**OCSP URLs**</span></span>|
|<span data-ttu-id="8fce5-709">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-709"></span></span>|
   
 <span data-ttu-id="8fce5-710">**GlobalSign estendido validação CA - SHA256 - G2**</span><span class="sxs-lookup"><span data-stu-id="8fce5-710">**GlobalSign Extended Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="8fce5-711">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-711">**Subject**</span></span>|
|<span data-ttu-id="8fce5-712">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-712"></span></span>|
|<span data-ttu-id="8fce5-713">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="8fce5-713">**Issuer**</span></span>|
|<span data-ttu-id="8fce5-714">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-714"></span></span>|
|<span data-ttu-id="8fce5-715">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="8fce5-715">**Serial Number**</span></span>|
|<span data-ttu-id="8fce5-716">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-716"></span></span>|
|<span data-ttu-id="8fce5-717">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="8fce5-717">**Public Key Length**</span></span>|
|<span data-ttu-id="8fce5-718">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-718"></span></span>|
|<span data-ttu-id="8fce5-719">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="8fce5-719">**Signature Algorithm**</span></span>|
|<span data-ttu-id="8fce5-720">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-720"></span></span>|
|<span data-ttu-id="8fce5-721">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-721">**Validity Not Before**</span></span>|
|<span data-ttu-id="8fce5-722">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-722"></span></span>|
|<span data-ttu-id="8fce5-723">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="8fce5-723">**Validity Not After**</span></span>|
|<span data-ttu-id="8fce5-724">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-724"></span></span>|
|<span data-ttu-id="8fce5-725">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-725">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-726">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-726"></span></span>|
|<span data-ttu-id="8fce5-727">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-727">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-728">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-728"></span></span>|
|<span data-ttu-id="8fce5-729">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-729">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="8fce5-730">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-730"></span></span>|
|<span data-ttu-id="8fce5-731">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-731">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-732">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-732"></span></span>|
|<span data-ttu-id="8fce5-733">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-733">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-734">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-734"></span></span>|
|<span data-ttu-id="8fce5-735">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="8fce5-735">**CRL URLs**</span></span>|
|<span data-ttu-id="8fce5-736">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-736"></span></span>|
|<span data-ttu-id="8fce5-737">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="8fce5-737">**OCSP URLs**</span></span>|
|<span data-ttu-id="8fce5-738">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-738"></span></span>|
   
 <span data-ttu-id="8fce5-739">**GlobalSign estendido validação CA - SHA256 - G3**</span><span class="sxs-lookup"><span data-stu-id="8fce5-739">**GlobalSign Extended Validation CA - SHA256 - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="8fce5-740">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-740">**Subject**</span></span>|
|<span data-ttu-id="8fce5-741">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-741"></span></span>|
|<span data-ttu-id="8fce5-742">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="8fce5-742">**Issuer**</span></span>|
|<span data-ttu-id="8fce5-743">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-743"></span></span>|
|<span data-ttu-id="8fce5-744">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="8fce5-744">**Serial Number**</span></span>|
|<span data-ttu-id="8fce5-745">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-745"></span></span>|
|<span data-ttu-id="8fce5-746">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="8fce5-746">**Public Key Length**</span></span>|
|<span data-ttu-id="8fce5-747">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-747"></span></span>|
|<span data-ttu-id="8fce5-748">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="8fce5-748">**Signature Algorithm**</span></span>|
|<span data-ttu-id="8fce5-749">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-749"></span></span>|
|<span data-ttu-id="8fce5-750">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-750">**Validity Not Before**</span></span>|
|<span data-ttu-id="8fce5-751">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-751"></span></span>|
|<span data-ttu-id="8fce5-752">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="8fce5-752">**Validity Not After**</span></span>|
|<span data-ttu-id="8fce5-753">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-753"></span></span>|
|<span data-ttu-id="8fce5-754">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-754">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-755">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-755"></span></span>|
|<span data-ttu-id="8fce5-756">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-756">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-757">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-757"></span></span>|
|<span data-ttu-id="8fce5-758">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-758">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="8fce5-759">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-759"></span></span>|
|<span data-ttu-id="8fce5-760">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-760">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-761">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-761"></span></span>|
|<span data-ttu-id="8fce5-762">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-762">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-763">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-763"></span></span>|
|<span data-ttu-id="8fce5-764">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="8fce5-764">**CRL URLs**</span></span>|
|<span data-ttu-id="8fce5-765">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-765"></span></span>|
|<span data-ttu-id="8fce5-766">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="8fce5-766">**OCSP URLs**</span></span>|
|<span data-ttu-id="8fce5-767">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-767"></span></span>|
   
 <span data-ttu-id="8fce5-768">**GlobalSign organização validação CA - SHA256 - G2**</span><span class="sxs-lookup"><span data-stu-id="8fce5-768">**GlobalSign Organization Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="8fce5-769">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-769">**Subject**</span></span>|
|<span data-ttu-id="8fce5-770">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-770"></span></span>|
|<span data-ttu-id="8fce5-771">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="8fce5-771">**Issuer**</span></span>|
|<span data-ttu-id="8fce5-772">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-772"></span></span>|
|<span data-ttu-id="8fce5-773">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="8fce5-773">**Serial Number**</span></span>|
|<span data-ttu-id="8fce5-774">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-774"></span></span>|
|<span data-ttu-id="8fce5-775">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="8fce5-775">**Public Key Length**</span></span>|
|<span data-ttu-id="8fce5-776">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-776"></span></span>|
|<span data-ttu-id="8fce5-777">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="8fce5-777">**Signature Algorithm**</span></span>|
|<span data-ttu-id="8fce5-778">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-778"></span></span>|
|<span data-ttu-id="8fce5-779">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-779">**Validity Not Before**</span></span>|
|<span data-ttu-id="8fce5-780">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-780"></span></span>|
|<span data-ttu-id="8fce5-781">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="8fce5-781">**Validity Not After**</span></span>|
|<span data-ttu-id="8fce5-782">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-782"></span></span>|
|<span data-ttu-id="8fce5-783">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-783">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-784">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-784"></span></span>|
|<span data-ttu-id="8fce5-785">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-785">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-786">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-786"></span></span>|
|<span data-ttu-id="8fce5-787">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-787">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="8fce5-788">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-788"></span></span>|
|<span data-ttu-id="8fce5-789">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-789">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-790">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-790"></span></span>|
|<span data-ttu-id="8fce5-791">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-791">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-792">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-792"></span></span>|
|<span data-ttu-id="8fce5-793">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="8fce5-793">**CRL URLs**</span></span>|
|<span data-ttu-id="8fce5-794">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-794"></span></span>|
|<span data-ttu-id="8fce5-795">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="8fce5-795">**OCSP URLs**</span></span>|
|<span data-ttu-id="8fce5-796">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-796"></span></span>|
   
 <span data-ttu-id="8fce5-797">**GlobalSign organização validação CA - SHA256 - G2**</span><span class="sxs-lookup"><span data-stu-id="8fce5-797">**GlobalSign Organization Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="8fce5-798">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-798">**Subject**</span></span>|
|<span data-ttu-id="8fce5-799">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-799"></span></span>|
|<span data-ttu-id="8fce5-800">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="8fce5-800">**Issuer**</span></span>|
|<span data-ttu-id="8fce5-801">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-801"></span></span>|
|<span data-ttu-id="8fce5-802">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="8fce5-802">**Serial Number**</span></span>|
|<span data-ttu-id="8fce5-803">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-803"></span></span>|
|<span data-ttu-id="8fce5-804">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="8fce5-804">**Public Key Length**</span></span>|
|<span data-ttu-id="8fce5-805">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-805"></span></span>|
|<span data-ttu-id="8fce5-806">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="8fce5-806">**Signature Algorithm**</span></span>|
|<span data-ttu-id="8fce5-807">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-807"></span></span>|
|<span data-ttu-id="8fce5-808">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-808">**Validity Not Before**</span></span>|
|<span data-ttu-id="8fce5-809">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-809"></span></span>|
|<span data-ttu-id="8fce5-810">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="8fce5-810">**Validity Not After**</span></span>|
|<span data-ttu-id="8fce5-811">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-811"></span></span>|
|<span data-ttu-id="8fce5-812">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-812">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-813">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-813"></span></span>|
|<span data-ttu-id="8fce5-814">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-814">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-815">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-815"></span></span>|
|<span data-ttu-id="8fce5-816">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-816">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="8fce5-817">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-817"></span></span>|
|<span data-ttu-id="8fce5-818">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-818">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-819">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-819"></span></span>|
|<span data-ttu-id="8fce5-820">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-820">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-821">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-821"></span></span>|
|<span data-ttu-id="8fce5-822">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="8fce5-822">**CRL URLs**</span></span>|
|<span data-ttu-id="8fce5-823">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-823"></span></span>|
|<span data-ttu-id="8fce5-824">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="8fce5-824">**OCSP URLs**</span></span>|
|<span data-ttu-id="8fce5-825">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-825"></span></span>|
   
 <span data-ttu-id="8fce5-826">**Criptografar vamos autoridade X3**</span><span class="sxs-lookup"><span data-stu-id="8fce5-826">**Let's Encrypt Authority X3**</span></span>
  
||
|:-----|
|<span data-ttu-id="8fce5-827">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-827">**Subject**</span></span>|
|<span data-ttu-id="8fce5-828">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-828"></span></span>|
|<span data-ttu-id="8fce5-829">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="8fce5-829">**Issuer**</span></span>|
|<span data-ttu-id="8fce5-830">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-830"></span></span>|
|<span data-ttu-id="8fce5-831">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="8fce5-831">**Serial Number**</span></span>|
|<span data-ttu-id="8fce5-832">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-832"></span></span>|
|<span data-ttu-id="8fce5-833">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="8fce5-833">**Public Key Length**</span></span>|
|<span data-ttu-id="8fce5-834">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-834"></span></span>|
|<span data-ttu-id="8fce5-835">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="8fce5-835">**Signature Algorithm**</span></span>|
|<span data-ttu-id="8fce5-836">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-836"></span></span>|
|<span data-ttu-id="8fce5-837">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-837">**Validity Not Before**</span></span>|
|<span data-ttu-id="8fce5-838">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-838"></span></span>|
|<span data-ttu-id="8fce5-839">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="8fce5-839">**Validity Not After**</span></span>|
|<span data-ttu-id="8fce5-840">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-840"></span></span>|
|<span data-ttu-id="8fce5-841">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-841">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-842">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-842"></span></span>|
|<span data-ttu-id="8fce5-843">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-843">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-844">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-844"></span></span>|
|<span data-ttu-id="8fce5-845">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-845">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="8fce5-846">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-846"></span></span>|
|<span data-ttu-id="8fce5-847">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-847">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-848">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-848"></span></span>|
|<span data-ttu-id="8fce5-849">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-849">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-850">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-850"></span></span>|
|<span data-ttu-id="8fce5-851">**URLs AIA**</span><span class="sxs-lookup"><span data-stu-id="8fce5-851">**AIA URLs**</span></span>|
|<span data-ttu-id="8fce5-852">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-852"></span></span>|
|<span data-ttu-id="8fce5-853">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="8fce5-853">**CRL URLs**</span></span>|
|<span data-ttu-id="8fce5-854">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-854"></span></span>|
|<span data-ttu-id="8fce5-855">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="8fce5-855">**OCSP URLs**</span></span>|
|<span data-ttu-id="8fce5-856">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-856"></span></span>|
   
 <span data-ttu-id="8fce5-857">**O TI da Microsoft SSL SHA2**</span><span class="sxs-lookup"><span data-stu-id="8fce5-857">**Microsoft IT SSL SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="8fce5-858">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-858">**Subject**</span></span>|
|<span data-ttu-id="8fce5-859">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-859"></span></span>|
|<span data-ttu-id="8fce5-860">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="8fce5-860">**Issuer**</span></span>|
|<span data-ttu-id="8fce5-861">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-861"></span></span>|
|<span data-ttu-id="8fce5-862">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="8fce5-862">**Serial Number**</span></span>|
|<span data-ttu-id="8fce5-863">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-863"></span></span>|
|<span data-ttu-id="8fce5-864">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="8fce5-864">**Public Key Length**</span></span>|
|<span data-ttu-id="8fce5-865">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-865"></span></span>|
|<span data-ttu-id="8fce5-866">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="8fce5-866">**Signature Algorithm**</span></span>|
|<span data-ttu-id="8fce5-867">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-867"></span></span>|
|<span data-ttu-id="8fce5-868">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-868">**Validity Not Before**</span></span>|
|<span data-ttu-id="8fce5-869">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-869"></span></span>|
|<span data-ttu-id="8fce5-870">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="8fce5-870">**Validity Not After**</span></span>|
|<span data-ttu-id="8fce5-871">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-871"></span></span>|
|<span data-ttu-id="8fce5-872">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-872">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-873">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-873"></span></span>|
|<span data-ttu-id="8fce5-874">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-874">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-875">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-875"></span></span>|
|<span data-ttu-id="8fce5-876">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-876">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="8fce5-877">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-877"></span></span>|
|<span data-ttu-id="8fce5-878">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-878">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-879">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-879"></span></span>|
|<span data-ttu-id="8fce5-880">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-880">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-881">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-881"></span></span>|
|<span data-ttu-id="8fce5-882">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="8fce5-882">**CRL URLs**</span></span>|
|<span data-ttu-id="8fce5-883">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-883"></span></span>|
   
 <span data-ttu-id="8fce5-884">**O TI da Microsoft SSL SHA2**</span><span class="sxs-lookup"><span data-stu-id="8fce5-884">**Microsoft IT SSL SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="8fce5-885">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-885">**Subject**</span></span>|
|<span data-ttu-id="8fce5-886">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-886"></span></span>|
|<span data-ttu-id="8fce5-887">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="8fce5-887">**Issuer**</span></span>|
|<span data-ttu-id="8fce5-888">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-888"></span></span>|
|<span data-ttu-id="8fce5-889">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="8fce5-889">**Serial Number**</span></span>|
|<span data-ttu-id="8fce5-890">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-890"></span></span>|
|<span data-ttu-id="8fce5-891">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="8fce5-891">**Public Key Length**</span></span>|
|<span data-ttu-id="8fce5-892">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-892"></span></span>|
|<span data-ttu-id="8fce5-893">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="8fce5-893">**Signature Algorithm**</span></span>|
|<span data-ttu-id="8fce5-894">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-894"></span></span>|
|<span data-ttu-id="8fce5-895">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-895">**Validity Not Before**</span></span>|
|<span data-ttu-id="8fce5-896">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-896"></span></span>|
|<span data-ttu-id="8fce5-897">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="8fce5-897">**Validity Not After**</span></span>|
|<span data-ttu-id="8fce5-898">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-898"></span></span>|
|<span data-ttu-id="8fce5-899">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-899">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-900">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-900"></span></span>|
|<span data-ttu-id="8fce5-901">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-901">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-902">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-902"></span></span>|
|<span data-ttu-id="8fce5-903">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-903">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="8fce5-904">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-904"></span></span>|
|<span data-ttu-id="8fce5-905">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-905">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-906">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-906"></span></span>|
|<span data-ttu-id="8fce5-907">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-907">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-908">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-908"></span></span>|
|<span data-ttu-id="8fce5-909">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="8fce5-909">**CRL URLs**</span></span>|
|<span data-ttu-id="8fce5-910">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-910"></span></span>|
|<span data-ttu-id="8fce5-911">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="8fce5-911">**OCSP URLs**</span></span>|
|<span data-ttu-id="8fce5-912">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-912"></span></span>|
   
 <span data-ttu-id="8fce5-913">**Autoridade de certificação do Microsoft IT TLS 1**</span><span class="sxs-lookup"><span data-stu-id="8fce5-913">**Microsoft IT TLS CA 1**</span></span>
  
||
|:-----|
|<span data-ttu-id="8fce5-914">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-914">**Subject**</span></span>|
|<span data-ttu-id="8fce5-915">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-915"></span></span>|
|<span data-ttu-id="8fce5-916">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="8fce5-916">**Issuer**</span></span>|
|<span data-ttu-id="8fce5-917">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-917"></span></span>|
|<span data-ttu-id="8fce5-918">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="8fce5-918">**Serial Number**</span></span>|
|<span data-ttu-id="8fce5-919">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-919"></span></span>|
|<span data-ttu-id="8fce5-920">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="8fce5-920">**Public Key Length**</span></span>|
|<span data-ttu-id="8fce5-921">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-921"></span></span>|
|<span data-ttu-id="8fce5-922">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="8fce5-922">**Signature Algorithm**</span></span>|
|<span data-ttu-id="8fce5-923">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-923"></span></span>|
|<span data-ttu-id="8fce5-924">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-924">**Validity Not Before**</span></span>|
|<span data-ttu-id="8fce5-925">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-925"></span></span>|
|<span data-ttu-id="8fce5-926">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="8fce5-926">**Validity Not After**</span></span>|
|<span data-ttu-id="8fce5-927">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-927"></span></span>|
|<span data-ttu-id="8fce5-928">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-928">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-929">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-929"></span></span>|
|<span data-ttu-id="8fce5-930">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-930">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-931">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-931"></span></span>|
|<span data-ttu-id="8fce5-932">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-932">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="8fce5-933">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-933"></span></span>|
|<span data-ttu-id="8fce5-934">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-934">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-935">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-935"></span></span>|
|<span data-ttu-id="8fce5-936">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-936">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-937">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-937"></span></span>|
|<span data-ttu-id="8fce5-938">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="8fce5-938">**CRL URLs**</span></span>|
|<span data-ttu-id="8fce5-939">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-939"></span></span>|
|<span data-ttu-id="8fce5-940">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="8fce5-940">**OCSP URLs**</span></span>|
|<span data-ttu-id="8fce5-941">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-941"></span></span>|
   
 <span data-ttu-id="8fce5-942">**Autoridade de certificação do Microsoft IT TLS 2**</span><span class="sxs-lookup"><span data-stu-id="8fce5-942">**Microsoft IT TLS CA 2**</span></span>
  
||
|:-----|
|<span data-ttu-id="8fce5-943">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-943">**Subject**</span></span>|
|<span data-ttu-id="8fce5-944">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-944"></span></span>|
|<span data-ttu-id="8fce5-945">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="8fce5-945">**Issuer**</span></span>|
|<span data-ttu-id="8fce5-946">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-946"></span></span>|
|<span data-ttu-id="8fce5-947">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="8fce5-947">**Serial Number**</span></span>|
|<span data-ttu-id="8fce5-948">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-948"></span></span>|
|<span data-ttu-id="8fce5-949">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="8fce5-949">**Public Key Length**</span></span>|
|<span data-ttu-id="8fce5-950">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-950"></span></span>|
|<span data-ttu-id="8fce5-951">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="8fce5-951">**Signature Algorithm**</span></span>|
|<span data-ttu-id="8fce5-952">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-952"></span></span>|
|<span data-ttu-id="8fce5-953">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-953">**Validity Not Before**</span></span>|
|<span data-ttu-id="8fce5-954">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-954"></span></span>|
|<span data-ttu-id="8fce5-955">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="8fce5-955">**Validity Not After**</span></span>|
|<span data-ttu-id="8fce5-956">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-956"></span></span>|
|<span data-ttu-id="8fce5-957">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-957">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-958">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-958"></span></span>|
|<span data-ttu-id="8fce5-959">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-959">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-960">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-960"></span></span>|
|<span data-ttu-id="8fce5-961">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-961">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="8fce5-962">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-962"></span></span>|
|<span data-ttu-id="8fce5-963">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-963">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-964">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-964"></span></span>|
|<span data-ttu-id="8fce5-965">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-965">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-966">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-966"></span></span>|
|<span data-ttu-id="8fce5-967">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="8fce5-967">**CRL URLs**</span></span>|
|<span data-ttu-id="8fce5-968">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-968"></span></span>|
|<span data-ttu-id="8fce5-969">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="8fce5-969">**OCSP URLs**</span></span>|
|<span data-ttu-id="8fce5-970">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-970"></span></span>|
   
 <span data-ttu-id="8fce5-971">**Autoridade de certificação do Microsoft IT TLS 4**</span><span class="sxs-lookup"><span data-stu-id="8fce5-971">**Microsoft IT TLS CA 4**</span></span>
  
||
|:-----|
|<span data-ttu-id="8fce5-972">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-972">**Subject**</span></span>|
|<span data-ttu-id="8fce5-973">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-973"></span></span>|
|<span data-ttu-id="8fce5-974">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="8fce5-974">**Issuer**</span></span>|
|<span data-ttu-id="8fce5-975">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-975"></span></span>|
|<span data-ttu-id="8fce5-976">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="8fce5-976">**Serial Number**</span></span>|
|<span data-ttu-id="8fce5-977">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-977"></span></span>|
|<span data-ttu-id="8fce5-978">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="8fce5-978">**Public Key Length**</span></span>|
|<span data-ttu-id="8fce5-979">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-979"></span></span>|
|<span data-ttu-id="8fce5-980">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="8fce5-980">**Signature Algorithm**</span></span>|
|<span data-ttu-id="8fce5-981">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-981"></span></span>|
|<span data-ttu-id="8fce5-982">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-982">**Validity Not Before**</span></span>|
|<span data-ttu-id="8fce5-983">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-983"></span></span>|
|<span data-ttu-id="8fce5-984">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="8fce5-984">**Validity Not After**</span></span>|
|<span data-ttu-id="8fce5-985">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-985"></span></span>|
|<span data-ttu-id="8fce5-986">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-986">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-987">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-987"></span></span>|
|<span data-ttu-id="8fce5-988">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-988">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-989">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-989"></span></span>|
|<span data-ttu-id="8fce5-990">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-990">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="8fce5-991">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-991"></span></span>|
|<span data-ttu-id="8fce5-992">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-992">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-993">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-993"></span></span>|
|<span data-ttu-id="8fce5-994">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-994">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-995">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-995"></span></span>|
|<span data-ttu-id="8fce5-996">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="8fce5-996">**CRL URLs**</span></span>|
|<span data-ttu-id="8fce5-997">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-997"></span></span>|
|<span data-ttu-id="8fce5-998">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="8fce5-998">**OCSP URLs**</span></span>|
|<span data-ttu-id="8fce5-999">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-999"></span></span>|
   
 <span data-ttu-id="8fce5-1000">**Autoridade de certificação do Microsoft IT TLS 5**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1000">**Microsoft IT TLS CA 5**</span></span>
  
||
|:-----|
|<span data-ttu-id="8fce5-1001">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1001">**Subject**</span></span>|
|<span data-ttu-id="8fce5-1002">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1002"></span></span>|
|<span data-ttu-id="8fce5-1003">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1003">**Issuer**</span></span>|
|<span data-ttu-id="8fce5-1004">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1004"></span></span>|
|<span data-ttu-id="8fce5-1005">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1005">**Serial Number**</span></span>|
|<span data-ttu-id="8fce5-1006">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1006"></span></span>|
|<span data-ttu-id="8fce5-1007">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1007">**Public Key Length**</span></span>|
|<span data-ttu-id="8fce5-1008">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1008"></span></span>|
|<span data-ttu-id="8fce5-1009">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1009">**Signature Algorithm**</span></span>|
|<span data-ttu-id="8fce5-1010">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1010"></span></span>|
|<span data-ttu-id="8fce5-1011">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1011">**Validity Not Before**</span></span>|
|<span data-ttu-id="8fce5-1012">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1012"></span></span>|
|<span data-ttu-id="8fce5-1013">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1013">**Validity Not After**</span></span>|
|<span data-ttu-id="8fce5-1014">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1014"></span></span>|
|<span data-ttu-id="8fce5-1015">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1015">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-1016">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1016"></span></span>|
|<span data-ttu-id="8fce5-1017">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1017">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-1018">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1018"></span></span>|
|<span data-ttu-id="8fce5-1019">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1019">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="8fce5-1020">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1020"></span></span>|
|<span data-ttu-id="8fce5-1021">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1021">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-1022">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1022"></span></span>|
|<span data-ttu-id="8fce5-1023">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1023">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-1024">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1024"></span></span>|
|<span data-ttu-id="8fce5-1025">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1025">**CRL URLs**</span></span>|
|<span data-ttu-id="8fce5-1026">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1026"></span></span>|
|<span data-ttu-id="8fce5-1027">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1027">**OCSP URLs**</span></span>|
|<span data-ttu-id="8fce5-1028">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1028"></span></span>|
   
 <span data-ttu-id="8fce5-1029">**CA de SSL Symantec classe EV 3 - G3**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1029">**Symantec Class 3 EV SSL CA - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="8fce5-1030">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1030">**Subject**</span></span>|
|<span data-ttu-id="8fce5-1031">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1031"></span></span>|
|<span data-ttu-id="8fce5-1032">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1032">**Issuer**</span></span>|
|<span data-ttu-id="8fce5-1033">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1033"></span></span>|
|<span data-ttu-id="8fce5-1034">**Nome alternativo da entidade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1034">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="8fce5-1035">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1035"></span></span>|
|<span data-ttu-id="8fce5-1036">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1036">**Serial Number**</span></span>|
|<span data-ttu-id="8fce5-1037">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1037"></span></span>|
|<span data-ttu-id="8fce5-1038">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1038">**Public Key Length**</span></span>|
|<span data-ttu-id="8fce5-1039">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1039"></span></span>|
|<span data-ttu-id="8fce5-1040">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1040">**Signature Algorithm**</span></span>|
|<span data-ttu-id="8fce5-1041">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1041"></span></span>|
|<span data-ttu-id="8fce5-1042">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1042">**Validity Not Before**</span></span>|
|<span data-ttu-id="8fce5-1043">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1043"></span></span>|
|<span data-ttu-id="8fce5-1044">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1044">**Validity Not After**</span></span>|
|<span data-ttu-id="8fce5-1045">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1045"></span></span>|
|<span data-ttu-id="8fce5-1046">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1046">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-1047">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1047"></span></span>|
|<span data-ttu-id="8fce5-1048">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1048">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-1049">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1049"></span></span>|
|<span data-ttu-id="8fce5-1050">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1050">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="8fce5-1051">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1051"></span></span>|
|<span data-ttu-id="8fce5-1052">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1052">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-1053">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1053"></span></span>|
|<span data-ttu-id="8fce5-1054">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1054">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-1055">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1055"></span></span>|
|<span data-ttu-id="8fce5-1056">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1056">**CRL URLs**</span></span>|
|<span data-ttu-id="8fce5-1057">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1057"></span></span>|
|<span data-ttu-id="8fce5-1058">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1058">**OCSP URLs**</span></span>|
|<span data-ttu-id="8fce5-1059">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1059"></span></span>|
   
 <span data-ttu-id="8fce5-1060">**Symantec classe 3 servidores seguros CA - G4**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1060">**Symantec Class 3 Secure Server CA - G4**</span></span>
  
||
|:-----|
|<span data-ttu-id="8fce5-1061">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1061">**Subject**</span></span>|
|<span data-ttu-id="8fce5-1062">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1062"></span></span>|
|<span data-ttu-id="8fce5-1063">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1063">**Issuer**</span></span>|
|<span data-ttu-id="8fce5-1064">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1064"></span></span>|
|<span data-ttu-id="8fce5-1065">**Nome alternativo da entidade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1065">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="8fce5-1066">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1066"></span></span>|
|<span data-ttu-id="8fce5-1067">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1067">**Serial Number**</span></span>|
|<span data-ttu-id="8fce5-1068">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1068"></span></span>|
|<span data-ttu-id="8fce5-1069">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1069">**Public Key Length**</span></span>|
|<span data-ttu-id="8fce5-1070">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1070"></span></span>|
|<span data-ttu-id="8fce5-1071">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1071">**Signature Algorithm**</span></span>|
|<span data-ttu-id="8fce5-1072">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1072"></span></span>|
|<span data-ttu-id="8fce5-1073">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1073">**Validity Not Before**</span></span>|
|<span data-ttu-id="8fce5-1074">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1074"></span></span>|
|<span data-ttu-id="8fce5-1075">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1075">**Validity Not After**</span></span>|
|<span data-ttu-id="8fce5-1076">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1076"></span></span>|
|<span data-ttu-id="8fce5-1077">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1077">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-1078">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1078"></span></span>|
|<span data-ttu-id="8fce5-1079">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1079">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-1080">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1080"></span></span>|
|<span data-ttu-id="8fce5-1081">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1081">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="8fce5-1082">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1082"></span></span>|
|<span data-ttu-id="8fce5-1083">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1083">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-1084">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1084"></span></span>|
|<span data-ttu-id="8fce5-1085">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1085">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-1086">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1086"></span></span>|
|<span data-ttu-id="8fce5-1087">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1087">**CRL URLs**</span></span>|
|<span data-ttu-id="8fce5-1088">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1088"></span></span>|
|<span data-ttu-id="8fce5-1089">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1089">**OCSP URLs**</span></span>|
|<span data-ttu-id="8fce5-1090">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1090"></span></span>|
   
 <span data-ttu-id="8fce5-1091">**Thawte SHA256 SSL da autoridade de certificação**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1091">**thawte SHA256 SSL CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="8fce5-1092">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1092">**Subject**</span></span>|
|<span data-ttu-id="8fce5-1093">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1093"></span></span>|
|<span data-ttu-id="8fce5-1094">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1094">**Issuer**</span></span>|
|<span data-ttu-id="8fce5-1095">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1095"></span></span>|
|<span data-ttu-id="8fce5-1096">**Nome alternativo da entidade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1096">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="8fce5-1097">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1097"></span></span>|
|<span data-ttu-id="8fce5-1098">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1098">**Serial Number**</span></span>|
|<span data-ttu-id="8fce5-1099">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1099"></span></span>|
|<span data-ttu-id="8fce5-1100">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1100">**Public Key Length**</span></span>|
|<span data-ttu-id="8fce5-1101">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1101"></span></span>|
|<span data-ttu-id="8fce5-1102">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1102">**Signature Algorithm**</span></span>|
|<span data-ttu-id="8fce5-1103">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1103"></span></span>|
|<span data-ttu-id="8fce5-1104">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1104">**Validity Not Before**</span></span>|
|<span data-ttu-id="8fce5-1105">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1105"></span></span>|
|<span data-ttu-id="8fce5-1106">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1106">**Validity Not After**</span></span>|
|<span data-ttu-id="8fce5-1107">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1107"></span></span>|
|<span data-ttu-id="8fce5-1108">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1108">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-1109">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1109"></span></span>|
|<span data-ttu-id="8fce5-1110">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1110">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-1111">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1111"></span></span>|
|<span data-ttu-id="8fce5-1112">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1112">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="8fce5-1113">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1113"></span></span>|
|<span data-ttu-id="8fce5-1114">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1114">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-1115">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1115"></span></span>|
|<span data-ttu-id="8fce5-1116">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1116">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-1117">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1117"></span></span>|
|<span data-ttu-id="8fce5-1118">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1118">**CRL URLs**</span></span>|
|<span data-ttu-id="8fce5-1119">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1119"></span></span>|
|<span data-ttu-id="8fce5-1120">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1120">**OCSP URLs**</span></span>|
|<span data-ttu-id="8fce5-1121">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1121"></span></span>|
   
 <span data-ttu-id="8fce5-1122">**Verizon Akamai SureServer CA G14-SHA2**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1122">**Verizon Akamai SureServer CA G14-SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="8fce5-1123">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1123">**Subject**</span></span>|
|<span data-ttu-id="8fce5-1124">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1124"></span></span>|
|<span data-ttu-id="8fce5-1125">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1125">**Issuer**</span></span>|
|<span data-ttu-id="8fce5-1126">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1126"></span></span>|
|<span data-ttu-id="8fce5-1127">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1127">**Serial Number**</span></span>|
|<span data-ttu-id="8fce5-1128">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1128"></span></span>|
|<span data-ttu-id="8fce5-1129">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1129">**Public Key Length**</span></span>|
|<span data-ttu-id="8fce5-1130">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1130"></span></span>|
|<span data-ttu-id="8fce5-1131">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1131">**Signature Algorithm**</span></span>|
|<span data-ttu-id="8fce5-1132">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1132"></span></span>|
|<span data-ttu-id="8fce5-1133">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1133">**Validity Not Before**</span></span>|
|<span data-ttu-id="8fce5-1134">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1134"></span></span>|
|<span data-ttu-id="8fce5-1135">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1135">**Validity Not After**</span></span>|
|<span data-ttu-id="8fce5-1136">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1136"></span></span>|
|<span data-ttu-id="8fce5-1137">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1137">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-1138">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1138"></span></span>|
|<span data-ttu-id="8fce5-1139">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1139">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="8fce5-1140">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1140"></span></span>|
|<span data-ttu-id="8fce5-1141">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1141">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="8fce5-1142">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1142"></span></span>|
|<span data-ttu-id="8fce5-1143">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1143">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-1144">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1144"></span></span>|
|<span data-ttu-id="8fce5-1145">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1145">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="8fce5-1146">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1146"></span></span>|
|<span data-ttu-id="8fce5-1147">**URLs AIA**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1147">**AIA URLs**</span></span>|
|<span data-ttu-id="8fce5-1148">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1148"></span></span>|
|<span data-ttu-id="8fce5-1149">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1149">**CRL URLs**</span></span>|
|<span data-ttu-id="8fce5-1150">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1150"></span></span>|
|<span data-ttu-id="8fce5-1151">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="8fce5-1151">**OCSP URLs**</span></span>|
|<span data-ttu-id="8fce5-1152">:-----</span><span class="sxs-lookup"><span data-stu-id="8fce5-1152"></span></span>|
   
## <a name="additional-certificate-paths"></a><span data-ttu-id="8fce5-1153">Caminhos de certificado adicional</span><span class="sxs-lookup"><span data-stu-id="8fce5-1153">Additional certificate paths</span></span>
<span data-ttu-id="8fce5-1154"><a name="IntermediateCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="8fce5-1154"></span></span>

<span data-ttu-id="8fce5-1155">A seguir incluem certificados herdados que não estão incluídos acima e serão mesclados com a lista acima ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="8fce5-1155">The following include legacy certificates that aren't included above and will be merged with the list above over time.</span></span>
  
```
evsecure-aia.verisign.com
sa.symcb.com
sd.symcb.com
*.omniroot.com
*.verisign.com
*.symcb.com
*.symcd.com
*.verisign.net
*.geotrust.com
*.entrust.net
*.public-trust.com
EVIntl-ocsp.verisign.com
EVSecure-ocsp.verisign.com
isrg.trustid.ocsp.identrust.com
ocsp.digicert.com
ocsp.entrust.net
ocsp.globalsign.com/ExtendedSSLSHA256CACross
ocsp.globalsign.com/rootr1
ocsp.globalsign.com/rootr2
ocsp2.globalsign.com/rootr3
ocsp.int-x3.letsencrypt.org/
ocsp.msocsp.com
ocsp.omniroot.com/baltimoreroot
ocsp2.globalsign.com/gsextendvalsha2g3r3
ocsp2.globalsign.com/gsorganizationvalsha2g2
ocsp2.globalsign.com/gsorganizationvalsha2g3
ocsp2.globalsign.com/rootr3
ocspx.digicert.com
s2.symcb.com
sr.symcd.com
su.symcd.com
vassg142.ocsp.omniroot.com
cdp1.public-trust.com/CRL/Omniroot2025.crl
crl.entrust.net/2048ca.crl
crl.entrust.net/g2ca.crl
crl.entrust.net/level1k.crl
crl.entrust.net/rootca1.crl
crl.globalsign.com/gs/gsextendvalsha2g3r3.crl
crl.globalsign.com/gs/gsorganizationvalsha2g2.crl
crl.globalsign.com/gsorganizationvalsha2g3.crl
crl.globalsign.com/root.crl
crl.globalsign.net/root-r2.crl
crl.globalsign.com/root-r3.crl
crl.globalsign.net/root.crl
crl.identrust.com/DSTROOTCAX3CRL.crl
crl.microsoft.com/pki/mscorp/crl/msitwww1.crl
crl.microsoft.com/pki/mscorp/crl/msitwww2.crl
crl3.digicert.com/DigiCertCloudServicesCA-1-g1.crl
crl3.digicert.com/DigiCertGlobalRootCA.crl
crl3.digicert.com/sha2-ev-server-g1.crl
crl3.digicert.com/sha2-ha-server-g5.crl
crl3.digicert.com/ssca-sha2-g5.crl
crl4.digicert.com/DigiCertCloudServicesCA-1-g1.crl
crl4.digicert.com/DigiCertGlobalRootCA.crl
crl4.digicert.com/DigiCertHighAssuranceEVRootCA.crl
crl4.digicert.com/sha2-ev-server-g1.crl
crl4.digicert.com/sha2-ha-server-g5.crl
crl4.digicert.com/ssca-sha2-g5.crl
EVIntl-crl.verisign.com/EVIntl2006.crl
EVSecure-crl.verisign.com/pca3-g5.crl
mscrl.microsoft.com/pki/mscorp/crl/msitwww1.crl
mscrl.microsoft.com/pki/mscorp/crl/msitwww2.crl
s1.symcb.com/pca3-g5.crl
sr.symcb.com/sr.crl
su.symcb.com/su.crl
vassg142.crl.omniroot.com/vassg142.crl
aia.entrust.net/l1k-chain256.cer
apps.identrust.com/roots/dstrootcax3.p7c
https://cacert.a.omniroot.com/vassg142.crt
https://cacert.a.omniroot.com/vassg142.der
https://cacert.omniroot.com/baltimoreroot.crt
https://cacert.omniroot.com/baltimoreroot.der
cacerts.digicert.com/DigiCertCloudServicesCA-1.crt
cacerts.digicert.com/DigiCertSHA2ExtendedValidationServerCA.crt
cacerts.digicert.com/DigiCertSHA2HighAssuranceServerCA.crt
cacerts.digicert.com/DigiCertSHA2SecureServerCA.crt
cert.int-x3.letsencrypt.org/
EVIntl-aia.verisign.com/EVIntl2006.cer
secure.globalsign.com/cacert/gsextendvalsha2g2r2.crt
secure.globalsign.com/cacert/gsextendvalsha2g3r3.crt
secure.globalsign.com/cacert/gsorganizationvalsha2g2r1.crt
secure.globalsign.com/cacert/gsorganizationvalsha2g3.crt
sr.symcb.com/sr.crt
su.symcb.com/su.crt
https://www.digicert.com/CACerts/DigiCertGlobalRootCA.crt
https://www.digicert.com/CACerts/DigiCertHighAssuranceEVRootCA.crt
www.microsoft.com/pki/mscorp/msitwww1.crt
www.microsoft.com/pki/mscorp/msitwww2.crt

```



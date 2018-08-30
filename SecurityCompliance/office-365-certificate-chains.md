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
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523938"
---
# <a name="office-365-certificate-chains"></a><span data-ttu-id="13fa7-106">Cadeias de certificados do Office 365</span><span class="sxs-lookup"><span data-stu-id="13fa7-106">Office 365 Certificate Chains</span></span>

<span data-ttu-id="13fa7-p102">O Office 365 utiliza um número de provedores de certificado diferente. O exemplo a seguir descreve a lista completa de certificados de raiz Office 365 conhecidos que os clientes podem encontrar ao acessar o Office 365. Para obter informações sobre os certificados que você talvez precise instalar em sua própria infra-estrutura, consulte [Planejar certificados SSL de terceiros para o Office 365](https://support.office.com/article/b48cdf63-07e0-4cda-8c12-4871590f59ce). As seguintes informações de certificado se aplica a todas as instâncias de nuvem em todo o mundo e Nacional do Office 365.</span><span class="sxs-lookup"><span data-stu-id="13fa7-p102">Office 365 leverages a number of different certificate providers. The following describes the complete list of known Office 365 root certificates that customers may encounter when accessing Office 365. For information on the certificates you may need to install in your own infrastructure, see [Plan for third-party SSL certificates for Office 365](https://support.office.com/article/b48cdf63-07e0-4cda-8c12-4871590f59ce). The following certificate information applies to all worldwide and national cloud instances of Office 365.</span></span>
  

|<span data-ttu-id="13fa7-111">**Tipo de certificado**</span><span class="sxs-lookup"><span data-stu-id="13fa7-111">**Certificate type**</span></span>|<span data-ttu-id="13fa7-112">**P7b download**</span><span class="sxs-lookup"><span data-stu-id="13fa7-112">**P7b download**</span></span>|<span data-ttu-id="13fa7-113">**Pontos de extremidade da lista de certificados Revogados**</span><span class="sxs-lookup"><span data-stu-id="13fa7-113">**CRL Endpoints**</span></span>|<span data-ttu-id="13fa7-114">**Pontos de extremidade OCSP**</span><span class="sxs-lookup"><span data-stu-id="13fa7-114">**OCSP Endpoints**</span></span>|<span data-ttu-id="13fa7-115">**Pontos de extremidade AIA**</span><span class="sxs-lookup"><span data-stu-id="13fa7-115">**AIA Endpoints**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="13fa7-116">Certificados raiz de publicamente confiáveis</span><span class="sxs-lookup"><span data-stu-id="13fa7-116">Publicly Trusted Root Certificates</span></span>](https://support.office.com/article/0c03e6b3-e73f-4316-9e2b-bf4091ae96bb#rootcerts) <br/> |[<span data-ttu-id="13fa7-117">Pacote de certificado raiz do Office 365 (P7B)</span><span class="sxs-lookup"><span data-stu-id="13fa7-117">Office 365 Root Certificate Bundle (P7B)</span></span>](http://download.microsoft.com/download/A/5/A/A5AE01F3-D19B-4A11-9407-801263CEF72C/O365_Root_Certs_20170321.p7b) <br/> |<span data-ttu-id="13fa7-118">CRL.GlobalSign.NET</span><span class="sxs-lookup"><span data-stu-id="13fa7-118">crl.globalsign.net</span></span>  <br/> <span data-ttu-id="13fa7-119">www.d-Trust.NET</span><span class="sxs-lookup"><span data-stu-id="13fa7-119">www.d-trust.net</span></span>  <br/> |<span data-ttu-id="13fa7-120">N/D</span><span class="sxs-lookup"><span data-stu-id="13fa7-120">N/A</span></span>  <br/> |<span data-ttu-id="13fa7-121">N/D</span><span class="sxs-lookup"><span data-stu-id="13fa7-121">N/A</span></span>  <br/> |
|[<span data-ttu-id="13fa7-122">Publicamente confiáveis certificados intermediários</span><span class="sxs-lookup"><span data-stu-id="13fa7-122">Publicly Trusted Intermediate Certificates</span></span>](https://support.office.com/article/0c03e6b3-e73f-4316-9e2b-bf4091ae96bb#IntermediateCerts) <br/> |[<span data-ttu-id="13fa7-123">Pacote do Office 365 intermediário de certificado (P7B)</span><span class="sxs-lookup"><span data-stu-id="13fa7-123">Office 365 Intermediate Certificate Bundle (P7B)</span></span>](http://download.microsoft.com/download/4/D/5/4D5339A4-0A4A-46AB-AE52-B179DEDA4BEC/O365_Intermediate_Certs_20170321.p7b)  <br/> |<span data-ttu-id="13fa7-124">cdp1.Public-trust.com</span><span class="sxs-lookup"><span data-stu-id="13fa7-124">cdp1.public-trust.com</span></span>  <br/> <span data-ttu-id="13fa7-125">CRL.cnnic.CN</span><span class="sxs-lookup"><span data-stu-id="13fa7-125">crl.cnnic.cn</span></span>  <br/> <span data-ttu-id="13fa7-126">CRL.Entrust.NET</span><span class="sxs-lookup"><span data-stu-id="13fa7-126">crl.entrust.net</span></span>  <br/> <span data-ttu-id="13fa7-127">CRL.GlobalSign.com</span><span class="sxs-lookup"><span data-stu-id="13fa7-127">crl.globalsign.com</span></span>  <br/> <span data-ttu-id="13fa7-128">CRL.GlobalSign.NET</span><span class="sxs-lookup"><span data-stu-id="13fa7-128">crl.globalsign.net</span></span>  <br/> <span data-ttu-id="13fa7-129">CRL.identrust.com</span><span class="sxs-lookup"><span data-stu-id="13fa7-129">crl.identrust.com</span></span>  <br/> <span data-ttu-id="13fa7-130">CRL.Thawte.com</span><span class="sxs-lookup"><span data-stu-id="13fa7-130">crl.thawte.com</span></span>  <br/> <span data-ttu-id="13fa7-131">crl3.digicert.com</span><span class="sxs-lookup"><span data-stu-id="13fa7-131">crl3.digicert.com</span></span>  <br/> <span data-ttu-id="13fa7-132">crl4.digicert.com</span><span class="sxs-lookup"><span data-stu-id="13fa7-132">crl4.digicert.com</span></span>  <br/> <span data-ttu-id="13fa7-133">S1.symcb.com</span><span class="sxs-lookup"><span data-stu-id="13fa7-133">s1.symcb.com</span></span>  <br/> <span data-ttu-id="13fa7-134">www.d-Trust.NET</span><span class="sxs-lookup"><span data-stu-id="13fa7-134">www.d-trust.net</span></span>  <br/> |<span data-ttu-id="13fa7-135">isrg.trustid.OCSP.identrust.com</span><span class="sxs-lookup"><span data-stu-id="13fa7-135">isrg.trustid.ocsp.identrust.com</span></span>  <br/> <span data-ttu-id="13fa7-136">OCSP.digicert.com</span><span class="sxs-lookup"><span data-stu-id="13fa7-136">ocsp.digicert.com</span></span>  <br/> <span data-ttu-id="13fa7-137">OCSP.Entrust.NET</span><span class="sxs-lookup"><span data-stu-id="13fa7-137">ocsp.entrust.net</span></span>  <br/> <span data-ttu-id="13fa7-138">OCSP.GlobalSign.com</span><span class="sxs-lookup"><span data-stu-id="13fa7-138">ocsp.globalsign.com</span></span>  <br/> <span data-ttu-id="13fa7-139">OCSP.omniroot.com</span><span class="sxs-lookup"><span data-stu-id="13fa7-139">ocsp.omniroot.com</span></span>  <br/> <span data-ttu-id="13fa7-140">OCSP.startssl.com</span><span class="sxs-lookup"><span data-stu-id="13fa7-140">ocsp.startssl.com</span></span>  <br/> <span data-ttu-id="13fa7-141">OCSP.Thawte.com</span><span class="sxs-lookup"><span data-stu-id="13fa7-141">ocsp.thawte.com</span></span>  <br/> <span data-ttu-id="13fa7-142">ocsp2.GlobalSign.com</span><span class="sxs-lookup"><span data-stu-id="13fa7-142">ocsp2.globalsign.com</span></span>  <br/> <span data-ttu-id="13fa7-143">ocspcnnicroot.cnnic.CN</span><span class="sxs-lookup"><span data-stu-id="13fa7-143">ocspcnnicroot.cnnic.cn</span></span>  <br/> <span data-ttu-id="13fa7-144">raiz-c3-ca2-2009.ocsp.d-trust.net</span><span class="sxs-lookup"><span data-stu-id="13fa7-144">root-c3-ca2-2009.ocsp.d-trust.net</span></span>  <br/> <span data-ttu-id="13fa7-145">root-C3-ca2-EV-2009.OCSP.d-Trust.NET</span><span class="sxs-lookup"><span data-stu-id="13fa7-145">root-c3-ca2-ev-2009.ocsp.d-trust.net</span></span>  <br/> <span data-ttu-id="13fa7-146">S2.symcb.com</span><span class="sxs-lookup"><span data-stu-id="13fa7-146">s2.symcb.com</span></span>  <br/> |<span data-ttu-id="13fa7-147">AIA.startssl.com</span><span class="sxs-lookup"><span data-stu-id="13fa7-147">aia.startssl.com</span></span>  <br/> <span data-ttu-id="13fa7-148">Apps.identrust.com</span><span class="sxs-lookup"><span data-stu-id="13fa7-148">apps.identrust.com</span></span>  <br/> <span data-ttu-id="13fa7-149">cacert.omniroot.com</span><span class="sxs-lookup"><span data-stu-id="13fa7-149">cacert.omniroot.com</span></span>  <br/> <span data-ttu-id="13fa7-150">www.cnnic.CN</span><span class="sxs-lookup"><span data-stu-id="13fa7-150">www.cnnic.cn</span></span>  <br/> |
   
<span data-ttu-id="13fa7-151">Expanda a raiz e intermediárias seções abaixo para ver detalhes adicionais sobre os provedores de certificado.</span><span class="sxs-lookup"><span data-stu-id="13fa7-151">Expand the root and intermediate sections below to see additional details about the certificate providers.</span></span>
  
## <a name="office-365-root-certificate-details"></a><span data-ttu-id="13fa7-152">O Office 365 detalhes do certificado raiz</span><span class="sxs-lookup"><span data-stu-id="13fa7-152">Office 365 Root Certificate Details</span></span>
<span data-ttu-id="13fa7-153"><a name="RootCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="13fa7-153"></span></span>

 <span data-ttu-id="13fa7-154">**Baltimore CyberTrust Root**</span><span class="sxs-lookup"><span data-stu-id="13fa7-154">**Baltimore CyberTrust Root**</span></span>
  
<span data-ttu-id="13fa7-155">|:-----|</span><span class="sxs-lookup"><span data-stu-id="13fa7-155">|:-----|</span></span>
|<span data-ttu-id="13fa7-156">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-156">**Subject**</span></span>|
|:-----|
|<span data-ttu-id="13fa7-157">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="13fa7-157">**Serial Number**</span></span>|
|<span data-ttu-id="13fa7-158">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-158"></span></span>|
|<span data-ttu-id="13fa7-159">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="13fa7-159">**Public Key Length**</span></span>|
|<span data-ttu-id="13fa7-160">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-160"></span></span>|
|<span data-ttu-id="13fa7-161">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="13fa7-161">**Signature Algorithm**</span></span>|
|<span data-ttu-id="13fa7-162">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-162"></span></span>|
|<span data-ttu-id="13fa7-163">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-163">**Validity Not Before**</span></span>|
|<span data-ttu-id="13fa7-164">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-164"></span></span>|
|<span data-ttu-id="13fa7-165">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="13fa7-165">**Validity Not After**</span></span>|
|<span data-ttu-id="13fa7-166">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-166"></span></span>|
|<span data-ttu-id="13fa7-167">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-167">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-168">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-168"></span></span>|
|<span data-ttu-id="13fa7-169">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-169">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="13fa7-170">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-170"></span></span>|
|<span data-ttu-id="13fa7-171">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-171">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-172">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-172"></span></span>|
|<span data-ttu-id="13fa7-173">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-173">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-174">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-174"></span></span>|
   
 <span data-ttu-id="13fa7-175">**RAIZ CNNIC**</span><span class="sxs-lookup"><span data-stu-id="13fa7-175">**CNNIC ROOT**</span></span>
  
||
|:-----|
|<span data-ttu-id="13fa7-176">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-176">**Subject**</span></span>|
|<span data-ttu-id="13fa7-177">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-177"></span></span>|
|<span data-ttu-id="13fa7-178">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="13fa7-178">**Serial Number**</span></span>|
|<span data-ttu-id="13fa7-179">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-179"></span></span>|
|<span data-ttu-id="13fa7-180">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="13fa7-180">**Public Key Length**</span></span>|
|<span data-ttu-id="13fa7-181">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-181"></span></span>|
|<span data-ttu-id="13fa7-182">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="13fa7-182">**Signature Algorithm**</span></span>|
|<span data-ttu-id="13fa7-183">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-183"></span></span>|
|<span data-ttu-id="13fa7-184">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-184">**Validity Not Before**</span></span>|
|<span data-ttu-id="13fa7-185">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-185"></span></span>|
|<span data-ttu-id="13fa7-186">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="13fa7-186">**Validity Not After**</span></span>|
|<span data-ttu-id="13fa7-187">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-187"></span></span>|
|<span data-ttu-id="13fa7-188">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-188">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-189">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-189"></span></span>|
|<span data-ttu-id="13fa7-190">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-190">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-191">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-191"></span></span>|
|<span data-ttu-id="13fa7-192">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-192">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="13fa7-193">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-193"></span></span>|
|<span data-ttu-id="13fa7-194">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-194">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-195">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-195"></span></span>|
|<span data-ttu-id="13fa7-196">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-196">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-197">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-197"></span></span>|
   
 <span data-ttu-id="13fa7-198">**CA de raiz Global DigiCert**</span><span class="sxs-lookup"><span data-stu-id="13fa7-198">**DigiCert Global Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="13fa7-199">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-199">**Subject**</span></span>|
|<span data-ttu-id="13fa7-200">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-200"></span></span>|
|<span data-ttu-id="13fa7-201">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="13fa7-201">**Serial Number**</span></span>|
|<span data-ttu-id="13fa7-202">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-202"></span></span>|
|<span data-ttu-id="13fa7-203">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="13fa7-203">**Public Key Length**</span></span>|
|<span data-ttu-id="13fa7-204">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-204"></span></span>|
|<span data-ttu-id="13fa7-205">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="13fa7-205">**Signature Algorithm**</span></span>|
|<span data-ttu-id="13fa7-206">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-206"></span></span>|
|<span data-ttu-id="13fa7-207">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-207">**Validity Not Before**</span></span>|
|<span data-ttu-id="13fa7-208">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-208"></span></span>|
|<span data-ttu-id="13fa7-209">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="13fa7-209">**Validity Not After**</span></span>|
|<span data-ttu-id="13fa7-210">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-210"></span></span>|
|<span data-ttu-id="13fa7-211">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-211">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-212">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-212"></span></span>|
|<span data-ttu-id="13fa7-213">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-213">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-214">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-214"></span></span>|
|<span data-ttu-id="13fa7-215">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-215">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="13fa7-216">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-216"></span></span>|
|<span data-ttu-id="13fa7-217">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-217">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-218">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-218"></span></span>|
|<span data-ttu-id="13fa7-219">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-219">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-220">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-220"></span></span>|
   
 <span data-ttu-id="13fa7-221">**Autoridade de certificação de raiz de garantia EV alta DigiCert**</span><span class="sxs-lookup"><span data-stu-id="13fa7-221">**DigiCert High Assurance EV Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="13fa7-222">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-222">**Subject**</span></span>|
|<span data-ttu-id="13fa7-223">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-223"></span></span>|
|<span data-ttu-id="13fa7-224">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="13fa7-224">**Serial Number**</span></span>|
|<span data-ttu-id="13fa7-225">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-225"></span></span>|
|<span data-ttu-id="13fa7-226">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="13fa7-226">**Public Key Length**</span></span>|
|<span data-ttu-id="13fa7-227">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-227"></span></span>|
|<span data-ttu-id="13fa7-228">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="13fa7-228">**Signature Algorithm**</span></span>|
|<span data-ttu-id="13fa7-229">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-229"></span></span>|
|<span data-ttu-id="13fa7-230">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-230">**Validity Not Before**</span></span>|
|<span data-ttu-id="13fa7-231">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-231"></span></span>|
|<span data-ttu-id="13fa7-232">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="13fa7-232">**Validity Not After**</span></span>|
|<span data-ttu-id="13fa7-233">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-233"></span></span>|
|<span data-ttu-id="13fa7-234">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-234">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-235">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-235"></span></span>|
|<span data-ttu-id="13fa7-236">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-236">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-237">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-237"></span></span>|
|<span data-ttu-id="13fa7-238">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-238">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="13fa7-239">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-239"></span></span>|
|<span data-ttu-id="13fa7-240">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-240">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-241">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-241"></span></span>|
|<span data-ttu-id="13fa7-242">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-242">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-243">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-243"></span></span>|
   
 <span data-ttu-id="13fa7-244">**Autoridade de certificação da classe 3 de raiz de confiança D 2 de 2009**</span><span class="sxs-lookup"><span data-stu-id="13fa7-244">**D-TRUST Root Class 3 CA 2 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="13fa7-245">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-245">**Subject**</span></span>|
|<span data-ttu-id="13fa7-246">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-246"></span></span>|
|<span data-ttu-id="13fa7-247">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="13fa7-247">**Serial Number**</span></span>|
|<span data-ttu-id="13fa7-248">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-248"></span></span>|
|<span data-ttu-id="13fa7-249">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="13fa7-249">**Public Key Length**</span></span>|
|<span data-ttu-id="13fa7-250">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-250"></span></span>|
|<span data-ttu-id="13fa7-251">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="13fa7-251">**Signature Algorithm**</span></span>|
|<span data-ttu-id="13fa7-252">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-252"></span></span>|
|<span data-ttu-id="13fa7-253">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-253">**Validity Not Before**</span></span>|
|<span data-ttu-id="13fa7-254">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-254"></span></span>|
|<span data-ttu-id="13fa7-255">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="13fa7-255">**Validity Not After**</span></span>|
|<span data-ttu-id="13fa7-256">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-256"></span></span>|
|<span data-ttu-id="13fa7-257">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-257">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-258">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-258"></span></span>|
|<span data-ttu-id="13fa7-259">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-259">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="13fa7-260">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-260"></span></span>|
|<span data-ttu-id="13fa7-261">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-261">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-262">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-262"></span></span>|
|<span data-ttu-id="13fa7-263">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-263">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-264">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-264"></span></span>|
|<span data-ttu-id="13fa7-265">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="13fa7-265">**CRL URLs**</span></span>|
|<span data-ttu-id="13fa7-266">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-266"></span></span>|
   
 <span data-ttu-id="13fa7-267">**Autoridade de certificação raiz confiável D classe 3 2 EV de 2009**</span><span class="sxs-lookup"><span data-stu-id="13fa7-267">**D-TRUST Root Class 3 CA 2 EV 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="13fa7-268">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-268">**Subject**</span></span>|
|<span data-ttu-id="13fa7-269">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-269"></span></span>|
|<span data-ttu-id="13fa7-270">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="13fa7-270">**Serial Number**</span></span>|
|<span data-ttu-id="13fa7-271">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-271"></span></span>|
|<span data-ttu-id="13fa7-272">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="13fa7-272">**Public Key Length**</span></span>|
|<span data-ttu-id="13fa7-273">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-273"></span></span>|
|<span data-ttu-id="13fa7-274">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="13fa7-274">**Signature Algorithm**</span></span>|
|<span data-ttu-id="13fa7-275">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-275"></span></span>|
|<span data-ttu-id="13fa7-276">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-276">**Validity Not Before**</span></span>|
|<span data-ttu-id="13fa7-277">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-277"></span></span>|
|<span data-ttu-id="13fa7-278">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="13fa7-278">**Validity Not After**</span></span>|
|<span data-ttu-id="13fa7-279">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-279"></span></span>|
|<span data-ttu-id="13fa7-280">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-280">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-281">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-281"></span></span>|
|<span data-ttu-id="13fa7-282">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-282">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="13fa7-283">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-283"></span></span>|
|<span data-ttu-id="13fa7-284">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-284">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-285">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-285"></span></span>|
|<span data-ttu-id="13fa7-286">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-286">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-287">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-287"></span></span>|
|<span data-ttu-id="13fa7-288">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="13fa7-288">**CRL URLs**</span></span>|
|<span data-ttu-id="13fa7-289">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-289"></span></span>|
   
 <span data-ttu-id="13fa7-290">**Horário de verão raiz da autoridade de certificação X3**</span><span class="sxs-lookup"><span data-stu-id="13fa7-290">**DST Root CA X3**</span></span>
  
||
|:-----|
|<span data-ttu-id="13fa7-291">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-291">**Subject**</span></span>|
|<span data-ttu-id="13fa7-292">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-292"></span></span>|
|<span data-ttu-id="13fa7-293">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="13fa7-293">**Serial Number**</span></span>|
|<span data-ttu-id="13fa7-294">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-294"></span></span>|
|<span data-ttu-id="13fa7-295">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="13fa7-295">**Public Key Length**</span></span>|
|<span data-ttu-id="13fa7-296">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-296"></span></span>|
|<span data-ttu-id="13fa7-297">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="13fa7-297">**Signature Algorithm**</span></span>|
|<span data-ttu-id="13fa7-298">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-298"></span></span>|
|<span data-ttu-id="13fa7-299">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-299">**Validity Not Before**</span></span>|
|<span data-ttu-id="13fa7-300">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-300"></span></span>|
|<span data-ttu-id="13fa7-301">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="13fa7-301">**Validity Not After**</span></span>|
|<span data-ttu-id="13fa7-302">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-302"></span></span>|
|<span data-ttu-id="13fa7-303">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-303">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-304">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-304"></span></span>|
|<span data-ttu-id="13fa7-305">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-305">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="13fa7-306">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-306"></span></span>|
|<span data-ttu-id="13fa7-307">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-307">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-308">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-308"></span></span>|
|<span data-ttu-id="13fa7-309">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-309">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-310">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-310"></span></span>|
   
 <span data-ttu-id="13fa7-311">**Entrust autoridade de certificação raiz - G2**</span><span class="sxs-lookup"><span data-stu-id="13fa7-311">**Entrust Root Certification Authority - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="13fa7-312">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-312">**Subject**</span></span>|
|<span data-ttu-id="13fa7-313">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-313"></span></span>|
|<span data-ttu-id="13fa7-314">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="13fa7-314">**Serial Number**</span></span>|
|<span data-ttu-id="13fa7-315">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-315"></span></span>|
|<span data-ttu-id="13fa7-316">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="13fa7-316">**Public Key Length**</span></span>|
|<span data-ttu-id="13fa7-317">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-317"></span></span>|
|<span data-ttu-id="13fa7-318">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="13fa7-318">**Signature Algorithm**</span></span>|
|<span data-ttu-id="13fa7-319">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-319"></span></span>|
|<span data-ttu-id="13fa7-320">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-320">**Validity Not Before**</span></span>|
|<span data-ttu-id="13fa7-321">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-321"></span></span>|
|<span data-ttu-id="13fa7-322">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="13fa7-322">**Validity Not After**</span></span>|
|<span data-ttu-id="13fa7-323">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-323"></span></span>|
|<span data-ttu-id="13fa7-324">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-324">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-325">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-325"></span></span>|
|<span data-ttu-id="13fa7-326">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-326">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="13fa7-327">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-327"></span></span>|
|<span data-ttu-id="13fa7-328">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-328">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-329">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-329"></span></span>|
|<span data-ttu-id="13fa7-330">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-330">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-331">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-331"></span></span>|
   
 <span data-ttu-id="13fa7-332">**Entrust.net Certification Authority (2048)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-332">**Entrust.net Certification Authority (2048)**</span></span>
  
||
|:-----|
|<span data-ttu-id="13fa7-333">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-333">**Subject**</span></span>|
|<span data-ttu-id="13fa7-334">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-334"></span></span>|
|<span data-ttu-id="13fa7-335">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="13fa7-335">**Serial Number**</span></span>|
|<span data-ttu-id="13fa7-336">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-336"></span></span>|
|<span data-ttu-id="13fa7-337">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="13fa7-337">**Public Key Length**</span></span>|
|<span data-ttu-id="13fa7-338">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-338"></span></span>|
|<span data-ttu-id="13fa7-339">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="13fa7-339">**Signature Algorithm**</span></span>|
|<span data-ttu-id="13fa7-340">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-340"></span></span>|
|<span data-ttu-id="13fa7-341">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-341">**Validity Not Before**</span></span>|
|<span data-ttu-id="13fa7-342">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-342"></span></span>|
|<span data-ttu-id="13fa7-343">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="13fa7-343">**Validity Not After**</span></span>|
|<span data-ttu-id="13fa7-344">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-344"></span></span>|
|<span data-ttu-id="13fa7-345">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-345">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-346">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-346"></span></span>|
|<span data-ttu-id="13fa7-347">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-347">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="13fa7-348">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-348"></span></span>|
|<span data-ttu-id="13fa7-349">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-349">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-350">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-350"></span></span>|
|<span data-ttu-id="13fa7-351">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-351">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-352">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-352"></span></span>|
   
 <span data-ttu-id="13fa7-353">**GlobalSign**</span><span class="sxs-lookup"><span data-stu-id="13fa7-353">**GlobalSign**</span></span>
  
||
|:-----|
|<span data-ttu-id="13fa7-354">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-354">**Subject**</span></span>|
|<span data-ttu-id="13fa7-355">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-355"></span></span>|
|<span data-ttu-id="13fa7-356">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="13fa7-356">**Serial Number**</span></span>|
|<span data-ttu-id="13fa7-357">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-357"></span></span>|
|<span data-ttu-id="13fa7-358">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="13fa7-358">**Public Key Length**</span></span>|
|<span data-ttu-id="13fa7-359">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-359"></span></span>|
|<span data-ttu-id="13fa7-360">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="13fa7-360">**Signature Algorithm**</span></span>|
|<span data-ttu-id="13fa7-361">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-361"></span></span>|
|<span data-ttu-id="13fa7-362">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-362">**Validity Not Before**</span></span>|
|<span data-ttu-id="13fa7-363">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-363"></span></span>|
|<span data-ttu-id="13fa7-364">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="13fa7-364">**Validity Not After**</span></span>|
|<span data-ttu-id="13fa7-365">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-365"></span></span>|
|<span data-ttu-id="13fa7-366">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-366">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-367">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-367"></span></span>|
|<span data-ttu-id="13fa7-368">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-368">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-369">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-369"></span></span>|
|<span data-ttu-id="13fa7-370">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-370">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="13fa7-371">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-371"></span></span>|
|<span data-ttu-id="13fa7-372">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-372">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-373">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-373"></span></span>|
|<span data-ttu-id="13fa7-374">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-374">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-375">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-375"></span></span>|
|<span data-ttu-id="13fa7-376">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="13fa7-376">**CRL URLs**</span></span>|
|<span data-ttu-id="13fa7-377">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-377"></span></span>|
   
 <span data-ttu-id="13fa7-378">**GlobalSign Root CA**</span><span class="sxs-lookup"><span data-stu-id="13fa7-378">**GlobalSign Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="13fa7-379">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-379">**Subject**</span></span>|
|<span data-ttu-id="13fa7-380">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-380"></span></span>|
|<span data-ttu-id="13fa7-381">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="13fa7-381">**Serial Number**</span></span>|
|<span data-ttu-id="13fa7-382">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-382"></span></span>|
|<span data-ttu-id="13fa7-383">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="13fa7-383">**Public Key Length**</span></span>|
|<span data-ttu-id="13fa7-384">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-384"></span></span>|
|<span data-ttu-id="13fa7-385">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="13fa7-385">**Signature Algorithm**</span></span>|
|<span data-ttu-id="13fa7-386">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-386"></span></span>|
|<span data-ttu-id="13fa7-387">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-387">**Validity Not Before**</span></span>|
|<span data-ttu-id="13fa7-388">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-388"></span></span>|
|<span data-ttu-id="13fa7-389">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="13fa7-389">**Validity Not After**</span></span>|
|<span data-ttu-id="13fa7-390">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-390"></span></span>|
|<span data-ttu-id="13fa7-391">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-391">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-392">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-392"></span></span>|
|<span data-ttu-id="13fa7-393">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-393">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="13fa7-394">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-394"></span></span>|
|<span data-ttu-id="13fa7-395">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-395">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-396">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-396"></span></span>|
|<span data-ttu-id="13fa7-397">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-397">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-398">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-398"></span></span>|
   
 <span data-ttu-id="13fa7-399">**Thawte autoridade de certificação raiz primária - G3**</span><span class="sxs-lookup"><span data-stu-id="13fa7-399">**thawte Primary Root CA - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="13fa7-400">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-400">**Subject**</span></span>|
|<span data-ttu-id="13fa7-401">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-401"></span></span>|
|<span data-ttu-id="13fa7-402">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="13fa7-402">**Serial Number**</span></span>|
|<span data-ttu-id="13fa7-403">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-403"></span></span>|
|<span data-ttu-id="13fa7-404">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="13fa7-404">**Public Key Length**</span></span>|
|<span data-ttu-id="13fa7-405">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-405"></span></span>|
|<span data-ttu-id="13fa7-406">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="13fa7-406">**Signature Algorithm**</span></span>|
|<span data-ttu-id="13fa7-407">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-407"></span></span>|
|<span data-ttu-id="13fa7-408">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-408">**Validity Not Before**</span></span>|
|<span data-ttu-id="13fa7-409">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-409"></span></span>|
|<span data-ttu-id="13fa7-410">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="13fa7-410">**Validity Not After**</span></span>|
|<span data-ttu-id="13fa7-411">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-411"></span></span>|
|<span data-ttu-id="13fa7-412">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-412">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-413">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-413"></span></span>|
|<span data-ttu-id="13fa7-414">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-414">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="13fa7-415">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-415"></span></span>|
|<span data-ttu-id="13fa7-416">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-416">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-417">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-417"></span></span>|
|<span data-ttu-id="13fa7-418">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-418">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-419">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-419"></span></span>|
   
 <span data-ttu-id="13fa7-420">**Autoridade de certificação principal pública classe VeriSign 3 - G5**</span><span class="sxs-lookup"><span data-stu-id="13fa7-420">**VeriSign Class 3 Public Primary Certification Authority - G5**</span></span>
  
||
|:-----|
|<span data-ttu-id="13fa7-421">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-421">**Subject**</span></span>|
|<span data-ttu-id="13fa7-422">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-422"></span></span>|
|<span data-ttu-id="13fa7-423">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="13fa7-423">**Serial Number**</span></span>|
|<span data-ttu-id="13fa7-424">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-424"></span></span>|
|<span data-ttu-id="13fa7-425">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="13fa7-425">**Public Key Length**</span></span>|
|<span data-ttu-id="13fa7-426">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-426"></span></span>|
|<span data-ttu-id="13fa7-427">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="13fa7-427">**Signature Algorithm**</span></span>|
|<span data-ttu-id="13fa7-428">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-428"></span></span>|
|<span data-ttu-id="13fa7-429">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-429">**Validity Not Before**</span></span>|
|<span data-ttu-id="13fa7-430">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-430"></span></span>|
|<span data-ttu-id="13fa7-431">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="13fa7-431">**Validity Not After**</span></span>|
|<span data-ttu-id="13fa7-432">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-432"></span></span>|
|<span data-ttu-id="13fa7-433">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-433">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-434">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-434"></span></span>|
|<span data-ttu-id="13fa7-435">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-435">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="13fa7-436">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-436"></span></span>|
|<span data-ttu-id="13fa7-437">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-437">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-438">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-438"></span></span>|
|<span data-ttu-id="13fa7-439">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-439">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-440">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-440"></span></span>|
   
## <a name="office-365-intermediate-certificate-details"></a><span data-ttu-id="13fa7-441">Detalhes do certificado intermediário de Office 365</span><span class="sxs-lookup"><span data-stu-id="13fa7-441">Office 365 Intermediate Certificate Details</span></span>
<span data-ttu-id="13fa7-442"><a name="IntermediateCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="13fa7-442"></span></span>

 <span data-ttu-id="13fa7-443">**CNNIC SHA256 SSL**</span><span class="sxs-lookup"><span data-stu-id="13fa7-443">**CNNIC SHA256 SSL**</span></span>
  
||
|:-----|
|<span data-ttu-id="13fa7-444">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-444">**Subject**</span></span>|
|<span data-ttu-id="13fa7-445">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-445"></span></span>|
|<span data-ttu-id="13fa7-446">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="13fa7-446">**Issuer**</span></span>|
|<span data-ttu-id="13fa7-447">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-447"></span></span>|
|<span data-ttu-id="13fa7-448">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="13fa7-448">**Serial Number**</span></span>|
|<span data-ttu-id="13fa7-449">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-449"></span></span>|
|<span data-ttu-id="13fa7-450">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="13fa7-450">**Public Key Length**</span></span>|
|<span data-ttu-id="13fa7-451">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-451"></span></span>|
|<span data-ttu-id="13fa7-452">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="13fa7-452">**Signature Algorithm**</span></span>|
|<span data-ttu-id="13fa7-453">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-453"></span></span>|
|<span data-ttu-id="13fa7-454">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-454">**Validity Not Before**</span></span>|
|<span data-ttu-id="13fa7-455">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-455"></span></span>|
|<span data-ttu-id="13fa7-456">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="13fa7-456">**Validity Not After**</span></span>|
|<span data-ttu-id="13fa7-457">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-457"></span></span>|
|<span data-ttu-id="13fa7-458">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-458">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-459">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-459"></span></span>|
|<span data-ttu-id="13fa7-460">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-460">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-461">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-461"></span></span>|
|<span data-ttu-id="13fa7-462">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-462">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="13fa7-463">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-463"></span></span>|
|<span data-ttu-id="13fa7-464">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-464">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-465">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-465"></span></span>|
|<span data-ttu-id="13fa7-466">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-466">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-467">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-467"></span></span>|
|<span data-ttu-id="13fa7-468">**URLs AIA**</span><span class="sxs-lookup"><span data-stu-id="13fa7-468">**AIA URLs**</span></span>|
|<span data-ttu-id="13fa7-469">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-469"></span></span>|
|<span data-ttu-id="13fa7-470">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="13fa7-470">**CRL URLs**</span></span>|
|<span data-ttu-id="13fa7-471">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-471"></span></span>|
|<span data-ttu-id="13fa7-472">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="13fa7-472">**OCSP URLs**</span></span>|
|<span data-ttu-id="13fa7-473">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-473"></span></span>|
   
 <span data-ttu-id="13fa7-474">**D-TRUST SSL classe 3 CA 1 2009**</span><span class="sxs-lookup"><span data-stu-id="13fa7-474">**D-TRUST SSL Class 3 CA 1 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="13fa7-475">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-475">**Subject**</span></span>|
|<span data-ttu-id="13fa7-476">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-476"></span></span>|
|<span data-ttu-id="13fa7-477">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="13fa7-477">**Issuer**</span></span>|
|<span data-ttu-id="13fa7-478">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-478"></span></span>|
|<span data-ttu-id="13fa7-479">**Nome alternativo da entidade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-479">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="13fa7-480">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-480"></span></span>|
|<span data-ttu-id="13fa7-481">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="13fa7-481">**Serial Number**</span></span>|
|<span data-ttu-id="13fa7-482">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-482"></span></span>|
|<span data-ttu-id="13fa7-483">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="13fa7-483">**Public Key Length**</span></span>|
|<span data-ttu-id="13fa7-484">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-484"></span></span>|
|<span data-ttu-id="13fa7-485">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="13fa7-485">**Signature Algorithm**</span></span>|
|<span data-ttu-id="13fa7-486">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-486"></span></span>|
|<span data-ttu-id="13fa7-487">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-487">**Validity Not Before**</span></span>|
|<span data-ttu-id="13fa7-488">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-488"></span></span>|
|<span data-ttu-id="13fa7-489">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="13fa7-489">**Validity Not After**</span></span>|
|<span data-ttu-id="13fa7-490">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-490"></span></span>|
|<span data-ttu-id="13fa7-491">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-491">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-492">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-492"></span></span>|
|<span data-ttu-id="13fa7-493">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-493">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-494">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-494"></span></span>|
|<span data-ttu-id="13fa7-495">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-495">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="13fa7-496">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-496"></span></span>|
|<span data-ttu-id="13fa7-497">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-497">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-498">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-498"></span></span>|
|<span data-ttu-id="13fa7-499">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-499">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-500">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-500"></span></span>|
|<span data-ttu-id="13fa7-501">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="13fa7-501">**CRL URLs**</span></span>|
|<span data-ttu-id="13fa7-502">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-502"></span></span>|
|<span data-ttu-id="13fa7-503">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="13fa7-503">**OCSP URLs**</span></span>|
|<span data-ttu-id="13fa7-504">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-504"></span></span>|
   
 <span data-ttu-id="13fa7-505">**Autoridade de certificação confiável D SSL classe 3 1 EV de 2009**</span><span class="sxs-lookup"><span data-stu-id="13fa7-505">**D-TRUST SSL Class 3 CA 1 EV 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="13fa7-506">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-506">**Subject**</span></span>|
|<span data-ttu-id="13fa7-507">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-507"></span></span>|
|<span data-ttu-id="13fa7-508">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="13fa7-508">**Issuer**</span></span>|
|<span data-ttu-id="13fa7-509">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-509"></span></span>|
|<span data-ttu-id="13fa7-510">**Nome alternativo da entidade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-510">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="13fa7-511">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-511"></span></span>|
|<span data-ttu-id="13fa7-512">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="13fa7-512">**Serial Number**</span></span>|
|<span data-ttu-id="13fa7-513">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-513"></span></span>|
|<span data-ttu-id="13fa7-514">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="13fa7-514">**Public Key Length**</span></span>|
|<span data-ttu-id="13fa7-515">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-515"></span></span>|
|<span data-ttu-id="13fa7-516">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="13fa7-516">**Signature Algorithm**</span></span>|
|<span data-ttu-id="13fa7-517">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-517"></span></span>|
|<span data-ttu-id="13fa7-518">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-518">**Validity Not Before**</span></span>|
|<span data-ttu-id="13fa7-519">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-519"></span></span>|
|<span data-ttu-id="13fa7-520">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="13fa7-520">**Validity Not After**</span></span>|
|<span data-ttu-id="13fa7-521">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-521"></span></span>|
|<span data-ttu-id="13fa7-522">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-522">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-523">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-523"></span></span>|
|<span data-ttu-id="13fa7-524">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-524">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-525">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-525"></span></span>|
|<span data-ttu-id="13fa7-526">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-526">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="13fa7-527">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-527"></span></span>|
|<span data-ttu-id="13fa7-528">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-528">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-529">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-529"></span></span>|
|<span data-ttu-id="13fa7-530">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-530">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-531">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-531"></span></span>|
|<span data-ttu-id="13fa7-532">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="13fa7-532">**CRL URLs**</span></span>|
|<span data-ttu-id="13fa7-533">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-533"></span></span>|
|<span data-ttu-id="13fa7-534">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="13fa7-534">**OCSP URLs**</span></span>|
|<span data-ttu-id="13fa7-535">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-535"></span></span>|
   
 <span data-ttu-id="13fa7-536">**Serviços em nuvem de DigiCert CA-1**</span><span class="sxs-lookup"><span data-stu-id="13fa7-536">**DigiCert Cloud Services CA-1**</span></span>
  
||
|:-----|
|<span data-ttu-id="13fa7-537">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-537">**Subject**</span></span>|
|<span data-ttu-id="13fa7-538">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-538"></span></span>|
|<span data-ttu-id="13fa7-539">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="13fa7-539">**Issuer**</span></span>|
|<span data-ttu-id="13fa7-540">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-540"></span></span>|
|<span data-ttu-id="13fa7-541">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="13fa7-541">**Serial Number**</span></span>|
|<span data-ttu-id="13fa7-542">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-542"></span></span>|
|<span data-ttu-id="13fa7-543">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="13fa7-543">**Public Key Length**</span></span>|
|<span data-ttu-id="13fa7-544">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-544"></span></span>|
|<span data-ttu-id="13fa7-545">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="13fa7-545">**Signature Algorithm**</span></span>|
|<span data-ttu-id="13fa7-546">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-546"></span></span>|
|<span data-ttu-id="13fa7-547">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-547">**Validity Not Before**</span></span>|
|<span data-ttu-id="13fa7-548">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-548"></span></span>|
|<span data-ttu-id="13fa7-549">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="13fa7-549">**Validity Not After**</span></span>|
|<span data-ttu-id="13fa7-550">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-550"></span></span>|
|<span data-ttu-id="13fa7-551">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-551">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-552">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-552"></span></span>|
|<span data-ttu-id="13fa7-553">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-553">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-554">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-554"></span></span>|
|<span data-ttu-id="13fa7-555">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-555">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="13fa7-556">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-556"></span></span>|
|<span data-ttu-id="13fa7-557">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-557">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-558">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-558"></span></span>|
|<span data-ttu-id="13fa7-559">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-559">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-560">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-560"></span></span>|
|<span data-ttu-id="13fa7-561">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="13fa7-561">**CRL URLs**</span></span>|
|<span data-ttu-id="13fa7-562">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-562"></span></span>|
|<span data-ttu-id="13fa7-563">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="13fa7-563">**OCSP URLs**</span></span>|
|<span data-ttu-id="13fa7-564">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-564"></span></span>|
   
 <span data-ttu-id="13fa7-565">**Servidor de alta garantia DigiCert SHA2 CA**</span><span class="sxs-lookup"><span data-stu-id="13fa7-565">**DigiCert SHA2 High Assurance Server CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="13fa7-566">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-566">**Subject**</span></span>|
|<span data-ttu-id="13fa7-567">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-567"></span></span>|
|<span data-ttu-id="13fa7-568">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="13fa7-568">**Issuer**</span></span>|
|<span data-ttu-id="13fa7-569">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-569"></span></span>|
|<span data-ttu-id="13fa7-570">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="13fa7-570">**Serial Number**</span></span>|
|<span data-ttu-id="13fa7-571">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-571"></span></span>|
|<span data-ttu-id="13fa7-572">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="13fa7-572">**Public Key Length**</span></span>|
|<span data-ttu-id="13fa7-573">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-573"></span></span>|
|<span data-ttu-id="13fa7-574">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="13fa7-574">**Signature Algorithm**</span></span>|
|<span data-ttu-id="13fa7-575">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-575"></span></span>|
|<span data-ttu-id="13fa7-576">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-576">**Validity Not Before**</span></span>|
|<span data-ttu-id="13fa7-577">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-577"></span></span>|
|<span data-ttu-id="13fa7-578">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="13fa7-578">**Validity Not After**</span></span>|
|<span data-ttu-id="13fa7-579">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-579"></span></span>|
|<span data-ttu-id="13fa7-580">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-580">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-581">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-581"></span></span>|
|<span data-ttu-id="13fa7-582">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-582">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-583">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-583"></span></span>|
|<span data-ttu-id="13fa7-584">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-584">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="13fa7-585">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-585"></span></span>|
|<span data-ttu-id="13fa7-586">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-586">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-587">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-587"></span></span>|
|<span data-ttu-id="13fa7-588">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-588">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-589">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-589"></span></span>|
|<span data-ttu-id="13fa7-590">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="13fa7-590">**CRL URLs**</span></span>|
|<span data-ttu-id="13fa7-591">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-591"></span></span>|
|<span data-ttu-id="13fa7-592">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="13fa7-592">**OCSP URLs**</span></span>|
|<span data-ttu-id="13fa7-593">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-593"></span></span>|
   
 <span data-ttu-id="13fa7-594">**Servidores de seguros DigiCert SHA2 CA**</span><span class="sxs-lookup"><span data-stu-id="13fa7-594">**DigiCert SHA2 Secure Server CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="13fa7-595">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-595">**Subject**</span></span>|
|<span data-ttu-id="13fa7-596">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-596"></span></span>|
|<span data-ttu-id="13fa7-597">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="13fa7-597">**Issuer**</span></span>|
|<span data-ttu-id="13fa7-598">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-598"></span></span>|
|<span data-ttu-id="13fa7-599">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="13fa7-599">**Serial Number**</span></span>|
|<span data-ttu-id="13fa7-600">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-600"></span></span>|
|<span data-ttu-id="13fa7-601">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="13fa7-601">**Public Key Length**</span></span>|
|<span data-ttu-id="13fa7-602">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-602"></span></span>|
|<span data-ttu-id="13fa7-603">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="13fa7-603">**Signature Algorithm**</span></span>|
|<span data-ttu-id="13fa7-604">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-604"></span></span>|
|<span data-ttu-id="13fa7-605">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-605">**Validity Not Before**</span></span>|
|<span data-ttu-id="13fa7-606">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-606"></span></span>|
|<span data-ttu-id="13fa7-607">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="13fa7-607">**Validity Not After**</span></span>|
|<span data-ttu-id="13fa7-608">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-608"></span></span>|
|<span data-ttu-id="13fa7-609">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-609">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-610">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-610"></span></span>|
|<span data-ttu-id="13fa7-611">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-611">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-612">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-612"></span></span>|
|<span data-ttu-id="13fa7-613">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-613">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="13fa7-614">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-614"></span></span>|
|<span data-ttu-id="13fa7-615">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-615">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-616">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-616"></span></span>|
|<span data-ttu-id="13fa7-617">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-617">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-618">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-618"></span></span>|
|<span data-ttu-id="13fa7-619">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="13fa7-619">**CRL URLs**</span></span>|
|<span data-ttu-id="13fa7-620">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-620"></span></span>|
|<span data-ttu-id="13fa7-621">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="13fa7-621">**OCSP URLs**</span></span>|
|<span data-ttu-id="13fa7-622">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-622"></span></span>|
   
 <span data-ttu-id="13fa7-623">**Entrust autoridade de certificação - L1C**</span><span class="sxs-lookup"><span data-stu-id="13fa7-623">**Entrust Certification Authority - L1C**</span></span>
  
||
|:-----|
|<span data-ttu-id="13fa7-624">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-624">**Subject**</span></span>|
|<span data-ttu-id="13fa7-625">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-625"></span></span>|
|<span data-ttu-id="13fa7-626">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="13fa7-626">**Issuer**</span></span>|
|<span data-ttu-id="13fa7-627">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-627"></span></span>|
|<span data-ttu-id="13fa7-628">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="13fa7-628">**Serial Number**</span></span>|
|<span data-ttu-id="13fa7-629">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-629"></span></span>|
|<span data-ttu-id="13fa7-630">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="13fa7-630">**Public Key Length**</span></span>|
|<span data-ttu-id="13fa7-631">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-631"></span></span>|
|<span data-ttu-id="13fa7-632">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="13fa7-632">**Signature Algorithm**</span></span>|
|<span data-ttu-id="13fa7-633">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-633"></span></span>|
|<span data-ttu-id="13fa7-634">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-634">**Validity Not Before**</span></span>|
|<span data-ttu-id="13fa7-635">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-635"></span></span>|
|<span data-ttu-id="13fa7-636">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="13fa7-636">**Validity Not After**</span></span>|
|<span data-ttu-id="13fa7-637">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-637"></span></span>|
|<span data-ttu-id="13fa7-638">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-638">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-639">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-639"></span></span>|
|<span data-ttu-id="13fa7-640">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-640">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-641">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-641"></span></span>|
|<span data-ttu-id="13fa7-642">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-642">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="13fa7-643">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-643"></span></span>|
|<span data-ttu-id="13fa7-644">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-644">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-645">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-645"></span></span>|
|<span data-ttu-id="13fa7-646">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-646">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-647">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-647"></span></span>|
|<span data-ttu-id="13fa7-648">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="13fa7-648">**CRL URLs**</span></span>|
|<span data-ttu-id="13fa7-649">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-649"></span></span>|
|<span data-ttu-id="13fa7-650">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="13fa7-650">**OCSP URLs**</span></span>|
|<span data-ttu-id="13fa7-651">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-651"></span></span>|
   
 <span data-ttu-id="13fa7-652">**Entrust autoridade de certificação - L1K**</span><span class="sxs-lookup"><span data-stu-id="13fa7-652">**Entrust Certification Authority - L1K**</span></span>
  
||
|:-----|
|<span data-ttu-id="13fa7-653">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-653">**Subject**</span></span>|
|<span data-ttu-id="13fa7-654">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-654"></span></span>|
|<span data-ttu-id="13fa7-655">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="13fa7-655">**Issuer**</span></span>|
|<span data-ttu-id="13fa7-656">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-656"></span></span>|
|<span data-ttu-id="13fa7-657">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="13fa7-657">**Serial Number**</span></span>|
|<span data-ttu-id="13fa7-658">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-658"></span></span>|
|<span data-ttu-id="13fa7-659">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="13fa7-659">**Public Key Length**</span></span>|
|<span data-ttu-id="13fa7-660">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-660"></span></span>|
|<span data-ttu-id="13fa7-661">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="13fa7-661">**Signature Algorithm**</span></span>|
|<span data-ttu-id="13fa7-662">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-662"></span></span>|
|<span data-ttu-id="13fa7-663">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-663">**Validity Not Before**</span></span>|
|<span data-ttu-id="13fa7-664">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-664"></span></span>|
|<span data-ttu-id="13fa7-665">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="13fa7-665">**Validity Not After**</span></span>|
|<span data-ttu-id="13fa7-666">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-666"></span></span>|
|<span data-ttu-id="13fa7-667">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-667">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-668">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-668"></span></span>|
|<span data-ttu-id="13fa7-669">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-669">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-670">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-670"></span></span>|
|<span data-ttu-id="13fa7-671">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-671">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="13fa7-672">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-672"></span></span>|
|<span data-ttu-id="13fa7-673">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-673">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-674">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-674"></span></span>|
|<span data-ttu-id="13fa7-675">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-675">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-676">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-676"></span></span>|
|<span data-ttu-id="13fa7-677">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="13fa7-677">**CRL URLs**</span></span>|
|<span data-ttu-id="13fa7-678">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-678"></span></span>|
|<span data-ttu-id="13fa7-679">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="13fa7-679">**OCSP URLs**</span></span>|
|<span data-ttu-id="13fa7-680">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-680"></span></span>|
   
 <span data-ttu-id="13fa7-681">**GlobalSign**</span><span class="sxs-lookup"><span data-stu-id="13fa7-681">**GlobalSign**</span></span>
  
||
|:-----|
|<span data-ttu-id="13fa7-682">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-682">**Subject**</span></span>|
|<span data-ttu-id="13fa7-683">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-683"></span></span>|
|<span data-ttu-id="13fa7-684">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="13fa7-684">**Issuer**</span></span>|
|<span data-ttu-id="13fa7-685">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-685"></span></span>|
|<span data-ttu-id="13fa7-686">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="13fa7-686">**Serial Number**</span></span>|
|<span data-ttu-id="13fa7-687">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-687"></span></span>|
|<span data-ttu-id="13fa7-688">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="13fa7-688">**Public Key Length**</span></span>|
|<span data-ttu-id="13fa7-689">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-689"></span></span>|
|<span data-ttu-id="13fa7-690">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="13fa7-690">**Signature Algorithm**</span></span>|
|<span data-ttu-id="13fa7-691">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-691"></span></span>|
|<span data-ttu-id="13fa7-692">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-692">**Validity Not Before**</span></span>|
|<span data-ttu-id="13fa7-693">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-693"></span></span>|
|<span data-ttu-id="13fa7-694">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="13fa7-694">**Validity Not After**</span></span>|
|<span data-ttu-id="13fa7-695">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-695"></span></span>|
|<span data-ttu-id="13fa7-696">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-696">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-697">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-697"></span></span>|
|<span data-ttu-id="13fa7-698">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-698">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-699">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-699"></span></span>|
|<span data-ttu-id="13fa7-700">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-700">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="13fa7-701">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-701"></span></span>|
|<span data-ttu-id="13fa7-702">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-702">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-703">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-703"></span></span>|
|<span data-ttu-id="13fa7-704">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-704">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-705">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-705"></span></span>|
|<span data-ttu-id="13fa7-706">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="13fa7-706">**CRL URLs**</span></span>|
|<span data-ttu-id="13fa7-707">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-707"></span></span>|
|<span data-ttu-id="13fa7-708">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="13fa7-708">**OCSP URLs**</span></span>|
|<span data-ttu-id="13fa7-709">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-709"></span></span>|
   
 <span data-ttu-id="13fa7-710">**GlobalSign estendido validação CA - SHA256 - G2**</span><span class="sxs-lookup"><span data-stu-id="13fa7-710">**GlobalSign Extended Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="13fa7-711">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-711">**Subject**</span></span>|
|<span data-ttu-id="13fa7-712">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-712"></span></span>|
|<span data-ttu-id="13fa7-713">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="13fa7-713">**Issuer**</span></span>|
|<span data-ttu-id="13fa7-714">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-714"></span></span>|
|<span data-ttu-id="13fa7-715">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="13fa7-715">**Serial Number**</span></span>|
|<span data-ttu-id="13fa7-716">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-716"></span></span>|
|<span data-ttu-id="13fa7-717">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="13fa7-717">**Public Key Length**</span></span>|
|<span data-ttu-id="13fa7-718">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-718"></span></span>|
|<span data-ttu-id="13fa7-719">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="13fa7-719">**Signature Algorithm**</span></span>|
|<span data-ttu-id="13fa7-720">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-720"></span></span>|
|<span data-ttu-id="13fa7-721">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-721">**Validity Not Before**</span></span>|
|<span data-ttu-id="13fa7-722">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-722"></span></span>|
|<span data-ttu-id="13fa7-723">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="13fa7-723">**Validity Not After**</span></span>|
|<span data-ttu-id="13fa7-724">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-724"></span></span>|
|<span data-ttu-id="13fa7-725">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-725">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-726">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-726"></span></span>|
|<span data-ttu-id="13fa7-727">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-727">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-728">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-728"></span></span>|
|<span data-ttu-id="13fa7-729">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-729">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="13fa7-730">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-730"></span></span>|
|<span data-ttu-id="13fa7-731">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-731">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-732">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-732"></span></span>|
|<span data-ttu-id="13fa7-733">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-733">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-734">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-734"></span></span>|
|<span data-ttu-id="13fa7-735">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="13fa7-735">**CRL URLs**</span></span>|
|<span data-ttu-id="13fa7-736">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-736"></span></span>|
|<span data-ttu-id="13fa7-737">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="13fa7-737">**OCSP URLs**</span></span>|
|<span data-ttu-id="13fa7-738">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-738"></span></span>|
   
 <span data-ttu-id="13fa7-739">**GlobalSign estendido validação CA - SHA256 - G3**</span><span class="sxs-lookup"><span data-stu-id="13fa7-739">**GlobalSign Extended Validation CA - SHA256 - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="13fa7-740">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-740">**Subject**</span></span>|
|<span data-ttu-id="13fa7-741">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-741"></span></span>|
|<span data-ttu-id="13fa7-742">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="13fa7-742">**Issuer**</span></span>|
|<span data-ttu-id="13fa7-743">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-743"></span></span>|
|<span data-ttu-id="13fa7-744">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="13fa7-744">**Serial Number**</span></span>|
|<span data-ttu-id="13fa7-745">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-745"></span></span>|
|<span data-ttu-id="13fa7-746">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="13fa7-746">**Public Key Length**</span></span>|
|<span data-ttu-id="13fa7-747">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-747"></span></span>|
|<span data-ttu-id="13fa7-748">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="13fa7-748">**Signature Algorithm**</span></span>|
|<span data-ttu-id="13fa7-749">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-749"></span></span>|
|<span data-ttu-id="13fa7-750">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-750">**Validity Not Before**</span></span>|
|<span data-ttu-id="13fa7-751">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-751"></span></span>|
|<span data-ttu-id="13fa7-752">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="13fa7-752">**Validity Not After**</span></span>|
|<span data-ttu-id="13fa7-753">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-753"></span></span>|
|<span data-ttu-id="13fa7-754">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-754">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-755">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-755"></span></span>|
|<span data-ttu-id="13fa7-756">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-756">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-757">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-757"></span></span>|
|<span data-ttu-id="13fa7-758">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-758">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="13fa7-759">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-759"></span></span>|
|<span data-ttu-id="13fa7-760">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-760">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-761">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-761"></span></span>|
|<span data-ttu-id="13fa7-762">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-762">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-763">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-763"></span></span>|
|<span data-ttu-id="13fa7-764">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="13fa7-764">**CRL URLs**</span></span>|
|<span data-ttu-id="13fa7-765">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-765"></span></span>|
|<span data-ttu-id="13fa7-766">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="13fa7-766">**OCSP URLs**</span></span>|
|<span data-ttu-id="13fa7-767">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-767"></span></span>|
   
 <span data-ttu-id="13fa7-768">**GlobalSign organização validação CA - SHA256 - G2**</span><span class="sxs-lookup"><span data-stu-id="13fa7-768">**GlobalSign Organization Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="13fa7-769">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-769">**Subject**</span></span>|
|<span data-ttu-id="13fa7-770">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-770"></span></span>|
|<span data-ttu-id="13fa7-771">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="13fa7-771">**Issuer**</span></span>|
|<span data-ttu-id="13fa7-772">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-772"></span></span>|
|<span data-ttu-id="13fa7-773">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="13fa7-773">**Serial Number**</span></span>|
|<span data-ttu-id="13fa7-774">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-774"></span></span>|
|<span data-ttu-id="13fa7-775">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="13fa7-775">**Public Key Length**</span></span>|
|<span data-ttu-id="13fa7-776">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-776"></span></span>|
|<span data-ttu-id="13fa7-777">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="13fa7-777">**Signature Algorithm**</span></span>|
|<span data-ttu-id="13fa7-778">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-778"></span></span>|
|<span data-ttu-id="13fa7-779">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-779">**Validity Not Before**</span></span>|
|<span data-ttu-id="13fa7-780">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-780"></span></span>|
|<span data-ttu-id="13fa7-781">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="13fa7-781">**Validity Not After**</span></span>|
|<span data-ttu-id="13fa7-782">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-782"></span></span>|
|<span data-ttu-id="13fa7-783">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-783">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-784">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-784"></span></span>|
|<span data-ttu-id="13fa7-785">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-785">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-786">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-786"></span></span>|
|<span data-ttu-id="13fa7-787">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-787">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="13fa7-788">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-788"></span></span>|
|<span data-ttu-id="13fa7-789">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-789">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-790">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-790"></span></span>|
|<span data-ttu-id="13fa7-791">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-791">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-792">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-792"></span></span>|
|<span data-ttu-id="13fa7-793">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="13fa7-793">**CRL URLs**</span></span>|
|<span data-ttu-id="13fa7-794">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-794"></span></span>|
|<span data-ttu-id="13fa7-795">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="13fa7-795">**OCSP URLs**</span></span>|
|<span data-ttu-id="13fa7-796">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-796"></span></span>|
   
 <span data-ttu-id="13fa7-797">**GlobalSign organização validação CA - SHA256 - G2**</span><span class="sxs-lookup"><span data-stu-id="13fa7-797">**GlobalSign Organization Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="13fa7-798">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-798">**Subject**</span></span>|
|<span data-ttu-id="13fa7-799">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-799"></span></span>|
|<span data-ttu-id="13fa7-800">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="13fa7-800">**Issuer**</span></span>|
|<span data-ttu-id="13fa7-801">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-801"></span></span>|
|<span data-ttu-id="13fa7-802">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="13fa7-802">**Serial Number**</span></span>|
|<span data-ttu-id="13fa7-803">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-803"></span></span>|
|<span data-ttu-id="13fa7-804">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="13fa7-804">**Public Key Length**</span></span>|
|<span data-ttu-id="13fa7-805">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-805"></span></span>|
|<span data-ttu-id="13fa7-806">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="13fa7-806">**Signature Algorithm**</span></span>|
|<span data-ttu-id="13fa7-807">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-807"></span></span>|
|<span data-ttu-id="13fa7-808">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-808">**Validity Not Before**</span></span>|
|<span data-ttu-id="13fa7-809">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-809"></span></span>|
|<span data-ttu-id="13fa7-810">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="13fa7-810">**Validity Not After**</span></span>|
|<span data-ttu-id="13fa7-811">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-811"></span></span>|
|<span data-ttu-id="13fa7-812">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-812">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-813">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-813"></span></span>|
|<span data-ttu-id="13fa7-814">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-814">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-815">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-815"></span></span>|
|<span data-ttu-id="13fa7-816">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-816">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="13fa7-817">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-817"></span></span>|
|<span data-ttu-id="13fa7-818">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-818">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-819">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-819"></span></span>|
|<span data-ttu-id="13fa7-820">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-820">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-821">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-821"></span></span>|
|<span data-ttu-id="13fa7-822">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="13fa7-822">**CRL URLs**</span></span>|
|<span data-ttu-id="13fa7-823">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-823"></span></span>|
|<span data-ttu-id="13fa7-824">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="13fa7-824">**OCSP URLs**</span></span>|
|<span data-ttu-id="13fa7-825">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-825"></span></span>|
   
 <span data-ttu-id="13fa7-826">**Criptografar vamos autoridade X3**</span><span class="sxs-lookup"><span data-stu-id="13fa7-826">**Let's Encrypt Authority X3**</span></span>
  
||
|:-----|
|<span data-ttu-id="13fa7-827">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-827">**Subject**</span></span>|
|<span data-ttu-id="13fa7-828">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-828"></span></span>|
|<span data-ttu-id="13fa7-829">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="13fa7-829">**Issuer**</span></span>|
|<span data-ttu-id="13fa7-830">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-830"></span></span>|
|<span data-ttu-id="13fa7-831">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="13fa7-831">**Serial Number**</span></span>|
|<span data-ttu-id="13fa7-832">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-832"></span></span>|
|<span data-ttu-id="13fa7-833">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="13fa7-833">**Public Key Length**</span></span>|
|<span data-ttu-id="13fa7-834">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-834"></span></span>|
|<span data-ttu-id="13fa7-835">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="13fa7-835">**Signature Algorithm**</span></span>|
|<span data-ttu-id="13fa7-836">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-836"></span></span>|
|<span data-ttu-id="13fa7-837">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-837">**Validity Not Before**</span></span>|
|<span data-ttu-id="13fa7-838">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-838"></span></span>|
|<span data-ttu-id="13fa7-839">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="13fa7-839">**Validity Not After**</span></span>|
|<span data-ttu-id="13fa7-840">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-840"></span></span>|
|<span data-ttu-id="13fa7-841">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-841">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-842">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-842"></span></span>|
|<span data-ttu-id="13fa7-843">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-843">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-844">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-844"></span></span>|
|<span data-ttu-id="13fa7-845">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-845">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="13fa7-846">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-846"></span></span>|
|<span data-ttu-id="13fa7-847">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-847">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-848">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-848"></span></span>|
|<span data-ttu-id="13fa7-849">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-849">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-850">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-850"></span></span>|
|<span data-ttu-id="13fa7-851">**URLs AIA**</span><span class="sxs-lookup"><span data-stu-id="13fa7-851">**AIA URLs**</span></span>|
|<span data-ttu-id="13fa7-852">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-852"></span></span>|
|<span data-ttu-id="13fa7-853">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="13fa7-853">**CRL URLs**</span></span>|
|<span data-ttu-id="13fa7-854">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-854"></span></span>|
|<span data-ttu-id="13fa7-855">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="13fa7-855">**OCSP URLs**</span></span>|
|<span data-ttu-id="13fa7-856">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-856"></span></span>|
   
 <span data-ttu-id="13fa7-857">**O TI da Microsoft SSL SHA2**</span><span class="sxs-lookup"><span data-stu-id="13fa7-857">**Microsoft IT SSL SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="13fa7-858">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-858">**Subject**</span></span>|
|<span data-ttu-id="13fa7-859">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-859"></span></span>|
|<span data-ttu-id="13fa7-860">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="13fa7-860">**Issuer**</span></span>|
|<span data-ttu-id="13fa7-861">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-861"></span></span>|
|<span data-ttu-id="13fa7-862">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="13fa7-862">**Serial Number**</span></span>|
|<span data-ttu-id="13fa7-863">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-863"></span></span>|
|<span data-ttu-id="13fa7-864">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="13fa7-864">**Public Key Length**</span></span>|
|<span data-ttu-id="13fa7-865">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-865"></span></span>|
|<span data-ttu-id="13fa7-866">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="13fa7-866">**Signature Algorithm**</span></span>|
|<span data-ttu-id="13fa7-867">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-867"></span></span>|
|<span data-ttu-id="13fa7-868">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-868">**Validity Not Before**</span></span>|
|<span data-ttu-id="13fa7-869">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-869"></span></span>|
|<span data-ttu-id="13fa7-870">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="13fa7-870">**Validity Not After**</span></span>|
|<span data-ttu-id="13fa7-871">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-871"></span></span>|
|<span data-ttu-id="13fa7-872">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-872">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-873">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-873"></span></span>|
|<span data-ttu-id="13fa7-874">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-874">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-875">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-875"></span></span>|
|<span data-ttu-id="13fa7-876">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-876">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="13fa7-877">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-877"></span></span>|
|<span data-ttu-id="13fa7-878">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-878">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-879">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-879"></span></span>|
|<span data-ttu-id="13fa7-880">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-880">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-881">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-881"></span></span>|
|<span data-ttu-id="13fa7-882">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="13fa7-882">**CRL URLs**</span></span>|
|<span data-ttu-id="13fa7-883">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-883"></span></span>|
   
 <span data-ttu-id="13fa7-884">**O TI da Microsoft SSL SHA2**</span><span class="sxs-lookup"><span data-stu-id="13fa7-884">**Microsoft IT SSL SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="13fa7-885">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-885">**Subject**</span></span>|
|<span data-ttu-id="13fa7-886">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-886"></span></span>|
|<span data-ttu-id="13fa7-887">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="13fa7-887">**Issuer**</span></span>|
|<span data-ttu-id="13fa7-888">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-888"></span></span>|
|<span data-ttu-id="13fa7-889">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="13fa7-889">**Serial Number**</span></span>|
|<span data-ttu-id="13fa7-890">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-890"></span></span>|
|<span data-ttu-id="13fa7-891">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="13fa7-891">**Public Key Length**</span></span>|
|<span data-ttu-id="13fa7-892">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-892"></span></span>|
|<span data-ttu-id="13fa7-893">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="13fa7-893">**Signature Algorithm**</span></span>|
|<span data-ttu-id="13fa7-894">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-894"></span></span>|
|<span data-ttu-id="13fa7-895">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-895">**Validity Not Before**</span></span>|
|<span data-ttu-id="13fa7-896">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-896"></span></span>|
|<span data-ttu-id="13fa7-897">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="13fa7-897">**Validity Not After**</span></span>|
|<span data-ttu-id="13fa7-898">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-898"></span></span>|
|<span data-ttu-id="13fa7-899">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-899">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-900">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-900"></span></span>|
|<span data-ttu-id="13fa7-901">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-901">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-902">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-902"></span></span>|
|<span data-ttu-id="13fa7-903">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-903">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="13fa7-904">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-904"></span></span>|
|<span data-ttu-id="13fa7-905">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-905">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-906">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-906"></span></span>|
|<span data-ttu-id="13fa7-907">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-907">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-908">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-908"></span></span>|
|<span data-ttu-id="13fa7-909">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="13fa7-909">**CRL URLs**</span></span>|
|<span data-ttu-id="13fa7-910">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-910"></span></span>|
|<span data-ttu-id="13fa7-911">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="13fa7-911">**OCSP URLs**</span></span>|
|<span data-ttu-id="13fa7-912">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-912"></span></span>|
   
 <span data-ttu-id="13fa7-913">**Autoridade de certificação do Microsoft IT TLS 1**</span><span class="sxs-lookup"><span data-stu-id="13fa7-913">**Microsoft IT TLS CA 1**</span></span>
  
||
|:-----|
|<span data-ttu-id="13fa7-914">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-914">**Subject**</span></span>|
|<span data-ttu-id="13fa7-915">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-915"></span></span>|
|<span data-ttu-id="13fa7-916">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="13fa7-916">**Issuer**</span></span>|
|<span data-ttu-id="13fa7-917">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-917"></span></span>|
|<span data-ttu-id="13fa7-918">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="13fa7-918">**Serial Number**</span></span>|
|<span data-ttu-id="13fa7-919">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-919"></span></span>|
|<span data-ttu-id="13fa7-920">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="13fa7-920">**Public Key Length**</span></span>|
|<span data-ttu-id="13fa7-921">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-921"></span></span>|
|<span data-ttu-id="13fa7-922">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="13fa7-922">**Signature Algorithm**</span></span>|
|<span data-ttu-id="13fa7-923">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-923"></span></span>|
|<span data-ttu-id="13fa7-924">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-924">**Validity Not Before**</span></span>|
|<span data-ttu-id="13fa7-925">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-925"></span></span>|
|<span data-ttu-id="13fa7-926">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="13fa7-926">**Validity Not After**</span></span>|
|<span data-ttu-id="13fa7-927">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-927"></span></span>|
|<span data-ttu-id="13fa7-928">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-928">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-929">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-929"></span></span>|
|<span data-ttu-id="13fa7-930">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-930">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-931">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-931"></span></span>|
|<span data-ttu-id="13fa7-932">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-932">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="13fa7-933">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-933"></span></span>|
|<span data-ttu-id="13fa7-934">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-934">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-935">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-935"></span></span>|
|<span data-ttu-id="13fa7-936">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-936">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-937">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-937"></span></span>|
|<span data-ttu-id="13fa7-938">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="13fa7-938">**CRL URLs**</span></span>|
|<span data-ttu-id="13fa7-939">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-939"></span></span>|
|<span data-ttu-id="13fa7-940">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="13fa7-940">**OCSP URLs**</span></span>|
|<span data-ttu-id="13fa7-941">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-941"></span></span>|
   
 <span data-ttu-id="13fa7-942">**Autoridade de certificação do Microsoft IT TLS 2**</span><span class="sxs-lookup"><span data-stu-id="13fa7-942">**Microsoft IT TLS CA 2**</span></span>
  
||
|:-----|
|<span data-ttu-id="13fa7-943">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-943">**Subject**</span></span>|
|<span data-ttu-id="13fa7-944">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-944"></span></span>|
|<span data-ttu-id="13fa7-945">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="13fa7-945">**Issuer**</span></span>|
|<span data-ttu-id="13fa7-946">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-946"></span></span>|
|<span data-ttu-id="13fa7-947">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="13fa7-947">**Serial Number**</span></span>|
|<span data-ttu-id="13fa7-948">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-948"></span></span>|
|<span data-ttu-id="13fa7-949">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="13fa7-949">**Public Key Length**</span></span>|
|<span data-ttu-id="13fa7-950">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-950"></span></span>|
|<span data-ttu-id="13fa7-951">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="13fa7-951">**Signature Algorithm**</span></span>|
|<span data-ttu-id="13fa7-952">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-952"></span></span>|
|<span data-ttu-id="13fa7-953">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-953">**Validity Not Before**</span></span>|
|<span data-ttu-id="13fa7-954">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-954"></span></span>|
|<span data-ttu-id="13fa7-955">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="13fa7-955">**Validity Not After**</span></span>|
|<span data-ttu-id="13fa7-956">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-956"></span></span>|
|<span data-ttu-id="13fa7-957">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-957">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-958">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-958"></span></span>|
|<span data-ttu-id="13fa7-959">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-959">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-960">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-960"></span></span>|
|<span data-ttu-id="13fa7-961">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-961">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="13fa7-962">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-962"></span></span>|
|<span data-ttu-id="13fa7-963">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-963">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-964">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-964"></span></span>|
|<span data-ttu-id="13fa7-965">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-965">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-966">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-966"></span></span>|
|<span data-ttu-id="13fa7-967">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="13fa7-967">**CRL URLs**</span></span>|
|<span data-ttu-id="13fa7-968">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-968"></span></span>|
|<span data-ttu-id="13fa7-969">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="13fa7-969">**OCSP URLs**</span></span>|
|<span data-ttu-id="13fa7-970">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-970"></span></span>|
   
 <span data-ttu-id="13fa7-971">**Autoridade de certificação do Microsoft IT TLS 4**</span><span class="sxs-lookup"><span data-stu-id="13fa7-971">**Microsoft IT TLS CA 4**</span></span>
  
||
|:-----|
|<span data-ttu-id="13fa7-972">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-972">**Subject**</span></span>|
|<span data-ttu-id="13fa7-973">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-973"></span></span>|
|<span data-ttu-id="13fa7-974">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="13fa7-974">**Issuer**</span></span>|
|<span data-ttu-id="13fa7-975">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-975"></span></span>|
|<span data-ttu-id="13fa7-976">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="13fa7-976">**Serial Number**</span></span>|
|<span data-ttu-id="13fa7-977">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-977"></span></span>|
|<span data-ttu-id="13fa7-978">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="13fa7-978">**Public Key Length**</span></span>|
|<span data-ttu-id="13fa7-979">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-979"></span></span>|
|<span data-ttu-id="13fa7-980">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="13fa7-980">**Signature Algorithm**</span></span>|
|<span data-ttu-id="13fa7-981">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-981"></span></span>|
|<span data-ttu-id="13fa7-982">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-982">**Validity Not Before**</span></span>|
|<span data-ttu-id="13fa7-983">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-983"></span></span>|
|<span data-ttu-id="13fa7-984">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="13fa7-984">**Validity Not After**</span></span>|
|<span data-ttu-id="13fa7-985">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-985"></span></span>|
|<span data-ttu-id="13fa7-986">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-986">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-987">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-987"></span></span>|
|<span data-ttu-id="13fa7-988">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-988">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-989">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-989"></span></span>|
|<span data-ttu-id="13fa7-990">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-990">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="13fa7-991">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-991"></span></span>|
|<span data-ttu-id="13fa7-992">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-992">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-993">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-993"></span></span>|
|<span data-ttu-id="13fa7-994">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-994">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-995">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-995"></span></span>|
|<span data-ttu-id="13fa7-996">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="13fa7-996">**CRL URLs**</span></span>|
|<span data-ttu-id="13fa7-997">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-997"></span></span>|
|<span data-ttu-id="13fa7-998">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="13fa7-998">**OCSP URLs**</span></span>|
|<span data-ttu-id="13fa7-999">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-999"></span></span>|
   
 <span data-ttu-id="13fa7-1000">**Autoridade de certificação do Microsoft IT TLS 5**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1000">**Microsoft IT TLS CA 5**</span></span>
  
||
|:-----|
|<span data-ttu-id="13fa7-1001">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1001">**Subject**</span></span>|
|<span data-ttu-id="13fa7-1002">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1002"></span></span>|
|<span data-ttu-id="13fa7-1003">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1003">**Issuer**</span></span>|
|<span data-ttu-id="13fa7-1004">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1004"></span></span>|
|<span data-ttu-id="13fa7-1005">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1005">**Serial Number**</span></span>|
|<span data-ttu-id="13fa7-1006">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1006"></span></span>|
|<span data-ttu-id="13fa7-1007">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1007">**Public Key Length**</span></span>|
|<span data-ttu-id="13fa7-1008">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1008"></span></span>|
|<span data-ttu-id="13fa7-1009">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1009">**Signature Algorithm**</span></span>|
|<span data-ttu-id="13fa7-1010">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1010"></span></span>|
|<span data-ttu-id="13fa7-1011">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1011">**Validity Not Before**</span></span>|
|<span data-ttu-id="13fa7-1012">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1012"></span></span>|
|<span data-ttu-id="13fa7-1013">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1013">**Validity Not After**</span></span>|
|<span data-ttu-id="13fa7-1014">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1014"></span></span>|
|<span data-ttu-id="13fa7-1015">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1015">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-1016">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1016"></span></span>|
|<span data-ttu-id="13fa7-1017">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1017">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-1018">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1018"></span></span>|
|<span data-ttu-id="13fa7-1019">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1019">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="13fa7-1020">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1020"></span></span>|
|<span data-ttu-id="13fa7-1021">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1021">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-1022">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1022"></span></span>|
|<span data-ttu-id="13fa7-1023">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1023">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-1024">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1024"></span></span>|
|<span data-ttu-id="13fa7-1025">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1025">**CRL URLs**</span></span>|
|<span data-ttu-id="13fa7-1026">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1026"></span></span>|
|<span data-ttu-id="13fa7-1027">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1027">**OCSP URLs**</span></span>|
|<span data-ttu-id="13fa7-1028">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1028"></span></span>|
   
 <span data-ttu-id="13fa7-1029">**CA de SSL Symantec classe EV 3 - G3**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1029">**Symantec Class 3 EV SSL CA - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="13fa7-1030">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1030">**Subject**</span></span>|
|<span data-ttu-id="13fa7-1031">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1031"></span></span>|
|<span data-ttu-id="13fa7-1032">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1032">**Issuer**</span></span>|
|<span data-ttu-id="13fa7-1033">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1033"></span></span>|
|<span data-ttu-id="13fa7-1034">**Nome alternativo da entidade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1034">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="13fa7-1035">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1035"></span></span>|
|<span data-ttu-id="13fa7-1036">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1036">**Serial Number**</span></span>|
|<span data-ttu-id="13fa7-1037">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1037"></span></span>|
|<span data-ttu-id="13fa7-1038">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1038">**Public Key Length**</span></span>|
|<span data-ttu-id="13fa7-1039">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1039"></span></span>|
|<span data-ttu-id="13fa7-1040">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1040">**Signature Algorithm**</span></span>|
|<span data-ttu-id="13fa7-1041">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1041"></span></span>|
|<span data-ttu-id="13fa7-1042">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1042">**Validity Not Before**</span></span>|
|<span data-ttu-id="13fa7-1043">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1043"></span></span>|
|<span data-ttu-id="13fa7-1044">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1044">**Validity Not After**</span></span>|
|<span data-ttu-id="13fa7-1045">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1045"></span></span>|
|<span data-ttu-id="13fa7-1046">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1046">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-1047">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1047"></span></span>|
|<span data-ttu-id="13fa7-1048">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1048">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-1049">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1049"></span></span>|
|<span data-ttu-id="13fa7-1050">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1050">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="13fa7-1051">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1051"></span></span>|
|<span data-ttu-id="13fa7-1052">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1052">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-1053">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1053"></span></span>|
|<span data-ttu-id="13fa7-1054">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1054">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-1055">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1055"></span></span>|
|<span data-ttu-id="13fa7-1056">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1056">**CRL URLs**</span></span>|
|<span data-ttu-id="13fa7-1057">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1057"></span></span>|
|<span data-ttu-id="13fa7-1058">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1058">**OCSP URLs**</span></span>|
|<span data-ttu-id="13fa7-1059">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1059"></span></span>|
   
 <span data-ttu-id="13fa7-1060">**Symantec classe 3 servidores seguros CA - G4**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1060">**Symantec Class 3 Secure Server CA - G4**</span></span>
  
||
|:-----|
|<span data-ttu-id="13fa7-1061">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1061">**Subject**</span></span>|
|<span data-ttu-id="13fa7-1062">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1062"></span></span>|
|<span data-ttu-id="13fa7-1063">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1063">**Issuer**</span></span>|
|<span data-ttu-id="13fa7-1064">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1064"></span></span>|
|<span data-ttu-id="13fa7-1065">**Nome alternativo da entidade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1065">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="13fa7-1066">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1066"></span></span>|
|<span data-ttu-id="13fa7-1067">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1067">**Serial Number**</span></span>|
|<span data-ttu-id="13fa7-1068">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1068"></span></span>|
|<span data-ttu-id="13fa7-1069">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1069">**Public Key Length**</span></span>|
|<span data-ttu-id="13fa7-1070">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1070"></span></span>|
|<span data-ttu-id="13fa7-1071">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1071">**Signature Algorithm**</span></span>|
|<span data-ttu-id="13fa7-1072">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1072"></span></span>|
|<span data-ttu-id="13fa7-1073">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1073">**Validity Not Before**</span></span>|
|<span data-ttu-id="13fa7-1074">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1074"></span></span>|
|<span data-ttu-id="13fa7-1075">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1075">**Validity Not After**</span></span>|
|<span data-ttu-id="13fa7-1076">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1076"></span></span>|
|<span data-ttu-id="13fa7-1077">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1077">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-1078">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1078"></span></span>|
|<span data-ttu-id="13fa7-1079">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1079">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-1080">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1080"></span></span>|
|<span data-ttu-id="13fa7-1081">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1081">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="13fa7-1082">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1082"></span></span>|
|<span data-ttu-id="13fa7-1083">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1083">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-1084">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1084"></span></span>|
|<span data-ttu-id="13fa7-1085">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1085">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-1086">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1086"></span></span>|
|<span data-ttu-id="13fa7-1087">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1087">**CRL URLs**</span></span>|
|<span data-ttu-id="13fa7-1088">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1088"></span></span>|
|<span data-ttu-id="13fa7-1089">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1089">**OCSP URLs**</span></span>|
|<span data-ttu-id="13fa7-1090">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1090"></span></span>|
   
 <span data-ttu-id="13fa7-1091">**Thawte SHA256 SSL da autoridade de certificação**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1091">**thawte SHA256 SSL CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="13fa7-1092">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1092">**Subject**</span></span>|
|<span data-ttu-id="13fa7-1093">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1093"></span></span>|
|<span data-ttu-id="13fa7-1094">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1094">**Issuer**</span></span>|
|<span data-ttu-id="13fa7-1095">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1095"></span></span>|
|<span data-ttu-id="13fa7-1096">**Nome alternativo da entidade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1096">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="13fa7-1097">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1097"></span></span>|
|<span data-ttu-id="13fa7-1098">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1098">**Serial Number**</span></span>|
|<span data-ttu-id="13fa7-1099">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1099"></span></span>|
|<span data-ttu-id="13fa7-1100">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1100">**Public Key Length**</span></span>|
|<span data-ttu-id="13fa7-1101">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1101"></span></span>|
|<span data-ttu-id="13fa7-1102">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1102">**Signature Algorithm**</span></span>|
|<span data-ttu-id="13fa7-1103">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1103"></span></span>|
|<span data-ttu-id="13fa7-1104">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1104">**Validity Not Before**</span></span>|
|<span data-ttu-id="13fa7-1105">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1105"></span></span>|
|<span data-ttu-id="13fa7-1106">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1106">**Validity Not After**</span></span>|
|<span data-ttu-id="13fa7-1107">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1107"></span></span>|
|<span data-ttu-id="13fa7-1108">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1108">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-1109">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1109"></span></span>|
|<span data-ttu-id="13fa7-1110">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1110">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-1111">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1111"></span></span>|
|<span data-ttu-id="13fa7-1112">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1112">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="13fa7-1113">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1113"></span></span>|
|<span data-ttu-id="13fa7-1114">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1114">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-1115">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1115"></span></span>|
|<span data-ttu-id="13fa7-1116">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1116">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-1117">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1117"></span></span>|
|<span data-ttu-id="13fa7-1118">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1118">**CRL URLs**</span></span>|
|<span data-ttu-id="13fa7-1119">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1119"></span></span>|
|<span data-ttu-id="13fa7-1120">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1120">**OCSP URLs**</span></span>|
|<span data-ttu-id="13fa7-1121">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1121"></span></span>|
   
 <span data-ttu-id="13fa7-1122">**Verizon Akamai SureServer CA G14-SHA2**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1122">**Verizon Akamai SureServer CA G14-SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="13fa7-1123">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1123">**Subject**</span></span>|
|<span data-ttu-id="13fa7-1124">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1124"></span></span>|
|<span data-ttu-id="13fa7-1125">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1125">**Issuer**</span></span>|
|<span data-ttu-id="13fa7-1126">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1126"></span></span>|
|<span data-ttu-id="13fa7-1127">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1127">**Serial Number**</span></span>|
|<span data-ttu-id="13fa7-1128">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1128"></span></span>|
|<span data-ttu-id="13fa7-1129">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1129">**Public Key Length**</span></span>|
|<span data-ttu-id="13fa7-1130">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1130"></span></span>|
|<span data-ttu-id="13fa7-1131">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1131">**Signature Algorithm**</span></span>|
|<span data-ttu-id="13fa7-1132">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1132"></span></span>|
|<span data-ttu-id="13fa7-1133">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1133">**Validity Not Before**</span></span>|
|<span data-ttu-id="13fa7-1134">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1134"></span></span>|
|<span data-ttu-id="13fa7-1135">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1135">**Validity Not After**</span></span>|
|<span data-ttu-id="13fa7-1136">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1136"></span></span>|
|<span data-ttu-id="13fa7-1137">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1137">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-1138">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1138"></span></span>|
|<span data-ttu-id="13fa7-1139">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1139">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="13fa7-1140">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1140"></span></span>|
|<span data-ttu-id="13fa7-1141">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1141">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="13fa7-1142">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1142"></span></span>|
|<span data-ttu-id="13fa7-1143">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1143">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-1144">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1144"></span></span>|
|<span data-ttu-id="13fa7-1145">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1145">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="13fa7-1146">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1146"></span></span>|
|<span data-ttu-id="13fa7-1147">**URLs AIA**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1147">**AIA URLs**</span></span>|
|<span data-ttu-id="13fa7-1148">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1148"></span></span>|
|<span data-ttu-id="13fa7-1149">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1149">**CRL URLs**</span></span>|
|<span data-ttu-id="13fa7-1150">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1150"></span></span>|
|<span data-ttu-id="13fa7-1151">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="13fa7-1151">**OCSP URLs**</span></span>|
|<span data-ttu-id="13fa7-1152">:-----</span><span class="sxs-lookup"><span data-stu-id="13fa7-1152"></span></span>|
   
## <a name="additional-certificate-paths"></a><span data-ttu-id="13fa7-1153">Caminhos de certificado adicional</span><span class="sxs-lookup"><span data-stu-id="13fa7-1153">Additional certificate paths</span></span>
<span data-ttu-id="13fa7-1154"><a name="IntermediateCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="13fa7-1154"></span></span>

<span data-ttu-id="13fa7-1155">A seguir incluem certificados herdados que não estão incluídos acima e serão mesclados com a lista acima ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="13fa7-1155">The following include legacy certificates that aren't included above and will be merged with the list above over time.</span></span>
  
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



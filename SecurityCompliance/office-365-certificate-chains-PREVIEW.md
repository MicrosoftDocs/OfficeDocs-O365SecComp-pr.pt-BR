---
title: Cadeias de certificados do Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/26/2018
ms.audience: ITPro
ms.topic: conceptual
ms.service: o365-administration
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Ent_O365
ms.assetid: 0c03e6b3-e73f-4316-9e2b-bf4091ae96bb
description: O Office 365 utiliza um número de provedores de certificado diferente. O exemplo a seguir descreve a lista completa de certificados de raiz Office 365 conhecidos que os clientes podem encontrar ao acessar o Office 365. Para obter informações sobre os certificados que você talvez precise instalar em sua própria infra-estrutura, consulte Plan for certificados SSL de terceiros para o Office 365. As seguintes informações de certificado se aplica a todas as instâncias de nuvem em todo o mundo e Nacional do Office 365.
ms.openlocfilehash: 97e00833e57f8f6b7352650b0efdef51ddba77fa
ms.sourcegitcommit: 659b5f5b38ef7e838cdb44eaa38c18e48d922768
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2018
ms.locfileid: "25575355"
---
# <a name="office-365-certificate-chains"></a><span data-ttu-id="27423-106">Cadeias de certificados do Office 365</span><span class="sxs-lookup"><span data-stu-id="27423-106">Office 365 Certificate Chains</span></span>

<span data-ttu-id="27423-p102">O Office 365 utiliza um número de provedores de certificado diferente. O exemplo a seguir descreve a lista completa de certificados de raiz Office 365 conhecidos que os clientes podem encontrar ao acessar o Office 365. Para obter informações sobre os certificados que você talvez precise instalar em sua própria infra-estrutura, consulte [Planejar certificados SSL de terceiros para o Office 365](https://support.office.com/article/b48cdf63-07e0-4cda-8c12-4871590f59ce). As seguintes informações de certificado se aplica a todas as instâncias de nuvem em todo o mundo e Nacional do Office 365.</span><span class="sxs-lookup"><span data-stu-id="27423-p102">Office 365 leverages a number of different certificate providers. The following describes the complete list of known Office 365 root certificates that customers may encounter when accessing Office 365. For information on the certificates you may need to install in your own infrastructure, see [Plan for third-party SSL certificates for Office 365](https://support.office.com/article/b48cdf63-07e0-4cda-8c12-4871590f59ce). The following certificate information applies to all worldwide and national cloud instances of Office 365.</span></span>
  

|<span data-ttu-id="27423-111">**Tipo de certificado**</span><span class="sxs-lookup"><span data-stu-id="27423-111">**Certificate type**</span></span>|<span data-ttu-id="27423-112">**P7b download**</span><span class="sxs-lookup"><span data-stu-id="27423-112">**P7b download**</span></span>|<span data-ttu-id="27423-113">**Pontos de extremidade da lista de certificados Revogados**</span><span class="sxs-lookup"><span data-stu-id="27423-113">**CRL Endpoints**</span></span>|<span data-ttu-id="27423-114">**Pontos de extremidade OCSP**</span><span class="sxs-lookup"><span data-stu-id="27423-114">**OCSP Endpoints**</span></span>|<span data-ttu-id="27423-115">**Pontos de extremidade AIA**</span><span class="sxs-lookup"><span data-stu-id="27423-115">**AIA Endpoints**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="27423-116">Certificados raiz de publicamente confiáveis</span><span class="sxs-lookup"><span data-stu-id="27423-116">Publicly Trusted Root Certificates</span></span>](https://support.office.com/article/0c03e6b3-e73f-4316-9e2b-bf4091ae96bb#rootcerts) <br/> |[<span data-ttu-id="27423-117">Pacote de certificado raiz do Office 365 (P7B)</span><span class="sxs-lookup"><span data-stu-id="27423-117">Office 365 Root Certificate Bundle (P7B)</span></span>](http://download.microsoft.com/download/A/5/A/A5AE01F3-D19B-4A11-9407-801263CEF72C/O365_Root_Certs_20170321.p7b) <br/> |<span data-ttu-id="27423-118">CRL.GlobalSign.NET</span><span class="sxs-lookup"><span data-stu-id="27423-118">crl.globalsign.net</span></span>  <br/> <span data-ttu-id="27423-119">www.d-Trust.NET</span><span class="sxs-lookup"><span data-stu-id="27423-119">www.d-trust.net</span></span>  <br/> |<span data-ttu-id="27423-120">N/D</span><span class="sxs-lookup"><span data-stu-id="27423-120">N/A</span></span>  <br/> |<span data-ttu-id="27423-121">N/D</span><span class="sxs-lookup"><span data-stu-id="27423-121">N/A</span></span>  <br/> |
|[<span data-ttu-id="27423-122">Publicamente confiáveis certificados intermediários</span><span class="sxs-lookup"><span data-stu-id="27423-122">Publicly Trusted Intermediate Certificates</span></span>](https://support.office.com/article/0c03e6b3-e73f-4316-9e2b-bf4091ae96bb#IntermediateCerts) <br/> |[<span data-ttu-id="27423-123">Pacote do Office 365 intermediário de certificado (P7B)</span><span class="sxs-lookup"><span data-stu-id="27423-123">Office 365 Intermediate Certificate Bundle (P7B)</span></span>](http://download.microsoft.com/download/4/D/5/4D5339A4-0A4A-46AB-AE52-B179DEDA4BEC/O365_Intermediate_Certs_20170321.p7b)  <br/> |<span data-ttu-id="27423-124">cdp1.Public-trust.com</span><span class="sxs-lookup"><span data-stu-id="27423-124">cdp1.public-trust.com</span></span>  <br/> <span data-ttu-id="27423-125">CRL.cnnic.CN</span><span class="sxs-lookup"><span data-stu-id="27423-125">crl.cnnic.cn</span></span>  <br/> <span data-ttu-id="27423-126">CRL.Entrust.NET</span><span class="sxs-lookup"><span data-stu-id="27423-126">crl.entrust.net</span></span>  <br/> <span data-ttu-id="27423-127">CRL.GlobalSign.com</span><span class="sxs-lookup"><span data-stu-id="27423-127">crl.globalsign.com</span></span>  <br/> <span data-ttu-id="27423-128">CRL.GlobalSign.NET</span><span class="sxs-lookup"><span data-stu-id="27423-128">crl.globalsign.net</span></span>  <br/> <span data-ttu-id="27423-129">CRL.identrust.com</span><span class="sxs-lookup"><span data-stu-id="27423-129">crl.identrust.com</span></span>  <br/> <span data-ttu-id="27423-130">CRL.Thawte.com</span><span class="sxs-lookup"><span data-stu-id="27423-130">crl.thawte.com</span></span>  <br/> <span data-ttu-id="27423-131">crl3.digicert.com</span><span class="sxs-lookup"><span data-stu-id="27423-131">crl3.digicert.com</span></span>  <br/> <span data-ttu-id="27423-132">crl4.digicert.com</span><span class="sxs-lookup"><span data-stu-id="27423-132">crl4.digicert.com</span></span>  <br/> <span data-ttu-id="27423-133">S1.symcb.com</span><span class="sxs-lookup"><span data-stu-id="27423-133">s1.symcb.com</span></span>  <br/> <span data-ttu-id="27423-134">www.d-Trust.NET</span><span class="sxs-lookup"><span data-stu-id="27423-134">www.d-trust.net</span></span>  <br/> |<span data-ttu-id="27423-135">isrg.trustid.OCSP.identrust.com</span><span class="sxs-lookup"><span data-stu-id="27423-135">isrg.trustid.ocsp.identrust.com</span></span>  <br/> <span data-ttu-id="27423-136">OCSP.digicert.com</span><span class="sxs-lookup"><span data-stu-id="27423-136">ocsp.digicert.com</span></span>  <br/> <span data-ttu-id="27423-137">OCSP.Entrust.NET</span><span class="sxs-lookup"><span data-stu-id="27423-137">ocsp.entrust.net</span></span>  <br/> <span data-ttu-id="27423-138">OCSP.GlobalSign.com</span><span class="sxs-lookup"><span data-stu-id="27423-138">ocsp.globalsign.com</span></span>  <br/> <span data-ttu-id="27423-139">OCSP.omniroot.com</span><span class="sxs-lookup"><span data-stu-id="27423-139">ocsp.omniroot.com</span></span>  <br/> <span data-ttu-id="27423-140">OCSP.startssl.com</span><span class="sxs-lookup"><span data-stu-id="27423-140">ocsp.startssl.com</span></span>  <br/> <span data-ttu-id="27423-141">OCSP.Thawte.com</span><span class="sxs-lookup"><span data-stu-id="27423-141">ocsp.thawte.com</span></span>  <br/> <span data-ttu-id="27423-142">ocsp2.GlobalSign.com</span><span class="sxs-lookup"><span data-stu-id="27423-142">ocsp2.globalsign.com</span></span>  <br/> <span data-ttu-id="27423-143">ocspcnnicroot.cnnic.CN</span><span class="sxs-lookup"><span data-stu-id="27423-143">ocspcnnicroot.cnnic.cn</span></span>  <br/> <span data-ttu-id="27423-144">raiz-c3-ca2-2009.ocsp.d-trust.net</span><span class="sxs-lookup"><span data-stu-id="27423-144">root-c3-ca2-2009.ocsp.d-trust.net</span></span>  <br/> <span data-ttu-id="27423-145">root-C3-ca2-EV-2009.OCSP.d-Trust.NET</span><span class="sxs-lookup"><span data-stu-id="27423-145">root-c3-ca2-ev-2009.ocsp.d-trust.net</span></span>  <br/> <span data-ttu-id="27423-146">S2.symcb.com</span><span class="sxs-lookup"><span data-stu-id="27423-146">s2.symcb.com</span></span>  <br/> |<span data-ttu-id="27423-147">AIA.startssl.com</span><span class="sxs-lookup"><span data-stu-id="27423-147">aia.startssl.com</span></span>  <br/> <span data-ttu-id="27423-148">Apps.identrust.com</span><span class="sxs-lookup"><span data-stu-id="27423-148">apps.identrust.com</span></span>  <br/> <span data-ttu-id="27423-149">cacert.omniroot.com</span><span class="sxs-lookup"><span data-stu-id="27423-149">cacert.omniroot.com</span></span>  <br/> <span data-ttu-id="27423-150">www.cnnic.CN</span><span class="sxs-lookup"><span data-stu-id="27423-150">www.cnnic.cn</span></span>  <br/> |
   
<span data-ttu-id="27423-151">Expanda a raiz e intermediárias seções abaixo para ver detalhes adicionais sobre os provedores de certificado.</span><span class="sxs-lookup"><span data-stu-id="27423-151">Expand the root and intermediate sections below to see additional details about the certificate providers.</span></span>
  
## <a name="office-365-root-certificate-details"></a><span data-ttu-id="27423-152">O Office 365 detalhes do certificado raiz</span><span class="sxs-lookup"><span data-stu-id="27423-152">Office 365 Root Certificate Details</span></span>
<span data-ttu-id="27423-153"><a name="RootCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="27423-153"></span></span>

 <span data-ttu-id="27423-154">**Baltimore CyberTrust Root**</span><span class="sxs-lookup"><span data-stu-id="27423-154">**Baltimore CyberTrust Root**</span></span>
  
<span data-ttu-id="27423-155">|:-----|</span><span class="sxs-lookup"><span data-stu-id="27423-155">|:-----|</span></span>
|<span data-ttu-id="27423-156">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-156">**Subject**</span></span>|
|:-----|
|<span data-ttu-id="27423-157">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="27423-157">**Serial Number**</span></span>|
|<span data-ttu-id="27423-158">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-158"></span></span>|
|<span data-ttu-id="27423-159">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="27423-159">**Public Key Length**</span></span>|
|<span data-ttu-id="27423-160">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-160"></span></span>|
|<span data-ttu-id="27423-161">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="27423-161">**Signature Algorithm**</span></span>|
|<span data-ttu-id="27423-162">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-162"></span></span>|
|<span data-ttu-id="27423-163">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="27423-163">**Validity Not Before**</span></span>|
|<span data-ttu-id="27423-164">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-164"></span></span>|
|<span data-ttu-id="27423-165">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="27423-165">**Validity Not After**</span></span>|
|<span data-ttu-id="27423-166">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-166"></span></span>|
|<span data-ttu-id="27423-167">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-167">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="27423-168">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-168"></span></span>|
|<span data-ttu-id="27423-169">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="27423-169">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="27423-170">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-170"></span></span>|
|<span data-ttu-id="27423-171">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-171">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="27423-172">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-172"></span></span>|
|<span data-ttu-id="27423-173">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-173">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="27423-174">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-174"></span></span>|
   
 <span data-ttu-id="27423-175">**RAIZ CNNIC**</span><span class="sxs-lookup"><span data-stu-id="27423-175">**CNNIC ROOT**</span></span>
  
||
|:-----|
|<span data-ttu-id="27423-176">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-176">**Subject**</span></span>|
|<span data-ttu-id="27423-177">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-177"></span></span>|
|<span data-ttu-id="27423-178">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="27423-178">**Serial Number**</span></span>|
|<span data-ttu-id="27423-179">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-179"></span></span>|
|<span data-ttu-id="27423-180">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="27423-180">**Public Key Length**</span></span>|
|<span data-ttu-id="27423-181">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-181"></span></span>|
|<span data-ttu-id="27423-182">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="27423-182">**Signature Algorithm**</span></span>|
|<span data-ttu-id="27423-183">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-183"></span></span>|
|<span data-ttu-id="27423-184">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="27423-184">**Validity Not Before**</span></span>|
|<span data-ttu-id="27423-185">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-185"></span></span>|
|<span data-ttu-id="27423-186">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="27423-186">**Validity Not After**</span></span>|
|<span data-ttu-id="27423-187">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-187"></span></span>|
|<span data-ttu-id="27423-188">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-188">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="27423-189">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-189"></span></span>|
|<span data-ttu-id="27423-190">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="27423-190">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="27423-191">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-191"></span></span>|
|<span data-ttu-id="27423-192">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="27423-192">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="27423-193">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-193"></span></span>|
|<span data-ttu-id="27423-194">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-194">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="27423-195">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-195"></span></span>|
|<span data-ttu-id="27423-196">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-196">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="27423-197">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-197"></span></span>|
   
 <span data-ttu-id="27423-198">**CA de raiz Global DigiCert**</span><span class="sxs-lookup"><span data-stu-id="27423-198">**DigiCert Global Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="27423-199">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-199">**Subject**</span></span>|
|<span data-ttu-id="27423-200">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-200"></span></span>|
|<span data-ttu-id="27423-201">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="27423-201">**Serial Number**</span></span>|
|<span data-ttu-id="27423-202">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-202"></span></span>|
|<span data-ttu-id="27423-203">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="27423-203">**Public Key Length**</span></span>|
|<span data-ttu-id="27423-204">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-204"></span></span>|
|<span data-ttu-id="27423-205">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="27423-205">**Signature Algorithm**</span></span>|
|<span data-ttu-id="27423-206">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-206"></span></span>|
|<span data-ttu-id="27423-207">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="27423-207">**Validity Not Before**</span></span>|
|<span data-ttu-id="27423-208">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-208"></span></span>|
|<span data-ttu-id="27423-209">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="27423-209">**Validity Not After**</span></span>|
|<span data-ttu-id="27423-210">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-210"></span></span>|
|<span data-ttu-id="27423-211">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-211">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="27423-212">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-212"></span></span>|
|<span data-ttu-id="27423-213">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="27423-213">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="27423-214">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-214"></span></span>|
|<span data-ttu-id="27423-215">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="27423-215">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="27423-216">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-216"></span></span>|
|<span data-ttu-id="27423-217">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-217">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="27423-218">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-218"></span></span>|
|<span data-ttu-id="27423-219">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-219">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="27423-220">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-220"></span></span>|
   
 <span data-ttu-id="27423-221">**Autoridade de certificação de raiz de garantia EV alta DigiCert**</span><span class="sxs-lookup"><span data-stu-id="27423-221">**DigiCert High Assurance EV Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="27423-222">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-222">**Subject**</span></span>|
|<span data-ttu-id="27423-223">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-223"></span></span>|
|<span data-ttu-id="27423-224">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="27423-224">**Serial Number**</span></span>|
|<span data-ttu-id="27423-225">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-225"></span></span>|
|<span data-ttu-id="27423-226">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="27423-226">**Public Key Length**</span></span>|
|<span data-ttu-id="27423-227">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-227"></span></span>|
|<span data-ttu-id="27423-228">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="27423-228">**Signature Algorithm**</span></span>|
|<span data-ttu-id="27423-229">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-229"></span></span>|
|<span data-ttu-id="27423-230">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="27423-230">**Validity Not Before**</span></span>|
|<span data-ttu-id="27423-231">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-231"></span></span>|
|<span data-ttu-id="27423-232">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="27423-232">**Validity Not After**</span></span>|
|<span data-ttu-id="27423-233">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-233"></span></span>|
|<span data-ttu-id="27423-234">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-234">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="27423-235">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-235"></span></span>|
|<span data-ttu-id="27423-236">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="27423-236">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="27423-237">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-237"></span></span>|
|<span data-ttu-id="27423-238">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="27423-238">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="27423-239">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-239"></span></span>|
|<span data-ttu-id="27423-240">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-240">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="27423-241">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-241"></span></span>|
|<span data-ttu-id="27423-242">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-242">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="27423-243">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-243"></span></span>|
   
 <span data-ttu-id="27423-244">**Autoridade de certificação da classe 3 de raiz de confiança D 2 de 2009**</span><span class="sxs-lookup"><span data-stu-id="27423-244">**D-TRUST Root Class 3 CA 2 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="27423-245">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-245">**Subject**</span></span>|
|<span data-ttu-id="27423-246">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-246"></span></span>|
|<span data-ttu-id="27423-247">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="27423-247">**Serial Number**</span></span>|
|<span data-ttu-id="27423-248">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-248"></span></span>|
|<span data-ttu-id="27423-249">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="27423-249">**Public Key Length**</span></span>|
|<span data-ttu-id="27423-250">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-250"></span></span>|
|<span data-ttu-id="27423-251">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="27423-251">**Signature Algorithm**</span></span>|
|<span data-ttu-id="27423-252">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-252"></span></span>|
|<span data-ttu-id="27423-253">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="27423-253">**Validity Not Before**</span></span>|
|<span data-ttu-id="27423-254">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-254"></span></span>|
|<span data-ttu-id="27423-255">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="27423-255">**Validity Not After**</span></span>|
|<span data-ttu-id="27423-256">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-256"></span></span>|
|<span data-ttu-id="27423-257">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-257">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="27423-258">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-258"></span></span>|
|<span data-ttu-id="27423-259">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="27423-259">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="27423-260">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-260"></span></span>|
|<span data-ttu-id="27423-261">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-261">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="27423-262">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-262"></span></span>|
|<span data-ttu-id="27423-263">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-263">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="27423-264">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-264"></span></span>|
|<span data-ttu-id="27423-265">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="27423-265">**CRL URLs**</span></span>|
|<span data-ttu-id="27423-266">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-266"></span></span>|
   
 <span data-ttu-id="27423-267">**Autoridade de certificação raiz confiável D classe 3 2 EV de 2009**</span><span class="sxs-lookup"><span data-stu-id="27423-267">**D-TRUST Root Class 3 CA 2 EV 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="27423-268">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-268">**Subject**</span></span>|
|<span data-ttu-id="27423-269">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-269"></span></span>|
|<span data-ttu-id="27423-270">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="27423-270">**Serial Number**</span></span>|
|<span data-ttu-id="27423-271">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-271"></span></span>|
|<span data-ttu-id="27423-272">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="27423-272">**Public Key Length**</span></span>|
|<span data-ttu-id="27423-273">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-273"></span></span>|
|<span data-ttu-id="27423-274">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="27423-274">**Signature Algorithm**</span></span>|
|<span data-ttu-id="27423-275">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-275"></span></span>|
|<span data-ttu-id="27423-276">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="27423-276">**Validity Not Before**</span></span>|
|<span data-ttu-id="27423-277">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-277"></span></span>|
|<span data-ttu-id="27423-278">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="27423-278">**Validity Not After**</span></span>|
|<span data-ttu-id="27423-279">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-279"></span></span>|
|<span data-ttu-id="27423-280">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-280">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="27423-281">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-281"></span></span>|
|<span data-ttu-id="27423-282">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="27423-282">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="27423-283">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-283"></span></span>|
|<span data-ttu-id="27423-284">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-284">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="27423-285">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-285"></span></span>|
|<span data-ttu-id="27423-286">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-286">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="27423-287">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-287"></span></span>|
|<span data-ttu-id="27423-288">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="27423-288">**CRL URLs**</span></span>|
|<span data-ttu-id="27423-289">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-289"></span></span>|
   
 <span data-ttu-id="27423-290">**Horário de verão raiz da autoridade de certificação X3**</span><span class="sxs-lookup"><span data-stu-id="27423-290">**DST Root CA X3**</span></span>
  
||
|:-----|
|<span data-ttu-id="27423-291">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-291">**Subject**</span></span>|
|<span data-ttu-id="27423-292">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-292"></span></span>|
|<span data-ttu-id="27423-293">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="27423-293">**Serial Number**</span></span>|
|<span data-ttu-id="27423-294">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-294"></span></span>|
|<span data-ttu-id="27423-295">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="27423-295">**Public Key Length**</span></span>|
|<span data-ttu-id="27423-296">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-296"></span></span>|
|<span data-ttu-id="27423-297">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="27423-297">**Signature Algorithm**</span></span>|
|<span data-ttu-id="27423-298">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-298"></span></span>|
|<span data-ttu-id="27423-299">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="27423-299">**Validity Not Before**</span></span>|
|<span data-ttu-id="27423-300">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-300"></span></span>|
|<span data-ttu-id="27423-301">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="27423-301">**Validity Not After**</span></span>|
|<span data-ttu-id="27423-302">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-302"></span></span>|
|<span data-ttu-id="27423-303">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-303">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="27423-304">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-304"></span></span>|
|<span data-ttu-id="27423-305">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="27423-305">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="27423-306">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-306"></span></span>|
|<span data-ttu-id="27423-307">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-307">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="27423-308">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-308"></span></span>|
|<span data-ttu-id="27423-309">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-309">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="27423-310">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-310"></span></span>|
   
 <span data-ttu-id="27423-311">**Entrust autoridade de certificação raiz - G2**</span><span class="sxs-lookup"><span data-stu-id="27423-311">**Entrust Root Certification Authority - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="27423-312">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-312">**Subject**</span></span>|
|<span data-ttu-id="27423-313">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-313"></span></span>|
|<span data-ttu-id="27423-314">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="27423-314">**Serial Number**</span></span>|
|<span data-ttu-id="27423-315">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-315"></span></span>|
|<span data-ttu-id="27423-316">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="27423-316">**Public Key Length**</span></span>|
|<span data-ttu-id="27423-317">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-317"></span></span>|
|<span data-ttu-id="27423-318">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="27423-318">**Signature Algorithm**</span></span>|
|<span data-ttu-id="27423-319">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-319"></span></span>|
|<span data-ttu-id="27423-320">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="27423-320">**Validity Not Before**</span></span>|
|<span data-ttu-id="27423-321">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-321"></span></span>|
|<span data-ttu-id="27423-322">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="27423-322">**Validity Not After**</span></span>|
|<span data-ttu-id="27423-323">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-323"></span></span>|
|<span data-ttu-id="27423-324">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-324">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="27423-325">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-325"></span></span>|
|<span data-ttu-id="27423-326">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="27423-326">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="27423-327">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-327"></span></span>|
|<span data-ttu-id="27423-328">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-328">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="27423-329">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-329"></span></span>|
|<span data-ttu-id="27423-330">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-330">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="27423-331">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-331"></span></span>|
   
 <span data-ttu-id="27423-332">**Entrust.net Certification Authority (2048)**</span><span class="sxs-lookup"><span data-stu-id="27423-332">**Entrust.net Certification Authority (2048)**</span></span>
  
||
|:-----|
|<span data-ttu-id="27423-333">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-333">**Subject**</span></span>|
|<span data-ttu-id="27423-334">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-334"></span></span>|
|<span data-ttu-id="27423-335">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="27423-335">**Serial Number**</span></span>|
|<span data-ttu-id="27423-336">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-336"></span></span>|
|<span data-ttu-id="27423-337">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="27423-337">**Public Key Length**</span></span>|
|<span data-ttu-id="27423-338">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-338"></span></span>|
|<span data-ttu-id="27423-339">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="27423-339">**Signature Algorithm**</span></span>|
|<span data-ttu-id="27423-340">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-340"></span></span>|
|<span data-ttu-id="27423-341">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="27423-341">**Validity Not Before**</span></span>|
|<span data-ttu-id="27423-342">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-342"></span></span>|
|<span data-ttu-id="27423-343">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="27423-343">**Validity Not After**</span></span>|
|<span data-ttu-id="27423-344">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-344"></span></span>|
|<span data-ttu-id="27423-345">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-345">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="27423-346">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-346"></span></span>|
|<span data-ttu-id="27423-347">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="27423-347">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="27423-348">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-348"></span></span>|
|<span data-ttu-id="27423-349">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-349">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="27423-350">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-350"></span></span>|
|<span data-ttu-id="27423-351">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-351">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="27423-352">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-352"></span></span>|
   
 <span data-ttu-id="27423-353">**GlobalSign**</span><span class="sxs-lookup"><span data-stu-id="27423-353">**GlobalSign**</span></span>
  
||
|:-----|
|<span data-ttu-id="27423-354">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-354">**Subject**</span></span>|
|<span data-ttu-id="27423-355">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-355"></span></span>|
|<span data-ttu-id="27423-356">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="27423-356">**Serial Number**</span></span>|
|<span data-ttu-id="27423-357">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-357"></span></span>|
|<span data-ttu-id="27423-358">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="27423-358">**Public Key Length**</span></span>|
|<span data-ttu-id="27423-359">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-359"></span></span>|
|<span data-ttu-id="27423-360">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="27423-360">**Signature Algorithm**</span></span>|
|<span data-ttu-id="27423-361">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-361"></span></span>|
|<span data-ttu-id="27423-362">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="27423-362">**Validity Not Before**</span></span>|
|<span data-ttu-id="27423-363">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-363"></span></span>|
|<span data-ttu-id="27423-364">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="27423-364">**Validity Not After**</span></span>|
|<span data-ttu-id="27423-365">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-365"></span></span>|
|<span data-ttu-id="27423-366">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-366">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="27423-367">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-367"></span></span>|
|<span data-ttu-id="27423-368">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="27423-368">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="27423-369">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-369"></span></span>|
|<span data-ttu-id="27423-370">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="27423-370">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="27423-371">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-371"></span></span>|
|<span data-ttu-id="27423-372">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-372">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="27423-373">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-373"></span></span>|
|<span data-ttu-id="27423-374">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-374">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="27423-375">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-375"></span></span>|
|<span data-ttu-id="27423-376">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="27423-376">**CRL URLs**</span></span>|
|<span data-ttu-id="27423-377">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-377"></span></span>|
   
 <span data-ttu-id="27423-378">**GlobalSign Root CA**</span><span class="sxs-lookup"><span data-stu-id="27423-378">**GlobalSign Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="27423-379">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-379">**Subject**</span></span>|
|<span data-ttu-id="27423-380">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-380"></span></span>|
|<span data-ttu-id="27423-381">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="27423-381">**Serial Number**</span></span>|
|<span data-ttu-id="27423-382">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-382"></span></span>|
|<span data-ttu-id="27423-383">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="27423-383">**Public Key Length**</span></span>|
|<span data-ttu-id="27423-384">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-384"></span></span>|
|<span data-ttu-id="27423-385">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="27423-385">**Signature Algorithm**</span></span>|
|<span data-ttu-id="27423-386">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-386"></span></span>|
|<span data-ttu-id="27423-387">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="27423-387">**Validity Not Before**</span></span>|
|<span data-ttu-id="27423-388">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-388"></span></span>|
|<span data-ttu-id="27423-389">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="27423-389">**Validity Not After**</span></span>|
|<span data-ttu-id="27423-390">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-390"></span></span>|
|<span data-ttu-id="27423-391">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-391">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="27423-392">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-392"></span></span>|
|<span data-ttu-id="27423-393">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="27423-393">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="27423-394">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-394"></span></span>|
|<span data-ttu-id="27423-395">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-395">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="27423-396">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-396"></span></span>|
|<span data-ttu-id="27423-397">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-397">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="27423-398">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-398"></span></span>|
   
 <span data-ttu-id="27423-399">**Thawte autoridade de certificação raiz primária - G3**</span><span class="sxs-lookup"><span data-stu-id="27423-399">**thawte Primary Root CA - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="27423-400">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-400">**Subject**</span></span>|
|<span data-ttu-id="27423-401">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-401"></span></span>|
|<span data-ttu-id="27423-402">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="27423-402">**Serial Number**</span></span>|
|<span data-ttu-id="27423-403">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-403"></span></span>|
|<span data-ttu-id="27423-404">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="27423-404">**Public Key Length**</span></span>|
|<span data-ttu-id="27423-405">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-405"></span></span>|
|<span data-ttu-id="27423-406">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="27423-406">**Signature Algorithm**</span></span>|
|<span data-ttu-id="27423-407">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-407"></span></span>|
|<span data-ttu-id="27423-408">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="27423-408">**Validity Not Before**</span></span>|
|<span data-ttu-id="27423-409">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-409"></span></span>|
|<span data-ttu-id="27423-410">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="27423-410">**Validity Not After**</span></span>|
|<span data-ttu-id="27423-411">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-411"></span></span>|
|<span data-ttu-id="27423-412">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-412">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="27423-413">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-413"></span></span>|
|<span data-ttu-id="27423-414">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="27423-414">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="27423-415">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-415"></span></span>|
|<span data-ttu-id="27423-416">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-416">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="27423-417">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-417"></span></span>|
|<span data-ttu-id="27423-418">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-418">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="27423-419">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-419"></span></span>|
   
 <span data-ttu-id="27423-420">**Autoridade de certificação principal pública classe VeriSign 3 - G5**</span><span class="sxs-lookup"><span data-stu-id="27423-420">**VeriSign Class 3 Public Primary Certification Authority - G5**</span></span>
  
||
|:-----|
|<span data-ttu-id="27423-421">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-421">**Subject**</span></span>|
|<span data-ttu-id="27423-422">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-422"></span></span>|
|<span data-ttu-id="27423-423">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="27423-423">**Serial Number**</span></span>|
|<span data-ttu-id="27423-424">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-424"></span></span>|
|<span data-ttu-id="27423-425">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="27423-425">**Public Key Length**</span></span>|
|<span data-ttu-id="27423-426">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-426"></span></span>|
|<span data-ttu-id="27423-427">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="27423-427">**Signature Algorithm**</span></span>|
|<span data-ttu-id="27423-428">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-428"></span></span>|
|<span data-ttu-id="27423-429">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="27423-429">**Validity Not Before**</span></span>|
|<span data-ttu-id="27423-430">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-430"></span></span>|
|<span data-ttu-id="27423-431">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="27423-431">**Validity Not After**</span></span>|
|<span data-ttu-id="27423-432">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-432"></span></span>|
|<span data-ttu-id="27423-433">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-433">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="27423-434">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-434"></span></span>|
|<span data-ttu-id="27423-435">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="27423-435">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="27423-436">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-436"></span></span>|
|<span data-ttu-id="27423-437">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-437">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="27423-438">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-438"></span></span>|
|<span data-ttu-id="27423-439">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-439">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="27423-440">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-440"></span></span>|
   
## <a name="office-365-intermediate-certificate-details"></a><span data-ttu-id="27423-441">Detalhes do certificado intermediário de Office 365</span><span class="sxs-lookup"><span data-stu-id="27423-441">Office 365 Intermediate Certificate Details</span></span>
<span data-ttu-id="27423-442"><a name="IntermediateCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="27423-442"></span></span>

 <span data-ttu-id="27423-443">**CNNIC SHA256 SSL**</span><span class="sxs-lookup"><span data-stu-id="27423-443">**CNNIC SHA256 SSL**</span></span>
  
||
|:-----|
|<span data-ttu-id="27423-444">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-444">**Subject**</span></span>|
|<span data-ttu-id="27423-445">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-445"></span></span>|
|<span data-ttu-id="27423-446">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="27423-446">**Issuer**</span></span>|
|<span data-ttu-id="27423-447">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-447"></span></span>|
|<span data-ttu-id="27423-448">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="27423-448">**Serial Number**</span></span>|
|<span data-ttu-id="27423-449">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-449"></span></span>|
|<span data-ttu-id="27423-450">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="27423-450">**Public Key Length**</span></span>|
|<span data-ttu-id="27423-451">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-451"></span></span>|
|<span data-ttu-id="27423-452">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="27423-452">**Signature Algorithm**</span></span>|
|<span data-ttu-id="27423-453">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-453"></span></span>|
|<span data-ttu-id="27423-454">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="27423-454">**Validity Not Before**</span></span>|
|<span data-ttu-id="27423-455">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-455"></span></span>|
|<span data-ttu-id="27423-456">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="27423-456">**Validity Not After**</span></span>|
|<span data-ttu-id="27423-457">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-457"></span></span>|
|<span data-ttu-id="27423-458">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-458">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="27423-459">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-459"></span></span>|
|<span data-ttu-id="27423-460">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="27423-460">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="27423-461">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-461"></span></span>|
|<span data-ttu-id="27423-462">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="27423-462">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="27423-463">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-463"></span></span>|
|<span data-ttu-id="27423-464">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-464">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="27423-465">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-465"></span></span>|
|<span data-ttu-id="27423-466">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-466">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="27423-467">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-467"></span></span>|
|<span data-ttu-id="27423-468">**URLs AIA**</span><span class="sxs-lookup"><span data-stu-id="27423-468">**AIA URLs**</span></span>|
|<span data-ttu-id="27423-469">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-469"></span></span>|
|<span data-ttu-id="27423-470">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="27423-470">**CRL URLs**</span></span>|
|<span data-ttu-id="27423-471">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-471"></span></span>|
|<span data-ttu-id="27423-472">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="27423-472">**OCSP URLs**</span></span>|
|<span data-ttu-id="27423-473">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-473"></span></span>|
   
 <span data-ttu-id="27423-474">**D-TRUST SSL classe 3 CA 1 2009**</span><span class="sxs-lookup"><span data-stu-id="27423-474">**D-TRUST SSL Class 3 CA 1 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="27423-475">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-475">**Subject**</span></span>|
|<span data-ttu-id="27423-476">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-476"></span></span>|
|<span data-ttu-id="27423-477">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="27423-477">**Issuer**</span></span>|
|<span data-ttu-id="27423-478">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-478"></span></span>|
|<span data-ttu-id="27423-479">**Nome alternativo da entidade**</span><span class="sxs-lookup"><span data-stu-id="27423-479">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="27423-480">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-480"></span></span>|
|<span data-ttu-id="27423-481">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="27423-481">**Serial Number**</span></span>|
|<span data-ttu-id="27423-482">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-482"></span></span>|
|<span data-ttu-id="27423-483">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="27423-483">**Public Key Length**</span></span>|
|<span data-ttu-id="27423-484">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-484"></span></span>|
|<span data-ttu-id="27423-485">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="27423-485">**Signature Algorithm**</span></span>|
|<span data-ttu-id="27423-486">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-486"></span></span>|
|<span data-ttu-id="27423-487">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="27423-487">**Validity Not Before**</span></span>|
|<span data-ttu-id="27423-488">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-488"></span></span>|
|<span data-ttu-id="27423-489">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="27423-489">**Validity Not After**</span></span>|
|<span data-ttu-id="27423-490">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-490"></span></span>|
|<span data-ttu-id="27423-491">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-491">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="27423-492">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-492"></span></span>|
|<span data-ttu-id="27423-493">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="27423-493">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="27423-494">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-494"></span></span>|
|<span data-ttu-id="27423-495">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="27423-495">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="27423-496">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-496"></span></span>|
|<span data-ttu-id="27423-497">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-497">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="27423-498">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-498"></span></span>|
|<span data-ttu-id="27423-499">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-499">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="27423-500">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-500"></span></span>|
|<span data-ttu-id="27423-501">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="27423-501">**CRL URLs**</span></span>|
|<span data-ttu-id="27423-502">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-502"></span></span>|
|<span data-ttu-id="27423-503">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="27423-503">**OCSP URLs**</span></span>|
|<span data-ttu-id="27423-504">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-504"></span></span>|
   
 <span data-ttu-id="27423-505">**Autoridade de certificação confiável D SSL classe 3 1 EV de 2009**</span><span class="sxs-lookup"><span data-stu-id="27423-505">**D-TRUST SSL Class 3 CA 1 EV 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="27423-506">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-506">**Subject**</span></span>|
|<span data-ttu-id="27423-507">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-507"></span></span>|
|<span data-ttu-id="27423-508">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="27423-508">**Issuer**</span></span>|
|<span data-ttu-id="27423-509">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-509"></span></span>|
|<span data-ttu-id="27423-510">**Nome alternativo da entidade**</span><span class="sxs-lookup"><span data-stu-id="27423-510">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="27423-511">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-511"></span></span>|
|<span data-ttu-id="27423-512">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="27423-512">**Serial Number**</span></span>|
|<span data-ttu-id="27423-513">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-513"></span></span>|
|<span data-ttu-id="27423-514">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="27423-514">**Public Key Length**</span></span>|
|<span data-ttu-id="27423-515">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-515"></span></span>|
|<span data-ttu-id="27423-516">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="27423-516">**Signature Algorithm**</span></span>|
|<span data-ttu-id="27423-517">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-517"></span></span>|
|<span data-ttu-id="27423-518">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="27423-518">**Validity Not Before**</span></span>|
|<span data-ttu-id="27423-519">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-519"></span></span>|
|<span data-ttu-id="27423-520">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="27423-520">**Validity Not After**</span></span>|
|<span data-ttu-id="27423-521">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-521"></span></span>|
|<span data-ttu-id="27423-522">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-522">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="27423-523">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-523"></span></span>|
|<span data-ttu-id="27423-524">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="27423-524">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="27423-525">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-525"></span></span>|
|<span data-ttu-id="27423-526">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="27423-526">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="27423-527">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-527"></span></span>|
|<span data-ttu-id="27423-528">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-528">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="27423-529">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-529"></span></span>|
|<span data-ttu-id="27423-530">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-530">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="27423-531">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-531"></span></span>|
|<span data-ttu-id="27423-532">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="27423-532">**CRL URLs**</span></span>|
|<span data-ttu-id="27423-533">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-533"></span></span>|
|<span data-ttu-id="27423-534">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="27423-534">**OCSP URLs**</span></span>|
|<span data-ttu-id="27423-535">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-535"></span></span>|
   
 <span data-ttu-id="27423-536">**Serviços em nuvem de DigiCert CA-1**</span><span class="sxs-lookup"><span data-stu-id="27423-536">**DigiCert Cloud Services CA-1**</span></span>
  
||
|:-----|
|<span data-ttu-id="27423-537">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-537">**Subject**</span></span>|
|<span data-ttu-id="27423-538">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-538"></span></span>|
|<span data-ttu-id="27423-539">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="27423-539">**Issuer**</span></span>|
|<span data-ttu-id="27423-540">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-540"></span></span>|
|<span data-ttu-id="27423-541">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="27423-541">**Serial Number**</span></span>|
|<span data-ttu-id="27423-542">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-542"></span></span>|
|<span data-ttu-id="27423-543">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="27423-543">**Public Key Length**</span></span>|
|<span data-ttu-id="27423-544">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-544"></span></span>|
|<span data-ttu-id="27423-545">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="27423-545">**Signature Algorithm**</span></span>|
|<span data-ttu-id="27423-546">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-546"></span></span>|
|<span data-ttu-id="27423-547">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="27423-547">**Validity Not Before**</span></span>|
|<span data-ttu-id="27423-548">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-548"></span></span>|
|<span data-ttu-id="27423-549">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="27423-549">**Validity Not After**</span></span>|
|<span data-ttu-id="27423-550">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-550"></span></span>|
|<span data-ttu-id="27423-551">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-551">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="27423-552">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-552"></span></span>|
|<span data-ttu-id="27423-553">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="27423-553">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="27423-554">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-554"></span></span>|
|<span data-ttu-id="27423-555">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="27423-555">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="27423-556">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-556"></span></span>|
|<span data-ttu-id="27423-557">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-557">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="27423-558">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-558"></span></span>|
|<span data-ttu-id="27423-559">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-559">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="27423-560">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-560"></span></span>|
|<span data-ttu-id="27423-561">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="27423-561">**CRL URLs**</span></span>|
|<span data-ttu-id="27423-562">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-562"></span></span>|
|<span data-ttu-id="27423-563">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="27423-563">**OCSP URLs**</span></span>|
|<span data-ttu-id="27423-564">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-564"></span></span>|
   
 <span data-ttu-id="27423-565">**Servidor de alta garantia DigiCert SHA2 CA**</span><span class="sxs-lookup"><span data-stu-id="27423-565">**DigiCert SHA2 High Assurance Server CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="27423-566">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-566">**Subject**</span></span>|
|<span data-ttu-id="27423-567">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-567"></span></span>|
|<span data-ttu-id="27423-568">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="27423-568">**Issuer**</span></span>|
|<span data-ttu-id="27423-569">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-569"></span></span>|
|<span data-ttu-id="27423-570">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="27423-570">**Serial Number**</span></span>|
|<span data-ttu-id="27423-571">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-571"></span></span>|
|<span data-ttu-id="27423-572">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="27423-572">**Public Key Length**</span></span>|
|<span data-ttu-id="27423-573">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-573"></span></span>|
|<span data-ttu-id="27423-574">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="27423-574">**Signature Algorithm**</span></span>|
|<span data-ttu-id="27423-575">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-575"></span></span>|
|<span data-ttu-id="27423-576">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="27423-576">**Validity Not Before**</span></span>|
|<span data-ttu-id="27423-577">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-577"></span></span>|
|<span data-ttu-id="27423-578">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="27423-578">**Validity Not After**</span></span>|
|<span data-ttu-id="27423-579">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-579"></span></span>|
|<span data-ttu-id="27423-580">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-580">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="27423-581">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-581"></span></span>|
|<span data-ttu-id="27423-582">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="27423-582">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="27423-583">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-583"></span></span>|
|<span data-ttu-id="27423-584">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="27423-584">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="27423-585">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-585"></span></span>|
|<span data-ttu-id="27423-586">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-586">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="27423-587">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-587"></span></span>|
|<span data-ttu-id="27423-588">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-588">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="27423-589">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-589"></span></span>|
|<span data-ttu-id="27423-590">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="27423-590">**CRL URLs**</span></span>|
|<span data-ttu-id="27423-591">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-591"></span></span>|
|<span data-ttu-id="27423-592">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="27423-592">**OCSP URLs**</span></span>|
|<span data-ttu-id="27423-593">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-593"></span></span>|
   
 <span data-ttu-id="27423-594">**Servidores de seguros DigiCert SHA2 CA**</span><span class="sxs-lookup"><span data-stu-id="27423-594">**DigiCert SHA2 Secure Server CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="27423-595">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-595">**Subject**</span></span>|
|<span data-ttu-id="27423-596">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-596"></span></span>|
|<span data-ttu-id="27423-597">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="27423-597">**Issuer**</span></span>|
|<span data-ttu-id="27423-598">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-598"></span></span>|
|<span data-ttu-id="27423-599">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="27423-599">**Serial Number**</span></span>|
|<span data-ttu-id="27423-600">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-600"></span></span>|
|<span data-ttu-id="27423-601">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="27423-601">**Public Key Length**</span></span>|
|<span data-ttu-id="27423-602">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-602"></span></span>|
|<span data-ttu-id="27423-603">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="27423-603">**Signature Algorithm**</span></span>|
|<span data-ttu-id="27423-604">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-604"></span></span>|
|<span data-ttu-id="27423-605">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="27423-605">**Validity Not Before**</span></span>|
|<span data-ttu-id="27423-606">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-606"></span></span>|
|<span data-ttu-id="27423-607">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="27423-607">**Validity Not After**</span></span>|
|<span data-ttu-id="27423-608">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-608"></span></span>|
|<span data-ttu-id="27423-609">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-609">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="27423-610">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-610"></span></span>|
|<span data-ttu-id="27423-611">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="27423-611">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="27423-612">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-612"></span></span>|
|<span data-ttu-id="27423-613">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="27423-613">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="27423-614">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-614"></span></span>|
|<span data-ttu-id="27423-615">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-615">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="27423-616">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-616"></span></span>|
|<span data-ttu-id="27423-617">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-617">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="27423-618">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-618"></span></span>|
|<span data-ttu-id="27423-619">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="27423-619">**CRL URLs**</span></span>|
|<span data-ttu-id="27423-620">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-620"></span></span>|
|<span data-ttu-id="27423-621">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="27423-621">**OCSP URLs**</span></span>|
|<span data-ttu-id="27423-622">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-622"></span></span>|
   
 <span data-ttu-id="27423-623">**Entrust autoridade de certificação - L1C**</span><span class="sxs-lookup"><span data-stu-id="27423-623">**Entrust Certification Authority - L1C**</span></span>
  
||
|:-----|
|<span data-ttu-id="27423-624">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-624">**Subject**</span></span>|
|<span data-ttu-id="27423-625">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-625"></span></span>|
|<span data-ttu-id="27423-626">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="27423-626">**Issuer**</span></span>|
|<span data-ttu-id="27423-627">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-627"></span></span>|
|<span data-ttu-id="27423-628">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="27423-628">**Serial Number**</span></span>|
|<span data-ttu-id="27423-629">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-629"></span></span>|
|<span data-ttu-id="27423-630">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="27423-630">**Public Key Length**</span></span>|
|<span data-ttu-id="27423-631">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-631"></span></span>|
|<span data-ttu-id="27423-632">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="27423-632">**Signature Algorithm**</span></span>|
|<span data-ttu-id="27423-633">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-633"></span></span>|
|<span data-ttu-id="27423-634">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="27423-634">**Validity Not Before**</span></span>|
|<span data-ttu-id="27423-635">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-635"></span></span>|
|<span data-ttu-id="27423-636">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="27423-636">**Validity Not After**</span></span>|
|<span data-ttu-id="27423-637">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-637"></span></span>|
|<span data-ttu-id="27423-638">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-638">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="27423-639">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-639"></span></span>|
|<span data-ttu-id="27423-640">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="27423-640">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="27423-641">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-641"></span></span>|
|<span data-ttu-id="27423-642">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="27423-642">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="27423-643">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-643"></span></span>|
|<span data-ttu-id="27423-644">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-644">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="27423-645">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-645"></span></span>|
|<span data-ttu-id="27423-646">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-646">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="27423-647">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-647"></span></span>|
|<span data-ttu-id="27423-648">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="27423-648">**CRL URLs**</span></span>|
|<span data-ttu-id="27423-649">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-649"></span></span>|
|<span data-ttu-id="27423-650">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="27423-650">**OCSP URLs**</span></span>|
|<span data-ttu-id="27423-651">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-651"></span></span>|
   
 <span data-ttu-id="27423-652">**Entrust autoridade de certificação - L1K**</span><span class="sxs-lookup"><span data-stu-id="27423-652">**Entrust Certification Authority - L1K**</span></span>
  
||
|:-----|
|<span data-ttu-id="27423-653">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-653">**Subject**</span></span>|
|<span data-ttu-id="27423-654">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-654"></span></span>|
|<span data-ttu-id="27423-655">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="27423-655">**Issuer**</span></span>|
|<span data-ttu-id="27423-656">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-656"></span></span>|
|<span data-ttu-id="27423-657">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="27423-657">**Serial Number**</span></span>|
|<span data-ttu-id="27423-658">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-658"></span></span>|
|<span data-ttu-id="27423-659">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="27423-659">**Public Key Length**</span></span>|
|<span data-ttu-id="27423-660">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-660"></span></span>|
|<span data-ttu-id="27423-661">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="27423-661">**Signature Algorithm**</span></span>|
|<span data-ttu-id="27423-662">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-662"></span></span>|
|<span data-ttu-id="27423-663">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="27423-663">**Validity Not Before**</span></span>|
|<span data-ttu-id="27423-664">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-664"></span></span>|
|<span data-ttu-id="27423-665">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="27423-665">**Validity Not After**</span></span>|
|<span data-ttu-id="27423-666">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-666"></span></span>|
|<span data-ttu-id="27423-667">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-667">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="27423-668">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-668"></span></span>|
|<span data-ttu-id="27423-669">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="27423-669">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="27423-670">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-670"></span></span>|
|<span data-ttu-id="27423-671">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="27423-671">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="27423-672">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-672"></span></span>|
|<span data-ttu-id="27423-673">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-673">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="27423-674">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-674"></span></span>|
|<span data-ttu-id="27423-675">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-675">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="27423-676">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-676"></span></span>|
|<span data-ttu-id="27423-677">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="27423-677">**CRL URLs**</span></span>|
|<span data-ttu-id="27423-678">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-678"></span></span>|
|<span data-ttu-id="27423-679">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="27423-679">**OCSP URLs**</span></span>|
|<span data-ttu-id="27423-680">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-680"></span></span>|
   
 <span data-ttu-id="27423-681">**GlobalSign**</span><span class="sxs-lookup"><span data-stu-id="27423-681">**GlobalSign**</span></span>
  
||
|:-----|
|<span data-ttu-id="27423-682">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-682">**Subject**</span></span>|
|<span data-ttu-id="27423-683">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-683"></span></span>|
|<span data-ttu-id="27423-684">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="27423-684">**Issuer**</span></span>|
|<span data-ttu-id="27423-685">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-685"></span></span>|
|<span data-ttu-id="27423-686">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="27423-686">**Serial Number**</span></span>|
|<span data-ttu-id="27423-687">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-687"></span></span>|
|<span data-ttu-id="27423-688">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="27423-688">**Public Key Length**</span></span>|
|<span data-ttu-id="27423-689">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-689"></span></span>|
|<span data-ttu-id="27423-690">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="27423-690">**Signature Algorithm**</span></span>|
|<span data-ttu-id="27423-691">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-691"></span></span>|
|<span data-ttu-id="27423-692">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="27423-692">**Validity Not Before**</span></span>|
|<span data-ttu-id="27423-693">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-693"></span></span>|
|<span data-ttu-id="27423-694">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="27423-694">**Validity Not After**</span></span>|
|<span data-ttu-id="27423-695">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-695"></span></span>|
|<span data-ttu-id="27423-696">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-696">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="27423-697">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-697"></span></span>|
|<span data-ttu-id="27423-698">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="27423-698">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="27423-699">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-699"></span></span>|
|<span data-ttu-id="27423-700">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="27423-700">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="27423-701">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-701"></span></span>|
|<span data-ttu-id="27423-702">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-702">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="27423-703">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-703"></span></span>|
|<span data-ttu-id="27423-704">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-704">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="27423-705">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-705"></span></span>|
|<span data-ttu-id="27423-706">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="27423-706">**CRL URLs**</span></span>|
|<span data-ttu-id="27423-707">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-707"></span></span>|
|<span data-ttu-id="27423-708">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="27423-708">**OCSP URLs**</span></span>|
|<span data-ttu-id="27423-709">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-709"></span></span>|
   
 <span data-ttu-id="27423-710">**GlobalSign estendido validação CA - SHA256 - G2**</span><span class="sxs-lookup"><span data-stu-id="27423-710">**GlobalSign Extended Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="27423-711">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-711">**Subject**</span></span>|
|<span data-ttu-id="27423-712">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-712"></span></span>|
|<span data-ttu-id="27423-713">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="27423-713">**Issuer**</span></span>|
|<span data-ttu-id="27423-714">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-714"></span></span>|
|<span data-ttu-id="27423-715">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="27423-715">**Serial Number**</span></span>|
|<span data-ttu-id="27423-716">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-716"></span></span>|
|<span data-ttu-id="27423-717">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="27423-717">**Public Key Length**</span></span>|
|<span data-ttu-id="27423-718">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-718"></span></span>|
|<span data-ttu-id="27423-719">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="27423-719">**Signature Algorithm**</span></span>|
|<span data-ttu-id="27423-720">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-720"></span></span>|
|<span data-ttu-id="27423-721">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="27423-721">**Validity Not Before**</span></span>|
|<span data-ttu-id="27423-722">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-722"></span></span>|
|<span data-ttu-id="27423-723">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="27423-723">**Validity Not After**</span></span>|
|<span data-ttu-id="27423-724">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-724"></span></span>|
|<span data-ttu-id="27423-725">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-725">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="27423-726">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-726"></span></span>|
|<span data-ttu-id="27423-727">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="27423-727">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="27423-728">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-728"></span></span>|
|<span data-ttu-id="27423-729">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="27423-729">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="27423-730">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-730"></span></span>|
|<span data-ttu-id="27423-731">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-731">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="27423-732">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-732"></span></span>|
|<span data-ttu-id="27423-733">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-733">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="27423-734">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-734"></span></span>|
|<span data-ttu-id="27423-735">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="27423-735">**CRL URLs**</span></span>|
|<span data-ttu-id="27423-736">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-736"></span></span>|
|<span data-ttu-id="27423-737">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="27423-737">**OCSP URLs**</span></span>|
|<span data-ttu-id="27423-738">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-738"></span></span>|
   
 <span data-ttu-id="27423-739">**GlobalSign estendido validação CA - SHA256 - G3**</span><span class="sxs-lookup"><span data-stu-id="27423-739">**GlobalSign Extended Validation CA - SHA256 - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="27423-740">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-740">**Subject**</span></span>|
|<span data-ttu-id="27423-741">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-741"></span></span>|
|<span data-ttu-id="27423-742">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="27423-742">**Issuer**</span></span>|
|<span data-ttu-id="27423-743">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-743"></span></span>|
|<span data-ttu-id="27423-744">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="27423-744">**Serial Number**</span></span>|
|<span data-ttu-id="27423-745">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-745"></span></span>|
|<span data-ttu-id="27423-746">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="27423-746">**Public Key Length**</span></span>|
|<span data-ttu-id="27423-747">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-747"></span></span>|
|<span data-ttu-id="27423-748">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="27423-748">**Signature Algorithm**</span></span>|
|<span data-ttu-id="27423-749">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-749"></span></span>|
|<span data-ttu-id="27423-750">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="27423-750">**Validity Not Before**</span></span>|
|<span data-ttu-id="27423-751">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-751"></span></span>|
|<span data-ttu-id="27423-752">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="27423-752">**Validity Not After**</span></span>|
|<span data-ttu-id="27423-753">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-753"></span></span>|
|<span data-ttu-id="27423-754">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-754">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="27423-755">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-755"></span></span>|
|<span data-ttu-id="27423-756">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="27423-756">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="27423-757">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-757"></span></span>|
|<span data-ttu-id="27423-758">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="27423-758">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="27423-759">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-759"></span></span>|
|<span data-ttu-id="27423-760">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-760">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="27423-761">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-761"></span></span>|
|<span data-ttu-id="27423-762">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-762">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="27423-763">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-763"></span></span>|
|<span data-ttu-id="27423-764">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="27423-764">**CRL URLs**</span></span>|
|<span data-ttu-id="27423-765">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-765"></span></span>|
|<span data-ttu-id="27423-766">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="27423-766">**OCSP URLs**</span></span>|
|<span data-ttu-id="27423-767">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-767"></span></span>|
   
 <span data-ttu-id="27423-768">**GlobalSign organização validação CA - SHA256 - G2**</span><span class="sxs-lookup"><span data-stu-id="27423-768">**GlobalSign Organization Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="27423-769">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-769">**Subject**</span></span>|
|<span data-ttu-id="27423-770">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-770"></span></span>|
|<span data-ttu-id="27423-771">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="27423-771">**Issuer**</span></span>|
|<span data-ttu-id="27423-772">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-772"></span></span>|
|<span data-ttu-id="27423-773">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="27423-773">**Serial Number**</span></span>|
|<span data-ttu-id="27423-774">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-774"></span></span>|
|<span data-ttu-id="27423-775">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="27423-775">**Public Key Length**</span></span>|
|<span data-ttu-id="27423-776">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-776"></span></span>|
|<span data-ttu-id="27423-777">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="27423-777">**Signature Algorithm**</span></span>|
|<span data-ttu-id="27423-778">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-778"></span></span>|
|<span data-ttu-id="27423-779">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="27423-779">**Validity Not Before**</span></span>|
|<span data-ttu-id="27423-780">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-780"></span></span>|
|<span data-ttu-id="27423-781">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="27423-781">**Validity Not After**</span></span>|
|<span data-ttu-id="27423-782">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-782"></span></span>|
|<span data-ttu-id="27423-783">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-783">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="27423-784">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-784"></span></span>|
|<span data-ttu-id="27423-785">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="27423-785">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="27423-786">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-786"></span></span>|
|<span data-ttu-id="27423-787">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="27423-787">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="27423-788">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-788"></span></span>|
|<span data-ttu-id="27423-789">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-789">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="27423-790">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-790"></span></span>|
|<span data-ttu-id="27423-791">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-791">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="27423-792">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-792"></span></span>|
|<span data-ttu-id="27423-793">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="27423-793">**CRL URLs**</span></span>|
|<span data-ttu-id="27423-794">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-794"></span></span>|
|<span data-ttu-id="27423-795">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="27423-795">**OCSP URLs**</span></span>|
|<span data-ttu-id="27423-796">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-796"></span></span>|
   
 <span data-ttu-id="27423-797">**GlobalSign organização validação CA - SHA256 - G2**</span><span class="sxs-lookup"><span data-stu-id="27423-797">**GlobalSign Organization Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="27423-798">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-798">**Subject**</span></span>|
|<span data-ttu-id="27423-799">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-799"></span></span>|
|<span data-ttu-id="27423-800">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="27423-800">**Issuer**</span></span>|
|<span data-ttu-id="27423-801">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-801"></span></span>|
|<span data-ttu-id="27423-802">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="27423-802">**Serial Number**</span></span>|
|<span data-ttu-id="27423-803">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-803"></span></span>|
|<span data-ttu-id="27423-804">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="27423-804">**Public Key Length**</span></span>|
|<span data-ttu-id="27423-805">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-805"></span></span>|
|<span data-ttu-id="27423-806">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="27423-806">**Signature Algorithm**</span></span>|
|<span data-ttu-id="27423-807">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-807"></span></span>|
|<span data-ttu-id="27423-808">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="27423-808">**Validity Not Before**</span></span>|
|<span data-ttu-id="27423-809">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-809"></span></span>|
|<span data-ttu-id="27423-810">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="27423-810">**Validity Not After**</span></span>|
|<span data-ttu-id="27423-811">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-811"></span></span>|
|<span data-ttu-id="27423-812">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-812">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="27423-813">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-813"></span></span>|
|<span data-ttu-id="27423-814">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="27423-814">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="27423-815">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-815"></span></span>|
|<span data-ttu-id="27423-816">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="27423-816">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="27423-817">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-817"></span></span>|
|<span data-ttu-id="27423-818">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-818">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="27423-819">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-819"></span></span>|
|<span data-ttu-id="27423-820">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-820">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="27423-821">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-821"></span></span>|
|<span data-ttu-id="27423-822">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="27423-822">**CRL URLs**</span></span>|
|<span data-ttu-id="27423-823">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-823"></span></span>|
|<span data-ttu-id="27423-824">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="27423-824">**OCSP URLs**</span></span>|
|<span data-ttu-id="27423-825">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-825"></span></span>|
   
 <span data-ttu-id="27423-826">**Criptografar vamos autoridade X3**</span><span class="sxs-lookup"><span data-stu-id="27423-826">**Let's Encrypt Authority X3**</span></span>
  
||
|:-----|
|<span data-ttu-id="27423-827">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-827">**Subject**</span></span>|
|<span data-ttu-id="27423-828">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-828"></span></span>|
|<span data-ttu-id="27423-829">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="27423-829">**Issuer**</span></span>|
|<span data-ttu-id="27423-830">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-830"></span></span>|
|<span data-ttu-id="27423-831">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="27423-831">**Serial Number**</span></span>|
|<span data-ttu-id="27423-832">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-832"></span></span>|
|<span data-ttu-id="27423-833">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="27423-833">**Public Key Length**</span></span>|
|<span data-ttu-id="27423-834">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-834"></span></span>|
|<span data-ttu-id="27423-835">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="27423-835">**Signature Algorithm**</span></span>|
|<span data-ttu-id="27423-836">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-836"></span></span>|
|<span data-ttu-id="27423-837">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="27423-837">**Validity Not Before**</span></span>|
|<span data-ttu-id="27423-838">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-838"></span></span>|
|<span data-ttu-id="27423-839">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="27423-839">**Validity Not After**</span></span>|
|<span data-ttu-id="27423-840">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-840"></span></span>|
|<span data-ttu-id="27423-841">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-841">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="27423-842">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-842"></span></span>|
|<span data-ttu-id="27423-843">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="27423-843">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="27423-844">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-844"></span></span>|
|<span data-ttu-id="27423-845">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="27423-845">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="27423-846">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-846"></span></span>|
|<span data-ttu-id="27423-847">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-847">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="27423-848">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-848"></span></span>|
|<span data-ttu-id="27423-849">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-849">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="27423-850">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-850"></span></span>|
|<span data-ttu-id="27423-851">**URLs AIA**</span><span class="sxs-lookup"><span data-stu-id="27423-851">**AIA URLs**</span></span>|
|<span data-ttu-id="27423-852">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-852"></span></span>|
|<span data-ttu-id="27423-853">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="27423-853">**CRL URLs**</span></span>|
|<span data-ttu-id="27423-854">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-854"></span></span>|
|<span data-ttu-id="27423-855">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="27423-855">**OCSP URLs**</span></span>|
|<span data-ttu-id="27423-856">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-856"></span></span>|
   
 <span data-ttu-id="27423-857">**O TI da Microsoft SSL SHA2**</span><span class="sxs-lookup"><span data-stu-id="27423-857">**Microsoft IT SSL SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="27423-858">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-858">**Subject**</span></span>|
|<span data-ttu-id="27423-859">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-859"></span></span>|
|<span data-ttu-id="27423-860">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="27423-860">**Issuer**</span></span>|
|<span data-ttu-id="27423-861">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-861"></span></span>|
|<span data-ttu-id="27423-862">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="27423-862">**Serial Number**</span></span>|
|<span data-ttu-id="27423-863">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-863"></span></span>|
|<span data-ttu-id="27423-864">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="27423-864">**Public Key Length**</span></span>|
|<span data-ttu-id="27423-865">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-865"></span></span>|
|<span data-ttu-id="27423-866">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="27423-866">**Signature Algorithm**</span></span>|
|<span data-ttu-id="27423-867">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-867"></span></span>|
|<span data-ttu-id="27423-868">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="27423-868">**Validity Not Before**</span></span>|
|<span data-ttu-id="27423-869">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-869"></span></span>|
|<span data-ttu-id="27423-870">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="27423-870">**Validity Not After**</span></span>|
|<span data-ttu-id="27423-871">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-871"></span></span>|
|<span data-ttu-id="27423-872">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-872">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="27423-873">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-873"></span></span>|
|<span data-ttu-id="27423-874">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="27423-874">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="27423-875">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-875"></span></span>|
|<span data-ttu-id="27423-876">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="27423-876">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="27423-877">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-877"></span></span>|
|<span data-ttu-id="27423-878">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-878">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="27423-879">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-879"></span></span>|
|<span data-ttu-id="27423-880">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-880">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="27423-881">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-881"></span></span>|
|<span data-ttu-id="27423-882">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="27423-882">**CRL URLs**</span></span>|
|<span data-ttu-id="27423-883">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-883"></span></span>|
   
 <span data-ttu-id="27423-884">**O TI da Microsoft SSL SHA2**</span><span class="sxs-lookup"><span data-stu-id="27423-884">**Microsoft IT SSL SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="27423-885">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-885">**Subject**</span></span>|
|<span data-ttu-id="27423-886">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-886"></span></span>|
|<span data-ttu-id="27423-887">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="27423-887">**Issuer**</span></span>|
|<span data-ttu-id="27423-888">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-888"></span></span>|
|<span data-ttu-id="27423-889">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="27423-889">**Serial Number**</span></span>|
|<span data-ttu-id="27423-890">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-890"></span></span>|
|<span data-ttu-id="27423-891">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="27423-891">**Public Key Length**</span></span>|
|<span data-ttu-id="27423-892">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-892"></span></span>|
|<span data-ttu-id="27423-893">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="27423-893">**Signature Algorithm**</span></span>|
|<span data-ttu-id="27423-894">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-894"></span></span>|
|<span data-ttu-id="27423-895">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="27423-895">**Validity Not Before**</span></span>|
|<span data-ttu-id="27423-896">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-896"></span></span>|
|<span data-ttu-id="27423-897">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="27423-897">**Validity Not After**</span></span>|
|<span data-ttu-id="27423-898">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-898"></span></span>|
|<span data-ttu-id="27423-899">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-899">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="27423-900">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-900"></span></span>|
|<span data-ttu-id="27423-901">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="27423-901">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="27423-902">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-902"></span></span>|
|<span data-ttu-id="27423-903">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="27423-903">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="27423-904">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-904"></span></span>|
|<span data-ttu-id="27423-905">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-905">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="27423-906">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-906"></span></span>|
|<span data-ttu-id="27423-907">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-907">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="27423-908">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-908"></span></span>|
|<span data-ttu-id="27423-909">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="27423-909">**CRL URLs**</span></span>|
|<span data-ttu-id="27423-910">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-910"></span></span>|
|<span data-ttu-id="27423-911">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="27423-911">**OCSP URLs**</span></span>|
|<span data-ttu-id="27423-912">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-912"></span></span>|
   
 <span data-ttu-id="27423-913">**Autoridade de certificação do Microsoft IT TLS 1**</span><span class="sxs-lookup"><span data-stu-id="27423-913">**Microsoft IT TLS CA 1**</span></span>
  
||
|:-----|
|<span data-ttu-id="27423-914">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-914">**Subject**</span></span>|
|<span data-ttu-id="27423-915">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-915"></span></span>|
|<span data-ttu-id="27423-916">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="27423-916">**Issuer**</span></span>|
|<span data-ttu-id="27423-917">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-917"></span></span>|
|<span data-ttu-id="27423-918">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="27423-918">**Serial Number**</span></span>|
|<span data-ttu-id="27423-919">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-919"></span></span>|
|<span data-ttu-id="27423-920">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="27423-920">**Public Key Length**</span></span>|
|<span data-ttu-id="27423-921">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-921"></span></span>|
|<span data-ttu-id="27423-922">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="27423-922">**Signature Algorithm**</span></span>|
|<span data-ttu-id="27423-923">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-923"></span></span>|
|<span data-ttu-id="27423-924">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="27423-924">**Validity Not Before**</span></span>|
|<span data-ttu-id="27423-925">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-925"></span></span>|
|<span data-ttu-id="27423-926">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="27423-926">**Validity Not After**</span></span>|
|<span data-ttu-id="27423-927">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-927"></span></span>|
|<span data-ttu-id="27423-928">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-928">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="27423-929">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-929"></span></span>|
|<span data-ttu-id="27423-930">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="27423-930">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="27423-931">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-931"></span></span>|
|<span data-ttu-id="27423-932">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="27423-932">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="27423-933">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-933"></span></span>|
|<span data-ttu-id="27423-934">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-934">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="27423-935">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-935"></span></span>|
|<span data-ttu-id="27423-936">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-936">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="27423-937">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-937"></span></span>|
|<span data-ttu-id="27423-938">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="27423-938">**CRL URLs**</span></span>|
|<span data-ttu-id="27423-939">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-939"></span></span>|
|<span data-ttu-id="27423-940">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="27423-940">**OCSP URLs**</span></span>|
|<span data-ttu-id="27423-941">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-941"></span></span>|
   
 <span data-ttu-id="27423-942">**Autoridade de certificação do Microsoft IT TLS 2**</span><span class="sxs-lookup"><span data-stu-id="27423-942">**Microsoft IT TLS CA 2**</span></span>
  
||
|:-----|
|<span data-ttu-id="27423-943">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-943">**Subject**</span></span>|
|<span data-ttu-id="27423-944">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-944"></span></span>|
|<span data-ttu-id="27423-945">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="27423-945">**Issuer**</span></span>|
|<span data-ttu-id="27423-946">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-946"></span></span>|
|<span data-ttu-id="27423-947">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="27423-947">**Serial Number**</span></span>|
|<span data-ttu-id="27423-948">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-948"></span></span>|
|<span data-ttu-id="27423-949">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="27423-949">**Public Key Length**</span></span>|
|<span data-ttu-id="27423-950">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-950"></span></span>|
|<span data-ttu-id="27423-951">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="27423-951">**Signature Algorithm**</span></span>|
|<span data-ttu-id="27423-952">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-952"></span></span>|
|<span data-ttu-id="27423-953">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="27423-953">**Validity Not Before**</span></span>|
|<span data-ttu-id="27423-954">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-954"></span></span>|
|<span data-ttu-id="27423-955">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="27423-955">**Validity Not After**</span></span>|
|<span data-ttu-id="27423-956">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-956"></span></span>|
|<span data-ttu-id="27423-957">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-957">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="27423-958">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-958"></span></span>|
|<span data-ttu-id="27423-959">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="27423-959">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="27423-960">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-960"></span></span>|
|<span data-ttu-id="27423-961">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="27423-961">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="27423-962">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-962"></span></span>|
|<span data-ttu-id="27423-963">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-963">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="27423-964">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-964"></span></span>|
|<span data-ttu-id="27423-965">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-965">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="27423-966">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-966"></span></span>|
|<span data-ttu-id="27423-967">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="27423-967">**CRL URLs**</span></span>|
|<span data-ttu-id="27423-968">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-968"></span></span>|
|<span data-ttu-id="27423-969">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="27423-969">**OCSP URLs**</span></span>|
|<span data-ttu-id="27423-970">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-970"></span></span>|
   
 <span data-ttu-id="27423-971">**Autoridade de certificação do Microsoft IT TLS 4**</span><span class="sxs-lookup"><span data-stu-id="27423-971">**Microsoft IT TLS CA 4**</span></span>
  
||
|:-----|
|<span data-ttu-id="27423-972">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-972">**Subject**</span></span>|
|<span data-ttu-id="27423-973">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-973"></span></span>|
|<span data-ttu-id="27423-974">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="27423-974">**Issuer**</span></span>|
|<span data-ttu-id="27423-975">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-975"></span></span>|
|<span data-ttu-id="27423-976">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="27423-976">**Serial Number**</span></span>|
|<span data-ttu-id="27423-977">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-977"></span></span>|
|<span data-ttu-id="27423-978">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="27423-978">**Public Key Length**</span></span>|
|<span data-ttu-id="27423-979">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-979"></span></span>|
|<span data-ttu-id="27423-980">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="27423-980">**Signature Algorithm**</span></span>|
|<span data-ttu-id="27423-981">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-981"></span></span>|
|<span data-ttu-id="27423-982">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="27423-982">**Validity Not Before**</span></span>|
|<span data-ttu-id="27423-983">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-983"></span></span>|
|<span data-ttu-id="27423-984">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="27423-984">**Validity Not After**</span></span>|
|<span data-ttu-id="27423-985">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-985"></span></span>|
|<span data-ttu-id="27423-986">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-986">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="27423-987">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-987"></span></span>|
|<span data-ttu-id="27423-988">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="27423-988">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="27423-989">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-989"></span></span>|
|<span data-ttu-id="27423-990">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="27423-990">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="27423-991">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-991"></span></span>|
|<span data-ttu-id="27423-992">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-992">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="27423-993">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-993"></span></span>|
|<span data-ttu-id="27423-994">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-994">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="27423-995">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-995"></span></span>|
|<span data-ttu-id="27423-996">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="27423-996">**CRL URLs**</span></span>|
|<span data-ttu-id="27423-997">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-997"></span></span>|
|<span data-ttu-id="27423-998">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="27423-998">**OCSP URLs**</span></span>|
|<span data-ttu-id="27423-999">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-999"></span></span>|
   
 <span data-ttu-id="27423-1000">**Autoridade de certificação do Microsoft IT TLS 5**</span><span class="sxs-lookup"><span data-stu-id="27423-1000">**Microsoft IT TLS CA 5**</span></span>
  
||
|:-----|
|<span data-ttu-id="27423-1001">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-1001">**Subject**</span></span>|
|<span data-ttu-id="27423-1002">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1002"></span></span>|
|<span data-ttu-id="27423-1003">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="27423-1003">**Issuer**</span></span>|
|<span data-ttu-id="27423-1004">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1004"></span></span>|
|<span data-ttu-id="27423-1005">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="27423-1005">**Serial Number**</span></span>|
|<span data-ttu-id="27423-1006">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1006"></span></span>|
|<span data-ttu-id="27423-1007">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="27423-1007">**Public Key Length**</span></span>|
|<span data-ttu-id="27423-1008">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1008"></span></span>|
|<span data-ttu-id="27423-1009">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="27423-1009">**Signature Algorithm**</span></span>|
|<span data-ttu-id="27423-1010">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1010"></span></span>|
|<span data-ttu-id="27423-1011">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="27423-1011">**Validity Not Before**</span></span>|
|<span data-ttu-id="27423-1012">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1012"></span></span>|
|<span data-ttu-id="27423-1013">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="27423-1013">**Validity Not After**</span></span>|
|<span data-ttu-id="27423-1014">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1014"></span></span>|
|<span data-ttu-id="27423-1015">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-1015">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="27423-1016">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1016"></span></span>|
|<span data-ttu-id="27423-1017">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="27423-1017">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="27423-1018">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1018"></span></span>|
|<span data-ttu-id="27423-1019">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="27423-1019">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="27423-1020">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1020"></span></span>|
|<span data-ttu-id="27423-1021">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-1021">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="27423-1022">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1022"></span></span>|
|<span data-ttu-id="27423-1023">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-1023">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="27423-1024">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1024"></span></span>|
|<span data-ttu-id="27423-1025">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="27423-1025">**CRL URLs**</span></span>|
|<span data-ttu-id="27423-1026">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1026"></span></span>|
|<span data-ttu-id="27423-1027">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="27423-1027">**OCSP URLs**</span></span>|
|<span data-ttu-id="27423-1028">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1028"></span></span>|
   
 <span data-ttu-id="27423-1029">**CA de SSL Symantec classe EV 3 - G3**</span><span class="sxs-lookup"><span data-stu-id="27423-1029">**Symantec Class 3 EV SSL CA - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="27423-1030">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-1030">**Subject**</span></span>|
|<span data-ttu-id="27423-1031">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1031"></span></span>|
|<span data-ttu-id="27423-1032">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="27423-1032">**Issuer**</span></span>|
|<span data-ttu-id="27423-1033">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1033"></span></span>|
|<span data-ttu-id="27423-1034">**Nome alternativo da entidade**</span><span class="sxs-lookup"><span data-stu-id="27423-1034">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="27423-1035">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1035"></span></span>|
|<span data-ttu-id="27423-1036">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="27423-1036">**Serial Number**</span></span>|
|<span data-ttu-id="27423-1037">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1037"></span></span>|
|<span data-ttu-id="27423-1038">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="27423-1038">**Public Key Length**</span></span>|
|<span data-ttu-id="27423-1039">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1039"></span></span>|
|<span data-ttu-id="27423-1040">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="27423-1040">**Signature Algorithm**</span></span>|
|<span data-ttu-id="27423-1041">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1041"></span></span>|
|<span data-ttu-id="27423-1042">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="27423-1042">**Validity Not Before**</span></span>|
|<span data-ttu-id="27423-1043">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1043"></span></span>|
|<span data-ttu-id="27423-1044">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="27423-1044">**Validity Not After**</span></span>|
|<span data-ttu-id="27423-1045">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1045"></span></span>|
|<span data-ttu-id="27423-1046">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-1046">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="27423-1047">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1047"></span></span>|
|<span data-ttu-id="27423-1048">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="27423-1048">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="27423-1049">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1049"></span></span>|
|<span data-ttu-id="27423-1050">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="27423-1050">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="27423-1051">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1051"></span></span>|
|<span data-ttu-id="27423-1052">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-1052">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="27423-1053">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1053"></span></span>|
|<span data-ttu-id="27423-1054">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-1054">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="27423-1055">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1055"></span></span>|
|<span data-ttu-id="27423-1056">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="27423-1056">**CRL URLs**</span></span>|
|<span data-ttu-id="27423-1057">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1057"></span></span>|
|<span data-ttu-id="27423-1058">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="27423-1058">**OCSP URLs**</span></span>|
|<span data-ttu-id="27423-1059">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1059"></span></span>|
   
 <span data-ttu-id="27423-1060">**Symantec classe 3 servidores seguros CA - G4**</span><span class="sxs-lookup"><span data-stu-id="27423-1060">**Symantec Class 3 Secure Server CA - G4**</span></span>
  
||
|:-----|
|<span data-ttu-id="27423-1061">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-1061">**Subject**</span></span>|
|<span data-ttu-id="27423-1062">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1062"></span></span>|
|<span data-ttu-id="27423-1063">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="27423-1063">**Issuer**</span></span>|
|<span data-ttu-id="27423-1064">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1064"></span></span>|
|<span data-ttu-id="27423-1065">**Nome alternativo da entidade**</span><span class="sxs-lookup"><span data-stu-id="27423-1065">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="27423-1066">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1066"></span></span>|
|<span data-ttu-id="27423-1067">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="27423-1067">**Serial Number**</span></span>|
|<span data-ttu-id="27423-1068">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1068"></span></span>|
|<span data-ttu-id="27423-1069">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="27423-1069">**Public Key Length**</span></span>|
|<span data-ttu-id="27423-1070">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1070"></span></span>|
|<span data-ttu-id="27423-1071">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="27423-1071">**Signature Algorithm**</span></span>|
|<span data-ttu-id="27423-1072">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1072"></span></span>|
|<span data-ttu-id="27423-1073">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="27423-1073">**Validity Not Before**</span></span>|
|<span data-ttu-id="27423-1074">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1074"></span></span>|
|<span data-ttu-id="27423-1075">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="27423-1075">**Validity Not After**</span></span>|
|<span data-ttu-id="27423-1076">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1076"></span></span>|
|<span data-ttu-id="27423-1077">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-1077">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="27423-1078">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1078"></span></span>|
|<span data-ttu-id="27423-1079">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="27423-1079">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="27423-1080">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1080"></span></span>|
|<span data-ttu-id="27423-1081">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="27423-1081">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="27423-1082">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1082"></span></span>|
|<span data-ttu-id="27423-1083">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-1083">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="27423-1084">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1084"></span></span>|
|<span data-ttu-id="27423-1085">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-1085">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="27423-1086">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1086"></span></span>|
|<span data-ttu-id="27423-1087">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="27423-1087">**CRL URLs**</span></span>|
|<span data-ttu-id="27423-1088">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1088"></span></span>|
|<span data-ttu-id="27423-1089">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="27423-1089">**OCSP URLs**</span></span>|
|<span data-ttu-id="27423-1090">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1090"></span></span>|
   
 <span data-ttu-id="27423-1091">**Thawte SHA256 SSL da autoridade de certificação**</span><span class="sxs-lookup"><span data-stu-id="27423-1091">**thawte SHA256 SSL CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="27423-1092">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-1092">**Subject**</span></span>|
|<span data-ttu-id="27423-1093">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1093"></span></span>|
|<span data-ttu-id="27423-1094">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="27423-1094">**Issuer**</span></span>|
|<span data-ttu-id="27423-1095">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1095"></span></span>|
|<span data-ttu-id="27423-1096">**Nome alternativo da entidade**</span><span class="sxs-lookup"><span data-stu-id="27423-1096">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="27423-1097">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1097"></span></span>|
|<span data-ttu-id="27423-1098">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="27423-1098">**Serial Number**</span></span>|
|<span data-ttu-id="27423-1099">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1099"></span></span>|
|<span data-ttu-id="27423-1100">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="27423-1100">**Public Key Length**</span></span>|
|<span data-ttu-id="27423-1101">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1101"></span></span>|
|<span data-ttu-id="27423-1102">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="27423-1102">**Signature Algorithm**</span></span>|
|<span data-ttu-id="27423-1103">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1103"></span></span>|
|<span data-ttu-id="27423-1104">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="27423-1104">**Validity Not Before**</span></span>|
|<span data-ttu-id="27423-1105">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1105"></span></span>|
|<span data-ttu-id="27423-1106">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="27423-1106">**Validity Not After**</span></span>|
|<span data-ttu-id="27423-1107">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1107"></span></span>|
|<span data-ttu-id="27423-1108">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-1108">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="27423-1109">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1109"></span></span>|
|<span data-ttu-id="27423-1110">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="27423-1110">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="27423-1111">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1111"></span></span>|
|<span data-ttu-id="27423-1112">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="27423-1112">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="27423-1113">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1113"></span></span>|
|<span data-ttu-id="27423-1114">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-1114">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="27423-1115">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1115"></span></span>|
|<span data-ttu-id="27423-1116">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-1116">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="27423-1117">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1117"></span></span>|
|<span data-ttu-id="27423-1118">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="27423-1118">**CRL URLs**</span></span>|
|<span data-ttu-id="27423-1119">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1119"></span></span>|
|<span data-ttu-id="27423-1120">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="27423-1120">**OCSP URLs**</span></span>|
|<span data-ttu-id="27423-1121">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1121"></span></span>|
   
 <span data-ttu-id="27423-1122">**Verizon Akamai SureServer CA G14-SHA2**</span><span class="sxs-lookup"><span data-stu-id="27423-1122">**Verizon Akamai SureServer CA G14-SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="27423-1123">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-1123">**Subject**</span></span>|
|<span data-ttu-id="27423-1124">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1124"></span></span>|
|<span data-ttu-id="27423-1125">**Emissor**</span><span class="sxs-lookup"><span data-stu-id="27423-1125">**Issuer**</span></span>|
|<span data-ttu-id="27423-1126">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1126"></span></span>|
|<span data-ttu-id="27423-1127">**Número de série**</span><span class="sxs-lookup"><span data-stu-id="27423-1127">**Serial Number**</span></span>|
|<span data-ttu-id="27423-1128">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1128"></span></span>|
|<span data-ttu-id="27423-1129">**Comprimento de chave pública**</span><span class="sxs-lookup"><span data-stu-id="27423-1129">**Public Key Length**</span></span>|
|<span data-ttu-id="27423-1130">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1130"></span></span>|
|<span data-ttu-id="27423-1131">**Algoritmo de assinatura**</span><span class="sxs-lookup"><span data-stu-id="27423-1131">**Signature Algorithm**</span></span>|
|<span data-ttu-id="27423-1132">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1132"></span></span>|
|<span data-ttu-id="27423-1133">**Não antes de validade**</span><span class="sxs-lookup"><span data-stu-id="27423-1133">**Validity Not Before**</span></span>|
|<span data-ttu-id="27423-1134">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1134"></span></span>|
|<span data-ttu-id="27423-1135">**Validade não após**</span><span class="sxs-lookup"><span data-stu-id="27423-1135">**Validity Not After**</span></span>|
|<span data-ttu-id="27423-1136">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1136"></span></span>|
|<span data-ttu-id="27423-1137">**Identificador de chave de assunto**</span><span class="sxs-lookup"><span data-stu-id="27423-1137">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="27423-1138">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1138"></span></span>|
|<span data-ttu-id="27423-1139">**Identificador de chave de autoridade**</span><span class="sxs-lookup"><span data-stu-id="27423-1139">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="27423-1140">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1140"></span></span>|
|<span data-ttu-id="27423-1141">**Impressão digital (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="27423-1141">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="27423-1142">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1142"></span></span>|
|<span data-ttu-id="27423-1143">**Impressão digital (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-1143">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="27423-1144">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1144"></span></span>|
|<span data-ttu-id="27423-1145">**PIN (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="27423-1145">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="27423-1146">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1146"></span></span>|
|<span data-ttu-id="27423-1147">**URLs AIA**</span><span class="sxs-lookup"><span data-stu-id="27423-1147">**AIA URLs**</span></span>|
|<span data-ttu-id="27423-1148">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1148"></span></span>|
|<span data-ttu-id="27423-1149">**URLs CRL**</span><span class="sxs-lookup"><span data-stu-id="27423-1149">**CRL URLs**</span></span>|
|<span data-ttu-id="27423-1150">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1150"></span></span>|
|<span data-ttu-id="27423-1151">**URLs OCSP**</span><span class="sxs-lookup"><span data-stu-id="27423-1151">**OCSP URLs**</span></span>|
|<span data-ttu-id="27423-1152">:-----</span><span class="sxs-lookup"><span data-stu-id="27423-1152"></span></span>|
   
## <a name="additional-certificate-paths"></a><span data-ttu-id="27423-1153">Caminhos de certificado adicional</span><span class="sxs-lookup"><span data-stu-id="27423-1153">Additional certificate paths</span></span>
<span data-ttu-id="27423-1154"><a name="IntermediateCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="27423-1154"></span></span>

<span data-ttu-id="27423-1155">A seguir incluem certificados herdados que não estão incluídos acima e serão mesclados com a lista acima ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="27423-1155">The following include legacy certificates that aren't included above and will be merged with the list above over time.</span></span>
  
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



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
# <a name="office-365-certificate-chains"></a>Cadeias de certificados do Office 365

O Office 365 utiliza um número de provedores de certificado diferente. O exemplo a seguir descreve a lista completa de certificados de raiz Office 365 conhecidos que os clientes podem encontrar ao acessar o Office 365. Para obter informações sobre os certificados que você talvez precise instalar em sua própria infra-estrutura, consulte [Planejar certificados SSL de terceiros para o Office 365](https://support.office.com/article/b48cdf63-07e0-4cda-8c12-4871590f59ce). As seguintes informações de certificado se aplica a todas as instâncias de nuvem em todo o mundo e Nacional do Office 365.
  

|**Tipo de certificado**|**P7b download**|**Pontos de extremidade da lista de certificados Revogados**|**Pontos de extremidade OCSP**|**Pontos de extremidade AIA**|
|:-----|:-----|:-----|:-----|:-----|
|[Certificados raiz de publicamente confiáveis](https://support.office.com/article/0c03e6b3-e73f-4316-9e2b-bf4091ae96bb#rootcerts) <br/> |[Pacote de certificado raiz do Office 365 (P7B)](http://download.microsoft.com/download/A/5/A/A5AE01F3-D19B-4A11-9407-801263CEF72C/O365_Root_Certs_20170321.p7b) <br/> |CRL.GlobalSign.NET  <br/> www.d-Trust.NET  <br/> |N/D  <br/> |N/D  <br/> |
|[Publicamente confiáveis certificados intermediários](https://support.office.com/article/0c03e6b3-e73f-4316-9e2b-bf4091ae96bb#IntermediateCerts) <br/> |[Pacote do Office 365 intermediário de certificado (P7B)](http://download.microsoft.com/download/4/D/5/4D5339A4-0A4A-46AB-AE52-B179DEDA4BEC/O365_Intermediate_Certs_20170321.p7b)  <br/> |cdp1.Public-trust.com  <br/> CRL.cnnic.CN  <br/> CRL.Entrust.NET  <br/> CRL.GlobalSign.com  <br/> CRL.GlobalSign.NET  <br/> CRL.identrust.com  <br/> CRL.Thawte.com  <br/> crl3.digicert.com  <br/> crl4.digicert.com  <br/> S1.symcb.com  <br/> www.d-Trust.NET  <br/> |isrg.trustid.OCSP.identrust.com  <br/> OCSP.digicert.com  <br/> OCSP.Entrust.NET  <br/> OCSP.GlobalSign.com  <br/> OCSP.omniroot.com  <br/> OCSP.startssl.com  <br/> OCSP.Thawte.com  <br/> ocsp2.GlobalSign.com  <br/> ocspcnnicroot.cnnic.CN  <br/> raiz-c3-ca2-2009.ocsp.d-trust.net  <br/> root-C3-ca2-EV-2009.OCSP.d-Trust.NET  <br/> S2.symcb.com  <br/> |AIA.startssl.com  <br/> Apps.identrust.com  <br/> cacert.omniroot.com  <br/> www.cnnic.CN  <br/> |
   
Expanda a raiz e intermediárias seções abaixo para ver detalhes adicionais sobre os provedores de certificado.
  
## <a name="office-365-root-certificate-details"></a>O Office 365 detalhes do certificado raiz
<a name="RootCerts"> </a>

 **Baltimore CyberTrust Root**
  
|:-----|
|**Assunto**|
|:-----|
|**Número de série**|
|:-----|
|**Comprimento de chave pública**|
|:-----|
|**Algoritmo de assinatura**|
|:-----|
|**Não antes de validade**|
|:-----|
|**Validade não após**|
|:-----|
|**Identificador de chave de assunto**|
|:-----|
|**Impressão digital (SHA-1)**|
|:-----|
|**Impressão digital (SHA-256)**|
|:-----|
|**PIN (SHA-256)**|
|:-----|
   
 **RAIZ CNNIC**
  
||
|:-----|
|**Assunto**|
|:-----|
|**Número de série**|
|:-----|
|**Comprimento de chave pública**|
|:-----|
|**Algoritmo de assinatura**|
|:-----|
|**Não antes de validade**|
|:-----|
|**Validade não após**|
|:-----|
|**Identificador de chave de assunto**|
|:-----|
|**Identificador de chave de autoridade**|
|:-----|
|**Impressão digital (SHA-1)**|
|:-----|
|**Impressão digital (SHA-256)**|
|:-----|
|**PIN (SHA-256)**|
|:-----|
   
 **CA de raiz Global DigiCert**
  
||
|:-----|
|**Assunto**|
|:-----|
|**Número de série**|
|:-----|
|**Comprimento de chave pública**|
|:-----|
|**Algoritmo de assinatura**|
|:-----|
|**Não antes de validade**|
|:-----|
|**Validade não após**|
|:-----|
|**Identificador de chave de assunto**|
|:-----|
|**Identificador de chave de autoridade**|
|:-----|
|**Impressão digital (SHA-1)**|
|:-----|
|**Impressão digital (SHA-256)**|
|:-----|
|**PIN (SHA-256)**|
|:-----|
   
 **Autoridade de certificação de raiz de garantia EV alta DigiCert**
  
||
|:-----|
|**Assunto**|
|:-----|
|**Número de série**|
|:-----|
|**Comprimento de chave pública**|
|:-----|
|**Algoritmo de assinatura**|
|:-----|
|**Não antes de validade**|
|:-----|
|**Validade não após**|
|:-----|
|**Identificador de chave de assunto**|
|:-----|
|**Identificador de chave de autoridade**|
|:-----|
|**Impressão digital (SHA-1)**|
|:-----|
|**Impressão digital (SHA-256)**|
|:-----|
|**PIN (SHA-256)**|
|:-----|
   
 **Autoridade de certificação da classe 3 de raiz de confiança D 2 de 2009**
  
||
|:-----|
|**Assunto**|
|:-----|
|**Número de série**|
|:-----|
|**Comprimento de chave pública**|
|:-----|
|**Algoritmo de assinatura**|
|:-----|
|**Não antes de validade**|
|:-----|
|**Validade não após**|
|:-----|
|**Identificador de chave de assunto**|
|:-----|
|**Impressão digital (SHA-1)**|
|:-----|
|**Impressão digital (SHA-256)**|
|:-----|
|**PIN (SHA-256)**|
|:-----|
|**URLs CRL**|
|:-----|
   
 **Autoridade de certificação raiz confiável D classe 3 2 EV de 2009**
  
||
|:-----|
|**Assunto**|
|:-----|
|**Número de série**|
|:-----|
|**Comprimento de chave pública**|
|:-----|
|**Algoritmo de assinatura**|
|:-----|
|**Não antes de validade**|
|:-----|
|**Validade não após**|
|:-----|
|**Identificador de chave de assunto**|
|:-----|
|**Impressão digital (SHA-1)**|
|:-----|
|**Impressão digital (SHA-256)**|
|:-----|
|**PIN (SHA-256)**|
|:-----|
|**URLs CRL**|
|:-----|
   
 **Horário de verão raiz da autoridade de certificação X3**
  
||
|:-----|
|**Assunto**|
|:-----|
|**Número de série**|
|:-----|
|**Comprimento de chave pública**|
|:-----|
|**Algoritmo de assinatura**|
|:-----|
|**Não antes de validade**|
|:-----|
|**Validade não após**|
|:-----|
|**Identificador de chave de assunto**|
|:-----|
|**Impressão digital (SHA-1)**|
|:-----|
|**Impressão digital (SHA-256)**|
|:-----|
|**PIN (SHA-256)**|
|:-----|
   
 **Entrust autoridade de certificação raiz - G2**
  
||
|:-----|
|**Assunto**|
|:-----|
|**Número de série**|
|:-----|
|**Comprimento de chave pública**|
|:-----|
|**Algoritmo de assinatura**|
|:-----|
|**Não antes de validade**|
|:-----|
|**Validade não após**|
|:-----|
|**Identificador de chave de assunto**|
|:-----|
|**Impressão digital (SHA-1)**|
|:-----|
|**Impressão digital (SHA-256)**|
|:-----|
|**PIN (SHA-256)**|
|:-----|
   
 **Entrust.net Certification Authority (2048)**
  
||
|:-----|
|**Assunto**|
|:-----|
|**Número de série**|
|:-----|
|**Comprimento de chave pública**|
|:-----|
|**Algoritmo de assinatura**|
|:-----|
|**Não antes de validade**|
|:-----|
|**Validade não após**|
|:-----|
|**Identificador de chave de assunto**|
|:-----|
|**Impressão digital (SHA-1)**|
|:-----|
|**Impressão digital (SHA-256)**|
|:-----|
|**PIN (SHA-256)**|
|:-----|
   
 **GlobalSign**
  
||
|:-----|
|**Assunto**|
|:-----|
|**Número de série**|
|:-----|
|**Comprimento de chave pública**|
|:-----|
|**Algoritmo de assinatura**|
|:-----|
|**Não antes de validade**|
|:-----|
|**Validade não após**|
|:-----|
|**Identificador de chave de assunto**|
|:-----|
|**Identificador de chave de autoridade**|
|:-----|
|**Impressão digital (SHA-1)**|
|:-----|
|**Impressão digital (SHA-256)**|
|:-----|
|**PIN (SHA-256)**|
|:-----|
|**URLs CRL**|
|:-----|
   
 **GlobalSign Root CA**
  
||
|:-----|
|**Assunto**|
|:-----|
|**Número de série**|
|:-----|
|**Comprimento de chave pública**|
|:-----|
|**Algoritmo de assinatura**|
|:-----|
|**Não antes de validade**|
|:-----|
|**Validade não após**|
|:-----|
|**Identificador de chave de assunto**|
|:-----|
|**Impressão digital (SHA-1)**|
|:-----|
|**Impressão digital (SHA-256)**|
|:-----|
|**PIN (SHA-256)**|
|:-----|
   
 **Thawte autoridade de certificação raiz primária - G3**
  
||
|:-----|
|**Assunto**|
|:-----|
|**Número de série**|
|:-----|
|**Comprimento de chave pública**|
|:-----|
|**Algoritmo de assinatura**|
|:-----|
|**Não antes de validade**|
|:-----|
|**Validade não após**|
|:-----|
|**Identificador de chave de assunto**|
|:-----|
|**Impressão digital (SHA-1)**|
|:-----|
|**Impressão digital (SHA-256)**|
|:-----|
|**PIN (SHA-256)**|
|:-----|
   
 **Autoridade de certificação principal pública classe VeriSign 3 - G5**
  
||
|:-----|
|**Assunto**|
|:-----|
|**Número de série**|
|:-----|
|**Comprimento de chave pública**|
|:-----|
|**Algoritmo de assinatura**|
|:-----|
|**Não antes de validade**|
|:-----|
|**Validade não após**|
|:-----|
|**Identificador de chave de assunto**|
|:-----|
|**Impressão digital (SHA-1)**|
|:-----|
|**Impressão digital (SHA-256)**|
|:-----|
|**PIN (SHA-256)**|
|:-----|
   
## <a name="office-365-intermediate-certificate-details"></a>Detalhes do certificado intermediário de Office 365
<a name="IntermediateCerts"> </a>

 **CNNIC SHA256 SSL**
  
||
|:-----|
|**Assunto**|
|:-----|
|**Emissor**|
|:-----|
|**Número de série**|
|:-----|
|**Comprimento de chave pública**|
|:-----|
|**Algoritmo de assinatura**|
|:-----|
|**Não antes de validade**|
|:-----|
|**Validade não após**|
|:-----|
|**Identificador de chave de assunto**|
|:-----|
|**Identificador de chave de autoridade**|
|:-----|
|**Impressão digital (SHA-1)**|
|:-----|
|**Impressão digital (SHA-256)**|
|:-----|
|**PIN (SHA-256)**|
|:-----|
|**URLs AIA**|
|:-----|
|**URLs CRL**|
|:-----|
|**URLs OCSP**|
|:-----|
   
 **D-TRUST SSL classe 3 CA 1 2009**
  
||
|:-----|
|**Assunto**|
|:-----|
|**Emissor**|
|:-----|
|**Nome alternativo da entidade**|
|:-----|
|**Número de série**|
|:-----|
|**Comprimento de chave pública**|
|:-----|
|**Algoritmo de assinatura**|
|:-----|
|**Não antes de validade**|
|:-----|
|**Validade não após**|
|:-----|
|**Identificador de chave de assunto**|
|:-----|
|**Identificador de chave de autoridade**|
|:-----|
|**Impressão digital (SHA-1)**|
|:-----|
|**Impressão digital (SHA-256)**|
|:-----|
|**PIN (SHA-256)**|
|:-----|
|**URLs CRL**|
|:-----|
|**URLs OCSP**|
|:-----|
   
 **Autoridade de certificação confiável D SSL classe 3 1 EV de 2009**
  
||
|:-----|
|**Assunto**|
|:-----|
|**Emissor**|
|:-----|
|**Nome alternativo da entidade**|
|:-----|
|**Número de série**|
|:-----|
|**Comprimento de chave pública**|
|:-----|
|**Algoritmo de assinatura**|
|:-----|
|**Não antes de validade**|
|:-----|
|**Validade não após**|
|:-----|
|**Identificador de chave de assunto**|
|:-----|
|**Identificador de chave de autoridade**|
|:-----|
|**Impressão digital (SHA-1)**|
|:-----|
|**Impressão digital (SHA-256)**|
|:-----|
|**PIN (SHA-256)**|
|:-----|
|**URLs CRL**|
|:-----|
|**URLs OCSP**|
|:-----|
   
 **Serviços em nuvem de DigiCert CA-1**
  
||
|:-----|
|**Assunto**|
|:-----|
|**Emissor**|
|:-----|
|**Número de série**|
|:-----|
|**Comprimento de chave pública**|
|:-----|
|**Algoritmo de assinatura**|
|:-----|
|**Não antes de validade**|
|:-----|
|**Validade não após**|
|:-----|
|**Identificador de chave de assunto**|
|:-----|
|**Identificador de chave de autoridade**|
|:-----|
|**Impressão digital (SHA-1)**|
|:-----|
|**Impressão digital (SHA-256)**|
|:-----|
|**PIN (SHA-256)**|
|:-----|
|**URLs CRL**|
|:-----|
|**URLs OCSP**|
|:-----|
   
 **Servidor de alta garantia DigiCert SHA2 CA**
  
||
|:-----|
|**Assunto**|
|:-----|
|**Emissor**|
|:-----|
|**Número de série**|
|:-----|
|**Comprimento de chave pública**|
|:-----|
|**Algoritmo de assinatura**|
|:-----|
|**Não antes de validade**|
|:-----|
|**Validade não após**|
|:-----|
|**Identificador de chave de assunto**|
|:-----|
|**Identificador de chave de autoridade**|
|:-----|
|**Impressão digital (SHA-1)**|
|:-----|
|**Impressão digital (SHA-256)**|
|:-----|
|**PIN (SHA-256)**|
|:-----|
|**URLs CRL**|
|:-----|
|**URLs OCSP**|
|:-----|
   
 **Servidores de seguros DigiCert SHA2 CA**
  
||
|:-----|
|**Assunto**|
|:-----|
|**Emissor**|
|:-----|
|**Número de série**|
|:-----|
|**Comprimento de chave pública**|
|:-----|
|**Algoritmo de assinatura**|
|:-----|
|**Não antes de validade**|
|:-----|
|**Validade não após**|
|:-----|
|**Identificador de chave de assunto**|
|:-----|
|**Identificador de chave de autoridade**|
|:-----|
|**Impressão digital (SHA-1)**|
|:-----|
|**Impressão digital (SHA-256)**|
|:-----|
|**PIN (SHA-256)**|
|:-----|
|**URLs CRL**|
|:-----|
|**URLs OCSP**|
|:-----|
   
 **Entrust autoridade de certificação - L1C**
  
||
|:-----|
|**Assunto**|
|:-----|
|**Emissor**|
|:-----|
|**Número de série**|
|:-----|
|**Comprimento de chave pública**|
|:-----|
|**Algoritmo de assinatura**|
|:-----|
|**Não antes de validade**|
|:-----|
|**Validade não após**|
|:-----|
|**Identificador de chave de assunto**|
|:-----|
|**Identificador de chave de autoridade**|
|:-----|
|**Impressão digital (SHA-1)**|
|:-----|
|**Impressão digital (SHA-256)**|
|:-----|
|**PIN (SHA-256)**|
|:-----|
|**URLs CRL**|
|:-----|
|**URLs OCSP**|
|:-----|
   
 **Entrust autoridade de certificação - L1K**
  
||
|:-----|
|**Assunto**|
|:-----|
|**Emissor**|
|:-----|
|**Número de série**|
|:-----|
|**Comprimento de chave pública**|
|:-----|
|**Algoritmo de assinatura**|
|:-----|
|**Não antes de validade**|
|:-----|
|**Validade não após**|
|:-----|
|**Identificador de chave de assunto**|
|:-----|
|**Identificador de chave de autoridade**|
|:-----|
|**Impressão digital (SHA-1)**|
|:-----|
|**Impressão digital (SHA-256)**|
|:-----|
|**PIN (SHA-256)**|
|:-----|
|**URLs CRL**|
|:-----|
|**URLs OCSP**|
|:-----|
   
 **GlobalSign**
  
||
|:-----|
|**Assunto**|
|:-----|
|**Emissor**|
|:-----|
|**Número de série**|
|:-----|
|**Comprimento de chave pública**|
|:-----|
|**Algoritmo de assinatura**|
|:-----|
|**Não antes de validade**|
|:-----|
|**Validade não após**|
|:-----|
|**Identificador de chave de assunto**|
|:-----|
|**Identificador de chave de autoridade**|
|:-----|
|**Impressão digital (SHA-1)**|
|:-----|
|**Impressão digital (SHA-256)**|
|:-----|
|**PIN (SHA-256)**|
|:-----|
|**URLs CRL**|
|:-----|
|**URLs OCSP**|
|:-----|
   
 **GlobalSign estendido validação CA - SHA256 - G2**
  
||
|:-----|
|**Assunto**|
|:-----|
|**Emissor**|
|:-----|
|**Número de série**|
|:-----|
|**Comprimento de chave pública**|
|:-----|
|**Algoritmo de assinatura**|
|:-----|
|**Não antes de validade**|
|:-----|
|**Validade não após**|
|:-----|
|**Identificador de chave de assunto**|
|:-----|
|**Identificador de chave de autoridade**|
|:-----|
|**Impressão digital (SHA-1)**|
|:-----|
|**Impressão digital (SHA-256)**|
|:-----|
|**PIN (SHA-256)**|
|:-----|
|**URLs CRL**|
|:-----|
|**URLs OCSP**|
|:-----|
   
 **GlobalSign estendido validação CA - SHA256 - G3**
  
||
|:-----|
|**Assunto**|
|:-----|
|**Emissor**|
|:-----|
|**Número de série**|
|:-----|
|**Comprimento de chave pública**|
|:-----|
|**Algoritmo de assinatura**|
|:-----|
|**Não antes de validade**|
|:-----|
|**Validade não após**|
|:-----|
|**Identificador de chave de assunto**|
|:-----|
|**Identificador de chave de autoridade**|
|:-----|
|**Impressão digital (SHA-1)**|
|:-----|
|**Impressão digital (SHA-256)**|
|:-----|
|**PIN (SHA-256)**|
|:-----|
|**URLs CRL**|
|:-----|
|**URLs OCSP**|
|:-----|
   
 **GlobalSign organização validação CA - SHA256 - G2**
  
||
|:-----|
|**Assunto**|
|:-----|
|**Emissor**|
|:-----|
|**Número de série**|
|:-----|
|**Comprimento de chave pública**|
|:-----|
|**Algoritmo de assinatura**|
|:-----|
|**Não antes de validade**|
|:-----|
|**Validade não após**|
|:-----|
|**Identificador de chave de assunto**|
|:-----|
|**Identificador de chave de autoridade**|
|:-----|
|**Impressão digital (SHA-1)**|
|:-----|
|**Impressão digital (SHA-256)**|
|:-----|
|**PIN (SHA-256)**|
|:-----|
|**URLs CRL**|
|:-----|
|**URLs OCSP**|
|:-----|
   
 **GlobalSign organização validação CA - SHA256 - G2**
  
||
|:-----|
|**Assunto**|
|:-----|
|**Emissor**|
|:-----|
|**Número de série**|
|:-----|
|**Comprimento de chave pública**|
|:-----|
|**Algoritmo de assinatura**|
|:-----|
|**Não antes de validade**|
|:-----|
|**Validade não após**|
|:-----|
|**Identificador de chave de assunto**|
|:-----|
|**Identificador de chave de autoridade**|
|:-----|
|**Impressão digital (SHA-1)**|
|:-----|
|**Impressão digital (SHA-256)**|
|:-----|
|**PIN (SHA-256)**|
|:-----|
|**URLs CRL**|
|:-----|
|**URLs OCSP**|
|:-----|
   
 **Criptografar vamos autoridade X3**
  
||
|:-----|
|**Assunto**|
|:-----|
|**Emissor**|
|:-----|
|**Número de série**|
|:-----|
|**Comprimento de chave pública**|
|:-----|
|**Algoritmo de assinatura**|
|:-----|
|**Não antes de validade**|
|:-----|
|**Validade não após**|
|:-----|
|**Identificador de chave de assunto**|
|:-----|
|**Identificador de chave de autoridade**|
|:-----|
|**Impressão digital (SHA-1)**|
|:-----|
|**Impressão digital (SHA-256)**|
|:-----|
|**PIN (SHA-256)**|
|:-----|
|**URLs AIA**|
|:-----|
|**URLs CRL**|
|:-----|
|**URLs OCSP**|
|:-----|
   
 **O TI da Microsoft SSL SHA2**
  
||
|:-----|
|**Assunto**|
|:-----|
|**Emissor**|
|:-----|
|**Número de série**|
|:-----|
|**Comprimento de chave pública**|
|:-----|
|**Algoritmo de assinatura**|
|:-----|
|**Não antes de validade**|
|:-----|
|**Validade não após**|
|:-----|
|**Identificador de chave de assunto**|
|:-----|
|**Identificador de chave de autoridade**|
|:-----|
|**Impressão digital (SHA-1)**|
|:-----|
|**Impressão digital (SHA-256)**|
|:-----|
|**PIN (SHA-256)**|
|:-----|
|**URLs CRL**|
|:-----|
   
 **O TI da Microsoft SSL SHA2**
  
||
|:-----|
|**Assunto**|
|:-----|
|**Emissor**|
|:-----|
|**Número de série**|
|:-----|
|**Comprimento de chave pública**|
|:-----|
|**Algoritmo de assinatura**|
|:-----|
|**Não antes de validade**|
|:-----|
|**Validade não após**|
|:-----|
|**Identificador de chave de assunto**|
|:-----|
|**Identificador de chave de autoridade**|
|:-----|
|**Impressão digital (SHA-1)**|
|:-----|
|**Impressão digital (SHA-256)**|
|:-----|
|**PIN (SHA-256)**|
|:-----|
|**URLs CRL**|
|:-----|
|**URLs OCSP**|
|:-----|
   
 **Autoridade de certificação do Microsoft IT TLS 1**
  
||
|:-----|
|**Assunto**|
|:-----|
|**Emissor**|
|:-----|
|**Número de série**|
|:-----|
|**Comprimento de chave pública**|
|:-----|
|**Algoritmo de assinatura**|
|:-----|
|**Não antes de validade**|
|:-----|
|**Validade não após**|
|:-----|
|**Identificador de chave de assunto**|
|:-----|
|**Identificador de chave de autoridade**|
|:-----|
|**Impressão digital (SHA-1)**|
|:-----|
|**Impressão digital (SHA-256)**|
|:-----|
|**PIN (SHA-256)**|
|:-----|
|**URLs CRL**|
|:-----|
|**URLs OCSP**|
|:-----|
   
 **Autoridade de certificação do Microsoft IT TLS 2**
  
||
|:-----|
|**Assunto**|
|:-----|
|**Emissor**|
|:-----|
|**Número de série**|
|:-----|
|**Comprimento de chave pública**|
|:-----|
|**Algoritmo de assinatura**|
|:-----|
|**Não antes de validade**|
|:-----|
|**Validade não após**|
|:-----|
|**Identificador de chave de assunto**|
|:-----|
|**Identificador de chave de autoridade**|
|:-----|
|**Impressão digital (SHA-1)**|
|:-----|
|**Impressão digital (SHA-256)**|
|:-----|
|**PIN (SHA-256)**|
|:-----|
|**URLs CRL**|
|:-----|
|**URLs OCSP**|
|:-----|
   
 **Autoridade de certificação do Microsoft IT TLS 4**
  
||
|:-----|
|**Assunto**|
|:-----|
|**Emissor**|
|:-----|
|**Número de série**|
|:-----|
|**Comprimento de chave pública**|
|:-----|
|**Algoritmo de assinatura**|
|:-----|
|**Não antes de validade**|
|:-----|
|**Validade não após**|
|:-----|
|**Identificador de chave de assunto**|
|:-----|
|**Identificador de chave de autoridade**|
|:-----|
|**Impressão digital (SHA-1)**|
|:-----|
|**Impressão digital (SHA-256)**|
|:-----|
|**PIN (SHA-256)**|
|:-----|
|**URLs CRL**|
|:-----|
|**URLs OCSP**|
|:-----|
   
 **Autoridade de certificação do Microsoft IT TLS 5**
  
||
|:-----|
|**Assunto**|
|:-----|
|**Emissor**|
|:-----|
|**Número de série**|
|:-----|
|**Comprimento de chave pública**|
|:-----|
|**Algoritmo de assinatura**|
|:-----|
|**Não antes de validade**|
|:-----|
|**Validade não após**|
|:-----|
|**Identificador de chave de assunto**|
|:-----|
|**Identificador de chave de autoridade**|
|:-----|
|**Impressão digital (SHA-1)**|
|:-----|
|**Impressão digital (SHA-256)**|
|:-----|
|**PIN (SHA-256)**|
|:-----|
|**URLs CRL**|
|:-----|
|**URLs OCSP**|
|:-----|
   
 **CA de SSL Symantec classe EV 3 - G3**
  
||
|:-----|
|**Assunto**|
|:-----|
|**Emissor**|
|:-----|
|**Nome alternativo da entidade**|
|:-----|
|**Número de série**|
|:-----|
|**Comprimento de chave pública**|
|:-----|
|**Algoritmo de assinatura**|
|:-----|
|**Não antes de validade**|
|:-----|
|**Validade não após**|
|:-----|
|**Identificador de chave de assunto**|
|:-----|
|**Identificador de chave de autoridade**|
|:-----|
|**Impressão digital (SHA-1)**|
|:-----|
|**Impressão digital (SHA-256)**|
|:-----|
|**PIN (SHA-256)**|
|:-----|
|**URLs CRL**|
|:-----|
|**URLs OCSP**|
|:-----|
   
 **Symantec classe 3 servidores seguros CA - G4**
  
||
|:-----|
|**Assunto**|
|:-----|
|**Emissor**|
|:-----|
|**Nome alternativo da entidade**|
|:-----|
|**Número de série**|
|:-----|
|**Comprimento de chave pública**|
|:-----|
|**Algoritmo de assinatura**|
|:-----|
|**Não antes de validade**|
|:-----|
|**Validade não após**|
|:-----|
|**Identificador de chave de assunto**|
|:-----|
|**Identificador de chave de autoridade**|
|:-----|
|**Impressão digital (SHA-1)**|
|:-----|
|**Impressão digital (SHA-256)**|
|:-----|
|**PIN (SHA-256)**|
|:-----|
|**URLs CRL**|
|:-----|
|**URLs OCSP**|
|:-----|
   
 **Thawte SHA256 SSL da autoridade de certificação**
  
||
|:-----|
|**Assunto**|
|:-----|
|**Emissor**|
|:-----|
|**Nome alternativo da entidade**|
|:-----|
|**Número de série**|
|:-----|
|**Comprimento de chave pública**|
|:-----|
|**Algoritmo de assinatura**|
|:-----|
|**Não antes de validade**|
|:-----|
|**Validade não após**|
|:-----|
|**Identificador de chave de assunto**|
|:-----|
|**Identificador de chave de autoridade**|
|:-----|
|**Impressão digital (SHA-1)**|
|:-----|
|**Impressão digital (SHA-256)**|
|:-----|
|**PIN (SHA-256)**|
|:-----|
|**URLs CRL**|
|:-----|
|**URLs OCSP**|
|:-----|
   
 **Verizon Akamai SureServer CA G14-SHA2**
  
||
|:-----|
|**Assunto**|
|:-----|
|**Emissor**|
|:-----|
|**Número de série**|
|:-----|
|**Comprimento de chave pública**|
|:-----|
|**Algoritmo de assinatura**|
|:-----|
|**Não antes de validade**|
|:-----|
|**Validade não após**|
|:-----|
|**Identificador de chave de assunto**|
|:-----|
|**Identificador de chave de autoridade**|
|:-----|
|**Impressão digital (SHA-1)**|
|:-----|
|**Impressão digital (SHA-256)**|
|:-----|
|**PIN (SHA-256)**|
|:-----|
|**URLs AIA**|
|:-----|
|**URLs CRL**|
|:-----|
|**URLs OCSP**|
|:-----|
   
## <a name="additional-certificate-paths"></a>Caminhos de certificado adicional
<a name="IntermediateCerts"> </a>

A seguir incluem certificados herdados que não estão incluídos acima e serão mesclados com a lista acima ao longo do tempo.
  
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



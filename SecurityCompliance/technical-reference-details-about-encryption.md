---
title: Detalhes de referências técnicas sobre a criptografia no Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/12/2018
ms.audience: ITPro
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: 862cbe93-4268-4ef9-ba79-277545ecf221
description: Exibir detalhes técnicos sobre criptografia no Office 365.
ms.openlocfilehash: 69365b66479ab89a9c036fe489b4087d327460eb
ms.sourcegitcommit: e4ebef6aaf756eefb86c9f3a602cf75f5d344271
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026518"
---
# <a name="technical-reference-details-about-encryption-in-office-365"></a>Detalhes de referências técnicas sobre a criptografia no Office 365

Consulte este artigo para saber mais sobre certificados, tecnologias e TLS conjuntos de codificação empregados para [criptografia no Office 365](encryption.md). Este artigo também fornece detalhes sobre reprovações planejadas.
  
- Se você estiver procurando por informações gerais, consulte [criptografia no Office 365](encryption.md).
    
- Se você estiver procurando informações sobre a instalação, consulte [Configure a criptografia no Office 365 Enterprise](set-up-encryption.md).
    
## <a name="microsoft-office-365-certificate-ownership-and-management"></a>Gerenciamento e propriedade de certificado do Microsoft Office 365

Não é necessário comprar nem manter certificados do Office 365, pois a Microsoft usa os próprios certificados.
  
## <a name="current-encryption-standards-and-planned-deprecations"></a>Padrões de criptografia atuais e reprovações planejadas

Para continuar a fornecer melhor classe criptografia para o Office 365, a Microsoft regularmente analisa os padrões de criptografia com suporte. Às vezes, precisamos preterir padrões antigos conforme se tornarem desatualizada e, portanto, menos seguro. Este tópico descreve os conjuntos de codificação com suporte no momento e outros padrões bem como detalhes sobre reprovações planejadas.
  
## <a name="versions-of-tls-supported-by-office-365"></a>Versões do TLS com suporte do Office 365

O TLS e o SSL, que veio antes do TLS, são protocolos de criptografia que protegem a comunicação em uma rede usando certificados de segurança para criptografar uma conexão entre computadores. O Office 365 é compatível com várias versões do TLS, entre elas:
  
- TLS versão 1.2 (TLS 1.2)
    
- TLS versão 1.1 (TLS 1.1)
    
- TLS versão 1.0 (TLS 1.0)
    
 Suporte a TLS 1.0 e TLS 1.1 será preterido 31 de outubro de 2018. Para obter mais informações, consulte o [Deprecating suporte a TLS 1.0 1.1 e o que isso significa para você](technical-reference-details-about-encryption.md#TLS11and12deprecation) . 
  
## <a name="deprecating-support-for-tls-10-and-11-and-what-this-means-for-you"></a>Substituição de suporte a TLS 1.0 1.1 e o que isso significa para você
<a name="TLS11and12deprecation"> </a>

A partir de 31 de outubro de 2018, Office 365 não dará suporte a TLS 1.0 e 1.1. Isso significa que a Microsoft não corrigirá novos problemas são encontrados em clientes, dispositivos ou serviços que se conectam ao Office 365 usando o TLS 1.0 e 1.1.

Observe que isso não significa o que Office 365 bloqueará TLS 1.0 e 1.1 conexões. Não há nenhuma data oficial de desativação ou remoção de TLS 1.0 e 1.1 no serviço de TLS para conexões de cliente. A data final preterir será determinada pela telemetria do cliente e ainda não é conhecida. Depois que for feita uma decisão, haverá um comunicado com antecedência de seis meses, a menos que podemos ficar atento um comprometimento conhecido, caso em que podemos pode precisar agir em menos de seis meses para proteger os clientes que usam os serviços.

Você deve certificar-se de que todas as combinações de cliente-servidor e servidor de navegador usam TLS 1.2 (ou uma versão posterior) para manter a conexão aos serviços do Office 365. Talvez você precise atualizar determinadas combinações de cliente-servidor e servidor de navegador. Para obter informações sobre como isso impacta, consulte [Preparando para o uso obrigatório de TLS 1.2 no Office 365](https://support.microsoft.com/en-us/help/4057306/preparing-for-tls-1-2-in-office-365).
  
## <a name="deprecating-support-for-3des"></a>Substituição de suporte para 3DES
<a name="TLS11and12deprecation"> </a>

A partir de 31 de outubro de 2018, Office 365 não são mais dará suporte o uso de conjuntos de codificação 3DES para comunicação com o Office 365. Mais especificamente, o Office 365 não dará suporte ao conjunto de codificação TLS_RSA_WITH_3DES_EDE_CBC_SHA. Clientes e servidores que se comunicam com O365 após esta data deve oferecer suporte a pelo menos um das codificações mais seguras listados neste tópico (consulte [TLS codificação pacotes suportados pelo Office 365](technical-reference-details-about-encryption.md#TLSCipherSuites)).
  
## <a name="deprecating-sha-1-certificate-support-in-office-365"></a>Substituição do suporte de certificado SHA-1 no Office 365
<a name="TLS11and12deprecation"> </a>

Desde junho de 2016, o Office 365 não são mais aceitas um certificado SHA-1 para conexões de entrada ou saídas. Se estiver no momento usando um certificado com SHA-1 na cadeia de certificados, você precisará atualizar a cadeia para usar SHA-2 (seguro 2 de algoritmo de Hash) ou um algoritmo de hash mais forte.
  
## <a name="deprecating-rc4-support-in-office-365"></a>Substituição do suporte a RC4 no Office 365
<a name="TLS11and12deprecation"> </a>

Em julho de 2015, o suporte aos seguintes conjuntos de codificação RC4 foi interrompido:
  
- TLS_RSA_WITH_RC4_128_SHA
    
- TLS_RSA_WITH_RC4_128_MD5
    
## <a name="deprecating-secure-sockets-layer-ssl-30-support-in-office-365"></a>Substituição de suporte de Secure Sockets Layer (SSL) 3.0 no Office 365
<a name="TLS11and12deprecation"> </a>

Iniciando 1 de dezembro de 2014, Office 365 começou desabilitando o suporte para SSL Secure Sockets Layer () 3.0, o predecessor para TLS. Para obter mais informações, consulte [Security 3009008 comunicado](https://technet.microsoft.com/library/security/3009008.aspx). Para obter instruções sobre como assegurar a clientes estão usando o TLS 1.0 ou superior e para desabilitar o SSL 3.0, consulte [proteção SSL 3.0 vulnerabilidade](http://blogs.office.com/2014/10/29/protecting-ssl-3-0-vulnerability/).
  
## <a name="tls-cipher-suites-supported-by-office-365"></a>Conjuntos de codificação TLS suportados pelo Office 365
<a name="TLSCipherSuites"> </a>

Um conjunto de codificações é uma coleção de algoritmos de criptografia que o TLS usa para estabelecer conexões seguras. Os conjuntos de codificações com suporte no Office 365 são apresentados na tabela a seguir em ordem de eficácia, com o conjunto de criptografia mais eficaz listado primeiro. Quando o Office 365 recebe uma solicitação de conexão, primeiro ele tenta se conectar usando o conjunto de codificações de nível superior e, caso não consiga, tenta o segundo conjunto da lista e assim por diante até o final da lista. Quando o Office 365 envia uma solicitação de conexão para outro servidor, ou para um cliente, o servidor ou o cliente deve escolher o conjunto de codificações ou se o TLS será usado.
  
|**Protocolos**|**Nome do conjunto de codificações**|**Algoritmo de troca de chave/Eficácia**|**Suporte ao protocolo PFS**|**Algoritmo de autenticação/Eficácia**|**Codificação/Eficácia**|
|:-----|:-----|:-----|:-----|:-----|:-----|
|TLS 1.2  <br/> |TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA384_P384  <br/> |ECDH/192  <br/> |Sim  <br/> |RSA/112  <br/> |AES/256  <br/> |
|TLS 1.2  <br/> |TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA256_P256  <br/> |ECDH/128  <br/> |Sim  <br/> |RSA/112  <br/> |AES/128  <br/> |
|TLS 1.0, 1.1, 1.2  <br/> |TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA_P384  <br/> |ECDH/192  <br/> |Sim  <br/> |RSA/112  <br/> |AES/256  <br/> |
|TLS 1.0, 1.1, 1.2  <br/> |TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA_P256  <br/> |ECDH/128  <br/> |Sim  <br/> |RSA/112  <br/> |AES/128  <br/> |
|TLS 1.2  <br/> |TLS_RSA_WITH_AES_256_CBC_SHA256  <br/> |RSA/112  <br/> |Não  <br/> |RSA/112  <br/> |AES/256  <br/> |
|TLS 1.2  <br/> |TLS_RSA_WITH_AES_128_CBC_SHA256  <br/> |RSA/112  <br/> |Não  <br/> |RSA/112  <br/> |AES/128  <br/> |
|TLS 1.0, 1.1, 1.2  <br/> |TLS_RSA_WITH_AES_256_CBC_SHA  <br/> |RSA/112  <br/> |Não  <br/> |RSA/112  <br/> |AES/256  <br/> |
|TLS 1.0, 1.1, 1.2  <br/> |TLS_RSA_WITH_AES_128_CBC_SHA  <br/> |RSA/112  <br/> |Não  <br/> |RSA/112  <br/> |AES/128  <br/> |
|TLS 1.0, 1.1, 1.2  <br/> |TLS_RSA_WITH_3DES_EDE_CBC_SHA  <br/> |RSA/112  <br/> |Não  <br/> |RSA/112  <br/> |3DES/192  <br/> |
   
## <a name="related-topics"></a>Tópicos relacionados
<a name="TLSCipherSuites"> </a>

[Criptografia no Office 365](encryption.md)
  
[Configure a criptografia no Office 365 Enterprise](set-up-encryption.md)
  
[Implementação de Schannel de TLS 1.0 na atualização de status de segurança do Windows: 24 de novembro de 2015](https://support.microsoft.com/kb/3117336)
  
[Aperfeiçoamentos de criptografia TLS/SSL (Windows IT Center)](https://technet.microsoft.com/en-us/library/cc766285%28v=ws.10%29.aspx)
  


---
title: Como o Exchange Online protege seus segredos de email
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/24/2018
ms.audience: ITPro
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 989ba10c-f73f-4efb-ad1b-af3322e5f376
description: Além do centro do Office 365 confiar que fornece informações de conformidade, de privacidade e de segurança para o Office 365, talvez você queira saber como o Office 365 ajuda a protege segredos você fornecer em seus centros de dados. Usamos uma tecnologia chamada Gerenciador de chave distribuído (DKM).
ms.openlocfilehash: a8fe1a2c9393958a391ec69a9a476a06de8c7576
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524579"
---
# <a name="how-exchange-online-secures-your-email-secrets"></a><span data-ttu-id="c42b8-104">Como o Exchange Online protege seus segredos de email</span><span class="sxs-lookup"><span data-stu-id="c42b8-104">How Exchange Online secures your email secrets</span></span>

<span data-ttu-id="c42b8-105">Este artigo descreve como a Microsoft protege seus segredos de email em seus datacenters.</span><span class="sxs-lookup"><span data-stu-id="c42b8-105">This article describes how Microsoft secures your email secrets in its datacenters.</span></span>
  
## <a name="how-do-we-secure-secret-information-provided-by-you"></a><span data-ttu-id="c42b8-106">Como protegemos as informações secretas fornecidas por você?</span><span class="sxs-lookup"><span data-stu-id="c42b8-106">How do we secure secret information provided by you?</span></span>

<span data-ttu-id="c42b8-p102">Além do centro do Office 365 confiar que fornece [segurança, privacidade e informações de conformidade para o Office 365](https://go.microsoft.com/fwlink/?linkid=874644), talvez você queira saber como o Office 365 ajuda a protege segredos você fornecer em seus centros de dados. Usamos uma tecnologia chamada Gerenciador de chave distribuído (DKM).</span><span class="sxs-lookup"><span data-stu-id="c42b8-p102">In addition to the Office 365 Trust Center which provides [Security, Privacy and Compliance Information for Office 365](https://go.microsoft.com/fwlink/?linkid=874644), you might want to know how Office 365 helps protects secrets you provide in its datacenters. We use a technology called Distributed Key Manager (DKM).</span></span>
  
<span data-ttu-id="c42b8-p103">O Distributed Key Manager (DKM) é uma funcionalidade no lado do cliente que usa um conjunto de chaves secretas para criptografar e descriptografar informações. Somente os membros de um grupo de segurança específico nos Serviços de Domínio Active Directory podem acessar essas chaves para descriptografar os dados criptografados pelo DKM. No Exchange Online, apenas certas contas de serviço, sob as quais os processos do Exchange são executados, fazem parte do grupo de segurança. Como parte do procedimento operacional padrão no datacenter, nenhum humano recebe credenciais que fazem parte deste grupo de segurança e, portanto, nenhuma pessoa tem acesso às chaves que podem descriptografar esses segredos.</span><span class="sxs-lookup"><span data-stu-id="c42b8-p103">Distributed Key Manager (DKM) is a client-side functionality that uses a set of secret keys to encrypt and decrypt information. Only members of a specific security group in Active Directory Domain Services can access those keys in order to decrypt the data that is encrypted by DKM. In Exchange Online, only certain service accounts under which the Exchange processes run are part of that security group. As part of standard operating procedure in the datacenter, no human is given credentials that are part of this security group and therefore no human has access to the keys that can decrypt these secrets.</span></span>
  
<span data-ttu-id="c42b8-p104">Para fins de depuração, solução de problemas ou auditoria, um administrador de datacenter deve solicitar acesso elevado para obter credenciais temporárias que fazem parte do grupo de segurança. Esse processo requer vários níveis de aprovação legal. Se o acesso for concedido, toda as atividades são registradas e auditadas. Além disso, o acesso é concedido apenas por um tempo definido, expirando automaticamente após esse período.</span><span class="sxs-lookup"><span data-stu-id="c42b8-p104">For debugging, troubleshooting, or auditing purposes, a datacenter administrator must request elevated access to gain temporary credentials that are part of the security group. This process requires multiple levels of legal approval. If access is granted, all activity is logged and audited. In addition access is only granted for a set interval of time after which it automatically expires.</span></span>
  
<span data-ttu-id="c42b8-p105">Para maior proteção, a tecnologia do DKM inclui a sobreposição de chave e o arquivamento automatizados. Isso também garante que você pode continuar acessando seu conteúdo antigo sem depender da mesma chave indefinidamente.
</span><span class="sxs-lookup"><span data-stu-id="c42b8-p105">For extra protection, DKM technology includes automated key rollover and archiving. This also ensures that you can continue to access your older content without having to rely on the same key indefinitely.</span></span>
  
## <a name="where-does-exchange-online-make-use-of-dkm"></a><span data-ttu-id="c42b8-119">Em que circunstâncias o Exchange Online usa o DKM?</span><span class="sxs-lookup"><span data-stu-id="c42b8-119">Where does Exchange Online make use of DKM?</span></span>

<span data-ttu-id="c42b8-p106">A Microsoft usa o DKM para criptografar seus segredos nos datacenters do Exchange Online. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="c42b8-p106">Microsoft uses DKM to encrypt your secrets in Exchange Online datacenters. For example:</span></span>
  
- <span data-ttu-id="c42b8-p107">Credenciais de conta de email para contas conectadas. As contas conectadas são as contas de email de terceiros, como Hotmail, Gmail e Yahoo!.</span><span class="sxs-lookup"><span data-stu-id="c42b8-p107">Email account credentials for connected accounts. Connected accounts are third-party accounts such as Hotmail, Gmail, and Yahoo! mail accounts.</span></span>
    
- <span data-ttu-id="c42b8-p108">Chaves de raiz de (RMS) do serviço de gerenciamento de direitos. Estas são as chaves de cliente são que uma importados a partir de RMS do Windows Azure ou implantações de RMS de serviços do Active Directory domínio de locais do cliente que são usadas para criptografia e descriptografia de emails com RMS ou Office 365 Message Encryption (OME).</span><span class="sxs-lookup"><span data-stu-id="c42b8-p108">Rights Management service (RMS) root keys. These are customer keys that are either imported from Azure RMS or from customer's on-premises Active Directory Domain Services RMS deployments that are used for encrypting and decrypting emails with RMS or Office 365 Message Encryption (OME).</span></span>
    
## <a name="related-topics"></a><span data-ttu-id="c42b8-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c42b8-127">Related topics</span></span>

[<span data-ttu-id="c42b8-128">Criptografia no Office 365</span><span class="sxs-lookup"><span data-stu-id="c42b8-128">Encryption in Office 365</span></span>](encryption.md)
  
[<span data-ttu-id="c42b8-129">Detalhes de referências técnicas sobre a criptografia no Office 365</span><span class="sxs-lookup"><span data-stu-id="c42b8-129">Technical reference details about encryption in Office 365</span></span>](technical-reference-details-about-encryption.md)
  
[<span data-ttu-id="c42b8-130">Pessoal assurance no Office 365 Security &amp; Centro de conformidade</span><span class="sxs-lookup"><span data-stu-id="c42b8-130">Service assurance in the Office 365 Security &amp; Compliance Center</span></span>](https://go.microsoft.com/fwlink/?linkid=874645)
  


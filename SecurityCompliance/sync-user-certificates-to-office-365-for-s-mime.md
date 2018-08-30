---
title: Sincronizar certificados de usuário com o Office 365 para S/MIME
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 351c932e-99c1-4512-a6e8-788e90b7838f
description: Antes que alguém possa enviar mensagens protegidas por S/MIME, os certificados adequados deverão ser configurados. Para enviar mensagens criptografadas por meio do Exchange Online, o programa de email do destinatário usa o certificado público do destinatário para criptografar a mensagem. Este certificado X.509 público deve ser publicado no Office 365.
ms.openlocfilehash: 452b538b4515bdbcd5fcbdedad17f0450c04207a
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002360"
---
# <a name="sync-user-certificates-to-office-365-for-smime"></a><span data-ttu-id="44b22-105">Sincronizar certificados de usuário com o Office 365 para S/MIME</span><span class="sxs-lookup"><span data-stu-id="44b22-105">Sync user certificates to Office 365 for S/MIME</span></span>

<span data-ttu-id="44b22-p102">Antes que alguém possa enviar mensagens protegidas por S/MIME, os certificados adequados deverão ser configurados. Para enviar mensagens criptografadas por meio do Exchange Online, o programa de email do destinatário usa o certificado público do destinatário para criptografar a mensagem. Este certificado X.509 público deve ser publicado no Office 365.</span><span class="sxs-lookup"><span data-stu-id="44b22-p102">Before anyone can send S/MIME-protected messages, the appropriate certificates must be set up. In order to send encrypted messages through Exchange Online, the sender's email program uses the public certificate of the recipient to encrypt the message. This public X.509 certificate has to be published to Office 365.</span></span>
  
## <a name="to-sync-certificates-that-support-smime"></a><span data-ttu-id="44b22-109">Para sincronizar certificados que dão suporte a S/MIME</span><span class="sxs-lookup"><span data-stu-id="44b22-109">To Sync certificates that support S/MIME</span></span>

<span data-ttu-id="44b22-p103">Comece a configurar o S/MIME emitindo certificados e publicando-os em seu Serviço de domínio do Active Directory. Para obter mais informações sobre o gerenciamento de certificados no Exchange 2013, consulte [Digital Certificates and SSL](http://technet.microsoft.com/library/a9e2e08c-d46a-4135-a387-eb653212b676.aspx).</span><span class="sxs-lookup"><span data-stu-id="44b22-p103">Begin setting up S/MIME by issuing certificates and publishing them in your local Active Directory Domain Service. For more information about managing certificates in Exchange 2013, see [Digital Certificates and SSL](http://technet.microsoft.com/library/a9e2e08c-d46a-4135-a387-eb653212b676.aspx).</span></span>
  
<span data-ttu-id="44b22-p104">Depois que os certificados são publicados, use a ferramenta de sincronização do Azure Active Directory para sincronizar dados do usuário do seu ambiente do Exchange no local para o Office 365. Para obter mais informações sobre esse processo, consulte [DirSync: o histórico de versão do Directory Sync ferramenta versão](https://go.microsoft.com/fwlink/p/?LinkId=392587).</span><span class="sxs-lookup"><span data-stu-id="44b22-p104">After your certificates are published, use the Azure Active Directory Sync tool to synchronize user data from your on-premises Exchange environment to Office 365. For more information on this process, see [DirSync: Directory Sync Tool Version Release History](https://go.microsoft.com/fwlink/p/?LinkId=392587).</span></span>
  
<span data-ttu-id="44b22-114">Além de sincronizar outros dados de diretório, para fins de S/MIME, a ferramenta sincronizará os atributos  `userCertificate` e  `userSMIMECertificate` para cada objeto de usuário, de forma que os dados possam ser usados para assinar e criptografar mensagens.</span><span class="sxs-lookup"><span data-stu-id="44b22-114">Along with synchronizing other directory data, for S/MIME purposes, the tool will synchronize the  `userCertificate` and  `userSMIMECertificate` attributes for each user object so the data can be used to sign and encrypt messages.</span></span> 
  
## <a name="more-information"></a><span data-ttu-id="44b22-115">Mais informações</span><span class="sxs-lookup"><span data-stu-id="44b22-115">More Information</span></span>

[<span data-ttu-id="44b22-116">S/MIME para assinatura e criptografia de mensagens</span><span class="sxs-lookup"><span data-stu-id="44b22-116">S/MIME for message signing and encryption</span></span>](s-mime-for-message-signing-and-encryption.md)
  
[<span data-ttu-id="44b22-117">Ferramenta de Sincronização do Microsoft Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="44b22-117">Azure Active Directory Sync tool</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=392587)
  


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
ms.assetid: 351c932e-99c1-4512-a6e8-788e90b7838f
description: Antes que alguém possa enviar mensagens protegidas por S/MIME, os certificados adequados deverão ser configurados. Para enviar mensagens criptografadas por meio do Exchange Online, o programa de email do destinatário usa o certificado público do destinatário para criptografar a mensagem. Este certificado X.509 público deve ser publicado no Office 365.
ms.openlocfilehash: aa94dfa6702a25b3fc6b8b883daceddf31d2f66a
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026188"
---
# <a name="sync-user-certificates-to-office-365-for-smime"></a>Sincronizar certificados de usuário com o Office 365 para S/MIME

Antes que alguém possa enviar mensagens protegidas por S/MIME, os certificados adequados deverão ser configurados. Para enviar mensagens criptografadas por meio do Exchange Online, o programa de email do destinatário usa o certificado público do destinatário para criptografar a mensagem. Este certificado X.509 público deve ser publicado no Office 365.
  
## <a name="to-sync-certificates-that-support-smime"></a>Para sincronizar certificados que dão suporte a S/MIME

Comece a configurar o S/MIME emitindo certificados e publicando-os em seu Serviço de domínio do Active Directory. Para obter mais informações sobre o gerenciamento de certificados no Exchange 2013, consulte [Digital Certificates and SSL](http://technet.microsoft.com/library/a9e2e08c-d46a-4135-a387-eb653212b676.aspx).
  
Depois que os certificados são publicados, use a ferramenta de sincronização do Azure Active Directory para sincronizar dados do usuário do seu ambiente do Exchange no local para o Office 365. Para obter mais informações sobre esse processo, consulte [DirSync: o histórico de versão do Directory Sync ferramenta versão](https://go.microsoft.com/fwlink/p/?LinkId=392587).
  
Além de sincronizar outros dados de diretório, para fins de S/MIME, a ferramenta sincronizará os atributos  `userCertificate` e  `userSMIMECertificate` para cada objeto de usuário, de forma que os dados possam ser usados para assinar e criptografar mensagens. 
  
## <a name="more-information"></a>Mais informações

[S/MIME para assinatura e criptografia](s-mime-for-message-signing-and-encryption.md)
  
[Ferramenta de Sincronização do Microsoft Azure Active Directory](https://go.microsoft.com/fwlink/p/?LinkId=392587)
  


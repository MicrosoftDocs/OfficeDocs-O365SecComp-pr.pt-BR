---
title: S/MIME para assinatura e criptografia de mensagens
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 887c710b-0ec6-4ff0-8065-5f05f74afef3
description: S/MIME permite criptografar emails e assinar digitalmente-los. Quando você usa o S/MIME com uma mensagem de email, ele ajuda as pessoas que recebem a mensagem, para certificar-se de que ele vê em suas caixas de entrada é a mensagem exata iniciados com o remetente.
ms.openlocfilehash: 3ce95132476417df8949cdc12f2d825047f6b76d
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027588"
---
# <a name="smime-for-message-signing-and-encryption"></a>S/MIME para assinatura e criptografia de mensagens

S/MIME (Secure/Multipurpose Internet Mail Extensions) é um método amplamente aceito, ou mais precisamente um protocolo, para o envio de mensagens assinadas e criptografadas digitalmente. S/MIME permite que você criptografe email e os assine digitalmente. Quando você usa S/MIME com uma mensagem de email, isso ajuda as pessoas que recebem essa mensagem a ter certeza de que o que veem em suas caixas de entrada é a mensagem exata que partiu do remetente. Isso também ajudará as pessoas que receberem mensagens a terem certeza de que a mensagem veio do remetente específico e não de alguém fingindo ser o remetente. Para fazer isso, S/MIME presta serviços de segurança criptográfica como autenticação, integridade da mensagem e não recusa da origem (usando assinaturas digitais). Isso também ajuda a melhorar a privacidade e a segurança dos dados (usando criptografia) para mensagens eletrônicas. Para obter informações mais completas sobre o histórico e a arquitetura de S/MIME no contexto de email, consulte [Compreendendo S/MIME](https://go.microsoft.com/fwlink/?LinkID=393948). 
  
Como administrador, você pode habilitar a segurança baseada em S/MIME para sua organização se você tiver caixas de correio em Exchange 2013 SP1 ou Exchange Online, uma parte do Office 365. Use a orientação nos tópicos vinculados aqui junto com o Shell de Gerenciamento do Exchange para configurar S/MIME. Para usar o S/MIME em versões suportadas do Outlook ou ActiveSync, com Exchange 2013 SP1 ou Exchange Online, os usuários em sua organização devem ter certificados emitidos para fins de assinatura e criptografia e dados publicados em seu Serviços de Domínio Active Directory (AD DS) local. Seu AD DS deve estar localizado em computadores em um local físico que você controla e não em uma instalação remota ou serviço baseado em nuvem em algum lugar na internet. Para obter mais informações sobre o AD DS, consulte [Serviços de Domínio Active Directory](https://go.microsoft.com/fwlink/?LinkID=394064).
  
## <a name="supported-scenarios-and-technical-considerations"></a>Cenários suportados e considerações técnicas
<a name="sectionSection0"> </a>

Se sua organização usa Exchange 2013 SP1 ou Exchange Online, você pode configurar o S/MIME para funcionar com qualquer um dos seguintes pontos finais: 
  
- Outlook 2010
    
- Outlook 2013
    
- Outlook Web App
    
- Exchange ActiveSync (EAS)
    
Os passos que você seguir para configurar S/MIME com cada um desses pontos finais são um pouco diferentes dependendo de quais você escolher. Geralmente, você precisará realizar o seguinte:
  
- Instale uma autoridade de certificação com base no Windows e configure uma infraestrutura de chave pública para emitir certificados S/MIME. Também há suporte para certificados emitidos por provedores de certificados de terceiros. Para obter detalhes, consulte [Visão Geral dos Serviços de Certificados do Active Directory](https://technet.microsoft.com/library/hh831740.aspx).
    
- Publicar o certificado de usuário em uma conta AD DS local nos atributos UserSMIMECertificate e/ou UserCertificate.
    
- Para organizações do Exchange Online, sincronize os certificados de usuário de AD DS para Active Directory do Azure usando uma versão apropriada de DirSync. Em seguida, esses certificados serão sincronizados do Active Directory do Azure para o diretório do Exchange Online e serão usados ao criptografar uma mensagem para um destinatário.
    
- Configurar uma coletânea de certificados virtuais para validar S/MIME. Essas informações são usadas pelo OWA ao validar a assinatura de um email e garantir que ele foi assinado por um certificado confiável.
    
- Configurar o ponto final do Outlook ou EAS para usar S/MIME. 
    
## <a name="setup-smime-with-outlook-web-app"></a>Configurar S/MIME com Outlook Web App
<a name="sectionSection1"> </a>

A configuração do S/MIME para Exchange 2013 SP1 ou Exchange Online com o Outlook Web App envolve as seguintes etapas principais:
  
1. [Definir configurações de S/MIME para o Outlook Web App](configure-s-mime-settings-for-outlook-web-app.md)
    
2. [Configurar coleção de certificados virtuais para validar S/MIME](set-up-virtual-certificate-collection-to-validate-s-mime.md)
    
3. [Sincronizar certificados de usuário para o Office 365 para S/MIME](sync-user-certificates-to-office-365-for-s-mime.md) Esta etapa somente se aplica ao Exchange Online. 
    
## <a name="related-message-encryption-technologies"></a>Tecnologias de criptografia de mensagem relacionadas
<a name="sectionSection2"> </a>

À medida que a segurança de mensagens se torna mais importante, os administradores precisam compreender os princípios e os conceitos de um sistema de mensagens seguro. Essa compreensão é especialmente importante por causa da crescente variedade de tecnologias relacionadas à proteção, como S/MIME, que se tornaram disponíveis. Para compreender mais sobre S/MIME e como ele funciona no contexto de email, consulte [Compreendendo S/MIME](https://go.microsoft.com/fwlink/?LinkID=393948). Várias tecnologias de criptografia trabalham em conjunto para oferecer proteção para mensagens em repouso ou em trânsito. O S/MIME pode trabalhar simultaneamente com as seguintes tecnologias, mas não depende delas:
  
> O **Transport Layer Security (TLS)** criptografa o túnel ou a rota entre servidores de email para ajudar a impedir a interceptação e a escuta não autorizada. 
    
> O **Secure Sockets Layer (SSL)** criptografa a conexão entre clientes de email e servidores do Office 365. 
    
> O **BitLocker** criptografa os dados em um disco rígido de um datacenter, de forma que se alguém obtiver acesso não autorizado, não poderá lê-lo. 
    
### <a name="smime-compared-with-office-365-message-encryption"></a>S/MIME em comparação com o Office 365 Message Encryption

S/MIME requer uma infraestrutura de certificado e publicação que é geralmente usada em situações entre empresas e entre empresas e consumidores. O usuário controla as chaves criptográficas no S/MIME e pode escolher se as usará para cada mensagem que enviar. Programas de email como o Outlook procuram um local de autoridade de certificado raiz confiável para realizar a assinatura digital e a verificação da assinatura. O Office 365 Message Encryption é um serviço de criptografia baseado em políticas que pode ser configurado por um administrador, e não um usuário individual, para criptografar email enviado a qualquer pessoa dentro ou fora da organização. É um serviço online que é desenvolvido no Azure Rights Management (RMS) e não conta com uma infraestrutura de chave pública. O Office 365 Message Encryption também oferece recursos adicionais, como o recurso para personalizar o email com a marca da organização. Para obter mais informações sobre o Office 365 Message Encryption, consulte [Office 365 Message Encryption ](https://go.microsoft.com/fwlink/?LinkID=392525).
  
## <a name="more-information"></a>Mais informações
<a name="sectionSection3"> </a>

[Outlook Web App](http://technet.microsoft.com/library/3814b665-01e8-4881-9a44-163f14789ee4.aspx)
  
[Email Seguro (2000)](https://technet.microsoft.com/en-us/library/cc962043.aspx)
  


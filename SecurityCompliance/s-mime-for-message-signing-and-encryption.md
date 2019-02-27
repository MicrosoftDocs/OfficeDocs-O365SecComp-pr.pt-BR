---
title: S/MIME para assinatura e criptografia de mensagens no Exchange Online
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 887c710b-0ec6-4ff0-8065-5f05f74afef3
description: Os administradores podem saber mais sobre como usar S/MIME no Exchange Online.
ms.openlocfilehash: 163ae5686adf934f07ee26717fa0b4998ddf3363
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296794"
---
# <a name="smime-for-message-signing-and-encryption-in-exchange-online"></a>S/MIME para assinatura e criptografia de mensagens no Exchange Online

S/MIME (Secure/Multipurpose Internet Mail Extensions) é um método amplamente aceito (ou mais precisamente, um protocolo) para enviar mensagens assinadas digitalmente e criptografadas. O S/MIME permite criptografar emails e assiná-los digitalmente. Quando você usa S/MIME com uma mensagem de email, ele ajuda as pessoas que recebem essa mensagem a certificar-se de que elas vejam na caixa de entrada são a mensagem exata que começou com o remetente. Também ajudará as pessoas que recebem mensagens a ter certeza de que a mensagem provém do remetente específico e não de alguém fingindo ser o remetente. Para fazer isso, o S/MIME fornece serviços de segurança de criptografia, como autenticação, integridade de mensagens e não repudiação de origem (usando assinaturas digitais). Também ajuda a aprimorar a privacidade e a segurança de dados (usando criptografia) para mensagens eletrônicas. Para obter um plano de fundo mais completo sobre o histórico e a arquitetura do S/MIME no contexto de email, consulte underStanding [s/MIME](https://go.microsoft.com/fwlink/?LinkID=393948).

Como administrador do Exchange Online, você pode habilitar a segurança baseada em S/MIME para as caixas de correio em sua organização. Use as orientações nos tópicos vinculados aqui, juntamente com o PowerShell do Exchange Online para configurar o S/MIME. Para usar S/MIME em clientes de email suportados, os usuários em sua organização devem ter certificados emitidos para assinatura e criptografia e dados publicados no serviço de domínio do Active Directory (AD DS) local. Seu AD DS deve estar localizado em computadores em um local físico que você controla e não em uma instalação remota ou em um serviço baseado em nuvem na Internet. Para obter mais informações sobre o AD DS, consulte [Active Directory Domain Services](https://go.microsoft.com/fwlink/?LinkID=394064).

## <a name="supported-scenarios-and-technical-considerations"></a>Cenários suportados e considerações técnicas

Você pode configurar o S/MIME para funcionar com qualquer um dos seguintes pontos de extremidade:

- Outlook 2010 ou posterior

- Outlook na Web (anteriormente conhecido como Outlook Web App)

- Exchange ActiveSync (EAS)

As etapas a seguir para configurar o S/MIME com cada um desses pontos de extremidade são um pouco diferentes. Geralmente, será necessário executar as seguintes etapas:

- Instale uma autoridade de certificação com base no Windows e configure uma infraestrutura de chave pública para emitir certificados S/MIME. Também há suporte para certificados emitidos por provedores de certificados de terceiros. Para obter detalhes, consulte [Visão Geral dos Serviços de Certificados do Active Directory](https://technet.microsoft.com/library/hh831740.aspx).

- Publique o certificado de usuário em uma conta do AD DS local nos atributos **UserSMIMECertificate** e/ou **** userCertificate.

- Para organizações do Exchange Online, sincronize os certificados de usuário de AD DS para Active Directory do Azure usando uma versão apropriada de DirSync. Em seguida, esses certificados serão sincronizados do Active Directory do Azure para o diretório do Exchange Online e serão usados ao criptografar uma mensagem para um destinatário.

- Configurar uma coleção de certificados virtuais para validar S/MIME. Essas informações são usadas pelo Outlook na Web ao validar a assinatura de um email e garantir que ele tenha sido assinado por um certificado confiável.

- Configurar o ponto final do Outlook ou EAS para usar S/MIME.

## <a name="setup-smime-with-outlook-on-the-web"></a>Configurar S/MIME com o Outlook na Web

A configuração do S/MIME para o Exchange Online com o Outlook na Web envolve as seguintes etapas principais:

1. [Configurar definições S/MIME para o Outlook na Web](configure-s-mime-settings-for-outlook-web-app.md)

2. [Configurar coleção de certificados virtuais para validar S/MIME](set-up-virtual-certificate-collection-to-validate-s-mime.md)

3. [Sincronizar certificados de usuário com o Office 365 para S/MIME](sync-user-certificates-to-office-365-for-s-mime.md)

## <a name="related-message-encryption-technologies"></a>Tecnologias de criptografia de mensagem relacionadas

À medida que a segurança da mensagem se torna mais importante, os administradores precisam compreender os princípios e os conceitos de mensagens seguras. Essa compreensão é especialmente importante devido à crescente variedade de tecnologias relacionadas à proteção (incluindo S/MIME) que estão disponíveis. Para entender mais sobre S/MIME e como ele funciona no contexto de email, consulte [UnderstandIng S/MIME](https://go.microsoft.com/fwlink/?LinkID=393948). Uma variedade de tecnologias de criptografia trabalham juntas para fornecer proteção para mensagens em repouso e em trânsito. O S/MIME pode funcionar simultaneamente com as seguintes tecnologias, mas não depende delas:

- O **Transport Layer Security (TLS)** criptografa o túnel ou a rota entre servidores de email para ajudar a impedir a interceptação e a escuta não autorizada.

- O **Secure Sockets Layer (SSL)** criptografa a conexão entre clientes de email e servidores do Office 365.

- O **BitLocker** criptografa os dados em um disco rígido de um datacenter, de forma que se alguém obtiver acesso não autorizado, não poderá lê-lo.

### <a name="smime-compared-with-office-365-message-encryption"></a>S/MIME em comparação com o Office 365 Message Encryption

S/MIME requer uma infraestrutura de certificado e publicação que é geralmente usada em situações entre empresas e entre empresas e consumidores. O usuário controla as chaves criptográficas no S/MIME e pode escolher se as usará para cada mensagem que enviar. Programas de email como o Outlook procuram um local de autoridade de certificado raiz confiável para realizar a assinatura digital e a verificação da assinatura. O Office 365 Message Encryption é um serviço de criptografia baseado em políticas que pode ser configurado por um administrador, e não um usuário individual, para criptografar email enviado a qualquer pessoa dentro ou fora da organização. É um serviço online que é desenvolvido no Azure Rights Management (RMS) e não conta com uma infraestrutura de chave pública. O Office 365 Message Encryption também oferece recursos adicionais, como o recurso para personalizar o email com a marca da organização. Para obter mais informações sobre o Office 365 Message Encryption, consulte [Office 365 Message Encryption ](https://go.microsoft.com/fwlink/?LinkID=392525).

## <a name="more-information"></a>Mais informações

[Outlook na Web](http://technet.microsoft.com/library/3814b665-01e8-4881-9a44-163f14789ee4.aspx)

[Email Seguro (2000)](https://technet.microsoft.com/en-us/library/cc962043.aspx)

---
title: Como o Exchange Online usa o TLS para proteger conexões de email no Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 8/2/2018
ms.audience: ITPro
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: 4cde0cda-3430-4dc0-b489-f2c0736c929f
description: Saiba como o Exchange Online e o Office 365 usarem segurança de camada de transporte (TLS) e encaminhar sigilo (FS) para proteger as comunicações de email. Também Obtenha informações sobre o certificado emitido pela Microsoft para Exchange Online.
ms.openlocfilehash: 079a6f574838f5710dbbbcb53726799abfae1d3a
ms.sourcegitcommit: ddfa0ac1f8ef95a78dcc1468241ef29363d56b5b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/30/2018
ms.locfileid: "23520140"
---
# <a name="how-exchange-online-uses-tls-to-secure-email-connections-in-office-365"></a>Como o Exchange Online usa o TLS para proteger conexões de email no Office 365

Saiba como o Exchange Online e o Office 365 usarem segurança de camada de transporte (TLS) e encaminhar sigilo (FS) para proteger as comunicações de email. Também fornece informações sobre o certificado emitido pela Microsoft para Exchange Online.
  
## <a name="tls-basics-for-office-365-and-exchange-online"></a>Noções básicas do TLS para o Office 365 e o Exchange Online

Segurança de camada de transporte (TLS) e SSL que vem antes de TLS, são protocolos de criptografia que protegem a comunicação por uma rede por meio de certificados de segurança para criptografar uma conexão entre computadores. TLS substitui o Secure Sockets Layer (SSL) e geralmente é conhecida como SSL 3.1. Para o Exchange Online, usamos o TLS para criptografar as conexões entre nossos servidores do Exchange e as conexões entre nossos servidores Exchange e outros servidores como seus servidores do Exchange no local ou servidores de email dos seus destinatários. Depois que a conexão é criptografada, todos os dados enviados por meio dessa conexão é enviada pelo canal criptografado. No entanto, se você encaminhar uma mensagem que foi enviada por meio de uma conexão criptografadas por TLS, mensagem não é necessariamente criptografada. Isso acontece porque, em termos simples, o TLS não criptografar a mensagem, apenas a conexão.
  
Caso pretenda criptografar a mensagem, você deve usar uma tecnologia de criptografia adequada para criptografar conteúdo de mensagens; por exemplo, algo como o recurso Criptografia de Mensagens do Office. Confira [Email encryption in Office 365](email-encryption.md) e [Office 365 Message Encryption (OME)](ome.md) para saber mais sobre as opções de criptografia de mensagens no Office 365. 
  
É recomendável usar o TLS em situações em que você deseja configurar um canal seguro de correspondência entre o Office 365 e sua organização local ou outra organização, como um parceiro. O Exchange Online sempre tenta usar TLS primeiro para proteger seu email, mas não pode fazer isto sempre se a outra parte não oferece segurança TLS. Continue lendo para descobrir como você pode proteger todas as mensagens para os servidores de local ou os parceiros importantes usando *conectores*. 
  
## <a name="how-exchange-online-uses-tls-between-exchange-online-customers"></a>Como o Exchange Online usa o TLS entre clientes do Exchange Online

Os servidores do Exchange Online sempre criptografam conexões com outros servidores do Exchange Online em nossos data centers com TLS 1.2. Quando você envia um email para um destinatário que está dentro da sua organização do Office 365, esse email é enviado automaticamente através de uma conexão criptografada usando TLS. Além disso, todos os emails enviados para outros clientes do Office 365 são enviados através de conexões criptografadas com TLS e protegidos por FS.
  
## <a name="how-office-365-uses-tls-between-office-365-and-external-trusted-partners"></a>Como o Office 365 usa TLS entre o Office 365 e parceiros externos e confiáveis

Por padrão, o Exchange Online sempre usa TLS oportunista. Isso significa que o Exchange Online sempre tenta criptografar conexões com a versão mais segura do TLS pela primeira vez, em seguida, aprofundando para baixo na lista de TLS codificações até encontrar uma em que as duas partes podem concordem. A menos que você configurou o Exchange Online para garantir que as mensagens que o destinatário são enviadas apenas por meio de conexões seguras, em seguida, por padrão a mensagem será enviada sem criptografia se a organização do destinatário não oferecer suporte à criptografia TLS. TLS oportunista é suficiente para a maioria das empresas. No entanto, for business que tenham requisitos de conformidade, como o médico, bancários ou organizações governamentais, você pode configurar o Exchange Online para exigir ou forçar o TLS. Para obter instruções, consulte [Configurar o fluxo de email usando conectores no Office 365](https://technet.microsoft.com/library/ms.exch.eac.connectorselection%28v=exchg.150%29.aspx).
  
Se você decidir configurar o TLS entre sua organização e uma organização parceira confiável, o Exchange Online pode usar TLS forçado para criar confiáveis canais de comunicação. TLS forçado requer a sua organização parceira se autentiquem no Exchange Online com um certificado de segurança para enviar emails para você. Seu parceiro precisará gerenciar seus próprios certificados para fazer isso. No Exchange Online, usamos conectores para proteger as mensagens enviadas de acesso não autorizado antes que elas cheguem ao provedor de email do destinatário. Para obter informações sobre como usar conectores para configurar o fluxo de emails, consulte [Configurar o fluxo de email usando conectores no Office 365](https://technet.microsoft.com/library/ms.exch.eac.connectorselection%28v=exchg.150%29.aspx).
  
## <a name="tls-and-hybrid-exchange-server-deployments"></a>TLS e implantações híbridas do Exchange Server

Se você estiver gerenciando uma implantação híbrida do Exchange, suas necessidades de servidor do Exchange local para autenticar para o Office 365 usando um certificado de segurança para enviar email para destinatários cujas caixas de correio são apenas no Office 365. Como resultado, você precisa gerenciar seus próprios certificados de segurança para os servidores do Exchange local. Você deve também com segurança armazenar e manter esses certificados de servidor. Para obter mais informações sobre o gerenciamento de certificados em implantações híbridas, consulte [requisitos de certificado para implantações híbridas](https://technet.microsoft.com/library/hh563848%28v=exchg.150%29.aspx).
  
## <a name="how-to-set-up-forced-tls-for-exchange-online-in-office-365"></a>Como configurar o TLS Forçado para Exchange Online no Office 365

Para clientes do Exchange Online, na ordem para TLS forçado funcionar para proteger todos os seus e-mails enviados e recebidos, você precisará configurar mais de um conector que requer o TLS. Você precisará de um conector para emails enviados para suas caixas de correio do usuário e outro conector para emails enviados a partir de suas caixas de correio do usuário. Crie esses conectores no Centro de administração do Exchange no Office 365. Para obter instruções, consulte [Configurar o fluxo de email usando conectores no Office 365](https://technet.microsoft.com/library/ms.exch.eac.connectorselection%28v=exchg.150%29.aspx).
  
## <a name="tls-certificate-information-for-exchange-online"></a>Informações do certificado TLS para o Exchange Online

As informações do certificado usadas pelo Exchange Online são descritas na tabela a seguir. Se seu parceiro de negócios está configurando o TLS forçado no seu servidor de email, você precisará fornecer essas informações para acessá-los. Lembre-se de que, por motivos de segurança, as nossos certificados altere do tempo. Podemos ter distribuiu uma atualização para o nosso certificado em nossos data centers. O novo certificado é válido de 3 de setembro de 2018.
  
 **Informações de certificado atual válidas a partir de 3 de setembro de 2018**
  
|**Atributo**|**Valor**|
|:-----|:-----|
|Emissor da raiz da autoridade de certificação  <br/> |GlobalSign CA raiz-R1 <br/> |
|Nome do certificado  <br/> |mail.Protection.Outlook.com  <br/> |
|Organização  <br/> |Microsoft Corporation  <br/> |
|Unidade organizacional  <br/> |  <br/> |
|Nível de segurança da chave do certificado  <br/> |2048  <br/> |
   
 **Informações de certificado preteridos válido até 3 de setembro de 2018**
  
Para ajudar a garantir uma transição suave, podemos continuará fornecer as informações do certificado antigo para referência por algum tempo, no entanto, você deve usar as informações do certificado atual de agora em diante.
  
****

|**Atributo**|**Valor**|
|:-----|:-----|
|Emissor da raiz da autoridade de certificação  <br/> |Baltimore CyberTrust Root  <br/> |
|Nome do certificado  <br/> |mail.Protection.Outlook.com  <br/> |
|Organização  <br/> |Microsoft Corporation  <br/> |
|Unidade organizacional  <br/> |Microsoft Corporation  <br/> |
|Nível de segurança da chave do certificado  <br/> |2048  <br/> |
   
## <a name="prepare-for-the-new-exchange-online-certificate"></a>Preparar o novo certificado do Exchange Online

O novo certificado emitido por uma autoridade de certificação diferente (CA) do certificado anterior usado pelo Exchange Online. Como resultado, você pode precisar executar algumas ações para usar o novo certificado.

O novo certificado requer conexão com os pontos de extremidade da nova autoridade de certificação como parte da validação do certificado. Falha ao fazer isso pode resultar em fluxo de email que está sendo afetado negativamente. Se você proteger os servidores de email com firewalls que permita que apenas os servidores de email se conectar com determinados destinos, que você precisa verificar se o servidor for capaz de validar o novo certificado. Para confirmar que o seu servidor pode usar o novo certificado, conclua estas etapas:

1. Conectar-se ao seu servidor Exchange local usando o Windows PowerShell e, em seguida, execute o seguinte comando:  
  `certutil -URL http://crl.globalsign.com/gsorganizationvalsha2g3.crl`
2. Na janela que aparece, escolha a **recuperar**.
3. Quando o utilitário conclui a verificação ela retorna um status. Se o status exibe **Okey**, seu servidor de email com êxito possa validar o novo certificado. Caso contrário, você precisa determinar o que está causando as falha nas conexões. Provavelmente, você precisará atualizar as configurações de firewall. A lista completa de pontos de extremidade que precisam ser acessados incluem:
    - OCSP.GlobalSign.com
     - CRL.GlobalSign.com
     - Secure.GlobalSign.com   

Normalmente, você recebe atualizações para os certificados raiz automaticamente pelo Windows Update. No entanto, algumas implantações tem adicionais de segurança que impede essas atualizações ocorram automaticamente. Nessas implantações bloqueado em que a atualização do Windows não é possível atualizar automaticamente certificados raiz, você precisará garantir que o certificado de autoridade de certificação de raiz correto seja instalado ao concluir estas etapas:
1.  Conectar-se ao seu servidor Exchange local usando o Windows PowerShell e, em seguida, execute o seguinte comando:  
  `certmgr.msc`
2. Sob **Confiáveis certificação/certificados de autoridade raiz**, confirme que o novo certificado está listado.

## <a name="get-more-information-about-tls-and-office-365"></a>Saiba mais sobre TLS e o Office 365

Para obter uma lista de conjuntos de codificação com suporte, consulte [os detalhes de referência técnica sobre criptografia no Office 365](technical-reference-details-about-encryption.md).
  
[Configurar conectores para fluxo de email seguro com uma organização parceira](https://technet.microsoft.com/library/dn751021%28v=exchg.150%29.aspx)
  
[Conectores com segurança avançada de email](https://technet.microsoft.com/library/261d92e4-7371-4555-b781-2062b5bb5278.aspx)
  
[Criptografia no Office 365](encryption.md)
  


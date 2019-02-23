---
title: Revogar e-mails criptografados por criptografia de mensagens do Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
description: Como administrador do Office 365, você pode revogar determinados emails que foram criptografados com a criptografia de mensagem do Office 365.
ms.openlocfilehash: 75b5e46e25f447ddac0de5a7911d0df8385da6b9
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214891"
---
# <a name="office-365-message-encryption-email-revocation"></a>Revogação de email de criptografia de mensagem do Office 365

Este artigo faz parte de uma série maior de artigos sobre a [criptografia de mensagens do Office 365](ome.md). Agora, a revogação de emails criptografados está em visualização. Espere atualizações e alterações no recurso e no conteúdo à medida que continuamos a melhorar nossa oferta.

Você pode achar necessário revogar um email que já tenha sido enviado. Se o email foi criptografado usando a criptografia de mensagem do Office 365 e você for um administrador do Office 365, poderá fazer isso para email sob determinadas condições. Este artigo descreve em que circunstâncias isso é possível e como fazê-lo.
  
## <a name="encrypted-emails-that-you-can-revoke"></a>Emails criptografados que podem ser revogados

Você pode revogar emails criptografados se o destinatário recebeu um email criptografado com base em link e com marca. Se o destinatário recebeu uma experiência interna nativa em um cliente do Outlook com suporte, esses emails não podem ser revogados.

Se um destinatário recebe uma experiência baseada em links ou uma experiência embutida depende do tipo de identidade do destinatário: o Office 365 e os destinatários da conta da Microsoft (por exemplo, usuários do outlook.com) recebem uma experiência embutida em clientes do Outlook com suporte. Todos os outros tipos de destinatários, como destinatários do Gmail, obtêm uma experiência baseada em links.

Em breve, as organizações terão a capacidade de forçar uma experiência baseada em links, independentemente da identidade do destinatário. Dessa forma, todos os destinatários receberão um email com marca com um link para o portal de criptografia de mensagens do Office 365, onde poderão ler e responder a emails criptografados. Todos esses emails criptografados serão revogável.
  
## <a name="recipient-experience-for-revoked-encrypted-emails"></a>Experiência de destinatário para emails criptografados revogados

Depois que um email tiver sido revogado, o destinatário receberá um erro ao tentar acessar o email criptografado por meio do portal de criptografia de mensagem do Office 365: "a mensagem foi revogada pelo remetente".

![Captura de tela que mostra um email criptografado revogado.](media/revoked-encrypted-email.png)

## <a name="how-to-revoke-an-encrypted-email"></a>Como revogar um email criptografado

### <a name="step-1-obtain-the-message-id-of-the-email"></a>Etapa 1. Obter a ID da mensagem do email

Antes de revogar um email criptografado, você precisa obter a ID da mensagem do email. Em geral, a MessageId é do formato:

`<xxxxxxxxxxxxxxxxxxxxxxx@xxxxxx.xxxx.prod.outlook.com>`  

Há várias maneiras de encontrar a ID da mensagem do email que você deseja revogar. Esta seção descreve algumas opções, mas você pode usar qualquer método que forneça a ID.

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-message-trace-in-the-security-amp-compliance-center"></a>Para identificar a ID de mensagem do email que você deseja revogar usando o rastreamento de mensagens no &amp; centro de conformidade de segurança

1. Pesquisar o email por remetente ou destinatário usando o [rastreamento de novas mensagens no centro de conformidade do Office 365 Security &](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).
2. Depois de localizar o email, selecione-o para exibir o painel de **detalhes de rastreamento de mensagens** . Expanda **mais informações** para localizar a ID da mensagem.

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-office-message-encryption-reports-in-the-security-amp-compliance-center"></a>Para identificar a ID de mensagem do email que você deseja revogar usando os relatórios de criptografia de mensagem do &amp; Office no centro de conformidade de segurança

1. No centro de &amp; conformidade de segurança, navegue até o **relatório de criptografia de mensagem**.
2. Escolha a tabela **Exibir detalhes** e identifique a mensagem que você deseja revogar.
3. Clique duas vezes na mensagem para exibir os detalhes que incluem a ID da mensagem.

### <a name="step-2-verify-that-the-mail-is-revocable"></a>Etapa 2. Verifique se o email é revogável

Para verificar se você pode ou não revogar uma mensagem de email específica, conclua estas etapas.

1. Usando uma conta corporativa ou de estudante que tenha permissões de administrador global em sua organização do Office 365, inicie uma sessão do Windows PowerShell e conecte-se ao Exchange Online. Para obter instruções, consulte [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Execute o cmdlet Set-OMEMessageStatus da seguinte maneira:
     ```powershell
     Get-OMEMessageStatus -MessageId "<messagieid>" | ft -a  Subject, IsRevocable
     ```

   Isso retorna o assunto da mensagem e se a mensagem é revogável. Por exemplo,

     ```text
     Subject IsRevocable
     ------- -----------
     “Test message”  True
     ```

### <a name="step-3-revoke-the-mail"></a>Etapa 3. Revogar o email  

Quando você souber a ID da mensagem do email que deseja revogar e tiver verificado que a mensagem é revogável, é possível revogar o email usando o cmdlet Set-OMEMessageRevocation.

1. [Conectar-se ao Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Execute o cmdlet Set-OMEMessageRevocation da seguinte maneira:

    ```powershell
    Set-OMEMessageRevocation -Revoke $true -MessageId "<messageId>"
    ```

3. Para verificar se o email foi revogado, execute o cmdlet Get-OMEMessageStatus da seguinte maneira:

    ```powershell
    Get-OMEMessageStatus -MessageId "<messageId>" | ft -a  Subject, Revoked
    ```  
    Se a revogação tiver sido bem-sucedida, o cmdlet retornará o seguinte resultado:  

    `Revoked: True`

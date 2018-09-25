---
title: Revogar emails criptografados por criptografia de mensagens do Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 9/24/2018
ms.audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
description: Como um administrador do Office 365, você pode revogar determinados emails que tenham sido criptografadas com o Office 365 Message Encryption.
ms.openlocfilehash: 19eb874fa15a21c29a9eb2823829e81ff244a555
ms.sourcegitcommit: c168410974bc90aaf55f1dcaa9e05c09b2b78d76
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/25/2018
ms.locfileid: "25011817"
---
# <a name="office-365-message-encryption-email-revocation"></a>Revogação de e-mail de criptografia de mensagem do Office 365

Este artigo faz parte de uma maior série de artigos sobre o [Office 365 Message Encryption](ome.md). Revogação de email criptografada, à direita agora está no modo de visualização. Espera alterações para o recurso e o conteúdo e atualizações como podemos continua melhorando nossa oferta.

Talvez seja necessário revogar um email que já foi enviado. Se o email criptografado usando a criptografia de mensagem do Office 365 e você for um administrador do Office 365, você pode fazer isso para e-mails de acordo com certas condições. Este artigo descreve em que circunstâncias, isso é possível e como fazê-lo.
  
## <a name="encrypted-emails-that-you-can-revoke"></a>Emails criptografados que você pode revogar
Você pode revogar emails criptografados, se o destinatário recebeu um link baseado em com a marca de email criptografadas. Se o destinatário recebeu uma experiência nativo embutida em um cliente com suporte do Outlook, esses emails não podem ser revogados.

Se um destinatário recebe uma experiência baseada no link ou uma experiência embutida depende do tipo de destinatário de identidade: Office 365 e Microsoft Account destinatários (por exemplo, usuários do outlook.com) obtém uma experiência embutida em clientes Outlook suportados.  
Todos os outros tipos de destinatário, como o Gmail destinatários, obtém uma experiência baseada no link. 

Em breve, as organizações terão a capacidade para forçar uma experiência baseada no link, independentemente da identidade do destinatário. Dessa maneira, todos os destinatários receberá um email com marca com um link para o portal do Office 365 Message Encryption onde eles serão capazes de ler e responder a emails criptografados. Todos esses emails criptografadas será revogável. 
  
## <a name="recipient-experience-for-revoked-encrypted-emails"></a>Experiência de destinatário para emails criptografados revogadas

Depois que um email foi revogado, o destinatário receberá um erro ao tentar acessar o email criptografado através do portal de criptografia de mensagem do Office 365: "a mensagem foi revogada pelo remetente".

![Captura de tela que mostra um email criptografado revogado.](media/revoked-encrypted-email.png)
    
## <a name="how-to-revoke-an-encrypted-email"></a>Como revogar um email criptografado

### <a name="step-1-obtain-the-message-id-of-the-email"></a>Etapa 1. Obter o ID de mensagem do email

Antes de você pode revogar um email criptografado, você precisa coletar a ID da mensagem do email. O MessageId normalmente está no formato:

`<xxxxxxxxxxxxxxxxxxxxxxx@xxxxxx.xxxx.prod.outlook.com>`  

Há várias maneiras para localizar a identificação de mensagem do email que você deseja revogar. Esta seção descreve algumas opções, mas você pode usar qualquer método que fornece a ID.

  #### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-message-trace-in-the-security-amp-compliance-center"></a>Para identificar a ID da mensagem de e-mail que você deseja revogar usando o rastreamento de mensagens na segurança &amp; Centro de conformidade

1. Pesquise o email por remetente ou destinatário usando um [Novo rastreamento de mensagem no Centro de conformidade e segurança do Office 365](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).
2. Após você ter localizado o email Selecione para abrir o painel de **detalhes de rastreamento de mensagem** . Expandir **Mais informações** para localizar a ID de mensagem.

  #### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-office-message-encryption-reports-in-the-security-amp-compliance-center"></a>Para identificar a ID da mensagem de e-mail que você deseja revogar usando relatórios de criptografia de mensagem do Office na segurança &amp; Centro de conformidade
1. Na segurança &amp; Centro de conformidade, navegue até o **Relatório de criptografia de mensagem**.
2. Escolha a tabela **Exibir detalhes** e identificar a mensagem que você deseja revogar. 
3. Clique duas vezes a mensagem para exibir os detalhes que incluem a ID de mensagem. 

### <a name="step-2-revoke-the-mail"></a>Etapa 2. Revogar o email  

Quando você souber a identificação da mensagem de e-mail que você deseja revogar, você pode revogar o email usando o cmdlet Set-OMEMessageRevocation. 

1. [Conecte-se ao Exchange Online usando o PowerShell remoto](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).
    
2. Execute o cmdlet Set-OMEMessageRevocation da seguinte maneira:
    
    ```
    Set-OMEMessageRevocation -Revoke $true -MessageId "<messageId>"
    ```  

3. Para verificar se o email foi revogado, execute o cmdlet Get-OMEMessageStatus da seguinte maneira:
    
    ```
    Get-OMEMessageStatus -MessageId "<messageId>"
    ```  
    Se a revogação teve êxito, o cmdlet retorna o resultado a seguir:  

    ```The encrypted email with the subject "<subject>" and Message ID "<messageId>" was successfully revoked.```

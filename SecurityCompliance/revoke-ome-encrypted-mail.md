---
title: Revogar e-mails criptografados por criptografia de mensagens do Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/29/2019
ms.audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
description: Como um administrador do Office 365, você pode revogar determinados emails que tenham sido criptografadas com o Office 365 Message Encryption.
ms.openlocfilehash: a3f5c08d2c8660e56c378fc5fa7a850ff2c12eb5
ms.sourcegitcommit: 03b9221d9885bcde1cdb5df2c2dc5d835802d299
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29614385"
---
# <a name="office-365-message-encryption-email-revocation"></a><span data-ttu-id="c8bfd-103">Revogação de e-mail de criptografia de mensagem do Office 365</span><span class="sxs-lookup"><span data-stu-id="c8bfd-103">Office 365 Message Encryption email revocation</span></span>

<span data-ttu-id="c8bfd-p101">Este artigo faz parte de uma maior série de artigos sobre o [Office 365 Message Encryption](ome.md). Revogação de email criptografada, à direita agora está no modo de visualização. Espera alterações para o recurso e o conteúdo e atualizações como podemos continua melhorando nossa oferta.</span><span class="sxs-lookup"><span data-stu-id="c8bfd-p101">This article is part of a larger series of articles about [Office 365 Message Encryption](ome.md). Right now, encrypted email revocation is in preview. Expect updates and changes to the feature and the content as we continue to improve our offering.</span></span>

<span data-ttu-id="c8bfd-p102">Talvez seja necessário revogar um email que já foi enviado. Se o email criptografado usando a criptografia de mensagem do Office 365 e você for um administrador do Office 365, você pode fazer isso para e-mails de acordo com certas condições. Este artigo descreve em que circunstâncias, isso é possível e como fazê-lo.</span><span class="sxs-lookup"><span data-stu-id="c8bfd-p102">You may find it necessary to revoke an email that has already been sent. If the email was encrypted using Office 365 Message Encryption, and you are an Office 365 admin, you can do this for email under certain conditions. This article describes under what circumstances this is possible and how to do it.</span></span>
  
## <a name="encrypted-emails-that-you-can-revoke"></a><span data-ttu-id="c8bfd-110">Emails criptografados que você pode revogar</span><span class="sxs-lookup"><span data-stu-id="c8bfd-110">Encrypted emails that you can revoke</span></span>

<span data-ttu-id="c8bfd-p103">Você pode revogar emails criptografados, se o destinatário recebeu um link baseado em com a marca de email criptografadas. Se o destinatário recebeu uma experiência nativo embutida em um cliente com suporte do Outlook, esses emails não podem ser revogados.</span><span class="sxs-lookup"><span data-stu-id="c8bfd-p103">You can revoke encrypted emails if the recipient received a link-based, branded encrypted email. If the recipient received a native inline experience in a supported Outlook client, then those emails cannot be revoked.</span></span>

<span data-ttu-id="c8bfd-p104">Se um destinatário recebe uma experiência baseada no link ou uma experiência embutida depende do tipo de destinatário de identidade: Office 365 e Microsoft Account destinatários (por exemplo, usuários do outlook.com) obtém uma experiência embutida em clientes Outlook suportados. Todos os outros tipos de destinatário, como o Gmail destinatários, obtém uma experiência baseada no link.</span><span class="sxs-lookup"><span data-stu-id="c8bfd-p104">Whether a recipient receives a link-based experience or an inline experience depends on the recipient identity type: Office 365 and Microsoft Account recipients (for example, outlook.com users) get an inline experience in supported Outlook clients. All other recipient types, such as Gmail recipients, get a link-based experience.</span></span>

<span data-ttu-id="c8bfd-p105">Em breve, as organizações terão a capacidade para forçar uma experiência baseada no link, independentemente da identidade do destinatário. Dessa maneira, todos os destinatários receberá um email com marca com um link para o portal do Office 365 Message Encryption onde eles serão capazes de ler e responder a emails criptografados. Todos esses emails criptografadas será revogável.</span><span class="sxs-lookup"><span data-stu-id="c8bfd-p105">Coming soon, organizations will have the ability to force a link-based experience regardless of the recipient identity. This way, all recipients will get a branded email with a link to the Office 365 Message Encryption portal where they will be able to read and reply to encrypted emails. All such encrypted emails will be revocable.</span></span>
  
## <a name="recipient-experience-for-revoked-encrypted-emails"></a><span data-ttu-id="c8bfd-118">Experiência de destinatário para emails criptografados revogadas</span><span class="sxs-lookup"><span data-stu-id="c8bfd-118">Recipient experience for revoked encrypted emails</span></span>

<span data-ttu-id="c8bfd-119">Depois que um email foi revogado, o destinatário receberá um erro ao tentar acessar o email criptografado através do portal de criptografia de mensagem do Office 365: "a mensagem foi revogada pelo remetente".</span><span class="sxs-lookup"><span data-stu-id="c8bfd-119">Once an email has been revoked, the recipient will get an error when trying to access the encrypted email through the Office 365 Message Encryption portal: “The message has been revoked by the sender”.</span></span>

![Captura de tela que mostra um email criptografado revogado.](media/revoked-encrypted-email.png)

## <a name="how-to-revoke-an-encrypted-email"></a><span data-ttu-id="c8bfd-121">Como revogar um email criptografado</span><span class="sxs-lookup"><span data-stu-id="c8bfd-121">How to revoke an encrypted email</span></span>

### <a name="step-1-obtain-the-message-id-of-the-email"></a><span data-ttu-id="c8bfd-p106">Etapa 1. Obter o ID de mensagem do email</span><span class="sxs-lookup"><span data-stu-id="c8bfd-p106">Step 1. Obtain the Message ID of the email</span></span>

<span data-ttu-id="c8bfd-p107">Antes de você pode revogar um email criptografado, você precisa coletar a ID da mensagem do email. O MessageId normalmente está no formato:</span><span class="sxs-lookup"><span data-stu-id="c8bfd-p107">Before you can revoke an encrypted mail you need to gather the Message ID of the mail. The MessageId is usually of the format:</span></span>

`<xxxxxxxxxxxxxxxxxxxxxxx@xxxxxx.xxxx.prod.outlook.com>`  

<span data-ttu-id="c8bfd-p108">Há várias maneiras para localizar a identificação de mensagem do email que você deseja revogar. Esta seção descreve algumas opções, mas você pode usar qualquer método que fornece a ID.</span><span class="sxs-lookup"><span data-stu-id="c8bfd-p108">There are multiple ways to find the Message ID of the email that you want to revoke. This section describes a couple of options, but you can use any method that provides the ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-message-trace-in-the-security-amp-compliance-center"></a><span data-ttu-id="c8bfd-128">Para identificar a ID da mensagem de e-mail que você deseja revogar usando o rastreamento de mensagens na segurança &amp; Centro de conformidade</span><span class="sxs-lookup"><span data-stu-id="c8bfd-128">To identify the Message ID of the email you want to revoke by using Message Trace in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="c8bfd-129">Pesquise o email por remetente ou destinatário usando um [Novo rastreamento de mensagem no Centro de conformidade de & de segurança do Office 365](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span><span class="sxs-lookup"><span data-stu-id="c8bfd-129">Search for the email by sender or recipient using [New Message Trace in Office 365 Security & Compliance Center](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span></span>
2. <span data-ttu-id="c8bfd-p109">Após você ter localizado o email Selecione para abrir o painel de **detalhes de rastreamento de mensagem** . Expandir **Mais informações** para localizar a ID de mensagem.</span><span class="sxs-lookup"><span data-stu-id="c8bfd-p109">Once you've located the email select it to bring up the **Message trace details** pane. Expand **More Information** to locate the Message ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-office-message-encryption-reports-in-the-security-amp-compliance-center"></a><span data-ttu-id="c8bfd-132">Para identificar a ID da mensagem de e-mail que você deseja revogar usando relatórios de criptografia de mensagem do Office na segurança &amp; Centro de conformidade</span><span class="sxs-lookup"><span data-stu-id="c8bfd-132">To identify the Message ID of the email you want to revoke by using Office Message Encryption reports in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="c8bfd-133">Na segurança &amp; Centro de conformidade, navegue até o **Relatório de criptografia de mensagem**.</span><span class="sxs-lookup"><span data-stu-id="c8bfd-133">In the Security &amp; Compliance Center, navigate to the **Message Encryption Report**.</span></span>
2. <span data-ttu-id="c8bfd-134">Escolha a tabela **Exibir detalhes** e identificar a mensagem que você deseja revogar.</span><span class="sxs-lookup"><span data-stu-id="c8bfd-134">Choose the **View details** table and identify the message that you want to revoke.</span></span>
3. <span data-ttu-id="c8bfd-135">Clique duas vezes a mensagem para exibir os detalhes que incluem a ID de mensagem.</span><span class="sxs-lookup"><span data-stu-id="c8bfd-135">Double-click the message to view details that include the Message ID.</span></span>

### <a name="step-2-revoke-the-mail"></a><span data-ttu-id="c8bfd-p110">Etapa 2. Revogar o email</span><span class="sxs-lookup"><span data-stu-id="c8bfd-p110">Step 2. Revoke the mail</span></span>  

<span data-ttu-id="c8bfd-138">Quando você souber a identificação da mensagem de e-mail que você deseja revogar, você pode revogar o email usando o cmdlet Set-OMEMessageRevocation.</span><span class="sxs-lookup"><span data-stu-id="c8bfd-138">Once you know the Message ID of the email you want to revoke, you can revoke the email by using the Set-OMEMessageRevocation cmdlet.</span></span>

1. <span data-ttu-id="c8bfd-139">[Conecte-se ao Exchange Online usando o PowerShell remoto](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="c8bfd-139">[Connect to Exchange Online Using Remote PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).</span></span>

2. <span data-ttu-id="c8bfd-140">Execute o cmdlet Set-OMEMessageRevocation da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c8bfd-140">Run the Set-OMEMessageRevocation cmdlet as follows:</span></span>

    ```powershell
    Set-OMEMessageRevocation -Revoke $true -MessageId "<messageId>"
    ```  

3. <span data-ttu-id="c8bfd-141">Para verificar se o email foi revogado, execute o cmdlet Get-OMEMessageStatus da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c8bfd-141">To check whether the email was revoked, run the Get-OMEMessageStatus cmdlet as follows:</span></span>

    ```powershell
    Get-OMEMessageStatus -MessageId "<messageId>" | fl Revoked
    ```  
    <span data-ttu-id="c8bfd-142">Se a revogação teve êxito, o cmdlet retorna o resultado a seguir:</span><span class="sxs-lookup"><span data-stu-id="c8bfd-142">If revocation was successful, the cmdlet returns the following result:</span></span>  

    `Revoked: True`

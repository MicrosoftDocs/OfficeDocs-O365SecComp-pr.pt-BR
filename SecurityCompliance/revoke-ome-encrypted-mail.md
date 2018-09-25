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
# <a name="office-365-message-encryption-email-revocation"></a><span data-ttu-id="79df1-103">Revogação de e-mail de criptografia de mensagem do Office 365</span><span class="sxs-lookup"><span data-stu-id="79df1-103">Office 365 Message Encryption email revocation</span></span>

<span data-ttu-id="79df1-p101">Este artigo faz parte de uma maior série de artigos sobre o [Office 365 Message Encryption](ome.md). Revogação de email criptografada, à direita agora está no modo de visualização. Espera alterações para o recurso e o conteúdo e atualizações como podemos continua melhorando nossa oferta.</span><span class="sxs-lookup"><span data-stu-id="79df1-p101">This article is part of a larger series of articles about [Office 365 Message Encryption](ome.md). Right now, encrypted email revocation is in preview. Expect updates and changes to the feature and the content as we continue to improve our offering.</span></span>

<span data-ttu-id="79df1-p102">Talvez seja necessário revogar um email que já foi enviado. Se o email criptografado usando a criptografia de mensagem do Office 365 e você for um administrador do Office 365, você pode fazer isso para e-mails de acordo com certas condições. Este artigo descreve em que circunstâncias, isso é possível e como fazê-lo.</span><span class="sxs-lookup"><span data-stu-id="79df1-p102">You may find it necessary to revoke an email that has already been sent. If the email was encrypted using Office 365 Message Encryption, and you are an Office 365 admin, you can do this for email under certain conditions. This article describes under what circumstances this is possible and how to do it.</span></span>
  
## <a name="encrypted-emails-that-you-can-revoke"></a><span data-ttu-id="79df1-110">Emails criptografados que você pode revogar</span><span class="sxs-lookup"><span data-stu-id="79df1-110">Encrypted emails that you can revoke</span></span>
<span data-ttu-id="79df1-p103">Você pode revogar emails criptografados, se o destinatário recebeu um link baseado em com a marca de email criptografadas. Se o destinatário recebeu uma experiência nativo embutida em um cliente com suporte do Outlook, esses emails não podem ser revogados.</span><span class="sxs-lookup"><span data-stu-id="79df1-p103">You can revoke encrypted emails if the recipient received a link-based, branded encrypted email. If the recipient received a native inline experience in a supported Outlook client, then those emails cannot be revoked.</span></span>

<span data-ttu-id="79df1-113">Se um destinatário recebe uma experiência baseada no link ou uma experiência embutida depende do tipo de destinatário de identidade: Office 365 e Microsoft Account destinatários (por exemplo, usuários do outlook.com) obtém uma experiência embutida em clientes Outlook suportados.</span><span class="sxs-lookup"><span data-stu-id="79df1-113">Whether a recipient receives a link-based experience or an inline experience depends on the recipient identity type: Office 365 and Microsoft Account recipients (for example, outlook.com users) get an inline experience in supported Outlook clients.</span></span>  
<span data-ttu-id="79df1-114">Todos os outros tipos de destinatário, como o Gmail destinatários, obtém uma experiência baseada no link.</span><span class="sxs-lookup"><span data-stu-id="79df1-114">All other recipient types, such as Gmail recipients, get a link-based experience.</span></span> 

<span data-ttu-id="79df1-p104">Em breve, as organizações terão a capacidade para forçar uma experiência baseada no link, independentemente da identidade do destinatário. Dessa maneira, todos os destinatários receberá um email com marca com um link para o portal do Office 365 Message Encryption onde eles serão capazes de ler e responder a emails criptografados. Todos esses emails criptografadas será revogável.</span><span class="sxs-lookup"><span data-stu-id="79df1-p104">Coming soon, organizations will have the ability to force a link-based experience regardless of the recipient identity. This way, all recipients will get a branded email with a link to the Office 365 Message Encryption portal where they will be able to read and reply to encrypted emails. All such encrypted emails will be revocable.</span></span> 
  
## <a name="recipient-experience-for-revoked-encrypted-emails"></a><span data-ttu-id="79df1-118">Experiência de destinatário para emails criptografados revogadas</span><span class="sxs-lookup"><span data-stu-id="79df1-118">Recipient experience for revoked encrypted emails</span></span>

<span data-ttu-id="79df1-119">Depois que um email foi revogado, o destinatário receberá um erro ao tentar acessar o email criptografado através do portal de criptografia de mensagem do Office 365: "a mensagem foi revogada pelo remetente".</span><span class="sxs-lookup"><span data-stu-id="79df1-119">Once an email has been revoked, the recipient will get an error when trying to access the encrypted email through the Office 365 Message Encryption portal: “The message has been revoked by the sender”.</span></span>

![Captura de tela que mostra um email criptografado revogado.](media/revoked-encrypted-email.png)
    
## <a name="how-to-revoke-an-encrypted-email"></a><span data-ttu-id="79df1-121">Como revogar um email criptografado</span><span class="sxs-lookup"><span data-stu-id="79df1-121">How to revoke an encrypted email</span></span>

### <a name="step-1-obtain-the-message-id-of-the-email"></a><span data-ttu-id="79df1-p105">Etapa 1. Obter o ID de mensagem do email</span><span class="sxs-lookup"><span data-stu-id="79df1-p105">Step 1. Obtain the Message ID of the email</span></span>

<span data-ttu-id="79df1-p106">Antes de você pode revogar um email criptografado, você precisa coletar a ID da mensagem do email. O MessageId normalmente está no formato:</span><span class="sxs-lookup"><span data-stu-id="79df1-p106">Before you can revoke an encrypted mail you need to gather the Message ID of the mail. The MessageId is usually of the format:</span></span>

`<xxxxxxxxxxxxxxxxxxxxxxx@xxxxxx.xxxx.prod.outlook.com>`  

<span data-ttu-id="79df1-p107">Há várias maneiras para localizar a identificação de mensagem do email que você deseja revogar. Esta seção descreve algumas opções, mas você pode usar qualquer método que fornece a ID.</span><span class="sxs-lookup"><span data-stu-id="79df1-p107">There are multiple ways to find the Message ID of the email that you want to revoke. This section describes a couple of options, but you can use any method that provides the ID.</span></span>

  #### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-message-trace-in-the-security-amp-compliance-center"></a><span data-ttu-id="79df1-128">Para identificar a ID da mensagem de e-mail que você deseja revogar usando o rastreamento de mensagens na segurança &amp; Centro de conformidade</span><span class="sxs-lookup"><span data-stu-id="79df1-128">To identify the Message ID of the email you want to revoke by using Message Trace in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="79df1-129">Pesquise o email por remetente ou destinatário usando um [Novo rastreamento de mensagem no Centro de conformidade e segurança do Office 365](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span><span class="sxs-lookup"><span data-stu-id="79df1-129">Search for the email by sender or recipient using [New Message Trace in Office 365 Security & Compliance Center](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span></span>
2. <span data-ttu-id="79df1-p108">Após você ter localizado o email Selecione para abrir o painel de **detalhes de rastreamento de mensagem** . Expandir **Mais informações** para localizar a ID de mensagem.</span><span class="sxs-lookup"><span data-stu-id="79df1-p108">Once you've located the email select it to bring up the **Message trace details** pane. Expand **More Information** to locate the Message ID.</span></span>

  #### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-office-message-encryption-reports-in-the-security-amp-compliance-center"></a><span data-ttu-id="79df1-132">Para identificar a ID da mensagem de e-mail que você deseja revogar usando relatórios de criptografia de mensagem do Office na segurança &amp; Centro de conformidade</span><span class="sxs-lookup"><span data-stu-id="79df1-132">To identify the Message ID of the email you want to revoke by using Office Message Encryption reports in the Security &amp; Compliance Center</span></span>
1. <span data-ttu-id="79df1-133">Na segurança &amp; Centro de conformidade, navegue até o **Relatório de criptografia de mensagem**.</span><span class="sxs-lookup"><span data-stu-id="79df1-133">In the Security &amp; Compliance Center, navigate to the **Message Encryption Report**.</span></span>
2. <span data-ttu-id="79df1-134">Escolha a tabela **Exibir detalhes** e identificar a mensagem que você deseja revogar.</span><span class="sxs-lookup"><span data-stu-id="79df1-134">Choose the **View details** table and identify the message that you want to revoke.</span></span> 
3. <span data-ttu-id="79df1-135">Clique duas vezes a mensagem para exibir os detalhes que incluem a ID de mensagem.</span><span class="sxs-lookup"><span data-stu-id="79df1-135">Double-click the message to view details that include the Message ID.</span></span> 

### <a name="step-2-revoke-the-mail"></a><span data-ttu-id="79df1-p109">Etapa 2. Revogar o email</span><span class="sxs-lookup"><span data-stu-id="79df1-p109">Step 2. Revoke the mail</span></span>  

<span data-ttu-id="79df1-138">Quando você souber a identificação da mensagem de e-mail que você deseja revogar, você pode revogar o email usando o cmdlet Set-OMEMessageRevocation.</span><span class="sxs-lookup"><span data-stu-id="79df1-138">Once you know the Message ID of the email you want to revoke, you can revoke the email by using the Set-OMEMessageRevocation cmdlet.</span></span> 

1. <span data-ttu-id="79df1-139">[Conecte-se ao Exchange Online usando o PowerShell remoto](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="79df1-139">[Connect to Exchange Online Using Remote PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).</span></span>
    
2. <span data-ttu-id="79df1-140">Execute o cmdlet Set-OMEMessageRevocation da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="79df1-140">Run the Set-OMEMessageRevocation cmdlet as follows:</span></span>
    
    ```
    Set-OMEMessageRevocation -Revoke $true -MessageId "<messageId>"
    ```  

3. <span data-ttu-id="79df1-141">Para verificar se o email foi revogado, execute o cmdlet Get-OMEMessageStatus da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="79df1-141">To check whether the email was revoked, run the Get-OMEMessageStatus cmdlet as follows:</span></span>
    
    ```
    Get-OMEMessageStatus -MessageId "<messageId>"
    ```  
    <span data-ttu-id="79df1-142">Se a revogação teve êxito, o cmdlet retorna o resultado a seguir:</span><span class="sxs-lookup"><span data-stu-id="79df1-142">If revocation was successful, the cmdlet returns the following result:</span></span>  

    ```The encrypted email with the subject "<subject>" and Message ID "<messageId>" was successfully revoked.```

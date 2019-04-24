---
title: Revogar emails criptografados por criptografia de mensagens do Office 365
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
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32264814"
---
# <a name="office-365-message-encryption-email-revocation"></a><span data-ttu-id="3f064-103">Revogação de email de criptografia de mensagem do Office 365</span><span class="sxs-lookup"><span data-stu-id="3f064-103">Office 365 Message Encryption email revocation</span></span>

<span data-ttu-id="3f064-104">Este artigo faz parte de uma série maior de artigos sobre a [criptografia de mensagens do Office 365](ome.md).</span><span class="sxs-lookup"><span data-stu-id="3f064-104">This article is part of a larger series of articles about [Office 365 Message Encryption](ome.md).</span></span> <span data-ttu-id="3f064-105">Agora, a revogação de emails criptografados está em visualização.</span><span class="sxs-lookup"><span data-stu-id="3f064-105">Right now, encrypted email revocation is in preview.</span></span> <span data-ttu-id="3f064-106">Espere atualizações e alterações no recurso e no conteúdo à medida que continuamos a melhorar nossa oferta.</span><span class="sxs-lookup"><span data-stu-id="3f064-106">Expect updates and changes to the feature and the content as we continue to improve our offering.</span></span>

<span data-ttu-id="3f064-107">Você pode achar necessário revogar um email que já tenha sido enviado.</span><span class="sxs-lookup"><span data-stu-id="3f064-107">You may find it necessary to revoke an email that has already been sent.</span></span> <span data-ttu-id="3f064-108">Se o email foi criptografado usando a criptografia de mensagem do Office 365 e você for um administrador do Office 365, poderá fazer isso para email sob determinadas condições.</span><span class="sxs-lookup"><span data-stu-id="3f064-108">If the email was encrypted using Office 365 Message Encryption, and you are an Office 365 admin, you can do this for email under certain conditions.</span></span> <span data-ttu-id="3f064-109">Este artigo descreve em que circunstâncias isso é possível e como fazê-lo.</span><span class="sxs-lookup"><span data-stu-id="3f064-109">This article describes under what circumstances this is possible and how to do it.</span></span>
  
## <a name="encrypted-emails-that-you-can-revoke"></a><span data-ttu-id="3f064-110">Emails criptografados que podem ser revogados</span><span class="sxs-lookup"><span data-stu-id="3f064-110">Encrypted emails that you can revoke</span></span>

<span data-ttu-id="3f064-111">Você pode revogar emails criptografados se o destinatário recebeu um email criptografado com base em link e com marca.</span><span class="sxs-lookup"><span data-stu-id="3f064-111">You can revoke encrypted emails if the recipient received a link-based, branded encrypted email.</span></span> <span data-ttu-id="3f064-112">Se o destinatário recebeu uma experiência interna nativa em um cliente do Outlook com suporte, esses emails não podem ser revogados.</span><span class="sxs-lookup"><span data-stu-id="3f064-112">If the recipient received a native inline experience in a supported Outlook client, then those emails cannot be revoked.</span></span>

<span data-ttu-id="3f064-113">Se um destinatário recebe uma experiência baseada em links ou uma experiência embutida depende do tipo de identidade do destinatário: o Office 365 e os destinatários da conta da Microsoft (por exemplo, usuários do outlook.com) recebem uma experiência embutida em clientes do Outlook com suporte.</span><span class="sxs-lookup"><span data-stu-id="3f064-113">Whether a recipient receives a link-based experience or an inline experience depends on the recipient identity type: Office 365 and Microsoft Account recipients (for example, outlook.com users) get an inline experience in supported Outlook clients.</span></span> <span data-ttu-id="3f064-114">Todos os outros tipos de destinatários, como destinatários do Gmail, obtêm uma experiência baseada em links.</span><span class="sxs-lookup"><span data-stu-id="3f064-114">All other recipient types, such as Gmail recipients, get a link-based experience.</span></span>

<span data-ttu-id="3f064-115">Em breve, as organizações terão a capacidade de forçar uma experiência baseada em links, independentemente da identidade do destinatário.</span><span class="sxs-lookup"><span data-stu-id="3f064-115">Coming soon, organizations will have the ability to force a link-based experience regardless of the recipient identity.</span></span> <span data-ttu-id="3f064-116">Dessa forma, todos os destinatários receberão um email com marca com um link para o portal de criptografia de mensagens do Office 365, onde poderão ler e responder a emails criptografados.</span><span class="sxs-lookup"><span data-stu-id="3f064-116">This way, all recipients will get a branded email with a link to the Office 365 Message Encryption portal where they will be able to read and reply to encrypted emails.</span></span> <span data-ttu-id="3f064-117">Todos esses emails criptografados serão revogável.</span><span class="sxs-lookup"><span data-stu-id="3f064-117">All such encrypted emails will be revocable.</span></span>
  
## <a name="recipient-experience-for-revoked-encrypted-emails"></a><span data-ttu-id="3f064-118">Experiência de destinatário para emails criptografados revogados</span><span class="sxs-lookup"><span data-stu-id="3f064-118">Recipient experience for revoked encrypted emails</span></span>

<span data-ttu-id="3f064-119">Depois que um email tiver sido revogado, o destinatário receberá um erro ao tentar acessar o email criptografado por meio do portal de criptografia de mensagem do Office 365: "a mensagem foi revogada pelo remetente".</span><span class="sxs-lookup"><span data-stu-id="3f064-119">Once an email has been revoked, the recipient will get an error when trying to access the encrypted email through the Office 365 Message Encryption portal: “The message has been revoked by the sender”.</span></span>

![Captura de tela que mostra um email criptografado revogado.](media/revoked-encrypted-email.png)

## <a name="how-to-revoke-an-encrypted-email"></a><span data-ttu-id="3f064-121">Como revogar um email criptografado</span><span class="sxs-lookup"><span data-stu-id="3f064-121">How to revoke an encrypted email</span></span>

### <a name="step-1-obtain-the-message-id-of-the-email"></a><span data-ttu-id="3f064-122">Etapa 1.</span><span class="sxs-lookup"><span data-stu-id="3f064-122">Step 1.</span></span> <span data-ttu-id="3f064-123">Obter a ID da mensagem do email</span><span class="sxs-lookup"><span data-stu-id="3f064-123">Obtain the Message ID of the email</span></span>

<span data-ttu-id="3f064-124">Antes de revogar um email criptografado, você precisa obter a ID da mensagem do email.</span><span class="sxs-lookup"><span data-stu-id="3f064-124">Before you can revoke an encrypted mail you need to gather the Message ID of the mail.</span></span> <span data-ttu-id="3f064-125">Em geral, a MessageId é do formato:</span><span class="sxs-lookup"><span data-stu-id="3f064-125">The MessageId is usually of the format:</span></span>

`<xxxxxxxxxxxxxxxxxxxxxxx@xxxxxx.xxxx.prod.outlook.com>`  

<span data-ttu-id="3f064-126">Há várias maneiras de encontrar a ID da mensagem do email que você deseja revogar.</span><span class="sxs-lookup"><span data-stu-id="3f064-126">There are multiple ways to find the Message ID of the email that you want to revoke.</span></span> <span data-ttu-id="3f064-127">Esta seção descreve algumas opções, mas você pode usar qualquer método que forneça a ID.</span><span class="sxs-lookup"><span data-stu-id="3f064-127">This section describes a couple of options, but you can use any method that provides the ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-message-trace-in-the-security-amp-compliance-center"></a><span data-ttu-id="3f064-128">Para identificar a ID de mensagem do email que você deseja revogar usando o rastreamento de mensagens no &amp; centro de conformidade de segurança</span><span class="sxs-lookup"><span data-stu-id="3f064-128">To identify the Message ID of the email you want to revoke by using Message Trace in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="3f064-129">Pesquisar o email por remetente ou destinatário usando o [rastreamento de novas mensagens no centro de conformidade do Office 365 Security &](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span><span class="sxs-lookup"><span data-stu-id="3f064-129">Search for the email by sender or recipient using [New Message Trace in Office 365 Security & Compliance Center](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span></span>
2. <span data-ttu-id="3f064-130">Depois de localizar o email, selecione-o para exibir o painel de **detalhes de rastreamento de mensagens** .</span><span class="sxs-lookup"><span data-stu-id="3f064-130">Once you've located the email select it to bring up the **Message trace details** pane.</span></span> <span data-ttu-id="3f064-131">Expanda **mais informações** para localizar a ID da mensagem.</span><span class="sxs-lookup"><span data-stu-id="3f064-131">Expand **More Information** to locate the Message ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-office-message-encryption-reports-in-the-security-amp-compliance-center"></a><span data-ttu-id="3f064-132">Para identificar a ID de mensagem do email que você deseja revogar usando os relatórios de criptografia de mensagem do &amp; Office no centro de conformidade de segurança</span><span class="sxs-lookup"><span data-stu-id="3f064-132">To identify the Message ID of the email you want to revoke by using Office Message Encryption reports in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="3f064-133">No centro de &amp; conformidade de segurança, navegue até o **relatório de criptografia de mensagem**.</span><span class="sxs-lookup"><span data-stu-id="3f064-133">In the Security &amp; Compliance Center, navigate to the **Message Encryption Report**.</span></span>
2. <span data-ttu-id="3f064-134">Escolha a tabela **Exibir detalhes** e identifique a mensagem que você deseja revogar.</span><span class="sxs-lookup"><span data-stu-id="3f064-134">Choose the **View details** table and identify the message that you want to revoke.</span></span>
3. <span data-ttu-id="3f064-135">Clique duas vezes na mensagem para exibir os detalhes que incluem a ID da mensagem.</span><span class="sxs-lookup"><span data-stu-id="3f064-135">Double-click the message to view details that include the Message ID.</span></span>

### <a name="step-2-verify-that-the-mail-is-revocable"></a><span data-ttu-id="3f064-136">Etapa 2.</span><span class="sxs-lookup"><span data-stu-id="3f064-136">Step 2.</span></span> <span data-ttu-id="3f064-137">Verifique se o email é revogável</span><span class="sxs-lookup"><span data-stu-id="3f064-137">Verify that the mail is revocable</span></span>

<span data-ttu-id="3f064-138">Para verificar se você pode ou não revogar uma mensagem de email específica, conclua estas etapas.</span><span class="sxs-lookup"><span data-stu-id="3f064-138">To verify whether or not you can revoke a particular email message, complete these steps.</span></span>

1. <span data-ttu-id="3f064-139">Usando uma conta corporativa ou de estudante que tenha permissões de administrador global em sua organização do Office 365, inicie uma sessão do Windows PowerShell e conecte-se ao Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="3f064-139">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="3f064-140">Para obter instruções, consulte [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="3f064-140">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="3f064-141">Execute o cmdlet Set-OMEMessageStatus da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="3f064-141">Run the Set-OMEMessageStatus cmdlet as follows:</span></span>
     ```powershell
     Get-OMEMessageStatus -MessageId "<messagieid>" | ft -a  Subject, IsRevocable
     ```

   <span data-ttu-id="3f064-142">Isso retorna o assunto da mensagem e se a mensagem é revogável.</span><span class="sxs-lookup"><span data-stu-id="3f064-142">This returns the subject of the message and whether the message is revocable.</span></span> <span data-ttu-id="3f064-143">For example,</span><span class="sxs-lookup"><span data-stu-id="3f064-143">For example,</span></span>

     ```text
     Subject IsRevocable
     ------- -----------
     “Test message”  True
     ```

### <a name="step-3-revoke-the-mail"></a><span data-ttu-id="3f064-144">Etapa 3.</span><span class="sxs-lookup"><span data-stu-id="3f064-144">Step 3.</span></span> <span data-ttu-id="3f064-145">Revogar o email</span><span class="sxs-lookup"><span data-stu-id="3f064-145">Revoke the mail</span></span>  

<span data-ttu-id="3f064-146">Quando você souber a ID da mensagem do email que deseja revogar e tiver verificado que a mensagem é revogável, é possível revogar o email usando o cmdlet Set-OMEMessageRevocation.</span><span class="sxs-lookup"><span data-stu-id="3f064-146">Once you know the Message ID of the email you want to revoke, and you have verified that the message is revocable, you can revoke the email by using the Set-OMEMessageRevocation cmdlet.</span></span>

1. <span data-ttu-id="3f064-147">[Conectar-se ao Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="3f064-147">[Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="3f064-148">Execute o cmdlet Set-OMEMessageRevocation da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="3f064-148">Run the Set-OMEMessageRevocation cmdlet as follows:</span></span>

    ```powershell
    Set-OMEMessageRevocation -Revoke $true -MessageId "<messageId>"
    ```

3. <span data-ttu-id="3f064-149">Para verificar se o email foi revogado, execute o cmdlet Get-OMEMessageStatus da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="3f064-149">To check whether the email was revoked, run the Get-OMEMessageStatus cmdlet as follows:</span></span>

    ```powershell
    Get-OMEMessageStatus -MessageId "<messageId>" | ft -a  Subject, Revoked
    ```  
    <span data-ttu-id="3f064-150">Se a revogação tiver sido bem-sucedida, o cmdlet retornará o seguinte resultado:</span><span class="sxs-lookup"><span data-stu-id="3f064-150">If revocation was successful, the cmdlet returns the following result:</span></span>  

    `Revoked: True`

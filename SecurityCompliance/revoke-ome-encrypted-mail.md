---
title: Revogar emails criptografados pela criptografia de mensagem avançada do Office 365
ms.author: krowley
author: kccross
manager: laurawi
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.date: 4/30/2019
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
description: Como administrador do Office 365, você pode revogar determinados emails que foram criptografados com a criptografia de mensagem avançada do Office 365.
ms.openlocfilehash: 098ce50791152c8bbb4e4692d6fb85e4c2c7cb58
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34156783"
---
# <a name="revoke-email-encrypted-by-office-365-advanced-message-encryption"></a><span data-ttu-id="2b5e5-103">Revogar emails criptografados pela criptografia de mensagem avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="2b5e5-103">Revoke email encrypted by Office 365 Advanced Message Encryption</span></span>

<span data-ttu-id="2b5e5-104">A revogação de emails é oferecida como parte da criptografia de mensagem avançada do Office 365.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-104">Email revocation is offered as part of Office 365 Advanced Message Encryption.</span></span> <span data-ttu-id="2b5e5-105">A criptografia de mensagem avançada do Office 365 está disponível na parte superior da criptografia de mensagem do Office 365 em determinadas assinaturas.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-105">Office 365 Advanced Message Encryption is available on top of Office 365 Message Encryption in certain subscriptions.</span></span> <span data-ttu-id="2b5e5-106">A criptografia avançada de mensagens está incluída no [Microsoft 365 Enterprise E5](https://www.microsoft.com/microsoft-365/enterprise/home), no Office 365 Enterprise E5 e no Office 365 Education a5.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-106">Advanced Message Encryption is included in [Microsoft 365 Enterprise E5](https://www.microsoft.com/microsoft-365/enterprise/home), Office 365 Enterprise E5, and Office 365 Education A5.</span></span> <span data-ttu-id="2b5e5-107">Se sua organização tiver uma assinatura do Office 365 que não inclua a criptografia de mensagem avançada do Office 365, você poderá comprar a criptografia de mensagem avançada como um complemento com a conformidade E5 do SKU de conformidade avançada.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-107">If your organization has an Office 365 subscription that does not include Office 365 Advanced Message Encryption, you can purchase Advanced Message Encryption as an add-on with E5 Compliance of the Advanced Compliance SKU.</span></span>

<span data-ttu-id="2b5e5-108">Este artigo faz parte de uma série maior de artigos sobre a [criptografia de mensagens do Office 365](ome.md).</span><span class="sxs-lookup"><span data-stu-id="2b5e5-108">This article is part of a larger series of articles about [Office 365 Message Encryption](ome.md).</span></span>

<span data-ttu-id="2b5e5-109">Você pode achar necessário revogar um email que já tenha sido enviado.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-109">You may find it necessary to revoke an email that has already been sent.</span></span> <span data-ttu-id="2b5e5-110">Se o email foi criptografado usando a criptografia de mensagem avançada do Office 365 e você for um administrador do Office 365, poderá fazer isso para email sob determinadas condições.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-110">If the email was encrypted using Office 365 Advanced Message Encryption, and you are an Office 365 admin, you can do this for email under certain conditions.</span></span> <span data-ttu-id="2b5e5-111">Este artigo descreve em que circunstâncias isso é possível e como fazê-lo.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-111">This article describes under what circumstances this is possible and how to do it.</span></span>
  
## <a name="encrypted-emails-that-you-can-revoke"></a><span data-ttu-id="2b5e5-112">Emails criptografados que podem ser revogados</span><span class="sxs-lookup"><span data-stu-id="2b5e5-112">Encrypted emails that you can revoke</span></span>

<span data-ttu-id="2b5e5-113">Você pode revogar emails criptografados se o destinatário recebeu um email criptografado com base em link e com marca.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-113">You can revoke encrypted emails if the recipient received a link-based, branded encrypted email.</span></span> <span data-ttu-id="2b5e5-114">Se o destinatário recebeu uma experiência interna nativa em um cliente do Outlook com suporte, esses emails não podem ser revogados.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-114">If the recipient received a native inline experience in a supported Outlook client, then those emails cannot be revoked.</span></span>

<span data-ttu-id="2b5e5-115">Se um destinatário recebe uma experiência baseada em links ou uma experiência embutida depende do tipo de identidade do destinatário: o Office 365 e os destinatários da conta da Microsoft (por exemplo, usuários do outlook.com) recebem uma experiência embutida em clientes do Outlook com suporte.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-115">Whether a recipient receives a link-based experience or an inline experience depends on the recipient identity type: Office 365 and Microsoft Account recipients (for example, outlook.com users) get an inline experience in supported Outlook clients.</span></span> <span data-ttu-id="2b5e5-116">Todos os outros tipos de destinatários, como destinatários do Gmail, obtêm uma experiência baseada em links.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-116">All other recipient types, such as Gmail recipients, get a link-based experience.</span></span>

## <a name="recipient-experience-for-revoked-encrypted-emails"></a><span data-ttu-id="2b5e5-117">Experiência de destinatário para emails criptografados revogados</span><span class="sxs-lookup"><span data-stu-id="2b5e5-117">Recipient experience for revoked encrypted emails</span></span>

<span data-ttu-id="2b5e5-118">Depois que um email tiver sido revogado, o destinatário receberá um erro ao tentar acessar o email criptografado por meio do portal de criptografia de mensagem do Office 365: "a mensagem foi revogada pelo remetente".</span><span class="sxs-lookup"><span data-stu-id="2b5e5-118">Once an email has been revoked, the recipient will get an error when trying to access the encrypted email through the Office 365 Message Encryption portal: “The message has been revoked by the sender”.</span></span>

![Captura de tela que mostra um email criptografado revogado.](media/revoked-encrypted-email.png)

## <a name="how-to-revoke-an-encrypted-email"></a><span data-ttu-id="2b5e5-120">Como revogar um email criptografado</span><span class="sxs-lookup"><span data-stu-id="2b5e5-120">How to revoke an encrypted email</span></span>

### <a name="step-1-obtain-the-message-id-of-the-email"></a><span data-ttu-id="2b5e5-121">Etapa 1.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-121">Step 1.</span></span> <span data-ttu-id="2b5e5-122">Obter a ID da mensagem do email</span><span class="sxs-lookup"><span data-stu-id="2b5e5-122">Obtain the Message ID of the email</span></span>

<span data-ttu-id="2b5e5-123">Antes de revogar um email criptografado, você precisa obter a ID da mensagem do email.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-123">Before you can revoke an encrypted mail you need to gather the Message ID of the mail.</span></span> <span data-ttu-id="2b5e5-124">Em geral, a MessageId é do formato:</span><span class="sxs-lookup"><span data-stu-id="2b5e5-124">The MessageId is usually of the format:</span></span>

`<xxxxxxxxxxxxxxxxxxxxxxx@xxxxxx.xxxx.prod.outlook.com>`  

<span data-ttu-id="2b5e5-125">Há várias maneiras de encontrar a ID da mensagem do email que você deseja revogar.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-125">There are multiple ways to find the Message ID of the email that you want to revoke.</span></span> <span data-ttu-id="2b5e5-126">Esta seção descreve algumas opções, mas você pode usar qualquer método que forneça a ID.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-126">This section describes a couple of options, but you can use any method that provides the ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-message-trace-in-the-security-amp-compliance-center"></a><span data-ttu-id="2b5e5-127">Para identificar a ID de mensagem do email que você deseja revogar usando o rastreamento de mensagens no &amp; centro de conformidade de segurança</span><span class="sxs-lookup"><span data-stu-id="2b5e5-127">To identify the Message ID of the email you want to revoke by using Message Trace in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="2b5e5-128">Pesquisar o email por remetente ou destinatário usando o [rastreamento de novas mensagens no centro de conformidade do Office 365 Security &](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span><span class="sxs-lookup"><span data-stu-id="2b5e5-128">Search for the email by sender or recipient using [New Message Trace in Office 365 Security & Compliance Center](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span></span>

2. <span data-ttu-id="2b5e5-129">Depois de localizar o email, selecione-o para exibir o painel de **detalhes de rastreamento de mensagens** .</span><span class="sxs-lookup"><span data-stu-id="2b5e5-129">Once you've located the email, select it to bring up the **Message trace details** pane.</span></span> <span data-ttu-id="2b5e5-130">Expanda **mais informações** para localizar a ID da mensagem.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-130">Expand **More Information** to locate the Message ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-office-message-encryption-reports-in-the-security-amp-compliance-center"></a><span data-ttu-id="2b5e5-131">Para identificar a ID de mensagem do email que você deseja revogar usando os relatórios de criptografia de mensagem do &amp; Office no centro de conformidade de segurança</span><span class="sxs-lookup"><span data-stu-id="2b5e5-131">To identify the Message ID of the email you want to revoke by using Office Message Encryption reports in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="2b5e5-132">No centro de &amp; conformidade de segurança, navegue até o **relatório de criptografia de mensagem**.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-132">In the Security &amp; Compliance Center, navigate to the **Message Encryption Report**.</span></span>

2. <span data-ttu-id="2b5e5-133">Escolha a tabela **Exibir detalhes** e identifique a mensagem que você deseja revogar.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-133">Choose the **View details** table and identify the message that you want to revoke.</span></span>

3. <span data-ttu-id="2b5e5-134">Clique duas vezes na mensagem para exibir os detalhes que incluem a ID da mensagem.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-134">Double-click the message to view details that include the Message ID.</span></span>

### <a name="step-2-verify-that-the-mail-is-revocable"></a><span data-ttu-id="2b5e5-135">Etapa 2.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-135">Step 2.</span></span> <span data-ttu-id="2b5e5-136">Verifique se o email é revogável</span><span class="sxs-lookup"><span data-stu-id="2b5e5-136">Verify that the mail is revocable</span></span>

<span data-ttu-id="2b5e5-137">Para verificar se você pode revogar uma mensagem de email específica, verifique se o campo status de revogação está visível na tabela **detalhes** no &amp; centro de conformidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-137">To verify whether you can revoke a particular email message, check whether the Revocation Status field is visible in the **Details** table in the Security &amp; Compliance Center.</span></span>

<span data-ttu-id="2b5e5-138">Para verificar se você pode ou não revogar uma mensagem de email específica usando o Windows PowerShell, conclua estas etapas.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-138">To verify whether or not you can revoke a particular email message by using Windows Powershell, complete these steps.</span></span>

1. <span data-ttu-id="2b5e5-139">Usando uma conta corporativa ou de estudante que tenha permissões de administrador global em sua organização do Office 365, inicie uma sessão do Windows PowerShell e conecte-se ao Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-139">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="2b5e5-140">Para obter instruções, consulte [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="2b5e5-140">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="2b5e5-141">Execute o cmdlet Set-OMEMessageStatus da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="2b5e5-141">Run the Set-OMEMessageStatus cmdlet as follows:</span></span>

     ```powershell
     Get-OMEMessageStatus -MessageId "<message id>" | ft -a  Subject, IsRevocable
     ```

   <span data-ttu-id="2b5e5-142">Isso retorna o assunto da mensagem e se a mensagem é revogável.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-142">This returns the subject of the message and whether the message is revocable.</span></span> <span data-ttu-id="2b5e5-143">For example,</span><span class="sxs-lookup"><span data-stu-id="2b5e5-143">For example,</span></span>

     ```text
     Subject IsRevocable
     ------- -----------
     “Test message”  True
     ```

### <a name="step-3-revoke-the-mail"></a><span data-ttu-id="2b5e5-144">Etapa 3.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-144">Step 3.</span></span> <span data-ttu-id="2b5e5-145">Revogar o email</span><span class="sxs-lookup"><span data-stu-id="2b5e5-145">Revoke the mail</span></span>  

<span data-ttu-id="2b5e5-146">Quando você souber a ID da mensagem do email que deseja revogar e tiver verificado que a mensagem é revogável, é possível revogar o email.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-146">Once you know the Message ID of the email you want to revoke, and you have verified that the message is revocable, you can revoke the email.</span></span>

<span data-ttu-id="2b5e5-147">Para revogar o email no centro &amp; de conformidade de segurança, na tabela **detalhes** , \*\*\*\* escolha Revogar.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-147">To revoke the email in the Security &amp; Compliance Center, in the **Details** table, choose **Revoke**.</span></span>

<span data-ttu-id="2b5e5-148">Você pode revogar um email usando o Windows PowerShell usando o cmdlet Set-OMEMessageRevocation.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-148">You can revoke an email by using Windows Powershell by using the Set-OMEMessageRevocation cmdlet.</span></span>

1. <span data-ttu-id="2b5e5-149">[Conectar-se ao Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="2b5e5-149">[Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="2b5e5-150">Execute o cmdlet Set-OMEMessageRevocation da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="2b5e5-150">Run the Set-OMEMessageRevocation cmdlet as follows:</span></span>

    ```powershell
    Set-OMEMessageRevocation -Revoke $true -MessageId "<messageId>"
    ```

3. <span data-ttu-id="2b5e5-151">Para verificar se o email foi revogado, execute o cmdlet Get-OMEMessageStatus da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="2b5e5-151">To check whether the email was revoked, run the Get-OMEMessageStatus cmdlet as follows:</span></span>

    ```powershell
    Get-OMEMessageStatus -MessageId "<messageId>" | ft -a  Subject, Revoked
    ```

    <span data-ttu-id="2b5e5-152">Se a revogação tiver sido bem-sucedida, o cmdlet retornará o seguinte resultado:</span><span class="sxs-lookup"><span data-stu-id="2b5e5-152">If revocation was successful, the cmdlet returns the following result:</span></span>  

     ```text
     Revoked: True
     ```

## <a name="more-information-about-office-365-advanced-message-encryption"></a><span data-ttu-id="2b5e5-153">Mais informações sobre a criptografia de mensagem avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="2b5e5-153">More information about Office 365 Advanced Message Encryption</span></span>

- [<span data-ttu-id="2b5e5-154">Criptografia de mensagem avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="2b5e5-154">Office 365 Advanced Message Encryption</span></span>](ome-advanced-message-encryption.md)

- [<span data-ttu-id="2b5e5-155">Criptografia de mensagem avançada do Office 365-expiração de email</span><span class="sxs-lookup"><span data-stu-id="2b5e5-155">Office 365 Advanced Message Encryption - email expiration</span></span>](ome-advanced-expiration.md)

- [<span data-ttu-id="2b5e5-156">Descrição do serviço de conformidade e política de mensagens</span><span class="sxs-lookup"><span data-stu-id="2b5e5-156">Message policy and compliance service description</span></span>](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/message-policy-and-compliance)
---
title: Criar uma política de tipo de informação confidencial para sua organização usando a criptografia de mensagem do Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 8/28/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- Strat_O365_Enterprise
description: 'Resumo: política de criptografia de mensagem do Office 365 para tipos de informações confidenciais.'
ms.openlocfilehash: d74712798ba9d46614b5fc916e4b1ce111582304
ms.sourcegitcommit: 73f1db241c0686020167d43442e7b07a2199ea3a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/28/2019
ms.locfileid: "36658117"
---
# <a name="create-a-sensitive-information-type-policy-for-your-organization-using-office-365-message-encryption"></a><span data-ttu-id="ccc0d-103">Criar uma política de tipo de informação confidencial para sua organização usando a criptografia de mensagem do Office 365</span><span class="sxs-lookup"><span data-stu-id="ccc0d-103">Create a sensitive information type policy for your organization using Office 365 Message Encryption</span></span>

<span data-ttu-id="ccc0d-104">Você pode usar as regras de fluxo de email do Exchange ou a prevenção de perda de dados do Office 365 (DLP) para criar uma política de tipo de informação confidencial com a criptografia de mensagem do Office 365.</span><span class="sxs-lookup"><span data-stu-id="ccc0d-104">You can use either Exchange mail flow rules or Office 365 Data Loss Prevention (DLP) to create a sensitive information type policy with Office 365 Message Encryption.</span></span> <span data-ttu-id="ccc0d-105">Para criar uma regra de fluxo de email do Exchange, você pode usar o centro de administração do Exchange (Eat) ou o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ccc0d-105">To create an Exchange mail flow rule, you can use either the Exchange admin center (EAC) or PowerShell.</span></span>

### <a name="to-create-the-policy-by-using-mail-flow-rules-in-the-eac"></a><span data-ttu-id="ccc0d-106">Para criar a política usando regras de fluxo de emails no Eat</span><span class="sxs-lookup"><span data-stu-id="ccc0d-106">To create the policy by using mail flow rules in the EAC</span></span>

<span data-ttu-id="ccc0d-107">Entre no centro de administração do Exchange (Eat) e vá para \*\*\*\* > **regras**de fluxo de emails.</span><span class="sxs-lookup"><span data-stu-id="ccc0d-107">Sign in to the Exchange admin center (EAC) and go to **Mail flow** > **Rules**.</span></span> <span data-ttu-id="ccc0d-108">Na página regras, crie uma regra que aplique a criptografia de mensagem do Office 365.</span><span class="sxs-lookup"><span data-stu-id="ccc0d-108">On the Rules page, create a rule that applies Office 365 Message Encryption.</span></span> <span data-ttu-id="ccc0d-109">Você pode criar uma regra com base em condições como a presença de determinadas palavras-chave ou tipos de informações confidenciais na mensagem ou no anexo.</span><span class="sxs-lookup"><span data-stu-id="ccc0d-109">You can create a rule based on conditions such as the presence of certain keywords or sensitive information types in the message or attachment.</span></span>

### <a name="to-create-the-policy-by-using-mail-flow-rules-in-powershell"></a><span data-ttu-id="ccc0d-110">Para criar a política usando regras de fluxo de email no PowerShell</span><span class="sxs-lookup"><span data-stu-id="ccc0d-110">To create the policy by using mail flow rules in PowerShell</span></span>

<span data-ttu-id="ccc0d-111">Use uma conta corporativa ou de estudante que tenha permissões de administrador global em sua organização do Office 365, inicie uma sessão do Windows PowerShell e conecte-se ao Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="ccc0d-111">Use a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="ccc0d-112">Para obter instruções, consulte [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="ccc0d-112">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span> <span data-ttu-id="ccc0d-113">Use os cmdlets Set-IRMConfiguration e New-TransportRule para criar a política.</span><span class="sxs-lookup"><span data-stu-id="ccc0d-113">Use the Set-IRMConfiguration and New-TransportRule cmdlets to create the policy.</span></span>

### <a name="example-mail-flow-rule-created-with-powershell"></a><span data-ttu-id="ccc0d-114">Regra de fluxo de emails de exemplo criada com o PowerShell</span><span class="sxs-lookup"><span data-stu-id="ccc0d-114">Example mail flow rule created with PowerShell</span></span>

<span data-ttu-id="ccc0d-115">Execute os seguintes comandos no PowerShell para criar uma regra de fluxo de email do Exchange que criptografa automaticamente os emails enviados fora da sua organização com a política *somente criptografia* se os emails ou seus anexos contiverem as seguintes informações confidenciais digitar</span><span class="sxs-lookup"><span data-stu-id="ccc0d-115">Run the following commands in PowerShell to create an Exchange mail flow rule that automatically encrypts emails sent outside your organization with the *Encrypt-Only* policy if the emails or their attachments contain the following sensitive information types:</span></span>

- <span data-ttu-id="ccc0d-116">Número de roteamento ABA</span><span class="sxs-lookup"><span data-stu-id="ccc0d-116">ABA routing number</span></span>
- <span data-ttu-id="ccc0d-117">Número do cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="ccc0d-117">Credit card Number</span></span>
- <span data-ttu-id="ccc0d-118">Número da Agência de aplicação de medicamentos (DEA)</span><span class="sxs-lookup"><span data-stu-id="ccc0d-118">Drug Enforcement Agency (DEA) number</span></span>
- <span data-ttu-id="ccc0d-119">EUA/REINO UNIDO</span><span class="sxs-lookup"><span data-stu-id="ccc0d-119">U.S. / U.K.</span></span> <span data-ttu-id="ccc0d-120">passport number</span><span class="sxs-lookup"><span data-stu-id="ccc0d-120">passport number</span></span>
- <span data-ttu-id="ccc0d-121">Número de conta bancária dos EUA</span><span class="sxs-lookup"><span data-stu-id="ccc0d-121">U.S. bank account number</span></span>
- <span data-ttu-id="ccc0d-122">Número de identificação de contribuinte individual (ITIN) dos EUA</span><span class="sxs-lookup"><span data-stu-id="ccc0d-122">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>
- <span data-ttu-id="ccc0d-123">Número de seguridade social dos EUA (SSN)</span><span class="sxs-lookup"><span data-stu-id="ccc0d-123">U.S. Social Security Number (SSN)</span></span>

```powershell
Set-IRMConfiguration -DecryptAttachmentForEncryptOnly $true
New-TransportRule -Name "Encrypt outbound sensitive emails (out of box rule)" -SentToScope  NotInOrganization  -ApplyRightsProtectionTemplate "Encrypt" -MessageContainsDataClassifications @(@{Name="ABA Routing Number"; minCount="1"},@{Name="Credit Card Number"; minCount="1"},@{Name="Drug Enforcement Agency (DEA) Number"; minCount="1"},@{Name="U.S. / U.K. Passport Number"; minCount="1"},@{Name="U.S. Bank Account Number"; minCount="1"},@{Name="U.S. Individual Taxpayer Identification Number (ITIN)"; minCount="1"},@{Name="U.S. Social Security Number (SSN)"; minCount="1"}) -SenderNotificationType "NotifyOnly"
```

<span data-ttu-id="ccc0d-124">Para obter mais informações, consulte [Set-IRMConfiguration](https://docs.microsoft.com/en-us/powershell/module/exchange/encryption-and-certificates/set-irmconfiguration?view=exchange-ps) e [New-TransportRule](https://docs.microsoft.com/en-us/powershell/module/exchange/policy-and-compliance/New-TransportRule?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="ccc0d-124">For more information, see [Set-IRMConfiguration](https://docs.microsoft.com/en-us/powershell/module/exchange/encryption-and-certificates/set-irmconfiguration?view=exchange-ps) and [New-TransportRule](https://docs.microsoft.com/en-us/powershell/module/exchange/policy-and-compliance/New-TransportRule?view=exchange-ps).</span></span>

## <a name="how-recipients-access-attachments"></a><span data-ttu-id="ccc0d-125">Como os destinatários acessam anexos</span><span class="sxs-lookup"><span data-stu-id="ccc0d-125">How recipients access attachments</span></span>

<span data-ttu-id="ccc0d-126">Depois que o Office 365 criptografa uma mensagem, os destinatários têm acesso irrestrito aos anexos quando acessam e abrem seus emails criptografados.</span><span class="sxs-lookup"><span data-stu-id="ccc0d-126">After Office 365 encrypts a message, recipients have unrestricted access to attachments when they access and open their encrypted email.</span></span>

## <a name="to-prepare-for-this-change"></a><span data-ttu-id="ccc0d-127">Para se preparar para essa alteração</span><span class="sxs-lookup"><span data-stu-id="ccc0d-127">To prepare for this change</span></span>

<span data-ttu-id="ccc0d-128">Talvez você queira atualizar qualquer material de treinamento e documentação do usuário final aplicável para preparar as pessoas em sua organização para essa alteração.</span><span class="sxs-lookup"><span data-stu-id="ccc0d-128">You may want to update any applicable end-user documentation and training materials to prepare people in your organization for this change.</span></span> <span data-ttu-id="ccc0d-129">Compartilhe estes recursos de criptografia de mensagem do Office 365 com seus usuários conforme apropriado:</span><span class="sxs-lookup"><span data-stu-id="ccc0d-129">Share these Office 365 Message Encryption resources with your users as appropriate:</span></span>

- [<span data-ttu-id="ccc0d-130">Enviar, exibir e responder a mensagens criptografadas no Outlook para PC</span><span class="sxs-lookup"><span data-stu-id="ccc0d-130">Send, view, and reply to encrypted messages in Outlook for PC</span></span>](https://support.office.com/article/send-view-and-reply-to-encrypted-messages-in-outlook-for-pc-eaa43495-9bbb-4fca-922a-df90dee51980)
- [<span data-ttu-id="ccc0d-131">Vídeo do Office 365 Essentials: criptografia de mensagem do Office</span><span class="sxs-lookup"><span data-stu-id="ccc0d-131">Office 365 Essentials Video: Office Message Encryption</span></span>](https://youtu.be/CQR0cG_iEUc)

## <a name="view-these-changes-in-the-audit-log"></a><span data-ttu-id="ccc0d-132">Exibir essas alterações no log de auditoria</span><span class="sxs-lookup"><span data-stu-id="ccc0d-132">View these changes in the Audit log</span></span>

<span data-ttu-id="ccc0d-133">O Office 365 audita essa atividade e a disponibiliza para os administradores do Office 365.</span><span class="sxs-lookup"><span data-stu-id="ccc0d-133">Office 365 audits this activity and makes it available to Office 365 administrators.</span></span> <span data-ttu-id="ccc0d-134">A operação é ' New-TransportRule ' e um trecho de uma amostra de auditoria de entrada da pesquisa de log de auditoria no centro de conformidade de segurança & está abaixo:</span><span class="sxs-lookup"><span data-stu-id="ccc0d-134">The operation is ‘New-TransportRule’ and a snippet of a sample audit entry from the Audit Log Search in Security & Compliance Center is below:</span></span>

```text
*{"CreationTime":"2018-11-28T23:35:01","Id":"a1b2c3d4-daa0-4c4f-a019-03a1234a1b0c","Operation":"New-TransportRule","OrganizationId":"123456-221d-12345 ","RecordType":1,"ResultStatus":"True","UserKey":"Microsoft Operator","UserType":3,"Version":1,"Workload":"Exchange","ClientIP":"123.456.147.68:17584","ObjectId":"","UserId":"Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso.onmicrosoft.com","OriginatingServer":"CY4PR13MBXXXX (15.20.1382.008)","Parameters": {"Name":"Organization","Value":"123456-221d-12346"{"Name":"ApplyRightsProtectionTemplate","Value":"Encrypt"},{"Name":"Name","Value":"Encrypt outbound sensitive emails (out of box rule)"},{"Name":"MessageContainsDataClassifications”…etc.*
```

## <a name="to-disable-or-customize-the-sensitive-information-types-policy"></a><span data-ttu-id="ccc0d-135">Para desabilitar ou personalizar a política de tipos de informações confidenciais</span><span class="sxs-lookup"><span data-stu-id="ccc0d-135">To disable or customize the sensitive information types policy</span></span>

<span data-ttu-id="ccc0d-136">Depois de criar a regra de fluxo de emails do Exchange, você pode [desabilitar ou editar a regra](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) indo para**regras** de **fluxo** > de emails no centro de administração do Exchange (Eat) e desabilitar a regra "*criptografar emails confidenciais de saída (regra fora de caixa)* ".</span><span class="sxs-lookup"><span data-stu-id="ccc0d-136">Once you've created the Exchange mail flow rule, you can [disable or edit the rule](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) by going to **Mail flow** > **Rules** in the Exchange admin center (EAC) and disable the rule “*Encrypt outbound sensitive emails (out of box rule)*”.</span></span>

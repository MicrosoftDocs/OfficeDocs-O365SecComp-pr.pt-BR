---
title: Política de criptografia de mensagem do Office 365 para informações confidenciais
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/31/2019
ROBOTS: NOINDEX, NOFOLLOW
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Resumo: política de criptografia de mensagem do Office 365 para tipos de informações confidenciais agora disponível.'
ms.openlocfilehash: 99cb7a9f94c9cf4036c11b74a5208ddf0e819ceb
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32261259"
---
# <a name="office-365-message-encryption-policy-for-sensitive-information"></a><span data-ttu-id="7413d-103">Política de criptografia de mensagem do Office 365 para informações confidenciais</span><span class="sxs-lookup"><span data-stu-id="7413d-103">Office 365 Message Encryption policy for sensitive information</span></span>

<span data-ttu-id="7413d-104">Atualização (1/30/19): em outubro de 2018, trabalhamos com uma pequena amostra de clientes para entender se podemos simplificar a proteção criptografando automaticamente emails confidenciais com base em determinados tipos de informações confidenciais.</span><span class="sxs-lookup"><span data-stu-id="7413d-104">Update (1/30/19): In October 2018, we worked with a small sample of customers to understand if we can simplify protection by automatically encrypting sensitive emails based on certain sensitive information types.</span></span> <span data-ttu-id="7413d-105">Com base nos comentários positivos deste exemplo, decidimos expandir para um perfil mais variado de locatários em dezembro de 2018.</span><span class="sxs-lookup"><span data-stu-id="7413d-105">Based on positive feedback from this sample, we decided to expand to a more diverse profile of tenants in December 2018.</span></span> <span data-ttu-id="7413d-106">Depois de comunicar a próxima implantação para selecionar locatários, ouvimos seus comentários e determinamos que os clientes com ambientes mais complexos queriam implementar as regras com mais cautela, e estamos, portanto, ajustando nossos planos.</span><span class="sxs-lookup"><span data-stu-id="7413d-106">After communicating the next roll-out to select tenants, we listened to your feedback and determined that customers with more complex environments wanted to implement the rules more cautiously, and we are therefore adjusting our plans.</span></span>

<span data-ttu-id="7413d-107">Se sua organização foi selecionada para a distribuição a partir de 15 de janeiro de 2019, não iremos distribuir a política automática.</span><span class="sxs-lookup"><span data-stu-id="7413d-107">If your organization was selected for the roll-out starting January 15, 2019, we will not roll out the automatic policy.</span></span> <span data-ttu-id="7413d-108">Em vez disso, forneceremos instruções neste artigo sobre como você pode concluir o yourselves de distribuição.</span><span class="sxs-lookup"><span data-stu-id="7413d-108">Instead, we are providing instructions in this article on how you can complete the roll-out yourselves.</span></span> <span data-ttu-id="7413d-109">Continue lendo para saber como.</span><span class="sxs-lookup"><span data-stu-id="7413d-109">Keep reading to find out how.</span></span>

||
|:-----|
|<span data-ttu-id="7413d-110">Este artigo faz parte de uma série maior de artigos sobre a criptografia de mensagens do Office 365.</span><span class="sxs-lookup"><span data-stu-id="7413d-110">This article is part of a larger series of articles about Office 365 Message Encryption.</span></span> <span data-ttu-id="7413d-111">Este artigo destina-se a administradores e ITPros.</span><span class="sxs-lookup"><span data-stu-id="7413d-111">This article is intended for administrators and ITPros.</span></span> <span data-ttu-id="7413d-112">Se você estiver apenas procurando informações sobre como enviar ou receber uma mensagem criptografada, consulte a lista de artigos na [ome (criptografia de mensagens do Office 365)](ome.md) e localize o artigo que melhor atende às suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="7413d-112">If you're just looking for information on sending or receiving an encrypted message, see the list of articles in [Office 365 Message Encryption (OME)](ome.md) and locate the article that best fits your needs.</span></span> |
||

## <a name="how-to-create-the-sensitive-information-type-policy-for-your-tenant"></a><span data-ttu-id="7413d-113">Como criar a política de tipo de informação confidencial para o locatário</span><span class="sxs-lookup"><span data-stu-id="7413d-113">How to create the sensitive information type policy for your tenant</span></span>

<span data-ttu-id="7413d-114">Você pode usar as regras de fluxo de email do Exchange ou a prevenção de perda de dados do Office 365 (DLP) para criar a política de tipo de informação confidencial.</span><span class="sxs-lookup"><span data-stu-id="7413d-114">You can use either Exchange mail flow rules or Office 365 Data Loss Prevention (DLP) to create the sensitive information type policy.</span></span> <span data-ttu-id="7413d-115">Para criar uma regra de fluxo de email do Exchange, você pode usar o centro de administração do Exchange (Eat) ou o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7413d-115">To create an Exchange mail flow rule you can use either the Exchange admin center (EAC) or PowerShell.</span></span>

### <a name="to-create-the-policy-by-using-mail-flow-rules-in-the-eac"></a><span data-ttu-id="7413d-116">Para criar a política usando regras de fluxo de emails no Eat</span><span class="sxs-lookup"><span data-stu-id="7413d-116">To create the policy by using mail flow rules in the EAC</span></span>

<span data-ttu-id="7413d-117">Entre no centro de administração do Exchange (Eat) e vá para**regras**de **fluxo** > de emails.</span><span class="sxs-lookup"><span data-stu-id="7413d-117">Sign-in to the Exchange admin center (EAC) and go to **Mail flow** > **Rules**.</span></span> <span data-ttu-id="7413d-118">Lá, crie uma regra que aplique a criptografia de mensagem do Office 365 com base em condições como a presença de determinadas palavras-chave ou tipos de informações confidenciais na mensagem ou no anexo.</span><span class="sxs-lookup"><span data-stu-id="7413d-118">There, create a rule that applies Office 365 Message Encryption based on conditions such as the presence of certain keywords or sensitive information types in the message or attachment.</span></span>

### <a name="to-create-the-policy-by-using-mail-flow-rules-in-powershell"></a><span data-ttu-id="7413d-119">Para criar a política usando regras de fluxo de email no PowerShell</span><span class="sxs-lookup"><span data-stu-id="7413d-119">To create the policy by using mail flow rules in PowerShell</span></span>

<span data-ttu-id="7413d-120">Usando uma conta corporativa ou de estudante que tenha permissões de administrador global em sua organização do Office 365, inicie uma sessão do Windows PowerShell e conecte-se ao Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="7413d-120">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="7413d-121">Para obter instruções, consulte [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="7413d-121">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span> <span data-ttu-id="7413d-122">Use os cmdlets Set-IRMConfiguration e New-TransporRule para criar a política.</span><span class="sxs-lookup"><span data-stu-id="7413d-122">Use the Set-IRMConfiguration and New-TransporRule cmdlets to create the policy.</span></span>

### <a name="example-mail-flow-rule-created-with-powershell"></a><span data-ttu-id="7413d-123">Regra de fluxo de emails de exemplo criada com o PowerShell</span><span class="sxs-lookup"><span data-stu-id="7413d-123">Example mail flow rule created with PowerShell</span></span>

<span data-ttu-id="7413d-124">A execução dos seguintes comandos no PowerShell cria uma regra de fluxo de email do Exchange que criptografa automaticamente os emails que estão fora da sua organização com a política *somente criptografia* se os emails ou seus anexos contiverem as seguintes informações confidenciais tipos de informações:</span><span class="sxs-lookup"><span data-stu-id="7413d-124">Running the following commands in PowerShell create an Exchange mail flow rule that automatically encrypts emails going outside your organization with the *Encrypt-Only* policy if the emails or their attachments contain the following sensitive information types:</span></span>

- <span data-ttu-id="7413d-125">Número de roteamento ABA</span><span class="sxs-lookup"><span data-stu-id="7413d-125">ABA routing number</span></span>
- <span data-ttu-id="7413d-126">Número do cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="7413d-126">Credit card Number</span></span>
- <span data-ttu-id="7413d-127">Número da Agência de aplicação de medicamentos (DEA)</span><span class="sxs-lookup"><span data-stu-id="7413d-127">Drug Enforcement Agency (DEA) number</span></span>
- <span data-ttu-id="7413d-128">EUA/REINO UNIDO</span><span class="sxs-lookup"><span data-stu-id="7413d-128">U.S. / U.K.</span></span> <span data-ttu-id="7413d-129">passport number</span><span class="sxs-lookup"><span data-stu-id="7413d-129">passport number</span></span>
- <span data-ttu-id="7413d-130">Número de conta bancária dos EUA</span><span class="sxs-lookup"><span data-stu-id="7413d-130">U.S. bank account number</span></span>
- <span data-ttu-id="7413d-131">Número de identificação de contribuinte individual (ITIN) dos EUA</span><span class="sxs-lookup"><span data-stu-id="7413d-131">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>
- <span data-ttu-id="7413d-132">Número de seguridade social dos EUA (SSN)</span><span class="sxs-lookup"><span data-stu-id="7413d-132">U.S. Social Security Number (SSN)</span></span>

```powershell
Set-IRMConfiguration -DecryptAttachmentsForEncryptOnly $true
New-TransportRule -Name "Encrypt outbound sensitive emails (out of box rule)" -SentToScope  NotInOrganization  -ApplyRightsProtectionTemplate "Encrypt" -MessageContainsDataClassifications @(@{Name="ABA Routing Number"; minCount="1"},@{Name="Credit Card Number"; minCount="1"},@{Name="Drug Enforcement Agency (DEA) Number"; minCount="1"},@{Name="U.S. / U.K. Passport Number"; minCount="1"},@{Name="U.S. Bank Account Number"; minCount="1"},@{Name="U.S. Individual Taxpayer Identification Number (ITIN)"; minCount="1"},@{Name="U.S. Social Security Number (SSN)"; minCount="1"}) -SenderNotificationType "NotifyOnly"
```

## <a name="how-recipients-access-attachments"></a><span data-ttu-id="7413d-133">Como os destinatários acessam anexos</span><span class="sxs-lookup"><span data-stu-id="7413d-133">How recipients access attachments</span></span>

<span data-ttu-id="7413d-134">Após a criptografia de uma mensagem, os destinatários terão acesso irrestrito aos anexos depois que acessarem e abrirem seus emails criptografados.</span><span class="sxs-lookup"><span data-stu-id="7413d-134">Once a message is encrypted, recipients will have unrestricted access to attachments once they access and open their encrypted email.</span></span>

## <a name="to-prepare-for-this-change"></a><span data-ttu-id="7413d-135">Para se preparar para essa alteração</span><span class="sxs-lookup"><span data-stu-id="7413d-135">To prepare for this change</span></span>

<span data-ttu-id="7413d-136">Talvez você queira atualizar qualquer material de treinamento e documentação do usuário final aplicável para preparar as pessoas em sua organização para essa alteração.</span><span class="sxs-lookup"><span data-stu-id="7413d-136">You may want to update any applicable end-user documentation and training materials to prepare people in your organization for this change.</span></span> <span data-ttu-id="7413d-137">Compartilhe estes recursos de criptografia de mensagem do Office 365 com seus usuários conforme apropriado:</span><span class="sxs-lookup"><span data-stu-id="7413d-137">Share these Office 365 Message Encryption resources with your users as appropriate:</span></span>

- [<span data-ttu-id="7413d-138">Enviar, exibir e responder a mensagens criptografadas no Outlook para PC</span><span class="sxs-lookup"><span data-stu-id="7413d-138">Send, view, and reply to encrypted messages in Outlook for PC</span></span>](https://support.office.com/article/send-view-and-reply-to-encrypted-messages-in-outlook-for-pc-eaa43495-9bbb-4fca-922a-df90dee51980)
- [<span data-ttu-id="7413d-139">Vídeo do Office 365 Essentials: criptografia de mensagem do Office</span><span class="sxs-lookup"><span data-stu-id="7413d-139">Office 365 Essentials Video: Office Message Encryption</span></span>](https://youtu.be/CQR0cG_iEUc)

## <a name="view-these-changes-in-the-audit-log"></a><span data-ttu-id="7413d-140">Exibir essas alterações no log de auditoria</span><span class="sxs-lookup"><span data-stu-id="7413d-140">View these changes in the Audit log</span></span>

<span data-ttu-id="7413d-141">Esta atividade é auditada e está disponível para os administradores do Office 365.</span><span class="sxs-lookup"><span data-stu-id="7413d-141">This activity is audited and is available to Office 365 administrators.</span></span> <span data-ttu-id="7413d-142">A operação é ' New-TransportRule ' e um trecho de uma amostra de entrada de auditoria da pesquisa de log de auditoria no centro de conformidade do & de segurança está abaixo:</span><span class="sxs-lookup"><span data-stu-id="7413d-142">The operation is ‘New-TransportRule’ and a snippet of a sample audit entry from the Audit Log Search in Security & Compliance Center is below:</span></span>

|     |
| --- |
| <span data-ttu-id="7413d-143">*{"CreationTime": "2018-11-28T23:35:01", "ID": "a1b2c3d4-DAA0-4c4f-a019-03a1234a1b0c", "Operation": "New-TransportRule", "OrganizationId": "123456-221d-12345", "RecordType": 1, "ResultStatus": "true", "UserKey": "operador da Microsoft", " UserType ": 3," Version ": 1," Workload ":" Exchange "," ClientIP ":" 123.456.147.68:17584 "," ObjectId ":" "," UserId ":" Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso. onmicrosoft. com "," OriginatingServer ":" CY4PR13MBXXXX ( 15.20.1382.008) "," paraMeters ": {" Name ":" organização "," valor ":" 123456-221d-12346 "{" Name ":" ApplyRightsProtectionTemplate "," value ":" Encrypt "}, {" Name ":" Name "," value ":" criptografar emails confidenciais (regra de entrada) "}, {" Name ":" MessageContainsDataClassifications "... etc.*</span><span class="sxs-lookup"><span data-stu-id="7413d-143">*{"CreationTime":"2018-11-28T23:35:01","Id":"a1b2c3d4-daa0-4c4f-a019-03a1234a1b0c","Operation":"New-TransportRule","OrganizationId":"123456-221d-12345 ","RecordType":1,"ResultStatus":"True","UserKey":"Microsoft Operator","UserType":3,"Version":1,"Workload":"Exchange","ClientIP":"123.456.147.68:17584","ObjectId":"","UserId":"Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso.onmicrosoft.com","OriginatingServer":"CY4PR13MBXXXX (15.20.1382.008)","Parameters": {"Name":"Organization","Value":"123456-221d-12346"{"Name":"ApplyRightsProtectionTemplate","Value":"Encrypt"},{"Name":"Name","Value":"Encrypt outbound sensitive emails (out of box rule)"},{"Name":"MessageContainsDataClassifications”…etc.*</span></span> |
| |

## <a name="to-disable-or-customize-the-sensitive-information-types-policy"></a><span data-ttu-id="7413d-144">Para desabilitar ou personalizar a política de tipos de informações confidenciais</span><span class="sxs-lookup"><span data-stu-id="7413d-144">To disable or customize the sensitive information types policy</span></span>

<span data-ttu-id="7413d-145">Depois de criar a regra de fluxo de emails do Exchange, você pode [desabilitar ou editar a regra](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) indo para**regras** de **fluxo** > de emails no centro de administração do Exchange (Eat) e desabilitar a regra "*criptografar emails confidenciais de saída (regra fora de caixa)* ".</span><span class="sxs-lookup"><span data-stu-id="7413d-145">Once you've created the Exchange mail flow rule, you can [disable or edit the rule](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) by going to **Mail flow** > **Rules** in the Exchange admin center (EAC) and disable the rule “*Encrypt outbound sensitive emails (out of box rule)*”.</span></span>

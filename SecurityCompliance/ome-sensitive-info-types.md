---
title: Nova política de criptografia de mensagem do Office 365 para informações confidenciais
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/7/2019
ROBOTS: NOINDEX, NOFOLLOW
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Resumo: Automaticamente aplicada a política de criptografia de mensagem do Office 365 para tipos de informações confidenciais aplicação a todos os locatários.'
ms.openlocfilehash: f5996707d1cafe8dc1bf90856878de0a4fb7b77b
ms.sourcegitcommit: 30faa3ba91cab4c36e3d8d8ed5858d5269ea8a56
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2019
ms.locfileid: "27752078"
---
# <a name="office-365-message-encryption-policy-for-sensitive-information"></a><span data-ttu-id="6967c-103">Política de criptografia de mensagem do Office 365 para informações confidenciais</span><span class="sxs-lookup"><span data-stu-id="6967c-103">Office 365 Message Encryption policy for sensitive information</span></span>

<span data-ttu-id="6967c-p101">Estamos criando uma nova política automática no locatários do Office 365 que se aplicarão a criptografia de mensagem do Office 365 para todos os emails que contenham informações confidenciais e que estão sendo enviadas de fora da sua organização. Essa nova regra de fluxo de correio do Exchange será automaticamente criada no seu locatário do Office 365 para que a sua organização será protegida por padrão.</span><span class="sxs-lookup"><span data-stu-id="6967c-p101">We will be creating a new automatic policy in Office 365 tenants that will apply Office 365 Message Encryption to all emails that contain sensitive information and that are being sent outside your organization. This new Exchange mail flow rule will be automatically created in your Office 365 tenant so that your organization will be protected by default.</span></span>

## <a name="when-to-expect-the-update-for-your-tenant"></a><span data-ttu-id="6967c-106">Quando esperar que a atualização para o seu locatário</span><span class="sxs-lookup"><span data-stu-id="6967c-106">When to expect the update for your tenant</span></span>

<span data-ttu-id="6967c-p102">Sua organização receberá uma notificação no Centro de mensagem do Office 365 informando a data em que essa diretiva automática será criada no seu locatário. Você receberá pelo menos um aviso de 30 dias e você também terá a opção de recusar. Um cenário em que convém potencialmente rejeitar é se você tiver uma solução de prevenção de perda de dados de terceiros 3rd que já verifica para tipos de confidenciais. Para obter mais detalhes sobre como recusar estão disponíveis neste artigo.</span><span class="sxs-lookup"><span data-stu-id="6967c-p102">Your organization will receive a notification in the Office 365 Message Center notifying you the date on which this automatic policy will be created in your tenant. You will be given at least a 30-day notice and you will also have the option to opt-out. A scenario in which you may want to potentially opt out is if you have a 3rd-party Data Loss Prevention solution that already scans for sensitive types. More details on how to opt-out are available later in this article.</span></span>

## <a name="sensitive-information-type-policy-details"></a><span data-ttu-id="6967c-110">Detalhes de política do tipo de informações confidenciais</span><span class="sxs-lookup"><span data-stu-id="6967c-110">Sensitive information type policy details</span></span>

<span data-ttu-id="6967c-111">Será criada uma regra de fluxo de email do Exchange na sua organização que serão automaticamente criptografados emails indo fora da sua organização com o *Criptografar somente* se eles contêm os seguintes tipos de informações confidenciais de política:</span><span class="sxs-lookup"><span data-stu-id="6967c-111">An Exchange mail flow rule will be created in your organization that will automatically encrypt emails going outside your organization with the *Encrypt-Only* policy if they contain the following sensitive information types:</span></span>

- <span data-ttu-id="6967c-112">Número de roteamento ABA</span><span class="sxs-lookup"><span data-stu-id="6967c-112">ABA routing number</span></span>
- <span data-ttu-id="6967c-113">Número de cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="6967c-113">Credit card Number</span></span>
- <span data-ttu-id="6967c-114">Número do Drug imposição Agency (DEA)</span><span class="sxs-lookup"><span data-stu-id="6967c-114">Drug Enforcement Agency (DEA) number</span></span>
- <span data-ttu-id="6967c-p103">US / número de passaporte do Reino Unido</span><span class="sxs-lookup"><span data-stu-id="6967c-p103">U.S. / U.K. passport number</span></span>
- <span data-ttu-id="6967c-117">Número de conta bancária dos EUA</span><span class="sxs-lookup"><span data-stu-id="6967c-117">U.S. bank account number</span></span>
- <span data-ttu-id="6967c-118">Número de identificação de contribuinte individual (ITIN) dos EUA</span><span class="sxs-lookup"><span data-stu-id="6967c-118">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>
- <span data-ttu-id="6967c-119">Número de seguridade social dos EUA (SSN)</span><span class="sxs-lookup"><span data-stu-id="6967c-119">U.S. Social Security Number (SSN)</span></span>

> [!Note]
> <span data-ttu-id="6967c-120">Os tipos de confidenciais exatos podem diferir por localidade da sua organização e serão comunicados na notificação de centro de mensagens.</span><span class="sxs-lookup"><span data-stu-id="6967c-120">The exact sensitive types may differ by your organization’s locale and will be communicated in the Message Center notification.</span></span>

## <a name="what-do-i-need-to-do-to-prepare-for-this-change"></a><span data-ttu-id="6967c-121">O que é necessário fazer para preparar para que essa alteração?</span><span class="sxs-lookup"><span data-stu-id="6967c-121">What do I need to do to prepare for this change?</span></span>

<span data-ttu-id="6967c-p104">Você não precisará atualizar ou modificar quaisquer definições de configuração do Office 365 existentes antes dessa nova alteração. No entanto, convém atualizar qualquer documentação aplicável do usuário final e materiais de treinamento para preparar a pessoas da sua organização para que essa alteração. Compartilhe esses recursos do Office 365 Message Encryption com seus usuários, conforme apropriado:</span><span class="sxs-lookup"><span data-stu-id="6967c-p104">You do not have to update or modify any existing Office 365 configuration settings prior to this new change. However, you may want to update any applicable end-user documentation and training materials to prepare people in your organization for this change. Share these Office 365 Message Encryption resources with your users as appropriate:</span></span>

- [<span data-ttu-id="6967c-125">Enviar, visualizar e responder a mensagens criptografadas no Outlook para PC</span><span class="sxs-lookup"><span data-stu-id="6967c-125">Send, view, and reply to encrypted messages in Outlook for PC</span></span>](https://support.office.com/article/send-view-and-reply-to-encrypted-messages-in-outlook-for-pc-eaa43495-9bbb-4fca-922a-df90dee51980)
- [<span data-ttu-id="6967c-126">Vídeo do Office 365 Essentials: Criptografia de mensagem do Office</span><span class="sxs-lookup"><span data-stu-id="6967c-126">Office 365 Essentials Video: Office Message Encryption</span></span>](https://youtu.be/CQR0cG_iEUc)

## <a name="how-will-this-change-be-represented-in-the-audit-log"></a><span data-ttu-id="6967c-127">Como essa alteração será representada no log de auditoria?</span><span class="sxs-lookup"><span data-stu-id="6967c-127">How will this change be represented in the Audit log?</span></span>

<span data-ttu-id="6967c-p105">Esta atividade é auditada e está disponível para clientes.  A operação é 'New-TransportRule' e um trecho de uma entrada de auditoria de amostra da pesquisa de Log de auditoria no Centro de conformidade e segurança está abaixo:</span><span class="sxs-lookup"><span data-stu-id="6967c-p105">This activity is audited and is available to customers.  The operation is ‘New-TransportRule’ and a snippet of a sample audit entry from the Audit Log Search in Security & Compliance Center is below:</span></span>

|     |
| --- |
| <span data-ttu-id="6967c-130">*{"CreationTime":"2018-11-28T23:35:01","Id":"a1b2c3d4-daa0-4c4f-a019-03a1234a1b0c","Operation":"New-TransportRule","OrganizationId":"123456-221d-12345", "RecordType": 1, "ResultStatus": "True", "UserKey": "Microsoft operador"," UserType": 3,"versão": 1,"carga de trabalho":"Do Exchange","ClientIP":"123.456.147.68:17584","ObjectId":"UserId "," ":"Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso.onmicrosoft.com","OriginatingServer":"CY4PR13MBXXXX ( 15.20.1382.008)","Parameters": {"Name":"Organização","Valor":" 123456-221 d - 12346"{"Name":"ApplyRightsProtectionTemplate","Valor":"Criptografar"}, {"Name":"Nome"e"Valor":"Criptografar emails de saída confidenciais (sem regra caixa)"}, {"Name":" MessageContainsDataClassifications"… etc.*</span><span class="sxs-lookup"><span data-stu-id="6967c-130">*{"CreationTime":"2018-11-28T23:35:01","Id":"a1b2c3d4-daa0-4c4f-a019-03a1234a1b0c","Operation":"New-TransportRule","OrganizationId":"123456-221d-12345 ","RecordType":1,"ResultStatus":"True","UserKey":"Microsoft Operator","UserType":3,"Version":1,"Workload":"Exchange","ClientIP":"123.456.147.68:17584","ObjectId":"","UserId":"Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso.onmicrosoft.com","OriginatingServer":"CY4PR13MBXXXX (15.20.1382.008)","Parameters": {"Name":"Organization","Value":"123456-221d-12346"{"Name":"ApplyRightsProtectionTemplate","Value":"Encrypt"},{"Name":"Name","Value":"Encrypt outbound sensitive emails (out of box rule)"},{"Name":"MessageContainsDataClassifications”…etc.*</span></span>
 |

## <a name="how-do-i-opt-out"></a><span data-ttu-id="6967c-131">Como eu sair?</span><span class="sxs-lookup"><span data-stu-id="6967c-131">How do I opt-out?</span></span>

<span data-ttu-id="6967c-132">Se você gostaria de recusar essa alteração, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="6967c-132">If you would like to opt-out of this change, please follow these steps:</span></span>

1. <span data-ttu-id="6967c-p106">Usando uma conta de trabalho ou da escola que tenha permissões de administrador global na sua organização do Office 365, iniciar uma sessão do Windows PowerShell e se conectar ao Exchange Online. Para obter instruções, consulte [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="6967c-p106">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online. For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>
2. <span data-ttu-id="6967c-135">Execute o cmdlet Set-IRMConfiguration da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="6967c-135">Run the Set-IRMConfiguration cmdlet as follows:</span></span>

   ```
   Set-IRMConfiguration -AutomaticServiceUpdateEnabled $false
   ```

## <a name="how-do-i-disable-the-automatic-policy"></a><span data-ttu-id="6967c-136">Como desabilitar o a diretiva automática?</span><span class="sxs-lookup"><span data-stu-id="6967c-136">How do I disable the automatic policy?</span></span>

<span data-ttu-id="6967c-137">Se você não tiver recusar essa alteração e a regra de correio do Exchange tiver sido criada, você pode [Desabilitar a regra](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) indo para **fluxo de email** > **regras** em que o administrador do Exchange center (EAC) e desabilitar a regra "*criptografar saída emails confidenciais (sem regra caixa)*".</span><span class="sxs-lookup"><span data-stu-id="6967c-137">If you didn’t opt-out of this change and the Exchange mail rule has already been created, you can [disable the rule](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) by going to **Mail flow** > **Rules** in the Exchange admin center (EAC) and disable the rule “*Encrypt outbound sensitive emails (out of box rule)*”.</span></span>

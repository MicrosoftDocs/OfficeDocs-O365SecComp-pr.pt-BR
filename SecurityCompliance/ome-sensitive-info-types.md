---
title: Nova política de criptografia de mensagem do Office 365 para informações confidenciais
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/16/2019
ROBOTS: NOINDEX, NOFOLLOW
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Resumo: Automaticamente aplicada a política de criptografia de mensagem do Office 365 para tipos de informações confidenciais aplicação a todos os locatários.'
ms.openlocfilehash: f83bf0fe572586b3becf2dd53395e611bdaaea24
ms.sourcegitcommit: 03b9221d9885bcde1cdb5df2c2dc5d835802d299
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29614375"
---
# <a name="office-365-message-encryption-policy-for-sensitive-information"></a><span data-ttu-id="9c047-103">Política de criptografia de mensagem do Office 365 para informações confidenciais</span><span class="sxs-lookup"><span data-stu-id="9c047-103">Office 365 Message Encryption policy for sensitive information</span></span>

<span data-ttu-id="9c047-p101">Para um grupo seleto de locatários, com base em sua organização tamanho e complexidade do fluxo de mensagens, estamos fazendo uma distribuídas lenta de uma nova diretiva automática no que se aplicarão a criptografia de mensagem do Office 365 para emails que contenham certos tipos de confidenciais locatários do Office 365 informações. Estamos testando isso com um pequeno grupo de inquilinos. Essa diretiva não será aplicada a todas as organizações e considerações sobre como o tamanho da organização e a complexidade do fluxo de email será usada para determinar a qualificação para este distribuídas. Se sua organização estiver selecionada para este distribuídas, você receberá uma notificação no Centro de mensagem do Office 365 informando a data em que essa diretiva automática será criada e você receberá pelo menos um aviso de 30 dias e a opção para sair. Se você não quer esperar para a Microsoft criar essa diretiva e gostaria de fazê-lo si, você pode criar essa diretiva automática usando regras de fluxo de emails do Exchange.</span><span class="sxs-lookup"><span data-stu-id="9c047-p101">For a select group of tenants, based on their organization size and complexity of mail flow, we are doing a slow roll-out of a new automatic policy in Office 365 tenants that will apply Office 365 Message Encryption to emails that contain certain types of sensitive information. We are testing this with a small group of tenants. This policy will not be rolled out to all organizations and considerations such as organization size and complexity of mail flow will be used to determine the eligibility for this roll-out. If your organization is selected for this roll-out, you will receive a notification in the Office 365 Message Center notifying you the date on which this automatic policy will be created and you will be given at least a 30-day notice and the option to opt-out. If you don't want to wait for Microsoft to create this policy and would like to do so yourselves, you can create this automatic policy using Exchange Mail Flow rules.</span></span>

## <a name="when-to-expect-the-update-for-your-tenant"></a><span data-ttu-id="9c047-107">Quando esperar que a atualização para o seu locatário</span><span class="sxs-lookup"><span data-stu-id="9c047-107">When to expect the update for your tenant</span></span>

<span data-ttu-id="9c047-p102">Sua organização receberá uma notificação no Centro de mensagem do Office 365 informando a data em que essa diretiva automática será criada no seu locatário. Você receberá pelo menos um aviso de 30 dias e você também terá a opção de recusar. Um cenário em que convém potencialmente rejeitar é se você tiver uma solução de prevenção de perda de dados de terceiros 3rd que já verifica para tipos de confidenciais. Para obter mais detalhes sobre como recusar estão disponíveis neste artigo.</span><span class="sxs-lookup"><span data-stu-id="9c047-p102">Your organization will receive a notification in the Office 365 Message Center notifying you the date on which this automatic policy will be created in your tenant. You will be given at least a 30-day notice and you will also have the option to opt-out. A scenario in which you may want to potentially opt out is if you have a 3rd-party Data Loss Prevention solution that already scans for sensitive types. More details on how to opt-out are available later in this article.</span></span>

## <a name="sensitive-information-type-policy-details"></a><span data-ttu-id="9c047-111">Detalhes de política do tipo de informações confidenciais</span><span class="sxs-lookup"><span data-stu-id="9c047-111">Sensitive information type policy details</span></span>

<span data-ttu-id="9c047-112">Será criada uma regra de fluxo de email do Exchange na sua organização que serão automaticamente criptografados emails indo fora da sua organização com o *Criptografar somente* se os emails ou seus anexos contenham os seguintes tipos de informações confidenciais de política:</span><span class="sxs-lookup"><span data-stu-id="9c047-112">An Exchange mail flow rule will be created in your organization that will automatically encrypt emails going outside your organization with the *Encrypt-Only* policy if the emails or their attachments contain the following sensitive information types:</span></span>

- <span data-ttu-id="9c047-113">Número de roteamento ABA</span><span class="sxs-lookup"><span data-stu-id="9c047-113">ABA routing number</span></span>
- <span data-ttu-id="9c047-114">Número de cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="9c047-114">Credit card Number</span></span>
- <span data-ttu-id="9c047-115">Número do Drug imposição Agency (DEA)</span><span class="sxs-lookup"><span data-stu-id="9c047-115">Drug Enforcement Agency (DEA) number</span></span>
- <span data-ttu-id="9c047-p103">US / número de passaporte do Reino Unido</span><span class="sxs-lookup"><span data-stu-id="9c047-p103">U.S. / U.K. passport number</span></span>
- <span data-ttu-id="9c047-118">Número de conta bancária dos EUA</span><span class="sxs-lookup"><span data-stu-id="9c047-118">U.S. bank account number</span></span>
- <span data-ttu-id="9c047-119">Número de identificação de contribuinte individual (ITIN) dos EUA</span><span class="sxs-lookup"><span data-stu-id="9c047-119">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>
- <span data-ttu-id="9c047-120">Número de seguridade social dos EUA (SSN)</span><span class="sxs-lookup"><span data-stu-id="9c047-120">U.S. Social Security Number (SSN)</span></span>

> [!Note]
> <span data-ttu-id="9c047-121">Os tipos de confidenciais exatos podem diferir por localidade da sua organização e serão comunicados na notificação de centro de mensagens.</span><span class="sxs-lookup"><span data-stu-id="9c047-121">The exact sensitive types may differ by your organization’s locale and will be communicated in the Message Center notification.</span></span>

## <a name="what-do-i-need-to-do-to-prepare-for-this-change"></a><span data-ttu-id="9c047-122">O que é necessário fazer para preparar para que essa alteração?</span><span class="sxs-lookup"><span data-stu-id="9c047-122">What do I need to do to prepare for this change?</span></span>

<span data-ttu-id="9c047-p104">Você não precisará atualizar ou modificar quaisquer definições de configuração do Office 365 existentes antes dessa nova alteração. No entanto, convém atualizar qualquer documentação aplicável do usuário final e materiais de treinamento para preparar a pessoas da sua organização para que essa alteração. Compartilhe esses recursos do Office 365 Message Encryption com seus usuários, conforme apropriado:</span><span class="sxs-lookup"><span data-stu-id="9c047-p104">You do not have to update or modify any existing Office 365 configuration settings prior to this new change. However, you may want to update any applicable end-user documentation and training materials to prepare people in your organization for this change. Share these Office 365 Message Encryption resources with your users as appropriate:</span></span>

- [<span data-ttu-id="9c047-126">Enviar, visualizar e responder a mensagens criptografadas no Outlook para PC</span><span class="sxs-lookup"><span data-stu-id="9c047-126">Send, view, and reply to encrypted messages in Outlook for PC</span></span>](https://support.office.com/article/send-view-and-reply-to-encrypted-messages-in-outlook-for-pc-eaa43495-9bbb-4fca-922a-df90dee51980)
- [<span data-ttu-id="9c047-127">Vídeo do Office 365 Essentials: Criptografia de mensagem do Office</span><span class="sxs-lookup"><span data-stu-id="9c047-127">Office 365 Essentials Video: Office Message Encryption</span></span>](https://youtu.be/CQR0cG_iEUc)

## <a name="how-will-this-change-be-represented-in-the-audit-log"></a><span data-ttu-id="9c047-128">Como essa alteração será representada no log de auditoria?</span><span class="sxs-lookup"><span data-stu-id="9c047-128">How will this change be represented in the Audit log?</span></span>

<span data-ttu-id="9c047-p105">Esta atividade é auditada e está disponível para clientes.  A operação é 'New-TransportRule' e um trecho de uma entrada de auditoria de amostra da pesquisa de Log de auditoria no Centro de conformidade de & de segurança está abaixo:</span><span class="sxs-lookup"><span data-stu-id="9c047-p105">This activity is audited and is available to customers.  The operation is ‘New-TransportRule’ and a snippet of a sample audit entry from the Audit Log Search in Security & Compliance Center is below:</span></span>

|     |
| --- |
| <span data-ttu-id="9c047-131">*{"CreationTime":"2018-11-28T23:35:01","Id":"a1b2c3d4-daa0-4c4f-a019-03a1234a1b0c","Operation":"New-TransportRule","OrganizationId":"123456-221d-12345", "RecordType": 1, "ResultStatus": "True", "UserKey": "Microsoft operador"," UserType": 3,"versão": 1,"carga de trabalho":"Do Exchange","ClientIP":"123.456.147.68:17584","ObjectId":"UserId "," ":"Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso.onmicrosoft.com","OriginatingServer":"CY4PR13MBXXXX ( 15.20.1382.008)","Parameters": {"Name":"Organização","Valor":" 123456-221 d - 12346"{"Name":"ApplyRightsProtectionTemplate","Valor":"Criptografar"}, {"Name":"Nome"e"Valor":"Criptografar emails de saída confidenciais (sem regra caixa)"}, {"Name":" MessageContainsDataClassifications"… etc.*</span><span class="sxs-lookup"><span data-stu-id="9c047-131">*{"CreationTime":"2018-11-28T23:35:01","Id":"a1b2c3d4-daa0-4c4f-a019-03a1234a1b0c","Operation":"New-TransportRule","OrganizationId":"123456-221d-12345 ","RecordType":1,"ResultStatus":"True","UserKey":"Microsoft Operator","UserType":3,"Version":1,"Workload":"Exchange","ClientIP":"123.456.147.68:17584","ObjectId":"","UserId":"Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso.onmicrosoft.com","OriginatingServer":"CY4PR13MBXXXX (15.20.1382.008)","Parameters": {"Name":"Organization","Value":"123456-221d-12346"{"Name":"ApplyRightsProtectionTemplate","Value":"Encrypt"},{"Name":"Name","Value":"Encrypt outbound sensitive emails (out of box rule)"},{"Name":"MessageContainsDataClassifications”…etc.*</span></span>
 |

## <a name="how-do-i-opt-out"></a><span data-ttu-id="9c047-132">Como eu sair?</span><span class="sxs-lookup"><span data-stu-id="9c047-132">How do I opt-out?</span></span>

<span data-ttu-id="9c047-133">Se você gostaria de recusar essa alteração, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="9c047-133">If you would like to opt-out of this change, please follow these steps:</span></span>

1. <span data-ttu-id="9c047-p106">Usando uma conta de trabalho ou da escola que tenha permissões de administrador global na sua organização do Office 365, iniciar uma sessão do Windows PowerShell e se conectar ao Exchange Online. Para obter instruções, consulte [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="9c047-p106">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online. For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>
2. <span data-ttu-id="9c047-136">Execute o cmdlet Set-IRMConfiguration da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="9c047-136">Run the Set-IRMConfiguration cmdlet as follows:</span></span>

   ```
   Set-IRMConfiguration -AutomaticServiceUpdateEnabled $false
   ```

## <a name="how-do-i-disable-or-customize-the-automatic-policy"></a><span data-ttu-id="9c047-137">Como desabilitar ou personalizar a diretiva automática?</span><span class="sxs-lookup"><span data-stu-id="9c047-137">How do I disable or customize the automatic policy?</span></span>

<span data-ttu-id="9c047-138">Se você não tiver recusar essa alteração e a regra de fluxo de email do Exchange tiver sido criada, você pode [desabilitar ou editar a regra](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) indo para **fluxo de email** > **regras** em que o administrador do Exchange center (EAC) e desabilitar a regra "*criptografar emails de saída confidenciais (sem regra caixa)*".</span><span class="sxs-lookup"><span data-stu-id="9c047-138">If you didn’t opt-out of this change and the Exchange mail flow rule has already been created, you can [disable or edit the rule](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) by going to **Mail flow** > **Rules** in the Exchange admin center (EAC) and disable the rule “*Encrypt outbound sensitive emails (out of box rule)*”.</span></span>

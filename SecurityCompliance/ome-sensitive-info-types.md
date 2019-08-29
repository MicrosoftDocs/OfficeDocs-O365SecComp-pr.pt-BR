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
# <a name="create-a-sensitive-information-type-policy-for-your-organization-using-office-365-message-encryption"></a>Criar uma política de tipo de informação confidencial para sua organização usando a criptografia de mensagem do Office 365

Você pode usar as regras de fluxo de email do Exchange ou a prevenção de perda de dados do Office 365 (DLP) para criar uma política de tipo de informação confidencial com a criptografia de mensagem do Office 365. Para criar uma regra de fluxo de email do Exchange, você pode usar o centro de administração do Exchange (Eat) ou o PowerShell.

### <a name="to-create-the-policy-by-using-mail-flow-rules-in-the-eac"></a>Para criar a política usando regras de fluxo de emails no Eat

Entre no centro de administração do Exchange (Eat) e vá para **** > **regras**de fluxo de emails. Na página regras, crie uma regra que aplique a criptografia de mensagem do Office 365. Você pode criar uma regra com base em condições como a presença de determinadas palavras-chave ou tipos de informações confidenciais na mensagem ou no anexo.

### <a name="to-create-the-policy-by-using-mail-flow-rules-in-powershell"></a>Para criar a política usando regras de fluxo de email no PowerShell

Use uma conta corporativa ou de estudante que tenha permissões de administrador global em sua organização do Office 365, inicie uma sessão do Windows PowerShell e conecte-se ao Exchange Online. Para obter instruções, consulte [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell). Use os cmdlets Set-IRMConfiguration e New-TransportRule para criar a política.

### <a name="example-mail-flow-rule-created-with-powershell"></a>Regra de fluxo de emails de exemplo criada com o PowerShell

Execute os seguintes comandos no PowerShell para criar uma regra de fluxo de email do Exchange que criptografa automaticamente os emails enviados fora da sua organização com a política *somente criptografia* se os emails ou seus anexos contiverem as seguintes informações confidenciais digitar

- Número de roteamento ABA
- Número do cartão de crédito
- Número da Agência de aplicação de medicamentos (DEA)
- EUA/REINO UNIDO passport number
- Número de conta bancária dos EUA
- Número de identificação de contribuinte individual (ITIN) dos EUA
- Número de seguridade social dos EUA (SSN)

```powershell
Set-IRMConfiguration -DecryptAttachmentForEncryptOnly $true
New-TransportRule -Name "Encrypt outbound sensitive emails (out of box rule)" -SentToScope  NotInOrganization  -ApplyRightsProtectionTemplate "Encrypt" -MessageContainsDataClassifications @(@{Name="ABA Routing Number"; minCount="1"},@{Name="Credit Card Number"; minCount="1"},@{Name="Drug Enforcement Agency (DEA) Number"; minCount="1"},@{Name="U.S. / U.K. Passport Number"; minCount="1"},@{Name="U.S. Bank Account Number"; minCount="1"},@{Name="U.S. Individual Taxpayer Identification Number (ITIN)"; minCount="1"},@{Name="U.S. Social Security Number (SSN)"; minCount="1"}) -SenderNotificationType "NotifyOnly"
```

Para obter mais informações, consulte [Set-IRMConfiguration](https://docs.microsoft.com/en-us/powershell/module/exchange/encryption-and-certificates/set-irmconfiguration?view=exchange-ps) e [New-TransportRule](https://docs.microsoft.com/en-us/powershell/module/exchange/policy-and-compliance/New-TransportRule?view=exchange-ps).

## <a name="how-recipients-access-attachments"></a>Como os destinatários acessam anexos

Depois que o Office 365 criptografa uma mensagem, os destinatários têm acesso irrestrito aos anexos quando acessam e abrem seus emails criptografados.

## <a name="to-prepare-for-this-change"></a>Para se preparar para essa alteração

Talvez você queira atualizar qualquer material de treinamento e documentação do usuário final aplicável para preparar as pessoas em sua organização para essa alteração. Compartilhe estes recursos de criptografia de mensagem do Office 365 com seus usuários conforme apropriado:

- [Enviar, exibir e responder a mensagens criptografadas no Outlook para PC](https://support.office.com/article/send-view-and-reply-to-encrypted-messages-in-outlook-for-pc-eaa43495-9bbb-4fca-922a-df90dee51980)
- [Vídeo do Office 365 Essentials: criptografia de mensagem do Office](https://youtu.be/CQR0cG_iEUc)

## <a name="view-these-changes-in-the-audit-log"></a>Exibir essas alterações no log de auditoria

O Office 365 audita essa atividade e a disponibiliza para os administradores do Office 365. A operação é ' New-TransportRule ' e um trecho de uma amostra de auditoria de entrada da pesquisa de log de auditoria no centro de conformidade de segurança & está abaixo:

```text
*{"CreationTime":"2018-11-28T23:35:01","Id":"a1b2c3d4-daa0-4c4f-a019-03a1234a1b0c","Operation":"New-TransportRule","OrganizationId":"123456-221d-12345 ","RecordType":1,"ResultStatus":"True","UserKey":"Microsoft Operator","UserType":3,"Version":1,"Workload":"Exchange","ClientIP":"123.456.147.68:17584","ObjectId":"","UserId":"Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso.onmicrosoft.com","OriginatingServer":"CY4PR13MBXXXX (15.20.1382.008)","Parameters": {"Name":"Organization","Value":"123456-221d-12346"{"Name":"ApplyRightsProtectionTemplate","Value":"Encrypt"},{"Name":"Name","Value":"Encrypt outbound sensitive emails (out of box rule)"},{"Name":"MessageContainsDataClassifications”…etc.*
```

## <a name="to-disable-or-customize-the-sensitive-information-types-policy"></a>Para desabilitar ou personalizar a política de tipos de informações confidenciais

Depois de criar a regra de fluxo de emails do Exchange, você pode [desabilitar ou editar a regra](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) indo para**regras** de **fluxo** > de emails no centro de administração do Exchange (Eat) e desabilitar a regra "*criptografar emails confidenciais de saída (regra fora de caixa)* ".

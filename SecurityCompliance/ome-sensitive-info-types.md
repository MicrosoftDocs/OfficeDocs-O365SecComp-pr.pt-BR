---
title: Política de criptografia de mensagem do Office 365 para informações confidenciais
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/31/2019
ROBOTS: NOINDEX, NOFOLLOW
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Resumo: política de criptografia de mensagem do Office 365 para tipos de informações confidenciais agora disponível.'
ms.openlocfilehash: e2a72ee85ca65a2fe8ae1543979b51915ff0a88f
ms.sourcegitcommit: 24659bdb09f49d0ffed180a4b80bbb7c45c2d301
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2019
ms.locfileid: "29696195"
---
# <a name="office-365-message-encryption-policy-for-sensitive-information"></a>Política de criptografia de mensagem do Office 365 para informações confidenciais

Atualização (1/30/19): em outubro de 2018, trabalhamos com uma pequena amostra de clientes para entender se podemos simplificar a proteção criptografando automaticamente emails confidenciais com base em determinados tipos de informações confidenciais. Com base nos comentários positivos deste exemplo, decidimos expandir para um perfil mais variado de locatários em dezembro de 2018. Depois de comunicar a próxima implantação para selecionar locatários, ouvimos seus comentários e determinamos que os clientes com ambientes mais complexos queriam implementar as regras com mais cautela, e estamos, portanto, ajustando nossos planos.

Se sua organização foi selecionada para a distribuição a partir de 15 de janeiro de 2019, não iremos distribuir a política automática. Em vez disso, forneceremos instruções neste artigo sobre como você pode concluir o yourselves de distribuição. Continue lendo para saber como.

||
|:-----|
|Este artigo faz parte de uma série maior de artigos sobre a criptografia de mensagens do Office 365. Este artigo destina-se a administradores e ITPros. Se você estiver apenas procurando informações sobre como enviar ou receber uma mensagem criptografada, consulte a lista de artigos na [ome (criptografia de mensagens do Office 365)](ome.md) e localize o artigo que melhor atende às suas necessidades. |
||

## <a name="how-to-create-the-sensitive-information-type-policy-for-your-tenant"></a>Como criar a política de tipo de informação confidencial para o locatário

Você pode usar as regras de fluxo de email do Exchange ou a prevenção de perda de dados do Office 365 (DLP) para criar a política de tipo de informação confidencial. Para criar uma regra de fluxo de email do Exchange, você pode usar o centro de administração do Exchange (Eat) ou o PowerShell.

### <a name="to-create-the-policy-by-using-mail-flow-rules-in-the-eac"></a>Para criar a política usando regras de fluxo de emails no Eat

Entre no centro de administração do Exchange (Eat) e vá para**regras**de **fluxo** > de emails. Lá, crie uma regra que aplique a criptografia de mensagem do Office 365 com base em condições como a presença de determinadas palavras-chave ou tipos de informações confidenciais na mensagem ou no anexo.

### <a name="to-create-the-policy-by-using-mail-flow-rules-in-powershell"></a>Para criar a política usando regras de fluxo de email no PowerShell

Usando uma conta corporativa ou de estudante que tenha permissões de administrador global em sua organização do Office 365, inicie uma sessão do Windows PowerShell e conecte-se ao Exchange Online. Para obter instruções, consulte [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell). Use os cmdlets Set-IRMConfiguration e New-TransporRule para criar a política.

### <a name="example-mail-flow-rule-created-with-powershell"></a>Regra de fluxo de emails de exemplo criada com o PowerShell

A execução dos seguintes comandos no PowerShell cria uma regra de fluxo de email do Exchange que criptografa automaticamente os emails que estão fora da sua organização com a política *somente criptografia* se os emails ou seus anexos contiverem as seguintes informações confidenciais tipos de informações:

- Número de roteamento ABA
- Número do cartão de crédito
- Número da Agência de aplicação de medicamentos (DEA)
- Número de passaporte americano/Reino Unido
- Número de conta bancária dos EUA
- Número de identificação de contribuinte individual (ITIN) dos EUA
- Número de seguridade social dos EUA (SSN)

```powershell
Set-IRMConfiguration -DecryptAttachmentsForEncryptOnly $true
New-TransportRule -Name "Encrypt outbound sensitive emails (out of box rule)" -SentToScope  NotInOrganization  -ApplyRightsProtectionTemplate "Encrypt" -MessageContainsDataClassifications @(@{Name="ABA Routing Number"; minCount="1"},@{Name="Credit Card Number"; minCount="1"},@{Name="Drug Enforcement Agency (DEA) Number"; minCount="1"},@{Name="U.S. / U.K. Passport Number"; minCount="1"},@{Name="U.S. Bank Account Number"; minCount="1"},@{Name="U.S. Individual Taxpayer Identification Number (ITIN)"; minCount="1"},@{Name="U.S. Social Security Number (SSN)"; minCount="1"}) -SenderNotificationType "NotifyOnly"
```

## <a name="how-recipients-access-attachments"></a>Como os destinatários acessam anexos

Após a criptografia de uma mensagem, os destinatários terão acesso irrestrito aos anexos depois que acessarem e abrirem seus emails criptografados.

## <a name="to-prepare-for-this-change"></a>Para se preparar para essa alteração

Talvez você queira atualizar qualquer material de treinamento e documentação do usuário final aplicável para preparar as pessoas em sua organização para essa alteração. Compartilhe estes recursos de criptografia de mensagem do Office 365 com seus usuários conforme apropriado:

- [Enviar, exibir e responder a mensagens criptografadas no Outlook para PC](https://support.office.com/article/send-view-and-reply-to-encrypted-messages-in-outlook-for-pc-eaa43495-9bbb-4fca-922a-df90dee51980)
- [Vídeo do Office 365 Essentials: criptografia de mensagem do Office](https://youtu.be/CQR0cG_iEUc)

## <a name="view-these-changes-in-the-audit-log"></a>Exibir essas alterações no log de auditoria

Esta atividade é auditada e está disponível para os administradores do Office 365. A operação é ' New-TransportRule ' e um trecho de uma amostra de entrada de auditoria da pesquisa de log de auditoria no centro de conformidade do & de segurança está abaixo:

|     |
| --- |
| *{"CreationTime": "2018-11-28T23:35:01", "ID": "a1b2c3d4-DAA0-4c4f-a019-03a1234a1b0c", "Operation": "New-TransportRule", "OrganizationId": "123456-221d-12345", "RecordType": 1, "ResultStatus": "true", "UserKey": "operador da Microsoft", " UserType ": 3," Version ": 1," Workload ":" Exchange "," ClientIP ":" 123.456.147.68:17584 "," ObjectId ":" "," UserId ":" Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso. onmicrosoft. com "," OriginatingServer ":" CY4PR13MBXXXX ( 15.20.1382.008) "," paraMeters ": {" Name ":" organização "," valor ":" 123456-221d-12346 "{" Name ":" ApplyRightsProtectionTemplate "," value ":" Encrypt "}, {" Name ":" Name "," value ":" criptografar emails confidenciais (regra de entrada) "}, {" Name ":" MessageContainsDataClassifications "... etc.* |
| |

## <a name="to-disable-or-customize-the-sensitive-information-types-policy"></a>Para desabilitar ou personalizar a política de tipos de informações confidenciais

Depois de criar a regra de fluxo de emails do Exchange, você pode [desabilitar ou editar a regra](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) indo para**regras** de **fluxo** > de emails no centro de administração do Exchange (Eat) e desabilitar a regra "*criptografar emails confidenciais de saída (regra fora de caixa)* ".

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
# <a name="office-365-message-encryption-policy-for-sensitive-information"></a>Política de criptografia de mensagem do Office 365 para informações confidenciais

Para um grupo seleto de locatários, com base em sua organização tamanho e complexidade do fluxo de mensagens, estamos fazendo uma distribuídas lenta de uma nova diretiva automática no que se aplicarão a criptografia de mensagem do Office 365 para emails que contenham certos tipos de confidenciais locatários do Office 365 informações. Estamos testando isso com um pequeno grupo de inquilinos. Essa diretiva não será aplicada a todas as organizações e considerações sobre como o tamanho da organização e a complexidade do fluxo de email será usada para determinar a qualificação para este distribuídas. Se sua organização estiver selecionada para este distribuídas, você receberá uma notificação no Centro de mensagem do Office 365 informando a data em que essa diretiva automática será criada e você receberá pelo menos um aviso de 30 dias e a opção para sair. Se você não quer esperar para a Microsoft criar essa diretiva e gostaria de fazê-lo si, você pode criar essa diretiva automática usando regras de fluxo de emails do Exchange.

## <a name="when-to-expect-the-update-for-your-tenant"></a>Quando esperar que a atualização para o seu locatário

Sua organização receberá uma notificação no Centro de mensagem do Office 365 informando a data em que essa diretiva automática será criada no seu locatário. Você receberá pelo menos um aviso de 30 dias e você também terá a opção de recusar. Um cenário em que convém potencialmente rejeitar é se você tiver uma solução de prevenção de perda de dados de terceiros 3rd que já verifica para tipos de confidenciais. Para obter mais detalhes sobre como recusar estão disponíveis neste artigo.

## <a name="sensitive-information-type-policy-details"></a>Detalhes de política do tipo de informações confidenciais

Será criada uma regra de fluxo de email do Exchange na sua organização que serão automaticamente criptografados emails indo fora da sua organização com o *Criptografar somente* se os emails ou seus anexos contenham os seguintes tipos de informações confidenciais de política:

- Número de roteamento ABA
- Número de cartão de crédito
- Número do Drug imposição Agency (DEA)
- US / número de passaporte do Reino Unido
- Número de conta bancária dos EUA
- Número de identificação de contribuinte individual (ITIN) dos EUA
- Número de seguridade social dos EUA (SSN)

> [!Note]
> Os tipos de confidenciais exatos podem diferir por localidade da sua organização e serão comunicados na notificação de centro de mensagens.

## <a name="what-do-i-need-to-do-to-prepare-for-this-change"></a>O que é necessário fazer para preparar para que essa alteração?

Você não precisará atualizar ou modificar quaisquer definições de configuração do Office 365 existentes antes dessa nova alteração. No entanto, convém atualizar qualquer documentação aplicável do usuário final e materiais de treinamento para preparar a pessoas da sua organização para que essa alteração. Compartilhe esses recursos do Office 365 Message Encryption com seus usuários, conforme apropriado:

- [Enviar, visualizar e responder a mensagens criptografadas no Outlook para PC](https://support.office.com/article/send-view-and-reply-to-encrypted-messages-in-outlook-for-pc-eaa43495-9bbb-4fca-922a-df90dee51980)
- [Vídeo do Office 365 Essentials: Criptografia de mensagem do Office](https://youtu.be/CQR0cG_iEUc)

## <a name="how-will-this-change-be-represented-in-the-audit-log"></a>Como essa alteração será representada no log de auditoria?

Esta atividade é auditada e está disponível para clientes.  A operação é 'New-TransportRule' e um trecho de uma entrada de auditoria de amostra da pesquisa de Log de auditoria no Centro de conformidade de & de segurança está abaixo:

|     |
| --- |
| *{"CreationTime":"2018-11-28T23:35:01","Id":"a1b2c3d4-daa0-4c4f-a019-03a1234a1b0c","Operation":"New-TransportRule","OrganizationId":"123456-221d-12345", "RecordType": 1, "ResultStatus": "True", "UserKey": "Microsoft operador"," UserType": 3,"versão": 1,"carga de trabalho":"Do Exchange","ClientIP":"123.456.147.68:17584","ObjectId":"UserId "," ":"Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso.onmicrosoft.com","OriginatingServer":"CY4PR13MBXXXX ( 15.20.1382.008)","Parameters": {"Name":"Organização","Valor":" 123456-221 d - 12346"{"Name":"ApplyRightsProtectionTemplate","Valor":"Criptografar"}, {"Name":"Nome"e"Valor":"Criptografar emails de saída confidenciais (sem regra caixa)"}, {"Name":" MessageContainsDataClassifications"… etc.*
 |

## <a name="how-do-i-opt-out"></a>Como eu sair?

Se você gostaria de recusar essa alteração, siga estas etapas:

1. Usando uma conta de trabalho ou da escola que tenha permissões de administrador global na sua organização do Office 365, iniciar uma sessão do Windows PowerShell e se conectar ao Exchange Online. Para obter instruções, consulte [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).
2. Execute o cmdlet Set-IRMConfiguration da seguinte maneira:

   ```
   Set-IRMConfiguration -AutomaticServiceUpdateEnabled $false
   ```

## <a name="how-do-i-disable-or-customize-the-automatic-policy"></a>Como desabilitar ou personalizar a diretiva automática?

Se você não tiver recusar essa alteração e a regra de fluxo de email do Exchange tiver sido criada, você pode [desabilitar ou editar a regra](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) indo para **fluxo de email** > **regras** em que o administrador do Exchange center (EAC) e desabilitar a regra "*criptografar emails de saída confidenciais (sem regra caixa)*".

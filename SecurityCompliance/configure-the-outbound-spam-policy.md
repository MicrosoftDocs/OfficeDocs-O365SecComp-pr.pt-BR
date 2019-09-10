---
title: Configurar notificações de política de spam de saída no Office 365
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 11/10/2016
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: a44764e9-a5d2-4c67-8888-e7fb871c17c7
ms.collection:
- M365-security-compliance
description: Os administradores podem aprender a modificar as configurações de notificação para detecções de spam de saída no Office 365.
ms.openlocfilehash: c48b6cd634417a00040fb5479313782b44f6aa8d
ms.sourcegitcommit: 81b3bff27bc60235a38004c5b0297ac454331b25
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2019
ms.locfileid: "36822511"
---
# <a name="configure-outbound-spam-policy-notifications-in-office-365"></a>Configurar notificações de política de spam de saída no Office 365

A filtragem de spam de saída está sempre habilitada se você utilizar o serviço de envio de email de saída, protegendo assim as organizações que utilizam o serviço e seus destinatários desejados. Semelhante a filtragem de entrada, a filtragem de spam de saída é composta de filtragem de conexão e de conteúdo, porém, as configurações do filtro de saída não são configuráveis. Se uma mensagem de saída é considerada spam, ela é roteada através do pool de entrega de risco mais alto, que reduz a probabilidade do pool de IP de saída normal estar sendo adicionado a uma lista de bloqueio. Se um cliente continua a enviar spam de saída através do serviço, será impedido de enviar mensagens.

Embora você não possa desabilitar ou alterar a filtragem de spam de saída, é possível definir as seguintes configurações de notificação de spam de saída:

- **Enviar cópias de mensagens suspeitas**: essas mensagens são marcadas como spam (independentemente da classificação de SCL) e não são rejeitadas pelo filtro, mas são roteadas através do pool de entrega de risco mais alto. Você pode usar o centro de administração do Exchange (Eat) ou os cmdlets ** \*-HostedOutboundSpamFilterPolicy** no PowerShell do Exchange Online ou do Exchange Online Protection para especificar destinatários de adição para essas mensagens detectadas. Observe que os destinatários são adicionados como destinatários **Cco** (os campos **de** e **para** são o remetente e o destinatário originais).

- **Enviar notificações quando um remetente é bloqueado**: quando uma quantidade significativa de spam é proveniente de um determinado usuário, o usuário é desabilitado de enviar mensagens de email. Os administradores são notificados por padrão, mas você pode usar a [política de alerta](alert-policies.md) **do usuário que está impedido de enviar emails** no centro de conformidade & segurança do Office 365 para configurar destinatários de notificação adicionais.

  Para ver a aparência dessa notificação, confira [exemplo de notificação quando um remetente estiver bloqueado enviando spam de saída](sample-notification-when-a-sender-is-blocked-sending-outbound-spam.md). Para obter informações sobre como habilitar novamente, consulte [removendo um usuário, domínio ou endereço IP de uma lista de bloqueios após o envio de email de spam](http://technet.microsoft.com/library/712cfcc1-31e8-4e51-8561-b64258a8f1e5.aspx).

## <a name="what-do-you-need-to-know-before-you-begin"></a>O que você precisa saber antes de começar?

- Tempo estimado para conclusão: 5 minutos

- Para abrir o Centro de Conformidade e Segurança, confira [Acessar o Centro de Conformidade e Segurança do Office 365](go-to-the-securitycompliance-center.md).

- Para abrir o Eat, confira [centro de administração do Exchange no Exchange Online](https://docs.microsoft.com/Exchange/exchange-admin-center) ou [no centro de administração do Exchange no Exchange Online Protection](exchange-admin-center-in-exchange-online-protection-eop.md).

- Para abrir o PowerShell do Exchange Online, confira [conectar-se ao PowerShell do Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell). Para abrir o PowerShell do Exchange Online Protection, confira [conectar-se ao PowerShell do Exchange Online Protection](https://docs.microsoft.com/powershell/exchange/exchange-eop/exchange-online-protection-powershell).

- Sua conta precisa receber permissões para que você possa executar este procedimento. Para ver de que permissões você precisa, consulte a entrada de função "Gerenciar alertas" em [permissões no centro de conformidade & segurança do Office 365](permissions-in-the-security-and-compliance-center.md).

## <a name="use-the-eac-to-configure-additional-recipients-for-outbound-spam-messages"></a>Use o Eat para configurar destinatários adicionais para mensagens de spam de saída

1. No Eat, vá para **proteção** \> **spam de saída**.

2. Selecione a política denominada **padrão**e clique em **Editar** ![ícone](media/ITPro-EAC-EditIcon.png)de edição.

3. Na página de propriedades que é aberta, verifique se a guia **preferências de spam de saída** está selecionada e, em seguida, defina a seguinte configuração:

   **Envie uma cópia de todas as mensagens de email de saída suspeitas para o endereço ou endereços de email a seguir**: marque a caixa de seleção e insira os endereços de email de um ou mais administradores que devem ser adicionados ao campo **Cco** de mensagens detectadas. Separe vários endereços de email com um ponto e vírgula (;).

   Quando concluir, clique em **Salvar**.

### <a name="use-exchange-online-powershell-or-exchange-online-protection-powershell-to-configure-additional-recipients-for-outbound-spam-messages"></a>Usar o PowerShell do Exchange Online ou do Exchange Online Protection para configurar destinatários adicionais para mensagens de spam de saída

Para habilitar e configurar destinatários adicionais para mensagens de spam de saída, use a seguinte sintaxe:

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity Default -BccSuspiciousOutboundMail $true -BccSuspiciousOutboundAdditionalRecipients <recipients>
```

- Para especificar os destinatários que substituem todos os valores existentes, `emailaddress1,emailaddress2,...emailaddressN`use a sintaxe.

- Para adicionar ou remover seletivamente destinatários sem afetar as outras entradas, use a sintaxe `@{Add="\<emailaddress1\>","\<emailaddress2\>"...; Remove="\<emailaddress1\>","\<emailaddress2\>"...}`.

Este exemplo habilita e configura o chris@contoso.com, o laura@contoso.com e o julia@contoso.com como destinatários Cco para mensagens de spam de saída.

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity Default -BccSuspiciousOutboundMail $true -BccSuspiciousOutboundAdditionalRecipients chris@contoso.com,laura@contoso.com,julia@contoso.com
```

Este exemplo adiciona michelle@contoso.com como um destinatário adicional Cco.

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity Default -BccSuspiciousOutboundAdditionalRecipients @{Add=michelle@contoso.com}
```

Este exemplo remove chris@contoso.com e julia@contoso.com da lista de destinatários Cco.

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity Default -BccSuspiciousOutboundAdditionalRecipients @{Remove='chris@contoso.com','julia@contoso.com'}
```

Para informações detalhadas de sintaxes e de parâmetros, consulte [set-HostedOutboundSpamFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedoutboundspamfilterpolicy).

**Observação**: execute o comando `Get-HostedOutboundSpamFilterPolicy | Format-List` para ver os valores atuais das propriedades *BccSuspiciousOutboundMail* e *BccSuspiciousOutboundAdditionalRecipients* .

## <a name="use-the-security--compliance-center-to-configure-notifications-when-a-sender-is-blocked"></a>Usar o centro de conformidade de & de segurança para configurar notificações quando um remetente for bloqueado

1. No centro de conformidade & segurança, vá para **** \> **políticas de alerta**de alertas.

2. Localize e selecione a política chamada **usuário impedida de enviar emails**.

3. Na saída aberta, clique em **Editar política**.

4. Na página **Editar destinatários** exibida, defina as seguintes configurações:

   - **Enviar notificações por email**: Verifique se **em** está selecionado.

   - **Destinatários de email**: por padrão, o **TenantAdmins** é o único valor aqui. Para adicionar destinatários adicionais, clique em um ponto vazio nesta caixa, comece a digitar o destinatário e selecione o destinatário quando seu nome for resolvido. Para remover destinatários, clique no **X** ao lado de seus nomes.

   - **Limite diário de notificação**: o valor padrão é **sem limite**, mas você pode configurar vários limites de 1 a 200.

   Quando concluir, clique em **Salvar**.

## <a name="for-more-information"></a>Para saber mais

[Pool de entrega de alto risco para mensagens de saída](high-risk-delivery-pool-for-outbound-messages.md)

[Perguntas frequentes sobre proteção antispam](anti-spam-protection-faq.md)

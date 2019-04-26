---
title: Identificar mensagens suspeitas no Outlook.com e no Outlook na Web
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 04/25/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: Para impedir que mensagens de phishing acessem sua caixa de correio, o Outlook.com e o Outlook na Web verificam se o remetente é quem dizem eles e marcam mensagens suspeitas como lixo eletrônico.
ms.openlocfilehash: edba30bb2ac0f9dc6ebc12db957a518de0c1b543
ms.sourcegitcommit: 9907bebc5f225032f681c4952de0b0be2df278ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2019
ms.locfileid: "33345876"
---
# <a name="identify-suspicious-messages-in-outlookcom-and-outlook-on-the-web"></a>Identificar mensagens suspeitas no Outlook.com e no Outlook na Web

Para impedir que mensagens de phishing acessem sua caixa de correio, o Outlook.com e o Outlook na Web verificam se o remetente é quem dizem eles e marcam mensagens suspeitas como lixo eletrônico.

> [!IMPORTANT]
> Quando uma mensagem é marcada como um golpe de phishing, o Outlook.com e o Outlook na Web exibem um aviso na parte superior da página, mas todos os links na mensagem ainda podem ser abertos.

## <a name="how-can-i-identify-a-suspicious-message-in-my-inbox"></a>Como identificar uma mensagem suspeita em minha caixa de entrada?

O Outlook.com e o Outlook na Web mostram indicadores quando o remetente de uma mensagem não pode ser identificado ou sua identidade é diferente da que você vê no endereço do remetente.

### <a name="you-see-a--in-the-sender-image"></a>Você vê um '? ' na imagem do remetente

Quando o Outlook.com e o Outlook na Web não conseguem verificar a identidade do remetente usando técnicas de autenticação de email, eles exibem um '? ' na foto do remetente.

![A mensagem não passou na verificação](media/message-did-not-pass-verification.jpg)

Nem todas as mensagens que não são autenticadas são mal-intencionadas. No enTanto, você deve ter cuidado para interagir com mensagens que não são autenticadas se você não reconhece o remetente. Ou, se você reconhece um remetente que normalmente não tem um '? ' na imagem do remetente, mas, repentinamente, você começa a vê-lo, que pode ser um sinal de que o remetente está sendo falsificado.

### <a name="the-senders-address-is-different-than-what-appears-in-the-from-address"></a>O endereço do remetente é diferente do que aparece no endereço do

Frequentemente, o endereço de email que você vê em uma mensagem é diferente daquele que você vê no endereço do remetente. Às vezes, os golpistas tentam enganar você pensando que o remetente é alguém que não é quem eles realmente estão.

Quando o Outlook.com e o Outlook na Web detectam uma diferença entre o endereço real do remetente e o endereço no endereço de, eles mostram o remetente real usando a marca via, que será sublinhada.

![texto alternativo de remetente não verificado](media/unverified-sender-feature1.png)

Neste exemplo, o domínio `suspicious.com` de envio é autenticado, mas o remetente colocou `unknown@contoso.com` no endereço de.

Nem todas as mensagens com uma marca de via é suspeitas. No enTanto, se você não reconhece uma mensagem com uma marca via, você deve ter cuidado para interagir com ela.

No Outlook.com e no novo Outlook na Web, você pode passar o cursor sobre o nome ou endereço de um remetente na lista de mensagens para ver seus endereços de email, sem a necessidade de abrir a mensagem.

![Introdução ao OneDrive](media/get-started-with-onedrive-message.png)

Como saber se você está usando o novo Outlook na Web? ConFira os seguintes exemplos:

![Outlook vs Office 365](media/outlook-vs-outlook365.png)

## <a name="frequently-asked-questions"></a>Perguntas frequentes

### <a name="what-criteria-does-outlookcom-and-outlook-on-the-web-use-to-add-the--and-the-via-properties"></a>Que critérios o Outlook.com e o Outlook na Web usam para adicionar as propriedades '? ' e ' via '?

Para o '? ' na imagem do remetente: Outlook.com requer que a mensagem passe o SPF ou a autenticação do DKIM. Para obter mais detalhes, consulte [set up SPF in Office 365 para ajudar a impedir](set-up-spf-in-office-365-to-help-prevent-spoofing.md) a falsificação e [uso do DKIM para validar emails de saída enviados do seu domínio personalizado no Office 365](use-dkim-to-validate-outbound-email.md).

Para o via Tag: se o domínio no endereço de for diferente do domínio na assinatura do DKIM ou do email SMTP de, Outlook.com exibe o domínio em um desses dois campos (preferência à assinatura DKIM).

### <a name="can-i-override-these-properties-with-ip-allows-exchange-transport-rule-allows-or-safe-senders"></a>Posso substituir essas propriedades por IP permite, a regra de transporte do Exchange permite ou remetentes confiáveis?

Você não pode substituir essas propriedades.

### <a name="how-do-i-remove-these-properties"></a>Como faço para remover essas propriedades?

Para o '? ' na imagem do remetente: como um remetente, você deve autenticar sua mensagem com o SPF ou o DKIM.

Para o via Tag: como um remetente, você deve garantir que o domínio na assinatura DKIM ou o email SMTP de seja o mesmo que ou seja um subdomínio de, o domínio no endereço de.

### <a name="does-outlookcom-and-outlook-on-the-web-show-this-for-every-message-that-doesnt-pass-authentication"></a>O Outlook.com e o Outlook na Web mostram isso para cada mensagem que não aprova a autenticação?

Não necessariamente. O Outlook.com e o Outlook na Web podem ter outras propriedades dentro da mensagem para autenticar o remetente.

## <a name="related-topics"></a>Tópicos relacionados

[Ajudar a proteger sua conta de email do Outlook.com](https://support.office.com/article/a4f20fc5-4307-4ece-8231-6d4d4bd8a9ba)

[Lidar com abuso, phishing ou falsificação no Outlook.com](https://support.office.com/article/0d882ea5-eedc-4bed-aebc-079ffa1105a3)

[Filtrar lixo eletrônico e spam no Outlook na Web](https://support.office.com/article/db786e79-54e2-40cc-904f-d89d57b7f41d)

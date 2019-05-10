---
title: Remetente não verificado
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
ms.openlocfilehash: 5d4315afb33964e7c466384366b7315287cf6298
ms.sourcegitcommit: d24f50347c671cf5d2d8afec2f80d37d18af8b5d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2019
ms.locfileid: "33867835"
---
# <a name="unverified-sender"></a>Remetente não verificado

Para impedir que mensagens de phishing acessem sua caixa de correio, o Outlook.com e o Outlook na Web verificam se o remetente é quem dizem eles e marcam mensagens suspeitas como lixo eletrônico.

> [!IMPORTANT]
> Quando uma mensagem é marcada como um golpe de phishing, o Outlook.com e o Outlook na Web exibem um aviso na parte superior da página, mas todos os links na mensagem ainda podem ser abertos.

## <a name="how-can-i-identify-a-suspicious-message-in-my-inbox"></a>Como identificar uma mensagem suspeita em minha caixa de entrada?

O Outlook.com e o Outlook na Web mostram indicadores quando o remetente de uma mensagem não pode ser identificado ou sua identidade é diferente da que você vê no endereço do remetente.

## <a name="how-to-manage-which-messages-receive-the-unverified-sender-treatment"></a>Como gerenciar quais mensagens recebem o tratamento de remetentes não verificados 

Se você for um cliente do Office 365, poderá gerenciar esse recurso através do centro de conformidade do & de segurança. 

- No centro de conformidade do & de segurança do Office 365, os administradores de locatários podem ativar ou desativar o recurso por meio da proteção contra falsificação na política de anti-phishing. Além disso, ele pode ser gerenciado por meio do cmdlet "Set-AntiPhishPolicy". Para obter mais detalhes, consulte proteção contra phishing no Office 365 e Set-AntiPhishPolicy.

    ![Edição de remetentes não autenticados na interface gráfica.](media/unverified-sender-article-editing-unauthenticated-senders.jpg)

- Se um administrador identificou um falso positivo e um remetente não deve receber o tratamento de remetente não verificado, eles podem executar uma das ações a seguir para adicionar o remetente à lista de permissões de falsificação de inteligência de falsificação:
        
    - Adicionar o par de domínios por meio da compreensão de inteligência de falsificação. Para obter mais detalhes, consulte Walkthrough: spoof Intelligence percepção
                
    - Adicione o par de domínios através do cmdlet PhishFilterPolicy. Para obter mais detalhes, consulte Set-PhishFilterPolicy e anti-falsification Protection in Office 365

Além disso, não aplicamos o tratamento de remetente não verificado se ele foi entregue à caixa de entrada por meio de uma lista de permissões de administração, incluindo regras de transporte de email (ETRs), lista de domínios seguros (política antispam), lista de remetentes seguros ou um usuário tiver definido esse usuário como um "remetente seguro" em seu postal.

### <a name="you-see-a--in-the-sender-image"></a>Você vê um '? ' na imagem do remetente

Quando o Outlook.com e o Outlook na Web não conseguem verificar a identidade do remetente usando técnicas de autenticação de email, eles exibem um '? ' na foto do remetente. 

![A mensagem não passou na verificação](media/message-did-not-pass-verification.jpg)

Nem todas as mensagens que não são autenticadas são mal-intencionadas. No entanto, você deve ter cuidado para interagir com mensagens que não são autenticadas se você não reconhece o remetente. Ou, se você reconhece um remetente que normalmente não tem um '? ' na imagem do remetente, mas, repentinamente, você começa a vê-lo, que pode ser um sinal de que o remetente está sendo falsificado.

### <a name="the-senders-address-is-different-than-what-appears-in-the-from-address"></a>O endereço do remetente é diferente do que aparece no endereço do

Frequentemente, o endereço de email que você vê em uma mensagem é diferente daquele que você vê no endereço do remetente. Às vezes, os golpistas tentam enganar você pensando que o remetente é alguém que não é quem eles realmente estão.

Quando o Outlook.com e o Outlook na Web detectam uma diferença entre o endereço real do remetente e o endereço no endereço de, eles mostram o remetente real usando a marca via, que será sublinhada.

![texto alternativo de remetente não verificado](media/unverified-sender-feature1.png)

Neste exemplo, o domínio `suspicious.com` de envio é autenticado, mas o remetente colocou `unknown@contoso.com` no endereço de.

Nem todas as mensagens com uma marca de via é suspeitas. No entanto, se você não reconhece uma mensagem com uma marca via, você deve ter cuidado para interagir com ela.

No Outlook.com e no novo Outlook na Web, você pode passar o cursor sobre o nome ou endereço de um remetente na lista de mensagens para ver seus endereços de email, sem a necessidade de abrir a mensagem.

![Introdução ao OneDrive](media/get-started-with-onedrive-message.png)

Como saber se você está usando o novo Outlook na Web? Confira os seguintes exemplos:

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

---
title: Como o Office 365 valida o endereço de para evitar phishing
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/11/2017
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- OWC150
- MET150
ms.assetid: eef8408b-54d3-4d7d-9cf7-ad2af10b2e0e
description: 'Para ajudar a impedir phishing, Office 365 e Outlook.com agora requerem conformidade RFC para do: endereços.'
ms.openlocfilehash: 562e08aa54cb6544beccb6f0e8760735f67b834b
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523495"
---
# <a name="how-office-365-validates-the-from-address-to-prevent-phishing"></a>Como o Office 365 valida o endereço de para evitar phishing

O Office 365 e contas de email do Outlook.com recebem um número cada vez maior de ataques de phishing. Uma técnica phishers usam é para enviar mensagens que têm valores para From: endereço que não são compatíveis com a [RFC 5322](https://tools.ietf.org/html/rfc5322). From: o endereço também é chamado de endereço de 5322.From. Para evitar esse tipo de phishing, Office 365 e Outlook.com exigem que as mensagens recebidas pelo serviço para incluir um compatível com RFC do: endereço, conforme descrito neste artigo.
  
> [!NOTE]
> As informações neste artigo exige que você tenha uma noção básica do formato geral dos endereços de email. Para obter mais informações, consulte [RFC 5322](https://tools.ietf.org/html/rfc5322) (particularmente seções 3.2.3, 3.4 e 3.4.1), [RFC 5321](https://tools.ietf.org/html/rfc5321), bem como [3696 RFC](https://tools.ietf.org/html/rfc3696). Este artigo fala sobre imposição de política para o endereço de 5322.From. Este artigo não é sobre o endereço de 5321.MailFrom. 
  
Infelizmente, ainda há alguns servidores herdados de email na Internet que continuam a enviar mensagens que têm uma falta de email "legítimo" ou mal formados do: endereço. Se você receber o email regularmente de organizações que usam esses sistemas legados, incentive dessas organizações para atualizar seus servidores de email para cumprir os padrões de segurança moderno.
  
Microsoft iniciará a aplicação do reforço das diretivas descrito neste artigo em 9 de novembro de 2017.
  
## <a name="how-office-365-enforces-the-use-of-a-valid-from-address-to-prevent-phishing-attacks"></a>Como o Office 365 impõe o uso de um valor válido de: endereço a prevenir ataques de phishing

O Office 365 está fazendo alterações à maneira como ele impõe o uso de From: endereço em mensagens recebidas para melhor protegê-lo contra ataques de phishing. Neste artigo:
  
- [Todas as mensagens devem incluir um valor válido de: endereço](how-office-365-validates-the-from-address.md#MustIncludeFromAddress)
    
- [Todas as mensagens devem incluir um valor válido de: endereço](how-office-365-validates-the-from-address.md#MustIncludeFromAddress)
    
- [Formato de From: se você não incluir um nome de exibição de endereços](how-office-365-validates-the-from-address.md#FormatNoDisplayName)
    
- [Formato de From: se você incluir um nome de exibição de endereços](how-office-365-validates-the-from-address.md#FormatDisplayName)
    
- [Exemplos adicionais de válidas e inválidas de: endereços](how-office-365-validates-the-from-address.md#Examples)
    
- [Suprimir as respostas automáticas para seu domínio personalizado sem quebrar From: política](how-office-365-validates-the-from-address.md#SuppressAutoReply)
    
- [Substituindo o Office 365 do: política de imposição de endereços](how-office-365-validates-the-from-address.md#Override)
    
- [Outras maneiras de prevenir e proteger contra aos cybercrimes no Office 365](how-office-365-validates-the-from-address.md#OtherProtection)
    
Enviar em nome de outro usuário não é afetado por essa alteração, para obter mais detalhes, leia o blog de Terry Zink "[que estamos falando quando nos referimos 'remetente' de um email?](https://blogs.msdn.microsoft.com/tzink/2017/06/22/what-do-we-mean-when-we-refer-to-the-sender-of-an-email/)".
  
### <a name="all-messages-must-include-a-valid-from-address"></a>Todas as mensagens devem incluir um valor válido de: endereço
<a name="MustIncludeFromAddress"> </a>

Algumas mensagens automatizadas não incluem um From: endereço quando eles forem enviados. No passado, quando o Office 365 ou Outlook.com recebeu uma mensagem sem um From: o serviço de endereço, adicionado o seguinte formato padrão do: endereço à mensagem para torná-lo o resultado final:
  
```
From: <>
```

Iniciando 9 de novembro de 2017, Office 365 estarão disponíveis alterações aos seus servidores de email e data centers que imporá uma nova regra onde mensagens sem um From: endereço não será aceito pelo Office 365 ou Outlook.com. Em vez disso, todas as mensagens recebidas pelo Office 365 já deverá conter um valor válido de: endereço. Caso contrário, a mensagem será enviada para o lixo eletrônico ou itens excluídos pastas no Outlook.com e no Office 365. 
  
### <a name="syntax-overview-valid-format-for-the-from-address-for-office-365"></a>Visão geral de sintaxe: formato válido para From: endereço para o Office 365
<a name="SyntaxOverviewFromAddress"> </a>

O formato para o valor do campo From: endereço é definido detalhadamente nas várias RFCs. Há muitas variações endereçamento e o que podem ser considerado válidos ou inválidos. Para manter simples, a Microsoft recomenda que você use as definições e o seguinte formato:
  
```
From: "displayname " <emailaddress >
```

Onde:
  
- (Opcional)  *DisplayName* é uma frase que descreve o proprietário do endereço de email. Por exemplo, isso pode ser um nome mais intuitivo para descrever o remetente do nome da caixa de correio. Usando um nome de exibição é opcional. No entanto, se você optar por usar um nome para exibição, a Microsoft recomenda que você sempre coloque-o entre aspas conforme mostrado. 
    
- (Necessário)  *EmailAddress* é formada pelo: 
    
  ```
  local-part @domain
  ```

    Onde:
    
  - (Necessário)  *parte de local* é uma cadeia de caracteres que identifica a caixa de correio associada ao endereço. Isso é exclusivo dentro do domínio. Muitas vezes, username ou o GUID do proprietário da caixa de correio é usado como o valor para a parte de local. 
    
  - (Necessário)  *domínio* é o nome de domínio totalmente qualificado (FQDN) do servidor de email que hospeda a caixa de correio identificada por parte local do endereço de email. 
    
### <a name="format-of-the-from-address-if-you-dont-include-a-display-name"></a>Formato de From: se você não incluir um nome de exibição de endereços
<a name="FormatNoDisplayName"> </a>

Uma formatada corretamente do: endereço que não inclua um nome de exibição inclui apenas um único endereço de email com ou sem colchetes angulares. A Microsoft recomenda que você não separe os colchetes angulares com espaços. Além disso, não inclua qualquer coisa após o endereço de email.
  
Os exemplos a seguir são válidos:
  
```
From: sender@contoso.com
```

```
From: <sender@contoso.com>
```

O exemplo a seguir é válido, mas não é recomendado porque ele contém espaços entre os colchetes angulares e o endereço de email:
  
```
From: < sender@contoso.com >
```

O exemplo a seguir é inválido, pois ele contém texto após o endereço de email:
  
```
From: "Office 365" <sender@contoso.com> (Sent by a process)
```

### <a name="format-of-the-from-address-if-you-include-a-display-name"></a>Formato de From: se você incluir um nome de exibição de endereços
<a name="FormatDisplayName"> </a>

Para partir: endereços que incluem um valor para o nome para exibição, as seguintes regras se aplicam:
  
- Se o endereço do remetente inclui um nome de exibição e o nome para exibição inclui uma vírgula, o nome para exibição deve estar entre aspas. Por exemplo:
    
    O exemplo a seguir é válido:
    
  ```
  From: "Sender, Example" <sender.example@contoso.com>
  ```

    O exemplo a seguir não é válido:
    
  ```
  From: Sender, Example <sender.example@contoso.com>
  ```

    Não é válido de acordo com a RFC 5322 não colocar o nome de exibição aspas se esse nome de exibição inclui uma vírgula.
    
    Como prática recomendada, colocar aspas em torno do nome de exibição, independentemente de se há ou não é uma vírgula entre o nome para exibição.
    
- Se o endereço do remetente inclui um nome para exibição, o endereço de email deve ser colocado entre colchetes angulares.
    
    Como prática recomendada, a Microsoft recomenda que você inserir um espaço entre o nome para exibição e o endereço de email.
    
### <a name="additional-examples-of-valid-and-invalid-from-addresses"></a>Exemplos adicionais de válidas e inválidas de: endereços
<a name="Examples"> </a>

- Válido:
    
  ```
  From: "Office 365" <sender@contoso.com>
  ```

- Inválido. O endereço de email não está incluído nos colchetes angulares:
    
  ```
  From: Office 365 sender@contoso.com
  ```

- Válido, mas não recomendado. O nome para exibição não está entre aspas. Como prática recomendada, sempre coloque o nome de exibição entre aspas:
    
  ```
  From: Office 365 <sender@contoso.com>
  ```

- Inválido. Tudo está entre aspas, não apenas o nome de exibição:
    
  ```
  From: "Office 365 <sender@contoso.com>"
  ```

- Inválido. Não há nenhum ângulo entre colchetes o endereço de email:
    
  ```
  From: "Office 365 <sender@contoso.com>" sender@contoso.com
  ```

- Inválido. Não há nenhum espaço entre o nome para exibição e colchetes esquerdo:
    
  ```
  From: Office 365<sender@contoso.com>
  ```

- Inválido. Não há nenhum espaço entre o quotation mark fechamento em torno do nome de exibição e o colchete esquerdo de ângulo.
    
  ```
  From: "Office 365"<sender@contoso.com>
  ```

### <a name="suppress-auto-replies-to-your-custom-domain-without-breaking-the-from-policy"></a>Suprimir as respostas automáticas para seu domínio personalizado sem quebrar From: política
<a name="SuppressAutoReply"> </a>

Com o novo com base em: aplicação de políticas, você não poderá mais usar do: \< \> para suprimir as respostas automáticas. Em vez disso, você precisará configurar um registro MX nulo para seu domínio personalizado.
  
O registro do mail exchanger (MX) é um registro de recurso no DNS que identifica o servidor de email que recebe o email para seu domínio. As respostas automáticas (e todas as respostas) são suprimidas naturalmente porque não há nenhum endereço publicado para o qual o servidor de resposta pode enviar mensagens.
  
Quando você configurar um nulo registro MX para seu domínio personalizado:
  
- Escolha um domínio do qual deseja enviar mensagens que não aceita (receber) emails. Por exemplo, se o seu domínio primário for contoso.com, você pode escolher noreply.contoso.com.
    
- Configure o registro MX nulo para seu domínio. Um registro de MX nulo consiste em um único ponto, por exemplo:
    
  ```
  noreply.contoso.com IN MX .
  ```

Para obter mais informações sobre como publicar um MX nulo, consulte [RFC 7505](https://tools.ietf.org/html/rfc7505).
  
### <a name="overriding-the-office-365-from-address-enforcement-policy"></a>Substituindo o Office 365 do: política de imposição de endereços
<a name="Override"> </a>

Uma vez concluída roll a nova política, você somente poderá ignorar essa diretiva para emails de entrada, que você recebe do Office 365 usando um dos seguintes métodos: 
  
- Listas de permissões de IP
    
- Regras de fluxo de correio Exchange Online
    
A Microsoft recomenda contra substituir a imposição de From: política. Substituir essa diretiva pode aumentar o risco de sua organização de exposição a spam, phishing e aos outros cybercrimes.
  
Você não pode substituir essa diretiva para mensagens de saída, que você pode enviar no Office 365. Além disso, o Outlook.com não permitirá substituições de qualquer tipo, mesmo por meio de suporte. 
  
### <a name="other-ways-to-prevent-and-protect-against-cybercrimes-in-office-365"></a>Outras maneiras de prevenir e proteger contra aos cybercrimes no Office 365
<a name="OtherProtection"> </a>

Para obter mais informações sobre como você pode fortalecer a sua organização em relação aos cybercrimes como o phishing, spam, violações de dados e outras ameaças, consulte [práticas recomendadas de segurança para o Office 365](https://support.office.com/article/9295e396-e53d-49b9-ae9b-0b5828cdedc3).
  
## <a name="related-topics"></a>Tópicos relacionados

[Mnsagens backscatter e EOP](https://technet.microsoft.com/en-us/library/dn499795%28v=exchg.150%29.aspx)
  


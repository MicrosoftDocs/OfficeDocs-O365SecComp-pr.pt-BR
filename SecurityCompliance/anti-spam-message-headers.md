---
title: Cabeçalhos de mensagem antispam
ms.author: krowley
author: kccross
manager: laurawi
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 2e3fcfc5-5604-4b88-ac0a-c5c45c03f1db
description: Quando o Proteção do Exchange Online examina emails de entrada, insere o cabeçalho **X-Forefront-Antispam-Report** em cada mensagem.
ms.openlocfilehash: 39cac8e1406bd4f7505ae4bc626b8c7e78f88101
ms.sourcegitcommit: 75b985b2574f4be70cf352498ea300b3d99dd338
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2018
ms.locfileid: "26255886"
---
# <a name="anti-spam-message-headers"></a>Cabeçalhos de mensagem antispam

Quando o Proteção do Exchange Online examina emails de entrada, insere o cabeçalho **X-Forefront-Antispam-Report** em cada mensagem. Os campos nesse cabeçalho podem ajudar a fornecer aos administradores informações sobre a mensagem e sobre como ela foi processada. Os campos no cabeçalho **X-Microsoft-Antispam** fornecem mais informações sobre email em massa e phishing. Além esses dois cabeçalhos, o Proteção do Exchange Online também insere resultados de autenticação de email para cada mensagem que ele processa no cabeçalho **Authentication-results**.
  
> [!TIP]
> Para obter informações sobre como exibir um cabeçalho da mensagem de email em vários clientes de email, consulte [Analisador de Cabeçalho de Mensagens](https://go.microsoft.com/fwlink/p/?LinkId=306583). Você pode copiar e colar o conteúdo do cabeçalho da mensagem na ferramenta [Analisador de Cabeçalhos de Mensagens](https://testconnectivity.microsoft.com/?tabid=mha). Quando você selecionar uma mensagem na quarentena no centro de administração do Exchange, o link **Visualizar cabeçalho da mensagem** também deixará que você facilmente copie e cole o texto do cabeçalho da mensagem na ferramenta. Quando estiver na ferramenta Analisador de Cabeçalhos de Mensagens, clique em **Analisar cabeçalhos** para recuperar informações sobre o cabeçalho.
  
## <a name="x-forefront-antispam-report-message-header-fields"></a>Campos de cabeçalho da mensagem X-Forefront-Antispam-Report
<a name="sectionSection0"> </a>

Depois de acessar as informações do cabeçalho da mensagem, procure **X-Forefront-Antispam-Report** e por estes campos. Outros campos neste cabeçalho são usados exclusivamente pela equipe anti-spam da Microsoft para fins de diagnóstico.

|**Campo do cabeçalho**|**Descrição**|
|:-----|:-----|
|CIP: [endereço IP]|Endereço IP da conexão. Talvez você queira especificar esse endereço IP ao criar uma lista de IPS permitidos ou uma lista de bloqueios de IP do filtro de conexão. Para obter mais informações, consulte [Configure a política de filtro de conexão](configure-the-connection-filter-policy.md).|
|CTRY|O país/região a partir do qual a mensagem se conectou ao serviço. Isso é determinado pelo endereço IP de conexão, que pode não ser o mesmo que o endereço IP de envio original.|
|LANG|O idioma no qual a mensagem foi escrita, conforme especificado pelo código de país/região (por exemplo, ru_RU para russo).|
|SCL|O valor de Nível de Confiança de Spam (SCL) da mensagem. Para obter mais informações sobre como interpretar esses valores, consulte [Níveis de confiança de spam](spam-confidence-levels.md).  |
|PCL|O valor do Nível de confiança de phishing (PCL) da mensagem. Consulte o [PCL](anti-spam-message-headers.md#PCL) para saber mais sobre os valores de PCL.  |
|SRV:BULK|A mensagem foi identificada como uma mensagem de email em massa. Se a **opção de filtragem de spam avançada Bloquear todas as mensagens de email em massa estiver habilitada**, ela será marcada como spam. Se não estiver habilitada, ela será apenas marcada como spam se o restante das regras de filtragem determinar que a mensagem é spam.  |
|SFV:SFE|A filtragem foi ignorada e foi permitida a passagem da mensagem porque ela foi enviada de um endereço em uma lista de remetentes seguros de um indivíduo.|
|SFV:BLK|A filtragem foi ignorada e foi bloqueada a passagem da mensagem porque ela foi enviada de um endereço em uma lista de remetentes bloqueados de um indivíduo.  <br/> **Dica**: para obter mais informações sobre como os usuários finais podem criar listas de remetentes bloqueados e seguros, consulte [Bloquear ou permitir (configurações de lixo eletrônico)](https://go.microsoft.com/fwlink/p/?LinkId=294862) (Outlook na web) e [Visão geral do filtro de lixo eletrônico](https://go.microsoft.com/fwlink/p/?LinkId=270065) (Outlook).|
|IPV:CAL|A mensagem foi permitida pelos filtros de spam porque o endereço IP estava especificado em uma Lista de Permissões de IP do filtro de conexão.|
|IPV:NLI|O endereço IP não está listado em qualquer lista de reputação de IP.|
|SFV:SPM|O filtro de conteúdo marcou a mensagem como spam.|
|SFV:SKS|A mensagem foi marcada como spam antes de ser processada pelo filtro de conteúdo. Isso inclui mensagens que atenderam a uma regra Transporte para marcá-la automaticamente como spam e ignorar toda filtragem adicional.|
|SFV:SKA|A mensagem ignorou a filtragem e foi entregue à caixa de entrada porque correspondeu a uma lista de permissões na política de filtro de spam, como a lista de **permissões do remetente**.|
|SFV:SKB|A mensagem foi marcada como spam porque correspondeu a uma lista de bloqueios na política de filtro de spam, como a lista de **bloqueio de remetente**.|
|SFV:SKN|A mensagem foi marcada como não sendo spam antes de ser processada pelo filtro de conteúdo. Isso inclui mensagens que atenderam a uma regra de transporte para marcá-la automaticamente como não sendo spam e ignorar qualquer filtragem adicional.|
|SFV:SKI|De forma semelhante a SFV:SKN, a filtragem de mensagem é ignorada por outro motivo, como sendo email intraorganizacional em um locatário.|
|SFV:SKQ|A mensagem foi liberada da quarentena e enviada para os destinatários pretendidos.|
|SFV:NSPM|A mensagem foi marcada como não spam e enviada aos destinatários pretendidos.|
|H: [helostring]|A cadeia de caracteres HELO ou EHLO do servidor de email que está se conectando.|
|PTR: [ReverseDNS]|O registro PTR, ou registro do ponteiro, do endereço IP de envio, também conhecido como o endereço de DNS reverso.|
|SFTY|A mensagem foi identificada como phishing e também será marcada com um dos seguintes valores: <br/>• 9.1: valor padrão. A mensagem contém uma URL de phishing, pode conter outros conteúdos de phishing ou talvez foram marcada como phishing por outro filtro de email, como uma versão local do Exchange Server antes de retransmitir a mensagem para o Office 365. <br/>• 9.11: mensagem falhou antifalsificação verificações onde o domínio de envio no campo From: cabeçalho é o mesmo, ou se alinha com ou é parte da mesma organização que o domínio de recebimento. <br/>• 9.21: mensagem falhou verificações antifalsificação e o domínio de envio no campo From: cabeçalho não autenticar. Usado em combinação com CompAuth (Consulte autenticação resultados). <br/>• 9.22: igual à 9.21, exceto que o usuário tem um remetente seguro que foi substituído. <br/>• 9.23: igual à 9.22, exceto que a organização tem um remetente permitido ou domínio que foi substituído. <br/>• 9,24: igual à 9.23, exceto que o usuário possui uma regra de fluxo de email do Exchange que foi substituída.|
|X-CustomSpam: [ASFOption]|A mensagem corresponde a uma opção de filtragem de spam avançada. Por exemplo, **X-CustomSpam: links para sites remotos da imagem** indica que a opção de **links de imagem para sites remotos** ASF correspondida. Para descobrir qual texto de cabeçalho X é adicionado para cada opção de ASF específica, consulte [Opções de filtragem de spam avançada](advanced-spam-filtering-asf-options.md).|
   
## <a name="x-microsoft-antispam-message-header-fields"></a>Campos de cabeçalho da mensagem X-Microsoft-Antispam
<a name="sectionSection1"> </a>

A tabela a seguir descreve campos úteis no cabeçalho da mensagem **X-Microsoft-Antispam**. Outros campos neste cabeçalho são usados exclusivamente pela equipe anti-spam da Microsoft para fins de diagnóstico.
  
|**Campo do cabeçalho**|**Descrição**|
|:-----|:-----|
|BCL|O Nível de Reclamação em Massa (BCL) da mensagem. Para saber mais, veja [Valores de nível compatível com dados em massa](bulk-complaint-level-values.md).  |
|PCL|O Phishing confiança nível (PCL) da mensagem, que indica se ele é uma mensagem de phishing. Esse status pode ser retornado como um dos seguintes valores numéricos:<br/>• **0-3**: conteúdo da mensagem não está provavelmente phishing. <br/>• **4 a 8**: provavelmente phishing é conteúdo da mensagem. <br/>• **-9990**: (Exchange Online Protection somente) provavelmente phishing é conteúdo da mensagem.  <br/>  Os valores são usados para determinar qual ação seu cliente de email leva em mensagens. Por exemplo, o Outlook usa o carimbo PCL para bloquear o conteúdo de mensagens suspeitas. Para obter mais informações sobre phishing e como o Outlook processa mensagens de phishing, consulte [Ativar ou desativar links em mensagens de email](https://support.office.com/article/2D79B907-93B6-4774-82E6-1F0385CF20F8).|
   
## <a name="authentication-results-message-header"></a>Cabeçalho da mensagem Authentication-results
<a name="sectionSection2"> </a>

Os resultados das verificações em relação a SPF, DKIM e DMARC são gravados ou marcados pelo Office 365 no cabeçalho da mensagem **Authentication-results** quando os servidores de email recebem uma mensagem de email.
  
### <a name="check-stamp-syntax-and-examples"></a>verificar sintaxe e exemplos de carimbo
<a name="referenceSPFstamp"> </a>

Os exemplos de sintaxe a seguir mostram uma parte do texto "carimbo" que o Office 365 aplica ao cabeçalho da mensagem para cada email que passa por uma verificação de autenticação de email quando é recebida por nossos servidores de email. O carimbo é adicionado ao cabeçalho **Authentication-Results**.
  
 **Sintaxe: Carimbo de verificação do SPF**
  
Para SPF, a seguinte sintaxe é aplicada.
  
```
spf=<pass (IP address)|fail (IP address)|softfail (reason)|neutral|none|temperror|permerror> smtp.mailfrom=<domain>
```

 **Exemplos: Carimbo de verificação do SPF**
  
```
spf=pass (sender IP is 192.168.0.1) smtp.mailfrom=contoso.com
spf=fail (sender IP is 127.0.0.1) smtp.mailfrom=contoso.com
```

 **Sintaxe: Carimbo de verificação do DKIM**
  
Para DKIM, a seguinte sintaxe é aplicada.
  
```
dkim=<pass|fail (reason)|none> header.d=<domain>
```

 **Exemplos: Carimbo de verificação do DKIM**
  
```
dkim=pass (signature was verified) header.d=contoso.com
dkim=fail (body hash did not verify) header.d=contoso.com
```

 **Sintaxe: Carimbo de verificação do DMARC**
  
Para DMARC, a seguinte sintaxe é aplicada.
  
```
dmarc=<pass|fail|bestguesspass|none> action=<permerror|temperror|oreject|pct.quarantine|pct.reject> header.from=<domain>
```

 **Exemplos: Carimbo de verificação do DMARC**
  
```
dmarc=pass action=none header.from=contoso.com
dmarc=bestguesspass action=none header.from=contoso.com
dmarc=fail action=none header.from=contoso.com
dmarc=fail action=oreject header.from=contoso.com
```

### <a name="authentication-results-message-header-fields-used-by-office-365-email-authentication"></a>Campos do cabeçalho da mensagem Authentication-results usados pela autenticação de email do Office 365
<a name="referenceSPFstamp"> </a>

Esta tabela descreve os campos e os valores possíveis para cada verificação de autenticação de email.
  
|**Campo do cabeçalho**|**Descrição**|
|:-----|:-----|
|spf|Descreve os resultados da verificação do SPF para a mensagem. Os valores possíveis incluem:  <br/>• **passar (endereço IP)**: indica a verificação SPF da mensagem passada e inclui o endereço IP do remetente. O cliente está autorizado a enviar ou retransmitir email em nome de domínio do remetente.<br/>• **falhar (endereço IP)**: indica a verificação SPF da mensagem falhou e inclui o endereço IP do remetente. Às vezes, isso é chamado _de falha grave_.<br/>• **softfail (razão)**: indica que o registro SPF tiver designado o host como não sendo permissão para enviar, mas está em transição. <br/>• **neutro**: indica que o registro SPF tenha declarado explicitamente que ele não está declarando se o endereço IP está autorizado. <br/>• **none**: indica que o domínio não possui um registro SPF ou o registro SPF não é avaliada como um resultado. <br/>• **temperror**: indica que ocorreu um erro que pode ser temporário de natureza temporária, por exemplo, um erro de DNS. Tentar novamente mais tarde, talvez seja bem-sucedida sem qualquer ação do administrador.<br/>• **permerror**: indica que ocorreu um erro permanente. Isso acontece quando, por exemplo, o domínio tem um registro de SPF formatado incorretamente.|
|SMTP.MailFrom|Contém o domínio da fonte a partir da qual a mensagem foi enviada. Os erros sobre esta mensagem de email serão enviados para o postmaster ou entidade responsável pelo domínio. Isso algumas vezes é chamado de endereço 5321.MailFrom ou endereço reverso no envelope da mensagem.|
|dkim|Descreve os resultados da verificação do DKIM para a mensagem. Os valores possíveis incluem:  <br/>• **passar**: indica a verificação de verificação para a mensagem passada. <br/>• **falhar (razão)**: indica a verificação de verificação para a mensagem de falha e por quê. Por exemplo, se a mensagem não foi assinada ou a assinatura não foi verificada.<br/>• **none**: indica que a mensagem não foi assinada. Isso pode ou não pode indicar que o domínio tem um registro de verificação ou o registro de verificação não é avaliada como um resultado, só que esta mensagem não foi assinada.|
|Header.d|Domínio identificado na assinatura DKIM, se houver. Este é o domínio consultado para a chave pública.|
|dmarc|Descreve os resultados da verificação do DMARC para a mensagem. Os valores possíveis incluem:  <br/>• **passar**: indica a verificação DMARC para a mensagem passada. <br/>• **falhar**: indica a verificação DMARC para a mensagem falhou. <br/>• **bestguesspass**: indica que existir nenhum registro TXT DMARC para o domínio, mas se um tivesse existido, a verificação DMARC da mensagem seria ter passado. Isso ocorre porque o domínio no endereço 5321.MailFrom corresponde ao domínio no endereço 5322.From.<br/>• **none**: indica que nenhum registro TXT DKIM existe para o domínio de envio no DNS.|
|action|Indica a ação executada pelo filtro de spam com base nos resultados da verificação do DMARC. Por exemplo:  <br/>• **permerror**: Ocorreu um erro permanente durante avaliação DMARC, como encontrando um formado incorretamente DMARC TXT registrar no DNS. Tentar reenviar esta mensagem não é provável que terminam com um resultado diferente. Em vez disso, talvez seja necessário entrar em contato com o proprietário do domínio para resolver o problema.<br/>• **temperror**: Ocorreu um erro temporário durante avaliação DMARC. Você poderá solicitar que o remetente reenviar a mensagem posteriormente para processar o email corretamente.<br/>• **oreject** ou **o.reject**: significa substituir rejeitar. Neste usa caso o Office 365 essa ação quando ele recebe uma mensagem que está falhando o DMARC de seleção de um domínio cujo registro TXT DMARC possui uma política de p = rejeitar. Em vez de exclusão ou rejeição da mensagem, o Office 365 marca a mensagem como spam. Para obter mais informações sobre por que o Office 365 é configurado dessa forma, consulte [identificadores de como o Office 365 que falha DMARC de email de entrada](use-dmarc-to-validate-email.md#inbounddmarcfail).<br/>• **pct.quarantine**: indica que uma porcentagem menor que 100% das mensagens que não passar DMARC serão entregues mesmo assim. Isso significa que a mensagem falhou DMARC e a política foi definida para a quarentena, mas o campo pct não foi definido como 100% e aleatoriamente determinar o sistema não aplicar a ação DMARC, conforme a política do domínio especificado.<br/>• **pct.reject**: indica que uma porcentagem menor que 100% das mensagens que não passar DMARC serão entregues mesmo assim. Isso significa que a mensagem falhou DMARC e a política foi definida para rejeitar, mas o campo pct não foi definido como 100% e o sistema aleatoriamente determinado que não se aplicam a ação DMARC, conforme a política do domínio especificado.|
|Header.From|O domínio do endereço de no cabeçalho da mensagem de email. Às vezes, isso é chamado de endereço de _5322.From_ .|
|compauth|Resultado de composição de autenticação. Usado pelo Office 365 para combinar vários tipos de autenticação como SPF, DKIM, DMARC ou qualquer outra parte da mensagem para determinar se ou não a mensagem é autenticada. Usa From: domínio como a base de avaliação.|
|motivo|O motivo pelo qual a autenticação de composição passou ou falhou. O valor para o motivo pelo qual é composto pelos três dígitos:<br/>• **000**: a mensagem falhou explicitamente autenticação. Por exemplo, a mensagem recebida de uma falha DMARC com uma ação de quarentena ou rejeitar.<br/>• **001**: a mensagem falhou implicitamente autenticação e o domínio de envio não publicou políticas de autenticação. Por exemplo, uma política DMARC de p = none.<br/>• **1xx**: A mensagem passou autenticação. Os segundo dois dígitos são códigos internos usados pelo Office 365.<br/>• **2xx**: A autenticação do passado para reversível. Os segundo dois dígitos são códigos internos usados pelo Office 365.<br/>• **3xx**: A mensagem não foi verificada para autenticação de composição. <br/>• **4xx**: A mensagem desviada autenticação composta. Os segundo dois dígitos são códigos internos usados pelo Office 365.|

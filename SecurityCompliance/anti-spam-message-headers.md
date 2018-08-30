---
title: Cabeçalhos de mensagem antispam
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 2/9/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 2e3fcfc5-5604-4b88-ac0a-c5c45c03f1db
description: Quando o Proteção do Exchange Online examina emails de entrada, insere o cabeçalho **X-Forefront-Antispam-Report** em cada mensagem.
ms.openlocfilehash: 192a1d3e3331256819ddd68fbe0aa0c1fa16c9a7
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23003140"
---
# <a name="anti-spam-message-headers"></a>Cabeçalhos de mensagem antispam

Quando o Proteção do Exchange Online examina emails de entrada, insere o cabeçalho **X-Forefront-Antispam-Report** em cada mensagem. Os campos nesse cabeçalho podem ajudar a fornecer aos administradores informações sobre a mensagem e sobre como ela foi processada. Os campos no cabeçalho **X-Microsoft-Antispam** fornecem mais informações sobre email em massa e phishing. Além esses dois cabeçalhos, o Proteção do Exchange Online também insere resultados de autenticação de email para cada mensagem que ele processa no cabeçalho **Authentication-results**. 
  
> [!TIP]
> Para obter informações sobre como exibir um cabeçalho da mensagem de email em vários clientes de email, consulte [Analisador de Cabeçalho de Mensagens](https://go.microsoft.com/fwlink/p/?LinkId=306583). Você pode copiar e colar o conteúdo do cabeçalho da mensagem na ferramenta [Analisador de Cabeçalhos de Mensagens](https://testconnectivity.microsoft.com/?tabid=mha). Quando você selecionar uma mensagem na quarentena no centro de administração do Exchange, o link **Visualizar cabeçalho da mensagem** também deixará que você facilmente copie e cole o texto do cabeçalho da mensagem na ferramenta. Quando estiver na ferramenta Analisador de Cabeçalhos de Mensagens, clique em **Analisar cabeçalhos** para recuperar informações sobre o cabeçalho. 
  
## <a name="x-forefront-antispam-report-message-header-fields"></a>Campos de cabeçalho da mensagem X-Forefront-Antispam-Report
<a name="sectionSection0"> </a>

Depois de acessar as informações do cabeçalho da mensagem, procure **X-Forefront-Antispam-Report** e por estes campos. Outros campos neste cabeçalho são usados exclusivamente pela equipe anti-spam da Microsoft para fins de diagnóstico. 
  
|||
|:-----|:-----|
|**Campo do cabeçalho** <br/> |**Descrição** <br/> |
|CIP: [endereço IP]  <br/> |Endereço IP da conexão. Talvez você queira especificar esse endereço IP ao criar uma lista de IPS permitidos ou uma lista de bloqueios de IP do filtro de conexão. Para obter mais informações, consulte [Configure a política de filtro de conexão](configure-the-connection-filter-policy.md).<br/> |
|CTRY  <br/> |O país/região a partir do qual a mensagem se conectou ao serviço. Isso é determinado pelo endereço IP de conexão, que pode não ser o mesmo que o endereço IP de envio original.  <br/> |
|LANG  <br/> |O idioma no qual a mensagem foi escrita, conforme especificado pelo código de país/região (por exemplo, ru_RU para russo).  <br/> |
|SCL  <br/> |O valor de Nível de Confiança de Spam (SCL) da mensagem. Para obter mais informações sobre como interpretar esses valores, consulte [Níveis de confiança de spam](spam-confidence-levels.md).  <br/> |
|PCL  <br/> |O valor do Nível de confiança de phishing (PCL) da mensagem. Consulte o [PCL](anti-spam-message-headers.md#PCL) para saber mais sobre os valores de PCL.  <br/> |
|SRV:BULK  <br/> |A mensagem foi identificada como uma mensagem de email em massa. Se a **opção de filtragem de spam avançada Bloquear todas as mensagens de email em massa estiver habilitada**, ela será marcada como spam. Se não estiver habilitada, ela será apenas marcada como spam se o restante das regras de filtragem determinar que a mensagem é spam.  <br/> |
|SFV:SFE  <br/> |A filtragem foi ignorada e foi permitida a passagem da mensagem porque ela foi enviada de um endereço em uma lista de remetentes seguros de um indivíduo.  <br/> |
|SFV:BLK  <br/> |A filtragem foi ignorada e foi bloqueada a passagem da mensagem porque ela foi enviada de um endereço em uma lista de remetentes bloqueados de um indivíduo.  <br/> **Dica:** Para obter mais informações sobre como os usuários finais podem criar listas de remetentes seguros e bloqueados, confira [Bloquear ou permitir (configurações de lixo eletrônico)](https://go.microsoft.com/fwlink/p/?LinkId=294862) (OWA) e [Visão geral do Filtro de Lixo Eletrônico](https://go.microsoft.com/fwlink/p/?LinkId=270065) (Outlook).  <br/> |
|IPV:CAL  <br/> |A mensagem foi permitida pelos filtros de spam porque o endereço IP estava especificado em uma Lista de Permissões de IP do filtro de conexão.  <br/> |
|IPV:NLI  <br/> |O endereço IP não está listado em qualquer lista de reputação de IP.  <br/> |
|SFV:SPM  <br/> |O filtro de conteúdo marcou a mensagem como spam.  <br/> |
|SFV:SKS  <br/> |A mensagem foi marcada como spam antes de ser processada pelo filtro de conteúdo. Isso inclui mensagens que atenderam a uma regra Transporte para marcá-la automaticamente como spam e ignorar toda filtragem adicional.  <br/> |
|SFV:SKA  <br/> |A mensagem ignorou a filtragem e foi entregue à caixa de entrada porque correspondeu a uma lista de permissões na política de filtro de spam, como a lista de **permissões do remetente**.  <br/> |
|SFV:SKB  <br/> |A mensagem foi marcada como spam porque correspondeu a uma lista de bloqueios na política de filtro de spam, como a lista de **bloqueio de remetente**.  <br/> |
|SFV:SKN  <br/> |A mensagem foi marcada como não sendo spam antes de ser processada pelo filtro de conteúdo. Isso inclui mensagens que atenderam a uma regra de transporte para marcá-la automaticamente como não sendo spam e ignorar qualquer filtragem adicional.  <br/> |
|SFV:SKI  <br/> |De forma semelhante a SFV:SKN, a filtragem de mensagem é ignorada por outro motivo, como sendo email intraorganizacional em um locatário.  <br/> |
|SFV:SKQ  <br/> |A mensagem foi liberada da quarentena e enviada para os destinatários pretendidos.  <br/> |
|SFV:NSPM  <br/> |A mensagem foi marcada como não spam e enviada aos destinatários pretendidos.  <br/> |
|H: [helostring]  <br/> |A cadeia de caracteres HELO ou EHLO do servidor de email que está se conectando.  <br/> |
|PTR: [ReverseDNS]  <br/> |O registro PTR, ou registro do ponteiro, do endereço IP de envio, também conhecido como o endereço de DNS reverso.  <br/> |
|SFTY  <br/> | A mensagem foi identificada como phishing e também será marcada com um dos seguintes valores:  <br/>  9.1 - o valor padrão. A mensagem contém uma URL de phishing, pode conter outros conteúdos de phishing ou talvez foram marcada como phishing por outro filtro de email, como uma versão local do Exchange Server antes de retransmitir a mensagem para o Office 365.  <br/>  9.11 - mensagem falhou antifalsificação verificações onde o domínio de envio no campo From: cabeçalho é o mesmo, ou se alinha com ou é parte da mesma organização que o domínio de recebimento.  <br/>  9.21 - mensagem falhou verificações antifalsificação e o domínio de envio no campo From: cabeçalho não autenticar. Usado em combinação com CompAuth (Consulte autenticação resultados).  <br/>  9.22 - igual à 9.21, exceto que o usuário tem um remetente seguro que foi substituído.  <br/>  9.23 - igual à 9.22, exceto que a organização tem um remetente permitido ou domínio que foi substituído.  <br/>  9,24 - iguais 9.23, exceto que o usuário tem um fluxo de mensagens do Exchange da regra que foi substituída.  <br/> |
|X-CustomSpam: [ASFOption]  <br/> |A mensagem corresponde a uma opção de filtragem de spam avançada. Por exemplo, **X-CustomSpam: links para sites remotos da imagem** indica que a opção de **links de imagem para sites remotos** ASF correspondida. Para descobrir qual texto de cabeçalho X é adicionado para cada opção de ASF específica, consulte [Opções de filtragem de spam avançada](advanced-spam-filtering-asf-options.md).<br/> |
   
## <a name="x-microsoft-antispam-message-header-fields"></a>Campos de cabeçalho da mensagem X-Microsoft-Antispam
<a name="sectionSection1"> </a>

A tabela a seguir descreve campos úteis no cabeçalho da mensagem **X-Microsoft-Antispam**. Outros campos neste cabeçalho são usados exclusivamente pela equipe anti-spam da Microsoft para fins de diagnóstico. 
  
|||
|:-----|:-----|
|**Campo do cabeçalho** <br/> |**Descrição** <br/> |
|BCL  <br/> |O Nível de Reclamação em Massa (BCL) da mensagem. Para saber mais, veja [Valores de nível compatível com dados em massa](bulk-complaint-level-values.md).  <br/> |
|PCL  <br/> | O Nível de Confiança de Phishing (PCL) da mensagem que indica se é uma mensagem de phishing.  <br/>  Esse status pode ser retornado como um dos seguintes valores numéricos:  <br/> **0-3** O conteúdo da mensagem provavelmente não é phishing.  <br/> **4-8** O conteúdo da mensagem provavelmente é phishing.  <br/> **-9990** (somente da Proteção do Exchange Online) O conteúdo da mensagem é provavelmente phishing.  <br/>  Os valores são usados para determinar que ação o seu cliente de email toma em relação às mensagens. Por exemplo, o Microsoft Office Outlook usa o carimbo PCL para bloquear o conteúdo de mensagens suspeitas. Para ter mais informações sobre phishing e como o Outlook processa as mensagens de phishing, consulte [Ativar ou desativar links em mensagens de email](https://support.office.com/article/2D79B907-93B6-4774-82E6-1F0385CF20F8).  <br/> |
   
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
|spf  <br/> | Descreve os resultados da verificação do SPF para a mensagem. Os valores possíveis incluem:  <br/> **pass (endereço IP)** indica a verificação do SPF para a mensagem passou e inclui um endereço IP do remetente. O cliente está autorizado a enviar ou retransmitir emails em nome do domínio do remetente.  <br/> **fail (endereço IP)** indica a verificação do SPF para a mensagem reprovada e inclui um endereço IP do remetente. Isso também é conhecido como falha grave.  <br/> **softfail (motivo)** indica que o registro SPF designou o host como não tendo permissão para enviar mas está em transição.  <br/> **neutral** indica que o registro SPF explicitamente declarou que não definiu se o endereço IP está autorizado.  <br/> **none** indica que o domínio não tem um registro SPF ou o registro SPF não é avaliado como um resultado.  <br/> **temperror** indica que ocorreu um erro que pode ser temporário, por exemplo, um erro de DNS. Tentar novamente mais tarde poderá ter sucesso sem precisar de nenhuma ação do administrador.  <br/> **permerror** indica que um erro permanente ocorreu. Isso acontece quando, por exemplo, o domínio tem um registro SPF mal formatado.  <br/> |
|SMTP.MailFrom  <br/> |Contém o domínio da fonte a partir da qual a mensagem foi enviada. Os erros sobre esta mensagem de email serão enviados para o postmaster ou entidade responsável pelo domínio. Isso algumas vezes é chamado de endereço 5321.MailFrom ou endereço reverso no envelope da mensagem.  <br/> |
|dkim  <br/> | Descreve os resultados da verificação do DKIM para a mensagem. Os valores possíveis incluem:  <br/> **pass** indica que a verificação DKIM para a mensagem passou.  <br/> **fail (motivo)** indica que a verificação do DKIM para a mensagem falhou e o porquê. Por exemplo, se a mensagem não foi assinada ou se a assinatura não foi verificada.  <br/> **none** indica que a mensagem não foi assinada. Isso pode ou não indicar que o domínio tem um registro DKIM ou o registro DKIM não foi avaliado como um resultado, apenas que essa mensagem não foi assinada.  <br/> |
|Header.d  <br/> |Domínio identificado na assinatura DKIM, se houver. Este é o domínio consultado para a chave pública.  <br/> |
|dmarc  <br/> | Descreve os resultados da verificação do DMARC para a mensagem. Os valores possíveis incluem:  <br/> **pass** indica que a verificação do DMARC para a mensagem passou.  <br/> **fail** indica que houve falha na verificação do DMARC para a mensagem.  <br/> **bestguesspass** indica que não existe nenhum registro TXT do DMARC para o domínio, mas, se houvesse, a verificação do DMARC para a mensagem teria passado. Isso ocorre porque o domínio no endereço 5321.MailFrom corresponde ao domínio no endereço 5322.From.  <br/> **none** indica que não há nenhum registro TXT do DKIM para o domínio de envio no DNS.  <br/> |
|action  <br/> | Indica a ação executada pelo filtro de spam com base nos resultados da verificação do DMARC. Por exemplo:  <br/> **permerror** Ocorreu um erro permanente durante a avaliação do DMARC, como encontrar um registro TXT do DMARC formado incorretamente no DNS. Tentar reenviar esta mensagem provavelmente não terminará com um resultado diferente. Em vez disso, talvez seja necessário entrar em contato com o proprietário do domínio para resolver o problema.  <br/> **temperror** Ocorreu um erro temporário durante a avaliação do DMARC. Você poderá solicitar ao remetente que reenvie a mensagem mais tarde para processar o email corretamente.  <br/> **oreject** ou **o.reject** Significa substituir a rejeição. Neste caso, o Office 365 usa essa ação quando recebe uma mensagem informando que houve falha na verificação do DMARC de um domínio cujo registro TXT do DMARC tem uma política p=reject. Em vez de excluir ou rejeitar a mensagem, o Office 365 marca a mensagem como spam. Para saber mais sobre por que o Office 365 está configurado dessa forma, confira [Como o Office 365 lida com emails de entrada que não passam na verificação do DMARC](use-dmarc-to-validate-email.md#inbounddmarcfail).  <br/> **pct.quarantine** Indica que uma porcentagem menor que 100% das mensagens que não passam na verificação do DMARC será enviada de qualquer forma. Isso significa que houve falha de DMARC na mensagem e a política foi definida como quarentena, mas o campo pct não foi definido como 100% e o sistema aleatoriamente determinou não aplicar a ação do DMARC, conforme a política especificada do domínio.  <br/> **pct.reject** Indica que uma porcentagem menor que 100% das mensagens que não passam na verificação do DMARC será enviada de qualquer forma. Isso significa que houve falha de DMARC na mensagem e a política foi definida como rejeitar, mas o campo pct não foi definido como 100% e o sistema aleatoriamente determinou não aplicar a ação do DMARC, conforme a política especificada do domínio.  <br/> |
|Header.From  <br/> |O domínio de endereço From no cabeçalho da mensagem de email. Isso também é conhecido como endereço 5322.From.  <br/> |
|compauth  <br/> |Resultado de composição de autenticação. Usado pelo Office 365 para combinar vários tipos de autenticação como SPF, DKIM, DMARC ou qualquer outra parte da mensagem para determinar se ou não a mensagem é autenticada. Usa From: domínio como a base de avaliação.  <br/> |
|motivo  <br/> | O motivo pelo qual a autenticação de composição passou ou falhou. O valor para o motivo pelo qual é composto pelos três dígitos:  <br/>  000 - a mensagem falhou explicitamente autenticação. Por exemplo, a mensagem recebida de uma falha DMARC com uma ação de quarentena ou rejeitar.  <br/>  001 - a mensagem falhou implicitamente autenticação e o domínio de envio não publicou políticas de autenticação. Por exemplo, uma política DMARC de p = none.  <br/>  1xx - a mensagem passou autenticação. Os segundo dois dígitos são códigos internos usados pelo Office 365.  <br/>  2xx - a autenticação do passado para reversível. Os segundo dois dígitos são códigos internos usados pelo Office 365.  <br/>  3xx - a mensagem não foi verificado para autenticação de composição.  <br/>  4xx - a mensagem desviada autenticação composta. Os segundo dois dígitos são códigos internos usados pelo Office 365.  <br/> |
  
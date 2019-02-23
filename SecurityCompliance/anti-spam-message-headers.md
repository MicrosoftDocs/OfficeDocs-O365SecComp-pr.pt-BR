---
Título: "cabeçalhos de mensagens antispam" MS. Author: Krowley Author: kccross Manager: laurawi MS. Audience: profissionais MS. Topic: artigo MS. Service: O365-seccomp MS. Custom: TN2DMC localization_priority: normal Search. appverid:
- MET150 MS. AssetID: 2e3fcfc5-5604-4b88-ac0a-c5c45c03f1db MS. Collection:
    - M365-segurança-Descrição da conformidade: "quando o Exchange Online Protection verifica uma mensagem de email de entrada, ele insere o cabeçalho **X-Forefront-antispam-Report** em cada mensagem."
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
|CIP: [endereço IP]|O endereço IP de conexão. Você pode querer especificar esse endereço IP ao criar uma lista de IPs permitidos ou uma lista de IPs bloqueados no filtro de conexão. Para obter mais informações, consulte [Configurar a política de filtro de conexão](configure-the-connection-filter-policy.md).|
|CTRY|O país/região a partir do qual a mensagem se conectou ao serviço. Isso é determinado pelo endereço IP de conexão, que pode não ser o mesmo que o endereço IP de envio original.|
|LANG|O idioma no qual a mensagem foi escrita, conforme especificado pelo código de país/região (por exemplo, ru_RU para russo).|
|SCL|O valor de Nível de Confiança de Spam (SCL) da mensagem. Para obter mais informações sobre como interpretar esses valores, consulte [Níveis de confiança de spam](spam-confidence-levels.md).  |
|PCL|O valor do Nível de confiança de phishing (PCL) da mensagem. |
|SRV:BULK|A mensagem foi identificada como uma mensagem de email em massa. Se a **opção de filtragem de spam avançada Bloquear todas as mensagens de email em massa estiver habilitada**, ela será marcada como spam. Se não estiver habilitada, ela será apenas marcada como spam se o restante das regras de filtragem determinar que a mensagem é spam.  |
|SFV:SFE|A filtragem foi ignorada e foi permitida a passagem da mensagem porque ela foi enviada de um endereço em uma lista de remetentes seguros de um indivíduo.|
|SFV:BLK|A filtragem foi ignorada e foi bloqueada a passagem da mensagem porque ela foi enviada de um endereço em uma lista de remetentes bloqueados de um indivíduo.  <br/> **Dica**: para obter mais informações sobre como os usuários finais podem criar listas de remetentes seguras e bloqueados, consulte [bloquear ou permitir (configurações de lixo eletrônico)](https://go.microsoft.com/fwlink/p/?LinkId=294862) (Outlook na Web) e [visão geral do filtro de lixo eletrônico](https://go.microsoft.com/fwlink/p/?LinkId=270065) (Outlook).|
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
|SFTY|A mensagem foi identificada como phishing e também será marcada com um dos seguintes valores: <br/>• 9,1: valor padrão. A mensagem contém uma URL de phishing, pode conter outros conteúdos de phishing ou pode ter sido marcada como phishing por outro filtro de email, como uma versão local do Exchange Server antes de retransmitir a mensagem para o Office 365. <br/>• 9,11: falha nas verificações antifalsificação de mensagens em que o domínio de envio no cabeçalho from: é o mesmo que ou é parte da mesma organização que o domínio de recebimento. Isso indica que uma dica de segurança de falsificação de organização interna será adicionada à mensagem. <br/>• 9,19: falha nas verificações de personificação de domínio de mensagens em que o domínio de envio está tentando representar um domínio de Propriedade do receptor ou um domínio personalizado protegido pela política anti-phishing. Isso indica que uma dica de segurança de representação será adicionada à mensagem, se habilitada por meio da política Phishig. <br/>• 9,20: as verificações de representação de usuário com falha de mensagem em que o usuário de envio está tentando representar um usuário dentro da organização de receptores ou um usuário personalizado protegido pela política anti-phishing. Isso indica que uma dica de segurança de representação será adicionada à mensagem, se habilitada por meio da política Phishig. <br/>• 9,21: a mensagem falhou nas verificações anti-falsificação e o domínio de envio no cabeçalho from: não autentica e é de um domínio externo. Usado em combinação com CompAuth (consulte Authentication-Results). <br/>• 9,22: igual a 9,21, exceto pelo fato de que o usuário tem um remetente seguro que foi substituído. <br/>• 9,23: igual a 9,22, exceto que a organização tem um remetente ou domínio permitido que foi substituído. <br/>• 9,24: igual a 9,23, exceto pelo fato de que o usuário tem uma regra de fluxo de email do Exchange que foi substituída.|
|X-CustomSpam: [ASFOption]|A mensagem corresponde a uma opção de filtragem de spam avançada. Por exemplo, **X-CustomSpam: links de imagem para sites remotos** denota que a opção **links de imagem para sites remotos** ASF foi correspondida. Para descobrir qual texto de cabeçalho X é adicionado para cada opção ASF específica, confira [Opções avançadas de filtragem de spam](advanced-spam-filtering-asf-options.md).|
   
## <a name="x-microsoft-antispam-message-header-fields"></a>Campos de cabeçalho da mensagem X-Microsoft-Antispam
<a name="sectionSection1"> </a>

A tabela a seguir descreve campos úteis no cabeçalho da mensagem **X-Microsoft-Antispam**. Outros campos neste cabeçalho são usados exclusivamente pela equipe anti-spam da Microsoft para fins de diagnóstico.
  
|**Campo do cabeçalho**|**Descrição**|
|:-----|:-----|
|BCL|O Nível de Reclamação em Massa (BCL) da mensagem. Para saber mais, veja [Valores de nível compatível com dados em massa](bulk-complaint-level-values.md).  |
|PCL|O nível de confiança de phishing (PCL) da mensagem, que indica se é uma mensagem de phishing. Esse status pode ser retornado como um dos seguintes valores numéricos:<br/>• **0-3**: o conteúdo da mensagem provavelmente não é phishing. <br/>• **4-8**: o conteúdo da mensagem provavelmente será phishing. <br/>• **-9990**: (somente proteção do Exchange Online) o conteúdo da mensagem provavelmente é phishing.  <br/>  Os valores são usados para determinar a ação que seu cliente de email executa em mensagens. Por exemplo, o Outlook usa o carimbo PCL para bloquear o conteúdo de mensagens suspeitas. Para obter mais informações sobre phishing e como o Outlook processa mensagens de phishing, consulte [Ativar ou desativar links em mensagens de email](https://support.office.com/article/2D79B907-93B6-4774-82E6-1F0385CF20F8).|
   
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
|spf|Descreve os resultados da verificação do SPF para a mensagem. Os valores possíveis incluem:  <br/>• **Pass (endereço IP)**: indica que a verificação do SPF para a mensagem passou e inclui o endereço IP do remetente. O cliente é autorizado a enviar ou retransmitir emails em nome do domínio do remetente.<br/>• **falha (endereço IP)**: indica que a verificação de SPF da mensagem falhou e inclui o endereço IP do remetente. Isso às vezes é chamado de _falha grave_.<br/>• **SoftFail (motivo)**: indica que o registro SPF designou o host como não sendo permitido para envio, mas está em transição. <br/>• **neutro**: indica que o registro SPF declarou explicitamente que não está afirmando se o endereço IP está autorizado. <br/>• **nenhum**: indica que o domínio não tem um registro SPF ou o registro SPF não é avaliado como um resultado. <br/>• **TempError**: indica que ocorreu um erro que pode ser temporário por natureza, por exemplo, um erro de DNS. Tentar novamente mais tarde pode ter êxito sem qualquer ação do administrador.<br/>• **PermError**: indica que um erro permanente ocorreu. Isso acontece quando, por exemplo, o domínio tem um registro SPF mal formatado.|
|SMTP. Mailfrom|Contém o domínio da fonte a partir da qual a mensagem foi enviada. Os erros sobre esta mensagem de email serão enviados para o postmaster ou entidade responsável pelo domínio. Isso algumas vezes é chamado de endereço 5321.MailFrom ou endereço reverso no envelope da mensagem.|
|dkim|Descreve os resultados da verificação do DKIM para a mensagem. Os valores possíveis incluem:  <br/>• **passagem**: indica a verificação do DKIM para a mensagem passada. <br/>• **falha (razão)**: indica que a verificação DKIM da mensagem falhou e por quê. Por exemplo, se a mensagem não foi assinada ou a assinatura não tiver sido verificada.<br/>• **nenhum**: indica que a mensagem não foi assinada. Isso pode ou não indicar que o domínio tem um registro DKIM ou o registro DKIM não é avaliado como um resultado, apenas que essa mensagem não foi assinada.|
|header. d|Domínio identificado na assinatura DKIM, se houver. Este é o domínio consultado para a chave pública.|
|dmarc|Descreve os resultados da verificação do DMARC para a mensagem. Os valores possíveis incluem:  <br/>• **passagem**: indica a verificação do DMARC para a mensagem passada. <br/>• **falha**: indica que a verificação de DMARC da mensagem falhou. <br/>• **bestguesspass**: indica que nenhum registro txt do DMARC para o domínio existe, mas se houver algum, a verificação DMARC da mensagem teria passado. Isso ocorre porque o domínio no endereço 5321. MailFrom corresponde ao domínio no endereço 5322. from.<br/>• **None**: indica que não existe registro txt do DKIM para o domínio de envio no DNS.|
|action|Indica a ação executada pelo filtro de spam com base nos resultados da verificação do DMARC. Por exemplo:  <br/>• **PermError**: ocorreu um erro permanente durante a avaliação do DMARC, como encontrar um registro txt incorretamente formado DMARC no DNS. A tentativa de reenviar esta mensagem provavelmente não terminará com um resultado diferente. Em vez disso, talvez seja necessário entrar em contato com o proprietário do domínio para resolver o problema.<br/>• **TempError**: ocorreu um erro temporário durante A avaliação do DMARC. Talvez você possa solicitar que o remetente reenvie a mensagem mais tarde para processar o email corretamente.<br/>• **oreject** ou **o. Reject**: significa rejeição de substituição. Neste caso, o Office 365 usa esta ação quando recebe uma mensagem que falha na verificação DMARC de um domínio cujo registro TXT DMARC tem uma política de p = rejeitar. Em vez de excluir ou rejeitar a mensagem, o Office 365 marca a mensagem como spam. Para saber mais sobre por que o Office 365 é configurado dessa forma, confira [como o office 365 trata emails de entrada que falhaRAM DMARC](use-dmarc-to-validate-email.md#inbounddmarcfail).<br/>• **PCT. Quarantine**: indica que uma porcentagem menor que 100% das mensagens que não passam DMARC será entregue mesmo assim. Isso significa que a mensagem falhou DMARC e a política foi definida como Quarantine, mas o campo PCT não foi definido como 100% e o sistema aleatoriamente determinou não aplicar a ação DMARC, de acordo com a política do domínio especificado.<br/>• **PCT. Reject**: indica que uma porcentagem menor que 100% das mensagens que não passam DMARC será entregue mesmo assim. Isso significa que a mensagem falhou DMARC e a política foi definida como rejeitar, mas o campo PCT não foi definido como 100% e o sistema aleatoriamente determinou não aplicar a ação DMARC, de acordo com a política do domínio especificado.|
|header. from|O domínio do endereço de no cabeçalho da mensagem de email. Isso às vezes é chamado de endereço _5322. from_ .|
|compauth|Resultado da autenticação composta. Usado pelo Office 365 para combinar vários tipos de autenticação como SPF, DKIM, DMARC ou qualquer outra parte da mensagem para determinar se a mensagem é ou não autenticada. Usa o domínio de: como base de avaliação.|
|motivos|O motivo pelo qual a autenticação composta passou ou falhou. O valor do motivo é composto de três dígitos:<br/>• **000**: a mensagem falhou explicitamente na autenticação. Por exemplo, a mensagem recebeu uma falha de DMARC com uma ação de quarentena ou rejeitar.<br/>• **001**: a mensagem falhou implicitamente na autenticação e o domínio de envio não publicou as políticas de autenticação. Por exemplo, uma política de DMARC de p = None.<br/>• **1xx**: a mensagem passou pela autenticação. Os dois dígitos de segundo são códigos internos usados pelo Office 365.<br/>• **2xx**: a mensagem de autenticação aprovada. Os dois dígitos de segundo são códigos internos usados pelo Office 365.<br/>• **3xx**: a mensagem não foi verificada para autenticação de composição. <br/>• **4xx**: a mensagem ignorou a autenticação composta. Os dois dígitos de segundo são códigos internos usados pelo Office 365.|

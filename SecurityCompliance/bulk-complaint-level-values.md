---
Título: "valores de nível de queixa em massa" MS. Author: Krowley Author: kccross Manager: laurawi MS. Date: 3/5/2015 MS. Audience: profissionais MS. tópico: artigo MS. Service: O365-seccomp MS. Custom: TN2DMC localization_priority: normal Search. appverid:
- MET150 MS. AssetID: a5b03b3c-37dd-429E-8e9b-2c1b25031794 MS. Collection:
    - M365 – descrição da conformidade com segurança: "os remetentes em massa variam em suas tternss de envio, criação de conteúdo e aquisição de lista. Alguns são bons remetentes em massa que enviam mensagens desejadas com conteúdo relevante para seus assinantes. Essas mensagens geram poucas reclamações de destinatários. Outros remetentes em massa enviam mensagens não solicitadas que parecem muito parecidas com spam e geram muitas queixas de destinatários. Para distinguir esses tipos de remetentes em massa, as mensagens de email em massa recebem uma classificação de BCL (nível de reclamação em massa). A classificação de BCL varia de 1 a 9, dependendo da probabilidade de o remetente de mensagens em massa gerar queixas. Um remetente que tenha uma classificação da BCL 9 provavelmente gerará muitas queixas de destinatários, enquanto uma classificação da BCL 3 será improvável de gerar muitas queixas. A Microsoft usa fontes internas e de terceiros para identificar emails em massa e determinar a BCL apropriada. Essa classificação é exposta no cabeçalho X-Microsoft-antispam de cada mensagem. Para obter mais informações sobre esse cabeçalho de mensagem, consulte anti-spam Message Headers.
---

# <a name="bulk-complaint-level-values"></a>Valores de nível de reclamação em massa

Os emails em massa variam em seus padrões de envio, criação de conteúdo e práticas de aquisição de lista. Alguns são bons remetentes em massa que enviam mensagens desejadas com conteúdo relevante para seus assinantes. Essas mensagens geram poucas reclamações de destinatários. Outros remetentes em massa enviam mensagens não solicitadas que parecem muito parecidas com spam e geram muitas queixas de destinatários. Para distinguir esses tipos de remetentes em massa, as mensagens de email em massa recebem uma classificação de BCL (nível de reclamação em massa). A classificação de BCL varia de 1 a 9, dependendo da probabilidade de o remetente de mensagens em massa gerar queixas. Um remetente que tenha uma classificação da BCL 9 provavelmente gerará muitas queixas de destinatários, enquanto uma classificação da BCL 3 será improvável de gerar muitas queixas. A Microsoft usa fontes internas e de terceiros para identificar emails em massa e determinar a BCL apropriada. Essa classificação é exposta no cabeçalho **X-Microsoft-antispam** de cada mensagem. Para obter mais informações sobre esse cabeçalho de mensagem, consulte [anti-spam Message Headers](anti-spam-message-headers.md). 
  
Você pode usar valores de BCL para definir o nível desejado de filtragem em massa que sua organização requer, seguindo as etapas em [Configure Your spam filter Policies](configure-your-spam-filter-policies.md).
  
Mais valores de BCL estão sendo adicionados e serão incluídos aqui no futuro. A tabela a seguir lista e descreve os valores de BCL que estão em uso no momento.
  
|||
|:-----|:-----|
|**Valor de BCL** <br/> |**Descrição** <br/> |
|,0  <br/> |A mensagem não é de um remetente em massa.  <br/> |
|1, 2, 3  <br/> |A mensagem é de um remetente em massa que gera algumas reclamações.  <br/> |
|4, 5, 6, 7  <br/> |A mensagem é de um remetente em massa que gera um número misto de reclamações.  <br/> |
|8, 9  <br/> |A mensagem é de um remetente em massa que gera um grande número de reclamações  <br/> |
   


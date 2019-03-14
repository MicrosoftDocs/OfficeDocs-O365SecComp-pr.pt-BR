---
title: Proteção contra falsificação no Office 365
ms.author: tracyp
author: MSFTtracyp
manager: laurawi
ms.date: 3/6/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.assetid: d24bb387-c65d-486e-93e7-06a4f1a436c0
ms.collection:
- M365-security-compliance
- Strat_O365_IP
description: Este artigo descreve como o Office 365 diminui contra ataques de phishing que usam domínios de remetente forjados, ou seja, domínios falsificados. Ele realiza isso analisando as mensagens e bloqueando as que podem ser autenticadas, nem usando métodos de autenticação de email padrão, nem outras técnicas de reputação de remetente. Essa alteração foi implementada para reduzir o número de ataques de phishing aos quais as organizações do Office 365 são expostas.
ms.openlocfilehash: 377bc75e7538dacab1180045ddfdeb1a2ac32a65
ms.sourcegitcommit: 5eb664b6ecef94aef4018a75684ee4ae66c486bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/08/2019
ms.locfileid: "30492870"
---
# <a name="anti-spoofing-protection-in-office-365"></a>Proteção contra falsificação no Office 365

Este artigo descreve como o Office 365 diminui contra ataques de phishing que usam domínios de remetente forjados, ou seja, domínios falsificados. Ele realiza isso analisando as mensagens e bloqueando as que não podem ser autenticadas usando métodos de autenticação de email padrão, nem outras técnicas de reputação do remetente. Essa alteração foi implementada para reduzir o número de ataques de phishing aos quais as organizações do Office 365 são expostas.
  
Este artigo também descreve por que essa alteração está sendo feita, como os clientes podem se preparar para essa alteração, como exibir mensagens que serão afetadas, como relatar mensagens, como reduzir os falsos positivos, bem como como os remetentes à Microsoft devem se preparar para esse trocar.
  
A tecnologia antifalsificação da Microsoft foi inicialmente implantada em suas organizações que possuíam uma assinatura do Office 365 Enterprise E5 ou compraram o complemento do Office 365 Advanced Threat Protection (ATP) para sua assinatura. A partir de outubro de 2018, estendemos a proteção para organizações que também têm o Exchange Online Protection (EOP). Além disso, devido à forma como todos os nossos filtros aprendem uns dos outros, os usuários do Outlook.com também podem ser afetados.
  
## <a name="how-spoofing-is-used-in-phishing-attacks"></a>Como a falsificação é usada em ataques de phishing

Quando se trata de proteger seus usuários, a Microsoft leva seriamente a ameaça de phishing. Uma das técnicas comumente usadas por spammers e phishers é a falsificação, que é quando o remetente é forjado, e uma mensagem parece originar de alguém ou de outro lugar que não seja a fonte real. Essa técnica é freqüentemente usada em campanhas de phishing projetadas para obter credenciais de usuário. A tecnologia antifalsificação da Microsoft examina especificamente a falsificação do cabeçalho ' de: ', que é aquele que aparece em um cliente de email como o Outlook. Quando a Microsoft tem alta confiança de que o cabeçalho from: é falsificado, ele identifica a mensagem como uma falsificação.
  
As mensagens de falsificação têm duas implicações negativas para usuários de vida real:
  
### <a name="1-spoofed-messages-deceive-users"></a>1. mensagens falsificadas usuários enganar
  
Primeiro, uma mensagem falsificada pode induzir o usuário a clicar em um link e fornecer suas credenciais, baixar malware ou responder a uma mensagem com conteúdo confidencial (o que é conhecido como comprometimento de email comercial). Por exemplo, a seguir está uma mensagem de phishing com um remetente falso de msoutlook94@service.outlook.com:
  
![Mensagem de phishing representando service.outlook.com](media/1a441f21-8ef7-41c7-90c0-847272dc5350.jpg)
  
O acima não veio realmente do service.outlook.com, mas, em vez disso, foi falsificado pelo phishing para que ele pareça ter sido. Ele está tentando induzir um usuário a clicar no link dentro da mensagem.
  
O próximo exemplo é o spoofing contoso.com:
  
![Mensagem de phishing-compromisso de email comercial](media/da15adaa-708b-4e73-8165-482fc9182090.jpg)
  
A mensagem parece legítima, mas, na verdade, é uma falsificação. Essa mensagem de phishing é um tipo de comprometimento de email comercial que é uma subcategoria de phishing.

### <a name="2-users-confuse-real-messages-for-fake-ones"></a>2. os usuários confundem mensagens reais para falsificações
  
Segundo, as mensagens falsificadas criam incertezas para os usuários que conhecem mensagens de phishing, mas não podem dizer a diferença entre uma mensagem real e uma falsificada. Por exemplo, o seguinte é um exemplo de uma redefinição de senha real do endereço de email da conta de segurança da Microsoft:
  
![Redefinição de senha legítima da Microsoft](media/58a3154f-e83d-4f86-bcfe-ae9e8c87bd37.jpg)
  
A mensagem acima vem da Microsoft, mas ao mesmo tempo, os usuários são usados para obter mensagens de phishing que podem enganar o usuário clicando em um link e fornecendo suas credenciais, baixando o malware ou respondendo a uma mensagem com conteúdo confidencial. Como é difícil dizer a diferença entre uma redefinição de senha real e uma falsa, muitos usuários ignoram essas mensagens, os relatam como spam ou relatam as mensagens de volta à Microsoft como golpes de phishing perdidos.

Para interromper a falsificação, o setor de filtragem de email desenvolveu protocolos de autenticação de email, como [SPF](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing), [DKIM](https://docs.microsoft.com/office365/SecurityCompliance/use-dkim-to-validate-outbound-email)e [DMARC](https://docs.microsoft.com/office365/SecurityCompliance/use-dmarc-to-validate-email). DMARC impede falsificação examinando o remetente de uma mensagem-o que o usuário vê no cliente de email (nos exemplos acima, isso é service.outlook.com, outlook.com e accountprotection.microsoft.com) – com o domínio que aprovou SPF ou DKIM. Ou seja, o domínio que o usuário vê foi autenticado e, portanto, não é falsificado. Para obter uma discussão mais completa, consulte a seção "*entendendo por que a autenticação de email nem sempre é suficiente para interromper a falsificação"* mais adiante neste artigo.
  
No enTanto, o problema é que os registros de autenticação de email são opcionais, não necessários. Portanto, enquanto os domínios com políticas de autenticação sólida como o microsoft.com e o skype.com são protegidos da falsificação, os domínios que publicam diretivas de autenticação mais fracas, ou nenhuma política, são alvos para serem falsificados. A partir de março de 2018, apenas 9% dos domínios de empresas no Fortune 500 publicam políticas de autenticação de email forte. As 91% restantes podem ser falsificadas por um phishing e, a menos que o filtro de email a detecte usando outra política, pode ser entregue a um usuário final e induzi-los:
  
![Políticas do DMARC das empresas Fortune 500](media/84e77d34-2073-4a8e-9f39-f109b32d06df.jpg)
  
A proporção de empresas de pequeno e médio porte que não estão no Fortune 500 que publicam políticas de autenticação de email forte é menor e ainda menor do que os domínios fora da América do Norte e da Europa Ocidental.
  
Esse é um grande problema porque, embora as empresas talvez não saibam como funciona a autenticação de email, os phishers entendem e aproveitam a falta da ti.
  
Para obter informações sobre como configurar o SPF, DKIM e DMARC, consulte a seção "*Customers of Office 365"* , mais adiante neste documento. 
  
## <a name="stopping-spoofing-with-implicit-email-authentication"></a>Interromper a falsificação com autenticação de email implícita

Como phishing e spear phishing é um problema, e por causa da adoção limitada de políticas seguras de autenticação de email, a Microsoft continua a investir em recursos para proteger seus clientes. Portanto, a Microsoft está se movendo para a *autenticação de email implícita* , se um domínio não se autenticar, a Microsoft o tratará como se tivesse publicado os registros de autenticação de email e o tratará de acordo, se não passar. 
  
Para fazer isso, a Microsoft criou inúmeras extensões para a autenticação de email regular, incluindo a reputação do remetente, histórico do remetente/destinatário, análise comportamental e outras técnicas avançadas. Uma mensagem enviada de um domínio que não publica a autenticação de email será marcada como falsa, a menos que contenha outros sinais para indicar que ela é legítima.
  
Fazendo isso, os usuários finais podem ter certeza de que um email enviado para eles não foi falsificado, os remetentes podem ter certeza de que ninguém está representando o domínio, e os clientes do Office 365 podem oferecer uma proteção ainda melhor, como a proteção de representação.
  
Para ver o comunicado geral da Microsoft, consulte [um mar de Phish parte 2-antifalsificaÇão aprimorada no Office 365](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Schooling-A-Sea-of-Phish-Part-2-Enhanced-Anti-spoofing/ba-p/176209).
  
## <a name="identifying-that-a-message-is-classified-as-spoofed"></a>Identificando se uma mensagem foi classificada como falsificada

### <a name="composite-authentication"></a>Autenticação composta

Embora os SPF, DKIM e DMARC sejam todos úteis por si mesmos, eles não comunicam o status de autenticação suficiente no caso de uma mensagem não ter registros de autenticação explícitos. Portanto, a Microsoft desenvolveu um algoritmo que combina vários sinais em um único valor chamado autenticação composta ou compauth para curto. Os clientes do Office 365 têm valores compauth marcados no cabeçalho *Authentication-Results* nos cabeçalhos da mensagem. 
  
```
Authentication-Results:
  compauth=<fail|pass|softpass|none> reason=<yyy>

```

|**Resultado CompAuth**|**Descrição**|
|:-----|:-----|
|malsucedida|Falha da mensagem autenticação explícita (envio de registros publicados de domínio explicitamente no DNS) ou autenticação implícita (o domínio de envio não publicou registros no DNS, portanto, o Office 365 interpolaru o resultado como se tivesse registros publicados).|
|passar|A mensagem passou autenticação explícita (mensagem passou DMARC ou [melhor palpite aprovado DMARC](https://blogs.msdn.microsoft.com/tzink/2015/05/06/what-is-dmarc-bestguesspass-in-office-365)) ou autenticação implícita com alta confiança (o domínio de envio não publica registros de autenticação de email, mas o Office 365 tem sinais de back-end fortes para indica que a mensagem é provavelmente legítima.|
|softpass|A mensagem passou a autenticação implícita com confiança de baixo para médio (o domínio de envio não publica a autenticação de email, mas o Office 365 tem sinais de back-end para indicar que a mensagem é legítima, mas a intensidade do sinal é mais fraca).|
|nenhum|A mensagem não foi autenticada (ou foi autenticada, mas não foi alinhada), mas a autenticação composta não foi aplicada devido à reputação do remetente ou a outros fatores.|
   
|||
|:-----|:-----|
|**Motivo**|**Descrição**|
|0XX|Falha na autenticação composta da mensagem.<br/>**000** significa que a mensagem falhou DMARC com uma ação de rejeição ou quarentena.  <br/>**001** significa que a mensagem falhou na autenticação de email implícita. Isso significa que o domínio de envio não tinha os registros de autenticação de email publicados, ou se eles tinham, uma diretiva de falha mais fraca (ou uma diretiva de erro de SPF Soft ou neutra, DMARC política de p = None).  <br/>**002** significa que a organização tem uma política para o par de remetente/domínio explicitamente proibido de enviar email falsificado, essa configuração é definida manualmente por um administrador.  <br/>**010** significa que a mensagem falhou DMARC com uma ação de rejeição ou quarentena, e o domínio de envio é um dos domínios aceitos de sua organização (isso faz parte de auto-para-self, ou intra-org, falsificação).  <br/>**011** significa que a mensagem falhou na autenticação de email implícita e o domínio de envio é um dos domínios aceitos de sua organização (isso faz parte de auto-para-self, ou intra-org).|
|Todos os outros códigos (1xx, 2xx, 3xx, 4xx, 5xx)|Corresponde a vários códigos internos por que uma mensagem passou autenticação implícita ou não teve autenticação, mas nenhuma ação foi aplicada.|
   
Ao examinar os cabeçalhos de uma mensagem, um administrador ou até mesmo um usuário final pode determinar como o Office 365 chega à conclusão de que o remetente pode ser falsificado.
  
### <a name="differentiating-between-different-types-of-spoofing"></a>Diferenciar entre diferentes tipos de falsificação

A Microsoft diferencia dois tipos diferentes de mensagens de falsificação:
  
 **Falsificação dentro da organização**
  
Também conhecido como falsificação autoautoria, isso ocorre quando o domínio no endereço de: é o mesmo que ou se alinha com o domínio do destinatário (quando o domínio do destinatário é um dos [domínios aceitos](https://technet.microsoft.com/en-us/library/jj945194%28v=exchg.150%29.aspx)de sua organização); ou, quando o domínio no endereço de: é parte da mesma organização.
  
Por exemplo, o seguinte tem remetente e destinatário do mesmo domínio (contoso.com). Os espaços são inseridos no endereço de email para impedir a coleta de spambots nesta página):
  
De: Sender @ contoso.com
  
Para: destinatário @ contoso.com
  
Os itens a seguir têm os domínios de remetente e destinatário alinhados ao domínio organizacional (fabrikam.com):
  
De: Sender @ foo.fabrikam.com
  
Para: destinatário @ bar.fabrikam.com
  
Os seguintes domínios de remetente e destinatário são diferentes (microsoft.com e bing.com), mas pertencem à mesma organização (ou seja, ambos fazem parte dos domínios aceitos da organização):
  
De: Sender @ microsoft.com
  
Para: destinatário @ bing.com
  
As mensagens que falham na falsificação dentro da organização contêm os seguintes valores nos cabeçalhos:
  
X-Forefront-antispam-Report:... GATO: SPM/HSPM/PHSH;... SFTY: 9.11
  
O gato é a categoria da mensagem e é normalmente marcado como SPM (spam), mas ocasionalmente pode ser HSPM (spam de alta confiança) ou PHISH (phishing), dependendo do que outros tipos de padrões ocorrem na mensagem.
  
O SFTY é o nível de segurança da mensagem, o primeiro dígito (9) significa que a mensagem é phishing e o segundo conjunto de dígitos após o ponto (11) significa que ele é falsificação dentro da organização.
  
Não há um código de motivo específico para a autenticação composta para falsificação dentro da organização, que será carimbada posteriormente em 2018 (cronograma ainda não definido).
  
 **Falsificação entre domínios**
  
Isso ocorre quando o domínio de envio no endereço de: é um domínio externo para a organização de recebimento. As mensagens que falharam na autenticação composta devido à falsificação entre domínios contêm os seguintes valores nos cabeçalhos:
  
Authentication-Results:... compauth = razão do falha = 000/001
  
X-Forefront-antispam-Report:... GATO: FALSIFICAR;... SFTY: 9.22
  
Em ambos os casos, a dica de segurança vermelha a seguir está marcada na mensagem ou um equivalente que é personalizado para o idioma da caixa de correio do destinatário:
  
![Dica de segurança vermelha-detecção de fraude](media/a366156a-14e8-4c14-bfe5-2031b21936f8.jpg)
  
É só observar o endereço de: e saber quais são seus emails de destinatário ou inspecionar os cabeçalhos de email, que você pode diferenciar entre a falsificação entre domínios e dentro da organização.
  
## <a name="how-customers-of-office-365-can-prepare-themselves-for-the-new-anti-spoofing-protection"></a>Como os clientes do Office 365 podem se preparar para a nova proteção contra falsificação

### <a name="information-for-administrators"></a>Informações para administradores

Como administrador de uma organização no Office 365, há várias informações importantes que você deve estar ciente.
  
### <a name="understanding-why-email-authentication-is-not-always-enough-to-stop-spoofing"></a>Entendendo por que a autenticação de email nem sempre é suficiente para interromper a falsificação

A nova proteção contra falsificação depende da autenticação de email (SPF, DKIM e DMARC) para não marcar uma mensagem como falsificação. Um exemplo comum é quando um domínio de envio nunca publicou registros SPF. Se não houver registros SPF ou se estiverem configurados incorretamente, uma mensagem enviada será marcada como falsificada, a menos que a Microsoft tenha inteligência de back-end que diga que a mensagem é legítima.
  
Por exemplo, antes de a antifalsificação ser implantada, uma mensagem pode ter a aparência a seguir sem o registro SPF, nenhum registro DKIM e nenhum registro DMARC: 
  
```
Authentication-Results: spf=none (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; contoso.com; dkim=none
  (message not signed) header.d=none; contoso.com; dmarc=none
  action=none header.from=example.com;
From: sender @ example.com
To: receiver @ contoso.com
```
Após a falsificação, se você tiver o Office 365 Enterprise e5, o EOP ou a ATP, o valor compauth será carimbado:
  
```
Authentication-Results: spf=none (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; contoso.com; dkim=none
  (message not signed) header.d=none; contoso.com; dmarc=none
  action=none header.from=example.com; compauth=fail reason=001
From: sender @ example.com
To: receiver @ contoso.com

```

Se o example.com corrigiu isso Configurando um registro SPF, mas não um registro DKIM, isso transmitiria a autenticação composta porque o domínio que passou o SPF alinhado ao domínio no endereço de: 
  
```
Authentication-Results: spf=pass (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; contoso.com; dkim=none
  (message not signed) header.d=none; contoso.com; dmarc=bestguesspass
  action=none header.from=example.com; compauth=pass reason=109
From: sender @ example.com
To: receiver @ contoso.com
```

Ou, se eles configurarem um registro DKIM, mas não um registro SPF, isso também passaria na autenticação composta, pois o domínio no DKIM-Signature que passou alinhado com o domínio no endereço de: 
  
```
Authentication-Results: spf=none (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; contoso.com; dkim=pass
  (signature was verified) header.d=outbound.example.com;
  contoso.com; dmarc=bestguesspass action=none
  header.from=example.com; compauth=pass reason=109
From: sender @ example.com
To: receiver @ contoso.com
```

No enTanto, um phishing também pode configurar o SPF e o DKIM e assinar a mensagem com seu próprio domínio, mas especificar um domínio diferente no endereço de:. Nem o SPF nem o DKIM exigem que o domínio seja alinhado com o domínio no endereço de:, a menos que example.com publicado DMARC registros, isso não seria marcado como um falso usando o DMARC: 
  
```
Authentication-Results: spf=pass (sender IP is 5.6.7.8)
  smtp.mailfrom=maliciousDomain.com; contoso.com; dkim=pass
  (signature was verified) header.d=maliciousDomain.com;
  contoso.com; dmarc=none action=none header.from=example.com;
From: sender @ example.com
To: receiver @ contoso.com
```

No cliente de email (Outlook, Outlook na Web ou qualquer outro cliente de email), somente o domínio de: é exibido, não o domínio no SPF ou DKIM e pode induzir o usuário a pensar que a mensagem provém do example.com, mas que, na verdade, vem de maliciousDomain.com .
  
![A mensagem autenticada, exceto: domain, não se alinha com o que passou SPF ou DKIM](media/a9b5ab2a-dfd3-47c6-8ee8-e3dab2fae528.jpg)
  
Por esse motivo, o Office 365 requer que o domínio no endereço: seja alinhado com o domínio na assinatura SPF ou DKIM e, se não contiver, contenha alguns outros sinais internos que indiquem que a mensagem é legítima. Caso contrário, a mensagem seria uma falha de compauth. 
  
```
Authentication-Results: spf=none (sender IP is 5.6.7.8)
  smtp.mailfrom=maliciousDomain.com; contoso.com; dkim=pass
  (signature was verified) header.d=maliciousDomain.com;
  contoso.com; dmarc=none action=none header.from=contoso.com;
  compauth=fail reason=001
From: sender@contoso.com
To: someone@example.com
```

Dessa forma, a antifalsificação do Office 365 protege contra domínios sem autenticação e de domínios que definem a autenticação, mas não são compatíveis com relação ao domínio no endereço de: como é aquele que o usuário vê e acredita ser o remetente da mensagem. Isso é verdadeiro tanto para domínios externos para sua organização, quanto para domínios dentro de sua organização.
  
Portanto, se você receber uma mensagem que falhou na autenticação composta e estiver marcada como falsificada, mesmo que a mensagem tenha passado SPF e DKIM, isso ocorre porque o domínio que aprovou o SPF e o DKIM não estão alinhados com o domínio no endereço de:.
  
### <a name="understanding-changes-in-how-spoofed-emails-are-treated"></a>Noções básicas sobre alterações no modo como os emails falsificados são tratados

Atualmente, para todas as organizações no Office 365-ATP e não-ATP-messages que falham DMARC com uma política de rejeição ou quarentena são marcadas como spam e normalmente têm a ação de spam de alta confiança ou, às vezes, a ação de spam regular (dependendo de se outro spam as regras primeiro o identificam como spam. As detecções de falsificação dentro da organização usam a ação regular de spam. Esse comportamento não precisa ser habilitado, nem pode ser desabilitado.
  
No enTanto, para mensagens de falsificação entre domínios, antes dessa alteração eles passaram por spam, phishing e verificações de malware regulares e, se outras partes do filtro as identificarem como suspeitas, marcariam como spam, Phish ou malware, respectivamente. Com a nova proteção de falsificação entre domínios, qualquer mensagem que não possa ser autenticada será, por padrão, a ação definida na política antifalsificação \> do anti-phishing. Se não houver um definido, ele será movido para uma pasta de lixo eletrônico de usuários. Em alguns casos, mais mensagens suspeitas também terão a dica de segurança vermelha adicionada à mensagem.
  
Isso pode resultar em algumas mensagens que foram previamente marcadas como spam ainda estão sendo marcadas como spam, mas também terão uma dica de segurança vermelha; em outros casos, as mensagens que foram previamente marcadas como não spam começarão a ser marcadas como spam (CAT: SPOOF) com uma dica de segurança vermelha adicionada. Ainda em outros casos, os clientes que estavam movendo todos os spams e phishing para a quarentena podem vê-los para a pasta de lixo eletrônico (esse comportamento pode ser alterado, confira [alterar suas configurações de anti-falsificação](#changing-your-anti-spoofing-settings)).
  
Há várias maneiras diferentes pelas quais uma mensagem pode ser falsificada (consulte [diferenciação entre diferentes tipos de falsificação](#differentiating-between-different-types-of-spoofing) anteriormente neste artigo), mas a partir de março de 2018, a maneira como o Office 365 trata essas mensagens ainda não são unificadas. A tabela a seguir é um resumo rápido, com a proteção de falsificação entre domínios sendo novo comportamento: 
  
|**Tipo de falsificação**|**Category**|**Dica de segurança adicionada?**|**Aplica-se a**|
|:-----|:-----|:-----|:-----|
|Falha de DMARC (quarentena ou rejeição)  <br/> |HSPM (padrão), também pode ser SPM ou PHSH  <br/> |Não (ainda não)  <br/> |Todos os clientes do Office 365, Outlook.com  <br/> |
|Auto para si  <br/> |SPM  <br/> |Sim  <br/> |Todas as organizações do Office 365, Outlook.com  <br/> |
|Entre domínios  <br/> |SIMULAÇÃO  <br/> |Sim  <br/> |Proteção avançada contra ameaças do Office 365 e clientes e5  <br/> |

### <a name="changing-your-anti-spoofing-settings"></a>Alterar as configurações de anti-falsificação

Para criar ou atualizar suas configurações de antifalsificação (entre domínios), navegue até as configurações antifalsificação \> do anti-phishing na guia política de gerenciamento \> de ameaças no centro de &amp; conformidade de segurança. Se você nunca criou nenhuma configuração anti-phishing, será necessário criar uma:
  
![Anti-phishing-criar uma nova política](media/9337ec91-270e-4fa7-9dfa-a51a2d1eb95e.jpg)
  
Se você já criou um, pode selecioná-lo para modificá-lo:
  
![Anti-phishing – modificar política existente](media/75457a7c-882e-4984-80d1-21a12b42c53a.jpg)
  
Selecione a política que você acabou de criar e siga as etapas descritas em [saiba mais sobre o spoof Intelligence](learn-about-spoof-intelligence.md).
  
![Habilitar ou desabilitar a suavização de antifalsificação](media/c49e2147-c954-443c-9144-1cbd139e1166.jpg)
  
![Habilitar ou desabilitar dicas de segurança antifalsificação](media/eec7c407-31fc-4f73-8325-307d82d1fb53.jpg)
  
Para criar uma nova política usando o PowerShell: 
  
```powershell
$org = Get-OrganizationConfig
$name = "My first anti-phishing policy for " + $org.Name
# Note: The name should not exclude 64 characters, including spaces.
# If it does, you will need to pick a smaller name.
# Next, create a new anti-phishing policy with the default values
New-AntiphishPolicy -Name $Name
# Select the domains to scope it to
# Multiple domains are specified in a comma-separated list
$domains = "domain1.com, domain2.com, domain3.com"
# Next, create the anti-phishing rule, scope it to the anti-phishing rule
New-AntiphishRule -Name $name -AntiphishPolicy $name -RecipientDomainIs $domains
```

Você pode modificar os parâmetros da política anti-phishing usando o PowerShell, seguindo a documentação em [set-AntiphishPolicy](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/Set-AntiPhishPolicy?view=exchange-ps). Você pode especificar o $name como um parâmetro:
  
```powershell
Set-AntiphishPolicy -Identity $name <fill in rest of parameters>
```

Mais tarde, no 2018, em vez de você precisar criar uma política padrão, uma será criada para você com escopo para todos os destinatários em sua organização para que você não precise especificá-la manualmente (as capturas de tela abaixo estão sujeitas a alterações antes da implementação final).
  
![Política padrão para anti-phishing](media/1f27a0bf-e202-4e12-bbac-24baf013c8f9.jpg)
  
Ao contrário de uma política que você cria, não é possível excluir a política padrão, modificar sua prioridade ou escolher quais usuários, domínios ou grupos para fazer o escopo.
  
![Detalhes da política padrão do anti-phishing](media/30c21ceb-df52-4c93-aa65-f44a55dc1009.jpg)
  
Para configurar sua proteção padrão usando o PowerShell:
  
```powershell
$defaultAntiphishPolicy = Get-AntiphishPolicy | ? {$_.IsDefault -eq $true}
Set-AntiphishPolicy -Identity $defaultAntiphishPolicy.Name -EnableAntispoofEnforcement <$true|$false>
```

Você só deve desabilitar a proteção contra falsificação se tiver outro servidor de email ou servidores na frente do Office 365 (Confira cenários legítimos para desabilitar a antifalsificação para obter mais detalhes).
  
```powershell
$defaultAntiphishPolicy = Get-AntiphishiPolicy | ? {$_.IsDefault $true}
Set-AntiphishPolicy -Identity $defaultAntiphishPolicy.Name -EnableAntispoofEnforcement $false 

```
> [!IMPORTANT]
> Se o primeiro salto no seu caminho de email for o Office 365 e você estiver recebendo muitos emails legítimos marcados como falsificados, primeiro você deve configurar seus remetentes que têm permissão para enviar emails falsificados para seu domínio (consulte a seção *"Gerenciando remetentes legítimos que estão enviando u nauthenticated email "* ). Se você ainda estiver recebendo muitos falsos positivos (ou seja, mensagens legítimas marcadas como falso), não recomendamos desabilitar totalmente a proteção contra falsificação. Em vez disso, recomendamos escolher Basic em vez de alta proteção. É melhor trabalhar através de falsos positivos do que expor sua organização a emails falsificados, que podem acabar impondo custos significativamente mais altos a longo prazo.

### <a name="managing-legitimate-senders-who-are-sending-unauthenticated-email"></a>Gerenciando remetentes legítimos que estão enviando emails não autenticados

O Office 365 acompanha quem está enviando emails não autenticados para sua organização. Se o serviço achar que o remetente não é legítimo, ele irá marcá-lo como uma falha de *compauth* . Isso será classificado como FALSIFICAção, embora dependa de sua política antifalsificação que foi aplicada à mensagem.
  
No enTanto, como administrador, você pode especificar quais remetentes têm permissão para enviar emails falsificados, substituindo a decisão do Office 365.
  
**Método 1-se a sua organização for proprietária do domínio, configure email Authentication**
  
Este método pode ser usado para resolver o spoofing da organização e a falsificação entre domínios em casos em que você possui ou interage com vários locatários. Também ajuda a resolver a falsificação entre domínios onde você envia para outros clientes no Office 365 e também para terceiros hospedados em outros provedores.
  
Para obter mais detalhes, consulte [Customers of Office 365](#customers-of-office-365).

**Método 2-usar inteligência de falsificação para configurar remetentes permitidos de emails não autenticados**
  
Você também pode usar o [spoof Intelligence](https://support.office.com/article/Learn-more-about-spoof-intelligence-978c3173-3578-4286-aaf4-8a10951978bf) para permitir que os remetentes transmitam mensagens não autenticadas para sua organização. 
  
Para domínios externos, o usuário falsificado é o domínio no endereço de, enquanto a infraestrutura de envio é o endereço IP de envio (dividido em/24 intervalos CIDR) ou o domínio organizacional do registro PTR (na captura de tela abaixo, o IP de envio pode ser 131.107.18.4 cujo registro PTR é outbound.mail.protection.outlook.com e isso seria mostrado como outlook.com para a infraestrutura de envio).
  
Para permitir que este remetente envie emails não autenticados, altere **não** para **Sim**.
  
![ConFigurando os remetentes permitidos contra falsificação](media/d4334921-d820-4334-8217-788279701e94.jpg)
  
Você também pode usar o PowerShell para permitir que o remetente específico falsifique seu domínio:
  
```powershell
$file = "C:\My Documents\Summary Spoofed Internal Domains and Senders.csv"
```

```powershell
Get-PhishFilterPolicy -Detailed -SpoofAllowBlockList -SpoofType External | Export-CSV $file
```

![Obtendo remetentes falsificados do PowerShell](media/0e27ffcf-a5db-4c43-a19b-fa62326d5118.jpg)
  
Na imagem anterior, foram adicionadas quebras de linha adicionais para fazer com que esta captura de tela caiba. Normalmente, todos os valores aparecem em uma única linha.
  
Edite o arquivo e procure a linha que corresponde ao outlook.com e ao bing.com e altere a entrada AllowedToSpoof de não para Sim:
  
![Configuração de falsificação permitir sim no PowerShell](media/62340452-62d3-4958-9ce9-afe5275a870d.jpg)
  
Salve o arquivo e, em seguida, execute:
  
```powershell
$UpdateSpoofedSenders = Get-Content -Raw "C:\My Documents\Spoofed Senders.csv"
Set-PhishFilterPolicy -Identity Default -SpoofAllowBlockList $UpdateSpoofedSenders
```

Isso agora permitirá que o bing.com envie emails não autenticados de \*. Outlook.com.

**Método 3-criar uma entrada de permissão para o par de remetente/destinatário**
  
Você também pode optar por ignorar a filtragem de spam de um remetente específico. Para obter mais detalhes, consulte [como adicionar um remetente com segurança a uma lista de permissões no Office 365](https://blogs.msdn.microsoft.com/tzink/2017/11/29/how-to-securely-add-a-sender-to-an-allow-list-in-office-365/).
  
Se você usar esse método, ele ignorará spam e parte da filtragem de phishing, mas não a filtragem de malware.
  
**Método 4 – contate o remetente e peça para configurar a autenticação de email**
  
Devido ao problema de spam e phishing, a Microsoft recomenda que todos os remetentes configurem a autenticação de email. Se você souber um administrador do domínio de envio, entre em contato com ele e solicite que eles configurem os registros de autenticação de email para que você não precise adicionar substituições. Para obter mais informações, consulte [Administradores de domínios que não são clientes do Office 365](#administrators-of-domains-that-are-not-office-365-customers)", mais adiante neste artigo. 
  
Embora isso possa ser difícil no princípio, para obter domínios de envio para autenticar, ao longo do tempo, à medida que mais e mais filtros de email começam a ser lixo eletrônico ou mesmo rejeitando seus emails, ele fará com que eles configurem os registros apropriados para garantir uma entrega melhor.
  
### <a name="viewing-reports-of-how-many-messages-were-marked-as-spoofed"></a>Exibindo relatórios sobre quantas mensagens foram marcadas como falsificadas

Depois que a política antifalsificação estiver habilitada, você poderá usar a inteligência de ameaças para obter números sobre quantas mensagens são marcadas como phishing. Para fazer isso, vá para o centro &amp; de conformidade de segurança (SCC) no \> Gerenciador de gerenciamento de ameaças, defina o modo de exibição como Phish e agrupe por domínio do remetente ou status de proteção:
  
![Visualizando quantas mensagens são marcadas como phishing](media/de25009a-44d4-4c5f-94ba-9c75cd9c64b3.jpg)
  
Você pode interagir com os vários relatórios para ver quantas foram marcadas como phishing, incluindo as mensagens marcadas como falso. Para saber mais, confira [introdução à inteligência contra ameaças do Office 365](get-started-with-ti.md).
  
Você ainda não pode dividir quais mensagens foram marcadas devido à falsificação em vez de outros tipos de phishing (phishing geral, de domínio ou usuário, e assim por diante). No enTanto, mais tarde, você poderá fazer isso por meio do &amp; centro de conformidade de segurança. Depois de fazer isso, você pode usar esse relatório como um local de início para identificar os domínios de envio que podem ser legítimos que estão sendo marcados como falsificados devido à falha na autenticação.
  
A captura de tela a seguir é uma proposta de como será a aparência desses dados, mas podem ser alteradas quando lançadas:
  
![Exibindo relatórios de phishing por tipo de detecção](media/dd25d63f-152c-4c55-a07b-184ecda2de81.jpg)
  
Para clientes não-ATP e e5, esses relatórios estarão disponíveis posteriormente nos relatórios de status de proteção contra ameaças (TPS), mas serão atrasados por pelo menos 24 horas. Esta página será atualizada à medida que elas forem integradas ao &amp; centro de conformidade de segurança.
  
### <a name="predicting-how-many-messages-will-be-marked-as-spoof"></a>PreVendo quantas mensagens serão marcadas como falsas

Quando o Office 365 atualiza suas configurações para permitir que você desative a imposição antifalsificação ou com a imposição básica ou alta, você terá a capacidade de ver como a disposição da mensagem será alterada nas várias configurações. Ou seja, se a antifalsificação estiver desAtivada, você poderá ver quantas mensagens serão detectadas como falsificadas, se você mudar para básico; ou, se for básico, você poderá ver quantas mensagens serão detectadas como falsificadas se você ativá-la para alta.
  
Este recurso está atualmente em desenvolvimento. À medida que mais detalhes são definidos, esta página será atualizada com capturas de tela do centro de segurança e conformidade e com os exemplos do PowerShell.
  
![Relatório "e se" para habilitar a anti-falsificação](media/fdd085ae-02c1-4327-a063-bfe9a32ff1eb.jpg)
  
![Possível UX para permitir um remetente falso](media/53f9f73e-fb01-47f3-9a6d-850c1aef5efe.jpg)
  
### <a name="understanding-how-spam-phishing-and-advanced-phishing-detections-are-combined"></a>Noções básicas sobre como spam, phishing e detecções avançadas de phishing são combinados

As organizações que usam o Exchange Online, com ou sem ATP, podem especificar quais ações serão executadas quando o serviço identificar mensagens como malware, spam, spam de alta confiança, phishing e massa. Com as políticas de anti-phishing do ATP para clientes ATP e as políticas anti-phishing para clientes do EOP e o fato de que uma mensagem pode atingir vários tipos de detecção (por exemplo, malware, phishing e representação do usuário), pode haver uma certa confusão quanto ao que política se aplica.
  
Em geral, a política aplicada a uma mensagem é identificada no cabeçalho X-Forefront-antispam-Report na propriedade CAT (categoria).
  
|**Prioridade**|**Política**|**Category**|**Onde gerenciado?**|**Aplica-se a**|
|:-----|:-----|:-----|:-----|:-----|
|1  <br/> |Software  <br/> |MALW  <br/> |[Política de malware](configure-anti-malware-policies.md) <br/> |Todas as organizações  <br/> |
|duas  <br/> |Fraude  <br/> |PHSH  <br/> |[Configurar suas políticas de filtro de spam](configure-your-spam-filter-policies.md) <br/> |Todas as organizações  <br/> |
|3D  <br/> |Spam de alta confiança  <br/> |HSPM  <br/> |[Configurar suas políticas de filtro de spam](configure-your-spam-filter-policies.md) <br/> |Todas as organizações  <br/> |
|quatro  <br/> |Spoofing  <br/> |SIMULAÇÃO  <br/> |[Política anti-phishing](https://go.microsoft.com/fwlink/?linkid=864553), inteligência de [falsificação](learn-about-spoof-intelligence.md) <br/> |Todas as organizações  <br/> |
|0,5  <br/> |Spam  <br/> |SPM  <br/> |[Configurar suas políticas de filtro de spam](configure-your-spam-filter-policies.md) <br/> |Todas as organizações  <br/> |
|6  <br/> |Impresso  <br/> |IMPRESSO  <br/> |[Configurar suas políticas de filtro de spam](configure-your-spam-filter-policies.md) <br/> |Todas as organizações  <br/> |
|178  <br/> |Representação de domínio  <br/> |DIMP  <br/> |[Configurar políticas de anti-phishing e anti-phishing do Office 365 ATP](set-up-anti-phishing-policies.md) <br/> |Organizações somente com ATP  <br/> |
|8  <br/> |Representação de usuário  <br/> |UIMP  <br/> |[Configurar políticas de anti-phishing e anti-phishing do Office 365 ATP](set-up-anti-phishing-policies.md) <br/> |Organizações somente com ATP <br/> |

Se você tiver várias políticas anti-phishing diferentes, será aplicada a prioridade mais alta. Por exemplo, suponha que você tenha duas políticas:

|**Política**|**Prioridade**|**Representação de usuário/domínio**|**Anti-falsificação**|
|:-----|:-----|:-----|:-----|
|A  <br/> |1  <br/> |Ativado  <br/> |Desligado  <br/> |
|B  <br/> |duas  <br/> |Desligado  <br/> |Ativado  <br/> |

Se uma mensagem chegar e for identificada como falsificação e representação do usuário, e o mesmo conjunto de usuários estiver no escopo da política A e da política B, a mensagem será tratada como uma falsificação, mas nenhuma ação será aplicada, pois a antifalsificação está desativada e a FALSIFICAção é executada em uma prioridade mais alta (4) que a representação de usuário (8).
  
Para fazer com que outros tipos de política de phishing se apliquem, será necessário ajustar as configurações das quais as várias políticas são aplicadas.
  
### <a name="legitimate-scenarios-to-disable-anti-spoofing"></a>Cenários legítimos para desabilitar a anti-falsificação

A antifalsificação melhor protege os clientes contra ataques de phishing e, portanto, desabilitar a proteção contra falsificação é altamente recomendável. Ao desabilitá-lo, você pode resolver alguns falsos positivos de curto prazo, mas o longo prazo será exposto a mais riscos. O custo para configurar a autenticação no lado do remetente ou fazer ajustes nas políticas de phishing, geralmente são eventos de ocorrência única ou exigem apenas manutenção mínima e periódica. No enTanto, o custo de recuperação de um ataque de phishing em que os dados foram expostos ou os ativos foram muito mais altos.
  
Por esse motivo, é melhor trabalhar com o antifalsificação de falsos positivos do que desabilitar a proteção antifalsificada.
  
No enTanto, há um cenário legítimo em que a anti-falsificação deve ser desabilitada e, quando há produtos adicionais de filtragem de email no roteamento de mensagens, e o Office 365 não é o primeiro salto no caminho de email:
  
![O registro MX do cliente não aponta para o Office 365](media/62127c16-cfb8-4880-9cad-3c12d827c67e.jpg)
  
O outro servidor pode ser um servidor de email local do Exchange, um dispositivo de filtragem de email, como o IronPort, ou outro serviço hospedado na nuvem.
  
Se o registro MX do domínio do destinatário não apontar para o Office 365, não há necessidade de desabilitar a antifalsificação, pois o Office 365 procura o registro MX do seu domínio de recebimento e suprime o antifalsificação se ele apontar para outro serviço. Se você não sabe se o seu domínio tem outro servidor na frente, você pode usar um site como o MX Toolbox para pesquisar o registro MX. Isso pode dizer algo como o seguinte:
  
![O registro MX indica que o domínio não aponta para o Office 365](media/d868bb9f-3462-49aa-baea-9447a3ce4877.jpg)
  
Este domínio tem um registro MX que não aponta para o Office 365, portanto, o Office 365 não aplicaria a aplicação antifalsificação.
  
No enTanto, se o registro MX do domínio do destinatário apontar para *o* Office 365, embora haja outro serviço na frente do Office 365, você deve desabilitar a antifalsificação. O exemplo mais comum é o uso de uma reconfiguração de destinatário: 
  
![Diagrama de roteamento para reconfiguração de destinatário](media/070d90d1-50a0-42e4-9fd3-920bc99a7cad.jpg)
  
O registro MX do domínio contoso. com aponta para o servidor local, enquanto o registro MX do domínio @office365. contoso. net aponta para o Office 365 porque contém \*. Protection.Outlook.com ou \*. eo.Outlook.com no registro MX:
  
![O registro MX aponta para o Office 365, portanto, provavelmente, a reconfiguração do destinatário](media/4101ad51-ef92-4907-b466-b41d14d344ca.jpg)
  
Certifique-se de diferenciar quando o registro MX de um domínio do destinatário não apontar para o Office 365 e quando tiver percorrido uma regravação do destinatário. É importante dizer a diferença entre esses dois casos.
  
Se você não tiver certeza se o domínio de recebimento passou ou não por regravação de destinatários, às vezes você pode saber com os cabeçalhos da mensagem.
  
a) primeiro, examine os cabeçalhos da mensagem do domínio do destinatário no cabeçalho Authentication-Results:
  
```
Authentication-Results: spf=fail (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; office365.contoso.net; dkim=fail
  (body hash did not verify) header.d=simple.example.com;
  office365.contoso.net; dmarc=none action=none
  header.from=example.com; compauth=fail reason=001
```

O domínio do destinatário é encontrado no texto em negrito vermelho acima, neste caso, office365.contoso.net. Isso pode ser diferente do destinatário no cabeçalho para::
  
Para: exemplo de \<destinatário @ contoso.com\>
  
Executar uma pesquisa de registro MX do domínio do destinatário real. Se ele contiver \*. protection.outlook.com, mail.Messaging.Microsoft.com \*,. eo.Outlook.com ou mail.global.frontbridge.com, isso significa que a MX aponta para o Office 365.
  
Se não contiver esses valores, significa que o MX não aponta para o Office 365. Uma ferramenta que você pode usar para verificar se essa é a caixa de ferramentas MX.
  
Para esse exemplo específico, o seguinte diz que contoso.com, o domínio que se parece com o destinatário, pois ele é o cabeçalho to:, tem um registro MX apontando para um servidor local:
  
![O registro MX aponta para o servidor local](media/2444144a-9a90-4319-96b2-d115041f669f.jpg)
  
No enTanto, o destinatário real é office365.contoso.net cujo registro MX aponta para o Office 365:
  
![MX aponta para o Office 365, deve ser reconfiguração de destinatário](media/10cf3245-9b50-475a-b655-d8a51f99d812.jpg)
  
Portanto, essa mensagem provavelmente passou por uma regravação de destinatário.
  
b) segunda, certifique-se de distinguir entre casos de uso comuns de regravações de destinatário. Se você pretende reescrever o domínio do destinatário para \*. onmicrosoft.com, em vez disso, reescreva \*-o em. mail.onmicrosoft.com.
  
Depois de identificar o domínio do destinatário final que é roteado por trás de outro servidor e o registro MX do domínio do destinatário realmente aponta para o Office 365 (conforme publicado em seus registros DNS), você pode continuar a desabilitar a antifalsificação.
  
Lembre-se de que você não deseja desabilitar a antifalsificação se o primeiro salto do domínio no caminho de roteamento for o Office 365, somente quando estiver por trás de um ou mais serviços.
  
### <a name="how-to-disable-anti-spoofing"></a>Como desabilitar a suavização de antifalsificação

Se você já tiver uma política anti-phishing criada, defina o parâmetro EnableAntispoofEnforcement como $false:
  
```
$name = "<name of policy>"
Set-AntiphishPolicy -Identity $name -EnableAntiSpoofEnforcement $false

```

Se você não souber o nome da política (ou políticas) a ser desativada, poderá exibi-las:
  
```
Get-AntiphishPolicy | fl Name
```

Se você não tiver políticas anti-phishing existentes, poderá criar uma e, em seguida, desabilitá-la (mesmo que você não tenha uma política, a antifalsificação ainda seja aplicada; posteriormente em 2018, uma política padrão será criada para você e você poderá então desabilitar isso em vez de criar uma) . Você terá que fazer isso em várias etapas:
  
```
$org = Get-OrganizationConfig
$name = "My first anti-phishing policy for " + $org.Name
# Note: If the name is more than 64 characters, you will need to choose a smaller one
```

```
# Next, create a new anti-phishing policy with the default values
New-AntiphishPolicy -Name $Name
# Select the domains to scope it to
# Multiple domains are specified in a comma-separated list
$domains = "domain1.com, domain2.com, domain3.com"
# Next, create the anti-phishing rule, scope it to the anti-phishing rule
New-AntiphishRule -Name $name -AntiphishPolicy -RecipientDomainIs $domains
# Finally, scope the anti-phishing policy to the domains
Set-AntiphishPolicy -Identity $name -EnableAntispoofEnforcement $false

```

A desabilitação da antifalsificação só estará disponível via cmdlet (posteriormente, ela estará disponível no centro &amp; de conformidade de segurança). Se você não tiver acesso ao PowerShell, crie um tíquete de suporte.
  
Lembre-se de que isso só deve ser aplicado a domínios que passam por roteamento indireto quando enviados para o Office 365. Resistir à tentação de desabilitar a antifalsificação devido a alguns falsos positivos, será melhor na execução longa para que funcionem.
  
### <a name="information-for-individual-users"></a>Informações para usuários individuais

Os usuários individuais são limitados em como podem interagir com a dica de segurança anti-falsificação. No enTanto, há várias coisas que você pode fazer para resolver cenários comuns.
  
### <a name="common-scenario-1---mailbox-forwarding"></a>#1 de cenário comum – encaminhamento de caixa de correio

Se você usar outro serviço de email e encaminhar seu email para o Office 365 ou Outlook.com, seu email poderá ser marcado como falsificação e receber uma dica de segurança vermelha. O Office 365 e o Outlook.com Plan para resolver isso automaticamente quando o encaminhador é um dos Outlook.com, Office 365, Gmail ou qualquer outro serviço que usa o [protocolo Arc](https://arc-spec.org). No enTanto, até que a correção seja implantada, os usuários devem usar o recurso de contas conectadas para importar suas mensagens diretamente, em vez de usar a opção de encaminhamento.
  
Para configurar contas conectadas no Office 365, selecione o ícone de engrenagem no canto superior direito das contas \> de caixa de \> correio \> de conta \> de email da interface da Web do Office 365 conectadas.
  
![Opção de contas conectadas do Office 365](media/e8e841ca-8861-4d83-8506-2a0858c51010.jpg)
  
No Outlook.com, o processo é a opção opções \> \> de ícone \> de \> engrenagem contas de email conectadas.
  
### <a name="common-scenario-2---discussion-lists"></a>#2 de cenário comuns – listas de discussão

As listas de discussão são conhecidas por ter problemas com a antifalsificação devido à maneira como encaminhar a mensagem e modificar o conteúdo ainda manter o original de: endereço.
  
Por exemplo, suponha que seu endereço de email seja User @ contoso.com, e você esteja interessado em assistir à visita e ingressar na lista de discussão birdwatchers @ example.com. Ao enviar uma mensagem para a lista de discussão, você pode enviá-la dessa forma:
  
**De:** John Doe \<usuário @ contoso.com\> 
  
**Para:** Lista \<de discussão do Birdwatcher birdwatchers @ example.com\> 
  
**Assunto:** Grande visualização de Jays azuis no topo de Mt. Rainier esta semana 
  
Qualquer pessoa deseja fazer o check-out da exibição desta semana de Mt. Rainier?
  
Quando a lista de emails receber a mensagem, ela formatará a mensagem, modificará seu conteúdo e a repetirá para o restante dos membros na lista de discussão que é composta por participantes de vários receptores de email diferentes.
  
**De:** John Doe \<usuário @ contoso.com\> 
  
**Para:** Lista \<de discussão do Birdwatcher birdwatchers @ example.com\> 
  
**Assunto:** [BIRDWATCHERS] Grande visualização de Jays azuis no topo de Mt. Rainier esta semana 
  
Qualquer pessoa deseja fazer o check-out da exibição desta semana de Mt. Rainier?
  
---
  
Essa mensagem foi enviada para a lista de discussão do birdwatchers. Você pode cancelar a assinatura a qualquer momento.
  
No acima, a mensagem repetida tem o mesmo de: Address (User @ contoso.com), mas a mensagem original foi modificada adicionando uma marca à linha de assunto e um rodapé à parte inferior da mensagem. Esse tipo de modificação de mensagem é comum nas listas de endereçamento e pode resultar em falsos positivos.
  
Se você ou alguém da sua organização for um administrador da lista de endereçamento, você poderá configurá-lo para passar por verificações anti-falsificação.
  
- Verificar as perguntas FREQUENTEs em DMARC.org: [eu opere uma lista de endereçamento e desejo interoperar com o DMARC, o que devo fazer?](https://dmarc.org/wiki/FAQ#I_operate_a_mailing_list_and_I_want_to_interoperate_with_DMARC.2C_what_should_I_do.3F)

- Leia as instruções nesta postagem de blog: [uma dica para que os operadores de lista de endereçamento interoperem com o DMARC para evitar falhas](https://blogs.msdn.microsoft.com/tzink/2017/03/22/a-tip-for-mailing-list-operators-to-interoperate-with-dmarc-to-avoid-failures/)

- Considere instalar atualizações no servidor de lista de endereçamento para dar suporte ao arco, consulte[https://arc-spec.org](https://arc-spec.org/)

Se você não tem a propriedade da lista de endereçamento:
  
- Você pode solicitar o mantenedor da lista de endereçamento para implementar uma das opções acima (elas também devem ter a autenticação de email configurada para o domínio para o qual a lista de endereçamento é retransmitida)

- Você pode criar regras de caixa de correio em seu cliente de email para mover mensagens para a caixa de entrada. Você também pode solicitar que os administradores da sua organização configurem regras de permissão ou substituições conforme discutido na seção Gerenciando remetentes legítimos que estão enviando emails não autenticados

- Você pode criar um tíquete de suporte com o Office 365 para criar uma substituição para a lista de endereçamento para tratá-la como legítima

### <a name="other-scenarios"></a>Outros cenários

1. Se nenhum dos cenários comuns acima se aplica à sua situação, relate a mensagem como um falso positivo de volta para a Microsoft. Para obter mais informações, consulte a seção [como posso relatar spam ou mensagens que não são spam de volta para a Microsoft?](#how-can-i-report-spam-or-non-spam-messages-back-to-microsoft) mais adiante neste artigo. 

2. Você também pode entrar em contato com seu administrador de email que pode ser gerado como um tíquete de suporte com a Microsoft. A equipe de engenharia da Microsoft investigará por que a mensagem foi marcada como falsa.

3. Além disso, se você souber quem é o remetente e tiver certeza de que eles não estão sendo falsificados de forma mal-intencionada, você poderá responder ao remetente, indicando que eles estão enviando mensagens de um servidor de email que não é autenticado. Às vezes, isso resulta no remetente original contatando seu administrador de ti, que configurará os registros de autenticação de email necessários.
  
Quando remetentes suficientes respondem a proprietários de domínio que devem configurar registros de autenticação de email, ele os Spurs a realizar ações. Embora a Microsoft também funcione com proprietários de domínio para publicar os registros necessários, ajuda ainda mais quando usuários individuais o solicitam.

4. Opcionalmente, adicione o remetente à sua lista de remetentes seguros. No enTanto, lembre-se de que, se um phishing falsificar essa conta, ele será entregue à sua caixa de correio. Portanto, essa opção deve ser usada com moderação.

## <a name="how-senders-to-microsoft-should-prepare-for-anti-spoofing-protection"></a>Como os remetentes da Microsoft devem se preparar para a proteção contra falsificação

Se você for um administrador que envia mensagens no momento para a Microsoft, o Office 365 ou o Outlook.com, verifique se o seu email está autenticado corretamente caso contrário, ele pode ser marcado como spam ou phishing.
  
### <a name="customers-of-office-365"></a>Clientes do Office 365

Se você é um cliente do Office 365 e usa o Office 365 para enviar emails de saída:
  
- Para seus domínios, [Configure o SPF no Office 365 para ajudar a impedir a falsificação](set-up-spf-in-office-365-to-help-prevent-spoofing.md)

- Para seus domínios primários, [use DKIM para validar emails de saída enviados do seu domínio personalizado no Office 365](use-dkim-to-validate-outbound-email.md)

- [Considere configurar registros do DMARC](use-dmarc-to-validate-email.md) para o seu domínio para determinar quem são seus remetentes legítimos

A Microsoft não fornece diretrizes de implementação detalhadas para cada SPF, DKIM e DMARC. No enTanto, há muitas informações publicadas online. Há também empresas de terceiros dedicadas para ajudar sua organização a configurar registros de autenticação de email.
  
### <a name="administrators-of-domains-that-are-not-office-365-customers"></a>Administradores de domínios que não são clientes do Office 365

Se você for um administrador de domínio, mas não for um cliente do Office 365:
  
- Você deve configurar o SPF para publicar os endereços IP de envio do seu domínio e também configurar o DKIM (se disponível) para assinar mensagens digitalmente. Você também pode considerar configurar registros do DMARC.

- Se você tiver remetentes em massa que transmitam emails em seu nome, você deve trabalhar com eles para enviar emails de forma que o domínio de envio no endereço de: (se ele pertencer a você) se alinhe com o domínio que passa SPF ou DMARC.

- Se você tiver servidores de email locais, ou enviar de um provedor de software como de serviço ou de um serviço de hospedagem na nuvem, como o Microsoft Azure, GoDaddy, Rackspace, serviços Web da Amazon ou similares, verifique se eles foram adicionados ao seu registro SPF.

- Se você for um domínio pequeno hospedado por um provedor de Internet, deverá configurar o registro SPF de acordo com as instruções fornecidas pelo provedor de Internet. A maioria dos ISPs fornece esses tipos de instruções e pode ser encontrada nas páginas de suporte da empresa.

- Mesmo que você não precise publicar registros de autenticação de email antes e funcionou bem, ainda deve publicar os registros de autenticação de email a serem enviados para a Microsoft. Fazendo isso, você está ajudando a lutar contra phishing e reduzindo a possibilidade de que você ou as organizações que você envia, serão enfeitas.

### <a name="what-if-you-dont-know-who-sends-email-as-your-domain"></a>E se você não souber quem envia emails como seu domínio?

Muitos domínios não publicam registros SPF porque não sabem quem todos os remetentes estão. Tudo bem, você não precisa saber quem são todos eles. Em vez disso, você deve começar publicando um registro SPF para aqueles que você conhece, especialmente onde o tráfego corporativo está localizado e publicar uma política SPF neutra,? All:
  
example.com em TXT "v = spf1 inclui include. example. com? All"
  
A política de SPF neutra significa que qualquer email que saia da infraestrutura corporativa transmitirá a autenticação de email em todos os outros receptores de email. Os emails provenientes de remetentes que você não conhece serão reproduzidos em neutro, o que é quase o mesmo que publicar nenhum registro SPF.
  
Ao enviar para o Office 365, os emails provenientes do seu tráfego corporativo serão marcados como autenticados, mas o email proveniente de fontes que você não sabe que ainda pode ser marcado como falso (dependendo se o Office 365 pode ou não ser autenticado implicitamente). No enTanto, ainda é uma melhoria de todos os emails que estão sendo marcados como falsificados pelo Office 365.
  
Depois de começar a usar um registro SPF com uma política de fallback de? tudo, você pode incluir mais e mais infraestrutura de envio e, em seguida, publicar uma política mais estrita. 
  
### <a name="what-if-you-are-the-owner-of-a-mailing-list"></a>E se você for o proprietário de uma lista de endereçamento?

Consulte a seção [cenários comuns de #2 de discussão](#common-scenario-2---discussion-lists).
  
### <a name="what-if-you-are-an-infrastructure-provider-such-as-an-internet-service-provider-isp-email-service-provider-esp-or-cloud-hosting-service"></a>E se você for um provedor de infra-estrutura, como um provedor de serviços de Internet (ISP), provedor de serviços de email (ESP) ou serviço de hospedagem na nuvem?

Se você hospedar o email de um domínio e ele enviar emails ou fornecer infraestrutura de hospedagem que possa enviar emails, faça o seguinte:
  
- Garantir que seus clientes tenham documentação detalhando o que publicar em seus registros SPF

- Considere assinar DKIM em email de saída, mesmo que o cliente não o configure explicitamente (assine com um domínio padrão). Você pode até assinar de forma dupla o email com assinaturas do DKIM (uma vez com o domínio do cliente, caso o tenha configurado e uma segunda vez com a assinatura do DKIM da sua empresa)

A entrega da Microsoft não é garantida, mesmo se você autenticar emails originários de sua plataforma, mas pelo menos ele garantirá que a Microsoft não envie lixo eletrônico por não ser autenticado. Para obter mais detalhes sobre como o Outlook.com filtra emails, consulte a [página postmaster do Outlook.com](https://postmaster.live.com/pm/postmaster.aspx).
  
Para obter mais detalhes sobre as práticas recomendadas de provedores de serviços, consulte [M3AAWG Mobile Messaging Best Practices for Service Providers](https://www.m3aawg.org/sites/default/files/M3AAWG-Mobile-Messaging-Best-Practices-Service-Providers-2015-08.pdf).
  
## <a name="frequently-asked-questions"></a>Perguntas Frequentes

### <a name="why-is-microsoft-making-this-change"></a>Por que a Microsoft está fazendo essa alteração?

Devido ao impacto de ataques de phishing, e como a autenticação de emails esteve por mais de 15 anos, a Microsoft acredita que o risco de continuar a permitir emails não autenticados é maior do que o risco de perder emails legítimos.
  
### <a name="will-this-change-cause-legitimate-email-to-be-marked-as-spam"></a>Essa alteração fará com que os emails legítimos sejam marcados como spam?

Em primeiro lugar, haverá algumas mensagens marcadas como spam. No enTanto, ao longo do tempo, os remetentes serão ajustados e a quantidade de mensagens intituladas informadamente como falsificada será insignificante para a maioria dos caminhos de email.
  
A própria Microsoft primeiro adotou este recurso várias semanas antes de implantá-lo para o restante de seus clientes. Enquanto houve interrupção no primeiro lugar, ela recusou gradualmente.
  
### <a name="will-microsoft-bring-this-feature-to-outlookcom-and-non-advanced-threat-protection-customers-of-office-365"></a>A Microsoft trará esse recurso para os clientes do Outlook.com e de proteção contra ameaças não avançados do Office 365?

A tecnologia antifalsificação da Microsoft foi inicialmente implantada em suas organizações que possuíam uma assinatura do Office 365 Enterprise E5 ou compraram o complemento do Office 365 Advanced Threat Protection (ATP) para sua assinatura. A partir de outubro de 2018, estendemos a proteção para organizações que também têm o Exchange Online Protection (EOP). No futuro, poderemos liberá-lo para o Outlook.com. No enTanto, se isso ocorrer, pode haver alguns recursos que não são aplicados, como relatórios e substituições personalizadas.
  
### <a name="how-can-i-report-spam-or-non-spam-messages-back-to-microsoft"></a>Como posso relatar spam ou mensagens que não são spam de volta para a Microsoft?

Você pode usar o [suplemento de mensagem de relatório para o Outlook](https://support.office.com/article/use-the-report-message-add-in-b5caa9f1-cdf3-4443-af8c-ff724ea719d2), ou se ele não estiver instalado, [enviar mensagens de spam, não spam e golpes de phishing para a Microsoft para análise](https://technet.microsoft.com/en-us/library/jj200769%28v=exchg.150%29.aspx).
  
### <a name="im-a-domain-administrator-who-doesnt-know-who-all-my-senders-are"></a>Sou um administrador de domínio que não sabe quem todos os meus remetentes estão!

Confira [os administradores de domínios que não são clientes do Office 365](#administrators-of-domains-that-are-not-office-365-customers).
  
### <a name="what-happens-if-i-disable-anti-spoofing-protection-for-my-organization-even-though-office-365-is-my-primary-filter"></a>O que acontece se eu desabilitar a proteção contra falsificação para minha organização, mesmo que o Office 365 seja meu filtro primário?

Não recomendamos isso, pois você ficará exposto a mensagens de phishing e spam perdidas. Nem todo phishing é falsificado, e nem todos os spoofs serão perdidos. No enTanto, o risco será maior do que um cliente que habilite a anti-falsificação.
  
### <a name="does-enabling-anti-spoofing-protection-mean-i-will-be-protected-from-all-phishing"></a>Habilitar a proteção contra falsificação significa que eu será protegido contra todos os phishing?

Infelizmente, não, como os phishers se adaptarão ao uso de outras técnicas, como contas comprometidas, ou a configuração de contas de serviços gratuitos. No enTanto, a proteção anti-phishing funciona muito melhor para detectar esses outros tipos de métodos de phishing, pois as camadas de proteção do Office 365 são projetadas juntas e se baseiam.
  
### <a name="do-other-large-email-receivers-block-unauthenticated-email"></a>Outros destinatários de email grandes bloqueiam emails não autenticados?

Quase todos os grandes receptores de emails implementam SPF, DKIM e DMARC tradicionais. Alguns receptores têm outras verificações que são mais estritas do que apenas esses padrões, mas poucos vão para o Office 365 bloquear emails não autenticados e tratá-los como falsificados. No enTanto, a maior parte do setor está se tornando cada vez mais estrita sobre esse tipo específico de email, particularmente por causa do problema de phishing.
  
### <a name="do-i-still-need-the-advanced-spam-filtering-option-enabled-for-spf-hard-fail-if-i-enable-anti-spoofing"></a>Ainda precisará da opção de filtragem de spam avançada habilitada para "falha de hardware SPF" se habilitar a antifalsificação?

Não, essa opção não é mais necessária porque o recurso antifalsificação não apenas considera a falha do SPF, mas um conjunto muito mais amplo de critérios. Se você tiver o antifalsificação habilitado e a opção de falha de hardware SPF habilitada, provavelmente receberá mais falsos positivos. Recomendamos desabilitar esse recurso, pois ele não forneceria quase nenhuma armadilha adicional para spam ou phishing e, em vez disso, geraria a maioria dos falsos positivos.
  
### <a name="does-sender-rewriting-scheme-srs-help-fix-forwarded-email"></a>A ajuda do esquema de reconfiguração do remetente (SRS) corrige emails encaminhados?

O SRS apenas corrige o problema de email encaminhado. Ao reescrever o email SMTP de, o SRS pode garantir que a mensagem encaminhada passe SPF no próximo destino. No enTanto, como a antifalsificação se baseia no endereço de: em combinação com o domínio de assinatura de email ou de DKIM (ou outros sinais), não é suficiente impedir que emails encaminhados sejam marcados como falsificados.
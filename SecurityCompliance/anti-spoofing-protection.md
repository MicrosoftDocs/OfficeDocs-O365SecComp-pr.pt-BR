---
title: Proteção antifalsificação no Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/06/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: d24bb387-c65d-486e-93e7-06a4f1a436c0
description: Este artigo descreve como Office 365 reduz contra ataques de phishing que usa falsificado domínios do remetente, ou seja, os domínios que são falsificados. Ele realiza isso analisando as mensagens e bloquear aqueles que podem ser autenticados neithe usando os métodos de autenticação de email padrão, nem outras técnicas de reputação do remetente. Essa alteração está sendo implementada para reduzir o número de ataques de phishing organizações no Office 365 estão expostas a.
ms.openlocfilehash: 95f4995b6447870700bc483f205ca3ff831045f5
ms.sourcegitcommit: 8c5a88433cff23c59b436260808cf3d91b06fdef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/07/2018
ms.locfileid: "27194712"
---
# <a name="anti-spoofing-protection-in-office-365"></a>Proteção antifalsificação no Office 365

Este artigo descreve como Office 365 reduz contra ataques de phishing que usa falsificado domínios do remetente, ou seja, os domínios que são falsificados. Ele realiza isso analisando as mensagens e bloqueando aqueles que não podem ser autenticados usando os métodos de autenticação de email padrão, nem outras técnicas de reputação do remetente. Essa alteração está sendo implementada para reduzir o número de ataques de phishing, os clientes estão expostos a.
  
Este artigo também descreve por que essa alteração está sendo feita, como os clientes podem se preparar para que essa alteração, como visualizar mensagens que serão afetadas, como a ser relatado nas mensagens, como reduzir os falsos positivos, bem como os remetentes à Microsoft devem se preparar para isso Altere.
  
A tecnologia da Microsoft antifalsificação inicialmente foi implantada para suas organizações que tinham uma assinatura do Office 365 Enterprise E5 ou comprou o complemento de proteção de ameaça avançadas (ATP) do Office 365 da assinatura deles. A partir de outubro de 2018, podemos estendi a proteção para as organizações que possuem o Exchange Online Protection (EOP) também. Além disso, por causa da maneira que todos nossos filtros Saiba uns dos outros, Outlook.com usuários também podem ser afetados.
  
## <a name="how-spoofing-is-used-in-phishing-attacks"></a>Como a falsificação é usada nos ataques de phishing

Quando se trata de proteger seus usuários, o Microsoft leva a ameaça de phishing sério. Uma das técnicas a remetentes de spam e phishers normalmente usam é a falsificação, que é quando o remetente é falsificado e uma mensagem parece ter vindo de alguém ou em algum lugar que não seja a origem real. Essa técnica é frequentemente usada em campanhas de phishing criadas para obter as credenciais do usuário. A tecnologia da Microsoft contra falsificação especificamente examina a falsificação do ' de: cabeçalho ' que é um nome que aparece em um cliente de email como o Outlook. Quando a Microsoft tem alta confiabilidade que From: cabeçalho é falsificado, ela identifica a mensagem como um falso.
  
Falsificação de mensagens tem duas implicações negativas para usuários da vida real:
  
### <a name="1-spoofed-messages-deceive-users"></a>1. falsificadas mensagens levando usuários
  
Primeiro, uma mensagem falsificada pode fazer o usuário clicar em um link e abandonada suas credenciais, baixando malware ou responder uma mensagem com conteúdo confidencial (o último é conhecido como comprometimento de Email comercial). Por exemplo, este é uma mensagem de phishing com um remetente falsificado da msoutlook94@service.outlook.com:
  
![Mensagem de phishing representando service.outlook.com](media/1a441f21-8ef7-41c7-90c0-847272dc5350.jpg)
  
Acima na verdade não provém da service.outlook.com, mas em vez disso, foi falsificadas pelo phisher torná-lo a aparência que tinha. Ele está tentando fazer o usuário clicar no link dentro da mensagem.
  
O próximo exemplo é falsificação contoso.com:
  
![Mensagem de phishing - comprometimento de email comercial](media/da15adaa-708b-4e73-8165-482fc9182090.jpg)
  
A mensagem parece legítima, mas é na verdade um falso. Essa mensagem de phishing é um tipo de comprometimento de Email de negócios que é uma subcategoria de phishing.
    
### <a name="2-users-confuse-real-messages-for-fake-ones"></a>2. usuários confunda mensagens reais para aqueles falsas
  
Segunda, falsificadas mensagens criar incerteza para usuários que saber sobre mensagens de phishing, mas não pode determinar a diferença entre uma mensagem real e um falsificados. Por exemplo, este é um exemplo de uma senha real redefinido a partir do endereço de email do Microsoft Security conta:
  
![Redefinição de senha legítimo do Microsoft](media/58a3154f-e83d-4f86-bcfe-ae9e8c87bd37.jpg)
  
A mensagem acima provém da Microsoft, mas ao mesmo tempo, os usuários são usados para obtenção de mensagens de phishing que pode fazer com que um usuário clicar em um link e abandonada suas credenciais, baixando malware ou responder a uma mensagem com conteúdo confidencial. Como é difícil dizer a diferença entre uma redefinição de senha real e um falso, muitos usuários ignoram essas mensagens, indicá-las como spam ou desnecessariamente indicá as mensagens de volta para a Microsoft como golpes de phishing perdidas.
    
Para interromper a falsificação, o setor de filtragem de email desenvolveu protocolos de autenticação de email como [SPF](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing), [DKIM](https://docs.microsoft.com/office365/SecurityCompliance/use-dkim-to-validate-outbound-email)e [DMARC](https://docs.microsoft.com/office365/SecurityCompliance/use-dmarc-to-validate-email). DMARC impede a falsificação examinando o remetente da mensagem - aquele que o usuário vê em seu cliente de email (nos exemplos acima, isto é service.outlook.com, outlook.com e accountprotection.microsoft.com) - com o domínio que transmita SPF ou DKIM. Ou seja, o domínio que o usuário vê tiverem sido autenticado e, portanto, não falsificado. Para obter uma discussão mais completa, consulte a seção "*Noções básicas sobre por que a autenticação de email nem sempre é suficiente para interromper a falsificação"* posteriormente contidas neste documento. 
  
No entanto, o problema é que a autenticação de email registros são opcionais, não é necessário. Portanto, enquanto os domínios com políticas de autenticação forte like microsoft.com e skype.com estão protegidos contra falsificação, domínios que publicar as políticas de autenticação mais fracas ou nenhuma diretiva nisso, são alvos de sendo falsificado. A partir de março de 2018, somente 9% dos domínios das empresas da Fortune 500 publicar as políticas de autenticação de alta segurança de email. O restante 91% pode ser falsificado pelo phisher e, a menos que o filtro de email detecta-lo usando a diretiva de outra, pode ser entregue a um usuário final e levando-las:
  
![Políticas DMARC de empresas da Fortune 500](media/84e77d34-2073-4a8e-9f39-f109b32d06df.jpg)
  
A proporção de empresas de pequeno a médio porte que não estão na Fortune 500 que publicar as políticas de autenticação forte email é menor e menor ainda para domínios que estão fora da América do Norte e Europa Ocidental.
  
Este é um grande problema porque enquanto as empresas podem não estar cientes de como funciona a autenticação de email, phishers entender e tirar proveito da falta de-lo.
  
Para obter informações sobre como configurar o SPF, DKIM e DMARC, consulte a seção "*os clientes do Office 365"* mais adiante neste documento. 
  
## <a name="stopping-spoofing-with-implicit-email-authentication"></a>Parando falsificação com a autenticação de email implícita

Porque phishing phishing e lança tal um problema e devido a adoção limitada de políticas de autenticação forte email, o Microsoft continua a investir em recursos, para proteger seus clientes. Portanto, Microsoft está se movendo com antecedência com a *autenticação de email implícita* - se um domínio não autenticados, Microsoft irá tratá-lo como se tivesse publicado registros de autenticação de e-mail e tratá-lo adequadamente, se ele não passa. 
  
Para realizar isso, a Microsoft criou inúmeras extensões para a autenticação de email regular incluindo reputação do remetente, histórico de remetente/destinatário, análise de comportamento e outras técnicas avançadas. Uma mensagem enviada de um domínio que não publica autenticação de email será marcada como falso, a menos que ele contém outros sinaliza para indicar que ela está legítima.
  
Fazendo isso, end, os usuários podem ter confiança que não tenha sido falsificado um email enviado a ele, remetentes podem ter certo que ninguém está representando o seu domínio e os clientes do Office 365 podem oferecer proteção ainda melhor como proteção de representação.
  
Para ver o lançamento de geral da Microsoft, consulte [A Sea de Phish parte 2 - Enhanced Antifalsificação no Office 365](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Schooling-A-Sea-of-Phish-Part-2-Enhanced-Anti-spoofing/ba-p/176209).
  
## <a name="identifying-that-a-message-is-classified-as-spoofed"></a>Identificação que uma mensagem é classificada como falsificado

### <a name="composite-authentication"></a>Autenticação de composição

Embora SPF, DKIM e DMARC sejam úteis tudo sozinhos, elas não se comunicar suficiente status de autenticação no caso de uma mensagem não possui autenticação explícita registros. Portanto, a Microsoft desenvolveu um algoritmo que combina os sinais de vários em um único valor chamado autenticação composição ou compauth para short. Os clientes no Office 365 têm valores compauth cortados no cabeçalho de *Autenticação resultados* nos cabeçalhos da mensagem. 
  
```
Authentication-Results:
  compauth=<fail|pass|softpass|none> reason=<yyy>

```

|**Resultado de CompAuth**|**Descrição**|
|:-----|:-----|
|falhar|Mensagem falhou explícitas de autenticação (Enviar domínio publicado registros explicitamente no DNS) ou autenticação implícita (envio domínio não publicou registros no DNS, para o Office 365 interpolados o resultado como se tivesse publicado registros).|
|passar|Mensagem passada explícitas de autenticação (mensagem passado DMARC ou [Adivinhar recomendadas passadas DMARC](https://blogs.msdn.microsoft.com/tzink/2015/05/06/what-is-dmarc-bestguesspass-in-office-365)) ou autenticação implícita com alta confiabilidade (enviando o domínio não publicar os registros de autenticação de e-mail, mas o Office 365 tem sinais de back-end forte para indicar que a mensagem é provável legítimo).|
|softpass|Mensagem passada autenticação implícita com confiança baixa e médio (enviando o domínio não publicar a autenticação de email, mas o Office 365 tem sinais de back-end para indicar a mensagem é legítima, mas a intensidade do sinal é mais fraca).|
|nenhum|Mensagem não autenticou (ou autenticar, mas não alinha), mas não são aplicada devido a reputação do remetente ou outros fatores de autenticação composta.|
   
|||
|:-----|:-----|
|**Motivo**|**Descrição**|
|0XX|Mensagem de falha na autenticação composta.<br/>**000** significa que a mensagem falhou DMARC com uma ação de rejeição ou quarentena.                    -001 significa que a mensagem de falha na autenticação de email implícita. Isso significa que o domínio de envio não tinha registros de autenticação de e-mail publicados ou se eles fizeram, que tinham uma política de falha mais fraca (fail suave de SPF ou neutro, política DMARC de p = none).<br/>**002** significa que a organização possui uma política para o par de remetente/domínio proibido explicitamente enviem email falsificado, essa configuração é definir manualmente por um administrador.  <br/>**010** significa a mensagem falhou DMARC com uma ação de rejeição ou quarentena e o domínio de envio é um dos domínios aceitos da sua organização (Isso é parte de auto-to-self ou interna da organização, falsificação).  <br/>**011** significa que a mensagem de falha na autenticação de email implícita, e o domínio de envio é um dos domínios aceitos de sua organização (Isso é parte de auto-to-self ou interna da organização, falsificação).|
|Todos os outros códigos (1xx, 2xx, 3xx, 4xx, 5xx)|Corresponde à diversos códigos internos para o motivo pelo qual uma mensagem passadas autenticação implícita ou não tinha nenhuma autenticação, mas nenhuma ação foi aplicada.|
   
Examinando os cabeçalhos de uma mensagem, um administrador ou até mesmo um usuário final pode determinar como o Office 365 chega na conclusão que o remetente pode ser falsificado.
  
### <a name="differentiating-between-different-types-of-spoofing"></a>Distinguir entre tipos diferentes de falsificação

Microsoft faz distinção entre dois tipos diferentes de falsificação de mensagens:
  
 **Falsificação de interna da organização**
  
Também conhecido como falsificação self-to-self, isso ocorre quando o domínio no campo From: endereço são os mesmos, ou se alinha com, o domínio do destinatário (quando o domínio do destinatário é um dos [Domínios aceitos](https://technet.microsoft.com/en-us/library/jj945194%28v=exchg.150%29.aspx)de sua organização); ou, quando o domínio no campo From: endereço é parte da mesma organização.
  
Por exemplo, o seguinte tem remetente e destinatário do mesmo domínio (contoso.com). Espaços são inseridos no endereço de email para evitar a coleta de spambot nesta página):
  
De: remetente @ contoso.com
  
Para: destinatário @ contoso.com
  
O exemplo a seguir possui os domínios de remetente e destinatário alinhando com o domínio organizacional (fabrikam.com):
  
De: remetente @ foo.fabrikam.com
  
Para: destinatário @ bar.fabrikam.com
  
Os seguintes domínios de remetente e destinatário são diferentes (microsoft.com e bing.com), mas eles pertencem à mesma organização (ou seja, ambos fazem parte de domínios aceitos da organização):
  
De: remetente @ microsoft.com
  
Para: destinatário @ bing.com
  
Mensagens que falham interna da organização falsificação contêm os seguintes valores nos cabeçalhos:
  
X-Forefront-Antispam-Report: … CAT:SPM/HSPM/PHSH; … SFTY:9.11
  
O gato está a categoria da mensagem e ela normalmente é marcada como SPM (spam), mas ocasionalmente podem ser HSPM (spam de alta confiabilidade) ou de PHISHING (phishing) dependendo das quais outros tipos de padrões ocorrer na mensagem.
  
O SFTY é o nível de segurança da mensagem, os meios de dígito (9) primeiro a mensagem é phishing e segundo conjunto de dígitos após o ponto (11) significa que ele é falsificação interna da organização.
  
Não há nenhum código de razão específica para autenticação composto de falsificação, interna da organização que receberá o carimbo / posteriormente no 2018 (cronograma ainda não foi definida).
  
 **Falsificação entre domínios**
  
Isso ocorre quando o domínio de envio no campo From: endereço é um domínio externo para a organização de recebimento. Mensagens que falham autenticação composto devido a falsificação entre domínios contêm os seguintes valores nos cabeçalhos:
  
Resultados de autenticação: … compauth = fail motivo = 000/001
  
X-Forefront-Antispam-Report: … CAT:SPOOF; … SFTY:9.22
  
Em ambos os casos, a seguinte dica safety vermelho é marcada na mensagem ou um equivalente que é personalizado para o idioma do destinatário da caixa de correio:
  
![Dica de segurança vermelho - detecção de fraude](media/a366156a-14e8-4c14-bfe5-2031b21936f8.jpg)
  
É apenas examinando From: de endereços e saber qual é o seu email do destinatário ou por inspecionando os cabeçalhos de email que você pode diferenciar entre interna da organização e entre domínios falsificação.
  
## <a name="how-customers-of-office-365-can-prepare-themselves-for-the-new-anti-spoofing-protection"></a>Como os clientes do Office 365 podem preparar sozinhos para a nova proteção antifalsificação

### <a name="information-for-administrators"></a>Informações para administradores

Como administrador de uma organização no Office 365, existem várias partes importantes de informações que você deve estar ciente.
  
### <a name="understanding-why-email-authentication-is-not-always-enough-to-stop-spoofing"></a>Noções básicas sobre por que a autenticação de email nem sempre é suficiente para interromper a falsificação

A nova proteção antifalsificação depende da autenticação de email (SPF, DKIM e DMARC) não marcar uma mensagem como falsificação. Um exemplo comum é quando um domínio de envio nunca tiver publicado registros SPF. Se não houver nenhum registro SPF ou eles estão configurados incorretamente, uma mensagem enviada será marcada como falsificado, a menos que a Microsoft possui inteligência de dados de back-end que diz que a mensagem é legítima.
  
Por exemplo, antes da antifalsificação que está sendo implantado, uma mensagem pode ter sido parecidas com as seguintes com nenhum registro SPF, nenhum registro de verificação e nenhum registro DMARC: 
  
```
Authentication-Results: spf=none (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; contoso.com; dkim=none
  (message not signed) header.d=none; contoso.com; dmarc=none
  action=none header.from=example.com;
From: sender @ example.com
To: receiver @ contoso.com
```
Após antifalsificação, se você tiver o Office 365 Enterprise E5, EOP ou ATP, o valor de compauth é marcado:
  
```
Authentication-Results: spf=none (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; contoso.com; dkim=none
  (message not signed) header.d=none; contoso.com; dmarc=none
  action=none header.from=example.com; compauth=fail reason=001
From: sender @ example.com
To: receiver @ contoso.com

```

Se example.com fixo isso, configurando um registro SPF, mas não é um registro de verificação, isso seria passar na autenticação composta porque o domínio que passado SPF alinhado com o domínio no campo From: endereço: 
  
```
Authentication-Results: spf=pass (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; contoso.com; dkim=none
  (message not signed) header.d=none; contoso.com; dmarc=bestguesspass
  action=none header.from=example.com; compauth=pass reason=109
From: sender @ example.com
To: receiver @ contoso.com
```

Ou, se eles configurarem um registro de verificação, mas não um registro SPF, isso também seria passar na autenticação composta porque o domínio em que a assinatura de verificação que passado alinhado com o domínio no campo From: endereço: 
  
```
Authentication-Results: spf=none (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; contoso.com; dkim=pass
  (signature was verified) header.d=outbound.example.com;
  contoso.com; dmarc=bestguesspass action=none
  header.from=example.com; compauth=pass reason=109
From: sender @ example.com
To: receiver @ contoso.com
```

No entanto, um phisher pode também configurar SPF e DKIM e assinar uma mensagem com seu próprio domínio, mas especificar um domínio diferente no campo From: endereço. Nem SPF nem DKIM requer o domínio para alinhar com o domínio no campo From: endereço, portanto, a menos que example.com publicado registros DMARC, isso não pode ser marcado como um falso usando DMARC: 
  
```
Authentication-Results: spf=pass (sender IP is 5.6.7.8)
  smtp.mailfrom=maliciousDomain.com; contoso.com; dkim=pass
  (signature was verified) header.d=maliciousDomain.com;
  contoso.com; dmarc=none action=none header.from=example.com;
From: sender @ example.com
To: receiver @ contoso.com
```

No cliente de email (Outlook, Outlook na web, ou qualquer outro cliente de email), somente From: domínio é exibido, não o domínio em SPF ou DKIM e que pode levar o usuário a pensar a mensagem tiver vindo de example.com, mas na verdade vêm da maliciousDomain.com .
  
![Mensagem autenticada mas do: domínio não se alinha com o que passado SPF ou DKIM](media/a9b5ab2a-dfd3-47c6-8ee8-e3dab2fae528.jpg)
  
Por esse motivo, o Office 365 exige que o domínio no campo From: endereço se alinha com o domínio em que a assinatura SPF ou DKIM, e se ele não estiver, contém alguns outros sinais internos que indica que a mensagem é legítima. Caso contrário, a mensagem seria um fail compauth. 
  
```
Authentication-Results: spf=none (sender IP is 5.6.7.8)
  smtp.mailfrom=maliciousDomain.com; contoso.com; dkim=pass
  (signature was verified) header.d=maliciousDomain.com;
  contoso.com; dmarc=none action=none header.from=contoso.com;
  compauth=fail reason=001
From: sender@contoso.com
To: someone@example.com
```

Assim, Office 365 antifalsificação protege contra domínios sem autenticação e os domínios que configurar a autenticação, mas incompatibilidade em relação ao domínio no campo From: endereços como isto é aquele que o usuário vê e acredita que são o remetente da mensagem. Isso é verdadeiro dois domínios externos à sua organização, bem como os domínios na sua organização.
  
Portanto, se você precisar receber uma mensagem que falhou na autenticação composta e marcada como falsificado, mesmo que a mensagem passou SPF e DKIM, é porque o domínio que passado SPF e DKIM não estão alinhados com o domínio no campo From: endereço.
  
### <a name="understanding-changes-in-how-spoofed-emails-are-treated"></a>Compreensão das mudanças em emails falsificados como é tratado

Atualmente, todas as organizações no Office 365 - ATP e não-ATP - mensagens que falharem DMARC com uma política de rejeição ou quarentena são marcadas como spam e geralmente levam a ação de spam de alta confiabilidade ou em alguns casos, a ação de spam regular (dependendo se outros spam regras primeiro identificá-lo como spam). Detecções de falsificação interna da organização executar a ação de spam regular. Esse comportamento não precisa estar habilitado, nem podem estar desabilitada.
  
No entanto, para mensagens de falsificação entre domínios, antes que esta alteração eles seriam passar regulares verificações de malware, spam e phishing e se outras partes do filtro identificado-las como suspeito, seriam marcá-las como spam, phishing ou malware respectivamente. Com a nova domínio cruzado proteção contra falsificação, qualquer mensagem que não pode ser autenticada, por padrão, executará a ação definida no antiphishing \> falsificação e política. Se uma não estiver definida, ele será movido para uma pasta de lixo eletrônico de usuários. Em alguns casos, mensagens suspeitas mais também terão a dica de vermelho safety adicionada à mensagem.
  
Isso pode resultar em algumas mensagens que foram marcadas anteriormente como sendo marcados como spam, mas agora também terão uma dica safety vermelho; de spam em outros casos, as mensagens que foram marcadas anteriormente como não spam iniciará sendo marcados como spam (CAT:SPOOF) com uma dica de vermelho safety adicionado. Ainda em outros casos, os clientes que foram mover todos spam e phishing, para a quarentena seriam agora vê-los indo para a pasta Lixo eletrônico (esse comportamento pode ser alterado, consulte [alterando as configurações de antifalsificação](#changing-your-anti-spoofing-settings)).
  
Há várias maneiras diferentes de que uma mensagem pode ser falsificada (consulte [Differentiating entre tipos diferentes de falsificação](#differentiating-between-different-types-of-spoofing) anteriormente neste artigo), mas a partir de março de 2018 a maneira como o Office 365 trata as mensagens não é unificada ainda. A tabela a seguir está um resumo rápido, com a proteção de falsificação entre domínios sendo novo comportamento: 
  
|**Tipo de falsificação**|**Categoria**|**Dica de segurança adicionada?**|**Aplica-se a**|
|:-----|:-----|:-----|:-----|
|Falha DMARC (quarentena ou rejeitar)  <br/> |HSPM (padrão), também podem ser SPM ou PHSH  <br/> |Não (ainda não)  <br/> |Todos os clientes do Office 365, Outlook.com  <br/> |
|Auto-to-self  <br/> |SPM  <br/> |Sim  <br/> |Todas as organizações do Office 365, Outlook.com  <br/> |
|Entre domínios  <br/> |REALIZAR A FALSIFICAÇÃO  <br/> |Sim  <br/> |Clientes do Office 365 avançadas Threat Protection e E5  <br/> |
   
### <a name="changing-your-anti-spoofing-settings"></a>Alterar as configurações de antifalsificação

Para criar ou atualizar suas configurações de antifalsificação (entre domínios), navegue até o antiphishing \> Anti-Falsificação configurações sob o gerenciamento de ameaça \> guia política na segurança &amp; Centro de conformidade. Se você nunca criou quaisquer definições de AntiPhishing, você precisará criar um:
  
![Antiphishing - criar uma nova política](media/9337ec91-270e-4fa7-9dfa-a51a2d1eb95e.jpg)
  
Se você já criou uma, você pode selecionar para modificá-la:
  
![Antiphishing - modificar política existente](media/75457a7c-882e-4984-80d1-21a12b42c53a.jpg)
  
Selecione a política que você acabou de criar e prossiga pelas etapas, conforme descrito em [Saiba mais sobre falsificação da inteligência.](https://support.office.com/article/Learn-more-about-spoof-intelligence-978c3173-3578-4286-aaf4-8a10951978bf)
  
![Habilitar ou desabilitar antispoofing](media/c49e2147-c954-443c-9144-1cbd139e1166.jpg)
  
![Ativar ou desativar dicas de segurança antispoofing](media/eec7c407-31fc-4f73-8325-307d82d1fb53.jpg)
  
Para criar uma nova política por meio do PowerShell: 
  
```
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

Você pode modificar os parâmetros de política de AntiPhishing usando o PowerShell, seguindo a documentação em [Set-AntiphishPolicy](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/Set-AntiPhishPolicy?view=exchange-ps). Você pode especificar o $name como um parâmetro:
  
```
Set-AntiphishPolicy -Identity $name <fill in rest of parameters>
```

Posteriormente nesta 2018, em vez de você ter que criar uma política padrão, um será criado para que o escopo é definido para todos os destinatários na sua organização para que você não precisa especificá-lo manualmente (as capturas de tela a seguir estão sujeitos a alterações antes da implementação do final).
  
![Política padrão para Antiphishing](media/1f27a0bf-e202-4e12-bbac-24baf013c8f9.jpg)
  
Ao contrário de uma política que você criar, você não pode excluir a política padrão, modificar sua prioridade ou escolha quais usuários, domínios ou grupos de fazer o escopo que ele.
  
![Detalhes da política padrão AntiPhishing](media/30c21ceb-df52-4c93-aa65-f44a55dc1009.jpg)
  
Para configurar sua proteção padrão por meio do PowerShell:
  
```
$defaultAntiphishPolicy = Get-AntiphishPolicy | ? {$_.IsDefault -eq $true}
Set-AntiphishPolicy -Identity $defaultAntiphishPolicy.Name -EnableAntispoofEnforcement <$true|$false>
```

Você deve desativar proteção antifalsificação somente se você tiver servidores na frente do Office 365 ou outro servidor de email (consulte legítimos cenários para desabilitar antifalsificação para obter mais detalhes). 
  
```
$defaultAntiphishPolicy = Get-AntiphishiPolicy | ? {$_.IsDefault $true}
Set-AntiphishPolicy -Identity $defaultAntiphishPolicy.Name -EnableAntispoofEnforcement $false 

```
> [!IMPORTANT]
> Se o primeiro salto no seu caminho de email é o Office 365 e você estiver recebendo muitos emails legítimos marcadas como falso, você primeiro deve configurar o seus remetentes que têm permissão para enviar email falsificado ao seu domínio (consulte a seção *"Managing remetentes legítimos que está enviando u email nauthenticated"* ). Se você ainda estiver recebendo muitos falsos positivos (por exemplo, legítimos mensagens marcadas como falso), não é recomendável desabilitar proteção antifalsificação todo. Em vez disso, é recomendável escolhendo básica em vez de proteção alta.                    É melhor funcionem por meio de falsos positivos que à expor sua organização para emails falsificados que poderia acabar impondo significativamente maiores custos no longo prazo.

### <a name="managing-legitimate-senders-who-are-sending-unauthenticated-email"></a>Gerenciando remetentes legítimos que estão enviando email não-autenticado

O Office 365 rastreia de quem está enviando email não-autenticado para sua organização. Se o serviço pensa que o remetente não é legítimo, ele será marcá-la como uma falha de *compauth* . Isso será classificado como realizar a FALSIFICAÇÃO embora ela depende da sua política antifalsificação que foi aplicada à mensagem. 
  
No entanto, como um administrador, você pode especificar quais remetentes têm permissão para enviar e-mail falsificado, substituindo decisão do Office 365.
  
**Método 1 - se a sua organização possui o domínio, configurar a autenticação de email**
  
Este método pode ser usado para resolver falsificação interna da organização e entre domínios falsificação em casos em que você possui ou interagir com vários locatários. Isso também ajuda a resolver entre domínios falsificação onde você enviar a outros clientes no Office 365 e também terceiros que são hospedados em outros provedores.
  
Para obter mais detalhes, consulte [os clientes do Office 365](#customers-of-office-365). 
 
**Método 2 - inteligência de falsificação de uso para configurar permitidos remetentes de email não-autenticado**
  
Você também pode usar a [Falsificação da inteligência de dados](https://support.office.com/article/Learn-more-about-spoof-intelligence-978c3173-3578-4286-aaf4-8a10951978bf) para permitir que os remetentes para transmitir mensagens não autenticadas para sua organização. 
  
Domínios externos, o usuário falsificado é o domínio no endereço de, enquanto a infra-estrutura de envio é o endereço IP envio (dividida em /24 intervalos CIDR), ou no domínio organizacional do registro PTR (a captura de tela abaixo, o IP de envio pode ser 131.107.18.4 cujo registro PTR é outbound.mail.protection.outlook.com, e isso seria exibido como outlook.com para a infra-estrutura de envio).
  
Para permitir que esse remetente para enviar email não-autenticado, altere **não** para um **Sim**.
  
![Configurando antispoofing remetentes permitido](media/d4334921-d820-4334-8217-788279701e94.jpg)
  
Você também pode usar o PowerShell para permitir que o remetente específico falsificar o seu domínio: 
  
```
$file = "C:\My Documents\Summary Spoofed Internal Domains and Senders.csv"
```

```
Get-PhishFilterPolicy -Detailed -SpoofAllowBlockList -SpoofType External | Export-CSV $file
```

![Obtendo remetentes falsificados via Powershell](media/0e27ffcf-a5db-4c43-a19b-fa62326d5118.jpg)
  
Na imagem anterior, quebras de linha adicionais foram adicionadas tornar esta captura de tela cabem, mas na realidade todos os valores apareceria em uma única linha.
  
Edite o arquivo e procure a linha que corresponde ao outlook.com e bing.com e altere a entrada de AllowedToSpoof de não para Sim:
  
![Permitir a falsificação da configuração como Sim, por meio do Powershell](media/62340452-62d3-4958-9ce9-afe5275a870d.jpg)
  
Salve o arquivo e, em seguida, execute: 
  
```
$UpdateSpoofedSenders = Get-Content -Raw "C:\My Documents\Spoofed Senders.csv"
Set-PhishFilterPolicy -Identity Default -SpoofAllowBlockList $UpdateSpoofedSenders
```

Isso permitirá que agora bing.com enviar email não-autenticado do \*. outlook.com.

**Método 3: criar uma entrada de permissões para o par de remetente/destinatário**
  
Você também pode optar por ignorar todos os filtragem de spam para um determinado remetente. Para obter mais detalhes, consulte [como adicionar forma segura um remetente a uma lista de permissões no Office 365](https://blogs.msdn.microsoft.com/tzink/2017/11/29/how-to-securely-add-a-sender-to-an-allow-list-in-office-365/).
  
Se você usar esse método, ele irá ignorar spam e algumas da filtragem de phishing, mas não a filtragem de malware.
  
**Método 4 - entre em contato com o remetente e pedir-lhe que configurar a autenticação de email**
  
Por causa do problema de spam e phishing, a Microsoft recomenda configurar a autenticação de email de todos os remetentes. Se você souber que um administrador do domínio envio, contate-los e solicitar que eles configurarem registros de autenticação de e-mail para que você não precisa adicionar qualquer substituições. Para obter mais informações, consulte [os administradores de domínios que são não os clientes do Office 365](#administrators-of-domains-that-are-not-office-365-customers)"mais adiante neste artigo. 
  
Enquanto pode ser difícil em primeiro a obter enviando domínios para autenticar, ao longo do tempo, quanto mais filtros de e-mail Iniciar junking ou até mesmo rejeitando seus emails, fará com que-los para configurar os registros adequados para garantir a entrega de melhor.
  
### <a name="viewing-reports-of-how-many-messages-were-marked-as-spoofed"></a>Exibindo relatórios sobre quantas mensagens foram marcadas como falsificado

Quando sua política antifalsificação estiver habilitada, você pode usar a inteligência de ameaça para obter os números em torno de quantas mensagens marcadas como phishing. Para fazer isso, vá para a segurança &amp; Centro de conformidade (SCC) em gerenciamento de ameaça \> Explorer, defina o modo de exibição como phishing e grupo por domínio do remetente ou Status de proteção:
  
![Exibindo quantas mensagens marcadas como phishing](media/de25009a-44d4-4c5f-94ba-9c75cd9c64b3.jpg)
  
Você pode interagir com os diversos relatórios para ver quantos foram marcados como phishing, incluindo mensagens marcadas como falso. Para saber mais, consulte [Introdução ao Office 365 Threat Intelligence](https://support.office.com/article/get-started-with-office-365-threat-intelligence-38e9b67f-d188-490f-bc91-a1ae4b270441).
  
Você ainda não pode dividir temporária que as mensagens foram marcadas devido a falsificação versus outros tipos de phishing (phishing geral, domínio ou usuário representação e assim por diante). No entanto, mais adiante no 2018, você poderá fazer isso por meio de segurança &amp; Centro de conformidade. Depois que você fizer isso, você pode usar este relatório como um ponto de partida para identificar os domínios de envio que podem ser legítimos que estão sendo marcados como falso devido à falha na autenticação.
  
A captura de tela a seguir é uma proposta de como esses dados terá a aparência, mas podem ser alteradas quando lançado:
  
![Visualizando relatórios de phishing por tipo de detecção](media/dd25d63f-152c-4c55-a07b-184ecda2de81.jpg)
  
Para clientes de E5 e de não-ATP, esses relatórios estarão disponíveis posteriormente no 2018 sob os relatórios de Status de proteção de ameaça (TPS), mas serão atrasados pelo menos 24 horas. Esta página será atualizada à medida que eles são integrados a segurança &amp; Centro de conformidade.
  
### <a name="predicting-how-many-messages-will-be-marked-as-spoof"></a>Prevendo quantas mensagens serão marcadas como falso

Mais tarde no 2018, uma vez o Office 365 atualiza suas configurações para permitir que você desative a imposição antifalsificação ou em com a imposição básica ou alta, você receberá a capacidade de ver como a disposição de mensagem será alterado em várias configurações. Ou seja, se antifalsificação estiver desativado, você poderá ver quantas mensagens serão detectadas como falso se você ativar o Basic; ou, se ele for Basic, você poderá ver quantas mensagens mais serão detectadas como falso se ativá-lo como alto.
  
Esse recurso está atualmente em desenvolvimento. Como obter mais detalhes são definidos, esta página será atualizada com capturas de tela do Centro de conformidade de segurança e e com exemplos do PowerShell.
  
!["E se" relatório para habilitar antispoofing](media/fdd085ae-02c1-4327-a063-bfe9a32ff1eb.jpg)
  
![Eu possível para permitir que um remetente falsificado](media/53f9f73e-fb01-47f3-9a6d-850c1aef5efe.jpg)
  
### <a name="understanding-how-spam-phishing-and-advanced-phishing-detections-are-combined"></a>Noções básicas sobre como spam, phishing e phishing avançadas detecções são combinadas

Organizações que usam o Exchange Online, com ou sem ATP, podem especificar quais ações tomar quando o serviço identifica mensagens como malware, spam, phishing, spam de alta confiabilidade e em massa. Com as políticas de AntiPhishing ATP para clientes ATP e as políticas de AntiPhishing para clientes do EOP e o fato de que uma mensagem pode alcance vários tipos de detecção (por exemplo, malware, phishing e representação de usuário), pode haver alguma confusão sobre qual política se aplica. 
  
Em geral, a diretiva aplicada a uma mensagem é identificada no cabeçalho X-Forefront-Antispam-Report na propriedade CAT (categoria). 
  
|**Prioridade**|**Política**|**Categoria**|**Onde gerenciadas?**|**Aplica-se a**|
|:-----|:-----|:-----|:-----|:-----|
|1   <br/> |Malware  <br/> |MALW  <br/> |[Política de malware](https://technet.microsoft.com/en-us/library/jj200745%28v=exchg.150%29.aspx) <br/> |Todas as organizações  <br/> |
|2   <br/> |Phishing  <br/> |PHSH  <br/> |[Política de filtro de conteúdo hospedado](https://technet.microsoft.com/library/jj200684%28v=exchg.150%29.aspx) <br/> |Todas as organizações  <br/> |
|3   <br/> |Spam de alta confiança  <br/> |HSPM  <br/> |[Política de filtro de conteúdo hospedado](https://technet.microsoft.com/library/jj200684%28v=exchg.150%29.aspx) <br/> |Todas as organizações  <br/> |
|4   <br/> |Falsificação  <br/> |REALIZAR A FALSIFICAÇÃO  <br/> |[Política de AntiPhishing](https://go.microsoft.com/fwlink/?linkid=864553), [inteligência de falsificação](https://support.office.com/article/Learn-more-about-spoof-intelligence-978c3173-3578-4286-aaf4-8a10951978bf) <br/> |Todas as organizações  <br/> |
|5   <br/> |Spam  <br/> |SPM  <br/> |[Política de filtro de conteúdo hospedado](https://technet.microsoft.com/library/jj200684%28v=exchg.150%29.aspx) <br/> |Todas as organizações  <br/> |
|6   <br/> |Em massa  <br/> |EM MASSA  <br/> |[Política de filtro de conteúdo hospedado](https://technet.microsoft.com/library/jj200684%28v=exchg.150%29.aspx) <br/> |Todas as organizações  <br/> |
|7   <br/> |Representação de domínio  <br/> |DIMP  <br/> |[Política de AntiPhishing](https://go.microsoft.com/fwlink/?linkid=864553) <br/> |Organizações com ATP  <br/> |
|8   <br/> |Representação de usuário  <br/> |UIMP  <br/> |[Política de AntiPhishing](https://go.microsoft.com/fwlink/?linkid=864553) <br/> |Organizações com ATP <br/> |
   
Se você tiver vários diferentes políticas AntiPhishing, aquele com a prioridade mais alta serão aplicadas. Por exemplo, suponha que você tem duas políticas:
  
|**Política**|**Prioridade**|**Representação de domínio do usuário**|**Antifalsificação**|
|:-----|:-----|:-----|:-----|
|A  <br/> |1   <br/> |Ativado  <br/> |Desativado  <br/> |
|B  <br/> |2   <br/> |Desligado  <br/> |Em  <br/> |
   
Se uma mensagem entra em ação e é identificada como representação de falsificação e o usuário e o mesmo conjunto de usuários destinado a política A e B de política, e em seguida, a mensagem é tratada como um falso mas nenhuma ação é aplicada desde e falsificação está desativado , e realizar a FALSIFICAÇÃO é executado em uma prioridade maior (4) que a representação de usuário (8).
  
Para tornar os outros tipos de phishing aplicar diretiva, você precisará ajustar as configurações de quem as várias políticas são aplicadas.
  
### <a name="legitimate-scenarios-to-disable-anti-spoofing"></a>Cenários legítimos para desabilitar antifalsificação

Melhor antifalsificação protege os clientes contra ataques de phishing e, portanto, não é recomendável desabilitar proteção antifalsificação. Desativando o recurso, você pode resolver alguns falsos positivos curto prazo, mas você será exposto a mais de risco de longo prazo. O custo de configuração de autenticação no lado do remetente ou fazer ajustes nas políticas de phishing, são geralmente ocasionais eventos ou exigem somente mínima, periódica de manutenção. No entanto, o custo para recuperar de um ataque de phishing onde dados foi expostos ou ativos têm sido comprometida é muito maior.
  
Por esse motivo, é melhor funciona por meio de antifalsificação falsos positivos que para desativar a proteção contra falsificação.
  
No entanto, há um cenário legítimo onde antifalsificação deve ser desabilitado, e isso ocorre quando há a possibilidade de filtragem de email adicional produtos no roteamento de mensagens e Office 365 não for o primeiro salto no caminho de email:
  
![Registro MX cliente não aponta para o Office 365](media/62127c16-cfb8-4880-9cad-3c12d827c67e.jpg)
  
O outro servidor pode ser um servidor de email no local do Exchange, um dispositivo como Ironport, a filtragem de email ou serviço hospedado de nuvem de outro.
  
Se o registro MX do domínio do destinatário não apontar para o Office 365, não é necessário desabilitar antifalsificação porque o Office 365 procura registro MX do seu domínio receptor e suprime antifalsificação se ela aponta para outro serviço. Se você não souber se o seu domínio tem outro servidor na frente, você pode usar um site como MX Toolbox para procurar o registro MX. Ele pode dizer algo semelhante ao seguinte:
  
![Registro MX indica o domínio não aponta para o Office 365](media/d868bb9f-3462-49aa-baea-9447a3ce4877.jpg)
  
O domínio possui um registro MX que não aponta para o Office 365, portanto Office 365 não se aplicam a imposição antifalsificação.
  
No entanto, se o registro MX do domínio do destinatário *does* apontar para o Office 365, mesmo se houver outro serviço na frente do Office 365, você deve desativar antifalsificação. O exemplo mais comum é devido ao uso de uma destinatário reconfiguração: 
  
![Diagrama de roteamento de reconfiguração de destinatário](media/070d90d1-50a0-42e4-9fd3-920bc99a7cad.jpg)
  
Registro MX do domínio contoso.com aponta para o servidor no local, enquanto o registro MX do domínio @office365.contoso .net aponta para o Office 365, porque ele contém \*. protection.outlook.com, ou \*. eo.outlook.com no registro MX:
  
![Pontos de registro MX para o Office 365, portanto, provavelmente destinatário reescrever](media/4101ad51-ef92-4907-b466-b41d14d344ca.jpg)
  
Certifique-se de diferenciar quando o registro MX de um domínio destinatário não aponta para o Office 365 e quando ele passou por uma destinatário reconfiguração. É importante saber a diferença entre esses dois casos.
  
Se você não tiver certeza se ou não seu domínio recebimento passou por uma reconfiguração de destinatário, às vezes, você pode dizer examinando os cabeçalhos de mensagem.
  
a) primeiro, examine os cabeçalhos da mensagem para o domínio do destinatário no cabeçalho da autenticação resultados: 
  
```
Authentication-Results: spf=fail (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; office365.contoso.net; dkim=fail
  (body hash did not verify) header.d=simple.example.com;
  office365.contoso.net; dmarc=none action=none
  header.from=example.com; compauth=fail reason=001
```

Domínio do destinatário é encontrado no negrito vermelho texto acima, nesta office365.contoso.net maiusculas. Isso pode ser diferente que o destinatário no campo para: cabeçalho:
  
Para: Destinatário de exemplo \<destinatário @ contoso.com\>
  
Execute uma pesquisa de registro MX do domínio do destinatário real. Se ele contiver \*. protection.outlook.com, mail.messaging.microsoft.com, \*. eo.outlook.com ou frontbridge.com, isso significa que o MX aponta para o Office 365.
  
Se ele não contiver esses valores, isso significa que o MX não aponta para o Office 365. Uma ferramenta que você pode usar para verificar isso é Toolbox MX.
  
Nesse exemplo específico, o seguinte diz que contoso.com, o domínio que se parece com o destinatário, pois ele foi para: cabeçalho, tem pontos de registro MX para um servidor em prem:
  
![Registro MX aponta para o servidor no prem](media/2444144a-9a90-4319-96b2-d115041f669f.jpg)
  
No entanto, o destinatário real é office365.contoso.net cujo registro MX que aponte para o Office 365:
  
![MX aponta para o Office 365, deve ser a reconfiguração de destinatário](media/10cf3245-9b50-475a-b655-d8a51f99d812.jpg)
  
Portanto, essa mensagem provavelmente passou por uma reconfiguração de destinatário.
  
b) em segundo lugar, certifique-se distinguir entre os casos de uso comuns do destinatário regrava. Se você pretende reescrever o domínio do destinatário para \*. onmicrosoft.com, em vez disso, reescreva-o para \*. mail.onmicrosoft.com.
  
Depois que você identificou o domínio do destinatário final é roteado por trás de outro servidor e o registro MX de domínio destinatário realmente aponta para o Office 365 (conforme publicado em seus registros DNS), você poderá passar para desabilitar antifalsificação.
  
Lembre-se de que você não deseja desabilitar antifalsificação se primeiro o salto no caminho de roteamento do domínio é o Office 365, somente quando ele estiver atrás de um ou mais serviços.
  
### <a name="how-to-disable-anti-spoofing"></a>Como desabilitar antifalsificação

Se você já tiver uma política de AntiPhishing criada, defina o parâmetro EnableAntispoofEnforcement para $false: 
  
```
$name = "<name of policy>"
Set-AntiphishPolicy -Identity $name -EnableAntiSpoofEnforcement $false 

```

Se você não souber o nome da política (ou políticas) para desabilitar, você poderá exibi-las: 
  
```
Get-AntiphishPolicy | fl Name
```

Se você não tiver quaisquer políticas antiphishing existentes, você pode criar um e, em seguida, desabilitá-lo (mesmo que você não possui uma política, antifalsificação estiver ainda aplicada; mais adiante no 2018, uma política padrão será criada para você e, em seguida, você pode desabilitar que, em vez de criar um) . Você precisará fazer isso em várias etapas: 
  
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
# Finally, scope the antiphishing policy to the domains
Set-AntiphishPolicy -Identity $name -EnableAntispoofEnforcement $false 

```

Desabilitar antifalsificação só está disponível por meio do cmdlet (posteriormente no T2 2018, ele estará disponível na segurança &amp; Centro de conformidade). Se você não tiver acesso ao PowerShell, crie um tíquete de suporte.
  
Lembre-se de que isso só deve ser aplicado a domínios que são submetidos roteamento indireta quando enviado para o Office 365. Resistir à tentação de desabilitar antifalsificação por causa de falsos positivos, será melhor a longo prazo trabalhar com elas.
  
### <a name="information-for-individual-users"></a>Informações para usuários individuais

Usuários individuais estão limitados em como eles podem interagir com a dica de safety antifalsificação. No entanto, há várias coisas que você pode fazer para resolver cenários comuns.
  
### <a name="common-scenario-1---mailbox-forwarding"></a>Cenário comum #1 - encaminhamento da caixa de correio

Se você usar outro serviço de email e encaminha seu email para o Office 365 ou Outlook.com, seu email pode ser marcado como falsificação e receber uma dica safety vermelho. O Office 365 e Outlook.com planejar lidar com isso automaticamente quando o encaminhador é uma das Outlook.com, Office 365, Gmail ou qualquer outro serviço que usa o [protocolo do arco](https://arc-spec.org). No entanto, até que essa correção é implantada, usuários devem usar o recurso de contas conectadas para importar suas mensagens diretamente, em vez de usar a opção de encaminhamento.
  
Para configurar contas conectadas no Office 365, selecione o ícone de engrenagem no canto superior direito da interface da web do Office 365 \> email \> email \> contas \> contas conectadas.
  
![Opção de contas do Office 365 - conectado](media/e8e841ca-8861-4d83-8506-2a0858c51010.jpg)
  
Em Outlook.com, o processo é o ícone de engrenagem \> opções \> email \> contas \> contas conectadas.
  
### <a name="common-scenario-2---discussion-lists"></a>Listas de discussão do cenário comum #2-

Listas de discussão são conhecidas como tiver problemas com antifalsificação devido a maneira como eles encaminhar a mensagem e modificar seu conteúdo ainda reter original do: endereço.
  
Por exemplo, suponha que o seu endereço de email é usuário @ contoso.com, e você está interessado pássaro Watching e ingressar os birdwatchers da lista de discussão @ example.com. Quando você enviar uma mensagem para a lista de discussões, você pode enviá-la desta forma:
  
**Do:** Carlos Grilo \<usuário @ contoso.com\> 
  
**Para:** Lista de discussão do birdwatcher \<birdwatchers @ example.com\> 
  
**Assunto:** Exibição excelente de jays azul na parte superior de MT. esta semana 
  
Qualquer pessoa que deseja fazer check-out à exibição nesta semana de MT. Rainier?
  
Quando a lista de email recebe a mensagem, eles formatar a mensagem, modificar seus conteúdos e reproduzi-lo novamente para o restante dos membros na lista de discussão que é composta de participantes de muitos receptores de email diferentes.
  
**Do:** Carlos Grilo \<usuário @ contoso.com\> 
  
**Para:** Lista de discussão do birdwatcher \<birdwatchers @ example.com\> 
  
**Assunto:** [BIRDWATCHERS] Exibição excelente de jays azul na parte superior de MT. esta semana 
  
Qualquer pessoa que deseja fazer check-out à exibição nesta semana de MT. Rainier?
  
---
  
Esta mensagem foi enviada para a lista de discussões Birdwatchers. Você pode cancelar a qualquer momento.
  
Em acima, a mensagem repetida tem o mesmo do: endereço (usuário @ contoso.com), mas a mensagem original foi modificado, adicionando uma marca à linha de assunto e um rodapé para a parte inferior da mensagem. Esse tipo de mensagem modificação é comum em listas de mala direta e pode resultar em falsos positivos.
  
Se você ou alguém em sua organização for um administrador da lista de endereçamento, você poderá configurá-lo para passar antifalsificação verificações.
  
- Verifique o FAQ em DMARC.org: [eu operar uma lista de endereçamento e eu quiser interoperar com DMARC, o que devo fazer?](https://dmarc.org/wiki/FAQ#I_operate_a_mailing_list_and_I_want_to_interoperate_with_DMARC.2C_what_should_I_do.3F)
    
- Leia as instruções nesta postagem de blog: [uma dica para os operadores de lista de endereçamento interoperar com DMARC para evitar falhas](https://blogs.msdn.microsoft.com/tzink/2017/03/22/a-tip-for-mailing-list-operators-to-interoperate-with-dmarc-to-avoid-failures/)
    
- Considere a instalação de atualizações no seu servidor de lista de endereçamento para suportar o arco, consulte[https://arc-spec.org](https://arc-spec.org/)
    
Se você não tiver a propriedade da lista de endereçamento:
  
- Você pode solicitar o maintainer da lista de endereçamento para implementar uma das opções acima (eles também devem ter a autenticação de email configurada para o domínio de que na lista de endereçamento é retransmissão)
    
- Você pode criar regras de caixa de correio em seu cliente de email para mover mensagens para a caixa de entrada. Você também pode solicitar administradores da sua organização para configurar regras de permissão ou substituições como discutido na seção remetentes legítimos Managing, que estão enviando email não-autenticado
    
- Você pode criar um tíquete de suporte com o Office 365 para criar uma substituição para a lista de endereçamento para tratá-lo como legítimo
    
### <a name="other-scenarios"></a>Outros cenários

1. Se nenhum dos cenários comuns acima se aplica à sua situação, denunciar a mensagem como um falso back positivo à Microsoft. Para obter mais informações, consulte a seção [como posso relatar mensagens de spam ou não spam volta para a Microsoft?](#how-can-i-report-spam-or-non-spam-messages-back-to-microsoft) mais adiante neste artigo. 
    
2. Você também pode contatar o administrador de email que pode fazê-lo como um tíquete de suporte com a Microsoft. A equipe de engenharia da Microsoft será investigar por que a mensagem foi marcada como um falso.
    
3. Além disso, se você sabe que o remetente é e estiver confiante de que eles não estão sendo modo mal-intencionado simulados, você pode responder ao remetente indicando que estão enviando mensagens de um servidor de email que não autenticar. Às vezes, isso resulta em remetente original entrando em contato com seu administrador de TI responsável por configurar os registros de autenticação de e-mail obrigatório.
  
Quando suficiente remetentes respondam volta para os proprietários do domínio que deve configurar registros de autenticação de e-mail, ele estimula os-los para executar uma ação. Enquanto o Microsoft também opera com os proprietários do domínio para publicar os registros necessários, ele ajuda ainda mais quando usuários individuais solicitarem.
    
4. Opcionalmente, adicione o remetente à sua lista de remetentes confiáveis. No entanto, lembre-se de que se phisher simula essa conta, ela será entregue à caixa de correio. Portanto, esta opção deve ser usada com moderação.
    
## <a name="how-senders-to-microsoft-should-prepare-for-anti-spoofing-protection"></a>Como os remetentes à Microsoft devem preparar para proteção antifalsificação

Se você é um administrador que atualmente envia mensagens à Microsoft, Office 365 ou Outlook.com, você deve assegurar que o seu email é autenticado adequadamente caso contrário, ele poderá ser marcado como phishing ou spam. 
  
### <a name="customers-of-office-365"></a>Clientes do Office 365

Se você for um cliente do Office 365 e usar o Office 365 para enviar emails de saída:
  
- Para seus domínios, [Configure SPF no Office 365 para ajudar a impedir a falsificação](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing)
    
- Para seus domínios principais, [Verificação de uso para validar emails de saída enviados a partir de seu domínio personalizado no Office 365](https://docs.microsoft.com/office365/SecurityCompliance/use-dkim-to-validate-outbound-email)
    
- [É recomendável configurar o registros DMARC](https://docs.microsoft.com/office365/SecurityCompliance/use-dmarc-to-validate-email) para seu domínio para determinar quem são os seus remetentes legítimos 
    
Microsoft não oferece diretrizes detalhadas de implementação para cada um dos SPF, DKIM e DMARC. No entanto, há muitas informações publicadas on-line. Também há 3º empresas de terceiros dedicado a ajudar sua organização a configurar registros de autenticação de email.
  
### <a name="administrators-of-domains-that-are-not-office-365-customers"></a>Administradores de domínios que não são clientes do Office 365

Se você for um administrador de domínio, mas não for um cliente do Office 365:
  
- Você deve configurar SPF publicar endereços IP de envio do seu domínio e também configurar DKIM (se disponível) para assinar digitalmente mensagens. Você também pode considerar a configuração de registros DMARC.
    
- Se você tiver remetentes de mala direta que estão transmitindo um email em seu nome, você deve trabalhar com eles para enviar email de uma forma, de forma que o domínio de envio no campo From: endereço (se ela pertence a você) se alinha com o domínio que passa SPF ou DMARC.
    
- Se você tiver no local servidores de email ou enviá-lo a partir de um provedor de Software como serviço ou um serviço de hospedagem de nuvem, como o Microsoft Azure, GoDaddy, rack, Amazon Web Services, ou semelhante, você deve assegurar que eles são adicionados ao seu registro SPF.
    
- Se você for um pequeno domínio que é hospedado por um ISP, você deve configurar seu registro SPF acordo com as instruções fornecidas a você pelo ISP. A maioria dos provedores fornecem esses tipos de instruções e podem ser encontradas nas páginas de suporte da empresa.
    
- Mesmo que não tiveram para registros de autenticação de email antes de publicar, e ela funcionou bem, você ainda deve publicar os registros de autenticação de e-mail para enviar à Microsoft. Fazendo isso, você está ajudando na combater phishing e reduzindo a possibilidade de que você, ou por organizações que você enviar para, obterá capturados.
    
### <a name="what-if-you-dont-know-who-sends-email-as-your-domain"></a>Se você não souber que envia o email como seu domínio?

Muitos domínios não publicar registros SPF porque elas não saiba quem são todos os seus remetentes. Que é okey, você não precisará saber quem todos eles sejam. Em vez disso, você deve começar publicando um registro SPF para aqueles conhece, especialmente onde o seu tráfego corporativo está localizado e publicar uma política de SPF neutra,? todos:
  
example.com pol TXT "v = spf1 include:spf.example.com? todos os"
  
A política de SPF neutra significa que qualquer email que vem de fora da sua infraestrutura corporativa passará a autenticação de email em todos os outros receptores de email. Email que vem de remetentes que você não souber sobre se voltará para neutral, que é quase o mesmo que não publicar nenhum registro SPF nisso.
  
Ao enviar para o Office 365, email proveniente do seu corporativo tráfego será marcado como autenticado, mas o email que vêm de fontes que você não souber sobre talvez ainda esteja marcado como falso (dependendo de estarem ou não Office 365 implicitamente pode autenticá-lo). No entanto, essa ainda é uma melhoria de todos os emails que está sendo marcado como realizar a falsificação pelo Office 365.
  
Depois que você tiver chegado começar com um registro SPF com uma política de fallback de? all, você pode incluir gradualmente a infra-estrutura de envio mais e publicar uma política mais restrito. 
  
### <a name="what-if-you-are-the-owner-of-a-mailing-list"></a>Se você for o proprietário de uma lista de endereçamento?

Consulte a seção [lista de cenário comum #2 - discussão](#common-scenario-2---discussion-lists). 
  
### <a name="what-if-you-are-an-infrastructure-provider-such-as-an-internet-service-provider-isp-email-service-provider-esp-or-cloud-hosting-service"></a>Se você é um provedor de infraestrutura como um provedor de serviços de Internet (ISP), provedor de serviço de Email (ESP) ou serviço de hospedagem de nuvem?

Se você hospedar o email de um domínio e ele envia email ou fornecer a infraestrutura de hospedagem que pode enviar email, você deve fazer o seguinte:
  
- Verifique se os que seus clientes têm documentação detalhando o que publicar em seus registros SPF
    
- Considere a possibilidade de assinaturas de verificação de assinatura em emails de saída, mesmo se o cliente não explicitamente montá-lo (sinal com um domínio padrão). Você pode até mesmo double sign-o email com assinaturas de verificação (uma vez com o domínio do cliente, se eles têm configurá-lo e uma segunda vez com assinatura de verificação da sua empresa)
    
Não é garantido que deliverability à Microsoft, mesmo se você autenticar email provenientes de sua plataforma, mas pelo menos garante que o Microsoft não lixo seu email porque não é autenticado. Para obter mais detalhes sobre como Outlook.com os filtros de email, consulte a [página Outlook.com Postmaster](https://postmaster.live.com/pm/postmaster.aspx).
  
Para obter mais detalhes sobre as práticas recomendadas de provedores de serviço, consulte [M3AAWG Mobile Messaging práticas recomendadas para provedores de serviços](https://www.m3aawg.org/sites/default/files/M3AAWG-Mobile-Messaging-Best-Practices-Service-Providers-2015-08.pdf).
  
## <a name="frequently-asked-questions"></a>Perguntas frequentes

### <a name="why-is-microsoft-making-this-change"></a>Por que a Microsoft está fazendo essa alteração?

Causa de attacks o impacto de phishing e porque a autenticação de email foi ao redor por mais de 15 anos, a Microsoft acredita que o risco de continuar permitir email não-autenticado é maior que o risco de perder emails legítimos.
  
### <a name="will-this-change-cause-legitimate-email-to-be-marked-as-spam"></a>Essa alteração fará com que os emails legítimos sejam marcadas como spam?

Inicialmente, haverá algumas mensagens marcadas como spam. No entanto, ao longo do tempo, ajustarão os remetentes e, em seguida, a quantidade de mensagens identificação incorreta como falso será insignificante para a maioria dos caminhos de email.
  
A própria Microsoft primeiro adotado esse recurso várias semanas antes de implantá-lo para o restante de seus clientes. Enquanto houve interrupção inicialmente, ele gradualmente recusada.
  
### <a name="will-microsoft-bring-this-feature-to-outlookcom-and-non-advanced-threat-protection-customers-of-office-365"></a>Microsoft trará esse recurso para o Outlook.com e não - avançadas proteção contra ameaças de clientes do Office 365?

A tecnologia da Microsoft antifalsificação inicialmente foi implantada para suas organizações que tinham uma assinatura do Office 365 Enterprise E5 ou comprou o complemento de proteção de ameaça avançadas (ATP) do Office 365 da assinatura deles. A partir de outubro de 2018, podemos estendi a proteção para as organizações que possuem o Exchange Online Protection (EOP) também. No futuro, podemos pode liberá-la para o Outlook.com. No entanto, se o fizermos, pode haver alguns recursos que não são aplicados, como relatórios e substitui personalizado.
  
### <a name="how-can-i-report-spam-or-non-spam-messages-back-to-microsoft"></a>Como posso relatar mensagens de spam ou não spam volta para a Microsoft?

Você pode usar o [suplemento relatório de mensagem do Outlook](https://support.office.com/article/use-the-report-message-add-in-b5caa9f1-cdf3-4443-af8c-ff724ea719d2), ou se ele não está instalado, [envio de spam, não spam e mensagens de golpes de phishing à Microsoft para análise](https://technet.microsoft.com/en-us/library/jj200769%28v=exchg.150%29.aspx).
  
### <a name="im-a-domain-administrator-who-doesnt-know-who-all-my-senders-are"></a>Sou um administrador de domínio que não saiba quem são todos os meus remetentes!

Consulte [os administradores de domínios que são não os clientes do Office 365](#administrators-of-domains-that-are-not-office-365-customers).
  
### <a name="what-happens-if-i-disable-anti-spoofing-protection-for-my-organization-even-though-office-365-is-my-primary-filter"></a>O que acontece se desabilitar a proteção antifalsificação da minha organização, mesmo que o Office 365 é meu filtro principal?

Não recomendamos isso porque você será exposto para mensagens de spam e phishing mais perdida. Nem todos os phishing é falsificação e será perdida falsifica nem todos os. No entanto, o risco será maior do que um cliente que permite antifalsificação.
  
### <a name="does-enabling-anti-spoofing-protection-mean-i-will-be-protected-from-all-phishing"></a>Habilitando a proteção antifalsificação significa que i estará protegido contra phishing todos?

Infelizmente, não, porque phishers será adaptar-se para usar outras técnicas como comprometida contas ou configuração de contas de serviços gratuitos. Entretanto, a proteção antiphishing funciona muito melhor para detectar esses outros tipos de métodos de phishing porque a proteção do Office 365 camadas são projetados trabalho juntos e criar na parte superior de umas às outras.
  
### <a name="do-other-large-email-receivers-block-unauthenticated-email"></a>Outros receptores de email grandes bloquear email não-autenticado?

Quase todos os receptores de email grandes implementam tradicional SPF, DKIM e DMARC. Alguns receptores têm outras verificações que são mais rigorosas que apenas os padrões, mas poucos vá quanto o Office 365 para bloquear não autenticado, email e tratá-los como um falso. No entanto, a maioria do setor de está se tornando cada vez mais restritiva sobre esse tipo específico de email, particularmente devido ao problema de phishing.
  
### <a name="do-i-still-need-the-advanced-spam-filtering-option-enabled-for-spf-hard-fail-if-i-enable-anti-spoofing"></a>Eu preciso ainda a opção de filtragem de Spam avançadas habilitada para "SPF rígido Fail" se permitir que antifalsificação?

Não, essa opção não mais é necessária porque o recurso antifalsificação não apenas considera a falha de disco rígida SPF, mas um mais amplo conjunto de critérios. Se você tiver antifalsificação habilitado e a opção de falha de disco rígido SPF habilitada, você provavelmente receberá mais falsos positivos. É recomendável desativar esse recurso, como ela seria não fornecer quase nenhum catch adicional para phishing ou spam, em vez disso, gerar principalmente falsos positivos.
  
### <a name="does-sender-rewriting-scheme-srs-help-fix-forwarded-email"></a>O esquema de reconfiguração de remetente (SRS) ajuda a corrigir email encaminhadas?

SRS apenas parcialmente corrige o problema de email encaminhadas. Reconfiguração de SMTP MAIL FROM, SRS garante que os passos de mensagem encaminhada SPF no próximo destino. No entanto, pois antifalsificação baseia-se de: endereço em combinação com o MAIL FROM ou assinatura de verificação de domínio (ou outros sinais), não é suficiente impedir que o email encaminhadas que está sendo marcado como falsificados.
  


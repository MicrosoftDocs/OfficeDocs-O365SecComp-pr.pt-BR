---
title: Saiba mais sobre a inteligência de falsificação
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 3/14/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 978c3173-3578-4286-aaf4-8a10951978bf
description: Use intelligence falso na segurança &amp; Centro de conformidade, na página Configurações do anti-spam para examinar todos os remetentes que são falsificação de qualquer um dos domínios que fazem parte da sua organização ou falsificação de domínios externos. Realizar a falsificação de inteligência de dados está disponível como parte do Office 365 Enterprise E5 ou, separadamente, como parte da proteção avançada de ameaça.
ms.openlocfilehash: a6e5f2daeab20b86354c4bf0d8d8abe0907095d1
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524138"
---
# <a name="learn-more-about-spoof-intelligence"></a>Saiba mais sobre a inteligência de falsificação

Use intelligence falso na segurança &amp; Centro de conformidade da **página de configurações antispam** para examinar todos os remetentes que são falsificação de qualquer um dos domínios que fazem parte da sua organização ou falsificação de domínios externos. Realizar a falsificação de inteligência de dados está disponível como parte do Office 365 Enterprise E5 ou, separadamente, como parte da proteção avançada de ameaça. 
  
## <a name="what-types-of-email-spoofing-can-i-review-and-which-should-i-protect-against-with-spoof-intelligence"></a>Quais tipos de falsificação de email posso revisar e qual deverá posso proteger contra com inteligência de falsificação?

Para domínios você próprio, você pode revisar remetentes que são falsificação seu domínio e, em seguida, optar por permitir que o remetente continuar ou bloquear o destinatário. Domínios externos, você pode permitir que o domínio do remetente combinado com a infra-estrutura de envio, embora não um individuais envio endereço de email.
  
Quando um remetente simula um endereço de email, eles parecem estar enviando emails em nome de uma ou mais contas de usuário dentro de um dos domínios da sua organização ou um domínio externo enviando para sua organização. Por incrível que pareça, existem algumas razões de negócios legítimos para falsificação. Por exemplo, nesses casos, você não seria bloquear o destinatário de falsificação de seu domínio:
  
- Você tem remetentes de terceiros que usam o seu domínio para enviar email em massa para seus próprios funcionários para pesquisas de empresa.
    
- Você contratado empresa de gerar e enviar atualizações de produto ou publicidade em seu nome.
    
- Um assistente que precisa regularmente para enviar email para outra pessoa em sua organização.
    
- Um aplicativo que está configurado para falsificar sua própria organização para enviar notificações internas por email.
    
Domínios externos com frequência enviar email falsificado e muitos destes motivos são legítimos. Por exemplo, aqui estão alguns casos legítimos quando os remetentes externos enviar emails falsificados:
  
- O remetente está em uma lista de endereçamento de discussão e a lista de endereçamento é retransmissão de email do remetente original para todos os participantes na lista de endereçamento.
    
- Empresa de está enviando email em nome de outra empresa (por exemplo, um relatório automatizado, ou uma empresa de software como serviço).
    
Você precisa de uma maneira de garantir que as mensagens enviadas por spoofers legítimos não se envolva nos filtros de spam no Office 365 ou sistemas de email externo. Normalmente, o Office 365 trata as mensagens de email como spam. Como um administrador do Office 365, você tem a capacidade de impedir isso, configurando filtros de falsificação na segurança &amp; Centro de conformidade. Se você é proprietário do domínio, você pode configurar SPF, DKIM e DMARC para permitir desses remetentes.
  
Por outro lado, spoofers mal-intencionado, os remetentes que são falsificação seu domínio, ou domínios externos, para enviar emails de spam ou phishing, precisam ser bloqueada. Falsificação também é uma maneira comum para phishers obter credenciais de usuário. O Office 365 possui proteção de falsificação internas para ajudar a proteger sua organização de remetentes esses emails mal-intencionados. Proteção de falsificação para domínios da sua organização está sempre ativa para todos os clientes do Office 365 e proteção de falsificação de domínio externo por padrão está ativado para clientes de proteção avançada de ameaça. Para reforçar ainda mais essa proteção, diga-nos quais os remetentes são autorizados a falsificar domínios da sua organização e enviar email em seu nome e se todos os domínios externos são permitidos para falsificar. Nenhum email enviado de um remetente que você não autorizar será tratado como spam ou falsificação pelo Office 365. Ficar atento os remetentes falsificação de seu domínio e ajudar a melhorar a falsificação de inteligência de dados usando a segurança &amp; Centro de conformidade.
  
## <a name="managing-spoof-intelligence-in-the-security-amp-compliance-center"></a>Gerenciando intelligence falso na segurança &amp; Centro de conformidade
<a name="Managespooflist"> </a>

A política de inteligência de falsificação que você configurar sempre é imposta pelo Office 365. Você não pode desabilitá-lo, mas você pode escolher quanto você deseja gerenciar ativamente-lo.
  
É possível revisar os remetentes que são falsificação seu domínio, ou domínios externos e, em seguida, decidir se cada remetente deve ter permissão para fazê-lo usando a segurança &amp; Centro de conformidade. Para cada conta de usuário falsificados que um remetente simula do seu domínio ou um domínio externo, você pode exibir as informações na tabela a seguir.
  
|**Parameter**|**Descrição**|
|:-----|:-----|
|Sender  <br/> |Também chamado de remetente true. Geralmente, esse é o domínio do qual se origina o email falso. O Office 365 determina o domínio do ponteiro do registro DNS (PTR) do endereço IP de envio que é falsificação de sua organização. Se nenhum domínio for localizado, o relatório exibe endereço IP do remetente.  <br/> |
|Usuário falsificado  <br/> |A conta de usuário que está sendo falsificada pelo remetente.  <br/> Guia **interno** somente. Este campo contém um único endereço de email ou se o remetente é a falsificação várias contas de usuário, ele contém **mais de um**.<br/> Guia **externos** somente. Domínios externos somente contém um domínio de envio e não contêm um endereço de email completo.<br/> > [!TIP]> **Para os administradores avançados.** O usuário falsificado é From endereço (5322.From), que também é o endereço exibido como o endereço de pelo cliente de email. Às vezes, isso é chamado de endereço de header.from. Este validade desse endereço não é verificada pelo SPF.           |
|Número de mensagens  <br/> |O número de mensagens enviadas pelo remetente para sua organização em nome do remetente falsificado identificado ou Remetentes nos últimos 30 dias.  <br/> |
|Número de reclamações do usuário  <br/> |Reclamações arquivadas por usuários em relação a esse remetente pelos usuários nos últimos 30 dias. Reclamações são geralmente na forma de envios de lixo eletrônico à Microsoft.  <br/> |
|Resultado de autenticação  <br/> |Esse valor é **passado** se o remetente passado remetente do Exchange Online Protection (EOP) verificações de autenticação, SPF ou DKIM, **Falha** se o remetente falhou verificações de autenticação do remetente EOP ou **desconhecida** , se o resultado dessas verificações não conhecido.  <br/> |
|Definido de decisão  <br/> |Mostra se o administrador do Office 365 ou a diretiva de inteligência de falsificação determinado se o remetente será permitido ou não falsificar o usuário.  <br/> |
|Visto pela última vez  <br/> |A última data em que uma mensagem foi recebida deste remetente em nome desse usuário falsificado.  <br/> |
|Permissão para falsificar?  <br/> | Mostra se ou não deste remetente tem permissão para enviar emails em nome do usuário falsificado. Os valores possíveis incluem:<br/> **Sim** Todos os endereços falsificados deste remetente falsificação poderão falsificar sua organização.  <br/> **Não** Endereços falsificados deste remetente falsificação não será possível falsificar sua organização. Em vez disso, as mensagens deste remetente serão marcadas como spam pelo Office 365.<br/> **Alguns usuários** Se um remetente é falsificação de vários usuários, alguns endereços falsificados deste remetente poderão falsificar sua organização, o restante será marcado como spam. Use a guia **Detailed** para ver os endereços específicos.<br/> |
|Tipo de falsificação  <br/> |Esse valor é **interno** , se o domínio estiver em um dos domínios provisionados da sua organização, caso contrário, o valor é **externa**.  <br/> |
   
 **Para gerenciar os remetentes que são falsificação seu domínio usando a segurança &amp; Centro de conformidade**
  
1. Vá até o [segurança &amp; Centro de conformidade](https://protection.office.com).
    
2. Faça logon no Office 365 com sua conta do trabalho ou da escola. Sua conta deve ter credenciais de administrador em sua organização do Office 365.
    
3. Na segurança &amp; Centro de conformidade, expanda **Gerenciamento de ameaça** \> **política** \> **anti-spam**.
  
![](media/0a098e68-5ecf-40d7-984f-d15fcc1f958d.jpg)
  
4. Na página **configurações antispam** no painel direito, selecione a guia **personalizada** , role para baixo e expanda **diretiva de inteligência de falso**. 
  
![](media/a5112100-0b37-460f-932d-5b2f98157871.jpg)
  
5. Para exibir a lista de remetentes falsificação de seu domínio, escolha **novos remetentes de revisão** e selecione o * * domínios Your * * guia. 
    
    Se você já analisou remetentes e deseja alterar algumas das suas escolhas anteriores, você pode escolher **Mostrar-me remetentes que eu já analisado** em vez disso. Em ambos os casos, o painel a seguir é exibida. 
  
![](media/c0c062fd-f4a4-4d78-96f7-2c22009052bb.jpg)
  
Cada usuário falsificado é exibido em uma linha separada para que você pode escolher se deseja permitir ou bloquear o remetente de falsificação de cada usuário individualmente.
  
Para adicionar um remetente à lista de permissões para um usuário, selecione **Sim** na coluna **permitidos falsificar** . Para adicionar um remetente à lista de bloqueios para um usuário, escolha **não**.
  
Para definir a diretiva para domínios você não proprietário, selecione na guia **Domínios externos** mudar qualquer remetente como **Sim** na coluna **permissão para realizar a falsificação** para permitir que esse remetente para enviar o email não-autenticado em sua organização. Como alternativa, se você achar que o Office 365 tem feito um erro em permitindo que o remetente para enviar emails falsificados, altere a coluna **permitidos falsificar** como **não**. 
  
![](media/5dbef9cf-103f-49cd-9638-4b0083d6baa7.jpg)
  
6. Escolha **Salvar** para salvar as alterações. 
    
## <a name="configuring-the-anti-spoofing-policy"></a>Configurando a política antifalsificação
<a name="Managespooflist"> </a>

Além de permitir ou bloquear um remetente específico enviem email falsificado em sua organização, você também pode configurar como rigor que você deseja que o filtro a ser, a ação a ser executada quando uma mensagem de falsificação for encontrada e se deseja ou não habilitar dicas de segurança para antifalsificação.
  
Proteção antifalsificação é aplicada ao email de remetentes de domínios que são externos à sua organização do Office 365. Você pode aplicar a política aos destinatários cujas caixas de correio são licenciadas para o Office 365 Enterprise E5 ou da proteção de ameaça avançadas. Você gerenciar a política antifalsificação junto com as outras configurações de AntiPhishing ATP. Para obter mais informações sobre configurações de AntiPhishing ATP, consulte [Configurar as diretivas de AntiPhishing do Office 365](https://support.office.com/article/set-up-office-365-atp-anti-phishing-policies-5a6f2d7f-d998-4f31-b4f5-f7cbf6f38578?ui=en-US&amp;rs=en-US&amp;ad=US#phishpolicyoptions).
  
O Office 365 inclui proteção antifalsificação padrão que sempre está sendo executado. Essa proteção padrão não estiver visível na segurança &amp; Centro de conformidade ou recuperável por meio de cmdlets do Windows PowerShell. Você não pode modificar a proteção antifalsificação de padrão. Em vez disso, você pode configurar como estritamente Office 365 impõe a proteção antifalsificação de cada política antiphishing que você criar. 
  
Embora a política antifalsificação aparece sob a política de AntiPhishing ATP na segurança &amp; Centro de conformidade, ele não herde seu comportamento padrão de phishing existente definindo sob a configuração de anti-spam. Se você tiver configurações em **anti-spam** \> **Phishing** que você deseja replicar para antifalsificação, você precisará criar uma política de AntiPhishing e editar a parte de falsificação da política antiphishing para refletir suas configurações de falsificação como descrito na seção a seguir, em vez de aceitar as configurações padrão que são executados em segundo plano. 
  
 **Configurar a proteção antifalsificação dentro de uma política de AntiPhishing usando a segurança &amp; Centro de conformidade**
  
1. Vá até o [segurança &amp; Centro de conformidade](https://protection.office.com).
    
2. Faça logon no Office 365 com sua conta do trabalho ou da escola. Sua conta deve ter credenciais de administrador em sua organização do Office 365.
    
3. Na segurança &amp; Centro de conformidade, expanda **Gerenciamento de ameaça** \> **política** \> **antiphishing ATP**. 
    
4. Na página **antiphishing** no painel direito, selecione a política de AntiPhishing que você deseja configurar. 
    
5. Na página que aparece na linha **Falso** , escolha **Editar**. 
    
6. Sobre os **limites de falsificação** de página, se você selecionar **padrão**, e em seguida, todas as mensagens que implícita ou explicitamente passam na autenticação serão entregues, ou seja, é enviado para filtragem de email normal. Se você selecionar **estrito**, então mensagens que passam autenticação implicitamente com confiança média, também chamado uma autenticação de composição de "pass suave", será ignorada mesmo assim e marcado como falsificação de mensagens de email. A configuração Strict é agressiva e irá gerar falsos positivos. Fazer sua escolha e selecione **ações**. 
  
![](media/62327314-a65f-49b0-bf60-ab4775e0bc9e.jpg)
  
7. Em seguida, configure as ações a serem executadas quando uma mensagem é detectada como um falso entre domínios. O comportamento padrão é mover a mensagem para a pasta de lixo eletrônico do destinatário. A outra opção é enviar a mensagem para a quarentena. Para obter mais informações sobre como gerenciar as mensagens enviadas para quarentena, consulte [mensagens de email de quarentena no Office 365](quarantine-email-messages.md).
  
![](media/7a868dff-2c4b-46b9-88ca-f2d523ca2307.jpg)
  
8. Escolha se deseja habilitar ou desabilitar antifalsificação dicas de segurança. O Office 365 recomenda a habilitação da dica de segurança **a autenticação falha** para avisar aos usuários quando eles estão interagindo com um remetente cuja identidade não pôde ser verificada. O Office 365 também recomenda habilitando a dica de segurança para um **autenticação soft-pass** para grupos menores de usuários, pois essa dica safety pode gerar muita avisos se o usuário recebe email de várias fontes legítimos, mas não-autenticados. 
  
![](media/1ed675c0-48c2-4587-a957-60eb68dc9628.jpg)
  
Fazer sua escolha e selecione **Salvar**. 
    
## <a name="other-ways-to-manage-spoofing-and-phishing-with-office-365"></a>Outras maneiras de gerenciar a falsificação e phishing com o Office 365
<a name="Managespooflist"> </a>

Estar atento sobre falsificação e proteção contra phishing. Aqui estão maneiras relacionadas a verificação de remetentes falsificação de seu domínio e ajudar a impedir prejudicar sua organização:
  
- Verifique o relatório de email do Exchange Online Protection falsificação como parte de sua rotina. Você pode usar este relatório com frequência para exibir e ajudar a gerenciar remetentes falsificados. Para obter informações, consulte o **relatório de email de falsificação** em [relatórios de proteção de email de uso no Office 365 para exibir dados sobre malware, spam e detecções de regra](https://technet.microsoft.com/library/dn500744%28v=exchg.150%29.aspx).
    
- Para obter mais informações avançadas de administradores do Office 365:
    
  - Analise sua configuração de política de remetente Framework (SPF). Para obter uma introdução rápida SPF e instalá-la configurado rapidamente, consulte [Configurar SPF no Office 365 para ajudar a impedir a falsificação](https://technet.microsoft.com/library/dn789058%28v=exchg.150%29.aspx). Para ter uma compreensão mais detalhada de como o Office 365 usa SPF ou para implantações não-padrão ou de solução de problemas, por exemplo, híbrida, inicie com [como o Office 365 usa Framework de política do remetente (SPF) para evitar a falsificação](https://technet.microsoft.com/library/mt712724%28v=exchg.150%29.aspx).
    
  - Analise sua configuração de email de identificado DomainKeys (DKIM). Você deve usar DKIM além SPF e DMARC para ajudar a impedir spoofers enviem mensagens que pareçam que eles são provenientes de seu domínio. DKIM permite adicionar uma assinatura digital para mensagens de email no cabeçalho da mensagem. Para obter informações, consulte [Verificação de uso para validar emails de saída enviados do seu domínio no Office 365](https://technet.microsoft.com/library/mt695945%28v=exchg.150%29.aspx).
    
  - Analise sua configuração de autenticação de mensagem, relatórios e conformidade (DMARC) baseada em domínio. Implementar DMARC com SPF e DKIM fornece proteção adicional contra email falsificação e phishing. Ajuda DMARC sistemas de recebimento de email determinam o que fazer com que as mensagens enviadas a partir de seu domínio SPF fail ou DKIM verifica. Para obter informações, consulte [DMARC de uso para validar emails no Office 365](https://technet.microsoft.com/library/mt734386%28v=exchg.150%29.aspx).
    
  - Use o cmdlet [Get-PhishFilterPolicy](https://technet.microsoft.com/en-us/library/mt735158%28v=exchg.160%29.aspx) Windows PowerShell para reunir dados detalhados sobre remetentes falsificados, gerar permitir, bloquear listas e ajudá-lo a determinar como gerar o mais abrangentes registros SPF, DKIM e DMARC DNS sem ter sua emails legítimos ficar preso em filtros de spam externo. Para obter mais informações, consulte [como antispoofing proteção funciona no Office 365](https://blogs.msdn.microsoft.com/tzink/2016/02/23/how-antispoofing-protection-works-in-office-365/).
    


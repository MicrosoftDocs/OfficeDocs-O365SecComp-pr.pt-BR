---
title: Regras de fluxo de emails (regras de transporte) no Exchange Online Protection
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/29/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 9c2cf227-eff7-48ef-87fb-487186e47363
description: Você pode usar regras de fluxo de emails (regras de transporte) para identificar e executar ações em mensagens que fluem pela sua organização do Office 365.
ms.openlocfilehash: a60035dc2ac17bcb944a5311827609381a7ed31e
ms.sourcegitcommit: 48fa456981b5c52ab8aeace173c8366b9f36723b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/28/2019
ms.locfileid: "30341202"
---
# <a name="mail-flow-rules-transport-rules-in-exchange-online-protection"></a>Regras de fluxo de emails (regras de transporte) no Exchange Online Protection

Você pode usar regras de fluxo de emails (também conhecidas como regras de transporte) para identificar e agir com base nas mensagens que fluem pela organização do Office 365. As regras de fluxo de emails são semelhantes às regras de Caixas de Entrada disponíveis no Outlook e no Outlook na Web. A principal diferença das regras de fluxo de emails é que elas atuam em mensagens que estão em trânsito, não depois que a mensagem foi entregue à caixa de correio. As regras de fluxo de emails contêm conjuntos mais amplos de condições, exceções e ações com os quais é possível desfrutar da flexibilidade necessária para implementar muitos tipos de políticas de mensagem.
  
Este artigo explica os componentes das regras de fluxo de emails e como eles funcionam.
  
Para obter as etapas para criar, copiar e gerenciar regras de fluxo de emails, consulte **Manage Mail Flow Rules**. Para cada regra, você tem a opção de fazê-lo, testá-lo ou testá-lo e notificar o remetente. Para saber mais sobre as opções de teste, confira **testar uma regra de fluxo** de emails e **dicas de política**.
  
Para relatórios de resumo e detalhes sobre as mensagens que correspondem a regras de fluxo de emails, confira **Usar relatórios de proteção de email no Office 365 para exibir dados sobre detecções de malware, spam e de regra**.
  
Para implementar políticas de mensagens específicas usando regras do fluxo de emails, confira estes tópicos:
  
- [Use mail flow rules to inspect message attachments in Office 365](http://technet.microsoft.com/library/874d1c78-a8ec-4938-b388-d3208c2fa971.aspx)
    
- [Configure a criptografia no Office 365 Enterprise](https://support.office.com/article/e86fc991-0161-4f01-9c1c-d25e87733d06)
    
- [Organization-wide message disclaimers, signatures, footers, or headers in Office 365](http://technet.microsoft.com/library/29ac61c2-77f1-4071-b14e-8cc64e3e76ba.aspx)
    
- [Use mail flow rules to set the spam confidence level (SCL) in messages](../use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages.md)
    
- [Create organization-wide safe sender or blocked sender lists in Office 365](../create-organization-wide-safe-sender-or-blocked-sender-lists-in-office-365.md)
    
- [Redução de ameaças de malware com o bloqueio de anexos de arquivo no Exchange Online Protection](reducing-malware-threats-through-file-attachment-blocking-in-exchange-online-pro.md)
    
- [Definir regras para criptografar ou descriptografar mensagens de email](https://go.microsoft.com/fwlink/p/?Linkid=402846).
    
O vídeo a seguir fornece uma demonstração da configuração de regras de fluxo de emails na proteção do Exchange Online.
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/7cdcd2cb-9382-4065-98e1-81257b32a189?autoplay=false]
  
## <a name="mail-flow-rule-components"></a>Componentes de regra de fluxo de email

Um regra de fluxo de emails é formada por condições, exceções, ações e propriedades:
  
- **Condições** Identificam as mensagens nas quais você gostaria de aplicar uma ação. Algumas condições examinam campos de cabeçalhos de mensagens (por exemplo, os campos Para, De ou Cc). Outras condições examinam propriedades de mensagens (por exemplo, assunto, corpo, anexos, tamanho e classificação da mensagem). A maioria das condições exige que você especifique um operador de comparação (por exemplo, igual a, diferente de ou contém) e um valor a ser correspondido. Se não houver condições ou exceções, a regra será aplicada a todas as mensagens. 
    
    Para obter mais informações sobre as condições de regra de fluxo de emails no Exchange Online Protection, consulte [Mail Flow Rule Conditions and exceptions (predicates) no Exchange Online.](https://docs.microsoft.com/en-us/exchange/security-and-compliance/mail-flow-rules/conditions-and-exceptions).
    
- **Exceções** Opcionalmente, identificam as mensagens às quais as ações não devem se aplicar. Os mesmos identificadores de mensagens disponíveis nas condições também estão disponíveis nas exceções. As exceções substituem as condições e impedem que as ações da regra sejam aplicadas a uma mensagem, mesmo que a mensagem atenda a todas as condições configuradas. 
    
- **Ações** Especificam o que fazer com as mensagens que atendem a todas as condições na regra, mas não se encaixam em nenhuma das exceções. Há muitas ações disponíveis, como rejeitar, excluir ou redirecionar mensagens, incluir destinatários adicionais, incluir prefixos no assunto da mensagem ou inserir avisos de isenção legal no corpo da mensagem. 
    
    Para obter mais informações sobre ações de regra de fluxo de emails disponíveis no Exchange Online Protection, consulte [Mail Flow Rule Actions in Exchange Online Protection](http://technet.microsoft.com/library/f8621ecb-a177-4025-9011-a6569999746a.aspx).
    
- **Propriedades** Especificam outras configurações de regras que não sejam condições, exceções ou ações. Por exemplo, quando a regra deve ser aplicada, se devemos impor ou testar a regra e o período em que a regra é ativa. 
    
     Para obter mais informações, confira a seção [Propriedades de regras de fluxo de email](mail-flow-rules-transport-rules-0.md#Properties) neste tópico. 
    
### <a name="multiple-conditions-exceptions-and-actions"></a>Várias condições, exceções e ações

A seguinte tabela mostra como várias condições, valores de condição, exceções e ações são tratadas em uma regra.
  
|**Componente**|**Lógica**|**Comentários**|
|:-----|:-----|:-----|
|Várias condições  <br/> |E  <br/> |Uma mensagem deve atender a todas as condições da regra. Se você precisar combinar uma condição ou outra, use regras separadas para cada condição. Por exemplo, se quiser adicionar o mesmo aviso de isenção legal a mensagens com anexos e mensagens com texto específico, crie uma regra para cada condição. No EAC, você pode facilmente copiar uma regra.  <br/> |
|Uma condição com vários valores  <br/> |OU  <br/> |Algumas condições permitem especificar mais de um valor. A mensagem deve corresponder a qualquer um dos valores especificados (não todos). Por exemplo, se o assunto de uma mensagem de email for Informações sobre o mercado de ações e a condição **O assunto inclui qualquer uma destas palavras** estiver configurada para corresponder às palavras Contoso ou ações, a condição será atendida, pois o assunto contém pelo menos um dos valores especificados.  <br/> |
|Várias exceções  <br/> |OU  <br/> |Se uma mensagem corresponder a qualquer uma das exceções, as ações não são aplicadas na mensagem. A mensagem não precisa coincidir com todas as exceções.  <br/> |
|Várias ações  <br/> |E  <br/> |As mensagens que atendem às condições de uma regra recebem todas as ações que estão especificadas na regra. Por exemplo, se as ações **Preceder o assunto da mensagem com** e **Adicionar destinatários à caixa Cco** estiverem selecionadas, ambas as ações serão aplicadas à mensagem.  <br/> Lembre-se que algumas ações, como **Excluir a mensagem sem notificar ninguém**, impedem que regras subsequentes sejam aplicadas à mensagem. Outras ações como **Encaminhar a mensagem** não permitem ações adicionais.  <br/> Também é possível configurar uma ação em uma regra de tal forma que, quando ela for aplicada, as regras seguintes não sejam aplicadas à mensagem.  <br/> |
   
### <a name="mail-flow-rule-properties"></a>Propriedades de regras de fluxo de email
<a name="Properties"> </a>

A tabela a seguir descreve as propriedades das regras que estão disponíveis nas regras de fluxo de emails.
  
|**Nome da propriedade no EAC**|**Nome do parâmetro no PowerShell**|**Descrição**|
|:-----|:-----|:-----|
|**Prioridade** <br/> | _Priority_ <br/> |Indica a ordem que as regras são aplicadas às mensagens. A prioridade padrão se baseia no momento em que a regra é criada (regras mais antigas têm uma prioridade mais alta que as regras mais recentes e as regras de prioridade mais alta são processadas antes das regras de prioridade mais baixa).    <br/> Altere a prioridade da regra no EAC movendo a regra para cima ou para baixo na lista de regras. No PowerShell, defina o número de prioridade (0 é a prioridade mais alta).    <br/> Por exemplo, se tiver uma regra para rejeitar mensagens que incluam um número de cartão de crédito e outra exigindo aprovação, você desejará que a regra de rejeição ocorra primeiro e pare a aplicação das outras regras.  |
|**Modo** <br/> | _Mode_ <br/> |Você pode especificar se deseja que a regra comece a processar as mensagens imediatamente, ou se deseja testar as regras sem afetar a entrega da mensagem (com ou sem Prevenção contra Perda de Dados ou Dicas de Política DLP).  <br/> As dicas de política apresentam uma anotação breve no Outlook ou no Outlook na Web que fornecem informações sobre possíveis violações de política para a pessoa que está criando a mensagem. Para saber mais, veja **Policy Tips**.  <br/> Para saber mais sobre os modos, confira **Test a mail flow rule**.  <br/> |
|**Ativar esta regra na seguinte data** <br/> **Desativar esta regra na seguinte data** <br/> | _ActivationDate_ <br/>  _ExpiryDate_ <br/> |Especifica o intervalo de datas quando a regra está ativa.  <br/> |
|**Na** caixa de seleção selecionada ou não selecionada  <br/> |Novas regras: parâmetro  _Enabled_ no cmdlet **New-TransportRule**.  <br/> Regras existentes: Use os cmdlets **Enable-TransportRule** ou **Disable-TransportRule**.  <br/> O valor é exibido na propriedade **State** da regra.  <br/> |Você pode criar uma regra desabilitada e ativá-la quando estiver pronto para testá-la. Ou, você pode desativar uma regra sem excluí-la para preservar as configurações.  <br/> |
|**Adiar a mensagem se o processamento de regra não for concluído** <br/> | _RuleErrorAction_ <br/> |Você pode especificar como a mensagem deveria ser tratada se o processamento de regra não puder ser concluído. Por padrão, a regra será ignorada, mas você pode optar por reenviar a mensagem para processamento.  <br/> |
|**Corresponder endereço do remetente da mensagem** <br/> | _SenderAddressLocation_ <br/> |Se a regra usa condições ou exceções que examinam o endereço de email do remetente, você pode procurar o valor no cabeçalho da mensagem, no envelope da mensagem ou em ambos.  <br/> |
|**Parar o processamento de mais regras** <br/> | _SenderAddressLocation_ <br/> |Essa é uma ação para a regra, mas se parece com uma propriedade no EAC. Você pode optar por evitar a aplicação de regras adicionais a uma mensagem após uma regra processar uma mensagem.  <br/> |
|**Comentários** <br/> | _Comments_ <br/> |Você pode inserir comentários descritivos sobre a regra.  <br/> |
   
## <a name="how-mail-flow-rules-are-applied-to-messages"></a>Como as regras de fluxo de emails são aplicadas a mensagens

Todas as mensagens que fluem por sua organização são avaliadas pelas regras de fluxo de emails habilitadas para a sua organização. As regras são processadas na ordem listada na página **Fluxo de emails** \> **Regras** ou baseadas no valor do parâmetro  _Priority_ correspondente no PowerShell. 
  
Cada regra também oferece a opção de parar o processamento de outras quando é encontrada correspondência com a regra. Esta configuração é importante para as mensagens que atendem às condições em várias regras de fluxo de emails (qual regra você deseja aplicar à mensagem? Todas? Apenas uma?).
  
### <a name="differences-in-processing-based-on-message-type"></a>Diferenças no processamento com base no tipo de mensagem

Existem vários tipos de mensagens que transitam por uma organização. A tabela a seguir mostra quais tipos de mensagens podem ser processados por regras de fluxo de emails.
  
****

|**Tipo de mensagem**|**Uma regra pode ser aplicada?**|
|:-----|:-----|
|**Mensagens normais** Mensagens que contêm um único corpo com formato rich text (RTF), HTML ou texto sem formatação, ou um conjunto de corpos de mensagem em várias partes ou alternativo.  <br/> |Sim  <br/> |
|**Criptografia de Mensagem do Office 365 ** As mensagens criptografadas por Criptografia de Mensagem do Office 365 em Office 365. Para saber mais, veja [Criptografia de Mensagens do Office 365](https://go.microsoft.com/fwlink/p/?LinkId=392525).  <br/> |As regras sempre podem acessar os cabeçalhos de envelope e processar as mensagens com base nas condições que inspecionam cabeçalhos.  <br/> Para uma regra inspecionar ou modificar o conteúdo de uma mensagem criptografada, é preciso verificar se a descriptografia de transporte está habilitada (Obrigatória ou Opcional; o padrão é Opcional). Para saber mais, veja [Habilitar ou desabilitar a descriptografia de transporte](https://go.microsoft.com/fwlink/p/?linkid=848060).  <br/> Você também pode criar uma regra que descriptografa automaticamente mensagens criptografadas. Para saber mais, veja [Definir regras para criptografar ou descriptografar mensagens de email](https://go.microsoft.com/fwlink/p/?Linkid=402846).  <br/> |
|**Mensagens criptografadas em S/MIME** <br/> |As regras podem apenas acessar os cabeçalhos de envelope e processar as mensagens com base nas condições que inspecionam cabeçalhos.  <br/> As regras com condições que exigem a inspeção do conteúdo da mensagem ou ações que modificam o conteúdo da mensagem não podem ser processadas.  <br/> |
|**Mensagens protegidas por RMS** Mensagens que tinham um Active Directory Rights Management Services (AD RMS) ou uma Azure Rights Management (RMS) política aplicada.  <br/> |As regras sempre podem acessar os cabeçalhos de envelope e processar as mensagens com base nas condições que inspecionam cabeçalhos.  <br/> Para uma regra inspecionar ou modificar o conteúdo de uma mensagem protegida por RMS, é preciso verificar se a descriptografia de transporte está habilitada (Obrigatória ou opcional; o padrão é opcional). Para saber mais, veja [Habilitar ou desabilitar a descriptografia de transporte](https://go.microsoft.com/fwlink/p/?linkid=848060).  <br/> |
|**Mensagem com assinatura não criptografada** Mensagens que foram assinadas, mas não foram criptografadas.  <br/> |Sim  <br/> |
|**Mensagens da UM** Mensagens criadas ou processadas pelo serviço de Unificação de Mensagens, como uma mensagem de voz, fax, notificações de chamadas não atendidas e mensagens criadas ou encaminhadas usando o Microsoft Outlook Voice Access.  <br/> |Sim  <br/> |
|**Mensagens anônimas** Mensagens enviadas por remetentes anônimos.  <br/> |Sim  <br/> |
|**Notificações de leitura** Relatórios gerados em resposta às solicitações de confirmação de leitura pelos remetentes. Notificações de leitura têm a classe de mensagem  `IPM.Note*.MdnRead` ou  `IPM.Note*.MdnNotRead`.  <br/> |Sim  <br/> |
   
## <a name="what-else-should-i-know"></a>O que mais devo saber?

- O valor da propriedade **version** ou **RuleVersion** para uma regra não é importante no Exchange Online Protection. 
    
- Após criar ou alterar uma regra de fluxo de emails, pode levar até 30 minutos para a regra nova ou atualizada ser aplicada às mensagens.
    
## <a name="for-more-information"></a>Para saber mais
  
[Usar regras de fluxo de email para inspecionar anexos de mensagens no Exchange Online](http://technet.microsoft.com/library/874d1c78-a8ec-4938-b388-d3208c2fa971.aspx)
  
[Criptografia de e-mail no Office 365](https://support.office.com/article/c0d87cbe-6d65-4c03-88ad-5216ea5564e8)
  
[Limites de regras de diário, transporte e caixa de entrada](https://go.microsoft.com/fwlink/p/?LinkId=324584)

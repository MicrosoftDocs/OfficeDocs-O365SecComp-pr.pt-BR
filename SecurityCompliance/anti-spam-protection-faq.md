---
title: Perguntas frequentes sobre a proteção antispam
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: c534a35d-b121-45da-9d0a-ce738ce51fce
description: Este tópico fornece as perguntas frequentes e respectivas respostas sobre a proteção contra spam. As respostas são aplicáveis aos clientes do Microsoft Exchange Online e do Proteção do Exchange Online (EOP).
ms.openlocfilehash: 21c399ed0ccf0f7a03c5396d8a594fccb0f133b8
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026428"
---
# <a name="anti-spam-protection-faq"></a><span data-ttu-id="d128c-104">Perguntas frequentes sobre a proteção antispam</span><span class="sxs-lookup"><span data-stu-id="d128c-104">Anti-spam protection FAQ</span></span>

<span data-ttu-id="d128c-p102">Este tópico fornece as perguntas frequentes e respectivas respostas sobre a proteção contra spam. As respostas são aplicáveis aos clientes do Microsoft Exchange Online e do Proteção do Exchange Online (EOP).</span><span class="sxs-lookup"><span data-stu-id="d128c-p102">This topic provides frequently asked questions and answers about anti-spam protection. Answers are applicable for Microsoft Exchange Online and Exchange Online Protection (EOP) customers.</span></span> 
  
> [!TIP]
> <span data-ttu-id="d128c-p103">Para perguntas e respostas sobre remetente seguro e listas de remetentes bloqueados, consulte [Remetentes seguros e bloqueados listas de remetentes no Exchange Online](safe-sender-and-blocked-sender-lists-faq.md). Para perguntas e respostas sobre a quarentena, consulte [Perguntas frequentes sobre a quarentena](quarantine-faq.md).</span><span class="sxs-lookup"><span data-stu-id="d128c-p103">For questions and answers about safe sender and blocked sender lists, see [Safe sender and blocked sender lists in Exchange Online](safe-sender-and-blocked-sender-lists-faq.md). For questions and answers about the quarantine, see [Quarantine FAQ](quarantine-faq.md).</span></span> 
  
 <span data-ttu-id="d128c-109">**P. Por padrão, o que acontece com uma mensagem de spam detectada?**</span><span class="sxs-lookup"><span data-stu-id="d128c-109">**Q. By default, what happens to a spam-detected message?**</span></span>
  
<span data-ttu-id="d128c-p104">R. **Para mensagens de entrada:** A maioria dos spams é excluída por meio da filtragem de conexão, que se baseia no endereço IP do remetente. O serviço então inspeciona o conteúdo da mensagem. Por padrão, o spam de conteúdo filtrado é enviado para a pasta Lixo Eletrônico do destinatário. Você pode alterar essa ação. Por exemplo, você pode optar por enviar mensagens de spam para a quarentena em vez de configurar a política de filtro de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="d128c-p104">A. **For inbound messages:** The majority of spam is deleted via connection filtering, which is based on the IP address of the sender. The service then inspects the contents of the message. By default, content-filtered spam is sent to the recipient's Junk Email folder. You can change this action. For example, you can choose to send spam messages to the quarantine instead by configuring the content filter policy.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="d128c-p105">Para clientes autônomos do EOP: Para garantir que a ação **Mover a mensagem para a pasta Lixo Eletrônico** funcionará com caixas de correio locais, você deve configurar duas regras de Transporte do Exchange em seus servidores locais para detectar cabeçalhos de spam adicionados por EOP. Para obter detalhes, consulte [Garantir que o spam seja direcionado para a pasta Lixo Eletrônico de cada usuário](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md).</span><span class="sxs-lookup"><span data-stu-id="d128c-p105">For EOP standalone customers: In order to ensure that the **Move message to Junk Email folder** action will work with on-premises mailboxes, you must configure two Exchange Transport rules on your on-premises servers to detect spam headers added by EOP. For details, see [Ensure that spam is routed to each user's Junk Email folder](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md).</span></span> 
  
 <span data-ttu-id="d128c-118">**Para mensagens de saída:** A mensagem foi roteada através do pool de entrega de risco mais alto ou foi devolvida sem ser entregue; em cujo caso o remetente receberá uma mensagem de notificação de status de entrega (DSN) informando que a mensagem não pôde ser entregue.</span><span class="sxs-lookup"><span data-stu-id="d128c-118">**For outbound messages:** The message is either routed through the higher risk delivery pool or is bounced and not delivered, in which case the sender should receive a delivery status notification (DSN) message telling them that the message couldn't be delivered.</span></span> 
  
 <span data-ttu-id="d128c-119">**P. o que é uma variant de spam de dia zero e como ela é manipulada pelo serviço?**</span><span class="sxs-lookup"><span data-stu-id="d128c-119">**Q. What's a zero-day spam variant and how is it handled by the service?**</span></span>
  
<span data-ttu-id="d128c-p106">R. uma variant de spam de dia zero é uma primeira geração, variant desconhecidas anteriormente que estejam de spam que nunca foi capturado ou analisado, para que nossos filtros de conteúdo de spam ainda não tenham nenhuma informação disponível para detectar a ele. Após um spam de dia zero amostra é capturada e analisada pelo nossos analistas de spam, se ela atende aos critérios de classificação de spam, nosso spam conteúdo filtros são atualizados para detectar a ele e não mais é considerada "zero-day". ( **Observação:** se você receber uma mensagem que pode ser uma variant de spam de dia zero, a fim de ajudar a melhorar o serviço, envie a mensagem para a Microsoft usando um dos métodos descritos na [enviar spam, não spam e mensagens de golpes de phishing à Microsoft para análise](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md).)</span><span class="sxs-lookup"><span data-stu-id="d128c-p106">A. A zero-day spam variant is a first generation, previously unknown variant of spam that's never been captured or analyzed, so our spam content filters don't yet have any information available for detecting it. After a zero-day spam sample is captured and analyzed by our spam analysts, if it meets the spam classification criteria, our spam content filters are updated to detect it, and it's no longer considered "zero-day." ( **Note:** If you receive a message that may be a zero-day spam variant, in order to help us improve the service, please submit the message to Microsoft using one of the methods described in [Submit spam, non-spam, and phishing scam messages to Microsoft for analysis](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md).)</span></span>
  
 <span data-ttu-id="d128c-124">**P. Eu preciso configurar o serviço para fornecer proteção contra spam?**</span><span class="sxs-lookup"><span data-stu-id="d128c-124">**Q. Do I need to configure the service to provide anti-spam protection?**</span></span>
  
<span data-ttu-id="d128c-p107">R. Depois de se inscrever no serviço e adicionar o seu domínio, a filtragem de spam é automaticamente habilitada em toda a empresa por meio das políticas padrão contra spam. As políticas padrão são ajustadas para protegê-lo sem a necessidade de configuração adicional (salvo a exceção mencionada acima para os clientes autônomos do EOP). Como administrador, você pode editar as políticas padrão contra spam para que sejam adaptadas para atender às necessidades da sua organização da melhor maneira possível. Para obter uma granularidade melhor, você também pode criar políticas de filtragem de conteúdo personalizadas e aplicá-las a usuários, grupos ou domínios específicos na sua organização. Políticas personalizadas sempre terão prioridade sobre a política padrão, mas você pode alterar a prioridade (ordem de execução) de suas políticas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="d128c-p107">A. After you sign up for the service and add your domain, spam filtering is automatically enabled company-wide through the default anti-spam policies. The default policies are tuned to protect you without needing any additional configuration (aside from the exception noted above for EOP standalone customers). As an admin, you can edit the default anti-spam policies so that they're tailored to best meet the needs of your organization. For greater granularity, you can also create custom content filter policies and apply them to specified users, groups, or domains in your organization. Custom policies always take precedence over the default policy, but you can change the priority (that is, the running order) of your custom policies.</span></span>
  
<span data-ttu-id="d128c-131">Para obter mais informações sobre como configurar suas políticas contra spam, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="d128c-131">For more about configuring your anti-spam policies, see the following topics:</span></span>
  
[<span data-ttu-id="d128c-132">Configurar a política de filtro de conexão</span><span class="sxs-lookup"><span data-stu-id="d128c-132">Configure the connection filter policy</span></span>](configure-the-connection-filter-policy.md)
  
[<span data-ttu-id="d128c-133">Configurar suas políticas de filtro de spam</span><span class="sxs-lookup"><span data-stu-id="d128c-133">Configure your spam filter policies</span></span>](configure-your-spam-filter-policies.md)
  
[<span data-ttu-id="d128c-134">Configurar a política de spam de saída</span><span class="sxs-lookup"><span data-stu-id="d128c-134">Configure the outbound spam policy</span></span>](configure-the-outbound-spam-policy.md)
  
 <span data-ttu-id="d128c-135">**P. Se eu fizer uma alteração em uma política contra spam, quanto tempo demora para que as alterações façam efeito após eu salvá-las?**</span><span class="sxs-lookup"><span data-stu-id="d128c-135">**Q. If I make a change to an anti-spam policy, how long does it take after I save my changes for them to take effect?**</span></span>
  
<span data-ttu-id="d128c-p108">R. Pode levar até 1 hora para que as alterações entrem em efeito.</span><span class="sxs-lookup"><span data-stu-id="d128c-p108">A. It may take up to 1 hour for the changes to take effect.</span></span>
  
 <span data-ttu-id="d128c-138">**P. A filtragem de email em massa é habilitada automaticamente?**</span><span class="sxs-lookup"><span data-stu-id="d128c-138">**Q. Is bulk email filtering automatically enabled?**</span></span>
  
<span data-ttu-id="d128c-p109">R. por padrão, o **email em massa** avançadas a opção de filtragem de spam é habilitada para novos clientes. Para clientes migrados, essa configuração isso coincidirá com a sua configuração do FOPE. Para obter mais informações sobre emails em massa, consulte [qual é a diferença entre lixo eletrônico e email em massa?](what-s-the-difference-between-junk-email-and-bulk-email.md)</span><span class="sxs-lookup"><span data-stu-id="d128c-p109">A. By default, the **Bulk mail** advanced spam filtering option is enabled for new customers. For migrated customers, this setting will match your FOPE configuration. For more information about bulk email, see [What's the difference between junk email and bulk email?](what-s-the-difference-between-junk-email-and-bulk-email.md)</span></span>
  
 <span data-ttu-id="d128c-143">**P. O serviço oferece filtragem de URL?**</span><span class="sxs-lookup"><span data-stu-id="d128c-143">**Q. Does the service provide URL filtering?**</span></span>
  
<span data-ttu-id="d128c-p110">R. Sim, o serviço possui um filtro de URL que verifica se há URLs nas mensagens. Se forem detectadas URLs associadas a spam ou conteúdo malicioso conhecido, a mensagem será marcada como spam.</span><span class="sxs-lookup"><span data-stu-id="d128c-p110">A. Yes the service has a URL filter that checks for URLs within messages. If URLs associated with known spam or malicious content are detected then the message is marked as spam.</span></span>
  
 <span data-ttu-id="d128c-147">**P. Como os clientes que utilizam o serviço podem enviar falsos negativos (spam) e falsos positivos (não spam) para a Microsoft?**</span><span class="sxs-lookup"><span data-stu-id="d128c-147">**Q. How can customers using the service send false negative (spam) and false positive (non-spam) messages to Microsoft?**</span></span>
  
<span data-ttu-id="d128c-p111">R. mensagens de Spam e não spam podem ser enviadas à Microsoft para análise de várias maneiras. Para obter mais informações, consulte o [envio de spam, não spam e mensagens de golpes de phishing à Microsoft para análise](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="d128c-p111">A. Spam and non-spam messages can be submitted to Microsoft for analysis in several ways. For more information, see [Submit spam, non-spam, and phishing scam messages to Microsoft for analysis](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md).</span></span> 
  
 <span data-ttu-id="d128c-151">**P. Posso obter relatórios de spam?**</span><span class="sxs-lookup"><span data-stu-id="d128c-151">**Q. Can I get spam reports?**</span></span>
  
<span data-ttu-id="d128c-p112">R. Sim, por exemplo você pode obter um relatório de detecção de spam no Centro de administração do Office 365. Este relatório mostra o volume de spam como uma contagem de mensagens exclusivas. Para obter mais informações sobre os relatórios, consulte os seguintes links:</span><span class="sxs-lookup"><span data-stu-id="d128c-p112">A. Yes, for example you can get a spam detection report in the Office 365 admin center. This report shows spam volume as a count of unique messages. For more information about reporting, see the following links:</span></span>
  
<span data-ttu-id="d128c-156">Clientes do Exchange Online: [monitoramento, emissão de relatórios e rastreamento no Exchange Online de mensagem](http://technet.microsoft.com/library/87bdeeae-bd80-4a3b-95c5-62fbaf97c2e8.aspx)</span><span class="sxs-lookup"><span data-stu-id="d128c-156">Exchange Online customers: [Monitoring, Reporting, and Message Tracing in Exchange Online](http://technet.microsoft.com/library/87bdeeae-bd80-4a3b-95c5-62fbaf97c2e8.aspx)</span></span>
  
<span data-ttu-id="d128c-157">Os clientes do Exchange Online Protection: [relatórios e rastreamento de mensagens no Exchange Online Protection](eop/reporting-and-message-trace-in-exchange-online-protection.md)</span><span class="sxs-lookup"><span data-stu-id="d128c-157">Exchange Online Protection customers: [Reporting and message trace in Exchange Online Protection](eop/reporting-and-message-trace-in-exchange-online-protection.md)</span></span>
  
 <span data-ttu-id="d128c-158">**P. Alguém me enviou uma mensagem e eu não consigo encontrá-la. Desconfio que ela foi detectada como spam. Existe uma ferramenta que posso usar para descobrir?**</span><span class="sxs-lookup"><span data-stu-id="d128c-158">**Q. Someone sent me a message and I can't find it. I suspect that it may have been detected as spam. Is there a tool that I can use to find out?**</span></span>
  
<span data-ttu-id="d128c-p113">R. Sim, a ferramenta de rastreamento de mensagens permite que você siga as mensagens de email à medida que elas passam pelo serviço, a fim de descobrir o que aconteceu com elas. Para obter mais informações sobre como usar a ferramenta de rastreamento de mensagens para descobrir por que uma mensagem foi marcada como spam, consulte [Uma mensagem foi marcada como spam?](http://technet.microsoft.com/library/aa49e3f9-a5b1-4410-aac2-ddbbf3f5bfb2.aspx#BKMB_Whywasamessagemarkedasspam)</span><span class="sxs-lookup"><span data-stu-id="d128c-p113">A. Yes, the message trace tool enables you to follow email messages as they pass through the service, in order to find out what happened to them. For more information about how to use the message trace tool to find out why a message was marked as spam, see [Was a message marked as spam? ](http://technet.microsoft.com/library/aa49e3f9-a5b1-4410-aac2-ddbbf3f5bfb2.aspx#BKMB_Whywasamessagemarkedasspam)</span></span>
  
 <span data-ttu-id="d128c-162">**Q. O serviço limitará (limite de taxa) meu email se os meus usuários enviarem spam de saída?**</span><span class="sxs-lookup"><span data-stu-id="d128c-162">**Q. Will the service throttle (rate limit) my mail if my users send outbound spam?**</span></span>
  
<span data-ttu-id="d128c-p114">R. Se mais da metade do email que é enviado de um usuário através do serviço em um determinado período de tempo (por exemplo, por hora), é determinado como spam pelo Office 365, o usuário será bloqueado enviem mensagens. Na maioria dos casos, se uma mensagem de saída é determinada como spam, ela é encaminhada pelo pool de entrega de alto risco, o que reduz a probabilidade de que o pool de saída-IP normal sejam adicionado a uma lista de bloqueios.</span><span class="sxs-lookup"><span data-stu-id="d128c-p114">A. If more than half of the mail that is sent from a user through the service within a certain time frame (for example, per hour), is determined to be spam by Office 365, the user will be blocked from sending messages. In most cases, if an outbound message is determined to be spam, it is routed through the high-risk delivery pool, which reduces the probability of the normal outbound-IP pool being added to a block list.</span></span>
  
<span data-ttu-id="d128c-p115">Você pode enviar uma notificação para um endereço de email especificado quando um remetente for bloqueado, envio de spam de saída. Para obter mais informações sobre essa configuração, consulte [Configure a política de spam de saída](configure-the-outbound-spam-policy.md).</span><span class="sxs-lookup"><span data-stu-id="d128c-p115">You can send a notification to a specified email address when a sender is blocked sending outbound spam. For more information about this setting, see [Configure the outbound spam policy](configure-the-outbound-spam-policy.md).</span></span>
  
 <span data-ttu-id="d128c-168">**P. Posso usar um provedor de antispam e antimalware de terceiros em conjunto com o Exchange Online?**</span><span class="sxs-lookup"><span data-stu-id="d128c-168">**Q. Can I use a third-party anti-spam and anti-malware provider in conjunction with Exchange Online?**</span></span>
  
<span data-ttu-id="d128c-p116">R. Sim, você pode configurar outro serviço de filtragem de spam e malwares para proteger suas caixas de correio do Exchange Online. Para fazer isso para emails de entrada, você deve redirecionar suas mensagens para o provedor de terceiros, alterando os registros MX para que apontem para o provedor de terceiros e, em seguida, redirecione as mensagens para o EOP para processamento adicional. Para fazer isso para emails de saída, configure o destino de entrega de mensagem para o provedor de terceiros (host inteligente), conforme mostrado em [Scenario: Outbound Smart Hosting](http://technet.microsoft.com/library/431b3f02-4efd-4bd3-94e7-eecd03f8ef5e.aspx).</span><span class="sxs-lookup"><span data-stu-id="d128c-p116">A. Yes, you may configure another spam and malware filtering service to protect your Exchange Online mailboxes. To do this for inbound mail, you should redirect your email messages to the third-party provider by changing your MX records to point to the third-party provider, and then redirect the messages to EOP for additional processing. To do this for outbound mail, please configure the message delivery destination to the third-party provider (smart host), as shown in [Scenario: Outbound Smart Hosting](http://technet.microsoft.com/library/431b3f02-4efd-4bd3-94e7-eecd03f8ef5e.aspx).</span></span>
  
 <span data-ttu-id="d128c-173">**P. A Microsoft possui alguma documentação sobre como eu posso me proteger contra golpes de phishing?**</span><span class="sxs-lookup"><span data-stu-id="d128c-173">**Q. Does Microsoft have any documentation about how I can protect myself from phishing scams?**</span></span>
  
<span data-ttu-id="d128c-p117">P. Sim. Veja estes artigos:</span><span class="sxs-lookup"><span data-stu-id="d128c-p117">A. Yes we do, please consult the following articles:</span></span>
  
[<span data-ttu-id="d128c-176">Obtenha ajuda contra golpes de phishing, fraude da loteria e outros tipos de golpes</span><span class="sxs-lookup"><span data-stu-id="d128c-176">Get help with phishing scams, lottery fraud, and other types of scams</span></span>](http://go.microsoft.com/fwlink/p/?LinkId=325606)
  
[<span data-ttu-id="d128c-177">Golpes de web e email: Como ajudar você a se proteger</span><span class="sxs-lookup"><span data-stu-id="d128c-177">Email and web scams: How to help protect yourself</span></span>](http://go.microsoft.com/fwlink/p/?LinkID=325607)
  
 <span data-ttu-id="d128c-178">**P. As mensagens de spam e malware são investigadas para identificar quem as enviou ou são transferidas para entidades legais?**</span><span class="sxs-lookup"><span data-stu-id="d128c-178">**Q. Are spam and malware messages being investigated as to who sent them, or being transferred to law enforcement entities?**</span></span>
  
<span data-ttu-id="d128c-p118">R. O objetivo do serviço é detectar e remover spam e malware, embora possamos, de vez em quando, investigar campanhas de spam ou de ataque particularmente perigosas ou prejudiciais, e processar legalmente os responsáveis. Isso pode envolver o trabalho conjunto com unidades legais de combate ao crime digital, para derrubar a botnet de um remetente de spam, impedir que o remetente de spam utilize o serviço (caso esteja usando o serviço para enviar emails) e passar informações à polícia para fins de processo criminal.</span><span class="sxs-lookup"><span data-stu-id="d128c-p118">A. The service focuses on spam and malware detection and removal, though we may occasionally investigate especially dangerous or damaging spam or attack campaigns and pursue the perpetrators. This may involve working with our legal and digital crime units to take down a spammer botnet, blocking the spammer from using the service (if they're using it for sending outbound email), and passing the information on to law enforcement for criminal prosecution.</span></span>
  
 <span data-ttu-id="d128c-182">**P. O que é um conjunto de práticas recomendadas de email de saída que garante que o meu email seja entregue?**</span><span class="sxs-lookup"><span data-stu-id="d128c-182">**Q. What are a set of best outbound mailing practices that will ensure that my mail is delivered?**</span></span>
  
<span data-ttu-id="d128c-p119">R. As diretrizes apresentadas abaixo são as práticas recomendas para o envio de mensagens de email de saída.</span><span class="sxs-lookup"><span data-stu-id="d128c-p119">A. The guidelines presented below are best practices for sending outbound email messages.</span></span>
  
1. <span data-ttu-id="d128c-185">**O domínio de envio do email deve resolver em DNS.**</span><span class="sxs-lookup"><span data-stu-id="d128c-185">**The sending domain of the email should resolve in DNS.**</span></span>
    
    <span data-ttu-id="d128c-p120">Por exemplo, se o remetente for user@example.com, o domínio exemplo.com resolve o endereço IP 192.0.43.10. Se um domínio de envio não tem nenhum registro e nenhum registro MX no DNS, o serviço roteará a mensagem por meio do seu pool de entrega de risco mais alto independentemente de estarem ou não o conteúdo da mensagem é spam. Para obter mais informações sobre o pool de entrega de risco mais alto, consulte o [pool de alto risco de entrega para mensagens de saída](high-risk-delivery-pool-for-outbound-messages.md).</span><span class="sxs-lookup"><span data-stu-id="d128c-p120">For example, if the sender is user@example.com, the domain example.com resolves to the IP address 192.0.43.10. If a sending domain has no A-record and no MX record in DNS, the service will route the message through its higher risk delivery pool regardless of whether or not the content of the message is spam. For more information about the higher risk delivery pool, see [High-risk delivery pool for outbound messages](high-risk-delivery-pool-for-outbound-messages.md).</span></span> 
    
2. <span data-ttu-id="d128c-189">**O endereço IP de envio do servidor de email de saída deve ter uma entrada de DNS reverso (PTR).**</span><span class="sxs-lookup"><span data-stu-id="d128c-189">**The sending IP address of the outbound mail server should have a reverse DNS (PTR) entry.**</span></span>
    
    <span data-ttu-id="d128c-190">Por exemplo, se o envio for do endereço IP 192.0.43.10, a entrada de DNS reverso deste IP é 43-10.any.icann.org.</span><span class="sxs-lookup"><span data-stu-id="d128c-190">For example, if sending from the IP address 192.0.43.10, the reverse DNS entry for this IP is 43-10.any.icann.org.</span></span> 
    
3. <span data-ttu-id="d128c-191">**Os comandos HELO/EHLO e MAIL FROM devem ser consistentes e estar presentes na forma de um nome de domínio em vez de um endereço IP.**</span><span class="sxs-lookup"><span data-stu-id="d128c-191">**The HELO/EHLO and MAIL FROM commands should be consistent and be present in the form of a domain name rather than an IP address.**</span></span>
    
    <span data-ttu-id="d128c-192">O comando HELO/EHLO deve ser configurado para corresponder com o DNS reverso do endereço IP de envio para que o domínio continue o mesmo nas diversas partes dos cabeçalhos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="d128c-192">The HELO/EHLO command should be configured to match the reverse DNS of the sending IP address so that the domain remains the same across the various parts of the message headers.</span></span>
    
4. <span data-ttu-id="d128c-193">**Certifique-se de que os registros SPF adequados estejam configurados no DNS.**</span><span class="sxs-lookup"><span data-stu-id="d128c-193">**Ensure that proper SPF records are set up in DNS.**</span></span>
    
    <span data-ttu-id="d128c-p121">Os registros SPF são um mecanismo para a validação de que os emails enviados de um domínio realmente vêm desse domínio e de que os emails não são falsificados. Para obter mais informações sobre registros SPF, consulte os seguintes links:</span><span class="sxs-lookup"><span data-stu-id="d128c-p121">SPF records are a mechanism for validating that mail sent from a domain really is coming from that domain and is not spoofed. For more information about SPF records, see the following links:</span></span>
    
    [<span data-ttu-id="d128c-196">Configurar o SPF no Office 365 para ajudar a evitar falsificações</span><span class="sxs-lookup"><span data-stu-id="d128c-196">Set up SPF in Office 365 to help prevent spoofing</span></span>](set-up-spf-in-office-365-to-help-prevent-spoofing.md)
    
    [<span data-ttu-id="d128c-197">Criar registros DNS do Office 365</span><span class="sxs-lookup"><span data-stu-id="d128c-197">Create DNS records for Office 365</span></span>](https://go.microsoft.com/fwlink/?LinkID=275414)
    
5. <span data-ttu-id="d128c-198">**Assinatura de email com DKIM, assinar com canonização relaxada.**</span><span class="sxs-lookup"><span data-stu-id="d128c-198">**Signing email with DKIM, sign with relaxed canonicalization.**</span></span>
    
    <span data-ttu-id="d128c-p122">Se um remetente deseja assinar suas mensagens usando o Email Identificado por Chaves de Domínio (DKIM) e desejam enviar mensagens de saída pelo serviço, eles devem assinar usando o algoritmo de canonização de cabeçalho relaxada. Assinar com canonização de cabeçalho estrita pode invalidar a assinatura quando ela passar pelo serviço.</span><span class="sxs-lookup"><span data-stu-id="d128c-p122">If a sender wants to sign their messages using Domain Keys Identified Mail (DKIM) and they want to send outbound mail through the service, they should sign using the relaxed header canonicalization algorithm. Signing with strict header canonicalization may invalidate the signature when it passes through the service.</span></span>
    
6. <span data-ttu-id="d128c-201">**Os proprietários do domínio devem ter informações precisas no banco de dados WHOIS.**</span><span class="sxs-lookup"><span data-stu-id="d128c-201">**Domain owners should have accurate information in the WHOIS database.**</span></span>
    
    <span data-ttu-id="d128c-202">Isso identifica os proprietários do domínio e como contatá-los inserindo a empresa pai estável, ponto de contato e servidores de nome.</span><span class="sxs-lookup"><span data-stu-id="d128c-202">This identifies the owners of the domain and how to contact them by entering the stable parent company, point of contact, and name servers.</span></span>
    
7. <span data-ttu-id="d128c-203">**Para remetentes de mala direta, o nome De: deve refletir quem está enviando a mensagem e a linha de assunto da mensagem deve ser um resumo breve do assunto da mensagem.**</span><span class="sxs-lookup"><span data-stu-id="d128c-203">**For bulk mailers, the From: name should reflect who is sending the message, while the subject line of the message should be a brief summary on what the message is about.**</span></span>
    
    <span data-ttu-id="d128c-p123">O corpo da mensagem deve ter uma indicação clara da oferta, serviço ou produto. Por exemplo, se um remetente estiver enviando uma mala direta para a empresa Contoso, veja a seguir como deverão ficar os campos De e Assunto:</span><span class="sxs-lookup"><span data-stu-id="d128c-p123">The message body should have a clear indication of the offering, service, or product. For example, if a sender is sending out a bulk mailing for the Contoso company, the following is what the email From and Subject should resemble:</span></span>
    
    <span data-ttu-id="d128c-206">De: marketing@contoso.com</span><span class="sxs-lookup"><span data-stu-id="d128c-206">From: marketing@contoso.com</span></span>
    
    <span data-ttu-id="d128c-207">Assunto: Novo catálogo atualizado para a temporada de Natal!</span><span class="sxs-lookup"><span data-stu-id="d128c-207">Subject: New updated catalog for the Christmas season!</span></span> 
    
    <span data-ttu-id="d128c-208">Veja a seguir é um exemplo do que não fazer, porque isso não é descritivo:</span><span class="sxs-lookup"><span data-stu-id="d128c-208">The following is an example of what not to do because it is not descriptive:</span></span>
    
    <span data-ttu-id="d128c-209">De: usuário@hotmail.com</span><span class="sxs-lookup"><span data-stu-id="d128c-209">From: user@hotmail.com</span></span>
    
    <span data-ttu-id="d128c-210">Assunto: Catálogos</span><span class="sxs-lookup"><span data-stu-id="d128c-210">Subject: Catalogs</span></span>
    
8. <span data-ttu-id="d128c-211">**Se for enviar uma mala direta para vários destinatários e a mensagem estiver em formato de boletim informativo, deve haver uma maneira de cancelar a assinatura na parte inferior da mensagem.**</span><span class="sxs-lookup"><span data-stu-id="d128c-211">**If sending a bulk mailing to many recipients and the message is in newsletter format, there should be a way of unsubscribing at the bottom of the message.**</span></span>
    
    <span data-ttu-id="d128c-212">A opção de cancelamento da assinatura deve ter a seguinte aparência:</span><span class="sxs-lookup"><span data-stu-id="d128c-212">The unsubscribe option should resemble the following:</span></span>
    
    <span data-ttu-id="d128c-p124">Esta mensagem foi enviada para exemplo@contoso.com por remetente@fabrikam.com. Atualizar Perfil/Endereço de Email | Remoção Instantânea com **SafeUnsubscribe** | Política de privacidade</span><span class="sxs-lookup"><span data-stu-id="d128c-p124">This message was sent to example@contoso.com by sender@fabrikam.com. Update Profile/Email Address | Instant removal with **SafeUnsubscribe**™ | Privacy Policy</span></span>
    
9. <span data-ttu-id="d128c-215">**Se for enviar uma mala direta, a aquisição da lista deve ser realizada utilizando double opt-in. Se você for remetente de mala direta, o double opt-in é uma prática recomendada da indústria.**</span><span class="sxs-lookup"><span data-stu-id="d128c-215">**If sending bulk email, list acquisition should be performed using double opt-in. If you are a bulk mailer, double opt-in is an industry best practice.**</span></span>
    
    <span data-ttu-id="d128c-216">O Double opt-in é a prática que exige que um usuário passe por dois processos para confirmar o recebimento de correio de marketing:</span><span class="sxs-lookup"><span data-stu-id="d128c-216">Double opt-in is the practice of requiring a user to take two actions to sign up for marketing mail:</span></span>
    
1. <span data-ttu-id="d128c-217">No primeiro processo, o usuário clica em uma caixa de seleção desmarcada anteriormente, onde ele opta por receber mais ofertas ou mensagens de email do comerciante.</span><span class="sxs-lookup"><span data-stu-id="d128c-217">Once when the user clicks on a previously unchecked check box where they opt-in to receive further offers or email messages from the marketer.</span></span>
    
2. <span data-ttu-id="d128c-218">No segundo processo, o comerciante envia um email de confirmação para o endereço de email do usuário, pedindo que ele clique em um link com limite de tempo para concluir a confirmação.</span><span class="sxs-lookup"><span data-stu-id="d128c-218">A second time when the marketer sends a confirmation email to the user's provided email address asking them to click on a time-sensitive link that will complete their confirmation.</span></span>
    
    <span data-ttu-id="d128c-219">Usar o double opt-in ajuda a formar uma boa reputação para os remetentes de mala direta.</span><span class="sxs-lookup"><span data-stu-id="d128c-219">Using double opt-in builds a good reputation for bulk email senders.</span></span>
    
10. <span data-ttu-id="d128c-220">**Os remetentes de mala direta devem criar conteúdo transparente pelo qual possam ser responsabilizados:**</span><span class="sxs-lookup"><span data-stu-id="d128c-220">**Bulk senders should create transparent content for which they can be held accountable:**</span></span>
    
1. <span data-ttu-id="d128c-221">A verbosidade solicitando que os destinatários adicionem o remetente ao catálogo de endereços deve indicar claramente que tal ação não é uma garantia de entrega.</span><span class="sxs-lookup"><span data-stu-id="d128c-221">Verbiage requesting that recipients add the sender to the address book should clearly state that such action is not a guarantee of delivery.</span></span>
    
2. <span data-ttu-id="d128c-222">Ao construir redirecionamentos no corpo da mensagem, use um estilo de vínculo consistente.</span><span class="sxs-lookup"><span data-stu-id="d128c-222">When constructing redirects in the body of the message, use a consistent link style.</span></span>
    
3. <span data-ttu-id="d128c-223">Não envie imagens nem anexos grandes, nem mensagens compostas por apenas uma imagem.</span><span class="sxs-lookup"><span data-stu-id="d128c-223">Don't send large images or attachments, or messages that are solely composed of an image.</span></span>
    
4. <span data-ttu-id="d128c-224">Ao empregar pixels de rastreamento (bugs da Web ou avisos), indique claramente a presença deles em sua privacidade pública ou configurações P3P.</span><span class="sxs-lookup"><span data-stu-id="d128c-224">When employing tracking pixels (web bugs or beacons), clearly state their presence in your public privacy or P3P settings.</span></span>
    
11. <span data-ttu-id="d128c-225">**Formatar notificações de status de entrega de saída.**</span><span class="sxs-lookup"><span data-stu-id="d128c-225">**Format outbound delivery status notifications.**</span></span>
    
    <span data-ttu-id="d128c-226">Ao gerar as mensagens de notificação de status de entrega, os remetentes devem seguir o formato de uma mensagem de devolução, conforme especificado em [RFC 3464](https://go.microsoft.com/fwlink/?LinkId=279715).</span><span class="sxs-lookup"><span data-stu-id="d128c-226">When generating delivery status notification messages, senders should follow the format of a bounce as specified in [RFC 3464](https://go.microsoft.com/fwlink/?LinkId=279715).</span></span>
    
12. <span data-ttu-id="d128c-227">**Remover endereços de email de devolução para usuários inexistentes.**</span><span class="sxs-lookup"><span data-stu-id="d128c-227">**Remove bounced email addresses for non-existent users.**</span></span>
    
    <span data-ttu-id="d128c-p125">Se você receber uma NDR indicando que um endereço de email não está mais em uso, remova da sua lista o alias de email inexistente. Os endereços de email mudam ao longo do tempo e as pessoas às vezes os descartam.</span><span class="sxs-lookup"><span data-stu-id="d128c-p125">If you receive an NDR indicating that an email address is no longer in use, remove the non-existent email alias from your list. Email addresses change over time, and people sometimes discard them.</span></span>
    
13. <span data-ttu-id="d128c-230">**Use o programa de Serviços de Dados de Rede Inteligente do Hotmail (SNDS) .**</span><span class="sxs-lookup"><span data-stu-id="d128c-230">**Use Hotmail's Smart Network Data Services (SNDS) program.**</span></span>
    
    <span data-ttu-id="d128c-p126">O Hotmail usa um programa chamado Serviços de Dados de Rede Inteligente do Hotmail que permite que os remetentes verifiquem as reclamações enviadas pelos usuários finais. O SNDS é o portal principal para a solução de problemas de entrega ao Hotmail.</span><span class="sxs-lookup"><span data-stu-id="d128c-p126">Hotmail uses a program called Smart Network Data Services that allows senders to check complaints submitted by end users. The SNDS is the primary portal for troubleshooting delivery problems to Hotmail.</span></span>
    
## <a name="for-more-information"></a><span data-ttu-id="d128c-233">Para obter mais informações</span><span class="sxs-lookup"><span data-stu-id="d128c-233">For more information</span></span>

[<span data-ttu-id="d128c-234">Proteção de Anti-Spam de Email do Office 365</span><span class="sxs-lookup"><span data-stu-id="d128c-234">Office 365 Email Anti-Spam Protection</span></span>](https://support.office.com/article/6a601501-a6a8-4559-b2e7-56b59c96a586)
  
[<span data-ttu-id="d128c-235">Remetentes seguros e bloqueados listas de remetentes no Exchange Online</span><span class="sxs-lookup"><span data-stu-id="d128c-235">Safe sender and blocked sender lists in Exchange Online</span></span>](safe-sender-and-blocked-sender-lists-faq.md)
  
[<span data-ttu-id="d128c-236">Cabeçalhos de mensagem antispam</span><span class="sxs-lookup"><span data-stu-id="d128c-236">Anti-spam message headers</span></span>](anti-spam-message-headers.md)
  
[<span data-ttu-id="d128c-237">Mnsagens backscatter e EOP</span><span class="sxs-lookup"><span data-stu-id="d128c-237">Backscatter messages and EOP</span></span>](backscatter-messages-and-eop.md)
  


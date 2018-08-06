---
title: Solucionando problemas de email enviadas para o Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/2/2016
ms.audience: ITPro
ms.topic: troubleshooting
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: f4caa4e1-e414-4b21-8822-31c08064c059
description: Este artigo fornece informações de solução de problemas para os remetentes que estão enfrentando problemas ao tentar enviar email para caixas de entrada no Office 365 e práticas recomendadas para mala direta para os clientes do Office 365.
ms.openlocfilehash: 29c30787f493c69eb7d42b8025b25c86acddfff9
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026408"
---
# <a name="troubleshooting-mail-sent-to-office-365"></a>Solucionando problemas de email enviadas para o Office 365

Este artigo fornece informações de solução de problemas para os remetentes que estão enfrentando problemas ao tentar enviar email para caixas de entrada no Office 365 e práticas recomendadas para mala direta para os clientes do Office 365.
  
## <a name="troubleshooting-common-problems-with-mail-delivery-to-office-365"></a>Solução de problemas comuns com a entrega de email para o Office 365

Escolha um desses problemas comumente encontrados.
  
- [Você está gerenciando seus IP e do domínio enviando reputação?](troubleshooting-mail-sent-to-office-365.md#ManageRep)
    
- [São enviar e-mails de novos endereços IP?](troubleshooting-mail-sent-to-office-365.md#NewIPs)
    
- [Confirme se o DNS está configurado corretamente](troubleshooting-mail-sent-to-office-365.md#ConfirmDNSsetup)
    
- [Certifique-se de que você não anuncie si mesmo como um IP não roteáveis](troubleshooting-mail-sent-to-office-365.md#NoReverseDNS)
    
- [Você recebeu um relatório de falha na entrega (NDR) ao enviar email a um usuário no Office 365](troubleshooting-mail-sent-to-office-365.md#NDRInbound)
    
- [Meu e-mail trouxe na pasta de lixo eletrônico do destinatário no EOP](troubleshooting-mail-sent-to-office-365.md#JunkMailBox)
    
- [Tráfego do meu endereço IP seja restringido pelo EOP](troubleshooting-mail-sent-to-office-365.md#AllowEOPIPs)
    
### <a name="are-you-managing-your-ip-and-domains-sending-reputation"></a>Você está gerenciando seus IP e do domínio enviando reputação?
<a name="ManageRep"> </a>

Tecnologias de filtragem do EOP são projetadas para fornecer recursos anti-spam proteções para Microsoft Office 365, bem como outros produtos da Microsoft como Windows Live Mail, Microsoft Office Outlook e Exchange Server. Também podemos aproveitar SPF, DKIM e DMARC; email tecnologias de autenticação que ajudam a solucionar o problema de falsificação e phishing, confirmando que o domínio enviando email está autorizado a fazê-lo. Filtragem do EOP é influenciada por um número de fatores relacionados para o IP de envio, domínio, autenticação, precisão de lista, taxas de reclamações, conteúdo e muito mais. Desses, um da entidade de segurança os fatores que baixam reputação do remetente e sua capacidade de oferecer o email é seu taxa de compatível com de lixo eletrônico. 
  
### <a name="are-you-sending-email-from-new-ip-addresses"></a>São enviar e-mails de novos endereços IP?
<a name="NewIPs"> </a>

Endereços IP não anteriormente usados para enviar email normalmente não têm qualquer reputação criada em nossos sistemas. Como resultado, emails do novo IPs são mais prováveis ter problemas de entrega. Depois que o IP tiver construído uma reputação por não enviem spam, normalmente permitirá EOP para uma melhor experiência de entrega de email.
  
Novo IPs que são adicionadas aos domínios que são autenticados em registros existentes de SPF geralmente experimentar o benefício adicional de herdando algumas das reputação do remetente do domínio. Se o domínio tiver uma boa reputação de envio IPs novo perceba uma tempo mais rápido de participação. Um novo IP pode esperar ser aumentada totalmente em algumas semanas ou mais cedo dependendo de volume, precisão de lista e taxas de reclamações de lixo eletrônico.
  
### <a name="confirm-that-your-dns-is-set-up-correctly"></a>Confirme se o DNS está configurado corretamente
<a name="ConfirmDNSsetup"> </a>

Para obter instruções sobre como criar e manter registros DNS, incluindo o registro MX necessário para roteamento de email, você precisará entrar em contato com seu provedor de hospedagem de DNS.
  
### <a name="ensure-that-you-do-not-advertise-yourself-as-a-non-routable-ip"></a>Certifique-se de que você não anuncie si mesmo como um IP não roteáveis
<a name="NoReverseDNS"> </a>

Podemos pode não aceitar emails de remetentes que falham uma pesquisa de DNS reverso. Em alguns casos, remetentes legítimos anunciam-se incorretamente como um IP roteável de não-internet ao tentar abrir uma conexão para o EOP. Endereços IP que são reservados para uma rede privada (não roteáveis) incluem:
  
- 192.168.0.0/16 (ou 192.168.0.0 - 192.168.255.255)
    
- 10.0.0.0/8 (ou 10.0.0.0 - 10.255.255.255)
    
- 172.16.0.0/11 (ou 172.16.0.0 - 172.31.255.255)
    
### <a name="you-received-a-non-delivery-report-ndr-when-sending-email-to-a-user-in-office-365"></a>Você recebeu um relatório de falha na entrega (NDR) ao enviar email a um usuário no Office 365
<a name="NDRInbound"> </a>

Alguns problemas de entrega são o resultado de endereço IP do remetente estão sendo bloqueado pela Microsoft ou porque a conta de usuário é identificada como remetente proibido devido à atividade de spam anterior. Se você acredita que você recebeu o NDR em erro, primeiro siga as instruções na mensagem de notificação de falha para resolver o problema. 
  
Para obter mais informações sobre o erro que você recebeu, consulte a lista completa dos códigos de erro do SMTP no [DSNs e NDRs no Exchange 2013 no local e o Office 365](http://technet.microsoft.com/library/8e91de84-76fa-49b2-898c-c5eface76560.aspx).
  
 Por exemplo, se você receber os seguintes NDR, indica que o endereço IP de envio foi bloqueado pelo Microsoft. 
  
 `550 5.7.606-649 Access denied, banned sending IP [x.x.x.x]; To request removal from this list please visit https://sender.office.com/ and follow the directions.`
  
Para solicitar a remoção dessa lista, você pode [usar o portal delist para remover seu nome na lista de remetentes bloqueados do Office 365](use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis.md).
  
### <a name="my-email-landed-in-the-recipients-junk-folder-in-eop"></a>Meu e-mail trouxe na pasta de lixo eletrônico do destinatário no EOP
<a name="JunkMailBox"> </a>

Se uma mensagem foi incorretamente identificada como spam pelo EOP, você pode trabalhar com o destinatário para enviar essa mensagem de falsa positiva à equipe de análise do Spam da Microsoft, que irá avaliar e analisar a mensagem. Dependendo dos resultados da análise, as regras de filtro de conteúdo de spam de todo o serviço podem ser ajustadas para permitir que a mensagem pelo. Você usa o email para enviar mensagens para a Microsoft não devem ser classificadas como spam. Ao fazer isso, certifique-se de usar as etapas no procedimento a seguir.
  
### <a name="to-use-email-to-submit-false-positive-messages-to-the-microsoft-spam-analysis-team"></a>Usar o e-mail para enviar mensagens de falso positivo à equipe de análise de Spam da Microsoft

1. Salve a mensagem que deseja enviar como não spam.
    
2. Crie uma nova mensagem em branco e anexe a ela a mensagem que não é spam.
    
    Se necessário, você pode anexar várias mensagens não spam.
    
3. Copie e cole a linha de assunto da mensagem original na linha de assunto da nova mensagem.
    
    > [!IMPORTANT]
    > Deixe o corpo da nova mensagem vazio. 
  
4. Envie a mensagem para [not_junk@office365.microsoft.com](mailto:not_junk@office365.microsoft.com).
    
### <a name="traffic-from-my-ip-address-is-throttled-by-eop"></a>Tráfego do meu endereço IP seja restringido pelo EOP
<a name="AllowEOPIPs"> </a>

Se você receber uma notificação de falha do EOP que indica que seu endereço IP está sendo limitado pelo EOP, por exemplo:
  
 `host xxxx.outlook.com [x.x.x.x]: 451 4.7.550 Access denied, please try again later`
  
Você recebeu o NDR porque foi detectada atividade suspeita do endereço IP e se ele tiver sido restringido temporariamente enquanto ele está sendo avaliado ainda mais. Se o desconfiança estiver desmarcada por meio de avaliação, essa restrição será ser elevada em breve.
  
### <a name="i-cant-receive-email-from-senders-in-office-365"></a>Não consigo receber email dos remetentes no Office 365
<a name="AllowEOPIPs"> </a>

 Para receber mensagens de nossos usuários, certifique-se de que sua rede permite conexões de saída dos endereços IP que EOP usa em nossos centros de dados. Para obter mais informações, consulte [endereços IP do Exchange Online Protection](eop/exchange-online-protection-ip-addresses.md). Para um registro de IP de todos os endereços que foram adicionados, alterados ou preteridos no ano passado, consulte a [notificação de alteração de endereços IP do EOP](eop/change-notification-for-eop-ip-addresses.md).
  
## <a name="best-practices-for-bulk-emailing-to-office-365-users"></a>Práticas recomendadas para um email em massa, aos usuários do Office 365
<a name="BulkMailer"> </a>

Se você geralmente conduzir campanhas de email em massa para usuários do Office 365 e para assegurar que seus emails chegarem na maneira segura e em tempo hábil, siga as dicas nesta seção.
  
### <a name="ensure-that-the-from-name-reflects-who-is-sending-the-message"></a>Certifique-se de que as From: nome reflete o que está enviando a mensagem

O assunto deve ser um breve resumo dos qual a mensagem é sobre e o corpo da mensagem deve claramente e sucinta indicam o que é a oferta, serviço ou produto sobre. Por exemplo:
  
Corrigir
  
 ` From: marketing@shoppershandbag.com `
  
 `Subject: Updated catalog for the Christmas season!`
  
Incorreto
  
 `From: someone@outlook.com`
  
 `Subject: Catalogs`
  
Mais fácil torná-lo para as pessoas saibam quem você é e o que está fazendo, a menos dificuldade terá como entregar a maioria dos filtros de spam.
  
### <a name="always-include-an-unsubscribe-option-in-campaign-emails"></a>Sempre incluir uma opção de cancelamento da assinatura em emails de campanha

Emails de marketing, especialmente boletins informativos, deve sempre incluir uma maneira de cancelar a assinatura de emails futuros. Por exemplo:
  
 `This email was sent to example@contoso.com by sender@fabrikam.com.`
  
 `Update Profile/Email Address | Instant removal with SafeUnsubscribe™ | Privacy Policy`
  
Alguns remetentes incluem essa opção, exigindo destinatários enviar um email para um determinado alias com "Cancelar inscrição" no assunto. Isso não é preferível o exemplo de um clique acima. Se você escolher exigir que os destinatários enviar um email, certifique-se de que, quando eles clicarem no link, todos os campos necessários são preenchidos previamente.
  
### <a name="use-the-double-opt-in-option-for-marketing-email-or-newsletter-registration"></a>Use a opção double opt-in para registro de email ou o boletim informativo de marketing

Essa prática recomendada do setor recomenda-se sua empresa requer ou incentiva os usuários para registrar as informações de contato para acessar seus produtos ou serviços. Algumas empresas tornam uma prática Inscreva-se automaticamente se seus usuários para emails de marketing ou f boletins informativos durante o processo de registro, mas isso é considerado uma prática de marketing questionável no mundo da filtragem de email.
  
Durante o processo de registro, se o de "Sim, Oriente-me o boletim informativo" ou "Sim, Oriente-me ofertas especiais" caixa de seleção é marcada por padrão, os usuários que não preste atenção acidentalmente poderão desconectá para marketing de email ou boletins informativos que não tiverem deseja receber.
  
 É recomendável a opção double opt-in em vez disso, que significa que a caixa de seleção para emails de marketing ou boletins informativos está desmarcada por padrão. Além disso, depois que o formulário de registro tiver sido enviado, um email de verificação é enviado ao usuário com uma URL que permite que eles confirmar sua decisão para receber emails de marketing. 
  
 Isso ajuda a garantir que somente os usuários que desejam receber email marketing são inscreveu para emails, subsequentemente desmarcar a empresa de envio de qualquer email questionável práticas de marketing. 
  
### <a name="ensure-that-email-message-content-is-transparent-and-traceable"></a>Certifique-se de que o conteúdo da mensagem de email é transparente e rastreável

Apenas tão importante quanto a maneira como os emails são enviados é o conteúdo que eles contêm. Ao criar o conteúdo de email, use as seguintes práticas recomendadas para garantir que seus emails não serão sinalizadas pelo serviços de filtragem de email:
  
- Quando a mensagem de email solicita que os destinatários adicionem o remetente ao catálogo de endereços, ele deve indicar claramente que tal ação não é uma garantia de entrega.
    
- Redirecionamentos incluídos no corpo da mensagem devem ser semelhante e consistente e não vários e variados. Um redirecionamento nesse contexto é qualquer coisa que aponta para longe da mensagem, links e documentos. Se você tiver muitos anúncios ou links de cancelamento da assinatura ou atualizar os vínculos de perfil, eles devem apontar para o mesmo domínio. Por exemplo:
    
    Corrigir
    
     `unsubscribe.bulkmailer.com`
    
     `profile.bulkmailer.com`
    
     `options.bulkmailer.com`
    
    Incorreto
    
     `unsubscribe.bulkmailer.com`
    
     `profiles.excite.com`
    
     `options.yahoo.com`
    
- Evite conteúdo com imagens grandes e anexos ou mensagens que são compostas por apenas uma imagem.
    
- Sua privacidade pública ou configurações P3P devem indicar claramente a presença de acompanhamento pixels (bugs da web ou avisos).
    
### <a name="remove-incorrect-email-aliases-from-your-databases"></a>Remover os aliases de email incorreto de seus bancos de dados

Qualquer alias de email em seu banco de dados que cria um retorno é desnecessário e coloca os seus emails de saída em risco para maiores investigações pelos serviços de filtragem de email. Certifique-se de que seu banco de dados de email seja atualizado.
  


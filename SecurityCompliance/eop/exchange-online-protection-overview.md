---
title: Visão geral do Exchange Online Protection
ms.author: tracyp
author: MSFTTracyp
manager: laurawi
ms.date: 01/31/2019
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 1270a65f-ddc3-4430-b500-4d3a481efb1e
description: O Microsoft Proteção do Exchange Online (EOP) é um serviço de filtragem de e-mails baseado na nuvem que ajuda a proteger sua organização contra spam e malware, e inclui recursos para defender sua organização das violações da política de mensagens.
ms.openlocfilehash: 16f2f423b6e517cf204e4b4f6a2949baebfd6223
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29686360"
---
# <a name="exchange-online-protection-overview"></a><span data-ttu-id="8fde3-103">Visão geral do Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="8fde3-103">Exchange Online Protection overview</span></span>

<span data-ttu-id="8fde3-p101">O Microsoft Proteção do Exchange Online (EOP) é um serviço de filtragem de email com base na nuvem que ajuda a proteger sua organização contra spam e malware e inclui recursos para proteger sua organização contra violações da política de envio de mensagens. O EOP pode simplificar o gerenciamento de seu ambiente de mensagens e aliviar muitos dos fardos que acompanham a manutenção de hardware e software locais.</span><span class="sxs-lookup"><span data-stu-id="8fde3-p101">Microsoft Exchange Online Protection (EOP) is a cloud-based email filtering service that helps protect your organization against spam and malware, and includes features to safeguard your organization from messaging-policy violations. EOP can simplify the management of your messaging environment and alleviate many of the burdens that come with maintaining on-premises hardware and software.</span></span>
  
<span data-ttu-id="8fde3-106">Veja a seguir algumas das principais formas de usar o EOP para proteção de mensagens:</span><span class="sxs-lookup"><span data-stu-id="8fde3-106">The following are the primary ways you can use EOP for messaging protection:</span></span>
  
- <span data-ttu-id="8fde3-107">**Em um cenário autônomo** EOP fornece proteção de email baseada em nuvem para seu ambiente do Microsoft Exchange Server 2013 local, versões herdadas do Exchange Server, ou para qualquer outro local a solução de email SMTP.</span><span class="sxs-lookup"><span data-stu-id="8fde3-107">**In a standalone scenario** EOP provides cloud-based email protection for your on-premises Microsoft Exchange Server 2013 environment, legacy Exchange Server versions, or for any other on-premises SMTP email solution.</span></span> 
    
- <span data-ttu-id="8fde3-108">**Como parte do Microsoft Exchange Online** Por padrão, o EOP protege caixas de correio do Microsoft Exchange Online hospedadas na nuvem.</span><span class="sxs-lookup"><span data-stu-id="8fde3-108">**As a part of Microsoft Exchange Online** By default, EOP protects Microsoft Exchange Online cloud-hosted mailboxes.</span></span> 
    
- <span data-ttu-id="8fde3-109">**Em uma implantação híbrida** O EOP pode ser configurado para proteger seu ambiente de mensagens e controlar o roteamento de email quando você tem uma combinação de caixas de correio locais e na nuvem.</span><span class="sxs-lookup"><span data-stu-id="8fde3-109">**In a hybrid deployment** EOP can be configured to protect your messaging environment and control mail routing when you have a mix of on-premises and cloud mailboxes.</span></span> 
    
## <a name="how-eop-works"></a><span data-ttu-id="8fde3-110">Como o EOP funciona</span><span class="sxs-lookup"><span data-stu-id="8fde3-110">How EOP works</span></span>

<span data-ttu-id="8fde3-111">Para entender como o EOP funciona, ele o ajuda a ver como processa o email de entrada:</span><span class="sxs-lookup"><span data-stu-id="8fde3-111">To understand how EOP works, it helps to see how it processes incoming email:</span></span>
  
![Processamento de email do EOP](../media/EOP-email-processing.png)
  
<span data-ttu-id="8fde3-p102">Mensagem recebida inicialmente passa por meio de filtragem de conexão, que verifica a reputação do remetente e inspeciona a mensagem para o malware. A maioria dos spam é interrompida nesse momento e excluída pelo EOP. Mensagens continuam pela filtragem de política, onde as mensagens são avaliadas pelas regras de transporte personalizado que você cria ou impor a partir de um modelo. Por exemplo, você pode ter uma regra que envia uma notificação para um gerente quando um email chega de um remetente específico. (Verificações de prevenção de perda de dados também ocorrem neste ponto, se você tiver que apresentam; para obter informações sobre disponibilidade de recurso, consulte o [Exchange Online Protection Service Description](https://go.microsoft.com/fwlink/p/?LinkId=320619).) Em seguida, mensagens que passam por meio de filtragem de conteúdo, onde o conteúdo é verificado de terminologia ou propriedades comuns como spam. Uma mensagem é determinado como spam pelo filtro de conteúdo pode ser enviada para a pasta de lixo eletrônico do usuário ou para a quarentena, entre outras opções, com base em suas configurações. Depois que uma mensagem passa todas essas camadas de proteção com êxito, ele é entregue ao destinatário.</span><span class="sxs-lookup"><span data-stu-id="8fde3-p102">An incoming message initially passes through connection filtering, which checks the sender's reputation and inspects the message for malware. The majority of spam is stopped at this point and deleted by EOP. Messages continue through policy filtering, where messages are evaluated against custom transport rules that you create or enforce from a template. For example, you can have a rule that sends a notification to a manager when mail arrives from a specific sender. (Data loss prevention checks also occur at this point, if you have that feature; for information about feature availability, see the [Exchange Online Protection Service Description](https://go.microsoft.com/fwlink/p/?LinkId=320619).) Next, messages pass through content filtering, where content is checked for terminology or properties common to spam. A message determined to be spam by the content filter can be sent to a user's Junk Email folder or to the quarantine, among other options, based on your settings. After a message passes all of these protection layers successfully, it's delivered to the recipient.</span></span>
  
### <a name="eop-datacenters"></a><span data-ttu-id="8fde3-120">Datacenters EOP</span><span class="sxs-lookup"><span data-stu-id="8fde3-120">EOP datacenters</span></span>

<span data-ttu-id="8fde3-p103">O EOP é executado em uma rede mundial de data center projetados para fornecer a melhor disponibilidade. Por exemplo, se um data center ficar indisponível, mensagens de email são automaticamente roteadas para um outro data center sem qualquer interrupção no serviço. Os servidores em cada data center aceitam mensagens em seu nome, fornecendo uma camada de separação entre sua organização e a Internet, reduzindo assim a carga em seus servidores. Por meio dessa rede altamente disponível, a Microsoft pode assegurar que esse email chegue a sua organização pontualmente.</span><span class="sxs-lookup"><span data-stu-id="8fde3-p103">EOP runs on a worldwide network of datacenters that are designed to provide the best availability. For example, if a datacenter becomes unavailable, email messages are automatically routed to another datacenter without any interruption in service. Servers in each datacenter accept messages on your behalf, providing a layer of separation between your organization and the Internet, thereby reducing load on your servers. Through this highly available network, Microsoft can ensure that email reaches your organization in a timely manner.</span></span> 
  
<span data-ttu-id="8fde3-p104">EOP realiza balanceamento de carga entre data centers, mas apenas dentro de uma região. Se você for aprovisionado em uma região, todas as suas mensagens serão processadas usando o roteamento de email para essa região. A lista a seguir mostra como o roteamento de email regional funciona para os data centers EOP:</span><span class="sxs-lookup"><span data-stu-id="8fde3-p104">EOP performs load balancing between datacenters but only within a region. If you're provisioned in one region all your messages will be processed using the mail routing for that region. The following list shows the how regional mail routing works for the EOP datacenters:</span></span>
  
    
- <span data-ttu-id="8fde3-128">Na Europa, Oriente Médio e África (EMEA), todas as caixas de correio do Exchange Online são localizadas nos data centers da EMEA e todas as mensagens são roteadas através de data centers da EMEA para filtragem do EOP.</span><span class="sxs-lookup"><span data-stu-id="8fde3-128">In Europe, the Middle East, and Africa (EMEA), all Exchange Online mailboxes are located in EMEA datacenters, and all messages are routed through EMEA datacenters for EOP filtering.</span></span>
    
- <span data-ttu-id="8fde3-129">No Pacífico Asiático (APAC), todas as caixas de correio Exchange Online estão localizadas em datacenters APAC, mas as mensagens são roteadas atualmente por meio de datacenters APAC para filtragem do EOP.</span><span class="sxs-lookup"><span data-stu-id="8fde3-129">In Asia-Pacific (APAC), all Exchange Online mailboxes are located in APAC datacenters, but messages are currently routed through APAC datacenters for EOP filtering.</span></span>
=======
- <span data-ttu-id="8fde3-p105">Américas, todas as caixas de correio Exchange Online estão localizadas em data centers nos EUA, com exceção de onde os data centers no Brasil e Chile são usados na América do Sul e no Canadá, onde os centros de dados no Canadá são usados. Todas as mensagens de email, incluindo mensagens para clientes na América do Sul e no Canadá, são roteadas através de centros de dados locais para filtragem do EOP; email quaratined é armazenado no datacenter onde se encontra o inquilino.</span><span class="sxs-lookup"><span data-stu-id="8fde3-p105">In the Americas, all Exchange Online mailboxes are located in U.S. datacenters, with the exception of South America where datacenters in Brazil and Chile are used and in Canada where datacenters in Canada are used. All email messages, including messages for customers in South America and Canada, are routed through local datacenters for EOP filtering; quaratined email is stored in the datacenter where the tenant is located.</span></span>
    
- <span data-ttu-id="8fde3-132">Na Europa, Oriente Médio e África (EMEA), todas as caixas de correio do Exchange Online são localizadas nos data centers da EMEA e todas as mensagens são roteadas através de data centers da EMEA para filtragem do EOP.</span><span class="sxs-lookup"><span data-stu-id="8fde3-132">In Europe, the Middle East, and Africa (EMEA), all Exchange Online mailboxes are located in EMEA datacenters, and all messages are routed through EMEA datacenters for EOP filtering.</span></span>
    
- <span data-ttu-id="8fde3-133">No Pacífico Asiático (APAC), todas as caixas de correio Exchange Online estão localizadas em datacenters APAC e mensagens atualmente são roteadas através de datacenters APAC para filtragem do EOP.</span><span class="sxs-lookup"><span data-stu-id="8fde3-133">In Asia-Pacific (APAC), all Exchange Online mailboxes are located in APAC datacenters, and messages are currently routed through APAC datacenters for EOP filtering.</span></span>
    
- <span data-ttu-id="8fde3-134">Para a Nuvem de Comunidade Governamental (GCC), todas as caixas de correio do Exchange Online localizadas em data centers dos EUA e todas as mensagens são roteadas através de data centers dos EUA para filtragem do EOP.</span><span class="sxs-lookup"><span data-stu-id="8fde3-134">For the Government Community Cloud (GCC), all Exchange Online mailboxes are located in U.S. datacenters and all messages are routed through U.S. datacenters for EOP filtering.</span></span>
    
## <a name="eop-plans-and-features"></a><span data-ttu-id="8fde3-135">Planos e recursos do EOP</span><span class="sxs-lookup"><span data-stu-id="8fde3-135">EOP plans and features</span></span>

<span data-ttu-id="8fde3-136">Estes são os planos de assinatura disponíveis do EOP:</span><span class="sxs-lookup"><span data-stu-id="8fde3-136">The following are the available EOP subscription plans:</span></span>
  
- <span data-ttu-id="8fde3-137">**EOP autônomo** No qual o EOP protege suas caixas de correio locais.</span><span class="sxs-lookup"><span data-stu-id="8fde3-137">**EOP standalone** Where EOP protects your on-premises mailboxes.</span></span> 
    
- <span data-ttu-id="8fde3-138">**Recursos do EOP no Exchange Online** No qual o EOP protege suas caixas de correio do Exchange Online hospedadas na nuvem.</span><span class="sxs-lookup"><span data-stu-id="8fde3-138">**EOP features in Exchange Online** Where EOP protects your Exchange Online cloud-hosted mailboxes.</span></span> 
    
- <span data-ttu-id="8fde3-139">**Exchange Enterprise CAL com serviços** Em que EOP protege suas caixas de correio locais, como o EOP autônomo, e inclui DLP (prevenção de perda de dados) e relatórios usando serviços da Web.</span><span class="sxs-lookup"><span data-stu-id="8fde3-139">**Exchange Enterprise CAL with Services** Where EOP protects your on-premises mailboxes, like EOP standalone, and includes data loss prevention (DLP) and reporting using web services.</span></span> 
    
<span data-ttu-id="8fde3-140">Para mais informações sobre as exigências, limites importantes e disponibilidade de recursos em todos os planos de assinatura do EOP, consulte a [Descrição do serviço de proteção do Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=320619).</span><span class="sxs-lookup"><span data-stu-id="8fde3-140">For information about requirements, important limits, and feature availability across all EOP subscription plans, see the [Exchange Online Protection Service Description](https://go.microsoft.com/fwlink/p/?LinkId=320619).</span></span>
  
## <a name="setting-up-eop"></a><span data-ttu-id="8fde3-141">Configuração do EOP</span><span class="sxs-lookup"><span data-stu-id="8fde3-141">Setting up EOP</span></span>

<span data-ttu-id="8fde3-p106">A configuração do EOP pode ser simples, especialmente no caso de uma pequena organização com um punhado de regras de conformidade. No entanto, se você tiver uma organização de grande porte com vários domínios, regras de conformidade personalizadas ou fluxo de email híbrido, a configuração pode precisar de mais planejamento e tempo.</span><span class="sxs-lookup"><span data-stu-id="8fde3-p106">Setting up EOP can be simple, especially in the case of a small organization with a handful of compliance rules. However, if you have a large organization with multiple domains, custom compliance rules, or hybrid mail flow, set up can take more planning and time.</span></span>
  
<span data-ttu-id="8fde3-144">Se você já comprou o EOP, consulte [Configurar seu serviço EOP](set-up-your-eop-service.md) para garantir a conclusão de todas as etapas necessárias de configuração do EOP, a fim de proteger seu ambiente de mensagens.</span><span class="sxs-lookup"><span data-stu-id="8fde3-144">If you've already purchased EOP, see [Set up your EOP service](set-up-your-eop-service.md) to ensure that you complete all the steps necessary to configure EOP to protect your messaging environment.</span></span> 
  
## <a name="for-more-information"></a><span data-ttu-id="8fde3-145">Para obter mais informações</span><span class="sxs-lookup"><span data-stu-id="8fde3-145">For more information</span></span>

[<span data-ttu-id="8fde3-146">Recursos EOP</span><span class="sxs-lookup"><span data-stu-id="8fde3-146">EOP features</span></span>](eop-features.md)
  
[<span data-ttu-id="8fde3-147">Vídeos de introdução ao EOP</span><span class="sxs-lookup"><span data-stu-id="8fde3-147">Videos for getting started with EOP</span></span>](videos-for-getting-started-with-eop.md)
  
[<span data-ttu-id="8fde3-148">Perguntas frequentes gerais sobre o EOP</span><span class="sxs-lookup"><span data-stu-id="8fde3-148">EOP general FAQ</span></span>](eop-general-faq.md)
  
[<span data-ttu-id="8fde3-149">Perguntas frequentes sobre mensagens enfileiradas, adiadas e retornadas do EOP</span><span class="sxs-lookup"><span data-stu-id="8fde3-149">EOP queued, deferred, and bounced messages FAQ</span></span>](eop-queued-deferred-and-bounced-messages-faq.md)
  
[<span data-ttu-id="8fde3-150">Perguntas frequentes sobre administração delegada</span><span class="sxs-lookup"><span data-stu-id="8fde3-150">Delegated administration FAQ</span></span>](delegated-administration-faq.md)
  
[<span data-ttu-id="8fde3-151">Mover domínios e configurações de uma organização do EOP para outra organização do EOP</span><span class="sxs-lookup"><span data-stu-id="8fde3-151">Move domains and settings from one EOP organization to another EOP organization</span></span>](move-domains-and-settings-from-one-eop-organization-to-another-eop-organization.md)
  


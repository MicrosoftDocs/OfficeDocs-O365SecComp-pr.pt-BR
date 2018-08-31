---
title: Inteligência de fluxo de emails no Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/27/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c29f75e5-c16e-409e-a123-430691e38276
description: 'Normalmente, você usa um conector para rotear mensagens da sua organização do Office 365 para seu local ambiente de mensagens. Você também pode usar um conector para rotear mensagens enviadas do Office 365 para uma organização parceira. Quando o Office 365 não pode entregar mensagens por meio do conector, eles-em fila no Office 365. '
ms.openlocfilehash: 4effbb783d6ba8f3b33d0aed446e031193d2f2a3
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002712"
---
# <a name="mail-flow-intelligence-in-office-365"></a><span data-ttu-id="ef45c-105">Inteligência de fluxo de emails no Office 365</span><span class="sxs-lookup"><span data-stu-id="ef45c-105">Mail flow intelligence in Office 365</span></span>
  
<span data-ttu-id="ef45c-p102">Normalmente, você usa um conector para rotear mensagens da sua organização do Office 365 para seu local ambiente de mensagens. Você também pode usar um conector para rotear mensagens enviadas do Office 365 para uma organização parceira. Quando o Office 365 não pode entregar mensagens por meio do conector, eles-em fila no Office 365. O Office 365 continuará tentar novamente a entrega para cada mensagem para 48 horas. Após 48 horas, a mensagem na fila expirará e a mensagem será retornada ao remetente original em um relatório de falha na entrega (também conhecido como uma mensagem de notificação de falha na ou rejeição).</span><span class="sxs-lookup"><span data-stu-id="ef45c-p102">Typically, you use a connector to route messages from your Office 365 organization to your on-premises messaging environment. You might also use a connector to route messages from Office 365 to a partner organization. When Office 365 can't deliver these messages via the connector, they're queued in Office 365. Office 365 will continue to retry delivery for each message for 48 hours. After 48 hours, the queued message will expire, and the message will be returned to the original sender in a non-delivery report (also known as an NDR or bounce message).</span></span>
  
<span data-ttu-id="ef45c-p103">O Office 365 gerará um erro quando uma mensagem não pode ser entregue por meio de um conector. Os erros mais comuns e suas soluções são descritas neste tópico. Coletivamente, erros de enfileiramento de mensagens e notificação não entregue mensagens enviadas por meio de conectores é conhecido como fluxo de mensagens de inteligência de dados.</span><span class="sxs-lookup"><span data-stu-id="ef45c-p103">Office 365 generates an error when a message can't be delivered by using a connector. The most common errors and their solutions are described in this topic. Collectively, queuing and notification errors for undeliverable messages sent via connectors is known as mailflow intelligence.</span></span>
  
 <span data-ttu-id="ef45c-114">**Sumário**</span><span class="sxs-lookup"><span data-stu-id="ef45c-114">**Contents**</span></span>
  
- [<span data-ttu-id="ef45c-115">Código de erro: falha de consulta de DNS 450 4.4.312</span><span class="sxs-lookup"><span data-stu-id="ef45c-115">Error code: 450 4.4.312 DNS query failed</span></span>](mail-flow-intelligence-in-office-365.md#ErrorCode44312)
    
- [<span data-ttu-id="ef45c-116">Código de erro: 450 4.4.315 Conexão esgotado</span><span class="sxs-lookup"><span data-stu-id="ef45c-116">Error code: 450 4.4.315 Connection timed out</span></span>](mail-flow-intelligence-in-office-365.md#ErrorCode44315)
    
- [<span data-ttu-id="ef45c-117">Código de erro: 450 4.4.316 Conexão recusada</span><span class="sxs-lookup"><span data-stu-id="ef45c-117">Error code: 450 4.4.316 Connection refused</span></span>](mail-flow-intelligence-in-office-365.md#ErrorCode44316)
    
- [<span data-ttu-id="ef45c-118">Código de erro: 450 4.4.317 não é possível conectar ao servidor remoto</span><span class="sxs-lookup"><span data-stu-id="ef45c-118">Error code: 450 4.4.317 Cannot connect to remote server</span></span>](mail-flow-intelligence-in-office-365.md#ErrorCode44317)
    
- [<span data-ttu-id="ef45c-119">Código de erro: 450 4.4.318 Conexão foi fechada abruptamente</span><span class="sxs-lookup"><span data-stu-id="ef45c-119">Error code: 450 4.4.318 Connection was closed abruptly</span></span>](mail-flow-intelligence-in-office-365.md#ErrorCode44318)
    
- [<span data-ttu-id="ef45c-120">Código de erro: Falha na validação do certificado de 450 4.7.320</span><span class="sxs-lookup"><span data-stu-id="ef45c-120">Error code: 450 4.7.320 Certificate validation failed</span></span>](mail-flow-intelligence-in-office-365.md#ErrorCode47320)
    
## <a name="error-code-450-44312-dns-query-failed"></a><span data-ttu-id="ef45c-121">Código de erro: falha de consulta de DNS 450 4.4.312</span><span class="sxs-lookup"><span data-stu-id="ef45c-121">Error code: 450 4.4.312 DNS query failed</span></span>

<span data-ttu-id="ef45c-p104">Normalmente, esse erro significa o Office 365 tentou se conectar ao host inteligente especificado no conector, mas a consulta DNS para localizar o IP do host inteligente lida com falha. As causas possíveis desse erro são:</span><span class="sxs-lookup"><span data-stu-id="ef45c-p104">Typically, this error means Office 365 tried to connect to the smart host that's specified in the connector, but the DNS query to find the smart host IP addresses failed. The possible causes for this error are:</span></span>
  
- <span data-ttu-id="ef45c-124">Há um problema com o DNS do seu domínio que hospeda o serviço (o participante que mantém os servidores de nomes de autorização para seu domínio).</span><span class="sxs-lookup"><span data-stu-id="ef45c-124">There's an issue with your domain's DNS hosting service (the party that maintains the authoritative name servers for your domain).</span></span>
    
- <span data-ttu-id="ef45c-125">Seu domínio recentemente expirou, para que o registro MX não possam ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="ef45c-125">Your domain has recently expired, so the MX record can't be retrieved.</span></span>
    
- <span data-ttu-id="ef45c-126">Registro de MX do seu domínio foi alterada recentemente e os servidores DNS do Office 365 ainda tem anteriormente no cache DNS informações do seu domínio.</span><span class="sxs-lookup"><span data-stu-id="ef45c-126">Your domain's MX record has recently changed, and the Office 365 DNS servers still have previously cached DNS information for your domain.</span></span>
    
<span data-ttu-id="ef45c-127">Você precisa para corrigir o problema DNS trabalhando com seu serviço de hospedagem de DNS.</span><span class="sxs-lookup"><span data-stu-id="ef45c-127">You need to fix the DNS issue by working with your DNS hosting service.</span></span>
  
<span data-ttu-id="ef45c-128">Se o erro for de sua organização parceira (por exemplo, um 3º nuvem serviço provedor de terceiros), será necessário entrar em contato com seu parceiro para corrigir o problema.</span><span class="sxs-lookup"><span data-stu-id="ef45c-128">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>
  
## <a name="error-code-450-44315-connection-timed-out"></a><span data-ttu-id="ef45c-129">Código de erro: 450 4.4.315 Conexão esgotado</span><span class="sxs-lookup"><span data-stu-id="ef45c-129">Error code: 450 4.4.315 Connection timed out</span></span>

<span data-ttu-id="ef45c-p105">Normalmente, isso significa que Office 365 não pode se conectar ao servidor de mensagens de destino. Detalhes do erro explicará o problema. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="ef45c-p105">Typically, this means Office 365 can't connect to the destination messaging server. The error details will explain the problem. For example:</span></span>
  
- <span data-ttu-id="ef45c-133">Seu servidor de mensagens está desativado no local.</span><span class="sxs-lookup"><span data-stu-id="ef45c-133">Your on-premises messaging server is down.</span></span>
    
- <span data-ttu-id="ef45c-134">Há um erro nas configurações de host inteligente do conector, para que o Office 365 está tentando se conectar a um endereço IP incorreto.</span><span class="sxs-lookup"><span data-stu-id="ef45c-134">There's an error in the connector's smart host settings, so Office 365 is trying to connect to the wrong IP address.</span></span>
    
<span data-ttu-id="ef45c-p106">Descobrir qual cenário se aplica a você e faça as correções necessárias. Por exemplo, se o fluxo de email tiver sido funcionando corretamente, e você não tiver alterado as configurações do conector, você precisa verificar seu local o ambiente de mensagens para verificar se o servidor está desativado, ou se houve alterações à sua infraestrutura de rede (por exemplo, Você alterou provedores de serviços de Internet, portanto você agora ter endereços IP diferentes).</span><span class="sxs-lookup"><span data-stu-id="ef45c-p106">Find out which scenario applies to you, and make the necessary corrections. For example, if mail flow has been working correctly, and you haven't changed the connector settings, you need to check your on-premises messaging environment to see if the server is down, or if there have been any changes to your network infrastructure (for example, you've changed Internet service providers, so you now have different IP addresses).</span></span>
  
<span data-ttu-id="ef45c-137">Se o erro for de sua organização parceira (por exemplo, um 3º nuvem serviço provedor de terceiros), será necessário entrar em contato com seu parceiro para corrigir o problema.</span><span class="sxs-lookup"><span data-stu-id="ef45c-137">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>
  
## <a name="error-code-450-44316-connection-refused"></a><span data-ttu-id="ef45c-138">Código de erro: 450 4.4.316 Conexão recusada</span><span class="sxs-lookup"><span data-stu-id="ef45c-138">Error code: 450 4.4.316 Connection refused</span></span>

<span data-ttu-id="ef45c-p107">Normalmente, esse erro significa que Office 365 encontrou um erro de conexão ao tentar se conectar ao servidor de mensagens de destino. Uma causa provável para este erro é que seu firewall está bloqueando conexões de endereços IP do Office 365. Esse erro pode ser por design, se você tiver migrado completamente seu local mensagens do sistema para o Office 365 e desligar o seu local ambiente de mensagens..</span><span class="sxs-lookup"><span data-stu-id="ef45c-p107">Typically, this error means Office 365 encountered a connection error when it tried to connect to the destination messaging server. A likely cause for this error is your firewall is blocking connections from Office 365 IP addresses. Or, this error might be by design if you've completely migrated your on-premises messaging system to Office 365 and shut down your on-premises messaging environment..</span></span>
  
- <span data-ttu-id="ef45c-p108">Se você tiver caixas de correio em seu ambiente local, você precisará modificar as configurações de firewall para permitir conexões de endereços de IP do Office 365 na porta TCP 25 para seu local servidores de mensagens. Para obter uma lista dos endereços IP do Office 365, consulte [URLs do Office 365 e intervalos de endereços IP](https://go.microsoft.com/fwlink/p/?linkid=228887).</span><span class="sxs-lookup"><span data-stu-id="ef45c-p108">If you have mailboxes in your on-premises environment, you need to modify your firewall settings to allow connections from Office 365 IP addresses on TCP port 25 to your on-premises messaging servers. For a list of the Office 365 IP addresses, see [Office 365 URLs and IP address ranges](https://go.microsoft.com/fwlink/p/?linkid=228887).</span></span>
    
- <span data-ttu-id="ef45c-p109">Se não há mais mensagens devem ser entregues ao seu ambiente local, clique em **corrigir agora** no alerta para que o Office 365 pode rejeitar imediatamente as mensagens com destinatários inválidos. Isso reduzirá o risco de exceder a cota da sua organização para destinatários inválidos, que poderiam afetar a entrega da mensagem normal. Ou então, você pode usar as instruções a seguir para manualmente para corrigir o problema:</span><span class="sxs-lookup"><span data-stu-id="ef45c-p109">If no more messages should be delivered to your on-premises environment, click **Fix now** in the alert so Office 365 can immediately reject the messages with invalid recipients. This will reduce the risk of exceeding your organization's quota for invalid recipients, which could impact normal message delivery. Or, you can use the following instructions to manually fix the issue:</span></span> 
    
  - <span data-ttu-id="ef45c-p110">Desabilitar ou excluir o conector do Office 365 ao seu ambiente local: Centro de administração do Office 365 \> **Admin centrais** \> **Exchange** \> **fluxo de emails** \> **conectores** \> selecione o conector com o valor **do** **Office 365** e o **para** **o servidor de email da sua organização**de valor. Excluir o conector clicando em **Excluir**![ícone Excluir](media/ITPro-EAC-DeleteIcon.gif), ou desativar o conector clicando em **Editar** ![ícone Editar](media/ITPro-EAC-EditIcon.gif) e desmarcando **ativá-lo**.</span><span class="sxs-lookup"><span data-stu-id="ef45c-p110">Disable or delete the connector from Office 365 to your on-premises environment: Office 365 admin center \> **Admin centers** \> **Exchange** \> **Mail flow** \> **Connectors** \> select the connector with the **From** value **Office 365** and the **To** value **Your organization's email server**. Delete the connector by clicking **Delete**![Delete icon](media/ITPro-EAC-DeleteIcon.gif), or disable the connector by clicking **Edit** ![Edit icon](media/ITPro-EAC-EditIcon.gif) and unchecking **Turn it on**.</span></span>
    
  - <span data-ttu-id="ef45c-p111">Alterar o domínio aceito no Office 365 que está associado ao seu local ambiente de mensagens de **Retransmissão interna** como **autoritativo**. Para obter instruções, consulte [Gerenciar domínios aceitos no Exchange Online](http://technet.microsoft.com/library/0fc0ecc0-e133-48fa-9d72-cb4793a73960.aspx).</span><span class="sxs-lookup"><span data-stu-id="ef45c-p111">Change the accepted domain in Office 365 that's associated with your on-premises messaging environment from **Internal Relay** to **Authoritative**. For instructions, see [Manage Accepted Domains in Exchange Online](http://technet.microsoft.com/library/0fc0ecc0-e133-48fa-9d72-cb4793a73960.aspx).</span></span>
    
    <span data-ttu-id="ef45c-p112">**Observação**: geralmente, essas alterações terão entre 30 minutos e uma hora entre em vigor. Após uma hora, verifique se você não é mais recebe o erro.</span><span class="sxs-lookup"><span data-stu-id="ef45c-p112">**Note**: Typically, these changes take between 30 minutes and one hour to take effect. After one hour, verify that you no longer receive the error.</span></span>
    
<span data-ttu-id="ef45c-153">Se o erro for de sua organização parceira (por exemplo, um 3º nuvem serviço provedor de terceiros), será necessário entrar em contato com seu parceiro para corrigir o problema.</span><span class="sxs-lookup"><span data-stu-id="ef45c-153">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>
  
## <a name="error-code-450-44317-cannot-connect-to-remote-server"></a><span data-ttu-id="ef45c-154">Código de erro: 450 4.4.317 não é possível conectar ao servidor remoto</span><span class="sxs-lookup"><span data-stu-id="ef45c-154">Error code: 450 4.4.317 Cannot connect to remote server</span></span>

<span data-ttu-id="ef45c-p113">Normalmente, esse erro significa o Office 365 é conectado ao servidor de mensagens de destino, mas o servidor respondeu com um erro imediato ou não cumprir os requisitos de conexão. Detalhes do erro explicará o problema. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="ef45c-p113">Typically, this error means Office 365 connected to the destination messaging server, but the server responded with an immediate error, or doesn't meet the connection requirements. The error details will explain the problem. For example:</span></span>
  
- <span data-ttu-id="ef45c-158">O servidor de mensagens de destino respondeu com um erro "Serviço não disponível", que indica que o servidor é capaz de manter a comunicação com o Office 365.</span><span class="sxs-lookup"><span data-stu-id="ef45c-158">The destination messaging server responded with a "Service not available" error, which indicates the server is unable to maintain communication with Office 365.</span></span>
    
- <span data-ttu-id="ef45c-159">O conector é configurado para exigir o TLS, mas o servidor de mensagens de destino não oferece suporte a TLS.</span><span class="sxs-lookup"><span data-stu-id="ef45c-159">The connector is configured to require TLS, but the destination messaging server doesn't support TLS.</span></span>
    
<span data-ttu-id="ef45c-160">Verifique as configurações de TLS e certificados em seu local mensagens servidores e as configurações de TLS no conector.</span><span class="sxs-lookup"><span data-stu-id="ef45c-160">Verify the TLS settings and certificates on your on-premises messaging servers, and the TLS settings on the connector.</span></span>
  
<span data-ttu-id="ef45c-161">Se o erro for de sua organização parceira (por exemplo, um 3º nuvem serviço provedor de terceiros), será necessário entrar em contato com seu parceiro para corrigir o problema.</span><span class="sxs-lookup"><span data-stu-id="ef45c-161">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>
  
## <a name="error-code-450-44318-connection-was-closed-abruptly"></a><span data-ttu-id="ef45c-162">Código de erro: 450 4.4.318 Conexão foi fechada abruptamente</span><span class="sxs-lookup"><span data-stu-id="ef45c-162">Error code: 450 4.4.318 Connection was closed abruptly</span></span>

<span data-ttu-id="ef45c-p114">Normalmente, esse erro significa o Office 365 está tendo dificuldade para se comunicar com o seu local ambiente de mensagens, portanto a conexão foi abandonada. As causas possíveis desse erro são:</span><span class="sxs-lookup"><span data-stu-id="ef45c-p114">Typically, this error means Office 365 is having difficulty communicating with your on-premises messaging environment, so the connection was dropped. The possible causes for this error are:</span></span>
  
- <span data-ttu-id="ef45c-165">Seu firewall usa regras de exame de pacotes de SMTP e as regras não estão funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="ef45c-165">Your firewall uses SMTP packet examination rules, and those rules aren't working correctly.</span></span>
    
- <span data-ttu-id="ef45c-166">Seu local no servidor de mensagens não está funcionando corretamente (por exemplo, serviço cai, panes ou poucos recursos no sistema), que está fazendo com que o servidor de tempo limite e fechar a conexão para o Office 365.</span><span class="sxs-lookup"><span data-stu-id="ef45c-166">Your on-premises messaging server isn't working correctly (for example, service hangs, crashes, or low system resources), which is causing the server to time out and close the connection to Office 365.</span></span>
    
- <span data-ttu-id="ef45c-p115">Existem problemas de rede entre seu ambiente local e o Office 365. Se o problema persistir, contate a equipe de rede para solucionar o problema.</span><span class="sxs-lookup"><span data-stu-id="ef45c-p115">There are network issues between your on-premises environment and Office 365. If the problem persists, contact your network team to troubleshoot the issue.</span></span>
    
<span data-ttu-id="ef45c-169">Descobrir qual cenário se aplica a você e faça as correções necessárias.</span><span class="sxs-lookup"><span data-stu-id="ef45c-169">Find out which scenario applies to you, and make the necessary corrections.</span></span>
  
<span data-ttu-id="ef45c-170">Se o erro for de sua organização parceira (por exemplo, um 3º nuvem serviço provedor de terceiros), será necessário entrar em contato com seu parceiro para corrigir o problema.</span><span class="sxs-lookup"><span data-stu-id="ef45c-170">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>
  
## <a name="error-code-450-47320-certificate-validation-failed"></a><span data-ttu-id="ef45c-171">Código de erro: Falha na validação do certificado de 450 4.7.320</span><span class="sxs-lookup"><span data-stu-id="ef45c-171">Error code: 450 4.7.320 Certificate validation failed</span></span>

<span data-ttu-id="ef45c-p116">Normalmente, esse erro significa que Office 365 encontrou um erro ao tentar validar o certificado do servidor de mensagens de destino. Detalhes do erro explicará o erro. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="ef45c-p116">Typically, this error means Office 365 encountered an error while trying to validate the certificate of the destination messaging server. The error details will explain the error. For example:</span></span>
  
- <span data-ttu-id="ef45c-175">O certificado expirou</span><span class="sxs-lookup"><span data-stu-id="ef45c-175">Certificate expired</span></span>
    
- <span data-ttu-id="ef45c-176">Incompatibilidade de assunto do certificado</span><span class="sxs-lookup"><span data-stu-id="ef45c-176">Certificate subject mismatch</span></span>
    
- <span data-ttu-id="ef45c-177">Certificado não é mais válido</span><span class="sxs-lookup"><span data-stu-id="ef45c-177">Certificate is no longer valid</span></span>
    
<span data-ttu-id="ef45c-178">Corrija o conector ou o certificado para que as mensagens em fila no Office 365can ser entregues.</span><span class="sxs-lookup"><span data-stu-id="ef45c-178">Please fix the certificate or the connector so that queued messages in Office 365can be delivered.</span></span>
  
<span data-ttu-id="ef45c-179">Se o erro for de sua organização parceira (por exemplo, um 3º nuvem serviço provedor de terceiros), será necessário entrar em contato com seu parceiro para corrigir o problema.</span><span class="sxs-lookup"><span data-stu-id="ef45c-179">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>
  
## <a name="other-error-codes"></a><span data-ttu-id="ef45c-180">Outros códigos de erro</span><span class="sxs-lookup"><span data-stu-id="ef45c-180">Other error codes</span></span>

<span data-ttu-id="ef45c-p117">O Office 365 está tendo mensagens oferecendo de dificuldade para seu local ou o servidor de mensagens de parceiro. Use as informações do **servidor de destino** no erro para examinar o problema em seu ambiente ou modificar o conector se houver um erro de configuração.</span><span class="sxs-lookup"><span data-stu-id="ef45c-p117">Office 365 is having difficulty delivering messages to your on-premises or partner messaging server. Use the **Destination server** information in the error to examine the issue in your environment, or modify the connector if there's a configuration error.</span></span> 
  
<span data-ttu-id="ef45c-183">Se o erro for de sua organização parceira (por exemplo, um 3º nuvem serviço provedor de terceiros), será necessário entrar em contato com seu parceiro para corrigir o problema.</span><span class="sxs-lookup"><span data-stu-id="ef45c-183">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>
  


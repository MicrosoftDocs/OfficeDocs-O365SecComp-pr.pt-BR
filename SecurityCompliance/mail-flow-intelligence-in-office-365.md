---
title: Inteligência de fluxo de emails no Office 365
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c29f75e5-c16e-409e-a123-430691e38276
description: Os administradores podem conhecer os códigos de erro que estão associados a entrega de mensagens usando conectores no Office 365 (também conhecido como inteligência de fluxo de email).
ms.openlocfilehash: 9f27dfd4c265eb62028d68c27764183202692ef4
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2019
ms.locfileid: "28327083"
---
# <a name="mail-flow-intelligence-in-office-365"></a><span data-ttu-id="580b9-103">Inteligência de fluxo de emails no Office 365</span><span class="sxs-lookup"><span data-stu-id="580b9-103">Mail flow intelligence in Office 365</span></span>

<span data-ttu-id="580b9-p101">Normalmente, você deve usar um conector para rotear mensagens de email da sua organização do Office 365 para seu ambiente de email local. Você também pode usar um conector para rotear mensagens enviadas do Office 365 para uma organização parceira. Quando o Office 365 não pode entregar mensagens por meio do conector, eles-em fila no Office 365. O Office 365 continuará tentar novamente a entrega para cada mensagem para 48 horas. Após 48 horas, a mensagem na fila expirará e a mensagem será retornada ao remetente original em um relatório de falha na entrega (também conhecido como uma mensagem de notificação de falha na ou rejeição).</span><span class="sxs-lookup"><span data-stu-id="580b9-p101">Typically, you use a connector to route email messages from your Office 365 organization to your on-premises email environment. You might also use a connector to route messages from Office 365 to a partner organization. When Office 365 can't deliver these messages via the connector, they're queued in Office 365. Office 365 will continue to retry delivery for each message for 48 hours. After 48 hours, the queued message will expire, and the message will be returned to the original sender in a non-delivery report (also known as an NDR or bounce message).</span></span>

<span data-ttu-id="580b9-p102">O Office 365 gerará um erro quando uma mensagem não pode ser entregue por meio de um conector. Os erros mais comuns e suas soluções são descritas neste tópico. Coletivamente, erros de enfileiramento de mensagens e notificação não entregue mensagens enviadas por meio de conectores é conhecido como _inteligência de dados de fluxo de email_.</span><span class="sxs-lookup"><span data-stu-id="580b9-p102">Office 365 generates an error when a message can't be delivered by using a connector. The most common errors and their solutions are described in this topic. Collectively, queuing and notification errors for undeliverable messages sent via connectors is known as _mail flow intelligence_.</span></span>

## <a name="error-code-450-44312-dns-query-failed"></a><span data-ttu-id="580b9-112">Código de erro: falha de consulta de DNS 450 4.4.312</span><span class="sxs-lookup"><span data-stu-id="580b9-112">Error code: 450 4.4.312 DNS query failed</span></span>

<span data-ttu-id="580b9-p103">Normalmente, esse erro significa que Office 365 tentou se conectar ao host inteligente especificado no conector, mas a consulta DNS para localizar os endereços IP do host inteligente falhou. As causas possíveis desse erro são:</span><span class="sxs-lookup"><span data-stu-id="580b9-p103">Typically, this error means Office 365 tried to connect to the smart host that's specified in the connector, but the DNS query to find the smart host's IP addresses failed. The possible causes for this error are:</span></span>

- <span data-ttu-id="580b9-115">Há um problema com o DNS do seu domínio que hospeda o serviço (o participante que mantém os servidores de nomes de autorização para seu domínio).</span><span class="sxs-lookup"><span data-stu-id="580b9-115">There's an issue with your domain's DNS hosting service (the party that maintains the authoritative name servers for your domain).</span></span>

- <span data-ttu-id="580b9-116">Seu domínio recentemente expirou, para que o registro MX não possam ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="580b9-116">Your domain has recently expired, so the MX record can't be retrieved.</span></span>

- <span data-ttu-id="580b9-117">Registro de MX do seu domínio foi alterada recentemente e os servidores DNS do Office 365 ainda tem anteriormente no cache DNS informações do seu domínio.</span><span class="sxs-lookup"><span data-stu-id="580b9-117">Your domain's MX record has recently changed, and the Office 365 DNS servers still have previously cached DNS information for your domain.</span></span>

### <a name="how-do-i-fix-error-code-450-44312"></a><span data-ttu-id="580b9-118">Como faço para corrigir o código de erro 450 4.4.312?</span><span class="sxs-lookup"><span data-stu-id="580b9-118">How do I fix error code 450 4.4.312?</span></span>

- <span data-ttu-id="580b9-119">Trabalhar com seu serviço de hospedagem de DNS para identificar e corrigir o problema com o seu domínio.</span><span class="sxs-lookup"><span data-stu-id="580b9-119">Work with your DNS hosting service to identify and fix the problem with your domain.</span></span>

- <span data-ttu-id="580b9-120">Se o erro for de sua organização parceira (por exemplo, um 3º nuvem serviço provedor de terceiros), contate seu parceiro para corrigir o problema.</span><span class="sxs-lookup"><span data-stu-id="580b9-120">If the error is from your partner organization (for example, a 3rd party cloud service provider), contact your partner to fix the issue.</span></span>

## <a name="error-code-450-44315-connection-timed-out"></a><span data-ttu-id="580b9-121">Código de erro: 450 4.4.315 Conexão esgotado</span><span class="sxs-lookup"><span data-stu-id="580b9-121">Error code: 450 4.4.315 Connection timed out</span></span>

<span data-ttu-id="580b9-p104">Normalmente, isso significa que Office 365 não pode se conectar ao servidor de email de destino. Detalhes do erro explicará o problema. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="580b9-p104">Typically, this means Office 365 can't connect to the destination email server. The error details will explain the problem. For example:</span></span>

- <span data-ttu-id="580b9-125">Seu servidor de email no local está inoperante.</span><span class="sxs-lookup"><span data-stu-id="580b9-125">Your on-premises email server is down.</span></span>

- <span data-ttu-id="580b9-126">Há um erro nas configurações de host inteligente do conector, para que o Office 365 está tentando se conectar a um endereço IP incorreto.</span><span class="sxs-lookup"><span data-stu-id="580b9-126">There's an error in the connector's smart host settings, so Office 365 is trying to connect to the wrong IP address.</span></span>

### <a name="how-do-i-fix-error-code-450-44315"></a><span data-ttu-id="580b9-127">Como faço para corrigir o código de erro 450 4.4.315?</span><span class="sxs-lookup"><span data-stu-id="580b9-127">How do I fix error code 450 4.4.315?</span></span>

- <span data-ttu-id="580b9-p105">Descobrir qual cenário se aplica a você e faça as correções necessárias. Por exemplo, se o fluxo de email tiver sido funcionando corretamente, e você não tiver alterado as configurações do conector, você precisa verificar seu ambiente de email local para ver se o servidor está inoperante ou se houve alterações à sua infraestrutura de rede (por exemplo, Você alterou provedores de serviços de internet, portanto você agora ter endereços IP diferentes).</span><span class="sxs-lookup"><span data-stu-id="580b9-p105">Find out which scenario applies to you, and make the necessary corrections. For example, if mail flow has been working correctly, and you haven't changed the connector settings, you need to check your on-premises email environment to see if the server is down, or if there have been any changes to your network infrastructure (for example, you've changed internet service providers, so you now have different IP addresses).</span></span>

- <span data-ttu-id="580b9-130">Se o erro for de sua organização parceira (por exemplo, um 3º nuvem serviço provedor de terceiros), contate seu parceiro para corrigir o problema.</span><span class="sxs-lookup"><span data-stu-id="580b9-130">If the error is from your partner organization (for example, a 3rd party cloud service provider), contact your partner to fix the issue.</span></span>

## <a name="error-code-450-44316-connection-refused"></a><span data-ttu-id="580b9-131">Código de erro: 450 4.4.316 Conexão recusada</span><span class="sxs-lookup"><span data-stu-id="580b9-131">Error code: 450 4.4.316 Connection refused</span></span>

<span data-ttu-id="580b9-p106">Normalmente, esse erro significa que Office 365 encontrou um erro de conexão ao tentar se conectar ao servidor de email de destino. Uma causa provável para este erro é que seu firewall está bloqueando conexões de endereços IP do Office 365. Ou, esse erro pode ser por design se você tiver sido migrado completamente seu local sistema de email para o Office 365 e desligar o seu ambiente de email local.</span><span class="sxs-lookup"><span data-stu-id="580b9-p106">Typically, this error means Office 365 encountered a connection error when it tried to connect to the destination email server. A likely cause for this error is your firewall is blocking connections from Office 365 IP addresses. Or, this error might be by design if you've completely migrated your on-premises email system to Office 365 and shut down your on-premises email environment.</span></span>

### <a name="how-do-i-fix-error-code-450-44316"></a><span data-ttu-id="580b9-135">Como faço para corrigir o código de erro 450 4.4.316?</span><span class="sxs-lookup"><span data-stu-id="580b9-135">How do I fix error code 450 4.4.316?</span></span>

- <span data-ttu-id="580b9-p107">Se você tiver caixas de correio em seu ambiente local, você precisará modificar as configurações de firewall para permitir conexões de endereços IP do Office 365 na porta TCP 25 para os servidores de email local. Para obter uma lista dos endereços IP do Office 365, consulte [URLs do Office 365 e intervalos de endereços IP](https://support.office.com/article/8548a211-3fe7-47cb-abb1-355ea5aa88a2.aspx).</span><span class="sxs-lookup"><span data-stu-id="580b9-p107">If you have mailboxes in your on-premises environment, you need to modify your firewall settings to allow connections from Office 365 IP addresses on TCP port 25 to your on-premises email servers. For a list of the Office 365 IP addresses, see [Office 365 URLs and IP address ranges](https://support.office.com/article/8548a211-3fe7-47cb-abb1-355ea5aa88a2.aspx).</span></span>

- <span data-ttu-id="580b9-p108">Se não há mais mensagens devem ser entregues ao seu ambiente local, clique em **corrigir agora** no alerta para que o Office 365 pode rejeitar imediatamente as mensagens com destinatários inválidos. Isso reduzirá o risco de exceder a cota da sua organização para destinatários inválidos, que poderiam afetar a entrega da mensagem normal. Ou então, você pode usar as instruções a seguir para manualmente para corrigir o problema:</span><span class="sxs-lookup"><span data-stu-id="580b9-p108">If no more messages should be delivered to your on-premises environment, click **Fix now** in the alert so Office 365 can immediately reject the messages with invalid recipients. This will reduce the risk of exceeding your organization's quota for invalid recipients, which could impact normal message delivery. Or, you can use the following instructions to manually fix the issue:</span></span>

  - <span data-ttu-id="580b9-141">No [Centro de administração do Exchange (EAC)](https://docs.microsoft.com/Exchange/exchange-admin-center) no Office 365, desabilitar ou excluir o conector de entrega de emails do Office 365 para seu ambiente de email local:</span><span class="sxs-lookup"><span data-stu-id="580b9-141">In the [Exchange admin center (EAC)](https://docs.microsoft.com/Exchange/exchange-admin-center) in Office 365, disable or delete the connector that delivers email from Office 365 to your on-premises email environment:</span></span>

    1. <span data-ttu-id="580b9-142">No EAC, vá para **fluxo de email** \> **conectores**.</span><span class="sxs-lookup"><span data-stu-id="580b9-142">In the EAC, go to **Mail flow** \> **Connectors**.</span></span>

    2. <span data-ttu-id="580b9-143">Selecione o conector com o valor **do** **Office 365** e o valor **para** **o servidor de email da sua organização** e execute uma das seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="580b9-143">Select the connector with the **From** value **Office 365** and the **To** value **Your organization's email server** and do one of the following steps:</span></span>

       - <span data-ttu-id="580b9-144">Excluir o conector clicando em **Excluir** ![ícone Remover](media/adf01106-cc79-475c-8673-065371c1897b.gif)</span><span class="sxs-lookup"><span data-stu-id="580b9-144">Delete the connector by clicking **Delete** ![Remove icon](media/adf01106-cc79-475c-8673-065371c1897b.gif)</span></span>

       - <span data-ttu-id="580b9-145">Desativar o conector clicando em **Editar** ![ícone Editar](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) e desmarcando **ativá-lo**.</span><span class="sxs-lookup"><span data-stu-id="580b9-145">Disable the connector by clicking **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) and unchecking **Turn it on**.</span></span>

  - <span data-ttu-id="580b9-p109">Altere o domínio aceito no Office 365 que está associado ao seu ambiente de email no local de **Retransmissão interna** como **autoritativo**. Para obter instruções, consulte [Gerenciar domínios aceitos no Exchange Online](https://go.microsoft.com/fwlink/p/?linkid=785428).</span><span class="sxs-lookup"><span data-stu-id="580b9-p109">Change the accepted domain in Office 365 that's associated with your on-premises email environment from **Internal Relay** to **Authoritative**. For instructions, see [Manage accepted domains in Exchange Online](https://go.microsoft.com/fwlink/p/?linkid=785428).</span></span>

  <span data-ttu-id="580b9-p110">**Observação**: geralmente, essas alterações terão entre 30 minutos e uma hora entre em vigor. Após uma hora, verifique se você não é mais recebe o erro.</span><span class="sxs-lookup"><span data-stu-id="580b9-p110">**Note**: Typically, these changes take between 30 minutes and one hour to take effect. After one hour, verify that you no longer receive the error.</span></span>

- <span data-ttu-id="580b9-150">Se o erro for de sua organização parceira (por exemplo, um 3º nuvem serviço provedor de terceiros), será necessário entrar em contato com seu parceiro para corrigir o problema.</span><span class="sxs-lookup"><span data-stu-id="580b9-150">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>

## <a name="error-code-450-44317-cannot-connect-to-remote-server"></a><span data-ttu-id="580b9-151">Código de erro: 450 4.4.317 não é possível conectar ao servidor remoto</span><span class="sxs-lookup"><span data-stu-id="580b9-151">Error code: 450 4.4.317 Cannot connect to remote server</span></span>

<span data-ttu-id="580b9-p111">Normalmente, esse erro significa o Office 365 é conectado ao servidor de email de destino, mas o servidor respondeu com um erro imediato ou não cumprir os requisitos de conexão. Detalhes do erro explicará o problema. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="580b9-p111">Typically, this error means Office 365 connected to the destination email server, but the server responded with an immediate error, or doesn't meet the connection requirements. The error details will explain the problem. For example:</span></span>

- <span data-ttu-id="580b9-155">O servidor de email de destino respondeu com um erro "Serviço não disponível", que indica que o servidor é capaz de manter a comunicação com o Office 365.</span><span class="sxs-lookup"><span data-stu-id="580b9-155">The destination email server responded with a "Service not available" error, which indicates the server is unable to maintain communication with Office 365.</span></span>

- <span data-ttu-id="580b9-156">O conector é configurado para exigir o TLS, mas o servidor de email de destino não oferece suporte a TLS.</span><span class="sxs-lookup"><span data-stu-id="580b9-156">The connector is configured to require TLS, but the destination email server doesn't support TLS.</span></span>

### <a name="how-do-i-fix-error-code-450-44317"></a><span data-ttu-id="580b9-157">Como faço para corrigir o código de erro 450 4.4.317?</span><span class="sxs-lookup"><span data-stu-id="580b9-157">How do I fix error code 450 4.4.317?</span></span>

- <span data-ttu-id="580b9-158">Verifique as configurações de TLS e certificados em seus servidores de email local e as configurações de TLS no conector.</span><span class="sxs-lookup"><span data-stu-id="580b9-158">Verify the TLS settings and certificates on your on-premises email servers, and the TLS settings on the connector.</span></span>

- <span data-ttu-id="580b9-159">Se o erro for de sua organização parceira (por exemplo, um 3º nuvem serviço provedor de terceiros), será necessário entrar em contato com seu parceiro para corrigir o problema.</span><span class="sxs-lookup"><span data-stu-id="580b9-159">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>

## <a name="error-code-450-44318-connection-was-closed-abruptly"></a><span data-ttu-id="580b9-160">Código de erro: 450 4.4.318 Conexão foi fechada abruptamente</span><span class="sxs-lookup"><span data-stu-id="580b9-160">Error code: 450 4.4.318 Connection was closed abruptly</span></span>

<span data-ttu-id="580b9-p112">Normalmente, esse erro significa o que Office 365 está tendo dificuldades para comunicação com o seu ambiente de email local, para que a conexão foi abandonada. As causas possíveis desse erro são:</span><span class="sxs-lookup"><span data-stu-id="580b9-p112">Typically, this error means Office 365 is having difficulty communicating with your on-premises email environment, so the connection was dropped. The possible causes for this error are:</span></span>

- <span data-ttu-id="580b9-163">Seu firewall usa regras de exame de pacotes de SMTP e as regras não estão funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="580b9-163">Your firewall uses SMTP packet examination rules, and those rules aren't working correctly.</span></span>

- <span data-ttu-id="580b9-164">Seu servidor de email no local não está trabalhando corretamente (por exemplo, serviço cai, panes ou poucos recursos no sistema), que está fazendo com que o servidor de tempo limite e fechar a conexão para o Office 365.</span><span class="sxs-lookup"><span data-stu-id="580b9-164">Your on-premises email server isn't working correctly (for example, service hangs, crashes, or low system resources), which is causing the server to time out and close the connection to Office 365.</span></span>

- <span data-ttu-id="580b9-165">Existem problemas de rede entre seu ambiente local e o Office 365.</span><span class="sxs-lookup"><span data-stu-id="580b9-165">There are network issues between your on-premises environment and Office 365.</span></span>

### <a name="how-do-i-fix-error-code-450-44318"></a><span data-ttu-id="580b9-166">Como faço para corrigir o código de erro 450 4.4.318?</span><span class="sxs-lookup"><span data-stu-id="580b9-166">How do I fix error code 450 4.4.318?</span></span>

- <span data-ttu-id="580b9-167">Descobrir qual cenário se aplica a você e faça as correções necessárias.</span><span class="sxs-lookup"><span data-stu-id="580b9-167">Find out which scenario applies to you, and make the necessary corrections.</span></span>

- <span data-ttu-id="580b9-168">Se o problema for causado por problemas de rede entre seu ambiente local e o Office 365, contate sua equipe de rede para solucionar o problema.</span><span class="sxs-lookup"><span data-stu-id="580b9-168">If the problem is caused by network issues between your on-premises environment and Office 365, contact your network team to troubleshoot the issue.</span></span>

- <span data-ttu-id="580b9-169">Se o erro for de sua organização parceira (por exemplo, um 3º nuvem serviço provedor de terceiros), será necessário entrar em contato com seu parceiro para corrigir o problema.</span><span class="sxs-lookup"><span data-stu-id="580b9-169">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>

## <a name="error-code-450-47320-certificate-validation-failed"></a><span data-ttu-id="580b9-170">Código de erro: Falha na validação do certificado de 450 4.7.320</span><span class="sxs-lookup"><span data-stu-id="580b9-170">Error code: 450 4.7.320 Certificate validation failed</span></span>

<span data-ttu-id="580b9-p113">Normalmente, esse erro significa que Office 365 encontrou um erro ao tentar validar o certificado do servidor de email de destino. Detalhes do erro explicará o erro. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="580b9-p113">Typically, this error means Office 365 encountered an error while trying to validate the certificate of the destination email server. The error details will explain the error. For example:</span></span>

- <span data-ttu-id="580b9-174">O certificado expirou</span><span class="sxs-lookup"><span data-stu-id="580b9-174">Certificate expired</span></span>

- <span data-ttu-id="580b9-175">Incompatibilidade de assunto do certificado</span><span class="sxs-lookup"><span data-stu-id="580b9-175">Certificate subject mismatch</span></span>

- <span data-ttu-id="580b9-176">Certificado não é mais válido</span><span class="sxs-lookup"><span data-stu-id="580b9-176">Certificate is no longer valid</span></span>

### <a name="how-do-i-fix-error-code-450-47320"></a><span data-ttu-id="580b9-177">Como faço para corrigir o código de erro 450 4.7.320?</span><span class="sxs-lookup"><span data-stu-id="580b9-177">How do I fix error code 450 4.7.320?</span></span>

- <span data-ttu-id="580b9-178">O certificado de corrigi-los ou as configurações no conector de forma que permanece na fila de mensagens no Office 365 podem ser entregues.</span><span class="sxs-lookup"><span data-stu-id="580b9-178">Fix the certificate or the settings on the connector so that queued messages in Office 365 can be delivered.</span></span>

- <span data-ttu-id="580b9-179">Se o erro for de sua organização parceira (por exemplo, um 3º nuvem serviço provedor de terceiros), será necessário entrar em contato com seu parceiro para corrigir o problema.</span><span class="sxs-lookup"><span data-stu-id="580b9-179">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>

## <a name="other-error-codes"></a><span data-ttu-id="580b9-180">Outros códigos de erro</span><span class="sxs-lookup"><span data-stu-id="580b9-180">Other error codes</span></span>

<span data-ttu-id="580b9-p114">O Office 365 está tendo dificuldades para entrega de mensagens no seu local ou servidor de email de parceiro. Use as informações do **servidor de destino** no erro para examinar o problema em seu ambiente ou modificar o conector se houver um erro de configuração.</span><span class="sxs-lookup"><span data-stu-id="580b9-p114">Office 365 is having difficulty delivering messages to your on-premises or partner email server. Use the **Destination server** information in the error to examine the issue in your environment, or modify the connector if there's a configuration error.</span></span> 

<span data-ttu-id="580b9-183">Se o erro for de sua organização parceira (por exemplo, um 3º nuvem serviço provedor de terceiros), será necessário entrar em contato com seu parceiro para corrigir o problema.</span><span class="sxs-lookup"><span data-stu-id="580b9-183">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>

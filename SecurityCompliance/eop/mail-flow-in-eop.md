---
title: Fluxo de emails no EOP
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 3/13/2015
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: e109077e-cc85-4c19-ae40-d218ac7d0548
description: Como um cliente do Proteção do Exchange Online (EOP), todas as mensagens enviadas para sua organização passam através de EOP antes que seus funcionários as vejam. Se você hospedar todas as suas caixas de correio na nuvem com o Exchange Online, ou se você hospedar suas caixas de correio no local (cenário autônomo), talvez para continuar aproveitando sua infraestrutura existente, você tem opções sobre como encaminhar mensagens que passarão pelo EOP para processamento antes que sejam encaminhadas para as caixas de entrada dos seus funcionários.
ms.openlocfilehash: 60ac643e70805de7937a12c9b8f08b593ecd8aab
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35599647"
---
# <a name="mail-flow-in-eop"></a><span data-ttu-id="4cc13-104">Fluxo de emails no EOP</span><span class="sxs-lookup"><span data-stu-id="4cc13-104">Mail flow in EOP</span></span>

<span data-ttu-id="4cc13-p102">Como um cliente do Proteção do Exchange Online (EOP), todas as mensagens enviadas para sua organização passam através de EOP antes que seus funcionários as vejam. Se você hospedar todas as suas caixas de correio na nuvem com o Exchange Online, ou se você hospedar suas caixas de correio no local (cenário autônomo), talvez para continuar aproveitando sua infraestrutura existente, você tem opções sobre como encaminhar mensagens que passarão pelo EOP para processamento antes que sejam encaminhadas para as caixas de entrada dos seus funcionários.</span><span class="sxs-lookup"><span data-stu-id="4cc13-p102">As an Exchange Online Protection (EOP) customer, all messages sent to your organization pass through EOP before your workers see them. Whether you host all of your mailboxes in the cloud with Exchange Online, or you host your mailboxes on premises (called a standalone scenario), perhaps to continue taking advantage of your existing infrastructure, you have options about how to route messages that will pass through EOP for processing before they are routed to your worker inboxes.</span></span>
  
<span data-ttu-id="4cc13-p103">Você pode querer configurar o encaminhamento de email padrão para que seu serviço de mensagens atenda a um requisito comercial. Por exemplo, você pode passar todos os seus emails de saída através de um dispositivo de filtragem de política.</span><span class="sxs-lookup"><span data-stu-id="4cc13-p103">You may want to configure custom mail routing to conform your messaging to a business requirement. For instance, you can pass all of your outbound mail through a policy-filtering appliance.</span></span> 
  
## <a name="working-with-messages-and-message-access-options"></a><span data-ttu-id="4cc13-109">Trabalhando com mensagens e opções de acesso a mensagens</span><span class="sxs-lookup"><span data-stu-id="4cc13-109">Working with messages and message access options</span></span>

<span data-ttu-id="4cc13-p104">O EOP oferece muita flexibilidade no modo como suas mensagens são encaminhadas. Os tópicos a seguir explicam as etapas no processo de fluxo de email.</span><span class="sxs-lookup"><span data-stu-id="4cc13-p104">EOP offers a lot of flexibility in how your messages are routed. The following topics explain steps in the mail flow process.</span></span>
  
<span data-ttu-id="4cc13-112">[Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx) Descreve o recurso Bloqueio de Borda Baseado em Diretório, que permite rejeitar mensagens para destinatários inválidos no perímetro da rede de serviço.</span><span class="sxs-lookup"><span data-stu-id="4cc13-112">[Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx) Describes the Directory Based Edge Blocking feature which lets you reject messages for invalid recipients at the service network perimeter.</span></span> 
  
<span data-ttu-id="4cc13-113">[View or Edit Managed Domains in EOP](https://docs.microsoft.com/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains) descreve como gerenciar domínios que são associados ao seu serviço EOP.</span><span class="sxs-lookup"><span data-stu-id="4cc13-113">[View or Edit Managed Domains in EOP](https://docs.microsoft.com/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains) describes how to manage domains that are associated with your EOP service.</span></span> 
  
<span data-ttu-id="4cc13-p105">Se você adicionar subdomínios à sua organização, o serviço do EOP poderá ajudá-lo a gerenciá-los também. Saiba mais sobre subdomínios em [Enable Mail Flow for Subdomains in Exchange Online](http://technet.microsoft.com/library/4033a30a-f506-481c-8ef0-fd9a0508ae38.aspx).</span><span class="sxs-lookup"><span data-stu-id="4cc13-p105">If you add subdomains to your organization, your EOP service can help you manage these too. Learn more about subdomains at [Enable Mail Flow for Subdomains in Exchange Online](http://technet.microsoft.com/library/4033a30a-f506-481c-8ef0-fd9a0508ae38.aspx).</span></span>
  
<span data-ttu-id="4cc13-p106">[Configure mail flow using connectors in Office 365](http://technet.microsoft.com/library/854b5a50-4462-4836-a092-37e208d29624.aspx) apresenta conectores de EOP e mostra como você pode usá-los para personalizar o roteamento de email. Os cenários incluem garantir uma comunicação segura com uma organização parceira e configurar um host inteligente.</span><span class="sxs-lookup"><span data-stu-id="4cc13-p106">[Configure mail flow using connectors in Office 365](http://technet.microsoft.com/library/854b5a50-4462-4836-a092-37e208d29624.aspx) introduces connectors and shows how you can use them to customize mail routing. Scenarios include ensuring secure communication with a partner organization and setting up a smart host.</span></span> 
  
<span data-ttu-id="4cc13-118">Para garantir que o lixo eletrônico seja roteado corretamente para a pasta de lixo eletrônico de cada usuário, é necessário realizar alguns passos de configuração.</span><span class="sxs-lookup"><span data-stu-id="4cc13-118">To ensure that junk email is routed correctly to each user's junk-email folder, you must perform a couple configuration steps.</span></span> <span data-ttu-id="4cc13-119">Eles são detalhados [para garantir que o spam seja roteado para a pasta lixo eletrônico de cada usuário](../ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md).</span><span class="sxs-lookup"><span data-stu-id="4cc13-119">These are detailed in [Ensure that spam is routed to each user's Junk Email folder](../ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md).</span></span> <span data-ttu-id="4cc13-120">Se não quiser mover mensagens para a pasta de lixo eletrônico de cada usuário, você pode escolher outra ação editando suas políticas de filtro de conteúdo no centro de administração do Exchange.</span><span class="sxs-lookup"><span data-stu-id="4cc13-120">If you do not want to move messages to each user's junk-email folder, you may choose another action by editing your content filter policies in the Exchange admin center.</span></span> <span data-ttu-id="4cc13-121">Para saber mais, confira [Configure your spam filter policies](../configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="4cc13-121">For more information, see [Configure your spam filter policies](../configure-your-spam-filter-policies.md).</span></span>
  
## <a name="verify-mail-flow"></a><span data-ttu-id="4cc13-122">Verificar fluxo de mensagens</span><span class="sxs-lookup"><span data-stu-id="4cc13-122">Verify mail flow</span></span>

<span data-ttu-id="4cc13-p108">Para verificar se a sua instalação do EOP, incluindo a configuração de conectores, está funcionando corretamente, consulte a seção "Como saber se esta tarefa funcionou?" em [Configurar seu serviço EOP](set-up-your-eop-service.md).</span><span class="sxs-lookup"><span data-stu-id="4cc13-p108">To verify that your EOP setup, including your connector configuration, is working correctly, see the "How do you know this task worked?" section in [Set up your EOP service](set-up-your-eop-service.md).</span></span> 
  
<span data-ttu-id="4cc13-125">[Test Mail Flow with the Remote Connectivity Analyzer](http://technet.microsoft.com/library/6c8c2964-d553-4329-8166-6e508dd63fa0.aspx) fornece instruções para testar se seu fluxo de email está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="4cc13-125">[Test Mail Flow with the Remote Connectivity Analyzer](http://technet.microsoft.com/library/6c8c2964-d553-4329-8166-6e508dd63fa0.aspx) provides instructions for testing that your mail flow is set up correctly.</span></span> 
  


---
title: Criptografia do Office 365 para dados em trânsito
ms.author: krowley
author: kccross
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Resumo: uma breve explicação de como a Microsoft criptografa dados em trânsito.'
ms.openlocfilehash: 987e923e242b47b07ad1ef65e5c7ce791c27d5bd
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217501"
---
# <a name="office-365-encryption-for-data-in-transit"></a><span data-ttu-id="659d2-103">Criptografia do Office 365 para dados em trânsito</span><span class="sxs-lookup"><span data-stu-id="659d2-103">Office 365 encryption for data in transit</span></span>

<span data-ttu-id="659d2-104">Além de proteger os dados do cliente em repouso, a Microsoft usa tecnologias de criptografia para proteger os dados do cliente do Office 365 em trânsito.</span><span class="sxs-lookup"><span data-stu-id="659d2-104">In addition to protecting customer data at rest, Microsoft uses encryption technologies to protect Office 365 customer data in transit.</span></span> 

<span data-ttu-id="659d2-105">Os dados estão em trânsito:</span><span class="sxs-lookup"><span data-stu-id="659d2-105">Data is in transit:</span></span>
- <span data-ttu-id="659d2-106">Quando uma máquina cliente se comunica com um servidor do Office 365;</span><span class="sxs-lookup"><span data-stu-id="659d2-106">when a client machine communicates with an Office 365 server;</span></span>
- <span data-ttu-id="659d2-107">Quando um servidor do Office 365 se comunica com outro servidor do Office 365; e</span><span class="sxs-lookup"><span data-stu-id="659d2-107">when an Office 365 server communicates with another Office 365 server; and</span></span>
- <span data-ttu-id="659d2-108">Quando um servidor do Office 365 se comunica com um servidor não-Office 365 (por exemplo, o Exchange Online que entrega emails para um servidor de email externo).</span><span class="sxs-lookup"><span data-stu-id="659d2-108">when an Office 365 server communicates with a non-Office 365 server (e.g., Exchange Online delivering email to a foreign email server).</span></span>

<span data-ttu-id="659d2-p101">A comunicação entre o datacenter entre os servidores do Office 365 ocorre por meio de TLS ou IPsec, e todos os servidores voltados ao cliente negociam uma sessão segura usando TLS com máquinas clientes (por exemplo, o Exchange Online usa TLS 1,2 com intensidade de codificação de 256 bits é usado (FIPS 140-2 nível 2-validado). (Veja [detalhes técnicos de referência sobre criptografia no office 365](https://support.office.com/article/Technical-reference-details-about-encryption-in-Office-365-862CBE93-4268-4EF9-BA79-277545ECF221) para obter uma lista de pacotes de criptografia TLS compatíveis com o Office 365.) Isso se aplica aos protocolos usados por clientes como Outlook, Skype for Business e Outlook na Web (por exemplo, HTTP, POP3, etc.).</span><span class="sxs-lookup"><span data-stu-id="659d2-p101">Inter-datacenter communications between Office 365 servers takes place over TLS or IPsec, and all customer-facing servers negotiate a secure session using TLS with client machines (e.g., Exchange Online uses TLS 1.2 with 256-bit cipher strength is used (FIPS 140-2 Level 2-validated). (See [Technical reference details about encryption in Office 365](https://support.office.com/article/Technical-reference-details-about-encryption-in-Office-365-862CBE93-4268-4EF9-BA79-277545ECF221) for a list of TLS cipher suites supported by Office 365.) This applies to the protocols that are used by clients such as Outlook, Skype for Business, and Outlook on the web (e.g., HTTP, POP3, etc.).</span></span>

<span data-ttu-id="659d2-p102">Os certificados públicos são emitidos pelo SSL de ti da Microsoft usando o SSLAdmin, uma ferramenta interna da Microsoft para proteger a confidencialidade das informações transmitidas. Todos os certificados emitidos pela TI da Microsoft têm um mínimo de 2048 bits de [](http://www.webtrust.org/homepage-documents/item70372.pdf) duração, e a conformidade do WebTrust requer o SSLAdmin para garantir que os certificados sejam emitidos apenas para endereços IP públicos pertencentes à Microsoft. Qualquer endereço IP que não atenda a esse critério é roteado por meio de um processo de exceção.</span><span class="sxs-lookup"><span data-stu-id="659d2-p102">The public certificates are issued by Microsoft IT SSL using SSLAdmin, an internal Microsoft tool to protect confidentiality of transmitted information. All certificates issued by Microsoft IT have a minimum of 2048 bits in length, and [Webtrust](http://www.webtrust.org/homepage-documents/item70372.pdf) compliance requires SSLAdmin to make sure that certificates are issued only to public IP addresses owned by Microsoft. Any IP addresses that fail to meet this criterion are routed through an exception process.</span></span>

<span data-ttu-id="659d2-p103">Todos os detalhes de implementação, como a versão do TLS que está sendo usada, se o sigilo total (FS) está habilitado, a ordem de pacotes de codificação, etc., estão disponíveis publicamente. Uma maneira de ver esses detalhes é usar um site de terceiros, como laboratórios de Qualys SSL (www.ssllabs.com). Veja a seguir os links para páginas de teste automatizadas do Qualys que exibem informações sobre os seguintes serviços:</span><span class="sxs-lookup"><span data-stu-id="659d2-p103">All implementation details such as the version of TLS being used, whether Forward Secrecy (FS) is enabled, the order of cipher suites, etc., are available publicly. One way to see these details is to use a third-party website, such as Qualys SSL Labs (www.ssllabs.com). Below are the links to automated test pages from Qualys that display information for the following services:</span></span>
- [<span data-ttu-id="659d2-117">Portal do Office 365</span><span class="sxs-lookup"><span data-stu-id="659d2-117">Office 365 Portal</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=portal.office.com&hideResults=on)
- [<span data-ttu-id="659d2-118">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="659d2-118">Exchange Online</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=outlook.office365.com&hideResults=on)
- [<span data-ttu-id="659d2-119">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="659d2-119">SharePoint Online</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=microsoft-my.sharepoint.com&hideResults=on)
- [<span data-ttu-id="659d2-120">Skype for Business (SIP)</span><span class="sxs-lookup"><span data-stu-id="659d2-120">Skype for Business (SIP)</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=sipdir.online.lync.com)
- [<span data-ttu-id="659d2-121">Skype for Business (Web)</span><span class="sxs-lookup"><span data-stu-id="659d2-121">Skype for Business (Web)</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=webdir.online.lync.com&hideResults=on)
- [<span data-ttu-id="659d2-122">Proteção do Exchange Online</span><span class="sxs-lookup"><span data-stu-id="659d2-122">Exchange Online Protection</span></span>](https://ssl-tools.net/mailservers/microsoft-com.mail.protection.outlook.com)
- [<span data-ttu-id="659d2-123">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="659d2-123">Microsoft Teams</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=teams.microsoft.com&latest)

<span data-ttu-id="659d2-124">Para o Exchange Online Protection, as URLs variam de acordo com nomes de locatários; no entanto, todos os clientes podem testar o Office 365 usando o **Microsoft-com.mail.Protection.Outlook.com**.</span><span class="sxs-lookup"><span data-stu-id="659d2-124">For Exchange Online Protection, URLs vary by tenant names; however, all customers can test Office 365 using **microsoft-com.mail.protection.outlook.com**.</span></span>

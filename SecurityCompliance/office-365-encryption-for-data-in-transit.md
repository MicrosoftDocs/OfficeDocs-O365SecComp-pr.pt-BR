---
title: Criptografia do Office 365 para dados em trânsito
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Resumo: Uma breve explicação sobre como o Microsoft criptografa os dados em trânsito.'
ms.openlocfilehash: 8f4781cf1127fb1b6bf742c267c76e3df39b8209
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523509"
---
# <a name="office-365-encryption-for-data-in-transit"></a><span data-ttu-id="f17dc-103">Criptografia do Office 365 para dados em trânsito</span><span class="sxs-lookup"><span data-stu-id="f17dc-103">Office 365 encryption for data in transit</span></span>

<span data-ttu-id="f17dc-104">Além de proteger os dados em repouso do cliente, a Microsoft usa as tecnologias de criptografia para proteger os dados do cliente do Office 365 em trânsito.</span><span class="sxs-lookup"><span data-stu-id="f17dc-104">In addition to protecting customer data at rest, Microsoft uses encryption technologies to protect Office 365 customer data in transit.</span></span> 

<span data-ttu-id="f17dc-105">Dados estão em trânsito:</span><span class="sxs-lookup"><span data-stu-id="f17dc-105">Data is in transit:</span></span>
- <span data-ttu-id="f17dc-106">Quando um computador cliente se comunica com um servidor do Office 365;</span><span class="sxs-lookup"><span data-stu-id="f17dc-106">when a client machine communicates with an Office 365 server;</span></span>
- <span data-ttu-id="f17dc-107">Quando um servidor do Office 365 se comunica com outro servidor do Office 365; e</span><span class="sxs-lookup"><span data-stu-id="f17dc-107">when an Office 365 server communicates with another Office 365 server; and</span></span>
- <span data-ttu-id="f17dc-108">Quando um servidor do Office 365 se comunica com um servidor do Office 365 (por exemplo, o Exchange Online oferecendo email para um servidor de email externa).</span><span class="sxs-lookup"><span data-stu-id="f17dc-108">when an Office 365 server communicates with a non-Office 365 server (e.g., Exchange Online delivering email to a foreign email server).</span></span>

<span data-ttu-id="f17dc-p101">Comunicações de datacenter inter entre os servidores do Office 365 acontece sobre TLS ou IPsec, e todos os servidores voltados para o cliente negociam uma sessão segura usando TLS com as máquinas do cliente (por exemplo, o Exchange Online usa TLS 1.2 com o nível de codificação de 256 bits é usado (FIPS Nível de 140-2 validado por 2). (Consulte [detalhes de referência técnica sobre criptografia no Office 365](https://support.office.com/article/Technical-reference-details-about-encryption-in-Office-365-862CBE93-4268-4EF9-BA79-277545ECF221) para uma lista de conjuntos de codificação TLS suportados pelo Office 365). Isso se aplica aos protocolos que são usados por clientes como o Outlook, Skype para Outlook na web (por exemplo, HTTP, POP3, etc.) e de negócios.</span><span class="sxs-lookup"><span data-stu-id="f17dc-p101">Inter-datacenter communications between Office 365 servers takes place over TLS or IPsec, and all customer-facing servers negotiate a secure session using TLS with client machines (e.g., Exchange Online uses TLS 1.2 with 256-bit cipher strength is used (FIPS 140-2 Level 2-validated). (See [Technical reference details about encryption in Office 365](https://support.office.com/article/Technical-reference-details-about-encryption-in-Office-365-862CBE93-4268-4EF9-BA79-277545ECF221) for a list of TLS cipher suites supported by Office 365.) This applies to the protocols that are used by clients such as Outlook, Skype for Business, and Outlook on the web (e.g., HTTP, POP3, etc.).</span></span>

<span data-ttu-id="f17dc-p102">Os certificados públicos são emitidos por SSL de TI da Microsoft usando SSLAdmin, uma ferramenta interna da Microsoft para proteger a confidencialidade das informações transmitidas. Todos os certificados emitidos pela Microsoft IT tenham um mínimo de 2048 bits de comprimento e conformidade [Webtrust](http://www.webtrust.org/homepage-documents/item70372.pdf) requer SSLAdmin certificar-se de que os certificados são emitidos apenas para os endereços IP públicos pertencentes à Microsoft. Qualquer endereço IP que não atendem a este critério é roteado através de um processo de exceção.</span><span class="sxs-lookup"><span data-stu-id="f17dc-p102">The public certificates are issued by Microsoft IT SSL using SSLAdmin, an internal Microsoft tool to protect confidentiality of transmitted information. All certificates issued by Microsoft IT have a minimum of 2048 bits in length, and [Webtrust](http://www.webtrust.org/homepage-documents/item70372.pdf) compliance requires SSLAdmin to make sure that certificates are issued only to public IP addresses owned by Microsoft. Any IP addresses that fail to meet this criterion are routed through an exception process.</span></span>

<span data-ttu-id="f17dc-p103">Todos os detalhes da implementação, como a versão do TLS sendo usado, se encaminhar sigilo (FS) está habilitada, a ordem dos conjuntos de codificação, etc., estão disponíveis publicamente. Uma maneira de ver esses detalhes é usar um site de terceiros, como laboratórios de SSL Qualys (www.ssllabs.com). Abaixo estão os links para páginas de teste automatizado de Qualys que exibem informações para os seguintes serviços:</span><span class="sxs-lookup"><span data-stu-id="f17dc-p103">All implementation details such as the version of TLS being used, whether Forward Secrecy (FS) is enabled, the order of cipher suites, etc., are available publicly. One way to see these details is to use a third-party website, such as Qualys SSL Labs (www.ssllabs.com). Below are the links to automated test pages from Qualys that display information for the following services:</span></span>
- [<span data-ttu-id="f17dc-117">Portal do Office 365</span><span class="sxs-lookup"><span data-stu-id="f17dc-117">Office 365 Portal</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=portal.office.com&hideResults=on)
- [<span data-ttu-id="f17dc-118">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="f17dc-118">Exchange Online</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=outlook.office365.com&hideResults=on)
- [<span data-ttu-id="f17dc-119">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="f17dc-119">SharePoint Online</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=microsoft-my.sharepoint.com&hideResults=on)
- [<span data-ttu-id="f17dc-120">Skype para negócios (SIP)</span><span class="sxs-lookup"><span data-stu-id="f17dc-120">Skype for Business (SIP)</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=sipdir.online.lync.com)
- [<span data-ttu-id="f17dc-121">Skype para negócios (Web)</span><span class="sxs-lookup"><span data-stu-id="f17dc-121">Skype for Business (Web)</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=webdir.online.lync.com&hideResults=on)
- [<span data-ttu-id="f17dc-122">Proteção do Exchange Online</span><span class="sxs-lookup"><span data-stu-id="f17dc-122">Exchange Online Protection</span></span>](https://ssl-tools.net/mailservers/microsoft-com.mail.protection.outlook.com)
- [<span data-ttu-id="f17dc-123">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="f17dc-123">Microsoft Teams</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=teams.microsoft.com&latest)

<span data-ttu-id="f17dc-124">Para o Exchange Online Protection, URLs variam de acordo com nomes de locatário; No entanto, todos os clientes podem testar o Office 365 usando o **microsoft-com.mail.protection.outlook.com**.</span><span class="sxs-lookup"><span data-stu-id="f17dc-124">For Exchange Online Protection, URLs vary by tenant names; however, all customers can test Office 365 using **microsoft-com.mail.protection.outlook.com**.</span></span>

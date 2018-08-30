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
# <a name="office-365-encryption-for-data-in-transit"></a>Criptografia do Office 365 para dados em trânsito

Além de proteger os dados em repouso do cliente, a Microsoft usa as tecnologias de criptografia para proteger os dados do cliente do Office 365 em trânsito. 

Dados estão em trânsito:
- Quando um computador cliente se comunica com um servidor do Office 365;
- Quando um servidor do Office 365 se comunica com outro servidor do Office 365; e
- Quando um servidor do Office 365 se comunica com um servidor do Office 365 (por exemplo, o Exchange Online oferecendo email para um servidor de email externa).

Comunicações de datacenter inter entre os servidores do Office 365 acontece sobre TLS ou IPsec, e todos os servidores voltados para o cliente negociam uma sessão segura usando TLS com as máquinas do cliente (por exemplo, o Exchange Online usa TLS 1.2 com o nível de codificação de 256 bits é usado (FIPS Nível de 140-2 validado por 2). (Consulte [detalhes de referência técnica sobre criptografia no Office 365](https://support.office.com/article/Technical-reference-details-about-encryption-in-Office-365-862CBE93-4268-4EF9-BA79-277545ECF221) para uma lista de conjuntos de codificação TLS suportados pelo Office 365). Isso se aplica aos protocolos que são usados por clientes como o Outlook, Skype para Outlook na web (por exemplo, HTTP, POP3, etc.) e de negócios.

Os certificados públicos são emitidos por SSL de TI da Microsoft usando SSLAdmin, uma ferramenta interna da Microsoft para proteger a confidencialidade das informações transmitidas. Todos os certificados emitidos pela Microsoft IT tenham um mínimo de 2048 bits de comprimento e conformidade [Webtrust](http://www.webtrust.org/homepage-documents/item70372.pdf) requer SSLAdmin certificar-se de que os certificados são emitidos apenas para os endereços IP públicos pertencentes à Microsoft. Qualquer endereço IP que não atendem a este critério é roteado através de um processo de exceção.

Todos os detalhes da implementação, como a versão do TLS sendo usado, se encaminhar sigilo (FS) está habilitada, a ordem dos conjuntos de codificação, etc., estão disponíveis publicamente. Uma maneira de ver esses detalhes é usar um site de terceiros, como laboratórios de SSL Qualys (www.ssllabs.com). Abaixo estão os links para páginas de teste automatizado de Qualys que exibem informações para os seguintes serviços:
- [Portal do Office 365](https://www.ssllabs.com/ssltest/analyze.html?d=portal.office.com&hideResults=on)
- [Exchange Online](https://www.ssllabs.com/ssltest/analyze.html?d=outlook.office365.com&hideResults=on)
- [SharePoint Online](https://www.ssllabs.com/ssltest/analyze.html?d=microsoft-my.sharepoint.com&hideResults=on)
- [Skype para negócios (SIP)](https://www.ssllabs.com/ssltest/analyze.html?d=sipdir.online.lync.com)
- [Skype para negócios (Web)](https://www.ssllabs.com/ssltest/analyze.html?d=webdir.online.lync.com&hideResults=on)
- [Proteção do Exchange Online](https://ssl-tools.net/mailservers/microsoft-com.mail.protection.outlook.com)
- [Microsoft Teams](https://www.ssllabs.com/ssltest/analyze.html?d=teams.microsoft.com&latest)

Para o Exchange Online Protection, URLs variam de acordo com nomes de locatário; No entanto, todos os clientes podem testar o Office 365 usando o **microsoft-com.mail.protection.outlook.com**.

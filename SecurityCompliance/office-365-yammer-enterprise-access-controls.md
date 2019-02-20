---
title: Controles de acesso corporativo do Office 365 Yammer
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
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: 'Resumo: um breve resumo sobre os controles de acesso corporativo do Yammer no ambiente de produção.'
ms.openlocfilehash: 33126ee6acf42a97148c12917855535a8578e8cf
ms.sourcegitcommit: c94cb88a9ce5bcc2d3c558f0fcc648519cc264a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2019
ms.locfileid: "30090723"
---
# <a name="yammer-enterprise-access-controls"></a><span data-ttu-id="b4c47-103">Controles de acesso do Yammer Enterprise</span><span class="sxs-lookup"><span data-stu-id="b4c47-103">Yammer Enterprise Access Controls</span></span> 

<span data-ttu-id="b4c47-p101">O acesso físico e lógico ao ambiente de produção do Yammer é restrito a um conjunto muito pequeno de pessoas (infraestrutura e operações). Como em outros engenheiros do Office 365, os engenheiros do Yammer têm zero acesso à dados dos clientes. O acesso deve ser solicitado usando um sistema de controle de acesso just-in-time baseado em aprovação semelhante ao Lockbox, e há um número limitado de aprovadores. Os aprovadores verificam a solicitação (por exemplo, eles verificam se a solicitação é legítima com base em necessidade, caso de negócios, hora etc.) e, em seguida, aprovar ou negar a solicitação. Se a solicitação for aprovada, o acesso JIT será concedido para um tempo definido e limitado, após o qual ele expirará automaticamente.</span><span class="sxs-lookup"><span data-stu-id="b4c47-p101">Both physical and logical access to the Yammer production environment is restricted to a very small set of people (infrastructure and operations). As with other Office 365 engineers, Yammer engineers have zero standing access to Customer Data. Access must be requested using an approval-based just-in-time access control system similar to Lockbox, and there is a limited number of approvers. Approvers verify the request (e.g., they verify whether the request is legitimate based on need, business case, time, etc.), and then approve or deny the request. If the request is approved, JIT access is granted for a defined and limited time, after which it automatically expires.</span></span> 

<span data-ttu-id="b4c47-p102">Como em outros serviços do Office 365, todo o acesso ao ambiente de produção do Yammer aproveita a autenticação multifator. Todos os acessos e o histórico de comandos são atribuídos a um usuário e registrados e revisados regularmente pela equipe de segurança do Yammer.</span><span class="sxs-lookup"><span data-stu-id="b4c47-p102">As with other Office 365 services, all access to the Yammer production environment leverages multi-factor authentication. All access and command history is attributed to a user, and logged and reviewed regularly by the Yammer security team.</span></span>

<span data-ttu-id="b4c47-111">Para obter mais informações sobre administração e gerenciamento do Yammer, consulte [ajuda do administrador do Yammer](https://support.office.com/article/yammer-–-admin-help-e1464355-1f97-49ac-b2aa-dd320b179dbe?ui=en-US&rs=en-US&ad=US).</span><span class="sxs-lookup"><span data-stu-id="b4c47-111">For more information about Yammer administration and management, see [Yammer Admin Help](https://support.office.com/article/yammer-–-admin-help-e1464355-1f97-49ac-b2aa-dd320b179dbe?ui=en-US&rs=en-US&ad=US).</span></span>
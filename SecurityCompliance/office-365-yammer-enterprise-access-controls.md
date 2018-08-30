---
title: Controles de acesso do Office 365 Yammer Enterprise
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
description: 'Resumo: Um breve resumo sobre controles de acesso do Yammer Enterprise no ambiente de produção.'
ms.openlocfilehash: 3f51e63c16022353e743b57d8e977f2ea2e6a835
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524576"
---
# <a name="yammer-enterprise-access-controls"></a><span data-ttu-id="596c7-103">Controles de acesso do Yammer Enterprise</span><span class="sxs-lookup"><span data-stu-id="596c7-103">Yammer Enterprise Access Controls</span></span> 

<span data-ttu-id="596c7-p101">Acesso físico e lógico para o ambiente de produção do Yammer é restrito a um conjunto muito pequeno de pessoas (infra-estrutura e operações). Assim como acontece com outros engenheiros do Office 365, Yammer engenheiros tem zero acessar a posição dados dos clientes. Acesso deve ser solicitado usando um sistema de controle de acesso baseado em aprovação de just-in-time semelhante a Lockbox e há um número limitado de aprovadores. Aprovadores verificar a solicitação (por exemplo, eles verificar que se a solicitação é legítima com base na necessidade, caso comercial, tempo, etc.) e, em seguida, aprovar ou negar a solicitação. Se a solicitação for aprovada, acesso JIT é concedido por um período definido e limitado, após o qual ele expira automaticamente.</span><span class="sxs-lookup"><span data-stu-id="596c7-p101">Both physical and logical access to the Yammer production environment is restricted to a very small set of people (infrastructure and operations). As with other Office 365 engineers, Yammer engineers have zero standing access to Customer Data. Access must be requested using an approval-based just-in-time access control system similar to Lockbox, and there is a limited number of approvers. Approvers verify the request (e.g., they verify whether the request is legitimate based on need, business case, time, etc.), and then approve or deny the request. If the request is approved, JIT access is granted for a defined and limited time, after which it automatically expires.</span></span> 

<span data-ttu-id="596c7-p102">Assim como acontece com outros serviços do Office 365, todo o acesso ao ambiente de produção do Yammer utiliza a autenticação multifator. Todo o histórico de acesso e o comando é atribuído a um usuário e conectado e revisado regularmente pela equipe de segurança do Yammer.</span><span class="sxs-lookup"><span data-stu-id="596c7-p102">As with other Office 365 services, all access to the Yammer production environment leverages multi-factor authentication. All access and command history is attributed to a user, and logged and reviewed regularly by the Yammer security team.</span></span>

<span data-ttu-id="596c7-111">Para obter mais informações sobre o Yammer administração e gerenciamento, consulte a [Ajuda de administração no Yammer](https://support.office.com/article/yammer-–-admin-help-e1464355-1f97-49ac-b2aa-dd320b179dbe?ui=en-US&rs=en-US&ad=US).</span><span class="sxs-lookup"><span data-stu-id="596c7-111">For more information about Yammer administration and management, see [Yammer Admin Help](https://support.office.com/article/yammer-–-admin-help-e1464355-1f97-49ac-b2aa-dd320b179dbe?ui=en-US&rs=en-US&ad=US).</span></span>
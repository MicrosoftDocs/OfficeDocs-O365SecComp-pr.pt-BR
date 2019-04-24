---
title: Controles de acesso corporativo do Office 365 Yammer
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: 'Resumo: um breve resumo sobre os controles de acesso corporativo do Yammer no ambiente de produção.'
ms.openlocfilehash: 61598235a010aaa1c578c449cb054073212a41f9
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262343"
---
# <a name="yammer-enterprise-access-controls"></a><span data-ttu-id="8a3fd-103">Controles de acesso do Yammer Enterprise</span><span class="sxs-lookup"><span data-stu-id="8a3fd-103">Yammer Enterprise Access Controls</span></span> 

<span data-ttu-id="8a3fd-104">O acesso físico e lógico ao ambiente de produção do Yammer é restrito a um conjunto muito pequeno de pessoas (infraestrutura e operações).</span><span class="sxs-lookup"><span data-stu-id="8a3fd-104">Both physical and logical access to the Yammer production environment is restricted to a very small set of people (infrastructure and operations).</span></span> <span data-ttu-id="8a3fd-105">Como em outros engenheiros do Office 365, os engenheiros do Yammer têm zero acesso à dados dos clientes.</span><span class="sxs-lookup"><span data-stu-id="8a3fd-105">As with other Office 365 engineers, Yammer engineers have zero standing access to Customer Data.</span></span> <span data-ttu-id="8a3fd-106">O acesso deve ser solicitado usando um sistema de controle de acesso just-in-time baseado em aprovação semelhante ao Lockbox, e há um número limitado de aprovadores.</span><span class="sxs-lookup"><span data-stu-id="8a3fd-106">Access must be requested using an approval-based just-in-time access control system similar to Lockbox, and there is a limited number of approvers.</span></span> <span data-ttu-id="8a3fd-107">Os aprovadores verificam a solicitação (por exemplo, eles verificam se a solicitação é legítima com base em necessidade, caso de negócios, hora etc.) e, em seguida, aprovar ou negar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="8a3fd-107">Approvers verify the request (e.g., they verify whether the request is legitimate based on need, business case, time, etc.), and then approve or deny the request.</span></span> <span data-ttu-id="8a3fd-108">Se a solicitação for aprovada, o acesso JIT será concedido para um tempo definido e limitado, após o qual ele expirará automaticamente.</span><span class="sxs-lookup"><span data-stu-id="8a3fd-108">If the request is approved, JIT access is granted for a defined and limited time, after which it automatically expires.</span></span> 

<span data-ttu-id="8a3fd-109">Como em outros serviços do Office 365, todo o acesso ao ambiente de produção do Yammer aproveita a autenticação multifator.</span><span class="sxs-lookup"><span data-stu-id="8a3fd-109">As with other Office 365 services, all access to the Yammer production environment leverages multi-factor authentication.</span></span> <span data-ttu-id="8a3fd-110">Todos os acessos e o histórico de comandos são atribuídos a um usuário e registrados e revisados regularmente pela equipe de segurança do Yammer.</span><span class="sxs-lookup"><span data-stu-id="8a3fd-110">All access and command history is attributed to a user, and logged and reviewed regularly by the Yammer security team.</span></span>

<span data-ttu-id="8a3fd-111">Para obter mais informações sobre administração e gerenciamento do Yammer, consulte [ajuda do administrador do Yammer](https://support.office.com/article/yammer-–-admin-help-e1464355-1f97-49ac-b2aa-dd320b179dbe?ui=en-US&rs=en-US&ad=US).</span><span class="sxs-lookup"><span data-stu-id="8a3fd-111">For more information about Yammer administration and management, see [Yammer Admin Help](https://support.office.com/article/yammer-–-admin-help-e1464355-1f97-49ac-b2aa-dd320b179dbe?ui=en-US&rs=en-US&ad=US).</span></span>
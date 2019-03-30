---
title: Office 365 lidando com corrupção de dados
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
description: Uma explicação sobre corrupção de dados no Office 365 e esforços de prevenção e recuperação da Microsoft.
ms.openlocfilehash: 9bf55243399ecd9f01f736e2da70d7c07231fa63
ms.sourcegitcommit: 1261a37c414111f869df5791548a768d853fda60
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/30/2019
ms.locfileid: "31004088"
---
# <a name="dealing-with-data-corruption-in-office-365"></a><span data-ttu-id="e2430-103">Lidando com corrupção de dados no Office 365</span><span class="sxs-lookup"><span data-stu-id="e2430-103">Dealing with Data Corruption in Office 365</span></span>

<span data-ttu-id="e2430-104">Um dos aspectos desafiadores de execução de um serviço de nuvem em larga escala é como lidar com a corrupção de dados, considerando o grande volume de dados e sistemas independentes.</span><span class="sxs-lookup"><span data-stu-id="e2430-104">One of the challenging aspects of running a large-scale cloud service is how to handle data corruption, given the large volume of data and independent systems.</span></span> <span data-ttu-id="e2430-105">A corrupção dos dados pode ser causada por:</span><span class="sxs-lookup"><span data-stu-id="e2430-105">Data corruption can be caused by:</span></span>
- <span data-ttu-id="e2430-106">Erros de infraestrutura ou aplicativo, corrompendo parte ou todo o estado do aplicativo</span><span class="sxs-lookup"><span data-stu-id="e2430-106">Application or infrastructure bugs, corrupting some or all of the application state</span></span> 
- <span data-ttu-id="e2430-107">Problemas de hardware que resultam em perda de dados ou incapacidade de ler dados</span><span class="sxs-lookup"><span data-stu-id="e2430-107">Hardware issues that result in lost data or an inability to read data</span></span> 
- <span data-ttu-id="e2430-108">Erros operacionais humanos</span><span class="sxs-lookup"><span data-stu-id="e2430-108">Human operational errors</span></span> 
- <span data-ttu-id="e2430-109">Hackers mal-intencionados e funcionários descontentes</span><span class="sxs-lookup"><span data-stu-id="e2430-109">Malicious hackers and disgruntled employees</span></span> 
- <span data-ttu-id="e2430-110">Incidentes em serviços externos que resultam em alguma perda de dados</span><span class="sxs-lookup"><span data-stu-id="e2430-110">Incidents in external services that result in some loss of data</span></span> 

<span data-ttu-id="e2430-111">Como a maior resiliência na integridade dos dados significa menos incidentes de corrupção de dados, a Microsoft incorporou os mecanismos de proteção do Office 365 para evitar que os danos ocorram, bem como sistemas e processos que nos permitam recuperar dados, se houver.</span><span class="sxs-lookup"><span data-stu-id="e2430-111">Because greater resiliency in data integrity means fewer data corruption incidents, Microsoft has built into Office 365 protection mechanisms to prevent corruption from happening, as well as systems and processes that enable us to recover data if it does.</span></span> <span data-ttu-id="e2430-112">Os cheques e processos existem dentro dos vários estágios do processo de lançamento da engenharia para aumentar a resiliência contra corrupção de dados, incluindo:</span><span class="sxs-lookup"><span data-stu-id="e2430-112">Checks and processes exist within the various stages of the engineering release process to increase resiliency against data corruption, including:</span></span>
- <span data-ttu-id="e2430-113">Design de sistema</span><span class="sxs-lookup"><span data-stu-id="e2430-113">System Design</span></span>
- <span data-ttu-id="e2430-114">Organização e estrutura de código</span><span class="sxs-lookup"><span data-stu-id="e2430-114">Code organization and structure</span></span> 
- <span data-ttu-id="e2430-115">Revisão de código</span><span class="sxs-lookup"><span data-stu-id="e2430-115">Code review</span></span> 
- <span data-ttu-id="e2430-116">Testes de unidade, testes de integração e testes de sistema</span><span class="sxs-lookup"><span data-stu-id="e2430-116">Unit tests, integration tests, and system tests</span></span>
- <span data-ttu-id="e2430-117">Testes/Gates dos fios de viagem</span><span class="sxs-lookup"><span data-stu-id="e2430-117">Trip wires tests/gates</span></span> 

<span data-ttu-id="e2430-118">Nos ambientes de produção do Office 365, a replicação de mesmo nível entre data centers garante que sempre haja várias cópias ao vivo de qualquer dado.</span><span class="sxs-lookup"><span data-stu-id="e2430-118">Within Office 365 production environments, peer replication between datacenters ensures that there are always multiple live copies of any data.</span></span> <span data-ttu-id="e2430-119">Imagens e scripts padrão são usados para recuperar servidores perdidos e dados replicados são usados para restaurar dados do cliente.</span><span class="sxs-lookup"><span data-stu-id="e2430-119">Standard images and scripts are used to recover lost servers, and replicated data is used to restore customer data.</span></span> <span data-ttu-id="e2430-120">Devido às verificações e processos de resiliência de dados internos, a Microsoft mantém backups somente da documentação do sistema de informações do Office 365 (incluindo documentação relacionada à segurança), usando a replicação interna no SharePoint Online e nosso código interno ferramenta de repositório, depósito de origem.</span><span class="sxs-lookup"><span data-stu-id="e2430-120">Because of the built-in data resiliency checks and processes, Microsoft maintains backups only of Office 365 information system documentation (including security-related documentation), using built-in replication in SharePoint Online and our internal code repository tool, Source Depot.</span></span> <span data-ttu-id="e2430-121">A documentação do sistema está armazenada no SharePoint Online e o depósito de origem contém imagens de sistema e de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e2430-121">System documentation is stored in SharePoint Online, and Source Depot contains system and application images.</span></span> <span data-ttu-id="e2430-122">O SharePoint Online e o Source Depot usam o controle de versão e são replicados quase em tempo real.</span><span class="sxs-lookup"><span data-stu-id="e2430-122">Both SharePoint Online and Source Depot use versioning and are replicated in near real-time.</span></span> 
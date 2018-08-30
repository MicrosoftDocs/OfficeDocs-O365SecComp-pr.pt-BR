---
title: O Office 365 lidando com corrupção de dados
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
description: Uma explicação dos corrupção de dados no Office 365 e esforços da Microsoft de prevenção e recuperação.
ms.openlocfilehash: 087be23ce5dad1daf62357cb08e27c0a15962792
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524147"
---
# <a name="dealing-with-data-corruption-in-office-365"></a><span data-ttu-id="59b93-103">Lidando com corrupção de dados no Office 365</span><span class="sxs-lookup"><span data-stu-id="59b93-103">Dealing with Data Corruption in Office 365</span></span>

<span data-ttu-id="59b93-p101">Um dos aspectos desafiadoras da execução de um serviço em nuvem em larga escala é como lidar com a corrupção de dados, recebe um grande volume de dados e sistemas independentes. Corrupção de dados pode ser causada por:</span><span class="sxs-lookup"><span data-stu-id="59b93-p101">One of the challenging aspects of running a large-scale cloud service is how to handle data corruption, given the large volume of data and independent systems. Data corruption can be caused by:</span></span>
- <span data-ttu-id="59b93-106">Aplicativo ou infraestrutura bugs, corromper parte ou todo o estado do aplicativo</span><span class="sxs-lookup"><span data-stu-id="59b93-106">Application or infrastructure bugs, corrupting some or all of the application state</span></span> 
- <span data-ttu-id="59b93-107">Problemas de hardware que resultam em perda de dados ou incapacidade de ler dados</span><span class="sxs-lookup"><span data-stu-id="59b93-107">Hardware issues that result in lost data or an inability to read data</span></span> 
- <span data-ttu-id="59b93-108">Erros operacionais humanos</span><span class="sxs-lookup"><span data-stu-id="59b93-108">Human operational errors</span></span> 
- <span data-ttu-id="59b93-109">Hackers mal-intencionados e funcionários insatisfeitos</span><span class="sxs-lookup"><span data-stu-id="59b93-109">Malicious hackers and disgruntled employees</span></span> 
- <span data-ttu-id="59b93-110">Em serviços externos que resultar em alguma perda de dados de incidentes</span><span class="sxs-lookup"><span data-stu-id="59b93-110">Incidents in external services that result in some loss of data</span></span> 

<span data-ttu-id="59b93-p102">Como maior resiliência em integridade dos dados significa menos incidentes de corrupção de dados, o Microsoft incorporou em mecanismos de proteção do Office 365 para evitar corrupção de aconteça, bem como sistemas e processos que permitem conosco recuperar dados, se existir. Verificações e processos existirem dentro aos vários estágios do processo de lançamento de engenharia para aumentar a resiliência contra corrupção de dados, incluindo:</span><span class="sxs-lookup"><span data-stu-id="59b93-p102">Because greater resiliency in data integrity means fewer data corruption incidents, Microsoft has built into Office 365 protection mechanisms to prevent corruption from happening, as well as systems and processes that enable us to recover data if it does. Checks and processes exist within the various stages of the engineering release process to increase resiliency against data corruption, including:</span></span>
- <span data-ttu-id="59b93-113">Design do sistema</span><span class="sxs-lookup"><span data-stu-id="59b93-113">System Design</span></span>
- <span data-ttu-id="59b93-114">Código de organização e estrutura</span><span class="sxs-lookup"><span data-stu-id="59b93-114">Code organization and structure</span></span> 
- <span data-ttu-id="59b93-115">Revisão de código</span><span class="sxs-lookup"><span data-stu-id="59b93-115">Code review</span></span> 
- <span data-ttu-id="59b93-116">Testes de unidade, testes de integração e testes do sistema</span><span class="sxs-lookup"><span data-stu-id="59b93-116">Unit tests, integration tests, and system tests</span></span>
- <span data-ttu-id="59b93-117">Viagem conecta/entradas de testes</span><span class="sxs-lookup"><span data-stu-id="59b93-117">Trip wires tests/gates</span></span> 

<span data-ttu-id="59b93-p103">Em ambientes de produção do Office 365, a replicação de ponto entre data centers garante que sempre existem várias cópias ao vivo de todos os dados. Scripts e arquivos de imagens padrão são usados para recuperar servidores perdidos e dados replicados são usados para restaurar dados do cliente. Devido às verificações de resiliência de dados interno e processos, a Microsoft mantém backups apenas de documentação do Office 365 informações sistema (incluindo documentação relacionada à segurança), usando a replicação interna no SharePoint Online e o nosso código interno ferramenta do repositório, depósito de origem. Documentação do sistema é armazenada no SharePoint Online e depósito de origem contém as imagens de sistema e de aplicativo. SharePoint Online e depósito de origem usam o controle de versão e são replicados em praticamente em tempo real.</span><span class="sxs-lookup"><span data-stu-id="59b93-p103">Within Office 365 production environments, peer replication between datacenters ensures that there are always multiple live copies of any data. Standard images and scripts are used to recover lost servers, and replicated data is used to restore customer data. Because of the built-in data resiliency checks and processes, Microsoft maintains backups only of Office 365 information system documentation (including security-related documentation), using built-in replication in SharePoint Online and our internal code repository tool, Source Depot. System documentation is stored in SharePoint Online, and Source Depot contains system and application images. Both SharePoint Online and Source Depot use versioning and are replicated in near real-time.</span></span> 
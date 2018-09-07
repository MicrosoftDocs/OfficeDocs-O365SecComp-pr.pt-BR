---
title: RGPD para Project Server
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
ms.custom: ''
localization_priority: Priority
description: Saiba mais sobre como atender aos requisitos de RGPD no Project Server local.
ms.openlocfilehash: aa74f29e522f24f330db6e53c7c81bc5b708bcf0
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272146"
---
# <a name="gdpr-for-project-server"></a><span data-ttu-id="83357-103">RGPD para Project Server</span><span class="sxs-lookup"><span data-stu-id="83357-103">GDPR for Project Server</span></span>

<span data-ttu-id="83357-p101">O Project Server usa scripts personalizados para exportar e ocultar dados do usuário no Project Web App. O processo básico é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="83357-p101">Project Server uses custom scripts to export and redact user data in Project Web App. The basic process is:</span></span>

1.  <span data-ttu-id="83357-106">Encontre os sites do Project Web App em seu farm.</span><span class="sxs-lookup"><span data-stu-id="83357-106">Find the Project Web App sites in your farm.</span></span>

2.  <span data-ttu-id="83357-107">Encontre os projetos que contêm o usuário em cada site.</span><span class="sxs-lookup"><span data-stu-id="83357-107">Find the projects in each site that contain the user.</span></span>

3.  <span data-ttu-id="83357-108">Exporte e verifique os tipos de dados que você deseja analisar.</span><span class="sxs-lookup"><span data-stu-id="83357-108">Export and review the types of data that you want to review.</span></span>

4.  <span data-ttu-id="83357-109">Oculte os dados conforme for necessário.</span><span class="sxs-lookup"><span data-stu-id="83357-109">Redact data as needed.</span></span>

<span data-ttu-id="83357-110">Estas etapas são abordadas em detalhes nos seguintes artigos:</span><span class="sxs-lookup"><span data-stu-id="83357-110">These steps are covered in detail in the following articles:</span></span>

- [<span data-ttu-id="83357-111">Exportar dados do usuário do Project Server</span><span class="sxs-lookup"><span data-stu-id="83357-111">Export user data from Project Server</span></span>](/Project/export-user-data-from-project-server?toc=/Office365/Enterprise/toc.json)

- [<span data-ttu-id="83357-112">Excluir dados do usuário do Project Server</span><span class="sxs-lookup"><span data-stu-id="83357-112">Delete user data from Project Server</span></span>](/Project/delete-user-data-from-project-server?toc=/Office365/Enterprise/toc.json)


<span data-ttu-id="83357-p102">Observe que o Project Server foi criado a partir do SharePoint Server e que ele registra eventos nos logs de ULS do SharePoint e no banco de dados de uso. Consulte [RGPD para SharePoint Server](gdpr-for-sharepoint-server.md) para ter mais informações.</span><span class="sxs-lookup"><span data-stu-id="83357-p102">Note that Project Server is built on top of SharePoint Server and logs events to the SharePoint ULS logs and Usage database.</span></span>

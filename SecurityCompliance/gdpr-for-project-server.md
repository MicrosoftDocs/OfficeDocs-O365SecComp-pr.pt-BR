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
# <a name="gdpr-for-project-server"></a>RGPD para Project Server

O Project Server usa scripts personalizados para exportar e ocultar dados do usuário no Project Web App. O processo básico é o seguinte:

1.  Encontre os sites do Project Web App em seu farm.

2.  Encontre os projetos que contêm o usuário em cada site.

3.  Exporte e verifique os tipos de dados que você deseja analisar.

4.  Oculte os dados conforme for necessário.

Estas etapas são abordadas em detalhes nos seguintes artigos:

- [Exportar dados do usuário do Project Server](/Project/export-user-data-from-project-server?toc=/Office365/Enterprise/toc.json)

- [Excluir dados do usuário do Project Server](/Project/delete-user-data-from-project-server?toc=/Office365/Enterprise/toc.json)


Observe que o Project Server foi criado a partir do SharePoint Server e que ele registra eventos nos logs de ULS do SharePoint e no banco de dados de uso. Consulte [RGPD para SharePoint Server](gdpr-for-sharepoint-server.md) para ter mais informações.

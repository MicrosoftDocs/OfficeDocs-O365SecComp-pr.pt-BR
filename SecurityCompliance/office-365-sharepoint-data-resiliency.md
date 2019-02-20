---
title: Resiliência de dados do SharePoint para o Office 365
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
description: Uma visão geral da resiliência de dados no SharePoint Online no Office 365.
ms.openlocfilehash: c550cb6572cb71b53cd544af64339129f72b888f
ms.sourcegitcommit: c94cb88a9ce5bcc2d3c558f0fcc648519cc264a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2019
ms.locfileid: "30090883"
---
# <a name="sharepoint-online-data-resiliency"></a>Resiliência de dados do SharePoint Online
Um princípio importante para O SharePoint Online nunca tem uma cópia única de qualquer parte dos dados. O SharePoint Online usa a replicação do SQL Server, que é um conjunto de tecnologias para copiar e distribuir dados e objetos de banco de dados de um banco de dados para outro e, em seguida, sincronizar entre bancos de dados para manter a consistência. 

Por exemplo, quando um usuário salva um arquivo no SharePoint Online, o arquivo é fragmentado, criptografado e armazenado no armazenamento de blob do Azure. O serviço de blob do Azure fornece mecanismos para garantir a integridade dos dados no aplicativo e nas camadas de transporte. Esta postagem detalha esses mecanismos da perspectiva do serviço e do cliente. A verificação de MD5 é opcional em operações colocar e obter; no entanto, ele fornece um recurso de conveniência para garantir a integridade dos dados na rede ao usar HTTP. Além disso, como o HTTPS fornece a verificação de MD5 adicional de segurança de camada de transporte, não é necessária enquanto se conecta via HTTPS, pois seria redundante. O serviço de blob do Azure fornece uma mídia de armazenamento durável e usa sua própria verificação de integridade para dados armazenados. O MD5's usado na interação com um aplicativo é fornecido para verificar a integridade dos dados ao transferir esses dados entre o aplicativo e o serviço via HTTP. 

Para garantir a integridade dos dados, o serviço de blob do Azure usa hashes MD5 dos dados em um conjunto diferente de Manners. É importante entender como esses valores são calculados, transmitidos, armazenados e, eventualmente, impostos para projetar apropriadamente o seu aplicativo a fim de usá-los para fornecer integridade de dados. Para obter mais informações, consulte [visão geral do Microsoft Azure Blob MD5](http://blogs.msdn.com/b/windowsazurestorage/archive/2011/02/18/windows-azure-blob-md5-overview.aspx). 

Os metadados e ponteiros para o arquivo são armazenados em um banco de dados do SQL Server (o banco de dados de conteúdo). Todos os blocos – arquivos, partes de arquivos e deltas de atualização – são armazenados como BLOBs no armazenamento do Azure que são distribuídos aleatoriamente em várias contas de armazenamento do Azure. O banco de dados SQL está hospedado em uma matriz de armazenamento RAID 10 que é espelhada de forma síncrona para outra matriz de armazenamento RAID 10 em um rack separado dentro do mesmo datacenter. O envio de logs assíncrono é usado para replicar os dados para outra matriz de armazenamento RAID 10 em um segundo datacenter. Além de proteger os dados com RAID 10 e replicação síncrona e assíncrona, são realizados backups de dados agendados que também são replicados de forma assíncrona para o segundo datacenter. 

No SharePoint Online, os backups de dados são realizados a cada 12 horas e mantidos por 14 dias. O SharePoint Online também usa um sistema de espera ativa que inclui datacenters geograficamente separados em pares dentro da mesma região de local de dados do cliente (por exemplo, Chicago e a San Antonio para clientes que provisionaram seus locatários nos Estados Unidos) configurado como ativo/ativo. Por exemplo, há usuários ativos que têm Chicago como datacenter principal e Antonio de San como um datacenter de failover e usuários ativos que têm San Antonio como seu datacenter principal e Chicago como datacenter de failover. 
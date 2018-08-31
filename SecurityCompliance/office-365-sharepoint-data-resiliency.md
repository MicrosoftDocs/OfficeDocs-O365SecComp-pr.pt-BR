---
title: Resiliência de dados do SharePoint do Office 365
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
description: Visão geral de resiliência de dados no SharePoint Online no Office 365.
ms.openlocfilehash: ba6259e8e582a4abcf0f184b162177119a57718f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524056"
---
# <a name="sharepoint-online-data-resiliency"></a>Resiliência de dados Online do SharePoint
Um princípio chave para o SharePoint Online é nunca ter uma única cópia de qualquer parte dos dados. SharePoint Online usa a replicação do SQL Server, o que é um conjunto de tecnologias para copiar e distribuir os objetos de dados e o banco de dados de um banco de dados para outro e depois sincronizar os bancos de dados para manter a consistência. 

Por exemplo, quando um usuário salvar um arquivo no SharePoint Online, o arquivo está em partes, criptografado e armazenado no armazenamento de Blob do Azure. Serviço de Blob Azure fornece mecanismos para garantir a integridade dos dados ambas nas camadas de aplicativo e de transporte. Esta postagem em detalhes esses mecanismos da perspectiva do cliente e de serviço. Verificação de MD5 é opcional nas operações de colocar e obter; No entanto, ele oferece um recurso de conveniência para garantir a integridade dos dados através da rede durante usando HTTP. Além disso, como HTTPS fornece segurança de camada de transporte adicionais verificando MD5 não é necessário ao se conectar via HTTPS, como seria redundante. Serviço de Blob Azure fornece um meio de armazenamento durável e usa seu próprio integridade verificação dos dados armazenados. O MD5 que são usadas quando interagindo com um aplicativo são fornecidos para verificar a integridade dos dados durante a transferência de dados entre o aplicativo e o serviço via HTTP. 

Para garantir a integridade dos dados Blob o Azure serviço usa hashes MD5 dos dados em algumas maneiras diferentes. É importante compreender como esses valores são calculados, transmitidos, armazenados e eventualmente impostos para desenhar apropriadamente seu aplicativo para utilizá-las para fornecer a integridade dos dados. Para obter mais informações, consulte [Visão geral do Windows Azure Blob MD5](http://blogs.msdn.com/b/windowsazurestorage/archive/2011/02/18/windows-azure-blob-md5-overview.aspx). 

Ponteiros para o arquivo e os metadados são armazenados em um banco de dados do SQL Server (o banco de dados). Todos os blocos – arquivos, partes de arquivos e atualização deltas – são armazenados como blobs no armazenamento do Azure aleatoriamente distribuídas em várias contas de armazenamento do Azure. O banco de dados do SQL está hospedado em uma matriz de armazenamento RAID 10 qual espelhada de forma síncrona a outra matriz de armazenamento RAID 10 em um rack separado no mesmo datacenter. Envio de log assíncrono é usado para replicar os dados para outro matriz de armazenamento RAID 10 em um segundo data center. Além de proteção de dados com RAID 10 e replicação síncrona e assíncrona, são realizados backups de dados agendados também de forma assíncrona, que são replicados para o segundo datacenter. 

No SharePoint Online, os backups de dados são executados a cada 12 horas e mantidos para 14 dias. SharePoint Online também usa um sistema em espera ativa que inclui os centros de dados geograficamente separados emparelhados com o mesmo cliente dados local região (por exemplo, Chicago e San Antonio para clientes que tenham configurados seus locatários nos Estados Unidos) configurado como ativo/ativo. Por exemplo, existem usuários ao vivo que tem Chicago como datacenter principal e San Antonio como um datacenter de failover e os usuários que possuem San Antonio como suas datacenter principal e Chicago como datacenters de failover do live. 
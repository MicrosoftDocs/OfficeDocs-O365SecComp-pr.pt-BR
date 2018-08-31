---
title: Destruição de dados do Office 365
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
description: Visão geral de políticas da Microsoft relacionados a reciclagem, descarte ou destruição das unidades de disco de datacenter do Office 365 e servidores.
ms.openlocfilehash: c9950be4919520f2f46badaa4a7d4cfce5c55b45
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523797"
---
# <a name="office-365-data-destruction"></a>Destruição de dados do Office 365
A Microsoft tem políticas padrão de manipulação de dados que atenda recycle e descarte de unidades de disco e de servidores com falha ou retiradas. Antes de usar novamente qualquer drives de disco no Office 365, Microsoft executa um processo de limpeza físico que é consistente com Instituto Nacional de padrões e tecnologia de publicação especial 800-88 ([diretrizes do SP NIST 800-88 para limpeza de mídia](http://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-88r1.pdf) ). Todas as unidades de disco no Office 365 são criptografadas usando a criptografia de nível de volume de disco BitLocker, portanto a eliminação compatíveis com 800-88 NIST SP na prática, não é necessária. No entanto, ele ainda é realizado pela Microsoft.

Falha de discos usados em datacenters fisicamente são destruídos e auditadas por meio do processo ISO do Office 365. O meio apropriado de descarte é determinado pelo tipo de ativo. Para os discos rígidos que não podem ser apagados, a Microsoft usa um processo de destruição que destrua a mídia (por exemplo, disintegrates, pulverizes ou incinerates) e renderiza a recuperação de informações impossíveis. Microsoft também mantém todos os registros de destruição. Microsoft executa um processo semelhante de limpeza em servidores que estão sendo reutilizados dentro do Office 365. Estas diretrizes abrangem a limpeza eletrônica e física.

Unidades de disco que não podem ser reutilizadas são descartadas usando um processo de destruição física que é executado no local dentro do data center que contém os discos sendo destruídos. Designado para o descarte de mídia de armazenamento é colocadas em bandejas seguras localizadas em cada área do datacenter. Cada estação bin segura é monitorada pelo vídeo. Depois que uma bandeja de descarte aproximadamente 50% atinge sua capacidade máxima, a equipe de serviços de Site entra em contato com a equipe de segurança física para coordenar a sua remoção. Equipe de serviços de site, remova a bandeja de disposição em escort pelo responsável por segurança até que ele é colocado em uma área de armazenamento seguro para aguardar destruição de dados. Políticas e procedimentos que regem a manipulação de dados identificando dispositivos durante o descarte rotineiramente são testados inclui procedimentos para garantir a condição de máquinas aprovada para destruição.

No processo de destruição de dados, o disco é apagado primeiro de uma maneira que seja compatível com NIST 800-88 (se possível) e, em seguida, ele é colocado em um shredder industrial e demolished fisicamente. A Microsoft mantém accountability para deixar o datacenter usando SP NIST 800-88 consistente limpeza/limpeza, destruição ativos, criptografia, precisos levantamento, controle e proteção de cadeia de custódia durante o transporte de ativos. Esse processo é monitorado por meio de circuito fechado de televisão e um certificado de destruição é emitida após a conclusão.

A Microsoft usa unidades de eliminação de dados de [Soluções de protocolo extrema](http://www.enterprisedataerasure.com/) (EPS). Software EPS suporta SP NIST 800-88 requisitos para eliminação de limpeza e limpeza/seguro. Antes da limpeza ou destruição, um inventário é criado pelo Gerenciador ativo do Microsoft. Se um fornecedor é usado para destruição, o fornecedor fornece um certificado de destruição para cada ativo destruído, que é validado pelo gerente de ativos.
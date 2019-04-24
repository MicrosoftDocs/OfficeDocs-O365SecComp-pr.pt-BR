---
title: Destruição de dados do Office 365
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
description: Uma visão geral das políticas da Microsoft sobre a reciclagem, a alienação ou a destruição de drives e servidores de disco de datacenter do Office 365.
ms.openlocfilehash: fec6065434fa9fa555a057c68eca60082225652c
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262903"
---
# <a name="office-365-data-destruction"></a>Destruição de dados do Office 365

## <a name="physical-data-destruction"></a>Destruição de dados físicos

A Microsoft tem políticas padrão de manipulação de dados que resolvem a reciclagem e a eliminação de drives de disco e falharam ou aposentaram servidores. Antes de reutilizar quaisquer drives de disco no Office 365, a Microsoft executa um processo de limpeza física consistente com a National Institute of Standards and Technology Special publication [[diretrizes do NIST SP 800-88 para a limpeza de mídia](http://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-88r1.pdf) ). Todas as unidades de disco no Office 365 são criptografadas usando a criptografia de nível de volume do BitLocker, portanto, na prática, a eliminação compatível com o NIST SP 800-88 não é necessária. No enTanto, ele ainda é executado pela Microsoft.

Os discos com falha usados nos datacenters do Office 365 são destruídos fisicamente e auditados por meio do processo ISO. O meio adequado de alienação é determinado pelo tipo de ativo. Para discos rígidos que não podem ser apagados, a Microsoft usa um processo de destruição que destrói a mídia (por exemplo, desintegra, pulverizes ou incinerates) e renderiza a recuperação de informações impossível. A Microsoft também mantém todos os registros da destruição. A Microsoft executa um processo de limpeza semelhante nos servidores que estão sendo reutilizados no Office 365. Essas diretrizes englobam a limpeza eletrônica e física.

As unidades de disco que não podem ser reutilizadas são descartadas de usar um processo de destruição física executado no local no datacenter que contém os discos que estão sendo destruídos. As mídias de armazenamento designadas para descarte são colocadas em compartimentos seguros localizados em cada área do datacenter. Cada estação de compartimento seguro é monitorada pela vigilância por vídeo. Depois que um compartimento de descarte alcança aproximadamente 50% de capacidade, a equipe de serviços de site contata a equipe de segurança física para coordenar sua remoção. Equipe de serviços de site em seguida, remova o compartimento de alienação em Escort por um diretor de segurança até que ele seja colocado em uma área de armazenamento segura para aguardar a destruição dos dados. Políticas e procedimentos que regem o tratamento de dados que ostentam os dispositivos durante o descarte são testados rotineiramente incluindo procedimentos para garantir a condição de maquinação aprovada para destruição.

No processo de destruição de dados, o disco é apagado primeiro de uma maneira que é compatível com o NIST 800-88 (se possível) e, em seguida, é colocado em um picador industrial e fisicamente demolished. A Microsoft mantém a responsabilidade dos ativos que saem do datacenter usando a limpeza/limpeza consistentes do NIST SP 800-88, destruição de ativos, criptografia, inventário preciso, acompanhamento e proteção da cadeia de custódia durante o transporte. Esse processo é monitorado via televisão de circuito fechado, e um certificado de destruição é emitido após a conclusão.

A Microsoft usa unidades de eliminação de dados das [soluções de protocolo extremo](http://www.enterprisedataerasure.com/) (EPS). O software EPS suporta os requisitos do NIST SP 800-88 para limpeza e limpeza/eliminação segura. Antes da limpeza ou destruição, um inventário é criado pelo Microsoft Asset Manager. Se um fornecedor for usado para destruição, o fornecedor fornecerá um certificado de destruição para cada ativo destruído, que é validado pelo Asset Manager.

## <a name="virtual-data-destruction"></a>Destruição de dados virtuais

A Microsoft tem políticas e procedimentos de manipulação de dados que também abordam a destruição virtual efetiva dos dados para proteger contra a possibilidade de dados sendo compartilhados inadequadamente entre os locatários de serviço ou podem ser acessados após a exclusão difícil no serviço. Os dados excluídos do serviço em um locatário não podem ser acessados por outro locatário de serviço, mesmo se algum ou todo o mesmo armazenamento físico subjacente for reatribuído posteriormente. Este é um resultado dos efeitos compostos de várias tecnologias de virtualização e fragmentação usadas para dimensionar ambientes virtuais, os comportamentos de exclusão ativa de aplicativos dentro de cada locatário de serviço (como anulação de [página](https://docs.microsoft.com/office365/securitycompliance/office-365-exchange-online-data-deletion#page-zeroing)) e os requisitos processos de criptografia de conteúdo de aplicativos e mídia.
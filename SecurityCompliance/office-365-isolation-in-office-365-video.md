---
title: Isolamento de Inquilino do Office 365 no vídeo do Office 365
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
description: 'Resumo: Uma explicação dos isolamento de Inquilino no vídeo do Office 365.'
ms.openlocfilehash: 9476047d56161ec2589fdf743d7ee837ea558865
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524319"
---
# <a name="tenant-isolation-in-office-365-video"></a>Isolamento de locatário no Vídeo do Office 365

> [!NOTE]
> Vídeo do Office 365 será substituído pelo Microsoft Stream. Para saber mais sobre o novo serviço de vídeo de empresa que adiciona inteligência a colaboração de vídeo e conheça os planos de transição para clientes atuais do vídeo do Office 365, consulte [migrar para o fluxo de vídeo do Office 365](https://docs.microsoft.com/stream/).

## <a name="introduction"></a>Introdução
Armazenamento do Azure é usado para armazenar dados de vários serviços do Office 365, incluindo vídeo do Office 365 e Sway. Armazenamento do Azure inclui o armazenamento de Blob, que é um armazenamento de objetos de nuvem altamente escalonável, baseado em REST, que é usado para armazenar os dados não estruturados. Armazenamento do Azure usa um modelo de controle de acesso simples; cada assinatura Azure pode criar uma ou mais contas de armazenamento. Cada conta de armazenamento tem uma única chave secreta usada para controlar o acesso a todos os dados no armazenamento de conta. Isso dá suporte o cenário típico onde o armazenamento é associado a aplicativos e esses aplicativos têm controle total sobre os dados associados; Por exemplo, Sway o armazenamento de conteúdo no armazenamento do Azure. Todo o conteúdo de cliente em Sway é armazenado em contas do armazenamento compartilhado do Azure. Conteúdo de cada usuário está em uma árvore de diretório separado de blobs em armazenamento do Azure.

Os sistemas de gerenciamento de acesso para ambientes do cliente (por exemplo, o Portal do Windows Azure SMAPI, etc.) são isolados dentro de um aplicativo Azure operado pela Microsoft. Isso separa, logicamente, a infraestrutura de acesso do cliente dos aplicativos do cliente e camada de armazenamento.

## <a name="tenant-isolation-in-office-365-video"></a>Isolamento de locatário no Vídeo do Office 365
[Vídeo do Office 365](https://support.office.com/article/Meet-Office-365-Video-ca1cc1a9-a615-46e1-b6a3-40dbd99939a6) é um portal empresarial que fornece as organizações com um destino altamente segura, toda a organização para o lançamento, compartilhamento e descobrir conteúdo de vídeo. Vídeo do Office 365, vídeos de cada locatário são mantidos isolado e criptografadas em todos os locais e estão disponíveis somente para usuários autenticados que tem acesso e permissões para vídeos da organização. Vídeo do Office 365 usa uma combinação de tecnologias para realizar isso:
- SharePoint Online é usado para armazenar o arquivo de vídeo e metadados (vídeo título, descrição, etc.). Ele também fornece a camada de segurança e conformidade (incluindo autenticação) e os recursos de pesquisa.
- Azure Media Services fornece transcodificação, streaming adaptável, entrega segura (usando a criptografia AES) e recursos em miniatura.

[Azure Media Services](https://azure.microsoft.com/services/media-services/) é um plataforma-como um serviço que oferece para habilitar fluxos de trabalho de ponta a ponta mídia na nuvem. A plataforma fornece uma API REST para carregamento, codificação, a criptografia (com PlayReady) e fornecimento de mídia por meio do Azure datacenters em todo o mundo.

Todos os carregamentos de vídeo do Office 365 ocorrem via HTTPS. Quando um arquivo de vídeo é carregado, ele está armazenado no SharePoint Online e uma cópia do arquivo é enviada por meio de um canal criptografado aos serviços de mídia do Windows Azure. Azure Media Services transcodificação o vídeo em vários formatos otimizados para a exibição de experiência (por exemplo, móvel, a largura de banda baixa, alta largura de banda, etc.). Esses arquivos, juntamente com o arquivo original adquirido durante o carregamento, são armazenados no armazenamento de Blob do Azure. Os arquivos são criptografados usando AES de 128 pelo algoritmo de criptografia de MPEG comuns de empacotamento (ou uma versão anterior do PlayReady) para reprodução e criptografados usando a criptografia AES 256 armazenamento antes que sejam armazenados no armazenamento de Blob do Azure. (Usando o SDK do Windows Azure Media Services cliente, os clientes podem controlar qual criptografia é usada. Por exemplo, um cliente poderia aplicar a criptografia de armazenamento do Windows Azure Media Services (AES 256) a um ativo de mídia de alto valor antes de carregamento de armazenamento de Blob do Azure.)

Azure Media Services também gera uma miniatura do vídeo, o que ele transmite, juntamente com metadados em miniatura para o SharePoint Online por meio de um canal criptografado.

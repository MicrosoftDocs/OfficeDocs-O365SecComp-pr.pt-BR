---
title: Arquivar dados de terceiros no Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid: MOE150
ms.assetid: 0ce338d5-3666-4a18-86ab-c6910ff408cc
description: Os administradores podem importar dados de terceiros de plataformas de mídia social, plataformas de mensagens instantâneas e plataformas de colaboração de documentos para caixas de correio em sua organização do Office 365. Isso permite que você arquive dados de Facebook, Twitter e outras fontes de dados de terceiros no Office 365. Em seguida, você pode usar e aplicar recursos de conformidade do Office 365 (como retenção legal, eDiscovery, arquivamento in-loco e políticas de retenção) para dados de terceiros.
ms.openlocfilehash: b96c4852c3c9226219120a1be014ea3988cf91a2
ms.sourcegitcommit: e23b84ef4eee9cccec7205826b71ddfe9aaac2f8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33402909"
---
# <a name="archive-third-party-data-in-office-365"></a>Arquivar dados de terceiros no Office 365

O Office 365 permite que os administradores importem e arquivem dados de terceiros de plataformas de mídia social, plataformas de mensagens instantâneas e plataformas de colaboração de documentos, para caixas de correio em sua organização do Office 365. Exemplos de fontes de dados de terceiros que podem ser importadas para o Office 365 incluem o seguinte: 
  
- **Social** -Twitter, Facebook, Yammer e LinkedIn 
    
- **Mensagens instantâneas** -Yahoo Messenger, GoogleTalk e Cisco Jabber 
    
- Documentar a caixa de **colaboração** e o Dropbox 
    
- **Setores verticais** – gerenciamento de relacionamento com o cliente (como o Salesforce informativo) e serviços financeiros (como Bloomberg e Thomson Reuters) 
    
- **SMS/mensagens de texto** -BlackBerry 
    
Após a importação dos dados de terceiros, é possível aplicar recursos de conformidade do Office 365, como retenção de litígio, eDiscovery, arquivamento in-loco, auditoria, supervisão e políticas de retenção do Office 365 — a esses dados. Por exemplo, quando uma caixa de correio é colocada em Retenção de Litígio, os dados de terceiros são preservados. Você pode pesquisar dados de terceiros usando as ferramentas de descoberta eletrônica da Microsoft. Se preferir, você pode aplicar políticas de arquivamento e de retenção aos dados de terceiros, assim como faz com os dados da Microsoft. Em suma, o arquivamento de dados de terceiros no Office 365 pode ajudar sua organização a se manter em conformidade com as políticas governamentais e regulamentares.

Há duas maneiras de importar e arquivar dados de terceiros no Office 365:

- **Use um conector de dados de terceiros no centro de conformidade do & de segurança** -use um conector de dados personalizado que está disponível no centro de conformidade do _AMP_ de segurança no Office 365. Após configurar e configurar o conector, ele se conecta à fonte de dados de terceiros, converte o conteúdo de um item em um formato de mensagem de email e, em seguida, importa o item para uma caixa de correio no Office 365. Para as fontes de dados de terceiros compatíveis com esses conectores e o processo passo a passo para configurar um conector, confira [usar conectores de exemplo para arquivar dados de terceiros no Office 365 (versão prévia)](archive-third-party-data-with-sample-connector.md).

- **Trabalhar com um parceiro da Microsoft** -sua organização trabalha com um parceiro da Microsoft que fornecerá um conector personalizado que será configurado para extrair itens da fonte de dados de terceiros (regularmente) e conectar-se ao Microsoft Cloud por um API de terceiros e importe esses itens para o Office 365. O conector de parceiro também converte o conteúdo de um item da fonte de dados de terceiros em uma mensagem de email e, em seguida, importa-os para uma caixa de correio no Office 365. Para obter uma lista de parceiros com os quais você pode trabalhar e o processo passo a passo desse método, confira [trabalhar com um parceiro para arquivar dados de terceiros no Office 365](work-with-partner-to-archive-third-party-data.md).
---
title: Visão geral do arquivamento ilimitado no Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 37cdbb02-a24a-4093-8bdb-2a7f0b3a19ee
description: Saiba mais sobre a expansão automática arquivamento no Office 365, que fornece armazenamento de arquivamento ilimitado para caixas de correio Exchange Online.
ms.openlocfilehash: 83eb49b3f2a7da418b61e509f44023809ed396c3
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29740813"
---
# <a name="overview-of-unlimited-archiving-in-office-365"></a>Visão geral do arquivamento ilimitado no Office 365

No Office 365, caixas de correio de arquivo morto oferecem aos usuários espaço de armazenamento de caixa de correio adicional. Depois de correio de arquivo morto de um usuário estiver habilitado, até 100 GB de armazenamento adicional está disponível. Quando a cota de armazenamento de 100 GB é atingida, as organizações tinham entrar em contato com a Microsoft para o espaço de armazenamento adicional de solicitação para uma caixa de correio de arquivo morto. Não há mais, que é o caso. O novo recurso de arquivamento ilimitado no Office 365 (chamados de *expansão automática arquivamento*) fornece uma quantidade ilimitada de armazenamento em caixas de correio de arquivo morto. Agora, quando a cota de armazenamento na caixa de correio de arquivo morto é atingida, o Office 365 aumenta automaticamente o tamanho do arquivamento, que significa que os usuários não serão executados sem espaço de armazenamento de caixa de correio e os administradores não devem solicitar o armazenamento adicional para caixas de correio de arquivo morto .
  
Para obter instruções passo a passo para ativem expansão automática arquivamento, consulte [Habilitar o arquivamento ilimitado no Office 365](enable-unlimited-archiving.md).
  
> [!NOTE]
> Expansão automática arquivamento também oferece suporte a caixas de correio compartilhadas. Para habilitar o arquivamento para uma caixa de correio compartilhada, é necessária uma licença do Exchange Online plano 2 ou uma licença do Exchange Online plano 1 com uma licença de arquivamento do Exchange Online. 
  
## <a name="how-auto-expanding-archiving-works"></a>Como expansão automática arquivamento funciona

Como explicada anteriormente, adicional para caixa de correio espaço de armazenamento é criado quando o correio de arquivo morto de um usuário está habilitado. Quando o arquivamento de expansão automática estiver habilitada, o Office 365 verifica periodicamente o tamanho da caixa de correio de arquivo morto. Quando uma caixa de correio de arquivo morto obtém e está perto do limite de armazenamento, o Office 365 cria automaticamente o espaço de armazenamento adicional para o arquivo morto. Se o usuário executa sem esse espaço de armazenamento adicional, o Office 365 adiciona mais espaço de armazenamento para o arquivo do usuário. Esse processo ocorre automaticamente, o que significa que os administradores não devem solicitar o armazenamento de arquivo morto adicionais ou gerenciar o arquivamento de expansão automática. 
  
Eis uma rápida visão geral do processo.
  
![Visão geral do processo de arquivamento expansão automática](media/74355385-d990-44fe-8a87-6c3639d1f63f.png)
  
1. Arquivamento está habilitado para uma caixa de correio do usuário ou uma caixa de correio compartilhada. Uma caixa de correio de arquivamento com 100 GB de espaço de armazenamento é criada e a cota de aviso para a caixa de correio de arquivo morto estiver definida como 90 GB.
    
2. Um administrador permite a expansão automática arquivamento da caixa de correio. Em seguida, quando a caixa de correio de arquivo morto (incluindo a pasta itens recuperáveis) atinge 90 GB, ele é convertido em um arquivo morto expansão automática e Office 365 adiciona espaço de armazenamento para o arquivo morto. Observe que pode demorar até 30 dias para o espaço de armazenamento adicional a ser provisionado.
    
3. O Office 365 adiciona automaticamente mais espaço de armazenamento para o arquivo morto quando necessário.
  
> [!IMPORTANT]
> Se uma caixa de correio é colocada em espera ou atribuída a uma política de retenção do Office 365, a cota de armazenamento para o arquivamento de maibox é aumentada para 110 GB quando o arquivamento de expansão automática está habilitada. Da mesma forma, a cota de aviso de arquivo morto é aumentada para 100 GB.

## <a name="what-gets-moved-to-the-additional-archive-storage-space"></a>O que foi movido para o espaço de armazenamento de arquivo morto adicionais?

Para fazer um uso eficiente do armazenamento de arquivo morto de expansão automática, pastas podem obter movidas. O Office 365 determina quais pastas são movidas quando armazenamento adicional é adicionado para o arquivo morto. Quando uma pasta é movida, uma subpasta é criada automaticamente sob a pasta original na parte de arquivo morto da lista de pastas no Outlook. Essa nova subpasta aponta para os itens que foram movidos. A convenção de nomenclatura que usa Office 365 para nomear essa pasta é ** \<nome da pasta\>_yyyy (criados na mmm dd, yyyy h_mm)**, onde: 
  
- **AAAA** é o ano que as mensagens na pasta foram recebidas. 
    
- **mmm dd, yyyy h_m** é a data e hora em que a subpasta foi criada pelo Office 365, no formato UTC, com base no fuso horário do usuário e as configurações regionais no Outlook. 
    
As capturas de tela a seguir mostram uma lista de pasta antes e depois que as mensagens são movidas em um arquivo morto expandido para automático.
  
 **Antes de é adicionado a armazenamento adicional**
  
![Lista de pastas da caixa de correio de arquivamento antes de arquivo morto de expansão automática está provisionado](media/5d6d6420-e562-4912-aaab-1c111762b3f6.png)
  
 **Depois que o armazenamento adicional é adicionado**
  
![Lista de pastas de correio de arquivo morto após a expansão automática de arquivamento é provisionado](media/c03c5f51-23fa-4fc2-b887-7e7e5cce30da.png)
  
## <a name="outlook-requirements-for-accessing-items-in-an-auto-expanded-archive"></a>Requisitos do Outlook para acessar os itens em um arquivo morto autoexpandida

Para acessar as mensagens que são armazenadas em um arquivo morto expandido para automático, os usuários precisam usar um dos seguintes clientes do Outlook:
  
- Outlook 2016 ou 2019 do Outlook para Windows
    
- Outlook na Web 
    
- Outlook 2016 ou 2019 do Outlook para Mac 
    
> [!NOTE]
> Usuários do Outlook 2013 podem acessar apenas os itens que estavam originalmente armazenados em suas caixas de correio de arquivo morto. Eles não poderão acessar os itens que são movidos para o armazenamento de arquivamento adicionais. 
  
Aqui estão algumas coisas a considerar ao usar o Outlook ou o Outlook na web para acessar mensagens armazenados em um arquivo morto expandido para automático.
  
- Você pode acessar qualquer pasta na sua caixa de correio de arquivo morto, incluindo aquelas que foram movidos para a área de armazenamento de autoexpandida.
    
- Você pode pesquisar para itens que foram movidos para uma área de armazenamento adicional pesquisando na pasta propriamente dita. Isso significa que você deve selecionar a pasta de arquivamento na lista de pastas para selecionar a opção de **Pasta atual** como o escopo da pesquisa. Da mesma forma, se uma pasta em uma área de armazenamento de autoexpandida contiver subpastas, você precisará pesquisar cada subpasta separadamente. 
    
- Contagens de item do Outlook e contagens de leitura/não lida (no Outlook e Outlook na web) em um arquivo morto autoexpandida talvez não sejam precisas.
    
- Você pode excluir itens em uma subpasta que aponta para uma área de armazenamento de autochave expandidas, mas na pasta propriamente dita não pode ser excluída.
    
- Você não pode usar o recurso de recuperar itens excluídos para recuperar um item que foi excluído de uma área de armazenamento de autoexpandida.
  
## <a name="auto-expanding-archiving-and-other-office-365-compliance-features"></a>Expansão automática de arquivamento e outros recursos de conformidade do Office 365

Esta seção explica a funcionalidade entre a expansão automática de arquivamento e outros conformidade do Office 365 e os recursos de governança de dados.
  
- **Descoberta eletrônica** - quando você usar uma ferramenta de descoberta eletrônica do Office 365, como pesquisa de conteúdo ou In-Place eDiscovery, as áreas de armazenamento adicional em um arquivo morto expandido para automático também são pesquisados.
    
- **Retenção** - quando você colocar uma caixa de correio em espera usando ferramentas como litígio no Exchange Online ou eDiscovery caso retenções e políticas de retenção no & de segurança do Office 365 Centro de conformidade, o conteúdo localizadas em um arquivo morto expandido para automático é também colocada em espera.
    
- **Mensagens (MRM) de gerenciamento de registros** - se você usar políticas de exclusão de MRM no Exchange Online para excluir permanentemente os itens expirados de caixa de correio, itens expirados localizados no arquivamento automático-expandida também serão excluídas.
    
- **Importar serviço** - você pode usar o serviço Office 365 importar para importar arquivos PST para o arquivo morto expandido para automático de um usuário. Você pode importar até 100 GB de dados de arquivos PST à caixa de correio de arquivo morto do usuário. 

## <a name="more-information"></a>Mais informações

Para obter mais detalhes técnicos sobre expansão automática, arquivamento, consulte [Office 365: perguntas Frequentes expansão automática de arquivos mortos](https://blogs.technet.microsoft.com/exchange/2018/04/09/office-365-auto-expanding-archives-faq/).
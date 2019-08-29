---
title: Visão geral do arquivamento ilimitado no Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 37cdbb02-a24a-4093-8bdb-2a7f0b3a19ee
description: Saiba mais sobre o arquivamento de expansão automática no Office 365, que fornece armazenamento de arquivo ilimitado para caixas de correio do Exchange Online.
ms.openlocfilehash: bf79ec35fe1ee55702f8a3715d62f102d1d88632
ms.sourcegitcommit: 73f1db241c0686020167d43442e7b07a2199ea3a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/28/2019
ms.locfileid: "36658127"
---
# <a name="overview-of-unlimited-archiving-in-office-365"></a>Visão geral do arquivamento ilimitado no Office 365

No Office 365, as caixas de correio de arquivo morto fornecem aos usuários espaço de armazenamento adicional da caixa de correio. Depois que a caixa de correio de arquivo morto de um usuário estiver habilitada, até 100 GB de armazenamento adicional estará disponível. No passado, quando a cota de armazenamento de 100 GB foi atingida, as organizações tinham que entrar em contato com a Microsoft para solicitar espaço de armazenamento adicional para uma caixa de correio de arquivo morto. Isso não é mais o caso.

O recurso de arquivamento ilimitado no Office 365 (chamado *de arquivamento de expansão automática*) fornece até 1 TB de armazenamento adicional em caixas de correio de arquivo morto. Quando a cota de armazenamento na caixa de correio de arquivo morto é atingida, o Office 365 aumenta automaticamente o tamanho do arquivamento, o que significa que os usuários não ficarão sem espaço de armazenamento de caixa de correio e os administradores não precisarão solicitar armazenamento adicional para caixas de correio de arquivo morto.
  
Para obter instruções detalhadas sobre como ativar o arquivamento de expansão automática, consulte [Enable Unlimited Archiving in Office 365](enable-unlimited-archiving.md).
  
> [!NOTE]
> A expansão automática do arquivamento também oferece suporte às caixas de correio compartilhadas. Para habilitar o arquivo morto para uma caixa de correio compartilhada, uma licença do Exchange Online Plan 2 ou uma licença do plano 1 do Exchange Online com uma licença de arquivamento do Exchange Online é necessária. 
  
## <a name="how-auto-expanding-archiving-works"></a>Como funciona o arquivamento de expansão automática

Conforme explicado anteriormente, o espaço de armazenamento adicional da caixa de correio é criado quando a caixa de correio de arquivo morto do usuário é habilitada. Quando o arquivamento de expansão automática está habilitado, o Office 365 verifica periodicamente o tamanho da caixa de correio de arquivo morto. Quando uma caixa de correio de arquivo morto fica próxima ao limite de armazenamento, o Office 365 cria automaticamente espaço de armazenamento adicional para a caixa de correio de arquivo morto. Esse espaço adicional é chamado de *arquivo auxiliar*. Se o usuário ficar sem espaço de armazenamento em um arquivo auxiliar, o Office 365 adicionará automaticamente um novo arquivo auxiliar. O Office 365 adicionará um máximo de 20 arquivos auxiliares para um total de 1 TB de armazenamento adicional. Esse processo ocorre automaticamente, o que significa que os administradores não precisam gerenciar o arquivamento de expansão automática. 
  
Veja aqui uma rápida visão geral do processo.
  
![Visão geral do processo de arquivamento de expansão automática](media/74355385-d990-44fe-8a87-6c3639d1f63f.png)
  
1. O arquivamento está habilitado para uma caixa de correio de usuário ou uma caixa de correio compartilhada. Uma caixa de correio de arquivo morto com 100 GB de espaço de armazenamento é criada e a cota de aviso da caixa de correio de arquivo morto é definida como 90 GB.
    
2. Um administrador permite o arquivamento de expansão automática da caixa de correio. Quando a caixa de correio de arquivo morto (incluindo a pasta itens recuperáveis) atinge 90 GB, ela é convertida em um arquivo de expansão automática e o Office 365 adiciona espaço de armazenamento ao arquivo morto. Observe que pode levar até 30 dias para que o espaço de armazenamento adicional seja provisionado.

> [!NOTE]
> Se uma caixa de correio for colocada em espera ou atribuída a uma política de retenção do Office 365, a cota de armazenamento do arquivo morto Maibox é aumentada para 110 GB quando o arquivamento de expansão automática está habilitado. Da mesma forma, a cota de aviso de arquivo morto é aumentada para 100 GB.
    
3. O Office 365 adiciona mais espaço de armazenamento automaticamente quando necessário. Conforme mencionado anteriormente, o Office 365 adicionará até 20 arquivos auxiliares, para um máximo de 1 TB de espaço de armazenamento de arquivo adicional.
  
> [!IMPORTANT]
> O arquivo de expansão automática só é suportado para caixas de correio usadas para usuários individuais (ou caixas de correio compartilhadas) com uma taxa de crescimento que não excede 1 GB por dia. A caixa de correio de arquivo morto de um usuário destina-se somente a esse usuário. O uso de registro no diário, regras de transporte ou regras de encaminhamento automático para copiar mensagens para uma caixa de correio de arquivo morto não é permitido. A Microsoft reserva o direito de negar o arquivamento ilimitado em situações onde a caixa de correio de arquivo morto do usuário é usada para armazenar dados de arquivo morto de outros usuários.

## <a name="what-gets-moved-to-the-additional-archive-storage-space"></a>O que é movido para o espaço de armazenamento de arquivo adicional?

Para fazer uso eficiente do armazenamento de arquivo morto de expansão automática, as pastas podem ser movidas. O Office 365 determina quais pastas são movidas quando o armazenamento adicional é adicionado ao arquivo morto. Quando uma pasta é movida, uma subpasta é automaticamente criada na pasta original na parte de arquivo morto da lista de pastas no Outlook. Essa nova subpasta aponta para os itens que foram movidos. A Convenção de nomenclatura que o Office 365 usa para nomear esta pasta é ** \<nome\>da pasta _yyyy (criado no Mmm dd, yyyy h_mm)**, em que: 
  
- **yyyy** é o ano em que as mensagens na pasta foram recebidas. 
    
- **dd mmm, yyyy h_m** é a data e hora em que a subpasta foi criada pelo Office 365, no formato UTC, com base no fuso horário e nas configurações regionais do usuário no Outlook. 
    
As capturas de tela a seguir mostram uma lista de pastas antes e depois que as mensagens são movidas em um arquivo morto expandido automaticamente.
  
 **Antes do armazenamento adicional ser adicionado**
  
![Lista de pastas da caixa de correio de arquivo morto antes de o arquivo morto de expansão automática ser provisionado](media/5d6d6420-e562-4912-aaab-1c111762b3f6.png)
  
 **Após adição de armazenamento adicional**
  
![Lista de pastas da caixa de correio de arquivo morto após o provisionamento automático do arquivo morto](media/c03c5f51-23fa-4fc2-b887-7e7e5cce30da.png)
  
## <a name="outlook-requirements-for-accessing-items-in-an-auto-expanded-archive"></a>Requisitos do Outlook para acessar itens em um arquivo morto expandido automaticamente

Para acessar mensagens armazenadas em um arquivo morto expandido automaticamente, os usuários precisam usar um dos seguintes clientes do Outlook:
  
- Outlook 2016 ou Outlook 2019 para Windows
    
- Outlook na Web 
    
- Outlook 2016 ou Outlook 2019 para Mac 
    
> [!NOTE]
> Os usuários do Outlook 2013 só podem acessar itens que foram originalmente armazenados em suas caixas de correio de arquivo morto. Eles não poderão acessar itens que são movidos para o armazenamento de arquivos adicional. 
  
Aqui estão alguns pontos a considerar ao usar o Outlook ou o Outlook na Web para acessar mensagens armazenadas em um arquivo morto expandido automaticamente.
  
- Você pode acessar qualquer pasta na caixa de correio de arquivo morto, incluindo aquelas que foram movidas para a área de armazenamento expandida automaticamente.
    
- Você pode pesquisar itens que foram movidos para uma área de armazenamento adicional somente pesquisando a própria pasta. Isso significa que você precisa selecionar a pasta de arquivo morto na lista de pastas para selecionar a opção **pasta atual** como o escopo de pesquisa. Da mesma forma, se uma pasta em uma área de armazenamento expandida contiver subpastas, você terá que pesquisar cada subpasta separadamente. 
    
- As contagens de itens no Outlook e nas contagens de leitura/não leitura (no Outlook e no Outlook na Web) em um arquivo morto expandido automaticamente podem não ser precisas.
    
- Você pode excluir itens em uma subpasta que aponta para uma área de armazenamento expandida automaticamente, mas a própria pasta não pode ser excluída.
    
- Você não pode usar o recurso recuperar itens excluídos para recuperar um item que foi excluído de uma área de armazenamento expandida automaticamente.
  
## <a name="auto-expanding-archiving-and-other-office-365-compliance-features"></a>Arquivamento automático e outros recursos de conformidade do Office 365

Esta seção explica a funcionalidade entre o arquivamento de expansão automática e outros recursos de conformidade e controle de dados do Office 365.
  
- **eDiscovery** – quando você usa uma ferramenta de descoberta eletrônica do Office 365, como pesquisa de conteúdo ou descoberta eletrônica in-loco, as áreas de armazenamento adicionais em um arquivo de arquivo expandido automático também são pesquisadas.
    
- **Retenção** : quando você coloca uma caixa de correio em espera usando ferramentas como retenção de litígio no Exchange Online ou bloqueios de ocorrências de descoberta eletrônica e políticas de retenção no centro de segurança e conformidade, o conteúdo localizado em um arquivo expandido automaticamente também é colocado em espera.
    
- **Gerenciamento de registros de mensagens (MRM)** : se você usar as políticas de exclusão do MRM no Exchange Online para excluir permanentemente os itens de caixa de correio expirados, os itens expirados localizados no arquivo expandido automaticamente também serão excluídos.
    
- **Importar serviço** -você pode usar o serviço de importação do Office 365 para importar arquivos pst para o arquivo do usuário expandido automaticamente. Você pode importar até 100 GB de dados de arquivos PST para a caixa de correio de arquivo morto do usuário. 

## <a name="more-information"></a>Mais informações

Para obter mais detalhes técnicos sobre o arquivamento de expansão automática, consulte [Office 365: auto-up de](https://blogs.technet.microsoft.com/exchange/2018/04/09/office-365-auto-expanding-archives-faq/)arquivamento perguntas frequentes.

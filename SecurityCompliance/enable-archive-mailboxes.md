---
title: Habilitar o arquivamento de caixas de correio no Office 365 Security &amp; Centro de conformidade
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.ArchivingHelp
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 268a109e-7843-405b-bb3d-b9393b2342ce
description: Usar a segurança do Office 365 &amp; Centro de conformidade para habilitar caixas de correio de arquivo morto suportar a retenção de mensagens da sua organização, eDiscovery e requisitos de retenção.
ms.openlocfilehash: 5ba578ba611f619194ac4f475121bd485b75f9e0
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524146"
---
# <a name="enable-archive-mailboxes-in-the-office-365-security-amp-compliance-center"></a>Habilitar o arquivamento de caixas de correio no Office 365 Security &amp; Centro de conformidade
  
Arquivamento no Office 365 (também chamado de arquivamento In-loco) fornece aos usuários com espaço de armazenamento de caixa de correio adicional. Depois que você ativa caixas de correio de arquivo morto, os usuários podem acessar e armazenar mensagens em suas caixas de correio de arquivamento usando o Microsoft Outlook e os usuários do Outlook Web App. também pode mover ou copiar mensagens entre suas caixas de correio principal e suas caixas de correio de arquivo morto. Eles também podem recuperar itens excluídos da pasta itens recuperáveis em suas caixas de correio de arquivo morto, usando a ferramenta de recuperar itens excluídos. 
  
> [!TIP]
> O Office 365 fornece uma quantidade ilimitada de armazenamento de arquivamento com o recurso de arquivamento expansão automática. Quando o arquivamento de expansão automática está ativado e, em seguida, a cota de armazenamento inicial na caixa de correio de arquivo morto do usuário for atingida, o Office 365 adiciona automaticamente espaço de armazenamento adicional. Isso significa que os usuários não serão executados sem espaço de armazenamento de caixa de correio e você não precisará gerenciar qualquer coisa inicialmente depois de habilitar a caixa de correio de arquivo morto e ativar o arquivamento para sua organização expansão automática. Para obter mais informações, consulte [Overview of arquivamento ilimitado no Office 365](unlimited-archiving.md). 
  
## <a name="before-you-begin"></a>Antes de começar

Você precisa ter a função de destinatários de email no Exchange Online para habilitar ou desabilitar as caixas de correio de arquivo morto. Por padrão, essa função é atribuída aos grupos de função de gerenciamento de destinatário e organização na página **permissões** no Centro de administração do Exchange. Se você não vir a página de **arquivo morto** na segurança &amp; Centro de conformidade, peça ao administrador para atribuir a você as permissões necessárias. 
  
## <a name="enable-an-archive-mailbox"></a>Habilitar uma caixa de correio de arquivo morto
  
1. Vá para [https://protection.office.com](https://protection.office.com).
    
2. Entrar no Office 365 usando sua conta do trabalho ou da escola.
    
3. No painel à esquerda da segurança &amp; Centro de conformidade, clique em **Governança dados** \> **arquivo morto**.
    
    A página **Arquivo Morto** é exibida. A coluna **Caixa de correio de arquivo morto** indica se uma caixa de correio de arquivo morto está habilitada ou desabilitada para cada usuário. 
    
4. Na lista de caixas de correio, selecione o usuário para o qual você deseja habilitar a caixa de correio de arquivo morto.
    
    ![Clique em Habilitar no painel de detalhes do usuário selecionado para habilitar a caixa de correio de arquivo morto](media/8b53cdec-d5c9-4c28-af11-611f95c37b34.png)
  
5. No painel de detalhes para o usuário selecionado, clique em **Ativar**. 
    
    Será exibido um aviso dizendo que se você habilitar a caixa de correio de arquivo morto, os itens na caixa de correio do usuário mais antigas que a política de arquivamento atribuída à caixa de correio serão movidos para a nova caixa de correio de arquivo morto. A política de arquivamento padrão que faz parte da política de retenção atribuída às caixas de correio Exchange Online move itens na caixa de correio de arquivo morto dois anos após a data em que o item foi entregue à caixa de correio ou criado pelo usuário. Para obter mais informações, consulte a seção de **mais informações** neste artigo. 
    
6. Clique em **Sim** para habilitar a caixa de correio de arquivo morto. 
    
    Ela pode levar alguns momentos para criar a caixa de correio de arquivo morto. Quando ele é criado, **caixa de correio de arquivo morto: habilitado** é exibido no painel de detalhes para o usuário selecionado. Talvez você precise clicar em **Atualizar** ![ícone atualizar](media/O365-MDM-Policy-RefreshIcon.gif) para atualizar as informações no painel de detalhes. 
    
> [!TIP]
> Você pode também habilitar caixas de correio de arquivo morto em massa, selecionando vários usuários com caixas de correio de arquivo morto (use as teclas Shift ou Ctrl). Depois de selecionar várias caixas de correio, clique em **Habilitar** no painel de detalhes.  
  
## <a name="disable-an-archive-mailbox"></a>Desabilitar uma caixa de correio de arquivo morto
  
Você também pode usar a página de **arquivo morto** na segurança &amp; Centro de conformidade para desabilitar a caixa de correio de arquivo morto do usuário. Após desativar uma caixa de correio de arquivamento, você pode reconectá-lo para a caixa de correio principal do usuário dentro de 30 dias do desabilitá-la. Nesse caso, o conteúdo original da caixa de correio de arquivo morto é restaurado. Após 30 dias, o conteúdo da caixa de correio de arquivo morto original é excluído permanentemente e não pode ser recuperado. Portanto, se você reabilitar o arquivamento mais de 30 dias após desativá-la, uma nova caixa de correio de arquivo morto será criada. 
  
Observe que a política de arquivamento padrão atribuídos às caixas de correio dos usuários move itens na caixa de correio de arquivo morto dois anos depois da data o item é entregue. Se você desabilitar o correio de arquivo morto do usuário, nenhuma ação será tomada em itens da caixa de correio e eles permanecerão na caixa de correio principal do usuário.
  
Para desabilitar uma caixa de correio de arquivo morto:
  
1. Vá para [https://protection.office.com](https://protection.office.com).
    
2. Entrar no Office 365 usando sua conta do trabalho ou da escola.
    
3. No painel à esquerda da segurança &amp; Centro de conformidade, clique em **Governança dados** \> **arquivo morto**.
    
    A página **Arquivo Morto** é exibida. A coluna **Caixa de correio de arquivo morto** indica se uma caixa de correio de arquivo morto está habilitada ou desabilitada para cada usuário. 
    
4. Na lista de caixas de correio, selecione o usuário para o qual você deseja habilitar a caixa de correio arquivo morto.
    
5. No painel de detalhes, clique em **Desabilitar**. 
    
    Será exibida uma mensagem de aviso dizendo que você terá 30 dias para reabilitar a caixa de correio de arquivo morto e que após 30 dias, todas as informações no arquivo morto serão excluídas permanentemente. 
    
6. Clique em **Sim** para desabilitar a caixa de correio de arquivo morto. 
    
    Ela pode levar alguns momentos para desabilitar a caixa de correio de arquivo morto. Quando ele estiver desabilitado, **caixa de correio de arquivo morto: desabilitado** é exibido no painel de detalhes para o usuário selecionado. Talvez você precise clicar em **Atualizar** ![ícone atualizar](media/O365-MDM-Policy-RefreshIcon.gif) para atualizar as informações no painel de detalhes. 
    
> [!TIP]
> Você pode também desabilitar caixas de correio de arquivo morto em massa, selecionando vários usuários com caixas de correio de arquivo morto (use as teclas Shift ou Ctrl). Depois de selecionar várias caixas de correio, clique em **Desabilitar** no painel de detalhes.  
  
## <a name="more-information"></a>Mais informações
  
- Caixas de correio de arquivo morto ajudam a você e seus usuários para atender a retenção da sua organização, o eDiscovery e requisitos de retenção. Por exemplo, você pode usar a política de retenção do Exchange da sua organização para mover conteúdo de caixa de correio ao correio de arquivo morto dos usuários. Quando você usar a ferramenta de pesquisa de conteúdo na segurança &amp; Centro de conformidade para a caixa de correio de um usuário para o conteúdo específico, caixa de correio de arquivo morto do usuário de pesquisa também devem ser pesquisado. Além disso, quando você coloca um litígio ou aplica uma política de retenção do Office 365 para caixa de correio do usuário, os itens na caixa de correio de arquivamento também são mantidas.
  
- Quando uma caixa de correio de arquivo morto estiver habilitada, os usuários podem armazenar mensagens em suas caixas de correio de arquivo morto. Os usuários podem acessar o suas caixas de correio de arquivamento usando o Microsoft Outlook e Outlook Web App. usando qualquer um desses aplicativos de cliente, os usuários podem exibir mensagens em suas caixas de correio de arquivo morto e mover ou copiar mensagens entre suas caixas de correio principal e suas caixas de correio de arquivo morto. Os usuários também podem recuperar itens excluídos da pasta itens recuperáveis em suas caixas de correio de arquivo morto, usando a ferramenta de recuperar itens excluídos. 
  
- Após o arquivamento de caixas de correio estão habilitadas, sua organização pode tirar proveito da padrão Exchange política de retenção (também chamado de política de gerenciamento de registros de mensagens ou MRM) que é automaticamente atribuído a cada caixa de correio. Quando uma caixa de correio de arquivo morto estiver habilitada, a política de retenção padrão Exchange automaticamente faz o seguinte: 
  
    - Move os itens que têm dois anos ou mais da caixa de correio principal do usuário para suas caixas de correio de arquivo morto. 
    
    - Move os itens que têm 14 dias ou mais da pasta Itens Recuperáveis na caixa de correio principal do usuário para a pasta Itens Recuperáveis nas caixas de correio de arquivo morto.
    
- Para obter mais informações sobre caixas de correio de arquivo morto e políticas de retenção do Exchange, consulte:
  
  - [Caixas de correio de arquivo morto no Exchange Online](https://go.microsoft.com/fwlink/?LinkId=404421)
    
  - [Marcas e políticas de retenção](https://go.microsoft.com/fwlink/?LinkId=404424)
    
  - [Padrão política de retenção no Exchange Online](https://go.microsoft.com/fwlink/?linkid=839418)
    
  - [Configurar uma política de arquivamento e exclusão de caixas de correio em sua organização do Office 365](set-up-an-archive-and-deletion-policy-for-mailboxes.md)

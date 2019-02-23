---
title: Adicionar os responsáveis a uma descoberta eletrônica avançada (visualização)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: c36e0a2228db042d50361460e2e22f13556e8715
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218211"
---
# <a name="add-custodians-to-an-advanced-ediscovery-preview-case"></a>Adicionar os responsáveis a uma descoberta eletrônica avançada (visualização)

Usando a descoberta eletrônica avançada (versão prévia), você pode aproveitar a ferramenta de gerenciamento de responsáveis interno para coordenar seus fluxos de trabalho em torno do gerenciamento de responsáveis e identificando fontes de dados relevantes e de custodial em um caso. Quando você adiciona um profissional, o sistema pode identificar automaticamente e colocar suspensões em sua caixa de correio principal do Exchange e no site do OneDrive for Business. Ao conduzir sua descoberta, você também pode descobrir e mapear caixas de correio ou sites adicionais que um acessado no passado ou nas equipes de que um responsáveis é membro de hoje.

Use o fluxo de trabalho a seguir para adicionar e gerenciar os responsáveis em casos de descoberta eletrônica avançada (visualização) no centro de conformidade do & de segurança. 

## <a name="step-1-identify-potential-custodians"></a>Etapa 1: identificar possíveis responsáveis

A primeira etapa é identificar os responsáveis apropriados para sua questão. Para adicionar os responsáveis a um caso, você deve ser membro do grupo de função gerenciadores de descoberta eletrônica ou administradores de descoberta eletrônica.   

Para adicionar os responsáveis a uma descoberta eletrônica avançada existente (visualização):

1. Na página **descoberta eletrônica avançada (visualização)** , vá para o seu caso.
 
2. Depois de selecionar uma ocorrência, vá para a guia **responsáveis** e clique em **+ Adicionar**um. 
 
3. Escolha os responsáveis que você deseja adicionar à ocorrência. Você pode começar digitando para pesquisar e selecionar os usuários do Azure Active Directory da sua organização.
 
4. Depois de finalizar a lista de responsáveis, clique em **Avançar** para começar a identificar as fontes de dados potenciais. 
   
## <a name="optional-step-2-select-custodian-data-sources"></a>Opcion Etapa 2: selecionar fontes de dados de responsáveis

Depois de adicionar os responsáveis a um caso, você pode aproveitar o Office 365 para ajudá-lo a identificar e preservar as fontes de dados dos responsáveis principais. A próxima etapa deste fluxo de trabalho é selecionar as fontes de dados de propriedade dos responsáveis especificados na etapa 1. 

Para identificar as fontes de dados de responsáveis: 

1. Para cada pessoa, selecione **Exchange** se quiser que o sistema identifique automaticamente e adicione a caixa de correio principal do Exchange do responsáveis. 
 
2. Para cada pessoa, selecione **onedrive** se quiser que o sistema identifique e adicione automaticamente a URL do onedrive principal do responsáveis. 

    Após fazer suas seleções, o sistema tentará automaticamente identificar as fontes de dados e adicioná-las ao seu caso.
 
4. Clique em **Avançar** para começar a mapear fontes de dados adicionais para seus responsáveis.

## <a name="optional-step-3-map-additional-data-sources"></a>Opcion Etapa 3: mapear fontes de dados adicionais

Dependendo do seu caso, você também pode querer adicionar caixas de correio que um determinado participante possa ter usado no passado, grupos nos quais um responsáveis é um membro no momento ou sites aos quais os responsáveis tinham acesso no passado. Além de fontes de dados principais responsáveis, você pode adicionar outras fontes de dados do Office 365 a um ou aproveitar o Office 365 para ajudá-lo também a identificar fontes de dados potencialmente relevantes. 

Para mapear caixas de correio, sites ou equipes para um determinado local:

1. Selecione **Atualizar** para atribuir locais de conteúdo, como caixas de correio, sites e equipes a um determinado local. 

2. No submenu, especifique o seguinte:
   
  -  **Caixas de correio do Exchange** -clique em **escolher usuários, grupos ou equipes** e, em seguida, clique em **escolher usuários, grupos ou equipes** novamente. Para especificar as caixas de correio a serem atribuídas aos responsáveis selecionados, use a caixa de pesquisa para localizar caixas de correio de usuário e grupos de distribuição. Você também pode atribuir a caixa de correio associada a um grupo do Office 365 ou a uma equipe da Microsoft. Marque a caixa de seleção usuário, grupo, equipe, clique em **escolher**e em **concluído**.

      > [!NOTE]
      > Ao clicar em escolher usuários, grupos ou equipes para especificar caixas de correio, o seletor de caixa de correio exibido estará vazio. Isso é projetado para melhorar o desempenho. Para adicionar pessoas a esta lista, digite um nome (no mínimo 3 caracteres) na caixa de pesquisa.
     
   - **Sites do SharePoint** -clique em **escolher sites** e, em seguida, clique em **escolher sites** novamente para especificar sites adicionais do SharePoint e do onedrive for Business que você gostaria de atribuir aos responsáveis selecionados. Você também pode adicionar a URL do site do SharePoint para um grupo do Office 365 ou uma equipe da Microsoft. Digite a URL de cada site que você deseja atribuir. Clique em **escolher**e em **concluído**.
   - **Microsoft Teams** – clique em **escolher equipes** e, em seguida, clique em **escolher Teams** novamente para exibir uma lista de grupos do Microsoft Team nos quais o responsáveis é membro de hoje. Selecione as equipes que você gostaria de adicionar a seus responsáveis. Depois de selecionado, o sistema identificará automaticamente o & selecione o site do SharePoint associado e a caixa de correio de grupo associados a essa equipe da Microsoft. Clique em **escolher**e em **concluído**.
        
      > [!NOTE]
      > Para adicionar outras Teams da Microsoft, você precisará adicionar separadamente a caixa de correio e o site do SharePoint, conforme mostrado acima.

Após concluir o mapeamento de suas fontes, você poderá exibir as caixas de correio de total, sites e equipes para os responsáveis que você acabou de adicionar. Depois de finalizar as fontes de dados relevantes para um determinado, esse mapeamento será mantido e estendido para os fluxos de trabalho de coleta de descoberta eletrônica, processamento e revisão. 

## <a name="optional-step-4-place-custodians-on-hold"></a>Opcion Etapa 4: colocar os responsáveis em espera

 Depois de finalizar os responsáveis e as fontes de dados que você deseja adicionar ao seu caso, você pode, opcionalmente, colocar alguns ou todos os seus responsáveis em espera. Quando você coloca um bloqueador, o conteúdo mapeado para esse usuário é mantido até que você libere os responsáveis do caso ou até que a retenção seja excluída. Em alguns casos, talvez você queira adicionar os responsáveis por um caso sem colocá-los em espera. 

Para colocar os responsáveis e as fontes de dados selecionados em retenção:

1. Verifique as seleções dos seus responsáveis e marque a caixa de seleção para colocar cada um em espera. Depois que um Objectfor colocado em espera, uma política de retenção de responsáveis contendo todas as fontes de custodial será criada automaticamente. Se a opção não for selecionada, as fontes de dados selecionadas pelo & serão adicionadas ao caso, mas o conteúdo não será preservado.

2. Vá até a guia **isenções** e selecione a **política de retenção de responsáveis**. 

3. Clique em **Editar** para exibir todas as fontes de dados do responsáveis.

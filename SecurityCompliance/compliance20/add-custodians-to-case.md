---
title: Adicionar responsáveis a um caso de eDiscovery avançado (Preview)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: d9a7dc6b1c2eeffdcd49be64d1d09d4a2bda782b
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607349"
---
# <a name="add-custodians-to-an-advanced-ediscovery-preview-case"></a>Adicionar responsáveis a um eDiscovery avançado (Preview) caso

Usando o eDiscovery avançado (Preview), você pode aproveitar a ferramenta de gerenciamento dos responsáveis internas para coordenar os fluxos de trabalho em torno Gerenciando responsáveis e identificar as fontes de dados relevantes, custódia dentro de um caso. Quando você adiciona um funcionário encarregado, o sistema pode identificar automaticamente e retenções locais em sua caixa de correio principal do Exchange e OneDrive para o site de negócios. Conforme você conduzir sua descoberta, você pode descobrir e mapear caixas de correio adicionais ou sites que um funcionário encarregado acessado no passado ou equipes que um funcionário encarregado é um membro de hoje.

Use o seguinte fluxo de trabalho para adicione e gerencie responsáveis em casos de eDiscovery avançado (Preview) dentro do Centro de conformidade do & de segurança. 

## <a name="step-1-identify-potential-custodians"></a>Etapa 1: Identificar potenciais responsáveis

A primeira etapa é identificar os responsáveis apropriados para sua questão. Para adicionar responsáveis a um caso, você deve ser um membro do gerentes de descoberta eletrônica ou um grupo de função de administradores de descoberta eletrônica.   

Para adicionar responsáveis a um caso de eDiscovery avançado (Preview) existente:

1. Na página **eDiscovery avançado (Preview)** , vá para o seu caso.
 
2. Depois de ter selecionado um caso, vá para a guia **responsáveis** e clique em **+ dos responsáveis a adicionar**. 
 
3. Escolha os responsáveis que você deseja adicionar ao caso. Você pode iniciar digitando para pesquisar e selecione os usuários Azure Active Directory da sua organização.
 
4. Depois de finalizar a lista dos responsáveis, clique em **Avançar** para começar a identificar possíveis fontes de dados. 
   
## <a name="optional-step-2-select-custodian-data-sources"></a>(Opcional) Etapa 2: Selecionar fontes de dados dos responsáveis

Após ter adicionado responsáveis a um caso, você pode aproveitar o Office 365 para ajudá-lo a identificar e preservar as fontes de dados dos responsáveis principal. A próxima etapa neste fluxo de trabalho é selecionar as fontes de dados pertencentes as responsáveis especificados na etapa 1. 

Para identificar as fontes de dados dos responsáveis: 

1. Para cada responsável, selecione **Exchange** se você quiser a identificar automaticamente e adicionar principal Exchange da caixa de correio do dos responsáveis do sistema. 
 
2. Para cada responsável, selecione **OneDrive** se você quiser a identificar automaticamente e Adicionar URL principal do dos responsáveis do OneDrive do sistema. 

    Depois de fazer suas seleções, eles sistema tentará automaticamente identificar as fontes de dados e adicioná-los ao seu caso.
 
4. Clique em **Avançar** para iniciar o mapeamento de fontes de dados adicionais para seu dos responsáveis.

## <a name="optional-step-3-map-additional-data-sources"></a>(Opcional) Etapa 3: Mapear fontes de dados adicionais

Dependendo do seu caso, você talvez queira adicionar caixas de correio que dos responsáveis determinado podem ter usado no passado, grupos em que um funcionário encarregado é membro atualmente ou sites que um funcionário encarregado tinha acesso a no passado. Além das fontes de dados dos responsáveis principal, pode adicionar fontes de dados adicionais do Office 365 a dos responsáveis ou aproveitar o Office 365 para ajudá-lo a identificar fontes de dados relevantes potencialmente também. 

Para mapear as equipes, sites ou caixas de correio para dos responsáveis específico:
1. Selecione a **atualização** para atribuir os locais de conteúdo, como caixas de correio, sites e equipes, a dos responsáveis específico. 

2. No submenu, especifique o seguinte:
   
  -  **Caixas de correio do Exchange** - clique em **Escolher usuários, grupos ou equipes** e, em seguida, clique em **Escolher usuários, grupos ou equipes** novamente. Para especificar as caixas de correio para atribuir ao dos responsáveis selecionado, use a caixa Pesquisar para localizar caixas de correio de usuário e grupos de distribuição. Você também pode atribuir a caixa de correio associada para um Team Microsoft ou de um grupo do Office 365. Selecione o usuário, grupo, caixa de seleção de equipe, clique em **Escolher**e, em seguida, clique em **concluído**.

      > [!NOTE]
      > Quando você clica em usuários, grupos ou equipes escolher para especificar as caixas de correio, o seletor de caixa de correio que é exibido está vazio. Isso ocorre por design para aprimorar o desempenho. Para adicionar pessoas a essa lista, digite um nome (um mínimo de 3 caracteres) na caixa Pesquisar.
     
   - **Sites do SharePoint** - clique em **sites de escolha** e clique em **Escolher sites** novamente para especificar o SharePoint e OneDrive adicionais para sites corporativos que você gostaria de atribuir para dos responsáveis selecionado. Você também pode adicionar a URL do site do SharePoint para um Team Microsoft ou de um grupo do Office 365. Digite a URL para cada site que você deseja atribuir. Clique em **Escolher**e, em seguida, clique em **concluído**.
   - **As equipes da Microsoft** – clique em **Escolher equipes** e clique em **Escolher equipes** novamente para exibir uma lista de grupos de Microsoft Team que dos responsáveis é um membro de hoje. Selecione as equipes que você gostaria de adicionar à sua dos responsáveis. Uma vez selecionado, o sistema automaticamente identificará selecionar & que o site do SharePoint associado e a caixa de correio de grupo associado a esse Team Microsoft. Clique em **Escolher**e, em seguida, clique em **concluído**.
        
      > [!NOTE]
      > Para adicionar Teams adicionais da Microsoft, você precisará adicionar separadamente a caixa de correio e o site do SharePoint, como mostrado acima.

Depois de concluir o mapeamento de suas fontes, você poderá exibir as caixas de correio total, sites e equipes para os responsáveis que você acabou de adicionar. Quando tiver finalizado as fontes de dados relevantes para dos responsáveis específico, esse mapeamento será mantido e estendido até o conjunto de descoberta eletrônica, processamento e fluxos de trabalho de revisão. 

## <a name="optional-step-4-place-custodians-on-hold"></a>(Opcional) Etapa 4: Local responsáveis em espera

 Depois de finalizar os responsáveis e as fontes de dados que você gostaria de adicionar ao seu caso, opcionalmente, você pode colocar alguns ou todos os seus responsáveis em espera. Quando você realiza um funcionário encarregado em espera, o conteúdo mapeado para o usuário será retido até que você libere dos responsáveis do gabinete ou até que você exclua isenção. Em alguns casos, convém adicionar responsáveis a um caso sem colocá-los em espera. 

Para colocar as origens selecionadas responsáveis e dados em espera:

1. Verifique suas seleções dos responsáveis e selecione o checkox para colocar cada responsável em espera. Depois que um funcionário encarregado é colocado em espera, uma política de retenção dos responsáveis contendo custódia todas as fontes será criada automaticamente. Se a opção não estiver marcada, as fontes de dados dos responsáveis & selecionada serão adicionadas ao caso, mas o conteúdo não será preservado.

2. Vá para a guia **contém** e selecione a **Política de retenção dos responsáveis**. 

3. Clique em **Editar** para exibir todas as fontes de dados dos responsáveis selecionado.

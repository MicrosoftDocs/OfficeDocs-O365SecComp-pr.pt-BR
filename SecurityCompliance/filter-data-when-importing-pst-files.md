---
title: Filtrar dados ao importar arquivos PST para o Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/24/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 26af16df-34cd-4f4a-b893-bc1d2e74039e
description: 'Use o novo recurso de importação inteligente no serviço de importação do Office 365 para filtrar os itens que realmente obtém importados para as caixas de correio de destino. Importação inteligente permite proativamente decidir quais dados para importação e o que deixar para trás. Importação inteligente também fornece ideias sobre os dados que você está importando para o Office 365. '
ms.openlocfilehash: 723a2e05a1f5d256e99bcf8497643435d0c98a23
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523466"
---
# <a name="filter-data-when-importing-pst-files-to-office-365"></a>Filtrar dados ao importar arquivos PST para o Office 365

Use o novo recurso de importação inteligente no serviço de importação do Office 365 para filtrar os itens em arquivos PST que realmente obtém importou para as caixas de correio de destino. Aqui está como ele funciona:
  
- Depois de criar e enviar um trabalho de importação de PST, arquivos PST são carregados para uma área de armazenamento do Azure na nuvem da Microsoft.
    
- O Office 365 analisa os dados em arquivos PST, de forma segura e, identificando a idade dos itens de caixa de correio e os tipos de mensagem diferente incluídos nos arquivos PST.
    
- Quando a análise for concluída e os dados estão prontos para importação, você tem a opção para importar todos os dados nos arquivos PST como está ou reduzir os dados são importados, definindo filtros que controlam quais dados obtém importados. Por exemplo, você pode optar por:
    
  - Importe apenas os itens de uma determinada idade.
    
  - Importe os tipos de mensagem selecionada.
    
  - Exclua mensagens enviadas ou recebidas por pessoas específicas.
    
- Depois de configurar as definições de filtro, o Office 365 importa somente os dados que satisfazem os critérios de filtragem para as caixas de correio de destino especificados no trabalho de importação.
    
O gráfico a seguir mostra o processo de importação inteligente e destaca as tarefas que você realizar e as tarefas realizadas pelo Office 365.
  
![O processo de importação inteligente no Office 365](media/f2ec309b-11f5-48f2-939c-a6ff72152d14.png)
  
## <a name="before-you-begin"></a>Antes de começar

- As etapas neste tópico pressupõem que você criou um trabalho de importação de PST no serviço de importação do Office 365 usando o carregamento de rede ou o envio de unidade. Para obter instruções detalhadas, consulte um dos seguintes tópicos:
    
  - [Usar o carregamento de rede para importar arquivos PST para o Office 365](use-network-upload-to-import-pst-files.md)
    
  - [Usar o envio de unidade para importar arquivos PST para o Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md)
    
- Depois de criar um trabalho de importação usando o carregamento de rede, o status do trabalho de importação na página Importar página na segurança do Office 365 &amp; Centro de conformidade é definido como **análise em andamento**, que significa que o Office 365 é analisar os dados nos arquivos PST que você carregado. Clique em **Atualizar**![atualizar](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png) para atualizar o status do trabalho de importação. 
    
- Para o envio de trabalhos de importação de unidade, os dados serão analisados pelo Office 365 depois que o pessoal do Microsoft data center recebe seu disco rígido e carregar os arquivos PST para a área de armazenamento do Azure para sua organização.
  
## <a name="filter-data-that-gets-imported-to-mailboxes"></a>Filtre os dados que obtém importou para caixas de correio

Depois que você criou um PST trabalho de importação, siga estas etapas para filtrar os dados antes de importá-lo para o Office 365.
  
1. Vá para [https://protection.office.com/](https://protection.office.com/) e entrar usando as credenciais para uma conta de administrador em sua organização do Office 365. 
    
2. No painel esquerdo da segurança do Office 365 &amp; Centro de conformidade, clique em **Governança dados** \> **importação**.
    
    Os trabalhos de importação para a sua organização estão listados na página **Importar** . Observe que o valor de **Análise concluída** na coluna **Status** indica os trabalhos de importação que tenham sido analisados pelo Office 365 e estiver pronto para ser importado. 
    
    ![Status de análise concluída indica o que Office 365 tenha analisado os dados em arquivos PST](media/de5294f4-f0ba-4b92-a48a-a4b32b6da490.png)
  
3. Clique em **pronto para importar para o Office 365** para o trabalho de importação que você deseja concluir. 
    
    Um efeito de saída de página é exibido com informações sobre os arquivos PST e outras informações sobre o trabalho de importação.
    
4. Clique em **Importar para o Office 365**.
    
    A página de **seus dados de filtro** é exibida. Ele contém as ideias de dados sobre os dados nos arquivos PST para o trabalho de importação, incluindo informações sobre a idade dos dados. 
    
    ![O filtro de sua página de dados mostra as ideias de dados dos arquivos PST para o trabalho de importação](media/3b537ec0-25a4-45a4-96d5-a429e2a33128.png)
  
5. Com base em se ou não deseja reduzir os dados são importados para o Office 365, em **você deseja filtrar seus dados?**, siga um destes procedimentos:
    
    a. clique em **Sim, desejo filtrá-la antes da importação** para reduzir os dados que você importar e clique em **Avançar**.
    
    A página **Importar dados para a página do Office 365** é exibida com as ideias de dados detalhados da análise que executadas do Office 365. 
    
    ![O Office 365 exibe as ideias de dados detalhados da sua análise dos arquivos PST](media/4881205f-0288-4c32-a440-37e2160295f2.png)
  
    O gráfico nesta página mostra a quantidade de dados que serão importados. Informações sobre cada tipo de mensagem encontrada nos arquivos PST são exibidas no gráfico. Você pode passar o cursor sobre cada barra para exibir informações específicas sobre esse tipo de mensagem. Há também uma lista suspensa com valores de idade diferentes com base na análise dos arquivos PST. Quando você seleciona uma idade na lista suspensa, o gráfico é atualizado para mostrar a quantidade de dados será importado para a idade selecionada. 
    
    b. para configurar filtros de adição para reduzir a quantidade de dados que serão importados, clique em **mais opções de filtragem**.
    
    ![Configurar os filtros na página mais opções para reduzir os dados importados](media/3f8d68c3-3fe2-4b4e-9488-b368b98fa9fe.png)
  
    Você pode configurar esses filtros:
    
      - **Idade** - selecionar uma idade, portanto, somente os itens que são mais recente do que a idade especificada será importada. Consulte a seção de [informações adicionais](filter-data-when-importing-pst-files.md#moreinfo) para obter uma descrição sobre como o Office 365 determina partições de memória de idade para o filtro de **duração** . 
    
      - **Tipo** - esta seção mostra todos os tipos de mensagem foram encontrados nos arquivos PST para o trabalho de importação. Você pode desmarcar uma caixa ao lado de um tipo de mensagem que você deseja excluir. Observe que você não pode excluir o tipo de mensagem. Consulte a seção de [informações adicionais](filter-data-when-importing-pst-files.md#moreinfo) para obter uma lista de itens de caixa de correio que estão incluídos na categoria outra. 
    
      - **Os usuários** - é possível excluir mensagens que são enviadas ou recebidas por pessoas específicas. Para excluir as pessoas que aparecem no campo From: campo para: field ou Cc: campo das mensagens, clique em **excluir usuários** ao lado desse tipo de destinatário. Digite o endereço de email (endereço SMTP) da pessoa, clique em **Adicionar**![novo ícone](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) adicioná-los à lista de usuários excluídos para esse tipo de destinatário, e clique em **Salvar** para salvar a lista de usuários excluídos. 
    
        > [!NOTE]
        > O Office 365 não mostra ideias de dados resultantes de configuração do filtro de **pessoas** . No entanto, se você definir esse filtro para excluir mensagens enviadas ou recebidas por pessoas específicas, essas mensagens não serão excluídas durante o processo de importação. 
  
    c. clique em **Aplicar** no dinamicamente **Opções de filtragem mais** check-out de página para salvar suas configurações de filtro. 
    
    Os dados ideias sobre na página **Importar dados para o Office 365** é atualizadas com base em suas configurações de filtro, incluindo a quantidade total de dados que serão importados com base nas configurações de filtro. Observe que um resumo das configurações de filtro também é mostrado. Você pode clicar em **Editar** ao lado de um filtro para alterar a configuração, se necessário. 
    
    ![As ideias de dados são atualizadas com base em suas configurações de filtro](media/897e20fb-3b13-44c3-9d56-9f330750f2a3.png)
  
    d. clique em **Avançar**.
    
    Uma página de status é exibida mostrando as configurações de filtro. Novamente, você pode editar as configurações de filtro.
    
    e. clique em **Importar dados** para iniciar a importação. Observe que a quantidade total de dados que serão importados é exibida. 
    
    Ou
    
    a. clique em **não, eu quiser importar tudo** para importar todos os dados nos arquivos PST para o Office 365 e clique em **Avançar**.
    
    b. na página **Importar dados para o Office 365** , clique em **Importar dados** para iniciar a importação. Observe que a quantidade total de dados que serão importados é exibida. 
    
6. Na página **Importar** , clique em **Atualizar** ![atualizar](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png). O status do trabalho de importação é exibido na coluna **Status** . 
    
7. Clique no trabalho para exibir informações mais detalhadas, como o status de cada arquivo PST e as configurações de filtro que você configurou à importação.

  
## <a name="more-information"></a>Mais informações

- Como o Office 365 determinar os incrementos para o filtro de idade? Quando o Office 365 analisa um arquivo PST, ele analisa o carimbo de hora de enviados ou recebidos de cada item (se um item tiver uma timestamp enviado e recebido, a data mais antiga estiver selecionado). Em seguida, o Office 365 examina o valor de ano para esse carimbo de hora e compara com a data atual para determinar a idade do item. Esses anos, em seguida, são usados como os valores na lista suspensa para o filtro de **duração** . Por exemplo, se um arquivo PST tem mensagens de 2015, 2016 e de 2014, valores do filtro de **idade** seria **ano 1**, **2 anos**e **3 anos**.
    
- A tabela a seguir lista os tipos de mensagem que estão incluídos na **categoria no filtro **tipo** dinamicamente **mais opções** check-out da página** (consulte a Etapa 5b no procedimento anterior). No momento, você não pode excluir itens na categoria "Outras" quando você importa PSTs para o Office 365. 
    
    |**ID de classe de mensagem**|**Itens de caixa de correio que usam essa classe de mensagem**|
    |:-----|:-----|
    |IPM. Atividade  <br/> |Entradas de diário  <br/> |
    |IPM. Documento  <br/> |Documentos e arquivos (não anexados a uma mensagem de email)  <br/> |
    |IPM. Arquivo  <br/> |(o mesmo que IPM. Documento)  <br/> |
    |IPM. Note.IMC.Notification  <br/> |Relatórios enviados por Internet Mail Connect, que é o gateway do Exchange Server para a Internet  <br/> |
    |IPM. Note.Microsoft.Fax  <br/> |Mensagens de fax  <br/> |
    |IPM. Note.Rules.Oof.Template.Microsoft  <br/> |Mensagens de resposta automática de ausência temporária  <br/> |
    |IPM. Note.Rules.ReplyTemplate.Microsoft  <br/> |Respostas enviadas por uma regra de caixa de entrada  <br/> |
    |IPM. OLE. Classe  <br/> |Exceções para uma série recorrente  <br/> |
    |IPM. Recall.Report  <br/> |Relatórios de cancelamento de mensagem  <br/> |
    |IPM. Remoto  <br/> |Mensagens de email remoto  <br/> |
    |IPM. Relatório  <br/> |Relatórios de status do item  <br/> |

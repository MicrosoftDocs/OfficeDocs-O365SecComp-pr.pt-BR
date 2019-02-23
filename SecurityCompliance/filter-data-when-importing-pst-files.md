---
title: Filtrar dados ao importar arquivos PST para o Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/24/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid: MOE150
ms.assetid: 26af16df-34cd-4f4a-b893-bc1d2e74039e
description: 'Use o novo recurso de importação inteligente no serviço de importação do Office 365 para filtrar os itens que realmente são importados para as caixas de correio de destino. A importação inteligente permite que você decida de forma proativa quais dados importar e o que deixar atrás. A importação inteligente também fornece informações sobre os dados que você está importando para o Office 365. '
ms.openlocfilehash: 49399f11a71069059ffae2d03482ac7ffe03daf0
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219811"
---
# <a name="filter-data-when-importing-pst-files-to-office-365"></a>Filtrar dados ao importar arquivos PST para o Office 365

Use o novo recurso de importação inteligente no serviço de importação do Office 365 para filtrar os itens em arquivos PST que realmente são importados para as caixas de correio de destino. Veja como funciona:
  
- Depois de criar e enviar um trabalho de importação de PST, os arquivos PST são carregados para uma área de armazenamento do Azure na nuvem da Microsoft.
    
- O Office 365 analisa os dados nos arquivos PST, de forma segura e segura, identificando a idade dos itens da caixa de correio e os diferentes tipos de mensagens incluídos nos arquivos PST.
    
- Quando a análise é concluída e os dados estão prontos para importação, você tem a opção de importar todos os dados nos arquivos PST como estão ou aparar os dados que são importados por meio da definição de filtros que controlam quais dados são importados. Por exemplo, você pode optar por:
    
  - Importe somente os itens de uma determinada idade.
    
  - Importar tipos de mensagem selecionados.
    
  - Excluir mensagens enviadas ou recebidas por pessoas específicas.
    
- Após definir as configurações de filtro, o Office 365 importa somente os dados que atendem aos critérios de filtragem para as caixas de correio de destino especificadas no trabalho de importação.
    
O gráfico a seguir mostra o processo de importação inteligente e realça as tarefas executadas e as tarefas realizadas pelo Office 365.
  
![O processo de importação inteligente no Office 365](media/f2ec309b-11f5-48f2-939c-a6ff72152d14.png)
  
## <a name="before-you-begin"></a>Antes de começar

- As etapas neste tópico pressupõem que você tenha criado um trabalho de importação de PST no serviço de importação do Office 365 usando o carregamento de rede ou o envio de unidades. Para obter instruções detalhadas, consulte um dos seguintes tópicos:
    
  - [Usar o carregamento de rede para importar arquivos PST para o Office 365](use-network-upload-to-import-pst-files.md)
    
  - [Usar o envio de unidade para importar arquivos PST para o Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md)
    
- Após criar um trabalho de importação usando o carregamento de rede, o status do trabalho de importação na página de importação no Office 365 &amp; Security Compliance Center é definido como **análise em andamento**, o que significa que o Office 365 está analisando os dados nos arquivos pst que você submeti. Clique ****![em atualizar](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png) atualização para atualizar o status do trabalho de importação. 
    
- Para trabalhos de importação de fornecimento de unidades, os dados serão analisados pelo Office 365 após a equipe de data center da Microsoft receber seu disco rígido e carregar os arquivos PST para a área de armazenamento do Azure para sua organização.
  
## <a name="filter-data-that-gets-imported-to-mailboxes"></a>Filtrar dados que são importados para caixas de correio

Depois de criar um trabalho de importação de PST, siga estas etapas para filtrar os dados antes de importá-los para o Office 365.
  
1. AcEsse [https://protection.office.com/](https://protection.office.com/) e entre usando as credenciais de uma conta de administrador na sua organização do Office 365. 
    
2. no painel esquerdo do centro de conformidade de segurança &amp; do Office 365, clique em **importação**de **governança** \> de dados.
    
    Os trabalhos de importação de sua organização estão listados na página **importar** . Observe que o valor de **análise concluída** na coluna **status** indica os trabalhos de importação que foram analisados pelo Office 365 e que estão prontos para importação. 
    
    ![O status de conclusão da análise indica que o Office 365 analisou os dados nos arquivos PST](media/de5294f4-f0ba-4b92-a48a-a4b32b6da490.png)
  
3. Clique em **pronto para importar para o Office 365** para o trabalho de importação que você deseja concluir. 
    
    Uma página de sobrevôo é exibida com informações sobre os arquivos PST e outras informações sobre o trabalho de importação.
    
4. Clique em **importar para o Office 365**.
    
    O **filtro em que sua página de dados** é exibida. Ele contém insights de dados sobre os dados nos arquivos PST para o trabalho de importação, incluindo informações sobre a idade dos dados. 
    
    ![A página Filtrar seus dados mostra as informações de dados dos arquivos PST para o trabalho de importação](media/3b537ec0-25a4-45a4-96d5-a429e2a33128.png)
  
5. Dependendo se você deseja ou não aparar os dados que são importados para o Office 365, em deseja **Filtrar seus dados?**, siga um destes procedimentos:
    
    a. clique em **Sim, quero filtrá-lo antes de importar** para aparar os dados que você importou e, em seguida, clique em **Avançar**.
    
    A página **importar dados para o office 365** é exibida com as informações detalhadas sobre os dados da análise que o Office 365 executou. 
    
    ![O Office 365 exibe informações detalhadas sobre os dados de análise dos arquivos PST](media/4881205f-0288-4c32-a440-37e2160295f2.png)
  
    O gráfico nesta página mostra a quantidade de dados que serão importados. As informações sobre cada tipo de mensagem encontrada nos arquivos PST são exibidas no gráfico. Você pode passar o cursor sobre cada barra para exibir informações específicas sobre esse tipo de mensagem. Há também uma lista suspensa com valores de idade diferentes com base na análise dos arquivos PST. Quando você seleciona uma idade na lista suspensa, o gráfico é atualizado para mostrar a quantidade de dados que será importada para a idade selecionada. 
    
    b. para configurar filtros de adição para reduzir a quantidade de dados importados, clique em **mais opções de filtragem**.
    
    ![Configure os filtros na página mais opções para aparar os dados que são importados](media/3f8d68c3-3fe2-4b4e-9488-b368b98fa9fe.png)
  
    Você pode configurar esses filtros:
    
      - **Idade** -selecione uma idade para que apenas os itens mais recentes do que a idade especificada serão importados. Consulte a seção [mais informações](filter-data-when-importing-pst-files.md#moreinfo) para obter uma descrição sobre como o Office 365 determina os buckets de idade para o filtro de **idade** . 
    
      - **Tipo** -esta seção mostra todos os tipos de mensagem que foram encontrados nos arquivos pst para o trabalho de importação. Você pode desmarcar uma caixa ao lado de um tipo de mensagem que você deseja excluir. Observe que não é possível excluir o outro tipo de mensagem. Consulte a seção [mais informações](filter-data-when-importing-pst-files.md#moreinfo) para obter uma lista de itens de caixa de correio que estão incluídos na outra categoria. 
    
      - **Usuários** – é possível excluir mensagens enviadas ou recebidas por pessoas específicas. Para excluir pessoas que aparecem no campo de:, para: ou no campo CC: de mensagens, clique em **excluir usuários** ao lado desse tipo de destinatário. Digite o endereço de email (endereço SMTP) da pessoa, clique em **Adicionar**![novo](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) ícone para adicioná-los à lista de usuários excluídos para esse tipo de destinatário e clique em **salvar** para salvar a lista de usuários excluídos. 
    
        > [!NOTE]
        > O Office 365 não mostra informações de dados que resultam da configuração do filtro de **pessoas** . No enTanto, se você definir esse filtro para excluir mensagens enviadas ou recebidas por pessoas específicas, essas mensagens serão excluídas durante o processo de importação real. 
  
    c. clique em **aplicar** na página **mais opções de filtragem** sair para salvar as configurações de filtro. 
    
    As informações sobre os dados da página **importar dados para o Office 365** são atualizadas com base nas configurações de filtro, incluindo a quantidade total de dados que serão importados com base nas configurações de filtro. Observe que um resumo das configurações de filtro também é mostrado. Você pode clicar em **Editar** ao lado de um filtro para alterar a configuração, se necessário. 
    
    ![As insights de dados são atualizadas com base nas configurações de filtro](media/897e20fb-3b13-44c3-9d56-9f330750f2a3.png)
  
    d. clique em **Avançar**.
    
    Uma página de status é exibida mostrando suas configurações de filtro. Novamente, você pode editar qualquer uma das configurações de filtro.
    
    e. clique em **importar dados** para iniciar a importação. Observe que a quantidade total de dados que serão importados é exibida. 
    
    Ou
    
    a. clique em **não, desejo importar tudo** para importar todos os dados dos arquivos pst para o Office 365 e, em seguida, clique em **Avançar**.
    
    b. na página **importar dados para o Office 365** , clique em **importar dados** para iniciar a importação. Observe que a quantidade total de dados que serão importados é exibida. 
    
6. Na página **importar** , clique em **Atualizar** ![atualização](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png). O status do trabalho de importação é exibido na coluna **status** . 
    
7. Clique em importar o trabalho para exibir informações mais detalhadas, como o status de cada arquivo PST e as configurações de filtro que você configurou.

  
## <a name="more-information"></a>Mais informações

- Como o Office 365 determina os incrementos para o filtro de idade? Quando o Office 365 analisa um arquivo PST, ele analisa o carimbo de data/hora enviado ou recebido de cada item (se um item tiver um carimbo de data/hora enviado e recebido, a data mais antiga é selecionada). Em seguida, o Office 365 examina o valor de ano desse carimbo de data/hora e o compara à data atual para determinar a idade do item. Essas idades são usadas como os valores na lista suspensa para o filtro de **idade** . Por exemplo, se um arquivo PST tiver mensagens de 2016, 2015 e 2014, os valores no filtro de **idade** serão **1 ano**, **2 anos**e **3 anos**.
    
- A tabela a seguir lista os tipos de mensagens que estão incluídos na **outra** categoria do filtro de **tipo** na página **mais opções** de saída (consulte a etapa 5b no procedimento anterior). No momento, não é possível excluir itens na categoria "outros" quando você importa PSTs para o Office 365. 
    
    |**ID da classe da mensagem**|**Itens de caixa de correio que usam esta classe de mensagem**|
    |:-----|:-----|
    |IPM. Atividade  <br/> |Entradas de diário  <br/> |
    |IPM. Documento  <br/> |Documentos e arquivos (não anexados a uma mensagem de email)  <br/> |
    |IPM. Arquivo  <br/> |(igual a IPM. Documento  <br/> |
    |IPM. Nota. IMC. Notification  <br/> |Relatórios enviados pelo Internet mail Connect, que é o gateway do Exchange Server para a Internet  <br/> |
    |IPM. Observação. Microsoft. fax  <br/> |Mensagens de fax  <br/> |
    |IPM. Note. Rules. OOF. Template. Microsoft  <br/> |Mensagens de resposta automática de ausência temporária  <br/> |
    |IPM. Note. Rules. Replytemplate. Microsoft  <br/> |Respostas enviadas por uma regra de caixa de entrada  <br/> |
    |IPM. OLE. Classificação  <br/> |Exceções de uma série recorrente  <br/> |
    |IPM. ReCall. Report  <br/> |Relatórios de recuperação de mensagens  <br/> |
    |IPM. Remota  <br/> |Mensagens de email remotas  <br/> |
    |IPM. Lo  <br/> |Relatórios de status do item  <br/> |

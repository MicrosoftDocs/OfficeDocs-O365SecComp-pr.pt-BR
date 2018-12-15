---
title: Exportar um relatório da Pesquisa de Conteúdo
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.CustomizeExportReport
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 5c8c1db6-d8ac-4dbb-8a7a-f65d452169b9
description: Em vez de exportar os resultados reais de uma pesquisa de conteúdo no Office 365 Security &amp; Centro de conformidade, você pode exportar apenas um relatório de resultados de pesquisa. O relatório contém um resumo dos resultados da pesquisa e um documento com informações detalhadas sobre cada item que deve ser exportado.
ms.openlocfilehash: e15c6550d58701abe9b268455deca0aef60265fb
ms.sourcegitcommit: 1bc36cd57ab1604f057e2b5d336cf1893ba00125
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/15/2018
ms.locfileid: "27283137"
---
# <a name="export-a-content-search-report"></a>Exportar um relatório da Pesquisa de Conteúdo

Em vez de exportar o conjunto completo de pesquisa resultados de uma pesquisa de conteúdo no Office 365 Security &amp; Centro de conformidade (e a partir de uma pesquisa de conteúdo que está associado a um caso de descoberta eletrônica), você pode exportar apenas os mesmos relatórios que são gerados quando você exporte resultados da pesquisa.
  
Quando você exporta um relatório, ele será baixado para uma pasta que tem o mesmo nome que a pesquisa de conteúdo, mas que foi acrescentado com *_ReportsOnly* . Por exemplo, se a pesquisa de conteúdo é denominada *ContosoCase0815* , o relatório é baixado para uma pasta denominada *ContosoCase0815_ReportsOnly* . Para obter uma lista de documentos que estão incluídos no relatório, consulte [o que está incluído no relatório](#whats-included-in-the-report).

## <a name="before-you-begin"></a>Antes de começar

- Para exportar um relatório de pesquisa de conteúdo, você precisa ter a função de gerenciamento de conformidade de pesquisa no Office 365 Security &amp; Centro de conformidade. Essa função é atribuída aos grupos de função de gerente e o gerenciamento da organização do eDiscovery internas. Ele não é atribuído por padrão ao grupo de funções de gerenciamento da organização. Para obter mais informações, consulte [atribuir permissões de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade](assign-ediscovery-permissions.md).
    
- Quando você exporta um relatório, os dados são armazenados temporariamente em uma área de armazenamento do Windows Azure exclusiva em nuvem da Microsoft antes de ele será baixado para o computador local. Certifique-se de que sua organização pode se conectar ao ponto de extremidade no Windows Azure, que é ** \*. blob.core.windows.net** (o caractere curinga representa um identificador exclusivo para a exportação). Os dados dos resultados de pesquisa são excluídos da área de armazenamento do Azure duas semanas após sua criação. 
    
- O computador que você usa para exportar os resultados da pesquisa devem atender aos seguintes requisitos de sistema:
    
  - Versões de 32 e 64 bits do Windows 7 e versões posteriores



    
  - Microsoft .NET Framework 4.7
    
  - Um navegador com suporte:
    
    - Microsoft Edge
    
      ou
    
    - Microsoft Internet Explorer 10 e versões posteriores
    
    **Observação:** A Microsoft não fabrica extensões de terceiros ou complementos para aplicativos ClickOnce. Exportar resultados de pesquisa usando um navegador sem suporte com extensões de terceiros ou complementos não é suportado. 

- Se o tamanho total estimado dos resultados retornados por uma pesquisa de conteúdo excede 20&nbsp;TB, exportar o relatório falhará. Para exportar um relatório com êxito, tente restringir o escopo e execute novamente a pesquisa para o tamanho estimado dos resultados seja menor que 20&nbsp;TB.

## <a name="generate-and-download-a-content-search-report"></a>Gerar e faça o download de um relatório de pesquisa de conteúdo

As etapas para gerar e faça o download de um relatório de pesquisa de conteúdo serão bastante similares às realmente exportar os resultados de pesquisa.
  
## <a name="step-1-generate-the-report-for-export"></a>Etapa 1: Gerar o relatório para exportação

A primeira etapa é preparar o relatório para baixar para seu computador exportando. Quando você o relatório, o relatório de documentos são carregados para uma área de armazenamento do Azure na Microsoft em nuvem.
  
1. Acesse [https://protection.office.com](https://protection.office.com).
    
2. Entre no Office 365 usando a sua conta corporativa ou de estudante.
    
3. No painel esquerdo do Centro de Conformidade e Segurança, clique em **Pesquisa&amp; investigação** \> **Pesquisa de Conteúdo**.
    
4. Na página de **pesquisa de conteúdo** , selecione uma pesquisa. 
    
5. No painel de detalhes, em **Exportar relatório em um computador**, clique em **Gerar relatório**.
    
    > [!NOTE]
    > Se os resultados para uma pesquisa mais de 7 dias, você precisará atualizar os resultados da pesquisa. Se isso acontecer, cancelar a exportação, clique em **resultados da pesquisa de atualização** no painel de detalhes para a pesquisa selecionado e inicie a exportação de relatório novamente depois que os resultados são atualizados. 
  
6. Na página **Exportar um relatório** , em **incluir estes itens da pesquisa**, escolha uma das seguintes opções:
    
    - Exportar somente itens indexados
    
    - Exportar itens indexados e não indexados
    
    - Exportar somente itens não indexados
    
    Para obter mais informações sobre os itens não indexadas, consulte [parcialmente indexados itens na pesquisa de conteúdo](partially-indexed-items-in-content-search.md).
    
7. Optar por incluir as estatísticas da pesquisa para todas as versões de documentos do SharePoint. Essa opção aparecerá somente se as fontes de conteúdo da pesquisa inclui SharePoint ou OneDrive para sites corporativos.
    
8. Clique em **Gerar relatório**.
    
    O relatório de resultados de pesquisa está preparado para download, o que significa que os documentos de relatório serão carregados para a área de armazenamento do Azure na nuvem da Microsoft. Quando o relatório está pronto para download, no link **baixar relatório** é exibido em **Exportar relatório em um computador** no painel de detalhes. 
    
> [!NOTE]
> Você também pode exportar um relatório para uma pesquisa de conteúdo que está associado a um caso de eDiscovery. Para fazer isso, vá para **pesquisa &amp; investigação** \> **eDiscovery**, selecione um caso e clique em **Editar** ![ícone Editar](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif). Na página de **pesquisa** , selecione uma pesquisa e, em seguida, clique em **Exportar** ![ícone de resultados de pesquisa de exportação](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) \> **Exportar um relatório**. 
  
## <a name="step-2-download-the-report"></a>Etapa 2: Baixar o relatório

A próxima etapa é baixar o relatório a partir da área de armazenamento do Azure ao computador local.
  
1. No painel de detalhes para a pesquisa que você gerou o relatório, em **Exportar relatório em um computador**, clique em **baixar relatório**.
    
    A página de **Download de relatório** é exibida e contém as seguintes informações sobre o relatório até ser baixado para seu computador. 
    
    - O número de itens que serão baixados.
    
    - O tamanho total estimado dos itens que serão baixados.
    
    - Se indexados ou não indexados serão exportados. Itens indexados são itens que têm um formato reconhecido, são criptografados ou não foram indexados por outros motivos.
    
    - Se serão baixadas ou não versões dos documentos do SharePoint.
    
    - O status do processo de exportação de relatório. Você pode iniciar o download do relatório, mesmo se a preparação do relatório não for concluída.
    
2. Em **Exportar chave**, clique em **Copiar para a área de transferência**. Você usará essa chave na etapa 5 para baixar o relatório.
    
    > [!IMPORTANT]
    > Porque qualquer pessoa pode instalar e iniciar a ferramenta de exportação de descoberta eletrônica e, em seguida, use essa chave para baixar o relatório de pesquisa, certifique-se de que tome precauções para proteger essa chave exatamente como você faria proteger senhas ou outras informações relacionadas à segurança. 
  
3. Clique em **baixar relatório**.
    
4. Se você for solicitado a instalar o **eDiscovery MicrosoftOffice 365 Tool exportar**, clique em **instalar**.
    
5. Na **Ferramenta de Exportação de Descoberta Eletrônica**, cole a chave de exportação que você copiou na etapa 2 na caixa apropriada.
    
6. Clique em **Procurar** para especificar o local onde você deseja baixar o relatório. 
    
7. Clique em **Iniciar** para baixar os resultados da pesquisa em seu computador. 
    
    A **ferramenta de exportação de descoberta eletrônica** exibe informações de status sobre o processo de exportação, incluindo uma estimativa do número (e tamanho) dos itens restantes a serem baixados. Quando o processo de exportação estiver concluído, você pode acessar os arquivos no local onde elas são baixadas. 
    
> [!NOTE]
> Você pode baixar o relatório para uma pesquisa de conteúdo que está associado a um caso de eDiscovery. Para fazer isso, vá para **pesquisa &amp; investigação** \> **eDiscovery**, selecione um caso e clique em **Editar** ![ícone Editar](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif). Na página **exportações** , selecione Exportar um relatório e clique em **baixar relatório** no painel de detalhes. 
  
## <a name="whats-included-in-the-report"></a>O que está incluído no relatório

Quando você gera e exporta um relatório sobre os resultados de uma pesquisa de conteúdo, os documentos a seguir são baixados:
  
- **Exportar resumo** - documento do Excel de uma contém um resumo da exportação. Isso inclui informações como o número de fontes de conteúdo que foram pesquisadas, o número de resultados de pesquisa de cada local do conteúdo, o número estimado de itens, o número real de itens que seria ser exportados e o tamanho estimado e real dos itens que poderia ser exportado. 
    
    > [!NOTE]
    > Se você incluir itens indexados ao exportar o relatório, o número de itens indexados é incluído no número total de resultados de pesquisa estimados e no número total de resultados da pesquisa baixado (se fosse exportar os resultados da pesquisa) que estão listados no Exporte o relatório de resumo. Em outras palavras, o número total de itens que seria ser baixado é igual ao número total de resultados estimados e o número total de itens indexados. 
  
- **Manifesto** - um arquivo de manifesto (no formato XML) que contém informações sobre cada item incluído nos resultados da pesquisa. 
    
- **Resultados** - documento An Excel que contém uma linha com informações sobre cada item indexado que seria ser exportado com os resultados da pesquisa. Para email, o log de resultado contém informações sobre cada mensagem, incluindo: 
    
  - O local da mensagem na caixa de correio de origem (inclusive se a mensagem está na caixa de correio principal ou de arquivo morto).
    
  - A data na qual a mensagem foi enviada ou recebida.
    
  - A linha de assunto da mensagem.
    
  - O remetente e os destinatários da mensagem.
    
    Para documentos do SharePoint e do OneDrive para sites corporativos, o log de resultados contém informações sobre cada documento, incluindo:
    
  - A URL para o documento.
    
  - A URL para o conjunto de sites onde o documento está localizado.
    
  - A data em que o documento foi modificado pela última vez.
    
  - O nome do documento (que está localizado na coluna Assunto no log de resultados).
    
    > [!NOTE]
    > O número de linhas no relatório de **resultados** deve ser igual ao número total de resultados de pesquisa que seria ser baixados menos o número total de itens listados no relatório de **Itens indexados** . 
  
- **Itens indexados** - documento do Excel de uma que contém informações sobre todos os itens indexados seriam incluídos nos resultados da pesquisa. Se você não incluir itens indexados quando você gera o relatório de resultados de pesquisa, ainda será baixado este relatório, mas estará vazio.

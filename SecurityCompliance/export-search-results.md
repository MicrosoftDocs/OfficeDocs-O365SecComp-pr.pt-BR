---
title: Exportar resultados da pesquisa de conteúdo no Centro de conformidade a segurança do Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.CustomizeExport
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: ed48d448-3714-4c42-85f5-10f75f6a4278
description: 'Exportar resultados da pesquisa de uma pesquisa de conteúdo no Office 365 Security &amp; Centro de conformidade para um computador local. Resultados de email Emaill são exportados como arquivos PST. Conteúdo do SharePoint e do OneDrive para sites corporativos são exportadas como documentos nativos do Office. '
ms.openlocfilehash: 35fb0aa8a037fc77020269d1b42d738dd801ea0a
ms.sourcegitcommit: da4aa7335b577148ecd61e09bbb11039b817b287
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/15/2018
ms.locfileid: "26539113"
---
# <a name="export-content-search-results-from-the-office-365-security--compliance-center"></a>Exportar resultados da pesquisa de conteúdo no Centro de conformidade a segurança do Office 365

Depois que uma pesquisa de conteúdo for executada com êxito, você pode exportar os resultados da pesquisa para um computador local. Quando você exporta os resultados de email, serem transferidas para seu computador como arquivos PST. Quando você exporta o conteúdo do SharePoint e OneDrive para sites corporativos, cópias de documentos do Office nativos são exportadas. Há documentos adicionais e relatórios que estão incluídos com os resultados da pesquisa exportado.
  
Além disso, todas as mensagens de email criptografadas RMS que estão incluídas nos resultados de uma pesquisa de conteúdo serão descriptografadas quando exportá-los (conforme mensagens individuais). Essa capacidade de descriptografia está habilitada por padrão para membros do grupo de função de Gerenciador de descoberta eletrônica. Isso ocorre porque a função de gerenciamento do RMS descriptografar é atribuída a este grupo de função. Ao exportar os resultados da pesquisa, consulte a seção de [informações adicionais](#more-information) para obter detalhes sobre a descriptografia do RMS. 
  
Exportando os resultados de uma pesquisa de conteúdo envolve Preparando os resultados e, em seguida, baixá-los para um computador local.
  
## <a name="before-you-begin"></a>Antes de começar

- Para exportar os resultados da pesquisa, você precisa ter a função de gerenciamento de exportação de segurança do Office 365 &amp; Centro de conformidade. Essa função é atribuída ao grupo de função de Gerenciador de eDiscovery internas. Ele não é atribuído por padrão ao grupo de funções de gerenciamento da organização. Para obter mais informações, consulte [atribuir permissões de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade](assign-ediscovery-permissions.md).
    
- O computador que você usa para exportar os resultados da pesquisa devem atender aos seguintes requisitos de sistema:
    
  - Versões de 32 e 64 bits do Windows 7 e versões posteriores



    
  - Microsoft .NET Framework 4.7
    
  - Um navegador com suporte:
    
     - Microsoft Edge
    
        OU
    
     - Microsoft Internet Explorer 10 e versões posteriores
    
    **Observação:** A Microsoft não fabrica extensões de terceiros ou complementos para aplicativos ClickOnce. Exportar resultados de pesquisa usando um navegador sem suporte com extensões de terceiros ou complementos não é suportado. 
    
- Quando você baixa os resultados da pesquisa (descritos na etapa 2), você pode aumentar a velocidade de download, definindo uma configuração de registro do Windows no computador que você usa para exportar os resultados da pesquisa. Para obter mais informações, consulte [aumentar a velocidade de download ao exportar os resultados da pesquisa de descoberta eletrônica do Office 365](increase-download-speeds-when-exporting-ediscovery-results.md).
    
- Ao exportar os resultados da pesquisa, os dados são armazenados temporariamente em um local de armazenamento do Microsoft Azure exclusivo em nuvem da Microsoft antes de ele será baixado para o computador local. Certifique-se de que sua organização pode se conectar ao ponto de extremidade no Windows Azure, que é ** \*. blob.core.windows.net** (o caractere curinga representa um identificador exclusivo para a exportação). Os dados dos resultados de pesquisa são excluídos do local de armazenamento do Azure duas semanas após sua criação. 
    
- Se sua organização usa um servidor proxy para se comunicar com a Internet, você precisará definir as configurações do servidor proxy no computador que você usa para exportar os resultados da pesquisa (para que a ferramenta de exportação pode ser autenticada pelo seu servidor proxy). Para fazer isso, abra o arquivo *Machine. config* no local que corresponda a sua versão do Windows. 
    
  - **32-bit** - `%windir%\Microsoft.NET\Framework\[version]\Config\machine.config`
    
  - **64 bits** - `%windir%\Microsoft.NET\Framework64\[version]\Config\machine.config`
    
    Adicione as seguintes linhas ao arquivo *Machine. config* em algum lugar entre o `<configuration>` e `</configuration>` marcas. Certifique-se de substituir `ProxyServer` e `Port` com os valores corretos para sua organização. Por exemplo, `proxy01.contoso.com:80` . 
    
    ```
    <system.net>
       <defaultProxy enabled="true" useDefaultCredentials="true">
         <proxy proxyaddress="http://ProxyServer :Port " 
                usesystemdefault="False" 
                bypassonlocal="True" 
                autoDetect="False" />
       </defaultProxy>
    </system.net>
    ```

- Consulte a seção para obter uma descrição dos limites para exportar os resultados da pesquisa. 
    
- O tamanho máximo de um arquivo PST que pode ser exportado é 10 GB. Se você quiser alterar esse tamanho padrão, você pode editar o registro do Windows no computador que você usa para exportar os resultados da pesquisa. Consulte [alterar o tamanho dos arquivos PST ao exportar os resultados da pesquisa de descoberta eletrônica](change-the-size-of-pst-files-when-exporting-results.md).
    
## <a name="step-1-prepare-search-results-for-export"></a>Etapa 1: Preparar resultados para exportação de pesquisa

A primeira etapa é preparar os resultados da pesquisa para a exportação. Quando você prepara resultados, elas são carregadas para um local de armazenamento do Azure em nuvem da Microsoft. Observe que o conteúdo de caixas de correio e de sites foi carregada em uma taxa máxima de 2 GB por hora.
  
1. Acesse [https://protection.office.com](https://protection.office.com).
    
2. Entre no Office 365 usando a sua conta corporativa ou de estudante.
    
3. No painel esquerdo do Centro de Conformidade e Segurança, clique em **Pesquisa&amp; investigação** \> **Pesquisa de Conteúdo**.
    
4. Na página de **pesquisa de conteúdo** , selecione uma pesquisa. 
    
5. No painel de detalhes, em **Exportar resultados para um computador**, clique em **Iniciar exportação**.
    
    > [!NOTE]
    > Se os resultados de uma pesquisa tiverem mais de 7 dias, você precisará atualizá-los. Se isso acontecer, cancele a exportação, clique em **Atualizar resultados de pesquisa** no painel de detalhes para a pesquisa selecionada e inicie a exportação novamente após os resultados serem atualizados.  
  
6. Na página **exportar os resultados da pesquisa** , em **incluir estes itens da pesquisa**, escolha uma das seguintes opções:
    
    - Exportar somente itens indexados
    
    - Exportar itens indexados e parcialmente indexados
    
    - Exportar itens indexados parcialmente somente
    
    Consulte a seção de [informações adicionais](#more-information) para obter uma descrição sobre itens indexados como parcialmente são exportados. Para obter mais informações sobre itens indexados parcialmente, consulte [parcialmente indexados itens na pesquisa de conteúdo](partially-indexed-items-in-content-search.md).
    
7. Em **Exchange exportar conteúdo como**, escolha uma das seguintes opções:
    
    - **Arquivo PST um para cada caixa de correio** - exporta um arquivo PST para cada caixa de correio de usuário que contém os resultados da pesquisa. Retorno de algum resultado da caixa de correio de arquivo morto do usuário está incluídos no mesmo arquivo PST. Observe que essa opção reproduz a estrutura de pasta de caixa de correio da caixa de correio de origem. 
    
    - **Arquivo PST um contendo todas as mensagens** - exporta um arquivo PST único (chamado *Exchange.pst* ) que contém os resultados de pesquisa de todas as caixas de correio de origem incluídas na pesquisa. Observe que essa opção reproduz a estrutura de pasta de caixa de correio para cada mensagem. 
    
    - **Arquivo PST um contendo todas as mensagens em uma única pasta** - exporta os resultados da pesquisa para um único arquivo de PST onde todas as mensagens estão localizados em uma pasta única e de nível superior. Essa opção permite que os revisores Reveja os itens em ordem cronológica (itens são classificados por data de envio) sem precisar navegar a estrutura original de pasta de caixa de correio para cada item. 
    
    - **Mensagens individuais** - exportações resultados de pesquisa como mensagens de email individuais, usando o formato do. msg. Se você selecionar essa opção, os resultados da pesquisa de email são exportados para uma pasta no sistema de arquivos. O caminho da pasta para mensagens individuais é o mesmo que o usado se você exportou os resultados para arquivos PST. 
    
      > [!IMPORTANT]
      > Para descriptografar mensagens criptografadas por RMS quando eles estiver exportados, você deve exportar os resultados da pesquisa de email como mensagens individuais. Mensagens criptografadas permanecerá inalterado criptografadas, se você exportar os resultados da pesquisa como um arquivo PST. 
  
8. Clique em caixa de seleção **Habilitar Desfazer duplicação** para excluir mensagens duplicadas. Essa opção aparecerá somente se as fontes de conteúdo da pesquisa inclui caixas de correio do Exchange ou pastas públicas. 
    
    Se você selecionar essa opção, apenas uma cópia de uma mensagem será exportada, mesmo se várias cópias da mesma mensagem forem encontradas nas caixas de correio que foram pesquisadas. O relatório de resultados de exportação (Results.csv) conterá uma linha para cada cópia de uma mensagem duplicada para que você possa identificar as caixas de correio (ou pastas públicas) que contêm uma cópia da mensagem duplicada. Para obter mais informações sobre desduplicação e itens duplicados como são identificados, consulte [desduplicação nos resultados da pesquisa de descoberta eletrônica](de-duplication-in-ediscovery-search-results.md).
    
9. Clique na caixa de seleção **incluir versões de documentos do SharePoint** para exportar todas as versões de documentos do SharePoint. Essa opção aparecerá somente se as fontes de conteúdo da pesquisa inclui SharePoint ou OneDrive para sites corporativos. 
    
10. Clique na caixa de seleção **Exportar arquivos em uma pasta (compactado) compactada** para exportar os resultados da pesquisa para pastas compactadas. Essa opção está disponível apenas quando você opta por exportar itens do Exchange como mensagens individuais e quando os resultados da pesquisa incluem os documentos do SharePoint ou OneDrive. Essa opção é usada principalmente para contornar o limite de 260 caracteres em nomes de caminho de arquivo do Windows quando itens são exportados. Consulte "Nomes de arquivo de itens exportados" na seção [mais informações](#more-information) . 
    
11. Clique em **Iniciar exportação**.
    
    Os resultados da pesquisa são preparados para download, o que significa que eles estiver sendo carregados no local de armazenamento do Azure em nuvem da Microsoft. Quando os resultados da pesquisa estiverem prontos para download, o link de **Download exportou resultados** é exibido em **exportar os resultados para um computador** no painel de detalhes. 
  
## <a name="step-2-download-the-search-results"></a>Etapa 2: Baixar os resultados da pesquisa

A próxima etapa é baixar os resultados da pesquisa do local de armazenamento do Windows Azure para seu computador local.
  
Conforme explicado anteriormente, você pode aumentar a velocidade de download, definindo uma configuração de registro do Windows no computador que você usa para exportar os resultados da pesquisa. Para obter mais informações, consulte [aumentar a velocidade de download ao exportar os resultados da pesquisa de descoberta eletrônica do Office 365](increase-download-speeds-when-exporting-ediscovery-results.md).
  
1. No painel de detalhes da pesquisa para a qual você iniciou a exportação, em **Exportar resultados para um computador**, clique em **Baixar resultados exportados**.
    
    A janela **Download exportou resultados** é exibida e contém as seguintes informações sobre os resultados de pesquisa que será baixada para o seu computador. 
    
    - O número de itens que serão baixados.
    
    - O tamanho total estimado dos itens que serão baixados.
    
    - Se serão exportados itens indexados ou não indexados. Os itens não indexados são itens que têm um formato reconhecido, estão criptografados ou não foram indexados por outros motivos. Para saber mais, confira [Unindexed items in Content Search](partially-indexed-items-in-content-search.md).
    
    - Se serão baixadas ou não versões dos documentos do SharePoint.
    
    - O status do processo de preparação de exportação. Você pode começar a baixar os resultados da pesquisa mesmo se a preparação dos dados não tiver sido concluída.
    
2. Em **Exportar chave**, clique em **Copiar para a área de transferência**. Você usará essa chave na etapa 5 para baixar os resultados da pesquisa.
    
    > [!NOTE]
    > Como qualquer pessoa pode instalar e iniciar a Ferramenta de Exportação de Descoberta Eletrônica e, em seguida, usar essa chave para baixar os resultados da pesquisa, tenha o cuidado de proteger essa chave exatamente como faria com senhas ou outras informações relacionadas à segurança.  
  
3. Clique em **Baixar resultados**.
    
4. Se você for solicitado a instalar o **eDiscovery MicrosoftOffice 365 Tool exportar**, clique em **instalar**.
    
5. Na **Ferramenta de Exportação de Descoberta Eletrônica**, cole a chave de exportação que você copiou na etapa 2 na caixa apropriada.
    
6. Clique em **Procurar** para especificar o local onde deseja baixar os arquivos de resultado da pesquisa. 
    
    > [!NOTE]
    > Devido à quantidade de atividade de disco (leituras e gravações) alta, você deve baixar os resultados da pesquisa para uma unidade de disco local; não baixá-los para uma unidade de rede mapeada ou outro local de rede. 
  
1. Clique em **Iniciar** para baixar os resultados da pesquisa em seu computador. 
    
    A **ferramenta de exportação de descoberta eletrônica** exibe informações de status sobre o processo de exportação, incluindo uma estimativa do número (e tamanho) dos itens restantes a serem baixados. Quando o processo de exportação estiver concluído, você pode acessar os arquivos no local onde elas são baixadas. 
    

  
## <a name="more-information"></a>Mais informações

Eis aqui para obter mais informações sobre como exportar os resultados da pesquisa.
  
[Limites de exportação](#export-limits)
  
[Relatórios de exportação](#export-reports)
  
[Exportando itens indexados parcialmente](#exporting-partially-indexed-items)

[Exportando mensagens individuais ou arquivos PST](#exporting-individual-messages-or-pst-files)
  
[Descriptografando mensagens criptografadas por RMS](#decrypting-rms-encrypted-messages)

[Nomes de arquivo de itens exportados](#filenames-of-exported-items)  
  
[Diversos](#miscellaneous)
  
 ### <a name="export-limits"></a>Limites de exportação
  
- Exportar resultados da pesquisa da segurança &amp; Centro de conformidade com os limites a seguir:
    
  - Você pode exportar um máximo de 2 TB de dados de uma única pesquisa de conteúdo. Se os resultados da pesquisa forem maiores que 2 TB, considere o uso de intervalos de data ou outros tipos de filtros para diminuir o tamanho total dos resultados da pesquisa.
    
  - Sua organização pode exportar um máximo de 2 TB de dados durante um único dia.
    
  - Você pode ter no máximo 10 exportações em execução ao mesmo tempo dentro de sua organização.
    
  - Um único usuário pode executar um máximo de três exportações ao mesmo tempo.
    
  - Exportando relatórios de pesquisa de conteúdo não conta em relação a qualquer um dos limites da exportação. 
    
- Conforme anteriormente mencionado, os resultados da pesquisa de caixas de correio e de sites são carregados para o local de armazenamento do Windows Azure (conforme descrito em [etapa 1: preparar resultados para exportação de pesquisa](#step-1-prepare-search-results-for-export)) a uma taxa máxima de 2 GB por hora.
    
- O tamanho máximo de um arquivo PST que pode ser exportado é 10 GB por padrão. Isso significa que se os resultados da pesquisa de caixa de correio do usuário são maiores que 10 GB, os resultados da pesquisa da caixa de correio serão exportados em arquivos PST da separados duas (ou mais). Além disso, se você optar por exportar todos os resultados da pesquisa em um único arquivo PST, o arquivo PST será divido em arquivos de PST adicionais se o tamanho total dos resultados da pesquisa for maior que 10 GB. Se você quiser alterar esse tamanho padrão, você pode editar o registro do Windows no computador que você usa para exportar os resultados da pesquisa. Consulte [alterar o tamanho dos arquivos PST ao exportar os resultados da pesquisa de descoberta eletrônica](change-the-size-of-pst-files-when-exporting-results.md).
    
    Além disso, os resultados da pesquisa a partir de uma caixa de correio específica não ser divididos entre vários arquivos PST, a menos que o conteúdo de uma única caixa de correio é mais de 10 GB. Se você escolher exportar os resultados da pesquisa no PST de um arquivo para que contém todas as mensagens em uma única pasta e os resultados da pesquisa são maiores que 10 GB, os itens ainda são organizados em ordem cronológica, portanto, eles serão ser dividos em arquivos PST adicionais, com base em d enviado ate.
     
 ### <a name="export-reports"></a>Relatórios de exportação
  
- Ao exportar os resultados da pesquisa, os relatórios a seguir estão incluídos além dos resultados da pesquisa.
    
  - **Exportar resumo** Um documento do Excel que contém um resumo da exportação. Isso inclui informações como o número de fontes de conteúdo que foram pesquisadas, os tamanhos estimados e baixados de resultados da pesquisa e o número de itens que foram exportados estimado e baixado. 
    
  - **Manifesto** Um arquivo de manifesto (no formato XML) que contém informações sobre cada item incluído nos resultados da pesquisa. 
    
  - **Resultados** Um documento do Excel que contém informações sobre cada item que é o download como um resultado de pesquisa. Para email, o log de resultado contém informações sobre cada mensagem, incluindo: 
    
      - O local da mensagem na caixa de correio de origem (inclusive se a mensagem está na caixa de correio principal ou de arquivo morto).
        
      - A data na qual a mensagem foi enviada ou recebida.
        
      - A linha de assunto da mensagem.
        
      - O remetente e os destinatários da mensagem.
        
      - Se a mensagem é uma mensagem duplicada se habilitado a opção de eliminação da duplicação ao exportar os resultados da pesquisa. Mensagens duplicadas terá um valor na coluna **duplicados ao Item** que identifica a mensagem como uma duplicata. O valor na coluna **Duplicar a Item** contém a identidade do item da mensagem que foi exportada. Para obter mais informações, consulte [desduplicação nos resultados da pesquisa de descoberta eletrônica](de-duplication-in-ediscovery-search-results.md).
        
      Para documentos do SharePoint e do OneDrive para sites corporativos, o log de resultado contém informações sobre cada documento, incluindo:
        
      - A URL para o documento.
        
      - A URL para o conjunto de sites onde o documento está localizado.
        
      - A data em que o documento foi modificado pela última vez.
        
      - O nome do documento (que está localizado na coluna Assunto no log de resultados).
    
  - **Itens não indexados** Um documento do Excel que contém informações sobre todos os itens indexados parcialmente seriam incluídos nos resultados da pesquisa. Se você não incluir itens indexados parcialmente ao gerar o relatório de resultados de pesquisa, ainda será baixado este relatório, mas estará vazio. 
    
  - **Erros e avisos** Contém os erros e avisos encontrados durante a exportação de arquivos. Consulte a coluna de detalhes do erro para obter informações específicas para cada erro individual ou um aviso. 
    
  - **Itens ignorados** Quando você exporta os resultados da pesquisa do SharePoint e OneDrive para sites corporativos, a exportação normalmente inclui um relatório de itens ignorados (SkippedItems.csv). Os itens citados neste relatório normalmente são itens que não serão baixados, como uma pasta ou um documento definido. Não exportando este tipos de itens é por design. Para outros itens que foram ignoradas, o 'tipo de erro ' e o campo de detalhes do erro no relatório de itens ignorados mostram o motivo pelo qual o item foi ignorado e não tenha sido download com os resultados da pesquisa. 
    
  - **Log de rastreamento** Contém informações de log detalhadas sobre o processo de exportação e pode ajudar a descobrir problemas durante a exportação. 
    
    > [!NOTE]
    > Você somente pode exportar esses documentos sem precisar exportar os resultados de pesquisa. Consulte [Exportar um relatório de pesquisa de conteúdo](export-a-content-search-report.md). 
  
 ### <a name="exporting-partially-indexed-items"></a>Exportando itens indexados parcialmente
  
- Se você está exportando itens de caixa de correio de uma pesquisa de conteúdo que retorne todos os itens de caixa de correio nos resultados da pesquisa (porque nenhuma palavras-chave onde incluídos na consulta de pesquisa), itens indexados parcialmente não serão copiados para o arquivo PST que contém os itens não indexados. Isso acontece porque todos os itens, incluindo quaisquer itens indexados parcialmente, automaticamente são incluídos nos resultados da pesquisa regular. Isso significa que os itens parcialmente indexados serão incluídos em um arquivo PST (ou como mensagens individuais) que contém os itens de outros, indexados.
    
    Além disso, se você exportar itens indexados e parcialmente indexados ou se você exportar somente os itens indexados de uma pesquisa de conteúdo que retorne todos os itens, o mesmo número de itens será baixado. Isso acontece, embora os estimado resultados da pesquisa para a pesquisa de conteúdo (exibida nas estatísticas da pesquisa na segurança &amp; Centro de conformidade) ainda incluirá uma estimativa separada para o número de itens indexados parcialmente. Por exemplo, suponha que a estimativa para uma pesquisa que inclui todos os itens (sem palavras-chave na consulta de pesquisa) mostra que 1.000 itens foram encontrados e que 200 itens indexados parcialmente também foram encontrados. Nesse caso, os itens de 1.000 incluem os itens indexados parcialmente, porque a pesquisa retorna todos os itens. Em outras palavras, há total de 1.000 itens retornado pela pesquisa e não de 1.200 itens (como esperado). Se você exportar os resultados da pesquisa e optar por exportar indexados e parcialmente indexados itens (ou itens indexados apenas) e 1.000 itens serão baixados. Novamente, que é como os itens indexados parcialmente estão inclusos com os resultados (indexados) regulares quando você usa uma consulta de pesquisa em branco para retornar todos os itens. Neste exemplo mesmo, se você optar por exportar somente os itens indexados parcialmente, em seguida, apenas os itens indexados 200 seriam ser baixados.
    
    Observe também que, no exemplo anterior (quando você exportar itens indexados e parcialmente indexados ou exportar itens indexados somente), o relatório de **Resumo de exportar** incluído com os resultados da pesquisa exportado seria listar itens estimado de 1.000 itens e 1.000 baixado itens pelos motivos mesmos conforme descritos anteriormente. 
    
- Se a pesquisa para o qual você está exportando os resultados de uma pesquisa de locais de conteúdo específico ou todos os locais de conteúdo na sua organização, apenas os parcialmente os itens de locais de conteúdo que contêm os itens que correspondem aos critérios de pesquisa serão exportados. Em outras palavras, se nenhum resultado de pesquisa forem encontrado em uma caixa de correio ou de um site, então qualquer indexados itens na caixa de correio que parcialmente ou sites não serão exportados. O motivo para isso é que exportar itens indexados parcialmente de muitos dos locais na organização pode aumentar a probabilidade de erros de exportação e aumentar o tempo que leva para exportar e baixe os resultados da pesquisa.
    
    Para exportar itens indexados parcialmente de todos os locais de conteúdo para uma pesquisa, configurar a pesquisa para retornar todos os itens (removendo qualquer palavra-chave da consulta de pesquisa) e exporte apenas itens indexados parcialmente ao exportar os resultados da pesquisa.
    
    ![Use a opção de exportação thrid para exportar somente os itens não indexados](media/5d7be338-a0e5-425f-8ba5-92769c24bf75.png)
  
- Ao exportar os resultados da pesquisa do SharePoint ou OneDrive para sites corporativos, a capacidade de exportar itens indexados também depende da opção de exportação que você seleciona e se um site que foi pesquisado contém um item indexado que corresponde aos critérios de pesquisa. Por exemplo, se você procurar específicas do SharePoint ou OneDrive sites corporativos e nenhum resultado de pesquisa for encontrado, então nenhum item não indexadas desses sites serão exportados se você escolher a segunda opção de exportação para exportar itens indexados e não indexados. Se um item indexado de um site correspondem aos critérios de pesquisa, em seguida, todos os itens indexados desse site serão exportados ao exportar itens indexados e não indexados. A ilustração a seguir descreve as opções de exportação com base em ou não um site contém um item indexado que corresponde aos critérios de pesquisa.
    
    ![Escolha a opção de exportação com base em ou não um site contém um item indexado que corresponde aos critérios de pesquisa](media/94f78786-c6bb-42fb-96b3-7ea3998bcd39.png)

    
    A - apenas os itens indexados que corresponde aos critérios de pesquisa são exportados. Não há itens indexados parcialmente são exportados.
    
    B - se não há itens indexados de um site correspondem aos critérios de pesquisa, itens indexados parcialmente desse site mesmo não serão exportadas. Se os itens indexados de um site são retornados nos resultados da pesquisa, os itens indexados parcialmente do site são exportados. Em outras palavras, apenas os itens indexados parcialmente de sites que contêm os itens que correspondem aos critérios de pesquisa são exportados.
    
    C - todos os itens indexados parcialmente de todos os sites na pesquisa serão exportados, independentemente se um site contém itens que correspondem aos critérios de pesquisa.
    
    Se você optar por exportar itens indexados parcialmente, itens de caixa de correio parcialmente indexados são exportados em um arquivo PST separado independentemente da opção que você escolher em **Exchange exportar conteúdo como**.

- Se os itens indexados parcialmente forem retornados na pesquisa resulta (porque outras propriedades de itens indexados parcialmente correspondem aos critérios de pesquisa), e em seguida, essas parcialmente indexados são exportados com os resultados de pesquisa comum. Portanto, se você optar por exportar itens indexados e itens indexados parcialmente (selecionando a opção de exportação de **todos os itens, incluindo aquelas que têm o formato não reconhecido, são criptografados, ou não foram indexados por outros motivos** ), os itens indexados parcialmente exportados com os resultados regulares serão listados no relatório Results.csv. Eles não serão listados no relatório items.csv não indexados.
    
 ### <a name="exporting-individual-messages-or-pst-files"></a>Exportando mensagens individuais ou arquivos PST
  
- Se o nome do caminho do arquivo de uma mensagem excede o limite máximo de caracteres para Windows, o nome do caminho de arquivo será truncado. Mas o nome de caminho do arquivo original será listado no manifesto e ResultsLog.
    
- Conforme explicado anteriormente, envie um email pesquisa resultados são exportados para uma pasta no sistema de arquivos. O caminho da pasta para mensagens individuais seria replicar o caminho da pasta na caixa de correio do usuário. Por exemplo, para uma pesquisa chamada "ContosoCase101" mensagens na caixa de entrada do usuário deve estar localizadas no caminho da pasta `~ContosoCase101\\<date of export\Exchange\user@contoso.com (Primary)\Top of Information Store\Inbox`. 
    
- Se você optar por exportar mensagens de email em um arquivo PST que contém todas as mensagens em uma única pasta, uma pasta de **Itens excluídos** e uma pasta de **Pastas de pesquisa** são incluídos no nível superior da pasta PST. Essas pastas estará vazias. 
  
 ### <a name="decrypting-rms-encrypted-messages"></a>Descriptografando mensagens criptografadas por RMS
  
- Conforme explicado anteriormente, para descriptografar mensagens criptografadas por RMS quando você exportá-los, você precisa exportar os resultados da pesquisa como mensagens individuais. Se você exportar os resultados da pesquisa para um arquivo PST, as mensagens criptografadas por RMS permanecerá inalterado criptografadas.
    
- O recurso de descriptografia RMS na pesquisa de conteúdo não descriptografa mensagens criptografadas com o Office 365 Message Encryption (OME) ao exportar os resultados da pesquisa. No entanto, se uma mensagem criptografada com OME é enviada por um usuário em sua organização, a cópia da mensagem na pasta de Sent do usuário não é criptografada e será visualizável após ele será exportado. No entanto, se as mensagens criptografadas com OME são recebidas pelos usuários em sua organização, eles não ser descriptografados após eles estiver exportados. Para obter mais informações sobre OME, consulte [Criptografia de mensagem do Office 365](https://go.microsoft.com/fwlink/p/?linkid=844966).
    
- Mensagens que sejam descriptografadas são identificadas no relatório **ResultsLog** . Este relatório contém uma coluna chamada **Decodificar Status**e um valor de **Decoded** nessa coluna identifica as mensagens a foram descriptografado. 
    
- No momento, esse recurso de descriptografia não inclui conteúdo criptografado do SharePoint e OneDrive para sites corporativos. Somente as mensagens de email criptografadas RMS serão descriptografadas, quando você exportá-los.
    
- Se uma mensagem de email criptografadas RMS tiver um anexo (por exemplo, um documento ou outra mensagem de email) que também é criptografado, será descriptografada, somente a mensagem de email de nível superior.
    
- Não é possível visualizar uma mensagem de email criptografadas RMS. Para exibir uma mensagem criptografada, você precisa exportá-lo.
    
- Se você precisar impedir que alguém descriptografando mensagens criptografadas por RMS, você precisará criar um grupo de função personalizada (copiando o grupo de função de Gerenciador de eDiscovery interna) e, em seguida, remova a função de gerenciamento do RMS descriptografar o grupo de função personalizada. Em seguida, adicione a pessoa que você não deseja descriptografar mensagens como membro do grupo de função personalizada.
  
 ### <a name="filenames-of-exported-items"></a>Nomes de arquivo de itens exportados
  
- Há um limite de 260 caracteres (imposto pelo sistema operacional) para o nome de caminho completo para mensagens de email e documentos do site exportados para o computador local. O nome de caminho completo para itens exportados inclui o local do item original e o local da pasta no computador local onde os resultados da pesquisa são baixados para. Por exemplo, se você especificar para baixar os resultados de pesquisa `C:\Users\Admin\Desktop\SearchResults` na ferramenta de exportação de descoberta eletrônica, em seguida, o nome do caminho completo para um item de email baixado seria `C:\Users\Admin\Desktop\SearchResults\ContentSearch1\03.15.2017-1242PM\Exchange\sarad@contoso.com (Primary)\Top of Information Store\Inbox\Insider trading investigation.msg`.
    
    Se for excedido o limite de 260 caracteres, o nome de caminho completo para um item será truncado.
    
  - Se o nome de caminho completo for mais de 260 caracteres, o nome do arquivo será abreviado para obter sob o limite; Observe que o nome de arquivo truncado (excluindo a extensão de arquivo) não será menos de 8 caracteres.
    
  - Se o nome de caminho completo ainda é muito longo após diminuindo o nome do arquivo, o item é movido de seu local atual para a pasta pai. Se o nome do caminho ainda é muito longo, então o processo é repetido: diminuir o nome de arquivo, e, se for necessário mover-se novamente para a pasta pai. Esse processo é repetido até que o nome do caminho completo está sob o limite de 260 caracteres.
    
  - Se um nome de caminho completo truncado já existir, um número de versão será adicionado ao final do nome de arquivo; Por exemplo, `statusmessage(2).msg`.
    
    Para ajudar a atenuar esse problema, considere baixando os resultados da pesquisa para um local com um nome de caminho curto; Por exemplo, baixando os resultados da pesquisa para uma pasta denominada `C:\Results` seria adicionar menos caracteres para os nomes de caminho dos itens exportados que baixá-los para uma pasta denominada `C:\Users\Admin\Desktop\Results`.
    
- Quando você exporta os documentos do site, também é possível que o nome do arquivo original de um documento será modificado. Isso acontece especificamente para documentos que foram excluídos de um SharePoint ou OneDrive para site de negócios que é foi colocada em espera. Depois que um documento que está localizado em um site que está em retenção for excluído, documento excluído automaticamente é movido para a biblioteca de retenção para preservação para o site (o que foi criado quando o site foi colocado em espera). Quando o documento excluído é movido para a biblioteca de retenção para preservação, uma ID exclusiva e gerada aleatoriamente é anexada ao nome do arquivo original do documento. Por exemplo, se o nome de arquivo para um documento é `FY2017Budget.xlsx` e este documento posteriormente é excluído e movido para a biblioteca de retenção para preservação, o nome de arquivo do documento que é movido para a biblioteca de retenção para preservação é modificada para algo como `FY2017Budget_DEAF727D-0478-4A7F-87DE-5487F033C81A2000-07-05T10-37-55.xlsx`. Se um documento na biblioteca de retenção para preservação corresponde à consulta de uma pesquisa de conteúdo e exportar os resultados da pesquisa, o arquivo exportado terá o nome do arquivo modificado; Neste exemplo, o nome de arquivo do documento exportado seria `FY2017Budget_DEAF727D-0478-4A7F-87DE-5487F033C81A2000-07-05T10-37-55.xlsx`.
    
    Além disso, quando um documento localizado em um site que está em retenção é modificado (e controle de versão da biblioteca de documentos no site tiver sido habilitado), uma cópia do arquivo é criada automaticamente na biblioteca de retenção para preservação. Nesse caso, uma ID exclusiva e gerada aleatoriamente também é anexada ao nome do arquivo do documento que é copiado para a biblioteca de retenção para preservação.
    
    O motivo por que os nomes de arquivos de documentos que forem movidos ou copiados para a biblioteca de retenção para preservação é para impedir que os nomes de arquivos em conflito. Para obter mais informações sobre a colocação de uma isenção em sites e a biblioteca de retenção para preservação, consulte [Overview of in-loco retenção no SharePoint Server 2016](https://support.office.com/article/5e400d68-cd51-444a-8fe6-e4df1d20aa95).
    
 ### <a name="miscellaneous"></a>Diversos
  
- Todos os resultados de pesquisa e os relatórios de exportação são incluídos em uma pasta que tem o mesmo nome que a pesquisa de conteúdo. As mensagens de email que foram exportadas estão localizadas em uma pasta denominada **Exchange**. Documentos estão localizados em uma pasta chamada **SharePoint**. 
    
- Os metadados do sistema de arquivo para documentos no SharePoint e OneDrive para sites corporativos é mantido quando os documentos são exportados para o computador local. Que significa propriedades do documento, como criado e modificado pela última vez datas, não é alterado quando os documentos são exportados.
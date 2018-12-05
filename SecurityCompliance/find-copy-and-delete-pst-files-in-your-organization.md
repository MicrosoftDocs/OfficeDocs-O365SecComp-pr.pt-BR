---
title: Usar a ferramenta de conjunto de PST para localizar, copiar e excluir arquivos PST em sua organização
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid: MOE150
ms.assetid: 7a150c84-049c-4a9c-8c91-22355b35f2a7
description: Use a ferramenta de conjunto de PST do Microsoft para pesquisar a rede da sua organização para fazer um inventário dos arquivos PST que estão espalhados por toda a sua organização. Depois de localizar arquivos PST, você pode usar a ferramenta de conjunto de PST para copiá-los em um local central para importá-los para o Office 365.
ms.openlocfilehash: 34395eee7776d8bff1ddccb7fed5b683e97c02c7
ms.sourcegitcommit: c59a082dca6593d0e35e58124ee6ba240547bfa5
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/05/2018
ms.locfileid: "27154207"
---
# <a name="use-the-pst-collection-tool-to-find-copy-and-delete-pst-files-in-your-organization"></a>Usar a ferramenta de conjunto de PST para localizar, copiar e excluir arquivos PST em sua organização

> [!IMPORTANT]
> A ferramenta de conjunto de PST descrita neste artigo não é suportada em qualquer serviço ou programa de suporte padrão da Microsoft. A ferramenta é fornecida como está sem qualquer garantia. Microsoft também se isenta de todas as garantias implícitas incluindo, sem limitações, qualquer implícitas de comercialização ou adequação a uma finalidade específica. O risco decorrente do uso ou o desempenho do ferramenta e da documentação permanece com você. Em nenhuma hipótese Microsoft, seus autores ou qualquer pessoa else envolvidas na criação, produção ou entrega da ferramenta será responsável por quaisquer danos (incluindo, sem limitação, danos por perda de lucros cessantes, perda de informações comerciais ou outras perdas PECUNIÁRIAS) decorrente do uso ou incapacidade de usar a ferramenta ou documentação, mesmo que a Microsoft tenha sido informada da possibilidade de tais danos.

Você pode usar a ferramenta Microsoft PST Collection para pesquisar a rede da sua organização para arquivos PST. A ferramenta ajuda você a obter um inventário dos arquivos PST que estão espalhados por toda a sua organização. Depois de localizar arquivos PST, você pode usar a ferramenta de conjunto de PST para copiá-los em um local central. Tendo PSTs em um local e permite que você importá-los para o Exchange Online caixas de correio (ou uma única caixa de correio Exchange Online), onde você pode então aplicar o rico conjunto de recursos de conformidade no Office 365. Isso inclui importando PSTs para arquivo morto contém caixas de correio, procurar mensagens específicas nos arquivos PST que você importou usando as ferramentas de pesquisa de descoberta eletrônica, retenção de mensagens usando a descoberta eletrônica e políticas de retenção do Office 365 dos usuários e gerenciando a vida ciclo dessas mensagens usando a mensagens registra os recursos de gerenciamento no Exchange Online. Depois que você estiver confiante de que os arquivos PST que você coletou foram importados com êxito para o Office 365, você pode usar a ferramenta para excluí-los a partir de seu local original em sua rede. 
  
Outra coisa que você pode fazer com que a ferramenta PST Collection é impedir que os usuários criem novos arquivos PST e alterando os arquivos PST existentes que você encontrar em sua rede. Esses recursos "bloquear" permitem que você encontre, coletar e importar um conjunto conhecido de arquivos PST para o Office 365 e impedir a proliferação futura de arquivos PST em sua organização. 
  
## <a name="how-the-pst-collection-tool-works"></a>Como funciona a ferramenta de conjunto de PST

Eis uma rápida visão geral do processo de usando a ferramenta de conjunto de PST para localizar, controlar, coletar e exclua arquivos PST em sua organização.
  
![Visão geral do processo de ferramenta de conjunto de PST](media/67a29f27-f83c-4f0a-9df4-7ed92d3086fe.png)
  
1. **[Etapa 1: localizar arquivos PST em sua rede](#step-1-find-pst-files-on-your-network)** - quando você executar a ferramenta para localizar arquivos PST, especifique um local, como uma unidade organizacional que contêm os objetos do Active Directory para computadores cliente e servidor. Você também pode pesquisar máquinas específicas ou compartilhamentos de arquivos de rede. Quando você executa a ferramenta, um agente de cobrança "leve" é instalado nos computadores de destino. Este agente procura no computador de destino para arquivos PST e envia informações de volta para a ferramenta de conjunto de PST sobre qualquer arquivo PST encontrar. A ferramenta cria arquivos de log que contém informações sobre os arquivos PST encontrados nos locais especificados. Esses arquivos são usados quando você executar a ferramenta nas etapas posteriores. 
    
2. **[(Opcional) etapa 2: controlar o acesso a arquivos PST](#optional-step-2-control-access-to-pst-files)** -a ferramenta cria um objeto de diretiva de grupo (GPO) com as configurações que impedem que os usuários criem ou alterando os arquivos PST. Esse GPO é aplicado a cada usuário em seu domínio. Esta etapa opcional ajuda você a "bloquear" dos arquivos PST que foram encontrados na etapa 1, para que você pode coletar, importar e excluí-los sem a necessidade de novos arquivos PST criados ou os arquivos PST existentes alterados. 
    
3. **[Etapa 3: Copie os arquivos PST para um local de coleção](#step-3-copy-the-pst-files-to-a-collection-location)** -Isso permite coletar os arquivos PST em um único local para que você pode importá-los para caixas de correio do Exchange Online usando o serviço Office 365 importar na etapa 4. Quando você executa a ferramenta no modo de "coletar", cada agente de coleção copia os arquivos PST da máquina destino que o agente está instalado para o local do conjunto. 
    
4. **[Etapa 4: importe os arquivos PST para o Office 365](#step-4-import-the-pst-files-to-office-365)** -depois que você tiver copiado os arquivos PST para um local, você está pronto para importá-los para caixas de correio do Exchange Online. 
    
5. **[Etapa 5: excluir os arquivos PST encontrados em sua rede](#step-5-delete-the-pst-files-found-on-your-network)** - após o PST arquivos que você encontrou e coletados tenha sido importadas para caixas de correio Exchange Online no Office 365, você pode usar a ferramenta de conjunto de PST para excluir os arquivos PST os originais locais onde eles foram encontrados na etapa 1. 

## <a name="before-you-begin"></a>Antes de começar

- Siga estas etapas para baixar a ferramenta de conjunto de PST ao computador local. 
    
    1. [Baixe a ferramenta de conjunto de PST](https://aka.ms/pstcollectiontool).
    
    2. Na janela pop-up, clique em **Salvar** \> **Salvar como** para salvar o arquivo de PSTCollectionTool.zip para uma pasta no computador local. 
    
    3. Extraia o arquivo PSTCollectionTool.zip para uma pasta no computador local; o nome da pasta padrão é PSTCollectionTool.
    
- Para executar a ferramenta de conjunto de PST em qualquer modo (Localizar, bloquear, copiar ou excluir), você precisa ser membro do grupo Administradores de domínio no domínio do Active Directory. 

## <a name="step-1-find-pst-files-on-your-network"></a>Etapa 1: Localizar arquivos PST em sua rede

A primeira etapa é executar a ferramenta de conjunto de PST para localizar arquivos PST em sua organização. Você pode usar a ferramenta para os seguintes tipos de locais de pesquisa. 
  
- Unidades organizacionais (OUs) em um domínio do Active Directory local. A ferramenta pesquisa todos os aparelhos contidos na unidade Organizacional especificada. 
    
- Computadores cliente e servidor. A ferramenta pesquisa as máquinas especificadas. 
    
- Compartilhamentos de arquivos de rede. A ferramenta pesquisa os compartilhamentos de arquivos de rede especificado. 
    
Consulte a descrição para o `Locations` parâmetro na tabela no procedimento a seguir para obter exemplos de sintaxe a ser usado para cada um desses tipos de local. 
  
> [!IMPORTANT]
> Você precisa executar a ferramenta de conjunto de PST no modo de localizar antes que você possa executar outras ações como bloquear, coletando ou excluindo arquivos PST. 
  
1. Abra um Prompt de comando (Executar como administrador) no computador local.
    
2. Vá para a pasta PSTCollectionTool (ou a pasta que você extraiu o arquivo PSTCollectionTool.zip para).
    
3. Mude para o diretório de DataCollectorMaster.
    
4. Execute o seguinte comando para encontrar arquivos PST em um local especificado.
    
    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Find -JobName <Name> -Locations <Locations to search for PSTs> -LogLocation <Location to store log files> -ConfigurationLocation <Location to store configuration files>
    ```

    A tabela a seguir descreve os parâmetros e seus valores necessários quando você executar o comando DataCollectorMaster.exe para encontrar arquivos PST. 
    
    |Parâmetro * * *|****Descrição****|Exemplos * * *|
    |:-----|:-----|:-----|
    | `DataSource` <br/> |Especifica o tipo de dados a ser pesquisado. No momento, você pode usar a ferramenta de conjunto de PST para procurar arquivos PST.  <br/> | `-DataSource Pst` <br/> |
    | `Mode` <br/> |Especifica o tipo de operação que executará a ferramenta. Use o valor `Find` para localizar arquivos PST nos locais especificados. Observe que a ferramenta pode encontrar e obter informações sobre arquivos PST que estão abertos em arquivos PST e Outlook que estão conectados aos perfis do Outlook.<br/> | `-Mode Find` <br/> |
    | `JobName` <br/> |Especifica o nome do trabalho de coleta de PST. Você usará esse mesmo nome de trabalho quando você executar a ferramenta de conjunto de PST para bloquear, coletar e exclua os arquivos PST que são encontrados quando você executar a ferramenta para encontrar arquivos PST. O nome do trabalho também será adicionado aos nomes dos arquivos de log e de configuração.  <br/> | `-JobName PstSearch1` <br/> |
    | `Locations` <br/> | Especifica um ou mais locais para procurar arquivos PST. Se você especificar mais de um local, use ponto e vírgula (;) para separar locais individuais. Certifique-se ao redor os valores individuais desse parâmetro com aspas duplas ("").<br/><br/>   Aqui está o formato de valor de identidade necessária para os tipos de locais que você pode pesquisar.  <br/><br/>        **OUs** - Use o nome diferenciado (DN) para identificar OUs; Por exemplo:`"OU=NorthAmerica,OU=NWRegion,OU=ITServices,DC=contoso,DC=com"` <br/> > [!IMPORTANT]> Não será possível especificar o contêiner de computadores interno (por exemplo, CN = computadores, DC = contoso, DC = com ") porque isso não é uma unidade organizacional.<br/> <br/> **Máquinas** - Use o DN ou o nome de domínio totalmente qualificado (FQDN) para identificar os computadores cliente e servidor na rede; Por exemplo:  <br/>  DN:`"CN=FILESERVER01,CN=Computers,DC=contoso,DC=com"` <br/>  Ou  <br/>  FQDN:`"FILESERVER01.contoso.com"` <br/><br/>  **Compartilhamentos de arquivos de rede** - Use um nome UNC para identificar compartilhamentos de arquivos de rede; Por exemplo,`"\\FILESERVER02\Users"` <br/> | `-Locations "CN=FILESERVER01,CN=Computers,DC=contoso,DC=com";"CN=FILESERVER02,CN=Computers,DC=contoso,DC=com"` <br/> |
    | `LogLocation` <br/> |Especifica a pasta em que os arquivos de log serão copiados para. Se a pasta não existir, ele será criado quando você executar a ferramenta.  <br/> | `-LogLocation "c:\users\admin\desktop\PSTCollection"` <br/> |
    | `ConfigurationLocation` <br/> |Especifica a pasta que será copiado para o arquivo de configuração XML. Esse arquivo contém informações sobre cada arquivo PST que for encontrado quando você executar a ferramenta. Este arquivo será usado quando você executar a ferramenta na etapa 3 para copiar os arquivos PST que são encontrados.  <br/> | `-ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration"` <br/> |
    | `ExcludedLocations` <br/> |Esse parâmetro opcional especifica locais para ignorar durante uma operação de localização. Você pode excluir UOs específicas, máquinas e compartilhamentos de arquivos de rede. Por exemplo, você pode excluir máquinas, como máquina configurado como um SQL server (ou outros tipos de servidores de aplicativos), que os usuários não têm acesso. Se você especificar mais de um local a ser excluído, use ponto e vírgula (;) para separar locais individuais. Certifique-se ao redor os valores individuais desse parâmetro com aspas duplas ("").  <br/> | `-ExcludedLocations "SQLSERVER01.contoso.com"` <br/> |
    | `ForceRestart` <br/> |Esta opção permite que você execute a ferramenta no modo de localização para um trabalho de coleta de PST existente. Quando você usa o `ForceRestart` alternar, os resultados da operação de localização anterior para fazer o trabalho será descartado e a ferramenta irá verificar novamente os locais especificados e criar novos arquivos de log e de configuração.<br/> | `-ForceRestart` <br/> |
   
    Aqui está um exemplo da sintaxe do comando DataCollectorMaster.exe usando valores reais para cada parâmetro:
    
    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Find -JobName PstSearch1 -Locations "CN=FILESERVER01,CN=Computers,DC=contoso,DC=com";"CN=FILESERVER02,CN=Computers,DC=contoso,DC=com" -LogLocation "c:\users\admin\desktop\PSTCollection" -ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration"
    ```

    Depois de executar o comando, serão exibidas mensagens de status detalhado que mostram o progresso de localização de arquivos PST nos locais especificados. Após algum tempo, uma mensagem de status final mostra o número total de arquivos PST que foram encontrados, se o trabalho foi concluída e se ocorreram erros. As mensagens de status mesmo são copiadas para o arquivo. log.
    
### <a name="results-of-running-datacollectormasterexe-in-the-find-mode"></a>Resultados da execução DataCollectorMaster.exe no modo de localizar

Após ter executado a ferramenta de conjunto de PST o modo de localizar, os seguintes arquivos são criados e armazenados nas pastas especificadas pelo `LogLocation` e `ConfigurationLocation` parâmetros. 
  
- **\<Nome_do_trabalho\>_Localizar_\<DateTimeStamp\>. log** -o arquivo de log contém as mensagens de status que foram exibidas. Esse arquivo é criado na pasta especificada pelo `LogLocation` parâmetro. 
    
- **\<Nome_do_trabalho\>_Localizar_\<DateTimeStamp\>. csv** -arquivo CSV The contém uma linha para cada arquivo PST que foi encontrado. As informações para cada PST incluem o computador onde o arquivo PST for encontrada, o local do caminho do arquivo completo do arquivo PST, o proprietário do arquivo PST e o tamanho (em quilobytes, KBs) do arquivo PST. Esse arquivo é criado na pasta especificada pelo `LogLocation` parâmetro. 
    
    > [!TIP]
    > Use a ferramenta AutoSum no Excel para calcular o tamanho total (em KB) de todos os arquivos PST listados no arquivo CSV. Em seguida, você pode usar uma calculadora de conversão para converter o tamanho total em megabytes (MB) ou gigabytes (GB). 
  
- **\<Nome_do_trabalho\>_Localizar_\<DateTimeStamp\>. XML** -o arquivo XML contém informações sobre o parâmetro valores que onde usado quando executou a ferramenta no modo de localizar. Esse arquivo também contém informações sobre cada arquivo PST que foi encontrado. Os dados nesse arquivo são usados quando você executar execute novamente a ferramenta para o mesmo trabalho como block, coletado ou excluir o PST arquivos encontrados. Esse arquivo é criado na pasta especificada pelo `ConfigurationLocation` parâmetro. 
    
    > [!IMPORTANT]
    > Não renomear, alterar ou mover este arquivo. Quando você executa novamente a ferramenta no bloco, cópia, ou excluir modo referente ao trabalho mesmo, ele é usado pela ferramenta de conjunto de PST. 

## <a name="optional-step-2-control-access-to-pst-files"></a>(Opcional) Etapa 2: Controlar o acesso a arquivos PST

Etapa opcional permite que você "bloquear" dos arquivos PST que foram encontrados na etapa 1, para que você possa coletar e importar um conjunto conhecido de arquivos PST para o Office 365. Quando você executar a ferramenta de conjunto de PST no modo de bloqueio, ocorre o seguinte: 
  
- A ferramenta cria um grupo diretiva GPO (objeto) denominado *Controles de uso de PST* . Esse GPO está vinculado ao seu domínio e se aplica a todos os usuários autenticados em sua organização. 
    
- O GPO de controles de uso de PST cria as configurações do registro em máquinas em sua organização. Dependendo do parâmetro que você usa, é possível criar uma configuração de registro para impedir que os usuários criem novos arquivos PST e uma configuração de registro que impede que os usuários alterem os arquivos PST existentes.
    
> [!NOTE]
> Se o controle de acesso a arquivos PST for muito destrutivos para sua organização, você pode considerar pular esta etapa e realizando a etapa 3 para copiar arquivos PST para um local central. E em seguida, repita a etapa 1 para o mesmo trabalho (usando o `ForceRestart` parâmetro) para encontrar arquivos PSTs adicionais que foram criados depois que você copiou os arquivos PSTs até o local do conjunto. Se forem encontrados novos arquivos PST, você pode copiá-los para o local do conjunto. Quando você usa o `ForceRestart` parâmetro quando você executar a ferramenta no modo de localizar novamente, os resultados da operação Localizar anterior para um trabalho serão descartados e a ferramenta irá verificar novamente os locais especificados. 

Para bloquear o acesso a arquivos PST:

1. Abra um Prompt de comando (Executar como administrador) no computador local.
    
2. Vá até o diretório onde você baixou a ferramenta conjunto de PST.
    
3. Execute o seguinte comando para bloquear o acesso aos arquivos PST encontrado na etapa 1.

    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Block -JobName <Name of job from Step 1> -ConfigurationLocation <Location of configuration files from Step 1> -BlockChangesToFiles -BlockNewFiles
    ```

    A tabela a seguir descreve os parâmetros e seus valores necessários quando você executar o comando DataCollectorMaster.exe para bloquear a criação e a alteração de arquivos PST. 
    
    |Parâmetro * * *|****Descrição****|Exemplos * * *|
    |:-----|:-----|:-----|
    | `DataSource` <br/> |Especifica o tipo de dados a ser pesquisado. No momento, você pode usar a ferramenta de conjunto de PST para procurar arquivos PST.  <br/> | `-DataSource Pst` <br/> |
    | `Mode` <br/> |Especifica o tipo de operação que executará a ferramenta. Use o valor `Block` para impedir que os usuários criem novos arquivos PST e fazendo alterações em arquivos PST existentes.<br/> | `-Mode Block` <br/> |
    | `JobName` <br/> |Especifica o nome de um trabalho de coleta de PST existente. Você tem que usar esse mesmo nome de trabalho que você usou quando executou a ferramenta no modo de localizar na etapa 1. Esse nome de trabalho, também é adicionado ao nome do arquivo de log que é criado quando você executar a ferramenta no modo de bloqueio.  <br/> | `-JobName PstSearch1` <br/> |
    | `ConfigurationLocation` <br/> |Especifica que a pasta contém o arquivo de configuração XML que foi criado quando você executou a ferramenta no modo de localizar. Use o mesmo valor que você usou para esse parâmetro na etapa 1.  <br/> | `-ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration"` <br/> |
    | `LogLocation` <br/> |Especifica a pasta que será copiado para o arquivo de log para a operação de bloqueio. Esse é um parâmetro opcional. Se você não incluir a ele, o arquivo de log é copiado para a pasta onde você baixou a ferramenta conjunto de PST. Considere usar o mesmo local de log que você usou quando executou a ferramenta no modo de localizar na etapa 1 para que todos os arquivos de log são salvos na mesma pasta.  <br/> | `-LogLocation "c:\users\admin\desktop\PSTCollection"` <br/> |
    | `BlockChangesToFiles` <br/> |Use esta opção para impedir que usuários alterem um arquivo PST. Quando você usar essa opção, a seguinte entrada do registro é criada: `HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\<version>\Outlook\PST\PstDisableGrow` e o valor dos dados estiver definido como 1. Essa configuração de registro é criada nas máquinas em sua organização pelo GPO que é criado quando você executar a ferramenta de conjunto de PST no modo de bloqueio.<br/> | `-BlockChangesToFiles` <br/> |
    | `BlockNewFiles` <br/> |Use esta opção para impedir que os usuários a criação de novos arquivos PST, abertura e importação dos arquivos PST para o Outlook e a exportação de arquivos PST do Outlook. Quando você usar essa opção, a seguinte entrada do registro é criada: `HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\<version>\Outlook\DisablePst` e o valor dos dados estiver definido como 1. Essa configuração de registro é criada nas máquinas em sua organização pelo GPO que é criado quando você executar a ferramenta de conjunto de PST no modo de bloqueio.<br/> | `-BlockNewFiles` <br/> |
   
    Aqui está um exemplo da sintaxe do comando DataCollectorMaster.exe usando valores reais para cada parâmetro:

    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Block -JobName PstSearch1 -ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration" -LogLocation "c:\users\admin\desktop\PSTCollection" -BlockChangesToFiles -BlockNewFiles
    ```
    
    Você for solicitado para confirmar que você deseja bloquear novos arquivos PST ou alterações em arquivos PST existentes. Depois de confirmar que você deseja continuar e o comando é executado com êxito, será exibida uma mensagem informando que um novo GPO, chamado "Controles de uso de PST," foi criado.
    
## <a name="step-3-copy-the-pst-files-to-a-collection-location"></a>Etapa 3: Copie os arquivos PST para um local de coleção

A próxima etapa é para copiar o PST arquivos que onde encontrado quando executou a ferramenta de conjunto de PST no modo de localizar. Isso permite coletar os arquivos PST em um único local para que você pode importá-los mais tarde para o Office 365. Antes de copiar os arquivos PST para o local do conjunto, considere a possibilidade de determinar a quantidade total de espaço de armazenamento é necessária. Você pode fazer isso usando o arquivo CSV que foi criado na etapa 1 para calcular o tamanho total de todos os arquivos PST.
  
> [!NOTE]
> Após você ter importado os arquivos PST para o Office 365 e excluídos-los do seu local original, convém excluí-los do local da coleção que você copiou nesta etapa. 
  
1. Abra um Prompt de comando (Executar como administrador) no computador local.
    
2. Vá até o diretório onde você baixou a ferramenta conjunto de PST.
    
3. Execute o seguinte comando para copiar os arquivos PST para um local especificado.
    
    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Collect -JobName <Name of job from Step 1> -Locations <same locations from Step 1> -ConfigurationLocation <Location of configuration files from Step 1> -CopyLocation <Location to copy PST files to>
    ```

    A tabela a seguir descreve os parâmetros e seus valores necessários quando você executar o comando DataCollectorMaster.exe para copiar arquivos PST. 
    
    |Parâmetro * * *|****Descrição****|Exemplos * * *|
    |:-----|:-----|:-----|
    | `DataSource` <br/> |Especifica o tipo de dados a ser pesquisado. No momento, você pode usar a ferramenta de conjunto de PST para procurar arquivos PST.  <br/> | `-DataSource Pst` <br/> |
    | `Mode` <br/> |Especifica o tipo de operação que executará a ferramenta. Use o valor `Collect` copiar arquivos PST que foram encontrados quando executou a ferramenta no modo de localizar. Observe que a ferramenta é arquivos PST de capaz de cópia que estão abertas no Outlook e copiam os arquivos PST que estão conectados aos perfis do Outlook.<br/> | `-Mode Collect` <br/> |
    | `JobName` <br/> |Especifica o nome de um trabalho de coleta de PST existente. Você tem que usar esse mesmo nome de trabalho que você usou quando executou a ferramenta no modo de localizar na etapa 1. Esse nome de trabalho, também é adicionado ao nome do arquivo de log que é criado quando você executar a ferramenta no modo de coletar.  <br/> | `-JobName PstSearch1` <br/> |
    | `Locations` <br/> |Usar o mesmo valor que você usou para o `Locations` parâmetro na etapa 1. Você tem incluir esse parâmetro quando você executar a ferramenta no modo de coletar, se você quiser executar novamente a ferramenta para excluir os arquivos PST do local de origem na etapa 5.<br/> | `-Locations "CN=FILESERVER01,CN=Computers,DC=contoso,DC=com"; "CN=FILESERVER02,CN=Computers,DC=contoso,DC=com"` <br/> |
    | `ConfigurationLocation` <br/> |Especifica a pasta que contém o arquivo de configuração XML que foi criado quando você executou a ferramenta no modo de localizar. Use o mesmo valor que você usou para esse parâmetro na etapa 1.  <br/> | `-ConfigurationLocation "c:\users\admin\desktop \PSTCollection\Configuration"` <br/> |
    | `CopyLocation` <br/> |Especifica o local da coleção onde você deseja copiar os arquivos PST. Você pode copiar arquivos para um servidor de arquivos, um compartilhamento de arquivos de rede ou um disco rígido. O local deve existir antes de executar a ferramenta no modo de coletar. A ferramenta não cria o local e retornará um erro dizendo que não existe.  <br/> Além disso, você tem permissões de gravação para o local da coleção especificado por esse parâmetro.  <br/> | `-CopyLocation "\\FILESERVER03\PSTs"` <br/> |
    | `LogLocation` <br/> |Especifica a pasta que será copiado para o arquivo de log para o modo de coletar. Esse é um parâmetro opcional. Se você não incluir a ele, o arquivo de log é copiado para a pasta onde você baixou a ferramenta conjunto de PST. Considere usar o mesmo local de log que você usou quando executou a ferramenta no modo de localizar na etapa 1 para que todos os arquivos de log são salvos na mesma pasta.  <br/> | `-LogLocation "c:\users\admin\desktop\PSTCollection"` <br/> |
    | `ForceRestart` <br/> |Esta opção permite que você execute novamente a ferramenta no modo de conjunto de um trabalho de coleta de PST existente. Se você executou anteriormente a ferramenta no modo de coletar, mas que executou a ferramenta novamente no modo de localizar com o `ForceRestart` alternar para verificar novamente os locais dos arquivos PST, você pode usar essa opção para executar novamente a ferramenta no modo de coleção e novamente copiar os arquivos PST havia encontrado quando sua verificadas novamente os locais. Ao usar o `ForceRestart` opção no modo de coleção, a ferramenta ignora quaisquer operações de coleção anteriores e tenta copiar os arquivos PST do zero.<br/> | `-ForceRestart` <br/> |
   
    Aqui está um exemplo da sintaxe para a ferramenta de DataCollectorMaster.exe usando valores reais para cada parâmetro:
    
    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Collect -JobName PstSearch1 -Locations "CN=FILESERVER01,CN=Computers,DC=contoso,DC=com";"CN=FILESERVER02,CN=Computers,DC=contoso,DC=com" -ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration" -CopyLocation "\\FILESERVER03\PSTs" -LogLocation "c:\users\admin\desktop\PSTCollection"
    ```

    Após executar o comando, serão exibidas mensagens de status detalhado que mostram o progresso de coleta dos arquivos PST que foram encontrados na etapa 1. Após algum tempo, uma mensagem de status final mostra se ocorreram erros e o local em que o log é copiado para. As mensagens de status mesmo são copiadas para o arquivo. log.
    
### <a name="results-of-running-datacollectormasterexe-in-the-collect-mode"></a>Resultados da execução DataCollectorMaster.exe no modo de coletar

Depois de executar com êxito DataCollectorMaster.exe no modo de coletar, os seguintes arquivos são criados e armazenados nas pastas especificadas pelo `LogLocation` e `ConfigurationLocation` parâmetros. 
  
- **\<Nome_do_trabalho\>_coletar_\<DateTimeStamp\>. log** -o arquivo de log contém as mensagens de status que foram exibidas. Esse arquivo é criado na pasta especificada pelo `LogLocation` parâmetro. 
    
- **\<Nome_do_trabalho\>_coletar_\<DateTimeStamp\>. XML** -o arquivo XML contém apenas informações sobre os valores de parâmetro que onde usado pela ferramenta foi executada no modo de coletar. Os dados nesse arquivo são usados quando você executa execute novamente a ferramenta DataCollectorMaster.exe para excluir arquivos PST; Consulte a [etapa 5](#step-5-delete-the-pst-files-found-on-your-network).
    

## <a name="step-4-import-the-pst-files-to-office-365"></a>Etapa 4: Importe os arquivos PST para o Office 365

Depois que você coletou os arquivos PST encontrados na etapa 1, a próxima etapa é importá-los para caixas de correio no Office 365. Como parte ou o processo de importação, você precisará criar um arquivo de mapeamento de CSV que contém uma linha de cada arquivo PST que você deseja importar. Informações em cada linha especifica o nome do arquivo PST, endereço de email do usuário e se você deseja importar o arquivo PST para o usuário principal da ou arquivar caixas de correio. Use as informações a **nome_do_trabalho\>_Localizar_\<DateTimeStamp.csv** (criado na etapa) do arquivo 1 para ajudá-lo a criar o arquivo de mapeamento de CSV. 
  
Para obter instruções passo a passo importar arquivos PST para o Office 365, consulte um dos seguintes tópicos:
  
- [Usar o carregamento de rede para importar arquivos PST para o Office 365](use-network-upload-to-import-pst-files.md)
    
- [Usar o envio de unidade para importar arquivos PST para o Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md)
    

## <a name="step-5-delete-the-pst-files-found-on-your-network"></a>Etapa 5: Excluir arquivos PST encontrados em sua rede

Depois que os arquivos PST que você encontrou e coletados tenham sido importados para caixas de correio Exchange Online no Office 365, você pode usar a ferramenta de conjunto de PST para excluir os arquivos PST os locais de origem original onde eles foram encontrados na etapa 1. 
  
1. Abra um Prompt de comando (Executar como administrador) no computador local.
    
2. Vá até o diretório onde você baixou a ferramenta conjunto de PST.
    
3. Execute o seguinte comando para excluir os arquivos PST.

    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Delete -JobName <Name of job from Step 1> -ConfigurationLocation <Location of configuration files from Step 1> -CopyLocation <Location to copy PST files to>
    ```

    A tabela a seguir descreve os parâmetros e seus valores necessários quando você executar o comando DataCollectorMaster.exe para excluir arquivos PST. 
    
    |Parâmetro * * *|****Descrição****|Exemplos * * *|
    |:-----|:-----|:-----|
    | `DataSource` <br/> |Especifica o tipo de dados a ser pesquisado. No momento, você pode usar a ferramenta de conjunto de PST para procurar arquivos PST. ![espaçador](media/b078d05c-3aee-4b9f-8805-6a8a9d8970ee.png)           <br/> | `-DataSource Pst` <br/> |
    | `Mode` <br/> |Especifica o tipo de operação que executará a ferramenta. Use o valor `Delete` excluir arquivos PST que foram encontrados quando executou a ferramenta no modo de localizar.<br/> | `-Mode Delete` <br/> |
    | `JobName` <br/> |Especifica o nome de um trabalho de coleta de PST existente. Você tem que usar esse mesmo nome de trabalho que você usou quando executou a ferramenta no modo de localizar e o modo de coletar na etapa 1 e a etapa 3. Esse nome de trabalho, também é adicionado ao nome do arquivo de log que é criado quando você executar a ferramenta no modo de excluir.  <br/> | `-JobName PstSearch1` <br/> |
    | `ConfigurationLocation` <br/> |Especifica a pasta que contém o arquivo de configuração XML que foi criado quando você executou a ferramenta no modo de coletar. Use o mesmo valor que você usou para esse parâmetro na etapa 3.  <br/> | `-ConfigurationLocation "c:\users\admin\ desktop\PSTCollection\Configuration"` <br/> |
    | `LogLocation` <br/> |Especifica a pasta que será copiado para o arquivo de log para o modo de excluir. Esse é um parâmetro opcional. Se você não incluir a ele, o arquivo de log é copiado para a pasta onde você baixou a ferramenta conjunto de PST. Considere usar o mesmo local de log que você usou quando executou a ferramenta no Find and coletar modos na etapa 1 e a etapa 3 para que todos os arquivos de log são salvos na mesma pasta.  <br/> | `-LogLocation "c:\users\admin\desktop\PSTCollection"` <br/> |
    | `ForceRestart` <br/> |Esta opção permite que você execute novamente a ferramenta no modo de exclusão de um trabalho de coleta de PST existente. Se você executou anteriormente a ferramenta no modo de exclusão, mas que executou a ferramenta novamente no modo de localizar com o `ForceRestart` alternar para verificar novamente os locais dos arquivos PST, você pode usar essa opção para executar novamente a ferramenta no modo Delete e exclua os arquivos PST havia encontrado quando sua re-sca nned os locais. Ao usar o `ForceRestart` opção no modo Delete, a ferramenta ignora quaisquer operações de exclusão anteriores e tenta excluir os arquivos PST novamente.<br/> | `-ForceRestart` <br/> 

    Aqui está um exemplo da sintaxe para a ferramenta de DataCollectorMaster.exe usando valores reais para cada parâmetro:
    
    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Delete -JobName PstSearch1 -ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration" -LogLocation "c:\users\admin\desktop\PSTCollection"
    ```
   
    Após executar o comando, serão exibidas mensagens de status detalhado que mostram o progresso da exclusão dos arquivos PST que foram encontrados na etapa 1 e coletados na etapa 3. Após algum tempo, uma mensagem de status final mostra se ocorreram erros e o local em que o log é copiado para. As mensagens de status mesmo são copiadas para o arquivo. log.
    
### <a name="results-of-running-datacollectormasterexe-in-the-delete-mode"></a>Resultados da execução DataCollectorMaster.exe no modo de excluir

Depois de executar com êxito DataCollectorMaster.exe no modo de exclusão, os seguintes arquivos são criados e armazenados na pasta especificada pelo `LogLocation` e `ConfigurationLocation` parâmetros. 
  
- **\<Nome_do_trabalho\>_Excluir_\<DateTimeStamp\>. log** -o arquivo de log contém as mensagens de status que foram exibidas. Esse arquivo é criado na pasta especificada pelo `LogLocation` parâmetro. 
    
- **\<Nome_do_trabalho\>_Excluir_\<DateTimeStamp\>. XML** -o arquivo XML contém apenas informações sobre os valores de parâmetro que onde usado pela ferramenta foi executada no modo de excluir. Ela também lista o caminho do arquivo e o nome de cada arquivo PST que foi excluído. Esse arquivo é criado na pasta especificada pelo `ConfigurationLocation` parâmetro. 

---
title: Usar o carregamento de rede para importar arquivos PST da sua organização para o Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 103f940c-0468-4e1a-b527-cc8ad13a5ea6
description: 'Para administradores: Saiba como usar o carregamento de rede para importar arquivos PST em massa para as caixas de correio dos usuários no Office 365.'
ms.openlocfilehash: bd15216df69e003a5aaddb2ec21ede4da5c5c312
ms.sourcegitcommit: 33c8e9c16143650ca443d73e91631f9180a9268e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35854815"
---
# <a name="use-network-upload-to-import-your-organization-pst-files-to-office-365"></a>Usar o carregamento de rede para importar arquivos PST da sua organização para o Office 365

> [!NOTE]
> Este artigo é para administradores. Você está tentando importar arquivos PST para sua própria caixa de correio? Confira [Importar emails, contatos e calendário de um arquivo .pst do Outlook](https://go.microsoft.com/fwlink/p/?LinkID=785075)
  
Estas são as instruções passo a passo necessárias para usar o carregamento de rede para importar arquivos PST em massa para as caixas de correio do Office 365. Para perguntas frequentes sobre como usar o carregamento de rede para importar arquivos PST em massa para as caixas de correio do Office 365, consulte [Perguntas frequentes sobre como usar o carregamento de rede para importar arquivos PST](faqimporting-pst-files-to-office-365.md#using-network-upload-to-import-pst-files).
  
[Etapa 1: Copiar a URL SAS e instalar o Azure AzCopy](#step-1-copy-the-sas-url-and-install-azure-azcopy)

[Etapa 2: Carregar os arquivos PST no Office 365](#step-2-upload-your-pst-files-to-office-365)

[(Opcional) Etapa 3: Exibir uma lista dos arquivos PST carregados para o Office 365](#optional-step-3-view-a-list-of-the-pst-files-uploaded-to-office-365)

[Etapa 4: Criar o arquivo de mapeamento para Importação de PST](#step-4-create-the-pst-import-mapping-file)

[Etapa 5: Criar um trabalho de Importação de PST no Office 365](#step-5-create-a-pst-import-job-in-office-365)

[Etapa 6: Filtrar os dados e iniciar o trabalho de importação de PST](#step-6-filter-data-and-start-the-pst-import-job)

Observe que só é preciso executar a Etapa 1 apenas uma vez para importar arquivos PST para as caixas de correio do Office 365. Em seguida, faça os procedimentos das Etapas 2 a 6, sempre que desejar carregar e importar um lote de arquivos PST.

## <a name="before-you-begin"></a>Antes de começar
  
- A função Exportação Importação da Caixa de Correio no Exchange deve estar Online para importar arquivos PST para as caixas de correio do Office 365. Por padrão, essa função não é atribuída a nenhum grupo de funções no Exchange Online. Você pode adicionar a função Importação e Exportação de Caixa de Correio no grupo de função Gerenciamento da Organização. Mas se preferir, crie um novo grupo de função, atribua a função Importação e Exportação de Caixa de Correio e adicione a si próprio como membro. Para mais informações, confira as seções "Adicionar uma função a um grupo de funções" ou "Criar um grupo de funções" em [Gerenciar grupos de funções](https://go.microsoft.com/fwlink/p/?LinkId=730688).
    
    Além disso, para criar trabalhos de importação no Centro de Conformidade e Segurança, uma das alternativas a seguir deve ser verdadeira:
    
  - Você precisa ter a função Destinatários de email no Exchange Online. Por padrão, essa função é atribuída aos grupos de funções Gerenciamento da Organização e Gerenciamento de Destinatários.
    
    Ou
    
  - Você precisa ser um administrador global na sua organização do Office 365.
    
  > [!TIP]
    > Considere a criação de um novo grupo de função no Exchange Online destinado especificamente a importar os arquivos PST para o Office 365. Para o nível mínimo de privilégios necessários para importar os arquivos PST, atribua as funções de Exportação Importação de Caixa de Correio e Destinatários de email ao novo grupo de função e, em seguida, adicione membros. 
  
- O único método com suporte para importar arquivos PST para o Office 365 é a ferramenta Azure AzCopy, conforme descrito neste tópico. Não é possível usar o Gerenciador de Armazenamento do Azure para carregar arquivos PST diretamente para a área de armazenamento do Azure.
    
- Armazene os arquivos PST que pretende importar para o Office365 em um servidor de arquivos ou pasta compartilhada da organização. Na Etapa 2, execute a ferramenta AzCopy do Azure para carregar os arquivos PST armazenados nesse servidor de arquivos ou pasta compartilhada com o Office 365.
    
- Esse procedimento envolve copiar e salvar a cópia de uma URL que contenha a chave de acesso. Essa informação será usada na Etapa 2 para carregar os arquivos PST e, na Etapa 3, se desejar exibir uma lista dos arquivos PST carregados para o Office 365. Não deixe de tomar medidas para proteger essa URL, do mesmo modo que faria com senhas ou outras informações relacionadas à segurança. Por exemplo, é possível salvá-la em um documento do Microsoft Word protegido por senha ou em uma unidade USB criptografada. Confira a seção [Mais informações](#more-information) para ver um exemplo dessa URL e chave combinadas. 
    
- É possível importar arquivos PST para uma caixa de correio inativa no Office 365. Isso é feito especificando o GUID da caixa de correio inativa no `Mailbox` parâmetro no arquivo de mapeamento de importação de PST. Confira a Etapa 4, na guia **Instruções** deste tópico para mais informações. 
    
- Em uma implantação híbrida do Exchange, você pode importar arquivos PST para uma caixa de correio de arquivo morto baseada na nuvem para um usuário cuja caixa de correio principal esteja no local. Para isso, faça o seguinte no arquivo de mapeamento de Importação de PST:
    
  - Especifique o endereço de email para a caixa de correio local do usuário no `Mailbox` parâmetro. 
    
  - Especifique o valor **VERDADEIRO** no `IsArchive` parâmetro. 
    
    Consulte a [Etapa 4](#step-4-create-the-pst-import-mapping-file) para obter mais informações. 
    
- Após a importação dos arquivos PST para uma caixa de correio do Office 365, a configuração de bloqueio de retenção para a caixa de correio é ativada com uma duração indefinida. Isso significa que a política de retenção atribuída à caixa de correio não será processada até que o bloqueio de retenção seja desativado ou que uma data para a desativação seja definida. Por que fazemos isso? Se as mensagens importadas para uma caixa de correio forem antigas, poderão ser excluídas permanentemente (eliminadas) porque o período de retenção expirou com base nas configurações de retenção definidas para a caixa de correio. Colocar a caixa de correio no bloqueio de retenção dará ao proprietário tempo de gerenciar essas mensagens importadas recentemente ou tempo para alterar as configurações de retenção da caixa de correio. Confira a guia **Mais informações** neste tópico para obter sugestões sobre como gerenciar o bloqueio de retenção. 
    
- Por padrão, o tamanho máximo da mensagem que pode ser recebida por uma caixa de correio do Office 365 é 35 MB. Isso ocorre porque o valor padrão da *Propriedade MaxReceiveSize* de uma caixa de correio está definida como 35 MB. No entanto, o limite para o tamanho máximo de recebimento de mensagens no Office 365 é 150 MB. Portanto, se você importar um arquivo PST que contenha um item com mais de 35 MB, o serviço de importação do Office 365 altera automaticamente o valor da propriedade *MaxReceiveSize* na caixa de correio de destino para 150 MB. Isso permite que mensagens de até 150 MB sejam importadas para as caixas de correio dos usuários. 
    
    > [!TIP]
    > Para identificar o tamanho de recebimento da mensagem de uma caixa de correio, execute esse comando no Exchange Online PowerShell:  `Get-Mailbox <user mailbox> | FL MaxReceiveSize`. 

## <a name="step-1-copy-the-sas-url-and-install-azure-azcopy"></a>Etapa 1: Copiar a URL SAS e instalar o Azure AzCopy

A primeira etapa consiste em baixar e instalar a ferramenta Azure AzCopy, que é a ferramenta que será executada na Etapa 2 para carregar os arquivos PST para o Office 365. Você também pode copiar o URL da SAS para a sua organização. Essa URL é uma combinação da URL de rede para o local de armazenamento do Azure na nuvem da Microsoft para a sua organização e uma chave de Assinatura de Acesso Compartilhado (SAS). Essa chave fornece as permissões necessárias para carregar arquivos PST no local de armazenamento do Azure. Certifique-se de proteger a URL da SAS. Ela é exclusiva da sua organização e será usada na etapa 2.

> [!IMPORTANT]
> Para importar arquivos PST usando o método de carregamento de rede, recomendamos o uso da versão do Azure AzCopy que pode ser baixada na etapa 6B do procedimento a seguir.
  
1. Vá para [https://protection.office.com](https://protection.office.com) e entre usando as credenciais de uma conta de administrador do Office 365 da organização. 
    
2. No painel esquerdo do Centro de Conformidade e Segurança, clique em **Governança de dados** \> **Importar**.
    
    > [!NOTE]
    > É preciso ter as permissões apropriadas para acessar a página **Importar** no Centro de Conformidade de & Segurança. Confira a seção **Antes de começar** para mais informações. 
    
3. Na página **Importar**, clique em ![Adicionar Ícone](media/ITPro-EAC-AddIcon.gif) **Novo trabalho de importação**.
    
    O assistente de importação de trabalho será exibido.
    
4. Digite um nome para o trabalho de Importação PST e clique em **Avançar**. Use letras minúsculas, números, hifens e sublinhados. Não é possível usar letras maiúsculas ou incluir espaços no nome.
    
5. Na página **Você deseja carregar ou enviar dados?**, clique em **Carregar dados** e, em seguida, clique em **Avançar**.
    
    ![Clique em Carregar dados para criar um trabalho de importação de carregamento de rede](media/e59f9dc3-ccde-44ff-ac38-c4e39d76ae85.png)
  
6. Na página **Importar Dados**, execute as duas seguintes etapas: 
    
    ![Copie a URL SAS e baixe a ferramenta Azure AzCopy na página Importar dados](media/74411014-ec4b-4e25-9065-404c934cce17.png)
  
    a. Na etapa 2, clique em **Mostrar URL SAS de carregamento de rede**. Quando a URL SAS for exibida, clique em **Copiar para área de transferência** e, em seguida, cole-a e salve-a em um arquivo para que possa ser acessado mais tarde.
    
    b. Na etapa 3, clique em **Baixar Azure AzCopy** para baixar e instalar a ferramenta Azure AzCopy. Na janela pop-up, clique em **Executar** para instalar o AzCopy.. 
    
> [!NOTE]
> Você pode deixar a página ** Importar dados** aberta (caso precise copiar novamente a URL SAS) ou clicar em **Cancelar** para fechá-la. 
 
## <a name="step-2-upload-your-pst-files-to-office-365"></a>Etapa 2: Carregar os arquivos PST no Office 365

Agora, você está pronto para usar a ferramenta AzCopy.exe para carregar arquivos PST no Office 365. Essa ferramenta carrega e armazena arquivos no local de armazenamento do Azure na nuvem da Microsoft. Como explicado anteriormente, o local de armazenamento do Azure para o qual você carrega seus arquivos PST está localizado no mesmo datacenter da Microsoft que o Office 365 da sua organização está. Para concluir essa etapa, você deve colocar os arquivos PST em um compartilhamento de arquivos ou servidor de arquivos da organização. Esse local é conhecido como diretório de origem no procedimento a seguir. Sempre que executar a ferramenta AzCopy, você pode especificar um diretório de origem diferente. 
  
1. Abra um Prompt de Comando no computador local.
    
2. Vá para o diretório em que instalou a ferramenta AzCopy.exe na Etapa 1. Se você instalou a ferramenta no local padrão, vá para `%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy`.
    
3. Execute o seguinte comando para carregar os arquivos PST no Office 365.

    ```
    AzCopy.exe /Source:<Location of PST files> /Dest:<SAS URL> /V:<Log file location> /Y
  
    ```
 
    > [!IMPORTANT] 
    > Você deve especificar um diretório como o local de origem no comando anterior; você não pode especificar um arquivo PST individual. Todos os arquivos PST na pasta de origem serão carregados.
 
    A tabela a seguir descreve os parâmetros AzCopy.exe os valores necessários.  As informações obtidas nas etapas anteriores são usadas nos valores desses parâmetros.
    
    |**Parâmetro**|**Descrição**|**Exemplo**|
    |:-----|:-----|:-----|
    | `/Source:` <br/> |Especifica o diretório de origem na organização que contém os arquivos PST a serem carregados no Office365.  <br/> Certifique-se de colocar o valor deste parâmetro entre aspas duplas (" ").  <br/> | `/Source:"\\FILESERVER01\PSTs"` <br/> |
    | `/Dest:` <br/> |Especifica a URL SAS obtida na Etapa 1.  <br/> Certifique-se de colocar o valor deste parâmetro entre aspas duplas (" ").  <br/> **Dica:** (Opcional) Você pode especificar uma subpasta no local de armazenamento do Azure para carregar os arquivos PST. Para fazer isso, adicione um local de subpasta (após "ingestiondata") na URL SAS. O primeiro exemplo não especifica uma subpasta. Isso significa que os PSTs serão carregados na raiz (chamada *ingestiondata* ) do local de armazenamento do Azure. O segundo exemplo carrega os arquivos PST para uma subpasta (chamada  *PSTFiles*  ) na raiz do local de armazenamento do Azure.  <br/> | `/Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"` <br/> Ou  <br/>  `/Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata/PSTFiles?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"` <br/> |
    | `/V:` <br/> |Gera mensagens de status detalhadas em um arquivo de log. Por padrão, o arquivo de log detalhado é chamado AzCopyVerbose.log in %LocalAppData%\Microsoft\Azure\AzCopy. Se você especificar um local de arquivo existente para essa opção, o log detalhado será anexado a esse arquivo.  <br/> Certifique-se de colocar o valor deste parâmetro entre aspas duplas (" ").  <br/> | `/V:"c:\Users\Admin\Desktop\Uploadlog.log"` <br/> |
    | `/S` <br/> |Esse botão opcional especifica o modo recursivo para que a ferramenta AzCopy copie os arquivos PST localizados em subpastas do diretório de origem que é especificado pelo parâmetro `/Source:`.  <br/> **Observação:** Se incluir esse botão, os arquivos PST das subpastas terão nomes de caminho de arquivo diferentes, depois de carregá-los no local de armazenamento do Azure. Especifique o nome do caminho de arquivo exato no arquivo CSV que criado na etapa 4.  <br/> | `/S` <br/> |
    | `/Y` <br/> |Essa opção necessária permite o uso de tokens SAS somente gravação ao carregar arquivos PST no local de armazenamento do Azure. A URL SAS obtida na etapa 1 (e especificada no parâmetro `/Dest:`) é uma URL de SAS somente gravação, e é por isso que você deve incluir essa opção. Observe que uma URL SAS somente gravação não impedirá que Gerenciador de Armazenamento do Azure exiba uma lista dos arquivos PST carregados para o local de armazenamento do Azure.  <br/> | `/Y` <br/> |
   
Veja um exemplo da sintaxe para a ferramenta AzCopy.exe, que usa valores reais para os parâmetros:
    
```
  AzCopy.exe /Source:"\\FILESERVER1\PSTs" /Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D" /V:"c:\Users\Admin\Desktop\AzCopy1.log" /Y
  
```

Depois de executar o comando, o sistema exibe mensagens de status que mostram o andamento do carregamento dos arquivos PST. Uma mensagem de status final mostra o número total de arquivos que foram carregados com êxito.

> [!TIP]
> Depois de executar o comando AzCopy.exe com êxito e verificar se todos os parâmetros estão corretos, salve uma cópia da sintaxe da linha de comando no mesmo arquivo (protegido) em que copiou as informações obtidas na Etapa 1. Em seguida, você pode copiar e colar esse comando em um Prompt de Comando sempre que desejar executar a ferramenta AzCopy.exe para carregar arquivos PST no Office 365. O único valor que você pode ter que alterar é o para o `/Source:` parâmetro. Isso depende do diretório de origem onde os arquivos PST estão localizados.

## <a name="optional-step-3-view-a-list-of-the-pst-files-uploaded-to-office-365"></a>(Opcional) Etapa 3: Exibir uma lista dos arquivos PST carregados para o Office 365

Como uma etapa opcional, você pode instalar e usar o Gerenciador de Armazenamento do Microsoft Azure (que é uma ferramenta gratuita de código aberto) para exibir a lista dos arquivos PST carregados para o blob do Azure. Existem dois bons motivos para fazer isso:
  
- Verifique se os arquivos PST da pasta compartilhada ou servidor de arquivos em sua organização foram carregadas com êxito para o blob do Azure.
    
- Verifique se o nome do arquivo (e o nome do caminho da subpasta, se você incluiu um) para cada arquivo PST carregado para o blob do Azure. Isso será muito útil quando você estiver criando o arquivo de mapeamento PST na próxima etapa porque será preciso especificar o nome do caminho da pasta e o nome do arquivo para cada arquivo PST. Verificar esses nomes pode ajudar a reduzir possíveis erros no arquivo de mapeamento PST.
    
O Gerenciador de Armazenamento do Microsoft Azure está em Prévia.
  
> [!IMPORTANT]
> Não é possível usar o Gerenciador de Armazenamento do Azure para carregar ou modificar arquivos PST. O único método com suporte para a importação de arquivos PST para o Office 365 é o AzCopy. Além disso, não é possível excluir os arquivos PST que você carregou no blob do Azure. Se tentar excluir um arquivo PST, você receberá uma mensagem de erro informando que você não tem as permissões necessárias. Todos os arquivos PST são excluídos automaticamente da sua área de armazenamento do Azure. Se não houver trabalhos de importação em andamento, todos os arquivos PST no contêiner **ingestiondata** serão excluídos 30 dias após a criação do trabalho de importação mais recente.
  
Para instalar o Gerenciador de Armazenamento do Azure e se conectar à sua área de armazenamento do Azure:
  
1. Baixe e instale a [Ferramenta Gerenciador de Armazenamento do Microsoft Azure ](https://go.microsoft.com/fwlink/p/?LinkId=544842).
    
2. Inicie o Gerenciador de armazenamento do Microsoft Azure, clique com o botão direito do mouse em **Contas de Armazenamento** no painel esquerdo e clique em **Conectar-se ao Armazenamento do Azure**.
    
    ![Clique com o botão direito em Contas de Armazenamento em Conectar-se ao Armazenamento do Azure](media/75b80cc3-c336-4f96-ad32-54ac9b96a7af.png)
  
3. Clique em **Usar uma assinatura de acesso (SAS) URI ou uma cadeia de conexão** e clique em **Avançar**.
    
4. Clique em **Usar um URI SAS**, cole a URL SAS obtida na Etapa 1 na caixa em **URI**e clique em **Avançar**.
    
5. Na página **Resumo da conexão**, você pode revisar as informações de conexão e, em seguida, clique em **Conectar**.
    
    O contêiner **ingestiondata** é aberto, ele contém os arquivos PST carregados na Etapa 2. O contêiner **ingestiondata** está localizado em uma **Conta de Armazenamento** \> **(SAS-Serviços Anexados)**\> **Contêineres de Blob**. 
    
    ![O Gerenciador de Armazenamento do Azure exibe uma lista dos arquivos PST que você carregou](media/12376fed-13a5-4a09-8fe6-e819e011b334.png)
  
6. Ao terminar de usar o Gerenciador de Armazenamento do Azure, clique com botão direito em **ingestiondata** e, em seguida, clique em **Desanexar** para desconectar-se da sua área de armazenamento do Azure. Caso contrário, você receberá uma mensagem de erro na próxima vez que tentar anexar. 
    
    ![Clique com o botão direito em ingestão e clique em Desanexar para desconectar da sua área de armazenamento do Azure](media/1e8e5e95-4215-4ce4-a13d-ab5f826a0510.png)
  
## <a name="step-4-create-the-pst-import-mapping-file"></a>Etapa 4: Criar o arquivo de mapeamento para Importação de PST

Depois de carregar os arquivos PST no local de armazenamento do Azure para a organização do Office 365, a etapa seguinte consiste em criar um arquivo CSV que especifica as caixas de correio de usuário nas quais os arquivos PST devem ser importados. Você enviará esse arquivo CSV na etapa seguinte, quando criar um trabalho de Importação de PST.
  
1. [Baixar uma cópia do arquivo de mapeamento para importação de PST](https://go.microsoft.com/fwlink/p/?LinkId=544717).
    
2. Abrir ou salvar o arquivo CSV no computador local. O exemplo a seguir mostra um arquivo de mapeamento para Importação de PST concluído (aberto no Bloco de notas). É muito mais fácil usar o Microsoft Excel para editar o arquivo CSV.


    ```
    Workload,FilePath,Name,Mailbox,IsArchive,TargetRootFolder,ContentCodePage,SPFileContainer,SPManifestContainer,SPSiteUrl
    Exchange,,annb.pst,annb@contoso.onmicrosoft.com,FALSE,/,,,,
    Exchange,,annb_archive.pst,annb@contoso.onmicrosoft.com,TRUE,,,,,
    Exchange,,donh.pst,donh@contoso.onmicrosoft.com,FALSE,/,,,,
    Exchange,,donh_archive.pst,donh@contoso.onmicrosoft.com,TRUE,,,,,
    Exchange,PSTFiles,pilarp.pst,pilarp@contoso.onmicrosoft.com,FALSE,/,,,,
    Exchange,PSTFiles,pilarp_archive.pst,pilarp@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    Exchange,PSTFiles,tonyk.pst,tonyk@contoso.onmicrosoft.com,FALSE,,,,,
    Exchange,PSTFiles,tonyk_archive.pst,tonyk@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    Exchange,PSTFiles,zrinkam.pst,zrinkam@contoso.onmicrosoft.com,FALSE,,,,,
    Exchange,PSTFiles,zrinkam_archive.pst,zrinkam@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    ```
    A primeira linha ou linha de cabeçalho do arquivo CSV enumera os parâmetros que serão usados pelo serviço de Importação de PST para importar os arquivos PST para as caixas de correio de usuário. Os nomes dos parâmetros são separados por vírgula. Cada linha sob a linha de cabeçalho representa os valores de parâmetro para a importação de um arquivo PST em uma caixa de correio específica. Use uma linha para cada arquivo PST que deseja importar para uma caixa de correio de usuário. Não deixe de substituir os dados de espaço reservado do arquivo de mapeamento pelos dados reais.

   **Observação**Não altere o conteúdo da linha do cabeçalho, inclusive os parâmetros SharePoint; eles serão ignorados durante o processo de Importação de PST. 

 3. Use as informações da tabela a seguir para preencher o arquivo CSV com as informações necessárias.


    |**Parâmetro**|**Descrição**|**Exemplo**|
    |:-----|:-----|:-----|
    | `Workload` <br/> |Especifica o serviço do Office 365 para o qual os dados serão importados. Para importar arquivos PST nas caixas de correio de usuário, use o  `Exchange`.  <br/> | `Exchange` <br/> |
    | `FilePath` <br/> |Especifica o local da pasta, no local de armazenamento do Azure, em que você carregou os arquivos PST na Etapa 2.  <br/> Se você não incluir um nome de subpasta opcional na URL SAS no parâmetro `/Dest:` na Etapa 2, deixe esse parâmetro em branco no arquivo CSV. Se você incluiu um nome de subpasta, especifique-o nesse parâmetro (consulte o segundo exemplo). O valor desse parâmetro diferencia maiúsculas de minúsculas.  <br/> De qualquer forma, *não* inclua "ingestiondata" no valor do parâmetro`FilePath`.  <br/><br/> **Importante:** A capitalização do nome do caminho do arquivo deve ser a mesma usada caso você tenha incluído um nome de subpasta opcional na URL SAS `/Dest:` no parâmetro na Etapa 2. Por exemplo, se você usou `PSTFiles` para o nome da subpasta na Etapa 2 e, em seguida usar `pstfiles` no parâmetro `FilePath` no arquivo CSV, a importação para o arquivo PST falhará. Certifique-se de usar a mesma capitalização nas duas instâncias.  <br/> |(deixar em branco)  <br/> Ou  <br/>  `PSTFiles` <br/> |
    | `Name` <br/> |Especifique o nome do arquivo PST que será importado para a caixa de correio do usuário. O valor desse parâmetro diferencia maiúsculas de minúsculas.  <br/> <br/>**Importante:** A capitalização do nome do arquivo PST no arquivo CSV deve ser igual ao arquivo PST que foi carregado para o local de armazenamento do Azure na Etapa 2. Por exemplo, se você usar `annb.pst` o `Name` no parâmetro no arquivo CSV, mas o nome do arquivo PST atual for `AnnB.pst`, a importação desse arquivo PST falhará. Certifique-se de que o nome do PST no arquivo CSV usa a mesma capitalização do arquivo PST atual.  <br/> | `annb.pst` <br/> |
    | `Mailbox` <br/> |Especifica o endereço de email da caixa de correio para a qual o arquivo PST será importado. Observe que não é possível especificar uma pasta pública porque o Serviço de Importação de PST não é compatível com a importação de arquivos PST para pastas públicas.  <br/> Para importar um arquivo PST para uma caixa de correio inativa, é preciso especificar o GUID da caixa de correio para esse parâmetro. Para obter esse GUID, execute o seguinte comando do PowerShell no Exchange Online:  `Get-Mailbox <identity of inactive mailbox> -InactiveMailboxOnly | FL Guid` <br/> <br/>**Observação:** Em alguns casos, você pode ter várias caixas de correio com o mesmo endereço de email, em que uma caixa de correio é uma caixa de correio ativa e a outra caixa de correio está em um estado de exclusão flexível (ou inativo). Nesses casos, você precisa especificar o GUID da caixa de correio para identificar exclusivamente a caixa de correio para a qual o arquivo PST será importado. Para obter esse GUID para caixas de correio ativas, execute o seguinte comando do PowerShell:  `Get-Mailbox <identity of active mailbox> | FL Guid`. Para obter o GUID de caixas de correio de exclusão flexível (ou inativos), execute este comando  `Get-Mailbox <identity of soft-deleted or inactive mailbox> -SoftDeletedMailbox | FL Guid`.  <br/> | `annb@contoso.onmicrosoft.com` <br/> Ou  <br/>  `2d7a87fe-d6a2-40cc-8aff-1ebea80d4ae7` <br/> |
    | `IsArchive` <br/> | Especifica se deve ou não importar o arquivo PST para a caixa de correio de arquivo morto do usuário. Há duas opções:  <br/><br/>**FALSO** - Importa o arquivo PST para a caixa de correio principal do usuário.  <br/> **VERDADEIRO** - Importa o arquivo PST para a caixa de correio de arquivo morto do usuário. Isso pressupõe que a [caixa de correio de arquivo morto do usuário está habilitada](enable-archive-mailboxes.md). <br/><br/>Se definir este parâmetro para `TRUE` e a caixa de correio de arquivo morto do usuário não estiver habilitada, a importação para esse usuário falhará. Se uma importação falhar para um usuário (porque o arquivo morto dele não está habilitado e esta propriedade está definida para `TRUE`), os outros usuários no trabalho de importação não serão afetados.  <br/>  Se você deixar este parâmetro em branco, o arquivo PST será importado para a caixa de correio principal do usuário.  <br/> <br/>**Observação:** para importar um arquivo PST para uma caixa de correio de arquivo morto baseada na nuvem de um usuário cuja caixa de correio principal está no local, basta especificar `TRUE` para este parâmetro e especificar o endereço de email da caixa de correio no local do usuário para o parâmetro `Mailbox`.  <br/> | `FALSE` <br/> Ou  <br/>  `TRUE` <br/> |
    | `TargetRootFolder` <br/> | Especifica a pasta da caixa de correio para a qual o arquivo PST será importado.  <br/>  Se deixar este parâmetro em branco, o arquivo PST será importado para uma nova pasta chamada **Itens importados**, localizada no nível raiz da caixa de correio (o mesmo nível da pasta Caixa de Entrada e de outras pastas da caixa de correio padrão).  <br/>  Se você especificar `/`, os itens no arquivo PST serão importados diretamente para a pasta Caixa de Entrada do usuário.  <br/><br/>  Se você especificar `/<foldername>`, os itens no arquivo PST serão importados para uma pasta chamada *\<foldername\>*  . Por exemplo, se você usar  `/ImportedPst` os itens serão importados para uma pasta chamada **ImportedPst**. Essa pasta estará localizada na caixa de correio do usuário, no mesmo nível da pasta Caixa de Entrada.  <br/><br/> **Dica:** Considere a execução de alguns lotes de teste para experimentar esse parâmetro, de modo que você possa determinar o melhor local da pasta para importar os arquivos PST.   <br/> |(deixar em branco)  <br/> Ou  <br/>  `/` <br/> Ou  <br/>  `/ImportedPst` <br/> |
    | `ContentCodePage` <br/> |Esse parâmetro opcional especifica um valor numérico para a página do código a ser usado para importar arquivos PST no formato de arquivo ANSI. Esse parâmetro é usado para importar arquivos PST de organizações em chinês, japonês e coreano (CJK) porque esses idiomas geralmente usam um DBCS (conjunto de caracteres de dois bytes) para codificação de caracteres. Se esse parâmetro não for usado para importar arquivos PST para idiomas que usam DBCS para nomes de pasta de caixa de correio, os nomes das pastas geralmente ficam incorretos após a importação.  <br/><br/> Para obter uma lista de valores com suporte para esse parâmetro, confira [Identificadores de Página de Código](https://go.microsoft.com/fwlink/p/?LinkId=328514).  <br/> <br/>**Observação:** Como mencionado anteriormente, esse é um parâmetro opcional, e você não precisa incluí-lo no arquivo CSV. Ou você pode incluí-lo e deixar o valor em branco para uma ou mais linhas.  <br/> |(deixar em branco)  <br/> Ou  <br/>  `932` (que é o identificador da página de código para ANSI/OEM japonês)  <br/> |
    | `SPFileContainer` <br/> |Deixe este parâmetro em branco para Importação de PST.  <br/> |Não aplicável  <br/> |
    | `SPManifestContainer` <br/> |Deixe este parâmetro em branco para Importação de PST.  <br/> |Não aplicável  <br/> |
    | `SPSiteUrl` <br/> |Deixe este parâmetro em branco para Importação de PST.  <br/> |Não aplicável  <br/> |

## <a name="step-5-create-a-pst-import-job-in-office-365"></a>Etapa 5: Criar um trabalho de Importação de PST no Office 365

A etapa a seguir consiste em criar o trabalho de Importação de PST no serviço Importação do Office 365. Conforme explicamos, envie o arquivo de mapeamento para Importação de PST criado na Etapa 4. Depois de criar o novo trabalho, o Office 365 analisa os dados dos arquivos PST e oferece a oportunidade de filtrar os dados que realmente serão importados para as caixas de correio especificadas no arquivo de mapeamento de importação PST (consulte a [Etapa 6](#step-6-filter-data-and-start-the-pst-import-job)).
  
1. Vá para [https://protection.office.com](https://protection.office.com) e entre usando as credenciais de uma conta de administrador do Office 365 da organização. 
    
2. No painel esquerdo do Centro de Conformidade e Segurança, clique em **Governança de dados** e clique em **Importar**.
    
3. Na página **Importar**, clique em ![Adicionar Ícone](media/ITPro-EAC-AddIcon.gif) **Novo trabalho de importação**.
    
    **Observação:** É preciso ter as permissões apropriadas para acessar a página **Importar** no Centro de Conformidade de & Segurança para criar um novo trabalho de importação. Confira a seção **Antes de começar** para mais informações. 
    
4. Digite um nome para o trabalho de Importação PST e clique em **Avançar**. Use letras minúsculas, números, hifens e sublinhados. Não é possível usar letras maiúsculas ou incluir espaços no nome.
    
5. Na página **Você deseja carregar ou enviar dados?**, clique em **Carregar dados** e, em seguida, clique em **Avançar**.
    
    ![Clique em Carregar dados para criar um trabalho de importação de carregamento de rede](media/e59f9dc3-ccde-44ff-ac38-c4e39d76ae85.png)
  
6. Na etapa 4 n página **Importar Dados**, marque as caixas de seleção **Eu acabei de carregar os meus arquivos** e **Eu tenho acesso aos arquivos de mapeamento** e, em seguida, clique em **Avançar**. 
    
    ![Clique nas duas caixas de seleção na etapa 4](media/9f2427e8-3af2-4e27-95e6-a9f08430d3d8.png)
  
7. Na página **Selecionar o arquivo de mapeamento**, clique em **Selecionar arquivo de mapeamento** para enviar o arquivo de mapeamento de Importação PST que você criou na Etapa 4. 
    
    ![Clique em Selecionar arquivo de mapeamento para enviar o arquivo CSV que você criou para o trabalho de importação](media/d30b1d73-80bb-491e-a642-a21673d06889.png)
  
8. Após o nome do arquivo CSV aparecer em **Nome do arquivo de mapeamento**, clique em **Validar** para verificar se há erros no arquivo CSV. 
    
    ![Clique em Validar para verificar se há erros no arquivo CSV](media/4680999d-5538-4059-b878-2736a5445037.png)
  
    O arquivo CSV deve ser validado com êxito para criar um trabalho de importação de PST. Observe que o nome do arquivo é alterado para verde após ser validado com êxito. Se a validação falhar, clique no link **Exibir log**. Um relatório de erro de validação é aberto, com uma mensagem de erro para cada linha no arquivo que falhou. 
    
9. Após validar o arquivo de mapeamento para Importação de PST com êxito, leia o documento de termos e condições e marque a caixa de seleção.
    
10. Clique em **Salvar** para enviar o trabalho e, em seguida, clique em **Fechar** após o trabalho ter sido criado com êxito. 
    
    Uma página de status com submenu é exibida, com o status da **Análise em andamento** e o novo trabalho de importação é exibido na lista da página **Importar**. 
    
11. Clique em **Atualizar** ![Ícone Atualizar](media/O365-MDM-Policy-RefreshIcon.gif) para atualizar as informações de status exibidas na coluna**Status**.  Quando a análise estiver concluída e os dados estiverem prontos para serem importados, o status será alterado para**Análise concluída**.
    
    Você pode clicar no trabalho de importação para exibir a página de status com submenu, que contém informações mais detalhadas sobre o trabalho de importação, como o status de cada arquivo PST listado no arquivo de mapeamento.
 
## <a name="step-6-filter-data-and-start-the-pst-import-job"></a>Etapa 6: Filtrar os dados e iniciar o trabalho de importação de PST

Depois de criar o trabalho de importação na Etapa 5, o Office 365 analisa os dados dos arquivos PST (de maneira segura) identificando a idade dos itens e os diferentes tipos de mensagem contidos nos arquivos PST. Quando esta análise for concluída e os dados estiverem prontos para importação, você terá a opção de importar todos os dados contidos nos arquivos PST ou cortar os dados que serão importados configurando filtros para controlar quais dados serão importados.
  
1. Na página **Importar** no Centro de Conformidade & de Segurança, clique em **Pronto para importar para o Office 365** para o trabalho de importação que você criou na Etapa 5. 
    
    ![Clique em Pronto para importar para o Office 365 ao lado do trabalho de importação criado](media/5760aac3-300b-4e31-b894-253c42a4b82b.png)
  
    Uma página com submenu é exibida com informações sobre os arquivos PST e outras informações sobre o trabalho de importação.
    
2. Na página com submenu, clique em **Importar para o Office 365**.
    
    A página **Filtrar seus dados** é exibida. Ela contém as informações sobre dados resultantes da análise realizada nos arquivos PST do Office 365, incluindo informações sobre a idade dos dados. Neste ponto, você tem a opção de filtrar os dados que serão importados ou importar todos os dados como estão. 
    
    ![Você pode cortar os dados dos arquivos PST ou importá-los](media/287fc030-99e9-417b-ace7-f64617ea5d4e.png)
  
3. Siga um destes procedimentos:
    
    a. Para cortar os dados importados, clique em **Sim, desejo filtrá-los antes de importá-los**.
    
    Para obter instruções passo a passo detalhadas sobre como filtrar os dados nos arquivos PST e iniciar o trabalho de importação, confira [Filtrar dados ao importar arquivos PST para o Office 365](filter-data-when-importing-pst-files.md).
    
    Ou
    
    b. Para importar todos os dados dos arquivos PST, clique em **Não, Desejo importar tudo** e clique em **Avançar**.
    
4. Se optar por importar todos os dados, clique em **Importar dados** para iniciar o trabalho de importação. 
    
    O status do trabalho de importação é exibido na página **Importar.** Clique no ![Ícone Atualizar](media/O365-MDM-Policy-RefreshIcon.gif) **Atualizar** para atualizar as informações de status exibidas na coluna**Status**.  Clique no trabalho de importação para exibir a página de status do submenu, que exibe informações de status sobre cada arquivo PST sendo importado.. 

## <a name="how-the-import-process-works"></a>Como o processo de importação funciona
  
Você pode usar a opção de carregamento de rede e o serviço de importação do Office 365 para importar arquivos PST para as caixas de correio dos usuários. O carregamento de rede significa que você carrega os arquivos PST em uma área de armazenamento temporário na nuvem da Microsoft. Em seguida, o serviço de Importação do Office 365 copia os arquivos PST da área armazenamento para as caixas de correio do usuário de destino.
  
Esta é uma ilustração e uma descrição do processo de carregamento de rede para importar arquivos PST para caixas de correio no Office 365.
  
![Fluxo de trabalho do processo de carregamento de rede para importar arquivos PST para o Office 365](media/9e05a19e-1e7a-4f1f-82df-9118f51588c4.png)
  
1. **Baixar a ferramenta de importação de PST e a chave para o local privado de armazenamento do Azure** - A primeira etapa é baixar a ferramenta de linha de comando do Azure AzCopy e uma chave de acesso usada para carregar os arquivos PST em um local de armazenamento do Azure na nuvem da Microsoft. Você obtém isso na página **Importar** no Centro de Conformidade e Segurança. A chave SAS (chamada de chave de assinatura de acesso seguro) fornece as permissões necessárias para carregar arquivos PST para um local de armazenamento do Azure particular e seguro. Essa chave de acesso é exclusiva à sua organização e ajuda a impedir o acesso não autorizado aos seus arquivos PST depois que eles são carregados na nuvem da Microsoft. Observe que importar arquivos PST para o Office 365 não exige que sua organização tenha uma assinatura separada do Azure. 
    
2. **Carregue os arquivos PST para o loca de armazenamento do Azurel** - Aa próxima etapa é usar a ferramenta AzCopy. exe (baixada na etapa 1) para carregar e armazenar os arquivos PST em um local de armazenamento do Azure que resida no mesmo datacenter regional da Microsoft que o Office 365 da organização está localizado. Para carregá-los, os arquivos PST que você deseja importar para o Office 365 devem estar localizados em um compartilhamento de arquivos ou em um servidor de arquivos em sua organização.
    
    Observe que há uma etapa opcional que você pode executar para exibir a lista de arquivos PST após eles serem carregados para o local de armazenamento do Azure.
    
3. **Criar um arquivo de mapeamento de importação de PST** - Depois de carregar os arquivos PST para o local de armazenamento do Azure, a próxima etapa é criar um arquivo de valores separados por vírgula (CSV) que especifica para quais caixas de correio de usuário os arquivos PST serão importados, observe que um arquivo PST pode ser importado para caixa de correio principal do usuário ou para a caixa de correio de arquivo morto. O serviço de Importação do Office 365 usará as informações no arquivo CSV para importar os arquivos PST.
    
4. **Criar um trabalho de importação PST** - A próxima etapa é criar um trabalho de importação PST na página **Importar** no Centro de Conformidade e Segurança e enviar o arquivo de mapeamento de importação PST criado na etapa anterior. Depois de criar o trabalho de importação, o Office 365 analisa os dados dos arquivos PST e oferece a oportunidade de definir filtros que controlam quais dados serão importados para as caixas de correio especificadas no arquivo de mapeamento de importação de PST. 
    
5. **Filtrar os dados PST que serão importados para as caixas de correio** - Depois que o trabalho de importação é criado e iniciado, o Office 365 analisa os dados nos arquivos PST (de forma segura) identificando a idade dos itens e os diferentes tipos de mensagens incluídas nos arquivos PST. Quando esta análise for concluída e os dados estiverem prontos para importação, você terá a opção de importar todos os dados contidos nos arquivos PST ou cortar os dados que serão importados configurando filtros para controlar quais dados serão importados.
    
6. **Iniciar o trabalho de importação de PST** - Depois que o trabalho de importação é iniciado, o Office 365 usa as informações do arquivo de mapeamento de importação de PST para importar os arquivos PSTs do local de armazenamento do Azure para caixas de correio de usuário. Informações de status sobre o trabalho de importação (incluindo informações sobre cada arquivo PST que está sendo importado) são exibidas na página **Importar** no Centro de Conformidade e Segurança. Quando o trabalho de importação for concluído, o status do trabalho será definido como **Concluído**. 
  
## <a name="more-information"></a>Mais informações

- Por que importar arquivos PST para o Office 365?
    
  - É uma boa maneira de importar os dados das mensagens de arquivamento da sua organização para o Office 365.
    
  - Os dados ficam disponíveis para o usuário em todos os dispositivos, pois eles são armazenados na nuvem.
    
  - Isso ajuda a lidar com as necessidades de conformidade da sua organização, permitindo que você aplique os recursos de conformidade do Office 365 aos dados dos arquivos PST que você importou. Isso inclui:
    
  - Ativar as caixas de correio de [arquivo morto](enable-archive-mailboxes.md) e [arquivamento com expansão automática](enable-unlimited-archiving.md) para fornecer aos usuários espaço adicional de armazenamento de caixa de correio para armazenar os dados que você importou. 
    
  - Colocar as caixas de correio em [Retenção de Litígio](https://go.microsoft.com/fwlink/?linkid=856286) para manter os dados que você importou. 
    
  - Usar as ferramentas de [Descoberta Eletrônica](search-for-content.md) da Microsoft para pesquisar os dados que você importou. 
    
  - Usar [as políticas de retenção do Office 365](retention-policies.md) para controlar quanto tempo os dados importados serão mantidos e qual ação deve ser realizada após o término do período de retenção. 
    
  - Pesquisar [o log de auditoria do Office 365](search-the-audit-log-in-security-and-compliance.md) para eventos relacionados à caixa de correio que afetem os dados que você importou. 
    
  - Importar dados para [caixas de correio inativas](create-and-manage-inactive-mailboxes.md) para arquivar dados para fins de conformidade. 
    
  - Usar [políticas de prevenção contra perda de dados](data-loss-prevention-policies.md) para evitar que dados confidenciais saiam da sua organização. 
  
- Veja um exemplo de URL SAS (Assinatura de Acesso Compartilhado) obtida na Etapa 1. Este exemplo inclui também a sintaxe do comando executado na ferramenta AzCopy.exe para carregar arquivos PST no Office 365. Certifique-se de tomar medidas para proteger a URL SAS, do mesmo modo que o faria com senhas ou outras informações relacionadas à segurança.

    ```
    SAS URL: https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D

    AzCopy.exe /Source:<Location of PST files> /Dest:<SAS URL> /V:<Log file location> /Y

    EXAMPLES

    This example uploads PST files to the root of the Azure storage location:

    AzCopy.exe /Source:"\\FILESERVER1\PSTs" /Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D" /V:"c:\Users\Admin\Desktop\AzCopy1.log" /Y
    
    This example uploads PST files to a subfolder named PSTFiles  in the Azure storage location:

    AzCopy.exe /Source:"\\FILESERVER1\PSTs" /Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata/PSTFiles?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D" /V:"c:\Users\Admin\Desktop\AzCopy1.log" /Y
``

- As previously explained, the Office 365 Import service turns on the retention hold setting (for an indefinite duration) after PST files are imported to a mailbox. This means the  *RetentionHoldEnabled*  property is set to  **True** so that the retention policy assigned to the mailbox won't be processed. This gives the mailbox owner time to manage the newly-imported messages by preventing a deletion or archive policy from deleting or archiving older messages. Here are some steps you can take to manage this retention hold: 
    
    - After a certain period of time, you can turn off the retention hold by running the **Set-Mailbox -RetentionHoldEnabled $false** command. For instructions, see [Place a mailbox on retention hold](https://go.microsoft.com/fwlink/p/?LinkId=544749).
    
   - You can configure the retention hold so that it's turned off on some date in the future. You do this by running the **Set-Mailbox -EndDateForRetentionHold *date*** command. For example, assuming that today's date is June 1, 2016 and you want the retention hold turned off in 30 days, you would run the following command:  **Set-Mailbox -EndDateForRetentionHold 7/1/2016**. In this scenario, you would leave the  **RetentionHoldEnabled**  property set to  *True*. For more information, see [Set-Mailbox](https://go.microsoft.com/fwlink/p/?LinkId=150317).
    
   - You can change the settings for the retention policy that's assigned to the mailbox so that older items that were imported won't be immediately deleted or moved to the user's archive mailbox. For example, you could lengthen the retention age for a deletion or archive policy that's assigned to the mailbox. In this scenario, you would turn off the retention hold on the mailbox after you changed the settings of the retention policy. For more information, see [Set up an archive and deletion policy for mailboxes in your Office 365 organization](set-up-an-archive-and-deletion-policy-for-mailboxes.md).
    

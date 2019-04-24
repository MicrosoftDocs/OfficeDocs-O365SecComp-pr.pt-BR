---
title: Usar o carregamento de rede para importar arquivos PST da sua organização para o Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 103f940c-0468-4e1a-b527-cc8ad13a5ea6
description: 'Para administradores: saiba como usar o carregamento de rede para importar em massa vários arquivos PST para caixas de correio de usuário no Office 365.'
ms.openlocfilehash: 73123d5f36a01b31cfc38e6404bd400bb722fb36
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32264182"
---
# <a name="use-network-upload-to-import-your-organization-pst-files-to-office-365"></a>Usar o carregamento de rede para importar arquivos PST da sua organização para o Office 365

> [!NOTE]
> Este artigo é para administradores. Você está tentando importar arquivos PST para sua própria caixa de correio? ConFira [importar email, contatos e calendário de um arquivo. pst do Outlook](https://go.microsoft.com/fwlink/p/?LinkID=785075)
  
Aqui estão as instruções passo a passo necessárias para usar o carregamento de rede para importar vários arquivos PST de importação em massa para as caixas de correio do Office 365. Para perguntas frequentes sobre como usar o carregamento de rede para arquivos PST de importação em massa para caixas de correio do Office 365, confira perguntas frequentes sobre como [usar o carregamento de rede para importar arquivos PST](faqimporting-pst-files-to-office-365.md#using-network-upload-to-import-pst-files).
  
[Etapa 1: copiar a URL SAS e instalar o Azure AzCopy](#step-1-copy-the-sas-url-and-install-azure-azcopy)

[Etapa 2: carregar os arquivos PST no Office 365](#step-2-upload-your-pst-files-to-office-365)

[Opcion Etapa 3: exibir uma lista dos arquivos PST carregados para o Office 365](#optional-step-3-view-a-list-of-the-pst-files-uploaded-to-office-365)

[Etapa 4: criar o arquivo de mapeamento de importação de PST](#step-4-create-the-pst-import-mapping-file)

[Etapa 5: criar um trabalho de importação de PST no Office 365](#step-5-create-a-pst-import-job-in-office-365)

[Etapa 6: filtrar os dados e iniciar o trabalho de importação de PST](#step-6-filter-data-and-start-the-pst-import-job)

Observe que você precisa executar a etapa 1 apenas uma vez para importar arquivos PST para caixas de correio do Office 365. Após executar essas etapas, siga a etapa 2 até a etapa 6 cada vez que desejar carregar e importar um lote de arquivos PST.

## <a name="before-you-begin"></a>Antes de começar
  
- Você deve ser atribuído à função de exportação de importação de caixa de correio no Exchange Online para importar arquivos PST para caixas de correio do Office 365. Por padrão, essa função não é atribuída a nenhum grupo de função no Exchange Online. You can add the Mailbox Import Export role to the Organization Management role group. Or you can create a new role group, assign the Mailbox Import Export role, and then add yourself as a member. Para obter mais informações, consulte as seções "adicionar uma função a um grupo de funções" ou "criar um grupo de função" em [Manage role groups](https://go.microsoft.com/fwlink/p/?LinkId=730688).
    
    Além disso, para criar trabalhos de importação no centro de conformidade do & de segurança, um dos seguintes deve ser verdadeiro:
    
  - Você precisa receber a função de destinatários de email no Exchange Online. By default, this role is assigned to the Organization Management and Recipient Management roles groups.
    
    Ou
    
  - Você deve ser um administrador global em sua organização do Office 365.
    
  > [!TIP]
    > Considere a criação de um novo grupo de função no Exchange Online destinado especificamente à importação de arquivos PST para o Office 365. Para obter o nível mínimo de privilégios necessários para importar arquivos PST, atribua as funções de importação de caixa de correio e destinatários de email ao novo grupo de funções e, em seguida, adicione membros. 
  
- O único método com suporte para importar arquivos PST para o Office 365 é usar a ferramenta AzCopy do Microsoft Azure, conforme descrito neste tópico. Você não pode usar o Gerenciador de armazenamento do Azure para carregar arquivos PST diretamente na área de armazenamento do Azure.
    
- Você precisa armazenar os arquivos PST que deseja importar para o Office 365 em um servidor de arquivos ou pasta compartilhada em sua organização. Na etapa 2, você executará a ferramenta AzCopy do Azure que carregará os arquivos PST armazenados neste servidor de arquivos ou pasta compartilhada para o Office 365.
    
- Este procedimento envolve copiar e salvar uma cópia de uma URL que contém uma chave de acesso. Essas informações serão usadas na etapa 2 para carregar os arquivos PST e, na etapa 3, se você quiser exibir uma lista dos arquivos PST carregados para o Office 365. Certifique-se de ter precauções para proteger esta URL como você protegeria senhas ou outras informações relacionadas à segurança. Por exemplo, você pode salvá-lo em um documento do Microsoft Word protegido por senha ou em uma unidade USB criptografada. Consulte a seção [mais informações](#more-information) para obter um exemplo desse URL e chave combinados. 
    
- Você pode importar arquivos PST para uma caixa de correio inativa no Office 365. Para fazer isso, especifique o GUID da caixa de correio inativa no `Mailbox` parâmetro no arquivo de mapeamento de importação de PST. Consulte a etapa 4 na guia **instruções** deste tópico para obter informações. 
    
- Em uma implantação híbrida do Exchange, você pode importar arquivos PST para uma caixa de correio de arquivo morto baseado na nuvem para um usuário cuja caixa de correio principal esteja no local. Para fazer isso, faça o seguinte no arquivo de mapeamento de importação de PST:
    
  - Especifique o endereço de email da caixa de correio local do usuário no `Mailbox` parâmetro. 
    
  - Especifique o valor **true** no `IsArchive` parâmetro. 
    
    Consulte a [etapa 4](#step-4-create-the-pst-import-mapping-file) para obter mais informações. 
    
- Depois que os arquivos PST são importados para uma caixa de correio do Office 365, a configuração de retenção da caixa de correio é ativada por uma duração indefinida. Isso significa que a política de retenção atribuída à caixa de correio não será processada até que você desative o bloqueio de retenção ou defina uma data para desativar o bloqueio. Por que fazemos isso? Se as mensagens importadas para uma caixa de correio forem antigas, elas poderão ser excluídas permanentemente (descartadas) porque o período de retenção expirou com base nas configurações de retenção configuradas para a caixa de correio. Colocar a caixa de correio no bloqueio de retenção fornecerá ao proprietário da caixa de correio o tempo para gerenciar essas mensagens importadas recentemente ou dará tempo para alterar as configurações de retenção da caixa de correio. Consulte a guia **mais informações** neste tópico para obter sugestões sobre como gerenciar a retenção. 
    
- Por padrão, o tamanho máximo de mensagens que podem ser recebidas por uma caixa de correio do Office 365 é de 35 MB. Isso ocorre porque o valor padrão para a propriedade *MaxReceiveSize* de uma caixa de correio é definido como 35 MB. No enTanto, o limite do tamanho máximo de recebimento de mensagens no Office 365 é de 150 MB. Portanto, se você importar um arquivo PST que contenha um item maior do que 35 MB, o serviço de importação do Office 365 alteraremos automaticamente o valor da propriedade *MaxReceiveSize* na caixa de correio de destino para 150 MB. Isso permite que as mensagens até 150 MB sejam importadas para as caixas de correio do usuário. 
    
    > [!TIP]
    > Para identificar o tamanho de recebimento da mensagem de uma caixa de correio, você pode executar este comando no `Get-Mailbox <user mailbox> | FL MaxReceiveSize`PowerShell do Exchange Online:. 

## <a name="step-1-copy-the-sas-url-and-install-azure-azcopy"></a>Etapa 1: copiar a URL SAS e instalar o Azure AzCopy

A primeira etapa é baixar e instalar a ferramenta AzCopy do Microsoft Azure, que é a ferramenta que você executará na etapa 2 para carregar os arquivos PST para o Office 365. Você também copiará a URL SAS de sua organização. Esta URL é uma combinação da URL de rede para o local de armazenamento do Azure na nuvem da Microsoft para sua organização e uma chave de assinatura de acesso compartilhado (SAS). Essa chave fornece as permissões necessárias para carregar os arquivos PST para seu local de armazenamento do Azure. Certifique-se de ter precauções para proteger a URL SAS. É exclusivo da sua organização e será usado na etapa 2.

> [!IMPORTANT]
> Para importar arquivos PST usando o método de carregamento de rede, recomendamos que você use a versão do Azure AzCopy que pode ser baixada na etapa 6B no procedimento a seguir.
  
1. AcEsse [https://protection.office.com](https://protection.office.com) e entre usando as credenciais de uma conta de administrador na sua organização do Office 365. 
    
2. No painel esquerdo do centro de conformidade do & de segurança, clique em **importação**de **governança** \> de dados.
    
    > [!NOTE]
    > Você precisa receber as permissões apropriadas para acessar a página de **importação** no centro de conformidade do _AMP_ de segurança. Consulte a seção **antes de começar** para obter mais informações. 
    
3. Na página **importar** , clique em ![adicionar ícone](media/ITPro-EAC-AddIcon.gif) **novo trabalho de importação**.
    
    O assistente de importação de trabalho é exibido.
    
4. Digite um nome para o trabalho de importação de PST e clique em **Avançar**. Use letras minúsculas, números, hifens e sublinhados. Não é possível usar letras maiúsculas ou incluir espaços no nome.
    
5. Na página **deseja carregar ou enviar dados?** , clique em **carregar seus dados** e, em seguida, clique em **Avançar**.
    
    ![Clique em carregar seus dados para criar um trabalho de importação de carregamento de rede](media/e59f9dc3-ccde-44ff-ac38-c4e39d76ae85.png)
  
6. Na página **importar dados** , faça o seguinte: 
    
    ![Copie a URL SAS e baixe a ferramenta AzCopy do Azure na página Importar dados](media/74411014-ec4b-4e25-9065-404c934cce17.png)
  
    a. Na etapa 2, clique em **Mostrar URL SAS de carregamento de rede**. Depois que a URL SAS for exibida, clique em **copiar para área de transferência** e cole-a e salve-a em um arquivo para que você possa acessá-la mais tarde.
    
    b. Na etapa 3, clique em **baixar o Azure AzCopy** para baixar e instalar a ferramenta AzCopy do Azure. Na janela pop-up, clique em **executar** para instalar o AzCopy. 
    
> [!NOTE]
> Você pode deixar a página **importar dados** aberta (caso precise copiar a URL SAS novamente) ou clicar em **Cancelar** para fechá-la. 
 
## <a name="step-2-upload-your-pst-files-to-office-365"></a>Etapa 2: carregar os arquivos PST no Office 365

Agora você está pronto para usar a ferramenta AzCopy. exe para carregar arquivos PST para o Office 365. Essa ferramenta carrega e armazena-as em um local de armazenamento do Azure na nuvem da Microsoft. Como explicado anteriormente, o local de armazenamento do Azure para o qual você carrega seus arquivos PST reside no mesmo datacenter regional da Microsoft onde sua organização do Office 365 está localizada. Para concluir essa etapa, você deve colocar os arquivos PST em um compartilhamento de arquivos ou servidor de arquivos da organização. Esse local é conhecido como diretório de origem no procedimento a seguir. Cada vez que você executa a ferramenta AzCopy, é possível especificar um diretório de origem diferente. 
  
1. Abra um prompt de comando no computador local.
    
2. Vá para o diretório onde você instalou a ferramenta AzCopy. exe na etapa 1. Se você instalou a ferramenta no local padrão, vá para `%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy`.
    
3. Execute o seguinte comando para carregar os arquivos PST no Office 365.

    ```
    AzCopy.exe /Source:<Location of PST files> /Dest:<SAS URL> /V:<Log file location> /Y
  
    ```
 
    > [!IMPORTANT] 
    > Você deve especificar um diretório como o local de origem no comando anterior; Você não pode especificar um arquivo PST individual. Todos os arquivos PST no diretório de origem serão carregados.
 
    A tabela a seguir descreve os parâmetros AzCopy. exe e seus valores necessários. As informações obtidas na etapa anterior são usadas nos valores desses parâmetros.
    
    |**Parâmetro**|**Descrição**|**Exemplo**|
    |:-----|:-----|:-----|
    | `/Source:` <br/> |Especifica o diretório de origem em sua organização que contém os arquivos PST que serão carregados no Office 365.  <br/> Não deixe de colocar o valor deste parâmetro entre aspas duplas (" ").  <br/> | `/Source:"\\FILESERVER01\PSTs"` <br/> |
    | `/Dest:` <br/> |Especifica a URL SAS obtida na etapa 1.  <br/> Não deixe de colocar o valor deste parâmetro entre aspas duplas (" ").  <br/> **Dica:** Opcion Você pode especificar uma subpasta no local de armazenamento do Azure para carregar os arquivos PST. Para fazer isso, adicione um local de subpasta (após "ingestiondata") na URL SAS. O primeiro exemplo não especifica uma subpasta; Isso significa que os PSTs serão carregados para a raiz (chamada *ingestiondata* ) do local de armazenamento do Azure. O segundo exemplo carrega os arquivos PST em uma subpasta (chamada *PSTFiles* ) na raiz do local de armazenamento do Azure.  <br/> | `/Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"` <br/> Ou  <br/>  `/Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata/PSTFiles?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"` <br/> |
    | `/V:` <br/> |Gera mensagens de status detalhadas em um arquivo de log. Por padrão, o arquivo de log detalhado é chamado AzCopyVerbose. log no%LocalAppData%\Microsoft\Azure\AzCopy. Se você especificar um local de arquivo existente para essa opção, o log detalhado será acrescentado a esse arquivo.  <br/> Não deixe de colocar o valor deste parâmetro entre aspas duplas (" ").  <br/> | `/V:"c:\Users\Admin\Desktop\Uploadlog.log"` <br/> |
    | `/S` <br/> |Essa opção opcional especifica o modo recursivo para que a ferramenta AzCopy Copie arquivos PSTs localizados em subpastas no diretório de origem especificado pelo `/Source:` parâmetro.  <br/> **Observação:** Se você incluir essa opção, os arquivos PST em subpastas terão um nome de caminho de arquivo diferente no local de armazenamento do Azure após serem carregados. Você precisará especificar o nome de caminho do arquivo exato no arquivo CSV criado na etapa 4.  <br/> | `/S` <br/> |
    | `/Y` <br/> |Essa opção obrigatória permite o uso de tokens de SAS somente gravação quando você carrega os arquivos PST no local de armazenamento do Azure. A URL SAS obtida na etapa 1 (e especificada em `/Dest:` Parameter) é uma URL SAS somente gravação, que é o motivo pelo qual você deve incluir essa opção. Observe que uma URL SAS somente gravação não impedirá que você use o explorador de armazenamento do Azure para exibir uma lista dos arquivos PST carregados para o local de armazenamento do Azure.  <br/> | `/Y` <br/> |
   
Veja um exemplo da sintaxe para a ferramenta AzCopy. exe usando valores reais para cada parâmetro:
    
```
  AzCopy.exe /Source:"\\FILESERVER1\PSTs" /Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D" /V:"c:\Users\Admin\Desktop\AzCopy1.log" /Y
  
```

Depois de executar o comando, as mensagens de status são exibidas, mostrando o progresso do carregamento dos arquivos PST. Uma mensagem de status final mostra o número total de arquivos que foram carregados com êxito.

> [!TIP]
> Depois de executar o comando AzCopy. exe com êxito e verificar se todos os parâmetros estão corretos, salve uma cópia da sintaxe da linha de comando no mesmo arquivo (protegido) onde você copiou as informações obtidas na etapa 1. Em seguida, você pode copiar e colar este comando em um prompt de comando sempre que desejar executar a ferramenta AzCopy. exe para carregar arquivos PST para o Office 365. O único valor que você pode ter de alterar são os para o `/Source:` parâmetro. Depende do diretório de origem em que os arquivos PST estão localizados.

## <a name="optional-step-3-view-a-list-of-the-pst-files-uploaded-to-office-365"></a>Opcion Etapa 3: exibir uma lista dos arquivos PST carregados para o Office 365

Como uma etapa opcional, você pode instalar e usar o Microsoft Azure Storage Explorer (que é uma ferramenta de código aberto gratuita) para exibir a lista dos arquivos PST que você carregou para o blob do Azure. Há dois bons motivos para fazer isso:
  
- Verifique se os arquivos PST da pasta compartilhada ou do servidor de arquivos em sua organização foram carregados com êxito para o blob do Azure.
    
- Verifique o nome de arquivo (e o nome de caminho da subpasta se você incluiu uma) para cada arquivo PST carregado no blob do Azure. Isso é realmente útil quando você está criando o arquivo de mapeamento de PST na próxima etapa, porque você precisa especificar o nome de caminho e o nome de arquivo da pasta para cada arquivo PST. A verificação desses nomes pode ajudar a reduzir possíveis erros no arquivo de mapeamento de PST.
    
O Microsoft Azure Storage Explorer está em versão prévia.
  
> [!IMPORTANT]
> Você não pode usar o Gerenciador de armazenamento do Azure para carregar ou modificar arquivos PST. O único método com suporte para importar arquivos PST para o Office 365 é usar o AzCopy. Além disso, não é possível excluir arquivos PST que você carregou para o blob do Azure. Se tentar excluir um arquivo PST, receberá um erro informando que você não tem as permissões necessárias. Observe que todos os arquivos PST são excluídos automaticamente de sua área de armazenamento do Azure. If there are no import jobs in progress, then all PST files in the **ingestiondata** container are deleted 30 days after the most recent import job was created.
  
Para instalar o Azure Storage Explorer e se conectar à sua área de armazenamento do Azure:
  
1. Baixe e instale a [ferramenta Microsoft Azure Storage Explorer](https://go.microsoft.com/fwlink/p/?LinkId=544842).
    
2. Inicie o Gerenciador de armazenamento do Microsoft Azure, clique com o botão direito do mouse em **contas de armazenamento** no painel esquerdo e, em seguida, clique em **conectar ao armazenamento do Azure**.
    
    ![Clique com o botão direito do mouse em contas de armazenamento e clique em conectar ao armazenamento do Azure](media/75b80cc3-c336-4f96-ad32-54ac9b96a7af.png)
  
3. Clique em **usar um URI ou uma cadeia de conexão de assinatura de acesso compartilhado (SAS)** e clique em **Avançar**.
    
4. Clique em **usar um URI SAS**, Cole a URL SAS obtida na etapa 1 na caixa em **URI**e clique em **Avançar**.
    
5. Na página **Resumo da conexão** , você pode revisar as informações de conexão e clique em **conectar**.
    
    O contêiner **ingestiondata** é aberto; Ele contém os arquivos PST que você carregou na etapa 2. O contêiner **ingestiondata** está localizado em contêineres de **blob**de **contas** \> **de armazenamento (serviços anexados por SAS)** \> . 
    
    ![O Azure Storage Explorer exibe uma lista dos arquivos PST que você carregou](media/12376fed-13a5-4a09-8fe6-e819e011b334.png)
  
6. Quando você terminar de usar o Microsoft Azure Storage Explorer, clique com o botão direito do mouse em **ingestiondata**e clique em Desanexar para desconectar da sua área de armazenamento do Azure. **** Caso contrário, você receberá um erro na próxima vez que tentar anexar. 
    
    ![Clique com o botão direito em inclusão e clique em Desconectar para desconectar da sua área de armazenamento do Azure](media/1e8e5e95-4215-4ce4-a13d-ab5f826a0510.png)
  
## <a name="step-4-create-the-pst-import-mapping-file"></a>Etapa 4: criar o arquivo de mapeamento de importação de PST

Após o carregamento dos arquivos PST para o local de armazenamento do Azure para sua organização do Office 365, a próxima etapa é criar um arquivo CSV (valor separado por vírgula) que especifica quais caixas de correio de usuário serão importadas. Você enviará esse arquivo CSV na próxima etapa ao criar um trabalho de importação de PST.
  
1. [Baixe uma cópia do arquivo de mapeamento de importação de PST](https://go.microsoft.com/fwlink/p/?LinkId=544717).
    
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

   **Observação:** Não altere nada na linha de cabeçalho, incluindo os parâmetros do SharePoint; Eles serão ignorados durante o processo de importação de PST. 

 3. Use as informações da tabela a seguir para preencher o arquivo CSV com as informações necessárias.


    |**Parâmetro**|**Descrição**|**Exemplo**|
    |:-----|:-----|:-----|
    | `Workload` <br/> |Especifica o serviço do Office 365 para o qual os dados serão importados. Para importar arquivos PST para caixas de correio de usuário `Exchange`, use.  <br/> | `Exchange` <br/> |
    | `FilePath` <br/> |Especifica o local da pasta no local de armazenamento do Azure em que você carregou os arquivos PST na etapa 2.  <br/> Se você não incluir um nome de subpasta opcional na URL SAS no `/Dest:` parâmetro da etapa 2, deixe esse parâmetro em branco no arquivo CSV. Se você tiver incluído um nome de subpasta, especifique-o nesse parâmetro (consulte o segundo exemplo). O valor desse parâmetro diferencia maiúsculas de minúsculas.  <br/> De qualquer forma, *não* inclua "ingestiondata" no valor para o `FilePath` parâmetro.  <br/><br/> **Importante:** O caso do nome do caminho do arquivo deve ser o mesmo que o caso usado se você tiver incluído um nome de subpasta opcional na URL SAS `/Dest:` no parâmetro da etapa 2. Por exemplo, se você usou `PSTFiles` para o nome da subpasta na etapa 2 e `pstfiles` usar no `FilePath` parâmetro no arquivo CSV, a importação do arquivo PST falhará. Certifique-se de usar o mesmo caso em ambas as instâncias.  <br/> |(deixar em branco)  <br/> Ou  <br/>  `PSTFiles` <br/> |
    | `Name` <br/> |Especifica o nome do arquivo PST que será importado para a caixa de correio do usuário.  O valor desse parâmetro diferencia maiúsculas de minúsculas.  <br/> <br/>**Importante:** O caso do nome de arquivo PST no arquivo CSV deve ser igual ao arquivo PST que foi carregado no local de armazenamento do Azure na etapa 2. Por exemplo, se você usar `annb.pst` no `Name` parâmetro no arquivo CSV, mas o nome do arquivo PST real for `AnnB.pst`, a importação desse arquivo PST falhará. Certifique-se de que o nome do PST no arquivo CSV use o mesmo caso do arquivo PST real.  <br/> | `annb.pst` <br/> |
    | `Mailbox` <br/> |Especifica o endereço de email da caixa de correio para a qual o arquivo PST será importado.  Observe que não é possível especificar uma pasta pública porque o Serviço de Importação de PST não tem suporte com a importação de arquivos PST para pastas públicas.  <br/> Para importar um arquivo PST para uma caixa de correio inativa, você precisa especificar o GUID da caixa de correio para esse parâmetro. Para obter esse GUID, execute o seguinte comando do PowerShell no Exchange Online:`Get-Mailbox <identity of inactive mailbox> -InactiveMailboxOnly | FL Guid` <br/> <br/>**Observação:** Em alguns casos, você pode ter várias caixas de correio com o mesmo endereço de email, em que uma caixa de correio está ativa e a outra caixa de correio está em um estado de exclusão reversível (ou inativa). Nessas situações, você precisa especificar o GUID da caixa de correio para identificar exclusivamente a caixa de correio para a qual importar o arquivo PST. Para obter esse GUID para caixas de correio ativas, execute o seguinte comando `Get-Mailbox <identity of active mailbox> | FL Guid`do PowerShell:. Para obter o GUID das caixas de correio excluídas por software (ou inativo), execute `Get-Mailbox <identity of soft-deleted or inactive mailbox> -SoftDeletedMailbox | FL Guid`este comando.  <br/> | `annb@contoso.onmicrosoft.com` <br/> Ou  <br/>  `2d7a87fe-d6a2-40cc-8aff-1ebea80d4ae7` <br/> |
    | `IsArchive` <br/> | Especifica se deve ou não importar o arquivo PST para a caixa de correio de arquivo morto do usuário. Há duas opções:  <br/><br/>**False** -importa o arquivo PST para a caixa de correio principal do usuário.  <br/> **True** -importa o arquivo PST para a caixa de correio de arquivo morto do usuário. This assumes that the [user's archive mailbox is enabled](enable-archive-mailboxes.md). <br/><br/>Se você definir esse parâmetro como `TRUE` e a caixa de correio de arquivo morto do usuário não estiver habilitada, a importação desse usuário falhará. Observe que, se uma importação falhar para um usuário (porque seu arquivo morto não está habilitado e essa propriedade `TRUE`for definida como), os outros usuários no trabalho de importação não serão afetados.  <br/>  If you leave this parameter blank, the PST file is imported to the user's primary mailbox.  <br/> <br/>**Observação:** Para importar um arquivo PST para uma caixa de correio de arquivo morto baseado na nuvem para um usuário cuja caixa de correio principal esteja `TRUE` no local, basta especificar para esse parâmetro e especificar o endereço de email da caixa de correio `Mailbox` local do usuário para o parâmetro.  <br/> | `FALSE` <br/> Ou  <br/>  `TRUE` <br/> |
    | `TargetRootFolder` <br/> | Especifica a pasta de caixa de correio para a qual o arquivo PST será importado.  <br/>  Se você deixar esse parâmetro em branco, o PST será importado para uma nova **** pasta denominaDa importada localizada no nível raiz da caixa de correio (o mesmo nível que a pasta caixa de entrada e as outras pastas de caixa de correio padrão).  <br/>  Se você especificar `/`, os itens no arquivo PST serão importados diretamente para a pasta caixa de entrada do usuário.  <br/><br/>  Se você especificar `/<foldername>`, os itens no arquivo PST serão importados para uma pasta denominada * \<\> FolderName* . Por exemplo, se você usar `/ImportedPst`, os itens serão importados para uma pasta chamada **ImportedPst**. Essa pasta estará localizada na caixa de correio do usuário no mesmo nível da pasta caixa de entrada.  <br/><br/> **Dica:** Considere a execução de alguns lotes de teste para experimentar esse parâmetro para que você possa determinar o melhor local da pasta para importar arquivos PSTs.  <br/> |(deixar em branco)  <br/> Ou  <br/>  `/` <br/> Ou  <br/>  `/ImportedPst` <br/> |
    | `ContentCodePage` <br/> |Este parâmetro opcional especifica um valor numérico para a página de código a ser usado para importar arquivos PST no formato de arquivo ANSI. Esse parâmetro é usado para importar arquivos PST de organizações chinesas, japonesas e coreanas (CJK), pois esses idiomas normalmente usam um DBCS (conjunto de caracteres de dois bytes) para codificação de caracteres. Se esse parâmetro não for usado para importar arquivos PST para idiomas que usam DBCS para nomes de pastas de caixa de correio, os nomes das pastas freqüentemente serão truncados após serem importados.  <br/><br/> Para obter uma lista de valores com suporte para usar esse parâmetro, confira identificadores de [página de código](https://go.microsoft.com/fwlink/p/?LinkId=328514).  <br/> <br/>**Observação:** Como mencionado anteriormente, este é um parâmetro opcional e você não precisa incluí-lo no arquivo CSV. Ou você pode incluí-lo e deixar o valor em branco para uma ou mais linhas.  <br/> |(deixar em branco)  <br/> Ou  <br/>  `932`(que é o identificador da página de código para ANSI/OEM japonês)  <br/> |
    | `SPFileContainer` <br/> |Deixe este parâmetro em branco para Importação de PST.   <br/> |Não aplicável  <br/> |
    | `SPManifestContainer` <br/> |Deixe este parâmetro em branco para Importação de PST.   <br/> |Não aplicável  <br/> |
    | `SPSiteUrl` <br/> |Deixe este parâmetro em branco para Importação de PST.   <br/> |Não aplicável  <br/> |

## <a name="step-5-create-a-pst-import-job-in-office-365"></a>Etapa 5: criar um trabalho de importação de PST no Office 365

A próxima etapa é criar o trabalho de importação de PST no serviço de importação do Office 365. Como explicado anteriormente, você enviará o arquivo de mapeamento de importação de PST criado na etapa 4. Depois de criar o novo trabalho, o Office 365 analisa os dados nos arquivos PST e dá a você uma oportunidade de filtrar os dados que realmente são importados para as caixas de correio especificadas no arquivo de mapeamento de importação de PST (consulte a [etapa 6](#step-6-filter-data-and-start-the-pst-import-job)).
  
1. AcEsse [https://protection.office.com](https://protection.office.com) e entre usando as credenciais de uma conta de administrador na sua organização do Office 365. 
    
2. No painel esquerdo do centro de conformidade do & de segurança, clique em **governança de dados** e, em seguida, clique em **importar**.
    
3. Na página **importar** , clique em ![adicionar ícone](media/ITPro-EAC-AddIcon.gif) **novo trabalho de importação**.
    
    **Observação:** Você precisa receber as permissões apropriadas para acessar a página **importar** no centro de conformidade do _AMP_ de segurança para criar um novo trabalho de importação. Consulte a seção **antes de começar** para obter mais informações. 
    
4. Digite um nome para o trabalho de importação de PST e clique em **Avançar**. Use letras minúsculas, números, hifens e sublinhados. Não é possível usar letras maiúsculas ou incluir espaços no nome.
    
5. Na página **deseja carregar ou enviar dados?** , clique em **carregar seus dados** e, em seguida, clique em **Avançar**.
    
    ![Clique em carregar seus dados para criar um trabalho de importação de carregamento de rede](media/e59f9dc3-ccde-44ff-ac38-c4e39d76ae85.png)
  
6. Na etapa 4 da página **importar dados** , clique na caixa de seleção Estou **pronto para carregar meus arquivos** e tenho **acesso ao arquivo de mapeamento** e, em seguida, clique em **Avançar**.
    
    ![Clique nas duas caixas de seleção na etapa 4](media/9f2427e8-3af2-4e27-95e6-a9f08430d3d8.png)
  
7. Na página **selecionar o arquivo de mapeamento** , clique em **Selecionar arquivo de mapeamento** para enviar o arquivo de mapeamento de importação de PST que você criou na etapa 4. 
    
    ![Clique em Selecionar arquivo de mapeamento para enviar o arquivo CSV que você criou para o trabalho de importação](media/d30b1d73-80bb-491e-a642-a21673d06889.png)
  
8. Depois que o nome do arquivo CSV aparecer em **nome do arquivo de mapeamento**, clique em **validar** para verificar se há erros no arquivo CSV. 
    
    ![Clique em validar para verificar se há erros no arquivo CSV](media/4680999d-5538-4059-b878-2736a5445037.png)
  
    Você deve validar o arquivo CSV com êxito para poder criar um trabalho de Importação de PST. Observação o nome do arquivo é alterado para verde depois de ser validado com êxito. Se a validação falhar, clique no link **Exibir log** . Um relatório de erro de validação é aberto, com uma mensagem de erro para cada linha no arquivo que falhou. 
    
9. Depois que o arquivo de mapeamento de PST for validado com êxito, leia o documento termos e condições e clique na caixa de seleção.
    
10. Clique em **salvar** para enviar o trabalho e clique em **fechar** após o trabalho ter sido criado com êxito. 
    
    Uma página de submenu de status é exibida, com o status de **análise em andamento** e o novo trabalho de importação é exibido na lista da página de **importação** . 
    
11. Clique em **Atualizar** ![ícone](media/O365-MDM-Policy-RefreshIcon.gif) de atualização para atualizar as informações de status exibidas na coluna **status** . Quando a análise é concluída e os dados estão prontos para serem importados, o status é alterado para **análise concluída**.
    
    Você pode clicar no trabalho de importação para exibir a página de submenu de status, que contém informações mais detalhadas sobre o trabalho de importação, como o status de cada arquivo PST listado no arquivo de mapeamento.
 
## <a name="step-6-filter-data-and-start-the-pst-import-job"></a>Etapa 6: filtrar os dados e iniciar o trabalho de importação de PST

Depois de criar o trabalho de importação na etapa 5, o Office 365 analisa os dados nos arquivos PST (de uma maneira segura e segura) identificando a idade dos itens e os diferentes tipos de mensagem incluídos nos arquivos PST. Quando a análise é concluída e os dados estão prontos para importação, você tem a opção de importar todos os dados contidos nos arquivos PST ou pode aparar os dados que são importados por meio da definição de filtros que controlam quais dados são importados.
  
1. Na página **importar** no centro de conformidade do _AMP_ de segurança, clique em **pronto para importar para o Office 365** para o trabalho de importação que você criou na etapa 5. 
    
    ![Clique em pronto para importar para o Office 365 ao lado do trabalho de importação criado](media/5760aac3-300b-4e31-b894-253c42a4b82b.png)
  
    Uma página de sobrevôo é exibida com informações sobre os arquivos PST e outras informações sobre o trabalho de importação.
    
2. Na página do menu suspenso, clique em **importar para o Office 365**.
    
    O **filtro em que sua página de dados** é exibida. Ele contém as insights de dados resultantes da análise realizada nos arquivos PST pelo Office 365, incluindo informações sobre a idade dos dados. Neste ponto, você tem a opção de filtrar os dados que serão importados ou importar todos os dados como estão. 
    
    ![Você pode aparar os dados nos arquivos PST ou importá-los](media/287fc030-99e9-417b-ace7-f64617ea5d4e.png)
  
3. Siga um destes procedimentos:
    
    a. Para aparar os dados que você importou, clique em **Sim, quero filtrá-lo antes de importar**.
    
    Para obter instruções passo a passo detalhadas sobre como filtrar os dados nos arquivos PST e, em seguida, iniciar o trabalho de importação, consulte [Filter data ao importar arquivos pst para o Office 365](filter-data-when-importing-pst-files.md).
    
    Ou
    
    b. Para importar todos os dados dos arquivos PST, clique em **não, desejo importar tudo** e clique em **Avançar**.
    
4. Se você optar por importar todos os dados, clique em **importar dados** para iniciar o trabalho de importação. 
    
    O status do trabalho de importação é exibido na página de **importação** . Clique ![em atualizar](media/O365-MDM-Policy-RefreshIcon.gif) ícone **Atualizar** para atualizar as informações de status exibidas na coluna **status** . Clique no trabalho de importação para exibir a página de submenu de status, que exibe informações de status sobre cada arquivo PST que está sendo importado. 

## <a name="how-the-import-process-works"></a>Como funciona o processo de importação
  
Você pode usar a opção de carregamento de rede e o serviço de importação do Office 365 para importar arquivos PST em massa para caixas de correio do usuário. O carregamento de rede significa que você carrega os arquivos PST uma área de armazenamento temporária na nuvem da Microsoft. Em seguida, o serviço de importação do Office 365 copia os arquivos PST da área de armazenamento para as caixas de correio do usuário de destino.
  
Aqui está uma ilustração e uma descrição do processo de carregamento de rede para importar arquivos PST para caixas de correio no Office 365.
  
![Fluxo de trabalho do processo de carregamento de rede para importar arquivos PST para o Office 365](media/9e05a19e-1e7a-4f1f-82df-9118f51588c4.png)
  
1. **Baixar a ferramenta de importação de PST e a chave para o local privado de armazenamento do Azure** – a primeira etapa é baixar a ferramenta de linha de comando AzCopy do Azure e uma chave de acesso usada para carregar os arquivos pst em um local de armazenamento do Azure na nuvem da Microsoft. Você obtém isso na página **importar** no centro de conformidade do _AMP_ de segurança. A chave (chamada de uma chave de assinatura de acesso seguro (SAS) fornece as permissões necessárias para carregar arquivos PST para um local de armazenamento do Azure privado e seguro. Essa chave de acesso é exclusiva para sua organização e ajuda a impedir o acesso não autorizado aos seus arquivos PST depois que eles são carregados na nuvem da Microsoft. Observe que a importação de arquivos PST para o Office 365 não exige que sua organização tenha uma assinatura separada do Azure. 
    
2. **Carregar os arquivos pst para o local de armazenamento do Azure** – a próxima etapa é usar a ferramenta AzCopy. exe (baixada na etapa 1) para carregar e armazenar seus arquivos pst em um local de armazenamento do Azure que reside no mesmo datacenter regional da Microsoft em que o Office 365 a organização está localizada. Para carregá-los, os arquivos PST que você deseja importar para o Office 365 devem estar localizados em um compartilhamento de arquivo ou servidor de arquivos em sua organização.
    
    Observe que há uma etapa opcional que você pode executar para exibir a lista de arquivos PST depois que eles são carregados no local de armazenamento do Azure.
    
3. **Criar um arquivo de mapeamento de importação de PST** -depois que os arquivos PST tiverem sido carregados no local de armazenamento do Azure, a próxima etapa é criar um arquivo CSV (valor separado por vírgula) que especifica quais caixas de correio de usuários serão importadas, observe que um arquivo PST pode ser  importado para a caixa de correio principal do usuário ou sua caixa de correio de arquivo morto. O serviço de importação do Office 365 usará as informações no arquivo CSV para importar os arquivos PST.
    
4. **Criar um trabalho de importação de PST** -a próxima etapa é criar um trabalho de importação de PST na página **importar** no centro de conformidade do & de segurança e enviar o arquivo de mapeamento de importação de pst criado na etapa anterior. Depois de criar o trabalho de importação, o Office 365 analisa os dados nos arquivos PST e fornece a você uma oportunidade de definir filtros que controlam quais dados são realmente importados para as caixas de correio especificadas no arquivo de mapeamento de importação de PST. 
    
5. **Filtrar os dados de PST que serão importados para caixas de correio** -após a criação e a inicialização do trabalho de importação, o Office 365 analisa os dados nos arquivos PST (com segurança e segurança) identificando a idade dos itens e os diferentes tipos de mensagens incluídos nos arquivos PST . Quando a análise é concluída e os dados estão prontos para importação, você tem a opção de importar todos os dados contidos nos arquivos PST ou pode aparar os dados que são importados por meio da definição de filtros que controlam quais dados são importados.
    
6. **Iniciar o trabalho de importação de PST** -depois que o trabalho de importação for iniciado, o Office 365 usará as informações do arquivo de mapeamento de importação de PST para importar os arquivos PSTs do local de armazenamento do Microsoft Azure para as caixas de correio do usuário. As informações de status sobre o trabalho de importação (incluindo informações sobre cada arquivo PST que está sendo importado) são exibidas na página **importar** no centro de conformidade do _AMP_ de segurança. Quando o trabalho de importação for concluído, o status do trabalho será definido como **concluído**.
  
## <a name="more-information"></a>Mais informações

- Por que importar arquivos PST para o Office 365?
    
  - É uma boa maneira de importar os dados de mensagens de arquivamento da sua organização para o Office 365.
    
  - Os dados ficam disponíveis para o usuário em todos os dispositivos, pois eles são armazenados na nuvem.
    
  - Ele ajuda a atender às necessidades de conformidade da sua organização, permitindo que você aplique recursos de conformidade do Office 365 aos dados dos arquivos PST que você importou. Isso inclui:
    
  - Habilitar [caixas de correio de arquivo morto](enable-archive-mailboxes.md) e arquivamento de [expansão automática](enable-unlimited-archiving.md) para dar aos usuários espaço de armazenamento de caixa de correio adicional para armazenar os dados que você importou. 
    
  - Colocar caixas de correio em [retenção de litígio](https://go.microsoft.com/fwlink/?linkid=856286) para manter os dados que você importou. 
    
  - Usar as [ferramentas de descoberta eletrônica](search-for-content.md) da Microsoft para pesquisar os dados que você importou. 
    
  - Usando [as políticas de retenção do Office 365](retention-policies.md) para controlar por quanto tempo os dados importados serão mantidos e a ação a ser tomada depois que o período de retenção expira. 
    
  - Pesquisando o [log de auditoria do Office 365](search-the-audit-log-in-security-and-compliance.md) para eventos relacionados à caixa de correio que afetam os dados que você importou. 
    
  - Importar dados para [caixas de correio](create-and-manage-inactive-mailboxes.md) inativas para arquivar dados para fins de conformidade. 
    
  - Usando [as políticas de prevenção contra perda de dados](data-loss-prevention-policies.md) para evitar que dados confidenciais entrem fora da sua organização. 
  
- Veja um exemplo da URL de assinatura de acesso compartilhado (SAS) obtida na etapa 1. Este exemplo também contém a sintaxe do comando executado na ferramenta AzCopy. exe para carregar arquivos PST para o Office 365. Certifique-se de ter precauções para proteger a URL SAS da mesma forma que você protegeria senhas ou outras informações relacionadas à segurança.

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
    

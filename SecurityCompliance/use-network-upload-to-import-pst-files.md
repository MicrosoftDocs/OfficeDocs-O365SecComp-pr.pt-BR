---
title: Use o carregamento de rede para importar seus arquivos PST da organização para o Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 103f940c-0468-4e1a-b527-cc8ad13a5ea6
description: 'Para administradores: Saiba como usar o carregamento de rede para vários arquivos PST às caixas de correio do usuário no Office 365 importação em massa.'
ms.openlocfilehash: 81c799a8c820e9d9287f4792fe463d6a99b90e36
ms.sourcegitcommit: 25f1028643d8a20d17306e8b09cafea46eaf7a58
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/31/2019
ms.locfileid: "29666151"
---
# <a name="use-network-upload-to-import-your-organization-pst-files-to-office-365"></a>Use o carregamento de rede para importar seus arquivos PST da organização para o Office 365

> [!NOTE]
> Este artigo destina-se a administradores. Você está tentando importar arquivos PST para sua própria caixa de correio? Consulte o [email de importação, contatos e calendário de um arquivo. pst do Outlook](https://go.microsoft.com/fwlink/p/?LinkID=785075)
  
Aqui estão as instruções passo a passo necessárias para usar o carregamento de rede para vários arquivos PST às caixas de correio do Office 365 importação em massa. Para perguntas frequentes sobre como usar o carregamento de rede para importação em massa de arquivos PST às caixas de correio do Office 365, consulte as [Perguntas frequentes para usar o carregamento de rede para importar arquivos PST](faqimporting-pst-files-to-office-365.md#using-network-upload-to-import-pst-files).
  
[Etapa 1: Copie a URL de SAS e instalar o Windows Azure AzCopy](#step-1-copy-the-sas-url-and-install-azure-azcopy)

[Etapa 2: Atualizar seus arquivos PST para o Office 365](#step-2-upload-your-pst-files-to-office-365)

[(Opcional) Etapa 3: Exibir uma lista dos arquivos PST carregados para o Office 365](#optional-step-3-view-a-list-of-the-pst-files-uploaded-to-office-365)

[Etapa 4: Criar o arquivo de mapeamento de importação de PST](#step-4-create-the-pst-import-mapping-file)

[Etapa 5: criar um trabalho de Importação de PST no Office 365](#step-5-create-a-pst-import-job-in-office-365)

[Etapa 6: Filtrar dados e iniciar o trabalho de importação de PST](#step-6-filter-data-and-start-the-pst-import-job)

Observe que você deve executar a etapa 1 somente uma vez para importar arquivos PST para caixas de correio do Office 365. Depois de executar estas etapas, siga a etapa 2, a etapa 6 sempre que você deseja carregar e importa um lote de arquivos PST.

## <a name="before-you-begin"></a>Antes de começar
  
- Você precisa ter a função caixa de correio importar exportar no Exchange Online para importar arquivos PST para caixas de correio do Office 365. Por padrão, essa função não é atribuída a nenhum grupo de função no Exchange Online. Você pode adicionar a função caixa de correio importar e exportar para o grupo de funções de gerenciamento da organização. Ou você pode criar um novo grupo de função, atribua a função caixa de correio importar e exportar e, em seguida, adicione si mesmo como membro. Para obter mais informações, consulte "Adicionar uma função para um grupo de funções" ou "Criar um grupo de funções" seções em [Gerenciar grupos de função](https://go.microsoft.com/fwlink/p/?LinkId=730688).
    
    Além disso criar a importação de trabalhos no Office 365 Security &amp; Centro de conformidade, uma das opções a seguir devem ser verdadeiro:
    
  - Você precisa ter a função de destinatários de email no Exchange Online. Por padrão, essa função é atribuída aos grupos de funções de gerenciamento de destinatário e gerenciamento da organização.
    
    Ou
    
  - Você precisa ser um administrador global na sua organização do Office 365.
    
  > [!TIP]
    > Considere a criação de um novo grupo de função no Exchange Online que destina-se especificamente para importar arquivos PST para o Office 365. Para o nível mínimo de privilégios necessários para importar arquivos PST, atribua as funções de caixa de correio importar exportar e destinatários de email para o novo grupo de função e, em seguida, adicionar membros. 
  
- O único método suportado para importar arquivos PST para o Office 365 é usar a ferramenta AzCopy do Azure, conforme descrito neste tópico. Você não pode usar o Gerenciador de armazenamento do Windows Azure para carregar arquivos PST diretamente para a área de armazenamento do Azure.
    
- Você precisa armazenar os arquivos PST que você deseja importar para o Office 365 em um servidor de arquivo ou a pasta compartilhada em sua organização. Na etapa 2, você executará a ferramenta Windows Azure AzCopy carregará os arquivos PST que são armazenados neste servidor de arquivo ou pasta para o Office 365 compartilhada.
    
- Esse procedimento envolve copiar e salvar uma cópia de uma URL que contém uma chave de acesso. Essas informações serão usadas na etapa 2 para carregar os arquivos PST e, na etapa 3 se você quiser exibir uma lista dos arquivos PST carregados para o Office 365. Certifique-se de que tome precauções para proteger essa URL como você faria proteger senhas ou outras informações relacionadas à segurança. Por exemplo, você pode salvá-lo a um documento do Microsoft Word protegido por senha ou para uma unidade USB criptografada. Consulte que a seção de [informações adicionais](#more-information) para obter um exemplo disso combinados URL e a chave. 
    
- Você pode importar arquivos PST para uma caixa de correio inativa no Office 365. Você pode fazer isso, especificando o GUID da caixa de correio inativa no `Mailbox` parâmetro no arquivo de mapeamento de importação de PST. Na guia **instruções** neste tópico para obter informações, consulte a etapa 4. 
    
- Em uma implantação híbrida do Exchange, você pode importar arquivos PST, uma caixa de correio de arquivamento baseado em nuvem para um usuário cuja caixa de correio primária está no local. Você pode fazer isso fazendo o seguinte no arquivo de mapeamento de importação de PST:
    
  - Especifique o endereço de email para a caixa de correio do usuário local no `Mailbox` parâmetro. 
    
  - Especificar o valor **TRUE** no `IsArchive` parâmetro. 
    
    Para obter mais informações, consulte a [etapa 4](#step-4-create-the-pst-import-mapping-file) . 
    
- Depois que os arquivos PST são importados para uma caixa de correio do Office 365, a configuração da caixa de correio de retenção é ativada por um período indefinido. Isso significa que a política de retenção atribuída à caixa de correio não será processada até que você desative o status em retenção ou definir uma data para desativar o bloqueio. Por que fazemos isso? Se mensagens importadas para uma caixa de correio são antigas, podem ser permanentemente excluídos (purgados) porque seu período de retenção expirou com base nas configurações de retenção configuradas para a caixa de correio. Colocação de caixa de correio em retenção fornecerá o tempo de proprietário da caixa de correio para gerenciar essas mensagens importado recentemente ou dê tempo para alterar as configurações de retenção da caixa de correio. Consulte a guia de **informações mais** neste tópico para obter sugestões sobre como gerenciar a retenção. 
    
- Por padrão, o tamanho de mensagem máximo que pode ser recebido por uma caixa de correio do Office 365 é 35 MB. Isso ocorre porque o valor padrão para a propriedade *MaxReceiveSize* para uma caixa de correio é definido como 35 MB. No entanto, o limite de tamanho de recebimento de mensagem máxima no Office 365 é 150 MB. Portanto, se você importar um arquivo PST que contém um item mais de 35 MB, o serviço Office 365 importar podemos automaticamente será alterado o valor da propriedade *MaxReceiveSize* na caixa de correio de destino para 150 MB. Isso permite que mensagens até 150 MB a ser importado para caixas de correio do usuário. 
    
    > [!TIP]
    > Para identificar a mensagem de tamanho de recebimento para uma caixa de correio, você pode executar esse comando no PowerShell do Exchange Online: `Get-Mailbox <user mailbox> | FL MaxReceiveSize`. 

## <a name="step-1-copy-the-sas-url-and-install-azure-azcopy"></a>Etapa 1: Copie a URL de SAS e instalar o Windows Azure AzCopy

A primeira etapa é baixar e instalar a ferramenta de AzCopy do Windows Azure, que é a ferramenta que você executará na etapa 2 para carregar os arquivos PST para o Office 365. Você também vai copiar a URL SAS para sua organização. Essa URL é uma combinação da URL de rede para o local de armazenamento do Azure em nuvem da Microsoft para sua organização e uma chave de assinatura de acesso compartilhado (SAS). Essa chave fornece as permissões necessárias para carregar arquivos PST para o seu local de armazenamento do Azure. Certifique-se de que tome precauções para proteger a URL SAS. Ele é exclusivo para a sua organização e será usado na etapa 2.

> [!IMPORTANT]
> Para importar PST método de upload de arquivos usando a rede, recomendamos que você use a versão do Windows Azure AzCopy que pode ser baixada na etapa 6b no procedimento a seguir.
  
1. Vá para [https://protection.office.com](https://protection.office.com) e entrar usando as credenciais para uma conta de administrador em sua organização do Office 365. 
    
2. No painel à esquerda da segurança &amp; Centro de conformidade, clique em **Governança dados** \> **importação**.
    
    > [!NOTE]
    > Você precisa ter as permissões apropriadas para acessar a página de **importação** na segurança &amp; Centro de conformidade. Consulte a seção **antes de começar** , para obter mais informações. 
    
3. Na página **Importar** , clique em ![ícone Adicionar](media/ITPro-EAC-AddIcon.gif) **novo trabalho de importação**.
    
    O Assistente para importação de trabalho é exibida.
    
4. Digite um nome para o trabalho de importação de PST e, em seguida, clique em **Avançar**. Use letras minúsculas, números, hifens e sublinhados. Você não pode usar letras maiusculas ou incluir espaços no nome de usuário.
    
5. Sobre o **você deseja carregar ou enviar dados?** página, clique em **carregar seus dados** e clique em **Avançar**.
    
    ![Clique em carregar dados para criar um carregamento de rede de trabalho de importação](media/e59f9dc3-ccde-44ff-ac38-c4e39d76ae85.png)
  
6. Na página **Importar dados** , siga estes dois procedimentos: 
    
    ![Copie a URL de SAS e baixar a ferramenta do Azure AzCopy na página Importar dados](media/74411014-ec4b-4e25-9065-404c934cce17.png)
  
    r. na etapa 2, clique em **Mostrar SAS URL de carregamento de rede**. Depois que a URL de SAS for exibida, clique em **Copiar para a área de transferência** e colá-lo e salvá-lo em um arquivo, portanto, você pode acessá-lo mais tarde.
    
    b. na etapa 3, clique em **Baixar AzCopy do Windows Azure** para baixar e instalar a ferramenta de AzCopy do Windows Azure. Na janela pop-up, clique em **Executar** para instalar o AzCopy. 
    
> [!NOTE]
> Você pode deixar página **Importar dados** aberta (caso seja necessário copiar a URL SAS novamente) ou clique em **Cancelar** para fechá-la. 
 
## <a name="step-2-upload-your-pst-files-to-office-365"></a>Etapa 2: Atualizar seus arquivos PST para o Office 365

Agora você está pronto para usar a ferramenta de AzCopy.exe para carregar arquivos PST para o Office 365. Essa ferramenta carrega e armazenando-as em um local de armazenamento do Azure em nuvem da Microsoft. Conforme explicado anteriormente, o local de armazenamento do Azure que você carregar arquivos PST em reside no mesmo datacenter Microsoft regional onde a sua organização do Office 365 está localizada. Para concluir esta etapa, os arquivos PST precisam estar localizado em um compartilhamento de arquivo ou o servidor de arquivos na sua organização. Isso é conhecido como o diretório de origem no procedimento a seguir. Cada vez que você executar a ferramenta AzCopy, você pode especificar um diretório de origem diferente. 
  
1. Abra um prompt de comando no computador local.
    
2. Vá até o diretório onde você instalou a ferramenta AzCopy.exe na etapa 1. Se você instalou a ferramenta no local padrão, vá para `%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy`.
    
3. Execute o seguinte comando para carregar os arquivos PST para o Office 365.

    ```
    AzCopy.exe /Source:<Location of PST files> /Dest:<SAS URL> /V:<Log file location> /Y
  
    ```
 
    A tabela a seguir descreve os parâmetros e seus valores necessários. Observe que as informações que você obteve na etapa anterior são usadas nos valores para esses parâmetros.
    
    |**Parameter**|**Descrição**|**Exemplo**|
    |:-----|:-----|:-----|
    | `/Source:` <br/> |Especifica o diretório de origem em sua organização que contém os arquivos PST que serão carregados para o Office 365.  <br/> Não deixe de colocar o valor deste parâmetro entre aspas duplas (" ").  <br/> | `/Source:"\\FILESERVER01\PSTs"` <br/> |
    | `/Dest:` <br/> |Especifica a URL de SAS obtido na etapa 1.  <br/> Não deixe de colocar o valor deste parâmetro entre aspas duplas (" ").  <br/> **Dica:** (Opcional) Você pode especificar uma subpasta no local para carregar os arquivos PST para armazenamento do Azure. Para fazer isso, adicionando um local de subpasta (após "ingestiondata") na URL SAS. O primeiro exemplo não especifica uma subpasta; Isso significa que o PSTs serão carregados até a raiz (chamada *ingestiondata* ) do local de armazenamento do Azure. O segundo exemplo carrega os arquivos PST para uma subpasta (chamado *PSTFiles* ) na raiz do local de armazenamento do Azure.<br/> | `/Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"` <br/> Ou  <br/>  `/Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata/PSTFiles?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"` <br/> |
    | `/V:` <br/> |Gera mensagens de status detalhadas em um arquivo de log. Por padrão, o arquivo de log detalhado tem o nome AzCopyVerbose.log em % LocalAppData%\Microsoft\Azure\AzCopy. Se você especificar um local de arquivo existente para essa opção, o log detalhado será incluído nesse arquivo.  <br/> Não deixe de colocar o valor deste parâmetro entre aspas duplas (" ").  <br/> | `/V:"c:\Users\Admin\Desktop\Uploadlog.log"` <br/> |
    | `/S` <br/> |Esta opção especifica o modo de recursiva para que a ferramenta de AzCopy copiará arquivos PSTs que estão localizados em subpastas no diretório de origem especificado pelo `/Source:` parâmetro.  <br/> **Observação:** Se você incluir este comutador, arquivos PST em subpastas terá um nome de caminho de arquivo diferente no local de armazenamento do Azure após terem sido carregadas. Você precisará especificar o caminho do arquivo exato no arquivo CSV que você criar na etapa 4.<br/> | `/S` <br/> |
    | `/Y` <br/> |Essa opção necessária permite o uso de tokens SAS somente gravação ao carregar os arquivos PST para o local de armazenamento do Azure. A URL de SAS obtida na etapa 1 (e especificadas no `/Dest:` parâmetro) é uma URL de SAS somente gravação, motivo pelo qual você deve incluir este comutador. Observe que uma URL de SAS somente gravação não impeçam de usar o Gerenciador de armazenamento do Windows Azure para exibir uma lista dos arquivos PST carregados no local de armazenamento do Azure.<br/> | `/Y` <br/> |
   
Veja um exemplo da sintaxe para a ferramenta AzCopy.exe, que usa valores reais para os parâmetros:
    
```
  AzCopy.exe /Source:"\\FILESERVER1\PSTs" /Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D" /V:"c:\Users\Admin\Desktop\AzCopy1.log" /Y
  
```

Depois de executar o comando, o sistema exibe mensagens de status que mostram o andamento do carregamento dos arquivos PST. Uma mensagem de status final mostra o número total de arquivos que foram carregados com êxito. 

> [!TIP]
> Depois de executar o comando AzCopy.exe com êxito e verificar se todos os parâmetros estão corretos, salvar uma cópia da sintaxe da linha de comando para o mesmo arquivo (protegido), onde você copiou as informações obtida na etapa 1. Em seguida, você pode copiar e colar esse comando em um Prompt de comando cada vez que você deseja executar a ferramenta de AzCopy.exe para carregar arquivos PST para o Office 365. O único valor que você pode precisar alterar são aqueles para o `/Source:` parâmetro. Isso depende do diretório de origem onde os arquivos PST estão localizados.

## <a name="optional-step-3-view-a-list-of-the-pst-files-uploaded-to-office-365"></a>(Opcional) Etapa 3: Exibir uma lista dos arquivos PST carregados para o Office 365

Como uma etapa opcional, você pode instalar e usar o Microsoft Azure Storage Explorer (que é uma ferramenta gratuita de código aberto) para exibir a lista dos arquivos PST que tenha carregado para o Azure blob. Existem dois bons motivos para fazer isso:
  
- Verifique se que os arquivos PST na pasta compartilhada ou servidor de arquivos na sua organização com êxito foram carregados o Azure blob.
    
- Verifique se o nome do arquivo (e o nome de caminho subpasta se você incluiu um) para cada arquivo PST carregado para o Azure blob. Isso é realmente útil quando você estiver criando o arquivo na próxima etapa de mapeamento porque você precisou para especificar o nome do caminho de pasta e o nome de arquivo para cada arquivo PST de PST. Verificando a esses nomes pode ajudar a reduzir os erros potenciais em seu arquivo de mapeamento de PST.
    
O Microsoft Azure Storage Explorer está no modo de visualização.
  
> [!IMPORTANT]
> Você não pode usar o Gerenciador de armazenamento do Windows Azure para carregar ou modificar arquivos PST. O único método suportado para importar arquivos PST para o Office 365 é usar AzCopy. Além disso, você não pode excluir arquivos PST que tenha carregado para o Azure blob. Se você tentar excluir um arquivo PST, você receberá um erro sobre não ter as permissões necessárias. Observe que todos os arquivos PST automaticamente são excluídos da sua área de armazenamento do Azure. Se não houver nenhum trabalho de importação em andamento, em seguida, todos os arquivos de PST no contêiner **ingestiondata** é excluído 30 dias após o trabalho de importação mais recente foi criado.
  
Para instalar o Windows Azure Storage Explorer e conectar-se a sua área de armazenamento do Azure:
  
1. Baixe e instale a [ferramenta Microsoft Azure Storage Explorer](https://go.microsoft.com/fwlink/p/?LinkId=544842).
    
2. Iniciar o Microsoft Azure Storage Explorer, clique com o botão **Contas de armazenamento** no painel esquerdo e, em seguida, clique em **conectar ao armazenamento do Azure**.
    
    ![Clique com o botão contas de armazenamento e clique em conectar ao armazenamento do Azure](media/75b80cc3-c336-4f96-ad32-54ac9b96a7af.png)
  
3. Clique em **usar uma sequência de conexão ou de URI de assinatura (SAS) acesso compartilhado** e clique em **Avançar**.
    
4. Clique em **usar um URI SAS**, cole a URL de SAS obtido na etapa 1 na caixa sob **URI**e clique em **Avançar**.
    
5. Na página **Resumo da Conexão** , revise as informações de conexão e, em seguida, clique em **Conectar**.
    
    O contêiner **ingestiondata** for aberto; ele contém os arquivos PST que você carregou na etapa 2. O contêiner **ingestiondata** encontra-se em **Contas de armazenamento** \> **(Serviços de SAS-Attached)** \> **Contêineres de Blob**. 
    
    ![O Azure Storage Explorer exibe uma lista dos arquivos PST que você carregou](media/12376fed-13a5-4a09-8fe6-e819e011b334.png)
  
6. Quando você terminar de usar o Microsoft Azure Storage Explorer, clique com o botão **ingestiondata**e clique em **Desanexar** para desconectar da sua área de armazenamento do Azure. Caso contrário, você receberá um erro na próxima vez que você tentar anexar. 
    
    ![Clique com o botão direito em inclusão e clique em Desconectar para desconectar da sua área de armazenamento do Azure](media/1e8e5e95-4215-4ce4-a13d-ab5f826a0510.png)
  
## <a name="step-4-create-the-pst-import-mapping-file"></a>Etapa 4: Criar o arquivo de mapeamento de importação de PST

Depois que os arquivos PST foram carregados para o local de armazenamento do Azure para sua organização do Office 365, a próxima etapa é criar uma vírgula separados arquivo CSV (valor) que especifica quais caixas de correio de usuário dos arquivos PST será importados para. Quando você cria um trabalho de importação de PST, você vai enviar esse arquivo CSV na próxima etapa.
  
1. [Baixar uma cópia do arquivo de mapeamento de importação de PST](https://go.microsoft.com/fwlink/p/?LinkId=544717).
    
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
    A primeira linha ou a linha de cabeçalho do arquivo CSV lista os parâmetros que serão usados pelo serviço de importação de PST para importar os arquivos PST para caixas de correio do usuário. O nome de cada parâmetro é separado por uma vírgula. Cada linha sob a linha de cabeçalho representa os valores de parâmetro para importar um arquivo PST para uma caixa de correio específica. Você precisará de uma linha para cada arquivo PST que você deseja importar uma caixa de correio do usuário. Certifique-se de substituir os dados de espaço reservado no arquivo de mapeamento com seus dados reais.

   **Observação:** Não altere nada na linha de cabeçalho, incluindo os parâmetros do SharePoint; eles serão ignorados durante o processo de importação de PST. 

 3. Use as informações da tabela a seguir para preencher o arquivo CSV com as informações necessárias.


    |**Parameter**|**Descrição**|**Exemplo**|
    |:-----|:-----|:-----|
    | `Workload` <br/> |Especifica que os dados serão importados para o serviço do Office 365. Para importar arquivos PST às caixas de correio do usuário, use `Exchange`.<br/> | `Exchange` <br/> |
    | `FilePath` <br/> |Especifica o local da pasta no local de armazenamento do Azure que você carregou os arquivos PST para na etapa 2.  <br/> Se você não incluir um nome da subpasta opcional na URL SAS no `/Dest:` parâmetro na etapa 2, deixe esse parâmetro em branco no arquivo CSV. Se você incluiu o nome da subpasta, especificá-lo nesse parâmetro (consulte o segundo exemplo). O valor para esse parâmetro diferencia maiusculas de minúsculas.<br/> De qualquer forma, *não* incluir "ingestiondata" no valor para o `FilePath` parâmetro.  <br/><br/> **Importante:** Caso o nome do caminho de arquivo deve ser o mesmo que o caso você usou se você incluiu um nome da subpasta opcional na URL SAS no `/Dest:` parâmetro na etapa 2. Por exemplo, se você usou `PSTFiles` para a subpasta nomeie na etapa 2 e, em seguida, use `pstfiles` no `FilePath` parâmetro no arquivo CSV, a importação do arquivo PST falhará. Certifique-se de usar o mesmo caso em ambas as instâncias.<br/> |(deixar em branco)  <br/> Ou  <br/>  `PSTFiles` <br/> |
    | `Name` <br/> |Especifica o nome do arquivo PST que será importado para a caixa de correio do usuário. O valor para esse parâmetro diferencia maiusculas de minúsculas.<br/> <br/>**Importante:** Caso o nome do arquivo PST no arquivo CSV deve ser o mesmo que o arquivo PST que foi atualizado para o local de armazenamento do Azure na etapa 2. Por exemplo, se você usar `annb.pst` no `Name` parâmetro no arquivo CSV, mas o nome do arquivo PST real é `AnnB.pst`, a importação desse arquivo PST falhará. Certifique-se de que o nome do arquivo PST no arquivo CSV usa o mesmo caso como o arquivo PST real.<br/> | `annb.pst` <br/> |
    | `Mailbox` <br/> |Especifica o endereço de email da caixa de correio que será importado para o arquivo PST. Observe que você não pode especificar uma pasta pública porque o serviço de importação de PST não dá suporte a importação dos arquivos PST para pastas públicas.<br/> Para importar um arquivo PST para uma caixa de correio inativa, você precisa especificar a caixa de correio GUID para esse parâmetro. Para obter essa GUID, execute o seguinte comando do PowerShell no Exchange Online: ' Get-Mailbox <identity of inactive mailbox> - InactiveMailboxOnly | Guid FL` <br/> <br/>**Note:** In some cases, you might have multiple mailboxes with the same email address, where one mailbox is an active mailbox and the other mailbox is in a soft-deleted (or inactive) state. In these situations, you have to specify the mailbox GUID to uniquely identify the mailbox to import the PST file to. To obtain this GUID for active mailboxes, run the following PowerShell command:  `Get-Mailbox<identity of active mailbox> | Guid FL`. To obtain the GUID for soft-deleted (or inactive) mailboxes, run this command  `Get-Mailbox <identity of soft-deleted or inactive mailbox> - SoftDeletedMailbox | Guid FL'.  <br/> | `annb@contoso.onmicrosoft.com` <br/> Ou  <br/>  `2d7a87fe-d6a2-40cc-8aff-1ebea80d4ae7` <br/> |
    | `IsArchive` <br/> | Especifica se deve ou não importar o arquivo PST para a caixa de correio de arquivo morto do usuário. Há duas opções:<br/><br/>**FALSE** - importa o arquivo PST para a caixa de correio principal do usuário.  <br/> **TRUE** - importa o arquivo PST para o correio de arquivo morto do usuário. Isso pressupõe que a [caixa de correio de arquivo morto do usuário está habilitada](enable-archive-mailboxes.md).<br/><br/>Se você definir esse parâmetro como `TRUE` e caixa de correio de arquivo morto do usuário não está habilitada, a importação para esse usuário falhará. Observe que, se uma importação falhar por um usuário (porque seu arquivo não está habilitado e essa propriedade é definida como `TRUE`), os outros usuários do trabalho de importação não serão afetados.<br/>  Se você deixar esse parâmetro em branco, o arquivo PST é importado para a caixa de correio principal do usuário.  <br/> <br/>**Observação:** Para importar um arquivo PST para uma caixa de correio de arquivamento baseado em nuvem para um usuário cuja caixa de correio primária está no local, basta especificar `TRUE` para esse parâmetro e especifique o endereço de email para a caixa de correio do usuário no local para o `Mailbox` parâmetro.  <br/> | `FALSE` <br/> Ou  <br/>  `TRUE` <br/> |
    | `TargetRootFolder` <br/> | Especifica a pasta de caixa de correio importado para o arquivo PST.  <br/>  Se você deixar esse parâmetro em branco, o PST será importado para uma nova pasta denominada **importados** localizada no nível raiz da caixa de correio (o mesmo nível que a pasta de caixa de entrada e as outras pastas de caixa de correio padrão).  <br/>  Se você especificar `/`, itens no arquivo PST serão importados diretamente na pasta de caixa de entrada do usuário.  <br/><br/>  Se você especificar `/<foldername>`, itens no arquivo PST serão importados para uma pasta denominada * \<foldername\> * . Por exemplo, se você usar `/ImportedPst`, itens seriam importadas para uma pasta denominada **ImportedPst**. Essa pasta estará localizada na caixa de correio do usuário no mesmo nível como a pasta de caixa de entrada.<br/><br/> **Dica:** Considere a execução de alguns lotes de teste para experimentar com esse parâmetro para que você possa determinar o melhor local de pasta para importar arquivos de PSTs para.  <br/> |(deixar em branco)  <br/> Ou  <br/>  `/` <br/> Ou  <br/>  `/ImportedPst` <br/> |
    | `ContentCodePage` <br/> |Esse parâmetro opcional especifica um valor numérico para a página de código a ser usado para importação de arquivos PST no formato de arquivo ANSI. Este parâmetro é usado para importar arquivos PST organizações chinês, japonês e coreano (CJK) porque esses idiomas geralmente usam um conjunto de caracteres de byte duplo (DBCS) para codificação de caracteres. Se esse parâmetro não é usado para importar arquivos PST para idiomas que usam DBCS para nomes de pasta de caixa de correio, os nomes de pasta frequentemente são truncados após a importação.<br/><br/> Para obter uma lista de valores suportados para usar para esse parâmetro, consulte [Identificadores de página de código](https://go.microsoft.com/fwlink/p/?LinkId=328514).  <br/> <br/>**Observação:** Conforme anteriormente mencionado, este é um parâmetro opcional e você não tiver incluí-lo no arquivo CSV. Ou você pode incluí-lo e deixe o valor em branco para uma ou mais linhas.<br/> |(deixar em branco)  <br/> Ou  <br/>  `932`(que é o identificador de página de código para ANSI/OEM japonês)  <br/> |
    | `SPFileContainer` <br/> |Deixe este parâmetro em branco para Importação de PST.   <br/> |Não aplicável  <br/> |
    | `SPManifestContainer` <br/> |Deixe este parâmetro em branco para Importação de PST.   <br/> |Não aplicável  <br/> |
    | `SPSiteUrl` <br/> |Deixe este parâmetro em branco para Importação de PST.   <br/> |Não aplicável  <br/> |

## <a name="step-5-create-a-pst-import-job-in-office-365"></a>Etapa 5: criar um trabalho de Importação de PST no Office 365

A próxima etapa é criar o trabalho de importação de PST no serviço de importação no Office 365. Conforme explicado anteriormente, você enviará o arquivo de mapeamento de importação de PST que você criou na etapa 4. Após criar o novo trabalho, o Office 365 analisa os dados nos arquivos PST e então oferece uma oportunidade para filtrar os dados que realmente obtém importou para as caixas de correio especificadas no arquivo de mapeamento de importação de PST (consulte a [etapa 6](#step-6-filter-data-and-start-the-pst-import-job)).
  
1. Vá para [https://protection.office.com](https://protection.office.com) e entrar usando as credenciais para uma conta de administrador em sua organização do Office 365. 
    
2. No painel à esquerda da segurança &amp; Centro de conformidade, clique **governança de dados** e clique em **Importar**.
    
3. Na página **Importar** , clique em ![ícone Adicionar](media/ITPro-EAC-AddIcon.gif) **novo trabalho de importação**.
    
    **Observação:** Você precisa ter as permissões apropriadas para acessar a página **Importar** na segurança &amp; Centro de conformidade para criar um novo trabalho de importação. Consulte a seção **antes de começar** , para obter mais informações. 
    
4. Digite um nome para o trabalho de importação de PST e, em seguida, clique em **Avançar**. Use letras minúsculas, números, hifens e sublinhados. Você não pode usar letras maiusculas ou incluir espaços no nome de usuário.
    
5. Sobre o **você deseja carregar ou enviar dados?** página, clique em **carregar seus dados** e clique em **Avançar**.
    
    ![Clique em carregar dados para criar um carregamento de rede de trabalho de importação](media/e59f9dc3-ccde-44ff-ac38-c4e39d76ae85.png)
  
6. Na etapa 4 na página **Importar dados** , clique o **eu terminei carregamento Meus arquivos** e **posso ter acesso ao arquivo de mapeamento** de caixas de seleção e, em seguida, clique em **Avançar**.
    
    ![Clique em duas caixas de seleção na etapa 4](media/9f2427e8-3af2-4e27-95e6-a9f08430d3d8.png)
  
7. Na página **Selecionar o arquivo de mapeamento** , clique em **Selecionar arquivo de mapeamento** para enviar o arquivo de mapeamento de importação de PST que você criou na etapa 4. 
    
    ![Clique em arquivo de mapeamento Select para enviar o arquivo CSV criado para o trabalho de importação](media/d30b1d73-80bb-491e-a642-a21673d06889.png)
  
8. Após o nome do CSV arquivo aparecerá sob **o mapeamento de nome de arquivo**, clique em **Validar** para verificar se há erros no arquivo CSV. 
    
    ![Clique em Validar para verificar o arquivo CSV para erros](media/4680999d-5538-4059-b878-2736a5445037.png)
  
    O arquivo CSV deve ser validado com êxito para criar um trabalho de importação de PST. Observe que o nome do arquivo é alterado para verde após ser validada com êxito. Se a validação falhar, clique no link **Exibir log** . Um relatório de erros de validação é aberto, com uma mensagem de erro para cada linha no arquivo que falharam. 
    
9. Depois que o arquivo de mapeamento de PST com êxito é validado, leia o documento termos e condições e clique em caixa de seleção.
    
10. Clique em **Salvar** para enviar o trabalho e clique em **Fechar** depois que o trabalho foi criado com êxito. 
    
    Uma página de status submenu é exibida, com um status da **análise em andamento** e o novo trabalho de importação é exibido na lista na página **Importar** . 
    
11. Clique em **Atualizar** ![ícone atualizar](media/O365-MDM-Policy-RefreshIcon.gif) para atualizar as informações de status são exibidas na coluna **Status** . Quando a análise for concluída e os dados estão prontos para ser importado, o status é alterado para **Análise concluída**.
    
    Você pode clicar o trabalho de importação para exibir a página status do submenu, que contém informações mais detalhadas sobre o trabalho de importação, como o status de cada arquivo PST listado no arquivo de mapeamento.
 
## <a name="step-6-filter-data-and-start-the-pst-import-job"></a>Etapa 6: Filtrar dados e iniciar o trabalho de importação de PST

Depois de criar o trabalho de importação na etapa 5, o Office 365 analisa os dados nos arquivos PST (em uma forma segura e) identificando a idade dos itens e os tipos de mensagem diferente incluídos nos arquivos PST. Quando a análise for concluída e os dados estão prontos para importação, você tem a opção para importar todos os dados contidos nos arquivos PST ou você pode reduzir os dados são importados, definindo filtros que controlam quais dados obtém importados.
  
1. Na página **Importar** na segurança &amp; Centro de conformidade, clique em **pronto para importar para o Office 365** para o trabalho de importação que você criou na etapa 5. 
    
    ![Clique em pronto para importar para o Office 365, ao lado do trabalho de importação que você criou](media/5760aac3-300b-4e31-b894-253c42a4b82b.png)
  
    Um efeito de saída de página é exibido com informações sobre os arquivos PST e outras informações sobre o trabalho de importação.
    
2. Na página submenu, clique em **Importar para o Office 365**.
    
    A página de **seus dados de filtro** é exibida. Ele contém as ideias de dados resultante da análise de executadas nos arquivos PST pelo Office 365, incluindo informações sobre a idade dos dados. Neste ponto, você tem a opção para filtrar os dados que serão importados ou importar todos os dados como está. 
    
    ![É possível reduzir os dados nos arquivos PST ou importar todas essas](media/287fc030-99e9-417b-ace7-f64617ea5d4e.png)
  
3. Siga um destes procedimentos:
    
    r. para reduzir os dados que você importar, clique em **Sim, desejo filtrá-la antes da importação**.
    
    Para obter instruções detalhadas passo a passo sobre como filtrar os dados nos arquivos PST e, em seguida, iniciar o trabalho de importação, consulte [Filtrar dados durante a importação de arquivos PST para o Office 365](filter-data-when-importing-pst-files.md).
    
    Ou
    
    b. para importar todos os dados nos arquivos PST, clique em **não, eu quiser importar tudo** e clique em **Avançar**.
    
4. Se você optar por importar todos os dados, clique em **Importar dados** para iniciar o trabalho de importação. 
    
    O status do trabalho de importação é exibição na página **Importar** . Clique em ![ícone atualizar](media/O365-MDM-Policy-RefreshIcon.gif) **Refresh** para atualizar as informações de status são exibidas na coluna **Status** . Clique no trabalho de importação para exibir a página status do submenu, que exibe informações de status sobre cada arquivo PST sendo importado. 

## <a name="how-the-import-process-works"></a>Como funciona o processo de importação
  
Você pode usar a opção de carregamento de rede e o serviço Office 365 importar para importação em massa de arquivos PST às caixas de correio do usuário. Carregamento de rede significa que você carregar os arquivos PST uma área de armazenamento temporário em nuvem da Microsoft. Em seguida, o serviço de importação do Office 365 copia os arquivos PST da área de armazenamento para as caixas de correio de usuário de destino.
  
Aqui está uma ilustração e uma descrição do processo de carregamento de rede para importar arquivos PST para caixas de correio no Office 365.
  
![Fluxo de trabalho da rede carregar o processo para importar arquivos PST para o Office 365](media/9e05a19e-1e7a-4f1f-82df-9118f51588c4.png)
  
1. **Download de arquivo PST importar ferramenta e o local de armazenamento do Azure principais para private** - a primeira etapa é para baixar a ferramenta de linha de comando do Windows Azure AzCopy e uma tecla de acesso usado para carregar os arquivos PST para um local de armazenamento do Azure em nuvem da Microsoft. Você obtê-los da página **importação** na segurança do Office 365 &amp; Centro de conformidade. A chave (chamado de uma chave de assinatura (SAS) de acesso seguro, fornece as permissões necessárias para carregar os arquivos PST para um particular e seguro local de armazenamento do Azure. Essa chave de acesso é exclusivo para a sua organização e ajuda a impedir o acesso não autorizado aos seus arquivos PST após terem sido carregadas para a nuvem da Microsoft. Observe que a importação dos arquivos PST para o Office 365 não exige sua organização tenha uma assinatura Azure separada. 
    
2. **Carregar os arquivos PST para o local de armazenamento do Azure** - a próxima etapa é usar a ferramenta de AzCopy.exe (baixada na etapa 1) para carregar e armazenar seus arquivos PST em um local de armazenamento do Azure que reside no mesmo datacenter regional Microsoft onde seu Office 365 organização está localizada. Para carregá-las, os arquivos PST que você deseja importar para o Office 365 precisam estar localizado em um compartilhamento de arquivo ou o servidor de arquivos na sua organização.
    
    Observe que não há uma etapa opcional que podem ser executadas para exibir a lista de arquivos PST após terem sido carregadas no local de armazenamento do Azure.
    
3. **Criar um arquivo de mapeamento de importação de PST** - após os arquivos PST foram carregados para o local de armazenamento do Azure, a próxima etapa é criar um arquivo (CSV) de valores separados por vírgula que especifica quais caixas de correio de usuário dos arquivos PST será importados para, observe que um arquivo PST pode ser  importados para a caixa de correio principal do usuário ou de suas caixas de correio de arquivo morto. O serviço Office 365 importar usará as informações no arquivo CSV para importar os arquivos PST.
    
4. **Trabalho de importação de criar um PST** - a próxima etapa é criar um trabalho de importação de PST na página **Importar** na segurança &amp; Centro de conformidade e enviar o arquivo de mapeamento de importação de PST criado na etapa anterior. Depois de criar o trabalho de importação, o Office 365 analisa os dados nos arquivos PST e então oferece a oportunidade de definir os filtros que controlam quais dados realmente obtém importados para as caixas de correio especificadas no arquivo de mapeamento de importação de PST. 
    
5. **Filtrar os dados de PST que serão importados para caixas de correio** - depois que o trabalho de importação é criado e iniciado, Office 365 analisa os dados nos arquivos PST (com segurança e com segurança) identificando a idade dos itens e os tipos de mensagem diferente incluídos nos arquivos PST . Quando a análise for concluída e os dados estão prontos para importação, você tem a opção para importar todos os dados contidos nos arquivos PST ou você pode reduzir os dados são importados, definindo filtros que controlam quais dados obtém importados.
    
6. **Iniciar o trabalho de importação de PST** - depois que o trabalho de importação é iniciado, o Office 365 usa as informações no arquivo de mapeamento de importação PST na importação dos arquivos de PSTs do local de armazenamento do Azure s às caixas de correio do usuário. Informações de status sobre o trabalho de importação (incluindo informações sobre cada arquivo PST sendo importado) são exibidas na página **Importar** na segurança &amp; Centro de conformidade. Quando o trabalho de importação for concluído, o status do trabalho for definido como **Complete**.
  
## <a name="more-information"></a>Mais informações

- Por que importar arquivos PST para o Office 365?
    
  - É uma boa maneira para importar dados para arquivamento mensagens da sua organização para o Office 365.
    
  - Os dados ficam disponíveis para o usuário em todos os dispositivos, pois eles são armazenados na nuvem.
    
  - Ele ajuda a atender às necessidades de conformidade da sua organização, permitindo que você aplicar recursos de conformidade do Office 365 aos dados de arquivos PST que você importou. Isso inclui:
    
  - Habilitando a [caixas de correio de arquivo morto](enable-archive-mailboxes.md) e a [expansão automática de arquivamento](enable-unlimited-archiving.md) para dar aos usuários de espaço de armazenamento de caixa de correio adicional para armazenar os dados que você importou. 
    
  - Colocação de caixas de correio em [Retenção de litígio](https://go.microsoft.com/fwlink/?linkid=856286) para reter os dados que você importou. 
    
  - Usando [Ferramentas de descoberta eletrônica](search-for-content.md) da Microsoft para pesquisar os dados que você importou. 
    
  - Usando [as políticas de retenção do Office 365](retention-policies.md) para controlar quanto tempo os dados que você importou serão mantidos e qual ação a ser executada depois que o período de retenção expira. 
    
  - Pesquisar o [log de auditoria do Office 365](search-the-audit-log-in-security-and-compliance.md) para eventos relacionados a caixa de correio que afetam os dados que você importou. 
    
  - Importando dados para [caixas de correio inativas](create-and-manage-inactive-mailboxes.md) para arquivar dados para fins de conformidade. 
    
  - Usando [políticas de prevenção de perda de dados](data-loss-prevention-policies.md) para impedir que os dados confidenciais vazamento de fora da sua organização. 
  
- Aqui está um exemplo da URL assinatura de acesso compartilhado (SAS) que é obtido na etapa 1. Este exemplo também contém a sintaxe para o comando que você pode executar na ferramenta AzCopy.exe para carregar os arquivos PST para o Office 365. Certifique-se de que tome precauções para proteger a URL SAS exatamente como você faria proteger senhas ou outras informações relacionadas à segurança.

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
    
   - You can configure the retention hold so that it's turned off on some date in the future. You do this by running the **Set-Mailbox -EndDateForRetentionHold *date*** command. For example, assuming that today's date is July 1, 2016 and you want the retention hold turned off in 30 days, you would run the following command:  **Set-Mailbox -EndDateForRetentionHold 8/1/2016**. In this scenario, you would leave the  **RetentionHoldEnabled**  property set to  *True*. For more information, see [Set-Mailbox](https://go.microsoft.com/fwlink/p/?LinkId=150317).
    
   - You can change the settings for the retention policy that's assigned to the mailbox so that older items that were imported won't be immediately deleted or moved to the user's archive mailbox. For example, you could lengthen the retention age for a deletion or archive policy that's assigned to the mailbox. In this scenario, you would turn off the retention hold on the mailbox after you changed the settings of the retention policy. For more information, see [Set up an archive and deletion policy for mailboxes in your Office 365 organization](set-up-an-archive-and-deletion-policy-for-mailboxes.md).
    

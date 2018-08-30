---
title: Use o envio de unidade para importar seus arquivos PST da organização para o Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/14/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 40829b57-793c-4d41-b171-e9270129173d
description: 'Para administradores: Aprenda a importação em massa arquivos PST de sua organização para caixas de correio do Office 365 copiando arquivos PST para um disco rígido e, em seguida, ele envio à Microsoft. '
ms.openlocfilehash: ebe88918b6c25e18562db7817d22fbf71f05e4c7
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523970"
---
# <a name="use-drive-shipping-to-import-your-organization-pst-files-to-office-365"></a>Use o envio de unidade para importar seus arquivos PST da organização para o Office 365

**Este artigo destina-se a administradores. Você está tentando importar arquivos PST para sua própria caixa de correio? Consulte o [email de importação, contatos e calendário de um arquivo. pst do Outlook](https://go.microsoft.com/fwlink/p/?LinkID=785075)**
   
Use o serviço Office 365 importar e a unidade de envio de importação em massa de arquivos PST às caixas de correio do usuário. Envio de unidade significa que você copie os arquivos PST para um disco rígido e, depois, enviar fisicamente unidade à Microsoft. Quando a Microsoft recebe seu disco rígido, o pessoal do data center copiar os dados do disco rígido para uma área de armazenamento em nuvem da Microsoft. Em seguida, você tem a oportunidade de reduzir os dados de PST realmente importado para as caixas de correio de destino, definindo filtros que controlam quais dados obtém importados. Depois de iniciar o trabalho de importação, o serviço de importação importa os dados de PST da área de armazenamento para caixas de correio do usuário. Usando o envio de unidade para importar arquivos PST para caixas de correio do usuário é uma maneira de migrar email de sua organização para o Office 365.
  
Aqui estão as etapas necessárias para usar o envio de unidade para importar arquivos PST para caixas de correio do Office 365:
  
[Etapa 1: Baixar a ferramenta de importação de PST e a chave de armazenamento seguro](#step-1-download-the-secure-storage-key-and-pst-import-tool)

[Etapa 2: Copie os arquivos PST para o disco rígido](#step-2-copy-the-pst-files-to-the-hard-drive)

[Etapa 3: Criar o arquivo de mapeamento de importação de PST](#step-3-create-the-pst-import-mapping-file)

[Etapa 4: criar um trabalho de Importação de PST no Office 365](#step-4-create-a-pst-import-job-in-office-365)

[Etapa 5: enviar o disco rígido para a Microsoft](#step-5-ship-the-hard-drive-to-microsoft)

[Etapa 6: Filtrar dados e iniciar o trabalho de importação de PST](#step-6-filter-data-and-start-the-pst-import-job)
  
> [!IMPORTANT]
> Você precisa executar a etapa 1 uma vez para pressionada carregar a chave de armazenamento seguro e a ferramenta de importação. Depois de executar estas etapas, siga a etapa 2, a etapa 6 cada vez que você deseja enviar um disco rígido para a Microsoft. 
  
Para perguntas frequentes sobre o uso de unidade de envio para importar arquivos PST para o Office 365, consulte as [Perguntas frequentes para usar a unidade de envio para importar arquivos PST](faqimporting-pst-files-to-office-365.md#using-drive-shipping-to-import-pst-files). 
  
## <a name="before-you-begin"></a>Antes de começar

- Você precisa ter a função caixa de correio importar exportar no Exchange Online para importar arquivos PST para caixas de correio do Office 365. Por padrão, essa função não é atribuída a nenhum grupo de função no Exchange Online. Você pode adicionar a função caixa de correio importar e exportar para o grupo de funções de gerenciamento da organização. Ou você pode criar um novo grupo de função, atribua a função caixa de correio importar e exportar e, em seguida, adicione si mesmo como membro. Para obter mais informações, consulte "Adicionar uma função para um grupo de funções" ou "Criar um grupo de funções" seções em [Gerenciar grupos de função](https://go.microsoft.com/fwlink/p/?LinkId=730688).
    
    Além disso criar a importação de trabalhos no Office 365 Security &amp; Centro de conformidade, uma das opções a seguir devem ser verdadeiro:
    
  - Você precisa ter a função de destinatários de email no Exchange Online. Por padrão, essa função é atribuída aos grupos de funções de gerenciamento de destinatário e gerenciamento da organização.
    
    Ou
    
  - Você precisa ser um administrador global na sua organização do Office 365.
    
    > [!TIP]
    > Considere a criação de um novo grupo de função no Exchange Online que destina-se especificamente para importar arquivos PST para o Office 365. Para o nível mínimo de privilégios necessários para importar arquivos PST, atribua as funções de caixa de correio importar exportar e destinatários de email para o novo grupo de função e, em seguida, adicionar membros. 
  
- Você precisa armazenar os arquivos PST que você deseja copiar para um disco rígido em um servidor de arquivo ou a pasta compartilhada em sua organização. Na etapa 2, você executará a ferramenta Azure importar e exportar (WAImportExport.exe) que irá copiar os arquivos PST que são armazenados neste servidor de arquivo ou pasta no disco rígido compartilhada.
    
- Unidades de apenas de 2,5 polegadas de estado sólida (SSDs) ou 2,5 ou 3,5 polegadas SATA II/III discos rígidos internos são compatíveis para uso com o serviço de importação do Office 365. Você pode usar os discos rígidos até 10 TB. Trabalhos de importação, apenas o primeiro volume de dados no disco rígido será processado. O volume de dados deve ser formatado com o NTFS. Ao copiar dados para um disco rígido, você pode anexá-lo diretamente usando um SSD de 2,5 polegadas ou 2.5 ou 3,5 polegadas conector do SATA II/III ou você pode anexá-lo externamente usando uma SSD externo de 2,5 polegadas ou adaptador USB do SATA II/III de polegada 2.5 ou 3.5.
    
    > [!IMPORTANT]
    > Discos rígidos externos que vêm com um adaptador USB interno não são suportados pelo serviço de importação do Office 365. Além disso, o disco de maiusculas e minúsculas de um disco rígido externo não pode ser usado. Por favor, não vêm discos rígidos externos. 
  
- Disco rígido que você copie os arquivos PST para deve ser criptografado com BitLocker. A ferramenta WAImportExport.exe que você pode executar na etapa 2 ajudarão você a configurar o BitLocker. Ele também gera uma chave de criptografia que o Microsoft pessoal do Centro de dados usará para acessar a unidade para carregar os arquivos PST para a área de armazenamento do Azure na nuvem da Microsoft.
    
- Envio de unidade está disponível por meio de um Microsoft EA (Enterprise Agreement). Envio de unidade não está disponível por meio de um Microsoft Products and Services contrato (MPSA).
    
- O custo para importar arquivos PST para caixas de correio do Office 365 usando o envio de unidade é de US $ 2 por GB de dados. Por exemplo, se você enviar um disco rígido que contém 1.000 GB (1TB) dos arquivos PST, o custo é de US $2.000. Você pode trabalhar com um parceiro para pagar a taxa de importação. Para obter informações sobre como encontrar um parceiro, consulte [Encontre seu parceiro do Office 365 ou um revendedor](https://go.microsoft.com/fwlink/p/?LinkId=785197).
    
- Você ou a organização devem ter uma conta da FedEx ou da DHL. 
    
  - Organizações nos Estados Unidos, no Brasil e na Europa devem ter contas de FedEx.
    
  - Organizações do Leste Asiático, Sudeste Asiático, Japão, República Popular da Coreia e Austrália devem ter contas DHL.
    
    A Microsoft usará e cobrará essa conta para devolver o disco rígido a você. 
    
- Pode ser que o disco rígido seja enviado para a Microsoft através de uma remessa internacional. Se esse for o caso, você é responsável por garantir que o disco rígido e os dados incluídos nele sejam importados e/ou exportados de acordo com a legislação vigente. Antes de enviar um disco rígido, peça aos seus consultores para verificar se a unidade e os dados podem ser enviados legalmente para o datacenter identificado da Microsoft. Isso ajudará a garantir que o material chegue à Microsoft em tempo hábil.
    
- Esse procedimento envolve copiar e salvar uma chave de armazenamento seguro e uma chave de criptografia. Certifique-se de que tome precauções para proteger essas chaves como você faria proteger senhas ou outras informações relacionadas à segurança. Por exemplo, você poderá salvá-los em um documento do Microsoft Word protegido por senha ou salvá-los em uma unidade USB criptografada. Consulte a seção de [informações adicionais](use-drive-shipping-to-import-pst-files-to-office-365.md#moreinfo) para obter um exemplo dessas chaves. 
    
- Depois que os arquivos PST são importados para uma caixa de correio do Office 365, a configuração da caixa de correio de retenção é ativada por um período indefinido. Isso significa que a política de retenção atribuída à caixa de correio não será processada até que você desative o status em retenção ou definir uma data para desativar o bloqueio. Por que fazemos isso? Se mensagens importadas para uma caixa de correio são antigas, podem ser permanentemente excluídos (purgados) porque seu período de retenção expirou com base nas configurações de retenção configuradas para a caixa de correio. Colocação de caixa de correio em retenção fornecerá o tempo de proprietário da caixa de correio para gerenciar essas mensagens importado recentemente ou dê tempo para alterar as configurações de retenção da caixa de correio. Consulte a seção de [informações adicionais](use-drive-shipping-to-import-pst-files-to-office-365.md#moreinfo) para obter sugestões sobre como gerenciar a retenção. 
    
- Por padrão, o tamanho de mensagem máximo que pode ser recebido por uma caixa de correio do Office 365 é 35 MB. Isso ocorre porque o valor padrão para a propriedade *MaxReceiveSize* para uma caixa de correio é definido como 35 MB. No entanto, o limite de tamanho de recebimento de mensagem máxima no Office 365 é 150 MB. Portanto, se você importar um arquivo PST que contém um item mais de 35 MB, o serviço Office 365 importar podemos automaticamente será alterado o valor da propriedade *MaxReceiveSize* na caixa de correio de destino para 150 MB. Isso permite que mensagens até 150 MB a ser importado para caixas de correio do usuário. 
    
    > [!TIP]
    > Para identificar a mensagem de tamanho de recebimento para uma caixa de correio, você pode executar esse comando no PowerShell do Exchange Online: `Get-Mailbox <user mailbox> | FL MaxReceiveSize`. 
  
- Você pode importar arquivos PST para uma caixa de correio inativa no Office 365. Você pode fazer isso, especificando o GUID da caixa de correio inativa no `Mailbox` parâmetro no arquivo de mapeamento de importação de PST. Consulte [etapa 3: criar o arquivo de mapeamento de importação de PST](use-drive-shipping-to-import-pst-files-to-office-365.md#step3) para obter mais informações. 
    
- Em uma implantação híbrida do Exchange, você pode importar arquivos PST, uma caixa de correio de arquivamento baseado em nuvem para um usuário cuja caixa de correio primária está no local. Você pode fazer isso fazendo o seguinte no arquivo de mapeamento de importação de PST:
    
  - Especifique o endereço de email para a caixa de correio do usuário local no `Mailbox` parâmetro. 
    
  - Especificar o valor **TRUE** no `IsArchive` parâmetro. 
    
    Consulte [etapa 3: criar o arquivo de mapeamento de importação de PST](use-drive-shipping-to-import-pst-files-to-office-365.md#step3) para obter mais informações. 

## <a name="step-1-download-the-secure-storage-key-and-pst-import-tool"></a>Etapa 1: Baixar a ferramenta de importação de PST e a chave de armazenamento seguro

A primeira etapa é para baixar a chave de armazenamento seguro e a ferramenta e que você usará na etapa 2 para copiar arquivos de PST para o disco rígido.
  
> [!IMPORTANT]
> Você precisa usar a versão da ferramenta de importação/exportação do Azure 1 (WAimportExportV1) para importar com êxito os arquivos PST usando o método de envio de unidade. Não há suporte para a versão 2 da ferramenta de importação/exportação do Windows Azure e usá-lo resultará em incorretamente Preparando o disco rígido para o trabalho de importação. Certifique-se baixar a ferramenta de importação/exportação do Windows Azure da segurança &amp; Centro de conformidade seguindo os procedimentos nesta etapa. 
  
1. Vá para [https://protection.office.com/](https://protection.office.com/) e entrar usando as credenciais para uma conta de administrador em sua organização do Office 365. 
    
2. No painel à esquerda da segurança &amp; Centro de conformidade, clique em **Governança dados** \> **importação**.
    
    > [!NOTE]
    > Conforme anteriormente mencionado, você precisa ter as permissões apropriadas para acessar a página de **importação** na segurança &amp; Centro de conformidade. 
  
3. Na página **Importar** , clique em ![ícone Adicionar](media/ITPro-EAC-AddIcon.gif) **novo trabalho de importação**.
    
4. No Assistente de importação de trabalho, digite um nome para o trabalho de importação de PST e, em seguida, clique em **Avançar**. Use letras minúsculas, números, hifens e sublinhados. Você não pode usar letras maiusculas ou incluir espaços no nome de usuário.
    
5. Na página **Escolher tipo de trabalho de importação** , clique em **unidades de disco rígido Ship até um dos nossos locais físicos** e clique em **Avançar**.
    
    ![Clique em unidades de disco rígido Ship até um dos nossos locais físicos para criar uma unidade de trabalho de importação de envio](media/1584fdc5-cd4c-4e47-932e-db6c8e07f5f8.png)
  
6. Na página **Importar dados** , siga estes dois procedimentos: 
    
    ![Copie a chave de armazenamento seguro e baixar a ferramenta Azure importar e exportar na página Importar dados](media/e22e0b48-e5ce-48e0-95bc-0490a2b3b983.png)
  
    r. na etapa 2, clique em **copiar a chave de armazenamento seguro**. Depois que a chave de armazenamento for exibida, clique em **Copiar para a área de transferência** e colá-lo e salvá-lo em um arquivo, portanto, você pode acessá-lo mais tarde.
    
    b. na etapa 3, **Baixe a ferramenta de importação/exportação do Windows Azure** para baixar e instalar a ferramenta de importação/exportação do Windows Azure (versão 1).
    
    - Na janela pop-up, clique em **Salvar** \> **Salvar como** para salvar o arquivo de WaImportExportV1.zip para uma pasta no computador local. 
    
    - Extraia o arquivo WaImportExportV1.zip.
    
7. Clique em **Cancelar** para fechar o assistente. 
    
    Você vai voltar à página **Importar** na segurança &amp; Centro de conformidade ao criar o trabalho de importação na etapa 4. 

## <a name="step-2-copy-the-pst-files-to-the-hard-drive"></a>Etapa 2: Copie os arquivos PST para o disco rígido

A próxima etapa é usar a ferramenta de WAImportExport.exe para copiar os arquivos PST para o disco rígido. Essa ferramenta criptografa o disco rígido com o BitLocker, copia os PSTs para o disco rígido e cria um arquivo de diário que armazena informações sobre o processo de cópia. Para concluir esta etapa, os arquivos PST precisam estar localizado em um compartilhamento de arquivo ou o servidor de arquivos na sua organização. Isso é conhecido como o diretório de origem no procedimento a seguir. 
  
> [!IMPORTANT]
> Depois de executar a ferramenta de WAImportExport.exe na primeira vez para um disco rígido, você precisa usar uma sintaxe diferente tempo depois disso. Essa sintaxe é explicada na etapa 4 deste procedimento para copiar os arquivos PST para o disco rígido. 
  
1. Abra um prompt de comando no computador local.
    
    > [!TIP]
    > Se você executar o prompt de comando como administrador (selecionando a opção "Executar como Administrador" exibida), o sistema exibirá mensagens de erro na janela do prompt de comando. Isso pode ser útil para solucionar problemas de execução da ferramenta WAImportExport.exe. 
  
2. Vá para o diretório em que instalou a ferramenta WAImportExport.exe na etapa 1.
    
3. Execute o seguinte comando na primeira vez que usar a ferramenta WAImportExport.exe para copiar arquivos PST em um disco rígido.

    ```
    WAImportExport.exe PrepImport /j:<Name of journal file> /t:<Drive letter> /id:<Name of session> /srcdir:<Location of PST files> /dstdir:<PST file path> /sk:<Storage account key> /encrypt /logdir:<Log file location>
    ```

    A tabela a seguir descreve os parâmetros e os valores necessários. 
    
    |**Parameter**|**Descrição**|**Exemplo**|
    |:-----|:-----|:-----|
    | `/j:` <br/> |Especifica o nome do arquivo de diário. Este arquivo será salvo na mesma pasta em que a ferramenta WAImportExport.exe está localizada. Cada disco rígido enviado para a Microsoft deve incluir um único arquivo de diário. Sempre que executar a ferramenta WAImportTool.exe para copiar arquivos PST em um disco rígido, as informações serão anexadas ao arquivo de diário dessa unidade. 
  <br/> Pessoal do Microsoft data center usará as informações no arquivo de diário para associar o disco rígido do trabalho de importação que você criar na etapa 4 e para carregar os arquivos PST para a área de armazenamento do Azure na nuvem da Microsoft.  <br/> | `/j:PSTHDD1.jrn` <br/> |
    | `/t:` <br/> |Especifica a letra da unidade do disco rígido quando ele está conectado ao computador local.  <br/> | `/t:h` <br/> |
    | `/id:` <br/> |Especifica o nome da sessão de cópia. A sessão é definida sempre que você executa a ferramenta WAImportExport.exe para copiar arquivos no disco rígido. Os arquivos PST são copiados em uma pasta com o nome da sessão especificado por este parâmetro.   <br/> | `/id:driveship1` <br/> |
    | `/srcdir:` <br/> |Especifica o diretório de origem em sua organização que contém os arquivos PST que serão copiados durante a sessão. Certifique-se ao redor do valor desse parâmetro com aspas duplas ("").  <br/> | `/srcdir:"\\FILESERVER01\PSTs"` <br/> |
    | `/dstdir:` <br/> |Especifica o diretório de destino na área de armazenamento do Azure na nuvem da Microsoft, onde os PSTs serão carregados. Você deve usar o valor `ingestiondata/`. Certifique-se ao redor do valor desse parâmetro com aspas duplas ("").<br/> Opcionalmente, você também pode adicionar um caminho de arquivo adicional para o valor desse parâmetro. Por exemplo, você pode usar o caminho do diretório de origem no disco rígido (convertido em um formato de URL), que é especificado no arquivo de `/srcdir:` parâmetro. Por exemplo, `\\FILESERVER01\PSTs` é alterado para `FILESERVER01/PSTs`. Nesse caso, você ainda deve incluir `ingestiondata` no caminho do arquivo. Portanto neste exemplo, o valor para o `/dstdir:` parâmetro seria `"ingestiondata/FILESERVER01/PSTs"`.<br/> Um motivo para adicionar o caminho de arquivo adicional é se você tem arquivos PSTs com o mesmo nome de arquivo.  <br/> > [!NOTE]> Se você incluir o nome do caminho opcional, o namespace para um arquivo PST depois que ele for carregado para a área de armazenamento do Azure incluirá o nome do caminho e o nome do arquivo PST. Por exemplo, `FILESERVER01/PSTs/annb.pst`. Se você não incluir um nome de caminho, o namespace é apenas o filename PST; Por exemplo `annb.pst`.           | `/dstdir:"ingestiondata/"` <br/> Ou  <br/>  `/dstdir:"ingestiondata/FILESERVER01/PSTs"` <br/> |
    | `/sk:` <br/> |Especifica a chave de conta de armazenamento que você obteve na etapa 1. Certifique-se ao redor do valor desse parâmetro com aspas duplas ("").  <br/> | `"yaNIIs9Uy5g25Yoak+LlSHfqVBGOeNwjqtBEBGqRMoidq6/e5k/VPkjOXdDIXJHxHvNoNoFH5NcVUJXHwu9ZxQ=="` <br/> |
    | `/encrypt` <br/> |Esta opção habilita o BitLocker no disco rígido. Este parâmetro é necessário na primeira vez que executar a ferramenta WAImportExport.exe.  <br/> A chave de criptografia de disco BitLocker é copiada para o arquivo de diário e o arquivo de log é criado, se você usar o `/logfile:` parâmetro. Conforme explicado anteriormente, o arquivo de registro no diário é salvo na mesma pasta onde a ferramenta WAImportExport.exe está localizada.<br/> | `/encrypt` <br/> |
    | `/logdir:` <br/> |Esse parâmetro opcional especifica uma pasta para salvar os arquivos de log. Se não especificado, os arquivos de log são salvar na mesma pasta onde a ferramenta WAImportExport.exe está localizada. Certifique-se ao redor do valor desse parâmetro com aspas duplas ("").  <br/> | `/logdir:"c:\users\admin\desktop\PstImportLogs"` <br/> |
   
    Veja um exemplo da sintaxe para a ferramenta WAImportExport.exe, que usa valores reais para os parâmetros:
    
    ```
    WAImportExport.exe PrepImport /j:PSTHDD1.jrn /t:f /id:driveship1 /srcdir:"\\FILESERVER01\PSTs" /dstdir:"ingestiondata/" /sk:"yaNIIs9Uy5g25Yoak+LlSHfqVBGOeNwjqtBEBGqRMoidq6/e5k/VPkjOXdDIXJHxHvNoNoFH5NcVUJXHwu9ZxQ==" /encrypt /logdir:"c:\users\admin\desktop\PstImportLogs"
    ```

    Depois de executar o comando, o sistema exibe mensagens de status que mostram o andamento da cópia dos arquivos PST no disco rígido. Uma mensagem de status final mostra o número total de arquivos que foram copiados com êxito. 
    
4. Execute este comando sempre que executar a ferramenta WAImportExport.ext para copiar arquivos PST no mesmo disco rígido.

    ```
    WAImportExport.exe PrepImport /j:<Name of journal file> /id:<Name of new session> /srcdir:<Location of PST files> /dstdir:<PST file path> 
    ```

    Veja um exemplo da sintaxe para a execução de sessões subsequentes para copiar os arquivos PST no mesmo disco rígido.  

    ```
    WAImportExport.exe PrepImport /j:PSTHDD1.jrn /id:driveship2 /srcdir:"\\FILESERVER01\PSTs\SecondBatch" /dstdir:"ingestiondata/"
    ```

## <a name="step-3-create-the-pst-import-mapping-file"></a>Etapa 3: Criar o arquivo de mapeamento de importação de PST

Depois que o pessoal do Microsoft data center carrega os arquivos PST do disco rígido para a área de armazenamento do Azure, o serviço de importação usará as informações no arquivo de mapeamento de importação de PST, que é um arquivo de valor (CSV) separados por vírgulas, que especifica quais caixas de correio do usuário de PST arquivos serão importados para. Quando você cria um trabalho de importação de PST, você enviará esse arquivo CSV na próxima etapa.
  
1. [Baixar uma cópia do arquivo de mapeamento de importação de PST](https://go.microsoft.com/fwlink/p/?LinkId=544717).
    
2. Abrir ou salvar o arquivo CSV no computador local. O exemplo a seguir mostra um arquivo de mapeamento para Importação de PST concluído (aberto no Bloco de notas). É muito mais fácil usar o Microsoft Excel para editar o arquivo CSV.

    ```
    Workload,FilePath,Name,Mailbox,IsArchive,TargetRootFolder,ContentCodePage,SPFileContainer,SPManifestContainer,SPSiteUrl
    Exchange,FILESERVER01/PSTs,annb.pst,annb@contoso.onmicrosoft.com,FALSE,/,,,,
    Exchange,FILESERVER01/PSTs,annb_archive.pst,annb@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    Exchange,FILESERVER01/PSTs,donh.pst,donh@contoso.onmicrosoft.com,FALSE,/,,,,
    Exchange,FILESERVER01/PSTs,donh_archive.pst,donh@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    Exchange,FILESERVER01/PSTs,pilarp.pst,pilarp@contoso.onmicrosoft.com,FALSE,/,,,,
    Exchange,FILESERVER01/PSTs,pilarp_archive.pst,pilarp@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    Exchange,,tonyk.pst,tonyk@contoso.onmicrosoft.com,FALSE,/,,,,
    Exchange,,tonyk_archive.pst,tonyk@contoso.onmicrosoft.com,TRUE,,,,,
    Exchange,,zrinkam.pst,zrinkam@contoso.onmicrosoft.com,FALSE,/,,,,
    Exchange,,zrinkam_archive.pst,zrinkam@contoso.onmicrosoft.com,TRUE,,,,,
    ```

    A primeira linha ou a linha de cabeçalho do arquivo CSV lista os parâmetros que serão usados pelo serviço de importação de PST para importar os arquivos PST para caixas de correio do usuário. O nome de cada parâmetro é separado por uma vírgula. Cada linha sob a linha de cabeçalho representa os valores de parâmetro para importar um arquivo PST para uma caixa de correio específica. Você precisará de uma linha para cada arquivo PST que foi copiado para o disco rígido. Certifique-se de substituir os dados de espaço reservado no arquivo de mapeamento com seus dados reais.

    > [!NOTE]
    > Não altere o conteúdo da linha de cabeçalho, inclusive os parâmetros SharePoint; eles serão ignorados durante o processo de Importação de PST. 
  
3. Use as informações da tabela a seguir para preencher o arquivo CSV com as informações necessárias.
    
    |**Parameter**|**Descrição**|**Exemplo**|
    |:-----|:-----|:-----|
    | `Workload` <br/> |Especifica que os dados serão importados para o serviço do Office 365. Para importar arquivos PST às caixas de correio do usuário, use `Exchange`.<br/> | `Exchange` <br/> |
    | `FilePath` <br/> | Especifica o local da pasta na área de armazenamento do Azure que arquivos PST serão copiados para quando o disco rígido é entregue à Microsoft.  <br/>  O que você adiciona nessa coluna no arquivo CSV depende o que você especificou para o `/dstdir:` parâmetro na etapa anterior.  <br/>  Se você tiver usado `/dstdir:"ingestiondata/"`, deixe esse parâmetro em branco no arquivo CSV.  <br/>  Se você incluiu um nome de caminho opcional para o valor do `/dstdir:` parâmetro (por exemplo, `/dstdir:"ingestiondata/FILESERVER01/PSTs"`, em seguida, use esse pathname (não incluindo "ingestiondata") para esse parâmetro no arquivo CSV. O valor para esse parâmetro diferencia maiusculas de minúsculas.<br/>  De qualquer forma, *não* incluir "ingestiondata" no valor para o `FilePath` parâmetro. Deixe esse parâmetro em branco ou especifique apenas o nome do caminho opcional.<br/> > [!IMPORTANT]> O caso, o nome do caminho de arquivo deve ser o mesmo caso em que você especificou no `/dstdir:` parâmetro na etapa anterior. Por exemplo, se você usou `"ingestiondata/FILESERVER01/PSTs"` para o nome da subpasta na etapa anterior, mas, em seguida, usado `fileserver01/psts` no `FilePath` parâmetro no arquivo CSV, a importação do arquivo PST falhará. Certifique-se de usar o mesmo caso em ambas as instâncias.           |(deixar em branco)  <br/> Ou  <br/>  `FILESERVER01/PSTs` <br/> |
    | `Name` <br/> |Especifica o nome do arquivo PST que será importado para a caixa de correio do usuário. O valor para esse parâmetro diferencia maiusculas de minúsculas.<br/> > [!IMPORTANT]> O caso o nome de arquivo PST no arquivo CSV deve ser o mesmo que o arquivo PST que foi atualizado para o local de armazenamento do Azure na etapa 2. Por exemplo, se você usar `annb.pst` no `Name` parâmetro no arquivo CSV, mas o nome do arquivo PST real é `AnnB.pst`, a importação desse arquivo PST falhará. Certifique-se de que o nome do arquivo PST no arquivo CSV usa o mesmo caso como o arquivo PST real.           | `annb.pst` <br/> |
    | `Mailbox` <br/> |Especifica o endereço de email da caixa de correio que será importado para o arquivo PST. Observe que você não pode especificar uma pasta pública porque o serviço de importação de PST não dá suporte a importação dos arquivos PST para pastas públicas.<br/> Para importar um arquivo PST para uma caixa de correio inativa, você precisa especificar a caixa de correio GUID para esse parâmetro. Para obter essa GUID, execute o seguinte comando do PowerShell no Exchange Online: ' Get-Mailbox <identity of inactive mailbox> - InactiveMailboxOnly | Guid FL` <br/> > [!NOTE]> In some cases, you might have multiple mailboxes with the same email address, where one mailbox is an active mailbox and the other mailbox is in a soft-deleted (or inactive) state. In these situations, you have to specify the mailbox GUID to uniquely identify the mailbox to import the PST file to. To obtain this GUID for active mailboxes, run the following PowerShell command:  `Get-Mailbox<identity of active mailbox> | Guid FL`. To obtain the GUID for soft-deleted (or inactive) mailboxes, run this command:  `Get-Mailbox <identity of soft-deleted or inactive mailbox> - SoftDeletedMailbox | Guid FL'.           | `annb@contoso.onmicrosoft.com` <br/> Ou  <br/>  `2d7a87fe-d6a2-40cc-8aff-1ebea80d4ae7` <br/> |
    | `IsArchive` <br/> | Especifica se deve ou não importar o arquivo PST para a caixa de correio de arquivo morto do usuário. Há duas opções:<br/> **FALSE** Importa o arquivo PST para a caixa de correio principal do usuário.  <br/> **TRUE** Importa o arquivo PST para o correio de arquivo morto do usuário. Isso pressupõe que a [caixa de correio de arquivo morto do usuário está habilitada](enable-archive-mailboxes.md). Se você definir esse parâmetro como `TRUE` e caixa de correio de arquivo morto do usuário não está habilitada, a importação para esse usuário falhará. Observe que, se uma importação falhar por um usuário (porque seu arquivo não está habilitado e essa propriedade é definida como `TRUE`), os outros usuários do trabalho de importação não serão afetados.<br/>  Se você deixar esse parâmetro em branco, o arquivo PST é importado para a caixa de correio principal do usuário.  <br/> **Observação:** Para importar um arquivo PST para uma caixa de correio de arquivamento baseado em nuvem para um usuário cuja caixa de correio primária está no local, basta especificar `TRUE` para esse parâmetro e especifique o endereço de email para a caixa de correio do usuário no local para o `Mailbox` parâmetro.  <br/> | `FALSE` <br/> Ou  <br/>  `TRUE` <br/> |
    | `TargetRootFolder` <br/> | Especifica a pasta de caixa de correio importado para o arquivo PST.  <br/>  Se você deixar esse parâmetro em branco, o PST será importado para uma nova pasta denominada **importados** localizada no nível raiz da caixa de correio (o mesmo nível que a pasta de caixa de entrada e as outras pastas de caixa de correio padrão).  <br/>  Se você especificar `/`, itens no arquivo PST serão importados diretamente na pasta de caixa de entrada do usuário.  <br/>  Se você especificar `/<foldername>`, itens no arquivo PST serão importados para uma pasta denominada * \<foldername\> * . Por exemplo, se você usar `/ImportedPst`, itens seriam importadas para uma pasta denominada **ImportedPst**. Essa pasta estará localizada na caixa de correio do usuário no mesmo nível como a pasta de caixa de entrada.<br/> |(deixar em branco)  <br/> Ou  <br/>  `/` <br/> Ou  <br/>  `/ImportedPst` <br/> |
    | `ContentCodePage` <br/> |Esse parâmetro opcional especifica um valor numérico para a página de código a ser usado para importação de arquivos PST no formato de arquivo ANSI. Este parâmetro é usado para importar arquivos PST organizações chinês, japonês e coreano (CJK) porque esses idiomas geralmente usam um conjunto de caracteres de byte duplo (DBCS) para codificação de caracteres. Se esse parâmetro não é usado para importar arquivos PST para idiomas que usam DBCS para nomes de pasta de caixa de correio, os nomes de pasta frequentemente são truncados após a importação.<br/> Para obter uma lista de valores suportados para usar para esse parâmetro, consulte [Identificadores de página de código](https://go.microsoft.com/fwlink/p/?LinkId=328514).  <br/> > [!NOTE]> Conforme anteriormente mencionado, este é um parâmetro opcional e você não tiver incluí-lo no arquivo CSV. Ou você pode incluí-lo e deixe o valor em branco para uma ou mais linhas.           |(deixar em branco)  <br/> Ou  <br/>  `932`(que é o identificador de página de código para ANSI/OEM japonês)  <br/> |
    | `SPFileContainer` <br/> |Deixe este parâmetro em branco para Importação de PST.   <br/> |Não aplicável  <br/> |
    | `SPManifestContainer` <br/> |Deixe este parâmetro em branco para Importação de PST.   <br/> |Não aplicável  <br/> |
    | `SPSiteUrl` <br/> |Deixe este parâmetro em branco para Importação de PST.   <br/> |Não aplicável  <br/> |

## <a name="step-4-create-a-pst-import-job-in-office-365"></a>Etapa 4: criar um trabalho de Importação de PST no Office 365

A próxima etapa é criar o trabalho de importação de PST no serviço de importação no Office 365. Conforme explicado anteriormente, você enviará o arquivo de mapeamento de importação de PST que você criou na etapa 3. Após criar o novo trabalho, o serviço de importação usará as informações no arquivo de mapeamento para importar os arquivos PST na caixa de correio do usuário especificado depois que os arquivos PST são copiados do disco rígido para a área de armazenamento do Windows Azure e criar e iniciar o trabalho de importação.
  
1. Vá para [https://protection.office.com](https://protection.office.com) e entrar usando as credenciais para uma conta de administrador em sua organização do Office 365. 
    
2. No painel à esquerda da segurança &amp; Centro de conformidade, clique **governança de dados** e clique em **Importar**.
    
3. Na página **Importar** , clique em ![ícone Adicionar](media/ITPro-EAC-AddIcon.gif) **novo trabalho de importação**.
    
    > [!NOTE]
    > Conforme anteriormente mencionado, você precisa ter as permissões apropriadas para acessar a página de **importação** na segurança &amp; Centro de conformidade. 
  
4. Digite um nome para o trabalho de importação de PST e, em seguida, clique em **Avançar**. Use letras minúsculas, números, hifens e sublinhados. Você não pode usar letras maiusculas ou incluir espaços no nome de usuário.
    
5. Na página **Escolher tipo de trabalho de importação** , clique em **unidades de disco rígido Ship até um dos nossos locais físicos** e clique em **Avançar**.
    
    ![Clique em unidades de disco rígido Ship até um dos nossos locais físicos para criar uma unidade de trabalho de importação de envio](media/1584fdc5-cd4c-4e47-932e-db6c8e07f5f8.png)
  
6. Na etapa 6, clique nas caixas de seleção **eu preparou meus discos rígidos e têm acesso aos arquivos de diário de unidade necessárias** e **posso ter acesso ao arquivo de mapeamento** e clique em **Avançar**.
    
    ![Clique em duas caixas de seleção na etapa 6](media/fad43078-ea68-4acd-b2ed-75a800183262.png)
  
7. Na página **Selecione o arquivo de unidade** , clique em **Selecionar arquivo de unidade**e, em seguida, vá para a mesma pasta onde a ferramenta WAImportExport.exe está localizada. O arquivo de diário que foi criado na etapa 2 foi copiado para essa pasta.
    
    ![Clique em Selecionar unidade arquivo para enviar o arquivo de diário que foi criado quando você executou a ferramenta WAImportExport.exe](media/1ea35c04-bd88-4d7e-b7d9-dc390149d94f.png)
  
8. Selecione o arquivo de diário. Por exemplo, `PSTHDD1.jrn`.
    
    > [!TIP]
    > Quando você executou a ferramenta de WAImportExport.exe na etapa 2, o nome do arquivo de registro no diário foi especificado pelo `/j:` parâmetro. 
  
9. Depois que o nome do arquivo unidade aparece sob **nome de arquivo de unidade**, clique em **Validar** para verificar se há erros no arquivo unidade. 
    
    ![Clique em Validar para validar o arquivo de unidade que você selecionou](media/4b707f5a-152a-4e74-b9f5-449c88d1fec4.png)
  
    O arquivo de unidade deve ser validado com êxito para criar um trabalho de importação de PST. Observe que o nome do arquivo é alterado para verde após ser validada com êxito. Se a validação falhar, clique no link **Exibir log** . Um relatório de erros de validação é aberto, com uma mensagem de erro com informações sobre por que o arquivo falhou. 
    
    > [!NOTE]
    > Você deve adicionar e validar um arquivo de diário para cada disco rígido que você enviar à Microsoft. 
  
10. Depois de adicionar e Validando um arquivo de diário para cada disco rígido que vai ser enviada à Microsoft, clique em **Avançar**.
    
11. Clique em ![ícone Adicionar](media/ITPro-EAC-AddIcon.gif) **Selecionar arquivo de mapeamento** para enviar o arquivo de mapeamento de importação de PST que você criou na etapa 3. 
    
    ![Clique em arquivo de mapeamento Select para enviar o arquivo CSV criado para o trabalho de importação](media/d30b1d73-80bb-491e-a642-a21673d06889.png)
  
12. Após o nome do CSV arquivo aparecerá sob **o mapeamento de nome de arquivo**, clique em **Validar** para verificar se há erros no arquivo CSV. 
    
    ![Clique em Validar para verificar o arquivo CSV para erros](media/4680999d-5538-4059-b878-2736a5445037.png)
  
    O arquivo CSV deve ser validado com êxito para criar um trabalho de importação de PST. Observe que o nome do arquivo é alterado para verde após ser validada com êxito. Se a validação falhar, clique no link **Exibir log** . Um relatório de erros de validação é aberto, com uma mensagem de erro para cada linha no arquivo que falharam. 
    
13. Depois que o arquivo de mapeamento de PST for validado com êxito, clique em **Avançar**.
    
14. Na página **fornecer informações de contato** , digite suas informações de contato nas caixas aplicáveis. 
    
    Observe que o endereço para o local da Microsoft que você entregará os discos rígidos para é exibido. Esse endereço é gerado automaticamente com base em seu local de centro de dados do Office 365. Copiar esse endereço para um arquivo ou assumir uma captura de tela.
    
15. Ler o documento termos e condições, clique na caixa de seleção e, em seguida, clique em **Salvar** para enviar o trabalho de importação. 
    
    Quando o trabalho de importação foi criado com êxito, será exibida uma página de status explica as próximas etapas da unidade do processo de envio.
    
16. Na página **Importar** , clique em ![ícone atualizar](media/O365-MDM-Policy-RefreshIcon.gif) **Atualizar** para exibida na nova unidade em que o trabalho de importação de envio na lista de trabalhos de importação. Observe que o status está definido como **Aguardando o número de rastreamento**. Também é possível clicar o trabalho de importação para exibir a página status do submenu, que contém informações mais detalhadas sobre o trabalho de importação.
 
## <a name="step-5-ship-the-hard-drive-to-microsoft"></a>Etapa 5: enviar o disco rígido para a Microsoft

A próxima etapa é enviados à Microsoft, disco rígido e forneça o número de rastreamento da remessa e retornar informações de remessa referente ao trabalho de envio de unidade. Depois que a unidade é recebida pela Microsoft, ela levará entre 7 e 10 dias de negócios para dados pessoal do centro para carregar os arquivos PST para a área de armazenamento do Azure para sua organização.
  
> [!NOTE]
> Se você não fornecer as informações de remessa de devolução até 14 dias de criação do trabalho de importação e o número de rastreamento, o trabalho de importação será expirado. Se isso ocorrer, você precisará criar uma nova unidade em que o trabalho de importação de envio (consulte [etapa 4: criar um trabalho de importação de PST no Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md#step4)) e envie-o novamente o arquivo de unidade e o arquivo de mapeamento de importação de PST. 
  
### <a name="ship-the-hard-drive"></a>Enviar o disco rígido

Quando enviar discos rígidos para a Microsoft, lembre-se do seguinte:
  
- Não vêm o adaptador do SATA para USB; Você precisa apenas fornecidos no disco rígido.
    
- Embale o disco rígido de forma adequada; por exemplo, use plástico-bolha ou uma bolsa antiestática.
    
- Use uma transportadora de entrega de sua preferência para enviar o disco rígido à Microsoft.
    
- O disco rígido para o endereço para o local da Microsoft que foi exibido quando você criou o trabalho de importação na etapa 4 são fornecidos. Certifique-se de incluir "Serviço de importação do Office 365" no endereço para remessa.
    
- Depois de enviar o disco rígido, lembre-se de anotar o nome da trasportadora e o número de rastreamento. Você vai precisar deles na etapa seguinte.
    
### <a name="enter-the-tracking-number-and-other-shipping-information"></a>Insira o número de rastreamento e outras informações da remessa.

Depois de enviar o disco rígido para a Microsoft, faça o procedimento a seguir na página do serviço Importar.
  
1. Vá para [https://protection.office.com](https://protection.office.com) e entrar usando as credenciais para uma conta de administrador em sua organização do Office 365. 
    
2. No painel esquerdo, clique em **controle de dados** e clique em **Importar**.
    
3. Na página **Importar** , clique no trabalho para a remessa de unidade que você deseja inserir o número de rastreamento. 
    
4. Na página status submenu, clique em **Inserir número de rastreamento**.
    
5. Forneça as seguintes informações sobre a remessa:
    
1. **Operadora de entrega** Digite o nome da operadora entrega que é usada para transportar o disco rígido para a Microsoft. 
    
2. **Número de rastreamento.** Digite o número de controle para a remessa de disco rígido. 
    
3. **Número de conta de retorno de carro** Digite o número de conta da sua organização para a operadora que listado em **retornar operadora**. Microsoft usará (e cobra) essa conta para enviar seu disco rígido para você. Observe que as organizações nos EUA e na Europa, deve ter uma conta com FedEx. As organizações na Ásia e o restante do mundo, deve ter uma conta com DHL.
    
6. Clique em **Salvar** para salvar essas informações do trabalho de importação. 
    
    Na página **Importar** , clique em ![ícone atualizar](media/O365-MDM-Policy-RefreshIcon.gif) **Refresh** para atualizar as informações para sua unidade de envio do trabalho de importação. Observe que o status agora está definido como **Drives em trânsito**.

## <a name="step-6-filter-data-and-start-the-pst-import-job"></a>Etapa 6: Filtrar dados e iniciar o trabalho de importação de PST

Depois que o seu disco rígido é recebido pela Microsoft, o status do trabalho de importação na página **Importar** será alterado para **unidades recebido**. Pessoal do Centro de dados usará as informações no arquivo de diário para carregar os arquivos PST para a área de armazenamento do Azure para sua organização. Neste ponto, o status será alterado para **importação em andamento**. Conforme indicado anteriormente, ela levará entre 7 a 10 dias de negócios depois de receber seu disco rígido para carregar os arquivos PST.
  
Depois que os arquivos PST são carregados para o Windows Azure, o status é alterado para **análise em andamento**. Isso indica que o Office 365 é analisar os dados nos arquivos PST (em uma forma segura e) para identificar a idade dos itens e os tipos de mensagem diferente incluídos nos arquivos PST. Quando a análise for concluída e os dados estão prontos para importação, o status do trabalho de importação é alterado para **Análise concluída**. Neste ponto, você tem a opção para importar todos os dados contidos nos arquivos PST ou você pode reduzir os dados são importados, definindo filtros que controlam quais dados obtém importados.
  
1. Vá para [https://protection.office.com](https://protection.office.com) e entrar usando as credenciais para uma conta de administrador em sua organização do Office 365. 
    
2. No painel esquerdo, clique em **Governança dados** > **importação**.
    
3. Na página **Importar** , clique em **pronto para importar para o Office 365** para o trabalho de importação que você criou na etapa 4. 
    
    ![Clique em pronto para importar para o Office 365, ao lado do trabalho de importação que você criou](media/5760aac3-300b-4e31-b894-253c42a4b82b.png)
  
    Um efeito de saída de página é exibido com informações sobre os arquivos PST e outras informações sobre o trabalho de importação.
    
4. Clique em **Importar para o Office 365**.
    
5. A página de **seus dados de filtro** é exibida. Ele contém as ideias de dados resultante da análise de executadas nos arquivos PST pelo Office 365, incluindo informações sobre a idade dos dados. Neste ponto, você tem a opção para filtrar os dados que serão importados ou importar todos os dados como está. 
    
    ![É possível reduzir os dados nos arquivos PST ou importar todas essas](media/287fc030-99e9-417b-ace7-f64617ea5d4e.png)
  
6. Siga um destes procedimentos:
    
    r. para reduzir os dados que você importar, clique em **Sim, desejo filtrá-la antes da importação**.
    
    Para obter instruções detalhadas passo a passo sobre como filtrar os dados nos arquivos PST e, em seguida, iniciar o trabalho de importação, consulte [Filtrar dados durante a importação de arquivos PST para o Office 365](filter-data-when-importing-pst-files.md).
    
    Ou
    
    b. para importar todos os dados nos arquivos PST, clique em **não, eu quiser importar tudo** e clique em **Avançar**.
    
7. Se você optar por importar todos os dados, clique em **Importar dados** para iniciar o trabalho de importação. 
    
    O status do trabalho de importação é exibido na página **Importar** . Clique em ![ícone atualizar](media/O365-MDM-Policy-RefreshIcon.gif) **Refresh** para atualizar as informações de status são exibidas na coluna **Status** . Clique no trabalho de importação para exibir a página status do submenu, que exibe informações de status sobre cada arquivo PST sendo importado. Quando a importação for concluída e os arquivos PST tenham sido importados para caixas de correio do usuário, o status será alterado para **concluída**.

## <a name="view-a-list-of-the-pst-files-uploaded-to-office-365"></a>Exibir uma lista dos arquivos PST carregados para o Office 365

Você pode instalar e usar o Microsoft Azure Storage Explorer (que é uma ferramenta gratuita de código aberto) para exibir a lista dos arquivos PST que podemos estão carregados (por pessoal do Microsoft data center) para a área de armazenamento do Azure para sua organização. Você pode fazer isso para verificar que os arquivos PST dos discos rígidos enviados à Microsoft foram carregados com êxito para a área de armazenamento do Azure.
  
O Microsoft Azure Storage Explorer está no modo de visualização.
  
 **Importante:** Você não pode usar o Gerenciador de armazenamento do Windows Azure para carregar ou modificar arquivos PST. O único método suportado para importar arquivos PST para o Office 365 é usar AzCopy. Além disso, você não pode excluir arquivos PST que tenha carregado para o Azure blob. Se você tentar excluir um arquivo PST, você receberá um erro sobre não ter as permissões necessárias. Observe que todos os arquivos PST automaticamente são excluídos da sua área de armazenamento do Azure. Se não houver nenhum trabalho de importação em andamento, em seguida, todos os arquivos PST no * * ingestiondata * * contêiner são excluídas de 30 dias após o trabalho de importação mais recente foi criado. 
  
Para instalar o Windows Azure Storage Explorer e conectar-se a sua área de armazenamento do Azure:
  
1. Execute as etapas a seguintes para obter a URL de assinatura de acesso compartilhado (SAS) para sua organização. Essa URL é uma combinação da URL para o local de armazenamento do Azure na nuvem para sua organização e uma chave SAS Microsoft network. Essa chave fornece as permissões necessárias para acessar o local de armazenamento do Azure da sua organização.
    
1. Vá para [https://protection.office.com/](https://protection.office.com/) e entrar usando as credenciais para uma conta de administrador em sua organização do Office 365. 
    
2. No painel à esquerda da segurança &amp; Centro de conformidade, clique em **Governança dados** \> **importação**.
    
3. Na página **Importar** , clique em ![ícone Adicionar](media/ITPro-EAC-AddIcon.gif) **novo trabalho de importação**.
    
4. No Assistente de importação de trabalho, digite um nome para o trabalho de importação de PST e, em seguida, clique em **Avançar**. Use letras minúsculas, números, hifens e sublinhados. Você não pode usar letras maiusculas ou incluir espaços no nome de usuário.
    
5. Na página **Escolher tipo de trabalho de importação** , clique em **carregar seus dados** e clique em **Avançar**.
    
6. Na etapa 2, clique em **Mostrar SAS URL de carregamento de rede**.
    
7. Depois que a URL for exibida, copiá-lo e salvá-lo em um arquivo. Certifique-se de copiar o URL completo.
    
    > [!IMPORTANT]
    > Certifique-se de que tome precauções para proteger a URL SAS. Isso pode ser usado por qualquer pessoa para acessar a área de armazenamento do Azure para sua organização. 
  
8. Clique em **Cancelar** para fechar o Assistente de trabalho de importação. 
    
2. Baixe e instale a [ferramenta Microsoft Azure Storage Explorer](https://go.microsoft.com/fwlink/p/?LinkId=544842).
    
3. Iniciar o Microsoft Azure Storage Explorer, clique com o botão **Contas de armazenamento** no painel esquerdo e, em seguida, clique em **conectar ao armazenamento do Azure**.
    
    ![Clique com o botão contas de armazenamento e clique em conectar ao armazenamento do Azure](media/75b80cc3-c336-4f96-ad32-54ac9b96a7af.png)
  
4. Clique em **usar uma sequência de conexão ou de URI de assinatura (SAS) acesso compartilhado** e clique em **Avançar**.
    
5. Clique em **usar um URI SAS**, cole a URL de SAS obtido na etapa 1 para na caixa em **URI**e clique em **Avançar**.
    
6. Na página **Resumo da Conexão** , revise as informações de conexão e, em seguida, clique em **Conectar**.
    
    O contêiner **ingestiondata** for aberto; ele contém os arquivos PST do disco rígido. O contêiner **ingestiondata** encontra-se em **Contas de armazenamento** \> **(Serviços de SAS-Attached)** \> **Contêineres de Blob**.
    
    ![O Azure Storage Explorer exibe uma lista dos arquivos PST que você carregou](media/12376fed-13a5-4a09-8fe6-e819e011b334.png)
  
7. Quando você terminar de usar o Microsoft Azure Storage Explorer, clique com o botão **ingestiondata**e clique em **Desanexar** para desconectar da sua área de armazenamento do Azure. Caso contrário, você receberá um erro na próxima vez que você tentar anexar. 
    
    ![Clique com o botão direito em inclusão e clique em Desconectar para desconectar da sua área de armazenamento do Azure](media/1e8e5e95-4215-4ce4-a13d-ab5f826a0510.png)
  

  
## <a name="troubleshooting-tips"></a>Dicas de solução de problemas
<a name="troubleshootingtips"> </a>

- **o que acontece se o trabalho de importação falhar devido a erros no arquivo de mapeamento de PST Importar CSV?** Se um trabalho de importação falhar devido a erros no arquivo de mapeamento, você não precisa enviar novamente o disco rígido para a Microsoft para criar um novo trabalho de importação. Isso ocorre porque os arquivos PST do disco rígido que você enviados para o trabalho de importação de envio de unidade já foram carregados para a área de armazenamento do Azure para sua organização. Nesse caso, você só precisa corrija os erros no arquivo de mapeamento de PST Importar CSV e, em seguida, criar um novo trabalho de importação "carregamento de rede" e enviar o arquivo de mapeamento de CSV revisado. Para criar e iniciar um novo trabalho de importação de carregamento de rede, consulte [etapa 5: criar um trabalho de importação de PST no Office 365](use-network-upload-to-import-pst-files.md#step-5-create-a-pst-import-job-in-office-365) e [etapa 6: filtrar dados e iniciar o trabalho de importação de PST](use-network-upload-to-import-pst-files.md#step-6-filter-data-and-start-the-pst-import-job) no tópico "Upload de rede usado para importar arquivos PST para o Office 365". 
    
    > [!NOTE]
    > Para ajudá-lo a solucionar problemas do arquivo de mapeamento de PST Import CSV, use a ferramenta de [Gerenciador de armazenamento do Windows Azure](#view-a-list-of-the-pst-files-uploaded-to-office-365) para exibir a estrutura de pasta no contêiner **ingestiondata** para os arquivos PST do disco rígido que foram carregados para a área de armazenamento do Azure. Erros de arquivo de mapeamento são geralmente causados por um valor incorreto no parâmetro FilePath. Este parâmetro especifica o local de um arquivo PST na área de armazenamento do Azure. Consulte a descrição do parâmetro FilePath na tabela na [etapa 3](#step-3-create-the-pst-import-mapping-file). Conforme explicado anteriormente, o local dos arquivos PST na área de armazenamento do Azure foi especificado pelo `/dstdir:` parâmetro quando executou a ferramenta de WAImportExport.exe na [etapa 2](#step-2-copy-the-pst-files-to-the-hard-drive). 
  

  
## <a name="more-information"></a>Mais informações

- Envio de unidade é uma maneira eficaz para importar grandes quantidades de dados de arquivamento de mensagens para o Office 365 para aproveitar os recursos de conformidade que estão disponíveis para sua organização. Após os dados de arquivamento são importados para caixas de correio do usuário, você pode:
    
  - Habilite [caixas de correio de arquivo morto](enable-archive-mailboxes.md) e a [expansão automática de arquivamento](enable-unlimited-archiving.md) para dar aos usuários de espaço de armazenamento de caixa de correio adicional para os dados. 
    
  - Colocar caixas de correio em [Retenção de litígio](https://go.microsoft.com/fwlink/?linkid=856286) para reter os dados. 
    
  - Use [Ferramentas de descoberta eletrônica](search-for-content.md) da Microsoft para pesquisar os dados. 
    
  - Aplica [políticas de retenção do Office 365](retention-policies.md) para controlar quanto tempo os dados são mantidos e a ação que será executada depois que o período de retenção expira. 
    
  - Pesquisa o [log de auditoria do Office 365](search-the-audit-log-in-security-and-compliance.md) para eventos relacionados a esses dados. 
    
  - Importar dados para [caixas de correio inativas](create-and-manage-inactive-mailboxes.md) para arquivar dados para fins de conformidade. 
    
  - Protege sua organização contra [perda de dados](data-loss-prevention-policies.md) de informações confidenciais. 
    
- Veja um exemplo da chave da conta de armazenamento seguro e de uma chave de criptografia BitLocker. Este exemplo inclui também a sintaxe para o comando da ferramenta WAImportExport.exe executada para copiar arquivos PST no disco rígido. Não deixe de tomar medidas para proteger esse conteúdo, do mesmo modo que o faria com senhas ou outras informações relacionadas à segurança.
    

    ```
    Secure storage account key: 

    yaNIIs9Uy5g25Yoak+LlSHfqVBGOeNwjqtBEBGqRMoidq6/e5k/VPkjOXdDIXJHxHvNoNoFH5NcVUJXHwu9ZxQ==

    BitLocker encryption key:

    397386-221353-718905-535249-156728-127017-683716-083391

  COMMAND SYNTAX

  First time:

  WAImportExport.exe PrepImport /j:<Name of journal file> /t:<Drive letter> /id:<Name of session> /srcdir:<Location of PST files> /dstdir:<PST file path> /sk:<Storage account key> /encrypt /logdir:<Log file location>

  Subsequent times:

  WAImportExport.exe PrepImport /j:<Name of journal file> /id:<Name of new session> /srcdir:<Location of PST files> /dstdir:<PST file path> 

  EXAMPLES

  First time:

  WAImportExport.exe PrepImport /j:PSTHDD1.jrn /t:f /id:driveship1 /srcdir:"\\FILESERVER1\PSTs" /dstdir:"ingestiondata/" /sk:"yaNIIs9Uy5g25Yoak+LlSHfqVBGOeNwjqtBEBGqRMoidq6/e5k/VPkjOXdDIXJHxHvNoNoFH5NcVUJXHwu9ZxQ==" /encrypt /logdir:"c:\users\admin\desktop\PstImportLogs"

  Subsequent times:

  WAImportExport.exe PrepImport /j:PSTHDD1.jrn /id:driveship2 /srcdir:"\\FILESERVER1\PSTs\SecondBatch" /dstdir:"ingestiondata/"
    ```
   
- Conforme explicado anteriormente, o serviço de importação do Office 365 ativa a retenção de configuração (por um período indefinido) depois de arquivos PST são importados para uma caixa de correio. Isso significa que a propriedade *RentionHoldEnabled* estiver definida como `True` para que a política de retenção atribuída à caixa de correio não será processada. Isso permite que o tempo de proprietário da caixa de correio para gerenciar as mensagens recentemente importados, impedindo a execução uma exclusão ou a política de arquivamento de exclusão ou arquivamento de mensagens mais antigas. Aqui estão algumas etapas a que seguir para gerenciar esse status em retenção: 
    
  - Depois de certo período de tempo, você pode desativar o status em retenção, executando o `Set-Mailbox -RetentionHoldEnabled $false` comando. Para obter instruções, consulte [retenção local de uma caixa de correio em retenção](https://go.microsoft.com/fwlink/p/?LinkId=544749).
    
  - Você pode configurar o intervalo de retenção para que ele está desativado em alguns data no futuro. Você pode fazer isso executando o `Set-Mailbox -EndDateForRetentionHold <date>` comando. Por exemplo, supondo que a data de hoje é 1 de julho de 2016 e você quiser que o status em retenção desativado no 30 dias, execute o seguinte comando: `Set-Mailbox -EndDateForRetentionHold 8/1/2016`. Neste cenário, você poderia deixar a propriedade *RentionHoldEnabled* definida como *True* . Para obter mais informações, consulte [Set-Mailbox](https://go.microsoft.com/fwlink/p/?LinkId=150317).
    
  - Você pode alterar as configurações para a política de retenção que é atribuída à caixa de correio, de forma que os itens mais antigos que foram importados não ser imediatamente excluídos ou movidos para a caixa de correio de arquivo morto do usuário. Por exemplo, você pode aumentar a idade de retenção para uma política de exclusão ou arquivamento atribuída à caixa de correio. Neste cenário, você faria desativar a retenção suspensa na caixa de correio depois que você alterou as configurações da política de retenção. Para obter mais informações, consulte [Configurar uma política de arquivamento e exclusão de caixas de correio em sua organização do Office 365](set-up-an-archive-and-deletion-policy-for-mailboxes.md).
    

  


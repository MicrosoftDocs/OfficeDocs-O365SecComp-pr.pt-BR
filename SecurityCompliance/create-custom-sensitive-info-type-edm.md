---
title: 'Criar tipos personalizados de informações confidenciais com Exact Data Match '
ms.author: chrfox
author: chrfox
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.date: 05/15/2019
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Criar tipos personalizados de informações confidenciais com classificação baseada em Exact Data Match.
ms.openlocfilehash: be86f22ec20d36aaf12ae253028d0896f885267e
ms.sourcegitcommit: 7a0cb7e1da39fc485fc29e7325b843d16b9808af
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/07/2019
ms.locfileid: "36230835"
---
# <a name="create-custom-sensitive-information-types-with-exact-data-match-based-classification-preview"></a>Criar tipos personalizados de informações confidenciais com classificação baseada em Exact Data Match (visualização)

## <a name="overview"></a>Visão Geral

[Tipos personalizados de informações confidenciais](custom-sensitive-info-types.md) são usadas para ajudar a prevenir o compartilhamento acidental ou inadequado de informações confidenciais. Como administrador, você pode usar o [Centro de Conformidade e Segurança](create-a-custom-sensitive-information-type.md) ou [PowerShell](create-a-custom-sensitive-information-type-in-scc-powershell.md) para definir um tipo personalizado de informação confidencial baseado em padrões, evidenciar (palavras-chave como *funcionário*, *crachá*, *ID* e assim por diante), proximidade de caractere (como evidência está próxima de caracteres em um padrão específico) e níveis de confiança. Esses tipos personalizados de informações confidenciais atendem às necessidades comerciais de várias organizações.

Mas e se você quiser um tipo personalizado de informações confidenciais que usa valores de dados exatos, em vez de padrões e proximidade? Com a classificação baseada em Exact Data Match (EDM), você pode criar um tipo personalizado de informações confidenciais que é criada para:
- ser dinâmico e atualizável.
- ser mais escalonável;
- resultar em menos falso positivos.
- trabalhar com dados confidenciais estruturados;
- lidar com as informações confidenciais com mais segurança; e
- ser usado com vários serviços de nuvem da Microsoft.

![Classificação baseada em EDM](media/EDMClassification.png)

A classificação baseada no EDM permite criar tipos personalizados de informações confidenciais que fazem referência a valores exatos em um banco de dados de informações confidenciais. O banco de dados pode ser atualizado diariamente ou semanalmente, e pode conter até 10 milhões linhas de dados. Assim como funcionários, pacientes ou clientes vêm e vão e os registros são alterados, os tipos personalizados de informações confidenciais permanecem atualizados e aplicáveis. Você também pode usar a classificação baseada em EDM com políticas, como [políticas de prevenção contra perda de dados](data-loss-prevention-policies.md) (DLP) ou [políticas de arquivo do Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security/data-protection-policies).

## <a name="required-licenses-and-permissions"></a>Licenças e permissões necessárias

- Você deve ser um administrador global, administrador de conformidade ou administrador do Exchange Online para executar as tarefas descritas neste artigo. Para saber mais sobre permissões DLP, consulte [Permissões](data-loss-prevention-policies.md#permissions).

- Quando estiver disponível geralmente, a classificação baseada em EDM será incluída nas seguintes assinaturas:
    - Office 365 E5
    - Microsoft 365 E5
    - Proteção de Informações e Conformidade do Microsoft 365
    - Conformidade Avançada do Office 365

> [!NOTE]
> **Classificação baseada em EDM está atualmente em modo de visualização** para [DLP no Office 365](data-loss-prevention-policies.md) (com o Exchange Online e o Microsoft Teams) e o [Cloud App Security](https://docs.microsoft.com/cloud-app-security). Se a sua organização tiver [recursos DLP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description/messaging-policy-and-compliance-servicedesc#data-loss-prevention-dlp), você poderá testar a classificação baseada em EDM. Se você ainda não estiver participando da visualização, [contatar a Microsoft](https://resources.office.com/us-landing-spe-contactus.html?LCID=EN-US) para começar. 

## <a name="the-work-flow-at-a-glance"></a>Visão geral do fluxo de trabalho 

|Fase  |Requisitos  |
|---------|---------|
|[Parte 1: Configuração da classificação baseada em EDM](#part-1-set-up-edm-based-classification)<br/><br/>(conforme o necessário)<br/>- [Edite o Esquema de Banco de Dados](#editing-the-schema-for-edm-based-classification) <br/>- [Remova o esquema](#removing-the-schema-for-edm-based-classification) |– Acesso de leitura aos dados confidenciais<br/>– Esquema de banco de dados no formato. XML (exemplo fornecido)<br/>– Pacote de regras no formato. XML (exemplo fornecido)<br/>– Permissões de administrador ao Centro de Conformidade e Segurança (usando o PowerShell) |
|[Parte 2: indexação e carregamento de dados confidenciais](#part-2-index-and-upload-the-sensitive-data)<br/><br/>(conforme o necessário)<br/>[Atualize os dados](#refreshing-your-sensitive-information-database) |– Grupo de segurança personalizado e conta de usuário<br/>– Acesso de administrador local à máquina com o agente de carregamento do EDM<br/>– Acesso de leitura aos dados confidenciais<br/>– Processar e agendar a atualização de dados|
|[Parte 3: uso da classificação baseada em EDM com os serviços de nuvem da Microsoft](#part-3-use-edm-based-classification-with-your-microsoft-cloud-services) |– Sua assinatura com DLP do Office 365<br/>– Recurso de classificação baseada em EDM habilitado (na visualização) |

## <a name="part-1-set-up-edm-based-classification"></a>Parte 1: Configuração da classificação baseada em EDM

Definição e configuração da classificação baseada em EDM envolve o salvamento de dados confidenciais no formato .csv, a definição de um esquema para seu banco de dados de informações confidenciais, a criação de um pacote de regras e o carregamento do esquema e do pacote de regras.

### <a name="define-the-schema-for-your-database-of-sensitive-information"></a>Definição do esquema para seu banco de dados de informações confidenciais

1. Identifique as informações confidenciais que deseja usar. Exporte os dados para um aplicativo, como o Microsoft Excel, e salve o arquivo no formato .csv. O arquivo de dados pode incluir:

    - Até 10 milhões linhas de dados confidenciais
    - Até 32 colunas (campos) por fonte de dados

2. Estruture os dados confidenciais no arquivo .csv, de modo que a primeira linha inclui os nomes dos campos usados na classificação baseada em EDM. Você pode ter nomes de campo no arquivo .csv, como "CPF", "data de nascimento", "nome", "sobrenome" e assim por diante. Por exemplo, o arquivo. csv é chamado *PatientRecords.csv*, e suas colunas incluem *PatientID*, *número de prontuário médico*, *sobrenome*, *nome*, *CPF* e mais.

3. Defina o esquema para o banco de dados de informações confidenciais no formato .xml (semelhante ao nosso exemplo a seguir). Nomeie esse esquema do arquivo `edm.xml` e configure-o para cada coluna no banco de dados, há uma linha que usa a sintaxe `<Field name="" unique="" searchable=""/>`. 

    - Use nomes da coluna para valores de *nome do campo*.
    - Use *unique="true"* para os campos que contêm valores exclusivos (CPF, números de identificação, etc.); caso contrário, *unique="false"*.
    - Use *searchable="true"* para os campos pesquisáveis. Não especifique mais de cinco campos pesquisáveis por banco de dados. O restante deve ter *searchable="false"*.  

    Por exemplo, o arquivo .xml a seguir define o esquema para um banco de dados de registros de paciente, com cinco campos especificados como pesquisável: *PatientID*, *Número de prontuário médico*, *CPF*, *Telefone*, e *data de nascimento*. 
    
    (Você pode copiar, modificar e usar nosso exemplo.)
    
    ```<?xml version="1.0" encoding="utf-8"?>
    <EdmSchema xmlns="http://schemas.microsoft.com/office/2018/edm">
        <DataStore name="PatientRecords" description="Schema for patient records" version="1">
            <Field name="PatientID" unique="false" searchable="true" />
            <Field name="MRN" unique="false" searchable="true" />
            <Field name="FirstName" unique="false" searchable="false" />
            <Field name="LastName" unique="false" searchable="false" />
            <Field name="SSN" unique="false" searchable="true" />
            <Field name="Phone" unique="false" searchable="true" />
            <Field name="DOB" unique="false" searchable="true" />
            <Field name="Gender" unique="false" searchable="false" />
            <Field name="Address" unique="false" searchable="false" />
        </DataStore>
    </EdmSchema>
    ```

4. [Conecte-se ao PowerShell do Centro de Conformidade e Segurança do Office 365](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).

5. Para carregar o esquema do banco de dados, execute os seguintes cmdlets, um de cada vez:

    `$edmSchemaXml=Get-Content .\edm.xml -Encoding Byte -ReadCount 0`

    `New-DlpEdmSchema -FileData $edmSchemaXml -Confirm:$true`

    Você será solicitado a confirmar da seguinte maneira:

       Confirm
       Are you sure you want to perform this action?
       New EDM Schema for the data store 'patientrecords' will be imported.
       [Y] Yes  [A] Yes to All  [N] No  [L] No to All  [?] Help (default is "Y"):

    > [!TIP]
    > Se você quiser que as suas alterações ocorram sem confirmação, na Etapa 5, use este cmdlet: `New-DlpEdmSchema -FileData $edmSchemaXml`
    
Agora que o esquema para o seu banco de dados de informações confidenciais está definido, a próxima etapa é configurar um pacote de regras. Continue na seção [Configurar um pacote de regras](#set-up-a-rule-package).

#### <a name="editing-the-schema-for-edm-based-classification"></a>Editando o esquema para classificação baseada em EDM 

(Conforme necessário) Se você quiser fazer alterações em seu arquivo edm.xml, como alterar quais os campos usados para a classificação baseada em EDM, siga estas etapas:

1. Edite o seu arquivo edm.xml (este é o arquivo discutido na seção [Definir o esquema](#define-the-schema-for-your-database-of-sensitive-information) deste artigo).

2. [Conecte-se ao PowerShell do Centro de Conformidade e Segurança do Office 365](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).

3. Para atualizar o seu esquema do banco de dados, execute os seguintes cmdlets, um de cada vez:

    `$edmSchemaXml=Get-Content .\edm.xml -Encoding Byte -ReadCount 0`

    `Set-DlpEdmSchema -FileData $edmSchemaXml -Confirm:$true`

    Você será solicitado a confirmar da seguinte maneira:

       Confirm
       Are you sure you want to perform this action?
       EDM Schema for the data store 'patientrecords' will be updated.
       [Y] Yes  [A] Yes to All  [N] No  [L] No to All  [?] Help (default is "Y"):

    > [!TIP]
    > Se você quiser que as suas alterações ocorram sem confirmação, na Etapa 3, use este cmdlet: `Set-DlpEdmSchema -FileData $edmSchemaXml`

#### <a name="removing-the-schema-for-edm-based-classification"></a>Removendo o esquema para classificação baseada em EDM

(Conforme necessário) Se você quiser remover o esquema que está usando para classificação baseada em EDM, siga estas etapas:

1. [Conecte-se ao PowerShell do Centro de Conformidade e Segurança do Office 365](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).

2. Execute o seguinte cmdlet do PowerShell, substituindo o nome do repositório de dados de "patientrecords" pelo nome que você deseja remover:

    `Remove-DlpEdmSchema -Identity patientrecords`

     Você será solicitado a confirmar da seguinte maneira:
    
       Confirm
       Are you sure you want to perform this action?
       EDM Schema for the data store 'patientrecords' will be removed.
       [Y] Yes  [A] Yes to All  [N] No  [L] No to All  [?] Help (default is "Y"):
    
    > [!TIP]
    > Se você quiser que as suas alterações ocorram sem confirmação, na Etapa 2, use este cmdlet: `Remove-DlpEdmSchema -Identity patientrecords -Confirm:$false`

### <a name="set-up-a-rule-package"></a>Configurar um pacote de regras

1. Crie um pacote de regras no formato .xml (com codificação Unicode), semelhante ao exemplo a seguir. (Você pode copiar, modificar e usar nosso exemplo.) 

   Lembre-se do procedimento anterior onde o nosso esquema PatientRecords define cinco campos como pesquisáveis: *PatientID*, *MRN*, *SSN*, *Phone* e *DOB*. O nosso pacote de regras de exemplo inclui esses campos e faz referência ao arquivo de esquema do banco de dados (edm.xml), com um item *ExactMatch* por campo pesquisável. Considere o seguinte item ExactMatch:

   ```
    <ExactMatch id = "E1CC861E-3FE9-4A58-82DF-4BD259EAB371" patternsProximity = "300" dataStore ="PatientRecords" recommendedConfidence = "65" >
      <Pattern confidenceLevel="65">
        <idMatch matches = "SSN" classification = "U.S. Social Security Number (SSN)" />
      </Pattern>
    </ExactMatch>
   ```

    Neste exemplo, observe o seguinte:

    - O nome do dataStore faz referência ao arquivo .csv que criamos anteriormente: **dataStore = "PatientRecords"**.
    - O valor idMatch faz referência a um campo pesquisável listado no arquivo de esquema do banco de dados: **idMatch matches = "SSN"**.
    - O valor de classificação faz referência a um tipo de informação confidencial existente ou personalizada: **classification = "Número de Seguridade Social dos EUA (SSN)"**. (Nesse caso, usamos o tipo de informação confidencial existente do Número de Seguridade Social dos EUA.)

    Ao configurar o seu pacote de regras, certifique-se de referenciar corretamente o arquivo .csv e o arquivo edm.xml. (Você pode copiar, modificar e usar nosso exemplo.) 

    ```<?xml version="1.0" encoding="utf-8"?>
    <RulePackage xmlns="http://schemas.microsoft.com/office/2018/edm">
      <RulePack id="fd098e03-1796-41a5-8ab6-198c93c62b11">
        <Version build="0" major="2" minor="0" revision="0" />
        <Publisher id="eb553734-8306-44b4-9ad5-c388ad970528" />
        <Details defaultLangCode="en-us">
          <LocalizedDetails langcode="en-us">
            <PublisherName>IP DLP</PublisherName>
            <Name>Health Care EDM Rulepack</Name>
            <Description>This rule package contains the EDM sensitive type for health care sensitive types.</Description>
          </LocalizedDetails>
        </Details>
      </RulePack>
      <Rules>
        <ExactMatch id = "E1CC861E-3FE9-4A58-82DF-4BD259EAB371" patternsProximity = "300" dataStore ="PatientRecords" recommendedConfidence = "65" >
          <Pattern confidenceLevel="65">
            <idMatch matches = "SSN" classification = "U.S. Social Security Number (SSN)" />
          </Pattern>
          <Pattern confidenceLevel="75">
            <idMatch matches = "SSN" classification = "U.S. Social Security Number (SSN)" />
            <Any minMatches ="3" maxMatches ="100">
              <match matches="PatientID" />
              <match matches="MRN"/>
              <match matches="FirstName"/>
              <match matches="LastName"/>
              <match matches="Phone"/>
              <match matches="DOB"/>
            </Any>
          </Pattern>
        </ExactMatch>
        <LocalizedStrings>
          <Resource idRef="E1CC861E-3FE9-4A58-82DF-4BD259EAB371">
            <Name default="true" langcode="en-us">Patient SSN Exact Match.</Name>
            <Description default="true" langcode="en-us">EDM Sensitive type for detecting Patient SSN.</Description>
          </Resource>
        </LocalizedStrings>
      </Rules>
    </RulePackage>
    ```
    
2. Carregue o pacote de regras executando os seguintes cmdlets do PowerShell, um de cada vez:

    `$rulepack=Get-Content .\rulepack.xml -Encoding Byte -ReadCount 0`

    `New-DlpSensitiveInformationTypeRulePackage -FileData $rulepack`

Nesse ponto, você configurou a classificação baseada em EDM. A próxima etapa é indexar os dados confidenciais e carregá-los. 

## <a name="part-2-index-and-upload-the-sensitive-data"></a>Parte 2: indexação e carregamento de dados confidenciais

Durante essa fase, você configura um grupo de segurança personalizado e uma conta de usuário, e configura a ferramenta do agente de carregamento do EDM. Depois indexe os dados confidenciais e carregá-los.

### <a name="set-up-the-security-group-and-user-account"></a>Configuração do grupo de segurança e conta de usuário

1. Como um administrador global, acesse o centro de administração ([https://admin.microsoft.com](https://admin.microsoft.com)) e [crie um grupo de segurança](https://docs.microsoft.com/office365/admin/email/create-edit-or-delete-a-security-group?view=o365-worldwide) chamado `EDM_DataUploaders`. 

2. Adicione um ou mais usuários ao grupo de segurança *EDM_DataUploaders*. (Esses usuários vão gerenciar o banco de dados de informações confidenciais.)

3. Certifique-se de que todos os usuários que estão gerenciando os dados confidenciais sejam um administrador local no computador usado para o agente de carregamento do EDM.

### <a name="set-up-the-edm-upload-agent"></a>Configurar o agente de carregamento do EDM

> [!NOTE]
> Antes de iniciar esse procedimento, certifique-se de que você é um membro do grupo de segurança *EDM_DataUploaders* e de um administrador local no computador.

1. Baixe e instale o agente de carregamento do EDM em [https://go.microsoft.com/fwlink/?linkid=2088639](https://go.microsoft.com/fwlink/?linkid=2088639). Por padrão, o local de instalação do deve ser `C:\Program Files\Microsoft\EdmUploadAgent`. 

2. Para autorizar o agente de carregamento do EDM, abra o prompt de comando do Windows (como um administrador) e execute o seguinte comando:

    `EdmUploadAgent.exe /Authorize`

3. Entre com sua conta corporativa ou de estudante do Office 365.

A próxima etapa é usar o agente de carregamento do EDM para indexar os dados confidenciais e depois carregá-los.

### <a name="index-and-upload-the-sensitive-data"></a>Indexação e carregamento de dados confidenciais

1. Salve o arquivo de dados confidenciais (Lembre-se de que o nosso exemplo é *PatientRecords.csv*) para a unidade local no computador. (Salvamos o arquivo do nosso exemplo *PatientRecords.csv* em `C:\Edm\Data`.)

2. Para indexar os dados confidenciais, execute o seguinte comando no prompt de comando do Windows:

    `EdmUploadAgent.exe /CreateHash /DataStoreName <DataStoreName> /DataFile <DataFilePath> /HashLocation <HashedFileLocation>`

    Exemplo: **EdmUploadAgent.exe /CreateHash /DataStoreName PatientRecords /DataFile C:\Edm\Data\PatientRecords.csv /HashLocation C:\Edm\Hash** 

3. Para indexar os dados indexados, execute o seguinte comando no prompt de comando do Windows:

    `EdmUploadAgent.exe /UploadHash /DataStoreName <DataStoreName> /HashFile <HashedSourceFilePath>`

    Exemplo: **EdmUploadAgent.exe /UploadHash /DataStoreName PatientRecords /HashFile C:\Edm\Hash\PatientRecords.EdmHash** 

4. Para verificar os dados confidenciais indexados, execute o seguinte comando no prompt de comando do Windows:

    `EdmUploadAgent.exe /GetDataStore`

    Você verá uma lista de repositórios de dados e a data da última atualização, similar à seguinte: <br/>![Exemplo de um cmdlet e resultado de GetDataStore](media/EDM-GetDataStore-example.png)

5. Prossiga para configurar seu processo e cronograma da [Atualização de banco de dados de informação confidencial](#refreshing-your-sensitive-information-database).

Nesse ponto, você já usou a classificação baseada em EDM com os serviços de nuvem da Microsoft. Por exemplo, você pode [configurar uma política usando a classificação baseada em EDM](#to-create-a-dlp-policy-with-edm). 

### <a name="refreshing-your-sensitive-information-database"></a>Atualização do banco de dados de informações confidenciais

Você pode atualizar seu banco de dados confidenciais diariamente ou semanalmente, e a ferramenta de carregamento do EDM pode reindexar os dados confidenciais e depois recarregar os dados indexados. 

1. Determine seu processo e a frequência (diariamente ou semanalmente) para atualização do banco de dados de informações confidenciais.

2. Exporte novamente os dados confidenciais para um aplicativo, como o Microsoft Excel, e salve o arquivo no formato .csv. Mantenha o mesmo nome do arquivo e o local que você usou ao seguir as etapas descritas em [indexação e carregamento de dados confidenciais](#index-and-upload-the-sensitive-data).

    > [!NOTE]
    > Se não houver alterações na estrutura (nomes de campos) do arquivo .csv, você não precisará fazer alterações no arquivo de esquema do banco de dados ao atualizar os dados. Mas se for necessário fazer alterações, não deixe de editar o [esquema de banco de dados](#editing-the-schema-for-edm-based-classification) e seu [pacote de regra](#set-up-a-rule-package) correspondente.        

3. Use o [Agendador de tarefas](https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page) para automatizar as etapas 2 e 3 no procedimento de [indexação e carregamento de dados confidenciais](#index-and-upload-the-sensitive-data). Você pode agendar tarefas usando vários métodos:
    
    |Método  |O que fazer  |
    |---------|---------|
    |Windows PowerShell     |Confira a documentação do [ScheduledTasks](https://docs.microsoft.com/powershell/module/scheduledtasks/?view=win10-ps) e o [exemplo do script do PowerShell](#example-powershell-script-for-task-scheduler) neste artigo|
    |API do Agendador de Tarefas |Confira a documentação do [Agendador de tarefas](https://docs.microsoft.com/windows/desktop/TaskSchd/using-the-task-scheduler) |
    |Interface do usuário do Windows     |No Windows, clique em **Iniciar** e insira `Task Scheduler`. Em seguida, na lista de resultados, clique com o botão direito do mouse no **Agendador de Tarefas**, e escolha **executar como administrador**.          |

#### <a name="example-powershell-script-for-task-scheduler"></a>Exemplo de script do PowerShell para o Agendador de Tarefas

Esta seção inclui um exemplo de script do PowerShell que pode ser usado para agendar as tarefas de indexação de dados e carregamento dos dados indexados:

```powershell
param([string]$dataStoreName,[string]$fileLocation)
# Assuming current user is also the user context to run the task
$user = "$env:USERDOMAIN\$env:USERNAME"
$edminstallpath = 'C:\Program Files\Microsoft\EdmUploadAgent\'
$edmuploader = $edminstallpath + 'EdmUploadAgent.exe'
$csvext = '.csv'
$edmext = '.EdmHash'
# Assuming CSV file name is same as data store name
$dataFile = "$fileLocation\$dataStoreName$csvext"
$hashFile = "$fileLocation\$dataStoreName$edmext"
# Assuming location to store hash file is same as the location of csv file
$hashLocation = $fileLocation
$createHashArgs = '/CreateHash /DataStoreName ' + $dataStoreName + ' /DataFile ' + $dataFile + ' /HashLocation ' + $hashLocation
$uploadHashArgs = '/UploadHash /DataStoreName ' + $dataStoreName + ' /HashFile ' + $hashFile
# Set up actions associated with the task
$actions = @()
$actions += New-ScheduledTaskAction -Execute $edmuploader -Argument $createHashArgs -WorkingDirectory $edminstallpath
$actions += New-ScheduledTaskAction -Execute $edmuploader -Argument $uploadHashArgs -WorkingDirectory $edminstallpath
# Set up trigger for the task
$trigger = New-ScheduledTaskTrigger -Weekly -DaysOfWeek Sunday -At 2am
# Set up task settings
$principal = New-ScheduledTaskPrincipal -UserId $user -LogonType S4U -RunLevel Highest
$settings = New-ScheduledTaskSettingsSet -RunOnlyIfNetworkAvailable -StartWhenAvailable -WakeToRun
# Create the scheduled task
$scheduledTask = New-ScheduledTask -Action $actions -Principal $principal -Trigger $trigger -Settings $settings
# Get credentials to run the task
$creds = Get-Credential -UserName $user -Message "Enter credentials to run the task"
$password=[Runtime.InteropServices.Marshal]::PtrToStringAuto([Runtime.InteropServices.Marshal]::SecureStringToBSTR($creds.Password))
# Register the scheduled task
$taskName = 'EDMUpload_' + $dataStoreName
Register-ScheduledTask -TaskName $taskName -InputObject $scheduledTask -User $user -Password $password
```
## <a name="part-3-use-edm-based-classification-with-your-microsoft-cloud-services"></a>Parte 3: uso da classificação baseada em EDM com os serviços de nuvem da Microsoft

Você também pode usar a classificação baseada em EDM como [políticas de DLP do Office 365](data-loss-prevention-policies.md) e [políticas de arquivo do Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security/data-protection-policies). O procedimento a seguir descreve como usar o EDM com uma política DLP criada no Centro de Conformidade & Segurança do Office 365.

### <a name="to-create-a-dlp-policy-with-edm"></a>Criação de uma política DLP com o EDM

1. Acesse o Centro de Conformidade e Segurança ([https://protection.office.com](https://protection.office.com)).

2. Clique em **Prevenção contra perda de dados** > **Política**.

3. Escolha **Criar uma política** > **Personalizar** > **Próximo**.

4. Na guia **Nomear sua política**, especifique um nome e uma descrição e, em seguida, escolha **Próximo**. 

5. Na guia **Escolher locais**, clique em **Escolher locais específicos** e, em seguida, clique em **Próximo**.<br/>![Opção escolher locais](media/DLP-EDM-newpolicy-chooselocations.png)<br/>

6. Na coluna **Status**, selecione somente **email do Exchange** e, em seguida, clique em **Próximo**. <br/>![Política EDM somente com o Exchange](media/EDM-DLPpolicy-ExchangeOnly.png)<br/>

7. Na guia **configurações de política**, escolha **usar configurações avançadas** e, em seguida, clique em **Próximo**.<br/>![Usar configurações avançadas](media/edm-dlp-policy-advancedsettings.png)<br/>

8. Escolha **+ nova regra**.<br/>![Criar uma regra](media/edm-dlp-newrule.png)<br/>

9. Na seção **Nome**, especifique um nome e uma descrição para a regra.<br/>![Campos de nova regra](media/edm-dlp-newruleform.png)<br/>

10. Na seção **Condições**, na lista **+ adicionar uma condição**, escolha **conteúdo contém tipo diferencial**.<br/>![Conteúdo tem tipos de informações confidenciais](media/edm-dlp-newrule-conditions.png)<br/>

11. Pesquise pelo tipo de informação confidencial que você criou ao configurar o pacote de regras e, em seguida, escolha **+ adicionar**.<br/>![Encontrar tipo de informação confidencial](media/edm-dlp-newrulefindsensitiverulepack.png)<br/>Depois escolha **Concluído**.

12. Termine de selecionar as opções para a regra, como **Notificações de usuário**, **Substituições do usuário**, **Relatórios de incidente**, e assim por diante, e depois clique em **Salvar**.

13. Na guia **Configurações de política**, revise suas regras e, em seguida, clique em **Próximo**.

14. Especifique se deseja ativar a política imediatamente, testá-la ou desativá-la. Depois clique em **Próximo**.

15. Na guia **Revisar suas configurações**, revise sua política. Faça todas as alterações necessárias. Quando concluir, clique em **Criar**.

    > [!NOTE]
    > Espere aproximadamente uma hora para sua nova política DLP funcionar em seu data center.

## <a name="related-articles"></a>Artigos relacionados

[Tipos de informações confidenciais integradas e o que procuram](what-the-sensitive-information-types-look-for.md)

[Tipos personalizados de informações confidenciais](custom-sensitive-info-types.md)

[Visão geral das políticas DLP](data-loss-prevention-policies.md)

[Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security)

---
title: Contatos externos do importação em massa para o Exchange Online
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: End User
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOP150
ms.assetid: bed936bc-0969-4a6d-a7a5-66305c14e958
description: Saiba como os administradores podem usar o PowerShell do Exchange Online e um arquivo CSV para em massa importar contatos externos à lista de endereços global.
ms.openlocfilehash: 4bde56d49ccf94dc91993df90e1ae693e25c961a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523543"
---
# <a name="bulk-import-external-contacts-to-exchange-online"></a>Contatos externos do importação em massa para o Exchange Online

**Este artigo destina-se a administradores. Você está tentando importar contatos à sua própria caixa de correio? Consulte [Importar contatos para o Outlook](https://support.office.com/article/bb796340-b58a-46c1-90c7-b549b8f3c5f8)**
   
Sua empresa possuem muitos contatos de negócios existentes que você deseja incluir no catálogo de endereços compartilhado (também chamado de lista de endereços global) no Exchange Online? Você deseja adicionar contatos externos como membros de grupos de distribuição, como se faz com que os usuários dentro da sua empresa? Se assim, você pode usar o PowerShell do Exchange Online e um arquivo CSV (valores separados por vírgula) em massa importe contatos externos para o Exchange Online. É um processo de três etapas:
  
[Etapa 1: Criar um arquivo CSV que contém informações sobre os contatos externos](#step-1-create-a-csv-file-that-contains-information-about-the-external-contacts)

[Etapa 2: Criar os contatos externos com o PowerShell](#step-2-create-the-external-contacts-with-powershell) 

[Etapa 3: Adicionar informações às propriedades dos contatos externos](#step-3-add-information-to-the-properties-of-the-external-contacts)

Após concluir estas etapas para importar contatos, você pode executar estas tarefas adicionais:
  
- [Adicionar contatos mais externos](bulk-import-external-contacts.md#AddMore)
  
- [Ocultar contatos externos do catálogo de endereços compartilhado](bulk-import-external-contacts.md#Hide)
  
## <a name="step-1-create-a-csv-file-that-contains-information-about-the-external-contacts"></a>Etapa 1: Criar um arquivo CSV que contém informações sobre os contatos externos

A primeira etapa é criar um arquivo CSV que contém informações sobre cada contato externo que você deseja importar para o Exchange Online. 
  
1. Copie o seguinte texto em um arquivo de texto no bloco de notas e salve-o em sua área de trabalho como um arquivo CSV usando um sufixo de nome de arquivo de. csv; Por exemplo, ExternalContacts.csv.
    
    > [!TIP]
    > Se seu idioma contém caracteres especiais (por exemplo, **å**, **ä**e **ö** em sueco) salvar o arquivo CSV com codificação UTF-8 ou outra codificação Unicode quando você salva o arquivo no bloco de notas. 
  
    ```
    ExternalEmailAddress,Name,FirstName,LastName,StreetAddress,City,StateorProvince,PostalCode,Phone,MobilePhone,Pager,HomePhone,Company,Title,OtherTelephone,Department,CountryOrRegion,Fax,Initials,Notes,Office,Manager
    danp@fabrikam.com,Dan Park,Dan,Park,1234 23rd Ave,Golden,CO,80215,206-111-1234,303-900-1234,555-1212,123-456-7890,Fabrikam,Shipping clerk,555-5555,Shipping,US,123-4567,R.,Good worker,31/1663,Dan Park
    pilar@contoso.com,Pilar Pinilla,Pilar,Pinilla,1234 Main St.,Seattle,WA,98017,206-555-0100,206-555-0101,206-555-0102,206-555-1234,Contoso,HR Manager,206-555-0104,Executive,US,206-555-0105,P.,Technical decision maker,31/1000,Dan Park 
    ```

    A primeira linha ou a linha de cabeçalho do arquivo CSV relaciona as propriedades de contatos que podem ser usadas quando você importá-los para o Exchange Online. O nome de cada propriedade é separado por uma vírgula. Cada linha sob a linha de cabeçalho representa os valores de propriedade para a importação de um único contato externo. 
    
    > [!NOTE]
    > Esse texto inclui os dados de exemplo, você pode excluir. Mas não exclua ou altere a primeira linha (cabeçalho). Ele contém todas as propriedades para os contatos externos. 
  
2. Abra o arquivo CSV no Microsoft Excel para editar o arquivo CSV, porque ele é muito mais fácil usar o Excel para editar o arquivo CSV.
    
3. Crie uma linha para cada contato que você deseja importar para o Exchange Online. Preencha como muitas das células possível. Essa informação será exibida no catálogo de endereços compartilhado para cada contato. 
    
    > [!IMPORTANT]
    >  As seguintes propriedades (que são os quatro primeiros itens na linha de cabeçalho) são necessárias para criar um contato externo e devem ser preenchidas em um arquivo CSV: **ExternalEmailAddress**, **nome**, **FirstName**, **LastName**. O comando do PowerShell que você executar na etapa 2 usará os valores para essas propriedades para criar os contatos. 

## <a name="step-2-create-the-external-contacts-with-powershell"></a>Etapa 2: Criar os contatos externos com o PowerShell

A próxima etapa é usar o arquivo CSV que você criou na etapa 1 e PowerShell para em massa importar os contatos externos listados no arquivo CSV para o Exchange Online. 
  
1.  Conecte o PowerShell para sua organização do Exchange Online. Para obter instruções detalhadas, consulte [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554). Certifique-se de usar o nome de usuário e senha para sua conta de administrador global do Office 365, quando você se conectar ao PowerShell do Exchange Online. 
    
2. Depois de conectar o PowerShell para o Exchange Online, vá para a pasta área de trabalho onde você salvou o arquivo CSV na etapa 1; Por exemplo `C:\Users\Administrator\desktop`.
    
3. Execute o seguinte comando para criar os contatos externos:

    ```
    Import-Csv .\ExternalContacts.csv|%{New-MailContact -Name $_.Name -DisplayName $_.Name -ExternalEmailAddress $_.ExternalEmailAddress -FirstName $_.FirstName -LastName $_.LastName}
    ```

    Ela pode levar algum tempo para criar os novos contatos, dependendo de quantos você está importando. Quando o comando estiver concluído em execução, PowerShell exibe uma lista dos novos contatos que foram criados. 
    
4. Para exibir os novos contatos externos, vá para o Centro de administração do Exchange (EAC) e, em seguida, clique em **destinatários** \> **Contatos**. 
    
    > [!TIP]
    > Para obter instruções para conectar-se ao EAC, consulte [Exchange admin center no Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=328197). 
  
5. Se necessário, clique em **Atualizar** ![ícone atualizar](media/O365-MDM-Policy-RefreshIcon.gif) para atualizar a lista e ver os contatos externos que foram importados. 
    
    Os contatos importados aparecerá no catálogo de endereços compartilhado no Outlook e Outlook na web.
    
    > [!NOTE]
    > Você também pode exibir os contatos no Centro de administração do Office 365 indo para **usuários** \> **Contatos**. 

## <a name="step-3-add-information-to-the-properties-of-the-external-contacts"></a>Etapa 3: Adicionar informações às propriedades dos contatos externos

Depois de executar o comando na etapa 2, os contatos externos são criados, mas não contêm as informações de contato ou da organização, que é a informação de que a maioria das células no arquivo CSV. Isso ocorre porque quando você cria novos contatos externos, somente as propriedades necessárias são preenchidas. Não se preocupe se você não possui todas as informações preenchidas no arquivo CSV. Se não estiver, ele não ser adicionado.
  
1.  Conecte o PowerShell para sua organização do Exchange Online. Para obter instruções detalhadas, consulte [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).
    
2. Vá para a pasta área de trabalho onde você salvou o arquivo CSV na etapa 1; Por exemplo `C:\Users\Administrator\desktop`.
    
3. Execute os dois comandos a seguir para adicionar outras propriedades de arquivo CSV para os contatos externos que você criou na etapa 2.
    
    ```
    $Contacts = Import-CSV .\ExternalContacts.csv
  
    ```

    ```
    $contacts | ForEach {Set-Contact $_.Name -StreetAddress $_.StreetAddress -City $_.City -StateorProvince $_.StateorProvince -PostalCode $_.PostalCode -Phone $_.Phone -MobilePhone $_.MobilePhone -Pager $_.Pager -HomePhone $_.HomePhone -Company $_.Company -Title $_.Title -OtherTelephone $_.OtherTelephone -Department $_.Department -Fax $_.Fax -Initials $_.Initials -Notes  $_.Notes -Office $_.Office -Manager $_.Manager}
    ```

    > [!NOTE]
    > O parâmetro _Manager_ pode ser problemático. Se a célula estiver em branco no arquivo CSV, você receberá um erro e nenhuma das informações de propriedade será adicionada ao contato. Se você não precisa especificar um gerente, basta excluir ` -Manager $_.Manager ` do comando PowerShell anterior. 
  
    Novamente, ela pode levar algum tempo para atualizar os contatos, dependendo de quantos você importou na etapa 1. 
    
4. Para verificar se as propriedades foram adicionadas aos contatos: 
    
1. No EAC, acesse **Destinatários** \> **Contatos**.
    
2. Clique em um contato e clique em **Editar** ![ícone Editar](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) para exibir as propriedades do contato. 
    
Isso é tudo! Os usuários podem ver os contatos e as informações adicionais no catálogo de endereços do Outlook e o Outlook na web.
  
## <a name="add-more-external-contacts"></a>Adicionar contatos mais externos

Você pode repetir as etapas de 1 a etapa 3 para adicionar novos contatos externos no Exchange Online. Usuários da sua empresa ou você podem adicionar apenas uma nova linha no arquivo CSV para o novo contato. Em seguida, você pode executar os comandos do PowerShell da etapa 2 e etapa 3 para criar e adicionar informações aos novos contatos.
  
> [!NOTE]
> Quando você executar o comando para criar novos contatos, você pode obter um erro dizendo que os contatos que foram criados anteriormente, já existem. Mas qualquer novo contato adicionado ao arquivo CSV é criado. 
  
## <a name="hide-external-contacts-from-the-shared-address-book"></a>Ocultar contatos externos do catálogo de endereços compartilhado >

Algumas empresas podem usar os contatos externos só para que eles podem ser adicionados como membros de grupos de distribuição. Neste cenário, eles talvez queira ocultar contatos externos do catálogo de endereços compartilhado. Veja como:
  
1.  Conecte o PowerShell para sua organização do Exchange Online. Para obter instruções detalhadas, consulte [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).
    
2. Para ocultar um único contato externo, execute o seguinte comando.
    
    ```
    Set-MailContact <external contact> -HiddenFromAddressListsEnabled $true 
    ```
 
    Por exemplo, para ocultar Pilar Pinilla do catálogo de endereços compartilhado, execute este comando:

    ```
    Set-MailContact "Pilar Pinilla" -HiddenFromAddressListsEnabled $true
    ```
   
3. Para ocultar todos os contatos externos do catálogo de endereços compartilhado, execute este comando:

    ```
    Get-Contact -ResultSize unlimited -Filter {(RecipientTypeDetails -eq 'MailContact')} | Set-MailContact -HiddenFromAddressListsEnabled $true  
    ```

Depois de você ocultá-las, contatos externos não são exibidos no catálogo de endereços compartilhado, mas você ainda poderá adicioná-los como membros de um grupo de distribuição.

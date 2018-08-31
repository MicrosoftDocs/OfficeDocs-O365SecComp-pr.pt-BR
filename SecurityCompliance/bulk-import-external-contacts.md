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
# <a name="bulk-import-external-contacts-to-exchange-online"></a><span data-ttu-id="d3720-103">Contatos externos do importação em massa para o Exchange Online</span><span class="sxs-lookup"><span data-stu-id="d3720-103">Bulk import external contacts to Exchange Online</span></span>

<span data-ttu-id="d3720-104">**Este artigo destina-se a administradores. Você está tentando importar contatos à sua própria caixa de correio? Consulte [Importar contatos para o Outlook](https://support.office.com/article/bb796340-b58a-46c1-90c7-b549b8f3c5f8)**</span><span class="sxs-lookup"><span data-stu-id="d3720-104">**This article is for administrators. Are you trying to import contacts to your own mailbox? See [Import contacts to Outlook](https://support.office.com/article/bb796340-b58a-46c1-90c7-b549b8f3c5f8)**</span></span>
   
<span data-ttu-id="d3720-p101">Sua empresa possuem muitos contatos de negócios existentes que você deseja incluir no catálogo de endereços compartilhado (também chamado de lista de endereços global) no Exchange Online? Você deseja adicionar contatos externos como membros de grupos de distribuição, como se faz com que os usuários dentro da sua empresa? Se assim, você pode usar o PowerShell do Exchange Online e um arquivo CSV (valores separados por vírgula) em massa importe contatos externos para o Exchange Online. É um processo de três etapas:</span><span class="sxs-lookup"><span data-stu-id="d3720-p101">Does your company have lots of existing business contacts that you want to include in the shared address book (also called the global address list) in Exchange Online? Do you want to add external contacts as members of distribution groups, just like you can with users inside your company? If so, you can use Exchange Online PowerShell and a CSV (Comma Separated Value) file to bulk import external contacts into Exchange Online. It's a three-step process:</span></span>
  
[<span data-ttu-id="d3720-109">Etapa 1: Criar um arquivo CSV que contém informações sobre os contatos externos</span><span class="sxs-lookup"><span data-stu-id="d3720-109">Step 1: Create a CSV file that contains information about the external contacts</span></span>](#step-1-create-a-csv-file-that-contains-information-about-the-external-contacts)

[<span data-ttu-id="d3720-110">Etapa 2: Criar os contatos externos com o PowerShell</span><span class="sxs-lookup"><span data-stu-id="d3720-110">Step 2: Create the external contacts with PowerShell</span></span>](#step-2-create-the-external-contacts-with-powershell) 

[<span data-ttu-id="d3720-111">Etapa 3: Adicionar informações às propriedades dos contatos externos</span><span class="sxs-lookup"><span data-stu-id="d3720-111">Step 3: Add information to the properties of the external contacts</span></span>](#step-3-add-information-to-the-properties-of-the-external-contacts)

<span data-ttu-id="d3720-112">Após concluir estas etapas para importar contatos, você pode executar estas tarefas adicionais:</span><span class="sxs-lookup"><span data-stu-id="d3720-112">After you complete these steps to import contacts, you can perform these additional tasks:</span></span>
  
- [<span data-ttu-id="d3720-113">Adicionar contatos mais externos</span><span class="sxs-lookup"><span data-stu-id="d3720-113">Add more external contacts</span></span>](bulk-import-external-contacts.md#AddMore)
  
- [<span data-ttu-id="d3720-114">Ocultar contatos externos do catálogo de endereços compartilhado</span><span class="sxs-lookup"><span data-stu-id="d3720-114">Hide external contacts from the shared address book</span></span>](bulk-import-external-contacts.md#Hide)
  
## <a name="step-1-create-a-csv-file-that-contains-information-about-the-external-contacts"></a><span data-ttu-id="d3720-115">Etapa 1: Criar um arquivo CSV que contém informações sobre os contatos externos</span><span class="sxs-lookup"><span data-stu-id="d3720-115">Step 1: Create a CSV file that contains information about the external contacts</span></span>

<span data-ttu-id="d3720-116">A primeira etapa é criar um arquivo CSV que contém informações sobre cada contato externo que você deseja importar para o Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="d3720-116">The first step is to create a CSV file that contains information about each external contact that you want to import to Exchange Online.</span></span> 
  
1. <span data-ttu-id="d3720-117">Copie o seguinte texto em um arquivo de texto no bloco de notas e salve-o em sua área de trabalho como um arquivo CSV usando um sufixo de nome de arquivo de. csv; Por exemplo, ExternalContacts.csv.</span><span class="sxs-lookup"><span data-stu-id="d3720-117">Copy the following text to a text file in NotePad, and save it to your desktop as a CSV file by using a filename suffix of .csv; for example, ExternalContacts.csv.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="d3720-118">Se seu idioma contém caracteres especiais (por exemplo, **å**, **ä**e **ö** em sueco) salvar o arquivo CSV com codificação UTF-8 ou outra codificação Unicode quando você salva o arquivo no bloco de notas.</span><span class="sxs-lookup"><span data-stu-id="d3720-118">If your language contains special characters (such as **å**, **ä**, and **ö** in Swedish) save the CSV file with UTF-8 or other Unicode encoding when you save the file in NotePad.</span></span> 
  
    ```
    ExternalEmailAddress,Name,FirstName,LastName,StreetAddress,City,StateorProvince,PostalCode,Phone,MobilePhone,Pager,HomePhone,Company,Title,OtherTelephone,Department,CountryOrRegion,Fax,Initials,Notes,Office,Manager
    danp@fabrikam.com,Dan Park,Dan,Park,1234 23rd Ave,Golden,CO,80215,206-111-1234,303-900-1234,555-1212,123-456-7890,Fabrikam,Shipping clerk,555-5555,Shipping,US,123-4567,R.,Good worker,31/1663,Dan Park
    pilar@contoso.com,Pilar Pinilla,Pilar,Pinilla,1234 Main St.,Seattle,WA,98017,206-555-0100,206-555-0101,206-555-0102,206-555-1234,Contoso,HR Manager,206-555-0104,Executive,US,206-555-0105,P.,Technical decision maker,31/1000,Dan Park 
    ```

    <span data-ttu-id="d3720-p102">A primeira linha ou a linha de cabeçalho do arquivo CSV relaciona as propriedades de contatos que podem ser usadas quando você importá-los para o Exchange Online. O nome de cada propriedade é separado por uma vírgula. Cada linha sob a linha de cabeçalho representa os valores de propriedade para a importação de um único contato externo.</span><span class="sxs-lookup"><span data-stu-id="d3720-p102">The first row, or header row, of the CSV file lists the properties of contacts that can be used when you import them to Exchange Online. Each property name is separated by a comma. Each row under the header row represents the property values for importing a single external contact.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="d3720-p103">Esse texto inclui os dados de exemplo, você pode excluir. Mas não exclua ou altere a primeira linha (cabeçalho). Ele contém todas as propriedades para os contatos externos.</span><span class="sxs-lookup"><span data-stu-id="d3720-p103">This text includes sample data, which you can delete. But don't delete or change the first (header) row. It contains all of the properties for the external contacts.</span></span> 
  
2. <span data-ttu-id="d3720-125">Abra o arquivo CSV no Microsoft Excel para editar o arquivo CSV, porque ele é muito mais fácil usar o Excel para editar o arquivo CSV.</span><span class="sxs-lookup"><span data-stu-id="d3720-125">Open the CSV file in Microsoft Excel to edit the CSV file because it's much easier to use Excel to edit the CSV file.</span></span>
    
3. <span data-ttu-id="d3720-p104">Crie uma linha para cada contato que você deseja importar para o Exchange Online. Preencha como muitas das células possível. Essa informação será exibida no catálogo de endereços compartilhado para cada contato.</span><span class="sxs-lookup"><span data-stu-id="d3720-p104">Create a row for each contact that you want to import to Exchange Online. Populate as many of the cells as possible. This information will be displayed in the shared address book for each contact.</span></span> 
    
    > [!IMPORTANT]
    >  <span data-ttu-id="d3720-p105">As seguintes propriedades (que são os quatro primeiros itens na linha de cabeçalho) são necessárias para criar um contato externo e devem ser preenchidas em um arquivo CSV: **ExternalEmailAddress**, **nome**, **FirstName**, **LastName**. O comando do PowerShell que você executar na etapa 2 usará os valores para essas propriedades para criar os contatos.</span><span class="sxs-lookup"><span data-stu-id="d3720-p105">The following properties (which are the first four items in the header row) are required to create an external contact and must be populated in the CSV file: **ExternalEmailAddress**, **Name**, **FirstName**, **LastName**. The PowerShell command that you run in Step 2 will use the values for these properties to create the contacts.</span></span> 

## <a name="step-2-create-the-external-contacts-with-powershell"></a><span data-ttu-id="d3720-131">Etapa 2: Criar os contatos externos com o PowerShell</span><span class="sxs-lookup"><span data-stu-id="d3720-131">Step 2: Create the external contacts with PowerShell</span></span>

<span data-ttu-id="d3720-132">A próxima etapa é usar o arquivo CSV que você criou na etapa 1 e PowerShell para em massa importar os contatos externos listados no arquivo CSV para o Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="d3720-132">The next step is to use the CSV file that you created in Step 1 and PowerShell to bulk import the external contacts listed in the CSV file to Exchange Online.</span></span> 
  
1.  <span data-ttu-id="d3720-p106">Conecte o PowerShell para sua organização do Exchange Online. Para obter instruções detalhadas, consulte [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554). Certifique-se de usar o nome de usuário e senha para sua conta de administrador global do Office 365, quando você se conectar ao PowerShell do Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="d3720-p106">Connect PowerShell to your Exchange Online organization. For step-by-step instructions, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554). Be sure to use the user name and password for your Office 365 global administrator account when you connect to Exchange Online PowerShell.</span></span> 
    
2. <span data-ttu-id="d3720-136">Depois de conectar o PowerShell para o Exchange Online, vá para a pasta área de trabalho onde você salvou o arquivo CSV na etapa 1; Por exemplo `C:\Users\Administrator\desktop`.</span><span class="sxs-lookup"><span data-stu-id="d3720-136">After you connect PowerShell to Exchange Online, go to the desktop folder where you saved the CSV file in Step 1; for example `C:\Users\Administrator\desktop`.</span></span>
    
3. <span data-ttu-id="d3720-137">Execute o seguinte comando para criar os contatos externos:</span><span class="sxs-lookup"><span data-stu-id="d3720-137">Run the following command to create the external contacts:</span></span>

    ```
    Import-Csv .\ExternalContacts.csv|%{New-MailContact -Name $_.Name -DisplayName $_.Name -ExternalEmailAddress $_.ExternalEmailAddress -FirstName $_.FirstName -LastName $_.LastName}
    ```

    <span data-ttu-id="d3720-p107">Ela pode levar algum tempo para criar os novos contatos, dependendo de quantos você está importando. Quando o comando estiver concluído em execução, PowerShell exibe uma lista dos novos contatos que foram criados.</span><span class="sxs-lookup"><span data-stu-id="d3720-p107">It might take a while to create the new contacts, depending on how many you're importing. When the command is finished running, PowerShell displays a list of the new contacts that were created.</span></span> 
    
4. <span data-ttu-id="d3720-140">Para exibir os novos contatos externos, vá para o Centro de administração do Exchange (EAC) e, em seguida, clique em **destinatários** \> **Contatos**.</span><span class="sxs-lookup"><span data-stu-id="d3720-140">To view the new external contacts, go to the Exchange admin center (EAC), and then click **Recipients** \> **Contacts**.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="d3720-141">Para obter instruções para conectar-se ao EAC, consulte [Exchange admin center no Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=328197).</span><span class="sxs-lookup"><span data-stu-id="d3720-141">For instructions for connecting to the EAC, see [Exchange admin center in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=328197).</span></span> 
  
5. <span data-ttu-id="d3720-142">Se necessário, clique em **Atualizar** ![ícone atualizar](media/O365-MDM-Policy-RefreshIcon.gif) para atualizar a lista e ver os contatos externos que foram importados.</span><span class="sxs-lookup"><span data-stu-id="d3720-142">If necessary, click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the list and see the external contacts that were imported.</span></span> 
    
    <span data-ttu-id="d3720-143">Os contatos importados aparecerá no catálogo de endereços compartilhado no Outlook e Outlook na web.</span><span class="sxs-lookup"><span data-stu-id="d3720-143">The imported contacts will appear in the shared address book in Outlook and Outlook on the web.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="d3720-144">Você também pode exibir os contatos no Centro de administração do Office 365 indo para **usuários** \> **Contatos**.</span><span class="sxs-lookup"><span data-stu-id="d3720-144">You can also view the contacts in the Office 365 admin center by going to **Users** \> **Contacts**.</span></span> 

## <a name="step-3-add-information-to-the-properties-of-the-external-contacts"></a><span data-ttu-id="d3720-145">Etapa 3: Adicionar informações às propriedades dos contatos externos</span><span class="sxs-lookup"><span data-stu-id="d3720-145">Step 3: Add information to the properties of the external contacts</span></span>

<span data-ttu-id="d3720-p108">Depois de executar o comando na etapa 2, os contatos externos são criados, mas não contêm as informações de contato ou da organização, que é a informação de que a maioria das células no arquivo CSV. Isso ocorre porque quando você cria novos contatos externos, somente as propriedades necessárias são preenchidas. Não se preocupe se você não possui todas as informações preenchidas no arquivo CSV. Se não estiver, ele não ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="d3720-p108">After you run the command in Step 2, the external contacts are created, but they don't contain any of the contact or organization information, which is the information from the most of the cells in the CSV file. This is because when you create new external contacts, only the required properties are populated. Don't worry if you don't have all the information populated in the CSV file. If it's not there, it won't be added.</span></span>
  
1.  <span data-ttu-id="d3720-p109">Conecte o PowerShell para sua organização do Exchange Online. Para obter instruções detalhadas, consulte [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).</span><span class="sxs-lookup"><span data-stu-id="d3720-p109">Connect PowerShell to your Exchange Online organization. For step-by-step instructions, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).</span></span>
    
2. <span data-ttu-id="d3720-152">Vá para a pasta área de trabalho onde você salvou o arquivo CSV na etapa 1; Por exemplo `C:\Users\Administrator\desktop`.</span><span class="sxs-lookup"><span data-stu-id="d3720-152">Go to the desktop folder where you saved the CSV file in Step 1; for example `C:\Users\Administrator\desktop`.</span></span>
    
3. <span data-ttu-id="d3720-153">Execute os dois comandos a seguir para adicionar outras propriedades de arquivo CSV para os contatos externos que você criou na etapa 2.</span><span class="sxs-lookup"><span data-stu-id="d3720-153">Run the following two commands to add the other properties from the CSV file to the external contacts that you created in Step 2.</span></span>
    
    ```
    $Contacts = Import-CSV .\ExternalContacts.csv
  
    ```

    ```
    $contacts | ForEach {Set-Contact $_.Name -StreetAddress $_.StreetAddress -City $_.City -StateorProvince $_.StateorProvince -PostalCode $_.PostalCode -Phone $_.Phone -MobilePhone $_.MobilePhone -Pager $_.Pager -HomePhone $_.HomePhone -Company $_.Company -Title $_.Title -OtherTelephone $_.OtherTelephone -Department $_.Department -Fax $_.Fax -Initials $_.Initials -Notes  $_.Notes -Office $_.Office -Manager $_.Manager}
    ```

    > [!NOTE]
    > <span data-ttu-id="d3720-p110">O parâmetro _Manager_ pode ser problemático. Se a célula estiver em branco no arquivo CSV, você receberá um erro e nenhuma das informações de propriedade será adicionada ao contato. Se você não precisa especificar um gerente, basta excluir ` -Manager $_.Manager ` do comando PowerShell anterior.</span><span class="sxs-lookup"><span data-stu-id="d3720-p110">The  _Manager_ parameter might be problematic. If the cell is blank in the CSV file, you will get an error and none of the property information will be added to the contact. If you don't need to specify a manager, then just delete  ` -Manager $_.Manager ` from the previous PowerShell command.</span></span> 
  
    <span data-ttu-id="d3720-157">Novamente, ela pode levar algum tempo para atualizar os contatos, dependendo de quantos você importou na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="d3720-157">Again, it might take a while to update the contacts, depending on how many you imported in Step 1.</span></span> 
    
4. <span data-ttu-id="d3720-158">Para verificar se as propriedades foram adicionadas aos contatos:</span><span class="sxs-lookup"><span data-stu-id="d3720-158">To verify that the properties were added to the contacts:</span></span> 
    
1. <span data-ttu-id="d3720-159">No EAC, acesse **Destinatários** \> **Contatos**.</span><span class="sxs-lookup"><span data-stu-id="d3720-159">In the EAC, go to **Recipients** \> **Contacts**.</span></span>
    
2. <span data-ttu-id="d3720-160">Clique em um contato e clique em **Editar** ![ícone Editar](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) para exibir as propriedades do contato.</span><span class="sxs-lookup"><span data-stu-id="d3720-160">Click a contact and then click **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) to display the contact's properties.</span></span> 
    
<span data-ttu-id="d3720-p111">Isso é tudo! Os usuários podem ver os contatos e as informações adicionais no catálogo de endereços do Outlook e o Outlook na web.</span><span class="sxs-lookup"><span data-stu-id="d3720-p111">That's it! Users can see the contacts and the additional information in the address book Outlook and Outlook on the web.</span></span>
  
## <a name="add-more-external-contacts"></a><span data-ttu-id="d3720-163">Adicionar contatos mais externos</span><span class="sxs-lookup"><span data-stu-id="d3720-163">Add more external contacts</span></span>

<span data-ttu-id="d3720-p112">Você pode repetir as etapas de 1 a etapa 3 para adicionar novos contatos externos no Exchange Online. Usuários da sua empresa ou você podem adicionar apenas uma nova linha no arquivo CSV para o novo contato. Em seguida, você pode executar os comandos do PowerShell da etapa 2 e etapa 3 para criar e adicionar informações aos novos contatos.</span><span class="sxs-lookup"><span data-stu-id="d3720-p112">You can repeat Steps 1 through Step 3 to add new external contacts in Exchange Online. You or users in your company can just add a new row in the CSV file for the new contact. Then you can run the PowerShell commands from Step 2 and Step 3 to create and add information to the new contacts.</span></span>
  
> [!NOTE]
> <span data-ttu-id="d3720-p113">Quando você executar o comando para criar novos contatos, você pode obter um erro dizendo que os contatos que foram criados anteriormente, já existem. Mas qualquer novo contato adicionado ao arquivo CSV é criado.</span><span class="sxs-lookup"><span data-stu-id="d3720-p113">When you run the command to create new contacts, you might get an error saying that the contacts that were created earlier already exist. But any new contact added to the CSV file is created.</span></span> 
  
## <a name="hide-external-contacts-from-the-shared-address-book"></a><span data-ttu-id="d3720-169">Ocultar contatos externos do catálogo de endereços compartilhado ></span><span class="sxs-lookup"><span data-stu-id="d3720-169">Hide external contacts from the shared address book></span></span>

<span data-ttu-id="d3720-p114">Algumas empresas podem usar os contatos externos só para que eles podem ser adicionados como membros de grupos de distribuição. Neste cenário, eles talvez queira ocultar contatos externos do catálogo de endereços compartilhado. Veja como:</span><span class="sxs-lookup"><span data-stu-id="d3720-p114">Some companies may use external contacts only so they can be added as members of distribution groups. In this scenario, they may want to hide external contacts from the shared address book. Here's how:</span></span>
  
1.  <span data-ttu-id="d3720-p115">Conecte o PowerShell para sua organização do Exchange Online. Para obter instruções detalhadas, consulte [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).</span><span class="sxs-lookup"><span data-stu-id="d3720-p115">Connect PowerShell to your Exchange Online organization. For step-by-step instructions, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).</span></span>
    
2. <span data-ttu-id="d3720-175">Para ocultar um único contato externo, execute o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="d3720-175">To hide a single external contact, run the following command.</span></span>
    
    ```
    Set-MailContact <external contact> -HiddenFromAddressListsEnabled $true 
    ```
 
    <span data-ttu-id="d3720-176">Por exemplo, para ocultar Pilar Pinilla do catálogo de endereços compartilhado, execute este comando:</span><span class="sxs-lookup"><span data-stu-id="d3720-176">For example, to hide Pilar Pinilla from the shared address book, run this command:</span></span>

    ```
    Set-MailContact "Pilar Pinilla" -HiddenFromAddressListsEnabled $true
    ```
   
3. <span data-ttu-id="d3720-177">Para ocultar todos os contatos externos do catálogo de endereços compartilhado, execute este comando:</span><span class="sxs-lookup"><span data-stu-id="d3720-177">To hide all external contacts from the shared address book, run this command:</span></span>

    ```
    Get-Contact -ResultSize unlimited -Filter {(RecipientTypeDetails -eq 'MailContact')} | Set-MailContact -HiddenFromAddressListsEnabled $true  
    ```

<span data-ttu-id="d3720-178">Depois de você ocultá-las, contatos externos não são exibidos no catálogo de endereços compartilhado, mas você ainda poderá adicioná-los como membros de um grupo de distribuição.</span><span class="sxs-lookup"><span data-stu-id="d3720-178">After you hide them, external contacts aren't displayed in the shared address book, but you can still add them as members of a distribution group.</span></span>

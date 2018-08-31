---
title: Criar um relatório sobre isenções em casos de descoberta eletrônica no Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 9/11/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: cca08d26-6fbf-4b2c-b102-b226e4cd7381
description: Use o script neste artigo para gerar um relatório que contém informações sobre todos os bloqueios que estão associados a casos de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade.
ms.openlocfilehash: 8bc1285f776e2b1aa0c0330c06ccffff8ce4585c
ms.sourcegitcommit: c166964fe14eec69139a2d3d9c10d2c40ab33f91
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/28/2018
ms.locfileid: "23258639"
---
# <a name="create-a-report-on-holds-in-ediscovery-cases-in-office-365"></a><span data-ttu-id="1412f-103">Criar um relatório sobre isenções em casos de descoberta eletrônica no Office 365</span><span class="sxs-lookup"><span data-stu-id="1412f-103">Create a report on holds in eDiscovery cases in Office 365</span></span>
  
<span data-ttu-id="1412f-p101">O script neste artigo permite que os administradores de descoberta eletrônica e gerentes de descoberta eletrônica geram um relatório que contém informações sobre todas as isenções que estão associados a casos de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade. O relatório contém informações como o nome do caso de uma isenção está associado, os locais de conteúdo são colocadas em espera e se a suspensão é baseado em consulta. Se houver casos que não têm qualquer isenções, o script criará um relatório adicional com uma lista de ocorrências sem isenções.</span><span class="sxs-lookup"><span data-stu-id="1412f-p101">The script in this article lets eDiscovery administrators and eDiscovery managers generate a report that contains information about all holds that are associated with eDiscovery cases in the Office 365 Security &amp; Compliance Center. The report contains information such as the name of the case a hold is associated with, the content locations that are placed on hold, and whether the hold is query-based. If there are cases that don't have any holds, the script will create an additional report with a list of cases without holds.</span></span>

<span data-ttu-id="1412f-107">Consulte a seção de [informações adicionais](#more-information) para obter uma descrição detalhada das informações incluídas no relatório.</span><span class="sxs-lookup"><span data-stu-id="1412f-107">See the [More information](#more-information) section for a detailed description of the information included in the report.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="1412f-108">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="1412f-108">Before you begin</span></span>

- <span data-ttu-id="1412f-p102">Para gerar um relatório sobre todos os casos de eDiscovery em sua organização, você precisa ser um administrador de eDiscovery em sua organização. Se você for uma gerente de descoberta eletrônica, o relatório só incluirá informações sobre os casos em que você pode acessar. Para obter mais informações sobre as permissões de descoberta eletrônica, consulte [atribuir permissões de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade](assign-ediscovery-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="1412f-p102">To generate a report on all eDiscovery cases in your organization, you have to be an eDiscovery Administrator in your organization. If you are an eDiscovery Manager, the report will only include information about the cases that you can access. For more information about eDiscovery permissions, see [Assign eDiscovery permissions in the Office‍ 365 Security &amp; Compliance Center](assign-ediscovery-permissions.md).</span></span>
    
- <span data-ttu-id="1412f-p103">O script neste artigo tem o tratamento de erros mínimas. O objetivo principal é criar rapidamente o relatório sobre os bloqueios que estão associados os casos de eDiscovery em sua organização.</span><span class="sxs-lookup"><span data-stu-id="1412f-p103">The script in this article has minimal error handling. The primary purpose is to quickly create report about the holds that are associated with the eDiscovery cases in your organization.</span></span>
    
- <span data-ttu-id="1412f-p104">Os scripts de exemplo fornecidos neste tópico não são suportados em qualquer serviço ou programa de suporte padrão da Microsoft. Os scripts de exemplo são fornecidos que se encontra, sem qualquer garantia. Microsoft também se isenta de todas as garantias implícitas incluindo, sem limitações, qualquer implícitas de comercialização ou adequação a uma finalidade específica. O risco decorrente do uso ou o desempenho dos scripts de amostra e documentação permanece com você. Em nenhuma hipótese Microsoft, seus autores ou qualquer pessoa else envolvidas na criação, produção ou entrega dos scripts será responsável por quaisquer danos (incluindo, sem limitação, danos por perda de lucros cessantes, perda de informações comerciais ou outras perdas PECUNIÁRIAS) decorrente do uso ou incapacidade de usar os scripts de exemplo ou a documentação, mesmo que a Microsoft tenha sido informada da possibilidade de tais danos.</span><span class="sxs-lookup"><span data-stu-id="1412f-p104">The sample scripts provided in this topic aren't supported under any Microsoft standard support program or service. The sample scripts are provided AS IS without warranty of any kind. Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample scripts and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
    
## <a name="step-1-connect-to-the-security-amp-compliance-center-using-remote-powershell"></a><span data-ttu-id="1412f-119">Etapa 1: Conectar à segurança &amp; usando o PowerShell remoto do Centro de conformidade</span><span class="sxs-lookup"><span data-stu-id="1412f-119">Step 1: Connect to the Security &amp; Compliance Center using Remote PowerShell</span></span>

<span data-ttu-id="1412f-120">A primeira etapa é conectar o Windows PowerShell para a segurança &amp; Centro de conformidade para sua organização.</span><span class="sxs-lookup"><span data-stu-id="1412f-120">The first step is to connect Windows PowerShell to the Security &amp; Compliance Center for your organization.</span></span>
  
1. <span data-ttu-id="1412f-121">Salve o seguinte texto em um arquivo de script do Windows PowerShell usando um sufixo de nome de arquivo de. ps1; Por exemplo, `ConnectSCC.ps1`.</span><span class="sxs-lookup"><span data-stu-id="1412f-121">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `ConnectSCC.ps1`.</span></span> 
    
      ```
      # Get login credentials 
      $UserCredential = Get-Credential 
      $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection 
      Import-PSSession $Session -AllowClobber -DisableNameChecking 
      $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Office 365 Security &amp; Compliance Center)" 
    ```

2. <span data-ttu-id="1412f-122">No computador local, abra o Windows PowerShell e vá para a pasta onde você salvou o script.</span><span class="sxs-lookup"><span data-stu-id="1412f-122">On your local computer, open Windows PowerShell and go to the folder where you saved the script.</span></span> 
    
3. <span data-ttu-id="1412f-123">Executar o script; Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="1412f-123">Run the script; for example:</span></span>

    ```
    .\ConnectSCC.ps1
    ```
   
4. <span data-ttu-id="1412f-124">Quando solicitado a fornecer suas credenciais, digite seu endereço de email e senha e clique em **Okey**.</span><span class="sxs-lookup"><span data-stu-id="1412f-124">When prompted for your credentials, enter your email address and password, and then click **OK**.</span></span> 
  
## <a name="step-2-run-the-script-to-report-on-holds-associated-with-ediscovery-cases"></a><span data-ttu-id="1412f-125">Etapa 2: Executar o script a ser relatado no retém associado casos de eDiscovery</span><span class="sxs-lookup"><span data-stu-id="1412f-125">Step 2: Run the script to report on holds associated with eDiscovery cases</span></span>

<span data-ttu-id="1412f-126">Depois de se conectar à segurança &amp; Centro de conformidade com o PowerShell remoto, a próxima etapa é criar e executar o script que coleta informações sobre os casos de eDiscovery em sua organização.</span><span class="sxs-lookup"><span data-stu-id="1412f-126">After you've connected to the Security &amp; Compliance Center with remote PowerShell, the next step is to create and run the script that collects information about the eDiscovery cases in your organization.</span></span> 
  
1. <span data-ttu-id="1412f-127">Salve o seguinte texto em um arquivo de script do Windows PowerShell usando um sufixo de nome de arquivo de. ps1; Por exemplo, CaseHoldsReport.ps1.</span><span class="sxs-lookup"><span data-stu-id="1412f-127">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, CaseHoldsReport.ps1.</span></span> 
    
  ```
#script begin
" " 
write-host "***********************************************"
write-host "   Office 365 Security & Compliance Center   " -foregroundColor yellow -backgroundcolor darkgreen
write-host "        eDiscovery cases - Holds report         " -foregroundColor yellow -backgroundcolor darkgreen 
write-host "***********************************************"
" " 
#prompt users to specify a path to store the output files
$time=get-date
$Path = Read-Host 'Enter a file path to save the report to a .csv file'
$outputpath=$Path+'\'+'CaseHoldsReport'+' '+$time.day+'-'+$time.month+'-'+$time.year+' '+$time.hour+'.'+$time.minute+'.csv'
$noholdsfilepath=$Path+'\'+'CaseswithNoHolds'+' '+$time.day+'-'+$time.month+'-'+$time.year+' '+$time.hour+'.'+$time.minute+'.csv'
#add case details to the csv file
function add-tocasereport{
Param([string]$casename,
[String]$casestatus,
[datetime]$casecreatedtime,
[string]$casemembers,
[datetime]$caseClosedDateTime,
[string]$caseclosedby,
[string]$holdname,
[String]$Holdenabled,
[string]$holdcreatedby,
[string]$holdlastmodifiedby,
[string]$ExchangeLocation,
[string]$sharePointlocation,
[string]$ContentMatchQuery,
[datetime]$holdcreatedtime,
[datetime]$holdchangedtime
)
$addRow = New-Object PSObject 
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Case name" -Value $casename
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Case status" -Value $casestatus
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Case members" -Value $casemembers
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Case created time" -Value $casecreatedtime
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Case closed time" -Value $caseClosedDateTime
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Case closed by" -Value $caseclosedby
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold name" -Value $holdname
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold enabled" -Value $Holdenabled
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold created by" -Value $holdcreatedby
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold last changed by" -Value $holdlastmodifiedby
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Exchange locations" -Value  $ExchangeLocation
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "SharePoint locations" -Value $sharePointlocation
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold query" -Value $ContentMatchQuery
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold created time (UTC)" -Value $holdcreatedtime
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold changed time (UTC)" -Value $holdchangedtime
$allholdreport = $addRow | Select-Object "Case name","Case status","Hold name","Hold enabled","Case members", "Case created time","Case closed time","Case closed by","Exchange locations","SharePoint locations","Hold query","Hold created by","Hold created time (UTC)","Hold last changed by","Hold changed time (UTC)"
$allholdreport | export-csv -path $outputPath -notypeinfo -append -Encoding ascii 
}
#get information on the cases and pass values to the case report function
" "
write-host "Gathering a list of cases and holds..."
" "
$edc =Get-ComplianceCase -ErrorAction SilentlyContinue
foreach($cc in $edc)
{
write-host "Working on case :" $cc.name
if($cc.status -eq 'Closed')
{
$cmembers = ((Get-ComplianceCaseMember -Case $cc.name).windowsLiveID)-join ';'
add-tocasereport -casename $cc.name -casestatus $cc.Status -caseclosedby $cc.closedby -caseClosedDateTime $cc.ClosedDateTime -casemembers $cmembers 
}
else{
$cmembers = ((Get-ComplianceCaseMember -Case $cc.name).windowsLiveID)-join ';'
$policies = Get-CaseHoldPolicy -Case $cc.Name | %{ Get-CaseHoldPolicy $_.Name -Case $_.CaseId -DistributionDetail}
if ($policies -ne $NULL)
{
foreach ($policy in $policies)
{
$rule=Get-CaseHoldRule -Policy $policy.name
add-tocasereport -casename $cc.name -casemembers $cmembers -casestatus $cc.Status -casecreatedtime $cc.CreatedDateTime -holdname $policy.name -holdenabled $policy.enabled -holdcreatedby $policy.CreatedBy -holdlastmodifiedby $policy.LastModifiedBy -ExchangeLocation (($policy.exchangelocation.name)-join ';') -SharePointLocation (($policy.sharePointlocation.name)-join ';') -ContentMatchQuery $rule.ContentMatchQuery -holdcreatedtime $policy.WhenCreatedUTC -holdchangedtime $policy.WhenChangedUTC
}
}
else{
write-host "No hold policies found in case:" $cc.name -foregroundColor 'Yellow'
" "
[string]$cc.name | out-file -filepath $noholdsfilepath -append 
}
}
}

" "
Write-host "Script complete! Report files saved to this folder: '$Path'"
" "
#script end
  ```

2. <span data-ttu-id="1412f-128">Na sessão do Windows PowerShell que aberto na etapa 1, vá para a pasta onde você salvou o script.</span><span class="sxs-lookup"><span data-stu-id="1412f-128">In the Windows PowerShell session that opened in Step 1, go to the folder where you saved the script.</span></span> 
    
3. <span data-ttu-id="1412f-129">Executar o script; Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="1412f-129">Run the script; for example:</span></span>

    ```
    .\CaseHoldsReport.ps1
    ```

    <span data-ttu-id="1412f-130">O script perguntará para uma pasta de destino para salvar o relatório.</span><span class="sxs-lookup"><span data-stu-id="1412f-130">The script will prompt for a target folder to save the report to.</span></span> 
    
4. <span data-ttu-id="1412f-131">Digite o nome do caminho completo da pasta para salvar o relatório e pressione **Enter**.</span><span class="sxs-lookup"><span data-stu-id="1412f-131">Type the full path name of the folder to save the report to, and then press **Enter**.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="1412f-p105">Para salvar o relatório na mesma pasta que o script está localizado em, digite um ponto (".") quando solicitado para uma pasta de destino. Para salvar o relatório em uma subpasta na pasta onde o script está localizado, basta digite o nome da subpasta.</span><span class="sxs-lookup"><span data-stu-id="1412f-p105">To save the report in the same folder that the script is located in, type a period (".") when prompted for a target folder. To save the report in a subfolder in the folder where the script is located, just type the name of the subfolder.</span></span> 
  
    <span data-ttu-id="1412f-p106">O script começa a coletar informações sobre todos os casos de eDiscovery em sua organização. Não acesse o arquivo de relatório enquanto o script está sendo executado. Quando o script for concluído, será exibida uma mensagem de confirmação da sessão do Windows PowerShell. Depois que essa mensagem é exibida, você pode acessar o relatório na pasta que você especificou na etapa 4. O nome de arquivo para o relatório é `CaseHoldsReport<DateTimeStamp>.csv`.</span><span class="sxs-lookup"><span data-stu-id="1412f-p106">The script starts to collect information about all the eDiscovery cases in your organization. Don't access the report file while the script is running. After the script is complete, a confirmation message is displayed in the Windows PowerShell session. After this message is displayed, you can access the report in the folder that you specified in Step 4. The file name for the report is `CaseHoldsReport<DateTimeStamp>.csv`.</span></span>

    <span data-ttu-id="1412f-p107">Addtionally, o script também cria um relatório com uma lista das ocorrências que não têm qualquer isenções. O nome de arquivo para este relatório é `CaseswithNoHolds<DateTimeStamp>.csv`.</span><span class="sxs-lookup"><span data-stu-id="1412f-p107">Addtionally, the script also creates a report with a list of cases that don't have any holds. The file name for this report is `CaseswithNoHolds<DateTimeStamp>.csv`.</span></span>
    
    <span data-ttu-id="1412f-141">Aqui está um exemplo de execução do script CaseHoldsReport.ps1.</span><span class="sxs-lookup"><span data-stu-id="1412f-141">Here's an example of running the CaseHoldsReport.ps1 script.</span></span> 
    
    ![A saída após executar o script CaseHoldsReport.ps1](media/7d312ed5-505e-4ec5-8f06-3571e3524a1a.png)
  
## <a name="more-information"></a><span data-ttu-id="1412f-143">Mais informações</span><span class="sxs-lookup"><span data-stu-id="1412f-143">More information</span></span>

<span data-ttu-id="1412f-p108">O caso contém o relatório que é criado quando você executar o script neste artigo contém as seguintes informações sobre cada isenção. Conforme explicado anteriormente, você precisa ser uma administrador para retornar informações sobre todas as isenções em sua organização de descoberta eletrônica. Para obter mais informações sobre o caso contém, consulte [casos de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade](ediscovery-cases.md).</span><span class="sxs-lookup"><span data-stu-id="1412f-p108">The case holds report that's created when you run the script in this article contains the following information about each hold. As previously explained, you have to be an eDiscovery Administrator to return information for all holds in your organization. For more information about case holds, see [eDiscovery cases in the Office 365 Security &amp; Compliance Center](ediscovery-cases.md).</span></span>
  
  - <span data-ttu-id="1412f-147">O nome da isenção e o nome no caso de eDiscovery que a suspensão está associada.</span><span class="sxs-lookup"><span data-stu-id="1412f-147">The name of the hold and the name of the eDiscovery case that the hold is associated with.</span></span>
    
  - <span data-ttu-id="1412f-148">Ou não o caso de descoberta eletrônica é ativo ou fechado.</span><span class="sxs-lookup"><span data-stu-id="1412f-148">Whether or not the eDiscovery case is active or closed.</span></span>
    
  - <span data-ttu-id="1412f-149">Ou não a espera está habilitada ou desabilitada.</span><span class="sxs-lookup"><span data-stu-id="1412f-149">Whether or not the hold is enabled or disabled.</span></span>
    
  - <span data-ttu-id="1412f-p109">Os membros no caso de eDiscovery que a suspensão está associada. Membros de maiusculas podem exibir ou gerenciar um caso, dependendo das permissões de descoberta eletrônica que tenham sido atribuídos a eles.</span><span class="sxs-lookup"><span data-stu-id="1412f-p109">The members of the eDiscovery case that the hold is associated with. Case members can view or manage a case, depending on the eDiscovery permissions they've been assigned.</span></span>
    
  - <span data-ttu-id="1412f-152">A hora e data que o caso foi criado.</span><span class="sxs-lookup"><span data-stu-id="1412f-152">The time and date the case was created.</span></span>
    
  - <span data-ttu-id="1412f-153">Se um caso for fechado, a pessoa que fechado-lo e a hora e data que ele foi fechada.</span><span class="sxs-lookup"><span data-stu-id="1412f-153">If a case is closed, the person who closed it and the time and date it was closed.</span></span>
    
  - <span data-ttu-id="1412f-154">Caixas de correio do Exchange e SharePoint sites locais que estão em espera.</span><span class="sxs-lookup"><span data-stu-id="1412f-154">The Exchange mailboxes and SharePoint sites locations that are on hold.</span></span>
    
  - <span data-ttu-id="1412f-155">Se a suspensão é baseado em consulta, a sintaxe de consulta.</span><span class="sxs-lookup"><span data-stu-id="1412f-155">If the hold is query-based, the query syntax.</span></span>
    
  - <span data-ttu-id="1412f-156">A hora e data que isenção foi criada e a pessoa que criou a ele.</span><span class="sxs-lookup"><span data-stu-id="1412f-156">The time and date the hold was created and the person who created it.</span></span>
    
  - <span data-ttu-id="1412f-157">A hora e data da que última alteração isenção e a pessoa que-la alterado.</span><span class="sxs-lookup"><span data-stu-id="1412f-157">The time and date the hold was last changed and the person who changed it.</span></span>

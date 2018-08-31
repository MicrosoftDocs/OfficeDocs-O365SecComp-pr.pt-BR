---
title: Configurar permissões de filtragem para a Pesquisa de Conteúdo
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 5/14/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 1adffc35-38e5-4f7d-8495-8e0e8721f377
description: Use as permissões de pesquisa de conteúdo de filtragem para permitir que um gerente de descoberta eletrônica pesquisar somente um subconjunto de caixas de correio e de sites em sua organização do Office 365.
ms.openlocfilehash: 2b6968a097e7abe5943a84b9ceb9b6d126057cc2
ms.sourcegitcommit: c166964fe14eec69139a2d3d9c10d2c40ab33f91
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/28/2018
ms.locfileid: "23258619"
---
# <a name="configure-permissions-filtering-for-content-search"></a>Configurar permissões de filtragem para a Pesquisa de Conteúdo

Você pode usar as permissões de pesquisa filtragem para permitir que um gerente de descoberta eletrônica pesquisar somente um subconjunto de caixas de correio e de sites em sua organização do Office 365. Você também pode usar as permissões de filtragem para permitir que esse mesmo gerente de descoberta eletrônica pesquisar somente o conteúdo de caixa de correio ou site que atenda a critérios de pesquisa específicos. Por exemplo, você pode permitir que um gerente de descoberta eletrônica procurem as caixas de correio de usuários em um local específico ou um departamento. Você pode fazer isso criando um filtro que usa um filtro de destinatário com suporte para limitar as caixas de correio que podem ser pesquisadas. Você também pode criar um filtro que especifica qual conteúdo de caixa de correio que pode ser pesquisado. Isso é feito criando um filtro que usa uma propriedade de mensagem pesquisável. Da mesma forma, você pode permitir que um gerente de descoberta eletrônica apenas procurem sites específicos do SharePoint em sua organização. Você pode fazer isso criando um filtro que limita a quais sites podem ser pesquisados. Você também pode criar um filtro que especifica qual conteúdo de site pode ser pesquisado. Isso é feito criando um filtro que usa uma propriedade do site pesquisável.

Você também pode usar as permissões de pesquisa de filtragem para criar limites lógicos (chamados de *limites de conformidade*) dentro de uma organização do Office 365 que controlam os locais de conteúdo do usuário (por exemplo, caixas de correio, sites do SharePoint e contas do OneDrive) que gerentes de descoberta eletrônica específico podem pesquisar. Para obter mais informações, consulte [Configurar limites de conformidade para investigações de descoberta eletrônica no Office 365](set-up-compliance-boundaries.md).
  
Filtragem de permissões de pesquisa é suportado pelo recurso de pesquisa de conteúdo no Office 365 Security &amp; Centro de conformidade. Esses quatro cmdlets permitem que você configurar e gerenciar filtros de permisisons de pesquisa:
  
[New-ComplianceSecurityFilter](#new-compliancesecurityfilter)

[Get-ComplianceSecurityFilter](#get-compliancesecurityfilter)

[Set-ComplianceSecurityFilter](#set-compliancesecurityfilter)

[Remove-ComplianceSecurityFilter](#remove-compliancesecurityfilter)

## <a name="before-you-begin"></a>Antes de começar

- Para executar os cmdlets de filtro de segurança de conformidade, você precisa ser membro do grupo de funções de gerenciamento da organização na segurança &amp; Centro de conformidade. Para obter mais informações, consulte [permissões no Office 365 Security &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md).
    
- Você precisará conectar o Windows PowerShell para ambos os a segurança &amp; Centro de conformidade e para sua organização do Exchange Online para usar os cmdlets de filtro de segurança de conformidade. Isso é necessário porque esses cmdlets requerem acesso às propriedades de caixa de correio, o motivo pelo qual você precisa se conectar ao Exchange Online. Consulte as etapas na próxima seção. 
    
- Consulte a seção [Mais informações](#more-information) para obter informações adicionais sobre os filtros de permissões de pesquisa. 
    
- Filtragem de permissões de pesquisa é aplicável a caixas de correio inativas, o que significa que você pode usar a caixa de correio e de filtragem para limitar quem pode pesquisar uma caixa de correio inativa de conteúdo de caixa de correio. Consulte a seção de [informações adicionais](#more-information) para obter informações adicionais sobre a filtragem de permissões e caixas de correio inativas. 
    
-  Filtragem de permissões de pesquisa não podem ser usadas para limitar quem pode pesquisar pastas públicas no Exchange. 
    
- Não há nenhum limite ao número de filtros de permissões de pesquisa que podem ser criados em uma organização. No entanto, o desempenho de pesquisa será afetado quando há mais de 100 filtros de permissões de pesquisa. Para manter o número de filtros de permissões de pesquisa em sua organização tão pequeno quanto possível, crie filtros que combinam regras para Exchange, SharePoint e OneDrive em um único filtro sempre que possível.
    
## <a name="connect-to-the-security-amp-compliance-center-and-exchange-online-in-a-single-remote-powershell-session"></a>Conecte-se à segurança &amp; Centro de conformidade e o Exchange Online em uma única sessão do PowerShell remota

1. Salve o seguinte texto em um arquivo de script do Windows PowerShell, usando um sufixo de nome de arquivo de. ps1. Por exemplo, você poderia salve-o em um arquivo denominado ConnectEXO-CC.ps1.
    
    ```
    $UserCredential = Get-Credential
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -DisableNameChecking
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -AllowClobber -DisableNameChecking
    $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Exchange Online + Compliance Center)"
    ```

2. No computador local, abra o Windows PowerShell, vá para a pasta onde se encontra o script que você criou na etapa anterior e, em seguida, execute o script; Por exemplo:
    
    ```
    .\ConnectEXO-CC.ps1
    ```
 
Como verifico se isso funcionou? Depois de executar o script, os cmdlets de segurança &amp; Centro de conformidade e o Exchange Online são importados para a sua sessão local do Windows PowerShell. Se você não receber algum erro, você conectado com êxito. Um teste rápido é executada uma segurança &amp; cmdlet do Centro de conformidade — por exemplo, **Install-UnifiedCompliancePrerequisite** — e um cmdlet do Exchange Online, como **Get-Mailbox**. 
  
Caso você receba erros, verifique os seguintes requisitos:
  
- Um problema comum é uma senha incorreta. Execute as duas etapas novamente e preste muita atenção ao nome de usuário e à senha inseridos na Etapa 1.
    
- Verificar se a sua conta tem permissão para acessar a segurança &amp; Centro de conformidade. Para obter detalhes, consulte [Conceder aos usuários acesso à segurança &amp; Centro de conformidade](grant-access-to-the-security-and-compliance-center.md).
    
- Para ajudar a impedir ataques (dos negação) de negação de serviço, você está limitado a três conexões abertas do remotas PowerShell à segurança &amp; Centro de conformidade.
    
- O Windows PowerShell deve ser configurado para executar scripts. Você só precisa definir essa configuração uma vez em seu computador, e não sempre que se conectar. Para habilitar o Windows PowerShell para executar scripts assinados, execute o seguinte comando em uma janela elevada do Windows PowerShell (uma janela do Windows PowerShell que você abriu ao selecionar a opção **Executar como administrador**).

    ```
    Set-ExecutionPolicy RemoteSigned
    ```
- Tráfego de porta 80 do TCP precisa ser aberta entre o computador local e o Office 365. Ele está provavelmente aberto, mas é algo a ser considerado se sua organização tem uma política de acesso de Internet restritiva.
    

  
## <a name="new-compliancesecurityfilter"></a>New-ComplianceSecurityFilter
<a name="New"> </a>

O **New-ComplianceSecurityFilter** é usado para criar um novo filtro de permissões de pesquisa. A tabela a seguir descreve os parâmetros para esse cmdlet. Todos os parâmetros são necessárias para criar um filtro de segurança de conformidade. 
  
|**Parameter**|**Descrição**|
|:-----|:-----|
| _Action_ <br/> | O parâmetro _Action_ Especifica que tipo de ação de pesquisa que o filtro é aplicado à. As ações de pesquisa de conteúdo possíveis são:<br/><br/> **Exportar** - o filtro é aplicado ao exportar os resultados da pesquisa.  <br/> **Visualização** - o filtro é aplicado ao visualizar os resultados da pesquisa.  <br/> **Limpar** - o filtro é aplicado ao limpar os resultados da pesquisa.  <br/> **Pesquisa** - o filtro é aplicado ao executar uma pesquisa.  <br/> **Todos** - o filtro é aplicado a todas as ações de pesquisa.  <br/> |
| _FilterName_ <br/> |O parâmetro _FilterName_ Especifica o nome do filtro permissões. Esse nome é usado para a identidade um filtro ao usar os cmdlets **Get-ComplianceSecurityFilter**, **Set-ComplianceSecurityFilter** e **Remove-ComplianceSecurityFilter** .<br/> |
| _Filtros_ <br/> | O parâmetro de _filtros_ Especifica os critérios de pesquisa para o filtro de segurança de conformidade. Você pode criar três diferentes tipos de filtros:<br/><br/> A **filtragem de caixa de correio** - esse tipo de filtro especifica as caixas de correio de usuários atribuídos (especificados pelo parâmetro _usuários_ ) podem pesquisar. A sintaxe para esse tipo de filtro é **Mailbox_** _MailboxPropertyName_, onde _MailboxPropertyName_ Especifica uma propriedade de caixa de correio usada para as caixas de correio que podem ser pesquisadas de escopo. Por exemplo, o filtro de caixa de correio `"Mailbox_CustomAttribute10 -eq 'OttawaUsers'"` só permitia o usuário atribuído a esse filtro para pesquisar somente caixas de correio que tenham o valor "OttawaUsers" na propriedade CustomAttribute10.<br/>  Qualquer propriedade de destinatário filtrável suportada pode ser usada para a propriedade _MailboxPropertyName_ . Para obter uma lista das propriedades com suporte, consulte [Propriedades filtráveis para o parâmetro - RecipientFilter](https://go.microsoft.com/fwlink/p/?LinkId=784903).<br/><br/> **Filtragem de conteúdo de caixa de correio** - esse tipo de filtro é aplicado no conteúdo que pode ser pesquisado. Especifica o conteúdo de caixa de correio, que os usuários atribuídos podem pesquisar. A sintaxe para esse tipo de filtro é **MailboxContent_** _SearchablePropertyName:value_, onde _SearchablePropertyName_ Especifica uma propriedade de linguagem de consulta de palavra-chave (KQL) que pode ser especificada em uma pesquisa de conteúdo. Por exemplo, o filtro de conteúdo de caixa de correio `MailboxContent_recipients:contoso.com` só permitia o usuário atribuído a esse filtro para pesquisar somente mensagens enviadas a destinatários no domínio contoso.com.<br/>  Para obter uma lista de propriedades de mensagem pesquisáveis, consulte [consultas de palavra-chave e condições de pesquisa para pesquisa de conteúdo](keyword-queries-and-search-conditions.md).  <br/><br/> **Filtragem de conteúdo de site e site** - existem dois SharePoint e OneDrive para filtros de negócios relacionadas ao site que você pode usar para especificar quais sites ou conteúdo do site, os usuários atribuídos podem pesquisar:  <br/><br/> - **Site_** _SearchableSiteProperty_ <br/> - **SiteContent_** _SearchableSiteProperty_ <br/><br/>  Esses dois filtros são intercambiáveis; Por exemplo `"Site_Path -like 'https://contoso.sharepoint.com/sites/doctors*'"` e `"SiteContent_Path -like 'https://contoso.sharepoint.com/sites/doctors*'"` retornará os mesmos resultados. Mas para ajudá-lo a identificar o que significa um filtro, você pode usar `Site_` para especificar propriedades relacionadas ao site (por exemplo, uma URL de site) e `SiteContent_` para especificar propriedades relacionadas ao conteúdo (por exemplo, tipos de documento. Por exemplo, o filtro `"Site_Path -like 'https://contoso.sharepoint.com/sites/doctors*'"` só permitia o usuário atribuído a esse filtro para pesquisar somente para o conteúdo a https://contoso.sharepoint.com/sites/doctors conjunto de sites. O filtro `"SiteContent_FileExtension -eq 'docx'"` só permitia o usuário atribuído a esse filtro para pesquisar somente para documentos do Word (Word 2007 e posterior).<br/><br/>  Para obter uma lista das propriedades do site pesquisáveis, consulte [Overview of rastreadas e propriedades gerenciadas no SharePoint](https://go.microsoft.com/fwlink/p/?LinkId=331599). Propriedades marcadas com um **Sim** no * * consultável * * coluna pode ser usada para criar um site ou o filtro de conteúdo do site.<br/> <br/> **Importante:**  Um filtro de pesquisa único só pode ter um tipo de filtro; ele não pode conter um filtro de caixa de correio e um filtro de site; da mesma forma, ele não pode conter um filtro de caixa de correio e um filtro de conteúdo de caixa de correio. No entanto, um filtro pode conter uma consulta mais complexa do mesmo tipo. Por exemplo,`"Mailbox_CustomAttribute10 -eq 'FTE' -and Mailbox_MemberOfGroup -eq '$($DG.DistinguishedName)'"` <br/><br/> **Importante:** Você precisa criar um filtro de permissões de pesquisa para explicitamente impedir que usuários pesquisando locais de conteúdo em um serviço específico do Office 365 (por exemplo, impedindo que um usuário pesquisa qualquer caixa de correio do Exchange ou de qualquer site do SharePoint). Em outras palavras, criar um filtro de permissões de pesquisa que permite que um usuário pesquise todos os sites do SharePoint na organização não impede que o usuário a pesquisa de caixas de correio. Por exemplo, para permitir que os administradores do SharePoint pesquisar somente os sites do SharePoint, você precisa criar um criar um filtro que impede que a pesquisa de caixas de correio. Da mesma forma, para permitir que os administradores do Exchange pesquisar somente caixas de correio, você precisará criar um criar um filtro que impede que a pesquisa de sites.           |
| _Usuários_ <br/> |O parâmetro de _usuários_ Especifica os usuários que obtém esse filtro aplicado às suas pesquisas de conteúdo. Identifica usuários por seus alias ou o endereço SMTP principal. Você pode especificar vários valores separados por vírgulas, ou você pode atribuir o filtro a todos os usuários usando o valor **All**.<br/> Você também pode usar o parâmetro de _usuários_ para especificar um título &amp; grupo de funções do Centro de conformidade. Um filtro de pesquisa de permissões de grupo permite que você cria um grupo de função personalizada e, em seguida, atribuir essa função. Por exemplo, digamos que você tenha um grupo de função personalizada para gerentes de descoberta eletrônica para a subsidiária dos EUA de uma multinacional. Você pode usar o parâmetro de _usuários_ para especificar a este grupo de função (usando a propriedade Name de um grupo de funções) e, em seguida, use o parâmetro _Filter_ para permitir que somente caixas de correio nos EUA a ser pesquisado.<br/> Você não pode especificar um grupo de distribuição com esse parâmetro.  <br/> |
   

## <a name="examples-of-creating-search-permissions-filters"></a>Exemplos de criação de filtros de permissões de pesquisa

Estes são exemplos de como usar o cmdlet **New-ComplianceSecurityFilter** para criar um filtro de permissões de pesquisa. 
  
Este exemplo permite que o usuário annb@contoso.com executar todas as ações de pesquisa de conteúdo somente para caixas de correio no Canadá. Esse filtro contém o código de país de três dígitos numéricos do Canadá do ISO 3166-1.

```
New-ComplianceSecurityFilter -FilterName CountryFilter  -Users annb@contoso.com -Filters "Mailbox_CountryCode  -eq '124'" -Action All
```

Este exemplo permite que os usuários viniciusm e clarab pesquisem apenas as caixas de correio que têm o valor Marketing para a propriedade de caixa de correio CustomAttribute1.

```
New-ComplianceSecurityFilter -FilterName MarketingFilter  -Users donh,suzanf -Filters "Mailbox_CustomAttribute1  -eq 'Marketing'" -Action Search
```
   
Este exemplo permite que os membros do grupo de função "Gerentes de Descoberta dos EUA" executem todas as ações de pesquisa de conteúdo apenas em caixas de correio nos Estados Unidos. O filtro usa o código de país numérico de três dígitos para os Estados Unidos da ISO 3166-1.
  
```
New-ComplianceSecurityFilter -FilterName USDiscoveryManagers  -Users "US Discovery Managers" -Filters "Mailbox_CountryCode  -eq '840'" -Action All
```

Este exemplo permite que os membros do grupo de função Gerente de Descoberta Eletrônica pesquisem apenas as caixas de correio dos membros do grupo de distribuição Usuários de Ottawa. 
  
```
$DG = Get-DistributionGroup "Ottawa Users"
```

```
New-ComplianceSecurityFilter -FilterName DGFilter  -Users eDiscoveryManager -Filters "Mailbox_MemberOfGroup -eq '$($DG.DistinguishedName)'" -Action Search
```
Este exemplo impede que qualquer usuário exclua o conteúdo de caixas de correio dos membros do grupo de distribuição Equipe Executiva.

```
$DG = Get-DistributionGroup "Executive Team"
```

```
New-ComplianceSecurityFilter -FilterName NoExecutivesPreview  -Users all -Filters "Mailbox_MemberOfGroup -ne '$($DG.DistinguishedName)'" -Action Purge
```
   
Este exemplo permite que os membros do grupo de função personalizada de OneDrive eDiscovery Managers para procurar somente conteúdo no OneDrive para locais de negócios na organização.

```
New-ComplianceSecurityFilter -FilterName OneDriveOnly  -Users "OneDrive eDiscovery Managers" -Filters "Site_Path -like 'https://contoso-my.sharepoint.com/personal*'" -Action Search
```
   
> [!NOTE]
> Para restringir os usuários a sites específicos de pesquisa, use o filtro `Site_Path`, conforme mostrado no exemplo anterior. Usando `Site_Site` não funcionará. 
  
Este exemplo restringe o usuário a executar todas as ações de Pesquisa de Conteúdo somente em mensagens de email enviadas durante o ano de 2015.

```
New-ComplianceSecurityFilter -FilterName EmailDateRestrictionFilter -Users donh@contoso.com -Filters "MailboxContent_Received -ge '01-01-2015' -and MailboxContent_Received -le '12-31-2015'" -Action All
```
   
Semelhante ao exemplo anterior, este exemplo restringe o usuário a executar todas as ações de pesquisa de conteúdo em documentos alterados pela última vez em algum ponto no ano de 2015.

```
New-ComplianceSecurityFilter -FilterName DocumentDateRestrictionFilter -Users donh@contoso.com -Filters "SiteContent_LastModifiedTime -ge '01-01-2015' -and SiteContent_LastModifiedTime -le '12-31-2015'" -Action All
```
   
Este exemplo impede que os membros do grupo de função "Gerentes de descoberta do OneDrive" a execução de ações de pesquisa de conteúdo em qualquer caixa de correio na organização. 

```
New-ComplianceSecurityFilter -FilterName NoEXO -Users "OneDrive Discovery Managers" -Filters "Mailbox_Alias -notlike '*'"  -Action All
```
  
## <a name="get-compliancesecurityfilter"></a>Get-ComplianceSecurityFilter

O **Get-ComplianceSecurityFilter** é usado para retornar uma lista de filtros de permissões de pesquisa. Use o parâmetro _FilterName_ para retornar informações sobre um filtro de pesquisa específica. 
  
## <a name="set-compliancesecurityfilter"></a>Set-ComplianceSecurityFilter

O **Set-ComplianceSecurityFilter** é usado para modificar um filtro de permissões de pesquisa existente. O único parâmetro necessário é _FilterName_. 
  
|**Parameter**|**Descrição**|
|:-----|:-----|
| _Action_| O parâmetro _Action_ Especifica que tipo de ação de pesquisa que o filtro é aplicado à. As ações de pesquisa de conteúdo possíveis são:<br/><br/> **Exportar** - o filtro é aplicado ao exportar os resultados da pesquisa.  <br/> **Visualização** - o filtro é aplicado ao visualizar os resultados da pesquisa.  <br/> **Limpar** - o filtro é aplicado ao limpar os resultados da pesquisa.  <br/> **Pesquisa** - o filtro é aplicado ao executar uma pesquisa.  <br/> **Todos** - o filtro é aplicado a todas as ações de pesquisa.  <br/> |
| _FilterName_|O parâmetro _FilterName_ Especifica o nome do filtro permissões. |
| _Filtros_| O parâmetro de _filtros_ Especifica os critérios de pesquisa para o filtro de segurança de conformidade. Você pode criar dois tipo diferente de filtros:<br/><br/>A **filtragem de caixa de correio** - esse tipo de filtro especifica as caixas de correio de usuários atribuídos (especificados pelo parâmetro _usuários_ ) podem pesquisar. A sintaxe para esse tipo de filtro é **Mailbox_** _MailboxPropertyName_, onde _MailboxPropertyName_ Especifica uma propriedade de caixa de correio usada para as caixas de correio que podem ser pesquisadas de escopo. Por exemplo, o filtro de caixa de correio `"Mailbox_CustomAttribute10 -eq 'OttawaUsers'"` só permitia o usuário atribuído a esse filtro para pesquisar somente caixas de correio que tenham o valor "OttawaUsers" na propriedade CustomAttribute10.  Qualquer propriedade de destinatário filtrável suportada pode ser usada para a propriedade _MailboxPropertyName_ . Para obter uma lista das propriedades com suporte, consulte [Propriedades filtráveis para o parâmetro - RecipientFilter](https://go.microsoft.com/fwlink/p/?LinkId=784903).<br/><br/>**Filtragem de conteúdo de caixa de correio**- esse tipo de filtro é aplicado no conteúdo que pode ser pesquisado. Especifica o conteúdo de caixa de correio, que os usuários atribuídos podem pesquisar. A sintaxe para esse tipo de filtro é **MailboxContent_** _SearchablePropertyName:value_, onde _SearchablePropertyName_ Especifica uma propriedade de linguagem de consulta de palavra-chave (KQL) que pode ser especificada em uma pesquisa de conteúdo. Por exemplo, o filtro de conteúdo de caixa de correio `MailboxContent_recipients:contoso.com` só permitia o usuário atribuído a esse filtro para pesquisar somente mensagens enviadas a destinatários no domínio contoso.com.  Para obter uma lista de propriedades de mensagem pesquisáveis, consulte [consultas de palavra-chave de pesquisa de conteúdo](keyword-queries-and-search-conditions.md).<br/><br/>**Filtragem de sites e conteúdo de site** Existem dois SharePoint e OneDrive para filtros de negócios relacionadas ao site que você pode usar para especificar quais sites ou conteúdo do site, os usuários atribuídos podem pesquisar: <br/><br/>- **Site_** *SearchableSiteProperty* <br/>- **SiteContent**_*SearchableSiteProperty*<br/><br/>Esses dois filtros são intercambiáveis; Por exemplo `"Site_Path -like 'https://contoso.spoppe.com/sites/doctors*'"` e `"SiteContent_Path -like 'https://contoso.spoppe.com/sites/doctors*'"` retornará os mesmos resultados. Mas para ajudá-lo a identificar o que significa um filtro, você pode usar `Site_` para especificar propriedades relacionadas ao site (por exemplo, uma URL de site) e `SiteContent_` para especificar propriedades relacionadas ao conteúdo (por exemplo, tipos de documento. Por exemplo, o filtro `"Site_Path -like 'https://contoso.spoppe.com/sites/doctors*'"` só permitia o usuário atribuído a esse filtro para pesquisar somente para o conteúdo a https://contoso.spoppe.com/sites/doctors conjunto de sites. O filtro `"SiteContent_FileExtension -eq 'docx'"` só permitia o usuário atribuído a esse filtro para pesquisar somente para documentos do Word (Word 2007 e posterior).<br/><br/>Para obter uma lista das propriedades do site pesquisáveis, consulte [Overview of rastreadas e propriedades gerenciadas no SharePoint](https://go.microsoft.com/fwlink/p/?LinkId=331599). Propriedades marcadas com um **Sim** na coluna **consultável** podem ser usadas para criar um site ou o filtro de conteúdo do site.<br/><br/> **Importante:** Um filtro de pesquisa único só pode ter um tipo de filtro; ele não pode conter um filtro de caixa de correio e um filtro de site; da mesma forma, ele não pode conter um filtro de caixa de correio e um filtro de conteúdo de caixa de correio. No entanto, um filtro pode conter uma consulta mais complexa do mesmo tipo. Por exemplo,`"Mailbox_CustomAttribute10 -eq 'FTE' -and Mailbox_MemberOfGroup -eq '$($DG.DistinguishedName)'"`          |
| _Usuários_|O parâmetro de _usuários_ Especifica os usuários que obtém esse filtro aplicado às suas pesquisas de conteúdo. Como esta é uma propriedade de valor múltiplos, a especificação de um usuário ou grupo de usuários com esse parâmetro substituirá a lista de usuários existentes. Consulte os exemplos a seguir para obter a sintaxe para adicionar e remover usuários selecionados.<br/><br/>Você também pode usar o parâmetro de _usuários_ para especificar um título &amp; grupo de funções do Centro de conformidade. Um filtro de pesquisa de permissões de grupo permite que você cria um grupo de função personalizada e, em seguida, atribuir essa função. Por exemplo, digamos que você tenha um grupo de função personalizada para gerentes de descoberta eletrônica para a subsidiária dos EUA de uma multinacional. Você pode usar o parâmetro de _usuários_ para especificar a este grupo de função (usando a propriedade Name de um grupo de funções) e, em seguida, use o parâmetro _Filter_ para permitir que somente caixas de correio nos EUA a ser pesquisado.<br/><br/>Você não pode especificar um grupo de distribuição com esse parâmetro. |

## <a name="examples-of-changing-search-permissions-filters"></a>Exemplos de alteração de filtros de permissões de pesquisa

Estes exemplos mostram como usar os cmdlets **Get-ComplianceSecurityFilter** e **Set-ComplianceSecurityFilter** para adicionar ou remover um usuário à lista de usuários que o filtro é atribuído a existente. Quando você adicionar ou remove usuários de um filtro, especifique o usuário usando seu endereço SMTP. 
  
Este exemplo adiciona um usuário ao filtro.

```
$filterusers = Get-ComplianceSecurityFilter -FilterName OttawaUsersFilter
```
```
$filterusers.users.add("pilarp@contoso.com")
```

```
Set-ComplianceSecurityFilter -FilterName OttawaUsersFilter -Users $filterusers.users
```
   
Este exemplo remove um usuário do filtro.

```
$filterusers = Get-ComplianceSecurityFilter -FilterName OttawaUsersFilter
```

```
$filterusers.users.remove("annb@contoso.com")
```

```
Set-ComplianceSecurityFilter -FilterName OttawaUsersFilter -Users $filterusers.users
```
  
## <a name="remove-compliancesecurityfilter"></a>Remove-ComplianceSecurityFilter

O **Remove-ComplianceSecurityFilter** é usado para excluir um filtro de pesquisa. Use o parâmetro _FilterName_ para especificar o filtro que você deseja excluir. 
  
## <a name="more-information"></a>Mais informações

- **Como pesquisar permissões filtragem trabalho?** O filtro de permissões é adicionado à consulta de pesquisa quando uma pesquisa de conteúdo for executada. O filtro de permissões é essencialmente incluído a consulta de pesquisa pelo operador booleano **AND** . Por exemplo, digamos que você tenha um filtro de permissões que permite Bob para executar todas as ações de pesquisa em caixas de correio dos membros do grupo de distribuição de funcionários. Então Bob executa uma pesquisa de conteúdo em todas as caixas de correio na organização com a consulta de pesquisa `sender:jerry@adatum.com`. Porque o filtro de permissões e a consulta de pesquisa são combinados logicamente por um operador **e** , a pesquisa retornará qualquer mensagem enviada por jerry@adatum.com para qualquer membro do grupo de distribuição de funcionários. 
    
- **o que acontece se você tiver vários filtros de permissões de pesquisa?** Em uma consulta de pesquisa de conteúdo, vários filtros de permissões são combinados por **ou** operadores booleanos. Portanto resultados serão retornados se qualquer um dos filtros forem verdadeiras. Em uma pesquisa de conteúdo, todos os filtros (combinados pelos operadores **ou** ), em seguida, são combinados com a consulta de pesquisa pelo operador **AND** . Vamos do exemplo anterior, onde um filtro de pesquisa permite Bob para pesquisar somente as caixas de correio dos membros do grupo de distribuição de funcionários. Em seguida, podemos criar outro filtro que impede que Bob pesquisando a caixa de correio Phil ("Mailbox_Alias - ne 'Phil'"). E vamos supor também que Phil é um membro do grupo de operadores. Quando Bob executa uma pesquisa de conteúdo (do exemplo anterior) em todas as caixas de correio na organização, os resultados da pesquisa serão retornados para caixa de correio Phil, mesmo que você aplicou filtro para impedir que o Bob pesquisando a caixa de correio Phil. Isso ocorre porque o primeiro filtro, que permite que Bob para pesquisar o grupo de funcionários, é true. E como Phil é um membro do grupo de operadores, Bob pode pesquisar a caixa de correio Phil. 
    
- **Pesquisar permissões a filtragem de trabalho para caixas de correio inativas?** Sim, você pode usar a caixa de correio e filtros de conteúdo de caixa de correio para limitar quem pode pesquisar caixas de correio inativas em sua organização. Como uma caixa de correio regular, uma caixa de correio inativa tem que ser configurada com a propriedade destinatário que é usada para criar um filtro de permissões. Se necessário, você pode usar o comando **Get-Mailbox-InactiveMailboxOnly** para exibir as propriedades de caixas de correio inativas. Para obter mais informações, consulte [criar e gerenciar caixas de correio inativas no Office 365](create-and-manage-inactive-mailboxes.md).
    
- **Pesquisar permissões a filtragem de trabalho para pastas públicas?** Não. Como explicada anteriormente, a pesquisa permissões filtragem não podem ser usadas para limitar quem pode pesquisar pastas públicas no Exchange. Por exemplo, os itens em locais de pasta pública não podem ser excluídos dos resultados da pesquisa por um filtro de permissões. 
    
- **Permitindo que um usuário pesquise todos os locais de conteúdo em um serviço específico também impedi-los de verificação ortográfica locais de conteúdo em um serviço diferente?** Não. Conforme explicado anteriormente, você precisa criar um filtro de permissões de pesquisa para explicitamente impedir que usuários pesquisando locais de conteúdo em um serviço específico do Office 365 (por exemplo, impedindo que um usuário pesquisa qualquer caixa de correio do Exchange ou de qualquer site do SharePoint). Em outras palavras, criar um filtro de permissões de pesquisa que permite que um usuário pesquise todos os sites do SharePoint na organização não impede que o usuário a pesquisa de caixas de correio. Por exemplo, para permitir que os administradores do SharePoint pesquisar somente os sites do SharePoint, você precisa criar um criar um filtro que impede que a pesquisa de caixas de correio. Da mesma forma, para permitir que os administradores do Exchange pesquisar somente caixas de correio, você precisará criar um criar um filtro que impede que a pesquisa de sites.

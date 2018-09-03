---
title: Propriedades detalhadas no log de auditoria do Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/8/2017
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- BCS160
- MET150
ms.assetid: ce004100-9e7f-443e-942b-9b04098fcfc3
description: Registro de log de auditoria de descrições das propriedades adicionais incluídos em um Office 365.
ms.openlocfilehash: 69c5565ac71715ba2cb22d93d80f7e5dd12c6440
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524101"
---
# <a name="detailed-properties-in-the-office-365-audit-log"></a>Propriedades detalhadas no log de auditoria do Office 365

Quando você exportar os resultados de uma pesquisa de log de auditoria da segurança do Office 365 &amp; Centro de conformidade, você tem a opção de download de todos os resultados que atendam aos critérios de pesquisa. Você pode fazer isso, selecionando **exportar os resultados da** \> **Baixe todos os resultados** na página de **pesquisa de log de auditoria** na segurança &amp; Centro de conformidade. Para obter mais informações, consulte [Pesquisar o log de auditoria de segurança do Office 365 &amp; Centro de conformidade](search-the-audit-log-in-security-and-compliance.md).
  
 Quando a exportação de todos os resultados para uma pesquisa de log de auditoria, os dados brutos do log de auditoria unificada é copiada para uma vírgula o Office 365 separados arquivo CSV (valor) isso será baixado para o computador local. Esse arquivo contém informações adicionais da entrada de log de auditoria em uma coluna **detalhe**de chamada. Essa coluna contém uma propriedade de múltiplos valor para várias propriedades do registro de log de auditoria. Cada um dos pares de **valor da propriedade:** nessa propriedade de valores múltiplos são separados por uma vírgula. 
  
A tabela a seguir descreve as propriedades que são incluídas — dependendo do Office 365 de serviço no qual ocorre um evento — na coluna de **detalhes** da propriedade múltiplos. A coluna de **serviço do Office 365 com esta propriedade** indica o serviço e o tipo de atividade (usuário ou administrador) que inclui a propriedade. Para obter informações mais detalhadas sobre como essas propriedades ou sobre propriedades que talvez não estejam listadas neste tópico, consulte [Esquema de API de atividades de gerenciamento do Office 365](https://go.microsoft.com/fwlink/p/?LinkId=717993).
  
> [!TIP]
> Você pode usar a consulta de energia no Excel para dividir essa coluna em várias colunas, de modo que cada propriedade terá sua própria coluna. Isso permitirá que você classificar e filtrar em uma ou mais dessas propriedades. Para saber como fazer isso, consulte a seção "Dividir uma coluna por delimitador" em [uma coluna de texto (Power consulta) de divisão](https://support.office.com/article/5282d425-6dd0-46ca-95bf-8e0da9539662). 
  
|**Propriedade**|**Descrição**|**Serviço do Office 365 com esta propriedade**|
|:-----|:-----|:-----|
|Ator  <br/> |A conta de usuário ou serviço que executou a ação. |Azure Active Directory  <br/> |
|AddOnName  <br/> |O nome de um complemento que foi adicionado, removido ou atualizado em uma equipe. O tipo de complementos no Microsoft Teams são um bot, um conector ou uma guia.  <br/> |Microsoft Teams  <br/> |
|AddOnType  <br/> |O tipo de um complemento que foi adicionado, removido ou atualizado em uma equipe. Os seguintes valores indicam o tipo de complemento.<br/> **1** - indica um bot.<br/> **2** - indica um conector.<br/> **3** - indica uma guia. |Microsoft Teams  <br/> |
|AzureActiveDirectoryEventType  <br/> |O tipo de evento do Windows Azure Active Directory. Os seguintes valores indicam o tipo de evento.<br/> **0** - indica um evento de logon da conta.<br/> **1** - indica um evento de segurança de aplicativo do Azure. |Azure Active Directory  <br/> |
|ChannelGuid  <br/> |A identificação de um canal de Teams da Microsoft. A equipe que o canal está localizado em é identificada pelas propriedades **nomedaequipe** e **TeamGuid** .<br/> |Microsoft Teams  <br/> |
|ChannelName  <br/> |O nome de um canal de Teams da Microsoft. A equipe que o canal está localizado em é identificada pelas propriedades **nomedaequipe** e **TeamGuid** .<br/> |Microsoft Teams  <br/> |
|Cliente  <br/> |O dispositivo do cliente, o sistema operacional do dispositivo e o navegador de dispositivo usado para o evento de logon (por exemplo, Nokia Lumia 920; Windows Phone 8; Mobile de IE 11).  <br/> |Azure Active Directory  <br/> |
|ClientInfoString  <br/> |Informações sobre o cliente de email que foi usado para executar a operação, como uma versão do navegador, versão do Outlook e informações do dispositivo móvel  <br/> |Exchange (atividade de caixa de correio)  <br/> |
|ClientIP  <br/> |O endereço IP do dispositivo que foi usado quando a atividade foi registrada. O endereço IP é exibido no formato de endereço de um IPv4 ou IPv6.  <br/> |Exchange e Windows Azure Active Directory  <br/> |
|ClientIPAddress  <br/> |O mesmo que ClientIP.  <br/> |SharePoint  <br/> |
|CreationTime  <br/> |A data e hora no tempo Universal Coordenado (UTC) quando o usuário desempenhou a atividade.  <br/> |Tudo  <br/> |
|DestinationFileExtension  <br/> |A extensão de arquivo de um arquivo for copiado ou movido. Essa propriedade é exibida somente para as atividades do usuário FileCopied e FileMoved.  <br/> |SharePoint  <br/> |
|DestinationFileName  <br/> |O nome do arquivo é copiado ou movido. Essa propriedade é exibida somente para as ações FileCopied e FileMoved.  <br/> |SharePoint  <br/> |
|DestinationRelativeUrl  <br/> |A URL da pasta de destino onde um arquivo for copiado ou movido. A combinação dos valores para as propriedades de **DestinationFileName** , o **DestinationRelativeURL**e o **SiteURL**é o mesmo que o valor da propriedade **ObjectID** , que é o nome de caminho completo para o arquivo que foi copiado. Essa propriedade é exibida somente para as atividades do usuário FileCopied e FileMoved.<br/> |SharePoint  <br/> |
|EventSource  <br/> |Identifica que um evento ocorreu no SharePoint. Valores possíveis são **SharePoint** e **ObjectModel**.<br/> |SharePoint  <br/> |
|ExternalAccess  <br/> |Para atividade de administração do Exchange, especifica se o cmdlet foi executado por um usuário em sua organização, pela equipe de datacenter da Microsoft ou uma conta de serviço do datacenter, ou por um administrador delegado. O valor **False** indica que o cmdlet foi executado por alguém em sua organização. O valor **True** indica que o cmdlet foi executado pelo pessoal de datacenter, uma conta de serviço do datacenter ou um administrador delegado.<br/> Para atividade de caixa de correio do Exchange, especifica se uma caixa de correio foi acessada por um usuário fora da sua organização.  <br/> |Exchange  <br/> |
|ExtendedProperties  <br/> |As propriedades estendidas para um evento do Windows Azure Active Directory.  <br/> |Azure Active Directory  <br/> |
|ID  <br/> |A identificação da entrada do relatório. A ID identifica exclusivamente a entrada do relatório.  <br/> |Tudo  <br/> |
|InternalLogonType  <br/> |Reservado para uso interno.  <br/> |Exchange (atividade de caixa de correio)  <br/> |
|ItemType  <br/> |O tipo de objeto que foi acessado ou modificado. Os valores possíveis incluem o **arquivo**, **pasta**, **Web**, **Site**, **locatário**e **DocumentLibrary**.<br/> |SharePoint  <br/> |
|LoginStatus  <br/> |Identifica as falhas de login que podem ter ocorrido.  <br/> |Azure Active Directory  <br/> |
|Tipo de logon  <br/> |O tipo de acesso de caixa de correio. Os seguintes valores indicam o tipo de usuário que acessaram a caixa de correio.<br/><br/> **0** - indica um proprietário de caixa de correio.<br/> **1** - indica que um administrador.<br/> **2** - indica um representante. <br/>**3** - indica que o serviço de transporte no datacenter Microsoft.<br/> **4** - ndicates uma conta de serviço no datacenter Microsoft. <br/>**6** - indica que um administrador delegado. |Exchange (atividade de caixa de correio)  <br/> |
|MailboxGuid  <br/> |O GUID do Exchange da caixa de correio que foi acessada.  <br/> |Exchange (atividade de caixa de correio)  <br/> |
|MailboxOwnerUPN  <br/> |O endereço de email da pessoa que possui a caixa de correio foi acessada.  <br/> |Exchange (atividade de caixa de correio)  <br/> |
|Membros  <br/> |Lista os usuários que foram adicionados ou removidos da equipe. Os valores a seguir indicam o tipo de função atribuído ao usuário.<br/><br/> **1** - indica a função de proprietário.<br/> **2** - indica a função de membro.<br/> **3** - indica a função de convidado. <br/><br/>A propriedade Members também inclui o nome da sua organização e o endereço de email do membro.  <br/> |Microsoft Teams  <br/> |
|ModifiedProperties (nome, NewValue, OldValue)  <br/> |A propriedade é incluída para eventos de administração, como a adição de um usuário como um membro de um site ou um grupo de administração do conjunto de sites. A propriedade inclui o nome da propriedade que foi modificado (por exemplo, o grupo de administração de Site) o novo valor da propriedade modificado (tal o usuário que foi adicionado como um administrador de site e o valor anterior do objeto modificado.  <br/> |Todos os (admin atividade)  <br/> |
|ObjectID  <br/> |Para Exchange admin do log de auditoria, o nome do objeto que foi modificado pelo cmdlet.  <br/> Para a atividade do SharePoint, o nome do caminho de URL completo do arquivo ou pasta acessado por um usuário.  <br/> Atividade do Azure AD, o nome da conta de usuário que foi modificado.  <br/> |Tudo  <br/> |
|Operation  <br/> |O nome da atividade do usuário ou administrador. O valor dessa propriedade corresponde ao valor que foi selecionado nas **atividades** de lista suspensa. Se **Mostrar resultados para todas as atividades** foi selecionado, o relatório será incluído entradas para todas as atividades de administrador e usuário para todos os serviços. Para obter uma descrição das operações/atividades que são registradas no log de auditoria do Office 365, consulte o guia **atividades auditadas** no [Pesquisar o log de auditoria de segurança do Office 365 &amp; Centro de conformidade](search-the-audit-log-in-security-and-compliance.md).<br/> Para atividade de administração do Exchange, esta propriedade identifica o nome do cmdlet que foi executado.  <br/> |Tudo  <br/> |
|ID da organização  <br/> |O GUID para sua organização do Office 365.  <br/> |Tudo  <br/> |
|Path  <br/> |O nome da pasta de caixa de correio onde se encontra a mensagem que foi acessada. Essa propriedade também identifica a pasta um onde uma mensagem é criada no ou copiado/movido para.  <br/> |Exchange (atividade de caixa de correio)  <br/> |
|Parâmetros  <br/> |Atividade de administração do Exchange, o nome e valor para todos os parâmetros que foram usados com o cmdlet que é identificado na propriedade operação.  <br/> |Exchange (admin atividade)  <br/> |
|RecordType  <br/> |O tipo de operação indicada pelo record. Os valores a seguir indicam o tipo de registro.<br/><br/> **1** - indica um registro de log de auditoria do administrador do Exchange. <br/>**2** - indica um registro do log de auditoria de caixa de correio do Exchange de uma operação realizada em um item de caixa de correio singled. <br/>**3** - também indica um registro de log de auditoria de caixa de correio do Exchange. Esse tipo de registro indica que a operação foi executada em vários itens na caixa de correio de origem (por exemplo, para mover vários itens para a pasta Itens excluídos ou excluir permanentemente os vários itens).<br/>**4** - indica que uma operação de administração de site no SharePoint, como um administrador ou usuário atribuindo permissões a um site. <br/>**6** - indica um arquivo ou uma operação relacionada a pasta no SharePoint, como um usuário exibir ou modificar um arquivo. <br/>**8** - indica que uma operação de admin realizada no Windows Azure Active Directory. <br/>**9** - indica OrgId eventos de logon no Windows Azure Active Directory. Esse tipo de registro que está sendo excluído.<br/>**10** - indica os eventos de segurança do cmdlet que foram executados pela equipe da Microsoft no data center. <br/>**11** - eventos de proteção (DLP) de perda de dados indica no SharePoint.<br/> **12** - indica Sway eventos. <br/>**14** - indica os eventos de compartilhamento no SharePoint.<br/> **15** - indica seguro Token Service (STS) de eventos de logon no Windows Azure Active Directory. <br/>**18** - segurança indica &amp; eventos do Centro de conformidade. <br/>**20** - eventos indica Power BI. <br/>**22** - eventos indica Yammer. <br/>**24** - indica os eventos de descoberta eletrônica. Esse tipo de registro indica as atividades que foram realizadas executando pesquisas de conteúdo e gerenciar casos de eDiscovery na segurança &amp; Centro de conformidade. Para obter mais informações, consulte Search para atividades de descoberta eletrônica no Office 365 no log de auditoria.<br/>**25, 26 ou 27** - eventos indica as equipes da Microsoft. |Tudo  <br/> |
|ResultStatus  <br/> |Indica se a ação (especificada na propriedade **operação** ) foi bem-sucedida ou não.  <br/> Para atividade de administração do Exchange, o valor é **True** (bem-sucedido) ou **False** (com falha).  <br/> |Tudo  <br/> |
|SecurityComplianceCenterEventType  <br/> |Indica que a atividade foi um título &amp; evento do Centro de conformidade. Toda a segurança &amp; atividades do Centro de conformidade terá um valor **0** para essa propriedade.<br/> |Segurança do Office 365 &amp; Centro de conformidade  <br/> |
|SharingType  <br/> |O tipo de permissões de compartilhamento que foi atribuído ao usuário que o recurso foi compartilhado com. Esse usuário é identificado na propriedade **UserSharedWith** .<br/> |SharePoint  <br/> |
|Site  <br/> |O GUID do site onde está localizada o arquivo ou pasta acessado pelo usuário.  <br/> |SharePoint  <br/> |
|SiteUrl  <br/> |A URL do site onde está localizada o arquivo ou pasta acessado pelo usuário.  <br/> |SharePoint  <br/> |
|SourceFileExtension  <br/> |A extensão de arquivo do arquivo que foi acessada pelo usuário. Esta propriedade estiver vazia, se o objeto que foi acessado for uma pasta.  <br/> |SharePoint  <br/> |
|SourceFileName  <br/> |O nome do arquivo ou pasta acessado pelo usuário.  <br/> |SharePoint  <br/> |
|SourceRelativeUrl  <br/> |A URL da pasta que contém o arquivo acessado pelo usuário. A combinação dos valores para as propriedades **SourceFileName** , o **SourceRelativeURL**e o **SiteURL**é o mesmo que o valor da propriedade **ObjectID** , que é o nome de caminho completo para o arquivo acessado pelo usuário.<br/> |SharePoint  <br/> |
|Subject  <br/> |A linha de assunto da mensagem que foi acessada.  <br/> |Exchange (atividade de caixa de correio)  <br/> |
|TabType  <br/> | O tipo de guia adicionado, removido ou atualizado em uma equipe. Os valores possíveis para essa propriedade são:<br/><br/> **Excelpin** - guia An Excel.  <br/> **Extensão** - todos os aplicativos primários e de terceiros; como planejador, VSTS e formulários.  <br/> **Observações** - guia do OneNote.  <br/> **Pdfpin** - guia uma PDF.  <br/> **Powerbi** - PowerBI de uma guia.  <br/> **Powerpointpin** - guia do PowerPoint de uma.  <br/> **Sharepointfiles** - SharePoint de uma guia.  <br/> **Página da Web** - uma guia fixados website.  <br/> **Guia de Wiki** - uma guia wiki.  <br/> **Wordpin** - guia uma palavra.  <br/> |Microsoft Teams  <br/> |
|Destino  <br/> |O usuário que a ação (identificada na propriedade **operação** ) foi executada em. Por exemplo, se um usuário convidado é adicionado ao SharePoint ou um Team Microsoft, que o usuário seria listado nessa propriedade.<br/> |Azure Active Directory  <br/> |
|TeamGuid  <br/> |A identificação de uma equipe de Teams da Microsoft.  <br/> |Microsoft Teams  <br/> |
|Nomedaequipe  <br/> |O nome de uma equipe de Teams da Microsoft.  <br/> |Microsoft Teams  <br/> |
|UserAgent  <br/> |Informações sobre o navegador do usuário. Essas informações são fornecidas pelo navegador.  <br/> |SharePoint  <br/> |
|UserDomain  <br/> |Informações de identidade sobre a organização de locatário do usuário (ator) que executou a ação.  <br/> |Azure Active Directory  <br/> |
|UserID  <br/> |O usuário que executou a ação (especificada na propriedade **operação** ) que resultou no registro que está sendo registrado. Observe que os registros de atividade realizada por contas do sistema (por exemplo, SHAREPOINT\system ou Autoridade NT\Sistema) também são incluídos no log de auditoria.<br/> |Tudo  <br/> |
|UserKey  <br/> |Uma ID alternativa para o usuário identificado na propriedade **UserID** . Por exemplo, esta propriedade é preenchida com a ID exclusiva do passport (PUID) para eventos realizadas pelos usuários no SharePoint. Essa propriedade também pode especificar o mesmo valor que a propriedade **UserID** para eventos que ocorrem em outros serviços e eventos realizados por contas do sistema.<br/> |Tudo  <br/> |
|UserSharedWith  <br/> |O usuário que um recurso foi compartilhado com. Essa propriedade é incluída se o valor da propriedade **operação** for **SharingSet**. Esse usuário também está listado na coluna **compartilhado com** no relatório.<br/> |SharePoint  <br/> |
|UserType  <br/> |O tipo de usuário que executou a operação. Os valores a seguir indicam o tipo de usuário.<br/> <br/> **0** - um usuário regular. <br/>**2** - administrador em sua organização do Office 365. <br/>**3** - administrador de datacenter da Microsoft de uma ou a conta do sistema de datacenter. <br/>**4** - uma conta do sistema. <br/>**5** - um aplicativo. <br/>**6** - uma entidade de serviço. |Tudo  <br/> |
|Versão  <br/> |Indica o número de versão da atividade (identificado pela propriedade **operação** ) que está conectado.  <br/> |Tudo  <br/> |
|Carga de trabalho  <br/> |O serviço do Office 365 onde a atividade ocorreu. Os valores possíveis para essa propriedade são:<br/> <br/>**SharePoint<br/>OneDrive<br/>Exchange<br/>AzureActiveDirectory<br/>DataCenterSecurity<br/>conformidade<br/>Sway<br/>SecurityComplianceCenter<br/>PowerBI<br/>MicrosoftTeams<br/> ThreatIntelligence**|Tudo  <br/> |
   
Observe que as propriedades descritas acima também são exibidas quando você clica em **obter mais informações** ao visualizar os detalhes de um evento específico. 
  
![Clique em obter mais informações para exibir as propriedades detalhadas sobre o registro de eventos de log de auditoria](media/6df582ae-d339-4735-b1a6-80914fb77a08.png)
  

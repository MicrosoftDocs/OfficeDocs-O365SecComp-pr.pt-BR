---
title: Consultas de palavra-chave e condições de pesquisa para Pesquisa de Conteúdo
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: reference
f1_keywords:
- ms.o365.cc.SearchQueryLearnMore
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: c4639c2e-7223-4302-8e0d-b6e10f1c3be3
description: 'Saiba mais sobre as propriedades de email e o arquivo que você pode pesquisar nas caixas de correio do Exchange Online e no SharePoint ou OneDrive para sites corporativos usando a ferramenta de pesquisa de conteúdo no Office 365 Security &amp; Centro de conformidade.  '
ms.openlocfilehash: c043b6667e6847ff944b05e6bbe91df8ed2f600c
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524213"
---
# <a name="keyword-queries-and-search-conditions-for-content-search"></a>Consultas de palavra-chave e condições de pesquisa para Pesquisa de Conteúdo

Este tópico descreve as propriedades de email e documentos que você pode pesquisar em itens de email no Exchange Online e documentos armazenados no SharePoint e sites do OneDrive for Business, usando o recurso de pesquisa de conteúdo no Office 365 Security &amp; conformidade Centro. Você também pode usar o ** \*- ComplianceSearch** cmdlets em Security &amp; PowerShell do Centro de conformidade para procurar essas propriedades. Também descreve o tópico: 
  
- Usando operadores de pesquisa booleana, condições de pesquisa e outras técnicas de consulta de pesquisa para refinar os resultados da pesquisa.
    
- Pesquisar os tipos de dados confidenciais e tipos de dados confidenciais personalizados no SharePoint e o OneDrive for Business.
    
- Procura por conteúdo de site que é compartilhado com usuários fora da sua organização
    
Para obter instruções passo a passo sobre como criar uma pesquisa de conteúdo, consulte a [Pesquisa de conteúdo no Office 365](content-search.md). |

  
> [!NOTE]
> Pesquisa na segurança de conteúdo &amp; Centro de conformidade e a correspondente ** \*- ComplianceSearch** cmdlets em Security &amp; PowerShell do Centro de conformidade use a linguagem de consulta de palavra-chave (KQL). Para obter informações mais detalhadas, consulte [referência de sintaxe de linguagem de consulta de palavra-chave](https://go.microsoft.com/fwlink/?LinkId=269603). 
  
## <a name="searchable-email-properties"></a>Propriedades de emails pesquisáveis

A tabela a seguir lista as propriedades da mensagem de email que podem ser pesquisadas, usando o recurso de pesquisa de conteúdo na segurança &amp; Centro de conformidade ou usando o **New-ComplianceSearch** ou o cmdlet **Set-ComplianceSearch** . A tabela inclui um exemplo da sintaxe do _valor da propriedade:_ para cada propriedade e uma descrição dos resultados da pesquisa retornados pelos exemplos. Você pode digitar essas `property:value` as palavras-chave os pares de caixa para uma pesquisa de conteúdo. 
  
|**Propriedade**|**Descrição da propriedade**|**Exemplos**|**Resultados de pesquisa retornados pelos exemplos**|
|:-----|:-----|:-----|:-----|
|AttachmentNames  <br/> |Os nomes dos arquivos anexados a uma mensagem de email.  <br/> |`attachmentnames:annualreport.ppt`  <br/> `attachmentnames:annual\*`  <br/> |Mensagens que têm um arquivo anexado chamado relatórioanual.ppt. No segundo exemplo, o uso do caractere curinga retorna mensagens com a palavra "anual" no nome de arquivo de um anexo.  <br/> |
|Cco  <br/> |O campo Cco de uma mensagem de email.<sup>1</sup> <br/> |`bcc:pilarp@contoso.com`  <br/> `bcc:pilarp`  <br/> `bcc:"Pilar Pinilla"`  <br/> |Todos os exemplos retornam mensagens com Brenda Fernandes incluída no campo Cco.  <br/> |
|Categoria  <br/> | As categorias a serem pesquisadas. As categorias podem ser definidas pelos usuários usando o Outlook ou o Outlook Web App. Os valores possíveis são:  <br/><br/>  azul  <br/>  verde  <br/>  laranja  <br/>  roxo  <br/>  vermelho  <br/>  amarelo  <br/> |`category:"Red Category"`  <br/> |Mensagens que foram atribuídas à categoria vermelho nas caixas de correio de origem.   <br/> |
|Cc  <br/> |O campo CC de uma mensagem de email.<sup>1</sup> <br/> |`cc:pilarp@contoso.com`  <br/> `cc:"Pilar Pinilla"`  <br/> |Em ambos os exemplos, mensagens com Brenda Fernandes especificada no campo CC.  <br/> |
|Folderid  <br/> |A pasta ID (GUID) de uma pasta de caixa de correio específica. Se você usar essa propriedade, certifique-se de pesquisar a caixa de correio localizada na pasta especificada. Observe que somente a pasta especificada será pesquisada. Todas as subpastas na pasta não ser pesquisadas. Para Pesquisar subpastas, você precisa usar a propriedade Folderid para a subpasta que você deseja pesquisar.<br/> Para obter mais informações sobre a propriedade Folderid pesquisando e usando um script para obter a pasta IDs para uma caixa de correio específica, consulte [Uso de pesquisa de conteúdo no Office 365 para conjuntos de destino](use-content-search-for-targeted-collections.md).  <br/> |`folderid:4D6DD7F943C29041A65787E30F02AD1F00000000013A0000`  <br/> `folderid:2370FB455F82FC44BE31397F47B632A70000000001160000 AND participants:garthf@contoso.com`  <br/> |O primeiro exemplo retorna todos os itens na pasta caixa de correio especificada. O segundo exemplo retorna todos os itens na pasta caixa de correio especificada que foram enviadas ou recebidas por garthf@contoso.com.  <br/> |
|De  <br/> |O remetente de uma mensagem de email.<sup>1</sup> <br/> |`from:pilarp@contoso.com`  <br/> `from:contoso.com`  <br/> |Mensagens enviadas pelo usuário especificado ou enviadas de um domínio especificado.  <br/> |
|HasAttachment  <br/> |Indica se uma mensagem tiver um anexo. Use os valores **true** ou **false**.<br/> |`from:pilar@contoso.com AND hasattachment:true`  <br/> |Mensagens enviadas pelo usuário especificado e que possuem anexos.  <br/> |
|Importância  <br/> |A prioridade de uma mensagem de email, que um remetente pode especificar ao enviar uma mensagem. Por padrão, as mensagens são enviadas com prioridade normal, a menos que o remetente defina a prioridade como **alta** ou **baixa**.<br/> |`importance:high`  <br/> `importance:medium`  <br/> `importance:low`  <br/> |Mensagens marcadas como alta prioridade, prioridade média ou baixa prioridade.  <br/> |
|Foi lido  <br/> |Indica se ou não mensagens que tenham sido lidas. Use os valores **true** ou **false**.<br/> |`isread:true`  <br/> `isread:false`  <br/> |O primeiro exemplo retorna as mensagens com a propriedade foi lido definida como **True**. O segundo exemplo retorna as mensagens com a propriedade foi lido definida como **False**.<br/> |
|ItemClass  <br/> |Use essa propriedade para pesquisar os tipos de dados específicos de terceiros que sua organização importada para o Office 365. Use a seguinte sintaxe para essa propriedade:`itemclass:ipm.externaldata.<third-party data type>*` <br/> |`itemclass:ipm.externaldata.Facebook\* AND subject:contoso`  <br/> `itemclass:ipm.externaldata.Twitter\* AND from:"Ann Beebe" AND "Northwind Traders"`  <br/> |O primeiro exemplo retorna os itens de Facebook que contêm a palavra "contoso" na propriedade Subject. O segundo exemplo retorna os itens do Twitter que foram lançadas por Ann Beebe e que contenham a frase de palavra-chave "Northwind Traders".<br/> Para obter uma lista completa dos valores a serem usados para tipos de dados de terceiros para a propriedade ItemClass, consulte [Use pesquisa de conteúdo para pesquisar dados de terceiros que foi importados para o Office 365](use-content-search-to-search-third-party-data-that-was-imported.md).  <br/> |
|Tipo  <br/> | O tipo de mensagem de email a ser pesquisado. Valores possíveis:  <br/>  contatos  <br/>  documentos  <br/>  email  <br/>  externaldata  <br/>  faxes  <br/>  mensagem instantânea  <br/>  diários  <br/>  reuniões  <br/>  microsoftteams (retorna itens de bate-papos, reuniões e chamadas em Microsoft Teams)  <br/>  observações  <br/>  postagens  <br/>  rssfeeds  <br/>  tarefas  <br/>  caixa postal  <br/> |`kind:email`  <br/> `kind:email OR kind:im OR kind:voicemail`  <br/> `kind:externaldata`  <br/> |O primeiro exemplo retorna as mensagens de email que satisfazem os critérios de pesquisa. O segundo exemplo retorna as mensagens de email, conversas de mensagens instantâneas e mensagens de voz que atendam aos critérios de pesquisa. O terceiro exemplo retorna os itens que foram importados para caixas de correio no Office 365 de fontes de dados de terceiros, como Twitter, Facebook e Cisco Jabber, que atendam aos critérios de pesquisa. Para obter mais informações, consulte [arquivamento dados de terceiros no Office 365](https://go.microsoft.com/fwlink/p/?linkid=716918).<br/> |
|Participants  <br/> |Todos os campos de pessoas em uma mensagem de email; os campos são De, Para, Cc e Cco.<sup>1</sup> <br/> |`participants:garthf@contoso.com`  <br/> `participants:contoso.com`  <br/> |Mensagens enviadas por ou para pauloa@contoso.com. O segundo exemplo retorna todas as mensagens enviadas por ou para um usuário no domínio contoso.com.  <br/> |
|Recebido  <br/> |A data em que uma mensagem de email foi recebida pelo destinatário.  <br/> |`received:04/15/2016`  <br/> `received\>=01/01/2016 AND received\<=03/31/2016`  <br/> |Mensagens que foram recebidas em 15 de abril de 2016. O segundo exemplo retorna todas as mensagens recebidas entre 1 de janeiro de 2016 e 31 de março de 2016.  <br/> |
|Destinatários  <br/> |Todos os campos de destinatários em uma mensagem de email; esses campos são Para, CC e Cco.<sup>1</sup> <br/> |`recipients:garthf@contoso.com`  <br/> `recipients:contoso.com`  <br/> |Mensagens enviadas para pauloa@contoso.com. O segundo exemplo retorna mensagens enviadas para qualquer destinatário no domínio contoso.com.  <br/> |
|Enviado  <br/> |A data em que uma mensagem de email foi enviada pelo remetente.  <br/> |`sent:07/01/2016`  <br/> `sent\>=06/01/2016 AND sent\<=07/01/2016`  <br/> |Mensagens que foram enviadas na data especificada ou dentro do intervalo de datas especificado.  <br/> |
|Size  <br/> |O tamanho de um item, em bytes.  <br/> |`size\>26214400`  <br/> `size:1..1048567`  <br/> |Mensagens maiores do que 25?? MB. O segundo exemplo retorna as mensagens de 1 a 1,048,567 bytes (1 MB) de tamanho.  <br/> |
|Subject  <br/> |O texto na linha de assunto de uma mensagem de email.  <br/> **Observação:** Quando você usa a propriedade Subject em uma consulta, a pesquisa de ???the retornará todas as mensagens nas quais a linha de assunto contém o texto que você está procurando. Em outras palavras, a consulta não retorna somente as mensagens que tenham uma correspondência exata. Por exemplo, se você procurar `subject:"Quarterly Financials"`, os resultados incluirão mensagens com o assunto "2018 de finanças trimestrais".<br/> |`subject:"Quarterly Financials"`  <br/> `subject:northwind`  <br/> |Mensagens que contenham a frase "Finanças trimestrais" em qualquer lugar no texto da linha de assunto. O segundo exemplo retorna todas as mensagens que contêm o palavra northwind na linha de assunto.  <br/> |
|Para  <br/> |O campo Para de uma mensagem de email.<sup>1</sup> <br/> |`to:annb@contoso.com`  <br/> `to:annb ` <br/> `to:"Ann Beebe"`  <br/> |Todos os exemplos retornam mensagens em que Clara Barbosa é especificada na linha Para:.  <br/> |
   
> [!NOTE]
> <sup>1</sup> para o valor de uma propriedade de destinatário, você pode usar o endereço de email (também chamado de *nome principal de usuário* ou nome UPN), nome para exibição ou alias para especificar um usuário. Por exemplo, você pode usar "Ann Beebe", annb ou annb@contoso.com para especificar o usuário de Ann Beebe.<br/><br/>Ao pesquisar qualquer uma das propriedades destinatários (From, To, Cc, Cco, participantes e destinatários), o Office 365 tenta expandir a identidade de cada usuário observando-los no Windows Azure Active Directory.  Se o usuário for encontrado no Windows Azure Active Directory, a consulta é expandida para incluir o usuário email endereço (ou UPN), alias, nome de exibição e LegacyExchangeDN.<br/><br/>Por exemplo, uma consulta como `participants:ronnie@contoso.com` expande até `participants:ronnie@contoso.com OR participants:ronnie OR participants:"Ronald Nelson" OR participants:"<LegacyExchangeDN>"`.

## <a name="searchable-site-properties"></a>Propriedades de sites pesquisáveis

A tabela a seguir lista algumas das OneDrive e SharePoint para as propriedades de negócios que podem ser pesquisadas, usando o recurso de pesquisa de conteúdo na segurança &amp; Centro de conformidade ou usando o **New-ComplianceSearch** ou o ** Set-ComplianceSearch** cmdlet. A tabela inclui um exemplo da sintaxe do _valor da propriedade:_ para cada propriedade e uma descrição dos resultados da pesquisa retornados pelos exemplos. 
  
Para obter uma lista completa das propriedades do SharePoint que podem ser pesquisados, consulte [Overview of rastreadas e propriedades gerenciadas no SharePoint](https://go.microsoft.com/fwlink/p/?LinkId=331599). As propriedades marcadas com um **Sim** na coluna **consultável** podem ser pesquisadas. 
  
|**Propriedade**|**Descrição da propriedade**|**Exemplo**|**Resultados de pesquisa retornados pelos exemplos**|
|:-----|:-----|:-----|:-----|
|Autor  <br/> |O campo autor dos documentos do Office, do qual persiste se um documento é copiado. Por exemplo, se um usuário cria um documento e os e-mails-la a alguém que carrega-lo no SharePoint, o documento ainda manterá o autor original. Certifique-se de usar o nome para exibição do usuário para essa propriedade.  <br/> |`author:"Garth Fort"`  <br/> |Todos os documentos criados por Paulo Araújo.  <br/> |
|ContentType  <br/> |O tipo de conteúdo do SharePoint de um item, como vídeo, documento ou Item.  <br/> |`contenttype:document`  <br/> |Todos os documentos seriam ser retornados.  <br/> |
|Created  <br/> |A data em que um item foi criado.  <br/> |`created\>=06/01/2016`  <br/> |Todos os itens são criados em ou após 1 de junho de 2016.  <br/> |
|CreatedBy  <br/> |A pessoa que criou ou carregado de um item. Certifique-se de usar o nome para exibição do usuário para essa propriedade.  <br/> |`createdby:"Garth Fort"`  <br/> |Todos os itens criados ou carregados por Paulo Araújo.  <br/> |
|DetectedLanguage  <br/> |O idioma de um item.  <br/> |`detectedlanguage:english`  <br/> |Todos os itens em inglês.  <br/> |
|FileExtension  <br/> |A extensão de um arquivo; Por exemplo, docx, um, pptx ou xlsx.  <br/> |`fileextension:xlsx`  <br/> |Todos os arquivos do Excel (Excel 2007 e posterior)  <br/> |
|FileName  <br/> |O nome de um arquivo.  <br/> |`filename:"marketing plan"`  <br/> `filename:estimate`  <br/> |O primeiro exemplo retorna os arquivos com a frase exata "plano de marketing" no título. O segundo exemplo retorna arquivos com a palavra "estimativa" no nome de arquivo.  <br/> |
|LastModifiedTime  <br/> |A data em que um item foi alterado pela última vez.  <br/> |`lastmodifiedtime\>=05/01/2016`  <br/> `lastmodifiedtime\>=05/10/2016 AND lastmodifiedtime\<=06/1/2016`  <br/> |O primeiro exemplo retorna os itens que foram alterados em ou após 1 de maio de 2016. O segundo exemplo retorna itens alterados entre 1 de maio de 2016 e 1 de junho de 2016.  <br/> |
|ModifiedBy  <br/> |A pessoa que a última alteração de um item. Certifique-se de usar o nome para exibição do usuário para essa propriedade.  <br/> |`modifiedby:"Garth Fort"`  <br/> |Todos os itens que foram alterados pela última vez por Paulo Araújo.  <br/> |
|Path  <br/> |O caminho (URL) de uma pasta específica em um SharePoint ou OneDrive para o site de negócios. Se você usar essa propriedade, certifique-se de pesquisar no site localizado na pasta especificada.<br/> Para retornar a itens localizados em subpastas na pasta que você especificar para a propriedade path, você precisa adicionar /\* para a URL da pasta especificada; Por exemplo, `path: https://contoso.sharepoint.com/Shared Documents/*`.  <br/> <br/> **Observação:** Usando o `Path` propriedade pesquisar OneDrive locais não devolvem arquivos de mídia, como arquivos. png,. wav ou. TIFF, nos resultados da pesquisa. Use uma propriedade de site diferente em sua consulta de pesquisa para pesquisar os arquivos de mídia nas pastas de OneDrive.<br/> <br/> Para obter mais informações sobre como pesquisar a propriedade Path e usando um script para obter as URLs de caminho das pastas em um site específico, consulte [Uso de pesquisa de conteúdo no Office 365 para conjuntos de destino](use-content-search-for-targeted-collections.md).  <br/> |`path:https://contoso-my.sharepoint.com/personal/garthf_contoso_com/Documents/Private`  <br/> `path:"https://contoso-my.sharepoint.com/personal/garthf_contoso_com/Documents/Shared with Everyone/\*" AND filename:confidential`  <br/> |O primeiro exemplo retorna todos os itens em OneDrive especificado para a pasta de negócios. O segundo exemplo retorna os documentos que contêm a palavra "confidencial" no nome do arquivo na pasta do site especificado (e todas as subpastas).  <br/> |
|SharedWithUsersOWSUser  <br/> |Documentos que foram compartilhados com o usuário especificado e exibidos na página **compartilhado** no OneDrive do usuário para o site de negócios. Esses são os documentos que foram explicitamente compartilhados com o usuário especificado por outras pessoas em sua organização. Quando você exporta documentos que correspondem a uma consulta de pesquisa que usa a propriedade SharedWithUsersOWSUser, os documentos são exportados a localização original de conteúdo da pessoa compartilhado do documento com o usuário especificado. Para obter mais detalhes, consulte [pesquisando para conteúdos de sites compartilhados dentro da sua organização](keyword-queries-and-search-conditions.md#internal).<br/> |`sharedwithusersowsuser:garthf`  <br/> `sharedwithusersowsuser:"garthf@contoso.com"`  <br/> |Os dois exemplos retornam todos os documentos internos que foram explicitamente compartilhados com Garth Fort e que aparecem na página **compartilhado** na Garth Fort OneDrive for Business account.  <br/> |
|Site  <br/> |A URL de um site ou grupo de sites em sua organização.  <br/> |`site:https://contoso-my.sharepoint.com`  <br/> `site:https://contoso.sharepoint.com/sites/teams`  <br/> |O primeiro exemplo retorna os itens de OneDrive para sites corporativos para todos os usuários na organização. O segundo exemplo retorna os itens de todos os sites de equipe.  <br/> |
|Tamanho  <br/> |O tamanho de um item, em bytes.  <br/> |`size\>=1`  <br/> `size:1..10000`  <br/> |O primeiro exemplo retorna itens com mais de 1 byte. O segundo exemplo retorna itens de 1 a 10.000 bytes de tamanho.  <br/> |
|Título  <br/> |O título do documento. A propriedade Title é metadados especificada em documentos do Microsoft Office. É diferente do nome do arquivo do documento.  <br/> |`title:"communication plan"`  <br/> |Qualquer documento que contém a frase "plano de comunicação" na propriedade de metadados Title de um documento do Office.  <br/> |
   
## <a name="searchable-contact-properties"></a>Propriedades do contato pesquisáveis

A tabela a seguir lista as propriedades de contato que são indexadas e que você pode pesquisar usando a pesquisa de conteúdo. Essas são as propriedades que estão disponíveis para os usuários configurem para os contatos (também chamados de contatos pessoais) que estão localizados no catálogo de endereços de pessoal da caixa de correio do usuário. Para procurar contatos, você pode selecionar as caixas de correio para pesquisar e, em seguida, use uma ou mais propriedades de visita na consulta de palavra-chave.
  
> [!TIP]
> Para procurar por valores que contêm espaços, use aspas duplas ("??") para conter a frase; Por exemplo, `businessaddress:"123 Main Street"`. 
  
|**Propriedade**|**Descrição da propriedade**|
|:-----|:-----|
|BusinessAddress  <br/> |O endereço na propriedade **Endereço comercial** . A propriedade também é chamada de endereço de **trabalho** na página Propriedades do contato.<br/> |
|Telefone comercial  <br/> |O número de telefone em qualquer uma do **Telefone comercial** do número de propriedades.  <br/> |
|CompanyName  <br/> |O nome na propriedade **empresa** .  <br/> |
|Departamento  <br/> |O nome na propriedade **departamento** .  <br/> |
|DisplayName  <br/> |O nome de exibição do contato. Este é o nome na propriedade **Nome completo** do contato.<br/> |
|EmailAddress  <br/> |O endereço de qualquer propriedade de endereço de email do contato. Observe que os usuários podem adicionar vários endereços de email para um contato. O uso desta propriedade retornaria contatos que correspondem a qualquer um dos endereços de email do contato.  <br/> |
|FileAs  <br/> |A propriedade de **arquivo como** . Essa propriedade é usada para especificar como o contato está listado na lista de contatos do usuário. Por exemplo, um contato pode ser escutado como *FirstName, LastName* ou *LastName, FirstName* .<br/> |
|GivenName  <br/> |O nome na propriedade **Name do primeiro** .  <br/> |
|HomeAddress  <br/> |O endereço em qualquer uma das propriedades do endereço **inicial** .  <br/> |
|HomePhone  <br/> |O número de telefone em qualquer uma das telefone **residencial** numerar propriedades.  <br/> |
|IMAddress  <br/> |A propriedade de endereço de mensagens Instantâneas, que normalmente é um endereço de email usado para mensagens instantâneas.  <br/> |
|MiddleName  <br/> |O nome na propriedade name **intermediário** .  <br/> |
|MobilePhone  <br/> |Propriedade número do número de telefone no telefone **celular** .  <br/> |
|Nickname  <br/> |O nome na propriedade **Nickname** .  <br/> |
|Local do escritório  <br/> |Valor da propriedade de **escritório** ou **local do escritório** .  <br/> |
|OtherAddress  <br/> |O valor da propriedade de **outros** de endereço.  <br/> |
|Sobrenome  <br/> |O nome na **última** propriedade name.  <br/> |
|Cargo  <br/> |O título na propriedade **cargo** .  <br/> |
   

## <a name="searchable-sensitive-data-types"></a>Tipos de dados confidenciais pesquisáveis

Você pode usar o recurso de pesquisa de conteúdo na segurança &amp; Centro de conformidade para pesquisar dados confidenciais, como números de cartão de crédito ou seguridade social, que é armazenado em documentos no SharePoint e OneDrive para sites corporativos. Você pode fazer isso usando o `SensitiveType` digite de propriedade e o nome de um informações confidenciais em uma consulta de palavra-chave. Por exemplo, a consulta `SensitiveType:"Credit Card Number"` retorna os documentos que contiverem um número de cartão de crédito. A consulta `SensitiveType:"U.S. Social Security Number (SSN)"` retorna os documentos que contém um número de seguridade social dos EUA. Para ver uma lista dos tipos de dados confidenciais que você pode procurar, vá para **classificações** \> **tipos de informações confidenciais** na segurança &amp; Centro de conformidade. Ou você pode usar o cmdlet **Get-DlpSensitiveInformationType** na segurança &amp; PowerShell do Centro de conformidade para exibir uma lista dos tipos de informações confidenciais. 
  
Você também pode usar o `SensitiveType` propriedade para procurar o nome de um tipo de informações confidenciais personalizadas que você (ou outro administrador) criado para sua organização. Observe que você pode usar a coluna do **Publisher** na página **tipos de informações confidenciais** na segurança &amp; Centro de conformidade (ou a propriedade **Publisher** no PowerShell) para diferenciar entre confidenciais internas e personalizadas tipos de informações. Para obter mais informações, consulte [criar um tipo de informação confidencial personalizado](create-a-custom-sensitive-information-type.md).
  
Para obter mais informações sobre como criar consultas usando o `SensitiveType` propriedade, consulte o [formulário uma consulta para localizar dados confidenciais armazenados em sites](form-a-query-to-find-sensitive-data-stored-on-sites.md).
  
## <a name="search-operators"></a>Operadores de pesquisa

Operadores de pesquisa booleana, **AND**, **OR**e **não**, ajudam você a definir a pesquisa precisa de mais incluindo ou excluindo palavras específicas na consulta de pesquisa. Outras técnicas, como o uso de operadores de propriedade (como \>= ou …), aspas, parênteses e caracteres curinga, ajudá-lo a refinar uma consulta de pesquisa. A tabela a seguir lista os operadores que você pode usar para limitar ou ampliar os resultados da pesquisa. 
  
|**Operador**|**Usage**|**Descrição**|
|:-----|:-----|:-----|
|AND  <br/> |palavra-chave1 AND palavra-chave2  <br/> |Retorna os itens que incluem todas as palavras-chave especificada ou `property:value` expressões. Por exemplo, `from:"Ann Beebe" AND subject:northwind` retornaria todas as mensagens enviadas por Ann Beebe que continha o word northwind na linha de assunto. <sup>2</sup> <br/> |
|+  <br/> |keyword1?? + keyword2?? + keyword3  <br/> |Retorna os itens que contenham *uma* `keyword2` ou `keyword3` *e* que também contêm `keyword1`. Portanto, este exemplo é equivalente à consulta `(keyword2 OR keyword3) AND keyword1`.  <br/> Observe que a consulta `keyword1 + keyword2` (com um espaço após o **+** símbolo) não é o mesmo que usar o * * e * * operador. Esta consulta seria equivalente à `"keyword1 + keyword2"` e retornar itens com a fase exata `"keyword1 + keyword2"`.<br/> |
|OR  <br/> |palavra-chave1 OR palavra-chave2  <br/> |Retorna os itens que incluem um ou mais das palavras-chave especificadas ou `property:value` expressões. <sup>2</sup> <br/> |
|NOT  <br/> |palavra-chave1 NOT palavra-chave2  <br/> NOT from:"Clara Barbosa"  <br/> Tipo: mensagem instantânea  <br/> |Exclui os itens especificados por uma palavra-chave ou um `property:value` expressão. No segundo exemplo exclui as mensagens enviadas por Ann Beebe. O exemplo de terceiro exclui qualquer conversas de mensagens instantâneas, como Skype para conversas de negócios que são salvas na pasta de caixa de correio do histórico de conversa. <sup>2</sup> <br/> |
|-  <br/> |palavra-chave1 -palavra-chave2  <br/> |O mesmo que o operador **não** . Portanto, essa consulta retorna itens que contenham `keyword1` e seria excluir itens que contenham `keyword2`.<br/> |
|NEAR  <br/> |palavra-chave1 NEAR(n) palavra-chave2  <br/> |Retorna os itens com palavras próximos uns aos outros, onde n é igual o número de palavras separadamente. Por exemplo, `best NEAR(5) worst` retorna qualquer item onde a palavra "pior" é dentro de cinco palavras das "melhor". Se nenhum número for especificado, a distância padrão é oito palavras. <sup>2</sup> <br/> |
|ONEAR  <br/> |palavra-chave1 ONEAR(n) palavra-chave2  <br/> |Semelhante ao **próximo**, mas retorna itens com palavras que estão próximas umas das outras na ordem especificada. Por exemplo, `best ONEAR(5) worst` retorna qualquer item onde a palavra "melhor" ocorre antes da palavra "pior" e as duas palavras estão entre cinco palavras umas das outras. Se nenhum número for especificado, a distância padrão é oito palavras. <sup>2</sup> <br/> > [!NOTE]> O operador **ONEAR** não é suportado ao pesquisar caixas de correio; funciona apenas durante a pesquisa do SharePoint e OneDrive para sites corporativos. Se você estiver pesquisando caixas de correio e de sites na mesma pesquisa e a consulta inclui o operador **ONEAR** , a pesquisa retornará itens de caixa de correio, como se estivesse usando o operador **NEAR** . Em outras palavras, a pesquisa retorna itens nos quais são as palavras especificadas próximas umas das outras independentemente da ordem na qual as palavras ocorrem.           |
|:  <br/> |property:valor  <br/> |Dois-pontos (:) no `property:value` sintaxe especifica que o valor da propriedade que está sendo pesquisado contém o valor especificado. Por exemplo, `recipients:garthf@contoso.com` retorna qualquer mensagem enviada ao garthf@contoso.com.<br/> |
|=  <br/> |property=valor  <br/> |O mesmo que o operador **:** .  <br/> |
|\<  <br/> |propriedade\<valor  <br/> |Indica que a propriedade que está sendo pesquisada é menor do que o valor especificado. <sup>1</sup> <br/> |
|\>  <br/> |propriedade\>valor  <br/> |Indica que a propriedade que está sendo pesquisada é maior do que o valor especificado.<sup>1</sup> <br/> |
|\<=  <br/> |propriedade\<= value  <br/> |Indica que a propriedade que está sendo pesquisada é menor ou igual a um valor específico.<sup>1</sup> <br/> |
|\>=  <br/> |propriedade\>= value  <br/> |Indica que a propriedade que está sendo pesquisada é maior ou igual a um valor específico.<sup>1</sup> <br/> |
|..  <br/> |propriedade: valor1.. Value2  <br/> |Indica que a propriedade que está sendo pesquisada é maior ou igual a valor1 e menor ou igual a valor2.<sup>1</sup> <br/> |
|"  "  <br/> |"valor justo"  <br/> assunto:"Finanças trimestrais"  <br/> |Usar aspas duplas ("") para pesquisar uma frase exata ou o termo de palavra-chave e `property:value` consultas de pesquisa.  <br/> |
|\*  <br/> |gato\*  <br/> Assunto: set\*  <br/> |Pesquisas de curinga prefixo (onde o asterisco é colocado no final de uma palavra) correspondem para zero ou mais caracteres em palavras-chave ou `property:value` consultas. Por exemplo, `title:set*` retorna os documentos que contenham o conjunto do word, o programa de instalação e configuração (e outras palavras que começam com "set") no título do documento.<br/><br/> **Observação:** Você pode usar somente o prefixo curinga pesquisas; Por exemplo, **cat\* ** ou **definir\***. Pesquisas de sufixo ( ** \*cat** ), pesquisas de infixo ( **c\*t** ) e pesquisas de subcadeia de caracteres ( ** \*cat\* ** ) não são suportados.           |
|(  )  <br/> | (justo OR grátis) AND (from:contoso.com)  <br/>  (IPO OR inicial) AND (ação OR títulos)  <br/>  (finanças trimestrais)  <br/> |Parênteses agrupar Boolean frases, `property:value` itens e palavras-chave. Por exemplo, `(quarterly financials)` retorna itens que contêm as palavras trimestrais e financials.<br/> |
   
> [!NOTE]
> <sup>1</sup>??????Use este operador para propriedades que possuem valores de data ou numérico. > operadores de pesquisa <sup>2</sup>??????Boolean devem estar em maiusculas; Por exemplo, **AND**. Se você usar um operador minúsculo, como **e**, ele será tratado como uma palavra-chave na consulta de pesquisa. 
  
## <a name="search-conditions"></a>Condições de pesquisa

Você pode adicionar condições para uma consulta de pesquisa para restringir uma pesquisa e retornar um conjunto mais refinado de resultados. Cada condição adiciona uma cláusula à consulta KQL pesquisa que é criada e executada quando você iniciar a pesquisa.
  
[Condições para propriedades comuns ](#conditions-for-common-properties)

[Condições para propriedades de email](#conditions-for-mail-properties)

[Condições para propriedades de documentos](#conditions-for-document-properties)

[Operadores usados com condições](#operators-used-with-conditions)

[Diretrizes para o uso de condições](#guidelines-for-using-conditions)

[Exemplos](#examples-of-using-conditions-in-search-queries)
  
### <a name="conditions-for-common-properties"></a>Condições para propriedades comuns 

Crie uma condição usando as propriedades comuns durante a pesquisa de caixas de correio e de sites na mesma pesquisa. A tabela a seguir lista as propriedades disponíveis para usar quando estiver adicionando uma condição.
  
|**Condição**|**Descrição**|
|:-----|:-----|
|Data  <br/> |Para email, a data em que a mensagem foi recebida por um destinatário ou enviada pelo remetente. Para documentos, a data em que um documento da última modificação.  <br/> |
|Remetente/Autor  <br/> |Para email, a pessoa que enviou uma mensagem. Para documentos, a pessoa citada no campo autor dos documentos do Office. Você pode digitar o nome de mais de um, separado por vírgulas. Dois ou mais valores são conectados logicamente pelo operador **ou** .<br/> |
|Tamanho (em bytes)  <br/> |Para emails e documentos, o tamanho do item (em bytes).  <br/> |
|Assunto/Título  <br/> |Para email, o texto na linha de assunto de uma mensagem. Para documentos, o título do documento. Conforme explicado anteriormente, a propriedade Title é especificado em documentos do Microsoft Office de metadados. Você pode digitar o nome do assunto/título mais de um, separado por vírgulas. Dois ou mais valores são conectados logicamente pelo operador **ou** .<br/> |
|Marca de conformidade  <br/> |Para email e documentos, rótulos que têm a incumbência documentos e mensagens automaticamente por políticas de rótulo ou etiquetas que foram atribuídos manualmente pelos usuários. Rótulos são usados para classificar documentos governança de dados e email e impor regras de retenção com base na classificação do definidos pelo rótulo. Você pode digitar a parte do nome do rótulo e, em seguida, usar um curinga ou digite o nome de rótulo completa. Para obter mais informações, consulte [Overview of rótulos no Office 365](labels.md).<br/> |
  
### <a name="conditions-for-mail-properties"></a>Condições para propriedades de email

Crie uma condição usando propriedades de email ao pesquisar caixas de correio ou pastas públicas. A tabela a seguir lista as propriedades de email que você pode usar para uma condição. Observe que essas propriedades são um subconjunto das propriedades de email que foram descritas anteriormente. Essas descrições são repetidas para sua conveniência.
  
|**Condição**|**Descrição**|
|:-----|:-----|
|Tipo de mensagem  <br/> | O tipo de mensagem a ser pesquisado. Esta é a mesma propriedade como a propriedade Kind email. Valores possíveis:  <br/><br/>  contatos  <br/>  documentos  <br/>  email  <br/>  externaldata  <br/>  faxes  <br/>  mensagem instantânea  <br/>  diários  <br/>  reuniões  <br/>  microsoftteams  <br/>  observações  <br/>  postagens  <br/>  rssfeeds  <br/>  tarefas  <br/>  caixa postal  <br/> |
|Participants  <br/> |Todos os campos de pessoas em uma mensagem de email; os campos são De, Para, Cc e Cco.  <br/> |
|Tipo  <br/> |A propriedade de classe de mensagem para um item de email. Esta é a mesma propriedade como a propriedade de email ItemClass. Também é uma condição de valor múltiplos. Portanto, para selecionar várias classes de mensagem, mantenha pressionada a tecla **CTRL** e clique em dois ou mais classes de mensagens na lista suspensa que você deseja adicionar à condição. Cada classe de mensagem que você seleciona na lista será conectado logicamente pelo operador **ou** na consulta de pesquisa correspondente.<br/> Para obter uma lista das classes de mensagem (e sua ID de classe de mensagem correspondente) que são usados pelo Exchange e que podem ser selecionados na lista de **classe de mensagem** , consulte [tipos de Item e Classes de mensagens](https://go.microsoft.com/fwlink/?linkid=848143).  <br/> |
|Recebido  <br/> |A data em que uma mensagem de email foi recebida pelo destinatário. Essa propriedade é igual à propriedade de email Received.  <br/> |
|Destinatários  <br/> |A pessoa uma mensagem de email foi enviada para. Esta é a mesma propriedade como a propriedade de email To.  <br/> |
|Sender  <br/> |O remetente de uma mensagem de email.  <br/> |
|Enviado  <br/> |A data em que uma mensagem de email foi enviada pelo remetente. Esta é a mesma propriedade como a propriedade de email enviadas.  <br/> |
|Subject  <br/> |O texto na linha de assunto de uma mensagem de email.  <br/> |
|Para  <br/> |O destinatário de uma mensagem de email.  <br/> |
  
### <a name="conditions-for-document-properties"></a>Condições para propriedades de documentos

Crie uma condição usando propriedades de documento durante a pesquisa de documentos no SharePoint e OneDrive para sites corporativos. A tabela a seguir lista as propriedades de documento que você pode usar uma condição. Observe que essas propriedades são um subconjunto das propriedades do site que foram descritos anteriormente; Essas descrições são repetidas para sua conveniência.
  
|**Condição**|**Descrição**|
|:-----|:-----|
|Autor  <br/> |O campo autor dos documentos do Office, do qual persiste se um documento é copiado. Por exemplo, se um usuário cria um documento e os e-mails-la a alguém que carrega-lo no SharePoint, o documento ainda manterá o autor original.  <br/> |
|Cargo  <br/> |O título do documento. A propriedade Title é metadados especificada em documentos do Office. É diferente do nome de arquivo do documento.  <br/> |
|Created  <br/> |A data em que um documento foi criado.  <br/> |
|Modificado pela última vez  <br/> |A data em que um documento foi alterado pela última vez.  <br/> |
|Tipo de arquivo  <br/> |A extensão de um arquivo; Por exemplo, docx, um, pptx ou xlsx. Esta é a mesma propriedade como a propriedade do site ExtensãoDeArquivo.  <br/> |
  
### <a name="operators-used-with-conditions"></a>Operadores usados com condições

Ao adicionar uma condição, você pode selecionar um operador que é relevante para o tipo de propriedade da condição. A tabela a seguir descreve os operadores que são usados com condições e lista o equivalente que é usado na consulta de pesquisa.
  
|**Operador**|**Equivalente de consulta**|**Descrição**|
|:-----|:-----|:-----|
|After  <br/> |`property\>date`  <br/> |Usado com condições de data. Retorna itens que foram enviados, recebidos ou modificados após a data especificada.   <br/> |
|Antes  <br/> |`property\<date`  <br/> |Usado com condições de data. Retorna itens que foram enviados, recebidos ou modificados antes da data especificada.  <br/> |
|Entre  <br/> |`date..date`  <br/> |Use com as condições de data e tamanho. Quando usado com uma condição de data, retorna itens lá foram enviadas, recebidas ou modificados dentro do intervalo de datas especificado. Quando usado com uma condição de tamanho, retorna os itens cujo tamanho é dentro do intervalo especificado.  <br/> |
|Contains any of  <br/> |`(property:value) OR (property:value)`  <br/> |Usada com condições para propriedades que especificam um valor string. Retorna os itens que contenham qualquer parte de um ou mais valores de cadeia de caracteres especificada.  <br/> |
|Doesn't contain any of  <br/> |`-property:value`  <br/> `NOT property:value`  <br/> |Usado com condições para propriedades que especificam um valor de cadeia de caracteres. Retorna itens que não contêm qualquer parte do valor da cadeia de caracteres especificada.  <br/> |
|Doesn't equal any of
  <br/> |`-property=value`  <br/> `NOT property=value`  <br/> |Usado com condições para propriedades que especificam um valor de cadeia de caracteres. Retorna itens que não contêm a cadeia de caracteres específica.  <br/> |
|Igual a  <br/> |`size=value`  <br/> |Retorna itens que são iguais ao tamanho especificado.<sup>1</sup> <br/> |
|Igual a qualquer  <br/> |`(property=value) OR (property=value)`  <br/> |Usado com condições para propriedades que especificam um valor de cadeia de caracteres. Retorna itens que são uma correspondência exata de um ou mais valores da cadeia de caracteres especificada.  <br/> |
|Maior que  <br/> |`size>value`  <br/> |Retorna itens em que a propriedade especificada é maior do que o valor especificado.<sup>1</sup> <br/> |
|Greater or equal  <br/> |`size>=value`  <br/> |Retorna itens em que a propriedade especificada é maior ou igual ao valor especificado.<sup>1</sup> <br/> |
|Menor que  <br/> |`size<value`  <br/> |Retorna itens que são maiores ou iguais ao valor específico.<sup>1</sup> <br/> |
|Less or equal  <br/> |`size<=value`  <br/> |Retorna itens que são maiores ou iguais ao valor específico.<sup>1</sup> <br/> |
|Not equal  <br/> |`size<>value`  <br/> | Retorna itens que não são iguais ao tamanho especificado.<sup>1</sup> <br/> |
   
> [!NOTE]
> <sup>1</sup> este operador está disponível somente para as condições que usam a propriedade Size. 
  
### <a name="guidelines-for-using-conditions"></a>Diretrizes para o uso de condições

Lembre-se do seguinte ao usar condições de pesquisa.
  
- Uma condição logicamente está conectada à consulta de palavra-chave (especificada na caixa de palavra-chave) pelo operador **e** . Isso significa que itens precisam satisfazer tanto a consulta de palavra-chave e a condição a ser incluído nos resultados. Isso é como ajudam a condições para restringir os resultados. 
    
- Se você adicionar duas ou mais condições exclusivas para uma consulta de pesquisa (condições que especificam as propriedades diferentes), essas condições logicamente são conectadas pelo operador **AND** . Isso significa que apenas os itens que satisfazem todas as condições (além de qualquer consulta de palavra-chave) são retornados. 
    
- Se você adicionar mais de uma condição para a mesma propriedade, essas condições logicamente são conectadas pelo operador **OR** . Isso significa que os itens que satisfazem a consulta de palavra-chave e qualquer uma das condições são retornados. Então, conectados uns aos outros grupos das condições mesmos pelo operador **ou** e, em seguida, os conjuntos de condições exclusivos são conectados pelo operador **AND** . 
    
- Se você adicionar vários valores (separados por vírgulas ou ponto e vírgula) a uma única condição, esses valores são conectados pelo operador **OR** . Isso significa que itens são retornados caso eles contenham qualquer um dos valores especificados para a propriedade da condição. 
    
- A consulta de pesquisa que é criada usando a caixa palavras-chave e condições é exibida na página da **pesquisa** , no painel de detalhes para a pesquisa selecionado. Em uma consulta, tudo à direita da notação `(c:c)` indica as condições que são adicionadas à consulta. 
    
- Condições apenas adicionar propriedades a consulta de pesquisa; o não adicionar operadores. Esse é o motivo pelo qual a consulta exibida no painel de detalhes não mostra os operadores à direita do `(c:c)` notação. KQL adiciona os operadores lógicos (de acordo com as regras explicadas anteriormente) quando a execução da consulta. 
    
- Você pode usar o recurso de arrastar e soltar o controle para sequenciar novamente a ordem das condições. Basta clicar no controle uma condição e movê-lo para cima ou para baixo.
    
- Conforme explicado anteriormente, algumas propriedades de condição permitem que você digitar vários valores. Cada valor logicamente está conectado pelo operador **ou** . Isso resulta na mesma lógica como tendo várias instâncias da mesma condição, onde cada uma tem um valor único. As ilustrações a seguir mostra um exemplo de uma única condição com vários valores e um exemplo de várias condições (para a mesma propriedade) com um único valor. Os dois exemplos resultam na mesma consulta:`(filetype="docx") OR (filetype="pptx") OR (filetype="xlsx")`
    
    ![Uma condição com vários valores](media/9880aa29-d117-4531-be20-6d53f1d21341.gif)
  
    ![Vários critérios de pesquisa para a mesma propriedade](media/1e63d37d-6d8d-4c9b-a509-a7e1c3a05193.gif)
  
> [!TIP]
> Se uma condição aceita vários valores, recomendamos que você use uma única condição e especifique vários valores (separados por vírgulas ou ponto-e-vírgula). Isso ajuda a garantir que a lógica de consulta aplicada seja o que você deseja. 
  
### <a name="examples-of-using-conditions-in-search-queries"></a>Exemplos

Os exemplos abaixo mostram a versão baseada em GUI de uma consulta de pesquisa com condições, a sintaxe de consulta de pesquisa que é exibido no painel de detalhes da pesquisa selecionada (que também é retornada pelo cmdlet **Get-ComplianceSearch** ) e a lógica do consulta KQL correspondente. 
  
#### <a name="example-1"></a>Exemplo 1

Este exemplo retorna a documentos no SharePoint e OneDrive para sites corporativos que contiverem um número de cartão de crédito e modificados pela última vez antes de 1 de janeiro de 2016.
  
 **GUI**
  
![Primeiro exemplo de critérios de pesquisa](media/099515ba-d4ee-474e-af25-3aa48816b87b.gif)
  
 **Sintaxe de consulta de pesquisa**
  
 `SensitiveType:"Credit Card Number(c:c)(lastmodifiedtime<2016-01-01)`
  
 **Lógica de consulta de pesquisa**
  
 `SensitiveType:"Credit Card Number" AND (lastmodifiedtime<2016-01-01)`
  
#### <a name="example-2"></a>Exemplo 2

O exemplo retorna itens de email ou documentos que contêm a palavra-chave "relatório", que foram enviados ou criados antes de 1º de abril de 2015 e que contêm a palavra "northwind" no campo de assunto de mensagens de email ou na propriedade title de documentos. A consulta exclui páginas da Web que atendem aos outros critérios de pesquisa. 
  
 **GUI**
  
![Segundo exemplo de critérios de pesquisa](media/fe07d495-df81-42da-8106-3cdb409c6e7f.gif)
  
 **Sintaxe de consulta de pesquisa**
  
 `report???(c:c)??????(date<2016-04-01)??????(subjecttitle:"northwind")??????(-filetype="aspx")???`
  
 **Lógica de consulta de pesquisa**
  
 `report AND (date<2016-04-01) AND (subjecttitle:"northwind") NOT (filetype="aspx")`
  
#### <a name="example-3"></a>Exemplo 3
<a name="conditionexamples"> </a>

Este exemplo retorna as mensagens de email ou reuniões de calendário que foram enviados entre 1/12/2016 e 11/30/2016 e que contêm palavras que começam com "telefone" ou "smartphone".
  
 **GUI**
  
![Terceiro exemplo de critérios de pesquisa](media/973d45fc-0923-43d6-9d0a-25e4a625f057.gif)
  
 **Sintaxe de consulta de pesquisa**
  
 `phone* OR smartphone*(c:c)(sent=2016-12-01..2016-11-30)(kind="email")(kind="meetings")`
  
 **Lógica de consulta de pesquisa**
  
 `phone* OR smartphone* AND (sent=2016-12-01..2016-11-30) AND ((kind="email") OR (kind="meetings"))`
  
## <a name="searching-for-site-content-shared-with-external-users"></a>Pesquisar conteúdo de site compartilhado com usuários externos

Você também pode usar o recurso de pesquisa de conteúdo na segurança &amp; Centro de conformidade para procurar documentos armazenados no SharePoint e OneDrive para sites corporativos que foram compartilhados com pessoas fora da sua organização. Isso pode ajudá-lo a identificar informações confidenciais ou proprietárias que está sendo compartilhadas fora da sua organização. Você pode fazer isso usando o `ViewableByExternalUsers` propriedade em uma consulta de palavra-chave. Esta propriedade retornará documentos ou sites que foram compartilhados com usuários externos usando um dos métodos de compartilhamento a seguir: 
  
- Um convite de compartilhamento que requer que os usuários entrar em sua organização como um usuário autenticado.
    
- Um link de convidado anônimo, que permite que qualquer pessoa com esse link para acessar o recurso sem precisar ser autenticado.
    
Estes são alguns exemplos:
  
- A consulta `ViewableByExternalUsers:true AND SensitiveType:"Credit Card Number"` retornará todos os itens que foram compartilhados com pessoas fora da sua organização e contiverem um número de cartão de crédito. 
    
- A consulta `ViewableByExternalUsers:true AND ContentType:document AND Site:https://contoso.sharepoint.com/Sites/Teams` retornará uma lista de documentos em todos os sites de equipe na organização que foram compartilhados com usuários externos. 
    
> [!TIP]
> Uma consulta de pesquisa, como `ViewableByExternalUsers:true AND ContentType:document` pode retornar muitos dos arquivos. aspx nos resultados da pesquisa. Para eliminar essas (ou outros tipos de arquivos), você pode usar o `FileExtension` propriedade para excluir tipos de arquivo específicos; Por exemplo `ViewableByExternalUsers:true AND ContentType:document NOT FileExtension:aspx`. 
  
O que é considerado o conteúdo que é compartilhado com pessoas fora da sua organização? Documentos do SharePoint e OneDrive da sua organização para sites corporativos que são compartilhadas, enviando um convites de compartilhamento ou que são compartilhadas em locais públicos. Por exemplo, as seguintes atividades do usuário resultam no conteúdo que é exibido por usuários externos:
  
- Um usuário compartilha um arquivo ou uma pasta com uma pessoa de fora da organização.

    
- Um usuário cria e envia um link para um arquivo compartilhado para uma pessoa fora da sua organização. Esse link permite que o usuário externo exibir o arquivo (ou editar uma).
    
- Um usuário envia um convite de compartilhamento ou um link de convidado a uma pessoa de fora da organização para exibir (ou editar) um arquivo compartilhado.
    
### <a name="issues-using-the-viewablebyexternalusers-property"></a>Use a propriedade ViewableByExternalUsers de problemas

Enquanto o `ViewableByExternalUsers` propriedade representa o status de um documento ou site é compartilhado com usuários externos, existem algumas advertências para que essa propriedade faz e refletir doesn???t. Nos cenários a seguir, o valor do `ViewableByExternalUsers` propriedade não será atualizada e os resultados de uma consulta de pesquisa de conteúdo que usa essa propriedade podem ser inadequados. 
  
- Alterações de compartilhamento de diretiva, como desativar o compartilhamento externo para um site ou para a organização. A propriedade ainda mostrará documentos compartilhados anteriormente como sendo acessível externamente, mesmo que o acesso externo pode ter sido revogado.
    
- Alterações de associação de grupo, adicionando ou removendo usuários externos aos grupos de segurança do Office 365 grupos ou do Office 365. A propriedade não será atualizada automaticamente para itens que o grupo tem acesso.
    
- Convites de compartilhamento de envio para usuários externos em que o destinatário ainda não aceita o convite e, portanto, não ainda têm acesso ao conteúdo.
    
Nesses cenários, o `ViewableByExternalUsers` propriedade não irão refletir o status de compartilhamento atual até o site ou biblioteca de documentos é rastreada novamente e reindexada. 

## <a name="searching-for-site-content-shared-within-your-organization"></a>Pesquisar conteúdo de site compartilhado dentro da sua organização

Conforme explicado anteriormente, você pode usar o `SharedWithUsersOWSUser` propriedade tão procurar documentos que foram compartilhados entre as pessoas na sua organização. Quando uma pessoa compartilha um arquivo (ou pasta) com outro usuário dentro da organização, um link para o arquivo compartilhado aparece na página **compartilhado** na OneDrive para a conta de negócios da pessoa que o arquivo foi compartilhado com. Por exemplo, para pesquisar os documentos que foram compartilhados com Sara Davis, você pode usar a consulta `SharedWithUsersOWSUser:"sarad@contoso.com"`. Se você exportar os resultados da pesquisa, os documentos originais (localizados no conteúdo local da pessoa que os documentos compartilhados com Sara) serão baixados.
  
Observe que os documentos devem ser compartilhados explicitamente com um usuário específico a serem retornadas nos resultados da pesquisa ao usar o `SharedWithUsersOWSUser` propriedade. Por exemplo, quando uma pessoa compartilha um documento em sua conta de OneDrive, eles tem a opção para compartilhá-lo com qualquer pessoa (dentro ou fora da organização), compartilhá-lo apenas com pessoas dentro da organização ou compartilhá-la com uma pessoa específica. Aqui está uma captura de tela da janela de **compartilhamento** no OneDrive, que mostra as três opções de compartilhamento. 
  
![Somente os arquivos compartilhados com pessoas específicas serão retornados por uma consulta de searcj que usa a propriedade SharedWithUsersOWSUser](media/469a4b61-68bd-4ab0-b612-ab6302973886.png)
  
Apenas os documentos que são compartilhados usando a terceira opção (compartilhada com **pessoas específicas**) serão retornados por uma consulta de pesquisa que usa a `SharedWithUsersOWSUser` propriedade. 

## <a name="search-tips-and-tricks"></a>Dicas e truques de pesquisa

- As pesquisas de palavra-chave não diferenciam maiúsculas de minúsculas. Por exemplo, **gato** e **GATO** retornam os mesmos resultados.  
    
- Os operadores booleanos **AND**, **ou**, **não**, **NEAR**e **ONEAR** devem estar em maiusculos. 
    
- Um espaço entre duas palavras-chave ou duas `property:value` expressões é o mesmo que usar **AND**. Por exemplo, `from:"Sara Davis" subject:reorganization` retorna todas as mensagens enviadas por Sara Davis que contêm a reorganização de word na linha de assunto. 
    
- Use uma sintaxe que corresponde a `property:value` formato. Valores não diferenciam maiusculas de minúsculas e eles não podem ter um espaço depois do operador. Se houver um espaço, o seu valor pretendido será apenas uma pesquisa de texto completo. Por exemplo `to: pilarp` pesquisas para "pilarp" como uma palavra-chave, em vez de para mensagens enviadas para pilarp. 
    
- Ao pesquisar uma propriedade de destinatário, como To, From, Cc ou Recipients, você pode usar um endereço SMTP, um alias ou um nome de exibição para indicar um destinatário. Por exemplo, você pode usar brendaf@contoso.com, brendaf ou "Brenda Fernandes".
    
- Você pode usar somente o prefixo curinga pesquisas; Por exemplo, **cat\* ** ou **definir\***. Pesquisas de sufixo ( ** \*cat** ), pesquisas de infixo ( **c\*t** ) e pesquisas de subcadeia de caracteres ( ** \*cat\* ** ) não são suportados. 
    
- Ao pesquisar uma propriedade, usar aspas duplas ("") se o valor de pesquisa consiste em várias palavras. Por exemplo `subject:budget Q1` retorna mensagens que contêm o **orçamento** na na linha de assunto e que contêm **T1** em qualquer lugar na mensagem ou em qualquer uma das propriedades de mensagem. Usando `subject:"budget Q1"` retorna todas as mensagens que contêm o **orçamento T1** em qualquer lugar na linha de assunto. 
    
- Para excluir o conteúdo marcado com um determinado valor de propriedade de seus resultados de pesquisa, coloque um sinal de menos (-) antes do nome da propriedade. Por exemplo, `-from:"Sara Davis"` excluirá todas as mensagens enviadas por Sara Davis. 

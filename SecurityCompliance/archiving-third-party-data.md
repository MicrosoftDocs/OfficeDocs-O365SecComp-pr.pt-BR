---
title: Arquivamento de dados de terceiros no Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 9/5/2017
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 0ce338d5-3666-4a18-86ab-c6910ff408cc
description: Os administradores podem importar dados de terceiros de plataformas de mídia social, as plataformas de mensagens instantâneas e plataformas de colaboração de documento para caixas de correio em sua organização do Office 365. Isso permite arquivar dados de fontes de dados, Twitter e Facebook no Office 365. Em seguida, você pode appply recursos de conformidade do Office 365 (por exemplo, retenção legal, pesquisa de conteúdo e políticas de retenção) aos dados de terceiros.
ms.openlocfilehash: 3d51d9f5cb546b33fa636fab0ca319e4d24b1ad4
ms.sourcegitcommit: edf5db9357c0d34573f8cc406314525ef10d1eb9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/28/2018
ms.locfileid: "23230033"
---
# <a name="archiving-third-party-data-in-office-365"></a>Arquivamento de dados de terceiros no Office 365

Permite os administradores importar e arquivar dados de terceiros de plataformas de mídia social, mensagens instantâneas plataformas e plataformas de colaboração de documento, a caixas de correio em sua organização do Office 365 do Office 365. Exemplos de fontes de dados de terceiros que podem ser importados para o Office 365 incluem o seguinte: 
  
- **Social** - Twitter, Facebook, LinkedIn e Yammer 
    
- **Mensagens instantâneas** - Jabber Cisco, GoogleTalk e Yahoo Messenger 
    
- **Colaboração de documentos** - caixa e a pasta de recados 
    
- **Setores verticais** - Customer Relationship Management (por exemplo, a equipe de vendas instabilidade) e Financials (por exemplo, Thomson Reuters e Bloomberg) 
    
- **Mensagens de SMS/texto** - BlackBerry 
    
Após a importação de dados de terceiros, você pode aplicar recursos de conformidade do Office 365 — como as políticas de retenção de litígio, pesquisa de conteúdo, arquivamento In-loco, auditoria e Office 365 — a esses dados. Por exemplo, quando uma caixa de correio for colocada em retenção de litígio, dados de terceiros serão preservados. Você pode pesquisar dados de terceiros usando a pesquisa de conteúdo. Ou você pode aplicar o arquivamento e políticas de retenção para dados de terceiros exatamente como você pode usar para dados da Microsoft. Em resumo, o arquivamento de dados de terceiros no Office 365 pode ajudar sua organização permanecer em conformidade com normas políticas e governamentais.
  
Aqui está uma visão geral do processo e as etapas necessárias para importar dados de terceiros para o Office 365.

[Etapa 1: encontrar um parceiro de dados de terceiros](#step-1-find-a-third-party-data-partner)

[Etapa 2: criar e configurar uma caixa de correio de dados de terceiros no Office 365](#step-2-create-and-configure-a-third-party-data-mailbox-in-office-365)

[Etapa 3: configurar caixas de correio de usuário para dados de terceiros](#step-3-configure-user-mailboxes-for-third-party-data)

[Etapa 4: fornecer informações ao seu parceiro](#step-4-provide-your-partner-with-information)

## <a name="how-the-third-party-data-import-process-works"></a>Como o processo de importação de dados de terceiros funciona >

A ilustração e a descrição a seguir explicam como funciona o processo de importação de dados de terceiros.
  
![Como funciona o processo de importação de dados de terceiros](media/5d4cf8e9-b4cc-4547-90c8-d12d04a9f0e7.png)
  
1. Cliente trabalha com seus parceiros de escolha para configurar um conector que irá extrair itens da fonte de dados de terceiros e depois importar os itens para o Office 365.
    
2. O conector de parceiro conecta-se às fontes de dados de terceiros por meio de uma API de terceiros (em uma base agendada ou configurado como) e extrai itens da fonte de dados. O conector de parceiro converte o conteúdo de um item em um formato de mensagem de email. Consulte a seção de [informações adicionais](#more-information) para obter uma descrição do esquema de formato de mensagem. 
    
3. Conector de parceiro conecta-se ao serviço Azure no Office 365 usando o serviço Web do Exchange (EWS) por meio de um ponto de extremidade conhecido.
    
4. Os itens são importados para a caixa de correio de um usuário específico ou para uma caixa de correio de dados de terceiros "pega-tudo". Os critérios a seguir definem se um item será importado para a caixa de correio de um usuário específico ou para a caixa de correio de dados de terceiros:
    
    r. **itens que têm uma ID de usuário que corresponde a uma conta de usuário do Office 365** - se o conector de parceiro pode mapear a ID de usuário do item na fonte de dados de terceiros para um usuário específico que ID no Office 365, o item é copiado para a pasta em que o usuário **limpa** Pasta de itens recuperáveis. Os usuários não podem acessar os itens na pasta limpezas. No entanto, você pode usar as ferramentas de descoberta eletrônica do Office 365 para procurar itens na pasta limpezas.
    
    b. **itens que não têm uma ID de usuário que corresponde a uma conta de usuário do Office 365** - se o conector de parceiro não pode mapear a ID de usuário de um item para um usuário específico que ID no Office 365, o item é copiado para a pasta de **caixa de entrada** da caixa de correio de dados de terceiros. Importação de itens na caixa de entrada permite a você ou alguém em sua organização para entrar na caixa de correio de terceiros para exibir e gerenciar esses itens e veja se qualquer ajustes precisam ser feitas na configuração do conector de parceiro.
 
## <a name="step-1-find-a-third-party-data-partner"></a>Etapa 1: encontrar um parceiro de dados de terceiros

Um componente essencial para arquivar dados de terceiros no Office 365 está encontrando e como trabalhar com um parceiro da Microsoft especializada na captura de dados de uma fonte de dados de terceiros e importá-lo para o Office 365. Depois que os dados são importados, podem ser arquivado e preservada juntamente com outros dados da Microsoft, como o email do Exchange e documentos do SharePoint e o OneDrive for Business da sua organização. Um parceiro cria um conector que extrai dados de fontes de dados de terceiros da sua organização (por exemplo, BlackBerry, Facebook, Google +, Reuters Thomson, Twitter e YouTube) e transmite dados para uma API do Office 365 que importa itens para caixas de correio do Exchange como mensagens de email. 
  
As seções a seguir listam os parceiros da Microsoft — e as fontes de dados de terceiros que eles suportam — que estão participando do programa para arquivar dados de terceiros no Office 365.

[17a-4 LLC](#17a-4-llc)
  
[Actiance](#actiance)
  
[ArchiveSocial](#archivesocial)
  
[Globanet](#globanet)
  
[OpenText](#opentext)
  
[Verba](#verba)
  
### <a name="17a-4-llc"></a>17a-4 LLC

17a-4 LLC é compatível com as seguintes fontes de dados de terceiros:
  
- BlackBerry
    
- Fluxos de dados do Bloomberg
    
- Cisco Jabber
    
- FactSet
    
- HipChat
    
- InvestEdge
    
- LivePerson
    
- 
MessageLabs Data Streams

    
- OpenText
    
- Oracle/ATG 'click-to-call' Live Help

    
- Pivot IMTRADER

    
- Microsoft SharePoint
    
- MindAlign
    
- Sitrion One (Newsgator)
    
- 
Skype for Business (Lync/OCS)
    
- 
Skype for Business Online (Lync Online)

    
- Bancos de dados SQL
    
- 
Squawker

    
- Thomson Reuters Eikon Messenger

  
### <a name="actiance"></a>Actiance

[Actiance](https://www.actiance.com) suporta as seguintes fontes de dados de terceiros: 
  
- OBJETIVO
    
- American Idol
    
- Apple Juice
    
- 
AOL with Pivot Client

    
- Ares
    
- Bazaar Voice
    
- Bear Share
    
- Bit Torrent
    
- BlackBerry Call Logs (v5, v10, v12)
    
- BlackBerry Messenger (v5, v10, v12)
    
- BlackBerry PIN (v5, v10, v12)
    
- BlackBerry SMS (v5, v10, v12)
    
- Bloomberg Mail

    
- CellTrust
    
- Importação de bate-papo

    
- Política e registros de bate-papo em tempo real

    
- Instabilidade

    
- Cisco IM &amp; servidor de presença (v9.0.1, v 9.1, v9.1.1 SU1, v10, v10.5.1 SU1)
    
- Cisco Unified Presence Server (v8.6.3, v8.6.4, v8.6.5)

    
- Importação de colaboração

    
- Registro de colaboração em tempo real

    
- Conexão Direta
    
- Facebook
    
- FactSet
    
- FastTrack
    
- Gnutella
    
- Google+

    
- GoToMyPC
    
- Hopster
    
- HubConnex
    
- IBM Connections (v3.0.1, v4.0, v4.5, v4.5 CR3, v5)

    
- IBM Connections Chat Cloud

    
- IBM Connections Social Cloud

    
- IBM SameTime Advanced 8.5.2 IFR1

    
- IBM SameTime Communicate 9.0

    
- IBM SameTime Community (v8.0.2, v8.5.1 IFR2, v8.5.2 IFR1, v9.1)

    
- IBM SameTime Complete 9.0

    
- IBM SameTime Conference 9.0

    
- IBM SameTime Meeting 8.5.2 IFR1

    
- ICE/YellowJacket
    
- Importação de mensagem Instantânea

    
- Política e registro de mensagem instantânea em tempo real

    
- Indii Messenger

    
- Instant Bloomberg

    
- IRC
    
- Jive

    
- Jive 6 Real Time Logging (v6, v7)

    
- Jive Import
    
- JXTA
    
- LinkedIn
    
- 
Microsoft Lync (2010, 2013)

    
- MFTP
    
- Microsoft Lync 2013 Voice

    
- Microsoft SharePoint (2010, 2013)

    
- Microsoft SharePoint Online
    
- Microsoft UC (Unified Communications)
    
- MindAlign
    
- Mobile Guard
    
- MSN
    
- My Space
    
- NEONetwork
    
- Office 365 Lync Dedicated

    
- Office 365 Shared IM

    
- Pinterest
    
- Tabela dinâmica
    
- QQ
    
- Skype for Business 2015
    
- SoftEther
    
- Symphony

    
- Thomson Reuters Eikon

    
- Thomson Reuters Messenger

    
- Tor
    
- TTT
    
- Twitter
    
- WinMX
    
- Winny
    
- Yahoo

    
- Yammer
    
- YouTube
    
  
### <a name="archivesocial"></a>ArchiveSocial

[ArchiveSocial](https://www.archivesocial.com) suporta as seguintes fontes de dados de terceiros: 
  
- Facebook
    
- Flickr

    
- Instagram

    
- LinkedIn
    
- Pinterest
    
- Twitter
    
- YouTube
    
- Vimeo
  
### <a name="globanet"></a>Globanet

[Globanet](https://www.globanet.com) suporta as seguintes fontes de dados de terceiros: 
  
- AOL with Pivot Client 
    
- BlackBerry Call Logs (v5, v10, v12)
    
- BlackBerry Messenger (v5, v10, v12)
    
- BlackBerry PIN (v5, v10, v12)
    
- BlackBerry SMS (v5, v10, v12)
    
- Bloomberg Chat

    
- Bloomberg Mail

    
- Box

    
- CipherCloud for Salesforce Chatter
    
- Cisco IM &amp; (v10, v10.5.1 SU1, v11.0, v11.5 SU2) do servidor de presença

- Cisco Webex equipes

- Espaço de trabalho do Citrix &amp; ShareFile

- CrowdCompass

- Arquivos de texto delimitado personalizado

    
- Arquivos XML personalizados

    
- Facebook (páginas)
    
- Factset

    
- FXConnect
    
- ICE Chat/YellowJacket
    
- Jive

    
- Macgregor XIP


- Microsoft Exchange Server
    
- Microsoft OneDrive for Business

- Microsoft Teams
       
- Microsoft Yammer

    
- Mobile Guard
    
- Tabela dinâmica
    
- Salesforce Chatter

- Skype for Business online
    
- Skype for Business, versões 2007 R2 - 2016 (local)

    
- Slack Enterprise Grid
    
- Symphony

    
- Thomson Reuters Eikon

    
- Thomson Reuters Messenger

    
- Thomson Reuters Dealings 3000 / FX Trading

    
- Twitter
    
- UBS Chat

    
- YouTube
  
### <a name="opentext"></a>OpenText

[OpenText](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) suporta as seguintes fontes de dados de terceiros: 
  
- Axs Encrypted
    
- Axs Exchange
    
- Axs Local Archive
    
- Axs PlaceHolder
    
- Axs Signed
    
- Bloomberg
    
- Thomson Reuters
  
### <a name="verba"></a>Verba

[Verba](https://www.verba.com) suporta as seguintes fontes de dados de terceiros: 
  
- Avaya Aura Video

    
- Avaya Aura Voice

    
- Avtec Radio

    
- Bosch/Telex Radio

    
- BroadSoft Vídeo

    
- BroadSoft Voice

    
- Centile Voice

    
- Cisco Jabber IM

    
- Cisco UC Video

    
- Cisco UC Voice

    
- Vídeo UCCX/UCCE Cisco
    
- Cisco UCCX/UCCE voz
    
- ESChat Radio
    
- Geoman Contact Expert
    
- IP Trade Voice

    
- Luware LUCS Contact Center
    
- Microsoft UC (Unified Communications)
    
- Mitel MiContact Center for Lync (prairieFyre) 

    
- Oracle / Acme Packet Session Border Controller Video  

    
- Oracle / Acme Packet Session Border Controller Voice

    
- Singtel Mobile Voice

    
- SIPREC Video
    
-  SIPREC Voice 
    
- Skype for Business / Lync IM

    
- Skype for Business / Lync Video

    
- Skype for Business / Lync Voice

    
- Speakerbus Voice

    
- Standard SIP/H.323 Video 

    
- Standard SIP/H.323 Voice 

    
- Truphone Voice

    
- TwistedPair Radio

    
- Windows Desktop Computer Screen 

  
## <a name="step-2-create-and-configure-a-third-party-data-mailbox-in-office-365"></a>Etapa 2: criar e configurar uma caixa de correio de dados de terceiros no Office 365

Aqui estão as etapas para criar e configurar uma caixa de correio de dados de terceiros para importar dados para o Office 365. Anterior conforme explicado, itens são importados para esta caixa de correio se o conector de parceiro não pode mapear a ID de usuário do item para uma conta de usuário do Office 365.
  
 **Concluir essas tarefas no Centro de administração do Office 365**
  
1. Criar uma nova conta de usuário no Office 365 e atribuí-lo uma licença do Exchange Online plano 2; consulte [Adicionar usuários para o Office 365](https://go.microsoft.com/fwlink/p/?LinkId=692098). É necessária uma licença de plano 2 para colocar a caixa de correio em retenção de litígio ou habilitar uma caixa de correio de arquivamento que tem uma cota de armazenamento ilimitado.
    
2. Adicione a conta de usuário para a caixa de correio de dados de terceiros para a função de administrador do **Exchange administrator** no Office 365; consulte [atribuir funções de administrador no Office 365](https://go.microsoft.com/fwlink/p/?LinkId=532393).
    
    > [!TIP]
    > Anote as credenciais da conta do usuário. Você precisa enviá-las para o seu parceiro, conforme descrito na Etapa 4. 
  
 **Concluir essas tarefas no Centro de administração do Exchange**
  
1. Ocultar a caixa de correio de dados de terceiros do catálogo de endereços e outras listas de endereços na organização; consulte [gerenciar caixas de correio do usuário](https://go.microsoft.com/fwlink/p/?LinkId=616058). Como alternativa, você pode executar o seguinte comando do PowerShell:
    
    ```
    Set-Mailbox -Identity <identity of third-party data mailbox> -HiddenFromAddressListsEnabled $true
    ```

2. Atribuir a permissão **FullAccess** para a caixa de correio de dados de terceiros para que os administradores ou oficiais de conformidade podem abrir a caixa de correio de dados de terceiros no cliente de desktop do Outlook; consulte [Manage permissions para destinatários](https://go.microsoft.com/fwlink/p/?LinkId=692104).
    
3. Habilite os seguintes recursos do Office 365 relacionados à conformidade para a caixa de correio de dados de terceiros:
    
    - Habilitar a caixa de correio de arquivo morto; consulte [Habilitar caixas de correio de arquivo morto no Office 365 Security &amp; Centro de conformidade](enable-archive-mailboxes.md) e [Habilitar o arquivamento ilimitado no Office 365](enable-unlimited-archiving.md). Isso permitirá que você espaço de armazenamento de livre-up, na caixa de correio principal, configurando uma política de arquivamento que move itens de dados de terceiros para a caixa de correio de arquivo morto. Isso fornecerá com armazenamento ilimitado para dados de terceiros.
    
    - Coloque a caixa de correio de dados de terceiros em retenção de litígio. Você também pode aplicar uma política de retenção do Office 365 no Office 365 Security &amp; Centro de conformidade. Fazer esta caixa de correio em espera reter itens de dados de terceiros (indefinidamente ou por um período especificado) e impedi-los de serem removidos da caixa de correio. Consulte um dos seguintes tópicos:
    
      - [Colocar uma caixa de correio em Retenção de litígio](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
      - [Visão geral das políticas de retenção no Office 365](retention-policies.md)
    
       
    
    - Habilitar a caixa de correio log de auditoria para acesso de proprietário, representante e admin na caixa de correio de dados de terceiros; consulte [Habilitar caixa de correio auditorias no Office 365](enable-mailbox-auditing.md). Isso permitirá a auditoria de todas as atividades realizadas por qualquer usuário que tenha acesso à caixa de correio de dados de terceiros.

## <a name="step-3-configure-user-mailboxes-for-third-party-data"></a>Etapa 3: configurar caixas de correio de usuário para dados de terceiros

A próxima etapa é configurar caixas de correio de usuário para oferecer suporte aos dados de terceiros. Conclua essas tarefas usando o Centro de administração do Exchange ou usando os cmdlets do Windows PowerShell correspondentes.
  
1. Habilitar a caixa de correio de arquivamento para cada usuário; consulte [Habilitar caixas de correio de arquivo morto no Office 365 Security &amp; Centro de conformidade](enable-archive-mailboxes.md) e [Habilitar o arquivamento ilimitado no Office 365](enable-unlimited-archiving.md).
    
2. Colocar caixas de correio do usuário em litígio ou aplicar uma política de retenção do Office 365; Consulte um dos seguintes tópicos: 
    
    - [Colocar uma caixa de correio em Retenção de litígio](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
    - [Visão geral das políticas de retenção no Office 365](retention-policies.md)
    
    Conforme mencionado anteriormente, quando você coloca as caixas de correio em retenção, é possível definir uma duração para a retenção dos itens da fonte de dados de terceiros, ou você pode optar por reter itens indefinidamente.

## <a name="step-4-provide-your-partner-with-information"></a>Etapa 4: fornecer informações ao seu parceiro

A etapa final é fornecer a seu parceiro as informações a seguir, para que ele possa configurar o conector a fim de se conectar à sua organização do Office 365 e importar dados para as caixas de correio do usuário e para a caixa de correio de dados de terceiros. 
  
- O ponto de extremidade usado para conectar ao serviço do Windows Azure no Office 365:

    ```
    https://office365ingestionsvc.gble1.protection.outlook.com/service/ThirdPartyIngestionService.svc
    ```

- Entrar no credenciais (ID de usuário do Office 365 e senha) da caixa de correio dados de terceiros que você criou na etapa 2. Essas credenciais são necessárias para que o conector de parceiro possa acessar e importar itens para caixas de correio do usuário e a caixa de correio de dados de terceiros.
    

  
## <a name="more-information"></a>Mais informações

- Anterior conforme explicado, itens de dados de terceiros fontes são importados para caixas de correio do Exchange como mensagens de email. O conector de parceiro importa o item usando um esquema necessário para a API do Office 365. A tabela a seguir descreve as propriedades de mensagem de um item de uma fonte de dados de terceiros depois que ela é importada para uma caixa de correio do Exchange como uma mensagem de email. A tabela também indica se a propriedade de mensagem é obrigatória. Propriedades obrigatórias devem ser preenchidas. Se um item estiver faltando uma propriedade obrigatória, ele não será importado para o Office 365. O processo de importação retornará uma mensagem de erro que explica por que um item não foi importado e qual propriedade está ausente.
    
    |**Propriedade da mensagem**|**Obrigatório?**|**Descrição**|**Valor de exemplo**|
    |:-----|:-----|:-----|:-----|
    |**DE ** <br/> |Sim  <br/> |O usuário que originalmente criada ou enviado o item na fonte de dados de terceiros. O conector de parceiro tentará mapear a ID de usuário do item fonte (por exemplo, uma alça Twitter) para uma conta de usuário do Office 365 para todos os participantes (usuários nos campos FROM e TO). Uma cópia da mensagem será importada para a caixa de correio de cada participante. Se nenhum dos participantes do item pode ser mapeado para uma conta de usuário do Office 365, o item será importado para a caixa de correio de arquivamento de terceiros no Office 365.<br/> <br/> O participante que é identificado como o remetente do item deve ter uma caixa de correio ativa em que o item que está sendo importado para a organização do Office 365. Se o remetente não tem uma caixa de correio ativa, o seguinte erro será retornado:<br/><br/>  `One or more messages in the Request failed to be delivered to either From or Sender email address. You will need to resend your entire Request. Error: The request failed. The remote server returned an error: (401) Unauthorized.`  | `bob@contoso.com` <br/> |
    |**PARA** <br/> |Sim  <br/> |O usuário que recebeu um item, caso seja aplicável a um item na fonte de dados.  <br/> | `bob@contoso.com` <br/> |
    |**ASSUNTO** <br/> |Não  <br/> |O assunto do item de origem.  <br/> | `"Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/> |
    |**DATA** <br/> |Sim  <br/> |A data na qual o item foi originalmente criado ou publicado na fonte de dados do cliente. Por exemplo, a data quando uma mensagem do Twitter foi enviada.  <br/> | `01 NOV 2015` <br/> |
    |**CORPO** <br/> |Não  <br/> |O conteúdo da mensagem ou postagem. Para algumas fontes de dados, o conteúdo desta propriedade pode ser o mesmo que o conteúdo para a propriedade **SUBJECT** . Durante o processo de importação, o conector de parceiro tenta manter com fidelidade total da fonte de conteúdo possível. Se possível arquivos, gráficos ou outros conteúdos do corpo do item de origem está incluído nesta propriedade. Caso contrário, o conteúdo do item fonte é incluído na propriedade **anexo** . O conteúdo dessa propriedade será dependem do conector de parceiro e a capacidade da plataforma do código-fonte.<br/> | `Author: bob@contoso.com` <br/>  `Date: 10 DEC 2014` <br/>  `Tweet: "Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/>  `Date: 01 NOV 2015` <br/> |
    |**ANEXO** <br/> |Não  <br/> |Se um item na fonte de dados (por exemplo, uma tweet no Twitter ou uma conversa de mensagem instantânea) tem um arquivo anexado ou incluir imagens, o parceiro conecte-se a primeira tentativa será incluir anexos na propriedade **BODY** . Se isso não é possível, então ela será adicionada ao * * anexo * * propriedade. Outros exemplos de anexos incluem Curtições no Facebook, metadados da fonte de conteúdo e as respostas a uma mensagem ou postagem.<br/> | `image.gif` <br/> |
    |**MESSAGECLASS** <br/> |Sim  <br/> | Esta é uma propriedade de valor múltiplos, que é criada e preenchida pelo conector de parceiro. O formato dessa propriedade é `IPM.NOTE.Source.Event`. (Esta propriedade deve começar com `IPM.NOTE`; esse formato é similar para o `IPM.NOTE.X` classe de mensagem.) Essa propriedade inclui as seguintes informações:<br/><br/>`Source`-Indica a fonte de dados de terceiros; Por exemplo, Twitter, Facebook ou BlackBerry.  <br/> <br/>  `Event`-Indica o tipo de atividade foi executada na fonte de dados de terceiros que produzidos os itens; Por exemplo, uma tweet no Twitter ou uma postagem em Facebook. Eventos são específicos para a fonte de dados.<br/> <br/>  Uma finalidade dessa propriedade é filtrar itens específicos com base na fonte de dados em que um item foi originada ou com base no tipo de evento. Por exemplo, em uma pesquisa de descoberta eletrônica, você pode criar uma consulta de pesquisa para localizar todas as tweets publicadas por um usuário específico.<br/> | `IPM.NOTE.Twitter.Tweet` <br/> |
   
- Quando os itens são importados com êxito a caixas de correio no Office 365, um identificador exclusivo é retornado de volta para o chamador como parte da resposta HTTP. Esse identificador — chamado `x-IngestionCorrelationID`— pode ser usado para fins de solução de problemas subsequentes por parceiros para o rastreamento de ponta a ponta de itens. É recomendável que os parceiros capturam essas informações e faça o logon adequadamente no seu lado. Aqui está um exemplo de uma resposta HTTP mostrando esse identificador:

    ```
    HTTP/1.1 200 OK
    Content-Type: text/xml; charset=utf-8
    Server: Microsoft-IIS/8.5
    x-IngestionCorrelationID: 1ec7667d-f097-47fe-a9a2-bc7ab0a7552b
    X-AspNet-Version: 4.0.30319
    X-Powered-By: ASP.NET
    Date: Tue, 02 Feb 2016 22:55:33 GMT 
    ```
 
- Você pode usar a ferramenta de pesquisa de conteúdo no Office 365 Security &amp; Centro de conformidade para procurar itens que tenham sido importados para caixas de correio no Office 365 de uma fonte de dados de terceiros. Para pesquisar especificamente para esses itens importados, você pode usar os seguintes pares de valor da propriedade de mensagem na caixa de palavra-chave para uma pesquisa de conteúdo. . 
    
  - **`kind:externaldata`**-Use este par de valor de propriedade para pesquisa todos os tipos de dados de terceiros. Por exemplo, para pesquisar itens que tenham sido importados de uma fonte de dados de terceiros e contêm a palavra "contoso" na propriedade assunto do item importado, você usaria a consulta de palavra-chave `kind:externaldata AND subject:contoso`.
    
  - **`itemclass:ipm.externaldata.<third-party data type>`**-Use este par de valor da propriedade à pesquisa somente um tipo de especificar de dados de terceiros. Por exemplo, para pesquisar somente dados de Facebook que contenham a palavra "contoso" na propriedade Subject, você usaria a consulta de palavra-chave `itemclass:ipm.externaldata.Facebook* AND subject:contoso`. 

  Para obter uma lista completa dos valores a serem usados para tipos de dados de terceiros para o `itemclass` propriedade, consulte [Use pesquisa de conteúdo para pesquisar dados de terceiros que foi importados para o Office 365](use-content-search-to-search-third-party-data-that-was-imported.md)
    
   Veja mais informações sobre como usar a Pesquisa de Conteúdo e criar consultas de pesquisa de palavra-chave em:
    
  - [Pesquisa de conteúdo no Office 365](content-search.md)
    
  - [Consultas de palavra-chave e condições de pesquisa para Pesquisa de Conteúdo](keyword-queries-and-search-conditions.md)
 

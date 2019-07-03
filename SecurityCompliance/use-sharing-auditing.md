---
title: Compartilhamento de auditoria para localizar recursos compartilhados com usuários externos
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- BCS160
- MET150
ms.assetid: 50bbf89f-7870-4c2a-ae14-42635e0cfc01
description: 'O compartilhamento é uma atividade importante no SharePoint Online e no OneDrive for Business. Agora, os administradores podem usar a auditoria de compartilhamento no log de auditoria do Office 365 para determinar como o compartilhamento está sendo usado em sua organização. '
ms.openlocfilehash: e2865d35e988d8c0e42a6c51f78507db8b170d4c
ms.sourcegitcommit: b262d40f6daf06be26e7586f37b736e09f8a4511
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/02/2019
ms.locfileid: "35435231"
---
# <a name="use-sharing-auditing-in-the-office-365-audit-log"></a>Compartilhamento de auditoria para localizar recursos compartilhados com usuários externos

O compartilhamento é uma atividade importante no SharePoint Online e no OneDrive for Business e é amplamente usado nas organizações do Office 365. Agora, os administradores podem usar a auditoria de compartilhamento no log de auditoria do Office 365 para determinar como o compartilhamento está sendo usado em sua organização. 
  
## <a name="the-sharepoint-sharing-schema"></a>O esquema de compartilhamento do SharePoint

Eventos de compartilhamento (exceto o compartilhamento de política e eventos de link de compartilhamento) são diferentes dos eventos relacionados a arquivos e pastas de uma maneira principal: um usuário está executando uma ação que tem algum efeito sobre outro usuário. Por exemplo, o usuário A fornece ao usuário B acesso a um arquivo. Neste exemplo, o usuário A é o *usuário* que está agindo e o usuário B é o *usuário de destino*. No esquema de arquivos do SharePoint, a ação do usuário que está agindo só afeta o próprio arquivo. Quando o usuário A abre um arquivo, as únicas informações necessárias no **** evento fileaccessed são o usuário que está agindo. Para resolver essa diferença, há um esquema separado, chamado esquema de *compartilhamento do SharePoint*, que captura mais informações sobre o compartilhamento de eventos. Isso garante que os administradores tenham mais informações sobre quem compartilhou um recurso e o usuário com o qual o recurso foi compartilhado. 
  
O esquema de compartilhamento fornece dois campos adicionais no log de auditoria relacionado aos eventos de compartilhamento: 
  
- **TargetUserOrGroupName** – armazena o UPN ou o nome do usuário ou grupo de destino com o qual um recurso foi compartilhado (usuário B no exemplo anterior). 
    
- **TargetUserOrGroupType** – identifica se o usuário ou grupo de destino é um membro, convidado, grupo ou parceiro. 
    
Esses dois campos, além de outras propriedades do esquema de log de auditoria do Office 365, como User, Operation e Date, podem informar a história completa sobre *qual* usuário compartilhou *o* recurso com *quem* e *quando*. 
  
Há outra propriedade de esquema que é importante para o texto de compartilhamento. A propriedade **EVENTDATA** armazena informações adicionais sobre o compartilhamento de eventos. Por exemplo, quando um usuário compartilha um site com outro usuário, isso é feito adicionando-se o usuário de destino a um grupo do SharePoint. A propriedade **EVENTDATA** captura essas informações adicionais para fornecer contexto para administradores. 

## <a name="the-sharepoint-sharing-model-and-sharing-events"></a>O modelo de compartilhamento do SharePoint e eventos de compartilhamento

O compartilhamento é definido por três eventos separados ****: sharingset, **SharingInvitationCreated**e **SharingInvitaitonAccepted**. Este é o fluxo de trabalho para como o compartilhamento de eventos é registrado no log de auditoria do Office 365. 
  
![Fluxograma de como o compartilhamento de auditoria funciona](media/d83dd40f-919b-484f-bfd6-5dc8de31bff6.png)
  
Quando um usuário (o usuário agindo) deseja compartilhar um recurso com outro usuário (o usuário de destino), o SharePoint (ou o OneDrive for Business) primeiro verifica se o endereço de email do usuário de destino já está associado a uma conta de usuário no diretório da organização. Se o usuário de destino estiver no diretório da organização, o SharePoint fará o seguinte:
  
-  Atribui imediatamente as permissões de usuário de destino para acessar o recurso. 
    
- Envia uma notificação de compartilhamento para o endereço de email do usuário de destino.
    
- Registra um **** evento sharingset. 
    
 Se uma conta de usuário para o usuário de destino não estiver no diretório da organização, o SharePoint fará o seguinte: 
  
- Cria um convite de compartilhamento e o envia para o endereço de email do usuário de destino.
    
- Registra um evento **SharingInvitationCreated** . 
    
    > [!NOTE]
    > O evento **SharingInvitationCreated** é sempre associado ao compartilhamento de convidados ou externo quando o usuário de destino não tem acesso ao recurso que foi compartilhado. 
  
Quando o usuário de destino aceita o convite de compartilhamento que é enviado a eles (clicando no link no convite), o SharePoint registra um evento **SharingInvitationAccepted** e atribui as permissões de usuário de destino para acessar o recurso. Informações adicionais sobre o usuário de destino também são registradas, como a identidade do usuário para o qual o convite foi enviado e o usuário que aceitou o convite. Em alguns casos, esses usuários (ou endereços de email) podem ser diferentes. 
  

  
## <a name="how-to-identify-resources-shared-with-external-users"></a>Como identificar recursos compartilhados com usuários externos

Um requisito comum para administradores é criar uma lista de todos os recursos que foram compartilhados com usuários fora da organização. Usando a auditoria de compartilhamento no Office 365, os administradores agora podem gerar essa lista. Veja como.
  
### <a name="step-1-search-for-sharing-events-and-export-the-results-to-a-csv-file"></a>Etapa 1: Pesquisar eventos de compartilhamento e exportar os resultados para um arquivo CSV

A primeira etapa é Pesquisar o log de auditoria do Office 365 para eventos de compartilhamento. Para obter mais informações (incluindo as permissões necessárias) sobre pesquisa no log de auditoria, consulte [Pesquisar o log de auditoria no centro de conformidade de & de segurança](search-the-audit-log-in-security-and-compliance.md).
  
1. Acesse [https://protection.office.com](https://protection.office.com).
    
2. Entre no Office 365 usando a sua conta corporativa ou de estudante.
    
3. No painel esquerdo do centro de conformidade & segurança, clique em ****  > **pesquisa de log de auditoria**de pesquisa.
    
    A página **pesquisa de log de auditoria** é exibida. 
    
4. Em **atividades**, clique em **compartilhar e acessar as atividades de solicitação** para pesquisar eventos relacionados ao compartilhamento. 
    
    ![Em atividades, selecione compartilhar e acessar atividades de solicitação](media/46bb25b7-1eb2-4adf-903a-cc9ab58639f9.png)
  
5.  Selecione um intervalo de data e hora para localizar os eventos de compartilhamento que ocorreram dentro desse período. 
    
6. Clique em **Pesquisar** para executar a pesquisa. 
    
7. Quando a pesquisa é concluída e os resultados são exibidos, clique em **Exportar resultados** \> **baixar todos os resultados**.
    
    Depois que você selecionar a opção Exportar, uma mensagem será exibida na parte inferior da janela que solicitará que você abra ou salve o arquivo CSV.
    
8. Clique em **salvar** \> **salvar como** e salve o arquivo CSV em uma pasta no computador local. 

### <a name="step-2-filter-the-csv-file-for-resources-shared-with-external-users"></a>Etapa 2: filtrar o arquivo CSV para recursos compartilhados com usuários externos

A próxima etapa é filtrar o CSV para os eventos **sharingset** e **SharingInvitationCreated** e exibir os eventos em que a propriedade **TargetUserOrGroupType** é **Guest**. Use a ferramenta Editor de consulta de alimentação no Excel para fazer isso. Para obter instruções detalhadas, consulte [Export, configure e View Audit Log Records](export-view-audit-log-records.md). 

Após seguir as instruções no tópico anterior para preparar o arquivo CSV, faça o seguinte:
    
1. Abra o arquivo CSV que você preparou com o editor de consulta de energia. 

2. Na guia **página inicial** , clique em **classificar & filtro**e, em seguida, clique em **Filtrar**.
    
3. Na lista suspensa **classificar & filtro** na coluna **operações** , desmarque todas as seleções e, em seguida, selecione **compartilhamento** e **SharingInvitationCreated**e clique em **OK**.
    
    O Excel exibe as linhas dos **** eventos sharingset e **SharingInvitationCreated** . 
    
4. Vá até a coluna chamada **TargetUserOrGroupType** e selecione-a. 
    
5. Na lista suspensa **classificar & filtro** , desmarque todas as seleções e, em seguida, selecione **TargetUserOrGroupType: convidado**e clique em **OK**.
    
    Agora o Excel exibe as linhas dos eventos **SharingInvitationCreated** e **sharingset** e onde o usuário de destino está fora da sua organização, pois os usuários externos são identificados pelo valor **TargetUserOrGroupType: Guest**. 
    
A tabela a seguir mostra todos os usuários da organização que compartilharam recursos com um usuário convidado em um intervalo de datas especificado.
  
![Compartilhando eventos no log de auditoria do Office 365](media/0e0ecbe3-c794-4ca6-a2ca-63478fb3bb34.png)
  
Embora não esteja incluído na tabela anterior, a propriedade **ObjectID** identifica o recurso que foi compartilhado com o usuário de destino; por exemplo `ObjectId:https:\/\/contoso-my.sharepoint.com\/personal\/sarad_contoso_com\/Documents\/Southwater Proposal.docx`.
  
> [!TIP]
> Se você deseja identificar quando um usuário convidado foi realmente atribuído a permissões para acessar um recurso (em vez de apenas os recursos que foram compartilhados com eles), repita as etapas 2, 3 e 4 e filtre o **SharingInvitationAccepted** e o **sharingset** eventos na etapa 5. 

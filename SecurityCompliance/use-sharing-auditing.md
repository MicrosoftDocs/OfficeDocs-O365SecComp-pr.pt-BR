---
title: Usar o compartilhamento auditorias no log de auditoria do Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 2/13/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- BCS160
- MET150
ms.assetid: 50bbf89f-7870-4c2a-ae14-42635e0cfc01
description: 'O compartilhamento é uma atividade fundamental no SharePoint Online e o OneDrive for Business. Os administradores agora podem usar compartilhamento auditorias no log de auditoria do Office 365 para determinar como compartilhamento está sendo usado em suas organizações. '
ms.openlocfilehash: 511f8b0e61d450659d78177d5b87fac9ee636cd4
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524165"
---
# <a name="use-sharing-auditing-in-the-office-365-audit-log"></a>Usar o compartilhamento auditorias no log de auditoria do Office 365

Compartilhamento é uma atividade fundamental no SharePoint Online e o OneDrive for Business e é amplamente usado nas organizações do Office 365. Os administradores agora podem usar compartilhamento auditorias no log de auditoria do Office 365 para determinar como compartilhamento está sendo usado em suas organizações. 
  
## <a name="the-sharepoint-sharing-schema"></a>O esquema de compartilhamento do SharePoint

Eventos de compartilhamento (excluindo compartilhamento de política e vincular eventos) são diferentes dos eventos relacionados a pasta e arquivo de uma maneira primária: um usuário está sendo uma ação que tem efeito algum outro usuário. Por exemplo, o usuário fornece acesso de usuário B para um arquivo. Neste exemplo, o usuário A é a *atuação de usuário* e o usuário B é o *usuário de destino*. No esquema de arquivo do SharePoint, a ação do usuário atuando afeta somente o arquivo em si. Quando o usuário A abre um arquivo, a única informação necessária para o evento **FileAccessed** é o usuário atuando. Para resolver essa diferença, não há um esquema separado, chamado o *esquema de compartilhamento do SharePoint*, que captura mais informações sobre compartilhamento de eventos. Isso garante que os administradores têm mais percepção que compartilhou um recurso e o recurso de usuário foi compartilhado com. 
  
O esquema de compartilhamento fornece dois campos adicionais no log de auditoria relacionados ao compartilhamento de eventos: 
  
- **TargetUserOrGroupName** - armazena o UPN ou o nome do usuário de destino ou grupo que um recurso foi compartilhado com (usuário B no exemplo anterior). 
    
- **TargetUserOrGroupType** - identifica se o usuário de destino ou grupo é um membro, convidado, grupo ou parceiro. 
    
Esses dois campos, além de outras propriedades do Office 365 o esquema de log de auditoria como usuário, operação e data podem dizer a história completa sobre *quais* usuários shared *quais* recursos com *quem* e *quando*. 
  
Não há outra propriedade de esquema que são importante para a história de compartilhamento. A propriedade **EventData** armazena informações adicionais sobre o compartilhamento de eventos. Por exemplo, quando um usuário compartilhar um site com outro usuário, isso é realizado por meio da adição de usuário de destino para um grupo do SharePoint. A propriedade **EventData** captura essas informações adicionais para fornecer um contexto para administradores. 

## <a name="the-sharepoint-sharing-model-and-sharing-events"></a>O modelo de compartilhamento e de eventos do SharePoint

Compartilhamento é definido por três eventos separados: **SharingSet**, **SharingInvitationCreated**e **SharingInvitaitonAccepted**. Aqui está o fluxo de trabalho para compartilhamento como eventos são registrados no log de auditoria do Office 365. 
  
![Fluxograma de como funciona a auditoria de compartilhamento](media/d83dd40f-919b-484f-bfd6-5dc8de31bff6.png)
  
Quando um usuário (o usuário atuando) quiser compartilhar um recurso com outro usuário (o usuário de destino), SharePoint (ou OneDrive for Business) primeiro verifica se o endereço de email do usuário de destino já está associado uma conta de usuário no diretório da organização. Se o usuário de destino está no diretório da organização, o SharePoint faz o seguinte:
  
-  Atribui imediatamente as permissões de usuário de destino para acessar o recurso. 
    
- Envia uma notificação de compartilhamento para o endereço de email do usuário de destino.
    
- Registra um evento **SharingSet** . 
    
 Se uma conta de usuário para o usuário de destino não estiver no diretório da organização, o SharePoint faz o seguinte: 
  
- Cria um convite de compartilhamento e envia para o endereço de email do usuário de destino.
    
- Registra um evento **SharingInvitationCreated** . 
    
    > [!NOTE]
    > O evento **SharingInvitationCreated** mais sempre é associado externo ou convidado de compartilhamento quando o usuário de destino não tem acesso ao recurso que foi compartilhado. 
  
Quando o usuário de destino aceita o convite de compartilhamento que enviou a eles (clicando no link do convite), SharePoint registra um evento **SharingInvitationAccepted** e atribui as permissões de usuário de destino para acessar o recurso. Informações adicionais sobre o usuário de destino também são registradas, como a identidade do usuário que você recebeu o convite e o usuário que realmente aceitou o convite. Em alguns casos, esses usuários (ou endereços de email) podem ser diferentes. 
  

  
## <a name="how-to-identify-resources-shared-with-external-users"></a>Como identificar os recursos compartilhados com usuários externos

Um requisito comum para administradores está criando uma lista de todos os recursos que foram compartilhados com usuários fora da organização. Usando o compartilhamento auditorias no Office 365, os administradores agora podem gerar nessa lista. Aqui está como.
  
### <a name="step-1-search-for-sharing-events-and-export-the-results-to-a-csv-file"></a>Etapa 1: Pesquisar eventos de compartilhamento e exportar os resultados para um arquivo CSV

A primeira etapa é pesquisar o log de auditoria do Office 365 para o compartilhamento de eventos. Para obter mais detalhes (incluindo as permissões necessárias) sobre como pesquisar no log de auditoria, consulte [Pesquisar o log de auditoria de segurança do Office 365 &amp; Centro de conformidade](search-the-audit-log-in-security-and-compliance.md).
  
1. Vá para [https://protection.office.com](https://protection.office.com).
    
2. Entrar no Office 365 usando sua conta do trabalho ou da escola.
    
3. No painel à esquerda da segurança &amp; Centro de conformidade, clique em **pesquisa &amp; investigação**e clique em **pesquisa de log de auditoria**.
    
    A página de **pesquisa de log de auditoria** é exibida. 
    
4. Em **atividades**, clique em **atividades de compartilhamento** para pesquisar somente para compartilhamento de eventos. 
    
    ![Em atividades, selecione atividades de compartilhamento](media/46bb25b7-1eb2-4adf-903a-cc9ab58639f9.png)
  
5.  Selecione um intervalo de data e hora para encontrar os eventos de compartilhamento que ocorreram nesse período. 
    
6. Clique em **pesquisa** para executar a pesquisa. 
    
7. Quando terminar a pesquisa em execução e os resultados são exibidos, clique em **exportar os resultados da** \> **Baixe todos os resultados**.
    
    Depois de selecionar a opção Exportar, uma mensagem é exibida na parte inferior da janela solicitando que você abrir ou salvar o arquivo CSV.
    
8. Clique em **Salvar** \> **Salvar como** e salve o arquivo CSV para uma pasta no computador local. 
    

  
### <a name="step-2-filter-the-csv-file-for-resources-shared-with-external-users"></a>Etapa 2: Filtrar o arquivo CSV para recursos compartilhados com usuários externos

A próxima etapa é para filtrar o CSV para os eventos **SharingSet** e **SharingInvitationCreated** e para exibir os eventos cuja propriedade **TargetUserOrGroupType** for **Convidado**. Você usará o recurso de consulta de energia no Excel para fazer isso. O procedimento a seguir é executado no Excel 2016. 
  
1. No Excel 2016, abra uma pasta de trabalho em branco.
    
2. Clique na guia **Dados**. 
    
3. Clique em **Nova consulta** \> **de arquivo** \> **De CSV**.
    
    ![Na guia dados, selecione nova consulta, selecione o arquivo e selecione de CSV](media/5170ab34-b449-40ea-bd3f-f1432c1c5973.png)
  
4. Abra o arquivo CSV que você baixou na etapa 1.
    
    O arquivo CSV é aberto no Editor de consulta. Observe que não existem quatro colunas: **tempo**, **usuário**, **ação**e **detalhes**. A coluna de **detalhes** é um campo de propriedade múltiplos. A próxima etapa é criar uma nova coluna para cada uma das propriedades na coluna **detalhes** . 
    
5. Selecione a coluna de **detalhes** e, em seguida, na guia **página inicial** , clique em **Coluna dividida** \> **Pelo delimitador**.
    
    ![Na guia página inicial, clique em coluna dividida e, em seguida, clique em por delimitador](media/aeb503e8-565b-42ea-91e2-9f127a74c00c.png)
  
6. Na janela de **Coluna dividida por delimitador** , faça o seguinte: 
    
      - Em **Selecionar ou digitar delimitador**, selecione **por vírgulas**.
    
      - Em **divisão**, selecione **em cada ocorrência do delimitador**.
    
7. Clique em **OK**.
    
    A coluna de **detalhes** é dividida em várias colunas. Cada nova coluna é nomeada **Detail.1**, **Detail.2**, **Detail.3**e assim por diante. Você perceberá que os valores em cada célula nas colunas **Detail.n** são prefixados com o nome da propriedade; Por exemplo, **Operação: SharingSet**, **Operação: SharingInvitationAccepted**e **Operação: SharingInvitationCreated**.
    
    ![A coluna de detalhes é dividida em várias colunas, um para cada propriedade](media/4b104ead-0313-4bd4-b2a9-f143ccb378ac.png)
  
8. Na guia **arquivo** , clique em **Fechar &amp; carga** feche o Editor de consulta e abra o arquivo em uma pasta de trabalho do Excel. 
    
    A próxima etapa é filtrar o arquivo para exibir somente os eventos **SharingSet** e **SharingInvitationCreated** . 
    
9. Vá para a guia **página inicial** e selecione a coluna **ação** . 
    
10. No **Classificar &amp; filtro** lista suspensa, limpar todas as seleções, em seguida, selecione **SharingSet** e **SharingInvitationCreated**e clique em **Okey**.
    
    Excel exibe as linhas para os eventos **SharingSet** e **SharingInvitationCreated** . 
    
11. Vá para a coluna nomeada **Detail.17** (ou que julgar coluna contém a propriedade **TargetUserOrGroupType** ) e selecioná-la. 
    
12. No **Classificar &amp; filtro** lista suspensa, limpar todas as seleções, em seguida, selecione **TargetUserOrGroupType:Guest**e clique **Okey**.
    
    Agora Excel exibe as linhas para eventos **SharingInvitationCreated** e **SharingSet** e onde o usuário de destino está fora da sua organização, pois os usuários externos são identificados pelo valor **TargetUserOrGroupType:Guest**. 
    
A tabela a seguir mostra todos os usuários da organização que recursos compartilhados com um usuário convidado dentro de um intervalo de datas especificado.
  
![Log de auditoria de eventos de compartilhamento no Office 365](media/0e0ecbe3-c794-4ca6-a2ca-63478fb3bb34.png)
  
Embora ele não está incluído na tabela anterior, a coluna **Detail.10** (ou que julgar coluna contém a propriedade **ObjectId** ) identifica o recurso que foi compartilhado com o usuário de destino; Por exemplo `ObjectId:https:\/\/contoso-my.sharepoint.com\/personal\/sarad_contoso_com\/Documents\/Southwater Proposal.docx`.
  
> [!TIP]
> Se você quiser identificar quando um usuário convidado foi realmente atribuído permissões para acessar um recurso (e não apenas os recursos que where compartilhados com eles), repita as etapas 10, 11 e 12 e filtrar os **SharingInvitationAccepted** e **SharingSet **eventos na etapa 10. 

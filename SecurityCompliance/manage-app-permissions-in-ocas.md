---
title: Gerenciar permissões de aplicativo usando o Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/22/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2062c312-b1e4-4ce7-8cb2-ea39bc0dfdad
description: Permissões do aplicativo na segurança de aplicativo de nuvem do Office 365 ajudarão-lo a gerenciar os aplicativos que seus usuários baixem para uso com dados do Office 365
ms.openlocfilehash: 7bda35bbbf3a16cd1d386adcb03b1c7c4176913a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524446"
---
# <a name="manage-app-permissions-using-office-365-cloud-app-security"></a>Gerenciar permissões de aplicativo usando o Office 365 Cloud App Security

Gerenciamento de segurança avançada do Office 365 agora é segurança de aplicativo de nuvem do Office 365.
  
|Avaliação * *\>**|Planejamento * *\>**|Implantação * *\>**|Utilização * * *|
|:-----|:-----|:-----|:-----|
|[Comece a avaliar](office-365-cas-overview.md) <br/> |[Começar a planejar](get-ready-for-office-365-cas.md) <br/> |[Começar a implantar](turn-on-office-365-cas.md) <br/> |Você está aqui!  <br/> [Próximas etapas](manage-app-permissions-in-ocas.md#nextsteps) <br/> |
   
Pessoas amor apps e eles baixá-las com frequência, especialmente os aplicativos que as pessoas utilizam pense salvará tempo, facilitando a obter no trabalho ou escola informações. No entanto, alguns aplicativos potencialmente poderia ser um risco de segurança para sua organização, dependendo de quais informações eles acessarem e como eles lidam com essas informações. Com a [Segurança de aplicativo de nuvem do Office 365](office-365-cas-overview.md), se você for um administrador global ou de segurança, você pode gerenciar permissões do aplicativo para sua organização. Você pode ver as pessoas de aplicativos estão usando com dados do Office 365, que permissões estes aplicativos tem e muito mais. 
  
Este artigo descreve como criar uma consulta de aplicativo, como aprovar ou proibir um aplicativo e aonde ir para gerenciar permissões de aplicativo.
  
## <a name="how-to-find-the-manage-app-permissions-page"></a>Como encontrar a página Gerenciar aplicativo permissões
<a name="findappperms"> </a>

> [!NOTE]
> Permissões de aplicativo são gerenciadas no portal de segurança de aplicativo de nuvem do Office 365. Você deve ser um administrador global ou administrador de segurança para executar a tarefa a seguir. Para saber mais, consulte [permissões no Office 365 Security &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md). 
  
1. Vá para [https://protection.office.com](https://protection.office.com) e entrar usando sua conta de trabalho ou da escola para o Office 365. (Isso leva você para a segurança &amp; Centro de conformidade.) 
    
2. Vá para **alertas** \> **avançadas de gerenciar alertas**.
    
3. Clique (ou toque) **vá para segurança de aplicativo de nuvem do Office 365**.
    
    ![Na segurança &amp; Centro de conformidade, escolha gerenciar alertas avançadas para ir à segurança de aplicativo de nuvem do Office 365](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)
  
    > [!NOTE]
    > Se a segurança de aplicativo de nuvem do Office 365 não está ativada ainda, você pode fazer isso nesta página. Consulte [Prepare-se para a segurança de aplicativo de nuvem do Office 365](get-ready-for-office-365-cas.md). 
  
4. Escolha **investigar** \> **permissões do aplicativo**.
    
    ![No portal do O365 CAS, escolha investigar.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)
  
## <a name="what-youll-see-on-the-manage-app-permissions-page"></a>O que você verá na página Gerenciar aplicativo permissões
<a name="whatsonpage"> </a>

A tabela a seguir descreve os controles e opções disponíveis na página Gerenciar aplicativo permissões.
  
|**Item**|**Descrição**|
|:-----|:-----|
|Ícone básica na barra de aplicativos de consulta  <br/> ![Ícone que indica o modo de exibição de consulta básica para consultar as permissões do aplicativo](media/a459bc51-e86b-43d5-a0ee-661b9fb4afc9.png)|Selecione essa opção para alternar para o modo de exibição avançado.  <br/> (Se você vir **básica**, você está usando o modo de exibição avançado)  <br/> |
|Ícone Avançado na barra de aplicativos de consulta  <br/> ![Ícone que indica avançadas do modo de exibição de consulta para consultar as permissões do aplicativo](media/9958d832-2c81-45ed-a642-d926310ba6b6.png)|Selecione essa opção para alternar para modo de exibição básico.  <br/> (Se você vir **Avançado**, você está usando o modo de exibição básico.)  <br/> |
|Abrir ou fechar o ícone de todos os detalhes na lista de aplicativos  <br/> ![Clique nesse ícone para abrir ou fechar todos os detalhes para todos os aplicativos](media/018fa996-10e8-48ff-986e-55f2b69a5753.png)|Selecione esse ícone para exibir mais ou menos detalhes sobre cada aplicativo.  <br/> |
|Ícone de exportar na lista de aplicativos  <br/> ![Clique nesse ícone para exportar um arquivo csv de todos os aplicativos](media/98446851-fd96-4d09-9bb0-831db33090c1.png)|Selecione esse ícone para exportar um arquivo CSV que contém uma lista de aplicativos, o número de usuários para cada aplicativo, permissões associadas com o aplicativo, o nível de permissões, estado do aplicativo e usar nível de comunidade.  <br/> |
|Nome  <br/> |Usar esse recurso para ver o nome de um App. Selecione o nome para exibir mais informações, como seu descrição, o publisher, o site da Web app e o ID do aplicativo.  <br/> |
|Autorizado pelo  <br/> |Use esta opção para ver quantos usuários tenham autorizados a um aplicativo para acessar sua conta do Office 365. Selecione o número para exibir mais informações, como uma lista de contas de usuário.  <br/> |
|Nível de permissões  <br/> ![Ícone que indica o nível de permisiions para um aplicativo](media/aaebdd29-35b6-4c62-aef1-7c7817bd803d.png)|Use esta opção para ver quanto acesso um aplicativo tem aos dados do Office 365. Níveis de permissões indicam **baixa**, **média**ou **alta**, onde **baixa** pode indicar que o aplicativo acessa somente perfil e o nome de um usuário. Selecione o nível para exibir mais informações, como permissões concedidas para o aplicativo, o uso da comunidade e atividade relacionada no [log de governança](suspend-or-restore-an-account-in-ocas.md).<br/> |
|Estado do aplicativo ( **Banned**, **aprovado**ou **Undetermined**)  <br/> ![Ícones de permissões do aplicativo depois sendo permitidos, bloqueados ou nenhuma ação foi executada por um administrador](media/5748bd02-cd59-4bd1-a36f-d25a186e8055.png)|Use esta opção para marcar um aplicativo como aprovado ou Banned ou deixá-lo como indeterminado.  <br/> |
   
## <a name="mark-an-app-as-approved"></a>Marcar um aplicativo como aprovados
<a name="approveapp"> </a>

Na página **Gerenciar permissões de aplicativo** , localize o aplicativo que você deseja aprovar e escolha o ícone **app marca como aprovado** . 
  
![Escolha o aplicativo de marca como ícone aprovado](media/dd1b7690-441a-48c9-9c3a-58466513c63d.png)
  
O ícone fica verde, e o aplicativo em particular for aprovado para todos os usuários do Office 365.
  
> [!NOTE]
> Quando você marca um aplicativo como aprovados, não há nenhum efeito sobre o usuário final. Marcação visualmente os aplicativos que foram aprovados ajuda a separá-los dos aplicativos que ainda não foram revisados ainda. 
  
## <a name="ban-an-app"></a>Proibir um aplicativo
<a name="banapp"> </a>

1. Na página **Gerenciar permissões de aplicativo** , localize o aplicativo que você deseja proibir e escolha o ícone **app marca como proibidos** . 
    
    ![Escolha o aplicativo de marca como ícone proibido](media/b9b1c5f6-fde7-46d5-8589-1564d05702b3.png)
  
2. Escolha se deseja que os usuários saibam o que foi proibido seu aplicativo.
    
    (Recomendado) Para permitir que os usuários saibam, selecione **usuários Notify que recebem acesso para este aplicativo proibido**e adicione ou edite uma mensagem de notificação personalizada.
    
    Para não permitir que os usuários saibam, desmarque **usuários Notify que recebem acesso para este aplicativo proibido**.
    
    ![O modelo de email para um aplicativo proibido](media/6d132700-5f7f-472c-bfb5-a44549e69c16.jpg)
  
3. Escolha **aplicativo proibir**.
    
## <a name="create-an-app-query"></a>Criar uma consulta de aplicativo
<a name="createapp"> </a>

1. Na barra de consulta do aplicativo, se você vir **Avançado**, clique (ou toque)-lo para ir para o modo de exibição avançado. (Se você vir Basic, você estiver usando o modo de exibição avançado; manter sua opinião como está.)
    
2. Use a lista **Selecionar um filtro** para escolher uma opção. A tabela a seguir resume as opções de filtro disponíveis. 
    
|**Utilize esse filtro**|**Para exibir**|
|:-----|:-----|
|**Aplicativo** <br/> |Aplicativos com determinados nomes  <br/> |
|**Estado do aplicativo** <br/> |Aplicativos com base em seu estado (aprovado, Banned ou Undetermined)  <br/> |
|**Uso da comunidade** <br/> |Aplicativos com base na comunidade usam níveis (Rare, Uncommon ou comum)  <br/> |
|**Nível de permissão** <br/> |Aplicativos com base em determinados níveis de permissão  <br/> |
|**Permissões** <br/> |Aplicativos que necessitam de determinadas permissões  <br/> |
|**Publicador** <br/> |Aplicativos de determinados fornecedores  <br/> |
|**Usuário** <br/> |Aplicativos que um determinado usuário autorizado  <br/> |
   
3. Selecione **é igual a** ou **diferente**e, em seguida, especifique um valor para o filtro.
    
4. Para adicionar mais filtros, selecione o (sinal de adição![Adicionar um ícone de filtro para consultar aplicativos](media/771b2958-67cd-4e14-9302-283ef238cae5.jpg)) e repita as etapas 2 e 3.
    
5. Para remover um filtro, selecione o x (![Remover um ícone de filtro para consultar aplicativos](media/5339277f-555d-4749-8dcc-d2574250556e.jpg)) ao lado do nome de um filtro.
    
Os filtros são aplicados automaticamente e a lista de aplicativos é atualizada de acordo.
  
## <a name="next-steps"></a>Próximas etapas
<a name="nextsteps"> </a>

- [Revise e agir em alertas](review-office-365-cas-alerts.md)
    
- Revise seus [logs de tráfego da Web e fontes de dados para segurança de aplicativo de nuvem do Office 365](web-traffic-logs-and-data-sources-for-ocas.md)
    
- Revise suas [atividades de utilização para segurança de aplicativo de nuvem do Office 365](utilization-activities-for-ocas.md)
    


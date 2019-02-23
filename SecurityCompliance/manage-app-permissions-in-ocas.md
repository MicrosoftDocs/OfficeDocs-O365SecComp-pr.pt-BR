---
title: Gerenciar aplicativos do OAuth usando o Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 12/26/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2062c312-b1e4-4ce7-8cb2-ea39bc0dfdad
description: Aplicativos OAuth no Office 365 Cloud app Security o ajudam a gerenciar os aplicativos que seus usuários baixam para uso com os dados do Office 365
ms.openlocfilehash: 510cb64f2267c99b783f86a69f7b7a84db8d84dd
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219821"
---
# <a name="manage-oauth-apps-using-office-365-cloud-app-security"></a>Gerenciar aplicativos do OAuth usando o Office 365 Cloud App Security

|Avaliação * *\>**|Planejamento * *\>**|Implantação * *\>**|Utilização * * *|
|:-----|:-----|:-----|:-----|
|[Iniciar avaliação](office-365-cas-overview.md) <br/> |[Iniciar planejamento](get-ready-for-office-365-cas.md) <br/> |[Iniciar implantação](turn-on-office-365-cas.md) <br/> |Você está aqui!  <br/> [Próximas etapas](manage-app-permissions-in-ocas.md#nextsteps) <br/> |
   
As pessoas adoram os aplicativos e os baixam com frequência, especialmente os aplicativos que as pessoas acham poupar tempo, facilitando a obtenção de suas informações de trabalho ou escola. No enTanto, alguns aplicativos podem ser um risco de segurança para sua organização, dependendo de quais informações eles acessam e como eles lidam com essas informações. Com o [Office 365 Cloud app Security](office-365-cas-overview.md), se você for um administrador de segurança ou global, você pode gerenciar aplicativos OAuth para sua organização. Você pode ver os aplicativos que as pessoas estão usando com dados do Office 365, quais permissões esses aplicativos têm e mais. 
  
Este artigo descreve onde ir para gerenciar aplicativos OAuth, como aprovar, proibir ou relatar um aplicativo e como criar uma consulta de aplicativo.
  
## <a name="how-to-find-the-manage-oauth-apps-page"></a>Como localizar a página Gerenciar aplicativos OAuth

> [!NOTE]
> Os aplicativos OAuth são gerenciados no portal do Office 365 Cloud app Security. Você deve ser um administrador global ou administrador de segurança para executar a tarefa a seguir. Para saber mais, confira [permissões no centro de &amp; conformidade de segurança do Office 365](permissions-in-the-security-and-compliance-center.md). 
  
1. Vá para o portal do Cloud app Security[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)() e entre.
  
2. Escolha **investigar** \> **aplicativos OAuth**.<br/>![No portal do O365 CAS, escolha investigar.](media/OCAS-OAuthApps.png)<br/>
  
## <a name="what-youll-see-on-the-manage-oauth-apps-page"></a>O que você verá na página Gerenciar aplicativos OAuth

A tabela a seguir descreve os controles e opções disponíveis na página Gerenciar aplicativos OAuth.
  
|**Item**|**Descrição**|
|:-----|:-----|
|Ícone básico na barra de consulta do aplicativo  <br/> ![Ícone que indica o modo de exibição de consulta básica para consulta](media/a459bc51-e86b-43d5-a0ee-661b9fb4afc9.png)|Selecione esta opção para mudar para o modo de exibição avançado.  <br/> (Se você vir **básico**, você está usando o modo de exibição avançado)  <br/> |
|Ícone avançado na barra de consulta do aplicativo  <br/> ![Ícone que indica o modo de exibição de consulta avançado para consulta](media/9958d832-2c81-45ed-a642-d926310ba6b6.png)|Selecione esta opção para alternar para o modo de exibição básico.  <br/> (Se você vir **avançado**, você está usando o modo de exibição básico.)  <br/> |
|Abrir ou fechar todos os ícones de detalhes na lista de aplicativos  <br/> ![Clique neste ícone para abrir ou fechar todos os detalhes de todos os aplicativos](media/018fa996-10e8-48ff-986e-55f2b69a5753.png)|Selecione este ícone para exibir mais ou menos detalhes sobre cada aplicativo.  <br/> |
|Ícone exportar na lista de aplicativos  <br/> ![Clique neste ícone para exportar um arquivo CSV de todos os aplicativos](media/98446851-fd96-4d09-9bb0-831db33090c1.png)|Selecione este ícone para exportar um arquivo CSV que contém uma lista de aplicativos, número de usuários para cada aplicativo, permissões associadas ao aplicativo, nível de permissões, estado do aplicativo e nível de uso da Comunidade.  <br/> |
|Nome  <br/> |Use este para ver o nome de um aplicativo. Selecione o nome para exibir mais informações, como descrição, editor, site de aplicativo e ID de aplicativo.  <br/> |
|Autorizado por  <br/> |Use esta para ver quantos usuários autorizaram um aplicativo a acessar sua conta do Office 365. Selecione o número para exibir mais informações, como uma lista de contas de usuário.  <br/> |
|Nível de permissões  <br/> ![Ícone que indica o nível de permisiions para um aplicativo](media/aaebdd29-35b6-4c62-aef1-7c7817bd803d.png)|Use isso para ver quanto acesso um aplicativo tem aos dados do Office 365. Os níveis de permissão indicam **baixo**, **médio**ou **alto**, onde **baixo** pode indicar que o aplicativo acessa apenas o perfil e o nome do usuário. Selecione o nível para exibir mais informações, como permissões concedidas ao aplicativo, uso da Comunidade e atividade relacionada no log de [governança](suspend-or-restore-an-account-in-ocas.md).<br/> |
|Último autorizado <br/> |Use isso para ver a data e a hora em que um aplicativo OAuth foi autorizado pela última vez a acessar os dados do Office 365 da sua organização. <br/>  |
|Ações<br/>![Aplicativos OAuth](media/OCAS-OAuthAppApproveBanReport.png)<br/> |Use esta caixa para ver ou marcar um aplicativo como aprovado ou proibido, relatar um aplicativo OAuth para a Microsoft ou deixá-lo como indeterminado.  <br/> |
   
## <a name="mark-an-app-as-approved"></a>Marcar um aplicativo como aprovado

Na página **gerenciar aplicativos OAuth** , localize o aplicativo que você deseja aprovar e escolha o ícone **Marcar aplicativo como aprovado** . 
  
![Escolha o ícone marcar aplicativo como aprovado](media/OCAS-MarkOAuthApproved.png)
  
O ícone fica verde e o aplicativo é aprovado para todos os seus usuários do Office 365.
  
> [!NOTE]
> Quando você marca um aplicativo como aprovado, não há efeito no usuário final. Marcar visualmente os aplicativos que são aprovados ajuda a separá-los de aplicativos que ainda não foram revisados. 
  
## <a name="ban-an-app"></a>Proibir um aplicativo

1. Na página **gerenciar aplicativos OAuth** , localize o aplicativo que você deseja proibir e escolha o ícone **Marcar aplicativo como proibido** .<br/>![Escolha o ícone marcar aplicativo como proibido](media/OCAS-MarkOAuthBanned.png)
  
2. Na caixa mensagem de notificação, mantenha o texto existente como está ou personalize o texto. Escolha se deseja permitir que os usuários saibam que seu aplicativo foi banido. <br/>![O modelo de email para um aplicativo proibido](media/6d132700-5f7f-472c-bfb5-a44549e69c16.jpg)<br/>
  
3. Escolha **proibir aplicativo**.

## <a name="report-an-oauth-app-to-microsoft"></a>Relatar um aplicativo OAuth para a Microsoft

Se você deseja enviar um aplicativo OAuth para a Microsoft para análise, é possível relatar esse aplicativo.

1. Na página **gerenciar aplicativos OAuth** , localize o aplicativo que você deseja enviar para análise.

2. Escolha as reticências verticais e, em seguida, escolha **relatar aplicativo..**..<br/>![Relatar um aplicativo OAuth](media/OCAS-MarkOAuthReported.png)<br/>

3. Na caixa de diálogo **relatar este aplicativo** , use a lista suspensa para indicar sua preocupação. Por padrão, **este aplicativo é mal-intencionado** selecionado. No enTanto, você pode escolher uma das outras opções disponíveis.<br/>![Relatar um aplicativo OAuth](media/OCAS-ReportOAuthApp.png)<br/>

4. Recomenda Mantenha a opção de contato selecionado e confirme (ou edite) o endereço de email listado.

5. Escolha **Enviar**. 
    
## <a name="create-an-app-query"></a>Criar uma consulta de aplicativo

Recomendamos usar o modo de exibição avançado, que tem a seguinte aparência: 

![Modo de exibição avançado](media/OCAS-OAuthAppsAdvQueryView.png)

Na barra de consulta do aplicativo, se você vir **avançado**, você está usando o modo de exibição básico. Clique (ou toque) em **avançado** para ir para o modo de exibição avançado. 

![Exibição básica](media/OCAS-OAuthAppsBasicQueryView.png)
    
1. Na barra de consulta, use a lista **selecionar um filtro** para escolher uma opção. 
    - **Aplicativo** Aplicativos com determinados nomes
    - **Estado do aplicativo** Aplicativos com base em seu estado (aprovado, proibido ou indeterminado)
    - **Uso da Comunidade** Aplicativos baseados em níveis de uso da Comunidade (raro, incomum ou comum)
    - **Nível de permissão** Aplicativos com base em determinados níveis de permissão 
    - **Permissões** Aplicativos que exigem determinadas permissões
    - **Publisher**  Aplicativos de determinados editores
    - **Usuário** Aplicativos que um determinado usuário autorizou
   
2. Selecione **igual a** ou **diferente**de e especifique um valor para o filtro.
    
3. Para adicionar mais filtros, selecione o sinal de adição (![Adicionar um ícone de filtro para consultar aplicativos](media/771b2958-67cd-4e14-9302-283ef238cae5.jpg)) e repita as etapas 2 e 3.
    
4. Para remover um filtro, selecione o x (![Remover um ícone de filtro para consultar aplicativos](media/5339277f-555d-4749-8dcc-d2574250556e.jpg)) ao lado de um nome de filtro.
    
Os filtros são aplicados automaticamente e a lista de aplicativos é atualizada de acordo.
  
## <a name="next-steps"></a>Próximas etapas

- [ReVisar e executar ação em alertas](review-office-365-cas-alerts.md)
    
- Examinar seus [logs de tráfego da Web e fontes de dados para o Office 365 Cloud app Security](web-traffic-logs-and-data-sources-for-ocas.md)
    
- ReVisar suas [atividades de utilização do Office 365 Cloud app Security](utilization-activities-for-ocas.md)
    


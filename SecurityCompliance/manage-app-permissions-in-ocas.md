---
title: Gerenciar aplicativos do OAuth usando o Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 12/26/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2062c312-b1e4-4ce7-8cb2-ea39bc0dfdad
description: Aplicativos de OAuth na segurança de aplicativo de nuvem do Office 365 ajudarão-lo a gerenciar os aplicativos que seus usuários baixem para uso com dados do Office 365
ms.openlocfilehash: ae32e3c6b15f4ad4794a3dd08c3992adaeba655c
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29603682"
---
# <a name="manage-oauth-apps-using-office-365-cloud-app-security"></a>Gerenciar aplicativos do OAuth usando o Office 365 Cloud App Security

|Avaliação * *\>**|Planejamento * *\>**|Implantação * *\>**|Utilização * * *|
|:-----|:-----|:-----|:-----|
|[Comece a avaliar](office-365-cas-overview.md) <br/> |[Começar a planejar](get-ready-for-office-365-cas.md) <br/> |[Começar a implantar](turn-on-office-365-cas.md) <br/> |Você está aqui!  <br/> [Próximas etapas](manage-app-permissions-in-ocas.md#nextsteps) <br/> |
   
Pessoas amor apps e eles baixá-las com frequência, especialmente os aplicativos que as pessoas utilizam pense salvará tempo, facilitando a obter no trabalho ou escola informações. No entanto, alguns aplicativos potencialmente poderia ser um risco de segurança para sua organização, dependendo de quais informações eles acessarem e como eles lidam com essas informações. Com a [Segurança de aplicativo de nuvem do Office 365](office-365-cas-overview.md), se você for um administrador global ou de segurança, você pode gerenciar aplicativos de OAuth para sua organização. Você pode ver as pessoas de aplicativos estão usando com dados do Office 365, que permissões estes aplicativos tem e muito mais. 
  
Este artigo descreve como criar uma consulta de aplicativo, como aprovar, proibir ou informar sobre um aplicativo e aonde ir para gerenciar aplicativos de OAuth.
  
## <a name="how-to-find-the-manage-oauth-apps-page"></a>Como encontrar a página Gerenciar OAuth aplicativos

> [!NOTE]
> Aplicativos do OAuth são gerenciados no portal de segurança de aplicativo de nuvem do Office 365. Você deve ser um administrador global ou administrador de segurança para executar a tarefa a seguir. Para saber mais, consulte [permissões no Office 365 Security &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md). 
  
1. Vá para o portal de segurança de aplicativo de nuvem ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) e entrar.
  
2. Escolha a **investigar** \> **OAuth apps**.<br/>![No portal do O365 CAS, escolha investigar.](media/OCAS-OAuthApps.png)<br/>
  
## <a name="what-youll-see-on-the-manage-oauth-apps-page"></a>O que você verá na página Gerenciar OAuth aplicativos

A tabela a seguir descreve os controles e opções disponíveis na página Gerenciar OAuth aplicativos.
  
|**Item**|**Descrição**|
|:-----|:-----|
|Ícone básica na barra de aplicativos de consulta  <br/> ![Ícone que indica o modo de exibição de consulta básica para consultar](media/a459bc51-e86b-43d5-a0ee-661b9fb4afc9.png)|Selecione essa opção para alternar para o modo de exibição avançado.  <br/> (Se você vir **básica**, você está usando o modo de exibição avançado)  <br/> |
|Ícone Avançado na barra de aplicativos de consulta  <br/> ![Ícone que indica o modo de exibição de consulta avançada para consultar](media/9958d832-2c81-45ed-a642-d926310ba6b6.png)|Selecione essa opção para alternar para modo de exibição básico.  <br/> (Se você vir **Avançado**, você está usando o modo de exibição básico.)  <br/> |
|Abrir ou fechar o ícone de todos os detalhes na lista de aplicativos  <br/> ![Clique nesse ícone para abrir ou fechar todos os detalhes para todos os aplicativos](media/018fa996-10e8-48ff-986e-55f2b69a5753.png)|Selecione esse ícone para exibir mais ou menos detalhes sobre cada aplicativo.  <br/> |
|Ícone de exportar na lista de aplicativos  <br/> ![Clique nesse ícone para exportar um arquivo csv de todos os aplicativos](media/98446851-fd96-4d09-9bb0-831db33090c1.png)|Selecione esse ícone para exportar um arquivo CSV que contém uma lista de aplicativos, o número de usuários para cada aplicativo, permissões associadas com o aplicativo, o nível de permissões, estado do aplicativo e usar nível de comunidade.  <br/> |
|Nome  <br/> |Usar esse recurso para ver o nome de um App. Selecione o nome para exibir mais informações, como seu descrição, o publisher, o site da Web app e o ID do aplicativo.  <br/> |
|Autorizado pelo  <br/> |Use esta opção para ver quantos usuários tenham autorizados a um aplicativo para acessar sua conta do Office 365. Selecione o número para exibir mais informações, como uma lista de contas de usuário.  <br/> |
|Nível de permissões  <br/> ![Ícone que indica o nível de permisiions para um aplicativo](media/aaebdd29-35b6-4c62-aef1-7c7817bd803d.png)|Use esta opção para ver quanto acesso um aplicativo tem aos dados do Office 365. Níveis de permissões indicam **baixa**, **média**ou **alta**, onde **baixa** pode indicar que o aplicativo acessa somente perfil e o nome de um usuário. Selecione o nível para exibir mais informações, como permissões concedidas para o aplicativo, o uso da comunidade e atividade relacionada no [log de governança](suspend-or-restore-an-account-in-ocas.md).<br/> |
|Última autorizados <br/> |Use esta opção para ver a data e hora de que um aplicativo de OAuth última foi autorizado para acessar dados do Office 365 da sua organização. <br/>  |
|Ações<br/>![Aplicativos do OAuth](media/OCAS-OAuthAppApproveBanReport.png)<br/> |Use esta opção para ver ou para marcar um aplicativo como aprovado ou Banned, um aplicativo do OAuth do relatório para a Microsoft ou deixá-lo como indeterminado.  <br/> |
   
## <a name="mark-an-app-as-approved"></a>Marcar um aplicativo como aprovados

Na página **Gerenciar OAuth apps** , localize o aplicativo que você deseja aprovar e escolha o ícone **app marca como aprovado** . 
  
![Escolha o aplicativo de marca como ícone aprovado](media/OCAS-MarkOAuthApproved.png)
  
O ícone fica verde, e o aplicativo em particular for aprovado para todos os usuários do Office 365.
  
> [!NOTE]
> Quando você marca um aplicativo como aprovados, não há nenhum efeito sobre o usuário final. Marcação visualmente os aplicativos que foram aprovados ajuda a separá-los dos aplicativos que ainda não foram revisados ainda. 
  
## <a name="ban-an-app"></a>Proibir um aplicativo

1. Na página **Gerenciar OAuth apps** , localize o aplicativo que você deseja proibir e escolha o ícone **app marca como proibidos** .<br/>![Escolha o aplicativo de marca como ícone proibido](media/OCAS-MarkOAuthBanned.png)
  
2. Na caixa de mensagem de notificação, mantenha o texto existente como está ou personalizar o texto. Escolha se deseja que os usuários saibam o que foi proibido seu aplicativo. <br/>![O modelo de email para um aplicativo proibido](media/6d132700-5f7f-472c-bfb5-a44549e69c16.jpg)<br/>
  
3. Escolha **aplicativo proibir**.

## <a name="report-an-oauth-app-to-microsoft"></a>Reportar um aplicativo do OAuth para a Microsoft

Se você deseja enviar um aplicativo do OAuth para a Microsoft para análise, é possível denunciar desse aplicativo.

1. Na página **Gerenciar OAuth apps** , localize o aplicativo que você deseja enviar para análise.

2. Escolha as reticências vertical e, em seguida, escolha **relatório App...**.<br/>![Informar sobre um aplicativo OAuth](media/OCAS-MarkOAuthReported.png)<br/>

3. Na caixa de diálogo **deste aplicativo de relatório** , use a lista suspensa para indicar sua preocupação. Por padrão, **Este aplicativo é mal-intencionado** está selecionada. No entanto, você pode escolher em uma das outras opções disponíveis.<br/>![Informar sobre um aplicativo OAuth](media/OCAS-ReportOAuthApp.png)<br/>

4. (Recomendado) Mantenha a opção para contatá-lo selecionado e o endereço de email listado confirmar (ou editar).

5. Escolha **Enviar**. 
    
## <a name="create-an-app-query"></a>Criar uma consulta de aplicativo

É recomendável usar o modo de exibição avançado, tem esta aparência: 

![Modo de exibição avançado](media/OCAS-OAuthAppsAdvQueryView.png)

Na barra de consulta do aplicativo, se você vir **Avançado**, você está usando o modo de exibição básico. Clique (ou toque) **Avançado** para ir para o modo de exibição avançado. 

![Exibição básica](media/OCAS-OAuthAppsBasicQueryView.png)
    
1. Na barra de consulta, use a lista **Selecionar um filtro** para escolher uma opção. 
    - **App** Aplicativos com determinados nomes
    - **Estado do aplicativo** Aplicativos com base em seu estado (aprovado, Banned ou Undetermined)
    - **Use da comunidade** Aplicativos com base na comunidade usam níveis (Rare, Uncommon ou comum)
    - **Nível de permissão** Aplicativos com base em determinados níveis de permissão 
    - **Permissões** Aplicativos que necessitam de determinadas permissões
    - **Publisher**  Aplicativos de determinados fornecedores
    - **Usuário** Aplicativos que um determinado usuário autorizado
   
2. Selecione **é igual a** ou **diferente**e, em seguida, especifique um valor para o filtro.
    
3. Para adicionar mais filtros, selecione o (sinal de adição![Adicionar um ícone de filtro para consultar aplicativos](media/771b2958-67cd-4e14-9302-283ef238cae5.jpg)) e repita as etapas 2 e 3.
    
4. Para remover um filtro, selecione o x (![Remover um ícone de filtro para consultar aplicativos](media/5339277f-555d-4749-8dcc-d2574250556e.jpg)) ao lado do nome de um filtro.
    
Os filtros são aplicados automaticamente e a lista de aplicativos é atualizada de acordo.
  
## <a name="next-steps"></a>Próximas etapas

- [Revise e agir em alertas](review-office-365-cas-alerts.md)
    
- Revise seus [logs de tráfego da Web e fontes de dados para segurança de aplicativo de nuvem do Office 365](web-traffic-logs-and-data-sources-for-ocas.md)
    
- Revise suas [atividades de utilização para segurança de aplicativo de nuvem do Office 365](utilization-activities-for-ocas.md)
    


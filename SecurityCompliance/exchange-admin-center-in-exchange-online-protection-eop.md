---
title: 'Centro de administração do Exchange na Proteção do Exchange Online '
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 97921f0e-832f-40c7-b56d-414faede5191
ms.collection:
- M365-security-compliance
description: O EAC (Centro de administração do Exchange) é o console de gerenciamento baseado na Web da EOP (Proteção do Exchange Online) da Microsoft.
ms.openlocfilehash: 0d1e56b85afe6655b5c6d08df51d4607df92d1d5
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220461"
---
# <a name="exchange-admin-center-in-exchange-online-protection"></a><span data-ttu-id="f4e57-103">Centro de administração do Exchange na Proteção do Exchange Online</span><span class="sxs-lookup"><span data-stu-id="f4e57-103">Exchange admin center in Exchange Online Protection</span></span> 

<span data-ttu-id="f4e57-104">O EAC (Centro de administração do Exchange) é o console de gerenciamento baseado na Web da EOP (Proteção do Exchange Online) da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f4e57-104">The Exchange admin center (EAC) is the web-based management console for Microsoft Exchange Online Protection (EOP).</span></span> 
  
<span data-ttu-id="f4e57-p101">Procurando a versão do Exchange 2013 deste tópico? Confira [Exchange admin center in Exchange 2013](http://technet.microsoft.com/library/a9aea11a-6ba3-4f4a-a76e-79072e7cfc7d.aspx).</span><span class="sxs-lookup"><span data-stu-id="f4e57-p101">Looking for the Exchange 2013 version of this topic? See [Exchange admin center in Exchange 2013](http://technet.microsoft.com/library/a9aea11a-6ba3-4f4a-a76e-79072e7cfc7d.aspx).</span></span>
  
<span data-ttu-id="f4e57-p102">Procurando a versão do Exchange Online deste tópico? Confira [Exchange admin center in Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center).</span><span class="sxs-lookup"><span data-stu-id="f4e57-p102">Looking for the Exchange Online version of this topic? See [Exchange admin center in Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center).</span></span>
  
## <a name="accessing-the-eac"></a><span data-ttu-id="f4e57-109">Acessando o EAC</span><span class="sxs-lookup"><span data-stu-id="f4e57-109">Accessing the EAC</span></span>

<span data-ttu-id="f4e57-p103">Na maioria dos casos, os clientes da EOP acessam o EAC por meio do Centro de administração do Office 365. Você encontra um link para a EOP no menu suspenso no bloco **Administrador**, que fica ao lado do bloco **Eu**. Clique no bloco **Administrador** e selecione **Proteção do Exchange Online** no menu suspenso para ir até o EAC.</span><span class="sxs-lookup"><span data-stu-id="f4e57-p103">In most cases, EOP customers will access the EAC through the Office 365 admin center. You can find a link to EOP in the drop-down menu in the **Admin** tile, which is next to the **Me** tile. Click the **Admin** tile and select **Exchange Online Protection** from the drop down menu to be taken to the EAC.</span></span> 
  
<span data-ttu-id="f4e57-p104">Você também pode acessar a página de entrada do Eat diretamente por meio da seguinte https://admin.protection.outlook.com/ecp/\<companydomain\>URL:. Por exemplo, https://admin.protection.outlook.com/ecp/contoso.onmicrosoft.com. Após especificar suas credenciais de usuário, você será levado diretamente para o Eat.</span><span class="sxs-lookup"><span data-stu-id="f4e57-p104">You can also access the EAC sign in page directly via the following URL: https://admin.protection.outlook.com/ecp/\<companydomain\>. For example, https://admin.protection.outlook.com/ecp/contoso.onmicrosoft.com. After specifying your user credentials you will be taken directly into the EAC.</span></span>
  
## <a name="common-user-interface-elements-in-the-eac"></a><span data-ttu-id="f4e57-116">Elementos da interface do usuário comuns no EAC</span><span class="sxs-lookup"><span data-stu-id="f4e57-116">Common user interface elements in the EAC</span></span>

<span data-ttu-id="f4e57-117">Esta seção descreve os elementos da interface do usuário encontrados no EAC.</span><span class="sxs-lookup"><span data-stu-id="f4e57-117">This section describes the user interface elements that are found in the EAC.</span></span>
  
![EOP-AdminCenter](media/EOP-AdminCenter.png)
  
### <a name="feature-pane"></a><span data-ttu-id="f4e57-119">Painel de recursos</span><span class="sxs-lookup"><span data-stu-id="f4e57-119">Feature Pane</span></span>

<span data-ttu-id="f4e57-p105">Este é o primeiro nível de navegação para a maioria das tarefas que você executará no EAC. O painel de recursos é organizado por áreas de recursos.</span><span class="sxs-lookup"><span data-stu-id="f4e57-p105">This is the first level of navigation for most of the tasks you'll perform in the EAC. The feature pane is organized by feature areas.</span></span>
  
1. <span data-ttu-id="f4e57-122">**Destinatários** Aqui, você vê os usuários internos e os contatos externos.</span><span class="sxs-lookup"><span data-stu-id="f4e57-122">**Recipients** This is where you'll view internal users and external contacts.</span></span> 
    
2. <span data-ttu-id="f4e57-123">**Permissões** Aqui, você gerencia as funções de administrador.</span><span class="sxs-lookup"><span data-stu-id="f4e57-123">**Permissions** This where you'll manage administrator roles.</span></span> 
    
3. <span data-ttu-id="f4e57-124">**Gerenciamento de Conformidade** Aqui, você encontra logs de auditoria e relatórios, como o relatório do grupo de funções de administrador.</span><span class="sxs-lookup"><span data-stu-id="f4e57-124">**Compliance Management** This is where you'll find audit logs and reports, such as the administrator role group report.</span></span> 
    
4. <span data-ttu-id="f4e57-125">**Proteção** Aqui, você gerencia a proteção antimalware e antispam da sua organização, além de gerenciar as mensagens em quarentena.</span><span class="sxs-lookup"><span data-stu-id="f4e57-125">**Protection** This is where you'll manage anti-malware and anti-spam protection for your organization, as well as manage messages in quarantine.</span></span> 
    
5. <span data-ttu-id="f4e57-126">**Fluxo de Mensagens** Aqui, você gerencia regras, domínios aceitos e conectores, além de executar o rastreamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="f4e57-126">**Mail Flow** This is where you'll manage rules, accepted domains, and connectors, as well as where you'll go to perform message trace.</span></span> 
    
### <a name="tabs"></a><span data-ttu-id="f4e57-127">Guias</span><span class="sxs-lookup"><span data-stu-id="f4e57-127">Tabs</span></span>

<span data-ttu-id="f4e57-p106">As guias são seu segundo nível de navegação. Cada uma das áreas de recursos contém várias guias, cada uma representando um recurso.</span><span class="sxs-lookup"><span data-stu-id="f4e57-p106">The tabs are your second level of navigation. Each of the feature areas contains various tabs, each representing a feature.</span></span>
  
### <a name="toolbar"></a><span data-ttu-id="f4e57-130">Barra de ferramentas</span><span class="sxs-lookup"><span data-stu-id="f4e57-130">Toolbar</span></span>

<span data-ttu-id="f4e57-p107">Ao clicar na maioria das guias, você verá uma barra de ferramentas. A barra de ferramentas possui ícones que realizam ações específicas, A tabela a seguir descreve os ícones e suas ações.</span><span class="sxs-lookup"><span data-stu-id="f4e57-p107">When you click most tabs, you'll see a toolbar. The toolbar has icons that perform a specific action. The following table describes the icons and their actions.</span></span>
  
|<span data-ttu-id="f4e57-134">**Ícone**</span><span class="sxs-lookup"><span data-stu-id="f4e57-134">**Icon**</span></span>|<span data-ttu-id="f4e57-135">**Nome**</span><span class="sxs-lookup"><span data-stu-id="f4e57-135">**Name**</span></span>|<span data-ttu-id="f4e57-136">**Action**</span><span class="sxs-lookup"><span data-stu-id="f4e57-136">**Action**</span></span>|
|:-----|:-----|:-----|
|![Ícone Adicionar](media/ITPro-EAC-AddIcon.gif)           <br/> |<span data-ttu-id="f4e57-138">Adicionar, Novo</span><span class="sxs-lookup"><span data-stu-id="f4e57-138">Add, New</span></span>  <br/> |<span data-ttu-id="f4e57-p108">Use esse ícone para criar um novo objeto. Alguns desses ícones têm uma seta para baixo associada, na qual é possível clicar para exibir objetos adicionais que você pode criar.</span><span class="sxs-lookup"><span data-stu-id="f4e57-p108">Use this icon to create a new object. Some of these icons have an associated down arrow you can click to show additional objects you can create.</span></span>  <br/> |
|![Ícone de edição](media/ITPro-EAC-EditIcon.gif)           <br/> |<span data-ttu-id="f4e57-142">Editar</span><span class="sxs-lookup"><span data-stu-id="f4e57-142">Edit</span></span>  <br/> |<span data-ttu-id="f4e57-143">Use esse ícone para editar um objeto.</span><span class="sxs-lookup"><span data-stu-id="f4e57-143">Use this icon to edit an object.</span></span>  <br/> |
|![Excluir ícone](media/ITPro-EAC-DeleteIcon.gif)           <br/> |<span data-ttu-id="f4e57-145">Excluir</span><span class="sxs-lookup"><span data-stu-id="f4e57-145">Delete</span></span>  <br/> |<span data-ttu-id="f4e57-p109">Use esse ícone para excluir um objeto. Alguns ícones excluídos têm uma seta para baixo na qual é possível clicar para mostrar opções adicionais.</span><span class="sxs-lookup"><span data-stu-id="f4e57-p109">Use this icon to delete an object. Some delete icons have a down arrow you can click to show additional options.</span></span>  <br/> |
|![Ícone Pesquisar](media/ITPro-EAC-.gif)           <br/> |<span data-ttu-id="f4e57-149">Pesquisar</span><span class="sxs-lookup"><span data-stu-id="f4e57-149">Search</span></span>  <br/> |<span data-ttu-id="f4e57-150">Use esse ícone para abrir uma caixa de pesquisa na qual é possível digitar a frase de pesquisa para um objeto que você deseja encontrar.</span><span class="sxs-lookup"><span data-stu-id="f4e57-150">Use this icon to open a search box in which you can type the search phrase for an object you want to find.</span></span>  <br/> |
|![Ícone Atualizar](media/ITPro-EAC-RefreshIcon.gif)           <br/> |<span data-ttu-id="f4e57-152">Atualizar</span><span class="sxs-lookup"><span data-stu-id="f4e57-152">Refresh</span></span>  <br/> |<span data-ttu-id="f4e57-153">Use essa opção para atualizar a exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="f4e57-153">Use this icon to refresh the list view.</span></span>  <br/> |
|![Ícone Mais opções](media/ITPro-EAC-MoreOptionsIcon.gif)           <br/> |<span data-ttu-id="f4e57-155">Mais opções</span><span class="sxs-lookup"><span data-stu-id="f4e57-155">More options</span></span>  <br/> |<span data-ttu-id="f4e57-p110">Use esse ícone para ver mais ações que podem ser realizadas para os objetos dessa guia. Por exemplo, em **Destinatários \> Usuários**, um clique neste ícone mostra a opção para executar uma **Pesquisa Avançada**.  </span><span class="sxs-lookup"><span data-stu-id="f4e57-p110">Use this icon to view more actions you can perform for that tab's objects. For example, in **Recipients \> Users** clicking this icon shows the option to perform an **Advanced Search**.  </span></span><br/> |
|![Ícone Seta para cima](media/ITPro-EAC-UpArrowIcon.gif)![Ícone Seta para baixo](media/ITPro-EAC-DownArrowIcon.gif)           <br/> |<span data-ttu-id="f4e57-160">Seta para cima e seta para baixo</span><span class="sxs-lookup"><span data-stu-id="f4e57-160">Up arrow and down arrow</span></span>  <br/> |<span data-ttu-id="f4e57-161">Use esses ícones para mover a prioridade de um objeto para cima ou para baixo.</span><span class="sxs-lookup"><span data-stu-id="f4e57-161">Use these icons to move an object's priority up or down.</span></span>  <br/> |
|![ícone Remover](media/ITPro-EAC-RemoveIcon.gif)           <br/> |<span data-ttu-id="f4e57-163">Remover</span><span class="sxs-lookup"><span data-stu-id="f4e57-163">Remove</span></span>  <br/> |<span data-ttu-id="f4e57-164">Use esse ícone para remover objetos de uma lista.</span><span class="sxs-lookup"><span data-stu-id="f4e57-164">Use this icon to remove objects from a list.</span></span>  <br/> |
   
### <a name="list-view"></a><span data-ttu-id="f4e57-165">Exibição de Lista</span><span class="sxs-lookup"><span data-stu-id="f4e57-165">List View</span></span>

<span data-ttu-id="f4e57-p111">Ao selecionar uma guia, na maioria dos casos, você verá uma exibição de lista. O limite visualizável com o modo de exibição em lista do EAC é de aproximadamente 10.000 objetos. Além disso, a paginação está incluída, para que você possa paginar os resultados.</span><span class="sxs-lookup"><span data-stu-id="f4e57-p111">When you select a tab, in most cases you'll see a list view. The viewable limit with the EAC list view is approximately 10,000 objects. In addition, paging is included so that you can page to results.</span></span>
  
### <a name="details-pane"></a><span data-ttu-id="f4e57-169">Painel de Detalhes</span><span class="sxs-lookup"><span data-stu-id="f4e57-169">Details Pane</span></span>

<span data-ttu-id="f4e57-p112">Quando você seleciona um objeto na exibição de lista, informações sobre esse objeto são exibidas no painel de detalhes. Em alguns casos, o painel de detalhes inclui tarefas de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="f4e57-p112">When you select an object from the list view, information about that object is displayed in the details pane. In some cases the details pane includes management tasks.</span></span>
  
### <a name="me-tile-and-help"></a><span data-ttu-id="f4e57-172">Bloco Eu e Ajuda</span><span class="sxs-lookup"><span data-stu-id="f4e57-172">Me tile and Help</span></span>

<span data-ttu-id="f4e57-p113">O bloco **Eu** permite sair do EAC e entrar como um usuário diferente. No menu suspenso **Ajuda**![Ícone Ajuda](media/ITPro-EAC-HelpIcon.gif), é possível realizar as seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="f4e57-p113">The **Me** tile allows you to sign out the EAC and sign in as a different user. From the **Help**![Help Icon](media/ITPro-EAC-HelpIcon.gif) drop-down menu, you can perform the following actions:</span></span> 
  
1. <span data-ttu-id="f4e57-175">**Ajuda** Clique em ![Ícone Ajuda](media/ITPro-EAC-HelpIcon.gif) para exibir o conteúdo da ajuda online.</span><span class="sxs-lookup"><span data-stu-id="f4e57-175">**Help** Click ![Help Icon](media/ITPro-EAC-HelpIcon.gif) to view the online help content.</span></span> 
    
2. <span data-ttu-id="f4e57-p114">**Desabilitar bolha de Ajuda** A bolha de Ajuda exibe ajuda contextual para os campos quando você cria ou edita um objeto. Você pode desativar a bolha de Ajuda ou ativá-la se tiver sido desabilitada.</span><span class="sxs-lookup"><span data-stu-id="f4e57-p114">**Disable Help bubble** The Help bubble displays contextual help for fields when you create or edit an object. You can turn off the Help bubble or turn it on if it has been disabled.</span></span> 
    
3. <span data-ttu-id="f4e57-178">**Direitos autorais** Clique neste link para ler o aviso de direitos autorais para o Exchange Online Protection.</span><span class="sxs-lookup"><span data-stu-id="f4e57-178">**Copyright** Click this link to read the copyright notice for Exchange Online Protection.</span></span> 
    
4. <span data-ttu-id="f4e57-179">**Privacidade** Clique para ler a política de privacidade do Proteção do Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="f4e57-179">**Privacy** Click to read the privacy policy for Exchange Online Protection.</span></span> 
    
## <a name="supported-browsers"></a><span data-ttu-id="f4e57-180">Navegadores com suporte</span><span class="sxs-lookup"><span data-stu-id="f4e57-180">Supported Browsers</span></span>

<span data-ttu-id="f4e57-p115">Para ter a melhor experiência ao usar o EAC, recomendamos que você sempre use os navegadores, clientes do Office e aplicativos mais recentes. Também recomendamos que você instale as atualizações de software quando elas estiverem disponíveis. Para obter mais informações sobre os navegadores suportados e requisitos do sistema para o serviço, consulte [Requisitos do sistema do Office 365](https://go.microsoft.com/fwlink/p/?LinkID=402699).</span><span class="sxs-lookup"><span data-stu-id="f4e57-p115">For the best experience using the EAC, we recommend that you always use the latest browsers, Office clients, and apps. We also recommend that you install software updates when they become available. For more information about the supported browsers and system requirements for the service, see [Office 365 System Requirements](https://go.microsoft.com/fwlink/p/?LinkID=402699).</span></span> 
  
## <a name="supported-languages-in-eop"></a><span data-ttu-id="f4e57-184">Idiomas com suporte na EOP</span><span class="sxs-lookup"><span data-stu-id="f4e57-184">Supported languages in EOP</span></span>

<span data-ttu-id="f4e57-185">Os seguintes idiomas têm suporte e estão disponíveis para o Proteção do Exchange Online:</span><span class="sxs-lookup"><span data-stu-id="f4e57-185">The following languages are supported and available for Exchange Online Protection.</span></span>
  
- <span data-ttu-id="f4e57-186">Amárico</span><span class="sxs-lookup"><span data-stu-id="f4e57-186">Amharic</span></span>
    
- <span data-ttu-id="f4e57-187">Árabe</span><span class="sxs-lookup"><span data-stu-id="f4e57-187">Arabic</span></span>
    
- <span data-ttu-id="f4e57-188">Basco (Basco)</span><span class="sxs-lookup"><span data-stu-id="f4e57-188">Basque (Basque)</span></span>
    
- <span data-ttu-id="f4e57-189">Bengali (Índia)</span><span class="sxs-lookup"><span data-stu-id="f4e57-189">Bengali (India)</span></span>
    
- <span data-ttu-id="f4e57-190">Búlgaro</span><span class="sxs-lookup"><span data-stu-id="f4e57-190">Bulgarian</span></span>
    
- <span data-ttu-id="f4e57-191">Catalão</span><span class="sxs-lookup"><span data-stu-id="f4e57-191">Catalan</span></span>
    
- <span data-ttu-id="f4e57-192">Chinês (simplificado)</span><span class="sxs-lookup"><span data-stu-id="f4e57-192">Chinese (Simplified)</span></span>
    
- <span data-ttu-id="f4e57-193">Chinês (tradicional)</span><span class="sxs-lookup"><span data-stu-id="f4e57-193">Chinese (Traditional)</span></span>
    
- <span data-ttu-id="f4e57-194">Croata</span><span class="sxs-lookup"><span data-stu-id="f4e57-194">Croatian</span></span>
    
- <span data-ttu-id="f4e57-195">Tcheco</span><span class="sxs-lookup"><span data-stu-id="f4e57-195">Czech</span></span>
    
- <span data-ttu-id="f4e57-196">Dinamarquês</span><span class="sxs-lookup"><span data-stu-id="f4e57-196">Danish</span></span>
    
- <span data-ttu-id="f4e57-197">Holandês</span><span class="sxs-lookup"><span data-stu-id="f4e57-197">Dutch</span></span>
    
- <span data-ttu-id="f4e57-198">Holandês</span><span class="sxs-lookup"><span data-stu-id="f4e57-198">Dutch</span></span>
    
- <span data-ttu-id="f4e57-199">Inglês</span><span class="sxs-lookup"><span data-stu-id="f4e57-199">English</span></span>
    
- <span data-ttu-id="f4e57-200">Estoniano</span><span class="sxs-lookup"><span data-stu-id="f4e57-200">Estonian</span></span>
    
- <span data-ttu-id="f4e57-201">Filipino (Filipinas)</span><span class="sxs-lookup"><span data-stu-id="f4e57-201">Filipino (Philippines)</span></span>
    
- <span data-ttu-id="f4e57-202">Finlandês</span><span class="sxs-lookup"><span data-stu-id="f4e57-202">Finnish</span></span>
    
- <span data-ttu-id="f4e57-203">Francês</span><span class="sxs-lookup"><span data-stu-id="f4e57-203">French</span></span>
    
- <span data-ttu-id="f4e57-204">Galego</span><span class="sxs-lookup"><span data-stu-id="f4e57-204">Galician</span></span>
    
- <span data-ttu-id="f4e57-205">Alemão</span><span class="sxs-lookup"><span data-stu-id="f4e57-205">German</span></span>
    
- <span data-ttu-id="f4e57-206">Grego</span><span class="sxs-lookup"><span data-stu-id="f4e57-206">Greek</span></span>
    
- <span data-ttu-id="f4e57-207">Gujarati</span><span class="sxs-lookup"><span data-stu-id="f4e57-207">Gujarati</span></span>
    
- <span data-ttu-id="f4e57-208">Hebraico</span><span class="sxs-lookup"><span data-stu-id="f4e57-208">Hebrew</span></span>
    
- <span data-ttu-id="f4e57-209">Híndi</span><span class="sxs-lookup"><span data-stu-id="f4e57-209">Hindi</span></span>
    
- <span data-ttu-id="f4e57-210">Húngaro</span><span class="sxs-lookup"><span data-stu-id="f4e57-210">Hungarian</span></span>
    
- <span data-ttu-id="f4e57-211">Islandês</span><span class="sxs-lookup"><span data-stu-id="f4e57-211">Icelandic</span></span>
    
- <span data-ttu-id="f4e57-212">Indonésio</span><span class="sxs-lookup"><span data-stu-id="f4e57-212">Indonesian</span></span>
    
- <span data-ttu-id="f4e57-213">Italiano</span><span class="sxs-lookup"><span data-stu-id="f4e57-213">Italian</span></span>
    
- <span data-ttu-id="f4e57-214">Japonês</span><span class="sxs-lookup"><span data-stu-id="f4e57-214">Japanese</span></span>
    
- <span data-ttu-id="f4e57-215">Kannada</span><span class="sxs-lookup"><span data-stu-id="f4e57-215">Kannada</span></span>
    
- <span data-ttu-id="f4e57-216">Cazaque</span><span class="sxs-lookup"><span data-stu-id="f4e57-216">Kazakh</span></span>
    
- <span data-ttu-id="f4e57-217">Quissuaíli</span><span class="sxs-lookup"><span data-stu-id="f4e57-217">Kiswahili</span></span>
    
- <span data-ttu-id="f4e57-218">Coreano</span><span class="sxs-lookup"><span data-stu-id="f4e57-218">Korean</span></span>
    
- <span data-ttu-id="f4e57-219">Letão</span><span class="sxs-lookup"><span data-stu-id="f4e57-219">Latvian</span></span>
    
- <span data-ttu-id="f4e57-220">Lituano</span><span class="sxs-lookup"><span data-stu-id="f4e57-220">Lithuanian</span></span>
    
- <span data-ttu-id="f4e57-221">Malaio (Brunei Darussalam)</span><span class="sxs-lookup"><span data-stu-id="f4e57-221">Malay (Brunei Darussalam)</span></span>
    
- <span data-ttu-id="f4e57-222">Malaio (Malásia)</span><span class="sxs-lookup"><span data-stu-id="f4e57-222">Malay (Malaysia)</span></span>
    
- <span data-ttu-id="f4e57-223">Malaiala</span><span class="sxs-lookup"><span data-stu-id="f4e57-223">Malayalam</span></span>
    
- <span data-ttu-id="f4e57-224">Marati</span><span class="sxs-lookup"><span data-stu-id="f4e57-224">Marathi</span></span>
    
- <span data-ttu-id="f4e57-225">Norueguês (Bokmål)</span><span class="sxs-lookup"><span data-stu-id="f4e57-225">Norwegian (Bokmål)</span></span>
    
- <span data-ttu-id="f4e57-226">Norueguês (Nynorsk)</span><span class="sxs-lookup"><span data-stu-id="f4e57-226">Norwegian (Nynorsk)</span></span>
    
- <span data-ttu-id="f4e57-227">Odia</span><span class="sxs-lookup"><span data-stu-id="f4e57-227">Oriya</span></span>
    
- <span data-ttu-id="f4e57-228">Persa</span><span class="sxs-lookup"><span data-stu-id="f4e57-228">Persian</span></span>
    
- <span data-ttu-id="f4e57-229">Polonês</span><span class="sxs-lookup"><span data-stu-id="f4e57-229">Polish</span></span>
    
- <span data-ttu-id="f4e57-230">Português (Brasil)</span><span class="sxs-lookup"><span data-stu-id="f4e57-230">Portuguese (Brazil)</span></span>
    
- <span data-ttu-id="f4e57-231">Português (Portugal)</span><span class="sxs-lookup"><span data-stu-id="f4e57-231">Portuguese (Portugal)</span></span>
    
- <span data-ttu-id="f4e57-232">Romeno</span><span class="sxs-lookup"><span data-stu-id="f4e57-232">Romanian</span></span>
    
- <span data-ttu-id="f4e57-233">Russo</span><span class="sxs-lookup"><span data-stu-id="f4e57-233">Russian</span></span>
    
- <span data-ttu-id="f4e57-234">Sérvio (cirílico, Sérvia)</span><span class="sxs-lookup"><span data-stu-id="f4e57-234">Serbian (Cyrillic, Serbia)</span></span>
    
- <span data-ttu-id="f4e57-235">Sérvio (Latino)</span><span class="sxs-lookup"><span data-stu-id="f4e57-235">Serbian (Latin)</span></span>
    
- <span data-ttu-id="f4e57-236">Eslovaco</span><span class="sxs-lookup"><span data-stu-id="f4e57-236">Slovak</span></span>
    
- <span data-ttu-id="f4e57-237">Esloveno</span><span class="sxs-lookup"><span data-stu-id="f4e57-237">Slovenian</span></span>
    
- <span data-ttu-id="f4e57-238">Espanhol</span><span class="sxs-lookup"><span data-stu-id="f4e57-238">Spanish</span></span>
    
- <span data-ttu-id="f4e57-239">Sueco</span><span class="sxs-lookup"><span data-stu-id="f4e57-239">Swedish</span></span>
    
- <span data-ttu-id="f4e57-240">Tâmil</span><span class="sxs-lookup"><span data-stu-id="f4e57-240">Tamil</span></span>
    
- <span data-ttu-id="f4e57-241">Télugo</span><span class="sxs-lookup"><span data-stu-id="f4e57-241">Telugu</span></span>
    
- <span data-ttu-id="f4e57-242">Tailandês</span><span class="sxs-lookup"><span data-stu-id="f4e57-242">Thai</span></span>
    
- <span data-ttu-id="f4e57-243">Turco</span><span class="sxs-lookup"><span data-stu-id="f4e57-243">Turkish</span></span>
    
- <span data-ttu-id="f4e57-244">Ucraniano</span><span class="sxs-lookup"><span data-stu-id="f4e57-244">Ukrainian</span></span>
    
- <span data-ttu-id="f4e57-245">Urdu</span><span class="sxs-lookup"><span data-stu-id="f4e57-245">Urdu</span></span>
    
- <span data-ttu-id="f4e57-246">Vietnamita</span><span class="sxs-lookup"><span data-stu-id="f4e57-246">Vietnamese</span></span>
    
- <span data-ttu-id="f4e57-247">Galês</span><span class="sxs-lookup"><span data-stu-id="f4e57-247">Welsh</span></span>
    


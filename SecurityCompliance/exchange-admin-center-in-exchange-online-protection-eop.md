---
title: 'Centro de administração do Exchange no Exchange Online Protection '
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 97921f0e-832f-40c7-b56d-414faede5191
description: O EAC (Centro de administração do Exchange) é o console de gerenciamento baseado na Web da EOP (Proteção do Exchange Online) da Microsoft.
ms.openlocfilehash: 99640e561b41e47a74e7c22f0bbdcacd0dd80bd7
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026308"
---
# <a name="exchange-admin-center-in-exchange-online-protection"></a><span data-ttu-id="512d4-103">Centro de administração do Exchange no Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="512d4-103">Exchange admin center in Exchange Online Protection</span></span> 

<span data-ttu-id="512d4-104">O EAC (Centro de administração do Exchange) é o console de gerenciamento baseado na Web da EOP (Proteção do Exchange Online) da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="512d4-104">The Exchange admin center (EAC) is the web-based management console for Microsoft Exchange Online Protection (EOP).</span></span> 
  
<span data-ttu-id="512d4-p101">Procurando a versão do Exchange 2013 deste tópico? Confira [Exchange admin center in Exchange 2013](http://technet.microsoft.com/library/a9aea11a-6ba3-4f4a-a76e-79072e7cfc7d.aspx).</span><span class="sxs-lookup"><span data-stu-id="512d4-p101">Looking for the Exchange 2013 version of this topic? See [Exchange admin center in Exchange 2013](http://technet.microsoft.com/library/a9aea11a-6ba3-4f4a-a76e-79072e7cfc7d.aspx).</span></span>
  
<span data-ttu-id="512d4-p102">Procurando a versão do Exchange Online deste tópico? Confira [Exchange admin center in Exchange Online](http://technet.microsoft.com/library/ace44f6b-4084-4f9c-89b3-e0317962472b.aspx).</span><span class="sxs-lookup"><span data-stu-id="512d4-p102">Looking for the Exchange Online version of this topic? See [Exchange admin center in Exchange Online](http://technet.microsoft.com/library/ace44f6b-4084-4f9c-89b3-e0317962472b.aspx).</span></span>
  
## <a name="accessing-the-eac"></a><span data-ttu-id="512d4-109">Acessando o EAC</span><span class="sxs-lookup"><span data-stu-id="512d4-109">Accessing the EAC</span></span>

<span data-ttu-id="512d4-p103">Na maioria dos casos, os clientes da EOP acessam o EAC por meio do Centro de administração do Office 365. Você encontra um link para a EOP no menu suspenso no bloco **Administrador**, que fica ao lado do bloco **Eu**. Clique no bloco **Administrador** e selecione **Proteção do Exchange Online** no menu suspenso para ir até o EAC.</span><span class="sxs-lookup"><span data-stu-id="512d4-p103">In most cases, EOP customers will access the EAC through the Office 365 admin center. You can find a link to EOP in the drop-down menu in the **Admin** tile, which is next to the **Me** tile. Click the **Admin** tile and select **Exchange Online Protection** from the drop down menu to be taken to the EAC.</span></span> 
  
<span data-ttu-id="512d4-p104">Você também pode acessar a página diretamente via a seguinte URL de entrada EAT: https://admin.protection.outlook.com/ecp/\<companydomain\>. Por exemplo, https://admin.protection.outlook.com/ecp/contoso.onmicrosoft.com. Após especificar suas credenciais de usuário, você será levado diretamente no EAC.</span><span class="sxs-lookup"><span data-stu-id="512d4-p104">You can also access the EAC sign in page directly via the following URL: https://admin.protection.outlook.com/ecp/\<companydomain\>. For example, https://admin.protection.outlook.com/ecp/contoso.onmicrosoft.com. After specifying your user credentials you will be taken directly into the EAC.</span></span>
  
## <a name="common-user-interface-elements-in-the-eac"></a><span data-ttu-id="512d4-116">Elementos da interface do usuário comuns no EAC</span><span class="sxs-lookup"><span data-stu-id="512d4-116">Common user interface elements in the EAC</span></span>
<span data-ttu-id="512d4-117"><a name="BKMK_CommonUserInterfaceElements"> </a></span><span class="sxs-lookup"><span data-stu-id="512d4-117"></span></span>

<span data-ttu-id="512d4-118">Esta seção descreve os elementos da interface do usuário encontrados no EAC.</span><span class="sxs-lookup"><span data-stu-id="512d4-118">This section describes the user interface elements that are found in the EAC.</span></span>
  
![EOP-AdminCenter](media/EOP-AdminCenter.png)
  
### <a name="feature-pane"></a><span data-ttu-id="512d4-120">Painel de recursos</span><span class="sxs-lookup"><span data-stu-id="512d4-120">Feature Pane</span></span>

<span data-ttu-id="512d4-p105">Este é o primeiro nível de navegação para a maioria das tarefas que você executará no EAC. O painel de recursos é organizado por áreas de recursos.</span><span class="sxs-lookup"><span data-stu-id="512d4-p105">This is the first level of navigation for most of the tasks you'll perform in the EAC. The feature pane is organized by feature areas.</span></span>
  
1. <span data-ttu-id="512d4-123">**Destinatários** Aqui, você vê os usuários internos e os contatos externos.</span><span class="sxs-lookup"><span data-stu-id="512d4-123">**Recipients** This is where you'll view internal users and external contacts.</span></span> 
    
2. <span data-ttu-id="512d4-124">**Permissões** Aqui, você gerencia as funções de administrador.</span><span class="sxs-lookup"><span data-stu-id="512d4-124">**Permissions** This where you'll manage administrator roles.</span></span> 
    
3. <span data-ttu-id="512d4-125">**Gerenciamento de Conformidade** Aqui, você encontra logs de auditoria e relatórios, como o relatório do grupo de funções de administrador.</span><span class="sxs-lookup"><span data-stu-id="512d4-125">**Compliance Management** This is where you'll find audit logs and reports, such as the administrator role group report.</span></span> 
    
4. <span data-ttu-id="512d4-126">**Proteção** Aqui, você gerencia a proteção antimalware e antispam da sua organização, além de gerenciar as mensagens em quarentena.</span><span class="sxs-lookup"><span data-stu-id="512d4-126">**Protection** This is where you'll manage anti-malware and anti-spam protection for your organization, as well as manage messages in quarantine.</span></span> 
    
5. <span data-ttu-id="512d4-127">**Fluxo de Mensagens** Aqui, você gerencia regras, domínios aceitos e conectores, além de executar o rastreamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="512d4-127">**Mail Flow** This is where you'll manage rules, accepted domains, and connectors, as well as where you'll go to perform message trace.</span></span> 
    
### <a name="tabs"></a><span data-ttu-id="512d4-128">Guias</span><span class="sxs-lookup"><span data-stu-id="512d4-128">Tabs</span></span>

<span data-ttu-id="512d4-p106">As guias são seu segundo nível de navegação. Cada uma das áreas de recursos contém várias guias, cada uma representando um recurso.</span><span class="sxs-lookup"><span data-stu-id="512d4-p106">The tabs are your second level of navigation. Each of the feature areas contains various tabs, each representing a feature.</span></span>
  
### <a name="toolbar"></a><span data-ttu-id="512d4-131">Barra de ferramentas</span><span class="sxs-lookup"><span data-stu-id="512d4-131">Toolbar</span></span>

<span data-ttu-id="512d4-p107">Ao clicar na maioria das guias, você verá uma barra de ferramentas. A barra de ferramentas possui ícones que realizam ações específicas, A tabela a seguir descreve os ícones e suas ações.</span><span class="sxs-lookup"><span data-stu-id="512d4-p107">When you click most tabs, you'll see a toolbar. The toolbar has icons that perform a specific action. The following table describes the icons and their actions.</span></span>
  
|<span data-ttu-id="512d4-135">**Ícone**</span><span class="sxs-lookup"><span data-stu-id="512d4-135">**Icon**</span></span>|<span data-ttu-id="512d4-136">**Nome**</span><span class="sxs-lookup"><span data-stu-id="512d4-136">**Name**</span></span>|<span data-ttu-id="512d4-137">**Action**</span><span class="sxs-lookup"><span data-stu-id="512d4-137">**Action**</span></span>|
|:-----|:-----|:-----|
|![Ícone Adicionar](media/ITPro-EAC-AddIcon.png)           <br/> |<span data-ttu-id="512d4-139">Adicionar, Novo</span><span class="sxs-lookup"><span data-stu-id="512d4-139">Add, New</span></span>  <br/> |<span data-ttu-id="512d4-p108">Use esse ícone para criar um novo objeto. Alguns desses ícones têm uma seta para baixo associada, na qual é possível clicar para exibir objetos adicionais que você pode criar.</span><span class="sxs-lookup"><span data-stu-id="512d4-p108">Use this icon to create a new object. Some of these icons have an associated down arrow you can click to show additional objects you can create.</span></span>  <br/> |
|![Ícone de edição](media/ITPro-EAC-EditIcon.png)           <br/> |<span data-ttu-id="512d4-143">Editar</span><span class="sxs-lookup"><span data-stu-id="512d4-143">Edit</span></span>  <br/> |<span data-ttu-id="512d4-144">Use esse ícone para editar um objeto.</span><span class="sxs-lookup"><span data-stu-id="512d4-144">Use this icon to edit an object.</span></span>  <br/> |
|![Excluir ícone](media/ITPro-EAC-DeleteIcon.png)           <br/> |<span data-ttu-id="512d4-146">Excluir</span><span class="sxs-lookup"><span data-stu-id="512d4-146">Delete</span></span>  <br/> |<span data-ttu-id="512d4-p109">Use esse ícone para excluir um objeto. Alguns ícones excluídos têm uma seta para baixo na qual é possível clicar para mostrar opções adicionais.</span><span class="sxs-lookup"><span data-stu-id="512d4-p109">Use this icon to delete an object. Some delete icons have a down arrow you can click to show additional options.</span></span>  <br/> |
|![Ícone Pesquisar](media/ITPro-EAC-.png)           <br/> |<span data-ttu-id="512d4-150">Pesquisar</span><span class="sxs-lookup"><span data-stu-id="512d4-150">Search</span></span>  <br/> |<span data-ttu-id="512d4-151">Use esse ícone para abrir uma caixa de pesquisa na qual é possível digitar a frase de pesquisa para um objeto que você deseja encontrar.</span><span class="sxs-lookup"><span data-stu-id="512d4-151">Use this icon to open a search box in which you can type the search phrase for an object you want to find.</span></span>  <br/> |
|![Ícone Atualizar](media/ITPro-EAC-RefreshIcon.png)           <br/> |<span data-ttu-id="512d4-153">Atualizar</span><span class="sxs-lookup"><span data-stu-id="512d4-153">Refresh</span></span>  <br/> |<span data-ttu-id="512d4-154">Use essa opção para atualizar a exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="512d4-154">Use this icon to refresh the list view.</span></span>  <br/> |
|![Ícone Mais opções](media/ITPro-EAC-MoreOptionsIcon.png)           <br/> |<span data-ttu-id="512d4-156">Mais opções</span><span class="sxs-lookup"><span data-stu-id="512d4-156">More options</span></span>  <br/> |<span data-ttu-id="512d4-p110">Use esse ícone para ver mais ações que podem ser realizadas para os objetos dessa guia. Por exemplo, em **Destinatários \> Usuários**, um clique neste ícone mostra a opção para executar uma **Pesquisa Avançada**.  </span><span class="sxs-lookup"><span data-stu-id="512d4-p110">Use this icon to view more actions you can perform for that tab's objects. For example, in **Recipients \> Users** clicking this icon shows the option to perform an **Advanced Search**.  </span></span><br/> |
|![Ícone Seta para cima](media/ITPro-EAC-UpArrowIcon.png)![Ícone Seta para baixo](media/ITPro-EAC-DownArrowIcon.png)           <br/> |<span data-ttu-id="512d4-161">Seta para cima e seta para baixo</span><span class="sxs-lookup"><span data-stu-id="512d4-161">Up arrow and down arrow</span></span>  <br/> |<span data-ttu-id="512d4-162">Use esses ícones para mover a prioridade de um objeto para cima ou para baixo.</span><span class="sxs-lookup"><span data-stu-id="512d4-162">Use these icons to move an object's priority up or down.</span></span>  <br/> |
|![ícone Remover](media/ITPro-EAC-RemoveIcon.png)           <br/> |<span data-ttu-id="512d4-164">Remover</span><span class="sxs-lookup"><span data-stu-id="512d4-164">Remove</span></span>  <br/> |<span data-ttu-id="512d4-165">Use esse ícone para remover objetos de uma lista.</span><span class="sxs-lookup"><span data-stu-id="512d4-165">Use this icon to remove objects from a list.</span></span>  <br/> |
   
### <a name="list-view"></a><span data-ttu-id="512d4-166">Exibição de Lista</span><span class="sxs-lookup"><span data-stu-id="512d4-166">List View</span></span>

<span data-ttu-id="512d4-p111">Ao selecionar uma guia, na maioria dos casos, você verá uma exibição de lista. O limite visualizável com o modo de exibição em lista do EAC é de aproximadamente 10.000 objetos. Além disso, a paginação está incluída, para que você possa paginar os resultados.</span><span class="sxs-lookup"><span data-stu-id="512d4-p111">When you select a tab, in most cases you'll see a list view. The viewable limit with the EAC list view is approximately 10,000 objects. In addition, paging is included so that you can page to results.</span></span>
  
### <a name="details-pane"></a><span data-ttu-id="512d4-170">Painel de Detalhes</span><span class="sxs-lookup"><span data-stu-id="512d4-170">Details Pane</span></span>

<span data-ttu-id="512d4-p112">Quando você seleciona um objeto na exibição de lista, informações sobre esse objeto são exibidas no painel de detalhes. Em alguns casos, o painel de detalhes inclui tarefas de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="512d4-p112">When you select an object from the list view, information about that object is displayed in the details pane. In some cases the details pane includes management tasks.</span></span>
  
### <a name="me-tile-and-help"></a><span data-ttu-id="512d4-173">Bloco Eu e Ajuda</span><span class="sxs-lookup"><span data-stu-id="512d4-173">Me tile and Help</span></span>

<span data-ttu-id="512d4-p113">O bloco **Eu** permite sair do EAC e entrar como um usuário diferente. No menu suspenso **Ajuda**![Ícone Ajuda](media/ITPro-EAC-HelpIcon.png), é possível realizar as seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="512d4-p113">The **Me** tile allows you to sign out the EAC and sign in as a different user. From the **Help**![Help Icon](media/ITPro-EAC-HelpIcon.png) drop-down menu, you can perform the following actions:</span></span> 
  
1. <span data-ttu-id="512d4-176">**Ajuda** Clique em ![Ícone Ajuda](media/ITPro-EAC-HelpIcon.png) para exibir o conteúdo da ajuda online.</span><span class="sxs-lookup"><span data-stu-id="512d4-176">**Help** Click ![Help Icon](media/ITPro-EAC-HelpIcon.png) to view the online help content.</span></span> 
    
2. <span data-ttu-id="512d4-p114">**Desabilitar bolha de Ajuda** A bolha de Ajuda exibe ajuda contextual para os campos quando você cria ou edita um objeto. Você pode desativar a bolha de Ajuda ou ativá-la se tiver sido desabilitada.</span><span class="sxs-lookup"><span data-stu-id="512d4-p114">**Disable Help bubble** The Help bubble displays contextual help for fields when you create or edit an object. You can turn off the Help bubble or turn it on if it has been disabled.</span></span> 
    
3. <span data-ttu-id="512d4-179">**Direitos autorais** Clique nesse link para ler o aviso de direitos autoral para o Exchange Online Protection.</span><span class="sxs-lookup"><span data-stu-id="512d4-179">**Copyright** Click this link to read the copyright notice for Exchange Online Protection.</span></span> 
    
4. <span data-ttu-id="512d4-180">**Privacidade** Clique para ler a política de privacidade do Proteção do Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="512d4-180">**Privacy** Click to read the privacy policy for Exchange Online Protection.</span></span> 
    
## <a name="supported-browsers"></a><span data-ttu-id="512d4-181">Navegadores com suporte</span><span class="sxs-lookup"><span data-stu-id="512d4-181">Supported Browsers</span></span>
<span data-ttu-id="512d4-182"><a name="BKMK_SupportedBrowsers"> </a></span><span class="sxs-lookup"><span data-stu-id="512d4-182"></span></span>

<span data-ttu-id="512d4-p115">Para ter a melhor experiência ao usar o EAC, recomendamos que você sempre use os navegadores, clientes do Office e aplicativos mais recentes. Também recomendamos que você instale as atualizações de software quando elas estiverem disponíveis. Para obter mais informações sobre os navegadores suportados e requisitos do sistema para o serviço, consulte [Requisitos do sistema do Office 365](https://go.microsoft.com/fwlink/p/?LinkID=402699).</span><span class="sxs-lookup"><span data-stu-id="512d4-p115">For the best experience using the EAC, we recommend that you always use the latest browsers, Office clients, and apps. We also recommend that you install software updates when they become available. For more information about the supported browsers and system requirements for the service, see [Office 365 System Requirements](https://go.microsoft.com/fwlink/p/?LinkID=402699).</span></span> 
  
## <a name="supported-languages-in-eop"></a><span data-ttu-id="512d4-186">Idiomas com suporte na EOP</span><span class="sxs-lookup"><span data-stu-id="512d4-186">Supported languages in EOP</span></span>
<span data-ttu-id="512d4-187"><a name="BKMK_SupportedLanguages"> </a></span><span class="sxs-lookup"><span data-stu-id="512d4-187"></span></span>

<span data-ttu-id="512d4-188">Os seguintes idiomas têm suporte e estão disponíveis para o Proteção do Exchange Online:</span><span class="sxs-lookup"><span data-stu-id="512d4-188">The following languages are supported and available for Exchange Online Protection.</span></span>
  
- <span data-ttu-id="512d4-189">Amárico</span><span class="sxs-lookup"><span data-stu-id="512d4-189">Amharic</span></span>
    
- <span data-ttu-id="512d4-190">Árabe</span><span class="sxs-lookup"><span data-stu-id="512d4-190">Arabic</span></span>
    
- <span data-ttu-id="512d4-191">Basco (Basco)</span><span class="sxs-lookup"><span data-stu-id="512d4-191">Basque (Basque)</span></span>
    
- <span data-ttu-id="512d4-192">Bengali (Índia)</span><span class="sxs-lookup"><span data-stu-id="512d4-192">Bengali (India)</span></span>
    
- <span data-ttu-id="512d4-193">Búlgaro</span><span class="sxs-lookup"><span data-stu-id="512d4-193">Bulgarian</span></span>
    
- <span data-ttu-id="512d4-194">Catalão</span><span class="sxs-lookup"><span data-stu-id="512d4-194">Catalan</span></span>
    
- <span data-ttu-id="512d4-195">Chinês (simplificado)</span><span class="sxs-lookup"><span data-stu-id="512d4-195">Chinese (Simplified)</span></span>
    
- <span data-ttu-id="512d4-196">Chinês (tradicional)</span><span class="sxs-lookup"><span data-stu-id="512d4-196">Chinese (Traditional)</span></span>
    
- <span data-ttu-id="512d4-197">Croata</span><span class="sxs-lookup"><span data-stu-id="512d4-197">Croatian</span></span>
    
- <span data-ttu-id="512d4-198">Tcheco</span><span class="sxs-lookup"><span data-stu-id="512d4-198">Czech</span></span>
    
- <span data-ttu-id="512d4-199">Dinamarquês</span><span class="sxs-lookup"><span data-stu-id="512d4-199">Danish</span></span>
    
- <span data-ttu-id="512d4-200">Holandês</span><span class="sxs-lookup"><span data-stu-id="512d4-200">Dutch</span></span>
    
- <span data-ttu-id="512d4-201">Holandês</span><span class="sxs-lookup"><span data-stu-id="512d4-201">Dutch</span></span>
    
- <span data-ttu-id="512d4-202">Inglês</span><span class="sxs-lookup"><span data-stu-id="512d4-202">English</span></span>
    
- <span data-ttu-id="512d4-203">Estoniano</span><span class="sxs-lookup"><span data-stu-id="512d4-203">Estonian</span></span>
    
- <span data-ttu-id="512d4-204">Filipino (Filipinas)</span><span class="sxs-lookup"><span data-stu-id="512d4-204">Filipino (Philippines)</span></span>
    
- <span data-ttu-id="512d4-205">Finlandês</span><span class="sxs-lookup"><span data-stu-id="512d4-205">Finnish</span></span>
    
- <span data-ttu-id="512d4-206">Francês</span><span class="sxs-lookup"><span data-stu-id="512d4-206">French</span></span>
    
- <span data-ttu-id="512d4-207">Galego</span><span class="sxs-lookup"><span data-stu-id="512d4-207">Galician</span></span>
    
- <span data-ttu-id="512d4-208">Alemão</span><span class="sxs-lookup"><span data-stu-id="512d4-208">German</span></span>
    
- <span data-ttu-id="512d4-209">Grego</span><span class="sxs-lookup"><span data-stu-id="512d4-209">Greek</span></span>
    
- <span data-ttu-id="512d4-210">Gujarati</span><span class="sxs-lookup"><span data-stu-id="512d4-210">Gujarati</span></span>
    
- <span data-ttu-id="512d4-211">Hebraico</span><span class="sxs-lookup"><span data-stu-id="512d4-211">Hebrew</span></span>
    
- <span data-ttu-id="512d4-212">Híndi</span><span class="sxs-lookup"><span data-stu-id="512d4-212">Hindi</span></span>
    
- <span data-ttu-id="512d4-213">Húngaro</span><span class="sxs-lookup"><span data-stu-id="512d4-213">Hungarian</span></span>
    
- <span data-ttu-id="512d4-214">Islandês</span><span class="sxs-lookup"><span data-stu-id="512d4-214">Icelandic</span></span>
    
- <span data-ttu-id="512d4-215">Indonésio</span><span class="sxs-lookup"><span data-stu-id="512d4-215">Indonesian</span></span>
    
- <span data-ttu-id="512d4-216">Italiano</span><span class="sxs-lookup"><span data-stu-id="512d4-216">Italian</span></span>
    
- <span data-ttu-id="512d4-217">Japonês</span><span class="sxs-lookup"><span data-stu-id="512d4-217">Japanese</span></span>
    
- <span data-ttu-id="512d4-218">Kannada</span><span class="sxs-lookup"><span data-stu-id="512d4-218">Kannada</span></span>
    
- <span data-ttu-id="512d4-219">Cazaque</span><span class="sxs-lookup"><span data-stu-id="512d4-219">Kazakh</span></span>
    
- <span data-ttu-id="512d4-220">Quissuaíli</span><span class="sxs-lookup"><span data-stu-id="512d4-220">Kiswahili</span></span>
    
- <span data-ttu-id="512d4-221">Coreano</span><span class="sxs-lookup"><span data-stu-id="512d4-221">Korean</span></span>
    
- <span data-ttu-id="512d4-222">Letão</span><span class="sxs-lookup"><span data-stu-id="512d4-222">Latvian</span></span>
    
- <span data-ttu-id="512d4-223">Lituano</span><span class="sxs-lookup"><span data-stu-id="512d4-223">Lithuanian</span></span>
    
- <span data-ttu-id="512d4-224">Malaio (Brunei Darussalam)</span><span class="sxs-lookup"><span data-stu-id="512d4-224">Malay (Brunei Darussalam)</span></span>
    
- <span data-ttu-id="512d4-225">Malaio (Malásia)</span><span class="sxs-lookup"><span data-stu-id="512d4-225">Malay (Malaysia)</span></span>
    
- <span data-ttu-id="512d4-226">Malaiala</span><span class="sxs-lookup"><span data-stu-id="512d4-226">Malayalam</span></span>
    
- <span data-ttu-id="512d4-227">Marati</span><span class="sxs-lookup"><span data-stu-id="512d4-227">Marathi</span></span>
    
- <span data-ttu-id="512d4-228">Norueguês (Bokmål)</span><span class="sxs-lookup"><span data-stu-id="512d4-228">Norwegian (Bokmål)</span></span>
    
- <span data-ttu-id="512d4-229">Norueguês (Nynorsk)</span><span class="sxs-lookup"><span data-stu-id="512d4-229">Norwegian (Nynorsk)</span></span>
    
- <span data-ttu-id="512d4-230">Odia</span><span class="sxs-lookup"><span data-stu-id="512d4-230">Oriya</span></span>
    
- <span data-ttu-id="512d4-231">Persa</span><span class="sxs-lookup"><span data-stu-id="512d4-231">Persian</span></span>
    
- <span data-ttu-id="512d4-232">Polonês</span><span class="sxs-lookup"><span data-stu-id="512d4-232">Polish</span></span>
    
- <span data-ttu-id="512d4-233">Português (Brasil)</span><span class="sxs-lookup"><span data-stu-id="512d4-233">Portuguese (Brazil)</span></span>
    
- <span data-ttu-id="512d4-234">Português (Portugal)</span><span class="sxs-lookup"><span data-stu-id="512d4-234">Portuguese (Portugal)</span></span>
    
- <span data-ttu-id="512d4-235">Romeno</span><span class="sxs-lookup"><span data-stu-id="512d4-235">Romanian</span></span>
    
- <span data-ttu-id="512d4-236">Russo</span><span class="sxs-lookup"><span data-stu-id="512d4-236">Russian</span></span>
    
- <span data-ttu-id="512d4-237">Sérvio (cirílico, Sérvia)</span><span class="sxs-lookup"><span data-stu-id="512d4-237">Serbian (Cyrillic, Serbia)</span></span>
    
- <span data-ttu-id="512d4-238">Sérvio (Latino)</span><span class="sxs-lookup"><span data-stu-id="512d4-238">Serbian (Latin)</span></span>
    
- <span data-ttu-id="512d4-239">Eslovaco</span><span class="sxs-lookup"><span data-stu-id="512d4-239">Slovak</span></span>
    
- <span data-ttu-id="512d4-240">Esloveno</span><span class="sxs-lookup"><span data-stu-id="512d4-240">Slovenian</span></span>
    
- <span data-ttu-id="512d4-241">Espanhol</span><span class="sxs-lookup"><span data-stu-id="512d4-241">Spanish</span></span>
    
- <span data-ttu-id="512d4-242">Sueco</span><span class="sxs-lookup"><span data-stu-id="512d4-242">Swedish</span></span>
    
- <span data-ttu-id="512d4-243">Tâmil</span><span class="sxs-lookup"><span data-stu-id="512d4-243">Tamil</span></span>
    
- <span data-ttu-id="512d4-244">Télugo</span><span class="sxs-lookup"><span data-stu-id="512d4-244">Telugu</span></span>
    
- <span data-ttu-id="512d4-245">Tailandês</span><span class="sxs-lookup"><span data-stu-id="512d4-245">Thai</span></span>
    
- <span data-ttu-id="512d4-246">Turco</span><span class="sxs-lookup"><span data-stu-id="512d4-246">Turkish</span></span>
    
- <span data-ttu-id="512d4-247">Ucraniano</span><span class="sxs-lookup"><span data-stu-id="512d4-247">Ukrainian</span></span>
    
- <span data-ttu-id="512d4-248">Urdu</span><span class="sxs-lookup"><span data-stu-id="512d4-248">Urdu</span></span>
    
- <span data-ttu-id="512d4-249">Vietnamita</span><span class="sxs-lookup"><span data-stu-id="512d4-249">Vietnamese</span></span>
    
- <span data-ttu-id="512d4-250">Galês</span><span class="sxs-lookup"><span data-stu-id="512d4-250">Welsh</span></span>
    


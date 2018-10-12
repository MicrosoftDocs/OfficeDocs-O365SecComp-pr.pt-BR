---
title: Configurar uma política de arquivamento e exclusão de caixas de correio em sua organização do Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/9/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MBS150
- BCS160
ms.assetid: ec3587e4-7b4a-40fb-8fb8-8aa05aeae2ce
description: Crie uma política de arquivamento e exclusão no Office 365 que automaticamente move itens à caixa de correio de arquivo morto do usuário.
ms.openlocfilehash: 740164ee840a32aff20f5c2dc1b1ae433d95cfe5
ms.sourcegitcommit: 448c5897e44448adfc82e3eaffb774c770c04815
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/12/2018
ms.locfileid: "25522292"
---
# <a name="set-up-an-archive-and-deletion-policy-for-mailboxes-in-your-office-365-organization"></a>Configurar uma política de arquivamento e exclusão de caixas de correio em sua organização do Office 365

 **Este artigo destina-se a administradores. Deseja adicionar políticas de arquivo morto e retenção para itens na sua caixa de correio? Consulte [atribuir a política de retenção para mensagens de email](https://support.office.com/article/3e5fd2dc-633f-4a38-b313-b31b81f7cf7a) | [políticas de retenção e arquivo morto no Outlook na web para negócios](https://support.office.com/article/465372e4-e16b-47db-bee0-aba44799085e)**
  
No Office 365, você pode criar uma política de arquivamento e exclusão que automaticamente move itens à caixa de correio de arquivo morto do usuário e exclui automaticamente os itens da caixa de correio. Você pode fazer isso criando uma política de retenção que ' s atribuída a caixas de correio e move itens à caixa de correio de arquivo morto do usuário depois de um certo período de tempo e que também exclui itens da caixa de correio depois atingirem um determinado limite de idade. As regras reais que determinam quais itens são movidas ou excluídas e quando isso acontece são marcas de retenção chamado. Marcas de retenção vinculadas a uma política de retenção, que por sua vez, é atribuída à caixa de correio do usuário. Uma marca de retenção aplica configurações de retenção para mensagens individuais e pastas na caixa de correio do usuário. Ele define quanto tempo uma mensagem permanece na caixa de correio e a ação a ser tomada quando a mensagem atingir a idade de retenção especificado. Quando uma mensagem atinge sua idade de retenção, ele é movido ou caixa de correio de arquivo morto do usuário ou que ele seja excluído. 
  
As etapas neste tópico irá configurar uma política de retenção e arquivamento para uma organização fictícia chamada Alpine House. Configurando a essa diretiva inclui as seguintes tarefas:
  
- Habilitar uma caixa de correio de arquivamento para cada usuário na organização. Isso oferece aos usuários armazenamento de caixa de correio de adição e é necessário para que uma política de retenção pode mover itens para a caixa de correio de arquivo morto. Ele também vamos um informações de arquivamento de repositório do usuário movendo itens a suas caixas de correio de arquivo morto. 
    
- Criando três marcas de retenção personalizada que faça o seguinte: 
    
  - Move automaticamente os itens que estão 3 anos a caixa de correio de arquivo morto do usuário. Mover itens para a caixa de correio de arquivo morto libera espaço na caixa de correio principal do usuário.
    
  - Exclui automaticamente os itens que têm 5 anos da pasta Itens excluídos. Isso também libera espaço na caixa de correio principal do usuário. Usuário terá a oportunidade de recuperar esses itens, se necessário. Consulte a nota de rodapé na seção [obter mais informações](set-up-an-archive-and-deletion-policy-for-mailboxes.md#moreinfo) , para obter mais detalhes. 
    
  - Automaticamente (e permanentemente) exclui os itens que estão sete anos antigos do ambas principal e caixa de correio de arquivo morto. Por causa de regulamentos de conformidade, alguns organização é necessárias para reter o email para um determinado período de tempo. Depois que o período de tempo expirar, uma organização talvez queira remover permanentemente essas caixas de correio de usuário de itens. 
    
- Criando uma nova política de retenção e adicionar as novas marcas de retenção personalizada a ele. Além disso, você adicionará também marcas de retenção integrada para a nova política de retenção. Isso inclui as marcas pessoais que os usuários podem atribuir aos itens em suas caixas de correio. Você também adicionará uma marca de retenção que move itens da pasta itens recuperáveis na caixa de correio principal do usuário para a pasta itens recuperáveis em suas caixas de correio de arquivo morto. Isso ajuda a libera espaço na pasta itens recuperáveis de um usuário, quando suas caixas de correio é colocada em espera.
    
Você pode seguir algumas ou todas as etapas neste artigo para configurar uma política de arquivamento e exclusão de caixas de correio em sua própria organização. Recomendamos que você teste esse processo em algumas caixas de correio antes de implementá-la em todas as caixas de correio em sua organização.
  
## <a name="before-you-begin"></a>Antes de começar

- Você precisa ser um administrador global na sua organização do Office 365 para executar as etapas neste tópico. 
    
-  Quando você cria uma nova conta de usuário no Office 365 e atribuir ao usuário uma licença do Exchange Online, uma caixa de correio é criada automaticamente para o usuário. Quando a caixa de correio é criada, ele tem automaticamente atribuído a uma política de retenção padrão, chamada política MRM padrão. Neste artigo, você criará uma nova política de retenção e atribuí-lo às caixas de correio do usuário, substituindo a política MRM padrão. Uma caixa de correio pode ter apenas uma política de retenção atribuída a ele qualquer momento.
    
- Para saber mais sobre marcas de retenção e políticas de retenção no Exchange Online, consulte [marcas de retenção e políticas de retenção](https://go.microsoft.com/fwlink/p/?LinkId=404424).
    
## <a name="step-1-enable-archive-mailboxes-for-users"></a>Etapa 1: Habilitar arquivar caixas de correio para usuários

A primeira etapa é habilitar a caixa de correio de arquivamento para cada usuário na sua organização. Caixa de correio de arquivo morto do usuário deve estar habilitado para que uma marca de retenção com uma ação de retenção "Mover para arquivamento" pode mover o item após a idade de retenção expira. 
  
> [!NOTE]
> Você pode habilitar caixas de correio de arquivo morto qualquer momento durante esse processo, desde que elas são habilitadas em algum momento antes de concluir o processo. Se uma caixa de correio de arquivo morto não estiver habilitada, nenhuma ação é executada em todos os itens que tenham uma política de arquivamento atribuída a ela. 
  
1. Acesse [https://protection.office.com](https://protection.office.com).
    
2. Entrar no Office 365 usando sua conta de administrador global.
    
    
3. Na segurança &amp; Centro de conformidade, vá para a **governança de dados** \> **arquivo morto**.
    
    É exibida uma lista de caixas de correio em sua organização e se a caixa de correio de arquivo morto correspondente está habilitada ou desabilitada. 
    
4. Marque as caixas de correio clicando em um primeiro na lista, mantenha pressionada a tecla **Shift** , e clicando em um último na lista. 
    
    > [!TIP]
    > Essa etapa pressupõe que nenhuma caixa de correio de arquivo está habilitadas. Se você tiver quaisquer caixas de correio com o arquivo morto habilitado, mantenha pressionada a tecla **Ctrl** e clique em cada caixa de correio que tem uma caixa de correio de arquivo morto desabilitado. Ou você pode clicar no cabeçalho da coluna de **caixa de correio de arquivo morto** para classificar as linhas com base em se a caixa de correio de arquivamento é habilitada ou desabilitada para facilitar a selecionar caixas de correio. 
  
5. No painel de detalhes, em **Editar em massa**, clique em **Ativar**.
    
    Será exibido um aviso dizendo que itens mais antigas que dois anos serão movidos para a nova caixa de correio de arquivo morto. Isso ocorre porque a política de retenção padrão que tiver atribuído a uma nova caixa de correio do usuário quando ele é criado possui uma marca de diretiva padrão de arquivamento que tenha uma idade de retenção de 2 anos. A marca de política padrão de arquivamento personalizado que você vai criar na etapa 2 tem uma idade de retenção de 3 anos. Isso significa que os itens que estão 3 anos ou mais antigos serão movidas para a caixa de correio de arquivo morto.
    
6. Clique em **Sim** para fechar a mensagem de aviso e iniciar o processo para habilitar a caixa de correio de arquivamento para cada caixa de correio selecionada. 
    
7. Quando o processo estiver concluído, clique em **Atualizar** ![atualizar](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png) para atualizar a lista na página **arquivo morto** . 
    
    A caixa de correio de arquivo morto está habilitada para todos os usuários em sua organização.
    
    ![A lista de caixas de correio com a caixa de correio de arquivo morto habilitado](media/61a7cb97-1bed-4808-aa5f-b6b761cfa8de.png)
  
8. Deixe a segurança &amp; abrir do Centro de conformidade. Você vai usá-lo na próxima etapa.
    
## <a name="step-2-create-new-retention-tags-for-the-archive-and-deletion-policies"></a>Etapa 2: Criar novas marcas de retenção para as políticas de arquivamento e exclusão

Nesta etapa, você criará as marcas de retenção personalizada três que foram descritas anteriormente.
  
- Alpine House 3 anos mover para arquivo morto (política de arquivamento personalizado)
    
- Alpine House 7 ano excluir permanentemente (política de exclusão personalizados)
    
- Alpine anos de 5 itens House excluído excluir e permitir recuperação (marca personalizada para a pasta Itens excluídos)
    
Para criar novas marcas de retenção, você usará o Centro de administração do Exchange (EAC) em sua organização do Exchange Online.
  
1. Na segurança &amp; Centro de conformidade, clique no iniciador app no canto superior esquerdo e, em seguida, clique no lado de **Administração** . 
    
2. No painel de navegação à esquerda do Centro de administração do Office 365, clique em **Admin centrais**e, em seguida, clique em **Exchange**.
    
    ![Captura de tela mostra que o Centro de administração do Office 365 com o administrador centrais expandida de opção e Exchange selecionado.](media/47399df2-0bc4-42e2-b183-07750a46bc68.png)
  
3. No EAC, vá até **gerenciamento de conformidade** \> **marcas de retenção**
    
    É exibida uma lista das marcas de retenção para a sua organização.
    
### <a name="create-a-custom-archive-default-policy-tag"></a>Criar uma marca de política personalizada de arquivamento padrão
  
Primeiro, você criará uma marca de diretiva um arquivo personalizado padrão (DPT) que moverá itens para a caixa de correio de arquivo morto após 3 anos. 
  
1. Na página **marcas de retenção** , clique em **nova marca**![novo ícone](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif)e selecione **aplicada automaticamente a caixa de correio inteira (padrão)**. 
    
2. Na página **nova marca aplicada automaticamente a caixa de correio inteira (padrão)** , preencha os seguintes campos: 
    
    ![Configurações para criar uma nova marca de política de padrão de arquivo morto](media/41c0a43c-9c72-44e0-8947-da0831896432.png)
  
1. **Nome** Digite um nome para a nova marca de retenção. 
    
2. **Ação de retenção** Selecione **Mover para arquivo morto** para mover itens para a caixa de correio de arquivo morto, quando o período de retenção expira. 
    
3. **Período de retenção** Selecione **quando o item atinge a seguinte idade (em dias)** e, em seguida, insira a duração do período de retenção. Para este cenário, itens serão movidas para a caixa de correio de arquivo morto após dias 1095 (3 anos).
    
4. **Comentário** (Opcional) Digite um comentário que explica a finalidade da marca de retenção personalizada. 
    
3. Clique em **Salvar** para criar o arquivo personalizado DPT. 
    
    O novo DPT de arquivamento é exibido na lista de marcas de retenção.
    
### <a name="create-a-custom-deletion-default-policy-tag"></a>Criar uma marca de política personalizada de exclusão padrão
  
Em seguida, você vai criar outro DPT personalizada, mas esse script será uma política de exclusão que exclui permanentemente os itens após sete anos.
  
1. Na página **marcas de retenção** , clique em **nova marca**![novo ícone](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif)e selecione **aplicada automaticamente a caixa de correio inteira (padrão)**. 
    
2. Na página **nova marca aplicada automaticamente a caixa de correio inteira (padrão)** , preencha os seguintes campos: 
    
    ![Configurações para criar uma nova marca de política de padrão de exclusão](media/f1f0ff62-eec9-4824-8e7c-d93dcfb09a79.png)
  
1. **Nome** Digite um nome para a nova marca de retenção. 
    
2. **Ação de retenção** Selecione **Excluir permanentemente** para limpar itens da caixa de correio quando o período de retenção expira. 
    
3. **Período de retenção** Selecione **quando o item atinge a seguinte idade (em dias)** e, em seguida, insira a duração do período de retenção. Para este cenário, os itens vão ser removidos após 2555 dias (7 anos).
    
4. **Comentário** (Opcional) Digite um comentário que explica a finalidade da marca de retenção personalizada. 
    
3. Clique em **Salvar** para criar a exclusão personalizada DPT. 
    
    O novo DPT de exclusão é exibido na lista de marcas de retenção.
    
### <a name="create-a-custom-retention-policy-tag-for-the-deleted-items-folder"></a>Criar uma marca de política de retenção personalizada para a pasta Itens excluídos
  
A última marca de retenção que você vai criar é uma marca de política de retenção personalizado (RPT) para a pasta Itens excluídos. Nesta marca excluirá itens na pasta Itens excluídos após cinco anos e fornece um ponto de recuperação quando os usuários podem usar a ferramenta de recuperar itens excluídos para recuperar um item.
  
1. Na página **marcas de retenção** , clique em **nova marca** ![novo ícone](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif)e selecione **aplicada automaticamente a uma pasta padrão**. 
    
2. Na página **nova marca aplicada automaticamente a uma pasta padrão** , preencha os seguintes campos: 
    
    ![Configurações para criar uma nova marca de política de retenção para a pasta Itens excluídos](media/6f3104bd-5edb-48ac-884d-5fe13d81dd1d.png)
  
1. **Nome** Digite um nome para a nova marca de retenção. 
    
2. **Aplicar nesta marca para a seguinte pasta padrão** Na lista suspensa, selecione os **Itens excluídos**.
    
3. **Ação de retenção** Selecione **Excluir e permitir recuperação** excluir itens quando o período de retenção expira, mas permitir que os usuários recuperar um item excluído dentro do período de retenção de item excluído (que, por padrão, é 14 dias). 
    
4. **Período de retenção** Selecione **quando o item atinge a seguinte idade (em dias)** e, em seguida, insira a duração do período de retenção. Para este cenário, os itens serão excluídos após 1825 dias (5 anos).
    
5. **Comentário** (Opcional) Digite um comentário que explica a finalidade da marca de retenção personalizada. 
    
3. Clique em **Salvar** para criar o RPT personalizado para a pasta Itens excluídos. 
    
    O novo RPT é exibido na lista de marcas de retenção.

## <a name="step-3-create-a-new-retention-policy"></a>Etapa 3: Criar uma nova política de retenção

Depois de criar as marcas de retenção personalizado, a próxima etapa é criar uma nova política de retenção e adicione as marcas de retenção. Você adicionará as três marcas de retenção personalizada que você criou na etapa 2 e as marcas internas que foram mencionadas na primeira seção. Na etapa 4, você vai atribuir essa nova política de retenção a caixas de correio do usuário.
  
1. No EAC, vá até **gerenciamento de conformidade** \> **políticas de retenção**.
    
2. Na página de **políticas de retenção** , clique em **novo** ![novo ícone](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif).
    
3. Na caixa **nome** , digite um nome para a nova política de retenção; Por exemplo, **arquivo morto de câmara Alpine e política de exclusão**. 
    
4. Em **marcas de retenção**, clique em **Adicionar** ![novo ícone](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif).
    
    É exibida uma lista das marcas de retenção em sua organização. Observe que as marcas personalizadas que você criou na etapa 2 são exibidas.
    
5. Adicione as marcas de retenção 9 que são destacadas na seguinte imagem (essas marcas são descritas em mais detalhes na seção [mais informações](set-up-an-archive-and-deletion-policy-for-mailboxes.md#moreinfo) ). Para adicionar uma marca de retenção, selecione-o e clique em **Adicionar**. 
    
    ![Adicionar marcas de retenção para a nova política de retenção](media/d8e87176-0716-4238-9e6a-7c4af35541dc.png)
  
    > [!TIP]
    > Você pode selecionar várias marcas de retenção mantendo pressionada a tecla **Ctrl** e clicando em cada marca. 
  
6. Depois de adicionar as marcas de retenção, clique em **Okey**.
    
7. Na página **nova política de retenção** , clique em **Salvar** para criar a nova diretiva. 
    
    A nova política de retenção é exibida na lista. Selecione para exibir as marcas de retenção vinculadas a ela, no painel de detalhes.
    
    ![A nova política de retenção e a lista de marcas de retenção vinculadas](media/63bc45e6-110b-4dc9-a85f-8eb1961a8258.png)
  
## <a name="step-4-assign-the-new-retention-policy-to-user-mailboxes"></a>Etapa 4: Atribuir a nova política de retenção a caixas de correio do usuário

Quando uma nova caixa de correio é criada, uma política de retenção denominada política MRM padrão é atribuída a ela, por padrão. Nesta etapa, você substituirá essa política de retenção (porque uma caixa de correio pode ter apenas uma política de retenção atribuída a ele), atribuindo a nova política de retenção que você criou na etapa 3 para as caixas de correio do usuário em sua organização. Essa etapa pressupõe que será atribuída a nova diretiva para todas as caixas de correio em sua organização.
  
1. No EAC, acesse **Destinatários ** \> **Caixas de Correio**.
    
    É exibida uma lista de todas as caixas de correio de usuário em sua organização. 
    
2. Marque as caixas de correio clicando em um primeiro na lista, mantenha pressionada a tecla **Shift** , e clicando em um último na lista. 
    
3. No painel de detalhes no lado direito do EAC, em **Editar em massa**, clique em **mais opções**.
    
4. Em **Política de Retenção**, clique em **Atualizar**.
    
5. Na página **em massa atribuir a política de retenção** , na lista suspensa **Selecione a política de retenção** , selecione a política de retenção que você criou na etapa 3; Por exemplo, **arquivo morto de câmara Alpine e política de retenção**.
    
6. Clique em **Salvar** para salvar a nova atribuição de política de retenção. 
    
7. Para verificar que a nova política de retenção foi atribuída às caixas de correio, você pode fazer o seguinte: selecione uma caixa de correio na página caixas de correio e clique em Editar. 
    
1. Selecione uma caixa de correio na página **caixas de correio** e clique em **Editar** ![editar](media/d7dc7e5f-17a1-4eb9-b42d-487db59e2e21.png). 
    
2. Na página de propriedades de caixa de correio do usuário selecionado, clique em **recursos de caixa de correio**.
    
    O nome da nova diretiva atribuída à caixa de correio é exibido na lista suspensa **política de retenção** . 
    

  
## <a name="optional-step-5-run-the-managed-folder-assistant-to-apply-the-new-settings"></a>(Opcional) Etapa 5: Executar o Assistente de pasta gerenciada para aplicar as novas configurações
<a name="step3"> </a>

Depois de aplicar a nova política de retenção a caixas de correio na etapa 4, pode demorar até sete dias no Exchange Online para que as novas configurações de retenção a ser aplicado às caixas de correio. Isso acontece porque um processo chamado as Assistente de pasta gerenciada caixas de correio de processos de uma vez a cada 7 dias. Em vez de esperar o Assistente de pasta gerenciada executar, você pode forçar isso aconteça, executando o cmdlet **Start-ManagedFolderAssistant** uma PowerShell no Exchange Online. 
  
 **o que acontece quando você executa o Assistente de pasta gerenciada?** Ele aplica as configurações na política de retenção inspecionando itens na caixa de correio e determinar se eles estão sujeitos a retenção. Ele então carimba itens sujeitos a retenção com a marca de retenção apropriadas e, em seguida, executa a ação de retenção especificado itens fora da sua idade de retenção. 
  
Aqui estão as etapas para se conectar ao Exchange Online PowerShell e execute o Assistente de pasta gerenciada em cada caixa de correio em sua organização.
  
1. No computador local, abra o Windows PowerShell e execute o comando a seguir.
    
    ```
    $UserCredential = Get-Credential
    ```

    Na caixa de diálogo **Solicitação de credencial do Windows PowerShell** , digite o nome de usuário e a senha da sua conta de administrador global do Office 365 e clique em **Okey**.
    
2. Execute o seguinte comando.
    
    ```
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://outlook.office365.com/powershell-liveid/ -Credential $UserCredential -Authentication Basic -AllowRedirection
    ```

3. Execute o seguinte comando.
    
    ```
    Import-PSSession $Session
    ```

4. Para verificar se você está conectado à sua organização do Exchange Online, execute o comando a seguir para obter uma lista de todas as caixas de correio de sua organização.
    
    ```
    Get-Mailbox
    ```

    > [!NOTE]
    > Para saber mais, ou se você tiver problemas para se conectar à sua organização do Exchange Online, confira [Conectar-se ao Exchange Online usando o PowerShell remoto](https://go.microsoft.com/fwlink/p/?LinkId=517283). 
  
5. Execute os dois comandos a seguir para iniciar o Assistente de pasta gerenciada para todas as caixas de correio do usuário em sua organização.
    
    ```
    $Mailboxes = Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"}
    ```

    ```
    $Mailboxes.Identity | Start-ManagedFolderAssistant
    ```

Isso é tudo! Você configurou uma política de arquivamento e de exclusão para a organização Alpine House.
  
## <a name="more-information"></a>Mais informações
<a name="moreinfo"> </a>

- Como a idade de retenção é calculada? A idade da retenção de itens de caixa de correio é calculado a partir da data de entrega ou a data de criação para itens como mensagens de rascunho que não são enviadas, mas são criados pelo usuário. Quando o Assistente de pasta gerenciada processa itens em uma caixa de correio, ele carimba uma data de início e uma data de validade para todos os itens que tenham marcas de retenção com a ação de retenção excluir e permitir recuperação ou excluir permanentemente. Itens que tenham uma marca de arquivo morto são marcados com uma move date. 
    
- A tabela a seguir fornece mais informações sobre cada marca de retenção é adicionada à política de retenção personalizada que foi criada seguindo as etapas neste tópico.
    
    |**Marca de retenção**|**O que significa nesta marca**|**Internos ou personalizados?**|**Tipo**|
    |:-----|:-----|:-----|:-----|
    |Alpine House movimentação de 3 anos para arquivo morto  <br/> |Move itens que estão 1095 dias (3 anos) na caixa de correio de arquivo morto.  <br/> |Sinalizador (consulte [etapa 2: criar novas marcas de retenção para as políticas de arquivamento e exclusão](set-up-an-archive-and-deletion-policy-for-mailboxes.md#step3) )  <br/> |Marca de diretiva padrão (archive); nesta marca será automaticamente aplicada à caixa de correio inteira.  <br/> |
    |Alpine House 7 anos excluir permanentemente  <br/> |Exclui permanentemente os itens na caixa de correio primária ou a caixa de correio de arquivo morto quando estiverem sete anos antigos.  <br/> |Sinalizador (consulte [etapa 2: criar novas marcas de retenção para as políticas de arquivamento e exclusão](set-up-an-archive-and-deletion-policy-for-mailboxes.md#step3) )  <br/> |Marca de diretiva padrão (exclusão); nesta marca será automaticamente aplicada à caixa de correio inteira.  <br/> |
    |Alpine House excluídos itens 5 anos excluir e permite recuperação  <br/> |Exclui os itens da pasta Itens excluídos que têm 5 anos. Os usuários podem recuperar esses itens para backup 14 dias após sendo excluído.<sup>\*</sup> <br/> |Sinalizador (consulte [etapa 2: criar novas marcas de retenção para as políticas de arquivamento e exclusão](set-up-an-archive-and-deletion-policy-for-mailboxes.md#step3) )  <br/> |Marca de política de retenção (itens excluídos); nesta marca será automaticamente aplicada a itens na pasta Itens excluídos.  <br/> |
    |Dias de 14 de itens recuperáveis mover para arquivo morto  <br/> |Move itens que tenham sido na pasta itens recuperáveis para 14 dias para a pasta itens recuperáveis na caixa de correio de arquivo morto.  <br/> |Integração  <br/> |Marca de política de retenção (itens recuperáveis); nesta marca será automaticamente aplicada aos itens na pasta itens recuperáveis.  <br/> |
    |Lixo eletrônico  <br/> |Exclui permanentemente os itens que foram na pasta Lixo eletrônico por 30 dias. Os usuários podem recuperar esses itens para backup 14 dias após sendo excluído.<sup>\*</sup> <br/> |Integração  <br/> |Marca de política de retenção (lixo eletrônico); nesta marca será automaticamente aplicada a itens na pasta Lixo eletrônico.  <br/> |
    |Excluir em 1 mês  <br/> |Exclui permanentemente os itens que são 30 dias. Os usuários podem recuperar esses itens para backup 14 dias após sendo excluído.<sup>\*</sup> <br/> |Integração  <br/> |Pessoais; nesta marca pode ser aplicada por usuários.  <br/> |
    |Excluir em 1 ano  <br/> |Exclui permanentemente os itens que estão 365 dias. Os usuários podem recuperar esses itens para backup 14 dias após sendo excluído.<sup>\*</sup> <br/> |Integração  <br/> |Pessoais; nesta marca pode ser aplicada por usuários.  <br/> |
    |Nunca excluir  <br/> |Nesta marca impedir que os itens que está sendo excluído por uma política de retenção.  <br/> |Integração  <br/> |Pessoais; nesta marca pode ser aplicada por usuários.  <br/> |
    |Pessoal: mover para arquivo morto em 1 ano  <br/> |Move itens na caixa de correio de arquivo morto após 1 ano.  <br/> |Integração  <br/> |Pessoais; nesta marca pode ser aplicada por usuários.  <br/> |
   
    > <sup>\*</sup>Os usuários podem usar a ferramenta de recuperar itens excluídos no Outlook e Outlook Web App para recuperar um item excluído dentro do período de retenção de item excluído, que, por padrão, há 14 dias no Exchange Online. Um administrador pode usar o Windows PowerShell para aumentar o período de retenção de item excluído até um máximo de 30 dias. Para obter mais informações, consulte: [recuperar itens excluídos no Outlook para Windows](https://support.office.com/article/49e81f3c-c8f4-4426-a0b9-c0fd751d48ce) e [alterar o período de retenção de item excluído de uma caixa de correio no Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=286940)
  
- Usando o livre ajuda de marca de retenção **14 de itens recuperáveis dias mover para arquivo morto** espaço de armazenamento na pasta itens recuperáveis na caixa de correio principal do usuário. Isso é útil quando a caixa de correio de um usuário é colocada em espera, o que significa que nada é nunca permanentemente excluídos da caixa de correio do usuário. Sem mover itens para a caixa de correio de arquivo morto, é possível que a cota de armazenamento para a pasta itens recuperáveis na caixa de correio principal seja atingida. Para obter mais informações sobre este e como evitá-lo, consulte [aumentar a cota de caixas de correio em retenção de itens recuperáveis](https://go.microsoft.com/fwlink/p/?LinkId=786479).

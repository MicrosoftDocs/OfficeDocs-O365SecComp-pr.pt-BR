---
title: A pesquisa de caixas de correio baseadas em nuvem para usuários locais no Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/4/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MST160
- MET150
ms.assetid: 3f7dde1a-a8ea-4366-86da-8ee6777f357c
description: Use a ferramenta de pesquisa de conteúdo no Office 365 Security &amp; Centro de conformidade para procurar e exportar dados de bate-papo MicrosoftTeams (chamados de chats 1xN) para usuários locais em uma implantação híbrida do Exchange.
ms.openlocfilehash: a504dfcf4c82bec036137b90312c01a0b2326ccc
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523864"
---
# <a name="searching-cloud-based-mailboxes-for-on-premises-users-in-office-365"></a>A pesquisa de caixas de correio baseadas em nuvem para usuários locais no Office 365

Se sua organização tem uma implantação híbrida do Exchange e tiver habilitado o Teams da Microsoft, os usuários podem usar o aplicativo de bate-papo de equipes para mensagens instantâneas. Para o usuário na nuvem, os dados de bate-papo de equipes (também chamados de chats 1xN) é salvo suas caixas de correio principal baseada na nuvem. Quando um usuário local usa o aplicativo de bate-papo de grupo, suas caixas de correio principal é localizado no local. Para contornar esta limitação, a Microsoft lançou um novo recurso em que uma área de armazenamento na nuvem (chamada de uma caixa de correio baseadas em nuvem para usuários no local) é criada para armazenar dados de bate-papo de equipes para usuários locais. Isso permite que você use a ferramenta de pesquisa de conteúdo no Office 365 Security &amp; equipes de centro de conformidade para pesquisar e exportar dados de chat para usuários locais. 
  
Aqui estão os requisitos e a limitação sobre a configuração e para configurar e caixas de correio baseadas em nuvem para usuários locais de pesquisa:
  
- As contas de usuário em seu serviço de diretório local (como o Active Directory) devem ser sincronizadas com o Windows Azure Active Directory, o serviço de diretório no Office 365. Isso significa que uma conta de usuário de email é criada no Office 365 e é associada a um usuário cuja caixa de correio principal está localizada na organização local.
    
- A caixa de correio baseadas em nuvem para usuários locais é usada apenas para armazenar dados de bate-papo de equipes. Um usuário local não consigo entrar na caixa de correio baseadas em nuvem ou acessar de forma alguma. Ele não pode ser usado para enviar ou receber mensagens de email. 
    
- Você precisa enviar uma solicitação ao Microsoft Support para permitir que sua organização pesquisar dados de chat para equipes nas caixas de correio baseadas em nuvem para usuários locais. Consulte [preenchendo uma solicitação com o Microsoft Support para habilitar esse recurso na segurança &amp; Centro de conformidade](#filing-a-request-with-microsoft-support-to-enable-this-feature-in-the-security-amp-compliance-center) neste artigo. 
    
 **Observação:** Conversas de canal de equipes sempre são armazenadas na caixa de correio baseadas em nuvem que está associado a equipe. Isso significa que você pode usar a pesquisa de conteúdo para conversas sem precisam uma solicitação de suporte do arquivo de canal de pesquisa. Para obter mais informações sobre como pesquisar equipes canal conversas, consulte [pesquisando equipes da Microsoft e grupos do Office 365](content-search.md#searching-microsoft-teams-and-office-365-groups).
  
## <a name="how-it-works"></a>Como funciona

Se um usuário habilitado para equipes da Microsoft possui uma caixa de correio local e seu produtos identidade da conta de usuário tenha sido sincronizada para a nuvem, o Microsoft cria uma caixa de correio baseadas em nuvem para armazenar os dados de bate-papo de equipes 1xN. Depois que os dados de bate-papo de equipes são armazenados na caixa de correio baseadas em nuvem, ela é indexada para pesquisa. Esse recurso permite usar pesquisa de conteúdo (e pesquisas associadas com os casos de eDiscovery) para pesquisar, visualizar e exportar dados de bate-papo de equipes para usuários locais. Você também pode usar ** \*ComplianceSearch** cmdlets de segurança do Office 365 &amp; PowerShell do Centro de conformidade para pesquisar por equipes dados de chat para usuários locais. 
  
O gráfico a seguir mostra o fluxo de trabalho de como as equipes de chat dados para usuários no local está disponível para pesquisa, visualizar e exportar.
  
![Armazenamento na nuvem para usuários locais no Microsoft Teams](media/895845f8-2ceb-47ed-96c9-5ab7f1aea916.png)
  
Além desse novo recurso, você ainda pode usar pesquisa de conteúdo para pesquisar, visualizar e exportar o conteúdo no site do SharePoint na nuvem e caixa de correio do Exchange associado a cada Team Microsoft e equipes 1xN dados de bate-papo na caixa de correio Exchange Online para as equipes usuários na nuvem.

## <a name="filing-a-request-with-microsoft-support-to-enable-this-feature-in-the-security-amp-compliance-center"></a>Preenchendo uma solicitação com o Microsoft Support para habilitar esse recurso na segurança &amp; Centro de conformidade

Precisa de uma solicitação com o Microsoft Support para habilitar a sua organização usar a interface gráfica do usuário na segurança arquivo &amp; Centro de conformidade para pesquisar dados de chat para equipes nas caixas de correio baseadas em nuvem para usuários locais. Observe que esse recurso está disponível na segurança do Office 365 &amp; PowerShell do Centro de conformidade. Você não precisa enviar uma solicitação de suporte para usar o PowerShell para pesquisar dados de bate-papo de equipes para usuários locais. 
  
Quando você envia a solicitação ao Microsoft Support, inclua as seguintes informações:
  
- O nome de domínio padrão da sua organização do Office 365.
    
- O ID do inquilino da sua organização do Office 365 e o nome do locatário. Você pode encontrá-los no portal do Azure Active Directory (em **Gerenciar** \> **Propriedades**). Consulte [Encontre seu ID de Inquilino do Office 365](https://support.office.com/article/6891b561-a52d-4ade-9f39-b492285e2c9b).
    
- O título ou a descrição do objetivo da solicitação de suporte a seguir: "Habilitar a pesquisa de conteúdo de aplicativo para usuários locais". Isso ajudará a rotear a solicitação para a equipe de engenharia de descoberta eletrônica de Office 365 que implementará a solicitação. 
    
Após a alteração de engenharia for feita, o Microsoft Support enviará uma data estimada de implantação. Observe que, em geral, o processo de implantação leva de 2 a 3 semanas após enviar a solicitação de suporte. 
  
### <a name="what-happens-after-this-feature-is-enabled"></a>O que acontece depois que esse recurso é habilitado?

Depois que esse recurso é implantado em sua organização do Office 365, as seguintes alterações são feitas na pesquisa de conteúdo e nas pesquisas associadas a um eDiscovery caso na segurança &amp; Centro de conformidade:
  
- A caixa de seleção **Adicionar Office conteúdo de aplicativo para usuários locais** será adicionada sob os **locais** na pesquisa de conteúdo. 
    
    ![A caixa de seleção "Adicionar conteúdo de aplicativo do Office para usuários no local" é adicionada para a interface de usuário de pesquisa de conteúdo](media/599e751e-17bd-408d-a18c-127538de6e85.png)
  
- Usuários locais são exibidos no seletor de locais de conteúdo que você usa para selecionar as caixas de correio do usuário a ser pesquisado. 
    

  
## <a name="searching-for-teams-chat-content-in-cloud-based-mailboxes-for-on-premises-users"></a>Pesquisar conteúdo de chat equipes em caixas de correio baseadas em nuvem para usuários locais

Depois que tiver sido habilitado o recurso, você pode usar a pesquisa de conteúdo na segurança &amp; Centro de conformidade para pesquisar dados de chat para equipes nas caixas de correio baseadas em nuvem para usuários locais. 
  
1. Na segurança &amp; Centro de conformidade, vá para **pesquisa &amp; investigação** \> **pesquisa de conteúdo**
    
2. Na página de **pesquisa** , clique em ![ícone Adicionar](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **nova pesquisa**.
    
    Conforme explicado anteriormente, a caixa de seleção **Adicionar Office conteúdo de aplicativo para usuários locais** é exibida em **locais**. Observe que ela está selecionada por padrão.
    
3. Crie a consulta de palavra-chave e adicionar condições para a consulta de pesquisa, se necessário. Para procurar somente equipe chats dados, você pode adicionar a seguinte consulta na caixa **palavras-chave** : 
    
    ```
    kind:im
    ``` 

4. Neste ponto, você pode escolher uma das opções a seguir em **locais**:
    
    - **Todos os locais** - Selecione essa opção para pesquisar as caixas de correio de todos os usuários em sua organização. Quando a caixa de seleção estiver marcada, todas as caixas de correio baseadas em nuvem para usuários locais também devem ser pesquisadas. 
    
    - **Locais específicos** - Selecione essa opção e, em seguida, clique em **Modificar** \> Escolher usuários, grupos ou equipes para pesquisar caixas de correio específicas. Conforme explicado anteriormente, o seletor de locais permitirá a procurar usuários no local. 
    
5. Salve e execute a pesquisa. Resultados da pesquisa de caixas de correio baseadas em nuvem para usuários locais podem ser visualizados como quaisquer outros resultados de pesquisa. Além disso, é possível que você pode exportar os resultados da pesquisa (incluindo quaisquer dados de bate-papo de equipes) para um arquivo PST. Para obter mais informações, consulte: 
    
    - [Criar uma nova pesquisa](content-search.md#create-a-new-search)
    
    - [Visualização de resultados de pesquisa](content-search.md#preview-search-results)
    
    - [Exportar resultados de pesquisa de conteúdo da segurança do Office 365 &amp; Centro de conformidade](export-search-results.md)
    
## <a name="using-powershell-to-search-for-teams-chat-data-in-cloud-based-mailboxes-for-on-premises-users"></a>Usando o PowerShell para pesquisar dados de chat para equipes em caixas de correio baseadas em nuvem para usuários locais

Você pode usar os cmdlets **New-ComplianceSearch** e **Set-ComplianceSearch** de segurança do Office 365 &amp; PowerShell do Centro de conformidade para pesquisar a caixa de correio baseadas em nuvem para usuários locais. Conforme explicado anteriormente, você não precisa enviar uma solicitação de suporte para usar o PowerShell para pesquisar dados de bate-papo de equipes para usuários locais. 
  
1. [Conectar-se à segurança do Office 365 &amp; PowerShell do Centro de conformidade](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).
    
2. Executar o PowerShell seguinte comando para criar um novo conteúdo procura as caixas de correio baseadas em nuvem de usuários no local.
    
    ```
    New-ComplianceSearch <name of new search> -ContentMatchQuery <search query> -ExchangeLocation <on-premises user> -IncludeUserAppContent $true -AllowNotFoundExchangeLocationsEnabled $true  
    ```
   
    O parâmetro *IncludeUserAppContent* é usado para especificar a caixa de correio baseadas em nuvem para o usuário ou usuários que são especificados pelo parâmetro *ExchangeLocation* . O *AllowNotFoundExchangeLocationsEnabled* permite que as caixas de correio baseadas em nuvem para usuários locais. Quando você usa o `$true` valor para esse parâmetro, a pesquisa não tenta validar a existência da caixa de correio antes que ele é executado. Isso é necessário para pesquisar as caixas de correio baseadas em nuvem para usuários locais, pois esses tipos de caixas de correio não resolverem como caixas de correio regulares. 
    
    O exemplo a seguir procura equipes chats (que são mensagens instantâneas) que contêm a palavra-chave "redstone" na caixa de correio baseadas em nuvem de Sara Davis, que é um usuário local na organização Contoso.
  
    ```
    New-ComplianceSearch "Redstone_Search" -ContentMatchQuery "redstone AND kind:im" -ExchangeLocation sarad@contoso.com -IncludeUserAppContent $true -AllowNotFoundExchangeLocationsEnabled $true  
    ```

   Depois de criar uma nova pesquisa, certifique-se de usar o cmdlet **Start-ComplianceSearch** para executar a pesquisa. 
  
Para obter mais informações utilizando esses cmdlets, consulte:
  
- [New-ComplianceSearch](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/new-compliancesearch)
    
- [Set-ComplianceSearch](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/set-compliancesearch)
    
- [Start-ComplianceSearch](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/start-compliancesearch)
    

## <a name="known-issues"></a>Problemas conhecidos

- No momento, você só pode pesquisar, visualizar e exportar conteúdo em caixas de correio baseadas em nuvem para usuários locais. Colocar uma caixa de correio baseadas em nuvem para um usuário local de uma isenção associada a um eDiscovery case ou atribuí-la a uma política de retenção do Office 365 não é suportado. 
    
- O seletor de local do conteúdo do eDiscovery contém exibe usuários de locais e permitirá que você selecione-os. No entanto, como previamente explicados que isenção não será aplicada ao usuário local.
    
## <a name="frequently-asked-questions"></a>Perguntas frequentes

 **Onde as caixas de correio baseadas em nuvem para usuários locais estão localizadas?**
  
Caixas de correio baseadas em nuvem são criadas e armazenadas no mesmo datacenter que sua organização do Office 365. 
  
 **Há outros requisitos que não seja enviando uma solicitação de suporte?**
  
 Conforme explicado anteriormente, as identidades dos usuários com caixas de correio no prem devem ser sincronizadas para sua organização baseada em nuvem para que uma conta de usuário de email correspondente é criada para cada conta de usuário local no Office 365. Além disso, sua organização deve ter uma assinatura do Office 365 enterprise, como uma assinatura do Office 365 Enterprise E1, E3 ou E5. 
  
 **Há um risco de perder os dados de bate-papo de equipes se a caixa de correio do usuário local for transferida para a nuvem?**
  
Não. Quando você migra a caixa de correio principal de um usuário local para a nuvem, os dados de bate-papo de equipes para esse usuário serão migrados para o seu novo correio primária baseada na nuvem.
  
 **Podem aplicar uma retenção de descoberta eletrônica ou políticas de retenção do Office 365 para usuários no local?**
  
Não.
  
 **Pode localizar de pesquisa de conteúdo mais antigas equipes chats para usuários locais antes do tempo minha organização enviados a solicitação para habilitar esse recurso?**
  
Microsoft iniciado armazenar os dados de bate-papo de equipes para usuários locais em 31 de janeiro de 2018. Assim, se a identidade de um usuário de equipes local tenha sido sincronizada entre o Active Directory e o Azure Active Directory desde essa data, em seguida, seus dados de bate-papo de equipes serão armazenados em uma caixa de correio baseadas em nuvem e serão pesquisáveis usando a pesquisa de conteúdo. Microsoft também está trabalhando sobre como armazenar dados de bate-papo de equipes de antes de 31 de janeiro de 2018 nas caixas de correio baseadas em nuvem para usuários locais. Para obter mais informações sobre isso estarão disponíveis em breve.

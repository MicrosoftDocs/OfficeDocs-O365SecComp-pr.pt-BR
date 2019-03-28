---
title: Pesquisando caixas de correio baseadas em nuvem para usuários locais no Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/4/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid:
- MOE150
- MST160
- MET150
ms.assetid: 3f7dde1a-a8ea-4366-86da-8ee6777f357c
description: Use a ferramenta de pesquisa de conteúdo no centro de &amp; conformidade de segurança do Office 365 para pesquisar e exportar dados de chat do MicrosoftTeams (chamados chat 1xN) para usuários locais em uma implantação híbrida do Exchange.
ms.openlocfilehash: b277557285df6944217b493bf0c5a11759f9d76b
ms.sourcegitcommit: 54a2cbe5d13f448e0c28655bdf88deb9e5434cac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/27/2019
ms.locfileid: "30935226"
---
# <a name="searching-cloud-based-mailboxes-for-on-premises-users-in-office-365"></a>Pesquisando caixas de correio baseadas em nuvem para usuários locais no Office 365

Se sua organização tiver uma implantação híbrida do Exchange e tiver habilitado o Microsoft Teams, os usuários poderão usar o aplicativo de chat do teams para mensagens instantâneas. Para o usuário baseado em nuvem, os dados de chat do Teams (também chamados de chats do 1xN) são salvos em sua caixa de correio baseada na nuvem principal. Quando um usuário local usa o aplicativo chat de equipe, sua caixa de correio principal está localizada no local. Para contornar essa limitação, a Microsoft lançou um novo recurso em que uma área de armazenamento baseada em nuvem (chamada de caixa de correio baseada em nuvem para usuários locais) é criada para armazenar dados de chat de equipes para usuários locais. Isso permite que você use a ferramenta de pesquisa de conteúdo no centro &amp; de conformidade de segurança do Office 365 para pesquisar e exportar dados de chat do teams para usuários locais. 
  
Estes são os requisitos e limitações para configurar e configurar e Pesquisar caixas de correio baseadas em nuvem para usuários locais:
  
- As contas de usuário no serviço de diretório local (como Active Directory) devem ser sincronizadas com o Active Directory do Azure, o serviço de diretório no Office 365. Isso significa que uma conta de usuário de email é criada no Office 365 e é associada a um usuário cuja caixa de correio principal está localizada na organização local.
    
- A caixa de correio baseada em nuvem para usuários locais é usada apenas para dados de chat de equipes de repositório. Um usuário local não pode entrar na caixa de correio baseada em nuvem ou acessar de qualquer forma. Ele não pode ser usado para enviar ou receber mensagens de email. 
    
- Você precisa enviar uma solicitação ao suporte da Microsoft para permitir que sua organização pesquise dados de chat de equipes nas caixas de correio baseadas em nuvem para usuários locais. ConFira [como arquivar uma solicitação com o suporte da Microsoft para habilitar esse recurso](#filing-a-request-with-microsoft-support-to-enable-this-feature) neste artigo. 
    
 **Observação:** As conversas de canal do teams sempre são armazenadas na caixa de correio baseada em nuvem associada à equipe. Isso significa que você pode usar a pesquisa de conteúdo para pesquisar conversas de canal sem ter que arquivar uma solicitação de suporte. Para obter mais informações sobre como Pesquisar conversas de canal de equipes, consulte [searchIng Microsoft Teams and Office 365 groups](content-search.md#searching-microsoft-teams-and-office-365-groups).
  
## <a name="how-it-works"></a>Como funciona

Se um usuário habilitado para o Microsoft Teams tem uma caixa de correio local e sua conta/identidade de usuário foi sincronizada com a nuvem, a Microsoft cria uma caixa de correio baseada em nuvem para armazenar dados de chat do 1xN Teams. Depois que os dados de bate-papo do teams são armazenados na caixa de correio baseada em nuvem, eles são indexados para pesquisa. Isso permite usar a pesquisa de conteúdo (e pesquisas associadas às ocorrências de descoberta eletrônica) para pesquisar, Visualizar e exportar dados de chat de equipes para usuários locais. você também pode usar ** \*** os cmdlets do ComplianceSearch no PowerShell do &amp; centro de conformidade de segurança do Office 365 para pesquisar dados de chat do teams para usuários locais. 
  
O gráfico a seguir mostra o fluxo de trabalho de como os dados de chat do Microsoft Teams para usuários locais estão disponíveis para pesquisa, visualização e exportação.
  
![Armazenamento baseado em nuvem para usuários locais no Microsoft Teams](media/895845f8-2ceb-47ed-96c9-5ab7f1aea916.png)
  
Além desse novo recurso, você ainda pode usar a pesquisa de conteúdo para pesquisar, Visualizar e exportar o conteúdo do teams no site do SharePoint baseado na nuvem e na caixa de correio do Exchange associada a todos os dados de chat do Microsoft Team e do 1xN Teams na caixa de correio do Exchange Online para usuários baseados em nuvem.

## <a name="filing-a-request-with-microsoft-support-to-enable-this-feature"></a>Como arquivar uma solicitação com o suporte da Microsoft para habilitar esse recurso

Você deve arquivar uma solicitação com o suporte da Microsoft para permitir que sua organização Use a interface gráfica do &amp; usuário no centro de conformidade de segurança para pesquisar dados de chat de equipes nas caixas de correio baseadas em nuvem para usuários locais. Observe que esse recurso está disponível no PowerShell do centro &amp; de conformidade de segurança do Office 365. Você não precisa enviar uma solicitação de suporte para usar o PowerShell para pesquisar dados de chat do teams para usuários locais. 
  
Inclua as seguintes informações ao enviar a solicitação para o suporte da Microsoft:
  
- O nome de domínio padrão da sua organização do Office 365.
    
- O nome do locatário e a ID do locatário de sua organização do Office 365. Você pode encontrá-los no portal do Azure Active Directory (em **gerenciar** \> **Propriedades**). ConFira [localizar sua ID de locatário do Office 365](https://support.office.com/article/6891b561-a52d-4ade-9f39-b492285e2c9b).
    
- O seguinte título ou descrição da finalidade da solicitação de suporte: "Habilitar pesquisa de conteúdo de aplicativo para usuários locais". Isso ajudará a encaminhar a solicitação para a equipe de engenharia de descoberta eletrônica do Office 365 que implementará a solicitação. 
    
Após a alteração da engenharia ser feita, o suporte da Microsoft lhe enviará uma data de implantação estimada. Observe que o processo de implantação geralmente leva 2-3 semanas após o envio da solicitação de suporte. 
  
### <a name="what-happens-after-this-feature-is-enabled"></a>O que acontece depois que este recurso é habilitado?

Depois que esse recurso é implantado na sua organização do Office 365, as seguintes alterações são feitas na pesquisa de conteúdo e nas pesquisas associadas a uma &amp; ocorrência de descoberta eletrônica no centro de conformidade de segurança:
  
- A caixa de seleção **adicionar conteúdo do aplicativo do Office para usuários locais** é adicionada sob os **locais** na pesquisa de conteúdo. 
    
    ![A caixa de seleção "adicionar conteúdo de aplicativo do Office para usuários locais" é adicionada à IU de pesquisa de conteúdo](media/599e751e-17bd-408d-a18c-127538de6e85.png)
  
- Os usuários locais são exibidos no seletor de locais de conteúdo que você usa para selecionar caixas de correio de usuário para pesquisa. 
    

  
## <a name="searching-for-teams-chat-content-in-cloud-based-mailboxes-for-on-premises-users"></a>Pesquisando conteúdo de chat do teams em caixas de correio baseadas em nuvem para usuários locais

Após a habilitação do recurso, você pode usar a pesquisa de conteúdo no &amp; centro de conformidade de segurança para pesquisar dados de chat de equipes nas caixas de correio baseadas em nuvem para usuários locais. 
  
1. No centro de &amp; conformidade de segurança, vá para pesquisa de \> **conteúdo** de **investigação de pesquisa &amp; **
    
2. Na página de **pesquisa** , clique ![em Adicionar](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) ícone **nova pesquisa**.
    
    Como explicado anteriormente, a caixa de seleção **adicionar conteúdo do aplicativo do Office para usuários locais** é exibida em **locais**. Observe que ela está selecionada por padrão.
    
3. Crie a consulta de palavra-chave e adicione condições à consulta de pesquisa, se necessário. Para pesquisar dados de chats de equipe apenas, você pode adicionar a seguinte consulta na caixa **palavras-chave** : 
    
    ```
    kind:im
    ``` 

4. Neste ponto, você pode escolher uma das seguintes opções em **locais**:
    
    - **Todos os locais** -Selecione essa opção para pesquisar as caixas de correio de todos os usuários em sua organização. Quando a caixa de seleção é selecionada, todas as caixas de correio baseadas em nuvem para usuários locais também serão pesquisadas. 
    
    - **Locais específicos** -Selecione essa opção e clique em **Modificar** \> escolher usuário, grupos ou equipes para pesquisar caixas de correio específicas. Conforme explicado anteriormente, o seletor de locais permitirá que você pesquise os usuários locais. 
    
5. Salve e execute a pesquisa. Quaisquer resultados de pesquisa das caixas de correio baseadas em nuvem para usuários locais podem ser visualizados como qualquer outro resultado de pesquisa. Além disso, você pode exportar os resultados da pesquisa (incluindo quaisquer dados de chat do Teams) para um arquivo PST. Para obter mais informações, consulte: 
    
    - [Criar uma nova pesquisa](content-search.md#create-a-new-search)
    
    - [Visualização de resultados de pesquisa](content-search.md#preview-search-results)
    
    - [Exportar resultados de pesquisa de conteúdo do centro de &amp; conformidade de segurança do Office 365](export-search-results.md)
    
## <a name="using-powershell-to-search-for-teams-chat-data-in-cloud-based-mailboxes-for-on-premises-users"></a>Usando o PowerShell para pesquisar dados de chat do teams em caixas de correio baseadas em nuvem para usuários locais

Você pode usar os cmdlets **New-ComplianceSearch** e **set-ComplianceSearch** no PowerShell do centro de &amp; conformidade de segurança do Office 365 para pesquisar a caixa de correio baseada em nuvem para usuários locais. Conforme explicado anteriormente, você não precisa enviar uma solicitação de suporte para usar o PowerShell para pesquisar dados de chat do teams para usuários locais. 
  
1. [Conecte-se ao PowerShell &amp; do centro de conformidade de segurança do Office 365](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).
    
2. Execute o seguinte comando do PowerShell para criar um novo conteúdo pesquisa as caixas de correio baseadas em nuvem de usuários locais.
    
    ```
    New-ComplianceSearch <name of new search> -ContentMatchQuery <search query> -ExchangeLocation <on-premises user> -IncludeUserAppContent $true -AllowNotFoundExchangeLocationsEnabled $true  
    ```
   
    O parâmetro *IncludeUserAppContent* é usado para especificar a caixa de correio baseada em nuvem para o usuário ou usuários que são especificados pelo parâmetro *ExchangeLocation* . O *AllowNotFoundExchangeLocationsEnabled* permite caixas de correio baseadas em nuvem para usuários locais. Quando você usa o `$true` valor para esse parâmetro, a pesquisa não tenta validar a existência da caixa de correio antes de ser executada. Isso é necessário para pesquisar as caixas de correio baseadas em nuvem para usuários locais, pois esses tipos de caixas de correio não são resolvidos como caixas de correio normais. 
    
    O exemplo a seguir procura por chats do Teams (que são mensagens instantâneas) que contêm palavra-chave "Redstone" na caixa de correio baseada em nuvem de Sara Davis, que é um usuário local na organização Contoso.
  
    ```
    New-ComplianceSearch "Redstone_Search" -ContentMatchQuery "redstone AND kind:im" -ExchangeLocation sarad@contoso.com -IncludeUserAppContent $true -AllowNotFoundExchangeLocationsEnabled $true  
    ```

   Depois de criar uma nova pesquisa, certifique-se de usar o cmdlet **Start-ComplianceSearch** para executar a pesquisa. 
  
Para obter mais informações sobre como usar esses cmdlets, consulte:
  
- [New-ComplianceSearch](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/new-compliancesearch)
    
- [Set-ComplianceSearch](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/set-compliancesearch)
    
- [Start-ComplianceSearch](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/start-compliancesearch)
    

## <a name="known-issues"></a>Problemas conhecidos

- No momento, só é possível pesquisar, Visualizar e exportar conteúdo em caixas de correio baseadas em nuvem para usuários locais. Não há suporte para a colocação de uma caixa de correio baseada em nuvem para um usuário local em um bloqueio associado a um caso de descoberta eletrônica ou a atribuição de uma política de retenção do Office 365. 
    
- O seletor de local de conteúdo para descoberta eletrônica exibe os usuários locais e permite que você os selecione. No enTanto, conforme explicado anteriormente, a suspensão não será aplicada ao usuário local.
    
## <a name="frequently-asked-questions"></a>Perguntas frequentes

 **Onde são localizadas caixas de correio baseadas em nuvem para usuários locais?**
  
Caixas de correio baseadas em nuvem são criadas e armazenadas no mesmo datacenter que sua organização do Office 365. 
  
 **Há outros requisitos diferentes de enviar uma solicitação de suporte?**
  
 Conforme explicado anteriormente, as identidades de usuários com caixas de correio locais devem ser sincronizadas com a sua organização baseada em nuvem para que uma conta de usuário de email correspondente seja criada para cada conta de usuário local no Office 365. Além disso, sua organização deve ter uma assinatura empresarial do Office 365, como uma assinatura do Office 365 Enterprise E1, E3 ou e5. 
  
 **Há um risco de perder os dados de chat do Microsoft Teams se a caixa de correio local do usuário for migrada para a nuvem?**
  
Não. Quando você migrar a caixa de correio principal de um usuário local para a nuvem, os dados de chat do teams para esse usuário serão migrados para sua nova caixa de correio principal baseada na nuvem.
  
 **Posso aplicar uma política de retenção de descoberta eletrônica ou do Office 365 a usuários locais?**
  
Não.
  
 **A pesquisa de conteúdo pode localizar chats mais antigos de equipes para usuários locais antes do momento em que minha organização enviou a solicitação para habilitar esse recurso?**
  
A Microsoft começou a armazenar dados de chat do Microsoft Teams para usuários locais em 31 de janeiro de 2018. Portanto, se a identidade de um usuário do teams local tiver sido sincronizada entre o Active Directory e o Azure Active Directory desde essa data, os dados de chat de suas equipes serão armazenados em uma caixa de correio baseada em nuvem e poderão ser pesquisados usando a pesquisa de conteúdo. A Microsoft também está trabalhando no armazenamento de dados de chat do Microsoft Teams de antes de 31 de janeiro de 2018 nas caixas de correio baseadas em nuvem para usuários locais. Mais informações sobre isso estarão disponíveis em breve.

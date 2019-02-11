---
title: Criar e gerenciar caixas de correio inativas no Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 296a02bd-ebde-4022-900e-547acf38ddd7
description: Você pode criar uma caixa de correio inativa no Office 365 aplicando uma espera ou a política de retenção do Office 365 à caixa de correio e, em seguida, excluindo a conta de usuário correspondente do Office 365. Itens em uma caixa de correio inativa são retidos para a duração da política de retenção ou retenção que foi aplicada a ele antes que ela foi feita inativa. Para excluir permanentemente uma caixa de correio inativa, basta remova a política de retenção ou retenção.
ms.openlocfilehash: de67068ded30f63e46a8a94c1030d45a12b56a2e
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29740833"
---
# <a name="create-and-manage-inactive-mailboxes-in-office-365"></a>Criar e gerenciar caixas de correio inativas no Office 365

O Office 365 torna possível a reter o conteúdo das caixas de correio excluídas. Esse recurso é chamado de [caixas de correio inativas](inactive-mailboxes-in-office-365.md). Caixas de correio inativas permitem que você reter email antigos empregados depois que saem da sua organização. Uma caixa de correio fica inativa quando um litígio ou uma política de retenção do Office 365 (criados no Office 365 Security &amp; Centro de conformidade) é aplicado à caixa de correio antes que a conta de usuário do Office 365 correspondente seja excluída. O conteúdo de uma caixa de correio inativa é retido para a duração da retenção feita na caixa de correio antes que ela foi feita inativa. Isso permite que os administradores responsáveis pela conformidade e registros gerentes usar a pesquisa de conteúdo na segurança &amp; Centro de conformidade para pesquisar e exportar o conteúdo de uma caixa de correio inativa. Caixas de correio inativas não podem receber email e não são exibidas no catálogo de endereços compartilhado da sua organização ou outras listas.
  
> [!NOTE]
> Adiamos o prazo de 1º de julho de 2017 para criar novos Bloqueios In-loco para tornar uma caixa de correio inativa. Mas no final deste ano ou no início do próximo, você não poderá criar novos Bloqueios In-loco no Exchange Online. Nesse momento, somente retenções de litígio e políticas de retenção do Office 365 poderão ser usadas para criar uma caixa de correio inativa. No entanto, as caixas de correio inativas existentes que estão com Bloqueio In-loco ainda terão suporte, e você poderá continuar a gerenciar Bloqueios In-loco em caixas de correio inativas. Isso inclui a alteração da duração de um Bloqueio In-loco e a exclusão permanente de uma caixa de correio inativa, removendo o Bloqueio In-loco. 
  
## <a name="before-you-begin"></a>Antes de começar

- Para tornar uma caixa de correio inativas, ele deve ser atribuído uma licença do Exchange Online plano 2 para que um litígio ou uma política de retenção do Office 365 pode ser aplicada à caixa de correio antes de serem excluído. Exchange Online plano 2 licenças são parte das assinaturas do Office 365 Enterprise E3 e E5. Se uma caixa de correio for atribuída a uma licença do Exchange Online plano 1 (que é parte de uma assinatura do Office 365 Enterprise E1), você teria que atribuir uma licença separada de arquivamento do Exchange Online para que possa ser aplicada a uma isenção à caixa de correio antes de serem excluído. Para obter mais informações, consulte [Arquivamento do Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=286153).
    
- A licença associada à caixa de correio Exchange Online excluída estará disponível depois que você excluir a conta de usuário correspondente do Office 365. Você pode então [Atribuir licenças aos usuários no Office 365 para empresas](https://support.office.com/article/997596b5-4173-4627-b915-36abac6786dc) para outro usuário. 
    
- Se um litígio ou uma política de retenção do Office 365 não é aplicada a uma caixa de correio, antes que ele seja excluído, o conteúdo da caixa de correio não será retido ou detectáveis. No entanto, a caixa de correio excluída pode ser recuperada dentro de 30 dias da exclusão, mas a caixa de correio e seu conteúdo será excluído permanentemente após 30 dias se ela não será recuperada.
    
- Para obter mais informações sobre retenção de litígio, consulte [bloqueio In-loco e retenção de litígio](https://go.microsoft.com/fwlink/p/?LinkId=846124). Para obter mais informações sobre as políticas de retenção do Office 365 na segurança &amp; Centro de conformidade, consulte [Overview of políticas de retenção no Office 365](retention-policies.md).
  
## <a name="create-an-inactive-mailbox"></a>Criar uma caixa de correio inativa

Tornar uma caixa de correio inativos envolve duas etapas: 1) colocar a caixa de correio em retenção de litígio ou aplicando uma política de retenção do Office 365 a ela e 2) excluindo a caixa de correio ou conta de usuário correspondente do Office 365. Depois que a caixa de correio está inativa, o seu conteúdo é mantido até que a política de retenção ou retenção seja removida.
  
### <a name="step-1-place-a-mailbox-on-litigation-hold-or-apply-an-office-365-retention-policy"></a>Etapa 1: Colocar uma caixa de correio em retenção de litígio ou aplicar uma política de retenção do Office 365

Colocar uma caixa de correio em retenção de litígio ou aplicar uma política de retenção do Office 365 retém o conteúdo na caixa de correio antes de serem excluído. Os dois tipos de isenções reterão todo o conteúdo de caixa de correio, incluindo itens excluídos e versões originais de itens modificados. Itens excluídos e modificados são mantidos na caixa de correio inativa por um período especificado, ou até que você excluir permanentemente a caixa de correio inativa, removendo a política de retenção ou retenção que é aplicada à caixa de correio inativa.
  
Se uma retenção já for colocada em uma caixa de correio, ou se uma política de retenção do Office 365 já for aplicada a uma caixa de correio, tudo o que você deve fazer é excluir a conta de usuário correspondente do Office 365, conforme explicado na etapa 2.
  
Para obter procedimentos passo a passo para a colocação de uma caixa de correio em retenção de litígio ou aplicando uma política de retenção do Office 365, consulte:
  
- [Colocar uma caixa de correio em Retenção de litígio](https://go.microsoft.com/fwlink/?linkid=856286)
    
- [Visão geral das políticas de retenção no Office 365](retention-policies.md)
    
> [!NOTE]
> Para retenções de litígio e políticas de retenção do Office 365, você pode criar um bloqueio indefinido ou em um tempo com base em espera. Em um bloqueio indefinido, o conteúdo da caixa de correio inativa será mantido indefinidamente ou até que a suspensão seja removida ou até que a duração da retenção é alterada. Depois que a política de retenção ou retenção for removida (supondo que a caixa de correio foi excluída há mais de 30 dias), a caixa de correio inativa será marcada para exclusão permanente e o conteúdo da caixa de correio deixará de ser retido ou detectáveis. Em uma baseadas em tempo de espera ou a política de retenção do Office 365, você deve especificar a duração da retenção. Esta duração é em uma base por item e é calculada a partir da data de um item de caixa de correio foi recebido ou criado. Depois que a retenção expira para um item de caixa de correio e que o item movido para ou está localizado na pasta itens recuperáveis na caixa de correio inativa, o item é excluído permanentemente (descartados) da caixa de correio inativa depois que o período de retenção de item excluído expira. 
  
### <a name="step-2-delete-the-mailbox"></a>Etapa 2: Excluir a caixa de correio

Depois que a caixa de correio é colocada em espera ou uma política de retenção do Office 365 é aplicada a ela, a próxima etapa é para excluir a caixa de correio. A melhor maneira de excluir uma caixa de correio é para excluir a conta de usuário do Office 365 correspondente no Centro de administração do Office 365. Para obter informações sobre a exclusão de contas de usuário do Office 365, consulte [Excluir um usuário da sua organização](https://support.office.com/article/d5155593-3bac-4d8d-9d8b-f4513a81479e).
  
> [!NOTE]
> Você também pode excluir a caixa de correio usando o cmdlet **Remove-Mailbox** no PowerShell do Exchange Online. Para obter mais informações, consulte [Excluir ou restaurar caixas de correio do usuário no Exchange Online](https://go.microsoft.com/fwlink/?linkid=856287). 
  

## <a name="view-a-list-of-inactive-mailboxes"></a>Exibir uma lista de caixas de correio inativas


Para exibir uma lista das caixas de correio inativas em sua organização:
  
1. Vá para [https://protection.office.com/](https://protection.office.com/) e entrar usando as credenciais para uma conta de administrador em sua organização do Office 365. 
    
2. No painel à esquerda da segurança &amp; Centro de conformidade, clique em **Governança dados** \> * * retenção * *.
    
3. Na página **retenção** , clique em **mais**![elipses da barra de navegação](media/9723029d-e5cd-4740-b5b1-2806e4f28208.gif)e clique em **caixas de correio inativas**.
    
    ![Na página retenção, clique em mais e clique em caixas de correio inativas para exibir uma lista de caixas de correio inativas](media/761bd90c-3e37-48f9-b1b9-479e90fea267.png)
  
    A página de **caixas de correio inativas** é exibida. Observe que o número total de caixas de correio inativas em sua organização é exibido. 
    
    ![É exibida uma lista de todas as caixas de correio inativas em sua organização](media/57d9d183-0c6c-4bd8-82e7-115f7b7b6de7.png)
  
Como alternativa, você pode executar o seguinte comando no Exchange Online PowerShell para exibir a lista de caixas de correio inativas.

```
 Get-Mailbox -InactiveMailboxOnly | FT DisplayName,PrimarySMTPAddress,WhenSoftDeleted
```

Você pode clicar em ![ícone de resultados de pesquisa de exportação](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **Exportar** para visualizar ou baixar um arquivo CSV que contém informações adicionais sobre as caixas de correio inativas em sua organização. 
  
Você também pode executar o comando a seguir para exportar a lista de caixas de correio inativas e outras informações para um arquivo CSV. Neste exemplo, o arquivo CSV é criado no diretório atual.

```
Get-Mailbox -InactiveMailboxOnly | Select Displayname,PrimarySMTPAddress,DistinguishedName,ExchangeGuid,WhenSoftDeleted | Export-Csv InactiveMailboxes.csv -NoType
```
   
> [!NOTE]
> É possível que uma caixa de correio inativa pode ter o mesmo endereço SMTP como uma caixa de correio de usuário ativo. Nesse caso, o valor da propriedade **DistinguishedName** ou **ExchangeGuid** pode ser usado para identificar exclusivamente uma caixa de correio inativa. 
  
## <a name="search-and-export-the-contents-of-an-inactive-mailbox"></a>Pesquisar e exportar o conteúdo de uma caixa de correio inativa

Você pode acessar o conteúdo da caixa de correio inativa, usando a ferramenta de pesquisa de conteúdo na segurança &amp; Centro de conformidade. Ao pesquisar uma caixa de correio inativa, você pode criar uma consulta de pesquisa de palavra-chave para procurar itens específicos ou é possível retornar todo o conteúdo da caixa de correio inativa. Você pode visualizar os resultados da pesquisa ou exportar os resultados da pesquisa para um arquivo de dados do Outlook (PST) ou como mensagens de email individuais. Para obter procedimentos passo a passo para as caixas de correio de pesquisa e exportar os resultados da pesquisa, consulte os seguintes tópicos:
  
- [Pesquisa de conteúdo no Office 365](content-search.md)
    
- [Exportar resultados de pesquisa de conteúdo da segurança do Office 365 &amp; Centro de conformidade](export-search-results.md)
    
Aqui estão algumas coisas ter em mente ao pesquisar caixas de correio inativas.
  
- Se uma pesquisa de conteúdo inclui uma caixa de correio do usuário e essa caixa de correio, em seguida, será feita inativa, continuará a pesquisa de conteúdo pesquisar a caixa de correio inativa quando você executar a pesquisa novamente depois que ele fique inativo.
    
- Em alguns casos, um usuário pode ter uma caixa de correio ativa e uma caixa de correio inativa que têm o mesmo endereço SMTP. Nesse caso, somente a caixa de correio específica que você selecionar como um local para uma pesquisa de conteúdo devem ser pesquisada. Em outras palavras, se você adicionar caixa de correio de um usuário a uma pesquisa, você não pode assumir que ambas as suas ativas e inativas caixas de correio devem ser pesquisadas; somente a caixa de correio que você os adicione explicitamente à pesquisa devem ser pesquisada.
    
- É altamente recomendável que você evite ter uma caixa de correio ativa e a caixa de correio inativa com o mesmo endereço SMTP. Se você precisar reutilizar o endereço SMTP que está atualmente atribuído a uma caixa de correio inativa, recomendamos que você recupere a caixa de correio inativa ou restaura o conteúdo de uma caixa de correio inativa para uma caixa de correio ativa (ou o arquivo morto de uma caixa de correio ativa) e exclua o caixa de correio inativa.
    
## <a name="change-the-hold-duration-for-an-inactive-mailbox"></a>Alterar a duração do bloqueio para uma caixa de correio inativa

Depois que uma caixa de correio é feita inativa, você pode alterar a duração da retenção ou a política de retenção do Office 365 aplicada à caixa de correio inativa. Para obter procedimentos passo a passo, consulte [alterar a duração de espera para uma caixa de correio inativa no Office 365](change-the-hold-duration-for-an-inactive-mailbox.md).
  
## <a name="recover-an-inactive-mailbox"></a>Recuperar uma caixa de correio inativa

Se um antigo funcionário retornará à sua organização, ou se um novo funcionário é contratado para assumir as responsabilidades de trabalho do funcionário departed, você pode recuperar o conteúdo da caixa de correio inativa. Ao recuperar uma caixa de correio inativa, a caixa de correio é convertida em uma nova caixa de correio, o conteúdo e estrutura de pastas da caixa de correio inativa são mantidos e a caixa de correio está vinculada a uma nova conta de usuário. Depois que ele seja recuperado, a caixa de correio inativa não existe mais. Para procedimentos passo a passo e obter mais informações sobre acontece quando você recuperar uma caixa de correio inativa, consulte [recuperar uma caixa de correio inativa no Office 365](recover-an-inactive-mailbox.md).
  
## <a name="restore-the-contents-of-an-inactive-mailbox-to-another-mailbox"></a>Restaurar o conteúdo de uma caixa de correio inativa em outra caixa de correio

Se outro funcionário leva as responsabilidades de trabalho de um funcionário anterior, ou se outra pessoa precisa acessar o conteúdo da caixa de correio inativa, você pode restaurar (ou mesclar) o conteúdo da caixa de correio inativa para uma caixa de correio existente. Quando você restaura uma caixa de correio inativa, o conteúdo é copiado para outra caixa de correio. A caixa de correio inativa é mantida e permanece uma caixa de correio inativa. A caixa de correio inativa ainda pode ser pesquisada usando a descoberta eletrônica, seu conteúdo possa ser restaurado para outra caixa de correio ou pode ser recuperado ou excluído posteriormente. Para obter procedimentos passo a passo, consulte [restaurar uma caixa de correio inativa no Office 365](restore-an-inactive-mailbox.md).
  
## <a name="delete-an-inactive-mailbox"></a>Excluir uma caixa de correio inativa

Se você não é mais necessário reter o conteúdo de uma caixa de correio inativa, você pode excluir permanentemente a caixa de correio inativa removendo isenção ou removendo a política de retenção do Office 365 aplicada à caixa de correio inativa. Se a caixa de correio foi excluída há mais de 30 dias, a caixa de correio será marcada para exclusão permanente depois de você remove a retenção e a caixa de correio se tornarão não recuperável. Se a caixa de correio foi excluída nos últimos 30 dias, você ainda poderá recuperar a caixa de correio depois de remover a política de retenção ou de espera. Para obter procedimentos passo a passo para a remoção de uma isenção ou uma política de retenção do Office 365 para excluir permanentemente uma caixa de correio inativa, consulte [Excluir uma caixa de correio inativa no Office 365](delete-an-inactive-mailbox.md).
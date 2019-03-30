---
title: Visão geral das caixas de correio inativas no Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/1/2018
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 1fbd74e8-7a60-4157-afe8-fe79f05d2038
description: Saiba mais sobre como reter o conteúdo de caixa de correio para funcionários antigos ao transformar a caixa de correio em uma caixa de correio inativa. Você pode fazer isso colocando a caixa de correio em retenção de litígio ou aplicando uma política de retenção do Office 365 à caixa de correio e, em seguida, removendo a conta do Office 365 correspondente.
ms.openlocfilehash: 12688cb1c0f1d165c21736ce5a6130245db36a06
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/29/2019
ms.locfileid: "31000794"
---
# <a name="overview-of-inactive-mailboxes-in-office-365"></a>Visão geral das caixas de correio inativas no Office 365

Sua organização, talvez seja necessário reter email antigos empregados depois que deixam a organização. Dependendo dos requisitos de retenção da sua organização, você pode precisar manter o conteúdo de caixa de correio para alguns meses ou anos após o término de emprego ou você pode precisar manter o conteúdo de caixa de correio indefinidamente. Independentemente de quanto tempo você precisa para reter o email, você pode criar caixas de correio inativas no Office 365 para manter a caixa de correio de antigos funcionários. 
  
## <a name="what-are-inactive-mailboxes"></a>Cite caixas de correio inativas.

Quando um funcionário deixa sua organização (ou fica em uma licença estendida de ausência), você pode remover a conta do Office 365. Os dados de caixa de correio do funcionário são mantidos por 30 dias após a conta ser removida. Durante esse período, você ainda pode recuperar os dados da caixa de correio, desfazendo a exclusão da conta. Após 30 dias, os dados são removidos permanentemente.
  
Mas se sua organização precisar reter o conteúdo de caixa de correio para ex-funcionários, você poderá transformar a caixa de correio em uma caixa de correio inativa, colocando a caixa de correio em retenção de litígio ou aplicando uma política de retenção do Office 365 à caixa de correio no centro de conformidade do & de segurança e, em seguida, removendo a conta correspondente do Office 365. The contents of an inactive mailbox are retained for the duration of the Litigation Hold placed on the mailbox or the retention period of the Office 365 retention policy applied to it before the mailbox was deleted. You can still recover the corresponding user account for a 30-day period. No enTanto, após 30 dias, a caixa de correio inativa é mantida no Office 365 até que a política de retenção ou bloqueio seja removida. 
  
**Importante:** Adiamos o prazo de 1º de julho de 2017 para criar novos bloqueios in-loco para tornar uma caixa de correio inativa. Mas no final deste ano ou no início do próximo, você não poderá criar novos Bloqueios In-loco no Exchange Online. Nesse momento, somente retenções de litígio e políticas de retenção do Office 365 poderão ser usadas para criar uma caixa de correio inativa. No entanto, as caixas de correio inativas existentes que estão com Bloqueio In-loco ainda terão suporte, e você poderá continuar a gerenciar Bloqueios In-loco em caixas de correio inativas. Isso inclui a alteração da duração de um Bloqueio In-loco e a exclusão permanente de uma caixa de correio inativa, removendo o Bloqueio In-loco. 
 
  
## <a name="inactive-mailboxes-and-office-365-retention-policies"></a>Caixas de correio inativas e políticas de retenção do Office 365

Além da retenção de litígio, o uso do novo recurso de política de retenção do Office 365 no centro de conformidade do & de segurança é outra maneira de tornar uma caixa de correio inativa. To use a retention policy to make an inactive mailbox: 
  
- Ele deve ser aplicadas a caixas de correio do Exchange ou locais de Skype for Business (porque o conteúdo relacionado à Skype é armazenado na caixa de correio do usuário). 
    
- Ela deve ser configurado para reter o conteúdo ou reter e, em seguida, o conteúdo de excluído. Se uma política de retenção estiver configurada para excluir apenas o conteúdo, a política é aplicada a uma caixa de correio não ficar inativa, quando a caixa de correio é excluída.
    
- Pode ser baseado em consulta para que ele mantém somente os itens que correspondem a uma consulta de pesquisa. 
    
Para obter mais informações sobre como configurar as políticas de retenção Office 365, consulte [Visão geral das políticas de retenção no Office 365](retention-policies.md).
  
Se você usar uma política de retenção Office 365 para tornar uma caixa de correio inativa, Office 365 continuará processar a política de retenção na caixa de correio inativa. Isso significa que se a política de retenção é configurada para manter e excluir conteúdo, itens serão movidos para a pasta itens recuperáveis quando a duração da retenção expira e eventualmente removidos da caixa de correio inativa. Se a política de retenção Office 365 não estiver configurada para itens excluídos, itens que ainda não foram excluídos permanentemente pelo usuário (antes que a caixa de correio foi feita inativa) não serão movidos para a pasta itens recuperáveis e serão mantidos indefinidamente depois que a caixa de correio se tornar inativa. 
  
Você pode considerar a criação de uma política de retenção Office 365 especificamente para caixas de correio inativas. Aqui estão alguns motivos para fazer isso e coisas em mente.
  
- Você pode configurar a política de retenção para reter somente desde que o necessário para atender aos requisitos da sua organização para ex-funcionários de conteúdo de caixa de correio.
    
- É uma maneira fácil de identificar caixas de correio inativas porque só será aplicada a política de retenção a caixas de correio inativas.
    
- You'll be able to easily identify the retention policy that's assigned to inactive mailboxes in your organization. This will make it easier to change the retention (or deletion) settings if necessary. Isso também facilitará a exclusão permanente de uma caixa de correio inativa, pois você só poderá removê-la da política usando o centro de conformidade do & de segurança. Caso contrário, será necessário usar o PowerShell do Exchange Online para remover uma retenção de litígio de uma caixa de correio inativa ou usar o & de segurança do centro de conformidade para excluir uma caixa de correio inativa de uma política de retenção do Office 365 em toda a organização.
    
- Se você criar uma política de retenção Office 365 especificamente para caixas de correio inativas, você pode adicionar um máximo de 1.000 caixas de correio para a política. Se você for uma organização muito grande, você pode precisar criar mais de uma política de retenção Office 365 a ser usado para caixas de correio inativas.
  
## <a name="inactive-mailboxes-and-ediscovery-case-holds"></a>Caixas de correio inativas e isenções casos de eDiscovery

Se uma retenção associada a um caso de descoberta eletrônica no centro de conformidade do & de segurança for colocada em uma caixa de correio e a conta de caixa de correio ou do usuário do Office 365 for excluída, a caixa de correio se tornará uma caixa de correio inativa. However, we don't recommend using eDiscovery case holds to make a mailbox inactive. That's because eDiscovery cases are intended for specific, time-bound cases related to a legal issue. At some point, a legal case will probably end and the holds associated with the case will be removed and the eDiscovery case will be closed. In fact, if a hold that's placed on an inactive mailbox is associated with an eDiscovery case, and then the hold is released or the eDiscovery case is closed (or deleted), the inactive mailbox will be permanently deleted. Additionally, you can't create a time-based eDiscovery hold. That's means content in an inactive mailbox will be retained forever or until the hold is removed and the inactive mailbox is deleted. Therefore, we recommend using a Litigation Hold or an Office 365 retention policy for inactive mailboxes.
  
Para obter mais informações sobre ocorrências de descoberta eletrônica e isenções, consulte [casos de descoberta eletrônica](ediscovery-cases.md).
  
## <a name="inactive-mailboxes-and-office-365-labels"></a>Caixas de correio inativas e rótulos do Office 365

Rótulos em Office 365 ajudarão-lo classificar dados de email na sua organização para um governança e impor regras de retenção com base nessa classificação. Um rótulo pode ser aplicado a um item de email manualmente por usuários ou automaticamente por administradores e um item de email só pode ter um rótulo único atribuído a ele. Se um item de email único na caixa de correio de um usuário possui um rótulo atribuído a ela e a caixa de correio ou a conta do usuário Office 365 for excluída, a caixa de correio se tornará uma caixa de correio inativa. Semelhante ao isenções casos de eDiscovery, não recomendamos o uso de rótulos para tornar uma caixa de correio inativa. Em vez disso, recomendamos que você use um litígio ou uma política de retenção Office 365. Lembre-se de que no caso de rótulos, talvez não saiba o que um rótulo tiver sido aplicada a um item de email e inadvertidamente tornar uma caixa de correio inativa quando você exclui a conta do usuário. 
  
Para obter mais informações sobre rótulos, consulte [Visão geral dos rótulos no Office 365](labels.md).
  
## <a name="inactive-mailboxes-and-exchange-mrm-retention-policies"></a>Caixas de correio inativas e políticas de retenção de MRM do Exchange

Se uma política de retenção do Exchange (o recurso Gerenciamento de registros de mensagens ou MRM, no Exchange Online ) foi aplicada à caixa de correio quando ela foi feita inativa, quaisquer políticas de exclusão (que são configuradas com uma ação de retenção **Excluir** as marcas de retenção) continuarão a serem processados na caixa de correio inativa. Isso significa que os itens que estão marcados com uma política de exclusão serão movidos para a pasta itens recuperáveis quando o período de retenção expira. Os itens são removidos da caixa de correio inativa quando a duração da retenção expira. Se um período de retenção não for especificado para a caixa de correio inativa, itens na pasta recuperar itens serão mantidos indefinidamente. 
  
Por outro lado, quaisquer políticas de arquivamento (que são marcas de retenção configuradas com uma ação de retenção **MoveToArchive** ) que estão incluídas na política de retenção atribuída a uma caixa de correio inativa serão ignoradas. Isso significa que itens em uma caixa de correio inativa que estão marcados com uma política de arquivamento permanecerá na caixa de correio principal quando o período de retenção expira. Elas não serão movidas para a caixa de correio de arquivo morto ou para a pasta itens recuperáveis na caixa de correio de arquivo morto. Eles serão mantidos indefinidamente. 
  
## <a name="creating-an-inactive-mailbox"></a>Criando uma caixa de correio inativa

Para tornar uma caixa de correio inativas, ele deve ser atribuído uma licença Exchange Online (plano 2) para que possa ser aplicada a uma política de retenção de litígio ou Office 365 à caixa de correio antes de serem excluído. Depois que a caixa de correio for excluída, a licença do Exchange Online associada a ela estará disponível para ser atribuída a um novo usuário. Caixas de correio inativas não exigem licenças em andamento.
  
A tabela a seguir resume o processo para tornar uma caixa de correio inativa para cenários de retenção diferente. Para obter mais informações, consulte [gerenciar caixas de correio inativas no Office 365](create-and-manage-inactive-mailboxes.md).
  
|**Para...**|**Faça isso …**|**Resultado**|
|:-----|:-----|:-----|
|Manter o conteúdo de caixa de correio indefinidamente depois que um funcionário deixa a organização  <br/> | Colocar a caixa de correio em retenção de litígio ou aplicar uma política de retenção Office 365 à caixa de correio.  <br/>  Não especificar um período de retenção para retenção de litígio ou não configurar a política de retenção Office 365 para excluir itens; Como alternativa, você pode usar uma política de retenção que mantém os itens indefinidamente.  <br/>  Remova a conta do usuário Office 365.  <br/> |Todo o conteúdo da caixa de correio inativa, incluindo itens na pasta itens recuperáveis, é retido indefinidamente.  <br/> |
|Manter o conteúdo de caixa de correio por um período específico após um funcionário deixa a organização e exclua-  <br/> | Aplicar uma política de retenção do Office 365 à caixa de correio.  <br/>  Configure a política de retenção para reter e, em seguida, excluir itens quando o período de retenção expirar.  <br/>  Remova a conta do usuário Office 365.  <br/> |Quando o período de retenção de um item de caixa de correio expira, o item é movido para a pasta itens recuperáveis e, em seguida, é excluído permanentemente (removido) da caixa de correio inativa quando o período de retenção do item excluído (para caixas de correio do Exchange) expira. O período de retenção da política de retenção do Office 365 pode ser configurado com base na data original em que um item de caixa de correio foi recebido ou criado, ou quando foi modificado pela última vez.  <br/> |
   
**Observação:** Se uma retenção de litígio já estiver colocada em uma caixa de correio ou se uma política de retenção do Office 365 já estiver aplicada a ela, tudo o que você precisará é excluir a conta de usuário do Office 365 correspondente para criar uma caixa de correio inativa. 
  
## <a name="managing-inactive-mailboxes"></a>Gerenciando caixas de correio inativas

Depois de fazer uma caixa de correio inativas, você pode executar várias tarefas de gerenciamento em caixas de correio inativas.
  
- **Alterar a duração de espera para uma caixa de correio inativa** Depois que uma caixa de correio é feita inativa, você pode alterar a duração da retenção da política de retenção de litígio ou Office 365 aplicada à caixa de correio inativa. Para obter os procedimentos passo a passo, consulte [alterar a duração da retenção para uma caixa de correio inativa no Office 365](change-the-hold-duration-for-an-inactive-mailbox.md).
    
- **Recuperar uma caixa de correio inativa** Se um antigo funcionário (ou um funcionário em uma licença de ausência) retorna à sua organização, ou se um novo funcionário é contratado para assumir as responsabilidades de trabalho do funcionário anterior, você pode recuperar o conteúdo da caixa de correio inativa. Ao recuperar uma caixa de correio inativa, a caixa de correio é convertida em uma nova caixa de correio, o conteúdo e estrutura de pastas da caixa de correio inativa são mantidos e a caixa de correio está vinculada a uma nova conta de usuário. Após sua recuperação, a caixa de correio inativa deixa de existir. Para obter os procedimentos passo a passo e informações sobre o que acontece quando você recupera uma caixa de correio inativa, consulte [recuperar uma caixa de correio inativa no Office 365](recover-an-inactive-mailbox.md).
    
- **Restaurar uma caixa de correio inativa** Se outro funcionário leva as responsabilidades de trabalho de um funcionário anterior, ou se outra pessoa precisa acessar o conteúdo da caixa de correio inativa, você poderá restaurar (ou direta) o conteúdo da caixa de correio inativa para uma caixa de correio existente. Quando você restaura uma caixa de correio inativa, o conteúdo é copiado para outra caixa de correio. A caixa de correio inativa é mantida e permanece uma caixa de correio inativa. A caixa de correio inativa ainda pode ser pesquisada usando as ferramentas de descoberta eletrônica, seu conteúdo possa ser restaurado para outra caixa de correio e pode ser recuperado ou excluído posteriormente. Para obter os procedimentos passo a passo, consulte [restaurar uma caixa de correio inativa no Office 365](restore-an-inactive-mailbox.md).
    
- **Excluir uma caixa de correio inativa** Quando não precisar mais reter o conteúdo de uma caixa de correio inativa, você pode excluí-lo permanentemente, removendo todas as isenções ou Office 365 políticas de retenção aplicadas à caixa de correio inativa. Se uma caixa de correio foi feita inativa mais de 30 dias atrás, ele será marcado para exclusão permanente depois de remover o bloqueio. Se a caixa de correio foi feita inativa nos últimos 30 dias, você pode torná-la ativa novamente após remover a política de retenção ou de espera. Para obter os procedimentos passo a passo, consulte [excluir uma caixa de correio inativa no Office 365](delete-an-inactive-mailbox.md).
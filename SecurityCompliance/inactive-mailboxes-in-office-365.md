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
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 1fbd74e8-7a60-4157-afe8-fe79f05d2038
description: Saiba mais sobre como reter o conteúdo de caixa de correio para funcionários antigos ao transformar a caixa de correio em uma caixa de correio inativa. Você pode fazer isso colocando a caixa de correio em retenção de litígio ou aplicando uma política de retenção do Office 365 à caixa de correio e, em seguida, removendo a conta do Office 365 correspondente.
ms.openlocfilehash: 67027ecd06771c0369e7f150c9eaa3e2030e2aab
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216681"
---
# <a name="overview-of-inactive-mailboxes-in-office-365"></a>Visão geral das caixas de correio inativas no Office 365

Sua organização pode precisar reter os emails antigos dos funcionários depois que eles saírem da organização. Dependendo dos requisitos de retenção da sua organização, talvez seja necessário manter o conteúdo de caixa de correio por alguns meses ou anos após o término do emprego, ou talvez você precise reter o conteúdo da caixa de correio indefinidamente. Independentemente de quanto tempo você precisa para reter o email, você pode criar caixas de correio inativas no Office 365 para manter a caixa de correio de antigos funcionários. 
  
## <a name="what-are-inactive-mailboxes"></a>Cite caixas de correio inativas.

Quando um funcionário deixa sua organização (ou fica em uma licença estendida de ausência), você pode remover a conta do Office 365. Os dados de caixa de correio do funcionário são mantidos por 30 dias após a conta ser removida. Durante esse período, você ainda pode recuperar os dados da caixa de correio, desfazendo a exclusão da conta. Após 30 dias, os dados são removidos permanentemente.
  
Mas se sua organização precisar reter o conteúdo de caixa de correio para ex-funcionários, você poderá transformar a caixa de correio em uma caixa de correio inativa, colocando a caixa de correio em retenção de litígio ou aplicando uma política de retenção &amp; do Office 365 à caixa de correio no Office 365 Security Centro de conformidade e, em seguida, removendo a conta correspondente do Office 365. O conteúdo de uma caixa de correio inativa é mantido pela duração da retenção de litígio na caixa de correio ou no período de retenção da política de retenção do Office 365 aplicada a ela antes da caixa de correio ser excluída. Você ainda pode recuperar a conta de usuário correspondente por um período de 30 dias. No enTanto, após 30 dias, a caixa de correio inativa é mantida no Office 365 até que a política de retenção ou bloqueio seja removida. 
  
**Importante:** Adiamos o prazo de 1º de julho de 2017 para criar novos bloqueios in-loco para tornar uma caixa de correio inativa. Mas, posteriormente neste ano ou no início do próximo ano, você não poderá criar novos bloqueios in-loco no Exchange Online. Nesse momento, apenas as reTenções de litígio e as políticas de retenção do Office 365 podem ser usadas para criar uma caixa de correio inativa. No enTanto, as caixas de correio inativas existentes que estão no bloqueio in-loco ainda terão suporte e você poderá continuar a gerenciar bloqueios in-loco em caixas de correio inativas. Isso inclui a alteração da duração de um bloqueio in-loco e a exclusão permanente de uma caixa de correio inativa, removendo o bloqueio in-loco. 
 
  
## <a name="inactive-mailboxes-and-office-365-retention-policies"></a>Caixas de correio inativas e políticas de retenção do Office 365

Além da retenção de litígio, o uso do novo recurso de política de retenção do Office 365 &amp; no centro de conformidade de segurança é outra maneira de tornar uma caixa de correio inativa. Para usar uma política de retenção para tornar uma caixa de correio inativa: 
  
- Ele deve ser aplicadas a caixas de correio do Exchange ou locais de Skype for Business (porque o conteúdo relacionado à Skype é armazenado na caixa de correio do usuário). 
    
- Ela deve ser configurado para reter o conteúdo ou reter e, em seguida, o conteúdo de excluído. Se uma política de retenção estiver configurada para excluir apenas o conteúdo, a política é aplicada a uma caixa de correio não ficar inativa, quando a caixa de correio é excluída.
    
- Pode ser baseado em consulta para que ele mantém somente os itens que correspondem a uma consulta de pesquisa. 
    
Para obter mais informações sobre como configurar as políticas de retenção Office 365, consulte [Visão geral das políticas de retenção no Office 365](retention-policies.md).
  
Se você usar uma política de retenção Office 365 para tornar uma caixa de correio inativa, Office 365 continuará processar a política de retenção na caixa de correio inativa. Isso significa que se a política de retenção é configurada para manter e excluir conteúdo, itens serão movidos para a pasta itens recuperáveis quando a duração da retenção expira e eventualmente removidos da caixa de correio inativa. Se a política de retenção Office 365 não estiver configurada para itens excluídos, itens que ainda não foram excluídos permanentemente pelo usuário (antes que a caixa de correio foi feita inativa) não serão movidos para a pasta itens recuperáveis e serão mantidos indefinidamente depois que a caixa de correio se tornar inativa. 
  
Você pode considerar a criação de uma política de retenção Office 365 especificamente para caixas de correio inativas. Aqui estão alguns motivos para fazer isso e coisas em mente.
  
- Você pode configurar a política de retenção para reter somente desde que o necessário para atender aos requisitos da sua organização para ex-funcionários de conteúdo de caixa de correio.
    
- É uma maneira fácil de identificar caixas de correio inativas porque só será aplicada a política de retenção a caixas de correio inativas.
    
- Você poderá identificar facilmente a política de retenção atribuída às caixas de correio inativas em sua organização. Isso facilitará a alteração das configurações de retenção (ou exclusão), se necessário. Isso também facilitará a exclusão permanente de uma caixa de correio inativa, pois você só poderá removê-la da política usando o &amp; centro de conformidade de segurança. Caso contrário, você terá que usar o PowerShell do Exchange Online para remover uma retenção de litígio de uma caixa de correio &amp; inativa ou usar o PowerShell do centro de conformidade de segurança para excluir uma caixa de correio inativa de uma política de retenção do Office 365 em toda a organização.
    
- Se você criar uma política de retenção Office 365 especificamente para caixas de correio inativas, você pode adicionar um máximo de 1.000 caixas de correio para a política. Se você for uma organização muito grande, você pode precisar criar mais de uma política de retenção Office 365 a ser usado para caixas de correio inativas.
  
## <a name="inactive-mailboxes-and-ediscovery-case-holds"></a>Caixas de correio inativas e isenções casos de eDiscovery

Se uma retenção associada a um caso de descoberta eletrônica no centro de &amp; conformidade de segurança for colocada em uma caixa de correio e a conta de caixa de correio ou do usuário do Office 365 for excluída, a caixa de correio se tornará uma caixa de correio inativa. No enTanto, não recomendamos o uso de bloqueios de ocorrência de descoberta eletrônica para tornar uma caixa de correio inativa. Isso ocorre porque os casos de descoberta eletrônica se destinam a casos específicos e associados a tempo relacionados a um problema legal. Em algum momento, um caso jurídico provavelmente será encerrado e as suspensões associadas ao caso serão removidas e o caso de descoberta eletrônica será fechado. Na verdade, se uma retenção colocada em uma caixa de correio inativa estiver associada a uma ocorrência de descoberta eletrônica e a retenção for liberada ou se a ocorrência de descoberta eletrônica estiver fechada (ou excluída), a caixa de correio inativa será excluída permanentemente. Além disso, você não pode criar um controle de descoberta eletrônica baseado em tempo. Isso significa que o conteúdo de uma caixa de correio inativa será retido para sempre ou até que a retenção seja removida e a caixa de correio inativa seja excluída. Portanto, recomendamos o uso de uma retenção de litígio ou de uma política de retenção do Office 365 para caixas de correio inativas.
  
Para obter mais informações sobre ocorrências de descoberta eletrônica e isenções, consulte [casos de descoberta &amp; eletrônica no centro de conformidade de segurança do Office 365](ediscovery-cases.md).
  
## <a name="inactive-mailboxes-and-office-365-labels"></a>Caixas de correio inativas e rótulos do Office 365

Rótulos em Office 365 ajudarão-lo classificar dados de email na sua organização para um governança e impor regras de retenção com base nessa classificação. Um rótulo pode ser aplicado a um item de email manualmente por usuários ou automaticamente por administradores e um item de email só pode ter um rótulo único atribuído a ele. Se um item de email único na caixa de correio de um usuário possui um rótulo atribuído a ela e a caixa de correio ou a conta do usuário Office 365 for excluída, a caixa de correio se tornará uma caixa de correio inativa. Semelhante ao isenções casos de eDiscovery, não recomendamos o uso de rótulos para tornar uma caixa de correio inativa. Em vez disso, recomendamos que você use um litígio ou uma política de retenção Office 365. Lembre-se de que no caso de rótulos, talvez não saiba o que um rótulo tiver sido aplicada a um item de email e inadvertidamente tornar uma caixa de correio inativa quando você exclui a conta do usuário. 
  
Para obter mais informações sobre rótulos, consulte [Visão geral dos rótulos no Office 365](labels.md).
  
## <a name="inactive-mailboxes-and-exchange-mrm-retention-policies"></a>Caixas de correio inativas e políticas de retenção de MRM do Exchange

Se uma política de retenção do Exchange (o recurso Gerenciamento de registros de mensagens ou MRM, no Exchange Online ) foi aplicada à caixa de correio quando ela foi feita inativa, quaisquer políticas de exclusão (que são configuradas com uma ação de retenção **Excluir** as marcas de retenção) continuarão a serem processados na caixa de correio inativa. Isso significa que os itens que estão marcados com uma política de exclusão serão movidos para a pasta itens recuperáveis quando o período de retenção expira. Os itens são removidos da caixa de correio inativa quando a duração da retenção expira. Se um período de retenção não for especificado para a caixa de correio inativa, itens na pasta recuperar itens serão mantidos indefinidamente. 
  
Por outro lado, quaisquer políticas de arquivamento (que são marcas de retenção configuradas com uma ação de retenção **MoveToArchive** ) que estão incluídas na política de retenção atribuída a uma caixa de correio inativa serão ignoradas. Isso significa que itens em uma caixa de correio inativa que estão marcados com uma política de arquivamento permanecerá na caixa de correio principal quando o período de retenção expira. Elas não serão movidas para a caixa de correio de arquivo morto ou para a pasta itens recuperáveis na caixa de correio de arquivo morto. Eles serão mantidos indefinidamente. 
  
## <a name="creating-an-inactive-mailbox"></a>Criando uma caixa de correio inativa

Para tornar uma caixa de correio inativa, ela deve ser atribuída a uma licença do Exchange Online (plano 2) para que uma retenção de litígio ou uma política de retenção do Office 365 possa ser aplicada à caixa de correio antes de ser excluída. Depois que a caixa de correio for excluída, a licença do Exchange Online associada a ela estará disponível para ser atribuída a um novo usuário. As caixas de correio inativas não exigem licenças contínuas.
  
A tabela a seguir resume o processo de criação de uma caixa de correio inativa para diferentes cenários de retenção. Para obter mais informações, consulte [gerenciar caixas de correio inativas no Office 365](create-and-manage-inactive-mailboxes.md).
  
|**Para...**|**Faça isso …**|**Resultado**|
|:-----|:-----|:-----|
|Manter o conteúdo de caixa de correio indefinidamente depois que um funcionário deixa a organização  <br/> | Colocar a caixa de correio em retenção de litígio ou aplicar uma política de retenção Office 365 à caixa de correio.  <br/>  Não especificar um período de retenção para retenção de litígio ou não configurar a política de retenção Office 365 para excluir itens; Como alternativa, você pode usar uma política de retenção que mantém os itens indefinidamente.  <br/>  Remova a conta do usuário Office 365.  <br/> |Todo o conteúdo da caixa de correio inativa, incluindo itens na pasta itens recuperáveis, é retido indefinidamente.  <br/> |
|Manter o conteúdo de caixa de correio por um período específico após um funcionário deixa a organização e exclua-  <br/> | Aplicar uma política de retenção do Office 365 à caixa de correio.  <br/>  Configure a política de retenção para reter e, em seguida, excluir itens quando o período de retenção expirar.  <br/>  Remova a conta do usuário Office 365.  <br/> |Quando o período de retenção de um item de caixa de correio expira, o item é movido para a pasta itens recuperáveis e, em seguida, é excluído permanentemente (removido) da caixa de correio inativa quando o período de retenção do item excluído (para caixas de correio do Exchange) expira. O período de retenção da política de retenção do Office 365 pode ser configurado com base na data original em que um item de caixa de correio foi recebido ou criado, ou quando foi modificado pela última vez.  <br/> |
   
**Observação:** Se uma retenção de litígio já estiver colocada em uma caixa de correio ou se uma política de retenção do Office 365 já estiver aplicada a ela, tudo o que você precisará é excluir a conta de usuário do Office 365 correspondente para criar uma caixa de correio inativa. 
  
## <a name="managing-inactive-mailboxes"></a>Gerenciando caixas de correio inativas

Depois de fazer uma caixa de correio inativas, você pode executar várias tarefas de gerenciamento em caixas de correio inativas.
  
- **Alterar a duração da retenção de uma caixa de correio inativa** Depois que uma caixa de correio for desativada, você poderá alterar a duração da retenção de litígio ou a política de retenção do Office 365 aplicada à caixa de correio inativa. Para obter os procedimentos passo a passo, consulte [alterar a duração da retenção para uma caixa de correio inativa no Office 365](change-the-hold-duration-for-an-inactive-mailbox.md).
    
- **Recuperar uma caixa de correio inativa** Se um antigo funcionário (ou um funcionário em uma licença de ausência) retornar à sua organização, ou se um novo funcionário for contratado para tomar as responsabilidades do cargo do funcionário anterior, você poderá recuperar o conteúdo da caixa de correio inativa. Ao recuperar uma caixa de correio inativa, a caixa de correio é convertida em uma nova caixa de correio, o conteúdo e a estrutura de pastas da caixa de correio inativa são mantidos e a caixa de correio é vinculada a uma nova conta de usuário. Após a recuperação, a caixa de correio inativa não existe mais. Para obter os procedimentos passo a passo e informações sobre o que acontece quando você recupera uma caixa de correio inativa, consulte [recuperar uma caixa de correio inativa no Office 365](recover-an-inactive-mailbox.md).
    
- **Restaurar uma caixa de correio inativa** Se outro funcionário tomar as responsabilidades de trabalho de um funcionário antigo ou se outra pessoa precisar acessar o conteúdo da caixa de correio inativa, você poderá restaurar (ou mesclar) o conteúdo da caixa de correio inativa para uma caixa de correio existente. Quando você restaura uma caixa de correio inativa, o conteúdo é copiado para outra caixa de correio. A caixa de correio inativa é mantida e permanece uma caixa de correio inativa. A caixa de correio inativa ainda pode ser pesquisada usando ferramentas de descoberta eletrônica, seu conteúdo pode ser restaurado para outra caixa de correio e pode ser recuperado ou excluído posteriormente. Para obter os procedimentos passo a passo, consulte [restaurar uma caixa de correio inativa no Office 365](restore-an-inactive-mailbox.md).
    
- **Excluir uma caixa de correio inativa** Quando você não precisa mais reter o conteúdo de uma caixa de correio inativa, é possível excluí-la permanentemente removendo todas as políticas de retenção ou de retenções do Office 365 aplicadas à caixa de correio inativa. Se uma caixa de correio foi feita inativa há mais de 30 dias, ela será marcada para exclusão permanente depois que você remover a retenção. Se a caixa de correio foi feita inativa nos últimos 30 dias, você poderá torná-la ativa novamente após remover a política de retenção ou bloqueio. Para obter os procedimentos passo a passo, consulte [excluir uma caixa de correio inativa no Office 365](delete-an-inactive-mailbox.md).
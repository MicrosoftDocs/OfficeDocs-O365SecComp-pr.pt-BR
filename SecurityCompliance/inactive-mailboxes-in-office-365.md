---
title: Visão geral das caixas de correio inativas no Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/1/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 1fbd74e8-7a60-4157-afe8-fe79f05d2038
description: Aprenda sobre retenção de conteúdo de caixa de correio para ex-funcionários, desativando a caixa de correio em uma caixa de correio inativa. Você pode fazer isso pelo colocação de caixa de correio em retenção de litígio ou a aplicação de uma política de retenção do Office 365 à caixa de correio e, em seguida, removendo a conta do Office 365 correspondente.
ms.openlocfilehash: 5b421e32df99a10d13528fe7a75e6a0e8fb54fdc
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524126"
---
# <a name="overview-of-inactive-mailboxes-in-office-365"></a>Visão geral das caixas de correio inativas no Office 365

Sua organização, talvez seja necessário reter email antigos empregados depois que deixam a organização. Dependendo dos requisitos de retenção da sua organização, você pode precisar manter o conteúdo de caixa de correio para alguns meses ou anos após o término de emprego ou você pode precisar manter o conteúdo de caixa de correio indefinidamente. Independentemente de quanto tempo você precisar manter o email, você pode criar caixas de correio inativas no Office 365 para manter a caixa de correio de funcionários anteriores. 
  
## <a name="what-are-inactive-mailboxes"></a>Cite caixas de correio inativas.

Quando um funcionário deixa sua organização (ou fica em uma licença estendida), você pode remover a conta do Office 365. Dados de caixa de correio do funcionário são mantidos por 30 dias depois que a conta for removida. Durante esse período, você ainda poderá recuperar os dados de caixa de correio por Cancelando a exclusão da conta. Após 30 dias, os dados são removidos permanentemente.
  
Mas se sua organização precisar manter o conteúdo de caixa de correio para ex-funcionários, você pode transformar a caixa de correio em uma caixa de correio inativa colocação de caixa de correio em retenção de litígio ou aplicando uma política de retenção do Office 365 à caixa de correio no Office 365 Security &amp; Centro de conformidade e, em seguida, removendo a conta correspondente do Office 365. O conteúdo de uma caixa de correio inativa é retido para a duração da retenção de litígio colocado na caixa de correio ou o período de retenção da política de retenção Office 365 aplicada a ele antes que a caixa de correio foi excluída. Você ainda pode recuperar a conta de usuário correspondente por um período de 30 dias. No entanto, depois de 30 dias, a caixa de correio inativa é mantida no Office 365 até que a política de retenção ou retenção seja removida. 
  
**Importante:** Podemos foi adiada o prazo 1 de julho de 2017 de criação de novos retenções locais para tornar uma caixa de correio inativa. Mas este ano ou próximo ano inicial, você não poderá criar novos retenções locais no Exchange Online. Nesse momento, políticas de retenção apenas contém de litígio e o Office 365 podem ser usadas para criar uma caixa de correio inativa. No entanto, existentes caixas de correio inativas que estão em In-loco bloqueio ainda serão suportadas e você pode continuar a gerenciar as isenções de In-loco em caixas de correio inativas. Isso inclui alterando a duração de um bloqueio In-loco e excluir permanentemente uma caixa de correio inativa, removendo o bloqueio In-loco. 
 
  
## <a name="inactive-mailboxes-and-office-365-retention-policies"></a>Caixas de correio inativas e políticas de retenção do Office 365

Além de litígio, usando o novo recurso de política de retenção do Office 365 na segurança &amp; Centro de conformidade é outra maneira de tornar uma caixa de correio inativa. Usar uma política de retenção para tornar uma caixa de correio inativa: 
  
- Ele deve ser aplicadas a caixas de correio do Exchange ou locais de Skype for Business (porque o conteúdo relacionado à Skype é armazenado na caixa de correio do usuário). 
    
- Ela deve ser configurado para reter o conteúdo ou reter e, em seguida, o conteúdo de excluído. Se uma política de retenção estiver configurada para excluir apenas o conteúdo, a política é aplicada a uma caixa de correio não ficar inativa, quando a caixa de correio é excluída.
    
- Pode ser baseado em consulta para que ele mantém somente os itens que correspondem a uma consulta de pesquisa. 
    
Para obter mais informações sobre como configurar as políticas de retenção Office 365, consulte [Visão geral das políticas de retenção no Office 365](retention-policies.md).
  
Se você usar uma política de retenção Office 365 para tornar uma caixa de correio inativa, Office 365 continuará processar a política de retenção na caixa de correio inativa. Isso significa que se a política de retenção é configurada para manter e excluir conteúdo, itens serão movidos para a pasta itens recuperáveis quando a duração da retenção expira e eventualmente removidos da caixa de correio inativa. Se a política de retenção Office 365 não estiver configurada para itens excluídos, itens que ainda não foram excluídos permanentemente pelo usuário (antes que a caixa de correio foi feita inativa) não serão movidos para a pasta itens recuperáveis e serão mantidos indefinidamente depois que a caixa de correio se tornar inativa. 
  
Você pode considerar a criação de uma política de retenção Office 365 especificamente para caixas de correio inativas. Aqui estão alguns motivos para fazer isso e coisas em mente.
  
- Você pode configurar a política de retenção para reter somente desde que o necessário para atender aos requisitos da sua organização para ex-funcionários de conteúdo de caixa de correio.
    
- É uma maneira fácil de identificar caixas de correio inativas porque só será aplicada a política de retenção a caixas de correio inativas.
    
- Você será capaz de identificar facilmente a política de retenção que é atribuída a caixas de correio inativas em sua organização. Isso irá facilitar alterar as configurações de retenção (ou exclusão), se necessário. Ele também facilitará excluir permanentemente uma caixa de correio inativa porque você pode apenas removê-lo da diretiva usando a segurança &amp; Centro de conformidade. Caso contrário, você precisará usar o PowerShell do Exchange Online para remover um litígio de uma caixa de correio inativa ou usar segurança &amp; PowerShell do Centro de conformidade para excluir uma caixa de correio inativa de uma política de retenção do Office 365 de toda a organização.
    
- Se você criar uma política de retenção Office 365 especificamente para caixas de correio inativas, você pode adicionar um máximo de 1.000 caixas de correio para a política. Se você for uma organização muito grande, você pode precisar criar mais de uma política de retenção Office 365 a ser usado para caixas de correio inativas.
  
## <a name="inactive-mailboxes-and-ediscovery-case-holds"></a>Caixas de correio inativas e isenções casos de eDiscovery

Se uma isenção que está associado a um caso de eDiscovery na segurança &amp; Centro de conformidade é colocado em uma caixa de correio e, em seguida, a caixa de correio ou a conta de usuário Office 365 é excluída, a caixa de correio se tornará uma caixa de correio inativa. No entanto, não recomendamos usar o caso de descoberta eletrônica retenções para tornar uma caixa de correio inativa. Isso ocorre porque os casos de eDiscovery servem para casos específicos e de ligação de tempo relacionados a uma questão legal. Em algum momento, um caso jurídico provavelmente será finalizado e os bloqueios associados à ocorrência serão removidos e o caso de descoberta eletrônica será fechado. Na verdade, se uma isenção que é colocada em uma caixa de correio inativa é associada a um caso de descoberta eletrônica e, em seguida, a suspensão seja removida ou o eDiscovery caso seja fechado (ou excluído), a caixa de correio inativa será excluída permanentemente. Além disso, é possível criar uma isenção baseadas em tempo de eDiscovery. Isso acontece significa conteúdo em uma caixa de correio inativa será mantido indefinidamente ou até que a suspensão seja removida e a caixa de correio inativa é excluída. Portanto, recomendamos o uso de um litígio ou uma política de retenção do Office 365 para caixas de correio inativas.
  
Para obter mais informações sobre os casos de eDiscovery e retenções, consulte [casos de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade](ediscovery-cases.md).
  
## <a name="inactive-mailboxes-and-office-365-labels"></a>Caixas de correio inativas e rótulos do Office 365

Rótulos em Office 365 ajudarão-lo classificar dados de email na sua organização para um governança e impor regras de retenção com base nessa classificação. Um rótulo pode ser aplicado a um item de email manualmente por usuários ou automaticamente por administradores e um item de email só pode ter um rótulo único atribuído a ele. Se um item de email único na caixa de correio de um usuário possui um rótulo atribuído a ela e a caixa de correio ou a conta do usuário Office 365 for excluída, a caixa de correio se tornará uma caixa de correio inativa. Semelhante ao isenções casos de eDiscovery, não recomendamos o uso de rótulos para tornar uma caixa de correio inativa. Em vez disso, recomendamos que você use um litígio ou uma política de retenção Office 365. Lembre-se de que no caso de rótulos, talvez não saiba o que um rótulo tiver sido aplicada a um item de email e inadvertidamente tornar uma caixa de correio inativa quando você exclui a conta do usuário. 
  
Para obter mais informações sobre rótulos, consulte [Visão geral dos rótulos no Office 365](labels.md).
  
## <a name="inactive-mailboxes-and-exchange-mrm-retention-policies"></a>Caixas de correio inativas e políticas de retenção de MRM do Exchange

Se uma política de retenção do Exchange (o recurso Gerenciamento de registros de mensagens ou MRM, no Exchange Online ) foi aplicada à caixa de correio quando ela foi feita inativa, quaisquer políticas de exclusão (que são configuradas com uma ação de retenção **Excluir** as marcas de retenção) continuarão a serem processados na caixa de correio inativa. Isso significa que os itens que estão marcados com uma política de exclusão serão movidos para a pasta itens recuperáveis quando o período de retenção expira. Os itens são removidos da caixa de correio inativa quando a duração da retenção expira. Se um período de retenção não for especificado para a caixa de correio inativa, itens na pasta recuperar itens serão mantidos indefinidamente. 
  
Por outro lado, quaisquer políticas de arquivamento (que são marcas de retenção configuradas com uma ação de retenção **MoveToArchive** ) que estão incluídas na política de retenção atribuída a uma caixa de correio inativa serão ignoradas. Isso significa que itens em uma caixa de correio inativa que estão marcados com uma política de arquivamento permanecerá na caixa de correio principal quando o período de retenção expira. Elas não serão movidas para a caixa de correio de arquivo morto ou para a pasta itens recuperáveis na caixa de correio de arquivo morto. Eles serão mantidos indefinidamente. 
  
## <a name="creating-an-inactive-mailbox"></a>Criando uma caixa de correio inativa

Para tornar uma caixa de correio inativas, ele deve ser atribuído uma licença do Exchange Online (plano 2) para que uma política de retenção de litígio ou do Office 365 pode ser aplicada à caixa de correio antes que ele seja excluído. Depois que a caixa de correio é excluída, a licença Exchange Online que tiver sido associada ele será disponível para atribuir a um novo usuário. Caixas de correio inativas não exigem licenças em andamento.
  
A tabela a seguir resume o processo para tornar uma caixa de correio inativa para cenários de retenção diferente. Para obter mais informações, consulte [gerenciar caixas de correio inativas no Office 365](create-and-manage-inactive-mailboxes.md).
  
|**Para...**|**Faça isso …**|**Resultado**|
|:-----|:-----|:-----|
|Manter o conteúdo de caixa de correio indefinidamente depois que um funcionário deixa a organização  <br/> | Colocar a caixa de correio em retenção de litígio ou aplicar uma política de retenção Office 365 à caixa de correio.  <br/>  Não especificar um período de retenção para retenção de litígio ou não configurar a política de retenção Office 365 para excluir itens; Como alternativa, você pode usar uma política de retenção que mantém os itens indefinidamente.  <br/>  Remova a conta do usuário Office 365.  <br/> |A caixa de correio inativa, incluindo os itens na pasta itens recuperáveis, todo o conteúdo é mantido indefinidamente.  <br/> |
|Manter o conteúdo de caixa de correio por um período específico após um funcionário deixa a organização e exclua-  <br/> | Aplica uma política de retenção do Office 365 à caixa de correio.  <br/>  Configure a política de retenção para manter e excluir itens quando o período de retenção expira.  <br/>  Remova a conta do usuário Office 365.  <br/> |Quando o período de retenção para um item de caixa de correio expira, o item é movido para a pasta itens recuperáveis e, em seguida, ele é excluído permanentemente (descartados) da caixa de correio inativa quando expira o período de retenção de item excluído (para caixas de correio do Exchange). O período de retenção da política de retenção do Office 365 pode ser configurado com base na data original um item de caixa de correio foi recebido ou criado ou quando ele foi modificado pela última vez.  <br/> |
   
**Observação:** Se um litígio já é colocada em uma caixa de correio, ou se uma política de retenção do Office 365 já for aplicada a ela, tudo o que você deve fazer é excluir a conta de usuário correspondente do Office 365 para criar uma caixa de correio inativa. 
  
## <a name="managing-inactive-mailboxes"></a>Gerenciando caixas de correio inativas

Depois de fazer uma caixa de correio inativas, você pode executar várias tarefas de gerenciamento em caixas de correio inativas.
  
- **Alterar a duração de espera para uma caixa de correio inativa** Depois que uma caixa de correio é feita inativa, você pode alterar a duração da retenção da política de retenção de litígio ou do Office 365 aplicada à caixa de correio inativa. Para obter procedimentos passo a passo, consulte [alterar a duração de espera para uma caixa de correio inativa no Office 365](change-the-hold-duration-for-an-inactive-mailbox.md).
    
- **Recuperar uma caixa de correio inativa** Se um antigo funcionário (ou um funcionário em uma licença de ausência) retorna à sua organização, ou se um novo funcionário é contratado para assumir as responsabilidades de trabalho do funcionário anterior, você pode recuperar o conteúdo da caixa de correio inativa. Ao recuperar uma caixa de correio inativa, a caixa de correio é convertida em uma nova caixa de correio, o conteúdo e estrutura de pastas da caixa de correio inativa são mantidos e a caixa de correio está vinculada a uma nova conta de usuário. Depois que ele seja recuperado, a caixa de correio inativa não existe mais. Para obter informações sobre o que acontece quando você recuperar uma caixa de correio inativa e procedimentos passo a passo, consulte [recuperar uma caixa de correio inativa no Office 365](recover-an-inactive-mailbox.md).
    
- **Restaurar uma caixa de correio inativa** Se outro funcionário leva as responsabilidades de trabalho de um funcionário anterior, ou se outra pessoa precisa acessar o conteúdo da caixa de correio inativa, você pode restaurar (ou mesclar) o conteúdo da caixa de correio inativa para uma caixa de correio existente. Quando você restaura uma caixa de correio inativa, o conteúdo é copiado para outra caixa de correio. A caixa de correio inativa é mantida e permanece uma caixa de correio inativa. A caixa de correio inativa ainda pode ser pesquisada usando as ferramentas de descoberta eletrônica, seu conteúdo possa ser restaurado para outra caixa de correio e pode ser recuperado ou excluído posteriormente. Para obter procedimentos passo a passo, consulte [restaurar uma caixa de correio inativa no Office 365](restore-an-inactive-mailbox.md).
    
- **Excluir uma caixa de correio inativa** Quando não precisar mais reter o conteúdo de uma caixa de correio inativa, você pode excluí-lo permanentemente, removendo todas as isenções ou Office 365 políticas de retenção aplicadas à caixa de correio inativa. Se uma caixa de correio foi feita inativa mais de 30 dias atrás, ele será marcado para exclusão permanente depois de remover o bloqueio. Se a caixa de correio foi feita inativa nos últimos 30 dias, você pode torná-la ativa novamente após remover a política de retenção ou de espera. Para obter procedimentos passo a passo, consulte [Excluir uma caixa de correio inativa no Office 365](delete-an-inactive-mailbox.md).
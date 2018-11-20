---
title: Criar alertas de atividade no Office 365 Security &amp; Centro de conformidade
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 11/7/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- BCS160
- MET150
ms.assetid: 72bbad69-035b-4d33-b8f4-549a2743e97d
description: Adicione e gerencie alertas de atividade na segurança &amp; Centro de conformidade para que o Office 365 enviará as notificações de email quando os usuários realizam atividades específicas no Office 365.
ms.openlocfilehash: 2a579e850d16b730a777ce6c4e5c0446305a027d
ms.sourcegitcommit: 3a376619dbae472495c29da7c061f5c5faeeaddb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/12/2018
ms.locfileid: "26282735"
---
# <a name="create-activity-alerts-in-the-office-365-security-amp-compliance-center"></a>Criar alertas de atividade no Office 365 Security &amp; Centro de conformidade

Você pode criar um alerta de atividade que lhe enviará uma notificação de email quando os usuários realizam atividades específicas no Office 365. Alertas de atividade são semelhantes às procurando eventos no log de auditoria do Office 365, exceto que você vai ser enviada uma mensagem de email quando um evento para uma atividade que você criou um alerta para acontece. 
  
 **Por que usar alertas de atividade em vez de pesquisar o log de auditoria?** Pode haver certos tipos de atividade ou atividade executadas pelos usuários específicos que você realmente deseja saber sobre. Em vez de lembrar pesquisar o log de auditoria para essas atividades, você pode usar os alertas de atividade ter o Office 365 enviar uma mensagem de email quando os usuários realizam essas atividades. Por exemplo, você pode criar um alerta de atividade para ser notificado quando um usuário exclui arquivos no SharePoint ou você pode criar um alerta para notificá-lo quando um usuário exclui permanentemente mensagens de suas caixas de correio. A notificação de email enviada a você inclui informações sobre qual atividade foi executada e o usuário que executou a ele. 

> [!NOTE]
> Recomendamos que você começar a usar políticas de alerta no Centro de conformidade & segurança em vez de criar novos alertas de atividade. Políticas de alerta fornecem funcionalidade de adição como a capacidade de criar uma política de alerta que dispara um alerta quando qualquer usuário realiza uma atividade especificada e exibindo os alertas na página **Exibir alertas** no Centro de conformidade & segurança. Para obter mais informações, consulte [políticas de segurança do Office 365 de alerta &amp; Centro de conformidade](alert-policies.md).
  
## <a name="before-you-begin"></a>Antes de começar

- Você deve ser atribuído à função de configuração da organização na segurança &amp; Centro de conformidade para gerenciar alertas de atividade. Por padrão, essa função é atribuída aos grupos de função de administrador de conformidade e gerenciamento da organização. Para obter mais informações sobre como adicionar membros a grupos de funções, consulte [Conceder aos usuários acesso para a segurança do Office 365 &amp; Centro de conformidade](grant-access-to-the-security-and-compliance-center.md).
    
- Você (ou outro administrador) primeiro deve ativar o log de auditoria para sua organização antes de começar a usar alertas de atividade. Para fazer isso, basta clicar em **Iniciar gravação de usuário e a atividade de admin** na página **alertas de atividade** . (Se você não vir este link, auditoria já foi ativado para sua organização.) Você também pode ativar auditoria na página de **pesquisa de log de auditoria** na segurança &amp; Centro de conformidade (vá para **pesquisa &amp; investigação** \> **pesquisa de log de auditoria**). Você só precisa fazer isso vez para sua organização.
  
- Você pode criar alertas para as mesmas atividades que você pode pesquisar no log de auditoria do Office 365. Ver as [informações mais](#more-information) seção para obter uma lista de cenários comuns (e a atividade específica para monitorar) que você pode criar alertas para. 
    
- Você pode usar a página **alertas de atividade** na segurança &amp; Centro de conformidade para criar alertas somente para atividades realizadas pelos usuários que estão listados no catálogo de endereços da sua organização. Você não pode usar esta página para criar alertas para atividade realizada por usuários externos que não estão listados no catálogo de endereços. 
    
## <a name="create-an-activity-alert"></a>Criar um alerta de atividade

1. Acesse [https://protection.office.com/#/managealerts](https://protection.office.com/#/managealerts).
    
2. Entre no Office 365 usando a sua conta corporativa ou de estudante.
    
3. Na página **alertas de atividade** , clique em ![ícone Adicionar](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **New**.

   A página de submenu para criar um alerta de atividade é exibida.

    
    ![Criar um alerta de atividade](media/53888bd5-9fa2-4398-8ccc-1a9dc72517ac.png)
  
4. Preencha os campos a seguintes para criar um alerta de atividade:
    
    r. **nome** - digite um nome para o alerta. Nomes de alertas devem ser exclusivos dentro da sua organização.
    
    b. **Descrição** (opcional) - descrevem alerta, as atividades e os usuários que está sendo rastreados, e os usuários que as notificações de email são enviados para. Descrições fornecem uma maneira rápida e fácil para descrever a finalidade do alerta para outros administradores.
    
    c. **tipo de alerta** - Verifique se a opção **personalizado** está selecionada. 

    d. **Enviar este alerta quando** - Click **Enviar este alerta quando** e defina esses dois campos:
    
    - **Atividades** - clique na lista suspensa lista para exibir as atividades que você pode criar um alerta para. Esta é a mesma lista de atividades que é exibida quando você pesquisar o log de auditoria do Office 365. Você pode selecionar uma ou mais atividades específicas ou você pode clicar no nome do grupo de atividade para selecionar todas as atividades no grupo. Para obter uma descrição dessas atividades, consulte a seção "Auditadas atividades" na [pesquisa da auditoria, faça logon no Centro de conformidade & segurança do Office 365](search-the-audit-log-in-security-and-compliance.md#audited-activities). Quando um usuário realiza qualquer uma das atividades que você tenha adicionado ao alerta, um email de notificação é enviada. 
    
     - **Os usuários** - clique nesta caixa e selecione um ou mais usuários. Se os usuários nesta caixa executam as atividades que você adicionou à caixa de **atividades** , um alerta será enviado. Deixe a caixa de **usuários** em branco para enviar um alerta quando qualquer usuário em sua organização executa as atividades especificadas no alerta. 

    e. **enviar esse alerta para** - clique em **enviar esse alerta**e, em seguida, clique na caixa de **destinatários** e digite um nome para adicionar um usuários que receberão uma notificação de email quando um usuário (especificado na caixa **usuários** ) realiza uma atividade (especificado no Caixa de **atividades** ). Observe que, por padrão, você é adicionado à lista de destinatários. Você pode remover o seu nome dessa lista.
    
5. Clique em **Salvar** para criar o alerta. 
    
    O novo alerta é exibido na lista na página **alertas de atividade** . 
    
    ![É exibida uma lista de alertas na página de atividade de alertas na segurança &amp; Centro de conformidade](media/02b774f2-1719-41de-bbc9-5e5b7576f335.png)
  
    O status do alerta é definido para **ativado**. Observe que os destinatários que serão recebeu uma notificação de email quando um alerta é enviado também são listados. 
  
## <a name="turn-off-an-activity-alert"></a>Desativar um alerta de atividade

Você pode desativar um alerta de atividade para que uma notificação de e-mail não será enviada. Após desativar o alerta de atividade, ele ainda é exibido na lista de alertas de atividade para sua organização e você ainda poderá exibir suas propriedades.
  
1. Acesse [https://protection.office.com/#/managealerts](https://protection.office.com/#/managealerts).
    
2. Entre no Office 365 usando a sua conta corporativa ou de estudante.
    
3. Na lista de alertas de atividade para sua organização, clique no alerta que você deseja desativar.
    
4. Na página **Editar alerta** , clique o switch de alternância **em** para alterar o status para **Desativar**e, em seguida, clique em **Salvar**.
    
    O status do alerta nas páginas de **alertas de atividade** estiver definido como **desativado**. 
    
Para ativar um alerta de atividade, basta Repita essas etapas e clique no switch de alternância **desativado** para alterar o status para **ativado**.
  
## <a name="more-information"></a>Mais informações

- Aqui está um exemplo do email de notificação é enviada para os usuários que são especificados no Sent nesse alerta ao campo (e listados em **destinatários** na página **alertas de atividade** ) na segurança &amp; Centro de conformidade. 
    
    ![Exemplo de uma notificação de email enviada para um alerta de atividade](media/a5f91611-fae6-4fe9-82f5-58521a2e2541.png)
  
- São do Eis aqui algumas atividades comuns do documento e de email que você pode criar uma atividade de alertas para. As tabelas descreve a atividade, o nome da atividade para criar um alerta para e o nome do grupo de atividades que a atividade está listada na lista suspensa de **atividades** . Para ver uma lista completa das atividades que você pode criar alertas de atividade para, consulte a seção "Auditadas atividades" na [pesquisa da auditoria, faça logon no Centro de conformidade & segurança do Office 365](search-the-audit-log-in-security-and-compliance.md#audited-activities).
    
    > [!TIP]
    > Talvez você queira criar um alerta de atividade para apenas uma atividade que é executada por qualquer usuário. Ou talvez você queira criar um alerta de atividade que controlar várias atividades realizadas por um ou outros contatos usuários. 
  
    A tabela a seguir lista algumas atividades comuns relacionadas a documentos no SharePoint ou OneDrive for Business.
    
    |**Quando um usuário faz isso …**|**Criar um alerta para esta atividade**|**Grupo de atividades**|
    |:-----|:-----|:-----|
    |Exibe um documento em um site.  <br/> |Arquivos acessados  <br/> |Atividades de arquivo e pasta  <br/> |
    |Edita ou altera um documento.  <br/> |Arquivo modificado  <br/> |Atividades de arquivo e pasta  <br/> |
    |Compartilhar um documento com um usuário fora da sua organização.  <br/> |Compartilhar o arquivo, pasta ou site  <br/> E  <br/> Criado o convite de compartilhamento  <br/> Para obter mais informações, consulte [Use compartilhamento auditorias no log de auditoria do Office 365](use-sharing-auditing.md).  <br/> |Atividades de solicitação de compartilhamento e acesso  <br/> |
    |Carrega ou descarrega um documento.  <br/> |Arquivo carregado  <br/> E/ou  <br/> Arquivo baixado  <br/> |Atividades de arquivo e pasta  <br/> |
    |Altera as permissões de acesso a um site.  <br/> |Permissões de site modificada  <br/> |Atividades de administração de site  <br/> |

    A tabela a seguir lista algumas atividades comuns relacionados a email no Exchange Online.

    |**Quando um usuário faz isso …**|**Criar um alerta para esta atividade**|**Grupo de atividades**|
    |:-----|:-----|:-----|
    |Permanentemente exclui (limpezas) um email mensagem da sua caixa de correio.  <br/> |Mensagens limpas de caixa de correio  <br/> | Atividades de caixa de correio do Exchange  <br/> |
    |Envia uma mensagem de email de uma caixa de correio compartilhada.  <br/> |Enviada usando permissões Enviar como de mensagem  <br/> E  <br/> Enviada usando permissões Enviar em nome de mensagem  <br/> | Atividades de caixa de correio do Exchange  <br/> |
   
- Você também pode usar os cmdlets **New-ActivityAlert** e **Set-ActivityAlert** na segurança &amp; PowerShell do Centro de conformidade para criar e editar alertas de atividade. Se você usar esses cmdlets para criar ou editar alertas de atividade, mantenha as seguintes coisas em mente: 
    
  - Se você usar um cmdlet para adicionar uma atividade para o alerta de que não está listado na lista suspensa de **atividades** , uma mensagem é exibida na página de propriedades para o alerta que diz, "Este alerta possui operações personalizadas que não está listadas no seletor de". 
    
  - Um bom motivo para usar os cmdlets para criar ou editar um alerta de atividade é para enviar notificações por email a alguém de fora da sua organização. Este usuário externo será listado na lista de destinatários para o alerta. Mas se você remover este usuário externo no alerta, que o usuário não pode ser adicionado ao alerta novamente usando a página **Editar alerta** na segurança &amp; Centro de conformidade. Você vai precisar adicione novamente o usuário externo usando o cmdlet **Set-ActivityAlert** ou use o cmdlet **New-ActivityAlert** para adicionar o usuário externo mesmo (ou diferente) para um novo alerta. 
    
  


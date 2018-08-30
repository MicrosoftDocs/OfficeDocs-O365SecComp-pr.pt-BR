---
title: Perguntas Frequentes sobre a Quarentena
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/16/2017
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c440b2ac-cafa-4be5-ba4c-14278a7990ae
description: Este tópico fornece as perguntas frequentes e respectivas respostas sobre a quarentena hospedada.
ms.openlocfilehash: cc8a05b575e17dbc71d4b9e214cb29a4cafe8b6b
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23003190"
---
# <a name="quarantine-faq"></a>Perguntas Frequentes sobre a Quarentena

Este tópico fornece as perguntas frequentes e respectivas respostas sobre a quarentena hospedada. As respostas se aplicam aos clientes do Microsoft Exchange Online e do Proteção do Exchange Online.
  
 **P. como gerenciar mensagens em quarentena de malware em quarentena?**
  
Você precisa usar a segurança &amp; Centro de conformidade para exibir e trabalhar com mensagens enviadas para quarentena porque eles contêm malware. Para obter mais informações, consulte [mensagens de email de quarentena no Office 365](https://support.office.com/article/Quarantine-email-messages-in-Office-365-4c234874-015e-4768-8495-98fcccfc639b).
  
 **P. Como configuro o serviço para enviar mensagens de spam para a quarentena?**
  
R. por padrão, o conteúdo filtrado mensagens são enviadas para a pasta de lixo eletrônico de destinatários. No entanto, os administradores podem configurar políticas de filtro de conteúdo para enviar mensagens em quarentena de spam para a quarentena em vez disso. Para obter mais informações sobre as ações diferentes que podem ser executadas em mensagens de conteúdo filtrado, consulte [configurar suas políticas de filtro de spam](configure-your-spam-filter-policies.md).
  
 **P. O serviço tem administrador e gerenciamento de usuário final de mensagens de spam em quarentena?**
  
R. Como administrador, você pode pesquisar e exibir detalhes sobre todas as mensagens de email em quarentena no Centro de Administração do Exchange (EAC). Depois de localizar a mensagem, você pode liberá-la para usuários específicos e, opcionalmente, relatá-la como falso positivo (não é lixo eletrônico) à Equipe de Análise de Spam da Microsoft. Para obter mais informações, consulte [Localizar e liberar mensagens em quarentena como um administrador](find-and-release-quarantined-messages-as-an-administrator.md).
  
Como usuário final, você pode gerenciar suas próprias mensagens em quarentena de spam via: 
  
- A interface de usuário de quarentena de spam. Para obter mais informações, consulte [Find and Release Quarantined Messages (End Users)](http://technet.microsoft.com/library/e439b560-827a-4807-abd3-6b861c1ff786.aspx).
        
 **P. Como posso conceder acesso à quarentena de spam para os usuários finais?**
  
A. para acessar a quarentena de spam do usuário final, os usuários finais devem ter um ID de usuário válido do Office 365 e uma senha. Os clientes do EOP protegendo as caixas de correio local devem ser criados por meio da sincronização de diretório ou o EAC de usuários de email válido. Para obter mais informações sobre como gerenciar usuários, os administradores do EOP podem consultar a [Gerenciar usuários de email no EOP](eop/manage-mail-users-in-eop.md). Para clientes do EOP, é recomendável usar a sincronização de diretórios e habilitando Directory Based Edge Blocking; Para obter mais informações, consulte [Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx).
  
 **P. É possível enviar qualquer outra mensagem, além de spam, para a quarentena?**
  
R. Uma mensagem que corresponda a uma regra de transporte também pode ser enviada para a quarentena do administrador, desde que a ação esteja configurada. A quarentena de usuário final destina-se apenas a spam.
  
 **P. Por quanto tempo as mensagens são mantidas na quarentena?**
  
R. por padrão, as mensagens de spam em quarentena são mantidas em quarentena por 15 dias, enquanto as mensagens em quarentena que correspondem a uma regra de transporte são mantidas em quarentena por 7 dias. Após este período de tempo, as mensagens são excluídas e não são recuperáveis. O período de retenção de mensagens em quarentena que correspondem a uma regra de transporte não é configurável. No entanto, o período de retenção para mensagens de spam em quarentena pode ser reduzido por meio da configuração de **spam de reter de (dias)** em suas políticas de filtro de conteúdo. Para obter mais informações, consulte [configurar suas políticas de filtro de spam](configure-your-spam-filter-policies.md).
  
 **P. Posso liberar ou relatar mais de uma mensagem em quarentena por vez?**
  
R. a capacidade de liberar ou relatar mensagens de vários ao mesmo tempo não está atualmente disponível no EAC ou na quarentena de spam do usuário final. Entretanto, os administradores podem criar um script do Windows PowerShell remoto para realizar essa tarefa. Use o cmdlet [Get-QuarantineMessage](http://technet.microsoft.com/library/88026da1-8dbc-49e7-80e8-112a32773c34.aspx) para pesquisar mensagens e o cmdlet [Versão-QuarantineMessage](http://technet.microsoft.com/library/4a3aa05c-238f-46f2-b8dd-b0e3c38eab3e.aspx) para liberá-los. 
  
 **P. Coringas são aceitos durante a pesquisa de mensagens em quarentena? Posso pesquisar mensagens em quarentena em um domínio específico?**
  
R. Não há suporte para curingas durante a especificação de critérios de pesquisa no Centro de Administração do Exchange. Por exemplo, ao pesquisar um remetente, especifique o endereço de email completo.
  
Usando o Windows PowerShell remoto, os administradores podem especificar o cmdlet [Get-QuarantineMessage](http://technet.microsoft.com/library/88026da1-8dbc-49e7-80e8-112a32773c34.aspx) para pesquisar por mensagens em quarentena em um domínio específico (por exemplo, contoso.com): 
  
```
Get-QuarantineMessage | ? {$_.Senderaddress -like "*@contoso.com"}
```

Os resultados podem ser passados para o cmdlet [Release-QuarantineMessage](http://technet.microsoft.com/library/4a3aa05c-238f-46f2-b8dd-b0e3c38eab3e.aspx). Inclua o parâmetro -ReleaseToAll para liberar a mensagem para todos os destinatários. Depois de liberada, a mensagem não poderá ser liberada novamente. 
  
```
Get-QuarantineMessage | ? {$_.Senderaddress -like "*@contoso.com"}
```



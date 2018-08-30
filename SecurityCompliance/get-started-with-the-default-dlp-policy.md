---
title: Introdução à política DLP padrão
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/10/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: e0ada764-6422-4b44-9472-513bed04837b
description: Antes de criar sua primeira diretiva de prevention (DLP) de perda de dados até mesmo, DLP é ajudar a proteger suas informações confidenciais com uma política padrão. Essa diretiva padrão e seu recomendação (mostrada abaixo) ajudam a manter seu conteúdo confidencial seguro por informando quando o número do cartão de email ou documentos contendo um crédito foram compartilhadas com alguém de fora da sua organização.
ms.openlocfilehash: 1b522a2c04e72353970ef5dfcd62183023a01994
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524718"
---
# <a name="get-started-with-the-default-dlp-policy"></a>Introdução à política DLP padrão

Antes de criar sua primeira diretiva de prevention (DLP) de perda de dados até mesmo, DLP é ajudar a proteger suas informações confidenciais com uma política padrão. Essa diretiva padrão e seu recomendação (mostrada abaixo) ajudam a manter seu conteúdo confidencial seguro por informando quando o número do cartão de email ou documentos contendo um crédito foram compartilhadas com alguém de fora da sua organização. Você verá essa recomendação na página **inicial** da segurança &amp; Centro de conformidade. 
  
Você pode usar este widget para visualizar rapidamente quando e quanta informação confidencial foi compartilhada e, em seguida, refinar a política DLP padrão em apenas um ou dois cliques. Você também pode editar a política DLP padrão a qualquer momento, porque ele é totalmente personalizável. Observe que se você não vir a recomendação inicialmente, tente clicando em **+ mais** na parte inferior da seção **recomendado para você** . 
  
![Widget denominado adicionais proteger conteúdo compartilhado](media/2bae6dbc-cc92-4f35-b54c-c36e60226b5b.png)
  
## <a name="view-the-report-and-refine-the-default-dlp-policy"></a>Exibir o relatório e refinar a política DLP padrão

Quando o widget mostra que os usuários compartilhou informações confidenciais com pessoas fora da sua organização, escolha a **política de DLP refinar** na parte inferior. 
  
O relatório detalhado mostra quando e como a quantidade de conteúdo que contém os números de cartão de crédito foi compartilhada nos últimos 30 dias. Observe que as correspondências de regra podem levar até 48 horas seja mostrada no widget.
  
Para ajudar a proteger as informações confidenciais, a política DLP padrão:
  
- Detecta quando o conteúdo no Exchange, SharePoint e OneDrive que contém o número de pelo menos um cartão de crédito é compartilhado com pessoas fora da sua organização.
    
- Mostra uma dica de política e envia uma notificação de e-mail para usuários quando eles tentam compartilhar essas informações confidenciais com pessoas fora da sua organização. Para obter mais informações sobre essas opções, consulte [Enviar notificações por email e Mostrar dicas de política para políticas de DLP](use-notifications-and-policy-tips.md).
    
- Gera relatórios de atividade detalhada de modo que você pode controlar coisas como quem o conteúdo compartilhado com pessoas fora da sua organização e quando eles fizeram. Você pode usar os [relatórios DLP](view-the-dlp-reports.md) e os [dados de log de auditoria](search-the-audit-log-in-security-and-compliance.md) (onde **atividade** = **DLP**) para ver essa informação.
    
Para refinar rapidamente a política DLP padrão, você pode optar por fazer com que ele:
  
- Envie um email de relatório de incidente quando usuários compartilharem essas informações confidenciais com pessoas fora da sua organização.
    
- Adicione outros usuários para o relatório de incidente de email.
    
- Bloqueie o acesso ao conteúdo que contém as informações confidenciais, mas permitir que o usuário substituir e compartilhar ou enviar se eles precisam.
    
Para obter mais informações sobre relatórios de incidentes ou restrição de acesso, consulte [Visão geral das políticas de prevenção de perda de dados](data-loss-prevention-policies.md).
  
Se você quiser alterar essas opções mais tarde, você pode editar o padrão a política de DLP a qualquer momento - consulte a próxima seção.
  
![Configurações de widget denominado adicionais de protegem conteúdo compartilhado](media/dad30a84-2715-4c0a-a5c5-44d85492363e.png)
  
## <a name="edit-the-default-dlp-policy"></a>Editar a política DLP padrão

Esta diretiva é chamada **política padrão DLP do Office 365** e aparece na **prevenção de perda de dados** na página **política** de segurança &amp; Centro de conformidade. 
  
Essa diretiva é totalmente personalizável, o mesmo que qualquer política DLP que você criou do zero. Você também pode desativar ou excluir a diretiva, para que os usuários não são mais recebem dicas de política ou notificações de email.
  
![Política de DLP chamada política padrão DLP do Office 365](media/260731e8-4d57-4c98-abec-07b052ec48d5.png)
  
## <a name="when-the-widget-does-and-does-not-appear"></a>Quando o widget e não aparecem

O widget denominado **proteger ainda mais o conteúdo compartilhado** aparece na seção **recomendado para você** da página **inicial** da segurança &amp; Centro de conformidade. 
  
Este widget aparece somente quando:
  
- Não há nenhuma políticas de prevenção de perda de dados na segurança &amp; Centro de conformidade ou centro de administração do Exchange. Este widget destina-se para ajudá-lo a começar a usar DLP, portanto, ela não será exibido se você já tem políticas de DLP.
    
- O conteúdo que contém pelo menos um cartão de crédito foi compartilhado com alguém de fora da sua organização nos últimos 30 dias.
    
Observe que as correspondências de regra podem levar até 48 horas esteja disponível para o widget, portanto após informações confidenciais shared externamente são detectadas, pode levar até dois dias para a recomendação apareça.
  
Finalmente, depois de usar o widget para refinar a política DLP padrão, o widget desaparecerá da página **inicial** . 
  


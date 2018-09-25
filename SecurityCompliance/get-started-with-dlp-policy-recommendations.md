---
title: Introdução às recomendações de políticas DLP
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/7/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 2ea4459b-cb13-4ce2-b9d1-0619316df88c
description: Essa recomendação orientado a percepção ajuda a sua organização manter o conteúdo confidencial seguras quando ele tem armazenado e compartilhado no Office 365 por informando quando há uma lacuna possível em sua cobertura de política DLP. Você verá essa recomendação na Home page da segurança &amp; Centro de conformidade, se seus documentos contêm qualquer um dos cinco maiores tipos mais comuns de informações confidenciais, mas não são protegidos por uma política DLP.
ms.openlocfilehash: fcd3a5a3a12932b22c310938c12f71fb01019411
ms.sourcegitcommit: ede6230c2df398dc0a633e8f32ee0bfede0d5142
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/25/2018
ms.locfileid: "25002624"
---
# <a name="get-started-with-dlp-policy-recommendations"></a>Introdução às recomendações de políticas DLP

Essa recomendação orientado a percepção ajuda a sua organização manter o conteúdo confidencial seguras quando ele tem armazenado e compartilhado no Office 365 por informando quando há uma lacuna possível em sua cobertura de política DLP. Você verá essa recomendação na página **inicial** da segurança &amp; Centro de conformidade, se seus documentos contêm qualquer um dos cinco maiores tipos mais comuns de informações confidenciais, mas não são protegidos por uma política de prevenção (DLP) de perda de dados. 
  
Você pode usar este widget para criar rapidamente uma política de DLP personalizada em apenas um ou dois cliques e depois de criar essa política DLP, ele é totalmente personalizável. Observe que se você não vir a recomendação inicialmente, tente clicando em **+ mais** na parte inferior da seção **recomendado para você** . 
  
![Widget denominado informações confidenciais desprotegidas](media/91bc04d2-6eff-4294-8b73-b2d56d26ffc4.png)
  
## <a name="create-the-recommended-dlp-policy"></a>Criar a política DLP recomendada

Quando o widget mostra que você desprotegido informações confidenciais, escolha a **guia de Introdução** na parte inferior para criar rapidamente uma política DLP. 
  
Para ajudar a proteger as informações sigilosas, essa política DLP:
  
- Detecta quando o conteúdo no Exchange, SharePoint e OneDrive que contém um dos tipos de informações confidenciais desprotegidos é compartilhado com pessoas fora da sua organização.
    
- Gera relatórios de atividade detalhada de modo que você pode controlar coisas como quem o conteúdo compartilhado com pessoas fora da sua organização e quando eles fizeram. Você pode usar os [relatórios DLP](view-the-dlp-reports.md) e os [dados de log de auditoria](search-the-audit-log-in-security-and-compliance.md) (onde **atividade** = **DLP**) para ver essa informação.
    
Você também pode optar por têm a política DLP:
  
- Envie um email de relatório de incidente quando usuários compartilharem muitas dessas informações confidenciais com pessoas fora da sua organização.
    
- Adicione outros usuários para o relatório de incidente de email.
    
- Mostrar uma dica de política e enviar uma notificação por e-mail aos usuários quando eles tentam compartilhar essas informações confidenciais com pessoas fora da sua organização. Para obter mais informações sobre essas opções, consulte [Enviar notificações por email e Mostrar dicas de política para políticas de DLP](use-notifications-and-policy-tips.md).
    
Se você quiser alterar essas opções mais tarde, você pode editar a política de DLP após sua criação. Por exemplo, você pode fazer a política mais restritivas por pessoas mesmo bloqueio de compartilhamento de conteúdo que contém informações confidenciais em primeiro lugar -, consulte a próxima seção.
  
![Configurações do widget denominado informações confidenciais desprotegidas](media/b6106cbd-1bed-4582-aaef-b678de470c9b.png)
  
## <a name="edit-the-recommended-dlp-policy"></a>Editar a política DLP recomendada

Depois de usar o widget para criar uma política DLP, a política aparece na **prevenção de perda de dados** na página **política** de segurança &amp; Centro de conformidade. 
  
Por padrão, a política é denominada **Diretiva recomendados do sistema para o compartilhamento de informações confidenciais**. Essa diretiva é totalmente personalizável, o mesmo que qualquer política DLP que você criou do zero. Por exemplo, se você decidiu não ativar dicas de política e relatórios de incidentes quando você usou o widget, você sempre pode editar a política e ativar essas opções a qualquer momento.
  
![Sistema recomendado de política para o compartilhamento de informações confidenciais](media/2fc49f25-ec25-4433-add4-d60f73888f13.png)
  
## <a name="when-the-widget-does-and-does-not-appear"></a>Quando o widget e não aparecem

O widget denominado **Informações confidenciais desprotegidas** aparece na seção **recomendado para você** da página **inicial** da segurança &amp; Centro de conformidade. 
  
Este widget aparece somente quando:
  
- Novos documentos que contenham qualquer um dos cinco tipos mais comuns de informações confidenciais detectados no SharePoint ou OneDrive nos últimos 30 dias.
    
- Que informações confidenciais já não estão protegidas por uma política DLP existente.
    
Ao contrário de políticas de DLP que estão constantemente verificação de seus dados, essa recomendação examina de falhas na sua cobertura de política DLP quase a cada 48 horas, portanto depois que o novo conteúdo é carregado, pode levar até dois dias para a recomendação apareça.
  
Finalmente, depois de usar o widget para criar uma política DLP recomendada, o widget desaparecerá da página **inicial** . 
  


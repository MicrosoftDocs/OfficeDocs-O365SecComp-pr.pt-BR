---
title: Como a DLP funciona entre o centro de conformidade do & de segurança e o centro de administração do Exchange
ms.author: stephow
author: stephow-msft
manager: laurawi
ms.date: 8/4/2017
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a7e4342a-a0a1-4b43-b166-3d7eecf5d2fd
description: Saiba como a DLP no centro de conformidade do & de segurança funciona com a DLP e regras de fluxo de emails (regras de transporte) no centro de administração do Exchange.
ms.openlocfilehash: 9912103ec95af9fed61c5c2d52d12b46342d16fb
ms.sourcegitcommit: 6aa82374eef09d2c1921f93bda3eabeeb28aadeb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2019
ms.locfileid: "30454903"
---
# <a name="how-dlp-works-between-the-security--compliance-center-and-exchange-admin-center"></a>Como a DLP funciona entre o centro de conformidade do & de segurança e o centro de administração do Exchange

No Office 365, você pode criar uma política de prevenção de perda de dados (DLP) em dois centros de administração diferentes:
  
- No **centro de conformidade do & de segurança**, você pode criar uma única política de DLP para ajudar a proteger o conteúdo no SharePoint, no onedrive e no Exchange. Quando possível, recomendamos que você crie uma política de DLP aqui. Para obter mais informações, consulte [DLP no centro de conformidade do & de segurança](data-loss-prevention-policies.md).
    
- No **centro de administração do Exchange**, você pode criar uma política de DLP para ajudar a proteger o conteúdo somente no Exchange. Essa política pode usar regras de fluxo de emails do Exchange (também conhecidas como regras de transporte), portanto, ela tem mais opções específicas para lidar com emails. Para obter mais informações, consulte [DLP no centro de administração do Exchange](https://go.microsoft.com/fwlink/?linkid=852311).
    
As políticas de DLP criadas nesses centros de administração funcionam lado a lado – este tópico explica como.
  
![Páginas de DLP no centro de administração de segurança e conformidade do Exchange](media/d3eaa7e7-3b16-457b-bd9c-26707f7b584f.png)
  
## <a name="how-dlp-in-the-security--compliance-center-works-with-dlp-and-mail-flow-rules-in-the-exchange-admin-center"></a>Como a DLP no centro de conformidade do & de segurança funciona com as regras de fluxo de email e DLP no centro de administração do Exchange

Depois de criar uma política de DLP no centro de conformidade do & de segurança, a política é implantada em todos os locais incluídos na política. Se a política incluir o Exchange Online, a política será sincronizada e aplicada exatamente da mesma maneira que uma política de DLP criada no centro de administração do Exchange. 
  
Se você tiver criado políticas de DLP no centro de administração do Exchange, essas políticas continuarão a funcionar lado a lado com todas as políticas de email que você cria no centro de conformidade do & de segurança. Mas Observe que as regras criadas no centro de administração do Exchange têm precedência. Todas as regras de fluxo de email do Exchange são processadas primeiro e, em seguida, as regras de DLP do centro de conformidade do & de segurança são processadas.
  
Isso significa que:
  
- As mensagens bloqueadas pelas regras de fluxo de mensagens do Exchange não serão verificadas pelas regras de DLP criadas no centro de conformidade do & de segurança.
    
- Se uma regra de fluxo de email do Exchange modifica uma mensagem de uma maneira que faz com que ela coincida com uma política de DLP no centro de conformidade do & de segurança, como a adição de usuários externos, as regras de DLP detectarão isso e imporão a política, conforme necessário.
    
Observe também que as regras de fluxo de email do Exchange que usam a ação "parar processamento" não afetam o processamento de regras de DLP no centro de conformidade do & de segurança, elas ainda serão processadas.
  
## <a name="policy-tips-in-the-security--compliance-center-vs-the-exchange-admin-center"></a>Dicas de política no centro de conformidade do & de segurança vs. o centro de administração do Exchange

As dicas de política podem funcionar com políticas de DLP e regras de fluxo de email criadas no centro de administração do Exchange ou com políticas de DLP criadas no centro de conformidade do & de segurança, mas não em ambos. Isso ocorre porque essas políticas são armazenadas em locais diferentes, mas as dicas de política podem desenhar apenas de um único local.
  
Se você configurou dicas de política no centro de administração do Exchange, qualquer dica de política configurada no centro de conformidade do & de segurança não aparecerá para os usuários no Outlook na Web e no Outlook 2013 e posterior até que você desative as dicas no centro de administração do Exchange. Isso garante que as regras atuais de fluxo de email do Exchange continuem a funcionar até que você opte por alternar para o centro de conformidade do & de segurança.
  
Observe que, embora as dicas de política possam desenhar apenas de um único local, as notificações por email são sempre enviadas, mesmo que você esteja usando políticas DLP no centro de conformidade do & de segurança e no centro de administração do Exchange.
  


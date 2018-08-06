---
title: Remetentes seguros e bloqueados listas de remetentes no Exchange Online
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/22/2018
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 111ab6b0-2dd2-4a87-a928-4931df6b3c4d
description: Como um administrador do Exchange Online ou Exchange Online Protection (EOP), você pode ajudar a garantir que uma mensagem de email em viagem através do serviço não está marcada como spam. Uma maneira de fazer isso é criar remetente seguro e listas de remetentes bloqueados para as pessoas na sua organização.
ms.openlocfilehash: fcb43f990750782788dc6f459dd5c7d296146a38
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22028078"
---
# <a name="safe-sender-and-blocked-sender-lists-in-exchange-online"></a>Remetentes seguros e bloqueados listas de remetentes no Exchange Online

Como um administrador do Exchange Online ou Exchange Online Protection (EOP), você pode ajudar a garantir que uma mensagem de email em viagem através do serviço não está marcada como spam. Uma maneira de fazer isso é criar remetente seguro e listas de remetentes bloqueados para as pessoas na sua organização. 
  
 *Consulte a versão atualizada das dicas e procedimentos sobre como trabalhar com essas listas como um administrador no* [Impedir email positivo falso marcada como spam com uma lista segura ou outras técnicas](https://go.microsoft.com/fwlink/p/?LinkID=534224). 
  
Se você não for um administrador e desejar apenas gerenciar sua próprias lixo eletrônico no Outlook usando uma lista de remetentes seguros, confira as etapas nesta visão geral do [Filtro de lixo eletrônico](https://go.microsoft.com/fwlink/?LinkId=817222). 
  
## <a name="what-is-the-safe-and-blocked-sender-limits-in-exchange-online"></a>O que é o remetente bloqueado e seguro limites no Exchange Online?

Os limites de remetentes bloqueados e seguros no Exchange Online são diferentes do Active Directory e limites do Outlook. Eles são:
  
- Limite de remetente seguro: 1.024
    
- Limite de remetentes bloqueados: 500
    
Observação:
  
Você pode enfrentar o erro descrita em KB 2590466 ("você recebe o erro"Erro de validação do lixo eletrônico"no Outlook Web App para Exchange Server 2010"). Para resolver esse problema, desmarque a caixa de seleção "Confiar em emails de Meus contatos". Como alternativa, diminua a quantidade de endereços de email que estão na pasta padrão Contatos de colocá-lo dentro o máximo permitido limitar 1.024 no Exchange Online que está definido para o atributo "MaxSafeSenders". Para obter mais informações sobre esse atributo e o cmdlet Set-Mailbox, seethe seguinte tópico:
  
[Set-Mailbox](https://docs.microsoft.com/en-us/powershell/module/exchange/mailboxes/Set-Mailbox?view=exchange-ps)
  
## <a name="see-also"></a>Confira também

[No Exchange 2016 a filtragem por remetente](http://technet.microsoft.com/library/b833f864-ff10-46a0-a653-28fb9ba30896.aspx)


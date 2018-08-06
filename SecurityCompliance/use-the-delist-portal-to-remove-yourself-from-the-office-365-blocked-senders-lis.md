---
title: Usar o portal de remoção da lista para ser removido da lista de remetentes bloqueados do Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/18/2016
ms.audience: ITPro
ms.topic: troubleshooting
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 0bcecdd4-3343-4cc0-9e58-e19d4de515e8
description: Você está recebendo uma mensagem de erro ao tentar enviar um email para um destinatário cujo endereço de email está no Office 365? Se acha que não deve estar recebendo a mensagem de erro, use o portal de remoção da lista para ser removido da lista de remetentes bloqueados do Office 365.
ms.openlocfilehash: 127b305cdb27cffadc7ad6a43a5d2db2440365ca
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026228"
---
# <a name="use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-list"></a>Usar o portal de remoção da lista para ser removido da lista de remetentes bloqueados do Office 365

Você está recebendo uma mensagem de erro ao tentar enviar um email para um destinatário cujo endereço de email está no Office 365? Se acha que não deve estar recebendo a mensagem de erro, use o portal de remoção da lista para ser removido da lista de remetentes bloqueados do Office 365.
  
## <a name="what-is-the-office-365-blocked-senders-list"></a>O que é a lista de remetentes bloqueados do Office 365?

A Microsoft usa a lista de remetentes bloqueados para proteger seus clientes contra spam, falsificação e ataques de phishing. O endereço IP do seu servidor de email, ou seja, o endereço que o seu servidor de email usa para se identificar na Internet, foi marcado como uma possível ameaça para o Office 365 por um de diversos motivos. Quando o Office 365 adiciona o endereço IP à lista, impede toda a comunicação entre o endereço IP e qualquer um dos nossos clientes por meio de nossos data centers.
  
Você saberá que foi adicionado à lista quando receber uma resposta a uma mensagem de email que inclui um erro parecido com o seguinte:
  
550 5.7.606-649 acesso negado, proibidos enviando IP [ _endereço IP_]; Para solicitar remoção dessa lista, visite https://sender.office.com/ e siga as instruções. Para obter mais informações, consulte [relatórios de entrega de Email no Office 365](http://go.microsoft.com/fwlink/?LinkID=526653).
  
em que  _IP address_ é o endereço IP do computador no qual o servidor de email é executado. 
  
### <a name="to-use-the-office-365-delist-portal-to-remove-yourself-from-the-blocked-senders-list"></a>Para usar o portal de remoção da lista do Office 365 a fim de ser removido da lista de remetentes bloqueados

1. Em um navegador da Web, acesse [https://sender.office.com](https://sender.office.com).
    
2. Siga as instruções descritas na página. Certifique-se de usar o endereço de email ao qual a mensagem de erro foi enviada e o endereço IP que é especificado na mensagem de erro. Você só pode inserir um endereço de email e um endereço IP por visita.
    
3. Clique em **Enviar**.
    
    O portal envia um email para o endereço de email que você fornecer. O email terá uma aparência semelhante a seguinte: ![captura de tela de email recebido quando você envia uma solicitação por meio do portal de delist](media/bf13e4f7-f68c-4e46-baa7-b6ab4cfc13f3.png)
  
4. Clique no link confirmação no email enviado a você pelo portal de remoção da lista.
    
    Isso leva você de volta ao portal de remoção da lista.
    
5. No portal de remoção da lista, clique em **remover IP da lista**.
    
    Depois que o endereço IP for removido da lista de remetentes bloqueados, as mensagens de email desse endereço IP serão entregues aos destinatários que usam o Office 365. Portanto, certifique-se de que os emails enviados a partir desse endereço IP não sejam ofensivos ou mal-intencionados; caso contrário, o endereço IP pode ser bloqueado novamente.
    


---
title: Usar notificações de spam do usuário para liberar e reportar mensagens em quarentena no Office 365spam
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 03/14/2019
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 56de4ed5-b0aa-4195-9f46-033d7cc086bc
ms.collection:
- M365-security-compliance
description: Se seu administrador habilitar as notificações para usuários, você receberá uma mensagem de notificação que lista as mensagens enviadas para sua caixa de correio que foram identificadas como spam, massa ou mensagens de phishing. Você pode liberar ou relatar mensagens depois de ser notificado.
ms.openlocfilehash: de67987b0028102bdf61889ce54ca4215182e279
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32263433"
---
# <a name="use-user-spam-notifications-to-release-and-report-quarantined-messages-in-office-365"></a>Usar notificações de spam do usuário para liberar e reportar mensagens em quarentena no Office 365spam

Se seu administrador habilitar notificações de spam para usuários, você receberá uma mensagem de notificação que lista as mensagens endereçadas à sua caixa de correio que foram identificadas como spam e colocadas em quarentena.
  
> [!TIP]
> Se você é um administrador e deseja habilitar esse recurso, você pode escolher a opção ao [modificar uma política antispam padrão](https://go.microsoft.com/fwlink/?LinkId=800313). 
  
A mensagem recebida inclui o número de mensagens de spam em quarentena que você tem e a data e a hora (no UTC ou horário coordenado universal) da última mensagem na lista. A lista inclui o seguinte para cada mensagem:
  
- **Remetente** O nome de envio e o endereço de email da mensagem em quarentena. 
    
- **Assunto** O texto da linha do assunto da mensagem em quarentena. 
    
- **Data** A data e a hora (em UTC) em que a mensagem foi colocada em quarentena. 
    
- **Tamanho** O tamanho da mensagem, em kilobytes (KBs). 
    
Estas são as ações que você pode realizar com uma mensagem em quarentena:

- **Visualize** a mensagem se quiser visualizar o conteúdo ou o cabeçalho antes de executar a ação.

- **Baixe** a mensagem se quiser revisar a mensagem e os anexos (se houver) no dispositivo antes de executar a ação.

- **Versão** se a mensagem não for spam e se você quiser que o Office 365 envie a mensagem para sua caixa de correio.

- **Release _AMP_ Allow Sender** se a mensagem não for spam e se você quiser que o Office 365 adicione o remetente à sua lista de remetentes e destinatários confiáveis para futuros emails. Tenha em mente que seu administrador pode ter outras configurações de permissão/bloqueio de toda a organização que substituem sua lista de remetentes seguros.

- **Release _AMP_ Report**, se a mensagem não for spam e você deseja enviar a mensagem para sua caixa de correio e relatá-la para a Microsoft para análise.

- **Bloquear** se você quiser que o Office 365 adicione o remetente à sua lista de remetentes bloqueados.

Esteja ciente do seguinte:
  
- As mensagens colocadas em quarentena porque corresponderam a uma regra de fluxo de emails não estão incluídas nas mensagens em quarentena do usuário. Somente as mensagens em quarentena por spam estão listadas.
    
- Você só pode liberar uma mensagem e relatá-la como falso positivo (e não como lixo eletrônico) uma vez.
    


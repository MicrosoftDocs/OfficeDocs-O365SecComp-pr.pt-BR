---
title: Email de domínio não registrado
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 10/17/2018
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection:
- M365-security-compliance
description: Se você enviar um alto volume de emails de domínio não registrados, correrá o risco de que seu email fique bloqueado. Leia este artigo para saber mais.
ms.openlocfilehash: 21c403c8072902565f63048782b06c531cdbceb0
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32263983"
---
# <a name="unregistered-domain-email-what-you-need-to-know"></a>Email de domínio não registrado: o que você precisa saber

O Office 365 permite que os locatários transmitam algumas mensagens por meio do Exchange Online Protection (EOP). Um exemplo com suporte é quando os usuários têm uma caixa de correio do Office 365 e alguém externo envia esses emails, mas o encaminhamento de emails é configurado para que ele volte para a caixa de correio externa do usuário. Isso é mais comum em ambientes educacionais em que os alunos querem aproveitar sua interface de email pessoal, mas ainda receber emails relacionados à escola. Outro exemplo é quando os clientes estão em um cenário híbrido e têm servidores locais que enviam emails do EOP.

## <a name="problems-with-unregistered-domains"></a>Problemas com domínios não registrados

O problema ocorre quando os servidores locais são comprometidos e acabam retransmitindo um grande volume de spam do EOP. Em quase todos os casos, os conectores corretos são configurados, mas o email é enviado de domínios não registrados, também conhecidos como desprovisionados,. O Office 365 permite uma quantidade razoável de emails provenientes de domínios não registrados, mas um domínio aceito deve ser configurado no centro de administração para cada domínio em que você pretende enviar.

Após o comprometimento, os locatários serão impedidos de enviar emails de saída para domínios não registrados. Os usuários receberão uma NDR (notificação de falha na entrega) que diz:

- 550 o serviço 5.7.750 não está disponível. Cliente impedido de enviar de domínios não registrados

## <a name="unblocking-tenant-in-order-to-send-again"></a>Desbloqueando o locatário para enviar novamente

Há várias coisas que você precisa fazer se você estiver bloqueado para envio de domínios não registrados:

1. Certifique-se de registrar todos os seus domínios no centro de administração do Microsoft 365. Mais informações podem ser encontradas [aqui](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).

2. Procure por conectores incomuns. Os atores mal-intencionados geralmente criarão novos conectores de entrada em seu locatário do Office 365 para enviar spam. Você pode encontrar mais informações sobre como verificar seus conectores [aqui](https://docs.microsoft.com/en-us/powershell/module/exchange/mail-flow/get-inboundconnector?view=exchange-ps). 

3. Bloqueie seus servidores locais e certifique-se de que eles não estão comprometidos.

> [!TIP]
> Há muitos fatores envolvidos aqui, especialmente se forem servidores de terceiros. Independentemente disso, você precisará confirmar que todos os emails que deixam seus servidores são legítimos.

4. Após concluir, você precisará ligar para o suporte da Microsoft e solicitar que o locatário seja desbloqueado para envio de domínios não registrados.  Fornecer o código de erro é útil, mas você precisará provar que seu ambiente está protegido e que o spam não será enviado novamente. É possível encontrar mais informações sobre como abrir um caso de suporte [aqui](https://support.office.com/en-us/article/Contact-support-for-business-products-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b#ID0EAADAAA=online).
  
## <a name="for-more-information"></a>Para obter mais informações

[Office 365 email anti-spam protection](anti-spam-protection.md)

[Notificações de falha na entrega de email no Office 365](https://support.office.com/article/email-non-delivery-reports-in-office-365-51daa6b9-2e35-49c4-a0c9-df85bf8533c3)

[Configurar o encaminhamento de email para uma caixa de correio](https://docs.microsoft.com/en-us/exchange/recipients-in-exchange-online/manage-user-mailboxes/configure-email-forwarding)

[Como configurar um dispositivo multifuncional ou aplicativo para enviar email usando o Office 365](https://support.office.com/en-us/article/How-to-set-up-a-multifunction-device-or-application-to-send-email-using-Office-365-69f58e99-c550-4274-ad18-c805d654b4c4)

[Gerenciar domínios aceitos no Exchange Online](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).

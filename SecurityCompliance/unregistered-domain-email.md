---
title: Email de domínio não registrados
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 09/17/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
description: Se você enviar um grande volume de email do domínio não registrados, você correrá o risco de seu email obtendo bloqueado. Leia este artigo para saber mais.
ms.openlocfilehash: f2b60f492197bf0dadb702a1c3f184c2d7e56bf1
ms.sourcegitcommit: 7b85c22fc85ec19e4b44a07e91bfa9ade768185a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2018
ms.locfileid: "23998595"
---
# <a name="unregistered-domain-email-what-you-need-to-know"></a>Email de domínio não registrado: O que você precisa saber

O Office 365 permite inquilinos retransmitir algumas mensagens por meio de Exchange Online Protection (EOP). Um exemplo com suporte, isso seria quando os usuários têm uma caixa de correio do Office 365 e alguém externo envia email mas encaminhamento de email está configurado de forma que ele volta check-out para a caixa de correio externa do usuário. Isso é mais comum em ambientes de educação em alunos desejarem aproveitar seu interface email pessoal mas ainda têm emails relacionados à escola. Outro exemplo é quando os clientes estão em um cenário híbrido e tem servidores no local que enviam emails fora do EOP.

## <a name="problems-with-unregistered-domains"></a>Problemas com domínios não registrados

O problema é quando os servidores no local estiver comprometidos e acabam retransmissão de um grande volume de spam fora do EOP. Em quase todos os casos, os conectores direita estiver configurados, mas email está sendo enviado do não registrados, também conhecido como desprovisionados, domínios. Office 365 permitem que uma quantidade razoável de emails provenientes de domínios não registrados, mas um domínio aceito deve ser configurado no Centro de administração para cada domínio que você planeja enviar ausência temporária.

Depois que comprometida, inquilinos serão impedidos de enviar mensagens de saída para domínios não registrados. Os usuários receberão um não-entrega relatório (NDR) declarando:

- 550 5.7.750 serviço indisponível. Cliente bloqueado para o envio de domínios não registrados

## <a name="unblocking-tenant-in-order-to-send-again"></a>Desbloqueando locatário para enviar novamente

Há várias coisas que você precisa fazer se obter bloqueado para o envio de domínios não registrados:

1. Certifique-se de que você registre todos os seus domínios no Centro de administração do Office 365. Mais informações podem ser encontradas [aqui](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).

2. Bloquear os servidores no local e certifique-se de que eles não estão comprometidos. Há vários fatores envolvidos aqui, especialmente se esses são os servidores de terceiros, mas você precisará ser capaz de certificar-se de que todos os emails deixando nesse servidor é legítimo.

Depois de concluído, você precisará chamar o Microsoft Support e pede para obter seu locatário desbloqueado para enviar de domínios não registrados novamente.  Fornecer o código de erro é útil, mas você precisará provar que seu ambiente esteja protegido e que spam não será enviada novamente. Mais informações podem ser encontradas [aqui](https://support.office.com/en-us/article/Contact-support-for-business-products-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b#ID0EAADAAA=online).
  
## <a name="for-more-information"></a>Para saber mais

[Proteção antispam de emails do Office 365](anti-spam-protection.md)

[Relatórios de entrega de email no Office 365](https://support.office.com/article/email-non-delivery-reports-in-office-365-51daa6b9-2e35-49c4-a0c9-df85bf8533c3)

[Configurar o encaminhamento de emails para uma caixa de correio](https://docs.microsoft.com/en-us/exchange/recipients-in-exchange-online/manage-user-mailboxes/configure-email-forwarding)

[Como configurar um dispositivo multifuncional ou aplicativo para enviar email usando o Office 365](https://support.office.com/en-us/article/How-to-set-up-a-multifunction-device-or-application-to-send-email-using-Office-365-69f58e99-c550-4274-ad18-c805d654b4c4)

[Gerenciar domínios aceitos no Exchange Online](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).

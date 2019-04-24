---
title: Fluxo de entrada e saída de emails
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: 8/7/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: f2738dec-41b0-43c4-b814-84c0a4e45c6d
description: Os administradores podem saber mais sobre o widget fluxo de email de saída e entrada no painel de fluxo de emails no centro de conformidade do & de segurança.
ms.openlocfilehash: 89408618e7c5b3c921382b3efa0257f263509b6d
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32252201"
---
# <a name="outbound-and-inbound-mail-flow"></a>Fluxo de entrada e saída de emails

O widget **saída e fluxo** de emails de entrada combina as informações do **relatório de conector** e o **relatório de visão geral de TLS** anterior em um só lugar.

![O relatório de fluxo de emails de entrada e de saída no painel de fluxo de emails no centro de conformidade do & de segurança](media/2c591d1c-bad6-4b72-890e-f8fdfd4f447a.png)

As informações no widget estão relacionadas a conectores e proteção de mensagem TLS no Office 365. Para obter mais informações, consulte estes tópicos:

- [Configure mail flow using connectors in Office 365](https://technet.microsoft.com/library/ms.exch.eac.connectorselection.aspx)

- [Como o Exchange Online usa o TLS para proteger conexões de email no Office 365](https://support.office.com/article/4CDE0CDA-3430-4DC0-B489-F2C0736C929F)

## <a name="message-protected-in-transit-by-tls"></a>Mensagem protegida em trânsito (por TLS)

O widget **saída e fluxo** de emails de entrada exibe a criptografia TLS que é usada para a conexão quando as mensagens são entregues e de sua organização do Office 365. As conexões estabelecidas com outros serviços de email são criptografadas por TLS quando o TLS é oferecido por ambos os lados. O widget oferece um instantâneo da última semana de fluxo de emails. Quando você clica em **Exibir detalhes**, o submenu **mensagem protegido por transporte (TLS)** mostra a proteção TLS para mensagens que entram e saem da sua organização.

![O submenu mensagens protegidas em trânsito (por TLS) no centro de conformidade de & de segurança](media/825aa74c-413d-4141-8e3c-dfe68ae78eed.png)

Atualmente, o TLS 1,2 é a versão mais segura do TLS oferecido pelo Office 365. Muitas vezes, você precisará saber a criptografia TLS que está sendo usada para auditorias de conformidade. Provavelmente você não tem uma relação direta com a maioria dos servidores de email de origem e de destino (você não é proprietário deles, e nenhuma da Microsoft), portanto, você não tem muitas opções para melhorar a criptografia TLS usada por esses servidores.

No enTanto, você [](https://technet.microsoft.com/library/ms.exch.eac.connectorselection.aspx) pode usar conectores para garantir a melhor proteção TLS disponível para mensagens enviadas entre seus servidores de email e o Office 365. O fluxo de email entre o Office 365 e seus próprios servidores de email ou servidores que pertencem a seus parceiros é freqüentemente mais importante e confidencial do que as mensagens normais, portanto, você deve aplicar segurança e vigilância extra a essas mensagens. Você pode atualizar ou corrigir seus próprios servidores de email para melhorar a criptografia TLS que está sendo usada ou acessar seus parceiros para fazer o mesmo. O **relatório do conector** exibe o volume de fluxo de emails e a criptografia TLS para mensagens que usam os conectores do Office 365.

## <a name="connector-report"></a>Relatório do conector

Quando você clica no link de **relatório do conector** a partir do submenu **mensagem protegido em trânsito (por TLS)** , o relatório exibe informações sobre as mensagens que são entregues na sua organização do Office 365 usando conectores. Você usa conectores entre seus próprios servidores de email e o Office 365 ou os servidores do seu parceiro e o Office 365. O volume da mensagem para cada conector e a criptografia TLS para a conexão está disponível. Além disso, você também pode exibir dados de mensagens que foram enviadas ou recebidas no Office 365 sem usar um conector.

O modo de exibição de **fluxo** de emails mostra o volume de mensagens por meio do conector da última semana. Você pode alterar o intervalo de datas selecionando **filtro** onde você pode aumentar o intervalo para no máximo 30 dias. O modo de exibição **All Mail Flow** mostra todo o fluxo de emails de e para sua organização do Office 365 por meio de todos os conectores. Você pode selecionar um conector específico por nome no menu suspenso.

Você pode selecionar o modo de exibição de **uso de TLS** no menu suspenso para ver a divisão da proteção TLS para mensagens por meio do conector. Assim como o relatório de **relatório de visão geral de TLS** , este modo de exibição mostra a porcentagem das diferentes versões de TLS. Para conexões TLS 1,0, você realmente precisa obter o servidor de email ou o servidor de seu parceiro atualizado ou corrigido para evitar qualquer problema quando o suporte a TLS 1,0 for eventualmente preterido no Office 365. Para obter mais informações, consulte [Technical Reference Details about Encryption in Office 365](https://support.office.com/article/862cbe93-4268-4ef9-ba79-277545ecf221).

O ideias aponta para conectores para ajudar a chamar a atenção para possíveis problemas de criptografia TLS para o conector. Os insights são: **nenhum TLS é maior que 25%** ou **TLS 1,0 está acima de 50%**. Se você vir esses insights, será necessário investigar seus servidores de email associados ao conector ou acessar sua organização de parceiro.

## <a name="see-also"></a>Confira também

Para obter mais informações sobre outros insights de fluxo de email no painel de fluxo de emails, consulte [Mail Flow insights no centro de conformidade de & de segurança](mail-flow-insights.md).

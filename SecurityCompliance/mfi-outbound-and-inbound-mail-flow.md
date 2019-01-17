---
title: Fluxo de emails de entrada e saída
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: 8/7/2018
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f2738dec-41b0-43c4-b814-84c0a4e45c6d
description: Os administradores podem conhecer a saída e widget de fluxo de emails de entrada no painel de fluxo de email no Centro de conformidade do & de segurança do Office 365.
ms.openlocfilehash: 57792c0347490b40f97a8b92945a9c809484ba4f
ms.sourcegitcommit: 25fb33a1f8b2844fde15f6c03db2936c610824e0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28685310"
---
# <a name="outbound-and-inbound-mail-flow"></a>Fluxo de emails de entrada e saída

O **fluxo de emails de entrada e saída** widget combina as informações do **Relatório de conector** e o primeiro **Relatório de visão geral de TLS** em um único local.

![O relatório de fluxo de email de saída e entrada no painel de fluxo de email no Centro de conformidade do & de segurança do Office 365](media/2c591d1c-bad6-4b72-890e-f8fdfd4f447a.png)

As informações no widget estão relacionadas à proteção de mensagem TLS no Office 365 e conectores. Para obter mais informações, consulte estes tópicos:

- [Configure mail flow using connectors in Office 365](https://technet.microsoft.com/library/ms.exch.eac.connectorselection.aspx)

- [Como o Exchange Online usa o TLS para proteger conexões de e-mail no Office 365](https://support.office.com/article/4CDE0CDA-3430-4DC0-B489-F2C0736C929F)

## <a name="message-protected-in-transit-by-tls"></a>Mensagem protegida em trânsito (por TLS)

O **fluxo de emails de entrada e saída** widget exibe a criptografia TLS que é usada para a conexão quando as mensagens são entregues para e da sua organização do Office 365. As conexões estabelecidas com outros serviços de email são criptografadas por TLS quando TLS é oferecido por ambos os lados. O widget oferece um instantâneo da última semana do fluxo de emails. Quando você clica em **Exibir detalhes**, o **mensagem protegida em trânsito (por TLS)** submenu mostra a proteção de TLS para mensagens entram e saem da sua organização.

![As mensagens protegidas em trânsito (por TLS) submenu no Centro de conformidade do & de segurança do Office 365](media/825aa74c-413d-4141-8e3c-dfe68ae78eed.png)

Atualmente, o TLS 1.2 é a versão mais segura do TLS é oferecida pelo Office 365. Muitas vezes, você precisará saber a criptografia TLS que está sendo usada para auditorias de conformidade. Você provavelmente não tem uma relação direta com a maioria dos servidores de origem e destino email (você não possui-los e nem faz Microsoft), portanto você não tem várias opções para melhorar a criptografia TLS que é usada por esses servidores.

Mas, você pode usar [conectores](https://technet.microsoft.com/library/ms.exch.eac.connectorselection.aspx) para garantir a melhor TLS proteção disponível para mensagens enviadas entre os servidores de email e o Office 365. Fluxo de email entre o Office 365 e seus próprios servidores de email ou servidores que pertencem aos seus parceiros geralmente é mais importantes e confidenciais que mensagens normais, portanto você vai querer aplicar segurança extra e vigilância a essas mensagens. Você pode atualizar ou corrigir seus próprios servidores de email para melhorar a criptografia TLS que está sendo usada ou chegar aos seus parceiros para fazer o mesmo. O **Relatório de conector** exibe o volume de fluxo de emails e a criptografia TLS para mensagens que usam conectores seu Office 365.

## <a name="connector-report"></a>Relatório de conector

Quando você clica no link de **Relatório de conector** do submenu da **mensagem protegida em trânsito (por TLS)** , o relatório exibe informações sobre mensagens enviadas de e para sua organização do Office 365 usando conectores. Você pode usar conectores entre seus próprios servidores de email e Office 365 ou seu parceiro servidores e Office 365. O volume de mensagem para cada conector e a criptografia TLS para a conexão estão disponíveis. Além disso, também é possível exibir os dados para mensagens que foram enviadas ou recebidas no Office 365 sem usar um conector.

O modo de exibição **Mail Flow** mostra o volume de mensagens por meio do conector para a semana passada. Você pode alterar o intervalo de datas, selecionando **filtro** , onde você pode aumentar o intervalo máximo de 30 dias. O modo de exibição de **Todo o fluxo de email** mostra todos os emails de e para sua organização do Office 365 por meio de todos os conectores de fluxo. Você pode selecionar um conector específico pelo nome, no menu suspenso.

Você pode selecionar o modo de exibição **uso TLS** do menu para baixo para ver a divisão da proteção de TLS para mensagens por meio do conector. Como com o relatório de **Relatório de visão geral de TLS** , esse modo de exibição mostra o percentual de diferentes versões TLS. Para conexões TLS 1.0, você realmente precisa fazer o seu servidor de email ou o servidor do seu parceiro atualizados ou fixo evitar problemas ao suporte a TLS 1.0 eventualmente foi preterido no Office 365. Para obter mais informações, consulte [os detalhes de referência técnica sobre criptografia no Office 365](https://support.office.com/article/862cbe93-4268-4ef9-ba79-277545ecf221).

Ideias apontam para conectores para ajudar a desenhar sua atenção aos potenciais problemas de criptografia TLS para o conector. São as ideias: **TLS não for mais de 25%** ou **TLS 1.0 acima de 50%**. Se você vir esses ideias, você precisará investigar seus servidores de email que estão associadas com o conector ou chegar aos sua organização parceira.

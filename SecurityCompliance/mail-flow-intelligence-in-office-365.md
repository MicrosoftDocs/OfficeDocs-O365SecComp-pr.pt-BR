---
title: Inteligência de fluxo de emails no Office 365
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c29f75e5-c16e-409e-a123-430691e38276
description: Os administradores podem conhecer os códigos de erro que estão associados a entrega de mensagens usando conectores no Office 365 (também conhecido como inteligência de fluxo de email).
ms.openlocfilehash: 9f27dfd4c265eb62028d68c27764183202692ef4
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2019
ms.locfileid: "28327083"
---
# <a name="mail-flow-intelligence-in-office-365"></a>Inteligência de fluxo de emails no Office 365

Normalmente, você deve usar um conector para rotear mensagens de email da sua organização do Office 365 para seu ambiente de email local. Você também pode usar um conector para rotear mensagens enviadas do Office 365 para uma organização parceira. Quando o Office 365 não pode entregar mensagens por meio do conector, eles-em fila no Office 365. O Office 365 continuará tentar novamente a entrega para cada mensagem para 48 horas. Após 48 horas, a mensagem na fila expirará e a mensagem será retornada ao remetente original em um relatório de falha na entrega (também conhecido como uma mensagem de notificação de falha na ou rejeição).

O Office 365 gerará um erro quando uma mensagem não pode ser entregue por meio de um conector. Os erros mais comuns e suas soluções são descritas neste tópico. Coletivamente, erros de enfileiramento de mensagens e notificação não entregue mensagens enviadas por meio de conectores é conhecido como _inteligência de dados de fluxo de email_.

## <a name="error-code-450-44312-dns-query-failed"></a>Código de erro: falha de consulta de DNS 450 4.4.312

Normalmente, esse erro significa que Office 365 tentou se conectar ao host inteligente especificado no conector, mas a consulta DNS para localizar os endereços IP do host inteligente falhou. As causas possíveis desse erro são:

- Há um problema com o DNS do seu domínio que hospeda o serviço (o participante que mantém os servidores de nomes de autorização para seu domínio).

- Seu domínio recentemente expirou, para que o registro MX não possam ser recuperado.

- Registro de MX do seu domínio foi alterada recentemente e os servidores DNS do Office 365 ainda tem anteriormente no cache DNS informações do seu domínio.

### <a name="how-do-i-fix-error-code-450-44312"></a>Como faço para corrigir o código de erro 450 4.4.312?

- Trabalhar com seu serviço de hospedagem de DNS para identificar e corrigir o problema com o seu domínio.

- Se o erro for de sua organização parceira (por exemplo, um 3º nuvem serviço provedor de terceiros), contate seu parceiro para corrigir o problema.

## <a name="error-code-450-44315-connection-timed-out"></a>Código de erro: 450 4.4.315 Conexão esgotado

Normalmente, isso significa que Office 365 não pode se conectar ao servidor de email de destino. Detalhes do erro explicará o problema. Por exemplo:

- Seu servidor de email no local está inoperante.

- Há um erro nas configurações de host inteligente do conector, para que o Office 365 está tentando se conectar a um endereço IP incorreto.

### <a name="how-do-i-fix-error-code-450-44315"></a>Como faço para corrigir o código de erro 450 4.4.315?

- Descobrir qual cenário se aplica a você e faça as correções necessárias. Por exemplo, se o fluxo de email tiver sido funcionando corretamente, e você não tiver alterado as configurações do conector, você precisa verificar seu ambiente de email local para ver se o servidor está inoperante ou se houve alterações à sua infraestrutura de rede (por exemplo, Você alterou provedores de serviços de internet, portanto você agora ter endereços IP diferentes).

- Se o erro for de sua organização parceira (por exemplo, um 3º nuvem serviço provedor de terceiros), contate seu parceiro para corrigir o problema.

## <a name="error-code-450-44316-connection-refused"></a>Código de erro: 450 4.4.316 Conexão recusada

Normalmente, esse erro significa que Office 365 encontrou um erro de conexão ao tentar se conectar ao servidor de email de destino. Uma causa provável para este erro é que seu firewall está bloqueando conexões de endereços IP do Office 365. Ou, esse erro pode ser por design se você tiver sido migrado completamente seu local sistema de email para o Office 365 e desligar o seu ambiente de email local.

### <a name="how-do-i-fix-error-code-450-44316"></a>Como faço para corrigir o código de erro 450 4.4.316?

- Se você tiver caixas de correio em seu ambiente local, você precisará modificar as configurações de firewall para permitir conexões de endereços IP do Office 365 na porta TCP 25 para os servidores de email local. Para obter uma lista dos endereços IP do Office 365, consulte [URLs do Office 365 e intervalos de endereços IP](https://support.office.com/article/8548a211-3fe7-47cb-abb1-355ea5aa88a2.aspx).

- Se não há mais mensagens devem ser entregues ao seu ambiente local, clique em **corrigir agora** no alerta para que o Office 365 pode rejeitar imediatamente as mensagens com destinatários inválidos. Isso reduzirá o risco de exceder a cota da sua organização para destinatários inválidos, que poderiam afetar a entrega da mensagem normal. Ou então, você pode usar as instruções a seguir para manualmente para corrigir o problema:

  - No [Centro de administração do Exchange (EAC)](https://docs.microsoft.com/Exchange/exchange-admin-center) no Office 365, desabilitar ou excluir o conector de entrega de emails do Office 365 para seu ambiente de email local:

    1. No EAC, vá para **fluxo de email** \> **conectores**.

    2. Selecione o conector com o valor **do** **Office 365** e o valor **para** **o servidor de email da sua organização** e execute uma das seguintes etapas:

       - Excluir o conector clicando em **Excluir** ![ícone Remover](media/adf01106-cc79-475c-8673-065371c1897b.gif)

       - Desativar o conector clicando em **Editar** ![ícone Editar](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) e desmarcando **ativá-lo**.

  - Altere o domínio aceito no Office 365 que está associado ao seu ambiente de email no local de **Retransmissão interna** como **autoritativo**. Para obter instruções, consulte [Gerenciar domínios aceitos no Exchange Online](https://go.microsoft.com/fwlink/p/?linkid=785428).

  **Observação**: geralmente, essas alterações terão entre 30 minutos e uma hora entre em vigor. Após uma hora, verifique se você não é mais recebe o erro.

- Se o erro for de sua organização parceira (por exemplo, um 3º nuvem serviço provedor de terceiros), será necessário entrar em contato com seu parceiro para corrigir o problema.

## <a name="error-code-450-44317-cannot-connect-to-remote-server"></a>Código de erro: 450 4.4.317 não é possível conectar ao servidor remoto

Normalmente, esse erro significa o Office 365 é conectado ao servidor de email de destino, mas o servidor respondeu com um erro imediato ou não cumprir os requisitos de conexão. Detalhes do erro explicará o problema. Por exemplo:

- O servidor de email de destino respondeu com um erro "Serviço não disponível", que indica que o servidor é capaz de manter a comunicação com o Office 365.

- O conector é configurado para exigir o TLS, mas o servidor de email de destino não oferece suporte a TLS.

### <a name="how-do-i-fix-error-code-450-44317"></a>Como faço para corrigir o código de erro 450 4.4.317?

- Verifique as configurações de TLS e certificados em seus servidores de email local e as configurações de TLS no conector.

- Se o erro for de sua organização parceira (por exemplo, um 3º nuvem serviço provedor de terceiros), será necessário entrar em contato com seu parceiro para corrigir o problema.

## <a name="error-code-450-44318-connection-was-closed-abruptly"></a>Código de erro: 450 4.4.318 Conexão foi fechada abruptamente

Normalmente, esse erro significa o que Office 365 está tendo dificuldades para comunicação com o seu ambiente de email local, para que a conexão foi abandonada. As causas possíveis desse erro são:

- Seu firewall usa regras de exame de pacotes de SMTP e as regras não estão funcionando corretamente.

- Seu servidor de email no local não está trabalhando corretamente (por exemplo, serviço cai, panes ou poucos recursos no sistema), que está fazendo com que o servidor de tempo limite e fechar a conexão para o Office 365.

- Existem problemas de rede entre seu ambiente local e o Office 365.

### <a name="how-do-i-fix-error-code-450-44318"></a>Como faço para corrigir o código de erro 450 4.4.318?

- Descobrir qual cenário se aplica a você e faça as correções necessárias.

- Se o problema for causado por problemas de rede entre seu ambiente local e o Office 365, contate sua equipe de rede para solucionar o problema.

- Se o erro for de sua organização parceira (por exemplo, um 3º nuvem serviço provedor de terceiros), será necessário entrar em contato com seu parceiro para corrigir o problema.

## <a name="error-code-450-47320-certificate-validation-failed"></a>Código de erro: Falha na validação do certificado de 450 4.7.320

Normalmente, esse erro significa que Office 365 encontrou um erro ao tentar validar o certificado do servidor de email de destino. Detalhes do erro explicará o erro. Por exemplo:

- O certificado expirou

- Incompatibilidade de assunto do certificado

- Certificado não é mais válido

### <a name="how-do-i-fix-error-code-450-47320"></a>Como faço para corrigir o código de erro 450 4.7.320?

- O certificado de corrigi-los ou as configurações no conector de forma que permanece na fila de mensagens no Office 365 podem ser entregues.

- Se o erro for de sua organização parceira (por exemplo, um 3º nuvem serviço provedor de terceiros), será necessário entrar em contato com seu parceiro para corrigir o problema.

## <a name="other-error-codes"></a>Outros códigos de erro

O Office 365 está tendo dificuldades para entrega de mensagens no seu local ou servidor de email de parceiro. Use as informações do **servidor de destino** no erro para examinar o problema em seu ambiente ou modificar o conector se houver um erro de configuração. 

Se o erro for de sua organização parceira (por exemplo, um 3º nuvem serviço provedor de terceiros), será necessário entrar em contato com seu parceiro para corrigir o problema.

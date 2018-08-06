---
title: Inteligência de dados de fluxo de email no Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/27/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: c29f75e5-c16e-409e-a123-430691e38276
description: 'Normalmente, você usa um conector para rotear mensagens da sua organização do Office 365 para seu local ambiente de mensagens. Você também pode usar um conector para rotear mensagens enviadas do Office 365 para uma organização parceira. Quando o Office 365 não pode entregar mensagens por meio do conector, eles-em fila no Office 365. '
ms.openlocfilehash: 495d73524afb3ab3a34fd2f1f5f4cd747481f9d8
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027618"
---
# <a name="mail-flow-intelligence-in-office-365"></a>Inteligência de dados de fluxo de email no Office 365
  
Normalmente, você usa um conector para rotear mensagens da sua organização do Office 365 para seu local ambiente de mensagens. Você também pode usar um conector para rotear mensagens enviadas do Office 365 para uma organização parceira. Quando o Office 365 não pode entregar mensagens por meio do conector, eles-em fila no Office 365. O Office 365 continuará tentar novamente a entrega para cada mensagem para 48 horas. Após 48 horas, a mensagem na fila expirará e a mensagem será retornada ao remetente original em um relatório de falha na entrega (também conhecido como uma mensagem de notificação de falha na ou rejeição).
  
O Office 365 gerará um erro quando uma mensagem não pode ser entregue por meio de um conector. Os erros mais comuns e suas soluções são descritas neste tópico. Coletivamente, erros de enfileiramento de mensagens e notificação não entregue mensagens enviadas por meio de conectores é conhecido como fluxo de mensagens de inteligência de dados.
  
 **Sumário**
  
- [Código de erro: falha de consulta de DNS 450 4.4.312](mail-flow-intelligence-in-office-365.md#ErrorCode44312)
    
- [Código de erro: 450 4.4.315 Conexão esgotado](mail-flow-intelligence-in-office-365.md#ErrorCode44315)
    
- [Código de erro: 450 4.4.316 Conexão recusada](mail-flow-intelligence-in-office-365.md#ErrorCode44316)
    
- [Código de erro: 450 4.4.317 não é possível conectar ao servidor remoto](mail-flow-intelligence-in-office-365.md#ErrorCode44317)
    
- [Código de erro: 450 4.4.318 Conexão foi fechada abruptamente](mail-flow-intelligence-in-office-365.md#ErrorCode44318)
    
- [Código de erro: Falha na validação do certificado de 450 4.7.320](mail-flow-intelligence-in-office-365.md#ErrorCode47320)
    
## <a name="error-code-450-44312-dns-query-failed"></a>Código de erro: falha de consulta de DNS 450 4.4.312
<a name="ErrorCode44312"> </a>

Normalmente, esse erro significa o Office 365 tentou se conectar ao host inteligente especificado no conector, mas a consulta DNS para localizar o IP do host inteligente lida com falha. As causas possíveis desse erro são:
  
- Há um problema com o DNS do seu domínio que hospeda o serviço (o participante que mantém os servidores de nomes de autorização para seu domínio).
    
- Seu domínio recentemente expirou, para que o registro MX não possam ser recuperado.
    
- Registro de MX do seu domínio foi alterada recentemente e os servidores DNS do Office 365 ainda tem anteriormente no cache DNS informações do seu domínio.
    
Você precisa para corrigir o problema DNS trabalhando com seu serviço de hospedagem de DNS.
  
Se o erro for de sua organização parceira (por exemplo, um 3º nuvem serviço provedor de terceiros), será necessário entrar em contato com seu parceiro para corrigir o problema.
  
## <a name="error-code-450-44315-connection-timed-out"></a>Código de erro: 450 4.4.315 Conexão esgotado
<a name="ErrorCode44315"> </a>

Normalmente, isso significa que Office 365 não pode se conectar ao servidor de mensagens de destino. Detalhes do erro explicará o problema. Por exemplo:
  
- Seu servidor de mensagens está desativado no local.
    
- Há um erro nas configurações de host inteligente do conector, para que o Office 365 está tentando se conectar a um endereço IP incorreto.
    
Descobrir qual cenário se aplica a você e faça as correções necessárias. Por exemplo, se o fluxo de email tiver sido funcionando corretamente, e você não tiver alterado as configurações do conector, você precisa verificar seu local o ambiente de mensagens para verificar se o servidor está desativado, ou se houve alterações à sua infraestrutura de rede (por exemplo, Você alterou provedores de serviços de Internet, portanto você agora ter endereços IP diferentes).
  
Se o erro for de sua organização parceira (por exemplo, um 3º nuvem serviço provedor de terceiros), será necessário entrar em contato com seu parceiro para corrigir o problema.
  
## <a name="error-code-450-44316-connection-refused"></a>Código de erro: 450 4.4.316 Conexão recusada
<a name="ErrorCode44316"> </a>

Normalmente, esse erro significa que Office 365 encontrou um erro de conexão ao tentar se conectar ao servidor de mensagens de destino. Uma causa provável para este erro é que seu firewall está bloqueando conexões de endereços IP do Office 365. Esse erro pode ser por design, se você tiver migrado completamente seu local mensagens do sistema para o Office 365 e desligar o seu local ambiente de mensagens..
  
- Se você tiver caixas de correio em seu ambiente local, você precisará modificar as configurações de firewall para permitir conexões de endereços de IP do Office 365 na porta TCP 25 para seu local servidores de mensagens. Para obter uma lista dos endereços IP do Office 365, consulte [URLs do Office 365 e intervalos de endereços IP](https://go.microsoft.com/fwlink/p/?linkid=228887).
    
- Se não há mais mensagens devem ser entregues ao seu ambiente local, clique em **corrigir agora** no alerta para que o Office 365 pode rejeitar imediatamente as mensagens com destinatários inválidos. Isso reduzirá o risco de exceder a cota da sua organização para destinatários inválidos, que poderiam afetar a entrega da mensagem normal. Ou então, você pode usar as instruções a seguir para manualmente para corrigir o problema: 
    
  - Desabilitar ou excluir o conector do Office 365 ao seu ambiente local: Centro de administração do Office 365 \> **Admin centrais** \> **Exchange** \> **fluxo de emails** \> **conectores** \> selecione o conector com o valor **do** **Office 365** e o **para** **o servidor de email da sua organização**de valor. Excluir o conector clicando em **Excluir**![ícone Excluir](media/ITPro-EAC-DeleteIcon.png), ou desativar o conector clicando em **Editar**![ícone Editar](media/ITPro-EAC-EditIcon.png) e desmarcando **ativá-lo**.
    
  - Alterar o domínio aceito no Office 365 que está associado ao seu local ambiente de mensagens de **Retransmissão interna** como **autoritativo**. Para obter instruções, consulte [Gerenciar domínios aceitos no Exchange Online](http://technet.microsoft.com/library/0fc0ecc0-e133-48fa-9d72-cb4793a73960.aspx).
    
    **Observação**: geralmente, essas alterações terão entre 30 minutos e uma hora entre em vigor. Após uma hora, verifique se você não é mais recebe o erro.
    
Se o erro for de sua organização parceira (por exemplo, um 3º nuvem serviço provedor de terceiros), será necessário entrar em contato com seu parceiro para corrigir o problema.
  
## <a name="error-code-450-44317-cannot-connect-to-remote-server"></a>Código de erro: 450 4.4.317 não é possível conectar ao servidor remoto
<a name="ErrorCode44317"> </a>

Normalmente, esse erro significa o Office 365 é conectado ao servidor de mensagens de destino, mas o servidor respondeu com um erro imediato ou não cumprir os requisitos de conexão. Detalhes do erro explicará o problema. Por exemplo:
  
- O servidor de mensagens de destino respondeu com um erro "Serviço não disponível", que indica que o servidor é capaz de manter a comunicação com o Office 365.
    
- O conector é configurado para exigir o TLS, mas o servidor de mensagens de destino não oferece suporte a TLS.
    
Verifique as configurações de TLS e certificados em seu local mensagens servidores e as configurações de TLS no conector.
  
Se o erro for de sua organização parceira (por exemplo, um 3º nuvem serviço provedor de terceiros), será necessário entrar em contato com seu parceiro para corrigir o problema.
  
## <a name="error-code-450-44318-connection-was-closed-abruptly"></a>Código de erro: 450 4.4.318 Conexão foi fechada abruptamente
<a name="ErrorCode44318"> </a>

Normalmente, esse erro significa o Office 365 está tendo dificuldade para se comunicar com o seu local ambiente de mensagens, portanto a conexão foi abandonada. As causas possíveis desse erro são:
  
- Seu firewall usa regras de exame de pacotes de SMTP e as regras não estão funcionando corretamente.
    
- Seu local no servidor de mensagens não está funcionando corretamente (por exemplo, serviço cai, panes ou poucos recursos no sistema), que está fazendo com que o servidor de tempo limite e fechar a conexão para o Office 365.
    
- Existem problemas de rede entre seu ambiente local e o Office 365. Se o problema persistir, contate a equipe de rede para solucionar o problema.
    
Descobrir qual cenário se aplica a você e faça as correções necessárias.
  
Se o erro for de sua organização parceira (por exemplo, um 3º nuvem serviço provedor de terceiros), será necessário entrar em contato com seu parceiro para corrigir o problema.
  
## <a name="error-code-450-47320-certificate-validation-failed"></a>Código de erro: Falha na validação do certificado de 450 4.7.320
<a name="ErrorCode47320"> </a>

Normalmente, esse erro significa que Office 365 encontrou um erro ao tentar validar o certificado do servidor de mensagens de destino. Detalhes do erro explicará o erro. Por exemplo:
  
- O certificado expirou
    
- Incompatibilidade de assunto do certificado
    
- Certificado não é mais válido
    
Corrija o conector ou o certificado para que as mensagens em fila no Office 365can ser entregues.
  
Se o erro for de sua organização parceira (por exemplo, um 3º nuvem serviço provedor de terceiros), será necessário entrar em contato com seu parceiro para corrigir o problema.
  
## <a name="other-error-codes"></a>Outros códigos de erro
<a name="sectionSection6"> </a>

O Office 365 está tendo mensagens oferecendo de dificuldade para seu local ou o servidor de mensagens de parceiro. Use as informações do **servidor de destino** no erro para examinar o problema em seu ambiente ou modificar o conector se houver um erro de configuração. 
  
Se o erro for de sua organização parceira (por exemplo, um 3º nuvem serviço provedor de terceiros), será necessário entrar em contato com seu parceiro para corrigir o problema.
  


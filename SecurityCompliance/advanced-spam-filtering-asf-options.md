---
title: Opções avançadas de filtragem de spam
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 6/26/2015
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: b286f853-b484-4af0-b01f-281fffd85e7a
ms.collection:
- M365-security-compliance
description: As opções avançadas de filtragem de spam oferecem aos administradores a capacidade de inspecionar vários atributos de conteúdo de uma mensagem. A presença desses atributos em uma mensagem aumenta a pontuação de spam da mensagem (aumentando assim o potencial para que possa ser identificada como spam) ou marcar a mensagem como spam. As propriedades da mensagem específica do alvo das opções ASF, como marcas de HTML e redirecionamento de URL, que são comumente encontrados em mensagens de spam.
ms.openlocfilehash: 0fad573c29c440d69e27b1e70810bf2fc67be164
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/20/2019
ms.locfileid: "30692880"
---
# <a name="advanced-spam-filtering-options"></a>Opções avançadas de filtragem de spam

As opções avançadas de filtragem de spam oferecem aos administradores a capacidade de inspecionar vários atributos de conteúdo de uma mensagem. A presença desses atributos em uma mensagem aumenta a pontuação de spam da mensagem (aumentando assim o potencial para que possa ser identificada como spam) ou marcar a mensagem como spam. As propriedades da mensagem específica do alvo das opções ASF, como marcas de HTML e redirecionamento de URL, que são comumente encontrados em mensagens de spam.
  
Habilitar as opções ASF é uma abordagem agressiva para filtragem de spam e todas as mensagens filtradas por essas opções não podem ser relatadas como falso positivos. Essas mensagens podem ser identificadas por meio de notificações periódicas de spam do usuário final e recuperadas da quarentena de spam. Elas também podem ser identificadas pelo texto de cabeçalho X específico para cada opção ASF e que aparece no cabeçalho de Internet das mensagens nas quais uma opção ASF tenha sido correspondida. Para obter mais informações, consulte [Cabeçalhos de mensagem antispam](anti-spam-message-headers.md).
  
As opções de ASF podem ser definidas sobre, fora ou para o modo de teste ao editar suas políticas de filtro de conteúdo. Para saber mais, confira [Configure your spam filter policies](configure-your-spam-filter-policies.md). O modo de teste não está disponível para a dispersão de **NDR**, **registro SPF: falha grave**, **filtragem de ID de remetente condicional: falha de hardware**e opções de **email em massa** . 
  
> > [!TIP]
> Informações opcionais para ajudar um usuário a ser mais bem sucedido considere habilitar as opções ASF no modo de teste para maximizar o bloqueio de spam com base em seu ambiente. Para clientes com percentagens elevadas de spam para opções ASF específicas, recomendamos que você teste essas opções antes de implementá-las em seu ambiente de produção. >  Recomenda-se que as organizações que se preocupam com phishing ativem as opções **Registro SPF: Opção de** falha grave. 
  
A tabela a seguir, descreve cada opção de filtragem de spam avançada.
  
||||
|:-----|:-----|:-----|
|**Opção de Filtragem de Spam Avançada** <br/> |**Descrição** <br/> |**texto de cabeçalho X** <br/> |
|**Aumentar a seção de Pontuação de Spam** <br/> |Quando habilitadas, essas opções definem o nível de confiança de spam (SCL) de uma mensagem correspondente para 5 ou 6, o que é considerado spam suspeito. A ação executada na mensagem corresponderá às configurações de **Spam** na sua política de filtro de conteúdo.<br/> ||
|Links de imagem para sites remotos  <br/> |Quando essa configuração é habilitada, qualquer mensagem com conteúdo HTML que tenha uma marca IMG vinculada remotamente (por exemplo, usando http) receberá uma pontuação maior de spam.  <br/> |X-CustomSpam: Links de imagem para sites remotos  <br/> |
|Endereço IP numérico na URL  <br/> |Quando essa configuração é habilitada, qualquer mensagem que tenha URLs com base em números (mais frequentemente na forma de um endereço IP) receberá uma pontuação maior de spam.  <br/> |X-CustomSpam: IP numérico na URL  <br/> |
|URL redirecionada para outra porta  <br/> |Quando essa configuração é habilitada, qualquer mensagem que contenha um hiperlink que redireciona o usuário para portas diferentes da porta 80 (porta de protocolo HTTP normal), 8080 (porta alternativa HTTP) ou 443 (porta HTTPS) receberá uma pontuação maior de spam.  <br/> |X-CustomSpam: URL redirecionada para outra porta  <br/> |
|URL para sites da web .biz ou .info  <br/> |Quando essa configuração é habilitada, qualquer mensagem que contenha uma extensão. biz ou. info no corpo de uma mensagem receberá uma pontuação maior de spam.  <br/> |X-CustomSpam: URL para sites .biz ou .info  <br/> |
|**Marcar como Seção de Spam** <br/> |Quando habilitadas, essas opções definem o nível de confiança de spam (SCL) de uma mensagem correspondente como 9, o que é considerado spam determinado. A ação executada na mensagem corresponderá às configurações de **Spam de alta confiança** na sua política de filtro de conteúdo.<br/> ||
|Mensagens vazias  <br/> |Quando essa configuração estiver habilitada, qualquer mensagem em que o corpo e a linha de assunto estão ambos vazios e além disso não possui anexos, será marcada como spam.  <br/> |X-CustomSpam: Mensagem Vazia  <br/> |
|JavaScript ou VBScript em HTML  <br/> |Quando essa configuração estiver habilitada, qualquer mensagem que utilize JavaScript ou Visual Basic Script Edition em HTML será marcada como spam. Estas duas linguagens de script são utilizadas dentro de uma mensagem HTML para automaticamente fazer com que uma ação específica ocorra. O navegador irá analisar e processar o script junto com o resto do documento.  <br/> |X-CustomSpam: Marcas de Javascript ou VBscript em HTML  <br/> |
|Estrutura ou IMarcas da estrutura em HTML  <br/> |Quando essa configuração estiver habilitada, qualquer mensagem que contenha a \<marca HTML frame\> ou \<iframe\> será marcada como spam. Essas marcas são utilizadas em sites da web ou em mensagens  HTML para formatar a página para exibição de texto ou gráfico..  <br/> |X-CustomSpam: IFRAME ou FRAME em HTML  <br/> |
|Marcas de objeto em HTML  <br/> |Quando essa configuração estiver habilitada, qualquer mensagem que \<contenha\> o objeto html tag será marcada como spam. Essa marca HTML permite  que plug-ins ou aplicativos sejam executados em uma janela HTML.  <br/> |X-CustomSpam: Marca de objeto em HTML  <br/> |
|Marcas de inserção em HTML  <br/> |Quando essa configuração estiver habilitada, qualquer mensagem que \<contenha\> a marca HTML embed será marcada como spam. Essa marca HTML permite que diferentes tipos de documentos de tipos de dados variados sejam inseridos em um documento HTML. Exemplos incluem sons, filmes ou imagens.  <br/> |X-CustomSpam: Marca de inserção em HTML  <br/> |
|Marca de Formulároo em HTML  <br/> |Quando essa configuração estiver habilitada, qualquer mensagem que contenha a marca HTML de \<formulário\> será marcada como spam. Essa marca HTML é usada para criar formulários de site. Os anúncios de email geralmente incluem essa marca para solicitar informações do destinatário.  <br/> |X-CustomSpam: Marca Form em HTML  <br/> |
|Erros da web em HTML  <br/> |Quando essa configuração estiver habilitada, qualquer mensagem que contenha um erro da web será marcada como spam. Um erro da web é um gráfico que é projetado para determinar se a página da web ou mensagem de email foi lida. Bugs da web muitas vezes são invisíveis para o destinatário porque normalmente são adicionados a uma mensagem como um gráfico que é tão pequeno quanto um pixel por um pixel. Boletins informativos legítimos também podem utilizar esta técnica, embora muitos considerem isso uma invasão de privacidade.  <br/> |X-CustomSpam: Bug da Web  <br/> |
|Aplicar lista de palavras sensíveis  <br/> |Quando essa configuração estiver habilitada, qualquer mensagem que contenha uma palavra de uma lista de palavras sensíveis será marcada como spam. Utilizar a lista de palavras sensíveis permite um bloqueio fácil das palavras que estão associadas a mensagens potencialmente ofensivas. Algumas destas palavras diferenciam maiúsculas de minúsculas Como administrador, não é possível editar esta lista. Filtragem contra a lista de palavras sensíveis é aplicada ao corpo e ao assunto de uma mensagem.  <br/> |X-CustomSpam: Palavras confidenciais no assunto/corpo  <br/> |
|Registro SPF: falha grave  <br/> |Quando esta configuração estiver habilitada, as mensagens que não passarem na verificação SPF (o que significa que foram enviadas de um endereço de IP não especificado no registro SPF) serão marcadas como spam. Ativar essa configuração é recomendado para organizações que estão preocupadas com recebimento de mensagens de phishing.<br/> <br/>> [!NOTE]
o modo de teste > não está disponível para essa opção.  <br/> |X-CustomSpam: Falha de registro SPF  <br/> |
|Filtragem de ID por remetente condicional: falha grave  <br/> |Quando essa configuração estiver habilitada, qualquer mensagem que contenha uma falha grave de verificação condicional de ID do remetente será marcada como spam. Essa opção combina uma verificação SPF com uma verificação de ID para ajudar a proteger contra os cabeçalhos de mensagem que contenham remetentes forjados.<br/> <br/>> [!NOTE]
o modo de teste > não está disponível para essa opção.  <br/> |X-CustomSpam: Falha de registro SPF  <br/> |
|Backscatter NDR  <br/> |Se você estiver usando o EOP para proteger caixas de correio locais, quando essa configuração estiver habilitada, todas as mensagens de NDR (notificação de falha na entrega legítima) serão entregues ao remetente original, e todas as mensagens de dispersão (NDR ilegítimo) serão marcadas como spam. Se você não habilitar essa configuração, todos os NDRs ainda passarão por filtragem de spam. Nesse caso, a maioria das mensagens legítimas será entregue ao remetente original enquanto algumas, mas não todas, as mensagens de inspersão serão marcadas como spam. No enTanto, as mensagens de dispersão que não estão marcadas como spam não vão para o remetente original, pois ele vai para o remetente falsificado. <br/> <br/> Se você estiver usando o serviço para proteger caixas de correio hospedadas na nuvem do Exchange Online, não é necessário definir essa configuração.  <br/><br/> > [!NOTE]
> Para ambos os cenários (caixas de correio locais e hospedadas na nuvem), também não é necessário habilitar essa configuração para mensagens de saída enviadas por meio do serviço, pois os NDRs que são mensagens de devolução legítimas serão automaticamente detectadas e entregues ao remetente original . o modo de teste > não está disponível para essa opção.           <br/><br/>> [!TIP]
> Dica: para obter mais informações sobre mensagens de dispersão e EOP, confira [mensagens de dispersão e EOP](backscatter-messages-and-eop.md).           | X-CustomSpam: NDR de inspersão  <br/> | | Email em massa  <br/> | Avançada-a filtragem de spam de email em massa foi removida e substituída com as configurações de limite de email e em massa. ConFira [o que é a diferença entre lixo eletrônico e email em massa?](what-s-the-difference-between-junk-email-and-bulk-email.md) e [configure suas políticas de filtro de spam](configure-your-spam-filter-policies.md) para obter mais informações e como configurar o Ings de inserção.  <br/> ||
   


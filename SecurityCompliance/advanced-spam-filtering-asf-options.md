---
title: Opções de filtragem de spam avançadas
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/26/2015
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: b286f853-b484-4af0-b01f-281fffd85e7a
description: Opções de filtragem de spam avançada oferecem aos administradores a capacidade de inspecionar vários atributos de conteúdo de uma mensagem. A presença desses atributos em uma mensagem aumenta a pontuação de spam da mensagem (aumentando o potencial para que ele seja identificado como spam) ou marca a mensagem como spam. As opções de ASF direcionar as propriedades de mensagem específica, como marcas HTML e o redirecionamento de URL, que costumam ser encontradas nas mensagens de spam.
ms.openlocfilehash: 9a372d002717eacf9470b11b65c4b8f268f48e5a
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23003060"
---
# <a name="advanced-spam-filtering--options"></a>Opções de filtragem de spam avançadas

Opções de filtragem de spam avançada oferecem aos administradores a capacidade de inspecionar vários atributos de conteúdo de uma mensagem. A presença desses atributos em uma mensagem aumenta a pontuação de spam da mensagem (aumentando o potencial para que ele seja identificado como spam) ou marca a mensagem como spam. As opções de ASF direcionar as propriedades de mensagem específica, como marcas HTML e o redirecionamento de URL, que costumam ser encontradas nas mensagens de spam.
  
Habilitar as opções ASF é uma abordagem agressiva para filtragem de spam e todas as mensagens filtradas por essas opções não podem ser relatadas como falso positivos. Essas mensagens podem ser identificadas por meio de notificações periódicas de spam do usuário final e recuperadas da quarentena de spam. Elas também podem ser identificadas pelo texto de cabeçalho X específico para cada opção ASF e que aparece no cabeçalho de Internet das mensagens nas quais uma opção ASF tenha sido correspondida. Para obter mais informações, consulte [Cabeçalhos de mensagem antispam](anti-spam-message-headers.md).
  
Opções de ASF podem ser definidas no, desativar ou para o modo de teste quando você edita suas políticas de filtro de conteúdo. Para obter mais informações, consulte [configurar suas políticas de filtro de spam](configure-your-spam-filter-policies.md). Modo de teste não está disponível para o **backscatter NDR**, **registro SPF: falha grave**, **a filtragem de ID de remetente condicional: falha grave**e as opções de **email em massa** . 
  
> [!TIP]
>  Considere habilitar suas opções de ASF no modo de teste, a fim de maximizar o bloqueio de spam baseado em seu ambiente. Para clientes com percentagens elevadas de spam para opções ASF específicas, recomendamos que você teste essas opções antes de implementá-las em seu ambiente de produção. >  Recomenda-se que as organizações que se preocupam com phishing ativem as opções **Registro SPF: Opção de** falha grave. 
  
A tabela a seguir, descreve cada opção de filtragem de spam avançada.
  
||||
|:-----|:-----|:-----|
|**Opção de Filtragem de Spam Avançada** <br/> |**Descrição** <br/> |**texto de cabeçalho X** <br/> |
|**Aumentar a seção de Pontuação de Spam** <br/> |Quando habilitadas, essas opções definem o nível de confiança de spam (SCL) de uma mensagem correspondente para 5 ou 6, o que é considerado spam suspeito. A ação executada na mensagem corresponderá às configurações de **Spam** na sua política de filtro de conteúdo.<br/> ||
|Links de imagem para sites remotos  <br/> |Quando essa configuração estiver habilitada, qualquer mensagem com conteúdo HTML que tem uma tag IMG que vincula remotamente (por exemplo, usando http) receberá uma pontuação maior de spam.  <br/> |X-CustomSpam: Links de imagem para sites remotos  <br/> |
|Endereço IP numérico na URL  <br/> |Quando essa configuração estiver habilitada, qualquer mensagem que possua URLs numéricas (mais frequente na forma de um endereço IP) receberá uma pontuação maior de spam.  <br/> |X-CustomSpam: IP numérico na URL  <br/> |
|URL redirecionada para outra porta  <br/> |Quando essa configuração estiver habilitada, qualquer mensagem que contém um hiperlink que redireciona o usuário para as portas diferente, a porta 80 (porta de protocolo HTTP regular,) 8080 (porta alternativa de HTTP) ou 443 (HTTPS porta) receberá uma pontuação maior de spam.  <br/> |X-CustomSpam: URL redirecionada para outra porta  <br/> |
|URL para sites da web .biz ou .info  <br/> |Quando essa configuração estiver habilitada, qualquer mensagem que possua uma extensão Biz ou no corpo de uma mensagem receberá uma pontuação maior de spam.  <br/> |X-CustomSpam: URL para sites .biz ou .info  <br/> |
|**Marcar como Seção de Spam** <br/> |Quando habilitadas, essas opções definem o nível de confiança de spam (SCL) de uma mensagem correspondente como 9, o que é considerado spam determinado. A ação executada na mensagem corresponderá às configurações de **Spam de alta confiança** na sua política de filtro de conteúdo.<br/> ||
|Mensagens vazias  <br/> |Quando essa configuração estiver habilitada, qualquer mensagem em que o corpo e a linha de assunto estão ambos vazios e além disso não possui anexos, será marcada como spam.  <br/> |X-CustomSpam: Mensagem Vazia  <br/> |
|JavaScript ou VBScript em HTML  <br/> |Quando essa configuração estiver habilitada, qualquer mensagem que utilize JavaScript ou Visual Basic Script Edition em HTML será marcada como spam. Estas duas linguagens de script são utilizadas dentro de uma mensagem HTML para automaticamente fazer com que uma ação específica ocorra. O navegador irá analisar e processar o script junto com o resto do documento.  <br/> |X-CustomSpam: Marcas de Javascript ou VBscript em HTML  <br/> |
|Estrutura ou IMarcas da estrutura em HTML  <br/> |Quando essa configuração estiver habilitada, qualquer mensagem que contém o \<quadro\> ou \<IFrame\> marca HTML será marcada como spam. Essas marcas são usadas em sites ou em mensagens HTML para formatar a página para exibir texto ou elementos gráficos.  <br/> |X-CustomSpam: IFRAME ou FRAME em HTML  <br/> |
|Marcas de objeto em HTML  <br/> |Quando essa configuração estiver habilitada, qualquer mensagem que contém o \<objeto\> marca HTML será marcada como spam. Nesta marca HTML permite plug-ins ou aplicativos a serem executados em uma janela HTML.  <br/> |X-CustomSpam: Marca de objeto em HTML  <br/> |
|Marcas de inserção em HTML  <br/> |Quando essa configuração estiver habilitada, qualquer mensagem que contém o \<Embed\> marca HTML será marcada como spam. Nesta marca HTML permite que os diferentes tipos de documentos de diversos tipos de dados para ser incorporado em um documento HTML. Exemplos incluem sons, filmes ou imagens.  <br/> |X-CustomSpam: Marca de inserção em HTML  <br/> |
|Marca de Formulároo em HTML  <br/> |Quando essa configuração estiver habilitada, qualquer mensagem que contém o \<formulário\> marca HTML será marcada como spam. Nesta marca HTML é usada para criar formulários de sites. Anúncios de email geralmente incluem nesta marca para solicitar informações do destinatário.  <br/> |X-CustomSpam: Marca Form em HTML  <br/> |
|Erros da web em HTML  <br/> |Quando essa configuração estiver habilitada, qualquer mensagem que contenha um erro da web será marcada como spam. Um erro da web é um gráfico que é projetado para determinar se a página da web ou mensagem de email foi lida. Bugs da web muitas vezes são invisíveis para o destinatário porque normalmente são adicionados a uma mensagem como um gráfico que é tão pequeno quanto um pixel por um pixel. Boletins informativos legítimos também podem utilizar esta técnica, embora muitos considerem isso uma invasão de privacidade.  <br/> |X-CustomSpam: Bug da Web  <br/> |
|Aplicar lista de palavras sensíveis  <br/> |Quando essa configuração estiver habilitada, qualquer mensagem que contenha uma palavra de uma lista de palavras sensíveis será marcada como spam. Utilizar a lista de palavras sensíveis permite um bloqueio fácil das palavras que estão associadas a mensagens potencialmente ofensivas. Algumas destas palavras diferenciam maiúsculas de minúsculas Como administrador, não é possível editar esta lista. Filtragem contra a lista de palavras sensíveis é aplicada ao corpo e ao assunto de uma mensagem.  <br/> |X-CustomSpam: Palavras confidenciais no assunto/corpo  <br/> |
|Registro SPF: falha grave  <br/> |Quando esta configuração estiver habilitada, as mensagens que não passarem na verificação SPF (o que significa que foram enviadas de um endereço de IP não especificado no registro SPF) serão marcadas como spam. Ativar essa configuração é recomendado para organizações que estão preocupadas com recebimento de mensagens de phishing.<br/> **Observação:** O modo de teste não está disponível para esta opção.  <br/> |X-CustomSpam: Falha de registro SPF  <br/> |
|Filtragem de ID por remetente condicional: falha grave  <br/> |Quando essa configuração estiver habilitada, qualquer mensagem que contenha uma falha grave de verificação condicional de ID do remetente será marcada como spam. Essa opção combina uma verificação SPF com uma verificação de ID para ajudar a proteger contra os cabeçalhos de mensagem que contenham remetentes forjados.<br/> **Observação:** O modo de teste não está disponível para esta opção.  <br/> |X-CustomSpam: Falha de registro SPF  <br/> |
|Backscatter NDR  <br/> |Se você estiver usando o EOP para proteger as caixas de correio local, quando essa configuração estiver habilitada, todas as mensagens de NDR legítimo de entrega (NDR) são entregues ao remetente original e todas as mensagens de backscatter (ilegítimas NDR) serão marcadas como spam. Se você não habilitar essa configuração, ainda vá NDRs todos por meio de filtragem de spam. Nesse caso, mensagens mais legítimas receberá entregue ao remetente original enquanto alguns, mas não todos, mnsagens serão obtido marcadas como spam. No entanto, mnsagens que não são marcadas como spam não vão ao remetente original, porque ele irão para o remetente falsificado.<br/> Se você estiver usando o serviço para proteger as caixas de correio Exchange Online hospedado na nuvem, você não precisará definir essa configuração.  <br/> > [!NOTE]> Para ambos os cenários (no local e caixas de correio hospedadas em nuvem), também não é necessário habilitar essa configuração para mensagens de saída enviadas através do serviço, como os NDRs legítima rejeição mensagens serão automaticamente detectadas e entregue original remetente. > Modo de teste de não está disponível para essa opção.           > [!TIP]> Para obter mais informações sobre mensagens backscatter e EOP, consulte [mnsagens backscatter e EOP](backscatter-messages-and-eop.md).           |X-CustomSpam: Notificação de falha na entrega - Backscatter  <br/> |
|Email em Massa  <br/> |Filtragem de spam avançadas de email em massa foi desativado e substituído com as configurações de limite em massa e email. Fazer check-out [qual é a diferença entre lixo eletrônico e email em massa?](what-s-the-difference-between-junk-email-and-bulk-email.md) e [configurar suas políticas de filtro de spam](configure-your-spam-filter-policies.md) para obter mais informações e como definir as configurações.<br/> ||
   


---
title: Usar regras de transporte para configurar a filtragem de email em massa
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/20/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 2889c82e-fab0-4e85-87b0-b001b2ccd4f7
description: Você pode definir filtros de conteúdo de toda a empresa para e-mails de spam e em massa usando as políticas de filtro de conteúdo de spam padrão. Confira configurar suas políticas de filtro de spam e Set-HostedContentFilterPolicy sobre como configurar as políticas de filtro de conteúdo.
ms.openlocfilehash: 8fa4ba619b55ae12207f36b7625acfaa9838e696
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002464"
---
# <a name="use-transport-rules-to-configure-bulk-email-filtering"></a>Usar regras de transporte para configurar a filtragem de email em massa

Você pode definir filtros de conteúdo de toda a empresa para e-mails de spam e em massa usando as políticas de filtro de conteúdo de spam padrão. Confira [configurar suas políticas de filtro de spam](configure-your-spam-filter-policies.md) e [Set-HostedContentFilterPolicy](http://technet.microsoft.com/library/f597aa65-baa7-49d0-8832-2a300073f211.aspx) sobre como configurar as políticas de filtro de conteúdo. 
  
Se você quiser mais opções para filtrar mensagens em massa, você pode criar regras de transporte do Exchange para procurar padrões de texto ou frases frequentemente encontradas em emails em massa. Qualquer mensagem que contém essas duas características será marcada como spam. Usar essas regras pode ajudar a reduzir a quantidade de email em massa indesejados que recebe de sua organização.
  
> [!NOTE]
> Antes de criar as regras de transporte documentados neste tópico, recomendamos que você leia primeiro [qual é a diferença entre lixo eletrônico e email em massa?](what-s-the-difference-between-junk-email-and-bulk-email.md) e [valores de nível de reclamações em massa](bulk-complaint-level-values.md). 
  
> [!NOTE]
> Os procedimentos a seguir marcar uma mensagem como spam para toda sua organização. No entanto, você pode adicionar outra condição para aplicar essas regras apenas a destinatários específicos na sua organização. Dessa forma, o email em massa agressivo filtragem de configurações pode ser aplicadas a alguns usuários que são altamente direcionados, enquanto o restante de seus usuários (que principalmente obter email em massa que eles se inscreveu no) não são afetados. 
  
### <a name="create-an-exchange-transport-rule-to-filter-bulk-email-messages-based-on-text-patterns"></a>Criar uma regra de transporte do Exchange para filtrar mensagens de email em massa com base em padrões de texto

1. No Centro de administração do Exchange (EAC), vá para **Fluxo de emails** \> **Regras**.
    
2. Clique em **Adicionar**![Ícone Adicionar](media/ITPro-EAC-AddIcon.gif) e selecione **Criar uma nova regra**.
    
3. Especifique um nome para a regra.
    
4. Clique em **mais opções**. Em **Aplicar esta regra se**, selecione **o assunto ou corpo** \> **assunto ou corpo corresponde a esses padrões de texto**.
    
5. Na caixa de diálogo **especificar palavras ou expressões**, adicione, uma de cada vez, as seguintes expressões regulares que são normalmente encontradas em emails em massa e clique em **ok** quando tiver concluído: 
    
  - Se não puder ver o conteúdo desse email\,
    
  - \\>cancele sua inscrição( aqui)?( com segurança)?\\</a\\>
    
  - Se não quiser receber mais comunicações como esta\,
    
  - \\<img height\="?1"? width\="?1"? src\=.?http\://
    
  - Para parar de receber esses+emails\:http\://
    
  - Para cancelar a assinatura de \w+ (f\-?letter | e?-?mail | newsletter)
    
  - não (deseja )mais?(receber|ver) \w+ email
    
  - Se não puder ver o conteúdo desse email\, clique aqui
    
  - Para garantir o recebimento de (ofertas diárias|nossos e-?mails)\, adicione
    
  - Se não quiser mais receber esses emails
    
  - para alterar (preferências de inscrição|preferências or cancelar inscrição)
    
  - clique (aqui para|em) cancelar a inscrição
    
    **Observações**:
    
  - A lista acima não é um conjunto exaustiva de expressões regulares encontradas em emails em massa; mais podem ser adicionados ou removidos conforme necessário. No entanto, é um bom ponto de partida.
    
  - A pesquisa por palavras ou padrões de texto no assunto ou outros campos de cabeçalho na mensagem ocorre *depois que* a mensagem tem sido decodificada desde a transferência de conteúdo MIME método que foi usado para transmitir a mensagem binária entre os servidores SMTP texto ASCII de codificação. Você não pode usar as condições ou exceções para pesquisar o raw (geralmente, Base64) codificado valores do assunto ou outros campos de cabeçalho nas mensagens. 
    
6. Em **Execute a ação a seguir**, selecione **Modificar as propriedades da mensagem** \> **definir o SCL (nível de confiança de spam)**.
    
7. Na caixa de diálogo **especificar SCL**, defina o SCL como **5**, **6** ou **9** e clique em **ok**.
    
    Definir o SCL como 5 ou 6 executará a ação de **Spam** , durante a configuração do SCL para 9 leva a ação de **spam de alta confiança** , conforme configurado na política de filtro de conteúdo. O serviço executará a ação definida na política de filtro de conteúdo. A ação padrão é entregar a mensagem para a pasta de lixo eletrônico dos destinatários, mas ações diferentes podem ser configuradas conforme descrito em [configurar suas políticas de filtro de spam](configure-your-spam-filter-policies.md).
    
    > [!NOTE]
    > Se sua ação configurada for a mensagem em quarentena em vez de enviá-lo para a pasta de lixo eletrônico dos destinatários, a mensagem será enviada para a quarentena administrador conforme uma correspondência de regra de transporte e ele não estará disponível em quarentena de spam do usuário final ou através de notificações de spam do usuário final. 
  
    Para saber mais sobre os valores de SCL do serviço, veja [Níveis de confiança de spam](spam-confidence-levels.md).
    
8. Salve a regra.
    
### <a name="create-an-exchange-transport-rule-to-filter-bulk-email-messages-based-on-phrases"></a>Criar uma regra de transporte do Exchange para filtrar mensagens de email em massa com base em frases

1. No EAC, vá para **Fluxo de emails** \> **Regras**.
    
2. Clique em **Adicionar**![Ícone Adicionar](media/ITPro-EAC-AddIcon.gif) e selecione **Criar uma nova regra**.
    
3. Especifique um nome para a regra.
    
4. Clique em **mais opções**. Em **Aplicar esta regra se**, selecione **o assunto ou corpo** \> **assunto ou corpo inclui qualquer uma destas palavras**.
    
5. Na caixa de diálogo **especificar palavras ou expressões**, adicione, uma de cada vez, as seguintes frases comuns encontradas em emails em massa e clique em **ok** quando tiver concluído: 
    
  - para alterar suas preferências ou cancelar a assinatura
    
  - Alterar as preferências de email ou cancelar a assinatura
    
  - Este é um email promocional
    
  - Você está recebendo este email porque solicitou uma assinatura
    
  - clique aqui para cancelar a assinatura
    
  - Você recebeu este email porque se inscreveu em
    
  - Se não quiser mais receber nosso boletim informativo por email
    
  - para cancelar a assinatura desse boletim informativo
    
  - Se tiver problema para ver este email
    
  - Isto é um anúncio
    
  - você gostaria de cancelar a assinatura ou alterar sua
    
  - ver este email como uma página da Web
    
  - Você está recebendo este email porque se inscreveu em
    
    **Observação**: mais uma vez, esta lista não é um conjunto exaustiva de frases encontradas em emails em massa; mais podem ser adicionados ou removidos conforme necessário. No entanto, é um bom ponto de partida.
    
6. Em **Execute a ação a seguir**, selecione **Modificar as propriedades da mensagem** \> **definir o SCL (nível de confiança de spam)**.
    
7. Na caixa de diálogo **especificar SCL**, defina o SCL como **5**, **6** ou **9** e clique em **ok**.
    
    Definir o SCL como 5 ou 6 executará a ação de **Spam** , durante a configuração do SCL para 9 leva a ação de **spam de alta confiança** , conforme configurado na política de filtro de conteúdo. O serviço executará a ação definida na política de filtro de conteúdo. A ação padrão é entregar a mensagem para a pasta de lixo eletrônico dos destinatários, mas ações diferentes podem ser configuradas conforme descrito em [configurar suas políticas de filtro de spam](configure-your-spam-filter-policies.md).
    
    > [!NOTE]
    > Se sua ação configurada for a mensagem em quarentena em vez de enviá-lo para a pasta de lixo eletrônico dos destinatários, a mensagem será enviada para a quarentena administrador conforme uma correspondência de regra de transporte e ele não estará disponível em quarentena de spam do usuário final ou através de notificações de spam do usuário final. 
  
    Para saber mais sobre os valores de SCL do serviço, veja [Níveis de confiança de spam](spam-confidence-levels.md).
    
8. Salve a regra.
    
## <a name="for-more-information"></a>Para obter mais informações

[Qual é a diferença entre lixo eletrônico e email em massa?](what-s-the-difference-between-junk-email-and-bulk-email.md)
  
[Valores de nível compatível com dados em massa](bulk-complaint-level-values.md)
  
[Configurar suas políticas de filtro de spam](configure-your-spam-filter-policies.md)
  
[Opções de filtragem de spam avançadas](advanced-spam-filtering-asf-options.md)
  


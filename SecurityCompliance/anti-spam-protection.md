---
title: Proteção antispam de emails do Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 6a601501-a6a8-4559-b2e7-56b59c96a586
description: Saiba mais sobre as configurações de recursos anti-spam e os filtros que irão ajudar que você impedir spam no Exchange Online e o Office 365. Obtendo uma quantidade excessiva de spam no Office 365? Você pode personalizar seus filtros de spam e configurações de política anti-spam.
ms.openlocfilehash: 0a23ddd0610599bbd6478781c61e5e32b06726bc
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29652266"
---
# <a name="office-365-email-anti-spam-protection"></a>Proteção antispam de emails do Office 365

Você está preocupado muito spam no Office 365? Criamos vários filtros de spam em seu serviço do Office 365 ou Exchange Online Protection (EOP), para que seu email é protegido a partir do momento em que você recebe a primeira mensagem. Para ajudar a evitar spam no Office 365, talvez você queira alterar uma configuração de proteção para lidar com um problema específico em sua organização — dizer que você está recebendo uma grande quantidade de spam de um remetente específico, por exemplo — ou para simplesmente fino ajustar suas configurações para que sejam adaptados para atender melhor às necessidades da sua organização. Para fazer isso, você pode alterar configurações antispam no Office 365 Security &amp; Centro de conformidade.
  
Este artigo destina-se a administradores do Office 365. Se você não for um administrador, mas você é um usuário do Office 365 e você deseja saber como lidar com spam recebido, isso não é o artigo que você está procurando. Em vez disso, se você usar o Outlook para PC ou o Outlook para Mac, comece com [Visão geral do filtro de lixo eletrônico](https://support.office.com/article/5ae3ea8e-cf41-4fa0-b02a-3b96e21de089). Se você usar o Outlook na web, comece com [Saiba mais sobre lixo eletrônico e phishing](https://support.office.com/article/86c1d76f-4d5a-4967-9647-35665dc17c31).
  
## <a name="these-options-help-you-prevent-spam-in-office-365"></a>Essas opções ajudarão-lo a evitar spam no Office 365

 **Filtragem de Conexão.** Quando você usa a filtragem de conexão, o Office 365 verifica a reputação do remetente antes de permitir que uma mensagem a ser obtido. Você pode criar uma lista de permissões ou lista de remetentes seguros, para certificar-se de que você recebe todas as mensagens enviadas para você, de um endereço IP específico ou intervalo de endereços IP. Você também pode criar uma lista de endereços IP da qual bloquear mensagens, chamadas de uma lista de bloqueios. Para obter mais informações, consulte [Configure a política de filtro de Conexão](https://technet.microsoft.com/library/jj200718%28v=exchg.150%29.aspx). Se você estiver preocupado com spam no Office 365, use a conexão de filtragem para ajudar a impedir spam.
  
Para clientes que têm o Office 365 Enterprise E5 ou adquiriram licenças da proteção de ameaça avançadas (ATP), a filtragem de conexão é usada pelo intelligence falso para criar permitir e bloquear as listas de remetentes que são falsificação de seu domínio. Para obter mais informações, consulte [Saiba mais sobre inteligência de falso](https://go.microsoft.com/fwlink/?LinkID=735009).
  
 **Filtragem de Spam.** O Office 365 verifica as características de mensagem consistentes com spam usando o recurso de filtragem de spam. Você pode alterar quais ações para receber as mensagens identificadas como spam e escolha se deseja filtrar mensagens escritas em idiomas específicos ou enviadas de determinados países ou regiões. Você também pode ativar opções de filtragem, se desejar buscar uma abordagem agressiva para filtragem de spam de spam avançada. Além disso, você pode configurar as notificações de spam do usuário final para informar os usuários quando as mensagens pretendidas que eles foram enviadas para a quarentena em vez disso. (O envio de mensagens para a quarentena é uma das ações configuráveis.) Dessas notificações, os usuários finais podem liberar falsos positivos e indicá-las à Microsoft para análise. Para obter mais informações, consulte [configurar suas políticas de filtro de spam](https://go.microsoft.com/fwlink/p/?LinkId=617147). Para ajudar a evitar spam no Office 365, use a filtragem de spam, se você estiver preocupado com muita spam no Office 365, use para ajudar a impedir spam de filtragem de conexão.
  
> [!NOTE]
> Para clientes do EOP: por padrão, os filtros de spam EOP enviam mensagens de spam detectado para pasta de lixo eletrônico de cada dos destinatários. No entanto, para garantir que a ação de **mover a mensagem para a pasta Lixo eletrônico** funcionará com caixas de correio local, você deve configurar duas regras de transporte do Exchange em seus servidores locais para detectar os cabeçalhos de spam adicionados pelo EOP. Para obter detalhes, consulte [Certifique-se de que o spam é roteado para a pasta de lixo eletrônico de cada usuário](https://technet.microsoft.com/library/jj837173%28v=exchg.150%29.aspx). 
  
## <a name="extra-information-if-you-receive-too-much-spam-in-office-365"></a>Informações extras se você receber uma quantidade excessiva de spam no Office 365

O vídeo a seguir fornece uma visão geral de configuração no EOP de filtragem de spam.
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/608be94c-d763-4c47-af94-99e7cb277713?autoplay=false]
  
Para obter mais detalhes, consulte o tópico [Configure políticas de filtro de spam](https://go.microsoft.com/fwlink/p/?LinkId=617147) .
  
## <a name="check-your-outgoing-messages-to-prevent-spam-in-office-365"></a>Verificar suas mensagens de saída para impedir que o spam no Office 365

 **Filtragem de saída.** O Office 365 também verifica para certificar-se de que os usuários não enviem spam. Por exemplo, o computador de um usuário pode obter infectado com malware que faz com que ele enviar mensagens de spam, por isso criamos proteção contra que chamado a *filtragem de saída* . Você não pode desativar a filtragem de saída, mas você pode definir as configurações que descrito em [Configure a política de spam de saída](https://technet.microsoft.com/library/jj200737%28v=exchg.150%29.aspx). Se você estiver preocupado com muita spam no Office 365, use a filtragem de saída para ajudar a evitar spam no Exchange Online.
  
## <a name="beyond-the-basics-more-ways-to-prevent-spam-in-office-365"></a>Além do básico: outras maneiras de impedir que o spam no Office 365

 **Regras de fluxo de email.** Se quiser ir além de filtragem de spam interna e criar regras personalizadas que são baseados em suas políticas de negócios, *[regras de fluxo de email](https://technet.microsoft.com/library/jj919238%28v=exchg.150%29.aspx)*, também chamadas de *regras de transporte*, são outro filtro que ajudá-lo a evitar spam no Office 365. Por exemplo, você pode usar as regras de fluxo de correio para definir o valor de (SCL) nível do spam confidence para mensagens que correspondam às condições específicas, conforme descrito em [usar regras de fluxo de email para definir o nível de confiança de spam (SCL) em mensagens](https://technet.microsoft.com/library/dn798345%28v=exchg.150%29.aspx).
  
 **Autenticação de email.** Técnicas que usam o sistema de nome de domínio (DNS) para adicionar informações verificáveis às mensagens de email sobre o remetente de uma mensagem de email são chamadas de autenticação de email. Usar o Office 365 mais avançado, os administradores podem fazer desses métodos de autenticação de email:
  
- **(SPF) de estrutura de política do remetente.** SPF valida à origem de mensagens de email, verificando o endereço IP do remetente contra o proprietário denúncia do domínio de envio. Para obter uma introdução rápida SPF e instalá-la configurado rapidamente, consulte [Configurar SPF no Office 365 para ajudar a impedir a falsificação](https://technet.microsoft.com/library/dn789058%28v=exchg.150%29.aspx). Para ter uma compreensão mais detalhada de como o Office 365 usa SPF ou para implantações não-padrão ou de solução de problemas, por exemplo, híbrida, inicie com [como o Office 365 usa Framework de política do remetente (SPF) para evitar a falsificação](https://technet.microsoft.com/library/mt712724%28v=exchg.150%29.aspx).

- **DomainKeys identificado Mail (DKIM).** DKIM permite anexar uma assinatura digital para mensagens de email no cabeçalho da mensagem de emails que você enviar. Sistemas de email que recebam email de seu domínio usam essa assinatura digital para determinar se o email de entrada que eles recebem é legítimo. Para obter informações sobre a verificação e o Office 365, consulte [Verificação de uso para validar emails de saída enviados do seu domínio no Office 365](https://technet.microsoft.com/library/mt695945%28v=exchg.150%29.aspx).

- **Autenticação de mensagens baseada em domínio, relatórios e conformidade (DMARC).** Ajuda do DMARC recebendo sistemas de email determinar o que fazer com mensagens que falham verificações SPF ou DKIM e fornece um outro nível de confiança para seus parceiros de email. Para obter informações sobre como configurar o DMARC, consulte [DMARC de uso para validar emails no Office 365](https://technet.microsoft.com/library/mt734386%28v=exchg.150%29.aspx).

Se você estiver preocupado com spam, phishing e falsificação no Office 365, use SPF, DKIM e DMARC juntos para ajudar a evitar spam e falsificação indesejadas.
  
 **Configurações do usuário final gerenciado.** Se você estiver procurando informações sobre como os usuários finais podem gerenciar suas próprias configurações de spam, consulte [Visão geral do filtro de lixo eletrônico](https://go.microsoft.com/fwlink/?LinkId=270065) (para usuários do Microsoft Outlook) ou [Saiba mais sobre lixo eletrônico e phishing](https://go.microsoft.com/fwlink/?LinkId=270068) (para o Outlook em que os usuários da web). Se você estiver usando o EOP para proteger as caixas de correio local, certifique-se de usar a sincronização de diretórios para garantir que essas configurações são sincronizadas para o serviço. Para obter mais informações sobre como configurar a sincronização de diretórios, consulte "Usar a sincronização de diretórios para gerenciar usuários de email" em [Gerenciar usuários de email no EOP](https://technet.microsoft.com/library/dn636911%28v=exchg.150%29.aspx).
  
## <a name="for-more-information"></a>Para saber mais

[Blog: Por que spam e phishing obtém por meio do Office 365?](https://go.microsoft.com/fwlink/?LinkId=528179 )
  
[Perguntas frequentes sobre a proteção antispam](https://technet.microsoft.com/library/jj937231%28v=exchg.150%29.aspx)
  
[Impedir falsos positivos marcados como spam usando uma lista confiável ou outras técnicas](prevent-email-from-being-marked-as-spam-0.md)
  
[Como configurar a filtragem para ajudar a bloquear mensagens de lixo eletrônico de spam do Office 365](block-email-spam-to-prevent-false-negatives.md)
  
[Qual é a diferença entre lixo eletrônico e Email em massa?](https://technet.microsoft.com/library/dn720441%28v=exchg.150%29.aspx)
  
[Cabeçalhos de mensagem antispam](https://technet.microsoft.com/library/dn205071%28v=exchg.150%29.aspx)
  
[Mnsagens backscatter e EOP](https://technet.microsoft.com/library/dn499795%28v=exchg.150%29.aspx)

## <a name="more-resources"></a>Mais recursos

[Obter ajuda de fóruns da comunidade do Office 365](https://go.microsoft.com/fwlink/p/?LinkId=518605)
  
[Administradores: Entrar e criar uma solicitação de serviço](https://go.microsoft.com/fwlink/p/?LinkId=519124)
  
[Administradores: Ligar para o Suporte](https://go.microsoft.com/fwlink/p/?LinkID=518322)

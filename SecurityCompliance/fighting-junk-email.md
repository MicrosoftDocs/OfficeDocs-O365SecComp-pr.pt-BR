---
title: Combater o lixo eletrônico enviado para o Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 5fd7d05b-96db-456f-81d6-1ac0e5bff530
description: Mapa de segurança de email da Microsoft envolve uma abordagem de entre produtos incomparável. Tecnologia de filtragem anti-spam e antiphishing Exchange Online Protection (EOP) está sendo aplicada em todas as plataformas de email da Microsoft para fornecer aos usuários a últimas ferramentas antispams e anti-phishing e inovações em toda a rede. O objetivo do EOP é oferecer um serviço de email abrangente e utilizáveis que ajuda a detectar e proteger os usuários de lixo eletrônico, ameaças de e-mail fraudulento (phishing) e malware.
ms.openlocfilehash: d4047e373b7808fe4b30dd23a1e7486ee7eb5a66
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002870"
---
# <a name="fighting-junk-email-sent-to-office-365"></a>Combater o lixo eletrônico enviado para o Office 365

Mapa de segurança de email da Microsoft envolve uma abordagem de entre produtos incomparável. Tecnologia de filtragem anti-spam e antiphishing Exchange Online Protection (EOP) está sendo aplicada em todas as plataformas de email da Microsoft para fornecer aos usuários a últimas ferramentas antispams e anti-phishing e inovações em toda a rede. O objetivo do EOP é oferecer um serviço de email abrangente e utilizáveis que ajuda a detectar e proteger os usuários de lixo eletrônico, ameaças de e-mail fraudulento (phishing) e malware.
  
## <a name="the-challenge"></a>O desafio

Email se tornou uma ferramenta importante de comunicação não apenas para os consumidores, mas também para ajudar empresas de todos os tamanhos, a equipe de suporte, organizações de vendas e comerciantes. Como o uso de email cresceu, isso tem mau uso de email. Não monitorado lixo eletrônico pode obstruir caixas de entrada e redes, satisfação de impacto do usuário e dificultar a eficácia das comunicações de emails legítimos. É por isso que a Microsoft continua a investir em tecnologias anti-spam. Em outras palavras, ele começa contendo e filtragem de lixo eletrônico. 
  
## <a name="our-efforts"></a>Nossos esforços

EOP oferece diversas etapas para minimizar o impacto negativo lixo eletrônico tem sobre a experiência de email dos nossos usuários.
  
### <a name="exchange-online-protection-technology"></a>Tecnologia do Exchange Online Protection

Para ajudar a reduzir o lixo eletrônico, EOP inclui a proteção de lixo eletrônico usando tecnologias de filtragem de EOP proprietária email tela para identificar e separar lixo eletrônico de emails legítimos. O filtro de conteúdo do EOP aprende do conhecida spam e phishing ameaças e comentários de usuário de nossa plataforma de consumidor, Outlook.com. Esses tipos de dados ajudar no treinamento tecnologias EOP reconhecer lixo eletrônico e email legítimo e são principais entradas em reputação do remetente. Em andamento comentários de usuários EOP no programa de classificação de lixo eletrônico ajuda a garantir que as tecnologias EOP são treinadas e aprimoradas continuamente.
  
#### <a name="how-does-eop-work"></a>Como o EOP funciona?

Quando um usuário externo envia uma mensagem de email a um usuário do EOP, tecnologias de filtragem do EOP avaliar o conteúdo da mensagem e atribui uma classificação à mensagem com base na probabilidade que a mensagem é lixo eletrônico. Essa classificação é armazenada como uma propriedade de mensagem chamada um nível de confiança de Spam (SCL) dentro da mensagem em si. A classificação SCL permanece com a mensagem como ele é enviado a outras camadas de proteção antispam no EOP. 
  
Regras de EOP estão definidas para lidar com as mensagens de email com várias classificações de SCL. Se uma mensagem tiver uma classificação de SCL maior do que um determinado limite, ele será considerado spam. A mensagem será colocada em quarentena ou entregue para a pasta de lixo eletrônico do usuário dependendo de como o administrador do sistema configura a opção de entrega de spam.
  
#### <a name="eop-filters"></a>Filtros do EOP

As tecnologias de filtragem de antispam, além de EOP também proporciona ao administrador do sistema a capacidade de definir os níveis de filtro para personalizar a entrega de email para suas contas de usuário. Os administradores podem facilmente adicionar um remetente ou nome de domínio para a lista de domínios e de remetentes confiáveis, para que o email desse remetente ou domínio nunca é tratado como lixo eletrônico, independentemente do conteúdo da mensagem. Para obter informações, consulte [Remetentes seguros e bloqueados listas de remetentes no Exchange Online](safe-sender-and-blocked-sender-lists-faq.md).
  
### <a name="phishing-protection"></a>Proteção contra phishing

O phishing (pronuncia-se "phishing") é um formulário de roubo de identidade e uma das ameaças mais rápido crescimento na Internet. Geralmente, você pode identificar uma mensagem de phishing quando ele solicita informações pessoais ou financeiras ou inclui um link para um site que solicite tais informações. EOP oferece proteção contra phishing como parte das tecnologias de filtragem EOP proprietárias. Tecnologias de filtragem do EOP analisam o email para ajudar a detectar links fraudulentos ou domínios falsificados para ajudar a proteger os usuários contra esses tipos de golpes on-line.
  
#### <a name="how-does-phishing-protection-work"></a>Como funciona a proteção contra phishing?

Geralmente um email de phishing será enviado contendo um link, uma vez clicado no link redireciona os usuários para um site fraudulento exibida válido (como seu instituição financeira ou serviço on-line). Este site de phishing geralmente solicita que os usuários insiram as informações pessoais, como nomes de usuário, senhas e números de seguridade social. Qualquer informação digitada no site de phishing ajuda o phisher roubar sua identidade. Usando nomes de marca confiáveis conhecidos e logotipos, phishers são capazes de parecer legítimo. Tecnologia de filtro de phishing oferecidas no EOP verifica as características de phishing possíveis em email. Se encontrado, o email é movido para a pasta Lixo eletrônico.
  
Microsoft está concentrando os esforços de tecnologia antiphishing em dois aspectos: primeiro, ajudando a impedir que as mensagens de email de phishing atinja nossos usuários e a segunda, ajudando a eliminar a possibilidade de usuários que está sendo enganado por emails falsificados e sites da web. 
  
> [!TIP]
> Internet Explorer versão 7 e acima será bloquear ou avisar aos usuários quando eles visitam conhecidos ou sites de phishing em potencial para que eles não são levados a fornecer informações pessoais. [Verifique se você tem a versão mais recente do Internet Explorer](https://www.microsoft.com/windows/ie/default.mspx). 
  
#### <a name="authentication"></a>Autenticação

Falsificação de domínio é uma maneira de imitar um endereço de email legítimo para fazer com que o e-mail fraudulento pareça legítimo. Falsificação é usada pelo mal-intencionado pessoas ou organizações em golpes de phishing para atrair pessoas a divulgar informações pessoais confidenciais. Divulgação de informações pode levar a identificar roubo e outros tipos de fraude.
  
EOP usa Framework de proteção do remetente (SPF), DomainKeys identificado Mail (DKIM) e a autenticação baseada em domínio de mensagens, relatórios e conformidade (DMARC) e outras autenticações implícitas para verificar que a mensagens provenientes do domínio que dizem ser originadas de . Recomendamos que todos os remetentes usam SPF e DKIM para proteger seus destinatários de lixo eletrônico e golpes de phishing. Recomendamos remetentes considere um DMARC para rejeitar ou colocar em quarentena mensagens enviadas de remetentes não autorizados de publicação.
  
- Para saber mais sobre SPF, consulte [RFC 7208](https://tools.ietf.org/html/rfc7208) e [Estrutura de política do remetente](http://www.openspf.org/).
    
- Para saber mais sobre DKIM, consulte [RFC 6376](https://tools.ietf.org/html/rfc6376) e [DKIM.org](http://dkim.org/).
    
- Para saber mais sobre DMARC, consulte [DMARC.org](https://dmarc.org/).
    
### <a name="legislation"></a>Legislação

Na Microsoft, podemos acredite que o desenvolvimento de novas tecnologias e Autoregulamentação requer o suporte da política do governo efetiva e estruturas de legais. A proliferação de spam em todo o mundo tem spurred vários corpos legislativas para regular emails comerciais. Muitos países/regiões agora ter contra os spams leis in-loco. Estados Unidos possui leis federais e estaduais orientando spam e essa abordagem complementar é ajudar a diminuir o spam, permitindo a criação de comércio legítimo prosperar. O ato de SPAM CAN expande as ferramentas disponíveis para restrição aos emails fraudulentos e falsos.
  


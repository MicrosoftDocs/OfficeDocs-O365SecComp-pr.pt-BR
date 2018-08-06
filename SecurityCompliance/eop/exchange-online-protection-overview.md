---
title: Visão geral do Exchange Online Protection
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 1270a65f-ddc3-4430-b500-4d3a481efb1e
description: O Microsoft Proteção do Exchange Online (EOP) é um serviço de filtragem de e-mails baseado na nuvem que ajuda a proteger sua organização contra spam e malware, e inclui recursos para defender sua organização das violações da política de mensagens.
ms.openlocfilehash: 89852c7ba211ccb266c8b231b00d3d83987a5f20
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026688"
---
# <a name="exchange-online-protection-overview"></a>Visão geral do Exchange Online Protection

O Microsoft Proteção do Exchange Online (EOP) é um serviço de filtragem de email com base na nuvem que ajuda a proteger sua organização contra spam e malware e inclui recursos para proteger sua organização contra violações da política de envio de mensagens. O EOP pode simplificar o gerenciamento de seu ambiente de mensagens e aliviar muitos dos fardos que acompanham a manutenção de hardware e software locais.
  
Veja a seguir algumas das principais formas de usar o EOP para proteção de mensagens:
  
- **Em um cenário autônomo** EOP fornece proteção de email baseada em nuvem para seu ambiente do Microsoft Exchange Server 2013 local, versões herdadas do Exchange Server, ou para qualquer outro local a solução de email SMTP. 
    
- **Como parte do Microsoft Exchange Online** Por padrão, o EOP protege caixas de correio do Microsoft Exchange Online hospedadas na nuvem. 
    
- **Em uma implantação híbrida** O EOP pode ser configurado para proteger seu ambiente de mensagens e controlar o roteamento de email quando você tem uma combinação de caixas de correio locais e na nuvem. 
    
## <a name="how-eop-works"></a>Como o EOP funciona

Para entender como o EOP funciona, ele o ajuda a ver como processa o email de entrada:
  
![Processamento de email do EOP](../media/EOP-email-processing.png)
  
Mensagem recebida inicialmente passa por meio de filtragem de conexão, que verifica a reputação do remetente e inspeciona a mensagem para o malware. A maioria dos spam é interrompida nesse momento e excluída pelo EOP. Mensagens continuam pela filtragem de política, onde as mensagens são avaliadas pelas regras de transporte personalizado que você cria ou impor a partir de um modelo. Por exemplo, você pode ter uma regra que envia uma notificação para um gerente quando um email chega de um remetente específico. (Verificações de prevenção de perda de dados também ocorrem neste ponto, se você tiver que apresentam; para obter informações sobre disponibilidade de recurso, consulte o [Exchange Online Protection Service Description](https://go.microsoft.com/fwlink/p/?LinkId=320619).) Em seguida, mensagens que passam por meio de filtragem de conteúdo, onde o conteúdo é verificado de terminologia ou propriedades comuns como spam. Uma mensagem é determinado como spam pelo filtro de conteúdo pode ser enviada para a pasta de lixo eletrônico do usuário ou para a quarentena, entre outras opções, com base em suas configurações. Depois que uma mensagem passa todas essas camadas de proteção com êxito, ele é entregue ao destinatário.
  
### <a name="eop-datacenters"></a>Datacenters EOP

O EOP é executado em uma rede mundial de data center projetados para fornecer a melhor disponibilidade. Por exemplo, se um data center ficar indisponível, mensagens de email são automaticamente roteadas para um outro data center sem qualquer interrupção no serviço. Os servidores em cada data center aceitam mensagens em seu nome, fornecendo uma camada de separação entre sua organização e a Internet, reduzindo assim a carga em seus servidores. Por meio dessa rede altamente disponível, a Microsoft pode assegurar que esse email chegue a sua organização pontualmente. 
  
EOP realiza balanceamento de carga entre data centers, mas apenas dentro de uma região. Se você for aprovisionado em uma região, todas as suas mensagens serão processadas usando o roteamento de email para essa região. A lista a seguir mostra como o roteamento de email regional funciona para os data centers EOP:
  
- Nos América, todos os Exchange on-line caixas postais estejam localizadas em datacenters EUA, com exceção da América do Sul onde datacenters no Brasil e Chile são usados e no Canadá, onde os centros de dados no Canadá são usados. Todas as mensagens de email, incluindo mensagens para clientes na América do Sul e no Canadá, são roteadas através dos EUA datacenters para filtragem do EOP; No entanto, quaratined email é armazenado no datacenter onde se encontra o inquilino..
    
- Na Europa, Oriente Médio e África (EMEA), todas as caixas de correio do Exchange Online são localizadas nos data centers da EMEA e todas as mensagens são roteadas através de data centers da EMEA para filtragem do EOP.
    
- Na Ásia Pacífico (APAC), todas as caixas de correio do Exchange Online estão localizadas em datacenters da APAC, mas as mensagens são atualmente roteadas através de datacenters da EMEA para filtragem do EOP. Tem-se o objetivo de mudar isso no quarto trimestre de 2014, quando as mensagens serão roteadas através de datacenters da APAC para a filtragem do EOP.
    
- Para a Nuvem de Comunidade Governamental (GCC), todas as caixas de correio do Exchange Online localizadas em data centers dos EUA e todas as mensagens são roteadas através de data centers dos EUA para filtragem do EOP.
    
## <a name="eop-plans-and-features"></a>Planos e recursos do EOP

Estes são os planos de assinatura disponíveis do EOP:
  
- **EOP autônomo** No qual o EOP protege suas caixas de correio locais. 
    
- **Recursos do EOP no Exchange Online** No qual o EOP protege suas caixas de correio do Exchange Online hospedadas na nuvem. 
    
- **Exchange Enterprise CAL com serviços** Em que EOP protege suas caixas de correio locais, como o EOP autônomo, e inclui DLP (prevenção de perda de dados) e relatórios usando serviços da Web. 
    
Para mais informações sobre as exigências, limites importantes e disponibilidade de recursos em todos os planos de assinatura do EOP, consulte a [Descrição do serviço de proteção do Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=320619).
  
## <a name="setting-up-eop"></a>Configuração do EOP

A configuração do EOP pode ser simples, especialmente no caso de uma pequena organização com um punhado de regras de conformidade. No entanto, se você tiver uma organização de grande porte com vários domínios, regras de conformidade personalizadas ou fluxo de email híbrido, a configuração pode precisar de mais planejamento e tempo.
  
Se você já comprou o EOP, consulte [Configurar seu serviço EOP](set-up-your-eop-service.md) para garantir a conclusão de todas as etapas necessárias de configuração do EOP, a fim de proteger seu ambiente de mensagens. 
  
## <a name="for-more-information"></a>Para obter mais informações

[Recursos EOP](eop-features.md)
  
[Vídeos de introdução ao EOP](videos-for-getting-started-with-eop.md)
  
[Perguntas frequentes gerais sobre o EOP](eop-general-faq.md)
  
[Perguntas frequentes sobre mensagens enfileiradas, adiadas e retornadas do EOP](eop-queued-deferred-and-bounced-messages-faq.md)
  
[Perguntas frequentes sobre administração delegada](delegated-administration-faq.md)
  
[Mover domínios e configurações de uma organização do EOP para outra organização do EOP](move-domains-and-settings-from-one-eop-organization-to-another-eop-organization.md)
  


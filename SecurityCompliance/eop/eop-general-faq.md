---
title: Perguntas frequentes gerais sobre o EOP
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/2/2018
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 9dbff00a-474e-4452-aeb5-5be9a6b8c6d5
description: 'Aqui, respondemos às dúvidas gerais mais comuns sobre o Proteção do Exchange Online (EOP), o serviço de filtragem de email hospedado na nuvem da Microsoft. Para ver mais tópicos de perguntas frequentes, vá para os seguintes links:'
ms.openlocfilehash: 00618618d251e1478cb0dc0a0fbb116db2565fad
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693190"
---
# <a name="eop-general-faq"></a>Perguntas frequentes gerais sobre o EOP

Aqui, respondemos às dúvidas gerais mais comuns sobre o Proteção do Exchange Online (EOP), o serviço de filtragem de email hospedado na nuvem da Microsoft. Para ver mais tópicos de perguntas frequentes, vá para os seguintes links:
  
- [Perguntas frequentes sobre mensagens enfileiradas, adiadas e retornadas do EOP](eop-queued-deferred-and-bounced-messages-faq.md)
    
- [Perguntas frequentes sobre administração delegada](delegated-administration-faq.md)
    
- [PERGUNTAS FREQUENTEs sobre proteção antispam](../anti-spam-protection-faq.md)
    
- [Listas de remetentes seguros e remetentes bloqueados no Exchange Online](../safe-sender-and-blocked-sender-lists-faq.md)
    
- [Quarantine FAQ](../quarantine-faq.md)
    
- [PERGUNTAS FREQUENTEs sobre proteção contra malware](../anti-malware-protection-faq-eop.md)
    
- [Message Trace FAQ](http://technet.microsoft.com/library/aa49e3f9-a5b1-4410-aac2-ddbbf3f5bfb2.aspx)
    
- [FOPE to EOP Transition FAQ](http://technet.microsoft.com/library/e0e76b89-b0d3-4c0a-bfc8-137b579e983b.aspx)
    
 **P. O que é o EOP?**
  
R. EOP é um serviço de filtragem de email hospedado na nuvem, criado para proteger os clientes contra spam e malware, além de implementar regras de política personalizadas.
  
 **P. Como eu me inscrevo para uma avaliação do EOP ou para comprar o EOP?**
  
R. Inscreva-se para uma avaliação do EOP ou para comprar o EOP pela Web na [home page do Exchange Online Protection](https://go.microsoft.com/fwlink/p/?LinkId=279912). Observe que a funcionalidade de uma compra de avaliação é a mesma de uma assinatura paga, mas também inclui recursos adicionais fornecidos com o plano de assinatura [Exchange Enterprise CAL com serviços](https://go.microsoft.com/fwlink/p/?LinkId=320619). 
  
 **R. Como é definido o preço do EOP?**
  
R. O EOP é licenciado por usuário. Para ver as informações mais recentes sobre preços, consulte a [Home page do Exchange Online Protection](https://go.microsoft.com/fwlink/p/?LinkId=279912).
  
 **P. Quanto tempo é necessário para colocar o EOP em produção?**
  
R. Quando você altera seu registro do MX, de acordo com as etapas descritas em [Configurar seu serviço EOP](set-up-your-eop-service.md), e seu email flui pelo EOP, a filtragem começa imediatamente. O registro MX pode demorar até 24 a 48 horas para ser propagado via DNS. Você pode ajustar suas configurações de proteção no centro de administração do Exchange (EAC) a qualquer momento durante esse processo.
  
 **P. Eu tenho que usar todos os recursos do Microsoft Office 365 para usar o EOP? E se eu quiser apenas a proteção do EOP e nada mais?**
  
R. Você pode usar a EOP para proteger suas caixas de correio locais sem usar nenhum outro recurso do Office 365. Isso é conhecido como assinatura autônoma. Uma lista de recursos da EOP pode ser encontrada em [Serviço de Descrição da Proteção do Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=320619).
  
 **P. Por que preciso de um locatário do Office 365 ao me inscrever na filtragem de email por meio do EOP?**
  
R. O Office 365 é o nome dado a um conjunto de produtos e serviços que podem ser acessados por meio do locatário do Office 365. Pense no locatário do Office 365 como o ponto de partida em que você adiciona licenças para a filtragem de email.
  
 **P. O EOP tem um portal de comunicação em que posso obter informações sobre problemas conhecidos e resoluções esperadas? E quanto a novos recursos?**
  
R. O centro de administração do Microsoft 365 terá algumas dessas informações. Se você for afetado por um evento de nível de serviço, deverá ver um alerta de comunicação (normalmente acompanhado por um ícone de sino) após entrar no centro de administração do Microsoft 365. Recomendamos ler as informações e executar as ações necessárias para qualquer item, conforme apropriado.
  
Em relação aos novos recursos do EOP, o [Mapa de recursos do Office 365 para empresas](https://office.microsoft.com/en-us/products/office-365-roadmap-FX104343353.aspx) é uma boa ferramenta para encontrar informações sobre novos recursos. Postaremos também artigos de blog sobre os novos recursos no site [Office Blogs](https://go.microsoft.com/fwlink/p/?LinkId=392724). 
  
 **P. O serviço funciona com versões herdadas do Exchange (como o Exchange Server 2010) e ambientes que não sejam Exchange?**
  
R. Sim, o serviço é independente do servidor e pode ser usado com qualquer agente de transferência de email SMTP.
  
 **P. O serviço pode ser usado por organizações de que tamanho?**
  
R. Qualquer tamanho. A rede do EOP tem capacidade suficiente para acomodar seu crescimento, mesmo que ele seja muito rápido.
  
 **Quais são as permissões necessárias para configurar o EOP?**
  
Para configurar o EOP, você precisa ser um administrador global do Office 365 ou um administrador da empresa do Exchange (o grupo de funções Gerenciamento de Organização).
  
 **P. Como eu sei se meus dados e informações particulares estão seguros?**
  
R. Para saber mais sobre as medidas que adotamos para garantir a segurança dos seus dados e informações particulares, inclusive informações sobre Contratos de Nível de Serviço (SLAs), vá para a [Central de Confiabilidade do Office 365](https://go.microsoft.com/fwlink/p/?LinkId=285405).
  
 **P. Há algum limite que eu deva conhecer; por exemplo, limitações de tamanho da mensagem?**
  
A. Sim. Para obter mais informações sobre limites no EOP, consulte [Limites do Exchange Online Protection](https://go.microsoft.com/fwlink/p/?LinkId=402617). 
  
 **P. O EOP é compatível com o Microsoft PowerShell remoto?**
  
A. Sim, todos os recursos do EOP estão disponíveis através do Windows PowerShell remoto. Para obter mais informações, consulte [PowerShell da Proteção do Exchange Online](http://technet.microsoft.com/library/f7918a88-774a-405e-945b-bc2f5ee9f748.aspx).
  


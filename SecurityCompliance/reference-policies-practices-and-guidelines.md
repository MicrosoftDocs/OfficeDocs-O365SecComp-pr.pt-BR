---
title: Políticas de referência, práticas e diretrizes
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
ms.assetid: ff3f140b-b005-445f-bfe0-7bc3f328aaf0
description: Microsoft desenvolveu várias políticas, os procedimentos e adotado várias práticas recomendadas do setor para ajudar a proteger nossos usuários de email ofensivas, indesejada ou mal-intencionado.
ms.openlocfilehash: e552128a06ce942383e7c5410508df61331fb874
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23003080"
---
# <a name="reference-policies-practices-and-guidelines"></a>Referência: políticas, práticas e diretrizes
  
Microsoft é dedicada a ajudar a fornecer a experiência do usuário mais confiável na web. Portanto, Microsoft desenvolveu várias políticas, os procedimentos e adotado várias práticas recomendadas do setor para ajudar a proteger nossos usuários de email ofensivas, indesejada ou mal-intencionado. Remetentes tentando enviar email para usuários do Office 365 devem assegurar totalmente entender e esteja seguindo as diretrizes deste artigo para ajudar nesse esforço e para ajudar a evitar possíveis problemas de entrega.
  
Se ainda não estiver em conformidade com essas políticas e diretrizes, pode não ser possível para a nossa equipe de suporte para ajudá-lo. Se você estiver aderir às políticas apresentadas neste artigo, práticas e diretrizes e ainda estiver tendo problemas de entrega com base em seu endereço IP de envio, siga as etapas para enviar uma solicitação delisting. Para obter instruções, consulte [usar o portal delist para remover seu nome na lista de remetentes bloqueados do Office 365](use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis.md).
  
## <a name="general-microsoft-policies"></a>Políticas de Microsoft gerais
<a name="GenMsftPolicies"> </a>

Emails enviados para usuários do Office 365 devem cumprir todas as políticas da Microsoft que regem a transmissão de email e o uso do Office 365.
  
- Termos dos serviços aplicáveis ao Office 365; em particular, a proibição usando o serviço de spam ou para distribuir malware
    
- [Contrato de serviços da Microsoft](https://www.microsoft.com/servicesagreement/)
    
## <a name="governmental-regulations"></a>Normas governamentais
<a name="GovtRegulations"> </a>

Emails enviados para usuários do Office 365 devem cumprir todas as leis e regulamentações sobre comunicações de email na jurisdição aplicável.
  
- [SPAM CAN Act: Um guia de conformidade para empresas](https://www.ftc.gov/tips-advice/business-center/guidance/can-spam-act-compliance-guide-business)
    
- ["Remover mim" respostas e responsabilidades: Email comerciantes devem honram declarações "Cancelar"](https://www.lawpublish.com/ftc-emai-marketers-unsubscribe-claims.mdl)
    
## <a name="technical-guidelines"></a>Diretrizes técnicas
<a name="TechGuidelines"> </a>

Emails enviados para o Office 365 devem ser compatíveis com as recomendações aplicáveis listadas nos documentos abaixo (alguns links só estão disponíveis em inglês).
  
- [RFC 2505: Recomendações de antispam para MTAs SMTP](https://www.ietf.org/rfc/rfc2505.txt)
    
- [RFC 2920: Extensão serviço SMTP para o pipeline de comando](https://www.ietf.org/rfc/rfc2920.txt)
    
Além disso, os servidores de email conectar-se ao Office 365 devem atender aos seguintes requisitos:
  
- Remetente é esperado em conformidade com todos os padrões técnicos para a transmissão de email da Internet, como publicado do The Internet Society Internet Engineering Task Force (IETF), incluindo a RFC 5321, RFC 5322 e outros. 
    
- Depois de dado um código de resposta de erro SMTP numérico entre 500 e 599 (também conhecido como uma resposta de falha na entrega permanente ou NDR), o remetente não deve tentar retransmitir a mensagem, para que o destinatário.
    
- Após várias respostas de falha na entrega, o remetente deve deixarão de existir ainda mais tenta enviar email para que o destinatário.
    
- As mensagens não devem ser transmitidas por meio de servidores de proxy ou de retransmissão de email inseguro.
    
- O mecanismo para cancelar a assinatura, a partir listas individuais ou de todas as listas hospedadas pelo remetente, deve ser claramente documentados e fácil para os destinatários encontrarem e usarem.
    
- Conexões do espaço de IP dinâmica podem não ser aceito.
    
- Servidores de email devem ter registros DNS reversos válidos.
    
## <a name="reputation-management"></a>Gerenciamento de reputação
<a name="RepManagement"> </a>

Remetentes, do provedor e outros provedores de serviços devem gerenciar ativamente a reputação de seus endereços IP de saída.
  
## <a name="office-365-limits"></a>Limites do Office 365
<a name="sectionSection4"> </a>

Os remetentes devem cumprir os limites de Office 365 listados no [Exchange Online Protection Limits](https://technet.microsoft.com/library/exchange-online-protection-limits.aspx).
  
## <a name="email-delivery-resources-and-organizations"></a>Recursos de entrega de email e organizações
<a name="sectionSection5"> </a>

A Microsoft trabalha ativamente com corpos de setor e provedores de serviços para melhorar o ecossistema de internet e email. Essas organizações publicaram documentos de práticas recomendadas que podemos suportam e recomendável cumpram remetentes. Isso melhora a capacidade de entregar mensagens de email entre vários provedores de serviço de email em todo o mundo.
  
- [Mensagens do grupo de trabalho de mau anti-uso Malware Mobile](https://www.m3aawg.org/)
    
- [Aliança de confiança online](https://www.otalliance.org/resources)
    
- [Email do remetente &amp; Coalition de provedor](http://www.espcoalition.org/)
    
## <a name="abuse-and-spam-reporting"></a>Abusar e relatório de spam
<a name="AbuseSpamReports"> </a>

Para relatar ilegal, ofensivos, indesejada ou mal-intencionadas de email, faça o [relatório de lixo eletrônico e golpes de phishing no Outlook na web ](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md). Enviar esses tipos de comunicações é uma violação da política da Microsoft e apropriada ação será tomada em relatórios confirmados.
  
## <a name="law-enforcement"></a>Cumprimento da lei
<a name="sectionSection7"> </a>

Se você é um membro do cumprimento da lei e desejar servir Microsoft Corporation com legal documentação sobre o Office 365, ou se você tiver dúvidas sobre documentação legal enviada à Microsoft, entre em contato com (1) (425) 722-1299.
  


---
title: Perguntas frequentes sobre Criptografia de Mensagem do Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 8/28/2018
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 0432dce9-d9b6-4e73-8a13-4a932eb0081e
description: Tem uma pergunta sobre como os novos recursos de proteção de mensagem no Office 365 funcionam? Verifique se há uma resposta aqui.
ms.openlocfilehash: 8fc3fa2378dfc8dba6ed17c042269f726235bc58
ms.sourcegitcommit: a8884b9675559018e1fddec1c0cc2de0bc3bdde5
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/06/2018
ms.locfileid: "23839951"
---
# <a name="office-365-message-encryption-faq"></a>Perguntas frequentes sobre Criptografia de Mensagem do Office 365

Tem uma pergunta sobre como os novos recursos de proteção de mensagem no Office 365 funcionam? Verifique se há uma resposta aqui. Além disso, dê uma olhada em [Perguntas frequentes sobre proteção de dados em proteção de informações do Windows Azure](https://docs.microsoft.com/information-protection/get-started/faqs-rms) para obter respostas a perguntas sobre o serviço de proteção de dados, o Azure Rights Management, em proteção de informações do Windows Azure. 
  
## <a name="what-is-office-365-message-encryption-ome"></a>O que é o Office 365 Message Encryption (OME)?

OME combina os recursos de gerenciamento de direitos e criptografia de email. Recursos de gerenciamento de direitos são possibilitados pela proteção de informações do Windows Azure.
  
## <a name="who-can-use-ome"></a>Quem pode usar OME?

Você pode usar os novos recursos para o OME sob as seguintes condições:
  
- Se você nunca definiu OME ou IRM para o Exchange Online no Office 365.
    
- Se você tiver configurado a OME e o IRM, você pode usar essas etapas se você estiver usando o serviço de gerenciamento de direitos do Windows Azure de proteção de informações do Windows Azure.
    
- Se você estiver usando o Exchange Online com o serviço de gerenciamento de direitos do Active Directory (AD RMS), não será possível habilitar esses novos recursos imediatamente. Em vez disso, será preciso [migrar do AD RMS à proteção de informações do Windows Azure](https://docs.microsoft.com/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms) pela primeira vez. Quando tiver concluído a migração, você pode configurar com êxito OME. 
    
    Se você escolher continuar a usar o local do AD RMS com o Exchange Online em vez de migração para proteção de informações do Windows Azure, não será capaz de usar esses novos recursos.
    
## <a name="what-subscriptions-do-i-need-to-use-the-new-ome-capabilities"></a>Quais assinaturas precisa usar os novos recursos OME?

Para usar os novos recursos OME, você precisa de um dos seguintes planos:
  
- O Office 365 Message Encryption é oferecido como parte do Office 365 E3 e E5, Microsoft E3 e E5, A1 do Office 365, A3 e A5 e Office 365 G3 e G5. Os clientes não precisam licenças adicionais para receber os novos recursos de proteção possibilitados pela proteção de informações do Windows Azure. 
    
- Você também pode adicionar Azure informações proteção plano 1 para os seguintes planos receber os novos recursos do Office 365 Message Encryption: Exchange Online plano 1, Exchange Online plano 2, F1 do Office 365, Essentials do Office 365 Business, Business Premium do Office 365, ou O Office 365 Enterprise E1.
    
- Cada usuário se beneficiando da criptografia de mensagem do Office 365 precisa ser licenciados para ser abordados pelo recurso.
    
- Para obter a lista completa, consulte as [descrições do serviço do Exchange Online](https://technet.microsoft.com/library/exchange-online-service-description.aspx) para Office 365 Message Encryption. 
    
## <a name="can-i-use-exchange-online-with-bring-your-own-key-byok-in-azure-information-protection"></a>Posso usar o Exchange Online com Traga sua própria chave (BYOK) na proteção de informações do Windows Azure?

Sim! A Microsoft recomenda que você conclua as etapas para configurar BYOK antes de configurar o OME.
  
Para obter mais informações sobre BYOK, consulte [planejamento e implementação de sua chave do locatário de proteção de informações do Windows Azure](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key).
  
## <a name="do-ome-and-byok-with-azure-information-protection-change-microsofts-approach-to-third-party-data-requests-such-as-subpoenas"></a>OME e BYOK com a proteção de informações do Azure alterar abordagem da Microsoft para solicitações de dados de terceiros, como intimações?

Não. OME e a opção para fornecer e controlar suas próprias chaves de criptografia, chamados BYOK, a partir de proteção de informações do Windows Azure não foram projetados para responder a lei imposição intimações. OME, com BYOK para proteção de informações do Windows Azure, foi projetado para os clientes centrados em conformidade. Microsoft leva muito a sério a solicitações de terceiros para dados do cliente. Como um provedor de serviços de nuvem, podemos sempre defendem à privacidade dos dados do cliente. No caso de recebemos intimação, sempre, tentaremos redirecionar o terceiro ao cliente para obter as informações. (Por favor, leia o blog de Brad Smith: [dados do cliente Protecting do governo snooping](https://blogs.microsoft.com/blog/2013/12/04/protecting-customer-data-from-government-snooping/)). Periodicamente, podemos publicar informações detalhadas da solicitação que recebemos. Para obter mais informações relacionadas a solicitações de dados de terceiros, consulte [responder a solicitações de imposição de lei para acessar dados do cliente e governamentais](https://www.microsoft.com/en-us/trustcenter/privacy/govt-requests-for-data) no Microsoft Trust Center. Além disso, consulte "Divulgação de dados do cliente" em [Termos de serviços Online (OST)](https://www.microsoft.com/en-us/Licensing/product-licensing/products.aspx).
  
## <a name="how-is-this-feature-related-to-legacy-office-365-message-encryption-ome-and-information-rights-management-irm-features"></a>Como esse recurso está relacionado aos recursos do Office 365 Message Encryption (OME) e o gerenciamento de direitos de informação (IRM) herdados?

Os novos recursos para o Office 365 Message Encryption são uma evolução do IRM existente e soluções OME herdada. A tabela a seguir fornece mais detalhes.
  
**Comparação de OME herdado, IRM e novos recursos OME**

|**Funcionalidade**|**Versões anteriores do OME**|**IRM**|**Novos recursos OME**|
|:-----|:-----|:-----|:-----|
|**Enviar um email criptografado**|Apenas por meio de regras de fluxo de correio do Exchange|Usuários finais iniciados a partir do Outlook para PC, o Outlook para Mac ou Outlook na web; ou regras de fluxo de emails por meio do Exchange|Usuários finais iniciados a partir do Outlook para PC, o Outlook para Mac ou Outlook na web; ou por meio de regras de fluxo de email|
|**Gerenciamento de direitos**|-|Faça a opção não encaminhar e modelos personalizados|Faça a opção não encaminhar, opção somente para criptografar, padrão e modelos personalizados|
|**Tipo de destinatário com suporte**|Somente os destinatários externos|Somente a destinatários internos|Destinatários internos e externos|
|**Experiência de destinatário**|Destinatários externos receberam uma mensagem HTML que eles baixado e aberto em um navegador ou baixado aplicativos móveis.|Destinatários internos apenas receberam email criptografadas no Outlook para PC, o Outlook para Mac e o Outlook na web.|Destinatários internos e externos recebem email no Outlook para PC, o Outlook para Mac, Outlook na web, o Outlook para Android e o Outlook para iOS ou por meio de um portal da web, independentemente de estarem ou não estejam na mesma organização Office 365 ou em qualquer Office 365 organização. O portal OME não requer nenhum download separado.|
|**Traga suporte Your Key próprias**|Não disponível|Não disponível| BYOK suportado|

## <a name="how-do-i-enable-the-new-ome-capabilities-for-my-organization"></a>Como habilitar os novos recursos OME para minha organização?

Consulte [configurar novos recursos do Office 365 Message Encryption](set-up-new-message-encryption-capabilities.md).
  
## <a name="will-the-previous-version-of-ome-be-deprecated"></a>A versão anterior do OME será preterida?

Você ainda pode usar a versão anterior do OME, ele não será preterido neste momento. No entanto, recomendamos altamente as organizações usam a solução OME nova e aprimorada. Os clientes que ainda não tiver implantado OME não é possível configurar uma nova implantação da versão anterior do OME.
  
## <a name="my-organization-uses-active-directory-rights-management-can-i-use-this-functionality"></a>Minha organização usa o Active Directory Rights Management, posso usar essa funcionalidade?

Não. Se você estiver usando o Exchange Online com o serviço de gerenciamento de direitos do Active Directory (AD RMS), não será possível habilitar esses novos recursos imediatamente. Em vez disso, será preciso [migrar do AD RMS à proteção de informações do Windows Azure](https://docs.microsoft.com/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms) pela primeira vez. 
  
## <a name="my-organization-has-an-exchange-hybrid-deployment-can-i-use-this-feature"></a>Minha organização tem uma implantação híbrida do Exchange. Posso usar esse recurso?

No local os usuários podem enviar mensagens criptografadas usando regras de fluxo de correio Exchange Online. Para fazer isso, você precisa rotear emails através do Exchange Online.
  
## <a name="what-email-client-do-i-need-to-use-in-order-to-create-an-ome-encrypted-message-what-applications-are-supported-for-sending-protected-messages"></a>O cliente de email que precisa ser usado para criar uma mensagem criptografada de OME? Quais aplicativos são suportados para o envio de mensagens protegidas?

Você pode criar mensagens protegidas contra 2016 do Outlook e Outlook 2013 para PC e Mac e do Outlook na web.
  
## <a name="what-email-clients-are-supported-to-read-and-reply-to-protected-emails"></a>Quais clientes de email são suportados para ler e responder a emails protegidos?

Você pode ler e responder a partir do Outlook para PC e Mac (2013 e 2016), Outlook na web e móveis do Outlook (Android e iOS) se você for um usuário do Office 365. Você também pode usar o cliente de email native iOS se sua organização permitir. Se você for um usuário do Office 365, você pode ler e responder a mensagens criptografadas na web através do navegador da web.
  
## <a name="what-file-types-are-supported-as-attachments-in-protected-emails-do-attachments-inherit-the-protection-policies-associated-with-protected-emails"></a>Quais tipos de arquivo são suportados como anexos em emails protegidos? Anexos herdam as políticas de proteção associadas a emails protegidos?

Você pode anexar qualquer tipo de arquivo a um email protegido, no entanto, as políticas de proteção são aplicadas apenas no arquivo formatos mencionado [aqui](https://docs.microsoft.com/information-protection/rms-client/client-admin-guide-file-types). 
  
Se um formato de arquivo é suportado, como um arquivo do Word, PowerPoint ou Excel, o arquivo é sempre protegido, mesmo depois que o anexo foi baixado pelo destinatário. Por exemplo, se um anexo é protegido por não encaminhar e o destinatário original baixa e encaminha o anexo a um novo destinatário, o novo destinatário não será capaz de abrir o arquivo protegido.
  
## <a name="are-pdf-file-attachments-supported"></a>Anexos de arquivo PDF são suportados?

Se você anexar um arquivo PDF a uma mensagem protegida, a própria mensagem será protegida, mas sem proteção adicional será aplicada ao arquivo PDF depois que o destinatário recebeu. Isso significa que o destinatário pode salvar como, encaminhar, copiar e imprimir o arquivo PDF.
  
## <a name="are-onedrive-for-business-attachments-supported"></a>São OneDrive para suporte de anexos de negócios?

Ainda não. OneDrive para anexos de negócios não são suportados e os usuários finais não podem criptografar um email que contém uma nuvem OneDrive para anexo de negócios.
  
## <a name="can-i-automatically-encrypt-messages-by-setting-up-policies"></a>Posso automaticamente criptografar mensagens, configurando políticas?

Sim. Use regras de fluxo de correio no Exchange Online para criptografar automaticamente uma mensagem com base em certas condições. Por exemplo, você pode criar políticas que se baseiam em destinatário ID, o domínio do destinatário, ou no conteúdo do corpo ou no assunto da mensagem. Consulte [definir regras de fluxo de email para criptografar mensagens de email no Office 365.](define-mail-flow-rules-to-encrypt-email.md)
  
## <a name="can-i-automatically-encrypt-messages-by-setting-up-policies-in-data-loss-prevention-dlp-through-the-security-amp-compliance-center"></a>Posso automaticamente criptografar mensagens, configurando políticas em Data Loss Prevention (DLP) através de segurança &amp; Centro de conformidade?

No momento você pode apenas definir as regras de fluxo de email no Exchange Online. Criptografia atualmente não é suportada no DLP através de segurança &amp; Centro de conformidade.
  
## <a name="can-i-customize-encrypted-messages-with-my-company-branding"></a>Pode personalizar mensagens criptografadas com a minha empresa branding?

Sim! Para obter informações sobre como personalizar mensagens de email e o portal OME, consulte Adicionar a marca da sua organização às mensagens criptografadas. Consulte [Adicionar a marca da sua organização às mensagens criptografadas.](add-your-organization-brand-to-encrypted-messages.md)
  
## <a name="are-there-any-reporting-capabilities-or-insights-for-encrypted-emails"></a>Existem recursos ou ideias para emails criptografados relatórios?

Não no momento, mas em breve.
  
## <a name="can-i-use-message-encryption-with-compliance-features-such-as-ediscovery"></a>Pode usar a criptografia de mensagem com recursos de conformidade, como a descoberta eletrônica?

Sim. Todas as mensagens de email criptografadas são descobertas pelos recursos de conformidade do Office 365.
  


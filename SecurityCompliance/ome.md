---
title: Criptografia de Mensagens do Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/6/2018
ms.audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f87cb016-7876-4317-ae3c-9169b311ff8a
description: Com a criptografia de mensagem do Office 365, sua organização pode enviar e receber mensagens de email criptografadas entre pessoas de dentro e fora da sua organização. Criptografia de mensagem de email ajuda a garantir que destinada apenas os destinatários pode exibir o conteúdo da mensagem.
ms.openlocfilehash: ae66ca79b2b0464e11d27fef553faccfd4787d75
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523954"
---
# <a name="office-365-message-encryption"></a>Criptografia de Mensagens do Office 365

Com a criptografia de mensagem do Office 365, sua organização pode enviar e receber mensagens de email criptografadas entre pessoas de dentro e fora da sua organização. O Office 365 Message Encryption funciona com Outlook.com, Yahoo!, Gmail e outros serviços de email. Criptografia de mensagem de email ajuda a garantir que destinada apenas os destinatários pode exibir o conteúdo da mensagem.
  
Este artigo faz parte de uma maior série de artigos sobre o Office 365 Message Encryption. Use a tabela a seguir para localizar rapidamente as informações que necessárias.
  
|||
|:-----|:-----|
|Leia este artigo …  <br/> |Se você …  <br/> |
|[Saiba mais sobre as mensagens protegidas no Office 365](https://support.office.com/article/2baf3ac7-12db-40a4-8af7-1852204b4b67.aspx) <br/> |Um usuário final que quer saber mais sobre como criptografadas mensagens de trabalho e quais opções estão disponíveis para você.  <br/> |
|[Como abrir uma mensagem protegida?](https://support.office.com/article/1157a286-8ecc-4b1e-ac43-2a608fbf3098.aspx) <br/> |Um usuário final que deseja ler uma mensagem protegida que foi enviada para você. Este artigo inclui informações sobre a leitura de mensagens em várias versões do Outlook e de contas de email diferentes, incluindo aqueles fora do Office 365, como o gmail e contas do Yahoo!.  <br/> |
|[Enviar, visualizar e responder a mensagens criptografadas no Outlook](https://support.office.com/article/eaa43495-9bbb-4fca-922a-df90dee51980.aspx) <br/> |Um usuário final que deseja enviar, visualizar ou responder a uma mensagem criptografada do Outlook. Mesmo se você não for um membro de uma organização do Office 365, você ainda receber notificações de mensagens criptografadas enviada para você no Outlook. Use este artigo para obter instruções sobre como visualizar e responder a mensagens criptografadas enviadas do Office 365.  <br/> |
|[Enviar uma mensagem assinada digitalmente ou criptografada](https://support.office.com/article/a18ecf7f-a7ac-4edd-b02e-687b05eff547) <br/> |Um usuário final que deseja enviar, visualizar ou responder a mensagens criptografadas usando o Outlook para Mac. Este artigo também aborda o uso de métodos de criptografia que não seja OME, como S/MIME.  <br/> |
|[Visualizar mensagens criptografadas no seu dispositivo Android](https://support.office.com/article/83d60f17-2305-407a-a762-7d518401fdeb) <br/> |Um usuário final que recebeu uma mensagem criptografada com o Office 365 Message Encryption no seu dispositivo Android, você pode usar o app OME visualizador gratuito para exibir a mensagem e enviar uma resposta criptografada. Este artigo explica como.  <br/> |
|[Visualizar mensagens criptografadas no seu iPhone ou iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf) <br/> |Um usuário final que recebeu uma mensagem criptografada com o Office 365 Message Encryption no seu iPhone ou iPad, você pode usar o app OME visualizador gratuito para exibir a mensagem e enviar uma resposta criptografada. Este artigo explica como.  <br/> |
|O Office 365 Message Encryption (OME) (Este artigo)  <br/> |Um administrador de Office 365 ou Exchange Online Protection que quer saber onde você pode encontrar recursos adicionais.  <br/> |
|[Perguntas frequentes sobre Criptografia de Mensagem do Office 365](ome-faq.md) <br/> |Um administrador de Office 365 ou Exchange Online Protection que deseja respostas para comumente frequentes incluindo licenciamento e uma comparação entre os novos recursos e OME herdado.  <br/> |
|[Configurar novos recursos de Criptografia de Mensagens do Office 365](set-up-new-message-encryption-capabilities.md) <br/> |Um administrador de Office 365 ou Exchange Online Protection que quiser saber mais sobre como configurar os novos recursos do Office 365 Message Encryption para sua organização do Office 365.  <br/> |
|[Definir regras de fluxo de email para criptografar mensagens de email no Office 365](define-mail-flow-rules-to-encrypt-email.md) <br/> |Um administrador do Office 365 ou Exchange Online Protection que já configurou a criptografia de mensagem do Office 365 e você está pronto para definir regras de fluxo de email para criptografar automaticamente mensagens de email enviadas de sua organização.  <br/> |
|[Gerenciar a Criptografia de Mensagens do Office 365](manage-office-365-message-encryption.md) <br/> |Um administrador de Office 365 ou Exchange Online Protection que já tenha configurado o Office 365 Message Encryption e deseja definir configurações opcionais para OME.  <br/> |
|[Adicionar a marca da sua organização a suas mensagens criptografadas](add-your-organization-brand-to-encrypted-messages.md) <br/> |Um administrador de Office 365 ou Exchange Online Protection que deseja aplicar a sua empresa branding para personalizar a aparência das mensagens de email do Office 365 Message Encryption da sua organização e o conteúdo do portal OME.  <br/> |
|Criptografia de mensagem do Office 365 na [política de mensagem e a descrição do serviço de conformidade](https://technet.microsoft.com/en-us/library/5c43c8eb-f8f7-4b5a-a743-b1dab7dc2fc8#bkmk_O365_MessageEncryption) <br/> |Procurando por uma descrição detalhada do recurso de criptografia de mensagem do Office 365, incluindo suporte para SKUs, disponíveis no Office 365.  <br/> |
|[Informações herdadas de Criptografia de Mensagens do Office 365](legacy-information-for-message-encryption.md) <br/> |Um administrador do Office 365 ou Exchange Online Protection que já configurou a criptografia de mensagem do Office 365 e você deseja obter informações sobre como OME funcionou antes do lançamento de novos recursos. Enquanto você não puder configurar uma nova implantação usando OME sem os novos recursos, o Microsoft continua a oferecer suporte a implantações existentes.  <br/> |
   
O restante deste artigo se aplica aos novos recursos OME.
  
## <a name="how-office-365-message-encryption-works"></a>Como funciona a criptografia de mensagem do Office 365

Criptografia de mensagem do Office 365 é um serviço online que é baseado no Microsoft Azure Rights Management (RMS do Windows Azure) que é parte da proteção de informações do Windows Azure. Administradores do Office 365 podem definir regras de fluxo de email para determinar as condições de criptografia. Por exemplo, uma regra pode exigir a criptografia de todas as mensagens endereçadas para um destinatário específico.
  
Quando alguém envia uma mensagem de email no Exchange Online que corresponda a uma regra de fluxo de email de criptografia, a mensagem é criptografada antes de serem enviada. Todos os usuários finais de Office 365 que usam clientes do Outlook para ler email recebem nativo, primeira classe experiências para emails criptografados e protegidos por direitos de leitura, mesmo que eles não estejam na mesma organização como o remetente. Clientes Outlook suportados incluem Outlook área de trabalho, Mac do Outlook, Outlook Web App e Outlook mobile em iOS e Android.
  
Destinatários das mensagens criptografadas que recebem email criptografado ou protegido por direitos enviada para suas contas do Outlook.com, Gmail e Yahoo facilmente podem autenticar ao portal OME usando suas credenciais do Gmail ou Yahoo! ou a conta da Microsoft.
  
Os usuários finais que leia email criptografado ou protegido por direitos em clientes diferentes do Outlook também usam o portal OME para exibir as mensagens criptografadas e protegidas por direitos que eles recebem.
  
Aumentou os limites de tamanho de mensagens e anexos que você pode criptografar usando o Office 365 Message Encryption. Para obter mais informações sobre os limites, consulte [limites do Exchange Online.](https://technet.microsoft.com/en-us/library/exchange-online-limits.aspx)
  
## <a name="defining-rules-for-office-365-message-encryption"></a>Definir regras para a Criptografia de Mensagens do Office 365
<a name="Rules"> </a>

Uma maneira para habilitar os novos recursos para o Office 365 Message Encryption é para administradores do Exchange Online e Exchange Online Protection definir regras de fluxo de email. Essas regras determinam em email quais condições mensagens devem ser criptografadas. Quando uma ação de criptografia é definida para uma regra, todas as mensagens que correspondam às condições de regra são criptografadas antes que eles enviados.
  
Regras de fluxo de correio são flexíveis, permitindo que você combinar condições para que você pode atender a requisitos de segurança específicos em uma única regra. Por exemplo, você pode criar uma regra para criptografar todas as mensagens que contêm palavras-chave especificadas e são endereçadas a destinatários externos. Os novos recursos para a criptografia de mensagem do Office 365 também criptografar respostas de destinatários de email criptografada.
  
Para obter mais informações sobre como criar regras de fluxo tirar vantagem dos novos recursos OME de email, consulte [Define Rules for Office 365 Message Encryption](define-mail-flow-rules-to-encrypt-email.md).
  
## <a name="sending-viewing-and-replying-to-encrypted-email-messages"></a>Enviar, visualizar e responder mensagens de email criptografadas
<a name="SendRecip"> </a>

Com o Office 365 Message Encryption, os usuários podem enviar email criptografado do Outlook e do Outlook na web. Além disso, os administradores podem configurar regras de fluxo de correio no Office 365 para criptografar automaticamente emails com base nas condições de correspondência ou outras de palavra-chave.
  
Os destinatários das mensagens criptografadas que estiverem no Office 365 organizações poderão ler essas mensagens integralmente em qualquer versão do Outlook, incluindo o Outlook para PC, o Outlook para Mac, Outlook na web, o Outlook para iOS e Outlook para Android. Os usuários que recebem mensagens criptografadas em outros clientes de email podem exibir as mensagens no portal do OME.
  
Para obter orientações detalhadas sobre como enviar e visualizar mensagens criptografadas, dê uma olhada nestes artigos:
  
- [Como abrir uma mensagem protegida?](https://support.office.com/article/1157a286-8ecc-4b1e-ac43-2a608fbf3098.aspx)
    
- [Enviar, visualizar e responder a mensagens criptografadas no Outlook](https://support.office.com/article/eaa43495-9bbb-4fca-922a-df90dee51980.aspx)
    
## <a name="get-started-with-the-new-ome-capabilities"></a>Guia de Introdução com os novos recursos OME
<a name="SendRecip"> </a>

Se você estiver pronto para começar a usar os novos recursos OME dentro da sua organização, consulte [configurar novos recursos do Office 365 Message Encryption](set-up-new-message-encryption-capabilities.md).
  


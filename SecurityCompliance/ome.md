---
title: Criptografia de Mensagem do Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/6/2018
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f87cb016-7876-4317-ae3c-9169b311ff8a
description: Com a criptografia de mensagem do Office 365, sua organização pode enviar e receber mensagens de email criptografadas entre pessoas dentro e fora da sua organização. A criptografia de mensagens de email ajuda a garantir que somente os destinatários pretendidos possam exibir o conteúdo da mensagem.
ms.openlocfilehash: 04a7cc23b7a9c4218a719c172544147b3daedd7a
ms.sourcegitcommit: 696c1ed6b270be3f9da7395b49a7d8fec98e6db0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/29/2019
ms.locfileid: "33470401"
---
# <a name="office-365-message-encryption"></a>Criptografia de Mensagem do Office 365

As pessoas geralmente usam email para trocar informações importantes, como dados financeiros, contratos, informações confidenciais de produtos, relatórios e projeções de vendas, informações sobre a saúde de pacientes ou informações sobre clientes e empregados. Portanto, as caixas de correio podem se tornar repositórios de grandes quantidades de informações potencialmente confidenciais, e o vazamento de informações pode se tornar uma séria ameaça à sua organização.

Com a criptografia de mensagem do Office 365, sua organização pode enviar e receber mensagens de email criptografadas entre pessoas dentro e fora da sua organização. A criptografia de mensagem do Office 365 funciona com o Outlook.com, Yahoo!, Gmail e outros serviços de email. A criptografia de mensagens de email ajuda a garantir que somente os destinatários pretendidos possam exibir o conteúdo da mensagem.
  
Este artigo faz parte de uma série maior de artigos sobre a criptografia de mensagens do Office 365. Use a tabela a seguir para encontrar rapidamente as informações de que você precisa.
  
|||
|:-----|:-----|
|Leia este artigo...  <br/> |Se você for...  <br/> |
|[Saiba mais sobre mensagens protegidas no Office 365](https://support.office.com/article/2baf3ac7-12db-40a4-8af7-1852204b4b67.aspx) <br/> |Um usuário final que deseja saber mais sobre como funcionam as mensagens criptografadas e quais opções estão disponíveis para você.  <br/> |
|[Como abro uma mensagem protegida?](https://support.office.com/article/1157a286-8ecc-4b1e-ac43-2a608fbf3098.aspx) <br/> |Um usuário final que deseja ler uma mensagem protegida que foi enviada a você. Este artigo inclui informações sobre a leitura de mensagens em várias versões do Outlook e de diferentes contas de email, incluindo aquelas fora do Office 365, como Gmail e Yahoo! las.  <br/> |
|[Enviar, exibir e responder a mensagens criptografadas no Outlook](https://support.office.com/article/eaa43495-9bbb-4fca-922a-df90dee51980.aspx) <br/> |Um usuário final que deseja enviar, exibir ou responder a uma mensagem criptografada do Outlook. Mesmo que você não seja membro de uma organização do Office 365, ainda receberá uma notificação de mensagens criptografadas enviadas para você no Outlook. Use este artigo para obter instruções sobre como exibir e responder a mensagens criptografadas enviadas do Office 365.  <br/> |
|[Enviar uma mensagem assinada digitalmente ou criptografada](https://support.office.com/article/a18ecf7f-a7ac-4edd-b02e-687b05eff547) <br/> |Um usuário final que deseja enviar, exibir ou responder a mensagens criptografadas usando o Outlook para Mac. Este artigo também cobre o uso de métodos de criptografia diferentes de OME, como S/MIME.  <br/> |
|[Exibir mensagens criptografadas no seu dispositivo Android](https://support.office.com/article/83d60f17-2305-407a-a762-7d518401fdeb) <br/> |Um usuário final que recebeu uma mensagem criptografada com a criptografia de mensagem do Office 365 no seu dispositivo Android, você pode usar o aplicativo OME Viewer gratuito para exibir a mensagem e enviar uma resposta criptografada. Este artigo explica como.  <br/> |
|[Exibir mensagens criptografadas no seu iPhone ou iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf) <br/> |Um usuário final que recebeu uma mensagem criptografada com a criptografia de mensagem do Office 365 em seu iPhone ou iPad, você pode usar o aplicativo OME Viewer gratuito para exibir a mensagem e enviar uma resposta criptografada. Este artigo explica como.  <br/> |
|Criptografia de mensagem do Office 365 (OME) (este artigo)  <br/> |Um administrador de proteção do Office 365 ou do Exchange Online que deseja saber onde você pode encontrar recursos adicionais.  <br/> |
|[Comparar versões de OME](ome-version-comparison.md)  <br/> |Um administrador de proteção do Office 365 ou do Exchange Online que deseja saber as diferenças entre a criptografia de mensagem herdada do Office 365 e os novos recursos do OME, além de como eles podem trabalhar juntos.  <br/> |
|[Perguntas frequentes sobre Criptografia de Mensagem do Office 365](ome-faq.md) <br/> |Um administrador de proteção do Office 365 ou do Exchange Online que deseja respostas a perguntas frequentes, incluindo licenciamento e uma comparação entre os novos recursos e o OME herdado.  <br/> |
|[Configurar novos recursos de Criptografia de Mensagens do Office 365](set-up-new-message-encryption-capabilities.md) <br/> |Um administrador de proteção do Office 365 ou do Exchange Online que deseja saber como configurar os novos recursos de criptografia de mensagens do Office 365 para sua organização do Office 365.  <br/> |
|[Definir regras de fluxo de e-mail para criptografar mensagens de e-mail no Office 365](define-mail-flow-rules-to-encrypt-email.md) <br/> |Um administrador de proteção do Office 365 ou do Exchange Online que já configurou a criptografia de mensagem do Office 365 e você está pronto para definir regras de fluxo de emails para criptografar automaticamente mensagens de email enviadas da sua organização.  <br/> |
|[Gerenciar a Criptografia de Mensagens do Office 365](manage-office-365-message-encryption.md) <br/> |Um administrador de proteção do Office 365 ou do Exchange Online que já configurou a criptografia de mensagem do Office 365 e deseja definir configurações opcionais para o OME.  <br/> |
|[Adicionar a marca da sua organização a suas mensagens criptografadas](add-your-organization-brand-to-encrypted-messages.md) <br/> |Um administrador de proteção do Office 365 ou do Exchange Online que deseja aplicar a identidade visual da sua empresa para personalizar a aparência das mensagens de email de criptografia de mensagem do Office 365 da sua organização e o conteúdo do portal do OME.  <br/> |
|[Revogação de email de criptografia de mensagem do Office 365](revoke-ome-encrypted-mail.md) <br/> |Um administrador de proteção do Office 365 ou do Exchange Online que deseja revogar um email criptografado usando a criptografia de mensagem do Office 365.  <br/> |
|Criptografia de mensagem do Office 365 na [Descrição de política de mensagens e serviço de conformidade](https://technet.microsoft.com/en-us/library/5c43c8eb-f8f7-4b5a-a743-b1dab7dc2fc8#bkmk_O365_MessageEncryption) <br/> |Procurando uma descrição detalhada do recurso de criptografia de mensagem do Office 365, incluindo SKUs suportados, disponível no Office 365.  <br/> |
|[Informações herdadas de Criptografia de Mensagens do Office 365](legacy-information-for-message-encryption.md) <br/> |Um administrador de proteção do Office 365 ou do Exchange Online que já configurou a criptografia de mensagem do Office 365 e você deseja obter informações sobre como o OME funcionou antes do lançamento dos novos recursos. Embora você não possa configurar uma nova implantação usando o OME sem os novos recursos, a Microsoft continua a oferecer suporte a implantações existentes. <br/> |
||

O restante deste artigo se aplica aos novos recursos do OME.
  
## <a name="how-office-365-message-encryption-works"></a>Como funciona a criptografia de mensagens do Office 365

A criptografia de mensagem do Office 365 é um serviço online desenvolvido no Microsoft Azure Rights Management (Azure RMS), que faz parte da proteção de informações do Azure. Isso inclui políticas de criptografia, identidade e autorização para ajudar a proteger seu email. Você pode criptografar mensagens usando modelos de gerenciamento de direitos, a [opção](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails)não encaminhar e a [opção somente criptografia](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails).

Os usuários podem então criptografar mensagens de email e uma variedade de anexos do Office 365 usando essas opções. Para obter uma lista completa de tipos de anexo compatíveis, consulte ["tipos de arquivo cobertos por políticas de IRM quando estão anexados a mensagens" em Introdução ao IRM para mensagens de email](https://support.office.com/article/bb643d33-4a3f-4ac7-9770-fd50d95f58dc#FileTypesforIRM).

Como administrador, você também pode definir regras de fluxo de email para aplicar essa proteção. Por exemplo, você pode criar uma regra que exija a criptografia de todas as mensagens endereçadas a um destinatário específico ou que contenha palavras específicas na linha de assunto, além de especificar que os destinatários não possam copiar ou imprimir o conteúdo da mensagem.

Ao contrário da versão anterior do OME, os novos recursos oferecem uma experiência de remetente unificado se você estiver enviando emails dentro da sua organização ou para destinatários fora do Office 365. Além disso, os destinatários que recebem uma mensagem de email protegida enviadas para uma conta do Office 365 no Outlook 2016 ou no Outlook na Web não precisam realizar qualquer ação adicional para exibir a mensagem. Funciona perfeitamente. Os destinatários que usam outros clientes de email e provedores de serviço de email também têm uma experiência aprimorada. Para obter informações, consulte [saiba mais sobre mensagens protegidas no Office 365](https://support.office.com/article/Learn-about-protected-messages-in-Office-365-2baf3ac7-12db-40a4-8af7-1852204b4b67) e [como eu abro uma mensagem protegida](https://support.office.com/article/How-do-I-open-a-protected-message-1157a286-8ecc-4b1e-ac43-2a608fbf3098).

Para obter uma lista detalhada das diferenças entre a versão anterior do OME e os novos recursos do OME, consulte [comparar versões do ome](ome-version-comparison.md).

Quando alguém envia uma mensagem de email que corresponde a uma regra de fluxo de mensagens de criptografia, a mensagem é criptografada antes de ser enviada. Todos os usuários finais do Office 365 que usam os clientes do Outlook para ler email recebem experiências de leitura nativas de primeira classe para mensagens criptografadas e protegidas por direitos, mesmo que não estejam na mesma organização que o remetente. Os clientes do Outlook com suporte incluem a área de trabalho do Outlook, o Outlook Mac, o Outlook Mobile no iOS e o Android, e o Outlook na Web (anteriormente conhecido como Outlook Web App).
  
Os destinatários de mensagens criptografadas que recebem mensagens criptografadas ou protegidas por direitos enviados para suas contas do Outlook.com, do Gmail e do Yahoo recebem um email de wrapper que os direciona para o portal do OME onde podem autenticar facilmente usando uma conta da Microsoft, Gmail ou Credenciais do Yahoo.
  
Os usuários finais que lêem mensagens criptografadas ou protegidas por direitos em clientes diferentes do Outlook também usam o portal OME para exibir mensagens criptografadas e protegidas por direitos recebidas.

Além disso, se o remetente do email protegido estiver em GCC alta e o destinatário estiver fora da GCC alta, incluindo os usuários do Office 365, usuários do Outlook.com e usuários de outros provedores de email, como o Gmail, o destinatário receberá um email de conteúdo que redireciona para o portal do OME em que o destinatário é capaz de ler e responder à mensagem. Caso contrário, se o remetente e o destinatário estiverem ambos no ambiente GCC, os destinatários que usam os clientes do Outlook para ler emails recebem experiências de leitura nativas e de primeira classe para mensagens criptografadas e protegidas por direitos, mesmo que não estejam na mesma organização. como o remetente.
  
Aumentamos os limites de tamanho de mensagens e anexos que você pode criptografar usando o OME. Para obter mais informações sobre limites, consulte [limites do Exchange Online](https://technet.microsoft.com/en-us/library/exchange-online-limits.aspx).
  
## <a name="defining-rules-for-office-365-message-encryption"></a>Definir regras para a Criptografia de Mensagens do Office 365

Uma maneira de habilitar os novos recursos para a criptografia de mensagem do Office 365 é para os administradores do Exchange Online e do Exchange Online Protection definir regras de fluxo de email. Essas regras determinam sob quais condições as mensagens de email devem ser criptografadas. Quando uma ação de criptografia é definida para uma regra, quaisquer mensagens que correspondam às condições de regra são criptografadas antes de serem enviadas.
  
As regras de fluxo de emails são flexíveis, permitindo que você combine condições para que possa atender a requisitos específicos de segurança em uma única regra. Por exemplo, você pode criar uma regra para criptografar todas as mensagens que contenham palavras-chave específicas e que sejam endereçadas a destinatários externos. Os novos recursos da criptografia de mensagem do Office 365 também criptografam respostas de destinatários de emails criptografados.
  
Para obter mais informações sobre como criar regras de fluxo de email para aproveitar os novos recursos do OME, consulte [definir regras para a criptografia de mensagem do Office 365](define-mail-flow-rules-to-encrypt-email.md).
  
## <a name="sending-viewing-and-replying-to-encrypted-email-messages"></a>Enviar, visualizar e responder mensagens de email criptografadas

Com a criptografia de mensagem do Office 365, os usuários podem enviar emails criptografados do Outlook e do Outlook na Web. Além disso, os administradores podem configurar regras de fluxo de email no Office 365 para criptografar emails automaticamente com base na correspondência de palavras-chave ou outras condições.
  
Os destinatários de mensagens criptografadas que estão nas organizações do Office 365 poderão ler essas mensagens de forma transparente em qualquer versão do Outlook, incluindo o Outlook para PC, o Outlook para Mac, o Outlook na Web, o Outlook para iOS e o Outlook para Android. Os usuários que recebem mensagens criptografadas em outros clientes de email podem exibir as mensagens no portal do OME.
  
Para obter orientações detalhadas sobre como enviar e exibir mensagens criptografadas, consulte estes artigos:
  
- [Como abro uma mensagem protegida?](https://support.office.com/article/1157a286-8ecc-4b1e-ac43-2a608fbf3098.aspx)

- [Enviar, exibir e responder a mensagens criptografadas no Outlook](https://support.office.com/article/eaa43495-9bbb-4fca-922a-df90dee51980.aspx)

## <a name="get-started-with-the-new-ome-capabilities"></a>Introdução aos novos recursos do OME

Se você estiver pronto para começar a usar os novos recursos do OME em sua organização, confira [configurar os novos recursos de criptografia de mensagens do Office 365](set-up-new-message-encryption-capabilities.md).

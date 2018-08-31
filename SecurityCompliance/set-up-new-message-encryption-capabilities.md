---
title: Configurar novos recursos de Criptografia de Mensagens do Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/19/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 7ff0c040-b25c-4378-9904-b1b50210d00e
description: Novo Office 365 Message Encryption recursos internos na parte superior de proteção de informações do Windows Azure, sua organização podem usar protegido a comunicação com pessoas de dentro e fora da sua organização por email. As novas capacidades OME trabalham com outras organizações do Office 365, Outlook.com, Gmail e outros serviços de email.
ms.openlocfilehash: e59368f5854c86c04f4f0bdf376537d3f6b02d33
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524634"
---
# <a name="set-up-new-office-365-message-encryption-capabilities"></a>Configurar novos recursos de Criptografia de Mensagens do Office 365

Com os novos recursos do Office 365 Message Encryption (OME), que aproveitar os recursos de proteção em proteção de informações do Windows Azure, sua organização pode compartilhar facilmente email protegido com qualquer pessoa em qualquer dispositivo. Os usuários podem enviar e receber mensagens protegidas com outras organizações do Office 365, bem como os clientes do Office 365 usando o Outlook.com, Gmail e outros serviços de email.
  
## <a name="get-started-with-ome-by-activating-azure-rights-management-part-of-azure-information-protection"></a>Introdução ao OME ativando o Azure Rights Management, parte de proteção de informações do Windows Azure

Agora é fácil começar com os novos recursos OME. A partir de fevereiro de 2018, o Office 365 habilita automaticamente os novos recursos OME para organizações elegíveis em nossos data centers. Sua organização está qualificada se for um novo inquilino do Office 365 e sua organização tem as assinaturas apropriadas. * * Se * * * * você habilitou o Azure Rights Management (RMS do Windows Azure), parte de proteção de informações do Windows Azure, então estamos habilitar automaticamente a criptografia de mensagem do Office 365 para você. * * Você não precisa fazer nada para habilitar OME. Para ativar o Azure Rights Management, consulte [Ativar o Azure Rights Management](https://docs.microsoft.com/azure/information-protection/deploy-use/activate-service). Para obter informações sobre inscrições, consulte "quais assinaturas preciso usar o novo capabilities? OME" nas [Perguntas frequentes sobre a criptografia de mensagem do Office 365](ome-faq.md). Para obter informações sobre como adquirir uma assinatura à proteção de informações do Windows Azure, consulte [Proteção de informações do Windows Azure](https://azure.microsoft.com/services/information-protection/).
  
Se você estiver usando o Exchange Online com o serviço de gerenciamento de direitos do Active Directory (AD RMS), não será possível habilitar esses novos recursos imediatamente. Em vez disso, você precisa migrar do AD RMS à proteção de informações do Windows Azure pela primeira vez. Quando tiver concluído a migração, você pode concluir estas etapas com sucesso.
  
Se você escolher continuar a usar o local do AD RMS com o Exchange Online em vez de migração para proteção de informações do Windows Azure, não será capaz de usar esses novos recursos.
  
## <a name="how-the-new-capabilities-for-ome-work"></a>Como funcionam os novos recursos para o OME

Os novos recursos do Office 365 Message Encryption usem os recursos de proteção, também chamados Azure Rights Management (RMS do Windows Azure), a partir de proteção de informações do Windows Azure. Isso inclui as políticas de criptografia, identidade e autorização para ajudar a proteger seu email. Você pode criptografar mensagens usando a [opção somente para criptografar](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails), a [opção não encaminhar](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails)e modelos de gerenciamento de direitos. Os usuários podem criptografar mensagens de email e uma variedade de anexos do Office 365 usando essas opções. Para obter uma lista completa dos tipos de anexos suportados, consulte ["tipos de arquivo coberto por políticas IRM quando eles forem anexados às mensagens" em Introdução ao IRM para mensagens de email](https://support.office.com/article/bb643d33-4a3f-4ac7-9770-fd50d95f58dc#FileTypesforIRM). Como administrador, você também pode definir regras de fluxo de email para aplicar essa proteção. Por exemplo, você pode definir uma regra onde todas as mensagens desprotegidas que são endereçadas a um destinatário específico ou que contêm palavras específicas na linha de assunto são protegidas de acesso não autorizado, e os destinatários não podem copiar ou imprimir o conteúdo da mensagem.
  
Ao contrário da versão anterior do OME, esses novos recursos oferecem uma experiência de remetente unificada, se você estiver enviando email dentro da organização ou para destinatários fora do Office 365. Além disso, os destinatários que recebem uma mensagem de email protegido enviada para uma conta do Office 365 no 2016 do Outlook ou no Outlook na web, não precisa realizar nenhuma ação adicional para exibir a mensagem. Ele funciona com facilidade. Destinatários usando outros clientes de email e provedores de serviços de email também têm uma experiência aprimorada. Para obter informações, consulte [aprender sobre mensagens protegidas no Office 365](https://support.office.com/article/Learn-about-protected-messages-in-Office-365-2baf3ac7-12db-40a4-8af7-1852204b4b67) e [como abrir uma mensagem protegida](https://support.office.com/article/How-do-I-open-a-protected-message-1157a286-8ecc-4b1e-ac43-2a608fbf3098).
  
## <a name="steps-to-manually-set-up-the-new-capabilities-for-ome"></a>Etapas para configurar manualmente os novos recursos para o OME

Se sua organização não tiver OME habilitado automaticamente, ou se você ativou o OME desativado, siga estas etapas para configurar manualmente os novos recursos para o OME.
  
### <a name="to-manually-set-up-the-new-capabilities-for-ome"></a>Para configurar manualmente os novos recursos para o OME

1. Certifique-se de que você tenha a assinatura certa para sua organização. Para obter informações sobre inscrições, consulte "quais assinaturas preciso usar o novo capabilities? OME" in a [Perguntas frequentes sobre a criptografia de mensagem do Office 365.](ome-faq.md) Para obter informações sobre como adquirir uma assinatura à proteção de informações do Windows Azure, consulte [Proteção de informações do Windows Azure](https://azure.microsoft.com/services/information-protection/).
    
2. Decida se deseja que a Microsoft para gerenciar a chave de raiz para a proteção de informações do Windows Azure (padrão), ou gerar e gerenciar essa chave sozinho (conhecido como trazer sua própria chave ou BYOK). Se você deseja gerar e gerenciar essa chave por conta própria, você precisará concluir algumas etapas antes de configurar os novos recursos para o OME. Para obter mais informações, consulte [planejamento e implementação de sua chave do locatário de proteção de informações do Windows Azure](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key). A Microsoft recomenda que você conclua estas etapas para configurar o OME.
    
3. Habilite os novos recursos para o OME ativando o Azure Rights Management. Para obter instruções, consulte [Ativar o Azure Rights Management](https://docs.microsoft.com/azure/information-protection/deploy-use/activate-service). Quando você fizer isso, o Office 365 habilita automaticamente as novas capacidades OME para você.
    
    > [!TIP]
    > Outlook na Web caches sua interface do usuário, portanto, é uma boa ideia esperar um dia antes de tentar aplicar os novos recursos para OME para mensagens de email usando este cliente. Antes da interface do usuário é atualizado para refletir a nova configuração, os novos recursos para o OME não estarão disponíveis. Depois que a interface do usuário atualiza, os usuários podem proteger mensagens de email usando os novos recursos para o OME. 
  
4. (Opcional) Configure as novas regras de fluxo de email ou atualizar as regras de fluxo de email existentes que definem como e quando você deseja que o Office 365 para criptografar mensagens enviadas de sua organização.
    
## <a name="verify-that-the-new-capabilities-for-ome-are-configured-properly-by-using-windows-powershell"></a>Verificar se os novos recursos para o OME estão configurados corretamente usando o Windows PowerShell

Siga estas etapas para verificar se o seu locatário está configurado corretamente para usar os novos recursos para o OME por meio do PowerShell do Exchange Online.
  
1. Usando uma conta de trabalho ou da escola que tenha permissões de administrador global na sua organização do Office 365, iniciar uma sessão do Windows PowerShell e se conectar ao Exchange Online. Para obter instruções, consulte [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).
    
2. Execute o cmdlet Test-IRMConfiguration usando a seguinte sintaxe:
    
  ```
  Test-IRMConfiguration [-Sender <email address >]
  ```

    Por exemplo:
    
  ```
  Test-IRMConfiguration -Sender securityadmin@contoso.com
  ```

    Onde o endereço de email é o endereço de email de um usuário em sua organização do Office 365. Embora opcional, oferecendo um endereço de email do remetente força o sistema para executar verificações adicionais.
    
    Os resultados devem se parecer com estas:
    
  ```
  Results : Acquiring RMS Templates ...
                - PASS: RMS Templates acquired.  Templates available: Contoso  - Confidential View Only, Contoso  - Confidential, Do Not 
            Forward.
            Verifying encryption ...
                - PASS: Encryption verified successfully.
            Verifying decryption ...
                - PASS: Decryption verified successfully.
            Verifying IRM is enabled ...
                - PASS: IRM verified successfully.
            
            OVERALL RESULT: PASS
  ```

    Onde *Contoso* é substituído com o nome da sua organização do Office 365. 
    
    Os nomes dos modelos padrão retornados nos resultados podem ser diferentes dos exibidos nos resultados da acima.
    
    Para obter uma introdução aos modelos e informações sobre os modelos padrão, consulte [Configurando e gerenciando modelos de proteção de informações do Windows Azure](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates). Para obter informações sobre não encaminhar opção, a opção de criptografar somente e como criar modelos adicionais ou Descubra quais direitos estão incluídos em um modelo existente, consulte [Configurando os direitos de uso para o gerenciamento de direitos do Windows Azure](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights).
    
3. Execute o cmdlet Remove-PSSession para desconectar o serviço de gerenciamento de direitos.
    
  ```
  Remove-PSSession $session
  ```

## <a name="next-steps-define-new-mail-flow-rules-that-use-the-new-ome-capabilities"></a>Próximas etapas: definir novas regras de fluxo de email que usam os novos recursos OME
<a name="Rules_1"> </a>

Esta etapa é opcional para novas implantações OME, no entanto, esta etapa é necessária para implantações OME existentes que já têm regras de fluxo de correio configuradas para criptografar emails de saída. Se você quiser tirar vantagem dos novos recursos OME, você deve atualizar suas regras de fluxo de email existente. Caso contrário, os usuários continuarão receber emails criptografados que usa o formato de anexo HTML anterior, em vez da experiência OME nova e sem interrupções.
  
Regras de fluxo de email determinam em email quais condições a mensagens devem ser criptografadas, bem como condições para que a criptografia de remoção. Quando você define uma ação para uma regra, todas as mensagens que correspondam às condições de regra são criptografadas quando são enviados.
  
Para obter mais informações sobre regras de fluxo de correio, consulte [definir regras de fluxo de email para criptografar mensagens de email no Office 365](define-mail-flow-rules-to-encrypt-email.md).
  
## <a name="related-topics"></a>Tópicos relacionados
<a name="Rules_1"> </a>

[Enviar, visualizar e responder a mensagens criptografadas no Outlook](https://support.office.com/article/eaa43495-9bbb-4fca-922a-df90dee51980.aspx)
  
[Enable-Aadrm](https://docs.microsoft.com/powershell/module/aadrm/enable-aadrm?view=azureipps)
  
[Conectar-se ao Exchange Online usando o PowerShell Remoto](https://technet.microsoft.com/library/jj984289%28v=exchg.160%29.aspx)
  
[Definir regras de fluxo de email para criptografar mensagens de email no Office 365](define-mail-flow-rules-to-encrypt-email.md)
  


---
title: Configurar novos recursos de Criptografia de Mensagens do Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 7ff0c040-b25c-4378-9904-b1b50210d00e
description: Novos recursos de criptografia de mensagens do Office 365 criados sobre a proteção de informações do Azure, sua organização pode usar comunicação de email protegido com pessoas dentro e fora da sua organização. Os novos recursos do OME funcionam com outras organizações do Office 365, Outlook.com, Gmail e outros serviços de email.
ms.openlocfilehash: eddafca15fa4efdd3f929145e7933a3b7dfb5f27
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220641"
---
# <a name="set-up-new-office-365-message-encryption-capabilities"></a>Configurar novos recursos de Criptografia de Mensagens do Office 365

Com os novos recursos de criptografia de mensagens do Office 365 (OME), que aproveitam os recursos de proteção na proteção de informações do Azure, sua organização pode compartilhar facilmente email protegido com qualquer pessoa em qualquer dispositivo. Os usuários podem enviar e receber mensagens protegidas com outras organizações do Office 365, bem como clientes não-Office 365, usando o Outlook.com, o Gmail e outros serviços de email.

||
|:-----|
|Este artigo faz parte de uma série maior de artigos sobre a criptografia de mensagens do Office 365. Este artigo destina-se a administradores e ITPros. Se você estiver apenas procurando informações sobre como enviar ou receber uma mensagem criptografada, consulte a lista de artigos na [ome (criptografia de mensagens do Office 365)](ome.md) e localize o artigo que melhor atende às suas necessidades. |
||

## <a name="get-started-with-ome-by-activating-azure-rights-management-part-of-azure-information-protection"></a>Introdução ao OME ativando o Azure Rights Management, parte da proteção de informações do Azure

Agora é fácil começar a usar os novos recursos do OME. A partir de fevereiro de 2018, o Office 365 habilita automaticamente os novos recursos do OME para organizações qualificadas em nossos data centers. Sua organização estará qualificada se for um novo locatário do Office 365 e sua organização tiver as assinaturas apropriadas. **Se você tiver habilitado o Azure Rights Management (Azure RMS), parte da proteção de informações do Azure, habilitará automaticamente a criptografia de mensagem do Office 365 para você.** Você não precisa fazer mais nada para habilitar o OME. Para ativar o Azure Rights Management, confira ativando o [Azure Rights Management](https://docs.microsoft.com/azure/information-protection/deploy-use/activate-service). Para obter informações sobre assinaturas, consulte "What subscriptions I use the New OME capabilities?" nas [perguntas frequentes sobre a criptografia de mensagens do Office 365](ome-faq.md). Para obter informações sobre como adquirir uma assinatura para a proteção de informações do Azure, consulte [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).
  
Se estiver usando o Exchange Online com o Active Directory Rights Management Service (AD RMS), você não poderá habilitar esses novos recursos imediatamente. Em vez disso, você precisa migrar primeiro do AD RMS para a proteção de informações do Azure. Após concluir a migração, você poderá concluir essas etapas com êxito.
  
Se você optar por continuar a usar o AD RMS local com o Exchange Online em vez de migrar para a proteção de informações do Azure, não será possível usar esses novos recursos.
  
## <a name="how-the-new-capabilities-for-ome-work"></a>Como os novos recursos para o OME funcionam

Os novos recursos de criptografia de mensagem do Office 365 usam os recursos de proteção, também chamados de Azure Rights Management (Azure RMS), da proteção de informações do Azure. Isso inclui políticas de criptografia, identidade e autorização para ajudar a proteger seu email. Você pode criptografar mensagens usando modelos de gerenciamento de direitos, a [opção](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails)não encaminhar e a [opção somente criptografia](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails). Os usuários podem então criptografar mensagens de email e uma variedade de anexos do Office 365 usando essas opções. Para obter uma lista completa de tipos de anexo compatíveis, consulte ["tipos de arquivo cobertos por políticas de IRM quando estão anexados a mensagens" em Introdução ao IRM para mensagens de email](https://support.office.com/article/bb643d33-4a3f-4ac7-9770-fd50d95f58dc#FileTypesforIRM). Como administrador, você também pode definir regras de fluxo de email para aplicar essa proteção. Por exemplo, você pode definir uma regra onde todas as mensagens não protegidas endereçadas a um destinatário específico ou que contenham palavras específicas na linha de assunto são protegidas de acesso não autorizado e os destinatários não podem copiar nem imprimir o conteúdo da mensagem.
  
Ao contrário da versão anterior do OME, esses novos recursos oferecem uma experiência de remetente unificado se você estiver enviando emails dentro da sua organização ou para destinatários fora do Office 365. Além disso, os destinatários que recebem uma mensagem de email protegida enviadas para uma conta do Office 365 no Outlook 2016 ou no Outlook na Web não precisam realizar qualquer ação adicional para exibir a mensagem. Funciona perfeitamente. Os destinatários que usam outros clientes de email e provedores de serviço de email também têm uma experiência aprimorada. Para obter informações, consulte [saiba mais sobre mensagens protegidas no Office 365](https://support.office.com/article/Learn-about-protected-messages-in-Office-365-2baf3ac7-12db-40a4-8af7-1852204b4b67) e [como eu abro uma mensagem protegida](https://support.office.com/article/How-do-I-open-a-protected-message-1157a286-8ecc-4b1e-ac43-2a608fbf3098).

Para obter uma lista detalhada das diferenças entre a versão anterior do OME e os novos recursos do OME, consulte [comparar versões do ome](ome-version-comparison.md).
  
## <a name="steps-to-manually-set-up-the-new-capabilities-for-ome"></a>Etapas para configurar manualmente os novos recursos para o OME

Os novos recursos do OME são automaticamente habilitados para a maioria das organizações do Office 365. Se sua organização não tiver o OME habilitado automaticamente ou se você desativou os novos recursos do OME, siga estas etapas para configurar manualmente os novos recursos para o OME.
  
### <a name="to-manually-set-up-the-new-capabilities-for-ome"></a>Para configurar manualmente os novos recursos do OME

1. Verifique se você tem a assinatura certa para sua organização. Para obter informações sobre inscrições, consulte "quais assinaturas eu preciso usar o novo OME capabilities?", nas [perguntas frequentes de criptografia de mensagem do Office 365.](ome-faq.md) Para obter informações sobre como adquirir uma assinatura para a proteção de informações do Azure, consulte [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).

2. Decida se você deseja que a Microsoft gerencie a chave raiz da proteção de informações do Azure (o padrão), ou gere e gerencie essa chave por conta própria (conhecida como trazer sua própria chave ou BYOK). Se você deseja gerar e gerenciar essa chave sozinho, precisa concluir algumas etapas antes de configurar os novos recursos do OME. Para obter mais informações, consulte [Planning and Implementing Your Azure Information Protection locatário Key](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key). A Microsoft recomenda que você conclua estas etapas antes de configurar o OME.

3. Habilite os novos recursos do OME ativando o Azure Rights Management. Para obter instruções, consulte Ativando o [Azure Rights Management](https://docs.microsoft.com/azure/information-protection/deploy-use/activate-service). Ao fazer isso, o Office 365 habilita automaticamente os novos recursos do OME para você.

    > [!TIP]
    > O Outlook na Web armazena sua interface do usuário em cache, portanto, é uma boa ideia aguardar um dia antes de tentar aplicar os novos recursos do OME a mensagens de email usando esse cliente. Antes que as atualizações da interface do usuário reflitam a nova configuração, os novos recursos do OME não estarão disponíveis. Após as atualizações da interface do usuário, os usuários podem proteger mensagens de email usando os novos recursos do OME.
  
4. Opcion Configure novas regras de fluxo de email ou atualize regras de fluxo de email existentes que definem como e quando você deseja que o Office 365 criptografe as mensagens enviadas da sua organização.

## <a name="verify-that-the-new-capabilities-for-ome-are-configured-properly-by-using-windows-powershell"></a>Verificar se os novos recursos do OME estão configurados corretamente usando o Windows PowerShell

Siga estas etapas para verificar se o locatário está configurado corretamente para usar os novos recursos do OME através do PowerShell do Exchange Online.
  
1. Usando uma conta corporativa ou de estudante que tenha permissões de administrador global em sua organização do Office 365, inicie uma sessão do Windows PowerShell e conecte-se ao Exchange Online. Para obter instruções, consulte [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Execute o cmdlet Test-IRMConfiguration usando a seguinte sintaxe:

     ```powershell
     Test-IRMConfiguration [-Sender <email address >]
     ```  

   Por exemplo:

     ```powershell
     Test-IRMConfiguration -Sender securityadmin@contoso.com
     ```

    Onde endereço de email é o endereço de email de um usuário em sua organização do Office 365. Embora opcional, fornecer um endereço de email do remetente força o sistema a executar verificações adicionais. Os resultados devem ter a seguinte aparência:

     ```text
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

    Onde a *contoso* é substituída pelo nome da sua organização do Office 365.

    Os nomes dos modelos padrão retornados nos resultados podem ser diferentes daqueles exibidos nos resultados acima.

    Para obter uma introdução aos modelos e informações sobre os modelos padrão, confira conFigurando [e Gerenciando modelos para a proteção de informações do Azure](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates). Para obter informações sobre a opção não enCaminhar, somente criptografia e como criar modelos adicionais ou descobrir quais direitos estão incluídos em um modelo existente, consulte [Configuring Usage Rights for Azure Rights Management](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights).

3. Execute o cmdlet Remove-PSSession para desconectar do serviço de gerenciamento de direitos.
    
     ```powershell
     Remove-PSSession $session
     ```

## <a name="next-steps-define-new-mail-flow-rules-that-use-the-new-ome-capabilities"></a>Próximas etapas: definir novas regras de fluxo de emails que usam os novos recursos do OME

Esta etapa é opcional para novas implantações do OME, mas essa etapa é necessária para implantações existentes do OME que já têm regras de fluxo de email configuradas para criptografar emails de saída. Se quiser aproveitar os novos recursos do OME, você deve atualizar suas regras de fluxo de emails existentes. Caso contrário, seus usuários continuarão a receber emails criptografados que usam o formato de anexo HTML anterior em vez da nova experiência de OME sem problemas.
  
As regras de fluxo de emails determinam sob quais condições as mensagens de email devem ser criptografadas, bem como as condições para remover essa criptografia. Quando você define uma ação para uma regra, quaisquer mensagens que correspondam às condições de regra são criptografadas quando são enviadas.
  
Para obter mais informações sobre regras de fluxo de emails, consulte [definir regras de fluxo de email para criptografar mensagens de email no Office 365](define-mail-flow-rules-to-encrypt-email.md).
  
## <a name="related-topics"></a>Tópicos Relacionados

[Enviar, exibir e responder a mensagens criptografadas no Outlook](https://support.office.com/article/eaa43495-9bbb-4fca-922a-df90dee51980.aspx)
  
[Enable-Aadrm](https://docs.microsoft.com/powershell/module/aadrm/enable-aadrm?view=azureipps)
  
[Conectar-se ao Exchange Online usando o PowerShell Remoto](https://technet.microsoft.com/library/jj984289%28v=exchg.160%29.aspx)
  
[Definir regras de fluxo de e-mail para criptografar mensagens de e-mail no Office 365](define-mail-flow-rules-to-encrypt-email.md)

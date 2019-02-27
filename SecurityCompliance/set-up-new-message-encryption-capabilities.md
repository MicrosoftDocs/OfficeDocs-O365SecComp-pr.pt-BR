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
ms.openlocfilehash: 90247a7e3cd7e5978eb144a2b6f66a9de21a8f96
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296184"
---
# <a name="set-up-new-office-365-message-encryption-capabilities"></a>Configurar novos recursos de Criptografia de Mensagens do Office 365

Os novos recursos do Office 365 Message Encryption (OME) permitem que as organizações compartilhem emails protegidos com qualquer pessoa em qualquer dispositivo. Os usuários podem trocar mensagens protegidas com outras organizações do Office 365, bem como clientes não-Office 365 que usam o Outlook.com, o Gmail e outros serviços de email.


>[!NOTE]
>Este artigo destina-se a administradores e profissionais de ti. Se você for um usuário final, consulte a lista de artigos no [Office 365 Message Encryption (ome)](ome.md) para obter soluções apropriadas.

Siga as etapas abaixo para garantir que os novos recursos do OME estão disponíveis em seu locatário do Office 365. 

## <a name="verify-azure-rights-management-arm-is-active"></a>Verificar se o Azure Rights Management (ARM) está ativo

>[!NOTE]
>Os novos recursos do OME aproveitam os recursos de proteção na [proteção de informações do Azure](https://docs.microsoft.com/en-us/azure/information-protection/what-is-information-protection), a tecnologia usada pelo [ARM (Azure Rights Management)](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms).

O único pré-requisito para usar os novos recursos do OME é que o [Azure Rights Management (ARM)](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms) deve ser ativado em seu locatário do Office 365. Se for, o Office 365 ativa os novos recursos do OME automaticamente e você não precisa fazer nada. 

O ARM também é ativado automaticamente para os planos mais qualificados e, portanto, você provavelmente não precisará fazer nada nesse sentido. ConFira ativando o [Azure Rights Management](https://docs.microsoft.com/en-gb/azure/information-protection/activate-service) para mais.

>[!IMPORTANT]
>Se você usar o AD RMS (Active Directory Rights Management Service) com o Exchange Online, precisará [migrar para a proteção de informações do Azure](https://docs.microsoft.com/en-us/azure/information-protection/migrate-from-ad-rms-to-azure-rms) antes de poder usar os novos recursos do ome. O AD RMS não é compatível com o ARM.  

Para saber mais, confira:

- [Quais assinaturas são necessárias para usar os novos recursos do ome?](ome-faq.md#what-subscriptions-do-i-need-to-use-the-new-ome-capabilities) para verificar se o seu plano de assinatura inclui a proteção de informações do Azure (que inclui o ARM).   
-  [Proteção de informações do Azure](https://azure.microsoft.com/en-us/services/information-protection/) para obter informações sobre como adquirir uma assinatura qualificada.  

### <a name="manually-activating-arm"></a>Ativando o braço manualmente

Se você desabilitou o braço, ou se ele não foi ativado automaticamente por algum motivo, você pode ativá-lo manualmente no:

- **Centro de administração do office 365**: Confira [como ativar o Azure Rights Management no centro de administração do Office 365](https://docs.microsoft.com/en-us/azure/information-protection/activate-office365) para obter instruções
- **Portal do Azure**: Confira [como ativar o Azure Rights Management no portal do Azure](https://docs.microsoft.com/en-gb/azure/information-protection/activate-azure) para obter instruções. 


## <a name="configure-management-of-your-azure-information-protection-tenant-key"></a>Configurar o gerenciamento de sua chave do locatário de proteção de informações do Azure

Esta é uma etapa opcional. Permitir que a Microsoft gerencie a chave raiz da proteção de informações do Azure é a configuração padrão e a prática recomendada recomendada para a maioria dos locatários do Office 365. Se esse for o caso, não será necessário fazer nada. 

Há vários motivos, por exemplo, requisitos de conformidade, que podem exigir a geração e o gerenciamento de sua própria chave raiz (também conhecida como trazer sua própria chave (BYOK)). Se esse for o caso, recomendamos que você conclua as etapas necessárias antes de configurar os novos recursos do OME. ConFira [o planejamento e a implementação da chave do locatário de proteção de informações do Azure](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key) para mais. 


## <a name="verify-new-ome-configuration-in-exchange-online-powershell"></a>Verificar a nova configuração do OME no PowerShell do Exchange Online

Você pode verificar se o seu locatário do Office 365 está configurado corretamente para usar os novos recursos do OME no [PowerShell do Exchange Online](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).
  
1. [Conecte-se ao PowerShell do Exchange Online](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) usando uma conta com permissões de administrador global em seu locatário do Office 365.

2. Execute o cmdlet Test-IRMConfiguration usando a seguinte sintaxe:

     ```powershell
     Test-IRMConfiguration [-Sender <email address >]
     ```  

   **Exemplo**: 
   
     ```powershell
     Test-IRMConfiguration -Sender securityadmin@contoso.com
     ```
     
     - Fornecer um email de remetente é opcional, mas obriga o sistema a executar verificações adicionais. Use o endereço de email de qualquer usuário em seu locatário do Office 365. 
     
    Os resultados devem ser semelhantes a:

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

   - O nome da organização do Office 365 substituirá *contoso*.

   - Os nomes de modelo padrão podem ser diferentes dos exibidos acima. ConFira conFigurando [e Gerenciando modelos para a proteção de informações do Azure](https://docs.microsoft.com/en-us/azure/information-protection/configure-policy-templates) para mais.

3. Execute o cmdlet Remove-PSSession para desconectar do serviço de gerenciamento de direitos.
    
     ```powershell
     Remove-PSSession $session
     ```

## <a name="update-mail-flow-rules-to-use-new-ome-capabilities"></a>Atualizar regras de fluxo de email para usar novos recursos do OME

Se houver [regras de fluxo de email](define-mail-flow-rules-to-encrypt-email.md) configuradas anteriormente para criptografar emails em seu locatário do Office 365, você precisará atualizar essas regras existentes para usar os novos recursos do ome. Para novas implantações, esta etapa não é necessária neste estágio.   

>[!Note]
>As regras de fluxo de email definem as condições sob as quais as mensagens de email são criptografadas e quando a criptografia deve ser removida. ConFira [definir regras de fluxo de emails para criptografar mensagens de email no Office 365](define-mail-flow-rules-to-encrypt-email.md) .

Para atualizar as regras existentes para usar os novos recursos do OME:

1. No centro de administração do Office 365, acesse **centros de administração _GT_ Exchange**.

2. No centro de administração do Exchange, acesse **regras de > de fluxo**de emails. 
3. Para cada regra, em **faça o seguinte**:
    - Selecione **Modificar a segurança da mensagem**.
    - Selecione **aplicar a criptografia de mensagem do Office 365 e proteção de direitos**.
    - Selecionar um modelo do RMS na lista
    - Selecione **Salvar**.
    - Selecione **OK**.
  
>[!IMPORTANT]
>Se você não atualizar as regras de fluxo de emails existentes, seus usuários continuarão a receber emails criptografados que usam o formato de anexo HTML anterior, em vez dos novos recursos do OME.

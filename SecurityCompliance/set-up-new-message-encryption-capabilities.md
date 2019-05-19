---
title: Configurar novos recursos de Criptografia de Mensagens do Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/30/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 7ff0c040-b25c-4378-9904-b1b50210d00e
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Novos recursos de criptografia de mensagens do Office 365 criados sobre a proteção de informações do Azure, sua organização pode usar comunicação de email protegido com pessoas dentro e fora da sua organização. Os novos recursos do OME funcionam com outras organizações do Office 365, Outlook.com, Gmail e outros serviços de email.
ms.openlocfilehash: 415e598a28033271b115aff639fb1ddd7a6345af
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34156503"
---
# <a name="set-up-new-office-365-message-encryption-capabilities"></a>Configurar novos recursos de Criptografia de Mensagens do Office 365

Os novos recursos do Office 365 Message Encryption (OME) permitem que as organizações compartilhem emails protegidos com qualquer pessoa em qualquer dispositivo. Os usuários podem trocar mensagens protegidas com outras organizações do Office 365, bem como clientes não-Office 365 que usam o Outlook.com, o Gmail e outros serviços de email.

||
|:-----|
|Este artigo faz parte de uma série maior de artigos sobre a criptografia de mensagens do Office 365. Este artigo destina-se a administradores e profissionais de ti. Se você estiver apenas procurando informações sobre como enviar ou receber uma mensagem criptografada, consulte a lista de artigos na [ome (criptografia de mensagens do Office 365)](ome.md) e localize o artigo que melhor atende às suas necessidades. |
||

Siga as etapas abaixo para garantir que os novos recursos do OME estão disponíveis na sua organização do Office 365.

## <a name="verify-that-azure-rights-management-is-active"></a>Verificar se o Azure Rights Management está ativo

Os novos recursos do OME aproveitam os recursos de proteção no [Azure Rights Management Services (Azure RMS)](https://docs.microsoft.com/en-us/azure/information-protection/what-is-information-protection), a tecnologia usada pela [proteção de informações do Azure](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms) para proteger emails e documentos por meio de controles de criptografia e acesso.

O único pré-requisito para usar os novos recursos do OME é que o [Azure Rights Management](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms) deve ser ativado no locatário da sua organização. Se for, o Office 365 ativa os novos recursos do OME automaticamente e você não precisa fazer nada.

O Azure RMS também é ativado automaticamente para os planos mais qualificados e, portanto, você provavelmente não precisará fazer nada nesse sentido. Confira ativando o [Azure Rights Management](https://docs.microsoft.com/en-gb/azure/information-protection/activate-service) para obter mais informações.

>[!IMPORTANT]
>Se você usar o AD RMS (Active Directory Rights Management Service) com o Exchange Online, precisará [migrar para a proteção de informações do Azure](https://docs.microsoft.com/en-us/azure/information-protection/migrate-from-ad-rms-to-azure-rms) antes de poder usar os novos recursos do ome. OME não é compatível com o AD RMS.  

Para obter mais informações, consulte:

- [Quais assinaturas são necessárias para usar os novos recursos do ome?](ome-faq.md#what-subscriptions-do-i-need-to-use-the-new-ome-capabilities) para verificar se o seu plano de assinatura inclui a proteção de informações do Azure (que inclui a funcionalidade do Azure RMS).
- [Proteção de informações do Azure](https://azure.microsoft.com/en-us/services/information-protection/) para obter informações sobre como adquirir uma assinatura qualificada.  

### <a name="manually-activating-azure-rights-management"></a>Ativando manualmente o Azure Rights Management

Se você desabilitou o Azure RMS, ou se ele não foi ativado automaticamente por algum motivo, você pode ativá-lo manualmente no:

- **Centro de administração do office 365**: Confira [como ativar o Azure Rights Management no centro de administração do Office 365](https://docs.microsoft.com/en-us/azure/information-protection/activate-office365) para obter instruções.
- **Portal do Azure**: Confira [como ativar o Azure Rights Management no portal do Azure](https://docs.microsoft.com/en-gb/azure/information-protection/activate-azure) para obter instruções.

## <a name="configure-management-of-your-azure-information-protection-tenant-key"></a>Configurar o gerenciamento de sua chave do locatário de proteção de informações do Azure

Esta é uma etapa opcional. Permitir que a Microsoft gerencie a chave raiz da proteção de informações do Azure é a configuração padrão e a prática recomendada recomendada para a maioria dos locatários do Office 365. Se esse for o caso, não será necessário fazer nada.

Há vários motivos, por exemplo, requisitos de conformidade, que podem exigir a geração e o gerenciamento de sua própria chave raiz (também conhecida como trazer sua própria chave (BYOK)). Se esse for o caso, recomendamos que você conclua as etapas necessárias antes de configurar os novos recursos do OME. Confira [o planejamento e a implementação da chave do locatário de proteção de informações do Azure](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key) para mais.

## <a name="verify-new-ome-configuration-in-exchange-online-powershell"></a>Verificar a nova configuração do OME no PowerShell do Exchange Online

Você pode verificar se o seu locatário do Office 365 está configurado corretamente para usar os novos recursos do OME no [PowerShell do Exchange Online](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).
  
1. [Conecte-se ao PowerShell do Exchange Online](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) usando uma conta com permissões de administrador global em seu locatário do Office 365.

2. Execute o cmdlet Get-IRMConfiguration.

     Você deve ver um valor de $True para o parâmetro AzureRMSLicensingEnabled, que indica que o OME está configurado em seu locatário. Se não estiver, use Set-IRMConfiguration para definir o valor de AzureRMSLicensingEnabled como $True para habilitar o OME.

3. Execute o cmdlet Test-IRMConfiguration usando a seguinte sintaxe:

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

   - Os nomes de modelo padrão podem ser diferentes dos exibidos acima. Confira Configurando [e Gerenciando modelos para a proteção de informações do Azure](https://docs.microsoft.com/en-us/azure/information-protection/configure-policy-templates) para mais.

4. Execute o cmdlet Remove-PSSession para desconectar do serviço de gerenciamento de direitos.

     ```powershell
     Remove-PSSession $session
     ```

## <a name="next-steps-define-mail-flow-rules-to-use-new-ome-capabilities"></a>Próximas etapas: definir regras de fluxo de email para usar novos recursos do OME

Se houver regras de fluxo de email configuradas anteriormente para criptografar emails na sua organização do Office 365, você precisará atualizar as regras existentes para usar os novos recursos do OME. Para novas implantações, você precisa criar novas regras de fluxo de emails.

>[!IMPORTANT]
>Se você não atualizar as regras de fluxo de emails existentes, seus usuários continuarão a receber emails criptografados que usam o formato de anexo HTML anterior, em vez da nova experiência de OME perfeita.

As regras de fluxo de emails determinam sob quais condições as mensagens de email devem ser criptografadas, bem como as condições para remover essa criptografia. Quando você define uma ação para uma regra, quaisquer mensagens que correspondam às condições de regra são criptografadas quando são enviadas.
  
Para obter etapas sobre como criar regras de fluxo de email para o OME, consulte [definir regras de fluxo de emails para criptografar mensagens de email no Office 365](define-mail-flow-rules-to-encrypt-email.md).

Para atualizar as regras existentes para usar os novos recursos do OME:

1. No centro de administração do Office 365, acesse **centros de administração _GT_ Exchange**.
2. No centro de administração do Exchange, acesse **regras de > de fluxo**de emails.
3. Para cada regra, em **faça o seguinte**:
    - Selecione **Modificar a segurança da mensagem**.
    - Selecione **aplicar a criptografia de mensagem do Office 365 e proteção de direitos**.
    - Selecione um modelo do RMS na lista.
    - Selecione **Salvar**.
    - Selecione **OK**.

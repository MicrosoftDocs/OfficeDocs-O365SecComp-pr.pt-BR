---
title: Configurar novos recursos de Criptografia de Mensagens do Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/30/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.assetid: 7ff0c040-b25c-4378-9904-b1b50210d00e
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Novos recursos de criptografia de mensagens do Office 365 criados no topo da proteção de informações do Azure, sua organização pode usar comunicações de email protegidas com pessoas dentro e fora da sua organização. Os novos recursos do OME funcionam com outras organizações do Office 365, Outlook.com, Gmail e outros serviços de email.
ms.openlocfilehash: 835b1d6f40868684536dbea8f75dab0665950210
ms.sourcegitcommit: 33c8e9c16143650ca443d73e91631f9180a9268e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35854795"
---
# <a name="set-up-new-office-365-message-encryption-capabilities"></a>Configurar novos recursos de Criptografia de Mensagens do Office 365

Os novos recursos de criptografia de mensagens do Office 365 (OME) permitem que as organizações compartilhem emails protegidos com qualquer pessoa em qualquer dispositivo. Os usuários podem trocar mensagens protegidas com outras organizações do Office 365, bem como os clientes que não têm o Office 365 usando Outlook.com, Gmail e outros serviços de email.

||
|:-----|
|Esse artigo faz parte de uma série maior de artigos sobre a criptografia de mensagens do Office 365. Este artigo é destinado a administradores e profissionais de TI. Se você estiver apenas procurando informações sobre como enviar ou receber uma mensagem criptografada, confira a lista de artigos em [Criptografia de Mensagens do Office 365 (OME)](ome.md) e localize o artigo que melhor atende às suas necessidades. |
||

Siga as etapas abaixo para garantir que os novos recursos do OME estejam disponíveis na sua organização do Office 365.

## <a name="verify-that-azure-rights-management-is-active"></a>Verifique se o Azure Rights Management está ativo

Os novos recursos da OME aproveitam os recursos de proteção no[Azure RMS (Azure Rights Management Services)](https://docs.microsoft.com/pt-BR/azure/information-protection/what-is-information-protection), e a tecnologia usada pela[Proteção de Informações do Azure](https://docs.microsoft.com/pt-BR/azure/information-protection/what-is-azure-rms) para proteger emails e documentos por meio de controles de criptografia e acesso.

O único pré-requisito para usar os novos recursos de OME que o [Azure Rights Management](https://docs.microsoft.com/pt-BR/azure/information-protection/what-is-azure-rms) deve ser ativado no locatário da sua organização. Caso esteja, o Office 365 ativa automaticamente os novos recursos de OME e você não precisa fazer nada.

O Azure RMS também é ativado automaticamente para a maioria dos planos qualificados, portanto, provavelmente você não precise fazer nada. Para saber mais confira [Ativar o Gerenciamento de Direitos do Azure](https://docs.microsoft.com/en-gb/azure/information-protection/activate-service).

>[!IMPORTANT]
>Se você usa o AD RMS (Active Directory Rights Management Services) com o Exchange Online, [é preciso migrar para a Proteção de Informações do Azure](https://docs.microsoft.com/pt-BR/azure/information-protection/migrate-from-ad-rms-to-azure-rms) antes de poder usar os novos recursos do OME. OME não é compatível com AD RMS.  

Para saber mais, veja:

- [Quais assinaturas eu preciso para usar os novos recursos do OME? ](ome-faq.md#what-subscriptions-do-i-need-to-use-the-new-ome-capabilities) para verificar se o seu plano de assinatura inclui a proteção de informações do Azure (que inclui a funcionalidade do Azure RMS).
- [Proteção de Informações do Azure](https://azure.microsoft.com/en-us/services/information-protection/) para saber mais sobre como adquirir uma assinatura qualificada.  

### <a name="manually-activating-azure-rights-management"></a>Ativar manualmente o Gerenciamento de Direitos do Azure

Se você tiver desabilitado o Azure RMS, ou se ele não tiver sido ativado automaticamente por algum motivo, você poderá ativá-lo manualmente no:

- 
  **Centro de administração do Microsoft 365** Confira [: Como ativar o Azure Rights Management no centro de administração](https://docs.microsoft.com/pt-BR/azure/information-protection/activate-office365) para obter instruções.
- **Portal do Azure**: [Confira como ativar o Azure Rights Management no portal do Azure](https://docs.microsoft.com/en-gb/azure/information-protection/activate-azure) para obter instruções.

## <a name="configure-management-of-your-azure-information-protection-tenant-key"></a>Configurar o gerenciamento de sua chave do locatário de proteção de informações do Azure

Esta etapa é opcional. Permitir que a Microsoft gerencie a chave raiz da proteção de informações do Azure é a configuração padrão e a melhor prática recomendada para a maioria dos locatários do Office 365. Se esse for o caso, você não precisa fazer nada.

Há muitos motivos, por exemplo, os requisitos de conformidade, que podem exigir a geração e o gerenciamento de sua própria chave raiz (também conhecida como (BYOK)). Se esse for o caso, recomendamos que você conclua as etapas necessárias antes de configurar os novos recursos do OME. Confira o artigo [Como planejar e implementar a chave locatário de proteção de informações do Azure](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key) para saber mais.

## <a name="verify-new-ome-configuration-in-exchange-online-powershell"></a>Verificar a nova configuração do OME no PowerShell do Exchange Online

Você pode verificar se o locatário do Office 365 está configurado corretamente para usar os novos recursos do Ome[no PowerShell do Exchange Online](https://docs.microsoft.com/pt-BR/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).
  
1. 
  [Conecte-se ao Exchange Online do PowerShell](https://docs.microsoft.com/pt-BR/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) usando uma conta com permissões de administrador global em seu locatário do Office 365.

2. Execute o cmdlet Get-IRMConfiguration.

     Você deverá ver um valor de $True para o parâmetro AzureRMSLicensingEnabled, que indica que o OME está configurado em seu locatário. Caso contrário, use Set-IRMConfiguration para definir o valor de AzureRMSLicensingEnabled como $True para habilitar o OME.

3. Execute o cmdlet Test-IRMConfiguration usando a seguinte sintaxe:

     ```powershell
     Test-IRMConfiguration [-Sender <email address >]
     ```  

   **Exemplo**:

     ```powershell
     Test-IRMConfiguration -Sender securityadmin@contoso.com
     ```

     - Fornecer um email de remetente é opcional, mas força o sistema a executar verificações adicionais. Use o endereço de email de qualquer usuário em seu locatário do Office 365.

     Seus resultados devem ser semelhantes a:

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

   - O nome da sua organização do Office 365 substituirá *Contoso*.

   - Os nomes dos modelos padrão podem ser diferentes daqueles exibidos acima. Confira [Configurando e Gerenciando modelos para a proteção de informações do Azure](https://docs.microsoft.com/pt-BR/azure/information-protection/configure-policy-templates) para saber mais.

4. Execute o cmdlet Remove-PSSession para se desconectar do serviço de gerenciamento de direitos.

     ```powershell
     Remove-PSSession $session
     ```

## <a name="next-steps-define-mail-flow-rules-to-use-new-ome-capabilities"></a>Próximas etapas: definir regras de fluxo de emails para usar novos recursos do OME

Se houver regras de fluxo de email configuradas anteriormente para criptografar emails na sua organização do Office 365, você precisará atualizar as regras existentes para usar os novos recursos do OME. Para novas implantações, você precisa criar novas regras de fluxo de emails.

>[!IMPORTANT]
>Se você não atualizar as regras de fluxo de email existentes, os usuários continuarão a receber emails criptografados que usam o formato de anexo HTML anterior, em vez da nova experiência contínua do OME.

As regras de fluxo de email determinam em quais condições as mensagens de email devem ser criptografadas, bem como as condições para a remoção dessa criptografia. Quando você define uma ação para uma regra, todas as mensagens que correspondem às condições da regra são criptografadas quando são enviadas.
  
Para ver as etapas sobre como criar regras de fluxo, confira [Definir regras de fluxo de e-mail para criptografar mensagens de e-mail no Office 365](define-mail-flow-rules-to-encrypt-email.md).

Para atualizar regras existentes para usar os novos recursos do OME:

1. No Centro de administração do Microsoft 365, selecione **Centros de administração > Exchange**.
2. No Centro de administração do Exchange, acesse **Fluxo de email > Regras**.
3. Para cada regra, no ** siga este procedimento**:
    - Selecione **Modificar a segurança de mensagem**.
    - Selecione **Aplicar a Criptografia e os Direitos de Mensagem do Office 365**.
    - Selecione um modelo RMS na lista.
    - Selecione **Salvar**.
    - Selecione **OK**.

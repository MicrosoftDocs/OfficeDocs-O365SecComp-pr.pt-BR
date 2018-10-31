---
title: Configurar o Azure Rights Management para a Criptografia de Mensagens do Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/30/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2cba47b3-f09e-4911-9207-ac056fcb9db7
description: A versão anterior do Office 365 Message Encryption depende do Microsoft Azure Rights Management (anteriormente conhecida como Windows Azure Active Directory Rights Management).
ms.openlocfilehash: f8759da8628d4c78fe5409f5c47e3fc2b3e9484e
ms.sourcegitcommit: c05076501dfe118e575998ecfc08ad69d13c8abc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25853066"
---
# <a name="this-article-applies-to-the-previous-version-of-ome"></a>Este artigo aplica-se a versão anterior do OME
Se você ainda não migraram sua organização do Office 365 para os novos recursos OME, mas você já implantou OME, as informações neste artigo se aplicam à sua organização. A Microsoft recomenda que você faça um plano para mover-se para as novas capacidades OME tão logo razoáveis para sua organização. Para obter instruções, consulte [configurar novos recursos do Office 365 Message Encryption](set-up-new-message-encryption-capabilities.md). Se você deseja saber mais sobre como as novas capacidades funcionam pela primeira vez, consulte [Criptografia de mensagem do Office 365](ome.md). O restante deste artigo refere-se ao comportamento OME antes do lançamento de novos recursos OME.

# <a name="set-up-azure-rights-management-for-the-previous-version-of-office-365-message-encryption"></a>Configurar o Azure Rights Management para a versão anterior do Office 365 Message Encryption

Este tópico descreve as etapas que precisam ser seguidas para ativar e, em seguida, defina o Azure RMS (Rights Management), a parte de proteção de informações do Windows Azure, para uso com o Office 365 Message Encryption (OME).
  
## <a name="prerequisites-for-using-the-previous-version-of-office-365-message-encryption"></a>Pré-requisitos para usar a versão anterior do Office 365 Message Encryption
<a name="warmprereqs"> </a>

O Office 365 Message Encryption (OME), incluindo o IRM, depende do Azure Rights Management (RMS do Windows Azure). RMS Azure é a tecnologia de proteção usada pela proteção de informações do Windows Azure. Para usar o OME, sua organização do Office 365 deve incluir uma assinatura do Exchange Online ou Exchange Online Protection que, por sua vez, inclui uma assinatura de gerenciamento de direitos do Windows Azure.
  
- Se você não tiver certeza sobre o que inclui a sua assinatura, consulte as descrições de serviço Exchange Online para [política de mensagem, recuperação e conformidade](https://technet.microsoft.com/library/exchange-online-message-policy-recovery-and-compliance.aspx).
    
- Se você não tiver uma assinatura do Windows Azure RMS para Exchange Online ou Exchange Online Protection, você deve adquirir uma assinatura e ativá-lo primeiro.
    
    Para obter informações sobre como adquirir uma assinatura para o Azure Rights Management, consulte [Gerenciamento de direitos do Windows Azure](https://portal.office.com/Signup/MainSignUp15.aspx?&amp;OfferId=9DF77AF9-DAAE-4d51-8E0E-EEEADD4866B8&amp;dl=RIGHTSMANAGEMENT). A próxima seção fornece informações sobre como ativar o Azure Rights Management.
    
- Se você tiver o Azure Rights Management, mas ele não está configurado para o Exchange Online ou Exchange Online Protection, este artigo explica como ativar o Azure Rights Management e, em seguida o descreve a melhor maneira de configurar OME para funcionar com o Azure Rights Management.
    
- Se você já configurou OME para funcionar com o Azure Rights Management para o Exchange Online ou Exchange Online Protection, dependendo de como configurá-lo, você pode estar pronto para começar a usar o OME e seus novos recursos imediatamente. Este artigo explica como determinar se você configurou OME corretamente, o que fazer se você precisar alterar sua instalação e o que acontece se você optar por não alterar sua instalação. Por exemplo, para usar os novos recursos, você deve usar o RMS do Windows Azure com OME. Você não pode usar os novos recursos com um RMS diretório ativo do local.
    
## <a name="activate-azure-rights-management-for--the-previous-version-of-ome-in-office-365"></a>Ativar o Azure Rights Management para a versão anterior do OME no Office 365
<a name="activatewarm"> </a>

Você precisa ativar o Azure Rights Management para que os usuários em sua organização possam aplicar proteção de informações para mensagens enviadas por eles e abrir mensagens e arquivos que foram protegidos pelo serviço de gerenciamento de direitos do Windows Azure. Para obter instruções, consulte [Ativar o Azure Rights Management](https://go.microsoft.com/fwlink/p/?LinkId=525775). Depois de ter concluído a ativação, volte aqui e continuar com as tarefas neste artigo.
  
## <a name="set-up-the-previous-version-of-ome-to-use-azure-rms-by-importing-trusted-publishing-domains-tpds"></a>Configurar a versão anterior do OME para usar o Azure RMS importando domínios de publicação confiáveis (TPDs)
<a name="importTPDs"> </a>

O TPD é um arquivo XML que contém informações sobre configurações de gerenciamento de direitos da sua organização. Por exemplo, o TPD contém informações sobre o certificado de licenciador de servidor (SLC) usado para assinatura e criptografia de certificados e licenças, as URLs usadas para licenciamento e publicação e assim por diante. Você pode importar o TPD para sua organização do Office 365 usando o Windows PowerShell.
  
> [!IMPORTANT]
> Anteriormente, você pode optar por importar TPDs do serviço de gerenciamento de direitos do Active Directory (AD RMS) para sua organização do Office 365. No entanto, isso impedirá de usando os novos recursos OME e não é recomendado. Se sua organização estiver no momento do Office 365 configurado dessa forma, a Microsoft recomenda que você crie um plano para migrar do RMS de diretório ativo seu local à proteção de informações do Windows Azure baseados em nuvem. Para obter mais informações, consulte [Migrando do AD RMS à proteção de informações do Windows Azure](https://docs.microsoft.com/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms). Você não poderá usar os novos recursos OME até que tenha concluído a migração à proteção de informações do Windows Azure. 
  
 **Para importar TPDs do RMS do Azure**
  
1. [Conecte-se ao Exchange Online usando o PowerShell remoto](https://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).
    
2. Escolha a URL de compartilhamento de chave que corresponde à localização geográfica do sua organização Office 365:
    
|**Localização**|**URL do local de compartilhamento de chave**|
|:-----|:-----|
|América do Norte  <br/> |https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|União Europeia  <br/> |https://sp-rms.eu.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|Ásia  <br/> |https://sp-rms.ap.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|América do Sul  <br/> |https://sp-rms.sa.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|Office 365 para agências governamentais (Nuvem de Comunidade Governamental)  <br/> Este local de compartilhamento de chave do RMS é reservado para clientes que adquiriram o Office 365 para SKUs do governo.  <br/> |https://sp-rms.govus.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
   
3. Configure o local de compartilhamento de chave, executando o cmdlet [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.160%29.aspx) da seguinte maneira: 
    
  ```
  Set-IRMConfiguration -RMSOnlineKeySharingLocation "<RMSKeySharingURL >"
  ```

    Por exemplo, para configurar a chave local de compartilhamento se sua organização estiver localizada na América do Norte:
    
  ```
  Set-IRMConfiguration -RMSOnlineKeySharingLocation "https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc"
  ```

4. Execute o cmdlet [Import-RMSTrustedPublishingDomain](https://technet.microsoft.com/library/jj200724%28v=exchg.150%29.aspx) com a opção - RMSOnline para importar o TPD do gerenciamento de direitos do Windows Azure: 
    
  ```
  Import-RMSTrustedPublishingDomain -RMSOnline -Name "<TPDName> "
  ```

    Onde *TPDName* é o nome que você deseja usar para o TPD. Por exemplo, "Contoso North American TPD". 
    
5. Para verificar se você configurou com êxito sua organização do Office 365 para usar o serviço de gerenciamento de direitos do Windows Azure, execute o cmdlet [Test-IRMConfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.160%29.aspx) com a opção - RMSOnline, da seguinte maneira: 
    
  ```
  Test-IRMConfiguration -RMSOnline
  ```

    Entre outras coisas, este cmdlet verifica a conectividade com o serviço de gerenciamento de direitos do Windows Azure, baixa o TPD e verifica sua validade.
    
6. Execute o cmdlet [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) da seguinte maneira para desabilitar os modelos de gerenciamento de direitos do Windows Azure sejam disponíveis no Outlook na web e Outlook: 
    
  ```
  Set-IRMConfiguration -ClientAccessServerEnabled $false
  ```

7. Execute o cmdlet [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) da seguinte maneira para habilitar o Azure Rights Management para a sua organização de email baseada em nuvem e configurá-lo para usar o Azure Rights Management para a criptografia de mensagem do Office 365: 
    
  ```
  Set-IRMConfiguration -InternalLicensingEnabled $true
  ```

8. Para verificar que você com êxito importado o TPD e habilitou o Azure Rights Management, use o cmdlet Test-IRMConfiguration para testar a funcionalidade de gerenciamento de direitos do Windows Azure. Para obter detalhes, consulte "Exemplo 1" em [Test-IRMConfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.150%29.aspx).
    
## <a name="i-have-the-previous-version-of-ome-set-up-with-active-directory-rights-management-not-azure-information-protection-what-do-i-do"></a>Tenho a versão anterior do OME configurado com o Active Directory Rights Management não proteção de informações do Windows Azure, o que eu faço?
<a name="importTPDs"> </a>

Você pode continuar a usar suas regras de fluxo de email existentes do Office 365 Message Encryption com gerenciamento de direitos do Active Directory, mas não é possível configurar ou usar os novos recursos OME. Em vez disso, será preciso migrar à proteção de informações do Windows Azure. Para obter informações sobre migração e o que isso significa para sua organização, consulte [Migrando do AD RMS à proteção de informações do Windows Azure](https://docs.microsoft.com/information-protection/deploy-use/prepare-environment-adrms).
  
## <a name="next-steps"></a>Próximas etapas
<a name="importTPDs"> </a>

Depois que você tiver concluído a instalação do Azure Rights Management, se você deseja habilitar os novos recursos de OME, consulte [configurar novos recursos do Office 365 Message Encryption construídos sobre a proteção de informações do Azure.](https://support.office.com/article/7ff0c040-b25c-4378-9904-b1b50210d00e)
  
Depois de configurar sua organização para usar os novos recursos OME, você está pronto para [definir regras de fluxo de email para proteger as mensagens de email com os novos recursos OME](define-mail-flow-rules-to-encrypt-email.md).
  
## <a name="related-topics"></a>Tópicos relacionados
<a name="importTPDs"> </a>

[Criptografia no Office 365](encryption.md)
  
[Detalhes de referências técnicas sobre a criptografia no Office 365](technical-reference-details-about-encryption.md)
  
[Qual é o Azure Rights Management?](https://docs.microsoft.com/information-protection/understand-explore/what-is-azure-rms)
  


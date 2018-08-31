---
title: Recursos de proteção em aplicação a locatários do Office 365 existentes de proteção de informações do Azure
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/29/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 7ad6f58e-65d7-4c82-8e65-0b773666634d
description: Para ajudar a etapa inicial na protegendo suas informações, iniciando julho de 2018 todos os locatários elegíveis de proteção de informações do Azure serão tem os recursos de proteção em proteção de informações do Azure ativado por padrão. Os recursos de proteção em proteção de informações do Azure eram conhecidos anteriormente no Office 365, como gerenciamento de direitos ou RMS do Azure. Se sua organização tiver um plano de serviço do Office E3 ou um plano de serviço mais alto, que agora, você receberá um ponto de partida protegendo as informações por meio de proteção de informações do Azure quando podemos distribuir esses recursos.
ms.openlocfilehash: be0200da3032dccbcf54e67f3bdfbac800b65526
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523785"
---
# <a name="protection-features-in-azure-information-protection-rolling-out-to-existing-office-365-tenants"></a>Recursos de proteção em aplicação a locatários do Office 365 existentes de proteção de informações do Azure

Para ajudar a etapa inicial na protegendo suas informações, iniciando julho de 2018 todos os locatários elegíveis de proteção de informações do Azure serão tem os recursos de proteção em proteção de informações do Azure ativado por padrão. Os recursos de proteção em proteção de informações do Azure eram conhecidos anteriormente no Office 365, como gerenciamento de direitos ou RMS do Azure. Se sua organização tiver um plano de serviço do Office E3 ou um plano de serviço mais alto, que agora, você receberá um ponto de partida protegendo as informações por meio de proteção de informações do Azure quando podemos distribuir esses recursos.
  
## <a name="changes-beginning-july-1-2018"></a>Alterações começando 1 de julho de 2018

Iniciando 1 de julho de 2018, Microsoft habilitará o recurso de proteção em proteção de informações do Windows Azure para todos os locatários do Office 365, que têm um dos seguintes planos de assinatura:
  
- O Office 365 Message Encryption é oferecido como parte do Office 365 E3 e E5, Microsoft E3 e E5, A1 do Office 365, A3 e A5 e Office 365 G3 e G5. Não é necessário licenças adicionais para receber os novos recursos de proteção possibilitados pela proteção de informações do Windows Azure. 
    
- Você também pode adicionar Azure informações proteção plano 1 para os seguintes planos receber os novos recursos do Office 365 Message Encryption: Exchange Online plano 1, Exchange Online plano 2, F1 do Office 365, Essentials do Office 365 Business, Business Premium do Office 365, ou O Office 365 Enterprise E1.
    
- Cada usuário se beneficiando da criptografia de mensagem do Office 365 precisa ser licenciados para ser abordados pelo recurso.
    
- Para obter a lista completa, consulte as [descrições do serviço do Exchange Online](https://technet.microsoft.com/library/exchange-online-service-description.aspx) para Office 365 Message Encryption. 
    
Administradores de Inquilino podem verificar o status de proteção no portal do administrador do Office 365. 
  
![Captura de tela que mostra que o gerenciamento de direitos no Office 365 é ativado.](media/303453c8-e4a5-4875-b49f-e80c3eb7b91e.png)
  
## <a name="why-are-we-making-this-change"></a>Por que estamos fazendo essa alteração?

Criptografia de mensagem do Office 365 aproveita os recursos de proteção em proteção de informações do Windows Azure. No Centro de nossos investimentos amplos à proteção de informações no Microsoft 365 e os aperfeiçoamentos recentes para o Office 365 Message Encryption, podemos são tornando mais fácil para organizações ativar e usar nossos recursos de proteção, como criptografia Historicamente, tecnologias foram difíceis de configurar. Ativando os recursos de proteção em proteção de informações do Windows Azure, por padrão, você rapidamente pode começar a proteger dados confidenciais.
  
## <a name="does-this-impact-me"></a>Isso afeta mim?

Se sua organização do Office 365 adquiriu uma licença do Office 365 elegível, então seu locatário será afetado por essa alteração.
  
 **Importante!** Se você estiver usando o Active Directory Rights Management Services (AD RMS) no seu ambiente local, você deverá sair dessa alteração imediatamente ou migrar à proteção de informações do Azure antes que podemos distribuir essa alteração dentro de 30 dias. Para obter informações sobre como recusar, consulte "usar o AD RMS, como consentimento out?" mais adiante neste artigo. Se você preferir migrar, consulte [Migrando do AD RMS para proteção de informações do Azure.](https://docs.microsoft.com/azure/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms)
  
## <a name="can-i-use-azure-information-protection-with-active-directory-rights-management-services-ad-rms"></a>Pode usar o Windows Azure Information Protection com o Active Directory Rights Management Services (AD RMS)?

Não. Isso não é um cenário de implantação com suporte. Sem levar as etapas adicionais de recusar, alguns computadores podem iniciar automaticamente usando o serviço de gerenciamento de direitos do Windows Azure e também se conectar ao cluster do AD RMS. Esse cenário não é suportado e tem resultados não confiáveis, portanto, é importante que você recusar essa alteração dentro de 30 dias antes que podemos distribuir esses novos recursos. Para obter informações sobre como recusar, consulte "usar o AD RMS, como consentimento out?" mais adiante neste artigo. Se você preferir migrar, consulte [Migrando do AD RMS para proteção de informações do Azure.](https://docs.microsoft.com/azure/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms)
  
## <a name="how-do-i-know-if-im-using-ad-rms"></a>Como saber se estou usando o AD RMS?

Use estas instruções de [preparação do ambiente para o Azure Rights Management quando você também tem o Active Directory Rights Management Services (AD RMS)](https://docs.microsoft.com/azure/information-protection/deploy-use/prepare-environment-adrms) para verificar se você tiver implantado o AD RMS: 
  
1. Embora opcional, a maioria das implantações do AD RMS publicar o ponto de conexão de serviço (SCP) no Active Directory para que os computadores de domínio podem descobrir o cluster do AD RMS. 
  
Use o ADSI Edit para verificar se você tem um SCP publicado no Active Directory: CN = configuração [nome do servidor], CN = Serviços, CN = RightsManagementServices, CN = SCP
    
2. Se você não estiver usando um SCP, computadores com Windows que se conectam a um cluster AD RMS devem ser configurados para descoberta do serviço do lado do cliente e o redirecionamento de licenciamento por meio do registro do Windows: HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MSIPC\ServiceLocation ou HKEY _ LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\MSIPC\ServiceLocation 
  
Para obter mais informações sobre essas configurações do registro, consulte [Habilitando a descoberta de serviço de cliente usando o registro do Windows](https://docs.microsoft.com/azure/information-protection/rms-client/client-deployment-notes#enabling-client-side-service-discovery-by-using-the-windows-registry) e o [tráfego do servidor de licenciamento de redirecionamento](https://docs.microsoft.com/azure/information-protection/rms-client/client-deployment-notes#redirecting-licensing-server-traffic).
    
## <a name="i-use-ad-rms-how-do-i-opt-out"></a>Devo usar o AD RMS, como eu rejeitar?

Para rejeitar a alteração futura, conclua estas etapas:
  
1. Usando uma conta de trabalho ou da escola que tenha permissões de administrador global na sua organização do Office 365, iniciar uma sessão do Windows PowerShell e se conectar ao Exchange Online. Para obter instruções, consulte [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).
    
2. Execute o cmdlet Set-IRMConfiguration usando a seguinte sintaxe:
    
  ```
  Set-IRMConfiguration -AutomaticServiceUpdateEnabled $false 
  ```

## <a name="what-can-i-expect-after-this-change-has-been-made"></a>O que eu esperava depois que essa alteração foi feita?

Quando esta opção estiver ativada, desde que você ainda não tiver optado check-out, você pode começar a usar a nova versão do Office 365 Message Encryption, que foi anunciado no [Microsoft Ignite 2017](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Email-Encryption-and-Rights-Protection/ba-p/110801) e aproveita os recursos de criptografia e a proteção das informações do Windows Azure Proteção. 
  
![Captura de tela que mostra uma OME protegido mensagem no Outlook na web.](media/599ca9e7-c05a-429e-ae8d-359f1291a3d8.png)
  
Para obter mais informações sobre os novos aprimoramentos, consulte [Criptografia de mensagem do Office 365](ome.md).
  


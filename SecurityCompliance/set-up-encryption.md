---
title: Configure a criptografia no Office 365 Enterprise
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/2/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e86fc991-0161-4f01-9c1c-d25e87733d06
description: Com o Office 365, alguns recursos de criptografia são ativados por padrão; outros recursos podem ser configurados para atender a certos requisitos legais ou conformidade.
ms.openlocfilehash: 80deced80283ac36d82ac15cee9af6d390c4749a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523804"
---
# <a name="set-up-encryption-in-office-365-enterprise"></a>Configure a criptografia no Office 365 Enterprise

Criptografia pode proteger o conteúdo contra sendo lidos por usuários não autorizados. Porque a [criptografia no Office 365](encryption.md) pode ser feita usando vários métodos e tecnologias, há não um lugar único onde você pode ativar ou configure a criptografia. Este artigo fornece informações sobre diversas maneiras que você pode definir ou configurar a criptografia como parte de sua estratégia de proteção de informações. 
  
> [!TIP]
> Se você estiver procurando por mais detalhes técnicos sobre criptografia, consulte [os detalhes de referência técnica sobre criptografia no Office 365](technical-reference-details-about-encryption.md). 
  
Com o Office 365, várias capacidades de criptografia estão disponíveis por padrão. Recursos de criptografia adicionais podem ser configurados para atender a certos requisitos legais ou conformidade. A tabela a seguir descreve os diversos métodos de criptografia para diferentes cenários.
  
|**Cenário**|**Métodos de criptografia**|
|:-----|:-----|
|Arquivos são salvos em computadores com Windows  <br/> |Criptografia no nível do computador pode ser feita usando o BitLocker em dispositivos do Windows. Como um administrador da empresa ou profissional de TI, você pode configurar isso usando o Microsoft Deployment Toolkit (MDT). Consulte [Configurar o MDT para o BitLocker](https://go.microsoft.com/fwlink/?linkid=849282).<br/> |
|Arquivos são salvos em dispositivos móveis  <br/> |Alguns tipos de dispositivos móveis criptografar arquivos salvos por padrão para esses dispositivos. Com os [recursos de gerenciamento de dispositivos móveis internos para o Office 365](https://support.office.com/article/a1da44e5-7475-4992-be91-9ccec25905b0), você pode definir políticas para determinar se você deseja permitir dispositivos móveis acessar dados no Office 365. Por exemplo, você pode definir uma política que permite que somente os dispositivos que criptografar conteúdo para acessar dados do Office 365. Consulte [criar e implantar diretivas de segurança de dispositivo](https://support.office.com/article/d310f556-8bfb-497b-9bd7-fe3c36ea2fd6).<br/> Para controle adicional sobre como os dispositivos móveis interagir com o Office 365, você pode considerar a inclusão [Microsoft Intune](https://aka.ms/qzln04). Consulte [escolher entre MDM para o Office 365 e Microsoft Intune](https://support.office.com/article/c93d9ab9-efb2-4349-9b93-30c30562ee22).<br/> |
|Você precisa controle sobre as chaves de criptografia usado para criptografar os dados em centros de dados da Microsoft  <br/> | Como um administrador do Office 365, você pode controlar as chaves de criptografia da sua organização e configurar o Office 365 para usá-los para criptografar dados em repouso em centros de dados da Microsoft.  <br/> [Controlar seus dados no Office 365 usando a Chave do cliente](controlling-your-data-using-customer-key.md) <br/> [Chave de cliente para perguntas Frequentes do Office 365](service-encryption-with-customer-key-faq.md) <br/> |
|As pessoas estão se comunicando via email (Exchange Online)  <br/> | Como administrador do Exchange Online, você tem várias opções para configurar a criptografia de email. Elas incluem:<br/>  Usando [a criptografia de mensagem do Office 365 (OME)](set-up-new-message-encryption-capabilities.md) com o Azure Rights Management (RMS Azure) para permitir que as pessoas enviem mensagens criptografadas dentro ou fora da sua organização  <br/>  Usando [S/MIME para assinatura e criptografia](https://aka.ms/c6dozg) para criptografar e assinar digitalmente mensagens de email  <br/>  Usar o TLS para [Configurar conectores para o fluxo de mensagens seguras com outra organização](https://aka.ms/hs809p) <br/>  Consulte [criptografia de Email no Office 365](https://aka.ms/hic3f7).  <br/> |
|Arquivos que são acessados a partir de sites de equipe ou bibliotecas de documentos (OneDrive for Business ou SharePoint Online)  <br/> |Quando as pessoas estiver trabalhando com arquivos salvos ao OneDrive para negócios ou SharePoint Online, conexões TLS são usados. Isso é incorporado ao Office 365 automaticamente. Consulte [criptografia de dados no OneDrive for Business e o SharePoint Online](https://go.microsoft.com/fwlink/?linkid=526379).<br/> |
|Arquivos que são compartilhados em reuniões online e conversas de mensagens Instantâneas (Skype para Business Online)  <br/> |Quando as pessoas estiver trabalhando com arquivos usando o Skype para Business Online, o TLS é usado para a conexão. Isso é incorporado ao Office 365 automaticamente. Consulte [Security and Archiving (Skype para negócios on-line)](https://aka.ms/nuq4ws).<br/> |
   
## <a name="additional-information"></a>Additional information

Para saber mais sobre as soluções de proteção de arquivo que incluem as opções de criptografia, consulte [Soluções de proteção de arquivo no Office 365](https://www.microsoft.com/en-us/download/details.aspx?id=55523).
  


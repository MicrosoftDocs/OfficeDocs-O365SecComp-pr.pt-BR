---
title: Escolher entre MDM para o Office 365 e Microsoft Intune
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 10/3/2017
ms.audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: c93d9ab9-efb2-4349-9b93-30c30562ee22
description: Microsoft Intune e gerenciamento de dispositivos móveis internos para o Office 365 proporcionam a capacidade de gerenciar dispositivos móveis em sua organização. Mas há diferenças fundamentais, como descritas neste tópico.
ms.openlocfilehash: 553d401179f82b0f119f9e7d929b4af7d3df0c4a
ms.sourcegitcommit: 9034809b6f308bedc3b8ddcca8242586b5c30f94
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/15/2019
ms.locfileid: "28014733"
---
# <a name="choose-between-mdm-for-office-365-and-microsoft-intune"></a>Escolher entre MDM para o Office 365 e Microsoft Intune

Microsoft Intune e gerenciamento de dispositivos móveis internos para o Office 365 proporcionam a capacidade de gerenciar dispositivos móveis em sua organização. Mas há diferenças fundamentais, como descritas na tabela a seguir.
  
> [!NOTE]
> Você pode gerenciar usuários e seus dispositivos móveis usando Intune e o Office 365 no mesmo inquilino do Office 365. Configurando Intune e MDM permite que você decida qual solução é melhor para usuários específicos e seus dispositivos. Se você tem as duas opções disponíveis, você pode escolher se você gerencia dispositivos de um usuário com MDM para Office 365 ou a solução de Intune mais recursos avançados. 
  
||||
|:-----|:-----|:-----|
|**Área de recurso** <br/> |**MDM para Office 365** <br/> |**Microsoft Intune** <br/> |
|Cost  <br/> |Incluído com muitos assinaturas comerciais do Office 365.  <br/> |Requer uma assinatura paga para Microsoft Intune ou pode ser adquirido com pacote de mobilidade do Enterprise.  <br/> |
|Como você gerencia dispositivos  <br/> |Gerenciar dispositivos usando o [a segurança do Office 365 &amp; Centro de conformidade](https://protection.office.com) Office 365.  <br/> |Se você usar Intune por si só, você gerencia dispositivos usando o console de administração Intune.  <br/> Se você integre Intune System Center Configuration Manager 2012, use o console do Configuration Manager para gerenciar dispositivos local e na nuvem.  <br/> |
|Você pode gerenciar de dispositivos  <br/> |Gerenciamento baseado em nuvem para iOS, Android e Windows dispositivos  <br/> |Baseado em nuvem gerenciamento para iOS, Mac OS X, Android, Windows 8.1 (telefone e PC) ou posterior para incluir Windows 10. <br/> |
|Principais recursos  <br/> |Ajuda a garantir que documentos e emails corporativos do Office 365 podem ser acessados apenas em telefones e tablets que são gerenciados por sua empresa e que são compatíveis com suas diretivas de TI.  <br/> Definir e gerenciar políticas de segurança, como o pin de nível lock e jailbreak detecção do dispositivo, para ajudar a impedir que usuários não autorizados acessem email corporativo e dados em um dispositivo quando ele for perdido ou roubado.  <br/> Remova o Office 365 dados da empresa do dispositivo de um funcionário, deixando os seus dados pessoais no lugar.  <br/> Detalhes são incluídos nos [recursos de gerenciamento de dispositivos móveis internos para o Office 365](https://support.office.com/article/a1da44e5-7475-4992-be91-9ccec25905b0).  <br/> |MDM para recursos do Office 365, mais:  <br/> Ajuda os usuários acessarem o recurso corporativo com certificados, Wi-Fi, VPN e perfis de email.  <br/> Registrar e gerenciar conjuntos de dispositivos pertencentes corporativo, simplificando a implantação de política e app.  <br/> Implante seus aplicativos de linha de negócios internos e armazena os aplicativos para os usuários.  <br/> Permitir que os usuários acessem com mais segurança informações corporativas, usando o Office mobile e linha de negócios apps souberem, garantindo a segurança dos dados, ajudando a restringir ações copiar, colar recortado,, como e salvar como, apenas estes aplicativos gerenciados por Intune.  <br/> Habilite a navegação mais seguro da web usando o app Intune gerenciados navegador.  <br/> Gerenciar PCs da nuvem com nenhuma infra-estrutura necessária usando Intune ou conecte Intune até o Configuration Manager para gerenciar todos os seus dispositivos, incluindo PCs, Macs, Linux e UNIX servidores e dispositivos móveis de um console de gerenciamento único.  <br/> Uma assinatura Intune também permite que você defina as políticas do MAM (gerenciamento de aplicativos móveis) usando o portal do Azure, mesmo se os dispositivos de pessoas não estão inscritos no Intune. Consulte a [proteger os dados de aplicativo usando diretivas MAM](https://go.microsoft.com/fwlink/?LinkId=825439).<br/> |


## <a name="related-topics"></a>Tópicos relacionados
   
Saiba mais sobre o Microsoft Intune com o curso de treinamento em vídeo [Serviços de nuvem da Microsoft: administrar o Office 365 e Intune](https://support.office.com/article/c1224e20-3d49-4f40-99ee-fd0991880376.aspx), levado a você pelo aprendizado LinkedIn.
  


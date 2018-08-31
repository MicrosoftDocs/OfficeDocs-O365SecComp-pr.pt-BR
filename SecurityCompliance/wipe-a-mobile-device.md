---
title: Apagar um dispositivo móvel no Office 365
ms.author: dianef
author: dianef77
manager: scotv
ms.date: 6/11/2018
ms.audience: Admin
ms.topic: get-started-article
f1_keywords:
- O365M_WipeDevice
- O365E_WipeDevice
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 9d727c7d-8b47-4499-bf24-d046b449214c
description: Você pode usar o gerenciamento de dispositivo móvel interna para o Office 365 para realizar uma limpeza seletiva para remover apenas informações organizacionais, ou uma limpeza completa para excluir todas as informações de um dispositivo móvel e restaurá-lo para suas configurações de fábrica.
ms.openlocfilehash: d3eb28575924ca3bb4a647ae9af2f96b55116a53
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272496"
---
# <a name="wipe-a-mobile-device-in-office-365"></a>Apagar um dispositivo móvel no Office 365
  
Você pode usar o gerenciamento de dispositivo móvel interna para o Office 365 para realizar uma limpeza seletiva para remover apenas informações organizacionais, ou uma limpeza completa para excluir todas as informações de um dispositivo móvel e restaurá-lo para suas configurações de fábrica.
  
## <a name="what-to-know-before-you-begin"></a>O que saber antes de começar

- Dispositivos móveis podem armazenar informações organizacionais confidenciais e fornecer acesso aos recursos do Office 365 da sua organização. Para ajudar a proteger as informações da sua organização, você pode fazer uma limpeza completa ou uma limpeza seletiva:
    
  - **Apagamento completo**: exclui todos os dados no dispositivo móvel de um usuário, incluindo aplicativos instalados, fotos e informações pessoais. Quando a limpeza estiver concluída, o dispositivo é restaurado para suas configurações de fábrica. 
    
  - **Apagar seletiva**: remove apenas dados da organização e aplicativos deixará instalado, fotos e informações pessoais no dispositivo móvel de um usuário. 
    
- Quando um dispositivo é apagado (apagamento completo ou apagamento seletivo), o dispositivo é removido da lista de dispositivos gerenciados.
    
- Você pode configurar uma política de gerenciamento de dispositivo móvel que automaticamente apaga (apagamento completo) um dispositivo após o usuário tenta sem sucesso inserir a senha do dispositivo um número específico de vezes. Siga as etapas em [criar e implantar diretivas de segurança de dispositivo](create-device-security-policies.md).
    
- Se você deseja saber o que um usuário observarão quando você apagar seus dispositivos, consulte [qual é o impacto de usuário e o dispositivo?](wipe-a-mobile-device.md#BKMK_Impact).
    
## <a name="wipe-a-mobile-device"></a>Apagar um dispositivo móvel

1. Vá para o [ ![clique aqui para ir para o Centro de administração do Office 365.](media/e00ba917-c3fb-4173-b344-43eb5c7eeb15.png)](https://portal.office.com/adminportal/home).

2. Vá para [Ir para a segurança do Office 365 &amp; Centro de conformidade](https://support.office.com/article/7e696a40-b86b-4a20-afcc-559218b7b1b8) \> **prevenção de perda de dados** \> **gerenciamento de dispositivo**.
    
3. Selecione o dispositivo que você deseja limpar.
    
4. Selecione o tipo de apagamento remoto que você deseja fazer.
    
  - Para fazer uma limpeza seletiva e excluir apenas Office 365 informações da organização, no painel direito, selecione **Apagar seletiva**.
    
  - Para fazer uma limpeza completa e restaurar o dispositivo para suas configurações de fábrica, no painel direito, selecione **apagamento completo**.
    
![Selecione um dispositivo e, em seguida, escolha o tipo de apagamento fazer.](media/ac940abe-0c4a-404e-a842-a1ad2af13ce3.png)
  
5. Selecione **Sim** para confirmar. 
    
Até que a limpeza estiver concluída, o **status do dispositivo** será exibido como **RetirePending** ou **RetireIssued**.
  
### <a name="how-do-i-know-it-worked"></a>Como saber se que ele funcionou?

Não há mais, você verá o dispositivo móvel na lista de dispositivos gerenciados.
  
## <a name="why-would-you-want-to-wipe-a-device"></a>Por que você deseja limpar um dispositivo?

Há vários motivos para apagar dispositivos dispositivos:
  
- Dispositivos móveis, como smartphones e tablets estão se tornando mais completo sempre. Isso significa que é mais fácil para os usuários armazenar informações corporativas confidenciais (como ou comunicações confidenciais de identificação pessoal) e acessá-lo em trânsito. Se um desses dispositivos móveis é perdido ou roubado, apagar dispositivos o dispositivo imediatamente podem ajudar a impedir que as informações da sua organização terminando em mãos erradas.
    
- Quando um usuário sai da organização com um dispositivo pessoal que está inscrito no MDM para o Office 365, você pode ajudar a impedir que informações organizacionais indo com esse usuário fazendo uma limpeza seletiva.
    
- Se sua organização fornece dispositivos móveis aos usuários, você talvez seja necessário reatribuir os dispositivos do tempo. Fazer uma limpeza completa em um dispositivo antes de atribuí-la a um novo ajuda de usuário garante que qualquer informação confidencial do proprietário anterior é excluída.
    
## <a name="whats-the-user-and-device-impact"></a>O que é o usuário e o impacto de dispositivo?

A limpeza é enviada imediatamente para o dispositivo móvel. O dispositivo também será marcado como não compatível com em AAD.
  
A tabela a seguir descreve o conteúdo que foi removido para cada tipo de dispositivo, quando um dispositivo é apagado seletivamente.
  
|**Impacto de conteúdo**|**Windows Phone 8.1**|**iOS 7.1 ou posterior**|**Android 4 ou posterior**|
|:-----|:-----|:-----|:-----|
|Aplicativo de Portal da empresa\* é desinstalado.  <br/> |N/D  <br/> |✔  <br/> |N/D  <br/> |
|Dados de aplicativo Office 365 hospedados por aplicativos onde o controle de acesso é suportado pelo MDM para Office 365 são removida (Outlook atualmente e OneDrive for Business). Os aplicativos não serão removidos.  <br/> Outlook para Android não remove emails em cache.  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |
|Configurações de diretiva que foram aplicadas por MDM para o Office 365 para dispositivos não são impostas no dispositivo e os usuários podem alterar as configurações.  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |
|Perfis de email criados pelo MDM para o Office 365 são removidos e email em cache no dispositivo será excluído.  <br/> |N/D  <br/> |✔  <br/> |N/D  <br/> |
   
> [!NOTE]
> \*Aplicativo de Portal da empresa está disponível na App Store para iOS e o repositório de tocar para dispositivos com Android. 
  
## <a name="related-content"></a>Conteúdo relacionado

[Gerenciar dispositivos móveis no Office 365](set-up-mobile-device-management.md)
  


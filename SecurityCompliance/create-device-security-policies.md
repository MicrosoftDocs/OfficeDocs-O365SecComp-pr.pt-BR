---
title: Criar e implantar políticas de segurança de dispositivo
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/9/2018
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.NewDevicePolicy
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: d310f556-8bfb-497b-9bd7-fe3c36ea2fd6
description: 'Etapas para criar e implantar diretivas de segurança para o gerenciamento de dispositivos móveis no Office 365 pode ajudar a protegem informações da sua organização no Office 365 contra acesso não autorizado. '
ms.openlocfilehash: ab1fc1960a3e55eb3080dde7df0ec742c58b2cc7
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272066"
---
# <a name="create-and-deploy-device-security-policies"></a>Criar e implantar políticas de segurança de dispositivo

Você pode usar o gerenciamento de dispositivos móveis para o Office 365 para criar políticas de segurança que ajudam a proteger as informações da sua organização no Office 365 contra acesso não autorizado. Você pode aplicar políticas para qualquer dispositivo móvel em sua organização onde o usuário do dispositivo tem uma licença do Office 365 aplicável e tem inscritos o dispositivo em MDM para o Office 365.
  
## <a name="before-you-begin"></a>Antes de começar

- Saiba mais sobre os dispositivos, aplicativos de dispositivo móvel e configurações de segurança que suporta MDM para o Office 365. Consulte os [recursos de gerenciamento de dispositivos móveis para o Office 365](capabilities-of-mobile-device-management.md).
    
- Criar grupos de segurança que incluem usuários do Office 365 que você deseja implantar políticas e para usuários que você deseja excluir sejam bloqueados acesso ao Office 365. Recomendamos que, antes de implantar uma nova política à sua organização, você teste a política por implantá-lo para um pequeno número de usuários. Você pode criar e usar um grupo de segurança que inclui apenas sozinho ou um número usuários do Office 365 small que podem testar a diretiva para você. Para saber mais sobre grupos de segurança, consulte [criar, editar ou excluir um grupo de segurança](https://go.microsoft.com/fwlink/p/?LinkId=518555).
    
- **Importante:** Antes de criar uma política de dispositivo móvel, você deve ativar e configurar o MDM para Office 365. Consulte [Visão geral do gerenciamento de dispositivos móveis para o Office 365](overview-of-mdm.md).
    
- Para criar e implantar políticas de gerenciamento de dispositivos móveis no Office 365, você precisa ser um administrador global do Office 365. Consulte [Permissions in a segurança do Office 365 &amp; Centro de conformidade](https://support.office.com/article/d10608af-7934-490a-818e-e68f17d0e9c1).
    
- Antes de implantar políticas, permitem que sua organização Saiba os impactos potenciais da inscrição um dispositivo em MDM para Office 365. Dependendo de como configurar as políticas, dispositivos fora de conformidade podem ser impedidos de acessar o Office 365 e dados, incluindo aplicativos instalados, fotos e informações pessoais em um dispositivo registrado, podem ser excluídos.
    
> [!NOTE]
> Políticas e regras de acesso criadas no MDM para Office 365 substituirão políticas de caixa de correio de dispositivo móvel do Exchange ActiveSync e regras de acesso de dispositivo criadas no Centro de administração do Exchange. Depois que um dispositivo está inscrito no MDM para o Office 365, qualquer política de caixa de correio de dispositivo móvel do Exchange ActiveSync ou aplicada ao dispositivo da regra de acesso de dispositivo será ignorada. Para saber mais sobre o Exchange ActiveSync, consulte [Exchange ActiveSync no Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=524380). 
  
## <a name="step-1-create-a-security-policy-and-deploy-to-a-test-group"></a>Etapa 1: Criar uma política de segurança e implantar a um grupo de teste

Antes de começar, certifique-se de ter ativado e configurar o MDM para Office 365. Consulte [Visão geral do gerenciamento de dispositivos móveis para o Office 365](overview-of-mdm.md) para obter instruções. 
  
1. No Office 365, na segurança &amp; Centro de conformidade, vá para a **prevenção de perda de dados** \> **diretivas de segurança de dispositivo**.
    
    > [!NOTE]
    > As **diretivas de segurança do dispositivo** será exibida no menu apenas após ter ativado o gerenciamento de dispositivo móvel. 
  
2. Escolha **+ criar uma política**.
    
    ![Criar uma política de dispositivo MDN sob as diretivas de segurança de dispositivo](media/fbcdbecd-0016-42f1-81a9-9fbad610da90.png)
  
3. Especifique um **nome** e uma **Descrição** para a nova política e escolha **Avançar**.
    
    ![Configurar um nome para a diretiva de segurança de dispositivo](media/d382e845-4a7f-4f72-8a09-813ea4cbd0c4.png)
  
4. No **que requisitos você deseja ter em dispositivos?** página, especifique os requisitos que você deseja aplicar a dispositivos móveis em sua organização e escolha **Avançar**.
    
    ![A página de configurações na diretiva de segurança de dispositivo](media/186b3bd5-5e3d-4059-978f-94113111a8ca.png)
  
5. Sobre o **o que você deseja configurar?** página, especifique os requisitos adicionais que você deseja aplicar a dispositivos móveis em sua organização e escolha **Avançar**.
    
6. Sobre o **você deseja aplicar esta diretiva agora?** página, escolha **Sim**e, em seguida, escolha **+ Add**. 
    
    ![Adicione a política](media/89ab7cab-1b7a-4c78-9aa6-3db7d7667f8e.png)
  
7. Selecione os grupos que testará a política antes de implantá-lo à sua organização e, em seguida, escolha **Adicionar**.
    
8. Escolha **Próximo**.
    
9. Revise e confirme os detalhes da nova diretiva de dispositivo e, em seguida, escolha **criar essa diretiva**.
    
    ![Escolha criar essa diretiva para finsih criando uma política de dispositivo](media/e410bcf3-8a36-44ed-9fea-00e742db06fb.png)
  
10. Clique em **Fechar**.
    
Cada usuário que a política se aplica a terão a política enviada para seu dispositivo na próxima vez que entrarem no Office 365 usando seu dispositivo móvel. Se os usuários não tiveram uma diretiva aplicada aos seus dispositivos móveis antes, em seguida, após a implantação da diretiva, eles obterá uma notificação no dispositivo que inclui as [etapas para registrar e ativar o MDM para o Office 365](https://go.microsoft.com/fwlink/?LinkId=615272). Até que sejam concluídas inscrição, acesso a email, OneDrive e outros serviços será restritos. Após a conclusão de inscrição usando o app Intune Portal da empresa, eles serão capazes de usar os serviços e a diretiva será aplicada ao seu dispositivo.
  
## <a name="step-2-verify-your-policy-works"></a>Etapa 2: Verificar sua funciona a diretiva

Depois que você criou uma diretiva de segurança, você deve verificar se a política funciona conforme o esperado antes de implantá-lo à sua organização.
  
1. No Office 365, vá para **segurança &amp; Centro de conformidade** \> **prevenção de perda de dados** \> **gerenciamento de dispositivo**.
    
2. Na página **Gerenciamento de dispositivos móveis para o Office 365** , verifique o status de dispositivos de usuário que tenham a diretiva aplicada. Você pode filtrar ou classificar por **todos** para exibir todos os dispositivos ou **bloqueado** para exibir dispositivos bloqueados. 
    
    ![Exibição de dispositivos que são gerenciados por MDM](media/5c9fd069-b716-40d8-9b36-f9cfeae2139f.png)
  
3. Você também pode fazer uma limpeza completa ou seletiva no dispositivo. Para obter instruções, consulte [Apagar um dispositivo móvel no Office 365](wipe-a-mobile-device.md).
    
## <a name="step-3-deploy-a-policy-to-your-organization"></a>Etapa 3: Implantar uma política para a sua organização

Depois que você criou uma política de dispositivo móvel e verificado que ele funciona conforme o esperado, implantá-lo à sua organização.
  
1. No Office 365, vá para **segurança &amp; Centro de conformidade** \> **prevenção de perda de dados** \> **diretivas de segurança de dispositivo**.
    
2. Selecione a política que você deseja implantar e escolha **Editar política** no \< _nome da política_ \> painel.  
    
3. Selecione a guia **Implantação**. 
    
4. Na guia de **implantação** , escolha **Sim** acima **Selecionar um ou mais grupos de segurança que contêm as pessoas que você deseja aplicar a esta diretiva** e, em seguida, **Adicionar**.
    
  - No painel **Selecionar grupo** , você pode procurar um grupo ao qual adicionar, você pode filtrar por alias ou por nome para exibição. Você também pode adicionar um grupo existente na lista **grupos** . 
    
    Você pode adicionar vários grupos para aplicar a política.
    
    Escolha **Adicionar** na parte inferior do painel. 
    
5. Escolha **Salvar** na guia de **implantação** . 
    
    ![Implante a diretiva MDM à sua organização.](media/dc3e7fe5-201a-4e45-abe3-fc93e0b59028.png)
  
Cada usuário que a política se aplica a terão a política enviada para seu dispositivo na próxima vez que entrarem no Office 365 usando seu dispositivo móvel. Se os usuários não tiveram uma diretiva aplicada aos seus dispositivos móveis, eles vai [fazer uma notificação em seus dispositivos](https://go.microsoft.com/fwlink/?LinkId=615272) com etapas para inscrever e ativá-lo para MDM para o Office 365. Depois que eles concluir o registro, a política será aplicada ao seu dispositivo. 
  
## <a name="step-4-block-email-access-for-unsupported-devices"></a>Etapa 4: Bloquear email o acesso de dispositivos sem suporte

Para ajudar a proteger informações da sua organização, você deverá bloquear acesso de app para email do Office 365 para dispositivos móveis que não são suportados pelo MDM para o Office 365. Consulte os [recursos de gerenciamento de dispositivos móveis internos para o Office 365](capabilities-of-mobile-device-management.md) para obter uma lista de dispositivos que são suportados. Para fazer isso: 
  
1. Vá para segurança &amp; Centro de conformidade\> **prevenção de perda de dados** \> **diretivas de segurança de dispositivo**.
    
2. Selecione **Gerenciar definições de acesso do dispositivo de toda a organização**.
    
    ![Vá para o Centro de conformidade \> dispositivos e clique em vincular as gerenciar configurações de acesso de dispositivo.](media/b9f4da3c-dfa5-4913-8482-42a077cb4f56.png)
  
3. Para bloquear dispositivos sem suporte, escolha **Bloquear** em **se um dispositivo não é suportado pelo MDM para o Office 365, você deseja permitir ou bloquear a partir usando uma conta do Exchange para acessar email da sua organização** \> **Salvar**.
  
## <a name="step-5-choose-security-groups-to-be-excluded-from-conditional-access-checks"></a>Etapa 5: Escolher grupos de segurança a serem excluídos de verificações de acesso condicional

Se quiser excluir algumas pessoas de verificações de acesso condicional em seus dispositivos móveis e você criou um ou mais grupos de segurança para essas pessoas, adicione os grupos de segurança aqui. As pessoas nesses grupos não terão políticas aplicadas a seus dispositivos móveis compatíveis.
  
1. Vá para segurança &amp; Centro de conformidade\> **prevenção de perda de dados** \> **diretivas de segurança de dispositivo**.
    
2. Selecione **Gerenciar definições de acesso do dispositivo de toda a organização**.
    
    ![Vá para o Centro de conformidade \> dispositivos e clique em vincular as gerenciar configurações de acesso de dispositivo.](media/b9f4da3c-dfa5-4913-8482-42a077cb4f56.png)
  
3. Selecione **Adicionar** para adicionar o grupo de segurança que possui usuários que você gostaria de excluir sejam bloqueados acesso ao Office 365. Quando um usuário é adicionado a essa lista, ele poderá acessar o email do Office 365 ao usar um dispositivo sem suporte. 
    
4. Selecione o grupo de segurança que você deseja usar no painel **Selecione grupo** . 
    
5. Selecione o nome e, em seguida, **Adicionar** \> **Salvar**.
    
6. No painel de **configurações de acesso de dispositivo de toda a organização** , escolha **Salvar**.
  
## <a name="what-is-the-impact-of-security-policies-on-different-device-types"></a>Qual é o impacto das políticas de segurança em tipos diferentes de dispositivos?

Quando você aplicar uma política a dispositivos de usuário, o impacto em cada dispositivo varia um pouco entre tipos diferentes de dispositivos. Consulte a tabela a seguir para obter exemplos do impacto das políticas em dispositivos diferentes.
  


|**Política de segurança**|**Windows Phone 8.1 +**|**Android 4 ou posterior**|**Samsung Knox**|**IOS 6 +**|**Anotações**|
|:-----|:-----|:-----|:-----|:-----|:-----|
|Exige backup criptografado  <br/> |✖  <br/> |✖  <br/> |✔  <br/> |✔  <br/> |Requer backup criptografado para IOS.  <br/> |
|Bloquear cópia de segurança na nuvem  <br/> |✖  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |Bloquear backup no Google no Android (esmaecido), backup na nuvem no iOS.  <br/> |
|Bloquear sincronização de documento  <br/> |✖  <br/> |✖  <br/> |✖  <br/> |✔  <br/> |iOS: Bloquear documentos na nuvem.  <br/> |
|Bloquear sincronização de fotos  <br/> |✖  <br/> |✖  <br/> |✖  <br/> |✔  <br/> |iOS (nativo): Bloquear fluxo de foto.  <br/> |
|Bloquear captura de tela  <br/> |✔  <br/> |X  <br/> |✔  <br/> |✔  <br/> |Bloqueado quando tentado.  <br/> |
|Bloquear videoconferência  <br/> |✖  <br/> |✖  <br/> |✖  <br/> |✔  <br/> |FaceTime bloqueado no iOS, não no Skype ou outros.  <br/> |
|Bloquear o envio de dados de diagnóstico  <br/> |✖  <br/> |X  <br/> |✔  <br/> |✔  <br/> |Bloquear o envio de relatório de falha do Google no Android.  <br/> |
|Bloquear o acesso à loja de aplicativos  <br/> |✔  <br/> |X  <br/> |✔  <br/> |✔  <br/> |Ícone de armazenamento de aplicativo ausente na página inicial do Android, desabilitado no Windows, ausente no iOS.  <br/> |
|Exigir senha para a loja de aplicativos  <br/> |✖  <br/> |✖  <br/> |✖  <br/> |✔  <br/> |iOS: Senha necessária para compras do iTunes.  <br/> |
|Bloquear a conexão ao armazenamento removível  <br/> |✔  <br/> |X  <br/> |✔  <br/> |NA  <br/> |Android: O cartão SD ficará esmaecido nas configurações, Windows notifica o usuário, aplicativos instalados que não estão disponíveis  <br/> |
|Bloquear conexão Bluetooth  <br/> |✔  <br/> |\*\*\*  <br/> |\*\*\*  <br/> |✖  <br/> |\*\*\*Não é possível desabilitamos BlueTooth como uma configuração no Android. Em vez disso, podemos desabilitar todas as transações que exigem BlueTooth: distribuição de áudio avançado, controle remoto de áudio/vídeo, dispositivos viva-voz, headset, acesso de catálogo telefônico e porta Serial. Uma mensagem de proposta pequeno aparece na parte inferior da página quando qualquer uma dessas é usada.  <br/> |
   
## <a name="what-happens-when-you-delete-a-policy-or-remove-a-user-from-the-policy"></a>O que acontece quando você exclui uma política ou remove um usuário da política?

Quando você excluir uma política ou remove um usuário de um grupo ao qual a política foi implantada, as configurações de diretiva, perfil de email do Office 365 e emails em cache podem ser removidos do dispositivo do usuário. Consulte a tabela a seguir para ver o que foi removido para os tipos diferentes de dispositivos:
  
|**O que é removido**|**Windows Phone 8.1 +**|**iOS 6 +**|**Android 4 + (incluindo Samsung Knox)**|
|:-----|:-----|:-----|:-----|
|Perfis de email gerenciadas\*  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|Configurações de política  <br/> |✔  <br/>           Exceto para **Bloquear o envio de dados de diagnóstico do dispositivo.** <br/> |✔  <br/> |✖  <br/> |
   
> [!NOTE]
> \*Se a política foi implantada com a opção de **perfil de Email é gerenciado** selecionado, faça o perfil de email gerenciadas e cache emails em que o perfil será excluído do dispositivo do usuário. 
  
Cada usuário que a diretiva removida aplicada ao terão a política removida do seu dispositivo na próxima vez em que seus dispositivos móveis verifica com MDM para o Office 365. Se você implantar uma nova política que se aplica a dispositivos desses usuários, eles serão solicitados a registrar-se novamente no MDM para o Office 365.
  
Você também pode [Apagar um dispositivo](wipe-a-mobile-device.md), tanto completamente ou seletivamente revelar informações organizacionais do dispositivo.
  
## <a name="related-topics"></a>Tópicos relacionados

[Visão geral do Gerenciamento de Dispositivos Móveis para o Office 365](overview-of-mdm.md)
  
[Recursos do Gerenciamento de Dispositivos Móveis para o Office 365](capabilities-of-mobile-device-management.md)
  


---
title: Perguntas frequentes sobre o gerenciamento de dispositivos móveis para o Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 12/30/2016
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 3871f99c-c9db-4a23-86f9-902c1b02f58d
description: Este artigo contém perguntas frequentes sobre o Mobile Device Management (MDM) para o Office 365, um recurso que ajuda você a gerenciar e proteger dispositivos móveis no Office 365.
ms.openlocfilehash: 6c4a5b3603d392b3d83769cd0f17450ce70565be
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272266"
---
# <a name="frequently-asked-questions-about-mobile-device-management-for-office-365"></a>Perguntas frequentes sobre o gerenciamento de dispositivos móveis para o Office 365

Este artigo contém perguntas frequentes sobre o Mobile Device Management (MDM) para o Office 365, um recurso que ajuda você a gerenciar e proteger dispositivos móveis no Office 365.
  
## <a name="faqs"></a>Perguntas frequentes

- [Como posso obter MDM para o Office 365? Eu não vejo-lo no Centro de administração do Office 365](#how-can-i-get-mdm-for-office-365-i-dont-see-it-in-the-office-365-admin-center)
    
- [Como posso começar com o gerenciamento de dispositivo no MDM](#how-can-i-get-started-with-device-management-in-mdm)
    
- [Estou tentando configurar MDM mas parece travado. A integridade do serviço do Office 365 tenha sido mostrando "provisionamento" por algum tempo. O que pode fazer?](#im-trying-to-set-up-mdm-but-it-seems-stuck-the-office-365-service-health-has-been-showing-provisioning-for-a-while-what-can-i-do)
    
- [O que posso fazer se ocorrer falha de registro do dispositivo?](#what-can-i-do-if-device-enrollment-fails)
    
- [O que é a diferença entre Intune e MDM para o Office 365?](#whats-the-difference-between-intune-and-mdm-for-office-365)
    
- [Como funcionam as diretivas para MDM? Como configuro-los? Desabilitá-los?](#how-do-policies-work-for-mdm-how-do-i-set-them-up-disable-them)
    
- [Posso alternar de gerenciamento de dispositivo do Exchange ActiveSync para MDM para o Office 365?](#can-i-switch-from-exchange-activesync-device-management-to-mdm-for-office-365)
    
- [Eu configuro MDM, mas agora eu quiser removê-lo. Quais são as etapas?](#i-set-up-mdm-but-now-i-want-to-remove-it-what-are-the-steps)
    
- [Precisa de mais ajuda](#still-need-help)
    
## <a name="how-can-i-get-mdm-for-office-365-i-dont-see-it-in-the-office-365-admin-center"></a>Como posso obter MDM para o Office 365? Eu não vejo-lo no Centro de administração do Office 365

Concluímos a aplicação desse recurso para os clientes do Office 365. Procure a guia de **Gerenciamento de dispositivo** no [Ir para a segurança do Office 365 &amp; Centro de conformidade](https://support.office.com/article/7e696a40-b86b-4a20-afcc-559218b7b1b8). Se você não estiver visível, informe-nos. Consulte [ainda precisa de ajuda?](#still-need-help), e nós vai ajudá-lo a começar. 
  
## <a name="how-can-i-get-started-with-device-management-in-mdm"></a>Como posso começar com o gerenciamento de dispositivo no MDM

Há quatro etapas getting Started with MDM para o Office 365 (Saiba detalhes em [Set up Mobile Device Management (MDM) no Office 365](set-up-mobile-device-management.md)):
  
1. **Ativar MDM.** Vá até o [Ir para a segurança do Office 365 &amp; Centro de conformidade](https://support.office.com/article/7e696a40-b86b-4a20-afcc-559218b7b1b8) e selecione **gerenciamento de dispositivos**. Clique em **Vamos começar** disparar o processo de ativação. 
    
2. **Configuração completa para MDM**. Isso pode exigir APNs configuração de certificado e atualizações nos registros DNS do seu domínio. 
    
3. **Criar políticas**. Criar políticas de gerenciamento de dispositivo e aplicá-las a grupos de usuários que serão [configurados em grupos de segurança](create-device-security-policies.md). Recomendamos que você inicie Implantando as políticas para um pequeno grupo de teste. Na segurança &amp; Centro de conformidade, selecione **diretivas de segurança de dispositivo**.
    
4. **Usuários inscrever dispositivos.** Os usuários que tiveram uma diretiva aplicada a eles são solicitados a [registrar seus dispositivos](enroll-your-mobile-device.md) quando tentarem acessar dados do Office 365 (usando seu cliente de e-mail, por exemplo). 
    
## <a name="im-trying-to-set-up-mdm-but-it-seems-stuck-the-office-365-service-health-has-been-showing-provisioning-for-a-while-what-can-i-do"></a>Estou tentando configurar MDM mas parece travado. A integridade do serviço do Office 365 tenha sido mostrando "provisionamento" por algum tempo. O que pode fazer?

Pode levar algum tempo para obter o serviço pronto para você. Quando o provisionamento estiver concluído, você verá o gerenciamento de dispositivos móveis para o Office 365. Se você ter esperado 24 horas e o status ainda é **provisionamento**, consulte [ainda precisa de ajuda?](#still-need-help) e vamos ajudá descobrir qual é o problema. 
  
## <a name="what-can-i-do-if-device-enrollment-fails"></a>O que posso fazer se ocorrer falha de registro do dispositivo?

Se você estiver tendo problemas para inserir um dispositivo inscrito, primeiro tente verificar o seguinte:
  
- Certifique-se de que o dispositivo não está inscrito já com outro provedor de gerenciamento de dispositivo móvel, como Intune.
    
- Certifique-se de que o dispositivo está definido como a data e hora correta.
    
- Alternar para um Wi-Fi diferente ou a rede celular no dispositivo.
    
- Para dispositivos Android ou iOS, desinstale e reinstale o aplicativo de Portal da empresa Intune no dispositivo.
    
Se a inscrição ainda não está funcionando, [tente as seguintes etapas de solução de problemas adicionais](troubleshoot-mdm.md).
  
## <a name="whats-the-difference-between-intune-and-mdm-for-office-365"></a>O que é a diferença entre Intune e MDM para o Office 365?

Ambos os MDM para Office 365 e Intune fornecem soluções baseadas em nuvem para o gerenciamento de dispositivos em sua organização. Use este [lado a lado comparação](choose-between-mdm-and-intune.md) de dois serviços para ajudá-lo a decidir se usar o Intune ou MDM para o Office 365 é o melhor ajuste para você. 
  
## <a name="how-do-policies-work-for-mdm-how-do-i-set-them-up-disable-them"></a>Como funcionam as diretivas para MDM? Como configuro-los? Desabilitá-los?

Após concluir a instalação inicial para MDM para o Office 365, você [criar políticas e aplicá-las a grupos de usuários](create-device-security-policies.md) no [Ir para a segurança do Office 365 &amp; Centro de conformidade](https://support.office.com/article/7e696a40-b86b-4a20-afcc-559218b7b1b8). Para os usuários que as diretivas serão aplicadas, as políticas de exigirem que os usuários que se inscrevam seus dispositivos em MDM para Office 365, antes que o dispositivo pode ser usado para acessar dados do Office 365. As políticas que você configurou determinam configurações para dispositivos móveis, por exemplo, frequência de senhas devem ser redefinidas ou se a criptografia de dados é necessária. 
  
Fornecemos instruções passo a passo para [criar e implantar diretivas de segurança de dispositivo](create-device-security-policies.md). Crie as diretivas na segurança &amp; Centro de conformidade e você pode desabilitar uma ou mais políticas, retornando à segurança &amp; Centro de conformidade e editando a política para remover o grupo aplicado. Ou você pode optar por não remover a diretiva todo.
  
Se você deseja excluir um grupo específico de usuários sejam afetados pelas políticas, você pode adicionar um grupo ao grupo de exclusão. Na segurança &amp; Centro de conformidade, na guia **dispositivos** , selecione **Gerenciar definições de acesso de dispositivo**e, em seguida, adicione o grupo para o **existem quaisquer grupos de segurança que você deseja excluir do controle de acesso?** seção. 
  
## <a name="can-i-switch-from-exchange-activesync-device-management-to-mdm-for-office-365"></a>Posso alternar de gerenciamento de dispositivo do Exchange ActiveSync para MDM para o Office 365?

Se você já estiver usando [políticas do Exchange ActiveSync](https://go.microsoft.com/fwlink/?LinkId=615145) para gerenciar os dispositivos móveis, você pode começar a usar o MDM para o Office 365 seguindo as etapas para [definir o backup Mobile Device Management (MDM) no Office 365](set-up-mobile-device-management.md).
  
Quando você aplica as políticas que você criar no MDM para o Office 365 para grupos de usuários, essas políticas substituem políticas de caixa de correio de dispositivo móvel do Exchange ActiveSync e regras de acesso de dispositivo que você criou anteriormente no Centro de administração do Exchange para os usuários. 
  
Depois que um dispositivo está inscrito no MDM para o Office 365, qualquer política de caixa de correio de dispositivo móvel do Exchange ActiveSync ou aplicada ao dispositivo da regra de acesso de dispositivo será ignorada.
  
## <a name="i-set-up-mdm-but-now-i-want-to-remove-it-what-are-the-steps"></a>Eu configuro MDM, mas agora eu quiser removê-lo. Quais são as etapas?

Infelizmente, você não pode simplesmente "desprovisionar" MDM para o Office 365 depois de configurá-lo. Mas você pode removê-lo para grupos de usuários, removendo os grupos de segurança do usuário através da política de dispositivo que você criou. Ou desabilitá-lo para que todos, removendo as políticas de dispositivo para que eles não estão no local e não são impostos. Veja [como desativar o gerenciamento de dispositivos móveis no Office 365](turn-off-mdm.md).
  
## <a name="still-need-help"></a>Precisa de mais ajuda?

[![Obtenha ajuda nos fóruns da comunidade do Office 365](media/12a746cc-184b-4288-908c-f718ce9c4ba5.png)](https://go.microsoft.com/fwlink/p/?LinkId=518605)
  
[![Administradores: Entre e crie uma solicitação de serviço](media/10862798-181d-47a5-ae4f-3f8d5a2874d4.png)]( https://go.microsoft.com/fwlink/p/?LinkId=519124)
  
[![Administradores: Chame o suporte técnico](media/9f262e67-e8c9-4fc0-85c2-b3f4cfbc064e.png)](https://go.microsoft.com/fwlink/p/?LinkID=518322)
  

  


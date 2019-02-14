---
title: Habilitar o suplemento de Mensagem de Relatório
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/18/2019
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 4250c4bc-6102-420b-9e0a-a95064837676
ms.collection:
- M365-security-compliance
description: Aprenda a habilitar o suplemento de mensagem de relatório para o Outlook e Outlook na web, para usuários individuais ou em toda sua organização.
ms.openlocfilehash: 8c061d14d11aa868567487186c5dcca534b86215
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995152"
---
# <a name="enable-the-report-message-add-in"></a>Habilitar o suplemento de Mensagem de Relatório

## <a name="overview"></a>Visão geral

O suplemento de mensagem de relatório para o Outlook e Outlook na web permite que as pessoas facilmente relatado email classificados incorretamente, se seguros ou mal-intencionada, Microsoft e suas afiliadas para análise. A Microsoft usa essas envios para melhorar a eficácia das tecnologias de proteção de email. Além disso, se sua organização estiver usando [A proteção de ameaça avançadas do Office 365](office-365-atp.md) ou [Office 365 Threat Intelligence](office-365-ti.md), o suplemento de mensagem de relatório fornece equipe de segurança da sua organização com informações úteis, que eles podem usar para analisar e atualizar diretivas de segurança. 

Por exemplo, suponha que as pessoas são relatórios muitas mensagens como phishing. Este mostra informações no [Painel de segurança](security-dashboard.md) e outros relatórios. Equipe de segurança da sua organização pode usar essas informações como uma indicação de que as políticas de AntiPhishing talvez precisem ser atualizados. Ou, se as pessoas estão relatando muita mensagens que foram sinalizados como lixo eletrônico, como não sendo lixo eletrônico usando o suplemento de mensagem de relatório, talvez seja necessário ajustar o [políticas antispam](configure-the-anti-spam-policies.md)equipe de segurança da sua organização. 

O suplemento de mensagem de relatório funciona com sua assinatura do Office 365 e produtos a seguir:
 - Outlook na Web
 - Outlook 2013 SP1
 - Outlook 2016
 - Outlook 2016 para Mac
 - Outlook incluído com o Office 365 ProPlus

> [!NOTE]
> O suplemento de mensagem de relatório para o Outlook e Outlook na web não é exatamente a mesma coisa que o [Filtro de Email de lixo eletrônico do Outlook](https://support.office.com/article/Overview-of-the-Junk-Email-Filter-5ae3ea8e-cf41-4fa0-b02a-3b96e21de089), embora ambos podem ser usados para marcar um email como lixo eletrônico, não lixo ou uma tentativa de phishing. O suplemento de mensagem de relatório para o Outlook e Outlook na web notifica Microsoft sobre email classificados incorretamente, enquanto o filtro de lixo eletrônico do Outlook é usado para organizar as mensagens de email na caixa de correio do usuário. 
  
Se você for um usuário individual, você pode [Habilitar o suplemento de mensagem de relatório por conta própria](#get-the-report-message-add-in-for-yourself). 
  
Se você é um administrador global do Office 365 ou um administrador do Exchange Online e Exchange está configurado para usar a autenticação OAuth, você pode [Habilitar o suplemento de mensagem de relatório para sua organização](#get-and-enable-the-report-message-add-in-for-your-organization). O suplemento do relatório de mensagem agora está disponível por meio da [Implantação centralizados](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins).
    
## <a name="get-the-report-message-add-in-for-yourself"></a>Obtenha a mensagem de relatório suplemento para si mesmo

1. No [Microsoft AppSource](https://appsource.microsoft.com/marketplace/apps), procure o [suplemento de mensagem de relatório](https://appsource.microsoft.com/product/office/wa104381180).
    
2. Escolha **GET IT agora**.<br/>![Relatar mensagem - obtê-lo agora](media/ReportMessageGETITNOW.png)<br/> 
    
3. Analise os termos da política de uso e de privacidade. Em seguida, clique em **continuar**. 
    
4. Entrar no Office 365 usando o seu trabalho ou conta escola (para uso de negócios) ou sua conta da Microsoft (para uso pessoal).
    
Depois que o suplemento está instalado e habilitado, você verá os ícones a seguir: 

- No Outlook, o ícone tem esta aparência: <br/> ![Relatar o ícone do suplemento de mensagem do Outlook](media/OutlookReportMessageIcon.png)<br/>
- No Outlook Web App (ou Outlook na web), o ícone tem esta aparência:<br/>![Outlook no ícone de mensagem de relatório na web](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

> [!TIP]
> Como o próximo passo, Aprenda como [usar o suplemento de mensagem de relatório](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).
  
## <a name="get-and-enable-the-report-message-add-in-for-your-organization"></a>Obter e habilitar o suplemento de mensagem de relatório para sua organização

> [!IMPORTANT]
> Você deve ser um administrador global do Office 365 ou um administrador do Exchange Online para completar esta tarefa. Além disso, o Exchange deve ser configurado para usar a autenticação OAuth para saber mais, consulte [requisitos do Exchange (centralizados implantação dos suplementos)](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins&view=o365-worldwide#exchange-requirements). 

1. Vá até a [página de suplementos do serviços &](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) no Centro de administração do Microsoft 365.<br/>![Página de serviços e suplementos no novo Microsoft 365 Admin Center](media/ServicesAddInsPageNewM365AdminCenter.png)<br/> 
    
2. Escolha **+ implantar o suplemento**.<br/>![Escolha implantar o suplemento](media/ServicesAddIns-ChooseDeployAddIn.png)<br/> 
    
3. Na tela do **Novo suplemento** , revise as informações e escolha **Avançar**.<br/>![Detalhes do novo suplemento](media/NewAddInScreen1.png)<br/>
    
4. Selecione **eu quiser adicionar um suplemento da Office Store**e escolha **Avançar**.<br/>![Eu quiser adicionar um novo suplemento](media/NewAddInScreen2.png)<br/> 
    
5. Mensagem de **Relatório**e na lista de resultados, ao lado do **Suplemento de mensagem do relatório**de pesquisa, escolha **Adicionar**.<br/>![Procure a mensagem de relatório e escolha Adicionar](media/NewAddInScreen3.png)<br/>
    
6. Na tela de **Mensagem de relatório** , revise as informações e escolha **Avançar**.<br/>![Detalhes da mensagem de relatório](media/ReportMessageAdd-InNewScreen4.png)<br/>

7. Especifique as configurações de usuário padrão para o Outlook e escolha **Avançar**.<br/>![Relatar as configurações padrão de mensagem do Outlook](media/ReportMessageOptionsScreen5.png)<br/>

8. Especificar quem obtém o suplemento de mensagem de relatório e escolha **Salvar**. <br/>![Quem obtém a mensagem de relatório suplemento](media/ReportMessageOptionsScreen6.png)<br/>

> [!TIP]
> Recomendamos a [configuração de uma regra para obter uma cópia das mensagens de email relatado pelos usuários](#set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users).

Dependendo do item selecionado ao configurar o suplemento (etapas 7-8 acima), as pessoas na sua organização terão o [suplemento de mensagem de relatório](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) disponíveis. Pessoas da sua organização verá os ícones a seguir: 

- No Outlook, o ícone tem esta aparência: <br/> ![Suplemento de mensagem ícone de relatório para o Outlook](media/OutlookReportMessageIcon.png)<br/>
- No Outlook Web App (ou Outlook na web), o ícone tem esta aparência:<br/>![Outlook no ícone do suplemento de mensagem de relatório na Web](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

> [!TIP]
> Quando você notifica os usuários sobre o suplemento de mensagem de relatório, inclua um link para [usar o suplemento de mensagem de relatório](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).

## <a name="set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users"></a>Configurar uma regra para obter uma cópia das mensagens de email relatado pelos usuários

> [!IMPORTANT]
> Você deve ser um administrador do Exchange Online para executar essa tarefa.
  
Você pode configurar uma regra para obter uma cópia das mensagens de email relatado pelos usuários em sua organização. Isso é feito depois que você baixou e habilitou o suplemento de mensagem de relatório para sua organização.
  
1. No Centro de administração do Exchange, escolha **fluxo de emails** \> **regras**. 
    
2. Escolha **+** \> **criar uma nova regra**. 
    
3. Na caixa **nome** , digite um nome, como envios.
    
4. Na lista **Aplicar esta regra se** , escolha **o endereço do destinatário inclui...**. 
    
5. Na tela **Especificar palavras ou expressões** , adicione `junk@office365.microsoft.com` e `phish@office365.microsoft.com`e escolha **Okey**.<br/>![Especificar os endereços de email de lixo eletrônico e phishing para a regra](media/018c1833-f336-4333-a45c-f2e8b75cd698.png)<br/>
  
6. Na lista **faça o seguinte …** , escolha **Cco da mensagem para...**. 
    
7. Adicione um administrador global, administrador de segurança e/ou leitor de segurança que deve receber uma cópia de cada mensagem de email que pessoas reportam à Microsoft e escolha **Okey**.<br/>![Adicionar um administrador global ou de segurança para receber uma cópia de cada mensagem relatada](media/a91ab9d1-66f2-4a2e-9dc1-f9f81a2298ad.png)<br/>
  
8. Selecione **Auditar esta regra com nível de severidade**e escolha **Médio**. 
    
9. Em **Escolher um modo para essa regra**, escolha **Enforce**.<br/>![Configurar uma regra para obter uma cópia de cada mensagem relatada](media/f1cd95ce-e40d-4a8a-8f48-893469eba691.png)<br/>
  
10. Escolha **Salvar**. 
    
Com essa regra in-loco, sempre que alguém em sua organização relata uma mensagem de email usando o suplemento do relatório de mensagem, seu administrador global, administrador de segurança e/ou leitor de segurança receberá uma cópia da mensagem. Essas informações podem permitem definir ou ajustar políticas, como políticas de [Vínculos do Office 365 ATP seguros](atp-safe-links.md) ou suas configurações [antispam](anti-spam-protection.md) . 

## <a name="learn-how-to-use-the-report-message-add-in"></a>Saiba como usar o suplemento de mensagem de relatório

Consulte [usar o suplemento de mensagem de relatório](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).

## <a name="review-or-edit-settings-for-the-report-message-add-in"></a>Analisar ou editar as configurações para o suplemento de mensagem de relatório

Você pode examinar e editar as configurações padrão para o suplemento de mensagem de relatório na [página de suplementos do & de serviços](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns). 

> [!IMPORTANT]
> Você deve ser um administrador global do Office 365 ou um administrador do Exchange Online para completar esta tarefa.
    
1. Vá até a [página de suplementos do serviços &](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) no Centro de administração do Microsoft 365.<br/>![Página de serviços e suplementos no novo Microsoft 365 Admin Center](media/ServicesAddInsPageNewM365AdminCenter.png)<br/>

2. Localize e selecione o suplemento de mensagem de relatório.<br/>![Localize e selecione o suplemento de mensagem de relatório](media/FindReportMessageAddIn.png)<br/> 
    
3. Na tela de mensagem de relatório, revise e editar configurações, conforme apropriado para sua organização.<br/>![Configurações para o suplemento de mensagem de relatório](media/EditReportMessageAddIn.png)<br/> 
  
## <a name="related-topics"></a>Tópicos relacionados

[Usar o suplemento de mensagem de relatório](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)
  
[Exibir relatórios de segurança de email na segurança &amp; Centro de conformidade](view-email-security-reports.md)

[Exibir relatórios de proteção de ameaça avançadas do Office 365](view-reports-for-atp.md)

[Use o Explorer na segurança &amp; Centro de conformidade](use-explorer-in-security-and-compliance.md)
  


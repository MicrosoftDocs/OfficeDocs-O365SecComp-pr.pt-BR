---
title: Habilitar o suplemento de Mensagem de relatório
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 11/19/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 4250c4bc-6102-420b-9e0a-a95064837676
description: Aprenda a habilitar o suplemento de mensagem de relatório para o Outlook e Outlook na web, para usuários individuais ou em toda sua organização.
ms.openlocfilehash: a62e3e6250d2eccd2109a71f994713e2dd1b262e
ms.sourcegitcommit: 6669b7aae26965145e85d9613d3091bf389f000b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/19/2018
ms.locfileid: "26618917"
---
# <a name="enable-the-report-message-add-in"></a>Habilitar o suplemento de Mensagem de relatório

## <a name="overview"></a>Visão geral

O suplemento de mensagem de relatório para o Outlook e Outlook na Web permite que as pessoas facilmente relatado email classificados incorretamente, se seguros ou mal-intencionada, Microsoft e suas afiliadas para análise. A Microsoft usa essas envios para melhorar a eficácia das tecnologias de proteção de email. Além disso, se sua organização estiver usando [A proteção de ameaça avançadas do Office 365](office-365-atp.md) ou [Office 365 Threat Intelligence](office-365-ti.md), o suplemento de mensagem de relatório fornece equipe de segurança da sua organização com informações úteis, que eles podem usar para analisar e atualizar diretivas de segurança. 

Por exemplo, suponha que as pessoas são relatórios muitas mensagens como phishing. Este mostra informações no [Painel de segurança](security-dashboard.md) e outros relatórios. Equipe de segurança da sua organização pode usar essas informações como uma indicação de que as políticas de AntiPhishing talvez precisem ser atualizados. Ou, se as pessoas estão relatando muita mensagens que foram sinalizados como lixo eletrônico, como não sendo lixo eletrônico usando o suplemento de mensagem de relatório, talvez seja necessário ajustar o [políticas antispam](configure-the-anti-spam-policies.md)equipe de segurança da sua organização. 

O suplemento de mensagem de relatório funciona com sua assinatura do Office 365 e produtos a seguir:
 - Outlook na Web
 - Outlook 2013 SP1
 - Outlook 2016
 - Outlook 2016 para Mac
 - Outlook incluído com o Office 365 ProPlus
  
Se você for um usuário individual, você pode [Habilitar o suplemento de mensagem de relatório por conta própria](#get-the-report-message-add-in-for-yourself). 
  
Se você é um administrador global do Office 365 ou um administrador do Exchange Online e Exchange está configurado para usar a autenticação OAuth, você pode [Habilitar o suplemento de mensagem de relatório para sua organização](#get-and-enable-the-report-message-add-in-for-your-organization). O suplemento do relatório de mensagem agora está disponível por meio da [Implantação centralizados](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins).
    
## <a name="get-the-report-message-add-in-for-yourself"></a>Obtenha a mensagem de relatório suplemento para si mesmo

1. No [Microsoft AppSource](https://appsource.microsoft.com/marketplace/apps), procure o [suplemento de mensagem de relatório](https://appsource.microsoft.com/product/office/wa104381180).
    
2. Escolha **GET IT agora**.<br/>![Relatar mensagem - obtê-lo agora](media/ReportMessageGETITNOW.png)<br/> 
    
3. Analise os termos da política de uso e de privacidade. Em seguida, clique em **continuar**. 
    
4. Entrar no seu email do Office 365 usando seu trabalho ou a conta de escola (para uso de negócios) ou a sua conta da Microsoft (para uso pessoal).
    
Depois que o suplemento está instalado e habilitado, você verá os ícones a seguir: 

- No Outlook no ícone tem esta aparência: <br/> ![Suplemento de mensagem ícone de relatório para o Outlook](media/OutlookReportMessageIcon.png)<br/>
- No Outlook Web App no ícone tem esta aparência:<br/>![Outlook no ícone do suplemento de mensagem de relatório na Web](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

Como o próximo passo, Aprenda como [usar o suplemento de mensagem de relatório](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).
  
## <a name="get-and-enable-the-report-message-add-in-for-your-organization"></a>Obter e habilitar o suplemento de mensagem de relatório para sua organização

> [!IMPORTANT]
> Você deve ser um administrador global do Office 365 ou um administrador do Exchange Online para completar esta tarefa. Além disso, o Exchange deve ser configurado para usar a autenticação OAuth para saber mais, consulte [requisitos do Exchange (centralizados implantação dos suplementos)](https://docs.microsoft.com/en-us/office365/admin/manage/centralized-deployment-of-add-ins&view=o365-worldwide#exchange-requirements). 

1. Ir para a [página de suplementos & serviços](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) no Centro de administração do Microsoft 365 novo.<br/>![Página de serviços e suplementos no novo Microsoft 365 Admin Center](media/ServicesAddInsPageNewM365AdminCenter.png)<br/> 
    
2. Escolha **+ implantar o suplemento**.<br/>![Escolha implantar o suplemento](media/ServicesAddIns-ChooseDeployAddIn.png)<br/> 
    
3. Na tela do novo suplemento, revise as informações e escolha **Avançar**.<br/>![Detalhes do novo suplemento](media/NewAddInScreen1.png)<br/>
    
4. Selecione **eu quiser adicionar um suplemento da Office Store**e escolha **Avançar**.<br/>![Eu quiser adicionar um novo suplemento](media/NewAddInScreen2.png)<br/> 
    
5. Pesquisa de mensagem de relatório e na lista de resultados, ao lado do relatório de mensagem suplemento, escolha Adicionar.<br/>![Procure a mensagem de relatório e escolha Adicionar](media/NewAddInScreen3.png)<br/>
    
6. Na tela de mensagem de relatório, revise as informações e escolha **Avançar**.<br/>![Detalhes da mensagem de relatório](media/ReportMessageAdd-InNewScreen4.png)<br/>

7. Especifique as configurações de usuário padrão para o Outlook e escolha **Avançar**.<br/>![Relatar as configurações padrão de mensagem do Outlook](media/ReportMessageOptionsScreen5.png)<br/>

8. Especificar quem obtém o suplemento de mensagem de relatório e escolha **Salvar**. <br/>![Quem obtém a mensagem de relatório suplemento](media/ReportMessageOptionsScreen6.png)<br/>

> [!TIP]
> Recomendamos a [configuração de uma regra para obter uma cópia das mensagens de email relatado pelos usuários](#set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users)

Dependendo do que você selecionou usando o assistente, pessoas da sua organização terão o [suplemento de mensagem de relatório](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) disponíveis. Pessoas da sua organização verá os ícones a seguir: 

- No Outlook no ícone tem esta aparência: <br/> ![Suplemento de mensagem ícone de relatório para o Outlook](media/OutlookReportMessageIcon.png)<br/>
- No Outlook Web App no ícone tem esta aparência:<br/>![Outlook no ícone do suplemento de mensagem de relatório na Web](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

## <a name="set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users"></a>Configurar uma regra para obter uma cópia das mensagens de email relatado pelos usuários

> [!IMPORTANT]
> Você deve ser um administrador do Exchange Online para executar essa tarefa.
  
Você pode configurar uma regra para obter uma cópia das mensagens de email relatado pelos usuários em sua organização. Isso é feito depois que você baixou e habilitou o suplemento de mensagem de relatório para sua organização.
  
1. No EAC, selecione o **fluxo de email** \> **regras**. 
    
2. Escolha **+** \> **criar uma nova regra**. 
    
3. Na caixa **nome** , digite um nome, como envios.
    
4. Na lista **Aplicar esta regra se** , escolha **o endereço do destinatário inclui...**. 
    
5. Na tela **Especificar palavras ou expressões** , adicione `junk@office365.microsoft.com` e `phish@office365.microsoft.com`e escolha **Okey**.<br/>![Especificar os endereços de email de lixo eletrônico e phishing para a regra](media/018c1833-f336-4333-a45c-f2e8b75cd698.png)<br/>
  
6. Na lista **faça o seguinte …** , escolha **Cco da mensagem para...**. 
    
7. Adicione um administrador global, administrador de segurança e/ou leitor de segurança que deve receber uma cópia de cada mensagem de email que pessoas reportam à Microsoft e escolha **Okey**.<br/>![Adicionar um administrador global ou de segurança para receber uma cópia de cada mensagem relatada](media/a91ab9d1-66f2-4a2e-9dc1-f9f81a2298ad.png)<br/>
  
8. Selecione **Auditar esta regra com nível de severidade**e escolha **Médio**. 
    
9. Em **Escolher um modo para essa regra**, escolha **Enforce**.<br/>![Configurar uma regra para obter uma cópia de cada mensagem relatada](media/f1cd95ce-e40d-4a8a-8f48-893469eba691.png)<br/>
  
10. Escolha **Salvar**. 
    
Com essa regra in-loco, sempre que alguém em sua organização relata uma mensagem de email usando o suplemento do relatório de mensagem, seu administrador global, administrador de segurança e/ou leitor de segurança receberá uma cópia da mensagem. Essas informações podem permitem definir ou ajustar políticas, como políticas de [Vínculos do Office 365 ATP seguros](atp-safe-links.md) . 

## <a name="review-or-edit-settings-for-the-report-message-add-in"></a>Analisar ou editar as configurações para o suplemento de mensagem de relatório

Você pode examinar e editar as configurações padrão para o relatório de mensagem suplemento na [página serviços e suplementos](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns). 

> [!IMPORTANT]
> Você deve ser um administrador global do Office 365 ou um administrador do Exchange Online para completar esta tarefa.
    
1. Ir para a [página de suplementos & serviços](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) no Centro de administração do Microsoft 365 novo.<br/>![Página de serviços e suplementos no novo Microsoft 365 Admin Center](media/ServicesAddInsPageNewM365AdminCenter.png)<br/>

2. Localize e selecione o suplemento do relatório de mensagem.<br/>![Localize e selecione o suplemento de mensagem de relatório](media/FindReportMessageAddIn.png)<br/> 
    
3. Na tela de mensagem de relatório, revise e editar configurações, conforme apropriado para sua organização.<br/>![Configurações para o suplemento de mensagem de relatório](media/EditReportMessageAddIn.png)<br/> 

## <a name="learn-how-to-use-the-report-message-add-in"></a>Saiba como usar o suplemento de mensagem de relatório

Consulte [usar o suplemento de mensagem de relatório](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).
  
## <a name="related-topics"></a>Tópicos relacionados

[Usar o suplemento de mensagem de relatório](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)
  
[Exibir relatórios de segurança de email na segurança &amp; Centro de conformidade](view-email-security-reports.md)

[Exibir relatórios de proteção de ameaça avançadas do Office 365](view-reports-for-atp.md)

[Use o Explorer na segurança &amp; Centro de conformidade](use-explorer-in-security-and-compliance.md)
  


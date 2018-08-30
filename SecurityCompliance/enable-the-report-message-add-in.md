---
title: Habilitar o suplemento de Mensagem de relatório
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/28/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 4250c4bc-6102-420b-9e0a-a95064837676
description: Aprenda a habilitar o suplemento de mensagem de relatório para o Outlook e Outlook na web, para usuários individuais ou em toda sua organização.
ms.openlocfilehash: 2260f8823132d23e0e1f57a421fd223ea3ab14bd
ms.sourcegitcommit: edf5db9357c0d34573f8cc406314525ef10d1eb9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/28/2018
ms.locfileid: "23229993"
---
# <a name="enable-the-report-message-add-in"></a>Habilitar o suplemento de Mensagem de relatório

O suplemento de mensagem de relatório para o Outlook permite que as pessoas facilmente relatado email classificados incorretamente, se seguros ou mal-intencionada, Microsoft e suas afiliadas para análise. A Microsoft usa essas envios para melhorar a eficácia das tecnologias de proteção de email.
  
Se você for um usuário individual, você pode habilitar o suplemento de mensagem de relatório por conta própria. 
  
Se você for um administrador do Exchange Online, você poderá habilitar o suplemento de mensagem de relatório para sua organização.
    
## <a name="get-the-report-message-add-in-for-yourself"></a>Obtenha a mensagem de relatório suplemento para si mesmo

1. Vá para [https://store.office.com](https://store.office.com)e procure o suplemento de mensagem de relatório.
    
2. Escolha **obtê-lo agora** (ou **Adicionar** ). 
    
3. Analise os termos da política de uso e de privacidade. Em seguida, clique em **continuar**. 
    
4. Entrar no seu email do Office 365 usando seu trabalho ou a conta de escola (para uso de negócios) ou a sua conta da Microsoft (para uso pessoal).
    
Depois que o suplemento está instalado e habilitado, você verá os ícones a seguir: 

- No Outlook no ícone tem esta aparência: </br> ![Suplemento de mensagem ícone de relatório para o Outlook](media/OutlookReportMessageIcon.png)</br>
- No Outlook Web App no ícone tem esta aparência:</br>![Outlook no ícone do suplemento de mensagem de relatório na Web](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)</br>

  
Como o próximo passo, Aprenda como [usar o suplemento de mensagem de relatório](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).
  
## <a name="get-and-enable-the-report-message-add-in-for-your-organization"></a>Obter e habilitar o suplemento de mensagem de relatório para sua organização

> [!IMPORTANT]
> Você deve ser um administrador do Exchange Online para executar essa tarefa.
  
1. Vá para [https://portal.office.com](https://portal.office.com) e entrar usando sua conta do trabalho ou da escola. 
    
2. Escolha **Admin** para ir para o Centro de administração. 
    
3. Escolha **Admin centrais** \> **Exchange** para ir para o Centro de administração do Exchange (EAC). 
    
4. Escolha **organização** \> **suplementos**. 
    
5. Escolha **+** \> **Adicionar da Office Store**. 
    
6. Procure a mensagem de relatório.
    
7. Na lista de **resultados de aplicativo** , localize **A mensagem de relatório**e escolha **obtê-lo agora** (ou **Adicionar** ). 
    
8. Analise os termos da política de uso e de privacidade. Em seguida, clique em **continuar**. 
    
    ![Clique em Continuar para aceitar os termos e a diretiva de privacidade](media/3c813cd6-1601-4791-97dc-f8edbbd3fb6b.png)
  
9. Na tela de confirmação, escolha **Sim**. 
    
10. Após instalar o suplemento de mensagem de relatório, você deve ativá-lo. Para fazer isso, siga estas etapas:
    
1. Volte para o EAC e atualize a janela do navegador.
    
2. Escolha **organização** \> **suplementos**. 
    
3. Na lista de suplementos, selecione a **Mensagem de relatório**. 
    
    ![No EAC, você pode habilitar o suplemento de mensagem de relatório para o Outlook](media/b496743c-55fa-4cdb-aa06-0b2a7aec6dab.png)
  
4. Escolha **Editar**e selecione uma opção para habilitar o suplemento. 
    
    ![Habilitar o suplemento de mensagem de relatório no EAC](media/578b1b66-3620-4a8a-9819-1c9cc6836f37.png)
  
5. Escolha **Salvar**. 
    
> [!TIP]
> Depois que o suplemento está instalado e habilitado, as pessoas na sua organização verá os ícones a seguir: 
  
Em seguida, saiba como [usar o suplemento de mensagem de relatório](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)e configurar uma regra para ver as mensagens de email relatados.
  
### <a name="set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users"></a>Configurar uma regra para obter uma cópia das mensagens de email relatado pelos usuários

> [!IMPORTANT]
> Você deve ser um administrador do Exchange Online para executar essa tarefa.
  
Você pode configurar uma regra para obter uma cópia das mensagens de email relatado pelos usuários em sua organização. Isso é feito depois que você baixou e habilitou o suplemento de mensagem de relatório para sua organização.
  
1. No EAC, selecione o **fluxo de email** \> **regras**. 
    
2. Escolha **+** \> **criar uma nova regra**. 
    
3. Na caixa **nome** , digite um nome, como envios.
    
4. Na lista **Aplicar esta regra se** , escolha **o endereço do destinatário inclui...**. 
    
5. Na tela **Especificar palavras ou expressões** , adicione junk@office365.microsoft.com e phish@office365.microsoft.com e escolha **Okey**. 
    
    ![Especificar os endereços de email de lixo eletrônico e phishing para a regra](media/018c1833-f336-4333-a45c-f2e8b75cd698.png)
  
6. Na lista **faça o seguinte …** , escolha **Cco da mensagem para...**. 
    
7. Adicione um administrador global, administrador de segurança e/ou leitor de segurança que deve receber uma cópia de cada mensagem de email que pessoas reportam à Microsoft e escolha **Okey**. 
    
    ![Adicionar um administrador global ou de segurança para receber uma cópia de cada mensagem relatada](media/a91ab9d1-66f2-4a2e-9dc1-f9f81a2298ad.png)
  
8. Selecione **Auditar esta regra com nível de severidade**e escolha **Médio**. 
    
9. Em **Escolher um modo para essa regra**, escolha **Enforce**. 
    
    ![Configurar uma regra para obter uma cópia de cada mensagem relatada](media/f1cd95ce-e40d-4a8a-8f48-893469eba691.png)
  
10. Escolha **Salvar**. 
    
Com essa regra in-loco, sempre que alguém em sua organização relata uma mensagem de email usando o suplemento do relatório de mensagem, seu administrador global, administrador de segurança e/ou leitor de segurança receberá uma cópia da mensagem. Essas informações podem permitem definir ou ajustar políticas, como políticas de [Vínculos do Office 365 ATP seguros](atp-safe-links.md) . 
  
## <a name="related-topics"></a>Tópicos relacionados

[Usar o suplemento de mensagem de relatório](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)
  
[Proteção Avançada contra Ameaças do Office 365](office-365-atp.md) 
  


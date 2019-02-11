---
title: Classificação de Segurança do Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/25/2019
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c9e7160f-2c34-4bd0-a548-5ddcc862eaef
description: Já se perguntou como seguro sua organização realmente esteja no Office 365? Pontuação segura está aqui para ajudar. Pontuação segura analisa a segurança da sua organização com base nas suas atividades regulares e configurações de segurança no Office 365 e atribui uma pontuação.
ms.openlocfilehash: bc0379e40b09e63e5fded1b1a289d40c306def91
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29559084"
---
# <a name="office-365-secure-score"></a>Classificação de Segurança do Office 365

**Resumo** Já se perguntou como seguro sua organização realmente esteja no Office 365? Pontuação segura está aqui para ajudar. Pontuação segura analisa a segurança da sua organização com base nas suas atividades regulares e configurações de segurança no Office 365 e atribui uma pontuação. Leia este artigo para obter uma visão geral de pontuação seguro e como você pode usá-lo.
  
## <a name="how-to-get-to-secure-score"></a>Como obter a pontuação de seguro

Se sua organização tiver uma assinatura que inclui o [Office 365 Enterprise](https://docs.microsoft.com/office365/enterprise/), [Microsoft 365 Business](https://docs.microsoft.com/microsoft-365/business/)ou Business Premium do Office 365 e você tem as [permissões necessárias](#required-permissions), você pode exibir a pontuação da organização seguro visitando [https://securescore.office.com](https://securescore.office.com). 

Como alternativa, você pode visitar o Centro de conformidade do & de segurança ([https://protection.office.com](https://protection.office.com)), onde você encontrará um widget pontuação seguro que fornece com sua pontuação atual.

![Widget da pontuação de seguro](media/SecureScoreWidget-o365.png)

O widget inclui um link para seu painel pontuação seguro.

![Painel de pontuação de seguro](media/SecureScore-WelcomeScreen.png)
  
## <a name="how-it-works"></a>Como funciona

Pontuação segura determina quais serviços do Office 365 que você estiver usando (por exemplo, Exchange, SharePoint e OneDrive), em seguida, compara as configurações e as atividades a uma linha de base estabelecida pela Microsoft. Você receberá uma pontuação com base em como bem alinhado à sua organização estiver com as práticas recomendadas de segurança. Você também terá recomendações sobre etapas que podem ser realizadas para melhorar a pontuação da sua organização. 
  
![Fila de ações na ferramenta de pontuação seguro do Office 365](media/SecureScore-ActionsToTake.png)
  
Pontuação segura calcula sua pontuação com base nos serviços fornecidos por que você comprou. Por exemplo, se você comprou somente um plano do Exchange Online, você não marcados para recursos de segurança do SharePoint Online. Denominador da pontuação de é a soma de todas as linhas de base para os controles que se aplicam aos produtos que você comprou. O numerador é a soma de todos os controles para os quais você concluída ou parcialmente concluído, as ações para atender a esse controle.

Expanda uma ação para saber quais etapas a serem seguidas, protegem-lo contra as ameaças que ele ajudará e quantos pontos sua pontuação aumentará depois que você segue a recomendação.
  
![Ação expandida na ferramenta de pontuação seguro do Office 365](media/SecureScore-DetailedActionToTake.png)
  
Para ver o impacto de suas ações na segurança da sua organização, selecione a guia do **Analisador de pontuação** e analisar o histórico. 
  
![Guia do analisador de pontuação da ferramenta pontuação seguro do Office 365](media/SecureScore-ScoreAnalyzer-7days.png)
  
O gráfico abaixo, você verá uma lista de ações e pontuações por categoria. 
  
![Na guia analisador de pontuação mostrando um ponto de dados selecionado do gráfico](media/SecureScore-Analyzer-breakdownbelowchart.png)
 
Ações que são rotuladas como **[Não avaliados]** são aquelas que você pode executar para sua organização, mas porque não estão conectados à pontuação seguro, eles não são avaliados.  

Na página do **Analisador de pontuação** , clique em um ponto de dados para um determinado dia, role para baixo para ver as ações concluídas e incompletas daquele dia descobrir o que são alteradas. A pontuação é calculada uma vez por dia (cerca 1:00 AM. PST). Se você fizer uma alteração em uma ação medida, a pontuação atualizará automaticamente o próximo dia. Leva até 48 horas para que uma alteração refletido na sua pontuação.

Pontuação segura não expressa uma medida absoluta de como provavelmente você devem obter violado. Ele expressa a extensão ao qual você adotaram recursos que podem deslocar o risco de ser violado. Nenhum serviço pode garantir que você não vai ser violado e a pontuação seguro não deve ser interpretada como uma garantia de nenhuma maneira.
 
## <a name="how-secure-score-helps"></a>Como o ajuda a pontuação de seguro

Com pontuação seguro, você pode ajudar a melhorar a situação de segurança da sua organização usando os recursos internos de segurança no Office 365 (muitos dos quais você já adquiriu mas não estar ciente). Aprender mais sobre esses recursos pode ajudar a fornecer tranquilo que você estiver levando os procedimentos apropriados para proteger sua organização contra ameaças.
  
Mas não apenas se o nosso word para ele. Clientes que utilizam o Secure pontuação vimos seus pontuação aumentar a cinco vezes maior em relação a clientes que não são utilizá-lo. (O aumento de seus pontuação corresponde com os recursos de segurança que está sendo usados em suas organizações.)
  
> [!NOTE]
> Pontuação segura não expressa uma medida absoluta de como provavelmente você devem obter violado. Ele expressa a extensão ao qual você adotaram controles que podem deslocar o risco de ser violado. Nenhum serviço pode garantir que você não vai ser violado e pontuação seguro não deve ser interpretada como uma garantia de nenhuma maneira. 
  
## <a name="required-permissions"></a>Permissões necessárias

Para exibir e usar o seu painel pontuação seguro, você deve ter uma das seguintes funções no Windows Azure Active Directory:
- Administrador global
- Administrador de faturamento
- Administrador de usuários
- Administrador de senha
- Administrador de segurança
- Leitor de segurança
- Administrador do Exchange
- Administrador do SharePoint

 Usuários que não estão atribuídos a uma função de administrador não conseguirá acessar pontuação seguro.

## <a name="related-topics"></a>Tópicos relacionados

[Visão geral do painel de segurança](security-dashboard.md)

[Qual assinatura eu tenho?](https://docs.microsoft.com/office365/admin/admin-overview/what-subscription-do-i-have?view=o365-worldwide)
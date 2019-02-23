---
title: Classificação de Segurança do Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/13/2019
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c9e7160f-2c34-4bd0-a548-5ddcc862eaef
description: Você já se perguntou qual é a segurança da sua organização no Office 365? A pontuação segura está aqui para ajudar. A pontuação segura analisa a segurança da sua organização com base em suas atividades regulares e configurações de segurança no Office 365 e atribui uma pontuação.
ms.openlocfilehash: dd0dc87910853eba9f2ec3ec6752e857462b46e5
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220351"
---
# <a name="office-365-secure-score"></a>Classificação de Segurança do Office 365

**Resumo** Você já se perguntou qual é a segurança da sua organização no Office 365? A pontuação segura está aqui para ajudar. A pontuação segura analisa a segurança da sua organização com base em suas atividades regulares e configurações de segurança no Office 365 e atribui uma pontuação. Leia este artigo para obter uma visão geral da Pontuação segura e como você pode usá-lo.
  
## <a name="how-to-get-to-secure-score"></a>Como obter a pontuação segura

Se sua organização tem uma assinatura que inclui o [office 365 Enterprise](https://docs.microsoft.com/office365/enterprise/), [o Microsoft 365 Business](https://docs.microsoft.com/microsoft-365/business/)ou o Office 365 Business Premium e você tem as [permissões necessárias](#required-permissions), pode exibir a pontuação segura da sua organização visitando [https://securescore.office.com](https://securescore.office.com). 

Como alternativa, você pode visitar o centro de conformidade do &[https://protection.office.com](https://protection.office.com)de segurança (), onde encontrará um widget de Pontuação segura que fornece a sua pontuação atual.

![Widget Pontuação segura](media/SecureScoreWidget-o365.png)

O widget inclui um link para seu painel de Pontuação segura.

![Painel de Pontuação segura](media/SecureScore-WelcomeScreen.png)
  
## <a name="how-it-works"></a>Como funciona

A pontuação segura determina quais serviços do Office 365 você está usando (como OneDrive, SharePoint e Exchange) e compara suas configurações e atividades com uma linha de base estabelecida pela Microsoft. Você receberá uma pontuação com base em como a organização está bem alinhada com as práticas recomendadas de segurança. Você também terá recomendações sobre as etapas que você pode tomar para melhorar a pontuação da sua organização. 
  
![Fila de ações na ferramenta de Pontuação segura do Office 365](media/SecureScore-ActionsToTake.png)
  
A pontuação segura calcula sua pontuação com base nos serviços que você comprou. Por exemplo, se você comprou apenas um plano do Exchange Online, você não terá a Pontuação dos recursos de segurança do SharePoint Online. O denominador da pontuação é a soma de todas as linhas de base para os controles que se aplicam aos produtos que você comprou. O numerador é a soma de todos os controles que você concluiu, ou parcialmente concluído, as ações para preencher esse controle.

Expanda uma ação para saber mais sobre as etapas a serem tomadas, as ameaças às quais ele ajudará a proteger você e quantos pontos sua pontuação aumentará depois que você seguir a recomendação.
  
![Ação expandida na ferramenta de Pontuação segura do Office 365](media/SecureScore-DetailedActionToTake.png)
  
Para ver o impacto de suas ações na segurança da sua organização, selecione a guia analisador de **pontos** e revise o histórico. 
  
![Guia analisador de pontos da ferramenta de Pontuação segura do Office 365](media/SecureScore-ScoreAnalyzer-7days.png)
  
Abaixo do gráfico, você verá uma lista de resultados e ações por categoria. 
  
![Gráfico na guia do analisador de pontos mostrando um ponto de dados selecionado](media/SecureScore-Analyzer-breakdownbelowchart.png)
 
As ações que são rotuladas como **[não classificadas]** são aquelas que podem ser realizadas na sua organização, mas como não estão conectadas à pontuação segura, elas não são pontuadas.  

Na página **analisador de Pontuação** , clique em um ponto de dados para um dia específico e, em seguida, role para baixo para ver as ações concluídas e incompletas desse dia para descobrir o que foi alterado. A pontuação é calculada uma vez por dia (em torno de 1:00 AM PST). Se você fizer uma alteração em uma ação medida, a pontuação será automaticamente atualizada no dia seguinte. Leva até 48 horas para que uma alteração seja refletida na sua pontuação.

A pontuação segura não expressa uma medida absoluta da probabilidade de você ser violada. Ele expressa a extensão à qual você adotou recursos que podem compensar o risco de ser violado. Nenhum serviço pode garantir que você não será violado, e a pontuação segura não deve ser interpretada como uma garantia de qualquer forma.
 
## <a name="how-secure-score-helps"></a>Como a pontuação segura ajuda

Com a pontuação segura, você pode ajudar a melhorar a postura de segurança da sua organização usando os recursos de segurança internos no Office 365 (muitos dos quais você já comprou, mas pode não estar ciente). Saber mais sobre esses recursos pode ajudar a garantir que você esteja seguindo as etapas certas para proteger sua organização contra ameaças.
  
Mas não considere apenas nossa palavra. Os clientes que usam a pontuação segura perceberam que a pontuação aumentou cinco vezes mais do que os clientes que não o estão usando. (O aumento na pontuação corresponde aos recursos de segurança que estão sendo usados em suas organizações.)
  
> [!NOTE]
> A pontuação segura não expressa uma medida absoluta da probabilidade de você ser violada. Ele expressa a extensão à qual você adotou controles que podem compensar o risco de ser violado. Nenhum serviço pode garantir que você não será violado, e a pontuação segura não deve ser interpretada como uma garantia de qualquer forma. 
  
## <a name="required-permissions"></a>Permissões necessárias

Para exibir e usar seu painel de Pontuação segura, você deve receber uma das seguintes funções no [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles):
- Administrador global
- Administrador de cobrança
- Administrador de usuários
- Administrador de senha
- Administrador de segurança
- Leitor de segurança
- Administrador do Exchange
- Administrador do SharePoint

 Os usuários que não são atribuídos a uma função de administrador não poderão acessar a pontuação segura.

## <a name="related-topics"></a>Tópicos relacionados

[Visão geral do painel de segurança](security-dashboard.md)

[Qual assinatura eu tenho?](https://docs.microsoft.com/office365/admin/admin-overview/what-subscription-do-i-have?view=o365-worldwide)

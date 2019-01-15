---
title: Classificação de Segurança do Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 11/27/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c9e7160f-2c34-4bd0-a548-5ddcc862eaef
description: Já se perguntou como seguro sua organização realmente esteja no Office 365? Pontuação segura está aqui para ajudar. Pontuação segura analisa a segurança da sua organização com base nas suas atividades regulares e configurações de segurança no Office 365 e atribui uma pontuação.
ms.openlocfilehash: 08d452f2b297948c13243a5eb36ae6e22839e545
ms.sourcegitcommit: 9034809b6f308bedc3b8ddcca8242586b5c30f94
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/15/2019
ms.locfileid: "28015063"
---
# <a name="office-365-secure-score"></a>Classificação de Segurança do Office 365

**Resumo** Já se perguntou como seguro sua organização realmente esteja no Office 365? Pontuação segura está aqui para ajudar. Pontuação segura analisa a segurança da sua organização com base nas suas atividades regulares e configurações de segurança no Office 365 e atribui uma pontuação. Leia este artigo para obter uma visão geral de pontuação seguro e como você pode usá-lo.
  
## <a name="how-to-get-to-secure-score"></a>Como obter a pontuação de seguro

Se sua organização tiver uma assinatura que inclui o [Office 365 Enterprise](https://docs.microsoft.com/office365/enterprise/), [Microsoft 365 Business](https://docs.microsoft.com/microsoft-365/business/)ou Business Premium do Office 365 e você tem as permissões necessárias, você pode exibir a pontuação da organização seguro visitando [https://securescore.office.com](https://securescore.office.com). 

Como alternativa, você pode visitar o Centro de conformidade e segurança ([https://protection.office.com](https://protection.office.com)), onde você encontrará um widget pontuação seguro que fornece com sua pontuação atual.

![Widget da pontuação de seguro](media/SecureScoreWidget-o365.png)

O widget inclui um link para os pontuação de seguro da Microsoft, que leva para seu painel pontuação seguro para o Office 365.

![Painel de pontuação de seguro](media/SecureScore-WelcomeScreen.png)

> [!NOTE]
> Você deve ser um administrador do Office 365, como um administrador global ou administrador de segurança, para acessar a pontuação seguro.
  
## <a name="how-it-works"></a>Como funciona

Proteja a pontuação descobre o que você estiver usando (por exemplo, Exchange, SharePoint e OneDrive), em seguida, serviços do Office 365 analisa suas configurações e atividades e compará-los a uma linha de base estabelecida pela Microsoft. Você receberá uma pontuação com base em como alinhado estiver com as práticas recomendadas de segurança.
  
Você também terá recomendações sobre etapas que podem ser realizadas para melhorar a pontuação da sua organização. 
  
![Fila de ações na ferramenta de pontuação seguro do Office 365](media/SecureScore-ActionsToTake.png)
  
Expanda uma ação para saber quais etapas a serem seguidas, protegem-lo contra as ameaças que ele ajudará e quantos pontos sua pontuação aumentará depois que você segue a recomendação.
  
![Ação expandida na ferramenta de pontuação seguro do Office 365](media/SecureScore-DetailedActionToTake.png)
  
Para ver o impacto de suas ações na segurança da sua organização, selecione a guia do **Analisador de pontuação** e analisar o histórico. 
  
![Guia do analisador de pontuação da ferramenta pontuação seguro do Office 365](media/SecureScore-ScoreAnalyzer-7days.png)
  
O gráfico abaixo, você verá uma lista de ações e pontuações por categoria.
  
![Na guia analisador de pontuação mostrando um ponto de dados selecionado do gráfico](media/SecureScore-Analyzer-breakdownbelowchart.png)
  
## <a name="how-secure-score-helps"></a>Como o ajuda a pontuação de seguro

Usar pontuação seguro ajuda a aumentar a segurança da sua organização por encorajando utilizar os recursos internos de segurança no Office 365 (muitos dos quais você já adquiriu mas não estar ciente). Aprender mais sobre esses recursos, como usar a ferramenta permitirão que você peça mente que você estiver levando os procedimentos apropriados para proteger sua organização contra ameaças.
  
Mas não apenas se o nosso word para ele. Clientes que utilizam o Secure pontuação vimos seus pontuação aumentar a cinco vezes maior em relação a clientes que não são utilizá-lo. (O aumento de seus pontuação corresponde com os recursos de segurança que está sendo usados em suas organizações.)
  
> [!NOTE]
> Pontuação segura não expressa uma medida absoluta de como provavelmente você devem obter violado. Ele expressa a extensão ao qual você adotaram controles que podem deslocar o risco de ser violado. Nenhum serviço pode garantir que você não vai ser violado e pontuação seguro não deve ser interpretada como uma garantia de nenhuma maneira. 
  
## <a name="faqs"></a>Perguntas frequentes

### <a name="who-can-use-secure-score"></a>Quem pode usar pontuação seguro?

Qualquer pessoa que tenha permissões de administrador (administrador global ou uma função personalizada admin) para uma assinatura do Office 365 Enterprise, Microsoft 365 Business ou Office 365 Business Premium pode acessar seguro pontuação no [https://securescore.office.com](https://securescore.office.com). Usuários que não estão atribuídos a uma função de administrador não conseguirá acessar pontuação seguro. No entanto, os administradores podem usar a ferramenta para compartilhar seus resultados com outras pessoas em suas organizações. Estamos examinando incluindo outras, funções de não-administrador na lista de permissões no futuro. Se houver funções específicas que você gostaria que nós a serem considerados, fale pelo lançamento no [segurança do Office, privacidade &amp; comunidade de conformidade](https://techcommunity.microsoft.com/t5/Security-Privacy-Compliance/bd-p/security_privacy).
  
### <a name="what-does-not-scored-mean"></a>O que significa [não avaliados] significa?

Ações de rotulado como **[Não avaliados]** são aquelas você pode executar em sua organização, mas não marcados porque eles não estão conectados na ferramenta (ainda!). Portanto, você ainda pode melhorar sua segurança, mas você não obterá crédito para essas ações conveniente. 
  
### <a name="how-often-is-my-score-updated"></a>Frequência é minha pontuação atualizada?

A pontuação é calculada uma vez por dia (cerca 1:00 AM. PST). Se você fizer uma alteração em uma ação medida, a pontuação atualizará automaticamente o próximo dia. Leva até 48 horas para que uma alteração refletido na sua pontuação.
  
### <a name="who-can-see-my-results"></a>Quem pode ver meus resultados?

Os resultados são filtrados para mostrar as pontuações somente para pessoas na sua organização que são atribuídos a uma função de administrador (administrador global ou uma função personalizada admin).
  
### <a name="my-score-changed-how-do-i-figure-out-why"></a>Minha pontuação foi alterada. Como descobrir o porquê?

Na página do **Analisador de pontuação** , clique em um ponto de dados para um determinado dia, role para baixo para ver as ações concluídas e incompletas daquele dia descobrir o que são alteradas. 
  
### <a name="does-the-secure-score-measure-my-risk-of-getting-breached"></a>A pontuação seguro avalia a minha risco de obtenção violado?

Em breve, não. Pontuação segura não expressa uma medida absoluta de como provavelmente você devem obter violado. Ele expressa a extensão ao qual você adotaram recursos que podem deslocar o risco de ser violado. Nenhum serviço pode garantir que você não vai ser violado e a pontuação seguro não deve ser interpretada como uma garantia de nenhuma maneira.
  
### <a name="how-should-i-interpret-my-score"></a>Como posso deve interpretar minha pontuação?

Você receba pontos para a configuração recomendada de recursos de segurança ou a realização de tarefas relacionadas à segurança (por exemplo, exibindo relatórios). Algumas ações são avaliadas para conclusão parcial, como permitir que a autenticação multifator (MFA) para seus usuários. Sua pontuação seguro diretamente é representante dos serviços de segurança do Microsoft que você usa. Lembre-se de que a segurança deve sempre ser equilibrada com facilidade de uso. Todos os controles de segurança tem um componente de impacto do usuário. Controles contendo o impacto de usuário baixa não devem ter pouco ou nenhum efeito nas operações diárias de seus usuários.
  
Para ver seu histórico de pontuação, vá para a página do **Analisador de pontuação** . Escolha uma data específica para ver quais controles foram habilitados para se dia e o que aponta você acumulado para cada um deles. 
  
### <a name="i-have-an-idea-for-another-control-how-do-i-let-you-know-what-it-is"></a>Posso ter uma ideia para outro controle. Como eu permitem que você sabe o que ele?

Nós queremos saber a sua opinião. Envie suas ideias sobre o [segurança do Office, privacidade &amp; comunidade de conformidade](https://go.microsoft.com/fwlink/?linkid=836898). Estamos está ouvindo e a pontuação seguro para incluir todas as opções que são importantes para você.
  
### <a name="something-isnt-working-right-who-should-i-contact"></a>Algo não está funcionando direito. Quem posso contatar?

Se você tiver quaisquer problemas, informe-pelo lançamento no [segurança do Office, privacidade &amp; comunidade de conformidade](hhttps://techcommunity.microsoft.com/t5/Security-Privacy-Compliance/bd-p/security_privacy). Estamos monitorando da comunidade e fornecerá a Ajuda.
  
### <a name="my-organization-only-has-certain-security-features-does-this-affect-my-score"></a>Minha organização tem apenas alguns recursos de segurança. Isso afeta minha pontuação?

Pontuação segura calcula sua pontuação com base nos serviços fornecidos por que você comprou. Por exemplo, se você comprou somente um plano do Exchange Online, você não marcados para recursos de segurança do SharePoint Online. Denominador da pontuação de é a soma de todas as linhas de base para os controles que se aplicam aos produtos que você comprou. O numerador é a soma de todos os controles para os quais você concluída ou parcialmente concluído, as ações para atender a esse controle.

## <a name="related-topics"></a>Tópicos relacionados

[Visão geral do painel de segurança](security-dashboard.md)

[Qual assinatura eu tenho?](https://docs.microsoft.com/office365/admin/admin-overview/what-subscription-do-i-have?view=o365-worldwide)
  


---
title: Exibir os relatórios de prevenção contra perda de dados
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/7/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid:
- MOE150
- MET150
description: Com os relatórios de DLP no Office 365, você pode exibir rapidamente o número de correspondências de política de DLP, substituições ou falsos positivos; Veja se eles estão em tendência de cima ou para baixo ao longo do tempo; filtrar o relatório de formas diferentes; e exiba detalhes adicionais selecionando um ponto em uma linha no gráfico.
ms.openlocfilehash: 480ab99b2d84adfbb87288e1e0986441ef56ef99
ms.sourcegitcommit: ed822a776d3419853453583e882f3c61ca26d4b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2019
ms.locfileid: "30410696"
---
# <a name="view-the-reports-for-data-loss-prevention"></a>Exibir os relatórios de prevenção contra perda de dados

Após criar as políticas de prevenção de perda de dados (DLP), convém verificar se estão funcionando conforme o esperado e ajudando você a se manter em conformidade. Com os relatórios de DLP no centro de conformidade &amp; de segurança do Office 365, você pode rapidamente exibir:
  
- **Correspondências de política DLP** Este relatório mostra a contagem de correspondências de política de DLP ao longo do tempo. Você pode filtrar o relatório por data, local, política ou ação. Você pode usar este relatório para: 
    
  - Ajuste ou Refine suas políticas de DLP enquanto as executa no modo de teste. Você pode exibir a regra específica que correspondeu ao conteúdo.
    
  - Se concentrar em períodos de tempo específicos e entender os motivos para picos e tendências.
    
  - Descubra os processos de negócios que violam as políticas de DLP da sua organização.
    
  - Entenda qualquer impacto nos negócios das políticas de DLP observando quais ações estão sendo aplicadas ao conteúdo.
    
  - Verificar a conformidade com uma determinada política DLP mostrando as correspondências dessa política.
    
  - Exibir uma lista dos principais usuários e repetir usuários que estão contribuindo com incidentes em sua organização.
    
  - Exibir uma lista dos principais tipos de informações confidenciais em sua organização.
    
- **Incidentes de DLP** Este relatório também mostra correspondências de política com o tempo, como o relatório de correspondências de política. No enTanto, o relatório de correspondências de política mostra correspondências em um nível de regra; por exemplo, se um email coincidir com três regras diferentes, o relatório de correspondência de política mostrará três itens de linha diferentes. Por outro lado, o relatório de incidentes mostra correspondências em um nível de item; por exemplo, se um email coincidir com três regras diferentes, o relatório de incidentes mostrará um único item de linha para essa parte do conteúdo. 
    
  Como as contagens de relatórios são agregadas de forma diferente, o relatório de correspondências de política é melhor para identificar correspondências com regras específicas e ajustar as políticas de DLP. O relatório de incidentes é melhor para identificar partes específicas do conteúdo que são problemáticas para suas políticas de DLP.
    
- **Falsos positivos e substituições de DLP** Se sua política de DLP permitir que os usuários substituam ou relatem um falso positivo, esse relatório mostrará uma contagem de tais instâncias ao longo do tempo. Você pode filtrar o relatório por data, local ou política. Você pode usar este relatório para: 
    
  - Ajuste ou Refine suas políticas de DLP, conferindo quais políticas provocam um grande número de falsos positivos.
    
  - Exibir as justificativas enviadas pelos usuários quando eles resolverem uma dica de política substituindo a política.
    
  - Descubra onde as políticas de DLP entram em conflito com processos de negócios válidos incorrendo um grande número de substituições de usuário.
    
Todos os relatórios DLP podem mostrar dados do período de tempo de quatro meses mais recente. Os dados mais recentes podem levar até 24 horas para serem exibidos nos relatórios.
  
Você &amp; pode encontrar esses relatórios no **painel** **relatórios** \> do centro \> de conformidade de segurança.
  
![Relatório de correspondências de política DLP](media/117d20c9-d379-403f-ad68-1f5cd6c4e5cf.png)
  
## <a name="view-the-justification-submitted-by-a-user-for-an-override"></a>Exibir a justificativa enviada por um usuário para uma substituição

Se sua política de DLP permitir que os usuários o substituam, você poderá usar o falso positivo e substituir relatório para exibir o texto enviado por usuários na dica de política.
  
![Campo de justificativa em detalhes do relatório falso positivo e substituição do DLP](media/e11e3126-026d-4e77-a16d-74a0686d1fa3.png)
  
## <a name="take-action-on-insights-and-recommendations"></a>Executar ações em ideias e recomendações

Os relatórios podem mostrar ideias e recomendações onde você pode clicar no ícone de aviso vermelho para ver detalhes sobre possíveis problemas e realizar ações corretivas possíveis.
  
![Clicando em um ícone do insights para ver detalhes e ações a serem tomadas](media/51782036-7299-4960-8175-75c2b1637159.png)
  
## <a name="find-the-cmdlets-for-the-dlp-reports"></a>Localizar os cmdlets dos relatórios de DLP

Para usar a maioria dos cmdlets do centro de &amp; conformidade de segurança, você precisa:
  
1. [Conectar ao &amp;Centro de Conformidade e Segurança do Office 365 usando o PowerShell remoto](http://go.microsoft.com/fwlink/?LinkID=799771&amp;clcid=0x409)
    
2. Use qualquer um destes [cmdlets do &amp; centro de conformidade de segurança do Office 365](http://go.microsoft.com/fwlink/?LinkID=799772&amp;clcid=0x409)
    
No enTanto, os relatórios de DLP precisam de dados de recebimento no Office 365, incluindo o Exchange Online. Por esse motivo, os cmdlets dos relatórios DLP estão disponíveis no PowerShell do Exchange Online, e não no &amp; PowerShell do centro de conformidade de segurança. Portanto, para usar os cmdlets dos relatórios de DLP, você precisa:
  
1. [Conectar-se ao Exchange Online usando o PowerShell remoto](http://go.microsoft.com/fwlink/?LinkID=799773&amp;clcid=0x409)
    
2. Use qualquer um destes cmdlets para os relatórios de DLP:
    
      - [Get-DlpDetectionsReport](http://go.microsoft.com/fwlink/?LinkID=799774&amp;clcid=0x409)
    
      - [Get-DlpDetailReport](http://go.microsoft.com/fwlink/?LinkID=799775&amp;clcid=0x409)
    


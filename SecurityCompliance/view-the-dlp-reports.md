---
title: Exibir os relatórios de prevenção contra perda de dados
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/7/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 41eb4324-c513-4fa5-91c8-8fbd8aaba83b
description: Com os relatórios DLP no Office 365, você pode exibir rapidamente o número de correspondências de política DLP, substituições ou falsos positivos; Consulte se eles estiver tendências para cima ou para baixo ao longo do tempo; Filtrar o relatório de maneiras diferentes; e exibir os detalhes adicionais, selecionando um ponto em uma linha no gráfico.
ms.openlocfilehash: 379e66fc3f2611cf338739d030c2b1d48e7416d8
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "23013905"
---
# <a name="view-the-reports-for-data-loss-prevention"></a>Exibir os relatórios de prevenção contra perda de dados

Depois de criar sua perda de dados políticas prevention (DLP), você vai querer verificar se ele estão funcionando conforme você destinada e ajudá-lo a permanecer em conformidade. Com o DLP relatórios na segurança do Office 365 &amp; Centro de conformidade, você pode visualizar rapidamente:
  
- **Correspondências de política DLP** Este relatório mostra a contagem de correspondências de política DLP ao longo do tempo. Você pode filtrar o relatório por data, local, política ou ação. Você pode usar este relatório para: 
    
  - Ajustar ou refinar suas políticas de DLP conforme você executá-los no modo de teste. Você pode exibir a regra específica que correspondem o conteúdo.
    
  - Se concentrar em períodos de tempo específicos e entender os motivos para picos e tendências.
    
  - Descubra os processos de negócios que violam as políticas de DLP da sua organização.
    
  - Compreenda qualquer impacto nos negócios das diretivas DLP, conferindo quais ações estão sendo aplicadas ao conteúdo.
    
  - Verificar a conformidade com uma determinada política DLP mostrando as correspondências dessa política.
    
  - Exibir uma lista dos principais usuários e repita a usuários que estão contribuindo para incidentes em sua organização.
    
  - Exiba uma lista dos principais tipos de informações confidenciais em sua organização.
    
- **Incidentes DLP** Este relatório também mostra correspondências de política ao longo do tempo, como a política faz a correspondência de relatório. No entanto, a política corresponde correspondências de apresentações de relatório em um nível de regra; Por exemplo, se um email correspondida três regras diferentes, a correspondências de política relatório mostra três diferentes itens de linha. Em contrapartida, o relatório de incidentes mostra correspondências em um nível de item; Por exemplo, se um email correspondida três regras diferentes, o relatório de incidentes mostra um único item de linha para essa parte do conteúdo. 
    
  Porque as contagens de relatório são agregadas de forma diferente, o relatório de correspondências de política é melhor para identificando correspondências com regras específicas e ajuste fino políticas de DLP. O relatório de incidentes é melhor para identificar partes específicas de conteúdo que são problemáticos para suas políticas de DLP.
    
- **Substituições e falsos positivos DLP** Se a sua política DLP permite aos usuários substituí-la ou relatar um falso positivo, esse relatório mostra uma contagem de tais instâncias ao longo do tempo. Você pode filtrar o relatório por data, local ou política. Você pode usar este relatório para: 
    
  - Ajustar ou refinar suas políticas de DLP, conferindo quais políticas incorrem um alto número de falsos positivos.
    
  - Exiba as justificativas enviadas pelos usuários quando eles resolvem uma dica de política, substituindo a política.
    
  - Descobrir onde o conflito de políticas DLP com processos de negócios válida por incorrer em um alto número de usuário substitui.
    
Todos os relatórios DLP podem mostrar dados desde o período de tempo de quatro meses mais recente. Os dados mais recentes podem demorar até 24 horas apareça nos relatórios.
  
Você pode encontrar esses relatórios na segurança &amp; Centro de conformidade \> **relatórios** \> **painel**.
  
![Relatório de correspondências de política DLP](media/117d20c9-d379-403f-ad68-1f5cd6c4e5cf.png)
  
## <a name="view-the-justification-submitted-by-a-user-for-an-override"></a>Exibir a justificação enviada por um usuário para uma substituição

Se sua política DLP permite que os usuários substituí-la, use o falso positivo e substituir o relatório para exibir o texto enviado por usuários na dica de política.
  
![Campo justificativa nos detalhes do relatório de substituição de falso positivo DLP e](media/e11e3126-026d-4e77-a16d-74a0686d1fa3.png)
  
## <a name="take-action-on-insights-and-recommendations"></a>Combater ideias e recomendações

Relatórios podem mostrar ideias e recomendações, onde você pode clicar no ícone de aviso vermelho para ver detalhes específicos sobre possíveis problemas e tomar corretivas possíveis.
  
![Clicar em um ícone de ideias para ver os detalhes e ações a serem tomadas](media/51782036-7299-4960-8175-75c2b1637159.png)
  
## <a name="find-the-cmdlets-for-the-dlp-reports"></a>Encontre os cmdlets para os relatórios DLP

Para usar a maioria dos cmdlets para a segurança &amp; Centro de conformidade, você precisa:
  
1. [Conecte-se para a segurança do Office 365 &amp; usando o PowerShell remoto do Centro de conformidade](http://go.microsoft.com/fwlink/?LinkID=799771&amp;clcid=0x409)
    
2. Use qualquer uma dessas [a segurança do Office 365 &amp; cmdlets do Centro de conformidade](http://go.microsoft.com/fwlink/?LinkID=799772&amp;clcid=0x409)
    
No entanto, os relatórios DLP precisam receber dados dos across Office 365, incluindo o Exchange Online. Por esse motivo, os cmdlets para os relatórios de DLP estão disponíveis no Exchange Online Powershell — não na segurança &amp; Powershell do Centro de conformidade. Portanto, para usar os cmdlets para os relatórios de DLP, você precisa:
  
1. [Conectar-se ao Exchange Online usando o PowerShell remoto](http://go.microsoft.com/fwlink/?LinkID=799773&amp;clcid=0x409)
    
2. Use qualquer um desses cmdlets para os relatórios de DLP:
    
      - [Get-DlpDetectionsReport](http://go.microsoft.com/fwlink/?LinkID=799774&amp;clcid=0x409)
    
      - [Get-DlpDetailReport](http://go.microsoft.com/fwlink/?LinkID=799775&amp;clcid=0x409)
    


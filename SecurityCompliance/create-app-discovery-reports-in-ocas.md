---
title: Criar relatórios de descoberta de aplicativo usando o Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 1/28/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 3e68e691-1fc4-4d3e-a2c0-d3134eb64055
description: Criar relatórios com o Office 365 Cloud app Security que permite que você entenda como as pessoas em sua organização estão usando o Office 365 e outros aplicativos.
ms.openlocfilehash: 23165a52a09e5bcde46ee3ab2110dc17d0faf7f4
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220291"
---
# <a name="create-app-discovery-reports-using-office-365-cloud-app-security"></a>Criar relatórios de descoberta de aplicativo usando o Office 365 Cloud App Security

|Avaliação * *\>**|Planejamento * *\>**|Implantação * *\>**|Utilização * * *|
|:-----|:-----|:-----|:-----|
|[Iniciar avaliação](office-365-cas-overview.md) <br/> |[Iniciar planejamento](get-ready-for-office-365-cas.md) <br/> |[Iniciar implantação](turn-on-office-365-cas.md) <br/> |Você está aqui!  <br/> [Próximas etapas](#next-steps) <br/> |
   
O Office 365 Cloud app Security ajuda administradores globais, administradores de segurança e leitores de segurança a obter informações sobre os serviços de nuvem que as pessoas de uma organização estão usando. Por exemplo, você pode ver onde os usuários estão armazenando e colaborando em documentos e quantos dados estão sendo carregados para aplicativos ou serviços que estão fora do Office 365.
  
Para gerar um relatório de descoberta de aplicativos, você carrega manualmente seus arquivos de log de tráfego da Web de seus firewalls e proxies e, em seguida, o Office 365 Cloud app Security analisa e analisa esses arquivos para o seu relatório.
  
> [!NOTE]
> Você deve ser um administrador global, administrador de segurança ou leitor de segurança para executar as tarefas descritas neste artigo. Para saber mais, confira [permissões no centro de conformidade &amp; de segurança do Office 365](permissions-in-the-security-and-compliance-center.md). 
  
## <a name="create-a-report-with-app-discovery"></a>Criar um relatório com descoberta de aplicativos

Para criar um relatório de descoberta de aplicativos, identifique a fonte de dados do fornecedor para os arquivos de log que você deseja que sejam analisados, selecione os arquivos de log e solicite o relatório.
  
> [!NOTE]
> Use arquivos de log de tráfego da Web que incluem períodos de pico de tráfego para obter a melhor representação de uso em sua organização. 
  
1. Coletar seus [logs de tráfego da Web e fontes de dados para o Office 365 Cloud app Security](web-traffic-logs-and-data-sources-for-ocas.md).
    
2. Vá para o portal do Cloud app Security[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)() e entre. 
       
3. Escolha **descobrir** \> **criar novo relatório**. <br>![No portal CAS do Office 365, escolha descobrir](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)<br>
  
4. Especifique um nome e uma descrição para o seu relatório e, em seguida, selecione a fonte de dados para os logs de tráfego da Web na lista de **fontes de dados** . <br>![Em CAS do O365, escolha \> descobrir criar novo relatório](media/22e660f0-5eb2-49fa-9fea-f88a5809a07b.png)<br>Se uma fonte de dados que você gostaria de usar não estiver listada, você poderá solicitar que ela seja adicionada. Selecione **outro** para a **fonte de dados**e, em seguida, digite o nome da fonte de dados que você está tentando carregar. Examinaremos o log e informaremos se Adicionamos suporte para a fonte de dados que a gerou. 
  
5. Navegue até o local dos arquivos de log coletados e selecione os arquivos. Os arquivos de log devem ter sido gerados pela fonte de dados que você escolheu para o relatório.
    
6. Clique em **criar** para iniciar o processo de criação de relatórios. 
    
7. Para ver o status do relatório, clique em **Gerenciar relatórios de instantâneo**. Quando um relatório estiver pronto, você verá a opção **Exibir relatório** . 
    
## <a name="next-steps"></a>Próximas etapas

- [ReVisar e executar ação em alertas](review-office-365-cas-alerts.md)
    
- [Analisar descobertas de aplicativos do Office 365 Cloud App Security](review-app-discovery-findings-in-ocas.md)
    
- ReVisar suas [atividades de utilização do Office 365 Cloud app Security](utilization-activities-for-ocas.md)
    


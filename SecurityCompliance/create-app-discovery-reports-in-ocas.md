---
title: Criar relatórios de descoberta de aplicativo usando o Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/26/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 3e68e691-1fc4-4d3e-a2c0-d3134eb64055
description: Crie relatórios com o Office 365 App segurança na nuvem que permitem que você entenda como pessoas da sua organização estiver usando o Office 365 e outros aplicativos.
ms.openlocfilehash: f801c70e839a62b5bbb5423ff5e7c513dd1f09b4
ms.sourcegitcommit: 2cf7f5bb282c971d33e00f65d9982a3f14aec74e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/27/2018
ms.locfileid: "26706295"
---
# <a name="create-app-discovery-reports-using-office-365-cloud-app-security"></a>Criar relatórios de descoberta de aplicativo usando o Office 365 Cloud App Security

Gerenciamento de segurança avançada do Office 365 agora é segurança de aplicativo de nuvem do Office 365.
  
|Avaliação * *\>**|Planejamento * *\>**|Implantação * *\>**|Utilização * * *|
|:-----|:-----|:-----|:-----|
|[Comece a avaliar](office-365-cas-overview.md) <br/> |[Começar a planejar](get-ready-for-office-365-cas.md) <br/> |[Começar a implantar](turn-on-office-365-cas.md) <br/> |Você está aqui!  <br/> [Próximas etapas](#next-steps) <br/> |
   
Segurança de aplicativo de nuvem do Office 365 ajuda administradores globais, os administradores de segurança e leitores de segurança percepção pessoas em uma organização estiver usando os serviços de nuvem. Por exemplo, você pode ver onde os usuários estão armazenando e colaborando em documentos e a quantidade de dados está sendo carregado para aplicativos ou serviços que estão fora do Office 365.
  
Para gerar um relatório de descoberta de aplicativo, você carregar seus arquivos de log do tráfego da web a partir de seus firewalls e proxies manualmente e, em seguida, a segurança de aplicativo de nuvem do Office 365 analisa e analisa esses arquivos para o seu relatório.
  
> [!NOTE]
> Você deve ser um administrador global, administrador de segurança ou leitor de segurança para executar as tarefas descritas neste artigo. Para saber mais, consulte [permissões no Office 365 Security &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md). 
  
## <a name="create-a-report-with-app-discovery"></a>Criar um relatório com a descoberta de aplicativo

Para criar um relatório de descoberta de aplicativo, você deve identificar a fonte de dados de fornecedor para os arquivos de log que você deseja ter analisado, selecione os arquivos de log e, em seguida, solicitar o relatório.
  
> [!NOTE]
> Use os arquivos de log do tráfego da web que incluem os períodos de tráfego para obter a melhor representação de uso em sua organização. 
  
1. Colete [logs de tráfego da web e fontes de dados para segurança de aplicativo de nuvem do Office 365](web-traffic-logs-and-data-sources-for-ocas.md).
    
2. Vá para [https://security.microsoft.com](https://security.microsoft.com) e entrar usando sua conta do trabalho ou da escola. 
    
3. Na segurança &amp; Centro de conformidade, escolha **alertas** \> **avançadas de gerenciar alertas**.
    
4. Escolha **vá para segurança de aplicativo do Office 365 nuvem**.
    
5. Escolha **descobrir** \> **Criar novo relatório**.
    
    ![No portal do Office 365 CAS, escolha Discover](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)
  
6. Especifique um nome e uma descrição para o seu relatório e, em seguida, selecione a fonte de dados de logs de tráfego da web na lista **fonte de dados** . 
    
    ![O CAS O365, escolha descobrir \> criar novo relatório](media/22e660f0-5eb2-49fa-9fea-f88a5809a07b.png)
  
    > [!NOTE]
    > Se uma fonte de dados que você deseja usar não estiver listada, você poderá solicitar a ser adicionado. Selecione **outra** **fonte**de dados e, em seguida, digite o nome da fonte de dados que você está tentando carregar. Vamos examinar o log e permitem que você saiba se podemos adicionar suporte para a fonte de dados que geraram a ele. 
  
7. Navegue até o local dos arquivos de log que você coletou e selecione os arquivos. Os arquivos de log devem ter sido gerados por fonte de dados que você escolheu para o relatório.
    
8. Clique em **criar** para iniciar o processo de criação do relatório. 
    
9. Para ver o status do relatório, clique em **Gerenciar relatórios de instantâneo**. Quando um relatório estiver pronto, você verá a opção **Exibir relatório** . 
    
## <a name="next-steps"></a>Próximas etapas

- [Revise e agir em alertas](review-office-365-cas-alerts.md)
    
- [Analisar descobertas de aplicativos do Office 365 Cloud App Security](review-app-discovery-findings-in-ocas.md)
    
- Revise suas [atividades de utilização para segurança de aplicativo de nuvem do Office 365](utilization-activities-for-ocas.md)
    


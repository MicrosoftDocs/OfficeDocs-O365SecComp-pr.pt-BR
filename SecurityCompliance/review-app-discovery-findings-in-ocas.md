---
title: Analisar descobertas de aplicativos do Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: aac65513-e75e-4c82-a668-9a6604dd9f9d
description: Analisar relatórios de descoberta de aplicativo no gerenciamento de segurança avançadas pode ajudá-lo a saber mais sobre como as pessoas na sua organização usam aplicativos na nuvem. Depois de criar relatórios de descoberta de aplicativo usando os arquivos de log de seus firewalls e proxies, revise os resultados no painel de descoberta do aplicativo.
ms.openlocfilehash: 6195c9aae7ae5e398ac555cc820de04dee05d4fd
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29603742"
---
# <a name="review-app-discovery-findings-in-office-365-cloud-app-security"></a>Analisar descobertas de aplicativos do Office 365 Cloud App Security
  
|Avaliação * *\>**|Planejamento * *\>**|Implantação * *\>**|Utilização * * *|
|:-----|:-----|:-----|:-----|
|[Comece a avaliar](office-365-cas-overview.md) <br/> |[Começar a planejar](get-ready-for-office-365-cas.md) <br/> |[Começar a implantar](turn-on-office-365-cas.md) <br/> |Você está aqui!  <br/> [Próximas etapas](#next-steps) <br/> |
   
O painel de descoberta de nuvem trabalha com logs de tráfego da web para fornecer informações detalhadas sobre o uso do aplicativo de nuvem da sua organização. Se você for um administrador global, administrador de segurança ou leitor de segurança e sua organização tenha [criado os relatórios de descoberta de aplicativo na segurança de aplicativo de nuvem do Office 365](create-app-discovery-reports-in-ocas.md), você pode usar o painel de descoberta de nuvem para percepção como as pessoas na sua organização estiver usando o Office 365 e outros aplicativos de nuvem. (O painel de descoberta de nuvem é também conhecido como descoberta de aplicativos de produtividade.)
  
 O painel de descoberta de nuvem permite exibir informações detalhadas sobre como as pessoas na sua organização estiver usando o Office 365 e outros aplicativos. 
  
![O painel de descoberta de nuvem foi atualizado](media/12712681-c0b3-4cb3-b7fd-2cf2ad4e825f.png)
     
## <a name="go-to-the-cloud-discovery-dashboard"></a>Vá para o painel de descoberta de nuvem

1. Vá para o portal de segurança de aplicativo de nuvem ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) e entrar.
    
2. Vá para **descobrir** \> **Painel de descoberta de nuvem**.
    
## <a name="see-your-top-users-ip-addresses-apps-and-risk-levels"></a>Veja os principais usuários, endereços IP, aplicativos e níveis de risco

O painel de descoberta de nuvem oferece uma visão geral de um resumo geral de aplicativos que são usados com o Office 365 em sua organização, qualquer open alertas, principais usuários e níveis de risco.
  
![Dashboaard da descoberta de nuvem](media/06696946-fbdf-4781-b5b8-2ac074fcb2a1.png)
  
1. Na guia do **painel** , examine o uso geral de aplicativo de nuvem em sua organização, na seção Visão geral na parte superior da tela. 
    
2. Consulte as **categorias do Office 365** para aplicativos que são usados em sua organização. 
    
3. Examinar o widget **Discovered apps** para ver o uso do Office 365 e outros aplicativos nesse modo de exibição. 
    
4. Examinar o widget **principais usuários** e **endereços IP de cima** para identificar aqueles que usam o Office 365 e aplicativos o máximo em sua organização em nuvem. 
    
5. Visualizar onde estão os aplicativos pessoas estão usando por localização geográfica, usando o mapa de **local de matrizes de aplicativos** . 
    
6. Acima da área de mapas, dê uma olhada na pontuação de risco dos aplicativos descobertos na visão geral de **níveis de risco** . Você pode examinar riscos pelo mesmo grupos e categorias que você usou na área **Discovered aplicativos** . Por exemplo, você pode ver a quantidade de tráfego em cada agrupamento é de aplicativos de risco baixa, média ou alta. 
    
## <a name="dive-deeper-into-the-information"></a>Se aprofundam nas informações

Você pode usar a descoberta de nuvem para dar uma olhada mais aprofundada em aplicativos, subdomínios, endereços IP e os usuários.
  
1. No painel descoberta de nuvem, escolha a guia de **Discovered aplicativos** . 
    
2. Use a seção filtros para exibir aplicativos pelo nome, categoria, nível de uso ou data da última Vista.
    
3. Na lista de resultados, passe o mouse por um nome de aplicativo para revelar o link **Exibir subdomínios** .<br/> ![Passe o mouse ao lado de um aplicativo para revelar um link para exibir detalhes do subdomínio](media/4a212215-8a2c-46fd-9ef9-89e4064658a6.png)<br/>Informações detalhadas sobre o aplicativo selecionado serão exibida.
    
4. Para exibir detalhes sobre os endereços IP, escolha a guia de **endereços IP** .<br/>![Descoberta de nuvem mostra informações detalhadas sobre endereços IP](media/0c742bf6-da9e-4d22-8656-a27a5007d5d5.png)<br/>Na lista de resultados, selecione um endereço IP individual para exibir informações mais detalhadas.
    
5. Para exibir detalhes sobre os usuários do Office 365 dentro da sua organização, escolha a guia de **usuários** .<br/>![Descoberta de nuvem - info de usuários](media/2d9c2d85-01e6-4057-8020-d9a68f26bbac.png)
  
## <a name="exclude-entities"></a>Excluir entidades

Você pode excluir determinados usuários do sistema ou endereços IP para focalizar em informações mais específicas.
  
1. Escolha **configurações** \> **configurações de descoberta de nuvem**.
    
2. Escolha **Excluir entidades**.
    
3. Escolha **usuários excluídos** ou **endereços IP excluídos**.
    
4. Especificar os usuários ou os endereços IP e, na caixa **comentários** , digite as informações sobre por que você está excluindo a esses usuários ou endereços IP. 
    
5. Escolha **Adicionar**.
    
## <a name="next-steps"></a>Próximas etapas

- [Revise e agir em alertas](review-office-365-cas-alerts.md)
    
- [Criar relatórios de descoberta de aplicativo](create-app-discovery-reports-in-ocas.md)
    
- Revise suas [atividades de utilização para segurança de aplicativo de nuvem do Office 365](utilization-activities-for-ocas.md)
    


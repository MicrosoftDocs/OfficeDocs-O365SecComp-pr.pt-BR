---
title: Analisar descobertas de aplicativos do Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: aac65513-e75e-4c82-a668-9a6604dd9f9d
description: ReVisando os relatórios de descoberta de aplicativos no Office 365 Cloud app Security pode ajudá-lo a saber mais sobre como as pessoas em sua organização usam aplicativos de nuvem. Depois de criar relatórios de descoberta de aplicativos usando arquivos de log de seus firewalls e proxies, revise os resultados no painel de descoberta de aplicativos.
ms.openlocfilehash: f50ad372450b2a1404829eeb6f6964c1d954dccd
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216251"
---
# <a name="review-app-discovery-findings-in-office-365-cloud-app-security"></a>Analisar descobertas de aplicativos do Office 365 Cloud App Security
  
|Avaliação * *\>**|Planejamento * *\>**|Implantação * *\>**|Utilização * * *|
|:-----|:-----|:-----|:-----|
|[Iniciar avaliação](office-365-cas-overview.md) <br/> |[Iniciar planejamento](get-ready-for-office-365-cas.md) <br/> |[Iniciar implantação](turn-on-office-365-cas.md) <br/> |Você está aqui!  <br/> [Próximas etapas](#next-steps) <br/> |
   
O painel de descoberta de nuvem funciona com os logs de tráfego da Web da sua organização para fornecer informações detalhadas sobre o uso do aplicativo na nuvem. Se você é um administrador global, administrador de segurança ou leitor de segurança e sua organização [criou relatórios de descoberta de aplicativos no Office 365 Cloud app Security](create-app-discovery-reports-in-ocas.md), você pode usar o painel de descoberta de nuvem para obter informações sobre como as pessoas em seu a organização está usando o Office 365 e outros aplicativos em nuvem. (O painel de descoberta de nuvem também é conhecido como descoberta de aplicativos de produtividade.)
  
 O painel de descoberta de nuvem permite que você exiba informações detalhadas sobre como as pessoas em sua organização estão usando o Office 365 e outros aplicativos. 
  
![O painel de descoberta de nuvem foi atualizado](media/12712681-c0b3-4cb3-b7fd-2cf2ad4e825f.png)
     
## <a name="go-to-the-cloud-discovery-dashboard"></a>Vá para o painel de descoberta de nuvem

1. Vá para o portal do Cloud app Security[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)() e entre.
    
2. Vá para **descobrir** \> **painel de descoberta de nuvem**.
    
## <a name="see-your-top-users-ip-addresses-apps-and-risk-levels"></a>Ver seus principais usuários, endereços IP, aplicativos e níveis de risco

O painel de descoberta de nuvem oferece uma visão geral dos aplicativos usados com o Office 365 em sua organização, quaisquer alertas abertos, principais usuários e níveis de risco.
  
![Dashboaard de descoberta de nuvem](media/06696946-fbdf-4781-b5b8-2ac074fcb2a1.png)
  
1. Na guia **painel** , examine o uso geral do aplicativo na nuvem em sua organização na seção visão geral na parte superior da tela. 
    
2. ConFira as **categorias do Office 365** para aplicativos usados em sua organização. 
    
3. Examine o widget **aplicativos** descobertos para ver o uso do Office 365 e outros aplicativos neste modo de exibição. 
    
4. Examine o widget **principais usuários** e **endereços IP principais** para identificar aqueles que usam o Office 365 e os aplicativos de nuvem mais em sua organização. 
    
5. Veja onde os aplicativos que as pessoas estão usando são por localização geográfica usando o mapa de **localização do centro de aplicativos** . 
    
6. Acima da área mapas, confira a pontuação de risco dos aplicativos detectados na visão geral dos **níveis de risco** . Você pode examinar riscos pelos mesmos grupos e categorias usados na área **aplicativos** descobertos. Por exemplo, você pode ver quanto tráfego em cada agrupamento é de aplicativos de alto, médio ou baixo risco. 
    
## <a name="dive-deeper-into-the-information"></a>Mergulhe mais fundo nas informações

Você pode usar a descoberta de nuvem para obter uma análise mais profunda de aplicativos, subdomínios, endereços IP e usuários.
  
1. No painel de descoberta de nuvem, escolha a guia **aplicativos** descobertos. 
    
2. Use a seção filtros para exibir os aplicativos por nome, categoria, nível de uso ou data da última exibição.
    
3. Na lista de resultados, passe o mouse por um nome de aplicativo para revelar o link de subdomínios de **exibição** .<br/> ![Focalize ao lado de um aplicativo para mostrar um link para exibir os detalhes do subdomínio](media/4a212215-8a2c-46fd-9ef9-89e4064658a6.png)<br/>Serão exibidas informações detalhadas sobre o aplicativo selecionado.
    
4. Para exibir detalhes sobre endereços IP, escolha a guia **endereços IP** .<br/>![A descoberta de nuvem mostra informações detalhadas sobre endereços IP](media/0c742bf6-da9e-4d22-8656-a27a5007d5d5.png)<br/>Na lista de resultados, selecione um endereço IP individual para exibir informações mais detalhadas.
    
5. Para exibir detalhes sobre os usuários do Office 365 dentro da sua organização, escolha a guia **usuários** .<br/>![Descoberta de nuvem-informações de usuários](media/2d9c2d85-01e6-4057-8020-d9a68f26bbac.png)
  
## <a name="exclude-entities"></a>Excluir entidades

Você pode excluir determinados usuários do sistema ou endereços IP para se concentrar em informações mais específicas.
  
1. Escolha **configurações** \> **descoberta de nuvem**.
    
2. Escolha **excluir entidades**.
    
3. Escolha **usuários excluídos** ou **endereços IP excluídos**.
    
4. Especifique os usuários ou endereços IP e, na caixa **comentários** , digite as informações sobre o motivo pelo qual você está excluindo os endereços IP ou usuários. 
    
5. Escolha **Adicionar**.
    
## <a name="next-steps"></a>Próximas etapas

- [ReVisar e executar ação em alertas](review-office-365-cas-alerts.md)
    
- [Criar relatórios de descoberta de aplicativos](create-app-discovery-reports-in-ocas.md)
    
- ReVisar suas [atividades de utilização do Office 365 Cloud app Security](utilization-activities-for-ocas.md)
    


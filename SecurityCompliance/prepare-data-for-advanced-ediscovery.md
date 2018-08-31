---
title: Preparar dados para a Descoberta Eletrônica Avançada do Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 2fb94c23-1846-4a0e-994d-da6d02445f15
description: 'Saiba como usar a segurança do Office 365 &amp; Centro de conformidade para preparar os dados do Office 365 para análise com eDiscovery avançadas do Office 365. '
ms.openlocfilehash: cf0c76b0c274121da435de7829c769abf5111cab
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524449"
---
# <a name="prepare-data-for-office-365-advanced-ediscovery"></a>Preparar dados para a Descoberta Eletrônica Avançada do Office 365

Este tópico descreve como carregar os resultados de uma pesquisa de conteúdo em um caso de eDiscovery avançado. 
  
> [!NOTE]
> EDiscovery Avançado requer um Office 365 E3 com o complemento de conformidade avançadas ou uma assinatura E5 para sua organização. Se você não tiver que plano e quiser tentar eDiscovery avançado, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
## <a name="step-1-prepare-office-365-data-for-advanced-ediscovery"></a>Etapa 1: Preparar os dados do Office 365 para eDiscovery avançado

Para analisar dados com eDiscovery avançado, você pode usar os resultados da pesquisa de conteúdo que você executa na segurança do Office 365 &amp; Centro de conformidade (listado na página **pesquisa de conteúdo** no Office 365 Security &amp; Centro de conformidade) ou uma pesquisa associado a um caso de descoberta eletrônica (listado na página **eDiscovery** na segurança &amp; Centro de conformidade). 
  
Para conhecer as etapas detalhadas sobre como preparar os resultados da pesquisa para análise no eDiscovery avançado, consulte [Prepare search results para eDiscovery avançadas do Office 365](prepare-search-results-for-advanced-ediscovery.md).
  
> [!NOTE]
> Se você tiver dados fora do Office 365 e quiser importá-lo para o Office 365 para que você possa preparar e analisá-los de eDiscovery avançado, um, consulte [Overview of importando arquivos PST para o Office 365](https://support.office.com/article/ba688e0a-0fcb-4bd7-8e57-2b669564ea84) e [dados de terceiros de arquivamento no Office 365](https://go.microsoft.com/fwlink/p/?linkid=716918). 
  
## <a name="step-2-load-search-result-data-in-to-a-case-in-advanced-ediscovery"></a>Etapa 2: Carregar pesquisa resultado dados na um caso de eDiscovery avançado

Depois de preparar os resultados da pesquisa na segurança &amp; Centro de conformidade para análise, a próxima etapa é carregar os resultados de pesquisa em um caso de eDiscovery avançado. Para obter informações mais detalhadas, consulte [executar o módulo de processo](run-the-process-module-in-advanced-ediscovery.md).
  
1. Vá para [https://protection.office.com](https://protection.office.com).
    
2. Entrar no Office 365 usando sua conta do trabalho ou da escola.
    
3. Na segurança &amp; Centro de conformidade, clique em **pesquisa &amp; investigação** \> **eDiscovery** para exibir a lista de ocorrências em sua organização. 
    
4. Clique em **Abrir** , ao lado do caso em que você deseja carregar dados no eDiscovery avançado. 
    
5. Na página **inicial** para o caso, clique em **Avançado de eDiscovery**. 
    
    ![Clique em Alternar para descoberta eletrônica avançada para abrir o caso no eDiscovery avançado](media/8e34ba23-62e3-4e68-a530-b6ece39b54be.png)
  
    A barra de progresso **Conectando-se a descoberta eletrônica avançada** é exibida. Quando você estiver conectado ao eDiscovery avançado, é exibida uma lista de contêineres na página configuração para o caso. 
    
    ![O caso é exibido no eDiscovery avançado](media/8036e152-70dc-4bb7-9379-61c1ed8326b4.png)
  
     Desses contêineres representam os resultados da pesquisa que você preparou para análise no eDiscovery Avançado na etapa 1. Observe que o nome do contêiner tem o mesmo nome que a pesquisa de conteúdo no caso de segurança &amp; Centro de conformidade. Os contêineres na lista são aqueles que você preparou. Se um usuário diferente preparado os resultados da pesquisa para a descoberta eletrônica avançada, os contêineres correspondentes não serão incluídos na lista. 
    
6. Para carregar os dados de resultado de pesquisa de um contêiner ao caso no eDiscovery avançada, selecione um contêiner e, em seguida, clique em **processar**.
    
Após os resultados de pesquisa da segurança &amp; Centro de conformidade são adicionados ao caso no eDiscovery avançada, a próxima etapa é usar as ferramentas no eDiscovery avançada para analisar e analisar os dados que são relevantes para o caso. 
  
## <a name="see-also"></a>Confira também

[Descoberta Eletrônica Avançada do Office 365](office-365-advanced-ediscovery.md)
  
[Configurar e casos de usuários](set-up-users-and-cases-in-advanced-ediscovery.md)
  
[Analisando dados maiusculas](analyze-case-data-with-advanced-ediscovery.md)
  
[Gerenciando a instalação de relevância](manage-relevance-setup-in-advanced-ediscovery.md)
  
[Usando o módulo de relevância](use-relevance-in-advanced-ediscovery.md)
  
[Exportando dados maiusculas](export-case-data-in-advanced-ediscovery.md)


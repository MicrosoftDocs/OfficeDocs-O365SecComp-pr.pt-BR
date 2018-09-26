---
title: Preparar resultados de pesquisa para Descoberta Eletrônica Avançada do Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 5/10/2017
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.CustomizeExportWithZoom
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid: MOE150
ms.assetid: 0b6fac2d-8627-4b05-9df0-03609db6248b
description: Saiba como preparar os resultados de uma pesquisa de conteúdo no Office 365 Security &amp; Centro de conformidade para análise adicional com a ferramenta de descoberta eletrônica avançado.
ms.openlocfilehash: f5b10ac7fcfa67f67618c936000832b9bdb7d533
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038304"
---
# <a name="prepare-search-results-for-office-365-advanced-ediscovery"></a>Preparar resultados de pesquisa para Descoberta Eletrônica Avançada do Office 365

Após uma pesquisa que está associado a um caso de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade é executado com êxito, você pode preparar os resultados da pesquisa para análise adicional com eDiscovery avançadas do Office 365, que permite que você analise grandes, dados não estruturados define e reduzem a quantidade de dados relevantes a um caso jurídico. Recursos de descoberta eletrônica avançada incluem:
  
- **Reconhecimento óptico de caracteres** - quando você prepara os resultados da pesquisa para eDiscovery avançada, a funcionalidade de reconhecimento óptico de caracteres (OCR) automaticamente extrai texto de imagens e inclui isso com os resultados da pesquisa que são carregados em para EDiscovery avançada para análise. OCR é suportado para arquivos flexível, anexos de email e imagens incorporadas. Isso permite que você aplique as capacidades analíticas de texto de eDiscovery avançado (perto duplicatas, email threading, temas e previsão de codificação) para o conteúdo de texto em arquivos de imagem. 
    
- **Detecção de quase duplicados** - permite que você estruturar sua análise de dados com mais eficiência, para que uma pessoa analisa um grupo de documentos semelhantes. Isso ajuda a impedir que vários revisores tenham que exibir diferentes versões do mesmo documento. 
    
- **Email threading** - o ajudará a identificar as mensagens exclusivas em um segmento de email para poder focalizar somente as novas informações em cada mensagem. Em um segmento de email, a segunda mensagem contém a mensagem primeira. Da mesma forma, as mensagens de posteriores contêm todas as mensagens anteriores. Email threading remove a necessidade de revisar todas as mensagens em sua totalidade em um segmento de email. 
    
- **Temas** - ajudá-lo a obter informações valiosas sobre seus dados além apenas estatísticas de pesquisa de palavra-chave. Temas ajudam investigações agrupando documentos relacionados, portanto, você pode examinar os documentos em contexto. Ao usar temas, você pode exibir os temas relacionados para um conjunto de documentos, determinar quaisquer sobreposição e, em seguida, identificar seções cruzadas de dados relacionados. 
    
- **Previsão de codificação** - lhe permite treinar o sistema no qual você está procurando, permitindo que você tomar decisões (sobre se algo é relevante ou não) em um conjunto pequeno de documentos. EDiscovery avançada aplica esse aprendizado (com base em sua orientação) quando analisando todos os documentos no conjunto de dados. Com base no que aprendizado, eDiscovery avançado oferece uma classificação de relevância para que você possa decidir quais documentos a serem analisados com base em qual documento são bem provável de ser relevante ao caso. 
    
- **Exportando dados para revisar os aplicativos** - você pode exportar dados de descoberta eletrônica avançada e o Office 365 depois de concluir sua análise e reduziu o conjunto de dados. O pacote de exportação inclui um arquivo CSV que contém as propriedades dos metadados de análise e o conteúdo exportado. Esse pacote de exportação, em seguida, pode ser importado para um aplicativo de revisão de descoberta eletrônica. 
    
## <a name="before-you-begin"></a>Antes de começar

- Para analisar dados de um usuário usando o eDiscovery avançado, o usuário (o de responsáveis dos dados) deve ser atribuído uma licença do Office 365 E5. Como alternativa, os usuários com uma licença do Office 365 E1 ou E3 podem ser atribuídos uma licença autônoma de eDiscovery avançado. Os administradores e oficiais de conformidade que estão atribuídos ao casos e usam o eDiscovery avançada para analisar dados não precisam de uma licença E5. 
    
- Você precisa ser uma administrador no Office 365 Security descoberta eletrônica ou uma gerente de descoberta eletrônica &amp; Centro de conformidade para preparar os resultados da pesquisa avançada de eDiscovery. Uma gerente de descoberta eletrônica é um membro do grupo de função de Gerenciador de descoberta eletrônica. Um eDiscovery administrador também é membro do grupo de função de gerente de descoberta eletrônica, mas foi atribuído privilégios de descoberta eletrônica adicionais. Para obter instruções sobre como atribuir permissões de administrador de descoberta eletrônica, consulte a etapa 1 em [casos de descoberta eletrônica no Centro de conformidade & segurança do Office 365](ediscovery-cases.md#step-1-assign-ediscovery-permissions-to-potential-case-members).
    
## <a name="step-1-prepare-search-results-for-advanced-ediscovery"></a>Etapa 1: Preparar resultados para eDiscovery avançada de pesquisa

Você pode preparar os resultados de uma pesquisa que está associado a um caso de eDiscovery. Ao preparar os resultados da pesquisa para a descoberta eletrônica avançada, os dados são carregados e temporariamente armazenados em uma área de armazenamento do Windows Azure exclusiva em nuvem da Microsoft. É nesse momento que a funcionalidade de OCR extrai o texto da imagens nos resultados da pesquisa. Em [etapa 2](#step-2-add-the-search-results-data-to-the-case-in-advanced-ediscovery), esse texto e a pesquisa de outra dados dos resultados são carregados ao caso no eDiscovery avançado.
  
1. No Centro de Conformidade e Segurança, clique em **Pesquisa e investigação** \> **Descoberta Eletrônica** para exibir a lista de casos na sua organização. 
    
2. Clique em **Abrir** , ao lado do caso em que você deseja preparar os resultados da pesquisa para análise no eDiscovery avançado. 
    
3. Na página **inicial** para o caso, clique em **Pesquisar**e, em seguida, selecione a pesquisa.
    
4. No painel de detalhes, **Analisar resultados com eDiscovery avançada**, clique em **Preparar resultados para análise**.
    
    > [!NOTE]
    > Se os resultados de pesquisa tiverem mais de sete dias, você será solicitado a atualizá-los. 
  
5. Na página **Preparar os resultados para análise**, faça o seguinte:  
    
    - Escolha preparar itens indexados, itens indexados e não indexados ou apenas itens indexados para análise no eDiscovery avançado.
    
    - Escolha se deseja incluir todas as versões de documentos encontrados no SharePoint que atendidos os critérios de pesquisa. Essa opção aparecerá somente se as fontes de conteúdo para a pesquisa inclui sites.
    
    - Especifique se deseja que uma mensagem de notificação enviada (ou copiou) para uma pessoa quando o processo de preparação é concluído e os dados estão prontos para ser processado no eDiscovery avançado.
    
6. Clique em **Preparar**.
    
    Os resultados da pesquisa são preparados para análise com eDiscovery avançado.
    
7. No painel de detalhes, clique em **Verificar status de preparação** para exibir informações sobre o processo de preparação. Quando o processo de preparação for concluído, você pode ir para o caso da eDiscovery avançada para processar os dados para análise. 
    
## <a name="step-2-add-the-search-results-data-to-the-case-in-advanced-ediscovery"></a>Etapa 2: Adicionar os dados dos resultados de pesquisa para o caso da eDiscovery avançado
<a name="step2"> </a>

Quando a preparação for concluída, a próxima etapa é ir para descoberta eletrônica avançada e carregar os dados dos resultados de pesquisa (que foram carregados para uma área de armazenamento do Azure em nuvem da Microsoft) para o caso da eDiscovery avançado. Explicado como anteriormente, para acessar o eDiscovery avançado, você precisa ser um administrador na segurança do eDiscovery &amp; Centro de conformidade ou um administrador no eDiscovery avançado.
  
> [!NOTE]
> O tempo que leva para os dados a partir de segurança &amp; Centro de conformidade esteja disponível para adicionar a um caso de eDiscovery avançado varia, dependendo do tamanho dos resultados da pesquisa de descoberta eletrônica. 
  
1. No Centro de Conformidade e Segurança, clique em **Pesquisa e investigação** \> **Descoberta Eletrônica** para exibir a lista de casos na sua organização. 
    
2. Clique em **Abrir** , ao lado do caso em que você deseja carregar dados no eDiscovery avançado. 
    
3. Na página **Início** do caso, clique em **Descoberta Eletrônica Avançada**. 
    
    ![Clique em Alternar para descoberta eletrônica avançada para abrir o caso no eDiscovery avançado](media/8e34ba23-62e3-4e68-a530-b6ece39b54be.png)
  
    A barra de progresso **Conectando-se a descoberta eletrônica avançada** é exibida. Quando você estiver conectado ao eDiscovery avançado, é exibida uma lista de contêineres na página configuração para o caso. 
    
    ![O caso é exibido no eDiscovery avançado](media/8036e152-70dc-4bb7-9379-61c1ed8326b4.png)
  
     Desses contêineres representam os resultados da pesquisa que você preparou para análise no eDiscovery Avançado na etapa 1. Observe que o nome do contêiner tem o mesmo nome que a pesquisa no caso de segurança &amp; Centro de conformidade. Os contêineres na lista são aqueles que você preparou. Se um usuário diferente preparado os resultados da pesquisa para a descoberta eletrônica avançada, os contêineres correspondentes não serão incluídos na lista. 
    
4. Para carregar os dados de resultado de pesquisa de um contêiner ao caso no eDiscovery avançada, selecione um contêiner e, em seguida, clique em **processar**.
    
## <a name="next-steps"></a>Próximas etapas

Após os resultados de uma descoberta eletrônica pesquisa são adicionados a um caso, a próxima etapa é usar as ferramentas de descoberta eletrônica avançadas para analisar os dados e identifique o conteúdo que está respondendo de forma a um caso jurídico específico. Para obter informações sobre como usar a descoberta eletrônica avançada, consulte [eDiscovery avançadas do Office 365](office-365-advanced-ediscovery.md).
  
## <a name="more-information"></a>Mais informações

Todas as mensagens de email criptografadas RMS que estão incluídas nos resultados da pesquisa serão descriptografadas quando prepará-los para análise no eDiscovery avançado. Essa capacidade de descriptografia está habilitada por padrão para membros do grupo de função de Gerenciador de descoberta eletrônica. Isso ocorre porque a função de gerenciamento do RMS descriptografar é atribuída a este grupo de função. Mantenha as seguintes coisas em mente sobre descriptografando mensagens de email:
  
- No momento, esse recurso de descriptografia não inclui conteúdo criptografado do SharePoint e OneDrive para sites corporativos. Somente as mensagens de email criptografadas RMS serão descriptografadas, quando você exportá-los.
    
- Se uma mensagem de email criptografadas RMS tiver um anexo (por exemplo, um documento ou outra mensagem de email) que também é criptografado, será descriptografada, somente a mensagem de email de nível superior.
    
- Se você precisar impedir que alguém descriptografando mensagens criptografadas por RMS ao preparar os resultados da pesquisa para análise no eDiscovery avançado, você precisará criar um grupo de função personalizada (copiando o grupo de função de Gerenciador de eDiscovery interna) e remova o RMS Descriptografe a função de gerenciamento do grupo de função personalizada. Em seguida, adicione a pessoa que você não deseja descriptografar mensagens como membro do grupo de função personalizada.

---
title: Introdução às diretivas de gerenciamento de informações
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/16/2014
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- WSU150
- SPO160
- OSU150
- MET150
ms.assetid: 63a0b501-ba59-44b7-a35c-999f3be057b2
description: Uma política de gerenciamento de informações é um conjunto de regras para um tipo de conteúdo. Informações de políticas de gerenciamento permitem que as organizações controle e controlar coisas como quanto tempo o conteúdo é mantido ou quais ações que os usuários podem levar com esse conteúdo. Políticas de gerenciamento de informações podem ajudar as organizações a conformidade com normas legais ou governamentais, ou eles podem impor simplesmente processos internos de negócios.
ms.openlocfilehash: 9ec64cd7e015acc6a7d8da324ba18cf74405cc71
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523951"
---
# <a name="introduction-to-information-management-policies"></a>Introdução às diretivas de gerenciamento de informações

Uma política de gerenciamento de informações é um conjunto de regras para um tipo de conteúdo. Informações de políticas de gerenciamento permitem que as organizações controle e controlar coisas como quanto tempo o conteúdo é mantido ou quais ações que os usuários podem levar com esse conteúdo. Políticas de gerenciamento de informações podem ajudar as organizações a conformidade com normas legais ou governamentais, ou eles podem impor simplesmente processos internos de negócios. 
  
Por exemplo, uma organização que deve seguir regulamentos do governo exigir que eles demonstram "adequadas controls" de seus demonstrativos financeiros pode criar informações de uma ou mais políticas de gerenciamento que Audite ações específicas na criação e processo de aprovação para todos os documentos relacionados a arquivamentos financeiros.
  
Para obter informações, consulte [criar e aplicar políticas de gerenciamento de informações](create-info-mgmt-policies.md).
  
## <a name="features-of-information-management-policies"></a>Recursos de diretivas de gerenciamento de informações
<a name="__top"> </a>

Há quatro categorias básicas dos recursos de política predefinidos que as organizações podem usar individualmente ou em combinação para gerenciar conteúdo e processos. 
  
![Tipos de políticas de conteúdo](media/19fcb8a3-974b-40d3-a13f-b76088d122f8.png)
  
O recurso de política de auditoria ajuda as organizações a analisar como seus sistemas de gerenciamento de conteúdo são usados pelo log de eventos e operações que são executadas em documentos e itens de lista. Você pode configurar o recurso de política de auditoria para registrar eventos, como quando um documento ou item for editado, exibidos, check-in, check-out, excluída, ou tem suas permissões alterados. Todas as informações de auditoria são armazenadas em um log de auditoria único no servidor, e os administradores de sites podem executar relatórios nele. 
  
O recurso de política de expiração ajuda as organizações excluir ou remover o conteúdo desatualizado de seus sites de maneira consistente e rastreável. Isso ajuda você a gerenciar o custo e os riscos associados à retenção de conteúdo desatualizado. Você pode configurar uma política de expiração para especificar que certos tipos de conteúdo expiram em uma determinada data ou em um período de tempo depois que o documento foi criado ou modificado pela última vez.
  
As organizações também podem criar e implantar os recursos de política personalizada para atender às necessidades específicas. Por exemplo, uma organização de fabricação talvez queira definir uma política de gerenciamento de informações para todos os documentos de especificação de design de produto de rascunho que proíbe os usuários de impressão cópias desses documentos em impressoras não seguras. Para definir esse tipo de política de gerenciamento de informações, você pode criar e implantar um recurso de diretiva de restrição de impressão que pode ser adicionado para a política de gerenciamento de informações relevantes para o tipo de conteúdo de especificação do produto design.
  
## <a name="locations-to-use-an-information-management-policy"></a>Locais para usar uma política de gerenciamento de informações
<a name="__toc340213528"> </a>

Para implementar uma política de gerenciamento de informações, você deve adicioná-lo para uma lista, biblioteca ou tipo de conteúdo em um site. O local onde você cria ou adiciona uma política de gerenciamento de informações afeta como amplamente a política se aplica ou como amplamente pode ser usado. É possível:
  
 **Criar uma política de conjunto de sites e, em seguida, adicione essa política a um tipo de conteúdo, lista ou biblioteca** Você pode criar uma política de conjunto de sites na lista de políticas no site de nível superior de um conjunto de sites. Depois de criar uma política de conjunto de sites, você poderá exportá-lo para que os administradores de outros conjuntos de sites podem importá-lo para sua lista de políticas. Criar uma política de conjunto de sites exportável permite padronizar as políticas de gerenciamento de informações entre os sites em sua organização. 
  
Quando você adicionar uma política de conjunto de sites a um tipo de conteúdo de site e uma instância desse tipo de conteúdo de site é adicionada a uma lista ou biblioteca, o proprietário dessa lista ou biblioteca não pode modificar a política de conjunto de sites para a lista ou biblioteca. Adicionando uma política de conjunto de sites a um tipo de conteúdo de site é uma boa maneira de garantir nesse site políticas de coleção são impostos em cada nível da hierarquia do seu site.
  
![Link de modelo de política de tipo de conteúdo na página Configurações do Site](media/26d3466a-23ec-443f-88f0-2aaff38e992b.png)
  
 **Criar uma política de gerenciamento de informações para um tipo de conteúdo de site na Galeria de tipos de conteúdo do Site de nível superior do site e em seguida, adicione esse tipo de conteúdo a um ou mais listas ou bibliotecas** Você pode também criar uma política de gerenciamento de informações diretamente para um tipo de conteúdo de site e associe uma instância desse tipo de conteúdo de site com várias listas ou bibliotecas. Se você criar uma política de gerenciamento de informações dessa maneira, cada item no conjunto de sites do tipo de conteúdo ou um tipo de conteúdo que herda a partir desse tipo de conteúdo tem a política. No entanto, se você criar uma política de gerenciamento de informações diretamente para um tipo de conteúdo do site, é mais difícil reutilizar essa política de gerenciamento de informações em outros conjuntos de sites, porque as diretivas criadas dessa forma não podem ser exportadas. 
  
![Link de tipos de conteúdo de site na página Configurações do Site](media/6f6fa51f-15d7-4782-b06f-a7b36e874cd3.png)
  
![Link de política de gerenciamento de informações na página Configurações de um tipo de conteúdo de site](media/15d83a34-6c8f-4b6e-b6ee-e9b0a70cbb4b.png)
  
Observação para controlar quais políticas são usadas em um conjunto de sites, os administradores de conjunto de sites podem desabilitar a capacidade de definir os recursos de política diretamente em um tipo de conteúdo. Quando essa restrição está em vigor, os usuários que criar tipos de conteúdo são limitados à seleção políticas de lista de políticas de conjunto de sites.
  
 **Criar uma política de gerenciamento de informações para uma lista ou biblioteca** Se sua organização precisar aplicar uma política de gerenciamento de informações específicas para um conjunto muito limitado do conteúdo, você pode criar uma política de gerenciamento de informações que se aplica somente a uma lista individual ou a biblioteca. Esse método de criação de uma política de gerenciamento de informações é o menos flexível, porque a política se aplica somente a único local, e não podem ser exportado ou reutilizada para outros locais. No entanto, em alguns casos, você pode precisar criar políticas de gerenciamento de informações exclusivas com capacidade limitada de aplicação para atender a situações específicas. 
  
![Link de políticas de gerenciamento de informações na página de configurações de biblioteca de documentos](media/9fa6d366-6aab-49e1-a05c-898ac6f536e6.png)
  
Observações 
  
Você pode criar uma política de gerenciamento de informações para uma lista ou biblioteca somente se dessa lista ou biblioteca não oferece suporte a vários tipos de conteúdo. Se uma lista ou biblioteca oferece suporte a vários tipos de conteúdo, você precisará definir uma política de gerenciamento de informações para cada tipo de conteúdo de lista individuais que está associado essa lista ou biblioteca. (Instâncias de um tipo de conteúdo de site que estão associadas uma lista ou biblioteca específica são conhecidas como tipos de conteúdo de lista).
  
Para controlar quais políticas são usadas em um conjunto de sites, os administradores de conjunto de sites podem desabilitar a capacidade de definir os recursos de política diretamente em uma lista ou biblioteca. Quando essa restrição está em vigor, os usuários que gerenciam a listas ou bibliotecas são limitados à seleção políticas de lista de políticas de conjunto de sites.
  
[Uma política de gerenciamento de informações é um conjunto de regras para um tipo de conteúdo. Informações de políticas de gerenciamento permitem que as organizações controle e controlar coisas como quanto tempo o conteúdo é mantido ou quais ações que os usuários podem levar com esse conteúdo. Políticas de gerenciamento de informações podem ajudar as organizações a conformidade com normas legais ou governamentais, ou eles podem impor simplesmente processos internos de negócios. Por exemplo, uma organização que deve seguir regulamentos do governo exigir que eles demonstram "adequadas controls" de seus demonstrativos financeiros pode criar informações de uma ou mais políticas de gerenciamento que Audite ações específicas na criação e processo de aprovação para todos os documentos relacionados a arquivamentos financeiros. Para obter instruções informações, consulte Criar e aplicar políticas de gerenciamento de informações.](intro-to-info-mgmt-policies.md#__top)
  


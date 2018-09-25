---
title: Visão geral das políticas de exclusão de documentos
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/12/2017
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
ms.assetid: 55e8d858-f278-482b-a198-2e62d6a2e6e5
description: Sua organização pode ser necessário para reter os documentos por um período de tempo devido à conformidade, legal, ou outros requisitos de negócios. No entanto, se sua organização mantém documentos mais que o necessário, você cria riscos legais desnecessários. Com uma política de exclusão de documentos, você proativamente pode reduzir riscos, a exclusão de documentos em um site após um período de tempo específico — por exemplo, você pode excluir documentos em OneDrive dos usuários para negócios sites cinco anos depois que os documentos foram criados.
ms.openlocfilehash: 7af818dd7d9dd87eb671bdd86ef03e0b5dead1e2
ms.sourcegitcommit: ede6230c2df398dc0a633e8f32ee0bfede0d5142
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/25/2018
ms.locfileid: "25002664"
---
# <a name="overview-of-document-deletion-policies"></a>Visão geral das políticas de exclusão de documentos

> [!IMPORTANT]
> Mais adiante, recomendamos que você use uma política de retenção ou etiquetas criadas na segurança &amp; Centro de conformidade, em vez de uma política de exclusão de documentos. Políticas de exclusão de documentos continuará inserido lado a lado com políticas de retenção, mas se você precisar reter ou excluir conteúdo em qualquer lugar no Office 365, é recomendável que você use uma política de retenção. Para obter mais informações, consulte [usar uma política de retenção em vez desses recursos](retention-policies.md#use-a-retention-policy-instead-of-these-features).
  
Sua organização pode ser necessário para reter os documentos por um período de tempo devido à conformidade, legal, ou outros requisitos de negócios. No entanto, se sua organização mantém documentos mais que o necessário, você cria riscos legais desnecessários. Com uma política de exclusão de documentos, você proativamente pode reduzir riscos, a exclusão de documentos em um site após um período de tempo específico — por exemplo, você pode excluir documentos em OneDrive dos usuários para negócios sites cinco anos depois que os documentos foram criados.
  
Políticas de exclusão de documentos são poderosas ainda flexível — por exemplo, você pode:
  
- Permitir que os proprietários de sites escolham políticas a partir das políticas que você criar e gerenciar centralmente. Também pode permitir que os proprietários de sites recusem aplicar uma política se decidirem que ela não se aplica aos seus conteúdos.
    
- Aplicar uma única política obrigatória a todos os sites de um conjunto de sites, como sites do OneDrive for Business, ou aplicar uma política a todos os conjuntos de sites criados a partir de um modelo específico de conjunto de sites, como o modelo Site da Equipe.
    
- Fornecer uma política padrão com uma regra padrão que será aplicada automaticamente, sem exigir qualquer ação por parte dos proprietários de site.
    
- Criar uma política que inclua várias regras de exclusão que possam ser escolhidas por um proprietário de site.
    
Criar e gerenciar políticas de exclusão de documentos usando o Centro de política de exclusão de documento, que pode ser encontrado em **retenção** no Office 365 Security &amp; Centro de conformidade. Como alternativa, você pode criar o centro da diretiva manualmente, [Criando o conjunto de sites](https://go.microsoft.com/fwlink/p/?LinkID=404342) e escolhendo o **Centro de conformidade de diretiva** na guia **empresa** . Cada locatário pode ter apenas um centro de política de exclusão de documentos, e ele será criado automaticamente se iniciar a partir de segurança &amp; Centro de conformidade. 
  
![Página inicial do Centro de Políticas de Exclusão de Documentos](media/IP-Document-Deletion-Policy-Center-home-page.png)
  
## <a name="when-to-use-document-deletion-policies"></a>Quando usar as políticas de exclusão de documentos

Além das políticas de exclusão de documentos, o Office 365 fornece estas políticas de retenção para conteúdos de sites:
  
- [Gerenciamento de registros](https://go.microsoft.com/fwlink/p/?LinkID=404250)
    
- [Políticas de gerenciamento de informações para tipos de conteúdo, listas e bibliotecas](https://go.microsoft.com/fwlink/p/?LinkID=404239)
    
- [Políticas de site](https://go.microsoft.com/fwlink/p/?LinkID=404242)
    
Cada tipo de política funciona melhor para um tipo específico de site ou dados. Por exemplo, a sua organização pode ter um site altamente estruturado que use tipos de conteúdo, como um site financeiro para contratos ou uma base de dados de conhecimento para artigos. Nesse caso, você pode usar políticas de tipo de conteúdo. Ou a sua organização pode ter que reter documentos legais, em cujo caso você poderá usar tipos de conteúdo e uma Central de Registros para implementar um planejamento de arquivos.
  
Políticas de exclusão de documentos não substituem registros informações ou gerenciamento de políticas de gerenciamento, que funcionam melhor com dados estruturados e tipos de conteúdo. Em vez disso, você deve usar políticas de exclusão de documentos quando você precisa gerenciar amplamente a exclusão automática de dados não estruturados como OneDrive para sites corporativos e sites de equipe.
  
![Diagrama mostrando opções de retenção para conteúdos de site](media/IP-Retention-policies-for-site-content.png)
  
Se você aplicar uma política de exclusão de documentos a um site que já usa políticas de tipo de conteúdo ou de gerenciamento de informações para uma lista ou biblioteca, essas políticas serão ignoradas enquanto a política de exclusão de documentos estiver em vigor. Isso significa que você deverá fazer um plano para que um site use somente políticas feitas para conteúdos estruturados ou não estruturados, e não ambos. Para obter mais informações sobre como as políticas de exclusão de documentos substituem outras políticas, consulte [Apply or remove a document deletion policy for a site](apply-or-remove-a-document-deletion-policy-for-a-site.md).
  
Ao contrário de outras políticas, as políticas de exclusão de documentos funcionam somente em bibliotecas de documentos, e não em listas.
  
## <a name="deletion-policies-and-rules"></a>Políticas e regras de exclusão

Uma política de exclusão de documentos contém uma ou mais regras de exclusão que especificam:
  
- O período de tempo até a exclusão.
    
- Se a data de exclusão será calculada com base em quando o documento foi criado ou na data da última alteração.
    
- Se deseja excluir o documento permanentemente ou para a Lixeira.
    
Se uma política contiver mais do que uma regra, os proprietários de sites podem selecionar a regra que melhor se aplique ao seu conteúdo.
  
![Nova página de regra de exclusão](media/IP-New-deletion-rule.png)
  
## <a name="policies-and-assignments"></a>Políticas e atribuições

Depois de criar uma política de exclusão de documentos, você pode atribuí-lo a um modelo de conjunto de sites — por exemplo, você pode atribuir uma política para o OneDrive para o modelo de negócios, para que ele inclua cada OneDrive site de usuário. Quando você atribuir uma política a um modelo de conjunto de sites, isso se aplica a todos os conjuntos de sites que já criados a partir desse modelo, além de quaisquer conjuntos de sites criados a partir desse modelo no futuro.
  
![Escolha uma página modelo exibindo a opção do OneDrive](media/IP-Choose-a-template.png)
  
Você pode ainda atribuir uma política a um conjunto específico de sites, fazer isso substitui quaisquer políticas que tenham sido atribuídas a esse modelo de conjunto de sites. Por exemplo, você pode atribuir políticas ao modelo Site de Equipe, mas depois substituí-las aplicando um conjunto de políticas diferente a um conjunto de sites específico criado a partir daquele modelo.
  
### <a name="one-mandatory-policy-or-several-policies-to-choose-from"></a>Uma política obrigatória ou várias políticas à sua escolha

Quando você atribui uma política, pode escolher torná-la obrigatória, para que apenas essa política possa ser atribuída e para que seja aplicada a todos os sites no conjunto de sites. Os proprietários de sites podem optar por não usar uma política obrigatória, o que significa que os documentos no site estarão inevitavelmente sujeitos à política de exclusão.
  
Em vez de tornar uma única política obrigatória, você também pode atribuir várias políticas a um conjunto de sites, o que permite que cada proprietário de site escolha qual política aplicar a seu site, ou ainda cancelar todas as políticas. Por exemplo, você pode criar uma política para documentos corporativos gerais e outra política para documentos financeiros que tenham agendas de retenção diferentes. Um proprietário de site saberá melhor que conteúdo o seu site contém e, consequentemente, qual política de exclusão de documentos aplicar. Cada site pode ter somente uma política aplicada a ele.
  
### <a name="one-rule-or-several-rules-to-choose-from"></a>Uma regra ou várias regras à sua escolha

Por sua vez, cada diretiva pode conter várias regras — por exemplo, uma política de exclusão de documentos gerais de negócios pode ter duas regras:
  
- Documentos que não necessitem de retenção com base em obrigações legais ou necessidades recorrentes da empresa não deverão ser retidos por mais de um ano de criação.
    
- Os documentos necessários para uso ativo e recorrente da empresa, que sejam precisos por mais do que um ano, não deverão ser retidos por mais do que três anos a partir da sua data de criação.
    
Um proprietário de site pode determinar que o seu site contém comercial geral documentos, selecione essa política de exclusão e, em seguida, selecione a regra apropriada da diretiva. Você só pode selecionar uma regra da política que atualmente é aplicada ao site (e não de qualquer política) e a regra será aplicada a todas as bibliotecas de documentos no site.
  
## <a name="the-relationship-of-site-collections-policies-and-rules"></a>A relação entre conjuntos de sites, políticas e regras

O relacionamento básico é o seguinte:
  
Um conjunto de sites ou de um modelo de conjunto de sites pode ter uma ou mais políticas atribuídas a ele e cada uma dessas políticas pode ter uma ou mais regras. Entretanto, pode haver apenas uma diretiva que está ativa por site e pode haver apenas uma regra de exclusão que está ativa a qualquer momento para as bibliotecas dentro do site.
  
![Diagrama mostrando a relação entre as políticas](media/IP-Two-policies-four-rules.png)
  
## <a name="document-deletion-policies-are-inherited"></a>As políticas de exclusão de documentos são herdadas

Como as permissões, a navegação e muitos outros recursos de sites, as políticas de exclusão de documentos são herdadas. Um proprietário pode selecionar uma política de exclusão de documentos para seu site e, consequentemente, todos os subsites herdarão a política do site principal. O proprietário de um subsite pode interromper a herança selecionando uma combinação diferente de políticas e regras, desse modo a política será aplicada a todos os subsites até que a herança seja interrompida novamente.
  
## <a name="assigning-document-deletion-policies-for-the-first-time"></a>Atribuir políticas de exclusão de documentos pela primeira vez

É importante entender que o período de tempo especificado para um documento exclusão diretiva significa que o tempo desde que o documento foi criado ou modificado, não ao tempo desde que a política foi atribuída. Por exemplo, você pode criar uma política de exclusão de documentos que exclui permanentemente documentos dois anos após terem sido criados e, em seguida, essa política seja atribuída a um modelo de conjunto de sites do qual vários conjuntos de sites criados quatro ou cinco anos atrás. Nesse caso, é provável que os conjuntos de sites existente contêm vários documentos que já estão mais antigos do que os dois anos especificados pela política de exclusão — isso significa que uma grande quantidade de conteúdo será excluída logo depois de atribuir a política de exclusão de documentos para o primeiro tempo.
  
Quando você atribui uma política pela primeira vez, todos os documentos no site são avaliados, e são excluídos se atenderem aos critérios. Isto se aplica a todos os documentos existentes, e não somente aos novos documentos criados desde que a política foi atribuída. E lembre-se de que o período de tempo é relativo à idade de cada documento, e não ao tempo passado desde que a política foi atribuída pela primeira vez.
  
Portanto, antes de adicionar uma política a um site pela primeira vez, você deverá primeiro considerar a idade dos conteúdos existentes e de que modo a política poderá afetá-los. Você também poderá informar os proprietários de sites sobre a nova política antes de atribuí-la, para que eles tenham tempo para avaliar o possível impacto.
  
## <a name="time-lag-for-propagating-policies"></a>Intervalo de tempo para propagação de políticas

Após atribuir políticas a um conjunto de sites, os proprietários de sites podem usar o link **Políticas de exclusão de documentos** na página **Configurações do Site** para ver e aplicar as políticas disponíveis para o site. 
  
O link **Políticas de exclusão de documentos** não aparecerá, a menos que as políticas foram atribuídas ao conjunto de sites. Além disso, o link não aparece imediatamente após a políticas que tiverem sido atribuídas a site — pode demorar até 24 horas de quando as políticas são atribuídas para quando o link **Políticas de exclusão de documento** é exibido. 
  
## <a name="permissions"></a>Permissões

Os membros da sua equipe de conformidade que utilizam o Centro de Política de Exclusão de Documento precisam ter permissões para o centro de políticas e para os conjuntos de sites a que as políticas serão aplicadas. Recomendamos que você:
  
1. Criar um grupo de segurança que contém todos os usuários da Central de política de exclusão de documentos — mais provável sua equipe de gerenciamento de políticas de conformidade. Consulte [Grupos de segurança Manage Mail-Enabled](https://go.microsoft.com/fwlink/p/?LinkID=404345) para obter mais informações. 
    
2. Na Central de política de exclusão de documentos, atribua os conjunto de sites de permissões de proprietário ao grupo de segurança. Consulte as [permissões para os administradores de conjunto de sites](https://go.microsoft.com/fwlink/p/?LinkID=404346) para obter mais informações. 
    
3. Em cada conjunto de sites a que você precisa atribuir políticas de exclusão de documentos, atribua permissões de proprietário de conjunto de sites ao grupo de segurança.
    
## <a name="how-document-deletion-policies-work-with-hold-policies"></a>Como as políticas de exclusão de documentos funcionam com políticas de retenção

Uma política de retenção garante que todo o conteúdo seja preservado por um período específico de tempo, enquanto que uma política de exclusão de documentos garante que todo o conteúdo seja excluído após um período específico de tempo.
  
Se você deseja reter documentos por um período fixo de tempo, pode utilizar uma política de retenção com uma política de exclusão. Por exemplo, pode reter documentos por três anos após eles terem sido modificados e, depois, configurar uma política de exclusão para excluir esses documentos três anos após a última modificação.
  
Observe que uma política de exclusão não substitui uma retenção. Se um site estiver em retenção e uma política de exclusão de documentos excluir um documento, ele será preservado na Biblioteca de Retenções para Preservação exatamente como se tivesse sido excluído manualmente.
  
## <a name="see-also"></a>Confira também

[Aplicar ou remover uma política de exclusão de documentos de um site](apply-or-remove-a-document-deletion-policy-for-a-site.md)

[Criar uma política de exclusão de documentos](create-a-document-deletion-policy.md)



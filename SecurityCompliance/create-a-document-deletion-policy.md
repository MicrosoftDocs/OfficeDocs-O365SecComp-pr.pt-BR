---
title: Criar uma política de exclusão de documentos
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- SPO160
ms.assetid: 41b2ed73-eb8d-4429-945e-a8197894585a
description: As organizações frequentemente são obrigadas a manter documentos por um determinado período devido a regulamentações de conformidade, legais ou outras. No entanto, reter os documentos por mais tempo do que o necessário poderá expor a organização a riscos legais.
ms.openlocfilehash: 115e4d7df93d81e7ee5a860f20a00d9cb175f927
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "23013995"
---
# <a name="create-a-document-deletion-policy"></a>Criar uma política de exclusão de documentos

> [!IMPORTANT]
> Mais adiante, recomendamos que você use uma política de retenção ou etiquetas criadas na segurança &amp; Centro de conformidade, em vez de uma política de exclusão de documentos. Políticas de exclusão de documentos continuará inserido lado a lado com políticas de retenção, mas se você precisar reter ou excluir conteúdo em qualquer lugar no Office 365, é recomendável que você use uma política de retenção. Para obter mais informações, consulte [usar uma política de retenção em vez desses recursos](retention-policies.md#use-a-retention-policy-instead-of-these-features). 
  
As organizações frequentemente são obrigadas a manter documentos por um determinado período devido a regulamentações de conformidade, legais ou outras. No entanto, reter os documentos por mais tempo do que o necessário poderá expor a organização a riscos legais.
  
Com uma política de exclusão de documentos, você proativamente pode reduzir riscos, a exclusão de documentos em um site após um período de tempo específico — por exemplo, você pode excluir documentos em OneDrive dos usuários para negócios sites cinco anos depois que os documentos foram criados. 
  
Depois de criar uma política de exclusão de documentos, você poderá atribuí-la a um modelo de conjunto de sites, de forma que a política esteja disponível para todos os conjuntos de sites criados a partir desse modelo. Você pode ainda atribuir uma política a um conjunto específico de sites, que substitui qualquer política que possa ter sido atribuída ao modelo para esse conjunto de sites.
  
![Página inicial do Centro de Políticas de Exclusão de Documentos](media/IP-Document-Deletion-Policy-Center-home-page.png)
  
## <a name="policy-templates"></a>Modelos de política

Você pode criar uma política de exclusão do documento do zero ou pode usar uma das políticas de amostra. A Central de Política de Conformidade inclui políticas de amostra que você pode usar como estão, ou como ponto de partida e, em seguida, renomeá-las ou modificá-las.
  
![Amostra de políticas de exclusão de documentos](media/IP-Sample-deletion-policies.png)
  
## <a name="examples-of-how-to-use-document-deletion-policies"></a>Exemplos

Um conjunto de sites ou de um modelo de conjunto de sites pode ter um mais diretivas atribuídas a ele e cada uma dessas políticas pode ter uma ou mais regras. Entretanto, pode haver apenas uma diretiva que está ativa por site e pode haver apenas uma regra de exclusão que está ativa a qualquer momento para as bibliotecas dentro do site.
  
![Diagrama mostrando a relação entre as políticas](media/IP-Two-policies-four-rules.png)
  
Além disso, você pode selecionar uma política como obrigatória ou padrão, e poderá selecionar uma regra de exclusão como uma regra padrão: 
  
- **Política obrigatória** Quando uma diretiva é marcada como obrigatória, apenas uma diretiva pode ser atribuída ao conjunto de sites ou modelo. A diretiva deve ser marcada como padrão e será aplicada a todos os sites. Os proprietários de sites não podem recusar a política.
    
- **Política padrão** Quando uma política for definida como padrão, a política é automaticamente ativa em todos os sites que foi atribuída com nenhuma ação necessária pelo proprietário do site.
    
- **Regra padrão** Quando uma regra de exclusão for definida como padrão, ela será automaticamente aplicada a todas as bibliotecas nos sites que usam a política.
    
Os exemplos a seguir explicam quando você pode querer usar uma política obrigatória ou políticas e regras padrão.
  
### <a name="example-1-apply-a-single-policy-with-a-single-rule-to-a-site-collection-template"></a>Exemplo 1: aplicar uma política única com uma regra única a um modelo de conjunto de sites

Talvez você queira impor uma política de exclusão de documentos a uma ampla variedade de conteúdos não estruturados, como todos os sites do OneDrive for Business ou todos os sites de equipe. Se quiser garantir que uma única política de exclusão de documentos esteja ativa em todos os sites criados a partir de um modelo de conjunto de sites, você pode:
  
1. Criar uma única política com uma rúnica regra de exclusão padrão.
    
2. Definir a política como obrigatória e padrão.
    
3. Atribuir a política a um modelo de conjunto de sites.
    
Neste exemplo, a regra de exclusão padrão será aplicada a todas as bibliotecas em todos os conjuntos de sites criados a partir do modelo, e os proprietários do site não poderão recusar a política. Essa é a maneira mais simples de impor de forma ampla e rígida uma política de exclusão de documentos.
  
![Diagrama mostrando uma única política obrigatória](media/IP-Example-1-doc-deletion-policies.png)
  
### <a name="example-2-apply-a-single-policy-with-several-rules-to-a-site-collection-template"></a>Exemplo 2: Aplicar uma única política com várias regras a um modelo de conjunto de sites

Os proprietários de site sabem melhor qual é o tipo de conteúdo de seus sites e, portanto, talvez você opte por permitir que os proprietários selecionem a regra de exclusão que se aplique melhor ao site deles. Talvez também queira permitir que os proprietários do site recusem completamente uma política.
  
Ao mesmo tempo, você ainda pode criar e gerenciar centralmente as políticas. Também é possível selecionar uma política e uma regra como o padrão, de forma que uma política esteja sempre em vigor até o proprietário do site escolha uma diferente ou a recuse. Se desejar fornecer essa flexibilidade a proprietários do site, você pode:
  
1. Criar uma única política com várias regras de exclusão e definir uma regra como padrão.
    
2. Definir a política como a política padrão.
    
3. Atribuir a política a um modelo de conjunto de sites.
    
Os proprietários do site podem selecionar uma das regras de exclusão alternativas, recusar a política ou fazer nada e ficarem sujeitos à política e à regra padrão.
  
![Diagrama mostrando uma única política com diversas regras](media/IP-Example-2-doc-deletion-policies.png)
  
### <a name="example-3-apply-several-policies-with-one-or-more-rules-to-a-site-collection"></a>Exemplo 3: aplicar várias políticas com uma ou mais regras para um conjunto de sites

Este exemplo oferece a flexibilidade máxima a proprietários de sites, porque eles terão várias opções de políticas e, após a seleção de uma política, terão opções de várias regras. Uma política e uma regra estão definidas como padrão, de forma que uma política esteja sempre em vigor até que o proprietário do site escolha uma diferente ou a recuse. Observe que se você não definir uma política e uma regra como o padrão, então nenhuma política ou regra estará ativa para as bibliotecas de documentos no site até que o proprietário do site tome uma ação para selecioná-las e aplicá-las.
  
Ao contrário dos dois exemplos anteriores, essas políticas são atribuídas a um conjunto de sites específico e não ao modelo de conjunto de sites. Isso significa que as políticas poderão ser ajustadas mais especificamente para o conteúdo de um conjunto de sites específico.
  
Regras e políticas são herdadas. Os proprietários do site podem selecionar uma política e uma regra para seu site, e todos os subsites herdarão a política do site principal. Entretanto, um proprietário de um subsite poderá interromper a herança selecionando uma política e uma regra diferentes que, por sua vez, será aplicada a todos os subsites até a herança ser interrompida novamente.
  
Para configurar este cenário, você pode:
  
1. Criar várias políticas que contenham uma ou mais regras cada uma.
    
2. Definir uma política e uma regra como o padrão.
    
3. Atribuir as políticas a um conjunto de sites específico.
    
Além disso, as políticas e regras são ajustadas a um conjunto de sites específico, onde proprietários do site podem interromper a herança selecionando a política e a regra que melhor se aplique ao site.
  
![Diagrama mostrando diversas políticas e regras](media/IP-Example-3-doc-deletion-policies.png)
  
## <a name="create-a-document-deletion-policy"></a>Criar uma política de exclusão de documentos

1. No 365Security Office &amp; Centro de conformidade, navegue até **gerenciamento de dados** \> **retenção**. Em **Excluir**, clique em **Gerenciar políticas de exclusão de documentos para o SharePoint Online e o OneDrive for Business**. Centro de política de exclusão do documento é aberto em uma nova guia de navegador.
    
    Na primeira vez que você navega a partir de segurança &amp; Centro de conformidade para o Centro de política de exclusão de documento, o centro da diretiva é criado automaticamente para você. Como alternativa, você pode criar manualmente o centro da diretiva [Criando o conjunto de sites](http://go.microsoft.com/fwlink/p/?LinkID=404342) e escolhendo o **Centro de conformidade de diretiva** na guia **empresa** . 
    
2. Escolha **políticas de exclusão**.
    
    ![Opção Políticas de Exclusão](media/IP-Deletion-Policies-option.png)
  
3. Escolha **novo item**.
    
4. Insira um nome de política e uma descrição. Os proprietários do site podem estar selecionando uma política para o site deles com base nesse nome e descrição, portanto inclua informações suficientes para que eles escolham a política correta.
    
5. Para criar uma regra, escolha **Novo**.
    
6. Insira um nome e escolha estas opções:
    
  - Escolha se a regra será permanentemente excluir documentos ou excluí-los para a Lixeira. A Lixeira fornece uma rede de segurança de segundo estágio antes de um item é excluído permanentemente de um site. Para obter mais informações sobre a Lixeira, consulte [Esvaziar a Lixeira ou restaurar seus arquivos](http://go.microsoft.com/fwlink/p/?LinkID=404348).
    
  - Escolha se a data de exclusão será calculada a partir da data em que um documento foi criado ou modificado pela última vez.
    
  - Insira um número de dias, meses ou anos como o período após o qual um documento será excluído.
    
  - Escolha se a regra será uma regra padrão. A primeira regra criada será automaticamente definida como a regra padrão. Uma regra padrão será automaticamente aplicada a todas as bibliotecas nos sites que usam a política.
    
![Nova página de regra de exclusão](media/IP-New-deletion-rule.png)
  
7. Clique em **Salvar**.
    
8. Crie regras adicionais se quiser que proprietários do site sejam capazes de escolher regras diferentes para aplicarem ao site deles. A regra padrão, se houver, será aplicada se o proprietário do site não executar nenhuma ação.
    
9. Para remover uma regra de uma política, selecione a regra, clique em **Excluir**e, em seguida, clique em **Okey**.
    
    > [!NOTE]
    > Se você excluir uma regra e a diretiva não contiver uma regra padrão, então nenhuma regra estará em vigor para essa política — em outras palavras, não há documentos serão excluídos. 
  
![Confirmar remoção de regra de mensagem de política](media/IP-Remove-rule-from-policy-message.png)
  
## <a name="assign-the-document-deletion-policy-to-a-site-collection-template"></a>Atribuir a política de exclusão de documentos a um modelo de conjunto de sites

Atribuindo uma política a um modelo de conjunto de sites, você disponibiliza a política para todos os conjuntos de sites criados a partir desse modelo, incluindo conjuntos de sites existentes e conjuntos de sites criados no futuro.
  
É importante entender que o período de tempo especificado para um documento exclusão diretiva significa que o tempo desde que o documento foi criado ou modificado, não ao tempo desde que a política foi atribuída. Quando você atribui a política pela primeira vez, todos os documentos no site são avaliados e, se eles atendam aos critérios, elas serão excluídas. Isso se aplica a todos os documentos existentes, não apenas novos documentos criados desde que a política foi atribuída.
  
1. Na segurança &amp; Centro de conformidade, navegue até **gerenciamento de dados** \> **retenção**. Em **Excluir**, clique em **Gerenciar políticas de exclusão de documentos para o SharePoint Online e o OneDrive for Business**. Centro de política de exclusão do documento é aberto em uma nova guia de navegador.
    
2. Escolha **Atribuições de políticas para modelos**.
    
    ![Atribuição de Políticas para opção de Modelos](media/IP-Policy-Assignments-for-Templates-option.png)
  
3. Escolha **novo item**.
    
4. Siga um destes procedimentos:
    
  - Para atribuir a política a um modelo de conjunto de sites, como o modelo Site da Equipe, selecione **Atribuir ao modelo de conjunto de sites** e escolha o modelo de conjunto de sites.
    
  - Para atribuir a política a Onedrive dos usuários for Business, escolha **atribuir ao OneDrive for Business modelo**, realçado abaixo.
    
    > [!NOTE]
    > Quando você atribuir uma política a um modelo de conjunto de sites, essa política estará disponível a conjuntos de sites existentes criados a partir desse modelo e para conjuntos de sites criados no futuro. 
  
![Escolha uma página modelo exibindo a opção do OneDrive](media/IP-Choose-a-template.png)
  
5. Clique em **Salvar**.
    
    > [!NOTE]
    > Cada modelo pode ter apenas um conjunto de políticas atribuídas a ela. Se você vir um erro dizendo que este modelo já tem políticas atribuídas a ela, escolha **Cancelar** \> **atribuir ao conjunto de sites** no painel de navegação esquerdo \> selecione um conjunto de sites para exibir e gerenciar o conjunto de diretivas que já estão atribuído. 
  
6. Escolha **Gerenciar políticas atribuídas**, selecione as diretivas que você deseja atribuir e, em seguida, escolha se uma política é a política padrão. Quando você definir uma política padrão, todos os sites atribuídos à política automaticamente têm a política ativa com nenhuma ação necessária pelo proprietário do site.
    
    ![Adicione e gerencie páginas de políticas](media/IP-Add-and-manage-policies-page.png)
  
7. Clique em **Salvar**.
    
8. Se quiser impor a política a todos os sites sem permitir que os proprietários do site a recusem, escolha **Marcar política como obrigatória**. Quando uma política for marcada como obrigatória, somente uma única política poderá ser atribuída ao modelo de conjunto de sites. A política também deve ser marcada como padrão.
    
    Se essa opção estiver esmaecida, escolha **Gerenciar políticas atribuídas** e verifique se pelo menos uma política foi atribuída e definida como padrão. 
    
9. Clique em **Salvar**.
    
## <a name="assign-the-document-deletion-policy-to-a-site-collection"></a>Atribuir a política de exclusão de documentos a um conjunto de sites

Ao atribuir uma política a um conjunto de sites específico, você disponibilizará a política somente àquele conjunto de sites específico. Isso significa que você poderá ajustar melhor as políticas ao conteúdo no conjunto de sites. Além disso, políticas atribuídas a um conjunto de sites específico substituirão todas as políticas atribuídas ao modelo para aquele conjunto de sites. Por exemplo, uma política atribuída ao conjunto de sites Departamento de Vendas (criado a partir do modelo Site da Equipe) substituirá qualquer política atribuída ao modelo Site da Equipe.
  
É importante entender que o período de tempo especificado para um documento exclusão diretiva significa que o tempo desde que o documento foi criado ou modificado, não ao tempo desde que a política foi atribuída. Quando você atribui a política pela primeira vez, todos os documentos no site são avaliados e, se eles atendam aos critérios, elas serão excluídas. Isso se aplica a todos os documentos existentes, não apenas novos documentos criados desde que a política foi atribuída.
  
1. Na segurança &amp; Centro de conformidade, navegue até **gerenciamento de dados** \> **retenção**. Em **Excluir**, escolha **Gerenciar políticas de exclusão de documentos para o SharePoint Online e o OneDrive for Business**. Centro de política de exclusão do documento é aberto em uma nova guia de navegador.
    
2. Escolha **Atribuições de políticas para conjuntos de sites**.
    
    ![Atribuições de Políticas para opções de Conjuntos de Sites](media/IP-Policy-Assignments-for-Site-Collections-option.png)
  
3. Escolha **novo item**.
    
4. Selecione **Escolher um conjunto de sites**. Pesquise o conjunto de sites por nome ou URL, selecione o conjunto de sites e clique em **Salvar**.
    
    > [!NOTE]
    > Cada conjunto de sites pode ter apenas um conjunto de políticas atribuídas a ela. Se você vir um erro dizendo que este conjunto de sites já tem políticas atribuídas a ela, escolha **Cancelar** \> **atribuir ao conjunto de sites** e selecione um conjunto de sites para exibir e gerenciar o conjunto de diretivas que já estão atribuídos. 
  
![Escolha uma página de conjuntos de sites](media/IP-Choose-a-site-collection-page.png)
  
5. Escolha **Gerenciar políticas atribuídas**, selecione as diretivas que você deseja atribuir e, em seguida, escolha se uma política é a política padrão. Quando você definir uma política padrão, todos os sites atribuídos à política automaticamente têm a política ativa com nenhuma ação necessária pelo proprietário do site.
    
    ![Adicione e gerencie páginas de políticas](media/IP-Add-and-manage-policies-page.png)
  
6. Clique em **Salvar**.
    
7. Se quiser impor a política a todos os sites sem permitir que os proprietários do site a recusem, escolha **Marcar política como obrigatória**. Quando uma política for marcada como obrigatória, somente uma única política poderá ser atribuída ao conjunto de sites. A política também deve ser marcada como padrão.
    
    Se essa opção estiver esmaecida, escolha **Gerenciar políticas atribuídas** e verifique se pelo menos uma política foi atribuída e definida como padrão. 
    
8. Clique em **Salvar**.
    
## <a name="delete-a-policy-assignment"></a>Excluir uma atribuição de política

Quando você excluir uma atribuição, as políticas atribuídas não se aplicarão mais a qualquer site do conjunto de sites ou do modelo de conjunto de sites.
  
1. Na segurança &amp; Centro de conformidade, navegue até **gerenciamento de dados** \> **retenção**. Em **Excluir**, escolha **Gerenciar políticas de exclusão de documentos para o SharePoint Online e o OneDrive for Business**. Centro de política de exclusão do documento é aberto em uma nova guia de navegador.
    
2. Escolha uma destas opções **Atribuições de políticas para modelos** ou **Atribuições de políticas para conjuntos de sites**.
    
3. Selecione o item de atribuição e clique em **Excluir Item**.
    
    ![Exclua o comando Item para atribuição de política](media/IP-Delete-policy-assignment.png)
  
## <a name="delete-a-policy"></a>Excluir uma política

Você não pode excluir uma política que está em uso. Antes de excluir uma política, você precisará primeiro excluir todas as atribuições para conjuntos de sites e modelos de conjunto de sites que incluem a essa política — consulte a seção anterior.
  
1. Na segurança &amp; Centro de conformidade \> escolha **gerenciamento de dados** \> de **retenção** no painel de navegação esquerdo \> em **Excluir** \> **exclusão de documentos de gerenciar políticas para o SharePoint Online e OneDrive para negócios**. Centro de política de exclusão do documento é aberto em uma nova guia de navegador.
    
2. Escolha * * políticas de exclusão * *.
    
    ![Opção Políticas de Exclusão](media/IP-Deletion-Policies-option.png)
  
3. Selecione a política.
    
4. Na faixa de opções \> guia **itens** \> **Remover política**.
    
    ![Botão Remover Política na Faixa de Opções](media/IP-Remove-Policy-button-on-Ribbon.png)
  
5. Se a política estiver em uso, você será solicitado se deseja remover a diretiva de todos os conjuntos de sites onde ele está sendo usado. Se você tiver certeza, escolha **Okey**.
    
    ![Exclua a mensagem de confirmação de política](media/IP-Delete-policy-confirmation.png)
  
## <a name="see-also"></a>Confira também

[Visão geral das políticas de exclusão de documentos](document-deletion-policies.md)

[Aplicar ou remover uma política de exclusão de documentos de um site](apply-or-remove-a-document-deletion-policy-for-a-site.md)
 


---
title: Colocar uma caixa de correio em Retenção de Litígio
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/18/2016
ms.audience: End User
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid: ''
ms.assetid: adee4621-3626-4aec-aa53-00b35ff0d0b0
description: 'Colocar uma caixa de correio em Retenção de Litígio também preserva todo o conteúdo da caixa de correio, incluindo itens excluídos e versões originais de itens modificados. '
ms.openlocfilehash: b2d2a60fddb51aa310d01a765c1ebbbf127ecd19
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296974"
---
# <a name="place-a-mailbox-on-litigation-hold"></a>Colocar uma caixa de correio em Retenção de Litígio
 
Colocar uma caixa de correio em Retenção de Litígio também preserva todo o conteúdo da caixa de correio, incluindo itens excluídos e versões originais de itens modificados. Ao colocar a caixa de correio de um usuário em Retenção de Litígio, o conteúdo na caixa de correio de arquivo morto do usuário (se habilitada) também é colocado em retenção. Itens excluídos e modificados são preservados por um determinado período, ou até você remover a caixa de correio da Retenção de Litígio. Todos os itens da caixa de correio são retornados em uma pesquisa de [In-Place eDiscovery](http://technet.microsoft.com/library/6377cb7a-3416-4e15-8571-c45d2160fc6f.aspx). 
  
> [!IMPORTANT]
> A retenção de litígio preserva os itens na pasta itens recuperáveis na caixa de correio do usuário. Dependendo do número e do tamanho dos itens excluídos ou modificados, o tamanho da pasta itens recuperáveis da caixa de correio pode aumentar rapidamente. A pasta itens recuperáveis é configurada com uma cota alta por padrão. No Exchange Online, essa cota é aumentada automaticamente quando você coloca uma caixa de correio em retenção de litígio. No Exchange Server 2013, recomendamos que você monitore caixas de correio que são colocadas em retenção de litígio semanal para garantir que elas não atinjam os limites das cotas de itens recuperáveis. 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>O que você precisa saber antes de começar?
<a name="sectionSection0"> </a>

- Tempo estimado para conclusão: 5 minutos
    
- A configuração de Retenção de Litígio pode demorar até 60 minutos para entrar em vigor.
    
- Você precisa receber permissões antes de executar este procedimento ou procedimentos. Para ver de que permissões você precisa, consulte o entrada "bloqueio in-loco" no tópico [Messaging Policy and Compliance Permissions](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) . 
    
- Para colocar uma caixa de correio do Exchange Online em retenção de litígio, ela deve ser atribuída a uma licença do Exchange Online (plano 2). Se uma licença do Exchange Online (plano 1) for atribuída a uma caixa de correio, você precisará atribuí-la a uma licença de arquivamento do Exchange Online separada para colocá-la em espera.
    
- Conforme explicado anteriormente, quando você coloca uma retenção de litígio na caixa de correio de um usuário, o conteúdo da caixa de correio de arquivo morto do usuário também é colocado em espera. Se você colocar uma retenção de litígio em uma caixa de correio principal no local em uma implantação híbrida do Exchange, a caixa de correio de arquivo morto baseado na nuvem (se habilitada) também será colocada em espera.
    
- No Exchange Online, a cota da pasta itens recuperáveis é aumentada automaticamente para 100 GB quando você coloca uma caixa de correio em retenção de litígio. O tamanho padrão dessa pasta é de 30 GB.
    
- A retenção de litígio preserva itens excluídos e também preserva as versões originais de itens modificados até que a retenção seja removida. Opcionalmente, você pode especificar uma duração de retenção, que preserva um item de caixa de correio para o período de duração especificado. Se você especificar um período de duração de retenção, ele é calculado a partir da data em que uma mensagem é recebida ou de um item de caixa de correio é criado. Para preservar itens que atendam aos critérios especificados, use um bloqueio in-loco para criar uma retenção baseada em consulta. Para obter detalhes, consulte [criar ou remover um bloqueio in-loco](http://technet.microsoft.com/library/9d5d8d37-a053-4830-9cb1-6e1ede25e963.aspx).
    
- Para usar o Shell para colocar uma caixa de correio do Exchange Online em espera, você precisa usar o PowerShell do Exchange Online. Para obter mais informações, consulte [conectar-se ao Exchange Online usando o PowerShell remoto](http://technet.microsoft.com/library/c8bea338-6c1a-4bdf-8de0-7895d427ee5b.aspx).
    
- Não há suporte para colocar uma Retenção de Litígio em uma caixa de correio de pasta pública. Você precisa usar o Bloqueio In-loco para colocar uma retenção em pastas públicas.
    
## <a name="use-the-eac-to-place-a-mailbox-on-litigation-hold"></a>Usar o EAC para colocar uma caixa de correio em retenção de litígio
<a name="sectionSection1"> </a>

1. Acesse **Destinatários** \> **Caixas de Correio**.
    
2. Na lista de caixas de correio de usuários, clique na caixa de correio que você deseja colocar em retenção de litígio e, **** ![em seguida,](media/ITPro-EAC-EditIcon.gif)clique em Editar ícone de edição.
    
3. Na página de propriedades da caixa de correio, clique em **recursos da caixa de correio.**
    
4. Em **Retenção de Litígio: Desativado**, clique em **Habilitar** para colocar a caixa de correio em Retenção de Litígio. 
    
5. Na página **de Litígio**, insira as seguintes informações opcionais. 
    
  - **Duração da retenção de litígio (dias)** Use esta caixa para especificar por quanto tempo os itens da caixa de correio devem ser mantidos quando esta estiver em Retenção de Litígio. A duração é calculada a partir da data em que um item de caixa de correio é recebido ou criado. Se você deixar esta caixa em branco, os itens serão mantidos indefinidamente ou até que a retenção seja removida. Use dias para especificar a duração. 
    
  - **Observação** Use esta caixa para informar ao usuário que sua caixa de correio está em retenção de litígio. A observação aparecerá na caixa de correio do usuário se estiver usando o Outlook 2010 ou posterior. 
    
  - **URL** Use esta caixa para direcionar o usuário para um site para obter mais informações sobre a retenção de litígio. Essa URL aparece na caixa de correio do usuário se estiver usando o Outlook 2010 ou posterior. 
    
6. Clique em **Salvar** na página **Retenção de Litígio** e, em seguida, clique em **Salvar** na página de propriedades da caixa de correio. 
  
## <a name="use-the-shell-to-place-a-mailbox-on-litigation-hold-indefinitely"></a>Usar o Shell para colocar uma caixa de correio em Retenção de Litígio indefinidamente
<a name="sectionSection2"> </a>

Este exemplo coloca a caixa de correio bsuneja@contoso.com em Retenção de Litígio. Os itens na caixa de correio serão retidos indefinidamente ou até que a retenção seja removida.
  
```
Set-Mailbox bsuneja@contoso.com -LitigationHoldEnabled $true
```

> [!NOTE]
> Quando você coloca uma caixa de correio em retenção de litígio indefinidamente (ao não especificar um período de duração), o valor da propriedade  _LitigationHoldDuration_ é definido como  `Unlimited`. 
  
## <a name="use-the-shell-to-place-a-mailbox-on-litigation-hold-and-preserve-items-for-a-specified-duration"></a>Usar o Shell para colocar uma caixa de correio em Retenção de Litígio e preservar itens por um período específico
<a name="sectionSection3"> </a>

Este exemplo coloca a caixa de correio bsuneja@contoso.com em Retenção de Litígio e preserva itens por 2555 dias (aproximadamente sete anos). 
  
```
Set-Mailbox bsuneja@contoso.com -LitigationHoldEnabled $true -LitigationHoldDuration 2555
```

## <a name="use-the-shell-to-place-all-mailboxes-on-litigation-hold-for-a-specified-duration"></a>Usar o Shell para colocar todas as caixas de correio em Retenção de Litígio por um período específico
<a name="sectionSection4"> </a>

A sua organização pode exigir que todos os dados de caixas de correio sejam preservados durante um período específico. Antes de colocar todas as caixas de correio de uma organização em Retenção de Litígio, considere o seguinte:
  
Este exemplo coloca todas as caixas de correio de usuários na organização em Retenção de Litígio por um ano (365 dias).
  
```
Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | Set-Mailbox -LitigationHoldEnabled $true -LitigationHoldDuration 365
```

O exemplo usa o cmdlet [Get-Mailbox](http://technet.microsoft.com/library/8a5a6eb9-4a75-47f9-ae3b-a3ba251cf9a8.aspx)para recuperar todas as caixas de correio na organização, especifica um filtro de destinatários para incluir todas as caixas de correio de usuários e, então, envia essa lista ao cmdlet [Set-Mailbox](http://technet.microsoft.com/library/a0d413b9-d949-4df6-ba96-ac0906dedae2.aspx) para ativar a Retenção de Litígio e definir a duração da retenção.  
  
Para aplicar uma retenção indefinida a todas as caixas de correio de usuários, execute o comando anterior, mas não inclua o parâmetro  _LitigationHoldDuration_. 
  
Consulte a seção [Mais informações](#moreinfo.md) para obter exemplos de como usar outras propriedades de destinatários em um filtro para incluir ou excluir uma ou mais caixas de correio. 
  
## <a name="use-the-shell-to-remove-a-mailbox-from-litigation-hold"></a>Usar o Shell para remover a Retenção de Litígio de uma caixa de correio 
<a name="sectionSection5"> </a>

Este exemplo remove a Retenção de Litígio da caixa de correio bsuneja@contoso.com.
  
```
Set-Mailbox bsuneja@contoso.com -LitigationHoldEnabled $false
```

M
## <a name="how-do-you-know-this-worked"></a>Como saber se funcionou?
<a name="sectionSection6"> </a>

Para verificar se você aplicou com sucesso a Retenção de Litígio em uma caixa de correio, faça um dos seguintes:
  
- No EAC:
    
1. Acesse **Destinatários** \> **Caixas de Correio**.
    
2. Na lista de caixas de correio de usuários, clique na caixa de correio para a qual você deseja verificar as configurações de retenção de **** ![litígio e clique](media/ITPro-EAC-EditIcon.gif)em Editar ícone de edição.
    
3. Na página de propriedades da caixa de correio, clique em **recursos da caixa de correio.**
    
4. Em **Retenção de Litígio**, verifique se a retenção está habilitada.
    
5. Clique em **Exibir detalhes** para verificar quando a caixa de correio foi colocada em retenção de litígio e por quem. Você também pode verificar ou alterar os valores nas caixas opcionais **Duração da retenção de litígio (dias)**, **Observação** e **URL**. 
    
- No Shell, execute um destes comandos:
    
  ```
  Get-Mailbox <name of mailbox> | FL LitigationHold*
  ```

    ou
    
  ```
  Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | FL Name,LitigationHold*
  ```

    Se uma caixa de correio é colocada em Retenção de Litígio indefinidamente, o valor da propriedade  _LitigationHoldDuration_ é definido como  `Unlimited`.
    
## <a name="more-information"></a>Mais informações
<a name="moreinfo"> </a>

- Se sua organização exige que todos os dados da caixa de correio sejam preservados por um período específico de tempo, considere o seguinte antes de colocar todas as caixas de correio da organização em retenção de litígio.
    
  - Quando você usa o comando anterior para colocar uma retenção em todas as caixas de correio em uma organização (ou um subconjunto de caixas de correio que correspondem a um filtro de destinatário especificado) somente caixas de correio que existem no momento em que você executar o comando são colocadas em retenção. Se você criar novas caixas de correio posteriormente, execute o comando mais uma vez para colocá-las em retenção. Caso crie novas caixas de correio com frequência, você pode executar o comando como uma tarefa agendada com a frequência necessária.
    
  - Colocar todas as caixas de correio em retenção de litígio pode impactar significativamente os tamanhos da caixa de correio. Em uma organização do Exchange Server 2013, planeje o armazenamento adequado para atender aos requisitos de preservação da sua organização.
    
  - A pasta Itens Recuperáveis tem seu próprio limite de armazenamento, portanto, os itens na pasta não contam para o limite de armazenamento da caixa de correio. Conforme explicado anteriormente, preservar os dados de caixa de correio por um longo período de tempo resultará no crescimento da pasta itens recuperáveis na caixa de correio de um usuário e no arquivo morto. Para acomodar esse aumento no Exchange Online, a cota da pasta itens recuperáveis é aumentada automaticamente de 30 GB para 100 GB quando você coloca uma caixa de correio em retenção de litígio. 
    
    No Exchange Server 2013, o limite de armazenamento padrão para a pasta itens recuperáveis também é de 30 GB. Recomendamos que você monitore periodicamente o tamanho dessa pasta para garantir que ela não alcance o limite. Para obter mais informações, consulte [pasta itens recuperáveis](http://technet.microsoft.com/library/efc48fb4-2ed8-4d05-93af-f3505fbc389d.aspx).
    
- O comando anterior coloca uma retenção em todas as caixas de correio usando um filtro de destinatário que retorna todas as caixas de correio. Você pode usar outras propriedades de destinatário para obter uma lista de caixas de correio específicas, que você pode, então, enviar ao cmdlet **Set-Mailbox** para colocar uma Retenção de Litígio nessas caixas de correio. 
    
    Eis alguns exemplos de usar os cmdlets **Get-Mailbox** e **Get-Recipient** para obter um subconjunto de caixas de correio com base em propriedades de usuário ou de caixa de correio comuns. Esses exemplos supõem que as propriedades de caixa de correio relevantes (como  _CustomAttributeN_ ou  _Department_) foram preenchidas.
    
  ```
  Get-Mailbox -RecipientTypeDetails UserMailbox -ResultSize unlimited -Filter 'CustomAttribute15 -eq "OneYearLitigationHold"'
  ```

  ```
  Get-Recipient -RecipientTypeDetails UserMailbox -ResultSize unlimited -Filter 'Department -eq "HR"'
  ```

  ```
  Get-Recipient -RecipientTypeDetails UserMailbox -ResultSize unlimited -Filter 'PostalCode -eq "98052"'
  ```

  ```
  Get-Recipient -RecipientTypeDetails UserMailbox -ResultSize unlimited -Filter 'StateOrProvince -eq "WA"'
  ```

  ```
  Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -ne "DiscoveryMailbox"}
  ```

    Você pode usar outras propriedades de caixa de correio em um filtro para incluir ou excluir caixas de correio. Para saber mais, confira [Filterable Properties for the -Filter Parameter](http://technet.microsoft.com/library/b02b0005-2fb6-4bc2-8815-305259fa5432.aspx).
    


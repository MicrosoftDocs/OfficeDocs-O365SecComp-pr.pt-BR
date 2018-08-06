---
title: 'Executar relatório do grupo de funções de administrador no EOP '
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 23b47b57-0eec-46a3-a03b-366ea014ab31
description: Quando um administrador adiciona ou remove membros dos grupos de função de administrador, o Microsoft Proteção do Exchange Online (EOP) registra cada ocorrência.
ms.openlocfilehash: 49311faa4ee54fafa1c05a2314ed2f9d74cbe5a5
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027198"
---
# <a name="run-an-administrator-role-group-report-in-eop"></a>Executar relatório do grupo de funções de administrador no EOP 

 Quando um administrador adiciona ou remove membros dos grupos de função de administrador, o Microsoft Proteção do Exchange Online (EOP) registra cada ocorrência. Quando você executa um relatório de grupo de funções de administrador no Centro de administração do Exchange, as entradas são exibidas como resultados de pesquisa e incluem os grupos de função afetados, quem e quando alterou a associação do grupo de função, e quais atualizações de associação foram feitas. Use esse relatório para monitorar as alterações nas permissões administrativas atribuídas aos usuários da sua organização.
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>O que você precisa saber antes de começar?

- Tempo estimado para conclusão: 2 minutos
    
- Para executar este procedimento ou estes procedimentos, você precisa receber permissões. Para ver de que permissões você precisa, consulte o Seção "Relatórios" do tópico [Permissões de recurso no EOP](feature-permissions-in-eop.md). 
    
- Para informações sobre atalhos de teclado que possam se aplicar aos procedimentos neste tópico, consulte **Atalhos de teclado no Centro de administração do Exchange**.
    
> [!TIP]
> Está enfrentando problemas? Peça ajuda nos fóruns do Exchange. Visite os fóruns em: [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), ou [Proteção do Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=285351). 
  
## <a name="use-the-eac-to-run-an-administrator-role-group-report"></a>Usar o EAC para executar o relatório de grupo de funções de administrador

Execute o relatório de grupo de funções de administrador para encontrar as alterações nos grupos de função de gerenciamento em sua organização dentro de um período específico.
  
1. No EAC, navegue até **Gerenciamento de conformidade** \> **Auditoria** e escolha **Executar o relatório do grupo de funções do administrador**.
    
2. Escolha a **Data de início** e a **Data de término**. Por padrão, o relatório procura alterações feitas nos grupos de funções do administrador nas duas últimas semanas.
    
3. Para exibir as alterações de um grupo de funções específico, clique em **Selecionar grupos de função**. Selecione o grupo de função (ou grupos) na caixa de diálogo subsequente e clique em **OK**. Você também pode deixar o campo em branco para encontrar todos os grupos de função alterados.
    
4. Clique em **Pesquisar**.
    
Se quaisquer alterações forem encontradas usando os critérios especificados, elas aparecerão no painel de resultados. Clique em um grupo de função nos resultados da pesquisa para ver as alterações no painel de detalhes.
  
## <a name="how-do-you-know-this-worked"></a>Como saber se funcionou?

Se você executou com sucesso um relatório de grupo de funções do administrador, os grupos de funções que foram alterados dentro do intervalo de datas serão exibidos no painel de resultados da pesquisa. Se não houver resultados, nenhuma alteração nos grupos de funções será executada dentro do intervalo de datas especificado. Se julgar que deveria haver resultados, altere o intervalo de dados e execute novamente o relatório.
  
## <a name="monitor-changes-to-role-group-membership"></a>Monitorar alterações na associação de grupo de funções

Quando os membros são adicionados ou removidos de um grupo de funções, os resultados da pesquisa exibidos no painel de detalhes indicam que a associação de grupo de funções foi atualizada e lista os membros atuais. Os resultados não informam explicitamente qual usuário foi adicionado ou removido.
  
Para determinar se um usuário foi adicionado ou removido, você terá que comparar duas entradas separadas no relatório. Por exemplo, vamos observar as entradas de log a seguir do grupo de funções de **HelpDesk**: 
  
 **27/01/2013 16h43**
  
 **Administrador**
  
 **Membros atualizados: Administrator;annb,florencef;pilarp**
  
 **06/02/2013 10h09**
  
 **Administrador**
  
 **Membros atualizados: Administrator;annb;florencef;pilarp;tonip**
  
 **19/02/2013 14h12**
  
 **Administrador**
  
 **Membros atualizados: Administrator;annb;florencef;tonip**
  
Nesse exemplo, a conta de usuário Administrador fez as seguintes alterações:
  
- Em 02/06/2013, ela adicionou o usuário tonip.
    
- Em 19/02/2013, ela removeu o usuário pilarp.
    


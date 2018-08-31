---
title: Exclusão de dados on-line do Exchange Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: Como flexível e grave exclusões de dados são tratadas em Exchange Online.
ms.openlocfilehash: 3a17b09e9c21ae309e00bcb0ddc0b51b93478bc1
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523906"
---
# <a name="exchange-online-data-deletion-in-office-365"></a>Exclusão de dados on-line do Exchange no Office 365
Em Exchange Online, existem dois tipos de exclusões: suaves exclusões e exclusões de disco rígidas. Isso se aplica aos itens dentro de uma caixa de correio e caixas de correio.

## <a name="soft-deleted-and-hard-deleted-mailboxes"></a>Caixas de correio excluída e disco rígido excluído
Uma caixa de correio do usuário excluída é uma caixa de correio que tenha sido excluída usando o Centro de administração do Office 365 ou o cmdlet Remove-Mailbox e ainda tiver ficado da Lixeira do Azure Active Directory para menos de 30 dias. Uma caixa de correio pode se tornar excluída em qualquer uma das seguintes maneiras:
- A caixa de correio de usuário associada do Azure Active Directory conta de usuário é excluída (o objeto de usuário está fora do escopo ou no contêiner recycle bin).
- Conta de usuário da caixa de correio de usuário associada Azure Active Directory tiver sido excluída por disco rígido, mas a caixa de correio do Exchange Online está sob um litígio ou bloqueio de descoberta eletrônica.
- A caixa de correio de usuário associados a conta de usuário foi removida nos últimos 30 dias; Active Directory do Azure qual é o tamanho máximo de retenção Exchange Online manterá a caixa de correio em um estado excluída antes que ela seja limpas e não serão permanentemente.

Uma caixa de correio de usuário que foi excluído rígido é uma caixa de correio que tenha sido excluída de uma das seguintes maneiras:
- A caixa de correio do usuário tenha sido excluída por mais de 30 dias e o usuário associado do Azure Active Directory tiver sido excluída por disco rígido. Todo o conteúdo de caixa de correio, como emails, contatos e arquivos são excluídos permanentemente.
- A conta de usuário associada a caixa de correio do usuário foi excluído do Azure Active Directory. A caixa de correio do usuário agora é excluída no Exchange Online e permanece em um estado excluída por 30 dias. Se no período de 30 dias, um novo usuário do Windows Azure Active Directory é sincronizado da conta destinatário original com o mesmo **ExchangeGuid** ou **ArchiveGuid**e licenciada nova conta para o Exchange Online, isso resultará em uma disco rígida exclusão de a caixa de correio do usuário original. Todo o conteúdo de caixa de correio, como emails, contatos e arquivos são excluídos permanentemente.
- Uma caixa de correio excluída é excluída usando **Remove-Mailbox-PermanentlyDelete**.

Os cenários de exclusão acima pressupõem que a caixa de correio do usuário não estiver em qualquer um dos Estados de espera, como litígio ou bloqueio de descoberta eletrônica. Se houver qualquer tipo de espera na caixa de correio, a caixa de correio não pode ser excluída. Para todos os tipos de destinatário do usuário de email, quaisquer configurações de [retenção](https://support.office.com/article/manage-legal-investigations-in-office-365-2e5fbe9f-ee4d-4178-8ff8-4356bc1b168e?ui=en-US&rs=en-US&ad=US) são ignoradas e não têm efeito sobre exclusões de disco rígido ou exclusões de reversível.

## <a name="soft-deleted-and-hard-deleted-items"></a>Itens excluída e disco rígido excluído
Quando um usuário exclui um item de caixa de correio (por exemplo, uma mensagem de email, um contato, um compromisso do calendário ou uma tarefa), o item é movido para a pasta itens recuperáveis e em uma subpasta chamada exclusões. Isso é conhecido como uma exclusão suave. Excluído por quanto tempo os itens são mantidos nas exclusões de pasta depende do período de retenção de item excluído é definido para a caixa de correio. Uma caixa de correio do Exchange Online mantém os itens excluídos por 14 dias por padrão, mas os administradores do Exchange Online podem alterar essa configuração para aumentar o período até um máximo de 30 dias. (Para obter etapas detalhadas aumentar o período de retenção de item excluído de uma caixa de correio do Exchange Online, consulte [itens de alteração quanto tempo permanentemente excluída são mantidos por uma caixa de correio do Exchange Online](https://docs.microsoft.com/exchange/recipients-in-exchange-online/manage-user-mailboxes/change-deleted-item-retention).) Os usuários podem recuperar ou limpar, itens excluídos antes do tempo de retenção para um item excluído expirar. Para fazer isso, eles usarem o recurso de recuperar itens excluídos no Microsoft Outlook ou no Outlook na web.

Se um usuário limpa um item excluído, usando o recurso de recuperar itens excluídos no Outlook ou no Outlook na web, isso é conhecido como uma exclusão de disco rígida. No Exchange Online, recuperação de item único está habilitada por padrão quando uma nova caixa de correio é criada, para que um administrador ainda possa [recuperar](https://docs.microsoft.com/Exchange/recipients/user-mailboxes/recover-deleted-messages) itens excluídos de disco rígido antes que o período de retenção de item excluído expire. Além disso, se uma mensagem for alterada por um usuário ou um processo, cópias do item original também são mantidas quando a recuperação de item único está habilitada.

## <a name="page-zeroing"></a>Anulação de página
*Zeramento* é um mecanismo de segurança que grava zeros ou um padrão de binário sobre dados excluídos, de modo que os dados excluídos serão mais difícil recuperar. No Exchange Online, bancos de dados de caixa de correio usam *páginas* como sua unidade de armazenamento em implementam um processo de sobrescrever chamado *anulação de página*. Anulação de página é habilitada por padrão e não pode ser desabilitado por clientes ou pela Microsoft. Operações de anulação de página são registradas nos arquivos de log de transação para que todas as cópias de um determinado banco de dados são página-anuladas de maneira semelhante. Anulação de uma página em uma cópia do banco de dados ativo faz com que a página a ser obtido anuladas em cópias passivas do banco de dados.

Anulação de página grava um binário padrão sobre registros excluídos de disco rígido. O padrão de anulação de página é específico para operações de mecanismo de armazenamento extensível (ESE) (o nome do mecanismo de banco de dados interno usado pelos servidores no Exchange Online) e for diferente para operações de tempo de execução versus operações de manutenção de banco de dados em segundo plano. (A manutenção de banco de dados do plano de fundo é um processo que continuamente somas de verificação e exames que cada banco de dados. Sua função principal é páginas de banco de dados de soma de verificação, mas também trata limpando espaço e anulação de registros e páginas que não foram anuladas check-out por causa de uma falha de armazenamento.)

A tabela a seguir lista os padrões de preenchimento que correspondem a operações em tempo de execução específicas.

| Operação em tempo real do ESE   | Padrão de preenchimento |
|--------------------------|--------------|
| Substituir                  | N            |
| Exclusão de valor longo/registro | D            |
| Liberação de espaço em página         | H            |


A tabela a seguir lista os padrões de preenchimento que correspondem a operações específicas que ocorrem durante a manutenção de banco de dados em segundo plano do ESE.

| Operação de manutenção de banco de dados em segundo plano do ESE | Padrão de preenchimento |
|-----------------------------------------------|--------------|
| Exclusão de gravação                                 | D            |
| Exclusão de valor longo                             | L            |
| Liberação de espaço em página parcialmente utilizada       | Z            |
| Liberação de espaço em página não utilizada               | U            |


### <a name="page-zeroing-process"></a>Processo de anulação de página
O processo de anulação de página depende do cenário de exclusão. A tabela a seguir discute os cenários de exclusão de banco de dados, e quando as funções de anulação de página ocorrem.

| Cenário de exclusão de banco de dados | Processo do ESE e tempo para anulação dos dados do banco de dados |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Item expira com base no período de retenção de item excluído. | Um thread assíncrono grava um padrão binário sobre os dados excluídos. Essa ação ocorre milissegundos após a exclusão do registro. Se o processo de armazenamento falhar enquanto a operação de anulação assíncrona estiver em curso (ou se a limpeza do armazenamento de versão for cancelada devido ao crescimento do armazenamento de versão), a anulação será concluída quando a manutenção de banco de dados em segundo plano processar essa seção do banco de dados. |
| Cenário de exibição: Expiração de itens do Outlook para o Outlook na visualização de pastas da web (por exemplo, a exibição de conversa) | A anulação de dados ocorre quando uma manutenção de banco de dados em segundo plano processa esta seção do banco de dados. |
| Cenário de caixa de correio de caixa de correio/excluir movimentação: De correio de origem excluído (expiração de caixa de correio excluída) | A anulação de dados ocorre quando uma manutenção de banco de dados em segundo plano processa esta seção do banco de dados. |

### <a name="mailbox-data-types-without-page-zeroing"></a>Tipos de dados de caixa de correio sem anulação de página
Os seguintes tipos de dados de caixa de correio não têm provisões para anulação de página:
- **Logs de transações do banco de dados de caixa de correio** - quando os logs de transação serão excluídos como parte das operações normais, não há nenhum processo como zero os blocos no sistema de arquivos que são armazenados os arquivos de log excluído. É provável que o sistema de arquivos rapidamente utilizará novamente esse espaço livre para logs recém-criados, mas não há nenhuma garantia de que isso acontecerá.
- **Arquivos de catálogo do índice de conteúdo** - Exchange Online usa Search Foundation (também conhecido como FAST) para a funcionalidade de indexação de pesquisa. O catálogo de índice de pesquisa é composto de vários arquivos de dezenas armazenados no mesmo volume como o arquivo de banco de dados de caixa de correio. Quando uma mensagem é excluído do banco de dados de caixa de correio, o conteúdo associado no catálogo de pesquisa não é excluído imediatamente. Exclusão de conteúdo ocorre quando o Search Foundation uma sombra (ou mesclagem mestra) dos arquivos de catálogo pequeno muitos em para um único arquivo maior. Quando a mesclagem mestra for concluída, os arquivos de catálogo menores são excluídos. Não há nenhum processo como zero blocos que armazenados os arquivos de catálogo excluído.

## <a name="continuous-replication"></a>Replicação Contínua
Replicação contínua (também conhecido como o envio de log e repetição) é uma tecnologia no Exchange Online que cria e mantém cópias de cada banco de dados de caixa de correio para fornecer alta disponibilidade, resiliência do site e recuperação de desastres. Replicação contínua aproveita o suporte de recuperação de travamento de banco de dados Exchange Server para fornecer a tecnologia que está executando a atualização assíncrona de um ou mais cópias de um banco de dados de caixa de correio. Cada servidor de caixa de correio registra as atualizações do banco de dados feitas em um banco de dados ativo (por exemplo, atividade de email de usuário) como um registro de log em um conjunto sequencial dos arquivos de log de transação de 1 MB. Este conjunto de arquivos é conhecido como fluxo de log. Replicação contínua, fluxo de log também é usado para atualizar assincronamente uma ou mais cópias de um banco de dados. Isso é realizado através da transmissão os logs para um local que contém uma cópia passiva do banco de dados ativo e, em seguida, reproduzi-las na cópia passiva do banco de dados. Se todos os logs do banco de dados ativo são reproduzidos sobre uma cópia passiva do banco de dados, em seguida, os dois bancos de dados são equivalentes e é por meio desse processo que qualquer alteração de física feita em um banco de dados ativo seja replicada em todas as cópias passivas do banco de dados.

Qualquer exclusão de um banco de dados de caixa de correio, se um item de caixa de correio ou uma caixa de correio inteira e se uma exclusão reversível- ou -delete, rígido representa uma alteração física no banco de dados ativo. Também de anulação de página envolve a realização de alterações físicas no banco de dados ativo. Essas alterações são gravadas nos arquivos de log por meio de um processo chamado replicação contínua e quando os arquivos de log são repetidos contra cópias passivas do banco de dados, as mesmas alterações físicas são feitas desses bancos de dados passivos.
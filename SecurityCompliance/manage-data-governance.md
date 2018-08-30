---
title: Gerenciar controle de dados no Office 365
ms.author: stephow
author: stephow-msft
manager: laurawi
ms.date: 5/9/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 48064107-fed2-4db0-9e5c-aa5ddd5ccb09
description: Governança de dados é tudo sobre seus dados em torno quando você precisar de capacidade de manter e Obtendo elimine-quando você não. Com a governança de dados no Office 365, você pode gerenciar o ciclo de vida completo de conteúdo, de importação e armazenamento de dados no início, para criar políticas de mantém e excluir permanentemente o conteúdo no final.
ms.openlocfilehash: ca3443c3b90a067bf171ddf89be604d262a7b9a4
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524573"
---
# <a name="manage-data-governance-in-office-365"></a>Gerenciar controle de dados no Office 365

Governança de dados é tudo sobre seus dados em torno quando você precisar de capacidade de manter e Obtendo elimine-quando você não. Com a governança de dados no Office 365, você pode gerenciar o ciclo de vida completo de conteúdo, de importação e armazenamento de dados no início, para criar políticas de mantém e excluir permanentemente o conteúdo no final.
  
## <a name="import"></a>Importar

Alguns dos seus dados podem ser armazenadas em locais de fora da nuvem, assim como os servidores no local ou em aplicativos de terceiros. O serviço de importação facilita trazer suas mensagens, SharePoint e OneDrive para dados corporativos no Office 365, pelo carregá-la diretamente pela rede ou envio de uma unidade criptografada para nós. Você também pode usar o recurso de importação inteligente no serviço de importação para filtrar os itens em arquivos PST que realmente obtém importou para as caixas de correio de destino. 
  
- [Visão geral da importação de arquivos PST para o Office 365](https://support.office.com/article/ba688e0a-0fcb-4bd7-8e57-2b669564ea84)
    
- [Usar o carregamento de rede para importar arquivos PST para o Office 365](use-network-upload-to-import-pst-files.md)
    
- [Usar o envio de unidade para importar arquivos PST para o Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md)
    
- [Usar a ferramenta de conjunto de PST para localizar, copiar e excluir arquivos PST em sua organização](find-copy-and-delete-pst-files-in-your-organization.md)
    
- [Filtrar dados ao importar arquivos PST para o Office 365](filter-data-when-importing-pst-files.md)
    
- [Carregar conteúdo local para o SharePoint Online usando cmdlets do PowerShell](https://support.office.com/article/555049c6-15ef-45a6-9a1f-a1ef673b867c)
    
## <a name="govern-i-store-data"></a>Controlar os dados do repositório de i:

Depois de importar dados, talvez seja necessário aumentar o seu armazenamento. O recurso de arquivamento ilimitado no Office 365 (chamado expansão automática de arquivamento) fornece uma quantidade ilimitada de armazenamento em caixas de correio de arquivo morto.
  
- [Habilitar o arquivamento de caixas de correio no Office 365 Security &amp; Centro de conformidade](enable-archive-mailboxes.md)

- [Visão geral do arquivamento ilimitado no Office 365](unlimited-archiving.md)
    
- [Habilitar o arquivamento ilimitado no Office 365](enable-unlimited-archiving.md)
    

    
## <a name="govern-ii-create-policies-and-labels-to-retain-content"></a>Administrar II: Criar políticas e rótulos para reter o conteúdo

Uma política de retenção ajuda você a proativamente cumprir com as normas do setor e políticas internas, garantindo que você detém desde conforme necessário mas não é mais do que o de conteúdo. Uma única política de retenção pode cobrir toda sua organização. Além disso, você pode usar rótulos para implementar um plano de arquivo, a classificação de dados em toda a organização governança e, em seguida, aplicando regras de retenção com base nessa classificação.
  
- [Visão geral de políticas de retenção](retention-policies.md)
    
- [Visão geral de rótulos](labels.md)
    
- [Em massa criar e publicar rótulos usando PowerShell](https://support.office.com/article/8986701b-ffa1-46ec-8fd0-8f7e81d5b25f.aspx)
    
- [Visão geral das revisões de disposição](disposition-reviews.md)
    
- [Visão geral de retenção orientada a eventos](event-driven-retention.md)
    
## <a name="govern-iii-retain-the-email-of-former-employees"></a>Administrar III: Manter o email de funcionários anteriores

Quando uma pessoa sair de sua organização, você pode reter seus emails através da criação de uma caixa de correio inativa. Uma caixa de correio torna-se inativa quando um litígio, política de retenção do Office 365, ou outro tipo de bloqueio é aplicado a ele e, em seguida, a conta de usuário do Office 365 correspondente é excluída. Itens em uma caixa de correio inativa são retidos para a duração da política de retenção ou retenção feita na caixa de correio antes que ela foi feita inativa.
  
- [Visão geral das caixas de correio inativas no Office 365](inactive-mailboxes-in-office-365.md)
    
- [Criar e gerenciar caixas de correio inativas no Office 365](create-and-manage-inactive-mailboxes.md)

- [Alterar a duração de espera para uma caixa de correio inativa no Office 365](change-the-hold-duration-for-an-inactive-mailbox.md)
  
- [Recuperar uma caixa de correio inativa no Office 365](recover-an-inactive-mailbox.md)
 
- [Restaurar uma caixa de correio inativa no Office 365](restore-an-inactive-mailbox.md)

- [Excluir uma caixa de correio inativa no Office 365](delete-an-inactive-mailbox.md)

## <a name="monitor"></a>Monitorar

Supervisão permite definir políticas que capturam email e comunicações de terceiros 3rd em sua organização para que eles podem ser examinados pelos revisores internos ou externos. Revisores podem classificar essas comunicações, certificar-se de que eles estão em conformidade com as diretivas da sua organização e escalonar material questionável, se necessário.
  
Você também pode usar os relatórios de governança de dados e o Gerenciador de atividade de rótulo para monitorar a que as etiquetas estão sendo aplicadas ao conteúdo conforme pretendido.
  
- [Configurar políticas de supervisão da sua organização](configure-supervision-policies.md)
    
- [Relatórios de supervisão](supervision-reports.md)
    
- [Exibir a atividade de rótulos de documentos](view-label-activity-for-documents.md)
    
- [Exibir os relatórios de governança de dados](view-the-data-governance-reports.md)
    
## <a name="more-information"></a>Mais informações

- [Assistir aos vídeos da equipe de Governança de dados da Microsoft](https://go.microsoft.com/fwlink/?linkid=867039)
    
- [Assista a uma visão geral de governança de dados no Office 365](https://go.microsoft.com/fwlink/?linkid=852644)
    
- [Segurança do Office 365 &amp; cmdlets do Centro de conformidade](https://go.microsoft.com/fwlink/?linkid=852310)
    


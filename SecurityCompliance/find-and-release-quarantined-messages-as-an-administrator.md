---
title: Localizar e liberar mensagens em quarentena como um administrador
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/16/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: ab95bf17-bb09-4dd1-9990-ddd02ddecf05
description: Este tópico descreve como os administradores do Exchange Online e do Exchange Online Protection (EOP) podem localizar, liberar e relatar mensagens que estejam na quarentena do Centro de administração do Exchange (EAC).
ms.openlocfilehash: 5ebe65bf703087e8ad4bace827d84833eddb038f
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027478"
---
# <a name="find-and-release-quarantined-messages-as-an-administrator"></a>Localizar e liberar mensagens em quarentena como um administrador

Este tópico descreve como os administradores do Exchange Online e do Exchange Online Protection (EOP) podem localizar, liberar e relatar mensagens que estejam na quarentena do Centro de administração do Exchange (EAC). O Office 365envia as mensagens para a quarentena porque foram identificadas como spam ou porque corresponderam a uma regra de transporte. 
  
Usar a segurança &amp; Centro de conformidade, em vez do EAC para concluir qualquer uma destas tarefas, bem como exibir e trabalhar com mensagens enviadas para quarentena porque eles contêm malware. Para obter mais informações, consulte [mensagens de email de quarentena no Office 365](https://support.office.com/en-US/article/Quarantine-email-messages-in-Office-365-4c234874-015e-4768-8495-98fcccfc639b).
  
As mensagens em quarentena são listadas na página **quarentena** do EAC. Por padrão, as mensagens são classificadas da mais nova para a mais antiga no campo **RECEBIDAS**. Os valores **REMETENTE**, **ASSUNTO** e **EXPIRA** também são listados para cada mensagem. Você pode classificar com base em qualquer um desses campos clicando nos cabeçalhos. Clicar em um cabeçalho de coluna uma segunda vez inverterá a ordem de classificação. No máximo 500 mensagens podem ser exibidas na página **quarentena** 
  
É possível exibir uma lista de todas as mensagens em quarentena ou pesquisar por mensagens específicas determinando critérios de filtragem (a filtragem também pode ajudar a reduzir o conjunto de resultados se você tiver mais de 500 mensagens). Após procurar e localizar uma mensagem em quarentena específica, é possível visualizar detalhes sobre a mensagem. Você também pode:
  
- Liberar a mensagem para um ou mais destinatários e, como opção, relatá-la como um falso positivo (que não é lixo eletrônico) para a equipe de análise de spam da Microsoft, que avaliará e analisará a mensagem. Dependendo dos resultados da análise, as regras de filtro de conteúdo de spam de todo o serviço podem ser ajustadas para permitir a mensagem.
    
- Liberar a mensagem e permitir todas as mensagens futuras desse remetente.
    
## <a name="what-do-you-need-to-know-before-you-begin"></a>O que você precisa saber antes de começar?
<a name="sectionSection0"> </a>

- Você precisa ter permissões antes de executar este procedimento ou procedimentos. Para ver quais permissões você precisa, consulte a entrada "Quarentena" no tópico [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) . 
    
- Você pode liberar ou relatar várias mensagens ao mesmo tempo na página **quarentena**. Como alternativa, pode criar um script do Windows PowerShell remoto para realizar essa tarefa. Use o cmdlet [Get-QuarantineMessage](http://technet.microsoft.com/library/88026da1-8dbc-49e7-80e8-112a32773c34.aspx) para procurar as mensagens e o cmdlet [Release-QuarantineMessage](http://technet.microsoft.com/library/4a3aa05c-238f-46f2-b8dd-b0e3c38eab3e.aspx) para liberá-las. 
    
- Para informações sobre atalhos de teclado que possam se aplicar aos procedimentos neste tópico, consulte **Atalhos de teclado no Centro de administração do Exchange**.
    
> [!TIP]
> Está enfrentando problemas? Peça ajuda nos fóruns do Exchange. Visite os fóruns em: [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), ou [Proteção do Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=285351). 
  
## <a name="use-advanced-search-to-filter-and-locate-quarantined-messages"></a>Usar a pesquisa avançada para filtrar e localizar mensagens em quarentena
<a name="BKMK_UseAdvancedSearchtoFilterMessages"> </a>

No Centro de administração do Exchange (EAC), você pode filtrar itens da quarentena de acordo com várias condições usando a pesquisa avançada. É possível utilizar estes critérios separadamente ou combinados. A pesquisa fornecerá uma lista de mensagens que atendem a todos os seus critérios de filtro.
  
1. No EAC, navegue até **Proteção** \> **quarentena** e clique em **Pesquisa Avançada**.
    
2. Na janela **Pesquisa Avançada** selecione qualquer combinação das condições a seguir. Marque a caixa de seleção associada para permitir cada condição. Caracteres curinga não são suportados. 
    
1. **ID da Mensagem** Você pode usar este parâmetro para realizar uma busca direcionada para uma mensagem específica. Por exemplo, se uma mensagem específica é enviada por, ou destinada a, um usuário em sua organização, mas ela nunca chega ao seu destino, você pode procurar a mensagem utilizando o recurso de rastreamento de mensagens. Para saber mais, confira [Executar um rastreamento de mensagem e exibir os resultados](http://technet.microsoft.com/library/74a9fc59-7e0e-4832-baf9-2a86418b0079.aspx). Se você descobrir que a mensagem foi enviada para a quarentena, talvez porque ela corresponde a uma regra ou foi identificada como spam, é possível encontrá-la facilmente na quarentena especificando sua ID de Mensagem. Lembre-se de incluir a sequência completa da ID da Mensagem. Isso pode incluir colchetes angulares (\<\>). 
    
2. **Endereço de email do remetente** Especifica o endereço de email da pessoa que enviou a mensagem. 
    
3. **Endereço de email do destinatário** Especifica o endereço de email do destinatário desejado da mensagem. 
    
4. **Assunto** Especifica o texto da linha de assunto da mensagem. 
    
5. **Recebido** Você pode selecionar se a mensagem foi recebida pela quarentena nas últimas 24 horas ( **Hoje**), nas últimas 48 horas ( **Últimos 2 dias**), na última semana ( **Últimos 7 dias**) ou pode escolher um intervalo de tempo personalizado durante o qual a mensagem foi recebida pela quarentena. 
    
6. **Expira** Você pode escolher se a mensagem será excluída da quarentena nas próximas 24 horas ( **Hoje**), nas próximas 48 horas ( **Próximos 2 dias**), na próxima semana ( **Próximos 7 dias**) ou pode escolher um intervalo de tempo personalizado durante o qual a mensagem será excluída da quarentena.
    
    > [!IMPORTANT]
    > Por padrão, as mensagens de spam em quarentena são mantidas em quarentena por 15 dias, enquanto as mensagens em quarentena que correspondem a uma regra de transporte são mantidas em quarentena por 7 dias. Após este período de tempo que o Office 365 exclui as mensagens e elas não são recuperáveis. O período de retenção de mensagens em quarentena que correspondem a uma regra de transporte não é configurável. No entanto, o período de retenção para mensagens de spam em quarentena pode ser reduzido por meio da configuração de **spam de reter de (dias)** em suas políticas de filtro de conteúdo. Para obter mais informações, consulte [configurar suas políticas de filtro de spam](configure-your-spam-filter-policies.md). 
  
7. **Tipo** É possível especificar se deseja pesquisar por mensagens em quarentena que foram identificadas como **Spam**, ou se deseja pesquisar por mensagens que correspondem a uma **Regra de transporte**.
    
3. Clique em **OK** para iniciar a pesquisa avançada. 
    
    > [!NOTE]
    > Para apagar seus critérios de pesquisa e exibir todas as mensagens em quarentena, apague todas as caixas de seleção na janela **Pesquisa avançada** e, em seguida, clique em **OK**. 
  
Após pesquisar por mensagens, os resultados que correspondem aos seus critérios especificados serão exibidos na interface do usuário. No máximo 500 mensagens podem ser exibidas no EAC. 
  
## <a name="view-details-about-a-specific-quarantined-message"></a>Visualizar detalhes sobre uma mensagem específica colocada em quarentena
<a name="BKMK_ViewDetailsAboutaSpecificQuarantinedMessage"> </a>

Após localizar uma determinada mensagem em quarentena na página **quarentena**, é possível exibir detalhes sobre ela. 
  
1. Na página **quarentena**, selecione uma mensagem específica e um resumo das propriedades dessa mensagem é exibido no painel de detalhes no lado direito da tela. 
    
    Os valores de **Status da mensagem** são os seguintes: 
    
  - **Tipo** Indica se a mensagem foi identificada como **Spam** ou se corresponde a uma **Regra de transporte**.
    
  - **Vencimento** A data em que a mensagem será excluída da quarentena. 
    
    Os valores dos **Detalhes da mensagem** são os seguintes: 
    
  - **Remetente** Endereço de email da pessoa que enviou a mensagem. 
    
  - **Assunto** O texto da linha de assunto da mensagem. 
    
  - **Recebido** A data em que a mensagem foi recebida pela quarentena 
    
  - **Tamanho** O tamanho da mensagem em kilobytes (KB) ou, se o tamanho da mensagem for maior do que 999 KB, em megabytes (MB). 
    
  - **Exibir cabeçalho de mensagem** Clique neste link para abrir a caixa de diálogo **cabeçalho de mensagem**, que lhe permite ver o texto do cabeçalho da mensagem. Você também pode copiar o texto do cabeçalho da mensagem e colá-lo no [Analisador de Cabeçalho de Mensagem](https://testconnectivity.microsoft.com/?tabid=mha). Quando estiver na ferramenta Analisador de Cabeçalho de Mensagem, clique em **Analisar cabeçalhos** para recuperar informações sobre o cabeçalho. 
    
    > [!TIP]
    > Para saber mais sobre campos de cabeçalho de mensagens antispam específicas inseridos pelo serviço, veja [Cabeçalhos de mensagem antispam](anti-spam-message-headers.md). 
  
  - **Visualizar a mensagem de email** Clique nesse link para analisar o texto da mensagem. 
    
2. Se você clicar duas vezes em uma mensagem em quarentena, a janela **Mensagem em quarentena** abre e exibe a informação a seguir: 
    
  - **Liberado para** Uma lista de todos os endereços de email para quem a mensagem foi liberada, se houver algum. 
    
  - **Ainda não liberado para** Uma lista de todos os endereços de email para quem a mensagem não foi liberada, se houver algum. Você pode clicar no link **Liberar para** para liberar a mensagem; para saber mais sobre como liberar uma mensagem, confira a próxima seção. 
    
  - **ID da Mensagem** A ID da mensagens de Internet (também conhecida como ID do Cliente) encontrada no cabeçalho da mensagem. 
    
    Clique em **Fechar** para retornar ao painel principal da quarentena. 
    
## <a name="release-messages-from-quarantine"></a>Liberar as mensagens da quarentena
<a name="sectionSection3"> </a>

Se você quiser liberar as mensagens para destinatários, as opções são:
  
- [Liberar uma mensagem em quarentena e permitir as mensagens futuras do remetente](find-and-release-quarantined-messages-as-an-administrator.md#Releasequarantinedmessageallowfuturemessagesfromsender)
    
- [Liberar uma mensagem em quarentena para destinatários específicos sem relatá-la como falso positivo](find-and-release-quarantined-messages-as-an-administrator.md#Releasequarantinedmessagetospecificrecipientswithoutreportingasfalsepositive)
    
- [Liberar uma ou mais mensagens em quarentena a todos os destinatários](find-and-release-quarantined-messages-as-an-administrator.md#Releaseoneormorequarantinedmessagestoallrecipients)
    
- [Liberar uma ou mais mensagens em quarentena a todos os destinatários e relatar falsos positivos](find-and-release-quarantined-messages-as-an-administrator.md#Releaseoneormorequarantinedmessagestoallrecipientsandreportfalsepositives)
    
### <a name="release-a-quarantined-message-and-allow-future-messages-from-the-sender"></a>Liberar uma mensagem em quarentena e permitir as mensagens futuras do remetente
<a name="Releasequarantinedmessageallowfuturemessagesfromsender"> </a>

1. No EAC, navegue até **Proteção** \> **quarentena**.
    
2. Clique em uma mensagem para selecioná-la e, em seguida, clique no ícone **Liberar Mensagem**, conforme mostrado na captura de tela a seguir. 
  
![Mostra a página de quarentena com o ícone de mensagem lançamento realçado e as opções de lançamento exibindo](media/36ee081f-3e30-40c9-8ce3-240cee1970cc.png)
  
Clique em **Liberar mensagem selecionada e permitir remetente** na lista suspensa. 
    
3. A caixa de diálogo **liberar mensagem e permitir remetente** é exibida. Opcionalmente, você pode optar por relatar a mensagem para a Microsoft e, então, clicar em **liberar e permitir**. A mensagem será disponibilizada a todos os destinatários para os quais é endereçada e todas as mensagens futuras deste remetente serão permitidas. No entanto, se essa mensagem foi colocada em quarentena devido a uma regra de transporte ou remetente bloqueado, o remetente continuará a ser bloqueado para mensagens futuras. 
    
### <a name="release-a-quarantined-message-to-specific-recipients-without-reporting-it-as-a-false-positive"></a>Liberar uma mensagem em quarentena para destinatários específicos sem relatá-la como falso positivo
<a name="Releasequarantinedmessagetospecificrecipientswithoutreportingasfalsepositive"> </a>

1. No EAC, navegue até **Proteção** \> **quarentena**.
    
2. Selecione uma mensagem, clique no ícone **Liberar Mensagem** e, então, clique em **Liberar a mensagem para destinatários específicos** na lista suspensa. 
    
3. Na caixa de diálogo **Liberar mensagem**, selecione uma das seguintes opções: 
    
  - **Liberar mensagem para todos os destinatários** Ao selecionar esta opção, você está ciente que uma mensagem não pode ser liberada mais que uma vez para o mesmo destinatário. Se um destinatário recebeu a mensagem anteriormente, ela não será liberada novamente para esse destinatário. 
    
  - **Liberar mensagem para destinatários específicos** Selecione o(s) dstinatário(s) para o(s) qual(is) a mensagem pode ser liberada. Como uma mensagem só pode ser liberada uma vez para cada destinatário, apenas aqueles para os quais ela pode ser liberada aparecem nesta lista. Há suporte para várias seleções. Você pode escolher vários destinatários. Depois de fazer suas seleções, clique em **adicionar**.
    
4. Clique em **Liberar**. 
    
Se você clicar no ícone **Atualizar**![Ícone Atualizar](media/ITPro-EAC-RefreshIcon.png) para atualizar seus dados e, depois, clicar duas vezes na mensagem, ela deverá ser liberada para os destinatários pretendidos. 
  
### <a name="release-one-or-more-quarantined-messages-to-all-recipients"></a>Liberar uma ou mais mensagens em quarentena a todos os destinatários
<a name="Releaseoneormorequarantinedmessagestoallrecipients"> </a>

1. No EAC, navegue até **Proteção** \> **quarentena**.
    
2. Clique em uma mensagem para selecioná-la, ou use a tecla Shift para selecionar várias mensagens. Clique no ícone **Liberar Mensagem**. 
    
3. Clique em **Liberar as mensagens selecionadas para TODOS os destinatários** na lista suspensa. 
    
4. A caixa de diálogo de aviso. Leia o aviso e selecione **Sim** se quiser prosseguir. Ao selecionar esta opção, esteja ciente que uma mensagem não pode ser liberada mais que uma vez para o mesmo destinatário. Se um destinatário recebeu a mensagem anteriormente, ela não será liberada novamente para esse destinatário. 
    
### <a name="release-one-or-more-quarantined-messages-to-all-recipients-and-report-false-positives"></a>Liberar uma ou mais mensagens em quarentena a todos os destinatários e relatar falsos positivos
<a name="Releaseoneormorequarantinedmessagestoallrecipientsandreportfalsepositives"> </a>

1. No EAC, navegue até **Proteção** \> **quarentena**.
    
2. Clique em uma mensagem para selecioná-la, ou use a tecla Shift para selecionar várias mensagens. Clique no ícone **Liberar Mensagem**. 
    
3. Clique em **Liberar as mensagens selecionadas e relatá-las como falsos positivos** na lista suspensa. 
    
4. A caixa de diálogo de aviso. Leia o aviso e selecione **Sim** se quiser prosseguir. Ao selecionar esta opção, esteja ciente que uma mensagem não pode ser liberada mais que uma vez para o mesmo destinatário. Se um destinatário recebeu a mensagem anteriormente, ela não será liberada novamente para esse destinatário. 
    
     Ao escolher esta opção, a mensagem será liberada para todos os destinatários que ainda não a receberam. Se for uma mensagem de spam em quarentena, ela também será relatada à Equipe de Análise de Spam da Microsoft, a qual avaliará e analisará a mensagem. Dependendo dos resultados da análise, as regras de filtro de conteúdo de spam de todo o serviço podem ser ajustadas para permitir a mensagem. 
    
> [!TIP]
> Ajude a garantir que uma mensagem não seja marcada como spam seguindo as etapas em [Como ajudar a garantir que uma mensagem não foi marcada como spam](how-to-help-ensure-that-a-message-isn-t-marked-as-spam.md). 
  
Se você clicar no ícone **Atualizar**![Ícone Atualizar](media/ITPro-EAC-RefreshIcon.png) para atualizar seus dados e, depois, clicar duas vezes na mensagem, ela deverá ser liberada para os destinatários pretendidos. 
  
## <a name="for-more-information"></a>Para saber mais
<a name="sectionSection4"> </a>

[Perguntas Frequentes sobre a Quarentena](quarantine-faq.md)
  


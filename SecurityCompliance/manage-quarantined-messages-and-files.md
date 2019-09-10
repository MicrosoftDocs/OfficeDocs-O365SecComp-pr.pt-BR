---
title: Gerenciar arquivos e mensagens em quarentena como um administrador no Office 365
ms.author: tracyp
author: MSFTTracyp
manager: dansimp
ms.date: 09/05/2018
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 065cc2cf-2f3a-47fd-a434-2a20b8f51d0c
ms.collection:
- M365-security-compliance
description: Os administradores podem aprender a exibir e gerenciar mensagens em quarentena no centro de conformidade & segurança do Office 365.
ms.openlocfilehash: 0b67abe3dbf21650925b53d2882bc40096d6a646
ms.sourcegitcommit: 81b3bff27bc60235a38004c5b0297ac454331b25
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2019
ms.locfileid: "36822521"
---
# <a name="manage-quarantined-messages-and-files-as-an-admin-in-office-365"></a>Gerenciar arquivos e mensagens em quarentena como um administrador no Office 365

Como administrador, você pode exibir, liberar e excluir mensagens em quarentena e relatar mensagens em quarentena falsas positivas no Office 365. Você também pode exibir, baixar e excluir arquivos em quarentena capturados pela proteção avançada contra ameaças (ATP) para o SharePoint Online, OneDrive for Business e Microsoft Teams. Você pode configurar políticas para que o Office 365 Filtre mensagens e as envie para quarentena por vários motivos: porque elas foram identificadas como spam, email em massa, emails de phishing, contendo malware ou porque corresponderam a uma regra de fluxo de emails.

Por padrão, o Office 365 envia mensagens de phishing e mensagens contendo malware diretamente para a quarentena. Outras mensagens filtradas são enviadas para a pasta lixo eletrônico dos usuários, a menos que você configure uma política para enviá-las à quarentena.

Para exibir e executar ações em mensagens em quarentena no centro de conformidade e segurança &, sua conta precisa de uma das seguintes permissões:

**Função de destinatários somente para exibição**: exiba a lista de mensagens em quarentena.

**Função do leitor de segurança**: exibir a lista de mensagens em quarentena e seus cabeçalhos de mensagens.

**Função de administrador de segurança**: exibir a lista de mensagens em quarentena e seus cabeçalhos de mensagens; Visualizar, liberar, excluir e baixar mensagens em quarentena.

Por padrão, os grupos de função de gerenciamento de organização e de administrador de segurança no centro de conformidade do & de segurança têm a função de administrador de segurança atribuída a eles (portanto, a associação a um desses grupos de função fornece as permissões). Para obter mais informações, consulte [permissões no centro de conformidade & segurança do Office 365](permissions-in-the-security-and-compliance-center.md).

> [!IMPORTANT]
> Por padrão, as mensagens de spam, de massa e de phishing são mantidas em quarentena por 30 dias. As mensagens colocadas em quarentena porque corresponderam a uma regra de fluxo de emails são mantidas em quarentena por 7 dias. As mensagens de malware são mantidas em quarentena por 15 dias. Você pode personalizar o tempo de quarentena de spam nas configurações antispam no centro de conformidade de & de segurança. Quando o Office 365 exclui uma mensagem da quarentena, não é possível obtê-la novamente. Se desejar, você pode alterar o período de retenção para mensagens em quarentena nas políticas de filtro antispam. Para obter mais informações, consulte a seção [definir o período de retenção de quarentena](#set-the-quarantine-retention-period) neste tópico.

## <a name="view-your-organizations-quarantined-messages"></a>Exibir as mensagens em quarentena da sua organização

1. [Abra o centro de conformidade & segurança](go-to-the-securitycompliance-center.md) e vá para a **quarentena**de **análise** \> de **Gerenciamento** \> de ameaças.

   > [!TIP]
   > Para ir diretamente para a página **quarentena** , use esta URL: [https://protection.office.com/?hash=/quarantine](https://protection.office.com/?hash=/quarantine).

   Por padrão, o centro de conformidade & segurança exibe todas as mensagens de email em quarentena como spam. As mensagens são classificadas da mais nova para a mais antiga com base na **Data** em que a mensagem foi recebida. O **remetente**, o **assunto**e a data de expiração (em **vencimento**) também são exibidos para cada mensagem. Você pode classificar em um campo clicando no cabeçalho da coluna correspondente; clique em um cabeçalho de coluna uma segunda vez para reverter a ordem de classificação.

2. Você pode exibir uma lista de todas as mensagens em quarentena ou pode reduzir o conjunto de resultados por filtragem. Você só pode realizar operações em massa em até 100 itens, então a filtragem também pode ajudar a reduzir o conjunto de resultados se você tiver mais do que isso. Você pode filtrar mensagens rapidamente por um único motivo de quarentena escolhendo uma opção do filtro na parte superior da página. As opções incluem:

   - Email identificado como spam

   - Email colocado em quarentena porque correspondeu a uma política definida por uma regra de fluxo de emails (também conhecida como regra de transporte)

   - Email identificado como email em massa

   - Email identificado como email de phishing

   - Email colocado em quarentena porque contém malware

Como administrador, você também pode optar por filtrar todas as mensagens de sua organização ou apenas as mensagens enviadas a você. Os usuários finais só podem exibir e trabalhar com mensagens que foram enviadas a eles.

Você também pode filtrar seus resultados para encontrar mensagens específicas. Para obter dicas, consulte a seção [filtrar os resultados para localizar mensagens e arquivos em quarentena](#filter-the-results-to-find-quarantined-messages-and-files) neste tópico.

Após localizar uma mensagem em quarentena específica, clique na mensagem para exibir detalhes sobre ela e execute ações, como liberar a mensagem para a caixa de correio de alguém.

## <a name="view-your-organizations-quarantined-files"></a>Exibir os arquivos em quarentena de sua organização

1. [Abra o centro de conformidade & segurança](go-to-the-securitycompliance-center.md) e vá para a **quarentena**de **análise** \> de **Gerenciamento** \> de ameaças.

   > [!TIP]
   > Para ir diretamente para a página **quarentena** no centro de conformidade de & de segurança, use esta URL: >[https://protection.office.com/?hash=/quarantine](https://protection.office.com/?hash=/quarantine)

   Por padrão, a página exibe mensagens de email em quarentena. Para exibir os arquivos em quarentena, defina os filtros na parte superior da página para mostrar os **arquivos**em quarentena devido a **malware**.

   Os arquivos são classificados do mais recente para o mais antigo com base na data em que o arquivo foi colocado em quarentena. O **usuário** que modificou o arquivo pela última vez, o **serviço** no qual o arquivo foi postado, o **nome do arquivo**, o **local**, o **tamanho do arquivo**e a data de expiração ( **expira**) também estão listados para cada arquivo. Você pode classificar em um campo clicando em um cabeçalho; clique em um cabeçalho de coluna uma segunda vez para reverter a ordem de classificação.

2. Você pode exibir uma lista de todos os arquivos em quarentena ou pode pesquisar arquivos específicos por filtragem. Assim como as mensagens, você só pode realizar operações em massa em até 100 itens. Atualmente, o centro de conformidade & segurança permite que você visualize e gerencie arquivos que estão em quarentena porque foram identificados como contendo malware. Para obter dicas, consulte a próxima seção.

## <a name="filter-the-results-to-find-quarantined-messages-and-files"></a>Filtrar os resultados para localizar arquivos e mensagens em quarentena

Dependendo das suas configurações, pode haver muito de arquivos e mensagens em quarentena. Para localizar uma mensagem ou um arquivo específico ou um conjunto de mensagens ou arquivos, você pode filtrar itens em quarentena com base em uma variedade de informações adicionais.

1. Na página **quarentena** , verifique se a linha superior dos filtros está definida para exibir mensagens ou arquivos conforme apropriado:

   - Para procurar arquivos, defina os filtros para mostrar **arquivos** em quarentena devido a **malware**.

     Para arquivos em quarentena, a página exibe todos os arquivos em quarentena, não apenas os seus, independentemente do que você deseja que seja mostrado.

   - Para pesquisar mensagens em quarentena, defina filtros para mostrar **todos** ou **apenas o meu** **email**. Para o último filtro, escolha o tipo de mensagem em quarentena que você está procurando. Você pode pesquisar por mensagens em quarentena que foram identificadas como **spam**, para mensagens que correspondam a uma regra de fluxo de emails (**regra de transporte**), emails **em massa** , emails de **phishing** ou emails que contenham **malware**.

2. Em **classificar resultados por**, escolha o filtro ou filtros que você deseja usar para Pesquisar nas listas suspensas. As opções variam de acordo com o fato de você estar pesquisando arquivos ou mensagens. Não há suporte para caracteres curinga nos campos de pesquisa no momento.

   Para arquivos e mensagens, você pode optar por filtrar pela data em que a mensagem ou o arquivo foi enviado para a quarentena. Você pode especificar a data ou um intervalo de datas, incluindo a hora. Você também pode filtrar os resultados da pesquisa pela data de expiração na qual o arquivo ou a mensagem será excluído da quarentena ou você pode usar uma combinação de filtros. Para pesquisar por data de expiração, escolha **filtro avançado**. Em **expirar**, você pode selecionar mensagens que serão excluídas da quarentena nas próximas 24 horas ( **hoje**), nas próximas 48 horas ( **próximos 2 dias**), na próxima semana (próximos **7 dias**) ou você pode selecionar um intervalo de tempo personalizado.

   Para mensagens, você tem as seguintes opções adicionais:

   - **ID da mensagem**: Use esta para identificar uma mensagem específica quando você souber a ID da mensagem.

     Por exemplo, se uma mensagem específica é enviada por ou destinada a um usuário em sua organização, mas nunca atingiu seu destino, você pode pesquisar a mensagem usando um [rastreamento de mensagem](message-trace-scc.md). Se você descobrir que a mensagem foi enviada para a quarentena, talvez porque correspondeu a uma regra de fluxo de emails ou tenha sido identificada como spam, você pode facilmente localizar essa mensagem em quarentena, especificando sua ID de mensagem. Certifique-se de incluir a cadeia de ID de mensagem completa. Isso pode incluir colchetes angulares\<\>(), por exemplo `<79239079-d95a-483a-aacf-e954f592a0f6@XYZPR00BM0200.contoso.com>`:.

   - **Endereço de email do remetente**: escolha filtrar por um único endereço de email do remetente.

   - **Endereço de email do destinatário**: escolha filtrar por um único endereço de email do destinatário.

   - **Assunto**. Insira o assunto de um endereço de email que você deseja localizar. Como a pesquisa curinga não é suportada, você deve usar o assunto inteiro da mensagem para que a pesquisa retorne a mensagem nos resultados. A pesquisa não diferencia maiúsculas de minúsculas.

## <a name="view-details-about-quarantined-messages-and-files"></a>Exibir detalhes sobre mensagens e arquivos em quarentena

Ao selecionar um item exibido na lista de quarentena, você verá um resumo de suas propriedades no painel de **detalhes** no lado direito do centro de conformidade do & de segurança.

### <a name="details-displayed-for-quarantined-messages"></a>Detalhes exibidos para mensagens em quarentena

- **ID da mensagem**: o identificador exclusivo da mensagem.

- **Endereço do remetente**: quem enviou a mensagem.

- **Recebido**: data e hora em que a mensagem foi recebida.

- **Subject**: o texto da linha de assunto da mensagem.

- **Tipo**: mostra se uma mensagem foi identificada como **spam**, **em massa**, **Phish**, corresponde a uma regra de fluxo de emails (**regra de transporte**) ou foi identificada como contendo **malware**.

- **Expira**: a data e a hora em que a mensagem será automaticamente excluída da quarentena.

- **Liberado para**: todos os endereços de email (se houver) para os quais a mensagem foi liberada.

- **Ainda não foi liberado para**: todos os endereços de email (se houver) para os quais a mensagem ainda não foi liberada.

### <a name="details-displayed-for-quarantined-files"></a>Detalhes exibidos para arquivos em quarentena

- **Nome do arquivo**: o nome do arquivo em quarentena.

- **Caminho do site**: URL que define o local do arquivo no Office 365.

- **Data/hora detectada**: a data e a hora em que o arquivo foi colocado em quarentena.

- **Expira**: a data em que a mensagem será excluída da quarentena.

- **Detectado por**: o método usado para detectar o malware no arquivo. Isso pode ser a ATP (proteção avançada contra ameaças) ou o mecanismo antimalware da Microsoft.

- **Lançamento**: descreve se o arquivo foi ou não liberado.

- **Nome do malware**: família e nome do malware detectado no arquivo.

- **ID do documento**: um identificador exclusivo para o documento.

- **Tamanho do arquivo**: o tamanho do arquivo em KB.

- **Organização**: a ID exclusiva da sua organização no Office 365.

- **Modificado por**: a conta corporativa ou de estudante do usuário que modificou o arquivo pela última vez.

- **Tamanho do arquivo**: o tamanho do arquivo em KB.

- **Hash SHA256**: o hash do arquivo. Você pode usá-lo para procurar outros repositórios de reputação que você pode ter ou investigar onde senão o arquivo pode estar em seu ambiente.

## <a name="manage-messages-and-files-in-quarantine"></a>Gerenciar mensagens e arquivos em quarentena

Após selecionar uma mensagem ou grupo de mensagens em quarentena, você tem várias opções para o que fazer com as mensagens:

- Não fazer nada: se você optar por não fazer nada, a mensagem será excluída pelo Office 365 automaticamente após a expiração. Por padrão, spam, massa, malware, phishing e mensagens em quarentena porque corresponderam a uma regra de fluxo de emails são mantidas em quarentena por 30 dias. Quando o Office 365 exclui uma mensagem da quarentena, não é possível obtê-la novamente. Se desejar, você pode alterar o período de retenção para mensagens em quarentena Configurando a configuração **reter spam para (dias)** em suas políticas antispam. Para obter mais informações, consulte a seção [definir o período de retenção de quarentena](#set-the-quarantine-retention-period) neste tópico.

- **Exibir cabeçalho da mensagem**: escolha este link para ver o texto do cabeçalho da mensagem. Para analisar o cabeçalho em camadas, copie o texto do cabeçalho da mensagem para a área de transferência e escolha **analisador de cabeçalho de mensagem da Microsoft** para ir para o analisador de conectividade remota (clique com o botão direito do mouse e escolha **abrir em uma nova guia** se não quiser deixar o Office 365 para concluir esta tarefa). Cole o cabeçalho da mensagem na página na seção analisador de cabeçalho de mensagem e escolha **analisar cabeçalhos**.

- **Visualizar mensagem**: permite que você veja versões brutas ou de HTML do corpo do texto da mensagem. No modo de exibição HTML, os links estão desabilitados.

- **Baixar mensagem** ou **baixar arquivo**: escolha esta opção para baixar uma cópia da mensagem ou arquivo para o dispositivo local. Você precisará confirmar se entendeu os riscos associados ao download de itens da quarentena antes que você possa fazer isso. As mensagens são salvas no formato. eml em uma pasta que você especificar. Os arquivos em quarentena são salvos em seu formato original.

- **Excluir**: se quiser, você pode excluir imediatamente um item em quarentena (ou conjunto de itens) em vez de esperar pela data de expiração definida pelo Office 365. Para excluir uma mensagem ou arquivo, na lista quarentena, selecione o item e, em seguida, escolha **excluir**. Para excluir vários itens de uma vez, marque a caixa de seleção à esquerda dos itens na lista quarentena e, em seguida, na página **ações em massa** exibida, escolha **excluir mensagens selecionadas** ou **Excluir arquivos selecionados**.

- **Versão**: Libere um item em quarentena (ou um conjunto de itens) e informe os itens como em quarentena de forma falsa (falsos positivos) à Microsoft.

  Para liberar e relatar uma única mensagem ou arquivo, na lista quarentena, selecione o item, escolha **liberar arquivo** ou **liberar mensagem**. Na próxima página, verifique se **as mensagens de relatório para a Microsoft para** análise ou **arquivos de relatório para a Microsoft para análise** estão selecionadas.

  Para liberar vários itens de uma vez, marque a caixa de seleção à esquerda dos itens na lista quarentena e, em seguida, na página **ações em massa** exibida, escolha **liberar arquivos** ou **liberar mensagens**. Na próxima página, verifique se **as mensagens de relatório para a Microsoft para** análise ou **arquivos de relatório para a Microsoft para análise** estão selecionadas.

Quando você estiver liberando mensagens, esteja ciente do seguinte:

- Quando você executa uma versão em massa de várias mensagens ao mesmo tempo, as mensagens são liberadas para todos os destinatários originalmente identificados. Se você só quiser liberar mensagens somente para destinatários específicos, precisará liberar as mensagens uma de cada vez e identificar os destinatários individualmente.

- Uma mensagem não pode ser liberada mais de uma vez para o mesmo destinatário.

- Quando você estiver liberando uma mensagem para mais de um destinatário, somente os destinatários que não receberam a mensagem aparecerão na lista de possíveis destinatários.

- Quando você optar por relatar falsos positivos, se a mensagem ou as mensagens liberadas forem colocadas em quarentena como spam, em massa, phishing ou como contendo malware, a mensagem também será relatada à equipe de análise de spam da Microsoft. A equipe avaliará e analisará a mensagem e, dependendo dos resultados da análise, as regras de filtro de conteúdo de spam de todo o serviço podem ser ajustadas para permitir a mensagem.

## <a name="set-the-quarantine-retention-period"></a>Definir o período de retenção de quarentena

Você pode configurar por quanto tempo as mensagens e os arquivos permanecerão em quarentena antes de expirarem. Por padrão, os itens em quarentena são mantidos por 30 dias. Você define essa configuração para cada política que criar. Você também pode modificar o valor da política padrão, conforme descrito neste artigo.

### <a name="modify-the-quarantine-retention-period-for-the-default-spam-filter-policy-in-the-security--compliance-center"></a>Modificar o período de retenção de quarentena para a política de filtro de spam padrão no centro de conformidade de & de segurança

1. [Abra o centro de conformidade & segurança](go-to-the-securitycompliance-center.md) e vá para **anti-spam**da **política** \> de **Gerenciamento** \> de ameaças.

   > [!TIP]
   > Para ir diretamente para a página **antispam** , use esta URL:[https://protection.office.com/?hash=/antispam](https://protection.office.com/?hash=/antispam)

2. Escolha **personalizado** para exibir a guia **configurações personalizadas** .

3. Expanda a linha **padrão da política de filtro de spam (AlwaysOn)** .

4. Escolha **Editar política**. As configurações da política de filtro de spam padrão aparecem em uma nova página.

5. Expanda **spam e ações em massa**.

6. Em **quarentena**, na caixa de texto **reter spam por (dias)** , insira a quantidade de tempo que você deseja que o Office 365 retenha mensagens e arquivos em quarentena. O padrão é 30 dias. Este também é o máximo.

7. Escolha **Salvar**.

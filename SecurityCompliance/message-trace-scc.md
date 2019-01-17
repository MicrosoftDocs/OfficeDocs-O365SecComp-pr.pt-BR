---
title: Rastreamento de mensagem no Centro de conformidade do & de segurança
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3e64f99d-ac33-4aba-91c5-9cb4ca476803
description: Os administradores podem usar o rastreamento de mensagens em que o Centro de conformidade do & de segurança para descobrir o que aconteceu com mensagens.
ms.openlocfilehash: 9dfdab4adc5caba55664e93b49c8428791670ab3
ms.sourcegitcommit: 25fb33a1f8b2844fde15f6c03db2936c610824e0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28685317"
---
# <a name="message-trace-in-the-security--compliance-center"></a>Rastreamento de mensagem no Centro de conformidade do & de segurança

Rastreamento de mensagem no Centro de conformidade do & de segurança segue mensagens de email, conforme elas viajam através de sua organização do Exchange Online. Você pode determinar se uma mensagem foi recebida, rejeitada, adiada ou entregue pelo serviço. Ele também mostra quais ações foram realizadas na mensagem antes de que atingiu seu status final.

Rastreamento de mensagem no Centro de conformidade do & de segurança melhora após o rastreamento de mensagem que estava disponível no Centro de administração do Exchange (EAC). Você pode usar as informações de rastreamento de mensagem para responder perguntas do usuário sobre o que aconteceu com suas mensagens com eficiência, solucionar problemas de fluxo de email e validar alterações de política.

## <a name="open-message-trace"></a>Rastreamento de mensagem aberta

1. [Entre no Office 365](https://support.office.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4) com sua conta corporativa ou de estudante.

2. Selecione o ícone do inicializador de aplicativos do ![Ícone inicializador de aplicativo do Office 365](media/0aaa6945-f9a4-4b13-bf5f-d5c5dbe978fb.png) no canto superior esquerdo e escolha **Administrador**.

3. No painel de navegação inferior esquerdo, expanda a **centrais de Admin** e selecione **segurança & conformidade**.

4. Na página **segurança & conformidade** que abre, expanda o **fluxo de emails**e selecione o **rastreamento de mensagens**.

## <a name="message-trace-page"></a>Página de rastreamento de mensagem

A partir daqui, você pode iniciar um novo rastreamento padrão clicando no botão **Iniciar um rastreamento** . Isso irá pesquisar para todas as mensagens de todos os remetentes e destinatários nos últimos dois dias. Ou você pode usar uma das consultas armazenadas entre as categorias de consulta disponíveis e uma executá-los como-está ou usá-las como ponto de partida para suas próprias consultas:

- **Padrão de consultas**: consultas internas fornecidas pelo Office 365.

- **Consultas personalizadas**: consultas salvas por administradores em sua organização para uso futuro.

- **Salva automaticamente consultas**: as últimos dez mais recentemente executar consultas. Esta lista simplifica a pegue onde você parou.

Também nesta página é uma seção **Downloadable relatórios** para as solicitações enviados, bem como os próprios relatórios quando há disponível para download.

## <a name="options-for-a-new-message-trace"></a>Opções para um novo rastreamento de mensagem

### <a name="filter-by-senders-and-recipients"></a>Filtrar por remetentes e destinatários

Os valores padrão são **todos os remetentes** e **todos os destinatários**, mas você pode usar os seguintes campos para filtrar os resultados:

- **Por essas pessoas**: clique neste campo para selecionar um ou mais remetentes da sua organização. Você também pode iniciar digitar um nome e os itens na lista serão filtrados pelo que você digitou, bem como se comporta como de uma página de pesquisa.

- **Para que essas pessoas**: clique neste campo para selecionar um ou mais destinatários na sua organização.

Você também pode digitar os endereços de email de destinatários e remetentes externos. Caracteres curinga é suportada (`*@contoso.com` ou `scot?@contoso.com`), mas você não pode usar várias entradas com curinga no mesmo campo ao mesmo tempo.

### <a name="time-range"></a>Intervalo de tempo

O valor padrão é **2 dias**, mas você pode especificar intervalos de data/hora de até 90 dias. Quando você usa os intervalos de data/hora, considere estas questões:

- Por padrão, você seleciona o intervalo de tempo no modo de exibição do **controle deslizante** usando uma linha de tempo. Só pode selecionar o dia ou configurações que são exibidas de tempo. Tentando selecionar um valor intermediária se encaixem bolha inicial/final para o mais próximo exibido a configuração.

   ![Um intervalo de tempo do controle deslizante em um novo rastreamento de mensagem no Centro de conformidade do & de segurança](media/55a9e9c1-f7d5-4047-b217-824e8b976bcb.png)

   Porém, você também pode alternar para modo de exibição **personalizado** onde você pode especificar os valores de **Data de início** e **Data de término** (incluindo vezes), e você também pode selecionar o **fuso horário** para o intervalo de data/hora. Observe que a definição de **fuso horário** se aplica ao seus entradas de consulta e os resultados da consulta.

   ![Um intervalo de tempo personalizado em um novo rastreamento de mensagem no Centro de conformidade do & de segurança](media/ed4c8d50-9ea5-4694-93f9-ee3ab6660b4f.png)

   Para 10 dias ou menos, os resultados estão disponíveis instantaneamente como um relatório de **Resumo** . Se você especificar um intervalo de tempo até mesmo ligeiramente maior do que 10 dias, os resultados serão atrasados conforme eles estão disponíveis apenas como um arquivo CSV de página de download (relatórios de **Resumo do Enhanced** ou **Extended** ).

   Para obter mais informações sobre os diferentes tipos de relatórios, consulte a seção de [tipo de relatório de escolher](#choose-report-type) neste tópico.

   **Observação**: relatórios de resumo e estendidos avançados preparados com dados de rastreamento de mensagem arquivada e pode levar várias horas antes que seu relatório está disponível para download. Dependendo de quantos outros administradores também enviaram solicitações de relatório ao mesmo tempo, você também poderá observar um atraso antes de processamento inicia para sua solicitação na fila.

- Salvar uma consulta no modo de exibição do **controle deslizante** salva o intervalo de tempo relativo (por exemplo, 3 dias a partir de hoje). Salvar uma consulta no modo de exibição **personalizado** salva o intervalo de data/hora absoluta (por exemplo, 2018-05-06 13:00 a 2018-05-08 18:00).

### <a name="more-search-options"></a>Mais opções de pesquisa

#### <a name="delivery-status"></a>Status de entrega

Você pode deixar o valor padrão, **todos os** selecionado ou você pode selecionar um dos seguintes valores para filtrar os resultados:

- **Entregue**: A mensagem foi entregue com êxito para o destino desejado.

- **Pendente**: entrega da mensagem está sendo uma tentativa ou uma nova tentativa.

- **Expanded**: um destinatário de grupo de distribuição expandido antes da entrega aos membros individuais do grupo.

- **Falha**: A mensagem não foi entregue.

- **Em quarentena**: A mensagem foi colocada em quarentena (como spam, emails em massa ou phishing). Para obter mais informações, consulte [mensagens de email de quarentena no Office 365](https://support.office.com/article/4c234874-015e-4768-8495-98fcccfc639b.aspx).

- **Filtrado como spam**: A mensagem foi identificada como spam e foi rejeitada ou bloqueado (não em quarentena).

- **Obter o status:** A mensagem foi recebida recentemente pelo Office 365, mas nenhum dado de status outros ainda está disponível. Verifique novamente em alguns minutos.

**Observação**: os valores de **filtro como spam** e **pendente,** **em quarentena**só estão disponíveis para pesquisas de menos de 10 dias. Além disso, pode haver um atraso de 5 a 10 minutos entre o status de entrega real e relatados.

#### <a name="message-id"></a>ID da mensagem

Esta é a ID de mensagem da internet (também conhecida como ID do cliente) encontrado no **Message-ID:** campo de cabeçalho no cabeçalho da mensagem. Os usuários podem dar esse valor para investigar mensagens específicas.

Esse valor é constante para o tempo de vida da mensagem. Para mensagens criadas no Office 365 ou Exchange, o valor está no formato `<GUID@ServerFQDN>`, incluindo os colchetes angulares (\< \>). Por exemplo, `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`. Outros sistemas de mensagens podem usar a sintaxe diferente ou valores. Este valor deve para ser exclusivo, mas nem todos os sistemas de email estritamente seguem esse requisito. Se o **Message-ID:** campo de cabeçalho não existe ou estiver em branco para mensagens recebidas de fontes externas, é atribuído a um valor arbitrário.

Quando você usa o **ID da mensagem** para filtrar os resultados, certifique-se de incluir a cadeia de caracteres completa, incluindo qualquer colchetes angulares.

#### <a name="direction"></a>Direção

Você pode deixar o valor padrão, **todos os** selecionado, ou você pode selecionar **entrada** (mensagens enviadas a destinatários na sua organização) ou **saída** (mensagens enviadas de usuários em sua organização) para filtrar os resultados.

#### <a name="original-client-ip-address"></a>Endereço IP do cliente original

Você pode arquivador os resultados por endereço IP do cliente para investigar violadas computadores que estão enviando grandes quantidades de spam ou malware. Embora as mensagens podem parecem ser originadas de vários remetentes, é provável que está gerando o mesmo computador, todas as mensagens.

**Observação**: as informações de endereço IP do cliente está disponíveis somente para 10 dias e só está disponíveis nos relatórios de **Resumo do Enhanced** ou **Extended** (página de download arquivos CSV).

### <a name="choose-report-type"></a>Escolha o tipo de relatório

Os tipos de relatório disponíveis são:

- **Resumo**: disponível se o intervalo de tempo é menor do que 10 dias e requer sem opções de filtragem adicionais. Os resultados estão disponíveis quase imediatamente após você clicar em **Pesquisar**.

- **Resumo do Enhanced** ou **Extended**: esses relatórios estão disponíveis apenas como arquivos CSV baixáveis e exigir uma ou mais das seguintes opções de filtragem, independentemente do intervalo de tempo: **por essas pessoas**, **para que essas pessoas**ou ** ID da mensagem**. Você pode usar caracteres curinga para os remetentes ou destinatários (por exemplo, \*@contoso.com).

**Observações**:

- Relatórios de resumo e estendidos avançados preparados com dados de rastreamento de mensagem arquivada e pode levar várias horas antes que seu relatório está disponível para download. Dependendo de quantos outros administradores também enviaram solicitações de relatório ao mesmo tempo, você também poderá observar um atraso antes de iniciar sua solicitação de na fila ser processado.

- Embora você possa selecionar um relatório de resumo ou estendidos avançada de qualquer intervalo de data/hora, comumente últimas quatro horas dos dados arquivados não ainda esteja disponível para esses dois tipos de relatórios.

Quando você clicar em **Avançar**, você verá uma página de resumo que lista as opções de filtragem que você selecionou, um título (editável) exclusivo para o relatório e o endereço de email que recebe a notificação quando o rastreamento de mensagem for concluído (também editável, e deve estar em um dos domínios aceitos de sua organização). Clique em **relatório de preparar** para enviar o rastreamento de mensagens. Em principal página de **rastreamento de mensagens** , você pode ver o status do relatório na seção **Downloadable relatórios** .

Para obter mais informações sobre as informações que são retornadas em diferentes tipos de relatório, consulte a próxima seção.

## <a name="message-trace-results"></a>Resultados de rastreamento de mensagem

Diferentes tipos de relatório retornam níveis diferentes de informações. As informações que estão disponíveis nos diferentes relatórios são descritas nas seções a seguir.

### <a name="summary-report-output"></a>Saída de relatório de resumo

Depois de executar o rastreamento de mensagens, os resultados serão listados, classificados por decrescente data/hora (primeiro mais recente).

![Resultados do relatório de resumo para rastreamento de mensagens em que o Centro de conformidade do & de segurança](media/0664bafe-0b03-477b-b571-0b046ac8c977.png)

O relatório de resumo contém as seguintes informações:

- **Data**: A data e hora em que a mensagem foi recebida pelo serviço, usando o fuso horário UTC configurado.

- **Remetente**: O endereço de email do remetente (*alias*@*domínio*).

- **Destinatário**: O endereço de email do destinatário ou destinatários. Para uma mensagem enviada a vários destinatários, há uma linha por destinatário. Se o destinatário é um grupo de distribuição, grupo dinâmico de distribuição ou grupo de segurança habilitados para email, o grupo será primeiro destinatário e, em seguida, cada membro do grupo está em uma linha separada.

- **Assunto**: os primeiros 256 caracteres da mensagem de **Assunto:** campo.

- **Status**: esses valores são descritos na seção [status de entrega](#delivery-status) .

Por padrão, os primeiros 250 resultados são carregados e prontamente disponível. Quando você rola para baixo, há uma pausa ligeiramente conforme o próximo lote de resultados são carregadas. Em vez de rolagem, você pode clicar **carregar todos** para carregar todos os resultados até um máximo de 10.000.

Você pode clicar nos cabeçalhos de coluna para classificar os resultados pelos valores essa coluna na ordem crescente ou decrescente.

Você pode clicar em **resultados de filtro** para filtrar os resultados por uma ou mais colunas.

Depois que você tiver selecionado uma ou mais linhas clicando em **exportar os resultados** e, em seguida, selecionando **Exportar selecionado**, **exportação carregado resultados**ou **Exportar todos os resultados**, você pode exportar os resultados.

#### <a name="find-related-records-for-this-message"></a>Localizar registros relacionados para esta mensagem

Registros de mensagem relacionadas são registros que compartilhados a mesma ID de mensagem. Lembre-se de que, até mesmo, uma única mensagem enviada entre duas pessoas pode gerar vários registros. O número de registros aumenta quando a mensagem é afetada por expansão de grupo de distribuição, encaminhamento, regras de fluxo de correio (também conhecido como regras de transporte), etc.

Depois de selecionar caixa de seleção de uma linha, você pode localizar registros relacionados para a mensagem clicando no botão **Localizar relacionados** que aparece, ou selecionando o **mais opções** ![mais](media/1ea52bbf-9d00-48ce-9362-307f7f6fb7fe.png) \> **Localizar registros relacionados para esta mensagem**).

Para obter mais informações sobre a ID da mensagem, consulte a seção ID da mensagem anteriormente neste tópico.

#### <a name="message-trace-details"></a>Detalhes do rastreamento de mensagem

Na saída do relatório de resumo, você pode exibir detalhes sobre uma mensagem usando um dos seguintes métodos:

- Selecione a linha (clique em qualquer lugar na linha, exceto a caixa de seleção).

- Marque a caixa de seleção da linha e clique em **mais opções** ![mais](media/1ea52bbf-9d00-48ce-9362-307f7f6fb7fe.png) \> **Exibir detalhes da mensagem**.

   ![Detalhes após clicando duas vezes em uma linha em que os resultados de rastreamento de mensagem de relatório de resumo no Centro de conformidade do & de segurança](media/e50ee7cd-810a-4c06-8b58-e56ffd7028d1.png)

Os detalhes de rastreamento de mensagem contêm as seguintes informações adicionais que não está presentes no relatório de resumo:

- **Eventos de mensagem**: Esta seção contém as classificações que ajudam a categorizar as ações que o serviço leva em mensagens. Estes são alguns dos eventos mais interessantes que você pode encontrar:

   - **Recebimento**: A mensagem foi recebida pelo serviço.

   - **Enviar**: A mensagem foi enviada pelo serviço.

   - **Falha**: A mensagem falhou ao ser entregue.

   - **Entregar**: A mensagem foi entregue a uma caixa de correio.

   - **Expandir**: A mensagem foi enviada a um grupo de distribuição que foi expandido.

   - **Transferir**: os destinatários foram movidos para uma mensagem bifurcada devido à conversão de conteúdo, limites de destinatário de mensagem ou agentes.

   - **Defer**: A entrega da mensagem foi adiada e pode ser nova tentativa mais tarde.

   - **Resolved**: A mensagem foi redirecionada para um novo endereço de destinatário com base em uma visão do Active Directory para cima. Quando isso acontece, o endereço do destinatário original é listado em uma linha separada no rastreamento de mensagem, juntamente com o status de entrega final da mensagem.

   Observe que mesmo uma mensagem normal for entregue com êxito irá gerar várias entradas de **evento** no rastreamento de mensagem.

- **Obter mais informações**: Esta seção contém os seguintes detalhes:

   - **ID da mensagem**: esse valor é descrito na seção a [ID da mensagem](#message-id) anteriormente neste tópico. Por exemplo, `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`.

   - **Tamanho da mensagem**

   - **De IP**: O endereço IP do computador que enviou a mensagem. Para mensagens de saída enviadas a partir do Exchange Online, este valor fica em branco.

   - **Para IP**: O endereço IP ou endereços de onde o serviço tentou entregar a mensagem. Se a mensagem tiver vários destinatários, elas serão exibidas. Para mensagens de entrada enviadas para o Exchange Online, esse valor estará vazio.

### <a name="enhanced-summary-reports"></a>Relatórios de resumo avançados

Relatórios resumidos de avançada (concluídos) disponíveis estão disponíveis na seção **Downloadable relatórios** no rastreamento de mensagens de início. As informações a seguir estão disponíveis no relatório:

- **origin_timestamp**<sup>*</sup>: A data e hora em que a mensagem inicialmente foi recebida pelo serviço, usando o fuso horário UTC configurado.

- **sender_address**: o endereço de email do remetente (*alias*@*domínio*).

- **Recipient_status**: O status da entrega da mensagem ao destinatário. Se a mensagem foi enviada para vários destinatários, ela mostrará todos os destinatários e o status correspondente para cada um, no formato: \< *endereço de email*\>##\<*status*\>. Por exemplo:

   - **Enviar ##Receive,** significa que a mensagem foi recebida pelo serviço e enviada ao destinatário.

   - **Falha de ##Receive,** significa que a mensagem foi recebida pelo serviço, mas entrega ao destinatário falhou.

   - **Entregar ##Receive,** significa que a mensagem foi recebida pelo serviço e foi entregue à caixa de correio do destinatário.

- **assunto_da_mensagem**: os primeiros 256 caracteres de campo de **assunto** da mensagem.

- **total_bytes**: O tamanho da mensagem em bytes, incluindo anexos.

- **identificação_da_mensagem**: esse valor é descrito na seção a [ID da mensagem](#message-id) anteriormente neste tópico. Por exemplo, `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`.

- **network_message_id**: um valor de ID de mensagem exclusiva que se mantêm em todas as cópias da mensagem que pode ser criado devido à expansão de grupo de distribuição ou bifurcação. Um valor de exemplo é `1341ac7b13fb42ab4d4408cf7f55890f`.

- **original_client_ip**: O endereço IP do cliente do remetente.

- **direcionalidade**: indica se a mensagem foi enviada internamente (1) na sua organização, ou se foi enviada para fora (2) da sua organização.

- **connector_id**: O nome do conector origem ou destino. Para obter mais informações sobre conectores no Exchange Online, consulte [Configurar o fluxo de email usando conectores no Office 365](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow).

- **delivery_priority**<sup>*</sup>: se a mensagem foi enviada com prioridade **alta**, **baixa**ou **Normal** .

<sup>*</sup>Essas propriedades só estão disponíveis em relatórios de resumo avançada.

### <a name="extended-reports"></a>Relatórios estendidos

Relatórios de Extended disponíveis (concluídos) estão disponíveis na seção **Downloadable relatórios** no início do rastreamento de mensagens. Praticamente todas as informações de um relatório de resumo avançada está disponível em um relatório de Extended (com exceção de **origin_timestamp** e **delivery_priority**). As seguintes informações adicionais só estão disponíveis em um relatório de Extended:

- **client_ip**: O endereço IP do servidor de email ou o cliente de mensagens que enviou a mensagem.

- **client_hostname**: O nome do host ou o FQDN do servidor de email ou o cliente de mensagens que enviou a mensagem.

- **server_ip**: O endereço IP do servidor de origem e destino.

- **server_hostname**: O nome do host ou o FQDN do servidor de destino.

- **source_context**: informações Extra associadas ao campo de **origem** . Por exemplo:

   - `Protocol Filter Agent`

   - `3489061114359050000`

- **origem**: O Exchange Online componente que é responsável pelo evento. Por exemplo:

   - `AGENT`

   - `MAILBOXRULE`

   - `SMTP`

- **identificação_de_evento**: esses correspondem aos valores de **evento de mensagem** que são explicados na seção [Localizar registros relacionados para esta mensagem](#find-related-records-for-this-message) .

- **internal_message_id**: um identificador de mensagem que é atribuído pelo servidor do Exchange Online que está processando a mensagem.

- **recipient_address**: os endereços de email dos destinatários da mensagem. Vários endereços de email são separados por vírgula (;).

- **recipient_count**: O número total de destinatários da mensagem.

- **related_recipient_address**: usado com `EXPAND`, `REDIRECT`, e `RESOLVE` endereços que estão associados a mensagem de email de eventos para exibir os demais destinatários.

- **referência**: este campo contém informações adicionais para tipos específicos de eventos. Por exemplo:

   - **DSN**: contém o link de relatório, que é o valor de **identificação_da_mensagem** da notificação de status de entrega associado (também conhecido como um DSN, o relatório de entrega, NDR ou mensagem de rejeição) se um DSN é gerado logo após este evento. Se essa for uma mensagem DSN, esse campo contém o valor de **identificação_da_mensagem** da mensagem original que o DSN foi gerado por.

   - **Expandir**: contém o valor de **related_recipient_address** das mensagens relacionados.

   - **Recebimento**: pode conter o valor de **identificação_da_mensagem** da mensagem relacionada se a mensagem foi gerada por outros processos (por exemplo, regras de caixa de entrada).

   - **Enviar**: contém o valor de **internal_message_id** de todas as mensagens DSN.

   - **Transferir**: contém o valor de **internal_message_id** da mensagem que está sendo bifurcada (por exemplo, por conversão de conteúdo, limites de destinatário de mensagem ou agentes).

   - **MAILBOXRULE**: contém o valor de **internal_message_id** da mensagem de entrada que causou a regra de caixa de entrada gerar a mensagem de saída.

   Para outros tipos de eventos, o campo geralmente está em branco.

- **return_path**: O endereço de email de retorno especificado pelo comando **MAIL FROM** que enviou a mensagem. Embora este campo nunca estiver vazio, ele pode ter o valor de endereço de remetente nulo representado como `<>`.

- **message_info**: informações adicionais sobre a mensagem. Por exemplo:

   - A data / hora de origem de mensagem em UTC para `DELIVER` e `SEND` eventos. A data / hora de origem é o horário quando a mensagem primeiro inseridos organização do Exchange Online. A data e hora em UTC é representada no formato de data / hora ISO 8601: `yyyy-mm-ddThh:mm:ss.fffZ`, onde `yyyy` = ano, `mm` = mês, `dd` = dia, `T` indica o início do componente de hora, `hh` = hora, `mm` = minuto, `ss` = segundo, `fff` = frações de um segundo, e `Z` significa `Zulu`, que é outra maneira para denotar UTC.

   - Erros de autenticação. Por exemplo, você pode ver o valor `11a` e o tipo de autenticação que foi usado quando ocorreu o erro de autenticação.

- **tenant_id**: um valor GUID que representa a organização do Exchange Online (por exemplo, `39238e87-b5ab-4ef6-a559-af54c6b07b42`).

- **original_server_ip**: O endereço IP do servidor original.

- **custom_data**: contém dados relacionados a tipos de evento específicos. Para obter mais informações, consulte as seções a seguir.

#### <a name="customdata-values"></a>valores de custom_data

O campo **custom_data** para um `AGENTINFO` evento é usado por uma variedade de operadores do Exchange Online para registrar em log detalhes de processamento de mensagens. Alguns dos agentes mais interessantes são descritos nas seções a seguir.

#### <a name="spam-filter-agent"></a>Agente de filtro de spam

Um valor de **custom_data** que começa com `S:SFA` é do agente de filtro de spam. Os principais detalhes são descritos na tabela a seguir:

|**Valor**|**Descrição**|
|:-----|:-----|
|`SFV=NSPM`|A mensagem foi marcada como não spam e enviada aos destinatários pretendidos.|
|`SFV=SPM`|O filtro de conteúdo marcou a mensagem como spam.|
|`SFV=BLK`|A filtragem foi ignorada e a mensagem foi bloqueada, pois originou-se em um remetente bloqueado.|
|`SFV=SKS`|A mensagem foi marcada como spam antes de ser processada pelo filtro de conteúdo. Isso inclui mensagens que atenderam a uma regra Transporte para marcá-la automaticamente como spam e ignorar toda filtragem adicional.|
|`SCL=<number>`|Para saber mais sobre os diferentes valores SCL e seu significado, veja [Níveis de confiança de spam](https://technet.microsoft.com/library/jj200686.aspx).|
|`PCL=<number>`|O valor do Nível de confiança de phishing (PCL) da mensagem. Podem ser interpretados da mesma maneira que os valores de SCL documentados em [Níveis de confiança de spam](https://technet.microsoft.com/library/jj200686.aspx).  |
|`DI=SB`|O remetente da mensagem foi bloqueado.|
|`DI=SQ`|A mensagem foi colocada em quarentena.|
|`DI=SD`|A mensagem foi excluída.|
|`DI=SJ`|A mensagem foi enviada para a pasta de lixo eletrônico do destinatário.|
|`DI=SN`|A mensagem foi roteada através do pool de entrega de risco mais alto. Para obter mais informações, consulte o [pool de alto risco de entrega para mensagens de saída](https://technet.microsoft.com/library/jj200746.aspx).|
|`DI=SO`|A mensagem foi roteada através do pool normal de entrega de saída.|
|' SFS = [a]|Busca de site Catalogado = [b]'|Isso indica que houve correspondência com regras de spam.|
|`IPV=CAL`|A mensagem foi permitida pelos filtros de spam porque o endereço IP estava especificado em uma Lista de Permissões de IP do filtro de conexão.|
|`H=<EHLOstring>`|A cadeia de caracteres HELO ou EHLO do servidor de email conectado.|
|`PTR=<ReverseDNS>`|O registro PTR do endereço IP de envio, também conhecido como o endereço de DNS reverso.|

Um valor de **custom_data** de exemplo para uma mensagem que é feita a filtragem de spam semelhante a esta:

`S:SFA=SUM|SFV=SPM|IPV=CAL|SRV=BULK|SFS=470454002|SFS=349001|SCL=9|SCORE=-1|LIST=0|DI=SN|RD=ftmail.inc.com|H=ftmail.inc.com|CIP=98.129.140.74|SFP=1501|ASF=1|CTRY=US|CLTCTRY=|LANG=en|LAT=287|LAT=260|LAT=18;`

#### <a name="malware-filter-agent"></a>Agente de filtro de malware

Um valor de **custom_data** que começa com `S:AMA` é do agente de filtro de malware. Os principais detalhes são descritos na tabela a seguir:

|**Valor**|**Descrição**|
|:-----|:-----|
|' AMA = SOMA|v=1|` or `AMA=EV|v = 1'|A mensagem foi determinada por conter malware. `SUM` indica que o malware poderia ter foi detectado por qualquer número de mecanismos. `EV` indica que o malware foi detectado por um mecanismo específico. Quando malware é detectado pelo mecanismo que isso dispara as ações subsequentes.|
|`Action=r`|A mensagem foi substituída.|
|`Action=p`|A mensagem foi ignorada.|
|`Action=d`|A mensagem foi adiada.|
|`Action=s`|A mensagem foi excluída.|
|`Action=st`|A mensagem foi ignorada.|
|`Action=sy`|A mensagem foi ignorada.|
|`Action=ni`|A mensagem foi rejeitada.|
|`Action=ne`|A mensagem foi rejeitada.|
|`Action=b`|A mensagem foi bloqueada.|
|`Name=<malware>`|O nome do malware foi detectado.|
|`File=<filename>`|O nome do arquivo que continha o malware.|

Um valor de **custom_data** de exemplo para uma mensagem que contenha malware tem esta aparência:

`S:AMA=SUM|v=1|action=b|error=|atch=1;S:AMA=EV|engine=M|v=1|sig=1.155.974.0|name=DOS/Test_File|file=filename;S:AMA=EV|engine=A|v=1|sig=201707282038|name=Test_File|file=filename`

#### <a name="transport-rule-agent"></a>Agente de regras de transporte

Um valor de **custom_data** que começa com`S:TRA` é do agente de regras de transporte para regras de fluxo de email (também conhecido como regras de transporte). Os principais detalhes são descritos na tabela a seguir:

|**Valor**|**Descrição**|
|:-----|:-----|
|' ETR|ruleId =<guid>`|A identificação da regra encontrou uma correspondência.|
|`St=<datetime>`|A data e hora em UTC quando ocorreu a correspondência da regra.|
|`Action=<ActionDefinition>`|A ação que foi aplicada. Para obter uma lista de ações disponíveis, consulte [Mail flow ações de regra no Exchange Online](https://technet.microsoft.com/library/jj919237.aspx).|
|`Mode=<Mode>`|O modo da regra. Valores válidos são:<br/>• **Impor**: todas as ações da regra serão impostas. <br/>• **Testar com dicas de política:**: dica de política qualquer ação será enviada, mas outras ações impositivas não serão realizadas em. <br/>• **Teste sem dicas de política**: ações serão listadas em um arquivo de log, mas os remetentes não serão notificados de nenhuma maneira e as ações impositivas não serão realizadas em.|

Um valor de **custom_data** de exemplo para uma mensagens que corresponde às condições de uma regra de fluxo de email tem esta aparência:

`S:TRA=ETR|ruleId=19a25eb2-3e43-4896-ad9e-47b6c359779d|st=7/17/2017 12:31:25 AM|action=ApplyHtmlDisclaimer|sev=1|mode=Enforce`

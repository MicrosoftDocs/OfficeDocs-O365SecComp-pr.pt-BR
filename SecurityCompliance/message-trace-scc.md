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
# <a name="message-trace-in-the-security--compliance-center"></a><span data-ttu-id="6d785-103">Rastreamento de mensagem no Centro de conformidade do & de segurança</span><span class="sxs-lookup"><span data-stu-id="6d785-103">Message trace in the Security & Compliance Center</span></span>

<span data-ttu-id="6d785-p101">Rastreamento de mensagem no Centro de conformidade do & de segurança segue mensagens de email, conforme elas viajam através de sua organização do Exchange Online. Você pode determinar se uma mensagem foi recebida, rejeitada, adiada ou entregue pelo serviço. Ele também mostra quais ações foram realizadas na mensagem antes de que atingiu seu status final.</span><span class="sxs-lookup"><span data-stu-id="6d785-p101">Message trace in the Security & Compliance Center follows email messages as they travel through your Exchange Online organization. You can determine if a message was received, rejected, deferred, or delivered by the service. It also shows what actions were taken on the message before it reached its final status.</span></span>

<span data-ttu-id="6d785-p102">Rastreamento de mensagem no Centro de conformidade do & de segurança melhora após o rastreamento de mensagem que estava disponível no Centro de administração do Exchange (EAC). Você pode usar as informações de rastreamento de mensagem para responder perguntas do usuário sobre o que aconteceu com suas mensagens com eficiência, solucionar problemas de fluxo de email e validar alterações de política.</span><span class="sxs-lookup"><span data-stu-id="6d785-p102">Message trace in the Security & Compliance Center improves upon message trace that was available in the Exchange admin center (EAC). You can use the information from message trace to efficiently answer user questions about what happened to their messages, troubleshoot mail flow issues, and validate policy changes.</span></span>

## <a name="open-message-trace"></a><span data-ttu-id="6d785-109">Rastreamento de mensagem aberta</span><span class="sxs-lookup"><span data-stu-id="6d785-109">Open message trace</span></span>

1. <span data-ttu-id="6d785-110">[Entre no Office 365](https://support.office.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4) com sua conta corporativa ou de estudante.</span><span class="sxs-lookup"><span data-stu-id="6d785-110">[Sign in to Office 365](https://support.office.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4) with your work or school account.</span></span>

2. <span data-ttu-id="6d785-111">Selecione o ícone do inicializador de aplicativos do ![Ícone inicializador de aplicativo do Office 365](media/0aaa6945-f9a4-4b13-bf5f-d5c5dbe978fb.png) no canto superior esquerdo e escolha **Administrador**.</span><span class="sxs-lookup"><span data-stu-id="6d785-111">Select the app launcher icon ![Office 365 app launcher icon](media/0aaa6945-f9a4-4b13-bf5f-d5c5dbe978fb.png) in the upper-left and choose **Admin**.</span></span>

3. <span data-ttu-id="6d785-112">No painel de navegação inferior esquerdo, expanda a **centrais de Admin** e selecione **segurança & conformidade**.</span><span class="sxs-lookup"><span data-stu-id="6d785-112">In the lower-left navigation, expand **Admin centers** and select **Security & Compliance**.</span></span>

4. <span data-ttu-id="6d785-113">Na página **segurança & conformidade** que abre, expanda o **fluxo de emails**e selecione o **rastreamento de mensagens**.</span><span class="sxs-lookup"><span data-stu-id="6d785-113">In the **Security & Compliance** page that opens, expand **Mail flow**, and select **Message trace**.</span></span>

## <a name="message-trace-page"></a><span data-ttu-id="6d785-114">Página de rastreamento de mensagem</span><span class="sxs-lookup"><span data-stu-id="6d785-114">Message trace page</span></span>

<span data-ttu-id="6d785-p103">A partir daqui, você pode iniciar um novo rastreamento padrão clicando no botão **Iniciar um rastreamento** . Isso irá pesquisar para todas as mensagens de todos os remetentes e destinatários nos últimos dois dias. Ou você pode usar uma das consultas armazenadas entre as categorias de consulta disponíveis e uma executá-los como-está ou usá-las como ponto de partida para suas próprias consultas:</span><span class="sxs-lookup"><span data-stu-id="6d785-p103">From here you can start a new default trace by clicking on the **Start a trace** button. This will search for all messages for all senders and recipients for the last two days. Or you can use one of the stored queries from the available query categories and either run them as-is or use them as starting points for your own queries:</span></span>

- <span data-ttu-id="6d785-118">**Padrão de consultas**: consultas internas fornecidas pelo Office 365.</span><span class="sxs-lookup"><span data-stu-id="6d785-118">**Default queries**: Built-in queries provided by Office 365.</span></span>

- <span data-ttu-id="6d785-119">**Consultas personalizadas**: consultas salvas por administradores em sua organização para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="6d785-119">**Custom queries**: Queries saved by admins in your organization for future use.</span></span>

- <span data-ttu-id="6d785-p104">**Salva automaticamente consultas**: as últimos dez mais recentemente executar consultas. Esta lista simplifica a pegue onde você parou.</span><span class="sxs-lookup"><span data-stu-id="6d785-p104">**Autosaved queries**: The last ten most recently run queries. This list makes it simple to pick up where you left off.</span></span>

<span data-ttu-id="6d785-122">Também nesta página é uma seção **Downloadable relatórios** para as solicitações enviados, bem como os próprios relatórios quando há disponível para download.</span><span class="sxs-lookup"><span data-stu-id="6d785-122">Also on this page is a **Downloadable reports** section for the requests you've submitted, as well as the reports themselves when they're are available for download.</span></span>

## <a name="options-for-a-new-message-trace"></a><span data-ttu-id="6d785-123">Opções para um novo rastreamento de mensagem</span><span class="sxs-lookup"><span data-stu-id="6d785-123">Options for a new message trace</span></span>

### <a name="filter-by-senders-and-recipients"></a><span data-ttu-id="6d785-124">Filtrar por remetentes e destinatários</span><span class="sxs-lookup"><span data-stu-id="6d785-124">Filter by senders and recipients</span></span>

<span data-ttu-id="6d785-125">Os valores padrão são **todos os remetentes** e **todos os destinatários**, mas você pode usar os seguintes campos para filtrar os resultados:</span><span class="sxs-lookup"><span data-stu-id="6d785-125">The default values are **All senders** and **All recipients**, but you can use the following fields to filter the results:</span></span>

- <span data-ttu-id="6d785-p105">**Por essas pessoas**: clique neste campo para selecionar um ou mais remetentes da sua organização. Você também pode iniciar digitar um nome e os itens na lista serão filtrados pelo que você digitou, bem como se comporta como de uma página de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="6d785-p105">**By these people**: Click in this field to select one or more senders from your organization. You can also start to type a name and the items in the list will be filtered by what you've typed, much like how a search page behaves.</span></span>

- <span data-ttu-id="6d785-128">**Para que essas pessoas**: clique neste campo para selecionar um ou mais destinatários na sua organização.</span><span class="sxs-lookup"><span data-stu-id="6d785-128">**To these people**: Click in this field to select one or more recipients in your organization.</span></span>

<span data-ttu-id="6d785-p106">Você também pode digitar os endereços de email de destinatários e remetentes externos. Caracteres curinga é suportada (`*@contoso.com` ou `scot?@contoso.com`), mas você não pode usar várias entradas com curinga no mesmo campo ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="6d785-p106">You can also type the email addresses of external senders and recipients. Wildcards are supported (`*@contoso.com` or `scot?@contoso.com`), but you can't use multiple wildcard entries in the same field at the same time.</span></span>

### <a name="time-range"></a><span data-ttu-id="6d785-131">Intervalo de tempo</span><span class="sxs-lookup"><span data-stu-id="6d785-131">Time range</span></span>

<span data-ttu-id="6d785-p107">O valor padrão é **2 dias**, mas você pode especificar intervalos de data/hora de até 90 dias. Quando você usa os intervalos de data/hora, considere estas questões:</span><span class="sxs-lookup"><span data-stu-id="6d785-p107">The default value is **2 days**, but you can specify date/time ranges of up to 90 days. When you use date/time ranges, consider these issues:</span></span>

- <span data-ttu-id="6d785-p108">Por padrão, você seleciona o intervalo de tempo no modo de exibição do **controle deslizante** usando uma linha de tempo. Só pode selecionar o dia ou configurações que são exibidas de tempo. Tentando selecionar um valor intermediária se encaixem bolha inicial/final para o mais próximo exibido a configuração.</span><span class="sxs-lookup"><span data-stu-id="6d785-p108">By default, you select the time range in **Slider** view using a time line. You can only select the day or time settings that are displayed. Trying to select an in-between value will snap the start/end bubble to the nearest displayed setting.</span></span>

   ![Um intervalo de tempo do controle deslizante em um novo rastreamento de mensagem no Centro de conformidade do & de segurança](media/55a9e9c1-f7d5-4047-b217-824e8b976bcb.png)

   <span data-ttu-id="6d785-p109">Porém, você também pode alternar para modo de exibição **personalizado** onde você pode especificar os valores de **Data de início** e **Data de término** (incluindo vezes), e você também pode selecionar o **fuso horário** para o intervalo de data/hora. Observe que a definição de **fuso horário** se aplica ao seus entradas de consulta e os resultados da consulta.</span><span class="sxs-lookup"><span data-stu-id="6d785-p109">But, you can also switch to **Custom** view where you can specify the **Start date** and **End date** values (including times), and you can also select the **Time zone** for the date/time range. Note that the **Time zone** setting applies to both your query inputs and your query results.</span></span>

   ![Um intervalo de tempo personalizado em um novo rastreamento de mensagem no Centro de conformidade do & de segurança](media/ed4c8d50-9ea5-4694-93f9-ee3ab6660b4f.png)

   <span data-ttu-id="6d785-p110">Para 10 dias ou menos, os resultados estão disponíveis instantaneamente como um relatório de **Resumo** . Se você especificar um intervalo de tempo até mesmo ligeiramente maior do que 10 dias, os resultados serão atrasados conforme eles estão disponíveis apenas como um arquivo CSV de página de download (relatórios de **Resumo do Enhanced** ou **Extended** ).</span><span class="sxs-lookup"><span data-stu-id="6d785-p110">For 10 days or less, the results are available instantly as a **Summary** report. If you specify a time range that's even slightly greater than 10 days, the results will be delayed as they are only available as a downloadable CSV file ( **Enhanced summary** or **Extended** reports).</span></span>

   <span data-ttu-id="6d785-143">Para obter mais informações sobre os diferentes tipos de relatórios, consulte a seção de [tipo de relatório de escolher](#choose-report-type) neste tópico.</span><span class="sxs-lookup"><span data-stu-id="6d785-143">For more information about the different report types, see the [Choose report type](#choose-report-type) section in this topic.</span></span>

   <span data-ttu-id="6d785-p111">**Observação**: relatórios de resumo e estendidos avançados preparados com dados de rastreamento de mensagem arquivada e pode levar várias horas antes que seu relatório está disponível para download. Dependendo de quantos outros administradores também enviaram solicitações de relatório ao mesmo tempo, você também poderá observar um atraso antes de processamento inicia para sua solicitação na fila.</span><span class="sxs-lookup"><span data-stu-id="6d785-p111">**Note**: Enhanced summary and Extended reports are prepared using archived message trace data, and it can take up to several hours before your report is available for download. Depending on how many other admins have also submitted report requests around the same time, you might also notice a delay before processing starts for your queued request.</span></span>

- <span data-ttu-id="6d785-p112">Salvar uma consulta no modo de exibição do **controle deslizante** salva o intervalo de tempo relativo (por exemplo, 3 dias a partir de hoje). Salvar uma consulta no modo de exibição **personalizado** salva o intervalo de data/hora absoluta (por exemplo, 2018-05-06 13:00 a 2018-05-08 18:00).</span><span class="sxs-lookup"><span data-stu-id="6d785-p112">Saving a query in **Slider** view saves the relative time range (for example, 3 days from today). Saving a query in **Custom** view saves the absolute date/time range (for example, 2018-05-06 13:00 to 2018-05-08 18:00).</span></span>

### <a name="more-search-options"></a><span data-ttu-id="6d785-148">Mais opções de pesquisa</span><span class="sxs-lookup"><span data-stu-id="6d785-148">More search options</span></span>

#### <a name="delivery-status"></a><span data-ttu-id="6d785-149">Status de entrega</span><span class="sxs-lookup"><span data-stu-id="6d785-149">Delivery status</span></span>

<span data-ttu-id="6d785-150">Você pode deixar o valor padrão, **todos os** selecionado ou você pode selecionar um dos seguintes valores para filtrar os resultados:</span><span class="sxs-lookup"><span data-stu-id="6d785-150">You can leave the default value **All** selected, or you can select one of the following values to filter the results:</span></span>

- <span data-ttu-id="6d785-151">**Entregue**: A mensagem foi entregue com êxito para o destino desejado.</span><span class="sxs-lookup"><span data-stu-id="6d785-151">**Delivered**: The message was successfully delivered to the intended destination.</span></span>

- <span data-ttu-id="6d785-152">**Pendente**: entrega da mensagem está sendo uma tentativa ou uma nova tentativa.</span><span class="sxs-lookup"><span data-stu-id="6d785-152">**Pending**: Delivery of the message is being attempted or re-attempted.</span></span>

- <span data-ttu-id="6d785-153">**Expanded**: um destinatário de grupo de distribuição expandido antes da entrega aos membros individuais do grupo.</span><span class="sxs-lookup"><span data-stu-id="6d785-153">**Expanded**: A distribution group recipient was expanded before delivery to the individual members of the group.</span></span>

- <span data-ttu-id="6d785-154">**Falha**: A mensagem não foi entregue.</span><span class="sxs-lookup"><span data-stu-id="6d785-154">**Failed**: The message was not delivered.</span></span>

- <span data-ttu-id="6d785-p113">**Em quarentena**: A mensagem foi colocada em quarentena (como spam, emails em massa ou phishing). Para obter mais informações, consulte [mensagens de email de quarentena no Office 365](https://support.office.com/article/4c234874-015e-4768-8495-98fcccfc639b.aspx).</span><span class="sxs-lookup"><span data-stu-id="6d785-p113">**Quarantined**: The message was quarantined (as spam, bulk mail, or phishing). For more information, see [Quarantine email messages in Office 365](https://support.office.com/article/4c234874-015e-4768-8495-98fcccfc639b.aspx).</span></span>

- <span data-ttu-id="6d785-157">**Filtrado como spam**: A mensagem foi identificada como spam e foi rejeitada ou bloqueado (não em quarentena).</span><span class="sxs-lookup"><span data-stu-id="6d785-157">**Filtered as spam**: The message was identified spam, and was rejected or blocked (not quarantined).</span></span>

- <span data-ttu-id="6d785-p114">**Obter o status:** A mensagem foi recebida recentemente pelo Office 365, mas nenhum dado de status outros ainda está disponível. Verifique novamente em alguns minutos.</span><span class="sxs-lookup"><span data-stu-id="6d785-p114">**Getting status:** The message was recently received by Office 365, but no other status data is yet available. Check back in a few minutes.</span></span>

<span data-ttu-id="6d785-p115">**Observação**: os valores de **filtro como spam** e **pendente,** **em quarentena**só estão disponíveis para pesquisas de menos de 10 dias. Além disso, pode haver um atraso de 5 a 10 minutos entre o status de entrega real e relatados.</span><span class="sxs-lookup"><span data-stu-id="6d785-p115">**Note**: The values **Pending,** **Quarantined**, and **Filter as spam** are only available for searches less than 10 days. Also, there might be a 5 to 10 minute delay between the actual and reported delivery status.</span></span>

#### <a name="message-id"></a><span data-ttu-id="6d785-162">ID da mensagem</span><span class="sxs-lookup"><span data-stu-id="6d785-162">Message ID</span></span>

<span data-ttu-id="6d785-p116">Esta é a ID de mensagem da internet (também conhecida como ID do cliente) encontrado no **Message-ID:** campo de cabeçalho no cabeçalho da mensagem. Os usuários podem dar esse valor para investigar mensagens específicas.</span><span class="sxs-lookup"><span data-stu-id="6d785-p116">This is the internet message ID (also known as the Client ID) that's found in the **Message-ID:** header field in the message header. Users can give you this value to investigate specific messages.</span></span>

<span data-ttu-id="6d785-p117">Esse valor é constante para o tempo de vida da mensagem. Para mensagens criadas no Office 365 ou Exchange, o valor está no formato `<GUID@ServerFQDN>`, incluindo os colchetes angulares (\< \>). Por exemplo, `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`. Outros sistemas de mensagens podem usar a sintaxe diferente ou valores. Este valor deve para ser exclusivo, mas nem todos os sistemas de email estritamente seguem esse requisito. Se o **Message-ID:** campo de cabeçalho não existe ou estiver em branco para mensagens recebidas de fontes externas, é atribuído a um valor arbitrário.</span><span class="sxs-lookup"><span data-stu-id="6d785-p117">This value is constant for the lifetime of the message. For messages created in Office 365 or Exchange, the value is in the format `<GUID@ServerFQDN>`, including the angle brackets (\< \>). For example, `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`. Other messaging systems might use different syntax or values. This value is supposed to be unique, but not all email systems strictly follow this requirement. If the **Message-ID:** header field doesn't exist or is blank for incoming messages from external sources, an arbitrary value is assigned.</span></span>

<span data-ttu-id="6d785-171">Quando você usa o **ID da mensagem** para filtrar os resultados, certifique-se de incluir a cadeia de caracteres completa, incluindo qualquer colchetes angulares.</span><span class="sxs-lookup"><span data-stu-id="6d785-171">When you use **Message ID** to filter the results, be sure to include the full string, including any angle brackets.</span></span>

#### <a name="direction"></a><span data-ttu-id="6d785-172">Direção</span><span class="sxs-lookup"><span data-stu-id="6d785-172">Direction</span></span>

<span data-ttu-id="6d785-173">Você pode deixar o valor padrão, **todos os** selecionado, ou você pode selecionar **entrada** (mensagens enviadas a destinatários na sua organização) ou **saída** (mensagens enviadas de usuários em sua organização) para filtrar os resultados.</span><span class="sxs-lookup"><span data-stu-id="6d785-173">You can leave the default value **All** selected, or you can select **Inbound** (messages sent to recipients in your organization) or **Outbound** (messages sent from users in your organization) to filter the results.</span></span>

#### <a name="original-client-ip-address"></a><span data-ttu-id="6d785-174">Endereço IP do cliente original</span><span class="sxs-lookup"><span data-stu-id="6d785-174">Original client IP address</span></span>

<span data-ttu-id="6d785-p118">Você pode arquivador os resultados por endereço IP do cliente para investigar violadas computadores que estão enviando grandes quantidades de spam ou malware. Embora as mensagens podem parecem ser originadas de vários remetentes, é provável que está gerando o mesmo computador, todas as mensagens.</span><span class="sxs-lookup"><span data-stu-id="6d785-p118">You can filer the results by client IP address to investigate hacked computers that are sending large amounts of spam or malware. Although the messages might appear to come from multiple senders, it's likely that the same computer is generating all of the messages.</span></span>

<span data-ttu-id="6d785-177">**Observação**: as informações de endereço IP do cliente está disponíveis somente para 10 dias e só está disponíveis nos relatórios de **Resumo do Enhanced** ou **Extended** (página de download arquivos CSV).</span><span class="sxs-lookup"><span data-stu-id="6d785-177">**Note**: The client IP address information is only available for 10 days, and is only available in the **Enhanced summary** or **Extended** reports (downloadable CSV files).</span></span>

### <a name="choose-report-type"></a><span data-ttu-id="6d785-178">Escolha o tipo de relatório</span><span class="sxs-lookup"><span data-stu-id="6d785-178">Choose report type</span></span>

<span data-ttu-id="6d785-179">Os tipos de relatório disponíveis são:</span><span class="sxs-lookup"><span data-stu-id="6d785-179">The available report types are:</span></span>

- <span data-ttu-id="6d785-p119">**Resumo**: disponível se o intervalo de tempo é menor do que 10 dias e requer sem opções de filtragem adicionais. Os resultados estão disponíveis quase imediatamente após você clicar em **Pesquisar**.</span><span class="sxs-lookup"><span data-stu-id="6d785-p119">**Summary**: Available if the time range is less than 10 days, and requires no additional filtering options. The results are available almost immediately after you click **Search**.</span></span>

- <span data-ttu-id="6d785-p120">**Resumo do Enhanced** ou **Extended**: esses relatórios estão disponíveis apenas como arquivos CSV baixáveis e exigir uma ou mais das seguintes opções de filtragem, independentemente do intervalo de tempo: **por essas pessoas**, **para que essas pessoas**ou \*\* ID da mensagem\*\*. Você pode usar caracteres curinga para os remetentes ou destinatários (por exemplo, \*@contoso.com).</span><span class="sxs-lookup"><span data-stu-id="6d785-p120">**Enhanced summary** or **Extended**: These reports are only available as downloadable CSV files, and require one or more of the following filtering options regardless of the time range: **By these people**, **To these people**, or **Message ID**. You can use wildcards for the senders or the recipients (for example, \*@contoso.com).</span></span>

<span data-ttu-id="6d785-184">**Observações**:</span><span class="sxs-lookup"><span data-stu-id="6d785-184">**Notes**:</span></span>

- <span data-ttu-id="6d785-p121">Relatórios de resumo e estendidos avançados preparados com dados de rastreamento de mensagem arquivada e pode levar várias horas antes que seu relatório está disponível para download. Dependendo de quantos outros administradores também enviaram solicitações de relatório ao mesmo tempo, você também poderá observar um atraso antes de iniciar sua solicitação de na fila ser processado.</span><span class="sxs-lookup"><span data-stu-id="6d785-p121">Enhanced summary and Extended reports are prepared using archived message trace data, and it can take up to several hours before your report is available to download. Depending on how many other admins have also submitted report requests around the same time, you might also notice a delay before your queued request starts to be processed.</span></span>

- <span data-ttu-id="6d785-187">Embora você possa selecionar um relatório de resumo ou estendidos avançada de qualquer intervalo de data/hora, comumente últimas quatro horas dos dados arquivados não ainda esteja disponível para esses dois tipos de relatórios.</span><span class="sxs-lookup"><span data-stu-id="6d785-187">While you can select an Enhanced summary or Extended report for any date/time range, commonly the last four hours of archived data will not yet be available for these two types of reports.</span></span>

<span data-ttu-id="6d785-p122">Quando você clicar em **Avançar**, você verá uma página de resumo que lista as opções de filtragem que você selecionou, um título (editável) exclusivo para o relatório e o endereço de email que recebe a notificação quando o rastreamento de mensagem for concluído (também editável, e deve estar em um dos domínios aceitos de sua organização). Clique em **relatório de preparar** para enviar o rastreamento de mensagens. Em principal página de **rastreamento de mensagens** , você pode ver o status do relatório na seção **Downloadable relatórios** .</span><span class="sxs-lookup"><span data-stu-id="6d785-p122">When you click **Next**, you're presented with a summary page that lists the filtering options that you selected, a unique (editable) title for the report, and the email address that receives the notification when the message trace completes (also editable, and must be in one of your organization's accepted domains). Click **Prepare report** to submit the message trace. On the main **Message trace** page, you can see the status of the report in the **Downloadable reports** section.</span></span>

<span data-ttu-id="6d785-191">Para obter mais informações sobre as informações que são retornadas em diferentes tipos de relatório, consulte a próxima seção.</span><span class="sxs-lookup"><span data-stu-id="6d785-191">For more information about the information that's returned in the different report types, see the next section.</span></span>

## <a name="message-trace-results"></a><span data-ttu-id="6d785-192">Resultados de rastreamento de mensagem</span><span class="sxs-lookup"><span data-stu-id="6d785-192">Message trace results</span></span>

<span data-ttu-id="6d785-p123">Diferentes tipos de relatório retornam níveis diferentes de informações. As informações que estão disponíveis nos diferentes relatórios são descritas nas seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="6d785-p123">The different report types return different levels of information. The information that's available in the different reports is described in the following sections.</span></span>

### <a name="summary-report-output"></a><span data-ttu-id="6d785-195">Saída de relatório de resumo</span><span class="sxs-lookup"><span data-stu-id="6d785-195">Summary report output</span></span>

<span data-ttu-id="6d785-196">Depois de executar o rastreamento de mensagens, os resultados serão listados, classificados por decrescente data/hora (primeiro mais recente).</span><span class="sxs-lookup"><span data-stu-id="6d785-196">After running the message trace, the results will be listed, sorted by descending date/time (most recent first).</span></span>

![Resultados do relatório de resumo para rastreamento de mensagens em que o Centro de conformidade do & de segurança](media/0664bafe-0b03-477b-b571-0b046ac8c977.png)

<span data-ttu-id="6d785-198">O relatório de resumo contém as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="6d785-198">The summary report contains the following information:</span></span>

- <span data-ttu-id="6d785-199">**Data**: A data e hora em que a mensagem foi recebida pelo serviço, usando o fuso horário UTC configurado.</span><span class="sxs-lookup"><span data-stu-id="6d785-199">**Date**: The date and time at which the message was received by the service, using the configured UTC time zone.</span></span>

- <span data-ttu-id="6d785-200">**Remetente**: O endereço de email do remetente (*alias*@*domínio*).</span><span class="sxs-lookup"><span data-stu-id="6d785-200">**Sender**: The email address of the sender (*alias*@*domain*).</span></span>

- <span data-ttu-id="6d785-p124">**Destinatário**: O endereço de email do destinatário ou destinatários. Para uma mensagem enviada a vários destinatários, há uma linha por destinatário. Se o destinatário é um grupo de distribuição, grupo dinâmico de distribuição ou grupo de segurança habilitados para email, o grupo será primeiro destinatário e, em seguida, cada membro do grupo está em uma linha separada.</span><span class="sxs-lookup"><span data-stu-id="6d785-p124">**Recipient**: The email address of the recipient or recipients. For a message sent to multiple recipients, there's one line per recipient. If the recipient is a distribution group, dynamic distribution group, or mail-enabled security group, the group will be the first recipient, and then each member of the group is on a separate line.</span></span>

- <span data-ttu-id="6d785-204">**Assunto**: os primeiros 256 caracteres da mensagem de **Assunto:** campo.</span><span class="sxs-lookup"><span data-stu-id="6d785-204">**Subject**: The first 256 characters of the message's **Subject:** field.</span></span>

- <span data-ttu-id="6d785-205">**Status**: esses valores são descritos na seção [status de entrega](#delivery-status) .</span><span class="sxs-lookup"><span data-stu-id="6d785-205">**Status**: These values are described in the [Delivery status](#delivery-status) section.</span></span>

<span data-ttu-id="6d785-p125">Por padrão, os primeiros 250 resultados são carregados e prontamente disponível. Quando você rola para baixo, há uma pausa ligeiramente conforme o próximo lote de resultados são carregadas. Em vez de rolagem, você pode clicar **carregar todos** para carregar todos os resultados até um máximo de 10.000.</span><span class="sxs-lookup"><span data-stu-id="6d785-p125">By default, the first 250 results are loaded and readily available. When you scroll down, there's a slight pause as the next batch of results are loaded. Instead of scrolling, you can click **Load all** to load all of the results up to a maximum of 10,000.</span></span>

<span data-ttu-id="6d785-209">Você pode clicar nos cabeçalhos de coluna para classificar os resultados pelos valores essa coluna na ordem crescente ou decrescente.</span><span class="sxs-lookup"><span data-stu-id="6d785-209">You can click on the column headers to sort the results by the values in that column in ascending or descending order.</span></span>

<span data-ttu-id="6d785-210">Você pode clicar em **resultados de filtro** para filtrar os resultados por uma ou mais colunas.</span><span class="sxs-lookup"><span data-stu-id="6d785-210">You can click **Filter results** to filter the results by one or more columns.</span></span>

<span data-ttu-id="6d785-211">Depois que você tiver selecionado uma ou mais linhas clicando em **exportar os resultados** e, em seguida, selecionando **Exportar selecionado**, **exportação carregado resultados**ou **Exportar todos os resultados**, você pode exportar os resultados.</span><span class="sxs-lookup"><span data-stu-id="6d785-211">You can export the results after you've selected one or more rows by clicking **Export results** and then selecting **Export all results**, **Export loaded results**, or **Export selected**.</span></span>

#### <a name="find-related-records-for-this-message"></a><span data-ttu-id="6d785-212">Localizar registros relacionados para esta mensagem</span><span class="sxs-lookup"><span data-stu-id="6d785-212">Find related records for this message</span></span>

<span data-ttu-id="6d785-p126">Registros de mensagem relacionadas são registros que compartilhados a mesma ID de mensagem. Lembre-se de que, até mesmo, uma única mensagem enviada entre duas pessoas pode gerar vários registros. O número de registros aumenta quando a mensagem é afetada por expansão de grupo de distribuição, encaminhamento, regras de fluxo de correio (também conhecido como regras de transporte), etc.</span><span class="sxs-lookup"><span data-stu-id="6d785-p126">Related message records are records that shared the same Message ID. Remember, even a single message sent between two people can generate multiple records. The number of records increases when the message is affected by distribution group expansion, forwarding, mail flow rules (also known as transport rules), etc.</span></span>

<span data-ttu-id="6d785-216">Depois de selecionar caixa de seleção de uma linha, você pode localizar registros relacionados para a mensagem clicando no botão **Localizar relacionados** que aparece, ou selecionando o **mais opções** ![mais](media/1ea52bbf-9d00-48ce-9362-307f7f6fb7fe.png) \> **Localizar registros relacionados para esta mensagem**).</span><span class="sxs-lookup"><span data-stu-id="6d785-216">After you select a row's check box, you can find related records for the message by clicking the **Find related** button that appears, or by selecting **More options** ![More](media/1ea52bbf-9d00-48ce-9362-307f7f6fb7fe.png) \> **Find related records for this message**).</span></span>

<span data-ttu-id="6d785-217">Para obter mais informações sobre a ID da mensagem, consulte a seção ID da mensagem anteriormente neste tópico.</span><span class="sxs-lookup"><span data-stu-id="6d785-217">For more information about the Message ID, see the Message ID section earlier in this topic.</span></span>

#### <a name="message-trace-details"></a><span data-ttu-id="6d785-218">Detalhes do rastreamento de mensagem</span><span class="sxs-lookup"><span data-stu-id="6d785-218">Message trace details</span></span>

<span data-ttu-id="6d785-219">Na saída do relatório de resumo, você pode exibir detalhes sobre uma mensagem usando um dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="6d785-219">In the summary report output, you can view details about a message by using either of the following methods:</span></span>

- <span data-ttu-id="6d785-220">Selecione a linha (clique em qualquer lugar na linha, exceto a caixa de seleção).</span><span class="sxs-lookup"><span data-stu-id="6d785-220">Select the row (click anywhere in the row except the check box).</span></span>

- <span data-ttu-id="6d785-221">Marque a caixa de seleção da linha e clique em **mais opções** ![mais](media/1ea52bbf-9d00-48ce-9362-307f7f6fb7fe.png) \> **Exibir detalhes da mensagem**.</span><span class="sxs-lookup"><span data-stu-id="6d785-221">Select the row's check box and click **More options** ![More](media/1ea52bbf-9d00-48ce-9362-307f7f6fb7fe.png) \> **View message details**.</span></span>

   ![Detalhes após clicando duas vezes em uma linha em que os resultados de rastreamento de mensagem de relatório de resumo no Centro de conformidade do & de segurança](media/e50ee7cd-810a-4c06-8b58-e56ffd7028d1.png)

<span data-ttu-id="6d785-223">Os detalhes de rastreamento de mensagem contêm as seguintes informações adicionais que não está presentes no relatório de resumo:</span><span class="sxs-lookup"><span data-stu-id="6d785-223">The message trace details contain the following additional information that's not present in the summary report:</span></span>

- <span data-ttu-id="6d785-p127">**Eventos de mensagem**: Esta seção contém as classificações que ajudam a categorizar as ações que o serviço leva em mensagens. Estes são alguns dos eventos mais interessantes que você pode encontrar:</span><span class="sxs-lookup"><span data-stu-id="6d785-p127">**Message events**: This section contains classifications that help categorize the actions that the service takes on messages. Some of the more interesting events that you might encounter are:</span></span>

   - <span data-ttu-id="6d785-226">**Recebimento**: A mensagem foi recebida pelo serviço.</span><span class="sxs-lookup"><span data-stu-id="6d785-226">**Receive**: The message was received by the service.</span></span>

   - <span data-ttu-id="6d785-227">**Enviar**: A mensagem foi enviada pelo serviço.</span><span class="sxs-lookup"><span data-stu-id="6d785-227">**Send**: The message was sent by the service.</span></span>

   - <span data-ttu-id="6d785-228">**Falha**: A mensagem falhou ao ser entregue.</span><span class="sxs-lookup"><span data-stu-id="6d785-228">**Fail**: The message failed to be delivered.</span></span>

   - <span data-ttu-id="6d785-229">**Entregar**: A mensagem foi entregue a uma caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="6d785-229">**Deliver**: The message was delivered to a mailbox.</span></span>

   - <span data-ttu-id="6d785-230">**Expandir**: A mensagem foi enviada a um grupo de distribuição que foi expandido.</span><span class="sxs-lookup"><span data-stu-id="6d785-230">**Expand**: The message was sent to a distribution group that was expanded.</span></span>

   - <span data-ttu-id="6d785-231">**Transferir**: os destinatários foram movidos para uma mensagem bifurcada devido à conversão de conteúdo, limites de destinatário de mensagem ou agentes.</span><span class="sxs-lookup"><span data-stu-id="6d785-231">**Transfer**: Recipients were moved to a bifurcated message because of content conversion, message recipient limits, or agents.</span></span>

   - <span data-ttu-id="6d785-232">**Defer**: A entrega da mensagem foi adiada e pode ser nova tentativa mais tarde.</span><span class="sxs-lookup"><span data-stu-id="6d785-232">**Defer**: The message delivery was postponed and might be re-attempted later.</span></span>

   - <span data-ttu-id="6d785-p128">**Resolved**: A mensagem foi redirecionada para um novo endereço de destinatário com base em uma visão do Active Directory para cima. Quando isso acontece, o endereço do destinatário original é listado em uma linha separada no rastreamento de mensagem, juntamente com o status de entrega final da mensagem.</span><span class="sxs-lookup"><span data-stu-id="6d785-p128">**Resolved**: The message was redirected to a new recipient address based on an Active Directory look up. When this happens, the original recipient address is listed in a separate row in the message trace along with the final delivery status for the message.</span></span>

   <span data-ttu-id="6d785-235">Observe que mesmo uma mensagem normal for entregue com êxito irá gerar várias entradas de **evento** no rastreamento de mensagem.</span><span class="sxs-lookup"><span data-stu-id="6d785-235">Note that even an uneventful message that's successfully delivered will generate multiple **Event** entries in the message trace.</span></span>

- <span data-ttu-id="6d785-236">**Obter mais informações**: Esta seção contém os seguintes detalhes:</span><span class="sxs-lookup"><span data-stu-id="6d785-236">**More information**: This section contains the following details:</span></span>

   - <span data-ttu-id="6d785-p129">**ID da mensagem**: esse valor é descrito na seção a [ID da mensagem](#message-id) anteriormente neste tópico. Por exemplo, `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`.</span><span class="sxs-lookup"><span data-stu-id="6d785-p129">**Message ID**: This value is described in the [Message ID](#message-id) section earlier in this topic. For example, `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`.</span></span>

   - <span data-ttu-id="6d785-239">**Tamanho da mensagem**</span><span class="sxs-lookup"><span data-stu-id="6d785-239">**Message size**</span></span>

   - <span data-ttu-id="6d785-p130">**De IP**: O endereço IP do computador que enviou a mensagem. Para mensagens de saída enviadas a partir do Exchange Online, este valor fica em branco.</span><span class="sxs-lookup"><span data-stu-id="6d785-p130">**From IP**: The IP address of the computer that sent the message. For outbound messages sent from Exchange Online, this value is blank.</span></span>

   - <span data-ttu-id="6d785-p131">**Para IP**: O endereço IP ou endereços de onde o serviço tentou entregar a mensagem. Se a mensagem tiver vários destinatários, elas serão exibidas. Para mensagens de entrada enviadas para o Exchange Online, esse valor estará vazio.</span><span class="sxs-lookup"><span data-stu-id="6d785-p131">**To IP**: The IP address or addresses where the service attempted to deliver the message. If the message has multiple recipients, these are displayed. For inbound messages sent to Exchange Online, this value is blank.</span></span>

### <a name="enhanced-summary-reports"></a><span data-ttu-id="6d785-245">Relatórios de resumo avançados</span><span class="sxs-lookup"><span data-stu-id="6d785-245">Enhanced summary reports</span></span>

<span data-ttu-id="6d785-p132">Relatórios resumidos de avançada (concluídos) disponíveis estão disponíveis na seção **Downloadable relatórios** no rastreamento de mensagens de início. As informações a seguir estão disponíveis no relatório:</span><span class="sxs-lookup"><span data-stu-id="6d785-p132">Available (completed) Enhanced summary reports are available in the **Downloadable reports** section at the beginning message trace. The following information is available in the report:</span></span>

- <span data-ttu-id="6d785-248">**origin_timestamp**<sup>\*</sup>: A data e hora em que a mensagem inicialmente foi recebida pelo serviço, usando o fuso horário UTC configurado.</span><span class="sxs-lookup"><span data-stu-id="6d785-248">**origin_timestamp**<sup>\*</sup>: The date and time when the message was initially received by the service, using the configured UTC time zone.</span></span>

- <span data-ttu-id="6d785-249">**sender_address**: o endereço de email do remetente (*alias*@*domínio*).</span><span class="sxs-lookup"><span data-stu-id="6d785-249">**sender_address**: The sender's email address (*alias*@*domain*).</span></span>

- <span data-ttu-id="6d785-p133">**Recipient_status**: O status da entrega da mensagem ao destinatário. Se a mensagem foi enviada para vários destinatários, ela mostrará todos os destinatários e o status correspondente para cada um, no formato: \< *endereço de email*\>##\<*status*\>. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="6d785-p133">**Recipient_status**: The status of the delivery of the message to the recipient. If the message was sent to multiple recipients, it will show all the recipients and the corresponding status for each, in the format: \<*email address*\>##\<*status*\>. For example:</span></span>

   - <span data-ttu-id="6d785-253">**Enviar ##Receive,** significa que a mensagem foi recebida pelo serviço e enviada ao destinatário.</span><span class="sxs-lookup"><span data-stu-id="6d785-253">**##Receive, Send** means the message was received by the service and was sent to the intended destination.</span></span>

   - <span data-ttu-id="6d785-254">**Falha de ##Receive,** significa que a mensagem foi recebida pelo serviço, mas entrega ao destinatário falhou.</span><span class="sxs-lookup"><span data-stu-id="6d785-254">**##Receive, Fail** means the message was received by the service but delivery to the intended destination failed.</span></span>

   - <span data-ttu-id="6d785-255">**Entregar ##Receive,** significa que a mensagem foi recebida pelo serviço e foi entregue à caixa de correio do destinatário.</span><span class="sxs-lookup"><span data-stu-id="6d785-255">**##Receive, Deliver** means the message was received by the service and was delivered to the recipient's mailbox.</span></span>

- <span data-ttu-id="6d785-256">**assunto_da_mensagem**: os primeiros 256 caracteres de campo de **assunto** da mensagem.</span><span class="sxs-lookup"><span data-stu-id="6d785-256">**message_subject**: The first 256 characters of the message's **Subject** field.</span></span>

- <span data-ttu-id="6d785-257">**total_bytes**: O tamanho da mensagem em bytes, incluindo anexos.</span><span class="sxs-lookup"><span data-stu-id="6d785-257">**total_bytes**: The size of the message in bytes, including attachments.</span></span>

- <span data-ttu-id="6d785-p134">**identificação_da_mensagem**: esse valor é descrito na seção a [ID da mensagem](#message-id) anteriormente neste tópico. Por exemplo, `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`.</span><span class="sxs-lookup"><span data-stu-id="6d785-p134">**message_id**: This value is described in the [Message ID](#message-id) section earlier in this topic. For example, `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`.</span></span>

- <span data-ttu-id="6d785-p135">**network_message_id**: um valor de ID de mensagem exclusiva que se mantêm em todas as cópias da mensagem que pode ser criado devido à expansão de grupo de distribuição ou bifurcação. Um valor de exemplo é `1341ac7b13fb42ab4d4408cf7f55890f`.</span><span class="sxs-lookup"><span data-stu-id="6d785-p135">**network_message_id**: A unique message ID value that persists across all copies of the message that might be created due to bifurcation or distribution group expansion. An example value is `1341ac7b13fb42ab4d4408cf7f55890f`.</span></span>

- <span data-ttu-id="6d785-262">**original_client_ip**: O endereço IP do cliente do remetente.</span><span class="sxs-lookup"><span data-stu-id="6d785-262">**original_client_ip**: The IP address of the sender's client.</span></span>

- <span data-ttu-id="6d785-263">**direcionalidade**: indica se a mensagem foi enviada internamente (1) na sua organização, ou se foi enviada para fora (2) da sua organização.</span><span class="sxs-lookup"><span data-stu-id="6d785-263">**directionality**: Indicates whether the message was sent inbound (1) to your organization, or whether it was sent outbound (2) from your organization.</span></span>

- <span data-ttu-id="6d785-p136">**connector_id**: O nome do conector origem ou destino. Para obter mais informações sobre conectores no Exchange Online, consulte [Configurar o fluxo de email usando conectores no Office 365](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow).</span><span class="sxs-lookup"><span data-stu-id="6d785-p136">**connector_id**: The name of the source or destination connector. For more information about connectors in Exchange Online, see [Configure mail flow using connectors in Office 365](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow).</span></span>

- <span data-ttu-id="6d785-266">**delivery_priority**<sup>\*</sup>: se a mensagem foi enviada com prioridade **alta**, **baixa**ou **Normal** .</span><span class="sxs-lookup"><span data-stu-id="6d785-266">**delivery_priority**<sup>\*</sup>: Whether the message was sent with **High**, **Low**, or **Normal** priority.</span></span>

<span data-ttu-id="6d785-267"><sup>\*</sup>Essas propriedades só estão disponíveis em relatórios de resumo avançada.</span><span class="sxs-lookup"><span data-stu-id="6d785-267"><sup>\*</sup>These properties are only available in Enhanced summary reports.</span></span>

### <a name="extended-reports"></a><span data-ttu-id="6d785-268">Relatórios estendidos</span><span class="sxs-lookup"><span data-stu-id="6d785-268">Extended reports</span></span>

<span data-ttu-id="6d785-p137">Relatórios de Extended disponíveis (concluídos) estão disponíveis na seção **Downloadable relatórios** no início do rastreamento de mensagens. Praticamente todas as informações de um relatório de resumo avançada está disponível em um relatório de Extended (com exceção de **origin_timestamp** e **delivery_priority**). As seguintes informações adicionais só estão disponíveis em um relatório de Extended:</span><span class="sxs-lookup"><span data-stu-id="6d785-p137">Available (completed) Extended reports are available in the **Downloadable reports** section at the beginning of message trace. Virtually all of the information from an Enhanced summary report is available in an Extended report (with the exception of **origin_timestamp** and **delivery_priority**). The following additional information is only available in an Extended report:</span></span>

- <span data-ttu-id="6d785-272">**client_ip**: O endereço IP do servidor de email ou o cliente de mensagens que enviou a mensagem.</span><span class="sxs-lookup"><span data-stu-id="6d785-272">**client_ip**: The IP address of the email server or messaging client that submitted the message.</span></span>

- <span data-ttu-id="6d785-273">**client_hostname**: O nome do host ou o FQDN do servidor de email ou o cliente de mensagens que enviou a mensagem.</span><span class="sxs-lookup"><span data-stu-id="6d785-273">**client_hostname**: The host name or FQDN of the email server or messaging client that submitted the message.</span></span>

- <span data-ttu-id="6d785-274">**server_ip**: O endereço IP do servidor de origem e destino.</span><span class="sxs-lookup"><span data-stu-id="6d785-274">**server_ip**: The IP address of the source or destination server.</span></span>

- <span data-ttu-id="6d785-275">**server_hostname**: O nome do host ou o FQDN do servidor de destino.</span><span class="sxs-lookup"><span data-stu-id="6d785-275">**server_hostname**: The host name or FQDN of the destination server.</span></span>

- <span data-ttu-id="6d785-p138">**source_context**: informações Extra associadas ao campo de **origem** . Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="6d785-p138">**source_context**: Extra information associated with the **source** field. For example:</span></span>

   - `Protocol Filter Agent`

   - `3489061114359050000`

- <span data-ttu-id="6d785-p139">**origem**: O Exchange Online componente que é responsável pelo evento. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="6d785-p139">**source**: The Exchange Online component that's responsible for the event. For example:</span></span>

   - `AGENT`

   - `MAILBOXRULE`

   - `SMTP`

- <span data-ttu-id="6d785-280">**identificação_de_evento**: esses correspondem aos valores de **evento de mensagem** que são explicados na seção [Localizar registros relacionados para esta mensagem](#find-related-records-for-this-message) .</span><span class="sxs-lookup"><span data-stu-id="6d785-280">**event_id**: These correspond to the **Message event** values that are explained in the [Find related records for this message](#find-related-records-for-this-message) section.</span></span>

- <span data-ttu-id="6d785-281">**internal_message_id**: um identificador de mensagem que é atribuído pelo servidor do Exchange Online que está processando a mensagem.</span><span class="sxs-lookup"><span data-stu-id="6d785-281">**internal_message_id**: A message identifier that's assigned by the Exchange Online server that's currently processing the message.</span></span>

- <span data-ttu-id="6d785-p140">**recipient_address**: os endereços de email dos destinatários da mensagem. Vários endereços de email são separados por vírgula (;).</span><span class="sxs-lookup"><span data-stu-id="6d785-p140">**recipient_address**: The email addresses of the message's recipients. Multiple email addresses are separated by the semicolon character (;).</span></span>

- <span data-ttu-id="6d785-284">**recipient_count**: O número total de destinatários da mensagem.</span><span class="sxs-lookup"><span data-stu-id="6d785-284">**recipient_count**: The total number of recipients in the message.</span></span>

- <span data-ttu-id="6d785-285">**related_recipient_address**: usado com `EXPAND`, `REDIRECT`, e `RESOLVE` endereços que estão associados a mensagem de email de eventos para exibir os demais destinatários.</span><span class="sxs-lookup"><span data-stu-id="6d785-285">**related_recipient_address**: Used with `EXPAND`, `REDIRECT`, and `RESOLVE` events to display other recipient email addresses that are associated with the message.</span></span>

- <span data-ttu-id="6d785-p141">**referência**: este campo contém informações adicionais para tipos específicos de eventos. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="6d785-p141">**reference**: This field contains additional information for specific types of events. For example:</span></span>

   - <span data-ttu-id="6d785-p142">**DSN**: contém o link de relatório, que é o valor de **identificação_da_mensagem** da notificação de status de entrega associado (também conhecido como um DSN, o relatório de entrega, NDR ou mensagem de rejeição) se um DSN é gerado logo após este evento. Se essa for uma mensagem DSN, esse campo contém o valor de **identificação_da_mensagem** da mensagem original que o DSN foi gerado por.</span><span class="sxs-lookup"><span data-stu-id="6d785-p142">**DSN**: Contains the report link, which is the **message_id** value of the associated delivery status notification (also known as a DSN, non-delivery report, NDR, or bounce message) if a DSN is generated subsequent to this event. If this is a DSN message, this field contains the **message_id** value of the original message that the DSN was generated for.</span></span>

   - <span data-ttu-id="6d785-290">**Expandir**: contém o valor de **related_recipient_address** das mensagens relacionados.</span><span class="sxs-lookup"><span data-stu-id="6d785-290">**EXPAND**: Contains the **related_recipient_address** value of the related messages.</span></span>

   - <span data-ttu-id="6d785-291">**Recebimento**: pode conter o valor de **identificação_da_mensagem** da mensagem relacionada se a mensagem foi gerada por outros processos (por exemplo, regras de caixa de entrada).</span><span class="sxs-lookup"><span data-stu-id="6d785-291">**RECEIVE**: Might contain the **message_id** value of the related message if the message was generated by other processes (for example, Inbox rules).</span></span>

   - <span data-ttu-id="6d785-292">**Enviar**: contém o valor de **internal_message_id** de todas as mensagens DSN.</span><span class="sxs-lookup"><span data-stu-id="6d785-292">**SEND**: Contains the **internal_message_id** value of any DSN messages.</span></span>

   - <span data-ttu-id="6d785-293">**Transferir**: contém o valor de **internal_message_id** da mensagem que está sendo bifurcada (por exemplo, por conversão de conteúdo, limites de destinatário de mensagem ou agentes).</span><span class="sxs-lookup"><span data-stu-id="6d785-293">**TRANSFER**: Contains the **internal_message_id** value of the message that's being forked (for example, by content conversion, message recipient limits, or agents).</span></span>

   - <span data-ttu-id="6d785-294">**MAILBOXRULE**: contém o valor de **internal_message_id** da mensagem de entrada que causou a regra de caixa de entrada gerar a mensagem de saída.</span><span class="sxs-lookup"><span data-stu-id="6d785-294">**MAILBOXRULE**: Contains the **internal_message_id** value of the inbound message that caused the Inbox rule to generate the outbound message.</span></span>

   <span data-ttu-id="6d785-295">Para outros tipos de eventos, o campo geralmente está em branco.</span><span class="sxs-lookup"><span data-stu-id="6d785-295">For other types of events, this field is usually blank.</span></span>

- <span data-ttu-id="6d785-p143">**return_path**: O endereço de email de retorno especificado pelo comando **MAIL FROM** que enviou a mensagem. Embora este campo nunca estiver vazio, ele pode ter o valor de endereço de remetente nulo representado como `<>`.</span><span class="sxs-lookup"><span data-stu-id="6d785-p143">**return_path**: The return email address specified by the **MAIL FROM** command that sent the message. Although this field is never empty, it can have the null sender address value represented as `<>`.</span></span>

- <span data-ttu-id="6d785-p144">**message_info**: informações adicionais sobre a mensagem. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="6d785-p144">**message_info**: Additional information about the message. For example:</span></span>

   - <span data-ttu-id="6d785-p145">A data / hora de origem de mensagem em UTC para `DELIVER` e `SEND` eventos. A data / hora de origem é o horário quando a mensagem primeiro inseridos organização do Exchange Online. A data e hora em UTC é representada no formato de data / hora ISO 8601: `yyyy-mm-ddThh:mm:ss.fffZ`, onde `yyyy` = ano, `mm` = mês, `dd` = dia, `T` indica o início do componente de hora, `hh` = hora, `mm` = minuto, `ss` = segundo, `fff` = frações de um segundo, e `Z` significa `Zulu`, que é outra maneira para denotar UTC.</span><span class="sxs-lookup"><span data-stu-id="6d785-p145">The message origination date-time in UTC for `DELIVER` and `SEND` events. The origination date-time is the time when the message first entered the Exchange Online organization. The UTC date-time is represented in the ISO 8601 date-time format: `yyyy-mm-ddThh:mm:ss.fffZ`, where `yyyy` = year, `mm` = month, `dd` = day, `T` indicates the beginning of the time component, `hh` = hour, `mm` = minute, `ss` = second, `fff` = fractions of a second, and `Z` signifies `Zulu`, which is another way to denote UTC.</span></span>

   - <span data-ttu-id="6d785-p146">Erros de autenticação. Por exemplo, você pode ver o valor `11a` e o tipo de autenticação que foi usado quando ocorreu o erro de autenticação.</span><span class="sxs-lookup"><span data-stu-id="6d785-p146">Authentication errors. For example, you might see the value `11a` and the type of authentication that was used when the authentication error occurred.</span></span>

- <span data-ttu-id="6d785-305">**tenant_id**: um valor GUID que representa a organização do Exchange Online (por exemplo, `39238e87-b5ab-4ef6-a559-af54c6b07b42`).</span><span class="sxs-lookup"><span data-stu-id="6d785-305">**tenant_id**: A GUID value that represents the Exchange Online organization (for example, `39238e87-b5ab-4ef6-a559-af54c6b07b42`).</span></span>

- <span data-ttu-id="6d785-306">**original_server_ip**: O endereço IP do servidor original.</span><span class="sxs-lookup"><span data-stu-id="6d785-306">**original_server_ip**: The IP address of the original server.</span></span>

- <span data-ttu-id="6d785-p147">**custom_data**: contém dados relacionados a tipos de evento específicos. Para obter mais informações, consulte as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="6d785-p147">**custom_data**: Contains data related to specific event types. For more information, see the following sections.</span></span>

#### <a name="customdata-values"></a><span data-ttu-id="6d785-309">valores de custom_data</span><span class="sxs-lookup"><span data-stu-id="6d785-309">custom_data values</span></span>

<span data-ttu-id="6d785-p148">O campo **custom_data** para um `AGENTINFO` evento é usado por uma variedade de operadores do Exchange Online para registrar em log detalhes de processamento de mensagens. Alguns dos agentes mais interessantes são descritos nas seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="6d785-p148">The **custom_data** field for an `AGENTINFO` event is used by a variety of Exchange Online agents to log message processing details. Some of the more interesting agents are described in the following sections.</span></span>

#### <a name="spam-filter-agent"></a><span data-ttu-id="6d785-312">Agente de filtro de spam</span><span class="sxs-lookup"><span data-stu-id="6d785-312">Spam filter agent</span></span>

<span data-ttu-id="6d785-p149">Um valor de **custom_data** que começa com `S:SFA` é do agente de filtro de spam. Os principais detalhes são descritos na tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="6d785-p149">A **custom_data** value that starts with `S:SFA` is from the spam filter agent. The key details are described in the following table:</span></span>

|<span data-ttu-id="6d785-315">**Valor**</span><span class="sxs-lookup"><span data-stu-id="6d785-315">**Value**</span></span>|<span data-ttu-id="6d785-316">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6d785-316">**Description**</span></span>|
|:-----|:-----|
|`SFV=NSPM`|<span data-ttu-id="6d785-317">A mensagem foi marcada como não spam e enviada aos destinatários pretendidos.</span><span class="sxs-lookup"><span data-stu-id="6d785-317">The message was marked as non-spam and was sent to the intended recipients.</span></span>|
|`SFV=SPM`|<span data-ttu-id="6d785-318">O filtro de conteúdo marcou a mensagem como spam.</span><span class="sxs-lookup"><span data-stu-id="6d785-318">The message was marked as spam by the content filter.</span></span>|
|`SFV=BLK`|<span data-ttu-id="6d785-319">A filtragem foi ignorada e a mensagem foi bloqueada, pois originou-se em um remetente bloqueado.</span><span class="sxs-lookup"><span data-stu-id="6d785-319">Filtering was skipped and the message was blocked because it originated from a blocked sender.</span></span>|
|`SFV=SKS`|<span data-ttu-id="6d785-p150">A mensagem foi marcada como spam antes de ser processada pelo filtro de conteúdo. Isso inclui mensagens que atenderam a uma regra Transporte para marcá-la automaticamente como spam e ignorar toda filtragem adicional.</span><span class="sxs-lookup"><span data-stu-id="6d785-p150">The message was marked as spam prior to being processed by the content filter. This includes messages where the message matched a Transport rule to automatically mark it as spam and bypass all additional filtering.</span></span>|
|`SCL=<number>`|<span data-ttu-id="6d785-322">Para saber mais sobre os diferentes valores SCL e seu significado, veja [Níveis de confiança de spam](https://technet.microsoft.com/library/jj200686.aspx).</span><span class="sxs-lookup"><span data-stu-id="6d785-322">For more information about the different SCL values and what they mean, see [Spam confidence levels](https://technet.microsoft.com/library/jj200686.aspx).</span></span>|
|`PCL=<number>`|<span data-ttu-id="6d785-p151">O valor do Nível de confiança de phishing (PCL) da mensagem. Podem ser interpretados da mesma maneira que os valores de SCL documentados em [Níveis de confiança de spam](https://technet.microsoft.com/library/jj200686.aspx).  </span><span class="sxs-lookup"><span data-stu-id="6d785-p151">The Phishing Confidence Level (PCL) value of the message. These can be interpreted the same way as the SCL values documented in [Spam confidence levels](https://technet.microsoft.com/library/jj200686.aspx).</span></span>|
|`DI=SB`|<span data-ttu-id="6d785-325">O remetente da mensagem foi bloqueado.</span><span class="sxs-lookup"><span data-stu-id="6d785-325">The sender of the message was blocked.</span></span>|
|`DI=SQ`|<span data-ttu-id="6d785-326">A mensagem foi colocada em quarentena.</span><span class="sxs-lookup"><span data-stu-id="6d785-326">The message was quarantined.</span></span>|
|`DI=SD`|<span data-ttu-id="6d785-327">A mensagem foi excluída.</span><span class="sxs-lookup"><span data-stu-id="6d785-327">The message was deleted.</span></span>|
|`DI=SJ`|<span data-ttu-id="6d785-328">A mensagem foi enviada para a pasta de lixo eletrônico do destinatário.</span><span class="sxs-lookup"><span data-stu-id="6d785-328">The message was sent to the recipient's Junk Email folder.</span></span>|
|`DI=SN`|<span data-ttu-id="6d785-p152">A mensagem foi roteada através do pool de entrega de risco mais alto. Para obter mais informações, consulte o [pool de alto risco de entrega para mensagens de saída](https://technet.microsoft.com/library/jj200746.aspx).</span><span class="sxs-lookup"><span data-stu-id="6d785-p152">The message was routed through the higher risk delivery pool. For more information, see [High-risk delivery pool for outbound messages](https://technet.microsoft.com/library/jj200746.aspx).</span></span>|
|`DI=SO`|<span data-ttu-id="6d785-331">A mensagem foi roteada através do pool normal de entrega de saída.</span><span class="sxs-lookup"><span data-stu-id="6d785-331">The message was routed through the normal outbound delivery pool.</span></span>|
|<span data-ttu-id="6d785-332">' SFS = [a]</span><span class="sxs-lookup"><span data-stu-id="6d785-332">\`SFS=[a]</span></span>|<span data-ttu-id="6d785-333">Busca de site Catalogado = [b]'</span><span class="sxs-lookup"><span data-stu-id="6d785-333">SFS=[b]\`</span></span>|<span data-ttu-id="6d785-334">Isso indica que houve correspondência com regras de spam.</span><span class="sxs-lookup"><span data-stu-id="6d785-334">This denotes that spam rules were matched.</span></span>|
|`IPV=CAL`|<span data-ttu-id="6d785-335">A mensagem foi permitida pelos filtros de spam porque o endereço IP estava especificado em uma Lista de Permissões de IP do filtro de conexão.</span><span class="sxs-lookup"><span data-stu-id="6d785-335">The message was allowed through the spam filters because the IP address was specified in an IP Allow list in the connection filter.</span></span>|
|`H=<EHLOstring>`|<span data-ttu-id="6d785-336">A cadeia de caracteres HELO ou EHLO do servidor de email conectado.</span><span class="sxs-lookup"><span data-stu-id="6d785-336">The HELO or EHLO string of the connecting email server.</span></span>|
|`PTR=<ReverseDNS>`|<span data-ttu-id="6d785-337">O registro PTR do endereço IP de envio, também conhecido como o endereço de DNS reverso.</span><span class="sxs-lookup"><span data-stu-id="6d785-337">The PTR record of the sending IP address, also known as the reverse DNS address.</span></span>|

<span data-ttu-id="6d785-338">Um valor de **custom_data** de exemplo para uma mensagem que é feita a filtragem de spam semelhante a esta:</span><span class="sxs-lookup"><span data-stu-id="6d785-338">An example **custom_data** value for a message that's filtered for spam like this:</span></span>

`S:SFA=SUM|SFV=SPM|IPV=CAL|SRV=BULK|SFS=470454002|SFS=349001|SCL=9|SCORE=-1|LIST=0|DI=SN|RD=ftmail.inc.com|H=ftmail.inc.com|CIP=98.129.140.74|SFP=1501|ASF=1|CTRY=US|CLTCTRY=|LANG=en|LAT=287|LAT=260|LAT=18;`

#### <a name="malware-filter-agent"></a><span data-ttu-id="6d785-339">Agente de filtro de malware</span><span class="sxs-lookup"><span data-stu-id="6d785-339">Malware filter agent</span></span>

<span data-ttu-id="6d785-p153">Um valor de **custom_data** que começa com `S:AMA` é do agente de filtro de malware. Os principais detalhes são descritos na tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="6d785-p153">A **custom_data** value that starts with `S:AMA` is from the malware filter agent. The key details are described in the following table:</span></span>

|<span data-ttu-id="6d785-342">**Valor**</span><span class="sxs-lookup"><span data-stu-id="6d785-342">**Value**</span></span>|<span data-ttu-id="6d785-343">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6d785-343">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6d785-344">' AMA = SOMA</span><span class="sxs-lookup"><span data-stu-id="6d785-344">\`AMA=SUM</span></span>|<span data-ttu-id="6d785-345">v=1</span><span class="sxs-lookup"><span data-stu-id="6d785-345">v=1</span></span>|<span data-ttu-id="6d785-346">` or `AMA=EV</span><span class="sxs-lookup"><span data-stu-id="6d785-346">` or `AMA=EV</span></span>|<span data-ttu-id="6d785-347">v = 1'</span><span class="sxs-lookup"><span data-stu-id="6d785-347">v=1\`</span></span>|<span data-ttu-id="6d785-p154">A mensagem foi determinada por conter malware. `SUM` indica que o malware poderia ter foi detectado por qualquer número de mecanismos. `EV` indica que o malware foi detectado por um mecanismo específico. Quando malware é detectado pelo mecanismo que isso dispara as ações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="6d785-p154">The message was determined to contain malware. `SUM` indicates the malware could've been detected by any number of engines. `EV` indicates the malware was detected by a specific engine. When malware is detected by an engine this triggers the subsequent actions.</span></span>|
|`Action=r`|<span data-ttu-id="6d785-352">A mensagem foi substituída.</span><span class="sxs-lookup"><span data-stu-id="6d785-352">The message was replaced.</span></span>|
|`Action=p`|<span data-ttu-id="6d785-353">A mensagem foi ignorada.</span><span class="sxs-lookup"><span data-stu-id="6d785-353">The message was bypassed.</span></span>|
|`Action=d`|<span data-ttu-id="6d785-354">A mensagem foi adiada.</span><span class="sxs-lookup"><span data-stu-id="6d785-354">The message was deferred.</span></span>|
|`Action=s`|<span data-ttu-id="6d785-355">A mensagem foi excluída.</span><span class="sxs-lookup"><span data-stu-id="6d785-355">The message was deleted.</span></span>|
|`Action=st`|<span data-ttu-id="6d785-356">A mensagem foi ignorada.</span><span class="sxs-lookup"><span data-stu-id="6d785-356">The message was bypassed.</span></span>|
|`Action=sy`|<span data-ttu-id="6d785-357">A mensagem foi ignorada.</span><span class="sxs-lookup"><span data-stu-id="6d785-357">The message was bypassed.</span></span>|
|`Action=ni`|<span data-ttu-id="6d785-358">A mensagem foi rejeitada.</span><span class="sxs-lookup"><span data-stu-id="6d785-358">The message was rejected.</span></span>|
|`Action=ne`|<span data-ttu-id="6d785-359">A mensagem foi rejeitada.</span><span class="sxs-lookup"><span data-stu-id="6d785-359">The message was rejected.</span></span>|
|`Action=b`|<span data-ttu-id="6d785-360">A mensagem foi bloqueada.</span><span class="sxs-lookup"><span data-stu-id="6d785-360">The message was blocked.</span></span>|
|`Name=<malware>`|<span data-ttu-id="6d785-361">O nome do malware foi detectado.</span><span class="sxs-lookup"><span data-stu-id="6d785-361">The name of the malware that was detected.</span></span>|
|`File=<filename>`|<span data-ttu-id="6d785-362">O nome do arquivo que continha o malware.</span><span class="sxs-lookup"><span data-stu-id="6d785-362">The name of the file that contained the malware.</span></span>|

<span data-ttu-id="6d785-363">Um valor de **custom_data** de exemplo para uma mensagem que contenha malware tem esta aparência:</span><span class="sxs-lookup"><span data-stu-id="6d785-363">An example **custom_data** value for a message that contains malware looks like this:</span></span>

`S:AMA=SUM|v=1|action=b|error=|atch=1;S:AMA=EV|engine=M|v=1|sig=1.155.974.0|name=DOS/Test_File|file=filename;S:AMA=EV|engine=A|v=1|sig=201707282038|name=Test_File|file=filename`

#### <a name="transport-rule-agent"></a><span data-ttu-id="6d785-364">Agente de regras de transporte</span><span class="sxs-lookup"><span data-stu-id="6d785-364">Transport rule agent</span></span>

<span data-ttu-id="6d785-p155">Um valor de **custom_data** que começa com`S:TRA` é do agente de regras de transporte para regras de fluxo de email (também conhecido como regras de transporte). Os principais detalhes são descritos na tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="6d785-p155">A **custom_data** value that starts with`S:TRA` is from the transport rule agent for mail flow rules (also known as transport rules). The key details are described in the following table:</span></span>

|<span data-ttu-id="6d785-367">**Valor**</span><span class="sxs-lookup"><span data-stu-id="6d785-367">**Value**</span></span>|<span data-ttu-id="6d785-368">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6d785-368">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6d785-369">' ETR</span><span class="sxs-lookup"><span data-stu-id="6d785-369">\`ETR</span></span>|<span data-ttu-id="6d785-370">ruleId =<guid>\`</span><span class="sxs-lookup"><span data-stu-id="6d785-370">ruleId=<guid>\`</span></span>|<span data-ttu-id="6d785-371">A identificação da regra encontrou uma correspondência.</span><span class="sxs-lookup"><span data-stu-id="6d785-371">The rule ID that was matched.</span></span>|
|`St=<datetime>`|<span data-ttu-id="6d785-372">A data e hora em UTC quando ocorreu a correspondência da regra.</span><span class="sxs-lookup"><span data-stu-id="6d785-372">The date and time in UTC when the rule match occurred.</span></span>|
|`Action=<ActionDefinition>`|<span data-ttu-id="6d785-p156">A ação que foi aplicada. Para obter uma lista de ações disponíveis, consulte [Mail flow ações de regra no Exchange Online](https://technet.microsoft.com/library/jj919237.aspx).</span><span class="sxs-lookup"><span data-stu-id="6d785-p156">The action that was applied. For a list of available actions, see [Mail flow rule actions in Exchange Online](https://technet.microsoft.com/library/jj919237.aspx).</span></span>|
|`Mode=<Mode>`|<span data-ttu-id="6d785-p157">O modo da regra. Valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="6d785-p157">The mode of the rule. Valid values are: </span></span><br/><span data-ttu-id="6d785-377">• **Impor**: todas as ações da regra serão impostas.</span><span class="sxs-lookup"><span data-stu-id="6d785-377">• **Enforce**: All actions on the rule will be enforced.</span></span> <br/><span data-ttu-id="6d785-378">• **Testar com dicas de política:**: dica de política qualquer ação será enviada, mas outras ações impositivas não serão realizadas em.</span><span class="sxs-lookup"><span data-stu-id="6d785-378">• **Test with Policy Tips:**: Any Policy Tip actions will be sent, but other enforcement actions will not be acted on.</span></span> <br/><span data-ttu-id="6d785-379">• **Teste sem dicas de política**: ações serão listadas em um arquivo de log, mas os remetentes não serão notificados de nenhuma maneira e as ações impositivas não serão realizadas em.</span><span class="sxs-lookup"><span data-stu-id="6d785-379">• **Test without Policy Tips**: Actions will be listed in a log file, but senders will not be notified in any way, and enforcement actions will not be acted on.</span></span>|

<span data-ttu-id="6d785-380">Um valor de **custom_data** de exemplo para uma mensagens que corresponde às condições de uma regra de fluxo de email tem esta aparência:</span><span class="sxs-lookup"><span data-stu-id="6d785-380">An example **custom_data** value for a messages that matches the conditions of a mail flow rule looks like this:</span></span>

`S:TRA=ETR|ruleId=19a25eb2-3e43-4896-ad9e-47b6c359779d|st=7/17/2017 12:31:25 AM|action=ApplyHtmlDisclaimer|sev=1|mode=Enforce`

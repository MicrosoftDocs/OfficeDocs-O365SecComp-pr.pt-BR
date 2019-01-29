---
title: Diretivas de supervisão no Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.SupervisoryReview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: d14ae7c3-fcb0-4a03-967b-cbed861bb086
description: Noções básicas sobre diretivas de supervisão no Office 365
ms.openlocfilehash: 0c76ba5b17277d8bd441810415e7e9acd1adbf36
ms.sourcegitcommit: 3cb775e60b3806b66568ed2f9664c17ef96ca8de
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/28/2019
ms.locfileid: "29603521"
---
# <a name="supervision-policies-in-office-365"></a>Diretivas de supervisão no Office 365

Diretivas de supervisão no Office 365 permitem que você capture comunicações de funcionários para exame por revisores designados. Você pode definir políticas específicas que capturam email interno e externo, Microsoft Teams ou comunicações de terceiros 3rd em sua organização. Os revisores podem, em seguida, examine as mensagens para certificar-se de que são compatíveis com os padrões de mensagem da sua organização e resolvê-los com o tipo de classificação. Essas políticas também podem ajudá-lo a superar muitos desafios de conformidade moderna, incluindo os tipos de aumento dos canais de comunicação, o aumento do volume de dados de mensagem e imposição normativos & o risco de multas de monitoramento.

Em algumas organizações, pode haver uma separação de tarefas entre o suporte de TI e grupo de gerenciamento de conformidade. O Office 365 oferece suporte a separação entre Configurando o inquilino com recursos de suporte de diretiva de supervisão e a configuração de políticas e agindo em comunicações capturadas. Por exemplo, o grupo de TI para uma organização pode ser responsável por configurar permissões de função e grupos para dar suporte a políticas de supervisão que estão configuradas e gerenciadas pela equipe de conformidade da organização.

## <a name="scenarios-for-supervision-policies"></a>Cenários para diretivas de supervisão

Diretivas de supervisão podem auxiliar communications monitoramento na sua organização em várias áreas:

- **Políticas corporativas**

    Funcionários devem estar em conformidade com o uso aceitável, os padrões éticos e outras políticas corporativas em todas as suas comunicações relacionado aos negócios. Diretivas de supervisão podem detectar violações de política e ajudá-lo a tomar as ações corretivas para ajudar a reduzir esses tipos de incidentes. Por exemplo, você pode monitorar sua organização para potenciais violações de recursos humanos, como assédio ou o uso da linguagem inadequado ou ofensivo nas comunicações do funcionário.

- **Gerenciamento de riscos**

    As organizações são responsáveis todas as comunicações distribuídas em toda a sua infraestrutura e os sistemas de rede corporativa. Usando diretivas de supervisão para ajudar a identificar e gerenciar os riscos e exposição legal potencial pode ajudar a minimizar os riscos antes que eles podem danificar operações corporativas. Por exemplo, você pode monitorar a sua organização para comunicações não autorizadas para projetos confidenciais como futuras aquisições, fusões, comunicados de ganhos, reorganizações ou alterações da equipe de liderança.

- **Conformidade a normas**

    A maioria das organizações deve cumprir algum tipo de padrões de conformidade a normas como parte de suas procedimentos operacionais normais. Essas normas geralmente exigem que as organizações a implementar algum tipo de supervisão ou processo de supervisão de mensagens que é apropriado para seu setor. A regra de financeiros setor normativos autoridade (FINRA) 3110 é um bom exemplo de um requisito para organizações adotar os procedimentos de supervisão para monitorar as atividades de seus funcionários e os tipos de empresas em que ele é ativado. Outro exemplo pode ser uma necessidade para monitorar corretores em sua organização para a proteção contra lavagem potencial de dinheiro, insider comerciais, fraude ou atividades suborno. Diretivas de supervisão podem ajudar sua organização a atender a esses requisitos, fornecendo um processo para monitorar e relatório na comunicação corporativa.

## <a name="feature-components"></a>Componentes de recursos

### <a name="supervision-policy"></a>Diretiva de supervisão

Você vai criar diretivas de supervisão no Centro de conformidade do & de segurança. Essas políticas definem quais comunicações e os usuários estão sujeitos a revisão na sua organização, definir condições personalizadas que as comunicações devem atender e especifica que deve executar as revisões. Usuários incluídos na análise de supervisão grupo de função pode configurar políticas e qualquer pessoa que tenha essa função atribuída podem acessar a página de supervisão em dados governança no Centro de conformidade do & de segurança do Office 365.

### <a name="supervised-users"></a>Usuários supervisionados

Antes de começar a usar supervisão, você precisará determinar que terão suas comunicações analisadas. Na política, você usará endereços de email do usuário para identificar indivíduos ou grupos de pessoas para for o Supervisor. Alguns exemplos de como esses grupos são grupos do Office 365, listas de distribuição baseada no Exchange e canais de Teams da Microsoft. Você também pode excluir o usuários ou grupos específicos de supervisão incluídos dentro de um grupo supervisionado ou uma lista de grupos.

> [!IMPORTANT]
> Monitorado pelo diretivas de supervisão de todos os usuários devem ter uma licença de Office 365 Enterprise E3 com o complemento de conformidade avançadas ou ser incluídos em uma assinatura do Office 365 Enterprise E5. Se você não tiver um plano de Enterprise E5 existente e quiser tentar supervisão, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).

### <a name="reviewers"></a>Revisores

Quando você cria uma diretiva de supervisão, você vai determinar quem executará as análises das mensagens dos usuários supervisionadas. Na política, você usará endereços de email do usuário para identificar indivíduos ou grupos de pessoas para examinar comunicações supervisionadas.

### <a name="groups-for-supervised-users-and-reviewers"></a>Grupos de usuários supervisionados e revisores

Para simplificar sua instalação, crie grupos para as pessoas que terão sua comunicação analisada e grupos para as pessoas que analisará essas comunicações. Se você estiver usando grupos, talvez seja necessário várias. Por exemplo, se você deseja monitorar as comunicações entre os dois grupos distintos de pessoas, ou se você deseja especificar um grupo que não vai ser supervisionados.

### <a name="supported-communication-types"></a>Tipos de comunicação com suporte

Com as diretivas de supervisão, você pode optar por monitorar as mensagens em uma ou mais das seguintes plataformas de comunicação:

- **Email do exchange:** Caixas de correio hospedadas no Exchange Online como parte de sua assinatura do Office 365 são todos os candidatos para supervisão de mensagem. Emails e anexos condições de diretiva de supervisão correspondentes são instantaneamente disponíveis para o monitoramento e nos relatórios de supervisão. Tipos de anexos suportados são:

    - Microsoft Word (. docx)
    - Microsoft Excel (. xlsx)
    - Microsoft PowerPoint (. pptx)

- **Equipes da Microsoft:** Comunicações de bate-papo e anexos associados no canais de Teams Microsoft públicos e particulares e chats individuais podem ser supervisionados. Condições da diretiva de supervisão de correspondência de chats de equipes são processadas uma vez a cada 24 horas e, em seguida, estão disponíveis para o monitoramento e nos relatórios de supervisão.
- **Fontes de terceiros:** Você pode for o Supervisor comunicações de fontes de terceiros (como do Facebook ou pasta de recados) se que você importou esses dados para caixas de correio do Office 365 em sua organização. [Saiba como importar dados de terceiros 3rd no Office 365](https://docs.microsoft.com/office365/securitycompliance/archiving-third-party-data).

### <a name="policy-settings"></a>Configurações de política

#### <a name="direction"></a>Direção

Por padrão, a condição de **direção é** é exibida e não pode ser removida. Configurações de direção de comunicação em uma diretiva podem ser escolhidas individualmente ou em conjunto:

- **Entrada** - você pode escolher a **entrada** para examinar comunicações que são enviadas **para** as pessoas que você escolher for o Supervisor **de** pessoas não incluídas na política.
- **Saída** - você pode escolher a **saída** se desejar examinar as comunicações que são enviadas **das** pessoas que você escolher for o Supervisor **para** pessoas não incluídas na política.
- **Internal** - você pode escolher **interno** para analisar comunicações enviadas **entre** as pessoas que você identificou na política.

#### <a name="sensitive-information-types"></a>Tipos de informações confidenciais

Você tem a opção de tipos de informações confidenciais, incluindo como parte da sua política de supervisão. Tipos de informações confidenciais são um dos tipos de dados predefinido ou personalizado que pode ajudar a identificar e proteger os números de cartão de crédito, números de conta bancária, números de passaporte e muito mais. Como parte do Office 365 [prevenção de perda de dados (DLP)](data-loss-prevention-policies.md), a configuração de informações confidenciais pode aproveitar padrões, proximidade caractere, níveis de confiança e tipos de dados personalizados, até mesmo, para ajudar a identificar e sinalizar o conteúdo que pode ser confidencial. Os tipos de informações confidenciais padrão são:

- Financeiro
- Médicos e integridade
- Privacidade
- Tipo de informações personalizadas

Para saber mais sobre os detalhes de informações confidenciais e os padrões incluídos entre os tipos padrão, consulte a [quais tipos de informações confidenciais procurar](what-the-sensitive-information-types-look-for.md).

#### <a name="custom-keyword-dictionaries"></a>Dicionários personalizados de palavra-chave

Configurando os dicionários personalizados de palavra-chave (ou dicionários) pode fornecer um gerenciamento simples de palavras-chave específicas para sua organização ou o setor e pode oferecer suporte a até 100.000 termos por dicionário. Se necessário, você pode aplicar vários dicionários personalizados de palavra-chave a uma única política ou ter um dicionário de palavra-chave única política por. Esses dicionários são atribuídos em uma diretiva de supervisão e podem ser originados de um arquivo (por exemplo, uma lista de arquivo. csv ou. txt) ou a partir de uma lista, você pode [Inserir diretamente em um cmdlet do PowerShell](create-a-keyword-dictionary.md).

#### <a name="conditional-settings"></a>Configurações condicionais

As condições que você escolher para a política se aplicará à comunicação de fontes de email e de terceiros 3rd em sua organização (como do Facebook ou pasta de recados).

A tabela a seguir explica mais sobre cada condição.
  
|**Condição**|**Como usar essa condição**|
|:-----|:-----|
|Mensagem é recebida de qualquer um desses domínios  <br><br> Mensagem não é recebida de qualquer um desses domínios | Para aplicar a política quando determinados domínios são incluídos ou excluídos em uma mensagem recebida, insira cada domínio e separe múltiplos domínios com uma vírgula. Cada domínio que você digitar será aplicado separadamente (apenas um desses domínios deve aplicar para a política seja aplicada à mensagem). |
|Mensagem é enviada para qualquer um desses domínios  <br><br> Mensagem não é enviada para qualquer um desses domínios | Para aplicar a política quando determinados domínios são incluídos ou excluídos em uma mensagem enviada, insira cada domínio e separe múltiplos domínios com uma vírgula. Cada domínio que você digitar será aplicado separadamente (apenas um desses domínios deve aplicar para a política seja aplicada à mensagem). |
|Mensagem é classificada com qualquer uma dessas etiquetas  <br><br> Mensagem não foi classificada com qualquer uma dessas etiquetas | Para aplicar a política quando determinados rótulos de retenção são incluídos ou excluídos em uma mensagem. Rótulos de retenção devem ser configurados separadamente e rótulos configurados podem ser escolhidos como parte dessa condição. Cada rótulo que você escolher será aplicado separadamente (apenas um desses rótulos deve aplicar para a política seja aplicada à mensagem). Para obter mais informações sobre como configurar rótulos de retenção, consulte [Overview of rótulos de retenção](https://docs.microsoft.com/office365/securitycompliance/labels).|
|Mensagem contém qualquer uma destas palavras  <br><br> Mensagem contém nenhuma dessas palavras | Para aplicar a política quando determinadas palavras ou frases são incluídas ou excluídas em uma mensagem, insira cada palavra ou frase em uma linha separada. Cada linha de palavras inseridas será aplicada separadamente (apenas um dessas linhas deve aplicar para a política seja aplicada à mensagem). Para obter mais informações sobre como inserir palavras ou frases, consulte a próxima seção [correspondência de palavras e frases para emails ou anexos](supervision-policies.md#Matchwords).|
|O anexo contém qualquer uma destas palavras  <br><br> O anexo contém nenhuma dessas palavras | Para aplicar a política quando determinadas palavras ou frases são incluídas ou excluídas no anexo de uma mensagem (por exemplo, um documento do Word), insira cada palavra ou frase em uma linha separada. Cada linha de palavras inseridas será aplicada separadamente (somente uma linha deve se aplicam para a política seja aplicada ao anexo). Para obter mais informações sobre como inserir palavras ou frases, consulte a próxima seção [correspondência de palavras e frases para emails ou anexos](supervision-policies.md#Matchwords).|
|Anexo é qualquer um desses tipos de arquivo  <br><br> Anexo é nenhum desses tipos de arquivo | Para for o Supervisor de comunicações que incluem ou exclua tipos específicos de anexos, insira as extensões de arquivo (por exemplo, .exe ou. PDF). Se desejar incluir ou excluir várias extensões de arquivo, digite em linhas separadas. Extensão de apenas um anexo precisa corresponder para aplicar a política.|
|O tamanho da mensagem é maior do que  <br><br> Tamanho de mensagem não for maior que | Para revisar as mensagens com base em um determinado tamanho, use essas condições para especificar o tamanho máximo ou mínimo, que uma mensagem pode ser antes que ele está sujeito a revisão. Por exemplo, se você especificar o **tamanho da mensagem for maior que** \> **1.0 MB**, todas as mensagens que são 1.01 MB e maior vão estar sujeitos a revisão. Você pode escolher bytes, kilobytes, megabytes ou gigabytes para essa condição.|
|Anexo é maior que  <br><br> Anexo não for maior que | Para revisar as mensagens com base no tamanho dos seus anexos, especifique o tamanho máximo ou mínimo um anexo pode ser antes da mensagem e seus respectivos anexos estão sujeitos a revisão. Por exemplo, se você especificar o **anexo é maior do que** \> **MB 2.0**, todas as mensagens com anexos 2.01 MB e o failover não serão sujeitos a revisão. Você pode escolher bytes, kilobytes, megabytes ou gigabytes para essa condição.|
   
##### <a name="matching-words-and-phrases-to-emails-or-attachments"></a>Palavras e frases correspondentes a emails ou anexos
<a name="Matchwords"> </a>

Cada linha de palavras inseridas será aplicada separadamente (somente uma linha deve se aplicam para a condição de política a ser aplicado ao email ou anexo). Por exemplo, vamos usar a condição, a **que mensagem contém qualquer uma dessas palavras**, com o bancário"palavras-chave" e "insider comercialização" em linhas separadas. A política será aplicada a todas as mensagens que inclui "bancário" ou a frase "insider comercialização". Apenas uma dessas palavras ou frases deve ocorrer para essa condição de política a ser aplicado. Palavras na mensagem ou no anexo devem corresponder exatamente o que você digita.
  
##### <a name="entering-multiple-conditions"></a>Inserindo várias condições

Se você inserir várias condições, o Office 365 usa todas as condições juntos para determinar quando aplicar a política aos itens de comunicação. Quando você configura várias condições, eles devem todos ser atendidos para a política seja aplicada, a menos que você insira uma exceção. Por exemplo, digamos que você precisa criar uma política que deve ser aplicadas se uma mensagem contendo a palavra "comércio" e for maior que 2MB. No entanto, se a mensagem também contém as palavras "Aprovado pelo financeiro da Contoso", a diretiva não deve aplicar. Assim, nesse caso, as três condições seria da seguinte maneira:
  
- **Mensagem contém qualquer uma dessas palavras**, com as palavras-chave "comercial"

- **Tamanho da mensagem for maior que**, com o valor de 2 MB

- **Mensagem contém nenhuma dessas palavras**, com as palavras-chave "Aprovado pela equipe financeiro da Contoso".

#### <a name="review-percentage"></a>Porcentagem de revisão

Você pode especificar uma porcentagem de todas as comunicações governados por uma política de supervisão se você deseja reduzir a quantidade de conteúdo para analisar. Podemos aleatoriamente vai Selecione essa quantidade de conteúdo a porcentagem total que correspondem às condições que você escolheu. Se você quiser revisores para examinar todos os itens, você pode inserir **100%** em uma diretiva de supervisão.

## <a name="monitoring--managing"></a>Gerenciando & de monitoramento

Os resultados de suas diretivas de supervisão de monitoramento e a aplicação de uma marca de resolução são fácil e conveniente. Você pode ver rapidamente o status de itens revisados, os usuários e grupos com supervisão e usuários e grupos designados como revisores.

### <a name="supervision-policy-dashboard"></a>Painel de diretiva de supervisão

Usar o painel de diretiva de supervisão é a maneira mais fácil para gerenciar os resultados de diretiva de supervisão e resolver os itens pendentes. Este painel permite que os revisores para ver rapidamente os itens que precisam ser revisados, realize uma ação em um item e revise os resultados da anteriormente analisado e resolvido itens para cada política de supervisão. Você pode acessar o painel de diretiva de supervisão no & de segurança do Office 365 Centro de conformidade em **supervisão** > *Sua política de sinalizador* > **Open**.

#### <a name="dashboard-home"></a>Página inicial do painel

A página **inicial** do painel tem várias seções para ajudá-lo a executar ações rapidamente suas diretivas de supervisão. Aqui, você pode:

- Examinar rapidamente os destaques pendentes e resolvidos para a semana
- Ver uma lista dos supervisionadas usuários e grupos supervisionados para a política selecionada
- Ver uma lista dos revisores e revise as equipes para a política selecionada
- Consulte quais plataformas de comunicação com o conteúdo sob supervisão para a política.

#### <a name="supervise-tab"></a>Guia for o Supervisor

Na guia **Supervise** é onde os revisores possam tirar ação e resolver itens identificada pela diretiva selecionada. Aqui, você pode:

- Filtrar por itens questionáveis compatíveis e incompatíveis pendentes
- Marca um único item como compatível com, não compatível ou questionáveis. Você também poderá gravar um comentário com o item para ajudar a esclarecer a marca ação tomada.
- Em massa marcar vários itens como compatível com, não compatível ou questionáveis. Você também poderá gravar um comentário com vários itens para ajudar a esclarecer a marca ação tomada.
- Exiba o histórico da marcação de um único item, incluindo que resolve o item, a data e hora de quaisquer comentários incluídos, a marca de resolução e a ação.
- Reclassificá anteriormente analisado itens como compatível com, não compatível ou questionáveis. Você também poderá gravar um comentário com um único ou vários itens para ajudar a esclarecer a ação reclassificação tomada.

#### <a name="resolved-items-tab"></a>Resolvido guia itens

Na guia **Itens resolvido** é onde os revisores podem exibir todos os itens anteriormente resolvidos para a política selecionada. Aqui, você pode:

- Exibir e classificar o assunto, remetente e data de itens resolvidos rapidamente.
- Exibir o histórico de classificação e comentário de qualquer item selecionado

### <a name="other-ways-to-review-items"></a>Outras maneiras de examinar itens

Se os revisores preferisse não usar o painel de supervisão no Office 365, eles também têm outras opções para examinar e gerenciar itens coletados pelo diretivas de supervisão.

#### <a name="outlook-on-the-web"></a>Outlook na Web

Os usuários designados como revisores em uma diretiva de supervisão podem usar o Outlook na web para analisar e itens de supervisão de resolvido. O suplemento de supervisão é instalado automaticamente no Outlook na web para todos os revisores que você especificou na política. Nenhuma configuração adicional será necessária por sua organização para pastas de compartilhadas de diretiva de supervisão esteja disponível para os revisores configurados.

Usando o Outlook na web, os revisores podem:

- Exibir itens filtrados por status compatível com, não compatível, questionável e resolvido
- Marca um único item seguinte compatível com, não compatível, questionável ou resolvido. Você também poderá gravar um comentário com o item para ajudar a esclarecer a marca ação tomada.
- Exiba o histórico da marcação de um único item, incluindo que resolve o item, a data e hora de quaisquer comentários incluídos, a marca de resolução e a ação.
- Reclassificá anteriormente analisado itens como compatível com, não compatível ou questionáveis. Você também poderá gravar um comentário com itens de única para ajudar a esclarecer a ação reclassificação tomada.

#### <a name="microsoft-outlook"></a>Microsoft Outlook

Para revisar identificadas por uma política de supervisão de comunicações, revisores também podem usar o suplemento de supervisão para o Microsoft Outlook. No entanto, os revisores devem executar algumas etapas para instalá-lo na versão para desktop do Outlook. Para obter orientações detalhadas sobre como instalar o suplemento de supervisão para o Outlook, consulte [Configurar diretivas de supervisão](configure-supervision-policies.md).

Usando o Outlook, os revisores podem:

- Exibir itens filtrados por status compatível com, não compatível, questionável e resolvido
- Marca um único item seguinte compatível com, não compatível, questionável ou resolvido. Você também poderá gravar um comentário com o item para ajudar a esclarecer a marca ação tomada.
- Exiba o histórico da marcação de um único item, incluindo que resolve o item, a data e hora de quaisquer comentários incluídos, a marca de resolução e a ação.
- Reclassificá anteriormente analisado itens como compatível com, não compatível ou questionáveis. Você também poderá gravar um comentário com itens de única para ajudar a esclarecer a ação reclassificação tomada.

## <a name="reporting"></a>Relatório

Use os relatórios de supervisão para ver a atividade de revisão no nível de política e revisor. Para cada diretiva, você também pode exibir live estatísticas sobre o estado atual da atividade de revisão. Você pode usar os relatórios de supervisão para:
  
- Verificar se as suas políticas estão funcionando conforme pretendido.
- Descubra quantos comunicações estão sendo identificados para revisão.
- Descubra quantos communications não são compatíveis e quais estão passando revise. Essas informações podem ajudá-lo a decidir se deseja ajustar suas políticas ou alterar o número de revisores.

### <a name="view-the-supervision-report"></a>Exibir o relatório de supervisão

1. Entrar no [Centro de conformidade de & de segurança](https://protection.office.com/) usando as credenciais de uma conta de administrador em sua organização do Office 365 que tenha permissões para exibir relatórios de supervisão.
2. Vá para qualquer um dos **relatórios** \> **supervisão**ou do **painel** . Você verá uma supervisão reporting widget com um resumo das atividades de diretiva de supervisão atual.
3. Selecione o widget **supervisão** para abrir a página de relatório detalhado.

> [!NOTE]
> Se você não conseguir acessar a página de **relatórios** , verifique se você for um membro do grupo de função de análise de supervisão, conforme descrito em [tornar supervisão disponível na sua organização](configure-supervision-policies.md). Sejam incluídos na função grupo permite que você criar e gerenciar supervisão políticas e executar o relatório.
  
### <a name="how-to-use-the-report"></a>Como usar o relatório

Quando uma diretiva de supervisão identifica uma mensagem de comunicação para revisão, o email é entregue a pasta de supervisão do revisor no Outlook e Outlook web app. Este relatório lista o nome da política de cada e o número de comunicações em cada estágio no processo de revisão.
  
Use o relatório para:
  
- Exibir dados para todos ou políticas específicas.
- Exibir dados agrupados por tipo de marca (por exemplo, compatível, Questionable, etc.), revisor ou tipo de mensagem.
- Exportar dados para um arquivo CSV com base na data de atividade, política e pela atividade do revisor.
- Filtre dados com base na data de atividade, tipo de marca, revisor e tipo de mensagem.

Aqui está uma divisão dos valores que talvez você veja na coluna **tipo de marca** .
  
|**Tipo de marca**|**O que significa**|
|:-----|:-----|
| Não examinado | O número de emails que ainda não foram revisadas. Esses emails são Aguardando revisão no painel de supervisão do Office 365 ou na pasta de supervisão do revisor do Outlook para o Outlook Web App.|
| Compatível com | O número de emails revisado e marcado como compatível. Essas mensagens ainda precisam ser resolvidos. |
| Questionáveis | O número de emails analisado e marcado questionável. Isso funciona como um sinalizador; outros revisores podem ajudar a verificar se um email precisa investigação para fins de conformidade. Essas mensagens ainda precisam ser resolvidos. |
| Incompatíveis (ativo) | O número de emails não compatíveis que revisores estão atualmente investigando. |
| Incompatíveis (resolvido) | O número de emails não compatíveis que revisores investigados e resolvido. |
| Política de acertos | O número total (diariamente) de mensagens do Exchange, equipes e fontes de dados de terceiros que correspondem a uma ou mais condições definidas em uma diretiva de supervisão |
| No alcance | O número total (diariamente) de mensagens do Exchange, equipes e verificados por uma política de supervisão de fontes de dados de terceiros |
| Resolvido | O número total de mensagens do Exchange, equipes e fontes de dados de terceiros que foram classificados como **resolvido**|

> [!NOTE]
> Diretivas de supervisão primeiro devem ser provisionadas antes que eles serão exibidos nesse relatório. Além disso, se as diretivas forem excluídas, dados históricos ainda são mostrados. No entanto, eles estiver indicados como "política inexistente" e a função **Exportar** não está disponível.

## <a name="auditing"></a>Auditoria

Em alguns casos, você precisará fornecer informações regulamentar ou auditores de conformidade para provar supervisão das atividades do funcionário e comunicações. Isso pode ser um resumo de todas as atividades de supervisão associados com uma diretiva definida ou sempre que uma política de supervisão foi alterada ou atualizada. As diretivas de supervisão têm trilhas de auditoria interna para preparação concluída para auditorias internas ou externas. Prova de procedimentos de supervisão pode ser demonstrada com um histórico de auditoria detalhada de cada ação monitorada pelo suas diretivas de supervisão.

As seguintes atividades de diretiva de supervisão sejam auditadas e podem ser exibidas usando os logs de auditoria do Office 365 unificados:

|**Atividade**|**Comandos associados**|
|:-----|:-----|
| Criando uma política | New-SupervisoryReviewPolicy <br> New-SupervisoryReviewRule |
| Editar uma política | Set-SupervisoryReviewPolicy <br> Set-SupervisoryReviewRule |
| Excluindo uma política| Remove-SupervisoryReviewPolicy |

As auditorias podem ser recuperadas usando a função de pesquisa de log de auditoria unificada ou usando o cmdlet do PowerShell [UnifiedAuditLog de pesquisa](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/search-unifiedauditlog) .

Por exemplo, o exemplo a seguir retorna as atividades para as todas as análise de supervisão atividades (políticas e regras) e lista as informações detalhadas para cada um:

```
Search-UnifiedAuditLog -StartDate $startDate -EndDate $endDate -RecordType DataGovernance -ResultSize 5000 | Where-Object {$_.Operations -like "*SupervisoryReview*"} | fl CreationDate,Operations,UserIds,AuditData 
```

Além das informações fornecidas nos logs e relatórios de supervisão, você também pode usar o cmdlet [Get-SupervisoryReviewActivity](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/get-supervisoryreviewactivity?view=exchange-ps) do PowerShell para retornar uma lista detalhada completa de supervisão de todas as atividades de política.

## <a name="ready-to-get-started"></a>Pronto para começar?

Para iniciar a configuração de políticas de supervisão para sua organização, consulte [Configurar diretivas de supervisão](configure-supervision-policies.md).
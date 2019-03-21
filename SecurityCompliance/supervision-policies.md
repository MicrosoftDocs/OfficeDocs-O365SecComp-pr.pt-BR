---
title: Políticas de supervisão no Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.SupervisoryReview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
- MOE150
ms.assetid: d14ae7c3-fcb0-4a03-967b-cbed861bb086
description: Noções básicas sobre políticas de supervisão no Office 365
ms.openlocfilehash: c22abdf315b2301ae9c63b26f548eff302df8e2a
ms.sourcegitcommit: fec1010e405f14e792d650aee0312b78fced3343
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/21/2019
ms.locfileid: "30720271"
---
# <a name="supervision-policies-in-office-365"></a>Políticas de supervisão no Office 365

As políticas de supervisão no Office 365 permitem que você capture comunicações de funcionários para verificação por revisores designados. Você pode definir políticas específicas que capturam emails internos e externos, Microsoft Teams ou comunicações de terceiros em sua organização. Os revisores podem, então, examinar as mensagens para garantir que estejam em conformidade com os padrões de mensagem da sua organização e resolvê-los com o tipo de classificação. Essas políticas também podem ajudá-lo a superar muitos desafios de conformidade modernos, incluindo o monitoramento de tipos crescentes de canais de comunicação, o aumento do volume de dados da mensagem e a imposição normativa &ndo o risco de multas.

Em algumas organizações, pode haver uma separação de tarefas entre o suporte de ti e o grupo de gerenciamento de conformidade. O Office 365 oferece suporte à separação entre configurar o locatário com recursos de suporte de política de supervisão e a configuração de políticas e atuar em comunicações capturadas. Por exemplo, o grupo de ti de uma organização pode ser responsável por configurar permissões e grupos de função para dar suporte a políticas de supervisão configuradas e gerenciadas pela equipe de conformidade da organização.

## <a name="scenarios-for-supervision-policies"></a>Cenários para políticas de supervisão

As políticas de supervisão podem ajudar a monitorar as comunicações em sua organização em várias áreas:

- **Políticas corporativas**

    Os funcionários devem estar em conformidade com o uso aceitável, padrões éticos e outras políticas corporativas em todas as comunicações relacionadas aos negócios. As políticas de supervisão podem detectar violações de política e ajudá-lo a realizar ações corretivas para ajudar a reduzir esses tipos de incidentes. Por exemplo, você pode monitorar sua organização em busca de possíveis violações de recursos humanos, como assédio ou uso de linguagem inadequada ou ofensiva em comunicações de funcionários.

- **Gerenciamento de risco**

    As organizações são responsáveis por todas as comunicações distribuídas por toda a infraestrutura e sistemas corporativos de rede. O uso de políticas de supervisão para ajudar a identificar e gerenciar o risco e a exposição legal em potencial pode ajudar a minimizar os riscos antes que eles possam danificar as operações corporativas. Por exemplo, você pode monitorar sua organização para comunicações não autorizadas para projetos confidenciais, como aquisições futuras, fusões, divulgação de ganhos, reorganizações ou alterações de equipe de liderança.

- **Conformidade normativa**

    A maioria das organizações deve estar em conformidade com algum tipo de padrões de conformidade normativa como parte de seus procedimentos operacionais normais. Essas regulamentações geralmente exigem que as organizações implementem algum tipo de processo de supervisão ou supervisão para mensagens que sejam apropriadas para o seu setor. A regra 3110 da autoridade de regulamentação da indústria financeira (FINRA) é um bom exemplo de um requisito para que as organizações tenham procedimentos de supervisão em vigor para monitorar as atividades de seus funcionários e os tipos de negócios nos quais ele está participando. Outro exemplo pode ser a necessidade de monitorar os revendedores do corretor em sua organização para garantir a proteção contra possíveis atividades de dinheiro-Laundering, Insider Trading, collusion ou Bribery. As políticas de supervisão podem ajudar sua organização a atender a esses requisitos fornecendo um processo para monitorar e relatar comunicações corporativas.

## <a name="feature-components"></a>Componentes de recurso

### <a name="supervision-policy"></a>Política de supervisão

Você criará políticas de supervisão no centro de conformidade do & de segurança. Essas políticas definem quais comunicações e usuários estão sujeitos a revisar em sua organização, definir condições personalizadas que as comunicações devem atender e especifica quem deve realizar revisões. Os usuários incluídos no grupo de função de análise de supervisão podem configurar políticas e qualquer pessoa que tenha essa função atribuída pode acessar a página de supervisão sob governança de dados no centro de conformidade do & de segurança do Office 365.

### <a name="supervised-users"></a>Usuários supervisionados

Antes de começar a usar a supervisão, você precisará determinar quem terá suas comunicações revisadas. Na política, você usará endereços de email do usuário para identificar pessoas ou grupos de pessoas a supervisionar. Alguns exemplos desses grupos são grupos do Office 365, listas de distribuição baseados no Exchange e canais do Microsoft Teams. Você também pode excluir usuários ou grupos específicos da supervisão que estão incluídos em um grupo supervisionado ou uma lista de grupos.

> [!IMPORTANT]
> Os usuários monitorados pelas políticas de supervisão devem ter uma licença de conformidade do Microsoft 365 e5, uma licença do Office 365 Enterprise E3 com o complemento de conformidade avançada ou ser incluída em uma assinatura do Office 365 Enterprise e5.
Se você não tem um plano Enterprise E5 existente e deseja tentar a supervisão, você pode [se inscrever para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).

### <a name="reviewers"></a>Reviewers

Ao criar uma política de supervisão, você também determinará quem executará as revisões das mensagens dos usuários supervisionados. Na política, você usará endereços de email do usuário para identificar pessoas ou grupos de pessoas para analisar comunicações supervisionadas.

### <a name="groups-for-supervised-users-and-reviewers"></a>Grupos de usuários e revisores supervisionados

Para simplificar a configuração, crie grupos para pessoas que terão suas comunicações revisadas e grupos para pessoas que examinarão essas comunicações. Se você estiver usando grupos, talvez precise de vários. Por exemplo, se você quiser monitorar comunicações entre dois grupos distintos de pessoas ou se quiser especificar um grupo que não será supervisionado.

### <a name="supported-communication-types"></a>Tipos de comunicação com suporte

Com políticas de supervisão, você pode optar por monitorar mensagens em uma ou mais das seguintes plataformas de comunicação:

- **Email do Exchange:** As caixas de correio hospedadas no Exchange Online como parte da sua assinatura do Office 365 estão qualificadas para supervisão de mensagens. Os emails e anexos que correspondem às condições de política de supervisão estão disponíveis instantaneamente para monitoramento e relatórios de supervisão. Os tipos de anexo com suporte para supervisão são os mesmos que os [tipos de arquivo com suporte para inspeções de conteúdo de regra de fluxo de email do Exchange](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/inspect-message-attachments#supported-file-types-for-mail-flow-rule-content-inspection).
- **Microsoft Teams:** Comunicações de chat e anexos associados nos canais do Microsoft Teams públicos e privados e chats individuais podem ser supervisionados. O Team chats que correspondem às condições de política de supervisão são processados uma vez a cada 24 horas e, em seguida, estão disponíveis para monitoramento e relatórios de supervisão.
- **Fontes de terceiros:** Você pode supervisionar as comunicações de fontes de terceiros (como do Facebook ou do DropBox) se tiver importado esses dados para as caixas de correio do Office 365 em sua organização. [Saiba como importar dados de terceiros para o Office 365](https://docs.microsoft.com/office365/securitycompliance/archiving-third-party-data).

### <a name="policy-settings"></a>Configurações de política

#### <a name="direction"></a>Direção

Por padrão, a **direção é** a condição é exibida e não pode ser removida. As configurações de direção de comunicação em uma política podem ser escolhidas individualmente ou juntas:

- **Entrada** -você pode escolher a **entrada** para revisar as comunicações enviadas **às** pessoas que você optou por supervisionar **de** pessoas que não estão incluídas na política.
- **Saída** -você pode escolher **saída** se quiser revisar as comunicações enviadas **de** pessoas que você optou por supervisionar **para** pessoas que não estão incluídas na política.
- **Interno** -você pode escolher **interno** para revisar as comunicações enviadas **entre** as pessoas que você identificou na política.

#### <a name="sensitive-information-types"></a>Tipos de informações confidenciais

Você tem a opção de incluir tipos de informações confidenciais como parte da sua política de supervisão. Os tipos de informações confidenciais são tipos de dados predefinidos ou personalizados que podem ajudar a identificar e proteger números de cartão de crédito, números de contas bancárias, números de passaportes e muito mais. Como parte da [DLP (prevenção de perda de dados)](data-loss-prevention-policies.md)do Office 365, a configuração de informações confidenciais pode aproveitar padrões, proximidade de caracteres, níveis de confiança e até mesmo tipos de dados personalizados para ajudar a identificar e sinalizar conteúdo que possa ser confidencial. Os tipos de informações confidenciais padrão são:

- Financeiro
- Assistência médica e saúde
- Privacidade
- Tipo de informação personalizada

Para saber mais sobre detalhes de informações confidenciais e os padrões incluídos nos tipos padrão, confira [quais tipos de informações confidenciais](what-the-sensitive-information-types-look-for.md)há.

#### <a name="custom-keyword-dictionaries"></a>Dicionários de palavras-chave personalizados

Configurar dicionários de palavras-chave personalizados (ou léxicos) pode fornecer gerenciamento simples de palavras-chave específicas para sua organização ou setor e pode suportar até 100.000 termos por dicionário. Se necessário, você pode aplicar vários dicionários de palavras-chave personalizados a uma única política ou ter um único dicionário de palavra-chave por política. Esses dicionários são atribuídos em uma política de supervisão e podem ser originados de um arquivo (como uma lista. csv ou. txt) ou de uma lista que pode ser importada [no centro de conformidade](create-a-keyword-dictionary.md).

#### <a name="conditional-settings"></a>Configurações condicionais

As condições escolhidas para a política serão aplicadas às comunicações de emails e fontes de terceiros em sua organização (como no Facebook ou no DropBox).

A tabela a seguir explica mais sobre cada condição.
  
|**Condition**|**Como usar essa condição**|
|:-----|:-----|
|A mensagem é recebida de qualquer um desses domínios  <br><br> A mensagem não é recebida de nenhum desses domínios | Para aplicar a política quando determinados domínios são incluídos ou excluídos em uma mensagem recebida, insira cada domínio e separe vários domínios com uma vírgula. Cada domínio inserido será aplicado separadamente (apenas um desses domínios deve ser aplicado à política para aplicar à mensagem). |
|A mensagem é enviada para qualquer um desses domínios  <br><br> A mensagem não é enviada a nenhum desses domínios | Para aplicar a política quando determinados domínios são incluídos ou excluídos em uma mensagem enviada, insira cada domínio e separe vários domínios com uma vírgula. Cada domínio inserido será aplicado separadamente (apenas um desses domínios deve ser aplicado à política para aplicar à mensagem). |
|A mensagem é classificada com qualquer um desses rótulos  <br><br> A mensagem não é classificada com nenhum desses rótulos | Para aplicar a política quando determinados rótulos de retenção são incluídos ou excluídos em uma mensagem. Os rótulos de retenção devem ser configurados separadamente e os rótulos configurados podem ser escolhidos como parte dessa condição. Cada rótulo escolhido será aplicado separadamente (somente um desses rótulos deve se aplicar à política para aplicar à mensagem). Para obter mais informações sobre a configuração de rótulos de retenção, consulte [Overview of Retention Labels](https://docs.microsoft.com/office365/securitycompliance/labels).|
|A mensagem contém qualquer uma destas palavras  <br><br> A mensagem não contém nenhuma destas palavras | Para aplicar a política quando determinadas palavras ou frases forem incluídas ou excluídas em uma mensagem, insira cada palavra ou frase em uma linha separada. Cada linha de palavras inserida será aplicada separadamente (apenas uma destas linhas deve ser aplicada para que a política seja aplicada à mensagem). Para saber mais sobre como inserir palavras ou frases, consulte a próxima seção [Matching words and phrases to emails or attachments](supervision-policies.md#Matchwords).|
|O anexo contém qualquer uma destas palavras  <br><br> O anexo não contém nenhuma destas palavras | Para aplicar a política quando determinadas palavras ou frases forem incluídas ou excluídas em um anexo de mensagem (como um documento do Word), insira cada palavra ou frase em uma linha separada. Cada linha de palavras inserida será aplicada separadamente (somente uma linha deve ser aplicada à política para ser aplicada ao anexo). Para saber mais sobre como inserir palavras ou frases, consulte a próxima seção [Matching words and phrases to emails or attachments](supervision-policies.md#Matchwords).|
|O anexo é qualquer um desses tipos de arquivo  <br><br> O anexo não é nenhum desses tipos de arquivo | Para supervisionar as comunicações que incluem ou excluem tipos específicos de anexos, insira as extensões de arquivo (como. exe ou. pdf). Se você quiser incluir ou excluir várias extensões de arquivo, insira-as em linhas separadas. Basta apenas uma correspondência de extenção de anexo para que a política seja aplicada.|
|O tamanho da mensagem é maior do que  <br><br> O tamanho da mensagem não é maior que | Para revisar mensagens com base em um determinado tamanho, use essas condições para especificar o tamanho máximo ou mínimo que uma mensagem pode ser antes de estar sujeita a revisão. por exemplo, se você especificar o **tamanho da mensagem é maior que** \> **1,0 MB**, todas as mensagens com 1, 1 mb ou mais serão sujeitas à revisão. Você pode optar por bytes, kilobytes, megabytes ou gigabytes para essa condição.|
|O anexo é maior que  <br><br> O anexo não é maior que | Para revisar mensagens com base no tamanho de seus anexos, especifique o tamanho máximo ou mínimo que um anexo pode ser antes da mensagem e seus anexos estão sujeitos à revisão. por exemplo, se você especificar que o **anexo é maior do que** \> **2,0 MB**, todas as mensagens com anexos de 2, 1 MB e mais serão sujeitas à revisão. Você pode optar por bytes, kilobytes, megabytes ou gigabytes para essa condição.|
   
##### <a name="matching-words-and-phrases-to-emails-or-attachments"></a>Palavras e frases correspondentes a emails ou anexos
<a name="Matchwords"> </a>

Cada linha de palavras inserida será aplicada separadamente (somente uma linha deve ser aplicada à condição de política a ser aplicada ao email ou anexo). Por exemplo, vamos usar a condição, a **mensagem contém qualquer uma destas palavras**, com as palavras-chave "banco" e "comércio Insider" em linhas separadas. A política será aplicada a qualquer mensagem que inclua a palavra "banco" ou a frase "insider trading". Apenas uma destas palavras ou frases deve ocorrer para que se aplique a condição dessa política. Palavras na mensagem ou anexo devem corresponder exatamente ao que você inserir.
  
##### <a name="entering-multiple-conditions"></a>Inserindo várias condições

Se você inserir várias condições, o Office 365 usará todas as condições juntas para determinar quando aplicar a política a itens de comunicação. Quando você configura várias condições, todas elas devem ser atendidas para que a política seja aplicada, a menos que você digite uma exceção. Por exemplo, digamos que você precise criar uma política que deve ser aplicada se uma mensagem contiver a palavra "comércio" e maior do que 2MB. No enTanto, se a mensagem também contiver as palavras "aprovadas pela contoso Financial", a política não deverá ser aplicada. Portanto, nesse caso, as três condições seriam as seguintes:
  
- A **mensagem contém qualquer uma destas palavras**, com as palavras-chave "trade"

- O **tamanho da mensagem é maior que**, com o valor 2 MB

- A **mensagem contém nenhuma destas palavras**, com as palavras-chave "aprovadas pela equipe financeira da Contoso".

#### <a name="review-percentage"></a>Porcentagem de revisão

Você pode especificar uma porcentagem de todas as comunicações governadas por uma política de supervisão se quiser reduzir a quantidade de conteúdo a ser revisado. Selecionaremos aleatoriamente essa quantidade de conteúdo da porcentagem total que corresponde às condições escolhidas. Se quiser que os revisores Revisem todos os itens, você pode inserir **100%** em uma política de supervisão.

## <a name="monitoring--managing"></a>Monitoramento do & gerenciamento

Monitorar os resultados de suas políticas de supervisão e aplicar uma marca de resolução é fácil e conveniente. Você pode ver rapidamente o status dos itens revisados, os usuários e grupos em supervisão e os usuários e grupos designados como revisores.

### <a name="supervision-policy-dashboard"></a>Painel de política de supervisão

A maneira mais fácil de gerenciar os resultados da política de supervisão e resolver itens pendentes é usar o painel de política de supervisão. Este painel permite que os revisores vejam rapidamente os itens que precisam ser revisados, executem ações em um item e analise os resultados de itens previamente revisados e resolvidos para cada política de supervisão. você pode acessar o painel de política de supervisão no centro de conformidade do & de segurança do Office 365 em **supervisão** > *de sua política* > personalizada**aberta**.

#### <a name="dashboard-home"></a>Página inicial do painel

A **Home** Page do painel tem várias seções para ajudá-lo a tomar medidas rapidamente em suas políticas de supervisão. Aqui você pode:

- Revise rapidamente os destaques pendentes e resolvidos da semana
- Ver uma lista dos usuários supervisionados e dos grupos supervisionados da política selecionada
- Ver uma lista dos revisores e das equipes de revisão da política selecionada
- Veja quais plataformas de comunicação têm conteúdo sob supervisão para a política.

#### <a name="review-tab"></a>Guia revisão

A guia **revisão** é onde os revisores podem executar a ação e resolver itens identificados pela política selecionada. Aqui você pode:

- Filtrar por itens pendentes, compatíveis, não compatíveis e questionáveis
- Marcar um item único como compatível, não compatível ou questionável. Você também pode gravar um comentário com o item para ajudar a esclarecer a ação de marcação executada.
- Marcar vários itens em massa como em conformidade, não compatível ou questionável. Você também pode gravar um comentário com vários itens para ajudar a esclarecer a ação de marcação executada.
- Exibir o histórico da marcação de um único item, incluindo quem resolveu o item, a data e a hora da ação, a marca de resolução e quaisquer comentários incluídos.
- Reclassificar itens revisados anteriormente como em conformidade, não compatível ou questionável. Você também pode gravar um comentário com um ou vários itens para ajudar a esclarecer a ação de reclassificação executada.

#### <a name="resolved-items-tab"></a>Guia itens resolvidos

A guia **itens resolvidos** é onde os revisores podem exibir todos os itens resolvidos anteriormente para a política selecionada. Aqui você pode:

- Exibir e classificar rapidamente o assunto, o remetente e a data de itens resolvidos.
- Exibir o histórico de comentários e classificação de qualquer item selecionado

### <a name="other-ways-to-review-items"></a>Outras maneiras de revisar itens

Se os revisores preferem não usar o painel de supervisão no Office 365, eles também têm outras opções para revisar e gerenciar itens coletados por políticas de supervisão.

#### <a name="outlook-on-the-web"></a>Outlook na Web

Os usuários designados como revisores em uma política de supervisão podem usar o Outlook na Web para analisar e resolver os itens de supervisão. O suplemento de supervisão é instalado automaticamente no Outlook na Web para todos os revisores que você especificou na política. Nenhuma configuração adicional é necessária para sua organização para que as pastas compartilhadas da política de supervisão estejam disponíveis para revisores configurados.

Usando o Outlook na Web, os revisores podem:

- Exibir itens filtrados por status de conformidade, sem conformidade, questionável e resolvido
- Marcar um item único como compatível, não compatível, questionável ou resolvido. Você também pode gravar um comentário com o item para ajudar a esclarecer a ação de marcação executada.
- Exibir o histórico da marcação de um único item, incluindo quem resolveu o item, a data e a hora da ação, a marca de resolução e quaisquer comentários incluídos.
- Reclassificar itens revisados anteriormente como em conformidade, não compatível ou questionável. Você também pode gravar um comentário com itens únicos para ajudar a esclarecer a ação de reclassificação executada.

#### <a name="microsoft-outlook"></a>Microsoft Outlook

Para revisar as comunicações identificadas por uma política de supervisão, os revisores também podem usar o suplemento de supervisão para o Microsoft Outlook. No enTanto, os revisores devem ser executados por meio de algumas etapas para instalá-lo na versão da área de trabalho do Outlook. Para obter orientações detalhadas sobre como instalar o suplemento de supervisão para o Outlook, consulte [Configure supervisão Policies](configure-supervision-policies.md).

Usando o Outlook, os revisores podem:

- Exibir itens filtrados por status de conformidade, sem conformidade, questionável e resolvido
- Marcar um item único como compatível, não compatível, questionável ou resolvido. Você também pode gravar um comentário com o item para ajudar a esclarecer a ação de marcação executada.
- Exibir o histórico da marcação de um único item, incluindo quem resolveu o item, a data e a hora da ação, a marca de resolução e quaisquer comentários incluídos.
- Reclassificar itens revisados anteriormente como em conformidade, não compatível ou questionável. Você também pode gravar um comentário com itens únicos para ajudar a esclarecer a ação de reclassificação executada.

## <a name="reporting"></a>Reporting

Use os relatórios de supervisão para ver a atividade de análise no nível de política e de revisor. Para cada política, você também pode exibir estatísticas dinâmicas no estado atual da atividade de análise. Você pode usar os relatórios de supervisão para:
  
- Verifique se as políticas estão funcionando conforme desejado.
- Descubra quantas comunicações estão sendo identificadas para revisão.
- Descubra quantas comunicações não estão em conformidade e quais estão passando revisão. Essas informações podem ajudá-lo a decidir se deve ajustar suas políticas ou alterar o número de revisores.

### <a name="view-the-supervision-report"></a>Exibir o relatório de supervisão

1. Entre no [centro de conformidade do & de segurança](https://protection.office.com/) usando as credenciais de uma conta de administrador na sua organização do Office 365 que tenha permissões para exibir relatórios de supervisão.
2. Vá para o **** \> **painel** de relatórios ou **supervisão**. Você verá um widget relatório de supervisão com um resumo da atividade atual de política de supervisão.
3. Selecione o widget **supervisão** para abrir a página relatório detalhado.

> [!NOTE]
> Se você não conseguir acessar a página **relatórios** , verifique se você é membro do grupo de função de análise de supervisão, conforme descrito em [disponibilizar supervisão disponível em sua organização](configure-supervision-policies.md). Ser incluído nesse grupo de função permite que você crie e gerencie políticas de supervisão e execute o relatório.
  
### <a name="how-to-use-the-report"></a>Como usar o relatório

Quando uma política de supervisão identifica uma mensagem de comunicação para revisão, o email é entregue na pasta de supervisão do revisor no Outlook e no Outlook na Web (anteriormente conhecido como Outlook Web App). Este relatório lista o nome de cada política e o número de comunicações em cada estágio no processo de revisão.
  
Use o relatório para:
  
- Exibir dados para todas as políticas ou para políticas específicas.
- Exibir dados agrupados por tipo de marca (como compatível, questionável, etc.), revisor ou tipo de mensagem.
- Exportar dados para um arquivo CSV com base na data da atividade, política e pela atividade do revisor.
- Filtrar dados com base na data da atividade, no tipo de marca, no revisor e no tipo de mensagem.

Aqui está uma divisão dos valores que podem ser exibidos na coluna **tipo de marca** .
  
|**Tipo de marca**|**O que significa**|
|:-----|:-----|
| Não reVisado | O número de emails que ainda não foram revisados. Estes emails estão aguardando revisão no painel de supervisão do Office 365 ou na pasta de supervisão do revisor no Outlook/Outlook na Web
| Compliant | O número de emails revisados e marcados como em conformidade. Essas mensagens ainda precisam ser resolvidas. |
| Questionáveis | O número de emails revisados e marcados como questionáveis. Isso atua como um sinalizador; outros revisores podem ajudar a verificar se um email precisa de investigação de conformidade. Essas mensagens ainda precisam ser resolvidas. |
| Não compatível (ativo) | O número de emails não compatíveis que os revisores estão investigando no momento. |
| Não compatível (resolvido) | O número de emails não compatíveis que os revisores investigaram e resolveram. |
| Política de hit | O número total (diário) de mensagens do Exchange, do Microsoft Teams e de fontes de dados de terceiros que correspondem a uma ou mais condições definidas em uma política de supervisão |
| No âmbito | O número total (diário) de mensagens do Exchange, do Microsoft Teams e de fontes de dados de terceiros verificados por uma política de supervisão |
| Resolvido | O número total de mensagens do Exchange, do Microsoft Teams e de fontes de dados de terceiros que foram **** classificadas como resolvidas|

> [!NOTE]
> As políticas de supervisão devem primeiro ser provisionadas para que apareçam no relatório. Além disso, se as políticas forem excluídas, os dados históricos ainda serão exibidos. No enTanto, eles são indicados como uma política não existente e a função de **exportação** não está disponível.

## <a name="auditing"></a>Auditoria

Em alguns casos, você precisará fornecer informações a auditores normativos ou de conformidade para provar a supervisão de atividades e comunicações de funcionários. Isso pode ser um resumo de todas as atividades de supervisão associadas a uma política definida ou sempre que uma política de supervisão foi alterada ou atualizada. As políticas de supervisão têm trilhas de auditoria internas para uma preparação completa para auditorias internas ou externas. A prova de procedimentos de supervisão pode ser demonstrada com um histórico de auditoria detalhado de todas as ações monitoradas por suas políticas de supervisão.

As seguintes atividades de política de supervisão são auditadas e podem ser exibidas usando os logs de auditoria unificados do Office 365:

|**Atividades**|**Comandos associados**|
|:-----|:-----|
| Criar uma política | [New-SupervisoryReviewPolicyV2](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-supervisoryreviewpolicyv2) <br> [New-SupervisoryReviewRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-supervisoryreviewrule) |
| Editando uma política | [Set-SupervisoryReviewPolicyV2](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/set-supervisoryreviewpolicyv2) <br> [Set-SupervisoryReviewRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/set-supervisoryreviewrule) |
| Excluindo uma política| [Remove-SupervisoryReviewPolicyV2](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/remove-supervisoryreviewpolicyv2) |
| Exibindo uma política | [Get-SupervisoryReviewPolicyV2](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/get-supervisoryreviewpolicyv2) |

As auditorias podem ser recuperadas usando a função de pesquisa de log de auditoria unificada ou usando o cmdlet [Search-UnifiedAuditLog](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/search-unifiedauditlog) do PowerShell.

Por exemplo, o exemplo a seguir retorna as atividades para todas as atividades de análise de supervisão (políticas e regras) e lista informações detalhadas de cada:

```
Search-UnifiedAuditLog -StartDate 3/1/2019 -EndDate ([System.DateTime]::Now) -RecordType DataGovernance -ResultSize 5000 | Where-Object {$_.Operations -like "*SupervisoryReview*"}  | fl CreationDate,Operations,UserIds,AuditData
```

Além das informações fornecidas nos logs e relatórios de supervisão, você também pode usar o cmdlet [Get-SupervisoryReviewActivity](https://docs.microsoft.com/powershell/module/exchange/reporting/get-supervisoryreviewactivity?view=exchange-ps) do PowerShell para retornar uma listagem detalhada completa de todas as atividades de política de supervisão.

## <a name="ready-to-get-started"></a>Pronto para começar?

Para começar a configurar as políticas de supervisão para sua organização, consulte [Configure supervisão Policies](configure-supervision-policies.md).
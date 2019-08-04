---
title: Solicitações do Sistema de Proteção de Dados do Cliente do Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
audience: Admin
ms.topic: troubleshooting
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
search.appverid:
- BCS160
- MET150
- MOE150
description: Saiba mais sobre as solicitações de lockbox de clientes que permitem controlar como um engenheiro de suporte da Microsoft pode acessar seus dados quando você se deparar com um problema.
ms.openlocfilehash: 2cbf19ad3c648373704c379794e24590fcb6d290
ms.sourcegitcommit: f0d23e57b00f07cef5b1b2d366eaeeeacda37e3e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2019
ms.locfileid: "35786616"
---
# <a name="customer-lockbox-in-office-365"></a>Lockbox de cliente no Office 365

> [!NOTE]
> Este artigo fornece orientações de implantação e configuração para um recurso atualmente disponível apenas para organizações que têm um Microsoft 365 e5, o Office 365 e5, a proteção de informações e conformidade ou a assinatura de complemento de conformidade avançada.

A Lockbox do cliente garante que a Microsoft não possa acessar seu conteúdo para executar uma operação de serviço sem a sua aprovação explícita. O Lockbox do cliente o coloca no fluxo de trabalho de aprovação para solicitações de acesso ao seu conteúdo.

Ocasionalmente, os engenheiros da Microsoft ajudam a solucionar problemas e corrigir problemas relatados pelo cliente no processo de suporte. Normalmente, os problemas são corrigidos por ferramentas de telemetria e depuração abrangentes que a Microsoft tem em vigor para seus serviços. No entanto, alguns casos exigem um engenheiro da Microsoft para acessar o conteúdo do cliente para determinar a causa raiz e corrigir o problema. A Lockbox do cliente exige que o engenheiro solicite acesso do cliente como uma etapa final no fluxo de trabalho de aprovação. Isso oferece às organizações a opção de aprovar ou negar essas solicitações e fornecer controle de acesso direto ao cliente.

### <a name="customer-lockbox-overview-video"></a>Vídeo visão geral da Lockbox de clientes

> [!VIDEO https://www.microsoft.com/videoplayer/embed/8fecf10b-1f03-4849-8b67-76d3d2a43f26?autoplay=false]

> [!NOTE]
> O Lockbox do cliente oferece suporte a solicitações de acesso a dados no Exchange Online, no SharePoint Online e no OneDrive for Business. Para recomendar o suporte para outros serviços do Office 365, envie uma solicitação no [Office 365 UserVoice](https://office365.uservoice.com/).

## <a name="customer-lockbox-workflow"></a>Fluxo de trabalho de lockbox do cliente

As etapas a seguir descrevem o fluxo de trabalho típico quando uma solicitação de lockbox do cliente é iniciada por um engenheiro da Microsoft:

1. Alguém em uma organização tem um problema com sua caixa de correio do Office 365.

2. Depois que o usuário solucionar o problema, mas não conseguir corrigi-lo, ele abrirá uma solicitação de suporte com o suporte da Microsoft.

3. Um engenheiro de suporte revisa a solicitação de serviço e determina a necessidade de acessar o conteúdo do Exchange Online do cliente para reparar o problema.

4. O engenheiro de suporte faz logon na ferramenta de solicitação de lockbox do cliente e faz uma solicitação de acesso aos dados especificando o nome do locatário do cliente, o número da solicitação de serviço e a duração estimada para a qual o acesso aos dados é necessário.

5. Depois que um gerente de suporte da Microsoft aprova a solicitação, o Lockbox do cliente envia o aprovador designado na organização do cliente uma notificação por email sobre a solicitação de acesso pendente da Microsoft.

    ![Exemplo de notificação de email de lockbox de cliente](media/CustomerLockbox1.png)

   > [!NOTE]
   > Qualquer pessoa que tenha atribuído a função de administrador do aprovador de [acesso de lockbox do cliente](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) no centro de administração do Microsoft 365 pode aprovar as solicitações de lockbox do cliente.

7. O aprovador entra no centro de administração do Microsoft 365 e aprova a solicitação. Esta etapa dispara a criação de um registro de auditoria disponível pesquisando o log de auditoria do Office 365. Para obter mais informações, consulte a seção [solicitações de lockbox de cliente de auditoria](#auditing-customer-lockbox-requests) .

   Se o cliente rejeitar a solicitação ou a solicitação não for aprovada dentro de 12 horas, a solicitação expirará e nenhum acesso será concedido ao engenheiro da Microsoft.

   > [!IMPORTANT]
   > A Microsoft não inclui nenhum link em notificações por email de lockbox de clientes que exijam que você entre no Office 365.

8. Depois que o cliente aprova a solicitação, o engenheiro da Microsoft recebe a mensagem de aprovação, faz logon no Exchange Online e corrige o problema do cliente. Os engenheiros da Microsoft têm a duração solicitada para corrigir o problema após o qual o acesso é automaticamente revogado.

> [!NOTE]
> Todas as ações executadas por um engenheiro da Microsoft são registradas no log de auditoria do Office 365. Você pode pesquisar e revisar esse registro de auditoria e pode ser pesquisada e revisada.

## <a name="turn-customer-lockbox-requests-on-or-off"></a>Ativar ou desativar solicitações de lockbox do cliente

Um administrador do Office 365 pode ativar os controles de lockbox do cliente no centro de administração do Microsoft 365. Quando a Lockbox do cliente está ativada, a Microsoft é obrigada a obter aprovação de uma organização antes de acessar qualquer um de seus conteúdos.

> [!NOTE]
> Para executar o procedimento a seguir, você deve ser um administrador global em sua organização do Microsoft 365 ou do Office 365 ou receber a função de administrador do aprovador de **acesso de lockbox do cliente** .

1. Acesse [https://admin.microsoft.com](https://admin.microsoft.com) e entre com sua conta corporativa ou de estudante.

2. Clique em **configurações > segurança & privacidade**.

    ![Editar as configurações de lockbox do cliente no centro de administração](media/CustomerLockbox2.png)

3. No bloco de **Lockbox do cliente** , clique em **Editar**e, em seguida, mova a opção para **ativado** ou **desativado** para ativar ou desativar o recurso.

    ![Require approval for Customer Lockbox](media/CustomerLockbox4.png)

## <a name="approve-or-deny-a-customer-lockbox-request"></a>Aprovar ou negar uma solicitação de lockbox do cliente

> [!NOTE]
> Para executar o procedimento a seguir, você deve ser um administrador global em sua organização do Microsoft 365 ou do Office 365 ou receber a função de administrador do aprovador de **acesso de lockbox do cliente** .

1. Acesse [https://admin.microsoft.com](https://admin.microsoft.com) e entre com sua conta corporativa ou de estudante.

2. Clique em **suporte > solicitações de lockbox do cliente**.

    ![Clique em suporte e, em seguida, clique em solicitações de lockbox do cliente](media/CustomerLockbox5.png)

    Uma lista de solicitações de lockbox do cliente é exibida.

    ![Lista de solicitações de lockbox do cliente](media/CustomerLockbox6.png)

3. Selecione uma solicitação de lockbox de cliente e clique em **aprovar** ou **negar**.

    ![Aprovar ou negar solicitações de lockbox do cliente](media/CustomerLockbox7.png)

    É exibida uma mensagem de confirmação sobre a aprovação da solicitação de lockbox do cliente.

    ![Aprovar ou negar solicitações de lockbox do cliente](media/CustomerLockbox8.png)

## <a name="auditing-customer-lockbox-requests"></a>Auditar solicitações de lockbox do cliente 

Os registros de auditoria que correspondem às solicitações de lockbox do cliente são registrados no log de auditoria do Office 365 e podem ser acessados por meio da [ferramenta de pesquisa de log de auditoria](https://docs.microsoft.com/office365/securitycompliance/search-the-audit-log-in-security-and-compliance) no centro de conformidade & segurança do Office 365. As ações relacionadas a um cliente que aceita ou nega uma solicitação de lockbox de cliente e ações executadas por engenheiros da Microsoft (quando as solicitações de acesso são aprovadas) são registradas no log de auditoria do Office 365. Você pode pesquisar e revisar esses registros de auditoria.

> [!NOTE]
> Você precisa receber a função de logs de auditoria somente para exibição ou logs de auditoria no Exchange Online para pesquisar o log de auditoria do Office 365. Para saber mais, confira [Pesquisar o log de auditoria no Centro de Conformidade e Segurança do Office 365](https://docs.microsoft.com/en-us/office365/securitycompliance/search-the-audit-log-in-security-and-compliance#before-you-begin).

### <a name="search-the-audit-log-for-activity-related-to-customer-lockbox-requests"></a>Pesquisar o log de auditoria para atividades relacionadas às solicitações de lockbox do cliente

Confira aqui como criar uma consulta de pesquisa de log de auditoria para retornar registros de auditoria relacionados à Lockbox do cliente:

1. Acesse [https://protection.office.com](https://protection.office.com).
  
2. Entre no Office 365 usando a sua conta corporativa ou de estudante.

3. No painel esquerdo do centro de conformidade & segurança, clique em Pesquisar **&** > **pesquisa de log de auditoria**.

    A página **pesquisa de log de auditoria** é exibida.

    ![Página pesquisa de log de auditoria](media/auditlogsearch1.png)
  
4. Configure os seguintes critérios de pesquisa:

    a. **Atividades** -deixe este campo em branco para que a pesquisa retorne registros de auditoria de todas as atividades. Isso é necessário para retornar registros de auditoria relacionados às solicitações de lockbox do cliente e à atividade correspondente executada pelos engenheiros da Microsoft.

    b. **Data de início** e **data de término** -selecione um intervalo de data e hora para exibir os eventos que ocorreram dentro desse período.

    c. **Usuários** -deixe este campo em branco.

    d. **Arquivo, pasta ou site** -deixe este campo em branco.

5. Clique em **Pesquisar** para executar a pesquisa usando seus critérios de pesquisa. 

    Os resultados da pesquisa são carregados e após alguns momentos em que são exibidos em **resultados** na página **pesquisa de log de auditoria** .

6. Clique em **filtrar resultados** na página de resultados da pesquisa e siga um destes procedimentos:

   - Para exibir registros de auditoria relacionados a um Aprovador em sua organização aprovar ou negar uma solicitação de lockbox de cliente: na caixa da coluna **atividade** , digite **set-AccessToCustomerDataRequest**.

   - Para exibir registros de auditoria relacionados a um engenheiro da Microsoft executando ações em resposta a uma solicitação de lockbox de cliente aprovado: na caixa abaixo da coluna **usuário** , digite **operador da Microsoft**. Observe que a ação executada pelo engenheiro é exibida int a coluna **atividade** .

      ![Filtro em "operador da Microsoft" para exibir registros de auditoria](media/CustomerLockbox10.png)

7. Na lista de resultados, clique em um registro de auditoria para exibi-lo.

### <a name="audit-record-for-a-customer-lockbox-access-request"></a>Registro de auditoria para uma solicitação de acesso de lockbox do cliente

Quando uma pessoa em sua organização aprova ou nega uma solicitação de lockbox do cliente, um registro de auditoria é registrado no log de auditoria do Office 365. Este registro contém as informações a seguir. 

| Propriedade do registro de auditoria| Descrição|
|:---------- |:----------|
| Date       | A data e a hora em que a solicitação de lockbox do cliente foi aprovada ou negada.
| Endereço IP | O endereço IP do computador que o aprovador usou para aprovar ou negar uma solicitação. |
| Usuário       | A conta de serviço BOXServiceAccount\[@\]customerforest. Prod.Outlook.com.            |
| Atividade   | Set-AccessToCustomerDataRequest; Esta é a atividade de auditoria que é registrada quando você aprova ou nega uma solicitação de lockbox do cliente.                                |
| Item       | O GUID da solicitação de lockbox do cliente                             |

A captura de tela a seguir mostra um exemplo de um registro de log de auditoria que corresponde a uma solicitação de lockbox de cliente aprovado. Se uma solicitação de lockbox do cliente tiver sido negada, o valor do parâmetro **ApprovalDecision** seria **negado**.

![Registro de auditoria para uma solicitação de lockbox de cliente aprovada](media/CustomerLockbox9.png)

> [!TIP]
> Para exibir informações mais detalhadas em um registro de auditoria, clique em **mais informações**.

### <a name="audit-record-for-an-action-performed-by-a-microsoft-engineer"></a>Registro de auditoria para uma ação executada por um engenheiro da Microsoft

Conforme explicado anteriormente, as ações executadas por um engenheiro da Microsoft depois que uma solicitação de lockbox de cliente é aprovada (e que pode resultar no acesso ao conteúdo do cliente) são registradas no log de auditoria. Esses registros contêm as informações a seguir.

| Propriedade do registro de auditoria| Descrição|
|:---------- |:----------|
| Date       | Data e hora em que a ação foi executada. Observe que a hora em que essa ação foi executada estará dentro de 4 horas após a aprovação da solicitação de lockbox do cliente.              |
| Endereço IP | O endereço IP do engenheiro de máquina da Microsoft usado. |
| Usuário       | Operador da Microsoft; Esse valor indica que esse registro está relacionado a uma solicitação de lockbox do cliente.                                  |
| Atividade   | Nome da atividade realizada pelo engenheiro da Microsoft.|
| Item       | \<Empty\>                                             |


## <a name="frequently-asked-questions"></a>Perguntas frequentes

#### <a name="which-office-365-services-does-customer-lockbox-apply-to"></a>Para quais serviços do Office 365 a Lockbox do cliente se aplica?

No momento, o Lockbox do cliente é compatível com o Exchange Online, o SharePoint Online e o OneDrive for Business.

#### <a name="is-customer-lockbox-available-to-all-office-365-customers"></a>A Lockbox de cliente está disponível para todos os clientes do Office 365?

O Lockbox do cliente está incluído nas assinaturas do Microsoft 365 ou do Office 365 E5 e pode ser adicionado a outros planos com proteção e conformidade de informações ou uma assinatura complementar de conformidade avançada. Confira [planos e preços](https://products.office.com/business/office-365-enterprise-e5-business-software) para obter mais informações.

#### <a name="what-is-customer-content"></a>O que é conteúdo do cliente?

O conteúdo do cliente é os dados criados por usuários dos serviços e aplicativos do Office 365. Exemplos de conteúdo do cliente incluem:

- Envio de email ou anexos de email

- Conteúdo do site do SharePoint

- Informações no corpo de um arquivo do SharePoint

- Corpo do arquivo de apresentação do Skype for Business

- Mensagens instantâneas (IM) ou conversas de voz

- Blob gerado pelo cliente ou dados de armazenamento estruturados (por exemplo, contêineres SQL)

- Informações de segurança de Propriedade do cliente (por exemplo, certificados, chaves de criptografia e senhas)

- Inferências e todas as inferências subsequentes, se o conteúdo do cliente permanecer

Para obter informações adicionais sobre o conteúdo do cliente no Office 365, consulte a [central de confiabilidade do office 365](https://products.office.com/en-US/business/office-365-trust-center-privacy/).

#### <a name="who-is-notified-when-there-is-a-request-to-access-my-content"></a>Quem é notificado quando há uma solicitação para acessar meu conteúdo?

Os administradores globais e qualquer pessoa que tenha atribuído a função de administrador de aprovador do acesso de lockbox do cliente são notificados. Eles também são os mesmos usuários que podem aprovar solicitações de lockbox do cliente.

#### <a name="who-can-approve-or-reject-these-requests-in-my-organization"></a>Quem pode aprovar ou rejeitar essas solicitações em minha organização?

Os administradores globais e qualquer pessoa que tenha atribuído a função de administrador do aprovador de acesso de lockbox do cliente podem aprovar solicitações de lockbox do cliente. Os clientes controlam essas atribuições de função em suas organizações.

#### <a name="how-do-i-opt-in-to-customer-lockbox"></a>Como posso me inscrever no Lockbox de cliente?

Um administrador global pode habilitar e configurar o Lockbox do cliente no centro de administração do Microsoft 365 ou do Microsoft 365.

#### <a name="if-i-approve-a-customer-lockbox-request-what-can-the-engineer-do-and-how-will-i-know-what-the-microsoft-engineer-did"></a>Se eu aprovar uma solicitação de lockbox do cliente, o que o engenheiro pode fazer e como saberei o que o engenheiro da Microsoft fazia?

Depois que você aprova uma solicitação de lockbox do cliente, o engenheiro da Microsoft concedeu esses privilégios necessários para acessar o conteúdo do cliente usando cmdlets pré-aprovados. Ações executadas por engenheiros da Microsoft em resposta a solicitações de lockbox do cliente são registradas e acessíveis no log de auditoria no centro de conformidade & segurança do Office 365.

#### <a name="how-do-i-know-that-microsoft-follows-the-approval-process"></a>Como saber se a Microsoft segue o processo de aprovação?

Você pode fazer referência cruzada as notificações de aprovação de email enviadas para administradores e aprovadores em sua organização com o histórico de solicitação de lockbox do cliente no centro de administração do Microsoft 365.

O Lockbox do cliente está incluído no relatório de auditoria mais recente do [SOC 1 SSAE 16](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=91592749-e86a-43ac-801e-121382614681&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_SOC%20%2F%20SSAE%2016%20Reports). Para obter mais detalhes, você pode encontrar os relatórios mais recentes no [portal de confiança do serviço Microsoft](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=91592749-e86a-43ac-801e-121382614681&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_SOC%20%2F%20SSAE%2016%20Reports).

#### <a name="can-microsoft-modify-the-list-of-approvers-for-my-tenant-if-not-how-is-it-prevented"></a>A Microsoft pode modificar a lista de aprovadores para meu locatário? Caso contrário, como ela é impedida?

Somente um administrador global em sua organização pode especificar quem pode aprovar as solicitações de lockbox do cliente. Isso significa que somente os membros do grupo de administradores global no Azure Active Directory podem especificar quem pode aprovar a solicitação. A associação ao grupo de administradores global no Azure Active Directory é gerenciada apenas pela sua organização.

#### <a name="what-if-i-need-more-information-about-a-content-access-request-to-approve-it"></a>E se eu precisar de mais informações sobre uma solicitação de acesso ao conteúdo para aprová-la?

Cada solicitação de lockbox de cliente contém um número de solicitação de serviço do Office 365. Você pode entrar em contato com o suporte da Microsoft e fazer referência a esse número de serviço para obter mais informações sobre a solicitação.

#### <a name="when-a-customer-lockbox-request-is-approved-how-long-are-the-permissions-valid"></a>Quando uma solicitação de lockbox de cliente é aprovada, quanto tempo as permissões são válidas?

Atualmente, o período máximo para as permissões de acesso concedidas ao engenheiro da Microsoft é de quatro horas. O engenheiro da Microsoft também pode solicitar um período mais curto.

#### <a name="how-can-i-get-a-history-of-all-customer-lockbox-requests"></a>Como posso obter um histórico de todas as solicitações de lockbox do cliente?

Todas as solicitações de lockbox do cliente são exibidas no centro de administração do Microsoft 365.

#### <a name="how-do-i-correlate-the-content-access-requests-with-the-related-audit-logs"></a>Como faço para correlacionar as solicitações de acesso de conteúdo com os logs de auditoria relacionados?

O feed de atividades do centro de conformidade contém atividades de log de lockbox de cliente. Os clientes podem fazer referência cruzada às atividades de log de lockbox do cliente do feed de atividades em relação à solicitação de email recebida.

#### <a name="what-happens-when-a-customer-doesnt-respond-to-a-customer-lockbox-request"></a>O que acontece quando um cliente não responde a uma solicitação de lockbox do cliente?

As solicitações de lockbox do cliente têm uma duração padrão de 12 horas. Se você não responder a uma solicitação dentro de 12 horas, a solicitação expirará.

#### <a name="what-does-microsoft-do-when-a-customer-rejects-a-customer-lockbox-request"></a>O que a Microsoft faz quando um cliente rejeita uma solicitação de lockbox do cliente?

Se um cliente rejeitar uma solicitação de lockbox do cliente, não ocorrerá nenhum acesso ao conteúdo do cliente. Se um usuário da sua organização continuar a enfrentar um problema de serviço que requer que a Microsoft acesse o conteúdo do cliente para resolver o problema, o problema de serviço pode persistir e a Microsoft informará o usuário sobre isso.

#### <a name="does-customer-lockbox-protect-against-data-requests-from-law-enforcement-agencies-or-other-third-parties"></a>A Lockbox do cliente protege contra solicitações de dados de agências de imposição de leis ou outras terceiros?

Não. A Microsoft leva seriamente as solicitações de terceiros aos dados dos clientes. Como um provedor de serviços de nuvem, a Microsoft sempre defende a privacidade dos dados dos clientes. No evento, obtemos uma intimação, a Microsoft sempre tenta redirecionar o terceiro para o cliente para obter as informações. (Leia o blog de Brad Smith: [proteção dos dados do cliente a partir do rastreamento governamental](https://blogs.microsoft.com/blog/2013/12/04/protecting-customer-data-from-government-snooping/)). Publicamos periodicamente [informações detalhadas](https://www.microsoft.com/en-us/corporate-responsibility/lerr) sobre as solicitações de cumprimento de leis que a Microsoft recebe.

Consulte a [central de confiabilidade da Microsoft](https://www.microsoft.com/en-us/trustcenter/default.aspx) sobre solicitações de dados de terceiros e a seção "divulgação de dados do cliente" nos [termos dos serviços online](https://www.microsoft.com/Licensing/product-licensing/products.aspx) para obter mais informações.

#### <a name="how-does-microsoft-ensure-that-a-member-of-its-staff-doesnt-have-standing-access-to-customer-content-in-office-365-applications"></a>Como a Microsoft garante que um membro de sua equipe não tenha acesso ao conteúdo do cliente em aplicativos do Office 365?

A Microsoft implementa medidas preventivas extensivas por meio de sistemas de controle de acesso e medidas de detecção para identificar e tratar de tentativas de burlar esses sistemas de controle de acesso. O Office 365 funciona com os princípios de privilégios mínimos e acesso just-in-time. Portanto, nenhum pessoal da Microsoft tem permissão para acessar o conteúdo do cliente de forma contínua. Se a permissão for concedida, ela será para uma duração limitada. 

O Office 365 usa um sistema de controle de acesso chamado *Lockbox* para processar as solicitações de permissões que concedem a capacidade de executar funções operacionais e administrativas dentro do serviço. Um operador deve solicitar acesso ao conteúdo do cliente usando o Lockbox, que requer uma segunda pessoa para executar a ação na solicitação (por exemplo, aprová-la) antes que o acesso seja concedido. Essa segunda pessoa não pode ser o solicitante e deve ser designada para aprovar o acesso ao conteúdo do cliente. Somente se a solicitação for aprovada, o operador adquirirá acesso temporário ao conteúdo do cliente. Depois que o período de elevação expira, o Lockbox revoga o acesso.

Consulte os [termos dos serviços online](https://www.microsoft.com/licensing/product-licensing/products) para obter mais detalhes sobre as práticas de segurança geral da Microsoft.

#### <a name="under-what-circumstances-do-microsoft-engineers-need-access-to-my-content"></a>Em que circunstâncias os engenheiros da Microsoft precisam acessar o meu conteúdo?

O cenário mais comum em que os engenheiros da Microsoft precisam acessar o conteúdo do cliente é quando o cliente faz uma solicitação de suporte que requer acesso à solução de problemas. Um princípio básico do Office 365 é que o serviço opera sem o Microsoft Access para o conteúdo do cliente. Quase todas as operações de serviço realizadas pela Microsoft são totalmente automatizadas e o envolvimento humano é altamente controlado e resumido fora do conteúdo do cliente. O objetivo do Office 365 é o acesso ao conteúdo do cliente para dar suporte ao serviço não é necessário até que o cliente aprove uma solicitação específica para o Microsoft Access.

#### <a name="i-already-thought-my-data-was-secure-with-the-microsoft-cloud-so-why-do-i-need-customer-lockbox"></a>Já pensei que meus dados estavam seguros com a nuvem da Microsoft, portanto, por que eu preciso de lockbox de cliente?

O Lockbox do cliente fornece uma camada extra de controle, oferecendo aos clientes a capacidade de fornecer autorização de acesso explícito para operações de serviço. Ao demonstrar que os procedimentos estão disponíveis para autorização explícita de acesso a dados, a Lockbox de clientes também ajuda os clientes a atender a certas obrigações de conformidade, como HIPAA e FEDRAMP.

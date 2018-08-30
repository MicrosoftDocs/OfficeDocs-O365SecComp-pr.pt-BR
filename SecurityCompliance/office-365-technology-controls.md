---
title: Controles de tecnologia do Office 365
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
description: 'Resumo: Uma visão geral das práticas de controle de tecnologia da Microsoft para o Office 365.'
ms.openlocfilehash: 2ef04b558f5fa82075d9aa602b83d437aa4b2ee6
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523944"
---
# <a name="office-365-technology-controls"></a>Controles de tecnologia do Office 365 

A Microsoft usa várias ferramentas para controlar, gerenciar e auditar o acesso a dados do cliente no Exchange Online e tecnologias do SharePoint Online, incluindo Lockbox e Lockbox do cliente, a autenticação multifator e mais. Yammer que Enterprise usa controles semelhantes, conforme descrito em [Controles de acesso do Yammer Enterprise](office-365-yammer-enterprise-access-controls.md).

Engenheiros do Office 365 tem zero acesso de uma posição para dados do cliente do Office 365 e eles devem passar um processo de aprovação que inclui Microsoft e – se o cliente licencia o recurso de Lockbox de cliente do Exchange Online e SharePoint Online – cliente aprovação, antes que o acesso aos dados do cliente para operações de serviço pode ocorrer. Quando é concedida a aprovação, específico do serviço de contas administrativas são provisionado just-in-time com acesso apenas o suficiente para executar as tarefas necessárias para a solicitação de serviço.

## <a name="lockbox-and-customer-lockbox"></a>Lockbox e Lockbox do cliente
Embora seja extremamente raro, um cliente pode solicitar assistência da Microsoft que pode expor um engenheiro da Microsoft para o conteúdo do cliente para ajudá-lo com um problema. Para controlar o acesso ao Exchange Online (que inclui qualquer Skype para dados corporativos armazenados em caixas de correio dos usuários (Skype para cobertura de negócios não incluir transmissão do Skype reunião gravações ou conteúdo carregado para reuniões pelos usuários)) e o SharePoint Online (que inclui OneDrive for Business), a Microsoft usa um sistema de controle de acesso chamado Lockbox. Para que qualquer engenheiro de Microsoft possa acessar todos os sistemas Exchange Online ou SharePoint Online ou dados, eles devem enviar uma solicitação de acesso usando Lockbox. Usar Lockbox é necessária para todo o acesso elevado ao Exchange Online ou SharePoint Online.

Lockbox processa solicitações de permissões que concedem engenheiros a capacidade de executar funções administrativas e operacionais dentro do serviço. Engenheiros enviam solicitações por meio do Lockbox, que devem ser aprovados por um gerente antes do engenheiro ganhando a capacidade de acessar dados do cliente. Após a aprovação do gerente, o engenheiro tem tempo limitado e escopo-limited acesso aos dados de cliente para trabalhar em que o problema do cliente.

Lockbox do cliente para o Office 365 pode ajudá-lo a cumprir as obrigações de conformidade, como os encontrados em FedRAMP e HIPAA, se você precisar procedimentos no local para autorização de acesso de dados explícita. Na instância rara ao engenheiro de serviço do Microsoft precisa ter acesso aos seus dados, você concede que o acesso somente aos dados necessários para resolver o problema e por um tempo limitado. Ações tomadas pelo engenheiro de suporte são registradas para fins de auditoria e podem ser acessadas por meio da [API de atividade de gerenciamento do Office 365](https://msdn.microsoft.com/library/office/dn707383.aspx) e o [Centro de conformidade e segurança](http://protection.office.com/). Cliente Lockbox insere o cliente do processo de aprovação de Lockbox e fornece a eles a capacidade de controlar a autorização do Microsoft access para seu Exchange Online ou o conteúdo do SharePoint Online para operações de serviço.

>**Observação**: Lockbox do cliente está disponível no [Office 365 Enterprise E5](https://products.office.com/business/office-365-enterprise-e5-business-software) e como compra um complemento, mas manual ação deve ser realizada no Centro de administração do Office 365 (em configurações do serviço | Cliente Lockbox) para habilitá-lo. Para obter mais informações, consulte [Solicitações de Lockbox do cliente do Office 365](https://support.office.com/article/Office-365-Customer-Lockbox-Requests-36f9cdd1-e64c-421b-a7e4-4a54d16440a2).

Todas as solicitações de serviço do Exchange Online e SharePoint Online são tratadas pelo sistema Lockbox. E com Lockbox do cliente, qualquer operação de serviço a necessidade de acesso a esses serviços com a exposição em dados do cliente passa o processo de aprovação de Lockbox e, em seguida, permite que o cliente aprovar ou rejeitar a solicitação depois disso.
 
*Figura 1: fluxo de trabalho do cliente Lockbox*

Se a solicitação será rejeitada pelo cliente, o engenheiro de Microsoft não terão acesso ao conteúdo do cliente e não será possível concluir a operação de serviço. Se a solicitação for aprovada pelo cliente, o engenheiro de Microsoft terá limitados just-in-time acesso ao conteúdo do cliente por meio de interfaces de gerenciamento monitorados e restrita. Com Lockbox e Lockbox do cliente, todo o acesso aprovado é atribuído a um usuário exclusivo, tornando os engenheiros responsável tratamento de dados do cliente.

## <a name="just-in-time-access"></a>Acesso just-in-Time
A Microsoft usa o princípio de acesso just-in-time (JIT) para o Office 365 para atenuar ainda mais o risco de violação de credencial e ataques laterais. JIT remove persistente acesso administrativo aos serviços e substitui esses direitos a capacidade de elevar para essas funções sob demanda. Removendo direitos persistentes de administradores garante que as credenciais estão disponíveis apenas quando eles são necessários e remove o risco apresentado à empresa em casos de roubo de credenciais.

O modelo de acesso JIT requer os engenheiros solicitar privilégios elevados por um período limitado executar tarefas administrativas. Além disso, o OCEs use contas temporárias que são criadas com senhas complexas geradas e concedido apenas as funções que permitem a eles executar as tarefas necessárias. Por exemplo, acesso administrativo concedido pelo Lockbox está vinculado à hora e a quantidade de tempo de acesso seja concedido depende da função que está sendo solicitada. Um engenheiro Especifica a duração do access tempo necessário durante a solicitação para o sistema de Lockbox. O sistema de Lockbox rejeitará solicitações onde o tempo solicitado excede o máximo permitido de tempo para a elevação. Após a expiração da solicitação de elevação, acesso administrativo é removido e a conta temporária expira.

Quando autorizados e aprovados para o access (por exemplo, para um sistema de depuração), os engenheiros recebem uma senha de uso de uma única vez administrativos que seja gerada pelo sistema de autorização de cada vez que uma solicitação de acesso elevado em particular for aprovada. Essa senha é copiada com o engenheiro em uma senha segura, é separada da credenciais do engenheiro para o ambiente corporativo da Microsoft e é válida somente para a sessão para o qual o acesso elevado foi aprovado.

## <a name="constrained-management-interfaces"></a>Interfaces de gerenciamento restrita
OCEs use duas interfaces de gerenciamento para executar tarefas administrativas: a área de trabalho remota por meio de Gateways de serviços de Terminal protegido (os guias de solução) e o PowerShell remoto. Dentro desses management interfaces existem diretivas de software e acessar os controles que colocar restrições significativas sobre quais aplicativos podem ser executados e quais comandos e cmdlets estão disponíveis. 

Servidores do Office 365 restringem sessões simultâneas para um administrador de equipe por serviço de sessão, por servidor. Os guias de solução são configurados para permitir que somente uma única sessão simultânea para usuários, e não permitir que várias sessões. Os guias de solução permitem que os administradores de equipe de serviços do Office 365 para se conectar a vários servidores simultaneamente, usando uma única sessão por servidor, de modo que os administradores podem realizar com eficiência suas obrigações. Administradores de serviço de equipe não têm nenhuma permissão no guias de solução sozinhos. O TSG é usado somente para impor a autenticação multifator (MFA) e requisitos de criptografia. Depois que o administrador da equipe de serviço se conecta a um servidor específico por meio de um TSG, o servidor específico imporá um limite de sessão de um por um administrador.

Restrições de uso e os requisitos de configuração e de conexão para o Office 365 pessoal são estabelecidos pelas diretivas de grupo do Active Directory. Essas políticas incluem as seguintes características:
- Os guias de solução são configurados para usar apenas [FIPS](https://www.microsoft.com/en-us/TrustCenter/Compliance/FIPS) de criptografia FIPS 140-2
- Sessões TSG são configuradas para se desconectar após 30 minutos de inatividade
- Sessões TSG são configuradas automaticamente log desativado após 24 horas

Conexões com os guias de solução também requerem MFA usando um cartão de inteligente físico separado e uma conta que seja separada do credenciais corporativas do engenheiro Microsoft. Engenheiros são emitidos diferentes cartões inteligentes para várias plataformas e plataformas de gerenciamento de segredos são usadas para garantir o armazenamento seguro de credenciais. Os guias de solução usam diretivas de grupo do Active Directory para controlar quem pode fazer logon servidores remotos, o número de sessões permitidas e configurações de tempo limite de ociosidade. Políticas adicionais são usadas para limitar o acesso a aplicativos permitidos e para restringir o acesso à Internet.

Além de acesso remoto usando os guias de solução especialmente configurados, o Exchange Online permite aos usuários com a função de operações de engenheiro de serviço acessar algumas funcionalidades administrativas nos servidores de produção usando o PowerShell remoto. Para fazer isso, o usuário deve ser autorizado para acesso somente leitura (depuração) para o ambiente de produção do Office 365. Escalonamento de privilégio está habilitado da mesma maneira que ele está habilitado para os guias de solução usando o processo de Lockbox.

Para acesso remoto, há um IP virtual com balanceamento de carga em cada data center que serve como um único ponto de acesso. Os cmdlets do PowerShell remoto que podem ser executados se baseiam em nível de privilégio identificado nessa declaração acesso obtida durante a autenticação. Esses cmdlets são a funcionalidade administrativa apenas que pode ser acessada e executada por usuários conectando-se de usar esse método. PowerShell remoto é usado para limitar o escopo dos comandos disponíveis para o engenheiro, que baseia-se o nível de acesso concedido através do processo de Lockbox. Por exemplo, no Exchange Online, o Get-Mailbox pode estar disponível, mas não seria Set-Mailbox.

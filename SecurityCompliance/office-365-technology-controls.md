---
title: Controles de tecnologia do Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: 'Resumo: uma visão geral das práticas de controle de tecnologia da Microsoft para o Office 365.'
ms.openlocfilehash: a8dcb65880fc729fc067b2f2bcf25c7db76dbca9
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262333"
---
# <a name="office-365-technology-controls"></a>Controles de tecnologia do Office 365 

A Microsoft usa várias ferramentas e tecnologias para controlar, gerenciar e auditar o acesso aos dados do cliente no Exchange Online e no SharePoint Online, incluindo Lockbox e Lockbox de cliente, autenticação multifator e muito mais. O Yammer Enterprise usa controles similares, conforme descrito nos [controles de acesso corporativo do Yammer](office-365-yammer-enterprise-access-controls.md).

Os engenheiros do Office 365 têm zero acesso de pé aos dados do cliente do Office 365 e precisam passar por um processo de aprovação que inclui tanto a Microsoft quanto o cliente licenciar o recurso de lockbox do cliente para o Exchange Online e o SharePoint Online – cliente a aprovação, antes que o acesso aos dados do cliente para as operações de serviço possa ocorrer. Quando a aprovação é concedida, as contas administrativas específicas de serviço são provisionadas no momento certo com acesso apenas o suficiente para executar as tarefas exigidas pela solicitação de serviço.

## <a name="lockbox-and-customer-lockbox"></a>Lockbox e Lockbox de cliente
Embora seja extremamente raro, um cliente pode solicitar assistência da Microsoft que possa expor um engenheiro da Microsoft ao conteúdo do cliente para ajudá-lo com um problema. Para controlar o acesso ao Exchange Online (que inclui quaisquer dados do Skype for Business armazenados nas caixas de correio dos usuários (a cobertura do Skype for Business não inclui gravações de transmissão de reunião do Skype ou conteúdo carregado em reuniões por usuários)) e o SharePoint Online (que inclui o OneDrive for Business), a Microsoft usa um sistema de controle de acesso chamado lockbox. Antes que qualquer engenheiro da Microsoft possa acessar qualquer sistema ou dados do Exchange Online ou do SharePoint Online, eles devem enviar uma solicitação de acesso usando o Lockbox. O uso de lockbox é necessário para todo o acesso elevado ao Exchange Online ou ao SharePoint Online.

O Lockbox processa as solicitações que concedem aos engenheiros a capacidade de executar funções operacionais e administrativas dentro do serviço. Os engenheiros enviam solicitações por meio de Lockbox, que devem ser aprovadas por um gerente antes que o engenheiro obtenha a capacidade de acessar os dados do cliente. Após a aprovação do gerente, o engenheiro tem acesso limitado por tempo e com escopo limitado aos dados do cliente para trabalhar no problema do cliente.

O Lockbox do cliente para o Office 365 pode ajudá-lo a cumprir as obrigações de conformidade, como as encontradas no FedRAMP e HIPAA, se você precisar de procedimentos para autorização explícita de acesso a dados. Na rara instância, quando um engenheiro de serviços da Microsoft precisa acessar seus dados, você concede a eles acesso apenas aos dados necessários para resolver o problema e por um tempo limitado. As ações realizadas pelo engenheiro de suporte são registradas para fins de auditoria e podem ser acessadas por meio da [API de atividade de gerenciamento do Office 365](https://msdn.microsoft.com/library/office/dn707383.aspx) e do [centro de segurança e conformidade](http://protection.office.com/). O Lockbox do cliente insere o cliente no processo de aprovação de Lockbox e fornece a capacidade de controlar a autorização do Microsoft Access para o conteúdo do Exchange Online ou do SharePoint Online para operações de serviço.

>**Observação**: a Lockbox de clientes está disponível no [Office 365 Enterprise E5](https://products.office.com/business/office-365-enterprise-e5-business-software) e como uma compra de complemento, mas a ação manual deve ser realizada no centro de administração do Microsoft 365 (em configurações de serviço | Lockbox de cliente) para habilitá-lo. Para saber mais, consulte [Solicitações do Sistema de Proteção de Dados do Cliente do Office 365](https://support.office.com/article/Office-365-Customer-Lockbox-Requests-36f9cdd1-e64c-421b-a7e4-4a54d16440a2).

Todas as solicitações de serviço do Exchange Online e do SharePoint Online são tratadas pelo sistema de lockbox. E com o Lockbox do cliente, qualquer operação de serviço que precisa de acesso a esses serviços com a exposição aos dados do cliente passa pelo processo de aprovação de Lockbox e permite que o cliente aprove ou rejeite a solicitação posteriormente.
 
*Figura 1: fluxo de trabalho de lockbox do cliente*

Se a solicitação for rejeitada pelo cliente, o engenheiro da Microsoft não terá acesso ao conteúdo do cliente e não poderá concluir a operação do serviço. Se a solicitação for aprovada pelo cliente, o engenheiro da Microsoft terá acesso limitado ao conteúdo do cliente por meio de interfaces de gerenciamento restritas e restringidas. Com o Lockbox e o Lockbox do cliente, todos os acessos aprovados são rastreáveis para um usuário exclusivo, tornando os engenheiros informativos sobre a manipulação dos dados dos clientes.

## <a name="just-in-time-access"></a>Acesso just-in-time
A Microsoft usa o princípio de acesso just-in-time (JIT) para o Office 365 para reduzir ainda mais o risco de violação de credenciais e ataques de lateral. O JIT remove o acesso administrativo persistente aos serviços e substitui esses direitos com a capacidade de elevar essas funções sob demanda. A remoção de direitos persistentes de administradores garante que as credenciais estarão disponíveis somente quando forem necessárias e removerá o risco apresentado à empresa em casos de roubo de credenciais.

O modelo de acesso JIT exige que os engenheiros solicitem privilégios elevados por um período limitado para realizar tarefas administrativas. Além disso, o OCEs usa contas temporárias que são criadas com senhas complexas geradas por máquina e concedidas apenas às funções que permitem executar as tarefas necessárias. Por exemplo, o acesso administrativo concedido pelo lockbox é limitado por tempo, e a quantidade de tempo que o acesso é concedido depende da função que está sendo solicitada. Um engenheiro especifica a duração do tempo de acesso necessário durante a solicitação para o sistema de lockbox. O sistema de lockbox rejeitará solicitações em que o tempo solicitado excede o tempo máximo permitido para a elevação. Após a expiração da solicitação de elevação, o acesso administrativo será removido e a conta temporária expirará.

Quando autorizado e aprovado para acesso (por exemplo, para depurar um sistema), os engenheiros recebem uma senha administrativa de uso único gerada pelo sistema de autorização cada vez que uma solicitação de acesso elevado é aprovada. Essa senha é copiada pelo engenheiro em uma senha segura, é separada das credenciais do engenheiro para o ambiente corporativo da Microsoft e só é válida para a sessão para a qual o acesso elevado foi aprovado.

## <a name="constrained-management-interfaces"></a>Interfaces de gerenciamento restritas
OCEs Use duas interfaces de gerenciamento para executar tarefas administrativas: área de trabalho remota através de gateways de serviço de terminal protegido (TSGs) e PowerShell remoto. Dentro dessas interfaces de gerenciamento, há diretivas de software e controles de acesso que colocam restrições significativas em quais aplicativos podem ser executados e quais comandos e cmdlets estão disponíveis. 

Os servidores do Office 365 restringem sessões simultâneas a uma sessão por administrador de equipe por serviço, por servidor. TSGs são configurados para permitir apenas uma única sessão simultânea para os usuários e não permitem várias sessões. TSGs permitir que os administradores do Office 365 Service Team se conectem a vários servidores simultaneamente, usando uma única sessão por servidor, para que os administradores possam efetivamente realizar suas tarefas. Os administradores da equipe de serviço não têm nenhuma permissão no TSGs. O TSG é usado apenas para impor os requisitos de criptografia e autenticação multifator (MFA). Depois que o administrador da equipe de serviço se conectar a um servidor específico por meio de um TSG, o servidor específico aplicará um limite de sessão de um por administrador.

As restrições de uso e os requisitos de conexão e configuração do pessoal do Office 365 são estabelecidos pelas políticas de grupo do Active Directory. Essas políticas incluem as seguintes características:
- TSGs estão configurados para usar apenas a criptografia validada pelo [FIPS](https://www.microsoft.com/en-us/TrustCenter/Compliance/FIPS) 140-2
- As sessões do TSG são configuradas para serem desconectadas após 30 minutos de inatividade
- As sessões do TSG estão configuradas para fazer logoff automaticamente após 24 horas

As conexões com o TSGs também exigem o MFA usando um cartão inteligente físico separado e uma conta separada das credenciais corporativas da Microsoft do engenheiro. Os engenheiros são emitidos diferentes cartões inteligentes para várias plataformas e as plataformas de gerenciamento de segredos são usadas para garantir o armazenamento seguro de credenciais. TSGs use as políticas de grupo do Active Directory para controlar quem pode fazer logon em servidores remotos, o número de sessões permitidas e as configurações de tempo limite de ociosidade. Políticas adicionais estão disponíveis para limitar o acesso a aplicativos permitidos e para restringir o acesso à Internet.

Além do acesso remoto usando o TSGs especialmente configurado, o Exchange Online permite que os usuários com a função de operações do engenheiro de serviço acessem determinada funcionalidade administrativa em servidores de produção usando o PowerShell remoto. Para fazer isso, o usuário deve estar autorizado para acesso somente leitura (depuração) ao ambiente de produção do Office 365. O escalonamento de privilégio é habilitado da mesma forma que está habilitado para o TSGs usando o processo de lockbox.

Para o acesso remoto, há um IP virtual com balanceamento de carga em cada datacenter que serve como um único ponto de acesso. Os cmdlets do PowerShell remoto que podem ser executados são baseados no nível de privilégio identificado na declaração de acesso obtida durante a autenticação. Estes cmdlets são a única funcionalidade administrativa que pode ser acessada e executada pelos usuários que se conectam usando este método. O PowerShell remoto é usado para limitar o escopo de comandos disponíveis para o engenheiro, que baseia-se no nível de acesso concedido por meio do processo de lockbox. Por exemplo, no Exchange Online, o Get-Mailbox pode estar disponível, mas Set-Mailbox não seria.

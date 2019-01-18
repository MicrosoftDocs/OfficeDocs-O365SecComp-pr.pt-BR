---
title: Privilégios acessar management no Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.service: o365-solutions
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Strat_O365_IP
ms.custom: Ent_Solutions
ms.assetid: ''
description: Use este tópico para saber mais sobre privilegiada acessar management no Office 365
ms.openlocfilehash: f3cd5fb263fe3bb83d60a7938f0e22dc38f199e3
ms.sourcegitcommit: b0b0b716718c22779c7c04775b8010d65cd6656b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28723228"
---
# <a name="privileged-access-management-in-office-365"></a>Privilégios acessar management no Office 365

> [!IMPORTANT]
> Este tópico aborda as diretrizes de implantação e configuração para recursos somente está disponíveis no Office 365 E5 e avançadas SKUs de conformidade.

Privilegiado acesso gerenciamento permite que o controle de acesso granular sobre tarefas de administração com privilégios no Office 365. Ele pode ajudar a proteger sua organização contra violações que possam usar contas de administração com privilégios existentes com acesso a posição a dados confidenciais ou acesso às definições de configuração crítico. Após habilitar o gerenciamento de acesso privilegiado, serão necessário solicitar acesso just-in-time para executar tarefas com privilégios elevados e privilegiadas por meio de um fluxo de trabalho de aprovação que é altamente no escopo do tempo-limite e usuários. Isso dá usuários just-o suficiente-acesso para realizar a tarefa em questão, sem o risco de exposição dos dados confidenciais ou definições de configuração crítico. Habilitando o gerenciamento de acesso privilegiado no Office 365 permitirá a sua organização para operar com zero privilégios a posição e fornecem uma camada de defesa contra vulnerabilidades resultantes por causa de tal acesso administrativo de posição. 

## <a name="layers-of-protection"></a>Camadas de proteção

Privilegiado acesso gerenciamento complementa outras proteções de recurso de dados e o acesso dentro da arquitetura de segurança do Office 365. Habilitando o gerenciamento de acesso privilegiado como parte de uma abordagem integrada à segurança e proteção de sua organização, um modelo de segurança em camadas pode ser usado para aumentar a proteção de informações confidenciais e definições de configuração do Office 365. Conforme mostrado no diagrama a seguir, habilitando privilegiado ajuda de gerenciamento de acesso amplia a proteção fornecida com criptografia nativa de dados do Office 365 e o modelo de segurança do controle de acesso baseado na função dos serviços do Office 365. Quando usado em conjunto com o [Windows Azure AD privilegiado gerenciamento de identidade](https://docs.microsoft.com/azure/active-directory/active-directory-privileged-identity-management-configure), esses dois recursos fornecem controle de acesso com acesso just-in-time em escopos diferentes.

![Proteção em camadas no Office 365](media/pam-layered-protection.png)

Privilegiado access pode ser definido e com escopo no nível da **tarefa** , enquanto o Azure AD privilegiado Identity Management se aplica a proteção no nível de **função** com a capacidade de executar várias tarefas de gerenciamento no Office 365.  Gerenciamento de identidade do Azure AD privilegiada principalmente permite Gerenciando acessos para grupos de função e funções do AD, enquanto com privilégios de acesso gerenciamento no Office 365 é aplicado apenas no nível da tarefa.

- **Privilegiada habilitando acessar management no Office 365 durante o uso do Windows Azure AD privilegiado gerenciamento de identidade já:** A adição de gerenciamento de acesso privilegiado no Office 365 fornece outra camada granular dos recursos de proteção e a auditoria para acesso privilegiado aos dados do Office 365.

- **Habilitando o Azure AD privilegiado gerenciamento de identidade durante a utilização do já privilegiado gerenciamento de acesso no Office 365:**  Adicionando o Azure AD privilegiado gerenciamento de identidade a privilegiada gerenciamento de acesso no Office 365 pode estender privilegiado acesso aos dados fora do Office 365 definida principalmente por função ou a identidade de um usuário.  

## <a name="privileged-access-management-architecture-and-process-flow"></a>Fluxo de processo e a arquitetura de gerenciamento de acesso privilegiado

Cada um dos fluxos de processo a seguir destacam a arquitetura do acesso privilegiado e como ele interage com substrate o Office 365, auditoria do Office 365 e o runspace de gerenciamento do Exchange.

### <a name="step-1-configuring-a-privileged-access-policy"></a>Etapa 1: Configurar uma política de acesso privilegiado

Ao configurar uma política de acesso privilegiado usando o Centro de administração do Office 365 ou PowerShell de gerenciamento do Exchange, você cria e define a política e o recurso de acesso privilegiado processa os atributos de política no Office 365 substrate e logs a no Centro de conformidade de segurança do Office 365 e a atividade. A política agora está habilitada e pronto para lidar com as solicitações de entrada para aprovações.

![Etapa 1: criação de políticas](media/pam-step1-policy-creation.jpg)

### <a name="step-2-access-request"></a>Etapa 2: Solicitação de acesso

Usando o Centro de administração do Office 365 ou PowerShell de gerenciamento do Exchange, os usuários podem solicitar acesso às tarefas com privilégios elevados ou privilegiados. O recurso de acesso privilegiado envia a solicitação para o Office 365 substrate para processamento em relação à política de acesso de privilégio configurado e registra o sctivity de segurança do Office 365 e os logs de centro de conformidade.

![Etapa 2: a solicitação de acesso](media/pam-step2-access-request.jpg)

### <a name="step-3-access-approval"></a>Etapa 3: Aprovação de acesso

Uma solicitação de aprovação é criada e o grupo de aprovação seja notificado por email da solicitação pendente. Se for concedida a aprovação, a solicitação de acesso privilegiado é processada como uma aprovação e a tarefa está pronta para ser concluída. Se a solicitação for negada, tarefa está bloqueada e não tem acesso para o reqeustor. O solicitante será notificado da aprovação de solicitação ou negação via mensagem de email.

![Etapa 3 - aprovação de acesso](media/pam-step3-access-approval.jpg)

### <a name="step-4-access-processing"></a>Etapa 4: Processamento de acesso

Para solicitações de aprovadas, a tarefa é processada pelo runspace gerenciamento do Exchange. A aprovação é verificada em relação à política de acesso privilegiado e processada pelo substrate Office 365. Todas as atividades da tarefa é registrada no Centro de conformidade de segurança do Office 365 e.

![Etapa 4 - processamento de acesso](media/pam-step4-access-processing.jpg)

## <a name="frequently-asked-questions"></a>Perguntas frequentes

### <a name="what-skus-do-i-need-to-use-privileged-access-in-office-365"></a>Quais SKUs precisa usar acesso privilegiado no Office 365?
Privilegiado acesso gerenciamento atualmente só está disponível para clientes com o Office 365 E5 e avançadas SKUs de conformidade.

### <a name="when-will-privileged-access-be-available-for-office-365-workloads-beyond-exchange"></a>Quando o acesso privilegiado estará disponível para cargas de trabalho do Office 365 além do Exchange?
Pretendemos oferecer esse recurso em outras cargas de trabalho do Office 365 em breve. Quando estamos prontos para compartilhar um cronograma, ele estará disponível por meio do [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap).

### <a name="my-organization-needs-more-than-30-privileged-access-polices-will-this-limit-be-increased"></a>Minhas necessidades da organização com mais de 30 acesso privilegiado diretivas, esse limite ser aumentado?

Estamos planejando aumentar o limite atual de 30 políticas de acesso privilegiado por organização do Office 365 em breve.

### <a name="do-i-need-to-be-a-global-admin-to-manage-privileged-access-in-office-365"></a>É necessário ser um Administrador Global para gerenciar o acesso privilegiado no Office 365?
Não, você precisa ter a função de gerenciamento de função do Exchange atribuída às contas que gerenciará o acesso privilegiado no Office 365. No entanto, a função de Administrador Global inclui essa função por padrão e pode ser usada para gerenciar o acesso privilegiado se não desejar configurar a função de gerenciamento de função como uma permissão de conta autônomo. Os usuários que estão incluídos no grupo dos aprovadores um não precisam ser um Administrador Global ou ter a função de gerenciamento de função atribuída a revisar e aprovar solicitações. 

### <a name="how-is-privileged-access-management-in-office-365-related-to-customer-lockbox"></a>Como é o gerenciamento de acesso privilegiado no Office 365 relacionadas ao cliente Lockbox?
[Lockbox do cliente](https://docs.microsoft.com/office365/admin/manage/customer-lockbox-requests) permite que um nível de controle de acesso para as organizações para acesso a dados pelo seu provedor de serviço, ou seja, a Microsoft. Privilegiado acesso management no Office 365 permite que o controle de acesso granular dentro de uma organização para todas as tarefas do Office 365 privilegiado.

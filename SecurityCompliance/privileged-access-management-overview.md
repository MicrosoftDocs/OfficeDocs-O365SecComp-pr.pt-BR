---
title: Gerenciamento de acesso privilegiado no Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
ms.custom: Ent_Solutions
ms.assetid: ''
description: Use este tópico para saber mais sobre o gerenciamento de acesso privilegiado no Office 365
ms.openlocfilehash: 2a464bacaa568515e470e29a0c9c45a91a79cf8e
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/29/2019
ms.locfileid: "31001244"
---
# <a name="privileged-access-management-in-office-365"></a>Gerenciamento de acesso privilegiado no Office 365

> [!IMPORTANT]
> Este tópico aborda as diretrizes de implantação e configuração dos recursos disponíveis atualmente no Office 365 E5 e nas SKUs de conformidade avançada.

O gerenciamento de acesso privilegiado permite o controle de acesso granular sobre tarefas administrativas privilegiadas no Office 365. Ele pode ajudar a proteger sua organização contra violações que podem usar contas de administrador privilegiadas existentes com acesso à dados confidenciais ou acesso a definições de configuração crítica. Depois de habilitar o gerenciamento de acesso privilegiado, os usuários precisarão solicitar acesso just-in-time para concluir tarefas elevadas e privilegiadas por meio de um fluxo de trabalho de aprovação com alta abrangência e limite de tempo. Isso permite que os usuários tenham acesso apenas o suficiente para executar a tarefa em mãos, sem risco de exposição de dados confidenciais ou definições de configuração crítica. Habilitar o gerenciamento de acesso privilegiado no Office 365 permitirá que sua organização opere com zero privilégios de duração e forneça uma camada de defesa contra vulnerabilidades decorrentes por esse acesso administrativo mais duradouro.

Para obter uma visão geral rápida da Lockbox de cliente integrada e do gerenciamento de acesso privilegiado de ponta a ponta, consulte este [cofre de clientes e gerenciamento de acesso privilegiado no Office 365 Video](https://go.microsoft.com/fwlink/?linkid=2066800).

## <a name="layers-of-protection"></a>Camadas de proteção

O gerenciamento de acesso privilegiado complementa outras proteções de recursos de dados e acesso dentro da arquitetura de segurança do Office 365. Ao habilitar o gerenciamento de acesso privilegiado como parte de uma abordagem integrada à segurança e à proteção da sua organização, um modelo de segurança em camadas pode ser usado para maximizar a proteção de informações confidenciais e definições de configuração do Office 365. Conforme mostrado no diagrama abaixo, habilitar o gerenciamento de acesso privilegiado ajuda a criar a proteção fornecida com a criptografia nativa dos dados do Office 365 e o modelo de segurança de controle de acesso baseado em função dos serviços do Office 365. Quando usado em conjunto com o [Azure ad Privileged Identity Management](https://docs.microsoft.com/azure/active-directory/active-directory-privileged-identity-management-configure), esses dois recursos fornecem controle de acesso com acesso just-in-time em escopos diferentes.

![Proteção em camadas no Office 365](media/pam-layered-protection.png)

O gerenciamento de acesso privilegiado no Office 365 pode ser definido e escopos no nível da **tarefa** , enquanto o gerenciamento de identidade privilegiada do Azure ad aplica proteção no nível da **função** com a capacidade de executar várias tarefas.  O gerenciamento de identidade privilegiada do Azure AD permite principalmente o gerenciamento de acessos para funções do AD e grupos de função, enquanto o gerenciamento de acesso privilegiado no Office 365 é aplicado apenas no nível da tarefa.

- **Habilitando o gerenciamento de acesso privilegiado no Office 365 enquanto já estava usando o gerenciamento de identidade privilegiaDa do Azure AD:** A adição de gerenciamento de acesso privilegiado no Office 365 fornece outra camada granular de recursos de proteção e auditoria para acesso privilegiado aos dados do Office 365.

- **Habilitar o Azure ad Privileged Identity Management enquanto já usa o gerenciamento de acesso privilegiado no Office 365:**  Adicionar o Azure AD Privileged Identity Management ao gerenciamento de acesso privilegiado no Office 365 pode estender o acesso privilegiado aos dados fora do Office 365, que é definido principalmente pela função ou identidade de um usuário.  

## <a name="privileged-access-management-architecture-and-process-flow"></a>Arquitetura de gerenciamento de acesso privilegiado e fluxo de processo

Cada um dos fluxos de processo a seguir descreve a arquitetura de acesso privilegiado e como ele interage com o substrato do Office 365, a auditoria do Office 365 e o espaço de gerenciamento do Exchange.

### <a name="step-1-configuring-a-privileged-access-policy"></a>Etapa 1: conFigurando uma política de acesso privilegiado

Ao configurar uma política de acesso privilegiado usando o [centro de administração do Microsoft 365](https://admin.microsoft.com) ou o PowerShell de gerenciamento do Exchange, você cria e define a política e o recurso de acesso privilegiado processa os atributos de política no substrato do Office 365 e registra a atividade no centro de segurança e conformidade do Office 365. A política agora está habilitada e pronta para lidar com solicitações de entrada para aprovações.

![Etapa 1-criação de política](media/pam-step1-policy-creation.jpg)

### <a name="step-2-access-request"></a>Etapa 2: solicitação de acesso

Usando o [centro de administração do Microsoft 365](https://admin.microsoft.com) ou o PowerShell de gerenciamento do Exchange, os usuários podem solicitar acesso a tarefas elevadas ou privilegiadas. O recurso de acesso privilegiado envia a solicitação para o substrato do Office 365 para processamento com a política de acesso de privilégio configurada e registra a atividade nos logs do centro de conformidade e segurança do Office 365.

![Etapa 2-solicitação de acesso](media/pam-step2-access-request.jpg)

### <a name="step-3-access-approval"></a>Etapa 3: aprovação do acesso

Uma solicitação de aprovação é gerada e o grupo de aprovação é notificado por email da solicitação pendente. Se a aprovação for concedida, a solicitação de acesso privilegiado será processada como uma aprovação e a tarefa estará pronta para ser concluída. Se a solicitação for negada, a tarefa será bloqueada e nenhum acesso será concedido ao solicitante. O solicitante será notificado sobre a aprovação da solicitação ou a negação via mensagem de email.

![Etapa 3: aprovação do acesso](media/pam-step3-access-approval.jpg)

### <a name="step-4-access-processing"></a>Etapa 4: processamento de acesso

Para solicitações aprovadas, a tarefa é processada pelo runspace de gerenciamento do Exchange. A aprovação é verificada em relação à política de acesso privilegiado e processada pelo substrato do Office 365. Todas as atividades da tarefa são registradas no centro de segurança e conformidade do Office 365.

![Etapa 4-processamento de acesso](media/pam-step4-access-processing.jpg)

## <a name="frequently-asked-questions"></a>Perguntas frequentes

### <a name="what-skus-do-i-need-to-use-privileged-access-in-office-365"></a>Quais SKUs eu preciso usar o acesso privilegiado no Office 365?
O gerenciamento de acesso privilegiado atualmente só está disponível para clientes com SKUs de conformidade avançada e do Office 365 e5.

### <a name="when-will-privileged-access-be-available-for-office-365-workloads-beyond-exchange"></a>Quando o acesso privilegiado estará disponível para cargas de trabalho do Office 365 além do Exchange?
Planejamos oferecer esse recurso em outras cargas de trabalho do Office 365 em breve. Quando estiver pronto para compartilhar uma linha do tempo, ela estará disponível por meio do [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap).

### <a name="my-organization-needs-more-than-30-privileged-access-polices-will-this-limit-be-increased"></a>Minha organização precisa de mais de 30 políticas de acesso privilegiado, esse limite será aumentado?

Estamos planejando aumentar o limite atual de 30 políticas de acesso privilegiado por organização do Office 365 em breve.

### <a name="do-i-need-to-be-a-global-admin-to-manage-privileged-access-in-office-365"></a>Preciso ser um administrador global para gerenciar o acesso privilegiado no Office 365?
Não, você precisa ter a função de gerenciamento de função do Exchange atribuída às contas que irão gerenciar o acesso privilegiado no Office 365. No enTanto, a função de administrador global inclui essa função por padrão e pode ser usada para gerenciar o acesso privilegiado se você não quiser configurar a função de gerenciamento de função como uma permissão de conta autônoma. Os usuários que estão incluídos em um grupo de aprovadores não precisam ser um administrador global ou ter a função de gerenciamento de função atribuída para revisar e aprovar solicitações.

### <a name="how-is-privileged-access-management-in-office-365-related-to-customer-lockbox"></a>Como o gerenciamento de acesso privilegiado no Office 365 está relacionado ao Lockbox do cliente?
O [Lockbox de clientes](https://docs.microsoft.com/office365/admin/manage/customer-lockbox-requests) permite que um nível de controle de acesso para as organizações acessem os dados de acordo com o provedor de serviços, ou seja, a Microsoft. O gerenciamento de acesso privilegiado no Office 365 permite o controle de acesso granular dentro de uma organização para todas as tarefas privilegiadas do Office 365.

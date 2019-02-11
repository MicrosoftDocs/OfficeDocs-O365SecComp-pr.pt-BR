---
title: Configurar usuários e casos na Descoberta Eletrônica Avançada do Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 60ffd80b-4376-419d-b6e4-a72029b9907c
description: 'Saiba como configurar funções de usuário, crie casos e atribuir usuários a casos de eDiscovery avançadas do Office 365.  '
ms.openlocfilehash: 4c0043b7651cc82272492e19faf01041c6f67932
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29559054"
---
# <a name="set-up-users-and-cases-in-office-365-advanced-ediscovery"></a>Configurar usuários e casos na Descoberta Eletrônica Avançada do Office 365

Este tópico descreve como configurar usuários e casos de eDiscovery avançadas do Office 365.
  
> [!NOTE]
> A Descoberta Eletrônica Avançada exige um Office 365 E3, com um complemento de Conformidade Avançada ou uma assinatura do E5 para sua organização. Se você não tiver esse plano e quiser tentar a Descoberta Eletrônica Avançada, poderá [Inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
## <a name="prerequisites"></a>Pré-requisitos

Antes de configurar os usuários no eDiscovery avançado e casos, é necessário o seguinte:
  
- Para analisar dados de um usuário usando o eDiscovery avançado, o usuário (o de responsáveis dos dados) deve ser atribuído uma licença do Office 365 E5. Como alternativa, os usuários com uma licença do Office 365 E1 ou E3 podem ser atribuídos uma licença autônoma de eDiscovery avançado. Os administradores e oficiais de conformidade que estão atribuídos ao casos e usam o eDiscovery avançada para analisar dados não precisam de uma licença E5. 
    
- Você precisa ser membro do grupo de função do Gerenciador de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade para criar um caso de eDiscovery e adicionar membros a ela. Adicionar-se ao grupo de função de Gerenciador de descoberta eletrônica em Security &amp; Centro de conformidade, você precisa ser um administrador global na sua organização do Office 365. Se você não for um administrador global, você terá que pedir um administrador global para adicioná-lo ao grupo de função de Gerenciador de descoberta eletrônica. Para obter mais informações, consulte:
    
  - [Permissões de segurança do Office 365 &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md)
    
  - [Atribuir permissões de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade](assign-ediscovery-permissions.md)
    
## <a name="step-1-assign-users-ediscovery-permissions"></a>Etapa 1: Atribuir aos usuários permissões de descoberta eletrônica

A primeira etapa é atribuir as permissões de requisito na segurança de usuários &amp; Centro de conformidade para que eles possam me adicionada como um membro de um caso de eDiscovery. Depois que um usuário é adicionado como um membro de um caso na segurança &amp; Centro de conformidade, eles serão capazes de acessar o caso da eDiscovery avançado.
  
Para atribuir um usuário as permissões necessárias para que eles podem ser adicionados como um membro de um caso de eDiscovery, consulte a etapa 1 em [casos de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade](ediscovery-cases.md#step-1-assign-ediscovery-permissions-to-potential-case-members).
  
## <a name="step-2-create-an-ediscovery-case-and-add-members"></a>Etapa 2: Criar um caso de eDiscovery e adicionar membros

A próxima etapa é criar um novo caso de descoberta eletrônica na segurança &amp; Centro de conformidade e adicionar membros. Membros do caso será capazes de acessar o caso da eDiscovery avançado.
  
1. Para criar um novo caso de descoberta eletrônica, consulte a etapa 2 no [casos de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade](ediscovery-cases.md#step-2-create-a-new-case).
    
2. Para adicionar membros a um caso de descoberta eletrônica, consulte a etapa 3 em [casos de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade](ediscovery-cases.md#step-3-add-members-to-a-case)
    
## <a name="step-3-go-a-case-in-advanced-ediscovery"></a>Etapa 3: Ir um caso de eDiscovery avançado

Depois de criar um caso de eDiscovery e adicionar membros, você (ou qualquer membro do caso) pode acessar o caso correspondente no eDiscovery avançado. Para acessar um caso de descoberta eletrônica avançada, consulte Step 8 em [casos de descoberta eletrônica no Office 365 Security &amp; Centro de conformidade](ediscovery-cases.md#step-8-go-to-the-case-in-advanced-ediscovery).
  
## <a name="see-also"></a>Confira também

[Descoberta Eletrônica Avançada do Office 365](office-365-advanced-ediscovery.md)
  
[Preparação de dados](prepare-data-for-advanced-ediscovery.md)
 
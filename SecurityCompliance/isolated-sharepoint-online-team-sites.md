---
title: Sites de equipe isolados do SharePoint Online
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/15/2017
audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.custom:
- Ent_Solutions
ms.assetid: 71250a04-fd2d-4c3c-a32b-b8a838b19a54
description: 'Resumo: conheça as utilizações dos sites de equipe do SharePoint Online isolados.'
ms.openlocfilehash: 07f4d84493cdc7c0e153186164824fe8aa1e36bc
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34150063"
---
# <a name="isolated-sharepoint-online-team-sites"></a>Sites de equipe isolados do SharePoint Online

 **Resumo:** conheça as utilizações dos sites de equipe do SharePoint Online isolados.
  
Os sites de equipe do SharePoint Online são uma maneira fácil de criar rapidamente um espaço para colaboração em anotações, documentos, artigos, um calendário e outros recursos do Microsoft Office 365. Os sites de equipe do SharePoint Online são baseados em um grupo do Office 365 e possuem um modelo de administração simplificado para permitir a colaboração aberta entre um determinado conjunto de membros do grupo ou toda a organização. Um site de equipe padrão do SharePoint Online permite que os membros do grupo do Office 365 convidem outros usuários e controlem as configurações de permissões.
  
No entanto, em alguns casos, você quer criar um site de equipe do SharePoint Online para colaboração em locais onde as permissões desse site sejam controladas com maior rigidez por meio da associação ao grupo e níveis de permissão do SharePoint Online, que são gerenciados apenas por administradores do SharePoint. Chamamos isso de um site isolado, que é isolado do conjunto de usuários que estão colaborando, visualizando seu conteúdo ou administrando o site. Um site isolado pode ser necessário para o seguinte:
  
- Um projeto secreto em sua organização.
    
- O local da propriedade intelectual altamente confidencial ou valiosa para sua organização.
    
- Os recursos de uma ação judicial iniciada por sua organização ou à qual a empresa está sendo submetida.
    
- Para compartilhar uma assinatura do Office 365 entre várias organizações que possuem alguma sobreposição, mas, na maioria das vezes, existem como entidades comerciais separadas.
    
Veja os requisitos de um site isolado:
  
- Apenas os administradores do SharePoint Online podem realizar a administração de sites, o que inclui a associação ao grupo para acessar o site e a configuração de permissões personalizadas.
    
- Os membros do site não podem convidar outros membros para o site de equipe.
    
- Os usuários que não são membros do site isolado não podem solicitar acesso ao site e verão uma página da Web de acesso negado ao tentar acessar qualquer URL associada ao site.
    
A desvantagem de exigir controle de acesso centralizado e permissões personalizadas pelos administradores do SharePoint Online é que o site manterá-se isolado ao longo do tempo. Por exemplo, os membros atuais não poderão, intencionalmente ou acidentalmente, convidar ou configurar permissões personalizadas para outros usuários na assinatura do Office 365 que não sejam membros do site.
  
Um site isolado pode ser usado com outros recursos, como:
  
- Gerenciamento de Direitos de Informação para garantir que os recursos do site permaneçam criptografados, mesmo que eles sejam baixados localmente e carregados em outro site que esteja disponível para toda a organização.
    
- Prevenção contra a perda de dados para evitar que os usuários enviem os recursos do site, como arquivos, por email.
    
## <a name="next-steps"></a>Próximas etapas

Para experimentar um site de equipe do SharePoint Online isolado em uma assinatura de avaliação, confira as instruções passo a passo no [Site de equipe do SharePoint Online isolado no seu ambiente de desenvolvimento/teste](isolated-sharepoint-online-team-site-dev-test-environment.md).
  
Quando estiver pronto para implantar um site de equipe do SharePoint Online isolado na produção, confira as considerações de design passo a passo no [Projetar um site de equipe do SharePoint Online isolado](design-an-isolated-sharepoint-online-team-site.md).
  
## <a name="see-also"></a>Confira também

[Projetar um site de equipe do SharePoint Online isolado](design-an-isolated-sharepoint-online-team-site.md)
  
[Gerenciar um site de equipe do SharePoint Online isolado](manage-an-isolated-sharepoint-online-team-site.md)

[Implantar um site de equipe do SharePoint Online isolado](deploy-an-isolated-sharepoint-online-team-site.md)



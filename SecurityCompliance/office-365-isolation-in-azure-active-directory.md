---
title: Controle de acesso no Azure Active Directory e isolamento do Office 365
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
description: 'Resumo: Como o isolamento e controle de acesso trabalham dentro do Azure Active Directory.'
ms.openlocfilehash: db4fa0d026c6c608f09252c65bf1e0de5354f68c
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524583"
---
# <a name="isolation-and-access-control-in-azure-active-directory"></a>Isolamento e controle de acesso do Azure Active Directory

Azure Active Directory foi projetado para hospedar vários locatários de maneira altamente segura por meio de isolamento de dados lógicos. Acesso ao Active Directory do Windows Azure, determinado por uma camada de autorização. Azure Active Directory isola clientes usando o locatário contêineres como limites de segurança para proteger o conteúdo do cliente para que o conteúdo não pode ser acessado ou comprometido por inquilinos colegas. Três verificações são executadas pela camada de autorização do Azure Active Directory:
- A entidade está habilitada para acesso ao locatário do Azure Active Directory?
- A entidade está habilitada para acesso aos dados neste locatário?
- É função do principal neste locatário autorizado para o tipo de acesso a dados solicitado?

Nenhum aplicativo, usuário, servidor ou serviço pode acessar o Azure Active Directory sem a devida autenticação e o token ou o certificado. Solicitações serão rejeitadas se eles não são acompanhados por credenciais apropriadas.

Com eficácia, o Azure Active Directory hospeda cada locatário em seu próprio contêiner protegido, com políticas e permissões para e dentro do contêiner exclusivamente pertencentes e gerenciados por inquilino.
 
![Contêiner do Azure](media/office-365-isolation-azure-container.png)

O conceito de contêineres de Inquilino é extremamente bicicletas no serviço de diretório em todas as camadas de portais totalmente para armazenamento persistente. Mesmo quando vários metadados de locatário do Azure Active Directory são armazenados no mesmo disco físico, há nenhuma relação entre os contêineres que não seja o que é definido pelo serviço de diretório, por sua vez, é determinado pelo administrador do locatário. Não pode haver nenhum conexões diretas para o armazenamento do Azure Active Directory de qualquer aplicativo solicitante ou de serviço sem passar primeiro por meio da camada de autorização.

No exemplo a seguir, a Contoso e Fabrikam tem contêineres separados e dedicados e Apesar desses contêineres podem compartilhar algumas da mesma infra-estrutura subjacente, como servidores e armazenamento, eles permanecem separadas e isolados entre si e com porta por camadas de controle de acesso e autorização.
 
![Azure contêineres dedicados](media/office-365-isolation-azure-dedicated-containers.png)

Além disso, não há nenhum componente do aplicativo que pode ser executado de dentro do Windows Azure Active Directory, e não é possível para um locatário obrigatoriamente violar a integridade do outro locatário, acessar as chaves de criptografia do outro locatário ou ler dados brutos do servidor.

Por padrão, o Azure Active Directory proíbe todas as operações emitidas por identidades em outros tenants. Cada locatário é isolado logicamente dentro do Azure Active Directory por meio de controles de acesso baseado em declarações. Leituras e gravações de dados são contêineres de locatário o escopo e de entrada para uma camada de abstração interno e a camada de acesso baseado em função RBAC (controle), que juntos impor o locatário como o limite de segurança de diretório. Todas as solicitações de acesso de dados do diretório é processada por essas camadas e todas as solicitações de acesso no Office 365 é controlada pela lógica de acima.

Azure Active Directory possui América do Norte, governo dos Estados Unidos, União Europeia, Alemanha e World Wide partições. Um locatário existe em uma única partição e partições podem conter vários locatários. Informações de partição são abstraídas dos usuários. Uma determinada partição (incluindo todos os locatários dentro dele) é replicada para vários centros de dados. A partição para um inquilino for escolhida com base nas propriedades do inquilino (por exemplo, o código do país). Segredos e outras informações confidenciais em cada partição é criptografado com uma chave dedicada. As chaves são geradas automaticamente quando uma nova partição é criada.

Funcionalidades de sistema do Azure Active Directory são uma instância exclusiva para cada sessão de usuário. Além disso, o Azure Active Directory usa as tecnologias de criptografia para oferecer isolamento de recursos compartilhados do sistema no nível da rede para evitar a transferência não autorizada e acidentais de informações.

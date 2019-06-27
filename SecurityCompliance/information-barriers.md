---
title: Visão geral das barreiras de informações
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 06/26/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: Use as barreiras de informação para garantir a conformidade de comunicação usando o Microsoft Teams em sua organização.
ms.openlocfilehash: 6565fc28d70ac6ff9a6f4df6edc75b89d19ae29a
ms.sourcegitcommit: 1c254108c522d0cb44023565268b5041d07748aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/27/2019
ms.locfileid: "35279469"
---
# <a name="information-barriers-preview"></a>Barreiras de informação (visualização)

## <a name="overview"></a>Visão geral

Os serviços de nuvem da Microsoft incluem recursos avançados de comunicação e colaboração. Mas suponha que você deseja restringir as comunicações entre dois grupos para evitar um conflito de interesse de ocorrer em sua organização. Ou, talvez você queira restringir as comunicações entre determinadas pessoas dentro da sua organização para proteger informações internas. A Microsoft 365 permite a comunicação e a colaboração entre grupos e organizações, portanto, há uma maneira de restringir as comunicações entre grupos específicos de usuários quando necessário? Com as barreiras de informação, você pode! 

As barreiras de informação estão em versão prévia agora, começando com o Microsoft Teams. Quando esses recursos estão disponíveis para sua organização, um administrador de conformidade ou barreiras de informações pode definir políticas para permitir ou impedir a comunicação entre grupos de usuários no Microsoft Teams. As políticas de barreira de informações podem ser usadas para situações como estas:

- Um dia dos traders não pode ligar para alguém na equipe de marketing
- O pessoal financeiro que trabalha em informações confidenciais da empresa não pode receber chamadas de determinados grupos dentro de sua organização
- Uma equipe interna com material secreto comercial não pode ligar ou bater papo com pessoas de determinados grupos de sua organização
- Uma equipe de pesquisa pode apenas ligar ou conversar online com uma equipe de desenvolvimento de produtos

Para todos esses cenários de exemplo (e mais), as políticas de barreira de informações podem ser definidas para impedir ou permitir comunicações no Microsoft Teams. Essas políticas podem impedir que as pessoas chamem ou chat com as que elas não deveriam ou permitir que as pessoas se comuniquem somente com grupos específicos no Microsoft Teams. Com as políticas de barreira de informações em vigor, sempre que os usuários que estão cobertos por essas políticas tentarem se comunicar com outras pessoas no Microsoft Teams, as verificações são realizadas para impedir (ou permitir) a comunicação (conforme definido pelas políticas de barreira de informações). Para saber mais sobre a experiência do usuário com barreiras de informações, confira [barreiras de informações no Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams).

> [!NOTE]
> As barreiras de informação não se aplicam às comunicações por email ou ao compartilhamento de arquivos por meio do SharePoint Online ou do OneDrive. Além disso, as barreiras de informação são independentes dos [limites de conformidade](set-up-compliance-boundaries.md).

## <a name="required-licenses-and-permissions"></a>Licenças e permissões necessárias

**No momento, o recurso de barreira de informações está em visualização privada**. Quando esses recursos estão disponíveis em geral, eles serão incluídos em assinaturas, como:

- Microsoft 365 E5
- Office 365 e5
- Conformidade Avançada do Office 365
- Conformidade e proteção de informações do Microsoft 365 e5

Para obter mais detalhes, consulte [soluções de conformidade](https://products.office.com/business/security-and-compliance/compliance-solutions).

Para [definir ou editar as políticas de barreira de informações](information-barriers-policies.md), você deve ter uma das seguintes funções:

- Administrador global do Microsoft 365
- Administrador global do Office 365
- Administrador de conformidade
- Administrador de barreiras de informações

Você deve estar familiarizado com os cmdlets do PowerShell para definir, validar ou editar as políticas de barreira de informações. Embora forneçamos vários exemplos de cmdlets do PowerShell nas [informações de instruções](information-barriers-policies.md), você precisará saber detalhes adicionais, como parâmetros, para sua organização.

## <a name="concepts-of-information-barrier-policies"></a>Conceitos de políticas de barreira de informações

É útil saber os conceitos subjacentes das políticas de barreira de informações:

- Os **atributos da conta de usuário** são definidos no Azure Active Directory (ou no Exchange Online). Esses atributos podem incluir departamento, cargo, local, nome da equipe e outros detalhes do perfil de trabalho. 

- Os **segmentos** são conjuntos de usuários que são definidos no centro de conformidade & segurança do Office 365 usando um **atributo de conta de usuário**selecionado. (Confira a [lista de atributos com suporte](information-barriers-attributes.md).) 

- **As políticas de barreira de informações** determinam limites ou restrições de comunicação. Ao definir políticas de barreira de informações, escolha um dos dois tipos de políticas:
    - As políticas de "bloqueio" impedem um segmento de se comunicar com outro segmento.
    - As políticas de "permitir" permitem que um segmento se comunique apenas com determinados segmentos.

- O **aplicativo de política** é feito após a definição de todas as políticas de barreira de informações e você está pronto para aplicá-las em sua organização.

## <a name="next-steps"></a>Próximas etapas

- [Saiba mais sobre as barreiras de informação no Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams)
- [Ver os atributos que podem ser usados para políticas de barreira de informações](information-barriers-attributes.md)
- [Definir políticas para barreiras de informações](information-barriers-policies.md) 


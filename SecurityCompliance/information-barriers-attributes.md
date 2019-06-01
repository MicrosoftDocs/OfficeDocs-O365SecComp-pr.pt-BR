---
title: Atributos para políticas de barreira de informações
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 05/31/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: Use este artigo como referência para vários atributos que podem ser usados em políticas de barreira de informações.
ms.openlocfilehash: e72e37950442974897de479c7c11f0053a578d1c
ms.sourcegitcommit: 4fedeb06a6e7796096fc6279cfb091c7b89d484d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/31/2019
ms.locfileid: "34668272"
---
# <a name="attributes-for-information-barrier-policies-preview"></a>Atributos para políticas de barreira de informações (versão prévia)

Determinados atributos no Azure Active Directory podem ser usados para segmentar usuários. Os segmentos são então usados como filtros para políticas de barreira de informações. Por exemplo, você pode usar o **Departamento** para definir segmentos de usuários por departamento em sua organização (supondo que nenhum único funcionário funcione para dois departamentos ao mesmo tempo). 

Este artigo fornece uma lista de atributos que podem ser usados. Para saber mais sobre as barreiras de informação, confira os seguintes recursos:
- [Barreiras de informação (visualização)](information-barriers.md)
- [Definir políticas para barreiras de informações no Microsoft Teams (visualização)](information-barriers-policies.md)

## <a name="how-to-use-attributes-in-information-barrier-policies"></a>Como usar atributos em políticas de barreira de informações

Os atributos listados neste artigo podem ser usados para definir (ou editar) segmentos de usuários. Os segmentos são usados como parâmetros (UserGroupFilter) em políticas de barreira de informações, conforme mostrado nos exemplos a seguir:

|Exemplo  |Cmdlet  |
|---------|---------|
|Definir um segmento chamado Segment1 usando o atributo Department     | `New-OrganizationSegment -Name "Segment1" -UserGroupFilter "Department -eq 'Department1'"`        |
|Defina um segmento chamado segmenta usando o atributo MemberOf (Suponha que este atributo contenha nomes de grupo, como "Blueus")     | `New-OrganizationSegment -Name "SegmentA" -UserGroupFilter "MemberOf -eq 'BlueGroup'"`        |
|Defina um segmento chamado DayTraders usando ExtensionAttribute1 (Suponha que este atributo contenha cargos, como "DayTrader")|`New-OrganizationSegment -Name "DayTraders" -UserGroupFilter "ExtensionAttribute1 -eq 'DayTrader'"` |

Ao definir segmentos, use o mesmo atributo para todos os seus segmentos. Por exemplo, se você definir alguns segmentos usando *Departamento*, defina todos os segmentos usando *Departamento*. Não defina alguns segmentos usando o *Departamento* e outros usando *memberOf*. Certifique-se de que seus segmentos não se sobreponham; cada usuário deve ser atribuído a exatamente um segmento. 

Para saber mais, confira [definir segmentos usando o PowerShell](information-barriers-policies.md#define-segments-using-powershell).

## <a name="reference"></a>Referência

A tabela a seguir lista os atributos que você pode usar com as barreiras de informação.

|Nome da Propriedade do Active Directory do Azure (nome para exibição LDAP)  |Nome da Propriedade do Exchange  |
|---------|---------|
|Coautores       | Coautores        |
|Empresa     |Empresa         |
|Departamento     |Departamento         |
|ExtensionAttribute1 |CustomAttribute1  |
|ExtensionAttribute2 |CustomAttribute2  |
|ExtensionAttribute3 |CustomAttribute3  |
|ExtensionAttribute4 |CustomAttribute4  |
|ExtensionAttribute5 |CustomAttribute5  |
|ExtensionAttribute6 |CustomAttribute6  |
|ExtensionAttribute7 |CustomAttribute7  |
|ExtensionAttribute8 |CustomAttribute8  |
|ExtensionAttribute9 |CustomAttribute9  |
|ExtensionAttribute10 |CustomAttribute10  |
|ExtensionAttribute11 |CustomAttribute11  |
|ExtensionAttribute12 |CustomAttribute12  |
|ExtensionAttribute13 |CustomAttribute13  |
|ExtensionAttribute14 |CustomAttribute14  |
|ExtensionAttribute15 |CustomAttribute15  |
|MSExchExtensionCustomAttribute1 |ExtensionCustomAttribute1 |
|MSExchExtensionCustomAttribute2 |ExtensionCustomAttribute2 |
|MSExchExtensionCustomAttribute3 |ExtensionCustomAttribute3 |
|MSExchExtensionCustomAttribute4 |ExtensionCustomAttribute4 |
|MSExchExtensionCustomAttribute5 |ExtensionCustomAttribute5 |
|MailNickname |Alias |
|PhysicalDeliveryOfficeName |Office |
|PostalCode |PostalCode |
|ProxyAddresses |EndereçosEmail |
|StreetAddress |StreetAddress |
|TargetAddress |ExternalEmailAddress |
|UsageLocation |UsageLocation |
|Principal  |Principal  |
|Correio   |WindowsEmailAddress    |
|Descrição    |Descrição    |
|Tattoo   |MemberOfGroup  |

## <a name="related-topics"></a>Tópicos relacionados

[Definir políticas para barreiras de informações no Microsoft Teams (visualização)](information-barriers-policies.md)

[Solucionando problemas de barreiras de informações (versão prévia)](information-barriers-troubleshooting.md)

[Barreiras de informação (visualização)](information-barriers.md)




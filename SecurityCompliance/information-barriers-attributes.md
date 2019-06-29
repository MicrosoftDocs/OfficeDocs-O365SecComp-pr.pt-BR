---
title: Atributos para políticas de barreira de informações
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 06/28/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: Use este artigo como referência para vários atributos que podem ser usados em políticas de barreira de informações.
ms.openlocfilehash: 896b87a3ccc696d3a8193e37237fe555d326ca52
ms.sourcegitcommit: 011bfa60cafdf47900aadf96a17eb275efa877c4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/29/2019
ms.locfileid: "35394306"
---
# <a name="attributes-for-information-barrier-policies-preview"></a>Atributos para políticas de barreira de informações (versão prévia)

Determinados atributos no Azure Active Directory podem ser usados para segmentar usuários. Depois que os segmentos são definidos, esses segmentos podem ser usados como filtros para políticas de barreira de informações. Por exemplo, você pode usar o **Departamento** para definir segmentos de usuários por departamento em sua organização (supondo que nenhum único funcionário funcione para dois departamentos ao mesmo tempo). 

Este artigo descreve como usar atributos com barreiras de informação e fornece uma lista de atributos que podem ser usados. Para saber mais sobre as barreiras de informação, confira os seguintes recursos:
- [Barreiras de informação (visualização)](information-barriers.md)
- [Definir políticas para barreiras de informações no Microsoft Teams (visualização)](information-barriers-policies.md)
- [Editar (ou remover) políticas de barreira de informações (visualização)](information-barriers-edit-segments-policies.md.md)

## <a name="how-to-use-attributes-in-information-barrier-policies"></a>Como usar atributos em políticas de barreira de informações

Os atributos listados neste artigo podem ser usados para definir ou editar segmentos de usuários. Seus segmentos definidos servem como parâmetros (chamados valores *UserGroupFilter* ) em [políticas de barreira de informações](information-barriers-policies.md).

1. Determine o atributo que você deseja usar para definir segmentos. (Consulte a seção [referência](#reference) neste artigo.)

2. Verifique se as contas de usuário têm valores preenchidos para o (s) atributo (s) que você selecionou na etapa 1. Exibir detalhes da conta de usuário e, se necessário, editar contas de usuário para incluir valores de atributo. 

    Para fazer isso usando o PowerShell, confira [Configurar Propriedades da conta de usuário com o Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/configure-user-account-properties-with-office-365-powershell).

    Para fazer isso no Azure Active Directory, confira [Adicionar ou atualizar as informações de perfil de um usuário usando o Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal).

3. [Defina segmentos usando o PowerShell](information-barriers-policies.md#define-segments-using-powershell), de forma semelhante aos seguintes exemplos:

    |Exemplo  |Cmdlet  |
    |---------|---------|
    |Definir um segmento chamado Segment1 usando o atributo Department     | `New-OrganizationSegment -Name "Segment1" -UserGroupFilter "Department -eq 'Department1'"`        |
    |Defina um segmento chamado segmenta usando o atributo MemberOf (Suponha que este atributo contenha nomes de grupo, como "Blueus")     | `New-OrganizationSegment -Name "SegmentA" -UserGroupFilter "MemberOf -eq 'BlueGroup'"`        |
    |Defina um segmento chamado DayTraders usando ExtensionAttribute1 (Suponha que este atributo contenha cargos, como "DayTrader")|`New-OrganizationSegment -Name "DayTraders" -UserGroupFilter "ExtensionAttribute1 -eq 'DayTrader'"` |

    > [!TIP]
    > Ao definir segmentos, use o mesmo atributo para todos os seus segmentos. Por exemplo, se você definir alguns segmentos usando *Departamento*, defina todos os segmentos usando *Departamento*. Não defina alguns segmentos usando o *Departamento* e outros usando *memberOf*. Certifique-se de que seus segmentos não se sobreponham; cada usuário deve ser atribuído a exatamente um segmento. 

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




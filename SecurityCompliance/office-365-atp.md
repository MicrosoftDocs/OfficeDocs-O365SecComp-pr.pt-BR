---
title: Proteção Avançada contra Ameaças do Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/28/2019
ms.audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e100fe7c-f2a1-4b7d-9e08-622330b83653
ms.collection:
- M365-security-compliance
description: A proteção avançada contra ameaças do Office 365 inclui anexos seguros, links seguros, ferramentas anti-phishing avançadas, ferramentas de relatórios e recursos de inteligência de ameaças.
ms.openlocfilehash: 402110fa7b835cd86ffbcf14439304d364cf03dd
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262943"
---
# <a name="office-365-advanced-threat-protection"></a>Proteção Avançada contra Ameaças do Office 365

> [!IMPORTANT]
> Este artigo destina-se aos clientes do Office 365 Enterprise e do Microsoft 365 Enterprise. Se você estiver usando o Outlook.com, o Office 365 Home ou o Office 365 Personal e estiver procurando informações sobre links seguros no Outlook, consulte [Advanced Outlook.com Security](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2).

## <a name="overview"></a>Visão Geral

A proteção avançada contra ameaças (ATP) do Office 365 protege sua organização contra ameaças maliciosas representadas por mensagens de email, links (URLs) e ferramentas de colaboração. A ATP inclui:

- [Políticas de proteção contra ameaças](#configure-atp-policies): defina as políticas de proteção contra ameaças para definir o nível apropriado de proteção para sua organização. 

- [Relatórios](#view-atp-reports): exibir relatórios em tempo real para monitorar o desempenho da ATP em sua organização. 

- [Recursos de investigação e resposta contra ameaças](#use-threat-investigation-and-response-capabilities): Use ferramentas de ponta para investigar, entender, simular e evitar ameaças. 

- [Recursos automatizados de investigação e resposta](#save-time-with-automated-investigation-and-response): Economize tempo e esforço ao investigar e reduzir as ameaças.

## <a name="configure-atp-policies"></a>Configurar diretivas ATP

O Office 365 ATP oferece várias ferramentas para definir um nível apropriado de proteção para sua organização. 

A equipe de segurança da sua organização deve definir políticas para cada ferramenta ATP no centro de conformidade do & de segurança do Office 365. Vá para **** > **política** de gerenciamento de ameaças para acessar opções de política. (Para obter ajuda para isso, confira [Guia de início rápido: configurar a proteção avançada contra ameaças do Office 365](checklist-atp-setup.md).)

As políticas definidas para sua organização determinam o comportamento e o nível de proteção para ameaças predefinidas. As opções de política são extremamente flexíveis. Por exemplo, a equipe de segurança da sua organização pode definir a proteção de ameaças refinada no nível de usuário, organização, destinatário e domínio. É importante revisar suas políticas regularmente, pois surgem novas ameaças e desafios.  

- [Anexos seguros de ATP](atp-safe-attachments.md): oferece proteção de dia zero para proteger seu sistema de mensagens, verificando anexos de email em busca de conteúdo mal-intencionado. Ele roteia todas as mensagens e anexos que não têm uma assinatura de vírus/malware para um ambiente especial e, em seguida, usa as técnicas de aprendizado e análise da máquina para detectar más intenções. Se nenhuma atividade suspeita for encontrada, a mensagem será encaminhada para a caixa de correio. Para saber mais, confira [configurar as políticas de anexos seguros de ATP do Office 365](set-up-atp-safe-attachments-policies.md).

- [Links seguros de ATP](atp-safe-links.md): oferece verificação de tempo de clique de URLs em mensagens de email e arquivos do Office. A proteção está em andamento e se aplica a seu ambiente de mensagens e do Office. Os links são verificados para cada clique: os links seguros permanecem acessíveis e os links mal-intencionados são bloqueados dinamicamente. Para saber mais, confira [configurar as políticas de links seguros de ATP do Office 365](https://docs.microsoft.com/en-us/office365/securitycompliance/set-up-atp-safe-links-policies). 

- [ATP para SharePoint, onedrive e Microsoft Teams](atp-for-spo-odb-and-teams.md): protege sua organização quando os usuários colaboram e compartilham arquivos, identificando e bloqueando arquivos mal-intencionados em sites de equipe e bibliotecas de documentos. Para saber mais, confira [ativar o Office 365 ATP para SharePoint, onedrive e Microsoft Teams](turn-on-atp-for-spo-odb-and-teams.md). 

- [Proteção anti-phishing do ATP](atp-anti-phishing.md): detecta tentativas de representar seus usuários e domínios personalizados. Ele aplica modelos de aprendizado de máquina e algoritmos avançados de detecção de representação a ataques de phishing da AVERT. Para saber mais, confira [configurar as políticas de anti-phishing e anti-phishing do Office 365 ATP](set-up-anti-phishing-policies.md).

## <a name="view-atp-reports"></a>Exibir relatórios da ATP

O Office 365 ATP inclui um [painel](view-reports-for-atp.md) avançado de relatórios para monitorar o desempenho da ATP. Você pode acessá-lo em **relatórios do _GT_ Dashboard** no centro de conformidade do _AMP_ de segurança. 

Relata a atualização em tempo real, fornecendo as informações mais recentes. Esses relatórios também fornecem recomendações e alertam você sobre ameaças iminentes. Relatórios preDefinidos incluem o [Explorador de ameaças](use-explorer-in-security-and-compliance.md), o relatório de [status de proteção contra ameaças](view-reports-for-atp.md#threat-protection-status-report), o relatório de tipos de [arquivos ATP](view-reports-for-atp.md#atp-file-types-report), o [relatório de disposição de mensagens ATP](view-reports-for-atp.md#atp-message-disposition-report) e muito mais. 

## <a name="use-threat-investigation-and-response-capabilities"></a>Usar os recursos de investigação e resposta contra ameaças

O Office 365 ATP Plan 2 inclui as melhores ferramentas de [investigação e resposta de ameaças](office-365-ti.md) que permitem que a equipe de segurança da sua organização antecipe, entenda e Evite ataques mal-intencionados. 

- Os rastreadores de [ameaças](threat-trackers.md) fornecem a mais recente inteligência em problemas de cybersecurity de prevalecentes. Por exemplo, você pode exibir informações sobre o malware mais recente e tomar medidas defensivas antes de se tornar uma ameaça real à sua organização. Os rastreadores disponíveis [](threat-trackers.md#noteworthy-trackers)incluem rastreadores dignos de [tendências](threat-trackers.md#trending-trackers), rastreadores, [consultas rastreadas](threat-trackers.md#tracked-queries)e [consultas salvas](threat-trackers.md#saved-queries).

- [Explorer](use-explorer-in-security-and-compliance.md) (também chamado de Gerenciador de ameaças) é um relatório em tempo real que permite identificar e analisar ameaças recentes. Você pode configurar o Explorer para mostrar dados para períodos personalizados.

- O simulador de [ataques](attack-simulator.md) permite que você execute cenários de ataque realísticos em sua organização para identificar o vulnerabilites. Estão disponíveis simulações de tipos de ataques atuais, incluindo o [nome de exibição spear-phishing Attack](attack-simulator.md#display-name-spear-phishing-attack), um ataque de irrigação de [senha](attack-simulator.md#password-spray-attack), um ataque de [senha de força bruta](attack-simulator.md#brute-force-password-attack)e muito mais.
    
## <a name="save-time-with-automated-investigation-and-response"></a>Economize tempo com investigação e resposta automatizadas

(**Novo!**) Quando você está investigando um ataque potencial na CyberSource, o tempo é da essência. Quanto mais cedo você puder identificar e reduzir as ameaças, melhor será a sua organização. O Office 365 ATP Plan 2 agora inclui recursos [de investigação e resposta automatizados (Air)](automated-investigation-response-office.md) . (Se você ainda não tem esses recursos, você os terá em breve com o plano ATP 2).

O AIR inclui um conjunto de guias de segurança que podem ser iniciados automaticamente, como quando um alerta é disparado ou manualmente, como de um modo de exibição no explorador de ameaças. O AIR pode economizar tempo e esforço da equipe de operações de segurança para reduzir as ameaças, com eficácia e eficiência. Para saber mais, confira [investigação e resposta automatizadas (Air) com o Office 365](automated-investigation-response-office.md).

## <a name="permissions-required-to-use-atp-features"></a>Permissões necessárias para usar os recursos de ATP

Para acessar os recursos de ATP no centro de conformidade do & de segurança, você deve ter uma função apropriada atribuída. A tabela a seguir inclui alguns exemplos:

|Função ou grupo de função  |Recursos para saber mais  |
|---------|---------|
|Administrador global do Office 365 |[Tudo sobre as funções de administrador do Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles)|
|Administrador de segurança |[Permissões de função de administrador no Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/directory-assign-admin-roles)|
|Gerenciamento da organização do Exchange Online |[Permissões no Exchange Online](https://docs.microsoft.com/en-us/exchange/permissions-exo/permissions-exo) <br>e<br> [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)|

Para obter mais informações, consulte:

- [Permissões no centro de conformidade do & de segurança](permissions-in-the-security-and-compliance-center.md) 

- [Conceder aos usuários acesso ao centro de conformidade do & de segurança](grant-access-to-the-security-and-compliance-center.md)

## <a name="get-office-365-atp"></a>Obter o Office 365 ATP

O Office 365 ATP Plan 2 está incluído no Office 365 Enterprise e5, no Office 365 Education e no Microsoft 365 Business. Se sua assinatura não incluir o Office 365 ATP, você poderá comprar ATP como um complemento. Para saber mais, confira os seguintes recursos:

- Consulte [disponibilidade de proteção avançada contra ameaças (ATP) do Office 365](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#office-365-advanced-threat-protection-atp-availability) para obter uma lista de assinaturas que incluem planos ATP.

- Consulte [disponibilidade de recursos nos planos de proteção avançada contra ameaças (ATP)](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#feature-availability-across-advanced-threat-protection-atp-plans) para obter uma lista de recursos incluídos no plano 1 e 2.

- ConFira [obter a proteção avançada contra ameaças avançadas do office 365](https://products.office.com/exchange/advance-threat-protection#pmg-allup-content) para comparar planos e comprar o Office 365 ATP.

## <a name="new-features-in-office-365-atp"></a>Novos recursos no Office 365 ATP

Novos recursos são adicionados ao Office 365 ATP continuamente. Para saber mais, confira os seguintes recursos:

- O [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap?filters=&searchterms=advanced%2Cthreat%2Cprotection) fornece uma lista de novos recursos de desenvolvimento e distribuição.

- A [Descrição do serviço proteção avançada contra ameaças do Office 365](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp) descreve os recursos e a disponibilidade nos planos ATP.

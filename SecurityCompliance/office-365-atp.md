---
title: Proteção Avançada contra Ameaças do Office 365
ms.author: tracyp
author: msfttracyp
manager: dansimp
ms.date: 03/28/2019
audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
- MOE150
ms.assetid: e100fe7c-f2a1-4b7d-9e08-622330b83653
ms.collection:
- M365-security-compliance
description: O Office 365 proteção avançada contra ameaças inclui anexos seguros, links seguros, ferramentas anti-phishing avançadas, ferramentas de relatório e recursos de inteligência de ameaças.
ms.openlocfilehash: ca948fdd99ca04830ecb7685ed8930a71345299f
ms.sourcegitcommit: 7a0cb7e1da39fc485fc29e7325b843d16b9808af
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/07/2019
ms.locfileid: "36231085"
---
# <a name="office-365-advanced-threat-protection"></a>Proteção Avançada contra Ameaças do Office 365

> [!IMPORTANT]
> Esse artigo destina-se aos clientes corporativos [que têm proteção avançada contra](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)ameaças do Office 365. Se você estiver usando o Outlook.com, o Office 365 Home ou o Office 365 Personal e estiver procurando por informações sobre links seguros no Outlook, confira [segurança avançada do Outlook.com](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2).

## <a name="overview"></a>Visão Geral

O Office 365 proteção avançada contra ameaças (ATP) protege sua organização contra ameaças maliciosas, que são enviadas por mensagens de email, links (URLs) e ferramentas de colaboração. ATP inclui:

- [Políticas de proteção contra ameaças](#configure-atp-policies): definir políticas de proteção contra ameaças para definir o nível de proteção apropriado para a sua organização. 

- [Relatórios](#view-atp-reports): exibir relatórios em tempo real para monitorar o desempenho ATP na sua organização. 

- [Recursos de investigação e resposta de ameaças](#use-threat-investigation-and-response-capabilities): Use as ferramentas de ponta para investigar, compreender, simular e prevenir ameaças. 

- [Recursos](#save-time-with-automated-investigation-and-response)automatizados de investigação e resposta: Poupe tempo e esforço investigando e reduza as ameaças.

## <a name="office-365-atp-plan-1-and-plan-2"></a>Office 365 ATP plano 1 e plano 2

ATP está incluído no Office 365 E5; no entanto, o plano ATP 1 e o plano ATP 2 estão disponíveis como um complemento para determinadas assinaturas. Para saber mais, confira [disponibilidade de recursos em planos ATP](https://docs.microsoft.com/pt-BR/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#feature-availability-across-advanced-threat-protection-atp-plans).

## <a name="configure-atp-policies"></a>Configurar políticas ATP

O Office 365 ATP oferece inúmeras ferramentas para definir um nível de proteção apropriado para a sua organização. 

A equipe de segurança da sua organização deve definir políticas para cada ferramenta ATP no centro de conformidade & segurança do Office 365. Vá para **política de gerenciamento** > **de ameaças **para acessar as opções de política. (Para obter ajuda par isso, confira[Guia de início rápido: configurar a proteção avançada contra ameaças do Office 365](checklist-atp-setup.md).)

As políticas definidas para a sua organização determinam o comportamento e o nível de proteção das ameaças predefinidas. As opções de política são extremamente flexíveis. Por exemplo, a equipe de segurança da sua organização pode definir a proteção de ameaças individualizada no nível do usuário, da organização, do destinatário e do domínio. É importante revisar suas políticas regularmente porque novas ameaças e desafios surgem diariamente.  

- [Anexos seguros do ATP](atp-safe-attachments.md): fornece proteção zero ao seu sistema de mensagens, verificando anexos de email em busca de conteúdo mal-intencionado. Ele roteia todas as mensagens e anexos que não têm uma assinatura de vírus/malware em um ambiente especial e, em seguida, usa técnicas de aprendizagem e análise de máquina para detectar tentativas maliciosas. Se nenhuma atividade suspeita for encontrada, a mensagem será encaminhada para a caixa de correio. Para saber mais, confira [configurar a política de anexos seguros do Office 365 ATP](set-up-atp-safe-attachments-policies.md).

- [Links de segurança ATP](atp-safe-links.md): fornece verificação de tempo de clique das URLs, por exemplo, em mensagens de email e arquivos do Office. A proteção é contínua e se aplica a suas mensagens e ambiente do Office. Os links são verificados para cada clique: links seguros permanecem acessíveis e os links mal-intencionados são bloqueados dinamicamente. Para saber mais, confira [Configurar políticas de links seguros do Office 365 ATP ](https://docs.microsoft.com/pt-BR/office365/securitycompliance/set-up-atp-safe-links-policies). 

- [ATP para o SharePoint, o onedrive e o Microsoft Teams](atp-for-spo-odb-and-teams.md): protege sua organização quando os usuários colaboram e compartilham arquivos, identificando e bloqueando arquivos mal-intencionados em sites de equipe e bibliotecas de documentos. Para saber mais, confira [Office 365 ATP para SharePoint, OneDrive e Microsoft Teams](turn-on-atp-for-spo-odb-and-teams.md). 

- [Proteção anti-phishing do ATP](atp-anti-phishing.md): detecta tentativas de representar seus usuários e domínios personalizados. Ele aplica modelos de aprendizagem de computador e algoritmos avançados de detecção de representação para evitar ataques de phishing. Para saber mais, confira[ Configurar políticas antiphishing e antiphishing da ATP do Office 365](set-up-anti-phishing-policies.md).

## <a name="view-atp-reports"></a>Exibir relatórios da ATP

O Office 365 ATP inclui um painel [de relatórios avançado](view-reports-for-atp.md) para monitorar o desempenho do ATP. Você pode acessá-lo em ** relatórios > Dashboard **no centro de conformidade & de segurança. 

Os relatórios são atualizados em tempo real, fornecendo as informações mais recentes. Esses relatórios também fornecem recomendações e alertam você sobre ameaças iminentes. Os relatórios predefinidos incluem o seguinte: 

- [Explorador de Ameaças (e detecções em tempo real)](threat-explorer.md)

- [Status da proteção contra ameaças](view-reports-for-atp.md#threat-protection-status-report)

- [Relatório de tipos de arquivo ATP](view-reports-for-atp.md#atp-file-types-report)

- [Relatório de disposição da mensagem ATP](view-reports-for-atp.md#atp-message-disposition-report)

- ... e muito mais. 

## <a name="use-threat-investigation-and-response-capabilities"></a>Como funciona a investigação e resposta a ameaças

O Office 365 ATP plano 2 inclui uma melhor investigação de [ameaças e ferramentas](office-365-ti.md) de resposta que permitem que a equipe de segurança da sua organização facilite, entenda e impeça ataques mal-intencionados. 

- [Os rastreadores](threat-trackers.md) de ameaças oferecem a mais recente inteligência sobre problemas segurança cibernéticas. Por exemplo, você pode exibir informações sobre o malware mais recente e executar medidas defensivas antes que ele se torne uma ameaça real à sua organização. Os acompanhantes disponíveis incluem rastreadores[rastreadores notaveis](threat-trackers.md#noteworthy-trackers), [rastreadores de tendências](threat-trackers.md#trending-trackers), [consultas controladas ](threat-trackers.md#tracked-queries)e [consultas salvas](threat-trackers.md#saved-queries).

- [O explorador de ameaças (ou detecções em tempo real](threat-explorer.md) ) (também chamado de Gerenciador) é um relatório em tempo real que permite identificar e analisar ameaças recentes. Você pode configurar o Explorer para mostrar dados de períodos personalizados.

- [O Attack Simulator ](attack-simulator.md) permite que você execute cenários de ataque realista em sua organização para identificar as vulnerabilidades. As simulações de tipos de ataque atuais estão disponíveis, incluindo [um nome de exibição, um](attack-simulator.md#display-name-spear-phishing-attack)ataque de [spear phishing, um](attack-simulator.md#password-spray-attack)ataque de [borrifada por senha,](attack-simulator.md#brute-force-password-attack)um ataque de senha de força bruta, e muito mais.
    
## <a name="save-time-with-automated-investigation-and-response"></a>Como funciona a investigação e resposta automatizada

(**Novo! **) Quando você estiver investigando um ataque potencial, tempo é uma essência. Quanto mais cedo você puder identificar e reduzir as ameaças, melhor será a sua organização. O Office 365 ATP plano 2 agora inclui [os recursos de investigação e resposta automatizada (Air).](automated-investigation-response-office.md) (Se você ainda não tiver esses recursos, estará tudo em breve com o plano ATP 2.)

O AIR inclui um conjunto de guias de segurança que podem ser iniciados automaticamente, como quando um alerta é acionado ou manualmente, como em um modo de exibição no Explorer. O AIR pode economizar o tempo e o esforço da equipe de operações de segurança para reduzir as ameaças de maneira eficaz e eficiente. Para saber mais, confira [Introdução à resposta e investigação de ameaças do Office 365](automated-investigation-response-office.md).

## <a name="permissions-required-to-use-atp-features"></a>Permissões necessárias para usar os recursos do ATP

Para acessar os recursos do ATP no centro de conformidade & de segurança, você deve ter uma função adequada. A tabela abaixo fornece alguns exemplos:

|Função ou grupo de função  |Recursos para saber mais  |
|---------|---------|
|Administrador global do Office 365 |[Tudo sobre as funções de administrador do Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles)|
|Administrador de Segurança |
  [Permissões da função de administrador no Azure Active Directory](https://docs.microsoft.com/pt-BR/azure/active-directory/users-groups-roles/directory-assign-admin-roles)|
|Gerenciamento de Organização do Exchange Online |
  [Permissões no Exchange Online](https://docs.microsoft.com/pt-BR/exchange/permissions-exo/permissions-exo) <br>e<br> [PowerShell do Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)|

Para saber mais, veja:

- [Permissões no Centro de Conformidade e Segurança](permissions-in-the-security-and-compliance-center.md) 

- [Conceder aos usuários acesso ao Centro de Conformidade e Segurança](grant-access-to-the-security-and-compliance-center.md)

## <a name="get-office-365-atp"></a>Obter o Office 365 ATP

O Office 365 ATP plano 2 está incluído no Office 365 Enterprise e5, no Office 365 Education A5 e no Microsoft 365 Business. Se a sua assinatura não inclui o Office 365 ATP, você pode comprar plano ATP 1 ou plano ATP 2 como um complemento para determinadas assinaturas. Para saber mais, confira os seguintes recursos:

- Confira [disponibilidade da proteção avançada contra ameaças (ATP) do Office 365](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#office-365-advanced-threat-protection-atp-availability) para obter uma lista de assinaturas que incluem planos ATP.

- Veja [a disponibilidade de recursos em planos de proteção avançada contra ameaças (ATP) ](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#feature-availability-across-advanced-threat-protection-atp-plans)para obter uma lista dos recursos incluídos no plano 1 e 2.

- Confira [obter a proteção avançada contra ameaças do Office 365 ](https://products.office.com/exchange/advance-threat-protection#pmg-allup-content) para comparar os planos e comprar o Office 365 ATP.

## <a name="new-features-in-office-365-atp"></a>Experimentar novos recursos no Office 365

Novos recursos são adicionados ao Office 365 ATP continuamente. Para saber mais, confira os seguintes recursos:

- O [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap?filters=&searchterms=advanced%2Cthreat%2Cprotection) fornece uma lista dos novos recursos de desenvolvimento e implantação.

- A [Descrição do serviço proteção avançada contra ameaças do Office 365 ](https://docs.microsoft.com/pt-BR/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp) descreve os recursos e a disponibilidade dos planos ATP.

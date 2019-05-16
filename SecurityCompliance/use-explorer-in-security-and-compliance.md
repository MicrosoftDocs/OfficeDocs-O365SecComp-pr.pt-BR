---
title: Usar o explorador de ameaças no &amp; centro de conformidade de segurança
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/31/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 82ac9922-939c-41be-9c8a-7c75b0a4e27d
ms.collection:
- M365-security-compliance
description: Saiba mais sobre o Explorer (também chamado de Gerenciador de ameaças &amp; ) no centro de conformidade de segurança.
ms.openlocfilehash: 30f3759b6eb35508a9de8c03abb72562417aa04f
ms.sourcegitcommit: 0d5a863f48914eeaaf29f7d2a2022618de186247
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/15/2019
ms.locfileid: "34077327"
---
# <a name="use-threat-explorer-in-the-security-amp-compliance-center"></a>Usar o explorador de ameaças no &amp; centro de conformidade de segurança

Se sua organização tiver o [Office 365 Advanced Threat Protection Plan 2](office-365-ti.md) (ATP) e você tiver as permissões necessárias, você pode usar o explorador de ameaças (também chamado de Gerenciador) para identificar e analisar ameaças. (Para usar o Explorer, no centro &amp; de conformidade de segurança, vá para **Gerenciador**de **Gerenciamento** \> de ameaças.)

![Vá para o Gerenciador \> de gerenciamento de ameaças](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)

O Explorer é uma ferramenta poderosa, quase em tempo real, para ajudar as equipes de operações de segurança a investigar e &amp; responder a ameaças no centro de conformidade de segurança. Veja algumas coisas que você pode fazer:
- [Consulte malware detectado pelos recursos de segurança do Office 365](#see-malware-detected-in-email-by-technology)
- [Exibir dados sobre URLs de phishing e clicar em veredicto](#view-data-about-phishing-urls-and-click-verdict)
- [Iniciar um processo de investigação e resposta automatizado de um modo de exibição no Explorer](#start-automated-investigation-and-response)
- ... [e muito mais](#more-ways-to-use-explorer)!

## <a name="see-malware-detected-in-email-by-technology"></a>Confira malware detectado em email por tecnologia

Suponha que você queira ver o malware detectado no email e por qual tecnologia no Office 365. Para fazer isso, use o [email _GT_ malware](threat-explorer-views.md#email--malware) View do Explorer.

1. No centro de conformidade do & de[https://protection.office.com](https://protection.office.com)segurança (), escolha**Gerenciador**de **Gerenciamento** > de ameaças.
2. No menu **Exibir** , escolha**malware**de **email** > .<br/>![Menu Exibir para Explorer](media/ExplorerViewEmailMalwareMenu.png)<br/>
3. Clique em **remetente**e escolha**tecnologia de detecção** **básica** > .<br/>Agora, suas tecnologias de detecção estão disponíveis como filtros para o relatório.<br/>![Tecnologias de detecção de malware](media/ExplorerEmailMalwareDetectionTech.png)<br/> 
4. Selecione uma opção e, em seguida, clique no botão atualizar para aplicar esse filtro.<br/>![Tecnologia de detecção selecionada](media/ExplorerEmailMalwareDetectionTechATP.png)<br/> 

O relatório é atualizado para mostrar o malware de resultados detectado no email, usando a opção de tecnologia que você selecionou. A partir daqui, você pode realizar uma análise adicional.

## <a name="view-data-about-phishing-urls-and-click-verdict"></a>Exibir dados sobre URLs de phishing e clicar em veredicto

Suponha que você queira ver as tentativas de phishing por meio de URLs no email, incluindo uma lista de URLs que foram permitidas, bloqueadas e substituídas.  A identificação de URLs que foram clicadas requer [links seguros de ATP](atp-safe-links.md). (Verifique se você configurou e aplicou [as políticas de links seguros de ATP](set-up-atp-safe-links-policies.md) aos seus usuários para proteção de clique em tempo e log de clique em verdicts por links seguros de ATP.) Para examinar as URLs de phishing em mensagens e clicar em URLs nas mensagens de phishing, use o [email _GT_ Phish](threat-explorer-views.md#email--phish) View do Explorer.

1. No centro de conformidade do & de[https://protection.office.com](https://protection.office.com)segurança (), escolha**Gerenciador**de **Gerenciamento** > de ameaças.
2. No menu **Exibir** , escolha**phishing**de **email** > .<br/>![Menu Exibir para Explorer](media/ExplorerViewEmailPhishMenu.png)<br/>
3. Clique em **remetente**e, em seguida, escolha **URLs** > **clique em veredicto**.
4. Selecione uma ou mais opções, como **bloqueado** e o **bloco substituído**, e clique no botão **Atualizar** para aplicar esse filtro.<br/>![URLs e clique em verdicts](media/ThreatExplorerEmailPhishClickVerdictOptions.png)<br/>

O relatório é atualizado para mostrar duas tabelas de URL diferentes na guia URL abaixo:
1. As **principais URLs** são as URLs contidas nas mensagens que foram filtradas para baixo e a ação de entrega de emails conta para cada URL. No modo de exibição email de phishing, essa lista normalmente conterá URLs legítimas. Os invasores incluem uma mistura de URLs boas e ruins nas mensagens para tentar obtê-las, mas eles tornarão os links mal-intencionados mais interessantes para o usuário clicar. A tabela de URLs é classificada pela contagem total de emails (Observação: esta coluna não é mostrada para simplificar o modo de exibição).
2. Os **principais cliques** são as URLs encapsuladas de links seguros que foram clicados, classificados por contagem de clique total (essa coluna também não é exibida para simplificar o modo de exibição). Total de contagens por coluna indicam os links seguros clique em contagem de veredicto para cada URL clicada. No modo de exibição email de phishing, esses links serão freqüentemente suspeitos ou mal-intencionados, mas podem incluir URLs limpas que estão em mensagens de phishing. Os cliques de URL em links não ajustados não aparecerão aqui.

As duas tabelas URLs mostram as principais URLs nos emails de phishing por status de entrega e mostram cliques de URL que foram bloqueados (ou visitados apesar de um aviso) para que você possa entender quais links defeituosos possíveis foram recebidos por usuários e interagem com os usuários. A partir daqui, você pode realizar uma análise adicional. Por exemplo, abaixo do gráfico, você pode ver as principais URLs nos emails que foram bloqueados no ambiente da sua organização. 

![URLs do Explorer que foram bloqueadas](media/ExplorerPhishClickVerdictURLs.png) 

Selecione uma URL para exibir informações mais detalhadas. Observe que, na caixa de diálogo de submenu URL, a filtragem de emails é removida para mostrar a exibição completa da exposição da URL em seu ambiente. Isso permite que você filtre emails no Explorer para os quais você está preocupado, encontre URLs específicas que são ameaças potenciais e, em seguida, expanda a compreensão da exposição de URL no seu ambiente (por meio da caixa de diálogo detalhes da URL) sem ter que adicionar filtros de URL ao Visualização do Explorer.

## <a name="review-email-messages-reported-by-users"></a>Analisar mensagens de email relatadas por usuários

Suponha que você queira ver as mensagens de email que os usuários em sua organização relataram como lixo eletrônico, não lixo eletrônico ou phishing usando o [suplemento de mensagem de relatório para o Outlook e o Outlook na Web](enable-the-report-message-add-in.md). Para fazer isso, use a exibição de [email > relatada pelo usuário](threat-explorer-views.md#email--user-reported) do Explorer.

1. No centro de conformidade do & de[https://protection.office.com](https://protection.office.com)segurança (), escolha**Gerenciador**de **Gerenciamento** > de ameaças.
2. No menu **Exibir** , escolha **email** > **reportado pelo usuário**.<br/>![Menu Exibir para Explorer](media/ExplorerViewMenuEmailUserReported.png)<br/>
3. Clique em **remetente**e, em seguida, escolha**tipo de relatório** **básico** > .
4. Selecione uma opção, como **Phish**, e clique no botão **Atualizar** . <br/>![Phishing relatado pelo usuário](media/EmailUserReportedReportType.png)<br/> 

O relatório é atualizado para mostrar dados sobre mensagens de email que as pessoas em sua organização relataram como uma tentativa de phishing. Você pode usar essas informações para realizar mais análises e, se necessário, ajustar as [políticas de anti-phishing da ATP](set-up-anti-phishing-policies.md).

## <a name="start-automated-investigation-and-response"></a>Iniciar investigação e resposta automatizadas

(Novo!) A [investigação e a resposta automatizadas](automated-investigation-response-office.md), recentemente adicionadas ao plano ATP 2, podem poupar sua equipe de operações de segurança muito tempo e esforço na investigação e redução de ataques de Cyber. Além de configurar alertas que podem acionar um guia de segurança, você pode iniciar um processo de investigação e resposta automatizado de um modo de exibição no Explorer. 

Para obter detalhes sobre isso, consulte [example: um administrador de segurança dispara uma investigação do explorador de ameaças](automated-investigation-response-office.md#example-a-security-administrator-triggers-an-investigation-from-threat-explorer).

## <a name="more-ways-to-use-explorer"></a>Outras maneiras de usar o Explorer

Além dos cenários descritos neste artigo, você tem muito mais opções de relatórios disponíveis no Explorer. 
- [Localizar e investigar email malicioso que foi entregue](investigate-malicious-email-that-was-delivered.md)
- [Exibir arquivos mal-intencionados detectados no SharePoint Online, no OneDrive e no Microsoft Teams](malicious-files-detected-in-spo-odb-or-teams.md)
- [Obter uma visão geral dos modos de exibição no explorador de ameaças](threat-explorer-views.md)

## <a name="required-licenses-and-permissions"></a>Licenças e permissões necessárias

O Explorer está incluído no [Office 365 Advanced Threat Protection Plan 2](office-365-ti.md). 

Para exibir e usar o Explorer, você deve ter as permissões apropriadas, como aquelas concedidas a um administrador de segurança ou leitor de segurança. 

- Para o centro &amp; de conformidade de segurança, você deve ter uma das seguintes funções atribuídas:
    - Gerenciamento de Organização
    - Administrador de segurança (pode ser atribuído no centro[https://aad.portal.azure.com](https://aad.portal.azure.com)de administração do Azure Active Directory)
    - Leitor de segurança

- Para o Exchange Online, você deve ter uma das seguintes funções atribuídas no centro de administração do Exchange[https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)() ou com cmdlets do PowerShell (Confira [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)):
    - Gerenciamento de Organização
    - Gerenciamento de Organização Somente para Exibição
    - Função de Destinatários Somente para Exibição
    - Gerenciamento de Conformidade

Para saber mais sobre funções e permissões, confira os seguintes recursos:

- [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md)

- [Permissões de recursos no Exchange Online](https://docs.microsoft.com/exchange/permissions-exo/feature-permissions)
  

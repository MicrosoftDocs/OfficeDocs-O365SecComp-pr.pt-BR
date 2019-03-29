---
title: Usar o explorador de ameaças no &amp; centro de conformidade de segurança
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/28/2019
ms.audience: ITPro
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
ms.openlocfilehash: e6177970edc67c8b9e1c0ae6144f4c37f116012f
ms.sourcegitcommit: 787a0fef671e5dc6f5e805b580321b2edbfad8e9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/29/2019
ms.locfileid: "30989606"
---
# <a name="use-threat-explorer-in-the-security-amp-compliance-center"></a>Usar o explorador de ameaças no &amp; centro de conformidade de segurança

Se sua organização tiver o [Office 365 Advanced Threat Protection Plan 2](office-365-ti.md) (ATP) e você tiver as permissões necessárias, você pode usar o explorador de ameaças (também chamado de Gerenciador) para identificar e analisar ameaças. (Para usar o Explorer, no centro &amp; de conformidade de segurança, vá para **Gerenciador**de **Gerenciamento** \> de ameaças.)

![Vá para o Gerenciador \> de gerenciamento de ameaças](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)

O Explorer é uma ferramenta poderosa, quase em tempo real, para ajudar as equipes de operações de segurança a investigar e &amp; responder a ameaças no centro de conformidade de segurança. Veja algumas coisas que você pode fazer:
- [Consulte malware detectado pelos recursos de segurança do Office 365](#see-malware-detected-in-email-by-technology)
- [Exibir dados sobre URLs de phishing e clicar em veredicto](#view-data-about-phishing-urls-and-click-verdict)
- [Iniciar um processo de investigação e resposta automatizado de um modo de exibição no Explorer](#start-automated-investigation-and-response)
- ... [e muito mais](#more-ways-to-use-explorer)!

## <a name="see-malware-detected-in-email-by-technology"></a>ConFira malware detectado em email por tecnologia

Suponha que você queira ver o malware detectado no email e por qual tecnologia no Office 365. Para fazer isso, use o [email _GT_ malware](threat-explorer-views.md#email--malware) View do Explorer.

1. No centro de conformidade do & de[https://protection.office.com](https://protection.office.com)segurança (), escolha**Gerenciador**de **Gerenciamento** > de ameaças.
2. No menu **Exibir** , escolha**malware**de **email** > .<br/>![Menu Exibir para Explorer](media/ExplorerViewEmailMalwareMenu.png)<br/>
3. Clique em **remetente**e escolha**tecnologia de detecção** **básica** > .<br/>Agora, suas tecnologias de detecção estão disponíveis como filtros para o relatório.<br/>![Tecnologias de detecção de malware](media/ExplorerEmailMalwareDetectionTech.png)<br/> 
4. Selecione uma opção e, em seguida, clique no botão atualizar para aplicar esse filtro.<br/>![Tecnologia de detecção selecionada](media/ExplorerEmailMalwareDetectionTechATP.png)<br/> 

O relatório é atualizado para mostrar o malware de resultados detectado no email, usando a opção de tecnologia que você selecionou. A partir daqui, você pode realizar uma análise adicional.

## <a name="view-data-about-phishing-urls-and-click-verdict"></a>Exibir dados sobre URLs de phishing e clicar em veredicto

Suponha que você queira ver as tentativas de phishing por meio de URLs no email, incluindo uma lista de URLs que foram permitidas, bloqueadas e substituídas. Para fazer isso, use o [E-mail _GT_ Phish](threat-explorer-views.md#email--phish) View do Explorer.

1. No centro de conformidade do & de[https://protection.office.com](https://protection.office.com)segurança (), escolha**Gerenciador**de **Gerenciamento** > de ameaças.
2. No menu **Exibir** , escolha**phishing**de **email** > .<br/>![Menu Exibir para Explorer](media/ExplorerViewEmailPhishMenu.png)<br/>
3. Clique em **remetente**e, em seguida, escolha **URLs** > **clique em veredicto**.
4. Selecione uma ou mais opções, como **bloqueado** e o **bloco substituído**, e clique no botão **Atualizar** para aplicar esse filtro.<br/>![URLs e clique em verdicts](media/ThreatExplorerEmailPhishClickVerdictOptions.png)<br/>

O relatório é atualizado para mostrar URLs de phishing detectadas em emails que foram bloqueados (ou visitados apesar de um aviso), junto com o status de entrega de email. A partir daqui, você pode realizar uma análise adicional. Por exemplo, abaixo do gráfico, você pode ver as principais URLs que foram bloqueadas no email da sua organização. 

![URLs do Explorer que foram bloqueadas](media/ExplorerPhishClickVerdictURLs.png) 

Selecione uma URL para exibir informações mais detalhadas.

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
- [Encontre e investigue emails mal-intencionados que foram entregues](investigate-malicious-email-that-was-delivered.md)
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
  

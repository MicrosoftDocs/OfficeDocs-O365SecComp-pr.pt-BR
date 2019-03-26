---
title: Usar o explorador de ameaças no &amp; centro de conformidade de segurança
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/21/2019
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
ms.openlocfilehash: 202898873bb9611c747aed335d295c749c7cd0fa
ms.sourcegitcommit: a56128c7be5d59e976851c27301031e19fa1997d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/21/2019
ms.locfileid: "30732254"
---
# <a name="use-threat-explorer-in-the-security-amp-compliance-center"></a>Usar o explorador de ameaças no &amp; centro de conformidade de segurança

Se sua organização tiver o [plano de proteção avançada contra ameaças do Office 365](office-365-ti.md)e tiver as permissões necessárias, você poderá usar o Gerenciador de ameaças para identificar e analisar ameaças. Por exemplo, você pode identificar e excluir emails mal-intencionados que foram entregues ou confira o malware que foi detectado pelos recursos de segurança do Office 365. O Gerenciador de ameaças (também mencionado como Explorer) é uma poderosa ferramenta quase em tempo real para ajudar as equipes de operações de segurança a investigar e responder &amp; a ameaças no centro de conformidade de segurança.
  
![Vá para o Gerenciador \> de gerenciamento de ameaças](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)
  
Para usar o Explorer, no centro &amp; de conformidade de segurança, vá para **Gerenciador**de **Gerenciamento** \> de ameaças.

> [!IMPORTANT]
> O Office 365 Threat Intelligence é agora o Office 365 Advanced Threat Protection Plan 2, juntamente com outros recursos de proteção contra ameaças. Para saber mais, veja [planos e preços avançados de proteção contra ameaças do office 365](https://products.office.com/exchange/advance-threat-protection) e a [Descrição do serviço de proteção avançada contra ameaças do Office 365](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).
      
## <a name="explorer-overview"></a>Visão geral do Explorer

Se sua organização tiver [recursos de investigação e resposta contra ameaças do Office 365](office-365-ti.md) (isso é incluído no plano ATP 2) e você tiver as permissões necessárias, poderá usar o explorador de ameaças (também chamado de Gerenciador) para identificar e analisar ameaças. (No centro de &amp; conformidade de segurança, vá para **Gerenciador**de **Gerenciamento** \> de ameaças.)

![Vá para o Gerenciador \> de gerenciamento de ameaças](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)

Este artigo descreve algumas coisas que você pode fazer com o Explorer (há muito mais possibilidades):

- [Veja quais tipos de malware foram detectados no email](#see-malware-detected-in-email-by-technology)e por tecnologia de proteção contra ameaças (proteção contra malware, anexos seguros de ATP etc.)

- [Exibir dados sobre links de phishing (URLs)](#view-data-about-phishing-urls-and-click-verdict)e o que o verdicts de clique (URLs bloqueados, permitidos ou visitados apesar de avisos)

- [Revise mensagens de email relatadas como lixo eletrônico, não lixo eletrônico ou phishing](#review-email-messages-reported-by-users)e identifique as tendências (como um número maior do que o normal de mensagens relatadas como phishing) 

## <a name="see-malware-detected-in-email-by-technology"></a>ConFira malware detectado em email por tecnologia

Suponha que você queira ver o malware detectado no email e por qual tecnologia no Office 365. Para fazer isso, use o [email _GT_ malware](threat-explorer-views.md#email--malware) View do Explorer.

1. no centro de conformidade do & de segurança do[https://protection.office.com](https://protection.office.com)Office 365 (), escolha**gerenciador**de **gerenciamento** > de ameaças.
2. No menu **Exibir** , escolha**malware**de **email** > .<br/>![Menu Exibir para Explorer](media/ExplorerViewEmailMalwareMenu.png)<br/>
3. Clique em **remetente**e escolha**tecnologia de detecção** **básica** > .<br/>Agora, suas tecnologias de detecção estão disponíveis como filtros para o relatório.<br/>![Tecnologias de detecção de malware](media/ExplorerEmailMalwareDetectionTech.png)<br/> 
4. Selecione uma opção e, em seguida, clique no botão atualizar para aplicar esse filtro.<br/>![Tecnologia de detecção selecionada](media/ExplorerEmailMalwareDetectionTechATP.png)<br/> 

O relatório é atualizado para mostrar o malware de resultados detectado no email, usando a opção de tecnologia que você selecionou. A partir daqui, você pode realizar uma análise adicional.

## <a name="view-data-about-phishing-urls-and-click-verdict"></a>Exibir dados sobre URLs de phishing e clicar em veredicto

Suponha que você queira ver as tentativas de phishing por meio de URLs no email, incluindo uma lista de URLs que foram permitidas, bloqueadas e substituídas. Para fazer isso, use o [E-mail _GT_ Phish](threat-explorer-views.md#email--phish) View do Explorer.

1. no centro de conformidade do & de segurança do[https://protection.office.com](https://protection.office.com)Office 365 (), escolha**gerenciador**de **gerenciamento** > de ameaças.
2. No menu **Exibir** , escolha**phishing**de **email** > .<br/>![Menu Exibir para Explorer](media/ExplorerViewEmailPhishMenu.png)<br/>
3. Clique em **remetente**e, em seguida, escolha **URLs** > **clique em veredicto**.
4. Selecione uma ou mais opções, como **bloqueado** e o **bloco substituído**, e clique no botão **Atualizar** para aplicar esse filtro.<br/>![URLs e clique em verdicts](media/ThreatExplorerEmailPhishClickVerdictOptions.png)<br/>

O relatório é atualizado para mostrar URLs de phishing detectadas em emails que foram bloqueados (ou visitados apesar de um aviso), junto com o status de entrega de email. A partir daqui, você pode realizar uma análise adicional. Por exemplo, abaixo do gráfico, você pode ver as principais URLs que foram bloqueadas no email da sua organização. 

![URLs do Explorer que foram bloqueadas](media/ExplorerPhishClickVerdictURLs.png) 

Selecione uma URL para exibir informações mais detalhadas.

## <a name="review-email-messages-reported-by-users"></a>Analisar mensagens de email relatadas por usuários

Suponha que você queira ver as mensagens de email que os usuários em sua organização relataram como lixo eletrônico, não lixo eletrônico ou phishing usando o [suplemento de mensagem de relatório para o Outlook e o Outlook na Web](enable-the-report-message-add-in.md). Para fazer isso, use a exibição de [email > relatada pelo usuário](threat-explorer-views.md#email--user-reported) do Explorer.

1. no centro de conformidade do & de segurança do[https://protection.office.com](https://protection.office.com)Office 365 (), escolha**gerenciador**de **gerenciamento** > de ameaças.
2. No menu **Exibir** , escolha **email** > **reportado pelo usuário**.<br/>![Menu Exibir para Explorer](media/ExplorerViewMenuEmailUserReported.png)<br/>
3. Clique em **remetente**e, em seguida, escolha**tipo de relatório** **básico** > .
4. Selecione uma opção, como **Phish**, e clique no botão **Atualizar** . <br/>![Phishing relatado pelo usuário](media/EmailUserReportedReportType.png)<br/> 

O relatório é atualizado para mostrar dados sobre mensagens de email que as pessoas em sua organização relataram como uma tentativa de phishing. Você pode usar essas informações para realizar mais análises e, se necessário, ajustar as [políticas de anti-phishing da ATP](set-up-anti-phishing-policies.md).

## <a name="theres-more"></a>Há mais!

Além dos três cenários descritos neste artigo, você tem vários cenários de relatórios disponíveis no Explorer. Aqui estão alguns exemplos:

- [Encontre e investigue emails mal-intencionados que foram entregues](investigate-malicious-email-that-was-delivered.md)

- [Exibir arquivos mal-intencionados detectados no SharePoint Online, no OneDrive e no Microsoft Teams](malicious-files-detected-in-spo-odb-or-teams.md)

- [Obter uma visão geral dos modos de exibição no explorador de ameaças](threat-explorer-views.md)

## <a name="how-to-get-explorer"></a>Como obter o Explorer

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

Para saber mais, confira os seguintes recursos:

- [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md)

- [Permissões de recursos no Exchange Online](https://docs.microsoft.com/exchange/permissions-exo/feature-permissions)
  
## <a name="related-topics"></a>Tópicos relacionados

- [Investigação e resposta automatizadas (AIR)](automated-investigation-response-office.md)

- [Modos de exibição do Gerenciador de ameaças](threat-explorer-views.md)

- [Exibir relatórios para a proteção avançada contra ameaças do Office 365](view-reports-for-atp.md)

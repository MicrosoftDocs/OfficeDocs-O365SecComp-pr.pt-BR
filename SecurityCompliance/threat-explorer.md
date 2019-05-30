---
title: Explorador de ameaças (e detecções em tempo real)
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 05/22/2019
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
description: Saiba mais sobre o Explorer (e as detecções em tempo real) no &amp; centro de conformidade de segurança.
ms.openlocfilehash: 030f866c5e86daa3dc543bddae7152e19f377d3b
ms.sourcegitcommit: 6c0fcb82178a4ac26375545f328389a6852a81be
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/28/2019
ms.locfileid: "34490527"
---
# <a name="threat-explorer-and-real-time-detections"></a>Explorador de ameaças (e detecções em tempo real)

Se sua organização tem a [proteção avançada contra ameaças do office 365](office-365-atp.md) (Office 365 ATP) e você tem as [permissões necessárias](#required-licenses-and-permissions), você tem as detecções do **Explorer** ou do **tempo real** (anteriormente conhecida como *relatórios em tempo real* , [consulte o que há de novo](#new-features-in-real-time-detections)!). No centro de conformidade do & de segurança, vá para **Gerenciamento de ameaças**e escolha as detecções do **Explorer** ou **em tempo real**. 

|Com o plano ATP 2, você vê:  |Com o plano ATP 1, você vê:  |
|---------|---------|
|![Explorador de ameaças](media/threatmgmt-explorer.png)      |![Detecções em tempo real](media/threatmgmt-realtimedetections.png)         |

Com o Explorer (ou detecções em tempo real), você tem um relatório poderoso que permite que sua equipe de operações de segurança investigue e responda às ameaças de forma eficaz e eficiente e se assemelha à imagem a seguir: 

![Vá para o Gerenciador \> de gerenciamento de ameaças](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)

Com esse relatório, você pode:
- [Consulte malware detectado pelos recursos de segurança do Office 365](#see-malware-detected-in-email-by-technology)
- [Exibir dados sobre URLs de phishing e clicar em veredicto](#view-data-about-phishing-urls-and-click-verdict)
- [Iniciar um processo de investigação e resposta automatizado de um modo de exibição no Explorer](#start-automated-investigation-and-response) (Somente plano ATP 2)
- ... [Investigue emails mal-intencionados e muito mais](#more-ways-to-use-explorer-or-real-time-detections)!

## <a name="new-features-in-real-time-detections"></a>Novos recursos em detecções em tempo real

Para clientes do Office 365 ATP Plan 1, o relatório de *detecções em tempo real* era conhecido anteriormente como *relatórios em tempo real*. Além da alteração do nome, vários novos recursos e aprimoramentos estão sendo lançados:

- No modo de exibição phishing, você pode ver mais detalhes sobre URLs detectadas por meio de [links seguros de ATP](atp-safe-links.md). Os novos detalhes e recursos incluem:
  - URLs em mensagens de email
  - Filtragem com base nas informações de URL
  - Informações de URL exibidas em gráficos de dados
  - Dados de tempo de clique sobre cliques em mensagens

- Sempre que houver uma alteração em uma URL, clique em veredicto, você verá um alerta. URL clique em verdicts pode mudar quando a reputação de uma URL muda de post-acionamento ou quando um usuário protegido por links seguros de ATP substitui um [aviso de links seguros de ATP](atp-safe-links-warning-pages.md).  
 
Esses aprimoramentos permitem que os administradores de segurança da sua organização vejam mais detalhes do que antes. Os administradores de segurança podem exibir informações sobre domínios de URL, URLs perdidas, clicar em verdicts e mais e ajustar as políticas de ATP do Office 365 apropriadamente.

> [!NOTE]
> Embora esses recursos estejam em visualização, os dados de URL estarão disponíveis por um número limitado de dias. 

## <a name="see-malware-detected-in-email-by-technology"></a>Confira malware detectado em email por tecnologia

Suponha que você queira ver o malware detectado no email, pela tecnologia do Office 365. Para fazer isso, use a exibição de [email _GT_ malware](threat-explorer-views.md#email--malware) do Explorer (ou detecções em tempo real).

1. No centro de conformidade do & de[https://protection.office.com](https://protection.office.com)segurança (), escolha**Gerenciador** de **Gerenciamento** > de ameaças (ou **detecções em tempo real**). (Este exemplo usa o Explorer.)

2. No menu **Exibir** , escolha**malware**de **email** > .<br/>![Menu Exibir para Explorer](media/ExplorerViewEmailMalwareMenu.png)<br/>

3. Clique em **remetente**e escolha**tecnologia de detecção** **básica** > .<br/>Agora, suas tecnologias de detecção estão disponíveis como filtros para o relatório.<br/>![Tecnologias de detecção de malware](media/ExplorerEmailMalwareDetectionTech.png)<br/> 

4. Selecione uma opção e, em seguida, clique no botão **Atualizar** para aplicar esse filtro.<br/>![Tecnologia de detecção selecionada](media/ExplorerEmailMalwareDetectionTechATP.png)<br/> 

O relatório é atualizado para mostrar o malware de resultados detectado no email, usando a opção de tecnologia que você selecionou. A partir daqui, você pode realizar uma análise adicional.

## <a name="view-data-about-phishing-urls-and-click-verdict"></a>Exibir dados sobre URLs de phishing e clicar em veredicto

Suponha que você queira ver as tentativas de phishing por meio de URLs no email, incluindo uma lista de URLs que foram permitidas, bloqueadas e substituídas. A identificação de URLs que foram clicadas requer que os [links seguros de ATP](atp-safe-links.md) sejam configurados. Verifique se você configurou [as políticas de links seguros de ATP](set-up-atp-safe-links-policies.md) para proteção de tempo de clique e log de clique em verdicts por links seguros de ATP. 

Para examinar as URLs de phishing em mensagens e clicar em URLs nas mensagens de phishing, use o [email _GT_ Phish](threat-explorer-views.md#email--phish) View of Explorer (ou detecções em tempo real).

1. No centro de conformidade do & de[https://protection.office.com](https://protection.office.com)segurança (), escolha**Gerenciador** de **Gerenciamento** > de ameaças (ou **detecções em tempo real**). (Este exemplo usa o Explorer.)

2. No menu **Exibir** , escolha**phishing**de **email** > .<br/>![Menu Exibir para Explorer](media/ExplorerViewEmailPhishMenu.png)<br/>

3. Clique em **remetente**e, em seguida, escolha **URLs** > **clique em veredicto**.

4. Selecione uma ou mais opções, como **bloqueado** e **substituído**e, em seguida, clique no botão **Atualizar** que está na mesma linha que as opções para aplicar esse filtro. (Não atualize a janela do navegador.)<br/>![URLs e clique em verdicts](media/ThreatExplorerEmailPhishClickVerdictOptions.png)<br/>

    O relatório é atualizado para mostrar duas tabelas de URL diferentes na guia URL no relatório:

   1. As **principais URLs** são as URLs contidas nas mensagens que foram filtradas para baixo e a ação de entrega de emails conta para cada URL. No modo de exibição email de phishing, essa lista normalmente conterá URLs legítimas. Os invasores incluem uma mistura de URLs boas e ruins nas mensagens para tentar obtê-las, mas eles farão com que os links mal-intencionados sejam mais interessantes para o usuário clicar. A tabela de URLs é classificada pela contagem total de emails (Observação: esta coluna não é mostrada para simplificar o modo de exibição).

   2. Os **principais cliques** são as URLs encapsuladas de links seguros que foram clicados, classificados por contagem de clique total (essa coluna também não é exibida para simplificar o modo de exibição). Total de contagens por coluna indicam os links seguros clique em contagem de veredicto para cada URL clicada. No modo de exibição email de phishing, eles são URLs suspeitas ou maliciosas mais frequentes, mas podem incluir URLs limpas que estão nas mensagens de phishing. Os cliques de URL em links não ajustados não aparecerão aqui.
   
   As duas tabelas URLs mostram as principais URLs nos emails de phishing por ação de entrega e local, e mostram cliques de URL que foram bloqueados (ou visitados apesar de um aviso) para que você possa entender quais links defeituosos potenciais foram recebidos por usuários e interagem com os usuários. A partir daqui, você pode realizar uma análise adicional. Por exemplo, abaixo do gráfico, você pode ver as principais URLs nos emails que foram bloqueados no ambiente da sua organização.
   
   ![URLs do Explorer que foram bloqueadas](media/ExplorerPhishClickVerdictURLs.png)
   
   Selecione uma URL para exibir informações mais detalhadas. Observe que, na caixa de diálogo de submenu URL, a filtragem de emails é removida para mostrar a exibição completa da exposição da URL em seu ambiente. Isso permite que você filtre emails no Explorer para os quais você está preocupado, encontre URLs específicas que são ameaças potenciais e, em seguida, expanda a compreensão da exposição de URL no seu ambiente (por meio da caixa de diálogo detalhes da URL) sem ter que adicionar filtros de URL ao Visualização do Explorer.

## <a name="review-email-messages-reported-by-users"></a>Analisar mensagens de email relatadas por usuários

Suponha que você queira ver as mensagens de email que os usuários em sua organização relataram como lixo eletrônico, não lixo eletrônico ou phishing usando o [suplemento de mensagem de relatório para Outlook e Outlook na Web](enable-the-report-message-add-in.md). Para fazer isso, use a exibição de [email > relatada pelo usuário](threat-explorer-views.md#email--user-reported) do Explorer (ou detecções em tempo real).

1. No centro de conformidade do & de[https://protection.office.com](https://protection.office.com)segurança (), escolha**Gerenciador** de **Gerenciamento** > de ameaças (ou **detecções em tempo real**). (Este exemplo usa o Explorer.)

2. No menu **Exibir** , escolha **email** > **reportado pelo usuário**.<br/>![Menu Exibir para Explorer](media/ExplorerViewMenuEmailUserReported.png)<br/>

3. Clique em **remetente**e, em seguida, escolha**tipo de relatório** **básico** > .

4. Selecione uma opção, como **Phish**, e clique no botão **Atualizar** . <br/>![Phishing relatado pelo usuário](media/EmailUserReportedReportType.png)<br/> 

O relatório é atualizado para mostrar dados sobre mensagens de email que as pessoas em sua organização relataram como uma tentativa de phishing. Você pode usar essas informações para realizar mais análises e, se necessário, ajustar as [políticas de anti-phishing da ATP](set-up-anti-phishing-policies.md).

## <a name="start-automated-investigation-and-response"></a>Iniciar investigação e resposta automatizadas

> [!NOTE]
> Os recursos de investigação e resposta automatizados estão disponíveis no **office 365 ATP Plan 2** e no **Office 365 E5**.

(Novo!) A [investigação e a resposta automatizadas](automated-investigation-response-office.md) podem salvar sua equipe de operações de segurança muito tempo e esforço na investigação e redução de ataques de cyberismo. Além de configurar alertas que podem acionar um guia de segurança, você pode iniciar um processo de investigação e resposta automatizado de um modo de exibição no Explorer. 

Para obter detalhes sobre isso, consulte [example: um administrador de segurança dispara uma investigação do Explorer](automated-investigation-response-office.md#example-a-security-administrator-triggers-an-investigation-from-threat-explorer).

## <a name="more-ways-to-use-explorer-or-real-time-detections"></a>Outras maneiras de usar o Explorer (ou detecções em tempo real)

Além dos cenários descritos neste artigo, você tem muito mais opções de relatórios disponíveis com o Explorer (ou detecções em tempo real). 
- [Localizar e investigar email malicioso que foi entregue](investigate-malicious-email-that-was-delivered.md)
- [Exibir arquivos mal-intencionados detectados no SharePoint Online, no OneDrive e no Microsoft Teams](malicious-files-detected-in-spo-odb-or-teams.md)
- [Obter uma visão geral dos modos de exibição no explorador de ameaças (e detecções em tempo real)](threat-explorer-views.md)

## <a name="required-licenses-and-permissions"></a>Licenças e permissões necessárias

Você deve ter o [Office 365 ATP](office-365-atp.md) para obter as detecções do Explorer ou em tempo real.
- O Explorer está incluído no plano 2 do Office 365 ATP. 
- O relatório de detecções em tempo real está incluído no plano 1 de ATP do Office 365.

Para exibir e usar as detecções do Explorer ou em tempo real, você deve ter as permissões apropriadas, como aquelas concedidas a um administrador de segurança ou leitor de segurança. 

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
  

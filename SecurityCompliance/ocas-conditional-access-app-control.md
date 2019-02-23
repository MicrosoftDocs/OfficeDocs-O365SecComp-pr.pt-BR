---
title: Proteger aplicativos com o Office 365 Cloud app Security controle de aplicativo de acesso condicional
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.reviewer: alesibov
ms.audience: Admin
ms.topic: reference
ms.date: 02/14/2019
ms.service: O365-seccomp
localization_priority: Normal
description: Parar violações e vazamentos em tempo real com o controle de aplicativo de acesso condicional do Office 365 Cloud app Security.
ms.openlocfilehash: 23c4b29e86eb8ba92cfa8a544d6484965ec6372b
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217081"
---
# <a name="protect-apps-with-office-365-cloud-app-security-conditional-access-app-control"></a>Proteger aplicativos com o Office 365 Cloud app Security controle de aplicativo de acesso condicional

|Avaliação * *\>**|Planejamento * *\>**|Implantação * *\>**|Utilização * * *|
|:-----|:-----|:-----|:-----|
|[Iniciar avaliação](office-365-cas-overview.md) <br/> |[Iniciar planejamento](get-ready-for-office-365-cas.md) <br/> |Você está aqui!  <br/> [Próxima etapa](ocas-deploy-conditional-access-app-control.md) <br/> |[Começar a usar](utilization-activities-for-ocas.md) <br/> |

No local de trabalho atual, geralmente não é suficiente saber o que está acontecendo no seu ambiente de nuvem após o fato. Você deseja interromper violações e vazamentos em tempo real, antes que os funcionários coloquem de forma intencional ou inadvertida seus dados e sua organização em risco. É importante permitir que os usuários em sua organização tornem a maior parte dos serviços e ferramentas disponíveis para eles em aplicativos de nuvem e permitam que eles coloquem seus próprios dispositivos para trabalhar. Ao mesmo tempo, você precisa de ferramentas para ajudar a proteger sua organização contra vazamentos de dados e roubo de dados, em tempo real. Junto com o Azure Active Directory, o Office 365 Cloud app Security fornece esses recursos em uma experiência holística e integrada com controle de aplicativo de acesso condicional.

> [!IMPORTANT]
> para usar o controle de aplicativo de acesso condicional do cloud App Security, você precisa de uma  [licença do Azure Active Directory P1](https://azure.microsoft.com/pricing/details/active-directory/)e uma assinatura ativa [do Office 365 Cloud App Security](office-365-cas-overview.md) .

## <a name="how-it-works"></a>Como funciona

O controle de aplicativo Conditional Access usa uma arquitetura de proxy reversa e é exclusivamente integrado ao acesso condicional do Azure AD. O acesso condicional do Azure AD permite que você aplique controles de acesso nos aplicativos da sua organização com base em determinadas condições. As condições definem *quem* (usuário ou grupo de usuários) e *o que* (quais aplicativos de nuvem) e *onde* (quais locais e redes) uma política de acesso condicional é aplicada. Depois de determinar as condições, você pode encaminhar usuários para o Office 365 Cloud app Security onde você pode proteger dados com o controle de aplicativo de acesso condicional aplicando controles de acesso e sessão.

O controle de aplicativos de acesso condicional permite que as sessões e o acesso de aplicativos do usuário sejam monitorados e controlados em tempo real com base nas políticas de acesso e de sessão. As políticas de acesso e de sessão são usadas no portal do Cloud app Security para refinar os filtros e definir ações a serem tomadas em um usuário. Com as políticas de acesso e de sessão, você pode:

- **Bloquear ao baixar**: você pode bloquear o download de documentos confidenciais. Por exemplo, em dispositivos não gerenciados.

- **Proteger ao baixar**: em vez de bloquear o download de documentos confidenciais, você pode exigir que os documentos sejam protegidos por meio da criptografia no download. Essa criptografia garante que o documento esteja protegido e o acesso do usuário seja autenticado se os dados forem baixados para um dispositivo não confiável.

- **Monitorar sessões de usuário de baixa confiança**: os usuários arriscados são monitorados quando entram em aplicativos e suas ações são registradas de dentro da sessão. Você pode investigar e analisar o comportamento do usuário para entender onde e em que condições as políticas de sessão devem ser aplicadas no futuro.

- **Bloquear o acesso**: você pode bloquear completamente o acesso a aplicativos específicos para usuários provenientes de dispositivos não gerenciados ou de redes não corporativas.

- **Criar modo somente leitura**: ao monitorar e bloquear atividades personalizadas no aplicativo, você pode criar um modo somente leitura para aplicativos específicos para usuários específicos.

- **Restringir sessões de usuário de redes não corporativas**: os usuários que acessam um aplicativo protegido de um local que não faz parte da sua rede corporativa têm permissão para acesso restrito. O download de materiais sensíveis é bloqueado ou protegido.

### <a name="how-session-control-works"></a>Como funciona o controle de sessão

A criação de uma política de sessão com controle de aplicativo de acesso condicional permite controlar as sessões de usuário redirecionando o usuário por meio de um proxy reverso, em vez de diretamente para o aplicativo. A partir de então, as solicitações e respostas do usuário passam pelo Office 365 Cloud app Security, em vez de diretamente para o aplicativo.

Para manter o usuário na sessão, todas as URLs relevantes, scripts Java e cookies dentro da sessão de aplicativo são substituídas pelas URLs do Office 365 Cloud app Security. Por exemplo, se o aplicativo retornar uma página com links cujos domínios terminam com myapp.com, o link será substituído por domínios terminados com algo como: myapp.com.us.cas.ms

Este método não exige que você instale nada no dispositivo. Este método é ideal ao monitorar sessões de dispositivos não gerenciados.

Depois que uma sessão é direcionada através do Office 365 Cloud app Security, as seguintes ações podem ser feitas:

1. Inspecionar o tráfego de atividades do usuário

2. Exibir as atividades identificadas no log de atividades do Office 365 Cloud app Security

3. Salvar os logs de tráfego e analisá-los

4. Habilitar o administrador para exportar os logs de tráfego

5. Impor políticas na sessão

## <a name="managed-device-identification"></a>Identificação do dispositivo gerenciado

O controle de aplicativos de acesso condicional permite que você crie políticas que levam em consideração se um dispositivo é ou não gerenciado. Para identificar se um dispositivo é ou não gerenciado, o recurso usa:

- Dispositivos em conformidade

- Dispositivos ingressados no domínio

- Implantação de certificados de cliente

### <a name="compliant-and-domain-joined-devices"></a>Dispositivos compatíveis e associados ao domínio

O acesso condicional do Azure AD permite que as informações de dispositivo compatíveis e de domínio sejam passadas diretamente para o Office 365 Cloud app Security. A partir daí, uma política de acesso ou uma política de sessão pode ser desenvolvida que usa o estado do dispositivo como um filtro. Para obter mais informações, consulte o [tópico introdução ao gerenciamento de dispositivos no Azure Active Directory](https://docs.microsoft.com/azure/active-directory/device-management-introduction).

### <a name="client-certificate-authenticated-devices"></a>Dispositivos autenticados pelo cliente-certificado

O mecanismo de identificação de dispositivo pode solicitar a autenticação de dispositivos relevantes usando certificados de cliente. Você pode usar certificados de cliente existentes já implantados em sua organização ou implantar novos certificados de cliente em dispositivos gerenciados. Você usa a presença desses certificados para definir políticas de acesso e de sessão. Para obter informações sobre como implantar certificados de cliente, consulte [Deploy Conditional Access app Control for Office 365 apps](ocas-deploy-conditional-access-app-control.md).

## <a name="supported-apps-and-clients"></a>Aplicativos e clientes com suporte

O controle de aplicativo Conditional Access para Office 365 suporta os seguintes aplicativos em destaque:

- Exchange Online (versão prévia)

- OneDrive for Business (visualização)

- Power BI (visualização)

- SharePoint Online (visualização)

- Microsoft Teams (visualização)

- Yammer (versão prévia)

Aplicativos adicionais estão sendo continuamente integrados ao controle de sessão.

## <a name="next-steps"></a>Próximas etapas

- [Implantar o controle de aplicativo do Access condicional para aplicativos do Office 365](ocas-deploy-conditional-access-app-control.md)

- [Saiba mais sobre as políticas de sessão no Office 365 Cloud app Security](ocas-session-policies.md)

- [Saiba mais sobre as políticas de acesso no Office 365 Cloud app Security](ocas-access-policies.md) 
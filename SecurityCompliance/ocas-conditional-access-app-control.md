---
title: Proteger aplicativos com o Office 365 Cloud app Security controle de aplicativo de acesso condicional
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.reviewer: alesibov
ms.audience: Admin
ms.topic: reference
ms.date: 02/14/2019
ms.service: o365-administration
localization_priority: Normal
description: Parar violações e vazamentos em tempo real com o controle de aplicativo de acesso condicional do Office 365 Cloud app Security.
ms.openlocfilehash: 8656bf9d3e028bf6b44731c397b74d9c883db707
ms.sourcegitcommit: 8679937354c1d8870ecd41519a59d2d7468c23c4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2019
ms.locfileid: "30103356"
---
# <a name="protect-apps-with-office-365-cloud-app-security-conditional-access-app-control"></a><span data-ttu-id="9c64c-103">Proteger aplicativos com o Office 365 Cloud app Security controle de aplicativo de acesso condicional</span><span class="sxs-lookup"><span data-stu-id="9c64c-103">Protect apps with Office 365 Cloud App Security Conditional Access App Control</span></span>

|<span data-ttu-id="9c64c-104">Avaliação \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="9c64c-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="9c64c-105">Planejamento \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="9c64c-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="9c64c-106">Implantação \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="9c64c-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="9c64c-107">Utilização \* \* \*</span><span class="sxs-lookup"><span data-stu-id="9c64c-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="9c64c-108">Iniciar avaliação</span><span class="sxs-lookup"><span data-stu-id="9c64c-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="9c64c-109">Iniciar planejamento</span><span class="sxs-lookup"><span data-stu-id="9c64c-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="9c64c-110">Você está aqui!</span><span class="sxs-lookup"><span data-stu-id="9c64c-110">You are here!</span></span>  <br/> [<span data-ttu-id="9c64c-111">Próxima etapa</span><span class="sxs-lookup"><span data-stu-id="9c64c-111">Next step</span></span>](ocas-deploy-conditional-access-app-control.md) <br/> |[<span data-ttu-id="9c64c-112">Começar a usar</span><span class="sxs-lookup"><span data-stu-id="9c64c-112">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |

<span data-ttu-id="9c64c-p101">No local de trabalho atual, geralmente não é suficiente saber o que está acontecendo no seu ambiente de nuvem após o fato. Você deseja interromper violações e vazamentos em tempo real, antes que os funcionários coloquem de forma intencional ou inadvertida seus dados e sua organização em risco. É importante permitir que os usuários em sua organização tornem a maior parte dos serviços e ferramentas disponíveis para eles em aplicativos de nuvem e permitam que eles coloquem seus próprios dispositivos para trabalhar. Ao mesmo tempo, você precisa de ferramentas para ajudar a proteger sua organização contra vazamentos de dados e roubo de dados, em tempo real. Junto com o Azure Active Directory, o Office 365 Cloud app Security fornece esses recursos em uma experiência holística e integrada com controle de aplicativo de acesso condicional.</span><span class="sxs-lookup"><span data-stu-id="9c64c-p101">In today’s workplace, it’s often not enough to know what’s happening in your cloud environment after the fact. You want to stop breaches and leaks in real time, before employees intentionally or inadvertently put your data and your organization at risk. It's important to enable users in your organization to make the most of the services and tools available to them in cloud apps, and let them bring their own devices to work. At the same time, you need tools to help protect your organization from data leaks, and data theft, in real time. Together with Azure Active Directory, Office 365 Cloud App Security delivers these capabilities in a holistic and integrated experience with Conditional Access App Control.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9c64c-118">para usar o controle de aplicativo de acesso condicional do cloud App Security, você precisa de uma  [licença do Azure Active Directory P1](https://azure.microsoft.com/pricing/details/active-directory/)e uma assinatura ativa [do Office 365 Cloud App Security](office-365-cas-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="9c64c-118">To use Cloud App Security Conditional Access App Control, you need an [Azure Active Directory P1 license](https://azure.microsoft.com/pricing/details/active-directory/) and an active [Office 365 Cloud App Security](office-365-cas-overview.md) subscription.</span></span>

## <a name="how-it-works"></a><span data-ttu-id="9c64c-119">Como funciona</span><span class="sxs-lookup"><span data-stu-id="9c64c-119">How it works</span></span>

<span data-ttu-id="9c64c-p102">O controle de aplicativo Conditional Access usa uma arquitetura de proxy reversa e é exclusivamente integrado ao acesso condicional do Azure AD. O acesso condicional do Azure AD permite que você aplique controles de acesso nos aplicativos da sua organização com base em determinadas condições. As condições definem *quem* (usuário ou grupo de usuários) e *o que* (quais aplicativos de nuvem) e *onde* (quais locais e redes) uma política de acesso condicional é aplicada. Depois de determinar as condições, você pode encaminhar usuários para o Office 365 Cloud app Security onde você pode proteger dados com o controle de aplicativo de acesso condicional aplicando controles de acesso e sessão.</span><span class="sxs-lookup"><span data-stu-id="9c64c-p102">Conditional Access App Control uses a reverse proxy architecture and is uniquely integrated with Azure AD conditional access. Azure AD conditional access allows you to enforce access controls on your organization’s apps based on certain conditions. The conditions define *who* (user or group of users) and *what* (which cloud apps) and *where* (which locations and networks) a conditional access policy is applied to. After you’ve determined the conditions, you can route users to Office 365 Cloud App Security where you can protect data with Conditional Access App Control by applying access and session controls.</span></span>

<span data-ttu-id="9c64c-p103">O controle de aplicativos de acesso condicional permite que as sessões e o acesso de aplicativos do usuário sejam monitorados e controlados em tempo real com base nas políticas de acesso e de sessão. As políticas de acesso e de sessão são usadas no portal do Cloud app Security para refinar os filtros e definir ações a serem tomadas em um usuário. Com as políticas de acesso e de sessão, você pode:</span><span class="sxs-lookup"><span data-stu-id="9c64c-p103">Conditional Access App Control enables user app access and sessions to be monitored and controlled in real time based on access and session policies. Access and session policies are used within the Cloud App Security portal to further refine filters and set actions to be taken on a user. With the access and session policies, you can:</span></span>

- <span data-ttu-id="9c64c-p104">**Bloquear ao baixar**: você pode bloquear o download de documentos confidenciais. Por exemplo, em dispositivos não gerenciados.</span><span class="sxs-lookup"><span data-stu-id="9c64c-p104">**Block on download**: You can block the download of sensitive documents. For example, on unmanaged devices.</span></span>

- <span data-ttu-id="9c64c-p105">**Proteger ao baixar**: em vez de bloquear o download de documentos confidenciais, você pode exigir que os documentos sejam protegidos por meio da criptografia no download. Essa criptografia garante que o documento esteja protegido e o acesso do usuário seja autenticado se os dados forem baixados para um dispositivo não confiável.</span><span class="sxs-lookup"><span data-stu-id="9c64c-p105">**Protect on download**: Instead of blocking the download of sensitive documents, you can require documents to be protected via encryption on download. This encryption makes sure the document is protected and user access is authenticated if the data is downloaded to an untrusted device.</span></span>

- <span data-ttu-id="9c64c-p106">**Monitorar sessões de usuário de baixa confiança**: os usuários arriscados são monitorados quando entram em aplicativos e suas ações são registradas de dentro da sessão. Você pode investigar e analisar o comportamento do usuário para entender onde e em que condições as políticas de sessão devem ser aplicadas no futuro.</span><span class="sxs-lookup"><span data-stu-id="9c64c-p106">**Monitor low-trust user sessions**: Risky users are monitored when they sign into apps and their actions are logged from within the session. You can investigate and analyze user behavior to understand where, and under what conditions, session policies should be applied in the future.</span></span>

- <span data-ttu-id="9c64c-133">**Bloquear o acesso**: você pode bloquear completamente o acesso a aplicativos específicos para usuários provenientes de dispositivos não gerenciados ou de redes não corporativas.</span><span class="sxs-lookup"><span data-stu-id="9c64c-133">**Block access**: You can completely block access to specific apps for users coming from unmanaged devices or from non-corporate networks.</span></span>

- <span data-ttu-id="9c64c-134">**Criar modo somente leitura**: ao monitorar e bloquear atividades personalizadas no aplicativo, você pode criar um modo somente leitura para aplicativos específicos para usuários específicos.</span><span class="sxs-lookup"><span data-stu-id="9c64c-134">**Create read-only mode**: By monitoring and blocking custom in-app activities, you can create a read-only mode to specific apps for specific users.</span></span>

- <span data-ttu-id="9c64c-p107">**Restringir sessões de usuário de redes não corporativas**: os usuários que acessam um aplicativo protegido de um local que não faz parte da sua rede corporativa têm permissão para acesso restrito. O download de materiais sensíveis é bloqueado ou protegido.</span><span class="sxs-lookup"><span data-stu-id="9c64c-p107">**Restrict user sessions from non-corporate networks**: Users accessing a protected app from a location that isn't part of your corporate network are allowed restricted access. The download of sensitive materials is blocked or protected.</span></span>

### <a name="how-session-control-works"></a><span data-ttu-id="9c64c-137">Como funciona o controle de sessão</span><span class="sxs-lookup"><span data-stu-id="9c64c-137">How session control works</span></span>

<span data-ttu-id="9c64c-p108">A criação de uma política de sessão com controle de aplicativo de acesso condicional permite controlar as sessões de usuário redirecionando o usuário por meio de um proxy reverso, em vez de diretamente para o aplicativo. A partir de então, as solicitações e respostas do usuário passam pelo Office 365 Cloud app Security, em vez de diretamente para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9c64c-p108">Creating a session policy with Conditional Access App Control enables you to control user sessions by redirecting the user through a reverse proxy instead of directly to the app. From then on, user requests and responses go through Office 365 Cloud App Security rather than directly to the app.</span></span>

<span data-ttu-id="9c64c-p109">Para manter o usuário na sessão, todas as URLs relevantes, scripts Java e cookies dentro da sessão de aplicativo são substituídas pelas URLs do Office 365 Cloud app Security. Por exemplo, se o aplicativo retornar uma página com links cujos domínios terminam com myapp.com, o link será substituído por domínios terminados com algo como: myapp.com.us.cas.ms</span><span class="sxs-lookup"><span data-stu-id="9c64c-p109">To keep the user within the session, all the relevant URLs, Java scripts, and cookies within the app session are replaced with Office 365 Cloud App Security URLs. For example, if the app returns a page with links whose domains end with myapp.com, the link is replaced with domains ending with something like: myapp.com.us.cas.ms</span></span>

<span data-ttu-id="9c64c-p110">Este método não exige que você instale nada no dispositivo. Este método é ideal ao monitorar sessões de dispositivos não gerenciados.</span><span class="sxs-lookup"><span data-stu-id="9c64c-p110">This method doesn't require you to install anything on the device. This method is ideal when monitoring sessions from unmanaged devices.</span></span>

<span data-ttu-id="9c64c-144">Depois que uma sessão é direcionada através do Office 365 Cloud app Security, as seguintes ações podem ser feitas:</span><span class="sxs-lookup"><span data-stu-id="9c64c-144">After a session is directed through Office 365 Cloud App Security, the following actions can be done:</span></span>

1. <span data-ttu-id="9c64c-145">Inspecionar o tráfego de atividades do usuário</span><span class="sxs-lookup"><span data-stu-id="9c64c-145">Inspect the traffic for user activities</span></span>

2. <span data-ttu-id="9c64c-146">Exibir as atividades identificadas no log de atividades do Office 365 Cloud app Security</span><span class="sxs-lookup"><span data-stu-id="9c64c-146">Display the identified activities in the Office 365 Cloud App Security Activity log</span></span>

3. <span data-ttu-id="9c64c-147">Salvar os logs de tráfego e analisá-los</span><span class="sxs-lookup"><span data-stu-id="9c64c-147">Save the traffic logs and analyze them</span></span>

4. <span data-ttu-id="9c64c-148">Habilitar o administrador para exportar os logs de tráfego</span><span class="sxs-lookup"><span data-stu-id="9c64c-148">Enable the admin to export the traffic logs</span></span>

5. <span data-ttu-id="9c64c-149">Impor políticas na sessão</span><span class="sxs-lookup"><span data-stu-id="9c64c-149">Enforce policies on the session</span></span>

## <a name="managed-device-identification"></a><span data-ttu-id="9c64c-150">Identificação do dispositivo gerenciado</span><span class="sxs-lookup"><span data-stu-id="9c64c-150">Managed device identification</span></span>

<span data-ttu-id="9c64c-p111">O controle de aplicativos de acesso condicional permite que você crie políticas que levam em consideração se um dispositivo é ou não gerenciado. Para identificar se um dispositivo é ou não gerenciado, o recurso usa:</span><span class="sxs-lookup"><span data-stu-id="9c64c-p111">Conditional Access App Control enables you to create policies that take into account whether a device is managed or not. To identify whether a device is managed or not, the feature uses:</span></span>

- <span data-ttu-id="9c64c-153">Dispositivos em conformidade</span><span class="sxs-lookup"><span data-stu-id="9c64c-153">Compliant devices</span></span>

- <span data-ttu-id="9c64c-154">Dispositivos ingressados no domínio</span><span class="sxs-lookup"><span data-stu-id="9c64c-154">Domain-joined devices</span></span>

- <span data-ttu-id="9c64c-155">Implantação de certificados de cliente</span><span class="sxs-lookup"><span data-stu-id="9c64c-155">Client certificates deployment</span></span>

### <a name="compliant-and-domain-joined-devices"></a><span data-ttu-id="9c64c-156">Dispositivos compatíveis e associados ao domínio</span><span class="sxs-lookup"><span data-stu-id="9c64c-156">Compliant and domain-joined devices</span></span>

<span data-ttu-id="9c64c-p112">O acesso condicional do Azure AD permite que as informações de dispositivo compatíveis e de domínio sejam passadas diretamente para o Office 365 Cloud app Security. A partir daí, uma política de acesso ou uma política de sessão pode ser desenvolvida que usa o estado do dispositivo como um filtro. Para obter mais informações, consulte o [tópico introdução ao gerenciamento de dispositivos no Azure Active Directory](https://docs.microsoft.com/azure/active-directory/device-management-introduction).</span><span class="sxs-lookup"><span data-stu-id="9c64c-p112">Azure AD conditional access enables compliant and domain-joined device information to be passed directly to Office 365 Cloud App Security. From there, an access policy or a session policy can be developed that uses device state as a filter. For more information, see the [Introduction to device management in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/device-management-introduction).</span></span>

### <a name="client-certificate-authenticated-devices"></a><span data-ttu-id="9c64c-160">Dispositivos autenticados pelo cliente-certificado</span><span class="sxs-lookup"><span data-stu-id="9c64c-160">Client-certificate authenticated devices</span></span>

<span data-ttu-id="9c64c-p113">O mecanismo de identificação de dispositivo pode solicitar a autenticação de dispositivos relevantes usando certificados de cliente. Você pode usar certificados de cliente existentes já implantados em sua organização ou implantar novos certificados de cliente em dispositivos gerenciados. Você usa a presença desses certificados para definir políticas de acesso e de sessão. Para obter informações sobre como implantar certificados de cliente, consulte [Deploy Conditional Access app Control for Office 365 apps](ocas-deploy-conditional-access-app-control.md).</span><span class="sxs-lookup"><span data-stu-id="9c64c-p113">The device identification mechanism can request authentication from relevant devices using client certificates. You can either use existing client certificates already deployed in your organization or roll out new client certificates to managed devices. You then use the presence of those certificates to set access and session policies. For information on how to deploy client certificates see [Deploy Conditional Access App Control for Office 365 apps](ocas-deploy-conditional-access-app-control.md).</span></span>

## <a name="supported-apps-and-clients"></a><span data-ttu-id="9c64c-165">Aplicativos e clientes com suporte</span><span class="sxs-lookup"><span data-stu-id="9c64c-165">Supported apps and clients</span></span>

<span data-ttu-id="9c64c-166">O controle de aplicativo Conditional Access para Office 365 suporta os seguintes aplicativos em destaque:</span><span class="sxs-lookup"><span data-stu-id="9c64c-166">Conditional Access App Control for Office 365 supports the following featured apps:</span></span>

- <span data-ttu-id="9c64c-167">Exchange Online (versão prévia)</span><span class="sxs-lookup"><span data-stu-id="9c64c-167">Exchange Online (preview)</span></span>

- <span data-ttu-id="9c64c-168">OneDrive for Business (visualização)</span><span class="sxs-lookup"><span data-stu-id="9c64c-168">OneDrive for Business (preview)</span></span>

- <span data-ttu-id="9c64c-169">Power BI (visualização)</span><span class="sxs-lookup"><span data-stu-id="9c64c-169">Power BI (preview)</span></span>

- <span data-ttu-id="9c64c-170">SharePoint Online (visualização)</span><span class="sxs-lookup"><span data-stu-id="9c64c-170">SharePoint Online (preview)</span></span>

- <span data-ttu-id="9c64c-171">Microsoft Teams (visualização)</span><span class="sxs-lookup"><span data-stu-id="9c64c-171">Microsoft Teams (preview)</span></span>

- <span data-ttu-id="9c64c-172">Yammer (versão prévia)</span><span class="sxs-lookup"><span data-stu-id="9c64c-172">Yammer (preview)</span></span>

<span data-ttu-id="9c64c-173">Aplicativos adicionais estão sendo continuamente integrados ao controle de sessão.</span><span class="sxs-lookup"><span data-stu-id="9c64c-173">Additional apps are being continuously on-boarded to session control.</span></span>

## <a name="next-steps"></a><span data-ttu-id="9c64c-174">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="9c64c-174">Next steps</span></span>

- [<span data-ttu-id="9c64c-175">Implantar o controle de aplicativo do Access condicional para aplicativos do Office 365</span><span class="sxs-lookup"><span data-stu-id="9c64c-175">Deploy Conditional Access App Control for Office 365 apps</span></span>](ocas-deploy-conditional-access-app-control.md)

- [<span data-ttu-id="9c64c-176">Saiba mais sobre as políticas de sessão no Office 365 Cloud app Security</span><span class="sxs-lookup"><span data-stu-id="9c64c-176">Learn about session policies in Office 365 Cloud App Security</span></span>](ocas-session-policies.md)

- [<span data-ttu-id="9c64c-177">Saiba mais sobre as políticas de acesso no Office 365 Cloud app Security</span><span class="sxs-lookup"><span data-stu-id="9c64c-177">Learn about access policies in Office 365 Cloud App Security</span></span>](ocas-access-policies.md) 
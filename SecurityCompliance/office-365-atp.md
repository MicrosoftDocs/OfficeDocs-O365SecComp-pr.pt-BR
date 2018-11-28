---
title: Proteção Avançada contra Ameaças do Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 11/27/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e100fe7c-f2a1-4b7d-9e08-622330b83653
description: Proteção de ameaça avançada do Office 365 inclui falso intelligence, links confiáveis, anexos seguros e recursos avançados de AntiPhishing. Proteção avançada de ameaça é também está sendo estendida para arquivos no SharePoint Online, o OneDrive for Business e Teams da Microsoft.
ms.openlocfilehash: c147fde4e470b998a66a2cb456be71f635db25d7
ms.sourcegitcommit: 2cf7f5bb282c971d33e00f65d9982a3f14aec74e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/27/2018
ms.locfileid: "26706305"
---
# <a name="office-365-advanced-threat-protection"></a><span data-ttu-id="fd482-104">Proteção Avançada contra Ameaças do Office 365</span><span class="sxs-lookup"><span data-stu-id="fd482-104">Office 365 Advanced Threat Protection</span></span>

## <a name="overview"></a><span data-ttu-id="fd482-105">Visão geral</span><span class="sxs-lookup"><span data-stu-id="fd482-105">Overview</span></span>

<span data-ttu-id="fd482-106">O Office 365 avançadas ameaça proteção (ATP) ajuda a proteger sua organização contra ataques mal-intencionados por:</span><span class="sxs-lookup"><span data-stu-id="fd482-106">Office 365 Advanced Threat Protection (ATP) helps to protect your organization from malicious attacks by:</span></span>
  
- <span data-ttu-id="fd482-107">Anexos de email de verificação de malware com [Anexos de seguros ATP](atp-safe-attachments.md)</span><span class="sxs-lookup"><span data-stu-id="fd482-107">Scanning email attachments for malware with [ATP Safe Attachments](atp-safe-attachments.md)</span></span>
    
- <span data-ttu-id="fd482-108">Verificação de web endereços (URLs) em mensagens de email e documentos do Office com [Links de seguros ATP](atp-safe-links.md)</span><span class="sxs-lookup"><span data-stu-id="fd482-108">Scanning web addresses (URLs) in email messages and Office documents with [ATP Safe Links](atp-safe-links.md)</span></span>
    
- <span data-ttu-id="fd482-109">Identificando e bloqueando mal-intencionado arquivos em bibliotecas online com [ATP para SharePoint, OneDrive e as equipes da Microsoft](atp-for-spo-odb-and-teams.md)</span><span class="sxs-lookup"><span data-stu-id="fd482-109">Identifying and blocking malicious files in online libraries with [ATP for SharePoint, OneDrive, and Microsoft Teams](atp-for-spo-odb-and-teams.md)</span></span>
    
- <span data-ttu-id="fd482-110">Verificando mensagens de email para falsificação não autorizado com [falsificação de inteligência de dados](learn-about-spoof-intelligence.md)</span><span class="sxs-lookup"><span data-stu-id="fd482-110">Checking email messages for unauthorized spoofing with [spoof intelligence](learn-about-spoof-intelligence.md)</span></span>
    
- <span data-ttu-id="fd482-111">Detectando quando alguém tenta representar seus usuários e domínios personalizados de sua organização com [recursos de AntiPhishing ATP no Office 365](atp-anti-phishing.md)</span><span class="sxs-lookup"><span data-stu-id="fd482-111">Detecting when someone attempts to impersonate your users and your organization's custom domains with [ATP anti-phishing capabilities in Office 365](atp-anti-phishing.md)</span></span>
    
<span data-ttu-id="fd482-p102">**Proteção por meio do Office 365 ATP é determinada pelas políticas que define as equipe de segurança da sua organização para Links de seguros, anexos seguros e antiphishing**. É importante Revise periodicamente e revisar suas políticas para mantê-los atualizados e para realizar as vantagens dos novos recursos que são adicionados ao serviço. [Os relatórios estão disponíveis](view-reports-for-atp.md) para mostrar como ATP está trabalhando para sua organização. Esses relatórios também podem mostrar áreas onde você pode precisar revisar e atualizar suas políticas. E, se você tiver arquivos que são marcados como malware que não deveria estar ou arquivos que você gostaria que a Microsoft para examinar, você pode [Enviar um arquivo para a Microsoft para análise](#submit-a-suspicious-file-to-microsoft-for-analysis).</span><span class="sxs-lookup"><span data-stu-id="fd482-p102">**Protection through Office 365 ATP is determined by policies that your organization's security team defines for Safe Links, Safe Attachments, and Anti-Phishing**. It's important to periodically review and revise your policies to keep them up to date and to take advantages of new features that are added to the service. [Reports are available](view-reports-for-atp.md) to show how ATP is working for your organization. These reports can also show you areas where you might need to review and update your policies. And, if you have files that are marked as malware that shouldn't be, or files you'd like Microsoft to examine, you can [submit a file to Microsoft for analysis](#submit-a-suspicious-file-to-microsoft-for-analysis).</span></span>

## <a name="new-features-are-continually-being-added-to-atp"></a><span data-ttu-id="fd482-117">Novos recursos são adicionados constantemente a ATP</span><span class="sxs-lookup"><span data-stu-id="fd482-117">New features are continually being added to ATP</span></span>

<span data-ttu-id="fd482-p103">Podemos está prosseguindo adicionar novos recursos para o Office 365 e que inclui ATP. Abaixo é uma lista de vários recursos novos; alguns deles chamadas por uma política de ATP para serem revisadas e atualizado. Para saber mais sobre os novos recursos, chegando ao ATP (ou Microsoft 365 em geral), visite o [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap?filters=O365).</span><span class="sxs-lookup"><span data-stu-id="fd482-p103">We are continuing to add new features to Office 365, and that includes ATP. Below is a list of several new features, some of which call for an ATP policy to be reviewed and updated. To learn more about new features coming to ATP (or Microsoft 365 in general), visit the [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap?filters=O365).</span></span>
  
- <span data-ttu-id="fd482-p104">Proteção de Links de seguros ATP a partir do final de 2017 de outubro, é estendida para aplicar a URLs em email, bem como as URLs em documentos do Office 365 ProPlus, como Word, Excel, PowerPoint e Visio no Windows, bem como Office apps em dispositivos com Android e iOS. (Certifique-se de que você estiver usando [Autenticação moderna do Office](https://docs.microsoft.com/office365/enterprise/modern-auth-for-office-2013-and-2016).)</span><span class="sxs-lookup"><span data-stu-id="fd482-p104">Beginning in late October 2017, ATP Safe Links protection is extended to apply to URLs in email as well as URLs in Office 365 ProPlus documents, such as Word, Excel, PowerPoint, and Visio on Windows, as well as Office apps on iOS and Android devices. (Make sure you're using [Modern Authentication for Office](https://docs.microsoft.com/office365/enterprise/modern-auth-for-office-2013-and-2016).)</span></span>
    
- <span data-ttu-id="fd482-p105">Iniciando no de 2018 de março, proteção de Links de seguros ATP é estendida para aplicar a emails enviados entre pessoas dentro de uma organização. (Certifique-se para [rever e editar suas políticas de Links de seguros ATP](set-up-atp-safe-links-policies.md).)</span><span class="sxs-lookup"><span data-stu-id="fd482-p105">Beginning in March 2018, ATP Safe Links protection is extended to apply to email sent between people within an organization. (Make sure to [review and edit your ATP Safe Links policies](set-up-atp-safe-links-policies.md).)</span></span>

- <span data-ttu-id="fd482-125">Iniciando no tardia de 2018 de maio, recursos de [quarentena](quarantine-email-messages.md) na segurança &amp; Centro de conformidade estão sendo estendidas para [ATP para o SharePoint Online, OneDrive for Business e equipes da Microsoft](atp-for-spo-odb-and-teams.md).</span><span class="sxs-lookup"><span data-stu-id="fd482-125">Beginning in late May 2018, [quarantine](quarantine-email-messages.md) capabilities in the Security &amp; Compliance Center are being extended to [ATP for SharePoint Online, OneDrive for Business, and Microsoft Teams](atp-for-spo-odb-and-teams.md).</span></span>
 
- <span data-ttu-id="fd482-p106">Proteção de Links de seguros ATP começando na segunda metade do 2018, é estendida para aplicar a URLs no Office Online (on-line do Word, Excel Online, on-line do PowerPoint e OneNote Online) e Office 365 ProPlus em Mac. (Certifique-se para [rever e editar suas políticas de Links de seguros ATP](set-up-atp-safe-links-policies.md).)</span><span class="sxs-lookup"><span data-stu-id="fd482-p106">Beginning in the second half of 2018, ATP Safe Links protection is extended to apply to URLs in Office Online (Word Online, Excel Online, PowerPoint Online, and OneNote Online) and Office 365 ProPlus on Mac. (Make sure to [review and edit your ATP Safe Links policies](set-up-atp-safe-links-policies.md).)</span></span>

- <span data-ttu-id="fd482-128">Início em setembro de 2018, o recurso de [páginas de aviso do Office 365 ATP](atp-safe-links-warning-pages.md) um novo esquema de cores, mais detalhes e a capacidade para continuar a um site apesar recebe avisos e recomendações.</span><span class="sxs-lookup"><span data-stu-id="fd482-128">Beginning in September 2018, [Office 365 ATP warning pages](atp-safe-links-warning-pages.md) feature a new color scheme, more details, and the ability to continue to a site despite given warnings and recommendations.</span></span> 
 
- <span data-ttu-id="fd482-p107">Iniciando no outubro de 2018 e aplicação nos próximos meses várias, quando pessoas estão usando o Outlook Web Application (OWA) ou o Outlook, Links confiáveis de ATP renderiza URLs originais, não regravado URLs. (Chamamos essa visibilidade link nativo.)</span><span class="sxs-lookup"><span data-stu-id="fd482-p107">Beginning in October 2018 and rolling out over the next several months, when people are using Outlook Web Application (OWA) or Outlook, ATP Safe Links renders original URLs, not rewritten URLs. (We call this native link visibility.)</span></span>

      
## <a name="get-office-365-atp"></a><span data-ttu-id="fd482-131">Obter ATP do Office 365</span><span class="sxs-lookup"><span data-stu-id="fd482-131">Get Office 365 ATP</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fd482-p108">O Office 365 ATP está incluído no inscrições, como Microsoft 365 Enterprise, Office 365 Enterprise E5, A5 de educação do Office 365 e [Microsoft 365 Business](https://docs.microsoft.com/en-us/microsoft-365/business/security-features). Se sua organização tiver uma assinatura do Office 365 que não inclui ATP do Office 365, você pode adquirir potencialmente ATP como um complemento. Para obter mais informações, consulte [Office 365 avançadas Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span><span class="sxs-lookup"><span data-stu-id="fd482-p108">Office 365 ATP is included in subscriptions, such as Microsoft 365 Enterprise, Office 365 Enterprise E5, Office 365 Education A5, and [Microsoft 365 Business](https://docs.microsoft.com/en-us/microsoft-365/business/security-features). If your organization has an Office 365 subscription that does not include Office 365 ATP, you can potentially purchase ATP as an add-on. For more information, see [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span> 

1. <span data-ttu-id="fd482-135">Como um administrador global ou de segurança, vá para [https://portal.office.com](https://portal.office.com) e entre com sua conta de trabalho ou da escola para o Office 365.</span><span class="sxs-lookup"><span data-stu-id="fd482-135">As a global or security administrator, go to [https://portal.office.com](https://portal.office.com) and sign in with your work or school account for Office 365.</span></span> 
    
2. <span data-ttu-id="fd482-136">Escolha **administrador** \> **cobrança** para ver o que inclui a sua assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="fd482-136">Choose **Admin** \> **Billing** to see what your current subscription includes.</span></span> <br/><span data-ttu-id="fd482-137">![Como um administrador global, entrar no portal.office.com e vá até Admin \> de cobrança](media/18a3546c-bd1f-4f49-82ec-0184909b42c2.png)</span><span class="sxs-lookup"><span data-stu-id="fd482-137">![As a global admin, sign in at portal.office.com and go to Admin \> Billing](media/18a3546c-bd1f-4f49-82ec-0184909b42c2.png)</span></span>
  
3. <span data-ttu-id="fd482-138">Se você vir **E5 do Office 365 Enterprise**, **A5 de educação do Office 365**ou **Microsoft 365 Business**, sua organização tem ATP.</span><span class="sxs-lookup"><span data-stu-id="fd482-138">If you see **Office 365 Enterprise E5**, **Office 365 Education A5**, or **Microsoft 365 Business**, then your organization has ATP.</span></span> <br/><span data-ttu-id="fd482-p109">Se você vir uma assinatura diferente, como o **Office 365 Enterprise E3** ou **Office 365 Enterprise E1**, considere a adição de ATP. Para fazer isso, escolha **+ Adicionar assinatura**.</span><span class="sxs-lookup"><span data-stu-id="fd482-p109">If you see a different subscription, such as **Office 365 Enterprise E3** or **Office 365 Enterprise E1**, consider adding ATP. To do that, choose **+ Add subscription**.</span></span>
    
<span data-ttu-id="fd482-141">Depois que você tiver ATP, a próxima etapa é para sua equipe de segurança definir políticas.</span><span class="sxs-lookup"><span data-stu-id="fd482-141">Once you have ATP, the next step is for your security team to define policies.</span></span> 
  
## <a name="define-policies-for-atp"></a><span data-ttu-id="fd482-142">Definir diretivas para ATP</span><span class="sxs-lookup"><span data-stu-id="fd482-142">Define policies for ATP</span></span>

- <span data-ttu-id="fd482-143">**[Configurar políticas de AntiPhishing ATP no Office 365](set-up-anti-phishing-policies.md)** incluindo ataques baseados em representação para proteger contra invasores que enviam mensagens de email que parecem ser de pessoas confiáveis ou domínios</span><span class="sxs-lookup"><span data-stu-id="fd482-143">**[Set up ATP anti-phishing policies in Office 365](set-up-anti-phishing-policies.md)** including impersonation-based attacks to protect against attackers who send email messages that appear to be from trusted people or domains</span></span> 

- <span data-ttu-id="fd482-144">**[Configurar políticas de Links de ATP seguros no Office 365](set-up-atp-safe-links-policies.md)** , incluindo [lista personalizada de URLs bloqueada](set-up-a-custom-blocked-urls-list-wtih-atp.md) e a [lista de URLs personalizada "Não regravação"](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) da sua organização</span><span class="sxs-lookup"><span data-stu-id="fd482-144">**[Set up ATP Safe Links policies in Office 365](set-up-atp-safe-links-policies.md)** including your organization's [custom blocked URLs list](set-up-a-custom-blocked-urls-list-wtih-atp.md) and [custom "Do not rewrite" URLs list](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md)</span></span>
    
- <span data-ttu-id="fd482-145">**[Configurar políticas de anexos de ATP seguros no Office 365](set-up-atp-safe-attachments-policies.md)** que pode incluir a [entrega dinâmica e visualização](dynamic-delivery-and-previewing.md)</span><span class="sxs-lookup"><span data-stu-id="fd482-145">**[Set up ATP Safe Attachments policies in Office 365](set-up-atp-safe-attachments-policies.md)** that can include [Dynamic Delivery and previewing](dynamic-delivery-and-previewing.md)</span></span>
  
## <a name="see-how-atp-is-working-by-viewing-reports"></a><span data-ttu-id="fd482-146">Consulte como ATP está funcionando exibindo relatórios</span><span class="sxs-lookup"><span data-stu-id="fd482-146">See how ATP is working by viewing reports</span></span>

<span data-ttu-id="fd482-147">Depois que suas políticas de ATP estão funcionando, relatórios estão disponíveis para mostrar como o serviço está funcionando.</span><span class="sxs-lookup"><span data-stu-id="fd482-147">After your ATP policies are in place, reports are available to show how the service is working.</span></span>

<span data-ttu-id="fd482-148">[![A segurança &amp; painel do Centro de conformidade pode ajudá-lo a ver onde a proteção de ameaça Avançado está funcionando](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)](view-reports-for-atp.md)</span><span class="sxs-lookup"><span data-stu-id="fd482-148">[![The Security &amp; Compliance Center dashboard can help you see where Advanced Threat Protection is working](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)](view-reports-for-atp.md)</span></span>
  
1. <span data-ttu-id="fd482-p110">Certifique-se de que você é um administrador global, administrador de segurança ou leitor de segurança do Office 365. (Consulte [Permissions in a segurança do Office 365 &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md).)</span><span class="sxs-lookup"><span data-stu-id="fd482-p110">Make sure that you are an Office 365 global administrator, security administrator, or security reader. (See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).)</span></span>
    
2. <span data-ttu-id="fd482-151">[Exibir relatórios de proteção avançada de ameaça](view-reports-for-atp.md).</span><span class="sxs-lookup"><span data-stu-id="fd482-151">[View reports for Advanced Threat Protection](view-reports-for-atp.md).</span></span>
    
3. <span data-ttu-id="fd482-p111">Se necessário, fazer ajustes suas políticas de segurança. Consulte os seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="fd482-p111">If needed, make adjustments to your security policies. See the following resources:</span></span>

  - [<span data-ttu-id="fd482-154">Políticas de AntiPhishing ATP no Office 365</span><span class="sxs-lookup"><span data-stu-id="fd482-154">ATP anti-phishing policies in Office 365</span></span>](set-up-anti-phishing-policies.md)
    
  - [<span data-ttu-id="fd482-155">Políticas de Links de ATP seguros no Office 365</span><span class="sxs-lookup"><span data-stu-id="fd482-155">ATP Safe Links policies in Office 365</span></span>](set-up-atp-safe-links-policies.md)
    
  - [<span data-ttu-id="fd482-156">Políticas de anexos de ATP seguros no Office 365</span><span class="sxs-lookup"><span data-stu-id="fd482-156">ATP Safe Attachments policies in Office 365</span></span>](set-up-atp-safe-attachments-policies.md)
    
    
## <a name="submit-a-suspicious-file-to-microsoft-for-analysis"></a><span data-ttu-id="fd482-157">Enviar um arquivo suspeito à Microsoft para análise</span><span class="sxs-lookup"><span data-stu-id="fd482-157">Submit a suspicious file to Microsoft for analysis</span></span>

- <span data-ttu-id="fd482-p112">Se você receber um arquivo que você supõe que poderia ser malware, você poderá enviar esse arquivo para a Microsoft para análise. Visite o [portal de envio de inteligência de segurança do Windows Defender](https://go.microsoft.com/fwlink/?linkid=857185).</span><span class="sxs-lookup"><span data-stu-id="fd482-p112">If you get a file that you suspect could be malware, you can submit that file to Microsoft for analysis. Visit the [Windows Defender Security Intelligence submission portal](https://go.microsoft.com/fwlink/?linkid=857185).</span></span>

- <span data-ttu-id="fd482-160">Se você receber uma mensagem de email (com ou sem um anexo) que deseja usar para enviar à Microsoft para análise, use o [suplemento de mensagem de relatório](enable-the-report-message-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="fd482-160">If you get an email message (with or without an attachment) that you'd like to submit to Microsoft for analysis, use the [Report Message add-in](enable-the-report-message-add-in.md).</span></span> 
  


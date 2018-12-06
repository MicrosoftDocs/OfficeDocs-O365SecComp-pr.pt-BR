---
title: Habilitar ou desabilitar dicas de segurança no Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/05/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f09668bd-fe1a-4c01-89e3-e88c370e66c7
description: Informa os administradores do Office 365 e o EOP como habilitar e desabilitar dicas de segurança em mensagens de email.
ms.openlocfilehash: 8e5d8bf1d2f831b5d74ca3accd8b434519bfeaab
ms.sourcegitcommit: 204fb0269b5c10b63941055824e863d77e3e9b02
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/06/2018
ms.locfileid: "27180851"
---
# <a name="enable-or-disable-safety-tips-in-office-365"></a><span data-ttu-id="e1566-103">Habilitar ou desabilitar dicas de segurança no Office 365</span><span class="sxs-lookup"><span data-stu-id="e1566-103">Enable or disable safety tips in Office 365</span></span>

<span data-ttu-id="e1566-p101">Exchange Online Protection (EOP) adiciona ou carimbos, um safety dica para mensagens de email que ele oferece. Destinatários com uma maneira rápida e visual para determinar se uma mensagem é de um seguro, de fornecer essas dicas de segurança verificadas remetente, se a mensagem foi marcada como spam pelo Office 365, se a mensagem contiver algo suspeito, como um esquema de phishing, ou se tiverem imagens externas foi bloqueado. Office 365 e o EOP autônomo admins pode editar uma configuração de política de spam para ativar ou desativar dicas de segurança seja exibido em um email no Outlook e outros clientes de email da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e1566-p101">Exchange Online Protection (EOP) adds, or stamps, a safety tip to email messages that it delivers. These safety tips provide recipients with a quick, visual way to determine if a message is from a safe, verified sender, if the message has been marked as spam by Office 365, if the message contains something suspicious such as a phishing scam, or if external images have been blocked. Office 365 and EOP-standalone admins can edit a spam policy setting to enable or disable safety tips from being displayed in email in Outlook and other desktop email clients.</span></span> 
  
<span data-ttu-id="e1566-p102">O Office 365 habilita dicas de segurança por padrão para a sua organização e é recomendável que você deixe-los ativado para ajudar a combater ataques de spam e phishing. Você não pode desativar dicas de segurança para Outlook na web.</span><span class="sxs-lookup"><span data-stu-id="e1566-p102">Office 365 enables safety tips by default for your organization and we recommend that you leave them enabled to help combat spam and phishing attacks. You can't disable safety tips for Outlook on the web.</span></span>
  
<span data-ttu-id="e1566-109">Para ver exemplos e para saber mais sobre as informações exibidas em dicas de segurança, consulte [Safety dicas em mensagens de email no Office 365.](safety-tips-in-office-365.md)</span><span class="sxs-lookup"><span data-stu-id="e1566-109">To see examples and to learn about the information displayed in safety tips, see [Safety tips in email messages in Office 365.](safety-tips-in-office-365.md)</span></span>
  
<span data-ttu-id="e1566-110">Neste tópico:</span><span class="sxs-lookup"><span data-stu-id="e1566-110">In this topic:</span></span>
  
- [<span data-ttu-id="e1566-111">Para ativar ou desativar dicas de segurança usando a segurança do Office 365 &amp; Centro de conformidade</span><span class="sxs-lookup"><span data-stu-id="e1566-111">To enable or disable safety tips by using the Office 365 Security &amp; Compliance Center</span></span>](enable-or-disable-safety-tips.md#SandCCsafetytip)
    
- [<span data-ttu-id="e1566-112">Para ativar ou desativar dicas de segurança usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="e1566-112">To enable or disable safety tips by using PowerShell</span></span>](enable-or-disable-safety-tips.md#pshellsafetytip)
    
## <a name="to-enable-or-disable-safety-tips-by-using-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="e1566-113">Para ativar ou desativar dicas de segurança usando a segurança do Office 365 &amp; Centro de conformidade</span><span class="sxs-lookup"><span data-stu-id="e1566-113">To enable or disable safety tips by using the Office 365 Security &amp; Compliance Center</span></span>
<span data-ttu-id="e1566-114"><a name="SandCCsafetytip"> </a></span><span class="sxs-lookup"><span data-stu-id="e1566-114"></span></span>

1. <span data-ttu-id="e1566-115">Acesse [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="e1566-115">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="e1566-116">Entre no Office 365 com a sua conta corporativa ou de estudante.</span><span class="sxs-lookup"><span data-stu-id="e1566-116">Sign in to Office 365 with your work or school account.</span></span>
    
3. <span data-ttu-id="e1566-117">Escolha **gerenciamento de ameaça** \> **política**.</span><span class="sxs-lookup"><span data-stu-id="e1566-117">Choose **Threat Management** \> **Policy**.</span></span> 
    
4. <span data-ttu-id="e1566-118">Na página **política** , escolha **Anti-Spam**.</span><span class="sxs-lookup"><span data-stu-id="e1566-118">On the **Policy** page, choose **Anti-Spam**.</span></span>
    
    ![Esta captura de tela mostra como obter para a página de configurações antispam na segurança &amp; Centro de conformidade.](media/b8eb2ee3-2eb1-4ea2-b138-f6d7fb2e23de.png)
  
5. <span data-ttu-id="e1566-120">Na página **configurações antispam** escolha a guia **personalizada** .</span><span class="sxs-lookup"><span data-stu-id="e1566-120">On the **Anti-spam settings** page choose the **Custom** tab.</span></span> 
    
    ![Esta captura de tela mostra a localização da guia personalizada na página Configurações antispam na segurança &amp; Centro de conformidade.](media/1d688d23-e6f3-4de5-84a7-e8ce31786193.png)
  
6. <span data-ttu-id="e1566-p103">Se necessário, escolha a opção **configurações personalizadas** para ativar configurações personalizadas. Se a opção configurações personalizadas é definida como **desativado**, você não conseguirá modificar políticas de filtro de spam.</span><span class="sxs-lookup"><span data-stu-id="e1566-p103">If necessary, choose the **Custom settings** switch to turn on custom settings. If the custom settings switch is set to **Off**, you won't be able to modify spam filter policies.</span></span>
    
    ![Esta captura de tela mostra personalizada de filtro antispam configurações de política desativadas.](media/94f900ad-b556-4a31-a3ac-acfcd72e71b8.png)
  
7. <span data-ttu-id="e1566-p104">Expanda a política de spam que você deseja modificar e, em seguida, escolha **Editar política**. Por exemplo, escolha a seta para baixo ao lado de **política de filtro de spam de padrão**. Ou, se desejar, você pode criar uma nova política escolhendo **Adicionar uma política**.</span><span class="sxs-lookup"><span data-stu-id="e1566-p104">Expand the spam policy you want to modify and then choose **Edit policy**. For example, choose the down arrow next to **Default spam filter policy**. Or, if you want, you can create a new policy by choosing **Add a policy**.</span></span>
    
8. <span data-ttu-id="e1566-128">Expanda ações **em massa e Spam** .</span><span class="sxs-lookup"><span data-stu-id="e1566-128">Expand **Spam and bulk** actions.</span></span> 
    
9. <span data-ttu-id="e1566-p105">Para ativar as dicas de segurança, em **Dicas de segurança**, marque a caixa de seleção **em** . Para desativar dicas de segurança, desmarque a caixa de seleção **no** .</span><span class="sxs-lookup"><span data-stu-id="e1566-p105">To enable safety tips, under **Safety Tips**, check the **On** checkbox. To disable safety tips, clear the **On** checkbox.</span></span> 
    
10. <span data-ttu-id="e1566-131">Escolha **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="e1566-131">Choose **Save**.</span></span>
    
## <a name="to-enable-or-disable-safety-tips-by-using-powershell"></a><span data-ttu-id="e1566-132">Para ativar ou desativar dicas de segurança usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="e1566-132">To enable or disable safety tips by using PowerShell</span></span>
<span data-ttu-id="e1566-133"><a name="pshellsafetytip"> </a></span><span class="sxs-lookup"><span data-stu-id="e1566-133"></span></span>

<span data-ttu-id="e1566-p106">Os administradores podem usar o PowerShell do Exchange Online para habilitar ou desabilitar sugestões de segurança. Use o cmdlet Set-HostedContentFilterPolicy para ativar ou desativar dicas de segurança em uma política de filtro de spam.</span><span class="sxs-lookup"><span data-stu-id="e1566-p106">Admins can use Exchange Online PowerShell to enable or disable safety tips. Use the Set-HostedContentFilterPolicy cmdlet to enable or disable safety tips in a spam filter policy.</span></span>
  
1. <span data-ttu-id="e1566-p107">Conecte-se para o Exchange Online PowerShell. Para obter informações, consulte [Connect to Exchange Online PowerShell](http://go.microsoft.com/fwlink/p/?LinkId=396554).</span><span class="sxs-lookup"><span data-stu-id="e1566-p107">Connect to Exchange Online PowerShell. For information, see [Connect to Exchange Online PowerShell](http://go.microsoft.com/fwlink/p/?LinkId=396554).</span></span>
    
2. <span data-ttu-id="e1566-138">Execute o cmdlet Set-HostedContentFilterPolicy para ativar ou desativar dicas de segurança:</span><span class="sxs-lookup"><span data-stu-id="e1566-138">Run the Set-HostedContentFilterPolicy cmdlet to enable or disable safety tips:</span></span>
    
  ```
  Set-HostedContentFilterPolicy -Identity "policy name " -InlineSafetyTipsEnabled <$true|$false>
  ```

<span data-ttu-id="e1566-139">Onde:</span><span class="sxs-lookup"><span data-stu-id="e1566-139">Where:</span></span>
    
  -  <span data-ttu-id="e1566-140">*nome da política* é o nome da política que deseja modificar, por exemplo **padrão**.</span><span class="sxs-lookup"><span data-stu-id="e1566-140">*policy name*  is the name of the policy you want to modify, for example **default**.</span></span>
    
  -  <span data-ttu-id="e1566-141">`$true`Habilita as dicas de segurança para a política de filtro de spam.</span><span class="sxs-lookup"><span data-stu-id="e1566-141">`$true` enables safety tips for the spam filter policy.</span></span> 
    
  -  <span data-ttu-id="e1566-142">`$false`Desabilita as dicas de segurança para a política de filtro de spam.</span><span class="sxs-lookup"><span data-stu-id="e1566-142">`$false` disables safety tips for the spam filter policy.</span></span> 
    
    <span data-ttu-id="e1566-143">Por exemplo, para desabilitar dicas de segurança para a política de filtro de spam padrão, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="e1566-143">For example, to disable safety tips for the default spam filter policy, run the following command:</span></span>
    
  ```
  PS C:\> Set-HostedContentFilterPolicy -Identity "default" -InlineSafetyTipsEnabled $false
  ```

<span data-ttu-id="e1566-144">Para obter mais informações sobre esse cmdlet, consulte [Set-HostedContentFilterPolicy](https://technet.microsoft.com/library/jj200781.aspx).</span><span class="sxs-lookup"><span data-stu-id="e1566-144">For more information about this cmdlet, see [Set-HostedContentFilterPolicy](https://technet.microsoft.com/library/jj200781.aspx).</span></span>
    
## <a name="still-need-help"></a><span data-ttu-id="e1566-145">Ainda precisa de ajuda?</span><span class="sxs-lookup"><span data-stu-id="e1566-145">Still need help?</span></span>
<span data-ttu-id="e1566-146"><a name="pshellsafetytip"> </a></span><span class="sxs-lookup"><span data-stu-id="e1566-146"></span></span>

<span data-ttu-id="e1566-147">Se desabilitada dicas de segurança, mas são ainda vê-las em suas mensagens de email, verifique esses aspectos:</span><span class="sxs-lookup"><span data-stu-id="e1566-147">If you disabled safety tips but are still seeing them in your email messages, check these things:</span></span>
  
- <span data-ttu-id="e1566-p108">Você não pode desativar dicas de segurança para Outlook na web. Tente exibindo o mesmo email em outro cliente, como o Outlook.</span><span class="sxs-lookup"><span data-stu-id="e1566-p108">You can't disable safety tips for Outlook on the web. Try viewing the same email in another client, such as Outlook.</span></span>
    
- <span data-ttu-id="e1566-p109">Dicas de segurança estão ativas, por padrão para cada um que usa o EOP, isso inclui todas as pessoas que possui o Office 365. Para desabilitar dicas de segurança seja exibido no email, você deve desabilitá-los usando uma política de filtro de spam, conforme descrito neste tópico. Depois que você tiver configurado a política, certifique-se de que ele está habilitado. Para obter informações sobre como habilitar as políticas de filtro de spam, consulte [configurar suas políticas de filtro de spam](https://technet.microsoft.com/library/jj200684.aspx).</span><span class="sxs-lookup"><span data-stu-id="e1566-p109">Safety tips are on by default for every one who uses EOP, this includes everyone who has Office 365. In order to disable safety tips from showing up in email, you must disable them by using a spam filter policy as described in this topic. Once you've set up the policy, ensure that it is enabled. For information on enabling spam filter policies, see [Configure your spam filter policies](https://technet.microsoft.com/library/jj200684.aspx).</span></span>
    
<span data-ttu-id="e1566-154">Para obter mais formas combater spam e phishing, consulte [Proteção de Anti-Spam de Email do Office 365](anti-spam-protection.md).</span><span class="sxs-lookup"><span data-stu-id="e1566-154">For more ways to combat spam and phishing, see [Office 365 Email Anti-Spam Protection](anti-spam-protection.md).</span></span>
  


---
title: Ativar ou desativar as dicas de segurança no Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/05/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f09668bd-fe1a-4c01-89e3-e88c370e66c7
ms.collection:
- M365-security-compliance
description: Informa aos administradores do Office 365 e do EOP como habilitar e desabilitar dicas de segurança em mensagens de email.
ms.openlocfilehash: 9be9c4cd7fc8e94208aac2ad8812c93a3465f58b
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32256932"
---
# <a name="enable-or-disable-safety-tips-in-office-365"></a><span data-ttu-id="ebfc5-103">Ativar ou desativar as dicas de segurança no Office 365</span><span class="sxs-lookup"><span data-stu-id="ebfc5-103">Enable or disable safety tips in Office 365</span></span>

<span data-ttu-id="ebfc5-104">O proteção do Exchange Online (EOP) adiciona, ou carimbos, uma dica de segurança a mensagens de email que ele fornece.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-104">Exchange Online Protection (EOP) adds, or stamps, a safety tip to email messages that it delivers.</span></span> <span data-ttu-id="ebfc5-105">Essas dicas de segurança fornecem aos destinatários uma forma rápida e Visual de determinar se uma mensagem é de um remetente seguro e verificado, se a mensagem tiver sido marcada como spam pelo Office 365, se a mensagem contiver algo suspeito, como um golpe de phishing, ou se imagens externas tiverem foi bloqueado.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-105">These safety tips provide recipients with a quick, visual way to determine if a message is from a safe, verified sender, if the message has been marked as spam by Office 365, if the message contains something suspicious such as a phishing scam, or if external images have been blocked.</span></span> <span data-ttu-id="ebfc5-106">Os administradores do Office 365 e do EOP-autônomo podem editar uma configuração de política de spam para habilitar ou desabilitar que as dicas de segurança sejam exibidas no email no Outlook e em outros clientes de email de área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-106">Office 365 and EOP-standalone admins can edit a spam policy setting to enable or disable safety tips from being displayed in email in Outlook and other desktop email clients.</span></span> 
  
<span data-ttu-id="ebfc5-107">O Office 365 permite dicas de segurança por padrão para sua organização e recomendamos que você as deixe habilitadas para ajudar a combater spam e ataques de phishing.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-107">Office 365 enables safety tips by default for your organization and we recommend that you leave them enabled to help combat spam and phishing attacks.</span></span> <span data-ttu-id="ebfc5-108">Não é possível desabilitar dicas de segurança para o Outlook na Web.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-108">You can't disable safety tips for Outlook on the web.</span></span>
  
<span data-ttu-id="ebfc5-109">Para ver exemplos e saber mais sobre as informações exibidas em dicas de segurança, consulte [dicas de segurança em mensagens de email no Office 365.](safety-tips-in-office-365.md)</span><span class="sxs-lookup"><span data-stu-id="ebfc5-109">To see examples and to learn about the information displayed in safety tips, see [Safety tips in email messages in Office 365.](safety-tips-in-office-365.md)</span></span>
  
<span data-ttu-id="ebfc5-110">Neste tópico:</span><span class="sxs-lookup"><span data-stu-id="ebfc5-110">In this topic:</span></span>
  
- [<span data-ttu-id="ebfc5-111">Para habilitar ou desabilitar dicas de segurança usando o centro de conformidade &amp; de segurança do Office 365</span><span class="sxs-lookup"><span data-stu-id="ebfc5-111">To enable or disable safety tips by using the Office 365 Security &amp; Compliance Center</span></span>](enable-or-disable-safety-tips.md#SandCCsafetytip)
    
- [<span data-ttu-id="ebfc5-112">Para habilitar ou desabilitar dicas de segurança usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="ebfc5-112">To enable or disable safety tips by using PowerShell</span></span>](enable-or-disable-safety-tips.md#pshellsafetytip)
    
## <a name="to-enable-or-disable-safety-tips-by-using-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="ebfc5-113">Para habilitar ou desabilitar dicas de segurança usando o centro de conformidade &amp; de segurança do Office 365</span><span class="sxs-lookup"><span data-stu-id="ebfc5-113">To enable or disable safety tips by using the Office 365 Security &amp; Compliance Center</span></span>
<span data-ttu-id="ebfc5-114"><a name="SandCCsafetytip"> </a></span><span class="sxs-lookup"><span data-stu-id="ebfc5-114"></span></span>

1. <span data-ttu-id="ebfc5-115">Acesse [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="ebfc5-115">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="ebfc5-116">Entre no Office 365 com uma conta corporativa ou de estudante.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-116">Sign in to Office 365 with your work or school account.</span></span>
    
3. <span data-ttu-id="ebfc5-117">Escolha \*\*\*\* \> **política**de gerenciamento de ameaças.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-117">Choose **Threat Management** \> **Policy**.</span></span> 
    
4. <span data-ttu-id="ebfc5-118">Na página **política** , escolha **anti-spam**.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-118">On the **Policy** page, choose **Anti-Spam**.</span></span>
    
    ![Esta captura de tela mostra como acessar a página configurações antispam no centro de conformidade de &amp; segurança.](media/b8eb2ee3-2eb1-4ea2-b138-f6d7fb2e23de.png)
  
5. <span data-ttu-id="ebfc5-120">Na página **configurações antispam,** escolha a guia **personalizado** .</span><span class="sxs-lookup"><span data-stu-id="ebfc5-120">On the **Anti-spam settings** page choose the **Custom** tab.</span></span> 
    
    ![Esta captura de tela mostra a localização da guia personalizada na página configurações antispam no centro de conformidade de &amp; segurança.](media/1d688d23-e6f3-4de5-84a7-e8ce31786193.png)
  
6. <span data-ttu-id="ebfc5-122">Se necessário, escolha a opção **configurações personalizadas** para ativar as configurações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-122">If necessary, choose the **Custom settings** switch to turn on custom settings.</span></span> <span data-ttu-id="ebfc5-123">Se a opção configurações personalizadas estiver definida como \*\*\*\* desativada, você não poderá modificar as políticas de filtro de spam.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-123">If the custom settings switch is set to **Off**, you won't be able to modify spam filter policies.</span></span>
    
    ![Esta captura de tela mostra as configurações de política de filtro antispam personalizadas desativadas.](media/94f900ad-b556-4a31-a3ac-acfcd72e71b8.png)
  
7. <span data-ttu-id="ebfc5-125">Expanda a política de spam que você deseja modificar e, em seguida, escolha **Editar política**.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-125">Expand the spam policy you want to modify and then choose **Edit policy**.</span></span> <span data-ttu-id="ebfc5-126">Por exemplo, escolha a seta para baixo ao lado de **política padrão de filtro de spam**.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-126">For example, choose the down arrow next to **Default spam filter policy**.</span></span> <span data-ttu-id="ebfc5-127">Ou, se quiser, você pode criar uma nova política escolhendo **Adicionar uma política**.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-127">Or, if you want, you can create a new policy by choosing **Add a policy**.</span></span>
    
8. <span data-ttu-id="ebfc5-128">Expanda **spam e ações em massa** .</span><span class="sxs-lookup"><span data-stu-id="ebfc5-128">Expand **Spam and bulk** actions.</span></span> 
    
9. <span data-ttu-id="ebfc5-129">Para habilitar as dicas de segurança, em **dicas de segurança**, marque a caixa **de seleção ao** .</span><span class="sxs-lookup"><span data-stu-id="ebfc5-129">To enable safety tips, under **Safety Tips**, check the **On** checkbox.</span></span> <span data-ttu-id="ebfc5-130">Para desabilitar as dicas de segurança, desmarque a caixa **de seleção ao** .</span><span class="sxs-lookup"><span data-stu-id="ebfc5-130">To disable safety tips, clear the **On** checkbox.</span></span> 
    
10. <span data-ttu-id="ebfc5-131">Selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-131">Choose **Save**.</span></span>
    
## <a name="to-enable-or-disable-safety-tips-by-using-powershell"></a><span data-ttu-id="ebfc5-132">Para habilitar ou desabilitar dicas de segurança usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="ebfc5-132">To enable or disable safety tips by using PowerShell</span></span>
<span data-ttu-id="ebfc5-133"><a name="pshellsafetytip"> </a></span><span class="sxs-lookup"><span data-stu-id="ebfc5-133"></span></span>

<span data-ttu-id="ebfc5-134">Os administradores podem usar o PowerShell do Exchange Online para habilitar ou desabilitar dicas de segurança.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-134">Admins can use Exchange Online PowerShell to enable or disable safety tips.</span></span> <span data-ttu-id="ebfc5-135">Use o cmdlet Set-HostedContentFilterPolicy para habilitar ou desabilitar dicas de segurança em uma política de filtro de spam.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-135">Use the Set-HostedContentFilterPolicy cmdlet to enable or disable safety tips in a spam filter policy.</span></span>
  
1. <span data-ttu-id="ebfc5-136">Conectar-se ao Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-136">Connect to Exchange Online PowerShell.</span></span> <span data-ttu-id="ebfc5-137">Para saber mais, confira [conectar-se ao PowerShell do Exchange Online](http://go.microsoft.com/fwlink/p/?LinkId=396554).</span><span class="sxs-lookup"><span data-stu-id="ebfc5-137">For information, see [Connect to Exchange Online PowerShell](http://go.microsoft.com/fwlink/p/?LinkId=396554).</span></span>
    
2. <span data-ttu-id="ebfc5-138">Execute o cmdlet Set-HostedContentFilterPolicy para habilitar ou desabilitar dicas de segurança:</span><span class="sxs-lookup"><span data-stu-id="ebfc5-138">Run the Set-HostedContentFilterPolicy cmdlet to enable or disable safety tips:</span></span>
    
  ```
  Set-HostedContentFilterPolicy -Identity "policy name " -InlineSafetyTipsEnabled <$true|$false>
  ```

<span data-ttu-id="ebfc5-139">Em que:</span><span class="sxs-lookup"><span data-stu-id="ebfc5-139">Where:</span></span>
    
  -  <span data-ttu-id="ebfc5-140">*nome da política* é o nome da política que você deseja modificar, por exemplo, **padrão**.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-140">*policy name*  is the name of the policy you want to modify, for example **default**.</span></span>
    
  -  <span data-ttu-id="ebfc5-141">`$true`permite dicas de segurança para a política de filtro de spam.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-141">`$true` enables safety tips for the spam filter policy.</span></span> 
    
  -  <span data-ttu-id="ebfc5-142">`$false`desabilita as dicas de segurança da política de filtro de spam.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-142">`$false` disables safety tips for the spam filter policy.</span></span> 
    
    <span data-ttu-id="ebfc5-143">Por exemplo, para desabilitar as dicas de segurança para a política de filtro de spam padrão, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="ebfc5-143">For example, to disable safety tips for the default spam filter policy, run the following command:</span></span>
    
  ```
  PS C:\> Set-HostedContentFilterPolicy -Identity "default" -InlineSafetyTipsEnabled $false
  ```

<span data-ttu-id="ebfc5-144">Para obter mais informações sobre esse cmdlet, consulte [set-HostedContentFilterPolicy](https://technet.microsoft.com/library/jj200781.aspx).</span><span class="sxs-lookup"><span data-stu-id="ebfc5-144">For more information about this cmdlet, see [Set-HostedContentFilterPolicy](https://technet.microsoft.com/library/jj200781.aspx).</span></span>
    
## <a name="still-need-help"></a><span data-ttu-id="ebfc5-145">Ainda precisa de ajuda?</span><span class="sxs-lookup"><span data-stu-id="ebfc5-145">Still need help?</span></span>
<span data-ttu-id="ebfc5-146"><a name="pshellsafetytip"> </a></span><span class="sxs-lookup"><span data-stu-id="ebfc5-146"></span></span>

<span data-ttu-id="ebfc5-147">Se você desabilitou as dicas de segurança, mas ainda as está vendo nas mensagens de email, Confira estas coisas:</span><span class="sxs-lookup"><span data-stu-id="ebfc5-147">If you disabled safety tips but are still seeing them in your email messages, check these things:</span></span>
  
- <span data-ttu-id="ebfc5-148">Não é possível desabilitar dicas de segurança para o Outlook na Web.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-148">You can't disable safety tips for Outlook on the web.</span></span> <span data-ttu-id="ebfc5-149">Tente exibir o mesmo email em outro cliente, como o Outlook.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-149">Try viewing the same email in another client, such as Outlook.</span></span>
    
- <span data-ttu-id="ebfc5-150">As dicas de segurança são ativadas por padrão para todos os usuários que usam o EOP, incluindo todos os que têm o Office 365.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-150">Safety tips are on by default for every one who uses EOP, this includes everyone who has Office 365.</span></span> <span data-ttu-id="ebfc5-151">Para desabilitar as dicas de segurança da exibição no email, você deve desabilitá-las usando uma política de filtro de spam, conforme descrito neste tópico.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-151">In order to disable safety tips from showing up in email, you must disable them by using a spam filter policy as described in this topic.</span></span> <span data-ttu-id="ebfc5-152">Depois de configurar a política, verifique se ela está habilitada.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-152">Once you've set up the policy, ensure that it is enabled.</span></span> <span data-ttu-id="ebfc5-153">Para obter informações sobre como habilitar políticas de filtro de spam, consulte [Configure Your spam filter Policies](https://technet.microsoft.com/library/jj200684.aspx).</span><span class="sxs-lookup"><span data-stu-id="ebfc5-153">For information on enabling spam filter policies, see [Configure your spam filter policies](https://technet.microsoft.com/library/jj200684.aspx).</span></span>
    
<span data-ttu-id="ebfc5-154">Para obter mais maneiras de combater spam e phishing, consulte [Office 365 email anti-spam Protection](anti-spam-protection.md).</span><span class="sxs-lookup"><span data-stu-id="ebfc5-154">For more ways to combat spam and phishing, see [Office 365 Email Anti-Spam Protection](anti-spam-protection.md).</span></span>
  


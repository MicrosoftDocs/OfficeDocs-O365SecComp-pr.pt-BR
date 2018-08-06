---
title: Perguntas frequentes sobre administração delegada
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: d6a87ce8-2c22-433a-b430-5eab14f6afdc
description: Este tópico fornece perguntas frequentes e suas respostas para parceiros e revendedores Microsoft que desejam executar tarefas de administração delegadas do Office 365, incluindo a habilidade de gerenciar o Exchange Online Protection (EOP) para outros locatários (empresas).
ms.openlocfilehash: b6096e835f90a0d5f22a39a5df76e52f1a25a79d
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027488"
---
# <a name="delegated-administration-faq"></a><span data-ttu-id="b2366-103">Perguntas frequentes sobre administração delegada</span><span class="sxs-lookup"><span data-stu-id="b2366-103">Delegated administration FAQ</span></span>

<span data-ttu-id="b2366-104">Este tópico fornece perguntas frequentes e suas respostas para parceiros e revendedores Microsoft que desejam executar tarefas de administração delegadas do Office 365, incluindo a habilidade de gerenciar o Exchange Online Protection (EOP) para outros locatários (empresas).</span><span class="sxs-lookup"><span data-stu-id="b2366-104">This topic provides frequently asked questions and answers for Microsoft partners and resellers who want to perform delegated Office 365 administration tasks, including the ability to manage Exchange Online Protection (EOP) for other tenants (companies).</span></span>
  
 <span data-ttu-id="b2366-105">**P. Sou revendedor e preciso gerenciar os locatários do meu cliente. Como isso funciona?**</span><span class="sxs-lookup"><span data-stu-id="b2366-105">**Q. I'm a reseller and I need to manage my customer's tenants; how does this work?**</span></span>
  
<span data-ttu-id="b2366-p101">R. Se você é um parceiro ou revendedor Microsoft e se inscreveu para ser um consultor Microsoft, você pode solicitar permissão para administrar os locatários no Centro de administração do Office 365. Isso é conhecido como administração delegada e permite que você gerencie os locatários do Office 365 (incluindo configurações de EOP) como se você fosse um administrador dentro da organização deles. Veja a seguir as etapas para execução da administração delegada:</span><span class="sxs-lookup"><span data-stu-id="b2366-p101">A. If you are a Microsoft partner or reseller, and you've signed up to be a Microsoft advisor, you can request permission to administer their tenant within the Office 365 admin center. This is known as delegated administration, and it allows you to manage their Office 365 tenant (including EOP settings) as if you were an administrator within their organization. The steps for performing delegated administration are as follows:</span></span>
  
1. <span data-ttu-id="b2366-110">Inscreva-se para ser um [Consultor do Microsoft Office 365](https://aka.ms/cloudbenefits).</span><span class="sxs-lookup"><span data-stu-id="b2366-110">Sign up to be a [Microsoft Office 365 Advisor](https://aka.ms/cloudbenefits).</span></span>
    
2. <span data-ttu-id="b2366-p102">Inscreva-se para a administração delegada do Office 365. Para que você possa começar a administrar a conta de um cliente, ele deverá autorizá-lo como um administrador delegado. Para obter a aprovação dele, é necessário [enviar primeiro uma oferta para administração delegada](https://go.microsoft.com/fwlink/?LinkId=396829). (Você também pode oferecer posteriormente a administração delegada ao seu cliente.)</span><span class="sxs-lookup"><span data-stu-id="b2366-p102">Sign up for Office 365 delegated administration. Before you can start administering a customer's account, they must authorize you as a delegated administrator. To obtain their approval, you first [send them an offer for delegated administration](https://go.microsoft.com/fwlink/?LinkId=396829). (You can also offer delegated administration to your customer at a later time.)</span></span> 
    
3. <span data-ttu-id="b2366-115">Crie a conta de administração delegada usando as etapas documentadas em [Adicionar ou excluir uma administração delegada](https://go.microsoft.com/fwlink/?LinkId=396831).</span><span class="sxs-lookup"><span data-stu-id="b2366-115">Create the delegated admin account using the steps documented in [Add or delete a delegated admin](https://go.microsoft.com/fwlink/?LinkId=396831).</span></span>
    
<span data-ttu-id="b2366-116">Visite [Parceiros: construa seu negócio e administre sua conta de parceiro do Office 365](https://go.microsoft.com/fwlink/?LinkId=301485) para obter mais informações sobre como configurar a administração delegada do Office 365.</span><span class="sxs-lookup"><span data-stu-id="b2366-116">Visit [Partners: Build your business and administer your Office 365 partner account](https://go.microsoft.com/fwlink/?LinkId=301485) for more information about how to set up Office 365 delegated administration.</span></span> 
  
 <span data-ttu-id="b2366-117">**P. Sou um cliente, não é um revendedor, como posso configurar o administrador delegado para meus sublocatários?**</span><span class="sxs-lookup"><span data-stu-id="b2366-117">**Q. I'm a customer, not a reseller, how can set up delegated administrator for my sub-tenants?**</span></span>
  
<span data-ttu-id="b2366-p103">R. A administração delegada só está disponível para parceiros e revendedores no momento. No entanto, fornecemos um script de amostra do Windows PowerShell que ajudará você a aplicar políticas aos seus sublocatários (empresas). Para obter mais informações, consulte [Amostra de script para aplicação de configurações de EOP a vários locatários](sample-script-for-applying-eop-settings-to-multiple-tenants.md).</span><span class="sxs-lookup"><span data-stu-id="b2366-p103">A. Delegated administration is only available for resellers and partners at this time. However, we've provided a sample Windows PowerShell script that will help you apply policies to your sub-tenants (companies). For more information, see [Sample script for applying EOP settings to multiple tenants](sample-script-for-applying-eop-settings-to-multiple-tenants.md).</span></span>
  
 <span data-ttu-id="b2366-122">**P. Posso impedir que a administração de sublocatário modifique minha política?**</span><span class="sxs-lookup"><span data-stu-id="b2366-122">**Q. Can I prevent my sub-tenant admin from modifying my policy?**</span></span>
  
<span data-ttu-id="b2366-p104">R. O Office 365 não tem esse recurso no momento.</span><span class="sxs-lookup"><span data-stu-id="b2366-p104">A. Office 365 does not currently have this capability.</span></span>
  
 <span data-ttu-id="b2366-125">**P. Posso obter um relatório consolidado em todos os meus sublocatários?**</span><span class="sxs-lookup"><span data-stu-id="b2366-125">**Q. Can I get consolidated reporting across all of my sub-tenants?**</span></span>
  
<span data-ttu-id="b2366-p105">R. Os relatórios consolidados entre as empresas que você gerencia não estão disponíveis para os relatórios do Centro de administração do Office 365 no momento. No entanto, isso pode ser feito por meio do Windows PowerShell remoto ou do [serviço Web de relatório](https://go.microsoft.com/fwlink/?LinkId=279926).</span><span class="sxs-lookup"><span data-stu-id="b2366-p105">A. Consolidated reporting across the companies you manage is not available for the Office 365 admin center reports at this time. However, this can be done via remote Windows PowerShell or the [reporting web service](https://go.microsoft.com/fwlink/?LinkId=279926).</span></span> 
  


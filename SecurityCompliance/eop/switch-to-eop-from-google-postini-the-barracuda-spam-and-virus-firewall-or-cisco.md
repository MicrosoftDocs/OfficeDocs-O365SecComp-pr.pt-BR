---
title: Mudando para EOP da Google Postini, Firewall de Vírus ou Spam Barracuda ou Cisco IronPort
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 81b75194-3b04-48da-8b81-951afbabedde
description: O objetivo deste tópico é ajudar você a entender o processo de optar pelo Exchange Online Protection (EOP) a partir de um serviço de proteção na nuvem ou ferramenta de higienização de email local e então oferecer recursos de ajuda para começar.
ms.openlocfilehash: 0c33d89be5cb4ebf7719e6742532ebfc7a2e5c20
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32256199"
---
# <a name="switch-to-eop-from-google-postini-the-barracuda-spam-and-virus-firewall-or-cisco-ironport"></a>Mudando para EOP da Google Postini, Firewall de Vírus ou Spam Barracuda ou Cisco IronPort

 O objetivo deste tópico é ajudar você a entender o processo de optar pelo Exchange Online Protection (EOP) a partir de um serviço de proteção na nuvem ou ferramenta de higienização de email local e então oferecer recursos de ajuda para começar. Existem muitas soluções de filtragem de spam, mas o processo de alterar para EOP é similar na maioria dos casos.
  
Se você é novo no EOP e deseja ler uma visão geral dos seus recursos antes de decidir pela troca, inicie com o [Visão geral do Exchange Online Protection](exchange-online-protection-overview.md) no TechNet. 
  
Antes de mudar para EOP, é importante que você decida se deseja hospedar as suas caixas de correio protegias pelo EOP na nuvem, com o Exchange Online, localmente ou em um cenário híbrido. (Hybrid significa que você tem algumas caixas de correio hospedadas no local e outra parte hospedado com o Exchange Online.) Cada um desses cenários de hospedagem: nuvem, no local, e híbrido, é possível, mas as etapas de configuração podem variar. Aqui estão algumas considerações para ajudar você a escolher a implantação apropriada:
  
- **EOP protection with on-premises mailboxes** This scenario is appropriate if you have existing mail-hosting infrastructure you want to use, or you have business requirements to keep mailboxes on-premises, and you want EOP's cloud-based email protection. [Switch to EOP standalone](#switch-to-eop-standalone) describes this scenario in more detail. 
    
- **EOP protection with Exchange Online mailboxes** This scenario is appropriate if you want EOP protection and all of your mailboxes hosted in the cloud. It can help you reduce complexity, because you don't have to maintain on-premises messaging servers. [Switch to Exchange Online](switch-to-eop-from-google-postini-the-barracuda-spam-and-virus-firewall-or-cisco.md#BKMK_SwitchEXO) describes this scenario. 
    
- **EOP protection with hybrid mailboxes** Perhaps you want cloud mailboxes, but you need to keep mailboxes for some users on-premises. Choose this scenario if you want some mailboxes hosted on-premises and another portion hosted with Exchange Online. [Switch to a hybrid solution](#switch-to-a-hybrid-solution) describes this scenario. 
    
## <a name="switch-to-eop-standalone"></a>Mudar para EOP standalone

Se você atualmente hospeda as suas caixas de correio localmente e use uma ferramenta de proteção local ou um serviço de proteção de mensagem na nuvem, você pode mudar para EOP para tirar vantagem dos seus recursos de proteção e disponibilidade. Para instalar o EOP em um cenário autônomo, o que significa que você hospeda as suas caixas de correio localmente e usa o EOP para fornecer proteção de email, você pode seguir as etapas destacadas em [Configurar seu serviço EOP](set-up-your-eop-service.md). O tópico destaca as etapas para instalar a proteção EOP, incluindo se inscrever, adicionar o seu domínio e configurar o fluxo de email com conectores.
  
## <a name="switch-to-exchange-online"></a>Mude para o Exchange Online
<a name="BKMK_SwitchEXO"> </a>

Talvez você tenha caixas de correio locais protegidos por um aparelho no local, e você quer ir para Exchange Online caixas de correio em nuvem hospedados e proteção EOP para aproveitar Office 365 Mensagens de nuvem e recursos de proteção. Para começar, você pode inscrever-se no Office 365 e adicionar o seu domínio. Este cenário não exige que você instale conectores, porque nao há nenhum roteamento para caixas de correio locais. Comece na [Página de inscrição no Office 365](https://www.microsoft.com/en-us/office365/online-software.aspx). ([ Comece a trabalhar com o Office 365 ](https://go.microsoft.com/fwlink/p/?LinkId=275407) fornece recursos para se familiarizar com as suas características.) 
  
Durante o processo de instalação do Office 365 , você criará usuários de caixa de correio baseados na nuvem.
  
## <a name="switch-to-a-hybrid-solution"></a>Mudar para uma solução híbrida
<a name="BKMK_SwitchHybrid"> </a>

Você pode querer mover apenas uma porção das suas caixas de correio para a nuvem por causa de considerações regulatórias ou de requisitos de negócio. Quando você implanta um cenário híbrido, você pode mover as caixas de correio para a nuvem conforme determinação dos requisitos do seu negócio. Migrar para um cenário híbrido com proteção EOP é mais complicado do que mover para um cenário completamente na nuvem, mas a Microsoft fornece suporte total e amplos recursos para facilitar a mudança para um cenário híbrido.
  
O melhor lugar para começar, se você está considerando uma implantação híbrida, é [Exchange Server 2013 Hybrid Deployments](http://technet.microsoft.com/library/59e32000-4fcf-417f-a491-f1d8f9aeef9b.aspx). Além disso, existem algumas maneiras diferentes de você rotear o seu email em um cenário híbrido que é importante que você entenda. [Transport Routing in Exchange 2013 Hybrid Deployments](http://technet.microsoft.com/library/36c2cea3-2e2f-40ac-88bd-7e1b6bd27828.aspx) explica cada tipo, assim você pode escolher o melhor cenário de roteamento, com base em suas necessidades empresariais. 
  
## <a name="migration-planning"></a>Planejamento de migração
<a name="sectionSection3"> </a>

Quando você decide mudar para EOP, certifique-se de que você está considerando especialmente as seguintes áreas:
  
- **Custom Filtering Rules** If you have custom filtering or business-policy rules to catch specific spam, we recommend that you try EOP with the default settings for a period, before you migrate your rules. EOP offers enterprise-level spam protection with the default settings, it may turn out that you don't need to migrate some of your rules to EOP. Of course, if you have rules in place that enforce specific custom business policies, you can create those. [Regras de fluxo de email (regras de transporte) no Exchange Online Protection](mail-flow-rules-transport-rules-0.md) fornece instruções detalhadas para a criação de regras de fluxo de email no EOP. 
    
- **IP allow lists and IP block lists** If you have per-user allow lists and block lists, allow some time to copy the lists to EOP as part of your setup process. Para obter mais informações sobre listas de IPs permitidos e listas de bloqueios de IP, consulte [Configurar a política de filtro de conexão](../configure-the-connection-filter-policy.md).
    
- **Secure Communication** If you have a partner that requires encrypted messaging, we recommend that you set this up in the Exchange admin center. To configure this scenario, see [Create connectors for a secure mail channel using transport layer security (TLS)](http://technet.microsoft.com/library/1ce4d6a4-41ba-4d1e-9ca9-e826252c1041.aspx).
    
> [!TIP]
> Quando você mudar de uma ferramenta local para EOP, é possível deixar a sua ferramenta ou um servidor preparado para realizar as verificações de regra de negócio. Por exemplo, se a sua ferramenta realiza filtragem personalizada no email de saída e você deseja que isso continue sendo feito, você pode configurar o EOP para enviar email diretamente para a ferramenta para uma filtragem adicional antes que o mesmo seja roteado para a Internet. [Exchange Online Protection Connectors - Outbound Smart Host Scenario](http://technet.microsoft.com/library/431b3f02-4efd-4bd3-94e7-eecd03f8ef5e.aspx) mostra como configurar o fluxo de mensagens nesse caso. 
  


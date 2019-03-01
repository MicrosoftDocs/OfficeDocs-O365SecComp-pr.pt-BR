---
title: Mudando para EOP da Google Postini, Firewall de Vírus ou Spam Barracuda ou Cisco IronPort
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 81b75194-3b04-48da-8b81-951afbabedde
description: O objetivo deste tópico é ajudar você a entender o processo de optar pelo Exchange Online Protection (EOP) a partir de um serviço de proteção na nuvem ou ferramenta de higienização de email local e então oferecer recursos de ajuda para começar.
ms.openlocfilehash: a1fa7b63dfc1e6eb193d458545722c4b5331bc48
ms.sourcegitcommit: 48fa456981b5c52ab8aeace173c8366b9f36723b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/28/2019
ms.locfileid: "30340752"
---
# <a name="switch-to-eop-from-google-postini-the-barracuda-spam-and-virus-firewall-or-cisco-ironport"></a>Mudando para EOP da Google Postini, Firewall de Vírus ou Spam Barracuda ou Cisco IronPort

 O objetivo deste tópico é ajudar você a entender o processo de optar pelo Exchange Online Protection (EOP) a partir de um serviço de proteção na nuvem ou ferramenta de higienização de email local e então oferecer recursos de ajuda para começar. Existem muitas soluções de filtragem de spam, mas o processo de alterar para EOP é similar na maioria dos casos.
  
Se você é novo no EOP e deseja ler uma visão geral dos seus recursos antes de decidir pela troca, inicie com o [Visão geral do Exchange Online Protection](exchange-online-protection-overview.md) no TechNet. 
  
Antes de mudar para EOP, é importante que você decida se deseja hospedar as suas caixas de correio protegias pelo EOP na nuvem, com o Exchange Online, localmente ou em um cenário híbrido. (Hybrid significa que você tem algumas caixas de correio hospedadas no local e outra parte hospedado com o Exchange Online.) Cada um desses cenários de hospedagem: nuvem, no local, e híbrido, é possível, mas as etapas de configuração podem variar. Aqui estão algumas considerações para ajudar você a escolher a implantação apropriada:
  
- **Proteção do EOP com caixas de correio locais** Esse cenário será apropriado se você tiver uma infraestrutura de Hospedagem de emails existente que você deseja usar ou se tiver requisitos de negócios para manter as caixas de correio locais e quiser a proteção de email baseada em nuvem do EOP. [Alternar para EOP autônomo](#BKMK_SwitchStandalone.md) descreve esse cenário em mais detalhes. 
    
- **Proteção do EOP com caixas de correio do Exchange Online** Este cenário será apropriado se você quiser proteção do EOP e todas as suas caixas de correio hospedadas na nuvem. Ele pode ajudá-lo a reduzir a complexidade, porque você não precisa manter os servidores de mensagens locais. [Mudar para o Exchange Online](switch-to-eop-from-google-postini-the-barracuda-spam-and-virus-firewall-or-cisco.md#BKMK_SwitchEXO) descreve esse cenário. 
    
- **Proteção do EOP com caixas de correio híbridas** Talvez você queira as caixas de correio na nuvem, mas precisa manter caixas de correio para alguns usuários no local. Escolha este cenário se quiser algumas caixas de correio hospedadas no local e outra parte hospedada com o Exchange Online. [Alternar para uma solução híbrida](#BKMK_SwitchHybrid.md) descreve esse cenário. 
    
## <a name="switch-to-eop-standalone"></a>Mudar para EOP standalone
<a name="BKMK_SwitchStandalone"> </a>

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
  
- **Regras de filtragem personalizadas** Se você tiver regras de filtro ou política de negócios personalizadas para detectar spam específico, recomendamos que tente EOP com as configurações padrão para um período, antes de migrar suas regras. O EOP oferece proteção de spam de nível empresarial com as configurações padrão, pode ser que você não precise migrar algumas de suas regras para o EOP. Obviamente, se você tiver regras no local que imponham políticas de negócios personalizadas específicas, você poderá criá-las. [Regras de fluxo de email (regras de transporte) no Exchange Online Protection](mail-flow-rules-transport-rules-0.md) fornece instruções detalhadas para a criação de regras de fluxo de email no EOP. 
    
- Listas **de IPs permitidos e listas de IPs bloqueados** Se você tiver listas de permissões e listas de bloqueio por usuário, aguarde algum tempo para copiar as listas para o EOP como parte do processo de instalação. Para obter mais informações sobre listas de IPs permitidos e listas de bloqueios de IP, consulte [Configurar a política de filtro de conexão](../configure-the-connection-filter-policy.md).
    
- **Comunicação segura** Se você tiver um parceiro que exija mensagens criptografadas, recomendamos que você configure isso no centro de administração do Exchange. Para configurar esse cenário, consulte [Create Connectors for a Secure Mail Channel using Transport Layer Security (TLS)](http://technet.microsoft.com/library/1ce4d6a4-41ba-4d1e-9ca9-e826252c1041.aspx).
    
> [!TIP]
> Quando você mudar de uma ferramenta local para EOP, é possível deixar a sua ferramenta ou um servidor preparado para realizar as verificações de regra de negócio. Por exemplo, se a sua ferramenta realiza filtragem personalizada no email de saída e você deseja que isso continue sendo feito, você pode configurar o EOP para enviar email diretamente para a ferramenta para uma filtragem adicional antes que o mesmo seja roteado para a Internet. [Exchange Online Protection Connectors - Outbound Smart Host Scenario](http://technet.microsoft.com/library/431b3f02-4efd-4bd3-94e7-eecd03f8ef5e.aspx) mostra como configurar o fluxo de mensagens nesse caso. 
  


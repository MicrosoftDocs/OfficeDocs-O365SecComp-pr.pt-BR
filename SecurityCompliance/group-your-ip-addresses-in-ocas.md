---
title: Agrupar seus endereços IP para simplificar o gerenciamento do Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/28/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: b5e1471c-1ad6-4bc5-9e75-ce791aee283c
description: Para identificar facilmente conjuntos de endereços IP que você usará no Office 365 Cloud app Security, como seus endereços IP do Office físico, você pode configurar grupos de intervalos de endereços IP.
ms.openlocfilehash: b8f5c1dd46b2e3990d53a65881d12ca8f3961b16
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32254850"
---
# <a name="group-your-ip-addresses-to-simplify-management-in-office-365-cloud-app-security"></a>Agrupar seus endereços IP para simplificar o gerenciamento do Office 365 Cloud App Security
  
|Avaliação * *\>**|Planejamento * *\>**|Implantação * *\>**|Utilização * * *|
|:-----|:-----|:-----|:-----|
|[Iniciar avaliação](office-365-cas-overview.md) <br/> |[Iniciar planejamento](get-ready-for-office-365-cas.md) <br/> |Você está aqui!  <br/> [Próximas etapas](#next-steps) <br/> |[Começar a usar](utilization-activities-for-ocas.md) <br/> |
   
Para identificar facilmente conjuntos de endereços IP que você usará no Office 365 Cloud app Security, como seus endereços IP do Office físico, você pode configurar grupos de intervalos de endereços IP. A definição desses intervalos permite marcá-los e categorizá-los e, em seguida, você pode usar marcas e categorias para personalizar como seus logs de atividade e alertas são exibidos e investigados.
  
Cada grupo de intervalos IP pode ser marcado com nomes de marca que você escolhe e, em seguida, as marcas podem ser categorizadas com base em uma lista padrão de categorias de IP (como corporações, administrativas, arriscadas e VPN). Há suporte para os endereços IPv4 e IPv6.
  
> [!NOTE]
> Você deve ser um administrador global ou administrador de segurança para executar os procedimentos deste artigo. Para saber mais, confira [permissões no centro de conformidade &amp; de segurança do Office 365](permissions-in-the-security-and-compliance-center.md). 
  
## <a name="to-set-up-an-ip-address-range-in-office-365-cloud-app-security"></a>Para configurar um intervalo de endereços IP no Office 365 Cloud app Security

1. Como administrador global ou administrador de segurança, vá para o portal do Cloud app Security[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)() e entre.
    
2. No canto superior direito da página, clique em **configurações** \> de **intervalos de endereços IP**.<br>![No O365 Cloud app Security, escolha configurações para acessar o sistema e as configurações de dados](media/f6c48ee3-39b4-4b5a-8252-b6493b7bcd3d.png)<br>
  
3. Clique no botão novo, que se assemelha a um sinal de **+** mais ().
    
4. Na janela **novo intervalo de endereços IP** , especifique os seguintes valores: 
    
|**Campo ou lista**|**O que fazer**|
|:-----|:-----|
|**Nome** <br/> |Use este campo para gerenciar o intervalo de endereços IP e as configurações. (Esse valor não será exibido nos logs de atividades.)  <br/> |
|**Intervalos de endereços IP** <br/> |Especifique um intervalo, usando a notação de prefixo de rede (também conhecida como notação CIDR). Por exemplo, 192.168.1.0/27 inclui o intervalo de valores 192.168.1.0 a 192.168.1.31 (inclusive).  <br/> |
|**Local** e **ISP registrado** <br/> |Especifique o local e o provedor de serviços de Internet (ISP) para o intervalo de endereços IP. Isso substitui os campos públicos definidos para os endereços, o que é útil para casos, como um endereço IP é considerado público para estar na Irlanda, mas na verdade nos EUA.  <br/> |
|**Marcas** <br/> |Use marcas para nomear seus grupos de endereços IP. (Ao contrário do campo nome, você verá marcas nos logs de atividades.) Digite uma palavra ou frase que você deseja usar para uma marca. Você pode adicionar quantas marcas quiser para cada intervalo de endereços IP. E se você já configurou uma marca e deseja adicionar esse intervalo de endereços IP a ela, escolha-a na lista de marcas atuais que aparece ao começar a digitar.  <br/> |
|**Categoria** <br/> | Atribua categorias às suas marcas para facilitar o reconhecimento de atividades provenientes de determinados endereços IP. Escolha uma das seguintes opções:  <br/> **Administrativo** Todos os endereços IP de seus administradores.  <br/> **Provedor de nuvem** O endereço IP do seu proxy na nuvem.  <br/> **Corporativo** Todos os endereços IP na sua rede interna, suas filiais e seus endereços de roaming de Wi-Fi.  <br/> **Arriscado** Qualquer endereço IP que você considere como um risco, como endereços IP suspeitos que você viu nos passados, endereços IP nas redes dos concorrentes e assim por diante. Por padrão, as categorias arriscadas incluem duas marcas de IP: **proxy anônimo** e **Tor** <br/> **VPN** Qualquer endereço IP que seus funcionários remotos utilizam.  <br/> |
   
7. Selecione **Salvar**.
    
Depois de configurar os intervalos de endereços IP, lembre-se de que apenas eventos futuros serão afetados por essas alterações.
  
## <a name="next-steps"></a>Próximas etapas

- [Políticas e alertas de atividade](activity-policies-and-alerts.md)
    
- [Políticas de detecção de anomalias](anomaly-detection-policies-in-ocas.md)
    
- [Integrar seu servidor SIEM](integrate-your-siem-server-with-office-365-cas.md)
    
- [Revisar e tomar atitudes sobre alertas no Office 365 Cloud App Security](review-office-365-cas-alerts.md)
    


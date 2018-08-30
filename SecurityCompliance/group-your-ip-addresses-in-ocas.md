---
title: Agrupar seus endereços IP para simplificar o gerenciamento do Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/22/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: b5e1471c-1ad6-4bc5-9e75-ce791aee283c
description: Para identificar facilmente os conjuntos de endereços IP que você usará na segurança de aplicativo de nuvem do Office 365, como seus endereços IP do escritório físico, você pode configurar grupos de intervalos de endereços IP.
ms.openlocfilehash: 76cb9625a46d1f5eceaab696de5dcbb72f4d2b47
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523476"
---
# <a name="group-your-ip-addresses-to-simplify-management-in-office-365-cloud-app-security"></a>Agrupar seus endereços IP para simplificar o gerenciamento do Office 365 Cloud App Security
  
|Avaliação * *\>**|Planejamento * *\>**|Implantação * *\>**|Utilização * * *|
|:-----|:-----|:-----|:-----|
|[Comece a avaliar](office-365-cas-overview.md) <br/> |[Começar a planejar](get-ready-for-office-365-cas.md) <br/> |Você está aqui!  <br/> [Próximas etapas](#next-steps) <br/> |[Iniciar a utilização](utilization-activities-for-ocas.md) <br/> |
   
Para identificar facilmente os conjuntos de endereços IP que você usará na segurança de aplicativo de nuvem do Office 365, como seus endereços IP do escritório físico, você pode configurar grupos de intervalos de endereços IP. Definindo permite esses intervalos você marca e categorizá-las e, em seguida, você pode usar marcas e categorias para personalizar como sua atividade logs e os alertas são exibidas e investigadas.
  
Cada grupo de intervalos de IP pode ser identificado com nomes de marca que você escolhe, e, em seguida, as marcas podem ser categorizadas com base em uma lista padrão de categorias IP (por exemplo, Corporate, administrativos, Risky e VPN). Há suporte para endereços IPv4 e IPv6.
  
> [!NOTE]
> Você deve ser um administrador global ou administrador de segurança para executar os procedimentos neste artigo. Para saber mais, consulte [permissões no Office 365 Security &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md). 
  
## <a name="to-set-up-an-ip-address-range-in-office-365-cloud-app-security"></a>Para configurar um intervalo de endereços IP na segurança de aplicativo de nuvem do Office 365

1. Como administrador global ou administrador de segurança, vá para [https://protection.office.com](https://protection.office.com) e entrar usando sua conta do trabalho ou da escola. (Isso leva você para a segurança &amp; Centro de conformidade.) 
    
2. Na segurança &amp; Centro de conformidade, escolha **alertas** \> **avançadas de gerenciar alertas**.
    
3. Escolha **vá para segurança de aplicativo do Office 365 nuvem**.
    
    ![Na segurança &amp; Centro de conformidade, escolha gerenciar alertas avançadas para ir à segurança de aplicativo de nuvem do Office 365](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)
  
4. Na parte superior direita da página, clique em **configurações** \> **intervalos de endereços IP**.
    
    ![Em segurança de aplicativo de nuvem O365, escolha configurações para acessar as configurações do sistema e dados](media/f6c48ee3-39b4-4b5a-8252-b6493b7bcd3d.png)
  
5. Clique no botão novo, que se parece com um sinal de adição ( **+**).
    
6. Na janela do **intervalo de endereços IP do novo** , especifique os seguintes valores: 
    
|**Campo ou lista**|**O que fazer**|
|:-----|:-----|
|**Nome** <br/> |Use este campo para gerenciar as configurações e do intervalo de endereços IP. (Você não verá esse valor nos logs de atividades).  <br/> |
|**Intervalos de endereços IP** <br/> |Especifique um intervalo, usando a notação de prefixo de rede (também conhecido como notação CIDR). Por exemplo, 192.168.1.0/27 inclui o intervalo de valores 192.168.1.0 por meio de 192.168.1.31 (inclusive).  <br/> |
|**Local** e **registrados ISP** <br/> |Especifique o local e o provedor de serviços de Internet (ISP) para o intervalo de endereços IP. Isso substitui os campos públicos definidos para os endereços, que é útil para casos, como um endereço IP é o que é considerado publicamente na Irlanda, mas é realmente nos EUA  <br/> |
|**Tags** <br/> |Use marcas para nomear os grupos de endereços IP. (Ao contrário do campo nome, você verá marcas nos logs de atividade.) Digite uma palavra ou frase que você deseja usar para uma marca. Você pode adicionar quantas marcas desejar para cada intervalo de endereços IP. E se você já configurou uma marca e você deseja adicionar esse intervalo de endereços IP a ele, escolha da lista de marcas atuais que aparecem conforme você começa a digitar.  <br/> |
|**Categoria** <br/> | Atribua categorias a suas marcas para facilitar a reconhecer atividades que vêm de certos endereços IP. Escolha entre as seguintes opções:<br/> **Administrativas** Todos os endereços IP do seus grupo Administradores.  <br/> **Provedor de nuvem** O endereço IP do seu proxy na nuvem.  <br/> **Corporativo** Todos o endereços IP na sua rede interna, suas filiais e seus endereços de roaming Wi-Fi.  <br/> **Riscado** Qualquer endereço IP que você considera riscado, como os endereços de IP de suspeito você visto no passado, endereços IP nas redes de concorrentes e assim por diante. Por padrão, as categorias riscadas inclui duas marcas IP: **proxy anônimo** e **Tor** <br/> **VPN** Os endereços IP que usam seus funcionários remotos.  <br/> |
   
7. Escolha **Salvar**.
    
Depois de configurar seus intervalos de endereços IP, lembre-se de que apenas futuros eventos são afetados por essas alterações.
  
## <a name="next-steps"></a>Próximas etapas

- [Alertas e políticas de atividade](activity-policies-and-alerts.md)
    
- [Políticas de detecção de anomalia](anomaly-detection-policies-in-ocas.md)
    
- [Integrar seu servidor SIEM](integrate-your-siem-server-with-office-365-cas.md)
    
- [Revisar e tomar atitudes sobre alertas no Office 365 Cloud App Security](review-office-365-cas-alerts.md)
    


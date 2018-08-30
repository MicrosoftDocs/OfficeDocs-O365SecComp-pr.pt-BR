---
title: Logs do tráfego da Web e fontes de dados do Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/26/2018
ms.audience: ITPro
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 290b02bf-a988-4fb9-88b2-34e408216ac8
description: O Office 365 segurança de aplicativo de nuvem trabalha com logs de tráfego da web a partir de uma ampla gama de provedores. Leia este artigo para saber mais sobre logs de tráfego da web e suporte a fontes de dados para segurança de aplicativo de nuvem do Office 365.
ms.openlocfilehash: 09b0358e0d8b9a6ed59393d8771237f7eaf8bb98
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524150"
---
# <a name="web-traffic-logs-and-data-sources-for-office-365-cloud-app-security"></a>Logs do tráfego da Web e fontes de dados do Office 365 Cloud App Security
  
|Avaliação * *\>**|Planejamento * *\>**|Implantação * *\>**|Utilização * * *|
|:-----|:-----|:-----|:-----|
|[Comece a avaliar](office-365-cas-overview.md) <br/> |[Começar a planejar](get-ready-for-office-365-cas.md) <br/> |[Começar a implantar](turn-on-office-365-cas.md) <br/> |Você está aqui!  <br/> [Próximas etapas](#next-steps) <br/> |
  
Você pode usar uma ampla variedade de fontes de dados e arquivos de log do tráfego de web com segurança de aplicativo de nuvem do Office 365. No entanto, seus arquivos de log do tráfego da web devem incluir informações específicas e ser formatados de uma maneira para que eles funcionem com relatórios de descoberta de aplicativo de segurança de aplicativo de nuvem do Office 365 e o painel de descoberta de nuvem. Use este artigo como um guia de referência para os logs de tráfego da web e fontes de dados que você usará com segurança de aplicativo de nuvem do Office 365.
  
> [!NOTE]
> Você deve ser um administrador global, administrador de segurança ou leitor de segurança para acessar a segurança &amp; portal do Centro de conformidade e segurança de aplicativo de nuvem do Office 365. Consulte [Permissions in a segurança do Office 365 &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md). 
  
## <a name="web-traffic-log-requirements"></a>Requisitos de log do tráfego da Web

O Office 365 segurança de aplicativo de nuvem usa dados em logs de tráfego da web para ajudá-lo a entender quais aplicativos de pessoas em sua organização está usando. Mais detalhes são incluídos nos arquivos de log, a melhor visibilidade terá atividade do usuário.
  
A tabela a seguir lista os requisitos e os atributos necessários para logs de tráfego da web funcionar corretamente com segurança de aplicativo de nuvem do Office 365:
  
|**Atributos**|**Requisitos adicionais **|
|:-----|:-----|
| Data da transação  <br/>  IP de origem  <br/>  Usuário de origem (recomendado)  <br/>  Endereço IP de destino  <br/>  URL de destino (recomendado: URLs oferecem maior precisão para detecção de aplicativo de nuvem que endereços IP)  <br/>  Quantidade total de dados (recomendados)  <br/>  Quantidade de carregamento ou download de dados (recomendado: fornece ideias sobre nuvem padrões de uso do aplicativo)  <br/>  Ação executada (permitidas ou bloqueadas)  <br/> | Fonte de dados para os arquivos de log deve ser suportada.  <br/>  O formato de que usam os arquivos de log deve corresponder ao formato padrão. Quando o arquivo for carregado, a descoberta de aplicativo verificar isso.  <br/>  Os eventos no log de devem ocorreram não mais de 90 dias.  <br/>  O arquivo de log deve incluir as informações de tráfego de saída que podem ser analisadas para atividade de rede.  <br/> |
   
Se os atributos não estão incluídos nos logs que são carregados, segurança de aplicativo de nuvem do Office 365 não podem mostrar ou analisar as informações para você. Por exemplo, o formato de log padrão do Firewall do Cisco ASA não inclui a quantidade de bytes carregados por transação, o nome de usuário ou uma URL de destino (somente um IP de destino). Como essas informações não está nos arquivos de log Cisco, a segurança de aplicativo de nuvem do Office 365 não incluí-lo ao analisar o tráfego de rede da sua organização.
  
> [!NOTE]
> Para alguns tipos de firewalls, você deve definir um nível de informações para logs de tráfego da web incluir os atributos necessários. Por exemplo, Cisco ASA firewalls devem ter o nível de informações definida como 6. Certifique-se confirmar que os seus firewalls estão definidos para fornecer as informações corretas em logs de tráfego da web. 
  
## <a name="data-attributes-for-different-vendors"></a>Atributos de dados para diferentes fornecedores
<a name="BKMK_LogAndData"> </a>

A tabela a seguir resume as informações nos logs de tráfego da web de vários fornecedores. **Verifique com seu fornecedor para obter as informações mais recentes.**
  
|**Fonte de dados**|**URL do aplicativo de destino**|**IP de aplicativo de destino**|**Username**|**Origem IP**|**Tráfego total**|**Bytes carregados**|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|Barracuda  <br/> |**Sim** <br/> |**Sim** <br/> |**Sim** <br/> |**Sim** <br/> |Não  <br/> |Não  <br/> |
|Azul pelo  <br/> |**Sim** <br/> |Não  <br/> |**Sim** <br/> |**Sim** <br/> |**Sim** <br/> |**Sim** <br/> |
|Ponto de verificação  <br/> |Não  <br/> |**Sim** <br/> |Não  <br/> |**Sim** <br/> |Não  <br/> |Não  <br/> |
|Cisco ASA  <br/> |Não  <br/> |**Sim** <br/> |Não  <br/> |**Sim** <br/> |**Sim** <br/> |Não  <br/> |
|Cisco FWSM  <br/> |Não  <br/> |**Sim** <br/> |Não  <br/> |**Sim** <br/> |**Sim** <br/> |Não  <br/> |
|Cisco Ironport WSA  <br/> |**Sim** <br/> |**Sim** <br/> |**Sim** <br/> |**Sim** <br/> |**Sim** <br/> |**Sim** <br/> |
|Cisco Meraki  <br/> |**Sim** <br/> |**Sim** <br/> |Não  <br/> |**Sim** <br/> |Não  <br/> |Não  <br/> |
|Clavister NGFW (Syslog)  <br/> |**Sim** <br/> |**Sim** <br/> |**Sim** <br/> |**Sim** <br/> |**Sim** <br/> |**Sim** <br/> |
|SonicWall da Dell  <br/> |**Sim** <br/> |**Sim** <br/> |Não  <br/> |**Sim** <br/> |**Sim** <br/> |**Sim** <br/> |
|FortiGate  <br/> |Não  <br/> |**Sim** <br/> |Não  <br/> |**Sim** <br/> |**Sim** <br/> |**Sim** <br/> |
|Juniper SRX  <br/> |Não  <br/> |**Sim** <br/> |Não  <br/> |**Sim** <br/> |**Sim** <br/> |**Sim** <br/> |
|Juniper SSG  <br/> |Não  <br/> |**Sim** <br/> |Não  <br/> |**Sim** <br/> |**Sim** <br/> |**Sim** <br/> |
|McAfee SWG  <br/> |**Sim** <br/> |Não  <br/> |Não  <br/> |**Sim** <br/> |**Sim** <br/> |**Sim** <br/> |
|Meraki (Cisco)  <br/> |**Sim** <br/> |**Sim** <br/> |Não  <br/> |**Sim** <br/> |Não  <br/> |Não  <br/> |
|Microsoft Threat Management Gateway  <br/> |**Sim** <br/> |Não  <br/> |**Sim** <br/> |**Sim** <br/> |**Sim** <br/> |**Sim** <br/> |
|Redes Palo Alto  <br/> |**Sim** <br/> |**Sim** <br/> |**Sim** <br/> |**Sim** <br/> |**Sim** <br/> |**Sim** <br/> |
|Sophos  <br/> |**Sim** <br/> |**Sim** <br/> |**Sim** <br/> |**Sim** <br/> |**Sim** <br/> |Não  <br/> |
|Lula (comum)  <br/> |**Sim** <br/> |Não  <br/> |**Sim** <br/> |**Sim** <br/> |Não  <br/> |**Sim** <br/> |
|Lula (nativo)  <br/> |**Sim** <br/> |Não  <br/> |**Sim** <br/> |**Sim** <br/> |Não  <br/> |**Sim** <br/> |
|Websense - relatório de detalhe investigação (CSV)  <br/> |**Sim** <br/> |**Sim** <br/> |**Sim** <br/> |**Sim** <br/> |**Sim** <br/> |**Sim** <br/> |
|Websense - registro de atividade da Internet (CEF)  <br/> |**Sim** <br/> |**Sim** <br/> |**Sim** <br/> |**Sim** <br/> |**Sim** <br/> |**Sim** <br/> |
|Zscaler  <br/> |**Sim** <br/> |**Sim** <br/> |**Sim** <br/> |**Sim** <br/> |**Sim** <br/> |**Sim** <br/> |
   
## <a name="supported-vendor-firewalls-and-proxies"></a>Com suporte do fornecedor de firewalls e proxies
<a name="BKMK_Supported"> </a>

Segurança de aplicativo de nuvem do Office 365 suporta os seguintes firewalls e proxies.
  
- Barracuda - Firewall de aplicativo da Web (W3C)
    
- Azul pelo Proxy SG - log de acesso (W3C)
    
- Ponto de verificação
    
- Cisco ASA Firewall (Observe que você deve definir o nível de informações como 6)
    
- Cisco IronPort WSA
    
- Cisco ScanSafe
    
- Cisco Merkai - o log de URLs
    
- Sonicwall da Dell
    
- Fortinet Fortigate
    
- Juniper SRX
    
- Juniper SSG
    
- Gateway da Web seguro McAfee
    
- Microsoft Forefront Threat Management Gateway (W3C)
    
- Série de Palo Alto Firewall
    
- Sophos SG
    
- Sophos Cyberoam
    
- Lula (comum)
    
- Lula (nativo)
    
- Relatório de detalhe investigação Websense - soluções de segurança de Web - (CSV)
    
- Log de atividade de Internet Websense - soluções de segurança de Web - (CEF)
    
- Zscaler
    
> [!NOTE]
> Se uma fonte de dados que você gostaria de usar não é incluída aqui, você poderá solicitar que ele seja adicionado ao descoberta de aplicativo. Para fazer isso, quando você estiver criando um relatório, selecione **outra** **fonte**de dados. Digite o nome da fonte de dados que você está tentando carregar. Vamos examinar o log e permitem que você saiba se adicionamos suporte para esse tipo de log. 
  
## <a name="troubleshoot-errors-when-log-files-are-uploaded"></a>Solucionar erros quando os arquivos de log são carregados

Depois de carregar arquivos de log do tráfego da web, verifique o log de governança para ver se ocorreram erros. Se houver erros, use as informações na tabela a seguir para resolver esses erros.
  
|**Erro**|**Descrição**|**Solução**|
|:-----|:-----|:-----|
|Tipo de arquivo incompatíveis  <br/> |O arquivo carregado não é um arquivo de log válido. Por exemplo, um arquivo de imagem.  <br/> |Carrega um arquivo de texto, zip ou gzip que foi exportá-los diretamente de seu firewall ou proxy.  <br/> |
|Erro interno  <br/> |Uma falha de recursos internos foi detectada.  <br/> |Clique em **Repetir** para executar novamente a tarefa.  <br/> |
|O formato do log não corresponde  <br/> |O formato de log que você carregou não coincide com o formato de log esperada para esta fonte de dados.  <br/> |
Verifique se o log não está corrompido. Compare e coincidir com o formato de arquivo de log para o formato de exemplo mostrado na página carregar. |
|As transações são mais de 90 dias  <br/> |Todas as transações mais de 90 dias e, portanto, estão sendo ignoradas.  <br/> |Exportar um novo log com eventos recentes e carregue-o novamente.  <br/> |
|Nenhuma transação aos aplicativos de nuvem de catálogo  <br/> |Nenhuma transação para quaisquer aplicativos de nuvem reconhecidas são encontrados no log.  <br/> |Verifique se o log contém informações sobre o tráfego de saída.  <br/> |
|Tipo de log sem suporte  <br/> |Quando você seleciona **fonte de dados = outros (sem suporte)**, o log não é analisado. Em vez disso, ele é enviado para revisão para a equipe de [Segurança de aplicativo do Microsoft Cloud](https://aka.ms/whatiscas) técnica.<br/> |A equipe de [Segurança de aplicativo do Microsoft Cloud](https://aka.ms/whatiscas) técnica constrói um analisador dedicado para cada fonte de dados. Já há suporte para fontes de dados mais populares. Quando uma fonte de dados sem suporte é carregada, é analisado e adicionado à lista de possíveis novos analisadores de fonte de dados.<br/> Quando um novo analisador é adicionado ao recurso, uma notificação está incluída nas notas de versão do Microsoft Cloud App Security.  <br/> |
   
## <a name="next-steps"></a>Próximas etapas

- [Revise e agir em alertas](review-office-365-cas-alerts.md)
    
- [Criar relatórios de descoberta de aplicativo](create-app-discovery-reports-in-ocas.md)
    
- [Revise as descobertas de descoberta de aplicativo](review-app-discovery-findings-in-ocas.md)
    
- [Revise suas atividades de utilização de segurança de aplicativo de nuvem do Office 365](utilization-activities-for-ocas.md)
    


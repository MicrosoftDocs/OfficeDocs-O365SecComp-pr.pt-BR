---
title: Logs do tráfego da Web e fontes de dados do Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 12/26/2018
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 290b02bf-a988-4fb9-88b2-34e408216ac8
description: O Office 365 Cloud app Security funciona com logs de tráfego da Web de uma ampla variedade de provedores. Leia este artigo para saber mais sobre os logs de tráfego da Web e as fontes de dados com suporte para o Office 365 Cloud app Security.
ms.openlocfilehash: 67246ded0e3d39c81b5b906f753b91298309d1d8
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218101"
---
# <a name="web-traffic-logs-and-data-sources-for-office-365-cloud-app-security"></a>Logs do tráfego da Web e fontes de dados do Office 365 Cloud App Security
  
|Avaliação * *\>**|Planejamento * *\>**|Implantação * *\>**|Utilização * * *|
|:-----|:-----|:-----|:-----|
|[Iniciar avaliação](office-365-cas-overview.md) <br/> |[Iniciar planejamento](get-ready-for-office-365-cas.md) <br/> |[Iniciar implantação](turn-on-office-365-cas.md) <br/> |Você está aqui!  <br/> [Próximas etapas](#next-steps) <br/> |
  
Você pode usar uma ampla variedade de arquivos de log de tráfego da Web e fontes de dados com o Office 365 Cloud app Security. No enTanto, os arquivos de log de tráfego da Web devem incluir informações específicas e ser formatados de uma determinada maneira para que eles funcionem com os relatórios de descoberta do aplicativo do Office 365 Cloud app Security e o painel de descoberta de nuvem. Use este artigo como um guia de referência para os logs de tráfego da Web e fontes de dados que você usará com o Office 365 Cloud app Security.
  
> [!NOTE]
> Você deve ser um administrador global, administrador de segurança ou leitor de segurança para acessar o &amp; centro de conformidade de segurança e o portal do Office 365 Cloud app Security. Consulte [permissões no centro de conformidade de &amp; segurança do Office 365](permissions-in-the-security-and-compliance-center.md). 
  
## <a name="web-traffic-log-requirements"></a>Requisitos de log de tráfego da Web

O Office 365 Cloud app Security usa dados em seus logs de tráfego da Web para ajudá-lo a entender quais aplicativos estão que as pessoas da sua organização estão usando. Quanto mais detalhes são incluídos nos arquivos de log, melhor visibilidade que você terá na atividade do usuário.
  
As seções a seguir listam os atributos necessários e os requisitos adicionais para que seus logs de tráfego da Web funcionem corretamente com o Office 365 Cloud app Security.

### <a name="attributes"></a>Atributos

O Office 365 Cloud app Security não pode mostrar ou analisar atributos que não estão incluídos em seus logs de tráfego da Web. Por exemplo, o formato de log padrão do Cisco ASA firewall não tem o número de bytes carregados por transação, o nome de usuário ou uma URL de destino (somente um IP de destino). Portanto, esses atributos não são mostrados nos dados de descoberta na nuvem e a visibilidade dos aplicativos na nuvem é limitada. Para firewalls Cisco ASA, o nível de informação deve ser definido como 6. 

Os logs de tráfego da Web devem incluir os seguintes atributos:

- Data da transação
- IP de origem
- Usuário de origem (altamente recomendado)
- Endereço IP de destino
- URL de destino (recomendada; As URLs fornecem maior precisão para a detecção de aplicativos de nuvem do que os endereços IP
- Quantidade total de dados (recomendado; as informações de dados são altamente valiosas)
- Quantidade de dados carregados ou baixados (recomendado; fornece ideias sobre padrões de uso do aplicativo em nuvem)
- Ação tomada (permitido ou bloqueado)

### <a name="additional-requirements"></a>Requisitos adicionais 

Além de incluir os atributos listados anteriormente neste artigo, seus logs de tráfego da Web devem atender aos seguintes requisitos:

- A fonte de dados dos arquivos de log deve ser suportada.
- O formato que os arquivos de log usam deve corresponder ao formato padrão. Quando o arquivo for carregado, a descoberta de aplicativos verificará isso.
- Os eventos no log devem ter ocorrido em não mais de 90 dias atrás.
- O arquivo de log deve incluir informações de tráfego de saída que podem ser analisadas para atividades de rede.
  
## <a name="data-attributes-for-different-vendors"></a>Atributos de dados para diferentes fornecedores

A tabela a seguir resume as informações nos logs de tráfego da Web de vários fornecedores. **Certifique-se de verificar com seu fornecedor as informações mais recentes.**


|                 Fonte de dados                  |    URL do aplicativo de destino    |    IP do aplicativo de destino     |       Nome de usuário       |      IP de origem       |    Tráfego total     |    Bytes carregados    |
|----------------------------------------------|----------------------|----------------------|----------------------|----------------------|----------------------|----------------------|
|                  Barracuda                   | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> |          Não          |          Não          |
|                  Revestimento azul                   | <strong>Sim</strong> |          Não          | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> |
|                  Verificação                  |          Não          | <strong>Sim</strong> |          Não          | <strong>Sim</strong> |          Não          |          Não          |
|              Cisco ASA (syslog)              |          Não          | <strong>Sim</strong> |          Não          | <strong>Sim</strong> | <strong>Sim</strong> |          Não          |
|           Cisco ASA com FirePOWER           | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> |
|                  Cisco FWSM                  |          Não          | <strong>Sim</strong> |          Não          | <strong>Sim</strong> | <strong>Sim</strong> |          Não          |
|              CABEÇALHO do Cisco IronPort              | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> |
|                 Cisco Meraki                 | <strong>Sim</strong> | <strong>Sim</strong> |          Não          | <strong>Sim</strong> |          Não          |          Não          |
|           Clavister NGFW (syslog)            | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> |
|                SonicWall (anteriormente Dell)                | <strong>Sim</strong> | <strong>Sim</strong> |          Não          | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> |
|            FILTRO digital de arte             | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> |
|                  FortiGate                   |          Não          | <strong>Sim</strong> |          Não          | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> |
|                 Juniper SRX                  |          Não          | <strong>Sim</strong> |          Não          | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> |
|                 Juniper SSG                  |          Não          | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> |
|                  McAfee SWG                  | <strong>Sim</strong> |          Não          |          Não          | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> |
|                    MS TMG                    | <strong>Sim</strong> |          Não          | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> |
|              Redes de Palo Alto              |          Não          | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> |
|                    Sophos                    | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> |          Não          |
|                Squid (comum)                | <strong>Sim</strong> |          Não          | <strong>Sim</strong> | <strong>Sim</strong> |          Não          | <strong>Sim</strong> |
|                Squid (nativo)                | <strong>Sim</strong> |          Não          | <strong>Sim</strong> | <strong>Sim</strong> |          Não          | <strong>Sim</strong> |
| WebSense-relatório detalhado de investigação (CSV) | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> |
|    WebSense-log de atividades da Internet (CEF)    | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> |
|                   Zscaler                    | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> | <strong>Sim</strong> |
   
## <a name="supported-vendor-firewalls-and-proxies"></a>Firewalls e proxies de fornecedor suportados

O Office 365 Cloud app Security oferece suporte aos seguintes firewalls e proxies.
  
- Barracuda-Firewall do aplicativo Web (W3C)  
- Log de acesso do proxy de revestimento azul (W3C)
- Ponto de verificação
- Cisco ASA firewall (certifique-se de definir o nível de informações como 6)
- Cisco ASA com FirePOWER   
- CABEÇALHO do Cisco IronPort
- Cisco ScanSafe
- Log de URLs do Cisco Merkai
- Clavister NGFW (syslog)
- FILTRO digital de arte
- Fortinet FortiGate
- iboss Secure Cloud gateway
- Juniper SRX
- Juniper SSG
- Gateway Web seguro da McAfee
- Microsoft Forefront Threat Management Gateway (W3C)
- Firewall do Palo Alto Series
- SonicWALL (anteriormente Dell)   
- O Sophos SG
- Sophos XG
- Sophos Cyberoam
- Squid (comum)
- Squid (nativo)
- WebSense-soluções de segurança da Web-relatório detalhado de investigação (CSV)
- WebSense-soluções de segurança da Web-log de atividades da Internet (CEF)
- Zscaler
    
> [!NOTE]
> Se uma fonte de dados que você gostaria de usar não estiver incluída aqui, você pode solicitar que ela seja adicionada à descoberta de aplicativos. Para fazer isso, quando você estiver criando um relatório, selecione **outro** para a **fonte de dados**. Em seguida, digite o nome da fonte de dados que você está tentando carregar. Examinaremos o log e informaremos se Adicionamos suporte para esse tipo de log. Como alternativa, você pode [definir um analisador personalizado](https://docs.microsoft.com/cloud-app-security/custom-log-parser) que corresponda ao seu formato. 
  
## <a name="troubleshoot-errors-when-log-files-are-uploaded"></a>Solucionar erros quando os arquivos de log são carregados

Após carregar os arquivos de log de tráfego da Web, verifique o log de governança para ver se houve algum erro. Se houver erros, use as informações da tabela a seguir para resolver esses erros.
  
|**Erro**|**Descrição**|**Resolução**|
|:-----|:-----|:-----|
|Tipo de arquivo não suportado  <br/> |O arquivo carregado não é um arquivo de log válido. Por exemplo, um arquivo de imagem.  <br/> |Carregar um arquivo de texto, zip ou gzip que foi exportado diretamente do seu firewall ou proxy.  <br/> |
|Erro interno  <br/> |Uma falha interna de recurso foi detectada.  <br/> |Clique em **repetir** para executar novamente a tarefa.  <br/> |
|O formato de log não corresponde  <br/> |O formato de log carregado não corresponde ao formato de log esperado para esta fonte de dados.  <br/> |
Verifique se o log não está corrompido. Compare e coincida o formato de arquivo de log no formato de exemplo mostrado na página de upload. |
|As transações têm mais de 90 dias  <br/> |Todas as transações têm mais de 90 dias e, portanto, estão sendo ignoradas.  <br/> |Exporte um novo log com eventos recentes e carregue-o novamente.  <br/> |
|Nenhuma transação para catalogar aplicativos de nuvem  <br/> |Nenhuma transação para qualquer aplicativo de nuvem reconhecido é encontrada no log.  <br/> |Verifique se o log contém informações de tráfego de saída.  <br/> |
|Tipo de log sem suporte  <br/> |Quando você seleciona a **fonte de dados = outro (sem suporte)**, o log não é analisado. Em vez disso, ele é enviado para revisão para a equipe técnica do [Microsoft Cloud app Security](https://aka.ms/whatiscas) .<br/> |A equipe técnica do [Microsoft Cloud app Security](https://aka.ms/whatiscas) cria um analisador dedicado para cada fonte de dados. As fontes de dados mais populares já têm suporte. Quando uma fonte de dados sem suporte é carregada, ela é revisada e adicionada à lista de possíveis analisadores de novas fontes de dados.<br/> Quando um novo analisador é adicionado ao recurso, uma notificação é incluída nas notas de versão do Microsoft Cloud app Security.  <br/> |
   
## <a name="next-steps"></a>Próximas etapas

- [ReVisar e executar ação em alertas](review-office-365-cas-alerts.md)
    
- [Criar relatórios de descoberta de aplicativos](create-app-discovery-reports-in-ocas.md)
    
- [Analisar resultados de descoberta de aplicativo](review-app-discovery-findings-in-ocas.md)
    
- [ReVisar suas atividades de utilização do Office 365 Cloud app Security](utilization-activities-for-ocas.md)
    


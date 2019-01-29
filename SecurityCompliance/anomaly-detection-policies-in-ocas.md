---
title: Políticas de detecção de anomalias no Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/28/2019
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 88935b4e-dcb1-47f1-8aca-1bf8fb069db6
description: 'Políticas de detecção de anomalias na segurança de aplicativo do Office 365 nuvem usam algoritmos internos para ajudar a descobrir possíveis problemas. Você deve ter a política de detecção de anomalia pelo menos um, que você pode ajustar (quando você criá-lo) usando filtros. '
ms.openlocfilehash: 7a1cb795531df168f0a5c425e7555ae6b1412d2b
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29604412"
---
# <a name="anomaly-detection-policies-in-office-365-cloud-app-security"></a>Políticas de detecção de anomalias no Office 365 Cloud App Security

Gerenciamento de segurança avançada do Office 365 agora é segurança de aplicativo de nuvem do Office 365.
  
|Avaliação * *\>**|Planejamento * *\>**|Implantação * *\>**|Utilização * * *|
|:-----|:-----|:-----|:-----|
|[Comece a avaliar](office-365-cas-overview.md) <br/> |[Começar a planejar](get-ready-for-office-365-cas.md) <br/> |Você está aqui!  <br/> [Próxima etapa](integrate-your-siem-server-with-office-365-cas.md) <br/> |[Iniciar a utilização](utilization-activities-for-ocas.md) <br/> |
   
Começando com a [versão de segurança de aplicativo do Microsoft Cloud 116](new-in-office-365-cas-2018.md#office-365-cloud-app-security-release-116-3), segurança de aplicativo de nuvem do Office 365 inclui várias anomalia predefinidos detecção diretivas ("pronto") que incluem o usuário e análise de comportamento de entidade (UEBA) e máquina aprendizagem (ML).
  
![Para exibir suas políticas de detecção de anomalias, selecione controle \> políticas.](media/9663baa5-98bf-45e0-9458-6e572b43ec72.png)
  
Essas políticas de detecção de anomalia fornecem resultados imediatos, fornecendo detecções imediatas, direcionamento vários problemas de comportamentos entre os usuários e as máquinas e dispositivos conectados à sua rede. Além disso, as novas políticas exponham mais dados do mecanismo de detecção de segurança de aplicativo de nuvem para ajudá-lo a acelerar o processo de investigação e conter ameaças em andamento.
  
Como um administrador global do Office 365 ou um administrador de segurança, você pode examinar e, se necessário, revise as diretivas padrão que estão disponíveis com a segurança de aplicativo de nuvem do Office 365.
  
 > [!IMPORTANT]
> Não há um período inicial de aprendizado de sete (7) dias durante os quais os alertas de comportamento anômalos não são disparados. O algoritmo de detecção de anomalia é otimizado para reduzir o número de alertas falsos. 
  
## <a name="before-you-begin"></a>Antes de começar

Verifique se:
  
- Sua organização tem [Segurança de aplicativo de nuvem do Office 365](office-365-cas-overview.md)e o serviço está [ativado](turn-on-office-365-cas.md).
    
- [Log de auditoria](turn-audit-log-search-on-or-off.md) está ativado para o seu ambiente do Office 365. 
    
- Você é um administrador global ou administrador de segurança para o Office 365.
    
## <a name="view-your-anomaly-detection-policies"></a>Exibir suas políticas de detecção de anomalia

1. Como administrador global ou administrador de segurança, vá para o portal de segurança de aplicativo de nuvem ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) e entrar.<br>Isso leva você para a página de diretivas de segurança de aplicativo de nuvem do Office 365.
    
2. Na lista **tipo** , escolha a **política de detecção de anomalia**.<br>Padrão da sua organização (ou existente) diretivas de detecção de anomalia são exibidas.<br>![Políticas de detecção de anomalias no Office 365 Cloud App Security](media/2e0ee770-787a-4d4a-bea8-389dc765d4c6.png)
  
3. Selecione uma política para analisar ou editar suas configurações.
    
4. Selecione **Atualizar** para salvar as alterações. 
    
## <a name="learn-more-about-anomaly-detection-policies"></a>Saiba mais sobre políticas de detecção de anomalia

Políticas de detecção de anomalia são automaticamente habilitadas; Entretanto, a segurança de aplicativo de nuvem do Office 365 tem um período inicial de aprendizado de sete dias durante os quais anomalia nem todos os alertas de detecção são geradas. Depois disso, cada sessão é comparada à atividade, quando os usuários estavam ativos, endereços IP, dispositivos, etc. detectadas do mês anterior e a pontuação de risco dessas atividades. Essas detecções fazem parte do mecanismo de detecção de anomalia heurística que seu ambiente de perfis e dispara alertas com relação uma linha de base que foi conhecidas a atividade da sua organização. Essas detecções também aproveitam os algoritmos de aprendizado de máquina projetados para os usuários e os padrões de log para reduzir os falsos positivos de perfil.
  
Problemas são detectados, verificando a atividade do usuário. O risco é avaliado examinando a mais de 30 indicadores de risco diferentes, agrupados em vários fatores de risco, como endereço IP riscado, falhas de login, atividade de admin, contas inativas, local, impossíveis viagens, dispositivo e agente do usuário e taxa de atividade.
  
Alertas de segurança com base nos resultados da política, são acionados. Segurança de aplicativo de nuvem do Office 365 procura em cada sessão do usuário no Office 365 e avisa sempre que acontece algo diferente da linha de base da sua organização ou de atividade de um usuário regular.
  
A tabela a seguir descreve as políticas de detecção de anomalia padrão, o que fazer e como eles funcionam.
  
|**Nome de política de detecção de anomalia**|**Como funciona**|
|:-----|:-----|
|Impossível viagens  <br/> |Identifica as duas atividades do usuário (é uma única ou várias sessões) provenientes de geograficamente distantes locais dentro de um período de tempo menor que o tempo ela teria levado o usuário passe da primeiro local para a segunda, indicando que um diferentes usuário está usando as mesmas credenciais. Esta detecção aproveita uma máquina aprendizagem algoritmo que ignora óbvios "falsos positivos" sua contribuição para a condição de viagens impossíveis, como VPNs e locais regularmente usados por outros usuários na organização. A detecção tem um período inicial de aprendizado de sete dias durante os quais ele aprende padrão da atividade de um novo usuário.  <br/> |
|Atividade de país não frequentes  <br/> |Considera antigas atividade locais para determinar o novos e não frequentes locais. O mecanismo de detecção de anomalia armazena informações sobre locais anteriores utilizado pelos usuários na organização. Um alerta é acionado quando ocorre uma atividade de um local que não foi recentemente ou nunca visitado pelo usuário ou por qualquer usuário na organização.  <br/> |
|Atividade de endereços IP anônimos  <br/> |Identifica que usuários estavam ativos a partir de um endereço IP que tenha sido identificado como um endereço IP de proxy anônimo. Esses proxies são usados por pessoas que deseja ocultar o endereço IP do seu dispositivo e podem ser usadas para fins maliciosos. Esta detecção aproveita uma máquina aprendizagem algoritmo que reduz "falsos positivos", como endereços IP de forma incorreta marcados que são amplamente usados pelos usuários na organização.  <br/> |
|Atividade de endereços IP suspeitos  <br/> |Identifica que usuários estavam ativos a partir de um endereço IP que tenha sido identificado como riscado pelo Microsoft Threat Intelligence. Esses endereços IP envolvidos nas atividades mal-intencionado, como Botnet C&amp;C e pode indicar conta comprometida. Esta detecção aproveita uma máquina aprendizagem algoritmo que reduz "falsos positivos", como endereços IP de forma incorreta marcados que são amplamente usados pelos usuários na organização.  <br/> |
|Atividades incomuns (por usuário)  <br/> | Identifica os usuários que executam atividades incomuns, tais como:  <br/>  – Múltiplos downloads de arquivo  <br/>  -- Atividades de compartilhamento de arquivo  <br/>  -- Arquivo atividades de exclusão  <br/>  – Atividades representação  <br/>  – Atividades administrativas  <br/>  Essas políticas procuram a atividades dentro de uma única sessão com relação a linha de base aprendida, o que pode indicar em uma tentativa de violação. Essas detecções aproveitar uma máquina algoritmo que perfis os usuários fazem logon no padrão de aprendizado e reduz os falsos positivos. Essas detecções fazem parte do mecanismo de detecção de anomalia heurística que seu ambiente de perfis e dispara alertas com relação uma linha de base que foi conhecidas a atividade da sua organização.  <br/> |
|Várias tentativas de login com falha  <br/> |Identifica os usuários que falharam várias tentativas de logon em uma única sessão com relação a linha de base aprendida, que poderia indicar em uma tentativa de violação.  <br/> |
   
## <a name="triage-anomaly-detection-alerts"></a>Alertas de detecção de anomalia triagem

À medida que chegam alertas, você pode triagem esses alertas rapidamente e determinar quais devem lidar com pela primeira vez. Ter o contexto de um alerta permite que você consulte panorama e determine se algo mal-intencionado está acontecendo na verdade. Use o procedimento a seguir para dar início a explorando um alerta:
  
1. Como administrador global ou administrador de segurança, vá para o portal de segurança de aplicativo de nuvem ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) e entrar. 
    
2. Escolha **alertas** para exibir os alertas. 
    
3. Para obter o contexto de um alerta, siga estas etapas:
    
4. Escolha **investigar** \> **log da atividade**.
    
5. Selecione um item, como um usuário ou o endereço IP. Isso abre o dinheiro ideias relevantes.<br>![No log de atividade, você pode investigar um endereço IP.](media/32a727c5-e406-4fe2-9443-c1a7fb6628fc.png)
  
6. No dinheiro ideias relevantes, clique em um comando disponível, como um ícone na seção **Mostrar SEMELHANTE** .<br> ![Clique no ícone de relógio para ver as atividades realizadas dentro de uma atividade selecionada 48 horas](media/c6c96aa0-98e5-4205-8873-45f8d6fd0843.png)
  
7. Obtém ideias sobre o item selecionado ao continuar a explorar os detalhes de item.
    
Um alerta em vários logins com falha de fato ser suspeito e pode indicar um ataque de força bruta potencial. No entanto, um alerta tal também pode ser um erro de configuração de aplicativo, fazendo com que o alerta para ser um positivo true benigno. Se você vir um alerta de logons falhou múltiplo com atividades suspeitas adicionais, há uma probabilidade maior que uma conta for comprometida. Por exemplo, suponha que um alerta de login falhou múltiplo é seguido por atividade de um endereço IP TOR e viagens impossíveis de atividade, ambos os indicadores fortes de comprometimento. Você ainda pode ver que o mesmo usuário realizada uma atividade de download em massa, que é geralmente um indicador do invasor executando exfiltration de dados. Ele do coisas como o que você pode explorar na segurança do aplicativo de nuvem do Office 365 visualizar e triagem os alertas e agir onde for necessário.
  
## <a name="next-steps"></a>Próximas etapas

- [Integrar seu servidor SIEM](integrate-your-siem-server-with-office-365-cas.md)
    
- [Revise e agir em alertas](review-office-365-cas-alerts.md)
    
- [Seus endereços IP para simplificar o gerenciamento de grupo](group-your-ip-addresses-in-ocas.md)
    


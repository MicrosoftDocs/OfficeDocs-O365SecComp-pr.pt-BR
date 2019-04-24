---
title: Políticas de detecção de anomalias no Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/15/2019
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 88935b4e-dcb1-47f1-8aca-1bf8fb069db6
description: 'Diretivas de detecção de anomalias no Office 365 Cloud app Security usam algoritmos internos para ajudar a descobrir possíveis problemas. Você deve ter pelo menos uma política de detecção de anomalias, que você pode ajustar (ao criá-la) usando filtros. '
ms.openlocfilehash: 5308af139a46dad0793ed7eedacab0aee62dcc6c
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32242838"
---
# <a name="anomaly-detection-policies-in-office-365-cloud-app-security"></a>Políticas de detecção de anomalias no Office 365 Cloud App Security

|Avaliação * *\>**|Planejamento * *\>**|Implantação * *\>**|Utilização * * *|
|:-----|:-----|:-----|:-----|
|[Iniciar avaliação](office-365-cas-overview.md) <br/> |[Iniciar planejamento](get-ready-for-office-365-cas.md) <br/> |Você está aqui!  <br/> [Próxima etapa](ocas-conditional-access-app-control.md) <br/> |[Começar a usar](utilization-activities-for-ocas.md) <br/> |
   
Começando com [o Microsoft Cloud app Security versão 116, o](new-in-office-365-cas-2018.md#office-365-cloud-app-security-release-116)Office 365 Cloud app Security inclui várias políticas de detecção de anomalias predefinidas ("pronta para uso") que incluem Ueba (análise comportamental de usuário e entidade) e o Machine Learning (ml).
  
![Para exibir as políticas de detecção de anomalias, \> escolha políticas de controle.](media/9663baa5-98bf-45e0-9458-6e572b43ec72.png)
  
Essas políticas de detecção de anomalias fornecem resultados imediatos, fornecendo detecções imediatas, direcionando várias anomalias comportamentais nos seus usuários e nas máquinas e dispositivos conectados à sua rede. Além disso, as novas políticas expõem mais dados do mecanismo de detecção do Cloud app Security para ajudá-lo a acelerar o processo de investigação e a conter ameaças em andamento.
  
Como administrador global ou administrador de segurança do Office 365, você pode examinar e, se necessário, revisar as políticas padrão que estão disponíveis com o Office 365 Cloud app Security.
  
 > [!IMPORTANT]
> Há um período de aprendizado inicial de sete (7) dias durante os quais os alertas de comportamento anômala não são acionados. O algoritmo de detecção de anomalias é otimizado para reduzir o número de alertas falsos positivos. 
  
## <a name="before-you-begin"></a>Antes de começar

Verifique se:
  
- Sua organização tem o [Office 365 Cloud app Security](office-365-cas-overview.md)e o serviço está [ativado](turn-on-office-365-cas.md).
    
- O [registro em log de auditoria](turn-audit-log-search-on-or-off.md) está ativado para seu ambiente do Office 365. 
    
- Você é um administrador global ou administrador de segurança do Office 365.
    
## <a name="view-your-anomaly-detection-policies"></a>Exibir suas políticas de detecção de anomalias

1. Como administrador global ou administrador de segurança, vá para o portal do Cloud app Security[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)() e entre.<br>Isso leva você à página de políticas de segurança do aplicativo nuvem do Office 365.
    
2. Na lista **tipo** , escolha **política de detecção**de anomalias.<br>As políticas de detecção de anomalias padrão (ou existentes) da sua organização são exibidas.<br>![Políticas de detecção de anomalias no Office 365 Cloud App Security](media/2e0ee770-787a-4d4a-bea8-389dc765d4c6.png)
  
3. Selecione uma política para revisar ou editar suas configurações.
    
4. Selecione **Atualizar** para salvar as alterações. 
    
## <a name="learn-more-about-anomaly-detection-policies"></a>Saiba mais sobre as políticas de detecção de anomalias

As políticas de detecção de anomalias são habilitadas automaticamente; no entanto, o Office 365 Cloud app Security tem um período de aprendizado inicial de sete dias durante o qual nem todos os alertas de detecção de anomalia são gerados. Após isso, cada sessão é comparada com a atividade, quando os usuários estavam ativos, endereços IP, dispositivos etc. detectados no último mês e a pontuação de risco dessas atividades. Essas detecções fazem parte do mecanismo de detecção de anomalias heurística que faz o perfil de seu ambiente e dispara alertas com relação a uma linha de base que foi aprendida na atividade da sua organização. Essas detecções também aproveitam os algoritmos de aprendizado de máquina projetados para criar um perfil dos usuários e dos padrões de login para reduzir os falsos positivos.
  
As anomalias são detectadas pela verificação da atividade do usuário. O risco é avaliado com a análise de mais de 30 indicadores de risco diferentes, agrupados em vários fatores de risco, como endereço IP arriscado, falhas de logon, atividade de administração, contas inativas, local, viagem impossível, controle de dispositivo e de usuário e taxa de atividade.
  
Com base nos resultados da política, os alertas de segurança são disparados. O Office 365 Cloud app Security examina cada sessão de usuário no Office 365 e alerta você sempre que algo acontecer diferente da linha de base da sua organização ou da atividade regular de um usuário.
  
A tabela a seguir descreve as políticas padrão de detecção de anomalias, o que elas fazem e como funcionam.
  
|**Nome da política de detecção de anomalias**|**Como funciona**|
|:-----|:-----|
|Viagens impossível  <br/> |Identifica duas atividades do usuário (é uma única ou várias sessões) originadas de locais geograficamente distantes dentro de um período de tempo menor do que o tempo em que teria levado o usuário a viajar do primeiro local para o segundo, indicando que um outro o usuário está usando as mesmas credenciais. Essa detecção utiliza um algoritmo de aprendizado de máquina que ignora "falsos positivos" que contribuem para a condição de viagens impossível, como VPNs e locais usados regularmente por outros usuários na organização. A detecção tem um período de aprendizado inicial de sete dias durante o qual ele aprende o padrão de atividade de um novo usuário.  <br/> |
|Atividade do país não frequente  <br/> |Considera locais de atividades passadas para determinar locais novos e pouco frequentes. O mecanismo de detecção de anomalias armazena informações sobre locais anteriores usados por usuários na organização. Um alerta é disparado quando ocorre uma atividade de um local que não foi recentemente ou nunca visitado pelo usuário ou por qualquer usuário na organização.  <br/> |
|Atividade de endereços IP anônimos  <br/> |Identifica se os usuários estavam ativos de um endereço IP que foi identificado como um endereço IP de proxy anônimo. Esses proxies são usados por pessoas que desejam ocultar o endereço IP do dispositivo e podem ser usadas para propósito mal-intencionado. Essa detecção utiliza um algoritmo de aprendizado de máquina que reduz "falsos positivos", como endereços IP com marca de informações incorretas que são amplamente usados por usuários na organização.  <br/> |
|Atividade de endereços IP suspeitos  <br/> |Identifica se os usuários estavam ativos de um endereço IP que foi identificado como arriscado pelo Microsoft Threat Intelligence. Esses endereços IP estão envolvidos em atividades mal-intencionadas, como botnet C&amp;c, e podem indicar uma conta comprometida. Essa detecção utiliza um algoritmo de aprendizado de máquina que reduz "falsos positivos", como endereços IP com marca de informações incorretas que são amplamente usados por usuários na organização.  <br/> |
|Atividades inComuns (por usuário)  <br/> | Identifica os usuários que executam atividades anormais, como:  <br/>  --Downloads de vários arquivos  <br/>  --Atividades de compartilhamento de arquivos  <br/>  --Atividades de exclusão de arquivo  <br/>  --Atividades de representação  <br/>  --Atividades administrativas  <br/>  Essas políticas procuram atividades dentro de uma única sessão com relação à linha de base aprendida, que pode indicar uma tentativa de violação. Essas detecções aproveitam um algoritmo de aprendizagem de máquina que faz o perfil do padrão de logon dos usuários e reduz os falsos positivos. Essas detecções fazem parte do mecanismo de detecção de anomalias heurística que faz o perfil de seu ambiente e dispara alertas com relação a uma linha de base que foi aprendida na atividade da sua organização.  <br/> |
|Várias tentativas de logon com falha  <br/> |Identifica os usuários que falharam várias tentativas de logon em uma única sessão com relação à linha de base aprendida, que pode indicar uma tentativa de violação.  <br/> |
   
## <a name="triage-anomaly-detection-alerts"></a>Filtrar alertas de detecção de anomalias

À medida que os alertas chegam, você pode fazer uma triagem desses alertas rapidamente e determinar quais deles lidar primeiro. Ter contexto para um alerta permite que você veja a imagem maior e determine se algo mal-intencionado está realmente acontecendo. Use o seguinte procedimento para começar a explorar um alerta:
  
1. Como administrador global ou administrador de segurança, vá para o portal do Cloud app Security[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)() e entre. 
    
2. Escolha **alertas** para exibir seus alertas. 
    
3. Para obter o contexto de um alerta, siga estas etapas:
    
4. Escolha **investigar** \> **log de atividades**.
    
5. Selecione um item, como um usuário ou endereço IP. Isso abre a gaveta relevante do insights.<br>![No log de atividades, você pode investigar um endereço IP.](media/32a727c5-e406-4fe2-9443-c1a7fb6628fc.png)
  
6. Na gaveta relevante de ideias, clique em um comando disponível, como um ícone na seção **Mostrar semelhante** .<br> ![Clique no ícone de relógio para ver as atividades realizadas em 48 horas de uma atividade selecionada](media/c6c96aa0-98e5-4205-8873-45f8d6fd0843.png)
  
7. Obtenha informações sobre o item selecionado continuando a explorar detalhes desse item.
    
Um alerta em vários logons com falha pode ser de fato suspeito, e pode indicar um possível ataque de força bruta. No enTanto, esse alerta também pode ser uma configuração incorreta do aplicativo, fazendo com que o alerta seja um verdadeiro positivo. Se você vir um alerta de vários logons com falha com atividades suspeitas adicionais, haverá uma maior probabilidade de uma conta ser comprometida. Por exemplo, suponha que um alerta de logon múltiplo de falha seja seguido por atividade de um endereço IP do TOR e atividade de viagem impossível, tanto indicadores fortes de comprometimento. Você pode até mesmo ver que o mesmo usuário realizou uma atividade de download em massa, que geralmente é um indicador do invasor que realiza exfiltration de dados. É como isso que você pode explorar no Office 365 Cloud app Security para exibir e fazer a triagem de seus alertas e tomar as medidas necessárias.
  
## <a name="next-steps"></a>Próximas etapas

- [Implantar o Controle de Aplicativos de Acesso Condicional nos aplicativos do Office 365](ocas-deploy-conditional-access-app-control.md)

- [Agrupar seus endereços IP para simplificar o gerenciamento](group-your-ip-addresses-in-ocas.md)

- [Integrar seu servidor SIEM](integrate-your-siem-server-with-office-365-cas.md)
    
- [ReVisar e executar ação em alertas](review-office-365-cas-alerts.md)
    
    


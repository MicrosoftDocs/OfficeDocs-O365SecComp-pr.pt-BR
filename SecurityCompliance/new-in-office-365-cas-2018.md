---
title: O que há de novo no Office 365 Cloud app Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: reference
ms.date: 01/25/2019
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
description: Veja o que foi lançado durante 2018 para o Office 365 Cloud app Security
ms.openlocfilehash: 986fb64eedf8184e7835d1fec41845fde13b294b
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214341"
---
# <a name="office-365-cloud-app-security-updates-during-2018"></a>Atualizações do Office 365 Cloud app Security durante 2018

## <a name="office-365-cloud-app-security-release-138"></a>Versão 138 do Office 365 Cloud app Security

*Lançamento de 23 de dezembro de 2018*

**Seguinte [Microsoft Cloud app Security versão 138](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-138)**:

- **Upload de log automático usando o Docker no Windows** O Cloud app Security agora oferece suporte ao carregamento automático de logs para o Windows 10 ([atualização de criadores de outono](https://docs.microsoft.com/windows/whats-new/whats-new-windows-10-version-1709) e mais recente) e ao Windows Server ([versão 1709](https://docs.microsoft.com/windows-server/get-started/whats-new-in-windows-server-1709) e posterior) usando o Docker no Windows. ConFira [Este artigo](https://docs.microsoft.com/cloud-app-security/discovery-docker-windows) para saber mais e configurar o Docker.  

- **Integração com o Microsoft Flow** O Cloud app Security agora integra-se ao [Microsoft Flow](https://docs.microsoft.com/flow/getting-started) para fornecer automação de alerta personalizada e guias de organização. ConFira [Este artigo](https://docs.microsoft.com/cloud-app-security/flow-integration) para saber mais e configurar a integração do Microsoft Flow. 

## <a name="office-365-cloud-app-security-release-137"></a>Versão 137 do Office 365 Cloud app Security

*Lançamento de 8 de dezembro de 2018*

**Seguinte [Microsoft Cloud app Security versão 137](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-137)**:

- **Adicionado suporte para Dynamics** O Cloud app Security agora inclui suporte para as atividades do Microsoft Dynamics que são suportadas no log de auditoria do Office 365. 

- **Heads up – nova terminologia!** O nome dos recursos de permissões do aplicativo foi alterado para fins de clareza – ele agora é chamado de aplicativos OAuth. 

## <a name="office-365-cloud-app-security-release-136"></a>Versão 136 do Office 365 Cloud app Security

*Lançado em 25 de novembro de 2018*

**Seguinte [Microsoft Cloud app Security versão 136](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-136)**:

- **Atualizações de descoberta de nuvem** O analisador de log personalizado foi aprimorado para suportar formatos adicionais e mais complexos de logs de tráfego da Web. Como parte desses aprimoramentos, os usuários agora podem inserir cabeçalhos personalizados para arquivos de log CSV com cabeçalho, usar delimitadores especiais para arquivos de valor chave, formato de arquivo de syslog de processo e muito mais.

- **Nova política de detecção de anomalia: regras de manipulação de caixa de entrada suspeitas** Esta política faz o perfil de seu ambiente e dispara alertas quando regras suspeitas que excluem ou movem mensagens ou pastas são definidas na caixa de entrada de um usuário. Isso pode indicar que a conta do usuário está comprometida, que as mensagens estão sendo intencionalmente ocultas e que a caixa de correio está sendo usada para distribuir spam ou malware em sua organização.

- **Suporte para grupos em políticas de permissão de aplicativo** O Cloud app Security agora oferece a capacidade de definir políticas de permissão de aplicativo de forma mais granular, com base nas associações de grupo dos usuários que autorizaram os aplicativos. Por exemplo, um administrador pode decidir definir uma política que revoga aplicativos incomuns se eles solicitarem permissões elevadas, somente se o usuário que autorizar as permissões for um membro do grupo de administradores.

## <a name="office-365-cloud-app-security-releases-133-134-and-135"></a>Office 365 Cloud app Security versões 133, 134 e 135

*Lançado em outubro de novembro de 2018*

**Seguinte [Microsoft Cloud app Security versão 133, 134 e 135](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-133-134-135)**:

- **Novas políticas de detecção** de anomalias estão distribuindo gradualmente:
    
    - A nova política de **dados exfiltration para aplicativos** não aprovados é automaticamente habilitada para alertá-lo quando um usuário ou endereço IP usa um aplicativo que não é aprovado para executar uma atividade que se assemelha a uma tentativa de Exfiltrate informações da sua organização.
    
    - A nova política de **atividades VM de exclusão múltipla** faz o seu ambiente e dispara alertas quando os usuários excluem várias VMs em uma única sessão, em relação à linha de base em sua organização.

- **Suporte de descoberta de nuvem para i-Filter** O recurso de descoberta de nuvem do Cloud app Security agora tem suporte avançado para o analisador de syslog de filtro.

## <a name="office-365-cloud-app-security-release-131"></a>Versão 131 do Office 365 Cloud app Security

*Lançamento de 16 de setembro de 2018*

**Seguinte [Microsoft Cloud app Security versão 131](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-131)**:

- **Revogar automaticamente as permissões em aplicativos OAuth arriscados** Agora você pode controlar quais aplicativos OAuth seus usuários têm acesso, revogando a permissão de aplicativo para aplicativos OAuth no Office. Ao criar uma política de permissão de aplicativo, agora você pode definir a política para revogar a permissão de um aplicativo.

- **Analisador integrado de descoberta de nuvem adicional suportado** A descoberta na nuvem agora oferece suporte ao formato de log de nuvem da Web segurança do Forcepoint.
  
## <a name="office-365-cloud-app-security-release-130"></a>Versão 130 do Office 365 Cloud app Security

*Lançamento de 5 de setembro de 2018*

**Seguinte [Microsoft Cloud app Security versão 130](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-130)**:

- **Nova barra de menus** Para fornecer uma experiência de administração mais consistente nos produtos da Microsoft 365 e permitir que você faça a dinamização mais fácil entre as soluções de segurança da Microsoft, a barra de menus do portal de segurança do Cloud app foi movida para o lado esquerdo da tela. Essa experiência de navegação consistente ajuda você a se orientar ao migrar de um portal de segurança da Microsoft para outro.<br/>![Barra de menus no Office Cloud app Security](media/OCAS-MenuBar.png)<br/>

- **Classificação do aplicativo OAuth de impacto** Agora você pode enviar o feedback da equipe de segurança do aplicativo na nuvem para que possamos saber se há um aplicativo OAuth descoberto em sua organização que parece mal-intencionado. Este novo recurso permite fazer parte da nossa comunidade de segurança e aprimorar a pontuação e a análise do risco do aplicativo OAuth. Para obter mais informações, consulte [Manage OAuth apps](manage-app-permissions-in-ocas.md).

- **Novos analisadores de descoberta de nuvem** Os analisadores de descoberta de nuvem agora oferecem suporte ao iboss Secure Cloud gateway e ao Sophos XG.

## <a name="office-365-cloud-app-security-release-128"></a>Versão 128 do Office 365 Cloud app Security

*Lançamento de 5 de agosto de 2018* 
  
**Seguinte [Microsoft Cloud app Security versão 128](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-128)**: 
  
- **Aplicativos OAuth em vários aplicativos** Para aplicativos OAuth, agora você pode proibir ou aprovar vários aplicativos em uma única ação. Por exemplo, você pode revisar todos os aplicativos que receberam permissão por usuários em sua organização, selecione todos os aplicativos que deseja proibir e clique em proibir aplicativos para revogar todos os consentimento concedidos e não permitirá que os usuários recebam mais permissões para esses aplicativos. Para saber mais, confira [gerenciar aplicativos OAuth usando o Office 365 Cloud app Security](manage-app-permissions-in-ocas.md). 
    
- **Nova consulta sugerida: aplicativos de nuvem prontos para rgpd** Há uma nova consulta sugerida para permitir que você identifique aplicativos descobertos que estão prontos para o RGPD. Como você provavelmente já sabe, o RGPD se tornou recentemente uma prioridade principal para administradores de segurança. Essa consulta ajuda você a identificar facilmente os aplicativos que estão RGPD prontos e reduzir a ameaça, avaliando o risco dos aplicativos que não estão. Para usar a nova consulta, no painel **de descoberta de nuvem** , na guia aplicativos descobertos, escolha **consultas** > **aplicativos de nuvem prontos para rgpd**. ****<br/>![Consulta de aplicativos de nuvem prontos para RGPD](media/OCAS-FindGDPRQueries.png)<br/>
    
## <a name="office-365-cloud-app-security-release-126"></a>Versão 126 do Office 365 Cloud app Security

*Lançamento de 7 de julho de 2018* 
  
**Seguinte [Microsoft Cloud app Security versão 126](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-126)**: 
  
- **Correção automatizada para atividades suspeitas** Agora você pode definir ações de correção automática para sessões suspeitas acionadas pelas políticas de detecção de anomalias. Esse aprimoramento permite que você seja alertado instantaneamente quando ocorrer uma violação e aplicar ações de governança automaticamente, como suspender usuário. Para obter mais informações, consulte [diretivas de detecção de anomalias no Office 365 Cloud app Security](anomaly-detection-policies-in-ocas.md).
    
- **Detecção automatizada de aplicativos OAuth arriscados** Além da investigação existente de aplicativos OAuth conectados ao seu ambiente, o Office 365 Cloud app Security agora permite que você defina as notificações automatizadas para permitir que você saiba quando um aplicativo OAuth atende a determinados critérios. Por exemplo, você pode ser alertado automaticamente quando há aplicativos que exigem um nível de permissão alto e foram autorizados por mais de 50 usuários. Para obter mais informações, consulte [Manage OAuth apps using Office 365 Cloud app Security](manage-app-permissions-in-ocas.md).
    
- **Suporte ao gerenciamento do provedor de serviços de segurança gerenciada (MSSP)** O Office 365 Cloud app Security agora oferece uma melhor experiência de gerenciamento para o MSSPs e permite que você configure parceiros externos como administradores com qualquer uma das funções atualmente disponíveis no Office 365 Cloud app Security. Além disso, os administradores com direitos de acesso a mais de um locatário agora podem dinamizar facilmente os locatários. 
    
## <a name="office-365-cloud-app-security-release-124"></a>Versão 124 do Office 365 Cloud app Security

*Lançamento de 10 de junho de 2018* 
  
**Seguinte [Microsoft Cloud app Security versão 124](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-124)**: 
  
- Implantações com **escopo** As organizações corporativas podem determinar, de granularidade, quais usuários monitorar e proteger com base na associação ao grupo. Este recurso permite que você selecione os usuários cujas atividades não serão exibidas para qualquer um dos aplicativos protegidos. O monitoramento com escopo é especialmente útil para conformidade e licenciamento. Algumas normas de conformidade exigem que você evite monitorar os usuários de determinados países devido às normas locais. E você pode monitorar menos usuários para permanecer dentro dos limites das suas licenças de segurança do aplicativo na nuvem do Office 365. 
    
- **Novo servidor de email** O servidor de email para o Office 365 Cloud app Security foi alterado e usa intervalos de endereços IP diferentes. Para garantir que você pode obter notificações, adicione os novos endereços IP à sua lista branca do anti-spam. Para organizações que personalizam suas notificações, o Cloud app Security permite que você use o MailChimp, um serviço de email de terceiros. Para obter a lista de endereços IP de servidor de email e instruções para habilitar o trabalho com o MailChimp, consulte [requisitos de rede (Microsoft Cloud app Security)](https://docs.microsoft.com/cloud-app-security/network-requirements) e [configurações de email (Microsoft Cloud app Security)](https://docs.microsoft.com/cloud-app-security/mail-settings).
    
## <a name="office-365-cloud-app-security-release-121"></a>Versão 121 do Office 365 Cloud app Security

*Lançamento de 6 de maio de 2018* 
  
**Seguinte [Microsoft Cloud app Security versão 121](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-121)**: 
  
- **Melhorias na política de detecção**de anomalias. As políticas de detecção de anomalias do Office 365 Cloud app Security foram aprimoradas para incluir dois novos tipos de detecção de ameaças que são implantadas gradualmente: 
    
  - **Atividade de ransomware.** Os recursos de detecção de ransomware são estendidos com detecção de anomalias para oferecer uma cobertura mais abrangente contra ataques de ransomware sofisticados. 
    
  - **Atividade do usuário terminada.** Atividade de usuário finalizada permite monitorar as contas de usuários demitidos que podem ter sido desprovisionados de aplicativos corporativos, mas que ainda podem ter acesso a determinados recursos corporativos. 
    
    para exibir as [políticas de detecção](anomaly-detection-policies-in-ocas.md)de anomalias, no portal do Office 365 Cloud App Security, escolha **políticas**de **controle** \> .
    
## <a name="office-365-cloud-app-security-release-120"></a>Versão 120 do Office 365 Cloud app Security

*Lançamento de 22 de abril de 2018* 
  
**Seguinte [Microsoft Cloud app Security versão 120](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-120)**: 
  
- **Aplicativos internos como atividades do usuário**. Para o Office 365 e o Azure Active Directory (Azure AD), agora estamos distribuindo a capacidade de detectar aplicativos internos como atividades de conta de usuário executadas pelos aplicativos do Office 365 e do Azure AD (tanto interna quanto externa). Isso permite que você crie políticas para alertá-lo se um aplicativo realizar atividades inesperadas e não autorizadas. 
    
- **Mais campos na exportação de lista de aplicativos OAuth**. Ao exportar uma lista de aplicativos OAuth para CSV, campos adicionais como o Publisher, o nível de permissões e o uso da Comunidade são incluídos para ajudar no processo de conformidade e investigação. 
    
## <a name="office-365-cloud-app-security-release-119"></a>Versão 119 do Office 365 Cloud app Security

*Lançamento de 1º de abril de 2018* 
  
**Seguinte [Microsoft Cloud app Security versão 119](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-119)**: 
  
- **Melhorias na descoberta na nuvem**. A descoberta em nuvem oferece mais informações sobre os principais usuários e endereços IP, facilitando a exibição de detalhes de uso sobre o Office 365 e outros aplicativos. Para saber mais, confira reVisar [resultados de descoberta de aplicativo no Office 365 Cloud app Security](review-app-discovery-findings-in-ocas.md).
    
    ![O painel de descoberta de nuvem foi atualizado](media/12712681-c0b3-4cb3-b7fd-2cf2ad4e825f.png)
  
## <a name="office-365-cloud-app-security-release-118"></a>Versão 118 do Office 365 Cloud app Security

*Lançamento de 18 de março de 2018* 
  
**Seguinte [Microsoft Cloud app Security versão 118](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-118)**: 
  
- **Suporte a Barracuda**. A descoberta na nuvem agora oferece suporte a firewalls de dataSérie Barracuda e a fluxo de Web do firewall da série D 
    
## <a name="office-365-cloud-app-security-release-117"></a>Versão 117 do Office 365 Cloud app Security

*Lançamento de 6 de março de 2018* 
  
**Seguinte [Microsoft Cloud app Security versão 117](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-117)**: 
  
- **i-filtro de suporte**. A descoberta na nuvem agora oferece suporte a i-FILTER. 
    
## <a name="office-365-cloud-app-security-release-116"></a>Versão 116 do Office 365 Cloud app Security

*Lançamento de 18 de fevereiro de 2018* 
  
**Seguinte [Microsoft Cloud app Security versão 116](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-116)**: 
  
- **Aprimoramentos de política de detecção**de anomalias. As políticas de detecção de anomalias no Office 365 Cloud app Security foram aprimoradas com novas detecções baseadas em cenário, incluindo o impossível viagem, a atividade de um endereço IP suspeito e várias tentativas de logon com falha. As novas políticas são habilitadas automaticamente, fornecendo uma detecção de ameaça pronta em todo o ambiente de nuvem. Além disso, as novas políticas expõem mais dados do mecanismo de detecção do Office 365 Cloud app Security, que pode ajudar a acelerar o processo de investigação e a conter ameaças em andamento. Para saber mais, confira o artigo Microsoft Cloud app Security, [obtenha análise de comportamento instantâneo e detecção de anomalias](https://docs.microsoft.com/cloud-app-security/anomaly-detection-policy).
    
- **Suporte a analisador de log para formatos de ponto de verificação**. Os analisadores de log de descoberta de nuvem agora dão suporte a dois formatos de ponto de verificação adicionais: XML e KPC. 
    
## <a name="office-365-cloud-app-security-release-114"></a>Versão 114 do Office 365 Cloud app Security

*Lançamento de 21 de janeiro de 2018* 
  
**Seguinte [Microsoft Cloud app Security versão 114](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-114)**: 
  
- **Status do serviço**. agora você pode verificar o status atual do serviço de segurança do Office 365 Cloud App **** \> , acessando o **status do sistema**. 
    
    ![Clique em \> status do sistema de ajuda para exibir o status de integridade do sistema](media/2b496dac-ed9d-4480-83b6-85f9510d3aea.png)
  
- **Consultas personalizadas para o log de atividades**. A partir da versão 114, a capacidade de criar e salvar consultas personalizadas no log de atividades é distribuir gradualmente. As consultas personalizadas permitem que você crie modelos de filtro que podem ser reutilizados para investigação aprofundada. Além disso, as consultas sugeridas foram adicionadas para fornecer modelos de investigação prontos para filtrar suas atividades e aplicativos descobertos. As consultas sugeridas incluem filtros personalizados para identificar riscos como atividades de representação, atividades do administrador, aplicativos de armazenamento em nuvem arriscados não compatíveis, aplicativos corporativos com criptografia fraca e riscos de segurança. Use as consultas sugeridas como ponto de partida, modifique-as conforme necessário e, em seguida, salve-as como uma nova consulta. 
    
## <a name="office-365-cloud-app-security-release-113"></a>Versão 113 do Office 365 Cloud app Security

*Lançamento de 8 de janeiro de 2018* 
  
**Seguinte [Microsoft Cloud app Security versão 113](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-113)**: 
  
- **Suporte a analisador de log para formatos genéricos**. Os analisadores de log de descoberta de nuvem agora oferecem suporte aos seguintes formatos genéricos: LEEF, CEF e W3C. 

## <a name="related-topics"></a>Tópicos relacionados

[O que há de novo no Office 365 Cloud app Security](new-in-office-365-cas.md)

[Consulte as atualizações 2017 para o Office 365 Cloud app Security](new-in-office-365-cas-2017.md)
    
[Atividades de utilização após a implantação do Office 365 Cloud App Security](utilization-activities-for-ocas.md)
---
title: Novidades na segurança de aplicativo de nuvem do Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: reference
ms.date: 11/28/2018
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: d674763c-a4c9-4604-8623-68c1836d27f3
description: Veja o que há de novo na segurança de aplicativo de nuvem do Office 365
ms.openlocfilehash: a3ca4504d80cbb39b51ecbcf3a5165bc5139e07c
ms.sourcegitcommit: bf628da123a89d9422e8cff02165b1e2d35dfe12
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/28/2018
ms.locfileid: "26872009"
---
# <a name="what-is-new-in-office-365-cloud-app-security"></a>Novidades na segurança de aplicativo de nuvem do Office 365

**Resumo** Leia este artigo para obter uma rápida visão geral das atualizações e novos recursos no Office 365 nuvem App segurança (anteriormente conhecido como gerenciamento de segurança avançada do Office 365), que é possibilitada pela [Microsoft Cloud App Security](https://aka.ms/whatiscas).
  
Este artigo foi atualizado com frequência, como recursos são adicionados ou aprimorados. Atualizações de segurança de aplicativo de nuvem do Office 365 sejam liberadas aproximadamente duas semanas após as atualizações de segurança de aplicativo do Microsoft Cloud e nem todas as atualizações de segurança de aplicativo do Microsoft Cloud aplicam à segurança de aplicativo de nuvem do Office 365. Além disso, os novos recursos podem levar uma semana ou mais após sua data de lançamento seja mostrada no seu ambiente de segurança de aplicativo de nuvem do Office 365.

## <a name="office-365-cloud-app-security-release-136"></a>Versão de segurança do aplicativo de nuvem do Office 365 136

*Lançada em 25 de novembro de 2018*

**Após o [lançamento de segurança de aplicativo do Microsoft Cloud 136](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-136)**:

- **Atualizações de descoberta de nuvem** O analisador de log personalizada foi melhorado para suportar adicionais e formatos de logs de tráfego da web mais complexo. Como parte desses usuários aprimoramentos agora pode inserir cabeçalhos personalizados para os arquivos de log sem cabeçalho CSV, use delimitadores especiais para arquivos de chave-valor, processo de formato de arquivo Syslog e muito mais.

- **Nova política de detecção de anomalia: regras de manipulação de caixa de entrada suspeitos** Essa diretiva profiles seu ambiente e gatilhos alertas quando suspeitas regras que excluir ou mover mensagens ou pastas são definidas na caixa de entrada do usuário. Isso pode indicar que a conta do usuário for comprometida, que as mensagens estão sendo intencionalmente ocultos e que a caixa de correio está sendo usada para distribuir spam ou malware em sua organização.

- **Suporte a grupos em políticas de permissão de aplicativo** Segurança de aplicativo de nuvem agora proporciona a capacidade de definir políticas de permissão do aplicativo de forma mais granular, com base em das associações de grupo dos usuários que são autorizados os aplicativos. Por exemplo, um administrador pode optar por definir uma política que revoga apps incomuns se eles solicitem permissões altas, somente se o usuário que as permissões de autorização é um membro do grupo Administradores.


## <a name="office-365-cloud-app-security-releases-133-134-and-135"></a>Lançamentos de segurança de aplicativo de nuvem do Office 365 133, 134 e 135

*Lançada em novembro de outubro, 2018*

**Após o [lançamento de segurança de aplicativo de nuvem do Microsoft 133, 134 e 135](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-133-134-135)**:

- **Novas políticas de detecção de anomalia** são aplicação gradualmente:
    
    - A nova política de **exfiltration dados aos aplicativos unsanctioned** é ativada automaticamente para alertá-lo quando um usuário ou o endereço IP usa um aplicativo que não é aprovado para executar uma atividade que se parece com uma tentativa para exfiltrate de informações da sua organização.
    
    - A nova política de **atividades VM excluir vários** perfis de seu ambiente e dispara alertas quando os usuários excluírem várias VMs em uma única sessão, em relação a linha de base na sua organização.

- **Suporte a descoberta de nuvem para i-Filter** O recurso de descoberta de nuvem de segurança de aplicativo de nuvem agora melhorou o suporte para o analisador de syslog i-Filter.


## <a name="office-365-cloud-app-security-release-131"></a>Versão de segurança do aplicativo de nuvem do Office 365 131

*Lançada em 16 de setembro de 2018*

**Após o [lançamento de segurança de aplicativo do Microsoft Cloud 131](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-131)**:

- **Automaticamente revogar permissões nos aplicativos do OAuth riscados** Agora você pode controlar quais aplicativos OAuth seus usuários têm acesso, por revogar permissão de aplicativo para aplicativos do OAuth no Office. Ao criar uma política de permissão do aplicativo, você agora pode definir a diretiva para revogar permissão de um aplicativo.

- **Descoberta de nuvem analisador interno adicional com suporte** Descoberta de nuvem agora é compatível com o formato de log Forcepoint nuvem de segurança de Web.

  
## <a name="office-365-cloud-app-security-release-130"></a>Versão de segurança do aplicativo de nuvem do Office 365 130

*Lançada em 5 de setembro de 2018*

**Após o [lançamento de segurança de aplicativo do Microsoft Cloud 130](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-130)**:

- **Nova barra de menus** Para fornecer uma experiência de administração mais consistente entre produtos Microsoft 365 e permitem que você dinamizar mais facilmente entre soluções de segurança da Microsoft, a barra de menus de portal de segurança de aplicativo de nuvem foi movido para o lado esquerdo da tela. A navegação consistente experiência ajuda a orientar você mesmo durante a mudança de um portal de segurança da Microsoft para outro.<br/>![Barra de menus na segurança de aplicativo de nuvem do Office](media/OCAS-MenuBar.png)<br/>

- **Impacto OAuth pontuação de aplicativo** Agora você pode enviar os comentários da equipe de segurança de aplicativo de nuvem para nos informar se houver um aplicativo de OAuth descoberto em sua organização que parece mal-intencionado. Esse novo recurso permite fazer parte da nossa comunidade de segurança e melhorar a pontuação de risco de app OAuth e análise. Para obter mais informações, consulte [Gerenciar permissões de aplicativo](manage-app-permissions-in-ocas.md).

- **Analisadores do novo descoberta de nuvem** Os analisadores de descoberta de nuvem agora suportam iboss Secure Cloud Gateway e Sophos XG.


## <a name="office-365-cloud-app-security-release-128"></a>Versão de segurança do aplicativo de nuvem do Office 365 128

*Lançada em 5 de agosto de 2018* 
  
**Após o [lançamento de segurança de aplicativo do Microsoft Cloud 128](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-128)**: 
  
- **Permissões do aplicativo entre vários aplicativos** Para aplicativos que tiverem sido concedidos permissões do aplicativo, você pode agora proibir ou aprovar vários aplicativos em uma única ação. Por exemplo, você pode examinar todos os aplicativos que receberam permissão por usuários em sua organização, selecione todos os aplicativos que você deseja proibir e clique em Proibir apps para revogar todos consentimento concedido e não são mais permitirá que os usuários conceder permissão para estes aplicativos. 
    
- **Nova consulta sugerida: pronto GDPR** Não há uma nova consulta sugerida para habilitá-lo identificar descobertos aplicativos que estão GDPR pronto. GDPR tem recentemente tornou-se uma prioridade para administradores de segurança. Esta consulta ajuda você a facilmente identificar aplicativos que estão GDPR pronto e atenuar ameaças, como avaliar o risco dos aplicativos que não estejam. 
    
## <a name="office-365-cloud-app-security-release-126"></a>Versão de segurança do aplicativo de nuvem do Office 365 126

*Lançada 7 de julho de 2018* 
  
**Após o [lançamento de segurança de aplicativo do Microsoft Cloud 126](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-126)**: 
  
- **Correção automatizada para atividades suspeitas** Agora você pode definir ações de correção automática para sessão suspeito acionada pelas políticas de detecção de anomalia. Essa melhoria permite ser alertado instantaneamente quando uma violação ocorre e aplicar ações de governança automaticamente, tais como suspender o usuário. Para obter mais informações, consulte [políticas de detecção de anomalias na segurança de aplicativo de nuvem do Office 365](anomaly-detection-policies-in-ocas.md).
    
- **Detecção automatizada de aplicativos de OAuth riscado** Além de investigar existente de aplicativos de OAuth conectados ao seu ambiente, segurança de aplicativo de nuvem do Office 365 agora permite que você definir notificações automatizadas para que você saiba quando um aplicativo OAuth atende a determinados critérios. Por exemplo, você pode automaticamente ser alertado quando há aplicativos que exigem um nível de permissão alta e eram autorizadas por mais de 50 usuários. Para obter mais informações, consulte [Gerenciar permissões de aplicativo usando a segurança de aplicativo de nuvem do Office 365](manage-app-permissions-in-ocas.md).
    
- **Suporte ao gerenciamento de provedor de serviços de segurança gerenciados (MSSP)** Segurança de aplicativo de nuvem do Office 365 agora oferece uma melhor experiência de gerenciamento para MSSPs e permite que você configure os parceiros externos como administradores com qualquer uma das funções disponíveis no momento na segurança de aplicativo de nuvem do Office 365. Além disso, os administradores com direitos de acesso a mais de um inquilino agora podem dinamizar facilmente entre os locatários. 
    
## <a name="office-365-cloud-app-security-release-124"></a>Versão de segurança do aplicativo de nuvem do Office 365 124

*Lançada em 10 de junho de 2018* 
  
**Após o [lançamento de segurança de aplicativo do Microsoft Cloud 124](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-124)**: 
  
- **Implantações de todo o escopo** Empresas forma granular podem determinar quais usuários para monitorar e proteger com base na associação de grupo. Esse recurso permite que você selecione usuários cujas atividades não serão exibidas para qualquer um dos aplicativos protegidos. Monitoramento com escopo é especialmente útil para conformidade e licenciamento. Alguns regulamentos de conformidade exigem que você evite usuários de determinados países/regiões devido às leis locais de monitoramento. E, então, você pode monitorar o menor número de usuários permaneçam dentro dos limites de suas licenças de segurança de aplicativo de nuvem do Office 365. 
    
- **Novo servidor de email** O servidor de email para segurança de aplicativo de nuvem do Office 365 foi alterado e usa os intervalos de endereços IP diferentes. Para certificar-se de que você pode obter notificações, adicione os novos endereços IP à sua lista de recursos anti-spam branca. Para organizações que personalizar suas notificações, a segurança de aplicativo de nuvem permite isso usando MailChimp, um serviço de email de terceiros. Para a lista de endereços IP do servidor de email e instruções para habilitar o trabalho com MailChimp, consulte [requisitos de rede (segurança de aplicativo do Microsoft Cloud)](https://docs.microsoft.com/cloud-app-security/network-requirements) e [configurações de email (segurança de aplicativo do Microsoft Cloud)](https://docs.microsoft.com/cloud-app-security/mail-settings).
    
## <a name="office-365-cloud-app-security-release-121"></a>Versão de segurança do aplicativo de nuvem do Office 365 121

*Lançada 6 de maio de 2018* 
  
**Após o [lançamento de segurança de aplicativo do Microsoft Cloud 121](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-121)**: 
  
- **Aprimoramentos de política de detecção de anomalia**. Políticas de detecção do título do Office 365 nuvem App anomalia foram melhoradas para incluir dois novos tipos de detecção de ameaça gradualmente divulgando: 
    
  - **Atividade Ransomware.** Recursos de detecção de ransomware são estendidos com detecção de anomalias para proporcionar mais abrangente cobertura contra ataques ransomware sofisticados. 
    
  - **Terminada a atividade do usuário.** Encerrada habilita de atividade do usuário monitorar as contas dos usuários encerradas quem pode ter sido desprovisionada de aplicativos corporativos, mas que talvez ainda têm acesso a certos recursos corporativos. 
    
    Para exibir suas [políticas de detecção de anomalias](anomaly-detection-policies-in-ocas.md), no portal de segurança de aplicativo de nuvem do Office 365, selecione **controle** \> **políticas**.
    
## <a name="office-365-cloud-app-security-release-120"></a>Versão de segurança do aplicativo de nuvem do Office 365 120

*Lançada em 22 de abril de 2018* 
  
**Após o [lançamento de segurança de aplicativo do Microsoft Cloud 120](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-120)**: 
  
- **Aplicativos internos como atividades do usuário**. Para Office 365 e Windows Azure Active Directory (AD Azure), podemos são agora gradualmente aplicação a capacidade de detectar aplicativos internos como atividades de conta de usuário realizadas pelos aplicativos do Office 365 e o Azure AD (internos e externos). Isso permite que você crie políticas para alertá-lo a se um aplicativo realiza atividades inesperadas e não autorizadas. 
    
- **Exportar mais campos na lista de permissões do aplicativo**. Ao exportar uma lista de permissões do aplicativo para csv, campos adicionais, como o publisher, o uso de comunidade e nível de permissões são incluídos para ajudar o processo de conformidade e investigação. 
    
## <a name="office-365-cloud-app-security-release-119"></a>Versão de segurança do aplicativo de nuvem do Office 365 119

*Lançada 1 de abril de 2018* 
  
**Após o [lançamento de segurança de aplicativo do Microsoft Cloud 119](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-119)**: 
  
- **Aprimoramentos para descoberta de nuvem**. A descoberta de nuvem fornece mais informações sobre os principais usuários e endereços IP, tornando mais fácil para exibir detalhes de uso sobre o Office 365 e outros aplicativos. Para saber mais, consulte [descobertas de descoberta de aplicativo da revisão na segurança de aplicativo de nuvem do Office 365](review-app-discovery-findings-in-ocas.md).
    
    ![O painel de descoberta de nuvem foi atualizado](media/12712681-c0b3-4cb3-b7fd-2cf2ad4e825f.png)
  
## <a name="office-365-cloud-app-security-release-118"></a>Versão de segurança do aplicativo de nuvem do Office 365 118

*Lançada 18 de março de 2018* 
  
**Após o [lançamento de segurança de aplicativo do Microsoft Cloud 118](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-118)**: 
  
- **Suporte a barracuda**. Descoberta de nuvem agora oferece suporte a série de F Barracuda firewalls e série Barracuda F firewall web log streaming. 
    
## <a name="office-365-cloud-app-security-release-117"></a>Versão de segurança do aplicativo de nuvem do Office 365 117

*Lançada 6 de março de 2018* 
  
**Após o [lançamento de segurança de aplicativo do Microsoft Cloud 117](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-117)**: 
  
- **suporte de i-FILTER**. Descoberta de nuvem agora oferece suporte a i-FILTER. 
    
## <a name="office-365-cloud-app-security-release-116"></a>Versão de segurança do aplicativo de nuvem do Office 365 116

*Lançada 18 de fevereiro de 2018* 
  
**Após o [lançamento de segurança de aplicativo do Microsoft Cloud 116](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-116)**: 
  
- **Aprimoramentos na diretiva de detecção de anomalia**. Políticas de detecção de anomalias em segurança de aplicativo de nuvem do Office 365 foram aprimorados com novas detecções baseado em cenário incluindo impossíveis viagens, a atividade de um endereço IP suspeito e tentativas de login vários. As novas políticas são automaticamente habilitadas, fornecendo detecção de ameaça da caixa em seu ambiente de nuvem. Além disso, as novas políticas exponham mais dados do mecanismo de detecção de segurança de aplicativo de nuvem do Office 365, que pode ajudar a acelerar o processo de investigação e conter ameaças em andamento. Para saber mais, consulte o artigo de segurança de aplicativo do Microsoft Cloud, [Obtenha instantâneo analytics comportamento e detecção de anomalias](https://docs.microsoft.com/cloud-app-security/anomaly-detection-policy).
    
- **Suporte do analisador de log para formatos de ponto de verificação**. Analisadores de log a descoberta de nuvem agora suportam dois formatos adicionais de ponto de verificação: XML e KPC. 
    
## <a name="office-365-cloud-app-security-release-114"></a>Versão de segurança do aplicativo de nuvem do Office 365 114

*Lançada 21 de janeiro de 2018* 
  
**Após o [lançamento de segurança de aplicativo do Microsoft Cloud 114](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-114)**: 
  
- **Status do serviço**. Agora você pode verificar o status atual do serviço de segurança de aplicativo de nuvem do Office 365 indo para **ajudar a** \> **status do sistema**. 
    
    ![Clique em Ajuda \> Status do sistema para exibir o status de integridade do sistema](media/2b496dac-ed9d-4480-83b6-85f9510d3aea.png)
  
- **Consultas personalizadas para o log de atividade**. Começando na versão 114, a capacidade de criar e salvar consultas personalizadas no log de atividade está aplicação gradualmente. Consultas personalizadas permitem que você criar modelos de filtro que podem ser reutilizados para aprofundar investigação. Além disso, sugerido consultas foram adicionados para fornecer modelos de caixa investigação para filtrar suas atividades e detectados apps. Filtros personalizados para identificar riscos como atividades de representação, as atividades de administrador, aplicativos de armazenamento de nuvem incompatíveis riscado, aplicativos empresariais com criptografia fraca e os riscos de segurança incluem as consultas sugeridas. Use as consultas sugeridas como um ponto de partida, modificá-los conforme necessário e salvá-las como uma nova consulta. 
    
## <a name="office-365-cloud-app-security-release-113"></a>Versão de segurança do aplicativo de nuvem do Office 365 113

*Lançada em 8 de janeiro de 2018* 
  
**Após o [lançamento de segurança de aplicativo do Microsoft Cloud 113](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-113)**: 
  
- **Suporte de analisador de log para formatos genéricos**. Analisadores de log a descoberta de nuvem agora suportam os seguintes formatos genéricos: LEEF, CEF e W3C. 
    
## <a name="office-365-cloud-app-security-release-112"></a>Versão de segurança do aplicativo de nuvem do Office 365 112

*Lançada em 24 de dezembro de 2017* 
  
**Após o [lançamento de segurança de aplicativo do Microsoft Cloud 112](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-112)**: 
  
- **Gaveta insight relevantes**. No registro de atividades, agora você pode acessar o dinheiro insight relevantes clicando em um nome de usuário ou o endereço IP. 
    
    ![Clique em um nome de usuário ou o endereço IP para ver o dinheiro insight relevantes no log de atividade.](media/8e32b3fa-8c0c-4c5e-b248-fe7d7e1b516d.png)
  
- **Habilidade de exibir mais atividades com um clique**. No dinheiro insight relevantes, você pode clicar no ícone de relógio para exibir todas as atividades realizadas dentro de uma atividade selecionada 48 horas. 
    
    ![No dinheiro ideias relevantes, você pode clicar no ícone de relógio para ver as atividades realizadas dentro de uma atividade selecionada 48 horas](media/c6c96aa0-98e5-4205-8873-45f8d6fd0843.png)
  
- **Melhorias do analisador de log para SRX Juniper**. Foram feitas melhorias para o analisador de log de descoberta de nuvem para SRX Juniper. 
    
## <a name="office-365-cloud-app-security-release-111"></a>Versão de segurança do aplicativo de nuvem do Office 365 111

*Lançada em 10 de dezembro de 2017* 
  
**Após o [lançamento de segurança de aplicativo do Microsoft Cloud 111](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-111)**: 
  
- **Aprimoramentos de filtro de tempo**. Filtros de tempo agora são mais fáceis de usar. Para acessar um filtro de tempo, em um modo de exibição, como alertas de log, políticas, atividade, usando o modo de exibição avançado, escolha a **Data** na lista de filtros. Escolha uma opção, como antes, depois ou entre para aplicar o filtro de tempo. 
    
    ![Use o filtro de data para exibir informações antes, depois ou entre datas.](media/9dbb2a10-f68f-413b-8b4e-88911152cb92.png)
  
## <a name="office-365-cloud-app-security-release-110"></a>Versão de segurança do aplicativo de nuvem do Office 365 110

*Lançada em 26 de novembro de 2017* 
  
**Após o [lançamento de segurança de aplicativo do Microsoft Cloud 110](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-110)**: 
  
- **Integração do servidor SIEM agora disponível**. Conecte seu servidor SIEM à segurança de aplicativo de nuvem do Office 365. Agora você pode enviar alertas e atividades automaticamente ao seu servidor SIEM de escolha Configurando agentes SIEM. Consulte [integra-se seu servidor SIEM com segurança de aplicativo de nuvem do Office 365](integrate-your-siem-server-with-office-365-cas.md).
    
- **Facilitar o acesso ao conteúdo da Ajuda**. Usando o novo ponto de interrogação no canto superior direito, agora você pode acessar o conteúdo da Ajuda de dentro de páginas do portal da segurança de aplicativo de nuvem do Office 365. Cada link é sensível ao contexto, levando você para as informações que necessárias, com base na página em que você está. 
    
- **Envie seus comentários**. Usando o rosto feliz no canto superior direito, agora você pode enviar comentários de cada página do portal da segurança de aplicativo de nuvem do Office 365. Isso permite que você relatar bugs, solicitar novos recursos e compartilhar sua experiência diretamente com a equipe de segurança de aplicativo de nuvem do Office 365. 
    
## <a name="office-365-cloud-app-security-release-102"></a>Versão de segurança do aplicativo de nuvem do Office 365 102

*Lançada em 13 de agosto de 2017* 
  
**Após o [lançamento de segurança de aplicativo do Microsoft Cloud 102](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-102)**: 
  
- **Novas ações de investigação de usuário** habilitar um nível de detalhamento adicional para investigações de usuário. Em uma página de investigar, você pode focalizar em uma atividade, o usuário ou a conta e aplicá-la como um filtro e a partir daí, você pode exibir as atividades relacionadas ou eventos. 
    
## <a name="office-365-cloud-app-security-release-100"></a>Versão de segurança do aplicativo de nuvem do Office 365 100

*Lançada em 17 de julho de 2017* 
  
**Após o [lançamento de segurança de aplicativo do Microsoft Cloud 100](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-100)**: 
  
- **Extensões de segurança** é um novo painel onde é possível gerenciar centralmente todas as suas extensões de segurança para Office 365 nuvem App segurança, incluindo tokens de API e agentes SIEM. Para exibir o painel de extensões de segurança, siga estas etapas: 
    
1. Vá para [https://protection.office.com](https://protection.office.com) e entrar usando sua conta de trabalho ou da escola para o Office 365. (Isso leva você para a segurança &amp; Centro de conformidade.) 
    
2. Vá para **alertas** \> **avançadas de gerenciar alertas**.
    
3. Escolha **vá para segurança de aplicativo do Office 365 nuvem**.
    
    ![Na segurança &amp; Centro de conformidade, escolha alertas \> gerenciar avançadas alertas \> vá para gerenciamento de segurança avançada](media/9792b121-9cd4-4faa-a6e0-81cfab4bf2f2.png)
  
4. Escolha **configurações** \> **extensões de segurança**.
    
    ![No portal do ASM, escolha configurações \> extensões de segurança](media/f03d47a1-91ff-41b9-9baf-b514cffe41a8.png)
  
- **Melhoria de análise**. Aperfeiçoamentos foram feitos no log de descoberta de nuvem do mecanismo de análise. Erros internos são consideravelmente menos suscetíveis a ocorrer. 
    
- **Formatos de log previstos**. O formato de log esperada para logs de descoberta de nuvem agora exemplifica para ambos os formatos de Syslog e FTP. 
    
## <a name="related-topics"></a>Tópicos relacionados

[Conteúdo da Ajuda do Office 365 segurança de aplicativo de nuvem](office-365-cas-help.md)
  
[Atividades de utilização após a implantação do Office 365 Cloud App Security](utilization-activities-for-ocas.md)
  
[Permissões de segurança do Office 365 &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md)
  


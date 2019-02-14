---
title: Mapa de segurança do Office 365 - principais prioridades para os primeiros 30 dias, 90 dias e além
ms.author: bcarter
author: BrendaCarter
manager: laurawi
ms.date: 10/08/2018
ms.audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Ent_O365
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
ms.assetid: 28c86a1c-e4dd-4aad-a2a6-c768a21cb352
description: 'Principais recomendações da equipe de cybersecurity da Microsoft para implementar os recursos de segurança para proteger seu ambiente do Office 365. '
ms.openlocfilehash: ce7b4371a284763c506ea4e1a06a63dbf2968ae5
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995282"
---
# <a name="office-365-security-roadmap---top-priorities-for-the-first-30-days-90-days-and-beyond"></a>Mapa de segurança do Office 365 - principais prioridades para os primeiros 30 dias, 90 dias e além

Este artigo inclui as principais recomendações da equipe de cybersecurity da Microsoft para implementar os recursos de segurança para proteger seu ambiente do Office 365. Este artigo foi adaptado de uma sessão do Microsoft Ignite — [seguro do Office 365 como um profissional de cybersecurity: principais prioridades para os primeiros 30 dias, 90 dias e além](https://www.youtube.com/watch?v=luignzNyR-o). Esta sessão foi desenvolvido e apresentado por Mark Simos e Matt Kemelhar, arquitetos de Cybersecurity da empresa.
  
Neste artigo:
  
- [Resultados do mapa](security-roadmap.md#Roadmap)
    
- [30 dias — poderosas wins rápidas](security-roadmap.md#Thirdaydays)
    
- [90 dias — enhanced proteções](security-roadmap.md#Ninetydays)
    
- [Além](security-roadmap.md#Beyond)
    
## <a name="roadmap-outcomes"></a>Resultados do mapa
<a name="Roadmap"> </a>

Estas recomendações de mapa são testadas em três fases em uma ordem lógica com os seguintes objetivos.

|||
|:-----|:-----|
| |Resultados
|30 dias|Configuração rápida:  <br/> • Proteções de admin básica  <br/> • Registro e análise  <br/> • Proteções de identidade básica  <br/> Configuração do inquilino  <br/>  Preparar os participantes  <br/> |
|90 dias|Proteções de avançadas:  <br/> • Contas de administração  <br/>  • Dados &amp; contas de usuário  <br/>  Visibilidade às necessidades de conformidade, ameaça e usuário  <br/>  Adaptar-se e implementar proteções e políticas padrão  <br/> |
|Além|Ajustar e refinar os principais políticas e controles  <br/> Estender proteções de dependências de local  <br/> Integração com processos comerciais e de segurança (legais, ameaça interna, etc.)  <br/> |
  

   
## <a name="30-days--powerful-quick-wins"></a>30 dias — poderosas wins rápidas
<a name="Thirdaydays"> </a>

Essas tarefas podem ser realizadas rapidamente e tem baixo impacto para os usuários.
  
|||
|:-----|:-----|
|Área  <br/> |Tasks  <br/> |
|Gerenciamento de segurança  <br/> |• Verificar pontuação seguro e tome nota das sua pontuação atual ( [https://securescore.office.com](https://securescore.office.com)).  <br/>  • Ativar o log de auditoria para o Office 365. Consulte [Pesquisar o log de auditoria de segurança do Office 365 &amp; Centro de conformidade](search-the-audit-log-in-security-and-compliance.md).<br/> • [Configure seu locatário do Office 365 para aumentar a segurança](tenant-wide-setup-for-increased-security.md) .  <br/>  • Examine regularmente painéis e relatórios na segurança do Office 365 e Centro de conformidade e segurança de aplicativo de nuvem.  <br/> |
|Proteção contra Ameaças  <br/> |[Conectar o Office 365 para segurança de aplicativo do Microsoft Cloud](https://docs.microsoft.com/cloud-app-security/connect-office-365-to-microsoft-cloud-app-security) ao iniciar a monitoração usando as políticas de detecção de ameaça padrão para comportamentos anômalos. Leva sete dias para criar uma linha de base para detecção de anomalias.<br><br/>  Implementar a proteção para contas de administração:  <br/> • Usar dedicada admin accounts para atividade de admin.  <br/>  • Impor a autenticação multifator (MFA) para contas de administrador.  <br/>  • Usar um [altamente seguros dispositivo Windows 10](https://docs.microsoft.com/windows-hardware/design/device-experiences/oem-highly-secure) para atividade de admin.  <br/> |
|Gerenciamento de identidades e acesso  <br/> |• [Habilitar a proteção de identidade do Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-identityprotection-enable).  <br/> • Para ambientes de identidade federada, impor a segurança da conta (comprimento da senha, idade, complexidade, etc.).  <br/> |
|Proteção de informações  <br/> | Revise as recomendações de proteção de informações de exemplo. Proteção das informações requer coordenação em toda a organização. Introdução a estes recursos:<br/> • [Proteção do office 365 informações para GDPR](http://aka.ms/o365gdpr) <br/> • [Arquivos e sites seguro do SharePoint Online](https://docs.microsoft.com/Office365/enterprise/secure-sharepoint-online-sites-and-files) (inclui compartilhamento, classificação, prevenção de perda de dados e proteção de informações do Windows Azure)  <br/> |
   
## <a name="90-days--enhanced-protections"></a>90 dias — enhanced proteções
<a name="Ninetydays"> </a>

Essas tarefas demoram um pouco mais para planejar e implementar, mas aumentam significativamente as condições de segurança. 
  
|||
|:-----|:-----|
|Área  <br/> |Tarefa  <br/> |
|Gerenciamento de segurança  <br/> | • Verificar pontuação seguro para as ações recomendadas para seu ambiente ( [https://securescore.office.com](https://securescore.office.com)).  <br/>  • Continuam a examinar regularmente painéis e relatórios na segurança do Office 365 e Centro de conformidade, segurança de aplicativo de nuvem e ferramentas SIEM.  <br/>  • Procure e implementar atualizações de software.  <br/>  • Simulações de ataque de conduta para lança-phishing, borrifada de senha e senha brute-force attacks usando [Simulador de ataque](https://support.office.com/article/attack-simulator-office-365-da5845db-c578-4a41-b2cb-5a09689a551b) (incluído no [Office 365 Threat Intelligence](office-365-ti.md)).  <br/>  • Olhar para o compartilhamento de risco examinando os relatórios internos na segurança do aplicativo de nuvem (na guia investigar).  <br/>  • Verifique o [Gerenciador de conformidade](meet-data-protection-and-regulatory-reqs-using-microsoft-cloud.md) para examinar o status de normas que se aplicam à sua organização (por exemplo, GDPR, NIST 800-171).  <br/> |
|Proteção contra Ameaças  <br/> | Implemente proteções avançadas para contas de administração:  <br/>  • Configure [Privilegiado estações de trabalho do Access](https://docs.microsoft.com/windows-server/identity/securing-privileged-access/privileged-access-workstations) (patas) de atividade de admin.  <br/>  • Configurar o [gerenciamento de identidade privilegiada do Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-privileged-identity-management-configure).  <br/>  • Configure uma segurança eventos e informações (SIEM) ferramenta de gerenciamento para coletar dados de registro em log do Office 365, segurança de aplicativo de nuvem e outros serviços, inclusive o AD FS. O Log de auditoria do Office 365 armazena dados por apenas 90 dias. Capturar dados na ferramenta SIEM permite que você armazene dados por um período maior.<br/> |
|Gerenciamento de identidades e acesso  <br/> | • Habilite e impor MFA para todos os usuários.  <br/>  • Implementar um conjunto de [acesso condicional e políticas relacionadas](https://docs.microsoft.com/en-us/microsoft-365/enterprise/microsoft-365-policies-configurations). |
|Proteção de informações  <br/> | Adaptar e implementar políticas de proteção de informações. Esses recursos incluem exemplos:<br/> • [Proteção do office 365 informações para GDPR](http://aka.ms/o365gdpr) <br/> • [Arquivos e sites seguro do SharePoint Online](https://docs.microsoft.com/Office365/enterprise/secure-sharepoint-online-sites-and-files) <br/> <br> Políticas de prevenção de perda de dados de uso e ferramentas de monitoramento no Office 365 para dados armazenados no Office 365 (em vez de segurança de aplicativo de nuvem). <br><br>Use a segurança de aplicativo de nuvem com o Office 365 para avançados recursos (além de prevenção de perda de dados) de alerta.  <br/> |
   
## <a name="beyond"></a>Além
<a name="Beyond"> </a>

Estas são as medidas de segurança importantes que se baseiam em trabalhos anterior. 
  
|||
|:-----|:-----|
|Área  <br/> |Tarefa  <br/> |
|Gerenciamento de segurança  <br/> |• Continuar a planejar as próximas ações usando pontuação seguro ( [https://securescore.office.com](https://securescore.office.com)).  <br/>  • Continuam a examinar regularmente painéis e relatórios na segurança do Office 365 e Centro de conformidade, segurança de aplicativo de nuvem e ferramentas SIEM.  <br/>  • Continuam a procurar e implementar atualizações de software.  <br/>  • Integrar o eDiscovery em seu legais e processos de resposta de ameaça.  <br/> |
|Proteção contra Ameaças  <br/> | • Implementar o [Acesso privilegiado seguro](https://docs.microsoft.com/windows-server/identity/securing-privileged-access/securing-privileged-access) (SPA) para componentes de identidade no local (AD, o AD FS).  <br/>  • Segurança de aplicativo de nuvem de uso para o monitoramento de ameaças internas.  <br/>  • Descobrir o uso de TI SaaS sombra usando a segurança de aplicativo de nuvem.  <br/> |
|Gerenciamento de identidades e acesso  <br/> | • Refinar políticas de proteção de informações:  <br/>  • Proteção de informações azure e o Office 365 prevenção de perda de dados (DLP).  <br/>  • Políticas de segurança de aplicativo de nuvem e alertas.  <br/> |
|Proteção de informações  <br/> | • Refinar políticas e processos operacionais.  <br/>  • Proteção de identidade de usar o Windows Azure AD para identificar as ameaças internas.  <br/> |
   
Consulte também: [como atenuar rapid cyberattacks como Petya e WannaCrypt](https://cloudblogs.microsoft.com/microsoftsecure/2018/02/21/how-to-mitigate-rapid-cyberattacks-such-as-petya-and-wannacrypt/). 
  


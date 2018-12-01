---
title: Configurar seu locatário do Office 365 para aumentar a segurança
ms.author: bcarter
author: BrendaCarter
manager: laurawi
ms.date: 10/11/2018
ms.audience: ITPro
ms.topic: get-started-article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MET150
ms.assetid: 8d274fe3-db51-4107-ba64-865e7155b355
description: O orienta durante a configuração recomendada para configurações de todo o locatário que afetam a segurança do seu ambiente do Office 365. Suas necessidades de segurança podem exigir mais ou menos segurança. Use estas recomendações como um ponto de partida.
ms.openlocfilehash: af34d4b70c5cc1122dab840f9b4af8e2fe3c3a30
ms.sourcegitcommit: c34f1a0d560117153fc9a7b8da8994bc6fc53791
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/30/2018
ms.locfileid: "27118107"
---
# <a name="configure-your-office-365-tenant-for-increased-security"></a>Configurar seu locatário do Office 365 para aumentar a segurança

Este tópico explora a configuração recomendada para todo o locatário configurações que afetam a segurança do seu ambiente do Office 365. Suas necessidades de segurança podem exigir mais ou menos segurança. Use estas recomendações como um ponto de partida.
  
## <a name="check-office-365-secure-score"></a>Verificar a pontuação de seguro do Office 365

O Office 365 seguro pontuação analisa a segurança do sua organização Office 365 com base nas suas atividades regulares e configurações de segurança e atribui uma pontuação. Comece executando-se nota de sua pontuação atual. Ajustar algumas configurações de todo o locatário aumentará sua pontuação. O objetivo é não para obter a máxima pontuação, mas a serem consideradas oportunidades para proteger seu ambiente que não afetam negativamente a produtividade para seus usuários. Consulte [apresentando a pontuação de seguro do Office 365](office-365-secure-score.md).
  
## <a name="tune-threat-management-policies-in-the-office-365-security-amp-compliance-center"></a>Ajustar as políticas de gerenciamento de ameaça no Office 365 Security &amp; Centro de conformidade

A segurança do Office 365 &amp; Centro de conformidade inclui recursos de proteger seu ambiente. Ele também inclui relatórios e painéis que você pode usar para monitorar e executar ação. Algumas áreas vêm com configurações de diretiva padrão. Algumas áreas não incluir políticas padrão ou regras. Visite a essas políticas em gerenciamento de ameaça para ajustar as configurações de gerenciamento de ameaça para um ambiente mais seguro. 
  
|Área * * *|Inclui um padrão política * * *|Recomendação * * *|
|:-----|:-----|:-----|
|**AntiPhishing** <br/> |Sim  <br/> | Se você tiver um domínio personalizado, crie uma política de AntiPhishing para proteger as contas de email dos seus usuários mais valiosos, como o CEO e proteger seu domínio. Revise a [Configurar uma política de AntiPhishing](set-up-anti-phishing-policies.md) e criar uma política utilizando o exemplo como um guia: "exemplo: política de AntiPhishing para proteger um usuário e um domínio."|
|**Mecanismo antimalware** <br/> |Sim  <br/> | Edite a política padrão:  <br/> Tipos de filtro do anexo comuns de • — selecione ativado  <br/><br>  Você também pode criar políticas de filtro de malware personalizado e aplicá-las a usuários especificados, grupos ou domínios em sua organização.  <br/> <br> Mais informações:  <br/> • [Proteção contra malware](https://technet.microsoft.com/en-us/library/jj200669%28v=exchg.150%29.aspx) <br/> • [Configurar políticas de antimalware](https://technet.microsoft.com/en-us/library/jj200745%28v=exchg.150%29.aspx) <br/> |
|**Anexos seguros de ATP** <br/> |Não  <br/> | Na página principal para anexos seguros, protege arquivos no SharePoint, OneDrive e Teams da Microsoft, marcando essa caixa:  <br/>  • Ativar ATP para SharePoint, OneDrive e equipes da Microsoft  <br/> <br> Adicione uma nova diretiva de segurança de anexo com estas configurações:  <br/>  • Bloco — bloquear a atuais e futuros emails e anexos com malware detectado (escolher essa opção)  <br/>  • Enable redirecionar — (essa caixa de seleção e insira um endereço de email, como uma conta de administrador ou quarentena)  <br/>  • Aplicar a seleção acima se esgotar o tempo limite malware faça a verificação de anexos ou ocorrerá erro (essa caixa de seleção)  <br/>  • Aplicadas ao — domínio do destinatário é (selecione seu domínio)  <br/>  <br>Obter mais informações: [Configurar políticas de anexos seguros ATP do Office 365](set-up-atp-safe-attachments-policies.md) <br/> |
|**Links seguros ATP** <br/> |Sim  <br/> | Adicione essa configuração para a política padrão para toda a organização:  <br/> • Links de seguros de uso em: Office 365 ProPlus, Office para iOS e Android (Selecione esta opção).  <br/> <br>Política recomendada para destinatários específicos:  <br/>  • URLs serão reconfigurados e verificadas em relação a uma lista de links mal-intencionado conhecidos, quando o usuário clica no link (Selecione esta opção).  <br/>  • Anexos seguros de uso para examinar o conteúdo baixável (essa caixa de seleção).  <br/>  • Aplicadas ao — domínio do destinatário é (selecione seu domínio).  <br/> <br> Obter mais informações: [links de seguros ATP do Office 365](atp-safe-links.md).  <br/> |
|**Anti-Spam (filtragem de email)** <br/> |Sim  <br/> | O que deve tomar para:  <br/>  • Muito spam — escolha as configurações personalizadas e editar a política de filtro de spam padrão.  <br/>  • Inteligência de falsificação — examine remetentes que são falsificação de seu domínio. Bloquear ou permitir desses remetentes.<br/>  <br>Obter mais informações: [Proteção de Anti-Spam de Email do Office 365](anti-spam-protection.md).  <br/> |
|**DKIM (DomainKeys identificado Mail)** <br/> |Sim  <br/> |DKIM é um processo de autenticação que pode ajudar a proteger os remetentes e destinatários para falsificado (FALSO) e email de phishing. Seu locatário inclui uma assinatura padrão para seu domínio. Crie uma assinatura de verificação adicional se você adicionar domínios personalizados ao seu locatário.<br/> <br>Use as instruções deste artigo para configurar uma nova assinatura DKIM, incluindo os registros CNAME, SPF e DMARC: [Verificação de uso para validar emails de saída enviados a partir de seu domínio personalizado no Office 365](https://docs.microsoft.com/office365/SecurityCompliance/use-dkim-to-validate-outbound-email).  <br/> |
   
## <a name="view-dashboards-and-reports-in-the-security-amp-compliance-center"></a>Exibir relatórios e painéis na segurança &amp; Centro de conformidade

Visite esses relatórios e painéis para saber mais sobre a integridade do seu ambiente. Os dados nesses relatórios se tornará mais ricas conforme sua organização usa os serviços do Office 365. No momento, estar familiarizado com o que você pode monitorar e agir em relação. Para obter mais informações, consulte: [Reports in a segurança do Office 365 &amp; Centro de conformidade](reports-in-security-and-compliance.md).
  
|Painel * * *|****Descrição****|
|:-----|:-----|
|Painel de gerenciamento de ameaça  <br/> |Na seção Gerenciamento de ameaças de segurança &amp; conformidade centraliza, use esse painel, consulte ameaças que já foram tratadas e como uma ferramenta útil para relatórios check-out para os tomadores de decisão de negócios em que o ameaça Intelligence já tenha feito para proteger sua negócios.  <br/> |
|Gerenciador de ameaça  <br/> |Isso também é na seção Gerenciamento de ameaças de segurança &amp; Centro de conformidade. Se você estiver investigando ou experimentando um ataque contra seu locatário do Office 365, use o Gerenciador de ameaça para analisar as ameaças. Gerenciador de ameaça mostra o volume de ataques ao longo do tempo e você pode analisar dados por famílias de ameaça, a infra-estrutura do invasor e muito mais. Você também pode marcar qualquer email suspeita para a lista de incidentes.  <br/> |
|Relatórios — painel  <br/> |Na seção relatórios de segurança &amp; relatórios de auditoria de modo de exibição do Centro de conformidade, para suas organizações do SharePoint Online e o Exchange Online. Você também pode acessar Azure AD (Active Directory) usuário entrar relatórios, relatórios de atividade do usuário e do log de auditoria do Azure AD da página exibir relatórios.  <br/> |
   
![Segurança &amp; painel do Centro de conformidade](media/870ab776-36d2-49c7-b615-93b2bc42fce5.png)
  
## <a name="configure-additional-exchange-online-tenant-wide-settings"></a>Definir configurações adicionais de todo o inquilino Exchange Online

Muitos dos controles de segurança e proteção no Centro de administração do Exchange também são incluídos no Centro de conformidade de segurança e. Você não precisará configurá-los em ambos os lugares. Aqui estão algumas configurações adicionais que são recomendados. 
  
|Área * * *|Inclui um padrão política * * *|Recomendação * * *|
|:-----|:-----|:-----|
|**Fluxo de emails** (As regras de transporte)  <br/> |Não  <br/> | Adicione uma regra de fluxo de email para se proteger contra ransomware. Consulte "Como usar regras de transporte do Exchange para acompanhar ou bloquear emails com extensões de arquivo usadas pelo ransomware" neste artigo de blog: [como lidar com ransomware](https://blogs.technet.microsoft.com/office365security/how-to-deal-with-ransomware/).<br><br/> Crie uma regra de transporte para impedir que o encaminhamento automático de email para domínios externos. Para obter mais informações, consulte [Atenuando cliente externo regras de encaminhamento com pontuação seguro](https://blogs.technet.microsoft.com/office365security/mitigating-client-external-forwarding-rules-with-secure-score/).<br/> <br>Obter mais informações: [Mail flow regras (regras de transporte) no Exchange Online](https://technet.microsoft.com/en-us/library/jj919238%28v=exchg.150%29.aspx) <br/> |
|**Habilitar autenticação moderna** <br/> |Não  <br/> | Autenticação moderna no Office 365 é um pré-requisito para usar a autenticação multifator (MFA). MFA é recomendada para proteger o acesso aos recursos de nuvem, incluindo email.<br/>  <br>Consulte estes tópicos:  <br/> • [Habilitar ou desabilitar a autenticação moderna no Exchange Online](https://support.office.com/article/58018196-f918-49cd-8238-56f57f38d662) <br/> • [Skype para Business Online: habilitar o seu locatário para autenticação moderno](https://social.technet.microsoft.com/wiki/contents/articles/34339.skype-for-business-online-enable-your-tenant-for-modern-authentication.aspx) <br/>  <br>Autenticação moderna está habilitada por padrão para o Office 2016 clientes, SharePoint Online e OneDrive for Business.  <br/>  <br>Obter mais informações: [a autenticação moderna com clientes do Office usando o Office 365](https://support.office.com/article/776c0036-66fd-41cb-8928-5495c0f9168a) <br/> |
   
## <a name="configure-tenant-wide-sharing-policies-in-sharepoint-admin-center"></a>Configurar políticas de compartilhamento de todo o inquilino no Centro de administração do SharePoint

Recomendações da Microsoft para configurar sites de equipe do SharePoint em aumentando os níveis de proteção, começando com a proteção de linha de base. Para obter mais informações, consulte [arquivos e sites seguro do SharePoint Online](https://docs.microsoft.com/microsoft-365-enterprise/secure-sharepoint-online-sites-and-files)
  
Sites de equipe do SharePoint definidas no nível da linha de base permitem o compartilhamento de arquivos com usuários externos usando links de acesso anônimo. Essa abordagem é recomendada em vez de enviando arquivos em email. 
  
Para suportar as metas para proteção da linha de base, defina as políticas de compartilhamento de todo o locatário, conforme recomendado aqui. Configurações para sites individuais de compartilhamento podem ser mais restritivas do que esta política de todo o locatário, mas não mais permissivo. 
  
|Área * * *|Inclui um padrão política * * *|Recomendação * * *|
|:-----|:-----|:-----|
|**Compartilhamento** (SharePoint Online e OneDrive for Business)  <br/> |Sim  <br/> | Compartilhamento externo é habilitado por padrão. Essas configurações são recomendadas:<br/>  • Permitir compartilhamento autenticados usuários externos e o uso de links de acesso anônimo (configuração padrão).  <br/>  • Links de acesso anônimo expiram nesta quantidade de dias. Insira um número, se desejado, como 30 dias.<br/>  Tipo de vínculo • padrão — Selecione interno (pessoas na organização apenas). Os usuários que desejam compartilhar usando links anônimo devem escolher esta opção no menu compartilhamento.<br/>  <br>Obter mais informações: [Visão geral do compartilhamento externo](https://support.office.com/article/c8a462eb-0723-4b0b-8d0a-70feafe4be85) <br/> |
   
Centro de administração do SharePoint e o OneDrive for Business admin center incluem as mesmas configurações. As configurações em um centro de administração se aplicam a ambos.
  
## <a name="configure-settings-in-azure-active-directory"></a>Definir as configurações no Windows Azure Active Directory

Certifique-se de que a visitar essas duas áreas no Windows Azure Active Directory para concluir a instalação de todo o locatário para ambientes mais seguros.
  
### <a name="configure-named-locations-under-conditional-access"></a>Configurar locais nomeadas (em acesso condicional)

Se sua organização incluir escritórios com acesso à rede segura, adicione os intervalos de endereços IP confiáveis para o Windows Azure Active Directory como locais nomeados. Esse recurso ajuda a reduzir o número de relatada falsos positivos para eventos de entrada risco. 
  
Consulte: [locais nomeada no Windows Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-named-locations)
  
### <a name="block-apps-that-dont-support-modern-authentication"></a>Bloquear aplicativos que não há suporte para autenticação moderna

A autenticação multifator requer aplicativos que oferecem suporte à autenticação moderna. Aplicativos que não têm suporte para autenticação moderna não podem ser bloqueados usando regras de acesso condicional.
  
Para ambientes seguros, certifique-se de desabilitar a autenticação para aplicativos que não têm suporte para autenticação moderna. Você pode fazer isso no Windows Azure Active Directory com um controle que estarão disponíveis em breve.
  
Enquanto isso, use um dos seguintes métodos para realizar essa tarefa para o SharePoint Online e o OneDrive for Business:
  
- Usar o PowerShell, consulte [bloquear aplicativos que não usam autenticação moderna](https://docs.microsoft.com/intune-classic/deploy-use/block-apps-with-no-modern-authentication).
    
- Configurá-lo no Centro de administração do SharePoint no "página de acesso de dispositivo —"Controlar o acesso a partir de aplicativos que não usam a autenticação moderna." Escolha bloquear. 
    
## <a name="get-started-with-cloud-app-security-or-office-365-cloud-app-security"></a>Introdução ao segurança de aplicativo de nuvem ou segurança de aplicativo de nuvem do Office 365

Use segurança de aplicativo de nuvem do Office 365 para avaliar o risco, para um alerta atividades suspeitas e deverá executar automaticamente uma ação. Requer o plano do Office 365 E5.
  
Ou, use a segurança de aplicativo de nuvem Microsoft para obter mais aprofundada visibilidade par depois que o acesso seja concedido, controles abrangentes e proteção aprimorada para todos os aplicativos de nuvem, incluindo o Office 365. 
  
Porque esta solução recomenda o plano de EMS E5, recomendamos que você inicie com segurança de aplicativo de nuvem para que você possa usar isso com outros aplicativos SaaS em seu ambiente. Inicie com as configurações e políticas padrão.
  
Mais informações:
  
- [Implantar o Cloud App Security](https://docs.microsoft.com/cloud-app-security/getting-started-with-cloud-app-security)
    
- [Mais informações sobre o Microsoft Cloud App Security](https://www.microsoft.com/en-us/cloud-platform/cloud-app-security)
    
- [Visão geral do Office 365 Cloud App Security](office-365-cas-overview.md)
    
![Painel do Cloud App Security](media/1fb2aa65-54b8-4746-9f5e-c187d339e9f5.png)
  
## <a name="additional-resources"></a>Recursos adicionais

Estes artigos e guias fornecem informações prescritivas adicionais para proteger seu ambiente do Office 365:
  
- [Diretrizes de segurança da Microsoft para campanhas políticas, organizações sem fins lucrativos e outras organizações ágil](https://docs.microsoft.com/microsoft-365-enterprise/microsoft-security-guidance) (você pode usar essas recomendação em qualquer ambiente, especialmente os ambientes somente nuvem) 
    
- [Recomendado diretivas de segurança e as configurações para identidades e dispositivos](https://docs.microsoft.com/microsoft-365-enterprise/microsoft-365-policies-configurations) (essas recomendações incluem ajuda para ambientes do AD FS) 
    


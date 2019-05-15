---
title: Configure o locatário do Office 365 para aumentar a segurança
ms.author: bcarter
author: BrendaCarter
manager: laurawi
ms.date: 10/11/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Ent_O365
- Strat_O365_IP
- M365-security-compliance
search.appverid: MET150
ms.assetid: 8d274fe3-db51-4107-ba64-865e7155b355
description: Orienta você na configuração recomendada para definições de todos os locatários que afetam a segurança de seu ambiente do Office 365. Suas necessidades de segurança podem exigir mais ou menos segurança. Use estas recomendações como ponto de partida.
ms.openlocfilehash: f9d0eb9cec597c44781539fa9231c5bf2b3cfe16
ms.sourcegitcommit: c7989a8ead235aaebb2503abbde598f2c26c0056
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2019
ms.locfileid: "33979467"
---
# <a name="configure-your-office-365-tenant-for-increased-security"></a>Configure o locatário do Office 365 para aumentar a segurança

Este tópico o orienta através da configuração recomendada para definições de todos os locatários que afetam a segurança do seu ambiente do Office 365. Suas necessidades de segurança podem exigir mais ou menos segurança. Use estas recomendações como ponto de partida.
  
## <a name="check-office-365-secure-score"></a>Verificar a pontuação segura do Office 365

A pontuação segura do Office 365 analisa a segurança da sua organização do Office 365 com base em suas atividades regulares e configurações de segurança e atribui uma pontuação. Comece anotando sua pontuação atual. O ajuste de algumas configurações de todos os locatários aumentará a sua pontuação. O objetivo não é atingir a pontuação máxima, mas para estar ciente das oportunidades de proteger seu ambiente que não afete negativamente a produtividade dos seus usuários. Confira a [Pontuação segura da Microsoft](microsoft-secure-score.md).
  
## <a name="tune-threat-management-policies-in-the-microsoft-365-security-center"></a>Ajustar as políticas de gerenciamento de ameaças no centro de segurança do Microsoft 365

O centro de segurança do Microsoft 365 inclui recursos que protegem o seu ambiente. Também inclui relatórios e painéis que você pode usar para monitorar e tomar medidas. Algumas áreas vêm com as configurações de política padrão. Algumas áreas não incluem políticas ou regras padrão. Visite estas políticas em gerenciamento de ameaças para ajustar as configurações de gerenciamento de ameaças para um ambiente mais seguro. 
  
|Área * * * *|Inclui uma política padrão * * * *|Recomendação * * * *|
|:-----|:-----|:-----|
|**Anti-phishing** <br/> |Sim  <br/> | Se você tiver um domínio personalizado, crie uma política anti-phishing para proteger as contas de email de seus usuários mais valiosos, como seu CEO, e para proteger seu domínio. Revisar [Configure uma política anti-phishing](set-up-anti-phishing-policies.md) e crie uma política usando o exemplo como guia: "exemplo: política anti-phishing para proteger um usuário e um domínio."|
|**Mecanismo Antimalware** <br/> |Sim  <br/> | Edite a política padrão:  <br/> &ensp;&ensp;• Filtro tipos de anexo comuns — selecione ativado  <br/><br>  Você também pode criar políticas de filtro de malware personalizadas e aplicá-las a usuários, grupos ou domínios especificados em sua organização.  <br/> <br> Mais informações:  <br/> &ensp;&ensp;• [Proteção Antimalware](https://technet.microsoft.com/en-us/library/jj200669%28v=exchg.150%29.aspx) <br/> &ensp;&ensp;• [Configurar políticas Antimalware](https://technet.microsoft.com/en-us/library/jj200745%28v=exchg.150%29.aspx) <br/> |
|**Anexos Seguros da ATP** <br/> |Não  <br/> | Na página principal de anexos seguros, proteja arquivos no SharePoint, no OneDrive e no Microsoft Teams marcando esta caixa:  <br/>  &ensp;&ensp;• Ative a ATP para SharePoint, OneDrive e Microsoft Teams  <br/> <br> Adicione uma nova política de anexo seguro com estas configurações:  <br/>  &ensp;&ensp;• Bloquear — bloquear emails e anexos atuais e futuros com malware detectado (escolha esta opção)  <br/>  &ensp;&ensp;• Habilitar o redirecionamento — (Marque esta caixa e insira um endereço de email, como uma conta de administrador ou de quarentena)  <br/>  &ensp;&ensp;• Aplique a seleção acima se o malware verificando se há anexos expirados ou se ocorrer um erro (Marque esta caixa)  <br/>  &ensp;&ensp;• Aplicado a – o domínio do destinatário é (selecione seu domínio)  <br/>  <br>Mais informações: [Configurar políticas de anexos seguros do Office 365 ATP](set-up-atp-safe-attachments-policies.md) <br/> |
|**Links seguros da ATP** <br/> |Sim  <br/> | Adicione essa configuração à política padrão para toda a organização:  <br/> &ensp;&ensp;• Use links seguros no: Office 365 ProPlus, Office para iOS e Android (Selecione essa opção).  <br/> <br>Política recomendada para destinatários específicos:  <br/>  &ensp;&ensp;• As URLs serão reescritas e verificadas em relação a uma lista de links mal-intencionados conhecidos quando o usuário clicar no link (Selecione essa opção).  <br/>  &ensp;&ensp;• Use anexos seguros para examinar Conteúdo baixável (Marque esta caixa).  <br/>  &ensp;&ensp;• Aplicado a – o domínio do destinatário é (selecione seu domínio).  <br/> <br> Mais informações: [Office 365 ATP Safe links](atp-safe-links.md).  <br/> |
|**Anti-spam (filtragem de email)** <br/> |Sim  <br/> | O que observar:  <br/>  &ensp;&ensp;• Muito spam — escolha as configurações personalizadas e edite a política padrão de filtro de spam.  <br/>  &ensp;&ensp;• Inteligência de falsificação — revise os remetentes que estão falsificando seu domínio. Bloquear ou permitir estes remetentes.  <br/>  <br>Mais informações: [proteção antispam de email do Office 365](anti-spam-protection.md).  <br/> |
|***Autenticação de email*** <br/> |Sim  <br/> |A autenticação de email usa um DNS (sistema de nomes de domínio) para adicionar informações verificáveis a mensagens de email sobre o remetente de um email. O Office 365 configura a autenticação de email para seu domínio padrão (onmicrosoft.com), mas os administradores do Office 365 também podem usar a autenticação de email para domínios personalizados. Três métodos de autenticação são usados: <br/> <br> &ensp;&ensp;• Estrutura de política de remetente (ou SPF).<br/>&ensp;&ensp;&ensp;&ensp;– Para configuração, consulte [set up SPF in Office 365 para ajudar a impedir a falsificação](set-up-spf-in-office-365-to-help-prevent-spoofing.md). <br/> &ensp;&ensp;• DomainKeys Identificated mail (DKIM). <br/> &ensp;&ensp;&ensp;&ensp;– Consulte [usar o DKIM para email em seu domínio personalizado no Office 365](https://docs.microsoft.com/office365/SecurityCompliance/use-dkim-to-validate-outbound-email). <br>&ensp;&ensp;&ensp;&ensp;Após configurar o DKIM, habilite-o na central de segurança.<br/> &ensp;&ensp;• Autenticação, geração de relatórios e conformidade de mensagens baseadas em domínio (DMARC). <br/> &ensp;&ensp;&ensp;&ensp;– Para a configuração do DMARC, [use o DMARC para validar emails no Office 365](use-dmarc-to-validate-email.md).<br/>  <br/>
|

> [!NOTE]
> Para implantações não padrão de SPF, implantações híbridas e solução de problemas: [como o Office 365 usa o Sender Policy Framework (SPF) para evitar a falsificação](how-office-365-uses-spf-to-prevent-spoofing.md).

## <a name="view-dashboards-and-reports-in-the-security-and-compliance-centers"></a>Exibir painéis e relatórios nos centros de segurança e conformidade

Visite esses relatórios e painéis para saber mais sobre a integridade de seu ambiente. Os dados desses relatórios ficarão mais sofisticados, pois sua organização usa os serviços do Office 365. Por enquanto, familiarize-se com o que você pode monitorar e tomar ações. Para obter mais informações, consulte: [relatórios nos centros de segurança e conformidade do Microsoft 365](reports-in-security-and-compliance.md).
  
|Painel * * * *|****Descrição****|
|:-----|:-----|
|Painel de gerenciamento de ameaças  <br/> |Na seção Gerenciamento de ameaças da central de segurança, use este painel para ver as ameaças que já foram tratadas e como uma ferramenta útil para relatar os tomadores de decisões de negócios sobre o que os recursos de investigação e resposta de ameaças já fizeram para proteger sua empresa.  <br/> |
|Explorador de ameaças  <br/> |Isso também está na seção Gerenciamento de ameaças da central de segurança. Se você estiver investigando ou experimentando um ataque contra o locatário do Office 365, use o Gerenciador de ameaças para analisar ameaças. O Gerenciador de ameaças mostra o volume de ataques ao longo do tempo, e você pode analisar esses dados por famílias de ameaças, infraestrutura de atacante e muito mais. Você também pode marcar qualquer email suspeito para a lista de incidentes.  <br/> |
|Relatórios — painel  <br/> |Na seção relatórios da central de segurança, exiba relatórios de auditoria para as organizações do SharePoint Online e do Exchange Online. Você também pode acessar os relatórios de entrada do usuário do Azure Active Directory (Azure AD), relatórios de atividades do usuário e o log de auditoria do Azure AD na página exibir relatórios.  <br/> |
   
![Painel central de segurança](media/870ab776-36d2-49c7-b615-93b2bc42fce5.png)
  
## <a name="configure-additional-exchange-online-tenant-wide-settings"></a>Definir configurações adicionais para todos os locatários do Exchange Online

Muitos dos controles de segurança e proteção no centro de administração do Exchange também estão incluídos na central de segurança. Não é necessário configurá-los nos dois lugares. Aqui estão algumas configurações adicionais recomendadas. 
  
|Área * * * *|Inclui uma política padrão * * * *|Recomendação * * * *|
|:-----|:-----|:-----|
|**Fluxo de mensagens** (regras de fluxo de email, também conhecidas como regras de transporte)|Não|Adicione uma regra de fluxo de emails para ajudar a proteger contra o ransomware. Consulte "como usar as regras de transporte do Exchange para rastrear ou bloquear emails com extensões de arquivo usadas pelo ransomware" neste artigo de blog: [como lidar com o ransomware](https://blogs.technet.microsoft.com/office365security/how-to-deal-with-ransomware/). <br><br/> Confira estes tópicos: <br/>•[Proteger contra o ransomware](https://docs.microsoft.com/office365/admin/security-and-compliance/secure-your-business-data?view=o365-worldwide#ransomware)<br/>•[Proteção contra malware e ransomware no Office 365](office-365-malware-and-ransomware-protection.md)<br/><br/>  Crie uma regra de fluxo de emails para impedir o encaminhamento automático de emails para domínios externos. Para obter mais informações, consulte [mitigating Client external Forwarding Rules with Secure Score](https://blogs.technet.microsoft.com/office365security/mitigating-client-external-forwarding-rules-with-secure-score/). <br/><br/> Mais informações: [regras de fluxo de emails (regras de transporte) no Exchange Online](https://technet.microsoft.com/en-us/library/jj919238%28v=exchg.150%29.aspx)|
|**Habilitar a autenticação moderna**|Não|A autenticação moderna no Office 365 é um pré-requisito para usar a protocolo de autenticação multifator (MFA). A MFA é recomendada para proteger o acesso a recursos de nuvem, incluindo email. <br/><br/> Confira estes tópicos:  <br/>• [Habilitar ou desabilitar a autenticação moderna no Exchange Online](https://support.office.com/article/58018196-f918-49cd-8238-56f57f38d662) <br/>• [Skype for Business Online: habilitar seu locatário para autenticação moderna](https://social.technet.microsoft.com/wiki/contents/articles/34339.skype-for-business-online-enable-your-tenant-for-modern-authentication.aspx) <br/><br/> A autenticação moderna está habilitada por padrão para clientes do Office 2016, SharePoint Online e OneDrive for Business. <br/><br/> Mais informações: [usando a autenticação moderna do office 365 com clientes do Office](https://support.office.com/article/776c0036-66fd-41cb-8928-5495c0f9168a)|
   
## <a name="configure-tenant-wide-sharing-policies-in-sharepoint-admin-center"></a>Configurar políticas de compartilhamento em todo o locatário no centro de administração do SharePoint

Recomendações da Microsoft para configuração de sites de equipe do SharePoint em níveis de proteção crescentes, começando com proteção de linha de base. Para obter mais informações, consulte [proteger sites e arquivos do SharePoint Online](https://docs.microsoft.com/microsoft-365-enterprise/secure-sharepoint-online-sites-and-files)
  
Sites de equipe do SharePoint configurados no nível da linha de base permitem compartilhar arquivos com usuários externos usando links de acesso anônimo. Essa abordagem é recomendada em vez de enviar arquivos no email. 
  
Para dar suporte às metas de proteção de linha de base, configure as políticas de compartilhamento em todo o locatário conforme recomendado aqui. As configurações de compartilhamento para sites individuais podem ser mais restritivas que essa política de todo o locatário, mas não mais permissivas. 
  
|Área * * * *|Inclui uma política padrão * * * *|Recomendação * * * *|
|:-----|:-----|:-----|
|**Compartilhamento** (SharePoint Online e OneDrive for Business)|Sim|O compartilhamento externo está habilitado por padrão. Estas configurações são recomendadas: <br/>• Permitir o compartilhamento de usuários externos autenticados e o uso de links de acesso anônimo (configuração padrão). <br/>  • Os links de acesso anônimo expiram em vários dias. Insira um número, se desejado, como 30 dias. <br/>• Tipo de link padrão — selecione interno (somente pessoas na organização). Os usuários que desejam compartilhar usando links anônimos devem escolher essa opção no menu compartilhamento. <br/><br/> Mais informações: [visão geral do compartilhamento externo](https://support.office.com/article/c8a462eb-0723-4b0b-8d0a-70feafe4be85)|
   
O centro de administração do SharePoint e o centro de administração do OneDrive for Business incluem as mesmas configurações. As configurações no centro de administração se aplicam a ambos.
  
## <a name="configure-settings-in-azure-active-directory"></a>Definir configurações no Azure Active Directory

Certifique-se de visitar essas duas áreas no Azure Active Directory para concluir a configuração em todo o locatário para ambientes mais seguros.
  
### <a name="configure-named-locations-under-conditional-access"></a>Configurar locais nomeados (sob acesso condicional)

Se sua organização incluir escritórios com acesso seguro à rede, adicione os intervalos de endereços IP confiáveis ao Azure Active Directory como locais nomeados. Este recurso ajuda a reduzir o número de falsos positivos informados para eventos de risco de entrada. 
  
Confira: [locais nomeados no Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-named-locations)
  
### <a name="block-apps-that-dont-support-modern-authentication"></a>Bloquear aplicativos que não dão suporte à autenticação moderna

A autenticação multifator requer aplicativos que dão suporte à autenticação moderna. Os aplicativos que não dão suporte à autenticação moderna não podem ser bloqueados usando regras de acesso condicional.
  
Para ambientes seguros, não deixe de desabilitar a autenticação para aplicativos que não dão suporte à autenticação moderna. Você pode fazer isso no Azure Active Directory com um controle em breve.
  
Enquanto isso, use um dos seguintes métodos para fazer isso para o SharePoint Online e o OneDrive for Business:
  
- Usar o PowerShell, consulte [bloquear aplicativos que não usam autenticação moderna](https://docs.microsoft.com/intune-classic/deploy-use/block-apps-with-no-modern-authentication).
    
- Configure isso no centro de administração do SharePoint na página "acesso ao dispositivo" — "controlar o acesso de aplicativos que não usam autenticação moderna". Escolha bloquear. 
    
## <a name="get-started-with-cloud-app-security-or-office-365-cloud-app-security"></a>Introdução ao Cloud app Security ou ao Office 365 Cloud app Security

Use o Office 365 Cloud app Security para avaliar o risco, para alertar sobre atividades suspeitas e para executar ações automaticamente. Requer plano do Office 365 e5.
  
Ou use o Microsoft Cloud app Security para obter visibilidade mais profunda, mesmo depois que o acesso é concedido, controles abrangentes e proteção aprimorada para todos os aplicativos de nuvem, incluindo o Office 365. 
  
Como esta solução recomenda o plano do EMS e5, recomendamos que você inicie o Cloud app Security para que possa usá-lo com outros aplicativos SaaS em seu ambiente. Comece com políticas e configurações padrão.
  
Mais informações:
  
- [Implantar o Cloud App Security](https://docs.microsoft.com/cloud-app-security/getting-started-with-cloud-app-security)
    
- [Mais informações sobre o Microsoft Cloud App Security](https://www.microsoft.com/cloud-platform/cloud-app-security)
    
- [O que é o Cloud app Security?](https://docs.microsoft.com/cloud-app-security/what-is-cloud-app-security)
    
![Painel do Cloud App Security](media/1fb2aa65-54b8-4746-9f5e-c187d339e9f5.png)
  
## <a name="additional-resources"></a>Recursos adicionais

Estes artigos e guias fornecem informações prescritivas adicionais para proteger seu ambiente do Office 365:
  
- [Diretrizes de segurança da Microsoft para campanhas políticas, sem fins lucrativos e outras organizações Agile](https://docs.microsoft.com/microsoft-365-enterprise/microsoft-security-guidance) (você pode usar essas recomendações em qualquer ambiente, especialmente em ambientes de nuvem) 
    
- [Políticas de segurança e configurações recomendadas para identidades e dispositivos](https://docs.microsoft.com/microsoft-365-enterprise/microsoft-365-policies-configurations) (estas recomendações incluem ajuda para ambientes do AD FS) 
    


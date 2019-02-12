---
title: Links seguros de ATP do Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.date: 02/11/2019
ms.topic: overview
f1_keywords:
- "197503"
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
- ZVO160
- ZXL160
- ZPP160
- ZWD160
ms.assetid: dd6a1fef-ec4a-4cf4-a25a-bb591c5811e3
description: O recurso de Links seguros fornece verificação de tempo do clique de hiperlinks em documentos do Office e em mensagens de email. Use os links seguros para proteger sua organização contra ataques de phishing e outros.
ms.openlocfilehash: 4d83aa65af47ea6723d6e2042c230fb2b07c174c
ms.sourcegitcommit: 065f5e72676511b5ecf7f10a17685999780e92d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29888027"
---
# <a name="office-365-atp-safe-links"></a>Links seguros de ATP do Office 365

## <a name="overview-of-office-365-atp-safe-links"></a>Visão geral do Office 365 ATP Safe Links

> [!IMPORTANT]
> Este artigo destina-se a clientes corporativos. Se você for um usuário doméstico procurando informações sobre Links seguros no Outlook, consulte [Outlook.com avançadas de segurança](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2).

Links do Office 365 ATP seguros (parte de [Proteção de ameaça avançadas](office-365-atp.md)) pode ajudar a proteger a sua organização, fornecendo a verificação de tempo do clique de endereços da web (URLs) em [mensagens de email](#how-atp-safe-links-works-with-email) e [documentos do Office](#how-atp-safe-links-works-with-office-documents). Proteção é definida por meio de [Links de seguros ATP políticas](set-up-atp-safe-links-policies.md) definidas pela sua equipe de segurança do Office 365. 
  
Depois que suas políticas de Links de seguros ATP estão funcionando, os administradores globais do Office 365, os administradores de segurança e leitores de segurança podem [Exibir relatórios de proteção avançada de ameaça](view-reports-for-atp.md). As informações contidas nesses relatórios podem ajudar sua equipe de segurança a executar etapas adicionais para proteger sua organização ou pesquisar incidentes de segurança.

Como [novos recursos são adicionados ao ATP](office-365-atp.md#new-features-are-continually-being-added-to-atp), sua equipe de segurança do Office 365 pode adicionar ou editar políticas de Links de seguros ATP da sua organização. Além disso, você poderá perceber alterações e melhorias, como nosso recentemente revisado [páginas de aviso](atp-safe-links-warning-pages.md) e o link nativo renderização no Outlook.
         
## <a name="how-atp-safe-links-works-with-urls-in-email"></a>Como os Links de seguros ATP funciona com URLs em email

Em um alto nível, aqui está como a proteção de Links de seguros ATP funciona para URLs no email (hospedado no Office 365, não no local):
  
1. Pessoas recebem mensagens de email, algumas das quais contêm URLs.
    
2. Todos os emails passa pelo Exchange Online Protection, onde o protocolo de internet (IP) e o envelope filtros, com base em assinatura malware protection, antispam e antimalware filtros são aplicados. 
    
3. O email chega nas caixas de entrada de pessoas.
    
4. Um usuário entra no Office 365 e vai para a sua caixa de entrada de email.
    
5. O usuário abre uma mensagem de email e clica em uma URL na mensagem de email.
    
6. O recurso de Links de seguros ATP verifica se a URL imediatamente antes de abrir o site. A URL é identificada como bloqueado, mal-intencionado ou seguros.
    
    - Se a URL para um site que está incluído em uma [lista personalizada de URLs "Não regravação"](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) para uma diretiva que se aplica ao usuário, o site será aberto. 
    
    - Se a URL for para um site que está incluído na [lista de URLs bloqueada personalizada](set-up-a-custom-blocked-urls-list-wtih-atp.md)da organização, uma [página de aviso](atp-safe-links-warning-pages.md) é exibida. 
    
    - Se a URL for para um site que determinou mal-intencionados, uma [página de aviso](atp-safe-links-warning-pages.md) é exibida. 
    
    - Se a URL vai para um arquivo baixável e da sua organização [políticas de Links de seguros ATP](set-up-atp-safe-links-policies.md) estejam configurados para examinar esse tipo de conteúdo, o arquivo baixável é verificado. 
    
    - Se a URL for determinada seguros, o site é aberto.
    
## <a name="how-atp-safe-links-works-with-urls-in-office-documents"></a>Como os Links de seguros ATP funciona com URLs em documentos do Office

Em um alto nível, aqui está como proteção de Links de seguros ATP funciona para URLs em aplicativos do Office 365 ProPlus (versões atuais do Word, Excel e PowerPoint no Windows ou Mac, Office apps em iOS ou dispositivos Android, o Visio no Office Online, OneNote Online e o Windows):
  
1. Pessoas instalou Office 365 ProPlus em seu computador, smartphone ou tablet. (Ou que estão usando o Office Online em seu navegador.)
    
2. Um usuário abre uma Word, Excel, PowerPoint ou Visio e entra no Office 365 Enterprise usando a conta do trabalho ou da escola. O documento contém URLs.
    
3. Quando o usuário clica em uma URL no documento, o link é verificado pelo serviço ATP Links de seguros.
    
  - Se a URL for para um site que está incluído em uma [lista personalizada de URLs "Não regravação"](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) para uma diretiva que se aplica ao usuário, que o usuário é colocado no site. 
    
  - Se a URL for para um site que está incluído na [lista de URLs bloqueada personalizada](set-up-a-custom-blocked-urls-list-wtih-atp.md)da organização, o usuário é colocado em uma [página de aviso](atp-safe-links-warning-pages.md).
    
  - Se a URL for para um site que determinou mal-intencionados, o usuário é colocado em uma [página de aviso](atp-safe-links-warning-pages.md).
    
  - Se a URL vai para um arquivo baixável e as [políticas de Links de seguros ATP](set-up-atp-safe-links-policies.md) estejam configurados para examinar tais downloads, o arquivo baixável é verificado. 
    
  - Se a URL é considerada segura, o usuário é colocado no site.

## <a name="how-to-get-atp-safe-links-protection"></a>Como obter proteção ATP Links de seguros

Primeiro, verifique se que sua assinatura incluir [Proteção avançada de ameaça](office-365-atp.md). ATP está incluído nas assinaturas, como [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 Enterprise E5, A5 de educação do Office 365, etc. Se sua organização tiver uma assinatura do Office 365 que não inclui ATP do Office 365, você pode adquirir potencialmente ATP como um complemento. Para obter mais informações, consulte [preços e planos de proteção de ameaça avançadas do Office 365](https://products.office.com/exchange/advance-threat-protection) e o [Office 365 avançadas Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description). 
  
Em seguida, certifique-se de que suas políticas de Links de seguros ATP são definidas. (Consulte [Configurar políticas de vínculos do Office 365 ATP seguros](set-up-atp-safe-links-policies.md).) Recursos de Links de seguros ATP estão ativos quando:
  
- **Políticas de Links de seguros ATP estiver configuradas** para email e documentos do Word, Excel, PowerPoint e Visio. (Consulte [Configurar políticas de links seguros ATP no Office 365](set-up-atp-safe-links-policies.md)).

- **Aplicativos de cliente do Office 365 estão configurados para usar autenticação moderno** (isto é para proteção de Links de seguros ATP em documentos do Office). (Consulte [autenticação moderna para 2016 do Office](https://docs.microsoft.com/office365/enterprise/modern-auth-for-office-2013-and-2016)). 
    
- **Os usuários entrou no Office 365** usando a conta do trabalho ou da escola. (Consulte [entrar no Office ou Office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426)).
    
- **Passa de email da sua organização no Exchange Online Protection**.  

Para definir (ou editar) políticas ATP, você deve ter uma das funções descritas na tabela a seguir:

|Função  |Onde/como atribuído  |
|---------|---------|
|Administrador Global do Office 365 |A pessoa que se inscreve para comprar o Office 365 é um administrador global por padrão. (Consulte [funções de administrador do Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) para saber mais).         |
|Administrador de segurança |Centro de administração do Azure Active Directory ([https://aad.portal.azure.com](https://aad.portal.azure.com))|
|Gerenciamento de organização Online do Exchange |Centro de administração do Exchange ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) <br>ou <br>  Cmdlets do PowerShell (consulte [PowerShell do Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)) |
    
## <a name="how-to-make-sure-atp-safe-links-protection-is-in-place"></a>Como tornar-se de proteção de Links de seguros ATP esteja in-loco

Como administrador global ou administrador de segurança, certifique-se de examinar suas [políticas de Links de ATP seguros](set-up-atp-safe-links-policies.md). Políticas de Links de seguros ATP determinam se proteção se aplica a hiperlinks em mensagens de email só ou a URLs em documentos do Office, bem.

Depois que as políticas de Links de seguros ATP estão no lugar, a equipe de segurança da sua organização pode ver consulte como a proteção de Links de seguros ATP está trabalhando para sua organização é por [Visualizando relatórios de proteção avançada de ameaça](view-reports-for-atp.md). 

## <a name="example-scenarios"></a>Exemplos de cenários
  
A tabela a seguir descreve alguns cenários de exemplo onde proteção de Links de seguros ATP pode ou não ser in-loco. (Em todos os casos, assumimos que a organização tiver E5 do Office 365 Enterprise.)
  
|**Cenário de exemplo**|**Proteção de Links de seguros ATP se aplicam neste caso?**|
|:-----|:-----|
|Jean é um membro de um grupo que tem políticas de Links de seguros ATP cobrindo as URLs em documentos do Office e de email. Jean abre uma apresentação do PowerPoint que alguém enviadas e, em seguida, clicar em uma URL da apresentação.  <br/> |Sim. As políticas de Links de seguros ATP definidas se aplicam ao de Jean grupo, de Jean email e os documentos do Word, Excel, PowerPoint ou Visio que Jean for aberto, contanto que Jean tiver entrada no e usando o Office 365 ProPlus em Windows, iOS ou dispositivos com Android.  <br/> |
|Na organização, não global ou de segurança de Chris administradores definiu quaisquer políticas de links seguros ATP ainda. Chris receberá um email que contém uma URL para um site mal-intencionado. Chris está a par a URL é mal-intencionado e clicar no link.  <br/> |Não. A política padrão que cobre URLs para todas as pessoas na organização deve ser definida em ordem para proteção estar em vigor.  <br/> |
|Na organização, não global ou de segurança da Pat administradores tem definido ou editados quaisquer políticas de Links de seguros ATP ainda. PAT abre um documento do Word e clicar em uma URL no arquivo.  <br/> |Política de No. A que inclui a documentos do Office deve ser definida em ordem para proteção estar em vigor. Consulte [Configurar políticas de Links de ATP seguros no Office 365](set-up-atp-safe-links-policies.md).<br/> |
|Organização de Lee possui uma política de Links de seguros ATP que tenha `http://tailspintoys.com` listado como um site bloqueado. Lee recebe uma mensagem de email que contém uma URL para `http://tailspintoys.com/aboutus/trythispage`. Lee clica a URL.<br/> |Isso depende se o site inteiro e todas as suas subpáginas estão incluídas na lista de bloqueados URLs. Consulte [Configurar uma lista de URLs bloqueada personalizada usando Links de ATP seguros](set-up-a-custom-blocked-urls-list-wtih-atp.md).<br/> |
|Jaime, colega de Jean, envia um email para Jean, não sabendo que o email contém uma URL mal-intencionada.  <br/> |Isso depende se as diretivas de Links de seguros ATP são definidas para emails enviados dentro da organização. Consulte [Configurar políticas de Links de ATP seguros no Office 365](set-up-atp-safe-links-policies.md).<br/> |


  


---
title: Links seguros de ATP do Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
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
ms.openlocfilehash: 9199c69d73a1585d76181c7a5feba79e465289db
ms.sourcegitcommit: e14dec9bed0c0009acbc1f1cb80b4d0794ad5739
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/05/2018
ms.locfileid: "25435108"
---
# <a name="office-365-atp-safe-links"></a>Links seguros de ATP do Office 365

O Office 365 ATP seguros Links (ATP seguros vínculos) (juntamente com o [Office 365 ATP seguros anexos](atp-safe-attachments.md)) é um conjunto de recursos de segurança oferecidos como parte de [Proteção de ameaça avançadas do Office 365](office-365-atp.md) para empresas. Links de seguros ATP pode ajudar a proteger a sua organização, fornecendo a verificação de tempo do clique de endereços da web (URLs) em [mensagens de email](#how-atp-safe-links-works-with-email) e [documentos do Office](#how-atp-safe-links-works-with-office-documents). Proteção é definida por meio de [Links de seguros ATP políticas](set-up-atp-safe-links-policies.md) definidas pela sua equipe de segurança do Office 365. 
  
Depois que suas políticas de Links de seguros ATP estão funcionando, os administradores globais do Office 365, os administradores de segurança e leitores de segurança podem [Exibir relatórios de proteção avançada de ameaça](view-reports-for-atp.md). As informações contidas nesses relatórios podem ajudar sua equipe de segurança a executar etapas adicionais para proteger sua organização ou pesquisar incidentes de segurança.
         
## <a name="how-atp-safe-links-works-with-email"></a>Como os Links de seguros ATP funciona com o email

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
    
## <a name="how-atp-safe-links-works-with-office-documents"></a>Como os Links de seguros ATP funciona com documentos do Office

Em um alto nível, aqui está como proteção de Links de seguros ATP funciona para URLs em aplicativos do Office 365 ProPlus (versões atuais do Word, Excel e PowerPoint no Windows ou Mac, Office apps em iOS ou dispositivos Android, o Visio no Office Online, OneNote Online e o Windows):
  
1. Pessoas instalou Office 365 ProPlus em seu computador, smartphone ou tablet. (Ou que estão usando o Office Online em seu navegador.)
    
2. Um usuário abre uma Word, Excel, PowerPoint ou Visio e entra no Office 365 Enterprise usando a conta do trabalho ou da escola. O documento contém URLs.
    
3. Quando o usuário clica em uma URL no documento, o link é verificado pelo serviço ATP Links de seguros.
    
  - Se a URL for para um site que está incluído em uma [lista personalizada de URLs "Não regravação"](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) para uma diretiva que se aplica ao usuário, que o usuário é colocado no site. 
    
  - Se a URL for para um site que está incluído na [lista de URLs bloqueada personalizada](set-up-a-custom-blocked-urls-list-wtih-atp.md)da organização, o usuário é colocado em uma [página de aviso](atp-safe-links-warning-pages.md).
    
  - Se a URL for para um site que determinou mal-intencionados, o usuário é colocado em uma [página de aviso](atp-safe-links-warning-pages.md).
    
  - Se a URL vai para um arquivo baixável e as [políticas de Links de seguros ATP](set-up-atp-safe-links-policies.md) estejam configurados para examinar tais downloads, o arquivo baixável é verificado. 
    
  - Se a URL é considerada segura, o usuário é colocado no site.

## <a name="new-features-added-to-atp-safe-links"></a>Novos recursos adicionados ao ATP Links de seguros

Podemos está prosseguindo adicionar novos recursos para Links de ATP seguros. Aqui estão alguns exemplos:
  
- Proteção de Links de seguros ATP a partir do final de 2017 de outubro, é estendida para aplicar a URLs em email, bem como as URLs em documentos do Office 365 ProPlus, como Word, Excel, PowerPoint e Visio no Windows, bem como Office apps em dispositivos com Android e iOS. (Certifique-se de que você estiver usando [Autenticação moderna do Office](https://docs.microsoft.com/office365/enterprise/modern-auth-for-office-2013-and-2016).)
    
- Iniciando no de 2018 de março, proteção de Links de seguros ATP é estendida para aplicar a emails enviados entre pessoas dentro de uma organização. (Certifique-se para [rever e editar suas políticas de Links de seguros ATP](set-up-atp-safe-links-policies.md).)

- Iniciando no de 2018 junho, quando pessoas estiverem usando o Outlook Web Application (OWA), Links de seguros ATP renderiza URLs originais e não mostrar URLs reconfigurados. Isso permite que os usuários exibam original links no email. (Chamamos visbility este link nativo.)

- Início em setembro de 2018, o recurso de [páginas de aviso do Office 365 ATP](atp-safe-links-warning-pages.md) um novo esquema de cores, mais detalhes e a capacidade para continuar a um site apesar recebe avisos e recomendações. 
  
- Proteção de Links de seguros ATP começando na segunda metade do 2018, é estendida para aplicar a URLs no Office Online (on-line do Word, Excel Online, on-line do PowerPoint e OneNote Online) e Office 365 ProPlus em Mac. (Certifique-se para [rever e editar suas políticas de Links de seguros ATP](set-up-atp-safe-links-policies.md).)
   
- Iniciando no tardia 2018, visibilidade de link nativo é disponível no Outlook. Os usuários são capazes de exibir URLs originais (não reconfigurados URLs) no email, quer estejam usando OWA ou Outlook.
    
## <a name="how-to-get-atp-safe-links-protection"></a>Como obter proteção ATP Links de seguros

Recursos de Links de seguros ATP fazem parte da [Proteção de ameaça avançadas](office-365-atp.md), incluído no Office 365 Enterprise E5. Se sua organização estiver usando outra assinatura do Office 365 Enterprise, a proteção avançada de ameaça pode ser adquirida como um complemento. Para obter mais informações, consulte [Descrição do serviço de plataforma do Office 365: segurança do Office 365 &amp; Centro de conformidade](https://technet.microsoft.com/en-us/library/dn933793.aspx) e [comprar ou editar um complemento para o Office 365 para empresas](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).
  
Os recursos de Links de seguros ATP estão ativos quando:
  
- **Políticas de Links de seguros ATP estiver configuradas** para email e documentos do Word, Excel, PowerPoint e Visio. (Consulte [Configurar políticas de links seguros ATP no Office 365](set-up-atp-safe-links-policies.md)).

- **Aplicativos de cliente do office 365 estão configurados para usar autenticação moderno**. (Consulte [autenticação moderna para 2016 do Office](https://docs.microsoft.com/office365/enterprise/modern-auth-for-office-2013-and-2016)). 
    
- **Os usuários entrou no Office 365** usando a conta do trabalho ou da escola. (Consulte [entrar no Office ou Office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426)).
    
- **Que email da sua organização está hospedada no Office 365**, não em um servidor local. 
    
## <a name="make-sure-atp-safe-links-protection-is-in-place"></a>Certifique-se de proteção de Links de seguros ATP esteja in-loco

Uma boa maneira de ver como a proteção de Links de seguros ATP está trabalhando para sua organização está exibindo [relatórios de proteção avançada de ameaça](view-reports-for-atp.md). Além disso, como um administrador global ou de segurança, certifique-se de examinar suas [políticas de Links de ATP seguros](set-up-atp-safe-links-policies.md). Políticas de Links de seguros ATP determinam se proteção se aplica a hiperlinks em mensagens de email só ou a URLs em documentos do Office, bem.

## <a name="example-scenarios-where-atp-safe-links-protection-might-or-might-not-be-in-place"></a>Cenários de exemplo onde proteção de Links de seguros ATP pode ou não ser in-loco
  
A tabela a seguir descreve alguns cenários de exemplo onde proteção de Links de seguros ATP pode ou não ser in-loco. (Em todos os casos, assumimos que a organização tiver E5 do Office 365 Enterprise.)
  
|**Cenário de exemplo**|**Proteção de Links de seguros ATP se aplicam neste caso?**|
|:-----|:-----|
|Jean é um membro de um grupo que tem políticas de Links de seguros ATP cobrindo as URLs em documentos do Office e de email. Jean abre uma apresentação que alguém enviada em 2016 do PowerPoint e, em seguida, clicar em uma URL da apresentação.  <br/> |Sim. As políticas de Links de seguros ATP definidas se aplicam ao de Jean grupo, de Jean email e os documentos do Word, Excel, PowerPoint ou Visio que Jean for aberto, contanto que Jean tiver entrada no e usando o Office 365 ProPlus em Windows, iOS ou dispositivos com Android.  <br/> |
|Na organização, não global ou de segurança de Chris administradores definiu quaisquer políticas de links seguros ATP ainda. Chris receberá um email que contém uma URL para um site mal-intencionado. Chris está a par a URL é mal-intencionado e clicar no link.  <br/> |Não. A política padrão que cobre URLs para todas as pessoas na organização deve ser definida em ordem para proteção estar em vigor.  <br/> |
|Na organização, não global ou de segurança da Pat administradores tem definido ou editados quaisquer políticas de Links de seguros ATP ainda. PAT abre um documento do Word e clicar em uma URL no arquivo.  <br/> |Política de No. A que inclui a documentos do Office deve ser definida em ordem para proteção estar em vigor. Consulte [Configurar políticas de Links de ATP seguros no Office 365](set-up-atp-safe-links-policies.md).<br/> |
|Organização de Lee possui uma política de Links de seguros ATP que tenha `http://tailspintoys.com` listado como um site bloqueado. Lee recebe uma mensagem de email que contém uma URL para `http://tailspintoys.com/aboutus/trythispage`. Lee clica a URL.<br/> |Isso depende se o site inteiro e todas as suas subpáginas estão incluídas na lista de bloqueados URLs. Consulte [Configurar uma lista de URLs bloqueada personalizada usando Links de ATP seguros](set-up-a-custom-blocked-urls-list-wtih-atp.md).<br/> |
|Jaime, colega de Jean, envia um email para Jean, não sabendo que o email contém uma URL mal-intencionada.  <br/> |Isso depende se as diretivas de Links de seguros ATP são definidas para emails enviados dentro da organização. Consulte [Configurar políticas de Links de ATP seguros no Office 365](set-up-atp-safe-links-policies.md).<br/> |
   
## <a name="related-topics"></a>Tópicos relacionados

[Proteção Avançada contra Ameaças do Office 365](office-365-atp.md) 
  
[Configurar políticas de Links de ATP seguros no Office 365](set-up-atp-safe-links-policies.md)
  
[Anexos de ATP seguros no Office 365](atp-safe-attachments.md)
  
[Recursos antiphishing ATP no Office 365](atp-anti-phishing.md)
  
[Exibir relatórios de Proteção avançada contra ameaças](view-reports-for-atp.md)
  


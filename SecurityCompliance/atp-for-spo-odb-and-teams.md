---
title: Office 365 ATP para SharePoint, OneDrive e Microsoft Teams
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 26261670-db33-4c53-b125-af0662c34607
description: Estenda a proteção de ameaça avançadas do Office 365 para arquivos no SharePoint Online, o OneDrive for Business e Teams da Microsoft habilitar a colaboração mais segura para sua organização.
ms.openlocfilehash: ff07d88a150d3f059681556feec9a5e89b5875a8
ms.sourcegitcommit: 099bbfb1d16b251fd5cf18ec6515faaf9a989176
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25454318"
---
# <a name="office-365-atp-for-sharepoint-onedrive-and-microsoft-teams"></a>Office 365 ATP para SharePoint, OneDrive e Microsoft Teams

## <a name="overview-of-office-365-atp-for-sharepoint-onedrive-and-microsoft-teams"></a>Visão geral do Office 365 ATP para SharePoint, OneDrive e equipes da Microsoft

Compartilhar arquivos de pessoas regularmente e colaborar através do SharePoint, OneDrive e Teams da Microsoft. Com [A proteção de ameaça avançadas do Office 365](office-365-atp.md) (ATP), sua organização pode colaborar de maneira mais segura. ATP ajuda a detectar e bloquear arquivos que são identificados como sendo maliciosas em bibliotecas de documentos e sites de equipe.  
  
### <a name="how-it-works"></a>Como funciona

Quando um arquivo no SharePoint Online, o OneDrive for Business e Teams da Microsoft foi identificado como sendo maliciosas, ATP integra-se diretamente com os repositórios de arquivos de bloqueio de arquivo. A imagem a seguir mostra um exemplo de um arquivo mal-intencionado detectado em uma biblioteca.
  
[![Captura de tela de arquivos no OneDrive for Business com um detectada como mal-intencionado](media/2bba71cc-7ad1-4799-8b9d-d56f923db3a7.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)
  
Embora os arquivos bloqueados ainda está listado na biblioteca de documentos e web, aplicativos móveis ou de mesa, os arquivos bloqueados não podem ser aberto, copiado, movido ou shared. Pessoas podem, no entanto, excluir um arquivo bloqueado. Aqui está um exemplo de quais que se parece com no dispositivo móvel de um usuário:
  
[![Captura de tela da exclusão de um arquivo bloqueado do OneDrive for Business do app móvel OneDrive](media/cb1c1705-fd0a-45b8-9a26-c22503011d54.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)
  
Dependendo de como o Office 365 é configurada, as pessoas podem ou podem não ter a capacidade de fazer o download de um arquivo bloqueado. Aqui está o download de arquivos bloqueados aparência no dispositivo móvel de um usuário:
  
[![Captura de tela de download de arquivos bloqueados no OneDrive for Business](media/be288a82-bdd8-4371-93d8-1783db3b61bc.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)
  
Para saber mais, consulte [Ativar ATP do Office 365 para SharePoint, OneDrive e as equipes da Microsoft](turn-on-atp-for-spo-odb-and-teams.md).
  
### <a name="keep-the-following-points-in-mind"></a>Tenha em mente os seguintes pontos

- ATP não examinará cada arquivo no SharePoint Online, OneDrive para negócios ou Teams da Microsoft. Isso ocorre por design. Os arquivos são examinados assincronamente, por meio de um processo que usa os eventos de atividade de compartilhamento e de convidado, juntamente com os sinais de ameaça e heurístico inteligente para identificar arquivos mal-intencionados.

- Certifique-se de que seus sites do SharePoint são configurados para usar a [experiência moderna](https://docs.microsoft.com/sharepoint/guide-to-sharepoint-modern-experience). Quando um arquivo é identificado como mal-intencionado e bloqueadas, pessoas podem ver o que isso tenha ocorrido na experiência moderna, mas não o modo de exibição clássico. Proteção de ATP é aplicável quer o a experiência moderna ou o modo de exibição clássico é usado; No entanto, os indicadores visuais que um arquivo é bloqueado estão presentes apenas na experiência moderna.
    
- Arquivos que são identificados como mal-intencionado no SharePoint Online, OneDrive for Business ou Microsoft Teams serão exibidas nos [relatórios de proteção de ameaça avançadas do Office 365](view-reports-for-atp.md) e no Explorer de ameaça (parte do [Office 365 Threat Intelligence](office-365-ti.md)).
    
- ATP é parte da estratégia geral de ameaça proteção sua organização, que inclui recursos anti-spam e proteção contra malware, bem como Links seguros e anexos seguros. Para saber mais, consulte [proteger contra ameaças no Office 365](protect-against-threats.md).
    
- Um administrador do SharePoint Online pode determinar se deseja habilitar pessoas baixar arquivos que são detectados como sendo maliciosas. Isso é feito executando o cmdlet Set-SPOTenant PowerShell usando um parâmetro de DisallowInfectedFileDownload (consulte [ativem ATP do Office 365 para SharePoint, OneDrive e as equipes da Microsoft](turn-on-atp-for-spo-odb-and-teams.md)).
    
## <a name="quarantine-in-atp-for-sharepoint-online-onedrive-for-business-and-microsoft-teams"></a>Quarentena no ATP para SharePoint Online, o OneDrive for Business e equipes da Microsoft

 Iniciando no tardia de 2018 de maio, recursos de [quarentena](quarantine-email-messages.md) na segurança &amp; Centro de conformidade estão sendo estendidas para ATP para SharePoint Online, OneDrive for Business e Teams da Microsoft.
  
Quando um arquivo no SharePoint Online, o OneDrive for Business ou Teams da Microsoft é identificado como mal-intencionado, além de ATP bloqueando o arquivo de ser aberto ou compartilhado, esse arquivo está incluído em uma lista de itens em quarentena. (Na segurança &amp; Centro de conformidade, vá para **gerenciamento de ameaça** \> **revisão** \> **quarentena** e filtro de **conteúdo**.) 
  
Caso você seja parte da equipe de segurança do Office 365 da sua organização e tem os necessários [permissões atribuídas no Office 365 Security &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md), você pode baixar, versão, relatar e exclua arquivos que são detectados como sendo maliciosas pelo ATP da quarentena.
  
- **Liberando e relatórios de** um arquivo remove o bloco de ATP no arquivo a respectivos team site ou biblioteca de documentos do SharePoint, OneDrive ou Teams da Microsoft. Os usuários são então capazes de abrir, compartilhar e baixe o arquivo. E, quando a opção **enviar o relatório para a Microsoft** está selecionada, o arquivo é relatado como um falso positivo para a Microsoft. 
    
- **Excluir um arquivo** remove o arquivo da quarentena; No entanto, o arquivo ainda está bloqueado sejam abertos ou compartilhado. O arquivo também deve ser excluído em seu respectivos biblioteca ou equipe site de documentos (SharePoint Online, OneDrive for Business ou Teams da Microsoft). 
    
- **Download de um arquivo** permite que você baixe e analisar o arquivo para qualquer falsos positivos. 
    
## <a name="next-steps"></a>Próximas etapas

- [Ativar o Office 365 ATP para SharePoint, OneDrive e equipes da Microsoft](turn-on-atp-for-spo-odb-and-teams.md)
    
- [Exibir informações sobre arquivos mal-intencionados detectada no SharePoint, OneDrive ou Teams da Microsoft](malicious-files-detected-in-spo-odb-or-teams.md)
    
## <a name="related-topics"></a>Tópicos relacionados

[Proteção Avançada contra Ameaças do Office 365](office-365-atp.md) 
  
[Exibir os relatórios de proteção de ameaça avançadas do Office 365](view-reports-for-atp.md)
  
[Permissões de segurança do Office 365 &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md)
  


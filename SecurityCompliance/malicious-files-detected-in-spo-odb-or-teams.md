---
title: Exibir informações sobre arquivos mal-intencionados detectada no SharePoint, OneDrive ou Teams da Microsoft
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 5/31/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 5ed8abf1-c0e9-4e5b-a5b7-2059cea50b61
description: Saiba como tirar ação nesses arquivos e aonde ir para exibir informações sobre arquivos mal-intencionados detectada no SharePoint, OneDrive ou equipes.
ms.openlocfilehash: e9a68c1cee1f2f3fb7fba148365449f0136fe637
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524038"
---
# <a name="view-information-about-malicious-files-detected-in-sharepoint-onedrive-or-microsoft-teams"></a>Exibir informações sobre arquivos mal-intencionados detectada no SharePoint, OneDrive ou Teams da Microsoft

[ATP do Office 365 para SharePoint, OneDrive e as equipes da Microsoft](atp-for-spo-odb-and-teams.md) protege a sua organização contra mal-intencionado arquivos em bibliotecas de documentos e sites de equipe. Quando um arquivo mal-intencionado é detectado, esse arquivo está bloqueado para que ninguém pode abrir, copiar, mover ou compartilhá-la até que outras ações são executadas pela equipe de segurança da organização. Leia este artigo para saber como exibir informações sobre arquivos detectados e quais ações tomar. 
  
> [!TIP]
> Para executar as tarefas descritas neste artigo, você deve ter o necessário [permissões atribuídas no Office 365 Security &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md). 
  
## <a name="view-reports-with-information-about-detected-files"></a>Exibir relatórios com informações sobre arquivos detectados

Para exibir o status e informações detalhadas sobre arquivos que foram detectados pelo Office 365 ATP, você pode usar o relatório de status de proteção de ameaça.
  
1. No Office 365 Security &amp; Centro de conformidade, escolha **relatórios** \> **painel** \> **o status de proteção de ameaça**.
    
2. No canto superior direito do relatório, escolha **tabela do modo de exibição detalhes**.
    
3. Exiba a lista de arquivos que foram detectados no relatório.
    
4. Selecione um item na lista para exibir informações detalhadas, incluindo as ações realizadas, o nome do arquivo, o caminho do arquivo e muito mais.
    
5. Escolha a guia **Advanced Analysis** para exibir informações, como detalhes de análise e comportamento observados. 
    
> [!TIP]
> Para saber mais sobre relatórios disponíveis, consulte [Exibir relatórios de proteção de ameaça avançadas do Office 365](view-reports-for-atp.md). 
  
## <a name="view-and-take-action-on-files-in-quarantine"></a>Exibir e agir em arquivos em quarentena

1. No Office 365 Security &amp; Centro de conformidade, escolha **gerenciamento de ameaça** \> **revisão** \> **quarentena**.
    
2. No canto superior esquerdo, altere o filtro de **Email** para o **conteúdo**.
    
3. Selecione um item na lista para exibir informações detalhadas, incluindo a URL do arquivo.
    
4. Escolha uma ação disponível.
    
  - Escolha **versão &amp; relatório** para desbloquear o arquivo. 
    
    Selecione **enviar o relatório para a Microsoft** para relatar o arquivo como um falso positivo para a Microsoft. 
    
  - Escolha a **baixar o arquivo** para investigar ainda mais o arquivo. 
    
  - Escolha **Excluir** para remover o arquivo da lista de itens em quarentena. Se você escolher essa opção, você também deve excluir o arquivo de seu respectiva biblioteca no SharePoint Online, OneDrive para negócios ou Teams da Microsoft. Essa opção não desbloquear um arquivo sejam abertos ou compartilhado. 
    
5. Escolha **Fechar** para fechar os detalhes para um item selecionado. 
    
> [!TIP]
> Para saber mais sobre o gerenciamento de arquivos em quarentena, consulte [Manage em quarentena mensagens e arquivos como um administrador no Office 365](manage-quarantined-messages-and-files.md). 
  
## <a name="related-topics"></a>Tópicos relacionados

[Proteção Avançada contra Ameaças do Office 365](office-365-atp.md) 
  
[Exibir os relatórios de proteção de ameaça avançadas do Office 365](view-reports-for-atp.md)
  
[Permissões de segurança do Office 365 &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md)
  


---
title: Exibir informações sobre arquivos mal-intencionados detectados no SharePoint, no OneDrive ou no Microsoft Teams
ms.author: deniseb
author: denisebmsft
manager: dansimp
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 5ed8abf1-c0e9-4e5b-a5b7-2059cea50b61
ms.collection:
- M365-security-compliance
description: Saiba onde ir para exibir informações sobre arquivos mal-intencionados detectados no SharePoint, no OneDrive ou no Microsoft Teams e como executar ações nesses arquivos.
ms.openlocfilehash: b16ba88cd4984754f92fac2917f0f2b393600692
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35598837"
---
# <a name="view-information-about-malicious-files-detected-in-sharepoint-onedrive-or-microsoft-teams"></a>Exibir informações sobre arquivos mal-intencionados detectados no SharePoint, no OneDrive ou no Microsoft Teams

O [Office 365 ATP para SharePoint, onedrive e Microsoft Teams](atp-for-spo-odb-and-teams.md) protege sua organização de arquivos mal-intencionados em bibliotecas de documentos e sites de equipe. Quando um arquivo mal-intencionado é detectado, esse arquivo é bloqueado para que ninguém possa abri-lo, copiá-lo ou compartilhá-lo até que outras ações sejam executadas pela equipe de segurança da organização. Leia este artigo para saber como exibir informações sobre arquivos detectados e quais ações executar. 

Para executar as tarefas descritas neste artigo, você deve ter as [permissões necessárias para o centro de conformidade de segurança &amp; do Office 365](permissions-in-the-security-and-compliance-center.md). 
  
## <a name="view-reports-with-information-about-detected-files"></a>Exibir relatórios com informações sobre arquivos detectados

Para exibir o status e informações detalhadas sobre arquivos detectados pelo Office 365 ATP, você pode usar o relatório de status de proteção contra ameaças.
  
1. No [centro de conformidade de &amp; segurança do Office 365](https://protection.office.com), escolha **painel** \> de **relatórios** \> **status da proteção contra ameaças**.
    
2. No canto superior direito do relatório, escolha **Exibir tabela de detalhes**.
    
3. Exiba a lista de arquivos que foram detectados no relatório.
    
4. Selecione um item na lista para exibir informações detalhadas, incluindo ações executadas, o nome do arquivo, o caminho do arquivo e muito mais.
    
5. Escolha a guia **análise avançada** para exibir informações, como comportamento observado e detalhes da análise. 
  
## <a name="view-and-take-action-on-files-in-quarantine"></a>Exibir e executar ação em arquivos em quarentena

1. No centro de conformidade de &amp; segurança do Office 365, escolha **quarentena**de **análise** \> de **Gerenciamento** \> de ameaças.
    
2. No canto superior esquerdo, altere o filtro de **email** para **conteúdo**.
    
3. Selecione um item na lista para exibir informações detalhadas, incluindo a URL do arquivo.
    
4. Escolha uma ação disponível.
    
  - Escolha **relatório &amp; de lançamento** para desbloquear o arquivo. 
    
    Selecione **Enviar relatório para a Microsoft** para relatar o arquivo como um falso positivo para a Microsoft. 
    
  - Escolha **baixar arquivo** para investigar o arquivo. 
    
  - Escolha **excluir** para remover o arquivo da lista de itens em quarentena. Se você escolher essa opção, também deverá excluir o arquivo de sua respectiva biblioteca no SharePoint Online, no OneDrive for Business ou no Microsoft Teams. Essa opção não desbloqueia um arquivo de ser aberto ou compartilhado. 
    
5. Escolha **fechar** para fechar os detalhes de um item selecionado. 
  
  


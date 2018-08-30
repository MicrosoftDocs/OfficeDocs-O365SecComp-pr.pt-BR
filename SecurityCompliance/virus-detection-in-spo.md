---
title: Detecção de vírus no SharePoint Online
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- MET150
ms.assetid: e3c6df61-8513-499d-ad8e-8a91770bff63
description: O Office 365 pode ajudar a proteger seu ambiente contra malware detectando vírus em arquivos que os usuários carregam no SharePoint Online. Arquivos de verificação de vírus depois que eles são carregados. Se um arquivo for encontrado para serem infectados, uma propriedade é definida para que os usuários não podem fazer download ou sincronizar o arquivo.
ms.openlocfilehash: 22e983d35283ff96e1469fdf913e25b8d1d1c485
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524311"
---
# <a name="virus-detection-in-sharepoint-online"></a>Detecção de vírus no SharePoint Online

O Office 365 pode ajudar a proteger seu ambiente contra malware detectando vírus em arquivos que os usuários carregam no SharePoint Online. Arquivos de verificação de vírus depois que eles são carregados. Se um arquivo for encontrado para serem infectados, uma propriedade é definida para que os usuários não podem fazer download ou sincronizar o arquivo.
  
> [!IMPORTANT]
> Esses recursos antivírus no SharePoint Online são uma maneira de conter vírus. Eles não são serve como um ponto único de defesa contra malware para seu ambiente. Recomendamos que todos os clientes para avaliar e implementar a proteção antimalware em diversas camadas e aplicar as práticas recomendadas para proteger sua infraestrutura empresarial. Para obter mais informações sobre as estratégias e práticas recomendadas, consulte [práticas recomendadas de segurança para o Office 365](security-best-practices.md). 
  
## <a name="what-happens-when-an-infected-file-is-uploaded-to-sharepoint-online"></a>O que acontece quando um arquivo infectado é carregado no SharePoint Online?

O Office 365 usa um mecanismo de detecção de vírus comuns. O mecanismo executa de forma assíncrona dentro do SharePoint Online e examina arquivos após terem sido carregadas. Quando um arquivo é encontrado contém um vírus, ela será sinalizada para que ele não pode ser baixado novamente. Em abril de 2018, removemos o limite de 25 MB para arquivos examinados.
  
Aqui está o que acontece:
  
1. Um usuário carrega um arquivo para o SharePoint Online.
    
2. O mecanismo de detecção de vírus varre o arquivo.
    
3. Se for encontrado um vírus, o mecanismo de vírus define uma propriedade no arquivo indicando que infectados.
    
## <a name="what-happens-when-a-user-tries-to-download-an-infected-file-by-using-the-browser"></a>O que acontece quando um usuário tentar baixar um arquivo infectado usando o navegador?

Se um arquivo é infectado com vírus, os usuários não podem baixar o arquivo do SharePoint Online usando o navegador.
  
Aqui está o que acontece:
  
1. Um usuário abre um navegador da web e tenta baixar um arquivo infectado do SharePoint Online.
    
2. O usuário recebe um aviso de que um vírus foi detectado e tem a opção para baixar o arquivo e tente limpá-la usando seu próprio software de vírus.
    
## <a name="what-happens-when-the-onedrive-sync-client-tries-to-sync-an-infected-file"></a>O que acontece quando o cliente de sincronização do OneDrive tenta sincronizar um arquivo infectado?

Se os usuários sincronizar arquivos com o novo cliente de sincronização do OneDrive (OneDrive.exe) ou o OneDrive anterior para o cliente de sincronização de negócios (Groove.exe), se um arquivo contém um vírus, o cliente de sincronização não baixá-lo. O cliente de sincronização exibirá uma notificação que o arquivo não pode ser sincronizado.
  


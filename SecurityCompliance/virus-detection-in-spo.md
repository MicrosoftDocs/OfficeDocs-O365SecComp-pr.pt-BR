---
title: Detecção de vírus no SharePoint Online
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 01/14/2019
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
ms.openlocfilehash: ab02d2d4e82e9427ec6b512490f94ccc9c14b54e
ms.sourcegitcommit: 5ccc3dd0d1c087bffd3a8fc807d5d1750f046eeb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/14/2019
ms.locfileid: "28009587"
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
    
2. O usuário recebe um aviso de que um vírus foi detectado. O usuário tem a opção para baixar o arquivo e tente limpá-la usando seu próprio software de vírus.

> [!NOTE]
> Você pode usar o cmdlet Set-SPOTenant com o parâmetro **DisallowInfectedFileDownload** para não permitir que os usuários baixem um arquivo detectado, até mesmo na janela de aviso do antivírus. Consulte [DisallowInfectedFileDownload] (https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant).
    
## <a name="what-happens-when-the-onedrive-sync-client-tries-to-sync-an-infected-file"></a>O que acontece quando o cliente de sincronização do OneDrive tenta sincronizar um arquivo infectado?

Se os usuários sincronizar arquivos com o novo cliente de sincronização do OneDrive (OneDrive.exe) ou o OneDrive anterior para o cliente de sincronização de negócios (Groove.exe), se um arquivo contém um vírus, o cliente de sincronização não baixá-lo. O cliente de sincronização exibirá uma notificação que o arquivo não pode ser sincronizado.
  


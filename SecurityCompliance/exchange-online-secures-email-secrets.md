---
title: Como o Exchange Online protege seus segredos de email
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/24/2018
ms.audience: ITPro
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 989ba10c-f73f-4efb-ad1b-af3322e5f376
description: Além do centro do Office 365 confiar que fornece informações de conformidade, de privacidade e de segurança para o Office 365, talvez você queira saber como o Office 365 ajuda a protege segredos você fornecer em seus centros de dados. Usamos uma tecnologia chamada Gerenciador de chave distribuído (DKM).
ms.openlocfilehash: a8fe1a2c9393958a391ec69a9a476a06de8c7576
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524579"
---
# <a name="how-exchange-online-secures-your-email-secrets"></a>Como o Exchange Online protege seus segredos de email

Este artigo descreve como a Microsoft protege seus segredos de email em seus datacenters.
  
## <a name="how-do-we-secure-secret-information-provided-by-you"></a>Como protegemos as informações secretas fornecidas por você?

Além do centro do Office 365 confiar que fornece [segurança, privacidade e informações de conformidade para o Office 365](https://go.microsoft.com/fwlink/?linkid=874644), talvez você queira saber como o Office 365 ajuda a protege segredos você fornecer em seus centros de dados. Usamos uma tecnologia chamada Gerenciador de chave distribuído (DKM).
  
O Distributed Key Manager (DKM) é uma funcionalidade no lado do cliente que usa um conjunto de chaves secretas para criptografar e descriptografar informações. Somente os membros de um grupo de segurança específico nos Serviços de Domínio Active Directory podem acessar essas chaves para descriptografar os dados criptografados pelo DKM. No Exchange Online, apenas certas contas de serviço, sob as quais os processos do Exchange são executados, fazem parte do grupo de segurança. Como parte do procedimento operacional padrão no datacenter, nenhum humano recebe credenciais que fazem parte deste grupo de segurança e, portanto, nenhuma pessoa tem acesso às chaves que podem descriptografar esses segredos.
  
Para fins de depuração, solução de problemas ou auditoria, um administrador de datacenter deve solicitar acesso elevado para obter credenciais temporárias que fazem parte do grupo de segurança. Esse processo requer vários níveis de aprovação legal. Se o acesso for concedido, toda as atividades são registradas e auditadas. Além disso, o acesso é concedido apenas por um tempo definido, expirando automaticamente após esse período.
  
Para maior proteção, a tecnologia do DKM inclui a sobreposição de chave e o arquivamento automatizados. Isso também garante que você pode continuar acessando seu conteúdo antigo sem depender da mesma chave indefinidamente.

  
## <a name="where-does-exchange-online-make-use-of-dkm"></a>Em que circunstâncias o Exchange Online usa o DKM?

A Microsoft usa o DKM para criptografar seus segredos nos datacenters do Exchange Online. Por exemplo:
  
- Credenciais de conta de email para contas conectadas. As contas conectadas são as contas de email de terceiros, como Hotmail, Gmail e Yahoo!.
    
- Chaves de raiz de (RMS) do serviço de gerenciamento de direitos. Estas são as chaves de cliente são que uma importados a partir de RMS do Windows Azure ou implantações de RMS de serviços do Active Directory domínio de locais do cliente que são usadas para criptografia e descriptografia de emails com RMS ou Office 365 Message Encryption (OME).
    
## <a name="related-topics"></a>Tópicos relacionados

[Criptografia no Office 365](encryption.md)
  
[Detalhes de referências técnicas sobre a criptografia no Office 365](technical-reference-details-about-encryption.md)
  
[Pessoal assurance no Office 365 Security &amp; Centro de conformidade](https://go.microsoft.com/fwlink/?linkid=874645)
  


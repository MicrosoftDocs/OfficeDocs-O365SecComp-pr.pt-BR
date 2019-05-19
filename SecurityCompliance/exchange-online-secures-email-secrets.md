---
title: Como o Exchange Online protege seus segredos de email
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 5/24/2018
audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 989ba10c-f73f-4efb-ad1b-af3322e5f376
ms.collection:
- M365-security-compliance
description: Além da central de confiabilidade do Office 365, que fornece informações de segurança, privacidade e conformidade do Office 365, você pode querer saber como o Office 365 ajuda a proteger os segredos que você fornece em seus datacenters. Usamos uma tecnologia chamada DKM (Distributed Key Manager).
ms.openlocfilehash: 609d59b6e4da779e0fa663b40fdbf26036753669
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34154582"
---
# <a name="how-exchange-online-secures-your-email-secrets"></a>Como o Exchange Online protege seus segredos de email

Este artigo descreve como a Microsoft protege seus segredos de email em seus datacenters.
  
## <a name="how-do-we-secure-secret-information-provided-by-you"></a>Como protegemos as informações secretas fornecidas por você?

Além da central de confiabilidade do Office 365, que fornece [informações de segurança, privacidade e conformidade do office 365](https://go.microsoft.com/fwlink/?linkid=874644), você pode querer saber como o Office 365 ajuda a proteger os segredos que você fornece em seus datacenters. Usamos uma tecnologia chamada DKM (Distributed Key Manager).
  
O Distributed Key Manager (DKM) é uma funcionalidade no lado do cliente que usa um conjunto de chaves secretas para criptografar e descriptografar informações. Somente os membros de um grupo de segurança específico nos Serviços de Domínio Active Directory podem acessar essas chaves para descriptografar os dados criptografados pelo DKM. No Exchange Online, apenas certas contas de serviço, sob as quais os processos do Exchange são executados, fazem parte do grupo de segurança. Como parte do procedimento operacional padrão no datacenter, nenhum humano recebe credenciais que fazem parte deste grupo de segurança e, portanto, nenhuma pessoa tem acesso às chaves que podem descriptografar esses segredos.
  
Para fins de depuração, solução de problemas ou auditoria, um administrador de datacenter deve solicitar acesso elevado para obter credenciais temporárias que fazem parte do grupo de segurança. Esse processo requer vários níveis de aprovação legal. Se o acesso for concedido, toda as atividades são registradas e auditadas. Além disso, o acesso é concedido apenas por um tempo definido, expirando automaticamente após esse período.
  
Para maior proteção, a tecnologia do DKM inclui a sobreposição de chave e o arquivamento automatizados. Isso também garante que você pode continuar acessando seu conteúdo antigo sem depender da mesma chave indefinidamente.
  
## <a name="where-does-exchange-online-make-use-of-dkm"></a>Em que circunstâncias o Exchange Online usa o DKM?

A Microsoft usa o DKM para criptografar seus segredos nos datacenters do Exchange Online. Por exemplo:
  
- Credenciais de conta de email para contas conectadas. As contas conectadas são as contas de email de terceiros, como Hotmail, Gmail e Yahoo!.
    
- Chaves-raiz do Rights Management Service (RMS). São as chaves de cliente que são importadas do Azure RMS ou de implantações do RMS de serviços de domínio do Active Directory no local que são usadas para criptografar e descriptografar emails com o RMS ou o OME (criptografia de mensagem do Office 365).
    
## <a name="related-topics"></a>Tópicos relacionados

[Criptografia no Office 365](encryption.md)
  
[Detalhes de referências técnicas sobre a criptografia no Office 365](technical-reference-details-about-encryption.md)
  
[Garantia de serviço no centro de conformidade &amp; de segurança do Office 365](https://go.microsoft.com/fwlink/?linkid=874645)
  


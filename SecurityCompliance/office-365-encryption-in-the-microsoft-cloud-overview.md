---
title: Criptografia no Microsoft Cloud
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: Visão geral de criptografia em que o Microsoft Cloud.
ms.openlocfilehash: b8dee7ca7a791878763b885ada40a1d87f074e8e
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524473"
---
# <a name="encryption-in-the-microsoft-cloud"></a>Criptografia no Microsoft Cloud

Dados do cliente em serviços de nuvem da Microsoft enterprise são protegidos por uma variedade de tecnologias e processos, incluindo várias formas de criptografia. (Dados do cliente do office 365 neste documento inclui conteúdo de caixa de correio Exchange Online (corpo do email, entradas de calendário e o conteúdo de anexos de email e, se aplicável, Skype para conteúdo de negócios), o conteúdo de site do SharePoint Online e os arquivos armazenados em sites e arquivos carregados no OneDrive para negócios ou Skype para a empresa.) A Microsoft usa vários métodos de criptografia, protocolos e codificações em seus produtos e serviços para ajudar a fornecer um caminho seguro para os dados do cliente para viajam através de nossos serviços de nuvem e para ajudar a proteger a confidencialidade de dados do cliente que estão armazenados dentro nossos serviços de nuvem. A Microsoft usa alguns dos protocolos mais forte criptografia mais seguro disponíveis para fornecer as barreiras contra acesso não autorizado aos dados do cliente. Gerenciamento de chaves adequado também é um elemento essencial de práticas recomendadas de criptografia e a Microsoft trabalha para garantir que todas as chaves de criptografia gerenciados Microsoft são protegidas adequadamente.

Independentemente da configuração do cliente, os dados do cliente armazenados em serviços de nuvem da Microsoft enterprise são protegidos usando um ou mais formas de criptografia. (Validação do seu imposição e nossa política criptográfica é verificada independentemente por vários auditores de terceiros e relatórios dessas auditorias estão disponíveis no [Portal do serviço de confiança](https://aka.ms/stp)).

A Microsoft fornece tecnologias no lado do serviço que criptografar dados em repouso e em trânsito do cliente. Por exemplo, para os dados em repouso cliente, Microsoft Azure usa [BitLocker](https://docs.microsoft.com/windows/device-security/bitlocker/bitlocker-overview) e [DM-Crypt](https://en.wikipedia.org/wiki/Dm-crypt)e Microsoft Office 365 usa o serviço de [Criptografia de serviço de armazenamento do Windows Azure](https://azure.microsoft.com/documentation/articles/storage-service-encryption/), BitLocker, [Distribuído Key Manager](https://support.office.com/article/989ba10c-f73f-4efb-ad1b-af3322e5f376) (DKM) e Office 365 criptografia. Para os dados de cliente em trânsito, Azure, Office 365, suporte comerciais da Microsoft, Microsoft Dynamics 365, Power BI da Microsoft e Visual Studio Team Services usam protocolos de transporte seguro de padrão do setor, como o Internet Protocol Security (IPsec) e Transport Layer Security (TLS), entre data centers da Microsoft e entre dispositivos do usuário e centros de dados do Microsoft.

Além do nível de linha de base de segurança criptográficos fornecido pela Microsoft, nossos serviços de nuvem também incluem as opções de criptografia adicionais que você pode gerenciar. Por exemplo, é possível habilitar a criptografia para o tráfego entre suas máquinas virtuais do Azure (VMs) e seus usuários. Com [Redes virtuais do Azure](https://azure.microsoft.com/services/virtual-network/), você pode usar o protocolo IPsec padrão do setor para criptografar o tráfego entre o gateway VPN corporativa e o Azure, bem como entre VMs localizado em sua rede Virtual. Além disso, além disso, [novos recursos do Office 365 Message Encryption](set-up-new-message-encryption-capabilities.md) permitem que você enviar emails criptografados para qualquer pessoa.

Acordo com o público chave infraestrutura operacionais padrão de segurança, que é um componente da [Diretiva de segurança da Microsoft](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5868ecc8-50b7-4f91-b43f-640e2b99e86e&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ%20and%20White%20Papers), a Microsoft aproveita os recursos de criptografia incluídos no sistema operacional Windows para certificados e mecanismos de autenticação, que inclui o uso de módulos de criptografia que atendem os do governo dos EUA [Padrões de processamento de informações federais](http://csrc.nist.gov/publications/PubsFIPS.html) (FIPS) padrão de 140-2. (Os números de certificados NIST relevantes para o Microsoft podem ser encontrados emhttp://csrc.nist.gov/groups/STM/cmvp/documents/140-1/1401vend.htm.)

> [NOTA] Para acessar a diretiva de segurança da Microsoft como um recurso, você deve entrar usando sua conta do trabalho ou da escola. Se você não tiver uma assinatura ao mesmo tempo, [você pode se inscrever para uma avaliação gratuita](https://servicetrust.microsoft.com/Home/TrialSubscriptions).

FIPS 140-2 é um padrão projetado especificamente para validar os módulos do produto que implementam criptografia ao invés os produtos que usá-los. Módulos de criptografia que são implementados dentro de um serviço podem ser certificados como atender aos requisitos de força de hash, gerenciamento de chaves e assim por diante. Sempre que recursos criptográficos são empregados para proteger a confidencialidade, integridade ou disponibilidade de dados nos serviços de nuvem da Microsoft, os módulos e codificações usadas atendem a FIPS 140-2 padrão.

Microsoft certifica os módulos criptográficos subjacentes usados em nossos serviços de nuvem com cada nova versão do sistema operacional Windows:
- Windows Azure e o Azure governo dos EUA
- Dynamics 365 e Dynamics 365 US governamentais
- O Office 365, governamentais do Office 365 e defesa do Office 365 dos EUA

Criptografia de dados de cliente do Office 365 em repouso é fornecida por várias tecnologias de no lado do serviço, incluindo o BitLocker, DKM, criptografia de serviço de armazenamento do Windows Azure e criptografia de serviço no Exchange Online, Skype for Business, OneDrive for Business e SharePoint Online. Criptografia do Office 365 service inclui uma opção para usar as chaves de criptografia gerenciado pelo cliente que são armazenadas no armazenamento de chave do Windows Azure. Essa opção de chave gerenciada do cliente, chamada [Chave de cliente do Office 365](https://support.office.com/article/f2cd475a-e592-46cf-80a3-1bfb0fa17697), está disponível para o Exchange Online, SharePoint Online, Skype para negócios e OneDrive for Business.

Para os dados de cliente em trânsito, todos os servidores do Office 365 negociam sessões seguras usando TLS por padrão com as máquinas do cliente para proteger os dados do cliente.  Isso se aplica aos protocolos em qualquer dispositivo usado pelos clientes, como Skype para negócios, Outlook e Outlook na web, os clientes móveis e navegadores da web.

(Todos os servidores voltados para o cliente negociam para TLS 1.2 por padrão, mas também há suporte para negociar um padrão inferior, se necessário).

## <a name="related-links"></a>Links relacionados

- [Criptografia no Azure](office-365-azure-encryption.md)
- [BitLocker e Distributed Key Manager (DKM) para criptografia](office-365-bitlocker-and-distributed-key-manager-for-encryption.md)
- [Criptografia de serviço do Office 365](office-365-service-encryption.md)
- [Criptografia do Office 365 para Skype for Business, OneDrive para negócios, SharePoint Online e Exchange Online](office-365-encryption-for-skype-onedrive-sharepoint-and-exchange.md)
- [Criptografia de dados em trânsito](office-365-encryption-for-data-in-transit.md)
- [Recursos de criptografia de gerenciamento de cliente](office-365-customer-managed-encryption-features.md)
- [Riscos e proteções de criptografia](office-365-encryption-risks-and-protections.md)
- [Criptografia no Microsoft Dynamics 365](office-365-encryption-in-microsoft-dynamics-365.md)
---
title: Criptografia do Office 365 no Microsoft Dynamics 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 5/31/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Resumo: Entenda a criptografia no Microsoft Dynamics 365.'
ms.openlocfilehash: 181db1724f140c86fb1ac1dbf4a4bfb7063d25a3
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523455"
---
# <a name="office-365-encryption-in-microsoft-dynamics-365"></a>Criptografia do Office 365 no Microsoft Dynamics 365

A Microsoft usa a tecnologia de criptografia para proteger os dados do cliente no Dynamics 365 enquanto estiver em repouso um banco de dados do Microsoft e enquanto ele estiver em trânsito entre dispositivos de usuário e nossos data centers. Conexões estabelecidas entre clientes e centros de dados da Microsoft são criptografadas e todos os pontos de extremidade públicos são protegidos por meio de TLS padrão do setor. TLS efetivamente estabelece uma conexão de servidor para navegador segurança avançada para ajudar a garantir a integridade entre áreas de trabalho e centros de dados e a confidencialidade de dados. Depois que a criptografia de dados estiver ativada, ele não pode ser desativado. Para obter mais informações, consulte [criptografia de dados de nível de campo](https://msdn.microsoft.com/en-us/library/dn481562.aspx).

Dynamics 365 usa criptografia padrão da nível de célula do Microsoft SQL Server para um conjunto de atributos da entidade padrão que contenham informações confidenciais, como nomes de usuário e senhas de email. Esse recurso pode ajudar as organizações a atender aos requisitos de conformidade associados com o FIPS 140-2. Criptografia de dados de nível de campo é especialmente importante em cenários que otimizam o [Roteador de Email do Microsoft Dynamics CRM](https://technet.microsoft.com/en-us/library/hh699800.aspx), que deve armazenar nomes de usuário e senhas para habilitar a integração entre uma instância de Dynamics 365 e um serviço de email. 

Todas as instâncias do Dynamics 365 usam [Criptografia de dados transparente do Microsoft SQL Server](https://docs.microsoft.com/sql/relational-databases/security/encryption/transparent-data-encryption?view=sql-server-2017) (TDE) para executar a criptografia de dados quando gravadas no disco (em repouso) em tempo real. TDE criptografa arquivos de dados do SQL Server, o banco de dados do Windows Azure SQL e armazém de dados do SQL Azure. Por padrão, o Microsoft armazena e gerencia as chaves de criptografia do banco de dados para suas instâncias do Dynamics 365. (As chaves que são usadas pelo Dynamics 365 for Financials geradas pela API de proteção de dados do .NET Framework.) 

O recurso de teclas de gerenciar no Centro de administração do Dynamics 365 fornece aos administradores a capacidade de gerenciar Self as chaves de criptografia do banco de dados que estão associadas a instâncias do Dynamics 365. (As chaves de criptografia do banco de dados gerenciados automaticamente só estão disponíveis na atualização para o Microsoft Dynamics 365 de 2017 janeiro e podem não ser disponibilizadas para versões posteriores. Para obter mais informações, consulte [Gerenciar as chaves de criptografia da instância (online) Dynamics 365](https://docs.microsoft.com/dynamics365/customer-engagement/admin/manage-encryption-keys-instance)). O recurso de gerenciamento de chaves suporta PFX e o BYOK criptografia principais arquivos, como aqueles armazenados em um HSM. (Para obter mais informações sobre como gerar e transferir uma chave HSM protegidos pela Internet, consulte [como gerar e transferir protegidos HSM chaves para o Windows Azure chave Vault](https://docs.microsoft.com/azure/key-vault/key-vault-hsm-protected-keys).) 

Para usar a opção de chave de criptografia de carregamento, você precisa de ambos os a chave de criptografia de públicos e particulares.

O recurso de gerenciamento de chaves leva a complexidade do gerenciamento de chaves de criptografia usando o Windows Azure chave Vault para armazenar com segurança as chaves de criptografia. Azure Vault de chave ajuda salvaguarda chaves de criptografia e segredos utilizados pelos aplicativos em nuvem e serviços. O recurso de gerenciamento de chaves não exige que você tem uma assinatura do Windows Azure chave Vault e para a maioria das situações não é necessário para acessar as chaves de criptografia usadas para Dynamics 365 dentro do compartimento.

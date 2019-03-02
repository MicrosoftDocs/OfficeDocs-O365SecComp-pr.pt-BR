---
title: BitLocker do Office 365 para criptografia
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_Enterprise
- M365-security-compliance
- Strat_O365_Enterprise
description: 'Resumo: informações sobre o BitLocker para criptografia na nuvem.'
ms.openlocfilehash: 293c7a3cef3ae2c55a0b12df139baf5302dd3b04
ms.sourcegitcommit: 7adfd8eda038cf25449bdf3df78b5e2fcc1999e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/01/2019
ms.locfileid: "30357422"
---
# <a name="bitlocker-and-distributed-key-manager-dkm-for-encryption"></a>BitLocker e Distributed Key Manager (DKM) para criptografia

Os servidores do Office 365 usam o BitLocker para criptografar as unidades de disco que contêm os dados do cliente em repouso no nível do volume. A criptografia BitLocker é um recurso de proteção de dados interno do Windows. O BitLocker é uma das tecnologias usadas para proteger contra ameaças caso haja interrupções em outros processos ou controles (por exemplo, controle de acesso ou reciclagem de hardware) que podem levar a alguém obtendo acesso físico a discos que contêm dados do cliente. Nesse caso, o BitLocker elimina a possibilidade de roubo de dados ou exposição por causa de computadores e discos perdidos, roubados ou indevidamente descomissionados.

O BitLocker é implantado com a criptografia de 256 bits do padrão de criptografia avançada (AES) em discos que contêm dados do cliente no Exchange Online, no SharePoint Online e no Skype for Business. Os setores de disco são criptografados com uma chave de criptografia de volume (FVEK), que é criptografada com a chave mestra de volume (VMK), que por sua vez está associada ao TPM (módulo de plataforma confiável) no servidor. A VMK protege diretamente a FVEK e, portanto, a proteção da VMK se torna crítica. A figura a seguir ilustra um exemplo da cadeia de proteção de chave do BitLocker para um determinado servidor (neste caso, usando um servidor Exchange Online).

A tabela a seguir descreve a cadeia de proteção de chave do BitLocker para um determinado servidor (neste caso, um servidor Exchange Online).

| PROTETOR DE CHAVE | GRANULARIDADE | COMO É GERADO? | ONDE É ARMAZENADO? | PROTE |
|--------------------------------------------------------------------------------|-------------------------------------------------|----------------|-------------------------|--------------------------------------------------------------------------------------------------|
| Chave externa AES de 256 bits | Por servidor | APIs do BitLocker | TPM ou secreto seguro | Lockbox/controle de acesso |
|  |  |  | Registro do servidor de caixa de correio | TPM criptografado |
| Senha numérica de 48 dígitos | Por disco | APIs do BitLocker | Active Directory | Lockbox/controle de acesso |
| O certificado X. 509 como o agente de recuperação de dados (DRA) também é chamado de protetor de chave pública | Ambiente (por exemplo, multilocatário do Exchange Online) | AUTORIDADE de certificação da Microsoft | Sistema de compilação | Não há um usuário com a senha completa para a chave privada. A senha está sob proteção física. |


O gerenciamento de chaves BitLocker envolve o gerenciamento de chaves de recuperação usadas para desbloquear/recuperar discos criptografados em um datacenter do Office 365. O Office 365 armazena as chaves mestre em um compartilhamento protegido, acessível somente por indivíduos que foram filtrados e aprovados. As credenciais para as chaves são armazenadas em um repositório seguro para dados de controle de acesso (o que chamamos de um "repositório secreto"), que exige um alto nível de aprovação de elevação e gerenciamento para acessar usando uma ferramenta de elevação de acesso just-in-time.

O BitLocker oferece suporte a chaves que se enquadram em duas categorias de gerenciamento:

- Chaves gerenciadas pelo BitLocker, que geralmente são de vida curta e ligadas à vida útil de uma instância do sistema operacional instalada em um servidor ou em um determinado disco. Essas chaves são excluídas e redefinidas durante a reinstalação do servidor ou a formatação do disco.

- Chaves de recuperação do BitLocker, que são gerenciadas fora do BitLocker, mas usadas para descriptografia de disco. O BitLocker usa chaves de recuperação para o cenário no qual um sistema operacional é reinstalado e os discos de dados criptografados já existem. As chaves de recuperação também são usadas por sondas de monitoramento de disponibilidade gerenciada no Exchange Online, onde um respondente pode precisar desbloquear um disco.

Os volumes protegidos por BitLocker são criptografados com uma chave de criptografia de volume completo, que, por sua vez, é criptografada com uma chave mestra de volume. O BitLocker usa algoritmos compatíveis com FIPS para garantir que as chaves de criptografia nunca sejam armazenadas ou enviadas pela conexão. A implementação do Office 365 de dados do cliente em repouso-proteção não se desvia da implementação padrão do BitLocker.
---
title: BitLocker do Office 365 para criptografia
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
description: 'Resumo: Informações sobre o BitLocker para criptografia na nuvem.'
ms.openlocfilehash: 86c6bc9282d7c2b0a7d4e08d4636c8f9c2fa5db8
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524071"
---
# <a name="bitlocker-and-distributed-key-manager-dkm-for-encryption"></a>BitLocker e Distributed Key Manager (DKM) para criptografia
Servidores do Office 365 usam BitLocker para criptografar as unidades de disco que contém os dados em repouso no nível de volume do cliente. Criptografia de disco BitLocker é um recurso de proteção de dados interno do Windows. O BitLocker é uma das tecnologias usadas para a proteção contra ameaças, caso haja falhas em outros processos ou controles (por exemplo, controle de acesso ou reciclagem de hardware) que poderiam levar a alguém que tenha acesso físico nos discos contendo os dados do cliente. Nesse caso, o BitLocker elimina o potencial de dados roubo ou exposição por causa de discos e computadores inadequadamente, perdidos ou roubados.

O BitLocker é implantado com criptografia de 256 bits padrão de criptografia avançada (AES) em discos contendo dados do cliente no Exchange Online, SharePoint Online e Skype para negócios. Setores do disco são criptografadas com um completo Volume criptografia FVEK (chave), que é criptografado com o Volume VMK (chave mestra), que por sua vez, está acoplado para o módulo de plataforma confiável (TPM) no servidor. A VMK protege diretamente a FVEK e portanto, protegendo a VMK se torna crítico. A figura a seguir ilustra um exemplo de cadeia de proteção de chave BitLocker para um determinado servidor (no caso, usando um servidor Exchange Online).

A tabela a seguir descreve a cadeia de proteção de chaves de BitLocker para um determinado servidor (neste caso, um servidor Exchange Online).

| PROTETOR DE CHAVE | GRANULARIDADE | COMO GERADO? | ONDE ELE ESTÁ ARMAZENADO? | PROTEÇÃO |
|--------------------------------------------------------------------------------|-------------------------------------------------|----------------|-------------------------|--------------------------------------------------------------------------------------------------|
| Chave AES de 256 bits externo | Por servidor | APIs de disco BitLocker | TPM ou secreto seguros | Lockbox / controle de acesso |
|  |  |  | Registro do servidor de caixa de correio | TPM criptografada |
| Senha numérica de 48 dígitos | Por disco | APIs de disco BitLocker | Active Directory | Lockbox / controle de acesso |
| Protetor de chave pública também chamado de certificado x. 509 como o agente de recuperação de dados (DRA) | Ambiente (por exemplo, o Exchange Online multi-inquilinos) | Autoridade de certificação da Microsoft | Criar sistema | Nenhum usuário tem a senha completa para a chave privada. A senha é sob proteção física. |


Gerenciamento de chaves BitLocker envolve o gerenciamento de chaves de recuperação que são usadas para desbloquear/recuperar discos criptografados em um datacenter do Office 365. O Office 365 armazena as chaves mestre em um compartilhamento protegido, acessível apenas por pessoas que foram analisadas e aprovadas. As credenciais para as chaves são armazenadas em um repositório seguro para dados de controle de acesso (o que é chamada "repositório secreto"), que exige um alto nível de aprovações elevação e gerenciamento para acessar usando uma ferramenta do access just-in-time elevação.

O BitLocker suporta chaves que se enquadram em duas categorias de gerenciamento:
- O BitLocker gerenciados chaves, que são geralmente temporários e e associado com o tempo de vida de uma instância de sistema operacional instalado em um servidor ou em um determinado disco. Essas chaves são excluídas e redefinidos durante a reinstalação do servidor ou a formatação de disco.
- Chaves de recuperação de disco BitLocker, que são gerenciadas fora BitLocker mas usadas para a descriptografia de disco. O BitLocker usa as chaves de recuperação para o cenário no qual um sistema operacional é reinstalado e discos de dados criptografados já existirem. Chaves de recuperação também são usadas pelo monitoramento sondas no Exchange Online onde um Respondente talvez precisem de disponibilidade gerenciada para desbloquear um disco.

Volumes protegidas pelo BitLocker são criptografados com uma chave de criptografia de volume completo, que por sua vez, é criptografada com uma chave mestra de volume. O BitLocker usa algoritmos compatíveis com FIPS para garantir que as chaves de criptografia nunca são armazenadas ou enviadas por telefone criptografado. A implementação do Office 365 do cliente em-rest-proteção de dados não desviar da implementação de disco BitLocker padrão.
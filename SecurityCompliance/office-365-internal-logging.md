---
title: Log de interno do Office 365 para engenharia do Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/18/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: Uma explicação de log como interno para o Office 365 engenharia equipes funciona.
ms.openlocfilehash: 1a613584b6b815524435acb20db7a8022d95e3bc
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523763"
---
# <a name="internal-logging-for-office-365-engineering"></a>Log interno de engenharia do Office 365
Além de eventos e dados de log disponíveis para os clientes, há também um sistema de conjunto de dados de log interno que está disponível para os engenheiros do Office 365. Muitos tipos diferentes de dados de log são carregados dos servidores do Office 365 para um serviço chamado Cosmos de computação de dados interno, ganhar. A equipe de cada serviço carrega os logs de auditoria de seus respectivos servidores no banco de dados Cosmos para agregação de lista segura e análise. Essa transferência de dados ocorre via uma conexão FIPS 140-2-validado TLS em especificamente aprovadas portas e protocolos usando uma ferramenta de automação proprietárias chamada o carregador de dados do Office (ODL).

Equipes de serviço usam Cosmos como um repositório centralizado para conduzir uma análise de uso do aplicativo para medir o desempenho operacional e do sistema e procurar anormalidades e padrões que podem indicar problemas ou problemas de segurança. A equipe de cada serviço carrega uma linha de base dos logs em Cosmos, dependendo se o que procuram para analisar, que geralmente incluem:
- Logs de eventos
- Logs de AppLocker
- Dados de desempenho
- Dados do System Center
- Registros de detalhe de chamada
- Dados qualidade da experiência
- Logs do servidor Web do IIS
- Logs do SQL Server
- Dados de syslog
- Logs de auditoria de segurança

Antes de carregar dados em Cosmos, o aplicativo ODL usa um serviço de depuração para obscurecer quaisquer campos que contêm dados de clientes, informações de locatário e informações de identificação do usuário final e substituir aos campos com um valor de hash. Os logs de anonymized e hash são reconfigurados e, em seguida, carregados em Cosmos. Equipes de atendimento executar consultas com escopo em relação a seus dados em Cosmos para correlação, alertas e relatórios. O período de retenção de dados de log de auditoria no Cosmos é determinado pelas equipes de serviço; a maioria dos dados de log de auditoria são mantidos por 90 dias ou mais para oferecer suporte a investigações de incidentes de segurança e atender aos requisitos normativos de retenção.

Acesso aos dados do Office 365 armazenados em Cosmos é restrito aos pessoal autorizado. Microsoft restringe o gerenciamento de auditoria funcionalidade limitado subconjunto dos membros da equipe de serviço que são responsáveis por funcionalidade de auditoria. Esses membros da equipe não têm a capacidade de modificar ou excluir dados de Cosmos e todas as alterações aos mecanismos de registro em log para Cosmos são registradas e auditadas.

A equipe de cada serviço acessa seus dados de log para análise por autorizar determinados aplicativos conduzir específicos de análise. Por exemplo, a equipe de segurança do Office 365 usa dados de Cosmos por meio de um analisador de log de eventos proprietárias para correlacionar, alerta e gerar relatórios acionáveis em atividades suspeitas possíveis no ambiente de produção do Office 365. Os relatórios a partir desses dados são usados para corrigir vulnerabilidades e para melhorar o desempenho geral do serviço. Se um alerta específico ou relatório requer ainda mais investigação, o pessoal de serviço pode solicitar que os dados importados volta para o serviço do Office 365. Desde o log específico sendo importados do Cosmos é em criptografado e pessoal de serviço não têm acesso às chaves de descriptografia, programaticamente, o log de destino é passado por meio de um serviço de descriptografia que retorna resultados com escopo para a equipe de suporte autorizado. Quaisquer vulnerabilidades encontradas a partir deste exercício informadas e escalonada usando canais de gerenciamento de incidentes de segurança padrão da Microsoft.

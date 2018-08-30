---
title: O que os modelos de política de DLP incluem
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: reference
f1_keywords:
- ms.o365.cc.DLPNewPolicyFromTemplate
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c2e588d3-8f4f-4937-a286-8c399f28953a
description: Prevenção de perda de dados (DLP) no Office 365 Security &amp; Centro de conformidade inclui os modelos de política de prontos para uso que abordam os requisitos de conformidade comuns, como ajudar a proteger informações confidenciais sujeito no (U.S. Health Insurance Act HIPAA), EUA Gramm-Leach-Bliley Act (GLBA) ou EUA Patriot Act. Este tópico lista toda a diretiva de modelos, quais tipos de informações confidenciais eles procuram e quais são as padrão condições e ações.
ms.openlocfilehash: 345738244b9573b1af4d55ede86a568bf136f048
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524218"
---
# <a name="what-the-dlp-policy-templates-include"></a>O que os modelos de política de DLP incluem

Prevenção de perda de dados (DLP) no Office 365 Security &amp; Centro de conformidade inclui os modelos de política de prontos para uso que abordam os requisitos de conformidade comuns, como ajudar a proteger informações confidenciais sujeito no (U.S. Health Insurance Act HIPAA), EUA Gramm-Leach-Bliley Act (GLBA) ou EUA Patriot Act. Este tópico lista toda a diretiva de modelos, quais tipos de informações confidenciais eles procuram e quais são as padrão condições e ações. Este tópico não inclui todos os detalhes de como cada modelo de política é configurado; em vez disso, o tópico apresenta com você informações suficientes para ajudá-lo a decidir qual modelo é o ponto de partida melhor para seu cenário. Lembre-se de que você pode personalizar esses modelos de política para atender às suas necessidades específicas.
  
## <a name="australia-financial-data"></a>Dados Financeiros da Austrália

|**Nome da regra**|**Condições <br/> (incluindo os tipos de informações confidenciais)**|**Ações**|
|:-----|:-----|:-----|
|Finanças da Austrália: Examinar o conteúdo compartilhado fora - contagem baixa  <br/> | Conteúdo tem informações confidenciais:  <br/>  Código SWIFT — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Contribuinte Australiano — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Conta Bancária na Austrália — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número do Cartão de Crédito — Contagem Mín. 1, Contagem Máx. 9  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> |Enviar uma notificação  <br/> |
|Finanças da Austrália: Examinar o conteúdo compartilhado fora - contagem alta  <br/> | Conteúdo tem informações confidenciais:  <br/>  Código SWIFT — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de Contribuinte Australiano — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de Conta Bancária na Austrália — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número do Cartão de Crédito — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> | Bloquear o acesso ao conteúdo  <br/>  Enviar uma notificação  <br/>  Permitir substituição  <br/>  Exigir justificativa comercial  <br/>  Enviar relatório de incidente  <br/> |
   
## <a name="australia-health-records-act-hrip-act"></a>Ato de Registros de Integridade da Austrália (Ato HRIP)

|**Nome da regra**|**Condições <br/> (incluindo os tipos de informações confidenciais)**|**Ações**|
|:-----|:-----|:-----|
|HRIP da Austrália: Examinar o conteúdo compartilhado fora - contagem baixa  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de Contribuinte Australiano — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Conta Médica da Austrália — Contagem Mín. 1, Contagem Máx. 9  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> |Enviar uma notificação  <br/> |
|HRIP da Austrália: Examinar o conteúdo compartilhado fora - contagem alta  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de Contribuinte Australiano — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de Conta Médica da Austrália — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> | Bloquear o acesso ao conteúdo  <br/>  Enviar uma notificação  <br/>  Permitir substituição  <br/>  Exigir justificativa comercial  <br/>  Enviar relatório de incidente  <br/> |
   
## <a name="australia-personally-identifiable-information-pii-data"></a>Dados de Informações Identificáveis Pessoalmente (PII) da Austrália

|**Nome da regra**|**Condições <br/> (incluindo os tipos de informações confidenciais)**|**Ações**|
|:-----|:-----|:-----|
|PII da Austrália: Examinar o conteúdo compartilhado fora - contagem baixa  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de Contribuinte Australiano — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de carteira de motorista da Austrália – Contagem Mín. 1, Contagem Máx. 9  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> |Enviar uma notificação  <br/> |
|PII da Austrália: Examinar o conteúdo compartilhado fora - contagem alta  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de Contribuinte Australiano — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de carteira de motorista da Austrália – Contagem Mín. 10, Contagem Máx. qualquer  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> | Bloquear o acesso ao conteúdo  <br/>  Enviar uma notificação  <br/>  Permitir substituição  <br/>  Exigir justificativa comercial  <br/>  Enviar relatório de incidente  <br/> |
   
## <a name="australia-privacy-act"></a>Ato de Privacidade da Austrália

|**Nome da regra**|**Condições <br/> (incluindo os tipos de informações confidenciais)**|**Ações**|
|:-----|:-----|:-----|
|Privacidade da Austrália: Examinar o conteúdo compartilhado fora - contagem baixa  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de carteira de motorista da Austrália – Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Passaporte da Austrália — Contagem Mín. 1, Contagem Máx. 9  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> |Enviar uma notificação  <br/> |
|Privacidade da Austrália: Examinar o conteúdo compartilhado fora - contagem alta  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de carteira de motorista da Austrália – Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de Passaporte da Austrália — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> | Bloquear o acesso ao conteúdo  <br/>  Enviar uma notificação  <br/>  Permitir substituição  <br/>  Exigir justificativa comercial  <br/>  Enviar relatório de incidente  <br/> |
   
## <a name="canada-financial-data"></a>Dados Financeiros do Canadá

|**Nome da regra**|**Condições <br/> (incluindo os tipos de informações confidenciais)**|**Ações**|
|:-----|:-----|:-----|
|Dados Financeiros do Canadá: Examinar o conteúdo compartilhado fora - contagem baixa  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número do Cartão de Crédito — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Conta Bancária do Canadá — Contagem Mín. 1, Contagem Máx. 9  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> |Enviar uma notificação  <br/> |
|Dados Financeiros do Canadá: Examinar o conteúdo compartilhado fora - contagem alta  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número do Cartão de Crédito — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de Conta Bancária do Canadá — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> | Bloquear o acesso ao conteúdo  <br/>  Enviar uma notificação  <br/>  Permitir substituição  <br/>  Exigir justificativa comercial  <br/>  Enviar relatório de incidente  <br/> |
   
## <a name="canada-health-information-act-hia"></a>Ato de Informações de Saúde do Canadá (HIA)

|**Nome da regra**|**Condições <br/> (incluindo os tipos de informações confidenciais)**|**Ações**|
|:-----|:-----|:-----|
|HIA do Canadá: Examinar o conteúdo compartilhado fora - contagem baixa  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de Passaporte do Canadá — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Seguro Social do Canadá — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número do Serviço de Saúde do Canadá — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Identificação de Saúde Pessoal (PHIN) Canadense – Contagem Mín. 1, Contagem Máx. 9  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> |Enviar uma notificação  <br/> |
|HIA do Canadá: Examinar o conteúdo compartilhado fora - contagem alta  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de Passaporte do Canadá — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de Seguro Social do Canadá — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número do Serviço de Saúde do Canadá — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de Identificação de Saúde Pessoal (PHIN) Canadense – Contagem Mín. 10, Contagem Máx. qualquer  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> | Bloquear o acesso ao conteúdo  <br/>  Enviar uma notificação  <br/>  Permitir substituição  <br/>  Exigir justificativa comercial  <br/>  Enviar relatório de incidente  <br/> |
   
## <a name="canada-personal-health-act-phipa---ontario"></a>Ato de Saúde Pessoal do Canadá (PHIPA) - Ontário

|**Nome da regra**|**Condições <br/> (incluindo os tipos de informações confidenciais)**|**Ações**|
|:-----|:-----|:-----|
|PHIPA do Canadá: Examinar o conteúdo compartilhado fora - contagem baixa  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de Passaporte do Canadá — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Seguro Social do Canadá — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número do Serviço de Saúde do Canadá — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Identificação de Saúde Pessoal (PHIN) Canadense – Contagem Mín. 1, Contagem Máx. 9  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> |Enviar uma notificação  <br/> |
|PHIPA do Canadá: Examinar o conteúdo compartilhado fora - contagem alta  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de Passaporte do Canadá — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de Seguro Social do Canadá — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número do Serviço de Saúde do Canadá — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de Identificação de Saúde Pessoal (PHIN) Canadense – Contagem Mín. 10, Contagem Máx. qualquer  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> | Bloquear o acesso ao conteúdo  <br/>  Enviar uma notificação  <br/>  Permitir substituição  <br/>  Exigir justificativa comercial  <br/>  Enviar relatório de incidente  <br/> |
   
## <a name="canada-personal-health-information-act-phia---manitoba"></a>Ato de Informações de Saúde Pessoais do Canadá (PHIA) - Manitoba

|**Nome da regra**|**Condições <br/> (incluindo os tipos de informações confidenciais)**|**Ações**|
|:-----|:-----|:-----|
|PHIA do Canadá: Examinar o conteúdo compartilhado fora - contagem baixa  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de Seguro Social do Canadá — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número do Serviço de Saúde do Canadá — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Identificação de Saúde Pessoal (PHIN) Canadense – Contagem Mín. 1, Contagem Máx. 9  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> |Enviar uma notificação  <br/> |
|PHIA do Canadá: Examinar o conteúdo compartilhado fora - contagem alta  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de Seguro Social do Canadá — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número do Serviço de Saúde do Canadá — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de Identificação de Saúde Pessoal (PHIN) Canadense – Contagem Mín. 10, Contagem Máx. qualquer  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> | Bloquear o acesso ao conteúdo  <br/>  Enviar uma notificação  <br/>  Permitir substituição  <br/>  Exigir justificativa comercial  <br/>  Enviar relatório de incidente  <br/> |
   
## <a name="canada-personal-information-protection-act-pipa"></a>Ato de Proteção a Informações Pessoais do Canadá (PIPA)

|**Nome da regra**|**Condições <br/> (incluindo os tipos de informações confidenciais)**|**Ações**|
|:-----|:-----|:-----|
|PIPA do Canadá: Examinar o conteúdo compartilhado fora - contagem baixa  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de Passaporte do Canadá — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Seguro Social do Canadá — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número do Serviço de Saúde do Canadá — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Identificação de Saúde Pessoal (PHIN) Canadense – Contagem Mín. 1, Contagem Máx. 9  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> |Enviar uma notificação  <br/> |
|PIPA do Canadá: Examinar o conteúdo compartilhado fora - contagem alta  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de Passaporte do Canadá — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de Seguro Social do Canadá — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número do Serviço de Saúde do Canadá — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de Identificação de Saúde Pessoal (PHIN) Canadense – Contagem Mín. 10, Contagem Máx. qualquer  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> | Bloquear o acesso ao conteúdo  <br/>  Enviar uma notificação  <br/>  Permitir substituição  <br/>  Exigir justificativa comercial  <br/>  Enviar relatório de incidente  <br/> |
   
## <a name="canada-personal-information-protection-act-pipeda"></a>Ato de Proteção a Informações Pessoais do Canadá (PIPEDA)

|**Nome da regra**|**Condições <br/> (incluindo os tipos de informações confidenciais)**|**Ações**|
|:-----|:-----|:-----|
|PIPEDA do Canadá: Examinar o conteúdo compartilhado fora - contagem baixa  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de carteira de motorista do Canadá – Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Conta Bancária do Canadá — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Passaporte do Canadá — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Seguro Social do Canadá — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número do Serviço de Saúde do Canadá — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Identificação de Saúde Pessoal (PHIN) Canadense – Contagem Mín. 1, Contagem Máx. 9  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> |Enviar uma notificação  <br/> |
|PIPEDA do Canadá: Examinar o conteúdo compartilhado fora - contagem alta  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de carteira de motorista do Canadá – Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de Conta Bancária do Canadá — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de Passaporte do Canadá — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de Seguro Social do Canadá — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número do Serviço de Saúde do Canadá — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de Identificação de Saúde Pessoal (PHIN) Canadense – Contagem Mín. 10, Contagem Máx. qualquer  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> | Bloquear o acesso ao conteúdo  <br/>  Enviar uma notificação  <br/>  Permitir substituição  <br/>  Exigir justificativa comercial  <br/>  Enviar relatório de incidente  <br/> |
   
## <a name="canada-personally-identifiable-information-pii-data"></a>Dados de Informações Identificáveis Pessoalmente (PII) do Canadá

|**Nome da regra**|**Condições <br/> (incluindo os tipos de informações confidenciais)**|**Ações**|
|:-----|:-----|:-----|
|PII do Canadá: Examinar o conteúdo compartilhado fora - contagem baixa  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de carteira de motorista do Canadá – Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Conta Bancária do Canadá — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Passaporte do Canadá — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Seguro Social do Canadá — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número do Serviço de Saúde do Canadá — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Identificação de Saúde Pessoal (PHIN) Canadense – Contagem Mín. 1, Contagem Máx. 9  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> |Enviar uma notificação  <br/> |
|PII do Canadá: Examinar o conteúdo compartilhado fora - contagem alta  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de carteira de motorista do Canadá – Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de Conta Bancária do Canadá — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de Passaporte do Canadá — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de Seguro Social do Canadá — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número do Serviço de Saúde do Canadá — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de Identificação de Saúde Pessoal (PHIN) Canadense – Contagem Mín. 10, Contagem Máx. qualquer  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> | Bloquear o acesso ao conteúdo  <br/>  Enviar uma notificação  <br/>  Permitir substituição  <br/>  Exigir justificativa comercial  <br/>  Enviar relatório de incidente  <br/> |
   
## <a name="france-data-protection-act"></a>Ato de Proteção de Dados da França

|**Nome da regra**|**Condições <br/> (incluindo os tipos de informações confidenciais)**|**Ações**|
|:-----|:-----|:-----|
|DPA da França: Examinar o conteúdo compartilhado fora - contagem baixa  <br/> | Conteúdo tem informações confidenciais:  <br/>  Cartão de ID Nacional (CNI) da França — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Inscrição na Previdência Social na França (INSEE) — Contagem Mín. 1, Contagem Máx. 9  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> |Enviar uma notificação  <br/> |
|DPA da França: Examinar o conteúdo compartilhado fora - contagem alta  <br/> | Conteúdo tem informações confidenciais:  <br/>  Cartão de ID Nacional (CNI) da França — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de Inscrição na Previdência Social na França (INSEE) — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> | Bloquear o acesso ao conteúdo  <br/>  Enviar uma notificação  <br/>  Permitir substituição  <br/>  Exigir justificativa comercial  <br/>  Enviar relatório de incidente  <br/> |
   
## <a name="france-financial-data"></a>Dados Financeiros da França

|**Nome da regra**|**Condições <br/> (incluindo os tipos de informações confidenciais)**|**Ações**|
|:-----|:-----|:-----|
|Finanças da França: Examinar o conteúdo compartilhado fora - contagem baixa  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número do Cartão de Crédito — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Cartão de Débito da UE — Contagem Mín. 1, Contagem Máx. 9  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> |Enviar uma notificação  <br/> |
|Finanças da França: Examinar o conteúdo compartilhado fora - contagem alta  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número do Cartão de Crédito — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de Cartão de Débito da UE — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> | Bloquear o acesso ao conteúdo  <br/>  Enviar uma notificação  <br/>  Permitir substituição  <br/>  Exigir justificativa comercial  <br/>  Enviar relatório de incidente  <br/> |
   
## <a name="france-personally-identifiable-information-pii-data"></a>Dados de Informações Identificáveis Pessoalmente (PII) da França

|**Nome da regra**|**Condições <br/> (incluindo os tipos de informações confidenciais)**|**Ações**|
|:-----|:-----|:-----|
|PII da França: Examinar o conteúdo compartilhado fora - contagem baixa  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de Inscrição na Previdência Social na França (INSEE) — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de carteira de motorista da França – Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Passaporte da França — Contagem Mín. 1, Contagem Máx. 9  <br/>  Cartão de ID Nacional (CNI) da França — Contagem Mín. 1, Contagem Máx. 9  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> |Enviar uma notificação  <br/> |
|PII da França: Examinar o conteúdo compartilhado fora - contagem alta  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de Inscrição na Previdência Social na França (INSEE) — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de carteira de motorista da França – Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de Passaporte da França — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Cartão de ID Nacional (CNI) da França — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> | Bloquear o acesso ao conteúdo  <br/>  Enviar uma notificação  <br/>  Permitir substituição  <br/>  Exigir justificativa comercial  <br/>  Enviar relatório de incidente  <br/> |
   
## <a name="general-data-protection-regulation-gdpr"></a>Proteção de dados gerais regulamentação (GDPR)

|**Nome da regra**|**Condições <br/> (incluindo os tipos de informações confidenciais)**|**Ações**|
|:-----|:-----|:-----|
|Volume baixo da UE confidenciais conteúdo encontrado  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de Cartão de Débito da UE — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de carteira de motorista da UE — Min contagem 1, a contagem máxima 9  <br/>  Número de identificação nacional da UE — Contagem Min 1, a contagem máxima 9  <br/>  Número de passaporte da UE — Contagem Min 1, a contagem máxima 9  <br/>  Número de Seguridade Social da UE (SSN) ou ID equivalente — Min contagem 1, a contagem máxima 9  <br/>  Contagem de Min da UE imposto identificação TIN (número) — 1, a contagem máxima 9  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> |Enviar relatórios de incidentes ao administrador  <br/> |
|Alto volume de conteúdo da UE confidenciais encontrado  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de Cartão de Débito da UE — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de carteira de motorista da UE — Min contagem 1, a contagem máxima 9  <br/>  Número de identificação nacional da UE — Contagem Min 1, a contagem máxima 9  <br/>  Número de passaporte da UE — Contagem Min 1, a contagem máxima 9  <br/>  Número de Seguridade Social da UE (SSN) ou ID equivalente — Min contagem 1, a contagem máxima 9  <br/>  Contagem de Min da UE imposto identificação TIN (número) — 1, a contagem máxima 9  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> | Restringir o acesso ao conteúdo para usuários externos  <br/>  Notificar os usuários com dicas de email e a diretiva  <br/>  Permitir substituição  <br/>  Exigir justificativa comercial  <br/>  Enviar relatórios de incidentes ao administrador  <br/> |
   
## <a name="germany-financial-data"></a>Dados Financeiros da Alemanha

|**Nome da regra**|**Condições <br/> (incluindo os tipos de informações confidenciais)**|**Ações**|
|:-----|:-----|:-----|
|Dados Financeiros da Alemanha: Examinar o conteúdo compartilhado fora - contagem baixa  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número do Cartão de Crédito — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Cartão de Débito da UE — Contagem Mín. 1, Contagem Máx. 9  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> |Enviar uma notificação  <br/> |
|Dados Financeiros da Alemanha: Examinar o conteúdo compartilhado fora - contagem alta  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número do Cartão de Crédito — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de Cartão de Débito da UE — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> | Bloquear o acesso ao conteúdo  <br/>  Enviar uma notificação  <br/>  Permitir substituição  <br/>  Exigir justificativa comercial  <br/>  Enviar relatório de incidente  <br/> |
   
## <a name="germany-personally-identifiable-information-pii-data"></a>Dados de Informações Identificáveis Pessoalmente (PII) da Alemanha

|**Nome da regra**|**Condições <br/> (incluindo os tipos de informações confidenciais)**|**Ações**|
|:-----|:-----|:-----|
|PII da Alemanha: Examinar o conteúdo compartilhado fora - contagem baixa  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de carteira de motorista da Alemanha – Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Passaporte da Alemanha — Contagem Mín. 1, Contagem Máx. 9  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> |Enviar uma notificação  <br/> |
|PII da Alemanha: Examinar o conteúdo compartilhado fora - contagem alta  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de carteira de motorista da Alemanha – Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de Passaporte da Alemanha — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> | Bloquear o acesso ao conteúdo  <br/>  Enviar uma notificação  <br/>  Permitir substituição  <br/>  Exigir justificativa comercial  <br/>  Enviar relatório de incidente  <br/> |
   
## <a name="israel-financial-data"></a>Dados Financeiros de Israel

|**Nome da regra**|**Condições <br/> (incluindo os tipos de informações confidenciais)**|**Ações**|
|:-----|:-----|:-----|
|Dados Financeiros de Israel: Examinar o conteúdo compartilhado fora - contagem baixa  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de Conta Bancária de Israel — Contagem Mín. 1, Contagem Máx. 9  <br/>  Código SWIFT — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número do Cartão de Crédito — Contagem Mín. 1, Contagem Máx. 9  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> |Enviar uma notificação  <br/> |
|Dados Financeiros de Israel: Examinar o conteúdo compartilhado fora - contagem alta  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de Conta Bancária de Israel — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Código SWIFT — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número do Cartão de Crédito — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> | Bloquear o acesso ao conteúdo  <br/>  Enviar uma notificação  <br/>  Permitir substituição  <br/>  Exigir justificativa comercial  <br/>  Enviar relatório de incidente  <br/> |
   
## <a name="israel-personally-identifiable-information-pii-data"></a>Dados de Informações Identificáveis Pessoalmente (PII) de Israel

|**Nome da regra**|**Condições <br/> (incluindo os tipos de informações confidenciais)**|**Ações**|
|:-----|:-----|:-----|
|PII de Israel: Examinar o conteúdo compartilhado fora - contagem baixa  <br/> | Conteúdo tem informações confidenciais:  <br/>  ID Nacional Israelense — Contagem Mín. 1, Contagem Máx. 9  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> |Enviar uma notificação  <br/> |
|PII de Israel: Examinar o conteúdo compartilhado fora - contagem alta  <br/> | Conteúdo tem informações confidenciais:  <br/>  ID Nacional Israelense — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> | Bloquear o acesso ao conteúdo  <br/>  Enviar uma notificação  <br/>  Permitir substituição  <br/>  Exigir justificativa comercial  <br/>  Enviar relatório de incidente  <br/> |
   
## <a name="israel-protection-of-privacy"></a>Proteção de Privacidade de Israel

|**Nome da regra**|**Condições <br/> (incluindo os tipos de informações confidenciais)**|**Ações**|
|:-----|:-----|:-----|
|Privacidade de Israel: Examinar o conteúdo compartilhado fora - contagem baixa  <br/> | Conteúdo tem informações confidenciais:  <br/>  ID Nacional Israelense — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Conta Bancária de Israel — Contagem Mín. 1, Contagem Máx. 9  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> |Enviar uma notificação  <br/> |
|Privacidade de Israel: Examinar o conteúdo compartilhado fora - contagem alta  <br/> | Conteúdo tem informações confidenciais:  <br/>  ID Nacional Israelense — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de Conta Bancária de Israel — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> | Bloquear o acesso ao conteúdo  <br/>  Enviar uma notificação  <br/>  Permitir substituição  <br/>  Exigir justificativa comercial  <br/>  Enviar relatório de incidente  <br/> |
   
## <a name="japan-financial-data"></a>Dados Financeiros do Japão

|**Nome da regra**|**Condições <br/> (incluindo os tipos de informações confidenciais)**|**Ações**|
|:-----|:-----|:-----|
|Finanças do Japão: Examinar o conteúdo compartilhado fora - contagem baixa  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de Conta Bancária do Japão — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número do Cartão de Crédito — Contagem Mín. 1, Contagem Máx. 9  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> |Enviar uma notificação  <br/> |
|Finanças do Japão: Examinar o conteúdo compartilhado fora - contagem alta  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de Conta Bancária do Japão — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número do Cartão de Crédito — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> | Bloquear o acesso ao conteúdo  <br/>  Enviar uma notificação  <br/>  Permitir substituição  <br/>  Exigir justificativa comercial  <br/>  Enviar relatório de incidente  <br/> |
   
## <a name="japan-personally-identifiable-information-pii-data"></a>Dados de Informações Identificáveis Pessoalmente (PII) do Japão

|**Nome da regra**|**Condições <br/> (incluindo os tipos de informações confidenciais)**|**Ações**|
|:-----|:-----|:-----|
|PII do Japão: Examinar o conteúdo compartilhado fora - contagem baixa  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de Registro de Residente no Japão — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número do Seguro Social Japonês (SIN) — Contagem Mín. 1, Contagem Máx. 9  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> |Enviar uma notificação  <br/> |
|PII do Japão: Examinar o conteúdo compartilhado fora - contagem alta  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de Registro de Residente no Japão — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número do Seguro Social Japonês (SIN) — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> | Bloquear o acesso ao conteúdo  <br/>  Enviar uma notificação  <br/>  Permitir substituição  <br/>  Exigir justificativa comercial  <br/>  Enviar relatório de incidente  <br/> |
   
## <a name="japan-protection-of-personal-information"></a>Proteção de Informações Pessoais do Japão

|**Nome da regra**|**Condições <br/> (incluindo os tipos de informações confidenciais)**|**Ações**|
|:-----|:-----|:-----|
|PPI do Japão: Examinar o conteúdo compartilhado fora - contagem baixa  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de Registro de Residente no Japão — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número do Seguro Social Japonês (SIN) — Contagem Mín. 1, Contagem Máx. 9  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> |Enviar uma notificação  <br/> |
|PPI do Japão: Examinar o conteúdo compartilhado fora - contagem alta  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de Registro de Residente no Japão — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número do Seguro Social Japonês (SIN) — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> | Bloquear o acesso ao conteúdo  <br/>  Enviar uma notificação  <br/>  Permitir substituição  <br/>  Exigir justificativa comercial  <br/>  Enviar relatório de incidente  <br/> |
   
## <a name="pci-data-security-standard-pci-dss"></a>Padrão de Segurança de Dados PCI (PCI DSS)

|**Nome da regra**|**Condições <br/> (incluindo os tipos de informações confidenciais)**|**Ações**|
|:-----|:-----|:-----|
|DSS PCI: Examinar o conteúdo compartilhado fora - contagem baixa  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número do Cartão de Crédito — Contagem Mín. 1, Contagem Máx. 9  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> |Enviar uma notificação  <br/> |
|DSS PCI: Examinar o conteúdo compartilhado fora - contagem alta  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número do Cartão de Crédito — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> | Bloquear o acesso ao conteúdo  <br/>  Enviar uma notificação  <br/>  Permitir substituição  <br/>  Exigir justificativa comercial  <br/>  Enviar relatório de incidente  <br/> |
   
## <a name="saudi-arabia---anti-cyber-crime-law"></a>Arábia Saudita - Lei Contra Crimes Cibernéticos

|**Nome da regra**|**Condições <br/> (incluindo os tipos de informações confidenciais)**|**Ações**|
|:-----|:-----|:-----|
|ACC da Arábia Saudita: Examinar o conteúdo compartilhado fora - contagem baixa  <br/> | Conteúdo tem informações confidenciais:  <br/>  Código SWIFT — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Conta Bancária Internacional (IBAN) — Contagem Mín. 1, Contagem Máx. 9  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> |Enviar uma notificação  <br/> |
|ACC da Arábia Saudita: Examinar o conteúdo compartilhado fora - contagem alta  <br/> | Conteúdo tem informações confidenciais:  <br/>  Código SWIFT — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de Conta Bancária Internacional (IBAN) — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> | Bloquear o acesso ao conteúdo  <br/>  Enviar uma notificação  <br/>  Permitir substituição  <br/>  Exigir justificativa comercial  <br/>  Enviar relatório de incidente  <br/> |
   
## <a name="saudi-arabia-financial-data"></a>Dados Financeiros da Arábia Saudita

|**Nome da regra**|**Condições <br/> (incluindo os tipos de informações confidenciais)**|**Ações**|
|:-----|:-----|:-----|
|Finanças da Arábia Saudita: Examinar o conteúdo compartilhado fora - contagem baixa  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número do Cartão de Crédito — Contagem Mín. 1, Contagem Máx. 9  <br/>  Código SWIFT — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Conta Bancária Internacional (IBAN) — Contagem Mín. 1, Contagem Máx. 9  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> |Enviar uma notificação  <br/> |
|Finanças da Arábia Saudita: Examinar o conteúdo compartilhado fora - contagem alta  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número do Cartão de Crédito — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Código SWIFT — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de Conta Bancária Internacional (IBAN) — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> | Bloquear o acesso ao conteúdo  <br/>  Enviar uma notificação  <br/>  Permitir substituição  <br/>  Exigir justificativa comercial  <br/>  Enviar relatório de incidente  <br/> |
   
## <a name="saudi-arabia-personally-identifiable-information-pii-data"></a>Dados de Informações Identificáveis Pessoalmente (PII) da Arábia Saudita

|**Nome da regra**|**Condições <br/> (incluindo os tipos de informações confidenciais)**|**Ações**|
|:-----|:-----|:-----|
|PII da Arábia Saudita: Examinar o conteúdo compartilhado fora - contagem baixa  <br/> | Conteúdo tem informações confidenciais:  <br/>  ID Nacional da Arábia Saudita — Contagem Mín. 1, Contagem Máx. 9  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> |Enviar uma notificação  <br/> |
|PII da Arábia Saudita: Examinar o conteúdo compartilhado fora - contagem alta  <br/> | Conteúdo tem informações confidenciais:  <br/>  ID Nacional da Arábia Saudita — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> | Bloquear o acesso ao conteúdo  <br/>  Enviar uma notificação  <br/>  Permitir substituição  <br/>  Exigir justificativa comercial  <br/>  Enviar relatório de incidente  <br/> |
   
## <a name="uk-access-to-medical-reports-act"></a>Ato de Acesso a Prontuários Médicos do Reino Unido

|**Nome da regra**|**Condições <br/> (incluindo os tipos de informações confidenciais)**|**Ações**|
|:-----|:-----|:-----|
|AMRA do Reino Unido: Examinar o conteúdo compartilhado fora - contagem baixa  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de Serviço de Saúde Nacional do Reino Unido — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Seguro Nacional do Reino Unido (NINO) — Contagem Mín. 1, Contagem Máx. 9  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> |Enviar uma notificação  <br/> |
|AMRA do Reino Unido: Examinar o conteúdo compartilhado fora - contagem alta  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de Serviço de Saúde Nacional do Reino Unido — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de Seguro Nacional do Reino Unido (NINO) — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> | Bloquear o acesso ao conteúdo  <br/>  Enviar uma notificação  <br/>  Permitir substituição  <br/>  Exigir justificativa comercial  <br/>  Enviar relatório de incidente  <br/> |
   
## <a name="uk-data-protection-act"></a>Ato de Proteção de Dados do Reino Unido

|**Nome da regra**|**Condições <br/> (incluindo os tipos de informações confidenciais)**|**Ações**|
|:-----|:-----|:-----|
|DPA do Reino Unido: Examinar o conteúdo compartilhado fora - contagem baixa  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de Seguro Nacional do Reino Unido (NINO) — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número do Passaporte EUA/Reino Unido — Contagem Mín. 1, Contagem Máx. 9  <br/>  Código SWIFT — Contagem Mín. 1, Contagem Máx. 9  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> |Enviar uma notificação  <br/> |
|DPA do Reino Unido: Examinar o conteúdo compartilhado fora - contagem alta  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de Seguro Nacional do Reino Unido (NINO) — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número do Passaporte EUA/Reino Unido — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Código SWIFT — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> | Bloquear o acesso ao conteúdo  <br/>  Enviar uma notificação  <br/>  Permitir substituição  <br/>  Exigir justificativa comercial  <br/>  Enviar relatório de incidente  <br/> |
   
## <a name="uk-financial-data"></a>Dados Financeiros do Reino Unido

|**Nome da regra**|**Condições <br/> (incluindo os tipos de informações confidenciais)**|**Ações**|
|:-----|:-----|:-----|
|Finanças do Reino Unido: Examinar o conteúdo compartilhado fora - contagem baixa  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número do Cartão de Crédito — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Cartão de Débito da UE — Contagem Mín. 1, Contagem Máx. 9  <br/>  Código SWIFT — Contagem Mín. 1, Contagem Máx. 9  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> |Enviar uma notificação  <br/> |
|Finanças do Reino Unido: Examinar o conteúdo compartilhado fora - contagem alta  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número do Cartão de Crédito — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de Cartão de Débito da UE — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Código SWIFT — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> | Bloquear o acesso ao conteúdo  <br/>  Enviar uma notificação  <br/>  Permitir substituição  <br/>  Exigir justificativa comercial  <br/>  Enviar relatório de incidente  <br/> |
   
## <a name="uk-personal-information-online-code-of-practice-piocp"></a>Código de Prática Online de Informações Pessoais (PIOCP) do Reino Unido

|**Nome da regra**|**Condições <br/> (incluindo os tipos de informações confidenciais)**|**Ações**|
|:-----|:-----|:-----|
|PIOCP do Reino Unido: Examinar o conteúdo compartilhado fora - contagem baixa  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de Seguro Nacional do Reino Unido (NINO) — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Serviço de Saúde Nacional do Reino Unido — Contagem Mín. 1, Contagem Máx. 9  <br/>  Código SWIFT — Contagem Mín. 1, Contagem Máx. 9  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> |Enviar uma notificação  <br/> |
|PIOCP do Reino Unido: Examinar o conteúdo compartilhado fora - contagem alta  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de Seguro Nacional do Reino Unido (NINO) — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de Serviço de Saúde Nacional do Reino Unido — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Código SWIFT — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> | Bloquear o acesso ao conteúdo  <br/>  Enviar uma notificação  <br/>  Permitir substituição  <br/>  Exigir justificativa comercial  <br/>  Enviar relatório de incidente  <br/> |
   
## <a name="uk-personally-identifiable-information-pii-data"></a>Dados de Informações Identificáveis Pessoalmente (PII) do Reino Unido

|**Nome da regra**|**Condições <br/> (incluindo os tipos de informações confidenciais)**|**Ações**|
|:-----|:-----|:-----|
|PII do Reino Unido: Examinar o conteúdo compartilhado fora - contagem baixa  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de Seguro Nacional do Reino Unido (NINO) — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número do Passaporte EUA/Reino Unido — Contagem Mín. 1, Contagem Máx. 9  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> |Enviar uma notificação  <br/> |
|PII do Reino Unido: Examinar o conteúdo compartilhado fora - contagem alta  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de Seguro Nacional do Reino Unido (NINO) — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número do Passaporte EUA/Reino Unido — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> | Bloquear o acesso ao conteúdo  <br/>  Enviar uma notificação  <br/>  Permitir substituição  <br/>  Exigir justificativa comercial  <br/>  Enviar relatório de incidente  <br/> |
   
## <a name="uk-privacy-and-electronic-communications-regulations"></a>Regulamentações de Comunicações Eletrônicas e Privacidade do Reino Unido

|**Nome da regra**|**Condições <br/> (incluindo os tipos de informações confidenciais)**|**Ações**|
|:-----|:-----|:-----|
|PECR do Reino Unido: Examinar o conteúdo compartilhado fora - contagem baixa  <br/> | Conteúdo tem informações confidenciais:  <br/>  Código SWIFT — Contagem Mín. 1, Contagem Máx. 9  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> |Enviar uma notificação  <br/> |
|PECR do Reino Unido: Examinar o conteúdo compartilhado fora - contagem alta  <br/> | Conteúdo tem informações confidenciais:  <br/>  Código SWIFT — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> | Bloquear o acesso ao conteúdo  <br/>  Enviar uma notificação  <br/>  Permitir substituição  <br/>  Exigir justificativa comercial  <br/>  Enviar relatório de incidente  <br/> |
   
## <a name="us-federal-trade-commission-ftc-consumer-rules"></a>Regras para Consumidores da Comissão Comercial Federal (FTC) dos EUA

|**Nome da regra**|**Condições <br/> (incluindo os tipos de informações confidenciais)**|**Ações**|
|:-----|:-----|:-----|
|Regras da FTC dos EUA: Examinar o conteúdo compartilhado fora - contagem baixa  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número do Cartão de Crédito — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Conta Bancária dos EUA — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Roteamento ABA — Contagem Mín. 1, Contagem Máx. 9  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> |Enviar uma notificação  <br/> |
|Regras da FTC dos EUA: Examinar o conteúdo compartilhado fora - contagem alta  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número do Cartão de Crédito — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de conta bancária dos EUA — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de Roteamento ABA — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> | Bloquear o acesso ao conteúdo  <br/>  Enviar uma notificação  <br/>  Permitir substituição  <br/>  Exigir justificativa comercial  <br/>  Enviar relatório de incidente  <br/> |
   
## <a name="us-financial-data"></a>Finanças dos Estados Unidos

|**Nome da regra**|**Condições <br/> (incluindo os tipos de informações confidenciais)**|**Ações**|
|:-----|:-----|:-----|
|Finanças dos Estados Unidos: Examinar o conteúdo compartilhado fora - contagem baixa  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número do Cartão de Crédito — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Conta Bancária dos EUA — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Roteamento ABA — Contagem Mín. 1, Contagem Máx. 9  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> |Enviar uma notificação  <br/> |
|Finanças dos Estados Unidos: Examinar o conteúdo compartilhado fora - contagem alta  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número do Cartão de Crédito — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de conta bancária dos EUA — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de Roteamento ABA — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> | Bloquear o acesso ao conteúdo  <br/>  Enviar uma notificação  <br/>  Permitir substituição  <br/>  Exigir justificativa comercial  <br/>  Enviar relatório de incidente  <br/> |
   
## <a name="us-gramm-leach-bliley-act-glba"></a>Ato Gramm-Leach-Bliley (GLBA) dos EUA

|**Nome da regra**|**Condições <br/> (incluindo os tipos de informações confidenciais)**|**Ações**|
|:-----|:-----|:-----|
|GLBA dos EUA: Examinar o conteúdo compartilhado fora - contagem baixa  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número do Cartão de Crédito — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Conta Bancária dos EUA — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Identificação de Contribuinte Individual (ITIN) dos EUA — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Inscrição na Previdência Social (SSN) dos EUA — Contagem Mín. 1, Contagem Máx. 9  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> |Enviar uma notificação  <br/> |
|GLBA dos EUA: Examinar o conteúdo compartilhado fora - contagem alta  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número do Cartão de Crédito — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de conta bancária dos EUA — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de Identificação de Contribuinte Individual (ITIN) dos EUA — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de Inscrição na Previdência Social (SSN) dos EUA — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> | Bloquear o acesso ao conteúdo  <br/>  Enviar uma notificação  <br/>  Permitir substituição  <br/>  Exigir justificativa comercial  <br/>  Enviar relatório de incidente  <br/> |
   
## <a name="us-health-insurance-act-hipaa"></a>Ato do Seguro de Saúde (HIPAA) dos EUA

|**Nome da regra**|**Condições <br/> (incluindo os tipos de informações confidenciais)**|**Ações**|
|:-----|:-----|:-----|
|Conteúdo corresponde HIPAA dos EUA  <br/> | Contém qualquer uma das seguintes informações confidenciais:  <br/>  Número de Seguridade Social da US (SSN) — Min contagem 1, Max contar qualquer um  <br/>  Número da Drug Enforcement Agency (DEA) — Min contagem 1, Max contar qualquer um  <br/> **E** <br/>  Conteúdo contém qualquer um desses termos:  <br/>  Classificação de internacional de doenças (ICD-9-CM) — Min contagem 1, Max contar qualquer um  <br/>  Classificação de internacional de doenças (ICD-10-CM) — Min contagem 1, Max contar qualquer um  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> |Enviar uma notificação  <br/> |
   
## <a name="us-patriot-act"></a>Lei Patriota dos EUA

|**Nome da regra**|**Condições <br/> (incluindo os tipos de informações confidenciais)**|**Ações**|
|:-----|:-----|:-----|
|Lei Patriota dos EUA: Examinar o conteúdo compartilhado fora - contagem baixa  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número do Cartão de Crédito — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Conta Bancária dos EUA — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Identificação de Contribuinte Individual (ITIN) dos EUA — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Inscrição na Previdência Social (SSN) dos EUA — Contagem Mín. 1, Contagem Máx. 9  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> |Enviar uma notificação  <br/> |
|Lei Patriota dos EUA: Examinar o conteúdo compartilhado fora - contagem alta  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número do Cartão de Crédito — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de conta bancária dos EUA — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de Identificação de Contribuinte Individual (ITIN) dos EUA — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de Inscrição na Previdência Social (SSN) dos EUA — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> | Bloquear o acesso ao conteúdo  <br/>  Enviar uma notificação  <br/>  Permitir substituição  <br/>  Exigir justificativa comercial  <br/>  Enviar relatório de incidente  <br/> |
   
## <a name="us-personally-identifiable-information-pii-data"></a>Dados de Informações Identificáveis Pessoalmente (PII) dos EUA

|**Nome da regra**|**Condições <br/> (incluindo os tipos de informações confidenciais)**|**Ações**|
|:-----|:-----|:-----|
|PII dos EUA: Examinar o conteúdo compartilhado fora - contagem baixa  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de Identificação de Contribuinte Individual (ITIN) dos EUA — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Inscrição na Previdência Social (SSN) dos EUA — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número do Passaporte EUA/Reino Unido — Contagem Mín. 1, Contagem Máx. 9  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> |Enviar uma notificação  <br/> |
|PII dos EUA: Examinar o conteúdo compartilhado fora - contagem alta  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de Identificação de Contribuinte Individual (ITIN) dos EUA — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de Inscrição na Previdência Social (SSN) dos EUA — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número do Passaporte EUA/Reino Unido — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> | Bloquear o acesso ao conteúdo  <br/>  Enviar uma notificação  <br/>  Permitir substituição  <br/>  Exigir justificativa comercial  <br/>  Enviar relatório de incidente  <br/> |
   
## <a name="us-state-breach-notification-laws"></a>Leis de Notificação de Ruptura de Estado dos EUA

|**Nome da regra**|**Condições <br/> (incluindo os tipos de informações confidenciais)**|**Ações**|
|:-----|:-----|:-----|
|Violação do Estado Americano: Examinar o conteúdo compartilhado fora - contagem baixa  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número do Cartão de Crédito — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Conta Bancária dos EUA — Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de carteira de motorista dos EUA – Contagem Mín. 1, Contagem Máx. 9  <br/>  Número de Inscrição na Previdência Social (SSN) dos EUA — Contagem Mín. 1, Contagem Máx. 9  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> |Enviar uma notificação  <br/> |
|Violação do Estado Americano: Examinar o conteúdo compartilhado fora - contagem alta  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número do Cartão de Crédito — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de conta bancária dos EUA — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de carteira de motorista dos EUA – Contagem Mín. 10, Contagem Máx. qualquer  <br/>  Número de Inscrição na Previdência Social (SSN) dos EUA — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> | Bloquear o acesso ao conteúdo  <br/>  Enviar uma notificação  <br/>  Permitir substituição  <br/>  Exigir justificativa comercial  <br/>  Enviar relatório de incidente  <br/> |
   
## <a name="us-state-social-security-number-confidentiality-laws"></a>Leis de Confidencialidade de Número de Seguro Social de Estado dos EUA

|**Nome da regra**|**Condições <br/> (incluindo os tipos de informações confidenciais)**|**Ações**|
|:-----|:-----|:-----|
|Leis de NSS dos EUA: Examinar o conteúdo compartilhado fora - contagem baixa  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de Inscrição na Previdência Social (SSN) dos EUA — Contagem Mín. 1, Contagem Máx. 9  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> |Enviar uma notificação  <br/> |
|Leis de NSS dos EUA: Examinar o conteúdo compartilhado fora - contagem alta  <br/> | Conteúdo tem informações confidenciais:  <br/>  Número de Inscrição na Previdência Social (SSN) dos EUA — Contagem Mín. 10, Contagem Máx. qualquer  <br/>  O conteúdo é compartilhado com:  <br/>  Pessoas de fora da minha organização  <br/> | Bloquear o acesso ao conteúdo  <br/>  Enviar uma notificação  <br/>  Permitir substituição  <br/>  Exigir justificativa comercial  <br/>  Enviar relatório de incidente  <br/> |
   


---
title: Relatórios e rastreamento de mensagem no Exchange Online Protection
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: 12/18/2017
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: f40253f2-50a1-426e-9979-be74ba74cb61
description: O Microsoft Proteção do Exchange Online (EOP) oferece muitos relatórios diferentes que podem ajudá-lo a determinar o status e a integridade gerais de sua organização. Existem também ferramentas que ajudam você a solucionar problemas com eventos específicos (tais como uma mensagem que não chega aos destinatários pretendidos), e relatórios de auditoria para ajudar nos requisitos de conformidade. A tabela a seguir descreve os relatórios e as ferramentas de solução de problemas disponíveis para o administradores de EOP.
ms.openlocfilehash: 0dcacec586408bf98ad4c67c11ae3bde3a8e9315
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34154613"
---
# <a name="reporting-and-message-trace-in-exchange-online-protection"></a>Relatórios e rastreamento de mensagem no Exchange Online Protection

O Microsoft Proteção do Exchange Online (EOP) oferece muitos relatórios diferentes que podem ajudá-lo a determinar o status e a integridade gerais de sua organização. Existem também ferramentas que ajudam você a solucionar problemas com eventos específicos (tais como uma mensagem que não chega aos destinatários pretendidos), e relatórios de auditoria para ajudar nos requisitos de conformidade. 

## <a name="usage-reports"></a>Relatórios de uso

**Grupos do Office 365atividade** Exibir informações sobre a quantidade de Grupos do Office 365 que são criados e usados.  

**Atividade de email** Exibir informações sobre o número de mensagens enviadas, recebidas e lidas em toda sua organização e por usuários específicos.  

**Uso do aplicativo de email** Exibir informações sobre os aplicativos de email usados. Isso inclui o número total de conexões para cada aplicativo, e as versões do Outlook que estão se conectando.  

**Uso de caixa de correio** Exibir informações sobre o armazenamento usado, consumo de cota, contagem de itens e última atividade (atividade de leitura ou envio) para caixas de correio.

Confira os recursos a seguir para obter mais informações:

- [Relatórios do Office 365 no centro de administração-grupos do Office 365](https://go.microsoft.com/fwlink/p/?linkid=861610) 
- [Relatórios do Office 365 no Centro de administrador - Atividade de email](https://go.microsoft.com/fwlink/p/?linkid=859706) 
- [Relatórios do Office 365 no Centro de administrador - Uso do aplicativo de email](https://go.microsoft.com/fwlink/p/?linkid=859707)
- [Relatórios do Office 365 no Centro de administrador - Uso de caixa de correio](https://go.microsoft.com/fwlink/p/?linkid=859708)

## <a name="security-amp-compliance-reports-in-the-microsoft-365-admin-center"></a>Relatórios &amp; de conformidade de segurança no centro de administração do Microsoft 365

Esses relatórios aprimorados fornecem uma experiência de relatório interativa para administradores do EOP, que inclui informações de resumo e a capacidade de aprofundar para obter mais detalhes.  

**Proteção avançada contra ameaças (ATP)** Exibir informações sobre links e anexos seguros que fazem parte da ATP.  

**EOP** Exibir informações sobre detecções de malware, email falsificado, detecções de spam e fluxo de emails de e para sua organização.  

[Exibir relatórios para proteção avançada contra ameaças e proteção do Exchange Online](https://go.microsoft.com/fwlink/p/?linkid=852409) 

##<a name="custom-reports-using-microsoft-graph"></a>Relatórios personalizados usando o Microsoft Graph

Criar programaticamente relatórios disponíveis no centro de administração do Microsoft 365 usando o Microsoft Graph Confira os subtópicos sobre [como trabalhar com os relatórios de uso do Office 365 no Microsoft Graph](https://go.microsoft.com/fwlink/p/?linkid=865135) 

##<a name="custom-reports-using-reporting-web-services"></a>Relatórios personalizados usando serviços Web de relatório

Criar programaticamente relatórios dos cmdlets disponíveis de relatórios do PowerShell do Exchange Online Protection usando a filtragem de consulta REST/ODATA2.

Confira [Serviços Web de relatório do Office 365](https://go.microsoft.com/fwlink/p/?LinkId=279926) 

##<a name="message-trace"></a>Rastreamento de mensagens

Acompanhe as mensagens enviadas conforme elas circulam através di EOP. Você pode determinar se uma mensagem de email foi recebida, rejeitada, adiada ou entregue pelo serviço. Também mostra as ações feitas na mensagem antes de ela chegar em seu status final.  

Você pode usar essa informação para responder com eficiência às perguntas dos seus usuários, solucionar problemas de fluxo de email, validar alterações de política e reduzir a necessidade de contatar o suporte técnico para obter assistência.  

Consulte [rastrear uma mensagem de email](http://technet.microsoft.com/library/0c83cde6-5b09-4106-8587-c200cdc59094.aspx) 

## <a name="audit-logging"></a>Registro em log de auditoria

Rastreie alterações específica feitas pelos administradores na sua organização. Estes relatórios ajudam você a solucionar problemas de configuração ou a encontrar a causa de problemas relacionados à conformidade ou à segurança.  Ver [relatórios de auditoria no EOP](auditing-reports-in-eop.md) 


## <a name="reporting-and-message-trace-data-availability-and-latency"></a>Disponibilidade e latência de dados de relatórios e rastreamento de mensagens

A tabela a seguir descreve quando dados de relatórios e rastreamento de mensagens do EOP estão disponíveis e por quanto tempo.
  
||||
|:-----|:-----|:-----|
|**Tipo de relatório** <br/> |**Dados disponíveis por (período retrospectivo)** <br/> |**Latência** <br/> |
|Relatórios de Resumo de proteção de email  <br/> |90 dias  <br/> |A agregação de dados de mensagens geralmente é concluída em 24 a 48 horas. Algumas pequenas alterações agregadas progressivas podem ocorrer por até 5 dias.  <br/> |
|Relatórios de detalhes de proteção de email  <br/> |90 dias  <br/> |Para obter dados detalhados de um período menor que 7 dias, os dados deverão aparecer no prazo de 24 horas, mas a operação talvez não seja concluída em até 48 horas. Algumas pequenas alterações incrementais podem ocorrer por até 5 dias.  <br/> Para exibir relatórios detalhados de mensagens ocorridas em um período superior a sete dias, os resultados podem demorar umas poucas horas.  <br/> |
|Dados de rastreamento de mensagem  <br/> |90 dias  <br/> |Ao rastrear mensagens ocorridas em um período menor que 7 dias, as mensagens devem aparecer no intervalo de 5 a 30 minutos.  <br/> Ao rastrear mensagens ocorridas em um período superior a 7 dias, os resultados podem demorar umas poucas horas.  <br/> |
   
> [!NOTE]
> A disponibilidade e a latência dos dados é a mesma, seja ela solicitada por meio do centro de administração do Microsoft 365 ou do PowerShell remoto. 
  


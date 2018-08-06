---
title: Relatórios e rastreamento de mensagem no Exchange Online Protection
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: 12/18/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: f40253f2-50a1-426e-9979-be74ba74cb61
description: O Microsoft Proteção do Exchange Online (EOP) oferece muitos relatórios diferentes que podem ajudá-lo a determinar o status e a integridade gerais de sua organização. Existem também ferramentas que ajudam você a solucionar problemas com eventos específicos (tais como uma mensagem que não chega aos destinatários pretendidos), e relatórios de auditoria para ajudar nos requisitos de conformidade. A tabela a seguir descreve os relatórios e as ferramentas de solução de problemas disponíveis para o administradores de EOP.
ms.openlocfilehash: 01a09b2b4b72161352af3793686c6cc888e44e29
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027138"
---
# <a name="reporting-and-message-trace-in-exchange-online-protection"></a>Relatórios e rastreamento de mensagem no Exchange Online Protection

Microsoft Exchange Online Protection (EOP) oferece vários relatórios diferentes que podem ajudá-lo a determinam o status geral e a integridade da sua organização. Há também ferramentas para ajudá-lo a solucionar problemas de eventos específicos (por exemplo, uma mensagem que chegam não para seus destinatários pretendidos) e relatórios de auditoria para auxiliar com os requisitos de conformidade. 

## <a name="usage-reports"></a>Relatórios de uso

**Grupos do Office 365atividade** Exibir informações sobre a quantidade de Grupos do Office 365 que são criados e usados.  

**Atividade de email** Exibir informações sobre o número de mensagens enviadas, recebidas e lidas em toda sua organização e por usuários específicos.  

**Uso do aplicativo de email** Exibir informações sobre os aplicativos de email que são usados. Isso inclui o número total de conexões para cada aplicativo e as versões do Outlook que estão se conectando.  

**Uso de caixa de correio** Exibir informações sobre o armazenamento usado, consumo de cota, contagem de itens e última atividade (atividade de leitura ou envio) para caixas de correio.

Consulte os seguintes recursos para obter mais informações:

- [Relatórios do Office 365 no Centro de administração - grupos do Office 365](https://go.microsoft.com/fwlink/p/?linkid=861610) 
- [Relatórios do Office 365 no Centro de administrador - Atividade de email](https://go.microsoft.com/fwlink/p/?linkid=859706) 
- [Relatórios do Office 365 no Centro de administrador - Uso do aplicativo de email](https://go.microsoft.com/fwlink/p/?linkid=859707)
- [Relatórios do Office 365 no Centro de administrador - Uso de caixa de correio](https://go.microsoft.com/fwlink/p/?linkid=859708)

## <a name="security-amp-compliance-reports-in-the-office-365-admin-center"></a>Segurança &amp; relatórios de conformidade no Centro de administração do Office 365

Esses relatórios aprimorados fornecem uma experiência interativa de relatórios para os administradores do EOP, que inclui informações de resumo e a capacidade de fazer uma busca detalhada para obter mais detalhes.  

**Proteção avançada contra ameaças (ATP)** Exibir informações sobre links e anexos seguros que fazem parte da ATP.  

**EOP** Exibir informações sobre detecções de malware, mensagens falsificadas, detecções de spam e fluxo de emails de e para sua organização.  

[Exibir relatórios de proteção de ameaça avançadas e Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkid=852409) 

##<a name="custom-reports-using-microsoft-graph"></a>Relatórios personalizados usando o Microsoft Graph

Criar relatórios que estão disponíveis no Centro de administração do Office 365 usando o Microsoft Graph ver programaticamente os subtópicos de [trabalhar com relatórios de uso do Office 365 no Microsoft Graph](https://go.microsoft.com/fwlink/p/?linkid=865135) 

##<a name="custom-reports-using-reporting-web-services"></a>Relatórios personalizados usando serviços Web de relatório

Crie relatórios de maneira programática disponível PowerShell do Exchange Online Protection cmdlets de relatório usando a filtragem de consulta do REST/ODATA2.

Consulte o [Office 365 Reporting Web Services](https://go.microsoft.com/fwlink/p/?LinkId=279926) 

##<a name="message-trace"></a>Rastreamento de mensagens

Mensagens de email são conforme elas viajam através do EOP. Você pode determinar se uma mensagem de email foi recebida, rejeitada, adiada ou entregue pelo serviço. Ele também mostra quais ações foram realizadas na mensagem antes de que atingiu seu status final.  

Você pode usar essa informação para responder com eficiência às perguntas dos seus usuários, solucionar problemas de fluxo de email, validar alterações de política e reduzir a necessidade de contatar o suporte técnico para obter assistência.  

Consulte [rastrear uma mensagem de Email](http://technet.microsoft.com/library/0c83cde6-5b09-4106-8587-c200cdc59094.aspx) 

## <a name="audit-logging"></a>Registro em log de auditoria

Rastreia alterações específicas feitas por administradores para sua organização. Esses relatórios podem ajudar você a solucionar problemas de configuração ou encontrar a causa de problemas relacionados à conformidade ou de segurança.  consulte [relatórios de auditoria no EOP](auditing-reports-in-eop.md) 


## <a name="reporting-and-message-trace-data-availability-and-latency"></a>Disponibilidade e latência de dados de relatórios e rastreamento de mensagens

A tabela a seguir descreve quando dados de relatórios e rastreamento de mensagens do EOP estão disponíveis e por quanto tempo.
  
||||
|:-----|:-----|:-----|
|**Tipo de relatório** <br/> |**Dados disponíveis por (período retrospectivo)** <br/> |**Latência** <br/> |
|Relatórios resumidos de proteção de email  <br/> |90 dias  <br/> |A agregação de dados de mensagens geralmente é concluída em 24 a 48 horas. Algumas pequenas alterações agregadas progressivas podem ocorrer por até 5 dias.  <br/> |
|Relatórios de detalhes de proteção de email  <br/> |90 dias  <br/> |Para obter dados detalhados de um período menor que sete dias, os dados deverão aparecer no prazo de 24 horas, mas a operação talvez não seja concluída em até 48 horas. Algumas pequenas alterações incrementais podem ocorrer por até cinco dias.  <br/> Para exibir relatórios detalhados de mensagens ocorridas em um período superior a sete dias, os resultados podem demorar umas poucas horas.  <br/> |
|Dados de rastreamento de mensagem  <br/> |90 dias  <br/> |Ao rastrear mensagens ocorridas em um período menor que 7 dias, as mensagens devem aparecer no intervalo de 5 a 30 minutos.  <br/> Ao rastrear mensagens ocorridas em um período superior a 7 dias, os resultados podem demorar umas poucas horas.  <br/> |
   
> [!NOTE]
> A disponibilidade e a latência de dados são as mesmas, sejam elas solicitadas por meio do Centro de administração do Office 365 ou pelo PowerShell remoto. 
  


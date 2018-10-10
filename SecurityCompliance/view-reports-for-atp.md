---
title: Exibir relatórios de proteção de ameaça avançadas do Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e47e838c-d99e-4c0b-b9aa-e66c4fae902f
description: Saiba como encontrar e usar os relatórios para o Office 365 avançadas Threat Protection na segurança &amp; Centro de conformidade.
ms.openlocfilehash: 4a76c6a5b888142dc4c35af432fa61916145d648
ms.sourcegitcommit: 099bbfb1d16b251fd5cf18ec6515faaf9a989176
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25454298"
---
# <a name="view-reports-for-office-365-advanced-threat-protection"></a>Exibir relatórios de proteção de ameaça avançadas do Office 365

Se sua organização tem [A proteção de ameaça avançadas do Office 365](office-365-atp.md) (ATP) e você tem as [permissões necessárias](#what-permissions-are-needed-to-view-these-reports), você pode usar vários relatórios ATP na segurança &amp; Centro de conformidade. (Vá para **relatórios** \> **Dashboard**.)
  
![A segurança &amp; painel do Centro de conformidade pode ajudá-lo a ver onde a proteção de ameaça Avançado está funcionando](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)
  
Relatórios de ATP incluem o [relatório de status de proteção contra ameaças](#threat-protection-status-report), o [relatório de tipos de arquivo ATP](#atp-file-types-report)e o [relatório de disposição de mensagem ATP](#atp-message-disposition-report). Este artigo descreve os relatórios de ATP e inclui links para [Exibir os relatórios adicionais](#additional-reports-to-view).
  
## <a name="threat-protection-status-report"></a>Relatório de status de proteção de ameaça

O relatório de **status de proteção de ameaça** é um modo de exibição único que reúne informações sobre email mal-intencionado do conteúdo e mal-intencionados detectadas e bloqueadas pelo Exchange Online e proteção avançada de ameaça. O relatório fornece uma contagem agregada exclusivo de mensagens de email com conteúdo mal-intencionado (arquivos ou URLs) bloqueadas pelo mecanismo antimalware, [zero horas automático Limpar (ZAP)](zero-hour-auto-purge.md)e recursos de proteção de ameaça avançadas, como [Links de seguros ATP](atp-safe-links.md), [ATP Anexos seguros](atp-safe-attachments.md)e [os recursos de AntiPhishing ATP no Office 365](atp-anti-phishing.md).
  
Para exibir o relatório de status de proteção de ameaça, na segurança &amp; Centro de conformidade, vá para **relatórios** \> **painel** \> **o status de proteção de ameaça**.
  
![Relatório de Status de proteção de ameaça ATP](media/6bdd41eb-62e0-423b-9fd4-d1d5baf0cbd5.png)
  
Para obter o status detalhado para um dia, passe o mouse sobre o gráfico.
  
![Dados de Status de proteção de ameaça ATP para um dia](media/d5c2c6ad-c002-4985-a032-c866e46fdea8.png)
  
Por padrão, o relatório de status de proteção de ameaça mostra dados para os últimos sete dias. No entanto, você pode escolher **filtros** e alterar o intervalo de datas para exibir dados por até 90 dias. 
  
![Filtros do Status de proteção de ameaça ATP](media/4f703369-642b-402b-9758-b9c828283410.png)
  
Você também pode usar o menu **Exibir dados por** alterar quais informações são exibidas no relatório. 
  
![Opções de visualização para o relatório de Status de proteção de ameaça ATP](media/4959bf8c-d192-4542-b00b-184e101e7513.png)
  
## <a name="atp-file-types-report"></a>Relatório de tipos de arquivo ATP

O relatório de **Tipos de arquivo ATP** mostra o tipo de arquivos detectados como mal-intencionado por [ATP anexos de seguros](atp-safe-attachments.md).
  
Para exibir este relatório, na segurança &amp; Centro de conformidade, vá para **relatórios** \> **painel** \> **ATP tipos de arquivo**.
  
![Relatório de tipos de arquivo ATP](media/6e3f5d33-79aa-4b2d-938c-6ef135d9e54c.png)
  
Quando você focaliza em um determinado dia, você pode ver a divisão dos tipos de arquivos mal-intencionado que foram detectados pelo [ATP anexos de seguros](atp-safe-attachments.md) e [antispam &amp; proteção antimalware no Office 365](anti-spam-and-anti-malware-protection.md).
  
![Dados de relatório de tipos de arquivo ATP por um dia](media/10d18428-699a-41d2-a73e-be3a8214ada1.png)
  
## <a name="atp-message-disposition-report"></a>Relatório de disposição de mensagem ATP

O relatório de **Disposição de mensagem ATP** mostra as ações que foram feitas para mensagens de email que foram detectadas como tendo conteúdo mal-intencionado. 
  
Para exibir este relatório, na segurança &amp; Centro de conformidade, vá para **relatórios** \> **painel** \> **ATP disposição de mensagem**.
  
![Relatório de descarte de mensagens de ATP](media/b0ff65c4-53d3-496d-bafa-8937a5eb69e5.png)
  
Quando você focaliza uma barra no gráfico, você pode ver quais ações foram realizadas para email detectado daquele dia.
  
![Dados de relatório de descarte de mensagens ATP para um dia](media/68d2beb8-4b30-48c4-8ba6-5e8ab88ae456.png)
  
## <a name="additional-reports-to-view"></a>Exibir os relatórios adicionais

Além dos relatórios de ATP descritos neste artigo, [os relatórios de segurança de email](view-email-security-reports.md) estão disponíveis na segurança &amp; Centro de conformidade. Relatórios de segurança de email incluem um [relatório de destinatários e remetentes da parte superior](view-email-security-reports.md#top-senders-and-recipients-report), um [relatório de mensagens de falso](view-email-security-reports.md#spoof-mail-report), um [relatório detecções de Spam](view-email-security-reports.md#spam-detections-report)e muito mais.
  
E, se sua organização tiver [Inteligência de ameaça do Office 365](office-365-ti.md), você também pode [uso Explorer na segurança &amp; Centro de conformidade](use-explorer-in-security-and-compliance.md).
  
## <a name="what-permissions-are-needed-to-view-the-atp-reports"></a>Quais permissões são necessárias para exibir os relatórios de ATP?

Para exibir e usar os relatórios descritos neste artigo, você deve ter uma função apropriada atribuída na segurança &amp; Centro de conformidade e no Centro de administração do Exchange.
  
|**Default management role assignments for this role**|**Onde atribuído**|**Saiba mais**|
|:-----|:-----|:-----|
| Uma das seguintes opções:  <br/>  Gerenciamento da Organização  <br/>  Administrador de segurança  <br/>  Leitor de segurança  <br/> |Segurança &amp; Centro de conformidade  <br/> |[Permissões de segurança do Office 365 &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md) <br/> |
| Uma das seguintes opções:  <br/>  Gerenciamento da Organização  <br/>  Gerenciamento da organização somente exibição  <br/>  Função destinatários de somente leitura  <br/>  Gerenciamento de Conformidade  <br/> |Centro de Administração do Exchange  <br/> |[Permissões de recursos no Exchange Online](https://technet.microsoft.com/library/jj200673%28v=exchg.150%29.aspx) <br/> |
   
## <a name="what-if-the-reports-arent-showing-data"></a>Se os relatórios não são mostrando dados?

Se você não estiver vendo dados em seus relatórios, verifique novamente se suas políticas estão configuradas corretamente. Sua organização deve ter [políticas de Links de ATP seguros](set-up-atp-safe-links-policies.md) e [anexos de seguros ATP políticas](set-up-atp-safe-attachments-policies.md) definidas na ordem de proteção de ATP estar em vigor. Consulte também a [proteção antispam e antimalware no Office 365](anti-spam-and-anti-malware-protection.md).
  
## <a name="related-topics"></a>Tópicos relacionados

[Relatórios e ideias de segurança do Office 365 &amp; Centro de conformidade](reports-and-insights-in-security-and-compliance.md)
  
[Para criar um cronograma para um relatório na segurança &amp; Centro de conformidade](create-a-schedule-for-a-report.md)
  
[Configurar e fazer o download de um relatório personalizado na segurança &amp; Centro de conformidade](set-up-and-download-a-custom-report.md)
  


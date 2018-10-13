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
ms.openlocfilehash: 1a0ecb9a6722deb50a491a15f720481a5bb7b0a4
ms.sourcegitcommit: e0c6f99d5514d8da8a70d9bd3616d1a1c0851254
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2018
ms.locfileid: "25552329"
---
# <a name="view-reports-for-office-365-advanced-threat-protection"></a>Exibir relatórios de proteção de ameaça avançadas do Office 365

Se sua organização tem [A proteção de ameaça avançadas do Office 365](office-365-atp.md) (ATP) e você tem as [permissões necessárias](#what-permissions-are-needed-to-view-these-reports), você pode usar vários relatórios ATP na segurança &amp; Centro de conformidade. (Vá para **relatórios** \> **Dashboard**.)
  
![A segurança &amp; painel do Centro de conformidade pode ajudá-lo a ver onde a proteção de ameaça Avançado está funcionando](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)
  
Relatórios de ATP incluem o [relatório de Status de proteção de ameaça](#threat-protection-status-report), o [relatório de tipos de arquivo ATP](#atp-file-types-report)e o [relatório de disposição de mensagem ATP](#atp-message-disposition-report). Este artigo descreve os relatórios de ATP e inclui links para [Exibir os relatórios adicionais](#additional-reports-to-view).
  
## <a name="threat-protection-status-report"></a>Relatório de Status de proteção de ameaça

O relatório de **Status de proteção de ameaça** é um modo de exibição único que reúne informações sobre email mal-intencionado do conteúdo e mal-intencionados detectadas e bloqueadas pelo [Office 365 ATP](office-365-atp.md)e o [Exchange Online Protection](eop/exchange-online-protection-overview.md) (EOP). O relatório fornece uma contagem agregada exclusivo de mensagens de email com conteúdo mal-intencionado (arquivos ou endereços de site (URLs)) bloqueado pelo mecanismo antimalware, [zero horas automático Limpar (ZAP)](zero-hour-auto-purge.md)e recursos de ATP, como [Links de seguros ATP](atp-safe-links.md), [ATP seguros Anexos](atp-safe-attachments.md)e [os recursos de AntiPhishing ATP](atp-anti-phishing.md).

> [!NOTE]
> Um relatório de Status de proteção de ameaça está disponível para clientes que possuem [ATP do Office 365](office-365-atp.md) ou [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EOP); No entanto, as informações exibidas no relatório de Status de proteção de ameaça para clientes ATP provavelmente irá conter dados diferentes de quais clientes EOP podem ver. Por exemplo, o relatório de Status de proteção de ameaça para clientes ATP irá conter informações sobre [arquivos mal-intencionados detectada no SharePoint Online, OneDrive ou equipes da Microsoft](atp-for-spo-odb-and-teams.md). Tais informações serão específicas para ATP, portanto, os clientes que tenham o EOP, mas não ATP não verá os detalhes em seu relatório de Status de proteção de ameaça.
  
Para exibir o relatório de Status de proteção de ameaça, na segurança &amp; Centro de conformidade, vá para **relatórios** \> **painel** \> **O Status de proteção de ameaça**.
  
![Relatório de Status de proteção de ameaça ATP](media/6bdd41eb-62e0-423b-9fd4-d1d5baf0cbd5.png)
  
Para obter o status detalhado para um dia, passe o mouse sobre o gráfico.
  
![Dados de Status de proteção de ameaça ATP para um dia](media/d5c2c6ad-c002-4985-a032-c866e46fdea8.png)
  
Por padrão, o relatório de Status de proteção de ameaça mostra dados para os últimos sete dias. No entanto, você pode escolher **filtros** e alterar o intervalo de datas para exibir dados por até 90 dias. 
  
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

Além dos relatórios de ATP descritos neste artigo, vários outros relatórios estão disponíveis, conforme descrito na tabela a seguir:


|Tipo de relatório  |Saiba mais  |
|---------|---------|
|**Relatórios de segurança de email**, como uma parte superior de remetentes e destinatários relatório, um relatório de falsificação de email e um relatório detecções de Spam. | [Exibir relatórios de segurança de email na segurança &amp; Centro de conformidade](view-email-security-reports.md)        |
|**Explorer** (também conhecido como ameaça Explorer, isso é incluído no [Office 365 Threat Intelligence](office-365-ti.md))     | [Use o Explorer na segurança &amp; Centro de conformidade](use-explorer-in-security-and-compliance.md)        |
|**Resultados do EOP e ATP** (Isto é um relatório personalizado que você gera usando o PowerShell). Este relatório contém informações, como o domínio, data, tipo de evento, direção, ação e contagem de mensagem.  | [Referência do cmdlet Get-MailTrafficATPReport](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/get-mailtrafficatpreport?view=exchange-ps) |
|**Detecções de EOP e ATP** (Isto é um relatório personalizado que você gera usando o PowerShell). Este relatório contém detalhes sobre arquivos mal-intencionados ou URLs, tentativas de phishing, representação e outras possíveis ameaças em arquivos ou email.   | [Referência do cmdlet Get-MailDetailATPReport](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/get-maildetailatpreport?view=exchange-ps)        |

  
## <a name="what-permissions-are-needed-to-view-the-atp-reports"></a>Quais permissões são necessárias para exibir os relatórios de ATP?

Para exibir e usar os relatórios descritos neste artigo, você deve ter uma função apropriada atribuída na segurança &amp; Centro de conformidade e no Centro de administração do Exchange.
  
|**Default management role assignments for this role**|**Onde atribuído**|**Saiba mais**|
|:-----|:-----|:-----|
| Uma das seguintes opções:  <br/><br/>– Organization Management  <br/>– Administrador segurança  <br/>– Leitor de segurança  <br/> |Segurança &amp; Centro de conformidade  <br/> |[Permissões de segurança do Office 365 &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md) <br/> |
| Uma das seguintes opções:  <br/><br/>– Organization Management  <br/>– Gerenciamento da organização somente leitura  <br/>– Função destinatários somente para exibição  <br/>– Gerenciamento de conformidade do  <br/> |Centro de Administração do Exchange  <br/> |[Permissões de recursos no Exchange Online](https://technet.microsoft.com/library/jj200673%28v=exchg.150%29.aspx) <br/> |
   
## <a name="what-if-the-reports-arent-showing-data"></a>Se os relatórios não são mostrando dados?

Se você não está vendo dados em seus relatórios ATP, confira a suas políticas estão configuradas corretamente. Sua organização deve ter [políticas de Links de ATP seguros](set-up-atp-safe-links-policies.md) e [anexos de seguros ATP políticas](set-up-atp-safe-attachments-policies.md) definidas na ordem de proteção de ATP estar em vigor. Consulte também a [proteção antispam e antimalware no Office 365](anti-spam-and-anti-malware-protection.md).
  
## <a name="related-topics"></a>Tópicos relacionados

[Relatórios e ideias de segurança do Office 365 &amp; Centro de conformidade](reports-and-insights-in-security-and-compliance.md)
  
[Para criar um cronograma para um relatório na segurança &amp; Centro de conformidade](create-a-schedule-for-a-report.md)
  
[Configurar e fazer o download de um relatório personalizado na segurança &amp; Centro de conformidade](set-up-and-download-a-custom-report.md)
  


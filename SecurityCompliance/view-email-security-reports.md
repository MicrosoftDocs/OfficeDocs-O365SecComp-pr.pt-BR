---
title: Exibir relatórios de segurança de email na segurança &amp; Centro de conformidade
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/07/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 3a137e28-1174-42d5-99af-f18868b43e86
ms.collection: M365-security-compliance
description: Saiba como encontrar e usar os relatórios de segurança de email para sua organização com o Office 365 Enterprise. Relatórios de segurança de email estão disponíveis na segurança &amp; Centro de conformidade.
ms.openlocfilehash: 0c9b4c4c75f1e2996217bea600b9d36145b30339
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995292"
---
# <a name="view-email-security-reports-in-the-security-amp-compliance-center"></a>Exibir relatórios de segurança de email na segurança &amp; Centro de conformidade

Uma variedade de relatórios de segurança de email estão disponíveis no [segurança &amp; Centro de conformidade](https://security.microsoft.com) para ajudá-lo a ver como os recursos antispam e antimalware no Office 365 proteção de sua organização. Se você tem as [permissões necessárias](#what-permissions-are-needed-to-view-these-reports), você pode exibir esses relatórios na segurança &amp; Centro de conformidade indo para **relatórios** \> **painel**.
  
![A segurança &amp; painel do Centro de conformidade pode ajudá-lo a ver onde a proteção de ameaça Avançado está funcionando](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)
  
Os relatórios de segurança de email incluem o seguinte:
  
- [Relatório de Status de proteção de ameaça](view-email-security-reports.md#tps) 
    
- [Relatório detecções de malware](view-email-security-reports.md#maldet)
    
- [Relatório de Malware principais](#top-malware-report)
    
- [Relatório de remetentes e destinatários principais](view-email-security-reports.md#topsenders)
    
- [Falsificar o relatório de email](#spoof-mail-report)
    
- [Relatório detecções de spam](#spam-detections-report)
    
- [Relatório email enviado e recebido](view-email-security-reports.md#sentreceivedemail)
    
- [Relatório de mensagens relatado pelo usuário](view-email-security-reports.md#userreported) (novo)! 
    
## <a name="threat-protection-status-report"></a>Relatório de Status de proteção de ameaça

O novo relatório de **Status de proteção de ameaça** é um relatório inteligente que mostra o email mal-intencionado que foi detectado e bloqueada pelo Exchange Online Protection. Este relatório mostra informações sobre email identificado como malware ou uma tentativa de phishing. 

> [!NOTE]
> Um relatório de Status de proteção de ameaça está disponível para clientes que possuem [ATP do Office 365](office-365-atp.md) ou [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EOP); No entanto, as informações exibidas no relatório de Status de proteção de ameaça para clientes ATP provavelmente irá conter dados diferentes de quais clientes EOP podem ver. Por exemplo, os clientes do EOP podem exibir informações sobre detecções de malware detectado em email, mas não informações sobre [arquivos mal-intencionados detectada no SharePoint Online, OneDrive ou equipes da Microsoft](atp-for-spo-odb-and-teams.md), um recurso específico ATP. ([Saiba mais sobre os relatórios de ATP](view-reports-for-atp.md)).
  
Para exibir este relatório, no [segurança &amp; Centro de conformidade](https://protection.office.com), vá para **relatórios** \> **painel** \> **O Status de proteção de ameaça**.
  
![Relatório de Status de proteção de ameaça](media/0ff86e12-c2b2-4d89-92a5-cefb054dc070.png)
  
Quando você abre o relatório de Status de proteção de ameaça, primeiro o relatório mostra dados para os últimos sete dias por padrão. No entanto, você pode clique em **filtros** e alterar o intervalo de datas por até 90 dias de detalhes. Este relatório é útil para exibir a eficácia e o impacto dos recursos do Exchange Online Protection da sua organização e para análise de tendências de longo prazo. 
  
![Filtros do relatório de Status de proteção de ameaça](media/ab6b6b8d-e97a-4c3a-8fb1-c4940dcb7a07.png)
  
Você também pode escolher se para exibir dados de email identificado como mal-intencionado, email identificado como um phishing tentativas ou email identificado como contendo o malware.
  
![Opções de exibição de relatório de Status de proteção de ameaça](media/d429ecd7-cb7a-4c99-8d27-79a2832cf467.png)
  
## <a name="malware-detections-report"></a>Relatório detecções de malware

O relatório **Detecções de Malware** mostra quantas mensagens de entrada e saídas que foram detectadas como contendo malware para sua organização. 
  
Para exibir este relatório, no [segurança &amp; Centro de conformidade](https://protection.office.com), vá para **relatórios** \> **painel** \> **Detecções de Malware**.
  
![Exemplo de relatório detecções de malware](media/a1ba61a3-565a-46d6-b0d5-6a6cff6b31d7.png)
  
Semelhante a outros relatórios, como o relatório de Status de proteção de ameaça, o relatório exibe dados para os últimos sete dias por padrão. No entanto, você pode escolher **filtros** para alterar o intervalo de datas. 
  
## <a name="top-malware-report"></a>Relatório de Malware principais

O relatório de **Malware da parte superior** mostra os vários tipos de malware foi detectado pelo Exchange Online. 
  
Para exibir este relatório, no [segurança &amp; Centro de conformidade](https://protection.office.com), vá para **relatórios** \> **painel** \> **Superior Malware**.
  
![SCC - malwares principais do EOP](media/763330b3-f56e-4ba4-b0bb-051500ae950a.png)
  
Quando você focaliza uma triangular no gráfico de pizza, você pode ver o nome de um tipo de malware e quantas mensagens detectadas como tendo que o malware.
  
Clique (ou toque) o relatório para abri-lo em uma nova janela do navegador, onde você pode obter uma visão mais detalhada do relatório.
  
![Este relatório mostra o principal malware detectado para sua organização](media/3fded224-fb31-4713-86f2-8afce5ce2991.png)
  
O gráfico abaixo, você verá uma lista de malware detectado e quantas mensagens detectadas como tendo que o malware.
  
## <a name="top-senders-and-recipients-report"></a>Relatório de remetentes e destinatários principais

O relatório **principais remetentes e destinatários** é um gráfico de pizza mostrando suas remetentes de email superior. 
  
Para exibir este relatório, no [segurança &amp; Centro de conformidade](https://protection.office.com), vá para **relatórios** \> **painel** \> **principais remetentes e destinatários**.
  
![Para exibir este relatório, na segurança &amp; Centro de conformidade, vá para relatórios \> painel \> principais remetentes e destinatários](media/b5506b5c-2420-4a5a-9ea3-d654294ac838.png)
  
Quando você focaliza uma triangular no gráfico de pizza, você pode ver uma contagem de mensagens enviadas ou recebidas.
  
Clique (ou toque) o relatório para abri-lo em uma nova janela do navegador, onde você pode obter uma visão mais detalhada do relatório.
  
Use a lista **Mostrar dados para** optar se deseja exibir os dados para os receptores, principais remetentes, destinatários de spam e malware destinatários. Você também pode ver que recebeu malware foi detectado pelo proteção avançada de ameaça. 
  
![Use a lista Mostrar dados para exibir informações específicas](media/bd91449f-7d42-4749-8666-7b44044049b8.png)
  
Abaixo do gráfico, você verá a quem os remetentes de email superior ou destinatários foram, juntamente com uma contagem de mensagens enviadas ou recebidas para o período de tempo determinado.
  
## <a name="spoof-mail-report"></a>Falsificar o relatório de email

O relatório de **Falsificação da mala** mostra quantas mensagens de email de falsificação detectadas e deles, quais foram considerados "good" (mail de falsificação feito por razões de negócios legítimos). 
  
Para exibir este relatório, no [segurança &amp; Centro de conformidade](https://protection.office.com), vá para **relatórios** \> **painel** \> **Falsificação de email**.
  
![Para exibir este relatório, na segurança &amp; Centro de conformidade, vá para relatórios \> painel \> falsificação de email](media/0427e85c-9e40-4225-a0f0-e21a4e8b0e44.png)
  
Quando você passe o mouse sobre um dia no gráfico, você pode ver quantas mensagens de email de falsificação fornecidos por meio.
  
Clique (ou toque) o relatório para abri-lo em uma nova janela do navegador, onde você pode obter uma visão mais detalhada do relatório.
  
## <a name="spam-detections-report"></a>Relatório detecções de spam

O relatório **Detecções de Spam** mostra todo o conteúdo de spam bloqueado pelo Exchange Online. 
  
Para exibir este relatório, no [segurança &amp; Centro de conformidade](https://protection.office.com), vá para **relatórios** \> **painel** \> **Detecções de Spam**.
  
![Para exibir este relatório, na segurança &amp; Centro de conformidade, vá para relatórios \> painel \> EOP detecções de Spam](media/028cff3c-79ce-4ec0-8f0f-ec32ac28243a.png)
  
Quando você passe o mouse sobre um dia no gráfico, você pode ver quantos itens foram bloqueado desse dia modo como os itens são categorizados. Por exemplo, você pode ver quantas mensagens de spam foram filtradas e quantos itens proveniente de um endereço IP (Internet Protocol) bloqueado.
  
Clique (ou toque) o relatório para abri-lo em uma nova janela do navegador, onde você pode obter uma visão mais detalhada do relatório.
  
![O relatório detecções de Spam informa quantas mensagens de spam foram bloqueadas ou filtradas](media/370ec67d-eb30-4863-bfcf-68a41be02295.png)
  
O gráfico abaixo, você verá uma lista de itens de spam que foram detectados. Selecione um item para exibir informações adicionais, como se o item de spam foi entrada ou de saída, sua ID de mensagem e o destinatário.
  
## <a name="sent-and-received-email-report"></a>Relatório email enviado e recebido

O relatório **Sent e email recebido** é um relatório inteligente que mostra informações sobre email de entrada e saída, incluindo detecções de spam e malware email identificado como "bom". 
  
Para exibir este relatório, no [segurança &amp; Centro de conformidade](https://protection.office.com), vá para **relatórios** \> **painel** \> **enviados e recebidos de email**.
  
![Para exibir este relatório, na segurança &amp; Centro de conformidade, vá para relatórios \> painel \> Sent e email recebido](media/0e710ed0-1b0e-4dac-8796-94a01a710f3a.png)
  
Quando você passe o mouse sobre um dia no gráfico, você pode ver quantas mensagens fornecidos e como as mensagens são categorizadas. Por exemplo, você pode ver quantas mensagens detectadas como contendo malware e quantos foram identificados como spam.
  
Clique (ou toque) o relatório para abri-lo em uma nova janela do navegador, onde você pode obter uma visão mais detalhada do relatório.
  
Você pode usar a lista **romper** para exibir informações por tipo ou direção (entrada e saída). 
  
![Use a lista se quebram para baixo por para exibir informações por tipo ou direção](media/a5b30c94-d75f-4bfc-851a-cb155685b177.png)
  
O gráfico abaixo, você verá uma lista de categorias de email, **GoodMail**, **SpamContentFiltered**e assim por diante. Selecionar uma categoria para exibir informações adicionais, como ações que foram feitas para malware e se um email era de entrada ou saída.
  
![Este relatório informa sobre outras detecções de mensagem, antispam e antimalware](media/9ea4b606-f27a-46ee-97a7-be018e2b839c.png)
  
## <a name="user-reported-messages-report-new"></a>Relatório de mensagens relatado pelo usuário (novo)!

O relatório de **mensagens relatado pelo usuário** mostra informações sobre as mensagens de email que os usuários informados como lixo eletrônico, tentativas de phishing ou BOM email usando o [suplemento de mensagem de relatório](enable-the-report-message-add-in.md).
  
Detalhes estão disponíveis para cada mensagem, incluindo o motivo da entrega, tal uma exceção de política de spam ou regra de fluxo de email configurados para sua organização. Para exibir detalhes, selecione um item na lista de relatórios do usuário e, em seguida, exiba as informações nas guias **Resumo** e **detalhes** . 
  
![O relatório de mensagens User-Reported mostra rotulados como lixo eletrônico, não lixo ou phishing tentativas de usuários de mensagens.](media/ad5e9a3d-b833-419c-bcc9-3425d9604ead.png)
  
Para exibir este relatório, no [segurança &amp; Centro de conformidade](https://protection.office.com), siga um destes procedimentos:
  
- Vá para **gerenciamento de ameaça** \> **painel** \> **mensagens relatado pelo usuário**.
    
- Vá para **gerenciamento de ameaça** \> **revisão** \> **mensagens relatado pelo usuário**.
    
![Na segurança &amp; Centro de conformidade, escolha gerenciamento de ameaça \> revisão \> usuário informou mensagens](media/e372c57c-1414-4616-957b-bc933b8c8711.png)
  
> [!IMPORTANT]
> Na ordem para o relatório de mensagens relatado pelo usuário funcionar corretamente, o **log de auditoria deve ser ativado** para o seu ambiente do Office 365. Normalmente, isso é feito por alguém que tenha a função de Logs de auditoria atribuída no Exchange Online. Para obter mais informações, consulte [Ativar o Office 365 pesquisa de log de auditoria ativado ou desativado](turn-audit-log-search-on-or-off.md). 
  
## <a name="what-permissions-are-needed-to-view-these-reports"></a>Quais permissões são necessárias para exibir esses relatórios?

Para exibir e usar os relatórios descritos neste artigo, **você deve ter uma função apropriada atribuída para ambos os a segurança &amp; Centro de conformidade e Exchange Admin Center**.

- Para obter a segurança &amp; Centro de conformidade, você deve ter uma das seguintes funções atribuídas:
    - Gerenciamento de Organização
    - Administrador de segurança (Isso pode ser atribuído no Centro de administração do Windows Azure Active Directory ([https://aad.portal.azure.com](https://aad.portal.azure.com))
    - Leitor de segurança

- Para o Exchange Online, você deve ter uma das seguintes funções atribuídas em um centro de administração do Exchange ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) ou com os cmdlets do PowerShell (consulte [PowerShell do Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)):
    - Gerenciamento de Organização
    - Gerenciamento de Organização Somente para Exibição
    - Função de Destinatários Somente para Exibição
    - Gerenciamento de Conformidade

Para saber mais, consulte os seguintes recursos:

- [Permissões de segurança do Office 365 &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md)

- [Permissões de recursos no Exchange Online](https://docs.microsoft.com/exchange/permissions-exo/feature-permissions)
   
   
## <a name="what-if-the-reports-arent-showing-data"></a>Se os relatórios não são mostrando dados?

Se você não estiver vendo dados em seus relatórios, verifique novamente se suas políticas estão configuradas corretamente. Para saber mais, consulte [proteção antispam e antimalware no Office 365](anti-spam-and-anti-malware-protection.md).
  
## <a name="related-topics"></a>Tópicos relacionados

[Proteção anti-spam de emails do Office 365](anti-spam-protection.md)
  
[Relatórios e ideias de segurança do Office 365 &amp; Centro de conformidade](reports-and-insights-in-security-and-compliance.md)
  
[Para criar um cronograma para um relatório na segurança &amp; Centro de conformidade](create-a-schedule-for-a-report.md)
  
[Configurar e fazer o download de um relatório personalizado na segurança &amp; Centro de conformidade](set-up-and-download-a-custom-report.md)
  


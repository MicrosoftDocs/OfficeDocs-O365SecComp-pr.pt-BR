---
title: Threat management in the Office 365 Security &amp; Compliance Center
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 9/24/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 0a73d5fa-b2c8-43e7-9ed4-61f0552b1c98
description: Use o gerenciamento de ameaça para ajudar a controlar e gerenciar o acesso de dispositivo móvel aos dados da sua organização, para ajudar a proteger sua organização contra perda de dados e ajudar a proteger mensagens de entrada e saídas contra spam e softwares mal-intencionados. Você também pode usar threat management para proteger a reputação do seu domínio e para determinar se ou não os remetentes são falsificação de modo mal-intencionado contas do seu domínio.
ms.openlocfilehash: fc7d0a3fd73c03e6eec6cfd265edbf3c47ce1803
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29652246"
---
# <a name="threat-management-in-the-office-365-security-amp-compliance-center"></a>Threat management in the Office 365 Security &amp; Compliance Center

Use o gerenciamento de ameaça para ajudar a controlar e gerenciar o acesso de dispositivo móvel aos dados da sua organização, para ajudar a proteger sua organização contra perda de dados e ajudar a proteger mensagens de entrada e saídas contra spam e softwares mal-intencionados. Você também pode usar threat management para proteger a reputação do seu domínio e para determinar se ou não os remetentes são falsificação de modo mal-intencionado contas do seu domínio.
  
## <a name="how-to-view-and-use-threat-management-in-the-security-amp-compliance-center"></a>Como exibir e usar o gerenciamento de ameaça na segurança &amp; Centro de conformidade

No Office 365, use a segurança &amp; Centro de conformidade para gerenciar as ameaças em sua organização.
  
 **Para ir diretamente para a segurança &amp; Centro de conformidade:**
  
1. Acesse [https://protection.office.com](https://protection.office.com).

2. Entre no Office 365 usando a sua conta corporativa ou de estudante.

3. No painel esquerdo, selecione **gerenciamento de ameaça**.

    ![Segurança do Office 365 &amp; menu de gerenciamento de ameaça do Centro de conformidade](media/dca29ff2-ad6d-4c27-becb-b5947268d55a.png)
  
 **Para ir para a segurança &amp; Centro de conformidade usando o iniciador de aplicativo do Office 365:**
  
1. Entre no Office 365 usando a sua conta corporativa ou de estudante.

2. Selecione o iniciador app ![ícone do iniciador de aplicativo no Office 365](media/7502f4ec-3c9a-435d-a7b4-b9cda85189a7.png) no canto superior esquerdo de canto e selecione o **segurança &amp; conformidade** lado a lado. 

3. No painel esquerdo, selecione **gerenciamento de ameaça**.

## <a name="about-threat-management-in-office-365"></a>Sobre o gerenciamento de ameaça no Office 365

Essas opções estarão disponíveis em **gerenciamento de ameaça** na segurança &amp; Centro de conformidade.
  
Podemos ainda está implantando o gerenciamento de ameaças de segurança &amp; Centro de conformidade, portanto, você não poderá ver todos esses ainda, ou talvez você veja mais do que as opções listadas aqui. Durante a distribuição, alguns deles, por exemplo antimalware, Dkim e outros, continuará estejam disponíveis por meio do Centro de administração do Exchange (EAC) por um tempo limitado.

Em alguns casos, há pequenas diferenças entre a segurança e a EAT &amp; implementações do Centro de conformidade. Por exemplo, caracteres com suporte para filtros de spam são diferentes entre as duas plataformas. Artigos são fornecidas que oferecem mais informações sobre as diferenças específicas quando ocorrem.
  
|**Ferramenta**|**Descrição**|
|:-----|:-----|
|**Painel Gerenciador de ameaça e incidentes** <br/> |Quando habilitado, esses painéis permitem gerenciar análise do Office 365 e threat intelligence. Para obter mais informações, consulte [Visão geral do Office 365 Threat Intelligence](office-365-ti.md).<br/> |
|**Filtragem de email** <br/> |Ajustar e monitorar definições que ajudam a evitar spam no Office 365. Criar permitir e bloquear listas, determine quem é falsificação seu domínio e por quê, configurar e visualizar as políticas de filtro de spam. Para obter mais informações, consulte [proteção de anti-spam de email do Office 365](anti-spam-protection.md).<br/> Você também pode configurar uma política para verificar se os usuários não enviem spam. Isso pode acontecer, por exemplo, se o computador de um usuário obtém infectado por malware é programada para enviar mensagens de email. Para saber como você pode impedir que o spam de saída, consulte [Configure a política de spam de saída](https://technet.microsoft.com/library/jj200737%28v=exchg.150%29.aspx).<br/> Se você estiver atualmente enfrentando um problema com spam, você pode utilize a [solução de problemas de Spam e malware](https://configure.office.com/Scenario.aspx?sid=73).           |
|**Antimalware** <br/> |Protege contra vírus e spyware e saia da sua organização no Office 365. Vírus são mal-intencionado programas de software que, quando executada, se replicar e modificar outros programas e os dados no computador. Vírus espalham em todo o seu computador procurando programas infectar e também são compartilhados de um computador para outro, geralmente por meio de email. Spyware reúne as suas informações pessoais, como informações de entrada e enviá-la de volta para seu autor. Para começar a configurar políticas antimalware, consulte [Configure anti-malware policies](https://technet.microsoft.com/library/jj200745%28v=exchg.150%29.aspx).<br/> Se você estiver atualmente enfrentando um problema com malware, você pode utilize a [solução de problemas de Spam e malware](https://configure.office.com/Scenario.aspx?sid=73).           |
|**POR DKIM** <br/> |Destinado para administradores do Office 365 mais avançados, mas está disponível para todos os clientes do Office 365, o email de identificado DomainKeys (DKIM) ajuda a assegurar que outros sistemas de email confiam em mensagens enviadas do Office 365. DKIM faz isso adicionando uma assinatura digital exclusiva para mensagens de email que você envia da sua organização. Sistemas de email que recebam email de que você podem usar essa assinatura digital para ajudar a determinar se o email é legítimo.<br/> Não se preocupe se os detalhes de como isso funciona ser um pouco complicados, porque o padrão que está configurado para você no Office 365 deve funcionar para a maioria das organizações. Se você não configurar DKIM sozinho, o Office 365 usa sua política padrão e chaves que ele cria para habilitar DKIM para seu domínio. Além disso, se você desabilitar a verificação de assinatura, após um período de tempo, o Office 365 habilita automaticamente a política padrão de Office 365 para seu domínio.<br/> Se desejar, você pode exibir esta página na segurança &amp; Centro de conformidade e consulte ou não assinaturas DKIM estiverem habilitadas para o seu domínio e você podem visualizar a última vez em que as chaves de criptografia usadas pelo Office 365 foram giradas. Você também manualmente pode girar as teclas sozinho.<br/> **Importante!** DKIM é técnica de autenticação de apenas um email usada pelo Office 365. Para ser mais eficiente, DKIM é usado juntamente com outras técnicas com suporte, como a estrutura de política do remetente (SPF) e autenticação baseada em domínio de mensagem, relatórios e conformidade (DMARC). Juntas, essas tecnologias de autenticação baseada em domínio ajudam a evitar spam e falsificação indesejadas.<br/>  Antes de fazer alterações usando a segurança DKIM &amp; Centro de conformidade, tornam-se à vontade com a tecnologia e como ele funciona. Para começar, consulte [além do básico: outras maneiras de impedir que o spam no Office 365](anti-spam-protection.md#beyond-the-basics-more-ways-to-prevent-spam-in-office-365).           |
|**Anexos Seguros**<br/>|[Anexos seguros](atp-safe-attachments.md) é parte da proteção avançada de ameaça. Quando habilitada, os anexos de email são abertos em um ambiente isolado especial que é separado do Office 365, antes de serem enviadas às caixas de entrada de destinatários. Anexos seguros foi projetado para ajudar a detectar anexos mal-intencionado mesmo antes de assinaturas de antivírus estão disponíveis. Para saber mais, consulte [Anexos seguros no Office 365](atp-safe-attachments.md).<br/> |
|**Links Seguros** <br/> |[Links seguros](atp-safe-links.md) é parte da proteção avançada de ameaça. Links seguros ajudam a impedir que os usuários seguintes URLs em email ou em documentos do Office que apontam para sites da web que são reconhecidos como sendo maliciosas. Para saber mais, consulte [Links seguros no Office 365](atp-safe-links.md).<br/> |
|**Quarentena**<br/>|Configurar a [quarentena](http://go.microsoft.com/fwlink/p/?LinkID=809005) para mensagens de email de entrada no Office 365 onde as mensagens que foram filtradas como spam, em massa, phishing, e malware email pode ser mantido para revisão posterior. Usuários e administradores podem trabalhar com mensagens em quarentena. Os usuários podem trabalhar com apenas suas próprias mensagens filtradas em quarentena. Os administradores podem pesquisar e gerenciar mensagens em quarentena para todos os usuários.<br/> |
|**Ameaças avançadas** <br/> |Exiba o [relatório de Status de proteção de ameaça](https://support.office.com/article/View-the-reports-for-Advanced-Threat-Protection-E47E838C-D99E-4C0B-B9AA-E66C4FAE902F#advancedthreats) para ver informações sobre o conteúdo mal-intencionado encontrado e bloqueadas pelo Exchange Online Protection e proteção avançada de ameaça.  <br/> |

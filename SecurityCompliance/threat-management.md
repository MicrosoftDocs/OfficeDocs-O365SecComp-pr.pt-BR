---
title: Threat management in the Office 365 Security &amp; Compliance Center
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 9/24/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 0a73d5fa-b2c8-43e7-9ed4-61f0552b1c98
ms.collection:
- M365-security-compliance
description: Use o gerenciamento de ameaças para ajudar a controlar e gerenciar o acesso de dispositivos móveis aos dados da sua organização, ajudar a proteger sua organização contra a perda de dados e ajudar a proteger mensagens de entrada e de saída de software mal-intencionado e spam. Você também usa o gerenciamento de ameaças para proteger a reputação do seu domínio e para determinar se ou não os remetentes estão falsificando contas de seu domínio de forma mal-intencionada.
ms.openlocfilehash: 9c6c39b7edc008c4a44146fac8076897e705b5f5
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32259931"
---
# <a name="threat-management-in-the-office-365-security-amp-compliance-center"></a>Threat management in the Office 365 Security &amp; Compliance Center

Use o gerenciamento de ameaças para ajudar a controlar e gerenciar o acesso de dispositivos móveis aos dados da sua organização, ajudar a proteger sua organização contra a perda de dados e ajudar a proteger mensagens de entrada e de saída de software mal-intencionado e spam. Você também usa o gerenciamento de ameaças para proteger a reputação do seu domínio e para determinar se ou não os remetentes estão falsificando contas de seu domínio de forma mal-intencionada.
  
## <a name="how-to-view-and-use-threat-management-in-the-security-amp-compliance-center"></a>Como exibir e usar o gerenciamento de ameaças no centro &amp; de conformidade de segurança

No Office 365, use o centro &amp; de conformidade de segurança para gerenciar ameaças em sua organização.
  
 **Para ir diretamente para o centro &amp; de conformidade de segurança:**
  
1. Acesse [https://protection.office.com](https://protection.office.com).

2. Entre no Office 365 usando a sua conta corporativa ou de estudante.

3. No painel esquerdo, selecione **Gerenciamento de ameaças**.

    ![Menu de gerenciamento &amp; de ameaças do centro de conformidade de segurança do Office 365](media/dca29ff2-ad6d-4c27-becb-b5947268d55a.png)
  
 **Para ir para o centro &amp; de conformidade de segurança usando o inicializador de aplicativos do Office 365:**
  
1. Entre no Office 365 usando a sua conta corporativa ou de estudante.

2. Selecione o inicializador ![de aplicativos no ícone do inicializador](media/7502f4ec-3c9a-435d-a7b4-b9cda85189a7.png) de aplicativos no Office 365 no canto superior esquerdo e selecione o bloco de **conformidade com segurança &amp; ** . 

3. No painel esquerdo, selecione **Gerenciamento de ameaças**.

## <a name="about-threat-management-in-office-365"></a>Sobre o gerenciamento de ameaças no Office 365

Essas opções estão disponíveis em **Gerenciamento de ameaças** no centro &amp; de conformidade de segurança.
  
Ainda estamos distribuindo o gerenciamento de ameaças para o &amp; centro de conformidade de segurança, portanto, você pode não ver todos eles ainda ou pode ver mais do que as opções listadas aqui. Durante a distribuição, alguns deles, por exemplo, Antimalware, DKIM e outros, continuarão disponíveis por meio do centro de administração do Exchange (Eat) por um tempo limitado.

Em alguns casos, há pequenas diferenças entre as implementações do centro de &amp; conformidade e segurança. Por exemplo, os caracteres com suporte para filtros de spam são diferentes entre as duas plataformas. São fornecidos artigos que fornecem mais informações sobre diferenças específicas quando eles ocorrem.
  
|**Ferramenta**|**Descrição**|
|:-----|:-----|
|**Painel, explorador de ameaças e incidentes** <br/> |Uma vez habilitado, esses painéis permitem que você gerencie a análise de ameaças e a investigação e a resposta do Office 365. Para obter mais informações, consulte [Office 365 Advanced Threat Protection Plan 2](office-365-ti.md).  <br/> |
|**Filtragem de email** <br/> |Ajustar e monitorar as configurações que ajudam a evitar spam no Office 365. Criar listas de permissões e bloqueios, determinar quem está falsificando seu domínio e por quê e configurar e exibir políticas de filtro de spam. Para obter mais informações, consulte [Office 365 email anti-spam Protection](anti-spam-protection.md).  <br/> Também é possível configurar uma política para verificar se os usuários não estão enviando spam. Isso pode acontecer, por exemplo, se o computador de um usuário é infectado por malware programado para enviar mensagens de email. Para saber como você pode impedir o spam de saída, consulte [Configure the Outbound Spam Policy](https://technet.microsoft.com/library/jj200737%28v=exchg.150%29.aspx).  <br/> Se você estiver tendo um problema com spam, poderá usar a solução de [problemas de spam e malware](https://configure.office.com/Scenario.aspx?sid=73).           |
|**Antimalware** <br/> |Protege contra vírus e spyware de viagem para ou da sua organização no Office 365. Os vírus são programas de software mal-intencionados que, quando executados, se replicam e modificam outros programas e dados no computador. Os vírus se espalham em todo o seu computador, procurando programas para infectar e também são compartilhados de um computador para outro, geralmente por email. O Spyware coleta suas informações pessoais, como informações de entrada, e as envia de volta ao autor. Para começar a configurar políticas Antimalware, consulte [Configure anti-malware Policies](https://technet.microsoft.com/library/jj200745%28v=exchg.150%29.aspx).  <br/> Se você estiver tendo um problema com o malware, poderá usar a [solução de problemas de spam e malware](https://configure.office.com/Scenario.aspx?sid=73).           |
|**DKIM** <br/> |Destinado a administradores do Office 365 mais avançados, mas disponíveis para todos os clientes do Office 365, DomainKeys identificadas por email (DKIM) ajuda a garantir que outros sistemas de email confiem em mensagens que você envia do Office 365. O DKIM faz isso adicionando uma assinatura digital exclusiva a mensagens de email que você envia da sua organização. Sistemas de email que recebem emails de você pode usar essa assinatura digital para ajudar a determinar se o email é legítimo.  <br/> Não se preocupe se os detalhes de como isso funciona parecerem complicados, porque o padrão configurado para você no Office 365 deve funcionar para a maioria das organizações. Se você não configurar o DKIM, o Office 365 usa sua política padrão e chaves que ele cria para habilitar o DKIM para o seu domínio. Além disso, se você desabilitar a assinatura do DKIM, após um período de tempo, o Office 365 habilitará automaticamente a política padrão do Office 365 para seu domínio.  <br/> Se quiser, você pode exibir esta página no centro de conformidade &amp; de segurança e ver se as assinaturas do DKIM estão ou não habilitadas no momento para seu domínio e pode exibir a última vez que as chaves de criptografia usadas pelo Office 365 foram giradas. Você também pode girar manualmente as teclas por conta própria.  <br/> **Important!** DKIM é apenas uma técnica de autenticação de email usada pelo Office 365. Para ser mais eficaz, o DKIM é usado junto com outras técnicas compatíveis, como a SPF (Sender Policy Framework) e autenticação de mensagens baseadas em domínio, relatórios e conformidade (DMARC). Juntas, essas tecnologias de autenticação baseadas em domínio ajudam a evitar spam e falsificação indesejada.<br/>  Antes de fazer alterações no DKIM usando o &amp; centro de conformidade de segurança, familiarize-se com a tecnologia e como ela funciona. Para começar, confira [além dos conceitos básicos: outras maneiras de evitar spam no Office 365](anti-spam-protection.md#beyond-the-basics-more-ways-to-prevent-spam-in-office-365).           |
|**Anexos Seguros**<br/>|Os [anexos seguros](atp-safe-attachments.md) fazem parte da proteção avançada contra ameaças. Quando habilitado, os anexos de email são abertos em um ambiente isolado e especial que é separado do Office 365 antes de serem enviados para caixas de entrada de destinatários. Os anexos seguros foram projetados para ajudar a detectar anexos mal-intencionados, mesmo antes que as assinaturas antivírus estejam disponíveis. Para saber mais, confira [anexos seguros no Office 365](atp-safe-attachments.md).<br/> |
|**Links Seguros** <br/> |O recurso [links seguros](atp-safe-links.md) é parte da proteção avançada contra ameaças. Os links seguros ajudam a evitar que os usuários façam seguintes URLs em email ou em documentos do Office que apontam para sites da Web que são reconhecidos como mal-intencionados. Para saber mais, confira [links seguros no Office 365](atp-safe-links.md).<br/> |
|**Quarentena**<br/>|Configure a [quarentena](http://go.microsoft.com/fwlink/p/?LinkID=809005) para mensagens de email de entrada no Office 365, onde as mensagens que foram filtradas como spam, emails em massa, phishing e malware podem ser mantidas para revisão posterior. Tanto usuários quanto administradores podem trabalhar com mensagens em quarentena. Os usuários podem trabalhar com apenas suas próprias mensagens filtradas em quarentena. Os administradores podem pesquisar e gerenciar mensagens em quarentena para todos os usuários.  <br/> |
|**Ameaças avançadas** <br/> |Exibir o [relatório de status de proteção contra ameaças](https://support.office.com/article/View-the-reports-for-Advanced-Threat-Protection-E47E838C-D99E-4C0B-B9AA-E66C4FAE902F#advancedthreats) para ver informações sobre o conteúdo mal-intencionado encontrado e bloqueado pela proteção do Exchange Online e proteção avançada contra ameaças.  <br/> |

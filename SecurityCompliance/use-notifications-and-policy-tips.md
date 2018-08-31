---
title: Enviar notificações por email e Mostrar dicas de política para políticas de DLP
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 3/21/2018
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.UnifiedDLPRuleNotifyUser
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 87496bc5-9601-4473-8021-cb05c71369c1
description: 'Uma dica de política é uma notificação ou um aviso que aparece quando alguém está funcionando com o conteúdo que está em conflito com uma política de DLP. Você pode usar as dicas de política e notificações por email para aumentar a conscientização e ajudar a instruir as pessoas sobre diretivas da sua organização. Você também pode conceder precisam de pessoas a opção de substituir a política, para que eles não estiver bloqueados caso possuam uma empresa válida ou se a diretiva está detectando um falso positivo. '
ms.openlocfilehash: a24afe6dd1203af4dc1f0f21468e828751bc5f3b
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524663"
---
# <a name="send-email-notifications-and-show-policy-tips-for-dlp-policies"></a>Enviar notificações por email e Mostrar dicas de política para políticas de DLP

Você pode usar uma política de prevenção (DLP) de perda de dados para identificar, monitorar e proteger informações confidenciais em Office 365. Você quiser que as pessoas na sua organização que trabalham com essas informações confidenciais permaneçam em conformidade com suas políticas de DLP, mas você não deseja impeça que ela desnecessariamente realizarem seus trabalhos. Isso é onde as notificações por email e dicas de política podem ajudar.
  
![Barra de mensagem mostra a dica de política no Excel 2016](media/7002ff54-1656-4a6c-993f-37427d6508c8.png)
  
Uma dica de política é uma notificação ou um aviso que aparece quando alguém esteja funcionando com o conteúdo que está em conflito com uma política de DLP — por exemplo, de conteúdo como uma planilha do Excel em um OneDrive para site de negócios que contém informações de identificação pessoal (PII) compartilhado com um usuário externo.
  
Você pode usar as dicas de política e notificações por email para aumentar a conscientização e ajudar a instruir as pessoas sobre diretivas da sua organização. Você também pode conceder precisam de pessoas a opção de substituir a política, para que eles não estiver bloqueados caso possuam uma empresa válida ou se a diretiva está detectando um falso positivo.
  
No Office 365 Security &amp; Centro de conformidade, quando você cria uma política de DLP, você pode configurar as notificações de usuário para:
  
- Enviar um email de notificação para as pessoas que você escolher que descreve o problema.
    
- Exiba uma dica de política para o conteúdo que esteja em conflito com a política DLP:
    
  - Para email no Outlook na web e Outlook 2013 e posterior, a dica de política aparece na parte superior de uma mensagem acima os destinatários enquanto a mensagem está sendo composta.
    
  - Para documentos em um OneDrive para negócios conta ou site do SharePoint Online, a dica de política é indicada por um ícone de aviso exibida no item. Para exibir mais informações, você pode selecionar um item e, em seguida, escolha **informações**![ícone do painel de informações](media/50b6d51b-92b4-4c5f-bb4b-4ca2d4aa3d04.png) no canto superior direito da página para abrir o painel de detalhes. 
    
  - Para 2016 do Excel, PowerPoint 2016 e documentos do Word 2016 que são armazenados em um OneDrive para o site de negócios ou o site do SharePoint Online que está incluído na política de DLP, a dica de política aparece na barra de mensagens e o modo de exibição Backstage (menu **arquivo** \> ** Info**).
    
## <a name="add-user-notifications-to-a-dlp-policy"></a>Adicionar notificações de usuário a uma política DLP

Quando você cria uma política de DLP, dicas de política e notificações por email são parte da seção **notificações de usuário** . 
  
1. Vá para [https://protection.office.com](https://protection.office.com).
    
2. Entrar no Office 365 usando sua conta do trabalho ou da escola. Agora você está de segurança do Office 365 &amp; Centro de conformidade.
    
3. Na segurança &amp; Centro de conformidade \> barra de navegação esquerda \> **prevenção de perda de dados** \> **política** \> **+ criar uma política**.
    
    ![Criar um botão de política](media/b1e48a08-92e2-47ca-abdc-4341694ddc7c.png)
  
4. Escolha o modelo de política DLP que protege os tipos de informações confidenciais que você precisa \> **próximo**.
    
    Para iniciar com um modelo vazio, escolha **personalizado** \> **política personalizada** \> **próximo**.
    
5. Nomeie a diretiva \> **próximo**.
    
6. Para escolher os locais que você deseja que a política DLP para proteger, siga um destes procedimentos:
    
  - Escolha **todos os locais no Office 365** \> **próximo**.
    
  - Escolha **Deixe-me escolher locais específicos** \> **próximo**.
    
    Para incluir ou excluir um local inteiro como todos os emails do Exchange ou todas as contas de OneDrive, alterne o **Status** desse local ativada ou desativada. 
    
    Para incluir somente específicos sites do SharePoint ou contas de OneDrive, alternar o **Status** para e, em seguida, clique nos links em **incluir** escolha sites específicos ou contas. 
    
7. Escolha **Configurações avançadas de uso** \> **próximo**.
    
8. Escolha **+ nova regra**.
    
9. No editor de regra, sob **as notificações de usuário**, alterne o status.
    
    ![Seção de notificações de usuário do editor de regra](media/47705927-c60b-4054-a072-ab914f33d15d.png)
  
## <a name="options-for-configuring-email-notifications"></a>Opções para a configuração de notificações por email

Para cada regra de uma política de DLP, você pode:
  
- Enviar a notificação para as pessoas que você escolher. Essas pessoas podem incluir o proprietário do conteúdo, a pessoa que modificou o conteúdo pela última vez, o proprietário do site em que o conteúdo está armazenado ou um usuário específico.
    
- Personalize o texto que está incluído na notificação usando HTML ou tokens. Consulte a seção a seguir para obter mais informações.
    
> [!NOTE]
>  Notificações de email podem ser enviadas a destinatários individuais apenas como — não grupos ou listas de distribuição. > Apenas conteúdo novo irá disparar uma notificação de e-mail. Edição de conteúdo existente irá disparar dicas de política, mas não uma notificação de e-mail. 
  
![Opções de notificação de email](media/4e7b9500-2a78-44e6-9067-09f4bfd50301.png)
  
### <a name="default-email-notification"></a>Notificação de email padrão

Notificações têm uma linha de assunto que começa com a ação tomada, como "Notificação", "Mensagem bloqueada" para email ou "Acesso bloqueado" para documentos. Se a notificação sobre um documento, o corpo da mensagem de notificação inclui um link que leva para o site de onde o documento do armazenado e abre a dica de política para o documento, onde é possível resolver qualquer problema (consulte a seção a seguir sobre dicas de política). Se a notificação sobre uma mensagem, a notificação inclui como um anexo a mensagem que corresponda a uma política de DLP.
  
![Mensagem de notificação](media/35813d40-5fd8-425f-9624-55655e74fa6b.png)
  
Por padrão, as notificações exibem um texto semelhante ao seguinte para um item em um site. O texto de notificação é configurado separadamente para cada regra, para que o texto exibido seja diferente dependendo da regra que for correspondida.
  
| |
|**Se a regra de política de DLP fizer isso...**|**Em seguida, a notificação de padrão para o SharePoint ou OneDrive para documentos comerciais diz que isso …**|**Em seguida, a notificação padrão para mensagens do Outlook diz que isso …**|
|:-----|:-----|:-----|
|Envia uma notificação, mas não permite a substituição  <br/> |Este item está em conflito com uma política de sua organização.  <br/> |Suas conflitos de mensagem de email com uma diretiva em sua organização.  <br/> |
|Bloqueia o acesso, envia uma notificação e permite a substituição  <br/> |Este item está em conflito com uma diretiva em sua organização. Se você não consegue resolver esse conflito, o acesso a este arquivo poderá ser bloqueado.  <br/> |Suas conflitos de mensagem de email com uma diretiva em sua organização. A mensagem não foi entregue a todos os destinatários.  <br/> |
|Bloqueia o acesso e envia uma notificação  <br/> |Este item está em conflito com uma política de sua organização. O acesso a este item está bloqueado para todos, exceto seu proprietário, o último modificador e o administrador de conjunto de site principal.  <br/> |Suas conflitos de mensagem de email com uma diretiva em sua organização. A mensagem não foi entregue a todos os destinatários.  <br/> |
   
### <a name="custom-email-notification"></a>Notificação de e-mail personalizado

Você pode criar uma notificação de e-mail personalizado em vez de enviar a notificação de e-mail padrão para seus usuários finais ou administradores. Notificação por e-mail personalizado ofereça suporte a HTML e tem um limite de 5.000 caracteres. Você pode usar o HTML para incluir imagens, formatação e outros branding na notificação.
  
Você também pode usar os símbolos a seguir para ajudar a personalizar a notificação por e-mail. Esses tokens são variáveis que são substituídas por uma informação específica na notificação é enviada.
  
| |
|**Token**|**Descrição**|
|:-----|:-----|
|% % AppliedActions % %  <br/> |As ações aplicadas ao conteúdo.  <br/> |
|% % ContentURL % %  <br/> |A URL do documento no site do SharePoint Online ou OneDrive para o site de negócios.  <br/> |
|% % MatchedConditions % %  <br/> |As condições que foram correspondidas pelo conteúdo. Use este token para informar as pessoas de possíveis problemas com o conteúdo.  <br/> |
   
![Mensagem de notificação mostrando onde tokens aparecem](media/cd3f36b3-40db-4f30-99e4-190750bd1955.png)
  
## <a name="options-for-configuring-policy-tips"></a>Opções para configurar dicas de política

Para cada regra de uma política de DLP, você pode configurar as dicas de política para:
  
- Simplesmente notifica a pessoa que o conteúdo está em conflito com uma política de DLP, para que eles possam tirar ação resolva o conflito. Você pode usar o texto padrão (consulte as tabelas a seguir) ou digite o texto personalizado sobre políticas específicas da sua organização.
    
- Permita que a pessoa substitua a política de DLP. Opcionalmente, você pode:
    
  - Exigem a pessoa inserir uma justificativa comercial para anular a política. Essa informação é registrada e você poderá exibi-lo nos relatórios de DLP na seção **relatórios** de segurança &amp; Centro de conformidade. 
    
  - Permitir que a pessoa relate falsos positivos e substitua a política de DLP. Essas informações também são registradas em log para fins de relatório, para que você possa usar falsos positivos para ajustar suas regras.
    
![Opções de dica de política](media/0d2f2c68-028a-4900-afe6-1d9fce5303ef.png)
  
Por exemplo, talvez você tenha uma política de DLP aplicada ao OneDrive para sites corporativos que detecta informações de identificação pessoal (PII) e esta diretiva tem três regras:
  
1. Primeira regra: Se menos de cinco instâncias dessas informações confidenciais forem detectadas em um documento e o documento for compartilhado com pessoas de dentro da organização, a ação **Enviar uma notificação** exibe uma dica de política. Para obter dicas de política, nenhuma opção de substituição é necessária porque essa regra está simplesmente notificando as pessoas e não bloqueando o acesso. 
    
2. Em segundo lugar da regra: se for maior do que cinco instâncias dessas informações confidenciais detectadas em um documento e o documento é compartilhado com pessoas dentro da organização, a ação **bloquear o acesso a conteúdo** restringe as permissões para o arquivo e o ** Enviar uma notificação** ação permite que as pessoas substituir as ações nesta regra, fornecendo uma justificativa comercial. Negócios da sua organização exigem às vezes pessoas internas compartilhem dados de PII e você não deseja sua política DLP bloquear este trabalho. 
    
3. Terceira regra: Se mais do que cinco instâncias dessas informações confidenciais forem detectadas em um documento e o documento for compartilhado com pessoas de fora organização, a ação **Revogar acesso ao conteúdo** restringe as permissões para o arquivo e a ação **Enviar uma notificação** não permite que as pessoas substituam as ações nesta regra, porque as informações são compartilhadas externamente. Sob nenhuma circunstância deve-se permitir que as pessoas em sua organização compartilhem dados de PII fora da organização. 
    
Veja aqui alguns pontos para entender sobre o uso de uma dica de política para substituir uma regra:
  
- A opção de substituição está por regra, e ela sobrepõe todas as ações na regra (exceto enviar uma notificação, que não pode ser substituída).
    
- É possível que o conteúdo coincidir com várias regras em uma política de DLP, mas apenas a dica de política da regra mais restritiva, mais alta prioridade será exibida. Por exemplo, uma dica de política de uma regra que bloqueia o acesso ao conteúdo será exibido em uma dica de política de uma regra que simplesmente envia uma notificação. Isso impede que as pessoas vejam uma cascata de dicas de política.
    
- Se as dicas de política na regra mais restritiva permitir que as pessoas substituam a regra, substituir essa regra também substitui quaisquer outras regras que o conteúdo correspondeu.
    
## <a name="policy-tips-on-onedrive-for-business-sites-and-sharepoint-online-sites"></a>Dicas de política nos sites do OneDrive for Business e do SharePoint Online

Quando um documento de um OneDrive for Business ou do site do SharePoint Online corresponde a uma regra em uma política de DLP e essa regra usa dicas de política, as dicas de política exibem ícones especiais no documento:
  
1. Se a regra enviar uma notificação sobre o arquivo, o ícone de aviso é exibido.
    
2. Se a regra bloquear o acesso ao documento, o ícone de bloqueado aparece.
    
![Ícones de dica de política em documentos em uma conta de OneDrive](media/d3e9f772-03f9-4d28-82f8-3064784332a2.png)
  
Para executar a ação em um documento, você pode selecionar um item \> escolha **informações**![ícone do painel de informações](media/50b6d51b-92b4-4c5f-bb4b-4ca2d4aa3d04.png) no canto superior direito da página para abrir o painel de detalhes \> **Dica de política de modo de exibição**.
  
A dica de política lista os problemas com o conteúdo e se as dicas de política forem configuradas com essas opções, você pode escolher **Resolver** e então **Substituir** a dica de política ou **Relatar** um falso positivo. 
  
![Dica de política de mostrando de painel de informações](media/0a191e70-80f0-4702-90f4-7a5b7aabcaab.png)
  
![Dica de política com opção para substituir](media/e250bff9-41d5-4ce4-82ea-1dc2d043fab1.png)
  
As políticas de DLP são sincronizadas para sites e o conteúdo é avaliado em comparação com elas de forma periódica e assíncrona, portanto, pode haver um pequeno atraso entre a hora em que você criar a política de DLP e a hora em que você começar a receber dicas de política. Pode haver um atraso semelhante ao resolver ou substituir uma dica de política em relação a quando o ícone do documento no site desaparece.
  
### <a name="default-text-for-policy-tips-on-sites"></a>Texto padrão para dicas de política em sites

Por padrão, as dicas de política exibem um texto semelhante ao seguinte para um item em um site. O texto de notificação é configurado separadamente para cada regra, para que o texto exibido seja diferente dependendo da regra que for correspondida.
  
| |
|**Se a regra de política de DLP fizer isso...**|**Em seguida, a dica de política padrão diz isso...**|
|:-----|:-----|
|Envia uma notificação, mas não permite a substituição  <br/> |Este item está em conflito com uma política de sua organização.  <br/> |
|Bloqueia o acesso, envia uma notificação e permite a substituição  <br/> |Este item está em conflito com uma diretiva em sua organização. Se você não consegue resolver esse conflito, o acesso a este arquivo poderá ser bloqueado.  <br/> |
|Bloqueia o acesso e envia uma notificação  <br/> |Este item está em conflito com uma política de sua organização. O acesso a este item está bloqueado para todos, exceto seu proprietário, o último modificador e o administrador de conjunto de site principal.  <br/> |
   
### <a name="custom-text-for-policy-tips-on-sites"></a>Texto personalizado para dicas de política em sites

Você pode personalizar o texto de dicas de política separadamente da notificação por e-mail. Ao contrário do texto personalizado para notificações de email (veja acima seção), texto personalizado para obter dicas de política não aceita HTML ou tokens. Em vez disso, o texto personalizado para dicas de política é apenas com um limite de 256 caracteres em texto sem formatação.
  
## <a name="policy-tips-in-outlook-on-the-web-and-outlook-2013-and-later"></a>Dicas de política no Outlook na web e o Outlook 2013 e posterior

Quando escreve um novo email no Outlook na web e o Outlook 2013 e versões posteriores, você verá uma dica de política se você adicionar conteúdo que corresponda a uma regra em uma política de DLP e essa regra usa dicas de política. A dica de política aparece na parte superior da mensagem, acima os destinatários, enquanto a mensagem está sendo composta.
  
![Dica de política na parte superior de uma mensagem que está sendo composta](media/9b3b6b74-17c5-4562-82d5-d17ecaaa8d95.png)
  
As dicas de política de trabalho se as informações confidenciais aparecem no corpo da mensagem, linha de assunto ou mesmo um anexo da mensagem, conforme mostrado aqui.
  
![Dica de política, mostrando que um anexo está em conflito com uma política de DLP](media/59ae6655-215f-47d9-ad1d-39c0d1e61740.png)
  
Se as dicas de política estão configuradas para permitir substituição, você pode escolher **Mostrar detalhes** \> **Substituir** \> insira uma justificativa comercial ou relatar um falso positivo \> **Substituir**.
  
![Dica de política na mensagem expandida para mostrar a opção de substituição](media/28bfb997-48a6-41f0-8682-d5e62488458a.png)
  
![Diálogo de dica de política, onde você pode substituir a dica de política](media/f97e836c-04bd-44b4-aec6-ed9526ea31f8.png)
  
Observe que quando você adiciona informações confidenciais a um email, pode haver latência entre quando das informações confidenciais são adicionadas e quando a dica de política será exibida.
  
### <a name="policy-tips-in-the-exchange-admin-center-vs-the-office-365-security-amp-compliance-center"></a>Dicas de política no Centro de administração do Exchange versus a segurança do Office 365 &amp; Centro de conformidade

Dicas de política podem trabalhar com políticas de DLP e criadas no Centro de administração do Exchange, ou com diretivas DLP, criadas no Office 365 Security de regras de fluxo de email &amp; Centro de conformidade, mas não ambos. Isso ocorre porque essas diretivas são armazenadas em locais diferentes, mas as dicas de política podem desenhar apenas de um único local.
  
Se você configurou dicas de política no Centro de administração do Exchange, quaisquer dicas de política que você configurar na segurança do Office 365 &amp; Centro de conformidade não aparecerá aos usuários do Outlook na web e o Outlook 2013 e posterior, até que você desative as dicas no Exchange Centro de administração. Isso garante que as regras de transporte do Exchange atuais continuará funcionando até que você escolher alternar para a segurança do Office 365 &amp; Centro de conformidade.
  
Observe que as notificações de email enquanto dicas de política podem desenhar apenas a partir de um único local são sempre enviados, mesmo se você estiver usando políticas de DLP em ambos o Office 365 Security &amp; Centro de conformidade e o Centro de administração do Exchange.
  
### <a name="default-text-for-policy-tips-in-email"></a>Texto padrão para dicas de política em email

Por padrão, dicas de política exibem texto semelhante ao seguinte para email.
  
| |
|**Se a regra de política de DLP fizer isso...**|**Em seguida, a dica de política padrão diz isso...**|
|:-----|:-----|
|Envia uma notificação, mas não permite a substituição  <br/> |Seu email está em conflito com uma diretiva em sua organização.  <br/> |
|Bloqueia o acesso, envia uma notificação e permite a substituição  <br/> |Seu email está em conflito com uma diretiva em sua organização.  <br/> |
|Bloqueia o acesso e envia uma notificação  <br/> |Seu email está em conflito com uma diretiva em sua organização.  <br/> |
   
## <a name="policy-tips-in-excel-2016-powerpoint-2016-and-word-2016"></a>Dicas de política no Excel 2016, PowerPoint 2016 e Word 2016

Quando as pessoas trabalham com conteúdo confidencial nas versões de área de trabalho do Excel 2016, PowerPoint 2016 e Word 2016, as dicas de política podem notificar a elas em tempo real que o conteúdo está em conflito com uma política de DLP. Isso requer que:
  
- O documento do Office esteja armazenado em um site do OneDrive for Business ou do SharePoint Online.
    
- O site está incluído em uma política DLP que está configurada para usar dicas de política.
    
Esses programas de desktop do Office 2016 sincronizar automaticamente as políticas de DLP diretamente do Office 365 e, então, verificar seus documentos para garantir que eles não estão em conflito com as suas políticas de DLP e exibir dicas de política em tempo real.
  
Dependendo de como você configurar as dicas de política na política de DLP, as pessoas podem optar por simplesmente ignorar a dica de política, substituir a diretiva com ou sem uma justificativa de negócios ou relatar um falso positivo.
  
As dicas de política são exibidas na barra de mensagens.
  
![Barra de mensagem mostra a dica de política no Excel 2016](media/7002ff54-1656-4a6c-993f-37427d6508c8.png)
  
As dicas de política também aparecem no modo de exibição Backstage (na guia **Arquivo**). 
  
![O Backstage mostra a dica de política no Excel 2016](media/44c561f6-8f3f-4878-b1b0-b7543f8a4120.png)
  
Se as dicas de política na política de DLP forem configuradas com essas opções, você pode escolher **Resolver** para **Substituir** uma dica de política ou **Relatar** um falso positivo. 
  
![Opções sobre dicas de política no Backstage no Excel 2016](media/5b3857ba-907e-456e-ae43-888b594c049c.png)
  
Em cada um desses programas de área de trabalho do Office 2016, as pessoas podem optar por desativar dicas de política. Se estiverem desativadas, as dicas de política que são simples notificações não aparecerão no modo de exibição Backstage ou Barra de mensagens (na guia **Arquivo**). Entretanto, as dicas de política sobre bloqueio e substituição ainda serão exibidas e ainda receberão a notificação de email. Além disso, desativar dicas de política não isenta o documento de quaisquer políticas de DLP que foram aplicadas a ele. 
  
### <a name="default-text-for-policy-tips-in-excel-2016-powerpoint-2016-and-word-2016"></a>Texto padrão para dicas de política no Excel 2016, PowerPoint 2016 e Word 2016

Por padrão, as dicas de política exibem texto semelhante ao seguinte no modo de exibição de Backstage e de Barra de mensagem de um documento aberto. O texto de notificação é configurado separadamente para cada regra, para que o texto exibido seja diferente dependendo da regra que for correspondida.
  
| |
|**Se a regra de política de DLP fizer isso...**|**Em seguida, a dica de política padrão diz isso...**|
|:-----|:-----|
|Envia uma notificação, mas não permite a substituição  <br/> |Esse arquivo está em conflito com uma diretiva em sua organização. Vá para o menu **arquivo** para obter mais informações.<br/> |
|Bloqueia o acesso, envia uma notificação e permite a substituição  <br/> |Esse arquivo está em conflito com uma diretiva em sua organização. Se você não consegue resolver esse conflito, o acesso a este arquivo poderá ser bloqueado. Vá para o menu **arquivo** para obter mais informações.<br/> |
|Bloqueia o acesso e envia uma notificação  <br/> |Esse arquivo está em conflito com uma diretiva em sua organização. Se você não consegue resolver esse conflito, o acesso a este arquivo poderá ser bloqueado. Vá para o menu **arquivo** para obter mais informações.<br/> |
   
### <a name="custom-text-for-policy-tips-in-excel-2016-powerpoint-2016-and-word-2016"></a>Dicas de texto personalizado para política no Excel 2016, 2016 do PowerPoint e Word 2016

Você pode personalizar o texto de dicas de política separadamente da notificação por e-mail. Ao contrário do texto personalizado para notificações de email (veja acima seção), texto personalizado para obter dicas de política não aceita HTML ou tokens. Em vez disso, o texto personalizado para dicas de política é apenas com um limite de 256 caracteres em texto sem formatação.
  
## <a name="more-information"></a>Mais informações

- [Visão geral das políticas de prevenção contra perda de dados](data-loss-prevention-policies.md)
    
- [Criar uma política DLP a partir de um modelo](create-a-dlp-policy-from-a-template.md)
    
- [Criar uma política DLP para proteger documentos com FCI ou outras propriedades](protect-documents-that-have-fci-or-other-properties.md)
    
- [O que os modelos de política DLP incluem](what-the-dlp-policy-templates-include.md)
    
- [O que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md)
    


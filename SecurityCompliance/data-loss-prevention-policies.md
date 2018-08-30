---
title: Visão geral das políticas de prevenção contra perda de dados
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: overview
f1_keywords:
- ms.o365.cc.DLPLandingPage
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
ms.assetid: 1966b2a7-d1e2-4d92-ab61-42efbb137f5e
description: Com uma política de prevention (DLP) de perda de dados no Office 365 Security &amp; Centro de conformidade, você pode identificar, monitorar e proteger automaticamente informações confidenciais across Office 365.
ms.openlocfilehash: e9d033bc54aae6bc1c8089793dbc618f11bef273
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "23013735"
---
# <a name="overview-of-data-loss-prevention-policies"></a>Visão geral das políticas de prevenção contra perda de dados

Para cumprir os padrões de negócios e normas do setor, as organizações precisam proteger informações confidenciais e evitar a sua divulgação acidental. Dados financeiros ou informações de identificação pessoal (PII) como números de cartão de crédito, números do seguro social ou registros de saúde são exemplos de informações confidenciais que você talvez queira impedir vazamento de fora da sua organização. Com uma política de prevention (DLP) de perda de dados no Office 365 Security &amp; Centro de conformidade, você pode identificar, monitorar e proteger automaticamente informações confidenciais across Office 365.
  
Com uma política de DLP, você pode:
  
- **Identificar informações confidenciais em vários locais, como Exchange Online, SharePoint Online e OneDrive for Business.**
    
    Por exemplo, você pode identificar qualquer documento que contém um número de cartão de crédito é armazenado em qualquer OneDrive para o site de negócios, ou você pode monitorar apenas dos sites de OneDrive de pessoas específicas.
    
- **Impedir o compartilhamento acidental de informações confidenciais**. 
    
    Por exemplo, você pode identificar qualquer documento ou email que contém um registro de integridade que é compartilhado com pessoas de fora da sua organização, e bloquear automaticamente o acesso ao documento ou bloquear o envio de email.
    
- **Monitore e proteja as informações confidenciais nas versões de área de trabalho do Excel 2016, PowerPoint 2016 e Word 2016.**
    
    Assim como no Exchange Online, SharePoint Online e OneDrive for Business, esses programas de desktop do Office 2016 incluem os mesmos recursos para identificar informações confidenciais e aplicar políticas DLP. DLP oferece monitoramento contínuo, quando as pessoas compartilham conteúdo nesses programas Office 2016.
    
- **Ajudar os usuários a aprender a manter a conformidade sem interromper o fluxo de trabalho.**
    
    Você pode instruir seus usuários sobre as políticas de DLP e ajudá-los a permanecer compatível com sem bloqueio de trabalho. Por exemplo, se um usuário tentar compartilhar um documento que contém informações confidenciais, uma política de DLP pode ambos enviar-lhes uma notificação de e-mail e mostrá-las em uma dica de política no contexto da biblioteca de documentos que permite que eles substituir a política caso possuam uma empresa justificativa. As dicas de política de mesma também aparecem no Outlook na web, Outlook 2013 e posterior, 2016 do Excel, PowerPoint 2016 e Word 2016.
    
- **Exibir DLP relatórios mostrando conteúdo que corresponda a políticas de DLP da sua organização.**
    
    Para avaliar como sua organização está em conformidade com uma política de DLP, você pode ver quantos faz a correspondência de cada política e regra tem ao longo do tempo. Se uma política de DLP permite aos usuários substituir uma dica de política e relatar falso positivo, também é possível exibir o que os usuários têm reportado.
    
Criar e gerenciar políticas de DLP na página de prevenção de perda de dados na segurança do Office 365 &amp; Centro de conformidade.
  
![Página de prevenção de perda de dados no Office 365 Security &amp; Centro de conformidade](media/943fd01c-d7aa-43a9-846d-0561321a405e.png)
  
## <a name="what-a-dlp-policy-contains"></a>O que uma política de DLP contém

Uma política de DLP contém algumas informações básicas:
  
- Onde proteger o conteúdo - **locais** como o Exchange Online, SharePoint Online e OneDrive para sites corporativos. 
    
- Quando e como proteger o conteúdo aplicando **regras** compostas por: 
    
  - **Condições** , o conteúdo deve corresponder antes que a regra é imposta – por exemplo, procure somente conteúdo que contêm números do seguro Social que tenha sido compartilhado com pessoas fora da sua organização. 
    
  - **Ações** que você deseja que a regra adote automaticamente quando o conteúdo correspondente às condições for encontrado -- por exemplo, bloquear o acesso ao documento e enviar uma notificação por email ao responsável pela conformidade e ao usuário. 
    
Você pode usar uma regra para atender a uma necessidade de proteção específicas e, em seguida, usar uma política de DLP para agrupar os requisitos de proteção comuns, como todas as regras necessárias para cumprir uma regulamentação específica.
  
Por exemplo, é possível adotar uma política DLP que ajuda a detectar a presença de informações sujeitos a Health Insurance Portability Accountability Act (HIPAA). Essa política DLP poderia ajudar a proteger os dados HIPAA (o que) em todos os sites do SharePoint Online e todos os OneDrive para sites corporativos (where) Localizando qualquer documento que contém essas informações confidenciais que são compartilhadas com pessoas fora da sua organização (a condições) e, em seguida, bloqueando o acesso ao documento e enviar uma notificação (as ações). Esses requisitos são armazenados como regras individuais e agrupados juntos como uma política de DLP para simplificar o gerenciamento e relatórios.
  
![Diagrama mostra que a política de DLP contém locais e regras](media/c006860c-2d00-42cb-aaa4-5b5638d139f7.png)
  
### <a name="locations"></a>Locais

Uma política de DLP pode localizar e proteger informações confidenciais entre o Office 365, se essa informação está localizada no Exchange Online, SharePoint Online ou OneDrive for Business. Você poderá optar facilmente proteger todos os sites do SharePoint ou as contas que OneDrive sites apenas específicos ou contas ou todas as caixas de correio. Observe que ele não ainda é possível selecionar apenas as caixas de correio de usuários específicos.
  
![Opções para locais onde uma política DLP pode ser aplicada](media/ee50a61a-e867-4571-a150-3eec8d83650f.png)
  
Observe que, se você optar por incluir ou excluir sites do SharePoint específicos ou contas de OneDrive, uma política de DLP pode conter não mais de 100 tais inclusões e exclusões. Embora esse limite existe, entenda que você pode exceder esse limite, aplicando uma política de toda a organização ou uma política que se aplica a todo locais.
  
### <a name="rules"></a>Regras

Regras são o que impor os requisitos de negócios no conteúdo da sua organização. Uma política contiver uma ou mais regras e cada regra consiste em condições e ações. Para cada regra, quando as condições forem atendidas, as ações são executadas automaticamente. Regras são executadas sequencialmente, começando com a regra de prioridade mais alta em cada diretiva.
  
Uma regra também oferece opções para notificar os usuários (com dicas de política e notificações por email) e administradores (com relatórios de incidentes de email) que o conteúdo tem correspondido a regra.
  
Aqui estão os componentes de uma regra, cada explicado abaixo.
  
![Seções do editor de regra DLP](media/1859d504-b9c2-45ed-961b-a0092251acc2.png)
  
#### <a name="conditions"></a>Condições

Condições são importantes porque determinam quais tipos de informações que você está procurando e quando executar uma ação. Por exemplo, você pode optar por ignorar o conteúdo que contenham números de passaporte, a menos que o conteúdo contém mais de dez esses números e é compartilhado com pessoas fora da sua organização.
  
Condições foco no **conteúdo**, como quais tipos de informações confidenciais que você está procurando por e também no **contexto**, como que o documento é compartilhado com. Você pode usar condições para atribuir ações diferentes aos níveis de risco diferentes – por exemplo, o conteúdo confidencial compartilhado internamente pode ser reduzir riscos e exigem menos ações do que o conteúdo confidencial compartilhadas com pessoas fora da organização. 
  
![Lista que mostra as condições DLP disponíveis](media/0fa43f90-d007-4506-ae93-43e8424fe103.png)
  
As condições disponíveis agora podem determinar se:
  
- Conteúdo contém um tipo de informações confidenciais.
    
- Conteúdo contém um rótulo. Para obter mais informações, consulte a seção a seguir [usando um rótulo como uma condição em uma política de DLP](data-loss-prevention-policies.md#label).
    
- O conteúdo é compartilhado com pessoas de fora ou de dentro da sua organização.
    
#### <a name="types-of-sensitive-information"></a>Tipos de informações confidenciais

Uma política de DLP pode ajudar a proteger informações confidenciais, que são definidas como um **tipo de informações confidenciais**. O Office 365 inclui as definições para muitos tipos de informações confidenciais comuns em diferentes regiões que estão prontos para uso, como um número de cartão de crédito, números de conta bancária, números de identificação nacionais e números de passaporte. 
  
![Lista de tipos de informações confidenciais disponíveis](media/3eaa9911-bc94-44be-902f-363dbf3b07fe.png)
  
Quando uma política de DLP procura por um tipo de informações confidenciais, como um número de cartão de crédito, ele simplesmente não parece estar para um número de 16 dígitos. Cada tipo de informação confidencial é definido e detectado usando uma combinação de:
  
- Palavras-chave
    
- Funções internas para validar as somas de verificação ou a composição
    
- Avaliação de expressões regulares para localizar correspondências padrão
    
- Análise de outros conteúdos
    
Isso ajuda a detecção de DLP atingir um alto grau de precisão enquanto reduz o número de falsos positivos que pode interromper o trabalho de pessoas.
  
#### <a name="actions"></a>Ações

Quando o conteúdo corresponde a uma condição em uma regra, você pode aplicar ações para proteger automaticamente o conteúdo.
  
![Lista de ações DLP disponíveis](media/8aef17fc-1e99-4ac7-adfc-0f2c9c1a0697.png)
  
Com as ações disponíveis agora, você pode:
  
- **Restringir o acesso ao conteúdo** Para o conteúdo do site, isso significa que o permissões para o documento são restritas para todos, exceto o administrador do conjunto de sites primário, o proprietário do documento e a pessoa que modificou o documento por último. Essas pessoas podem remover as informações confidenciais do documento ou executar outra ação corretiva. Quando o documento está em conformidade, as permissões originais serão restauradas automaticamente. Acesso a um documento quando estiver bloqueado, o documento é exibido com um ícone de dica de política especiais na biblioteca no site. 
    
    ![A dica de política mostrando acesso ao documento está bloqueada](media/b6cefed3-d212-43d7-8534-4b92b26ebd50.png)
  
    Para conteúdo de email, essa ação bloqueia a mensagem de que está sendo enviada. Dependendo como a regra DLP é configurada, o remetente verá uma NDR ou (se a regra usa uma notificação) uma notificação de dica e/ou email de política.
    
    ![Aviso de que os destinatários não autorizados devem ser removidos da mensagem](media/302f9994-912d-41e7-861f-8a4539b3c285.png)
  
#### <a name="user-notifications-and-user-overrides"></a>Notificações de usuário e substituições de usuário

Você pode usar notificações e substitui para instruir seus usuários sobre as políticas de DLP e ajudá-los a permanecer compatível com sem bloqueio de trabalho. Por exemplo, se um usuário tentar compartilhar um documento que contém informações confidenciais, uma política de DLP pode ambos enviar-lhes uma notificação de e-mail e mostrá-las em uma dica de política no contexto da biblioteca de documentos que permite que eles substituir a política caso possuam uma empresa justificativa.
  
![Notificações de usuário e de usuário substitui as seções do editor de regra DLP](media/37b560d4-6e4e-489e-9134-d4b9daf60296.png)
  
O email pode notificar a pessoa que enviou, compartilhados ou modificado pela última vez o conteúdo e, para o conteúdo do site, o administrador do conjunto de sites primário e o proprietário do documento. Além disso, é possível adicionar ou remover a quem você escolher de notificação por e-mail.
  
Além de enviar uma notificação de e-mail, uma notificação de usuário exibe uma dica de política:
  
- No Outlook 2013 e posterior e o Outlook na web.
    
- Para o documento em um SharePoint Online ou OneDrive para o site de negócios.
    
- No Excel 2016, 2016 do PowerPoint e Word 2016, quando o documento é armazenado em um site incluído uma política de DLP.
    
A dica de política e notificação por e-mail explicam por que conteúdo está em conflito com uma política de DLP. Se você escolher, a dica de notificação e a diretiva de email pode permitir que os usuários substituam uma regra relatórios um falso positivo ou fornecendo uma justificativa comercial. Isso pode ajudá-lo a instruir os usuários sobre suas políticas de DLP e impor-los sem impedindo que pessoas seus trabalhos. Informações sobre substituições e falsos positivos também é registrado em log para relatórios (veja abaixo sobre os relatórios de DLP) e incluídas no incidente relatar (próxima seção), para que o responsável pela conformidade regularmente pode revisar a essas informações.
  
Aqui está uma dica de política aparência em um OneDrive para a conta de negócios.
  
![Dica de política para um documento em uma conta de OneDrive](media/f9834d35-94f0-4511-8555-0fe69855ce6d.png)
  
#### <a name="incident-reports"></a>Relatórios de incidentes

Quando uma regra for atendida, você pode enviar um relatório de incidente para seu diretor de conformidade (ou qualquer pessoas que você escolhe) com detalhes do evento. Este relatório inclui informações sobre o item que foi correspondida, o conteúdo real que correspondem a regra e o nome da pessoa que o conteúdo da última modificação. Para mensagens de email, o relatório também inclui como um anexo da mensagem original que corresponda a uma política de DLP.
  
![Página para configurar relatórios de incidente](media/31c6da0e-981c-415e-91bf-d94ca391a893.png)
  
## <a name="grouping-and-logical-operators"></a>Operadores lógicos e agrupamento

Frequentemente sua política DLP possui um requisito direto, como identificar todos os conteúdos que contém um número de Seguridade Social dos EUA. No entanto, em outros cenários, sua política DLP talvez seja necessário identificar dados mais flexível definidas.
  
Por exemplo, para identificar conteúdo sujeito a US Health Insurance Act (HIPAA), você precisa procurar:
  
- Conteúdo que contém os tipos específicos de informações confidenciais, como um número de Seguridade Social dos EUA ou o número da Drug imposição Agency (DEA).
    
    E
    
- O conteúdo que é mais difícil identificar, como comunicações sobre atendimento médico de um paciente ou descrições de serviços médicos fornecidos. Identificar este conteúdo requer a correspondência de palavras-chave da listas de palavra-chave muito grande, como o internacional classificação de doenças (ICD-9-CM ou ICD-10-CM).
    
Você pode facilmente identificar o tais dados flexível definidas usando operadores lógicos e agrupamento (e, ou). Quando você cria uma política de DLP, você pode:
  
- Tipos de informações confidenciais de grupo.
    
- Escolha o operador lógico entre os tipos de informações confidenciais dentro de um grupo e entre os próprios grupos.
    
### <a name="choosing-the-operator-within-a-group"></a>Escolhendo o operador dentro de um grupo

Dentro de um grupo, você pode escolher se qualquer uma ou todas as condições nesse grupo devem ser atendidas para o conteúdo corresponder a regra.
  
![Grupo mostrando os operadores dentro do grupo](media/6a12f1e8-112d-48ee-9a73-82b3dd0542e7.png)
  
### <a name="adding-a-group"></a>Adicionando um grupo

Você pode adicionar rapidamente um grupo, que pode ter seu próprio condições e o operador dentro desse grupo.
  
![Adicionar botão de grupo](media/5f72f292-d1f3-4f11-a911-a9f71e10abf6.png)
  
### <a name="choosing-the-operator-between-groups"></a>Escolhendo o operador entre grupos

Entre grupos, você pode escolher se as condições em apenas um grupo ou todos os grupos devem ser atendidas para o conteúdo corresponder a regra.
  
Por exemplo, a diretiva **US HIPAA** interna possui uma regra que usa um operador **e** entre os grupos de modo que ele identifica o conteúdo que contém: 
  
- a partir do grupo **Identificadores PII** (pelo menos um número de SSN DEA **ou** número) 
    
    **E**
    
- a partir do grupo **Termos médicos** (pelo menos um ICD-9-CM palavra-chave **ou** ICD-10-CM palavra-chave) 
    
![Mostrando o operador entre grupos de grupos](media/354aa77f-569c-4847-9dfe-605ee2bb28d1.png)
  
## <a name="the-priority-by-which-rules-are-processed"></a>A prioridade pelo qual as regras são processadas.

Quando você cria regras em uma diretiva, cada regra é atribuída uma prioridade na ordem em que é criado - ou seja, a regra criada primeiro tem prioridade mais alta, a regra criada em segundo lugar tem prioridade de segunda e assim por diante. Depois de criar uma regra, sua prioridade não pode ser alterada, exceto excluindo e recriá-la.
  
![Regras na ordem de prioridade](media/f7dc06bf-bc6f-485c-bcdb-606edbcf6565.png)
  
Quando o conteúdo é avaliado em relação às regras, as regras são processadas na ordem de prioridade. Se o conteúdo corresponde a várias regras, as regras são processadas na ordem de prioridade e a ação mais restritiva é imposta. Por exemplo, se o conteúdo corresponde a todas as regras a seguintes, regra 3 é imposta porque ela é a prioridade mais alta, a regra mais restritiva:
  
- Regra 1: apenas notifica os usuários
    
- Regra 2: notifica os usuários, restringe o acesso e permite substituições de usuário
    
- Regra 3: notifica os usuários, restringe o acesso e não permitir substituições de usuário
    
- Regra 4: apenas notifica os usuários
    
- Regra de 5: restringe o acesso
    
- Regra de 6: notifica os usuários, restringe o acesso e não permitir substituições de usuário
    
Neste exemplo, observe que o correspondências para todas as regras são registradas nos logs de auditoria e mostradas nos relatórios de DLP, mesmo que apenas a regra mais restritiva é imposta.
  
Com relação à dicas de política, observe que:
  
- Somente a dica de política de prioridade, regra mais restritiva será mostrada. Por exemplo, uma dica de política de uma regra que bloqueia o acesso ao conteúdo será exibido em uma dica de política de uma regra que simplesmente envia uma notificação. Isso impede que as pessoas vejam uma cascata de dicas de política.
    
- Se as dicas de política na regra mais restritiva permitir que as pessoas substituam a regra, substituir essa regra também substitui quaisquer outras regras que o conteúdo correspondeu.
    
## <a name="tuning-rules-to-make-them-easier-or-harder-to-match"></a>Ajuste de regras para torná-los mais fácil ou mais difícil corresponder

Depois que as pessoas criam e ativem suas políticas DLP, às vezes são executados nesses problemas:
  
- Muito conteúdo que **não é** informações confidenciais coincida com as regras - em outras palavras, muitos falsos positivos. 
    
- Muito pouco conteúdo que **é** informações confidenciais coincida com as regras - em outras palavras, as ações de proteção não estão sendo aplicadas nas informações confidenciais. 
    
Para resolver esses problemas, você pode ajustar suas regras, ajustando a contagem de instância e corresponder a precisão de torná-la mais difícil ou mais fácil para conteúdo corresponder as regras. Cada tipo de informação confidencial usado em uma regra tem ambas uma instância contar e corresponder a precisão.
  
### <a name="instance-count"></a>Contagem de instância

Contagem de instância significa simplesmente quantas ocorrências de um tipo específico de informações confidenciais devem estar presentes para conteúdo corresponder a regra. Por exemplo, o conteúdo corresponderá a regra mostrada abaixo se entre 1 e 9 exclusivo dos Estados Unidos ou Reino Unido números de passaporte são identificados.
  
Observe que a contagem de instância inclui somente **exclusivo** correspondências para tipos de informações confidenciais e palavras-chave. Por exemplo, se um email contiver 10 ocorrências do mesmo número de cartão de crédito, aquelas 10 ocorrências contam como uma única instância de um número de cartão de crédito. 
  
Para usar a contagem de instância para ajustar regras, a orientação é simples:
  
- Para facilitar a regra a corresponder, diminuir a contagem de **min** e/ou aumentar a contagem **máxima** . Você também pode definir **máximo** para **qualquer** , excluindo o valor numérico. 
    
- Para tornar a regra mais difícil corresponder, aumente a contagem de **min** . 
    
Normalmente, você pode usar ações menos restritivas, por exemplo, enviar notificações de usuário, em uma regra com uma contagem de instância inferior (por exemplo, 1-9). E você usar ações mais restritivas, como restringir o acesso ao conteúdo sem permitindo substituições de usuário, em uma regra com uma contagem de instância superior (por exemplo, 10-qualquer).
  
![Contagens de instância no editor de regra](media/e7ea3c12-72c5-4bb3-9590-c924c665e84d.png)
  
### <a name="match-accuracy"></a>Precisão de correspondência

Conforme descrito acima, um tipo de informação confidencial é definido e detectado usando uma combinação de diferentes tipos de evidência. Geralmente, um tipo de informação confidencial é definido por várias dessas combinações, chamados padrões. Um padrão que requer menos evidência tem uma precisão de correspondência inferior (ou nível de confiança), enquanto um padrão que exige que mais evidências tem um maior precisão de correspondência (ou nível de confiança). Para saber mais sobre os padrões de reais e níveis de confiança usados por cada tipo de informação confidencial, consulte [quais tipos de informações confidenciais a procurar](what-the-sensitive-information-types-look-for.md).
  
Por exemplo, o tipo de informação confidencial chamado de número de cartão de crédito é definido por dois padrões:
  
- Um padrão com confiança 65% que requer:
    
  - Um número no formato de um número de cartão de crédito.
    
  - Um número que passa a soma de verificação.
    
- Um padrão com confiança 85% que requer:
    
  - Um número no formato de um número de cartão de crédito.
    
  - Um número que passa a soma de verificação.
    
  - Uma palavra-chave ou uma data de validade no formato correto.
    
Você pode usá-los confidence levels (ou precisão de correspondência) nas regras. Normalmente, você pode usar ações menos restritivas, por exemplo, enviar notificações de usuário, em uma regra com precisão de correspondência inferior. E você usar ações mais restritivas, como restringir o acesso ao conteúdo sem permitindo substituições de usuário, em uma regra com maior precisão de correspondência.
  
É importante entender que, quando um tipo específico de informações confidenciais, como um número de cartão de crédito, é identificado no conteúdo, será retornado somente um nível de confiança único:
  
- Se todos os pares para um único padrão, o nível de confiança com o padrão é retornado.
    
- Se houver correspondências para mais de um padrão (ou seja, há correspondências com dois níveis de confiança diferentes), um nível de confiança maior do que qualquer um dos padrões único sozinhos é retornado. Essa é a parte de complicado. Por exemplo, para um cartão de crédito, se forem correspondidos padrões de 65% tanto o 85%, o nível de confiança retornadas para que tipo de informação confidencial for maior que 90% porque mais evidências significa mais confiança.
    
Portanto, se você quiser criar duas regras mutuamente exclusivas para cartões de crédito, um para a precisão de correspondência de 65% e outro para a correspondência de 85% de precisão, os intervalos para fins de precisão de correspondência ficaria assim. A primeira regra seleciona apenas as correspondências do padrão 65%. O segundo selecionará regra backup corresponde com **pelo menos uma** correspondência de 85% e **potencialmente pode ter** outras correspondências de confiança de inferior. 
  
![Duas regras com diferentes intervalos para fins de precisão de correspondência](media/21bdfe36-7a91-4347-8098-11809a92f9a4.png)
  
Por esses motivos, a orientação para a criação de regras com correspondência diferente precisões é:
  
- O nível de confiança mais baixo geralmente usa o mesmo valor para **min** e **max** (e não em um intervalo). 
    
- Normalmente, o nível mais alto de confiança é um intervalo de logo acima o nível de confiança inferior a 100.
    
- Geralmente, quaisquer níveis de confiança intermediária variam de logo acima o nível de confiança inferior para imediatamente abaixo o nível mais alto de confiança.
    
## <a name="using-a-label-as-a-condition-in-a-dlp-policy"></a>Usando um rótulo como uma condição de uma política de DLP

Você pode criar um rótulo e, em seguida:
  
- **Publicar** , para que os usuários finais podem ver e aplicar manualmente a etiqueta de conteúdo. 
    
- Ele de conteúdo que **se aplicam automático** corresponde às condições que você escolher. 
    
Para obter mais informações sobre rótulos, consulte [Overview of rótulos](labels.md).
  
Depois de criar um rótulo, você pode usar esse rótulo como uma condição em suas políticas de DLP. Por exemplo, talvez você queira fazer isso porque:
  
- Você publicou um rótulo denominado **confidencial**, para que as pessoas da sua organização poderão aplicar manualmente o rótulo para documentos e emails confidenciais. Usando esse rótulo como uma condição na sua política DLP, você pode restringir o conteúdo rotulado **confidencial** sejam compartilhados com pessoas fora da sua organização. 
    
- Você criou um rótulo denominado **Alpine House** para um projeto esse nome e aplicado automaticamente esse rótulo para o conteúdo que contenha as palavras-chave "House Alpine". Usando esse rótulo como uma condição na sua política DLP, você pode mostrar uma dica de política aos usuários finais quando eles estão prestes a compartilhar esse conteúdo com alguém fora da sua organização. 
    
- Você publicou um rótulo denominado **registro imposto**, para que seu gerente de registros poderão aplicar manualmente o rótulo para o conteúdo que precisa ser classificadas como registros. Usando esse rótulo como uma condição na sua política DLP, você pode procurar por conteúdo com este rótulo juntamente com outros tipos de informações confidenciais, como ITINs ou números de identificação fiscal; Aplicar ações de proteção a conteúdo rotulada como o **registro de imposto**; e obter relatórios de atividade detalhada sobre a política de DLP a partir dos relatórios DLP e os dados de log de auditoria. 
    
- Você publicou um rótulo denominado **Equipe de liderança executiva - confidenciais** para as caixas de correio do Exchange e as contas de OneDrive de um grupo de executivos. Usando esse rótulo como uma condição na sua política DLP, é possível aplicar ações de retenção e proteção no mesmo subconjunto de conteúdo e usuários. 
    
Usando rótulos como uma condição em suas regras DLP, pode você aplicar seletivamente ações de proteção em um conjunto específico de conteúdo, locais ou usuários.
  
![Rótulos como uma condição](media/5b1752b4-a129-4a88-b010-8dcf8a38bb09.png)
  
### <a name="how-this-feature-relates-to-other-features"></a>Como esse recurso se relaciona com outros recursos

Vários recursos podem ser aplicados ao conteúdo que contém informações confidenciais:
  
- Um [aplicando um rótulo automaticamente com base nas condições](labels.md#applying-a-label-automatically-based-on-conditions) e uma [política de retenção](retention-policies.md) podem impor ações de **retenção** nesse conteúdo. 
    
- Uma política de DLP pode impor a **proteção** ações sobre este conteúdo. E antes de impô essas ações, uma política de DLP pode exigir outras condições sejam atendidas além do conteúdo que contém um rótulo. 
    
![Diagrama dos recursos que podem aplicar às informações confidenciais](media/dd410f97-a3a3-455c-a1e9-7ed8ae6893d6.png)
  
Observe que uma política de DLP tem uma rica e capacidade de detecção de uma política de rótulo ou uma retenção aplicada a informações confidenciais. Uma política de DLP pode impor ações de proteção no conteúdo que contém informações confidenciais e se o conteúdo é removida da informação confidencial, esses protetoras ações forem desfeitas na próxima vez em que o conteúdo verificado. Mas se uma política de retenção ou o rótulo é aplicado ao conteúdo que contém informações confidenciais, que é uma ação única que não poderá ser desfeita mesmo se forem removidos das informações confidenciais.
  
Usando um rótulo como uma condição em uma política de DLP, é possível aplicar ações de retenção e proteção em conteúdo com esse rótulo. Você pode pensar em conteúdo que contenha um rótulo exatamente como o conteúdo que contenha informações confidenciais - um rótulo e um tipo de informação confidencial são propriedades usadas para classificar o conteúdo, para que você pode aplicar ações em que o conteúdo.
  
![Diagrama da política de DLP usando rótulo como uma condição](media/4538fd8f-fb74-4743-bc22-a5de33adfebb.png)
  
## <a name="simple-settings-vs-advanced-settings"></a>Configurações simples versus configurações avançadas

Quando você cria uma política de DLP, você vai escolher entre as configurações simples ou avançadas:
  
- **Configurações simples** facilitam criar o tipo mais comum de política DLP sem usar o editor de regra para criar ou modificar as regras. 
    
- **Configurações avançadas de** usar o editor de regra para lhe conceder controle completo sobre cada configuração de sua política DLP. 
    
Não se preocupe, nos bastidores, configurações simples e as configurações avançadas funcionam exatamente da mesma forma, impondo regras compostas por condições e ações - somente com configurações simples, você não vir o editor de regra. É uma maneira rápida para criar uma política DLP.
  
### <a name="simple-settings"></a>Configurações simples

Sem dúvida, o cenário DLP mais comum é criar uma política para ajudar a proteger conteúdas contendo informações confidenciais sejam compartilhados com pessoas fora da sua organização e como dar uma ação corretiva automática, como restringir quem podem acessar o conteúdo, enviar notificações de administração ou de usuário final e o evento para investigação posterior a auditoria. As pessoas usam DLP para ajudar a evitar a inadvertidas divulgação de informações confidenciais.
  
Para simplificar a atingir essa meta, quando você cria uma política de DLP, você pode escolher **usar configurações simples**. Essas configurações fornecem tudo o que você precisa implementar a política de DLP mais comuns, sem ter de ir para o editor de regra.
  
![Opções de DLP para configurações simples e avançadas](media/33c93824-ead5-43b6-9c3e-fd1630c92a7d.png)
  
### <a name="advanced-settings"></a>Definições avançadas

Se você precisar criar políticas de DLP mais personalizadas, você pode escolher **Configurações avançadas de uso**.
  
As configurações avançadas apresentarão com o editor de regra, onde você tem controle total sobre cada opção possível, incluindo a contagem de instância e corresponde a exatidão (nível de confiança) para cada regra.
  
Para ir para uma seção rapidamente, clique em um item no painel de navegação superior do editor regra para ir até a seção abaixo.
  
![Menu de navegação superior do editor de regra DLP](media/c527b97f-ca53-4c79-ad19-1a63be8a8ecc.png)
  
## <a name="dlp-policy-templates"></a>Modelos de política de DLP

A primeira etapa na criação de uma política de DLP é escolher quais informações para proteger. Iniciando com um modelo DLP, você deve salvar o trabalho de criação de um novo conjunto de regras do zero e para saber quais tipos de informações devem ser incluídos por padrão. Você pode, em seguida, adicionar ou modificar esses requisitos, a fim de ajustar a regra para atender aos requisitos específicos da sua organização.
  
Um modelo de política DLP pré-configurado pode ajudá-lo a detectar tipos específicos de informações confidenciais, como dados HIPAA, dados PCI-DSS, dados do Gramm-Leach-Bliley Act ou até mesmo específicos da localidade informações de identificação pessoal (P.I.). Para facilitar a localização e proteger tipos comuns de informações confidenciais, os modelos de diretiva incluídos no Office 365 já contêm os tipos mais comuns de informações confidenciais necessários para você começar.
  
![Lista de modelos para políticas de prevenção contra perda de dados com o foco no modelo para a lei Patriot Act dos EUA](media/791b2403-430b-4987-8643-cc20abbd8148.png)
  
Sua organização também pode ter seus próprios requisitos específicos, caso em que você pode criar uma política de DLP do zero escolhendo a opção de **política personalizada** . Uma política personalizada está vazia e não contém nenhuma regra pré-criados. 
  
## <a name="roll-out-dlp-policies-gradually-with-test-mode"></a>Implementar políticas de DLP gradualmente com o modo de teste

Quando você cria suas políticas de DLP, você deve considerar distribuí-las gradualmente para avaliar o impacto e testar sua eficácia antes de impô-las totalmente. Por exemplo, você não quer uma nova política DLP acidentalmente bloquear o acesso a milhares de documentos que pessoas requerem acesso a fim de trabalho.
  
Se você estiver criando políticas de DLP com um grande potencial impacto, é recomendável seguir nesta sequência:
  
1. **Iniciar no modo de teste sem dicas de política** e, em seguida, usar a DLP relatórios e relatórios de qualquer incidente para avaliar o impacto. Você pode usar relatórios de DLP para exibir o número, local, tipo e gravidade da correspondências de política. Com base nos resultados, você pode ajustar as regras conforme necessário. No modo de teste, políticas de DLP não afetará a produtividade de pessoas que trabalham em sua organização. 
    
2. **Mover para o modo de teste com dicas de política e notificações de** modo que você pode começar a ensinar aos usuários sobre suas políticas de conformidade e prepará-los para as regras que estão prestes a ser aplicado. Nessa etapa, você também pode pedir aos usuários para relatar falsos positivos para que você pode refinar as regras. 
    
3. **Iniciar imposição total nas diretivas de** modo que as ações nas regras são aplicadas e o conteúdo do protegido. Continue a monitorar os relatórios DLP e quaisquer relatórios de incidentes ou notificações para certificar-se de que os resultados são o que você pretende. 
    
![Opções para usar o modo de teste e ativar a política](media/49fafaac-c6cb-41de-99c4-c43c3e380c3a.png)
  
Você pode desativar uma política de DLP a qualquer momento, o que afeta todas as regras na política. No entanto, cada regra pode também ser desativada individualmente alternando seu status no editor de regra.
  
![Opções para desativar uma regra em uma política](media/f7b258ff-1b8b-4127-b580-83c6492f2bef.png)
  
## <a name="dlp-reports"></a>Relatórios DLP

Depois de criar e ativar suas políticas de DLP, você desejará verificar se está trabalhando como pretendido você e ajudá-lo a permanecer em conformidade. Com os relatórios DLP, você pode exibir rapidamente o número de política de DLP e regra corresponde ao longo do tempo e o número de falsos positivos e substitui. Para cada relatório, você pode filtrar as correspondências por local, o período de tempo e até mesmo reduzi-lo para baixo até uma diretiva específica, a regra ou a ação.
  
Com os relatórios de DLP, você pode obter ideias de negócios e:
  
- Se concentrar em períodos de tempo específicos e entender os motivos para picos e tendências.
    
- Descubra os processos de negócios que violam as políticas de conformidade da sua organização.
    
- Compreender qualquer impacto nos negócios das políticas de DLP.
    
Além disso, você pode usar os relatórios de DLP para ajustar suas políticas de DLP conforme as executar.
  
![Painel de relatórios no Centro de conformidade e segurança](media/6d741252-a0ce-4429-95ba-6c857ecc9a7e.png)
  
## <a name="how-dlp-policies-work"></a>Como funcionam as políticas de DLP

A DLP detecta informações confidenciais usando análise profunda de conteúdo (não apenas uma simples verificação de texto). Essa análise profunda de conteúdo usa correspondências de palavra-chave, correspondências de dicionário, a avaliação de expressões regulares, funções internas e outros métodos para detectar conteúdos que violam as políticas de DLP. Possivelmente, apenas uma pequena porcentagem dos seus dados é considerada confidencial. Uma política de DLP pode identificar, monitorar e proteger automaticamente apenas esses dados, sem impedir ou afetar as pessoas que trabalham com o restante do seu conteúdo.
  
### <a name="policies-are-synced"></a>As políticas são sincronizadas

Depois de criar uma política de DLP na segurança &amp; Centro de conformidade, ele tem armazenados em um repositório central de política e, em seguida, sincronizados com várias fontes de conteúdo, incluindo:
  
- Exchange Online e de lá para Outlook na web e o Outlook 2013 e posterior
    
- Sites do OneDrive for Business
    
- Sites do SharePoint Online
    
- Programas de área de trabalho do Office 2016 (Excel 2016, PowerPoint 2016 e Word 2016)
    
Depois que a política do sincronizados para os locais corretos, ele começa a avaliar o conteúdo e impor ações.
  
### <a name="policy-evaluation-in-onedrive-for-business-and-sharepoint-online-sites"></a>Avaliação da política em sites do OneDrive for Business e SharePoint Online

Em todos os seus sites do SharePoint Online e OneDrive para sites corporativos, os documentos são constantemente alterados — eles são continuamente sendo criados, editado, compartilhado e assim por diante. Isso significa que documentos podem entrar em conflito ou se tornarem compatíveis com uma política de DLP a qualquer momento. Por exemplo, uma pessoa pode carregar um documento que não contenha nenhuma informações confidenciais no seu site de equipe, mas mais tarde, uma pessoa diferente pode editar o mesmo documento e adicionar informações confidenciais a ela.
  
Por esse motivo, as políticas de DLP verificam documentos em busca de correspondências de política com frequência em segundo plano. Você pode considerar isso uma avaliação assíncrona da política.
  
Aqui está como ele funciona. À medida que as pessoas adicionar ou alterar os documentos em seus sites, o mecanismo de pesquisa examina o conteúdo, para que você poderá procurá-la mais tarde. Enquanto isso acontece, o conteúdo também verificadas para informações confidenciais e verificar se ele é compartilhado. Qualquer informação confidencial que for encontrada será armazenada com segurança no índice de pesquisa, para que apenas a equipe de conformidade possa acessá-lo, mas os usuários não típicos. Cada política de DLP que você tenha ativado executa no plano de fundo (de maneira assíncrona), pesquisa frequentemente para qualquer conteúdo que corresponda a uma política de verificação e aplicação de ações para protegê-lo contra vazamento de inadvertidas.
  
![Diagrama que mostra como política de DLP avalia conteúdo de forma assíncrona](media/bdf73099-039a-4909-ae89-ac12c41992ba.png)
  
Por fim, os documentos podem conflitar uma política de DLP, mas eles também podem ficar em conformidade com ela. Por exemplo, se uma pessoa adicionar números de cartão de crédito a um documento, isso poderá fazer com que uma política de DLP bloqueie o acesso ao documento automaticamente. Mas, se a pessoa remover, mais tarde, as informações confidenciais, a ação (neste caso, bloqueio) será desfeita na próxima vez que se avaliar se o documento está de acordo com a política.
  
DLP avalia qualquer conteúdo que pode ser indexado. Para obter mais informações sobre quais tipos de arquivo são rastreados por padrão, consulte [padrão extensões de nome de arquivo rastreado e tipos de arquivo no SharePoint Server 2013 analisados](https://go.microsoft.com/fwlink/p/?LinkID=627430).
  
### <a name="policy-evaluation-in-exchange-online-outlook-2013-and-later-and-outlook-on-the-web"></a>Avaliação de política no Exchange Online, o Outlook 2013 e posterior e o Outlook na web

Quando você cria uma política de DLP que inclui o Exchange Online como um local, a política do sincronizados a partir de segurança do Office 365 &amp; Centro de conformidade para o Exchange Online e do Exchange Online para Outlook na web e o Outlook 2013 e posterior.
  
Quando uma mensagem está sendo redigida no Outlook, o usuário pode ver dicas de política como o conteúdo que está sendo criado é avaliado em relação às políticas DLP. E depois que uma mensagem é enviada, ela é avaliada em relação às políticas DLP como uma parte normal do fluxo de mensagens, juntamente com as regras de transporte do Exchange e diretivas DLP, criadas no Centro de administração do Exchange (consulte a próxima seção para obter mais informações). Políticas de DLP examina a mensagem e todos os anexos.
  
### <a name="policy-evaluation-in-the-office-2016-desktop-programs"></a>Avaliação de política nos programas de área de trabalho do Office 2016

Excel 2016, 2016 do PowerPoint e Word 2016 incluem o mesmo recurso para identificar informações confidenciais e aplicar políticas DLP como o SharePoint Online e o OneDrive for Business. Esses programas Office 2016 sincronizar suas políticas DLP diretamente do repositório central de política e avaliam continuamente o conteúdo contra as políticas DLP, quando as pessoas a trabalhar com documentos abertos a partir de um site que está incluído em uma política de DLP.
  
Avaliação de política DLP no Office 2016 foi projetada para não afetam o desempenho dos programas ou a produtividade de pessoas que trabalham no conteúdo. Se eles está trabalhando em um documento grande ou se o computador do usuário está ocupado, ela pode levar alguns segundos para uma dica de política apareça.
  
## <a name="permissions"></a>Permissões

Membros de sua equipe de conformidade que irá criar políticas de DLP precisam de permissões de segurança &amp; Centro de conformidade. Por padrão, o seu administrador proprietário terão acesso a esse local e pode dar oficiais de conformidade e acesso de outras pessoas para a segurança &amp; Centro de conformidade, sem lhes todas as permissões de um administrador de locatário. Para fazer isso, recomendamos que você:
  
1. Crie um grupo no Office 365 e adicione os responsáveis pela conformidade a ele.
    
2. Criar um grupo de função na página **permissões** de segurança &amp; Centro de conformidade. 
    
3. Adicione o grupo do Office 365 ao grupo de funções.
    
Para saber mais, confira [Give users access to the Office 365 Compliance Center](grant-access-to-the-security-and-compliance-center.md).
  
Essas permissões são necessárias somente para criar e aplicar uma política de DLP. A imposição da política não exige acesso ao conteúdo.
  
## <a name="find-the-dlp-cmdlets"></a>Encontre os cmdlets DLP

Para usar a maioria dos cmdlets para a segurança &amp; Centro de conformidade, você precisa:
  
1. [Conecte-se para a segurança do Office 365 &amp; usando o PowerShell remoto do Centro de conformidade](http://go.microsoft.com/fwlink/?LinkID=799771&amp;clcid=0x409)
    
2. Use qualquer uma dessas [a segurança do Office 365 &amp; cmdlets do Centro de conformidade](http://go.microsoft.com/fwlink/?LinkID=799772&amp;clcid=0x409)
    
No entanto, os relatórios DLP precisam receber dados dos across Office 365, incluindo o Exchange Online. Por esse motivo, os cmdlets para os relatórios de DLP estão disponíveis no Exchange Online, com Powershell não na segurança &amp; Powershell do Centro de conformidade. Portanto, para usar os cmdlets para os relatórios de DLP, você precisa:
  
1. [Conectar-se ao Exchange Online usando o PowerShell remoto](http://go.microsoft.com/fwlink/?LinkID=799773&amp;clcid=0x409)
    
2. Use qualquer um desses cmdlets para os relatórios de DLP:
    
  - [Get-DlpDetectionsReport](http://go.microsoft.com/fwlink/?LinkID=799774&amp;clcid=0x409)
    
  - [Get-DlpDetailReport](http://go.microsoft.com/fwlink/?LinkID=799775&amp;clcid=0x409)
    
## <a name="more-information"></a>Mais informações

- [Criar uma política DLP a partir de um modelo](create-a-dlp-policy-from-a-template.md)
    
- [Enviar notificações e mostrar dicas de política para políticas de DLP](use-notifications-and-policy-tips.md)
    
- [Criar uma política DLP para proteger documentos com FCI ou outras propriedades](protect-documents-that-have-fci-or-other-properties.md)
    
- [O que os modelos de política DLP incluem](what-the-dlp-policy-templates-include.md)
    
- [O que os tipos de informações confidenciais procuram](what-the-sensitive-information-types-look-for.md)
    
- [O que as funções DLP procuram](what-the-dlp-functions-look-for.md)
    
- [Criar um tipo de informação confidencial personalizado](create-a-custom-sensitive-information-type.md)
    


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
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
ms.assetid: 1966b2a7-d1e2-4d92-ab61-42efbb137f5e
description: Com uma política de prevenção de perda de dados (DLP) no centro &amp; de conformidade de segurança do Office 365, você pode identificar, monitorar e proteger automaticamente as informações confidenciais no Office 365.
ms.openlocfilehash: 6f96d7150047190e3fec2894383cd56312cfd872
ms.sourcegitcommit: 48fa456981b5c52ab8aeace173c8366b9f36723b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/28/2019
ms.locfileid: "30341762"
---
# <a name="overview-of-data-loss-prevention-policies"></a>Visão geral das políticas de prevenção contra perda de dados

Para estar em conformidade com padrões de negócios e regulamentações do setor, as organizações precisam proteger informações confidenciais e impedir sua divulgação inadvertida. Exemplos de informações confidenciais que você pode querer impedir de vazar fora da organização incluem dados financeiros ou informações de identificação pessoal (PII), como números de cartão de crédito, números de seguridade social ou registros de integridade. Com uma política de prevenção de perda de dados (DLP) no centro &amp; de conformidade de segurança do Office 365, você pode identificar, monitorar e proteger automaticamente as informações confidenciais no Office 365.
  
Com uma política de DLP, você pode:
  
- **Identificar informações confidenciais em vários locais, como o Exchange Online, o SharePoint Online e o OneDrive for Business.**
    
    Por exemplo, você pode identificar qualquer documento que contenha um número de cartão de crédito armazenado em qualquer site do OneDrive for Business ou pode monitorar apenas os sites do OneDrive de pessoas específicas.
    
- **Impedir o compartilhamento acidental de informações confidenciais**. 
    
    Por exemplo, você pode identificar qualquer documento ou email contendo um registro de integridade compartilhado com pessoas de fora da organização e, em seguida, bloquear automaticamente o acesso a esse documento ou bloquear o envio do email.
    
- **Monitore e proteja as informações confidenciais nas versões de área de trabalho do Excel 2016, PowerPoint 2016 e Word 2016.**
    
    Assim como no Exchange Online, no SharePoint Online e no OneDrive for Business, esses programas da área de trabalho do Office 2016 incluem os mesmos recursos para identificar informações confidenciais e aplicar políticas de DLP. A DLP fornece monitoramento contínuo quando as pessoas compartilham conteúdo nestes programas do Office 2016.
    
- **Ajudar os usuários a aprender a manter a conformidade sem interromper o fluxo de trabalho.**
    
    Você pode instruir seus usuários sobre as políticas de DLP e ajudá-los a permanecer em conformidade sem bloquear o trabalho. Por exemplo, se um usuário tenta compartilhar um documento contendo informações confidenciais, uma política de DLP pode enviá-los para uma notificação por email e mostrá-los uma dica de política no contexto da biblioteca de documentos que permite que eles substituam a política se tiverem uma empresa elabora. As mesmas dicas de política também aparecem no Outlook na Web, Outlook 2013 e posterior, Excel 2016, PowerPoint 2016 e Word 2016.
    
- **Exibir relatórios DLP mostrando o conteúdo que corresponde às políticas de DLP da sua organização.**
    
    Para avaliar como sua organização está em conformidade com uma política de DLP, você pode ver quantas correspondências cada política e regra tem ao longo do tempo. Se uma política de DLP permitir que os usuários substituam uma dica de política e informem um falso positivo, você também poderá ver o que os usuários relataram.
    
Você cria e gerencia políticas de DLP na página prevenção de perda de dados no centro de &amp; conformidade de segurança do Office 365.
  
![Página prevenção de perda de dados no centro de &amp; conformidade de segurança do Office 365](media/943fd01c-d7aa-43a9-846d-0561321a405e.png)
  
## <a name="what-a-dlp-policy-contains"></a>O que uma política de DLP contém

Uma política de DLP contém algumas informações básicas:
  
- Onde proteger os **locais** de conteúdo, como o Exchange Online, o SharePoint Online e o onedrive for Business sites. 
    
- Quando e como proteger o conteúdo aplicando **regras** compostas por: 
    
  - **Condições** que o conteúdo deve corresponder antes que a regra seja imposta – por exemplo, procure apenas o conteúdo que contém os números de seguridade social que foram compartilhados com pessoas de fora da sua organização. 
    
  - **Ações** que você deseja que a regra adote automaticamente quando o conteúdo correspondente às condições for encontrado -- por exemplo, bloquear o acesso ao documento e enviar uma notificação por email ao responsável pela conformidade e ao usuário. 
    
Você pode usar uma regra para atender a um requisito de proteção específico e, em seguida, usar uma política de DLP para agrupar os requisitos de proteção comuns, como todas as regras necessárias para cumprir uma regulamentação específica.
  
Por exemplo, você pode ter uma política de DLP que ajuda a detectar a presença de informações sujeitas ao ato de portabilidade e responsabilidade de seguro de saúde (HIPAA). Essa política de DLP pode ajudar a proteger os dados da HIPAA (o que) em todos os sites do SharePoint Online e todos os sites do OneDrive for Business (o onde) encontrando qualquer documento que contenha essas informações confidenciais que são compartilhadas com pessoas de fora da organização (o condições) e, em seguida, bloquear o acesso ao documento e enviar uma notificação (as ações). Esses requisitos são armazenados como regras individuais e agrupados como uma política de DLP para simplificar o gerenciamento e os relatórios.
  
![Diagrama mostra que a política de DLP contém locais e regras](media/c006860c-2d00-42cb-aaa4-5b5638d139f7.png)
  
### <a name="locations"></a>Locais

Uma política de DLP pode encontrar e proteger informações confidenciais no Office 365, se essas informações estão localizadas no Exchange Online, no SharePoint Online ou no OneDrive for Business. Você pode escolher facilmente proteger todos os sites do SharePoint ou contas do OneDrive, apenas sites ou contas específicos ou todas as caixas de correio. Observe que ainda não é possível selecionar apenas as caixas de correio de usuários específicos.
  
![Opções para locais onde uma política DLP pode ser aplicada](media/ee50a61a-e867-4571-a150-3eec8d83650f.png)
  
Observe que, se você optar por incluir ou excluir sites específicos do SharePoint ou contas do OneDrive, uma política de DLP não poderá conter mais de 100 tais inclusões e exclusões. Embora esse limite exista, entenda que você pode exceder esse limite aplicando uma política de toda a organização ou uma política que se aplica a locais inteiros.
  
### <a name="rules"></a>Regras

As regras são o que impõe seus requisitos de negócios no conteúdo da sua organização. Uma política contém uma ou mais regras, e cada regra consiste em condições e ações. Para cada regra, quando as condições forem atendidas, as ações serão realizadas automaticamente. As regras são executadas de forma seqüencial, começando com a regra de maior prioridade em cada política.
  
Uma regra também fornece opções para notificar os usuários (com dicas de política e notificações por email) e administradores (com relatórios de incidentes de email) de que o conteúdo correspondeu à regra.
  
Estes são os componentes de uma regra, cada um explicado abaixo.
  
![Seções do editor de regras DLP](media/1859d504-b9c2-45ed-961b-a0092251acc2.png)
  
#### <a name="conditions"></a>Condições

As condições são importantes porque determinam os tipos de informações que você está procurando e quando executar uma ação. Por exemplo, você pode optar por ignorar o conteúdo que contém os números do Passport, a menos que o conteúdo contenha mais de dez desses números e seja compartilhado com pessoas de fora da organização.
  
As condições se concentram no **conteúdo**, como os tipos de informações confidenciais que você está procurando e também no **contexto**, como quem o documento é compartilhado. Você pode usar as condições para atribuir diferentes ações a diferentes níveis de risco, por exemplo, conteúdo confidencial compartilhado internamente pode ser menor risco e exigir menos ações do que o conteúdo confidencial compartilhado com pessoas de fora da organização. 
  
![Lista que mostra as condições DLP disponíveis](media/0fa43f90-d007-4506-ae93-43e8424fe103.png)
  
As condições disponíveis agora podem determinar se:
  
- O conteúdo contém um tipo de informação confidencial.
    
- O conteúdo contém um rótulo. Para obter mais informações, consulte a seção a seguir [usando um rótulo como uma condição em uma política de DLP](data-loss-prevention-policies.md#label).
    
- O conteúdo é compartilhado com pessoas de fora ou de dentro da sua organização.
    
#### <a name="types-of-sensitive-information"></a>Tipos de informações confidenciais

Uma política de DLP pode ajudar a proteger informações confidenciais, que é definida como um **tipo de informação confidencial**. O Office 365 inclui definições para muitos tipos comuns de informações confidenciais em várias regiões diferentes que estão prontas para uso, como um número de cartão de crédito, números de contas bancárias, números de identificação nacional e números de passaporte. 
  
![Lista de tipos de informações confidenciais disponíveis](media/3eaa9911-bc94-44be-902f-363dbf3b07fe.png)
  
Quando uma política de DLP procura um tipo de informação confidencial, como um número de cartão de crédito, ele simplesmente não procura um número de 16 dígitos. Cada tipo de informação confidencial é definido e detectado usando uma combinação de:
  
- Palavras-chave
    
- Funções internas para validar as somas de verificação ou a composição
    
- Avaliação de expressões regulares para localizar correspondências padrão
    
- Análise de outros conteúdos
    
Isso ajuda a detecção de DLP a alcançar um alto grau de precisão enquanto reduz o número de falsos positivos que podem interromper o trabalho das pessoas.
  
#### <a name="actions"></a>Ações

Quando o conteúdo corresponde a uma condição em uma regra, você pode aplicar ações para proteger automaticamente o conteúdo.
  
![Lista de ações DLP disponíveis](media/8aef17fc-1e99-4ac7-adfc-0f2c9c1a0697.png)
  
Com as ações disponíveis agora, você pode:
  
- **Restringir o acesso ao conteúdo** Para o conteúdo do site, isso significa que as permissões para o documento são restritas a todos exceto o administrador principal do conjunto de sites, o proprietário do documento e a pessoa que modificou o documento pela última vez. Essas pessoas podem remover as informações confidenciais do documento ou executar outras ações corretivas. Quando o documento estiver em conformidade, as permissões originais serão restauradas automaticamente. Quando o acesso a um documento é bloqueado, o documento aparece com um ícone de dica de política especial na biblioteca no site. 
    
    ![A dica de política mostrando acesso ao documento está bloqueada](media/b6cefed3-d212-43d7-8534-4b92b26ebd50.png)
  
    Para conteúdo de email, esta ação impede que a mensagem seja enviada. Dependendo de como a regra DLP é configurada, o remetente verá um NDR ou (se a regra usar uma notificação) uma dica de política e/ou notificação por email.
    
    ![Aviso de que os destinatários não autorizados devem ser removidos da mensagem](media/302f9994-912d-41e7-861f-8a4539b3c285.png)
  
#### <a name="user-notifications-and-user-overrides"></a>Notificações de usuário e substituições de usuário

Você pode usar notificações e substituições para instruir seus usuários sobre as políticas de DLP e ajudá-los a permanecer em conformidade sem bloquear o trabalho. Por exemplo, se um usuário tenta compartilhar um documento contendo informações confidenciais, uma política de DLP pode enviá-los para uma notificação por email e mostrá-los uma dica de política no contexto da biblioteca de documentos que permite que eles substituam a política se tiverem uma empresa elabora.
  
![Notificações de usuário e seções de substituições de usuário do editor de regras DLP](media/37b560d4-6e4e-489e-9134-d4b9daf60296.png)
  
O email pode notificar a pessoa que enviou, compartilhou ou modificou o conteúdo e, para o conteúdo do site, o administrador do conjunto de sites principal e o proprietário do documento. Além disso, você pode adicionar ou remover o whomever escolhido da notificação por email.
  
Além de enviar uma notificação por email, uma notificação de usuário exibe uma dica de política:
  
- No Outlook 2013 e posterior e no Outlook na Web.
    
- Para o documento em um site do SharePoint Online ou do OneDrive for Business.
    
- No Excel 2016, PowerPoint 2016 e Word 2016, quando o documento é armazenado em um site incluído em uma política de DLP.
    
A dica de política e a notificação por email explicam por que o conteúdo está em conflito com uma política de DLP. Se você escolher, a notificação por email e a dica de política podem permitir que os usuários substituam uma regra, relatando um falso positivo ou fornecendo uma justificativa de negócios. Isso pode ajudá-lo a treinar os usuários sobre suas políticas de DLP e aplicá-los sem impedir que as pessoas façam seu trabalho. As informações sobre substituições e falsos positivos também são registradas para relatórios (consulte abaixo sobre os relatórios de DLP) e incluídas nos relatórios de incidentes (próxima seção), de modo que o responsável pela conformidade possa examiná-las regularmente.
  
Veja como é uma dica de política em uma conta do OneDrive for Business.
  
![Dica de política para um documento em uma conta do OneDrive](media/f9834d35-94f0-4511-8555-0fe69855ce6d.png)
  
#### <a name="incident-reports"></a>Relatórios de incidentes

Quando uma regra é correspondida, você pode enviar um relatório de incidentes para o responsável pela conformidade (ou qualquer pessoa que você escolher) com detalhes do evento. Este relatório inclui informações sobre o item que foi correspondido, o conteúdo real que correspondeu à regra e o nome da pessoa que modificou o conteúdo pela última vez. Para mensagens de email, o relatório também inclui um anexo a mensagem original que corresponde a uma política de DLP.
  
![Página para configurar relatórios de incidente](media/31c6da0e-981c-415e-91bf-d94ca391a893.png)
  
## <a name="grouping-and-logical-operators"></a>Agrupamento e operadores lógicos

Muitas vezes, sua política de DLP tem um requisito simples, como para identificar todo o conteúdo que contém um número de seguridade social dos EUA. No enTanto, em outros cenários, sua política de DLP pode precisar identificar dados mais flexíveis definidos.
  
Por exemplo, para identificar o conteúdo sujeito ao HIPAA (Health Insurance Act) dos EUA, você precisa procurar por:
  
- Conteúdo que contém tipos específicos de informações confidenciais, como um número de seguridade social ou um número de DEA (Agência de imPosição de medicamentos) nos EUA.
    
    E
    
- Conteúdo que é mais difícil de identificar, como comunicações sobre o atendimento de um paciente ou descrições de serviços médicos fornecidos. A identificação deste conteúdo requer palavras-chave correspondentes de listas de palavras-chave muito grandes, como a classificação internacional do Diseases (ICD-9-CM ou ICD-10-CM).
    
Você pode facilmente identificar esses dados com rigidez de definição usando operadores lógicos e de agrupamento (e, ou). Ao criar uma política de DLP, você pode:
  
- Tipos de informações confidenciais de grupo.
    
- Escolha o operador lógico entre os tipos de informações confidenciais dentro de um grupo e entre os grupos propriamente ditos.
    
### <a name="choosing-the-operator-within-a-group"></a>Escolhendo o operador dentro de um grupo

Dentro de um grupo, você pode escolher se qualquer uma ou todas as condições desse grupo devem ser atendidas para que o conteúdo corresponda à regra.
  
![Grupo mostrando os operadores no grupo](media/6a12f1e8-112d-48ee-9a73-82b3dd0542e7.png)
  
### <a name="adding-a-group"></a>Adicionar um grupo

Você pode adicionar rapidamente um grupo, que pode ter suas próprias condições e operador dentro desse grupo.
  
![Botão Adicionar grupo](media/5f72f292-d1f3-4f11-a911-a9f71e10abf6.png)
  
### <a name="choosing-the-operator-between-groups"></a>Escolhendo o operador entre grupos

Entre grupos, você pode escolher se as condições em apenas um grupo ou todos os grupos devem ser satisfeitas para que o conteúdo corresponda à regra.
  
Por exemplo, a política do HIPAA interna da **U.S.** tem uma regra que usa um operador **and** entre os grupos para que ele identifique conteúdo que contém: 
  
- no grupo **identificadorEs PII** (pelo menos um número de SSN **ou** número DEA) 
    
    **E**
    
- no grupo de **termos médicos** (pelo menos uma palavra-chave ICD-9-cm **ou** uma palavra-chave ICD-10-cm) 
    
![Grupos mostrando o operador entre grupos](media/354aa77f-569c-4847-9dfe-605ee2bb28d1.png)
  
## <a name="the-priority-by-which-rules-are-processed"></a>A prioridade pela qual as regras são processadas

Quando você cria regras em uma política, cada regra é atribuída a uma prioridade na ordem em que ela é criada, a regra criada primeiro tem prioridade, a regra criada segundo tem uma segunda prioridade e assim por diante. Depois de criar uma regra, sua prioridade não pode ser alterada, exceto por excluí-la e recriá-la.
  
![Regras em ordem de prioridade](media/f7dc06bf-bc6f-485c-bcdb-606edbcf6565.png)
  
Quando o conteúdo é avaliado em relação a regras, as regras são processadas em ordem de prioridade. Se o conteúdo corresponder a várias regras, as regras são processadas na ordem de prioridade e a ação mais restritiva é imposta. Por exemplo, se o conteúdo corresponder a todas as seguintes regras, a regra 3 será imposta porque é a prioridade mais alta e a regra mais restritiva:
  
- Regra 1: notifica apenas os usuários
    
- Regra 2: notifica os usuários, restringe o acesso e permite que o usuário substitua
    
- Regra 3: notifica os usuários, restringe o acesso e não permite que o usuário substitua
    
- Regra 4: notifica apenas os usuários
    
- Regra 5: restringe o acesso
    
- Regra 6: notifica os usuários, restringe o acesso e não permite que o usuário substitua
    
Neste exemplo, observe que as correspondências de todas as regras são registradas nos logs de auditoria e mostradas nos relatórios DLP, mesmo que apenas a regra mais restritiva seja imposta.
  
Com relação às dicas de política, observe que:
  
- Somente a dica de política da prioridade mais alta, a regra mais restritiva será mostrada. Por exemplo, uma dica de política de uma regra que bloqueia o acesso ao conteúdo será mostrada em uma dica de política de uma regra que simplesmente envia uma notificação. Isso impede que as pessoas vejam uma cascata de dicas de política.
    
- Se as dicas de política na regra mais restritiva permitir que as pessoas substituam a regra, substituir essa regra também substitui quaisquer outras regras que o conteúdo correspondeu.
    
## <a name="tuning-rules-to-make-them-easier-or-harder-to-match"></a>Ajustar regras para torná-las mais fáceis ou mais difíceis de corresponder

Depois que as pessoas criarem e ativarem suas políticas de DLP, elas às vezes podem executar estes problemas:
  
- Muito conteúdo que **não seja** de informações confidenciais corresponde às regras que estão em outras palavras, muitos falsos positivos. 
    
- Muito pouco conteúdo informações **** confidenciais correspondem às regras, em outras palavras, as ações de proteção não estão sendo aplicadas nas informações confidenciais. 
    
Para resolver esses problemas, você pode ajustar suas regras ajustando a contagem de instância e a precisão de correspondência para tornar mais difícil ou mais fácil para o conteúdo corresponder às regras. Cada tipo de informação confidencial usado em uma regra tem uma contagem de instância e uma precisão de correspondência.
  
### <a name="instance-count"></a>Contagem de instâncias

A contagem de instâncias significa simplesmente quantas ocorrências de um tipo específico de informações confidenciais devem estar presentes para que o conteúdo corresponda à regra. Por exemplo, o conteúdo corresponderá à regra mostrada abaixo se entre 1 e 9 números exclusivos dos EUA ou do Reino Unido são identificados.
  
Observe que a contagem de instância inclui **** somente correspondências exclusivas para tipos de informações confidenciais e palavras-chave. Por exemplo, se um email contiver 10 ocorrências do mesmo número de cartão de crédito, essas 10 ocorrências conterão como uma única instância de um número de cartão de crédito. 
  
Para usar a contagem de instâncias para ajustar regras, a orientação é simples:
  
- Para facilitar a correspondência da regra, reduza a contagem **mín** e/ou aumente a contagem **máxima** . Você também pode definir **Max** como **qualquer** excluindo o valor numérico. 
    
- Para tornar a regra mais difícil de corresponder, aumente a contagem **mín** . 
    
Normalmente, você usa ações menos restritivas, como enviar notificações de usuário, em uma regra com uma contagem de instância inferior (por exemplo, 1-9). E você usa ações mais restritivas, como restringir o acesso ao conteúdo sem permitir substituições de usuário, em uma regra com uma contagem de instância superior (por exemplo, 10-any).
  
![Contagens de instância no editor de regras](media/e7ea3c12-72c5-4bb3-9590-c924c665e84d.png)
  
### <a name="match-accuracy"></a>Corresponder à precisão

Conforme descrito acima, um tipo de informação confidencial é definido e detectado usando uma combinação de diferentes tipos de evidência. Normalmente, um tipo de informação confidencial é definido por várias combinações, chamadas padrões. Um padrão que requer menos evidências tem uma precisão de correspondência inferior (ou nível de confiança), enquanto um padrão que requer mais evidências tem maior precisão de correspondência (ou nível de confiança). Para saber mais sobre os padrões reais e os níveis de confiança usados por cada tipo de informação confidencial, confira [o que os tipos de informações confidenciais buscam](what-the-sensitive-information-types-look-for.md).
  
Por exemplo, o tipo de informação confidencial chamado número de cartão de crédito é definido por dois padrões:
  
- Um padrão com 65% de confiança que exige:
    
  - Um número no formato de um número de cartão de crédito.
    
  - Um número que passa a soma de verificação.
    
- Um padrão com 85% de confiança que exige:
    
  - Um número no formato de um número de cartão de crédito.
    
  - Um número que passa a soma de verificação.
    
  - Uma palavra-chave ou uma data de vencimento no formato correto.
    
Você pode usar esses níveis de confiança (ou corresponder precisão) em suas regras. Normalmente, você usa ações menos restritivas, como enviar notificações de usuário, em uma regra com precisão de correspondência inferior. E você usa ações mais restritivas, como restringir o acesso ao conteúdo sem permitir substituições pelo usuário, em uma regra com precisão maior de correspondência.
  
É importante entender que quando um tipo específico de informações confidenciais, como um número de cartão de crédito, é identificado no conteúdo, apenas um nível de confiança único é retornado:
  
- Se todas as correspondências forem para um único padrão, o nível de confiança desse padrão será retornado.
    
- Se houver correspondências para mais de um padrão (ou seja, se houver correspondências com dois níveis de confiança diferentes), um nível de confiança mais alto do que qualquer um dos padrões únicos é retornado sozinho. Esta é a parte complicada. Por exemplo, para um cartão de crédito, se os padrões de 65% e 85% forem correspondentes, o nível de confiança retornado para esse tipo de informação confidencial será maior que 90%, pois mais evidências significa mais confiança.
    
Portanto, se você quiser criar duas regras mutuamente exclusivas para cartões de crédito, uma para a precisão de correspondência de 65% e outra para a precisão de 85% de correspondência, os intervalos para a precisão da correspondência teriam a seguinte aparência. A primeira regra seleciona somente as correspondências do padrão 65%. A segunda regra seleciona correspondências com **pelo menos uma correspondência de** 85% e **pode potencialmente ter** outras correspondências de menor confiança. 
  
![Duas regras com intervalos diferentes para corresponder à precisão](media/21bdfe36-7a91-4347-8098-11809a92f9a4.png)
  
Por esses motivos, a orientação para a criação de regras com a mesma diferença de correspondência é:
  
- O nível de confiança mais baixo normalmente usa o mesmo valor para **mín** e **máx** (não um intervalo). 
    
- O nível mais alto de confiança normalmente é um intervalo entre o nível de confiança mais baixo e 100.
    
- Todos os níveis de confiança entre si normalmente variam desde o nível de confiança mais baixo até logo abaixo do nível de confiança maior.
    
## <a name="using-a-label-as-a-condition-in-a-dlp-policy"></a>Usar um rótulo como condição em uma política DLP

Você pode criar um rótulo e, em seguida:
  
- **Publique** -o, para que os usuários finais possam ver e aplicar manualmente o rótulo ao conteúdo. 
    
- **Aplique** -o automaticamente ao conteúdo que corresponda às condições escolhidas. 
    
Para obter mais informações sobre rótulos, consulte [Overview of Retention Labels](labels.md).
  
Depois de criar um rótulo, você poderá usar esse rótulo como uma condição nas suas políticas de DLP. Por exemplo, talvez você queira fazer isso porque:
  
- Você publicou um rótulo denominado **confidencial**, para que as pessoas em sua organização possam aplicar manualmente o rótulo a emails e documentos confidenciais. Usando esse rótulo como uma condição em sua política de DLP, você pode restringir o conteúdo rotulado **confidencial** de ser compartilhado com pessoas de fora da organização. 
    
- Você criou um rótulo chamado **Alpine House** para um projeto desse nome e, em seguida, aplicou esse rótulo automaticamente ao conteúdo que contém as palavras-chave "Alpine House". Usando esse rótulo como uma condição em sua política de DLP, você pode mostrar uma dica de política para os usuários finais quando eles estiverem prestes a compartilhar esse conteúdo com alguém fora da sua organização. 
    
- Você publicou um rótulo denominado **Record Tax**, para que o gerente de registros possa aplicar manualmente o rótulo ao conteúdo que precisa ser classificado como um registro. Usando esse rótulo como uma condição em sua política de DLP, você pode procurar conteúdo com esse rótulo em conjunto com outros tipos de informações confidenciais, como ITINs ou CPFs; aplicar ações de proteção ao registro de **impostos**rotulado de conteúdo; e obter relatórios de atividade detalhados sobre a política de DLP dos relatórios de DLP e log de auditoria. 
    
- Você publicou um rótulo denominado **executivo liderança em equipe-sensível** às caixas de correio do Exchange e às contas do onedrive de um grupo de executivos. Usando esse rótulo como uma condição em sua política de DLP, você pode aplicar ações de retenção e proteção no mesmo subconjunto de conteúdo e usuários. 
    
Com o uso de rótulos como uma condição em suas regras de DLP, você pode aplicar ações de proteção seletivamente em um conjunto específico de conteúdo, locais ou usuários.
  
![Rótulos como uma condição](media/5b1752b4-a129-4a88-b010-8dcf8a38bb09.png)

### <a name="support-for-sensitivity-labels-is-coming"></a>O suporte para rótulos de confidencialidade é proveniente

Observe que, no momento, você pode usar apenas um rótulo de retenção como uma condição, não um [rótulo](sensitivity-labels.md)de confidencialidade. No momento, estamos trabalhando no suporte para usar um rótulo de confidencialidade nessa condição.
  
### <a name="how-this-feature-relates-to-other-features"></a>Como este recurso se relaciona com outros recursos

Vários recursos podem ser aplicados ao conteúdo que contém informações confidenciais:
  
- Um [rótulo de retenção](labels.md#applying-a-retention-label-automatically-based-on-conditions) e uma [política de retenção](retention-policies.md) podem impor ações de **retenção** nesse conteúdo. 
    
- Uma política de DLP pode impor ações de **proteção** a esse conteúdo. E antes de impor essas ações, uma política de DLP pode exigir que outras condições sejam atendidas, além do conteúdo que contém um rótulo. 
    
![Diagrama dos recursos que podem ser aplicados a informações confidenciais](media/dd410f97-a3a3-455c-a1e9-7ed8ae6893d6.png)
  
Observe que uma política de DLP tem uma capacidade de detecção mais rica do que uma política de rótulo ou de retenção aplicada a informações confidenciais. Uma política de DLP pode impor ações de proteção ao conteúdo contendo informações confidenciais e, se as informações confidenciais forem removidas do conteúdo, essas ações de proteção serão desfeitas na próxima vez que o conteúdo for verificado. Mas se uma política ou um rótulo de retenção for aplicado ao conteúdo que contém informações confidenciais, essa será uma ação única que não será desfeita, mesmo que as informações confidenciais sejam removidas.
  
Usando um rótulo como uma condição em uma política de DLP, você pode aplicar ações de retenção e proteção ao conteúdo com esse rótulo. Você pode pensar no conteúdo que contém um rótulo exatamente como o conteúdo que contém informações confidenciais – tanto um rótulo quanto um tipo de informação confidencial são propriedades usadas para classificar o conteúdo, de modo que você possa impor ações nesse conteúdo.
  
![Diagrama de política DLP usando rótulo como uma condição](media/4538fd8f-fb74-4743-bc22-a5de33adfebb.png)
  
## <a name="simple-settings-vs-advanced-settings"></a>Configurações simples versus configurações avançadas

Ao criar uma política de DLP, você escolherá entre configurações simples ou avançadas:
  
- **As configurações simples** facilitam a criação do tipo mais comum de política de DLP sem usar o editor de regras para criar ou modificar regras. 
    
- **Configurações avançadas** use o editor de regras para dar a você controle completo sobre todas as configurações para sua política de DLP. 
    
Não se preocupe, nos bastidores, as configurações simples e as configurações avançadas funcionam exatamente da mesma forma, impondo regras compostas de condições e ações--apenas com configurações simples, você não vê o editor de regras. É uma maneira rápida de criar uma política de DLP.
  
### <a name="simple-settings"></a>Configurações simples

De longe, o cenário de DLP mais comum é a criação de uma política para ajudar a proteger o conteúdo que contém informações confidenciais de serem compartilhadas com pessoas de fora da organização e realizar uma ação corretiva automática, como restringir quem pode acessar o conteúdo, enviar notificações de administrador ou usuário final e auditar o evento para investigação posterior. As pessoas usam DLP para ajudar a evitar a divulgação inadvertida de informações confidenciais.
  
Para simplificar a obtenção desse objetivo, ao criar uma política de DLP, você pode escolher **usar configurações simples**. Essas configurações fornecem tudo o que você precisa para implementar a política DLP mais comum, sem ter que ir para o editor de regras.
  
![Opções de DLP para configurações simples e avançadas](media/33c93824-ead5-43b6-9c3e-fd1630c92a7d.png)
  
### <a name="advanced-settings"></a>Definições avançadas

Se for necessário criar mais políticas de DLP personalizadas, você poderá escolher **usar configurações avançadas**.
  
As configurações avançadas apresentam o editor de regras, onde você tem controle total sobre todas as opções possíveis, incluindo a contagem de instância e a precisão da correspondência (nível de confiança) para cada regra.
  
Para ir rapidamente para uma seção, clique em um item na navegação superior do editor de regras para ir para a seção abaixo.
  
![Menu de navegação superior do editor de regras DLP](media/c527b97f-ca53-4c79-ad19-1a63be8a8ecc.png)
  
## <a name="dlp-policy-templates"></a>Modelos de política DLP

A primeira etapa na criação de uma política de DLP é escolher quais informações proteger. Ao iniciar com um modelo DLP, você salva o trabalho de criar um novo conjunto de regras do zero e descobrir quais tipos de informações devem ser incluídos por padrão. Em seguida, você pode adicionar ou modificar esses requisitos para ajustar a regra para atender aos requisitos específicos da sua organização.
  
Um modelo de política de DLP pré-configurado pode ajudá-lo a detectar tipos específicos de informações confidenciais, como dados da HIPAA, dados PCI-DSS, dados da lei Gramm-Leach-Bliley ou até mesmo informações de identificação pessoal (P.I.) específicas de localidade. Para facilitar a localização e a proteção de tipos comuns de informações confidenciais, os modelos de política incluídos no Office 365 já contêm os tipos de informações confidenciais mais comuns necessários para que você comece.
  
![Lista de modelos para políticas de prevenção contra perda de dados com o foco no modelo para a lei Patriot Act dos EUA](media/791b2403-430b-4987-8643-cc20abbd8148.png)
  
Sua organização também pode ter seus próprios requisitos específicos, caso em que você pode criar uma política de DLP do zero, escolhendo a opção de **política personalizada** . Uma política personalizada está vazia e não contém regras prefeitas. 
  
## <a name="roll-out-dlp-policies-gradually-with-test-mode"></a>Implementar políticas de DLP gradualmente com o modo de teste

Ao criar suas políticas de DLP, considere a possibilidade de refazê-las gradualmente para avaliar o impacto e testar sua eficácia antes de aplicá-las completamente. Por exemplo, você não deseja que uma nova política de DLP bloqueie acidentalmente o acesso a milhares de documentos aos quais as pessoas precisam acessar para realizar o trabalho.
  
Se você estiver criando políticas DLP com um grande impacto em potencial, recomendamos seguir esta sequência:
  
1. **Inicie no modo de teste sem dicas de política** e use os relatórios de DLP e todos os relatórios de incidentes para avaliar o impacto. Você pode usar os relatórios de DLP para exibir o número, o local, o tipo e a severidade das correspondências de política. Com base nos resultados, você pode ajustar as regras conforme necessário. No modo de teste, as políticas de DLP não afetarão a produtividade das pessoas que trabalham na sua organização. 
    
2. **Mover para o modo de teste com notificações e dicas de política** para que você possa começar a ensinar os usuários sobre suas políticas de conformidade e prepará-los para as regras que serão aplicadas. Neste estágio, você também pode solicitar que os usuários reportem falsos positivos para que possa refinar ainda mais as regras. 
    
3. **Iniciar a aplicação completa nas políticas** para que as ações nas regras sejam aplicadas e que o conteúdo seja protegido. Continue a monitorar os relatórios de DLP e quaisquer relatórios de incidentes ou notificações para garantir que os resultados sejam os que você pretende. 
    
![Opções para usar o modo de teste e ativar a política](media/49fafaac-c6cb-41de-99c4-c43c3e380c3a.png)
  
Você pode desativar uma política de DLP a qualquer momento, o que afeta todas as regras da política. No enTanto, cada regra também pode ser desativada individualmente ao alternar seu status no editor de regras.
  
![Opções para desativar uma regra em uma política](media/f7b258ff-1b8b-4127-b580-83c6492f2bef.png)
  
## <a name="dlp-reports"></a>Relatórios DLP

Depois de criar e ativar suas políticas de DLP, convém verificar se elas estão funcionando conforme desejado e ajudando você a se manter em conformidade. Com os relatórios de DLP, você pode exibir rapidamente o número de correspondências de política de DLP e regras com o tempo e o número de falsos positivos e substituições. Para cada relatório, você pode filtrar essas correspondências por local, intervalo de tempo e até mesmo restringir a política, regra ou ação específica.
  
Com os relatórios de DLP, você pode obter ideias de negócios e:
  
- Se concentrar em períodos de tempo específicos e entender os motivos para picos e tendências.
    
- Descubra processos de negócios que violam as políticas de conformidade da sua organização.
    
- Compreender qualquer impacto nos negócios das políticas de DLP.
    
Além disso, você pode usar os relatórios de DLP para ajustar suas políticas de DLP conforme as executar.
  
![Painel de relatórios no centro de conformidade e segurança](media/6d741252-a0ce-4429-95ba-6c857ecc9a7e.png)
  
## <a name="how-dlp-policies-work"></a>Como funcionam as políticas de DLP

A DLP detecta informações confidenciais usando análise profunda de conteúdo (não apenas uma simples verificação de texto). Essa análise profunda de conteúdo usa correspondências de palavra-chave, correspondências de dicionário, a avaliação de expressões regulares, funções internas e outros métodos para detectar conteúdos que violam as políticas de DLP. Possivelmente, apenas uma pequena porcentagem dos seus dados é considerada confidencial. Uma política de DLP pode identificar, monitorar e proteger automaticamente apenas esses dados, sem impedir ou afetar as pessoas que trabalham com o restante do seu conteúdo.
  
### <a name="policies-are-synced"></a>As políticas são sincronizadas

Depois de criar uma política de DLP no centro &amp; de conformidade de segurança, ela é armazenada em um repositório central de políticas e, em seguida, sincronizada com várias fontes de conteúdo, incluindo:
  
- Exchange Online e de lá para o Outlook na Web e o Outlook 2013 e posterior
    
- Sites do OneDrive for Business
    
- Sites do SharePoint Online
    
- Programas de área de trabalho do Office 2016 (Excel 2016, PowerPoint 2016 e Word 2016)
    
Após a sincronização da política com os locais certos, ela começará a avaliar o conteúdo e imporá ações.
  
### <a name="policy-evaluation-in-onedrive-for-business-and-sharepoint-online-sites"></a>Avaliação da política em sites do OneDrive for Business e SharePoint Online

Em todos os sites do SharePoint Online e do OneDrive for Business, os documentos são constantemente alterados — eles estão sempre sendo criados, editados, compartilhados e assim por diante. Isso significa que os documentos podem entrar em conflito ou serem compatíveis com uma política de DLP a qualquer momento. Por exemplo, uma pessoa pode carregar um documento que não contém informações confidenciais para seu site de equipe, mas mais tarde, uma pessoa diferente pode editar o mesmo documento e adicionar informações confidenciais a ela.
  
Por esse motivo, as políticas de DLP verificam documentos em busca de correspondências de política com frequência em segundo plano. Você pode considerar isso uma avaliação assíncrona da política.
  
Veja como funciona. À medida que as pessoas adicionam ou alteram documentos em seus sites, o mecanismo de pesquisa verifica o conteúdo para que você possa procurá-lo mais tarde. Enquanto isso ocorre, o conteúdo também verifica informações confidenciais e verifica se ela é compartilhada. Todas as informações confidenciais encontradas são armazenadas com segurança no índice de pesquisa, de modo que somente a equipe de conformidade possa acessá-la, mas não usuários típicos. Cada política de DLP que você ativou é executada em segundo plano (de maneira assíncrona), verificando a pesquisa com frequência para qualquer conteúdo que corresponda a uma política e aplicando ações para protegê-lo contra vazamentos inadvertidos.
  
![Diagrama mostrando como a política de DLP avalia o conteúdo de forma assíncrona](media/bdf73099-039a-4909-ae89-ac12c41992ba.png)
  
Por fim, os documentos podem conflitar uma política de DLP, mas eles também podem ficar em conformidade com ela. Por exemplo, se uma pessoa adicionar números de cartão de crédito a um documento, isso poderá fazer com que uma política de DLP bloqueie o acesso ao documento automaticamente. Mas, se a pessoa remover, mais tarde, as informações confidenciais, a ação (neste caso, bloqueio) será desfeita na próxima vez que se avaliar se o documento está de acordo com a política.
  
O DLP avalia qualquer conteúdo que possa ser indexado. Para obter mais informações sobre quais tipos de arquivo são rastreados por padrão, confira [extensões de nome de arquivo rastreaDo padrão e tipos de arquivo analisados no SharePoint Server 2013](https://go.microsoft.com/fwlink/p/?LinkID=627430).
  
### <a name="policy-evaluation-in-exchange-online-outlook-2013-and-later-and-outlook-on-the-web"></a>Avaliação de política no Exchange Online, Outlook 2013 e posterior e Outlook na Web

Quando você cria uma política de DLP que inclui o Exchange Online como um local, a política foi sincronizada do centro de &amp; conformidade de segurança do Office 365 para o Exchange Online e, em seguida, do Exchange Online para o Outlook na Web e do Outlook 2013 e posterior.
  
Quando uma mensagem está sendo composta no Outlook, o usuário pode ver dicas de política à medida que o conteúdo que está sendo criado é avaliado em relação a políticas de DLP. E depois que uma mensagem é enviada, ela é avaliada em relação às políticas de DLP como uma parte normal do fluxo de emails, juntamente com as regras de fluxo de email do Exchange (também conhecidas como regras de transporte) e as políticas de DLP criadas no centro de administração do Exchange (consulte a próxima seção para obter mais informações). As políticas DLP examinam a mensagem e os anexos.
  
### <a name="policy-evaluation-in-the-office-2016-desktop-programs"></a>Avaliação de política nos programas de área de trabalho do Office 2016

Excel 2016, PowerPoint 2016 e Word 2016 incluem o mesmo recurso para identificar informações confidenciais e aplicar políticas de DLP como o SharePoint Online e o OneDrive for Business. Estes programas do Office 2016 sincronizam suas políticas de DLP diretamente no repositório de políticas central e, em seguida, avaliam continuamente o conteúdo em relação às políticas de DLP quando as pessoas trabalham com documentos abertos de um site incluído em uma política de DLP.
  
A avaliação de política de DLP no Office 2016 foi projetada para não afetar o desempenho dos programas ou a produtividade de pessoas que trabalham no conteúdo. Se eles estiverem trabalhando em um documento grande ou se o computador do usuário estiver ocupado, pode levar alguns segundos para que uma dica de política seja exibida.
  
## <a name="permissions"></a>Permissões

Os membros da sua equipe de conformidade que criarão políticas de DLP precisam de &amp; permissões para o centro de conformidade de segurança. Por padrão, o administrador de locatários terá acesso a esse local e poderá dar aos gerentes de conformidade e outras pessoas &amp; acesso ao centro de conformidade de segurança, sem fornecer todas as permissões de um administrador de locatários. Para fazer isso, recomendamos que você:
  
1. Crie um grupo no Office 365 e adicione os responsáveis pela conformidade a ele.
    
2. Crie um grupo de função na página **permissões** do centro de &amp; conformidade de segurança. 
    
3. Adicione o grupo do Office 365 ao grupo de funções.
    
Para saber mais, confira [Give users access to the Office 365 Compliance Center](grant-access-to-the-security-and-compliance-center.md).
  
Essas permissões são necessárias somente para criar e aplicar uma política de DLP. A imposição da política não exige acesso ao conteúdo.
  
## <a name="find-the-dlp-cmdlets"></a>Encontre os cmdlets DLP

Para usar a maioria dos cmdlets do centro de &amp; conformidade de segurança, você precisa:
  
1. [Conectar ao &amp;Centro de Conformidade e Segurança do Office 365 usando o PowerShell remoto](http://go.microsoft.com/fwlink/?LinkID=799771&amp;clcid=0x409)
    
2. Use qualquer um destes [cmdlets do &amp; centro de conformidade de segurança do Office 365](http://go.microsoft.com/fwlink/?LinkID=799772&amp;clcid=0x409)
    
No enTanto, os relatórios de DLP precisam de dados de recebimento no Office 365, incluindo o Exchange Online. Por esse motivo, os cmdlets dos relatórios de DLP estão disponíveis no PowerShell do Exchange Online, não no PowerShell &amp; do centro de conformidade de segurança. Portanto, para usar os cmdlets dos relatórios de DLP, você precisa:
  
1. [Conectar-se ao Exchange Online usando o PowerShell remoto](http://go.microsoft.com/fwlink/?LinkID=799773&amp;clcid=0x409)
    
2. Use qualquer um destes cmdlets para os relatórios de DLP:
    
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
    


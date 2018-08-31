---
title: Criar uma política de DLP para proteger documentos com FCI ou outras propriedades
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.UnifiedDLPRuleContentPropertyContainsWords
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Strat_O365_IP
ms.assetid: 1b9e3c6c-4308-4a20-b11e-c37b8013e177
description: Muitas organizações já tem um processo para identificar e classificar informações confidenciais usando as propriedades de classificação no arquivo de classificação de infraestrutura (FCI) do Windows Server, as propriedades de documento no SharePoint ou as propriedades do documento aplicada por um sistema de terceiros. Se essa for a sua organização, você pode criar uma política de DLP no Office 365 que reconhece as propriedades que tiverem sido aplicadas aos documentos por FCI do Windows Server ou outro sistema, para que a política de DLP pode ser imposta em documentos do Office com FCI específico ou outro valores de propriedade.
ms.openlocfilehash: 057cdad981249e39d6f39f231d8d60ab977e717a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "23013685"
---
# <a name="create-a-dlp-policy-to-protect-documents-with-fci-or-other-properties"></a>Criar uma política de DLP para proteger documentos com FCI ou outras propriedades

No Office 365, você pode usar uma política de prevenção (DLP) contra perda de dados para identificar, monitorar e proteger informações confidenciais. Muitas organizações já têm um processo para identificar e classificar informações confidenciais usando as propriedades de classificação no arquivo de classificação de infraestrutura (FCI) do Windows Server, as propriedades do documento no SharePoint ou as propriedades do documento aplicadas por um sistema de terceiros. Se essa for a sua organização, você pode criar uma política de DLP no Office 365 que reconhece as propriedades que foram aplicadas a documentos pelo FCI do Windows Server ou outro sistema, para que a política de DLP possa ser imposta em documentos do Office com FCI específico ou outros valores de propriedade.
  
![Diagrama mostrando o Office 365 e o sistema de classificação externa](media/59ad0ac1-4146-4919-abd1-c74d8508d25e.png)
  
Por exemplo, sua organização pode usar o Windows Server FCI para identificar documentos com informações de identificação pessoal (PII), como números de seguridade social e, em seguida, classificar o documento, definindo as **Informações de identificação pessoal** propriedade como **alto**, **moderado**, **baixa**, **público**ou **Não PII** com base no tipo e número de ocorrências do PII localizado no documento. No Office 365, você pode criar uma política de DLP que identifica os documentos que possuam essa propriedade definida como valores específicos, como **alto** e **Médio**e, em seguida, executa uma ação, como bloqueando o acesso a esses arquivos. A mesma política pode ter outra regra que leva uma ação diferente, se a propriedade estiver definida como **baixa**, por exemplo, enviar uma notificação de e-mail. Dessa forma, DLP no Office 365 é integrado ao Windows Server FCI e pode ajudar a proteger documentos do Office, carregado ou compartilhado para o Office 365 dos servidores de arquivo baseado no Windows Server.
  
Uma política de DLP simplesmente procura por um par de nome/valor de propriedade específico. Qualquer propriedade de documento pode ser usada, contanto que a propriedade tenha uma propriedade gerenciada correspondente para a pesquisa do SharePoint. Por exemplo, um conjunto de sites do SharePoint pode usar um tipo de conteúdo chamado **Relatório de viagem** com um campo obrigatório chamado **Cliente**. Sempre que uma pessoa criar um relatório de viagem, ela deve digitar o nome do cliente. Esse par de nome/valor de propriedade também pode ser usado em uma política de DLP — por exemplo, se você desejar que uma regra que bloqueia o acesso ao documento para usuários externos quando o campo **Cliente** contiver **Contoso**.
  
Observe que se você deseja aplicar a política de DLP para conteúdo com rótulos específicos do Office 365, você não deve seguir as etapas aqui. Em vez disso, saiba como [usar um rótulo como uma condição em uma política de DLP](data-loss-prevention-policies.md#using-a-label-as-a-condition-in-a-dlp-policy).
  
## <a name="before-you-create-the-dlp-policy"></a>Antes de criar a política de DLP

Antes de poder usar uma propriedade do Windows Server FCI ou outros direitos de propriedade em uma política de DLP, você precisa criar uma propriedade gerenciada no Centro de administração do SharePoint. Eis o motivo.
  
Exemplos
  
Isso é importante porque a DLP no Office 365 usa o rastreador de pesquisa para identificar e classificar informações confidenciais em seus sites e, em seguida, armazenar informações confidenciais em uma parte segura do índice de pesquisa. Quando você carregar um documento no Office 365, o SharePoint cria automaticamente propriedades rastreadas com base nas propriedades do documento. Mas, para usar uma FCI ou outra propriedade em uma política de DLP, essa propriedade rastreada precisa ser mapeada para uma propriedade gerenciada para que o conteúdo com essa propriedade seja mantido no índice.
  
Para obter mais informações sobre a pesquisa e propriedades gerenciadas, consulte [Gerenciar o esquema de pesquisa no SharePoint Online](http://go.microsoft.com/fwlink/p/?LinkID=627454).
  
### <a name="step-1-upload-a-document-with-the-needed-property-to-office-365"></a>Etapa 1: Carregar um documento com a propriedade necessária para o Office 365

Você precisará primeiro carregar um documento com a propriedade que você deseja fazer referência na sua política DLP. O Office 365 detectará a propriedade e criar automaticamente uma propriedade rastreada a partir dele. Na próxima etapa, você vai criar uma propriedade gerenciada e, em seguida, mapear a propriedade gerenciada para esta propriedade rastreada.
  
### <a name="step-2-create-a-managed-property"></a>Etapa 2: Criar uma propriedade gerenciada

1. Entre no Centro de administração do Office 365.
    
2. No painel de navegação esquerdo, escolha **Admin centrais** \> **SharePoint**. Agora você está no Centro de administração do SharePoint.
    
3. No painel de navegação esquerdo, escolha **Pesquisar** \> na página **Administração** da pesquisa \> **Gerenciar esquema de pesquisa**.
    
    ![página de administração de pesquisa no centro de administração do SharePoint](media/6bcd3aec-d11a-4f8c-9987-8f35da14d80b.png)
  
4. Na página **Propriedades gerenciadas** \> **Nova propriedade gerenciada**.
    
    ![Página de propriedades gerenciadas com o botão Nova Propriedade Gerenciada realçado](media/b161c764-414c-4037-83ed-503a49fb4410.png)
  
5. Insira um nome e uma descrição para a propriedade. Esse nome é o que aparecerá em suas políticas de DLP.
    
6. Para **Tipo**, escolha **Texto**. 
    
7. Em **Características principais**, selecione **Consultável** e **Recuperável**.
    
8. Sob **mapeamentos para propriedades rastreadas de** \> **Adicionar um mapeamento**.
    
9. Na caixa de diálogo **seleção de propriedade de rastreado** \> encontrar e selecionar a propriedade rastreada que corresponde à propriedade FCI do Windows Server ou outros direitos de propriedade que você usará em sua política DLP \> **Okey**.
    
    ![caixa de diálogo de seleção da propriedade rastreada](media/aeda1dce-1342-48bf-9594-a8e4f230e8aa.png)
  
10. Na parte inferior da página \> **Okey**.
    
## <a name="create-a-dlp-policy-that-uses-an-fci-property-or-other-property"></a>Criar uma política de DLP que usa uma propriedade FCI ou outra propriedade

Neste exemplo, uma organização está usando FCI em seus servidores de arquivo baseado no Windows Server; Especificamente, estejam usando a propriedade de classificação FCI chamada **Informações de identificação pessoal** com os valores possíveis de **alto**, **moderado**, **baixa**, **público**e **Não PII**. Agora, eles querem aproveitar seu classificação FCI existente em suas políticas de DLP no Office 365.
  
Primeiro, ela segue as etapas acima para criar uma propriedade gerenciada no SharePoint Online, a qual mapeia para a propriedade rastreada criada automaticamente da propriedade FCI.
  
Em seguida, eles criam uma política de DLP com duas regras que usam a condição de **Propriedades do documento contêm qualquer um desses valores**:
  
- **Conteúdo FCI PII - alto, moderado** A primeira regra restringe o acesso ao documento, se a propriedade de classificação FCI **Informações de identificação pessoal** é igual a **alta** ou **moderado** e o documento é compartilhado com pessoas fora da organização. 
    
- **Conteúdo FCI PII - Low** A segunda regra envia uma notificação para o proprietário do documento se a propriedade de classificação FCI **Informações de identificação pessoal** for igual a **baixa** e o documento é compartilhada com pessoas fora da organização. 
    
### <a name="create-the-dlp-policy-by-using-powershell"></a>Criar a política de DLP usando PowerShell

Observe que a condição de **Propriedades do documento contêm qualquer um desses valores** não temporariamente está disponível na interface de usuário de segurança &amp; Centro de conformidade, mas você ainda pode usar essa condição usando o PowerShell. Você pode usar o `New\Set\Get-DlpCompliancePolicy` cmdlets para trabalhar com uma política de DLP e usar o `New\Set\Get-DlpComplianceRule` cmdlets com o `ContentPropertyContainsWords` parâmetro para adicionar a condição de **Propriedades do documento contêm qualquer um desses valores**.
  
Para obter mais informações sobre esses cmdlets, consulte [a segurança do Office 365 &amp; cmdlets do Centro de conformidade](http://go.microsoft.com/fwlink/?LinkID=799772&amp;clcid=0x409).
  
1. [Conecte-se para a segurança do Office 365 &amp; usando o PowerShell remoto do Centro de conformidade](http://go.microsoft.com/fwlink/?LinkID=799771&amp;clcid=0x409)
    
2. Criar a política usando `New-DlpCompliancePolicy`.
    
    Aqui está um exemplo do PowerShell que cria uma política de DLP que se aplica a todos os locais.
    
      ```
      New-DlpCompliancePolicy -Name FCI_PII_policy -ExchangeLocation All -SharePointLocation All -OneDriveLocation All -Mode Enable
      ```

3. Criar as duas regras descritas acima usando `New-DlpComplianceRule`, onde uma regra é para o valor de **baixa** e outra regra é para os valores **altos** e **moderados** . 
    
    Aqui está um exemplo do PowerShell que cria essas duas regras. Observe que os pares de nome/valor de propriedade estão entre aspas e um nome de propriedade pode especificar vários valores separados por vírgulas, sem espaços, como`"<Property1>:<Value1>,<Value2>","<Property2>:<Value3>,<Value4>"....`
    
      ```
      New-DlpComplianceRule -Name FCI_PII_content-High,Moderate -Policy FCI_PII_policy -AccessScope NotInOrganization -BlockAccess $true -ContentPropertyContainsWords "Personally Identifiable Information:High,Moderate" -Disabled $falseNew-DlpComplianceRule -Name FCI_PII_content-Low -Policy FCI_PII_policy -AccessScope NotInOrganization -BlockAccess $false -ContentPropertyContainsWords "Personally Identifiable Information:Low" -Disabled $false -NotifyUser Owner
      ```

    Observe que o Windows Server FCI inclui várias propriedades internas, incluindo **Informações de identificação pessoal** usados neste exemplo. Os valores possíveis para cada propriedade podem ser diferentes para cada organização. O **alto**, **moderado**e **baixo** valores usados aqui são apenas um exemplo. Para sua organização, você pode exibir as propriedades de classificação do Windows Server FCI com seus valores possíveis no arquivo Server Resource Manager no servidor de arquivo baseado no Windows Server. Para obter mais informações, consulte [criar uma propriedade de classificação](http://go.microsoft.com/fwlink/p/?LinkID=627456).
    
Quando terminar, sua política deve ter duas novas regras que usam a condição de **Propriedades do documento contêm qualquer um desses valores** . Observe que essa condição não aparecerá na interface do usuário, porém outras condições, ações e configurações serão exibidas. 
  
Uma regra bloqueia o acesso para onde a propriedade de **Informações de identificação pessoal** é igual a **alta** ou **moderado**de conteúdo. Uma segunda regra envia uma notificação sobre o conteúdo, onde a propriedade de **Informações de identificação pessoal** é igual a **baixa**.
  
![Caixa de diálogo de nova política de DLP mostrando duas regras recém-criadas](media/5c56c13b-62a5-4f25-8eb7-ce83a844bb12.png)
  
## <a name="after-you-create-the-dlp-policy"></a>Depois de criar a política de DLP

Fazer as etapas nas seções anteriores criará uma política de DLP detectará rapidamente conteúdo com essa propriedade, mas somente se o conteúdo é carregado recentemente (de forma que o conteúdo indexado), ou se que o conteúdo está antiga mas apenas editada (de forma que o conteúdo reindexado) .
  
Para detectar o conteúdo com essa propriedade em todos os lugares, convém solicitar manualmente que sua biblioteca, site ou conjunto de sites seja reindexado, para que a política de DLP esteja ciente de todo o conteúdo com essa propriedade. No SharePoint Online, o conteúdo é rastreado automaticamente com base em um agendamento de rastreamento definido. O rastreador seleciona o conteúdo que foi alterado desde o último rastreamento e atualiza o índice. Se você precisar de sua política de DLP para proteger o conteúdo antes do próximo rastreamento agendado, você pode executar estas etapas.
  
> [!CAUTION]
> Indexar novamente um site pode causar uma grande carga no sistema de pesquisa. Não indexe novamente seu site, a menos que seu cenário absolutamente exigir a ele. 
  
Para obter mais informações, consulte [solicitar manualmente rastrear e indexar novamente de um site, uma biblioteca ou uma lista](http://go.microsoft.com/fwlink/p/?LinkID=627457).
  
### <a name="re-index-a-site-optional"></a>Reindexar um site (opcional)

1. No site, escolha **configurações** (ícone de engrenagem na parte superior direita) \> **Configurações do Site**.
    
2. Em **pesquisa**, escolha a **pesquisa e disponibilidade offline** \> **reindexar site**.
    
## <a name="more-information"></a>Mais informações

- [Visão geral das políticas de prevenção contra perda de dados](data-loss-prevention-policies.md)
    
- [Criar uma política DLP a partir de um modelo](create-a-dlp-policy-from-a-template.md)
    
- [Enviar notificações e mostrar dicas de política para políticas de DLP](use-notifications-and-policy-tips.md)
    
- [O que os modelos de política DLP incluem](what-the-dlp-policy-templates-include.md)
    
- [Inventário de tipos de informações confidenciais](what-the-sensitive-information-types-look-for.md)
    


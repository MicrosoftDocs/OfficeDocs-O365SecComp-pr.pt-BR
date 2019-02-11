---
title: Configurar políticas de supervisão da sua organização
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.SupervisoryReview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: d14ae7c3-fcb0-4a03-967b-cbed861bb086
description: Configure um diretivas de supervisão de revisão para capturar comunicações de funcionários para revisão.
ms.openlocfilehash: 898ef9951ea20dec1e0cc6c28ad1ed6f9a0ded6e
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29768032"
---
# <a name="configure-supervision-policies-for-your-organization"></a>Configurar políticas de supervisão da sua organização

Use diretivas de supervisão para capturar comunicações de funcionários para exame por revisores internos ou externos. Para obter mais informações sobre como as diretivas de supervisão podem ajudá-lo a monitorar comunicações em sua organização, consulte [diretivas de supervisão no Office 365](supervision-policies.md).

> [!NOTE]
> Usuários monitorados pelo diretivas de supervisão devem ter uma licença de Office 365 Enterprise E3 com o complemento de conformidade avançadas ou ser incluídos em uma assinatura do Office 365 Enterprise E5. Se você não tiver um plano de Enterprise E5 existente e quiser tentar supervisão, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).
  
Siga estas etapas para configurar e usar supervisão em sua organização do Office 365:
  
- **Etapa 1 (opcional)** - [Configurar grupos para supervisão](configure-supervision-policies.md#exampledist)

    Antes de começar a usar supervisão, determine quem serão suas comunicações revisou e quem executará as revisões. Se você deseja começar com apenas alguns usuários para ver como funciona a supervisão, você pode ignorar a configuração grupos por enquanto.

- **Etapa 2 (obrigatória)** - [tornar disponíveis em uma organização de supervisão](configure-supervision-policies.md#MakeAvailable)

    Adicione si mesmo ao grupo de funções de análise de supervisão, portanto, você pode configurar políticas. Qualquer pessoa que tenha essa função atribuída pode acessar a página de **supervisão** em **Dados governança** no Centro de conformidade do & de segurança. Se o email para ser revisadas está hospedada no Exchange Online, cada revisor também deve ter [acesso remoto do PowerShell para o Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/disable-access-to-exchange-online-powershell).

- **Etapa 3 (opcional)** - [Configurar tipos de informações confidenciais personalizado ou dicionários/dicionários de palavra-chave custom](configure-supervision-policies.md#sensitiveinfo)

    Se você precisar utilizar um tipo de informações confidenciais personalizado ou um dicionário personalizado de palavra-chave para a diretiva de supervisão, você precisará criá-lo antes de iniciar o Assistente de supervisão.

- **Etapa 4 (obrigatória)** - [definir uma política de supervisão](configure-supervision-policies.md#setupsuper)

    Você vai criar diretivas de supervisão no Centro de conformidade do & de segurança. Essas diretivas definem quais comunicações estão sujeitos a revisão na sua organização e especifica que deve executar as revisões. Comunicações incluem email e comunicações da Microsoft Teams, bem como as comunicações de plataforma de terceiros 3rd (por exemplo, Facebook, Twitter, etc.)

- **Etapa 5 - (opcional)** [Teste sua nova diretiva de supervisão](configure-supervision-policies.md#TestPolicy)

    Teste sua política de supervisão para certificar-se de que ele está funcionando conforme desejado é uma parte importante do garantindo que sua estratégia de conformidade é atender seus padrões.

- **Etapa 6: (opcional)** [Configurar o suplemento do Outlook para os revisores que não desejam usar o painel de supervisão do Office 365 ou no OWA para examinar comunicações supervisionadas](configure-supervision-policies.md#UseOutlook)

    O suplemento de supervisão para o Outlook oferece revisores acesso à direita supervisão funcionalidade dentro do cliente do Outlook para que eles possam avaliar e categorizar cada item.

<a name="exampledist"> </a>

## <a name="step-1---set-up-groups-for-supervision-optional"></a>Etapa 1: configurar grupos de supervisão (opcional)

 Quando você cria uma diretiva de supervisão, você determinará que terão suas comunicações analisadas e quem executará as revisões. Na política, você usará endereços de email para identificar indivíduos ou grupos de pessoas. Para simplificar sua instalação, crie grupos para as pessoas que terão sua comunicação analisada e grupos para as pessoas que analisará essas comunicações. Se você estiver usando grupos, talvez seja necessário várias — por exemplo, se você deseja monitorar as comunicações entre os dois grupos distintos de pessoas, ou se você deseja especificar um grupo que não vai ser supervisionados. Consulte [grupos de distribuição de exemplo](configure-supervision-policies.md#GroupExample) para obter detalhes sobre como isso funciona.
  
Para comunicações entre ou dentro de grupos na sua organização for o Supervisor, configurar os grupos de distribuição no Centro de administração do Exchange (vá em **destinatários** \> **grupos**). Para obter mais informações sobre como configurar grupos de distribuição, consulte [Gerenciar grupos de distribuição](http://go.microsoft.com/fwlink/?LinkId=613635)
  
> [!NOTE]
> Você também pode usar grupos dinâmicos de distribuição ou grupos de segurança para supervisão se você preferir. Para ajudá-lo a decidir se essas se ajuste melhor sua organização precisa, consulte [Gerenciar grupos de segurança habilitados para email](http://go.microsoft.com/fwlink/?LinkId=627033)e [Gerenciar grupos de distribuição dinâmica](http://go.microsoft.com/fwlink/?LinkId=627058).
  
<a name="GroupExample"> </a>

### <a name="example-distribution-groups"></a>Exemplos de grupos de distribuição

Este exemplo inclui um grupo de distribuição que foi configurado para uma organização financeira chamada internacional financeiro da Contoso.
  
Na Contoso Financial International, uma amostra das comunicações entre agentes nos Estados Unidos deve ser supervisionada. No entanto, os agentes de conformidade dentro desse grupo não exigem supervisão. Neste exemplo, podemos criar os seguintes grupos:
  
|**Configurar esse grupo de distribuição**|**Endereço do grupo (alias)**|**Descrição**|
|:-----|:-----|:-----|
|Todos os agentes dos EUA | US_Brokers@contoso.com | Esse grupo inclui endereços de email para todos os agentes dos EUA que trabalham para a Contoso. |
| Todos os agentes de conformidade dos EUA | US_Compliance@contoso.com  | Esse grupo inclui os endereços de email para todos os oficiais de conformidade com base nos EUA que trabalham para Contoso. Como este grupo é um subconjunto de todos os agentes baseada nos EUA, você pode usar este alias para responsáveis pela conformidade isentos de uma política de supervisão. |
  
<a name="MakeAvailable"> </a>

## <a name="step-2---make-supervision-available-in-your-organization-required"></a>Etapa 2: supervisão de tornar disponível na sua organização (obrigatória)

Para disponibilizar **supervisão** como uma opção de menu no Centro de conformidade do & de segurança, você deve ser atribuído a função de administrador de revisão de supervisão.
  
Para fazer isso, você pode adicionar si mesmo como membro do grupo de função da análise de supervisão, ou você pode criar um novo grupo de função.
  
### <a name="add-members-to-the-supervisory-review-role-group"></a>Adicionar membros ao grupo de funções de análise de supervisão

1. Entrar no [https://protection.office.com](https://protection.office.com) usando credenciais de uma conta de administrador em sua organização do Office 365.

2. No Centro de conformidade de segurança &, vá para **permissões**.

3. Selecione o grupo de funções de **Análise de supervisão** e, em seguida, clique no ícone Editar.

4. Na seção **membros** , adicione as pessoas que você deseja gerenciar supervisão para sua organização.

### <a name="create-a-new-role-group"></a>Criar um novo grupo de função

1. Entrar no [https://protection.office.com](https://protection.office.com) usando credenciais de uma conta de administrador em sua organização do Office 365.

2. No Centro de conformidade de segurança &, vá para **permissões** e clique em Adicionar (**+**).

3. Na seção **funções** , clique em Adicionar (**+**) e role para baixo até **Administrador supervisão de revisão**. Adicione essa função ao grupo de funções.

4. Na seção **membros** , adicione as pessoas que você deseja gerenciar supervisão para sua organização.

Para obter mais informações sobre grupos de funções e permissões, consulte [permissões no Office 365 Security &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md).

### <a name="enable-remote-powershell-access-for-reviewers-if-email-is-hosted-on-exchange-online"></a>Habilitar o acesso remoto do PowerShell para revisores (se o email está hospedada no Exchange Online)

1. Siga as orientações em [Habilitar ou desabilitar o acesso ao Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/disable-access-to-exchange-online-powershell).

<a name="sensitiveinfo"> </a>
  
## <a name="step-3---create-custom-sensitive-information-types-or-custom-keyword-dictionaries-optional"></a>Etapa 3: criar tipos de informações confidenciais personalizado ou dicionários personalizados de palavra-chave (opcional)

Para selecionar os tipos de informações confidenciais personalizadas existentes ou dicionários personalizados de palavra-chave no Assistente de diretiva de supervisão, você precisa primeiro criar estes itens, se necessário.

### <a name="create-custom-sensitive-information-types"></a>Criar tipos de informações confidenciais personalizadas

1. Crie um novo tipo de informações confidenciais no Centro de conformidade do & de segurança do Office 365. Navegue até **classificações** \> **tipos de informações confidenciais** e siga as etapas no **Assistente para novo tipo de informações confidenciais**. Aqui, você irá:

    - Definir um nome e uma descrição para o tipo de informações confidenciais
    - Definir a proximidade, nível de confiança e elementos padrão principal
    - Verifique suas seleções e criar o tipo de informações confidenciais

    Para obter informações mais detalhadas, consulte [criar um tipo de informação confidencial personalizado](create-a-custom-sensitive-information-type.md).

### <a name="create-custom-keyword-dictionarylexicon"></a>Criar um dicionário/dicionário de palavra-chave custom

1. Usando um editor de texto (como o bloco de notas), crie um novo arquivo que inclui os termos de palavra-chave que você gostaria de monitorar em uma diretiva de supervisão. Verifique se cada termo está em uma linha separada e salve o arquivo no formato **Unicode/UTF-16 (pouca Endian)** .
2. Importe o arquivo de palavra-chave para seu locatário do Office 365 usando o PowerShell. Para conectar ao Office 365 com o PowerShell, consulte [Connect to & de segurança do Office 365 PowerShell do Centro de conformidade](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).

    Depois de se conectar ao Office 365 com o PowerShell, execute os seguintes comandos para importar o dicionário de palavra-chave:

    ```
    $fileData = Get-Content "your keyword path and file name" -Encoding Byte -ReadCount 0

    New-DlpKeywordDictionary -Name "Name for your keyword dictionary" -Description "optional description for your keyword dictionary" -FileData $fileData
    ```
    Para obter informações mais detalhadas, consulte [criar um dicionário de palavra-chave](create-a-keyword-dictionary.md).

3. Crie um novo tipo de informações confidenciais no Centro de conformidade do & de segurança do Office 365. Navegue até **classificações** \> **tipos de informações confidenciais** e siga as etapas no **Assistente para novo tipo de informações confidenciais**. Aqui, você irá:

    - Definir um nome e uma descrição para o tipo de informações confidenciais
    - Adicionar dicionário personalizado como um requisito para o elemento correspondente
    - Verifique suas seleções e criar o tipo de informações confidenciais

    Depois que o dicionário/dicionário personalizado é criado, você pode exibir as palavras-chave configuradas usando o cmdlet [Get-DlpKeywordDictionary](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/get-dlpkeyworddictionary) ou adicionar e remover termos usando o cmdlet [Set-DlpKeywordDictionary](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/set-dlpkeyworddictionary) .

    Para obter informações mais detalhadas, consulte [criar um tipo de informação confidencial personalizado](create-a-custom-sensitive-information-type.md).

<a name="setupsuper"> </a>

## <a name="step-4---set-up-a-supervision-policy-required"></a>Etapa 4: configurar uma política de supervisão (obrigatória)
  
1. Entrar no [https://protection.office.com](https://protection.office.com) usando credenciais de uma conta de administrador em sua organização do Office 365.

2. No Centro de conformidade de segurança &, selecione **supervisão**.
  
3. Selecione **criar** e, em seguida, siga o Assistente para configurar as seguintes páginas da política. Usando o assistente, você irá:

    - Forneça um nome e descrição para a diretiva.
    - Escolha os usuários ou grupos for o Supervisor, incluindo a escolha de usuários ou grupos que você gostaria de excluir.
    - Defina as condições da diretiva de supervisão.
    - Escolha se você gostaria de incluir os tipos de informações confidenciais. Isso é onde você pode selecionar tipos de informações confidenciais personalizados e padrão.
    - Defina a porcentagem de comunicações para analisar.
    - Escolha os revisores para a política. Revisores podem ser usuários individuais ou [grupos de segurança habilitados para email](https://docs.microsoft.com/Exchange/recipients-in-exchange-online/manage-mail-enabled-security-groups#create-a-mail-enabled-security-group).
    - Verifique suas seleções de política e criar a política.

<a name="TestPolicy"> </a>

## <a name="step-5---test-your-supervision-policy-optional"></a>Etapa 5 - testar sua política de supervisão (opcional)

Depois de criar uma política de supervisão, é uma boa ideia fazer um teste para certificar-se de que as condições definidas por você estão sendo aplicadas corretamente pela política. Também convém [testar suas políticas de prevenção (DLP) de perda de dados](create-test-tune-dlp-policy.md) se suas diretivas de supervisão incluem os tipos de informações confidenciais. Siga as etapas abaixo para testar sua política de supervisão:

1. Abrir um cliente de email ou Microsoft Teams logado como um usuário supervisionado definido na política que você deseja testar.
2. Envie um email ou chat Teams da Microsoft que satisfaz os critérios que você definiu na diretiva de supervisão. Isso pode ser uma palavra-chave, o tamanho de anexo, o domínio, o etc. Certificar-se de que você determinar se as suas configurações condicionais na política é muito restritivo ou muito branda.

    > [!Note]
    > Emails sujeitos às políticas definidas são processadas na praticamente em tempo real e podem ser testadas imediatamente após a diretiva é configurada. Bate-papos no Microsoft Teams podem demorar até 24 horas para processar totalmente em uma política. 

3. Acesse seu locatário do Office 365 como um revisor designado na diretiva de supervisão. Navegue até **supervisão** > *Sua política de sinalizador* > **Open** para exibir o relatório para a política.

<a name="UseOutlook"> </a>

## <a name="step-6---set-up-outlook-add-in-for-reviewers-optional"></a>Etapa 6 - configurar o suplemento do Outlook para revisores (opcional)

Revisores que deseja usar o Outlook em vez de usar o painel de supervisão no Office 365 ou Outlook na web para examinar comunicações devem instalar o suplemento de supervisão para seus clientes Outlook.

### <a name="step-1-copy-the-address-for-the-supervision-mailbox"></a>Etapa 1: Copie o endereço da caixa de correio de supervisão

Para instalar o suplemento para desktop do Outlook, você precisará o endereço para a caixa de correio de supervisão que foi criada como parte da configuração da diretiva de supervisão.
  
> [!NOTE]
> Se alguém criou a política, você precisará obter esse endereço a partir deles para instalar o suplemento.

 **Para localizar o endereço da caixa de correio de supervisão**
  
1. Entrar no [segurança &amp; Centro de conformidade](https://protection.office.com) usando credenciais de uma conta de administrador em sua organização do Office 365.

2. Vá para **supervisão**.

3. Clique na política de supervisão que está juntando as comunicações que você deseja analisar.

4. No submenu de detalhes de política, sob a **caixa de correio de supervisão**, copie o endereço.<br/>![A seção de 'Caixa de correio de supervisão' do submenu de detalhes de uma diretiva de supervisão mostrando o endereço da caixa de correio de supervisão realçado](media/71779d0e-4f01-4dd3-8234-5f9c30eeb067.jpg)
  
### <a name="step-2-configure-the-supervision-mailbox-for-outlook-desktop-access"></a>Etapa 2: Configurar a caixa de correio de supervisão para acesso de área de trabalho do Outlook

Em seguida, os revisores precisará executar alguns comandos do PowerShell do Exchange Online para que eles possam se conectar à caixa de correio de supervisão.
  
1. Conecte-se para o Exchange Online PowerShell. [Como fazer isso?](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)

2. Execute os seguintes comandos, onde *SupervisoryReview{GUID}@domain.onmicrosoft.com* é o endereço que você copiou na etapa 1 acima, e o *usuário* é o nome do revisor que se conectarão à caixa de correio de supervisão na etapa 3.

    ```Add-MailboxPermission "SupervisoryReview{GUID}@domain.onmicrosoft.com" -User <alias or email address of the account that has reviewer permissions to the supervision mailbox> -AccessRights FullAccess```

    ```Set-Mailbox "<SupervisoryReview{GUID}@domain.onmicrosoft.com>" -HiddenFromAddressListsEnabled: $false```

3. Aguarde pelo menos uma hora antes de prosseguir para a etapa 3 abaixo.

### <a name="step-3-create-an-outlook-profile-to-connect-to-the-supervision-mailbox"></a>Etapa 3: Criar um perfil do Outlook para se conectar à caixa de correio de supervisão

Para a etapa final, serão necessário criar um perfil do Outlook para se conectar à caixa de correio de supervisão revisores.

> [!NOTE]
> Para criar um novo perfil do Outlook, você usará as configurações de email no painel de controle do Windows. O caminho que você tomar para chegar a essas configurações pode depender de qual sistema operacional do Windows (Windows 7, Windows 8 ou Windows 10) que você está usando e qual versão do Outlook está instalado.
  
1. Abra o painel de controle e, na caixa **Pesquisar** na parte superior da janela, digite o **email**.<br/>(Não tem certeza como chegar ao painel de controle? Consulte [onde está o painel de controle?](https://support.microsoft.com/help/13764/windows-where-is-control-panel))
  
2. Abra o aplicativo de **email** .

3. Em **Configurar email - Outlook**, clique em **Mostrar perfis**.<br/>!['Configurar email - Outlook' caixa de diálogo com o botão Mostrar perfis realçado](media/28b5dae9-d10c-4f2b-926a-294c857d555c.jpg)
  
4. No **email**, clique em **Adicionar**. Em seguida, em **Novo perfil**, digite um nome para a caixa de correio de supervisão (por exemplo, **supervisão**).<br/>![A caixa de diálogo 'Novo perfil' Mostrar o nome 'Supervisão' na caixa Nome do perfil](media/d02ae181-b541-4ec6-8f51-698f30033204.jpg)
  
5. No **Outlook se conectar ao Office 365**, clique em **Conectar para uma conta diferente**.<br/>![A mensagem 'Conectar o Outlook para o Office 365' com o link 'Conectar-se para uma conta diferente' realçado](media/fac49ff8-a7f0-4e82-a271-9ec045a95de1.jpg)
  
6. Na **Configuração automática de conta**, escolha a **instalação Manual ou tipos de servidor adicionais**e, em seguida, clique em **Avançar**.

7. Em **Escolha seu tipo de conta**, escolha o **Office 365**. Em seguida, na caixa **Endereço de Email** , digite o endereço da caixa de correio de supervisão que você copiou anteriormente.<br/>![A página 'Escolher o tipo de conta' da caixa de diálogo Adicionar conta no Outlook, mostrando a caixa de 'endereço de Email ' realçada.](media/4f601236-9f69-4cf6-a58c-0b91204aa8cb.jpg)
  
8. Quando solicitado, insira suas credenciais do Office 365.

9. Se tiver êxito, você verá o **supervisão - \<nome da política\> ** pasta listada no modo de exibição lista de pastas no Outlook.

## <a name="powershell-reference"></a>Referência do PowerShell

Se necessário, você pode criar e gerenciar diretivas de supervisão usando os cmdlets PowerShell a seguir:

- [New-SupervisoryReviewPolicyV2](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-supervisoryreviewpolicyv2?view=exchange-ps)
- [Get-SupervisoryReviewPolicyV2](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/get-supervisoryreviewpolicyv2?view=exchange-ps)
- [Set-SupervisoryReviewPolicyV2](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/set-supervisoryreviewpolicyv2?view=exchange-ps)
- [Remove-SupervisoryReviewPolicyV2](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/remove-supervisoryreviewpolicyv2?view=exchange-ps)
- [New-SupervisoryReviewRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-supervisoryreviewrule?view=exchange-ps)
- [Set-SupervisoryReviewRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/set-supervisoryreviewrule?view=exchange-ps)
- [Get-SupervisoryReviewActivity](https://docs.microsoft.com/powershell/module/exchange/reporting/get-supervisoryreviewactivity)
- [Get-SupervisoryReviewOverallProgressReport](https://docs.microsoft.com/powershell/module/exchange/reporting/get-supervisoryreviewoverallprogressreport)
- [Get-SupervisoryReviewTopCasesReport](https://docs.microsoft.com/powershell/module/exchange/reporting/get-supervisoryreviewtopcasesreport)
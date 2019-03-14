---
title: Configurar políticas de supervisão para sua organização
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.SupervisoryReview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
- MOE150
ms.assetid: d14ae7c3-fcb0-4a03-967b-cbed861bb086
description: Configurar uma política de análise de supervisão para capturar comunicações de funcionários para revisão.
ms.openlocfilehash: 2e321989934402b833d6190f65d696f4eb7919ca
ms.sourcegitcommit: 547a05da067a8f66fdaccf1cc399afcf863f5a87
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/07/2019
ms.locfileid: "30474152"
---
# <a name="configure-supervision-policies-for-your-organization"></a>Configurar políticas de supervisão para sua organização

Use políticas de supervisão para capturar comunicações de funcionários para verificação por revisores internos ou externos. Para obter mais informações sobre como as políticas de supervisão podem ajudá-lo a monitorar as comunicações em sua organização, consulte [políticas de supervisão no Office 365](supervision-policies.md).

> [!NOTE]
> Os usuários monitorados pelas políticas de supervisão devem ter uma licença de conformidade do Microsoft 365 e5, uma licença do Office 365 Enterprise E3 com o complemento de conformidade avançada ou ser incluída em uma assinatura do Office 365 Enterprise e5.
Se você não tem um plano Enterprise E5 existente e deseja tentar a supervisão, você pode [se inscrever para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).
  
Siga estas etapas para configurar e usar a supervisão na sua organização do Office 365:
  
- **Etapa 1 (opcional)** - [configurar grupos de supervisão](configure-supervision-policies.md#exampledist)

    Antes de começar a usar a supervisão, determine quem terá suas comunicações revisadas e quem executará essas análises. Se você quiser começar com apenas alguns usuários para ver como a supervisão funciona, você pode ignorar a configuração de grupos por enquanto.

- **Etapa 2 (obrigatório)** - [tornar a supervisão disponível em sua organização](configure-supervision-policies.md#MakeAvailable)

    Adicione a si mesmo ao grupo de função de análise de supervisão para que você possa configurar políticas. Qualquer pessoa que tenha essa função atribuída pode acessar a página de **supervisão** sob **governança de dados** no centro de conformidade do & de segurança. Se o email a ser revisado estiver hospedado no Exchange Online, cada revisor também deverá ter [acesso ao PowerShell remoto para o Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/disable-access-to-exchange-online-powershell).

- **Etapa 3 (opcional)** - [Configure tipos de informações confidenciais personalizados ou dicionários de palavras-chave personalizados](configure-supervision-policies.md#sensitiveinfo) e léxicos

    Se você precisar usar um tipo de informação confidencial personalizado ou um dicionário de palavras-chave personalizado para sua política de supervisão, você precisará criá-lo antes de iniciar o assistente de supervisão.

- **Etapa 4 (obrigatório)** - [Configurar uma política de supervisão](configure-supervision-policies.md#setupsuper)

    Você criará políticas de supervisão no centro de conformidade do & de segurança. Essas políticas definem quais comunicações estão sujeitas a revisar em sua organização e especifica quem deve realizar revisões. As comunicações incluem email e comunicações do Microsoft Teams, bem como comunicações de plataforma de terceiros (como Facebook, Twitter, etc.)

- **Etapa 5-(opcional)** [Testar sua nova política de supervisão](configure-supervision-policies.md#TestPolicy)

    Testar sua política de supervisão para garantir que esteja funcionando conforme o desejado é uma parte importante da garantia de que sua estratégia de conformidade esteja atendendo aos padrões.

- **Etapa 6-(opcional)** [Configurar o Outlook para revisores que não desejam usar o painel de supervisão do Office 365 ou o Outlook na Web (anteriormente conhecido como Outlook Web App) para examinar comunicações supervisionadas](configure-supervision-policies.md#UseOutlook)

    O Outlook pode ser configurado para dar aos revisores o acesso à funcionalidade de supervisão no cliente do Outlook para que eles possam avaliar e categorizar cada item.

<a name="exampledist"> </a>

## <a name="step-1---set-up-groups-for-supervision-optional"></a>Etapa 1-configurar grupos de supervisão (opcional)

 Ao criar uma política de supervisão, você determinará quem terá suas comunicações revisadas e quem executará essas análises. Na política, você usará endereços de email para identificar pessoas ou grupos de pessoas. Para simplificar a configuração, crie grupos para pessoas que terão suas comunicações revisadas e grupos para pessoas que examinarão essas comunicações. Se você estiver usando grupos, poderá precisar de vários — por exemplo, se quiser monitorar as comunicações entre dois grupos distintos de pessoas ou se quiser especificar um grupo que não será supervisionado. ConFira [exemplos de grupos de distribuição](configure-supervision-policies.md#GroupExample) para obter detalhes sobre como isso funciona.
  
Para supervisionar as comunicações entre ou dentro de grupos da sua organização, configure os grupos de distribuição no centro de administração do Exchange (vá para **grupos**de **destinatários** \> ). Para obter mais informações sobre como configurar grupos de distribuição, consulte [Manage Distribution groups](http://go.microsoft.com/fwlink/?LinkId=613635)
  
> [!NOTE]
> Você também pode usar grupos de distribuição dinâmica ou grupos de segurança para supervisão, se preferir. Para ajudá-lo a decidir se esses melhores atendem às necessidades da sua organização, confira [gerenciar grupos de segurança habilitados para email](http://go.microsoft.com/fwlink/?LinkId=627033)e [gerenciar grupos dinâmicos de distribuição](http://go.microsoft.com/fwlink/?LinkId=627058).
  
<a name="GroupExample"> </a>

### <a name="example-distribution-groups"></a>Exemplos de grupos de distribuição

Este exemplo inclui um grupo de distribuição que foi configurado para uma organização financeira chamada contoso Financial International.
  
Na Contoso Financial International, uma amostra das comunicações entre agentes nos Estados Unidos deve ser supervisionada. No entanto, os agentes de conformidade dentro desse grupo não exigem supervisão. Neste exemplo, podemos criar os seguintes grupos:
  
|**Configurar esse grupo de distribuição**|**Endereço do grupo (alias)**|**Descrição**|
|:-----|:-----|:-----|
|Todos os agentes dos EUA | US_Brokers@Contoso.com | Esse grupo inclui endereços de email para todos os agentes dos EUA que trabalham para a Contoso. |
| Todos os agentes de conformidade dos EUA | US_Compliance@Contoso.com  | Esse grupo inclui endereços de email para todos os agentes de conformidade dos EUA que trabalham para a Contoso. Como esse grupo é um subconjunto de todos os agentes baseados nos EUA, você pode usar esse alias para isentar os responsáveis pela conformidade de uma política de supervisão. |
  
<a name="MakeAvailable"> </a>

## <a name="step-2---make-supervision-available-in-your-organization-required"></a>Etapa 2-tornar a supervisão disponível em sua organização (obrigatório)

Para tornar a **supervisão** disponível como uma opção de menu no centro de conformidade do _AMP_ de segurança, você deve receber a função de administrador de análise de supervisão.
  
Para fazer isso, você pode adicionar a si mesmo como um membro do grupo de função de análise de supervisão ou pode criar um novo grupo de função.
  
### <a name="add-members-to-the-supervisory-review-role-group"></a>Adicionar membros ao grupo de função de análise de supervisão

1. Entre [https://protection.office.com](https://protection.office.com) usando as credenciais de uma conta de administrador na sua organização do Office 365.

2. No centro de conformidade do & de segurança, acesse **permissões**.

3. Selecione o grupo de função de **análise de supervisão** e clique no ícone Editar.

4. Na seção **Membros** , adicione as pessoas que você deseja gerenciar a supervisão da sua organização.

### <a name="create-a-new-role-group"></a>Criar um novo grupo de função

1. Entre [https://protection.office.com](https://protection.office.com) usando as credenciais de uma conta de administrador na sua organização do Office 365.

2. No centro de conformidade do & de segurança, acesse **permissões** e clique em**+** adicionar ().

3. Na seção **funções** , clique em Adicionar (**+**) e role para baixo até **administrador de análise de supervisão**. Adicione esta função ao grupo de função.

4. Na seção **Membros** , adicione as pessoas que você deseja gerenciar a supervisão da sua organização.

Para obter mais informações sobre grupos de funções e permissões, consulte [permissões no centro de &amp; conformidade de segurança do Office 365](permissions-in-the-security-and-compliance-center.md).

### <a name="enable-remote-powershell-access-for-reviewers-if-email-is-hosted-on-exchange-online"></a>Habilitar o acesso ao PowerShell remoto para revisores (se o email estiver hospedado no Exchange Online)

1. Siga as orientações em [habilitar ou desabilitar o acesso ao PowerShell do Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/disable-access-to-exchange-online-powershell).

<a name="sensitiveinfo"> </a>
  
## <a name="step-3---create-custom-sensitive-information-types-or-custom-keyword-dictionaries-optional"></a>Etapa 3: criar tipos de informações confidenciais personalizados ou dicionários de palavras-chave personalizados (opcional)

Para escolher entre os tipos de informações confidenciais personalizadas existentes ou os dicionários de palavras-chave personalizados no assistente de política de supervisão, primeiro você precisará criar esses itens, se necessário.

### <a name="create-custom-sensitive-information-types"></a>Criar tipos de informações confidenciais personalizados

1. Crie um novo tipo de informação confidencial no centro de conformidade do & de segurança do Office 365. Navegue até **classificações** \> de **tipos de informações confidenciais** e siga as etapas no **Assistente novo tipo de informação confidencial**. Aqui você irá:

    - Definir um nome e uma descrição para o tipo de informações confidenciais
    - Definir os elementos de proximidade, nível de confiança e padrão primário
    - ReVisar suas seleções e criar o tipo de informações confidenciais

    Para obter informações mais detalhadas, consulte [criar um tipo de informação confidencial personalizado](create-a-custom-sensitive-information-type.md).

### <a name="create-custom-keyword-dictionarylexicon"></a>Criar dicionário de palavras-chave personalizado/léxico

1. Usando um editor de texto (como o bloco de notas), crie um novo arquivo que inclui os termos de palavra-chave que você gostaria de monitorar em uma política de supervisão. Certifique-se de que cada termo está em uma linha separada e salve o arquivo no formato **Unicode/UTF-16 (little endian)** .
2. Importe o arquivo de palavra-chave para o seu locatário do Office 365 usando o PowerShell. Para conectar-se ao Office 365 com o PowerShell, confira [Connect to office 365 Security _AMP_ Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).

    Depois de se conectar ao Office 365 com o PowerShell, execute os seguintes comandos para importar seu dicionário de palavra-chave:

    ```
    $fileData = Get-Content "your keyword path and file name" -Encoding Byte -ReadCount 0

    New-DlpKeywordDictionary -Name "Name for your keyword dictionary" -Description "optional description for your keyword dictionary" -FileData $fileData
    ```
    Para obter informações mais detalhadas, consulte [criar um dicionário de palavras-chave](create-a-keyword-dictionary.md).

3. Crie um novo tipo de informação confidencial no centro de conformidade do & de segurança do Office 365. Navegue até **classificações** \> de **tipos de informações confidenciais** e siga as etapas no **Assistente novo tipo de informação confidencial**. Aqui você irá:

    - Definir um nome e uma descrição para o tipo de informações confidenciais
    - Adicionar seu dicionário personalizado como um requisito para o elemento correspondente
    - ReVisar suas seleções e criar o tipo de informações confidenciais

    Depois que o dicionário personalizado/léxico é criado, você pode exibir as palavras-chave configuradas usando o cmdlet [Get-DlpKeywordDictionary](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/get-dlpkeyworddictionary) ou adicionar e remover termos usando o cmdlet [set-DlpKeywordDictionary](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/set-dlpkeyworddictionary) .

    Para obter informações mais detalhadas, consulte [criar um tipo de informação confidencial personalizado](create-a-custom-sensitive-information-type.md).

<a name="setupsuper"> </a>

## <a name="step-4---set-up-a-supervision-policy-required"></a>Etapa 4-configurar uma política de supervisão (obrigatório)
  
1. Entre [https://protection.office.com](https://protection.office.com) usando as credenciais de uma conta de administrador na sua organização do Office 365.

2. No centro de conformidade do & de segurança, selecione **supervisão**.
  
3. Selecione **criar** e siga o assistente para configurar as seguintes páginas da política. Usando o assistente, você irá:

    - Forneça um nome e uma descrição para a política.
    - Escolha os usuários ou grupos para supervisionar, incluindo a escolha de usuários ou grupos que você gostaria de excluir.
    - Definir as condições da política de supervisão.
    - Escolha se você deseja incluir tipos de informações confidenciais. É aí que você pode selecionar os tipos de informações confidenciais padrão e personalizadas.
    - Defina a porcentagem de comunicação a ser revisada.
    - Escolha os revisores da política. Os revisores podem ser usuários individuais ou [grupos de segurança habilitados para email](https://docs.microsoft.com/Exchange/recipients-in-exchange-online/manage-mail-enabled-security-groups#create-a-mail-enabled-security-group).
    - Revise suas seleções de política e crie a política.

<a name="TestPolicy"> </a>

## <a name="step-5---test-your-supervision-policy-optional"></a>Etapa 5: testar sua política de supervisão (opcional)

Depois de criar uma política de supervisão, é uma boa ideia testar para garantir que as condições definidas estejam sendo aplicadas corretamente pela política. Você também pode querer [testar suas políticas de DLP (prevenção de perda de dados)](create-test-tune-dlp-policy.md) se suas políticas de supervisão incluírem tipos de informações confidenciais. Siga as etapas abaixo para testar sua política de supervisão:

1. Abra um cliente de email ou o Microsoft Teams conectado como um usuário supervisionado definido na política que você deseja testar.
2. Envie um email ou chat do Microsoft Teams que atendam aos critérios definidos na política de supervisão. Pode ser uma palavra-chave, o tamanho do anexo, o domínio, etc. Certifique-se de determinar se as configurações condicionais configuradas na política estão muito restritivas ou Lenient.

    > [!Note]
    > Os emails sujeitos às políticas definidas são processados quase em tempo real e podem ser testados imediatamente após a configuração da política. Os chats no Microsoft Teams podem levar até 24 horas para processar totalmente em uma política. 

3. Faça logon em seu locatário do Office 365 como um revisor designado na política de supervisão. Navegue até a **supervisão** > da*política* > personalizada**aberta** para exibir o relatório da política.

<a name="UseOutlook"> </a>

## <a name="step-6---configure-outlook-for-reviewers-optional"></a>Etapa 6: configurar o Outlook para revisores (opcional)

Os revisores que desejam usar o Outlook em vez de usar o painel de supervisão no Office 365 para rever as comunicações devem configurar o cliente do Outlook.

### <a name="step-1-copy-the-address-for-the-supervision-mailbox"></a>Etapa 1: copiar o endereço da caixa de correio de supervisão

Para configurar a revisão do Outlook para a área de trabalho do Outlook para a Web, você precisará do endereço da caixa de correio de supervisão criada como parte da configuração da política de supervisão.
  
> [!NOTE]
> Se outra pessoa criou a política, você precisará obter esse endereço deles para instalar o suplemento.

 **Para localizar o endereço da caixa de correio de supervisão**
  
1. Entre no [centro de &amp; conformidade de segurança](https://protection.office.com) usando credenciais para uma conta de administrador na sua organização do Office 365.

2. Vá até **supervisão**.

3. Clique na política de supervisão que está coletando as comunicações que você deseja revisar.

4. No submenu detalhes da política, em **caixa de correio de supervisão**, copie o endereço.<br/>![A seção "caixa de correio de supervisão" do submenu de detalhes da política de supervisão mostrando o endereço da caixa de correio de supervisão realçada](media/71779d0e-4f01-4dd3-8234-5f9c30eeb067.jpg)
  
### <a name="step-2-configure-the-supervision-mailbox-for-outlook-access"></a>Etapa 2: configurar a caixa de correio de supervisão para o acesso do Outlook

Em seguida, os revisores precisarão executar alguns comandos do PowerShell do Exchange Online para que eles possam conectar o Outlook à caixa de correio de supervisão.
  
1. Conectar-se ao Exchange Online PowerShell. [Como faço isso?](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)

2. Execute os seguintes comandos, onde *SupervisoryReview {GUID} @domain. onmicrosoft.com* é o endereço que você copiou na etapa 1 acima, e *User* é o nome do revisor que será conectado à caixa de correio de supervisão na etapa 3.

    ```Add-MailboxPermission "SupervisoryReview{GUID}@domain.onmicrosoft.com" -User <alias or email address of the account that has reviewer permissions to the supervision mailbox> -AccessRights FullAccess```

    ```Set-Mailbox "<SupervisoryReview{GUID}@domain.onmicrosoft.com>" -HiddenFromAddressListsEnabled: $false```

3. Aguarde pelo menos uma hora antes de passar para a etapa 3 abaixo.

### <a name="step-3-create-an-outlook-profile-to-connect-to-the-supervision-mailbox"></a>Etapa 3: criar um perfil do Outlook para se conectar à caixa de correio de supervisão

Para a etapa final, os revisores precisarão criar um perfil do Outlook para se conectar à caixa de correio de supervisão.

> [!NOTE]
> Para criar um novo perfil do Outlook, você usará as configurações de email no painel de controle do Windows. O caminho que você leva para acessar essas configurações pode depender de qual sistema operacional Windows (Windows 7, Windows 8 ou Windows 10) você está usando e qual versão do Outlook está instalada.
  
1. Abra o painel de controle e, na caixa de **pesquisa** na parte superior da janela, digite **email**.<br/>(Não sabe como acessar o painel de controle? Veja [onde está o painel de controle?](https://support.microsoft.com/help/13764/windows-where-is-control-panel))
  
2. Abra o aplicativo de **email** .

3. Em **configuração de email-Outlook**, clique em **Mostrar perfis**.<br/>![A caixa de diálogo "configuração de email-Outlook" com o botão "mostrar perfis" realçado](media/28b5dae9-d10c-4f2b-926a-294c857d555c.jpg)
  
4. Em **email**, clique em **Adicionar**. Em seguida, em **novo perfil**, insira um nome para a caixa de correio de supervisão (como **supervisão**).<br/>![A caixa de diálogo "novo perfil" mostrando o nome "supervisão" na caixa "nome do perfil"](media/d02ae181-b541-4ec6-8f51-698f30033204.jpg)
  
5. Em **conectar o Outlook ao Office 365**, clique em **conectar a uma conta diferente**.<br/>![A mensagem "conectar o Outlook ao Office 365" com o link "conectar a uma conta diferente" realçado](media/fac49ff8-a7f0-4e82-a271-9ec045a95de1.jpg)
  
6. Em **configuração automática de conta**, escolha **configuração manual ou tipos de servidor adicionais**e clique em **Avançar**.

7. Em **escolher o tipo de conta**, escolha **Office 365**. Em seguida, na caixa **endereço de email** , digite o endereço da caixa de correio de supervisão que você copiou anteriormente.<br/>![A página ' escolha o tipo de conta ' da caixa de diálogo ' adicionar conta ' no Outlook mostrando a caixa ' endereço de email ' realçada.](media/4f601236-9f69-4cf6-a58c-0b91204aa8cb.jpg)
  
8. Quando solicitado, insira suas credenciais do Office 365.

9. Se tiver êxito, você verá a pasta de **nome \<\> de política de supervisão** listada no modo de exibição lista de pastas no Outlook.

## <a name="powershell-reference"></a>Referência do PowerShell

Se necessário, você pode criar e gerenciar políticas de supervisão usando os seguintes cmdlets do PowerShell:

- [New-SupervisoryReviewPolicyV2](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-supervisoryreviewpolicyv2?view=exchange-ps)
- [Get-SupervisoryReviewPolicyV2](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/get-supervisoryreviewpolicyv2?view=exchange-ps)
- [Set-SupervisoryReviewPolicyV2](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/set-supervisoryreviewpolicyv2?view=exchange-ps)
- [Remove-SupervisoryReviewPolicyV2](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/remove-supervisoryreviewpolicyv2?view=exchange-ps)
- [New-SupervisoryReviewRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-supervisoryreviewrule?view=exchange-ps)
- [Set-SupervisoryReviewRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/set-supervisoryreviewrule?view=exchange-ps)
- [Get-SupervisoryReviewActivity](https://docs.microsoft.com/powershell/module/exchange/reporting/get-supervisoryreviewactivity)
- [Get-SupervisoryReviewOverallProgressReport](https://docs.microsoft.com/powershell/module/exchange/reporting/get-supervisoryreviewoverallprogressreport)
- [Get-SupervisoryReviewTopCasesReport](https://docs.microsoft.com/powershell/module/exchange/reporting/get-supervisoryreviewtopcasesreport)
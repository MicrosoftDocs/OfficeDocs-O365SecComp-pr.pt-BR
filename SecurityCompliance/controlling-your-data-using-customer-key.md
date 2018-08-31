---
title: Controlar seus dados no Office 365 usando a Chave do cliente
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 7/2/2018
ms.audience: ITPro
ms.topic: get-started-article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f2cd475a-e592-46cf-80a3-1bfb0fa17697
description: Saiba como configurar o chave de cliente para o Office 365 para Exchange Online, Skype para negócios, SharePoint Online e OneDrive for Business. Com a chave do cliente, você controlar as chaves de criptografia da sua organização e configurar o Office 365 para usá-los para criptografar dados em repouso em centros de dados da Microsoft.
ms.openlocfilehash: f8d7c12c32ca74b842f676f4a2ccde4d1c758361
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22559226"
---
# <a name="controlling-your-data-in-office-365-using-customer-key"></a>Controlar seus dados no Office 365 usando a Chave do cliente

Com a chave do cliente, você controlar as chaves de criptografia da sua organização e configurar o Office 365 para usá-los para criptografar dados em repouso em centros de dados da Microsoft. Dados em repouso incluem os dados do Exchange Online e do Skype for Business que é armazenado em caixas de correio e arquivos que são armazenados no SharePoint Online e o OneDrive for Business.
  
Você deve configurar o Azure antes de poder usar chave do cliente para o Office 365. Este tópico descreve as etapas que precisam ser seguidas para criar e configurar os recursos necessários do Windows Azure e então fornece as etapas para configurar a chave do cliente no Office 365. Após concluir a instalação do Azure, você deve determinar qual política e, portanto, quais teclas, para atribuir a caixas de correio e arquivos na sua organização. Caixas de correio e de arquivos para os quais você não atribuir uma política usará as diretivas de criptografia que são controladas e gerenciadas pela Microsoft. Para obter mais informações sobre a chave do cliente, ou para obter uma visão geral, consulte a [Chave do cliente para perguntas Frequentes do Office 365](service-encryption-with-customer-key-faq.md).
  
> [!IMPORTANT]
> É altamente recomendável que você siga as práticas recomendadas descritas neste tópico. Estes são chamados check-out como **Dica** e **importante**. Dá de chave do cliente controle sobre as chaves de criptografia de raiz cujo escopo pode ser tão grande quanto toda sua organização. Isso significa que cometidos com essas chaves podem ter um impacto amplo e podem resultar em interrupções do serviço ou perda irreversível dos seus dados. 
  
## <a name="before-you-begin-setting-up-customer-key"></a>Antes de começar a configurar a chave do cliente
<a name="Beforeyoustart"> </a>

Antes de começar, certifique-se de que você tem o licenciamento apropriado para sua organização. Chave do cliente no Office 365 é oferecida no Office 365 E5 ou a SKU de conformidade avançadas.
  
Em seguida, para entender os conceitos e procedimentos neste tópico, você deve consultar a documentação do [Windows Azure chave Vault](https://azure.microsoft.com/en-us/documentation/services/key-vault/) . Além disso, familiarize-se com os termos usados no Windows Azure, por exemplo, o [inquilino](https://msdn.microsoft.com/library/azure/jj573650.aspx#BKMK_WhatIsAnAzureADTenant).
  
Para fornecer comentários sobre a chave do cliente, incluindo a documentação, envie suas ideias, sugestões e perspectivas para customerkeyfeedback@microsoft.com.
  
## <a name="overview-of-setting-up-customer-key-for-office-365"></a>Visão geral da configuração de chave de cliente para o Office 365
<a name="Overview"> </a>

Para configurar a chave do cliente, você concluirá essas tarefas. O restante deste tópico fornece instruções detalhadas para cada tarefa ou links check-out para obter mais informações para cada etapa do processo.
  
**No Windows Azure e FastTrack da Microsoft:**
  
Você concluirá maioria dessas tarefas conectando remotamente ao PowerShell do Windows Azure. Para obter melhores resultados, use versão 4.4.0 ou posterior do Azure PowerShell.
  
- [Criar duas novas inscrições Azure](controlling-your-data-using-customer-key.md#Create2newsubs)
    
- [Registrar o Azure inscrições para usar um período de retenção obrigatória](controlling-your-data-using-customer-key.md#RegisterSubsforMRP)
    
    Registro pode levar de um a cinco dias úteis.
    
- [Enviar uma solicitação para ativar a chave do cliente para o Office 365](controlling-your-data-using-customer-key.md#FastTrack)
    
    Depois que você criou as duas novas inscrições Azure, você precisará enviar a solicitação de oferta de chave de cliente apropriada, completando um formulário da web que é hospedado no portal do Microsoft FastTrack. A equipe de FastTrack não prestar assistência com chave de cliente. Office simplesmente usa o portal de FastTrack para permitir que você envie o formulário e nos ajudar a controlar as ofertas relevantes para a chave do cliente.
  
Depois que você enviou uma oferta de chave de cliente, o Microsoft analisa sua solicitação e notifica você quando você pode continuar com o restante das tarefas de instalação. Esse processo pode levar até cinco dias úteis.
    
- [Criar um premium Azure chave Vault em cada uma assinatura](controlling-your-data-using-customer-key.md#CreateKeyVault)
    
- [Atribuir permissões a cada vault principal](controlling-your-data-using-customer-key.md#KeyVaultPerms)
    
- [Habilitar e Confirmar exclusão reversível na suas chaves compartimentos](controlling-your-data-using-customer-key.md#SoftDelete)
    
- [Adicionar uma chave para cada chave vault tanto criando ou importando uma chave](controlling-your-data-using-customer-key.md#AddKeystoKeyVault)
    
- [Marque o nível de recuperação de suas chaves](controlling-your-data-using-customer-key.md#CheckKeyRecoveryLevel)
    
- [Backup Vault Azure de chave](controlling-your-data-using-customer-key.md#BackupAzureKeyVaultkeys)
    
- [Validar as definições de configuração de armazenamento de chave do Windows Azure](controlling-your-data-using-customer-key.md#Validateconfiguration)
    
- [Obter o URI para cada chave Vault de chave do Windows Azure](controlling-your-data-using-customer-key.md#GetKeyURI)
    
**No Office 365:**
  
Exchange Online e Skype para negócios:
  
- [Criar uma política de criptografia de dados (DEP) para uso com o Exchange Online e Skype para negócios](controlling-your-data-using-customer-key.md#CreateDEP4EXOSkype)
    
- [Atribuir um DEP a uma caixa de correio](controlling-your-data-using-customer-key.md#assignDEPtomailbox)
    
- [Validar a criptografia de caixa de correio](controlling-your-data-using-customer-key.md#validatemailboxencryption)
    
SharePoint Online e o OneDrive for Business:
  
- [Criar uma diretiva de criptografia de dados (DEP) para cada SharePoint Online e o OneDrive for Business geo](controlling-your-data-using-customer-key.md#CreateDEP4SPOODfB)
    
- [Validar a criptografia do grupo de Sites, Sites de equipe e OneDrive for Business](controlling-your-data-using-customer-key.md#validateencryptionSPO)
    
## <a name="complete-tasks-in-azure-key-vault-and-microsoft-fasttrack-for-customer-key"></a>Concluir tarefas no Azure chave Vault e Microsoft FastTrack para a chave do cliente
<a name="AzureSteps"> </a>

Conclua essas tarefas no Azure chave Vault para configurar a chave de cliente para o Office 365. Você precisará concluir essas etapas, independentemente se você pretende configurar chave do cliente para o Exchange Online e Skype para negócios ou SharePoint Online e OneDrive for Business ou para todos os serviços com suporte no Office 365.
  
### <a name="create-two-new-azure-subscriptions"></a>Criar duas novas inscrições Azure
<a name="Create2newsubs"> </a>

Duas assinaturas Azure são necessárias para a chave do cliente. Como prática recomendada, a Microsoft recomenda que você crie novas inscrições Azure para uso com a chave do cliente. Chaves de chave Vault Azure só podem ser autorizadas para aplicativos no mesmo inquilino do Azure Active Directory (AAD), você deve criar as novas inscrições usando o mesmo inquilino Azure AD usado com a sua organização do Office 365 onde os DEPs serão atribuídos. Por exemplo, usando sua conta de trabalho ou da escola que tenha privilégios de administrador global na sua organização do Office 365. Para obter etapas detalhadas, consulte [inscrever-se no Azure como uma organização](https://azure.microsoft.com/en-us/documentation/articles/sign-up-organization/).
  
> [!IMPORTANT]
> Chave de cliente exige duas chaves para cada política de criptografia de dados (DEP). Para conseguir isso, você deve criar dois assinaturas do Azure. Como prática recomendada, a Microsoft recomenda que você tenha separados membros da sua organização configurar uma chave em cada uma assinatura. Além disso, essas assinaturas Azure só devem ser usadas para administrar as chaves de criptografia para o Office 365. Isso protege a sua organização no caso de um dos seus operadores acidentalmente, intencionalmente ou modo mal-intencionado exclui ou mismanages caso contrário, as chaves para os quais eles são responsáveis.<br/> Recomendamos que você configure novas inscrições Azure que são usadas exclusivamente para gerenciar recursos de armazenamento de chave do Windows Azure para uso com chave de cliente. Não há nenhum limite prático para o número de inscrições Azure que podem ser criados para sua organização. Estas práticas recomendadas minimizará o impacto de erro humano e ajudar a gerenciar os recursos usados pela chave do cliente. 
  
### <a name="submit-a-request-to-activate-customer-key-for-office-365"></a>Enviar uma solicitação para ativar a chave do cliente para o Office 365
<a name="FastTrack"> </a>

Depois de ter concluído as etapas do Azure, você precisará enviar uma solicitação de oferta no [portal do Microsoft FastTrack](https://fasttrack.microsoft.com/). Depois que você enviou uma solicitação por meio do portal da web FastTrack, Microsoft verifica as informações Azure chave Vault de dados e o contato configuração fornecidas por você. As seleções feitas no formato oferta relacionadas as oficiais autorizados da sua organização é necessário para a conclusão do registro da chave de cliente e não críticas. Os oficiais da sua organização que você seleciona no formulário será o valor usado para assegurar a autenticidade de qualquer solicitação revogar e destruir todas as chaves usadas com uma diretiva de criptografia de dados de chave do cliente. Você precisará executar esta etapa uma vez para ativar a chave de cliente do Exchange Online e Skype para cobertura de negócios e uma segunda vez ativar a chave do cliente para o SharePoint Online e o OneDrive for Business.
  
Para enviar uma oferta para ativar a chave do cliente, conclua estas etapas:
  
1. Usando uma conta de trabalho ou da escola que tenha permissões de administrador global na sua organização do Office 365, faça logon no [portal do Microsoft FastTrack](https://fasttrack.microsoft.com/).
    
2. Depois que você está logado, navegue até o **painel**.
    
3. Escolha **oferece**e examine a lista de ofertas atuais.
    
4. Escolha **Saiba mais** oferta do que se aplica a você: 
    
  - **Exchange Online e Skype for Business:** Escolha **Saiba mais** sobre a oferta de **Chave de cliente do Exchange** . 
    
  - **SharePoint Online e o OneDrive for Business:** Escolher **Saiba mais** sobre a oferta de **Chave de cliente para SharePoint e o OneDrive for Business** . 
    
5. Na página **detalhes da oferta** , escolha **Criar a solicitação**.
    
6. Preencha todos os detalhes aplicáveis e as informações solicitadas no formulário oferta. Preste atenção para suas seleções para quais oficiais da sua organização para o qual você deseja autorizar para aprovar a destruição permanente e irreversível de chaves de criptografia e dados. Depois de ter concluído o formulário, escolha **Enviar**.
    
    Esse processo pode levar até cinco dias de negócios depois que a Microsoft foi notificado da sua solicitação.
    
7. Prosseguir para a seção de período de retenção obrigatória abaixo.
    
### <a name="register-azure-subscriptions-to-use-a-mandatory-retention-period"></a>Registrar o Azure inscrições para usar um período de retenção obrigatória
<a name="RegisterSubsforMRP"> </a>

A perda temporária ou permanente de chaves de criptografia de raiz pode ser muito destrutivos ou até mesmo catastrófica a operação de serviço e pode resultar em perda de dados. Por esse motivo, os recursos usados com a chave de cliente exigem proteção de alta segurança. Todos os recursos do Azure que são usados com a chave de cliente oferecem mecanismos de proteção além da configuração padrão. Assinaturas do Azure podem ser marcadas ou registradas de forma que impedirá o cancelamento imediato e irrevogável. Isso é conhecido como registrando por um período de retenção obrigatória. As etapas necessárias para registrar o Azure inscrições por um período de retenção obrigatória exigem colaboração com a equipe do Office 365. Esse processo pode levar de um a cinco dias úteis. Anteriormente, isso era às vezes conhecido como "Não cancelar".
  
Antes de contatar a equipe do Office 365, você deve executar as seguintes etapas para cada assinatura Azure que você pode usar com a chave de cliente:
  
1. Faça logon em sua assinatura do Windows Azure com o Azure PowerShell. Para obter instruções, consulte [entrar nas Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).
    
2. Execute o cmdlet Register-AzureRmProviderFeature para registrar suas assinaturas para usar um período de retenção obrigatória.
    
  ```
  Register-AzureRmProviderFeature -FeatureName mandatoryRetentionPeriodEnabled -ProviderNamespace Microsoft.Resources
  ```

3. Contate a Microsoft para que o processo finalizado. Para o SharePoint e o OneDrive para a equipe de negócios, contate [spock@microsoft.com](mailto:spock@microsoft.com). Para o Exchange Online e Skype para a empresa, contate [exock@microsoft.com](mailto:exock@microsoft.com). O contrato de nível de serviço (SLA) para a conclusão desse processo é cinco dias úteis depois que a Microsoft foi notificado (e verificou) que você registrou suas assinaturas para usar um período de retenção obrigatória. Inclua o seguinte no seu email:
    
    **Assunto**: chave do cliente para \< *nome de domínio totalmente qualificado de seu locatário*\> 
    
    **Corpo**: IDs de assinatura para o qual você deseja ter o obrigatória finalizada período de retenção. 
    
4. Depois de receber a notificação da Microsoft que registro está concluído, verifique o status do seu registro executando o cmdlet Get-AzureRmProviderFeature da seguinte maneira:
    
  ```
  Get-AzureRmProviderFeature -ProviderNamespace Microsoft.Resources -FeatureName mandatoryRetentionPeriodEnabled
  ```

5. Depois de verificar se a propriedade **Estado do registro** do cmdlet Get-AzureRmProviderFeature retorna um valor de **Registered**, execute o seguinte comando para concluir o processo:
    
  ```
  Register-AzureRmResourceProvider -ProviderNamespace "Microsoft.KeyVault"
  ```

### <a name="create-a-premium-azure-key-vault-in-each-subscription"></a>Criar um premium Azure chave Vault em cada uma assinatura
<a name="CreateKeyVault"> </a>

As etapas para criar um armazenamento de chave estão documentadas no [Guia de Introdução ao Windows Azure chave Vault](https://azure.microsoft.com/documentation/articles/key-vault-get-started/), que lhe orienta durante a instalação e lançar o Azure PowerShell, conectando-se a sua assinatura do Windows Azure, criando um grupo de recursos e criando um armazenamento de chave em que grupo de recursos.
  
Quando você cria um armazenamento de chave, você deve escolher uma SKU: Standard ou Premium. A SKU Standard permite que as chaves do Azure chave Vault devem ser protegidos com o software - não há nenhuma proteção de chave do módulo de segurança de Hardware (HSM) - e a SKU Premium permite o uso de HSMs para proteção de chave Vault chaves. Chave de cliente aceita compartimentos principais que usam qualquer SKU, embora a Microsoft recomenda que você use apenas a SKU Premium. O custo das operações com chaves de qualquer tipo é o mesmo, portanto, a única diferença no custo é o custo por mês para cada chave HSM protegidas. Para obter detalhes, consulte [chave Vault preços](https://azure.microsoft.com/pricing/details/key-vault/) . 
  
> [!IMPORTANT]
> Use os compartimentos de chave Premium SKU e protegidos HSM as chaves para dados de produção e use apenas compartimentos principais de SKU Standard e chaves para fins de teste e validação. 
  
Para cada serviço do Office 365 com os quais você usará a chave de cliente, crie um armazenamento de chave em cada uma das duas inscrições Azure que você criou. Por exemplo, para o Exchange Online e Skype para negócios apenas ou SharePoint Online e o OneDrive for Business apenas, você criará somente um par de compartimentos. Para habilitar a chave de cliente para o Exchange Online e SharePoint Online, você irá criar dois pares de chaves compartimentos.
  
Use uma convenção de nomenclatura para compartimentos principais que reflete o uso pretendido da DEP com os quais você irá associar os compartimentos. Consulte a seção de práticas recomendadas abaixo recomendações da convenção de nomenclatura.
  
Crie um conjunto de compartimentos para cada política de criptografia de dados separado e emparelhado. Para o Exchange Online, o escopo de uma diretiva de criptografia de dados é escolhido por você ao atribuir a diretiva de caixa de correio. Uma caixa de correio pode ter apenas uma política atribuída e você pode criar até cinquenta diretivas. Para o SharePoint Online, o escopo de uma diretiva é todos os dados em uma organização em uma localização geográfica ou geo.
  
A criação de chaves compartimentos também requer a criação de grupos de recursos do Windows Azure, desde que compartimentos principais precisam de capacidade de armazenamento (embora muito pequeno) e Vault da chave de registro em log, se for habilitada, também gera dados armazenados. Como prática recomendada a Microsoft recomenda usar o administradores separados para gerenciar cada grupo de recursos, com a administração alinhada com o conjunto de administradores que irá gerenciar todos os recursos relacionados da chave de cliente.
  
> [!IMPORTANT]
> Para maximizar a disponibilidade, a suas chaves compartimentos devem ficar em regiões e está perto do seu serviço do Office 365. Por exemplo, se sua organização do Exchange Online for na América do Norte, coloque a suas chaves compartimentos na América do Norte. Se sua organização do Exchange Online for na Europa, coloque a suas chaves compartimentos na Europa.<br/>Use um prefixo comum para compartimentos chaves e incluir o escopo das principal vault e chaves e uma abreviação do uso (por exemplo, para o serviço de Contoso SharePoint onde os compartimentos estará localizados na América do Norte, um par de possível de nomes é Contoso-O365SP-NA-VaultA1 e Contoso-O365SP-NA-VaultA2. Nomes Vault são cadeias de caracteres globalmente exclusivas dentro do Azure, portanto, talvez você precise tente variações de seus nomes desejados, caso os nomes desejados já estão solicitados por outros clientes do Azure. A partir de julho de 2017 vault nomes não podem ser alterados, portanto, uma prática recomendada é ter um plano por escrito para a instalação e usar uma segunda pessoa para verificar que o plano é executado corretamente.<br/>Se possível, crie seus compartimentos em regiões não emparelhada. Emparelhados regiões Azure fornecem alta disponibilidade entre domínios de falha de serviço. Portanto, pares regionais podem ser considerados região backup uns dos outros. Isso significa que um recurso Azure que é colocado em uma região está ganhando automaticamente a tolerância a falhas por meio da região emparelhada. Por esse motivo, escolhendo áreas para dois compartimentos usados em um DEP onde as regiões são emparelhadas significa que apenas um total de duas regiões de disponibilidade estão em uso. Maioria das regiões têm apenas duas regiões, portanto, ele ainda não é possível selecionar regiões não emparelhada. Se possível, escolha duas regiões não emparelhada para os dois compartimentos usados com um DEP. Isso se beneficia de um total de quatro áreas de disponibilidade. Para obter mais informações, consulte [Business continuity e recuperação de desastres (BCDR): Azure emparelhada regiões](https://docs.microsoft.com/azure/best-practices-availability-paired-regions) para obter uma lista atual de pares regionais. 
  
### <a name="assign-permissions-to-each-key-vault"></a>Atribuir permissões a cada vault principal
<a name="KeyVaultPerms"> </a>

Para cada chave vault, você precisará definir três conjuntos de permissões para a chave do cliente, dependendo da sua implementação separados. Por exemplo, você precisará definir um conjunto de permissões para cada um dos seguintes procedimentos:
  
- **Os administradores de armazenamento de chave** que executará o gerenciamento diário da sua chave vault para sua organização. Essas tarefas incluem o backup, criar, obtém, importar, lista e restaurar. 
    
    > [!IMPORTANT]
    > O conjunto de permissões atribuídas aos administradores vault chave não inclui a permissão para excluir chaves. Isso é intencional e uma prática importante. Excluindo as chaves de criptografia não é geralmente feito, desde que fazer então permanentemente destruir dados. Como prática recomendada, não conceda essa permissão aos administradores vault principais por padrão. Em vez disso, reservar isso para colaboradores da chave vault e apenas atribuí-la a um administrador em uma base de curto prazo depois que uma compreensão clara das consequências é compreendida. 
  
    Para atribuir essas permissões a um usuário em sua organização do Office 365, faça logon em sua assinatura do Windows Azure com o Azure PowerShell. Para obter instruções, consulte [entrar nas Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).
    
- Execute o cmdlet Set-AzureRmKeyVaultAccessPolicy para atribuir as permissões necessárias.
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> 
  -UserPrincipalName <UPN of user> -PermissionsToKeys create,import,list,get,backup,restore
  ```

  Por exemplo:
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
  -UserPrincipalName alice@contoso.com -PermissionsToKeys create,import,list,get,backup,restore
  ```

- **Os colaboradores vault chave** que pode alterar permissões no compartimento de chave do Windows Azure em si. Você precisará alterar essas permissões, como funcionários saírem ou entrarem sua equipe ou na situação extremamente rara que a tecla compartimentalizar administradores legitimamente precisam de permissão para excluir ou restaurar uma chave. Este conjunto de colaboradores da chave vault precisa ser concedido a função de **Colaborador** em sua chave vault. Você pode atribuir essa função usando o Gerenciador de recursos do Windows Azure. Para obter etapas detalhadas, consulte [Use Role-Based de controle de acesso para gerenciar o acesso aos seus recursos de assinatura do Windows Azure](https://docs.microsoft.com/azure/active-directory/role-based-access-control-configure). O administrador que cria uma assinatura tem esse acesso implicitamente, bem como a capacidade de atribuir a outros administradores à função de Colaborador.
    
- Se você pretende usar chave do cliente com o Exchange Online e Skype for Business, você precisa conceder permissão para o Office 365 para usar o chave vault em nome do Exchange Online e Skype para negócios. Da mesma forma, se você pretende usar a chave de cliente com o SharePoint Online e o OneDrive for Business, você precisará adicionar a permissão para o Office 365 usar o chave vault em nome do SharePoint Online e o OneDrive for Business. Para conceder permissão para o Office 365, execute o cmdlet **Set-AzureRmKeyVaultAccessPolicy** usando a seguinte sintaxe: 
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName <Office 365 appID>
  ```

    Onde:
    
  - *vaultname* é o nome do chave vault que você criou. 
    
  - Para o Exchange Online e Skype para os negócios, substitua *appID do Office 365* com`00000002-0000-0ff1-ce00-000000000000`
    
  - Para o SharePoint Online e OneDrive for Business, substitua *appID do Office 365* com`00000003-0000-0ff1-ce00-000000000000`
    
  Exemplo: Definindo permissões para o Exchange Online e Skype para negócios:
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
  -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000002-0000-0ff1-ce00-000000000000
  ```

  Exemplo: Definindo permissões para o SharePoint Online e o OneDrive for Business
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365SP-NA-VaultA1 
  -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000003-0000-0ff1-ce00-000000000000
  ```

### <a name="enable-and-then-confirm-soft-delete-on-your-key-vaults"></a>Habilitar e Confirmar exclusão reversível na suas chaves compartimentos
<a name="SoftDelete"> </a>

Quando você pode recuperar rapidamente suas chaves, são menos suscetíveis a experiência de uma interrupção de serviço estendido devido às teclas de modo mal-intencionado ou acidentalmente excluídas. Você precisará habilitar essa configuração, conhecida como excluir suave, antes de poder usar as chaves com chave de cliente. Habilitando a excluir suave permite que você recupere compartimentos ou chaves dentro de 90 dias da exclusão sem precisar restaurá-los a partir do backup.
  
Para habilitar a excluir suave na suas chaves compartimentos, conclua estas etapas:
  
1. Faça logon em sua assinatura do Windows Azure com o Windows Powershell. Para obter instruções, consulte [entrar nas Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps).
    
2. Execute o cmdlet [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/azurerm.keyvault/get-azurermkeyvault) . Neste exemplo, *vaultname* é o nome do chave vault para o qual você está habilitando exclusão reversível: 
    
   ```
   $v = Get-AzureRmKeyVault -VaultName <vaultname>
   $r = Get-AzureRmResource -ResourceId $v.ResourceId
   $r.Properties | Add-Member -MemberType NoteProperty -Name enableSoftDelete -Value 'True'
   Set-AzureRmResource -ResourceId $r.ResourceId -Properties $r.Properties
   ``` 
    
3. Confirme a exclusão reversível está configurado para o chave vault executando o cmdlet **Get-AzureRmKeyVault** . Se a exclusão reversível está configurada corretamente para o armazenamento de chave, o Soft excluir habilitado? propriedade retorna um valor **True**: 
    
   ```
   Get-AzureRmKeyVault -VaultName <vaultname> | fl
   ```

   
    
### <a name="add-a-key-to-each-key-vault-either-by-creating-or-importing-a-key"></a>Adicionar uma chave para cada chave vault tanto criando ou importando uma chave
<a name="AddKeystoKeyVault"> </a>

Existem duas maneiras de adicionar chaves para um armazenamento de chave do Azure; Você pode criar uma chave diretamente no compartimento de chave, ou você pode importar uma chave. Criando uma chave diretamente no compartimento de chave é o método menos complicado, enquanto importando uma chave fornece um controle total sobre como a chave é gerada.
  
Para criar uma chave diretamente no seu vault principal, execute o cmdlet [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey) da seguinte maneira: 
  
```
Add-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname> -Destination <HSM|Software> -KeyOps wrapKey,unwrapKey
```

Onde:
  
-  *vaultname* é o nome do chave vault no qual você deseja criar a chave. 
    
-  *nome chave* é o nome que você deseja conceder a nova chave. 
    
    > [!TIP]
    > Chaves de nome usando uma convenção de nomenclatura semelhante, conforme descrito acima para compartimentos principais. Dessa forma, nas ferramentas que mostram apenas o nome da chave, a cadeia de caracteres é Self descrevendo. 
  
- Se você pretende proteger a chave com um HSM, certifique-se de que você especifique **HSM** como o valor do parâmetro de _destino_ , caso contrário, especifique a **Software**.
    
Por exemplo,
  
```
Add-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -Destination Software -KeyOps wrapKey,unwrapKey
```

Para importar uma chave diretamente para sua chave vault, você precisa ter um nShield Thales módulo de segurança de Hardware.
  
Algumas organizações preferem essa abordagem para estabelecer o provenance de suas chaves e este método também fornece os seguintes:
  
- O conjunto de ferramentas usado para importação inclui certificação de Thales não é exportável a chave Exchange chave KEK que é usado para criptografar a chave que é gerar e é gerado dentro de um genuíno HSM que foi fabricado pela Thales.
    
- O conjunto de ferramentas inclui certificação de Thales que o mundo da segurança do Windows Azure chave Vault também foi gerado em um genuíno HSM fabricado pela Thales. Essa certificação prova a você que Microsoft também está usando hardware de Thales autêntico.
    
Verifique com seu grupo de segurança para determinar se o attestations acima são necessárias. Para obter etapas detalhadas criar uma chave local e importá-lo para a sua chave vault, consulte [como gerar e transferir chaves protegidas HSM para armazenamento de chave do Windows Azure](https://azure.microsoft.com/documentation/articles/key-vault-hsm-protected-keys/). Use as instruções Azure para criar uma chave em cada compartimento principal.
  
### <a name="check-the-recovery-level-of-your-keys"></a>Marque o nível de recuperação de suas chaves
<a name="CheckKeyRecoveryLevel"> </a>

O Office 365 exige que a assinatura do Windows Azure chave Vault está definida como não cancelar e se as teclas usadas pela chave cliente tem como exclusão reversível habilitado. Você pode confirmar isso examinando o nível de recuperação em suas chaves.
  
Para verificar o nível de recuperação de uma chave, no Azure PowerShell, execute o cmdlet Get-AzureKeyVaultKey da seguinte maneira:
  
```
(Get-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname>).Attributes 
```

Se a propriedade de _Nível de recuperação_ retornar qualquer coisa diferente de um valor de **Recuperável + ProtectedSubscription**, você precisará analisar este tópico e certifique-se de ter seguido todas as etapas para colocar a assinatura na lista não cancelar e que você tenha habilitado em cada um dos seus principais compartimentos como exclusão reversível.
  
### <a name="backup-azure-key-vault"></a>Backup Vault Azure de chave
<a name="BackupAzureKeyVaultkeys"> </a>

Imediatamente após a criação ou qualquer alteração a uma chave, execute um backup e armazenar cópias do backup, online e offline. Cópias offline não devem estar conectadas para qualquer rede, como em um recurso de armazenamento físico de seguros ou comerciais. Pelo menos uma cópia de backup deve ser armazenada em um local que será acessível em caso de desastre. Os blobs backup são os meios exclusivo de restaurar o material da chave deve uma chave de chave Vault ser destruída permanentemente ou caso contrário, inoperante. Chaves que são externos para armazenamento de chave do Windows Azure e foram importadas para armazenamento de chave do Windows Azure não qualificados como um backup porque os metadados necessários para a chave do cliente usar a chave não existe com a chave externa. Somente um backup extraído do Azure chave Vault pode ser usado para operações de restauração com chave de cliente. Portanto, é essencial que um backup do Windows Azure chave Vault sejam feitas depois que uma chave é carregada ou criada.
  
Para criar um backup de uma chave de armazenamento de chave do Windows Azure, execute o cmdlet [Backup-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Backup-AzureKeyVaultKey) da seguinte maneira:
```
Backup-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname> 
-OutputFile <filename .backup>

```

Certifique-se de que o seu arquivo de saída usa o sufixo `.backup`.
  
O arquivo de saída resultante desse cmdlet é criptografado e não pode ser usado fora do Azure chave Vault. O backup pode ser restaurado somente a partir do qual foi feito o backup de assinatura do Azure.
  
> [!TIP]
> Para o arquivo de saída, escolha uma combinação de seu nome de armazenamento e o nome da chave. Isso fará com que o arquivo nome definido de forma automática. Ele também assegurará que os nomes de arquivo de backup não coincidem. 
  
Por exemplo:
  
```
Backup-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -OutputFile Contoso-O365EX-NA-VaultA1-Key001-Backup-20170802.backup
```

### <a name="validate-azure-key-vault-configuration-settings"></a>Validar as definições de configuração de armazenamento de chave do Windows Azure
<a name="Validateconfiguration"> </a>

Executar a validação antes de usar um DEP chaves é opcional, mas altamente recomendado. Em particular, se você usar as etapas para configurar chaves e compartimentos que seja diferente dos descritos neste tópico, você deve validar a integridade de seus recursos do Windows Azure chave Vault antes de configurar a chave do cliente.
  
Para verificar que sua chaves têm operações get, wrapKey e unwrapKey habilitadas:
  
Execute o cmdlet [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureRmKeyVault) da seguinte maneira: 
  
```
Get-AzureRMKeyVault -VaultName <vaultname>
```

Na saída, procure para a política de acesso e para a identidade (GUID) do Exchange Online ou a identidade do SharePoint Online (GUID), conforme apropriado. Todos os três das permissões acima devem ser mostrados em permissões às chaves.
  
Se a configuração de política de acesso estiver incorreta, execute o cmdlet Set-AzureRmKeyVaultAccessPolicy da seguinte maneira:
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName <Office 365 appID>
```

Por exemplo, para o Exchange Online e Skype para negócios:
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
-PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000002-0000-0ff1-ce00-000000000000
```

Por exemplo, para o SharePoint Online e OneDrive for Business:
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365SP-NA-VaultA1 
-PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName TBD
```

Para verificar se uma data de validade não está definida para essas chaves, executados o cmdlet [Get-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureKeyVaultKey) da seguinte maneira: 
  
```
Get-AzureKeyVaultKey -VaultName <vaultname> 
```

Uma chave expirada não pode ser usada pela chave cliente e operações tentadas com uma chave expirada irá falhar e possivelmente resultar em uma interrupção de serviço. É altamente recomendável que chaves usadas com a chave do cliente não têm uma data de validade. Uma data de expiração, depois que set, não podem ser removidas, mas pode ser alterada para uma data diferente. Se uma chave deve ser usada com uma data de validade definido, altere o valor de expiração para 31/12/9999. Chaves com uma data de validade é definido como uma data diferente de 31/12/9999 não passará a validação do Office 365.
  
Para alterar uma data de validade tiver sido definida como qualquer valor diferente de 31/12/9999, execute o cmdlet [Set-AzureKeyVaultKeyAttribute](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Set-AzureKeyVaultKeyAttribute) da seguinte maneira: 
  
```
Set-AzureKeyVaultKeyAttribute -VaultName <vaultname> -Name <keyname> 
-Expires (Get-Date -Date "12/31/9999")
```

> [!CAUTION]
> Não defina datas de expiração sobre chaves de criptografia, que você pode usar com a chave do cliente. 
  
### <a name="obtain-the-uri-for-each-azure-key-vault-key"></a>Obter o URI para cada chave Vault de chave do Windows Azure
<a name="GetKeyURI"> </a>

Depois de ter concluído todas as etapas no Windows Azure para configurar suas chaves compartimentos e adicionou seus chaves, execute o seguinte comando para obter o URI para a chave em cada compartimento principal. Você precisará usar esses URIs quando você cria e atribuir cada DEP posteriormente, portanto, salve essas informações em um local seguro. Lembre-se de executar esse comando uma vez para cada chave vault.
  
No PowerShell do Azure:
  
```
(Get-AzureKeyVaultKey -VaultName <vaultname>).Id
```

## <a name="office-365-setting-up-customer-key-for-exchange-online-and-skype-for-business"></a>Office 365: Configurando a chave do cliente para o Exchange Online e Skype para negócios
<a name="AzureSteps"> </a>

Antes de começar, certifique-se de que você concluiu as tarefas necessárias para configurar o armazenamento de chave do Windows Azure. Consulte [Concluir tarefas no Azure chave Vault e Microsoft FastTrack para a chave do cliente](controlling-your-data-using-customer-key.md#AzureSteps) para obter informações. 
  
Para configurar a chave do cliente para o Exchange Online e Skype for Business, você precisará executar estas etapas conectando remotamente ao Exchange Online com o Windows PowerShell.
  
### <a name="create-a-data-encryption-policy-dep-for-use-with-exchange-online-and-skype-for-business"></a>Criar uma política de criptografia de dados (DEP) para uso com o Exchange Online e Skype para negócios
<a name="CreateDEP4EXOSkype"> </a>

Um DEP é associado um conjunto de chaves armazenadas no compartimento de chave do Windows Azure. Você pode atribuir um DEP uma caixa de correio no Office 365. O Office 365, em seguida, usará as teclas identificadas na política para criptografar a caixa de correio. Para criar a DEP, você precisa ter os URIs de Vault chave tiver obtido anteriormente. Consulte [obter o URI para cada chave Azure chave Vault](controlling-your-data-using-customer-key.md#GetKeyURI) para obter instruções. 
  
Lembre-se! Quando você cria um DEP, você pode especificar duas chaves que residem em dois compartimentos diferentes de chave do Azure. Certifique-se de que essas chaves estão localizados em duas regiões Azure separados para garantir a redundância de geo.
  
Para criar a DEP, siga estas etapas:
  
1. No computador local, usando uma conta de trabalho ou da escola que tenha permissões de administrador global na sua organização do Office 365, [se conectar ao Exchange Online PowerShell](https://technet.microsoft.com/en-us/library/jj984289%28v=exchg.160%29.aspx) abrindo o Windows PowerShell e executando o seguinte comando. 
    
   ```
   $UserCredential = Get-Credential
   ```

2. Na caixa de diálogo solicitação de credencial do Windows PowerShell, insira seu trabalho ou escola informações da conta, clique **Okey**e, em seguida, insira o seguinte comando. 
    
   ```
   $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://outlook.office365.com/powershell-liveid/ -Credential $UserCredential -Authentication Basic -AllowRedirection
   ```

3. Execute o seguinte comando.
    
   ```
   Import-PSSession $Session
   ```

4. Para criar um DEP, use o cmdlet New-DataEncryptionPolicy digitando o seguinte comando.
    
   ```
   New-DataEncryptionPolicy -Name <PolicyName> -Description "PolicyDescription " -AzureKeyIDs <KeyVaultURI1>, <KeyVaultURI2>
   ```

   Onde:
    
   -  *PolicyName* é o nome que você deseja usar para a política. Nomes não podem conter espaços. Por exemplo, USA_mailboxes. 
    
   -  *PolicyDescription* é uma descrição amigável da política que o ajudará a se lembrar o que é a política por. Você pode incluir espaços na descrição. Por exemplo, raiz chave para caixas de correio nos Estados Unidos e seus territórios. 
    
   -  *KeyVaultURI1* é o URI para a primeira chave na política. Por exemplo, https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01. 
    
   -  *KeyVaultURI2* é o URI para a segunda chave na política. Por exemplo, https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02. Separe os URIs de dois por uma vírgula e um espaço. 
    
   Exemplo:
  
   ```
   New-DataEncryptionPolicy -Name USA_mailboxes -Description "Root key for mailboxes in USA and its territories" -AzureKeyIDs https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01, https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02
   ```

### <a name="assign-a-dep-to-a-mailbox"></a>Atribuir um DEP a uma caixa de correio
<a name="assignDEPtomailbox"> </a>

Atribua a DEP a uma caixa de correio usando o cmdlet Set-Mailbox. Depois de atribuir a política, o Office 365 pode criptografar a caixa de correio com a chave designada na DEP.
  
```
Set-Mailbox -Identity <MailboxIdParameter> -DataEncryptionPolicy <PolicyName>
```

Onde *MailboxIdParameter* Especifica uma caixa de correio. Para obter mais informações sobre o cmdlet Set-Mailbox, consulte [Set-Mailbox](https://technet.microsoft.com/library/bb123981%28v=exchg.160%29.aspx).
  
### <a name="validate-mailbox-encryption"></a>Validar a criptografia de caixa de correio
<a name="validatemailboxencryption"> </a>

Criptografar uma caixa de correio pode levar algum tempo. Para atribuição de política de tempo primeira, a caixa de correio também deverá concluir a movimentação de um banco de dados para outro antes que o serviço pode criptografar a caixa de correio. Recomendamos que você aguardar 72 horas antes de tentar validar criptografia depois que você alterar um DEP ou na primeira vez que você atribua um DEP uma caixa de correio.
  
Use o cmdlet Get-MailboxStatistics para determinar se uma caixa de correio é criptografada.
  
```
Get-MailboxStatistics -Identity <GeneralMailboxOrMailUserIdParameter> | fl IsEncrypted
```

A propriedade IsEncrypted retorna um valor de **true** se a caixa de correio é criptografada e um valor **false** se a caixa de correio não é criptografada. 

O tempo para concluir as movimentações de caixa de correio depende do número de caixas de correio à qual você atribui um DEP pela primeira vez, bem como o tamanho das caixas de correio. Se as caixas de correio não foram criptografadas depois de uma semana desde o momento em que você atribuiu a DEP, inicie uma movimentação de caixa de correio para as caixas de correio não criptografadas usando o cmdlet New-MoveRequest.

```
New-MoveRequest <mailbox alias>
``` 

## <a name="office-365-setting-up-customer-key-for-sharepoint-online-and-onedrive-for-business"></a>Office 365: Configurando a chave do cliente para o SharePoint Online e o OneDrive for Business
<a name="AzureSteps"> </a>

Antes de começar, certifique-se de que você concluiu as tarefas necessárias para configurar o armazenamento de chave do Windows Azure. Consulte [Concluir tarefas no Azure chave Vault e Microsoft FastTrack para a chave do cliente](controlling-your-data-using-customer-key.md#AzureSteps) para obter informações. 
  
Para configurar a chave do cliente para o SharePoint Online e o OneDrive for Business, você precisará executar estas etapas conectando remotamente ao SharePoint Online com o Windows PowerShell.
  
### <a name="create-a-data-encryption-policy-dep-for-each-sharepoint-online-and-onedrive-for-business-geo"></a>Criar uma diretiva de criptografia de dados (DEP) para cada SharePoint Online e o OneDrive for Business geo
<a name="CreateDEP4SPOODfB"> </a>

Um DEP é associado um conjunto de chaves armazenadas no compartimento de chave do Windows Azure. Você pode aplicar um DEP para todos os seus dados em uma localidade geográfica, também chamada de um geo. Se você usar o recurso de multi-geo do Office 365 (atualmente na visualização), você pode criar um DEP por geo. Se você não estiver usando multi-geo, você pode criar um DEP no Office 365 para uso com o SharePoint Online e o OneDrive for Business. O Office 365, em seguida, usará as teclas identificadas na DEP para criptografar dados em que geo. Para criar a DEP, você precisa ter os URIs de Vault chave tiver obtido anteriormente. Consulte [obter o URI para cada chave Azure chave Vault](controlling-your-data-using-customer-key.md#GetKeyURI) para obter instruções. 
  
Lembre-se! Quando você cria um DEP, você pode especificar duas chaves que residem em dois compartimentos diferentes de chave do Azure. Certifique-se de que essas chaves estão localizados em duas regiões Azure separados para garantir a redundância de geo.
  
Para criar um DEP, você precisará conectar-se remotamente ao SharePoint Online usando o Windows PowerShell.
  
1. No computador local, usando uma conta de trabalho ou da escola que tenha permissões de administrador global na sua organização do Office 365, [se conectar ao Powershell do SharePoint Online](https://technet.microsoft.com/library/fp161372.aspx).
    
2. No Microsoft SharePoint Online Management Shell, execute o cmdlet [Register-SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843950.aspx) da seguinte maneira: 
    
   ```
   Register-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl> -PrimaryKeyVaultName <PrimaryKeyVaultName> -PrimaryKeyName <PrimaryKeyName> -PrimaryKeyVersion <PrimaryKeyVersion> -SecondaryKeyVaultName <SecondaryKeyVaultName> -SecondaryKeyName <SecondaryKeyName> -SecondaryKeyVersion <SecondaryKeyVersion>
   ```

   Ao registrar a DEP, criptografia começa nos dados do geo. Isso pode levar algum tempo.
    
### <a name="validate-encryption-of-group-sites-team-sites-and-onedrive-for-business"></a>Validar a criptografia do grupo de Sites, Sites de equipe e OneDrive for Business
<a name="validateencryptionSPO"> </a>

Você pode verificar o status de criptografia, executando o cmdlet Get-SPODataEncryptionPolicy da seguinte maneira:
  
```
Get-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl>
```

A saída desse cmdlet inclui:
  
- O URI da chave primária.
    
- O URI da chave secundário.
    
- O status de criptografia para o geo. Estados possíveis incluem:
    
  - **Não registrados:** Criptografia de chave do cliente ainda não tiver sido aplicada. 
    
  - **Registrando:** Criptografia de chave do cliente tiver sido aplicada e seus arquivos estiverem sendo criptografado. Se seu geo estiver nesse estado, você vai também ser mostradas informações na qual o percentual de sites no geo forem concluídas, para que você pode monitorar o progresso de criptografia. 
    
  - **Registrado:** Criptografia de chave do cliente tiver sido aplicada e todos os arquivos em todos os sites foram criptografados. 
    
  - **Aplicação:** Uma chave roll está em andamento. Se seu geo estiver nesse estado, você vai também ser mostradas informações na qual o percentual de sites concluiu a operação roll principais para que você pode monitorar o andamento. 
    
## <a name="managing-customer-key-for-office-365"></a>Gerenciando a chave do cliente para o Office 365
<a name="ManageCustomerKey"> </a>

Depois que você definiu o backup da chave de cliente para o Office 365, você pode executar essas tarefas de gerenciamento adicionais.
  
- [Restaurar as chaves do Azure chave Vault](controlling-your-data-using-customer-key.md#RestoreAzureKeyVaultKeys)
    
- [Sem interrupção ou girando uma chave no Azure chave Vault que você pode usar com a chave do cliente](controlling-your-data-using-customer-key.md#RollCKkey)
    
- [Gerenciar permissões de chave vault](controlling-your-data-using-customer-key.md#Managekeyvaultperms)
    
- [Determinar a DEP atribuída a uma caixa de correio](controlling-your-data-using-customer-key.md#DeterminemailboxDEP)
    
### <a name="restore-azure-key-vault-keys"></a>Restaurar as chaves do Azure chave Vault
<a name="RestoreAzureKeyVaultKeys"> </a>

Antes de executar uma restauração, use os recursos de recuperação fornecidos pela exclusão reversível. Todas as chaves que são usadas com a chave do cliente serão necessárias ter habilitada como exclusão reversível. Exclusão reversível funciona como uma Lixeira e permite a recuperação por até 90 dias sem a necessidade de restauração. Restore só deve ser necessário em circunstâncias extremas ou incomuns, por exemplo, se a tecla ou vault chave for perdido. Se precisar restaurar uma chave para uso com a chave do cliente no Azure PowerShell, execute o cmdlet Restore-AzureKeyVaultKey da seguinte maneira:
  
```
Restore-AzureKeyVaultKey -VaultName <vaultname> -InputFile <filename>
```

Por exemplo:
  
```
Restore-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -InputFile Contoso-O365EX-NA-VaultA1-Key001-Backup-20170802.backup
```

Se uma chave com o mesmo nome já existir no compartimento principal, haverá falha na operação de restauração. Restore-AzureKeyVaultKey restaura todas as versões principais e todos os metadados para a chave, incluindo o nome da chave.
  
### <a name="rolling-or-rotating-a-key-in-azure-key-vault-that-you-use-with-customer-key"></a>Sem interrupção ou girando uma chave no Azure chave Vault que você pode usar com a chave do cliente
<a name="RollCKkey"> </a>

Aplicação de chaves não é necessário por qualquer um dos Vault de chave do Windows Azure ou por chave de cliente. Além disso, as chaves são protegidas com um HSM são praticamente impossíveis comprometer. Mesmo se uma chave raiz estavam em posse de um ator mal-intencionado não há nenhum significa viável de usá-lo para descriptografar os dados, desde que apenas o Office 365 código sabe como usá-lo. No entanto, a aplicação de uma chave é suportado pela chave do cliente.
  
> [!CAUTION]
> Rolo apenas uma chave de criptografia que usados com a chave do cliente quando existe um motivo desmarque técnico ou um requisito de conformidade dita que você precisa aplicar a chave. Além disso, não exclua todas as chaves que estão ou estavam associadas a políticas. Quando você distribuir seu chaves, haverá a ser conteúdo criptografado com as chaves anteriores. Por exemplo, enquanto caixas de correio ativas serão novamente criptografadas com frequência, inativa, caixas de correio desconectadas e desabilitadas ainda podem ser criptografadas com as chaves anteriores. SharePoint Online executa backup de conteúdo para fins de restauração e recuperação, portanto talvez ainda haja conteúdo arquivado usando as teclas mais antigas.<br/> Para garantir a segurança dos seus dados, SharePoint Online permitirá que não mais de uma operação de chave rolo estejam em andamento por vez. Se você deseja implantar ambas as chaves de um armazenamento de chave, você precisará aguardar a primeira operação chave roll totalmente concluída. Nossa recomendação é escalonar suas operações roll principais em intervalos diferentes, para que isso não é um problema. 
  
Quando você lançar uma chave, você está solicitando uma nova versão de uma chave existente. Para solicitar uma nova versão de uma chave existente, você pode usar o mesmo cmdlet, [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey), com a mesma sintaxe que você usou para criar a chave em primeiro lugar.
  
Por exemplo:
  
```
Add-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -Destination HSM -KeyOps @('wrapKey','unwrapKey') -NotBefore (Get-Date -Date "12/27/2016 12:01 AM")
```

Neste exemplo, desde que uma chave chamada **Contoso-O365EX-NA-VaultA1-Key001** já existe no compartimento **Contoso-O365EX-NA-VaultA1** , uma nova versão chave será criada. A operação adiciona uma nova versão principal. Essa operação preserva as versões anteriores de chave no histórico de versão da chave, para que os dados criptografados anteriormente com essa chave ainda podem ser descriptografados. Depois de ter concluído sem interrupção qualquer tecla que está associada um DEP, você deve executar um cmdlet adicional para garantir a que chave de cliente começa usando a nova chave. 
  
#### <a name="enable-exchange-online-and-skype-for-business-to-use-a-new-key-after-you-roll-or-rotate-keys-in-azure-key-vault"></a>Habilitar o Exchange Online e Skype for Business para usar uma nova chave após reverter ou girar chaves no Azure chave Vault

Quando você distribuir um das chaves de Azure chave Vault associadas a um DEP usadas com o Exchange Online e Skype for Business, você deve executar o seguinte comando para atualizar a DEP e ativar o Office 365 começar a usar a nova chave.
  
Para instruir o chave do cliente para usar a nova chave para criptografar as caixas de correio no Office 365, execute o cmdlet Set-DataEncryptionPolicy da seguinte maneira:
  
```
Set-DataEncryptionPolicy <policyname> -Refresh 
```

Em 48 horas, as caixas de correio ativas criptografadas usando esta diretiva se tornará associadas com a chave atualizada. Use as etapas em [Determine a DEP atribuída a uma caixa de correio](controlling-your-data-using-customer-key.md#DeterminemailboxDEP) para verificar o valor da propriedade DataEncryptionPolicyID da caixa de correio. O valor dessa propriedade será alterado depois que a chave atualizada tiver sido aplicada. 
  
#### <a name="enable-sharepoint-online-and-onedrive-for-business-to-use-a-new-key-after-you-roll-or-rotate-keys-in-azure-key-vault"></a>Habilitar o SharePoint Online e OneDrive for Business para usar uma nova chave após reverter ou girar chaves no Azure chave Vault

Quando você distribuir um das chaves de Azure chave Vault associadas a um DEP usadas com o SharePoint Online e o OneDrive for Business, você deve executar o cmdlet [Update-SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843948.aspx) para atualizar a DEP e ativar o Office 365 começar a usar a nova chave. 
  
```
Update-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl> -KeyVaultName <ReplacementKeyVaultName> -KeyName <ReplacementKeyName> -KeyVersion <ReplacementKeyVersion> -KeyType <Primary | Secondary>
```

Isso iniciará a operação roll principais para o SharePoint Online e o OneDrive for Business. Esta ação não é imediata. Para ver o progresso da chave rolo operation, execute o cmdlet Get-SPODataEncryptionPolicy da seguinte maneira:
  
```
Get-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl>
```

### <a name="manage-key-vault-permissions"></a>Gerenciar permissões de chave vault
<a name="Managekeyvaultperms"> </a>

Vários cmdlets estão disponíveis que permitem que você exiba e, se necessário, remover permissões de chave vault. Talvez seja necessário remover permissões, por exemplo, quando um funcionário deixa a equipe.
  
Para exibir as permissões de chave vault, execute o cmdlet Get-AzureRmKeyVault:
  
```
Get-AzureRmKeyVault -VaultName <vaultname>
```

Por exemplo:
  
```
Get-AzureRmKeyVault -VaultName Contoso-O365EX-NA-VaultA1
```

Para remover permissões de administrador, execute o cmdlet Remove-AzureRmKeyVaultAccessPolicy:
  
```
Remove-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> 
-UserPrincipalName <UPN of user>
```

Por exemplo:
  
```
Remove-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
-UserPrincipalName alice@contoso.com
```

### <a name="determine-the-dep-assigned-to-a-mailbox"></a>Determinar a DEP atribuída a uma caixa de correio
<a name="DeterminemailboxDEP"> </a>

Para determinar a DEP atribuída a uma caixa de correio, use o cmdlet Get-MailboxStatistics. O cmdlet retorna um identificador exclusivo (GUID).
  
```
Get-MailboxStatistics -Identity <GeneralMailboxOrMailUserIdParameter> | fl DataEncryptionPolicyID
```

Onde *GeneralMailboxOrMailUserIdParameter* Especifica uma caixa de correio. Para obter mais informações sobre o cmdlet Get-MailboxStatistics, consulte [Get-MailboxStatistics](https://technet.microsoft.com/library/bb124612%28v=exchg.160%29.aspx).
  
Use o GUID para descobrir o nome amigável da DEP ao qual a caixa de correio foi atribuída, executando o seguinte cmdlet.
  
```
Get-DataEncryptionPolicy <GUID>
```

Onde *GUID* é o GUID retornado pelo cmdlet Get-MailboxStatistics na etapa anterior. 
  


---
title: Criptografia de serviço com chave do cliente para perguntas frequentes do Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 7/31/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 41ae293a-bd5c-4083-acd8-e1a2b4329da6
description: Além da linha de base, o nível de volume criptografia que é habilitada por meio do BitLocker e Gerenciador de chave distribuído (DKM), o Office 365 oferece uma camada adicional de criptografia no nível do aplicativo para o conteúdo do cliente no Office 365, incluindo os dados do Exchange On-line, Skype para negócios, SharePoint Online e OneDrive for Business. Isso é chamado de criptografia de serviço.
ms.openlocfilehash: 38731d22b78274e42b0886c41884a0395d8df69f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22559236"
---
# <a name="service-encryption-with-customer-key-for-office-365-faq"></a>Criptografia de serviço com chave do cliente para perguntas frequentes do Office 365

Além da linha de base, o nível de volume criptografia que é habilitada por meio do BitLocker e Gerenciador de chave distribuído (DKM), o Office 365 oferece uma camada adicional de criptografia no nível do aplicativo para o conteúdo do cliente no Office 365, incluindo os dados do Exchange On-line, Skype para negócios, SharePoint Online e OneDrive for Business. Isso é chamado de criptografia de serviço.
  
Chave de cliente se baseia na criptografia de serviço e permite que você forneça e chaves de controle que são usadas para criptografar dados em repouso no Office 365, conforme descrito em [Termos de serviços Online (OST)](https://www.microsoft.com/en-us/Licensing/product-licensing/products.aspx). Chave de cliente ajuda a atender às obrigações de conformidade pois você controlar as chaves de criptografia que o Office 365 utiliza para descriptografar os dados.
  
Para fornecer comentários sobre a chave do cliente, incluindo a documentação, envie perspectivas, sugestões e ideias para customerkeyfeedback@microsoft.com.
  
## <a name="what-is-service-encryption-with-customer-key"></a>Qual é a criptografia de serviço com a chave do cliente?

Chave de cliente é um recurso que permite provisionar e gerenciar as teclas usadas para criptografar dados em repouso no Office 365. O recurso aproveita a criptografia de serviço, que é a criptografia é realizada pelo Office 365 Exchange e SharePoint. Criptografia de serviço fornece vantagens além do que o BitLocker fornecido - notadamente, maior na defesa contra invasores. A criptografia de serviço é uma medida defensiva forte se um invasor tenta ignorar o sistema de controle de acesso do Office 365 que é usado para processar todas as solicitações de acesso a dados do cliente. Isso ocorre porque a criptografia de serviço significa que um administrador de servidor não tem o controle ou par acesso para a criptografia de chaves e não é possível desabilitar a criptografia, ao contrário com BitLocker. Portanto, o invasor com acesso administrativo para um servidor que hospeda os dados do cliente que foi criptografados usando a criptografia de serviço não será possível ler os dados do cliente e mesmo se os dados criptografados são copiados logoff do servidor permanecerá inútil. 
  
## <a name="what-office-365-data-at-rest-is-covered-by-customer-key"></a>Quais dados o Office 365 em repouso são abordados pela chave cliente?
<a name="WhatDataIsCoveredbyCustomerKey"> </a>

O conteúdo do site do SharePoint Online e os arquivos armazenados no site e arquivos carregados ao OneDrive for Business são abordados. Conteúdo de caixa de correio Exchange Online (corpo do email, entradas de calendário e conteúdo de anexos de email) é abordado. Conversas de texto do Skype para negócios são abordadas, mas as gravações de transmissão do Skype reunião e carregamentos de conteúdo de reunião Skype não são abordados. Transmissão do Skype reunião e Skype reunião carregamentos de conteúdo são criptografados, juntamente com todos os outros conteúdos no Office 365, mas que atualmente não oferecemos controle das chaves de criptografia do cliente.
  
## <a name="what-is-the-difference-between-customer-key-and-bring-your-own-key-byok-with-azure-information-protection-for-exchange-online"></a>O que é a diferença entre a chave de cliente e Traga sua própria chave (BYOK) com o Windows Azure Information Protection para Exchange Online?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

As duas opções permitem que você forneça e controlar suas próprias chaves de criptografia; No entanto, a criptografia de serviço com chave de cliente criptografa os dados em repouso, que reside no Office 365 servidores em repouso, enquanto BYOK com o Azure Information Protection para Exchange Online criptografa seus dados em trânsito e fornece persistente online e offline proteção de mensagens de email e anexos para o Office 365. Chave de cliente e BYOK com o Azure Information Protection para Exchange Online são complementares, e se você optar por usar chaves de serviço gerenciada da Microsoft ou suas próprias teclas, a criptografia de seus dados em repouso e em trânsito pode fornecer adicionada proteção contra contra ataques mal-intencionados.
  
BYOK com o Azure Information Protection para Exchange Online é oferecido nos recursos do Office 365 Message Encryption.
  
## <a name="does-office-365-message-encryption-and-bring-your-own-key-with-azure-information-protection-change-microsofts-approach-to-third-party-data-requests-such-as-subpoenas"></a>Criptografia de mensagem do Office 365 e Traga sua própria chave com proteção de informações do Windows Azure alteram abordagem da Microsoft para solicitações de dados de terceiros, como intimações?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Não. Criptografia de mensagem do Office 365 e a opção para fornecer e controlar suas próprias chaves de criptografia com Traga sua própria chave (BYOK) para proteção de informações do Windows Azure (AIP) não foi projetado para responder a lei imposição intimações. Criptografia de mensagem do Office 365 com BYOK para AIP foi projetada para conformidade focalizados em clientes que precisam atender suas obrigações de conformidade internos ou externos. Microsoft leva muito a sério a solicitações de terceiros para dados do cliente. Como um provedor de serviços de nuvem, podemos sempre defendem à privacidade dos dados do cliente. No caso de recebemos intimação, sempre, tentaremos redirecionar o terceiro ao cliente para obter as informações. (Por favor, leia o blog de Brad Smith: [dados do cliente Protecting do governo snooping](https://blogs.microsoft.com/blog/2013/12/04/protecting-customer-data-from-government-snooping/)). Publicamos periodicamente informações detalhadas da solicitação recebemos [aqui](https://www.microsoft.com/en-us/trustcenter/Privacy/govt-requests-for-data).
  
Consulte a [Central de confiabilidade da Microsoft](https://www.microsoft.com/en-us/trustcenter/default.aspx) relacionadas a solicitações de dados de terceiros e "Divulgação de dados do cliente" em [Termos de serviços Online (OST) ](https://www.microsoft.com/en-us/Licensing/product-licensing/products.aspx)para obter mais informações.
  
## <a name="does-service-encryption-with-customer-key-change-microsofts-approach-to-third-party-data-requests-such-as-subpoenas"></a>Criptografia de serviço com chave de cliente alterar a abordagem da Microsoft às solicitações de dados de terceiros, como intimações?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Não. Chave do cliente não foi projetado para responder a lei imposição intimações. Ele foi projetado para clientes regulamentados atender às suas obrigações de conformidade internos ou externos. Microsoft leva muito a sério a solicitações de terceiros para dados do cliente. Como um provedor de serviços de nuvem, podemos sempre defendem à privacidade dos dados do cliente. No caso de recebemos intimação, sempre, tentaremos redirecionar o terceiro ao cliente para obter as informações. (Por favor, leia o blog de Brad Smith: [dados do cliente Protecting do governo snooping](http://blogs.microsoft.com/blog/2013/12/04/protecting-customer-data-from-government-snooping/)). Publicamos periodicamente informações detalhadas da solicitação recebemos [aqui](https://www.microsoft.com/en-us/trustcenter/Privacy/govt-requests-for-data).
  
Consulte a [Central de confiabilidade da Microsoft](https://www.microsoft.com/en-us/trustcenter/Privacy/govt-requests-for-data) relacionadas a solicitações de dados de terceiros e "Divulgação de dados do cliente" em [Termos de serviços Online (OST)](https://www.microsoft.com/en-us/Licensing/product-licensing/products.aspx) para obter mais informações. 
  
## <a name="is-fasttrack-support-available-for-implementing-customer-key"></a>É FastTrack suporte disponíveis para implementar a chave do cliente?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Não. FastTrack é usado apenas para coletar informações de configuração do inquilino e o serviço que é necessárias para registrar para a chave do cliente. A chave de cliente oferece são publicados por meio de FastTrack para que ele seja conveniente para clientes e parceiros enviar essas informações necessárias, usando o mesmo método e para facilitar os que os clientes fornecem da oferta de dados de arquivamento.
  
Se precisar de suporte adicional além da documentação, contate a Microsoft Consulting Services (MCS), engenharia de campo Premier (PFE) ou um parceiro da Microsoft para obter assistência.
  
## <a name="if-my-keys-are-destroyed-how-can-i-recover"></a>Se minhas chaves são destruídos, como recupero?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

A chave de disponibilidade oferece a capacidade de recuperar a perda inesperada de chaves de raiz que você gerencia. Se você perder as chaves de raiz, visita Microsoft Support e Microsoft ajudará durante o processo de habilitação da chave de disponibilidade. Você usará a chave de disponibilidade para migrar para uma nova política de criptografia de dados com novas chaves provisionadas por você. 
  
## <a name="what-is-the-availability-key"></a>Qual é a chave de disponibilidade?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

A chave de disponibilidade é uma chave de raiz que é provisionada quando você cria uma diretiva de criptografia de dados. A chave de disponibilidade é armazenada e protegida no Office 365 e é funcionalmente semelhante para as chaves de dois raiz que são fornecidas por você para uso com a criptografia de serviço com a chave do cliente. Ao contrário das chaves que você forneça e gerenciar o Azure chave Vault, você não pode acessar diretamente a chave de disponibilidade. O armazenamento e o controle da chave disponibilidade são deliberadamente diferentes das chaves do Azure chave Vault para três razões: primeiro, a chave de disponibilidade fornece um recurso de alta disponibilidade que serviços do Office 365 não conseguem chegar chaves hospedadas na chave do Azure Vault; em segundo lugar, a chave de disponibilidade fornece um recurso de "quebrar vidro" que ambas as chaves do Azure chave Vault sejam perdidas; e terceiro, a separação dos controles lógicas fornece a defesa em camadas e protege contra a perda de todas as chaves de um ataque de único ou ponto de falha. Basicamente compartilhamento a responsabilidade para proteger as chaves, ao mesmo tempo, usando uma variedade de proteções e processos para o gerenciamento de chaves, reduz o risco que todas as chaves (e, portanto, os dados) serão perdidos ou destruídos. A Microsoft fornece autoridade única sobre a destruição da chave de disponibilidade. Por design, ninguém na Microsoft tem acesso à chave de disponibilidade - só é acessível pelo código de serviço do Office 365.
  
## <a name="how-many-data-encryption-policies-deps-can-i-create"></a>Quantas políticas de criptografia de dados (DEPs) pode criar?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

 **Exchange Online e Skype for Business:** Você pode criar até 50 DEPs. 
  
 **SharePoint Online e o OneDrive for Business:** Um DEP aplica-se aos dados em uma localidade geográfica, também chamada de um geo. Se você usar o recurso de multi-geo do Office 365, você pode criar um DEP por geo. Se você não estiver usando multi-geo, você pode criar DEP um.
  
## <a name="can-i-assign-a-data-encryption-policy-before-migrating-a-mailbox-to-the-cloud"></a>Pode atribuir uma política de criptografia de dados antes de migrar uma caixa de correio para a nuvem?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Sim. Você pode usar o cmdlet Set-MailUser do Windows PowerShell para atribuir uma política de criptografia de dados (DEP) para o usuário antes de migrar a caixa de correio para o Office 365. Quando você fizer isso, o conteúdo da caixa de correio será criptografado usando a DEP atribuída, como o conteúdo é migrado. Isso pode ser mais eficiente do que a atribuição de um DEP após a caixa de correio já tenha sido migrada e então aguardar para criptografia ocorrer, o que poderá levar horas ou possivelmente dias. 
  
## <a name="how-do-i-verify-that-encryption-with-customer-key-is-activated-and-office-365-has-finished-encrypting-with-customer-key"></a>Como verificar que a criptografia com a chave do cliente está ativada e Office 365 concluiu a criptografia com a chave do cliente?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

 **Exchange Online e Skype for Business:** Você pode [se conectar ao Exchange Online usando o PowerShell remoto](https://technet.microsoft.com/en-us/library/jj984289%28v=exchg.160%29.aspx) e usar o cmdlet **[Get-MailboxStatistics]** para cada caixa de correio que você deseja verificar. Na saída do cmdlet Get-MailboxStatistics, a propriedade _IsEncrypted_ retorna um valor de **true** se a caixa de correio é criptografada e um valor **false** caso não seja. Se a caixa de correio é criptografada, o valor retornado da propriedade _DataEncryptionPolicyID_ é o GUID da DEP com os quais a caixa de correio é criptografada. Para obter mais informações sobre como executar esse cmdlet, consulte [Get-MailboxStatistics](https://technet.microsoft.com/en-us/library/bb124612%28v=exchg.160%29.aspx) e usando o PowerShell com o Exchange Online. 
  
Se as caixas de correio não são criptografadas após esperar 72 horas desde o momento em que você atribuiu a DEP, inicie uma movimentação de caixa de correio. Para fazer isso, [Conecte-se ao Exchange Online usando o PowerShell remoto](https://technet.microsoft.com/en-us/library/jj984289%28v=exchg.160%29.aspx) e, em seguida, use o cmdlet New-MoveRequest e fornecer o alias da caixa de correio da seguinte maneira: 
  
```
New-MoveRequest <alias>
```

 **SharePoint Online e o OneDrive for Business:** Você pode [se conectar ao SharePoint Online PowerShell](https://technet.microsoft.com/en-us/library/fp161372.aspx)e use o cmdlet **[Get-SPODataEncryptionPolicy]** para verificar o status do seu locatário. O * * _estado_* * propriedade retornará um valor de **registrado** , se a criptografia de chave do cliente está ativada e todos os arquivos em todos os sites foram criptografados. Se a criptografia ainda está em andamento, esse cmdlet fornece informações na qual o percentual de sites está concluído. 
  
## <a name="if-i-want-to-switch-to-a-different-set-of-keys-how-long-does-it-take-for-the-new-set-of-keys-to-protect-my-data"></a>Se eu quiser alternar para outro conjunto de chaves, quanto tempo leva para o novo conjunto de chaves para proteger meus dados?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

 **Exchange Online e Skype for Business:** Pode demorar até 72 horas para proteger uma caixa de correio de acordo com o novo dados criptografia política (DEP) desde o momento em que o novo DEP é atribuída à caixa de correio. 
  
 **SharePoint Online e o OneDrive for Business:** Pode levar até quatro horas para criptografar novamente o seu locatário inteiro depois que tiver sido atribuída a uma nova chave. 
  
## <a name="is-my-existing-data-stored-without-encryption-at-any-time-while-it-is-decrypted-or-encrypted-with-customer-key"></a>Os dados existentes são armazenados sem criptografia a qualquer momento durante descriptografado ou criptografada com a chave do cliente?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Não. Os dados são sempre criptografados em repouso no serviço Office 365 com o BitLocker e DKM. Para obter mais informações, consulte o "segurança, privacidade e informações de conformidade para o Office 365" e [como o Exchange da Online protege seus segredos de email](https://support.office.com/article/989BA10C-F73F-4EFB-AD1B-AF3322E5F376).
  
## <a name="if-i-no-longer-want-to-use-customer-managed-encryption-keys-can-i-switch-to-microsoft-managed-keys"></a>Se não há mais eu desejo usar chaves de criptografia do cliente gerenciado, pode alternar às chaves Microsoft gerenciados?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

 **Exchange Online e Skype for Business:** Ainda não. Isso terá suporte depois que a criptografia de serviço no Office 365 com as teclas gerenciados Microsoft é amplamente distribuída. Esperamos distribuir isso no serviço após o lançamento de criptografia de serviço com a chave do cliente. 
  
 **SharePoint Online e o OneDrive for Business:** Sim. Você pode optar por reverter para usando chaves Microsoft gerenciados separadamente para cada geo (se você usar o recurso de multi-geo) ou para todos os seus dados se ele estiver em um único geo. 
  
## <a name="if-i-lose-my-keys-how-long-does-it-take-to-recover-service-availability-using-the-recovery-key"></a>Se eu perder minhas chaves, quanto tempo leva para recuperar a disponibilidade de serviço usando a chave de recuperação?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

 **Exchange Online e Skype for Business:** Depois que você liga para usar a chave de disponibilidade, caixas de correio será acessíveis em minutos. 
  
 **SharePoint Online e o OneDrive for Business:** Essa operação é proporcional ao número de sites que você tem. Depois de você chamar Microsoft para usar a chave de disponibilidade, você será totalmente online dentro de cerca de quatro horas. 
  
## <a name="how-is-the-availability-key-used-with-exchange-online"></a>Como a chave de disponibilidade é usada com o Exchange Online?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Há três maneiras de que a chave de disponibilidade é usada com o Exchange Online:
  
- Serviço disponibilidade - que chaves do Azure chave Vault estão inacessíveis.
    
- Ações iniciadas pelo código de serviço do Office 365 -, como a criação do índice de pesquisa ou caixa de correio move.
    
- Recuperar de perda de chave - como a perda de ambas as chaves do Azure chave Vault associado a um único DEP.
    
 **Usando a chave de disponibilidade para disponibilidade de serviço, no caso de chaves do Windows Azure chave Vault estão inacessíveis.**
  
O Office 365 usa a chave de disponibilidade tanto a disponibilidade do serviço e a recuperação de um estado íntegro de chave de cliente para o Exchange Online. Não há uma hierarquia de chaves usadas pela chave do cliente. Essa hierarquia é ilustrada na figura a seguir.
  
![](media/a760156b-737f-469a-80ab-c28b7a8b9160.png)
  
Se ambas as chaves de um único dados criptografia política (DEP) do Azure chave Vault não estiverem disponíveis, o Office 365 pode usar a disponibilidade para alterar para um novo Office 365 da DEP. determina se deve usar a chave de disponibilidade para disponibilidade do serviço de forma diferente, dependendo se um atividade iniciadas pelo usuário, por exemplo, quando um usuário baixa o email para o cliente Outlook ou uma atividade iniciadas pelo sistema, como a indexação de conteúdo de caixa de correio ou para pesquisas de descoberta eletrônica, disparada o processo.
  
O Office 365 segue este processo em resposta às ações iniciadas pelo usuário para determinar quando usar a chave de disponibilidade para caixas de correio de usuário:
  
1. O Office 365 lê a DEP à qual a caixa de correio é atribuída para determinar o local das chaves de duas cliente no compartimento de chave do Windows Azure.
    
2. O Office 365 aleatoriamente escolhe uma das duas cliente chaves da DEP e envia uma solicitação para armazenamento de chave do Windows Azure para decodificar a chave DEP usando a chave do cliente.
    
3. Se a solicitação para decodificar a DEP chave usando a chave do cliente falha e retornará um erro, o Office 365 envia uma segunda solicitação para armazenamento de chave do Azure, desta vez instruindo-la para utilizar o alternativo (segunda) chave do cliente.
    
4. Se a segunda solicitação para decodificar a chave DEP usando o falhar chave do cliente e retornará um erro, o Office 365 examina os resultados de ambas as solicitações:
    
  - Se o exame determina que não faça os erros refletem uma ação explícita por uma identidade do cliente, o Office 365 usa a chave de disponibilidade para descriptografar a chave do DEP. A chave DEP, em seguida, é usada para descriptografar a chave de caixa de correio e concluir a solicitação do usuário.
    
    Nesse caso, o Azure chave Vault é incapaz de responder ou inacessível por qualquer motivo. O Office 365 não tem nenhuma maneira de determinar se o cliente tiver intencionalmente revogado acesso às chaves.
    
  - Se o exame indica essa ação deliberada foi executada para renderizar o cliente chaves não estiver disponível, e em seguida, a chave de disponibilidade não será usada, haverá falha na solicitação de usuário e o usuário recebe uma mensagem de erro, como falha de logon.
    
    Quando isso acontece, o cliente será feito ciente de que o serviço é afetado e a condição da chave do cliente não está íntegra. Por exemplo, se um cliente estiver usando um único DEP para todas as caixas de correio na organização, o cliente pode enfrentar uma falha generalizados para onde os usuários não podem acessar suas caixas de correio. Isso garante que, quando não íntegros ambas as chaves de cliente, o cliente é feito ciente a necessidade de corrigir a situação e restaurar o serviço para um estado íntegro.
    
 **Usando a chave de disponibilidade para ações iniciadas pelo código de serviço do Office 365.**
  
Código do Office 365 service sempre tem um token de login válido e não pode ser bloqueado. Portanto, até que a chave de disponibilidade tiver sido excluída, ele pode ser usado para ações iniciadas por, ou internos, código de serviço do Office 365, como a criação do índice de pesquisa ou mover caixas de correio.
  
 **Usando a chave de disponibilidade para recuperar de perda de chave.**
  
Você pode usar a chave de disponibilidade para recuperar a perda de ambas as chaves do Azure chave Vault que estão associados a DEP mesma, conforme descrito na resposta à entrada de perguntas Frequentes "se minhas chaves são destruídos, como posso recuperar?".
  
## <a name="how-is-the-availability-key-used-with-sharepoint-online-and-onedrive-for-business"></a>Como a chave de disponibilidade é usada com o SharePoint Online e o OneDrive for Business?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

O SharePoint Online e OneDrive para arquitetura de negócios e implementação para a chave de chave de cliente e a disponibilidade são diferentes do Exchange Online e do Skype para negócios.
  
Quando um cliente é movido para chaves gerenciado pelo cliente, o Office 365 cria uma chave de intermediária de específica do locatário (TIK). O Office 365 criptografa o TIK duas vezes, uma vez com cada uma das chaves de cliente e armazena as duas versões criptografadas do TIK. Somente as versões criptografadas do TIK são armazenadas e um TIK só pode ser descriptografada com as chaves de cliente. O TIK é usado para criptografar as chaves do site, que são usadas para criptografar as chaves de blob. Os blobs sozinhos são criptografados e armazenados no serviço de armazenamento do Microsoft Azure Blob.
  
O Office 365 segue este processo para acessar um blob com dados de arquivo do cliente:
  
1. Descriptografe o TIK usando a chave do cliente.
    
2. Use o TIK descriptografada para descriptografar uma chave de site.
    
3. Use a chave do site descriptografada para descriptografar uma chave de blob.
    
4. Use a chave de blob descriptografada para descriptografar o blob.
    
Quando descriptografando um TIK, o Office 365 emite duas solicitações de descriptografia para armazenamento de chave do Windows Azure com um deslocamento de pequeno. O primeiro que término fornece o resultado, cancelando a solicitação de outra.
  
Caso o cliente perde o acesso às suas chaves de cliente, o Office 365 também criptografa a TIK com uma chave de disponibilidade e armazena esse juntamente com os TIKs criptografadas com a chave de cada cliente. O TIK criptografada com a chave de disponibilidade é usado somente quando o cliente telefonar Microsoft inscrever-se o caminho de recuperação quando eles tem perdido acesso às suas chaves, de modo mal-intencionado ou acidentalmente.
  
Por motivos de escala e de disponibilidade, TIKs descriptografadas são armazenados em cache em um cache de memória de tempo limitado. Duas horas antes de um cache TIK está configurado para expirar, o Office 365 tenta descriptografar cada TIK. Descriptografar os TIKs estende o tempo de vida do cache. Se a descriptografia de TIK falhar por um período de tempo significativo, o Office 365 gera um alerta para notificar engenharia antes do vencimento de cache. Somente se o cliente chama o Microsoft Office 365 iniciará a operação de recuperação, o que envolve a descriptografia de que de TIK com a chave de disponibilidade armazenados no repositório secreto da Microsoft e a inclusão de Inquilino novamente usando o descriptografada TIK e um novo conjunto chaves do Azure chave Vault fornecido pelo cliente.
  
A partir de hoje, chave de cliente está envolvido na cadeia de criptografia e descriptografia de dados de arquivo do SharePoint Online armazenados no repositório de blob Azure, mas não os itens de lista do SharePoint Online ou metadados armazenados no banco de dados SQL. O Office 365 não usa a disponibilidade chave para o SharePoint Online ou OneDrive for Business que não seja o caso descrito acima, que é o cliente iniciado. Humano acesso aos dados do cliente é protegido por Lockbox do cliente.
  
## <a name="how-is-customer-key-licensed"></a>Como a chave do cliente é licenciado?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Chave de cliente é oferecida no Office 365 Enterprise Suite, "E5" e a SKU de conformidade avançadas. Além disso, os clientes também devem adquirir a licença apropriada para usar o Windows Azure chave Vault.
  
Cada usuário que se beneficiando da chave de cliente deve ser licenciados se desejam ser coberto por chave de cliente.
  
SharePoint Online, o administrador do Office 365 que configura a chave do cliente também precisa ser licenciados para executar as etapas de instalação. Além disso, os usuários que estão sendo beneficiados com o recurso precisam ser licenciados - isso inclui o proprietário do site e quaisquer usuários que acessam arquivos em um ou mais sites que são criptografadas usando a chave do cliente. Usuários externos não precisará ser licenciados para acessar arquivos em um ou mais sites que são criptografadas usando a chave do cliente.
  
Para o Exchange Online, caixas de correio de "usuário" e "mail" caixas de correio devem ser licenciadas. Todos os outros, como caixas de correio compartilhadas não são necessárias para ter uma licença para a chave do cliente. Para verificar que sua caixa de correio do Exchange Online é licenciada adequadamente, execute o seguinte cmdlet:
  
```
(Get-Mailbox <alias >).PersistedCapabilities
```

Se a cadeia de caracteres BPOS_S_EquivioAnalytics existir, a caixa de correio é licenciada adequadamente. Caso contrário, você deve aplicar a licença adequada para usar o recurso de chave de cliente para esta caixa de correio.
  
## <a name="can-i-enable-customer-key-for-a-trial-subscription"></a>Posso habilitar a chave de cliente para uma assinatura de avaliação?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Não. Por definição, assinaturas de avaliação têm uma vida útil limitada. Chaves de criptografia que são hospedadas em assinaturas de avaliação podem ser perdidas no final da vida útil do avaliação. Como a Microsoft não pode e não impede que os clientes colocar os dados de cliente importante em assinaturas de avaliação, o uso da chave de cliente com assinaturas de avaliação é proibido.
  
## <a name="how-much-will-using-customer-key-cost"></a>Quanto será usando o custo de chave do cliente?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Além do licenciamento necessários para a chave do cliente, os clientes provocará um custo para o uso de chave Vault. [Obter detalhes sobre preços do Azure chave Vault](https://azure.microsoft.com/en-us/pricing/details/key-vault/) descreve o modelo de custo e auxiliarão com estimando. Não há um meio para prever o custo exato que qualquer cliente incorrerá porque variam de padrões de uso. A experiência mostra que o custo é muito baixo e geralmente cair dentro do intervalo de US $0,002 para $0,005 por usuário por mês, mais o custo das teclas HSM reserva. O custo também variam de acordo com a configuração de registro em log escolhida pelo cliente e a quantidade de armazenamento Azure usado para o Windows Azure chave Vault logs. 
  
## <a name="for-more-information"></a>Para saber mais
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Para começar com a chave de cliente, consulte [controlar seus dados no Office 365 usando a chave do cliente](controlling-your-data-using-customer-key.md).
  


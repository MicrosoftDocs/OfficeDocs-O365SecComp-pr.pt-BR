---
title: Usar o carregamento de rede para importar arquivos PST criptografados por RMS para o Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 5/29/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 84a595b8-cd77-4f66-ac52-57a33ddd4773
description: Aprenda a usar o carregamento de rede para importar arquivos PST RMS criptografadas para caixas de correio do usuário no Office 365.
ms.openlocfilehash: 6460512e2d6085df684841248dc286d39dbd9d87
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524671"
---
# <a name="use-network-upload-to-import-rms-encrypted-pst-files-to-office-365"></a>Usar o carregamento de rede para importar arquivos PST criptografados por RMS para o Office 365

**Este artigo destina-se a administradores. Você está tentando importar arquivos PST para sua própria caixa de correio? Consulte o [email de importação, contatos e calendário de um arquivo. pst do Outlook](https://go.microsoft.com/fwlink/p/?LinkID=785075)**
   
O uso da rede carregar opção e o serviço Office 365 importar para importar arquivos PST para caixas de correio do usuário. Carregamento de rede significa que você carregar os arquivos PST uma área de armazenamento temporário em nuvem da Microsoft. Em seguida, o serviço de importação do Office 365 copia os arquivos PST da área de armazenamento para as caixas de correio de usuário de destino. Um novo recurso do serviço de importação lhe permite criptografar seus arquivos PST antes que eles são carregados e armazenados em nuvem da Microsoft. Esses arquivos estarão não criptografados quando elas forem importadas para caixas de correio do usuário. 
  
Aqui estão as etapas necessárias para criptografar e importar arquivos PST às caixas de correio do Office 365:
  
[Etapa 1: configurar o Azure Rights Management para Importação de PST ](#step-1-set-up-azure-rights-management-for-pst-import)

[Etapa 2: gerar uma chave de criptografia para Importação de PST](#step-2-generate-an-encryption-key-for-pst-import)

[Etapa 3: Obter o ID do inquilino de RMS e URL de licenciamento](#step-3-obtain-rms-tenant-id-and-licensing-url)

[Etapa 4: Baixar as ferramentas de importação de PST e copie a URL SAS](#step-4-download-the-pst-import-tools-and-copy-the-sas-url)

[Etapa 5: Criptografar e carregar seus arquivos PST para o Office 365](#step-5-encrypt-and-upload-your-pst-files-to-office-365)

[(Opcional) Etapa 6: Exibir uma lista dos arquivos PST carregados para o Office 365](#optional-step-6-view-a-list-of-the-pst-files-uploaded-to-office-365)

[Etapa 7: Criar o arquivo de mapeamento de importação de PST](#step-7-create-the-pst-import-mapping-file)

[Etapa 8: criar um trabalho de Importação de PST no Office 365](#step-8-create-a-pst-import-job-in-office-365)
  
> [!IMPORTANT]
> Você precisa executar a etapa 1 por meio da etapa 4 somente uma vez para instalar e configurar sua organização para criptografar e importar arquivos PST às caixas de correio do Office 365. Depois de executar estas etapas, siga a etapa 5 a etapa 8 cada vez que você deseja criptografar, carregar e importa um lote de arquivos PST. 
  
Para obter mais informações sobre como importar dados para o Office 365, consulte [Overview of importar os arquivos PST de organização para o Office 365](importing-pst-files-to-office-365.md).
  
## <a name="before-you-begin"></a>Antes de começar

- Você precisa ter a função caixa de correio importar exportar no Exchange Online para importar arquivos PST para caixas de correio do Office 365. Por padrão, essa função não é atribuída a nenhum grupo de função no Exchange Online. Você pode adicionar a função caixa de correio importar e exportar para o grupo de funções de gerenciamento da organização. Ou você pode criar um novo grupo de função, atribua a função caixa de correio importar e exportar e, em seguida, adicione si mesmo como membro. Para obter mais informações, consulte "Adicionar uma função para um grupo de funções" ou "Criar um grupo de funções" seções em [Gerenciar grupos de função](https://go.microsoft.com/fwlink/p/?LinkId=730688).
    
    Além disso criar a importação de trabalhos no Office 365 Security &amp; Centro de conformidade, uma das opções a seguir devem ser verdadeiro:
    
  - Você precisa ter a função de destinatários de email no Exchange Online. Por padrão, essa função é atribuída aos grupos de funções de gerenciamento de destinatário e gerenciamento da organização.
    
    Ou
    
  - Você precisa ser um administrador global na sua organização do Office 365.
    
  > [!TIP]
  > Considere a criação de um novo grupo de função no Exchange Online que destina-se especificamente para importar arquivos PST para o Office 365. Para o nível mínimo de privilégios necessários para importar arquivos PST, atribua as funções de caixa de correio importar exportar e destinatários de email para o novo grupo de função e, em seguida, adicionar membros. 
  
- Você precisa armazenar os arquivos PST que você deseja importar para o Office 365 em um servidor de arquivo ou a pasta compartilhada em sua organização. Na etapa 5, você executará o Office 365 ImportTool, que irá criptografar e carregar os arquivos PST que são armazenados neste servidor de arquivo ou pasta para o Office 365 compartilhada.
    
- Esse procedimento envolve copiar e salvar uma cópia de uma chave de criptografia, uma chave de armazenamento e um número de chaves de identificação e URLs. Este informações serão usadas na etapa 5 para criptografar e carregar seus arquivos PST. Certifique-se de que tome precauções para proteger esses apenas como você faria proteger senhas ou outras informações relacionadas à segurança. Por exemplo, você poderá salvá-los em um documento do Microsoft Word protegido por senha ou salvá-los em uma unidade USB criptografada. Consulte a seção de [informações adicionais](#more-information) para obter um exemplo dessas chaves, IDs e URLs. 
    
- Você pode importar arquivos PST para uma caixa de correio inativa no Office 365. Você pode fazer isso, especificando o GUID da caixa de correio inativa no `Mailbox` parâmetro no arquivo de mapeamento de importação de PST. Consulte a [etapa 7](#step-7-create-the-pst-import-mapping-file) para obter mais informações. 
    
- Em uma implantação híbrida do Exchange, você pode importar arquivos PST, uma caixa de correio de arquivamento baseado em nuvem para um usuário cuja caixa de correio primária está no local. Você pode fazer isso fazendo o seguinte no arquivo de mapeamento de importação de PST:
    
  - Especifique o endereço de email para a caixa de correio do usuário local no `Mailbox` parâmetro. 
    
  - Especificar o valor **TRUE** no `IsArchive` parâmetro. 
    
    Consulte a [etapa 7](#step-7-create-the-pst-import-mapping-file) para obter mais informações. 
    
- Depois que os arquivos PST são importados para uma caixa de correio do Office 365, a configuração da caixa de correio de retenção é ativada por um período indefinido. Isso significa que a política de retenção atribuída à caixa de correio não será processada até que você desative o status em retenção ou definir uma data para desativar o bloqueio. Por que fazemos isso? Se mensagens importadas para uma caixa de correio são antigas, podem ser permanentemente excluídos (purgados) porque seu período de retenção expirou com base nas configurações de retenção configuradas para a caixa de correio. Colocação de caixa de correio em retenção fornecerá o tempo de proprietário da caixa de correio para gerenciar essas mensagens importado recentemente ou dê tempo para alterar as configurações de retenção da caixa de correio. Consulte a seção de [informações adicionais](#more-information) para obter sugestões sobre como gerenciar a retenção. 
    
- Se você não precisa criptografar seus arquivos PST antes de que carregá-las para o Office 365, consulte [utilizar rede carregar para importar arquivos PST para o Office 365](use-network-upload-to-import-pst-files.md).
    
- Para perguntas frequentes sobre como usar o carregamento de rede para importar arquivos PST para o Office 365, consulte [perguntas Frequentes sobre a importação de arquivos PST para o Office 365](faqimporting-pst-files-to-office-365.md).
  
## <a name="step-1-set-up-azure-rights-management-for-pst-import"></a>Etapa 1: configurar o Azure Rights Management para Importação de PST 

Importação de PST usa a funcionalidade de criptografia fornecida pelo serviço de gerenciamento de direitos do Windows Azure (Azure RMS) no Office 365. Isso permite que você para criptografar arquivos PST antes carregando-os para o Office 365. 
  
Configurando o RMS do Windows Azure para importação de PST consiste em três etapas:
  
- [Ativando o RMS do Azure](#activate-azure-rms)
    
- [Configurando o RMS no Exchange Online](#configure-rms-in-exchange-online)
    
- [Instalando o cliente RMS do Active Directory](#install-the-active-directory-rms-client)
    
### <a name="activating-azure-rms"></a>Ativando o RMS do Azure

Azure RMS está desabilitada por padrão, mas você ou outro administrador em sua organização deve ter ativado-lo. Siga as instruções em [Ativando o Azure Rights Management](https://docs.microsoft.com/azure/information-protection/deploy-use/activate-service) para instalar e ativar o Azure DRM.
  
### <a name="configuring-rms-in-exchange-online"></a>Configurando o RMS no Exchange Online

Após ter ativado o serviço de gerenciamento de direitos, a próxima etapa é definir o backup de gerenciamento de direitos de informação (IRM) no Exchange Online para usar o RMS do Azure. Para obter mais informações, consulte [Configurar o IRM para usar o Azure Rights Management](https://go.microsoft.com/fwlink/p/?LinkId=394816).
  
1. [Conectar ao Exchange Online usando o PowerShell remoto](https://go.microsoft.com/fwlink/p/?LinkId=396554 ).
    
2. Execute o seguinte comando para definir a URL de compartilhamento de chave do RMS.
    
    ```
    Set-IRMConfiguration -RMSOnlineKeySharingLocation <RMS key sharing location>
    ```

    Use a tabela a seguir para determinar o local de compartilhamento correto da chave do RMS para o local da organização.
    
    |**Local**|**Local de compartilhamento de chave do RMS**|
    |:-----|:-----|
    |América do Norte  <br/> | `https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc` <br/> |
    |União Europeia  <br/> | `https://sp-rms.eu.aadrm.com/TenantManagement/ServicePartner.svc` <br/> |
    |Ásia  <br/> | `https://sp-rms.ap.aadrm.com/TenantManagement/ServicePartner.svc` <br/> |
    |América do Sul  <br/> | `https://sp-rms.sa.aadrm.com/TenantManagement/ServicePartner.svc` <br/> |
    |Office 365 para agências governamentais (Nuvem de Comunidade Governamental)  <br/> | `https://sp-rms.govus.aadrm.com/TenantManagement/ServicePartner.svc`<sup>1</sup> <br/> |
   
    > [!NOTE]
    > <sup>1</sup> Apenas os clientes que adquiriram os SKUs do Office 365 para agências governamentais (Nuvem de Comunidade Governamental) devem usar o local de compartilhamento de chaves RMS. 
  
    Por exemplo, este comando configura a chave do RMS Online local de compartilhamento no Exchange Online para um cliente localizado na América do Norte.
    
    ```
    Set-IRMConfiguration -RMSOnlineKeySharingLocation "https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc"
    ```

3. Execute o seguinte comando para importar uma publicação domínio confiável (TPD) do RMS Online para sua organização do Office 365. 
    
    ```
    Import-RMSTrustedPublishingDomain -RMSOnline -Name "RMS Online"
    ```

    Um TPD contém as configurações necessárias para usar recursos do RMS na organização, inclusive a criptografia de arquivos PST.  
    
4. Execute o seguinte comando para habilitar o IRM para sua organização do Office 365.
    
    ```
    Set-IRMConfiguration -InternalLicensingEnabled $true
    ```

### <a name="installing-the-active-directory-rms-client"></a>Instalando o cliente RMS do Active Directory

Baixar o cliente Rights Management Services (RMS) 2.1 é a última etapa nesta seção. Este software ajuda a proteger o acesso ao RMS do Windows Azure e protege informações que fluem em aplicativos que usam a instalar o Windows Azure RMS. o cliente RMS no mesmo computador que você usará para criptografar e carregar arquivos PST na etapa 5. 
  
1. Baixe o [cliente de serviço de gerenciamento de direitos 2.1](https://www.microsoft.com/en-us/download/details.aspx?id=38396).
    
2. Execute o assistente do Rights Management Service Client 2.1 do Active Directory para instalar o cliente.

## <a name="step-2-generate-an-encryption-key-for-pst-import"></a>Etapa 2: gerar uma chave de criptografia para Importação de PST

Depois de configurar o RMS do Azure, a próxima etapa é gerar uma chave de criptografia (chamada de uma chave simétrica) que será usada para criptografar os arquivos PST que você carrega para o Office 365. Você vai fazer isso, adicionando o serviço de importação de PST como um serviço principal no Windows Azure Active Directory. Adicionar este aplicativo como uma entidade de serviço permitirá que o serviço de importação de PST autenticar diretamente com o Windows Azure Active Directory quando você carrega criptografado os arquivos PST para o local de armazenamento do Azure na etapa 5.
  
1. Inicie o módulo do Azure Active Directory para o Windows PowerShell.
    
2. Execute o seguinte comando para se conectar ao serviço do Microsoft Online.
    
    ```
    Connect-MsolService
    ```

3. Insira as credenciais para uma conta de administrador em sua organização do Office 365 e clique em **Okey**.
    
4. Execute o seguinte comando para gerar uma chave de criptografia ou chave simétrica. Para fazer isso, crie uma nova entidade de criptografia de PST.
    
    ```
    New-MsolServicePrincipal -DisplayName PstEncryptionPrincipal
    ```

    O sistema exibe a chave simétrica e as propriedades da nova entidade de criptografia de PST.
    
    ![Copiar e salvar a chave simétrica que é exibida](media/0003fdea-dace-41d2-b49d-f5c98c6230ca.png)
  
5. Copie a chave simétrica em um arquivo de texto ou no Word. Conforme mencionamos, não deixe de tomar medidas para proteger esse arquivo. Como essa é a única ocasião em que o sistema exibe a chave simétrica, considere fazer uma captura de tela da janela e salvá-la no mesmo arquivo.  
    
    > [!IMPORTANT]
    > Depois de criar a entidade de criptografia de PST, o sistema não permite recuperar a chave simétrica usando o cmdlet **Get-MsolServicePrincipal**. Por isso é importante salvar a chave. 
  
Mantenha o Azure Active Directory módulo para Windows PowerShell aberto e conectado ao serviço Microsoft Online. Você vai executar um comando nessa janela na próxima etapa.

## <a name="step-3-obtain-rms-tenant-id-and-licensing-url"></a>Etapa 3: Obter o ID do inquilino de RMS e URL de licenciamento

A próxima etapa é obter o locatário ID e a URL do local do licenciamento para o serviço RMS do Windows Azure para sua organização. Copie e salve essas informações para o mesmo arquivo que contém a chave simétrica da etapa 2. A ID e a URL serão usado na etapa 5 para criptografar arquivos PST.
  
1. Do Azure Active Directory módulo para Windows PowerShell (que é conectado ao serviço Microsoft Online), execute o seguinte comando para conectar ao serviço RMS do Windows Azure em sua organização do Office 365.
    
    ```
    Connect-AadrmService 
    ```

2. Insira as credenciais para uma conta de administrador em sua organização do Office 365 e clique em **Okey**.
    
3. Execute o seguinte comando para exibir a ID do inquilino para o serviço do Windows Azure RMS na sua organização do Office 365.
    
    ```
    Get-AadrmConfiguration | FL BPOSId
    ```

    Copie e salve o valor para o `BPOSId` propriedade. 
    
4. Execute o seguinte comando para exibir o local de licenciamento para o seu serviço RMS do Azure.
    
    ```
    Get-AadrmConfiguration | FL LicensingIntranetDistributionPointUrl
    ```

    Copie e salve o valor para o `LicensingIntranetDistributionPointUrl` propriedade. 

## <a name="step-4-download-the-pst-import-tools-and-copy-the-sas-url"></a>Etapa 4: Baixar as ferramentas de importação de PST e copie a URL SAS

Agora que você tiver configurado o RMS do Windows Azure e obtidos as IDs necessárias para criptografar arquivos PST, a próxima etapa é baixar e instalar as ferramentas que você executará na etapa 5 para criptografar e PST de carregamento de arquivos para o Office 365. Essas ferramentas estão as ferramentas de AzCopy do Windows Azure e a criptografia de dados do Office 365. Você também vai copiar a URL SAS para sua organização. Essa URL é uma combinação da URL de rede para o local de armazenamento do Azure em nuvem da Microsoft para sua organização e uma chave de assinatura de acesso compartilhado (SAS). Essa chave fornece as permissões necessárias para carregar arquivos PST para o seu local de armazenamento do Azure. Salvá-lo para o mesmo arquivo que você copiou para as outras informações na etapa 2 e a etapa 3. Conforme indicado anteriormente, tome precauções para proteger a URL SAS. 
  
> [!IMPORTANT]
> Você precisa usar o Windows Azure AzCopy versão 5.0 para carregar arquivos PST com êxito o local de armazenamento do Azure. Versões mais recentes da ferramenta AzCopy não são suportadas para importar arquivos PST para o Office 365. Certifique-se de baixar a ferramenta de AzCopy na página **carregar arquivos pela rede** seguindo os procedimentos nesta etapa. 
  
1. Vá para [https://protection.office.com](https://protection.office.com).
    
2. Entrar no Office 365 usando as credenciais de uma conta de administrador em sua organização do Office 365.
    
3. No painel esquerdo, clique em **controle de dados** e clique em **Importar**.
    
4. Na página **Importar**, clique em **Ir para o serviço de Importação**.
    
5. Na página **Importar dados para o Office 365** , clique em **novo trabalho** ![ícone Adicionar](media/ITPro-EAC-AddIcon.gif)e clique em **mensagens de email de carregamento (arquivos. PST)**.
    
6. Na página **carregar arquivos através da rede** , na etapa 2, clique em **Mostrar SAS URL de carregamento de rede**.
    
7. Depois que a URL for exibida, copiá-lo e salvá-lo no arquivo onde você salvou as outras chaves. Certifique-se de copiar o URL completo. 
    
8. Na etapa 3, clique em **Baixar a ferramenta AzCopy do Windows Azure** para baixar e instalar a ferramenta de AzCopy do Windows Azure. 
    
9. Clique em **Executar**, na janela pop-up, para instalar a ferramenta AzCopy do Microsoft Azure. 
    
    > [!IMPORTANT]
    > Certifique-se instalar a ferramenta de AzCopy do Windows Azure no local padrão, que é `%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy` em um computador executando o Windows de 64 bits. Isso acontece porque quando você executa o O365ImportTool.exe na etapa 5, ele procura a ferramenta AzCopy neste local. 
  
10. Depois de instalar a ferramenta AzCopy do Azure, clique em **Baixar a ferramenta de importação e a criptografia de dados do Office 365**.
    
11. Na janela pop-up, clique em **Salvar** \> **Salvar como** para salvar o arquivo de O365ImportTool.zip para uma pasta no computador local. 
    
12. Extraia o arquivo O365ImportTool.zip.
    
13. Clique em **Cancelar** para fechar a página **carregar arquivos pela rede** . 
 
## <a name="step-5-encrypt-and-upload-your-pst-files-to-office-365"></a>Etapa 5: Criptografar e carregar seus arquivos PST para o Office 365

Depois que você concluiu a etapa 1, a etapa 4, você está pronto para usar a ferramenta de O365ImportTool.exe para criptografar e carregar arquivos PST para o Office 365. Essa ferramenta criptografa seus arquivos PST e, em seguida, carrega e armazenando-as em um local de armazenamento do Azure em nuvem da Microsoft. Para concluir esta etapa, os arquivos PST precisam estar localizado em um compartilhamento de arquivo ou o servidor de arquivos na sua organização. Isso é conhecido como o diretório de origem no procedimento a seguir. Cada vez que você executar a ferramenta O365ImportTool.exe, você vai pode especificar um diretório de origem diferente. 
  
1. Abra um prompt de comando no computador local.
    
2. Vá para o diretório em que instalou a ferramenta O365ImportTool.exe na etapa 4.
    
3. Execute o seguinte comando para criptografar e carregar arquivos PST para o Office 365.
    
    ```
    O365ImportTool.exe /srcdir:<Location of PST files> /protect-rmsserver:<RMS licensing location> /protect-tenantid:<BPOSId> /protect-key:<Symmetric key> /transfer:upload /upload-dest:<Network upload URL> /upload-destSAS:<SAS key>
    ```

    A tabela a seguir descreve os parâmetros e os valores necessários. Observe que as informações obtidas nas etapas anteriores são usadas nos valores desses parâmetros.
    
    |**Parameter**|**Descrição**|**Exemplo**|
    |:-----|:-----|:-----|
    | `/srcdir:` <br/> |Especifica o diretório de origem em sua organização que contém os arquivos PST que serão carregados para o Office 365.  <br/> | `/srcdir:\\FILESERVER01\PSTs` <br/> |
    | `/protect-rmsserver:` <br/> |Especifica o local de licenciamento para o seu serviço RMS do Azure. Use o valor do `LicensingIntranetDistributionPointUrl` propriedade que você obteve na etapa 3. Certifique-se ao redor do valor desse parâmetro com aspas duplas ("")<br/> | `/protect-rmsserver:"https://afcbd8ec-cb2b-4a1a-8246-0b4bc22d1978.rms.na.aadrm.com/_wmcs/licensing"` <br/> |
    | `/protect-tenantid:` <br/> |Especifica a identidade da sua organização de RMS do Azure. Use o valor do `BPOSId` propriedade que você obteve na etapa 3.<br/> | `/protect-tenantid:42745b33-2a5c-4726-8a2a-ca43caa0f74b` <br/> |
    | `/protect-key:` <br/> |Especifica a chave simétrica obtido na etapa 2. Certifique-se ao redor do valor desse parâmetro com aspas duplas ("").  <br/> | `/protect-key:"l+R+Umc5RGmSBh1oW+DoyMxm/h5h2JJXFcNOFiNp867="` <br/> |
    | `/transfer:` <br/> |Especifica se você carregar arquivos PST pela rede ou enviá-los em um disco rígido. O valor `upload` indica que você está carregando os arquivos pela rede. O valor `drive` indica que você estiver enviando os PSTs em um disco rígido.<br/> | `/transfer:upload` <br/> |
    | `/upload-dest:` <br/> |Especifica o destino no qual os arquivos PST serão carregados para; do Office 365 Esse é o local de armazenamento do Azure para sua organização. O valor para esse parâmetro consiste de URL de carregamento de rede da URL SAS que você copiou na etapa 4. Certifique-se ao redor do valor desse parâmetro com aspas duplas ("").<br/><br/> **Dica:** (Opcional) Você pode especificar uma subpasta no local para carregar os arquivos PST criptografados para armazenamento do Azure. Para fazer isso, adicionando um local de subpasta (após "ingestiondata") na URL de carregamento de rede. O primeiro exemplo não especifica uma subpasta; Isso significa que o PSTs serão carregados até a raiz (chamada *ingestiondata* ) do local de armazenamento do Azure. O segundo exemplo carrega os arquivos PST para uma subpasta (chamado *EncryptedPSTs* ) no local de armazenamento do Azure.           | `/upload-dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata"` <br/> Ou  <br/>  `/upload-dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata/EncryptedPSTs"` <br/> |
    | `/upload-destSAS:` <br/> |Especifica a chave SAS para sua organização. O valor para esse parâmetro consiste a chave SAS da URL SAS que você copiou na etapa 4. Observe que o primeiro caractere na chave SAS é um ponto de interrogação ("?"). Certifique-se ao redor do valor desse parâmetro com aspas duplas ("").  <br/> | `/upload-destSAS:"?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"` <br/> |
    | `/recurse` <br/> |Esta opção especifica o modo de recursiva para que a ferramenta de O365ImportTool.exe copiará arquivos PSTs que estão localizados em subpastas no diretório de origem especificado pelo `/srcdir:` parâmetro.  <br/><br/> **Observação:** Se você incluir este comutador, arquivos PST em subpastas terá um nome de caminho de arquivo diferente no local de armazenamento do Azure após terem sido carregadas. Você precisará especificar o caminho do arquivo exato no arquivo CSV que você criar na etapa 7.           | `/recurse` <br/> |
   
    Veja um exemplo da sintaxe para a ferramenta O365ImportTool.exe, que usa valores reais para os parâmetros:
    
    ```
    O365ImportTool.exe /srcdir:\\FILESERVER01\PSTs /protect-rmsserver:"https://afcbd8ec-cb2b-4a1a-8246-0b4bc22d1978.rms.na.aadrm.com/_wmcs/licensing" /protect-tenantid:42745b33-2a5c-4726-8a2a-ca43caa0f74b  /protect-key:"l+R+Umc5RGmSBh1oW+DoyMxm/h5h2JJXFcNOFiNp867=" /transfer:upload /upload-dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata" /upload-destSAS:"?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"
    ```

    Depois de executar o comando, o sistema exibe mensagens de status que mostram o andamento da criptografia e do carregamento dos arquivos PST. Uma mensagem de status final mostra o número total de arquivos que foram criptografados e carregados com êxito.  
    
    > [!TIP]
    > Depois de executar o comando O365ImportTool.exe com êxito e verificar se todos os parâmetros estão corretos, salvar uma cópia da sintaxe da linha de comando para o mesmo arquivo (protegido), onde você copiou as informações você obtido nas etapas anteriores. Em seguida, você pode copiar e colar esse comando em um Prompt de comando cada vez que você deseja executar a ferramenta de O365ImportTool.exe para criptografar e carregar arquivos PST para o Office 365. Os únicos valores que você pode precisar alterar são aqueles para o `/srcdir:` e `/upload-dest:` parâmetros. 
  
## <a name="optional-step-6-view-a-list-of-the-pst-files-uploaded-to-office-365"></a>(Opcional) Etapa 6: Exibir uma lista dos arquivos PST carregados para o Office 365

Como uma etapa opcional, você pode instalar e usar o Microsoft Azure Storage Explorer (que é uma ferramenta gratuita de código aberto) para exibir a lista dos arquivos PST que tenha carregado para o Azure blob. Há três boas razões para fazer isso:
  
- Verifique se que os arquivos PST na pasta compartilhada ou servidor de arquivos na sua organização com êxito foram carregados o Azure blob.

- Verifique se que os arquivos PST são criptografados. Os arquivos PST criptografados têm um `.pfile` extensão acrescentado ao nome do arquivo PST; Por exemplo, `pilarp.pst.pfile`.
    
- Verifique se o nome do arquivo (e o nome de caminho subpasta se você incluiu um) para cada arquivo PST carregado para o Azure blob. Isso é realmente útil quando você estiver criando o arquivo na próxima etapa de mapeamento porque você precisou para especificar o nome do caminho de pasta e o nome de arquivo para cada arquivo PST de PST. Verificando a esses nomes pode ajudar a reduzir os erros potenciais em seu arquivo de mapeamento de PST.
    
O Microsoft Azure Storage Explorer está no modo de visualização. 
  
 > [!IMPORTANT]
>  Você não pode usar o Gerenciador de armazenamento do Windows Azure para carregar ou modificar arquivos PST. O único método suportado para importar arquivos PST para o Office 365 é usar AzCopy. Além disso, você não pode excluir arquivos PST que tenha carregado para o Azure blob. Se você tentar excluir um arquivo PST, você receberá um erro sobre não ter as permissões necessárias. Observe que todos os arquivos PST automaticamente são excluídos da sua área de armazenamento do Azure. Se não houver nenhum trabalho de importação em andamento, em seguida, todos os arquivos de PST no contêiner **ingestiondata** é excluído 30 dias após o trabalho de importação mais recente foi criado. 
  
Para instalar o Windows Azure Storage Explorer e conectar-se a sua área de armazenamento do Azure:
  
1. Baixe e instale a [ferramenta Microsoft Azure Storage Explorer](https://go.microsoft.com/fwlink/p/?LinkId=544842).
    
2. Iniciar o Microsoft Azure Storage Explorer, clique com o botão **Contas de armazenamento** no painel esquerdo e, em seguida, clique em **conectar ao armazenamento do Azure**. 
    
    ![Clique com o botão contas de armazenamento e clique em conectar ao armazenamento do Azure](media/75b80cc3-c336-4f96-ad32-54ac9b96a7af.png)
  
3. Na caixa em **conectar ao armazenamento do Azure**, cole a URL de SAS obtido na etapa 4 e clique em **Avançar**. 
    
    ![Cole o URL do SAS na caixa conectar a página de armazenamento do Windows Azure](media/5d034128-e087-48e1-9ebc-4c9fa262d5b7.png)
  
4. Na página **Resumo da Conexão** , revise as informações de conexão e, em seguida, clique em **Conectar**. 
    
5. Em **Contas de armazenamento**, expanda o nó de **Serviço SAS ()** e expanda o nó de **Contêineres de Blob** . 
    
6. Clique com o botão **ingestiondata**e, em seguida, clique em **Abrir Editor de contêiner de Blob**.
    
    ![Clique com o botão direito em ingestiondata e clique em Abrir Editor de Contêiner de Blob.](media/f50eee30-9202-4efc-904a-2895a0bc388d.png)
  
    Área de armazenamento do Azure, com uma lista dos arquivos PST que você carregou na etapa 5 é exibida.
    
    ![O Azure Storage Explorer exibe uma lista dos arquivos PST que você carregou](media/a448ae43-e744-4153-8304-22b59e93883c.png)
  
7. Quando você terminar de usar o Microsoft Azure Storage Explorer, clique com o botão **ingestiondata**e clique em **Desanexar** para desconectar da sua área de armazenamento do Azure. Caso contrário, você receberá um erro na próxima vez que você tentar anexar. 
    
    ![Clique com o botão direito em inclusão e clique em Desconectar para desconectar da sua área de armazenamento do Azure](media/1e8e5e95-4215-4ce4-a13d-ab5f826a0510.png)
  
## <a name="step-7-create-the-pst-import-mapping-file"></a>Etapa 7: Criar o arquivo de mapeamento de importação de PST

Depois que os arquivos PST são criptografados e carregados no local de armazenamento do Azure para sua organização do Office 365, a próxima etapa é criar uma vírgula separados arquivo CSV (valor) que especifica quais caixas de correio de usuário dos arquivos PST será importados para. Quando você cria um trabalho de importação de PST, você enviará esse arquivo CSV na próxima etapa.
  
1. [Baixar uma cópia do arquivo de mapeamento de importação de PST](https://go.microsoft.com/fwlink/p/?LinkId=544717). 
    
2. Abrir ou salvar o arquivo CSV no computador local. O exemplo a seguir mostra um arquivo de mapeamento para Importação de PST concluído (aberto no Bloco de notas). É muito mais fácil usar o Microsoft Excel para editar o arquivo CSV.
    
    ```
    Workload,FilePath,Name,Mailbox,IsArchive,TargetRootFolder,ContentCodePage,SPFileContainer,SPManifestContainer,SPSiteUrl
    Exchange,,annb.pst.pfile,annb@contoso.onmicrosoft.com,FALSE,/,,,,
    Exchange,,annb_archive.pst.pfile,annb@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    Exchange,,donh.pst.pfile,donh@contoso.onmicrosoft.com,FALSE,/,,,,
    Exchange,,donh_archive.pst.pfile,donh@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    Exchange,EncryptedPSTs,pilarp.pst.pfile,pilarp@contoso.onmicrosoft.com,FALSE,,,,,
    Exchange,EncryptedPSTs,pilarp_archive.pst.pfile,pilarp@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    Exchange,EncryptedPSTs,tonyk.pst.pfile,tonyk@contoso.onmicrosoft.com,FALSE,,,,,
    Exchange,EncryptedPSTs,tonyk_archive.pst.pfile,tonyk@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    Exchange,EncryptedPSTs,zrinkam.pst.pfile,zrinkam@contoso.onmicrosoft.com,FALSE,,,,,
    Exchange,EncryptedPSTs,zrinkam_archive.pst.pfile,zrinkam@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    ```

    A primeira linha ou a linha de cabeçalho do arquivo CSV lista os parâmetros que serão usados pelo serviço de importação de PST para importar os arquivos PST para caixas de correio do usuário. O nome de cada parâmetro é separado por uma vírgula. Cada linha sob a linha de cabeçalho representa os valores de parâmetro para importar um arquivo PST para uma caixa de correio específica. Você precisará de uma linha para cada arquivo PST que você deseja importar uma caixa de correio do usuário. Certifique-se de substituir os dados de espaço reservado no arquivo de mapeamento com seus dados reais.
    
    > [!NOTE]
    > Não altere o conteúdo da linha de cabeçalho, inclusive os parâmetros SharePoint; eles serão ignorados durante o processo de Importação de PST. 
  
3. Use as informações da tabela a seguir para preencher o arquivo CSV com as informações necessárias.
    
    |**Parameter**|**Descrição**|**Exemplo**|
    |:-----|:-----|:-----|
    | `Workload` <br/> |Especifica que os dados serão importados para o serviço do Office 365. Para importar arquivos PST às caixas de correio do usuário, use `Exchange`.<br/> | `Exchange` <br/> |
    | `FilePath` <br/> |Especifica o local da pasta no local de armazenamento do Azure que você carregou os arquivos PST para na etapa 5.  <br/>  Se você não incluir um nome da subpasta opcional na URL na rede a `/upload-dest:` parâmetro na etapa 5, deixe esse parâmetro em branco no arquivo CSV. Se você incluiu o nome da subpasta, especificá-lo neste parâmetro. O valor para esse parâmetro diferencia maiusculas de minúsculas. De qualquer forma, *não* incluir "ingestiondata" no valor para o `FilePath` parâmetro.<br/> <br/>**Importante:** Caso o nome do caminho de arquivo deve ser usado se você incluiu um nome da subpasta opcional na URL SAS no mesmo caso o `/upload-dest:` parâmetro na etapa 5. Por exemplo, se você usou `EncryptedPSTs` para a subpasta nomeie na etapa 5 e, em seguida, use `encryptedpsts` no `FilePath` parâmetro no arquivo CSV, a importação do arquivo PST falhará. Certifique-se de usar o mesmo caso em ambas as instâncias.           |(deixar em branco)  <br/> Ou  <br/>  `EncryptedPSTs` <br/> |
    | `Name` <br/> |Especifica o nome do arquivo PST que será importado para a caixa de correio do usuário. O valor para esse parâmetro diferencia maiusculas de minúsculas. Como os arquivos PST que são carregados para o local de armazenamento do Azure são criptografados, um `.pfile` extensão é adicionada ao nome do arquivo PST. Você deve adicionar o `.pfile` arquivos de extensão ao nome do arquivo PST no arquivo CSV.<br/><br/> **Importante:** Caso o nome do arquivo PST no arquivo CSV deve ser o mesmo que o arquivo PST que foi atualizado para o local de armazenamento do Azure na etapa 5. Por exemplo, se você usar `annb.pst.pfile` no `Name` parâmetro no arquivo CSV, mas o nome do arquivo PST real é `AnnB.pst`, a importação desse arquivo PST falhará. Certifique-se de que o nome do arquivo PST no arquivo CSV usa o mesmo caso como o arquivo PST real.           | `annb.pst.pfile` <br/> |
    | `Mailbox` <br/> |Especifica o endereço de email da caixa de correio para a qual o arquivo PST será importado.   <br/> Para importar um arquivo PST para uma caixa de correio inativa, você precisa especificar a caixa de correio GUID para esse parâmetro. Para obter essa GUID, execute o seguinte comando do PowerShell no Exchange Online: ' Get-Mailbox - InactiveMailboxOnly<identity of inactive mailbox> | Guid FL` <br/><br/> **Note:** In some cases, you might have multiple mailboxes with the same email address, where one mailbox is an active mailbox and the other mailbox is in a soft-deleted (or inactive) state. In these situations, you have specify the mailbox GUID to uniquely identify the mailbox to import the PST file to. To obtain this GUID for active mailboxes, run the following PowerShell command:  `Get-Mailbox -<identity of active mailbox> | Guid FL`. To obtain the GUID for soft-deleted (or inactive) mailboxes, run this command  `Get-Mailbox - <identity of soft-deleted or inactive mailbox> - SoftDeletedMailbox | Guid FL'           | `annb@contoso.onmicrosoft.com` <br/> Ou  <br/>  `2d7a87fe-d6a2-40cc-8aff-1ebea80d4ae7` <br/> |
    | `IsArchive` <br/> | Especifica se deve ou não importar o arquivo PST para a caixa de correio de arquivo morto do usuário. Há duas opções:<br/> **FALSE** Importa o arquivo PST para a caixa de correio principal do usuário.  <br/> **TRUE** Importa o arquivo PST para o correio de arquivo morto do usuário.  <br/>  Se você deixar esse parâmetro em branco, o arquivo PST é importado para a caixa de correio principal do usuário.  <br/><br/> **Observação:** Para importar um arquivo PST para uma caixa de correio de arquivamento baseado em nuvem para um usuário cuja caixa de correio primária está no local, basta especificar **TRUE** para esse parâmetro e especifique o endereço de email para a caixa de correio do usuário no local para o `Mailbox` parâmetro.           | `FALSE` <br/> Ou  <br/>  `TRUE` <br/> |
    | `TargetRootFolder` <br/> | Especifica a pasta de caixa de correio importado para o arquivo PST.  <br/>  Se você deixar esse parâmetro em branco, o PST será importado para uma nova pasta denominada **importados** localizada no nível raiz da caixa de correio (o mesmo nível que a pasta de caixa de entrada e as outras pastas de caixa de correio padrão).  <br/>  Se você especificar `/`, itens no arquivo PST serão importados diretamente na pasta de caixa de entrada do usuário.  <br/>  Se você especificar `/<foldername>`, itens no arquivo PST serão importados para uma subpasta chamada * \<foldername\> * . Por exemplo, se você usou `/ImportedPst`, itens seriam importadas para uma subpasta chamada **ImportedPst**. Essa subpasta estará localizada na pasta de caixa de entrada do usuário.<br/><br/> **Dica:** Considere a execução de alguns lotes de teste para experimentar com esse parâmetro para que você possa determinar o melhor local de pasta para importar arquivos de PSTs para.           |(deixar em branco)  <br/> Ou  <br/>  `/` <br/> Ou  <br/>  `/ImportedPst` <br/> |
    | `ContentCodePage` <br/> |Esse parâmetro opcional especifica um valor numérico para a página de código a ser usado para importação de arquivos PST no formato de arquivo ANSI. Este parâmetro é usado para importar arquivos PST organizações chinês, japonês e coreano (CJK) porque esses idiomas geralmente usam um conjunto de caracteres de byte duplo (DBCS) para codificação de caracteres. Se esse parâmetro não é usado para importar arquivos PST para idiomas que usam DBCS para nomes de pasta de caixa de correio, os nomes de pasta frequentemente são truncados após a importação. Para obter uma lista de valores suportados para usar para esse parâmetro, consulte [Identificadores de página de código](https://go.microsoft.com/fwlink/p/?LinkId=328514).<br/><br/> **Observação:** Conforme anteriormente mencionado, este é um parâmetro opcional e você não tiver incluí-lo no arquivo CSV. Ou você pode incluí-lo e deixe o valor em branco para uma ou mais linhas.           |(deixar em branco)  <br/> Ou  <br/>  `932`(que é o identificador de página de código para ANSI/OEM japonês)  <br/> |
    | `SPFileContainer` <br/> |Deixe este parâmetro em branco para Importação de PST.   <br/> |Não aplicável  <br/> |
    | `SPManifestContainer` <br/> |Deixe este parâmetro em branco para Importação de PST.   <br/> |Não aplicável  <br/> |
    | `SPSiteUrl` <br/> |Deixe este parâmetro em branco para Importação de PST.   <br/> |Não aplicável  <br/> |
  
## <a name="step-8-create-a-pst-import-job-in-office-365"></a>Etapa 8: criar um trabalho de Importação de PST no Office 365

A última etapa é criar o trabalho de importação de PST no serviço de importação no Office 365. Conforme explicado anteriormente, você enviará o arquivo de mapeamento de importação de PST que você criou na etapa 7. Após criar o novo trabalho, o serviço de importação usará as informações no arquivo de mapeamento para un-criptografar e importe os arquivos PST (que você carregou para o Office 365 na etapa 5) na caixa de correio do usuário especificado. 
  
1. Vá para [https://protection.office.com](https://protection.office.com).
    
2. Entrar no Office 365 usando as credenciais de uma conta de administrador em sua organização do Office 365.
    
3. No painel esquerdo, clique em **controle de dados** e clique em **Importar**.
    
4. Na página **Importar**, clique em **Ir para o serviço de Importação**.
    
5. Na página **Importar dados para o Office 365** , clique em **novo trabalho**![ícone Adicionar](media/ITPro-EAC-AddIcon.gif)e clique em **mensagens de email de carregamento (arquivos. PST)**.
    
6. Na página **Carregar dados pela rede**, marque as caixas de seleção **Eu acabei de carregar os meus arquivos** e **Eu tenho acesso ao arquivo de mapeamento** e clique em **Avançar**.  
    
7. Digite um nome para o trabalho de Importação de PST e clique em **Avançar**.
    
8. Clique em **Adicionar** ![ícone Adicionar](media/ITPro-EAC-AddIcon.gif) para selecionar o arquivo de mapeamento de PST que você criou na etapa 7. 
    
9. Quando o nome do arquivo CSV for exibido na lista, selecione-o e clique em **Validar** para verificar se há falhas no arquivo.  
    
    > [!NOTE]
    > Explicado como anterior, quando os arquivos PST são criptografados, um `.pfile` extensão é acrescentada ao nome do arquivo PST. Você deve adicionar o `.pfile` arquivos de extensão ao nome do arquivo PST no arquivo CSV. Caso contrário, a validação do arquivo CSV falhará. 
  
    Você deve validar o arquivo CSV com êxito para poder criar um trabalho de Importação de PST. Se a validação falhar, clique no link **Inválida**, na coluna **Status**. O sistema vai abrir uma cópia do arquivo de mapeamento para Importação de PST, incluindo uma mensagem de erro para cada linha do arquivo que apresentar falha. 
    
10. Quando validar o arquivo de mapeamento para Importação de PST com êxito, leia o documento de termos e condições e marque a caixa de seleção.
    
11. Clique em **Concluir** para enviar o trabalho. 
    
    O trabalho é exibido na lista de trabalhos de importação de PST na página **Importar dados para o Office 365** . 
    
12. Selecione o trabalho e clique em **Atualizar**![ícone atualizar](media/O365-MDM-Policy-RefreshIcon.gif) para atualizar as informações de status são exibidas no painel de detalhes. 
    
13. No painel de detalhes, clique em **Exibir detalhes** para conferir o status mais recente do trabalho escolhido. 
 
## <a name="more-information"></a>Mais informações

- Por que importar arquivos PST para o Office 365?
    
  - É uma boa maneira de migrar email de sua organização para o Office 365.
    
  - Isso ajuda a atender às necessidades de conformidade da organização, permitindo:
    
  - Habilitar as caixas de correio de arquivo morto para conceder mais espaço de armazenamento de caixa de correio aos usuários.
    
  - Colocar as caixas de correio em retenção para preservar o conteúdo.
    
  - Use as ferramentas de Descoberta Eletrônica da Microsoft para pesquisar conteúdo em caixas de correio.
    
  - Use Políticas de Retenção para controlar o tempo de retenção do conteúdo da caixa de correio.
    
  - Pesquise o log de auditoria do Office 365 para eventos relacionados à caixa de correio.
    
  - Ele ajuda a proteger contra perda de dados. Arquivos PST que são importados para caixas de correio do Office 365 herdam os recursos de alta disponibilidade do Exchange Online, em vez de armazenar os dados em um computador do usuário.
    
  - Os dados ficam disponíveis para o usuário em todos os dispositivos, pois eles são armazenados na nuvem.
    
- Aqui está um exemplo de como as chaves, IDs e URLs que são obtidos nas etapas 2, 3 e 4. Este exemplo também contém a sintaxe para o comando que você execute na ferramenta O365ImportTool.exe para criptografar e PST de carregamento de arquivos para o Office 365. Certifique-se de que tome precauções para proteger esses apenas como você faria proteger senhas ou outras informações relacionadas à segurança.
    
  ```
  Symmetric key: l+R+Umc5RGmSBh1oW+DoyMxm/h5h2JJXFcNOFiNp867=

  BPOSId: 42745b33-2a5c-4726-8a2a-ca43caa0f74b

  LicensingIntranetDistributionPointUrl (RMS licensing location): https://afcbd8ec-cb2b-4a1a-8246-0b4bc22d1978.rms.na.aadrm.com/_wmcs/licensing
  
  SAS URL: https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D
  
  O365ImportTool.exe /srcdir:<Location of PST files> /protect-rmsserver:<RMS licensing location> /protect-tenantid:<BPOSId> /protect-key:<Symmetric key> /transfer:upload /upload-dest:<Network upload URL from the SAS URL> /upload-destSAS:<SAS key from the SAS URL>
  
  EXAMPLES
  
  This example uploads PST files to the root of the Azure storage location:

  O365ImportTool.exe /srcdir:\\FILESERVER01\PSTs /protect-rmsserver:"https://afcbd8ec-cb2b-4a1a-8246-0b4bc22d1978.rms.na.aadrm.com/_wmcs/licensing" /protect-tenantid:42745b33-2a5c-4726-8a2a-ca43caa0f74b /protect-ownerid:45beb445-4d06-47df-8e61-6ca1a88a080e /protect-key:"l+R+Umc5RGmSBh1oW+DoyMxm/h5h2JJXFcNOFiNp867=" /transfer:upload /upload-dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata" /upload-destSAS:"?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"
  
  This example uploads PST files to a subfolder named EncryptedPSTs  in the Azure storage location:
  
  O365ImportTool.exe /srcdir:\\FILESERVER01\PSTs /protect-rmsserver:"https://afcbd8ec-cb2b-4a1a-8246-0b4bc22d1978.rms.na.aadrm.com/_wmcs/licensing" /protect-tenantid:42745b33-2a5c-4726-8a2a-ca43caa0f74b /protect-ownerid:45beb445-4d06-47df-8e61-6ca1a88a080e /protect-key:"l+R+Umc5RGmSBh1oW+DoyMxm/h5h2JJXFcNOFiNp867=" /transfer:upload /upload-dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata/EncryptedPSTs" /upload-destSAS:"?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"
  ```

- Conforme explicado anteriormente, o serviço de importação do Office 365 ativa a retenção de configuração (por um período indefinido) depois de arquivos PST são importados para uma caixa de correio. Isso significa que a propriedade *RentionHoldEnabled* estiver definida como `True` para que a política de retenção atribuída à caixa de correio não será processada. Isso permite que o tempo de proprietário da caixa de correio para gerenciar as mensagens recentemente importados, impedindo a execução uma exclusão ou a política de arquivamento de exclusão ou arquivamento de mensagens mais antigas. Aqui estão algumas etapas a que seguir para gerenciar esse status em retenção: 
    
  - Depois de certo período de tempo, você pode desativar o status em retenção, executando o `Set-Mailbox -RetentionHoldEnabled $false` comando. Para obter instruções, consulte [retenção local de uma caixa de correio em retenção](https://go.microsoft.com/fwlink/p/?LinkId=544749).
    
  - Você pode configurar o intervalo de retenção para que ele está desativado em alguns data no futuro. Você pode fazer isso executando o `Set-Mailbox -EndDateForRetentionHold <date>` comando. Por exemplo, supondo que a data de hoje é 1 de julho de 2016 e você quiser que o status em retenção desativado no 30 dias, execute o seguinte comando: `Set-Mailbox -EndDateForRetentionHold 8/1/2016`. Neste cenário, você poderia deixar a propriedade *RentionHoldEnabled* definida como `True`. Para obter mais informações, consulte [Set-Mailbox](https://go.microsoft.com/fwlink/p/?LinkId=150317).
    
  - Você pode alterar as configurações para a política de retenção que é atribuída à caixa de correio, de forma que os itens mais antigos que foram importados não ser imediatamente excluídos ou movidos para a caixa de correio de arquivo morto do usuário. Por exemplo, você pode aumentar a idade de retenção para uma política de exclusão ou arquivamento atribuída à caixa de correio. Neste cenário, você faria desativar a retenção suspensa na caixa de correio depois que você alterou as configurações da política de retenção. Para obter mais informações, consulte [Configurar uma política de arquivamento e exclusão de caixas de correio em sua organização do Office 365](set-up-an-archive-and-deletion-policy-for-mailboxes.md).

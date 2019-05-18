---
title: Usar um exemplo de conector para arquivar dados do Facebook no Office 365 (versão prévia)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
description: Os administradores podem configurar um conector nativo para importar dados de terceiros de fontes de dados, como páginas de negócios do Facebook, páginas da empresa do LinkedIn e Bloomberg instantâneo. Isso permite que você arquive dados de fontes de dados de terceiros no Office 365 para que possa usar recursos de conformidade, como retenção legal, pesquisa de conteúdo e políticas de retenção para gerenciar a governança dos dados de terceiros da sua organização.
ms.openlocfilehash: 7a71eac07d3d3260809f90cd2e470c32c44e9dda
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34152183"
---
# <a name="use-a-sample-connector-to-archive-facebook-data-in-office-365-preview"></a>Usar um exemplo de conector para arquivar dados do Facebook no Office 365 (versão prévia)

O recurso de conector de exemplo para arquivar dados do Facebook no Office 365 está em versão prévia..

Use um conector de exemplo no centro de conformidade do & de segurança no Office 365 para importar e arquivar dados de fontes de dados de terceiros, como páginas de negócios do Facebook, LinkedIn, Twitter e Bloomberg. Depois de configurar e configurar um conector de exemplo, ele se conecta à fonte de dados de terceiros (em uma base agendada), converte o conteúdo de um item em um formato de mensagem de email e, em seguida, importa esses itens para uma caixa de correio no Office 365.

Após a importação dos dados de terceiros, é possível aplicar recursos de conformidade do Office 365, como retenção de litígio, pesquisa de conteúdo, arquivamento in-loco, auditoria, supervisão e políticas de retenção do Office 365 aos dados de terceiros. Por exemplo, quando uma caixa de correio é colocada em retenção de litígio ou atribuída a uma política de retenção, os dados de terceiros serão mantidos. Você pode pesquisar dados de terceiros usando a pesquisa de conteúdo ou associá-los a um funcionário em um caso de descoberta eletrônica avançada. O uso de conectores de amostra para importar e arquivar dados de terceiros no Office 365 pode ajudar sua organização a se manter em conformidade com as políticas governamentais e regulamentares.

> [!NOTE]
> Atualmente, somente os conectores de amostra para páginas de negócios do Facebook e o [Twitter](archive-twitter-data-with-sample-connector.md) estão disponíveis para visualização. Mais exemplos de conectores serão disponibilizados em breve.


## <a name="prerequisites-for-setting-up-a-connector-for-facebook-business-pages"></a>Pré-requisitos para configurar um conector para páginas de negócios do Facebook

Você deve concluir os pré-requisitos a seguir antes de configurar e configurar um conector de exemplo no centro de conformidade do & de segurança para importar e arquivar dados das páginas de negócios de Facebook da sua organização. 

- Você precisa de uma conta do Facebook para as páginas de negócios da sua organização (você precisa fazer logon nessa conta ao configurar o conector). Atualmente, você só pode arquivar dados de páginas de negócios do Facebook; Você não pode arquivar dados de perfis individuais do Facebook.

- Sua organização deve ter uma assinatura válida do Azure. Se você não tiver uma assinatura do Azure existente, poderá se inscrever em uma destas opções:

    - [Inscreva-se para obter uma assinatura gratuita do Azure em 1 ano](https://azure.microsoft.com/free) 

    - [Inscreva-se para obter uma assinatura do Azure de pagamento conforme a ser acessado](https://azure.microsoft.com/pricing/purchase-options/pay-as-you-go/)

    > [!NOTE]
    > A [assinatura gratuita do Azure Active Directory](use-your-free-azure-ad-subscription-in-office-365.md) incluída na assinatura do Office 365 não dá suporte aos conectores de amostra no centro de conformidade do _AMP_ de segurança.

- Sua organização deve dar o consentimento para permitir que o serviço de importação do Office 365 acesse dados de caixa de correio em sua organização. Para concordar com essa solicitação, acesse [esta página](https://login.microsoftonline.com/common/oauth2/authorize?client_id=570d0bec-d001-4c4e-985e-3ab17fdc3073&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent), entre com as credenciais de um administrador global do Office 365 e aceite a solicitação.

- O usuário que configura o conector personalizado na conformidade de & de segurança (na etapa 7) deve ser atribuído à função de exportação de importação de caixa de correio no Exchange Online. Por padrão, essa função não é atribuída a nenhum grupo de função no Exchange Online. Você pode adicionar a função de exportação de importação de caixa de correio ao grupo de funções Gerenciamento da organização no Exchange Online. Ou você pode criar um novo grupo de função, atribua a função de exportação de importação de caixa de correio e, em seguida, adicione os usuários apropriados como membros. Para obter mais informações, consulte as seções [criar grupos de função](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#create-role-groups) ou [modificar grupos de função](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#modify-role-groups) no artigo "gerenciar grupos de função no Exchange Online".

## <a name="step-1-download-the-pre-built-connector-app-package-from-github"></a>Etapa 1: baixar o pacote de aplicativos do conector pré-criado do github

A primeira etapa é baixar o código-fonte para o aplicativo de conector do Facebook pré-criado que usará uma API do Facebook para se conectar às suas páginas de negócios do Facebook e extrair os dados do Facebook para que você possa importá-lo para o Office 365.

1. Vá para [este site do GitHub](https://github.com/Microsoft/m365-sample-connector-csharp-aspnet/releases). 
2. Na versão mais recente, clique no arquivo **SampleConnector. zip** .
3. Salve o arquivo ZIP em um local no computador local. Você carregará este arquivo zip no Azure na etapa 4.

## <a name="step-2-create-an-app-in-azure-active-directory"></a>Etapa 2: criar um aplicativo no Azure Active Directory

A próxima etapa é registrar um novo aplicativo no Azure Active Directory (AAD). Este aplicativo corresponderá ao recurso do aplicativo Web que você implementará na etapa 4 para o conector do Facebook. 

Para obter instruções detalhadas, consulte [criar um aplicativo no Azure Active Directory](deploy-facebook-connector.md#step-2-create-an-app-in-azure-active-directory).

Durante a conclusão desta etapa (seguindo as instruções passo a passo), você salvará as informações a seguir em um arquivo de texto. Os valores para eles serão usados nas etapas posteriores do processo de implantação.

- ID do aplicativo AAD
- Segredo do aplicativo AAD
- URI do aplicativo AAD
- ID do locatário

## <a name="step-3-create-an-azure-storage-account"></a>Etapa 3: criar uma conta de armazenamento do Azure

O conector do Facebook que você implantar para sua organização carregará os itens de suas páginas de negócios do Facebook para o local de armazenamento do Azure que você criar nesta etapa. Após criar um conector personalizado no centro de conformidade do & de segurança (na etapa 7), o serviço de importação do Office 365 copiará os dados do Facebook do local de armazenamento do Azure para uma caixa de correio no Office 365. Conforme explicado anteriormente na seção [pré-requisitos](#prerequisites-for-setting-up-a-connector-for-facebook-business-pages) , você deve ter uma assinatura válida do Azure para criar uma conta de armazenamento do Azure.

Para obter instruções detalhadas, consulte [criar uma conta de armazenamento do Azure](deploy-facebook-connector.md#step-3-create-an-azure-storage-account).

Durante a conclusão desta etapa (seguindo as instruções passo a passo), você salvará o URI da cadeia de caracteres de conexão gerado. Você usará essa cadeia de caracteres ao criar um recurso do aplicativo Web no Azure na etapa 4.

## <a name="step-4-create-a-web-app-resource-in-azure"></a>Etapa 4: criar um recurso do aplicativo Web no Azure

A próxima etapa é criar um recurso do aplicativo Web no Azure para o conector do Facebook. 

Para obter instruções detalhadas, consulte [criar um novo recurso do aplicativo Web no Azure](deploy-facebook-connector.md#step-4-create-a-new-web-app-resource-in-azure).

Durante a conclusão desta etapa (seguindo as instruções passo a passo), você fornecerá as seguintes informações (que você copiou para um arquivo de texto depois de concluir as etapas anteriores) ao criar o recurso do aplicativo Web.

- APISecretKey – você criará esse segredo durante a conclusão desta etapa; Ele será usado na etapa 7.
- StorageAccountConnectionString – o URI da cadeia de caracteres de conexão que você copiou após a criação da conta de armazenamento do Azure na etapa 3.
- tenantid – a ID do locatário de sua organização do Office 365 que você copiou depois de criar o aplicativo do Facebook Connector no Azure Active Directory na etapa 2.

Além disso, você carregará o arquivo SampleConnector. zip (que você baixou na etapa 1) nesta etapa para implantar o código-fonte do aplicativo do Facebook Connector.

Após concluir esta etapa, certifique-se de copiar a URL do serviço de aplicativo ( https://fbconnector.azurewebsites.net)por exemplo,. Você precisará usá-lo para concluir a etapa 5, etapa 6 e etapa 7).

## <a name="step-5-register-the-web-app-on-facebook"></a>Etapa 5: registrar o aplicativo Web no Facebook

A próxima etapa é criar e configurar um novo aplicativo no Facebook. O conector personalizado criado na etapa 7 usará o Facebook Web App para interagir com a API do Facebook, a fim de obter dados das páginas de negócios do Facebook da sua organização.

Para obter instruções passo a passo, consulte [Register The Facebook app](deploy-facebook-connector.md#step-5-register-the-facebook-app).

Durante a conclusão desta etapa (seguindo as instruções passo a passo), você salvará as informações a seguir em um arquivo de texto. Os valores para eles serão usados para configurar o aplicativo do Facebook Connector na etapa 6.

- ID do aplicativo do Facebook
- Segredo do aplicativo do Facebook
- Token de verificação de WebHooks do Facebook

## <a name="step-6-configure-the-facebook-connector-app"></a>Etapa 6: configurar o aplicativo do Facebook Connector

A próxima etapa é adicionar configurações de configurações ao aplicativo do Facebook Connector carregado quando você criou o recurso do Azure Web App na etapa 4. Você fará isso indo para a home page do seu aplicativo conector e configurá-lo.

Para obter instruções detalhadas, consulte [etapa 6: Configure the Connector Web App](deploy-facebook-connector.md#step-6-configure-the-connector-web-app).

Durante a conclusão desta etapa (seguindo as instruções passo a passo), você fornecerá as seguintes informações (que você copiou para um arquivo de texto depois de concluir as etapas anteriores):

- ID do aplicativo do Facebook (obtida na etapa 5)
- Segredo do aplicativo do Facebook (obtido na etapa 5)
- Token de verificação de WebHooks do Facebook (obtido na etapa 5)
- ID de aplicativo do Azure Active Directory (a ID de aplicativo do AAD obtida na etapa 2)
- Segredo de aplicativo do Azure Active Directory (o segredo do aplicativo AAD obtido na etapa 2)
- URI do aplicativo do Azure Active Directory (o URI do aplicativo AAD obtido na etapa 2; por exemplo,https://microsoft.onmicrosoft.com/2688yu6n-12q3-23we-e3ee-121111123213)

## <a name="step-7-set-up-a-custom-connector-in-the-security--compliance-center"></a>Etapa 7: configurar um conector personalizado no centro de conformidade do & de segurança

A etapa final é configurar o conector personalizado no centro de conformidade do & de segurança, que importará dados de suas páginas de negócios do Facebook para uma caixa de correio especificada no Office 365. Depois de concluir com êxito esta etapa, o serviço de importação do Office 365 iniciará o processo de importação de dados de suas páginas de negócios do Facebook para o Office 365. 

Para obter instruções detalhadas, consulte [configurar um conector personalizado no centro de conformidade do & de segurança](deploy-facebook-connector.md#step-7-set-up-a-custom-connector-in-the-security--compliance-center). 

Durante a conclusão desta etapa (seguindo as instruções passo a passo), você fornecerá as seguintes informações (que você copiou para um arquivo de texto depois de concluir as etapas).

- URL do serviço de aplicativo do Azure (obtido na etapa 4; por exemplohttps://fbconnector.azurewebsites.net)
- APISecretKey (que você criou na etapa 4)

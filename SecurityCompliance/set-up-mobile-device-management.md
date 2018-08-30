---
title: Definir backup Mobile Device Management (MDM) no Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: get-started-article
f1_keywords:
- O365M_OverviewMDM
- 'O365E_OverviewMDM '
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: dd892318-bc44-4eb1-af00-9db5430be3cd
description: O gerenciamento de dispositivos móveis internos para o Office 365 ajuda a proteger e gerenciar dispositivos móveis dos usuários, como iPhones, iPads, Androids, e telefones do Windows. Para começar, siga estas etapas para ativar e configurar o gerenciamento de dispositivos móveis para o Office 365.
ms.openlocfilehash: c92290170b2937067e7407787282eaaa368b25b7
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272356"
---
# <a name="set-up-mobile-device-management-mdm-in-office-365"></a>Definir backup Mobile Device Management (MDM) no Office 365

O internas Mobile Device Management (MDM) para o Office 365 ajuda a proteger e gerenciar dispositivos móveis dos usuários, como iPhones, iPads, Androids, e telefones do Windows. Você pode criar e gerenciar diretivas de segurança de dispositivo, remotamente apagar um dispositivo e exibir relatórios detalhados de dispositivo.
  
Tem dúvidas? Nós incluímos [uma FAQ para ajudar a perguntas comuns sobre o endereço](frequently-asked-questions-about-mdm.md). Lembre-se de que você não pode usar um [parceiros: administração delegada de oferta](https://support.office.com/article/26530dc0-ebba-415b-86b1-b55bc06b073e) para gerenciar o gerenciamento de dispositivos móveis para o Office 365. 
  
Gerenciamento de dispositivo é parte da segurança &amp; Centro de conformidade, portanto você precisará ir para disparar a instalação MDM lá.
  
Para configurar o gerenciamento de dispositivos móveis para o Office 365 você precisará:
  
1. [Ativar o serviço de gerenciamento de dispositivos móveis](#activate-the-mobile-device-management-service)  
2. [Configurar o gerenciamento de dispositivos móveis](#set-up-mobile-device-management)
3. [Certifique-se de usuários inscrever seus dispositivos](#step-4-recommended-manage-device-security-policies)
  
## <a name="activate-the-mobile-device-management-service"></a>Ativar o serviço de gerenciamento de dispositivos móveis

1. Entre no Office 365 com sua conta corporativa ou de estudante. 
    
2. Vá para [segurança &amp; Centro de conformidade](https://protection.office.com).
    
3. Navegue até a **prevenção de perda de dados** \> **gerenciamento de dispositivo** e clique em **Vamos começar** disparar o processo de ativação. 
    
    ![Configurar o gerenciamento de dispositivos móveis para o Office 365](media/368e1026-9aa5-431b-a722-8f7cf528f263.png)
  
4. Criamos uma política de segurança padrão para você para ajudá-lo a começar. Atualize o nome da diretiva de segurança nesta página e clique em **Iniciar a instalação**.
    
    ![Definir a diretiva de segurança de gerenciamento de dispositivos móveis](media/5619a2d1-f900-4268-9050-5d7eb57429a5.png)
  
5. Você verá a tela de instalação que mostra o andamento sobre como configurar o serviço.
    
    ![Progresso da instalação MDM](media/db45d1bb-d247-4ac0-9deb-1b0c1ace9bfa.png)
  
> [!TIP]
> Você também pode localizar **MDM instalação** por meio de pesquisa. No Centro de administração do Office 365 \> página **inicial** , tipo de gerenciamento de dispositivos móveis na caixa **Pesquisar** . > ![Pesquisa para o gerenciamento de dispositivos móveis no Centro de administração](media/cd0ebf15-ef79-4eaa-ab5b-041ac0bd4e5b.png)
  
Ela pode levar algum tempo para ativar o gerenciamento de dispositivos móveis para o Office 365, mas quando ele estiver concluída, você receberá um email que explica as próximas etapas para usar.
  
## <a name="set-up-mobile-device-management"></a>Configurar o gerenciamento de dispositivos móveis

Quando o serviço estiver pronto, conclua as quatro etapas a seguintes para concluir a instalação. Você talvez precise clicar em [Gerenciar configurações](https://portal.office.com/EAdmin/Device/IntuneInventory.aspx) na página **gerenciamento de dispositivo** na segurança &amp; Centro de conformidade para ver as configurações a seguir. 
  
![Configurar o gerenciamento de dispositivo móvel etapas obrigatórias e recomendadas](media/d71e3c76-b6b9-4549-ade6-cbfab846d908.png)
  
### <a name="step-1-required-configure-domains-for-mdm"></a>Etapa 1: Domínios de Configure (obrigatório) para MDM

Se você não tiver um domínio personalizado associado com o Office 365 ou se não estiver gerenciando dispositivos do Windows, você poderá ignorar esta seção. Caso contrário, você precisará adicionar registros DNS para o domínio no seu host DNS. Se você adicionou os registros já, como parte da configuração do seu domínio ao Office 365, você all está definido. Depois de adicionar os registros, os usuários do Office 365 em sua organização que entram em seu dispositivo do Windows com um endereço de email que usa seu domínio personalizado serão redirecionados para registrar-se no MDM para o Office 365.
  
Precisa de ajuda para configurar os registros? Encontre seu registrador de domínio na lista fornecida em [criar registros DNS para Office 365 ao gerenciar seus registros DNS](https://support.office.com/article/b0f3fdca-8a80-4e8e-9ef3-61e8a2a9ab23) e selecione o nome do registrador para ir para a ajuda passo a passo para a criação de registros DNS. Use essas instruções para adicionar os dois registros a seguintes: 
  
|**Nome do host**|**Tipo de registro**|**Endereço**|**TTL**|
|:-----|:-----|:-----|:-----|
|EnterpriseEnrollment  <br/> |CNAME  <br/> |EnterpriseEnrollment.manage.microsoft.com  <br/> |3600  <br/> |
|EnterpriseRegistration  <br/> |CNAME  <br/> |EnterpriseRegistration.windows.net  <br/> |3600  <br/> |
   
Depois de adicionar os dois registros, volte para a segurança &amp; Centro de conformidade e navegue até **gerenciamento de dispositivo** \> **Gerenciar configurações** para concluir a próxima etapa. 
  
### <a name="step-2-required-configure-an-apns-certificate-for-ios-devices"></a>Etapa 2: Configure (obrigatório) um certificado APNs para dispositivos iOS

Para gerenciar dispositivos iOS como iPad e iPhones, você precisará criar um certificado APNs.
  
Para fazer isso, siga as etapas nos links **Configurar** na **página de gerenciamento de dispositivo móvel de instalação**.
  
1. Ao lado de **Configurar um certificado de APNs para dispositivos iOS**, selecione **Configurar**.
    
2. Selecione **baixar seu arquivo CSR** e salve a solicitação de certificado de assinatura em algum lugar no seu computador que irá se lembrar. 
    
    ![Instalar a caixa de diálogo certificado APN](media/03aa8a24-e95c-4077-9b6b-ef76a86bafd7.png)
  
3. Selecione **Avançar**.
    
4. Crie um certificado APN.
    
  - Selecione **Apple APNS Portal** para abrir o Portal de certificados do Apple Push. 
    
    ![Instalar a caixa de diálogo de cert de notificação de APN com o Portal do Apple APNS selecionado](media/ce19f53c-f44a-470b-baf3-9278dfda2ba5.png)
  
  - Entrar com uma ID de Apple.
    
    > [!IMPORTANT]
    > Use uma empresa que Apple ID associado a uma conta de email que permanecerão com sua organização, mesmo se deixa o usuário que gerencia a conta. Salve este ID, pois você precisará usar a mesma identificação quando é hora de renovar o certificado. 
  
  - Selecione **criar um certificado** e aceitar os **Termos de uso**.
    
  - **Navegue** para a assinatura de certificado solicitar que você baixou para seu computador do Office 365 e selecione **carregar**.
    
  - **Baixar** o certificado APN criados pelo Portal de certificado do Apple Push ao seu computador. 
    
    > [!TIP]
    > Se você estiver tendo problemas baixando o certificado, atualize o navegador. 
  
5. Voltar para o Office 365 e selecione **Avançar** para chegar à página **APNS carregar certificado** . 
    
6. Navegue até o certificado APN que você baixou a partir do Portal de certificados do Apple Push.
    
    ![Clique no botão Procurar para selecionar o cert APNS que você baixou da Apple](media/afe2849d-af23-4c55-9009-d8f25edaf6c0.png)
  
7. Selecione **Concluir**.
    
Depois de Adicionar certificado APN, volte para a segurança &amp; Centro de conformidade e navegue até **gerenciamento de dispositivo** \> **Gerenciar configurações** para concluir a próxima etapa. 
  
### <a name="step-3-recommended-set-up-multi-factor-authentication"></a>Etapa 3: (Recomendado) configurar a autenticação multifator

Se você não vir a autenticação multifator (MFA) em **etapas recomendado**, você pode ignorar esta seção. Se essa opção estiver listada, recomendamos que você ativar MFA no portal do Azure AD para aumentar a segurança do gerenciamento de dispositivo móvel para o processo de inscrição do Office 365. Ele está desativado por padrão.
  
MFA ajuda a proteger o entrar no Office 365 para o registro do dispositivo móvel exigindo uma segunda forma de autenticação. Os usuários são necessários para confirmar a uma chamada telefônica, uma mensagem de texto ou uma notificação de aplicativo em seu dispositivo móvel depois de inserir corretamente suas senhas de conta do trabalho. Eles só podem se inscrever seus dispositivos concluída a essa segunda forma de autenticação. Depois que os dispositivos dos usuários são inscritos no gerenciamento de dispositivos móveis para o Office 365, os usuários podem acessar os recursos do Office 365 com apenas sua conta do trabalho.
  
Ao lado de **Configurar a autenticação multifator**, selecione **Configurar**. Para saber como ativar MFA no portal do Azure AD, consulte [Configurar a autenticação multifator](https://go.microsoft.com/fwlink/p/?LinkId=519255).
  
Depois de configurar MFA, volte para a segurança &amp; Centro de conformidade e navegue até **gerenciamento de dispositivo** \> **Gerenciar configurações** para concluir a próxima etapa. 
  
### <a name="step-4-recommended-manage-device-security-policies"></a>Etapa 4: Diretivas de segurança de dispositivo gerenciar (recomendado)

A próxima etapa é criar e implantar diretivas de segurança de dispositivo para ajudar a proteger os dados do sua organização Office 365. Por exemplo, você pode ajudar a evitar a perda de dados se um usuário perder seus dispositivos criando uma política para dispositivos de bloqueio após cinco minutos de inatividade e ter dispositivos apagada após 3 falhas entrar.
  
No **segurança &amp; Centro de conformidade**, acesse **as diretivas de segurança** \> **diretivas de segurança de dispositivo** para criar políticas de segurança de dispositivo e regras de acesso. 
  
![Adicionar uma diretiva de segurança de dispositivo](media/69a027f5-fbfb-482a-b850-9ccb280b8c62.png)
  
Para obter instruções passo a passo sobre como criar uma nova política, consulte [criar e implantar diretivas de segurança de dispositivo](create-device-security-policies.md).
  
> [!TIP]
>  Quando você cria uma nova política, você talvez queira definir a diretiva para permitir que violação de política de acesso e o relatório em que um dispositivo do usuário não é compatível com a política. Isso permite que você veja quantos dispositivos móveis poderiam ser afetados pela política sem bloqueio de acesso para o Office 365. > Antes de implantar uma nova diretiva para todas as pessoas na sua organização, é recomendável que testá-lo nos dispositivos usados por um pequeno número de usuários. > Além disso, antes de implantar políticas, permitem que sua organização Saiba os impactos potenciais da inscrição um dispositivo em MDM para Office 365. Dependendo de como configurar as políticas, os dispositivos que não estão em conformidade com eles (dispositivos incompatíveis) poderiam ser bloqueados acessem o Office 365. Não compatível com dispositivos também podem ter os aplicativos instalados, fotos e outras informações pessoais, que, em um dispositivo registrado, poderiam ser excluídas se o dispositivo é apagado. Mais informações: [Apagar um dispositivo móvel no Office 365](wipe-a-mobile-device.md). 
  
## <a name="make-sure-users-enroll-their-devices"></a>Certifique-se de usuários inscrever seus dispositivos

Depois que você criou e implantou uma política de gerenciamento de dispositivo móvel, cada usuário licenciado do Office 365 em sua organização que se aplica a política de dispositivo, a receberá uma mensagem de inscrição na próxima vez que entrarem no Office 365 usando seu dispositivo móvel. Eles devem concluir as etapas de inscrição e ativação para poder acessar o email do Office 365 e documentos. Consulte [registrar seu dispositivo móvel para trabalho ou escola](enroll-your-mobile-device.md).
  
> [!IMPORTANT]
> Se o idioma de preferência do usuário não é suportado pelo processo de inscrição, os usuários podem receber notificação de inscrição e as etapas em seus dispositivos móveis em outro idioma. Nem todos os idiomas com suporte no Office 365 são suportados atualmente para o processo de inscrição em dispositivos móveis. 
  
Usuários com dispositivos Android ou iOS são necessárias para instalar o aplicativo de Portal da empresa como parte do processo de inscrição.
  
## <a name="related-topics"></a>Tópicos relacionados

[Recursos de gerenciamento de dispositivos móveis](capabilities-of-mobile-device-management.md)
  
[Criar e implantar políticas de segurança de dispositivo](create-device-security-policies.md)
  


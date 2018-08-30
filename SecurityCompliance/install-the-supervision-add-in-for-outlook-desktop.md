---
title: Instalar o suplemento de supervisão da área de trabalho do Outlook
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: 6/19/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
- ZOL160
ms.assetid: 6c5620e6-aba3-4910-8f3a-b55451656ff7
description: Instalar o suplemento do Office 365 supervisão para a versão da área de trabalho do Outlook
ms.openlocfilehash: 0bddf305087bf0d9552c7671da5306db8352143f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523567"
---
# <a name="install-the-supervision-add-in-for-outlook-desktop"></a>Instalar o suplemento de supervisão da área de trabalho do Outlook

Para revisar identificadas por uma política de supervisão de comunicações, o uso de revisores o suplemento de supervisão para o Outlook e Outlook web app. O suplemento é instalado automaticamente no Outlook web app para todos os revisores que você especificou na política. No entanto, os revisores devem executar algumas etapas para instalá-lo na versão para desktop do Outlook.
  
> [!NOTE]
> Usando diretivas de supervisão requer uma assinatura do Office 365 E5 para sua organização. Se você não tiver que plano e quiser tentar supervisão, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
## <a name="step-1-copy-the-address-for-the-supervision-mailbox"></a>Etapa 1: Copie o endereço da caixa de correio de supervisão

Para instalar o suplemento para desktop do Outlook, você precisará o endereço para a caixa de correio de supervisão que foi criada como parte da configuração da diretiva de supervisão. 
  
> [!NOTE]
> Se alguém criou a política, você precisará obter esse endereço a partir deles para instalar o suplemento. 
  
 **Para localizar o endereço da caixa de correio de supervisão**
  
1. Entrar no [segurança &amp; Centro de conformidade](https://protection.office.com) usando credenciais de uma conta de administrador em sua organização do Office 365. 
    
2. Vá até a **governança de dados** \> **supervisão**.
    
3. Clique na política de supervisão que está juntando as comunicações que você deseja analisar.
    
4. Na política detalha submenu, em * * caixa de correio de supervisão * *, copie o endereço. 
    
    ![A seção de 'Caixa de correio de supervisão' do submenu de detalhes de uma diretiva de supervisão mostrando o endereço da caixa de correio de supervisão realçado](media/71779d0e-4f01-4dd3-8234-5f9c30eeb067.jpg)
  
## <a name="step-2-configure-the-supervision-mailbox-for-outlook-desktop-access"></a>Etapa 2: Configurar a caixa de correio de supervisão para acesso de área de trabalho do Outlook

Em seguida, os revisores precisará executar alguns comandos do PowerShell do Exchange Online para que eles possam se conectar à caixa de correio de supervisão.
  
1. Conecte-se para o Exchange Online PowerShell. [Como fazer isso?](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)
    
2. Execute os seguintes comandos.
    
  ```
  Add-MailboxPermission "SupervisoryReview{GUID}@domain.onmicrosoft.com" -User <alias or email address of the account that has reviewer permissions to the supervision mailbox> -AccessRights FullAccessSet-Mailbox "<SupervisoryReview{GUID}@domain.onmicrosoft.com>" -HiddenFromAddressListsEnabled: $false
  ```

    Onde *SupervisoryReview{GUID}@domain.onmicrosoft.com* é o endereço que você copiou na etapa 1 acima, e o *usuário* é o nome do revisor que se conectarão à caixa de correio de supervisão na próxima etapa. 
    
3. Aguarde pelo menos uma hora antes de prosseguir para a etapa 3 abaixo.
    
## <a name="step-3-create-an-outlook-profile-to-connect-to-the-supervision-mailbox"></a>Etapa 3: Criar um perfil do Outlook para se conectar à caixa de correio de supervisão

Para a etapa final, serão necessário criar um perfil do Outlook para se conectar à caixa de correio de supervisão revisores. 
  
> [!NOTE]
> Para criar um novo perfil do Outlook, você usará as configurações de email no painel de controle do Windows. O caminho que você tomar para chegar a essas configurações pode dependem de qual sistema operacional do Windows (Windows 7, Windows 8 ou Windows 10) que você está usando e qual versão do Outlook está instalada. 
  
1. Abra o painel de controle e, na caixa **Pesquisar** na parte superior da janela, digite o **email**. 
    
    > [!NOTE]
    > Não tem certeza como chegar ao painel de controle? Consulte [onde está o painel de controle?](https://support.microsoft.com/help/13764/windows-where-is-control-panel)
  
2. Abra o aplicativo de **email** . 
    
3. Em **Configurar email - Outlook**, clique em **Mostrar perfis**.
    
    !['Configurar email - Outlook' caixa de diálogo com o botão Mostrar perfis realçado](media/28b5dae9-d10c-4f2b-926a-294c857d555c.jpg)
  
4. No **email**, clique em **Adicionar**. Em seguida, em **Novo perfil**, digite um nome para a caixa de correio de supervisão (por exemplo, **supervisão**).
    
    ![A caixa de diálogo 'Novo perfil' Mostrar o nome 'Supervisão' na caixa Nome do perfil](media/d02ae181-b541-4ec6-8f51-698f30033204.jpg)
  
5. No **Outlook se conectar ao Office 365**, clique em **Conectar para uma conta diferente**.
    
    ![A mensagem 'Conectar o Outlook para o Office 365' com o link 'Conectar-se para uma conta diferente' realçado](media/fac49ff8-a7f0-4e82-a271-9ec045a95de1.jpg)
  
6. Na **Configuração automática de conta**, escolha a **instalação Manual ou tipos de servidor adicionais**e, em seguida, clique em **Avançar**.
    
7. Em **Escolha seu tipo de conta**, escolha o **Office 365**. Em seguida, na caixa **Endereço de Email** , digite o endereço da caixa de correio de supervisão que você copiou anteriormente. 
    
    ![A página 'Escolher o tipo de conta' da caixa de diálogo Adicionar conta no Outlook, mostrando a caixa de 'endereço de Email ' realçada.](media/4f601236-9f69-4cf6-a58c-0b91204aa8cb.jpg)
  
8. Quando solicitado, insira suas credenciais do Office 365.
    
9. Se tiver êxito, você verá o **supervisão - \<nome da política\> ** pasta listada no modo de exibição lista de pastas no Outlook. 
    


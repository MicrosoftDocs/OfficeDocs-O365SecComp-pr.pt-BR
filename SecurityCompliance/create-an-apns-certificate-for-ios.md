---
title: Crie um certificado APNs para dispositivos iOS
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: 8/5/2016
ms.audience: Admin
ms.topic: get-started-article
f1_keywords:
- O365M_APNCertMDM
- O365E_APNCertMDM
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 522b43f4-a2ff-46f6-962a-dd4f47e546a7
description: Para gerenciar dispositivos iOS como iPad e iPhones no gerenciamento de dispositivos móveis para o Office 365, siga estas etapas para criar primeiro um certificado APNs.
ms.openlocfilehash: 28e8888d7dd57c3052cdcb5994725f11a5f0445f
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272046"
---
# <a name="create-an-apns-certificate-for-ios-devices"></a>Crie um certificado APNs para dispositivos iOS

 Para gerenciar dispositivos iOS como iPad e iPhones no gerenciamento de dispositivos móveis para o Office 365, você deve criar um certificado APNs. 
  
Para fazer isso, siga as etapas no link **Configurar** na página do portal. (Vá para **segurança &amp; Centro de conformidade** \> **diretivas de segurança** \> **Device management** \> **Gerenciar definições**.)
  
![Configurar o gerenciamento de dispositivo móvel etapas obrigatórias e recomendadas](media/d71e3c76-b6b9-4549-ade6-cbfab846d908.png)
  
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
    
Volte para **segurança &amp; Centro de conformidade** \> **diretivas de segurança** \> **Device management** \> **Gerenciar configurações** para concluir a instalação. 
  


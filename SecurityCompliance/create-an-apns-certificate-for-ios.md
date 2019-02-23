---
title: Criar um certificado APNs para dispositivos iOS
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: 8/5/2016
ms.audience: Admin
ms.topic: article
f1_keywords:
- O365M_APNCertMDM
- O365E_APNCertMDM
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 522b43f4-a2ff-46f6-962a-dd4f47e546a7
description: Para gerenciar dispositivos iOS como iPad e iPhones no gerenciamento de dispositivos móveis para o Office 365, siga estas etapas para criar primeiro um certificado APNs.
ms.openlocfilehash: 5f82690f0add5f1aae95a089d9cdfc0b320ae596
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220451"
---
# <a name="create-an-apns-certificate-for-ios-devices"></a>Criar um certificado APNs para dispositivos iOS

 Para gerenciar dispositivos iOS como iPad e iPhones no gerenciamento de dispositivos móveis para o Office 365, você deve criar um certificado APNs. 
  
Para fazer isso, siga as etapas do link **Configurar** na página do Portal. ( \> Acesse gerenciamento de **dispositivos** de **políticas** \> de segurança do \> **centro de conformidade de &amp; segurança** **gerenciar configurações**.)
  
![Configurar o gerenciamento de dispositivo móvel necessário e as etapas recomendadas](media/d71e3c76-b6b9-4549-ade6-cbfab846d908.png)
  
1. Ao lado de **configurar um certificado APNs para dispositivos IOS**, selecione **Configurar**.
    
2. Selecione **baixar seu arquivo CSR** e salvar a solicitação de assinatura de certificado em algum lugar no seu computador que você se lembrará. 
    
    ![Caixa de diálogo Instalar certificado APN](media/03aa8a24-e95c-4077-9b6b-ef76a86bafd7.png)
  
3. Selecione **Avançar**.
    
4. Criar um certificado APN.
    
  - Selecione **portal Apple APNS** para abrir o portal Apple Push Certificates. 
    
    ![Instalar a caixa de diálogo de certificado de notificação APN com o portal Apple APNS selecionado](media/ce19f53c-f44a-470b-baf3-9278dfda2ba5.png)
  
  - Entre com uma ID da Apple.
    
    > [!IMPORTANT]
    > Use uma ID da Apple associada a uma conta de email que permanecerá com sua organização, mesmo que o usuário que gerencia a conta saia. Salve esta ID porque você precisará usar a mesma ID quando for hora de renovar o certificado. 
  
  - Selecione **criar um certificado** e aceitar os **termos de uso**.
    
  - **Navegue** até a solicitação de assinatura de certificado que você baixou para seu computador no Office 365 e selecione **carregar**.
    
  - **Baixe** o certificado APN criado pelo portal de certificado por push da Apple no seu computador. 
    
    > [!TIP]
    > Se você estiver tendo problemas para baixar o certificado, atualize seu navegador. 
  
5. Volte para o Office 365 e selecione **Avançar** para acessar a página **carregar certificado APNS** . 
    
6. Navegue até o certificado APN que você baixou do portal de certificados por push da Apple.
    
    ![Clique no botão procurar para selecionar o certificado APNS baixado da Apple](media/afe2849d-af23-4c55-9009-d8f25edaf6c0.png)
  
7. Selecione **concluir**.
    
Voltar ao \> centro de **conformidade de segurança &amp; ** **as políticas** \> de segurança **Gerenciamento** \> de dispositivos **gerenciar configurações** para concluir a instalação. 
  


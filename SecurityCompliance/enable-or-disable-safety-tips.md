---
title: Habilitar ou desabilitar dicas de segurança no Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/6/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f09668bd-fe1a-4c01-89e3-e88c370e66c7
description: Informa os administradores do Office 365 e o EOP como habilitar e desabilitar dicas de segurança em mensagens de email.
ms.openlocfilehash: 3a8257f9d34ec5def54e2b9c9e919172366d023f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524157"
---
# <a name="enable-or-disable-safety-tips-in-office-365"></a>Habilitar ou desabilitar dicas de segurança no Office 365

Exchange Online Protection (EOP) adiciona ou carimbos, um safety dica para mensagens de email que ele oferece. Destinatários com uma maneira rápida e visual para determinar se uma mensagem é de um seguro, de fornecer essas dicas de segurança verificadas remetente, se a mensagem foi marcada como spam pelo Office 365, se a mensagem contiver algo suspeito, como um esquema de phishing, ou se tiverem imagens externas foi bloqueado. Office 365 e o EOP autônomo admins pode editar uma configuração de política de spam para ativar ou desativar dicas de segurança seja exibido em um email no Outlook e outros clientes de email da área de trabalho. 
  
O Office 365 habilita dicas de segurança por padrão para a sua organização e é recomendável que você deixe-los ativado para ajudar a combater ataques de spam e phishing. Você não pode desativar dicas de segurança para Outlook na web.
  
Para ver exemplos e para saber mais sobre as informações exibidas em dicas de segurança, consulte [Safety dicas em mensagens de email no Office 365.](safety-tips-in-office-365.md)
  
Neste tópico:
  
- [Para ativar ou desativar dicas de segurança usando a segurança do Office 365 &amp; Centro de conformidade](enable-or-disable-safety-tips.md#SandCCsafetytip)
    
- [Para ativar ou desativar dicas de segurança usando o PowerShell](enable-or-disable-safety-tips.md#pshellsafetytip)
    
## <a name="to-enable-or-disable-safety-tips-by-using-the-office-365-security-amp-compliance-center"></a>Para ativar ou desativar dicas de segurança usando a segurança do Office 365 &amp; Centro de conformidade
<a name="SandCCsafetytip"> </a>

1. Vá para [https://protection.office.com](https://protection.office.com).
    
2. Entre no Office 365 com sua conta corporativa ou de estudante.
    
3. Escolha **gerenciamento de ameaça** \> **política**. 
    
4. Na página **política** , escolha **Anti-Spam**.
    
    ![Esta captura de tela mostra como obter para a página de configurações antispam na segurança &amp; Centro de conformidade.](media/b8eb2ee3-2eb1-4ea2-b138-f6d7fb2e23de.png)
  
5. Na página **configurações antispam** escolha a guia **personalizada** . 
    
    ![Esta captura de tela mostra a localização da guia personalizada na página Configurações antispam na segurança &amp; Centro de conformidade.](media/1d688d23-e6f3-4de5-84a7-e8ce31786193.png)
  
6. Se necessário, escolha a opção **configurações personalizadas** para ativar configurações personalizadas. Se a opção configurações personalizadas é definida como **desativado**, você não conseguirá modificar políticas de filtro de spam.
    
    ![Esta captura de tela mostra personalizada de filtro antispam configurações de política desativadas.](media/94f900ad-b556-4a31-a3ac-acfcd72e71b8.png)
  
7. Expanda a política de spam que você deseja modificar e, em seguida, escolha **Editar política**. Por exemplo, escolha a seta para baixo ao lado de **política de filtro de spam de padrão**. Ou, se desejar, você pode criar uma nova política escolhendo **Adicionar uma política**.
    
8. Expanda ações **em massa e Spam** . 
    
9. Para ativar as dicas de segurança, em **Dicas de segurança**, marque a caixa de seleção **em** . Para desativar dicas de segurança, desmarque a caixa de seleção **no** . 
    
10. Escolha **Salvar**.
    
## <a name="to-enable-or-disable-safety-tips-by-using-powershell"></a>Para ativar ou desativar dicas de segurança usando o PowerShell
<a name="pshellsafetytip"> </a>

Os administradores podem usar o PowerShell do Exchange Online para habilitar ou desabilitar sugestões de segurança. Use o cmdlet Set-HostedContentFilterPolicy para ativar ou desativar dicas de segurança em uma política de filtro de spam.
  
1. Conecte-se para o Exchange Online PowerShell. Para obter informações, consulte [Connect to Exchange Online PowerShell](http://go.microsoft.com/fwlink/p/?LinkId=396554).
    
2. Execute o cmdlet Set-HostedContentFilterPolicy para ativar ou desativar dicas de segurança:
    
  ```
  Set-HostedContentFilterPolicy -Identity "policy name " -InlineSafetyTipsEnabled <$true|$false>
  ```

    Onde:
    
  -  *nome da política* é o nome da política que deseja modificar, por exemplo **padrão**.
    
  -  `$true`Habilita as dicas de segurança para a política de filtro de spam. 
    
  -  `$false`Desabilita as dicas de segurança para a política de filtro de spam. 
    
    Por exemplo, para desabilitar dicas de segurança para a política de filtro de spam padrão, execute o seguinte comando:
    
  ```
  PS C:\> Set-HostedContentFilterPolicy -Identity "default" -InlineSafetyTipsEnabled $false
  ```

    Para obter mais informações sobre esse cmdlet, consulte [Set-HostedContentFilterPolicy](https://technet.microsoft.com/library/jj200781.aspx).
    
## <a name="still-need-help"></a>Precisa de mais ajuda?
<a name="pshellsafetytip"> </a>

Se desabilitada dicas de segurança, mas são ainda vê-las em suas mensagens de email, verifique esses aspectos:
  
- Você não pode desativar dicas de segurança para Outlook na web. Tente exibindo o mesmo email em outro cliente, como o Outlook.
    
- Dicas de segurança estão ativas, por padrão para cada um que usa o EOP, isso inclui todas as pessoas que possui o Office 365. Para desabilitar dicas de segurança seja exibido no email, você deve desabilitá-los usando uma política de filtro de spam, conforme descrito neste tópico. Depois que você tiver configurado a política, certifique-se de que ele está habilitado. Para obter informações sobre como habilitar as políticas de filtro de spam, consulte [configurar suas políticas de filtro de spam](https://technet.microsoft.com/library/jj200684.aspx).
    
Para obter mais formas combater spam e phishing, consulte [Proteção de Anti-Spam de Email do Office 365](anti-spam-protection.md).
  


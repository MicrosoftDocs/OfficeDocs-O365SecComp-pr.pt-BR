---
title: Gerenciar usuários de email no EOP
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 4bfaf2ab-e633-4227-8bde-effefb41a3db
description: A definição de usuários de email é uma parte importante do gerenciamento do serviço Exchange Online Protection (EOP).
ms.openlocfilehash: 9ab4420dd9fcf6c056bc661b5f3646672a89a683
ms.sourcegitcommit: b688d67935edb036658bb5aa1671328498d5ddd3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/19/2019
ms.locfileid: "30670636"
---
# <a name="manage-mail-users-in-eop"></a>Gerenciar usuários de email no EOP

A definição de usuários de email é uma parte importante do gerenciamento do serviço Exchange Online Protection (EOP). Existem várias maneiras possíveis de gerenciar usuários no EOP:
  
- Utilizar a sincronização de diretórios para gerenciar usuários de email: se sua empresa possui contas de usuário existentes em um ambiente do Active Directory local, é possível sincronizar essas contas com o Azure Active Directory (AD), onde uma cópia dessas contas fica armazenada na nuvem. Ao sincronizar suas contas de usuário existentes com o Azure Active Directory, será possível exibir esses usuários no painel **Destinatários** do Centro de administração do Exchange (EAC). Recomendamos usar a sincronização de diretório. 
    
- Usar o EAC para gerenciar usuários de email: adicione e gerencie usuários de email diretamente no EAC. Esse é o modo mais fácil de adicionar usuários de email e é útil para adicionar um usuário por vez.
    
- Usar o Windows PowerShell remoto para gerenciar usuários de email: adicione e gerencie usuários de email executando o Windows PowerShell remoto. Este método é útil para adicionar vários registros e criar scripts.
    
> [!NOTE]
> Você pode adicionar usuários no centro de administração do Microsoft 365, no entanto, esses usuários não podem ser usados como destinatários de email. 
  
## <a name="before-you-begin"></a>Antes de você começar

- Os procedimentos neste tópico exigem permissões específicas. Consulte cada procedimento para ver informações sobre permissões.
    
- Para informações sobre atalhos de teclado que possam se aplicar aos procedimentos neste tópico, consulte **Atalhos de teclado no Centro de administração do Exchange**.
    
> [!TIP]
> Está enfrentando problemas? Peça ajuda nos fóruns do Exchange. Visite os fóruns em: [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), ou [Proteção do Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=285351). 
  
## <a name="use-directory-synchronization-to-manage-mail-users"></a>Utilizar a sincronização de diretórios para gerenciar usuários de email

Esta seção oferece informações sobre o gerenciamento de usuários de email usando a sincronização de diretório.
  
> [!IMPORTANT]
> Se você usar a sincronização de diretório para gerenciar seus destinatários, ainda poderá adicionar e gerenciar usuários no centro de administração do Microsoft 365, mas eles não serão sincronizados com o Active Directory local. Isso porque a sincronização de diretórios sincroniza apenas destinatários de seu Active Directory local com a nuvem. 
  
> [!TIP]
>  A sincronização de diretório é recomendada para uso com os seguintes recursos: > **Listas de remetentes confiáveis e bloqueados do Outlook**: quando sincronizadas com o serviço, essas listas terão precedência sobre a filtragem de spam. Isso permite que os usuários gerenciem suas próprias listas de remetentes confiáveis e bloqueados por usuário ou por domínio. > **Bloqueio de Borda Baseado em Diretório (DBEB)**: para obter mais informações sobre DBEB, consulte [Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx). > **Quarentena de spam de usuário final**: para acessar a quarentena de spam de usuário final, os usuários finais devem ter uma ID de usuário e senha válidas no Office 365. Os clientes do EOP que estão protegendo caixas de correio locais devem ser usuários de email válidos. > **Regras de fluxo** de emails-quando você usa a sincronização de diretório, os usuários e grupos existentes do Active Directory são carregados automaticamente para a nuvem e você pode criar regras de fluxo de emails (também conhecidas como regras de transporte) que direcionam usuários específicos e/ou grupos sem precisar adicioná-los manualmente por meio do PowerShell de proteção do Exchange Online ou do Eat. Observe que os [grupos dinâmicos de distribuição](https://go.microsoft.com/fwlink/?LinkId=507569) não podem ser sincronizados através da sincronização de diretório. 
  
 **Antes de você começar**
  
Obtenha as permissões necessárias e prepare-se para a sincronização de diretórios, como descrito em [Preparar a sincronização de diretórios](https://go.microsoft.com/fwlink/p/?LinkId=308908).
  
### <a name="to-synchronize-user-directories"></a>Sincronizar diretórios de usuário

1. Ative a sincronização de diretórios, como descrito em [Ativar a sincronização de diretórios](https://go.microsoft.com/fwlink/p/?LinkId=308909).
    
2. Configure seu computador de sincronização de diretórios, como descrito em [Configurar o computador de sincronização de diretórios](http://go.microsoft.com/fwlink/p/?LinkId=308911).
    
3. Sincronize seus diretórios como descrito em [Usar o Assistente de Configuração para sincronizar diretórios](http://go.microsoft.com/fwlink/?LinkId=308912).
    
    > [!IMPORTANT]
    > Após a conclusão do Assistente de Configuração da Ferramenta de Sincronização do Microsoft Azure Active Directory, a conta **MSOL_AD_SYNC** será criada em sua floresta do Active Directory. Esta conta é usada para ler e sincronizar suas informações do Active Directory local. Para que a sincronização de diretórios funcione corretamente, verifique se a porta TCP 443 em seu servidor de sincronização de diretórios local está aberta. 
  
4. Ative usuários sincronizados, como descrito em [Ative os usuários sincronizados](http://go.microsoft.com/fwlink/p/?LinkId=308913).
    
5. Gerencie a sincronização de diretórios, como descrito em [Gerenciar a sincronização de diretórios](http://go.microsoft.com/fwlink/p/?LinkId=308915).
    
6. Verifique se o EOP está sincronizando corretamente. No EAC, vá para **Destinatários** \> **Contatos** e veja se a lista de usuários foi corretamente sincronizada com seu ambiente local. 
    
## <a name="use-the-eac-to-manage-mail-users"></a>Usar o EAC para gerenciar usuários de email

Esta seção oferece informações sobre a adição e o gerenciamento de usuários de email diretamente no EAC.
  
 **Antes de iniciar**
  
Para executar este procedimento ou estes procedimentos, você precisa receber permissões. Para ver de que permissões você precisa, consulte o Entrada "Usuários, contatos e grupos de funções" no tópico [Permissões de recurso no EOP](feature-permissions-in-eop.md).
  
### <a name="to-add-a-mail-user-in-the-eac"></a>Adicionar um usuário de email ao EAC

1. Crie um usuário de email em **Destinatários** \> **Contatos** no EAC e clique em **Novo +**.
    
2. Na página **Novo usuário de email**, insira as informações do usuário, incluindo o seguinte: 
    
   ****

|**Propriedade do usuário de email**|**Descrição**|
|:-----|:-----|
|**Nome**, **Iniciais** e **Sobrenome** <br/> |Digite o nome completo do usuário nas caixas apropriadas.  <br/> |
|**Nome para exibição** <br/> |Digite um nome, usando até 64 caracteres. Por padrão, essa caixa mostra os nomes nas caixas **Nome**, **Iniciais** e **Sobrenome**, se houver. É necessário fornecer o nome para exibição.  <br/> |
|**Alias** <br/> |Digite um alias exclusivo, usando até 64 caracteres para o usuário. O alias é obrigatório.  <br/> |
|**Endereço de email externo** <br/> |Digite o endereço de email externo do usuário.  <br/> |
|**ID de usuário** <br/> |Digite o nome que o usuário de email usará para entrar no serviço. O nome de entrada do usuário consiste em um nome de usuário à esquerda do símbolo (@) e um sufixo à direita. Geralmente, o sufixo é o nome de domínio no qual a conta de usuário reside.  <br/> |
|**Nova senha** <br/> |Digite a senha que o usuário de email usará para entrar no serviço. Verifique se a senha fornecida é compatível com os requisitos de comprimento, complexidade e histórico do domínio no qual você está criando a conta do usuário.  <br/> |
|**Confirmação da senha** <br/> |Digite novamente a senha para confirmá-la.  <br/> |
   
3. Clique em **Salvar** para criar o novo usuário de email. O novo usuário deve aparecer na lista de usuários. 
    
### <a name="to-edit-or-remove-a-mail-user-in-the-eac"></a>Adicionar ou remover um usuário de email no EAC

- No EAC, acesse **Destinatários** \> **Contatos**. Na lista de usuários, clique no usuário que você deseja exibir ou alterar e selecione **Editar** ![ícone](../media/ITPro-EAC-EditIcon.gif) de edição para atualizar as configurações do usuário, conforme necessário. Você pode alterar o nome, o alias ou as informações de contato do usuário, e pode registrar informações detalhadas sobre a função do usuário na organização. Você também pode selecionar um usuário e escolher **Remover**![ícone Remover](../media/ITPro-EAC-RemoveIcon.gif) para excluí-lo. 
    
## <a name="use-remote-windows-powershell-to-manage-mail-users"></a>Usar o Windows PowerShell remoto para gerenciar usuários de email

Esta seção fornece informações sobre como adicionar e gerenciar usuários de email usando o Windows PowerShell remoto.
  
 **Antes de iniciar**
  
- Para executar este procedimento ou estes procedimentos, você precisa receber permissões. Para ver de que permissões você precisa, consulte o Entrada "Usuários, contatos e grupos de funções" no tópico [Permissões de recurso no EOP](feature-permissions-in-eop.md).
    
- Lembre-se de que quando estiver criando usuários de email usando cmdlets do PowerShell remoto, você pode encontrar limitações.
    
- Esse cmdlet usa um método de processamento em lotes que resulta em um atraso na propagação de alguns minutos até que os resultados do cmdlet estejam visíveis.
    
- Para saber como usar o Windows PowerShell para se conectar ao Exchange Online Protection, consulte [Conectar-se ao Exchange Online Protection usando o PowerShell Remoto](http://technet.microsoft.com/library/054e0fd7-d465-4572-93f8-a00a9136e4d1.aspx).
    
 **Para adicionar um usuário de email usando o PowerShell remoto**
  
O exemplo usa o cmdlet [New-EOPMailUser](http://technet.microsoft.com/library/0520cf33-4ad0-44e4-99a3-1b485739fc05.aspx) para criar uma conta de usuário habilitado para email em nome de Diogo Martins com os seguintes detalhes: 
  
- O primeiro nome é Diogo e o sobrenome é Martins.
    
- O nome é Diogo e o nome de exibição é Diogo Martins.
    
- O alias é diogom.
    
- O endereço de email externo é diogom@tailspintoys.com.
    
- O nome de usuário do Office 365 é diogom@contoso.onmicrosoft.com.
    
- A senha é Pa$$word1.
    
```Powershell
New-EOPMailUser -LastName Zeng -FirstName Jeffrey -DisplayName "Jeffrey Zeng" -Name Jeffrey -Alias jeffreyz -MicrosoftOnlineServicesID jeffreyz@contoso.onmicrosoft.com -ExternalEmailAddress jeffreyz@tailspintoys.com -Password (ConvertTo-SecureString -String 'Pa$$word1' -AsPlainText -Force)
```

 **Para verificar se funcionou**
  
Execute o cmdlet [Get-User](http://technet.microsoft.com/library/2a33c9e6-33da-438c-912d-28ce3f4c9afb.aspx) conforme as etapas a seguir para mostrar as informações sobre o novo usuário de email Diogo Martins: 
  
```Powershell
Get-User "Jeffrey Zeng"

```

 **Para editar as propriedades de um usuário de email usando o PowerShell remoto**
  
Use os cmdlets [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) e [Set-EOPMailUser](http://technet.microsoft.com/library/834c3de6-1485-4d50-bb96-262a2c0c8619.aspx) para visualizar ou alterar propriedades para usuários de email. 
  
Este exemplo define o endereço de email externo de Brenda Fernandes.
  
```Powershell
Set-EOPMailUser -Identity "Pilar Pinilla" -EmailAddresses pilarp@tailspintoys.com
```

Este exemplo define a propriedade Company de todos os usuários de email como Contoso.
  
```Powershell
$Recip = Get-Recipient -ResultSize unlimited -Filter {(RecipientTypeDetails -eq 'mailuser')}
$Recip | foreach {Set-EOPUser -Identity $_.Alias -Company Contoso}

```

 **Para verificar se funcionou**
  
No exemplo anterior, alteramos as propriedades do usuário de email Brenda Fernandes, use o cmdlet [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) para verificar as alterações. (Observe que você pode visualizar várias propriedades para vários contatos de email.) 
  
```Powershell
Get-Recipient -Identity "Pilar Pinilla" | Format-List 

```

No exemplo anterior em que a propriedade Company foi definida como Contoso para todos os usuários de email, execute o comando a seguir para verificar as alterações:
  
```Powershell
Get-Recipient -ResultSize unlimited -Filter {(RecipientTypeDetails -eq 'mailuser')} | Format-List Name,Company
```

> [!IMPORTANT]
> Esse cmdlet usa um método de processamento em lotes que resulta em um atraso na propagação de alguns minutos até que os resultados do cmdlet estejam visíveis. 
  
 **Para remover um usuário de email usando o PowerShell remoto**
  
Este exemplo usa o cmdlet [Remove-EOPMailUser](http://technet.microsoft.com/library/cb91dc26-ed22-4d3c-9f64-df9df1754edb.aspx) para excluir o usuário Diogo Martins: 
  
```Powershell
Remove-EOPMailUser -Identity Jeffrey
```

 **Para verificar se funcionou**
  
Execute o cmdlet [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) da seguinte maneira. Uma mensagem de erro deve ser exibida já que o usuário não existe mais. 
  
```Powershell
Get-Recipient Jeffrey | fl
```



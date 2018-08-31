---
title: Impedir que o email que está sendo marcada como spam no Office 365 e o Exchange Online Protection
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 74aaade0-efc0-46ac-b949-f2d1d59256fa
description: Dicas para administradores do Office 365 impedir que o e-mail bom marcada como spam sejam enviadas para quarentena como um falso positivo. Personalize uma lista segura e outras opções para impedir que o bom email marcada como spam.
ms.openlocfilehash: 42b27d237592e95e6d175ab335959bc82269c0f7
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523541"
---
# <a name="prevent-email-from-being-marked-as-spam-in-office-365-and-exchange-online-protection"></a>Impedir que o email que está sendo marcada como spam no Office 365 e o Exchange Online Protection

Os administradores do Exchange Online ou Exchange Online Protection (EOP) com as credenciais de acesso apropriado podem usar estas etapas para ajudar a garantir que uma mensagem de email em viagem através do serviço não está marcada como spam.
  
Pode ser frustrante ter email legítimo, boa em quarentena ou bloqueada como spam e inicial em uma pasta de quarentena. Você pode usar uma lista de remetentes confiáveis ou uma regra de fluxo de email a fim de ignorar a filtragem de spam e impedir que mensagens de email boa obtendo marcadas como lixo eletrônico. Quando uma mensagem é marcada incorretamente como spam pelo filtro de spam, ele se chama um falso positivo. O filtro de spam do Office 365 também fornece algumas opções que os usuários finais podem personalizar a fim de ajudar a evitar falsos positivos.
  
Se você está procurando ajuda com mensagens de falsa negativa, ou seja, uma mensagem de spam que obterá quando ele não deve, confira as dicas em [email de bloqueio de spam com o filtro de spam do Office 365 para evitar problemas de negativos falsos](block-email-spam-to-prevent-false-negatives.md).
  
## <a name="eop-only-customers-use-directory-synchronization"></a>Os clientes somente EOP: usar sincronização de diretórios

EOP é um serviço que ajuda a proteger sua organização contra spam e malware de filtragem de email baseada em nuvem. Se você tiver caixas de correio no Office 365, eles são protegidos automaticamente pelo EOP pois ele é parte do serviço. 
  
Se você é um cliente somente EOP, ou seja, você assina o serviço EOP para uso com o seu servidor do Exchange local, você deve sincronizar com o serviço de configurações do usuário usando a sincronização de diretório. Isso garante que seus remetentes listas são respeitadas pelo EOP. Para obter mais informações, consulte "Usar a sincronização de diretórios para gerenciar usuários de email" no [Manage Mail Users in EOP](https://go.microsoft.com/fwlink/?LinkId=534098).
  
## <a name="prevent-false-positive-email-by-using-the-connection-filters-ip-allow-list"></a>Impedir que o email positivo falso usando a conexão lista de permissões de IP do filtro

Se você achar que o email de um remetente sempre é movido para as pastas lixo em sua organização, você pode adicionar o endereço IP do remetente do email como IP do seu filtro de conexão lista de permissões. Normalmente, isso impede que false respostas positivas deste remetente para todos os destinatários dentro da sua organização. A exceção ocorre quando um usuário habilita a opção "seguros lista apenas: somente os emails de pessoas ou domínios na sua lista de remetentes confiáveis ou lista de destinatários confiáveis serão entregues na caixa de entrada" no Outlook e não adicionar remetente à lista de remetentes confiáveis. Para obter informações sobre como substituir essa opção, consulte [solução de problemas: uma mensagem termina na pasta Lixo eletrônico, embora EOP tiver marcado a mensagem como não spam](prevent-email-from-being-marked-as-spam-0.md#TroubleshootingJunkEOPNonSpam).
  
 **Para adicionar um endereço IP à sua conexão lista de permissões de IP do filtro**
  
1. Obter o cabeçalho da mensagem enviada pelo remetente que você deseja permitir. Você pode fazer isso do seu cliente de email, como o Outlook ou o Outlook na Web, conforme descrito no [Analisador de cabeçalho de mensagem](https://go.microsoft.com/fwlink/p/?LinkId=306583).
    
2. Procure manualmente o endereço IP após a marca CIP no cabeçalho X-Forefront-Antispam-Report ou usando a guia do **Analisador de mensagem** do [Remote Connectivity Analyzer](https://testconnectivity.microsoft.com/?tabid=mha).
    
3. Adicione o IP endereço como o IP lista de permissões, seguindo as etapas descritas em "Usar o EAC para editar a política de filtro de conexão padrão" em [Configure a política de filtro de conexão](https://go.microsoft.com/fwlink/?LinkId=534132).
    
## <a name="prevent-false-positive-email-by-configuring-spam-filter-policies"></a>Impedir que o email positivo falso, definindo políticas de filtro de spam

Você pode adicionar domínios ou endereços de email individuais a uma lista Permitir seguindo as etapas em [configurar suas políticas de filtro de spam](https://go.microsoft.com/fwlink/?LinkID=534136).
  
## <a name="review-your-advanced-spam-filter-policies"></a>Revise suas políticas de filtro de spam avançadas

Se você tiver restrição especial configurada em uma política de filtro de spam, por exemplo, se tiver bloqueado todo um domínio, você deve examiná-los para verificar se pode estar causando falsos positivos. Consulte [configurar suas políticas de filtro de spam](https://go.microsoft.com/fwlink/?LinkId=534136)e desativar adicional [Opções de filtragem de spam avançada](https://go.microsoft.com/fwlink/?LinkId=534137) que podem causar mensagens sejam marcadas como spam. 
  
## <a name="help-your-end-users-create-a-safe-sender-list-to-prevent-good-email-from-being-marked-as-spam"></a>Ajudar seus usuários finais a criar uma lista de remetentes seguros para impedir que o e-mail bom sendo marcada como spam
<a name="BKMK_email-user-help-safelist"> </a>

Avise os usuários para adicionar os endereços dos remetentes que eles confiam à sua lista de remetentes confiáveis do [Outlook](https://go.microsoft.com/fwlink/p/?LinkId=270065) ou do [Outlook na Web](https://go.microsoft.com/fwlink/p/?LinkId=294862). Para começar a no Outlook na Web, escolha **configurações**![ConfigureAPowerBIAnalysisServicesConnector_settingsIcon](media/24bd5467-c8d2-4936-9c37-a179bd0e21ec.png) \> **Opções** \> **Bloquear ou permitir**. O diagrama a seguir mostra um exemplo de adicionar algo a uma lista de remetentes seguros.
  
![Adicionando um remetente seguro no Outlook Web App](media/8de6b24e-429e-4e8f-8ce8-53ba659cbfcb.png)
  
Aceita a EOP remetentes confiáveis dos usuários e destinatários, mas não os domínios confiáveis. Isso ocorre mesmo se o domínio é adicionado por meio do Outlook na Web ou adicionado no Outlook e sincronizados usando a sincronização de diretório.
  
## <a name="troubleshooting-a-message-ends-up-in-the-junk-folder-even-though-eop-marked-the-message-as-non-spam"></a>Solução de problemas: Uma mensagem acaba na pasta Lixo eletrônico, embora EOP tiver marcado a mensagem como não spam
<a name="TroubleshootingJunkEOPNonSpam"> </a>

Se seus usuários terão a opção no Outlook habilitado para "Safe lista apenas: somente emails de pessoas ou domínios na sua lista de remetentes confiáveis ou lista de destinatários confiáveis serão entregues na caixa de entrada", e em seguida, todos os emails irão para a pasta Lixo eletrônico para que um remetente, a menos que o remetente está no reci lista de remetentes confiáveis do pient. Isso acontecerá independentemente de se EOP marca uma mensagem como não spam ou se você tiver configurado a uma regra no EOP para marcar uma mensagem como não spam.
  
Você pode desabilitar a opção apenas listas de confiança para os usuários do Outlook seguindo as instruções em [Outlook: configuração de diretiva para desabilitar a interface do usuário do lixo eletrônico e o mecanismo de filtragem](https://support.microsoft.com/en-us/kb/2180568).
  
Se você visualizar a mensagem no Outlook na Web, haverá uma dica safety amarelo que indica que a mensagem está na pasta Lixo eletrônico, porque o remetente não estiver na lista de remetentes confiáveis do destinatário.
  
Se você observar o cabeçalho de uma mensagem, ela pode incluir o carimbo sfv: skn (permissões de IP ou permitir ETR) ou SFV:NSPM (não-spam), mas a mensagem ainda for colocada na pasta de lixo eletrônico do usuário. Não há nada no cabeçalho da mensagem que indica que o usuário tem "Apenas listas de confiança" habilitado. Isso acontece porque a opção "Apenas listas de confiança" definida pelos usuários no Outlook substitui a configuração do EOP. 
  
 **Para verificar por que uma mensagem de um remetente seguro será marcada como não spam no cabeçalho da mensagem, mas ainda extremidades na pasta de lixo eletrônico do usuário**
  
1. Para saber como se conectar ao Exchange Online PowerShell, consulte [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554). 
    
2. Execute o seguinte comando para exibir as definições de configuração de lixo eletrônico do usuário:
    
  ```
  Get-MailboxJunkEmailConfiguration example@contoso.com | fl TrustedListsOnly,ContactsTrusted,TrustedSendersAndDomains
  ```

    Se TrustedListsOnly for definido como True, isso significa que essa configuração estiver habilitada. Se ContactsTrusted for definido como True, significa que o usuário confia contatos e remetentes confiáveis. O TrustedSendersAndDomains lista o conteúdo da lista de remetentes confiáveis do usuário.
    
## <a name="still-need-help"></a>Precisa de mais ajuda?
<a name="TroubleshootingJunkEOPNonSpam"> </a>

[![Obtenha ajuda nos fóruns da comunidade do Office 365](media/12a746cc-184b-4288-908c-f718ce9c4ba5.png)](https://go.microsoft.com/fwlink/p/?LinkId=518605)
  
[![Administradores: Entre e crie uma solicitação de serviço](media/10862798-181d-47a5-ae4f-3f8d5a2874d4.png)]( https://go.microsoft.com/fwlink/p/?LinkId=519124)
  
[![Administradores: Chame o suporte técnico](media/9f262e67-e8c9-4fc0-85c2-b3f4cfbc064e.png)](https://go.microsoft.com/fwlink/p/?LinkID=518322)
  
## <a name="see-also"></a>Confira também
<a name="TroubleshootingJunkEOPNonSpam"> </a>

[Visão geral do filtro de lixo eletrônico](https://support.office.com/article/5AE3EA8E-CF41-4FA0-B02A-3B96E21DE089)
  
[Bloquear ou permitir (configurações de lixo eletrônico)](https://support.office.com/article/48c9f6f7-2309-4f95-9a4d-de987e880e46)
  
[Bloquear spam de email com o filtro de spam do Office 365 para evitar problemas de falsos negativos](block-email-spam-to-prevent-false-negatives.md)


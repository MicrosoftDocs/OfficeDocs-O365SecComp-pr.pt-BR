---
title: Definir regras de fluxo de email para criptografar mensagens de email no Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 9b7daf19-d5f2-415b-bc43-a0f5f4a585e8
description: Como administrador global do Office 365, você pode criar email regras do fluxo para habilitar o Office 365 Message Encryption (OME). Você pode criptografar qualquer mensagens de email de saída e remover a criptografia de mensagens internas ou de respostas a mensagens criptografadas enviadas de sua organização.
ms.openlocfilehash: 0ed112e216060cdd56afa2dfd08cdebd5740621d
ms.sourcegitcommit: d7e87ce4b1579ac47af2e853ef59ef058c40191f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/16/2018
ms.locfileid: "26547263"
---
# <a name="define-mail-flow-rules-to-encrypt-email-messages-in-office-365"></a>Definir regras de fluxo de email para criptografar mensagens de email no Office 365

Como administrador global do Office 365, você pode criar regras de fluxo de email, também conhecidas como regras de transporte, para ajudar a proteger mensagens de email enviadas e recebidas. Você pode configurar regras para criptografar qualquer mensagens de email de saída e remover a criptografia de mensagens criptografadas provenientes de dentro da organização ou de respostas a mensagens criptografadas enviadas de sua organização. Você pode usar o Centro de administração do Exchange (EAC) ou os cmdlets do Windows PowerShell para Exchange Online para criar estas regras.  Além das regras de criptografia geral, você também pode optar por habilitar ou desabilitar as opções de criptografia de mensagem individual para usuários finais.
  
Se você recentemente migrado do AD RMS à proteção de informações do Windows Azure, você precisará reveja suas regras de fluxo de email existentes para garantir que eles continuam a trabalhar no novo ambiente. Além disso, se você quiser tirar vantagem dos novos recursos do Office 365 Message Encryption (OME) disponíveis para você, por meio de proteção de informações do Windows Azure, você precisará atualizar suas regras de fluxo de email existente. Caso contrário, os usuários continuarão receber emails criptografados que usa o formato de anexo HTML anterior, em vez da experiência OME nova e sem interrupções. Se você ainda não tiver configurado a OME ainda, consulte [configurar novos recursos do Office 365 Message Encryption construídos sobre a proteção de informações do Windows Azure](set-up-new-message-encryption-capabilities.md) para obter informações. 
  
Para obter informações sobre os componentes que compõem a regras de fluxo de correio e como as regras de fluxo de email comercial, consulte [(regras de transporte) de regras de fluxo de email no Exchange Online](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/mail-flow-rules). Para obter informações adicionais sobre como as regras de fluxo de correio funcionam com proteção de informações do Windows Azure, consulte [Configurando o Exchange Online regras de fluxo de email para os rótulos de proteção de informações do Windows Azure](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-exo-rules).
  
> [!IMPORTANT]
> Para ambientes híbridos do Exchange, os usuários no local podem enviar emails criptografados usando OME somente se o email é roteado através do Exchange Online. Para configurar o OME em um ambiente híbrido do Exchange, você precisará primeiro [Configurar híbrida usando o Assistente de configuração híbrida](https://docs.microsoft.com/Exchange/exchange-hybrid) e [Configurar o email para o fluxo do seu servidor de email para o Office 365](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/set-up-connectors-to-route-mail#part-2-configure-mail-to-flow-from-your-email-server-to-office-365). Uma vez, você configurou email a fluir através do Office 365, e em seguida, você pode definir regras de fluxo de correio para o OME usando esta orientação.

## <a name="create-a-mail-flow-rule-to-encrypt-email-messages-with-the-new-ome-capabilities"></a>Criar uma regra de fluxo de email para criptografar mensagens de email com os novos recursos OME

Você pode definir as regras de fluxo de correio para ativar a criptografia de mensagem com os novos recursos OME usando o EAC.
  
### <a name="to-create-a-rule-for-encrypting-email-messages-with-the-new-ome-capabilities-by-using-the-eac"></a>Para criar uma regra para criptografar mensagens de email com os novos recursos OME usando o EAC

1. Em um navegador da web, usando uma conta de trabalho ou da escola que recebeu permissões de administrador global, [entrar no Office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser).
    
2. Escolha os blocos de **Admin** . 
    
3. No Centro de administração do Office 365, escolha **Centros de Administração** \> **Exchange**.
    
4. No EAC, vá para **fluxo de email** \> **regras** \> ![novo ícone](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) ( **novo**) \> **criar uma nova regra**. Para obter mais informações sobre como usar o EAC, consulte o [Centro de administração do Exchange no Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center).
    
5. Em **nome**, digite um nome para a regra, como Encrypt mail for DrToniRamos@hotmail.com.
    
6. Em **Aplicar esta regra se**, selecione uma condição e digite um valor, se necessário. Por exemplo, para criptografar mensagens enviadas a DrToniRamos@hotmail.com:

  1. Em **Aplicar esta regra se**, selecione **o destinatário é**.

  2. Escolha um nome existente na lista de contatos ou digite um novo endereço de email na caixa **verificar nomes**. 
    
    Para selecionar um nome existente, escolha-o na lista e clique em **OK**.
    
    Insira um novo nome, digite um endereço de email na caixa **Verificar nomes** e selecione **Verificar nomes** \> **Okey**.
    
7. Para adicionar mais condições, escolha **mais opções** e, em seguida, escolha **Adicionar condição** e selecione na lista. 
    
  Por exemplo, para aplicar a regra apenas se o destinatário está fora da sua organização, selecione **Adicionar condição** e selecione **o destinatário é interno/externo** \> **fora da organização** \> **Okey**.
    
8. Para ativar a criptografia usando os novos recursos OME de **fazer o seguinte**, selecione **modificar a segurança da mensagem** e escolha **aplicar criptografia de mensagem do Office 365 e proteção de direitos**. Selecione um modelo do RMS na lista, escolha **Salvar**e escolha **Okey**.
    
  A lista de modelos inclui todos os modelos padrão e opções, assim como quaisquer modelos personalizados que você criou para usam pelo Office 365. Se a lista estiver vazia, certifique-se de que você configurou o Office 365 Message Encryption com os novos recursos conforme descrito em [configurar novos recursos do Office 365 Message Encryption baseados na parte superior da proteção de informações do Windows Azure](set-up-new-message-encryption-capabilities.md). Para obter informações sobre os modelos padrão, consulte [Configurando e gerenciando modelos de proteção de informações do Windows Azure](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates). Para obter informações sobre a opção **Não encaminhar** , consulte [não encaminhar uma opção para emails](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails). Para obter informações sobre a opção **criptografar apenas** , consulte [criptografar apenas a opção para emails](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails).
    
    Você pode escolher **Adicionar ação** se desejar especificar outra ação. 
    
### <a name="to-update-an-existing-mail-flow-rule-to-use-the-new-ome-capabilities-by-using-the-eac"></a>Para atualizar uma regra de fluxo de email existente para usar os novos recursos OME usando o EAC

1. Em um navegador da web, usando uma conta de trabalho ou da escola que recebeu permissões de administrador global, [entrar no Office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser).
    
2. Escolha os blocos de **Admin** . 
    
3. No Centro de administração do Office 365, escolha **Centros de Administração** \> **Exchange**.
    
4. No EAC, vá para **fluxo de email** \> **regras**.
    
5. Na lista de regras de fluxo de correio, selecione a regra que você deseja modificar para usar os novos recursos OME e escolha ![ícone Editar](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) ( **Editar**).
    
6. Para ativar a criptografia usando os novos recursos OME de **fazer o seguinte**, escolha **modificar a segurança da mensagem** e escolha **aplicar criptografia de mensagem do Office 365 e proteção de direitos**. Selecione um modelo do RMS na lista, escolha **Salvar** e escolha **Okey**.
    
    A lista de modelos inclui todos os modelos padrão e opções, assim como quaisquer modelos personalizados que você criou para usam pelo Office 365. Se a lista estiver vazia, certifique-se de que você configurou o Office 365 Message Encryption com os novos recursos conforme descrito em [configurar novos recursos do Office 365 Message Encryption baseados na parte superior da proteção de informações do Windows Azure](set-up-new-message-encryption-capabilities.md). Para obter informações sobre os modelos padrão, consulte [Configurando e gerenciando modelos de proteção de informações do Windows Azure](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates). Para obter informações sobre a opção **Não encaminhar** , consulte [não encaminhar uma opção para emails](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails). Para obter informações sobre a opção **criptografar apenas** , consulte [criptografar apenas a opção para emails](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails).
    
    Você pode escolher **Adicionar ação** se desejar especificar outra ação. 
    
7. **Faça o seguinte** na lista de, remover quaisquer ações que estão atribuídas ao **modificar a segurança da mensagem** \> **Aplicar a versão anterior do OME**.
    
8. Escolha **Salvar**.
    
## <a name="creating-rules-for-office-365-message-encryption-without-the-new-capabilities"></a>Criando regras de criptografia de mensagem do Office 365 sem os novos recursos

Se você ainda não tiver movido sua organização do Office 365 para os novos recursos OME, use essas tarefas para definir regras de fluxo de email para criptografar mensagens para sua organização. A Microsoft recomenda que você faça um plano para mover-se para as novas capacidades OME tão logo razoáveis para sua organização. Para obter instruções, consulte [configurar novos recursos do Office 365 Message Encryption construídos sobre a proteção de informações do Windows Azure](set-up-new-message-encryption-capabilities.md).
  
### <a name="to-create-a-rule-for-encrypting-email-messages-without-the-new-ome-capabilities-by-using-the-eac"></a>Para criar uma regra para criptografar mensagens de email sem os novos recursos OME usando o EAC

1. Em um navegador da web, usando uma conta de trabalho ou da escola que recebeu permissões de administrador global, [entrar no Office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser).
    
2. Escolha os blocos de **Admin** . 
    
3. No Centro de administração do Office 365, escolha **Centros de Administração** \> **Exchange**.
    
4. No EAC, vá para **fluxo de email** \> **regras** \> **+** ( **novo**) \> **criar uma nova regra**. Para obter mais informações sobre como usar o EAC, consulte [Exchange admin center no Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center).
    
5. Em **nome**, digite um nome para a regra, como Encrypt mail for DrToniRamos@hotmail.com.
    
6. Em **Aplicar esta regra se**, selecione uma condição e digite um valor, se necessário. Por exemplo, para criptografar mensagens enviadas a DrToniRamos@hotmail.com: 
    
  1. Em **Aplicar esta regra se**, selecione **o destinatário é**.
    
  2. Escolha um nome existente na lista de contatos ou digite um novo endereço de email na caixa **verificar nomes**. 
    
    - Para selecionar um nome existente, escolha-o na lista e clique em **OK**.
    
    - Insira um novo nome, digite um endereço de email na caixa **Verificar nomes** e selecione **Verificar nomes** \> **Okey**.
    
  7. Para adicionar mais condições, escolha **mais opções** e selecione **Adicionar condição** e selecione na lista. 
    
    Por exemplo, para aplicar a regra apenas se o destinatário está fora da sua organização, selecione **Adicionar condição** e selecione **o destinatário é interno/externo** \> **fora da organização** \> **Okey**.
    
  8. Para ativar a criptografia sem usar os novos recursos OME, em **faça o seguinte**, selecione **modificar a segurança da mensagem** \> **Aplicar a versão anterior do OME**e escolha **Salvar**.
    
    Se você receber um erro se o licenciamento de IRM não estiver habilitado, então você não configurou o OME para sua organização ainda. Se você quiser configurar OME agora, você deve montá-lo para usar os novos recursos OME. Para obter informações, consulte [configurar novos recursos do Office 365 Message Encryption construídos sobre a proteção de informações do Windows Azure](set-up-new-message-encryption-capabilities.md). Microsoft não oferece suporte para configuração das novas implantações do OME sem os novos recursos.
    
    Você pode escolher **Adicionar ação** se desejar especificar outra ação. 
    
### <a name="to-create-a-rule-for-encrypting-email-messages-without-the-new-ome-capabilities-by-using-windows-powershell-for-exchange-online"></a>Para criar uma regra para criptografar mensagens de email sem os novos recursos OME usando o Windows PowerShell para Exchange Online

1. Conecte-se para o Exchange Online PowerShell. Para obter mais informações, consulte [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).
    
2. Criar uma regra usando o cmdlet **New-TransportRule** e defina o parâmetro _ApplyOME_ para `$true`.
    
Por exemplo, para exigir que todas as mensagens de email que são endereçadas a DrToniRamos@hotmail.com deverão ser criptografadas, digite:
    
```
New-TransportRule -Name "Encrypt rule for Dr Toni Ramos" -SentTo "DrToniRamos@hotmail.com" -SentToScope "NotinOrganization" -ApplyOME $true
```

Neste exemplo:
    
- O nome da nova regra é "Criptografar a regra para recuperação de desastres Toni Ramos".
    
- O parâmetro _SentTo_ , especifica uma condição que procura por destinatários em mensagens de email. Você pode usar qualquer valor que identifica exclusivamente o destinatário, como um endereço de email, nome, o nome diferenciado (DN) etc. Neste exemplo, o destinatário é identificado pelo endereço de email "DrToniRamos@hotmail.com". 
    
- O parâmetro _SentToScope_ Especifica uma condição que procura o local de destinatários. Neste exemplo, a caixa de correio do destinatário é do hotmail e não é parte da organização do Office 365, portanto, o valor "NotInOrganization" é usado. 
    
Para obter mais informações sobre as condições que você pode definir nas regras de fluxo de email usando este cmdlet, consulte [New-TransportRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/New-TransportRule).
    
### <a name="remove-encryption-from-email-replies-encrypted-without-the-new-ome-capabilities"></a>Remover a criptografia de respostas de email criptografadas sem os novos recursos OME

Quando os usuários de email enviam mensagens criptografadas, os destinatários dessas mensagens podem responder com respostas criptografadas. Você pode criar regras de fluxo para remover automaticamente a criptografia de respostas para que usuários de email em sua organização não seja necessário que entrar no portal de criptografia para exibi-los para email. Você pode usar os cmdlets EAC ou o Windows PowerShell para definir essas regras. Se você ainda não estiver usando os novos recursos OME, você pode apenas descriptografar mensagens que são enviadas por qualquer um de dentro de sua organização ou as mensagens que são as respostas às mensagens enviadas de dentro da sua organização. Você não pode descriptografar mensagens criptografadas provenientes de fora da sua organização.
  
#### <a name="create-a-rule-for-removing-encryption-from-email-replies-encrypted-without-the-new-ome-capabilities-by-using-the-eac"></a>Criar uma regra para remover a criptografia das respostas de email criptografadas sem os novos recursos OME usando o EAC
<a name="DecryptruleEACNoNewOME"> </a>

1. Em um navegador da web, usando uma conta de trabalho ou da escola que recebeu permissões de administrador, [entrar no Office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser).
    
2. Escolha os blocos de **Admin** . 
    
3. No Centro de administração do Office 365, escolha **Centros de Administração** \> **Exchange**.
    
4. No EAC, vá para **fluxo de email** \> **regras** \> **+** ( **novo**) \> **criar uma nova regra**. Para obter mais informações sobre como usar o EAC, consulte [Exchange admin center no Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center).
    
5. Em **nome**, digite um nome para a regra, como Remove encryption from emails de entrada.
    
6. Em **Aplicar esta regra se** , selecione as condições em que a criptografia deve ser removida das mensagens, como **o destinatário está localizado** \> **dentro da organização**.
    
7. Em **faça o seguinte**, selecione **modificar a segurança da mensagem** \> **Remover a versão anterior do OME**.
    
8. Selecione **Salvar**.
    
#### <a name="create-a-rule-to-remove-encryption-from-email-replies-encrypted-without-the-new-ome-capabilities-by-using-exchange-online-powershell"></a>Criar uma regra para remover a criptografia de respostas de email criptografadas sem os novos recursos OME usando o PowerShell do Exchange Online
<a name="DecryptrulePShellNoNewOME"> </a>

1. Conecte-se para o Exchange Online PowerShell. Para obter mais informações, consulte [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).
    
2. Criar uma regra usando o cmdlet **New-TransportRule** e defina o parâmetro _RemoveOME_ para `$true`.
    
Por exemplo, para remover a criptografia de todos os emails enviados para destinatários na sua organização do Office 365, digite:
    
```
New-TransportRule -Name "Remove encryption from incoming mail" -SentToScope "InOrganization" -RemoveOME $true
```

Neste exemplo:

- O nome da nova regra é "Remove encryption from incoming mail".

- O parâmetro _SentToScope_ Especifica uma condição que procura o local de destinatários. Neste exemplo, o valor "InOrganization" é usado que indica que: 

  - O destinatário é uma caixa de correio, usuário de email, grupo ou pasta pública habilitada para email na sua organização.

  ou

  - Endereço de email do destinatário está em um domínio aceito que esteja configurado como um domínio autoritativo ou um domínio de retransmissão interna, e a mensagem foi enviada ou recebida por uma conexão autenticada.
    
Para obter mais informações sobre as condições que você pode definir nas regras de fluxo de email usando este cmdlet, consulte [New-TransportRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/New-TransportRule).
    
## <a name="related-topics"></a>Tópicos Relacionados

[Criptografia no Office 365](encryption.md)
  
[Configurar novos recursos do Office 365 Message Encryption construídos sobre a proteção de informações do Windows Azure](set-up-new-message-encryption-capabilities.md)
  
[Adicionar identidade visual a mensagens criptografadas](add-your-organization-brand-to-encrypted-messages.md)
  
[Regras de fluxo de emails (regras de transporte) no Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=506707)
  
[Regras de fluxo de emails (regras de transporte) no Exchange Online Protection](https://go.microsoft.com/fwlink/p/?LinkId=506708)
  


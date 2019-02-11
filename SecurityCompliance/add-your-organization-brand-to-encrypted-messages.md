---
title: Adicionar sua marca de organização a suas mensagens criptografadas
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 7a29260d-2959-42aa-8916-feceff6ee51d
description: Como um administrador do Exchange, você pode aplicar a sua organização identidade visual a mensagens de email criptografadas da sua organização e o conteúdo do portal de criptografia.
ms.openlocfilehash: 4b22b72a8b77c2978a7cf25166978759119c272c
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29696215"
---
# <a name="add-your-organizations-brand-to-your-encrypted-messages"></a>Adicionar a marca da sua organização a suas mensagens criptografadas

Como um administrador do Exchange Online ou Exchange Online Protection, você pode aplicar a sua empresa branding para personalizar a aparência das mensagens de email do Office 365 Message Encryption da sua organização e o conteúdo do portal de criptografia. Usando os cmdlets Get-OMEConfiguration e Set-OMEConfiguration Windows PowerShell, você pode personalizar os seguintes aspectos da experiência de visualização para os destinatários das mensagens de email criptografadas:
  
- Texto introdutório do email que contém a mensagem criptografada
- Texto do aviso de isenção de responsabilidade do email que contém a mensagem criptografada
- Texto que aparece no portal do OME
- Logotipo exibido na mensagem de email e portal OME
- Cor de plano de fundo na mensagem de email e portal OME

Você também pode reverter para a aparência padrão a qualquer momento.

Se você quiser mais controle, você pode criar vários modelos para emails criptografados provenientes de sua organização. Usando esses modelos, que você pode controlar mais do que apenas a aparência das mensagens de email, mas também controlar partes da experiência do usuário final. Por exemplo, você pode especificar se ou não os destinatários de email que tem este modelo foi aplicado e que usam o Google, Yahoo e Accounts do Microsoft podem usar essas contas para entrar no portal do Office 365 Message Encryption. Você pode usar modelos para atender aos vários casos de uso, tais como:

- Modelos para cada departamento, como vendas, finanças etc.
- Modelos de diferentes produtos
- Modelos para diferentes regiões geográficas ou países

Depois que você criou os modelos, você pode aplicá-las a emails criptografados usando regras de fluxo de correio do Exchange. Todos os emails são da marca usando esses modelos podem ser revogados.
  
||
|:-----|
|Este artigo faz parte de uma maior série de artigos sobre o Office 365 Message Encryption. Este artigo destina-se aos administradores e profissionais de TI. Se você apenas estiver procurando informações sobre como enviar ou receber uma mensagem criptografada, consulte a lista de artigos no [Office 365 Message Encryption (OME)](ome.md) e localize o artigo que atenda às suas necessidades. |
||

## <a name="create-branding-templates"></a>Criar modelos de marcas

Você pode criar modelos de marcas para sua organização no Windows PowerShell com o cmdlet New-OMEConfiguration. Depois de criar o modelo, você define as partes do modelo usando o cmdlet Set-OMEConfiguration. Você pode criar vários modelos.

![Partes de e-mail personalizável](media/ome-template-breakout.png)
  
1. Usando uma conta de trabalho ou da escola que tenha permissões de administrador global na sua organização do Office 365, iniciar uma sessão do Windows PowerShell e se conectar ao Exchange Online. Para obter instruções, consulte [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Use o cmdlet New-OMEConfiguration para criar um novo modelo.
     ```powershell
     New-OMEConfiguration -Identity <OMEConfigurationIdParameter>
     ```
     Por exemplo,
     ```powershell
     New-OMEConfiguration -Identity <Branding template 1>
     ```
3. Definir as personalizações para o modelo que você acabou de definir usando o cmdlet Set-OMEConfiguration como descrito em [Set-OMEConfiguration](https://docs.microsoft.com/powershell/module/exchange/encryption-and-certificates/Set-OMEConfiguration) ou use a tabela a seguir para obter orientação.

|**Para personalizar este recurso da experiência com criptografia**|**Utilize estes comandos**|
|:-----|:-----|
|Cor de plano de fundo  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -BackgroundColor "<Hexadecimal color code>"` <br/> **Exemplo:** <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -BackgroundColor "#ffffff"` <br/> |
|Logotipo  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <Byte[]>` <br/> **Exemplo:** <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -Image (Get-Content "C:\Temp\contosologo.png" -Encoding byte)` <br/> Formatos de arquivo com suporte: .png, .jpg, .bmp ou .tiff  <br/> Tamanho ideal do arquivo de logotipo: menos que 40 KB  <br/> Tamanho ideal da imagem de logotipo: 170 pixels x 70 pixels  <br/> |
|Texto ao lado do remetente nome e endereço de email| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -IntroductionText "<String up to 1024 characters>"` <br/> **Exemplo:** <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -IntroductionText "has sent you a secure message."`|
|Texto que aparece no botão "Ler mensagem"| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -ReadButtonText "<String up to 1024 characters>"` <br/> **Exemplo:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -ReadButtonText "Read Secure Message."`|
|Texto que aparece acima abaixo do botão "Ler mensagem"| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<String up to 1024 characters>"` <br/> **Exemplo:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -EmailText "Encrypted message from ContosoPharma secure messaging system."`|
|Declaração de isenção de responsabilidade nos emails que contêm a mensagem criptografada  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -DisclaimerText "<Disclaimer statement. String of up to 1024 characters.>"` <br/> **Exemplo:** <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -DisclaimerText "This message is confidential for the use of the addressee only."`|
|Texto que aparece na parte superior do portal de exibição do email criptografado<br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<Text for your portal. String of up to 128 characters.>"` <br/> **Exemplo:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -PortalText "ContosoPharma secure email portal."` <br/> |
|Para habilitar ou desabilitar a autenticação com uma única senha para esse modelo personalizado| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -OTPEnabled <$true|$false>` <br/> **Exemplos:** <br/>Para habilitar uma única vez códigos de acesso para esse modelo personalizado <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -OTPEnabled $true` <br/> Para desabilitar uma única vez códigos de acesso para esse modelo personalizado <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -OTPEnabled $false`|
|Para habilitar ou desabilitar a autenticação com identidades da Microsoft, Yahoo ou Google para esse modelo personalizado| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -SocialIdSignIn <$true|$false>` <br/> **Exemplos:** <br/>Para permitir que IDs sociais para esse modelo personalizado <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -SocialIdSignIn $true` <br/> Para desabilitar as IDs sociais para esse modelo personalizado <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -SocialIdSignIn $false`|

## <a name="to-remove-brand-customizations-from-the-ome-portal-and-email-messages-encrypted-by-ome"></a>Para remover as personalizações de marca das mensagens de email e portal OME criptografadas por OME
  
1. [Conectar-se ao Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Use o cmdlet Set-OMEConfiguration como descrito em [Set-OMEConfiguration](https://docs.microsoft.com/powershell/module/exchange/encryption-and-certificates/Set-OMEConfiguration). Para remover sua organização com marca personalizações de DisclaimerText, EmailText, e valores de PortalText, defina o valor como uma sequência vazia, `""`. Para todos os valores, como logotipo, de imagem, defina o valor como `"$null"`.

**Opções de personalização de criptografia**

**Para reverter esse recurso da experiência de criptografia para o texto e a imagem padrões**|**Utilize estes comandos**|
|:-----|:-----|
|Texto padrão que acompanha as mensagens de email criptografadas  <br/> O texto padrão é exibido acima das instruções para a exibição de mensagens criptografadas| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<empty string>"` <br/> **Exemplo:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -EmailText ""`|
|Declaração de isenção de responsabilidade nos emails que contêm a mensagem criptografada| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> DisclaimerText "<empty string>"` <br/> **Exemplo:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -DisclaimerText ""`|
|Texto que aparece na parte superior do portal de exibição do email criptografado| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<empty string>"` <br/> **Voltar revertendo de exemplo para o padrão:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -PortalText ""` <br/> |
|Logotipo| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <"$null">` <br/> **Voltar revertendo de exemplo para o padrão:** <br/>  `Set-OMEConfiguration -Identity "OME configuration" -Image $null`|
|Cor de plano de fundo| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -BackgroundColor <"$null">` <br/> **Voltar revertendo de exemplo para o padrão:** <br/>  `Set-OMEConfiguration -Identity "OME configuration" -BackgroundColor $null`|

## <a name="create-an-exchange-mail-flow-rule-that-applies-custom-branding-to-encrypted-emails"></a>Criar uma regra de fluxo de email do Exchange que se aplica a emails criptografados de marca personalizada

Depois que você criou um modelo de marcação, você pode criar regras de fluxo de email do Exchange para aplicar essa identidade visual personalizada com base em certas condições. Essa regra se aplicará identidade visual personalizada nos seguintes cenários:

- Se o email manualmente foi criptografado pelo usuário final entre os clientes do Outlook ou no OWA
- Se o email automaticamente foi criptografado por uma regra de fluxo de emails do Exchange ou a política de prevenção de perda de dados do Office 365

Para obter informações sobre como criar uma regra de fluxo de email do Exchange que se aplica a criptografia, consulte [definir regras de fluxo de email para criptografar mensagens de email no Office 365](define-mail-flow-rules-to-encrypt-email.md).

1. Em um navegador da web, usando uma conta de trabalho ou da escola que recebeu permissões de administrador global, [entrar no Office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser).

2. Escolha os blocos de **Admin** .

3. No Centro de administração do Office 365, escolha **Centros de Administração** \> **Exchange**.

4. No EAC, vá para **fluxo de email** \> **regras** e selecione **novo** ![novo ícone](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) \> **criar uma nova regra**. Para obter mais informações sobre como usar o EAC, consulte o [Centro de administração do Exchange no Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center).

5. Em **nome**, digite um nome para a regra, como marcas para o departamento de venda.

6. Em **Aplicar esta regra se** selecionar uma condição, selecione a condição que **o remetente está localizado dentro da organização** , bem como outras condições que você deseja na lista de condições disponíveis. Por exemplo, convém aplicar um modelo de marcação específico:

     - Todos criptografados emails enviados dos membros do departamento financeiro
     - Criptografadas emails enviados com uma determinada palavra-chave, como "Externa" ou "Parceiro"
     - Criptografadas emails enviados a um domínio específico

7. De **fazer o seguinte**, selecione **modificar a segurança da mensagem** > **Aplicar às mensagens OME de marca personalizada**. Em seguida, na lista suspensa, selecione um modelo de marcação daquelas que você criou.
8. (Opcional) Se quiser que a regra de fluxo de email também aplicar a criptografia além custom branding de **fazer o seguinte**, selecione **modificar a segurança da mensagem** e escolha **aplicar criptografia de mensagem do Office 365 e proteção de direitos**. Selecione um modelo do RMS na lista, escolha **Salvar**e escolha **Okey**.
  
     A lista de modelos inclui todos os modelos padrão e opções, assim como quaisquer modelos personalizados que você criou para usam pelo Office 365. Se a lista estiver vazia, certifique-se de que você configurou o Office 365 Message Encryption com os novos recursos conforme descrito em [Set up novos recursos do Office 365 Message Encryption](set-up-new-message-encryption-capabilities.md). Para obter informações sobre os modelos padrão, consulte [Configurando e gerenciando modelos de proteção de informações do Windows Azure](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates). Para obter informações sobre a opção **Não encaminhar** , consulte [não encaminhar uma opção para emails](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails). Para obter informações sobre a opção **criptografar apenas** , consulte [criptografar apenas a opção para emails](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails).

     Você pode escolher **Adicionar ação** se desejar especificar outra ação.

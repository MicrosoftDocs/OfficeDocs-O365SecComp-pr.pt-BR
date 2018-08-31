---
title: Adicionar sua marca de organização a suas mensagens criptografadas
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/2/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 7a29260d-2959-42aa-8916-feceff6ee51d
description: 'Como um administrador do Exchange, você pode aplicar a sua organização identidade visual a mensagens de email criptografadas da sua organização e o conteúdo do portal de criptografia. '
ms.openlocfilehash: 2f34b5cea3155f587fd7787f1f69270d1373400b
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524073"
---
# <a name="add-your-organizations-brand-to-your-encrypted-messages"></a>Adicionar a marca da sua organização a suas mensagens criptografadas

Como um administrador do Exchange Online ou Exchange Online Protection, você pode aplicar a sua empresa branding para personalizar a aparência das mensagens de email do Office 365 Message Encryption da sua organização e o conteúdo do portal de criptografia. Usando os cmdlets Get-OMEConfiguration e Set-OMEConfiguration Windows PowerShell, você pode personalizar os seguintes aspectos da experiência de visualização para os destinatários das mensagens de email criptografadas:
  
- Texto introdutório do email que contém a mensagem criptografada
    
- Texto do aviso de isenção de responsabilidade do email que contém a mensagem criptografada
    
- Texto que aparece no portal do OME
    
- Logotipo exibido na mensagem de email e portal OME
    
- Cor de plano de fundo na mensagem de email e portal OME
    
Você também pode reverter para a aparência padrão a qualquer momento.
  
||
|:-----|
|Este artigo faz parte de uma maior série de artigos sobre o Office 365 Message Encryption. Este artigo destina-se aos administradores e profissionais de TI. Se você apenas estiver procurando informações sobre como enviar ou receber uma mensagem criptografada, consulte a lista de artigos no [Office 365 Message Encryption (OME)](ome.md) e localize o artigo que atenda às suas necessidades. |
||
   
**Para personalizar a aparência das OME portal e email mensagens criptografadas por OME com a marca da sua organização**
  
1. Conectar ao Exchange Online usando o PowerShell remoto, conforme descrito em [conectar ao Exchange Online Using Remote PowerShell](http://technet.microsoft.com/en-us/library/jj984289%28v=exchg.150%29.aspx).
    
2. Use o cmdlet Set-OMEConfiguration, conforme descrito em [Set-OMEConfiguration](http://technet.microsoft.com/en-us/3ef0aec0-ce28-411d-abe8-7236f082af1b) ou use a tabela a seguir para obter orientação. 
    
**Opções de personalização de criptografia**

|**Para personalizar este recurso da experiência com criptografia**|**Utilize estes comandos**|
|:-----|:-----|
|Texto padrão que acompanha as mensagens de email criptografadas. O texto padrão exibido acima das instruções para exibição de mensagens criptografadas  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<String up to 1024 characters>"` <br/> **Exemplo:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -EmailText "Encrypted message from ContosoPharma secure messaging system."`|
|Declaração de isenção de responsabilidade nos emails que contêm a mensagem criptografada  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -DisclaimerText "<Disclaimer statement. String of up to 1024 characters.>"` <br/> **Exemplo:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -DisclaimerText "This message is confidential for the use of the addressee only."` <br/> |
|Texto que aparece na parte superior do portal de exibição do email criptografado<br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<Text for your portal. String of up to 128 characters.>"` <br/> **Exemplo:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -PortalText "ContosoPharma secure email portal."` <br/> |
|Logotipo  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <Byte[]>` <br/> **Exemplo:** <br/>  `Set-OMEConfiguration -Identity "OME configuration" -Image (Get-Content "C:\Temp\contosologo.png" -Encoding byte)` <br/> Formatos de arquivo com suporte: .png, .jpg, .bmp ou .tiff  <br/> Tamanho ideal do arquivo de logotipo: menos que 40 KB  <br/> Tamanho ideal da imagem de logotipo: 170 pixels x 70 pixels  <br/> |
|Cor de plano de fundo  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -BackgroundColor "<Hexadecimal color code>"` <br/> **Exemplo:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -BackgroundColor "#ffffff"` <br/> |
   
**Para remover as personalizações de marca das mensagens de email e portal OME criptografadas por OME**
  
1. Conectar ao Exchange Online usando o PowerShell remoto, conforme descrito em [conectar ao Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).
    
2. Use o cmdlet Set-OMEConfiguration como descrito em [Set-OMEConfiguration](http://technet.microsoft.com/3ef0aec0-ce28-411d-abe8-7236f082af1b). Para remover sua organização com marca personalizações de DisclaimerText, EmailText, e valores de PortalText, defina o valor como uma sequência vazia, `""`. Para todos os valores, como logotipo, de imagem, defina o valor como `"$null"`.
    
**Opções de personalização de criptografia**

**Para reverter esse recurso da experiência de criptografia para o texto e a imagem padrões**|**Utilize estes comandos**|
|:-----|:-----|
|Texto padrão que acompanha as mensagens de email criptografadas  <br/> O texto padrão é exibido acima das instruções para a exibição de mensagens criptografadas  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<empty string>"` <br/> **Exemplo:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -EmailText ""` <br/> |
|Declaração de isenção de responsabilidade nos emails que contêm a mensagem criptografada  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> DisclaimerText "<empty string>"` <br/> **Exemplo:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -DisclaimerText ""` <br/> |
|Texto que aparece na parte superior do portal de exibição do email criptografado  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<empty string>"` <br/> **Voltar revertendo de exemplo para o padrão:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -PortalText ""` <br/> |
|Logotipo  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <"$null">` <br/> **Voltar revertendo de exemplo para o padrão:** <br/>  `Set-OMEConfiguration -Identity "OME configuration" -Image $null` <br/> |
|Cor de plano de fundo  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -BackgroundColor <"$null">` <br/> **Voltar revertendo de exemplo para o padrão:** <br/>  `Set-OMEConfiguration -Identity "OME configuration" -BackgroundColor $null` <br/> |
   


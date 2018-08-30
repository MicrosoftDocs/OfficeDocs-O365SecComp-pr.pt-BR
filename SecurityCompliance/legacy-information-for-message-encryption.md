---
title: Informações herdadas de Criptografia de Mensagens do Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/4/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: None
search.appverid:
- MET150
ms.assetid: 5986b9e1-c824-4f8f-9b7d-a2b0ae2a7fe9
description: Se você ainda não migraram sua organização do Office 365 para os novos recursos OME, mas você já implantou OME, as informações neste artigo se aplicam à sua organização. A Microsoft recomenda que você faça um plano para mover-se para as novas capacidades OME tão logo razoáveis para sua organização. Para obter instruções, consulte Set up novos recursos do Office 365 Message Encryption construídos sobre a proteção de informações do Windows Azure. Se você deseja saber mais sobre como as novas capacidades funcionam pela primeira vez, consulte criptografia de mensagem do Office 365. O restante deste artigo refere-se ao comportamento OME antes do lançamento de novos recursos OME.
ms.openlocfilehash: d5b21cbe0004ca7bda38085bd5d8ef5f2a22b04e
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524141"
---
# <a name="legacy-information-for-office-365-message-encryption"></a>Informações herdadas de Criptografia de Mensagens do Office 365

Se você ainda não migraram sua organização do Office 365 para os novos recursos OME, mas você já implantou OME, as informações neste artigo se aplicam à sua organização. A Microsoft recomenda que você faça um plano para mover-se para as novas capacidades OME tão logo razoáveis para sua organização. Para obter instruções, consulte [configurar novos recursos do Office 365 Message Encryption construídos sobre a proteção de informações do Windows Azure](set-up-new-message-encryption-capabilities.md). Se você deseja saber mais sobre como as novas capacidades funcionam pela primeira vez, consulte [Criptografia de mensagem do Office 365](ome.md). O restante deste artigo refere-se ao comportamento OME antes do lançamento de novos recursos OME.
  
Com a criptografia de mensagem do Office 365, sua organização pode enviar e receber mensagens de email criptografadas entre pessoas de dentro e fora da sua organização. O Office 365 Message Encryption funciona com Outlook.com, Yahoo, Gmail e outros serviços de email. Criptografia de mensagem de email ajuda a garantir que destinada apenas os destinatários pode exibir o conteúdo da mensagem.
  
Estes são alguns exemplos:
  
- Um funcionário bank envia extratos de cartão de crédito aos clientes
    
- Um representante da empresa seguros fornece detalhes de diretiva para os clientes
    
- Um corretor de hipoteca solicita informações financeiras de um cliente para um aplicativo de empréstimo
    
- Um médico envia informações de saúde aos pacientes
    
- Um advogado envia informações confidenciais a um cliente ou a outro advogado
    
## <a name="how-office-365-message-encryption-works-without-the-new-capabilities"></a>Como o Office 365 Message Encryption funciona sem os novos recursos

Criptografia de mensagem do Office 365 é um serviço online que é baseado no Microsoft Azure Rights Management (RMS do Windows Azure). Com o Windows Azure RMS, os administradores podem definir regras de fluxo de correio para determinar as condições de criptografia. Por exemplo, uma regra pode exigir a criptografia de todas as mensagens endereçadas para um destinatário específico.
  
Assista a este pequeno vídeo para ver como o Office 365 Message Encryption funciona sem os novos recursos.
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/c55540e7-f7f0-42f5-b254-4b2d2fbb1d63?autoplay=false]
  
Quando alguém envia uma mensagem de email no Exchange Online que corresponde a uma regra de criptografia, a mensagem é enviada com um anexo em HTML. O destinatário abre o anexo HTML e segue as instruções para exibir a mensagem criptografada no portal do Office 365 Message Encryption. O destinatário poderá escolher exibir a mensagem entrando com uma conta da Microsoft ou de um trabalho ou escola associados com o Office 365, ou usando uma senha de uma única vez. As duas opções ajudam a garantir que somente o destinatário pretendido possa exibir a mensagem criptografada. Esse processo é muito diferente para os novos recursos OME.
  
O diagrama a seguir resume a passagem de uma mensagem de email pelo processo de criptografia e de descriptografia.
  
![Diagrama mostrando o caminho de um email criptografado](media/O365-Office365MessageEncryption-Concept.png)
  
Para obter mais informações, consulte [as informações de serviço de legado Office 365 Message Encryption antes do lançamento dos novos recursos OME](legacy-information-for-message-encryption.md#LegacyServiceInfo).
  
## <a name="defining-mail-flow-rules-for-office-365-message-encryption-that-dont-use-the-new-ome-capabilities"></a>Definindo regras de fluxo de email para o Office 365 Message Encryption que não usam os novos recursos OME

Para habilitar a criptografia de mensagem do Office 365 sem os novos recursos, os administradores do Exchange Online e Exchange Online Protection definem regras de fluxo de correio do Exchange. Essas regras determinam em email quais condições a mensagens devem ser criptografadas, bem como condições para remover a criptografia de mensagem. Quando uma ação de criptografia é definida para uma regra, todas as mensagens que correspondam às condições de regra são criptografadas antes que eles enviados.
  
Regras de fluxo de correio são flexíveis, permitindo que você combinar condições para que você pode atender a requisitos de segurança específicos em uma única regra. Por exemplo, você pode criar uma regra para criptografar todas as mensagens que contêm palavras-chave especificadas e são endereçadas a destinatários externos. Criptografia de mensagem do Office 365 também criptografa respostas de destinatários de email criptografada e você pode criar uma regra que descriptografa as respostas a conveniência para seus usuários de email. Dessa forma, os usuários em sua organização não precisará entrar no portal de criptografia para visualizar respostas.
  
Para obter mais informações sobre como criar regras de fluxo de email do Exchange, consulte [Define Rules for Office 365 Message Encryption](define-mail-flow-rules-to-encrypt-email.md).
  
## <a name="sending-viewing-and-replying-to-encrypted-email-messages"></a>Enviar, visualizar e responder mensagens de email criptografadas

Com o Office 365 Message Encryption, mensagens de email são criptografadas automaticamente, com base nas regras definidas pelo administrador. Um email que possui uma mensagem criptografada chega na caixa de entrada do destinatário com um arquivo HTML anexado.
  
Destinatários siga as instruções na mensagem para abrir o anexo e autenticar usando uma conta da Microsoft ou de um trabalho ou escola associados com o Office 365. Se os destinatários não possui qualquer uma das contas, eles estão direcionados para criar uma conta que permita que eles entrar para exibir a mensagem criptografada da Microsoft. Como alternativa, os destinatários podem optar por fazer uma senha de uma única vez para exibir a mensagem. Após entrando ou usando uma senha de uma única vez, os destinatários podem exibir a mensagem descriptografada e enviar uma resposta criptografada.
  
## <a name="customize-encrypted-messages-with-office-365-message-encryption"></a>Personalizar mensagens criptografadas com o Office 365 Message Encryption

Como um administrador do Exchange Online e Exchange Online Protection, você pode personalizar suas mensagens criptografadas. Por exemplo, você pode adicionar a marca da sua empresa e o logotipo, especifique uma introdução e adicione o texto de isenção de responsabilidade nas mensagens criptografadas e no portal do onde destinatários exibir suas mensagens criptografadas. Usando cmdlets do Windows PowerShell, você pode personalizar os seguintes aspectos da experiência de visualização para os destinatários das mensagens de email criptografadas:
  
- Texto introdutório do email que contém a mensagem criptografada
    
- Texto do aviso de isenção de responsabilidade do email que contém a mensagem criptografada
    
- Texto do portal que aparecerá no portal de visualização da mensagem
    
- Logotipo que será exibido na mensagem de email e no portal de visualização
    
Você também pode reverter para a aparência padrão a qualquer momento.
  
O exemplo a seguir mostra um logotipo personalizado para a ContosoPharma no anexo de email:
  
![Exemplo da página de exibição de mensagem criptografada](media/TA-OME-3attachment2.jpg)
  
 **Para personalizar as mensagens de email de criptografia e o portal de criptografia com a marca da sua organização**
  
1. Conectar ao Exchange Online usando o PowerShell remoto, conforme descrito em [conectar ao Exchange Online Using Remote PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-exchange-online-tenants-with-remote-windows-powershell-for-delegated).
    
2. Use o cmdlet Set-OMEConfiguration como descrito aqui: [Set-OMEConfiguration](http://technet.microsoft.com/en-us/3ef0aec0-ce28-411d-abe8-7236f082af1b) ou use a tabela a seguir para obter orientação. 
    
   **Opções de personalização de criptografia**

|**Para personalizar este recurso da experiência com criptografia**|**Utilize estes comandos do Windows PowerShell**|
|:-----|:-----|
|Texto padrão que acompanha as mensagens de email criptografadas  <br/> O texto padrão é exibido acima das instruções para a exibição de mensagens criptografadas  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<string of up to 1024 characters>"` <br/> **Exemplo:**`Set-OMEConfiguration -Identity "OME Configuration" -EmailText "Encrypted message from ContosoPharma secure messaging system"` <br/> |
|Declaração de isenção de responsabilidade nos emails que contêm a mensagem criptografada  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> DisclaimerText "<your disclaimer statement, string of up to 1024 characters>"` <br/> **Exemplo:**`Set-OMEConfiguration -Identity "OME Configuration" -DisclaimerText "This message is confidential for the use of the addressee only"` <br/> |
|Texto que aparece na parte superior do portal de exibição do email criptografado  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<text for your portal, string of up to 128 characters>"` <br/> **Exemplo:**`Set-OMEConfiguration -Identity "OME Configuration" -PortalText "ContosoPharma secure email portal"` <br/> |
|Logotipo  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <Byte[]>` <br/> **Exemplo:**`Set-OMEConfiguration -Identity "OME configuration" -Image (Get-Content "C:\Temp\contosologo.png" -Encoding byte)` <br/> Formatos de arquivo com suporte: .png, .jpg, .bmp ou .tiff  <br/> Tamanho ideal do arquivo de logotipo: menos que 40 KB  <br/> Tamanho ideal da imagem de logotipo: 170 pixels x 70 pixels  <br/> |
   
 **Para remover as personalizações de marca de mensagens de email de criptografia e o portal de criptografia**
  
1. Conectar ao Exchange Online usando o PowerShell remoto, conforme descrito em [conectar ao Exchange Online Using Remote PowerShell](http://technet.microsoft.com/en-us/library/jj984289%28v=exchg.150%29.aspx).
    
2. Use o cmdlet Set-OMEConfiguration como descrito aqui: [Set-OMEConfiguration](http://technet.microsoft.com/3ef0aec0-ce28-411d-abe8-7236f082af1b). Para remover sua organização com marca personalizações de DisclaimerText, EmailText, e valores de PortalText, defina o valor como uma sequência vazia, `""`. Para todos os valores, como logotipo, de imagem, defina o valor como `"$null"`.
    
   **Opções de personalização de criptografia**

|**Para reverter esse recurso da experiência de criptografia para o texto e a imagem padrões**|**Utilize estes comandos do Windows PowerShell**|
|:-----|:-----|
|Texto padrão que acompanha as mensagens de email criptografadas  <br/> O texto padrão é exibido acima das instruções para a exibição de mensagens criptografadas  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<empty string>"` <br/> **Exemplo:**`Set-OMEConfiguration -Identity "OME Configuration" -EmailText ""` <br/> |
|Declaração de isenção de responsabilidade nos emails que contêm a mensagem criptografada  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> DisclaimerText "<empty string>"` <br/> **Exemplo:**`Set-OMEConfiguration -Identity "OME Configuration" -DisclaimerText ""` <br/> |
|Texto que aparece na parte superior do portal de exibição do email criptografado  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<empty string>"` <br/> **Exemplo revertendo para padrão:**`Set-OMEConfiguration -Identity "OME Configuration" -PortalText ""` <br/> |
|Logotipo  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <"$null">` <br/> **Exemplo revertendo para padrão:**`Set-OMEConfiguration -Identity "OME configuration" -Image $null` <br/> |
   
## <a name="service-information-for-legacy-office-365-message-encryption-prior-to-the-release-of-the-new-ome-capabilities"></a>Informações de serviço para criptografia de mensagem herdadas do Office 365 antes do lançamento dos novos recursos OME
<a name="LegacyServiceInfo"> </a>

A tabela a seguir fornece detalhes técnicos para o serviço de criptografia de mensagem do Office 365 antes do lançamento dos novos recursos OME.
  
|**Detalhes do serviço**|**Descrição**|
|:-----|:-----|
|Requisitos do dispositivo cliente  <br/> |As mensagens criptografadas podem ser visualizadas em qualquer dispositivo cliente, desde que o anexo HTML possa ser aberto em um navegador moderno compatível com Postagem de Formulário.  <br/> |
|Conformidade com algoritmos de criptografia e Normas Federais de Processamento de Informações (FIPS)  <br/> |Criptografia de mensagem do Office 365 usa as mesmas chaves de criptografia como o Windows Azure Information Rights Management (IRM) e suporta criptográficas modo 2 (2 mil chave RSA) e chave de 256 bits de sistemas SHA-1. Para obter mais informações sobre os modos de criptográfica subjacentes do IRM, consulte [Modos criptográficos do AD RMS](http://technet.microsoft.com/library/hh867439%28WS.10%29.aspx).<br/> |
|Tipos de mensagem suportados  <br/> |Somente há suporte para a criptografia de mensagem do Office 365 para itens que tenham uma ID de classe de mensagem do **IPM. Observação**. Para obter mais informações, consulte [tipos de Item e classes de mensagens](https://msdn.microsoft.com/library/office/ff861573.aspx).<br/> |
|Limites de tamanhos de mensagens  <br/> |Criptografia de mensagem do Office 365 pode criptografar mensagens de até 25 megabytes. Para obter mais detalhes sobre os limites de tamanho de mensagem, consulte [Limites do Exchange Online](http://technet.microsoft.com/library/exchange-online-limits.aspx).<br/> |
|Políticas de retenção de email Exchange Online  <br/> |O Exchange Online não armazena as mensagens criptografadas.  <br/> |
|Suporte de idioma para a Criptografia de Mensagens do Office 365  <br/> | A Criptografia de Mensagens do Office 365 oferece suporte aos idiomas do Office 365, como a seguir:  <br/>  Mensagens de email de entrada e arquivos HTML anexados são localizados com base nas configurações de idioma do remetente.  <br/>  O portal de visualização está localizado com base nas configurações do navegador do destinatário.  <br/>  O corpo (conteúdo) da mensagem criptografada não está localizado.  <br/> |
|Informações de privacidade para o Portal OME e o aplicativo do Visualizador OME  <br/> |A [Office 365 Messaging Encryption Portal privacy statement](protected-message-viewer-portal-privacy-statement.md) fornece informações detalhadas sobre o que a Microsoft faz e não faz com suas informações particulares.  <br/> |
   
## <a name="frequently-asked-questions-about-legacy-ome"></a>Perguntas frequentes sobre OME herdado
<a name="LegacyServiceInfo"> </a>

Dúvidas sobre a criptografia de mensagem do Office 365? Aqui estão algumas respostas. Se você não puder encontrar o que você precisa, verifique os fóruns de comunidade do Office 365 na [comunidade do Office 365](http://community.office365.com/en-us/forums/default.aspx).
  
 **P. meus usuários enviam mensagens de email criptografadas para destinatários fora da nossa organização. Existe alguma coisa que destinatários externos terá que fazer para ler e responder a mensagens de email criptografadas com a criptografia de mensagem do Office 365?**
  
Destinatários externos à sua organização que recebam mensagens criptografadas do Office 365 podem exibi-las de duas maneiras:
  
- Entrando no serviço com uma conta Microsoft ou uma conta de trabalho ou da escola associada com o Office 365.
    
- Usando uma única senha.
    
 **P. As mensagens criptografadas do Office 365 são armazenadas na nuvem ou em servidores da Microsoft?**
  
Não, as mensagens criptografadas são mantidas no sistema de email do destinatário e quando o destinatário abrir a mensagem, ela é postada temporariamente para exibição nos servidores do Office 365. As mensagens não são armazenadas lá.
  
 **P. Posso personalizar mensagens de email criptografadas com minha marca?**
  
Sim. É possível usar os cmdlets do Windows PowerShell para personalizar o texto padrão exibido na parte superior da mensagem de email criptografada, o texto do aviso de isenção de responsabilidade e o logotipo que você deseja usar nas mensagens de email e no portal de criptografia. Para obter detalhes, consulte [Add branding to encrypted messages](add-your-organization-brand-to-encrypted-messages.md).
  
 **P. O serviço exige uma licença para cada usuário da organização?**
  
A licença é obrigatória para os usuários da organização que enviam emails criptografados.
  
 **P. São exigidas assinaturas para os destinatários externos?**
  
Não, os destinatários externos não necessitam de uma assinatura para ler ou responder mensagens criptografadas. 
  
 **P. como é o Office 365 Message Encryption diferentes de serviços RMS (Rights Management)?**
  
RMS oferece recursos de proteção de direitos de informação para emails internos de uma organização fornecendo modelos internos, tais como: não encaminhar e confidencial da empresa. O Office 365 Message Encryption suporta a criptografia de mensagens para mensagens enviadas a destinatários externos, bem como a destinatários internos.
  
 **P. como é o Office 365 Message Encryption diferente do S/MIME?**
  
Basicamente, o S/MIME é uma tecnologia de criptografia do lado do cliente e exige uma infraestrutura de publicação e de gerenciamento de certificados complicada. A Criptografia de Mensagem do Office 365 usa regras de transporte e não depende da publicação de certificados.
  
 **P. Posso ler as mensagens criptografadas em dispositivos móveis?**
  
Sim, você pode exibir mensagens no Android e iOS baixando os aplicativos do visualizador OME do [Google Play armazenar](http://go.microsoft.com/fwlink/?LinkID=525995&amp;clcid=0x409) e o [repositório de App Apple](http://go.microsoft.com/fwlink/?LinkID=525996&amp;clcid=0x409). Abra o anexo HTML no app visualizador OME e siga as instruções para abrir a sua mensagem criptografada. Para outros dispositivos móveis, você pode abrir o anexo HTML, desde que o cliente de email oferece suporte a postagem de formulário.
  
 **P. As respostas e as mensagens encaminhadas são criptografadas?**
  
Sim. As respostas continuam a ser criptografadas durante todo o decurso do thread.
  
 **P. A Criptografia de Mensagem do Office 365 oferece localização?**
  
O conteúdo HTML e de emails de entrada é localizado com base nas configurações de email do remetente. O portal de exibição é localizado com base nas configurações do navegador do destinatário. No entanto, o próprio corpo (conteúdo) da mensagem criptografada não é localizado.
  
 **P. que método de criptografia é usado para a criptografia de mensagem do Office 365?**
  
Criptografia de mensagem do Office 365 usa Rights Management Services (RMS) como sua infraestrutura de criptografia. O método de criptografia usado depende de onde você obter as chaves RMS usadas para criptografar e descriptografar mensagens.
  
- Se você usar o Microsoft Azure RMS para obter as chaves, modo 2 criptográfico é usado. Criptográficas modo 2 é uma implementação do criptográfica do AD RMS atualizada e aprimorada. Ele oferece suporte a 2048 RSA para assinatura e criptografia e suporta SHA-256 para assinatura.
    
- Se você usar o Active Directory (AD) RMS para obter as chaves, o Modo Criptográfico 1 ou o Modo Criptográfico 2 será utilizado. O método utilizado depende de sua implantação do AD RMS no local. O Modo Criptográfico 1 é a implementação criptográfica original do AD RMS. Ele é compatível com o RSA 1024 para assinatura e criptografia e oferece suporte ao SHA-1 para assinatura. Esse modo continua a receber suporte de todas as versões atuais do RMS.
    
Para obter mais informações, consulte [Modos criptográficos do AD RMS](http://go.microsoft.com/fwlink/p/?LinkId=398616).
  
 **P. Por que algumas mensagens criptografadas vêm de Office365@messaging.microsoft.com?**
  
Quando uma resposta criptografada é enviada do portal de criptografia ou pelo aplicativo Visualizador de OME, o endereço de email de envio é definido como Office365@messaging.microsoft.com, porque a mensagem criptografada é enviada por meio de um ponto de extremidade da Microsoft. Isso ajuda a impedir que mensagens criptografadas sejam marcadas como spam. O nome exibido no email e o endereço do portal de criptografia não são alterados por causa desse rótulo. Além disso, esse rótulo só se aplica às mensagens enviadas pelo portal, não por qualquer outro cliente de email.
  
 **P. estou assinante do Exchange Hosted Encryption (EHE). Onde obter mais informações sobre a atualização para o Office 365 Message Encryption?**
  
Todos os clientes do EHE tiverem sido atualizados para a criptografia de mensagem do Office 365. Para obter mais informações, visite o [Centro de atualização de criptografia do Exchange hospedado](http://go.microsoft.com/fwlink/p/?LinkID=511077).
  
 **P. é necessário para abrir lida com qualquer URLs, IP ou portas no firewall da minha organização para oferecer suporte a criptografia de mensagem do Office 365?**
  
Sim. Você precisa adicionar URLs para o Exchange Online à lista de permissões para a sua organização habilitar a autenticação para mensagens criptografadas pelo Office 365 Message Encryption. Para obter uma lista das URLs do Exchange Online, consulte [URLs do Office 365 e intervalos de endereço IP](https://support.office.com/article/f57e35b7-0a45-42f0-855e-11aa5e7f13fd.aspx).
  
 **P. Para quantos destinatários posso enviar uma mensagem criptografada do Office 365?**
  
O limite de destinatários para uma mensagem criptografada baseia-se no número de caracteres no campo **para** da mensagem. Quando combinado (após a expansão de lista de distribuição), endereços de destinatário no campo **para** não devem exceder 11,980 caracteres. Como endereços de email podem variar em comprimento de caracteres, não há um limite de destinatário padrão para uma única mensagem criptografada. 
  
 **P. É possível revogar uma mensagem enviada para um destinatário específico?**
  
Não. Você não pode revogar uma mensagem para uma pessoa específica após ela é enviada.
  
 **P. Posso exibir um relatório de mensagens criptografadas que foram recebidas e lidas?**
  
Não há um relatório que mostra se uma mensagem criptografada foi exibida, mas há relatórios do Office 365 disponíveis que você pode aproveitar para determinar o número de mensagens que correspondem a uma regra de transporte específica, por exemplo.
  
 **P. O que a Microsoft faz com as informações que forneço por meio do Portal do OME e do aplicativo Visualizador do OME?**
  
A [declaração de privacidade do Portal de criptografia de mensagens do Office 365](protected-message-viewer-portal-privacy-statement.md) fornece informações detalhadas sobre o que a Microsoft faz e não faz com suas informações particulares. 
  


---
title: Informações herdadas de Criptografia de Mensagens do Office 365
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 1/4/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.assetid: 5986b9e1-c824-4f8f-9b7d-a2b0ae2a7fe9
ms.collection:
- M365-security-compliance
description: Se você ainda não tiver movido a sua organização do Office 365 para os novos recursos do OME, mas já tiver implantado o OME, as informações neste artigo se aplicam à sua organização. A Microsoft recomenda que você faça um plano para migrar para os novos recursos do OME assim que for razoável para sua organização. Para obter instruções, consulte Configurar novos recursos de criptografia de mensagem do Office 365 criados com base na proteção de informações do Azure. Se quiser saber mais sobre como os novos recursos funcionam primeiro, confira criptografia de mensagem do Office 365. O restante deste artigo refere-se ao comportamento OME antes do lançamento dos novos recursos do OME.
ms.openlocfilehash: f6e407208735a53b98033e58a6f7b36fe9a37f62
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30276061"
---
# <a name="legacy-information-for-office-365-message-encryption"></a>Informações herdadas de Criptografia de Mensagens do Office 365

Se você ainda não tiver movido a sua organização do Office 365 para os novos recursos do OME, mas já tiver implantado o OME, as informações neste artigo se aplicam à sua organização. A Microsoft recomenda que você faça um plano para migrar para os novos recursos do OME assim que for razoável para sua organização. Para obter instruções, consulte [configurar novos recursos de criptografia de mensagem do Office 365 criados com base na proteção de informações do Azure](set-up-new-message-encryption-capabilities.md). Se quiser saber mais sobre como os novos recursos funcionam primeiro, confira criptografia de [mensagem do Office 365](ome.md). O restante deste artigo refere-se ao comportamento OME antes do lançamento dos novos recursos do OME.
  
Com a criptografia de mensagem do Office 365, sua organização pode enviar e receber mensagens de email criptografadas entre pessoas dentro e fora da sua organização. A criptografia de mensagem do Office 365 funciona com o Outlook.com, Yahoo, Gmail e outros serviços de email. A criptografia de mensagens de email ajuda a garantir que somente os destinatários pretendidos possam exibir o conteúdo da mensagem.
  
Aqui estão alguns exemplos:
  
- Um funcionário do banco envia instruções de cartão de crédito aos clientes
    
- Um representante da companhia de seguros fornece detalhes de política aos clientes
    
- Um corretor de hipoteca solicita informações financeiras de um cliente para um aplicativo de empréstimo
    
- Um provedor de assistência médica envia informações de assistência médica para pacientes
    
- Um advogado envia informações confidenciais para um cliente ou outro advogado
    
## <a name="how-office-365-message-encryption-works-without-the-new-capabilities"></a>Como a criptografia de mensagens do Office 365 funciona sem os novos recursos

A criptografia de mensagem do Office 365 é um serviço online desenvolvido no Microsoft Azure Rights Management (Azure RMS). Com o Azure RMS, os administradores podem definir regras de fluxo de email para determinar as condições de criptografia. Por exemplo, uma regra pode exigir a criptografia de todas as mensagens endereçadas a um destinatário específico.
  
Assista a este breve vídeo para ver como funciona a criptografia de mensagem do Office 365 sem os novos recursos.
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/c55540e7-f7f0-42f5-b254-4b2d2fbb1d63?autoplay=false]
  
Quando alguém envia uma mensagem de email no Exchange Online que corresponde a uma regra de criptografia, a mensagem é enviada com um anexo HTML. O destinatário abre o anexo HTML e segue as instruções para exibir a mensagem criptografada no portal de criptografia de mensagem do Office 365. O destinatário pode optar por exibir a mensagem entrando em uma conta da Microsoft ou em um trabalho ou escola associado ao Office 365 ou usando um código de passagem única. Ambas as opções ajudam a garantir que apenas o destinatário pretendido possa exibir a mensagem criptografada. Esse processo é muito diferente para os novos recursos do OME.
  
O diagrama a seguir resume a passagem de uma mensagem de email pelo processo de criptografia e de descriptografia.
  
![Diagrama mostrando o caminho de um email criptografado](media/O365-Office365MessageEncryption-Concept.png)
  
Para obter mais informações, consulte [Service Information for Legacy Office 365 Message Encryption antes do lançamento dos novos recursos do ome](legacy-information-for-message-encryption.md#LegacyServiceInfo).
  
## <a name="defining-mail-flow-rules-for-office-365-message-encryption-that-dont-use-the-new-ome-capabilities"></a>Definindo regras de fluxo de email para a criptografia de mensagem do Office 365 que não usam os novos recursos do OME

Para habilitar a criptografia de mensagem do Office 365 sem os novos recursos, os administradores do Exchange Online e do Exchange Online Protection definem as regras de fluxo de email do Exchange. Essas regras determinam sob quais condições as mensagens de email devem ser criptografadas, bem como as condições para remover a criptografia de mensagens. Quando uma ação de criptografia é definida para uma regra, quaisquer mensagens que correspondam às condições de regra são criptografadas antes de serem enviadas.
  
As regras de fluxo de emails são flexíveis, permitindo que você combine condições para que possa atender a requisitos específicos de segurança em uma única regra. Por exemplo, você pode criar uma regra para criptografar todas as mensagens que contêm palavras-chave especificadas e são endereçadas a destinatários externos. A criptografia de mensagem do Office 365 também criptografa respostas de destinatários de emails criptografados e você pode criar uma regra que descriptografa essas respostas como uma conveniência para seus usuários de email. Dessa forma, os usuários em sua organização não precisarão entrar no portal de criptografia para exibir respostas.
  
Para obter mais informações sobre como criar regras de fluxo de email do Exchange, consulte [definir regras para a criptografia de mensagem do Office 365](define-mail-flow-rules-to-encrypt-email.md).
  
## <a name="sending-viewing-and-replying-to-encrypted-email-messages"></a>Enviar, visualizar e responder mensagens de email criptografadas

Com a criptografia de mensagem do Office 365, as mensagens de email são criptografadas automaticamente, com base em regras definidas pelo administrador. Um email que possui uma mensagem criptografada chega à caixa de entrada do destinatário com um arquivo HTML anexado.
  
Os destinatários seguem instruções na mensagem para abrir o anexo e autenticar usando uma conta da Microsoft ou um trabalho ou escola associado ao Office 365. Se os destinatários não tiverem uma das contas, eles serão direcionados para criar uma conta da Microsoft que permitirá que eles entrem para exibir a mensagem criptografada. Como alternativa, os destinatários podem optar por obter um código de passagem única para exibir a mensagem. Após entrar ou usar um código de passagem única, os destinatários podem exibir a mensagem descriptografada e enviar uma resposta criptografada.
  
## <a name="customize-encrypted-messages-with-office-365-message-encryption"></a>Personalizar mensagens criptografadas com a criptografia de mensagem do Office 365

Como administrador de proteção do Exchange Online e do Exchange Online, você pode personalizar suas mensagens criptografadas. Por exemplo, você pode adicionar a marca e o logotipo da sua empresa, especificar uma introdução e adicionar texto de aviso de isenção de responsabilidade em mensagens criptografadas e no portal em que os destinatários exibem suas mensagens criptografadas. Usando os cmdlets do Windows PowerShell, você pode personalizar os seguintes aspectos da experiência de visualização para destinatários de mensagens de email criptografadas:
  
- Texto introdutório do email que contém a mensagem criptografada
    
- Texto do aviso de isenção de responsabilidade do email que contém a mensagem criptografada
    
- Texto do portal que aparecerá no portal de visualização da mensagem
    
- Logotipo que será exibido na mensagem de email e no portal de visualização
    
Você também pode reverter para a aparência padrão a qualquer momento.
  
O exemplo a seguir mostra um logotipo personalizado para a ContosoPharma no anexo de email:
  
![Exemplo da página de exibição de mensagem criptografada](media/TA-OME-3attachment2.jpg)
  
 **Para personalizar as mensagens de email de criptografia e o portal de criptografia com a marca da sua organização**
  
1. Conecte-se ao Exchange Online usando o PowerShell remoto, conforme descrito em [Connect to Exchange Online using Remote PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-exchange-online-tenants-with-remote-windows-powershell-for-delegated).
    
2. Use o cmdlet Set-OMEConfiguration conforme descrito aqui: [set-OMEConfiguration](http://technet.microsoft.com/en-us/3ef0aec0-ce28-411d-abe8-7236f082af1b) ou use a tabela a seguir para orientação. 
    
   **Opções de personalização de criptografia**

|**Para personalizar este recurso da experiência com criptografia**|**Utilize estes comandos do Windows PowerShell**|
|:-----|:-----|
|Texto padrão que acompanha as mensagens de email criptografadas  <br/> O texto padrão é exibido acima das instruções para a exibição de mensagens criptografadas  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<string of up to 1024 characters>"` <br/> **Exemplo:** `Set-OMEConfiguration -Identity "OME Configuration" -EmailText "Encrypted message from ContosoPharma secure messaging system"` <br/> |
|Declaração de isenção de responsabilidade nos emails que contêm a mensagem criptografada  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> DisclaimerText "<your disclaimer statement, string of up to 1024 characters>"` <br/> **Exemplo:** `Set-OMEConfiguration -Identity "OME Configuration" -DisclaimerText "This message is confidential for the use of the addressee only"` <br/> |
|Texto que aparece na parte superior do portal de exibição do email criptografado  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<text for your portal, string of up to 128 characters>"` <br/> **Exemplo:** `Set-OMEConfiguration -Identity "OME Configuration" -PortalText "ContosoPharma secure email portal"` <br/> |
|Logotipo  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <Byte[]>` <br/> **Exemplo:** `Set-OMEConfiguration -Identity "OME configuration" -Image (Get-Content "C:\Temp\contosologo.png" -Encoding byte)` <br/> Formatos de arquivo com suporte: .png, .jpg, .bmp ou .tiff  <br/> Tamanho ideal do arquivo de logotipo: menos que 40 KB  <br/> Tamanho ideal da imagem de logotipo: 170 pixels x 70 pixels  <br/> |
   
 **Para remover as personalizações de marca de mensagens de email de criptografia e do portal de criptografia**
  
1. Conecte-se ao Exchange Online usando o PowerShell remoto, conforme descrito em [Connect to Exchange Online using Remote PowerShell](http://technet.microsoft.com/en-us/library/jj984289%28v=exchg.150%29.aspx).
    
2. Use o cmdlet Set-OMEConfiguration conforme descrito aqui: [set-OMEConfiguration](http://technet.microsoft.com/3ef0aec0-ce28-411d-abe8-7236f082af1b). Para remover as personalizações da marca da sua organização dos valores DisclaimerText, EmailText e PortalText, defina o valor como uma cadeia de caracteres vazia `""`,. Para todos os valores de imagem, como logotipo, defina o valor `"$null"`como.
    
   **Opções de personalização de criptografia**

|**Para reverter esse recurso da experiência de criptografia para o texto e a imagem padrões**|**Utilize estes comandos do Windows PowerShell**|
|:-----|:-----|
|Texto padrão que acompanha as mensagens de email criptografadas  <br/> O texto padrão é exibido acima das instruções para a exibição de mensagens criptografadas  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<empty string>"` <br/> **Exemplo:** `Set-OMEConfiguration -Identity "OME Configuration" -EmailText ""` <br/> |
|Declaração de isenção de responsabilidade nos emails que contêm a mensagem criptografada  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> DisclaimerText "<empty string>"` <br/> **Exemplo:** `Set-OMEConfiguration -Identity "OME Configuration" -DisclaimerText ""` <br/> |
|Texto que aparece na parte superior do portal de exibição do email criptografado  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<empty string>"` <br/> **Exemplo reverter para o padrão:**`Set-OMEConfiguration -Identity "OME Configuration" -PortalText ""` <br/> |
|Logotipo  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <"$null">` <br/> **Exemplo reverter para o padrão:**`Set-OMEConfiguration -Identity "OME configuration" -Image $null` <br/> |
   
## <a name="service-information-for-legacy-office-365-message-encryption-prior-to-the-release-of-the-new-ome-capabilities"></a>Informações de serviço para a criptografia de mensagens herdada do Office 365 antes do lançamento dos novos recursos do OME
<a name="LegacyServiceInfo"> </a>

A tabela a seguir fornece detalhes técnicos para o serviço de criptografia de mensagem do Office 365 antes do lançamento dos novos recursos do OME.
  
|**Detalhes do serviço**|**Descrição**|
|:-----|:-----|
|Requisitos do dispositivo cliente  <br/> |As mensagens criptografadas podem ser visualizadas em qualquer dispositivo cliente, desde que o anexo HTML possa ser aberto em um navegador moderno compatível com Postagem de Formulário.  <br/> |
|Conformidade com algoritmos de criptografia e Normas Federais de Processamento de Informações (FIPS)  <br/> |A criptografia de mensagem do Office 365 usa as mesmas chaves de criptografia que o gerenciamento de direitos de informação (IRM) do Windows Azure e suporta o modo criptográfico 2 (chave 2K para a chave de bits RSA e 256 para sistemas SHA-1). Para obter mais informações sobre os modos de criptografia do IRM subjacentes, consulte [modos criptográficos do AD RMS](http://technet.microsoft.com/library/hh867439%28WS.10%29.aspx).<br/> |
|Tipos de mensagem suportados  <br/> |A criptografia de mensagem do Office 365 só é suportada para itens com ID de classe de mensagem **IPM. Nota**. Para obter mais informações, consulte [tipos de item e classes de mensagens](https://msdn.microsoft.com/library/office/ff861573.aspx).<br/> |
|Limites de tamanhos de mensagens  <br/> |A criptografia de mensagem do Office 365 pode criptografar mensagens de até 25 megabytes. Para obter mais detalhes sobre os limites de tamanho de mensagens, consulte [limites do Exchange Online](http://technet.microsoft.com/library/exchange-online-limits.aspx).<br/> |
|Políticas de retenção de email do Exchange Online  <br/> |O Exchange Online não armazena as mensagens criptografadas.  <br/> |
|Suporte de idioma para a Criptografia de Mensagens do Office 365  <br/> | A Criptografia de Mensagens do Office 365 oferece suporte aos idiomas do Office 365, como a seguir:  <br/>  As mensagens de email de entrada e os arquivos HTML anexados são localizados com base nas configurações de idioma do remetente.  <br/>  O portal de visualização está localizado com base nas configurações do navegador do destinatário.  <br/>  O corpo (conteúdo) da mensagem criptografada não está localizado.  <br/> |
|Informações de privacidade para o Portal OME e o aplicativo do Visualizador OME  <br/> |A [Office 365 Messaging Encryption Portal privacy statement](protected-message-viewer-portal-privacy-statement.md) fornece informações detalhadas sobre o que a Microsoft faz e não faz com suas informações particulares.  <br/> |
   
## <a name="frequently-asked-questions-about-legacy-ome"></a>Perguntas frequentes sobre o OME herdado
<a name="LegacyServiceInfo"> </a>

Você tem dúvidas sobre a criptografia de mensagens do Office 365? Veja algumas respostas. Se você não encontrar o que precisa, consulte os fóruns da Comunidade do Office 365 na [comunidade do office 365](http://community.office365.com/en-us/forums/default.aspx).
  
 **P. meus usuários enviam mensagens de email criptografadas para destinatários fora da organização. Há algo que os destinatários externos precisam fazer para ler e responder a mensagens de email criptografadas com a criptografia de mensagem do Office 365?**
  
Destinatários externos à sua organização que recebam mensagens criptografadas do Office 365 podem exibi-las de duas maneiras:
  
- Entrando com uma conta da Microsoft ou uma conta corporativa ou de estudante associada ao Office 365.
    
- Usando um código de passagem única.
    
 **P. As mensagens criptografadas do Office 365 são armazenadas na nuvem ou em servidores da Microsoft?**
  
Não, as mensagens criptografadas são mantidas no sistema de email do destinatário e, quando o destinatário abre a mensagem, ela é temporariamente publicada para exibição nos servidores do Office 365. As mensagens não são armazenadas ali.
  
 **P. Posso personalizar mensagens de email criptografadas com minha marca?**
  
Sim. É possível usar os cmdlets do Windows PowerShell para personalizar o texto padrão exibido na parte superior da mensagem de email criptografada, o texto do aviso de isenção de responsabilidade e o logotipo que você deseja usar nas mensagens de email e no portal de criptografia. Para obter detalhes, consulte [Add branding to encrypted messages](add-your-organization-brand-to-encrypted-messages.md).
  
 **P. O serviço exige uma licença para cada usuário da organização?**
  
A licença é obrigatória para os usuários da organização que enviam emails criptografados.
  
 **P. São exigidas assinaturas para os destinatários externos?**
  
Não, os destinatários externos não necessitam de uma assinatura para ler ou responder mensagens criptografadas. 
  
 **P. como a criptografia de mensagem do Office 365 é diferente dos RMS (Rights Management Services)?**
  
O RMS fornece recursos de proteção de direitos de informação para os emails internos de uma organização fornecendo modelos internos, como: não encaminhar e confidencial da empresa. A criptografia de mensagem do Office 365 suporta a criptografia de mensagem de email para mensagens enviadas para destinatários externos, bem como para destinatários internos.
  
 **P. como é a criptografia de mensagem do Office 365 diferente de S/MIME?**
  
Basicamente, o S/MIME é uma tecnologia de criptografia do lado do cliente e exige uma infraestrutura de publicação e de gerenciamento de certificados complicada. A Criptografia de Mensagem do Office 365 usa regras de transporte e não depende da publicação de certificados.
  
 **P. Posso ler as mensagens criptografadas em dispositivos móveis?**
  
Sim, você pode exibir mensagens no Android e no iOS baixando os aplicativos do Visualizador do OME no [Google Play Store](http://go.microsoft.com/fwlink/?LinkID=525995&amp;clcid=0x409) e na [Apple App Store](http://go.microsoft.com/fwlink/?LinkID=525996&amp;clcid=0x409). Abra o anexo HTML no aplicativo OME Viewer e siga as instruções para abrir sua mensagem criptografada. Para outros dispositivos móveis, você pode abrir o anexo HTML, desde que seu cliente de email ofereça suporte a postagem de formulário.
  
 **P. As respostas e as mensagens encaminhadas são criptografadas?**
  
Sim. As respostas continuam a ser criptografadas durante todo o decurso do thread.
  
 **P. A Criptografia de Mensagem do Office 365 oferece localização?**
  
O conteúdo HTML e de emails de entrada é localizado com base nas configurações de email do remetente. O portal de exibição é localizado com base nas configurações do navegador do destinatário. No entanto, o próprio corpo (conteúdo) da mensagem criptografada não é localizado.
  
 **P. qual método de criptografia é usado para a criptografia de mensagem do Office 365?**
  
A criptografia de mensagem do Office 365 usa o Rights Management Services (RMS) como sua infraestrutura de criptografia. O método de criptografia usado depende de onde você obtém as chaves de RMS usadas para criptografar e descriptografar mensagens.
  
- Se você usar o Microsoft Azure RMS para obter as chaves, o modo criptográfico 2 será usado. O modo criptográfico 2 é uma implementação criptográfica do AD RMS atualizada e aprimorada. Ele suporta o RSA 2048 para assinatura e criptografia e suporta SHA-256 para assinatura.
    
- Se você usar o Active Directory (AD) RMS para obter as chaves, o Modo Criptográfico 1 ou o Modo Criptográfico 2 será utilizado. O método utilizado depende de sua implantação do AD RMS no local. O Modo Criptográfico 1 é a implementação criptográfica original do AD RMS. Ele é compatível com o RSA 1024 para assinatura e criptografia e oferece suporte ao SHA-1 para assinatura. Esse modo continua a receber suporte de todas as versões atuais do RMS.
    
Para obter mais informações, consulte [modos criptográficos do AD RMS](http://go.microsoft.com/fwlink/p/?LinkId=398616).
  
 **P. Por que algumas mensagens criptografadas vêm de Office365@messaging.microsoft.com?**
  
Quando uma resposta criptografada é enviada do portal de criptografia ou pelo aplicativo Visualizador de OME, o endereço de email de envio é definido como Office365@messaging.microsoft.com, porque a mensagem criptografada é enviada por meio de um ponto de extremidade da Microsoft. Isso ajuda a impedir que mensagens criptografadas sejam marcadas como spam. O nome exibido no email e o endereço do portal de criptografia não são alterados por causa desse rótulo. Além disso, esse rótulo só se aplica às mensagens enviadas pelo portal, não por qualquer outro cliente de email.
  
 **P. sou um assinante do Exchange Hosted Encryption (EHE). Onde posso saber mais sobre a atualização para a criptografia de mensagem do Office 365?**
  
Todos os clientes do EHE foram atualizados para a criptografia de mensagem do Office 365. Para obter mais informações, visite o [centro de atualização de criptografia hospedado do Exchange](http://go.microsoft.com/fwlink/p/?LinkID=511077).
  
 **P. preciso abrir qualquer URL, endereço IP ou portas no firewall da minha organização para dar suporte à criptografia de mensagens do Office 365?**
  
Sim. Você precisa adicionar URLs para o Exchange Online à lista de permissões da sua organização para habilitar a autenticação para mensagens criptografadas pela criptografia de mensagem do Office 365. Para obter uma lista de URLs do Exchange Online, confira [URLs e intervalos de endereços IP do Office 365](https://support.office.com/article/f57e35b7-0a45-42f0-855e-11aa5e7f13fd.aspx).
  
 **P. Para quantos destinatários posso enviar uma mensagem criptografada do Office 365?**
  
O limite de destinatários para uma mensagem criptografada baseia-se no número de caracteres no campo **para** da mensagem. Quando combinado (após a expansão da lista de distribuição), os endereços de destinatário no campo **para** não devem exceder 11.980 caracteres. Como os endereços de email podem variar em comprimento de caractere, não há um limite de destinatário padrão para uma única mensagem criptografada. 
  
 **P. É possível revogar uma mensagem enviada para um destinatário específico?**
  
Não. Não é possível revogar uma mensagem para uma determinada pessoa após ela ser enviada.
  
 **P. Posso exibir um relatório de mensagens criptografadas que foram recebidas e lidas?**
  
Não há um relatório que mostra se uma mensagem criptografada foi exibida, mas há relatórios do Office 365 disponíveis que você pode aproveitar para determinar o número de mensagens que corresponderam a uma regra de transporte específica, por exemplo.
  
 **P. O que a Microsoft faz com as informações que forneço por meio do Portal do OME e do aplicativo Visualizador do OME?**
  
A [declaração de privacidade do portal de criptografia de mensagens do Office 365](protected-message-viewer-portal-privacy-statement.md) fornece informações detalhadas sobre o que a Microsoft faz e não faz com suas informações particulares. 
  


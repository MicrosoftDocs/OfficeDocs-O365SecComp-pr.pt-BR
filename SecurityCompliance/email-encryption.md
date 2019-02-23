---
title: Criptografia de email no Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/30/2018
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c0d87cbe-6d65-4c03-88ad-5216ea5564e8
description: Compare as opções de criptografia no Office 365, incluindo a criptografia de mensagem do Office (OME), S/MIME, gerenciamento de direitos de informação (IRM) e saiba mais sobre TLS (Transport Layer Security).
ms.openlocfilehash: 92751bd34a3ff002d53a8b1d088d5d1ac3fcb078
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30213362"
---
# <a name="email-encryption-in-office-365"></a>Criptografia de email no Office 365

Este artigo compara as opções de criptografia no Office 365, incluindo a criptografia de mensagens do Office (OME), S/MIME, gerenciamento de direitos de informação (IRM) e apresenta a segurança da camada de transporte (TLS).
  
O Office 365 oferece várias opções de criptografia para ajudá-lo a atender às suas necessidades comerciais de segurança de email. Este artigo apresenta três maneiras de criptografar emails no Office 365. Se você quiser saber mais sobre todos os recursos de segurança no Office 365, visite a [central de confiabilidade do office 365](http://go.microsoft.com/fwlink/p/?LinkID=282470). Este artigo apresenta os três tipos de criptografia disponíveis para os administradores do Office 365 para ajudar a proteger emails no Office 365:
  
- Criptografia de Mensagem do Office (OME).
    
- S/MIME (Secure/Multipurpose Internet Mail Extensions).
    
- Gerenciamento de Direitos de Informação (IRM).
    
## <a name="what-is-email-encryption-and-how-does-office-365-use-it"></a>O que é a criptografia de email e como o Office 365 a utiliza?

A criptografia é o processo pelo qual as informações são codificadas para que apenas um destinatário autorizado possa decodificar e consumir as informações. O Office 365 usa criptografia de duas maneiras: no serviço e como um controle de cliente. No serviço, a criptografia é usada no Office 365 por padrão; Você não precisa configurar nada. Por exemplo, o Office 365 usa Transport Layer Security (TLS) para criptografar a conexão, ou sessão, entre dois servidores. 
  
Veja aqui como a criptografia de email normalmente funciona:
  
- Uma mensagem é criptografada ou transformada de texto sem formatação em um texto cifrado ilegível, seja no computador do remetente ou por um servidor central enquanto a mensagem estiver em trânsito.
    
- A mensagem permanece em texto cifrado enquanto estiver em trânsito para protegê-la de ser lida, caso a mensagem seja interceptada.
    
- Depois que é recebida pelo destinatário, a mensagem é transformada novamente em texto sem formatação legível por meio de uma das duas maneiras:
    
  - O computador do destinatário usa uma chave para descriptografar a mensagem ou
    
  - Um servidor central descriptografa a mensagem em nome do destinatário, após a validação da identidade do destinatário.
    
Para obter mais informações sobre como o Office 365 protege a comunicação entre servidores, como entre organizações do Office 365 ou entre o Office 365 e um parceiro comercial confiável fora do Office 365, consulte [como o Exchange Online usa o TLS para proteger emails conexões no Office 365](exchange-online-uses-tls-to-secure-email-connections.md).
  
Assista a este vídeo para obter uma introdução à [criptografia no Office 365](https://www.youtube.com/watch?v=KmfxCd5ublI).
  
## <a name="comparing-email-encryption-options-available-in-office-365"></a>Comparação das opções de criptografia de email disponíveis no Office 365

||![Arte conceitual que descreve a OME](media/2bf27b5e-bbb3-46d1-95bf-884dc27a746c.png)|![Arte conceitual que descreve o IRM](media/9c0cc444-9448-40c6-b244-8fcc593a64e0.png)|![Arte conceitual que descreve SMIME](media/ae4613a8-c17e-47e1-8e13-12e891e43744.png)|
|:-----|:-----|:-----|:-----|
|O que é isso?|Criptografia de Mensagens do Office 365 (OME) é um serviço integrado ao Azure Rights Management (Azure RMS) que permite o envio de emails criptografados para pessoas dentro ou fora da sua organização, independente do endereço de email de destino (Gmail, Yahoo! Email, Outlook.com, etc.).  <br/> Como administrador, você pode configurar regras de transporte que definam as condições da criptografia. Quando um usuário envia uma mensagem que corresponde a uma regra, a criptografia é aplicada automaticamente.  <br/> Para exibir mensagens criptografadas, os destinatários podem obter uma senha de uso único, entrar com uma conta da Microsoft ou entrar com uma conta corporativa ou de estudante associada ao Office 365. Os destinatários também podem enviar respostas criptografadas. Eles não precisam de uma assinatura do Office 365 para exibir mensagens criptografadas ou enviar respostas criptografadas.|O IRM é uma solução de criptografia que também aplica restrições de uso a mensagens de email. Isso ajuda a evitar que informações confidenciais sejam impressas, encaminhadas ou copiadas por pessoas não autorizadas.  <br/> Os recursos IRM no Office 365 usam o Azure Rights Management (Azure RMS). 
|S/MIME é uma solução de criptografia baseada em certificado que permite criptografar e assinar digitalmente uma mensagem. A criptografia de mensagens ajuda a garantir que apenas o destinatário pretendido possa abrir e ler a mensagem. Uma assinatura digital ajuda o destinatário a validar a identidade do remetente.  <br/> As assinaturas digitais e a criptografia de mensagem são disponibilizadas por meio do uso de certificados digitais exclusivos que contêm as chaves para verificar assinaturas digitais e criptografar ou descriptografar mensagens.  <br/> Para usar S/MIME, você deve ter chaves públicas no arquivo para cada destinatário. Os destinatários precisam manter suas próprias chaves privadas, o que deve permanecer seguro. Se as chaves privadas de um destinatário estiverem comprometidas, o destinatário precisará obter uma nova chave privada e redistribuir as chaves públicas para todos os remetentes potenciais.|
|E o que isso faz?|OME:  <br/>  Criptografa as mensagens enviadas a destinatários internos ou externos.  <br/>  Permite que os usuários enviem mensagens criptografadas para qualquer endereço de email, incluindo Outlook.com, Yahoo! Mail e Gmail.  <br/>  Permite que você, como administrador, personalize o portal de exibição de email para refletir a marca da sua organização.  <br/>  A Microsoft gerencia e armazena as chaves com segurança, para que você não precise fazê-lo.  <br/>  Nenhum software especial do lado do cliente é necessário, desde que a mensagem criptografada (enviada como um anexo HTML) possa ser aberta em um navegador.|IRM:  <br/>  Usa a criptografia e as restrições de uso para fornecer proteção online e offline para mensagens de email e anexos.  <br/>  Fornece a você, como administrador, a capacidade de configurar as regras de transporte ou as regras de proteção do Outlook para aplicar o IRM automaticamente às mensagens selecionadas.  <br/>  Permite que os usuários apliquem modelos manualmente no Outlook ou no Outlook na Web (anteriormente conhecido como Outlook Web App).|Autenticação de endereços de remetente de S/MIME com assinaturas digitais e confidencialidade de mensagem com criptografia.|
|E o que isso não faz?|O OME não permite que você aplique restrições de uso a mensagens. Por exemplo, você não pode usá-lo para impedir que um destinatário encaminhe ou imprima uma mensagem criptografada.|Alguns aplicativos podem não oferecer suporte a emails do IRM em todos os dispositivos. Para obter mais informações sobre esses e outros produtos que dão suporte a emails do IRM, consulte [recursos do dispositivo cliente](https://technet.microsoft.com/library/dn655136.aspx#BKMK_ClientCapabilities).|O S/MIME não permite que mensagens criptografadas sejam verificadas por malware, spam ou políticas.|
|Cenários de exemplo e recomendações|Recomendamos o uso do OME quando você quiser enviar informações comerciais confidenciais para pessoas de fora da sua organização, seja eles consumidores ou outras empresas. Por exemplo:  <br/>  O funcionário de um banco enviando extratos de cartão de crédito aos clientes  <br/>  O escritório de doutor enviando registros médicos para um paciente  <br/>  Um advogado enviando informações legais confidenciais para outro advogado|É recomendável usar o IRM para aplicar restrições de uso, bem como a criptografia. Por exemplo:  <br/>  Um gerente que envia detalhes confidenciais para sua equipe sobre um novo produto aplica a opção "não enCaminhar".  <br/>  Um executivo que precisa compartilhar uma proposta de lance com outra empresa, que inclui um anexo de um parceiro que está usando o Office 365, e necessita que o email e o anexo sejam protegidos.|É recomendável usar S/MIME quando sua organização ou a organização do destinatário exigir a criptografia de ponto a ponto real.  <br/>  O S/MIME é mais usado nos seguintes cenários:  <br/>  Agências governamentais se comunicando com outras agências governamentais  <br/>  Uma empresa se comunicando com uma agência governamental|
   
## <a name="what-encryption-options-are-available-for-my-office-365-subscription"></a>Quais opções de criptografia estão disponíveis para minha assinatura do Office 365?

Para obter informações sobre as opções de criptografia de email para sua assinatura do Office 365, consulte a [Descrição do serviço do Exchange Online](https://technet.microsoft.com/en-us/library/exchange-online-service-description.aspx). Aqui, você pode encontrar informações sobre os seguintes recursos de criptografia:
  
- Azure RMS, incluindo recursos IRM e OME
    
- S/MIME
    
- TLS
    
- Criptografia de dados inativos (por meio do BitLocker)
    
## <a name="what-about-encryption-for-data-at-rest"></a>E a criptografia de dados inativos?

"Dados em repouso" referem-se aos dados que não estão ativamente em trânsito. No Office 365, os dados de email em repouso são criptografados usando a criptografia de unidade de disco BitLocker. O BitLocker criptografa os discos rígidos nos datacenters do Office 365 para fornecer proteção avançada contra o acesso não autorizado. Para saber mais, confira [visão geral do BitLocker](https://go.microsoft.com/fwlink/p/?LinkId=394737).
  
## <a name="more-information-about-email-encryption-options-in-office-365"></a>Para saber mais sobre as opções de criptografia de email no Office 365

Para saber mais sobre as opções de criptografia de email neste artigo, bem sobre TLS, consulte estes artigos:
  
 **OME**
  
[OME (Criptografia de Mensagens do Office 365)](ome.md)
  
 **IRM**
  
[Gerenciamento de Direitos de Informação no Exchange Online](https://technet.microsoft.com/en-us/library/jj983436%28v=exchg.150%29.aspx)
  
[O que é o Azure Rights Management?](https://technet.microsoft.com/library/jj585026)
  
 **S/MIME**
  
[S/MIME para assinatura e criptografia de mensagens](https://technet.microsoft.com/library/dn626158)
  
[Noções básicas sobre S/MIME](https://technet.microsoft.com/library/aa995740%28v=exchg.65%29.aspx)
  
[Noções básicas sobre criptografia de chave pública](https://technet.microsoft.com/library/aa998077%28v=exchg.65%29.aspx)
  
 **TLS**
  
[Configurar o fluxo de email personalizado usando conectores no Office 365](https://technet.microsoft.com/en-us/library/jj723138%28v=exchg.150%29.aspx)
  


---
title: Criptografia de email no Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/22/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c0d87cbe-6d65-4c03-88ad-5216ea5564e8
description: Comparar as opções de criptografia no Office 365, incluindo Office Message Encryption (OME), S/MIME, gerenciamento de direitos de informação (IRM) e saiba mais sobre a segurança de camada de transporte (TLS).
ms.openlocfilehash: a705637b85e73c6d1e5bcb3595dcd0b7766411e2
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524142"
---
# <a name="email-encryption-in-office-365"></a>Criptografia de email no Office 365

Este artigo compara as opções de criptografia no Office 365, incluindo Office Message Encryption (OME), S/MIME, gerenciamento de direitos de informação (IRM) e apresenta a segurança de camada de transporte (TLS).
  
O Office 365 oferece várias opções de criptografia para ajudá-lo a atender às suas necessidades de negócios para segurança de email. Este artigo apresenta três maneiras para criptografar email no Office 365. Se você deseja saber mais sobre todos os recursos de segurança no Office 365, visite o [Centro de confiança do Office 365](http://go.microsoft.com/fwlink/p/?LinkID=282470). Este artigo apresenta os três tipos de criptografia disponível para administradores do Office 365 ajudar a email seguro no Office 365:
  
- Criptografia de Mensagem do Office (OME).
    
- S/MIME (Secure/Multipurpose Internet Mail Extensions).
    
- Gerenciamento de Direitos de Informação (IRM).
    
## <a name="what-is-email-encryption-and-how-does-office-365-use-it"></a>O que é a criptografia de email e como o Office 365 a utiliza?

Criptografia é o processo pelo qual informação é codificada para que somente um destinatário autorizado possa decodificar e consumir as informações. O Office 365 usa criptografia de duas maneiras: no serviço e como um controle de cliente. No serviço de criptografia é usada no Office 365, por padrão. Você não precisa configurar nada. Por exemplo, o Office 365 usa a segurança de camada de transporte (TLS) para criptografar a conexão, ou sessão, entre dois servidores. 
  
Aqui está como criptografia de email geralmente funciona:
  
- Uma mensagem é criptografada ou transformada de texto sem formatação em texto ilegível codificado, na máquina do remetente ou por um servidor central enquanto a mensagem estiver em trânsito.
    
- A mensagem permanece no texto codificado enquanto ele estiver em trânsito para protegê-lo contra leitura no caso da mensagem é interceptada.
    
- Depois que é recebida pelo destinatário, a mensagem é transformada novamente em texto sem formatação legível por meio de uma das duas maneiras:
    
  - Máquina do destinatário usa uma chave para descriptografar a mensagem, ou
    
  - Um servidor central descriptografa a mensagem em nome do destinatário, após a validação de identidade do destinatário.
    
Para obter mais informações sobre como o Office 365 protege a comunicação entre servidores, tais como entre organizações em Office 365 ou entre o Office 365 e um parceiro de negócios confiáveis fora do Office 365, consulte [como o Exchange da Online usa o TLS para email seguro conexões no Office 365](exchange-online-uses-tls-to-secure-email-connections.md).
  
Assista a este vídeo para ver uma introdução à [criptografia no Office 365](https://www.youtube.com/watch?v=KmfxCd5ublI).
  
## <a name="comparing-email-encryption-options-available-in-office-365"></a>Comparação das opções de criptografia de email disponíveis no Office 365

||**        ![Arte conceitual que descreve a OME](media/2bf27b5e-bbb3-46d1-95bf-884dc27a746c.png)                 **|**        ![Arte conceitual que descreve o IRM](media/9c0cc444-9448-40c6-b244-8fcc593a64e0.png)                 **|**        ![Arte conceitual que descreve SMIME](media/ae4613a8-c17e-47e1-8e13-12e891e43744.png)                 **|
|:-----|:-----|:-----|:-----|
|O que é isso?  <br/> |Criptografia de Mensagens do Office 365 (OME) é um serviço integrado ao Azure Rights Management (Azure RMS) que permite o envio de emails criptografados para pessoas dentro ou fora da sua organização, independente do endereço de email de destino (Gmail, Yahoo! Email, Outlook.com, etc.).  <br/> Como administrador, você pode configurar regras de transporte que definam as condições da criptografia. Quando um usuário envia uma mensagem que corresponde a uma regra, a criptografia é aplicada automaticamente.  <br/> Para ler mensagens criptografadas, os destinatários podem obter uma senha de uma única vez, logon com uma conta da Microsoft ou sinal com um trabalho ou escola conta associada com o Office 365. Destinatários também podem enviar respostas criptografadas. Eles não precisam de uma assinatura do Office 365 para exibir mensagens criptografadas ou enviar respostas criptografadas.  <br/> |O IRM é uma solução de criptografia que também aplica restrições de uso a mensagens de email. Isso ajuda a evitar que informações confidenciais sejam impressas, encaminhadas ou copiadas por pessoas não autorizadas.  <br/> Os recursos IRM no Office 365 usam o Azure Rights Management (Azure RMS). 
  <br/> |S/MIME é uma solução baseada em certificado de criptografia que permite ao criptografar e assinar digitalmente uma mensagem. A criptografia de mensagem ajuda a garantir que somente o destinatário pretendido pode abrir e ler a mensagem. Uma assinatura digital ajuda o destinatário valida a identidade do remetente.  <br/> As assinaturas digitais e a criptografia de mensagem são disponibilizadas por meio do uso de certificados digitais exclusivos que contêm as chaves para verificar assinaturas digitais e criptografar ou descriptografar mensagens.  <br/> Para usar S/MIME, você deve ter as chaves públicas no arquivo para cada destinatário. Destinatários precisam manter suas próprias chaves particulares, que devem permanecer seguros. Se as chaves particulares de um destinatário estão comprometidas, o destinatário precisa fazer uma nova chave privada e redistribua chaves públicas para todos os remetentes possíveis.  <br/> |
|E o que isso faz?  <br/> | OME:  <br/>  Criptografa as mensagens enviadas a destinatários internos ou externos.  <br/>  Permite que os usuários enviem mensagens criptografadas para qualquer endereço de email, incluindo Outlook.com, Yahoo! Mail e Gmail.  <br/>  Permite que você, como um administrador, para personalizar o e-mail exibindo portal para refletir a marca da sua organização.  <br/>  Microsoft gerencia e armazena as chaves, portanto você não precisa com segurança.  <br/>  Nenhum software especial do lado do cliente é necessário, desde que a mensagem criptografada (enviada como um anexo HTML) possa ser aberta em um navegador.  <br/> | IRM:  <br/>  Usa a criptografia e as restrições de uso para fornecer proteção online e offline para mensagens de email e anexos.  <br/>  Fornece a você, como administrador, a capacidade de configurar as regras de transporte ou as regras de proteção do Outlook para aplicar o IRM automaticamente às mensagens selecionadas.  <br/>  Permite que os usuários apliquem modelos manualmente no Outlook ou no Outlook Web App.  <br/> |Autenticação de endereços de remetente de S/MIME com assinaturas digitais e confidencialidade de mensagem com criptografia.  <br/> |
|E o que isso não faz?  <br/> |OME não permitem que você aplique restrições de uso a mensagens. Por exemplo, você não pode usá-lo para interromper um destinatário de encaminhamento ou imprimir uma mensagem criptografada.  <br/> |Alguns aplicativos podem não suportar emails IRM em todos os dispositivos. Para obter mais informações sobre estes e outros produtos que oferecem suporte a email do IRM, consulte [recursos do dispositivo cliente](https://technet.microsoft.com/library/dn655136.aspx#BKMK_ClientCapabilities).<br/> |S/MIME não permite mensagens criptografadas devem ser verificadas para malware, spam ou políticas.  <br/> |
|Cenários de exemplo e recomendações  <br/> | É recomendável usar OME quando quiser enviar informações comerciais confidenciais para pessoas fora da sua organização, se eles estiverem consumidores ou outras empresas. Por exemplo:  <br/>  O funcionário de um banco enviando extratos de cartão de crédito aos clientes  <br/>  Office de um médico enviando registros médicos para um paciente  <br/>  Um advogado enviando informações legais confidenciais para outro advogado  <br/> | É recomendável usar o IRM para aplicar restrições de uso, bem como a criptografia. Por exemplo:  <br/>  Um gerente enviando detalhes confidenciais para sua equipe sobre um novo produto se aplica a opção "Não encaminhar".  <br/>  Um executivo que precisa compartilhar uma proposta de lance com outra empresa, que inclui um anexo de um parceiro que está usando o Office 365, e necessita que o email e o anexo sejam protegidos.  <br/> | É recomendável usar S/MIME quando a sua organização ou empresa do destinatário requer criptografia de ponto a ponto true.  <br/>  O S/MIME é mais usado nos seguintes cenários:  <br/>  Agências governamentais se comunicando com outras agências governamentais  <br/>  Uma empresa se comunicando com uma agência governamental  <br/> |
   
## <a name="what-encryption-options-are-available-for-my-office-365-subscription"></a>Quais opções de criptografia estão disponíveis para minha assinatura do Office 365?

Para obter informações sobre as opções de criptografia de email para sua assinatura do Office 365, consulte a [Descrição do serviço do Exchange Online](https://technet.microsoft.com/en-us/library/exchange-online-service-description.aspx). Aqui, você pode encontrar informações sobre os seguintes recursos de criptografia:
  
- Azure RMS, incluindo recursos IRM e OME
    
- S/MIME
    
- TLS
    
- Criptografia de dados inativos (por meio do BitLocker)
    
## <a name="what-about-encryption-for-data-at-rest"></a>E a criptografia de dados inativos?

"Dados em repouso" refere-se aos dados que não esteja ativamente em trânsito. No Office 365, os dados em repouso de email são criptografados usando a criptografia de unidade de disco BitLocker. O BitLocker criptografa os discos rígidos em centros de dados do Office 365 para fornecer proteção avançada contra acesso não autorizado. Para saber mais, consulte [Visão geral de disco BitLocker](https://go.microsoft.com/fwlink/p/?LinkId=394737).
  
## <a name="more-information-about-email-encryption-options-in-office-365"></a>Para saber mais sobre as opções de criptografia de email no Office 365

Para saber mais sobre as opções de criptografia de email neste artigo, bem sobre TLS, consulte estes artigos:
  
 **OME**
  
[OME (Criptografia de Mensagem do Office 365)](ome.md)
  
 **IRM**
  
[Gerenciamento de Direitos de Informação no Exchange Online](https://technet.microsoft.com/en-us/library/jj983436%28v=exchg.150%29.aspx)
  
[Qual é o Azure Rights Management?](https://technet.microsoft.com/library/jj585026)
  
 **S/MIME**
  
[S/MIME para assinatura e criptografia de mensagens](https://technet.microsoft.com/library/dn626158)
  
[Noções básicas sobre S/MIME](https://technet.microsoft.com/library/aa995740%28v=exchg.65%29.aspx)
  
[Noções básicas sobre a criptografia de chave pública](https://technet.microsoft.com/library/aa998077%28v=exchg.65%29.aspx)
  
 **TLS**
  
[Configurar o fluxo de email personalizado usando conectores no Office 365](https://technet.microsoft.com/en-us/library/jj723138%28v=exchg.150%29.aspx)
  


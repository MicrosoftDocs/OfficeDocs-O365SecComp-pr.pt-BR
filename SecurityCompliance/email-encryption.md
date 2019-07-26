---
title: Criptografia de email no Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/30/2018
audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MOE150
- MET150
ms.assetid: c0d87cbe-6d65-4c03-88ad-5216ea5564e8
ms.collection:
- M365-security-compliance
description: Compara as opções de criptografia no Office 365, incluindo a Criptografia de Mensagem do Office (OME), S/MIME, Gerenciamento de Direitos de Informação (IRM) e apresenta o protocolo TLS (Protocolo TLS).
ms.openlocfilehash: dba0c0d890a7018f9ca5daab2c1e88c4d234c5c3
ms.sourcegitcommit: 33c8e9c16143650ca443d73e91631f9180a9268e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35854675"
---
# <a name="email-encryption-in-office-365"></a>Criptografia de email no Office 365

Este artigo compara as opções de criptografia no Office 365, incluindo a Criptografia de Mensagens do Office (OME), S/MIME, Gerenciamento de Direitos de Informação (IRM) e apresenta o protocolo TLS (Transport Layer Security).
  
O Office 365 oferece várias opções de criptografia para ajudar a atender às necessidades de segurança de email da sua empresa. Este artigo apresenta três maneiras de criptografar emails no Office 365. Se você quiser saber mais sobre todos os recursos de segurança do Office 365, acesse a central [de confiabilidade do Office 365](http://go.microsoft.com/fwlink/p/?LinkID=282470). Este artigo apresenta os três tipos de criptografia disponíveis para administradores do Office 365 para ajudar a proteger o email no Office 365:
  
- Criptografia de Mensagem do Office (OME).
    
- S/MIME (Secure/Multipurpose Internet Mail Extensions).
    
- Gerenciamento de Direitos de Informação (IRM).
    
## <a name="what-is-email-encryption-and-how-does-office-365-use-it"></a>O que é a criptografia de email e como o Office 365 a utiliza?

Criptografia é o processo pelo qual as informações são codificadas para que somente um destinatário autorizado possa decodificar e consumir as informações. O Office 365 usa criptografia de duas maneiras: no serviço e como um controle de cliente. No serviço, a criptografia é usada no Office 365 por padrão; não é necessário configurar nada. Por exemplo, o Office 365 usa o protocolo Segurança na camada de transporte (TLS) para criptografar a conexão, ou sessão, entre dois servidores. 
  
Veja aqui como a criptografia de email normalmente funciona:
  
- Uma mensagem é criptografada, ou transformada de texto sem formatação em texto cifrado ilegível, no computador do remetente ou por um servidor central, enquanto a mensagem está em trânsito.
    
- A mensagem permanece em texto cifrado enquanto está em trânsito para impedir a leitura caso seja interceptada.
    
- Depois que é recebida pelo destinatário, a mensagem é transformada novamente em texto sem formatação legível por meio de uma das duas maneiras:
    
  - O computador do destinatário usa uma chave para descriptografar a mensagem, ou
    
  - Um servidor central descriptografa a mensagem em nome do destinatário, após a validação da identidade do destinatário.
    
Confira mais informações sobre como o Office 365 protege a comunicação entre servidores, por exemplo, entre organizações dentro do Office 365 ou entre o Office 365 e um parceiro de negócios confiável fora do Office 365, confira em [Como o Office 365 usa TLS para proteger conexões entre servidores](exchange-online-uses-tls-to-secure-email-connections.md).
  
Assista a este vídeo para obter uma [introdução à criptografia no Office 365](https://www.youtube.com/watch?v=KmfxCd5ublI).
  
## <a name="comparing-email-encryption-options-available-in-office-365"></a>Comparação das opções de criptografia de email disponíveis no Office 365

||![Arte conceitual que descreve a OME](media/2bf27b5e-bbb3-46d1-95bf-884dc27a746c.png)|![Arte conceitual que descreve o IRM](media/9c0cc444-9448-40c6-b244-8fcc593a64e0.png)|![Arte conceitual que descreve SMIME](media/ae4613a8-c17e-47e1-8e13-12e891e43744.png)|
|:-----|:-----|:-----|:-----|
|O que é isso?|Criptografia de Mensagens do Office 365 (OME) é um serviço integrado ao Azure Rights Management (Azure RMS) que permite o envio de emails criptografados para pessoas dentro ou fora da sua organização, independente do endereço de email de destino (Gmail, Yahoo! Email, Outlook.com, etc.).  <br/> Como administrador, você pode configurar regras de transporte que definam as condições da criptografia. Quando um usuário envia uma mensagem que corresponde a uma regra, a criptografia é aplicada automaticamente.  <br/> Para exibir mensagens criptografadas, os destinatários podem obter uma senha avulsa, entrar com uma conta da Microsoft ou com uma conta corporativa ou de estudante associada ao Office 365. Os destinatários também podem enviar respostas criptografadas. Não é necessário ter uma assinatura do Office 365 para exibir mensagens criptografadas ou enviar respostas criptografadas.|O IRM é uma solução de criptografia que também aplica restrições de uso a mensagens de email. Isso ajuda a evitar que informações confidenciais sejam impressas, encaminhadas ou copiadas por pessoas não autorizadas.  <br/> Os recursos IRM no Office 365 usam o Azure Rights Management (Azure RMS).|S/MIME é uma solução de criptografia baseada em certificados que permite criptografar e assinar digitalmente uma mensagem. A criptografia de mensagem ajuda a garantir que somente o destinatário pretendido poderá abrir e ler a mensagem. Uma assinatura digital ajuda o destinatário a validar a identidade do remetente.  <br/> As assinaturas digitais e a criptografia de mensagem são disponibilizadas por meio do uso de certificados digitais exclusivos que contêm as chaves para verificar assinaturas digitais e criptografar ou descriptografar mensagens.  <br/> Para usar S/MIME, você deve ter as chaves públicas no arquivo para cada destinatário. Os destinatários precisam manter suas próprias chaves privadas, que devem permanecer seguras. Se as chaves particulares de um destinatário estiverem comprometidas, o destinatário precisará obter uma nova chave privada e redistribuir chaves públicas para todos os possíveis remetentes.|
|E o que isso faz?|OME:  <br/>  Criptografa as mensagens enviadas a destinatários internos ou externos.  <br/>  Permite que os usuários enviem mensagens criptografadas para qualquer endereço de email, incluindo Outlook.com, Yahoo! Mail e Gmail.  <br/>  Permite que você, como administrador, personalize o portal de exibição do email para refletir a marca da sua organização.  <br/>  A Microsoft gerencia e armazena as chaves de maneira segura, para que você não precise fazer isso.  <br/>  Nenhum software especial do lado do cliente é necessário, desde que a mensagem criptografada (enviada como um anexo HTML) possa ser aberta em um navegador.|IRM:  <br/>  Usa a criptografia e as restrições de uso para fornecer proteção online e offline para mensagens de email e anexos.  <br/>  Fornece a você, como administrador, a capacidade de configurar as regras de transporte ou as regras de proteção do Outlook para aplicar o IRM automaticamente às mensagens selecionadas.  <br/>  Permite que os usuários apliquem modelos manualmente no Outlook ou no Outlook na Web (conhecida anteriormente com Outlook Web App).|Autenticação de endereços de remetente de S/MIME com assinaturas digitais e confidencialidade de mensagem com criptografia.|
|E o que isso não faz?|A OME não permite que você aplique restrições de uso às mensagens. Por exemplo, você não pode usá-la para impedir que um destinatário encaminhe ou imprima uma mensagem criptografada.|Alguns aplicativos podem não suportar emails IRM em todos os dispositivos. Para saber mais sobre esses e outros produtos que oferecem suporte a emails IRM, confira [ recursos de dispositivos cliente](https://technet.microsoft.com/library/dn655136.aspx#BKMK_ClientCapabilities).|O S/MIME não permite que mensagens criptografadas sejam verificadas para malware, spam ou políticas.|
|Cenários de exemplo e recomendações|É recomendável usar a OME para enviar informações comerciais confidenciais para pessoas fora da sua organização, sejam consumidores ou outras empresas. Por exemplo:  <br/>  O funcionário de um banco enviando extratos de cartão de crédito aos clientes  <br/>  Um consultório enviando prontuários médicos para um paciente  <br/>  Um advogado enviando informações legais confidenciais para outro advogado|É recomendável usar o IRM para aplicar restrições de uso, bem como a criptografia. Por exemplo:  <br/>  Um gerente enviando detalhes confidenciais para sua equipe sobre um novo produto aplica a opção "Não Encaminhar".  <br/>  Um executivo que precisa compartilhar uma proposta de lance com outra empresa, que inclui um anexo de um parceiro que está usando o Office 365, e necessita que o email e o anexo sejam protegidos.|É recomendável usar o S/MIME quando sua organização ou a empresa do destinatário exigirem criptografia de ponto a ponto verdadeira.  <br/>  O S/MIME é mais usado nos seguintes cenários:  <br/>  Agências governamentais se comunicando com outras agências governamentais  <br/>  Uma empresa se comunicando com uma agência governamental|
   
## <a name="what-encryption-options-are-available-for-my-office-365-subscription"></a>Quais opções de criptografia estão disponíveis para minha assinatura do Office 365?

Para saber mais sobre as opções de criptografia de email da sua assinatura [do Office 365,](https://technet.microsoft.com/en-us/library/exchange-online-service-description.aspx)Confira a descrição do serviço do Exchange Online. Aqui você pode encontra informações sobre os seguintes recursos de criptografia:
  
- Azure RMS, incluindo recursos IRM e OME
    
- S/MIME
    
- TLS
    
- Criptografia de dados inativos (por meio do BitLocker)
    
## <a name="what-about-encryption-for-data-at-rest"></a>E a criptografia de dados inativos?

"Dados inativos" se refere aos dados que não estão ativamente em trânsito. No Office 365, os dados inativos do email são criptografados usando a Criptografia de Unidade de Disco BitLocker. O BitLocker criptografa os discos rígidos em datacenters do Office 365 para fornecer proteção avançada contra acesso não autorizado. Saiba mais em [Visão geral do BitLocker](https://go.microsoft.com/fwlink/p/?LinkId=394737).
  
## <a name="more-information-about-email-encryption-options-in-office-365"></a>Para saber mais sobre as opções de criptografia de email no Office 365

Para saber mais sobre as opções de criptografia de email neste artigo, bem sobre TLS, consulte estes artigos:
  
 **OME**
  
[Criptografia de Mensagens do Office 365 (OME)](ome.md)
  
 **IRM**
  
[Gerenciamento de Direitos de Informação no Exchange Online](https://technet.microsoft.com/en-us/library/jj983436%28v=exchg.150%29.aspx)
  
[ O que é o Azure Rights Management? ](https://technet.microsoft.com/library/jj585026)
  
 **S/MIME**
  
[S/MIME para assinatura e criptografia de mensagens](https://technet.microsoft.com/library/dn626158)
  
[Noções básicas sobre S/MIME](https://technet.microsoft.com/library/aa995740%28v=exchg.65%29.aspx)
  
[Noções básicas sobre criptografia de chave pública](https://technet.microsoft.com/library/aa998077%28v=exchg.65%29.aspx)
  
 **TLS**
  
[Configurar o fluxo de emails usando conectores no Office 365](https://technet.microsoft.com/en-us/library/jj723138%28v=exchg.150%29.aspx)
  


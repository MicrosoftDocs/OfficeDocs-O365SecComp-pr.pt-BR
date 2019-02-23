---
title: Criptografia no Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/3/2018
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
search.appverid:
- MET150
- MOE150
ms.assetid: 0a322724-08ca-43db-b69a-afbfa20484cd
description: Com o Office 365, seu conteúdo é criptografado em repouso e em trânsito, usando a criptografia, protocolos e tecnologias mais fortes disponíveis. Obtenha uma visão geral da criptografia no Office 365.
ms.openlocfilehash: 6371bc7fabfccfca30d1e8fec94d4f22c1c6f492
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30223660"
---
# <a name="encryption-in-office-365"></a>Criptografia no Office 365

A criptografia é uma parte importante das estratégias de proteção de arquivos e proteção de informações. Leia este artigo para obter uma visão geral da criptografia usada para todas as versões do Office 365 e obter ajuda com tarefas de criptografia, desde configurar a criptografia para sua organização para proteger com senha os documentos do Office.
  
- Se você estiver procurando informações sobre certificados e tecnologias como TLS, consulte [Technical Reference Details about Encryption in Office 365](technical-reference-details-about-encryption.md).
    
- Se você estiver procurando informações sobre como configurar ou configurar a criptografia para sua organização, consulte [set up Encryption in Office 365 Enterprise](set-up-encryption.md).
    
## <a name="what-is-encryption-and-how-does-it-work-in-office-365"></a>O que é criptografia e como ela funciona no Office 365?

Em um nível alto, a criptografia é o processo de codificar seus dados (chamados de texto sem formatação) em texto cifrado que não pode ser usado por pessoas ou computadores, a menos que e até que o texto cifrado seja descriptografado. A desCriptografia requer uma chave de criptografia que apenas usuários autorizados têm. A criptografia ajuda a garantir que apenas destinatários autorizados possam descriptografar o conteúdo, como mensagens de email e arquivos.
  
A criptografia por si só não impede o conteúdo, como arquivos, mensagens de email, entradas de calendário e assim por diante, desde o recebimento das mãos erradas. A criptografia faz parte de uma estratégia de proteção de informações maior para sua organização. Usando a criptografia, você pode ajudar a garantir que apenas as pessoas que devem ser capazes de usar dados criptografados sejam capazes de fazê-lo.
  
Você pode ter várias camadas de criptografia no lugar ao mesmo tempo. Por exemplo, você pode criptografar mensagens de email e também os canais de comunicação através dos quais seu email flui. Com o Office 365, seus dados são criptografados em repouso e em trânsito, usando vários protocolos de criptografia fortes e tecnologias que incluem segurança da camada de transporte/Secure Sockets Layer (TLS/SSL), segurança do protocolo Internet (IPSec) e criptografia avançada Padrão (AES).
  
## <a name="encryption-for-data-at-rest-and-data-in-transit"></a>Criptografia de dados em repouso e dados em trânsito

 **Exemplos de dados em repouso** incluem arquivos que foram carregados para uma biblioteca do SharePoint, dados do Project online, documentos que foram carregados em uma reunião do Skype for Business, mensagens de email e anexos armazenados em pastas no seu Office 365 caixa de correio e arquivos carregados para o OneDrive for Business. 
  
 **Exemplos de dados em trânsito** incluem mensagens de email que estão no processo de entrega ou conversas que estão ocorrendo em uma reunião online. No Office 365, os dados estão em trânsito sempre que o dispositivo de um usuário está se comunicando com um servidor do Office 365 ou quando um servidor do Office 365 está se comunicando com outro servidor. 
  
Com o Office 365, você pode ter várias camadas e tipos de criptografia trabalhando juntos para proteger seus dados. A tabela a seguir inclui alguns exemplos, com links para informações adicionais.
  
|**Tipos de conteúdo**|**Tecnologias de criptografia**|**Recursos para saber mais**|
|:-----|:-----|:-----|
|Arquivos em um dispositivo. Isso pode incluir mensagens de email salvas em uma pasta, documentos do Office salvos em um computador, Tablet ou telefone ou dados salvos na nuvem da Microsoft.  <br/> |BitLocker nos datacenters da Microsoft. O BitLocker também pode ser usado em máquinas clientes, como computadores e tablets do Windows  <br/> Gerenciador de chaves distribuídas (DKM) nos datacenters da Microsoft  <br/> Chave de cliente do Office 365  <br/> |[Centro de ti do Windows: BitLocker](https://docs.microsoft.com/windows/device-security/bitlocker/bitlocker-overview) <br/> [Centro de confiança da Microsoft: criptografia](https://www.microsoft.com/en-us/TrustCenter/Security/Encryption) <br/> [Série de controles de segurança na nuvem: Criptografando dados em repouso](https://blogs.microsoft.com/microsoftsecure/2015/09/10/cloud-security-controls-series-encrypting-data-at-rest) <br/> [Como o Exchange Online protege seus segredos de e-mail](exchange-online-secures-email-secrets.md) <br/> [Controlar seus dados no Office 365 usando a Chave do cliente](controlling-your-data-using-customer-key.md) <br/> |
|Arquivos em trânsito entre usuários. Isso pode incluir documentos do Office ou itens de lista do SharePoint compartilhados entre usuários.  <br/> |TLS para arquivos em trânsito  <br/> |[Criptografia de dados no OneDrive for Business e no SharePoint Online](data-encryption-in-odb-and-spo.md) <br/> [Skype for Business Online: segurança e arquivamento](https://technet.microsoft.com/library/skype-for-business-online-security-and-archiving.aspx) <br/> |
|Email em trânsito entre destinatários. Isso inclui email hospedado pelo Exchange Online.  <br/> |Criptografia de mensagem do Office 365 com o Azure Rights Management, S/MIME e TLS para email em trânsito  <br/> |[OME (Criptografia de Mensagens do Office 365)](ome.md) <br/> [Criptografia de e-mail no Office 365](email-encryption.md) <br/> [Como o Exchange Online usa o TLS para proteger conexões de e-mail no Office 365](exchange-online-uses-tls-to-secure-email-connections.md) <br/> |
   
## <a name="what-if-i-need-more-control-over-encryption-to-meet-security-and-compliance-requirements"></a>E se eu precisar de mais controle sobre a criptografia para atender aos requisitos de segurança e conformidade?

Além das soluções gerenciadas pela Microsoft de criptografia de volume, criptografia de arquivo e criptografia de caixa de correio no Office 365, as opções gerenciadas pelo cliente podem ser usadas para atender a requisitos de segurança e conformidade mais rigorosos. Essas soluções usam o Azure Rights Management (Azure RMS) junto com o Office 365.
  
ConFira os seguintes recursos para saber mais:
  
- [O que é o Azure Rights Management?](https://docs.microsoft.com/information-protection/understand-explore/what-is-azure-rms)
    
- [Ativar o Rights Management no Centro de administração do Office 365](https://support.office.com/article/5b6d3ac7-b1ac-428e-b03e-50e882f85a6e)
    
- [Set up Information Rights Management (IRM) in SharePoint admin center](set-up-irm-in-sp-admin-center.md)
    
## <a name="how-do-i"></a>Como faço para...

|**Para executar esta tarefa**|**ConFira estes recursos**|
|:-----|:-----|
|Configurar a criptografia para minha organização  <br/> |[Configure a criptografia no Office 365 Enterprise](set-up-encryption.md) <br/> |
|Exibir detalhes sobre certificados, tecnologias e pacotes de criptografia TLS no Office 365  <br/> |[Detalhes técnicos sobre a criptografia no Office 365](technical-reference-details-about-encryption.md) <br/> |
|Trabalhar com mensagens criptografadas em um dispositivo móvel  <br/> |[Exibir mensagens criptografadas no seu dispositivo Android](https://support.office.com/article/83d60f17-2305-407a-a762-7d518401fdeb) <br/> [Exibir mensagens criptografadas no seu iPhone ou iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf) <br/> |
|Criptografar um documento usando a proteção por senha  <br/><br/>  No momento, a proteção por senha não é suportada no Office Online. Use versões de área de trabalho do Word, Excel e PowerPoint para proteção por senha.           |[Adicionar ou remover proteção em seu documento, pasta de trabalho ou apresentação](https://support.office.com/article/05084cc3-300d-4c1a-8416-38d3e37d6826) (Escolha uma seção **Adicionar proteção** e, em seguida, confira **criptografar com senha** )  <br/> |
|Remover a criptografia de um documento  <br/> |[Adicionar ou remover proteção em seu documento, pasta de trabalho ou apresentação](https://support.office.com/article/05084cc3-300d-4c1a-8416-38d3e37d6826) (Escolha uma seção **remover proteção** e, em seguida, consulte **remover criptografia de senha** )  <br/> |
   
## <a name="related-topics"></a>Tópicos relacionados

[Planejar recursos de proteção de informações e segurança do Office 365](https://support.office.com/article/3d4ac4a1-3920-4ff9-918f-011f3ce60408)
  
[Segurança e conformidade no Office 365 para empresas-ajuda para administradores](https://support.office.com/article/7fe448f7-49bd-4d3e-919d-0a6d1cf675bb)
  


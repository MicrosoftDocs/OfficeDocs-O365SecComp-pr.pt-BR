---
title: Criptografia no Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/3/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: 0a322724-08ca-43db-b69a-afbfa20484cd
description: Com o Office 365, seu conteúdo é criptografado em repouso e em trânsito, usando o mais forte criptografia, protocolos e tecnologias disponíveis. Obtenha uma visão geral da criptografia no Office 365.
ms.openlocfilehash: a9f37fddf28461ee4912e0b8a1f5b922c59c009f
ms.sourcegitcommit: 17c7e18d7d00135b1af40cbea117c9a817a41117
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/24/2018
ms.locfileid: "24972283"
---
# <a name="encryption-in-office-365"></a>Criptografia no Office 365

Criptografia é uma parte importante do seus estratégias de proteção de informações e a proteção de arquivo. Leia este artigo para obter uma visão geral de criptografia usada para todas as versões do Office 365 e obter ajuda com tarefas de criptografia, desde a configuração de criptografia para a sua organização a documentos do Office de proteção de senha.
  
- Se você estiver procurando informações sobre certificados e tecnologias, como o TLS, consulte [os detalhes de referência técnica sobre criptografia no Office 365](technical-reference-details-about-encryption.md).
    
- Se você estiver procurando por informações sobre como configurar ou configure a criptografia para sua organização, consulte [Configure a criptografia no Office 365 Enterprise](set-up-encryption.md).
    
## <a name="what-is-encryption-and-how-does-it-work-in-office-365"></a>O que é criptografia e como ele funciona no Office 365?

Em um alto nível, a criptografia é o processo de codificação de seus dados (conhecidos como texto não criptografado) em texto codificado que não pode ser usado por pessoas ou computadores, a menos e até que o texto codificado é descriptografado. Descriptografia requer uma chave de criptografia que têm apenas os usuários autorizados. Criptografia ajuda a garantir que somente os destinatários autorizados podem descriptografar seu conteúdo, como mensagens de email e arquivos.
  
Criptografia por si só não impede que conteúdo, como arquivos, mensagens de email, entradas de calendário e assim por diante, obtendo em mãos erradas. A criptografia é parte da estratégia de proteção de informações de maior para a sua organização. Usando criptografia, você pode ajudar a garantir que somente aqueles que deve ser capaz de usar os dados criptografados sejam capazes de.
  
Você pode ter várias camadas de criptografia no lugar ao mesmo tempo. Por exemplo, você pode criptografar mensagens de email e também os canais de comunicação por meio do qual seu email flui. Com o Office 365, os dados são criptografados em repouso e em trânsito, usando os vários protocolos de criptografia forte e tecnologias que incluem Transport Layer Security/Secure Sockets Layer (TLS/SSL), Internet Protocol Security (IPSec) e criptografia avançadas AES (padrão).
  
## <a name="encryption-for-data-at-rest-and-data-in-transit"></a>Criptografia de dados em repouso e os dados em trânsito

 **Exemplos de dados em repouso** incluem arquivos que foram carregados para uma biblioteca do SharePoint, dados do Project Online, os documentos que foram carregados em um Skype para reunião da empresa, mensagens de email e anexos que são armazenados em pastas no seu Office 365 caixa de correio e arquivos carregados ao OneDrive for Business. 
  
 Mensagens de email que estão no processo de ser entregue ou conversas que estão ocorrendo em uma reunião online são exemplos **de dados em trânsito** . No Office 365, dados estão em trânsito, sempre que um dispositivo do usuário está se comunicando com um servidor do Office 365, ou quando um servidor do Office 365 está se comunicando com outro servidor. 
  
Com o Office 365, você pode realizar várias camadas e tipos de criptografia trabalhando juntos para proteger os dados. A tabela a seguir inclui alguns exemplos, com links para informações adicionais.
  
|**Tipos de conteúdo**|**Tecnologias de criptografia**|**Recursos para saber mais**|
|:-----|:-----|:-----|
|Arquivos em um dispositivo. Isso pode incluir mensagens de email salvas em uma pasta, os documentos do Office salvos em um computador, um tablet ou um telefone ou dados salvos para a nuvem da Microsoft.  <br/> |BitLocker em centros de dados da Microsoft. O BitLocker também pode ser usado em computadores clientes, como computadores Windows e tablets  <br/> Gerenciador de chave distribuído (DKM) em centros de dados da Microsoft  <br/> Chave de cliente para o Office 365  <br/> |[Windows IT Center: BitLocker](https://docs.microsoft.com/windows/device-security/bitlocker/bitlocker-overview) <br/> [Central de confiabilidade da Microsoft: criptografia](https://www.microsoft.com/en-us/TrustCenter/Security/Encryption) <br/> [Série de controles de segurança na nuvem: criptografar dados em repouso](https://blogs.microsoft.com/microsoftsecure/2015/09/10/cloud-security-controls-series-encrypting-data-at-rest) <br/> [Como o Exchange Online protege seus segredos de email](exchange-online-secures-email-secrets.md) <br/> [Controlar seus dados no Office 365 usando a Chave do cliente](controlling-your-data-using-customer-key.md) <br/> |
|Arquivos em trânsito entre usuários. Isso pode incluir documentos do Office ou itens de lista do SharePoint compartilhadas entre usuários.  <br/> |TLS para arquivos em trânsito  <br/> |[Criptografia de dados no OneDrive for Business e no SharePoint Online](data-encryption-in-odb-and-spo.md) <br/> [Skype para negócios on-line: segurança e arquivamento](https://technet.microsoft.com/library/skype-for-business-online-security-and-archiving.aspx) <br/> |
|Em trânsito entre os destinatários de email. Isso inclui email hospedado pelo Exchange Online.  <br/> |Criptografia de mensagem do Office 365 com o Azure Rights Management, S/MIME e TLS para email em trânsito  <br/> |[OME (Criptografia de Mensagem do Office 365)](ome.md) <br/> [Criptografia de email no Office 365](email-encryption.md) <br/> [Como o Exchange Online usa o TLS para proteger conexões de email no Office 365](exchange-online-uses-tls-to-secure-email-connections.md) <br/> |
   
## <a name="what-if-i-need-more-control-over-encryption-to-meet-security-and-compliance-requirements"></a>O que ocorre se eu precisa de mais controle sobre a criptografia para atender aos requisitos de segurança e conformidade?

Além das soluções Microsoft gerenciados de criptografia de volume, a criptografia de arquivo e criptografia de caixa de correio no Office 365, opções de gerenciado pelo cliente podem ser usadas para atender aos requisitos mais exigentes de segurança e conformidade. Essas soluções usam o Azure Rights Management (RMS Azure) em conjunto com o Office 365.
  
Consulte os seguintes recursos para saber mais:
  
- [Qual é o Azure Rights Management?](https://docs.microsoft.com/information-protection/understand-explore/what-is-azure-rms)
    
- [Ativar o Rights Management no Centro de administração do Office 365](https://support.office.com/article/5b6d3ac7-b1ac-428e-b03e-50e882f85a6e)
    
- [Definir o gerenciamento de direitos de informação (IRM) no Centro de administração do SharePoint](set-up-irm-in-sp-admin-center.md)
    
## <a name="how-do-i"></a>Como posso fazer …

|**Para executar esta tarefa**|**Consulte estes recursos**|
|:-----|:-----|
|Configurar a criptografia para minha organização  <br/> |[Configure a criptografia no Office 365 Enterprise](set-up-encryption.md) <br/> |
|Exibir detalhes sobre certificados, tecnologias e os conjuntos de codificação TLS no Office 365  <br/> |[Detalhes técnicos sobre criptografia no Office 365](technical-reference-details-about-encryption.md) <br/> |
|Trabalhar com mensagens criptografadas em um dispositivo móvel  <br/> |[Visualizar mensagens criptografadas no seu dispositivo Android](https://support.office.com/article/83d60f17-2305-407a-a762-7d518401fdeb) <br/> [Visualizar mensagens criptografadas no seu iPhone ou iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf) <br/> |
|Criptografar um documento usando a proteção por senha  <br/><br/>  Atualmente, a proteção por senha não é suportada no Office Online. Use as versões da área de trabalho do Word, Excel e PowerPoint para proteção por senha.           |[Adicionar ou remover proteção em seu documento, pasta de trabalho ou apresentação](https://support.office.com/article/05084cc3-300d-4c1a-8416-38d3e37d6826) (Escolha uma seção de **proteção de adicionar** e, em seguida, consulte **Criptografar com senha** )  <br/> |
|Remover a criptografia de um documento  <br/> |[Adicionar ou remover proteção em seu documento, pasta de trabalho ou apresentação](https://support.office.com/article/05084cc3-300d-4c1a-8416-38d3e37d6826) (Escolha uma seção **Remover a proteção** e, em seguida, consulte **Remover a criptografia de senha** )  <br/> |
   
## <a name="related-topics"></a>Tópicos relacionados

[Planejar os recursos de proteção de segurança e as informações do Office 365](https://support.office.com/article/3d4ac4a1-3920-4ff9-918f-011f3ce60408)
  
[Segurança e conformidade no Office 365 para empresas - ajuda de Admin](https://support.office.com/article/7fe448f7-49bd-4d3e-919d-0a6d1cf675bb)
  


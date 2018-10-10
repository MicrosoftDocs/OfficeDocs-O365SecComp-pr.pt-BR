---
title: Proteção Avançada contra Ameaças do Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 10/09/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e100fe7c-f2a1-4b7d-9e08-622330b83653
description: Proteção de ameaça avançada do Office 365 inclui falso intelligence, links confiáveis, anexos seguros e recursos avançados de AntiPhishing. Proteção avançada de ameaça é também está sendo estendida para arquivos no SharePoint Online, o OneDrive for Business e Teams da Microsoft.
ms.openlocfilehash: fed816ec8cd0e3e7a6b5118fde35d81647b94f02
ms.sourcegitcommit: 099bbfb1d16b251fd5cf18ec6515faaf9a989176
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25454348"
---
# <a name="office-365-advanced-threat-protection"></a>Proteção Avançada contra Ameaças do Office 365

O Office 365 avançadas ameaça proteção (ATP) ajuda a proteger sua organização contra ataques mal-intencionados por:
  
- Anexos de email de verificação de malware com [Anexos de seguros ATP](atp-safe-attachments.md)
    
- Verificação de web endereços (URLs) em mensagens de email e documentos do Office com [Links de seguros ATP](atp-safe-links.md)
    
- Identificando e bloqueando mal-intencionado arquivos em bibliotecas online com [ATP para SharePoint, OneDrive e as equipes da Microsoft](atp-for-spo-odb-and-teams.md)
    
- Verificando mensagens de email para falsificação não autorizado com [falsificação de inteligência de dados](learn-about-spoof-intelligence.md)
    
- Detectando quando alguém tenta representar seus usuários e domínios personalizados de sua organização com [recursos de AntiPhishing ATP no Office 365](atp-anti-phishing.md)
    
**Proteção por meio do Office 365 ATP é determinada pelas políticas que define as equipe de segurança da sua organização para Links de seguros, anexos seguros e antiphishing**. É importante Revise periodicamente e revisar suas políticas para mantê-los atualizados e para realizar as vantagens dos novos recursos que são adicionados ao serviço. [Os relatórios estão disponíveis](view-reports-for-atp.md) para mostrar como ATP está trabalhando para sua organização. Esses relatórios também podem mostrar áreas onde você pode precisar revisar e atualizar suas políticas. E, se você tiver arquivos que são marcados como malware que não deveria estar ou arquivos que você gostaria que a Microsoft para examinar, você pode [Enviar um arquivo para a Microsoft para análise](#submit-a-suspicious-file-to-microsoft-for-analysis).
      
## <a name="get-office-365-atp"></a>Obter ATP do Office 365

> [!IMPORTANT]
> O Office 365 ATP está incluído no inscrições, como Microsoft 365 Enterprise, Office 365 Enterprise E5, A5 de educação do Office 365 e [Microsoft 365 Business](https://support.office.com/article/c123694a-1efb-459e-a8d5-2187975373dc). Se sua organização tiver uma assinatura do Office 365 que não inclui ATP do Office 365, você pode adquirir potencialmente ATP como um complemento. Para obter mais informações, consulte [Office 365 avançadas Threat Protection Service Description](https://technet.microsoft.com/library/exchange-online-advanced-threat-protection-service-description.aspx). 

1. Como um administrador global ou de segurança, vá para [https://portal.office.com](https://portal.office.com) e entre com sua conta de trabalho ou da escola para o Office 365. 
    
2. Escolha **administrador** \> **cobrança** para ver o que inclui a sua assinatura atual. <br/>![Como um administrador global, entrar no portal.office.com e vá até Admin \> de cobrança](media/18a3546c-bd1f-4f49-82ec-0184909b42c2.png)
  
3. Se você vir **E5 do Office 365 Enterprise**, **A5 de educação do Office 365**ou **Microsoft 365 Business**, sua organização tem ATP. <br/>Se você vir uma assinatura diferente, como o **Office 365 Enterprise E3** ou **Office 365 Enterprise E1**, considere a adição de ATP. Para fazer isso, escolha **+ Adicionar assinatura**.
    
Depois que você tiver ATP, a próxima etapa é para sua equipe de segurança definir políticas. 
  
## <a name="define-policies-for-atp"></a>Definir diretivas para ATP

- **[Configurar políticas de AntiPhishing ATP no Office 365](set-up-atp-anti-phishing-policies.md)** incluindo ataques baseados em representação para proteger contra invasores que enviam mensagens de email que parecem ser de pessoas confiáveis ou domínios 

- **[Configurar políticas de Links de ATP seguros no Office 365](set-up-atp-safe-links-policies.md)** , incluindo [lista personalizada de URLs bloqueada](set-up-a-custom-blocked-urls-list-wtih-atp.md) e a [lista de URLs personalizada "Não regravação"](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) da sua organização
    
- **[Configurar anexos seguros de ATP políticas no Office 365](set-up-atp-safe-attachments-policies.md)** que pode incluir a [entrega dinâmica e visualização](dynamic-delivery-and-previewing.md)
  
## <a name="see-how-atp-is-working-by-viewing-reports"></a>Consulte como ATP está funcionando exibindo relatórios

Depois que suas políticas de ATP estão funcionando, relatórios estão disponíveis para mostrar como o serviço está funcionando.

[![A segurança &amp; painel do Centro de conformidade pode ajudá-lo a ver onde a proteção de ameaça Avançado está funcionando](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)](view-reports-for-atp.md)
  
1. Certifique-se de que você é um administrador global, administrador de segurança ou leitor de segurança do Office 365. (Consulte [Permissions in a segurança do Office 365 &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md).)
    
2. [Exibir relatórios de proteção avançada de ameaça](view-reports-for-atp.md).
    
3. Se necessário, fazer ajustes suas políticas de segurança. Consulte os seguintes recursos:

  - [Políticas de AntiPhishing ATP no Office 365](set-up-atp-anti-phishing-policies.md)
    
  - [Políticas de Links de ATP seguros no Office 365](set-up-atp-safe-links-policies.md)
    
  - [Políticas de anexos de ATP seguros no Office 365](set-up-atp-safe-attachments-policies.md)
    
    
## <a name="submit-a-suspicious-file-to-microsoft-for-analysis"></a>Enviar um arquivo suspeito à Microsoft para análise

- Se você receber um arquivo que você supõe que poderia ser malware, você poderá enviar esse arquivo para a Microsoft para análise. Visite o [portal de envio de inteligência de segurança do Windows Defender](https://go.microsoft.com/fwlink/?linkid=857185).

- Se você receber uma mensagem de email (com ou sem um anexo) que deseja usar para enviar à Microsoft para análise, use o [suplemento de mensagem de relatório](enable-the-report-message-add-in.md). 
  
## <a name="related-topics"></a>Tópicos relacionados

[Exibir relatórios de Proteção avançada contra ameaças](view-reports-for-atp.md)
  
[Gerenciamento de segurança do Office 365 de ameaça &amp; Centro de conformidade](threat-management.md)
  


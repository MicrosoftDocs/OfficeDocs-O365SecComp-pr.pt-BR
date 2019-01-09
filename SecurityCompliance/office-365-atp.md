---
title: Proteção Avançada contra Ameaças do Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/08/2019
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e100fe7c-f2a1-4b7d-9e08-622330b83653
description: Proteção de ameaça avançada do Office 365 inclui falso intelligence, links confiáveis, anexos seguros e recursos avançados de AntiPhishing. Proteção avançada de ameaça é também está sendo estendida para arquivos no SharePoint Online, o OneDrive for Business e Teams da Microsoft.
ms.openlocfilehash: 6cdbdde2c91f8a9a77eb688ae27d509163da42a1
ms.sourcegitcommit: 03e64ead7805f3dfa9149252be8606efe50375df
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2019
ms.locfileid: "27769795"
---
# <a name="office-365-advanced-threat-protection"></a>Proteção Avançada contra Ameaças do Office 365

## <a name="overview"></a>Visão geral

O Office 365 avançadas ameaça proteção (ATP) ajuda a proteger sua organização contra ataques mal-intencionados por:
  
- Anexos de email de verificação de malware com [Anexos de seguros ATP](atp-safe-attachments.md)
    
- Verificação de web endereços (URLs) em mensagens de email e documentos do Office com [Links de seguros ATP](atp-safe-links.md)
    
- Identificando e bloqueando mal-intencionado arquivos em bibliotecas online com [ATP para SharePoint, OneDrive e as equipes da Microsoft](atp-for-spo-odb-and-teams.md)
    
- Verificando mensagens de email para falsificação não autorizado com [falsificação de inteligência de dados](learn-about-spoof-intelligence.md)
    
- Detectando quando alguém tenta representar seus usuários e domínios personalizados de sua organização com [recursos de AntiPhishing ATP no Office 365](atp-anti-phishing.md)
    
**Proteção por meio do Office 365 ATP é determinada pelas políticas que define as equipe de segurança da sua organização para Links de seguros, anexos seguros e antiphishing**. É importante Revise periodicamente e revisar suas políticas para mantê-los atualizados e para realizar as vantagens dos novos recursos que são adicionados ao serviço. 

[Os relatórios estão disponíveis](view-reports-for-atp.md) para mostrar como ATP está trabalhando para sua organização. Esses relatórios também podem mostrar áreas onde você pode precisar revisar e atualizar suas políticas. E, se você tiver arquivos que são marcados como malware que não deveria estar ou arquivos que você gostaria que a Microsoft para examinar, você pode [Enviar um arquivo para a Microsoft para análise](#submit-a-suspicious-file-to-microsoft-for-analysis).

## <a name="new-features-are-continually-being-added-to-atp"></a>Novos recursos são adicionados constantemente a ATP

Podemos está prosseguindo adicionar novos recursos para o Office 365 e que inclui ATP. Abaixo é uma lista de vários recursos novos; alguns deles chamadas por uma política de ATP para serem revisadas e atualizado. Para saber mais sobre os novos recursos, chegando ao ATP (ou Microsoft 365 em geral), visite o [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap?filters=O365).


|Atualizações de recursos  |Itens de ação  |
|---------|---------|
|Iniciando no outubro de 2018 e aplicação nos próximos meses várias, quando pessoas estão usando o Outlook Web Application (OWA) ou o Outlook, Links confiáveis de ATP renderiza URLs originais, não regravado URLs. (Chamamos essa visibilidade link nativo.)|Nenhum         |
|Início em setembro de 2018, o recurso de [páginas de aviso do Office 365 ATP](atp-safe-links-warning-pages.md) um novo esquema de cores, mais detalhes e a capacidade para continuar a um site apesar recebe avisos e recomendações. |Nenhum         |
|Proteção de Links de seguros ATP começando na segunda metade do 2018, é estendida para aplicar a URLs no Office Online (on-line do Word, Excel Online, on-line do PowerPoint e OneNote Online) e Office 365 ProPlus em Mac.   |[Revisar e editar suas políticas de Links de seguros ATP](set-up-atp-safe-links-policies.md)  |
|Iniciando no tardia de 2018 de maio, recursos de [quarentena](quarantine-email-messages.md) na segurança &amp; Centro de conformidade estão sendo estendidas para [ATP para o SharePoint Online, OneDrive for Business e equipes da Microsoft](atp-for-spo-odb-and-teams.md). |[Revisar e editar suas políticas de ATP anexos de seguros](set-up-atp-safe-attachments-policies.md) |
|Iniciando no de 2018 de março, proteção de Links de seguros ATP é estendida para aplicar a emails enviados entre pessoas dentro de uma organização. |[Revisar e editar suas políticas de Links de seguros ATP](set-up-atp-safe-links-policies.md) |
|Proteção de Links de seguros ATP a partir do final de 2017 de outubro, é estendida para aplicar a URLs em email, bem como as URLs em documentos do Office 365 ProPlus, como Word, Excel, PowerPoint e Visio no Windows, bem como Office apps em dispositivos com Android e iOS.  |Verifique se que você estiver usando [Autenticação moderno para Office](https://docs.microsoft.com/office365/enterprise/modern-auth-for-office-2013-and-2016) |

      
## <a name="get-office-365-atp"></a>Obter ATP do Office 365

O Office 365 ATP está incluído no inscrições, como [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 Enterprise E5 e A5 de educação do Office 365. Se sua organização tiver uma assinatura do Office 365 que não inclui ATP do Office 365, você pode adquirir potencialmente ATP como um complemento. Para obter mais informações, consulte [Office 365 avançadas Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description). 

## <a name="define-policies-for-atp"></a>Definir diretivas para ATP

- **[Configurar políticas de AntiPhishing ATP no Office 365](set-up-anti-phishing-policies.md)** incluindo ataques baseados em representação para proteger contra invasores que enviam mensagens de email que parecem ser de pessoas confiáveis ou domínios 

- **[Configurar políticas de Links de ATP seguros no Office 365](set-up-atp-safe-links-policies.md)** , incluindo [lista personalizada de URLs bloqueada](set-up-a-custom-blocked-urls-list-wtih-atp.md) e a [lista de URLs personalizada "Não regravação"](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) da sua organização
    
- **[Configurar políticas de anexos de ATP seguros no Office 365](set-up-atp-safe-attachments-policies.md)** e escolha uma das várias opções, como [entrega dinâmico e visualização](dynamic-delivery-and-previewing.md)
  
## <a name="see-how-atp-is-working-by-viewing-reports"></a>Consulte como ATP está funcionando exibindo relatórios

Depois que suas políticas de ATP estão funcionando, relatórios estão disponíveis para mostrar como o serviço está funcionando.

[![A segurança &amp; painel do Centro de conformidade pode ajudá-lo a ver onde a proteção de ameaça Avançado está funcionando](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)](view-reports-for-atp.md)
  
1. Certifique-se de que você é um administrador global, administrador de segurança ou leitor de segurança do Office 365. (Consulte [Permissions in a segurança do Office 365 &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md).)
    
2. [Exibir relatórios de proteção avançada de ameaça](view-reports-for-atp.md).
    
3. Se necessário, fazer ajustes suas políticas de segurança. Consulte os seguintes recursos:
      - [Políticas de AntiPhishing ATP no Office 365](set-up-anti-phishing-policies.md)
      - [Políticas de Links de ATP seguros no Office 365](set-up-atp-safe-links-policies.md)
      - [Políticas de anexos de ATP seguros no Office 365](set-up-atp-safe-attachments-policies.md)
    
    
## <a name="submit-a-suspicious-file-to-microsoft-for-analysis"></a>Enviar um arquivo suspeito à Microsoft para análise

- Se você receber um arquivo que você supõe que poderia ser malware, você poderá enviar esse arquivo para a Microsoft para análise. Visite o [portal de envio de inteligência de segurança do Windows Defender](https://go.microsoft.com/fwlink/?linkid=857185).

- Se você receber uma mensagem de email (com ou sem um anexo) que deseja usar para enviar à Microsoft para análise, use o [suplemento de mensagem de relatório](enable-the-report-message-add-in.md). 
  


---
title: Proteção Avançada contra Ameaças do Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/08/2019
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e100fe7c-f2a1-4b7d-9e08-622330b83653
ms.collection:
- M365-security-compliance
description: A proteção avançada contra ameaças do Office 365 inclui inteligência de falsificação, links seguros, anexos seguros, recursos avançados de anti-phishing e inteligência de ameaças.
ms.openlocfilehash: d78b37ca048187a298b6e083b54ad68b949638ef
ms.sourcegitcommit: 2af6c3e8a74995294a67429530af8f085e6ca136
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2019
ms.locfileid: "30051172"
---
# <a name="office-365-advanced-threat-protection"></a>Proteção Avançada contra Ameaças do Office 365

## <a name="overview-of-office-365-advanced-threat-protection"></a>Visão geral da proteção avançada contra ameaças do Office 365

> [!IMPORTANT]
> Este artigo destina-se a clientes corporativos. Se você for um usuário doméstico que procura informações sobre links seguros no Outlook, consulte [Advanced Outlook.com Security](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2).

A proteção avançada contra ameaças do Office 365 (ATP) ajuda a proteger sua organização contra ataques mal-intencionados por:
  
- Examinando anexos de email em busca de malware com [anexos seguros de ATP](atp-safe-attachments.md)
    
- Examinar endereços da Web (URLs) em mensagens de email e documentos do Office com [links de segurança ATP](atp-safe-links.md)
    
- Identificando e bloqueando arquivos mal-intencionados em bibliotecas online com [ATP para SharePoint, onedrive e Microsoft Teams](atp-for-spo-odb-and-teams.md)
    
- Verificando mensagens de email para falsificação não autorizada com [inteligência](learn-about-spoof-intelligence.md) de falsificação
    
- Detectar quando alguém tenta representar seus usuários e domínios personalizados da sua organização com recursos de [anti-phishing do ATP no Office 365](atp-anti-phishing.md)
    
**A proteção por meio do Office 365 ATP é determinada pelas políticas que a equipe de segurança da sua organização define para os links seguros, os anexos seguros e o anti-phishing**. É importante definir políticas e revisar periodicamente essas políticas para mantê-las atualizadas e para aproveitar as vantagens dos novos recursos adicionados ao serviço. 

[Relatórios estão disponíveis](view-reports-for-atp.md) para mostrar como a ATP está funcionando para sua organização. Esses relatórios também podem mostrar as áreas em que talvez seja necessário revisar e atualizar suas políticas. E, se você tiver arquivos marcados como malware que não deveriam ser, ou arquivos que você gostaria que a Microsoft examinasse, você pode [enviar um arquivo para a Microsoft para análise](#submit-a-suspicious-file-to-microsoft-for-analysis).

## <a name="new-features-are-continually-being-added-to-atp"></a>Novos recursos estão sempre sendo adicionados à ATP

Continuamos a adicionar novos recursos ao Office 365 e que inclui ATP. Veja a seguir uma lista de vários novos recursos, algumas das quais as chamadas para uma política ATP serão revisadas e atualizadas. Para saber mais sobre os novos recursos vindos à ATP (ou o Microsoft 365 em geral), visite o [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap?filters=O365).


|Atualizações de recursos  |Itens de ação  |
|---------|---------|
|A partir de fevereiro de 2019 e a distribuição dos próximos meses, os recursos de inteligência de ameaças estão sendo adicionados à ATP. Além disso, se sua organização não tiver a ATP no momento, você terá novas opções a considerar, incluindo o plano ATP 1 e o plano ATP 2. Para saber mais, veja [planos e preços avançados de proteção contra ameaças do office 365](https://products.office.com/exchange/advance-threat-protection) e a [Descrição do serviço de proteção avançada contra ameaças do Office 365](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description). |Revise a assinatura da sua organização e, se necessário, [compre ou edite um complemento](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/buy-or-edit-an-add-on).  |
|A partir de outubro de 2018 e saindo dos próximos meses, quando as pessoas estão usando o Outlook ou o Outlook Web Application (OWA), os links seguros de ATP renderizam URLs originais, não reconfiguradas URLs. (Chamamos isso de processamento de link nativo.)<br>Quando o processamento de link nativo estiver disponível para sua organização, esse recurso funcionará no Outlook 365 (clique para executar) e no OWA.|Nenhum         |
|A partir de setembro de 2018, as [páginas de aviso do Office 365 ATP](atp-safe-links-warning-pages.md) apresentam um novo esquema de cores, mais detalhes e a capacidade de continuar em um site apesar de receber avisos e recomendações. |Nenhum         |
|Começando na segunda metade de 2018, a proteção de links de segurança ATP é estendida para aplicar às URLs no Office Online (Word online, Excel online, PowerPoint online e OneNote online) e Office 365 proPlus no Mac.   |[ReVisar e editar suas políticas de links seguros de ATP](set-up-atp-safe-links-policies.md)  |
|A partir do final de maio [](quarantine-email-messages.md) de 2018, os recursos de &amp; quarentena no centro de conformidade de segurança estão sendo estendidos para [ATP para SharePoint Online, onedrive for Business e Microsoft Teams](atp-for-spo-odb-and-teams.md). |[ReVisar e editar suas políticas de anexos seguros de ATP](set-up-atp-safe-attachments-policies.md) |
|A partir de março de 2018, a proteção de links seguros ATP é estendida para ser aplicada ao email enviado entre as pessoas de uma organização. |[ReVisar e editar suas políticas de links seguros de ATP](set-up-atp-safe-links-policies.md) |
|A partir do final de outubro de 2017, a proteção de links seguros de ATP é estendida para ser aplicada às URLs em email, bem como URLs em documentos do Office 365 proPlus, como Word, Excel, PowerPoint e Visio no Windows, bem como aplicativos do Office em dispositivos iOS e Android.  |Verifique se você está usando [a autenticação moderna do Office](https://docs.microsoft.com/office365/enterprise/modern-auth-for-office-2013-and-2016) |

## <a name="get-office-365-atp"></a>Obter o Office 365 ATP

O Office 365 ATP está incluído em inscrições, como [o microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [o Microsoft 365 Business, o](https://www.microsoft.com/microsoft-365/business)Office 365 Enterprise E5 e o Office 365 Education. Se sua organização tiver uma assinatura do Office 365 que não inclua o Office 365 ATP, você poderá comprar ATP como um complemento. Confira mais informações em [planos e preços avançados de proteção contra ameaças do office 365](https://products.office.com/exchange/advance-threat-protection) e a [Descrição do serviço de proteção avançada contra ameaças do Office 365](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description). 

## <a name="define-policies-for-atp"></a>Definir políticas para ATP

Para definir (ou editar) políticas ATP, você deve receber uma das funções descritas na tabela a seguir:

|Função  |Onde/como a atribuição  |
|---------|---------|
|Administrador global do Office 365 |Por padrão, a pessoa que se inscreve para comprar o Office 365 é um administrador global. (ConFira [sobre as funções de administrador do Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) para saber mais.)         |
|Administrador de segurança |Centro de administração do Azure Active[https://aad.portal.azure.com](https://aad.portal.azure.com)Directory ()|
|Gerenciamento da organização do Exchange Online |Centro de administração do[https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)Exchange () <br>ou <br>  Cmdlets do PowerShell (consulte [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)) |

> [!TIP]
> Para saber mais sobre funções e permissões, confira [permissões no centro de conformidade &amp; de segurança do Office 365](permissions-in-the-security-and-compliance-center.md).

Há vários tipos de diretivas ATP para definir e revisar periodicamente.

1. **[Configure as políticas de anti-phishing do ATP no Office 365](set-up-anti-phishing-policies.md)** , incluindo ataques baseados em representação para proteger contra invasores que enviam mensagens de email que parecem ser de pessoas ou domínios confiáveis. 

2. **[Configure as políticas de links seguros de ATP no Office 365](set-up-atp-safe-links-policies.md)** , incluindo a [lista de URLs bloqueadas personalizadas](set-up-a-custom-blocked-urls-list-wtih-atp.md) da sua organização e a [lista de URLs personalizadas "não reconfigurar"](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).
    
3. **[Configure as políticas de anexos seguros de ATP no Office 365](set-up-atp-safe-attachments-policies.md)** e escolha dentre várias opções, como [entrega dinâmica e visualização](dynamic-delivery-and-previewing.md).
  
## <a name="see-how-atp-is-working-by-viewing-reports"></a>Veja como a ATP está funcionando exibindo relatórios

Após suas políticas ATP serem aplicadas, os relatórios estão disponíveis para mostrar como o serviço está funcionando. (no centro de conformidade do & de segurança do Office 365, vá para**painel**de **relatórios** > .)

[![O painel &amp; do centro de conformidade de segurança pode ajudá-lo a ver onde a proteção avançada contra ameaças está funcionando](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)](view-reports-for-atp.md)
  
1. Como um administrador global do Office 365, um administrador de segurança ou um leitor de segurança, [https://protection.office.com](https://protection.office.com) acesse e entre.
    
2. Vá para o**painel**de **relatórios** > . (Para obter ajuda com esses relatórios, confira [exibir relatórios para proteção avançada contra ameaças](view-reports-for-atp.md).)
    
3. Se necessário, faça ajustes em suas políticas de segurança. Para obter ajuda com isso, consulte os seguintes recursos:
    - [Políticas de anti-phishing da ATP](set-up-anti-phishing-policies.md)
    - [Políticas de links seguros de ATP](set-up-atp-safe-links-policies.md)
    - [Políticas de anexos seguros de ATP](set-up-atp-safe-attachments-policies.md)
    
    
## <a name="submit-a-suspicious-file-to-microsoft-for-analysis"></a>Enviar um arquivo suspeito para a Microsoft para análise

- Se você receber um arquivo que você suspeita que pode ser malware, envie esse arquivo para a Microsoft para análise. Visite o [portal de envio de inteligência de segurança do Windows Defender](https://go.microsoft.com/fwlink/?linkid=857185).

- Se você receber uma mensagem de email (com ou sem um anexo) que gostaria de enviar à Microsoft para análise, use o [suplemento de mensagem de relatório](enable-the-report-message-add-in.md). 
  


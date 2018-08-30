---
title: Gerenciamento de Direitos de Informação no Exchange Online
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/13/2017
ms.audience: End User
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 2c956776-0016-4be6-b4cd-133a237f4a9e
description: As pessoas geralmente usam email para trocar informações importantes, como dados financeiros, contratos, informações confidenciais de produtos, relatórios e projeções de vendas, informações sobre a saúde de pacientes ou informações sobre clientes e empregados. Portanto, as caixas de correio podem se tornar repositórios de grandes quantidades de informações potencialmente confidenciais, e o vazamento de informações pode se tornar uma séria ameaça à sua organização.
ms.openlocfilehash: 5036fe359215de1c2674d7efabbb283c78418a19
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002554"
---
# <a name="information-rights-management-in-exchange-online"></a>Gerenciamento de Direitos de Informação no Exchange Online

As pessoas geralmente usam email para trocar informações importantes, como dados financeiros, contratos, informações confidenciais de produtos, relatórios e projeções de vendas, informações sobre a saúde de pacientes ou informações sobre clientes e empregados. Portanto, as caixas de correio podem se tornar repositórios de grandes quantidades de informações potencialmente confidenciais, e o vazamento de informações pode se tornar uma séria ameaça à sua organização.
  
Para ajudar a impedir o vazamento de informações, o Exchange Online inclui funcionalidade de gerenciamento de direitos de informação (IRM) que oferece proteção online e offline de mensagens de email e anexos. Proteção de IRM pode ser aplicada por usuários no Microsoft Outlook ou no Outlook na web e pode ser aplicada por administradores usando regras de proteção de transporte ou regras de proteção do Outlook. O IRM ajuda a você e seu usuários controle quem pode acessar, encaminhar, imprimir ou copiar dados confidenciais em um email.
  
## <a name="changes-to-how-irm-works-with-office-365-message-encryption-ome-and-azure-active-directory"></a>Alterações como o IRM funciona com o Office 365 Message Encryption (OME) e o Azure Active Directory

A partir de 2017 setembro, quando você configurar os novos recursos do Office 365 Message Encryption para sua organização, você também configurar o IRM para uso com o Azure Rights Management (RMS do Windows Azure). Você não é mais definir o IRM com o Azure RMS separadamente. Em vez disso, gerenciamento de direitos e OME trabalhar em conjunto. Para obter mais detalhes sobre os novos recursos, consulte [Perguntas frequentes sobre a criptografia de mensagem do Office 365](https://support.office.com/article/0432dce9-d9b6-4e73-8a13-4a932eb0081e). Se você estiver pronto para começar a usar os novos recursos OME dentro da sua organização, consulte [configurar novos recursos do Office 365 Message Encryption construídos sobre a proteção de informações do Windows Azure](https://support.office.com/article/7ff0c040-b25c-4378-9904-b1b50210d00e).
  
## <a name="how-irm-works-with-exchange-online-and-active-directory-rights-management-services"></a>Como o IRM funciona com o Exchange Online e o Active Directory Rights Management Services

IRM Online do Exchange usa local Active Directory Rights Management Services (AD RMS), uma tecnologia de proteção de informações no Windows Server 2008 e posterior. Proteção de IRM é aplicada ao email, aplicando um modelo de diretiva de direitos do AD RMS para uma mensagem de email. Direitos estão anexados à mensagem em si, para que ocorra de proteção online e offline e dentro e fora do firewall da organização.
  
Os usuários podem aplicar um modelo para uma mensagem de email para controlar as permissões que os destinatários têm em uma mensagem. Ações, como encaminhamento, extrair informações de uma mensagem, salvando uma mensagem ou imprimir uma mensagem podem ser controladas aplicando uma política de direitos do AD RMS à mensagem.
  
Você pode configurar o IRM para usar um servidor AD RMS executando o Windows Server 2008 ou posterior. Você pode usar este servidor AD RMS para gerenciar os modelos de diretiva de direitos do AD RMS para sua organização baseada em nuvem. Outlook também se baseia no servidor AD RMS para permitir aos usuários aplicar proteção IRM a mensagens que enviam. Para obter detalhes, consulte [Configurar o IRM para usar um local servidor AD RMS](configure-irm-to-use-an-on-premises-ad-rms-server.md). 
  
Depois de habilitada, a proteção do IRM pode ser aplicada às mensagens da seguinte maneira:
  
- **Os usuários poderão aplicar manualmente um modelo usando o Outlook e Outlook na web.** Os usuários podem aplicar um modelo de diretiva de direitos do AD RMS para uma mensagem de email, selecionando o modelo do **conjunto de permissões de** lista. Quando os usuários enviam uma mensagem protegida por IRM, quaisquer arquivos anexados que usam um formato com suporte também recebem a mesma proteção de IRM que a mensagem. Proteção de IRM é aplicada a arquivos associados com o Word, Excel e PowerPoint, bem como arquivos. XPS e emails anexado. 
    
- **Administradores podem usar as regras de proteção de transporte para aplicar a proteção IRM automaticamente para o Outlook e Outlook na web.** Você pode criar regras de proteção de transporte para proteger o IRM mensagens. Configure a ação de regra de proteção de transporte para aplicar um modelo de diretiva de direitos do AD RMS para mensagens que atendam a condição de regra. Após habilitar o IRM, modelos de diretiva de direitos do AD RMS da sua organização estão disponíveis para uso com a ação de regra de proteção de transporte chamada **Aplicar proteção de direitos à mensagem com**.
    
- **Os administradores podem criar regras de proteção do Outlook.** Regras de proteção do Outlook aplicam automaticamente a proteção de IRM a mensagens no Outlook 2010 (não Outlook na web) com base em condições de mensagem que incluem o departamento do remetente, o que a mensagem é enviada para, e se os destinatários são interno ou externo sua organização. Para obter detalhes, consulte [criar uma regra de proteção do Outlook](http://technet.microsoft.com/library/da64750d-faaf-44de-ad8c-888eba7fbdbf.aspx).
    


---
title: Anexos seguros de ATP do Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.date: 04/04/2019
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 6e13311e-92ae-495e-a619-56d770199170
ms.collection:
- M365-security-compliance
description: O recurso de anexos seguros oferece verificação de horário de clique de anexos de email. Use anexos seguros para proteger sua organização contra arquivos mal-intencionados enviados ou recebidos por email.
ms.openlocfilehash: 933a533a6deb52a41d1412e319c6fb6840046390
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32250961"
---
# <a name="office-365-atp-safe-attachments"></a>Anexos seguros de ATP do Office 365

## <a name="overview-of-office-365-atp-safe-attachments"></a>Visão geral dos anexos seguros de ATP do Office 365

Os anexos seguros de ATP (juntamente com [links seguros de ATP](atp-safe-links.md)) fazem parte da [proteção avançada contra ameaças](office-365-atp.md) (atp) do Office 365. O recurso de anexos seguros de ATP verifica se os anexos de email são mal-intencionados e, em seguida, executa a ação de proteger sua organização. O recurso de anexos seguros de ATP protege sua organização de acordo com [as políticas de anexos seguros de ATP](set-up-atp-safe-attachments-policies.md) definidas pelo seu Office 365 global ou administradores de segurança. 
  
A proteção ATP também pode ser estendida para arquivos no SharePoint Online, no OneDrive for Business e no Microsoft Teams. Para saber mais, confira [Office 365 Advanced Threat Protection for SharePoint, onedrive e Microsoft Teams](atp-for-spo-odb-and-teams.md).

## <a name="how-it-works"></a>Como funciona

O recurso de anexos seguros de ATP verifica anexos de email de pessoas em sua organização. Quando uma política de anexos seguros de ATP está implementada e alguém abordado por essa política exibe seus emails no Office 365, seus anexos de email são verificados e as ações apropriadas são tomadas, com base nas suas políticas de anexos seguros de ATP. Dependendo de como suas políticas estiverem definidas, as pessoas poderão continuar a trabalhar sem ter sido sabendo que foram enviadas arquivos mal-intencionados.
  
Aqui estão dois exemplos de anexos seguros de ATP no trabalho.
  
- **Exemplo 1: anexo de email** Suponha que Lee receba uma mensagem de email que tenha um anexo. Não é óbvio para Lee se esse anexo é seguro ou realmente contém malware projetado para roubar as credenciais de usuário de Lee. Na organização de Lee, um administrador de segurança definiu uma política de anexos seguros de ATP alguns dias atrás. Com o recurso de anexos seguros de ATP, o anexo de email é aberto e testado em um ambiente virtual antes de ser recebido por Lee. Se o anexo for considerado mal-intencionado, ele será removido automaticamente. Se o anexo for seguro, ele será aberto conforme o esperado quando o Lee clicar nele.

- **Exemplo 2: arquivo no SharePoint Online** Suponha que Jean recebeu um arquivo e o carregou em uma biblioteca no SharePoint Online. Jean compartilha o link para o arquivo com o restante da equipe, não sabendo que o arquivo é realmente mal-intencionado. Felizmente, [a ATP para SharePoint, onedrive e Microsoft Teams](atp-for-spo-odb-and-teams.md) detecta o arquivo mal-intencionado e o bloqueia. Alguns dias depois, Chris vai abrir o documento. Embora Carla possa ver que o arquivo está lá, Carla não pode abrir ou compartilhar, o que impede o computador de Carla e outros do arquivo mal-intencionado.

As políticas de anexos seguros de ATP podem ser aplicadas a pessoas ou grupos específicos em sua organização ou a todo o seu domínio. Além disso, as políticas de anexos seguros de ATP podem ser configuradas para usar anexos de espaço reservado enquanto anexos reais estão sendo verificados. Para saber mais, confira **[configurar as políticas de anexos seguros de ATP no Office 365](set-up-atp-safe-attachments-policies.md)**.

> [!NOTE]
> A verificação de anexos seguros de ATP ocorre na mesma região onde seus dados do Office 365 residem. Para obter mais informações sobre a geografia do Data Center, confira [onde estão seus dados?](https://products.office.com/where-is-your-data-located?geo=All) 

  
## <a name="how-to-get-atp-safe-attachments"></a>Como obter anexos seguros de ATP

Primeiro, certifique-se de que sua assinatura inclua [proteção avançada contra ameaças](office-365-atp.md). A ATP está incluída em inscrições, como [o microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [o Microsoft 365 Business, o](https://www.microsoft.com/microsoft-365/business)Office 365 Enterprise E5, o Office 365 Education a5, etc. Se sua organização tiver uma assinatura do Office 365 que não inclua o Office 365 ATP, você poderá comprar ATP como um complemento. Confira mais informações em [planos e preços avançados de proteção contra ameaças do office 365](https://products.office.com/exchange/advance-threat-protection) e a [Descrição do serviço de proteção avançada contra ameaças do Office 365](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description). 

Em seguida, verifique se as políticas de anexos seguros de ATP estão definidas. (Consulte [Configurar políticas de anexos seguros de ATP do Office 365](set-up-atp-safe-attachments-policies.md)) Os recursos de anexos seguros de ATP estão ativos quando:
  
- As políticas de anexos seguros de ATP estão configuradas. (ConFira [Configurar políticas de anexos seguros de ATP no Office 365](set-up-atp-safe-attachments-policies.md).)

- Os usuários entraram no Office 365 usando sua conta corporativa ou de estudante. (Consulte [entrar no Office ou no office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426).)

Para definir (ou editar) políticas ATP, você deve ter uma função apropriada atribuída. Alguns exemplos são descritos na tabela a seguir:

|Função  |Onde/como a atribuição  |
|---------|---------|
|Administrador global do Office 365 |Por padrão, a pessoa que se inscreve para comprar o Office 365 é um administrador global. (ConFira [sobre as funções de administrador do Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) para saber mais.)         |
|Administrador de segurança |Centro de administração do Azure Active[https://aad.portal.azure.com](https://aad.portal.azure.com)Directory ()|
|Gerenciamento da organização do Exchange Online |Centro de administração do[https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)Exchange () <br>ou <br>  Cmdlets do PowerShell (consulte [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)) |

## <a name="how-to-know-if-atp-safe-attachments-protection-is-in-place"></a>Como saber se a proteção de anexos seguros de ATP está em vigor

Após [definir (ou revisar) suas políticas de anexos seguros de ATP](set-up-atp-safe-attachments-policies.md), uma boa maneira de ver como o serviço está funcionando é [exibindo relatórios para proteção avançada contra ameaças](view-reports-for-atp.md).
  
A tabela a seguir descreve alguns exemplos de cenários. Em todos esses casos, assumimos que a organização tem uma assinatura do Office 365 que inclui proteção avançada contra ameaças.
  
|**Cenário de exemplo**|**A proteção de anexos seguros ATP se aplica nesse caso?**|
|:-----|:-----|
|A organização do Luigi tem o Office 365 Enterprise e5, mas nenhuma política de anexos seguros de ATP ainda foi definida.  <br/> |Não. Embora o recurso esteja disponível, pelo menos uma política de anexos seguros de ATP deve ser definida para que a proteção de anexos seguros de ATP esteja em vigor.  <br/> |
|Lee é um funcionário no departamento de vendas da contoso. A organização de Lee tem uma política de anexos seguros de ATP em vigor que se aplica apenas aos funcionários de finanças.  <br/> |Não. Nesse caso, os funcionários de finanças teriam proteção de anexos seguros de ATP, mas outros funcionários, incluindo o departamento de vendas, não até as políticas que incluem esses grupos são definidas.  <br/> |
|Ontem, um administrador do Office 365 na organização de Jean configurou uma política de anexos seguros de ATP que se aplica a todos os funcionários. Hoje em dia, Jean recebeu uma mensagem de email que inclui um anexo.  <br/> |Sim. Neste exemplo, Jean tem uma licença para proteção avançada contra ameaças e uma política de anexos seguros de ATP que inclui Jean foi definida. Geralmente, leva cerca de 30 minutos para uma nova política entrar em vigor nos data centers; como um dia passou nesse caso, a política deve estar em vigor.  <br/> |
|A organização de Carla tem o Office 365 Enterprise E5 com as políticas de anexos seguros de ATP in-loco para todas as pessoas na organização. Chris recebe um email que tem um anexo e encaminha a mensagem para outras pessoas que estão fora da organização.  <br/> |A proteção de anexos seguros de ATP está em vigor para mensagens que Carla receber. Se as organizações dos destinatários também tiverem diretivas de anexos seguros de ATP em vigor, a mensagem informando que Carla estaria sujeita às políticas quando a mensagem encaminhada chegar.  <br/> |
|A organização de Jaime tem políticas de anexos seguros de ATP no local e [a ATP para SharePoint, onedrive e Microsoft Teams](atp-for-spo-odb-and-teams.md) foi ativada. Jaime supõe que cada arquivo no SharePoint Online foi verificado e é seguro para ser aberto ou baixado.  <br/> |A proteção de anexos seguros de ATP está no local de acordo com as políticas definidas; no entanto, isso não significa que cada arquivo único no SharePoint Online, no OneDrive for Business ou no Microsoft Teams seja verificado. (Para saber mais, confira [ATP para SharePoint, onedrive e Microsoft Teams](atp-for-spo-odb-and-teams.md).)  <br/> |

## <a name="submitting-files-for-malware-analysis"></a>Enviando arquivos para análise de malware

- Se você receber um arquivo que deseja solicitar à Microsoft para analisar, visite [enviar um arquivo para análise de malware](https://aka.ms/wdsi/submit).

- Se você receber uma mensagem de email (com ou sem um anexo) que deseja enviar para a Microsoft para análise, use o [suplemento de mensagem de relatório](enable-the-report-message-add-in.md).

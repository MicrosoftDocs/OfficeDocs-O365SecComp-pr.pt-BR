---
title: O Office 365 ATP Safe anexos
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: 6e13311e-92ae-495e-a619-56d770199170
description: O recurso de anexos seguros fornece verificação de tempo do clique de anexos de email. Uso de anexos seguros para proteger sua organização contra pessoas arquivos mal-intencionados enviar ou receber no email.
ms.openlocfilehash: 44a7aa56db6b19ac948184988c930841fc7ffb89
ms.sourcegitcommit: 099bbfb1d16b251fd5cf18ec6515faaf9a989176
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25454308"
---
# <a name="office-365-atp-safe-attachments"></a>O Office 365 ATP Safe anexos

## <a name="overview-of-office-365-atp-safe-attachments"></a>Visão geral do Office 365 ATP Safe anexos

Anexos de seguros ATP (juntamente com [Links de seguros ATP](atp-safe-links.md)) é parte da [Proteção de ameaça avançadas do Office 365](office-365-atp.md) (ATP). O recurso de anexos de seguros ATP verifica se os anexos de email estão mal-intencionado e, em seguida, executa a ação para proteger sua organização. O recurso de anexos de seguros ATP protege a sua organização de acordo com [anexos de seguros ATP políticas](set-up-atp-safe-attachments-policies.md) definidas por seu Office 365 global ou administradores de segurança. 
  
Recentemente, proteção ATP foi estendida para arquivos no SharePoint Online, o OneDrive for Business e Teams da Microsoft. Para saber mais, consulte [Office 365 avançadas Threat Protection for SharePoint, OneDrive e as equipes da Microsoft](atp-for-spo-odb-and-teams.md).
       
### <a name="how-it-works"></a>Como funciona

O recurso de anexos de seguros ATP verifica os anexos de email de pessoas da sua organização. Quando uma política de anexos de seguros ATP esteja in-loco e alguém coberto por que a política views seus emails no Office 365, seus anexos de email são verificados e ações adequadas são colocadas, com base nas suas políticas de anexos de ATP seguros. Dependendo de como as políticas são definidas, as pessoas podem continuar trabalhando sem saber que foram enviadas arquivos mal-intencionados.
  
Aqui estão dois exemplos de anexos de seguros ATP no trabalho.
  
- **Exemplo 1: anexo de Email** Suponha que Lee recebe uma mensagem de email que contenha um anexo. Não é óbvio para Lee se que o anexo é seguro ou realmente contém malware desenvolvido para roubar credenciais de usuário de Lee. Na organização de Lee, um administrador de segurança definida uma política de anexos de seguros ATP alguns dias. Com o recurso de anexos de seguros ATP, anexo de email é aberto e testado em um ambiente virtual, antes da Lee recebê-la. Se o anexo é determinado mal-intencionado, ela será removida automaticamente. Se o anexo é seguro, ele será aberto como esperado quando Lee clica nele. 
    
- **Exemplo 2: o arquivo no SharePoint Online** Suponha que Jean recebida de um arquivo e carregado-lo em uma biblioteca no SharePoint Online. Jean compartilha o link para o arquivo com o restante da equipe, não sabendo que o arquivo é realmente mal-intencionado. Felizmente, [ATP para SharePoint, OneDrive e as equipes da Microsoft](atp-for-spo-odb-and-teams.md) detecta o arquivo mal-intencionado e bloqueia a ele. Alguns dias mais tarde, Chris vai para abrir o documento. Embora Chris pode ver que o arquivo estiver listada, Chris não podem abrir ou compartilhá-lo, o que impede que o computador de Chris e outros o arquivo mal-intencionado. 
    
Diretivas de anexos de seguros ATP podem ser aplicadas a pessoas específicas ou grupos em sua organização ou para todo o seu domínio. Para saber mais, consulte **[Configurar políticas de anexos de ATP seguros no Office 365](set-up-atp-safe-attachments-policies.md)**. 
  
## <a name="how-to-get-atp-safe-attachments"></a>Como obter ATP anexos de seguros

O recurso de anexos de seguros ATP faz parte do avançada proteção contra ameaças, que está incluído no Microsoft 365 Enterprise, Office 365 Enterprise E5 e Microsoft 365 Business. Se sua organização estiver usando outra assinatura do Office 365 Enterprise, a proteção avançada de ameaça pode ser adquirida como um complemento. (Como um administrador global, no Centro de administração do Office 365, escolha **faturamento** \> **Adicionar assinaturas**.) Para obter mais informações, consulte [Descrição do serviço de plataforma do Office 365: segurança do Office 365 &amp; Centro de conformidade](https://technet.microsoft.com/en-us/library/dn933793.aspx) e [comprar ou editar um complemento para o Office 365 para empresas](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).
  
O recurso de anexos de seguros ATP aplica-se quando:
  
- Configurar políticas de anexos de ATP seguros. (Consulte [Configurar políticas de anexos de ATP seguros no Office 365](set-up-atp-safe-attachments-policies.md)).
    
- Os usuários entrou no Office 365 usando a conta do trabalho ou da escola. (Consulte [entrar no Office ou Office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426)).
    
### <a name="how-to-know-if-atp-safe-attachments-protection-is-in-place"></a>Como saber se a proteção de anexos de seguros ATP é in-loco

 [Anexos de seguros ATP políticas](set-up-atp-safe-attachments-policies.md) devem ser definidas em ordem para proteção de anexos de seguros ATP estar em vigor. 
  
Uma boa maneira de ver como o serviço está funcionando está exibindo [relatórios de proteção avançada de ameaça](view-reports-for-atp.md).
  
Além disso, a tabela a seguir descreve alguns cenários de exemplo. Em todos os casos, assumimos que a organização tiver o Office 365 Enterprise E5, que inclui a proteção avançada de ameaça.
  
|**Cenário de exemplo**|**Proteção de anexos de seguros ATP se aplicam neste caso?**|
|:-----|:-----|
|Organização da PAT tem o Office 365 Enterprise E5, mas ninguém tenha definido quaisquer políticas para anexos de seguros ATP ainda.  <br/> |Não. Embora o recurso esteja disponível, pelo menos uma política de anexos de seguros ATP deve ser definida em ordem para proteção de anexos de seguros ATP estar em vigor.  <br/> |
|Lee é um funcionário no departamento de vendas na Contoso. Organização de Lee possui uma diretiva de anexos de seguros ATP in-loco que se aplica a apenas para funcionários finance.  <br/> |Não. Nesse caso, funcionários finance teria proteção ATP anexos de seguros, mas outros funcionários, inclusive o departamento de vendas, seriam não até que as políticas que incluem esses grupos são definidas.  <br/> |
|Ontem, um administrador do Office 365 na organização de Jean configurar uma política de anexos de seguros ATP que se aplica a todos os funcionários. Anteriormente hoje, Jean recebeu uma mensagem de email que inclui um anexo.  <br/> |Sim. Neste exemplo, Jean tem uma licença para proteção de ameaça avançadas, e uma política de anexos de seguros ATP que inclui Jean tiver sido definida. Normalmente, levará cerca de 30 minutos para uma nova política entrem em vigor em datacenters; desde que um dia passou nesse caso, a política deve estar em vigor.  <br/> |
|Organização de Chris tem o Office 365 Enterprise E5 com políticas de anexos de seguros ATP em vigor para todas as pessoas na organização. Chris receberá um email que tem um anexo e encaminha a mensagem para outras pessoas que estão fora da organização.  <br/> |Proteção de anexos de seguros ATP está em vigor para mensagens que recebe Chris. Se organizações dos destinatários também têm políticas de anexos de seguros ATP in-loco, em seguida, a mensagem de Chris encaminha seria sujeitos a essas diretivas quando chega a mensagem encaminhada.  <br/> |
|Organização de Júlio tem políticas de anexos de seguros ATP in-loco e [ATP para SharePoint, OneDrive e as equipes da Microsoft](atp-for-spo-odb-and-teams.md) tiver sido ativada. Jaime pressupõe que todos os arquivos no SharePoint Online tem sido verificado e é seguro abrir ou baixar.<br/> |Proteção de anexos de seguros ATP está no lugar de acordo com as políticas que são definidos; No entanto, isso significa que cada arquivo no SharePoint Online, o OneDrive for Business ou Microsoft Teams sejam verificado. (Para saber mais, consulte [ATP para SharePoint, OneDrive e as equipes da Microsoft](atp-for-spo-odb-and-teams.md)).<br/> |
   
## <a name="submitting-files-for-malware-analysis"></a>Como enviar arquivos para análise de malware

- Se você receber um arquivo que você deseja pedir analisar a Microsoft, visite o [envio de um arquivo para análise de malware](https://aka.ms/wdsi/submit).

- Se você receber uma mensagem de email (com ou sem um anexo) que você deseja enviar à Microsoft para análise, use o [suplemento de mensagem de relatório](enable-the-report-message-add-in.md).
  
## <a name="related-topics"></a>Tópicos relacionados

[Proteção Avançada contra Ameaças do Office 365](office-365-atp.md) 
  
[Configurar políticas de anexos de ATP seguros no Office 365](set-up-atp-safe-attachments-policies.md)
  
[ATP para SharePoint, OneDrive e equipes da Microsoft](atp-for-spo-odb-and-teams.md)
  
[Links de ATP seguros no Office 365](atp-safe-links.md)
  
[Recursos antiphishing ATP no Office 365](atp-anti-phishing.md)
  
[Exibir relatórios de Proteção avançada contra ameaças](view-reports-for-atp.md)
  


---
title: Configurar políticas de anexos do Office 365 ATP seguros
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.date: 02/05/2019
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 078eb946-819a-4e13-8673-fe0c0ad3a775
description: Defina políticas de anexos seguros para proteger sua organização contra arquivos maliciosos no email.
ms.openlocfilehash: 229f5eb4ec1af4302f724151f599bd33b15055e1
ms.sourcegitcommit: a64af0ebd0b03e4a5e60a33e9108c44c7d74f356
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2019
ms.locfileid: "29741114"
---
# <a name="set-up-office-365-atp-safe-attachments-policies"></a>Configurar políticas de anexos do Office 365 ATP seguros

Pessoas regularmente enviar, receber e compartilhe anexos, como documentos, apresentações, planilhas e muito mais. Não sempre é fácil saber se um anexo é seguro ou mal intencionado apenas olhando uma mensagem de email. E a última coisa que você deseja é um anexo mal-intencionado de atravessar, causando muitos problemas para sua organização. Felizmente, pode ajudar a [Proteção de ameaça avançadas do Office 365](office-365-atp.md) (ATP). Você pode configurar políticas de [Anexos seguros de ATP](atp-safe-attachments.md) para ajudar a garantir que a sua organização está protegida contra ataques por anexos de email não seguros. 
  
## <a name="what-to-do"></a>O que fazer 
  
1. [Revise os pré-requisitos](#review-the-prerequisites)
    
2. [Configurar uma política de anexos de seguros ATP](#set-up-an-atp-safe-attachments-policy)
    
3. [Saiba mais sobre as opções de política de anexos de seguros ATP](#learn-about-atp-safe-attachments-policy-options)
    
## <a name="step-1-review-the-prerequisites"></a>Etapa 1: Revisar os pré-requisitos

- Certifique-se de que sua organização tenha [A proteção de ameaça avançadas do Office 365](office-365-atp.md).
    
- Verifique se você tem as permissões necessárias. Para definir (ou editar) políticas ATP, você deve ter uma das funções descritas na tabela a seguir: <br>

    |Função  |Onde/como atribuído  |
    |---------|---------|
    |Administrador Global do Office 365 |A pessoa que se inscreve para comprar o Office 365 é um administrador global por padrão. (Consulte [funções de administrador do Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) para saber mais).         |
    |Administrador de segurança do Office 365 |Centro de administração ([https://aka.ms/admincenter](https://aka.ms/admincenter))|
    |Gerenciamento de organização Online do Exchange |Centro de administração do Exchange ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) <br>ou <br>  Cmdlets do PowerShell (consulte [PowerShell do Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)) |
    
- [Saiba mais sobre as opções de política de anexos de seguros ATP](#learn-about-atp-safe-attachments-policy-options) (neste artigo). Algumas opções, como as opções de Monitor ou substituir, podem resultar em um atraso secundário de email, enquanto os anexos são examinados. Para evitar atrasos de mensagem, considere o uso [dinâmico de entrega e de visualização](dynamic-delivery-and-previewing.md).
    
- Permitir até 30 minutos para sua política novo ou atualizado à difusão em todos os centros de dados do Office 365.
    
## <a name="step-2-set-up-or-edit-an-atp-safe-attachments-policy"></a>Etapa 2: Configurar uma política de anexos de seguros ATP (ou editar uma)
  
1. Vá para [https://protection.office.com](https://protection.office.com) e entre com sua conta do trabalho ou da escola. 
    
2. No Office 365 Security &amp; Centro de conformidade, no painel de navegação à esquerda, em **gerenciamento de ameaça**, escolha **política** \> **Anexos seguros**.
    
3. Se você vir **ativem ATP para SharePoint, OneDrive e as equipes da Microsoft**, recomendamos que você selecionar essa opção. Isso habilitará o [Office 365 avançada proteção contra ameaças para SharePoint, OneDrive e as equipes da Microsoft](atp-for-spo-odb-and-teams.md) para o seu ambiente do Office 365. 
    
4. Escolha **novo** (botão novo se parece com um sinal de adição ( **+**)) para começar a criar sua política.
    
5. Especifique o nome, descrição e configurações para a política.<br/><br/>**Exemplo:** Para configurar uma política denominada "sem atrasos", o que fornece mensagens de todos os participantes imediatamente e, em seguida, anexa novamente anexos depois que eles são verificados, você pode especificar as configurações a seguir: 
    
      - Na caixa **nome** , digite sem atrasos.
    
      - Na caixa **Descrição** , digite uma descrição like, oferece mensagens imediatamente e anexos anexa novamente após a verificação.
    
      - Na seção de resposta, escolha a opção de **Entrega dinâmico** . ([Saiba mais sobre a entrega dinâmica e visualização de anexos de seguros ATP](dynamic-delivery-and-previewing.md)).
    
      - Na seção **Redirecionar anexo** , selecione a opção para habilitar o redirecionamento e digite o endereço de email do administrador global, administrador de segurança ou analista de segurança que será investigar anexos mal-intencionado seu Office 365. 
    
      - Na seção **Aplicada** , escolha **o domínio do destinatário é**e, em seguida, selecione seu domínio. Escolha **Adicionar**e escolha **Okey**.
    
6. Escolha **Salvar**.
    
Considere configurar várias políticas de anexos seguros de ATP para sua organização. Essas diretivas serão aplicadas na ordem em que são listados na página **ATP anexos de seguros** . Depois que uma política foi definida ou editada, permitir que pelo menos 30 minutos para as políticas entrem em vigor em toda a data centers da Microsoft. 
  
## <a name="step-3-learn-about-atp-safe-attachments-policy-options"></a>Etapa 3: Aprenda sobre as opções de política de anexos de seguros ATP

Como configurar suas políticas de anexos de seguros ATP, você escolher entre várias opções, incluindo o Monitor, bloquear, substituir, entrega dinâmico e assim por diante. Caso você esteja se perguntando sobre o que fazer essas opções, a tabela a seguir resume cada e seu efeito.
  
|**Opção**|**Efeito**|**Uso quando você deseja:**|
|:-----|:-----|:-----|
|**Desligado** <br/> |Não examina anexos de malware  <br/> Não atrasar a entrega da mensagem  <br/> |Desativar a verificação para remetentes internos, scanners, faxes ou hosts inteligentes que somente enviará conhecidos, boa anexos  <br/> Evitar atrasos desnecessários no roteamento de email interno  <br/> **Essa opção não é recomendada para a maioria dos usuários. Permite que você desative a verificação de anexos seguros de ATP para um pequeno grupo de remetentes internos.**           |
|**Monitorar** <br/> |Entrega de mensagens com anexos e, em seguida, controla o que acontece com malware detectado  <br/> |Consulte onde malware detectado vai em sua organização  <br/> |
|**Bloquear** <br/> |Impede que as mensagens com anexos de malware detectado do prosseguir  <br/> Envia mensagens com malware detectado para [quarentena no Office 365](manage-quarantined-messages-and-files.md) onde um administrador de segurança ou analista pode revisar e liberar (ou excluir) essas mensagens  <br/> Bloqueia as mensagens futuras e anexos automaticamente  <br/> |Proteger sua organização contra ataques repetidas usando os mesmo anexos de malware  <br/> |
|**Substituir** <br/> |Remove detectado malware de anexos  <br/> Notifica os destinatários que anexos foram removidos  <br/> Envia mensagens com malware detectado para [quarentena no Office 365](manage-quarantined-messages-and-files.md) onde um administrador de segurança ou analista pode revisar e liberar (ou excluir) essas mensagens  <br/> |Aumentar a visibilidade para destinatários que anexos foram removidos por causa de malware detectado  <br/> |
|**Entrega dinâmica** <br/> |Entrega de mensagens imediatamente  <br/> Substitui os anexos com um arquivo de espaço reservado até que o exame seja concluída e, em seguida, anexa novamente os anexos, se nenhum malware é detectado  <br/> Inclui o anexo a visualização de recursos para a maioria dos PDFs e Office arquivos durante a verificação  <br/> Envia mensagens com malware detectado para quarentena onde um administrador de segurança ou analista pode revisar e liberar (ou excluir) essas mensagens  <br/> [Saiba mais sobre entrega dinâmico e visualização de anexos de seguros ATP](dynamic-delivery-and-previewing.md) <br/> |Evitar atrasos de mensagem, protegendo a destinatários contra arquivos maliciosos  <br/> Permitir que os destinatários visualizar anexos no modo de segurança, enquanto a verificação estiver ocorrendo  <br/> |
|**Habilitar o redirecionamento** <br/> |Aplica-se quando a opção de Monitor, bloquear ou substituir for escolhida  <br/> Envia anexos para um endereço de email especificado onde os administradores de segurança ou os analistas podem investigar  <br/> |Permitir que os administradores de segurança e os analistas anexos suspeitos de pesquisas  <br/> |
   
## <a name="next-steps"></a>Próximas etapas

Depois que suas políticas de anexos de seguros ATP estão funcionando, você pode ver como ATP está trabalhando para sua organização exibindo relatórios. Consulte os seguintes recursos para saber mais:
- [Exibir relatórios de proteção de ameaça avançadas do Office 365](view-reports-for-atp.md)
- [Use o Explorer na segurança &amp; Centro de conformidade](use-explorer-in-security-and-compliance.md)

Mantenha-se na parte superior de novos recursos, chegando ao ATP. visite o [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap?filters=O365) e Aprenda sobre [novos recursos que estão sendo adicionados para ATP](office-365-atp.md#new-features-are-continually-being-added-to-atp).
 
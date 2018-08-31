---
title: Configurar políticas de anexos do Office 365 ATP seguros
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 5/8/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 078eb946-819a-4e13-8673-fe0c0ad3a775
description: Defina políticas de anexos seguros para proteger sua organização contra arquivos maliciosos no email.
ms.openlocfilehash: 03fb0b62d37dc628241a1108b4b256290c23509b
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523963"
---
# <a name="set-up-office-365-atp-safe-attachments-policies"></a>Configurar políticas de anexos do Office 365 ATP seguros

Pessoas regularmente enviar, receber e compartilhe anexos, como documentos, apresentações, planilhas e muito mais. Não sempre é fácil saber se um anexo é seguro ou mal intencionado apenas olhando uma mensagem de email. E a última coisa que você deseja é um anexo mal-intencionado de atravessar, causando muitos problemas para sua organização. Felizmente, pode ajudar a [Proteção de ameaça avançadas do Office 365](office-365-atp.md) (ATP). Você pode configurar políticas de [Anexos seguros de ATP](atp-safe-attachments.md) para ajudar a garantir que a sua organização está protegida contra ataques por anexos de email não seguros. 
  
## <a name="what-to-do"></a>O que fazer 
  
1. [Revise os pré-requisitos](#review-the-prerequisites)
    
2. [Configurar uma política de anexos de seguros ATP](#set-up-an-atp-safe-attachments-policy)
    
3. [Saiba mais sobre as opções de política de anexos de seguros ATP](#learn-about-atp-safe-attachments-policy-options)
    
## <a name="review-the-prerequisites"></a>Revise os pré-requisitos

- Certifique-se de que sua organização tenha [A proteção de ameaça avançadas do Office 365](office-365-atp.md).
    
- Certifique-se de que você tenha o necessário [permissões atribuídas no Office 365 Security &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md).
    
- [Saiba mais sobre as opções de política de anexos de seguros ATP](#learn-about-atp-safe-attachments-policy-options) (neste artigo). Algumas opções, como as opções de Monitor ou substituir, podem resultar em um atraso secundário de email, enquanto os anexos são examinados. Para evitar atrasos de mensagem, considere o uso de [entrega dinâmica e visualização](dynamic-delivery-and-previewing.md).
    
- Permitir até 30 minutos para sua política novo ou atualizado à difusão em todos os centros de dados do Office 365.
    
## <a name="set-up-an-atp-safe-attachments-policy"></a>Configurar uma política de anexos de seguros ATP

Você pode configurar uma política de anexos de seguros ATP usando a segurança do Office 365 &amp; Centro de conformidade ou centro de administração do Exchange (EAC). **é recomendável usar a segurança do Office 365 &amp; Centro de conformidade**. 
  
1. Como administrador global ou administrador de segurança, vá para [https://protection.office.com](https://protection.office.com) e entre com sua conta do trabalho ou da escola. 
    
2. No Office 365 Security &amp; Centro de conformidade, no painel de navegação à esquerda, em **gerenciamento de ameaça**, escolha **política** \> **Anexos seguros**.
    
3. Se você vir **ativem ATP para SharePoint, OneDrive e as equipes da Microsoft**, recomendamos que você selecionar essa opção. Isso habilitará o [Office 365 avançada proteção contra ameaças para SharePoint, OneDrive e as equipes da Microsoft](atp-for-spo-odb-and-teams.md) para o seu ambiente do Office 365. 
    
4. Escolha **novo** (botão novo se parece com um sinal de adição ( **+**)) para começar a criar sua política.
    
5. Especifique o nome, descrição e configurações para a política.
    
    **Exemplo:** Para configurar uma política denominada "sem atrasos", o que fornece mensagens de todos os participantes imediatamente e, em seguida, anexa novamente anexos depois que eles são verificados, você pode especificar as configurações a seguir: 
    
  - Na caixa **nome** , digite sem atrasos.
    
  - Na caixa **Descrição** , digite uma descrição like, oferece mensagens imediatamente e anexos anexa novamente após a verificação.
    
  - Na seção de resposta, escolha a opção de **Entrega dinâmico** . ([Saiba mais sobre entrega dinâmica e visualização de anexos de seguros ATP](dynamic-delivery-and-previewing.md)).
    
  - Na seção **Redirecionar anexo** , selecione a opção para habilitar o redirecionamento e digite o endereço de email do administrador global, administrador de segurança ou analista de segurança que será investigar anexos mal-intencionado seu Office 365. 
    
  - Na seção **Aplicada** , escolha **o domínio do destinatário é**e, em seguida, selecione seu domínio. Escolha **Adicionar**e escolha **Okey**.
    
6. Escolha **Salvar**.
    
Considere configurar várias políticas de anexos seguros de ATP para sua organização. Essas diretivas serão aplicadas na ordem em que são listados na página **ATP anexos de seguros** . Depois que uma política foi definida ou editada, permitir que pelo menos 30 minutos para as políticas entrem em vigor em toda a data centers da Microsoft. 
  
## <a name="learn-about-atp-safe-attachments-policy-options"></a>Saiba mais sobre as opções de política de anexos de seguros ATP

Como configurar suas políticas de anexos de seguros ATP, você escolher entre várias opções, incluindo o Monitor, bloquear, substituir, entrega dinâmico e assim por diante. Caso você esteja se perguntando sobre o que fazer essas opções, a tabela a seguir resume cada e seu efeito.
  
|**Opção**|**Efeito**|**Uso quando você deseja:**|
|:-----|:-----|:-----|
|**Desligado** <br/> |Não examina anexos de malware  <br/> Não atrasar a entrega da mensagem  <br/> |Desativar a verificação para remetentes internos, scanners, faxes ou hosts inteligentes que somente enviará conhecidos, boa anexos  <br/> Evitar atrasos desnecessários no roteamento de email interno  <br/> > [!IMPORTANT]> Essa opção não é recomendada para a maioria dos usuários. Permite que você desative a verificação de anexos seguros de ATP para um pequeno grupo de remetentes internos.           |
|**Monitorar** <br/> |Entrega de mensagens com anexos e, em seguida, controla o que acontece com malware detectado  <br/> |Consulte onde malware detectado vai em sua organização  <br/> |
|**Bloquear** <br/> |Impede que as mensagens com anexos de malware detectado do prosseguir  <br/> Envia mensagens com malware detectado para [quarentena no Office 365](manage-quarantined-messages-and-files.md) onde um administrador de segurança ou analista pode revisar e liberar (ou excluir) essas mensagens  <br/> Bloqueia as mensagens futuras e anexos automaticamente  <br/> |Proteger sua organização contra ataques repetidas usando os mesmo anexos de malware  <br/> |
|**Substituir** <br/> |Remove detectado malware de anexos  <br/> Notifica os destinatários que anexos foram removidos  <br/> Envia mensagens com malware detectado para [quarentena no Office 365](manage-quarantined-messages-and-files.md) onde um administrador de segurança ou analista pode revisar e liberar (ou excluir) essas mensagens  <br/> |Aumentar a visibilidade para destinatários que anexos foram removidos por causa de malware detectado  <br/> |
|**Entrega dinâmica** <br/> |Entrega de mensagens imediatamente  <br/> Substitui os anexos com um arquivo de espaço reservado até que o exame seja concluída e, em seguida, anexa novamente os anexos, se nenhum malware é detectado  <br/> Inclui o anexo a visualização de recursos para a maioria dos PDFs e Office arquivos durante a verificação  <br/> Envia mensagens com malware detectado para quarentena onde um administrador de segurança ou analista pode revisar e liberar (ou excluir) essas mensagens  <br/> [Saiba mais sobre entrega dinâmica e visualização de anexos de seguros ATP](dynamic-delivery-and-previewing.md) <br/> |Evitar atrasos de mensagem, protegendo a destinatários contra arquivos maliciosos  <br/> Permitir que os destinatários visualizar anexos no modo de segurança, enquanto a verificação estiver ocorrendo  <br/> |
|**Habilitar o redirecionamento** <br/> |Aplica-se quando a opção de Monitor, bloquear ou substituir for escolhida  <br/> Envia anexos para um endereço de email especificado onde os administradores de segurança ou os analistas podem investigar  <br/> |Permitir que os administradores de segurança e os analistas anexos suspeitos de pesquisas  <br/> |
   
## <a name="related-topics"></a>Tópicos relacionados

[Proteção Avançada contra Ameaças do Office 365](office-365-atp.md) 
  
[Anexos de ATP seguros no Office 365](atp-safe-attachments.md)
  
[Links de ATP seguros no Office 365](atp-safe-links.md)
  
[Configurar políticas de Links de ATP seguros no Office 365](set-up-atp-safe-links-policies.md)
  
[Exibir relatórios de Proteção avançada contra ameaças](view-reports-for-atp.md)

[Permissões de segurança do Office 365 &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md)
  

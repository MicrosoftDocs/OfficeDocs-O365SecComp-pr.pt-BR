---
title: Como funcionam os anexos seguros de ATP do Office 365
ms.author: deniseb
author: denisebmsft
manager: dansimp
audience: Admin
ms.date: 05/17/2019
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
description: O recurso de anexos seguros oferece verificação de horário de clique de anexos de email. Use anexos seguros para proteger sua organização contra arquivos mal-intencionados enviados ou recebidos por email.
ms.openlocfilehash: f0f117388957a14e3765b963a0e390ffb8fd7943
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35599163"
---
# <a name="how-ffice-365-atp-safe-attachments-works"></a>Como funciona o Office 365 ATP Safe Attachments

## <a name="how-it-works"></a>Como funciona

O recurso de anexos seguros de ATP verifica anexos de email de pessoas em sua organização. Quando uma política de anexos seguros de ATP está implementada e alguém abordado por essa política exibe seus emails no Office 365, seus anexos de email são verificados e as ações apropriadas são tomadas, com base nas suas políticas de anexos seguros de ATP. Dependendo de como suas políticas estiverem definidas, as pessoas poderão continuar a trabalhar sem ter sido sabendo que foram enviadas arquivos mal-intencionados.
  
Aqui estão dois exemplos de anexos seguros de ATP no trabalho.
  
- **Exemplo 1: anexo de email** Suponha que Lee receba uma mensagem de email que tenha um anexo. Não é óbvio para Lee se esse anexo é seguro ou realmente contém malware projetado para roubar as credenciais de usuário de Lee. Na organização de Lee, um administrador de segurança definiu uma política de anexos seguros de ATP alguns dias atrás. Com o recurso de anexos seguros de ATP, o anexo de email é aberto e testado em um ambiente virtual antes de ser recebido por Lee. Se o anexo for considerado mal-intencionado, ele será removido automaticamente. Se o anexo for seguro, ele será aberto conforme o esperado quando o Lee clicar nele.

- **Exemplo 2: arquivo no SharePoint Online** Suponha que Jean recebeu um arquivo e o carregou em uma biblioteca no SharePoint Online. Jean compartilha o link para o arquivo com o restante da equipe, não sabendo que o arquivo é realmente mal-intencionado. Felizmente, [a ATP para SharePoint, onedrive e Microsoft Teams](atp-for-spo-odb-and-teams.md) detecta o arquivo mal-intencionado e o bloqueia. Alguns dias depois, Chris vai abrir o documento. Embora Carla possa ver que o arquivo está lá, Carla não pode abrir ou compartilhar, o que protege o computador de Carla e outros do arquivo mal-intencionado.

As políticas de anexos seguros de ATP podem ser aplicadas a pessoas ou grupos específicos em sua organização ou a todo o seu domínio. Além disso, as políticas de anexos seguros de ATP podem ser configuradas para usar anexos de espaço reservado enquanto anexos reais estão sendo verificados. Para saber mais, confira **[configurar as políticas de anexos seguros de ATP no Office 365](set-up-atp-safe-attachments-policies.md)**.

> [!NOTE]
> A verificação de anexos seguros de ATP ocorre na mesma região onde seus dados do Office 365 residem. Para obter mais informações sobre a geografia do Data Center, confira [onde estão seus dados?](https://products.office.com/where-is-your-data-located?geo=All) 


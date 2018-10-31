---
title: Entrega dinâmica e visualização de anexos do Office 365 ATP seguros
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 10/30/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: f16c9928-8e3d-4219-b994-271dc9a16272
description: Ao configurar suas políticas de anexos seguros ATP, escolha entrega dinâmica para evitar atrasos de mensagem e permitem que as pessoas visualizem anexos que estão sendo examinados.
ms.openlocfilehash: b7b5f05170e6f27cbec9e0d5a121b2f71f16f41a
ms.sourcegitcommit: cda46434094bc2837dba90256d044ba77552df12
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/30/2018
ms.locfileid: "25850815"
---
# <a name="dynamic-delivery-and-previewing-with-office-365-atp-safe-attachments"></a>Entrega dinâmica e visualização de anexos do Office 365 ATP seguros

**Resumo**: entrega dinâmica é uma opção que pode ser selecionada para [ATP anexos de seguros](atp-safe-attachments.md). Leia este artigo para saber mais sobre a entrega dinâmicos e recursos de visualização de anexo no [ATP anexos de seguros no Office 365](atp-safe-attachments.md).
  
## <a name="how-dynamic-delivery-works"></a>Como funciona a entrega dinâmico

Quando [as políticas de anexos de seguros ATP são configuradas](set-up-atp-safe-attachments-policies.md) para sua organização, há várias opções para como anexos de email são manipulados. Isso inclui **Bloquear**, **Substitua**e **Entrega dinâmico**. Dependendo de como as políticas de anexos de seguros ATP são configuradas, os destinatários de email podem levar algum secundária na entrega de email enquanto seus anexos são verificados. Para evitar atrasos de mensagem, escolha **Entrega dinâmico**.
  
Entrega dinâmica elimina atrasos de email, enviando o corpo de uma mensagem de email por meio para o destinatário com um espaço reservado para cada anexo de email. O espaço reservado permanece até que uma cópia do anexo é examinada e determinada seguros pela [ATP anexos de seguros](atp-safe-attachments.md). A maioria dos PDFs e Office documentos podem ser visualizados no modo de segurança, enquanto a verificação ATP está em andamento. Se um anexo não é compatível com o Visualizador de entrega dinâmico, os destinatários de email Consulte um espaço reservado de anexo até que a verificação de anexos de seguros ATP seja concluída.

- Como cada anexo estiver desmarcado, ele está disponível para abrir ou baixar. 

- Se um anexo é determinado mal-intencionado, ela será enviada para quarentena, onde uma pessoa na equipe de segurança da sua organização (por exemplo, um administrador global do Office 365 ou segurança) pode [Gerenciar mensagens em quarentena no Office 365](manage-quarantined-messages-and-files.md).

Com o fornecimento dinâmico, os destinatários do email podem ler e responder às suas mensagens de email imediatamente, sabendo que seus anexos estão sendo analisados. 

Anexos de seguros ATP verificação leva coloque na mesma região onde estão seus dados do Office 365. Para obter mais informações sobre Geografia do Centro de dados, consulte [onde estão seus dados localizados?](https://products.office.com/where-is-your-data-located?geo=All) 
  
## <a name="what-happens-when-someone-forwards-an-email-that-contains-an-attachment"></a>O que acontece quando alguém encaminha um email que contenha um anexo?

Suponha que uma organização está usando dinâmico de entrega para a sua [política de anexos de ATP seguros](set-up-atp-safe-attachments-policies.md)e alguém recebe um email que contenha um anexo. Agora suponha que a pessoa está prestes a encaminhar a mensagem de email para outra pessoa. O que acontece? Isso depende se os destinatários adicionais são incluídos nas políticas de anexos de ATP seguros.
  
- Se um destinatário é coberto por uma política de anexos de seguros ATP usando a opção de entrega dinâmico, o receptor vê espaço reservado, com a capacidade de visualizar arquivos compatíveis.
    
- Se um destinatário não é abordado por uma política de anexos de seguros ATP, então a email e o anexo irão através de, sem anexos de seguros ATP verificação ou espaços reservados de anexo.
    
## <a name="whats-required-for-dynamic-delivery-to-work"></a>O que é necessário para entrega dinâmica funcionar?

- Sua organização deve ter [A proteção de ameaça avançadas do Office 365](office-365-atp.md)
    
- As políticas devem ser definidas para anexos seguros ATP, usando a opção de entrega dinâmico (consulte [Set up políticas ATP anexos de seguros no Office 365](set-up-atp-safe-attachments-policies.md))
    
- Email da sua organização deve ser hospedado no Office 365
    
## <a name="are-there-scenarios-for-which-dynamic-delivery-is-not-available"></a>Existem cenários entrega dinâmica para o qual não está disponível?

Há determinadas situações em que a entrega dinâmica não é suportada. Isso inclui o seguinte:
  
- Mensagens de email que estão em pastas públicas
    
- Mensagens de email que são roteadas de ausência temporária e, em seguida, que voltou ao caixa de correio do usuário usando regras personalizadas
    
- Mensagens que são movidas (automática ou manualmente) fora da caixa de correio hospedada e em outros locais, incluindo pastas de arquivo morto
    
- Mensagens que são excluídas
    
- Pasta de pesquisa de caixa de correio de um usuário que está em um estado de erro
    
- Ambientes em que um administrador do Exchange Online tiver habilitado Exclaimer. (Consulte [mensagens com anexos não são entregues quando são usados ATP dinâmicos de entrega e Exclaimer](https://support.microsoft.com/help/4014438/messages-with-attachments-are-not-delivered-when-atp-dynamic-delivery))

- Mensagens criptografadas com o Secure/Multipurpose Internet Mail Extensions ([S/MIME](s-mime-for-message-signing-and-encryption.md))
    
## <a name="related-topics"></a>Tópicos relacionados

[Proteção Avançada contra Ameaças do Office 365](office-365-atp.md) 
  
[Anexos de ATP seguros no Office 365](atp-safe-attachments.md)
  
[Configurar políticas de anexos de ATP seguros no Office 365](set-up-atp-safe-attachments-policies.md)
  
[Links de ATP seguros no Office 365](atp-safe-links.md)

[Permissões de segurança do Office 365 &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md)
  


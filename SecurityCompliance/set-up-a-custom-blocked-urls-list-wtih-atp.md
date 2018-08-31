---
title: Configurar uma lista de URLs bloqueada personalizada usando o Office 365 ATP seguros Links
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 5/30/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 896a7efb-1683-465e-a394-261349e5d866
description: Leia este artigo para saber como configurar uma lista das URLs bloqueados para sua organização usando a proteção de ameaça avançadas do Office 365. As URLs bloqueadas serão aplicados a mensagens de email e documentos do Office de acordo com suas políticas de links seguros ATP.
ms.openlocfilehash: cd1e7858c8929bf468b2a4d5e09ccde9d5adc7b1
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524099"
---
# <a name="set-up-a-custom-blocked-urls-list-using-office-365-atp-safe-links"></a>Configurar uma lista de URLs bloqueada personalizada usando o Office 365 ATP seguros Links

Com [A proteção de ameaça avançadas do Office 365](office-365-atp.md) (ATP), sua organização pode ter uma lista personalizada de endereços de site (URLs) que são bloqueados. Quando uma URL for bloqueada, as pessoas que clique nos links para a URL bloqueada são seguidas para uma [página de aviso](atp-safe-links-warning-pages.md) semelhante à seguinte imagem: 
  
![Este site está bloqueado](media/6b4bda2d-a1e6-419e-8b10-588e83c3af3f.png)
  
A lista de URLs bloqueada é definida pela equipe de segurança do Office 365 da sua organização e essa lista se aplica a todas as pessoas da organização que é coberto por políticas de vínculos do Office 365 ATP seguros. 
  
Leia este artigo para saber como configurar personalizada lista de URLs bloqueios da sua organização para [Links de ATP seguros no Office 365](atp-safe-links.md).
  
## <a name="view-or-edit-a-custom-list-of-blocked-urls"></a>Exibir ou editar uma lista personalizada de URLs bloqueados

[Links de ATP seguros no Office 365](atp-safe-links.md) usa várias listas, incluindo personalizado bloqueada lista de URLs da sua organização. Se você tiver as permissões necessárias, você pode configurar a lista personalizada de sua organização. Você pode fazer isso editando a política de seguros Links padrão da sua organização.
  
1. Vá para [https://protection.office.com](https://protection.office.com) e entre com sua conta do trabalho ou da escola. 
    
2. No painel de navegação esquerdo, em **gerenciamento de ameaça**, escolha **política** \> **Links seguros**.
    
3. Na seção **políticas que se aplicam a toda a organização** , selecione **padrão**e, em seguida, escolha **Editar** (no botão Editar se parece com um lápis). 
    
    ![Clique em Editar para editar sua política padrão para a proteção de Links de seguros](media/d08f9615-d947-4033-813a-d310ec2c8cca.png)
  
    Isso é onde você vai para exibir sua lista de URLs bloqueados. Observe que, inicialmente, você não terá nenhum URL listado.
    
    ![A lista de URLs bloqueado é no padrão política de seguros Links que se aplica a toda sua organização.](media/575e1449-6191-40ac-b626-030a2fd3fb11.png)
  
4. Selecione caixa **Digite uma URL válida** e, em seguida, digite uma URL e clique no sinal de adição (+). Aqui estão algumas coisas em mente: 
    
  - Você pode especificar uma URL de domínio somente (como `contoso.com` ou `tailspintoys.com`). Isso irá bloquear cliques em qualquer URL que contém o domínio.
    
  - Não inclua uma barra invertida ( **/**) no final da URL. Por exemplo, em vez de inserir `http://www.contoso.com/`, insira `http://www.contoso.com`.
    
  - Você pode incluir até três asteriscos de caractere curinga (\*) por URL. A tabela a seguir lista alguns exemplos de como você pode inserir e o que essas entradas de efeito tem.
    
|**Entrada de exemplo**|**O que ele faz**|
|:-----|:-----|
|`contoso.com`ou`\*contoso.com\*`  <br/> |Bloqueia o domínio, subdomínios e caminhos, tais como `https://www.contoso.com`, `http://sub.contoso.com`, e`http://contoso.com/abc`  <br/> |
|`http://contoso.com/a`  <br/> |Bloqueia um site `http://contoso.com/a` mas subcaminhos não adicionais, como`http://contoso.com/a/b`  <br/> |
|`http://contoso.com/a\*`  <br/> |Bloqueia um site `http://contoso.com/a` e subcaminhos adicionais, como`http://contoso.com/a/b`  <br/> |
   
5. Quando terminar de adicionar URLs, no canto inferior direito da tela, escolha **Salvar**.
    
## <a name="what-if-i-want-to-define-exceptions-for-certain-users-in-my-organization"></a>O que ocorre se eu quiser definir exceções para determinados usuários na minha organização?

Se você quiser determinados grupos possam exibir URLs que poderá ser bloqueadas para outras pessoas, você pode especificar uma política de Links de seguros ATP que se aplica a destinatários específicos. Consulte [Configurar uma lista de URLs "não regravação" personalizada usando Links de ATP seguros](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).
  
## <a name="related-topics"></a>Tópicos relacionados

[Proteção Avançada contra Ameaças do Office 365](office-365-atp.md) 
  
[Links de ATP seguros no Office 365](atp-safe-links.md)
  
[Configurar políticas de Links de ATP seguros no Office 365](set-up-atp-safe-links-policies.md)
  
[Anexos de ATP seguros no Office 365](atp-safe-attachments.md)

[Permissões de segurança do Office 365 &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md)
  


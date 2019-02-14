---
title: Configurar uma lista de URLs bloqueada personalizada usando o Office 365 ATP seguros Links
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.date: 02/06/2019
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 896a7efb-1683-465e-a394-261349e5d866
ms.collection: M365-security-compliance
description: Saiba como configurar uma lista das URLs bloqueados para sua organização usando a proteção de ameaça avançadas do Office 365. As URLs bloqueadas serão aplicados a mensagens de email e documentos do Office de acordo com suas políticas de links seguros ATP.
ms.openlocfilehash: 261d85ce72de3a19ed4c2327d56fe1f32107781b
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995312"
---
# <a name="set-up-a-custom-blocked-urls-list-using-office-365-atp-safe-links"></a>Configurar uma lista de URLs bloqueada personalizada usando o Office 365 ATP seguros Links

> [!IMPORTANT]
> Este artigo destina-se a clientes corporativos. Se você for um usuário doméstico procurando informações sobre Links seguros no Outlook, consulte [Outlook.com avançadas de segurança](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2).

Com [A proteção de ameaça avançadas do Office 365](office-365-atp.md) (ATP), sua organização pode ter uma lista personalizada de endereços de site (URLs) que são bloqueados. Quando uma URL for bloqueada, as pessoas que clique nos links para a URL bloqueada são seguidas para uma [página de aviso](atp-safe-links-warning-pages.md) semelhante à seguinte imagem: 
  
![Este site está bloqueado](media/6b4bda2d-a1e6-419e-8b10-588e83c3af3f.png)
  
A lista de URLs bloqueada é definida pela equipe de segurança do Office 365 da sua organização e essa lista se aplica a todas as pessoas da organização que é coberto por políticas de vínculos do Office 365 ATP seguros. 
  
Leia este artigo para saber como configurar personalizada lista de URLs bloqueios da sua organização para [Links de ATP seguros no Office 365](atp-safe-links.md).
  
## <a name="view-or-edit-a-custom-list-of-blocked-urls"></a>Exibir ou editar uma lista personalizada de URLs bloqueados

[Links de ATP seguros no Office 365](atp-safe-links.md) usa várias listas, incluindo personalizado bloqueada lista de URLs da sua organização. Se você tiver as permissões necessárias, você pode configurar a lista personalizada de sua organização. Você pode fazer isso editando a política de seguros Links padrão da sua organização.

Para editar (ou definir) políticas ATP, você deve ter uma das funções descritas na tabela a seguir: 

|Função  |Onde/como atribuído  |
|---------|---------|
|Administrador Global do Office 365 |A pessoa que se inscreve para comprar o Office 365 é um administrador global por padrão. (Consulte [funções de administrador do Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) para saber mais).         |
|Administrador de segurança |Centro de administração do Azure Active Directory ([https://aad.portal.azure.com](https://aad.portal.azure.com))|
|Gerenciamento de organização Online do Exchange |Centro de administração do Exchange ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) <br>ou <br>  Cmdlets do PowerShell (consulte [PowerShell do Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)) |

> [!TIP]
> Para saber mais sobre as funções e permissões, consulte [permissões no Office 365 Security &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md).

### <a name="to-view-or-edit-a-custom-blocked-urls-list"></a>Para exibir ou editar uma lista de URLs bloqueada personalizada
  
1. Vá para [https://protection.office.com](https://protection.office.com) e entre com sua conta do trabalho ou da escola. 
    
2. No painel de navegação esquerdo, em **gerenciamento de ameaça**, escolha **política** \> **Links seguros**.
    
3. Na seção **políticas que se aplicam a toda a organização** , selecione **padrão**e, em seguida, escolha **Editar** (no botão Editar se parece com um lápis).<br/>![Clique em Editar para editar sua política padrão para a proteção de Links de seguros](media/d08f9615-d947-4033-813a-d310ec2c8cca.png)<br/>Isso permite que você visualize sua lista de URLs bloqueados. Em um primeiro momento, você não pode ter qualquer URLs listadas aqui.<br/>![Lista de URLs na política padrão Links seguros bloqueados](media/575e1449-6191-40ac-b626-030a2fd3fb11.png)
  
4. Marque a caixa **Digite uma URL válida** , digite uma URL e clique no sinal de adição (**+**). 

5. Quando terminar de adicionar URLs, no canto inferior direito da tela, escolha **Salvar**.
    
## <a name="a-few-things-to-keep-in-mind"></a>Algumas coisas em mente

Você pode adicionar URLs à sua lista, lembre-se os seguintes pontos: 

- Não inclua uma barra invertida ( **/**) no final da URL. Por exemplo, em vez de inserir `http://www.contoso.com/`, insira `http://www.contoso.com`.
    
- Você pode especificar uma URL de domínio somente (como `contoso.com` ou `tailspintoys.com`). Isso irá bloquear cliques em qualquer URL que contém o domínio.

- Você pode especificar um subdomínio (como `toys.contoso.com*`) sem bloquear um domínio completo (como `contoso.com`). Isso impedirá bloco clica em qualquer URL que contém o subdomínio, mas ele não bloqueie cliques para uma URL que contém o domínio completo.  
    
- Você pode incluir até três asteriscos de caractere curinga (\*) por URL. A tabela a seguir lista alguns exemplos de como você pode inserir e o que essas entradas de efeito tem.
    
|**Entrada de exemplo**|**O que ele faz**|
|:-----|:-----|
|`contoso.com`ou`*contoso.com*`  <br/> |Bloqueia o domínio, subdomínios e caminhos, tais como `https://www.contoso.com`, `http://sub.contoso.com`, e`http://contoso.com/abc`  <br/> |
|`http://contoso.com/a`  <br/> |Bloqueia um site `http://contoso.com/a` mas subcaminhos não adicionais, como`http://contoso.com/a/b`  <br/> |
|`http://contoso.com/a*`  <br/> |Bloqueia um site `http://contoso.com/a` e subcaminhos adicionais, como`http://contoso.com/a/b`  <br/> |
|`http://toys.contoso.com*`  <br/> |Bloqueia um subdomínio ("toys" neste caso), mas permite cliques para outras URLs de domínio (como `http://contoso.com` ou `http://home.contoso.com`).  <br/> |
   

## <a name="how-to-define-exceptions-for-certain-users-in-an-organization"></a>Como definir exceções para determinados usuários em uma organização

Se você quiser determinados grupos possam exibir URLs que poderá ser bloqueadas para outras pessoas, você pode especificar uma política de Links de seguros ATP que se aplica a destinatários específicos. Consulte [Configurar uma lista de URLs "não regravação" personalizada usando Links de ATP seguros](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).
  


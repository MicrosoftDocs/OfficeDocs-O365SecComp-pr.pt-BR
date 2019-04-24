---
title: Configurar uma lista personalizada de URLs do não Rewrite usando os links seguros de ATP do Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.date: 02/06/2019
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 35dbfd99-da5a-422b-9b0e-c6caf3b645fa
ms.collection:
- M365-security-compliance
description: Ao configurar as políticas de links seguros de ATP, você pode incluir uma lista de URLs que não reconfigura para permitir que algumas pessoas em sua organização visitem sites que você inclui na sua lista.
ms.openlocfilehash: 006dab44054f9cb707bb13d158588ab6606fab5c
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32264444"
---
# <a name="set-up-a-custom-do-not-rewrite-urls-list-using-office-365-atp-safe-links"></a>Configurar uma lista personalizada de URLs do não Rewrite usando os links seguros de ATP do Office 365

> [!IMPORTANT]
> Este artigo destina-se a clientes corporativos. Se você for um usuário doméstico que procura informações sobre links seguros no Outlook, consulte [Advanced Outlook.com Security](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2).

Com a [proteção avançada contra ameaças do Office 365](office-365-atp.md) (ATP), sua organização pode ter um [URL bloqueado personalizado](set-up-a-custom-blocked-urls-list-wtih-atp.md), de modo que, quando as pessoas clicam em endereços da Web (URLs) em mensagens de email ou determinados documentos do Office, eles são impedidos de ir para essas URLs. Sua organização também pode ter listas personalizadas de "não reescrever" para grupos específicos em sua organização. Uma lista "não reconfigurar" permite que algumas pessoas visitem URLs que, de outra forma, são bloqueadas por [links de ATP seguros no Office 365](atp-safe-links.md). 
  
Este artigo descreve como especificar uma lista de URLs que são excluídas da verificação de links seguros de ATP e alguns pontos importantes a ter em mente.

## <a name="set-up-a-do-not-rewrite-list"></a>Configurar uma lista de "não reconfigurar"

A proteção de links seguros de ATP usa várias listas, incluindo a lista de URLs bloqueadas da organização e as listas "não reescrever" para exceções. Se você tiver as permissões necessárias, poderá configurar as listas personalizadas de "não reescrever". Você faz isso quando adiciona ou edita políticas de links seguros que se aplicam a destinatários específicos em sua organização. 

Para editar (ou definir) políticas ATP, você deve receber uma das funções descritas na tabela a seguir:

|Função  |Onde/como a atribuição  |
|---------|---------|
|Administrador global do Office 365 |Por padrão, a pessoa que se inscreve para comprar o Office 365 é um administrador global. (ConFira [sobre as funções de administrador do Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) para saber mais.)         |
|Administrador de segurança |Centro de administração do Azure Active[https://aad.portal.azure.com](https://aad.portal.azure.com)Directory ()|
|Gerenciamento da organização do Exchange Online |Centro de administração do[https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)Exchange () <br>ou <br>  Cmdlets do PowerShell (consulte [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)) |

> [!TIP]
> Para saber mais sobre funções e permissões, confira [permissões no centro de conformidade &amp; de segurança do Office 365](permissions-in-the-security-and-compliance-center.md).

### <a name="to-view-or-edit-a-custom-do-not-rewrite-urls-list"></a>Para exibir ou editar uma lista de URLs de "não reescrever" personalizada
  
1. AcEsse [https://protection.office.com](https://protection.office.com) e entre com sua conta corporativa ou de estudante. 
    
2. Na navegação à esquerda, em **links seguros**da **política** \> de **Gerenciamento** \> de ameaças.
    
3. Na seção **políticas que se aplicam a destinatários específicos** , escolha **novo** (o botão novo é semelhante a um sinal **+** de adição ()) para criar uma nova política. (Como alternativa, você pode editar uma política existente.)<br/>![Escolha novo para adicionar uma política de links seguros para destinatários de email específicos](media/01073f42-3cec-4ddb-8c10-4d33ec434676.png)
  
4. Especifique um nome e uma descrição para a política.
    
5. Na seção não **reescrever as seguintes URLs** , selecione a caixa **Insira uma URL válida** e, em seguida, digite uma URL e, em seguida, escolha o sinal de adição (+). 
    
6. Na seção **aplica-se** a, escolha **o destinatário é um membro de**e, em seguida, escolha o (s) grupo (s) que você deseja incluir na política. Escolha **Adicionar**e, em seguida, escolha **OK**.
    
7. Quando terminar de adicionar URLs, no canto inferior direito da tela, escolha **salvar**.
    
> [!NOTE]
> Certifique-se de revisar a lista personalizada de URLs bloqueadas da sua organização. ConFira [Configurar uma lista de URLs bloqueadas personalizada usando os links seguros de ATP](set-up-a-custom-blocked-urls-list-wtih-atp.md). 
  
## <a name="important-points-to-keep-in-mind"></a>Pontos importantes a ter em mente

- Qualquer URL especificada na lista "não reescrever" será excluída da verificação de links seguros de ATP para os destinatários que você especificar.
 
- Ao especificar uma lista "não reconfigurar" para uma política de links seguros de ATP, você pode incluir até três asteriscos curinga (\*). Caracteres curinga (\*) são considerados para entradas como `contoso.com`, por exemplo, que não incluem prefixos ou subdomínios, `http://` como `https://`ou. Isso significa que uma entrada, como `contoso.com` é semelhante à `*contoso.com*` da lista "não reconfigurar".

- Se você já tiver uma lista de URLs na lista de "não reescrever", verifique se a lista e adicione caracteres curinga conforme apropriado. Por exemplo, se a sua lista existente tem uma entrada `http://contoso.com/a` como e você deseja incluir subcaminhos como `http://contoso.com/a/b` em sua política, adicione um curinga à sua entrada para que ele se `http://contoso.com/a*`pareça.
    
- Não inclua uma barra (/) nas URLs que você especificar na lista "não reconfigurar". Por exemplo, em vez de `contoso.com/` inserir na lista "não reescrever", insira `contoso.com`.
    
A tabela a seguir lista exemplos do que você pode inserir e o efeito que essas entradas têm.
    
|**Entrada de exemplo**|**O que ele faz**|
|:-----|:-----|
|`*contoso.com*`  <br/> |Permite que destinatários específicos visitem um domínio, subdomínios e caminhos, como `http://www.contoso.com`, `https://www.contoso.com` `https://maps.contoso.com`, ou`http://www.contoso.com/a`  <br/> |
|`http://contoso.com/a`  <br/> |Permite que destinatários específicos visitem um site `http://contoso.com/a`como, mas não subcaminhos como`http://contoso.com/a/b`  <br/> |
|`http://contoso.com/a*`  <br/> |Permite que destinatários específicos visitem um site `http://contoso.com/a` como e subcaminhos como`http://contoso.com/a/b`  <br/> |
   
 
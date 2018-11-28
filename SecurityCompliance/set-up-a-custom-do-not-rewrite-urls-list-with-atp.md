---
title: Configurar uma lista de URLs execute-não-reconfiguração personalizada usando o Office 365 ATP seguros Links
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 35dbfd99-da5a-422b-9b0e-c6caf3b645fa
description: Ao configurar suas políticas de links seguros ATP, você pode incluir reconfiguração execute-não é ' lista de URLs para permitir que algumas pessoas na sua organização visitar sites que você pode incluir em sua lista.
ms.openlocfilehash: 89fafd5ff7def491a231bc8bc3eb19ef8db16a59
ms.sourcegitcommit: 2cf7f5bb282c971d33e00f65d9982a3f14aec74e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/27/2018
ms.locfileid: "26705975"
---
# <a name="set-up-a-custom-do-not-rewrite-urls-list-using-office-365-atp-safe-links"></a>Configurar uma lista de URLs execute-não-reconfiguração personalizada usando o Office 365 ATP seguros Links

Com [A proteção de ameaça avançadas do Office 365](office-365-atp.md) (ATP), sua organização pode ter um [URLs bloqueados personalizados](set-up-a-custom-blocked-urls-list-wtih-atp.md), de forma que, quando as pessoas clicarem na web endereços (URLs) em mensagens de email ou certos documentos do Office, eles são impedidos de pretende dessas URLs. Sua organização também pode ter listas personalizadas "não regravação" para grupos específicos na sua organização. Uma lista de "não regravação" permite que algumas pessoas visite URLs que são bloqueados contrário por [Links de ATP seguros no Office 365](atp-safe-links.md). 
  
Este artigo descreve como especificar uma lista das URLs que são excluídos da verificação de Links de ATP seguros e alguns pontos importantes a serem tenha em mente.

## <a name="set-up-a-do-not-rewrite-list"></a>Configurar uma lista de "não regravação"

Proteção de Links de seguros ATP usa várias listas, incluindo a lista de URLs bloqueios da sua organização e as listas de "não regravação" para exceções. Se você tiver as permissões necessárias, você pode configurar suas listas de "não regravação" personalizado. Você fazer isso quando você adicionar ou editar políticas de seguros Links que se aplicam a destinatários específicos na sua organização. 
  
1. Vá para [https://security.microsoft.com](https://security.microsoft.com) e entre com sua conta do trabalho ou da escola. 
    
2. No painel de navegação esquerdo, em **gerenciamento de ameaça** \> **política** \> **Links seguros**.
    
3. Na seção **políticas que se aplicam a destinatários específicos** , escolha **novo** (botão novo se parece com um sinal de adição ( **+**)) para criar uma nova política. (Como alternativa, você pode editar uma política existente).<br/>![Escolha Novo para adicionar uma diretiva de segurança Links para os destinatários de email específicos](media/01073f42-3cec-4ddb-8c10-4d33ec434676.png)
  
4. Especifique um nome e descrição para a diretiva.
    
5. Na seção **não reescrever as seguintes URLs** , marque a caixa **Digite uma URL válida** , digite uma URL e clique no sinal de adição (+). 
    
6. Na seção **Aplicada** , escolha **o destinatário é um membro da**e escolha o grupo (s) que você deseja incluir na sua política. Escolha **Adicionar**e escolha **Okey**.
    
7. Quando terminar de adicionar URLs, no canto inferior direito da tela, escolha **Salvar**.
    
> [!NOTE]
> Certifique-se de revisar a lista de bloqueados URLs personalizada da sua organização. Consulte [Configurar uma lista de URLs bloqueada personalizada usando Links de ATP seguros](set-up-a-custom-blocked-urls-list-wtih-atp.md). 
  
## <a name="important-points-to-keep-in-mind"></a>Pontos importantes a serem tenha em mente

- Nenhum URL que você especificar na lista "não regravação" é excluída dos Links de seguros ATP varredura para os destinatários que você especificar.
 
- Quando você especifica uma lista de "não regravação" para uma política de ATP Links de seguros, você pode incluir até três asteriscos de caractere curinga (\*). Caracteres curinga (\*) são considerados como entradas de `contoso.com`, que não explicitamente incluir prefixos ou subdomínios, como `http://` ou `https://`. Isso significa que uma entrada, tais como `contoso.com` é semelhante ao `*contoso.com*` para sua lista de "não regravação".

- Se você já tiver uma lista das URLs em sua lista de "não regravação", certifique-se revisar essa lista e adicionar caracteres curinga, conforme apropriado. Por exemplo, se sua lista existente tiver uma entrada como `http://contoso.com/a` e você deseja incluir subcaminhos como `http://contoso.com/a/b` em sua política, adicione um caractere curinga para a entrada para que ele se parece com `http://contoso.com/a*`.
    
- Não inclua uma barra (/) nas URLs que você especificar em sua lista de "não regravação". Por exemplo, em vez de inserir `contoso.com/` na sua lista de "não regravação", digite `contoso.com`.
    
Os seguintes exemplos de listas de tabela de que você pode digitar e o que essas entradas de efeito tem.
    
|**Entrada de exemplo**|**O que ele faz**|
|:-----|:-----|
|`*contoso.com*`  <br/> |Permite que os destinatários específicos a visitar um domínio, subdomínios e caminhos, tais como `http://www.contoso.com`, `https://www.contoso.com`, `https://maps.contoso.com`, ou`http://www.contoso.com/a`  <br/> |
|`http://contoso.com/a`  <br/> |Permite que os destinatários específicos visitar um site como `http://contoso.com/a`, mas não subcaminhos, como`http://contoso.com/a/b`  <br/> |
|`http://contoso.com/a*`  <br/> |Permite que os destinatários específicos visitar um site como `http://contoso.com/a` e subcaminhos like`http://contoso.com/a/b`  <br/> |
   
 
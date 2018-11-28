---
title: Configurar políticas de vínculos do Office 365 ATP seguros
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
ms.assetid: bdd5372d-775e-4442-9c1b-609627b94b5d
description: Configure políticas de Links seguros para proteger sua organização contra mal-intencionado links em arquivos do Word, Excel, PowerPoint e Visio, bem como nas mensagens de email.
ms.openlocfilehash: fb2af8e29bfe2de027a2d0e88cf9bcc07299fba9
ms.sourcegitcommit: 2cf7f5bb282c971d33e00f65d9982a3f14aec74e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/27/2018
ms.locfileid: "26706085"
---
# <a name="set-up-office-365-atp-safe-links-policies"></a>Configurar políticas de vínculos do Office 365 ATP seguros

[Links de seguros ATP](atp-safe-links.md) , um recurso de [Proteção de ameaça avançadas do Office 365](office-365-atp.md) (ATP) pode ajudar a proteger sua organização contra mal-intencionado links usados em phishing e outros ataques. Se você tiver o necessário [permissões para a segurança do Office 365 &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md), você pode configurar políticas de Links de seguros ATP para ajudar a garantir que, quando as pessoas clicarem endereços da web (URLs), sua organização seja protegida. Suas políticas de Links de seguros ATP podem ser configuradas para examinar URLs em email e em documentos do Office.
  
[Novos recursos são adicionados constantemente a ATP](office-365-atp.md#new-features-are-continually-being-added-to-atp). Como os novos recursos são adicionados, você pode precisar fazer ajustes em suas políticas de Links de seguros ATP existentes.

## <a name="what-to-do"></a>O que fazer 
  
1. [Revise os pré-requisitos](#review-the-prerequisites).
    
2. [Revisão e editar a política de Links de seguros ATP padrão que se aplica a todos](#define-an-atp-safe-links-policy-that-applies-to-everyone). Por exemplo, você pode [configurar sua lista de URLs bloqueada personalizada para Links de ATP seguros](set-up-a-custom-blocked-urls-list-wtih-atp.md).
    
3. [Adicionar ou editar políticas para destinatários de email específicos](#add-a-policy-for-specific-email-recipients), inclusive [Configurar a lista de URLs sua personalizada "Não regravação" para Links de ATP seguros](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).
    
4. [Saiba mais sobre as opções de política de Links de seguros ATP](#learn-about-atp-safe-links-policy-options) (neste artigo), incluindo configurações para alterações recentes
    
## <a name="step-1-review-the-prerequisites"></a>Etapa 1: Revisar os pré-requisitos

- Certifique-se de que sua organização tenha [A proteção de ameaça avançadas do Office 365](office-365-atp.md).
    
- Certifique-se de que você tem as permissões necessárias para definir ou editar políticas de ATP. Consulte [Permissions in a segurança do Office 365 &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md).

- Certifique-se de que os clientes do Office estejam configurados para usar a [Autenticação moderno](https://docs.microsoft.com/office365/enterprise/modern-auth-for-office-2013-and-2016) (isto é para proteção de Links de seguros ATP em documentos do Office).
    
- [Saiba mais sobre as opções de política de Links de seguros ATP](#learn-about-atp-safe-links-policy-options) (neste artigo). 

- Permitir até 30 minutos para sua política novo ou atualizado à difusão em todos os centros de dados do Office 365.
    
## <a name="step-2-define-or-review-the-atp-safe-links-policy-that-applies-to-everyone"></a>Etapa 2: Definir (ou revisar) a política de Links de seguros ATP que se aplica a todos

Quando você tem [A proteção de ameaça avançadas do Office 365](office-365-atp.md), você terá uma política de Links de seguros ATP padrão que se aplica a todas as pessoas da sua organização. Certifique-se de revisar e, se necessário, editar sua política padrão.
  
1. Vá para [https://security.microsoft.com](https://security.microsoft.com) e entre com sua conta do trabalho ou da escola. 
    
2. No painel de navegação esquerdo, em **gerenciamento de ameaça**, escolha **política \> ** **Links seguros**.
    
3. Na seção **políticas que se aplicam a toda a organização** , selecione **padrão**e, em seguida, escolha **Editar** (no botão Editar se parece com um lápis).<br/>![Clique em Editar para editar sua política padrão para a proteção de Links de seguros](media/d08f9615-d947-4033-813a-d310ec2c8cca.png)
  
4. Na seção **bloquear as seguintes URLs** , especifique uma ou mais URLs que você deseja evitar que as pessoas na sua organização do visitando. (Consulte [Configurar uma lista de URLs bloqueada personalizada usando Links de seguros ATP](set-up-a-custom-blocked-urls-list-wtih-atp.md)).
    
5. Na seção **configurações que se aplicam ao conteúdo, exceto o email** , marque (ou desmarque) as opções que você deseja usar. (É recomendável que você selecione todas as opções). 
    
6. Escolha **Salvar**.
    
## <a name="step-3-add-or-edit-atp-safe-links-policies-that-apply-to-specific-email-recipients"></a>Etapa 3: Adicionar (ou editar) diretivas de Links de seguros ATP que se aplicam aos destinatários de email específicos

Depois de ter analisado (ou editados) a política de Links de seguros ATP padrão que se aplica a todos, sua próxima etapa é definir políticas adicionais que seriam se aplicam a destinatários específicos. Por exemplo, você pode especificar exceções à diretiva padrão definindo uma política adicional. 
  
1. Vá para [https://security.microsoft.com](https://security.microsoft.com) e entre com sua conta do trabalho ou da escola. 
    
2. No painel de navegação esquerdo, em **gerenciamento de ameaça**, escolha **uma política**.
    
3. Escolha **Links seguros**.
    
4. Na seção **políticas que se aplicam a destinatários específicos** , escolha **novo** (botão novo se parece com um sinal de adição ( **+**)).<br/>![Escolha Novo para adicionar uma diretiva de segurança Links para os destinatários de email específicos](media/01073f42-3cec-4ddb-8c10-4d33ec434676.png)
  
5. Especifique o nome, a descrição e as configurações da política.<br/>**Exemplo:** Para configurar uma política não denominada "nenhum direto de Clickthrough do" que não permite que as pessoas em um determinado grupo em sua organização que clicar em um site específico sem proteção ATP Links de seguros, você pode especificar as seguintes configurações recomendadas: 
    
  - Na caixa **nome** , não digite nenhum clickthrough direto.
    
  - Na caixa **Descrição** , digite uma descrição like, evita que pessoas em determinados grupos de clicar para um site sem verificação de Links de ATP seguros.
    
  - Na seção **Selecionar a ação** , escolha **em**.
    
  - Selecione o **Uso de anexos seguros para examinar o conteúdo para download**.
    
  - Se essa opção estiver disponível, selecione **Aplicar seguros Links para as mensagens enviadas dentro da organização**.
    
  - Selecione **não permite o usuário clicar em URL original**.
    
  - (Isso é opcional) Na seção **não reescrever as seguintes URLs** , especifique uma ou mais URLs que são considerados como seguros para sua organização. (Consulte [Configurar uma lista de URLs "Não regravação" personalizada usando Links de seguros ATP](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md))
    
  - Na seção **Aplicada** , escolha **o destinatário é um membro da**e escolha o grupo (s) que você deseja incluir na sua política. Escolha **Adicionar**e escolha **Okey**.
    
6. Escolha **Salvar**.
    
## <a name="step-4-learn-about-atp-safe-links-policy-options"></a>Etapa 4: Saiba mais sobre as opções de política de Links de seguros ATP

Conforme você configurar ou editar suas políticas de Links de seguros ATP, verá diversas opções disponíveis. Caso você esteja se perguntando quais são essas opções, a tabela a seguir descreve cada um deles e seu efeito. Lembre-se de que não existem dois tipos principais de políticas de Links de seguros ATP para definir ou editar:
- uma [política padrão](#default-policy-options) que se aplica a todos 
- adicionais [que são definidas para destinatários específicos de políticas](#policies-that-apply-to-specific-email-recipients) 

### <a name="default-policy-options"></a>Opções de política padrão

Opções de política padrão se aplicam a todas as pessoas da sua organização.

|Essa opção  |Faça isto  |
|---------|---------|
| **Bloquear as seguintes URLs** <br/>    | Habilita sua organização tenha uma lista personalizada de URLs que são bloqueados automaticamente. Quando os usuários clicam uma URL nessa lista, ele será levado a uma [página de aviso](atp-safe-links-warning-pages.md) que explica por que a URL está bloqueada.<br/> Para saber mais, consulte [Set up uma lista de URLs bloqueada personalizada usando ATP Links de seguros      |
| **O Office 365 ProPlus, Office para iOS e Android** <br/>    | Quando essa opção é selecionada, Links confiáveis de ATP proteção é aplicada às URLs em documentos que estão no Office 365 ProPlus (Word, Excel e PowerPoint no Windows ou Mac OS), Office documentos abertos em iOS ou dispositivos com Android, 2016 do Visio no Windows e no Office Online (Word Online, on-line do PowerPoint, Excel Online e OneNote Online), fornecida que ao usuário tiver entrado no Office 365. <br/><br/>Se você vir **2016 do Office no Windows**, em seguida, as atualizações do recurso não atingiu seu ambiente do Office 365 ainda (e eles estão em breve). Até lá, proteção de Links de seguros ATP aplica-se a palavra 2016, 2016 do Excel, PowerPoint 2016 ou 2016 do Visio em execução no Windows.            |
| **Não rastrear quando os usuários clicam ATP Links de seguros** <br/>  | Quando essa opção é selecionada, clique em dados para URLs em documentos do Word, Excel, PowerPoint e Visio não são armazenados.  <br/> |
|**Não permita que os usuários clique nos Links de seguros de ATP para a URL original** <br/> |Quando essa opção é selecionada, os usuários não conseguir continuar após uma [página de aviso](atp-safe-links-warning-pages.md) para uma URL que é determinada por serem mal-intencionados.  <br/> |

### <a name="policies-that-apply-to-specific-email-recipients"></a>Diretivas que se aplicam aos destinatários de email específicos

|Essa opção  |Faça isto  |
|---------|---------|
|**Desligado** <br/> |Não examina URLs em mensagens de email.  <br/> Permite que você defina uma regra de exceção, como uma regra que não verifica URLs em mensagens de email para um grupo específico de destinatários.  <br/> |
|**Em** <br/> |Reconfigure URLs para usuários de rota por meio de proteção de Links de seguros ATP quando os usuários clicam em URLs em mensagens de email.  <br/> Verifica a uma URL quando clicado em relação a uma lista das URLs de bloqueios ou mal-intencionado.  <br/> |
|**Usar anexos seguros para examinar o conteúdo para download** <br/> |Quando essa opção é selecionada, as URLs que apontam para download de conteúdo são verificadas.  <br/> |
|**Aplicar seguros Links às mensagens enviadas dentro da organização** <br/> | Quando essa opção está disponível e marcada, a proteção de Links de seguros ATP é aplicada para emails, as mensagens enviadas entre as pessoas da sua organização, fornecida as contas de email são hospedadas no Office 365.  <br/> |
|**Não rastrear cliques do usuário** <br/> |Quando essa opção é selecionada, clique em dados para URLs em emails de remetentes externos não são armazenados. Click URL acompanhamento para links em emails enviados dentro da organização não é suportado no momento.  <br/> |
|**Não permita aos usuários clicarem por meio de URL original** <br/> |Quando essa opção é selecionada, os usuários não conseguir continuar após uma [página de aviso](atp-safe-links-warning-pages.md) para uma URL que é determinada por serem mal-intencionados.  <br/> |
|**Não reescrever as seguintes URLs** <br/> |Deixa URLs como estão. Mantém uma lista personalizada de seguros URLs que não necessitem de verificação para um grupo específico de destinatários de email na sua organização.  Consulte [Configurar uma lista de URLs "Não regravação" personalizada usando Links de seguros ATP](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) para obter mais detalhes, incluindo alterações recentes para dar suporte a curinga asteriscos (\*).<br/> |
   
## <a name="next-steps"></a>Próximas etapas

Depois que suas políticas de Links de seguros ATP estão funcionando, você pode ver como ATP está trabalhando para sua organização exibindo relatórios. Consulte os seguintes recursos para saber mais:

- [Exibir relatórios de proteção de ameaça avançadas do Office 365](view-reports-for-atp.md)

- [Use o Explorer na segurança &amp; Centro de conformidade](use-explorer-in-security-and-compliance.md) 
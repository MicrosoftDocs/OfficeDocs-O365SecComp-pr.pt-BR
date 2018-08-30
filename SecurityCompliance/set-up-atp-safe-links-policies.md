---
title: Configurar políticas de vínculos do Office 365 ATP seguros
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
ms.assetid: bdd5372d-775e-4442-9c1b-609627b94b5d
description: Configure políticas de Links seguros para proteger sua organização contra mal-intencionado links em arquivos do Word, Excel, PowerPoint e Visio, bem como nas mensagens de email.
ms.openlocfilehash: 0f43cf1eec63df4b70f88abf36e8f097da72ebbc
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524493"
---
# <a name="set-up-office-365-atp-safe-links-policies"></a>Configurar políticas de vínculos do Office 365 ATP seguros

[Links de seguros ATP](atp-safe-links.md) , um recurso de [Proteção de ameaça avançadas do Office 365](office-365-atp.md) (ATP) pode ajudar a proteger sua organização contra mal-intencionado links usados em phishing e outros ataques. Se você tiver o necessário [permissões atribuídas no Office 365 Security &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md), você pode configurar políticas de Links de seguros ATP para ajudar a garantir que, quando as pessoas clicarem endereços da web (URLs), sua organização seja protegida. Suas políticas de Links de seguros ATP podem ser configuradas para examinar URLs em email e em documentos do Office.
  
Novos recursos são adicionados constantemente a Links de seguros ATP:
  
- No de 2017 outubro tardia, proteção de Links de seguros ATP é estendida para aplicar ao URLs em email, bem como as URLs em documentos do Office 365 ProPlus, como Word, Excel, PowerPoint no Windows, iOS e dispositivos com Android e arquivos do Visio no Windows.
    
- Iniciando no de 2018 de março, proteção de Links de seguros ATP é estendida para aplicar a emails enviados entre pessoas em uma organização.
    
- Proteção de Links de seguros ATP a partir do final de 2018 de março, é estendida para aplicar a URLs no Office Online (on-line do Word, Excel Online, on-line do PowerPoint e OneNote Online) e Office 365 ProPlus no Mac OS.
    
- Iniciando no maio de 2018, [páginas de aviso](atp-safe-links-warning-pages.md) são atualizados com um novo esquema de cores, mais detalhes e a capacidade para continuar a um site apesar das recomendações de determinado. 

Como os novos recursos são adicionados, você pode precisar fazer ajustes em suas políticas de Links de seguros ATP existentes.

## <a name="what-to-do"></a>O que fazer 
  
1. [Revise os pré-requisitos](#review-the-prerequisites)
    
2. [Definir uma política de Links de seguros ATP que se aplica a todos](set-up-atp-safe-links-policies.md#reveddefaultscc), inclusive [configurar sua lista de URLs bloqueada personalizada para Links de seguros ATP](set-up-a-custom-blocked-urls-list-wtih-atp.md)
    
3. [Adicionar uma política para destinatários de email específicos](set-up-atp-safe-links-policies.md#addemailpolscc), inclusive [Configurar a lista de URLs sua personalizada "Não regravação" para Links de seguros ATP](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md)
    
4. [Saiba mais sobre as opções de política de Links de seguros ATP](set-up-atp-safe-links-policies.md#policyoptions), incluindo configurações para alterações recentes
    
## <a name="review-the-prerequisites"></a>Revise os pré-requisitos

- Certifique-se de que sua organização tenha [A proteção de ameaça avançadas do Office 365](office-365-atp.md).
    
- Certifique-se de que você tenha o necessário [permissões atribuídas no Office 365 Security &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md).
    
- [Saiba mais sobre as opções de política de Links de seguros ATP](#learn-about-atp-safe-links-policy-options) (neste artigo). 
    
- Permitir até 30 minutos para sua política novo ou atualizado à difusão em todos os centros de dados do Office 365.
    
## <a name="define-an-atp-safe-links-policy-that-applies-to-everyone"></a>Definir uma política de Links de seguros ATP que se aplica a todos

Quando você tem a proteção de ameaça avançadas no Office 365 Enterprise, você terá uma política de Links de seguros ATP para definir que se aplica a todas as pessoas da sua organização. Você pode editar sua política em ambos o Security &amp; Centro de conformidade ou centro de administração do Exchange. É recomendável usar a segurança &amp; Centro de conformidade para analisar ou editar qualquer uma das suas políticas de ATP.
  
1. Vá para [https://protection.office.com](https://protection.office.com) e entre com sua conta do trabalho ou da escola. 
    
2. No painel de navegação esquerdo, em **gerenciamento de ameaça**, escolha **política \> ** **Links seguros**.
    
3. Na seção **políticas que se aplicam a toda a organização** , selecione **padrão**e, em seguida, escolha **Editar** (no botão Editar se parece com um lápis). 
    
    ![Clique em Editar para editar sua política padrão para a proteção de Links de seguros](media/d08f9615-d947-4033-813a-d310ec2c8cca.png)
  
4. Na seção **bloquear as seguintes URLs** , especifique uma ou mais URLs que você deseja evitar que as pessoas na sua organização do visitando. (Consulte [Configurar uma lista de URLs bloqueada personalizada usando Links de seguros ATP](set-up-a-custom-blocked-urls-list-wtih-atp.md)).
    
5. Na seção **configurações que se aplicam ao conteúdo, exceto o email** , marque (ou desmarque) as opções que você deseja usar. (É recomendável que você selecione todas as opções). 
    
6. Escolha **Salvar**.
    
## <a name="add-a-policy-for-specific-email-recipients"></a>Adicionar uma diretiva para os destinatários de email específicos

Depois que você definiu uma política para todos os usuários, considere a adição de políticas para grupos específicos de destinatários de email. Isso permite que você especifique exceções à sua política padrão. Você pode adicionar políticas usando qualquer um da segurança &amp; Centro de conformidade (recomendado) ou o Centro de administração do Exchange. É recomendável usar a segurança &amp; Centro de conformidade para analisar ou editar qualquer uma das suas políticas de ATP.
  
1. Vá para [https://protection.office.com](https://protection.office.com) e entre com sua conta do trabalho ou da escola. 
    
2. No painel de navegação esquerdo, em **gerenciamento de ameaça**, escolha **uma política**.
    
3. Escolha **Links seguros**.
    
4. Na seção **políticas que se aplicam a destinatários específicos** , escolha **novo** (botão novo se parece com um sinal de adição ( **+**)).
    
    ![Escolha Novo para adicionar uma diretiva de segurança Links para os destinatários de email específicos](media/01073f42-3cec-4ddb-8c10-4d33ec434676.png)
  
5. Especifique o nome, a descrição e as configurações da política.
    
    **Exemplo:** Para configurar uma política não denominada "nenhum direto de Clickthrough do" que não permite que as pessoas em um determinado grupo em sua organização que clicar em um site específico sem proteção ATP Links de seguros, você pode especificar as seguintes configurações recomendadas: 
    
  - Na caixa **nome** , não digite nenhum clickthrough direto.
    
  - Na caixa **Descrição** , digite uma descrição like, evita que pessoas em determinados grupos de clicar para um site sem verificação de Links de ATP seguros.
    
  - Na seção **Selecionar a ação** , escolha **em**.
    
  - Selecione o **Uso de anexos seguros para examinar o conteúdo para download**.
    
  - Se essa opção estiver disponível, selecione **Aplicar seguros Links para as mensagens enviadas dentro da organização**.
    
  - Selecione **não permite o usuário clicar em URL original**.
    
  - (Isso é opcional) Na seção **não reescrever as seguintes URLs** , especifique uma ou mais URLs que são considerados como seguros para sua organização. (Consulte [Configurar uma lista de URLs "Não regravação" personalizada usando Links de seguros ATP](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md))
    
  - Na seção **Aplicada** , escolha **o destinatário é um membro da**e escolha o grupo (s) que você deseja incluir na sua política. Escolha **Adicionar**e escolha **Okey**.
    
6. Escolha **Salvar**.
    
## <a name="learn-about-atp-safe-links-policy-options"></a>Saiba mais sobre as opções de política de Links de seguros ATP

Conforme você configurar ou editar uma política de Links de seguros ATP, verá diversas opções disponíveis. Caso você esteja se perguntando quais são essas opções, a tabela a seguir descreve cada um deles e seu efeito. Observe que há dois tipos principais de políticas para definir ou editar: uma política padrão que se aplica a todas as pessoas e políticas adicionais que são definidas para destinatários específicos.
  
|**Para esta política**|**Essa opção**|**Faça isto**|
|:-----|:-----|:-----|
|Padrão (depois de definidas, a política padrão se aplica a todas as pessoas na organização)  <br/> |**Bloquear as seguintes URLs** <br/> |Habilita sua organização tenha uma lista personalizada de URLs que são bloqueados automaticamente. Quando os usuários clicam uma URL nessa lista, ele será levado a uma [página de aviso](atp-safe-links-warning-pages.md) que explica por que a URL está bloqueada.<br/> Consulte [Configurar uma lista de URLs bloqueada personalizada usando Links de seguros ATP](set-up-a-custom-blocked-urls-list-wtih-atp.md) para obter mais detalhes, como recém-adicionado suporte para até três asteriscos de caractere curinga (\*).  <br/> |
|Padrão  <br/> |**O Office 365 ProPlus, Office para iOS e Android** <br/> |Quando essa opção é selecionada, Links confiáveis de ATP proteção é aplicada às URLs em documentos que estão no Office 365 ProPlus (Word, Excel e PowerPoint no Windows ou Mac OS), Office documentos abertos em iOS ou dispositivos com Android, 2016 do Visio no Windows e no Office Online (Word Online, on-line do PowerPoint, Excel Online e OneNote Online), fornecida que ao usuário tiver entrado no Office 365.  <br/> > [!TIP]> Se você vir **2016 do Office no Windows**, em seguida, as atualizações do recurso não atingiu seu ambiente do Office 365 ainda (e eles estão em breve). Até lá, proteção de Links de seguros ATP aplica-se a palavra 2016, 2016 do Excel, PowerPoint 2016 ou 2016 do Visio em execução no Windows.           |
|Padrão  <br/> |**Não rastrear quando os usuários clicam ATP Links de seguros** <br/> |Quando essa opção é selecionada, clique em dados para URLs em documentos do Word, Excel, PowerPoint e Visio não são armazenados.  <br/> |
|Padrão  <br/> |**Não permita que os usuários clique nos Links de seguros de ATP para a URL original** <br/> |Quando essa opção é selecionada, os usuários não conseguir continuar após uma [página de aviso](atp-safe-links-warning-pages.md) para uma URL que é determinada por serem mal-intencionados.  <br/> |
|Uma política criada para destinatários de email específicos  <br/> |**Desligado** <br/> |Não examina URLs em mensagens de email.  <br/> Permite que você defina uma regra de exceção, como uma regra que não verifica URLs em mensagens de email para um grupo específico de destinatários.  <br/> |
|Uma política criada para destinatários de email específicos  <br/> |**Em** <br/> |Reconfigure URLs para usuários de rota por meio de proteção de Links de seguros ATP quando os usuários clicam em URLs em mensagens de email.  <br/> Verifica a uma URL quando clicado em relação a uma lista das URLs de bloqueios ou mal-intencionado.  <br/> |
|Uma política criada para destinatários de email específicos  <br/> |**Usar anexos seguros para examinar o conteúdo para download** <br/> |Quando essa opção é selecionada, as URLs que apontam para download de conteúdo são verificadas.  <br/> |
|Uma política criada para destinatários de email específicos  <br/> |**Aplicar seguros Links às mensagens enviadas dentro da organização** <br/> | *Esse recurso é aplicação do início no de 2018 março.*  <br/> Quando essa opção está disponível e marcada, a proteção de Links de seguros ATP é aplicada para emails, as mensagens enviadas entre as pessoas da sua organização, fornecida as contas de email são hospedadas no Office 365.  <br/> |
|Uma política criada para destinatários de email específicos  <br/> |**Não rastrear cliques do usuário** <br/> |Quando essa opção é selecionada, clique em dados para URLs em emails de remetentes externos não são armazenados.  <br/> Click URL acompanhamento para links em emails enviados dentro da organização não é suportado no momento.  <br/> |
|Uma política criada para destinatários de email específicos  <br/> |**Não permita aos usuários clicarem por meio de URL original** <br/> |Quando essa opção é selecionada, os usuários não conseguir continuar após uma [página de aviso](atp-safe-links-warning-pages.md) para uma URL que é determinada por serem mal-intencionados.  <br/> |
|Uma política criada para destinatários de email específicos  <br/> |**Não reescrever as seguintes URLs** <br/> |Deixa URLs como estão. Mantém uma lista personalizada de seguros URLs que não necessitem de verificação para um grupo específico de destinatários de email na sua organização.<br/> Consulte [Configurar uma lista de URLs "Não regravação" personalizada usando Links de seguros ATP](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) para obter mais detalhes, incluindo alterações recentes para dar suporte a curinga asteriscos (\*).  <br/> |
   
## <a name="related-topics"></a>Tópicos relacionados

[Proteção Avançada contra Ameaças do Office 365](office-365-atp.md) 
  
[Links de ATP seguros no Office 365](atp-safe-links.md)
  
[Anexos de ATP seguros no Office 365](atp-safe-attachments.md)
  
[Configurar uma lista de URLs bloqueada personalizada usando ATP Links de seguros](set-up-a-custom-blocked-urls-list-wtih-atp.md)
  
[Configurar uma lista de URLs "Não regravação" personalizada usando ATP Links de seguros](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md)
  
[Exibir relatórios de Proteção avançada contra ameaças](view-reports-for-atp.md)

[Permissões de segurança do Office 365 &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md)
  


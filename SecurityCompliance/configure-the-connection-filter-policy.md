---
title: Configurar a política do filtro de conexão
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/2/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 6ae78c12-7bbe-44fa-ab13-c3768387d0e3
description: Para certificar-se de que os emails enviados de pessoas que confiáveis não não bloqueado, você pode usar a política de filtro de conexão para criar uma lista de permissões, também conhecido como uma lista de remetentes seguros, de endereços IP que você confia. Você também pode criar uma lista de remetentes bloqueados.
ms.openlocfilehash: cb9b73ff61b477f1c7ea0bb8da4039bebce83d1b
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23003260"
---
# <a name="configure-the-connection-filter-policy"></a>Configurar a política do filtro de conexão
 
A maioria de nós tem amigos e parceiros de negócios, nos quais confiamos. Pode ser bem frustrante encontrar os emails deles na sua pasta de lixo eletrônico ou completamente bloqueados por um filtro de spam. Se quiser garantir que o email enviado por pessoas da sua confiança não seja bloqueado, use a política de filtro de conexão para criar uma Lista de permissões (ou "lista de remetentes confiáveis") contendo endereços IP nos quais você confia. Também é possível criar uma lista de remetentes bloqueados, que é uma lista de endereços IP, geralmente pertencentes a remetentes de spam conhecidos, dos quais você não quer receber mensagens.
  
 Para conhecer mais configurações de spam que se aplicam à toda a organização, consulte [Como ajudar a garantir que uma mensagem não seja marcada como spam](https://go.microsoft.com/fwlink/p/?LinkId=534224) ou [Bloquear spam no email com o filtro de spam do Office 365 para evitar problemas com falsos negativos](https://go.microsoft.com/fwlink/p/?LinkId=534225). Estes artigos são úteis se você tiver controle de administrador e quiser evitar falsos positivos ou falsos negativos.
  
O vídeo a seguir mostra as etapas de configuração da política de filtro de conexão:
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/b2f5bea3-e1a7-44b3-b7e2-07fac0d0ca40?autoplay=false]
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>O que você precisa saber antes de começar?
<a name="sectionSection0"> </a>

- Tempo estimado para conclusão: 15 minutos
    
- Você precisa ter permissões antes de executar este procedimento ou procedimentos. Para ver quais permissões você precisa, consulte a entrada "Antispam" no tópico [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) . 
    
- Para obter o endereço IP do remetente cujas mensagens você gostaria de permitir ou bloquear, verifique o cabeçalho de Internet da mensagem. Procure o cabeçalho CIP, conforme descrito em [Cabeçalhos de mensagem antispam](anti-spam-message-headers.md). Para obter informações sobre como exibir um cabeçalho de mensagem em vários clientes de email, confira o tópico [Analisador de Cabeçalho de Mensagens](https://go.microsoft.com/fwlink/p/?LinkId=306583). 
    
- Mensagens de email enviadas de um endereço IP na lista de bloqueios de IP são rejeitadas, não são marcadas como spam, e nenhum filtro adicional ocorre.
    
- O procedimento de filtro de conexão a seguir também pode ser executado via o PowerShell remoto. Use o cmdlet [Get-HostedConnectionFilterPolicy](http://technet.microsoft.com/library/bd751db2-3f26-495b-8e5a-4fcab53b17fd.aspx) para examinar suas configurações e o [Set-HostedConnectionFilterPolicy](http://technet.microsoft.com/library/ccb5731b-3fca-4d69-a91f-5049ea963fac.aspx) para editar suas configurações de política de filtro de conexão. Para saber como usar o Windows PowerShell para se conectar ao Exchange Online Protection, consulte [Connect to Exchange Online Protection PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627290). Para saber como usar o Windows PowerShell para se conectar ao Exchange Online, consulte [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).
    
- Para informações sobre atalhos de teclado que possam se aplicar aos procedimentos neste tópico, consulte **Keyboard shortcuts in Exchange 2013**.
    
## <a name="use-the-eac-to-edit-the-default-connection-filter-policy"></a>Use o EAC para editar a política padrão de filtro de conexão
<a name="sectionSection1"> </a>

Crie uma Lista de IP Permitidos ou uma Lista de IP Bloqueados editando a política de filtro de conexão no EAC (Centro de Administração do Exchange). As configurações da política de filtro de conexão são aplicadas apenas às mensagens de entrada.
  
1. No centro de administração do Exchange (EAC), vá em **Proteção** \> **Filtro de conexão**, e clique duas vezes na política padrão.
    
2. Clique no item de menu **Filtragem de conexão** e crie as listas que quiser: uma Lista de IP Permitidos, uma Lista de IP Bloqueados ou ambas. 
    
    Para criar estas listas, clique em ![Ícone Adicionar](media/ITPro-EAC-AddIcon.gif). Na caixa de diálogo posterior, especifique a faixa de endereço ou endereço IP, e então clique em **ok**. Repita este processo para adicionar mais endereços. (Você também pode editar ou remover endereços IP após eles terem sido adicionados.)
    
    > [!NOTE]
    >  Se você adicionar um endereço IP às duas listas, o email enviado será permitido. >  Os endereços IP do tipo IPV4 devem ser especificados no formato nnn.nnn.nnn.nnn em que nnn é um número de 0 a 255. Também é possível especificar intervalos CIDR (Roteamento entre Domínios sem Classificação) no formato nnn.nnn.nnn.nnn/rr em que rr é um número de 24 a 32. Para especificar intervalos fora do intervalo de 24 a 32, confira [Considerações adicionais ao configurar listas de IP Permitidos](configure-the-connection-filter-policy.md#bkmk_addtionalconsiderationswhenconfiguringipallowlists). >  Você pode especificar um máximo de 1.273 entradas, sendo cada entrada um único endereço IP ou um intervalo CIDR de endereços IP de /24 a /32. >  Se enviar mensagens criptografadas por TLS, não haverá suporte para endereços IPv6 e intervalos de endereços. 
  
3. Opcionalmente, marque a caixa de seleção **Habilitar lista de confiança** para evitar a perda de emails procedentes de determinados remetentes bem conhecidos. Como? A Microsoft assina fontes terceirizadas de remetentes confiáveis. O uso dessa lista de confiança significa que esses remetentes confiáveis não serão erroneamente marcados como spam. Recomendamos selecionar esta opção, porque ela deve reduzir a quantidade de falsos positivos (emails confiáveis que são classificados como spam) recebidos. 
    
4. Clique em **salvar**. Um resumo das suas configurações de política padrão aparece no painel à direita.
    
## <a name="additional-considerations-when-configuring-ip-allow-lists"></a>Considerações adicionais ao configurar listas de IP Permitidos
<a name="bkmk_addtionalconsiderationswhenconfiguringipallowlists"> </a>

A seguir estão algumas considerações adicionais que você pode desejar consultar ou que você deve estar ciente ao configurar uma lista de IP Permitidos.
  
### <a name="specifying-a-cidr-range-that-falls-outside-of-the-recommended-range"></a>Especificando uma faixa de CIDR que está fora da faixa recomendada

Para especificar um intervalo de endereços IP CIDR de /1 a /23, crie uma regra de transporte que opere no intervalo de endereços IP que define o nível de confiança de spam (SCL) como **Ignorar filtragem de spam** (significando que todas as mensagens recebidas nesse intervalo de endereços IP serão definidas como "não sendo spam" e nenhuma filtragem adicional será executada pelo serviço). Entretanto, se qualquer um destes endereços IP aparecer em qualquer uma das listas de bloqueio proprietárias da Microsoft ou em qualquer uma das listas de bloqueio de terceiros, estas mensagens ainda assim serão bloqueadas. Portanto, recomenda-se fortemente que você use a faixa de endereço IP de /32 a /24. 
  
Para criar esta regra de Transporte, realize as seguintes etapas.
  
1. No EAC, navegue até **Fluxo de email** \> **Regras**.
    
2. Clique em ![Ícone Adicionar](media/ITPro-EAC-AddIcon.gif) e em seguida, selecione **Criar uma nova regra**.
    
3. Dê um nome à regra e então clique em **Mais opções**.
    
4. Em **Aplicar esta regra se**, selecione **O remetente** e então selecione **endereço IP em qualquer uma destas faixas ou correspondências exatas**.
    
5. No campo **especificar endereços IP**, especifique o intervalo de endereços IP, clique em **Adicionar**![Ícone Adicionar](media/ITPro-EAC-AddIcon.gif) e clique em **ok**.
    
6. Na caixa **Faça o seguinte**, defina a ação, escolhendo **Modificar as propriedades da mensagem** e depois **definir o nível de confiança de spam (SCL)**. Na caixa **especificar SCL**, selecione **Ignorar filtragem de spam**, e clique em **ok**.
    
7. Se desejar, você pode optar por auditar a regra, testar a regra, ativar a regra durante um período de tempo específico e outras opções. Recomendamos testar a regra por um período antes de aplicá-la. O tópico [Manage Transport Rules](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx) contém mais informações sobre estas seleções. 
    
8. Clique no botão **salvar** para salvar a regra. Ela aparece na sua lista de regras. 
    
Depois de criar e fazer cumprir a regra, a filtragem de spam é desviada para o intervalo de endereços IP que você especificou.
  
### <a name="scoping-an-ip-allow-list-exception-for-a-specific-domain"></a>Controlando uma exceção da lista de IP Permitidos para um domínio específico

Em geral, recomendamos que você adicione endereços IP (ou faixas de endereço IP) para todos os domínios que você considerar seguro para a lista de IP Permitidos. No entanto, se você não quer que sua lista de permissões de IP se aplique a todos os seus domínios, é possível criar uma regra de transporte que excetua domínios específicos. 
  
Por exemplo, digamos que você tem três domínios: ContosoA.com, ContosoB.com e ContosoC.com, e você deseja adicionar o endereço IP (para simplificar, vamos usar 1.2.3.4) e pular a filtragem apenas para o domínio ContosoB.com. Você poderia criar uma lista de permissões de IP para 1.2.3.4, que define o nível de confiança de spam (SCL) a -1 (o que significa que é classificado como não-spam) em todos os domínios. Você pode, então, criar uma regra de transporte que define o SCL para todos os domínios, exceto ContosoB.com a 0. Isso resulta na mensagem sendo reexaminada novamente para todos os domínios relacionados com o endereço IP, exceto para ContosoB.com que é o domínio listado como exceção na regra. ContosoB.com ainda tem um SCL de -1, o que significa ignorar filtragem, enquanto ContosoA.com e ContosoC.com têm SCLs de 0, o que significa que será examinado novamente pelo filtro de conteúdo.
  
Para fazer isso, execute as seguintes etapas:
  
1. No EAC, navegue até **Fluxo de email** \> **Regras**.
    
2. Clique em ![Ícone Adicionar](media/ITPro-EAC-AddIcon.gif) e em seguida, selecione **Criar uma nova regra**.
    
3. Dê um nome à regra e então clique em **Mais opções**.
    
4. Em **Aplicar esta regra se**, selecione **O remetente** e então selecione **endereço IP em qualquer uma destas faixas ou correspondências exatas**.
    
5. Na caixa **especificar endereços IP**, especifique o endereço IP ou intervalo de endereços IP que você digitou na lista de permissões de IP, clique em **Adicionar**![Ícone Adicionar](media/ITPro-EAC-AddIcon.gif) e clique em **ok**.
    
6. Em **Faça**, configure a opção selecionando **Modificar as propriedades da mensagem** e então **defina o nível de confiança do spam (SCL)**. Na caixa **especificar SCL**, selecione **0**, e clique em **ok**.
    
7. Clique em **adicionar exceção**, e em **Exceto se**, selecione **O remetente** e selecione **domínio é**. 
    
8. Na caixa **especificar domínio**, digite o domínio para o qual deseja ignorar filtragem de spam, como **contosob.com**. Clique em **Adicionar**![Ícone Adicionar](media/ITPro-EAC-AddIcon.gif) para movê-lo para a lista de frases. Repita esta etapa se você deseja adicionar mais domínios como exceções e clique em **ok** após ter finalizado. 
    
9. Se desejar, você pode optar por auditar a regra, testar a regra, ativar a regra durante um período de tempo específico e outras opções. Recomendamos testar a regra por um período antes de aplicá-la. O tópico [Manage Transport Rules](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx) contém mais informações sobre estas seleções. 
    
10. Clique no botão **salvar** para salvar a regra. Ela aparece na sua lista de regras. 
    
Depois de criar e aplicar a regra, a filtragem de spam para o endereço IP ou intervalo de endereço IP que você especificou é ignorada apenas para a exceção de domínio que você digitou.
  
## <a name="new-to-office-365"></a>Começando a usar o Office 365?
<a name="sectionSection3"> </a>

||
|:-----|
|![O ícone pequeno do LinkedIn Learning](media/eac8a413-9498-4220-8544-1e37d1aaea13.png) **Começando a usar o Office 365?**         Descubra cursos em vídeo gratuitos para **Office 365 admins and IT pros**, oferecidos pelo LinkedIn Learning. |
   
## <a name="for-more-information"></a>Para saber mais
<a name="sectionSection4"> </a>

[Remetentes seguros e bloqueados listas de remetentes no Exchange Online](safe-sender-and-blocked-sender-lists-faq.md)
  
[Configurar suas políticas de filtro de spam](configure-your-spam-filter-policies.md)
  
[Configurar a política de spam de saída](configure-the-outbound-spam-policy.md)
  
[Como ajudar a garantir que uma mensagem não é marcada como spam](https://go.microsoft.com/fwlink/p/?LinkId=534224)
  
[Bloquear spam de email com o filtro de spam do Office 365 para evitar problemas de falsos negativos](https://go.microsoft.com/fwlink/p/?LinkId=534225)
  


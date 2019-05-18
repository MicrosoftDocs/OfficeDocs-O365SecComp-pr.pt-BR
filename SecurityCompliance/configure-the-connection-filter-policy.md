---
title: Configurar a política do filtro de conexão
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 10/24/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 6ae78c12-7bbe-44fa-ab13-c3768387d0e3
ms.collection:
- M365-security-compliance
description: Para garantir que os emails enviados de pessoas confiáveis não sejam bloqueados, você pode usar a política de filtro de conexão para criar uma lista de permissões, também conhecida como lista de remetentes confiáveis, dos endereços IP nos quais você confia. Você também pode criar uma lista de remetentes bloqueados.
ms.openlocfilehash: 5d19898b6baf01c7348b434f3caced202507c4d8
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34151293"
---
# <a name="configure-the-connection-filter-policy"></a>Configurar a política do filtro de conexão
 
A maioria de nós tem amigos e parceiros de negócios, nos quais confiamos. Pode ser bem frustrante encontrar os emails deles na sua pasta de lixo eletrônico ou completamente bloqueados por um filtro de spam. Se quiser garantir que o email enviado por pessoas da sua confiança não seja bloqueado, use a política de filtro de conexão para criar uma Lista de permissões (ou "lista de remetentes confiáveis") contendo endereços IP nos quais você confia. Também é possível criar uma lista de remetentes bloqueados, que é uma lista de endereços IP, geralmente pertencentes a remetentes de spam conhecidos, dos quais você não quer receber mensagens.
  
 Para conhecer mais configurações de spam que se aplicam à toda a organização, consulte [Como ajudar a garantir que uma mensagem não seja marcada como spam](https://go.microsoft.com/fwlink/p/?LinkId=534224) ou [Bloquear spam no email com o filtro de spam do Office 365 para evitar problemas com falsos negativos](https://go.microsoft.com/fwlink/p/?LinkId=534225). Estes artigos são úteis se você tiver controle de administrador e quiser evitar falsos positivos ou falsos negativos.
  
O vídeo a seguir mostra as etapas de configuração da política de filtro de conexão:
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/b2f5bea3-e1a7-44b3-b7e2-07fac0d0ca40?autoplay=false]
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>O que você precisa saber antes de começar?
<a name="sectionSection0"> </a>

- Tempo estimado para conclusão: 15 minutos
    
- Para executar este procedimento ou estes procedimentos, você precisa receber permissões. Para ver de que permissões você precisa, consulte o entrada "anti-spam" no tópico [permissões de recursos no Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) . 
    
- Para obter o endereço IP do remetente cujas mensagens você gostaria de permitir ou bloquear, verifique o cabeçalho de Internet da mensagem. Procure o cabeçalho CIP, conforme descrito em [Cabeçalhos de mensagem antispam](anti-spam-message-headers.md). Para obter informações sobre como exibir um cabeçalho de mensagem em vários clientes de email, consulte Analisador de [cabeçalho de mensagem](https://go.microsoft.com/fwlink/p/?LinkId=306583). 
    
- Mensagens de email enviadas de um endereço IP na lista de bloqueios de IP são rejeitadas, não são marcadas como spam, e nenhum filtro adicional ocorre.
    
- O procedimento de filtro de conexão a seguir também pode ser executado via PowerShell remoto. Use o cmdlet [Get-HostedConnectionFilterPolicy](http://technet.microsoft.com/library/bd751db2-3f26-495b-8e5a-4fcab53b17fd.aspx) para revisar suas configurações e o cmdlet [Set-HostedConnectionFilterPolicy](http://technet.microsoft.com/library/ccb5731b-3fca-4d69-a91f-5049ea963fac.aspx) para editar as configurações da política de filtro de conexão. Para saber como usar o Windows PowerShell para se conectar à proteção do Exchange Online, confira [conectar-se ao PowerShell do Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkid=627290). Para saber como usar o Windows PowerShell para se conectar ao Exchange Online, confira [Connect to Exchange Online Using Remote PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).
    
## <a name="use-the-eac-to-edit-the-default-connection-filter-policy"></a>Use o EAC para editar a política padrão de filtro de conexão
<a name="sectionSection1"> </a>

Crie uma Lista de IP Permitidos ou uma Lista de IP Bloqueados editando a política de filtro de conexão no EAC (Centro de Administração do Exchange). As configurações da política de filtro de conexão são aplicadas apenas às mensagens de entrada.
  
1. No centro de administração do Exchange (EAC), vá em **Proteção** \> **Filtro de conexão**, e clique duas vezes na política padrão.
    
2. Clique no item de menu **Filtragem de conexão** e crie as listas que quiser: uma Lista de IP Permitidos, uma Lista de IP Bloqueados ou ambas. 
    
    Para criar estas listas, clique em ![Ícone Adicionar](media/ITPro-EAC-AddIcon.gif). Na caixa de diálogo posterior, especifique a faixa de endereço ou endereço IP, e então clique em **ok**. Repita este processo para adicionar mais endereços. (Você também pode editar ou remover endereços IP após eles terem sido adicionados.)
    
    > [!NOTE]
    >  Se você adicionar um endereço IP a ambas as listas, os emails enviados desse endereço IP serão permitidos. 

    Especifique endereços IP IPV4 no formato nnn. nnn. nnn. nnn em que NNN é um número de 0 a 255. Também é possível especificar intervalos CIDR (Roteamento entre Domínios sem Classificação) no formato nnn.nnn.nnn.nnn/rr em que rr é um número de 24 a 32. Para especificar intervalos fora do intervalo de 24 a 32, confira [Considerações adicionais ao configurar listas de IP Permitidos](configure-the-connection-filter-policy.md#bkmk_addtionalconsiderationswhenconfiguringipallowlists). 

    Você pode especificar um máximo de 1.273 entradas, sendo cada entrada um único endereço IP ou um intervalo CIDR de endereços IP de /24 a /32. >  Se enviar mensagens criptografadas por TLS, não haverá suporte para endereços IPv6 e intervalos de endereços. 
  
3. Opcionalmente, marque a caixa de seleção **Habilitar lista de confiança** para evitar a perda de emails procedentes de determinados remetentes bem conhecidos. Como? A Microsoft assina fontes terceirizadas de remetentes confiáveis. O uso dessa lista de confiança significa que esses remetentes confiáveis não serão erroneamente marcados como spam. É recomendável selecionar essa opção, pois ela deve reduzir o número de falsos positivos (mensagens boas classificadas como spam) recebidas. 
    
4. Clique em **salvar**. Um resumo das suas configurações de política padrão aparece no painel à direita.
    
## <a name="additional-considerations-when-configuring-ip-allow-lists"></a>Considerações adicionais ao configurar listas de IP Permitidos
<a name="bkmk_addtionalconsiderationswhenconfiguringipallowlists"> </a>

A seguir estão algumas considerações adicionais que você pode desejar consultar ou que você deve estar ciente ao configurar uma lista de IP Permitidos.
  
### <a name="specifying-a-cidr-range-that-falls-outside-of-the-recommended-range"></a>Especificando uma faixa de CIDR que está fora da faixa recomendada

Para especificar um intervalo de endereços IP CIDR de/1 a/23, você deve criar uma regra de fluxo de emails que opere no intervalo de endereços IP que define o nível de confiança de spam (SCL) para **ignorar a filtragem de spam** (o que significa que todas as mensagens recebidas desse intervalo de endereços IP são definido como "não spam") e nenhuma filtragem adicional é realizada pelo serviço. No entanto, se qualquer um desses endereços IP aparecer em qualquer uma das listas de bloqueios proprietários da Microsoft ou em qualquer uma das listas de bloqueios de terceiros, essas mensagens ainda serão bloqueadas. Portanto, é altamente recomendável que você use o intervalo de endereços IP/24 para/32. 
  
Para criar essa regra de fluxo de emails, execute as etapas a seguir.
  
1. No EAC, navegue até **Fluxo de email** \> **Regras**.
    
2. Clique em ![Ícone Adicionar](media/ITPro-EAC-AddIcon.gif) e em seguida, selecione **Criar uma nova regra**.
    
3. Dê um nome à regra e então clique em **Mais opções**.
    
4. Em **Aplicar esta regra se**, selecione **O remetente** e então selecione **endereço IP em qualquer uma destas faixas ou correspondências exatas**.
    
5. Em **especificar endereços IP**, especifique o intervalo de endereços IP, clique em **Adicionar** ![ícone](media/ITPro-EAC-AddIcon.gif)de adição e, em seguida, clique em **OK**.
    
6. Na caixa **Faça o seguinte**, defina a ação, escolhendo **Modificar as propriedades da mensagem** e depois **definir o nível de confiança de spam (SCL)**. Na caixa **especificar SCL** , selecione **Ignorar filtragem de spam**, e clique em **ok**.
    
7. Se desejar, você pode optar por auditar a regra, testar a regra, ativar a regra durante um período de tempo específico e outras opções. Recomendamos testar a regra por um período antes de aplicá-la. [Procedimentos para regras de fluxo de emails no Exchange Server](https://docs.microsoft.com/en-us/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures) contém mais informações sobre essas seleções. 
    
8. Clique em **salvar** para salvar a regra. A regra é exibida na lista de regras. 
    
Depois de criar e impor a regra, o serviço ignora a filtragem de spam para o intervalo de endereços IP que você especificou.
  
### <a name="scoping-an-ip-allow-list-exception-for-a-specific-domain"></a>Controlando uma exceção da lista de IP Permitidos para um domínio específico

Em geral, recomendamos que você adicione endereços IP (ou faixas de endereço IP) para todos os domínios que você considerar seguro para a lista de IP Permitidos. No entanto, se você não quiser que a entrada da lista de IPs permitidos seja aplicada a todos os seus domínios, você pode criar uma regra de fluxo de emails (também conhecida como regra de transporte), exceto domínios específicos. 
  
Por exemplo, digamos que você tem três domínios: ContosoA.com, ContosoB.com e ContosoC.com, e você deseja adicionar o endereço IP (para simplificar, vamos usar 1.2.3.4) e pular a filtragem apenas para o domínio ContosoB.com. Você poderia criar uma lista de permissões de IP para 1.2.3.4, que define o nível de confiança de spam (SCL) a -1 (o que significa que é classificado como não-spam) em todos os domínios. Você pode criar uma regra de fluxo de emails que define o SCL de todos os domínios, exceto ContosoB.com para 0. Isso resulta na mensagem sendo reexaminada novamente para todos os domínios relacionados com o endereço IP, exceto para ContosoB.com que é o domínio listado como exceção na regra. ContosoB.com ainda tem um SCL de -1, o que significa ignorar filtragem, enquanto ContosoA.com e ContosoC.com têm SCLs de 0, o que significa que será examinado novamente pelo filtro de conteúdo.
  
Para fazer isso, execute as seguintes etapas:
  
1. No EAC, navegue até **Fluxo de email** \> **Regras**.
    
2. Clique em ![Ícone Adicionar](media/ITPro-EAC-AddIcon.gif) e em seguida, selecione **Criar uma nova regra**.
    
3. Dê um nome à regra e então clique em **Mais opções**.
    
4. Em **Aplicar esta regra se**, selecione **O remetente** e então selecione **endereço IP em qualquer uma destas faixas ou correspondências exatas**.
    
5. Na caixa **especificar endereços IP** , especifique o endereço IP ou o intervalo de endereços IP que você digitou na lista de permissões **** ![de IP,](media/ITPro-EAC-AddIcon.gif)clique em Adicionar ícone de adição e, em seguida, clique em **OK**.
    
6. Em **Faça**, configure a opção selecionando **Modificar as propriedades da mensagem** e então **defina o nível de confiança do spam (SCL)**. Na caixa **especificar SCL** , selecione **0**, e clique em **ok**.
    
7. Clique em **adicionar exceção**, e em **Exceto se**, selecione **O remetente** e selecione **domínio é**. 
    
8. Na caixa **especificar domínio** , digite o domínio para o qual deseja ignorar filtragem de spam, como **contosob.com**. Clique em **Adicionar** ![ícone](media/ITPro-EAC-AddIcon.gif) de adição para movê-lo para a lista de frases. Repita esta etapa se você deseja adicionar mais domínios como exceções e clique em **ok** após ter finalizado. 
    
9. Se desejar, você pode optar por auditar a regra, testar a regra, ativar a regra durante um período de tempo específico e outras opções. Recomendamos testar a regra por um período antes de aplicá-la. [Procedimentos para regras de fluxo de emails no Exchange Server](https://docs.microsoft.com/en-us/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures) contém mais informações sobre essas seleções. 
    
10. Clique em **salvar** para salvar a regra. A regra é exibida na lista de regras. 
    
Depois de criar e aplicar a regra, a filtragem de spam para o endereço IP ou intervalo de endereço IP que você especificou é ignorada apenas para a exceção de domínio que você digitou.
  
## <a name="new-to-office-365"></a>Começando a usar o Office 365?
<a name="sectionSection3"> </a>

||
|:-----|
|![O ícone pequeno do LinkedIn Learning](media/eac8a413-9498-4220-8544-1e37d1aaea13.png) **Começando a usar o Office 365?**         Descubra cursos em vídeo gratuitos para **Office 365 admins and IT pros**, oferecidos pelo LinkedIn Learning. |
   
## <a name="for-more-information"></a>Para saber mais
<a name="sectionSection4"> </a>

[Listas de remetentes seguros e remetentes bloqueados no Exchange Online](safe-sender-and-blocked-sender-lists-faq.md)
  
[Configurar suas políticas de filtro de spam](configure-your-spam-filter-policies.md)
  
[Configurar a política de spam de saída](configure-the-outbound-spam-policy.md)
  
[Como ajudar a garantir que uma mensagem não é marcada como spam](https://go.microsoft.com/fwlink/p/?LinkId=534224)
  
[Bloquear spam de email com o filtro de spam do Office 365 para evitar problemas de falsos negativos](https://go.microsoft.com/fwlink/p/?LinkId=534225)
  


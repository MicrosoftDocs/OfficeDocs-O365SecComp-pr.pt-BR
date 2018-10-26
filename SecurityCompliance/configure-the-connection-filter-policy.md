---
title: Configurar a política do filtro de conexão
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/24/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 6ae78c12-7bbe-44fa-ab13-c3768387d0e3
description: Para certificar-se de que os emails enviados de pessoas que confiáveis não não bloqueado, você pode usar a política de filtro de conexão para criar uma lista de permissões, também conhecido como uma lista de remetentes seguros, de endereços IP que você confia. Você também pode criar uma lista de remetentes bloqueados.
ms.openlocfilehash: 2f8ec3d01de4358d7394c68d0efae9222db08282
ms.sourcegitcommit: a07b91723bae9ecee2cb092bfbc5b208b30b11a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2018
ms.locfileid: "25793556"
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
    
- Para obter o endereço IP do remetente cujas mensagens você deseja permitir ou bloquear, você pode verificar o cabeçalho da mensagem de Internet. Procure o cabeçalho CIP conforme descrito em [cabeçalhos de mensagem antispam](anti-spam-message-headers.md). Para obter informações sobre como exibir o cabeçalho da mensagem em vários clientes de email, consulte o [Analisador de cabeçalho de mensagem](https://go.microsoft.com/fwlink/p/?LinkId=306583). 
    
- Mensagens de email enviadas de um endereço IP na lista de bloqueios de IP são rejeitadas, não são marcadas como spam, e nenhum filtro adicional ocorre.
    
- O procedimento de filtro de conexão a seguir também pode ser executado via o PowerShell remoto. Use o cmdlet [Get-HostedConnectionFilterPolicy](http://technet.microsoft.com/library/bd751db2-3f26-495b-8e5a-4fcab53b17fd.aspx) para examinar suas configurações e o [Set-HostedConnectionFilterPolicy](http://technet.microsoft.com/library/ccb5731b-3fca-4d69-a91f-5049ea963fac.aspx) para editar suas configurações de política de filtro de conexão. Para saber como usar o Windows PowerShell para se conectar ao Exchange Online Protection, consulte [Connect to Exchange Online Protection PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627290). Para saber como usar o Windows PowerShell para se conectar ao Exchange Online, consulte [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).
    
## <a name="use-the-eac-to-edit-the-default-connection-filter-policy"></a>Use o EAC para editar a política padrão de filtro de conexão
<a name="sectionSection1"> </a>

Crie uma Lista de IP Permitidos ou uma Lista de IP Bloqueados editando a política de filtro de conexão no EAC (Centro de Administração do Exchange). As configurações da política de filtro de conexão são aplicadas apenas às mensagens de entrada.
  
1. No centro de administração do Exchange (EAC), vá em **Proteção** \> **Filtro de conexão**, e clique duas vezes na política padrão.
    
2. Clique no item de menu **Filtragem de conexão** e crie as listas que quiser: uma Lista de IP Permitidos, uma Lista de IP Bloqueados ou ambas. 
    
    Para criar estas listas, clique em ![Ícone Adicionar](media/ITPro-EAC-AddIcon.gif). Na caixa de diálogo posterior, especifique a faixa de endereço ou endereço IP, e então clique em **ok**. Repita este processo para adicionar mais endereços. (Você também pode editar ou remover endereços IP após eles terem sido adicionados.)
    
    > [!NOTE]
    >  Se você adicionar um endereço IP às duas listas, emails enviados a partir do endereço IP é permitido. 

    Especifica endereços IP IPV4 no formato nnn. nnn onde nnn é um número de 0 a 255. Você também pode especificar intervalos de roteamento entre domínios (CIDR) no nnn.nnn.nnn.nnn/rr formato onde rr é um número de 24 a 32. Para especificar intervalos fora do intervalo de 24 a 32, consulte a [lista de considerações adicionais ao configurar permissões de IP](configure-the-connection-filter-policy.md#bkmk_addtionalconsiderationswhenconfiguringipallowlists). 

    Você pode especificar um máximo de 1.273 entradas, onde uma entrada é um único endereço IP ou um CIDR intervalo de endereços IP de/24 a/32. > Se você estiver enviando mensagens criptografadas por TLS, endereços IPv6 e intervalos de endereços não são suportados. 
  
3. Como opção, marque a caixa de seleção **Habilitar lista segura** para impedir que ausentes email de determinados remetentes conhecidos. Como? Microsoft se inscreve para fontes de terceiros de remetentes confiáveis. Usando essa lista segura significa que esses confiáveis remetentes não são marcados como spam por engano. É recomendável selecionar essa opção, pois ele deve reduzir o número de falsos positivos (BOM email que é classificada como spam) recebidos. 
    
4. Clique em **salvar**. Um resumo das suas configurações de política padrão aparece no painel à direita.
    
## <a name="additional-considerations-when-configuring-ip-allow-lists"></a>Considerações adicionais ao configurar listas de IP Permitidos
<a name="bkmk_addtionalconsiderationswhenconfiguringipallowlists"> </a>

A seguir estão algumas considerações adicionais que você pode desejar consultar ou que você deve estar ciente ao configurar uma lista de IP Permitidos.
  
### <a name="specifying-a-cidr-range-that-falls-outside-of-the-recommended-range"></a>Especificando uma faixa de CIDR que está fora da faixa recomendada

Para especificar um intervalo de endereços de IP CIDR de /1 ao /23, você deve criar uma regra de fluxo de email que opera em um intervalo de endereços IP que define o nível de confiança de spam (SCL) para **Ignorar a filtragem de spam** (o que significa que todas as mensagens recebidas neste intervalo de endereços IP são definido como não spam"") e nenhuma filtragem adicional é realizada pelo serviço). No entanto, se qualquer um desses endereços IP exibida em qualquer um bloco de proprietárias da Microsoft lista ou em qualquer um dos nosso bloco de terceiros listas, essas mensagens ainda serão bloqueadas. Portanto, recomenda que você use o intervalo de endereços IP /24 para /32. 
  
Para criar esta regra de fluxo de email, execute as seguintes etapas.
  
1. No EAC, navegue até **Fluxo de email** \> **Regras**.
    
2. Clique em ![Ícone Adicionar](media/ITPro-EAC-AddIcon.gif) e em seguida, selecione **Criar uma nova regra**.
    
3. Dê um nome à regra e então clique em **Mais opções**.
    
4. Em **Aplicar esta regra se**, selecione **O remetente** e então selecione **endereço IP em qualquer uma destas faixas ou correspondências exatas**.
    
5. Na **especificar endereços IP**, especifique o intervalo de endereços IP, clique em **Adicionar** ![ícone Adicionar](media/ITPro-EAC-AddIcon.gif)e clique em **okey**.
    
6. Na caixa **Faça o seguinte**, defina a ação, escolhendo **Modificar as propriedades da mensagem** e depois **definir o nível de confiança de spam (SCL)**. Na caixa **especificar SCL**, selecione **Ignorar filtragem de spam**, e clique em **ok**.
    
7. Se você quiser, você pode fazer as seleções para a regra de auditoria, testar a regra, ativar a regra durante um período de tempo específico e outras seleções. É recomendável testar a regra por um período antes de impor-lo. [Regras de procedimentos para fluxo de email no Exchange Server](https://docs.microsoft.com/en-us/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures) contém mais informações sobre essas seleções. 
    
8. Clique em **Salvar** para salvar a regra. A regra é exibida em sua lista de regras. 
    
Depois de criar e aplicar a regra, o serviço ignora a filtragem de spam para o intervalo de endereços IP que você especificou.
  
### <a name="scoping-an-ip-allow-list-exception-for-a-specific-domain"></a>Controlando uma exceção da lista de IP Permitidos para um domínio específico

Em geral, recomendamos que você adicione endereços IP (ou faixas de endereço IP) para todos os domínios que você considerar seguro para a lista de IP Permitidos. No entanto, se você não quer que sua lista de permissões de IP se aplique a todos os seus domínios, é possível criar uma regra de transporte que excetua domínios específicos. 
  
Por exemplo, digamos que você tem três domínios: ContosoA.com, ContosoB.com e ContosoC.com, e você deseja adicionar o endereço IP (para simplificar, vamos usar 1.2.3.4) e pular a filtragem apenas para o domínio ContosoB.com. Você poderia criar uma lista de permissões de IP para 1.2.3.4, que define o nível de confiança de spam (SCL) a -1 (o que significa que é classificado como não-spam) em todos os domínios. Você pode, então, criar uma regra de transporte que define o SCL para todos os domínios, exceto ContosoB.com a 0. Isso resulta na mensagem sendo reexaminada novamente para todos os domínios relacionados com o endereço IP, exceto para ContosoB.com que é o domínio listado como exceção na regra. ContosoB.com ainda tem um SCL de -1, o que significa ignorar filtragem, enquanto ContosoA.com e ContosoC.com têm SCLs de 0, o que significa que será examinado novamente pelo filtro de conteúdo.
  
Para fazer isso, execute as seguintes etapas:
  
1. No EAC, navegue até **Fluxo de email** \> **Regras**.
    
2. Clique em ![Ícone Adicionar](media/ITPro-EAC-AddIcon.gif) e em seguida, selecione **Criar uma nova regra**.
    
3. Dê um nome à regra e então clique em **Mais opções**.
    
4. Em **Aplicar esta regra se**, selecione **O remetente** e então selecione **endereço IP em qualquer uma destas faixas ou correspondências exatas**.
    
5. Na caixa **especificar endereços IP** , especifique o endereço IP ou intervalo de endereços IP você inseriu na lista de IPS permitidos, clique em **Adicionar** ![ícone Adicionar](media/ITPro-EAC-AddIcon.gif)e clique em **okey**.
    
6. Em **Faça**, configure a opção selecionando **Modificar as propriedades da mensagem** e então **defina o nível de confiança do spam (SCL)**. Na caixa **especificar SCL**, selecione **0**, e clique em **ok**.
    
7. Clique em **adicionar exceção**, e em **Exceto se**, selecione **O remetente** e selecione **domínio é**. 
    
8. Na caixa **Especificar domínio** , digite o domínio para o qual você deseja ignorar filtragem de spam, como **contosob.com**. Clique em **Adicionar** ![ícone Adicionar](media/ITPro-EAC-AddIcon.gif) para movê-lo à lista de frases. Repita essa etapa se desejar adicionar domínios adicionais como exceções e, em seguida, clique em **okey** quando terminar. 
    
9. Se você quiser, você pode fazer as seleções para a regra de auditoria, testar a regra, ativar a regra durante um período de tempo específico e outras seleções. É recomendável testar a regra por um período antes de impor-lo. [Regras de procedimentos para fluxo de email no Exchange Server](https://docs.microsoft.com/en-us/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures) contém mais informações sobre essas seleções. 
    
10. Clique em **Salvar** para salvar a regra. A regra é exibida em sua lista de regras. 
    
Depois de criar e aplicar a regra, a filtragem de spam para o endereço IP ou intervalo de endereço IP que você especificou é ignorada apenas para a exceção de domínio que você digitou.
  
## <a name="new-to-office-365"></a>Começando a usar o Office 365?
<a name="sectionSection3"> </a>

||
|:-----|
|![O ícone pequeno do LinkedIn Learning](media/eac8a413-9498-4220-8544-1e37d1aaea13.png) **Começando a usar o Office 365?**         Descubra cursos em vídeo gratuitos para **Office 365 admins and IT pros**, oferecidos pelo LinkedIn Learning. |
   
## <a name="for-more-information"></a>Para obter mais informações
<a name="sectionSection4"> </a>

[Remetentes seguros e bloqueados listas de remetentes no Exchange Online](safe-sender-and-blocked-sender-lists-faq.md)
  
[Configurar suas políticas de filtro de spam](configure-your-spam-filter-policies.md)
  
[Configurar a política de spam de saída](configure-the-outbound-spam-policy.md)
  
[Como ajudar a garantir que uma mensagem não é marcada como spam](https://go.microsoft.com/fwlink/p/?LinkId=534224)
  
[Bloquear spam de email com o filtro de spam do Office 365 para evitar problemas de falsos negativos](https://go.microsoft.com/fwlink/p/?LinkId=534225)
  


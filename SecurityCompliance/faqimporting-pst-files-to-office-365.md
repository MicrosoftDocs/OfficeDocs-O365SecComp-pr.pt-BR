---
title: Perguntas Frequentes sobre a importação de arquivos PST para o Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 2fe71b05-f5a2-4182-ade7-4dc5cabdfd51
description: 'Perguntas frequentes para administradores sobre como usar o serviço de importação do Office 365 para importar arquivos de PST do seu organizaiton às caixas de correio do Office 365. '
ms.openlocfilehash: 7230e68f896766df643f12b2a132f987670e9afa
ms.sourcegitcommit: eecf6f3aafbf460ee2ff9988f2b055e62b1fdb9d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25454048"
---
# <a name="faq-about-importing-pst-files-to-office-365"></a>Perguntas Frequentes sobre a importação de arquivos PST para o Office 365

**Este artigo destina-se a administradores. Você deseja importar arquivos PST para sua própria caixa de correio? Consulte o [email de importação, contatos e calendário de um arquivo. pst do Outlook](https://go.microsoft.com/fwlink/p/?LinkID=785075)**|
   
Aqui estão algumas perguntas frequentes sobre como usar o serviço de importação do Office 365 para importação em massa de arquivos PST às caixas de correio do Office 365. Para obter mais informações sobre como importar arquivos PST, consulte [Overview of importando arquivos PST para o Office 365](https://support.office.com/article/ba688e0a-0fcb-4bd7-8e57-2b669564ea84).
  
## <a name="using-network-upload-to-import-pst-files"></a>Usando o carregamento de rede para importar arquivos PST

Para obter instruções detalhadas, consulte [utilizar rede carregar para importar arquivos PST para o Office 365](use-network-upload-to-import-pst-files.md).
  
 **Quais permissões são necessárias para criar os trabalhos de importação no serviço de importação do Office 365?**
  
Você precisa ter a função caixa de correio importar exportar no Exchange Online para importar arquivos PST para caixas de correio do Office 365. Por padrão, essa função não é atribuída a nenhum grupo de função no Exchange Online. Você pode adicionar a função caixa de correio importar e exportar para o grupo de funções de gerenciamento da organização. Ou você pode criar um novo grupo de função, atribuir a função caixa de correio importar e exportar e, em seguida, adicione si mesmo ou para outros usuários como um membro. Para obter mais informações, consulte "Adicionar uma função para um grupo de funções" ou "Criar um grupo de funções" seções na [função de gerenciar grupos no Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=730688).
  
Além disso criar a importação de trabalhos no Office 365 Security &amp; Centro de conformidade, uma das opções a seguir devem ser verdadeiro:
  
- Você precisa ter a função de destinatários de email no Exchange Online. Por padrão, essa função é atribuída aos grupos de funções de gerenciamento de destinatário e gerenciamento da organização.
    
    Ou
    
- Você precisa ser um administrador global na sua organização do Office 365.
    
> [!TIP]
> Considere a criação de um novo grupo de função no Exchange Online que destina-se especificamente para importar arquivos PST para o Office 365. Para o nível mínimo de privilégios necessários para importar arquivos PST, atribua as funções de caixa de correio importar exportar e destinatários de email para o novo grupo de função e, em seguida, adicionar membros. 
  
 **Onde o carregamento de rede está disponível?**
  
Carregamento de rede está disponível atualmente nos Estados Unidos, Canadá, Brasil, o Reino Unido, França, Europa, Índia, Leste Asiático, Sudeste Asiático, Japão, República Popular da Coreia e Austrália. Carregamento de rede estará disponível em regiões mais breve.
  
 **Qual é o preço para importação dos arquivos PST usando o carregamento de rede?**
  
O uso de carregamento de rede para importar arquivos PST é livre.
  
Isso também significa que após arquivos PST são excluídos da área de armazenamento do Azure, não há mais exibi-los na lista de arquivos para um trabalho de importação concluída no Centro de administração do Office 365. Embora um trabalho de importação ainda pode ser listado na página **Importar dados para o Office 365** , a lista de arquivos PST pode estar vazia ao visualizar os detalhes de trabalhos de importação mais antigos. 
  
 **Qual versão do formato de arquivo PST é suportado para importar para o Office 365?**
  
Existem duas versões do formato de arquivo PST: ANSI e Unicode. Recomendamos a importação de arquivos que usam o formato de arquivo PST Unicode. No entanto, os arquivos que usam o formato de arquivo PST ANSI, como aquelas para idiomas que usam um caractere de byte duplo conjunto (DBCS), também podem ser importados para o Office 365. Para obter mais informações sobre como importar arquivos PST ANSI, consulte a etapa 4 na [rede de uso carregar para importar arquivos de PST da sua organização para o Office 365](use-network-upload-to-import-pst-files.md#step-4-create-the-pst-import-mapping-file).
  
Além disso, os arquivos PST do Outlook 2007 e versões posteriores podem ser importados para o Office 365.
  
 **Após carregar meus arquivos PST da área de armazenamento do Azure, quanto tempo são eles mantidos no Azure antes que eles estiver excluídos?**
  
Quando você usa o método de upload de rede para importar arquivos PST, você pode carregá-las para um contêiner de blob Azure chamado **ingestiondata**. Não se houver nenhum trabalho de importação em andamento na página **Importar** na segurança &amp; Centro de conformidade), e em seguida, todos os arquivos PST no contêiner **ingestiondata** no Azure são excluídos de 30 dias após o trabalho de importação mais recente foi criado na segurança &amp;Centro de conformidade. Isso também significa que você precisa criar um novo trabalho de importação na segurança &amp; arquivos do Centro de conformidade (descrito na etapa 5 as instruções de carregamento de rede) dentro de 30 dias do carregamento PST no Azure. 
  
Isso também significa que após arquivos PST são excluídos da área de armazenamento do Azure, não há mais exibi-los na lista de arquivos para um trabalho de importação concluída na segurança &amp; Centro de conformidade. Embora um trabalho de importação ainda pode estar listado na página **Importar** na segurança &amp; Centro de conformidade, a lista de arquivos PST pode estar vazia quando você exibir os detalhes de trabalhos de importação mais antigos. 
  
 **Quanto tempo leva para importar um arquivo PST para uma caixa de correio?**
  
Ela depende a capacidade de sua rede, mas normalmente leva várias horas para cada terabyte (TB) de dados sejam carregados para a área de armazenamento do Azure para sua organização. Depois que os arquivos PST são copiados para a área de armazenamento do Azure, um arquivo PST é importado para uma caixa de correio do Office 365 em uma taxa de pelo menos 24 GB por dia. Se essa taxa não atender às suas necessidades, você pode considerar outros métodos para migrar dados de email para o Office 365. Para obter mais informações, consulte [maneiras para migrar várias contas de email para o Office 365](https://support.office.com/article/ways-to-migrate-multiple-email-accounts-to-office-365-0a4913fe-60fb-498f-9155-a86516418842).
  
Se os diferentes arquivos PST são importados para caixas de correio de destino diferente, o processo de importação ocorre em paralelo; em outras palavras, cada par de PST/caixa de correio é importado simultaneamente. Da mesma forma, se vários arquivos PST são importados para a mesma caixa de correio, eles serão importados simultaneamente.
  
 **Há um limite de tamanho de mensagem ao importar arquivos PST?**
  
Sim. Se um arquivo PST contém um item de caixa de correio é maior do que 150 MB, o item será ignorado durante o processo de importação.
  
 **São as propriedades da mensagem, como quando a mensagem foi enviada ou recebida, a lista de destinatários e outras propriedades, preservadas quando os arquivos PST são importados para uma caixa de correio do Office 365?**
  
Sim. Os metadados da mensagem original não será alterado durante o processo de importação.
  
 **Há um limite no número de níveis em uma hierarquia de pastas para um arquivo PST que eu desejo importar uma caixa de correio?**
  
Sim. Você não pode importar um arquivo PST com 300 ou mais níveis de pastas aninhadas.
  
 **Pode usar o carregamento de rede para importar arquivos PST para uma caixa de correio inativa no Office 365?**
  
Sim, esse recurso está agora disponível.
  
 **Pode usar o carregamento de rede para importar arquivos PST para uma caixa de correio de arquivo morto online em uma implantação híbrida do Exchange?**
  
Sim, esse recurso está agora disponível.
  
 **Pode usar o carregamento de rede para importar arquivos PST para pastas públicas no Exchange Online?**
  
Não, você não pode importar arquivos PST a pastas públicas.
  
## <a name="using-drive-shipping-to-import-pst-files"></a>Usando o envio de unidade para importar arquivos PST

Para obter instruções detalhadas, consulte [usar unidade de envio para importar arquivos PST para o Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md).
  
 **Quais permissões são necessárias para criar os trabalhos de importação no serviço de importação do Office 365?**
  
Você precisa ser atribuído à função de caixa de correio importar exportar para importar arquivos PST para caixas de correio do Office 365. Por padrão, essa função não é atribuída a nenhum grupo de função no Exchange Online. Você pode adicionar a função caixa de correio importar e exportar para o grupo de funções de gerenciamento da organização. Ou você pode criar um novo grupo de função, atribuir a função caixa de correio importar e exportar e, em seguida, adicione si mesmo ou para outros usuários como um membro. Para obter mais informações, consulte "Adicionar uma função para um grupo de funções" ou "Criar um grupo de funções" seções na [função de gerenciar grupos no Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=730688).
  
Além disso criar a importação de trabalhos no Office 365 Security &amp; Centro de conformidade, uma das opções a seguir devem ser verdadeiro:
  
- Você precisa ter a função de destinatários de email no Exchange Online. Por padrão, essa função é atribuída aos grupos de funções de gerenciamento de destinatário e gerenciamento da organização.
    
    Ou
    
- Você precisa ser um administrador global na sua organização do Office 365.
    
> [!TIP]
> Considere a criação de um novo grupo de função no Exchange Online que destina-se especificamente para importar arquivos PST para o Office 365. Para o nível mínimo de privilégios necessários para importar arquivos PST, atribua as funções de caixa de correio importar exportar e destinatários de email para o novo grupo de função e, em seguida, adicionar membros. 
  
 **Onde unidade é envio disponível?**
  
Envio de unidade está disponível atualmente nos Estados Unidos, Canadá, Brasil, o Reino Unido, Europa, Índia, Leste Asiático, Sudeste Asiático, Japão, República Popular da Coreia e Austrália. Envio de unidade estarão disponível em regiões mais breve.
  
 **Envio de unidade oferece suporte a quais comerciais contratos de licenciamento?**
  
Unidade de envio para importar arquivos PST para o Office 365 está disponível por meio de um Microsoft EA (Enterprise Agreement). Envio de unidade não está disponível por meio de um Microsoft Products and Services contrato (MPSA).
  
 **Qual é o preço para usar a unidade de envio para importar arquivos PST para o Office 365?**
  
O custo para usar o envio de unidade para importar arquivos PST às caixas de correio do Office 365 é de US $ 2 por GB de dados. Por exemplo, se você enviar um disco rígido que contém 1.000 GB (1 TB) dos arquivos PST, o custo é de US $2.000. Você pode trabalhar com um parceiro para pagar a taxa de importação. Para obter informações sobre como encontrar um parceiro, consulte [Encontre seu parceiro do Office 365 ou um revendedor](https://go.microsoft.com/fwlink/p/?LinkId=785197).
  
 **Quais unidades de tipo de disco rígido são suportadas para o envio de unidade?**
  
Unidades de apenas de 2,5 polegadas de estado sólida (SSDs) ou 2,5 ou 3,5 polegadas SATA II/III discos rígidos internos são compatíveis para uso com o serviço de importação do Office 365. Você pode usar os discos rígidos até 10 TB. Trabalhos de importação, apenas o primeiro volume de dados no disco rígido será processado. O volume de dados deve ser formatado com o NTFS. Ao copiar dados para um disco rígido, você pode anexá-lo diretamente usando um SSD de 2,5 polegadas ou 2.5 ou 3,5 polegadas conector do SATA II/III ou você pode anexá-lo externamente usando uma SSD externo de 2,5 polegadas ou adaptador USB do SATA II/III de polegada 2.5 ou 3.5.
  
> [!IMPORTANT]
> Discos rígidos externos que vêm com um adaptador USB interno não são suportados pelo serviço de importação do Office 365. Além disso, o disco de maiusculas e minúsculas de um disco rígido externo não pode ser usado. Por favor, não vêm discos rígidos externos. 
  
 **Quantos discos rígidos pode entregar para um trabalho de importação única?**
  
Você pode entregar um máximo de 10 unidades de disco rígido para um trabalho único de importação.
  
 **Depois que eu enviar meu disco rígido, quanto tempo leva para chegar ao centro de dados da Microsoft?**
  
Isso dependerá de algumas coisas, como a proximidade seu centro de dados da Microsoft e que tipo de opção de envio é usada para transportar o seu disco rígido (como, entrega no próximo dia, dois dias entrega ou terra entrega). Com a maioria dos shippers, você pode usar o número de rastreamento para rastrear o status de sua entrega.
  
 **Depois que o meu disco rígido chega no Centro de dados da Microsoft, quanto tempo leva para carregar meus arquivos PST no Azure?**
  
Depois que o seu disco rígido é recebido no Centro de dados da Microsoft, ela levará entre 7 a 10 dias de negócios para carregar os arquivos PST para a área de armazenamento do Microsoft Azure para sua organização. Os arquivos PST serão carregados para um contêiner de blob Azure chamado **ingestiondata**. 
  
 **Quanto tempo leva para importar um arquivo PST para uma caixa de correio?**
  
Depois que os arquivos PST são carregados para a área de armazenamento do Azure, Office 365 analisa os dados nos arquivos PST (em uma forma segura e) para identificar a idade dos itens e os tipos de mensagem diferente incluídos nos arquivos PST. Quando essa análise estiver concluída, você terá a opção de importar todos os dados nos arquivos PST ou filtros de conjunto que controlam quais dados obtém importados. Depois de iniciar o trabalho de importação, um arquivo PST é importado para uma caixa de correio do Office 365 em uma taxa de pelo menos 24 GB por dia. Se essa taxa não atender às suas necessidades, você pode considerar outros métodos para importar dados de email para o Office 365. Para obter mais informações, consulte [maneiras para migrar várias contas de email para o Office 365](https://support.office.com/article/ways-to-migrate-multiple-email-accounts-to-office-365-0a4913fe-60fb-498f-9155-a86516418842).
  
Se os diferentes arquivos PST são importados para caixas de correio de destino diferente, o processo de importação ocorre em paralelo; em outras palavras, cada par de PST/caixa de correio é importado simultaneamente. Da mesma forma, se vários arquivos PST são importados para a mesma caixa de correio, eles serão importados simultaneamente.
  
 **Depois que o Microsoft carrega Meus arquivos PST no Azure, quanto tempo são eles mantidos no Azure antes que eles estiver excluídos?**
  
Todos os arquivos PST no local de armazenamento do Windows Azure para sua organização (no contêiner de blob denominado **ingestiondata** ), são excluídas de 30 dias após o trabalho de importação mais recente foi criado na página **Importar** na segurança &amp; Centro de conformidade. 
  
Isso também significa que após arquivos PST são excluídos da área de armazenamento do Azure, não há mais exibi-los na lista de arquivos para um trabalho de importação concluída na segurança &amp; Centro de conformidade. Embora um trabalho de importação ainda pode estar listado na página **Importar** na segurança &amp; Centro de conformidade, a lista de arquivos PST pode estar vazia quando você exibir os detalhes de trabalhos de importação mais antigos. 
  
 **Qual versão do formato de arquivo PST é suportado para importar para o Office 365?**
  
Existem duas versões do formato de arquivo PST: ANSI e Unicode. Recomendamos a importação de arquivos que usam o formato de arquivo PST Unicode. No entanto, os arquivos que usam o formato de arquivo PST ANSI, como aquelas para idiomas que usam um caractere de byte duplo conjunto (DBCS), também podem ser importados para o Office 365. Para obter mais informações sobre como importar arquivos PST ANSI, consulte a etapa 3 em [usar unidade de envio para importar arquivos PST para o Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md#step-3-create-the-pst-import-mapping-file).
  
Além disso, os arquivos PST do Outlook 2007 e versões posteriores podem ser importados para o Office 365.
  
 **Há um limite de tamanho de mensagem ao importar arquivos PST?**
  
Sim. Se um arquivo PST contém um item de caixa de correio é maior do que 150 MB, o item será ignorado durante o processo de importação.
  
 **São as propriedades da mensagem, como quando a mensagem foi enviada ou recebida, a lista de destinatários e outras propriedades, preservadas quando os arquivos PST são importados para uma caixa de correio do Office 365?**
  
Sim. Os metadados da mensagem original não será alterado durante o processo de importação
  
 **Há um limite no número de níveis em uma hierarquia de pastas para um arquivo PST que eu desejo importar uma caixa de correio?**
  
Sim. Você não pode importar um arquivo PST com 300 ou mais níveis de pastas aninhadas.
  
 **Pode usar o envio de unidade para importar arquivos PST para uma caixa de correio inativa no Office 365?**
  
Sim, esse recurso está agora disponível.
  
 **Pode usar o envio de unidade para importar arquivos PST para uma caixa de correio de arquivo morto online em uma implantação híbrida do Exchange?**
  
Sim, esse recurso está agora disponível.
  
 **Pode usar o envio de unidade para importar arquivos PST para pastas públicas no Exchange Online?**
  
Não, você não pode importar arquivos PST a pastas públicas.
  
 **Microsoft pode revelar meu disco rígido antes que eles envie para mim?**
  
Não, a Microsoft não pode revelar discos rígidos antes de enviá-los novamente aos clientes. Unidades de disco rígido são retornadas para você no mesmo estado em que estavam quando eles foram recebidos pela Microsoft.
  
 **Pode Microsoft destruir meu disco rígido, em vez de envio-lo de volta para mim?**
  
Não, a Microsoft não é possível destruir seu disco rígido. Unidades de disco rígido são retornadas para você no mesmo estado em que estavam quando eles foram recebidos pela Microsoft.
  
 **Quais serviços courier são suportados para o envio de retorno?**
  
Se você for um cliente nos Estados Unidos ou Europa, a Microsoft usa FedEx para retornar o disco rígido. Para todas as outras regiões, a Microsoft usa DHL.
  
 **Quais são os custos de envio de retorno?**
  
Retorne os custos de remessa variam, dependendo de sua proximidade que você acompanha seu disco rígido para o Centro de dados do Microsoft. Microsoft será bill sua conta FedEx ou DHL para retornar o disco rígido. O custo de envio de retorno é responsabilidade sua.
  
 **Pode usar um serviço de envio de courier personalizados, como FedEx personalizado envio entregar meu disco rígido para a Microsoft?**
  
Sim.
  
 **Se tiver o envio meu disco rígido para outro país, existe alguma coisa que preciso fazer?**
  
O disco rígido que ser enviada para a Microsoft pode precisar cruzar as fronteiras internacionais. Se este for o caso, você está responsável por garantir que o disco rígido e os dados que nele contidos são importados e/ou exportados de acordo com as leis aplicáveis. Antes de entregar um disco rígido, verifique com os consultores para verificar se sua unidade e dados legalmente podem ser enviados para o Centro de dados da Microsoft especificado. Isso ajudará a garantir que ele atingir Microsoft oportunamente.

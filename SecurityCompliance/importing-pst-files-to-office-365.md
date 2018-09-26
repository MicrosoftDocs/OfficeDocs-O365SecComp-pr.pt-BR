---
title: Visão geral da importação dos arquivos PST da organização para o Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: overview
f1_keywords:
- ms.o365.cc.IngestionHelp
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid: MET150
ms.assetid: ba688e0a-0fcb-4bd7-8e57-2b669564ea84
description: 'Para administradores: Aprenda a usar o serviço de importação de segurança do Office 365 &amp; Centro de conformidade para dados de email (arquivos. PST) de importação em massa para caixas de correio do usuário no Exchange Online. Este tópico fornece perguntas frequentes e explica como funciona o processo de importação de PST.'
ms.openlocfilehash: 2bd58b879d9d4d1ff9d3d2c6c8680a0171d42689
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038014"
---
# <a name="overview-of-importing-your-organization-pst-files-to-office-365"></a>Visão geral da importação dos arquivos PST da organização para o Office 365

> [!NOTE]
> Este artigo destina-se a administradores. Você está tentando importar arquivos PST para sua própria caixa de correio? Consulte o [email de importação, contatos e calendário de um arquivo. pst do Outlook](https://go.microsoft.com/fwlink/p/?LinkID=785075)

Você pode usar o serviço de importação de segurança do Office 365 &amp; arquivos do Centro de conformidade para rapidamente importação em massa-PST às caixas de correio Exchange Online em sua organização do Office 365. Há duas maneiras que você pode importar arquivos PST para o Office 365:
   
- **Carregar de rede** ![Carregamento de nuvem](media/54ab16ee-3822-4551-abef-3d926f4e1c01.png) -carregar os arquivos PST na rede para um local de armazenamento temporário de Azure na nuvem da Microsoft. Em seguida, você deve usar o serviço Office 365 importar para importar os dados de PST às caixas de correio em sua organização do Office 365. 

- **Unidade de envio** ![Disco rígido](media/e72b76f3-1f73-4296-b749-c325d95d9ef6.png) - copie os arquivos PST para uma unidade de disco BitLocker criptografadas e, depois, enviar fisicamente unidade à Microsoft. Quando a Microsoft recebe o disco rígido, o pessoal do data center carregar os dados para um local de armazenamento temporário de Azure na nuvem da Microsoft. Em seguida, você deve usar o serviço Office 365 importar para importar os dados para caixas de correio em sua organização do Office 365.

## <a name="step-by-step-instructions"></a>Instruções passo a passo
  
Consulte um dos seguintes tópicos para obter instruções detalhadas e passo a passo para a importação em massa de arquivos PST de sua organização para o Office 365. 
   
- [Usar o carregamento de rede para importar arquivos PST para o Office 365](use-network-upload-to-import-pst-files.md)
- [Usar o envio de unidade para importar arquivos PST para o Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md)

## <a name="how-importing-pst-files-works"></a>Como funciona a importação de arquivos PST

Aqui está uma ilustração e uma descrição do processo de importação completa do PST. A ilustração mostra o fluxo de trabalho principal e destaca as diferenças entre o carregamento de rede e a unidade de métodos de envio.
  
![Fluxo de trabalho do processo de importação de PST](media/76997b69-67d7-433a-a0ca-9389f85a36a1.png)
  
1. **Download de arquivo PST importar ferramentas e o local de armazenamento do Azure principais para private** - a primeira etapa é para baixar a chave de acesso e a ferramenta usada para carregar os arquivos PST ou copiá-los para um disco rígido. Você obtê-los da página **importação** na segurança do Office 365 &amp; Centro de conformidade. A chave fornece a você (ou pessoal do Microsoft data center no caso de envio de unidade) com as permissões necessárias para carregar arquivos PST para um local de armazenamento seguro e privadas do Azure. Essa chave de acesso é exclusivo para a sua organização e ajuda a impedir o acesso não autorizado aos seus arquivos PST após terem sido carregadas para a nuvem da Microsoft. Observe que a importação dos arquivos PST para o Office 365 não exige sua organização tenha uma assinatura Azure separada. 
    
2. **Carregar ou copiar o PST arquivos** - o próximo passo depende se você estiver usando o carregamento de rede ou o envio de unidade para importar arquivos PST. Em ambos os casos, você usará a ferramenta e a chave de armazenamento seguro que você obteve na etapa anterior.
    
    - **Carregar de rede** A ferramenta de AzCopy.exe (baixada na etapa 1) é usada para carregar e armazenar seus arquivos PST em um local de armazenamento do Azure de nuvem da Microsoft. Observe que o local de armazenamento do Azure que você carregar arquivos PST em reside no mesmo datacenter Microsoft regional onde a sua organização do Office 365 está localizada. 
    
      Para carregá-las, os arquivos PST que você deseja importar para o Office 365 precisam estar localizado em um compartilhamento de arquivo ou o servidor de arquivos na sua organização.
    
    - **Unidade de envio** A ferramenta de WAImportExport.exe (baixada na etapa 1) é usada para copiar os arquivos PST para o disco rígido. Essa ferramenta criptografa o disco rígido com o BitLocker e, em seguida, copia os PSTs no disco rígido. Como o carregamento de rede, os arquivos PST que você deseja copiar para o disco rígido têm a ser localizado em um compartilhamento de arquivo ou o servidor de arquivos na sua organização.
    
3. **Criar um arquivo de mapeamento de importação de PST** - após os arquivos PST foram carregados no local de armazenamento do Azure ou copiados para uma unidade de disco rígida, a próxima etapa é criar um arquivo (CSV) de valores separados por vírgula que especifica quais arquivos PST de caixas de correio de usuário será importados para (um término de um arquivo PST pode ser importado para a caixa de correio principal do usuário ou de suas caixas de correio de arquivo morto). O serviço Office 365 importar usará as informações na importação dos arquivos PST. 
    
4. **Trabalho de importação de criar um PST** - a próxima etapa é criar um trabalho de importação de PST na página **Importar** na segurança &amp; Centro de conformidade e enviar o arquivo de mapeamento de importação de PST criado na etapa anterior. Para carregamento de rede (porque os arquivos PST carregados no Azure) Office 365 analisa os dados nos arquivos PST e, em seguida, oferece a oportunidade de definir os filtros que controlam quais dados realmente obtém importados para as caixas de correio especificadas no arquivo de mapeamento de importação de PST. 
    
    Para o envio de unidade, algumas coisas adicionais aconteceram nesse ponto no processo.
    
    - Você entregar fisicamente o disco rígido para um data center da Microsoft (o endereço de envio do Centro de dados da Microsoft é exibido quando o trabalho de importação é criado)
    
    - Quando a Microsoft recebe o disco rígido, o pessoal do data center carregará os arquivos PSTs no disco rígido para o local de armazenamento do Azure para sua organização. Conforme explicado anteriormente, seus arquivos PST são carregados para um local de armazenamento do Azure que reside no mesmo datacenter regional Microsoft onde a sua organização do Office 365 está localizada.
    
      > [!NOTE]
      > Os arquivos PST no disco rígido são carregados no Azure dentro de 7 a 10 dias de negócios depois que a Microsoft recebe o disco rígido. 
  
      Como o processo de carregamento de rede, o Office 365, em seguida, analisa os dados nos arquivos PST e lhe dá a oportunidade de definir os filtros que controlam quais dados realmente obtém importados para as caixas de correio especificadas no arquivo de mapeamento de importação de PST.
    
    - Microsoft envia o disco rígido de volta para você. 
    
5. **Filtrar os dados de PST que serão importados para caixas de correio** - depois que o trabalho de importação for criado (e depois que os arquivos PST de um trabalho de envio de unidade são carregados para o local de armazenamento do Azure) Office 365 analisa os dados nos arquivos PST (com segurança e com segurança) por identificando a idade dos itens e os tipos de mensagem diferente incluídos nos arquivos PST. Quando a análise for concluída e os dados estão prontos para importação, você tem a opção para importar todos os dados contidos nos arquivos PST ou você pode reduzir os dados são importados, definindo filtros que controlam quais dados obtém importados. 
    
6. **Iniciar o trabalho de importação de PST** - depois que o trabalho de importação é iniciado, o Office 365 usa as informações no arquivo de mapeamento de importação PST na importação dos arquivos de PSTs do local de armazenamento do Azure s às caixas de correio do usuário. Informações de status sobre o trabalho de importação (incluindo informações sobre cada arquivo PST sendo importado) são exibidas na página **Importar** na segurança &amp; Centro de conformidade. Quando o trabalho de importação for concluído, o status do trabalho for definido como **Complete**.
  
## <a name="why-import-email-data-to-office-365"></a>Por que importar dados de email para o Office 365?

- A importação de arquivos PST às caixas de correio do usuário é uma maneira de migrar email de sua organização para o Office 365.
    
- Você pode usar o recurso de [Importação inteligente](filter-data-when-importing-pst-files.md) para filtrar os itens em arquivos PST que realmente obtém importou para as caixas de correio de destino. Permite que os dados são importados, definindo filtros que você trim controla quais dados obtém importados. 
    
- Importar dados de email para o Office 365 ajuda a atender às necessidades de conformidade da sua organização, permitindo que você:
    
  - Habilite [caixas de correio de arquivamento](enable-archive-mailboxes.md) e o [arquivamento ilimitado](unlimited-archiving.md) dar aos usuários de espaço de armazenamento de caixa de correio adicional. 
    
  - Colocar caixas de correio em [Retenção de litígio](https://go.microsoft.com/fwlink/?linkid=841243) para reter o conteúdo. 
    
  - Use a [ferramenta de pesquisa de conteúdo](content-search.md) de pesquisa de conteúdo de caixa de correio. 
    
  - Use [os casos de eDiscovery](ediscovery-cases.md) para gerenciar investigações legais da sua organização 
    
  - Usar [políticas de retenção](retention-policies.md) na segurança &amp; Centro de conformidade para controlar quanto tempo o conteúdo de caixa de correio é mantido e, em seguida, exclua o conteúdo depois que o período de retenção expira. 
    
- Importar dados para o Office 365 ajuda a proteger contra perda de dados. Dados de email que serão importados para o Office 365 herda os recursos de alta disponibilidade do Exchange Online.
    
- Dados de email no Office 365 estão disponíveis para usuários de todos os dispositivos, porque ele é armazenado na nuvem.
    
## <a name="importing-sharepoint-data-to-office-365"></a>Importando dados do SharePoint para o Office 365

Você também pode importar arquivos e documentos para contas do OneDrive e de sites do SharePoint em sua organização do Office 365. Para obter mais informações, consulte [carregar conteúdo local no SharePoint Online usando os cmdlets do PowerShell](https://docs.microsoft.com/sharepointmigration/upload-on-premises-content-to-sharepoint-online-using-powershell-cmdlets).


## <a name="frequently-asked-questions-about-importing-pst-files-to-office-365"></a>Perguntas frequentes sobre como importar arquivos PST para o Office 365
  
Aqui estão algumas perguntas frequentes sobre como usar o serviço Office 365 importar para importação em massa de arquivos PST às caixas de correio do Office 365. 
  
- [Usando o carregamento de rede para importar arquivos PST](#using-network-upload-to-import-pst-files)
  
- [Usando o envio de unidade para importar arquivos PST](#using-drive-shipping-to-import-pst-files)
  
### <a name="using-network-upload-to-import-pst-files"></a>Usando o carregamento de rede para importar arquivos PST

 **Quais permissões são necessárias para criar os trabalhos de importação no serviço de importação do Office 365?**
  
Você precisa ter a função caixa de correio importar exportar no Exchange Online para importar arquivos PST para caixas de correio do Office 365. Por padrão, essa função não é atribuída a nenhum grupo de função no Exchange Online. Você pode adicionar a função caixa de correio importar e exportar para o grupo de funções de gerenciamento da organização. Ou você pode criar um novo grupo de função, atribuir a função caixa de correio importar e exportar e, em seguida, adicione si mesmo ou para outros usuários como um membro. Para obter mais informações, consulte "Adicionar uma função para um grupo de funções" ou "Criar um grupo de funções" seções na [função de gerenciar grupos no Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=730688).
  
Além disso criar a importação de trabalhos no Office 365 Security &amp; Centro de conformidade, uma das opções a seguir devem ser verdadeiro:
  
- Você precisa ter a função de destinatários de email no Exchange Online. Por padrão, essa função é atribuída aos grupos de funções de gerenciamento de destinatário e gerenciamento da organização.
    
    Ou
    
- Você precisa ser um administrador global na sua organização do Office 365.
    
> [!TIP]
> Considere a criação de um novo grupo de função no Exchange Online que destina-se especificamente para importar arquivos PST para o Office 365. Para o nível mínimo de privilégios necessários para importar arquivos PST, atribua as funções de caixa de correio importar exportar e destinatários de email para o novo grupo de função e, em seguida, adicionar membros. 
  
 **Onde o carregamento de rede está disponível?**
  
Carregamento de rede está disponível atualmente nos Estados Unidos, Canadá, Brasil, o Reino Unido, Europa, Índia, Leste Asiático, Sudeste Asiático, Japão, República Popular da Coreia e Austrália. Carregamento de rede estará disponível em regiões mais breve.
  
 **Qual é o preço para importação dos arquivos PST usando o carregamento de rede?**
  
O uso de carregamento de rede para importar arquivos PST é livre.
  
Isso também significa que após arquivos PST são excluídos da área de armazenamento do Azure, não há mais exibi-los na lista de arquivos para um trabalho de importação concluída no Centro de administração do Office 365. Embora um trabalho de importação ainda pode ser listado na página **Importar dados para o Office 365** , a lista de arquivos PST pode estar vazia ao visualizar os detalhes de trabalhos de importação mais antigos. 
  
 **Qual versão do formato de arquivo PST é suportado para importar para o Office 365?**
  
Existem duas versões do formato de arquivo PST: ANSI e Unicode. Recomendamos a importação de arquivos que usam o formato de arquivo PST Unicode. No entanto, os arquivos que usam o formato de arquivo PST ANSI, como aquelas para idiomas que usam um caractere de byte duplo conjunto (DBCS), também podem ser importados para o Office 365. Para obter mais informações sobre como importar arquivos PST ANSI, consulte a etapa 4 na [rede de uso carregar para importar arquivos PST para o Office 365](https://go.microsoft.com/fwlink/p/?LinkId=823074).
  
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
  
### <a name="using-drive-shipping-to-import-pst-files"></a>Usando o envio de unidade para importar arquivos PST

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
  
Depois que o seu disco rígido é recebido no Centro de dados da Microsoft, ela levará entre 7 a 10 dias de negócios para carregar os arquivos PST para a área de armazenamento do Microsoft Azure para sua organização. Os arquivos PST serão carregados para um contêiner de blob Azure denominado `ingestiondata`. 
  
 **Quanto tempo leva para importar um arquivo PST para uma caixa de correio?**
  
Depois que os arquivos PST são carregados para a área de armazenamento do Azure, Office 365 analisa os dados nos arquivos PST (em uma forma segura e) para identificar a idade dos itens e os tipos de mensagem diferente incluídos nos arquivos PST. Quando essa análise estiver concluída, você terá a opção de importar todos os dados nos arquivos PST ou filtros de conjunto que controlam quais dados obtém importados. Depois de iniciar o trabalho de importação, um arquivo PST é importado para uma caixa de correio do Office 365 em uma taxa de pelo menos 24 GB por dia. Se essa taxa não atender às suas necessidades, você pode considerar outros métodos para importar dados de email para o Office 365. Para obter mais informações, consulte [maneiras para migrar várias contas de email para o Office 365](https://support.office.com/article/ways-to-migrate-multiple-email-accounts-to-office-365-0a4913fe-60fb-498f-9155-a86516418842).
  
Se os diferentes arquivos PST são importados para caixas de correio de destino diferente, o processo de importação ocorre em paralelo; em outras palavras, cada par de PST/caixa de correio é importado simultaneamente. Da mesma forma, se vários arquivos PST são importados para a mesma caixa de correio, eles serão importados simultaneamente.
  
 **Depois que o Microsoft carrega Meus arquivos PST no Azure, quanto tempo são eles mantidos no Azure antes que eles estiver excluídos?**
  
Todos os arquivos PST no local de armazenamento do Windows Azure para sua organização (no contêiner de blob denominado `ingestiondata`), serão excluídos 30 dias após o trabalho de importação mais recente foi criado na página **Importar** na segurança &amp; Centro de conformidade. 
  
Isso também significa que após arquivos PST são excluídos da área de armazenamento do Azure, não há mais exibi-los na lista de arquivos para um trabalho de importação concluída na segurança &amp; Centro de conformidade. Embora um trabalho de importação ainda pode estar listado na página **Importar** na segurança &amp; Centro de conformidade, a lista de arquivos PST pode estar vazia quando você exibir os detalhes de trabalhos de importação mais antigos. 
  
 **Qual versão do formato de arquivo PST é suportado para importar para o Office 365?**
  
Existem duas versões do formato de arquivo PST: ANSI e Unicode. Recomendamos a importação de arquivos que usam o formato de arquivo PST Unicode. No entanto, os arquivos que usam o formato de arquivo PST ANSI, como aquelas para idiomas que usam um caractere de byte duplo conjunto (DBCS), também podem ser importados para o Office 365. Para obter mais informações sobre como importar arquivos PST ANSI, consulte a etapa 3 em [usar unidade de envio para importar os arquivos PST da organização para o Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md#step-3-create-the-pst-import-mapping-file).
  
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

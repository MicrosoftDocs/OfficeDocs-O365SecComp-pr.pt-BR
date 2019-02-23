---
title: PERGUNTAS FREQUENTEs sobre a importação de arquivos PST para o Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 2fe71b05-f5a2-4182-ade7-4dc5cabdfd51
description: 'Perguntas frequentes para administradores sobre como usar o serviço de importação do Office 365 para importar os arquivos PST do Organizaiton para caixas de correio do Office 365. '
ms.openlocfilehash: 9ca2e206a1d06c1398181c51e41b4dc68d8d965c
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218401"
---
# <a name="faq-about-importing-pst-files-to-office-365"></a>PERGUNTAS FREQUENTEs sobre a importação de arquivos PST para o Office 365

**Este artigo é para administradores. Deseja importar arquivos PST para sua própria caixa de correio? ConFira [importar email, contatos e calendário de um arquivo. pst do Outlook](https://go.microsoft.com/fwlink/p/?LinkID=785075)**|
   
Aqui estão algumas perguntas frequentes sobre como usar o serviço de importação do Office 365 para importar arquivos PST em massa para caixas de correio do Office 365. Para obter mais informações sobre como importar arquivos PST, consulte [visão geral da importação de arquivos pst para o Office 365](https://support.office.com/article/ba688e0a-0fcb-4bd7-8e57-2b669564ea84).
  
## <a name="using-network-upload-to-import-pst-files"></a>Usando o carregamento de rede para importar arquivos PST

Para obter instruções passo a passo, consulte [usar o carregamento de rede para importar arquivos pst para o Office 365](use-network-upload-to-import-pst-files.md).
  
 **Quais permissões são necessárias para criar trabalhos de importação no serviço de importação do Office 365?**
  
Você deve ser atribuído à função de exportação de importação de caixa de correio no Exchange Online para importar arquivos PST para caixas de correio do Office 365. Por padrão, essa função não é atribuída a nenhum grupo de função no Exchange Online. Você pode adicionar a função de exportação de importação de caixa de correio ao grupo de funções Gerenciamento da organização. Ou você pode criar um novo grupo de função, atribua a função de exportação de importação de caixa de correio e, em seguida, adicione a si mesmo ou a outros usuários como um membro. Para obter mais informações, consulte as seções "adicionar uma função a um grupo de funções" ou "criar um grupo de função" em [gerenciar grupos de função no Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=730688).
  
Além disso, para criar trabalhos de importação no centro de &amp; conformidade de segurança do Office 365, um dos seguintes deve ser verdadeiro:
  
- Você precisa receber a função de destinatários de email no Exchange Online. Por padrão, essa função é atribuída aos grupos de gerenciamento da organização e de funções de gerenciamento de destinatários.
    
    Ou
    
- Você deve ser um administrador global em sua organização do Office 365.
    
> [!TIP]
> Considere a criação de um novo grupo de função no Exchange Online destinado especificamente à importação de arquivos PST para o Office 365. Para obter o nível mínimo de privilégios necessários para importar arquivos PST, atribua as funções de importação de caixa de correio e destinatários de email ao novo grupo de funções e, em seguida, adicione membros. 
  
 **Onde o carregamento de rede está disponível?**
  
O carregamento de rede está disponível atualmente nos Estados Unidos, Canadá, Brasil, Reino Unido, França, Europa, Índia, leste asiático, Sudeste Asiático, Japão, República da Coréia e Austrália. O carregamento de rede estará disponível em mais regiões em breve.
  
 **Qual é o preço da importação de arquivos PST usando o carregamento de rede?**
  
Usar o carregamento de rede para importar arquivos PST é gratuito.
  
Isso também significa que, após os arquivos PST serem excluídos da área de armazenamento do Azure, eles não serão mais exibidos na lista de arquivos para um trabalho de importação concluído no centro de administração do Office 365. Embora um trabalho de importação ainda possa ser listado na página **importar dados para o Office 365** , a lista de arquivos PST pode estar vazia quando você exibir os detalhes de trabalhos de importação mais antigos. 
  
 **Qual versão do formato de arquivo PST é suportada para importar para o Office 365?**
  
Há duas versões do formato de arquivo PST: ANSI e Unicode. É recomendável importar arquivos que usam o formato de arquivo PST Unicode. No enTanto, os arquivos que usam o formato de arquivo PST ANSI, como aqueles para idiomas que usam um conjunto de caracteres de dois bytes (DBCS), também podem ser importados para o Office 365. Para obter mais informações sobre a importação de arquivos PST ANSI, consulte a etapa 4 em [usar o carregamento de rede para importar arquivos pst da sua organização para o Office 365](use-network-upload-to-import-pst-files.md#step-4-create-the-pst-import-mapping-file).
  
Além disso, os arquivos PST do Outlook 2007 e versões posteriores podem ser importados para o Office 365.
  
 **Após carregar arquivos PST para a área de armazenamento do Azure, por quanto tempo eles são mantidos no Azure antes de serem excluídos?**
  
Quando você usa o método de carregamento de rede para importar arquivos PST, você os carrega em um contêiner de blob do Azure chamado **ingestiondata**. Se não houver trabalhos de importação em andamento na página de **importação** no centro de &amp; conformidade de segurança), todos os arquivos pst no contêiner do **ingestiondata** no Azure serão excluídos 30 dias após o trabalho de importação mais recente ter sido criado na segurança &amp;Centro de conformidade. Isso também significa que você precisa criar um novo trabalho de importação no centro &amp; de conformidade de segurança (descrito na etapa 5 nas instruções de upload de rede) em 30 dias de upload de arquivos pst para o Azure. 
  
Isso também significa que, após os arquivos PST serem excluídos da área de armazenamento do Azure, eles não serão mais exibidos na lista de arquivos para um trabalho de importação concluído &amp; no centro de conformidade de segurança. Embora um trabalho de importação ainda possa estar listado na página de **importação** no centro &amp; de conformidade de segurança, a lista de arquivos PST pode estar vazia quando você exibir os detalhes de trabalhos de importação mais antigos. 
  
 **Quanto tempo leva para importar um arquivo PST para uma caixa de correio?**
  
Ele depende da capacidade da sua rede, mas geralmente leva algumas horas para que cada terabyte (TB) de dados seja carregado na área de armazenamento do Azure para sua organização. Depois que os arquivos PST forem copiados para a área de armazenamento do Azure, um arquivo PST será importado para uma caixa de correio do Office 365 em uma taxa de pelo menos 24 GB por dia. Se essa taxa não atender às suas necessidades, você poderá considerar outros métodos para migrar dados de email para o Office 365. Para obter mais informações, consulte [maneiras de migrar várias contas de email para o Office 365](https://support.office.com/article/ways-to-migrate-multiple-email-accounts-to-office-365-0a4913fe-60fb-498f-9155-a86516418842).
  
Se arquivos PST diferentes forem importados para caixas de correio de destino diferentes, o processo de importação ocorrerá em paralelo; em outras palavras, cada par de PST/caixa de correio é importado simultaneamente. Da mesma forma, se vários arquivos PST forem importados para a mesma caixa de correio, eles serão importados simultaneamente.
  
 **Há um limite de tamanho de mensagem ao importar arquivos PST?**
  
Sim. Se um arquivo PST contiver um item de caixa de correio maior do que 150 MB, o item será ignorado durante o processo de importação.
  
 **São propriedades de mensagens, como quando a mensagem foi enviada ou recebida, a lista de destinatários e outras propriedades, preservadas quando os arquivos PST são importados para uma caixa de correio do Office 365?**
  
Sim. Os metadados da mensagem original não são alterados durante o processo de importação.
  
 **Há um limite para o número de níveis em uma hierarquia de pastas para um arquivo PST que eu desejo importar para uma caixa de correio?**
  
Sim. Você não pode importar um arquivo PST que tenha 300 ou mais níveis de pastas aninhadas.
  
 **Posso usar o carregamento de rede para importar arquivos PST para uma caixa de correio inativa no Office 365?**
  
Sim, esse recurso já está disponível.
  
 **Posso usar o carregamento de rede para importar arquivos PST para uma caixa de correio de arquivo morto online em uma implantação híbrida do Exchange?**
  
Sim, esse recurso já está disponível.
  
 **Posso usar o carregamento de rede para importar arquivos PST para pastas públicas no Exchange Online?**
  
Não, não é possível importar arquivos PST para pastas públicas.
  
## <a name="using-drive-shipping-to-import-pst-files"></a>Usando o envio de unidade para importar arquivos PST

Para obter instruções passo a passo, consulte [usar o envio de unidade para importar arquivos pst para o Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md).
  
 **Quais permissões são necessárias para criar trabalhos de importação no serviço de importação do Office 365?**
  
Você deve ser atribuído à função de exportação de importação de caixa de correio para importar arquivos PST para caixas de correio do Office 365. Por padrão, essa função não é atribuída a nenhum grupo de função no Exchange Online. Você pode adicionar a função de exportação de importação de caixa de correio ao grupo de funções Gerenciamento da organização. Ou você pode criar um novo grupo de função, atribua a função de exportação de importação de caixa de correio e, em seguida, adicione a si mesmo ou a outros usuários como um membro. Para obter mais informações, consulte as seções "adicionar uma função a um grupo de funções" ou "criar um grupo de função" em [gerenciar grupos de função no Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=730688).
  
Além disso, para criar trabalhos de importação no centro de &amp; conformidade de segurança do Office 365, um dos seguintes deve ser verdadeiro:
  
- Você precisa receber a função de destinatários de email no Exchange Online. Por padrão, essa função é atribuída aos grupos de gerenciamento da organização e de funções de gerenciamento de destinatários.
    
    Ou
    
- Você deve ser um administrador global em sua organização do Office 365.
    
> [!TIP]
> Considere a criação de um novo grupo de função no Exchange Online destinado especificamente à importação de arquivos PST para o Office 365. Para obter o nível mínimo de privilégios necessários para importar arquivos PST, atribua as funções de importação de caixa de correio e destinatários de email ao novo grupo de funções e, em seguida, adicione membros. 
  
 **Onde está disponível o envio da unidade?**
  
O envio de unidades está disponível atualmente nos Estados Unidos, Canadá, Brasil, Reino Unido, Europa, Índia, leste asiático, Sudeste Asiático, Japão, República da Coréia e Austrália. O envio de unidades estará disponível em mais regiões em breve.
  
 **Quais contratos de licenciamento comercial oferecem suporte ao envio de unidades?**
  
O envio de unidades para importar arquivos PST para o Office 365 está disponível por meio de um Microsoft Enterprise Agreement (EA). O envio de unidades não está disponível por meio de um contrato de produtos e serviços da Microsoft (MPSA).
  
 **Qual é o preço para usar o envio de unidade para importar arquivos PST para o Office 365?**
  
O custo para usar o envio de unidade para importar arquivos PST para caixas de correio do Office 365 é de US $ BRL por GB de dados. Por exemplo, se você enviar uma unidade de disco rígido que contenha 1.000 GB (1 TB) de arquivos PST, o custo será de US $ $2000. Você pode trabalhar com um parceiro para pagar a taxa de importação. Para obter informações sobre como encontrar um parceiro, consulte [encontre seu parceiro ou revendedor do Office 365](https://go.microsoft.com/fwlink/p/?LinkId=785197).
  
 **Que tipos de discos rígidos são compatíveis com o envio de unidades?**
  
Somente discos rígidos internos de estado sólido (SSDs) de 2,5 polegadas ou 2,5 ou 3,5 polegadas SATA II/III são suportados para uso com o serviço de importação do Office 365. Você pode usar discos rígidos de até 10 TB. Para trabalhos de importação, somente o primeiro volume de dados no disco rígido será processado. O volume de dados deve ser formatado com o NTFS. Ao copiar dados para uma unidade de disco rígido, você pode anexá-los diretamente usando um conector SATA de 2,5 polegadas ou 2,5 ou 3,5 polegada SATA II/III ou pode anexá-lo externamente usando um adaptador de USB de ou/ou/ou/ou/ou SATA II de 4 pol
  
> [!IMPORTANT]
> Discos rígidos externos que acompanham um adaptador USB interno não são compatíveis com o serviço de importação do Office 365. Além disso, o disco dentro do capitalização de um disco rígido externo não pode ser usado. Não envie discos rígidos externos. 
  
 **Quantas unidades de disco rígidos podem ser enviadas para um único trabalho de importação?**
  
Você pode fornecer no máximo 10 discos rígidos para um único trabalho de importação.
  
 **Após enviar meu disco rígido, quanto tempo demora para acessar o centro de dados da Microsoft?**
  
Isso depende de algumas coisas, como sua proximidade com o Data Center da Microsoft e qual tipo de opção de envio que você usou para enviar seu disco rígido (como entrega de dia seguinte, entrega de dois dias ou entrega de aterramento). Com a maioria das transportadoras, você pode usar o número de controle para acompanhar o status da sua entrega.
  
 **Após o meu disco rígido chegar ao Data Center da Microsoft, quanto tempo demora para carregar meus arquivos PST para o Azure?**
  
Depois que o disco rígido for recebido no centro de dados da Microsoft, levará entre 7 e 10 dias úteis para carregar os arquivos PST para a área de armazenamento do Microsoft Azure para sua organização. Os arquivos PST serão carregados para um contêiner de blob do Azure chamado **ingestiondata**. 
  
 **Quanto tempo leva para importar um arquivo PST para uma caixa de correio?**
  
Depois que os arquivos PST são carregados para a área de armazenamento do Azure, o Office 365 analisa os dados nos arquivos PST (de uma maneira segura e segura) para identificar a idade dos itens e os diferentes tipos de mensagem incluídos nos arquivos PST. Quando esta análise estiver concluída, você terá a opção de importar todos os dados dos arquivos PST ou definir filtros para que controlem quais dados são importados. Depois de iniciar o trabalho de importação, um arquivo PST é importado para uma caixa de correio do Office 365 em uma taxa de pelo menos 24 GB por dia. Se essa taxa não atender às suas necessidades, você poderá considerar outros métodos para importar dados de email para o Office 365. Para obter mais informações, consulte [maneiras de migrar várias contas de email para o Office 365](https://support.office.com/article/ways-to-migrate-multiple-email-accounts-to-office-365-0a4913fe-60fb-498f-9155-a86516418842).
  
Se arquivos PST diferentes forem importados para caixas de correio de destino diferentes, o processo de importação ocorrerá em paralelo; em outras palavras, cada par de PST/caixa de correio é importado simultaneamente. Da mesma forma, se vários arquivos PST forem importados para a mesma caixa de correio, eles serão importados simultaneamente.
  
 **Depois que a Microsoft carregar meus arquivos PST para o Azure, quanto tempo eles serão mantidos no Azure antes de serem excluídos?**
  
Todos os arquivos PST no local de armazenamento do Azure para sua organização (no contêiner de blob chamado **ingestiondata** ) são excluídos 30 dias após a criação do trabalho de importação mais recente na página **importar** no &amp; centro de conformidade de segurança. 
  
Isso também significa que, após os arquivos PST serem excluídos da área de armazenamento do Azure, eles não serão mais exibidos na lista de arquivos para um trabalho de importação concluído &amp; no centro de conformidade de segurança. Embora um trabalho de importação ainda possa estar listado na página de **importação** no centro &amp; de conformidade de segurança, a lista de arquivos PST pode estar vazia quando você exibir os detalhes de trabalhos de importação mais antigos. 
  
 **Qual versão do formato de arquivo PST é suportada para importar para o Office 365?**
  
Há duas versões do formato de arquivo PST: ANSI e Unicode. É recomendável importar arquivos que usam o formato de arquivo PST Unicode. No enTanto, os arquivos que usam o formato de arquivo PST ANSI, como aqueles para idiomas que usam um conjunto de caracteres de dois bytes (DBCS), também podem ser importados para o Office 365. Para obter mais informações sobre a importação de arquivos PST ANSI, consulte a etapa 3 em [usar o envio de unidade para importar arquivos pst para o Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md#step-3-create-the-pst-import-mapping-file).
  
Além disso, os arquivos PST do Outlook 2007 e versões posteriores podem ser importados para o Office 365.
  
 **Há um limite de tamanho de mensagem ao importar arquivos PST?**
  
Sim. Se um arquivo PST contiver um item de caixa de correio maior do que 150 MB, o item será ignorado durante o processo de importação.
  
 **São propriedades de mensagens, como quando a mensagem foi enviada ou recebida, a lista de destinatários e outras propriedades, preservadas quando os arquivos PST são importados para uma caixa de correio do Office 365?**
  
Sim. Os metadados da mensagem original não são alterados durante o processo de importação
  
 **Há um limite para o número de níveis em uma hierarquia de pastas para um arquivo PST que eu desejo importar para uma caixa de correio?**
  
Sim. Você não pode importar um arquivo PST que tenha 300 ou mais níveis de pastas aninhadas.
  
 **Posso usar o envio de unidade para importar arquivos PST para uma caixa de correio inativa no Office 365?**
  
Sim, esse recurso já está disponível.
  
 **Posso usar o envio de unidade para importar arquivos PST para uma caixa de correio de arquivo morto online em uma implantação híbrida do Exchange?**
  
Sim, esse recurso já está disponível.
  
 **Posso usar o envio de unidade para importar arquivos PST para pastas públicas no Exchange Online?**
  
Não, não é possível importar arquivos PST para pastas públicas.
  
 **A Microsoft pode apagar meu disco rígido antes de enviá-lo de volta para mim?**
  
Não, a Microsoft não pode apagar discos rígidos antes de enviá-los de volta para os clientes. Os discos rígidos são retornados para você no mesmo estado em que estavam quando foram recebidos pela Microsoft.
  
 **A Microsoft pode destruir meu disco rígido em vez de enviá-lo novamente?**
  
Não, a Microsoft não pode destruir sua unidade de disco rígido. Os discos rígidos são retornados para você no mesmo estado em que estavam quando foram recebidos pela Microsoft.
  
 **Quais serviços de Courier são compatíveis com a entrega de retorno?**
  
Se você for um cliente nos Estados Unidos ou na Europa, a Microsoft usará o FedEx para retornar seu disco rígido. Para todas as outras regiões, a Microsoft usa a DHL.
  
 **Quais são os custos de envio de devolução?**
  
Os custos de envio podem variar, dependendo de sua proximidade com o Data Center da Microsoft para o qual você enviou seu disco rígido. A Microsoft cobrará sua conta do FedEx ou DHL para retornar seu disco rígido. O custo da entrega de retorno é de sua responsabilidade.
  
 **Posso usar um serviço de envio do Courier personalizado, como o envio personalizado do FedEx, para entregar meu disco rígido à Microsoft?**
  
Sim.
  
 **Se eu tiver que enviar meu disco rígido para outro país, há alguma coisa que eu precise fazer?**
  
O disco rígido que você envia para a Microsoft pode ter que cruzar bordas internacionais. Se esse for o caso, você é responsável por garantir que a unidade de disco rígido e os dados que ele contém sejam importados e/ou exportados de acordo com as leis aplicáveis. Antes de enviar uma unidade de disco rígido, Confira seus conselheiros para verificar se a unidade e os dados podem ser enviados legalmente para o Data Center da Microsoft especificado. Isso ajudará a garantir que ele chegue à Microsoft de forma oportuna.

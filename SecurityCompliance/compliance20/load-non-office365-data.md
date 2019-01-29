---
title: Carregar dados do Office 365 em um conjunto de trabalho
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 427b4c8c9dfffe351827a6869ae26a5356d646d8
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607346"
---
# <a name="load-non-office-365-data-into-a-working-set"></a>Carregar dados do Office 365 em um conjunto de trabalho

Nem todos os documentos que você talvez precise analisar com eDiscovery avançadas do Office 365 residirá no Office 365. Com o conteúdo não-Office 365 importe recurso no eDiscovery avançado, que você pode carregar documentos que não live no Office 365 em um conjunto de trabalho para que ele é analisado com eDiscovery avançado. Esse procedimento mostra como trazer seus documentos do Office 365 para descoberta eletrônica avançada para análise.

>[!Note]
>A Descoberta Eletrônica Avançada exige um Office 365 E3, com um complemento de Conformidade Avançada ou uma assinatura do E5 para sua organização. Se você não tiver esse plano e quiser tentar a Descoberta Eletrônica Avançada, poderá Inscrever-se para uma avaliação do Office 365 Enterprise E5.

## <a name="before-you-begin"></a>Antes de começar
Usando o recurso de upload Non-Office 365, conforme descrito neste procedimento requer que você tenha:
* Um Office 365 E3 com inscrição de E5 ou complemento de conformidade avançadas
* Todos os responsáveis cujo conteúdo não - Office 365 será carregado devem ter E3 com licenças de E5 ou complemento de conformidade avançadas
* Uma ocorrência de descoberta eletrônica existente
* Todos os arquivos para carregar coletadas em pastas onde houver uma pasta por dos responsáveis e nome das pastas se situa este formato *alias@domainname* . O *alias@domainname* deve ser o domínio e alias de usuário Office 365. Você pode coletar todas as pastas de *alias@domainname* em uma pasta raiz. A pasta raiz pode conter apenas as pastas *alias@domainname* , não deve haver nenhum arquivo afastado na pasta raiz
* Uma conta que é uma gerente de descoberta eletrônica ou eDiscovery administrador Microsoft Azure armazenamento ferramentas instalado em um computador que tenha acesso na estrutura de pasta de conteúdo do Office 365.
* Instalar AzCopy, você poderá fazer isso daqui:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy

## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a>Carregar o conteúdo do Office 365 em eDiscovery avançado
1. Como um gerente de descoberta eletrônica ou eDiscovery administrador, abra o eDiscovery avançada, em seguida, o caso em que os dados não - Office 365 serão carregados.  Clique na guia **conjuntos de trabalho** e selecione o conjunto de trabalho que você deseja carregar os dados não-Office 365.  Se você já não tiver criado um conjunto de trabalho, você poderá fazer isso agora.  Finalmente, clique em **Gerenciar funcionamento definido** e **carregamentos de modo de exibição** , na seção de dados não-Office 365

2. Clique no botão **carregar arquivos** para iniciar o Assistente de importação de dados não-Office 365.

![Carregar arquivos](../media/574f4059-4146-4058-9df3-ec97cf28d7c7.png)

3. A primeira etapa do assistente simplesmente prepara um blob Azure seguro para os arquivos sejam carregados.  Após a preparação é compelted, clique no **próximo: carregar arquivos** botão.

![Não-Office 365 importar - preparar](../media/0670a347-a578-454a-9b3d-e70ef47aec57.png)
 
4. Na etapa **carregar arquivos** , especifique o **caminho para o local dos arquivos**, isso é onde os dados não-Office 365 que você planeja importando estão localizados.  Definir o local correto garante a AzCopy comando é atualizado corretamente.

> [!NOTE]
> Se você ainda não tiver instalado AzCopy, você pode fazer isso daqui:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy

5. Copie o comando predefinido clicando no link de **cópia para área de transferência** . Inicie um prompt de comando do windows, cole o comando e pressione enter.  Os arquivos serão carregados para o armazenamento de blob Azure segura para a próxima etapa.

![Importação de não-Office 365 - carregar arquivos](../media/3ea53b5d-7f9b-4dfc-ba63-90a38c14d41a.png)

![Importação de não-Office 365 - AzCopy](../media/504e2dbe-f36f-4f36-9b08-04aea85d8250.png)

6. Finalmente, retorne à conformidade de & de segurança e clique no **próximo: processar arquivos** botão.  Isso iniciará o processamento, extração de texto e indexação dos arquivos carregados.  Você pode controlar o andamento do processamento aqui ou na guia **Jobs** .  Depois de concluído, os novos arquivos estarão disponíveis no conjunto de trabalho.  Depois que o processamento estiver concluído, você pode recusar o assistente.

![Importação de não-Office 365 - processar arquivos](../media/218b1545-416a-4a9f-9b25-3b70e8508f67.png)


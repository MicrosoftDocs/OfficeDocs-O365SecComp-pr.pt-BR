---
title: Aumentar a velocidade de download ao exportar resultados de pesquisa de descoberta eletrônica do Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/14/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid: MOE150
ms.assetid: c4c8f689-9d52-4e80-ae4b-1411ee9efc43
description: Saiba como configurar o registro do Windows para aumentar a taxa de transferência de dados ao baixar os resultados da pesquisa e pesquisar dados do centro de conformidade e descoberta eletrônica avançada do & de segurança no Office 365.
ms.openlocfilehash: 10eff929d6b668d5e2bc22d8ee7f223da4943326
ms.sourcegitcommit: f0e3c9de0b545081a4d264f74559b941f6c71410
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2019
ms.locfileid: "31958614"
---
# <a name="increase-the-download-speed-when-exporting-ediscovery-search-results-from-office-365"></a>Aumentar a velocidade de download ao exportar resultados de pesquisa de descoberta eletrônica do Office 365

Ao usar a ferramenta de exportação de descoberta eletrônica do Office 365 para baixar os resultados de uma pesquisa de conteúdo no centro de conformidade do & de segurança ou baixar dados da descoberta eletrônica avançada do Office 365, a ferramenta inicia um determinado número de operações de exportação simultâneas para baixar os dados para o computador local. Por padrão, o número de operações simultâneas é definido como 8 vezes o número de núcleos no computador que você está usando para baixar os dados. Por exemplo, se você tiver um computador dual core (ou seja, duas unidades de processamento central em um único chip), o número padrão de operações de exportação simultâneas será 16. Para aumentar a taxa de transferência e acelerar o processo de download, é possível aumentar o número de operações simultâneas Configurando uma configuração do registro do Windows no computador que você usa para baixar os resultados da pesquisa. Para acelerar o processo de download, recomendamos que você comece com uma configuração de 24 operações simultâneas.
  
Se você baixar os resultados da pesquisa por uma rede de baixa largura de banda, aumentar essa configuração poderá ter um impacto negativo. Como alternativa, é possível aumentar a configuração para mais de 24 operações simultâneas em uma rede de alta largura de banda (o número máximo de operações simultâneas é 48). Depois de definir essa configuração do registro, talvez seja necessário alterá-la para encontrar o número ideal de operações simultâneas para seu ambiente.
  
## <a name="create-a-registry-setting-to-change-the-number-of-concurrent-operations-when-exporting-data"></a>Criar uma configuração de registro para alterar o número de operações simultâneas ao exportar dados

Execute o procedimento a seguir no computador que você usará para baixar os resultados da pesquisa do centro de conformidade do & de segurança ou dos dados da descoberta eletrônica avançada.
  
1. Feche a ferramenta de exportação de descoberta eletrônica do Office 365 se ela estiver aberta. 
    
2. Salve o seguinte texto em um arquivo de registro de janela usando um sufixo de nome de arquivo. reg; por exemplo, ConcurrentOperations. reg. 
    
    ```
    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool]
    "DownloadConcurrency"="24"
    ```

    Como explicado anteriormente, recomendamos que você comece com 24 operações simultâneas e, em seguida, altere essa configuração conforme apropriado.
    
3. No Windows Explorer, clique ou clique duas vezes no arquivo. reg que você criou na etapa anterior.
    
4. Na janela controle de acesso do usuário, clique em **Sim** para permitir que o editor do Registro faça a alteração. 
    
5. Quando for solicitado a continuar, clique em **Sim**.
    
    O editor do registro exibe uma mensagem dizendo que a configuração foi adicionada com êxito ao registro.
    
6. Você pode repetir as etapas 2-5 para alterar o valor da `DownloadConcurrency` configuração do registro. 
    
    > [!IMPORTANT]
    > Após criar ou alterar a `DownloadConcurrency` configuração do registro, certifique-se de criar um novo trabalho de exportação ou reinicie um trabalho de exportação existente para os resultados de pesquisa ou os dados que você deseja baixar. Consulte a seção [mais informações](#more-information) para obter mais detalhes. 
  
## <a name="more-information"></a>Mais informações

- Uma nova chave de registro é criada na primeira vez que você executa o arquivo. reg que você criou neste procedimento. Em seguida `DownloadConcurrency` , a configuração do registro será editada sempre que você alterar e executar novamente o arquivo. reg Edit. 
    
- A ferramenta de exportação de descoberta eletrônica do Office 365 usa o [utilitário AzCopy do Azure](https://go.microsoft.com/fwlink/?linkid=849949) para baixar dados de pesquisa do centro de conformidade do _AMP_ de segurança ou da descoberta eletrônica avançada. Definir a `DownloadConcurrency` configuração do registro é semelhante a usar o parâmetro **/NC** ao executar o utilitário AzCopy. Portanto, a configuração do `"DownloadConcurrency=24"` registro de teria o mesmo efeito que usar o valor do `/NC:24` parâmetro de com o utilitário AzCopy. 
    
- Se você interromper um download de exportação atualmente em andamento e reiniciá-lo (tentando baixar os resultados da pesquisa novamente), a ferramenta de exportação de descoberta eletrônica do Office 365 tentará continuar o mesmo download. Portanto, se você iniciar um download, interrompa-o e, em seguida `DownloadConcurrency` , altere a configuração do registro, o download provavelmente falhará se você reiniciá-lo (clicando em **baixar resultados**exportados). Isso ocorre porque a ferramenta de exportação tentará retomar o download anterior usando configurações que não são válidas, pois você alterou a configuração do registro.
    
    Portanto, depois de alterar a `DownloadConcurrency` configuração do registro, certifique-se de reiniciar o trabalho de exportação (clicando em **reiniciar exportação**) no centro de conformidade do & de segurança. Em seguida, você pode baixar os resultados exportados. Para obter mais informações sobre como exportar dados e resultados de pesquisa, consulte:
    
  - [Exportar os resultados da Pesquisa de Conteúdo](export-search-results.md)
    
  - [Exportar resultados na descoberta eletrônica avançada do Office 365](export-results-in-advanced-ediscovery.md)
    

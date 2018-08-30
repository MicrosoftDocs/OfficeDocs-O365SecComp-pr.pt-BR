---
title: Aumentar a velocidade de download ao exportar os resultados da pesquisa de descoberta eletrônica do Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/14/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c4c8f689-9d52-4e80-ae4b-1411ee9efc43
description: Saiba como configurar o registro do Windows para aumentar a taxa de transferência de dados ao fazer o download de resultados da pesquisa e pesquisa de dados a partir de segurança do Office 365 &amp; descoberta eletrônica do Centro de conformidade e avançadas do Office 365.
ms.openlocfilehash: 3f456f5ee0312d4d4d7b95f868520e6756a90fd1
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524714"
---
# <a name="increase-the-download-speed-when-exporting-ediscovery-search-results-from-office-365"></a>Aumentar a velocidade de download ao exportar os resultados da pesquisa de descoberta eletrônica do Office 365

Quando você usar a ferramenta de exportação de descoberta eletrônica do Office 365 para baixar os resultados de uma pesquisa de conteúdo no Office 365 Security &amp; dados Centro de conformidade ou fazer download de eDiscovery avançadas do Office 365, a ferramenta inicia um determinado número de exportação simultânea operações para baixar os dados em seu computador local. Por padrão, o número de operações simultâneas é definido como 8 vezes o número de núcleos no computador que você está usando para baixar os dados. Por exemplo, se você tiver um computador de núcleo duplo (ou seja, duas unidades de processamento central em um chip), o número padrão de operações de exportação simultâneas é 16. Para aumentar a taxa de transferência de transferência de dados e a velocidade do processo de download, você pode aumentar o número de operações simultâneas, definindo uma configuração de registro do Windows no computador que você pode usar para baixar os resultados da pesquisa. Para o processo de download de velocidade, recomendamos que você inicie com uma configuração de 24 operações simultâneas.
  
Se você pode baixar os resultados da pesquisa através de uma rede de pouca largura de banda, aumentando a essa configuração pode ter um impacto negativo. Como alternativa, você poderá aumentar a configuração para mais de 24 operações simultâneas em uma rede de alta largura de banda (o número máximo de operações simultâneas é 512). Depois de configurar essa configuração de registro, você pode precisar alterá-lo para localizar o número ideal de operações simultâneas para seu ambiente.
  
## <a name="create-a-registry-setting-to-change-the-number-of-concurrent-operations-when-exporting-data"></a>Criar uma configuração para alterar o número de operações simultâneas na exportação de dados de registro

Execute o procedimento a seguir no computador que você usará para baixar os resultados da pesquisa a partir de segurança &amp; dados do eDiscovery avançado ou centro de conformidade.
  
1. Feche a ferramenta de exportação de descoberta eletrônica do Office 365 se ele estiver aberto. 
    
2. Salve o seguinte texto em um arquivo de registro da janela usando um sufixo de nome de arquivo de. reg; Por exemplo, ConcurrentOperations.reg. 
    
    ```
    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool]
    "DownloadConcurrency"="24"
    ```

    Anterior conforme explicado, recomendamos que você inicie com 24 operações simultâneas e, em seguida, altere esta definição conforme apropriado.
    
3. No Windows Explorer, clique em ou duas vezes no arquivo. reg que você criou na etapa anterior.
    
4. Na janela de controle de acesso de usuário, clique em **Sim** para permitir que o Editor do registro faça a alteração. 
    
5. Quando solicitado a continuar, clique em **Sim**.
    
    O Editor do registro exibe uma mensagem informando que a configuração foi adicionada com êxito ao registro.
    
6. Você pode repetir as etapas 2 a 5 para alterar o valor para o `DownloadConcurrency` configuração do registro. 
    
    > [!IMPORTANT]
    > Depois que você criar ou alterar o `DownloadConcurrency` registro de configuração, certifique-se criar um novo trabalho de exportação ou reiniciar um trabalho de exportação existente para os resultados de pesquisa ou os dados que você deseja baixar. Consulte a seção de [informações adicionais](increase-download-speeds-when-exporting-ediscovery-results.md#moreinfo) para obter mais detalhes. 
  
## <a name="more-information"></a>Mais informações

- Uma nova chave de registro é criada na primeira vez que você executar o arquivo. reg que você criou neste procedimento. Em seguida, a `DownloadConcurrency` configuração do registro é editada sempre que você alterar e execute novamente o arquivo. reg editar. 
    
- A ferramenta de exportação de descoberta eletrônica do Office 365 usa o [utilitário AzCopy do Windows Azure](https://go.microsoft.com/fwlink/?linkid=849949) para baixar os dados de pesquisa a partir de segurança &amp; Centro de conformidade ou de descoberta eletrônica avançada. Configurando o `DownloadConcurrency` configuração do registro é semelhante a usar o parâmetro **/NC** ao executar o utilitário AzCopy. Então a configuração de registro de `"DownloadConcurrency=24"` teria o mesmo efeito que usar o valor do parâmetro da `/NC:24` com o utilitário AzCopy. 
    
- Se você interromper um download de exportação em andamento e, em seguida, reiniciá-lo (por tentando baixar os resultados da pesquisa novamente), a ferramenta de exportação de descoberta eletrônica do Office 365 tentará reiniciar o download do mesmo. Assim, se você iniciar um download, pará-lo e, em seguida, alterar o `DownloadConcurrency` registro definição, o download provavelmente falhará se você reiniciá-lo (clicando **Download exportou resultados**). Isso ocorre porque a ferramenta de exportação tentará reiniciar o download anterior usando as configurações que não são válidas, pois você alterou a configuração do registro.
    
    Portanto, após você alterar o `DownloadConcurrency` registro configuração, certifique-se de reiniciar o trabalho de exportação (clicando **Reiniciar exportação**) na segurança &amp; Centro de conformidade. Em seguida, você pode baixar os resultados exportados. Para obter mais informações sobre como exportar dados e resultados de pesquisa, consulte:
    
  - [Exportar resultados de pesquisa de conteúdo da segurança do Office 365 &amp; Centro de conformidade](export-search-results.md)
    
  - [Exportar resultados na Descoberta Eletrônica Avançada do Office 365](export-results-in-advanced-ediscovery.md)
    

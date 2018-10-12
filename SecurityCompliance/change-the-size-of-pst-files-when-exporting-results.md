---
title: Alterar o tamanho dos arquivos PST ao exportar os resultados da pesquisa de descoberta eletrônica
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/12/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 04e9de2d-765b-457b-a98a-d0f60bfb13f2
description: Você pode alterar o tamanho padrão dos arquivos PST que são baixadas para o computador ao exportar os resultados da pesquisa de descoberta eletrônica.
ms.openlocfilehash: c01f05a02fd94941eb2eb7a05b4c84ffecec9b39
ms.sourcegitcommit: 448c5897e44448adfc82e3eaffb774c770c04815
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/12/2018
ms.locfileid: "25522242"
---
# <a name="change-the-size-of-pst-files-when-exporting-ediscovery-search-results"></a>Alterar o tamanho dos arquivos PST ao exportar os resultados da pesquisa de descoberta eletrônica

Quando você usar a ferramenta de exportação de descoberta eletrônica do Office 365 para exportar os resultados de email de uma pesquisa de descoberta eletrônica das diferentes ferramentas de descoberta eletrônica da Microsoft, o tamanho padrão de um arquivo PST que pode ser exportado é 10 GB. Se você quiser alterar esse tamanho padrão, você pode editar o registro do Windows no computador que você usa para exportar os resultados da pesquisa. Um motivo para fazer isso é para que um arquivo PST pode caibam em mídia removível, tal um DVD, uma unidade USB ou um CD. 
  
> [!NOTE]
>  A ferramenta de exportação de descoberta eletrônica do Office 365 é usada para exportar os resultados da pesquisa ao usar a pesquisa de conteúdo no Office 365 Security &amp; Centro de conformidade, In-Place eDiscovery no Exchange Online e o Centro de descoberta eletrônica no SharePoint Online. 
  
## <a name="create-a-registry-setting-to-change-the-size-of-pst-files-when-you-export-ediscovery-search-results"></a>Criar uma configuração de registro para alterar o tamanho dos arquivos PST ao exportar os resultados da pesquisa de descoberta eletrônica

Execute o procedimento a seguir no computador que você usará para exportar os resultados de uma pesquisa de descoberta eletrônica.
  
1. Feche a ferramenta de exportação de descoberta eletrônica do Office 365 se ele estiver aberto. 
    
2. Salve o seguinte texto em um arquivo de registro da janela usando um sufixo de nome de arquivo de. reg; Por exemplo, PstExportSize.reg. 
    
    ```
    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool]
    "PstSizeLimitInBytes"="1073741824"
    ```

    No exemplo acima, o `PstSizeLimitInBytes` valor for definido como 1.073.741.824 bytes ou aproximadamente 1 GB. Aqui estão alguns outros valores de amostra para o `PstSizeLimitInBytes` configuração. 
    
    |**Tamanho em GB (aproximadamente)**|**Tamanho em bytes**|
    |:-----|:-----|
    |.7 GB (700 MB)  <br/> |751619277  <br/> |
    |2 GB  <br/> |2147483648  <br/> |
    |4 GB  <br/> |4294967296  <br/> |
    |8 GB  <br/> |8589934592  <br/> |
   
3. Alterar o `PstSizeLimitInBytes` valor ao tamanho máximo de um arquivo PST ao exportar os resultados da pesquisa e salve o arquivo desejado. 
    
4. No Windows Explorer, clique em ou duas vezes no arquivo. reg que você criou nas etapas anteriores.
    
5. Na janela de controle de acesso de usuário, clique em **Sim** para permitir que o Editor do registro faça a alteração. 
    
6. Quando solicitado a continuar, clique em **Sim**.
    
    O Editor do registro exibe uma mensagem informando que a configuração foi adicionada com êxito ao registro.
    
7. Você pode repetir as etapas 3 a 6 para alterar o valor para o `PstSizeLimitInBytes` configuração do registro. 
  
## <a name="frequently-asked-questions-about-changing-the-default-size-of-pst-files-when-you-export-ediscovery-search-results"></a>Perguntas frequentes sobre como alterar o tamanho padrão dos arquivos PST ao exportar os resultados da pesquisa de descoberta eletrônica

 **Por que é o padrão de tamanho de 10 GB?**
  
O tamanho padrão de 10 GB foi com base nos comentários do cliente; 10 GB é um bom equilíbrio entre a quantidade ideal de conteúdo em um único PST e com uma mínima chance de corrupção de arquivo.
  
 **Deve aumentar ou diminuir o tamanho padrão dos arquivos PST?**
  
Os clientes tendem a diminuir o limite de tamanho, para que os resultados da pesquisa irá caber em mídia removível que eles podem enviar fisicamente outros locais em suas organizações. Não recomendamos que você aumentar o tamanho padrão porque os arquivos maior do que 10 GB podem ter problemas de corrupção de PST.
  
 **Computador em que é necessário fazer isso em?**
  
Você precisará alterar a configuração de registro em qualquer computador local que você execute a ferramenta de exportação de descoberta eletrônica do Office 365 em.
  
 **Após alterar essa configuração, preciso reinicializar o computador?**
  
Não, você não precisa reinicializar o computador. Mas, se estiver executando a ferramenta de exportação de descoberta eletrônica do Office 365, você terá que fechá-lo e o reinício-lo depois que você alterar essa configuração.
  
 **Uma chave do registro existente fazer editada ou fazer uma nova chave criada?**
  
Uma nova chave de registro é criada na primeira vez que você executar o arquivo. reg que você criou neste procedimento. Em seguida, a configuração é editada sempre que você alterar e execute novamente o arquivo. reg editar.

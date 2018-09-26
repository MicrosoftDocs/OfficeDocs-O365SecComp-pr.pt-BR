---
title: Desativar relatórios ao exportar os resultados de pesquisa de conteúdo no Office 365 Security &amp; Centro de conformidade
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/30/2016
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: c9b0ff0c-282b-4a44-b43f-cfc5b96557f9
description: Edite o registro do Windows no computador local para desabilitar os relatórios ao exportar os resultados de uma pesquisa de conteúdo da segurança do Office 365 &amp; Comliance Center. Desabilitar esses relatórios pode reduzir o tempo de download e salve o espaço em disco.
ms.openlocfilehash: 62782c472adca892e1dcf239a45fe80f0fa7251b
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25037974"
---
# <a name="disable-reports-when-you-export-content-search-results-in-the-office-365-security-amp-compliance-center"></a>Desativar relatórios ao exportar os resultados de pesquisa de conteúdo no Office 365 Security &amp; Centro de conformidade

Quando você usar a ferramenta de exportação de descoberta eletrônica do Office 365 para exportar os resultados de uma pesquisa de conteúdo na segurança &amp; Centro de conformidade, a ferramenta cria automaticamente e exporta dois relatórios que contêm informações adicionais sobre o conteúdo exportado. Esses relatórios são o arquivo de Results.csv e o arquivo manifest XML (consulte a seção de [Perguntas frequentes sobre como desativar os relatórios de exportação](#frequently-asked-questions-about-disabling-export-reports) neste tópico para obter descrições detalhadas desses relatórios). Como esses arquivos podem ser muito grandes, você pode reduzir o tempo de download e salve o espaço em disco, impedindo que esses arquivos estão sendo exportados. Você pode fazer isso, alterando o registro do Windows no computador que você usa para exportar os resultados da pesquisa. Se você quiser incluir os relatórios mais tarde, você pode editar a configuração do registro. 
  
## <a name="create-registry-settings-to-disable-the-export-reports"></a>Criar configurações de registro para desativar os relatórios de exportação

Execute o procedimento a seguir no computador que você usará para exportar os resultados de uma pesquisa de conteúdo.
  
1. Feche a ferramenta de exportação de descoberta eletrônica do Office 365 se ele estiver aberto.
    
2. Execute uma das etapas a seguir, dependendo de qual relatório de exportação para o qual você deseja desabilitar ou ambas.
    
    - **Results.csv**
    
      Salve o seguinte texto em um arquivo de registro do Windows usando um sufixo de nome de arquivo de. reg; Por exemplo, DisableResultsCsv.reg.
    
      ```
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultCsvEnabled /t REG_SZ /d False 
      ```

    - **Manifest**
    
      Salve o seguinte texto em um arquivo de registro do Windows usando um sufixo de nome de arquivo de. reg; Por exemplo, DisableManifestXml.reg.
    
      ```
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultEdrmEnabled /t REG_SZ /d False 
      ```

3. No Windows Explorer, clique em ou duas vezes no arquivo. reg que você criou nas etapas anteriores.
    
4. Na janela de controle de acesso de usuário, clique em **Sim** para permitir que o Editor do registro faça a alteração. 
    
5. Quando solicitado a continuar, clique em **Sim**.
    
    O Editor do registro exibe uma mensagem informando que a configuração foi adicionada com êxito ao registro.
  
## <a name="edit-registry-settings-to-re-enable-the-export-reports"></a>Editar configurações de registro para habilitar novamente os relatórios de exportação

Se você desabilitou os relatórios Results.csv e manifest criando os arquivos. reg no procedimento anterior, você pode editar esses arquivos para reabilitar um relatório para que ele será exportado com os resultados da pesquisa. Novamente, execute o procedimento a seguir no computador que você usará para exportar os resultados de uma pesquisa de conteúdo.
  
1. Feche a ferramenta de exportação de descoberta eletrônica do Office 365 se ele estiver aberto.
    
2. Edite uma ou ambas dos editar os arquivos. reg que você criou no procedimento anterior.
    
    - **Results.csv**
    
        Abra o arquivo DisableResultsCsv.reg no bloco de notas, altere o valor `False` para `True`e salve o arquivo. Por exemplo, depois de editar o arquivo, ele tem esta aparência:
    
        ```
        Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultCsvEnabled /t REG_SZ /d True
        ```

    - **Manifest**
    
        Abra o arquivo DisableManifestXml.reg no bloco de notas, altere o valor `False` para `True`e salve o arquivo. Por exemplo, depois de editar o arquivo, ele tem esta aparência:
    
      ```
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultEdrmEnabled /t REG_SZ /d True
      ```

3. No Windows Explorer, clique ou clique duas vezes em um arquivo. reg que você editou na etapa anterior.
    
4. Na janela de controle de acesso de usuário, clique em **Sim** para permitir que o Editor do registro faça a alteração. 
    
5. Quando solicitado a continuar, clique em **Sim**.
    
    O Editor do registro exibe uma mensagem informando que a configuração foi adicionada com êxito ao registro.
  
## <a name="frequently-asked-questions-about-disabling-export-reports"></a>Perguntas frequentes sobre como desativar os relatórios de exportação
<a name="faqs"> </a>

 **Quais são os relatórios Results.csv e manifest?**
  
Os arquivos Results.csv e manifest contêm informações adicionais sobre o conteúdo que foi exportado.
  
- Documento do Excel de uma **Results.csv** que contém informações sobre cada item que é o download como um resultado de pesquisa. Para email, o log de resultado contém informações sobre cada mensagem, incluindo: 
    
  - O local da mensagem na caixa de correio de origem (inclusive se a mensagem está na caixa de correio principal ou de arquivo morto).
    
  - A data na qual a mensagem foi enviada ou recebida.
    
  - A linha de assunto da mensagem.
    
  - O remetente e os destinatários da mensagem.
    
  - Se a mensagem é uma mensagem duplicada se você habilitou a eliminação da duplicação ao exportar os resultados da pesquisa. Mensagens duplicadas terá um valor na coluna **Pai ItemId** que identifica a mensagem como uma duplicata. O valor na coluna **ItemId pai** é o mesmo que o valor na coluna **Item DocumentId** da mensagem que foi exportada. 
    
    Para documentos do SharePoint e do OneDrive para sites corporativos, o log de resultado contém informações sobre cada documento, incluindo:
    
  - A URL para o documento.
    
  - A URL para o conjunto de sites onde o documento está localizado.
    
  - A data em que o documento foi modificado pela última vez.
    
  - O nome do documento (que está localizado na coluna Assunto no log de resultados).
    
- **Manifest** um arquivo de manifesto (no formato XML) que contém informações sobre cada item incluído nos resultados da pesquisa. As informações neste relatório são o mesmo que o relatório de Results.csv, mas ele está no formato especificado pelo Electronic Discovery Reference Model (EDRM). Para obter mais informações sobre EDRM, vá para [https://www.edrm.net](https://www.edrm.net).
    
 **Quando eu desabilite exportando esses relatórios?**
  
Ela depende de suas necessidades específicas. Muitas organizações não exigem informações adicionais sobre os resultados da pesquisa e não precisam esses relatórios.
  
 **Computador em que é necessário fazer isso em?**
  
 Você precisa alterar a configuração de registro em qualquer computador local que você execute a ferramenta de exportação de descoberta eletrônica do Office 365 em. 
  
 **Após alterar essa configuração, eu tenho que reiniciar o computador?**
  
Não, você não precisa reiniciar o computador. Mas, se estiver executando a ferramenta de exportação de descoberta eletrônica do Office 365, você precisará fechá-la e, em seguida, reiniciá-lo depois de alterar a configuração do registro.
  
 **Uma chave do registro existente fazer editada ou fazer uma nova chave criada?**
  
Uma nova chave de registro é criada na primeira vez que você executar o arquivo. reg que você criou no procedimento neste tópico. Em seguida, a configuração é editada sempre que você alterar e execute novamente o arquivo. reg editar.

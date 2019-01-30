---
title: Correção de erro durante o processamento de dados
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
ms.openlocfilehash: 82e6d44ded64d586611f429f9b3eebe4f47e9898
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607376"
---
# <a name="error-remediation-when-processing-data"></a>Correção de erro durante o processamento de dados

Correção de erro permite que administradores de descoberta eletrônica a capacidade corrigir problemas de dados que impedir a corretamente o conteúdo de processamento do eDiscovery avançado (Preview). Por exemplo, arquivos que são protegidas por senha não podem ser processados, desde que os arquivos estão bloqueados ou criptografados. Usando a correção de erro, os administradores de descoberta eletrônica podem fazer o download de arquivos com esses erros, remover a proteção por senha e carregar os arquivos remediados por teste.

Use o seguinte fluxo de trabalho para remediar arquivos com erros em casos de eDiscovery avançado (Preview).

## <a name="creating-an-error-remediation-session-to-remediate-files-with-processing-errors"></a>Criando uma sessão de correção de erro para remediar arquivos com erros de processamento

>[!NOTE]
>Se o Assistente de correção de erro é fechado a qualquer momento durante o procedimento a seguir, é possível retornar para a sessão de correção de erro a partir da guia **processamento** selecionando **correções de erro** no menu suspenso **modo de exibição** .

1. Na guia **processamento** em um caso de eDiscovery avançado (Preview), selecione **erros** no menu suspenso **modo de exibição** .

2. Selecione os erros que você deseja remediar clicando no botão de opção ao lado do tipo de erro ou um tipo de arquivo.  No exemplo a seguir, podemos estiver correção um arquivo de protegido por senha.

3. Clique em **+ novo correção de erro**.

    ![Correção de erro](../media/8c2faf1a-834b-44fc-b418-6a18aed8b81a.png)

    A sessão de correção de erro será iniciada, começando com um estágio de preparação onde os arquivos ou com erros são movidos para um local seguro de Azure sejam baixados.

    ![Preparando a correção de erro](../media/390572ec-7012-47c4-a6b6-4cbb5649e8a8.png)

4. Após a preparação for concluída, clique em **próximo: baixar arquivos** para prosseguir com o download.

    ![Baixar arquivos](../media/6ac04b09-8e13-414a-9e24-7c75ba586363.png)

5. Para baixar arquivos, especifique o **caminho de destino para download**; Este é um caminho no computador local onde o arquivo deve ser baixado.  O caminho padrão, % USERPROFILE%\Downloads\errors, aponta para a pasta de downloads do usuário registrado no; Isso pode ser alterado conforme necessário.

    >[!NOTE]
    >Recomendamos que você use um caminho de arquivo local, em vez de um caminho de rede remoto para um desempenho ideal.

    > [!NOTE]
    > Se você não instalou AzCopy, você pode instalá-lo a partir daqui:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy

6. Copie o comando predefinido, clicando em **Copiar para a área de transferência**. Inicie um prompt de comando do windows, cole o comando e pressione **Enter**.  

    Os arquivos serão baixados.

    ![Preparando a correção de erro](../media/f364ab4d-31c5-4375-b69f-650f694a2f69.png)

     > [!NOTE]
     > Se você tiver problemas ao executar esse comando, consulte https://go.microsoft.com/fwlink/?linkid=2038117 para dicas de solução de problemas.

7. Depois de baixar os arquivos, você pode remediá-los com uma ferramenta adequada. Arquivos protegidos por senha, há um número de ferramentas que você pode usar para quebrar senhas. Se você souber as senhas para os arquivos, você pode abri-los e remover a proteção por senha.
    > [!NOTE]
    > IT é importante que você mantenha os nomes de arquivo e a estrutura de diretório dos arquivos remediados por teste intacto.  Todas as convenções de nomenclatura usada nos arquivos baixados e pastas tornam possível associar os arquivos remdiated original.

8. Agora, volte à eDiscovery avançado (Preview) e clique em **próximo: carregar arquivos**.  Isso moverá para a próxima etapa onde você agora pode carregar os arquivos.

    ![Carregar arquivos](../media/af3d8617-1bab-4ecd-8de0-22e53acba240.png)

9. Especifique o local dos arquivos remediados por teste na caixa de texto **caminho para o local dos arquivos** , clique em **Copiar para clibpboard**.

10. Cole o comando em um Prompt de comando do Windows e pressione **Enter** para carregar os arquivos.

    ![ff2ff691-629f-4065-9b37-5333f937daf6.png](../media/ff2ff691-629f-4065-9b37-5333f937daf6.png)

11. Finalmente, volte à eDiscovery avançado (Preview) e clique em **próximo: processar arquivos**.

12. Quando o processamento é concluído.  Você pode retornar ao conjunto de trabalho e consulte o arquivo remediados por teste.

## <a name="what-happens-when-files-are-remediated"></a>O que acontece quando os arquivos são remediados

Quando remediados por teste arquivos são carregados, os metadados original é preservado, com exceção dos seguintes campos: 

- DocumentExtractedUrl
- ExtractedTextSize
- HasText
- IsErrorRemediate
- IsParentExtractedUrl
- ItemExtractedUrl
- LoadId
- ProcessingErrorMessage
- Processamento
- Texto
- WordCount
- WorkingsetId

Para uma definição de todos os campos de metadados de documento no eDiscovery avançado (Preview), consulte [os campos de metadados de documento](document-metadata-fields.md).
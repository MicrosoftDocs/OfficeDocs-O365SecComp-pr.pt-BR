---
title: Correção de erros durante o processamento de dados
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: c9c2660929037430535c9b612218563c51b1f056
ms.sourcegitcommit: 3f3f3ecb28ef65d023f3573f9a4e09a0586d8f53
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2019
ms.locfileid: "36490788"
---
# <a name="error-remediation-when-processing-data"></a>Correção de erros durante o processamento de dados

A correção de erros permite que os administradores de descoberta eletrônica corrijam problemas de dados que impedem a descoberta eletrônica avançada do processamento adequado do conteúdo. Por exemplo, os arquivos protegidos por senha não podem ser processados, já que os arquivos são bloqueados ou criptografados. Usando a correção de erros, os administradores de descoberta eletrônica podem baixar arquivos com esses erros, remover a proteção por senha e carregar os arquivos corrigidos.

Use o fluxo de trabalho a seguir para corrigir arquivos com erros em casos de descoberta eletrônica avançada.

## <a name="create-an-error-remediation-session-to-remediate-files-with-processing-errors"></a>Criar uma sessão de correção de erro para corrigir arquivos com erros de processamento

>[!NOTE]
>Se o assistente de correção de erros for fechado a qualquer momento durante o procedimento a seguir, você poderá retornar à sessão de correção de erro na guia **processamento** selecionando as correções de **erro** no menu suspenso **Exibir** .

1. Na guia **processamento** em um caso de descoberta eletrônica avançada, selecione **erros** no menu suspenso **Exibir** .

2. Selecione os erros que você deseja corrigir clicando no botão de opção ao lado do tipo de erro ou tipo de arquivo.  No exemplo a seguir, estamos corrigindo um arquivo protegido por senha.

3. Clique em **nova correção de erro**.

    ![Correção de erro](../media/8c2faf1a-834b-44fc-b418-6a18aed8b81a.png)

    A sessão de correção de erro começa com um estágio de preparação onde os arquivos com erros são copiados para um local de armazenamento do Azure fornecido pela Microsoft para que você possa baixá-los para o computador local para correção.

    ![Preparando correção de erro](../media/390572ec-7012-47c4-a6b6-4cbb5649e8a8.png)

4. Após a conclusão da preparação, clique em **Avançar: baixar arquivos** para continuar com o download.

    ![Baixar arquivos](../media/6ac04b09-8e13-414a-9e24-7c75ba586363.png)

5. Para baixar arquivos, especifique o **caminho de destino para download**. Este é um caminho no computador local onde o arquivo é baixado.  O caminho padrão,%USERPROFILE%\Downloads\errors, aponta para a pasta downloads do usuário conectado. Você pode alterar esse caminho, se necessário. Se você alterar, recomendamos que você use um caminho de arquivo local para o melhor desempenho. Não use um caminho de rede remoto.

6. Copie o comando predefinido clicando em **copiar para área de transferência**. Inicie um prompt de comando do Windows, Cole o comando e pressione **Enter**.  

    Os arquivos são baixados.

    ![Preparar para correção de erros](../media/f364ab4d-31c5-4375-b69f-650f694a2f69.png)

    > [!NOTE]
    > Você deve usar o AzCopy v 8.1 para usar com êxito o comando fornecido na página **baixar arquivos** . Você também deve usar o AzCopy v 8.1 para carregar os arquivos na etapa 10 abaixo. Para instalar esta versão do AzCopy, confira [transferir dados com o AzCopy v 8.1 no Windows](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy). Se o comando AzCopy fornecido falhar, confira [solucionar problemas de AzCopy na descoberta eletrônica avançada](troubleshooting-azcopy.md).

7. Depois de baixar os arquivos, você pode corrigi-los com uma ferramenta apropriada. Para arquivos protegidos por senha, várias ferramentas de quebra de senha podem ser usadas. Se você souber as senhas dos arquivos, poderá abri-las e remover a proteção por senha.
    > [!NOTE]
    > É importante que você mantenha a estrutura de diretório e os nomes de arquivo dos arquivos corrigidos. Os nomes de caminho dos arquivos e pastas baixados possibilitam a Associação dos arquivos corrigidos aos arquivos originais.  Se a estrutura de diretório ou os nomes de arquivo forem alterados, você receberá o `Cannot apply Error Remediation to the current Workingset`seguinte erro:.

8. Agora, retorne à descoberta eletrônica avançada e clique em **Avançar: carregar arquivos**.  Isso passará para a próxima etapa, onde você pode agora carregar os arquivos.

    ![Carregar arquivos](../media/af3d8617-1bab-4ecd-8de0-22e53acba240.png)

9. Especifique o local dos arquivos corrigidos na caixa de texto **caminho para o local de arquivos** e clique em **copiar para área de transferência**.

10. Cole o comando em um prompt de comando do Windows e pressione **Enter** para carregar os arquivos.

    ![ff2ff691-629f-4065-9b37-5333f937daf6. png](../media/ff2ff691-629f-4065-9b37-5333f937daf6.png)

11. Retorne à descoberta eletrônica avançada e clique em **Avançar: processar arquivos**.

12. Quando o processamento estiver concluído. Você pode retornar ao conjunto de revisão e ver o arquivo corrigido.

## <a name="what-happens-when-files-are-remediated"></a>O que acontece quando os arquivos são corrigidos

Quando os arquivos corrigidos são carregados, os metadados originais são preservados, exceto os seguintes campos: 

- ExtractedTextSize
- HasText
- IsErrorRemediate
- Loadid
- ProcessingErrorMessage
- ProcessingStatus
- Texto
- WordCount
- WorkingsetId

Para obter uma definição de todos os campos de metadados na descoberta eletrônica avançada, confira [campos de metadados do documento](document-metadata-fields.md).

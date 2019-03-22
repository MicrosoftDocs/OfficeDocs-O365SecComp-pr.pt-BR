---
title: Solucionar problemas de AzCopy na descoberta eletrônica avançada (versão prévia)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 9711bee4ec9a61510b47568df37dfd3135e1e00c
ms.sourcegitcommit: cf9d9b545a7c153d314aa9c08c7fb16fcd785b3e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/21/2019
ms.locfileid: "30742491"
---
# <a name="troubleshoot-azcopy-in-advanced-ediscovery-preview"></a>Solucionar problemas de AzCopy na descoberta eletrônica avançada (versão prévia)

Ao carregar dados não-Office 365 ou documentos para correção de erros na descoberta eletrônica avançada (versão prévia), a interface do usuário fornece um comando do AzCopy do Azure que contém parâmetros com o local onde os arquivos que você deseja carregar estão armazenados e o Azure local de armazenamento no qual os arquivos serão carregados. Para carregar seus documentos, copie esse comando e execute-o em um prompt de comando no computador local.  A captura de tela a seguir mostra um exemplo de um comando do AzCopy:

![Carregar arquivos que não são do Office 365](../media/46ba68f6-af11-4e70-bb91-5fc7973516e3.png)

Na maioria dos casos, o comando fornecido funcionará quando você executá-lo. No enTanto, pode haver casos em que o comando exibido não seja executado com êxito. Veja alguns motivos possíveis.

## <a name="azcopy-isnt-installed-on-the-local-computer-or-its-not-installed-in-the-default-location"></a>O AzCopy não está instalado no computador local ou não está instalado no local padrão

Se o AzCopy não estiver instalado ou estiver instalado em um local diferente do local de instalação padrão (ou `%ProgramFiles(x86)%`seja), você pode receber o seguinte erro ao executar o comando AzCopy:

    The system cannot find the path specified.

Se o AzCopy não estiver instalado no computador local, você poderá instalar a partir daqui (não se esqueça de instalá-lo no local [https://docs.microsoft.com/azure/storage/common/storage-use-azcopy](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy)padrão):.


Se o AzCopy estiver instalado, mas estiver instalado em um local diferente do local padrão, você poderá copiar o comando, colá-lo em um arquivo de texto e alterar o caminho para o local em que o AzCopy está realmente instalado. Por exemplo, se Azcopy estiver localizado em `%ProgramFiles%`, então você poderá alterar a primeira parte do comando de `%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy.exe` para. `%ProgramFiles%\Microsoft SDKs\Azure\AzCopy` Após fazer essa alteração, copie-a do arquivo de texto e, em seguida, execute um prompt de comando.

> [!TIP]
> Se o AzCopy estiver instalado em um local diferente do local de instalação padrão, considere desinstalá-lo e, em seguida, instale-o novamente no local padrão. Isso ajudará a evitar esse problema no futuro.
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
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32241068"
---
# <a name="troubleshoot-azcopy-in-advanced-ediscovery-preview"></a><span data-ttu-id="23fce-102">Solucionar problemas de AzCopy na descoberta eletrônica avançada (versão prévia)</span><span class="sxs-lookup"><span data-stu-id="23fce-102">Troubleshoot AzCopy in Advanced eDiscovery (Preview)</span></span>

<span data-ttu-id="23fce-103">Ao carregar dados não-Office 365 ou documentos para correção de erros na descoberta eletrônica avançada (versão prévia), a interface do usuário fornece um comando do AzCopy do Azure que contém parâmetros com o local onde os arquivos que você deseja carregar estão armazenados e o Azure local de armazenamento no qual os arquivos serão carregados.</span><span class="sxs-lookup"><span data-stu-id="23fce-103">When loading non-Office 365 data or documents for error remediation in Advanced eDiscovery (Preview), the user interface supplies an Azure AzCopy command that contains parameters with the location of where the files that you want to upload are stored and the Azure storage location that the files will be uploaded to.</span></span> <span data-ttu-id="23fce-104">Para carregar seus documentos, copie esse comando e execute-o em um prompt de comando no computador local.</span><span class="sxs-lookup"><span data-stu-id="23fce-104">To upload your documents, you copy this command and then run it in a Command Prompt on your local computer.</span></span>  <span data-ttu-id="23fce-105">A captura de tela a seguir mostra um exemplo de um comando do AzCopy:</span><span class="sxs-lookup"><span data-stu-id="23fce-105">The follow screenshot shows an example of an AzCopy command:</span></span>

![Carregar arquivos que não são do Office 365](../media/46ba68f6-af11-4e70-bb91-5fc7973516e3.png)

<span data-ttu-id="23fce-107">Na maioria dos casos, o comando fornecido funcionará quando você executá-lo.</span><span class="sxs-lookup"><span data-stu-id="23fce-107">In most cases, the command that's provided will work when you run it.</span></span> <span data-ttu-id="23fce-108">No enTanto, pode haver casos em que o comando exibido não seja executado com êxito.</span><span class="sxs-lookup"><span data-stu-id="23fce-108">However, there may be cases when the command that's displayed will not run successfully.</span></span> <span data-ttu-id="23fce-109">Veja alguns motivos possíveis.</span><span class="sxs-lookup"><span data-stu-id="23fce-109">Here's a few possible reasons.</span></span>

## <a name="azcopy-isnt-installed-on-the-local-computer-or-its-not-installed-in-the-default-location"></a><span data-ttu-id="23fce-110">O AzCopy não está instalado no computador local ou não está instalado no local padrão</span><span class="sxs-lookup"><span data-stu-id="23fce-110">AzCopy isn't installed on the local computer or it's not installed in the default location</span></span>

<span data-ttu-id="23fce-111">Se o AzCopy não estiver instalado ou estiver instalado em um local diferente do local de instalação padrão (ou `%ProgramFiles(x86)%`seja), você pode receber o seguinte erro ao executar o comando AzCopy:</span><span class="sxs-lookup"><span data-stu-id="23fce-111">If AzCopy isn't installed or it's installed in a location other than the default install location (which is `%ProgramFiles(x86)%`), you may receive the following error when you run the AzCopy command:</span></span>

    The system cannot find the path specified.

<span data-ttu-id="23fce-112">Se o AzCopy não estiver instalado no computador local, você poderá instalar a partir daqui (não se esqueça de instalá-lo no local [https://docs.microsoft.com/azure/storage/common/storage-use-azcopy](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy)padrão):.</span><span class="sxs-lookup"><span data-stu-id="23fce-112">If AzCopy isn't install on the local computer, you can install from here (being sure to install it in the default location): [https://docs.microsoft.com/azure/storage/common/storage-use-azcopy](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy).</span></span>


<span data-ttu-id="23fce-113">Se o AzCopy estiver instalado, mas estiver instalado em um local diferente do local padrão, você poderá copiar o comando, colá-lo em um arquivo de texto e alterar o caminho para o local em que o AzCopy está realmente instalado.</span><span class="sxs-lookup"><span data-stu-id="23fce-113">If AzCopy is installed, but it's installed in a location different than the default location, you can copy the command, paste it to a text file, and then change the path to the location where AzCopy is actually installed.</span></span> <span data-ttu-id="23fce-114">Por exemplo, se Azcopy estiver localizado em `%ProgramFiles%`, então você poderá alterar a primeira parte do comando de `%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy.exe` para. `%ProgramFiles%\Microsoft SDKs\Azure\AzCopy`</span><span class="sxs-lookup"><span data-stu-id="23fce-114">For example, if Azcopy is located in `%ProgramFiles%`, then you can change the first part of the command from `%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy.exe` to `%ProgramFiles%\Microsoft SDKs\Azure\AzCopy`.</span></span> <span data-ttu-id="23fce-115">Após fazer essa alteração, copie-a do arquivo de texto e, em seguida, execute um prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="23fce-115">After you make this change, copy it from the text file and then run it a Command Prompt.</span></span>

> [!TIP]
> <span data-ttu-id="23fce-116">Se o AzCopy estiver instalado em um local diferente do local de instalação padrão, considere desinstalá-lo e, em seguida, instale-o novamente no local padrão.</span><span class="sxs-lookup"><span data-stu-id="23fce-116">If AzCopy is installed in a location other then the default install location, consider uninstalling it and then re-installing it in the default location.</span></span> <span data-ttu-id="23fce-117">Isso ajudará a evitar esse problema no futuro.</span><span class="sxs-lookup"><span data-stu-id="23fce-117">This will help prevent this issue in the future.</span></span>
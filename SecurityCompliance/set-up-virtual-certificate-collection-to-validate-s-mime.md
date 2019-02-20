---
title: Configurar coleção de certificados virtuais para validar S/MIME
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 04a616e6-197c-490c-ae8c-c8d5f0f0b3dd
description: s um administrador de locatários você precisará configurar uma coleção de certificados virtuais que será usada para validar certificados S/MIME.
ms.openlocfilehash: 0e8226ca35e872cd8c7da16ba353bf8b99a6954d
ms.sourcegitcommit: c94cb88a9ce5bcc2d3c558f0fcc648519cc264a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2019
ms.locfileid: "30091053"
---
# <a name="set-up-virtual-certificate-collection-to-validate-smime"></a><span data-ttu-id="561c9-103">Configurar coleção de certificados virtuais para validar S/MIME</span><span class="sxs-lookup"><span data-stu-id="561c9-103">Set up virtual certificate collection to validate S/MIME</span></span>

<span data-ttu-id="561c9-p101">Como um administrador de locatário, você precisará configurar uma coleção de certificados virtuais que será usada para validar certificados S/MIME. Esta coleção de certificados virtuais é configurada como um tipo de arquivo de repositório de certificados com uma extensão de nome de arquivo SST. O arquivo SST contém todos os certificados raiz e intermediários usados na validação de um certificado S/MIME.</span><span class="sxs-lookup"><span data-stu-id="561c9-p101">As a tenant administrator you will need to configure a virtual certificate collection that will be used to validate S/MIME certificates. This virtual certificate collection is set up as a certificate store file type with an SST filename extension. The SST file contains all the root and intermediate certificates that are used when validating an S/MIME certificate.</span></span>
  
## <a name="create-and-save-an-sst"></a><span data-ttu-id="561c9-107">Criar e salvar um SST</span><span class="sxs-lookup"><span data-stu-id="561c9-107">Create and save an SST</span></span>
<span data-ttu-id="561c9-108"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="561c9-108"></span></span>

<span data-ttu-id="561c9-p102">Você só pode usar o Shell para executar este procedimento. Para saber como abrir o Shell de gerenciamento do Exchange em sua organização local do Exchange, confira **abrir o Shell**. Para saber como usar o Windows PowerShell para se conectar ao Exchange Online, confira [conectar-se ao PowerShell do Exchange Online](https://go.microsoft.com/fwlink/p/?linkid=396554).</span><span class="sxs-lookup"><span data-stu-id="561c9-p102">You can only use the Shell to perform this procedure. To learn how to open the Exchange Management Shell in your on-premises Exchange organization, see **Open the Shell**. To learn how to use Windows PowerShell to connect to Exchange Online, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>
  
<span data-ttu-id="561c9-p103">Como administrador, você pode criar este arquivo SST exportando os certificados de uma máquina confiável usando o cmdlet  `Export-Certificate` e especificando o tipo como SST. Para obter mais informações sobre o cmdlet  `Export-Certificate`, consulte o tópico de referência sobre [Export-Certificate](https://docs.microsoft.com/en-us/powershell/module/pkiclient/export-certificate?view=win10-ps).</span><span class="sxs-lookup"><span data-stu-id="561c9-p103">As an administrator, you can create this SST file by exporting the certificates from a trusted machine using the  `Export-Certificate` cmdlet and specifying the type as SST. For more information the  `Export-Certificate` cmdlet, see the [Export-Certificate](https://docs.microsoft.com/en-us/powershell/module/pkiclient/export-certificate?view=win10-ps) reference topic.</span></span> 
  
<span data-ttu-id="561c9-p104">Assim que o arquivo SST for gerado, use o cmdlet  `Set-Smimeconfig` para salvá-lo no repositório de certificados virtuais usando o parâmetro  _-SMIMECertificateIssuingCA_. Por exemplo:  `Set-SmimeConfig -SMIMECertificateIssuingCA (Get-Content filename.sst -Encoding Byte)`</span><span class="sxs-lookup"><span data-stu-id="561c9-p104">Once the SST file is generated, use the  `Set-Smimeconfig` cmdlet to save it in the virtual certificate store by using the  _-SMIMECertificateIssuingCA_ parameter. For example:  `Set-SmimeConfig -SMIMECertificateIssuingCA (Get-Content filename.sst -Encoding Byte)`</span></span>
  
## <a name="ensuring-a-certificate-is-valid"></a><span data-ttu-id="561c9-116">Garantir que um certificado seja válido</span><span class="sxs-lookup"><span data-stu-id="561c9-116">Ensuring a certificate is valid</span></span>
<span data-ttu-id="561c9-117"><a name="sectionSection1"> </a></span><span class="sxs-lookup"><span data-stu-id="561c9-117"></span></span>

<span data-ttu-id="561c9-p105">O Exchange 2013 SP1 primeiro verifica o arquivo SST e valida o certificado. Se a validação falhar, ele examinará o repositório de certificados da máquina local para validar o certificado. Esse comportamento é novo no Exchange 2013 SP1 e diferente de versões anteriores do Exchange. No Exchange Online, somente o SST será usado para validação.</span><span class="sxs-lookup"><span data-stu-id="561c9-p105">Exchange 2013 SP1 first checks for the SST file and validates the certificate. If the validation fails, it will look at the local machine certificate store to validate the certificate. This behavior is new for Exchange 2013 SP1 and different from prior versions of Exchange. In Exchange Online only the SST will be used for validation.</span></span>
  
## <a name="more-information"></a><span data-ttu-id="561c9-122">Mais informações</span><span class="sxs-lookup"><span data-stu-id="561c9-122">More Information</span></span>
<span data-ttu-id="561c9-123"><a name="sectionSection2"> </a></span><span class="sxs-lookup"><span data-stu-id="561c9-123"></span></span>

[<span data-ttu-id="561c9-124">S/MIME para assinatura e criptografia de mensagens</span><span class="sxs-lookup"><span data-stu-id="561c9-124">S/MIME for message signing and encryption</span></span>](s-mime-for-message-signing-and-encryption.md)
  
[<span data-ttu-id="561c9-125">Get-SmimeConfig</span><span class="sxs-lookup"><span data-stu-id="561c9-125">Get-SmimeConfig</span></span>](http://technet.microsoft.com/library/4b29fa89-0840-4fe9-8885-019fcef2e02b.aspx)
  


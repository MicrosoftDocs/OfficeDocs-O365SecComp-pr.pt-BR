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
# <a name="set-up-virtual-certificate-collection-to-validate-smime"></a>Configurar coleção de certificados virtuais para validar S/MIME

Como um administrador de locatário, você precisará configurar uma coleção de certificados virtuais que será usada para validar certificados S/MIME. Esta coleção de certificados virtuais é configurada como um tipo de arquivo de repositório de certificados com uma extensão de nome de arquivo SST. O arquivo SST contém todos os certificados raiz e intermediários usados na validação de um certificado S/MIME.
  
## <a name="create-and-save-an-sst"></a>Criar e salvar um SST
<a name="sectionSection0"> </a>

Você só pode usar o Shell para executar este procedimento. Para saber como abrir o Shell de gerenciamento do Exchange em sua organização local do Exchange, confira **abrir o Shell**. Para saber como usar o Windows PowerShell para se conectar ao Exchange Online, confira [conectar-se ao PowerShell do Exchange Online](https://go.microsoft.com/fwlink/p/?linkid=396554).
  
Como administrador, você pode criar este arquivo SST exportando os certificados de uma máquina confiável usando o cmdlet  `Export-Certificate` e especificando o tipo como SST. Para obter mais informações sobre o cmdlet  `Export-Certificate`, consulte o tópico de referência sobre [Export-Certificate](https://docs.microsoft.com/en-us/powershell/module/pkiclient/export-certificate?view=win10-ps). 
  
Assim que o arquivo SST for gerado, use o cmdlet  `Set-Smimeconfig` para salvá-lo no repositório de certificados virtuais usando o parâmetro  _-SMIMECertificateIssuingCA_. Por exemplo:  `Set-SmimeConfig -SMIMECertificateIssuingCA (Get-Content filename.sst -Encoding Byte)`
  
## <a name="ensuring-a-certificate-is-valid"></a>Garantir que um certificado seja válido
<a name="sectionSection1"> </a>

O Exchange 2013 SP1 primeiro verifica o arquivo SST e valida o certificado. Se a validação falhar, ele examinará o repositório de certificados da máquina local para validar o certificado. Esse comportamento é novo no Exchange 2013 SP1 e diferente de versões anteriores do Exchange. No Exchange Online, somente o SST será usado para validação.
  
## <a name="more-information"></a>Mais informações
<a name="sectionSection2"> </a>

[S/MIME para assinatura e criptografia de mensagens](s-mime-for-message-signing-and-encryption.md)
  
[Get-SmimeConfig](http://technet.microsoft.com/library/4b29fa89-0840-4fe9-8885-019fcef2e02b.aspx)
  


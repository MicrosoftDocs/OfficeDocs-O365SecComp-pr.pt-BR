---
title: Tipos de arquivo com suporte na descoberta eletrônica avançada
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 378bd9ae88269d6a6d15a672473550e50179f772
ms.sourcegitcommit: 865b3dc071150b20bf3967e1263fc54e75898284
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/09/2019
ms.locfileid: "33834930"
---
# <a name="supported-file-types-in-advanced-ediscovery"></a>Tipos de arquivo com suporte na descoberta eletrônica avançada

A descoberta eletrônica avançada oferece suporte a vários tipos de arquivo e dá suporte a eles em diferentes níveis, que são descritos na tabela a seguir. Esta lista ainda não foi finalizada e adicionaremos novos tipos de arquivo, conforme continuamos com o teste de validação. A tabela também indica se um tipo de arquivo pode ser exibido nos visualizadores disponíveis em descoberta eletrônica avançada.

| Tipo MIME | Descrição | Visualizador nativo | Visualizador de texto | Visualizador de anotações | Extração de contêiner | Extensões |
| :- | :- | :- | :- | :- | :- | :- |
| aplicativo/mbox | Arquivo morto/contêiner |  |  |  | Sim | .mbox |
| application/msword | Produtividade | Sim | Sim | Sim |  | . doc;. dat |
| application/pdf | Produtividade | Sim | Sim | Sim |  | .pdf |
| Application/RTF | Documento | Sim | Sim | Sim |  | . rtf;. Doc |
| application/vnd. MS-Excel | Produtividade | Sim | Sim | Sim |  | . xls;. dat |
| application/vnd. MS-Excel. Sheet. Binary. macroenabled. 12 | Produtividade | Sim | Sim | Não |  | . xlsb |
| application/vnd. MS-Excel. Sheet. macroenabled. 12 | Produtividade | Sim | Sim | Sim |  | . xlsm |
| application/vnd. MS-Excel. Template. macroenabled. 12 | Produtividade | Não | Sim | Não |  | . xltm |
| application/vnd. MS-Outlook | Colaboração | Sim | Sim | Sim |  | . msg |
| application/vnd. MS-Outlook-PST | Arquivo morto/contêiner |  |  |  | Sim | . pst |
| application/vnd. ms-PowerPoint | Produtividade | Sim | Sim | Sim |  | . ppt;. PPS;. Pot |
| application/vnd. MS-Word. Document. macroenabled. 12 | Produtividade | Sim | Sim | Sim |  | .docm |
| application/vnd. MS-Word. Template. macroenabled. 12 | Produtividade | Sim | Sim | Sim |  | . dotm |
| application/vnd. Oasis. OpenDocument. Text | Produtividade | Sim | Sim | Sim |  | ODT  |
| application/vnd.openxmlformats-officedocument.presentationml.presentation | Produtividade | Sim | Sim | Sim |  | . pptx |
| application/vnd. openxmlformats-officeDocument. presentationml. slideshow | Produtividade | Sim | Sim | Sim |  | . ppsx |
| application/vnd. openxmlformats-officeDocument. presentationml. Template | Produtividade | Sim | Sim | Sim |  | . potx |
| application/vnd.openxmlformats-officedocument.spreadsheetml.sheet | Produtividade | Sim | Sim | Sim |  | . xlsx |
| application/vnd. openxmlformats-officeDocument. SpreadsheetML. Template | Produtividade | Sim | Sim | Sim |  | . xltx |
| application/vnd.openxmlformats-officedocument.wordprocessingml.document | Produtividade | Sim | Sim | Sim |  | . docx |
| application/vnd. openxmlformats-officeDocument. WordprocessingML. Template | Produtividade | Sim | Sim | Sim |  | . dotx |
| application/vnd. Visio | Produtividade | Sim | Sim | Sim |  | . vsd |
| aplicativo/x-7z-compactado | Arquivo morto/contêiner |  |  |  | Sim | .7z |
| aplicativo/XHTML + XML | Documento | Sim | Sim | Sim |  | . XHTML |
| aplicativo/XML | Documento | Sim | Sim | Sim |  | . xml |
| application/x-Msaccess | Produtividade | Sim | Sim | Sim |  | . mdb |
| aplicativo/x-mspublisher | Produtividade | Sim | Sim | Sim |  | . pub |
| application/x-rar-compactado | Arquivo morto/contêiner |  |  |  | Sim | . rar |
| application/x-tar | Arquivo morto/contêiner |  |  |  | Sim | . tar |
| aplicativo/zip | Arquivo morto/contêiner |  |  |  | Sim | . zip |
| imagem/BMP | Image | Sim | Sim | Sim |  | .bmp |
| imagem/EMF | Image | Sim | Sim | Sim |  | . EMF |
| image/gif | Image | Sim | Sim | Sim |  | .gif |
| image/jpeg | Image | Sim | Sim | Sim |  | . jpg;. jpeg;. dat;. jpgt |
| image/png | Image | Sim | Sim | Sim |  | .png |
| imagem/TIFF | Image | Sim | Sim | Sim |  | . tif |
| Image/vnd. dwg | Desenhos | Sim | Sim | Sim |  | . dwg;. DXF |
| imagem/WMF | Documento | Sim | Sim | Sim |  | . wmf |
| mensagem/RFC822 | Colaboração | Sim | Sim | Sim |  | . eml |
| texto/CSV | Documento | Sim | Sim | Sim |  | . csv |
| texto/HTML | Documento | Sim | Sim | Sim |  | . html;. shtml;. htm |
| texto/simples | Documento | Sim | Sim | Sim |  | . txt;. css;. con;. pl;. csv;. dat |
| texto/vCard-contato | Colaboração | Sim | Sim | Sim |  | . vcf |
||||||||

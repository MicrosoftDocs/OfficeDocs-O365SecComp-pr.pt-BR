---
title: Como o conteúdo é identificado para recomendações de governança de dados
ms.author: brendonb
author: stephow-MSFT
manager: laurawi
ms.date: 1/15/2019
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Priority
search.appverid:
- MOE150
- MET150
ROBOTS: NOINDEX, NOFOLLOW
description: O Centro de Segurança e Conformidade do Office 365 fornece recomendações para governança de dados com base na configuração atual da sua organização e permite que você configure as coisas com apenas alguns cliques. Algumas dessas recomendações detectam conteúdo específico em sua organização e, em seguida, fornecem etapas recomendadas para gerenciar esse conteúdo. Por exemplo, uma recomendação pode detectar itens que contenham conteúdo essencial para os negócios (como privilégio advogado-cliente ou informações do NDA) e permitir que você aplique automaticamente um rótulo de retenção a esses itens para garantir que eles sejam classificados e retidos conforme necessário. Este tópico lista as recomendações de controle de dados que você pode ver e descreve qual conteúdo é detectado para acionar cada um deles.
ms.openlocfilehash: a3f803105ea5c2626c8c2a26ad898df5f45af2f0
ms.sourcegitcommit: c7737903ff2e1d047682ee61f7ac21b0bdd1c6fd
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/16/2019
ms.locfileid: "28263934"
---
# <a name="how-content-is-identified-for-data-governance-recommendations"></a>Como o conteúdo é identificado para recomendações de governança de dados

O Centro de Segurança e Conformidade do Office 365 fornece recomendações para governança de dados com base na configuração atual da sua organização e permite que você configure as coisas com apenas alguns cliques. Algumas dessas recomendações detectam conteúdo específico em sua organização e, em seguida, fornecem etapas recomendadas para gerenciar esse conteúdo. Por exemplo, uma recomendação pode detectar itens que contenham conteúdo essencial para os negócios (como privilégio advogado-cliente ou informações do NDA) e permitir que você aplique automaticamente um rótulo de retenção a esses itens para garantir que eles sejam classificados e retidos conforme necessário.

Este tópico lista as recomendações de controle de dados que você pode ver e descreve qual conteúdo é detectado para acionar cada um deles.

## <a name="clean-up-voicemail"></a>Limpar a caixa postal

Essa recomendação é exibida quando as mensagens de e-mail identificadas como o tipo de mensagem "correio de voz" são detectadas nas caixas de correio dos usuários. Saiba mais sobre em [propriedades de mensagem do Exchange](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/ediscovery/message-properties-and-search-operators?view=exchserver-2019#searchable-properties-in-exchange).

## <a name="label-attorney-client-privilege-content"></a>Etiquetar conteúdo de privilégio advogado-cliente 

Este recomendação é exibida quando os seguintes critérios são atendidos.

- Qualquer combinação dessas palavras-chave for detectada no corpo da mensagem de email:
    - ACP
    - Privilégio advogado cliente
    - Privilégio advogado-cliente
    - Advogado-cliente privilegiados

- Qualquer combinação dessas palavras-chave é detectada em arquivos do SharePoint ou no OneDrive:
    - ACP
    - Advogado cliente privilégio *
    - Privilégio AC

## <a name="retain-audio-files"></a>Manter os arquivos de áudio

Este recomendação é exibida quando qualquer um dos seguintes tipos de arquivo é detectado no SharePoint ou OneDrive.

- .MP3
- .WMA
- .WAV
- .RA
- .RAM
- .RM
- .MID
- .OGG
- .AIFF
- .PCM
- .AAC
- .FLAC
- .ALAC

## <a name="retain-cad-files"></a>Manter os arquivos do CAD

Este recomendação é exibida quando qualquer um dos seguintes tipos de arquivo é detectado no SharePoint ou OneDrive.

- .3DXML
- .ACIS
- .ARC
- .ASM
- .CAT*
- .CGR
- .DW
- .DX
- .EDRW
- .IAM
- .IGES
- .IGS
- .IPT
- .JT
- .MF1
- .NEU
- .NOMINAL
- .PKG
- .PRC
- .PRT
- .PSM
- .PWD
- .SLD*
- .STEP
- .STL
- .STP
- .U3D
- .UNV
- .VRML
- .WRL
- .X_*
- .XAS
- .XMT*
- .XPR

## <a name="retain-image-files"></a>Manter os arquivos de imagem

Este recomendação é exibida quando qualquer um dos seguintes tipos de arquivo é detectado no SharePoint ou OneDrive.

- .JPEG
- .GIF
- .TIF*
- .BMP
- .PNG
- .RAW
- .PSD
- .PSP
- .JPG
- .EXIF
- .PPM
- .PGM
- .PBM
- .PNM
- .WEBP

## <a name="retain-nda-content"></a>Reter o conteúdo NDA 

Este recomendação é exibida quando os seguintes critérios são atendidos.

- Qualquer combinação dessas palavras-chave for detectada no corpo da mensagem de email:
    - NDA
    - "Contrato de não-divulgação"
    - "Contrato de não divulgação"

- Qualquer combinação dessas palavras-chave é detectada em arquivos .PDF ou .DOC no SharePoint ou no OneDrive:
    - NDA
    - Contrato de não divulgação

## <a name="retain-software-development-files"></a>Manter os arquivos de desenvolvimento de software

Este recomendação é exibida quando qualquer um dos seguintes tipos de arquivo é detectado no SharePoint ou OneDrive.

- .ASAX
- .ASM
- .ASP*
- .BAT
- .CONFIG
- .CS
- .CSS
- .DISCO
- .HTM*
- .INC
- .JAD
- .JAVA
- .JS*
- .LIB
- .O
- .PHP
- .RC
- .RESX
- .RPT
- .RSS
- .SCPT
- .SRC
- .VB*
- .WSF
- . XCODEPROJ
- .XML
- .XSD
- .XSL*

## <a name="retain-video-files"></a>Manter os arquivos de vídeo

Este recomendação é exibida quando qualquer um dos seguintes tipos de arquivo é detectado no SharePoint ou OneDrive.

- .AVCHD
- .AVI
- .FLV
- .MOV
- .MP2V
- .MP4
- .MP4V
- .MPE
- .MPEG
- .MPEG1
- .MPEG2
- .MPEG4
- .MPG
- .MPG2
- .MPG4
- .WMV
- .XMV

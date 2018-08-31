---
title: Criptografia de serviço do Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Resumo: Entenda a resiliência de dados no Microsoft Office 365.'
ms.openlocfilehash: 1273cd5556bf51dcdac9bbde1b3e8003ab818811
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524058"
---
# <a name="office-365-service-encryption"></a>Criptografia de serviço do Office 365

Além de usar a criptografia de nível de volume, o Exchange Online, Skype para negócios, SharePoint Online e OneDrive for Business também usar o serviço de criptografia para criptografar dados do cliente. Permite a criptografia de serviço para duas opções de gerenciamento de chaves:
- A Microsoft gerencia todas as chaves de criptografia. (Essa opção é está disponível atualmente no SharePoint Online, o OneDrive for Business e Skype para negócios. É atualmente no roadmap para Exchange Online.)
- O cliente fornece chaves de raiz usadas com a criptografia de serviço e o cliente gerencia essas chaves usando Vault de chave do Windows Azure. A Microsoft gerencia todas as outras chaves. Essa opção é chamada de chave de cliente e está atualmente disponível para o Exchange Online, SharePoint Online e OneDrive for Business. (Anteriormente conhecido como criptografia avançada com BYOK. Consulte [transparência de Enhancing e controle para clientes do Office 365](http://blogs.office.com/2015/04/21/enhancing-transparency-and-control-for-office-365-customers/) para o comunicado original.)

Criptografia de serviço oferece vários benefícios. Por exemplo, ele:
- fornece recursos de gerenciamento e a proteção na parte superior de proteção de criptografia forte de direitos.
- inclui uma opção de chave de cliente que habilita os serviços de multilocatários fornecer o gerenciamento de chaves por locatário.
- fornece a separação dos administradores de sistema operacional Windows contra o acesso aos dados do cliente armazenados ou processadas pelo sistema operacional.
- aumenta a capacidade do Office 365 para atender às demandas dos clientes que tenham requisitos de conformidade referentes à criptografia.

## <a name="customer-key"></a>Chave do Cliente
Usando a chave do cliente, você poderá gerar seus próprios chaves de criptografia usando um HSM local ou o Azure Vault de chave. Independentemente de como a chave é gerada, os clientes usar Azure chave Vault para controlar e gerenciar as chaves de criptografia usadas pelo Office 365. Depois que as chaves estiverem armazenadas no Azure chave Vault, eles podem ser atribuídos às cargas de trabalho, como o Exchange Online e SharePoint Online e costumava como raiz do conjunto de chaves usado para criptografar seus dados de caixa de correio e os arquivos. Um dos outros benefícios do uso de chave do cliente é controlar a capacidade da Microsoft para processar dados de cliente. Esse recurso existe para que um cliente que deseja remover dados do Office 365 (por exemplo, quando um cliente termina o serviço com a Microsoft ou remove uma parte dos dados armazenados na nuvem) pode fazê-lo e usar chave do cliente como um controle técnico para assegurar que ninguém , incluindo Microsoft, pode acessar ou processar os dados. Isso é Além disso (e um complemento) o recurso de Lockbox de cliente que pode ser usado para controlar o acesso aos dados do cliente pela equipe da Microsoft.

Para saber como configurar a chave do cliente para o Office 365 para Exchange Online, Skype para negócios, SharePoint Online e OneDrive for Business, consulte [controlar seus dados no Office 365 usando a chave do cliente](https://support.office.com/article/Controlling-your-data-in-Office-365-using-Customer-Key-f2cd475a-e592-46cf-80a3-1bfb0fa17697). Para obter informações adicionais, consulte a [Chave do cliente para perguntas Frequentes do Office 365](https://support.office.com/article/Customer-Key-for-Office-365-FAQ-41ae293a-bd5c-4083-acd8-e1a2b4329da6)e [Gerenciar e controle as necessidades de seus dados para ajudar a atender a conformidade com a chave do cliente](https://techcommunity.microsoft.com/t5/Microsoft-Ignite-Content-2017/Manage-and-control-your-data-to-help-meet-compliance-needs-with/td-p/117580).

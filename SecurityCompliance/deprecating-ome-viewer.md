---
title: ReProvando o aplicativo visualizador de criptografia de mensagens do Office 365
ms.author: krowley
author: kccross
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 6336cabb-b06e-402f-9e85-8bb9eb4ce68f
description: No dia 15 de agosto de 2018, iremos remover o aplicativo móvel do Visualizador de criptografia de mensagens do Office 365 (OME) do Android e dos repositórios da Apple. O aplicativo móvel Office 365 Message Encryption Viewer era necessário para ler mensagens de email e anexos que foram criptografados com a versão anterior do OME em telefones Apple e Android. Além de remover o aplicativo OME Viewer, não estamos fazendo outras alterações na versão anterior do OME.
ms.openlocfilehash: e08b6ecac9d68d7aa8e9e1d6cca6450a6461f67e
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216831"
---
# <a name="deprecating-office-365-message-encryption-viewer-app"></a>ReProvando o aplicativo visualizador de criptografia de mensagens do Office 365

No dia 15 de agosto de 2018, iremos remover o aplicativo móvel do Visualizador de criptografia de mensagens do Office 365 (OME) do Android e dos repositórios da Apple. O aplicativo móvel Office 365 Message Encryption Viewer era necessário para ler mensagens de email e anexos que foram criptografados com a versão anterior do OME em telefones Apple e Android. Além de remover o aplicativo OME Viewer, não estamos fazendo outras alterações na versão anterior do OME.
  
## <a name="changes-beginning-august-2018"></a>Alterações começando em agosto de 2018

Conforme anunciado em setembro, lançamos uma nova versão da [criptografia de mensagem do Office 365](https://aka.ms/ome2017) para que os usuários possam enviar mensagens criptografadas e protegidas para qualquer pessoa dentro ou fora da organização, sem a necessidade do aplicativo móvel. Desde então, adicionamos recursos adicionais: 
  
- [Modelo somente criptografia](https://aka.ms/encryptonly)
    
- [Controle para descriptografar anexos](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Admin-control-for-attachments-now-available-in-Office-365/ba-p/204007)
    
Com essa alteração, os usuários não poderão mais baixar o aplicativo móvel do Office 365 Message Encryption Viewer, começando em 1º de agosto. Como resultado, os destinatários de email podem não conseguir ler mensagens criptografadas com a versão anterior do OME em alguns dispositivos móveis Android e Apple. No enTanto, eles ainda poderão ler essas mensagens em computadores pessoais (por meio de navegadores da área de trabalho). Os usuários que já baixaram o aplicativo continuarão a ser capazes de usá-lo.
  
## <a name="why-this-change-was-made"></a>Por que essa alteração foi feita

A nova versão do OME não requer mais um aplicativo móvel para ler mensagens de email e anexos protegidos. Os clientes do Office 365 que usam os novos recursos do OME podem exibir a mensagem protegida no Outlook Mobile e os clientes não-Office 365 podem exibir mensagens protegidas em um navegador.
  
Exigir que os usuários baixem um aplicativo móvel é outro obstáculo para os clientes exibirem mensagens protegidas. Os novos recursos de criptografia de mensagem do Office 365 oferecem uma experiência móvel melhor.
  
## <a name="can-i-still-use-the-previous-version-of-office-365-message-encryption"></a>Ainda posso usar a versão anterior da criptografia de mensagem do Office 365

A versão anterior da criptografia de mensagem do Office 365 não será preterida no momento, no entanto, fizemos melhorias significativas na nova versão da criptografia de mensagem do Office 365, o que facilita a criptografia e os direitos de proteção de dados confidenciais para qualquer pessoa e, em qualquer dispositivo, incluindo a capacidade de os usuários do Office 365 lerem mensagens protegidas diretamente no Outlook (desktop, Mobile e Web). 
  
## <a name="what-do-i-need-to-do-to-prepare-for-this-change"></a>O que eu preciso fazer para se preparar para essa alteração

Se sua organização envia atualmente anexos criptografados para destinatários que exigem o aplicativo visualizador do OME, você deve atualizar a documentação e os recursos de treinamento.
  
Recomendamos a atualização de regras de fluxo de emails existentes do Exchange para usar a versão atual do OME para que sua organização possa aproveitar os recursos novos e aprimorados. Depois de configurar os novos recursos do OME, os destinatários não precisarão que o aplicativo do OME Viewer Leia mensagens criptografadas em dispositivos móveis.
  
A Microsoft recomenda que você faça um plano para migrar para os novos recursos do OME assim que for razoável para sua organização. Para obter instruções, consulte [configurar novos recursos de criptografia de mensagem do Office 365](set-up-new-message-encryption-capabilities.md). Se quiser saber mais sobre como os novos recursos funcionam primeiro, confira criptografia de [mensagem do Office 365](ome.md).
  


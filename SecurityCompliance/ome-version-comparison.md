---
title: Comparação de versão de criptografia de mensagem do Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
description: Ajuda explicam as diferenças nos recursos entregues com diferentes versões do Office 365 Message Encryption, bem como as duas continuam a trabalhar juntos.
ms.openlocfilehash: a418d840c7e0eb50ae076bf2b03164bef9488058
ms.sourcegitcommit: 88f3982217c29b558e3f9e838bcb425da395dd5e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/02/2019
ms.locfileid: "29708538"
---
# <a name="compare-versions-of-ome"></a>Comparar versões de OME

Este artigo compara herdado Office 365 Message Encryption para os novos recursos OME. As novas capacidades são uma fusão e a versão mais recente do OME tanto gerenciamento de direitos de informação (IRM). Também abordaremos como os dois podem coexistir em sua organização do Office 365.

||
|:-----|
|Este artigo faz parte de uma maior série de artigos sobre o Office 365 Message Encryption. Este artigo destina-se aos administradores e profissionais de TI. Se você apenas estiver procurando informações sobre como enviar ou receber uma mensagem criptografada, consulte a lista de artigos no [Office 365 Message Encryption (OME)](ome.md) e localize o artigo que atenda às suas necessidades. |
||

## <a name="side-by-side-comparison-of-features-and-capabilities"></a>Lado a lado de comparação de recursos e capacidades

|                                   |Recursos antigos       |                   |Novos recursos              |
|-----------------------------------|-------------------|-------------------|--------------------------|
|**Funcionalidade**                     | **OME herdado**    | **IRM**           | **Novos recursos OME** |
|*Enviar um email criptografado*        |Por meio de regras de fluxo de correio do Exchange|Usuários finais iniciados a partir da área de trabalho do Outlook ou do Outlook na Web; ou regras de fluxo de emails por meio do Exchange|Usuários finais iniciados a partir da área de trabalho do Outlook, o Outlook para Mac ou Outlook na Web; por meio de regras de transporte do Exchange e o Office 365 Data Loss Prevention (DLP)|
|*Modelo de gerenciamento de direitos*       |   N/D      |Faça a opção não encaminhar e modelos personalizados|Faça a opção não encaminhar, opção somente criptografar e modelos personalizados|
|*Tipo de destinatário*                   |Destinatários internos e externos|Somente a destinatários internos         |Destinatários internos e externos|
|*Experiência para destinatário interno*|Os destinatários recebem uma mensagem HTML, que eles baixado e aberto em um navegador da web ou aplicativos móveis|Experiência de embutida nativo nos clientes do Outlook|Experiência de nativo embutida para destinatários do Office 365. Todos os destinatários podem ler mensagem do portal OME (nenhum download ou app necessário).|
|*Experiência para destinatário externo*|Os destinatários recebem uma mensagem HTML, que eles baixado e aberto em um navegador da web ou aplicativos móveis|N/D|Experiência de nativo embutida para destinatários do Office 365. Todos os destinatários podem ler mensagem do portal OME (nenhum download ou app necessário).|
|*Permissões de anexo*           |Sem restrições em anexos|Anexos estão protegidos|Anexos estão protegidos para a opção não encaminhar e modelos personalizados. Admins pode escolher se anexos para a opção somente criptografar são protegidos ou não.|
|*Traga seu próprio suporte de chave (BYOK)*|Nenhum                |Nenhum               |BYOK suportado          |
||

## <a name="advantages-of-using-the-new-ome-capabilities-over-legacy-ome"></a>Vantagens de usar os novos recursos OME vez OME herdado

Os novos recursos oferecem as seguintes vantagens:

- Capacidade de usar criptografar somente (que permite a colaboração segura), não encaminhar, bem como restrições personalizadas.
- Remetentes podem enviar emails criptografados com os novos recursos manualmente a partir da área de trabalho do Outlook, o Outlook para Mac e o Outlook nos clientes da web.
- Os destinatários do Office 365 chegar ao usar uma experiência embutida em clientes Outlook suportados. Como alternativa, os administradores podem optar por mostrar uma experiência com marca de destinatários do Office 365.
- Contas fora do Office 365, como contas do Gmail, Yahoo! e da Microsoft, são federadas com o portal OME, que fornece uma melhor experiência de usuário para que esses destinatários. Todas as outras identidades usam uma senha única para acessar mensagens criptografadas.
- Administradores podem personalizar a identidade visual e criar vários modelos de marcas.
- Os administradores podem revogar emails criptografados com os novos recursos.
- Os novos recursos fornecem relatórios de uso detalhado por meio de segurança &amp; Centro de conformidade.

## <a name="coexistence-of-legacy-ome-and-the-new-capabilities-in-the-same-tenant"></a>Coexistência de OME herdado e os novos recursos no mesmo inquilino

Você pode usar o OME herdado e os novos recursos no mesmo inquilino. Como administrador, você fazer isso, escolhendo qual versão do OME que você deseja usar ao criar seu correio regras do fluxo.

- Para especificar a versão herdada do OME, use a ação de regra de fluxo de email Exchange "Aplicar a versão anterior do OME".
- Para especificar os novos recursos, use a Exchange mail flow regra ação "aplicar o Office 365 mensagem criptografia e direitos de proteção".

Os usuários também podem enviar email criptografado com os novos recursos manualmente a partir da área de trabalho do Outlook, o Outlook para Mac e o Outlook nos clientes da web.

## <a name="migrating-from-legacy-ome-to-the-new-capabilities"></a>Migrando do OME herdado para os novos recursos

Embora as duas versões do OME podem coexistir, é altamente recomendável que você edite suas regras de fluxo de email antigo que usam a ação de regra "Aplicam-se a versão anterior do OME" para usar os novos recursos, especificando a ação de regra de fluxo de email "Aplicar Office 365 Message Encryption e proteção de direitos". Para obter instruções, consulte [definir regras de fluxo de email para criptografar mensagens de email no Office 365](define-mail-flow-rules-to-encrypt-email.md).

## <a name="getting-started-with-ome"></a>Introdução ao OME

Normalmente, as novas capacidades OME são automaticamente habilitadas para sua organização do Office 365. Se você estiver pronto para começar a usar os novos recursos OME dentro da sua organização, consulte [configurar novos recursos do Office 365 Message Encryption](set-up-new-message-encryption-capabilities.md).

A versão herdada do OME é automaticamente habilitada para a sua organização do Office 365 se você habilitou a proteção de informações do Windows Azure. No passado, OME herdado funcionou mesmo se não foi habilitado para a proteção de informações do Windows Azure. Isso não é mais o caso.

Para começar a usar o OME legado, se você tiver habilitado a proteção de informações do Windows Azure, tudo o que você precisa fazer é configurar as regras de fluxo de email que usam a ação de regra "Aplicar a versão anterior do OME". Para obter instruções, consulte [definir regras de fluxo de email para criptografar mensagens de email no Office 365](define-mail-flow-rules-to-encrypt-email.md).
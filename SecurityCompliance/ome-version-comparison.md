---
title: Comparação de versões do Office 365 Message Encryption (OME)
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
description: Ajuda a explicar as diferenças nos recursos entregues com diferentes versões da criptografia de mensagem do Office 365 e como os dois continuam a trabalhar juntos.
ms.openlocfilehash: bb13208e2b630c8a6217b78b48a4cd3bb4b0de79
ms.sourcegitcommit: 895f67531f2b4afe46c7487ca5b44555ca791bae
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/12/2019
ms.locfileid: "31836835"
---
# <a name="compare-versions-of-ome"></a>Comparar versões de OME

Este artigo compara a criptografia de mensagem do Office 365 (OME) herdada com os novos recursos do OME. Os novos recursos são uma fusão e uma versão mais recente do OME e do gerenciamento de direitos de informação (IRM). As características exclusivas de implantação no GCC alto também são descritas. Também abordaremos como os dois podem coexistir na sua organização do Office 365.

||
|:-----|
|Este artigo faz parte de uma série maior de artigos sobre a criptografia de mensagens do Office 365. Este artigo destina-se a administradores e ITPros. Se você estiver apenas procurando informações sobre como enviar ou receber uma mensagem criptografada, consulte a lista de artigos na [ome (criptografia de mensagens do Office 365)](ome.md) e localize o artigo que melhor atende às suas necessidades. |
||

## <a name="side-by-side-comparison-of-features-and-capabilities"></a>Comparação de recursos e recursos lado a lado

|                                   |Recursos antigos       |                   |Novos recursos              |
|-----------------------------------|-------------------|-------------------|--------------------------|
|**Funcionalidade**                     | **OME herdado**    | **IRM**           | **Novos recursos do OME** |
|*Enviar um email criptografado*        |Por meio de regras de fluxo de email do Exchange|O usuário final iniciou a partir do Outlook na Web ou do Outlook na Web; ou por meio de regras de fluxo de email do Exchange|Usuário final iniciado a partir da área de trabalho do Outlook, Outlook para Mac ou Outlook na Web; por meio de regras de fluxo de email do Exchange (também conhecidas como regras de transporte) e prevenção de perda de dados do Office 365 (DLP)|
|*Modelo de gerenciamento de direitos*       |   N/D      |Opção não enCaminhar e modelos personalizados|Opção não enCaminhar, opção somente criptografia e modelos personalizados|
|*Tipo de destinatário*                   |Destinatários internos e externos|Somente destinatários internos         |Destinatários internos e externos|
|*Experiência para o destinatário interno*|Os destinatários recebem uma mensagem HTML, que eles baixam e abrem em um navegador da Web ou aplicativo móvel|Experiência interna nativa em clientes do Outlook|Experiência interna nativa para destinatários do Office 365. Todos os outros destinatários podem ler a mensagem do portal do OME (sem download ou aplicativo necessário).|
|*Experiência para destinatário externo*|Os destinatários recebem uma mensagem HTML, que eles baixam e abrem em um navegador da Web ou aplicativo móvel|N/D|Experiência interna nativa para destinatários do Office 365. Todos os outros destinatários podem ler a mensagem do portal do OME (sem download ou aplicativo necessário).|
|*Permissões de anexo*           |Sem restrições em anexos|Os anexos estão protegidos|Os anexos são protegidos para a opção não enCaminhar e modelos personalizados. Os administradores podem escolher se os anexos da opção somente criptografia estão protegidos ou não.|
|*Dê suporte a sua própria chave (BYOK)*|Nenhum                |Nenhum               |BYOK com suporte          |
||

## <a name="advantages-of-the-new-ome-capabilities-over-legacy-ome"></a>Vantagens dos novos recursos do OME sobre o OME herdado

Os novos recursos oferecem as seguintes vantagens:

- Capacidade de usar somente criptografia (o que permite colaboração segura), não enCaminhar e restrições personalizadas.
- Os remetentes podem enviar emails criptografados com os novos recursos manualmente da área de trabalho do Outlook, do Outlook para Mac e do Outlook nos clientes Web.
- Os destinatários do Office 365 utilizam uma experiência embutida em clientes do Outlook com suporte. Como alternativa, os administradores podem optar por mostrar aos destinatários do Office 365 uma experiência com identidade visual.
- As contas fora do Office 365, como Gmail, Yahoo e contas da Microsoft, são federadas com o portal do OME, que oferece uma experiência de usuário melhor para esses destinatários. Todas as outras identidades usam um código de passagem única para acessar mensagens criptografadas.
- Os administradores podem personalizar a identidade visual e criar vários modelos de identidade visual.
- Os administradores podem revogar emails criptografados com os novos recursos.
- Os novos recursos fornecem relatórios de uso detalhados por &amp; meio do centro de conformidade de segurança.

## <a name="unique-characteristics-of-office-365-message-encryption-in-a-gcc-high-deployment"></a>Características exclusivas da criptografia de mensagem do Office 365 em uma implantação avançada GCC

Se você planeja usar a criptografia de mensagem do Office 365 em um ambiente de maior GCC, há algumas características exclusivas sobre a experiência do destinatário.

### <a name="encrypted-email-from-gcc-high-to-gcc-high-recipients"></a>Emails criptografados de destinatários de GCC alto a GCC

Os remetentes podem criptografar manualmente emails no Outlook para PC e Mac e Outlook na Web, ou as organizações podem configurar uma política para criptografar emails usando regras de fluxo de email do Exchange.

Os destinatários dentro do GCC têm alta recepção da mesma experiência de leitura embutida no Outlook para PC e Mac e Outlook na Web como todos os outros usuários do Office 365.

### <a name="encrypted-email-from-gcc-high-to-non-gcc-high-recipients"></a>Email criptografado de GCC elevado para destinatários não-GCC altos

Os remetentes com GCC alta podem enviar emails criptografados fora do maior limite do GCC.

Todos os destinatários fora do GCC superior, incluindo os usuários do Office 365, usuários do Outlook.com e outros usuários de outros provedores de email, como Gmail e Yahoo, recebem um email de wrapper que redireciona o destinatário para o portal do OME onde o destinatário pode ler e responder à mensagem.

## <a name="coexistence-of-legacy-ome-and-the-new-capabilities-in-the-same-tenant"></a>A coexistência de OME herdados e os novos recursos no mesmo locatário

Você pode usar o OME herdado e os novos recursos no mesmo locatário. Como administrador, você faz isso escolhendo qual versão do OME você deseja usar ao criar suas regras de fluxo de emails.

- Para especificar a versão herdada do OME, use a ação regra de fluxo de email do Exchange **aplicar a versão anterior do ome**.
- Para especificar os novos recursos, use a ação de regra de fluxo de email do Exchange **aplica a criptografia de mensagem do Office 365 e a proteção de direitos**.

Os usuários podem enviar emails manualmente, que são criptografados com os novos recursos da área de trabalho do Outlook, do Outlook para Mac e do Outlook na Web.

## <a name="migrate-from-legacy-ome-to-the-new-capabilities"></a>Migrar do OME herdado para os novos recursos

Embora ambas as versões do OME possam coexistir, é altamente recomendável que você edite suas regras de fluxo de email antigas que usam a ação de regra **aplique a versão anterior do ome** para usar os novos recursos. Atualizar essas regras para usar a ação de regra de fluxo de emails **aplique a criptografia de mensagens e a proteção de direitos do Office 365**. Para obter instruções, consulte [definir regras de fluxo de emails para criptografar mensagens de email no Office 365](define-mail-flow-rules-to-encrypt-email.md).

## <a name="get-started-with-ome"></a>Introdução ao OME

Normalmente, os novos recursos do OME são automaticamente habilitados para sua organização do Office 365. Para obter mais informações sobre os novos recursos do OME em sua organização, consulte [configurar novos recursos de criptografia de mensagens do Office 365](set-up-new-message-encryption-capabilities.md).

A versão herdada do OME é automaticamente habilitada para sua organização do Office 365 se você tiver habilitado a proteção de informações do Azure. No passado, o OME herdado funcionou, mesmo se a proteção de informações do Azure não estivesse habilitada. Isso não acontece mais.

Para começar a usar o OME herdado, se você tiver habilitado a proteção de informações do Azure, basta configurar as regras de fluxo de email que usam a ação de regra **aplicar a versão anterior do ome**. Para obter instruções, consulte [definir regras de fluxo de emails para criptografar mensagens de email no Office 365](define-mail-flow-rules-to-encrypt-email.md).
---
title: Passo a passo percepção de inteligência de falsificação
ms.author: krowley
author: kccross
ms.date: 7/30/2018
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 59a3ecaf-15ed-483b-b824-d98961d88bdd
description: Veja como a novo percepção de inteligência de falsificação funciona.
ms.openlocfilehash: ca9c4ae6f2d65ef2700a2e02acd5b4f1dfbfe903
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22596090"
---
# <a name="walkthrough-spoof-intelligence-insight"></a>Passo a passo: percepção de inteligência de falsificação

Usando a percepção de falsificação de inteligência de dados, você pode determinar rapidamente quais remetentes legitimamente estão enviando a que você não autenticado email. Permitindo que eles enviem mensagens falsificadas, você pode reduzir o risco de falsos positivos indo para seus usuários.
  
Além disso, você também pode usar o monitor de inteligência de falsificação e gerenciar pares de domínio permitidos para oferecer uma camada adicional de segurança e evitar que as mensagens não seguras que chegam na sua organização.
  
Você pode usar a percepção de inteligência de falsificação na segurança &amp; Centro de conformidade, se a sua conta de trabalho ou da escola é concedida permissões de leitor de segurança, administrador de segurança ou administrador global do Office 365. Para obter mais informações, consulte [permissões no Office 365 Security &amp; Centro de conformidade](permissions-in-the-security-and-compliance-center.md).
  
Se estiver familiarizado com [relatórios e ideias de segurança do Office 365 &amp; Centro de conformidade](reports-and-insights-in-security-and-compliance.md), ele pode ser útil para visualizar como você pode facilmente navegar de um painel para um insight e ações recomendadas.
  
Você pode visualizar a percepção de inteligência falsificação de mais de um painel na segurança &amp; Centro de conformidade. Independentemente de qual painel que você estiver examinando, o insight fornece detalhes mesmos e lhe permite realizar rapidamente as mesmas tarefas.
  
Essa é uma das diversas orientações para a segurança &amp; Centro de conformidade. Sobre como navegar em relatórios e ideias, veja a passo a passo na seção Tópicos relacionados.
  
## <a name="getting-to-the-spoof-intelligence-insight-in-the-security-amp-compliance-center"></a>Conhecendo a percepção de inteligência de falsificação na segurança &amp; Centro de conformidade

1. Para começar, você precisará [vá para a segurança &amp; Centro de conformidade](go-to-the-securitycompliance-center.md).
    
2. Na segurança &amp; Centro de conformidade, vá para o **Gerenciamento de ameaça** \> **Dashboard.**
    
3. Na linha **ideias** , procure a percepção de inteligência de falso. Se você tiver habilitado a falsificação de inteligência de dados, então a percepção é chamada **domínios falsificado que apresentaram falhas de autenticação dos últimos 30 dias**. Se você ainda não habilitou a proteção de falsificação, então a percepção solicitará a fazê-lo usando o título **Habilitar falsificação da proteção**. 
    
## <a name="about-the-insight-on-the-dashboard"></a>Sobre as visões sobre o painel

As visões sobre o painel mostra informações como esta.
  
![Captura de tela da percepção de inteligência de falsificação](media/28aeabac-c1a1-4d16-9fbe-14996f742a9a.png)
  
Este insight possui dois modos:
  
 **Modo de percepção**. Se você tiver qualquer política de falsificação habilitada, então a percepção mostra quantos emails foram impactados por nossos recursos de inteligência de falsificação nos últimos 30 dias. 
  
 **e se o modo**. Se você não tiver qualquer política de falsificação habilitada, então a percepção mostra quantos emails *seria* ter sido afetados pelo nossos recursos de inteligência de falsificação nos últimos 30 dias. 
  
De qualquer forma, os domínios falsificados exibidos na percepção estão divididos em duas categorias; os pares de domínio suspeitos e pares de domínio não suspeitos. Essas categorias são posteriormente divididas em três partições diferentes para que você revise. 
  
Um *par de domínio* é uma combinação do "de:" endereço e a infra-estrutura de envio. 
  
- O endereço "De" é o endereço exibido como o endereço de ao seu aplicativo de email. Esse endereço identifica o autor do email. Ou seja, a caixa de correio da pessoa ou do sistema responsável pela elaboração a mensagem. Às vezes, isso é chamado de endereço de 5322.From.
    
- A infra-estrutura de envio ou remetente, é o domínio organizacional do registro PTR do endereço IP de envio. Se o endereço IP de envio não tem nenhum registro PTR, então o remetente é identificado pelo IP de envio com o 255.255.255.0 máscara de sub-rede na notação CIDR (/ 24). Por exemplo, se o endereço IP for 192.168.100.100 o endereço IP completo do remetente é 192.168.100.100/24.
    
 **Os pares de domínio suspeitos** incluem: 
  
- **Falsificação de alta confiabilidade**. O Office 365 recebida sinais fortes que esses domínios são suspeitos, com base nos padrões de envio históricos e a pontuação de reputação dos domínios. O Office 365 está altamente confiante de que os domínios são falsificação e que as mensagens enviadas desses domínios são menos suscetíveis a ser legítimo. 
    
- **Falsificação da confiança moderado**. O Office 365 recebida moderados sinais que esses domínios são suspeitos, com base em padrões de envio históricos e a pontuação de reputação dos domínios. O Office 365 é relativamente confiante de que os domínios são falsificação e que as mensagens enviadas desses domínios são legítimas. No processo de Balde tem uma chance maior de contendo falsos positivos (FPs) que o Balde de falsificação de alta confiabilidade. 
    
 **Pares de domínio suspeitos de não** incluir **recuperada falso**. Realizar a falsificação recuperada são domínios que tenham falhou as verificações de autenticação explícita ( [SPF](https://docs.microsoft.com/office365/SecurityCompliance/how-office-365-uses-spf-to-prevent-spoofing), [DKIM](https://docs.microsoft.com/office365/SecurityCompliance/use-dkim-to-validate-outbound-email), [DMARC](https://docs.microsoft.com/office365/SecurityCompliance/use-dmarc-to-validate-email)), mas passadas nossas verificações de autenticação estendida. Como resultado, o Office 365 recuperada do email em seu nome e nenhuma ação antifalsificação foi executada em relação a email. 
  
## <a name="view-detailed-information-about-suspicious-domain-pairs-from-the-spoof-intelligence-insight"></a>Exibir informações detalhadas sobre os pares de domínio suspeitos da percepção de inteligência de falsificação

1. Na percepção de inteligência de falso, clique em qualquer um dos pares de domínio (altos, moderados ou recuperados).
  
A página de **Falsificação da inteligência Insight** aparece mostrando a você uma lista de remetentes que estão enviando email não-autenticado em sua organização. As informações nesta página ajuda a determinar se as mensagens de falsas são autorizadas ou não, ou se você precisa fazer outra ação. Você pode classificar as informações por contagem de mensagem, a data em que a falsificação da última foi detectada, e muito mais. (Clique títulos de coluna, **a contagem de mensagem** ou **visto pela última vez**, por exemplo). 
    
2. Selecionar um item na tabela para abrir um painel de detalhes que contém informações avançadas sobre o par de domínio, incluindo por que podemos percebeu que isso, o que você precisa fazer, um resumo de domínio, dados WhoIs sobre o remetente e semelhantes emails que vimos no seu locatário do mesmo remetente. A partir daqui, você também pode optar por adicionar ou remover o par de domínio da lista de remetentes seguros **AllowedToSpoof** . 
  
![Captura de tela de um domínio no painel de detalhes do falsificação intelligence insight](media/03ad3e6e-2010-4e8e-b92e-accc8bbebb79.png)
  
## <a name="add-or-remove-a-domain-from-the-allowedtospoof-safe-sender-list"></a>Adicionar ou remover um domínio da lista de remetentes seguros AllowedToSpoof

Adicionar ou remover um domínio da lista de remetentes seguros AllowedToSpoof ao revisar o par de domínio no painel de detalhes da percepção de inteligência de falso. Basta defina a alternância adequadamente.
  
Isso modifica a combinação de par de domínio exclusivo do domínio falsificado e a infra-estrutura de envio e não fornece cobertura para todo o domínio falsificado ou da infra-estrutura de envio no isolamento. Por exemplo, se você adicionar o seguinte par de domínio ao remetente 'AllowedToSpoof' lista de permissões: *Falsificado domínio* "gmail.com" e a *Infra-estrutura de envio* "tms *. mx.com",* e em seguida, somente os emails de par desse domínio poderão falsificar. Outros remetentes tentar falsificar "gmail.com" e outros domínios que "tms.mx.com" tentam falsificar continuará serão protegidas pelo intelligence falso. 
  
## <a name="related-topics"></a>Tópicos relacionados

[Saiba mais sobre a inteligência de falsificação](learn-about-spoof-intelligence.md)
  
[Proteção antifalsificação no Office 365](anti-spoofing-protection.md)
  
[Passo a passo – de um painel para um insight](from-a-dashboard-to-an-insight.md)
  
[Passo a passo – de um relatório detalhado para um insight](from-a-detailed-report-to-an-insight.md)
  
[Passo a passo – de um insight para um relatório detalhado](from-an-insight-to-a-detailed-report.md)
  


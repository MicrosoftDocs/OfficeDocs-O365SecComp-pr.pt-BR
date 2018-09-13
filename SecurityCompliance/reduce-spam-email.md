---
title: Como reduzir emails de spam no Office 365
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/7/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Priority
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 07824c51-2c45-4005-8596-03c0d7c4ff2a
description: Aprenda as maneiras mais comuns de reduzir spam e lixo eletrônico no Office 365.
ms.openlocfilehash: e462bbb11862d795650b6378cd5de2681f0edf74
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524134"
---
# <a name="how-to-reduce-spam-email-in-office-365"></a>Como reduzir emails de spam no Office 365

 **Você está recebendo muito spam no Office 365? Faça o seguinte.**
  
Vários problemas com spam no Office 365 podem ser resolvidos pela opção [Exibir cabeçalhos de email](https://support.office.com/article/cd039382-dc6e-4264-ac74-c048563d212c) e determinar o que deu errado. Se você vir um cabeçalho de mensagem chamado X-Forefront-Antispam-Report que contém a cadeia de caracteres SFV:NSPM, isso significará que a Proteção do Exchange Online (EOP) analisou a mensagem e não achou que fosse spam. Nesse caso, recomendamos que você [Use o suplemento Mensagem de Relatório](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) para ajudar a melhorar nossos filtros. Se você não vir esse valor nos cabeçalhos, isso poderá significar que o email não passou pela verificação de spam ou que houve um problema de configuração que fez a mensagem ser ignorada. Nesse caso, confira as informações abaixo. 
  
Saiba mais sobre [cabeçalhos de mensagem antispam](https://technet.microsoft.com/library/dn205071%28v=exchg.150%29.aspx).
  
## <a name="solutions-to-common-causes-of-getting-too-much-spam"></a>Soluções para causas comuns de recebimento de muito spam

Para evitar que você receba muito spam, a Proteção do Exchange Online (EOP) exige que os administradores concluam algumas tarefas. Se você não for o administrador do locatário do Office 365 e estiver recebendo muito spam, fale com seu administrador sobre essas tarefas. Caso contrário, ignore e vá até a seção do usuário.
  
### <a name="for-admins"></a>Para administradores

- **Aponte seus registros DNS para o Office 365** Para a EOP fornecer proteção, os registros DNS do servidor de mensagens (MX) de todos os domínios devem ser apontados para o Office 365 e somente para ele. Se seu [MX não apontar para o Office 365](https://blogs.msdn.microsoft.com/tzink/2017/12/28/if-you-use-office-365-but-your-mx-record-doesnt-point-to-office-you-may-want-to-close-down-your-security-settings/), a EOP não fornecerá a filtragem de spam para seus usuários. Confira [Criar registros DNS para o Office 365 ao gerenciar seus registros DNS](https://support.office.com/article/b0f3fdca-8a80-4e8e-9ef3-61e8a2a9ab23).
    
- **Habilitar a regra de lixo eletrônico em todas as caixas de correio** Por padrão, a ação de filtragem de spam é definida como **Mover mensagem para a pasta Lixo eletrônico**. Se esta for a ação de política de spam preferida e atual, toda caixa de correio [também deverá ter a regra de lixo eletrônico habilitada](https://blogs.msdn.microsoft.com/tzink/2017/12/14/making-sure-your-junk-email-filtering-is-enabled-in-office-365/). Para verificar isso, você pode executar o cmdlet Get-MailboxJunkEmailConfiguration em uma ou mais caixas de correio. Por exemplo, você pode verificar se isso se aplica a todas as caixas de correio executando o seguinte: Get-MailboxJunkEmailConfiguration -Identity \* | Where {$_.Enabled -eq $false}
    
    Ao se exibir a saída, a propriedade Enable deve ser definida como True. Se ela estiver definida como False, você poderá executar Set-MailboxJunkEmailConfiguration para alterá-la para True.
    
- **Verificar suas regras de fluxo de email e listas de confiança** Procure no cabeçalho da mensagem uma mensagem que deve ter sido marcada como spam. Localize a propriedade SCL no cabeçalho X-Forefront-Antispam-Report. Se o valor do SCL for -1, isso indicará que a mensagem foi listada com segurança e contornou a filtragem de spam da EOP. Investigue regras de fluxo de email, listas de permissões e a lista de remetentes permitidos do destinatário. Um [Localizar e corrigir problemas de entrega de email como administrador do Office 365 para empresas](https://support.office.com/article/e7758b99-1896-41db-bf39-51e2dba21de6) também será útil para fornecer detalhes sobre por que uma mensagem recebeu um SCL -1. 
    
- **Criar regras de fluxo de email no servidor Exchange no local** Se você estiver usando a Proteção do Exchange Online, mas suas caixas de correio estiverem localizadas no Exchange Server Local, você precisará criar algumas regras de fluxo de emails no Exchange Server Local. Confira as [instruções para somente EOP](https://technet.microsoft.com/library/ms.exch.eac.EditAntispamPolicy_SpamAction%28EXCHG.150%29.aspx?v=15.20.548.14&amp;l=1&amp;s=BPOS_S_E15_0).
    
- **Marcar emails em massa como spam** Emails em massa são emails de newsletter nos quais os usuários podem ter se inscrito, mas ainda assim podem ser indesejados. No cabeçalho da mensagem, localize a propriedade BCL (Nível de Confiança em Massa) no cabeçalho X-Microsoft-Antispam. Se o valor de BCL for menor que o limite definido no filtro de spam, ajuste o limite para marcar esses tipos de mensagens em massa como spam. Usuários diferentes têm tolerâncias e preferências diferentes para [como o email em massa é tratado](https://blogs.msdn.microsoft.com/tzink/2014/08/25/different-levels-of-bulk-mail-filtering-in-office-365/). Você pode criar regras ou políticas diferentes para atender a diferentes preferências do usuário. 
    
- **Bloquear um remetente imediatamente** Caso você precise bloquear um remetente imediatamente, poderá bloquear por endereço de email, domínio ou endereço IP. Confira [Bloquear spam de email com o filtro de spam do Office 365 para evitar problemas de falso negativo](block-email-spam-to-prevent-false-negatives.md). Uma entrada em uma lista de permissões de usuário final pode substituir um bloqueio definido pelo administrador.
    
- **Habilitar o suplemento de mensagem de relatório para usuários** Recomendamos que você [habilite o suplemento de mensagem de relatório para os usuários](enable-the-report-message-add-in.md). Como administrador, você também poderá exibir os comentários que seus usuários estão enviando e usar os padrões para ajustar as configurações que podem causar problemas.
    
### <a name="for-users"></a>Para usuários

- **Habilitar a regra de lixo eletrônico e verificar sua lista de permissões** Verifique se a regra de ação de lixo eletrônico está habilitada e se o remetente ou domínio do remetente não está definido para ignorar em sua lista de permissões pessoal. A melhor maneira de acessar essas configurações é em [Bloquear ou permitir (configurações de lixo eletrônico)](https://support.office.com/article/48c9f6f7-2309-4f95-9a4d-de987e880e46). Enquanto estiver ali, você também pode optar por bloquear o endereço de email ou domínio do remetente.
    
- **Relatar o spam à Microsoft** Relatar mensagens de spam para a Microsoft usando a opção [Usar o suplemento Mensagem de Relatório](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2). Além disso, você pode enviar uma mensagem para junk@office365.microsoft.com e anexe uma ou mais mensagens ao relatório.
    
    **Importante** Se você não encaminhar as mensagens como anexos, [os cabeçalhos estarão ausentes e não poderemos melhorar](https://blogs.msdn.microsoft.com/tzink/2017/11/30/when-creating-support-tickets-about-spam-be-sure-to-include-message-headers/) a filtragem de lixo eletrônico no Office 365. 
    
- **Cancelar inscrição de emails em massa** Se a mensagem foi um newsletter no qual você se inscreveu (boletins informativos, lançamentos de produto etc.) e contiver um link Cancelar inscrição de uma fonte respeitável, basta cancelar a inscrição. O Office 365 normalmente não trata essas mensagens como spam. Você também pode optar por bloquear o remetente ou pedir para seu administrador fazer uma alteração que fará com que todos os emails em massa sejam tratados como spam. 
    


---
title: Como impedir que emails reais sejam marcados como spam no Office 365
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
ms.assetid: 34823bbc-a3e3-4949-ba42-97c73997eeed
description: Saiba como manter emails reais fora do lixo eletrônico e impedir que sejam marcadas como spam no Office 365.
ms.openlocfilehash: 4da27aea157d3d816f8ce9a9631dd608dd5cd164
ms.sourcegitcommit: 03b9221d9885bcde1cdb5df2c2dc5d835802d299
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29614425"
---
# <a name="how-to-prevent-real-email-from-being-marked-as-spam-in-office-365"></a>Como impedir que emails reais sejam marcados como spam no Office 365

 **Seu email real está sendo marcado como spam no Office 365? Faça isso.**
  
A Proteção do Exchange Online (EOP) tenta filtrar spams, manter sua caixa de entrada livre de conteúdo que os usuários não desejam ver. Mas, às vezes, o EOP filtra o que você deseja ver.
  
## <a name="determine-the-reason-why-the-message-was-marked-as-spam"></a>Determinar o motivo pelo qual a mensagem foi marcada como spam

Para resolver muitos problemas de spam no Office 365, confira o artigo [Exibir cabeçalhos de mensagens de email](https://support.office.com/article/cd039382-dc6e-4264-ac74-c048563d212c) e determine o que deu errado. Procure um cabeçalho chamado X-Forefront-Antispam-Report. [Saiba mais sobre cabeçalhos de mensagem antispam](https://technet.microsoft.com/library/dn205071%28v=exchg.150%29.aspx).
  
No cabeçalho, procure os cabeçalhos e os valores a seguir.
  
### <a name="x-forefront-antispam-report"></a>X-Forefront-Antispam-Report

- **SFV:SPM** Indica que a mensagem foi marcada como spam devido aos filtros de spam da Proteção do Exchange Online. 

- **SFV:BLK** Indica que a mensagem foi marcada como spam porque o endereço de envio está na lista de Remetentes Bloqueados do destinatário. 
    
- **SFV:SKS** Indica que a mensagem foi marcada como spam antes do filtro de conteúdo. Isso pode incluir uma regra de transporte marcando a mensagem como spam. Execute um rastreamento de mensagens para ver se uma regra de transporte disparada pode ter definido um nível de confiança alto de spam (SCL). 
    
- **SFV:SKB** Indica que a mensagem foi marcada como spam porque correspondeu a uma lista de bloqueios na política de filtro de spam. 
    
- **SFV:Bulk** Indica que o valor do Nível de Reclamação em Massa (BCL) localizado no cabeçalho x-microsoft-antispam está acima do limite de massa que foi definido para o filtro de conteúdo. Emails em massa são emails que os usuários podem ter se inscrito para receber, mas ainda assim podem ser indesejados. No cabeçalho da mensagem, localize a propriedade BCL (Nível de Confiança em Massa) no cabeçalho X-Microsoft-Antispam. Se o valor de BCL for menor que o limite definido no filtro de spam, ajuste o limite para marcar esses tipos de mensagens em massa como spam. Usuários diferentes têm tolerâncias e preferências diferentes para [como o email em massa é tratado](https://docs.microsoft.com/pt-BR/office365/SecurityCompliance/bulk-complaint-level-values). Você pode criar regras ou políticas diferentes para atender a diferentes preferências do usuário.
    
- **CAT:SPOOF** ou **CAT:PHISH** Indica que a mensagem parece ser falsa, ou seja, a fonte da mensagem não pode ser validada e pode ser suspeita. Se for válida, o remetente precisará garantir que ele tenha a configuração correta de DKIM e SPF. Verifique o cabeçalho Authentication-Results para obter mais informações. Embora possa ser difícil fazer todos os remetentes usarem métodos adequados de autenticação de email, ignorar essas verificações podem ser muito perigoso e é a principal causa de comprometimentos. 
    
### <a name="x-customspam"></a>x-customspam

- A presença desse cabeçalho indica que a mensagem foi marcada como spam porque uma das [opções avançadas de spam está habilitada](https://technet.microsoft.com/library/jj200750%28v=exchg.150%29.aspx) no filtro de spam. A menos que você precise desses recursos, recomendamos usar as configurações padrão. 
    
## <a name="solutions-to-additional-causes-of-too-much-spam"></a>Soluções para outras causas de excesso de spam

Para trabalhar com eficiência, a Proteção do Exchange Online (EOP) exige que os administradores concluam algumas tarefas. Se você não for o administrador do locatário do Office 365 e estiver recebendo muito spam, fale com seu administrador sobre essas tarefas. Caso contrário, ignore e vá até a seção do usuário.
  
### <a name="for-admins"></a>Para administradores

- **Aponte seus registros de DNS para o Office 365** Para que o EOP ofereça proteção, os registros DNS do seu servidor de mensagens (MX) para todos os domínios devem apontar para o Office 365 e apenas para o Office 365. Se seu MX não apontar para o Office 365, o EOP não fornecerá filtragem de spam para seus usuários. Se você desejar usar outro dispositivo ou serviço para fornecer a filtragem de spam do seu domínio, desabilite a proteção contra spam no EOP. Você pode fazer isso criando uma regra de transporte que defina o valor do SCL como -1. Se você mais tarde decidir usar o EOP, remova essa regra de transporte. 
    
- **Desabilitar a filtragem de SmartScreen no Outlook** Se os usuários estiverem usando o cliente de área de trabalho do Outlook, desabilite a funcionalidade de filtragem de SmartScreen, que foi descontinuada. Se estiver habilitado, ela poderá causar falsos positivos. Isso não será necessário se o cliente de área de trabalho do Outlook estiver atualizado. 
    
- **Habilitar o suplemento de mensagem de relatório para usuários** Recomendamos que você [habilite o suplemento de mensagem de relatório para os usuários](enable-the-report-message-add-in.md). Como administrador, você também poderá exibir os comentários que seus usuários estão enviando e usar os padrões para ajustar as configurações que podem causar problemas. 
    
- **Imediatamente permitir um remetente** Caso você precise imediatamente permitir um remetente, recomendamos que você **APENAS permita o endereço IP do remetente específico**. Como alternativa, você pode permitir um remetente e confira se o remetente passa em uma verificação de autenticação, como SPF ou DKIM ao criar uma regra de transporte que procura **as duas coisas**: um domínio do remetente e um cabeçalho Authentication-Results bem-sucedido. 
    
### <a name="for-users"></a>Para usuários

- **Relatar o spam à Microsoft** Relatar mensagens de spam para a Microsoft usando a opção [Usar o suplemento Mensagem de Relatório](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2). Além disso, você pode enviar uma mensagem para junk@office365.microsoft.com e anexe uma ou mais mensagens ao relatório.
    
    **Importante** Se você não encaminhar as mensagens como anexos, os cabeçalhos estarão ausentes e não poderemos melhorar a filtragem de lixo eletrônico no Office 365. 
    
- **Adicionar um remetente a sua lista de permissões, mas use com moderação** Como último recurso, você pode [Bloquear ou permitir (configurações de lixo eletrônico)](https://support.office.com/article/48c9f6f7-2309-4f95-9a4d-de987e880e46). Se fizer isso, esteja ciente de que uma tentativa de phishing direcionada poderá ter acesso a sua caixa de entrada.

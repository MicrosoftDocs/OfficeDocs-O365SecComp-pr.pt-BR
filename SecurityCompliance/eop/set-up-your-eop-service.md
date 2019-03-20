---
title: Configurar seu serviço EOP
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/23/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: d74c6ddf-11b0-43ee-b298-8bb0340895f0
description: Este tópico explica como configurar a Proteção do Exchange Online (EOP) da Microsoft. Se você foi direcionado do Assistente de domínios do Office 365, volte para o Assistente de domínios do Office 365 se você não quiser usar o Proteção do Exchange Online. Se você quiser mais informações sobre como configurar conectores, confira Configure mail flow using connectors in Office 365.
ms.openlocfilehash: 7c5b80ffa103f3ec9b554f69e4bc8ceeccaa6c22
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/20/2019
ms.locfileid: "30692700"
---
# <a name="set-up-your-eop-service"></a>Configurar seu serviço EOP

Este tópico explica como configurar a Proteção do Exchange Online (EOP) da Microsoft. Se você foi direcionado do Assistente de domínios do Office 365, volte para o Assistente de domínios do Office 365 se você não quiser usar o Proteção do Exchange Online. Se você quiser mais informações sobre como configurar conectores, confira [Configure mail flow using connectors in Office 365](http://technet.microsoft.com/library/854b5a50-4462-4836-a092-37e208d29624.aspx).
  
> [!NOTE]
> Este tópico assume que você tenha caixas de correio locais e que você queira protegê-las com a EOP, o que é conhecido como cenário autônomo. Se você deseja hospedar todas as suas caixas de correio na nuvem com o Exchange Online, não precisa concluir todas as etapas deste tópico. Acesse o [Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=286312) para se inscrever e comprar caixas de correio em nuvem. Se você quiser hospedar algumas de suas caixas de correio no local e algumas na nuvem, isso se chama cenário híbrido. Ele requer configurações de fluxo de email mais avançadas. [Exchange Server 2013 Hybrid Deployments](http://technet.microsoft.com/library/59e32000-4fcf-417f-a491-f1d8f9aeef9b.aspx) explica o fluxo de correio híbrido e possui links para recursos que mostram como configurá-lo. 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>O que você precisa saber antes de começar?

- Tempo estimado para a conclusão da tarefa: 1 hora
    
- Para configurar conectores, você precisa ter uma conta de administrador global do Office 365 ou de administrador da empresa do Exchange (grupo de funções do Gerenciamento de Organização). Para obter mais informações sobre como as permissões do Office 365 se relacionam às permissões do Exchange, confira [Permissões no Office 365](https://go.microsoft.com/fwlink/p/?LinkID=335814).
    
- Se você ainda não se inscreveu na EOP, visite [Proteção do Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=282660) para comprar ou experimentar o serviço. 
    
- Para informações sobre atalhos de teclado que possam se aplicar aos procedimentos neste tópico, consulte **Keyboard shortcuts in Exchange 2013**.
    
> [!TIP]
> Está enfrentando problemas? Peça ajuda nos fóruns do Exchange. Visite os fóruns em: [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), ou [Proteção do Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=285351). 
  
## <a name="how-do-you-do-this"></a>Como fazer isso?

### <a name="step-1-use-the-microsoft-365-admin-center-to-add-and-verify-your-domain"></a>Etapa 1: usar o centro de administração do Microsoft 365 para adicionar e verificar seu domínio

1. No centro de administração do Microsoft 365, navegue até **configuração** para adicionar seu domínio ao serviço. 
    
    Não sabe onde encontrar o centro de administração do Microsoft 365? Saiba mais em [sobre o centro de administração do Microsoft 365](https://go.microsoft.com/fwlink/p/?LinkId=521888).
    
2. Siga as etapas para adicionar os registros DNS aplicáveis ao seu provedor de hospedagem de DNS, a fim de verificar a propriedade do domínio.
    
> [!TIP]
> [Adicionar o domínio ao Office 365](https://support.office.com/en-us/article/add-a-domain-to-office-365-6383f56d-3d09-4dcb-9b41-b5f5a5efd611) e [Criar registros DNS para Office 365](https://support.office.com/en-us/article/create-dns-records-at-any-dns-hosting-provider-for-office-365-7b7b075d-79f9-4e37-8a9e-fb60c1d95166) são recursos úteis para referenciar conforme você adicionar o seu domínio ao serviço e configurar o DNS. 
  
### <a name="step-2-add-recipients-and-optionally-enable-dbeb"></a>Etapa 2: Adicionar destinatários e, opcionalmente, habilitar o DBEB

Antes de configurar seu email para entrar e sair do serviço da EOP, recomendamos que adicione seus destinatários ao serviço. Existem várias maneiras de fazer isso, conforme documentado no [Gerenciar usuários de email no EOP](manage-mail-users-in-eop.md). Se desejar habilitar o Bloqueio de Borda Baseado em Diretório (DBEB) para impor a verificação de destinatário dentro do serviço após adicionar seus destinatários, deverá configurar o tipo do seu domínio para Autoritativo. Para obter mais informações sobre o DBEB, consulte [Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx).
  
### <a name="step-3-use-the-eac-to-set-up-mail-flow"></a>Etapa 3: Usar o EAC para configurar o fluxo de emails

Crie conectores no EAC (Centro de administração do Exchange) que permitem o fluxo de emails entre a EOP e os servidores de email locais. Para saber mais detalhes, confira [Set up connectors to route mail between Office 365 and your own email servers](http://technet.microsoft.com/library/2e93fd60-a5ef-4e64-8e62-2b862b2d1033.aspx).
  
#### <a name="how-do-you-know-this-task-worked"></a>Como saber se essa tarefa funcionou?

Use o Analisador de Conectividade Remota para executar um teste que verifica o fluxo de mensagens entre o serviço e o seu ambiente. Para obter mais informações, consulte a seção "Usar o Analisador de Conectividade Remota para testar a entrega de email", em[Testing Mail Flow with the Remote Connectivity Analyzer](http://technet.microsoft.com/library/6c8c2964-d553-4329-8166-6e508dd63fa0.aspx).
  
### <a name="step-4-allow-inbound-port-25-smtp-access"></a>Etapa 4: Permitir acesso SMTP através da porta de entrada 25

Após configurar os conectores, espere 72 horas para permitir a propagação das atualizações dos registros de DNS. Depois, restrinja o tráfego SMTP da porta de entrada 25 no seu firewall ou servidores de mensagens para aceitar mensagens apenas de datacenters da EOP, especificamente dos endereços de IP listados em [Endereços de IP do Exchange Online Protection](exchange-online-protection-ip-addresses.md). Isso protege seu ambiente local limitando o escopo de mensagens de entrada que você pode receber. Além disso, atualize também quaisquer configurações em seu servidor de mensagens que controlam os endereços IP que podem se conectar para retransmitir mensagens.
  
> [!TIP]
> Configure o servidor SMTP com um tempo limite de conexão de 60 segundos. Essa configuração é aceita na maioria das situações, o que fornece um pequeno atraso no caso de uma mensagem enviada com um anexo grande, por exemplo. 
  
### <a name="step-5-use-the-shell-to-ensure-that-spam-is-routed-to-each-users-junk-email-folder"></a>Etapa 5: Usar o Shell para se certificar que spam é roteado para a pasta de email de lixo eletrônico de cada usuário

Para garantir que o spam (lixo eletrônico) é roteado corretamente para a pasta de Lixo Eletrônico de cada usuário, é necessário realizar alguns passos de configuração. As etapas são fornecidas [para garantir que o spam seja roteado para a pasta lixo eletrônico de cada usuário](../ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md).
  
Se não quiser mover mensagens para a pasta de Lixo Eletrônico de cada usuário, você pode escolher outra ação editando suas políticas de filtro de conteúdo no centro de administração do Exchange. Para saber mais, confira [Configure your spam filter policies](../configure-your-spam-filter-policies.md).
  
### <a name="step-6-use-the-microsoft-365-admin-center-to-point-your-mx-record-to-eop"></a>Etapa 6: usar o centro de administração do Microsoft 365 para apontar o seu registro MX para o EOP

Siga as etapas de configuração de domínio do Office 365 para atualizar o registro MX do seu domínio, para que haja fluxo da EOP no seu email de entrada. Certifique-se de apontar seu registro MX diretamente para a EOP em vez de ter um serviço de filtragem de terceiros relacionado ao email para a EOP. Para saber mais, você pode consultar novamente [Criar registros DNS para o Office 365](https://go.microsoft.com/fwlink/p/?LinkId=304219).
  
#### <a name="how-do-you-know-this-task-worked"></a>Como saber se essa tarefa funcionou?

Use o Analisador de Conectividade Remota para executar um teste que verifica o seu registro MX. Para obter mais informações, consulte a seção "Usar o Analisador de Conectividade Remota para testar seu registro MX e conector de saída" em [Testing Mail Flow with the Remote Connectivity Analyzer](http://technet.microsoft.com/library/6c8c2964-d553-4329-8166-6e508dd63fa0.aspx). 
  
Neste ponto, você já verificou se o conector de saída local da entrega de serviço está corretamente configurado bem como se o seu registro MX está apontando para a EOP. Agora, você pode optar por executar os seguintes testes adicionais para verificar se um email será entregue com êxito pelo serviço para o seu ambiente local:
  
- No Analisador de Conectividade Remota, clique na guia **Office 365** e execute o teste **Email SMTP de Entrada** localizado em **Testes de Email da Internet**. 
    
- Envie uma mensagem de email de qualquer conta de email baseado na Web para um destinatário de email de sua organização cujo domínio corresponde ao domínio que você adicionou ao serviço. Confirme a entrega da mensagem para a caixa de correio no local usando o Microsoft Outlook ou outro cliente de email.
    
- Se você deseja executar um teste de email enviado, envie uma mensagem de email de um usuário de sua organização para uma conta de email baseada na Web e confirme se a mensagem foi recebida.
    
> [!TIP]
> Quando você tiver concluído a configuração, não precisa executar etapas adicionais para fazer com que a EOP remova spam e malware. A EOP remove spam e malware automaticamente. No entanto, você pode ajustar as configurações na EAC de acordo com as necessidades da empresa. Para obter mais informações, consulte [Anti-Spam and Anti-Malware Protection](http://technet.microsoft.com/library/93c6c227-7442-4293-b64d-ec8f15c928db.aspx). > Agora que o serviço está em execução, recomendamos a leitura do[Práticas recomendadas para a configuração do EOP](best-practices-for-configuring-eop.md), que descreve as configurações e as considerações recomendadas para depois da configuração da EOP. 
  


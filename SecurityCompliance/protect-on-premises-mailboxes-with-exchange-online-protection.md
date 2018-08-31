---
title: Proteger as caixas de correio no local com Exchange Online Protection
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/1/2017
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- GEU150
- GMA150
- GPA150
- MET150
ms.assetid: c5e95951-da67-4ec7-92c5-982abd477e69
description: Mesmo se você pretende hospedar algumas ou todas sua caixas de correio local, você ainda pode proteger as caixas de correio com o Exchange Online Protection (EOP). Para configurar conectores, sua conta deve ser um Administrador Global do Office 365 ou um administrador de empresa do Exchange (o grupo de funções de gerenciamento da organização). Para obter informações sobre como o Office 365 permissões se relacionam com permissões do Exchange, consulte atribuindo funções de administrador no Office 365 operado pela 21Vianet. Se todas as suas caixas de correio do Exchange estão no local, siga estas etapas para configurar seu serviço EOP.
ms.openlocfilehash: 4751bb2183e61d292805d1799519644b77b08c2a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524706"
---
# <a name="protect-on-premises-mailboxes-with-exchange-online-protection"></a>Proteger as caixas de correio no local com Exchange Online Protection

> [!NOTE]
> Este artigo se aplica apenas ao Office 365 operado pela 21Vianet na China. 
  
Mesmo se você pretende hospedar algumas ou todas sua caixas de correio local, você ainda pode proteger as caixas de correio com o Exchange Online Protection (EOP). Para configurar conectores, sua conta deve ser um Administrador Global do Office 365 ou um administrador de empresa do Exchange (o grupo de funções de gerenciamento da organização). Para obter informações sobre como o Office 365 permissões se relacionam com permissões do Exchange, consulte [Atribuindo funções de administrador no Office 365 operado pela 21Vianet](https://support.office.com/article/d58b8089-cbfd-41ec-b64c-9cfcbef495ac). Se todas as suas caixas de correio do Exchange estão no local, siga estas etapas para configurar seu serviço EOP. 
  
## <a name="step-1-use-the-office-365-admin-center-to-add-and-verify-your-domain"></a>Etapa 1: Usar o Centro de administração do Office 365 para adicionar e verificar o domínio

1. No Centro de administração do Office 365, navegue para a Instalação para adicionar seu domínio ao serviço.
    
2.  Siga as etapas no portal para adicionar os registros DNS aplicáveis ao seu provedor de hospedagem de DNS para verificar a propriedade do domínio. 
    
> [!TIP]
> [Adicionar seu domínio e usuários para o Office 365 operado pela 21Vianet](https://support.office.com/article/1cd4839b-d051-46b8-ab9b-bc7752024e78) e [criar registros DNS para Office 365 ao gerenciar seus registros DNS](https://support.office.com/article/0669bf14-414d-4f51-8231-6b710ce7980b) são recursos úteis para referenciar conforme você adicionar seu domínio ao serviço e configurar o DNS. 
  
### <a name="step-2-add-recipients-and-configure-the-domain-type"></a>Etapa 2: Adicione destinatários e configure o tipo do domínio

Antes de configurar seu email para entrar e sair do serviço da EOP, recomendamos que adicione seus destinatários ao serviço. Existem várias maneiras de fazer isso, conforme documentado no [Gerenciar usuários de email no EOP](https://go.microsoft.com/fwlink/?LinkId=506782). Se desejar habilitar o Bloqueio de Borda Baseado em Diretório (DBEB) para impor a verificação de destinatário dentro do serviço após adicionar seus destinatários, deverá configurar o tipo do seu domínio para Autoritativo. Para obter mais informações sobre o DBEB, consulte [Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](https://go.microsoft.com/fwlink/?LinkId=506781).
  
## <a name="step-3-use-the-eac-to-set-up-mail-flow"></a>Etapa 3: Usar o EAC para configurar o fluxo de emails

Crie conectores no Centro de administração do Exchange (EAC) que permitem o fluxo de emails entre EOP e seus servidores de email local. Para obter instruções detalhadas, consulte [Create necessário conectores para configurar o fluxo de email básica por meio do EOP](https://go.microsoft.com/fwlink/?LinkId=506780).
  
 Como saber se essa tarefa funcionou? 
  
 Use the Remote Connectivity Analyzer para executar um teste que verifica o fluxo de emails entre o serviço e seu ambiente. Para obter mais informações, consulte a seção "Usar o analisador de conectividade remota para testar a entrega de email" [testar o fluxo de email com o Remote Connectivity Analyzer](https://go.microsoft.com/fwlink/?LinkId=506784).
  
## <a name="step-4-allow-inbound-port-25-smtp-access"></a>Etapa 4: Permitir acesso SMTP através da porta de entrada 25

Depois que você configurou conectores, aguarde a 72 horas para permitir a propagação de suas atualizações de registro de DNS. Depois disso, restringir o tráfego de SMTP de entrada 25 de porta em seus servidores de email ou firewall para aceitar mensagens somente dos datacenters EOP, especificamente dos endereços de IP listados em [intervalos para o Office 365 operado pela 21Vianet de endereço de IP e URLs](https://support.office.com/article/5c47c07d-f9b6-4b78-a329-bfdc1b6da7a0#__exchange_online_protection). Isso protege o seu ambiente local, limitando o escopo das mensagens de entrada, que você poderá receber. Além disso, se você tiver configurações no seu servidor de email que controlam os endereços IP permitidos para conectar-se para a retransmissão de email, atualize essas configurações também.
  
> [!TIP]
> Configure o servidor SMTP com um tempo limite de conexão de 60 segundos. Essa configuração é aceita na maioria das situações, o que fornece um pequeno atraso no caso de uma mensagem enviada com um anexo grande, por exemplo. 
  
## <a name="step-5-use-the-shell-to-ensure-that-spam-is-routed-to-each-users-junk-email-folder"></a>Etapa 5: Usar o Shell para se certificar que spam é roteado para a pasta de email de lixo eletrônico de cada usuário

Para garantir que as mensagens de spam (lixo) é roteada corretamente a pasta de lixo eletrônico de cada usuário, você deve executar algumas etapas de configuração. As etapas são fornecidas em [Certifique-se de que o spam é roteado para a pasta de lixo eletrônico de cada usuário](https://go.microsoft.com/fwlink/?LinkId=506804). Se você não quiser mover mensagens para a pasta de lixo eletrônico de cada usuário, você pode escolher outra ação por meio da edição suas políticas de filtro de conteúdo no Centro de administração do Exchange. Para obter mais informações, consulte [Configure Content Filter Policies](https://go.microsoft.com/fwlink/?LinkId=506805). 
  
## <a name="step-6-use-the-office-365-admin-center-to-point-your-mx-record-to-eop"></a>Etapa 6: Usar o Centro de administração do Office 365 para apontar o seu registro MX para a EOP

Siga as etapas de configuração de domínio do Office 365 para atualizar seu registro MX para seu domínio, de modo que seu email de entrada flui pelo EOP. Para obter mais informações, você pode consultar novamente [criar registros DNS para Office 365 ao gerenciar seus registros DNS](https://support.office.com/article/0669bf14-414d-4f51-8231-6b710ce7980b).
  
Como saber se essa tarefa funcionou?
  
 Use the Remote Connectivity Analyzer para executar um teste que verifica o seu registro MX. Para obter mais informações, consulte a seção "Usar o analisador de conectividade remota para testar seu registro MX e conector de saída" [testar o fluxo de email com o Remote Connectivity Analyzer](https://go.microsoft.com/fwlink/?LinkId=506784). 
  
Neste ponto, você já verificou se o conector de saída local da entrega de serviço está corretamente configurado bem como se o seu registro MX está apontando para a EOP. Agora, você pode optar por executar os seguintes testes adicionais para verificar se um email será entregue com êxito pelo serviço para o seu ambiente local:
  
- No Analisador de Conectividade Remota, clique na guia **Office 365** e execute o teste **Email SMTP de Entrada** localizado em **Testes de Email da Internet**.
    
- Envie uma mensagem de email de qualquer conta de email baseado na Web para um destinatário de email de sua organização cujo domínio corresponde ao domínio que você adicionou ao serviço. Confirme a entrega da mensagem para a caixa de correio no local usando o Microsoft Outlook ou outro cliente de email.
    
- Se você deseja executar um teste de email enviado, envie uma mensagem de email de um usuário de sua organização para uma conta de email baseada na Web e confirme se a mensagem foi recebida.
    
## <a name="less-common-a-hybrid-setup-with-mailboxes-on-premises-and-in-the-cloud"></a>Menos comuns: uma configuração híbrida com caixas de correio no local e na nuvem

Se você tiver o Exchange caixas de correio local e um ou mais caixas de correio na nuvem no Exchange Online, você tem uma configuração *híbrida* . Em uma configuração híbrida, recursos, como disponibilidade compartilhamento de calendário e roteamento de email funcionam juntos no seu local e ambientes em nuvem. Você pode ter uma configuração híbrida no lugar enquanto você fazer a transição de caixas de correio para o Exchange Online. Um ambiente híbrido é configurado diferente da proteção do EOP autônomo. 
  
Você pode escolher um cenário híbrido para tirar proveito de email baseada em nuvem para a maioria dos funcionários. Você pode fazer isso enquanto também hospeda algumas caixas de correio local; Por exemplo, para seu departamento jurídico. 
  
Uma configuração híbrida pode ser complexa, mas ele tem vários benefícios. Para saber mais sobre como configurar cenários híbridos com o Exchange, consulte [Exchange Configurando recursos de implantação híbrida com o Office 365 operado pela 21Vianet](https://support.office.com/article/26e7cc26-c980-4cc5-a082-c333de544b6d).
  


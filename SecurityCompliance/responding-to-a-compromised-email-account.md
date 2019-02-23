---
title: Responder a uma conta de email comprometida no Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.collection:
- o365_security_incident_response
- Strat_O365_IP
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.custom: ''
ms.assetid: ''
description: Saiba como reconhecer e responder a uma conta de email comprometida no Office 365
ms.openlocfilehash: 8d2e7f501b6e3ee73a14d4d7b3edb4c49f99d051
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30213211"
---
# <a name="responding-to-a-compromised-email-account-in-office-365"></a>Responder a uma conta de email comprometida no Office 365

**Resumo** Saiba como reconhecer e responder a uma conta de email comprometida no Office 365.

## <a name="what-is-a-compromised-email-account-in-office-365"></a>O que é uma conta de email comprometida no Office 365?
O acesso a caixas de correio, dados e outros serviços do Office 365 é controlado por meio do uso de credenciais, por exemplo, um nome de usuário e senha ou PIN. Quando alguém que não seja o usuário pretendido roubar essas credenciais, as credenciais roubadas serão consideradas comprometidas. Com eles, o invasor pode entrar como o usuário original e executar ações ilícitas. Usando as credenciais roubadas, o invasor pode acessar a caixa de correio do Office 365, pastas do SharePoint ou arquivos do usuário no OneDrive do usuário. Uma ação comumente vista é o atacante enviando emails como o usuário original para destinatários dentro e fora da organização. Quando o invasor envia dados para destinatários externos, isso é chamado de data exfiltration.

## <a name="symptoms-of-a-compromised-office-365-email-account"></a>Sintomas de uma conta de email comprometida do Office 365
Os usuários podem notar e relatar atividades incomuns em suas caixas de correio do Office 365. Estes são alguns sintomas comuns:
- Atividades suspeitas, como emails ausentes ou excluídos.
- Outros usuários podem receber emails da conta comprometida sem o email correspondente existente na pasta **itens enviados** do remetente.
- A presença de regras de caixa de entrada que não foram criadas pelo usuário ou pelo administrador desejado. Essas regras podem encaminhar emails automaticamente para endereços desconhecidos ou movê-los para as pastas **anotações**, **lixo eletrônico ou mensagens** **RSS** .
- O nome de exibição do usuário pode ser alterado na lista de endereços global.
- A caixa de correio do usuário é bloqueada para envio de email.
- As pastas itens enviados ou excluídos no Microsoft Outlook ou no Outlook na Web (anteriormente conhecido como Outlook Web App) contêm mensagens comuns de contas atacadas, como "Estou preso em Londres, enviar dinheiro".
- Alterações de perfil usuais, como o nome, o número de telefone ou o código postal foram atualizados.
- Alterações de credenciais inComuns, como várias alterações de senha são necessárias.
- O encaminhamento de emails foi adicionado recentemente.
- Uma assinatura incomum foi recentemente adicionada, como uma assinatura bancária falsa ou uma assinatura de medicamentos do medicamento.

Se um usuário relatar qualquer um dos sintomas acima, você deve realizar uma investigação adicional. O centro de conformidade do & de segurança do Office 365 e o portal do Azure oferecem ferramentas para ajudá-lo a investigar a atividade de uma conta de usuário que você suspeita que você pode estar comprometida.
- Office 365 logs de auditoria uniFicados no centro de conformidade do & de segurança-revise todas as atividades da conta suspeita filtrando os resultados para o intervalo de datas que se estenda imediatamente antes da atividade suspeita ocorrer na data atual. Não filtra as atividades durante a pesquisa.
- Use os logs de entrada do Azure AD e outros relatórios de riscos que estão disponíveis no portal do Azure AD. Examine os valores dessas colunas:
    - ReVisar endereço IP
    - locais de entrada
    - horários de entrada
    - êxito ou falha de entrada

## <a name="how-to-secure-and-restore-email-function-to-a-suspected-compromised-office-365-account-and-mailbox"></a>Como proteger e restaurar a função de email para uma conta e caixa de correio comprometida do Office 365

> [!VIDEO https://videoplayercdn.osi.office.net/hub/?csid=ux-cms-en-us-msoffice&uuid=RE2jvOb&AutoPlayVideo=false]

Mesmo depois de ter obtido o acesso à sua conta, o invasor pode ter adicionado entradas de back-door que permitem que o invasor retome o controle da conta.

Você deve executar todas as etapas a seguir para obter novamente acesso à sua conta o mais cedo para garantir que o seqüestro não retome o controle de sua conta. Estas etapas ajudam a remover entradas de back-door que o hijacker pode ter adicionado à sua conta. Após executar essas etapas, recomendamos que você execute uma verificação de vírus para garantir que o computador não seja comprometido.

### <a name="step-1-reset-the-users-password"></a>Etapa 1 redefinir a senha do usuário
> [!WARNING]
> Não envie a nova senha para o usuário pretendido por email, pois o invasor ainda tem acesso à caixa de correio neste ponto.

1. Siga a senha do Office 365 Business para procedimentos de outra pessoa em [Administradores: redefinir as senhas de negócios do office 365](https://support.office.com/article/admins-reset-office-365-business-passwords-7a5d073b-7fae-4aa5-8f96-9ecd041aba9c)

**Observações:**
- Certifique-se de que a senha é forte e que contém letras maiúsculas e minúsculas, pelo menos um número e pelo menos um caractere especial. 
- Não reutilize nenhuma de suas últimas cinco senhas. Embora a necessidade de histórico de senha permita que você reutilize uma senha mais recente, você deve selecionar algo que o invasor não possa adivinhar.
- Se sua identidade local é federada com o Office 365, você deve alterar sua senha local e, em seguida, deve notificar o administrador sobre o comprometimento.

> [!TIP]
> É altamente recomendável que você habilite a MFA (autenticação multiFator) para evitar o comprometimento, especialmente para contas com privilégios administrativos.  Você pode saber mais [aqui](https://support.office.com/en-us/article/Set-up-multi-factor-authentication-for-Office-365-users-8f0454b2-f51a-4d9c-bcde-2c48e41621c6).

### <a name="step-2-remove-suspicious-email-forwarding-addresses"></a>Etapa 2 remover endereços de encaminhamento de emails suspeitos
1. Abra o **centro de administração do Office 365 _GT_ usuários ativos**.
2. Encontre a conta de usuário em questão e expanda **configurações de email**.
3. Para **encaminhaMento de email**, clique em **Editar**.
4. Remova qualquer endereço de encaminhamento suspeito.

### <a name="step-3-disable-any-suspicious-inbox-rules"></a>Etapa 3 desabilitar qualquer regra de caixa de entrada suspeita
1. Entre na caixa de correio do usuário usando o Outlook na Web.
2. Clique no ícone de engrenagem e clique em **email**.
3. Clique em **regras de caixa de entrada e varredura** e revise as regras.
4. Desabilitar ou excluir regras suspeitas.

### <a name="step-4-unblock-the-user-from-sending-mail"></a>Etapa 4 desbloquear o usuário de enviar email
Se a caixa de correio comprometida suspeita foi usada de ilícito para enviar emails de spam, é provável que a caixa de correio tenha sido bloqueada para enviar emails.
1. Para impedir que uma caixa de correio envie emails, siga os procedimentos em [removendo um usuário, domínio ou endereço IP de uma lista de bloqueios após o envio de email de spam](https://docs.microsoft.com/Office365/SecurityCompliance/removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email ).

### <a name="step-5-optional-block-the-user-account-from-signing-in"></a>Etapa 5 opcional: bloquear a conta de usuário de entrar
> [!IMPORTANT]
> Você pode impedir que a conta comprometida suspeita de entrar até acreditar que é seguro reabilitar o acesso.

1. Vá para o centro de administração do Office 365.
2. No Centro de administração do Office 365, selecione **Usuários**.
3. Selecione o funcionário que você deseja bloquear e, em seguida, escolha **Editar** ao lado de **status de entrada** no painel do usuário
4. No painel **Status de entrada**, escolha **Entrada bloqueada** e **Salvar**. 
5. No centro de administração do Office 365, no painel de navegação inferior esquerdo, expanda **centros de administração** e selecione **Exchange**.
6. No centro de administração do Exchange, navegue até **destinatários _GT_ caixas de correio**.
7. Selecione o usuário e, na página de propriedades do usuário, em **dispositivos móveis**, clique em **desabilitar o Exchange ActivcSync** e **desabilitar o OWA para dispositivos** e responda **Sim** para ambos.
8. Em **conectividade de email**, **desabilitar** e responder **Sim**. 

### <a name="step-6-optional-remove-the-suspected-compromised-account-from-all-administrative-role-groups"></a>Etapa 6 opcional: remover a conta comprometida suspeita de todos os grupos de função administrativa
> [!NOTE]
> A associação de grupo de função administrativa pode ser restaurada após a segurança da conta.

1. Entre no centro de administração do Office 365 com uma conta de administrador global e abra **usuários ativos**.
2. Encontre a conta comprometida suspeita e verifique manualmente se há funções administrativas atribuídas à conta.
3. Abra o **centro de conformidade do & de segurança**.
4. Clique em **permissões**.
5. Revise manualmente os grupos de função para ver se a conta comprometida suspeita é um membro de qualquer um deles.  Se for: a. Clique no grupo de função e clique em **Editar grupo de função**.  b. clique em **escolher Membros** e **Editar** para remover o usuário do grupo de funções.
6. Abrir o **centro de administração do Exchange**
7. Clique em **permissões**.
8. Revise manualmente os grupos de função para ver se a conta comprometida suspeita é um membro de qualquer um deles. Se for: a. Clique no grupo de funções e clique em **Editar**.  b. Use a **** seção Members para remover o usuário do grupo de função.

### <a name="step-7-optional-additional-precautionary-steps"></a>Etapa 7 opcional: etapas de precaução adicionais
1. Certifique-se de verificar seus itens enviados. Talvez você precise informar as pessoas na sua lista de contatos de que sua conta foi comprometida. O invasor pode solicitar dinheiro, falsificação, por exemplo, que você esteve em um país diferente e que precisava de um dinheiro, ou o invasor pode enviar a eles um vírus para também seqüestrar seus computadores.
2. Qualquer outro serviço que usou essa conta do Exchange como sua conta de email alternativa pode ter sido comprometido. Primeiro, execute estas etapas para sua assinatura do Office 365 e execute estas etapas para suas outras contas.
3. Certifique-se de que suas informações de contato, como números de telefone e endereços, estão corretas.

## <a name="secure-office-365-like-a-cybersecurity-pro"></a>Proteger o Office 365 como um cybersecurity pro
Sua assinatura do Office 365 vem com um conjunto poderoso de recursos de segurança que você pode usar para proteger seus dados e seus usuários.  Use o [mapa de segurança do Office 365: as principais prioridades para os primeiros 30 dias, 90 dias e além da](https://support.office.com/article/Office-365-security-roadmap-Top-priorities-for-the-first-30-days-90-days-and-beyond-28c86a1c-e4dd-4aad-a2a6-c768a21cb352) implementação das práticas recomendaDas da Microsoft recomendadas para proteger seu locatário do Office 365.
- Tarefas a serem realizadas nos primeiros 30 dias.  Eles têm efeito imediato e têm baixo impacto para os usuários.
- Tarefas a serem realizadas em 90 dias. Esses tempos são mais demorados para planejar e implementar, mas melhorar muito a postura de segurança.
- Além de 90 dias. Esses aprimoramentos são criados nos seus primeiros 90 dias de trabalho.

## <a name="see-also"></a>ConFira também:
- [Práticas recomendadas de segurança para Office 365](https://support.office.com/article/Security-best-practices-for-Office-365-9295e396-e53d-49b9-ae9b-0b5828cdedc3)
- [Detectar e corrigir ataques de injeção a regras do Outlook e formulários personalizados no Office 365](detect-and-remediate-outlook-rules-forms-attack.md)
- [Centro de reclamações de crime da Internet](http://www.ic3.gov/preventiontips.aspx)
- [Interrupções de títulos e do Exchange – fraude de "phishing"](http://www.sec.gov/investor/pubs/phishing.htm)

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
ms.service: o365-solutions
localization_priority: Normal
search.appverid:
- MET150
ms.custom: ''
ms.assetid: ''
description: Saiba como reconhecer e responder a uma conta de email comprometido no Office 365
ms.openlocfilehash: bf3350da88804639356100fb5be2403c76cbcec6
ms.sourcegitcommit: 17dda7ece5c9e884944a92ac0f842cf1e62ec506
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/14/2018
ms.locfileid: "23977586"
---
# <a name="responding-to-a-compromised-email-account-in-office-365"></a>Responder a uma conta de email comprometida no Office 365

**Resumo** Saiba como reconhecer e responder a uma conta de email comprometido no Office 365.

## <a name="what-is-a-compromised-email-account-in-office-365"></a>O que é uma conta de Email comprometida no Office 365?
O acesso a caixas de correio, dados e outros serviços do Office 365, é controlada por meio do uso de credenciais, por exemplo um nome de usuário e senha ou PIN. Quando alguém que não seja o usuário desejado roubar essas credenciais, as credenciais furtadas são consideradas fiquem comprometidos. Com eles, o invasor pode entrar como o usuário original e executar ações ilícitas. Usando as credenciais roubadas, o invasor pode acessar caixas de correio do Office 365, pastas do SharePoint ou arquivos no OneDrive do usuário do usuário. Uma ação comumente vista é o invasor enviando emails como o usuário original para destinatários dentro e fora da organização. Quando o invasor envia dados por e-mail para destinatários externos, isso é chamado exfiltration de dados.

## <a name="symptoms-of-a-compromised-office-365-email-account"></a>Sintomas de uma conta de Email comprometido Office 365
Os usuários podem notar e relatar atividade incomum em suas caixas de correio do Office 365. Aqui estão alguns sintomas comuns:
- Atividades suspeitas, como emails ausentes ou excluídos.
- Outros usuários podem receber emails da conta comprometida sem o email correspondente existentes na pasta **Itens enviados** do remetente.
- A presença de regras de caixa de entrada que não foram criados pelo usuário pretendido ou pelo administrador. Essas regras automaticamente podem encaminhar emails para endereços desconhecidos ou transfira-os para as pastas de **Lixo eletrônico**, **anotações**ou **Assinaturas RSS** .
- Nome para exibição do usuário pode ser alterado na lista de endereços Global.
- Caixa de correio do usuário seja bloqueada para o envio de email.
- As pastas Sent ou itens excluídos no Microsoft Outlook ou no Microsoft Outlook Web App contêm mensagens de conta atacada comuns, como "Eu estou preso no London, enviar dinheiro."
- As alterações do perfil incomum, como o nome, o número de telefone ou o código postal foram atualizadas.
- Alterações de credencial incomum, como várias alterações de senha são necessárias.
- Encaminhamento de email foi adicionado recentemente.
- Uma assinatura incomum foi recentemente adicionada, como uma assinatura bancário falsa ou uma assinatura de drug receita médica.

Se um usuário relata qualquer um dos sintomas acima, você deve executar ainda mais investigação. A segurança do Office 365 & o Centro de conformidade e o Portal do Azure oferecem ferramentas para ajudar você a investigar a atividade de uma conta de usuário que você supõe que podem ser comprometidos.
- O Office 365 Unified Logs de auditoria no Centro de conformidade - & segurança revisar todas as atividades da conta suspeito filtrando os resultados para o data intervalo abrangência do imediatamente antes da ocorrência da atividade de suspeita à data atual. Não filtre as atividades durante a pesquisa.
- Use os logs do Windows Azure AD entrar e outros relatórios de risco que estão disponíveis no portal do Azure AD. Examine os valores dessas colunas:
    - Revise o endereço IP
    - locais de entrar
    - tempos de entrar
    - entrar sucesso ou falha



## <a name="how-to-secure-and-restore-email-function-to-a-suspected-compromised-office-365-account-and-mailbox"></a>Como proteger e restaurar a função de email para um suspeito comprometida caixa de correio e a conta do Office 365

> [!VIDEO https://videoplayercdn.osi.office.net/hub/?csid=ux-cms-en-us-msoffice&uuid=RE2jvOb&AutoPlayVideo=false]

Mesmo após você ter recuperou acesso à sua conta, o invasor pode adicionar entradas de porta traseira que permitem que o invasor retomar o controle da conta.

Você deve executar todas as seguintes etapas para recuperar o acesso à sua conta mais cedo melhor para certificar-se de que o Sequestrador do não retomar controlar sua conta. Estas etapas ajudarão-lo a remover quaisquer entradas de porta traseira o Sequestrador do pode ter adicionado à sua conta. Depois de executar estas etapas, é recomendável que você execute uma verificação de vírus para certificar-se de que o seu computador não estiver comprometido.

### <a name="step-1-reset-the-users-password"></a>Etapa 1 redefinir a senha do usuário
> [!WARNING]
> Não envie a nova senha para o usuário desejado por meio do e-mail conforme o invasor ainda tem o acesso à caixa de correio nesse momento.

1. Siga a senha de negócios redefinir um Office 365 para alguém procedimentos else [Admins: redefinir o Office 365 senhas de negócios](https://support.office.com/article/admins-reset-office-365-business-passwords-7a5d073b-7fae-4aa5-8f96-9ecd041aba9c)

**Observações:**
- Certifique-se de que a senha é segura e se ele contém pelo menos um caractere especial, pelo menos um número e letras maiusculas e minúsculas. 
- Não reutilize qualquer uma das suas senhas últimos cinco. Embora o requisito de histórico de senha permite que você reutilizar uma senha mais recente, você deve selecionar algo que o invasor não pode adivinhar.
- Se a sua identidade local é federada com o Office 365, você deverá alterar sua senha no local e, em seguida, você deverá notificar o administrador do comprometimento.

> [!TIP]
> É altamente recomendável que você habilite a autenticação multifator (MFA) para impedir o comprometimento, especialmente para contas com privilégios administrativos.  É possível aprender mais [aqui](https://support.office.com/en-us/article/Set-up-multi-factor-authentication-for-Office-365-users-8f0454b2-f51a-4d9c-bcde-2c48e41621c6).

### <a name="step-2-remove-suspicious-email-forwarding-addresses"></a>Etapa 2 endereços de encaminhamento de email suspeitas de remover
1. Abrir o **Centro de administração do Office 365 > usuários ativos**.
2. Para localizar a conta de usuário em questão e expanda **Configurações de email**.
3. Para **encaminhamento de Email**, clique em **Editar**.
4. Remova qualquer endereço de encaminhamento suspeitas.

### <a name="step-3-disable-any-suspicious-inbox-rules"></a>Etapa 3 desabilita as regras de caixa de entrada suspeitas
1. Inscreva-se a caixa de correio do usuário usando o Outlook Web App (OWA).
2. Clique no ícone de engrenagem e clique em **email**.
3. Clique em **regras de caixa de entrada e de varredura** e revise as regras.
4. Desabilitar ou excluir regras suspeitas.

### <a name="step-4-unblock-the-user-from-sending-mail"></a>Etapa 4 desbloquear o usuário de envio de e-mail
Se a caixa de correio comprometida suspeita foi usada ilicitamente para enviar emails de spam, é provável que a caixa de correio foi bloqueada de envio de e-mail.
1. Para desbloquear uma caixa de correio de envio de e-mail, siga os procedimentos na [remoção de um usuário, o domínio ou o endereço IP a partir de uma lista de bloqueios após o envio de mensagens de spam](https://docs.microsoft.com/Office365/SecurityCompliance/removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email ).

### <a name="step-5-optional-block-the-user-account-from-signing-in"></a>Etapa 5 opcional: Bloquear a conta de usuário de entrar no serviço
> [!IMPORTANT]
> Você pode bloquear a conta comprometida suspeita de entrar no serviço até que você acredita que é seguro reabilitar o acesso.

1. Vá para o centro de administração do Office 365.
2. No Centro de administração do Office 365, selecione **os usuários**.
3. Selecione o funcionário que você deseja bloquear e escolha **Editar** ao lado de **status de entrada** no painel de tarefas do usuário
4. No painel de **status de entrada** , escolha **entrar bloqueados** e **Salvar**. 
5. No Centro de administração do Office 365, no painel de navegação de inferior esquerdo, expanda **Centros do administrador** e selecione **Exchange**.
6. No Centro de administração do Exchange, navegue até **destinatários > caixas de correio**.
7. Selecione o usuário, na página de propriedades do usuário, em **Dispositivos móveis**, clique em **Desabilitar o Exchange ActivcSync** e **Desabilitar o OWA para dispositivos** e responder **Sim** a ambos.
8. Em **Conectividade de Email**, **desabilite** e resposta **Sim**. 

### <a name="step-6-optional-remove-the-suspected-compromised-account-from-all-administrative-role-groups"></a>Opcional da etapa 6: Remover a conta de comprometido suspeita de todos os grupos de função administrativa
> [!NOTE]
> A associação de grupo de função administrativa pode ser restaurada depois que a conta foi protegida.

1. Entrar no Centro de administração do Office 365, com uma conta de administrador global e abra **Usuários ativos**.
2. Encontre o suspeito comprometida conta e verifica manualmente para ver se há qualquer funções administrativas atribuídas à conta de.
3. Abra o **Centro de conformidade e segurança**.
4. Clique em **permissões**.
5. Revise manualmente os grupos de função para ver se o suspeito comprometida conta é um membro de qualquer um deles.  Se for: r. Clique no grupo de função e clique em **Editar grupo de função**.  b. clique em **Escolher membros** e em **Editar** para remover o usuário do grupo de funções.
6. Abrir o **Centro de administração do Exchange**
7. Clique em **permissões**.
8. Revise manualmente os grupos de função para ver se o suspeito comprometida conta é um membro de qualquer um deles. Se for: r. Clique no grupo de função e clique em **Editar**.  b. use a seção de **membros** para remover o usuário do grupo de funções.

### <a name="step-7-optional-additional-precautionary-steps"></a>Opcional da etapa 7: As etapas preventivas adicionais
1. Certifique-se de verificar itens enviados. Talvez você precise informar pessoas em sua lista de contatos que sua conta foi comprometida. O invasor pode ter solicitado-los em termos de dinheiro, falsificação, por exemplo, que foram perdidos em um país diferente e necessário dinheiro, ou o invasor pode enviar-lhes um vírus Capture também de seus computadores.
2. Qualquer outro serviço que usada essa conta do Exchange, como sua conta de email alternativos tenham sido comprometida. Primeiro, execute estas etapas para a sua assinatura do Office 365 e, em seguida, execute estas etapas para suas outras contas.
3. Certifique-se de que suas informações de contato, como números de telefone e endereços, estão corretas.

## <a name="secure-office-365-like-a-cybersecurity-pro"></a>Proteger o Office 365 como um cybersecurity pro
Sua assinatura do Office 365 é fornecido com um conjunto avançado de recursos de segurança que você pode usar para proteger seus dados e seus usuários.  Use o [mapa de segurança do Office 365: principais prioridades para os primeiros 30 dias, 90 dias e além](https://support.office.com/article/Office-365-security-roadmap-Top-priorities-for-the-first-30-days-90-days-and-beyond-28c86a1c-e4dd-4aad-a2a6-c768a21cb352) para implementar as práticas recomendadas para proteger seu locatário do Office 365 do Microsoft.
- Tarefas para realizar nos primeiros 30 dias.  Elas têm efeito imediato e são baixo impacto para seus usuários.
- Tarefas para realizar em 90 dias. Essas demoram um pouco mais para planejar e implementar mas melhorar consideravelmente sua situação de segurança.
- Além de 90 dias. Esses aperfeiçoamentos se baseiam em seu primeiro trabalho de 90 dias.

## <a name="see-also"></a>Consulte também:
- [Práticas recomendadas de segurança para Office 365](https://support.office.com/article/Security-best-practices-for-Office-365-9295e396-e53d-49b9-ae9b-0b5828cdedc3)
- [Detectar e corrigir ataques de injeção a regras do Outlook e formulários personalizados no Office 365](detect-and-remediate-outlook-rules-forms-attack.md)
- [Centro de reclamações de Crime de Internet](http://www.ic3.gov/preventiontips.aspx)
- [SEC - "Phishing" fraude](http://www.sec.gov/investor/pubs/phishing.htm)

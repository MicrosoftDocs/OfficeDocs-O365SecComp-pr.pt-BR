---
title: Simulador de ataque no Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/13/2019
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: da5845db-c578-4a41-b2cb-5a09689a551b
ms.collection:
- M365-security-compliance
description: Como administrador global do Office 365, você pode usar o simulador de ataques para executar cenários de ataque realistas em sua organização. Isso pode ajudá-lo a identificar e encontrar usuários vulneráveis antes que um ataque real atinja sua empresa.
ms.openlocfilehash: ba5658dfa9075b5779f8ca09ccad3547dbddcbb5
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216271"
---
# <a name="attack-simulator-in-office-365"></a><span data-ttu-id="24745-104">Simulador de ataque no Office 365</span><span class="sxs-lookup"><span data-stu-id="24745-104">Attack Simulator in Office 365</span></span>

<span data-ttu-id="24745-p102">**Resumo** Se você for um administrador global do Office 365 e sua organização tiver o [Office 365 Threat Intelligence](office-365-ti.md), você pode usar o Attack Simulator para executar cenários de ataque realísticos em sua organização. Isso pode ajudá-lo a identificar e encontrar usuários vulneráveis antes que um ataque real afete o resultado final. Leia este artigo para saber mais.</span><span class="sxs-lookup"><span data-stu-id="24745-p102">**Summary** If you are an Office 365 global administrator and your organization has [Office 365 Threat Intelligence](office-365-ti.md), you can use Attack Simulator to run realistic attack scenarios in your organization. This can help you identify and find vulnerable users before a real attack impacts your bottom line. Read this article to learn more.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="24745-p103">A partir de fevereiro de 2019 e saindo dos próximos meses, o Office 365 Threat Intelligence está se tornando o Office 365 Advanced Threat Protection Plan 2, com recursos adicionais de proteção contra ameaças. Para saber mais, veja [planos e preços avançados de proteção contra ameaças do office 365](https://products.office.com/exchange/advance-threat-protection) e a [Descrição do serviço de proteção avançada contra ameaças do Office 365](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span><span class="sxs-lookup"><span data-stu-id="24745-p103">Beginning in February 2019 and rolling out over the next several months, Office 365 Threat Intelligence is becoming Office 365 Advanced Threat Protection Plan 2, with additional threat protection capabilities. To learn more, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span>
  
## <a name="the-attacks"></a><span data-ttu-id="24745-110">Os ataques</span><span class="sxs-lookup"><span data-stu-id="24745-110">The Attacks</span></span>

<span data-ttu-id="24745-111">Três tipos de simulação de ataque estão disponíveis atualmente:</span><span class="sxs-lookup"><span data-stu-id="24745-111">Three kinds of attack simulations are currently available:</span></span>
  
- [<span data-ttu-id="24745-112">Nome de exibição spear-phishing Attack</span><span class="sxs-lookup"><span data-stu-id="24745-112">Display name spear-phishing attack</span></span>](attack-simulator.md#spearphish)
    
- [<span data-ttu-id="24745-113">Ataque de irrigação de senha</span><span class="sxs-lookup"><span data-stu-id="24745-113">Password-spray attack</span></span>](attack-simulator.md#passwordspray)
    
- [<span data-ttu-id="24745-114">Ataque de senha de força bruta</span><span class="sxs-lookup"><span data-stu-id="24745-114">Brute-force password attack</span></span>](attack-simulator.md#bruteforce)
    
<span data-ttu-id="24745-p104">Para que um ataque seja iniciado com êxito, use a autenticação multifator na conta que você está usando para executar ataques simulados. Além disso, você deve ser um administrador global do Office 365.</span><span class="sxs-lookup"><span data-stu-id="24745-p104">For an attack to be successfully launched, you use multi-factor authentication on the account you are using to run simulated attacks. In addition, you must be an Office 365 global administrator.</span></span>
  
> [!NOTE]
> <span data-ttu-id="24745-117">O suporte para acesso condicional estará disponível em breve.</span><span class="sxs-lookup"><span data-stu-id="24745-117">Support for Conditional Access is coming soon.</span></span> 
  
<span data-ttu-id="24745-118">Para acessar o simulador de conformidade, &amp; no centro de conformidade de segurança, escolha simulador de **ataque**de **Gerenciamento** \> de ameaças.</span><span class="sxs-lookup"><span data-stu-id="24745-118">To access Attack Simulator, in the Security &amp; Compliance Center, choose **Threat management** \> **Attack simulator**.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="24745-119">Antes de começar...</span><span class="sxs-lookup"><span data-stu-id="24745-119">Before you begin...</span></span>

<span data-ttu-id="24745-120">Verifique se você e sua organização atendem aos seguintes requisitos para o simulador de ataques:</span><span class="sxs-lookup"><span data-stu-id="24745-120">Make sure that you and your organization meet the following requirements for Attack Simulator:</span></span>
      
- <span data-ttu-id="24745-p105">O email da sua organização está hospedado no Exchange Online. (O simulador de ataque não está disponível para os servidores de email locais.)</span><span class="sxs-lookup"><span data-stu-id="24745-p105">Your organization's email is hosted in Exchange Online. (Attack Simulator is not available for on-premises email servers.)</span></span>
    
- <span data-ttu-id="24745-123">Você é um administrador global do Office 365</span><span class="sxs-lookup"><span data-stu-id="24745-123">You are an Office 365 global administrator</span></span>
    
- <span data-ttu-id="24745-124">Sua organização está usando a [autenticação multifator para usuários do Office 365](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication?view=o365-worldwide)</span><span class="sxs-lookup"><span data-stu-id="24745-124">Your organization is using [Multi-factor authentication for Office 365 users](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication?view=o365-worldwide)</span></span>
 
- <span data-ttu-id="24745-125">sua organização tem [o Office 365 Threat Intelligence](office-365-ti.md), com o simulador de ataques &amp; visível no centro de conformidade de segurança (vá para o **Threat management** \> **Attack simulator**)</span><span class="sxs-lookup"><span data-stu-id="24745-125">Your organization has [Office 365 Threat Intelligence](office-365-ti.md), with Attack Simulator visible in the Security &amp; Compliance Center (go to **Threat management** \> **Attack simulator**)</span></span><br/><span data-ttu-id="24745-126">![Gerenciamento de ameaças-simulador de ataques](media/ThreatMgmt-AttackSimulator.png)</span><span class="sxs-lookup"><span data-stu-id="24745-126">![Threat management - Attack Simulator](media/ThreatMgmt-AttackSimulator.png)</span></span>

    
## <a name="display-name-spear-phishing-attack"></a><span data-ttu-id="24745-127">Nome de exibição spear-phishing Attack</span><span class="sxs-lookup"><span data-stu-id="24745-127">Display name spear-phishing attack</span></span>

<span data-ttu-id="24745-p106">Phishing é um termo genérico para um amplo conjunto de ataques de classe como um ataque de estilo de engenharia social. Esse ataque está voltado para o spear phishing, um ataque mais direcionado para um grupo específico de pessoas ou uma organização. Normalmente, um ataque personalizado com algum reconhecimento executado e usando um nome de exibição que irá gerar confiança no destinatário, como uma mensagem de email que parece ser proveniente de um executivo dentro da sua organização.</span><span class="sxs-lookup"><span data-stu-id="24745-p106">Phishing is a generic term for a broad suite of attacks classed as a social engineering style attack. This attack is focused on spear phishing, a more targeted attack that is aimed at a specific group of individuals or an organization. Typically, a customized attack with some reconnaissance performed and using a display name that will generate trust in the recipient, such as an email message that looks like it came from an executive within your organization.</span></span>
  
<span data-ttu-id="24745-p107">Esse ataque se concentra em permitir que você manipule quem a mensagem parece ter originado alterando o nome de exibição e o endereço de origem. Quando os ataques de spear-phishing forem bem-sucedidos, cybercriminals obter acesso às credenciais dos usuários.</span><span class="sxs-lookup"><span data-stu-id="24745-p107">This attack focuses on letting you manipulate who the message appears to have originated from by changing the display name and source address. When spear-phishing attacks are successful, cybercriminals gain access to users' credentials.</span></span>
  
### <a name="to-simulate-a-spear-phishing-attack"></a><span data-ttu-id="24745-133">Para simular um ataque de spear-phishing</span><span class="sxs-lookup"><span data-stu-id="24745-133">To simulate a spear-phishing attack</span></span>

![Redigir corpo de email](media/9bd65af4-1f9d-45c1-8c06-796d7ccfd425.jpg)
  
<span data-ttu-id="24745-135">Você pode criar o editor de HTML avançado diretamente no próprio campo de **corpo de email** ou trabalhar com o código-fonte HTML.</span><span class="sxs-lookup"><span data-stu-id="24745-135">You can craft the rich HTML editor directly in the **Email body** field itself or work with HTML source.</span></span>
  
1. <span data-ttu-id="24745-136">No [centro de &amp; conformidade de segurança](https://protection.office.com), escolha simulador de **ataque**de **Gerenciamento** \> de ameaças.</span><span class="sxs-lookup"><span data-stu-id="24745-136">In the [Security &amp; Compliance Center](https://protection.office.com), choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="24745-137">Especifique um nome de campanha significativo para o ataque ou selecione um modelo.</span><span class="sxs-lookup"><span data-stu-id="24745-137">Specify a meaningful campaign name for the attack or select a template.</span></span> <br/>![Página de início de phishing](media/5e93b3cc-5981-462f-8b45-bdf85d97f1b8.jpg)
  
3. <span data-ttu-id="24745-p108">Especifique os destinatários de destino. Podem ser indivíduos ou grupos em sua organização. Cada destinatário de destino deve ter uma caixa de correio do Exchange Online para que o ataque seja bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="24745-p108">Specify the target recipients. This can be individuals or groups in your organization. Each targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span> <br/>![Seleção de destinatário](media/faf8c2e0-6175-4cd7-8265-0c8e727f4d0f.jpg)
  
4. <span data-ttu-id="24745-143">Configure os detalhes de email de phishing.</span><span class="sxs-lookup"><span data-stu-id="24745-143">Configure the Phishing email details.</span></span> <br/>![Configurar detalhes de email](media/f043608f-f8ce-4aae-be28-86e8ecc524a9.jpg)<br/><span data-ttu-id="24745-p109">A formatação HTML pode ser complexa ou básica quanto às necessidades de sua campanha. Como o formato de email é HTML, você pode inserir imagens e texto para aprimorar o believability. Você tem controle sobre qual será a aparência da mensagem recebida no cliente de recebimento de email.</span><span class="sxs-lookup"><span data-stu-id="24745-p109">The HTML formatting can be as complex or basic as your campaign needs. As the email format is HTML, you can insert images and text to enhance believability. You have control on what the received message will look like in the receiving email client.</span></span>
    
5. <span data-ttu-id="24745-p110">Especifique o texto para o campo **de (nome)** . Este é o campo que mostra o **nome de exibição** no cliente de recebimento de email.</span><span class="sxs-lookup"><span data-stu-id="24745-p110">Specify text for the **From (Name)** field. This is the field that shows in the **Display Name** in the receiving email client.</span></span> 
    
6. <span data-ttu-id="24745-p111">Especifique o texto ou o campo **de** . Este é o campo que aparece como o endereço de email do remetente no cliente de recebimento de email.</span><span class="sxs-lookup"><span data-stu-id="24745-p111">Specify text or the **From** field. This is the field that shows as the email address of the sender in the receiving email client. </span></span><br/><span data-ttu-id="24745-p112">Você pode inserir um namespace de email existente dentro da sua organização (isso fará com que o endereço de email seja realmente resolvido no cliente de recebimento, facilitando um modelo de confiança muito alto) ou você pode inserir um endereço de email externo. O endereço de email que você especificar não precisa realmente existir, mas ele precisa seguir o formato de um endereço SMTP válido, como User @ nome_do_domínio. Extension.</span><span class="sxs-lookup"><span data-stu-id="24745-p112">You can enter an existing email namespace within your organization (doing this will make the email address actually resolve in the receiving client, facilitating a very high trust model), or you can enter an external email address. The email address that you specify does not have to actually exist, but it does need to following the format of a valid SMTP address, such as user@domainname.extension.</span></span> 
  
7. <span data-ttu-id="24745-p113">Usando o seletor suspenso, selecione uma URL de servidor de logon de phishing que reflita o tipo de conteúdo que você terá dentro de seu ataque. Várias URLs com temas são fornecidas para você escolher, como entrega de documentos, técnica, folha de pagamento, etc. Isso é efetivamente a URL para a qual os usuários direcionados são solicitados a clicar.</span><span class="sxs-lookup"><span data-stu-id="24745-p113">Using the drop-down selector, select a Phishing Login server URL that reflects the type of content you will have within your attack. Several themed URLs are provided for you to choose from, such as document delivery, technical, payroll etc. This is effectively the URL that targeted users are asked to click.</span></span>
    
8. <span data-ttu-id="24745-p114">Especifique uma URL da página de aterrissagem personalizada. O uso dessa forma redirecionará os usuários para uma URL que você especificar no final de um ataque bem-sucedido. Se você tiver treinamento de conscientização interna, por exemplo, você pode especificar isso aqui.</span><span class="sxs-lookup"><span data-stu-id="24745-p114">Specify a custom landing page URL. Using this will redirect users to a URL you specify at the end of a successful attack. If you have internal awareness training, for example, you can specify that here.</span></span>
    
9. <span data-ttu-id="24745-p115">Especifique o texto do campo **assunto** . Este é o campo que aparece como o **nome da entidade** no cliente de recebimento de email.</span><span class="sxs-lookup"><span data-stu-id="24745-p115">Specify text for the **Subject** field. This is the field that shows as the **Subject Name** in the receiving email client.</span></span> 
    
10. <span data-ttu-id="24745-161">Redija o **corpo do email** que o destino receberá.</span><span class="sxs-lookup"><span data-stu-id="24745-161">Compose the **Email body** that the target will receive.</span></span> <br/><span data-ttu-id="24745-162">`${username}`Insere o nome do destino no corpo do email.</span><span class="sxs-lookup"><span data-stu-id="24745-162">`${username}` inserts the targets name into the Email body.</span></span> <br/><span data-ttu-id="24745-163">`${loginserverurl}`Insere a URL que os usuários de destino devem clicar</span><span class="sxs-lookup"><span data-stu-id="24745-163">`${loginserverurl}` inserts the URL we want target users to click</span></span> 
    
11. <span data-ttu-id="24745-p116">Escolha **Avançar e** **concluir** para iniciar o ataque. A mensagem de email de spear phishing é entregue às caixas de correio dos destinatários de destino.</span><span class="sxs-lookup"><span data-stu-id="24745-p116">Choose **Next,** then **Finish** to launch the attack. The spear phishing email message is delivered to your target recipients' mailboxes.</span></span> 
    
## <a name="password-spray-attack"></a><span data-ttu-id="24745-166">Ataque de irrigação de senha</span><span class="sxs-lookup"><span data-stu-id="24745-166">Password-spray attack</span></span>

<span data-ttu-id="24745-p117">Um ataque de irrigação de senha em uma organização é geralmente usado após um ator incorreto ter adquirido com êxito uma lista de usuários válidos do locatário. O ator ruim sabe sobre senhas comuns que as pessoas utilizam. Esse é um ataque amplamente usado, pois é um ataque barato que é executado e é mais difícil de detectar abordagens de força bruta.</span><span class="sxs-lookup"><span data-stu-id="24745-p117">A password spray attack against an organization is typically used after a bad actor has successfully acquired a list of valid users from the tenant. The bad actor knows about common passwords that people use. This is a widely used attack, as it is a cheap attack to run, and harder to detect than brute force approaches.</span></span>
  
<span data-ttu-id="24745-170">Esse ataque se concentra em permitir que você especifique uma senha comum para uma grande base de destino de usuários.</span><span class="sxs-lookup"><span data-stu-id="24745-170">This attack focuses on letting you specify a common password against a large target base of users.</span></span>
  
### <a name="to-simulate-a-password-spray-attack"></a><span data-ttu-id="24745-171">Para simular um ataque de irrigação de senha</span><span class="sxs-lookup"><span data-stu-id="24745-171">To simulate a password-spray attack</span></span>

1. <span data-ttu-id="24745-172">No [centro de &amp; conformidade de segurança](https://protection.office.com), escolha simulador de **ataque**de **Gerenciamento** \> de ameaças.</span><span class="sxs-lookup"><span data-stu-id="24745-172">In the [Security &amp; Compliance Center](https://protection.office.com), choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="24745-173">Especifique um nome de campanha significativo para o ataque.</span><span class="sxs-lookup"><span data-stu-id="24745-173">Specify a meaningful campaign name for the attack.</span></span>
    
3. <span data-ttu-id="24745-p118">Especifique os destinatários de destino. Podem ser indivíduos ou grupos em sua organização. Um destinatário direcionado deve ter uma caixa de correio do Exchange Online para que o ataque seja bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="24745-p118">Specify the target recipients. This can be individuals or groups in your organization. A targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span>
    
4. <span data-ttu-id="24745-p119">Especifique uma senha a ser usada para o ataque. Por exemplo, uma senha comum e relevante que você pode tentar `Fall2017`é. Outro pode ser `Spring2018`ou `Password1`.</span><span class="sxs-lookup"><span data-stu-id="24745-p119">Specify a password to use for the attack. For example, one common, relevant password you could try is `Fall2017`. Another might be `Spring2018`, or `Password1`.</span></span>
    
5. <span data-ttu-id="24745-180">Escolha **concluir** para iniciar o ataque.</span><span class="sxs-lookup"><span data-stu-id="24745-180">Choose **Finish** to launch the attack.</span></span> 
    
## <a name="brute-force-password-attack"></a><span data-ttu-id="24745-181">Ataque de senha de força bruta</span><span class="sxs-lookup"><span data-stu-id="24745-181">Brute-force password attack</span></span>

<span data-ttu-id="24745-p120">Um ataque de senha de força bruta em relação a uma organização é geralmente usado após um ator incorreto ter adquirido com êxito uma lista de usuários principais do locatário. Esse ataque se concentra em tentar um conjunto de senhas em uma única conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="24745-p120">A brute-force password attack against an organization is typically used after a bad actor has successfully acquired a list of key users from the tenant. This attack focuses on trying a set of passwords on a single user's account.</span></span>
  
### <a name="to-simulate-a-brute-force-password-attack"></a><span data-ttu-id="24745-184">Para simular um ataque de senha de força bruta</span><span class="sxs-lookup"><span data-stu-id="24745-184">To simulate a brute-force password attack</span></span>

1. <span data-ttu-id="24745-185">No [centro de &amp; conformidade de segurança](https://protection.office.com), escolha simulador de **ataque**de **Gerenciamento** \> de ameaças.</span><span class="sxs-lookup"><span data-stu-id="24745-185">In the [Security &amp; Compliance Center](https://protection.office.com), choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="24745-186">Especifique um nome de campanha significativo para o ataque.</span><span class="sxs-lookup"><span data-stu-id="24745-186">Specify a meaningful campaign name for the attack.</span></span>
    
3. <span data-ttu-id="24745-p121">Especifique o destinatário de destino. Um destinatário direcionado deve ter uma caixa de correio do Exchange Online para que o ataque seja bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="24745-p121">Specify the target recipient. A targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span>
    
4. <span data-ttu-id="24745-p122">Especifique um conjunto de senhas a ser usado para o ataque. Para fazer isso, você pode usar um arquivo de texto (. txt) para sua lista de senhas. O arquivo de texto não pode exceder 10 MB em tamanho de arquivo. Use uma senha por linha e certifique-se de incluir um retorno de disco rígido após a última senha em sua lista.</span><span class="sxs-lookup"><span data-stu-id="24745-p122">Specify a set of passwords to use for the attack. To do this, you can use a text (.txt) file for your list of passwords. The text file cannot exceed 10 MB in file size. Use one password per line, and make sure to include a hard return after the last password in your list.</span></span>
    
5. <span data-ttu-id="24745-193">Escolha **concluir** para iniciar o ataque.</span><span class="sxs-lookup"><span data-stu-id="24745-193">Choose **Finish** to launch the attack.</span></span> 
    
## <a name="new-features-in-attack-simulator"></a><span data-ttu-id="24745-194">Novos recursos no simulador de ataques</span><span class="sxs-lookup"><span data-stu-id="24745-194">New features in Attack Simulator</span></span>

<span data-ttu-id="24745-p123">Novos recursos estão sendo adicionados ao simulador de ataques. Eles incluem:</span><span class="sxs-lookup"><span data-stu-id="24745-p123">New features are being added to Attack Simulator. These include:</span></span>
- <span data-ttu-id="24745-p124">**Recursos avançados de relatórios**. Você poderá ver dados como o tempo mais rápido (ou mais lento) para abrir uma mensagem de email de simulação de ataque, o tempo mais rápido (ou mais lento) para clicar em um link na mensagem e muito mais.</span><span class="sxs-lookup"><span data-stu-id="24745-p124">**Advanced reporting capabilities**. You'll be able to see data such as the fastest (or slowest) time to open an attack simulation email message, the fastest (or slowest) time to click a link in the message, and more.</span></span>
- <span data-ttu-id="24745-p125">**Editor de modelos de email**. Você pode criar um modelo de email reutilizável e personalizado que pode ser usado para simulações de ataque futuras.</span><span class="sxs-lookup"><span data-stu-id="24745-p125">**Email template editor**. You can create a custom, reusable email template that you can use for future attack simulations.</span></span>

<span data-ttu-id="24745-201">Visite o [mapa do Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap) para ver o que está em desenvolvimento, o que está saindo e o que já foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="24745-201">Visit the [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap) to see what's in development, what's rolling out, and what's already launched.</span></span>




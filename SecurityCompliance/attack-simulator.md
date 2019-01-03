---
title: Simulador de ataque no Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/02/2019
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: da5845db-c578-4a41-b2cb-5a09689a551b
description: Como administrador global do Office 365, você pode usar o simulador de ataque para executar cenários de ataque realístico em sua organização. Isso pode ajudá-lo a identificar e encontrar vulnerável usuários antes de um ataque real atinge seu negócio.
ms.openlocfilehash: 1a1d22b0b36ce8b6a2086296be8f8b5d47d79280
ms.sourcegitcommit: d512c1df01377e305e8d5c0170c822cf78f09565
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/02/2019
ms.locfileid: "27471994"
---
# <a name="attack-simulator-in-office-365"></a><span data-ttu-id="35873-104">Simulador de ataque no Office 365</span><span class="sxs-lookup"><span data-stu-id="35873-104">Attack Simulator in Office 365</span></span>

<span data-ttu-id="35873-p102">**Resumo** Se você for um administrador global do Office 365 e sua organização tem [Inteligência de ameaça do Office 365](office-365-ti.md), você pode usar o simulador de ataque para executar cenários de ataque realístico em sua organização. Isso pode ajudá-lo a identificar e encontrar vulnerável usuários antes de um ataque real afeta sua linha inferior. Leia este artigo para saber mais.</span><span class="sxs-lookup"><span data-stu-id="35873-p102">**Summary** If you are an Office 365 global administrator and your organization has [Office 365 Threat Intelligence](office-365-ti.md), you can use Attack Simulator to run realistic attack scenarios in your organization. This can help you identify and find vulnerable users before a real attack impacts your bottom line. Read this article to learn more.</span></span>
  
## <a name="the-attacks"></a><span data-ttu-id="35873-108">Os ataques</span><span class="sxs-lookup"><span data-stu-id="35873-108">The Attacks</span></span>

<span data-ttu-id="35873-109">Três tipos de simulações de ataque estão atualmente disponíveis:</span><span class="sxs-lookup"><span data-stu-id="35873-109">Three kinds of attack simulations are currently available:</span></span>
  
- [<span data-ttu-id="35873-110">Ataque de phishing lança de nome de exibição</span><span class="sxs-lookup"><span data-stu-id="35873-110">Display name spear-phishing attack</span></span>](attack-simulator.md#spearphish)
    
- [<span data-ttu-id="35873-111">Ataque de borrifada de senha</span><span class="sxs-lookup"><span data-stu-id="35873-111">Password-spray attack</span></span>](attack-simulator.md#passwordspray)
    
- [<span data-ttu-id="35873-112">Ataque de senha de força bruta</span><span class="sxs-lookup"><span data-stu-id="35873-112">Brute-force password attack</span></span>](attack-simulator.md#bruteforce)
    
<span data-ttu-id="35873-p103">Para um ataque ser iniciados com êxito, você pode usar a autenticação multifator a conta que você está usando para executar ataques simulados. Além disso, você deve ser um administrador global do Office 365.</span><span class="sxs-lookup"><span data-stu-id="35873-p103">For an attack to be successfully launched, you use multi-factor authentication on the account you are using to run simulated attacks. In addition, you must be an Office 365 global administrator.</span></span>
  
> [!NOTE]
> <span data-ttu-id="35873-115">Suporte para acesso condicional estarão disponíveis em breve.</span><span class="sxs-lookup"><span data-stu-id="35873-115">Support for Conditional Access is coming soon.</span></span> 
  
<span data-ttu-id="35873-116">Para acessar o simulador de ataque, na segurança &amp; Centro de conformidade, escolha **gerenciamento de ameaça** \> **simulador de ataque**.</span><span class="sxs-lookup"><span data-stu-id="35873-116">To access Attack Simulator, in the Security &amp; Compliance Center, choose **Threat management** \> **Attack simulator**.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="35873-117">Antes de começar...</span><span class="sxs-lookup"><span data-stu-id="35873-117">Before you begin...</span></span>

<span data-ttu-id="35873-118">Certifique-se de que você e sua organização atendem aos seguintes requisitos para simulador de ataque:</span><span class="sxs-lookup"><span data-stu-id="35873-118">Make sure that you and your organization meet the following requirements for Attack Simulator:</span></span>
      
- <span data-ttu-id="35873-p104">Email da sua organização está hospedada no Exchange Online. (Simulador de ataque não está disponível para servidores de email local.)</span><span class="sxs-lookup"><span data-stu-id="35873-p104">Your organization's email is hosted in Exchange Online. (Attack Simulator is not available for on-premises email servers.)</span></span>
    
- <span data-ttu-id="35873-121">Você é um administrador global do Office 365</span><span class="sxs-lookup"><span data-stu-id="35873-121">You are an Office 365 global administrator</span></span>
    
- <span data-ttu-id="35873-122">Sua organização estiver usando [a autenticação multifator para usuários do Office 365](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication?view=o365-worldwide)</span><span class="sxs-lookup"><span data-stu-id="35873-122">Your organization is using [Multi-factor authentication for Office 365 users](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication?view=o365-worldwide)</span></span>
 
- <span data-ttu-id="35873-123">Sua organização tem [Inteligência de ameaça do Office 365](office-365-ti.md), com simulador de ataque visível na segurança &amp; Centro de conformidade (vá para **gerenciamento de ameaça** \> **simulador de ataque**)</span><span class="sxs-lookup"><span data-stu-id="35873-123">Your organization has [Office 365 Threat Intelligence](office-365-ti.md), with Attack Simulator visible in the Security &amp; Compliance Center (go to **Threat management** \> **Attack simulator**)</span></span><br/><span data-ttu-id="35873-124">![Gerenciamento de ameaça - simulador de ataque](media/ThreatMgmt-AttackSimulator.png)</span><span class="sxs-lookup"><span data-stu-id="35873-124">![Threat management - Attack Simulator](media/ThreatMgmt-AttackSimulator.png)</span></span>

    
## <a name="display-name-spear-phishing-attack"></a><span data-ttu-id="35873-125">Ataque de phishing lança de nome de exibição</span><span class="sxs-lookup"><span data-stu-id="35873-125">Display name spear-phishing attack</span></span>

<span data-ttu-id="35873-p105">O phishing é um termo genérico para um conjunto amplo de ataques classificado como um ataque de estilo de engenharia social. Esse ataque se concentra em lança phishing, um ataque mais direcionado que é destinado a um grupo específico de indivíduos ou uma organização. Normalmente, um ataque personalizado com alguns reconhecimento realizada e usando um nome de exibição que irá gerar a confiança no destinatário, como uma mensagem de email que parece que ele tenha vindo de executivo dentro da sua organização.</span><span class="sxs-lookup"><span data-stu-id="35873-p105">Phishing is a generic term for a broad suite of attacks classed as a social engineering style attack. This attack is focused on spear phishing, a more targeted attack that is aimed at a specific group of individuals or an organization. Typically, a customized attack with some reconnaissance performed and using a display name that will generate trust in the recipient, such as an email message that looks like it came from an executive within your organization.</span></span>
  
<span data-ttu-id="35873-p106">Esse ataque enfoca permitindo que você manipule a quem a mensagem é exibida para originada por alterando o endereço de origem e de nome de exibição. Quando os ataques de phishing lança foram bem sucedidos, cibercriminosos acessem as credenciais dos usuários.</span><span class="sxs-lookup"><span data-stu-id="35873-p106">This attack focuses on letting you manipulate who the message appears to have originated from by changing the display name and source address. When spear-phishing attacks are successful, cybercriminals gain access to users' credentials.</span></span>
  
### <a name="to-simulate-a-spear-phishing-attack"></a><span data-ttu-id="35873-131">Para simular um ataque de phishing de lança</span><span class="sxs-lookup"><span data-stu-id="35873-131">To simulate a spear-phishing attack</span></span>

![Corpo do Email de redação](media/9bd65af4-1f9d-45c1-8c06-796d7ccfd425.jpg)
  
<span data-ttu-id="35873-133">Você pode desenvolver o editor de HTML avançado diretamente no **corpo do Email** de campo próprio ou trabalhar com código fonte HTML.</span><span class="sxs-lookup"><span data-stu-id="35873-133">You can craft the rich HTML editor directly in the **Email body** field itself or work with HTML source.</span></span>
  
1. <span data-ttu-id="35873-134">No [segurança &amp; Centro de conformidade](https://security.microsoft.com), escolha **gerenciamento de ameaça** \> **simulador de ataque**.</span><span class="sxs-lookup"><span data-stu-id="35873-134">In the [Security &amp; Compliance Center](https://security.microsoft.com), choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="35873-135">Especifique um nome de campanha significativo para o ataque ou selecione um modelo.</span><span class="sxs-lookup"><span data-stu-id="35873-135">Specify a meaningful campaign name for the attack or select a template.</span></span> <br/>![Página inicial de phishing](media/5e93b3cc-5981-462f-8b45-bdf85d97f1b8.jpg)
  
3. <span data-ttu-id="35873-p107">Especifica os destinatários de destino. Isso pode ser indivíduos ou grupos em sua organização. Cada destinatário direcionado deve ter um Exchange Online da caixa de correio para o ataque seja bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="35873-p107">Specify the target recipients. This can be individuals or groups in your organization. Each targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span> <br/>![Seleção de destinatário](media/faf8c2e0-6175-4cd7-8265-0c8e727f4d0f.jpg)
  
4. <span data-ttu-id="35873-141">Configure os detalhes de email de Phishing.</span><span class="sxs-lookup"><span data-stu-id="35873-141">Configure the Phishing email details.</span></span> <br/>![Configurar detalhes de email](media/f043608f-f8ce-4aae-be28-86e8ecc524a9.jpg)<br/><span data-ttu-id="35873-p108">A formatação HTML pode ser tão complexa ou básica conforme as necessidades de sua campanha. Como o formato de email HTML, você pode inserir imagens e texto para aperfeiçoar credibilidade. Você tem controle na aparência a mensagem recebida no cliente de email do receptor.</span><span class="sxs-lookup"><span data-stu-id="35873-p108">The HTML formatting can be as complex or basic as your campaign needs. As the email format is HTML, you can insert images and text to enhance believability. You have control on what the received message will look like in the receiving email client.</span></span>
    
5. <span data-ttu-id="35873-p109">Especifica o texto do campo **de (nome)** . Esse é o campo que mostra o **Nome para exibição** do cliente de recebimento de email.</span><span class="sxs-lookup"><span data-stu-id="35873-p109">Specify text for the **From (Name)** field. This is the field that shows in the **Display Name** in the receiving email client.</span></span> 
    
6. <span data-ttu-id="35873-p110">Especifique o texto ou campo **de** . Esse é o campo que mostra como o endereço de email do remetente no cliente de email do receptor.</span><span class="sxs-lookup"><span data-stu-id="35873-p110">Specify text or the **From** field. This is the field that shows as the email address of the sender in the receiving email client. </span></span><br/><span data-ttu-id="35873-p111">Você pode inserir um namespace de email existente dentro da sua organização (Isso fará o endereço de email realmente resolver no cliente de recebimento, facilitando a um modelo de confiança muito alta), ou você pode inserir um endereço de email externo. O endereço de email que você especificar não tem que existe realmente, mas ela precisa seguir o formato de um endereço SMTP válido, como user@domainname.extension.</span><span class="sxs-lookup"><span data-stu-id="35873-p111">You can enter an existing email namespace within your organization (doing this will make the email address actually resolve in the receiving client, facilitating a very high trust model), or you can enter an external email address. The email address that you specify does not have to actually exist, but it does need to following the format of a valid SMTP address, such as user@domainname.extension.</span></span> 
  
7. <span data-ttu-id="35873-p112">Usando o seletor de lista suspensa, selecione uma URL de servidor de logon de Phishing que reflete o tipo de conteúdo, que você terá dentro de seu ataque. Várias URLs com temas são fornecidos para que você escolher, como o pagamento do documento entrega, técnica, etc. Isso é efetivamente a URL que os usuários de destino serão solicitados a clicar em.</span><span class="sxs-lookup"><span data-stu-id="35873-p112">Using the drop-down selector, select a Phishing Login server URL that reflects the type of content you will have within your attack. Several themed URLs are provided for you to choose from, such as document delivery, technical, payroll etc. This is effectively the URL that targeted users are asked to click.</span></span>
    
8. <span data-ttu-id="35873-p113">Especifique uma URL de página de aterrissagem personalizado. Usando essa redirecionar os usuários para uma URL que você especificar no final de um ataque bem-sucedido. Se você tiver o treinamento interno de divulgação, por exemplo, você pode especificar que aqui.</span><span class="sxs-lookup"><span data-stu-id="35873-p113">Specify a custom landing page URL. Using this will redirect users to a URL you specify at the end of a successful attack. If you have internal awareness training, for example, you can specify that here.</span></span>
    
9. <span data-ttu-id="35873-p114">Especifica o texto do campo **assunto** . Esse é o campo que mostra como o **Nome da entidade** no cliente de email do receptor.</span><span class="sxs-lookup"><span data-stu-id="35873-p114">Specify text for the **Subject** field. This is the field that shows as the **Subject Name** in the receiving email client.</span></span> 
    
10. <span data-ttu-id="35873-159">Componha o **corpo do Email** que receberá o destino.</span><span class="sxs-lookup"><span data-stu-id="35873-159">Compose the **Email body** that the target will receive.</span></span> <br/><span data-ttu-id="35873-160">`${username}`Insere o nome de destinos o corpo do Email.</span><span class="sxs-lookup"><span data-stu-id="35873-160">`${username}` inserts the targets name into the Email body.</span></span> <br/><span data-ttu-id="35873-161">`${loginserverurl}`Insere a URL que queremos que os usuários de destino, clique em</span><span class="sxs-lookup"><span data-stu-id="35873-161">`${loginserverurl}` inserts the URL we want target users to click</span></span> 
    
11. <span data-ttu-id="35873-p115">Escolha **Avançar,** em seguida, **término** para iniciar o ataque. A mensagem de email de phishing lança é entregue às caixas de correio dos seus destinatários de destino.</span><span class="sxs-lookup"><span data-stu-id="35873-p115">Choose **Next,** then **Finish** to launch the attack. The spear phishing email message is delivered to your target recipients' mailboxes.</span></span> 
    
## <a name="password-spray-attack"></a><span data-ttu-id="35873-164">Ataque de borrifada de senha</span><span class="sxs-lookup"><span data-stu-id="35873-164">Password-spray attack</span></span>

<span data-ttu-id="35873-p116">Um ataque de borrifada senha contra uma organização geralmente é utilizado após um ator bad adquiriu com êxito uma lista de usuários válidos de Inquilino. Bad ator conhece as senhas comuns que as pessoas utilizam o uso. Esse é um ataque amplamente usado, conforme ele é um ataque barato mais difícil detectar que força bruta abordagens e execução.</span><span class="sxs-lookup"><span data-stu-id="35873-p116">A password spray attack against an organization is typically used after a bad actor has successfully acquired a list of valid users from the tenant. The bad actor knows about common passwords that people use. This is a widely used attack, as it is a cheap attack to run, and harder to detect than brute force approaches.</span></span>
  
<span data-ttu-id="35873-168">Esse ataque enfoca permitindo que você especifique uma senha comum em relação a uma base de destino grande de usuários.</span><span class="sxs-lookup"><span data-stu-id="35873-168">This attack focuses on letting you specify a common password against a large target base of users.</span></span>
  
### <a name="to-simulate-a-password-spray-attack"></a><span data-ttu-id="35873-169">Para simular um ataque borrifada de senha</span><span class="sxs-lookup"><span data-stu-id="35873-169">To simulate a password-spray attack</span></span>

1. <span data-ttu-id="35873-170">No [segurança &amp; Centro de conformidade](https://security.microsoft.com), escolha **gerenciamento de ameaça** \> **simulador de ataque**.</span><span class="sxs-lookup"><span data-stu-id="35873-170">In the [Security &amp; Compliance Center](https://security.microsoft.com), choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="35873-171">Especifique um nome de campanha significativo para o ataque.</span><span class="sxs-lookup"><span data-stu-id="35873-171">Specify a meaningful campaign name for the attack.</span></span>
    
3. <span data-ttu-id="35873-p117">Especifica os destinatários de destino. Isso pode ser indivíduos ou grupos em sua organização. Um destinatário de destino deve ter um Exchange Online da caixa de correio para o ataque seja bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="35873-p117">Specify the target recipients. This can be individuals or groups in your organization. A targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span>
    
4. <span data-ttu-id="35873-p118">Especifique uma senha a serem usados para o ataque. Por exemplo, uma senha comum e relevante, você pode tentar é `Fall2017`. Outro método pode ser `Spring2018`, ou `Password1`.</span><span class="sxs-lookup"><span data-stu-id="35873-p118">Specify a password to use for the attack. For example, one common, relevant password you could try is `Fall2017`. Another might be `Spring2018`, or `Password1`.</span></span>
    
5. <span data-ttu-id="35873-178">Escolha **Concluir** para iniciar o ataque.</span><span class="sxs-lookup"><span data-stu-id="35873-178">Choose **Finish** to launch the attack.</span></span> 
    
## <a name="brute-force-password-attack"></a><span data-ttu-id="35873-179">Ataque de senha de força bruta</span><span class="sxs-lookup"><span data-stu-id="35873-179">Brute-force password attack</span></span>

<span data-ttu-id="35873-p119">Um ataque de senha de força bruta contra uma organização geralmente é utilizado após um ator bad adquiriu com êxito uma lista dos principais usuários de Inquilino. Esse ataque enfoca a tentativa de um conjunto de senhas em uma única conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="35873-p119">A brute-force password attack against an organization is typically used after a bad actor has successfully acquired a list of key users from the tenant. This attack focuses on trying a set of passwords on a single user's account.</span></span>
  
### <a name="to-simulate-a-brute-force-password-attack"></a><span data-ttu-id="35873-182">Para simular um ataque de senha de força bruta</span><span class="sxs-lookup"><span data-stu-id="35873-182">To simulate a brute-force password attack</span></span>

1. <span data-ttu-id="35873-183">No [segurança &amp; Centro de conformidade](https://security.microsoft.com), escolha **gerenciamento de ameaça** \> **simulador de ataque**.</span><span class="sxs-lookup"><span data-stu-id="35873-183">In the [Security &amp; Compliance Center](https://security.microsoft.com), choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="35873-184">Especifique um nome de campanha significativo para o ataque.</span><span class="sxs-lookup"><span data-stu-id="35873-184">Specify a meaningful campaign name for the attack.</span></span>
    
3. <span data-ttu-id="35873-p120">Especifique o destinatário de destino. Um destinatário de destino deve ter um Exchange Online da caixa de correio para o ataque seja bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="35873-p120">Specify the target recipient. A targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span>
    
4. <span data-ttu-id="35873-p121">Especifique um conjunto de senhas a ser usado para o ataque. Para fazer isso, você pode usar um arquivo de texto (. txt) para sua lista de senhas. O arquivo de texto não pode exceder 10 MB em tamanho de arquivo. Use uma senha por linha e certifique-se de incluir um retorno de carro após a última senha na sua lista.</span><span class="sxs-lookup"><span data-stu-id="35873-p121">Specify a set of passwords to use for the attack. To do this, you can use a text (.txt) file for your list of passwords. The text file cannot exceed 10 MB in file size. Use one password per line, and make sure to include a hard return after the last password in your list.</span></span>
    
5. <span data-ttu-id="35873-191">Escolha **Concluir** para iniciar o ataque.</span><span class="sxs-lookup"><span data-stu-id="35873-191">Choose **Finish** to launch the attack.</span></span> 
    
## <a name="new-features-in-attack-simulator"></a><span data-ttu-id="35873-192">Novos recursos no simulador de ataque</span><span class="sxs-lookup"><span data-stu-id="35873-192">New features in Attack Simulator</span></span>

<span data-ttu-id="35873-p122">Novos recursos são adicionados ao simulador de ataque. Elas incluem:</span><span class="sxs-lookup"><span data-stu-id="35873-p122">New features are being added to Attack Simulator. These include:</span></span>
- <span data-ttu-id="35873-p123">**Recursos de relatórios de avançado**. Você poderá ver dados como o tempo mais rápido (ou mais lento) para abrir uma mensagem de email de simulação de ataque, o tempo mais rápido (ou mais lento), cliquem em um link na mensagem e muito mais.</span><span class="sxs-lookup"><span data-stu-id="35873-p123">**Advanced reporting capabilities**. You'll be able to see data such as the fastest (or slowest) time to open an attack simulation email message, the fastest (or slowest) time to click a link in the message, and more.</span></span>
- <span data-ttu-id="35873-p124">**Editor de modelos de email**. Você pode criar um modelo de email personalizado, reutilizável que você pode usar para as simulações de ataque futuro.</span><span class="sxs-lookup"><span data-stu-id="35873-p124">**Email template editor**. You can create a custom, reusable email template that you can use for future attack simulations.</span></span>

<span data-ttu-id="35873-199">Visite o [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap) para ver as novidades no desenvolvimento, o que é aplicação e o que já é iniciado.</span><span class="sxs-lookup"><span data-stu-id="35873-199">Visit the [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap) to see what's in development, what's rolling out, and what's already launched.</span></span>




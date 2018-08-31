---
title: Simulador de ataque no Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/19/2018
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: da5845db-c578-4a41-b2cb-5a09689a551b
description: Saiba mais sobre três tipos diferentes de ataques virtuais que você pode executar usando simulador de ataque.
ms.openlocfilehash: 364144c0b2f8109c67fb262ce879414088380ebe
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523790"
---
# <a name="attack-simulator-in-office-365"></a><span data-ttu-id="65b7b-103">Simulador de ataque no Office 365</span><span class="sxs-lookup"><span data-stu-id="65b7b-103">Attack Simulator in Office 365</span></span>

<span data-ttu-id="65b7b-p101">Com simulador de ataque (incluído no [Office 365 Threat Intelligence](office-365-ti.md)), se você for um membro da equipe de segurança da sua organização, você pode executar os cenários de ataque realístico em sua organização. Isso pode ajudá-lo a identificar e encontrar vulnerável usuários antes de um ataque real afeta sua linha inferior.</span><span class="sxs-lookup"><span data-stu-id="65b7b-p101">With Attack Simulator (included in [Office 365 Threat Intelligence](office-365-ti.md)), if you are a member of your organization's security team, you can run realistic attack scenarios in your organization. This can help you identify and find vulnerable users before a real attack impacts your bottom line.</span></span>
  
## <a name="the-attacks"></a><span data-ttu-id="65b7b-106">Os ataques</span><span class="sxs-lookup"><span data-stu-id="65b7b-106">The Attacks</span></span>

<span data-ttu-id="65b7b-107">Na versão preview oferecemos três tipos de simulações de ataque que podem ser executadas:</span><span class="sxs-lookup"><span data-stu-id="65b7b-107">At preview release we offer three kinds of attack simulations that you can run:</span></span>
  
- [<span data-ttu-id="65b7b-108">Ataque de phishing lança de nome de exibição</span><span class="sxs-lookup"><span data-stu-id="65b7b-108">Display name spear-phishing attack</span></span>](attack-simulator.md#spearphish)
    
- [<span data-ttu-id="65b7b-109">Ataque de borrifada de senha</span><span class="sxs-lookup"><span data-stu-id="65b7b-109">Password-spray attack</span></span>](attack-simulator.md#passwordspray)
    
- [<span data-ttu-id="65b7b-110">Ataque de senha de força bruta</span><span class="sxs-lookup"><span data-stu-id="65b7b-110">Brute-force password attack</span></span>](attack-simulator.md#bruteforce)
    
<span data-ttu-id="65b7b-111">Para um ataque ser iniciados com êxito, a conta que está executando o ataque e conectado deve usar a autenticação multifator.</span><span class="sxs-lookup"><span data-stu-id="65b7b-111">For an attack to be successfully launched, the account that is running the attack and logged on must use multi-factor authentication.</span></span>
  
> [!NOTE]
> <span data-ttu-id="65b7b-112">Suporte para acesso condicional estarão disponíveis em breve.</span><span class="sxs-lookup"><span data-stu-id="65b7b-112">Support for Conditional Access is coming soon.</span></span> 
  
<span data-ttu-id="65b7b-113">Para acessar o simulador de ataque, na segurança &amp; Centro de conformidade, escolha **gerenciamento de ameaça** \> **simulador de ataque**.</span><span class="sxs-lookup"><span data-stu-id="65b7b-113">To access Attack Simulator, in the Security &amp; Compliance Center, choose **Threat management** \> **Attack simulator**.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="65b7b-114">Antes de começar...</span><span class="sxs-lookup"><span data-stu-id="65b7b-114">Before you begin...</span></span>

<span data-ttu-id="65b7b-115">Certifique-se de que você e sua organização atendem aos seguintes requisitos para simulador de ataque:</span><span class="sxs-lookup"><span data-stu-id="65b7b-115">Make sure that you and your organization meet the following requirements for Attack Simulator:</span></span>
  
- <span data-ttu-id="65b7b-116">Sua organização tem [Inteligência de ameaça do Office 365](office-365-ti.md), com simulador de ataque visível na segurança &amp; Centro de conformidade (vá para **gerenciamento de ameaça** \> **simulador de ataque**)</span><span class="sxs-lookup"><span data-stu-id="65b7b-116">Your organization has [Office 365 Threat Intelligence](office-365-ti.md), with Attack Simulator visible in the Security &amp; Compliance Center (go to **Threat management** \> **Attack simulator**)</span></span>
    
- <span data-ttu-id="65b7b-p102">Email da sua organização está hospedada no Exchange Online. (Simulador de ataque não está disponível para servidores de email local.)</span><span class="sxs-lookup"><span data-stu-id="65b7b-p102">Your organization's email is hosted in Exchange Online. (Attack Simulator is not available for on-premises email servers.)</span></span>
    
- <span data-ttu-id="65b7b-119">Você é um administrador global do Office 365</span><span class="sxs-lookup"><span data-stu-id="65b7b-119">You are an Office 365 global administrator</span></span>
    
- <span data-ttu-id="65b7b-120">Sua organização estiver usando [a autenticação multifator para usuários do Office 365](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)</span><span class="sxs-lookup"><span data-stu-id="65b7b-120">Your organization is using [Multi-factor authentication for Office 365 users](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)</span></span>
    
## <a name="display-name-spear-phishing-attack"></a><span data-ttu-id="65b7b-121">Ataque de phishing lança de nome de exibição</span><span class="sxs-lookup"><span data-stu-id="65b7b-121">Display name spear-phishing attack</span></span>

<span data-ttu-id="65b7b-p103">O phishing é um termo genérico para um conjunto amplo de ataques classificado como um ataque de estilo de engenharia social. Esse ataque se concentra em lança phishing, um ataque mais direcionado que é destinado a um grupo específico de indivíduos ou uma organização. Normalmente, um ataque personalizado com alguns reconhecimento realizada e usando um nome de exibição que irá gerar a confiança no destinatário, como uma mensagem de email que parece que ele tenha vindo de executivo dentro da sua organização.</span><span class="sxs-lookup"><span data-stu-id="65b7b-p103">Phishing is a generic term for a broad suite of attacks classed as a social engineering style attack. This attack is focused on spear phishing, a more targeted attack that is aimed at a specific group of individuals or an organization. Typically, a customized attack with some reconnaissance performed and using a display name that will generate trust in the recipient, such as an email message that looks like it came from an executive within your organization.</span></span>
  
<span data-ttu-id="65b7b-p104">Esse ataque enfoca permitindo que você manipule a quem a mensagem é exibida para originada por alterando o endereço de origem e de nome de exibição. Quando os ataques de phishing lança foram bem sucedidos, cibercriminosos acessem as credenciais dos usuários.</span><span class="sxs-lookup"><span data-stu-id="65b7b-p104">This attack focuses on letting you manipulate who the message appears to have originated from by changing the display name and source address. When spear-phishing attacks are successful, cybercriminals gain access to users' credentials.</span></span>
  
### <a name="to-simulate-a-spear-phishing-attack"></a><span data-ttu-id="65b7b-127">Para simular um ataque de phishing de lança</span><span class="sxs-lookup"><span data-stu-id="65b7b-127">To simulate a spear-phishing attack</span></span>

![Corpo do Email de redação](media/9bd65af4-1f9d-45c1-8c06-796d7ccfd425.jpg)
  
<span data-ttu-id="65b7b-p105">Você pode desenvolver o editor de HTML avançado diretamente no **corpo do Email** de campo próprio ou trabalhar com código fonte HTML. Há dois campos importantes para inclusão em HTML:</span><span class="sxs-lookup"><span data-stu-id="65b7b-p105">You can craft the rich HTML editor directly in the **Email body** field itself or work with HTML source. There are two important fields for inclusion in the HTML:</span></span> 
  
1. <span data-ttu-id="65b7b-131">Na segurança &amp; Centro de conformidade, escolha **gerenciamento de ameaça** \> **simulador de ataque**.</span><span class="sxs-lookup"><span data-stu-id="65b7b-131">In the Security &amp; Compliance Center, choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="65b7b-132">Especifique um nome de campanha significativo para o ataque ou selecione um modelo.</span><span class="sxs-lookup"><span data-stu-id="65b7b-132">Specify a meaningful campaign name for the attack or select a template.</span></span>
    
    ![Página inicial de phishing](media/5e93b3cc-5981-462f-8b45-bdf85d97f1b8.jpg)
  
3. <span data-ttu-id="65b7b-p106">Especifica os destinatários de destino. Isso pode ser indivíduos ou grupos em sua organização. Um destinatário de destino deve ter um Exchange Online da caixa de correio para o ataque seja bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="65b7b-p106">Specify the target recipients. This can be individuals or groups in your organization. A targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span>
    
    ![Seleção de destinatário](media/faf8c2e0-6175-4cd7-8265-0c8e727f4d0f.jpg)
  
4. <span data-ttu-id="65b7b-138">Configure os detalhes de email de Phishing.</span><span class="sxs-lookup"><span data-stu-id="65b7b-138">Configure the Phishing email details.</span></span>
    
    ![Configurar detalhes de email](media/f043608f-f8ce-4aae-be28-86e8ecc524a9.jpg)
  
    <span data-ttu-id="65b7b-p107">A formatação HTML pode ser tão complexa ou básica conforme as necessidades de sua campanha. Como ele é HTML, você pode inserir imagens e texto para aperfeiçoar credibilidade. Você tem controle na aparência a mensagem recebida no cliente de email do receptor.</span><span class="sxs-lookup"><span data-stu-id="65b7b-p107">The HTML formatting can be as complex or basic as your campaign needs. As it is HTML, you can insert images and text to enhance believability. You have control on what the received message will look like in the receiving email client.</span></span>
    
1. <span data-ttu-id="65b7b-p108">Insira o texto do campo **de (nome)** . Esse é o campo que mostra o **Nome para exibição** do cliente de recebimento de email.</span><span class="sxs-lookup"><span data-stu-id="65b7b-p108">Enter text for the **From (Name)** field. This is the field that shows in the **Display Name** in the receiving email client.</span></span> 
    
2. <span data-ttu-id="65b7b-p109">Insira o texto ou campo **de** . Esse é o campo que mostra como o endereço de email do remetente no cliente de email do receptor.</span><span class="sxs-lookup"><span data-stu-id="65b7b-p109">Enter text or the **From** field. This is the field that shows as the email address of the sender in the receiving email client.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="65b7b-p110">Você pode inserir um namespace de email existente dentro da sua organização (Isso fará o endereço de email realmente resolver no cliente de recebimento, facilitando a um modelo de confiança muito alta), ou você pode inserir um endereço de email externo. O endereço de email que você especificar não tem que existe realmente, mas ela precisa seguir o formato de um endereço SMTP válido, como user@domainname.extension.</span><span class="sxs-lookup"><span data-stu-id="65b7b-p110">You can enter an existing email namespace within your organization (doing this will make the email address actually resolve in the receiving client, facilitating a very high trust model), or you can enter an external email address. The email address that you specify does not have to actually exist, but it does need to following the format of a valid SMTP address, such as user@domainname.extension.</span></span> 
  
3. <span data-ttu-id="65b7b-p111">Usando o seletor de lista suspensa, selecione uma URL de servidor de logon de Phishing que reflete o tipo de conteúdo, que você terá dentro de seu ataque. Várias URLs com temas são fornecidos para que você escolher, como o pagamento do documento entrega, técnica, etc. Isso é efetivamente a URL que os usuários de destino serão solicitados a clicar em.</span><span class="sxs-lookup"><span data-stu-id="65b7b-p111">Using the drop-down selector, select a Phishing Login server URL that reflects the type of content you will have within your attack. Several themed URLs are provided for you to choose from, such as document delivery, technical, payroll etc. This is effectively the URL that targeted users are asked to click.</span></span>
    
4. <span data-ttu-id="65b7b-p112">Insira uma URL de página de aterrissagem personalizado. Usando essa redirecionar os usuários para uma URL que você especificar no final de um ataque bem-sucedido. Se você tiver o treinamento interno de divulgação, por exemplo, você pode especificar que aqui.</span><span class="sxs-lookup"><span data-stu-id="65b7b-p112">Enter a custom landing page URL. Using this will redirect users to a URL you specify at the end of a successful attack. If you have internal awareness training, for example, you can specify that here.</span></span>
    
5. <span data-ttu-id="65b7b-p113">Insira o texto do campo **assunto** . Esse é o campo que mostra como o **Nome da entidade** no cliente de email do receptor.</span><span class="sxs-lookup"><span data-stu-id="65b7b-p113">Enter text for the **Subject** field. This is the field that shows as the **Subject Name** in the receiving email client.</span></span> 
    
5. <span data-ttu-id="65b7b-156">Componha o **corpo do Email** que receberá o destino.</span><span class="sxs-lookup"><span data-stu-id="65b7b-156">Compose the **Email body** that the target will receive.</span></span> 
  
 <span data-ttu-id="65b7b-157">**${username}** insere o nome de destinos no corpo do Email</span><span class="sxs-lookup"><span data-stu-id="65b7b-157">**${username}** inserts the targets name into the Email body</span></span> 
  
 <span data-ttu-id="65b7b-158">**${loginserverurl}** insere a URL que queremos que os usuários de destino, clique em</span><span class="sxs-lookup"><span data-stu-id="65b7b-158">**${loginserverurl}** inserts the URL we want target users to click</span></span> 
    
6. <span data-ttu-id="65b7b-p114">Escolha **Avançar,** em seguida, **término** para iniciar o ataque. A mensagem de email de phishing lança é entregue às caixas de correio dos seus destinatários de destino.</span><span class="sxs-lookup"><span data-stu-id="65b7b-p114">Choose **Next,** then **Finish** to launch the attack. The spear phishing email message is delivered to your target recipients' mailboxes.</span></span> 
    
## <a name="password-spray-attack"></a><span data-ttu-id="65b7b-161">Ataque de borrifada de senha</span><span class="sxs-lookup"><span data-stu-id="65b7b-161">Password-spray attack</span></span>

<span data-ttu-id="65b7b-p115">Um ataque de borrifada senha contra uma organização geralmente é utilizado após um ator bad com êxito tem enumerado uma lista de usuários válidos de locatário, utilizando seus conhecimentos de senhas comuns usadas. É mais difícil detectar que força bruta abordagens e utilizados amplamente conforme ele é um ataque barato para executar.</span><span class="sxs-lookup"><span data-stu-id="65b7b-p115">A password spray attack against an organization is typically used after a bad actor has successfully enumerated a list of valid users from the tenant, utilizing their knowledge of common passwords used. It is utilized widely as it is a cheap attack to run, and harder to detect than brute force approaches.</span></span>
  
<span data-ttu-id="65b7b-164">Esse ataque enfoca permitindo que você especifique uma senha comum em relação a uma base de destino grande de usuários.</span><span class="sxs-lookup"><span data-stu-id="65b7b-164">This attack focuses on letting you specify a common password against a large target base of users.</span></span>
  
### <a name="to-simulate-a-password-spray-attack"></a><span data-ttu-id="65b7b-165">Para simular um ataque borrifada de senha</span><span class="sxs-lookup"><span data-stu-id="65b7b-165">To simulate a password-spray attack</span></span>

1. <span data-ttu-id="65b7b-166">Na segurança &amp; Centro de conformidade, escolha **gerenciamento de ameaça** \> **simulador de ataque**.</span><span class="sxs-lookup"><span data-stu-id="65b7b-166">In the Security &amp; Compliance Center, choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="65b7b-167">Especifique um nome de campanha significativo para o ataque.</span><span class="sxs-lookup"><span data-stu-id="65b7b-167">Specify a meaningful campaign name for the attack.</span></span>
    
3. <span data-ttu-id="65b7b-p116">Especifica os destinatários de destino. Isso pode ser indivíduos ou grupos em sua organização. Um destinatário de destino deve ter um Exchange Online da caixa de correio para o ataque seja bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="65b7b-p116">Specify the target recipients. This can be individuals or groups in your organization. A targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span>
    
4. <span data-ttu-id="65b7b-p117">Especifique uma senha a serem usados para o ataque. Por exemplo, uma senha comum e relevante, você pode tentar é `Fall2017`. Outro método pode ser `Spring2018`, ou `Password1`.</span><span class="sxs-lookup"><span data-stu-id="65b7b-p117">Specify a password to use for the attack. For example, one common, relevant password you could try is `Fall2017`. Another might be `Spring2018`, or `Password1`.</span></span>
    
5. <span data-ttu-id="65b7b-174">Escolha **Concluir** para iniciar o ataque.</span><span class="sxs-lookup"><span data-stu-id="65b7b-174">Choose **Finish** to launch the attack.</span></span> 
    
## <a name="brute-force-password-attack"></a><span data-ttu-id="65b7b-175">Ataque de senha de força bruta</span><span class="sxs-lookup"><span data-stu-id="65b7b-175">Brute-force password attack</span></span>

<span data-ttu-id="65b7b-p118">Um ataque de senha de força bruta contra uma organização geralmente é utilizado após um ator bad com êxito tem enumerado uma lista dos principais usuários de Inquilino. Esse ataque enfoca permitindo que você especifique um conjunto de senhas em relação a um único usuário.</span><span class="sxs-lookup"><span data-stu-id="65b7b-p118">A brute-force password attack against an organization is typically used after a bad actor has successfully enumerated a list of key users from the tenant. This attack focuses on letting you specify a set of passwords against a single user.</span></span>
  
### <a name="to-simulate-a-brute-force-password-attack"></a><span data-ttu-id="65b7b-178">Para simular um ataque de senha de força bruta</span><span class="sxs-lookup"><span data-stu-id="65b7b-178">To simulate a brute-force password attack</span></span>

1. <span data-ttu-id="65b7b-179">Na segurança &amp; Centro de conformidade, escolha **gerenciamento de ameaça** \> **simulador de ataque**.</span><span class="sxs-lookup"><span data-stu-id="65b7b-179">In the Security &amp; Compliance Center, choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="65b7b-180">Especifique um nome de campanha significativo para o ataque.</span><span class="sxs-lookup"><span data-stu-id="65b7b-180">Specify a meaningful campaign name for the attack.</span></span>
    
3. <span data-ttu-id="65b7b-p119">Especifique o destinatário de destino. Um destinatário de destino deve ter um Exchange Online da caixa de correio para o ataque seja bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="65b7b-p119">Specify the target recipient. A targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span>
    
4. <span data-ttu-id="65b7b-p120">Especifique um conjunto de senhas a ser usado para o ataque. Por exemplo, uma senha comum e relevante, você pode tentar é `Fall2017`. Outro método pode ser `Spring2018`, ou `Password1`.</span><span class="sxs-lookup"><span data-stu-id="65b7b-p120">Specify a set of passwords to use for the attack. For example, one common, relevant password you could try is `Fall2017`. Another might be `Spring2018`, or `Password1`.</span></span>
    
5. <span data-ttu-id="65b7b-186">Escolha **Concluir** para iniciar o ataque.</span><span class="sxs-lookup"><span data-stu-id="65b7b-186">Choose **Finish** to launch the attack.</span></span> 
    
## <a name="related-topics"></a><span data-ttu-id="65b7b-187">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="65b7b-187">Related topics</span></span>

[<span data-ttu-id="65b7b-188">Inteligência Contra Ameaças do Office 365</span><span class="sxs-lookup"><span data-stu-id="65b7b-188">Office 365 Threat Intelligence</span></span>](office-365-ti.md)
  


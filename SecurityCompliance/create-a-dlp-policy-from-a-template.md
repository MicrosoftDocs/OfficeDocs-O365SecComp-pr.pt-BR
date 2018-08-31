---
title: Criar uma política de DLP a partir de um modelo
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.NewPolicyFromTemplate
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Strat_O365_IP
search.appverid:
- MET150
ms.assetid: 59414438-99f5-488b-975c-5023f2254369
description: 'A maneira mais fácil e mais comuns para começar a políticas de DLP é usar um dos modelos incluídos no Office 365. '
ms.openlocfilehash: 4e3a5d731538e4998858b5f9f7a296c43e6774ac
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524109"
---
# <a name="create-a-dlp-policy-from-a-template"></a><span data-ttu-id="97bc8-103">Criar uma política de DLP a partir de um modelo</span><span class="sxs-lookup"><span data-stu-id="97bc8-103">Create a DLP policy from a template</span></span>

<span data-ttu-id="97bc8-p101">A maneira mais fácil e mais comuns para começar a políticas de DLP é usar um dos modelos incluídos no Office 365. Você pode usar um desses modelos encontram ou personalizar as regras para atender aos requisitos de conformidade específicos da sua organização.</span><span class="sxs-lookup"><span data-stu-id="97bc8-p101">The easiest, most common way to get started with DLP policies is to use one of the templates included in Office 365. You can use one of these templates as is, or customize the rules to meet your organization's specific compliance requirements.</span></span>
  
<span data-ttu-id="97bc8-p102">O Office 365 inclui mais de 40 modelos prontos para uso que podem ajudar você a atender a uma grande variedade de necessidades comuns de regulamentação e de política de negócios. Por exemplo, existem modelos de política de DLP para:</span><span class="sxs-lookup"><span data-stu-id="97bc8-p102">Office 365 includes over 40 ready-to-use templates that can help you meet a wide range of common regulatory and business policy needs. For example, there are DLP policy templates for:</span></span>
  
- <span data-ttu-id="97bc8-108">Ato Gramm-Leach-Bliley (GLBA)</span><span class="sxs-lookup"><span data-stu-id="97bc8-108">Gramm-Leach-Bliley Act (GLBA)</span></span>
    
- <span data-ttu-id="97bc8-109">Padrão de Segurança de Dados da Indústria de cartões de Pagamento (PCI-DSS)</span><span class="sxs-lookup"><span data-stu-id="97bc8-109">Payment Card Industry Data Security Standard (PCI-DSS)</span></span>
    
- <span data-ttu-id="97bc8-110">Informações Pessoalmente Identificáveis nos Estados Unidos (U.S. PII)</span><span class="sxs-lookup"><span data-stu-id="97bc8-110">United States Personally Identifiable Information (U.S. PII)</span></span>
    
- <span data-ttu-id="97bc8-111">Ato do Seguro de Saúde (HIPAA) dos EUA</span><span class="sxs-lookup"><span data-stu-id="97bc8-111">United States Health Insurance Act (HIPAA)</span></span>
    
<span data-ttu-id="97bc8-p103">Você pode ajustar um modelo modificando uma das regras existentes ou adicionando novas. Por exemplo, você pode adicionar novos tipos de informações confidenciais a uma regra, modificar as contagens em uma regra para torná-la mais difícil ou mais fácil de disparar, permitir que as pessoas substituam as ações em uma regra fornecendo uma justificativa de negócios ou alterar para quem as notificações e os relatórios de incidentes são enviados. Um modelo de política de DLP é um ponto de partida flexível para muitos cenários de conformidade comuns.</span><span class="sxs-lookup"><span data-stu-id="97bc8-p103">You can fine tune a template by modifying any of the existing rules or adding new ones. For example, you can add new types of sensitive information to a rule, modify the counts in a rule to make it harder or easier to trigger, allow people to override the actions in a rule by providing a business justification, or change who notifications and incident reports are sent to. A DLP policy template is a flexible starting point for many common compliance scenarios.</span></span>
  
<span data-ttu-id="97bc8-115">Você também pode escolher o modelo Personalizado, que não tem nenhuma regra padrão, e configurar sua política de DLP do zero, para atender aos requisitos de conformidade específicos de sua organização.</span><span class="sxs-lookup"><span data-stu-id="97bc8-115">You can also choose the Custom template, which has no default rules, and configure your DLP policy from scratch, to meet the specific compliance requirements for your organization.</span></span>
  
## <a name="example-identify-sensitive-information-across-all-onedrive-for-business-sites-and-restrict-access-for-people-outside-your-organization"></a><span data-ttu-id="97bc8-116">Exemplo: Identificar informações confidenciais entre todos os OneDrive para sites corporativos e restringir o acesso de pessoas fora da sua organização</span><span class="sxs-lookup"><span data-stu-id="97bc8-116">Example: Identify sensitive information across all OneDrive for Business sites and restrict access for people outside your organization</span></span>

<span data-ttu-id="97bc8-p104">OneDrive para contas de negócios tornam mais fácil para as pessoas em sua organização colaborem e compartilhem documentos. Mas uma preocupação comuns para oficiais de conformidade é que informações confidenciais armazenadas em OneDrive para contas de negócios podem ser compartilhadas inadvertidamente com pessoas fora da sua organização. Uma política de DLP pode ajudar a atenuar esse risco.</span><span class="sxs-lookup"><span data-stu-id="97bc8-p104">OneDrive for Business accounts make it easy for people across your organization to collaborate and share documents. But a common concern for compliance officers is that sensitive information stored in OneDrive for Business accounts may be inadvertently shared with people outside your organization. A DLP policy can help mitigate this risk.</span></span>
  
<span data-ttu-id="97bc8-p105">Neste exemplo, você criará uma política de DLP que identifica os dados de PII EUA, que inclui os números de passaporte EUA, números do seguro Social e números de identificação de contribuinte Individual (ITIN). Você começará usando um modelo e, em seguida, você irá modificar o modelo para atender aos requisitos de conformidade da sua organização — especificamente, você vai:</span><span class="sxs-lookup"><span data-stu-id="97bc8-p105">In this example, you'll create a DLP policy that identifies U.S. PII data, which includes Individual Taxpayer Identification Numbers (ITIN), Social Security Numbers, and U.S. passport numbers. You'll get started by using a template, and then you'll modify the template to meet your organization's compliance requirements—specifically, you'll:</span></span>
  
- <span data-ttu-id="97bc8-122">Adicionar alguns dos tipos de números de conta bancária information—U.S. confidenciais e números de licença de motorista US — para que a política de DLP protege ainda mais dos seus dados confidenciais.</span><span class="sxs-lookup"><span data-stu-id="97bc8-122">Add a couple of types of sensitive information—U.S. bank account numbers and U.S. driver's license numbers—so that the DLP policy protects even more of your sensitive data.</span></span>
    
- <span data-ttu-id="97bc8-123">Verifique a política mais sensíveis, para que uma única ocorrência de informações confidenciais seja suficiente para restringir o acesso de usuários externos.</span><span class="sxs-lookup"><span data-stu-id="97bc8-123">Make the policy more sensitive, so that a single occurrence of sensitive information is enough to restrict access for external users.</span></span>
    
- <span data-ttu-id="97bc8-p106">Permitir que os usuários substituam as ações fornecendo uma justificativa comercial ou relatar um falso positivo. Dessa forma, sua política DLP não impedirá que pessoas realizarem seus trabalhos, desde que eles tenham um motivo comercial válido para o compartilhamento de informações confidenciais da organização.</span><span class="sxs-lookup"><span data-stu-id="97bc8-p106">Allow users to override the actions by providing a business justification or reporting a false positive. This way, your DLP policy won't prevent people in your organization from getting their work done, provided they have a valid business reason for sharing the sensitive information.</span></span>
    
### <a name="create-a-dlp-policy-from-a-template"></a><span data-ttu-id="97bc8-126">Criar uma política de DLP a partir de um modelo</span><span class="sxs-lookup"><span data-stu-id="97bc8-126">Create a DLP policy from a template</span></span>

1. <span data-ttu-id="97bc8-127">Vá para [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="97bc8-127">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="97bc8-p107">Entrar no Office 365 usando sua conta do trabalho ou da escola. Agora você está de segurança do Office 365 &amp; Centro de conformidade.</span><span class="sxs-lookup"><span data-stu-id="97bc8-p107">Sign in to Office 365 using your work or school account. You're now in the Office 365 Security &amp; Compliance Center.</span></span>
    
3. <span data-ttu-id="97bc8-130">Na segurança &amp; Centro de conformidade \> barra de navegação esquerda \> **prevenção de perda de dados** \> **política** \> **+ criar uma política**.</span><span class="sxs-lookup"><span data-stu-id="97bc8-130">In the Security &amp; Compliance Center \> left navigation \> **Data loss prevention** \> **Policy** \> **+ Create a policy**.</span></span>
    
    ![Criar um botão de política](media/b1e48a08-92e2-47ca-abdc-4341694ddc7c.png)
  
4. <span data-ttu-id="97bc8-132">Escolha o modelo de política DLP que protege os tipos de informações confidenciais que você precisa \> **próximo**.</span><span class="sxs-lookup"><span data-stu-id="97bc8-132">Choose the DLP policy template that protects the types of sensitive information that you need \> **Next**.</span></span>
    
    <span data-ttu-id="97bc8-133">Neste exemplo, você vai selecionar **privacidade** \> **dados US pessoalmente identificáveis informações (PII)** porque ele já inclui a maioria dos tipos de informações confidenciais que você queira proteger — você adicionará algumas posteriormente.</span><span class="sxs-lookup"><span data-stu-id="97bc8-133">In this example, you'll select **Privacy** \> **U.S. Personally Identifiable Information ‎(PII)‎ Data** because it already includes most of the types of sensitive information that you want to protect—you'll add a couple later.</span></span> 
    
    <span data-ttu-id="97bc8-134">Quando você seleciona um modelo, você pode ler a descrição da direita para saber o que protege os tipos de informações confidenciais o modelo.</span><span class="sxs-lookup"><span data-stu-id="97bc8-134">When you select a template, you can read the description on the right to learn what types of sensitive information the template protects.</span></span>
    
    ![Página para escolher um modelo de política DLP](media/775266f6-ad87-4080-8d7c-97f2e7403b30.png)
  
5. <span data-ttu-id="97bc8-136">Nomeie a diretiva \> **próximo**.</span><span class="sxs-lookup"><span data-stu-id="97bc8-136">Name the policy \> **Next**.</span></span>
    
6. <span data-ttu-id="97bc8-137">Para escolher os locais que você deseja que a política DLP para proteger, siga um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="97bc8-137">To choose the locations that you want the DLP policy to protect, do one of the following:</span></span>
    
  - <span data-ttu-id="97bc8-138">Escolha **todos os locais no Office 365** \> **próximo**.</span><span class="sxs-lookup"><span data-stu-id="97bc8-138">Choose **All locations in Office 365** \> **Next**.</span></span>
    
  - <span data-ttu-id="97bc8-p108">Escolha **Deixe-me escolher locais específicos** \> **próximo**. Neste exemplo, escolha esta opção.</span><span class="sxs-lookup"><span data-stu-id="97bc8-p108">Choose **Let me choose specific locations** \> **Next**. For this example, choose this.</span></span>
    
    <span data-ttu-id="97bc8-141">Para incluir ou excluir um local inteiro como todos os emails do Exchange ou todas as contas de OneDrive, alterne o **Status** desse local ativada ou desativada.</span><span class="sxs-lookup"><span data-stu-id="97bc8-141">To include or exclude an entire location such as all Exchange email or all OneDrive accounts, switch the **Status** of that location on or off.</span></span> 
    
    <span data-ttu-id="97bc8-p109">Para incluir somente específico de sites do SharePoint ou OneDrive para contas de negócios, alternar o **Status** para e, em seguida, clique nos links em **incluir** escolha sites específicos ou contas. Quando você aplica uma política a um site, as regras configuradas nessa política são automaticamente aplicadas a todos os subsites desse site.</span><span class="sxs-lookup"><span data-stu-id="97bc8-p109">To include only specific SharePoint sites or OneDrive for Business accounts, switch the **Status** to on, and then click the links under **Include** to choose specific sites or accounts. When you apply a policy to a site, the rules configured in that policy are automatically applied to all subsites of that site.</span></span> 
    
    ![Opções para locais onde uma política DLP pode ser aplicada](media/ee50a61a-e867-4571-a150-3eec8d83650f.png)
  
    <span data-ttu-id="97bc8-145">Neste exemplo, para proteger informações confidenciais armazenadas em todos os OneDrive para contas de negócios, desativar o **Status** para **email do Exchange** e **sites do SharePoint**e deixe o **Status** em contas do **OneDrive**.</span><span class="sxs-lookup"><span data-stu-id="97bc8-145">In this example, to protect sensitive information stored in all OneDrive for Business accounts, turn off the **Status** for both **Exchange email** and **SharePoint sites**, and leave the **Status** on for **OneDrive accounts**.</span></span>
    
7. <span data-ttu-id="97bc8-146">Escolha **Configurações avançadas de uso** \> **próximo**.</span><span class="sxs-lookup"><span data-stu-id="97bc8-146">Choose **Use advanced settings** \> **Next**.</span></span>
    
8. <span data-ttu-id="97bc8-p110">Um modelo de política DLP contém predefinidas regras com condições e ações que detectam e agirá tipos específicos de informações confidenciais. Você pode editar, excluir, ou desativar qualquer uma das regras existentes ou adicionar novos. Quando terminar, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="97bc8-p110">A DLP policy template contains predefined rules with conditions and actions that detect and act upon specific types of sensitive information. You can edit, delete, or turn off any of the existing rules, or add new ones. When done, click **Next**.</span></span>
    
    ![Expandida de regras no modelo de diretiva de PII conosco](media/3bc9f1b6-f8ad-4334-863a-24448bb87687.png)
  
    <span data-ttu-id="97bc8-151">Neste exemplo, o modelo de dados de PII dos EUA inclui duas regras predefinidas:</span><span class="sxs-lookup"><span data-stu-id="97bc8-151">In this example, the U.S. PII Data template includes two predefined rules:</span></span>
    
  - <span data-ttu-id="97bc8-p111">**Baixo volume de conteúdo detectada PII dos EUA** Esta regra procura por arquivos que contêm entre 1 e 10 ocorrências de cada um dos três tipos de informações confidenciais (EUA, SSN e ITIN números de passaporte), onde os arquivos são compartilhados com pessoas fora da organização. Se encontrado, a regra envia uma notificação de e-mail para o administrador de conjunto de sites primário, o proprietário do documento, e a pessoa que fez a última modificação do documento.</span><span class="sxs-lookup"><span data-stu-id="97bc8-p111">**Low volume of content detected U.S. PII** This rule looks for files containing between 1 and 10 occurrences of each of three types of sensitive information (ITIN, SSN, and U.S. passport numbers), where the files are shared with people outside the organization. If found, the rule sends an email notification to the primary site collection administrator, document owner, and person who last modified the document.</span></span> 
    
  - <span data-ttu-id="97bc8-p112">**Alto volume de conteúdo detectada PII dos EUA** Esta regra procura por arquivos que contêm 10 ou mais ocorrências de cada uma dos mesmos três tipos de informações confidenciais, onde os arquivos são compartilhados com pessoas fora da organização. Se encontrado, essa ação também envia uma notificação de e-mail, mais ele restringe o acesso ao arquivo. Para conteúdo em um OneDrive for Business account, isso significa que as permissões do documento são restritas para todos, exceto o administrador do conjunto de sites primário, o proprietário do documento e a pessoa que modificou o documento por último.</span><span class="sxs-lookup"><span data-stu-id="97bc8-p112">**High volume of content detected U.S. PII** This rule looks for files containing 10 or more occurrences of each of the same three sensitive information types, where the files are shared with people outside the organization. If found, this action also sends an email notification, plus it restricts access to the file. For content in a OneDrive for Business account, this means that permissions for the document are restricted for everyone except the primary site collection administrator, document owner, and person who last modified the document.</span></span> 
    
    <span data-ttu-id="97bc8-p113">Para atender aos requisitos específicos da sua organização, convém tornar as regras mais fácil de gatilho, para que uma única ocorrência de informações confidenciais seja suficiente para bloquear o acesso de usuários externos. Depois de verificar a essas regras, você compreende que não precisa de regras de contagem de baixa e alta — você precisa apenas uma única regra que bloqueia o acesso se qualquer ocorrência de informações confidenciais for encontrada.</span><span class="sxs-lookup"><span data-stu-id="97bc8-p113">To meet your organization's specific requirements, you may want to make the rules easier to trigger, so that a single occurrence of sensitive information is enough to block access for external users. After looking at these rules, you understand that you don't need low and high count rules—you need only a single rule that blocks access if any occurrence of sensitive information is found.</span></span>
    
    <span data-ttu-id="97bc8-159">Para expandir a regra chamada **baixo volume de conteúdo detectada US PII** \> **Excluir regra**.</span><span class="sxs-lookup"><span data-stu-id="97bc8-159">So you expand the rule named **Low volume of content detected U.S. PII** \> **Delete rule**.</span></span>
    
    ![Excluir botão regra](media/bc36f7d2-0fae-4af1-92e8-95ba51077b12.png)
  
9. <span data-ttu-id="97bc8-p114">Agora, neste exemplo, você precisa adicionar dois tipos de informações confidenciais (números de conta bancária dos Estados Unidos e números de licença de motorista EUA), permitir que os usuários substituam uma regra e altere a contagem para qualquer ocorrência. Você pode fazer tudo isso editando uma regra, portanto, selecione **alto volume de conteúdo detectada US PII** \> **Editar regra**.</span><span class="sxs-lookup"><span data-stu-id="97bc8-p114">Now, in this example, you need to add two sensitive information types (U.S. bank account numbers and U.S. driver's license numbers), allow people to override a rule, and change the count to any occurrence. You can do all of this by editing one rule, so select **High volume of content detected U.S. PII** \> **Edit rule**.</span></span>
    
    ![Editar botão regra](media/eaf54067-4945-4c98-8dd6-fb2c5d6de075.png)
  
10. <span data-ttu-id="97bc8-p115">Para adicionar um tipo de informação confidencial, na seção **condições** da \> **tipos de adicionar ou alterar**. Em seguida, em **Adicionar ou alterar tipos** \> escolha **Adicionar** \> selecione **O número de conta bancária dos Estados Unidos** e **O número de carteira de motorista US** \> **Add** \> **feito**.</span><span class="sxs-lookup"><span data-stu-id="97bc8-p115">To add a sensitive information type, in the **Conditions** section \> **Add or change types**. Then, under **Add or change types** \> choose **Add** \> select **U.S. Bank Account Number** and **U.S. Driver's License Number** \> **Add** \> **Done**.</span></span>
    
    ![Opção para adicionar ou alterar tipos](media/c6c3ae86-f7db-40a8-a6e4-db11692024be.png)
  
    ![Adicionar ou alterar o painel de tipos](media/fdbb96af-b914-4a6c-a97b-bbd014689965.png)
  
11. <span data-ttu-id="97bc8-p116">Para alterar a contagem (o número de instâncias de informações confidenciais necessárias para acionar a regra), em **contagem de instância** \> , escolha o valor **mínimo** para cada tipo \> insira 1. A contagem mínima não pode estar vazia. A contagem máxima pode ficar em branco; um valor vazio **max** converter em **qualquer**.</span><span class="sxs-lookup"><span data-stu-id="97bc8-p116">To change the count (the number of instances of sensitive information required to trigger the rule), under **Instance count** \> choose the **min** value for each type \> enter 1. The minimum count cannot be empty. The maximum count can be empty; an empty **max** value convert to **any**.</span></span>
    
    <span data-ttu-id="97bc8-p117">Quando terminar, a contagem de min para todos os tipos de informações confidenciais deve ser **1** e a contagem máxima deve ser **qualquer**. Em outras palavras, qualquer ocorrência desse tipo de informações confidenciais serão satisfaz essa condição.</span><span class="sxs-lookup"><span data-stu-id="97bc8-p117">When finished, the min count for all of the sensitive information types should be **1** and the max count should be **any**. In other words, any occurrence of this type of sensitive information will satisfy this condition.</span></span>
    
    ![Contagens de instância para os tipos de informações confidenciais](media/5c6e08cb-59a9-4558-b54b-d899836d4737.png)
  
12. <span data-ttu-id="97bc8-174">Para a personalização final, você não quer suas políticas de DLP para impedir que pessoas fazendo seu trabalho, quando tiverem uma justificativa comercial válido ou encontrar um falso positivo, portanto você deseja que a notificação de usuário para incluir opções para substituir a ação de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="97bc8-174">For the final customization, you don't want your DLP policies to block people from doing their work when they have a valid business justification or encounter a false positive, so you want the user notification to include options to override the blocking action.</span></span>
    
    <span data-ttu-id="97bc8-175">Na seção **notificações de usuário** , você pode ver que notificações por email e dicas de política estiver ativadas por padrão para esta regra no modelo.</span><span class="sxs-lookup"><span data-stu-id="97bc8-175">In the **User notifications** section, you can see that email notifications and policy tips are turned on by default for this rule in the template.</span></span> 
    
    <span data-ttu-id="97bc8-p118">Na seção **usuário substitui** , você pode ver que são ativadas substituições de uma justificativa comercial, mas substituições a ser relatado falsos positivos não são. Escolha **Substituir a regra automaticamente se eles relatá-la como falso positivo**.</span><span class="sxs-lookup"><span data-stu-id="97bc8-p118">In the **User overrides** section, you can see that overrides for a business justification are turned on, but overrides to report false positives are not. Choose **Override the rule automatically if they report it as a false positive**.</span></span>
    
    ![Seção de notificações de usuário e a seção de substituições de usuário](media/62720e7a-a939-4c03-b414-67748f3d64a0.png)
  
13. <span data-ttu-id="97bc8-179">Na parte superior do editor de regra, altere o nome dessa regra do padrão **alto volume de conteúdo detectada PII EUA** para **qualquer conteúdo detectado com US PII** porque agora é disparado por qualquer ocorrência de seus tipos de informações confidenciais.</span><span class="sxs-lookup"><span data-stu-id="97bc8-179">At the top of the rule editor, change the name of this rule from the default **High volume of content detected U.S. PII** to **Any content detected with U.S. PII** because it's now triggered by any occurrence of its sensitive information types.</span></span> 
    
14. <span data-ttu-id="97bc8-180">Na parte inferior do editor de regra \> **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="97bc8-180">At the bottom of the rule editor \> **Save**.</span></span>
    
15. <span data-ttu-id="97bc8-181">Revise as condições e ações para essa regra \> **próximo**.</span><span class="sxs-lookup"><span data-stu-id="97bc8-181">Review the conditions and actions for this rule \> **Next**.</span></span>
    
    <span data-ttu-id="97bc8-p119">À direita, observe o **Status** de alternar para a regra. Se você desativar uma política inteira, todas as regras contidas na política também estão desativadas. No entanto, aqui você pode desativar uma regra específica sem desativar toda a diretiva. Isso pode ser útil quando você precisar investigar uma regra que está gerando um grande número de falsos positivos.</span><span class="sxs-lookup"><span data-stu-id="97bc8-p119">On the right, notice the **Status** switch for the rule. If you turn off an entire policy, all rules contained in the policy are also turned off. However, here you can turn off a specific rule without turning off the entire policy. This can be useful when you need to investigate a rule that is generating a large number of false positives.</span></span> 
    
16. <span data-ttu-id="97bc8-186">Na próxima página, ler e entender o seguinte e, em seguida, escolha se deseja ativar a regra ou teste-out primeiro \> **próximo**.</span><span class="sxs-lookup"><span data-stu-id="97bc8-186">On the next page, read and understand the following, and then choose whether to turn on the rule or test it out first \> **Next**.</span></span>
    
     <span data-ttu-id="97bc8-p120">Antes de criar suas políticas de DLP, você deve considerar distribuí-las gradualmente para avaliar o impacto e testar sua eficácia antes de você impô-las totalmente. Por exemplo, você não quer uma nova política DLP acidentalmente bloquear o acesso a milhares de documentos que pessoas precisam para realizar seus trabalhos.</span><span class="sxs-lookup"><span data-stu-id="97bc8-p120">Before you create your DLP policies, you should consider rolling them out gradually to assess their impact and test their effectiveness before you fully enforce them. For example, you don't want a new DLP policy to unintentionally block access to thousands of documents that people require to get their work done.</span></span> 
    
    <span data-ttu-id="97bc8-189">Se você estiver criando políticas de DLP com um grande potencial impacto, é recomendável seguir nesta sequência:</span><span class="sxs-lookup"><span data-stu-id="97bc8-189">If you're creating DLP policies with a large potential impact, we recommend following this sequence:</span></span>
    
17. <span data-ttu-id="97bc8-p121">Iniciar no modo de teste sem Dicas de Política e, em seguida, usar os relatórios de DLP para avaliar o impacto. Você pode usar relatórios de DLP para exibir o número, o local, o tipo e a gravidade das correspondências de política. Com base nos resultados, você pode ajustar as regras conforme necessário. No modo de teste, as políticas de DLP não afetarão a produtividade das pessoas que trabalham na sua organização.</span><span class="sxs-lookup"><span data-stu-id="97bc8-p121">Start in test mode without Policy Tips and then use the DLP reports to assess the impact. You can use DLP reports to view the number, location, type, and severity of policy matches. Based on the results, you can fine tune the rules as needed. In test mode, DLP policies will not impact the productivity of people working in your organization.</span></span> 
    
18. <span data-ttu-id="97bc8-p122">Mover para o modo de teste com Dicas de Política e notificações para que você possa começar a ensinar os usuários sobre suas políticas de conformidade e prepará-los para as regras que serão aplicadas. Nesse estágio, você também pode pedir aos usuários para relatar falsos positivos para que você possa refinar as regras.</span><span class="sxs-lookup"><span data-stu-id="97bc8-p122">Move to Test mode with notifications and Policy Tips so that you can begin to teach users about your compliance policies and prepare them for the rules that are going to be applied. At this stage, you can also ask users to report false positives so that you can further refine the rules.</span></span>
    
19. <span data-ttu-id="97bc8-p123">Ative as políticas para que as regras são impostas, e o conteúdo do protegidos. Continue a monitorar os relatórios DLP e quaisquer relatórios de incidentes ou notificações para certificar-se de que os resultados são o que você pretende.</span><span class="sxs-lookup"><span data-stu-id="97bc8-p123">Turn on the policies so that the rules are enforced and the content's protected. Continue to monitor the DLP reports and any incident reports or notifications to make sure that the results are what you intend.</span></span> 
    
    ![Opções para usar o modo de teste e ativar a política](media/49fafaac-c6cb-41de-99c4-c43c3e380c3a.png)
  
20. <span data-ttu-id="97bc8-199">Verifique as configurações para esta política \> escolha **criar**.</span><span class="sxs-lookup"><span data-stu-id="97bc8-199">Review your settings for this policy \> choose **Create**.</span></span>
    
<span data-ttu-id="97bc8-200">Depois de criar e ativar uma política de DLP, ele é implantado em quaisquer fontes de conteúdo que inclui, como sites do SharePoint Online ou OneDrive para contas de negócios, onde a política começa automaticamente aplicando suas regras em que o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="97bc8-200">After you create and turn on a DLP policy, it's deployed to any content sources that it includes, such as SharePoint Online sites or OneDrive for Business accounts, where the policy begins automatically enforcing its rules on that content.</span></span>
  
## <a name="view-the-status-of-a-dlp-policy"></a><span data-ttu-id="97bc8-201">Exibir o status de uma política de DLP</span><span class="sxs-lookup"><span data-stu-id="97bc8-201">View the status of a DLP policy</span></span>

<span data-ttu-id="97bc8-p124">A qualquer momento, você pode exibir o status de suas políticas de DLP na página **política** na seção de **prevenção de perda de dados** de segurança &amp; Centro de conformidade. Aqui, você pode encontrar informações importantes, como se uma política foi habilitada ou desabilitou com êxito, ou se a diretiva está no modo de teste.</span><span class="sxs-lookup"><span data-stu-id="97bc8-p124">At any time, you can view the status of your DLP policies on the **Policy** page in the **Data loss prevention** section of the Security &amp; Compliance Center. Here you can find important information, such as whether a policy was successfully enabled or disabled, or whether the policy is in test mode.</span></span> 
  
<span data-ttu-id="97bc8-204">Eis aqui os diferentes status e o que eles significam.</span><span class="sxs-lookup"><span data-stu-id="97bc8-204">Here are the different statuses and what they mean.</span></span>
  
|<span data-ttu-id="97bc8-205">**Status**</span><span class="sxs-lookup"><span data-stu-id="97bc8-205">**Status**</span></span>|<span data-ttu-id="97bc8-206">**Explicação**</span><span class="sxs-lookup"><span data-stu-id="97bc8-206">**Explanation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="97bc8-207">**Ativando…**</span><span class="sxs-lookup"><span data-stu-id="97bc8-207">**Turning on…**</span></span> <br/> |<span data-ttu-id="97bc8-p125">A política está sendo implantada nas fontes de conteúdo incluídas. A política ainda não foi imposta para todas as fontes.</span><span class="sxs-lookup"><span data-stu-id="97bc8-p125">The policy is being deployed to the content sources that it includes. The policy is not yet enforced on all sources.</span></span>  <br/> |
|<span data-ttu-id="97bc8-210">**Testando, com notificações**</span><span class="sxs-lookup"><span data-stu-id="97bc8-210">**Testing, with notifications**</span></span> <br/> |<span data-ttu-id="97bc8-p126">A política está no modo de teste. As ações em uma regra não são aplicadas, mas as correspondências de política são coletadas e podem ser visualizadas usando os relatórios de DLP. As notificações sobre correspondências de política são enviadas aos destinatários especificados.</span><span class="sxs-lookup"><span data-stu-id="97bc8-p126">The policy is in test mode. The actions in a rule are not applied, but policy matches are collected and can be viewed by using the DLP reports. Notifications about policy matches are sent to the specified recipients.</span></span>  <br/> |
|<span data-ttu-id="97bc8-214">**Testando, sem notificações**</span><span class="sxs-lookup"><span data-stu-id="97bc8-214">**Testing, without notifications**</span></span> <br/> |<span data-ttu-id="97bc8-p127">A política está no modo de teste. As ações em uma regra não são aplicadas, mas as correspondências de política são coletadas e podem ser visualizadas usando os relatórios de DLP. As notificações sobre correspondências de política não são enviadas aos destinatários especificados.</span><span class="sxs-lookup"><span data-stu-id="97bc8-p127">The policy is in test mode. The actions in a rule are not applied, but policy matches are collected and can be viewed by using the DLP reports. Notifications about policy matches are not sent to the specified recipients.</span></span>  <br/> |
|<span data-ttu-id="97bc8-218">**Ativado**</span><span class="sxs-lookup"><span data-stu-id="97bc8-218">**On**</span></span> <br/> |<span data-ttu-id="97bc8-p128">A política está ativa e imposta. A política foi implantada com êxito a todas as suas fontes de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="97bc8-p128">The policy is active and enforced. The policy was successfully deployed to all its content sources.</span></span>  <br/> |
|<span data-ttu-id="97bc8-221">**Desativando...**</span><span class="sxs-lookup"><span data-stu-id="97bc8-221">**Turning off…**</span></span> <br/> |<span data-ttu-id="97bc8-p129">A política está sendo removida para as fontes de conteúdo incluídas. A política ainda pode estar ativa e imposta em algumas fontes. Desativando uma política pode levar até 45 minutos.</span><span class="sxs-lookup"><span data-stu-id="97bc8-p129">The policy is being removed from the content sources that it includes. The policy may still be active and enforced on some sources. Turning off a policy may take up to 45 minutes.</span></span>  <br/> |
|<span data-ttu-id="97bc8-225">**Desativada**</span><span class="sxs-lookup"><span data-stu-id="97bc8-225">**Off**</span></span> <br/> |<span data-ttu-id="97bc8-p130">A política não está ativa e não foi imposta. As configurações da política (fontes, palavras-chave, duração, etc.) são salvas.</span><span class="sxs-lookup"><span data-stu-id="97bc8-p130">The policy is not active and not enforced. The settings for the policy (sources, keywords, duration, etc) are saved.</span></span>  <br/> |
|<span data-ttu-id="97bc8-228">**Excluindo...**</span><span class="sxs-lookup"><span data-stu-id="97bc8-228">**Deleting…**</span></span> <br/> |<span data-ttu-id="97bc8-p131">A política está sendo excluída. A política não está ativa e não foi imposta.</span><span class="sxs-lookup"><span data-stu-id="97bc8-p131">The policy is in the process of being deleted. The policy is not active and not enforced.</span></span>  <br/> |
   
## <a name="turn-off-a-dlp-policy"></a><span data-ttu-id="97bc8-231">Desativar uma política de DLP</span><span class="sxs-lookup"><span data-stu-id="97bc8-231">Turn off a DLP policy</span></span>

<span data-ttu-id="97bc8-p132">Você pode editar ou desativar uma política de DLP a qualquer momento. Desativar uma política desabilita todas as regras na política.</span><span class="sxs-lookup"><span data-stu-id="97bc8-p132">You can edit or turn off a DLP policy at any time. Turning off a policy disables all of the rules in the policy.</span></span>
  
<span data-ttu-id="97bc8-234">Para editar ou desativar uma política de DLP, na página **política** \> selecione a política \> **Editar política**.</span><span class="sxs-lookup"><span data-stu-id="97bc8-234">To edit or turn off a DLP policy, on the **Policy** page \> select the policy \> **Edit policy**.</span></span>
  
![Editar botão de política](media/ce319e92-0519-44fe-9507-45a409eaefe4.png)
  
<span data-ttu-id="97bc8-236">Além disso, você pode desativar cada regra individualmente editando a política e, em seguida, alternando desativa o **Status** da regra, conforme descrito acima.</span><span class="sxs-lookup"><span data-stu-id="97bc8-236">In addition, you can turn off each rule individually by editing the policy and then toggling off the **Status** of that rule, as described above.</span></span> 
  
## <a name="more-information"></a><span data-ttu-id="97bc8-237">Mais informações</span><span class="sxs-lookup"><span data-stu-id="97bc8-237">More information</span></span>

- [<span data-ttu-id="97bc8-238">Visão geral das políticas de prevenção contra perda de dados</span><span class="sxs-lookup"><span data-stu-id="97bc8-238">Overview of data loss prevention policies</span></span>](data-loss-prevention-policies.md)
    
- [<span data-ttu-id="97bc8-239">Enviar notificações e mostrar dicas de política para políticas de DLP</span><span class="sxs-lookup"><span data-stu-id="97bc8-239">Send notifications and show policy tips for DLP policies</span></span>](use-notifications-and-policy-tips.md)
    
- [<span data-ttu-id="97bc8-240">Criar uma política DLP para proteger documentos com FCI ou outras propriedades</span><span class="sxs-lookup"><span data-stu-id="97bc8-240">Create a DLP policy to protect documents with FCI or other properties</span></span>](protect-documents-that-have-fci-or-other-properties.md)
    
- [<span data-ttu-id="97bc8-241">O que os modelos de política DLP incluem</span><span class="sxs-lookup"><span data-stu-id="97bc8-241">What the DLP policy templates include</span></span>](what-the-dlp-policy-templates-include.md)
    
- [<span data-ttu-id="97bc8-242">Inventário de tipos de informações confidenciais</span><span class="sxs-lookup"><span data-stu-id="97bc8-242">Sensitive information types inventory</span></span>](what-the-sensitive-information-types-look-for.md)
    


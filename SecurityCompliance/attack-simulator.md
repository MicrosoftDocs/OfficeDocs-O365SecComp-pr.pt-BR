---
title: Simulador de ataque no Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 11/09/2018
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: da5845db-c578-4a41-b2cb-5a09689a551b
description: Como administrador global do Office 365, você pode usar o simulador de ataque para executar cenários de ataque realístico em sua organização. Isso pode ajudá-lo a identificar e encontrar vulnerável usuários antes de um ataque real atinge seu negócio.
ms.openlocfilehash: 9a7e1fd5327b4a764356df110c46ee7a9f496b53
ms.sourcegitcommit: 2cf7f5bb282c971d33e00f65d9982a3f14aec74e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/27/2018
ms.locfileid: "26706435"
---
# <a name="attack-simulator-in-office-365"></a>Simulador de ataque no Office 365

**Resumo** Se você for um administrador global do Office 365 e sua organização tem [Inteligência de ameaça do Office 365](office-365-ti.md), você pode usar o simulador de ataque para executar cenários de ataque realístico em sua organização. Isso pode ajudá-lo a identificar e encontrar vulnerável usuários antes de um ataque real afeta sua linha inferior. Leia este artigo para saber mais.
  
## <a name="the-attacks"></a>Os ataques

Três tipos de simulações de ataque estão atualmente disponíveis:
  
- [Ataque de phishing lança de nome de exibição](attack-simulator.md#spearphish)
    
- [Ataque de borrifada de senha](attack-simulator.md#passwordspray)
    
- [Ataque de senha de força bruta](attack-simulator.md#bruteforce)
    
Para um ataque ser iniciados com êxito, você pode usar a autenticação multifator a conta que você está usando para executar ataques simulados. Além disso, você deve ser um administrador global do Office 365.
  
> [!NOTE]
> Suporte para acesso condicional estarão disponíveis em breve. 
  
Para acessar o simulador de ataque, na segurança &amp; Centro de conformidade, escolha **gerenciamento de ameaça** \> **simulador de ataque**.
  
## <a name="before-you-begin"></a>Antes de começar...

Certifique-se de que você e sua organização atendem aos seguintes requisitos para simulador de ataque:
      
- Email da sua organização está hospedada no Exchange Online. (Simulador de ataque não está disponível para servidores de email local.)
    
- Você é um administrador global do Office 365
    
- Sua organização estiver usando [a autenticação multifator para usuários do Office 365](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication&view=o365-worldwide)
 
- Sua organização tem [Inteligência de ameaça do Office 365](office-365-ti.md), com simulador de ataque visível na segurança &amp; Centro de conformidade (vá para **gerenciamento de ameaça** \> **simulador de ataque**)<br/>![Gerenciamento de ameaça - simulador de ataque](media/ThreatMgmt-AttackSimulator.png)

    
## <a name="display-name-spear-phishing-attack"></a>Ataque de phishing lança de nome de exibição

O phishing é um termo genérico para um conjunto amplo de ataques classificado como um ataque de estilo de engenharia social. Esse ataque se concentra em lança phishing, um ataque mais direcionado que é destinado a um grupo específico de indivíduos ou uma organização. Normalmente, um ataque personalizado com alguns reconhecimento realizada e usando um nome de exibição que irá gerar a confiança no destinatário, como uma mensagem de email que parece que ele tenha vindo de executivo dentro da sua organização.
  
Esse ataque enfoca permitindo que você manipule a quem a mensagem é exibida para originada por alterando o endereço de origem e de nome de exibição. Quando os ataques de phishing lança foram bem sucedidos, cibercriminosos acessem as credenciais dos usuários.
  
### <a name="to-simulate-a-spear-phishing-attack"></a>Para simular um ataque de phishing de lança

![Corpo do Email de redação](media/9bd65af4-1f9d-45c1-8c06-796d7ccfd425.jpg)
  
Você pode desenvolver o editor de HTML avançado diretamente no **corpo do Email** de campo próprio ou trabalhar com código fonte HTML. Há dois campos importantes para inclusão em HTML: 
  
1. No [segurança &amp; Centro de conformidade](https://security.microsoft.com), escolha **gerenciamento de ameaça** \> **simulador de ataque**.
    
2. Especifique um nome de campanha significativo para o ataque ou selecione um modelo. <br/>![Página inicial de phishing](media/5e93b3cc-5981-462f-8b45-bdf85d97f1b8.jpg)
  
3. Especifica os destinatários de destino. Isso pode ser indivíduos ou grupos em sua organização. Cada destinatário direcionado deve ter um Exchange Online da caixa de correio para o ataque seja bem-sucedido. <br/>![Seleção de destinatário](media/faf8c2e0-6175-4cd7-8265-0c8e727f4d0f.jpg)
  
4. Configure os detalhes de email de Phishing. <br/>![Configurar detalhes de email](media/f043608f-f8ce-4aae-be28-86e8ecc524a9.jpg)<br/>A formatação HTML pode ser tão complexa ou básica conforme as necessidades de sua campanha. Como o formato de email HTML, você pode inserir imagens e texto para aperfeiçoar credibilidade. Você tem controle na aparência a mensagem recebida no cliente de email do receptor.
    
5. Especifica o texto do campo **de (nome)** . Esse é o campo que mostra o **Nome para exibição** do cliente de recebimento de email. 
    
6. Especifique o texto ou campo **de** . Esse é o campo que mostra como o endereço de email do remetente no cliente de email do receptor.<br/>Você pode inserir um namespace de email existente dentro da sua organização (Isso fará o endereço de email realmente resolver no cliente de recebimento, facilitando a um modelo de confiança muito alta), ou você pode inserir um endereço de email externo. O endereço de email que você especificar não tem que existe realmente, mas ela precisa seguir o formato de um endereço SMTP válido, como user@domainname.extension. 
  
7. Usando o seletor de lista suspensa, selecione uma URL de servidor de logon de Phishing que reflete o tipo de conteúdo, que você terá dentro de seu ataque. Várias URLs com temas são fornecidos para que você escolher, como o pagamento do documento entrega, técnica, etc. Isso é efetivamente a URL que os usuários de destino serão solicitados a clicar em.
    
8. Especifique uma URL de página de aterrissagem personalizado. Usando essa redirecionar os usuários para uma URL que você especificar no final de um ataque bem-sucedido. Se você tiver o treinamento interno de divulgação, por exemplo, você pode especificar que aqui.
    
9. Especifica o texto do campo **assunto** . Esse é o campo que mostra como o **Nome da entidade** no cliente de email do receptor. 
    
10. Componha o **corpo do Email** que receberá o destino. <br/>`${username}`Insere o nome de destinos o corpo do Email. <br/>`${loginserverurl}`Insere a URL que queremos que os usuários de destino, clique em 
    
11. Escolha **Avançar,** em seguida, **término** para iniciar o ataque. A mensagem de email de phishing lança é entregue às caixas de correio dos seus destinatários de destino. 
    
## <a name="password-spray-attack"></a>Ataque de borrifada de senha

Um ataque de borrifada senha contra uma organização geralmente é utilizado após um ator bad adquiriu com êxito uma lista de usuários válidos de Inquilino. Bad ator conhece as senhas comuns que as pessoas utilizam o uso. Esse é um ataque amplamente usado, conforme ele é um ataque barato mais difícil detectar que força bruta abordagens e execução.
  
Esse ataque enfoca permitindo que você especifique uma senha comum em relação a uma base de destino grande de usuários.
  
### <a name="to-simulate-a-password-spray-attack"></a>Para simular um ataque borrifada de senha

1. No [segurança &amp; Centro de conformidade](https://security.microsoft.com), escolha **gerenciamento de ameaça** \> **simulador de ataque**.
    
2. Especifique um nome de campanha significativo para o ataque.
    
3. Especifica os destinatários de destino. Isso pode ser indivíduos ou grupos em sua organização. Um destinatário de destino deve ter um Exchange Online da caixa de correio para o ataque seja bem-sucedido.
    
4. Especifique uma senha a serem usados para o ataque. Por exemplo, uma senha comum e relevante, você pode tentar é `Fall2017`. Outro método pode ser `Spring2018`, ou `Password1`.
    
5. Escolha **Concluir** para iniciar o ataque. 
    
## <a name="brute-force-password-attack"></a>Ataque de senha de força bruta

Um ataque de senha de força bruta contra uma organização geralmente é utilizado após um ator bad adquiriu com êxito uma lista dos principais usuários de Inquilino. Esse ataque enfoca a tentativa de um conjunto de senhas em uma única conta de usuário.
  
### <a name="to-simulate-a-brute-force-password-attack"></a>Para simular um ataque de senha de força bruta

1. No [segurança &amp; Centro de conformidade](https://security.microsoft.com), escolha **gerenciamento de ameaça** \> **simulador de ataque**.
    
2. Especifique um nome de campanha significativo para o ataque.
    
3. Especifique o destinatário de destino. Um destinatário de destino deve ter um Exchange Online da caixa de correio para o ataque seja bem-sucedido.
    
4. Especifique um conjunto de senhas a ser usado para o ataque. Você pode usar um arquivo de texto (. txt) para sua lista de senhas. O arquivo de texto não pode exceder 10 MB em tamanho de arquivo. Use uma senha por linha e certifique-se de incluir um retorno de carro após a última senha na sua lista.
    
5. Escolha **Concluir** para iniciar o ataque. 
    
## <a name="new-features-in-attack-simulator"></a>Novos recursos no simulador de ataque

Novos recursos são adicionados ao simulador de ataque. Elas incluem:
- **Recursos de relatórios de avançado**. Você poderá ver dados como o tempo mais rápido (ou mais lento) para abrir uma mensagem de email de simulação de ataque, o tempo mais rápido (ou mais lento), cliquem em um link na mensagem e muito mais.
- **Editor de modelos de email**. Você pode criar um modelo de email personalizado, reutilizável que você pode usar para as simulações de ataque futuro.

Visite o [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap) para ver as novidades no desenvolvimento, o que é aplicação e o que já é iniciado.




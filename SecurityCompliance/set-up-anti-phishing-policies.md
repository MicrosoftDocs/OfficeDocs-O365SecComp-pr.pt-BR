---
title: Configurar as políticas de antiphishing ATP do Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.date: 10/11/2018
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 5a6f2d7f-d998-4f31-b4f5-f7cbf6f38578
description: Proteção AntiPhishing, com uma proteção abrangente como parte da proteção de ameaça avançadas do Office 365 e proteção básica no Office 365 Exchange Online Protection, pode ajudar a proteger sua organização contra ataques mal-intencionados phishing baseados em representação e outros ataques de phishing. Se você for um administrador de segurança ou o Office 365 Enterprise global, você pode configurar políticas de AntiPhishing. Phishing ataques vêm em uma variedade de formulários de ataques baseados em mercadorias lança direcionado phishing ou whaling. Com a complexidade crescente, é difícil para o mesmo um olhar treinado identificar alguns desses ataques sofisticados. Felizmente, pode ajudar a proteção de ameaça avançadas do Office 365. Você pode configurar uma política de AntiPhishing para ajudar a garantir que sua organização seja protegida contra esses ataques.
ms.openlocfilehash: 0971ac2c653170f0242a1e9e3aaf111f5afc75d5
ms.sourcegitcommit: ba2175e394d0cb9f8ede9206aabb44b5b677fa0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/11/2018
ms.locfileid: "25497999"
---
# <a name="set-up-office-365-atp-anti-phishing-and-anti-phishing-policies"></a>Configurar políticas de AntiPhishing e antiphishing ATP do Office 365

[Proteção antiphishing de ATP](atp-anti-phishing.md), parte de [Proteção de ameaça avançadas do Office 365](office-365-atp.md), pode ajudar a proteger sua organização contra ataques mal-intencionados phishing baseados em representação e outros ataques de phishing. Se você for um administrador de segurança ou o Office 365 Enterprise global, você pode configurar políticas de AntiPhishing ATP. 

Phishing ataques vêm em uma variedade de formulários de ataques baseados em mercadorias lança direcionado phishing ou whaling. Com a complexidade crescente, é difícil para o mesmo um olhar treinado identificar alguns desses ataques sofisticados. Felizmente, pode ajudar a proteção de ameaça avançadas do Office 365. Você pode configurar uma política de AntiPhishing ATP para ajudar a garantir que sua organização seja protegida contra esses ataques.
  
> [!NOTE]
> ATP antiphishing só está disponível no Advanced proteção contra ameaças, disponível com o Office 365 Enterprise E5. Se sua organização estiver usando outra assinatura do Office 365 Enterprise, a proteção avançada de ameaça pode ser adquirida como um complemento. (Como um administrador global, no Centro de administração do Office 365, escolha **faturamento** \> **Adicionar assinaturas**.) Para obter mais informações sobre as opções de planejamento, consulte [Comparar todos os Office 365 para planos de negócios](https://go.microsoft.com/fwlink/?linkid=844053). Verifique se a que sua organização está usando a versão mais recente do Office 365 ProPlus no Windows para aproveitar totalmente proteção antiphishing de ATP. 

As políticas de AntiPhishing agora estão disponíveis para o Office 365 Exchange Online Protection, com um conjunto limitado de proteção antifalsificação que destina-se a proteção contra ataques baseados em descrição e autenticação.
  
O que fazer:
  
1. Revise os pré-requisitos.
    
2. Saiba mais sobre antiphishing e opções de política de AntiPhishing ATP.
    
3. Configure uma política de AntiPhishing ou um antiphishing ATP.
    
## <a name="review-the-prerequisites"></a>Revise os pré-requisitos

- Certifique-se de que você é um membro do grupo de funções **administradores de empresa** ou **administradores de segurança** . 
    
- [Saiba mais sobre as opções de política de AntiPhishing ATP](set-up-anti-phishing-policies.md#learn-about-atp-anti-phishing-policy-options) (neste artigo). 
    
- Provavelmente você irá configurar várias políticas de AntiPhishing para sua organização. O Office 365 impõe essas políticas na ordem em que são listados nas páginas **antiphishing página** e **antiphishing ATP** na segurança &amp; Centro de conformidade. Depois que você tiver revisado as opções de política, levar algum tempo para determinar quantas políticas que você precisará e a prioridade para cada um. 
    
- Planeje gastar cerca de 5 a 15 minutos para configurar sua política de AntiPhishing primeira.
    
- Permitir até 30 minutos para sua política novo ou atualizado à difusão em todos os centros de dados do Office 365.
    
## <a name="set-up-an-anti-phishing-or-atp-anti-phishing-policy"></a>Configurar uma política de AntiPhishing ATP ou de AntiPhishing

Cada organização no Office 365 tem uma política de AntiPhishing padrão que se aplica a todos os usuários. Você pode criar várias políticas antiphishing personalizadas que você pode definir o escopo para domínios, grupos ou usuários específicos dentro da sua organização. As políticas personalizadas que você criar têm precedência sobre a política padrão. Adicionar, editar e excluir diretivas de AntiPhishing no Office 365 Security &amp; Centro de conformidade.
  
1. Vá para [https://protection.office.com](https://protection.office.com) e entre com sua conta do trabalho ou da escola. 
    
2. No Office 365 Security &amp; Centro de conformidade, no painel de navegação à esquerda, em **gerenciamento de ameaça**, escolha a **política**.
    
3. Na página **política** , escolha **antiphishing** ou **antiphishing ATP**.
    
4. Na página **antiphishing** ou **ATP antiphishing** , siga um destes procedimentos: 
    
  - Para adicionar uma nova política selecione **+ criar**.
    
  - Para editar uma política existente, selecione o nome da política na lista exibida na página **antiphishing** ou escolha **Política padrão** acima da lista para editar o poicy padrão para sua organização. Na página que aparece, escolha **Editar política**.  
    
    Um assistente é iniciado que o orienta definindo sua política antiphishing.
    
5. Especifique o nome, descrição e configurações para sua política. Consulte [Saiba mais sobre as opções de política de AntiPhishing ATP](#learn-about-atp-anti-phishing-policy-options) para obter mais detalhes. 
    
6. Uma vez que você revisou suas configurações, escolha **criar essa diretiva** ou **Salvar** conforme apropriado. 
    
## <a name="learn-about-atp-anti-phishing-policy-options"></a>Saiba mais sobre opções de política de AntiPhishing ATP

Conforme você configurar ou editar suas políticas de AntiPhishing ATP, você pode escolher entre várias opções que oferecem proteção mais sofisticada e abrangente, conforme descrito na tabela a seguir:
  
|**Essa configuração**|**Faça isto**|**Uso quando você deseja:**|
|:-----|:-----|:-----|
|**Adicionar usuários para proteger** <br/> |Define quais endereços de email serão protegidos pela política. Você pode adicionar até 60 endereços internos e externos que você deseja proteger contra representação.  <br/> |Quando você deseja garantir que o email de fora da sua organização não uma representação de um dos usuários na lista de usuários que você está protegendo. Exemplos de usuários, que talvez você queira proteger são executivos de alto nível, os proprietários de negócios, membros da diretoria externos e assim por diante.<br/> Essa lista de usuários protegidos é diferente da lista de pessoas ao qual a política se aplica, ou em vez disso, para o qual a política é aplicada. Você define o aplica à lista na seção **aplicado a** das opções da diretiva.<br/> Por exemplo, se você adicionar Mary Smith \<marys@contoso.com\> como um usuário para proteger, em seguida, aplique a política para o grupo "todos os usuários". Isso garante que um email que aparecia se passem por "Mary Smith" enviada a um usuário no grupo "Todos os usuários" seria será realizado pela política.<br/> |
|**Adicionar domínios para proteger** <br/> |Permite que você escolha quais domínios que você deseja proteger contra representação. Você pode especificar que a política inclui todos os domínios personalizados, uma lista separada por vírgulas de domínios ou uma combinação dos dois. Se você escolher **incluir automaticamente os domínios que eu possuem**e mais tarde você adicionar um domínio à sua organização do Office 365, essa diretiva antiphishing será in-loco para o novo domínio.<br/> |Sempre que você deseja garantir que o email de fora da sua organização não uma representação de um dos domínios definidos na sua lista de domínios verificados ou de um domínio de parceiro.  <br/> |
|**Escolha ações** <br/> |Escolha a ação a ser executada quando o Office 365 detecta uma tentativa de representação contra os usuários e os domínios que você adicionou à política. Você pode escolher ações diferentes para os usuários e os domínios na mesma diretiva antiphishing. Essas ações se aplicam a qualquer email de entrada que tenha sido identificado pelo Office 365 como representando uma conta de usuário ou domínio que está sob a proteção dessa diretiva antiphishing.<br/> **Mensagem em quarentena** Email será enviada para quarentena do Office 365. Quando você escolher essa opção, o email não será enviado ao destinatário original.<br/> **Redirecionar a mensagem para outro endereço de email** Email será enviada para o endereço de email que você especificar. Você pode especificar vários endereços de email. Quando você escolher essa opção, o email não será enviado ao destinatário original.<br/> **Mover mensagem para a pasta Lixo eletrônico dos destinatários** Email será enviada para a pasta Lixo eletrônico dos destinatários. Quando você escolher essa opção, o email ainda é enviado ao destinatário original, mas não será colocado na caixa de entrada do destinatário.<br/> **Entregar a mensagem e adicionar outros endereços à linha Cco** Email será entregue ao destinatário original. Além disso, os usuários que você identificar serão adicionados à linha Cco da mensagem antes da entrega. Quando você escolher essa opção, o email ainda é enviado à caixa de entrada do destinatário original.<br/> **Não se aplicam a qualquer ação** Email será entregue à caixa de entrada do destinatário original. Nenhuma outra ação será tomada na mensagem de email.<br/> **Ativar dicas de proteção contra phishing** Habilita as dicas de AntiPhishing safety no email.  <br/> |Quando você deseja executar uma ação em mensagens que o Office 365 determinou seja uma representação de um usuário ou domínio, conforme definido na política.  <br/> |
|**Habilitar a inteligência de dados de caixa de correio** <br/> |Habilita ou desabilita a inteligência de dados de caixa de correio para esta diretiva. Você só pode ativar inteligência de dados de caixa de correio para nuvem contas, ou seja, contas cuja caixa de correio é hospedada inteiramente no Office 365.  <br/> |Quando você deseja melhorar os resultados de representação para usuários com base no mapa de remetente individuais de cada usuário. Inteligência de dados de caixa de correio é criada em torno das pessoas que você enviar e recebe emails de. Este intelligence permite que o Office 365 personalizar a política de representação em um nível de usuário para processar melhor os resultados positivos falsos.  <br/> |
|**Adicionar domínios e remetentes confiáveis** <br/> |Define os endereços de email e os domínios que não serão considerados impersonations por essa política. As mensagens dos endereços de email do remetente e domínios que você adiciona como remetentes confiáveis e domínios não precisar ser classificados como um ataque baseado em representação. Como resultado, as ações e configurações nessa política não ser aplicadas a mensagens destes remetentes e domínios.  <br/> |Quando os usuários interagem com domínios ou usuários que acionam a representação, mas são considerados seguras. Por exemplo, se um parceiro tiver o mesmo/semelhante Mostrar nome ou o nome de domínio como um usuário definido na lista.  <br/> |
|**Aplicadas ao** <br/> |Define os destinatários cujas mensagens de email de entrada estará sujeito as regras da política. Você pode criar condições e exceções para os destinatários associados à política.  <br/> Por exemplo, você pode criar uma política global para sua organização, aplicando a regra a todos os destinatários em seu domínio.  <br/> Você também pode criar regras de exceção, como uma regra que não verifica as mensagens de email para um grupo específico de destinatários.  <br/> |Cada diretiva deve ser associada um conjunto de usuários, por exemplo, os usuários em um domínio ou grupo específico.  <br/> |
|**Limites de phishing avançadas** <br/> |Define o nível das configurações para como mensagens de phishing são manipuladas.  <br/> **Standard** Eletrônico suspeito, ser phishing é tratado da maneira padrão.  <br/> **Agressivo** Eletrônico suspeito, seja de phishing com uma alta ou muito alto grau de confiança são manipuladas pelo sistema da mesma maneira.  <br/> **Mais agressiva** Eletrônico suspeito, seja de phishing com um meio, alto, ou muito alto grau de confiança são manipuladas pelo sistema da mesma maneira.  <br/> **Mais agressivo** Da mesma maneira, eletrônico suspeito, seja de phishing com baixo, médio, alto ou muito alto grau de confiança são tratadas pelo sistema.  <br/> |Quando você deseja ser mais agressivo no tratamento de mensagens de phishing potencialmente dentro do Office 365. Por exemplo, mensagens com uma probabilidade muito alta de sendo phishing terá as ações mais agressivas executadas neles enquanto mensagens com uma baixa probabilidade possuem menos agressivas ações executadas neles. Essa configuração também afeta outras partes do sistema de filtragem que combinam sinais juntos. A possibilidade de mover as mensagens de uma boa aumenta à medida que o nível de aumento de configurações.  <br/>|
   
## <a name="learn-about-anti-phishing-policy-options"></a>Saiba mais sobre as opções de política de AntiPhishing 

Como você configurar ou editar sua AntiPhishing, você poderá escolher entre várias opções, conforme descrito na tabela a seguir: 

|**Essa configuração**|**Faça isto**|**Uso quando você deseja:**|
|:-----|:-----|:-----|
|**Aplicadas ao** <br/> |Define os destinatários cujas mensagens de email de entrada estará sujeito as regras da política. Você pode criar condições e exceções para os destinatários associados à política.  <br/> Por exemplo, você pode criar uma política global para sua organização, aplicando a regra a todos os destinatários em seu domínio.  <br/> Você também pode criar regras de exceção, como uma regra que não verifica as mensagens de email para um grupo específico de destinatários.  <br/> |Cada diretiva deve ser associada um conjunto de usuários, por exemplo, os usuários em um domínio ou grupo específico.  <br/> | 
|**Escolha ações** <br/> |Escolha a ação a ser executada quando o Office 365 detecta uma tentativa de falsificação interna da organização ou externa-org em relação a seus usuários. Essas ações se aplicam a qualquer email de entrada que tenha sido identificado pelo Office 365, como uma tentativa de falsificação para usuários que estão sob a proteção dessa diretiva antiphishing.<br/> **Mensagem em quarentena** Email será enviada para quarentena do Office 365. Quando você escolher essa opção, o email não será enviado ao destinatário original.<br/> **Mover mensagem para a pasta Lixo eletrônico dos destinatários** Email será enviada para a pasta Lixo eletrônico dos destinatários. Quando você escolher essa opção, o email ainda é enviado ao destinatário original, mas não será colocado na caixa de entrada do destinatário.<br/> **Não se aplicam a qualquer ação** Email será entregue à caixa de entrada do destinatário original. Nenhuma outra ação será tomada na mensagem de email.<br/> |Quando você deseja executar uma ação em mensagens que o Office 365 determinou seja uma tentativa de falsificação de domínios internos ou externos, conforme definido na política.  <br/>|

Depois de sua organização tiver configurado a políticas de AntiPhishing ou políticas de AntiPhishing ATP, você pode ver como o serviço está funcionando exibindo [relatórios de proteção avançada de ameaça](view-reports-for-atp.md).
  
## <a name="example-anti-phishing-policy-to-protect-a-user-and-a-domain"></a>Exemplo: De diretiva de AntiPhishing para proteger um usuário e um domínio

Este exemplo configura uma política denominada "Domínio e CEO" que fornece proteção de usuário e o domínio de representação e, em seguida, aplica a política a todos os emails recebidos pelos usuários dentro do domínio `contoso.com`. O administrador de segurança determinou que a política deve atender a estes requisitos de negócios:
  
- A diretiva de precisa oferecem proteção para o CEO conta e todo o domínio de email.
    
- Mensagens que são determinadas para ser tentativas de representação em relação a conta de usuário do CEO precisam ser redirecionados para o endereço de email do administrador de segurança.
    
- Mensagens que são determinadas para ser tentativas de representação em relação ao domínio menos urgentes e devem ser colocados em quarentena para revisão posterior.
    
O administrador de segurança da Contoso pode usar valores como a seguir para criar uma diretiva de AntiPhishing que atenda a essas necessidades.
  
|||
|:-----|:-----|
|**Opção ou definição** <br/> |**Exemplo** <br/> |
|Nome  <br/> |Domínio e CEO  <br/> |
|Descrição  <br/> |Certifique-se de que o CEO e nosso domínio não estão sendo representadas.  <br/> |
|Adicionar usuários para proteger  <br/> |Endereço de email do CEO no mínimo.  <br/> |
|Adicionar domínios para proteger  <br/> |O domínio organizacional que inclui o escritório do CEO.  <br/> |
|Escolha ações  <br/> |Se o email é enviado por um usuário representado: escolher **redirecionar a mensagem para outro endereço de email** e digite o endereço de email do administrador de segurança, por exemplo, `securityadmin@contoso.com`.  <br/> Se o email é enviado por um domínio representado: escolher a **mensagem em quarentena**.  <br/> |
|Inteligência de dados de caixa de correio  <br/> |Por padrão, a inteligência de dados de caixa de correio é selecionada quando você cria uma nova política de AntiPhishing. Deixe esta configuração **em** para obter melhores resultados.<br/> |
|Adicionar domínios e remetentes confiáveis  <br/> |Nesse exemplo, não defina qualquer substituições.  <br/> |
|Aplicadas ao  <br/> |Selecione **o domínio do destinatário é**. Em **qualquer uma dessas**, selecione **Escolher**. Selecione **+ Adicionar**. Marque a caixa de seleção ao lado do nome do domínio, por exemplo, `contoso.com`, na lista e, em seguida, selecione **Adicionar**. Selecione **concluído**.<br/> |
   
## <a name="delete-an-anti-phishing-or-atp-anti-phishing-policy"></a>Excluir uma política de AntiPhishing ATP ou de AntiPhishing

Você pode excluir políticas personalizadas que você criou usando a segurança &amp; Centro de conformidade. Você não pode excluir a política padrão para sua organização. É recomendável usar a segurança &amp; Centro de conformidade para analisar ou editar qualquer uma das suas políticas de ATP.
  
1. Vá para [https://protection.office.com](https://protection.office.com) e entre com sua conta do trabalho ou da escola. 
    
2. No painel de navegação esquerdo, em **gerenciamento de ameaça**, escolha **uma política**.
    
3. Na página **política** , escolha **antiphishing** ou **antiphishing ATP**.
    
4. Na página **antiphishing** ou **ATP antiphishing** , selecione o nome da política na lista.

5. Na página que aparece, escolha **Excluir a política**. Permitir até 30 minutos para que suas alterações à difusão em todos os centros de dados do Office 365.
    
## <a name="related-topics"></a>Tópicos relacionados

[Proteção Avançada contra Ameaças do Office 365](office-365-atp.md) 
  
[Proteção antiphishing no Office 365](anti-phishing-protection.md)
  
[Recursos antiphishing ATP no Office 365](atp-anti-phishing.md)
  
[Configurar políticas de links seguros ATP no Office 365](set-up-atp-safe-links-policies.md)
  
[Configurar políticas de anexos seguros ATP no Office 365](set-up-atp-safe-attachments-policies.md)
  
[Exibir relatórios de Proteção avançada contra ameaças](view-reports-for-atp.md)
  


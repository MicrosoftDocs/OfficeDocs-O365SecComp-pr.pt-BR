---
title: Recursos antiphishing ATP no Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 7/2/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 5076d0f6-7a59-4d6c-bd07-ba95033f0682
description: Antiphishing ATP é oferecido como parte da proteção de ameaça avançadas do Office 365. ATP antiphishing aplica um conjunto de modelos de aprendizado de máquina junto com os algoritmos de detecção de representação às mensagens de entrada para fornecer proteção de mercadorias e lança ataques de phishing. Todas as mensagens estão sujeitos a um conjunto abrangente de modelos de aprendizado de máquina treinados para detectar mensagens de phishing, um conjunto de algoritmos avançados usado para proteger contra ataques de representação de usuário e domínio diversos. ATP antiphishing protege a sua organização de acordo com a políticas que são definidas por seu Office 365 global ou administradores de segurança.
ms.openlocfilehash: cff25316f9a03bdfafd195eb408584ab8bca6343
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523895"
---
# <a name="atp-anti-phishing-capabilities-in-office-365"></a>Recursos antiphishing ATP no Office 365

Antiphishing ATP é oferecido como parte da [Proteção de ameaça avançadas do Office 365](https://technet.microsoft.com/en-us/library/exchange-online-advanced-threat-protection-service-description.aspx). ATP antiphishing aplica um conjunto de modelos de aprendizado de máquina junto com os algoritmos de detecção de representação às mensagens de entrada para fornecer proteção de mercadorias e lança ataques de phishing. Todas as mensagens estão sujeitos a um conjunto abrangente de modelos de aprendizado de máquina treinados para detectar mensagens de phishing, um conjunto de algoritmos avançados usado para proteger contra ataques de representação de usuário e domínio diversos. ATP antiphishing protege a sua organização de acordo com a políticas que são definidas por seu Office 365 global ou administradores de segurança.
  
Para saber mais, consulte [Configurar políticas de AntiPhishing ATP no Office 365](set-up-atp-anti-phishing-policies.md).
  
> [!NOTE]
> ATP antiphishing só está disponível no Advanced proteção contra ameaças, disponível com o Office 365 Enterprise E5. Se sua organização estiver usando outra assinatura do Office 365 Enterprise, a proteção avançada de ameaça pode ser adquirida como um complemento. (Como um administrador global, no Centro de administração do Office 365, escolha **faturamento** \> **Adicionar assinaturas**.) Para obter mais informações sobre as opções de planejamento, consulte [Comparar todos os Office 365 para planos de negócios](https://go.microsoft.com/fwlink/?linkid=844053). 
    
## <a name="how-atp-anti-phishing-works"></a>Como funciona a ATP AntiPhishing
<a name="Howantiphishworks"> </a>

ATP antiphishing verifica as mensagens de entrada para que a mensagem pode ser phishing de indicadores. Sempre que um usuário é coberto por uma política de ATP (anexos seguros, links confiáveis ou antiphishing) a mensagem de entrada é avaliada por máquina vários modelos que analisar a mensagem para determinar se a política se aplica à mensagem e é a ação apropriada de aprendizagem obtido, com base na diretiva configurada.
  
ATP antiphishing permite que os administradores globais do Office 365 ou administradores de segurança definir políticas que oferecem proteção contra ataques de phishing que incluem a representação de usuários ou domínios. (ou ambos). Administradores globais do Office 365 ou administradores de segurança definem dentro da diretiva de qual usuário e os domínios deve ser protegida contra ataques de representação usando uma lista fixa de usuários ou domínios ou por meio de inteligência de dados de caixa de correio. Inteligência de dados de caixa de correio é uma compreensão avançada de hábitos de email do usuário e contatos pessoais. ATP aprende como cada usuário individual se comunica com outros usuários dentro e fora da organização e cria um mapa dessas relações. Este mapa permite ATP entender mais detalhes sobre como assegurar que as mensagens direita são identificadas como representação.
  
ATP antiphishing políticas podem ser aplicadas a um conjunto específico de pessoas ou grupos em sua organização, ou a um domínio inteiro ou todos os seus domínios personalizados. Para saber mais, consulte [Configurar políticas de AntiPhishing ATP no Office 365](set-up-atp-anti-phishing-policies.md).
  
## <a name="how-to-get-atp-anti-phishing"></a>Como obter ATP AntiPhishing
<a name="Howtogetantiphish"> </a>

Antiphishing ATP é parte da proteção de ameaça avançadas, que está incluído no Office 365 Enterprise E5. Proteção avançada de ameaça também pode ser adquirida como um complemento para o Office 365 Enterprise E1 ou Office 365 Enterprise E3. Para obter mais informações sobre as opções de planejamento, consulte [Comparar todos os Office 365 para planos de negócios](https://go.microsoft.com/fwlink/?linkid=844053).
  
ATP antiphishing se aplica quando uma política de AntiPhishing, como uma política de representação são configurados. (Consulte [Configurar políticas de AntiPhishing ATP no Office 365](set-up-atp-anti-phishing-policies.md)).
  
## <a name="how-to-know-if-atp-anti-phishing-is-in-place"></a>Como saber se antiphishing ATP é in-loco
<a name="IsantiphishOn"> </a>

Políticas de AntiPhishing ATP devem ser definidas em ordem para proteção estejam ativos. Para modelos de aprendizado de máquina de AntiPhishing ATP estar ativo para um usuário, que o usuário deve fazer parte de um anexo seguro definido, links confiáveis ou antiphishing política. A tabela a seguir descreve alguns cenários de exemplo. Em cada um desses exemplos, a empresa está usando o Office 365 Enterprise E5, que inclui a proteção avançada de ameaça.
  
|**Cenário de exemplo**|**ATP antiphishing se aplicam neste caso?**|
|:-----|:-----|
|Organização da PAT tem o Office 365 Enterprise E5, mas ninguém definiu quaisquer políticas para anexos seguros ATP, links confiáveis de ATP ou ATP avançadas phishing ainda.|Não. Embora o recurso esteja disponível, pelo menos uma política de ATP deve ser definida na ordem da máquina ATP modelos de aprendizado para trabalhar. Para representação também deve ser uma política de AntiPhishing ATP in-loco.|
|Lee é um funcionário no departamento de vendas na Contoso. Organização de Lee tem uma política de AntiPhishing ATP in-loco que se aplica aos funcionários de finance apenas.|Não. Nesse caso, ATP antiphishing (modelos de máquina e proteção de representação) aplicaria aos funcionários financeiro, mas outros funcionários, inclusive o departamento de vendas, não seriam.|
|Ontem, um administrador do Office 365 na organização de Jean configurar uma política de AntiPhishing ATP que se aplica a todos os funcionários. Anteriormente hoje, Jean recebeu uma mensagem de email que inclua uma representação coberta pela política.|Sim. Neste exemplo, Jean tem uma licença para proteção de ameaça avançadas, e uma política de AntiPhishing ATP que inclui Jean tiver sido definida. Normalmente, levará cerca de 30 minutos para uma nova política entrem em vigor em datacenters; desde que um dia passou nesse caso, a política deve estar em vigor.|
   
## <a name="related-topics"></a>Tópicos relacionados
<a name="IsantiphishOn"> </a>

[Proteção Avançada contra Ameaças do Office 365](office-365-atp.md) 
  
[Proteção antiphishing no Office 365](anti-phishing-protection.md)
  
[Configurar políticas de AntiPhishing ATP no Office 365](set-up-atp-anti-phishing-policies.md)
  
[Links de ATP seguros no Office 365](atp-safe-links.md)
  
[Configurar políticas de links seguros ATP no Office 365](set-up-atp-safe-links-policies.md)
  
[Anexos de ATP seguros no Office 365](atp-safe-attachments.md)
  
[Configurar políticas de anexos seguros ATP no Office 365](set-up-atp-safe-attachments-policies.md)
  
[Exibir relatórios de Proteção avançada contra ameaças](view-reports-for-atp.md)
  


---
title: Recursos antiphishing ATP no Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 5076d0f6-7a59-4d6c-bd07-ba95033f0682
description: Antiphishing ATP é parte da proteção de ameaça avançadas do Office 365. ATP antiphishing aplica um conjunto de modelos de aprendizado de máquina junto com os algoritmos de detecção de representação às mensagens de entrada para fornecer proteção de mercadorias e lança ataques de phishing. Todas as mensagens estão sujeitos a um conjunto abrangente de modelos de aprendizado de máquina treinados para detectar mensagens de phishing, um conjunto de algoritmos avançados usado para proteger contra ataques de representação de usuário e domínio diversos.
ms.openlocfilehash: c3e44a313bf9c823fbfda138fc5a10294993d509
ms.sourcegitcommit: c1c41744c2de89c9e172f817c8f73bb0ada81a58
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2019
ms.locfileid: "29792266"
---
# <a name="atp-anti-phishing-capabilities-in-office-365"></a>Recursos antiphishing ATP no Office 365

Antiphishing ATP é parte da [Proteção de ameaça avançadas do Office 365](office-365-atp.md). ATP antiphishing aplica um conjunto de modelos de aprendizado de máquina junto com os algoritmos de detecção de representação às mensagens de entrada para fornecer proteção de mercadorias e lança ataques de phishing. Todas as mensagens estão sujeitos a um conjunto abrangente de modelos de aprendizado de máquina treinados para detectar mensagens de phishing, um conjunto de algoritmos avançados usado para proteger contra ataques de representação de usuário e domínio diversos. ATP antiphishing protege a sua organização de acordo com a políticas que são definidas por seu Office 365 global ou administradores de segurança.
  
Para saber mais, consulte [Configurar políticas de AntiPhishing no Office 365](set-up-anti-phishing-policies.md).
  
> [!NOTE]
> ATP antiphishing só está disponível no Advanced proteção contra ameaças, que está incluído nas assinaturas, como [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 Enterprise E5, A5 de educação do Office 365, etc. Se sua organização tiver uma assinatura do Office 365 que não inclui ATP do Office 365, você pode adquirir potencialmente ATP como um complemento. Para obter mais informações, consulte [preços e planos de proteção de ameaça avançadas do Office 365](https://products.office.com/exchange/advance-threat-protection) e o [Office 365 avançadas Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).

## <a name="how-atp-anti-phishing-works"></a>Como funciona a ATP AntiPhishing

ATP antiphishing verifica as mensagens de entrada para que a mensagem pode ser phishing de indicadores. Sempre que um usuário é coberto por uma política de ATP (anexos seguros, links confiáveis ou antiphishing) a mensagem de entrada é avaliada por máquina vários modelos que analisar a mensagem para determinar se a política se aplica à mensagem e é a ação apropriada de aprendizagem obtido, com base na diretiva configurada.
  
ATP antiphishing permite que os administradores globais do Office 365 ou administradores de segurança definir políticas que oferecem proteção contra ataques de phishing que incluem a representação de usuários ou domínios. (ou ambos). Administradores globais do Office 365 ou administradores de segurança definem dentro da diretiva de qual usuário e os domínios deve ser protegida contra ataques de representação usando uma lista fixa de usuários ou domínios ou por meio de inteligência de dados de caixa de correio. Inteligência de dados de caixa de correio é uma compreensão avançada de hábitos de email do usuário e contatos pessoais. ATP aprende como cada usuário individual se comunica com outros usuários dentro e fora da organização e cria um mapa dessas relações. Este mapa permite ATP entender mais detalhes sobre como assegurar que as mensagens direita são identificadas como representação.
  
ATP antiphishing políticas podem ser aplicadas a um conjunto específico de pessoas ou grupos em sua organização, ou a um domínio inteiro ou todos os seus domínios personalizados. Para saber mais, consulte [Configurar políticas de AntiPhishing no Office 365](set-up-anti-phishing-policies.md).
  
## <a name="how-to-get-atp-anti-phishing"></a>Como obter ATP AntiPhishing

Recursos de AntiPhishing ATP fazem parte da [Proteção avançada de ameaça](office-365-atp.md); No entanto, a proteção antiphishing de ATP aplica quando antiphishing políticas são definidas. (Um exemplo é uma política de representação.) Consulte [Configurar políticas de AntiPhishing no Office 365](set-up-anti-phishing-policies.md).
  
## <a name="how-to-know-if-atp-anti-phishing-is-in-place"></a>Como saber se antiphishing ATP é in-loco

Políticas de AntiPhishing ATP devem ser definidas em ordem para proteção estejam em vigor. Verifique se essa opção primeiro para verificar a proteção está em vigor.

Além disso, os relatórios estão disponíveis para mostrar como o serviço está funcionando para sua organização. Para saber mais, consulte [Exibir relatórios de proteção de ameaça avançadas do Office 365](view-reports-for-atp.md).

Para a máquina de AntiPhishing ATP modelos para estar ativo para um usuário específico de aprendizagem, que o usuário deve fazer parte de uma diretiva de [Anexos de seguros ATP](atp-safe-attachments.md), [Links confiáveis de ATP](atp-safe-links.md)ou ATP antiphishing definida. 

A tabela a seguir descreve alguns cenários de exemplo. Em cada um desses exemplos, a empresa está usando o Office 365 Enterprise E5, que inclui a proteção avançada de ameaça.
  
|**Cenário de exemplo**|**ATP antiphishing se aplicam neste caso?**|
|:-----|:-----|
|Organização da PAT tem o Office 365 Enterprise E5, mas ninguém definiu quaisquer políticas para anexos seguros ATP, links confiáveis de ATP ou ATP avançadas phishing ainda.|Não. Embora o recurso esteja disponível, pelo menos uma política de ATP deve ser definida na ordem da máquina ATP modelos de aprendizado para trabalhar. Para representação também deve ser uma política de AntiPhishing ATP in-loco.|
|Lee é um funcionário no departamento de vendas na Contoso. Organização de Lee tem uma política de AntiPhishing ATP in-loco que se aplica aos funcionários de finance apenas.|Não. Nesse caso, ATP antiphishing (modelos de máquina e proteção de representação) aplicaria aos funcionários financeiro, mas outros funcionários, inclusive o departamento de vendas, não seriam.|
|Ontem, um administrador do Office 365 na organização de Jean configurar uma política de AntiPhishing ATP que se aplica a todos os funcionários. Anteriormente hoje, Jean recebeu uma mensagem de email que inclua uma representação coberta pela política.|Sim. Neste exemplo, Jean tem uma licença para proteção de ameaça avançadas, e uma política de AntiPhishing ATP que inclui Jean tiver sido definida. Normalmente, levará cerca de 30 minutos para uma nova política entrem em vigor em datacenters; desde que um dia passou nesse caso, a política deve estar em vigor.|

## <a name="related-topics"></a>Tópicos relacionados

[Proteção Avançada contra Ameaças do Office 365](office-365-atp.md) 
  
[Proteção antiphishing no Office 365](anti-phishing-protection.md)
  
[Configurar políticas de AntiPhishing no Office 365](set-up-anti-phishing-policies.md)
  
[Links de ATP seguros no Office 365](atp-safe-links.md)
  
[Configurar políticas de links seguros ATP no Office 365](set-up-atp-safe-links-policies.md)
  
[Anexos de ATP seguros no Office 365](atp-safe-attachments.md)
  
[Configurar políticas de anexos seguros ATP no Office 365](set-up-atp-safe-attachments-policies.md)
  
[Exibir relatórios de Proteção avançada contra ameaças](view-reports-for-atp.md)

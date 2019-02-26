---
title: Usar o Explorer no centro &amp; de conformidade de segurança
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/13/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 82ac9922-939c-41be-9c8a-7c75b0a4e27d
ms.collection:
- M365-security-compliance
description: Saiba mais sobre o Explorer (também chamado de Gerenciador de ameaças &amp; ) no centro de conformidade de segurança.
ms.openlocfilehash: 4a28626d0e643d7a7b96a34656e7678c71a86c66
ms.sourcegitcommit: 1c73c2f83703af0a30a5b0633db00d8e0e6b39b5
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/25/2019
ms.locfileid: "30241963"
---
# <a name="use-explorer-in-the-security-amp-compliance-center"></a>Usar o Explorer no centro &amp; de conformidade de segurança

Se sua organização tiver o [Office 365 Threat Intelligence](office-365-ti.md)e você tiver as permissões necessárias, você poderá usar o Explorer para identificar e analisar ameaças. Por exemplo, você pode identificar e excluir emails mal-intencionados que foram entregues ou confira o malware que foi detectado pelos recursos de segurança do Office 365. O Explorer (também chamado de Gerenciador de ameaças) é um relatório avançado próximo a tempo real no centro &amp; de conformidade de segurança.
  
![Vá para o Gerenciador \> de gerenciamento de ameaças](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)
  
Para usar o Explorer, no centro &amp; de conformidade de segurança, vá para **Gerenciador**de **Gerenciamento** \> de ameaças.

> [!IMPORTANT]
> A partir de fevereiro de 2019 e saindo dos próximos meses, o Office 365 Threat Intelligence está se tornando o Office 365 Advanced Threat Protection Plan 2, com recursos adicionais de proteção contra ameaças. Para saber mais, veja [planos e preços avançados de proteção contra ameaças do office 365](https://products.office.com/exchange/advance-threat-protection) e a [Descrição do serviço de proteção avançada contra ameaças do Office 365](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).
      
## <a name="explorer-overview"></a>Visão geral do Explorer

O Explorer exibe informações sobre o malware suspeito em emails e arquivos no Office 365, bem como outras ameaças de segurança e riscos à sua organização. Quando você abre o Explorer pela primeira vez, o modo de exibição padrão mostra as detecções de malware do antivírus nos últimos sete dias. O Explorer também pode mostrar recursos de proteção de segurança no Office 365, incluindo [links seguros](atp-safe-links.md) e [anexos seguros](atp-safe-attachments.md) e pode ser modificado para mostrar dados nos últimos 30 dias.
  
![Explorer mostra informações sobre os principais malware e usuários direcionados](media/8e8c1582-d6f4-4521-8591-686a1cb01f7e.png)
  
Use o menu Exibir para alterar as informações que são exibidas.
  
![O menu Exibir do Explorer](media/2bb34f58-555f-4967-ba55-740334ef1f8e.png)
  
O Explorer tem vários recursos de filtragem e consulta que permitem detalhar detalhes, como os principais usuários direcionados, famílias de malware principais e muito mais. Cada tipo de relatório oferece várias maneiras de exibir e explorar dados.

> [!IMPORTANT]
> Não use caracteres curinga, como um asterisco (*) ou um ponto de interrogação (?), com o Explorer. Quando você pesquisar o campo assunto de mensagens de email, o Explorer executará a correspondência parcial e produzirá resultados similares a uma pesquisa curinga.

## <a name="email--malware"></a>Malware \> de email

Este modo de exibição mostra mensagens de email identificadas como contendo malware.  

Exibir informações no gráfico por família de malware, domínio do remetente, IP do remetente, status de proteção (ações executadas por seus recursos e políticas de proteção contra ameaças no Office 365) e tecnologia de detecção (como o malware foi detectado).  

![Exibir dados sobre malware detectado](media/d11dc568-b091-4159-b261-df13d76b520b.png)         

Abaixo do gráfico, veja detalhes sobre as principais famílias de malware, principais usuários direcionados e mais detalhes sobre mensagens específicas. 

## <a name="email--phish"></a>Phishing \> de email

Este modo de exibição mostra mensagens de email identificadas como tentativas de phishing.  

Exibir informações por domínio do remetente, IP do remetente e status de proteção (ações executadas por seus recursos e políticas de proteção contra ameaças no Office 365). 

![Exibir dados sobre email identificados como tentativas de phishing](media/2e3f97fa-2b99-47f9-afd6-216d10633c50.png) 

Abaixo do gráfico, veja mais detalhes sobre mensagens específicas. 

## <a name="email--user-reported"></a>Emails \> relatados pelo usuário

Este modo de exibição mostra o email que os usuários relataram como lixo eletrônico, não lixo eletrônico ou email de phishing.  

Exibir informações por tipo de relatório (a determinação do usuário que o email era lixo eletrônico, não lixo eletrônico ou Phish) e por motivo de entrega (motivos pelos quais o email entrou em um local específico, como uma política de filtro de spam, uma regra de fluxo de emails, uma lista de remetentes bloqueados, uma lista de remetentes seguros, etc.).  

![Exibir dados sobre usuários de email relatados como lixo eletrônico, não lixo eletrônico ou phishing](media/255acd04-0d07-4b29-82af-5060a60c20ab.png)  

Abaixo do gráfico, veja mais detalhes sobre mensagens de email específicas, como a linha de assunto, o endereço IP do remetente, o usuário que informou a mensagem como lixo eletrônico, não lixo eletrônico ou Phish e muito mais. 

## <a name="email--all-mail"></a>Enviar \> todos os emails

Este modo de exibição mostra uma visão detalhada da atividade de email, incluindo emails identificados como mal-intencionados devido a phishing ou malware, bem como todos os emails não-mal-intencionados (emails, spam e emails em massa normais). 

> [!NOTE]
> Se você receber um erro que leia **muitos dados a serem exibidos**, adicione um filtro e, se necessário, restrinja o intervalo de datas que você está exibindo. 

Para aplicar um filtro, escolha **remetente**, selecione um item na lista e clique no botão atualizar. No nosso exemplo, usamos a **tecnologia de detecção** como um filtro (há várias opções disponíveis). Exibir informações por remetente, domínio do remetente, destinatários, assunto, nome do arquivo de anexo, família de malware, status de proteção (ações executadas por seus recursos e políticas de proteção contra ameaças no Office 365), tecnologia de detecção (como o malware foi detectado) e adicionais. 

![Exibir dados sobre o email detectado por tecnologia de detecção](media/0c032eb3-6021-4174-9f06-ff8f30c245ca.png) 

Abaixo do gráfico, veja mais detalhes sobre mensagens de email específicas, como linha de assunto, destinatário, remetente, status e assim por diante. 

## <a name="content--malware"></a>Malware \> de conteúdo

Este modo de exibição mostra arquivos que foram identificados como mal-intencionados no SharePoint Online, no OneDrive for Business e no Microsoft Teams.

Exibir informações pela família de malware, tecnologia de detecção (como o malware foi detectado) e carga de trabalho (OneDrive, SharePoint ou Teams). 

![Exibir dados sobre malware detectado](media/d11dc568-b091-4159-b261-df13d76b520b.png)  

Abaixo do gráfico, veja mais detalhes sobre arquivos específicos, como o nome do arquivo anexo, carga de trabalho, tamanho do arquivo, que modificou o arquivo e muito mais. 
  
## <a name="new-click-to-filter-capabilities"></a>(Novo!) Recursos de clique para filtrar

Novo no Explorer é a capacidade de clicar para filtrar. A partir do final de maio de 2018, quando você clica em um item na legenda, esse item se torna um filtro para o relatório. Por exemplo, vamos supor que estamos examinando o modo de exibição de malware no Explorer:
  
![Vá para o Gerenciador \> de gerenciamento de ameaças](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)
  
Clicar em **acionamento ATP** neste gráfico resultará em um modo de exibição como este: 
  
![Explorer filtrado para exibir somente os resultados do ATO acionamento](media/7241d7dd-27bc-467d-9db8-6e806c49df14.png)
  
Neste modo de exibição, agora estamos examinando dados para arquivos que foram destruídodos por [anexos seguros do Office 365 ATP](atp-safe-attachments.md). Abaixo do gráfico, podemos ver detalhes sobre mensagens de email específicas que tinham anexos detectados por anexos seguros de ATP.
  
![Detalhes específicos sobre mensagens de email com anexos detectados](media/c91fb05c-d1d4-4085-acc6-f7008a415c2a.png)
  
Selecionar um ou mais itens ativa o menu **ações** , que oferece várias opções de escolha para os itens selecionados. 
  
![Selecionar um item ativa o menu ações](media/95f127a4-1b2a-4a76-88b9-096e3ba27d1b.png)
  
A capacidade de filtrar em um clique e navegar para detalhes específicos pode poupar muito tempo na investigação de ameaças.
  
## <a name="how-do-i-get-explorer"></a>Como faço para obter o Explorer?

O Explorer está incluído no [Office 365 Threat Intelligence](office-365-ti.md). 

Você deve ter permissões apropriadas, como aquelas concedidas a um administrador de segurança ou leitor de segurança para exibir e usar o Explorer. Para saber mais, confira [permissões no centro de conformidade &amp; de segurança do Office 365](permissions-in-the-security-and-compliance-center.md).
  
## <a name="related-topics"></a>Tópicos relacionados

[Relatórios e insights no centro de conformidade de &amp; segurança do Office 365](reports-and-insights-in-security-and-compliance.md)
  
[Encontre e investigue emails mal-intencionados que foram entregues (inteligência de ameaças do Office 365)](investigate-malicious-email-that-was-delivered.md)
  
[Proteção antispam e antimalware do Office 365](anti-spam-and-anti-malware-protection.md)
  


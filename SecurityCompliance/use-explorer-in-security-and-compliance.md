---
title: Use o Explorer na segurança &amp; Centro de conformidade
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/20/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 82ac9922-939c-41be-9c8a-7c75b0a4e27d
description: Saiba mais sobre Explorer (também chamado de ameaça Explorer) na segurança &amp; Centro de conformidade.
ms.openlocfilehash: 51228101ba75eb2d51b2594db50f679ff107ed46
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524635"
---
# <a name="use-explorer-in-the-security-amp-compliance-center"></a>Use o Explorer na segurança &amp; Centro de conformidade

Se sua organização tem [Inteligência de ameaça do Office 365](office-365-ti.md)e você tem as [permissões no Centro de conformidade de segurança do Office 365 e](permissions-in-the-security-and-compliance-center.md)de necessárias, você pode usar o Explorer para identificar e analisar as ameaças. Por exemplo, você pode identificar e excluir email mal-intencionado que foi entregue ou consulte malware que foi detectada pelos recursos de segurança do Office 365. Explorer (também conhecido como ameaça Explorer) é uma poderosa perto de relatório em tempo real na segurança &amp; Centro de conformidade.
  
![Vá para gerenciamento de ameaça \> Explorer](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)
  
Para usar o Explorer, na segurança &amp; Centro de conformidade, vá para **gerenciamento de ameaça** \> **Explorer**.
      
## <a name="explorer-overview"></a>Visão geral do Explorer

Explorer exibe informações sobre suspeito malware em email e arquivos no Office 365, bem como outros ameaças de segurança e riscos à sua organização. Quando você abre o Explorer pela primeira vez, o modo de exibição padrão mostra detecções de malware do antivírus. Explorer também pode mostrar segurança recursos de proteção no Office 365, incluindo [Links seguros](atp-safe-links.md) e [Anexos seguros](atp-safe-attachments.md).
  
![Explorer mostra informações sobre malwares principais e usuários de destino](media/8e8c1582-d6f4-4521-8591-686a1cb01f7e.png)
  
Use o menu Exibir para alterar quais informações serão exibidas.
  
![No menu Exibir para o Explorer](media/2bb34f58-555f-4967-ba55-740334ef1f8e.png)
  
Explorer tem várias filtragem e consultas de recursos que permitem que você extrair para obter detalhes, como top destinadas aos usuários, malwares principais famílias e mais. Cada tipo de relatório oferece uma variedade de maneiras de exibir e explorar dados, conforme descrito na tabela a seguir.
  
|**Escolha esta opção**|**Para exibir estes dados**|
|:-----|:-----|
|**Email** \> **Malware** <br/> |Mensagens de email identificadas como contendo o malware.  <br/> Exibir informações no gráfico pela família de malware, domínio do remetente, IP do remetente, o status de proteção (ações realizadas por seus recursos de proteção de ameaça e diretivas no Office 365) e tecnologia de detecção (como o malware foi detectado).  <br/> ![Exibir dados sobre detecções de malware detectado](media/d11dc568-b091-4159-b261-df13d76b520b.png)           <br/> O gráfico abaixo, exibir detalhes sobre malwares principais famílias, superior direcionadas usuários e mais detalhes sobre mensagens específicas.  <br/> |
|**Email** \> **Phish** <br/> |Envie mensagens identificadas como tentativas de phishing.  <br/> Exibir informações de domínio do remetente, IP do remetente e o status de proteção (ações realizadas por seus recursos de proteção de ameaça e diretivas no Office 365).  <br/> ![Exibir dados sobre email identificado como tentativas de phishing](media/2e3f97fa-2b99-47f9-afd6-216d10633c50.png)           <br/> O gráfico abaixo, exiba mais detalhes sobre mensagens específicas.  <br/> |
|**Email** \> **Relatado pelo usuário** <br/> |Email que os usuários informados como lixo eletrônico, não lixo ou phishing de email.  <br/> Exibir informações por tipo de relatório (se o email foi lixo, não lixo ou phishing de determinação do usuário) e por motivo de entrega (motivos por que o email passou para um local específico, como uma política de filtro de spam, uma regra de fluxo de email, uma lista de remetentes bloqueados, uma lista de remetentes seguros, etc.).  <br/> ![Exibir dados sobre os usuários de email relatados como lixo eletrônico, não lixo ou phishing](media/255acd04-0d07-4b29-82af-5060a60c20ab.png)           <br/> O gráfico abaixo, exiba mais detalhes sobre mensagens de email específica, como linha de assunto, o endereço IP do remetente, o usuário que relatou a mensagem como lixo eletrônico, não lixo eletrônico, ou phishing e mais.  <br/> |
|**Email** \> **Todos os emails** <br/> |Um modo de exibição de todo o da atividade de email, incluindo email identificado como mal-intencionado devido ao phishing ou malware, como também todos os emails não mal-intencionados (email normal, spam e em massa email).  <br/> > [!NOTE]> Se você receber um erro que lê **demais quantidade de dados para exibir**, adicionar um filtro e, se necessário, restringir o intervalo de datas que você esteja visualizando. Para aplicar um filtro, escolha o **remetente**, selecione um item na lista e, em seguida, clique no botão Atualizar. No nosso exemplo, usamos a **tecnologia de detecção** como um filtro (há várias opções disponíveis).           Exibir informações por remetente, domínio do remetente, destinatários, assunto, nome de arquivo de anexo, família de malware, o status de proteção (ações realizadas por seus recursos de proteção de ameaça e diretivas no Office 365), a tecnologia de detecção (como o malware foi detectado), e mais.<br/> ![Exibir dados sobre o e-mail detectado por tecnologia de detecção](media/0c032eb3-6021-4174-9f06-ff8f30c245ca.png)           <br/> O gráfico abaixo, exiba mais detalhes sobre mensagens de email específica, como a linha de assunto, remetente, destinatário, status e assim por diante.  <br/> |
|**Conteúdo** \> **Malware** <br/> |Arquivos que foram identificados como sendo maliciosas no SharePoint Online, o OneDrive for Business e Teams da Microsoft.  <br/> Exibir informações por tecnologia de detecção família, malware (como o malware foi detectado) e a carga de trabalho (OneDrive, SharePoint ou equipes).  <br/> ![Exibir dados sobre detecções de malware detectado](media/d11dc568-b091-4159-b261-df13d76b520b.png)           <br/> O gráfico abaixo, exiba mais detalhes sobre arquivos específicos, como nome de arquivo de anexo, a carga de trabalho, tamanho do arquivo, que modificou por último o arquivo e muito mais.  <br/> |
  
## <a name="new-click-to-filter-capabilities"></a>(Novo)! Recursos de filtro de Click

Nova Explorer é a capacidade de clique para filtrar. Iniciando no tardia de 2018 maio, quando você clica em um item na legenda, que o item se torna um filtro para o relatório. Por exemplo, suponha que vemos o modo de exibição de Malware no Explorer:
  
![Vá para gerenciamento de ameaça \> Explorer](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)
  
Clicar em **ATP Detonation** nos resultados neste gráfico em uma exibição semelhante a esta: 
  
![Explorer filtrado para exibir somente os resultados do ATO Detonation](media/7241d7dd-27bc-467d-9db8-6e806c49df14.png)
  
Nesse modo de exibição, podemos agora está procurando dados para os arquivos que foram detonated pelo [Office 365 ATP seguros anexos](atp-safe-attachments.md). Abaixo do gráfico, podemos ver detalhes sobre mensagens de email específicos que tiveram anexos que foram detectados pelo ATP anexos de seguros.
  
![Detalhes específicos sobre mensagens de email com anexos detectados](media/c91fb05c-d1d4-4085-acc6-f7008a415c2a.png)
  
Selecionar um ou mais itens ativa o menu de **ações** , que oferece várias opções do qual escolher para os itens selecionados. 
  
![Selecionar um item ativa no menu Ações](media/95f127a4-1b2a-4a76-88b9-096e3ba27d1b.png)
  
A capacidade de filtrar um clique e navegue até detalhes específicos poderá poupá-lo muito tempo no investigando ameaças.
  
## <a name="how-do-i-get-explorer"></a>Como posso obter Explorer?

Explorer está incluída no [Office 365 Threat Intelligence](office-365-ti.md). Você deve ter apropriado [no Centro de conformidade de segurança do Office 365 e as permissões atribuídas](permissions-in-the-security-and-compliance-center.md), como administrador de segurança ou leitor de segurança, para exibir e usar o Explorer.
  
## <a name="related-topics"></a>Tópicos relacionados

[Relatórios e ideias de segurança do Office 365 &amp; Centro de conformidade](reports-and-insights-in-security-and-compliance.md)
  
[Localizar e investigar email mal-intencionado que foi entregue (Office 365 Threat Intelligence)](investigate-malicious-email-that-was-delivered.md)
  
[Proteção antispam e antimalware do Office 365](anti-spam-and-anti-malware-protection.md)
  


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
# <a name="create-a-dlp-policy-from-a-template"></a>Criar uma política de DLP a partir de um modelo

A maneira mais fácil e mais comuns para começar a políticas de DLP é usar um dos modelos incluídos no Office 365. Você pode usar um desses modelos encontram ou personalizar as regras para atender aos requisitos de conformidade específicos da sua organização.
  
O Office 365 inclui mais de 40 modelos prontos para uso que podem ajudar você a atender a uma grande variedade de necessidades comuns de regulamentação e de política de negócios. Por exemplo, existem modelos de política de DLP para:
  
- Ato Gramm-Leach-Bliley (GLBA)
    
- Padrão de Segurança de Dados da Indústria de cartões de Pagamento (PCI-DSS)
    
- Informações Pessoalmente Identificáveis nos Estados Unidos (U.S. PII)
    
- Ato do Seguro de Saúde (HIPAA) dos EUA
    
Você pode ajustar um modelo modificando uma das regras existentes ou adicionando novas. Por exemplo, você pode adicionar novos tipos de informações confidenciais a uma regra, modificar as contagens em uma regra para torná-la mais difícil ou mais fácil de disparar, permitir que as pessoas substituam as ações em uma regra fornecendo uma justificativa de negócios ou alterar para quem as notificações e os relatórios de incidentes são enviados. Um modelo de política de DLP é um ponto de partida flexível para muitos cenários de conformidade comuns.
  
Você também pode escolher o modelo Personalizado, que não tem nenhuma regra padrão, e configurar sua política de DLP do zero, para atender aos requisitos de conformidade específicos de sua organização.
  
## <a name="example-identify-sensitive-information-across-all-onedrive-for-business-sites-and-restrict-access-for-people-outside-your-organization"></a>Exemplo: Identificar informações confidenciais entre todos os OneDrive para sites corporativos e restringir o acesso de pessoas fora da sua organização

OneDrive para contas de negócios tornam mais fácil para as pessoas em sua organização colaborem e compartilhem documentos. Mas uma preocupação comuns para oficiais de conformidade é que informações confidenciais armazenadas em OneDrive para contas de negócios podem ser compartilhadas inadvertidamente com pessoas fora da sua organização. Uma política de DLP pode ajudar a atenuar esse risco.
  
Neste exemplo, você criará uma política de DLP que identifica os dados de PII EUA, que inclui os números de passaporte EUA, números do seguro Social e números de identificação de contribuinte Individual (ITIN). Você começará usando um modelo e, em seguida, você irá modificar o modelo para atender aos requisitos de conformidade da sua organização — especificamente, você vai:
  
- Adicionar alguns dos tipos de números de conta bancária information—U.S. confidenciais e números de licença de motorista US — para que a política de DLP protege ainda mais dos seus dados confidenciais.
    
- Verifique a política mais sensíveis, para que uma única ocorrência de informações confidenciais seja suficiente para restringir o acesso de usuários externos.
    
- Permitir que os usuários substituam as ações fornecendo uma justificativa comercial ou relatar um falso positivo. Dessa forma, sua política DLP não impedirá que pessoas realizarem seus trabalhos, desde que eles tenham um motivo comercial válido para o compartilhamento de informações confidenciais da organização.
    
### <a name="create-a-dlp-policy-from-a-template"></a>Criar uma política de DLP a partir de um modelo

1. Vá para [https://protection.office.com](https://protection.office.com).
    
2. Entrar no Office 365 usando sua conta do trabalho ou da escola. Agora você está de segurança do Office 365 &amp; Centro de conformidade.
    
3. Na segurança &amp; Centro de conformidade \> barra de navegação esquerda \> **prevenção de perda de dados** \> **política** \> **+ criar uma política**.
    
    ![Criar um botão de política](media/b1e48a08-92e2-47ca-abdc-4341694ddc7c.png)
  
4. Escolha o modelo de política DLP que protege os tipos de informações confidenciais que você precisa \> **próximo**.
    
    Neste exemplo, você vai selecionar **privacidade** \> **dados US pessoalmente identificáveis informações (PII)** porque ele já inclui a maioria dos tipos de informações confidenciais que você queira proteger — você adicionará algumas posteriormente. 
    
    Quando você seleciona um modelo, você pode ler a descrição da direita para saber o que protege os tipos de informações confidenciais o modelo.
    
    ![Página para escolher um modelo de política DLP](media/775266f6-ad87-4080-8d7c-97f2e7403b30.png)
  
5. Nomeie a diretiva \> **próximo**.
    
6. Para escolher os locais que você deseja que a política DLP para proteger, siga um destes procedimentos:
    
  - Escolha **todos os locais no Office 365** \> **próximo**.
    
  - Escolha **Deixe-me escolher locais específicos** \> **próximo**. Neste exemplo, escolha esta opção.
    
    Para incluir ou excluir um local inteiro como todos os emails do Exchange ou todas as contas de OneDrive, alterne o **Status** desse local ativada ou desativada. 
    
    Para incluir somente específico de sites do SharePoint ou OneDrive para contas de negócios, alternar o **Status** para e, em seguida, clique nos links em **incluir** escolha sites específicos ou contas. Quando você aplica uma política a um site, as regras configuradas nessa política são automaticamente aplicadas a todos os subsites desse site. 
    
    ![Opções para locais onde uma política DLP pode ser aplicada](media/ee50a61a-e867-4571-a150-3eec8d83650f.png)
  
    Neste exemplo, para proteger informações confidenciais armazenadas em todos os OneDrive para contas de negócios, desativar o **Status** para **email do Exchange** e **sites do SharePoint**e deixe o **Status** em contas do **OneDrive**.
    
7. Escolha **Configurações avançadas de uso** \> **próximo**.
    
8. Um modelo de política DLP contém predefinidas regras com condições e ações que detectam e agirá tipos específicos de informações confidenciais. Você pode editar, excluir, ou desativar qualquer uma das regras existentes ou adicionar novos. Quando terminar, clique em **Avançar**.
    
    ![Expandida de regras no modelo de diretiva de PII conosco](media/3bc9f1b6-f8ad-4334-863a-24448bb87687.png)
  
    Neste exemplo, o modelo de dados de PII dos EUA inclui duas regras predefinidas:
    
  - **Baixo volume de conteúdo detectada PII dos EUA** Esta regra procura por arquivos que contêm entre 1 e 10 ocorrências de cada um dos três tipos de informações confidenciais (EUA, SSN e ITIN números de passaporte), onde os arquivos são compartilhados com pessoas fora da organização. Se encontrado, a regra envia uma notificação de e-mail para o administrador de conjunto de sites primário, o proprietário do documento, e a pessoa que fez a última modificação do documento. 
    
  - **Alto volume de conteúdo detectada PII dos EUA** Esta regra procura por arquivos que contêm 10 ou mais ocorrências de cada uma dos mesmos três tipos de informações confidenciais, onde os arquivos são compartilhados com pessoas fora da organização. Se encontrado, essa ação também envia uma notificação de e-mail, mais ele restringe o acesso ao arquivo. Para conteúdo em um OneDrive for Business account, isso significa que as permissões do documento são restritas para todos, exceto o administrador do conjunto de sites primário, o proprietário do documento e a pessoa que modificou o documento por último. 
    
    Para atender aos requisitos específicos da sua organização, convém tornar as regras mais fácil de gatilho, para que uma única ocorrência de informações confidenciais seja suficiente para bloquear o acesso de usuários externos. Depois de verificar a essas regras, você compreende que não precisa de regras de contagem de baixa e alta — você precisa apenas uma única regra que bloqueia o acesso se qualquer ocorrência de informações confidenciais for encontrada.
    
    Para expandir a regra chamada **baixo volume de conteúdo detectada US PII** \> **Excluir regra**.
    
    ![Excluir botão regra](media/bc36f7d2-0fae-4af1-92e8-95ba51077b12.png)
  
9. Agora, neste exemplo, você precisa adicionar dois tipos de informações confidenciais (números de conta bancária dos Estados Unidos e números de licença de motorista EUA), permitir que os usuários substituam uma regra e altere a contagem para qualquer ocorrência. Você pode fazer tudo isso editando uma regra, portanto, selecione **alto volume de conteúdo detectada US PII** \> **Editar regra**.
    
    ![Editar botão regra](media/eaf54067-4945-4c98-8dd6-fb2c5d6de075.png)
  
10. Para adicionar um tipo de informação confidencial, na seção **condições** da \> **tipos de adicionar ou alterar**. Em seguida, em **Adicionar ou alterar tipos** \> escolha **Adicionar** \> selecione **O número de conta bancária dos Estados Unidos** e **O número de carteira de motorista US** \> **Add** \> **feito**.
    
    ![Opção para adicionar ou alterar tipos](media/c6c3ae86-f7db-40a8-a6e4-db11692024be.png)
  
    ![Adicionar ou alterar o painel de tipos](media/fdbb96af-b914-4a6c-a97b-bbd014689965.png)
  
11. Para alterar a contagem (o número de instâncias de informações confidenciais necessárias para acionar a regra), em **contagem de instância** \> , escolha o valor **mínimo** para cada tipo \> insira 1. A contagem mínima não pode estar vazia. A contagem máxima pode ficar em branco; um valor vazio **max** converter em **qualquer**.
    
    Quando terminar, a contagem de min para todos os tipos de informações confidenciais deve ser **1** e a contagem máxima deve ser **qualquer**. Em outras palavras, qualquer ocorrência desse tipo de informações confidenciais serão satisfaz essa condição.
    
    ![Contagens de instância para os tipos de informações confidenciais](media/5c6e08cb-59a9-4558-b54b-d899836d4737.png)
  
12. Para a personalização final, você não quer suas políticas de DLP para impedir que pessoas fazendo seu trabalho, quando tiverem uma justificativa comercial válido ou encontrar um falso positivo, portanto você deseja que a notificação de usuário para incluir opções para substituir a ação de bloqueio.
    
    Na seção **notificações de usuário** , você pode ver que notificações por email e dicas de política estiver ativadas por padrão para esta regra no modelo. 
    
    Na seção **usuário substitui** , você pode ver que são ativadas substituições de uma justificativa comercial, mas substituições a ser relatado falsos positivos não são. Escolha **Substituir a regra automaticamente se eles relatá-la como falso positivo**.
    
    ![Seção de notificações de usuário e a seção de substituições de usuário](media/62720e7a-a939-4c03-b414-67748f3d64a0.png)
  
13. Na parte superior do editor de regra, altere o nome dessa regra do padrão **alto volume de conteúdo detectada PII EUA** para **qualquer conteúdo detectado com US PII** porque agora é disparado por qualquer ocorrência de seus tipos de informações confidenciais. 
    
14. Na parte inferior do editor de regra \> **Salvar**.
    
15. Revise as condições e ações para essa regra \> **próximo**.
    
    À direita, observe o **Status** de alternar para a regra. Se você desativar uma política inteira, todas as regras contidas na política também estão desativadas. No entanto, aqui você pode desativar uma regra específica sem desativar toda a diretiva. Isso pode ser útil quando você precisar investigar uma regra que está gerando um grande número de falsos positivos. 
    
16. Na próxima página, ler e entender o seguinte e, em seguida, escolha se deseja ativar a regra ou teste-out primeiro \> **próximo**.
    
     Antes de criar suas políticas de DLP, você deve considerar distribuí-las gradualmente para avaliar o impacto e testar sua eficácia antes de você impô-las totalmente. Por exemplo, você não quer uma nova política DLP acidentalmente bloquear o acesso a milhares de documentos que pessoas precisam para realizar seus trabalhos. 
    
    Se você estiver criando políticas de DLP com um grande potencial impacto, é recomendável seguir nesta sequência:
    
17. Iniciar no modo de teste sem Dicas de Política e, em seguida, usar os relatórios de DLP para avaliar o impacto. Você pode usar relatórios de DLP para exibir o número, o local, o tipo e a gravidade das correspondências de política. Com base nos resultados, você pode ajustar as regras conforme necessário. No modo de teste, as políticas de DLP não afetarão a produtividade das pessoas que trabalham na sua organização. 
    
18. Mover para o modo de teste com Dicas de Política e notificações para que você possa começar a ensinar os usuários sobre suas políticas de conformidade e prepará-los para as regras que serão aplicadas. Nesse estágio, você também pode pedir aos usuários para relatar falsos positivos para que você possa refinar as regras.
    
19. Ative as políticas para que as regras são impostas, e o conteúdo do protegidos. Continue a monitorar os relatórios DLP e quaisquer relatórios de incidentes ou notificações para certificar-se de que os resultados são o que você pretende. 
    
    ![Opções para usar o modo de teste e ativar a política](media/49fafaac-c6cb-41de-99c4-c43c3e380c3a.png)
  
20. Verifique as configurações para esta política \> escolha **criar**.
    
Depois de criar e ativar uma política de DLP, ele é implantado em quaisquer fontes de conteúdo que inclui, como sites do SharePoint Online ou OneDrive para contas de negócios, onde a política começa automaticamente aplicando suas regras em que o conteúdo.
  
## <a name="view-the-status-of-a-dlp-policy"></a>Exibir o status de uma política de DLP

A qualquer momento, você pode exibir o status de suas políticas de DLP na página **política** na seção de **prevenção de perda de dados** de segurança &amp; Centro de conformidade. Aqui, você pode encontrar informações importantes, como se uma política foi habilitada ou desabilitou com êxito, ou se a diretiva está no modo de teste. 
  
Eis aqui os diferentes status e o que eles significam.
  
|**Status**|**Explicação**|
|:-----|:-----|
|**Ativando…** <br/> |A política está sendo implantada nas fontes de conteúdo incluídas. A política ainda não foi imposta para todas as fontes.  <br/> |
|**Testando, com notificações** <br/> |A política está no modo de teste. As ações em uma regra não são aplicadas, mas as correspondências de política são coletadas e podem ser visualizadas usando os relatórios de DLP. As notificações sobre correspondências de política são enviadas aos destinatários especificados.  <br/> |
|**Testando, sem notificações** <br/> |A política está no modo de teste. As ações em uma regra não são aplicadas, mas as correspondências de política são coletadas e podem ser visualizadas usando os relatórios de DLP. As notificações sobre correspondências de política não são enviadas aos destinatários especificados.  <br/> |
|**Ativado** <br/> |A política está ativa e imposta. A política foi implantada com êxito a todas as suas fontes de conteúdo.  <br/> |
|**Desativando...** <br/> |A política está sendo removida para as fontes de conteúdo incluídas. A política ainda pode estar ativa e imposta em algumas fontes. Desativando uma política pode levar até 45 minutos.  <br/> |
|**Desativada** <br/> |A política não está ativa e não foi imposta. As configurações da política (fontes, palavras-chave, duração, etc.) são salvas.  <br/> |
|**Excluindo...** <br/> |A política está sendo excluída. A política não está ativa e não foi imposta.  <br/> |
   
## <a name="turn-off-a-dlp-policy"></a>Desativar uma política de DLP

Você pode editar ou desativar uma política de DLP a qualquer momento. Desativar uma política desabilita todas as regras na política.
  
Para editar ou desativar uma política de DLP, na página **política** \> selecione a política \> **Editar política**.
  
![Editar botão de política](media/ce319e92-0519-44fe-9507-45a409eaefe4.png)
  
Além disso, você pode desativar cada regra individualmente editando a política e, em seguida, alternando desativa o **Status** da regra, conforme descrito acima. 
  
## <a name="more-information"></a>Mais informações

- [Visão geral das políticas de prevenção contra perda de dados](data-loss-prevention-policies.md)
    
- [Enviar notificações e mostrar dicas de política para políticas de DLP](use-notifications-and-policy-tips.md)
    
- [Criar uma política DLP para proteger documentos com FCI ou outras propriedades](protect-documents-that-have-fci-or-other-properties.md)
    
- [O que os modelos de política DLP incluem](what-the-dlp-policy-templates-include.md)
    
- [Inventário de tipos de informações confidenciais](what-the-sensitive-information-types-look-for.md)
    


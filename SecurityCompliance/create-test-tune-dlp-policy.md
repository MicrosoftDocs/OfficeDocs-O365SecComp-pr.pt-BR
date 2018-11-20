---
title: Criar, testar e ajustar uma política DLP
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: ''
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
ms.openlocfilehash: 1d4697811a5d8dd426fed80d3d60bcd2fbea6335
ms.sourcegitcommit: 42c7ad69f95fc4d2de13293b39cc44931b9f82e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/14/2018
ms.locfileid: "26522783"
---
# <a name="create-test-and-tune-a-dlp-policy"></a>Criar, testar e ajustar uma política DLP

**Autor principal** </br>
Paul Cunningham, MVP da Microsoft </br>
[365 prático](https://practical365.com/) </br>
[@Practical365](https://twitter.com/practical365)</br>
__________________________________________________

Prevenção de perda de dados é um recurso de conformidade do Office 365 foi projetado para ajudar sua organização a evitar a exposição intencional ou acidental de informações confidenciais partes indesejadas. DLP tem suas raízes no Exchange Server e o Exchange Online e também é aplicável no SharePoint Online e o OneDrive for Business.

DLP usa um mecanismo de análise de conteúdo para examinar o conteúdo das mensagens de email e arquivos, procurando por informações confidenciais, como números de cartão de crédito e informações de identificação pessoal (PII). Informações confidenciais devem geralmente não ser enviadas por email ou incluídas nos documentos, sem levar etapas adicionais, como criptografar a mensagem de email ou os arquivos. Usar DLP, você pode detectar informações confidenciais e agir como:

- Registrar o evento para fins de auditoria
- Exibirá um aviso ao usuário final que está enviando o email ou o arquivo de compartilhamento
- Bloquear ativamente o email ou o arquivo de compartilhamento de ocorrendo

Em alguns casos, os clientes descartar DLP porque elas não se ter o tipo de dados que precisa proteger consideram. Pressupõe-se que os dados confidenciais, como registros médicos ou informações financeiras, existem apenas para setores, como o plano de saúde ou para as empresas que executam as lojas online. Mas qualquer empresa pode lidar com informações confidenciais regularmente, mesmo se eles não percebem a ele. Uma planilha de nomes de funcionários e datas de nascimento são apenas como confidenciais, como uma planilha de nomes de clientes e detalhes de cartão de crédito. E este tipo de informação tende flutuar mais do que o esperado, à medida que os funcionários silenciosamente passar sobre suas tarefas de rotina, considerando a nothing da exportação de um arquivo CSV de um sistema e enviando por email a alguém. Você também pode ser surpreso com que frequência funcionários enviam emails contendo o cartão de crédito ou detalhes bancários sem considerar as consequências.

## <a name="how-sensitive-information-is-detected-by-dlp"></a>Como informações confidenciais são detectadas pelo DLP

Informações confidenciais são identificadas pela expressão regular (RegEx) correspondência de padrões, em combinação com outros indicadores, como a proximidade de determinadas palavras-chave para os padrões de correspondência. Um exemplo disso é números de cartão de crédito. Um número de cartão de crédito VISA tem 16 dígitos. No entanto, esses dígitos podem ser gravados em maneiras diferentes, como 1111-1111-1111-1111, 1111 1111 1111 1111 ou 1111111111111111.

Qualquer cadeia de caracteres com 16 dígitos não é necessariamente um número de cartão de crédito, pode ser um número de tíquete de um sistema de suporte técnico ou um número de série de um componente de hardware. Para informar a diferença entre um número de cartão de crédito e uma cadeia de caracteres de 16 dígitos inofensiva, um cálculo é realizada (soma de verificação) para confirmar que os números corresponderem a um padrão conhecido de várias marcas de cartão de crédito.

Além disso, a proximidade de palavras-chave, como "VISA" ou "AMEX", juntamente com a proximidade com valores de data que podem ser a data de expiração do cartão de crédito, também é considerada tomar uma decisão sobre se os dados são um número de cartão de crédito ou não.

Em outras palavras, DLP é geralmente inteligente para reconhecer a diferença entre esses dois textos em um email:

- "Pode você encomendar me um novo laptop. Use o número do meu VISA 1111-1111-1111-1111, expiração 11/22 e envie-me a data de entrega prevista quando você tiver."
- "Meu número de série de laptop é 2222-2222-2222-2222 e tiver sido adquirido no dia 11/2010. A propósito, é meu visa viagens aprovado ainda?"

Uma boa referência manter marcado pelo indicador é este [tópico sobre tipos de informações confidenciais](what-the-sensitive-information-types-look-for.md) que explica como cada tipo de informação é detectado.

## <a name="where-to-start-with-data-loss-prevention"></a>Onde começar a prevenção de perda de dados

Quando os riscos de vazamento de dados não são totalmente óbvios, é difícil calcular onde exatamente deve começar com a implementação de DLP. Felizmente, as políticas de DLP podem ser executadas em "modo de teste", permitindo que você medir sua eficiência e a precisão antes de ativá-los.

Políticas de DLP para Exchange Online podem ser gerenciadas por meio do Centro de administração do Exchange. Mas você pode configurar políticas DLP para todas as cargas de trabalho por meio do Centro de conformidade, & segurança, portanto, que é o que eu usarei para demonstrações neste artigo. No Centro de conformidade & segurança você encontrará as políticas DLP em **prevenção de perda de dados** > **política**. Clique em **criar uma política** para iniciar.

O Office 365 fornece uma variedade de [modelos de política DLP](what-the-dlp-policy-templates-include.md) , você pode usar para criar políticas DLP. Digamos que você tem uma empresa de australiana. Você pode filtrar os modelos de diretiva para exibir somente aqueles que são relevantes para a Austrália se encaixam nas categorias gerais de financeiro, médico e integridade e privacidade.

![Opção para escolher o país ou região](media/DLP-create-test-tune-choose-country.png)

Para esta demonstração devo escolher dados australiano pessoalmente identificáveis informações (PII), que inclui os tipos de informações de número de carteira de motorista e de número de arquivo de imposto australiano (TFN).

![Opção para escolher um modelo de política](media/DLP-create-test-tune-choose-policy-template.png)

Dê um nome de sua nova política de DLP. O nome padrão corresponderá ao modelo de política DLP, mas você deve escolher um nome mais descritivo de sua preferência, pois várias políticas podem ser criadas a partir do mesmo modelo.

![Opção nomear sua política](media/DLP-create-test-tune-name-policy.png)

Escolha os locais que a política será aplicada. Políticas de DLP podem aplicar o Exchange Online, SharePoint Online e OneDrive for Business. Vamos deixar essa diretiva configurada para aplicar a todos os locais.

![Opção escolher todos os locais](media/DLP-create-test-tune-choose-locations.png)

Em que a primeira etapa de **Configurações de diretiva** apenas aceite os padrões para agora. Há muito de personalização, que você pode fazer em políticas de DLP, mas os padrões são um ótimo lugar para começar.

![Opções para personalizar o tipo de conteúdo para proteger](media/DLP-create-test-tune-default-customization-settings.png)

Após clicar em **Avançar** será exibido com uma página de **Configurações de diretiva** adicional com mais opções de personalização. Para uma política que você está testando apenas, aqui é onde você pode iniciar fazer alguns ajustes.

- Posso ter desativado dicas de política para agora, que é uma etapa razoável a ser executada se você apenas estiver testando coisas check-out e não quiser exibir qualquer coisa ainda aos usuários. Dicas de política exibem avisos para os usuários que eles estão prestes a violar uma política DLP. Por exemplo, um usuário do Outlook verá um aviso de que o arquivo que eles tenham anexado contém os números de cartão de crédito e fará com que seus emails ser rejeitadas. O objetivo de dicas de política é parar o comportamento incompatíveis antes que elas ocorram.
- Eu também tiver reduzido o número de instâncias de 10 como 1, para que essa diretiva detectará qualquer compartilhamento de dados de PII australiano, não apenas dados em massa compartilhamento dos dados.
- Eu também adicionou outro destinatário para o email de relatório de incidente.

![Configurações de diretiva adicionais](media/DLP-create-test-tune-more-policy-settings.png)

Finalmente, posso configurou essa diretiva para ser executado no modo de teste inicialmente. Observe que também é uma opção para desabilitar dicas de política enquanto estiver no modo de teste. Isso proporciona a flexibilidade para ter habilitadas na política de dicas de política, mas, em seguida, decidir se deseja mostrar ou suprimi-las durante o teste.

![Opção para testar a diretiva pela primeira vez](media/DLP-create-test-tune-test-mode.png)

Na tela revisão final, clique em **criar** para concluir a criação da política.

## <a name="test-a-dlp-policy"></a>Testar uma política de DLP

Sua nova política de DLP começará entrem em vigor dentro de cerca de 1 hora. Você pode sit e aguarde até que ele seja disparado por atividade do usuário normal, ou você pode tentar acioná-lo. Anteriormente, eu vinculada neste [tópico sobre tipos de informações confidenciais](what-the-sensitive-information-types-look-for.md), que fornece informações sobre como acionar correspondências DLP.

Por exemplo, a política de DLP que eu criado para este artigo detectará números de arquivo de imposto australiano (TFN). De acordo com a documentação, a correspondência baseia-se nos seguintes critérios.

![Documentação sobre o número de imposto de renda Austrália](media/DLP-create-test-tune-Australia-Tax-File-Number-doc.png)
 
Para demonstrar a detecção de TFN de maneira franco em vez disso, um email com as palavras "Número de imposto de renda" e uma cadeia de caracteres de 9 dígitos perto serão tomar através sem quaisquer problemas. O motivo pelo qual que ele não dispara a política de DLP é que a cadeia de caracteres de dígitos 9 deve passar a soma de verificação que indica que é um TFN válido e não apenas uma cadeia de caracteres inofensiva de números.

![Número de imposto de renda Austrália que não passe soma de verificação](media/DLP-create-test-tune-email-test1.png)

Em comparação, um email com as palavras "Número de imposto de renda" e um TFN válido que passa a soma de verificação irá disparar a política. Para o registro, o TFN estou usando foi feito a partir de um site que gera válido, mas não original, TFNs. Há sites semelhantes que geram [números de cartão de crédito válido, mas falsa](http://www.fakecreditcardgenerator.net/). Esses sites estão muito útil porque um dos erros mais comuns ao testar uma política de DLP está usando um número falso que não é válida e não passa a soma de verificação (e, portanto, não aciona a política).

![Número de imposto de renda da Austrália que passa a soma de verificação](media/DLP-create-test-tune-email-test2.png)

O email de relatório de incidente inclui o tipo de informação confidencial detectado, quantas instâncias detectadas e o nível de confiança da detecção.

![Relatório de incidente mostrando o número de imposto de renda detectado](media/DLP-create-test-tune-email-incident-report.png)

Se você deixar sua política DLP no modo de teste e analisar os e-mails de relatório de incidente, você pode iniciar para ter uma ideia para a precisão da política de DLP e eficaz como será quando ele é imposto. Além dos relatórios de incidentes, você pode [usar os relatórios DLP](view-the-dlp-reports.md) para ver uma exibição agregada de correspondências de política entre seu locatário.

## <a name="tune-a-dlp-policy"></a>Ajustar a uma política de DLP

Talvez você queira fazer alguns ajustes como as políticas se comportam analisar atinge sua política. Como um exemplo simples, você pode determinar que um TFN em email não é um problema (acho que ainda é, mas vamos com ele para fins de demonstração), mas duas ou mais instâncias é um problema. Várias instâncias poderia ser um cenário riscado como um funcionário, enviando um e-mail para uma exportação CSV do banco de dados HR para um participante externo, por exemplo um serviço externo de contabilidade. Definitivamente algo preferir detectar e bloquear.

No Centro de conformidade & segurança, você pode editar uma política existente para ajustar o comportamento.

![Opção de Editar política](media/DLP-create-test-tune-edit-policy.png)
 
Você pode ajustar as configurações de local para que a política seja aplicada apenas para cargas de trabalho específicas ou para contas e sites específicos.

![Opções para escolher locais específicos](media/DLP-create-test-tune-edit-locations.png)

Você também pode ajustar as configurações de diretiva e editar as regras para atender melhor às suas necessidades.

![Opção de editar regra](media/DLP-create-test-tune-edit-rule.png)

Ao editar uma regra de uma política de DLP que você pode alterar:

- As condições, incluindo o tipo e o número de instâncias de dados confidenciais que acionarão a regra.
- As ações que serão executadas como restringir o acesso ao conteúdo.
- Notificações de usuário, que são as dicas de política que são exibidas ao usuário em seu navegador da web ou o cliente de email.
- Usuário substitui, que determina se os usuários podem escolher prosseguir com seu email ou qualquer forma de compartilhamento de arquivos.
- Relatórios de incidentes, para notificar os administradores.

![Opções para editar partes de uma regra](media/DLP-create-test-tune-editing-options.png)

Para esta demonstração adicionamos notificações de usuário à diretiva (cuidado de fazer isso sem treinamento do usuário adequado divulgação), e permitidos os usuários substituam a política com uma justificativa comercial ou sinalizando-la como falso positivo. Observe que você também pode personalizar o texto de dica de email e a diretiva se você quiser incluir informações adicionais sobre as diretivas da sua organização ou solicitar aos usuários a se tiverem dúvidas contate o suporte.

![Opções para notificações de usuário e substituições](media/DLP-create-test-tune-user-notifications.png)

A diretiva contém as duas regras para a manipulação de alto volume e volume baixo, por isso certifique-se de editar ambos com as ações que você deseja. Esta é uma oportunidade para tratar de casos de forma diferente dependendo de suas características. Por exemplo, você pode permitir substituições de violações de baixo volume, mas não permitir substituições de violações de alto volume.

![Uma regra para uma regra para baixo volume e de alto volume](media/DLP-create-test-tune-two-rules.png)

Além disso, se você deseja realmente bloquear ou restringir o acesso ao conteúdo que está em violação de política, você precisará configurar uma ação da regra de fazê-lo.

![Opção para restringir o acesso a conteúdo](media/DLP-create-test-tune-restrict-access-action.png)

Após salvar essas alterações nas configurações de diretiva, também preciso retornar à página principal de configurações para a política e habilitar a opção Mostrar dicas de política aos usuários enquanto a diretiva está no modo de teste. Essa é uma maneira eficaz para apresentar as políticas de DLP para seus usuários finais e faça o treinamento de reconhecimento de usuários, sem o risco de muitos falsos positivos que afetar sua produtividade.

![Opção para mostrar dicas de política no modo de teste](media/DLP-create-test-tune-show-policy-tips.png)

No servidor lado (nuvem lado ou se você preferir), a alteração talvez não entrem em vigor imediatamente, devido aos vários intervalos de processamento. Se você estiver fazendo uma alteração de política DLP que exibirá as novas dicas de política a um usuário, o usuário poderá não ver as alterações entrem em vigor imediatamente no seu cliente do Outlook, que verifica se há alterações na diretiva a cada 24 horas. Se você quiser acelerar um pouco para esse teste, você pode usar essa correção de registro para [Limpar o último carimbo de hora de download da chave PolicyNudges](https://support.microsoft.com/en-au/help/2823261/changes-to-a-data-loss-prevention-policy-don-t-take-effect-in-outlook?__hstc=18650278.46377037dc0a82baa8a30f0ef07a7b2f.1538687978676.1538693509953.1540315763430.3&__hssc=18650278.1.1540315763430&__hsfp=3446956451). Outlook baixará as informações mais recentes de política na próxima vez que você reiniciá-lo e começar a redigir uma mensagem de email.

Se você tiver habilitadas de dicas de política, o usuário terá início ver as dicas no Outlook e pode relatar falsos positivos para você quando eles ocorrerem.

![Dica de política com a opção para relatar como falso positivo](media/DLP-create-test-tune-policy-tip-in-outlook.png)

## <a name="investigate-false-positives"></a>Investigar falsos positivos

Modelos de política DLP não são perfeitos reta imediato. É provável que você encontrará alguns falsos positivos que ocorrem em seu ambiente, que é por isso que é tão importante facilitar a sua maneira em uma implantação de DLP, demorando para testar e ajustar suas políticas adequadamente.

Aqui está um exemplo de um falso positivo. Este email é bastante inofensiva. O usuário está fornecendo o seu número de telefone celular para alguém e incluindo sua assinatura de email.

![Email mostrando informações de positivas falsos](media/DLP-create-test-tune-false-positive-email.png)
 
Mas o usuário vê uma dica de política avisando que o email contém informações confidenciais, especificamente, o número de carteira de motorista um australiano.

![Opção para relatar como falso positivo na dica de política](media/DLP-create-test-tune-policy-tip-closeup.png)

O usuário pode relatar falso positivo, e o administrador pode examinar por que ele tenha ocorrido. No email relatório de incidente, o email é sinalizado como um falso positivo.

![Relatório de incidente mostrando de falsos positivos](media/DLP-create-test-tune-false-positive-incident-report.png)

Caso de licença de motorista, este é um bom exemplo para aprofundar. O motivo pelo qual este falso positivo ocorreu é que o "australiano carteira de motorista" tipo será acionado por qualquer cadeia de caracteres de dígitos 9 (até mesmo um que faz parte de uma cadeia de caracteres de 10 dígitos), dentro de proximidade de 300 caracteres às palavras-chave "Sidnei nsw" (não maiusculas de minúsculas). Isso é disparado por assinatura de número e email do telefone, só porque o usuário acontece estejam em Sidnei.

Curiosamente, se "Sidnei, NSW" possui uma vírgula, a política de DLP não é acionada. Não tenho ideia por que uma vírgula faz diferença aqui, nem por que outros estados na Austrália e cidades não estão incluídos nas palavras-chave para o tipo de informação de licença do driver australiano, mas há você ir. Portanto, o que podemos fazer sobre isso? Há duas opções.

Uma opção é remover o tipo de informação de licença do driver australiano da diretiva. É lá porque ela é parte do modelo de política de DLP, mas nós não serão forçados a usá-lo. Se você só está interessado em números de arquivo imposto e não a licenças do driver, você pode apenas removê-lo. Por exemplo, você pode removê-lo da regra de volume baixo na política, mas deixá-lo na regra de alto volume de modo que as listas de várias licenças de drivers ainda são detectadas.

![Opção para excluir o tipo de informações confidenciais da regra](media/DLP-create-test-tune-delete-low-volume-rule.png)
 
Outra opção é simplesmente aumentar a contagem da instância, para que um baixo volume de licenças do driver é detectado apenas quando há várias instâncias.

![Opção para editar a contagem de instância](media/DLP-create-test-tune-edit-instance-count.png)

Além de alterar a contagem de instância, você também pode ajustar a precisão de correspondência (ou nível de confiança). Se seu tipo de informação confidencial tiver vários padrões, você pode ajustar a precisão de correspondência em sua regra, para que a regra corresponda apenas padrões específicos. Por exemplo, para ajudar a reduzir os falsos positivos, você pode definir a precisão de correspondência da sua regra para que ele corresponda apenas o padrão com o nível mais alto de confiança. Noções básicas sobre como o nível de confiança é calculada é um pouco complicado (e além do escopo esta postagem), mas aqui está uma boa explicação sobre [como usar o nível de confiança para ajustar suas regras](https://docs.microsoft.com/en-us/office365/securitycompliance/data-loss-prevention-policies#match-accuracy).

Finalmente, se você deseja obter até mesmo um pouco mais avançada, você pode personalizar qualquer tipo de informação confidencial – por exemplo, você pode remover "Sidnei NSW" da lista de palavras-chave para [australiano carteira de motorista](https://docs.microsoft.com/en-us/office365/securitycompliance/what-the-sensitive-information-types-look-for#australia-drivers-license-number), para eliminar o falso positivo disparado acima. Para saber como fazer isso usando o XML e PowerShell, consulte este tópico sobre [como personalizar um tipo de informação confidencial internas](customize-a-built-in-sensitive-information-type.md).

## <a name="turn-off-a-dlp-policy"></a>Desativar uma política de DLP

Quando estiver satisfeito que sua política DLP é com precisão e efetivamente detectar tipos de informações confidenciais e que os usuários finais estão prontos para lidar com as políticas que está sendo in-loco, em seguida, você pode habilitar a diretiva.

![Opção para ativar política](media/DLP-create-test-tune-turn-on-policy.png)
 
Se você está aguardando para ver quando a política será entrem em vigor, [conectar-se a segurança do Office 365 & PowerShell do Centro de conformidade](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps) e execute o [cmdlet Get-DlpCompliancePolicy](https://docs.microsoft.com/en-us/powershell/module/exchange/policy-and-compliance-dlp/get-dlpcompliancepolicy?view=exchange-ps) para ver o DistributionStatus.

![A execução do cmdlet do PowerShell](media/DLP-create-test-tune-PowerShell.png)

Depois de ligar a política de DLP, você deve executar alguns testes finais sua própria política para certificar-se de que as ações de política esperada estão ocorrendo. Se você estiver tentando testar coisas como dados de cartão de crédito, há websites online com informações sobre como gerar o cartão de crédito de amostra ou outras informações pessoais que irá passar somas de verificação e acionam suas políticas.

Diretivas que permitem o usuário substituições apresentará essa opção para o usuário como parte da dica de política.

![Dica de política que permite a substituição do usuário](media/DLP-create-test-tune-override-option.png)

As diretivas que restringem o conteúdo serão apresentar o aviso ao usuário como parte da dica de política e impedi-los de enviar o email.

![Dica de política que o conteúdo é restrita](media/DLP-create-test-tune-restrict-warning.png)

## <a name="summary"></a>Resumo

Políticas de prevenção de perda de dados são úteis para organizações de todos os tipos. Testar algumas políticas de DLP é um exercício de baixo risco devido ao controle que você tem sobre coisas como dicas de política, substituições do usuário final e relatórios de incidentes. Silenciosamente, você pode testar algumas políticas de DLP para ver qual tipo de violações já estão ocorrendo em sua organização e, em seguida, políticas de comércio com baixa taxas positivas falsos, instruir os usuários sobre o que é permitido ou não permitido e suas políticas de DLP para distribuam, em seguida, o organização.

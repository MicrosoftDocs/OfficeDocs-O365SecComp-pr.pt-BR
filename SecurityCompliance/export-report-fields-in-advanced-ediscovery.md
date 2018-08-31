---
title: Exportar campos de relatórios na Descoberta Eletrônica Avançada do Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 840a5aff-ecd0-4e56-ad22-fe99bc143687
description: Descreve os campos que estão incluídos nos relatórios de exportação para eDiscovery avançado.
ms.openlocfilehash: a578523098248bcfa16ea8ba97d756d97ba060fa
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523742"
---
# <a name="export-report-fields-in-office-365-advanced-ediscovery"></a>Exportar campos de relatórios na Descoberta Eletrônica Avançada do Office 365

> [!NOTE]
> EDiscovery Avançado requer um Office 365 E3 com o complemento de conformidade avançadas ou uma assinatura E5 para sua organização. Se você não tiver que plano e quiser tentar eDiscovery avançado, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Este tópico descreve os campos de relatório de exportação de descoberta eletrônica avançado para o padrão e todos os modelos.
  
## <a name="export-report-fields"></a>Campos de exportação de relatório

A tabela a seguir lista os campos para cada modelo de exportação.
  
|**Nome do campo de exportação**|**Grupo**|**Descrição**|**Disponíveis no modelo padrão**|**Disponível em todos os modelos**|
|:-----|:-----|:-----|:-----|:-----|
|Núm_lin  <br/> |Geral  <br/> |Número da linha.  <br/> |Sim  <br/> |Sim  <br/> |
|File_ID  <br/> |Geral  <br/> |ID do arquivo.  <br/> |Sim  <br/> |Sim  <br/> |
|File_class  <br/> |Processamento  <br/> |Arquivo de classe.  <br/> |Sim  <br/> |Sim  <br/> |
|Family_ID  <br/> |Processamento  <br/> |Identificador numérico que é usado para agrupar arquivos (geralmente instância de email e seus respectivos anexos).  <br/> |Sim  <br/> |Sim  <br/> |
|For_review  <br/> |Processamento  <br/> |Sinalizador para indicar que o campo será incluído na exportação para revisão.  <br/> |Sim  <br/> |Sim  <br/> |
|Native_file_name  <br/> |Processamento  <br/> |Nome de arquivo nativo, sem fazer referência a pasta e a extensão.  <br/> |Sim  <br/> |Sim  <br/> |
|Responsáveis  <br/> |Geral  <br/> |Dos responsáveis do arquivo.  <br/> |Sim  <br/> |Sim  <br/> |
|Set_ID  <br/> |Analisar  <br/> |"Término definir" ou "Conjunto de Email" id.  <br/> |Sim  <br/> |Sim  <br/> |
|Inclusive_type  <br/> |Email  <br/> |Indica se o arquivo é inclusive, de acordo com os seguintes valores: 0 - não inclusive, 1 - 2 Inclusive, - Inclusive menos, 3 - cópia Inclusive.  <br/> |Sim  <br/> |Sim  <br/> |
|Marked_as_pivot  <br/> |Quase duplicatas  <br/> |Indica se o arquivo é uma tabela dinâmica.  <br/> |Sim  <br/> |Sim  <br/> |
|Similarity_percent  <br/> |Quase duplicatas  <br/> |Porcentagem de semelhança em relação a dinâmica.  <br/> |Sim  <br/> |Sim  <br/> |
|Duplicate_subset  <br/> |Quase duplicatas  <br/> |Identificador exclusivo do subconjunto de duplicados. Indica se o arquivo tem duplicatas texto exato.  <br/> |Sim  <br/> |Sim  <br/> |
|Data  <br/> |Geral  <br/> |Data do arquivo (depende do tipo de arquivo - email: Data enviada; documento: data de modificação).  <br/> |Sim  <br/> |Sim  <br/> |
|Dominant_theme  <br/> |Analisar  <br/> |Tema principal do arquivo.  <br/> |Sim  <br/> |Sim  <br/> |
|Themes_list  <br/> |Temas  <br/> |Lista de nomes de tema.  <br/> |Sim  <br/> |Sim  <br/> |
|ND_set  <br/> |EquiSet  <br/> |Identificador numérico exclusivo de um conjunto de Nearduplicate.  <br/> |Sim  <br/> |Sim  <br/> |
|Email_set  <br/> |Email  <br/> |Identificador numérico exclusivo de um conjunto de Email.  <br/> |Sim  <br/> |Sim  <br/> |
|Email_thread  <br/> |Email  <br/> |Descreve a posição do email dentro do E-mail definida Consists de todas as IDs de nó partindo da raiz para o e-mail atual, separado por pontos.  <br/> |Sim  <br/> |Sim  <br/> |
|Email_subject  <br/> |Email  <br/> |Assunto do email.  <br/> |Sim  <br/> |Sim  <br/> |
|Email_date_sent  <br/> |Email  <br/> |Data em que o email foi enviado.  <br/> |Sim  <br/> |Sim  <br/> |
|Email_participants  <br/> |Email  <br/> |Endereços de email de todos os participantes em um segmento de email, incluindo para vínculos ausentes.  <br/> |Sim  <br/> |Sim  <br/> |
|Email_participant_domains  <br/> |Email  <br/> |Domínios de todos os participantes em um segmento de email, incluindo o link ausente.  <br/> |Sim  <br/> |Sim  <br/> |
|Email_sender  <br/> |Email  <br/> |Nome do remetente de email e/ou endereço.  <br/> |Sim  <br/> |Sim  <br/> |
|Email_sender_domain  <br/> |Email  <br/> |Domínio do remetente de email.  <br/> |Sim  <br/> |Sim  <br/> |
|Email_to  <br/> |Email  <br/> |Para destinatário do email.  <br/> |Sim  <br/> |Sim  <br/> |
|Email_cc  <br/> |Email  <br/> |CC o destinatário do email.  <br/> |Sim  <br/> |Sim  <br/> |
|Email_bcc  <br/> |Email  <br/> |Destinatário Cco do email.  <br/> |Sim  <br/> |Sim  <br/> |
|Email_recipient_domains  <br/> |Email  <br/> |Destinatários do email domínios (para, CC e Cco).  <br/> |Sim  <br/> |Sim  <br/> |
|Email_date_received  <br/> |Email  <br/> |Data em que o email foi recebida.  <br/> |Sim  <br/> |Sim  <br/> |
|Email_action  <br/> |Email  <br/> |Valores: Acordo com o assunto de Email: "Avançar" (para "firmware:"), "Reply" (para "RE:") ou "Other" (outro assunto texto).  <br/> |Sim  <br/> |Sim  <br/> |
|Meeting_Start_Date/hora  <br/> ||A data e hora em que um item de reunião é iniciado.  <br/> |Sim  <br/> |Sim  <br/> |
|Meeting_End_Date/hora  <br/> ||A data e hora em que um item de reunião terminou.  <br/> |Sim  <br/> |Sim  <br/> |
|File_relevance_score  <br/> |Relevância  <br/> |Relevância pontuação (0 a 100). Por problema.  <br/> |Sim  <br/> |Sim  <br/> |
|Family_relevance_score  <br/> |Relevância  <br/> |Família max relevância pontuação (0 a 100). Por problema.  <br/> |Sim  <br/> |Sim  <br/> |
|Relevance_tag  <br/> |Relevância  <br/> |Marcação do arquivo, se o arquivo foi marcado manualmente na relevância. Por problema.  <br/> |Sim  <br/> |Sim  <br/> |
|Relevance_load_group  <br/> |Relevância  <br/> |Grupo de carga de relevância, do arquivo especificado, com um campo por um problema.  <br/> |Sim  <br/> |Sim  <br/> |
|Normalized_relevance_score  <br/> |Relevância  <br/> |Relevância normalizada pontuação (0 a 100), o que é comparável entre problemas e cargas.  <br/> |Sim  <br/> |Sim  <br/> |
|Marked_as_seed  <br/> |Relevância  <br/> |Marcação do arquivo, se ele foi definido para ser como um arquivo de propagação em relevância por/categoria do problema.  <br/> |Sim  <br/> |Sim  <br/> |
|Marked_as_pre-marcados  <br/> |Relevância  <br/> |Marcação do arquivo, caso este tenha sido definida como previamente marcado relevância por problema/categoria.  <br/> |Sim  <br/> |Sim  <br/> |
|Relevance_status_description  <br/> |Relevância  <br/> |Descrição do status relevância.  <br/> |Sim  <br/> |Sim  <br/> |
|Comentário  <br/> |Geral  <br/> |Comentário inserido pelo usuário.  <br/> |Sim  <br/> |Sim  <br/> |
|Export_input_path  <br/> |Processamento  <br/> |Caminho de entrada de exportação.  <br/> |Sim  <br/> |Sim  <br/> |
|Pivot_ID  <br/> |Quase duplicatas  <br/> |ID de Pivot do arquivo.  <br/> |Sim  <br/> |Sim  <br/> |
|Family_size  <br/> |Processamento  <br/> |Número de arquivos em uma família.  <br/> |Sim  <br/> |Sim  <br/> |
|Native_type  <br/> |Processamento  <br/> |Tipo de arquivo nativo. Por exemplo, planilha ou apresentação.  <br/> |Sim  <br/> |Sim  <br/> |
|Native_MD5  <br/> |Processamento  <br/> |Valor de hash MD5 do arquivo nativo.  <br/> |Sim  <br/> |Sim  <br/> |
|Native_size  <br/> |Processamento  <br/> |Tamanho de arquivo nativo.  <br/> |Sim  <br/> |Sim  <br/> |
|Native_extension  <br/> |Processamento  <br/> |Extensão de arquivo nativo.  <br/> |Sim  <br/> |Sim  <br/> |
|Doc_date_modified  <br/> |Propriedades do documento  <br/> |Data de modificação do arquivo nativo, tirado de metadados do arquivo.  <br/> |Sim  <br/> |Sim  <br/> |
|Doc_date_created  <br/> |Propriedades do documento  <br/> |Data nativo arquivo foi criado, obtido dos metadados do arquivo.  <br/> |Sim  <br/> |Sim  <br/> |
|Doc_modified_by  <br/> |Propriedades do documento  <br/> |Usuário que modificou o arquivo nativo, tirado de metadados do arquivo.  <br/> |Sim  <br/> |Sim  <br/> |
|O365_date_modified  <br/> |Propriedades do documento  <br/> |Arquivo nativo de data foi modificado, extraídos dos campos do SharePoint ou Exchange.  <br/> |Sim  <br/> |Sim  <br/> |
|O365_date_created  <br/> |Propriedades do documento  <br/> |Arquivo nativo de data foi criado, extraídos do SharePoint ou Exchange campos.  <br/> |Sim  <br/> |Sim  <br/> |
|O365_modified_by  <br/> |Propriedades do documento  <br/> |Último usuário que modificou o arquivo nativo, extraído do SharePoint ou Exchange campos.  <br/> |Sim  <br/> |Sim  <br/> |
|Compound_path  <br/> |Processamento  <br/> |Caminho de arquivo nativo incluindo sua origem composta.  <br/> |Sim  <br/> |Sim  <br/> |
|Input_path  <br/> |Processamento  <br/> |Caminho do arquivo de entrada.  <br/> |Sim  <br/> |Sim  <br/> |
|Input_date_modified  <br/> |Processamento  <br/> |Arquivo de entrada de data da última modificação.  <br/> |Sim  <br/> |Sim  <br/> |
|ND_ET_sort_excl_attach  <br/> |Analisar  <br/> |Defina concatenação de Email e término para revisão. Tinha ' é adicionado como um prefixo para conjuntos de término e 'E' é adicionado à ssets de Email.  <br/> |Sim  <br/> |Sim  <br/> |
|ND_ET_sort_incl_attach  <br/> |Analisar  <br/> |Definir concatenação de Email e término definido para revisão seria ' é adicionado como um prefixo para conjuntos de término e 'E' é adicionado aos conjuntos de Email. Além disso, cada email dentro de um Email_set é seguido por seus respectivos anexos de apropriado.  <br/> |Sim  <br/> |Sim  <br/> |
|Deduped_custodians  <br/> |Geral  <br/> |Responsáveis dos arquivos sua duplicação eliminados  <br/> |Sim  <br/> |Sim  <br/> |
|Deduped_file_IDs  <br/> |Geral  <br/> |IDs de arquivos sua duplicação eliminados  <br/> |Sim  <br/> |Sim  <br/> |
|Deduped_paths  <br/> |Geral  <br/> |Caminhos de arquivos sua duplicação eliminados  <br/> |Sim  <br/> |Sim  <br/> |
|File_key  <br/> |Geral  <br/> |Identificador interno para uso futuro.  <br/> |Sim  <br/> |Sim  <br/> |
|Export_native_path  <br/> |Processamento  <br/> |Caminho do arquivo nativo no pacote de exportação.  <br/> |Sim  <br/> |Sim  <br/> |
|Extracted_text_path  <br/> |Processamento  <br/> |Caminho do arquivo extraído.  <br/> |Sim  <br/> |Sim  <br/> |
|Process_batch  <br/> |Processamento  <br/> |Identificador de lote para o lote de importação.  <br/> |Sim  <br/> |Sim  <br/> |
|Process_status_ID  <br/> |Processamento  <br/> |Identificador que representa o status de estágio do processo.  <br/> |Sim  <br/> |Sim  <br/> |
|Process_status_description  <br/> |Processamento  <br/> |Descrição de status do estágio do processo: bem-sucedida ou a descrição do erro.  <br/> |Sim  <br/> |Sim  <br/> |
|Export_status_ID  <br/> |Processamento  <br/> |ID do status da exportação.  <br/> |Sim  <br/> |Sim  <br/> |
|Export_status_description  <br/> |Processamento  <br/> |Descrição do status exportação; bem-sucedida ou a descrição do erro.  <br/> |Sim  <br/> |Sim  <br/> |
|Read_percent  <br/> |Relevância  <br/> |% De leitura (0 a 100). Por problema.  <br/> |Sim  <br/> |Sim  <br/> |
|Doc_author  <br/> |Propriedades do documento  <br/> |Nas propriedades do documento: autor.  <br/> |Não  <br/> |Sim  <br/> |
|Doc_comments  <br/> |Propriedades do documento  <br/> |Nas propriedades do documento: comentários.  <br/> |Não  <br/> |Sim  <br/> |
|Doc_keywords  <br/> |Propriedades do documento  <br/> |Nas propriedades do documento: palavras-chave.  <br/> |Não  <br/> |Sim  <br/> |
|Doc_last_saved_by  <br/> |Propriedades do documento  <br/> |Nas propriedades do documento: salvo por último.  <br/> |Não  <br/> |Sim  <br/> |
|Doc_revision  <br/> |Propriedades do documento  <br/> |Nas propriedades do documento: número de revisão.  <br/> |Não  <br/> |Sim  <br/> |
|Doc_subject  <br/> |Propriedades do documento  <br/> |Nas propriedades do documento: assunto.  <br/> |Não  <br/> |Sim  <br/> |
|Doc_template  <br/> |Propriedades do documento  <br/> |Nas propriedades do documento: modelo.  <br/> |Não  <br/> |Sim  <br/> |
|Doc_title  <br/> |Propriedades do documento  <br/> |Nas propriedades do documento: título.  <br/> |Não  <br/> |Sim  <br/> |
|Email_has_attachment  <br/> |Email  <br/> |Indica se o email tem um ou mais anexos.  <br/> |Não  <br/> |Sim  <br/> |
|Email_importance  <br/> |Email  <br/> |Propriedade importance de email.  <br/> |Não  <br/> |Sim  <br/> |
|Email_level  <br/> |Email  <br/> |Indica a nível do email dentro do segmento de email. Anexos, o valor do email anexado.  <br/> |Não  <br/> |Sim  <br/> |
|Email_recipients  <br/> |Email  <br/> |Destinatários do email nome e/ou endereços (para, CC e Cco).  <br/> |Não  <br/> |Sim  <br/> |
|Email_security  <br/> |Email  <br/> |Propriedade de segurança de email.  <br/> |Não  <br/> |Sim  <br/> |
|Email_sensitivity  <br/> |Email  <br/> |Propriedade sensitivity de email.  <br/> |Não  <br/> |Sim  <br/> |
|Export_batch  <br/> |Processamento  <br/> |Último nome do lote de exportação do arquivo.  <br/> |Não  <br/> |Sim  <br/> |
|Export_session  <br/> |Processamento  <br/> |Última sessão de exportação do arquivo incluindo Id Data.  <br/> |Não  <br/> |Sim  <br/> |
|Extracted_text_length  <br/> |Processamento  <br/> |Comprimento de caracteres do arquivo de texto extraído.  <br/> |Não  <br/> |Sim  <br/> |
|Family_duplicate_set  <br/> |Processamento  <br/> |Identificador numérico para famílias duplicatas texto exato umas das outras (respectivamente - todos os membros das famílias sejam cópias exatas).  <br/> |Não  <br/> |Sim  <br/> |
|Has_Text  <br/> |Processamento  <br/> |Indica se há um texto no arquivo: 0 - nenhum; 1 - Sim.  <br/> |Não  <br/> |Sim  <br/> |
|Input_file_ID  <br/> |Processamento  <br/> |ID do arquivo de entrada do qual o arquivo foi extraído da.  <br/> |Não  <br/> |Sim  <br/> |
|Native_SHA_256  <br/> |Processamento  <br/> |Valor de hash SHA-256 do arquivo nativo.  <br/> |Não  <br/> |Sim  <br/> |
|O365_authors  <br/> |Propriedades do documento  <br/> |Usuários que modificou o arquivo nativo, extraído do SharePoint ou Exchange campos.  <br/> |Não  <br/> |Sim  <br/> |
|O365_created_by  <br/> |Propriedades do documento  <br/> |Usuário que criou o arquivo nativo, extraído do SharePoint ou Exchange campos.  <br/> |Não  <br/> |Sim  <br/> |
|Parent_node  <br/> |Email  <br/> |Se refere a um nó em um segmento de email para o nó pai mais próximo que não seja um link ausente.  <br/> |Não  <br/> |Sim  <br/> |
|Set_order_inclusives_first  <br/> |Email  <br/> |Emails e anexos: ordem cronológica de contador (Inclusives primeiro). Documentos: rotaciona primeiro e o restante por pontuação semelhança, em ordem decrescente.  <br/> |Não  <br/> |Sim  <br/> |
|Tagged_By  <br/> |Relevância  <br/> |Usuário que marcados o arquivo na relevância para o problema específico.  <br/> |Não  <br/> |Sim  <br/> |
|Word_count  <br/> |Analisar  <br/> |Número de palavras no documento.  <br/> |Não  <br/> |Sim  <br/> |
|||||||||||
||||||
||||||
   
## <a name="related-topics"></a>Tópicos relacionados

[Descoberta Eletrônica Avançada do Office 365](office-365-advanced-ediscovery.md)
  
[Exportando dados maiusculas com eDiscovery avançado](export-case-data-in-advanced-ediscovery.md)
  
[Exportar resultados](export-results-in-advanced-ediscovery.md)
  
[Exibir o histórico de lote e exportando resultados passado](view-batch-history-and-export-past-results.md)
  


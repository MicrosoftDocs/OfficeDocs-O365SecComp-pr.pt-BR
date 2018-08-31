---
title: Usar utilitários da Descoberta Eletrônica Avançada do Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 66ca9993-75f4-4724-aea2-5a0719b660c1
description: 'Saiba mais sobre os utilitários no eDiscovery avançadas do Office 365, incluindo o log de caso, limpar dados, processar erros, modifique a relevância e a transparência de análise.  '
ms.openlocfilehash: a68c98dd353971fcaa13fdc6b8e12bcf00c2faf0
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523538"
---
# <a name="use-office-365-advanced-ediscovery-utilities"></a>Usar utilitários da Descoberta Eletrônica Avançada do Office 365

> [!NOTE]
> EDiscovery Avançado requer um Office 365 E3 com o complemento de conformidade avançadas ou uma assinatura E5 para sua organização. Se você não tiver que plano e quiser tentar eDiscovery avançado, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Os utilitários que são exibidos e estão disponíveis no eDiscovery avançado dependem de funções de usuário e de contexto.
  
## <a name="case-log"></a>Log de caso

O log de caso fornece uma lista detalhada de atividades de processamento de aplicativo, que pode ser usado para acompanhamento, solução de problemas e para lidar com erros e avisos. O log pode ser gerado e armazenado localmente no servidor ou host ou enviado diretamente para um endereço de email.
  
O arquivo de log também pode ser baixado para o computador do cliente. A opção de download do cliente pode ser habilitada ou desabilitada acordo com a função de configuração e do usuário.
  
1. Na barra de menus, clique no ícone de **Cogwheel** . 
    
2. No **configurações e utilitários \> utilitários** guia, selecione **log caso \> instalação**.
    
3. Selecione o **nível de Log** da seguinte maneira: 
    
  - **Padrão**: inclui os dados de log basic. Essa opção é geralmente necessária para monitoramento e deve ser usada a menos que recomendado caso contrário.
    
  - **Mínimo**: usada para casos muito grandes e retorna apenas os dados mais recentes.
    
4. Clique em **Executar caso log**. O log é gerado e o caminho é exibido. As informações de andamento da tarefa atual e a última tarefa são exibidas no painel de status da tarefa.
    
## <a name="clear-data"></a>Limpar dados

Se for necessário excluir ou reinicializar dados casos, a instância do banco de dados deve ser inicializada. O utilitário de dados criptografado exclui especificadas todas as entradas do banco de dados de maiusculas, arquivos de texto, pasta maiusculas e resultados acumulados. A função só pode ser executada por um administrador.
  
> [!IMPORTANT]
> Essa ação não é reversível e limpará todas as marcas de relevância e análise executada pelo especialista. Salve um backup dos dados, se necessário. Use esta opção com muito cuidado. Excluindo arquivos marcados e classificados pode afetar os resultados de relevância. 
  
1. Na barra de menus, clique no ícone de **Cogwheel** . 
    
2. No **configurações e utilitários \> utilitários** guia, selecione **Limpar dados \> instalação**.
    
3. Selecione uma opção para obter as informações inicializar:
    
  - **Relevância**: exclui todo o trabalho feito na relevância, incluindo a definição de cargas e associação de arquivos para cargas. Ele exclui todos os exemplos e marcação.
    
  - **Perto duplicatas e segmentos de email**: exclui todas as informações de análise de perto duplicatas e segmentos de email.
    
  - **Temas**: exclui os dados relacionados à temas.
    
  - **Exportar histórico**: exclui informações de histórico de lotes de exportação.
    
4. Clique em **Limpar dados**. Os dados casos esteja desmarcados. As informações de andamento da tarefa atual e a última tarefa são exibidas no painel de **status da tarefa** . 
    
## <a name="modify-relevance"></a>Modificar a relevância

Esta seção descreve como ignorar ou reverter uma amostra de relevância.
  
1. Na barra de menus, clique no ícone de **Cogwheel** . 
    
2. No **configurações e utilitários \> utilitários** guia, selecione **Modificar relevância**.
    
3. Selecione uma das opções: 
    
  - **Amostra do atual Ignorar - para o usuário atual**: isso irá marcar, como **Ignorar**, todos os arquivos desmarcados na amostra de maiusculas open do usuário que executa o utilitário. Processamento de relevância não será executado nos arquivos marcados como **Ignorar**.
    
  - **Sample atual de ignorar - todas as abertas amostras**: isso irá marcar, como **Ignorar**, todos os arquivos desmarcados nas amostras abertos para todos os usuários. Essa opção não é recomendável se os usuários estão atualmente amostras de marcação.
    
  - **Reverter a última amostra**: O último concluído relevância amostra de treinamento será revertida, independentemente se ele está antes ou após o processo de "Calcular". Não é permitida a reversão de uma amostra os.
    
4. Clique em **Executar** para executar. 
    
## <a name="transparency-analysis"></a>Análise de transparência

O utilitário de análise de transparência permite uma exibição detalhada de arquivos e seus atribuídas pontuação de relevância. O relatório pode ser usado como uma verificação de integridade ou para comparar a relevância de um arquivo definido por um revisor humano em relação à relevância atribuído por eDiscovery avançado. 
  
Além da pontuação de relevância, o eDiscovery avançado calcula e atribui espessuras de palavra-chave que considerar o contexto de palavra-chave. A mesma palavra em um arquivo pode ser atribuída espessuras diferentes, dependendo do contexto e local. Cada palavra-chave é marcado usando uma escala de aumento de intensidade de cor desde amarelo para laranja escura e diversos tons de cinza. Codificação de cores é usada para indicar visualmente a palavra 's relativa positiva ou negativa contribuição para a pontuação de relevância. 
  
Em um cenário de problema de vários caso, um relatório de análise de transparência pode ser gerado para cada questão.
  
1. Na barra de menus, clique no ícone de **Cogwheel** . 
    
2. No **configurações e utilitários \> utilitários** guia, selecione **analysis transparência \> instalação**.
    
3. Em * * ID de arquivo * *, insira a ID de arquivo do arquivo para processar.
    
4. Na lista de **problema** , selecione o problema pertinente. 
    
5. Clique em **transparência de análise**. Após a conclusão, o relatório de análise de transparência para o arquivo é exibido, que mostra como as cores de palavra-chave marcadas correlacionam para a pontuação de relevância geral.
    
## <a name="see-also"></a>Confira também

[Descoberta Eletrônica Avançada do Office 365](office-365-advanced-ediscovery.md)
  
[Definindo configurações de maiusculas/minúsculas e locatário](define-case-and-tenant-settings-in-advanced-ediscovery.md)


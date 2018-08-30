---
title: Definir configurações de locatários e casos na Descoberta Eletrônica Avançada do Office 365
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
ms.assetid: 383809de-7f5e-4a1d-9098-c525f67b7a9a
description: 'Saiba mais sobre os rótulos, módulo cruzado e configurações de locatário que você pode definir no nível de maiusculas no eDiscovery avançadas do Office 365.  '
ms.openlocfilehash: 2230be8365e74ab21a0525bc2accc8469b22c9ed
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524716"
---
# <a name="define-case-and-tenant-settings-in-office-365-advanced-ediscovery"></a>Definir configurações de locatários e casos na Descoberta Eletrônica Avançada do Office 365

> [!NOTE]
> EDiscovery Avançado requer um Office 365 E3 com o complemento de conformidade avançadas ou uma assinatura E5 para sua organização. Se você não tiver que plano e quiser tentar eDiscovery avançado, você pode [inscrever-se para uma avaliação do Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
As configurações de maiusculas/minúsculas e locatário do eDiscovery avançado são descritas neste tópico.
  
## <a name="case-settings"></a>Configurações de maiusculas

Esta seção descreve as configurações que podem ser definidas no nível da caixa.
  
> [!NOTE]
> Se nenhum caso é selecionado no momento no eDiscovery avançada, na guia **configurações de ocorrência** está inativa. 
  
### <a name="cross-module"></a>Cruzar o módulo

O seguinte cruzado configurações do módulo é maiusculas opções que se aplicam a módulos de descoberta eletrônica avançado.
  
- Página padrão após o login: define a página padrão a ser exibido ao iniciar o eDiscovery avançado.
    
- Nome de exibição do arquivo: identificador de arquivo que será exibido em toda a descoberta eletrônica avançada para identificar o arquivo, como uma alternativa para o nome de exibição avançadas eDiscovery do assunto de email ou título/caminho do arquivo.
    
1. Abra **configurações e utilitários** , clicando no ícone **Cogwheel** . Open **configurações e utilitários \> caso configurações** guia \> **cruzar o módulo**. 
    
2. Selecione uma das opções **padrão de página após o logon** : 
    
  - **Última página do login anterior**
    
  - **Página ocorrências**
    
3. Clique em **Salvar**.
    
## <a name="tenant-settings"></a>Configurações de locatário

As configurações de locatário de descoberta eletrônica avançado são descritas nesta seção.
  
### <a name="user-administration"></a>Administração do usuário

As opções de administração do usuário são descritas em [Configurando usuários e casos](set-up-users-and-cases-in-advanced-ediscovery.md).
  
### <a name="event-log"></a>Log de eventos

O log de eventos fornece metadados relacionadas a eDiscovery avançado processando a qualquer momento durante a operação de descoberta eletrônica avançado. Por exemplo, ela inclui a hora de início dos processos de eDiscovery avançado principal (importar, analisar, relevância e exportação), bem como a hora de término e status. Esse log pode ser usado para rastreamento e atividades de processamento de dados de solução de problemas e para lidar com erros e avisos.
  
1. Abra **configurações e utilitários** , clicando no ícone **Cogwheel** . 
    
2. No **configurações e utilitários \> configurações de inquilinos** guia, selecione o **log de eventos**. Os dados de log de eventos são exibidos.
    
  - Para filtrar a saída de log por um caso, selecione o caso da lista de **casos** . 
    
  - Para classificar o log por colunas, clique em um cabeçalho de coluna. 
    
  - Para modificar a ordem das colunas, clique e arraste o cabeçalho da coluna.
    
  - Para mover entre as páginas de log, clique em **\>** e **\<** ícones. 
    
### <a name="system-information"></a>Informações do sistema

Informações do sistema de versão de descoberta eletrônica avançada e tarefas ativas são exibidas na guia Configurações de locatário.
  
1. Abra **configurações e utilitários** , clicando no ícone **Cogwheel** . 
    
2. No **configurações e utilitários \> configurações de inquilinos** guia, selecione **informações do sistema**. As informações de versão são exibidas.
    
A exibição pode ser atualizada clicando no ícone **Atualizar** abaixo da informação de locatário. 
  
## <a name="see-also"></a>Confira também

[Descoberta Eletrônica Avançada do Office 365](office-365-advanced-ediscovery.md)
  
[Usando os utilitários](use-advanced-ediscovery-utilities.md)


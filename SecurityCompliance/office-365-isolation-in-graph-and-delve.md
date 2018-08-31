---
title: Isolamento de Inquilino do Office 365 no escritório do gráfico e me aprofundar
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Resumo: Uma explicação dos isolamento de locatário o gráfico do Office e em Delve.'
ms.openlocfilehash: bdc0f34d558f25ec139861c9a91261a72418f18a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523893"
---
# <a name="tenant-isolation-in-the-office-graph-and-delve"></a>Isolamento de locatário no Office Graph e Delve

## <a name="tenant-isolation-in-the-office-graph"></a>Isolamento de locatário o gráfico do Office
A atividade de modelos de [Gráfico do Office](https://dev.office.com/officegraph) nos serviços do Office 365, incluindo o Exchange Online, SharePoint Online, Yammer, Skype para negócios, Azure Active Directory e mais algumas e em serviços externos, como outros serviços da Microsoft ou os serviços de terceiros. Componentes de gráfico do Office são usados em todo o Office 365. O gráfico Office representa uma coleção de conteúdo e a atividade e as relações entre eles que ocorrem com todo o pacote do Office. Ele usa técnicas de aprendizado de máquina sofisticada para conectar pessoas ao conteúdo relevante, conversas e pessoas ao redor deles. Por exemplo, o índice de Inquilino no SharePoint Online tem um índice de gráfico do Office que é usado para atender a consultas de Delve, o mecanismo de processamento de análise no SharePoint Online é usado para armazenar os sinais e calcular ideias e Exchange Online calcula a cada usuário cache de destinatários como entrada para análise de locatário.

O gráfico do Office contém informações sobre objetos da empresa, como pessoas e documentos, bem como as relações e interações entre esses objetos. As relações e interações são representadas como *bordas*. O gráfico Office segmentado por locatário, de forma que as bordas só podem existir entre os *nós* no mesmo aluguel. Um *nó* é uma entidade com um conjunto de facetas contendo *metadados* e bordas, tipo de nó, lista de controle de acesso e um identificador de recurso uniforme (URI). Cada nó possui associados metadados e bordas, organizadas em *facetas* como o modelo de dados de conhecimento comum. *Metadados* são denominadas propriedades armazenadas em um nó que pode ser usado para pesquisar, filtragem ou análise dentro do gráfico do office. Um *aspecto* é uma coleção lógica de metadados e bordas em um nó. Cada faceta descreve um aspecto de um nó. 

O gráfico do Office não colocar todos os dados em um único repositório; em vez disso, ele armazena metadados e relacionamentos de dados que estão em outros lugares. O gráfico Office consiste em vários repositórios de dados e componentes de processamento:
- O repositório de gráfico de locatário fornece armazenamento de massa otimizado para análise eficiente.
- O Cache de conteúdo ativo fornece rápido acesso aleatório ao nó ativo e bordas à unidade experiências do usuário.
- O roteador entrado notifica os componentes internos e externos das alterações no gráfico de locatário.

Análise dentro de cada carga de trabalho deduzir insights relevantes para os cálculos de todo o inquilino e fornecê-las no gráfico de locatário. Análise locatário motivos sobre todas as atividades em uma locação para produzir ideias em padrões de comportamento. Por exemplo, o Exchange Online calcula o cache de destinatário para cada usuário com o analytics com eficiência razão pela caixa de correio de cada usuário. Esses analytics por usuário produzir um conjunto de *Bordas RecipientCache* em cada pessoa, por sua vez, que são enviados para o gráfico de locatário. Isso mantém o como quantidade de processamento de análise mais próximo possível, os dados de origem.

## <a name="tenant-isolation-in-delve"></a>Isolamento de locatário em me aprofundar
Conforme mencionado anteriormente, o gráfico Office alimenta experiências que ajudam as pessoas a descobrir e colaborar em atividades atuais em sua empresa e fornece uma plataforma de centrados em entidade para análise a razão pela atividade e o conteúdo nas cargas de trabalho e Além do Office 365. Me aprofundar é o primeiro tal experiência possibilitada pelo gráfico do Office. Me aprofundar é uma experiência de web do Office 365 que reproduz o conteúdo do Office 365 e o Yammer Enterprise aos usuários do Office 365 via o gráfico do Office. A experiência da web exibe dados como quadros diferentes, cada um com um determinado tópico, como *# marcações de tendência ao redor me* ou *modificado por mim*. Cada placa consiste em vários cartões de documento que exibem o texto do resumo e uma imagem do documento. O cartão permite que os usuários façam coisas como abrir o documento ou uma página do Yammer para o documento. Não há uma página para cada pessoa em um locatário do Office 365 que exibe os documentos mais relevantes para essa pessoa e ícones que podem chamar o Exchange Online ou Skype for Business para interagir com essa pessoa. Como Delve é baseado na API de gráfico do Office, ele está vinculado pelo isolamento de locatário dessa API.
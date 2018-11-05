---
title: Criar um tipo de informação confidencial personalizado
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Priority
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Saiba como criar, modificar, remover e testar tipos de informações confidenciais personalizados para DLP na interface gráfica do usuário no Centro de Conformidade e Segurança do Office 365.
ms.openlocfilehash: cd7041ee9c20038fb7cb0c337f31d7cef7f7192d
ms.sourcegitcommit: ceb70ea863d8b97afea077a04fc7ec612b870695
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25857289"
---
# <a name="create-a-custom-sensitive-information-type"></a>Criar um tipo de informação confidencial personalizado

A Prevenção contra perda de dados (DLP) no Office 365 inclui vários [tipos de informações confidenciais](what-the-sensitive-information-types-look-for.md) que estão prontos para usar nas suas políticas DLP. Esses tipos internos podem ajudar a identificar e proteger números de cartão de crédito, números de contas bancárias, números de passaporte e muito mais. 

Porém, se você precisar identificar e proteger um tipo diferente de informação confidencial, como IDs de funcionário ou números de projeto que usam um formato específico para sua organização, será possível criar um tipo personalizado de informação confidencial.

As partes fundamentais de um tipo personalizado de informações confidenciais são:

- **Padrão principal**: números de ID de funcionário, números de projeto etc. Isso geralmente é identificado por uma expressão regular (RegEx), mas também pode ser uma lista de palavras-chave.

- **Evidências adicionais**: digamos que você esteja procurando por um número de ID de funcionário de nove dígitos. Nem todos os números de nove dígitos são números de ID de funcionário. Portanto, você pode pesquisar por texto adicional: palavras-chave como "funcionário", "crachá", "ID" ou outros padrões de texto com base em expressões regulares adicionais. Evidências de suporte (também chamadas de _suporte_ ou evidências _comprobatórias_) aumentam a probabilidade de que o número de nove dígitos no conteúdo seja realmente um número de ID de funcionário.

- **Caractere de proximidade**: faz sentido que quanto mais próximos o padrão principal e as evidências de suporte estejam entre si, mais provável seja que o conteúdo detectado seja o que você está procurando. Você pode especificar a distância de caracteres entre o padrão principal e as evidências de suporte (também conhecido como a _janela de proximidade_), conforme mostrado no seguinte diagrama:

    ![Diagrama da janela de proximidade e evidências comprobatórias](media/dc68e38e-dfa1-45b8-b204-89c8ba121f96.png)

- **Nível de confiança**: quanto mais evidências de suporte você tiver, maior será a probabilidade de que uma correspondência contenha as informações confidenciais que está procurando. Você pode atribuir níveis mais altos de confiança para correspondências detectadas usando mais evidências.

  Quando satisfeito, um padrão retorna uma contagem e um nível de confiança, que você pode usar nas condições de políticas DLP. Ao adicionar uma condição para detectar um tipo de informação confidencial a uma política DLP, você poderá editar o nível de confiança e a contagem, conforme mostrado no seguinte diagrama:

    ![Contagem de instâncias e opções de precisão de correspondência](media/11d0b51e-7c3f-4cc6-96d8-b29bcdae1aeb.png)

Para criar tipos de informações confidenciais personalizados no Centro de Conformidade e Segurança do Office 365, você tem as seguintes opções:

- **Usar a interface do usuário**: este método é mais fácil e rápido, mas você tem menos opções de configuração do PowerShell. O restante deste tópico descreve esses procedimentos.

- **Usar o PowerShell**: este método requer que você crie primeiro um arquivo XML (chamado de _pacote de regras_) que contém um ou mais tipos de informações confidenciais e use o PowerShell para importar o pacote de regras (a importação do pacote de regras é simples em comparação com a criação do pacote de regras). Esse método é muito mais complexo do que a interface do usuário, mas você tem mais opções de configuração. Para obter instruções, confira [Criar um tipo personalizado de informações confidenciais no PowerShell no Centro de Conformidade e Segurança do Office 365](create-a-custom-sensitive-information-type-in-scc-powershell.md).

As principais diferenças são descritas na seguinte tabela:

|Tipos de informações confidenciais personalizados na interface de usuário|Tipos de informações confidenciais personalizados no PowerShell|
|:-----|:-----|
|O Nome e a Descrição estão em um idioma|Dá suporte a vários idiomas para Nome e Descrição|
|Dá suporte a um padrão (o padrão principal).|Dá suporte a vários padrões além do padrão principal.|
|As evidências de suporte podem ser: <br/>• Expressões regulares <br/>• Palavras-chave <br/>• Dicionários de palavras-chave|As evidências de suporte podem ser: <br/>• Expressões regulares <br/>• Palavras-chave <br/>• Dicionários de palavras-chave <br/>• [Funções DLP internas](what-the-dlp-functions-look-for.md)|
|O nível de confiança é configurado para o tipo de informações confidenciais.|O nível de confiança é configurado para o tipo de informação confidencial e cada padrão individual.|
|O padrão de comparação requer a detecção do padrão principal e todas as evidências de suporte (o operador AND implícito é usado).|O padrão de comparação requer a detecção do padrão principal e uma quantidade de evidências de suporte configurável (podem ser usados os operadores AND e OR implícitos).|

## <a name="what-do-you-need-to-know-before-you-begin"></a>O que você precisa saber antes de começar?

- Para abrir o Centro de Conformidade e Segurança, confira [Acessar o Centro de Conformidade e Segurança do Office 365](go-to-the-securitycompliance-center.md).

- Tipos de informações confidenciais personalizados exigem familiaridade com expressões regulares (RegEx). Para saber mais sobre o mecanismo de RegEx do .NET usado para processar o texto, confira [Expressões Regulares do .NET](https://docs.microsoft.com/dotnet/standard/base-types/regular-expressions).

  O Suporte da Microsoft não pode ajudar no fornecimento de definições de correspondência de conteúdo personalizado (criação de classificações personalizadas ou padrões de expressões regulares). Os engenheiros de suporte podem fornecer suporte limitado para o recurso (por exemplo, fornecer padrões de expressões regulares de exemplo para fins de teste ou a assistência para solução de problemas de um padrão de expressão regular existente que não está sendo disparado conforme o esperado), mas não podem fornecer garantias de que qualquer desenvolvimento de correspondência de conteúdo personalizado atenderá a seus requisitos ou obrigações.

- Para saber mais sobre o mecanismo de RegEx do .NET que é usado para o processamento de texto, confira [Expressões regulares no .NET](https://docs.microsoft.com/dotnet/standard/base-types/regular-expressions).

- A DLP usa o rastreador de pesquisa para identificar e classificar informações confidenciais em sites do OneDrive e do SharePoint Online for Business. Para identificar o novo tipo personalizado de informações confidenciais no conteúdo existente, o conteúdo deve ser rastreado novamente. O conteúdo é rastreado novamente com base em uma agenda, mas você pode repetir manualmente o rastreamento do conteúdo de um conjunto de sites, uma lista ou uma biblioteca. Para saber mais, confira [Solicitar manualmente o rastreamento e a reindexação de um site, uma biblioteca ou uma lista](https://docs.microsoft.com/sharepoint/crawl-site-content).

## <a name="create-custom-sensitive-information-types-in-the-security--compliance-center"></a>Criar tipos de informações confidenciais personalizados no Centro de Conformidade e Segurança

No Centro de Conformidade e Segurança, acesse **Classificações** \> **Tipos de informações confidenciais** e clique em **Criar**.

As configurações são bastante óbvias e são explicadas na página associada do assistente:

- **Nome**

- **Descrição**

- **Proximidade**

- **Nível de confiança**

- **Elemento de padrão principal** (palavras-chave, expressão regular ou dicionário)

- **Elementos de padrão de suporte** opcionais (palavras-chave, expressão regular ou dicionário) e um valor de **Custo mínimo** correspondente.

Aqui está um cenário: você deseja um tipo personalizado de informação confidencial que detecte os números de funcionários com nove dígitos no conteúdo, juntamente com as palavras-chave "funcionário", "ID" e "crachá". Para criar esse tipo personalizado de informação confidencial, faça o seguinte:

1. No Centro de Conformidade e Segurança, acesse **Classificações** \> **Tipos de informações confidenciais** e clique em **Criar**.

2. Na página **Escolher um nome e uma descrição** que é aberta, insira os seguintes valores:

  - **Nome**: ID de funcionário.

  - **Descrição** detectar os números de nove dígitos de ID de funcionário da Contoso.

  Quando terminar, clique em **Avançar**.

3. Na página **Requisitos para correspondência** que é aberta, clique em **Adicionar um elemento** e defina as seguintes configurações:

  - **Detectar conteúdo que tenha**:
 
    a. Clique em **Qualquer um destes elementos** e selecione **Expressão regular**.

    b. Na caixa de expressão regular, insira `(\s)(\d{9})(\s)` (números de nove dígitos delimitados por espaço em branco)
  
  - **Elementos de suporte**: clique em **Adicionar elementos de suporte** e selecione **Contém esta lista de palavras-chave**.

  - Na área **Contém esta lista de palavra-chave** que é exibida, defina as seguintes configurações:

    - **Lista de palavra-chave**: insira o seguinte valor: funcionário,ID,crachá.

    - **Contagem mínima**: mantenha o valor padrão 1.

  - Mantenha o valor padrão de 60 para o **Nível de confiança**. 

  - Mantenha o valor padrão de 300 para a **Proximidade de caracteres**.

  Quando terminar, clique em **Avançar**.

4. Na página **Examinar e finalizar** que é aberta, examine as configurações e clique em **Concluir**.

5. A próxima página incentiva você a testar o novo tipo personalizado de informação confidencial. Para saber mais, confira [Testar tipos de informações confidenciais personalizados no Centro de Conformidade e Segurança](#test-custom-sensitive-information-types-in-the-security--compliance-center). Caso contrário, clique em **Cancelar**.

### <a name="how-do-you-know-this-worked"></a>Como saber se funcionou?

Para confirmar que você criou um novo tipo de informação confidencial com êxito, execute uma destas etapas:

  - Vá para **Classificações** \> **Tipos de informações confidenciais** e verifique se o novo tipo personalizado de informações confidenciais está listado.

  - Teste o novo tipo personalizado de informação confidencial. Para saber mais, confira [Testar tipos de informações confidenciais personalizados no Centro de Conformidade e Segurança](#test-custom-sensitive-information-types-in-the-security--compliance-center).

## <a name="modify-custom-sensitive-information-types-in-the-security--compliance-center"></a>Modificar tipos de informações confidenciais personalizados no Centro de Conformidade e Segurança

**Observação**: você só pode modificar tipos de informações confidenciais personalizados. Não é possível modificar tipos internos de informações confidenciais. Porém, você pode usar o PowerShell para exportar tipos de informações confidenciais personalizados internos, personalizá-los e importá-los como tipos de informações confidenciais personalizados. Para saber mais, confira [Personalizar um tipo de informação confidencial interno](customize-a-built-in-sensitive-information-type.md).

No Centro de Conformidade e Segurança, acesse **Classificações** \> **Tipos de informações confidenciais** e selecione os tipos de informações confidenciais personalizados que você deseja modificar.

Aqui estão disponíveis as mesmas opções oferecidas quando você criou o tipo de informação confidencial personalizado no Centro de Conformidade e Segurança. Para saber mais, confira [Criar tipos de informações confidenciais personalizados no Centro de Conformidade e Segurança](#create-custom-sensitive-information-types-in-the-security--compliance-center).

### <a name="how-do-you-know-this-worked"></a>Como saber se funcionou?

Para confirmar que você modificou um tipo de informação confidencial com êxito, execute uma destas etapas:

  - Vá para **classificações** \> **Tipos de informações confidenciais** para verificar as propriedades do tipo personalizado de informação confidencial modificado.

  - Teste o tipo personalizado de informação confidencial modificada. Para saber mais, confira [Testar tipos de informações confidenciais personalizados no Centro de Conformidade e Segurança](#test-custom-sensitive-information-types-in-the-security--compliance-center).

## <a name="remove-custom-sensitive-information-types-in-the-security--compliance-center"></a>Remover tipos de informações confidenciais personalizados no Centro de Conformidade e Segurança 

**Observações**:

- Você só pode remover tipos de informações confidenciais personalizados. Não é possível remover tipos internos de informações confidenciais.

- Antes de remover um tipo personalizado de informação confidencial, verifique se nenhuma política de DLP ou regras de fluxo de emails do Exchange (também conhecidas como regras de transporte) ainda fazem referência ao tipo de informação confidencial.

1. No Centro de Conformidade e Segurança, acesse **Classificações** \> **Tipos de informações confidenciais** e selecione um ou mais tipos de informações confidenciais personalizados que você deseja remover.

2. No submenu que é aberto, clique em **Excluir** (ou **Excluir tipos de informações confidenciais** se você tiver selecionado mais de um).

3. Na mensagem de aviso exibida, clique em **Sim**.

### <a name="how-do-you-know-this-worked"></a>Como saber se funcionou?

Para verificar se você removeu um tipo personalizado de informação confidencial com êxito, vá até **Classificações** \> **Tipos de informações confidenciais** para verificar se o tipo personalizado de informação confidencial não está mais presente.


## <a name="test-custom-sensitive-information-types-in-the-security--compliance-center"></a>Teste tipos de informações confidenciais personalizados no Centro de Conformidade e Segurança

1. No Centro de Conformidade e Segurança, acesse **Classificações** \> **Tipos de informações confidenciais**.

2. Selecione um ou mais tipos de informações confidenciais personalizados para testar. No submenu suspenso que é aberto, clique em **Testar tipo** (ou **Testar tipos de informações confidenciais** se você tiver selecionado mais de um).

3. Na página aberta, carregue um documento para testar, arrastando e soltando um arquivo ou clicando em **Procurar** e selecionando um arquivo.

4. Clique no botão **Testar** para testar o documento em busca de correspondências de padrão no arquivo.

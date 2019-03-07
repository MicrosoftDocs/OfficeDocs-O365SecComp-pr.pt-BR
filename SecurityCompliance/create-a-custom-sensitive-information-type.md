---
title: Criar um tipo de informação confidencial personalizado
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Saiba como criar, modificar, remover e testar tipos de informações confidenciais personalizados para DLP na interface gráfica do usuário no Centro de Conformidade e Segurança do Office 365.
ms.openlocfilehash: 5e20fac290a7d06c843a0043d95669d9c7f7cd05
ms.sourcegitcommit: 6aa82374eef09d2c1921f93bda3eabeeb28aadeb
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2019
ms.locfileid: "30455133"
---
# <a name="create-a-custom-sensitive-information-type"></a>Criar um tipo de informação confidencial personalizado

A Prevenção contra perda de dados (DLP) no Office 365 inclui vários [tipos de informações confidenciais](what-the-sensitive-information-types-look-for.md) que estão prontos para uso nas suas políticas DLP. Esses tipos internos podem ajudar a identificar e proteger números de cartão de crédito, números de contas bancárias, números de passaporte e muito mais. 

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

|**Tipos de informações confidenciais personalizados na interface de usuário**|**Tipos de informações confidenciais personalizados no PowerShell**|
|:-----|:-----|
|O Nome e a Descrição estão em um idioma.|Dá suporte a vários idiomas para Nome e Descrição.|
|Compatível com um padrão.|Compatível com vários padrões.|
|As evidências de suporte podem ser: <br/>• Expressões regulares <br/>• Palavras-chave <br/>• Dicionários de palavras-chave|As evidências de suporte podem ser: <br/>• Expressões regulares <br/>• Palavras-chave <br/>• Dicionários de palavras-chave <br/>• [Funções DLP internas](what-the-dlp-functions-look-for.md)|
|Os tipos de informações confidenciais personalizados são adicionados ao pacote de regras chamado Microsoft.SCCManaged.CustomRulePack|Você pode criar até 10 pacotes de regras com tipos de informações confidenciais personalizados.|
|O padrão de comparação requer a detecção do padrão principal e todas as evidências de suporte (o operador AND implícito é usado).|O padrão de comparação requer a detecção do padrão principal e uma quantidade de evidências de suporte configurável (podem ser usados os operadores AND e OR implícitos).|

## <a name="what-do-you-need-to-know-before-you-begin"></a>O que você precisa saber antes de começar?

- Para abrir o Centro de Conformidade e Segurança, confira [Acessar o Centro de Conformidade e Segurança do Office 365](go-to-the-securitycompliance-center.md).

- Os tipos de informações confidenciais personalizados exigem familiaridade com expressões regulares (RegEx). Para saber mais sobre o mecanismo de RegEx (anteriormente conhecido como RegEx++) usado para processar o texto, confira [Boost.RegEx 5.1.3](https://www.boost.org/doc/libs/1_68_0/libs/regex/doc/html/).

  O Suporte da Microsoft não pode ajudar no fornecimento de definições de correspondência de conteúdo personalizado (criação de classificações personalizadas ou padrões de expressões regulares). Os engenheiros de suporte podem fornecer suporte limitado para o recurso (por exemplo, fornecer padrões de expressões regulares de exemplo para fins de teste ou a assistência para solução de problemas de um padrão de expressão regular existente que não está sendo disparado conforme o esperado), mas não podem fornecer garantias de que qualquer desenvolvimento de correspondência de conteúdo personalizado atenderá a seus requisitos ou obrigações.

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

    ![Local dos tipos de informações confidenciais e botão Criar](media/scc-cust-sens-info-type-new.png)

2. Na página **Escolher um nome e uma descrição** que é aberta, insira os seguintes valores:

  - **Nome**: ID de funcionário.

  - **Descrição** detectar os números de nove dígitos de ID de funcionário da Contoso.

    ![Página de nome e descrição](media/scc-cust-sens-info-type-new-name-desc.png)

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

    ![Requisitos para a página correspondente](media/scc-cust-sens-info-type-new-reqs.png)

    Quando terminar, clique em **Avançar**.

4. Na página **Examinar e finalizar** que é aberta, examine as configurações e clique em **Concluir**.

    ![Examine e finalizar a página](media/scc-cust-sens-info-type-new-review.png)

5. A próxima página incentiva você a testar o novo tipo personalizado de informação confidencial clicando em **Sim**. Para saber mais, confira [Tipos de informações confidenciais personalizados no Centro de Conformidade e Segurança](#test-custom-sensitive-information-types-in-the-security--compliance-center). Para testar a regra mais tarde, clique em **Não**.

    ![Página de recomendações de teste](media/scc-cust-sens-info-type-new-test.png)

### <a name="how-do-you-know-this-worked"></a>Como saber se funcionou?

Para confirmar que você criou um novo tipo de informação confidencial com êxito, execute uma destas etapas:

  - Vá para **Classificações** \> **Tipos de informações confidenciais** e verifique se o novo tipo personalizado de informações confidenciais está listado.

  - Teste o novo tipo personalizado de informação confidencial. Para saber mais, confira [Testar tipos de informações confidenciais personalizados no Centro de Conformidade e Segurança](#test-custom-sensitive-information-types-in-the-security--compliance-center).

## <a name="modify-custom-sensitive-information-types-in-the-security--compliance-center"></a>Modificar tipos de informações confidenciais personalizados no Centro de Conformidade e Segurança

**Observações**:

- Você só pode modificar tipos de informações confidenciais personalizados. Não é possível modificar tipos internos de informações confidenciais. Porém, você pode usar o PowerShell para exportar tipos de informações confidenciais personalizados internos, personalizá-los e importá-los como tipos de informações confidenciais personalizados. Para saber mais, confira [Personalizar um tipo de informação confidencial interno](customize-a-built-in-sensitive-information-type.md).

- Somente você pode modificar os tipos de informações confidenciais personalizados que criou na interface do usuário. Se você tiver usado o [procedimento do PowerShell](create-a-custom-sensitive-information-type-in-scc-powershell.md) para importar um pacote de regras de tipo personalizado de informações confidenciais, você receberá um erro.

No Centro de Conformidade e Segurança, acesse **Classificações** \> **Tipos de informações confidenciais**, selecione os tipos de informações confidenciais personalizados que você deseja modificar e clique em **Editar**.

  ![Local dos tipos de informações confidenciais e botão Editar](media/scc-cust-sens-info-type-edit.png)

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

    ![Local dos tipos de informações confidenciais e botão Excluir](media/scc-cust-sens-info-type-delete.png)

3. Na mensagem de aviso exibida, clique em **Sim**.

### <a name="how-do-you-know-this-worked"></a>Como saber se funcionou?

Para verificar se você removeu um tipo personalizado de informação confidencial com êxito, vá até **Classificações** \> **Tipos de informações confidenciais** para verificar se o tipo personalizado de informação confidencial não está mais presente.

## <a name="test-custom-sensitive-information-types-in-the-security--compliance-center"></a>Teste tipos de informações confidenciais personalizados no Centro de Conformidade e Segurança

1. No Centro de Conformidade e Segurança, acesse **Classificações** \> **Tipos de informações confidenciais**.

2. Selecione um ou mais tipos de informações confidenciais personalizados para testar. No submenu suspenso que é aberto, clique em **Testar tipo** (ou **Testar tipos de informações confidenciais** se você tiver selecionado mais de um).

    ![Local dos tipos de informações confidenciais e botão de tipo de Teste](media/scc-cust-sens-info-type-test.png)

3. Na página **Carregar arquivo para teste** que se abre, carregue um documento para teste arrastando e soltando um arquivo, ou então clicando em **Procurar** e selecionando um arquivo.

    ![Carregar arquivos na página de teste](media/scc-cust-sens-info-type-test-upload.png)

4. Clique no botão **Testar** para testar o documento em busca de correspondências de padrão no arquivo.

5. Na página **Resultados da correspondência**, clique em **Concluir**.

    ![Resultados da correspondência](media/scc-cust-sens-info-type-test-results.png)
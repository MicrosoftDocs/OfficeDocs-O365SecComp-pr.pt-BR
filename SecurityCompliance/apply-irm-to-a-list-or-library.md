---
title: Aplicar o gerenciamento de direitos de informação (IRM) a uma lista ou biblioteca
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 7/2/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- OSU150
- OSU160
- MET150
ms.assetid: 3bdb5c4e-94fc-4741-b02f-4e7cc3c54aa1
description: Você pode usar o gerenciamento de direitos de informação (IRM) para ajudar a controlar e proteger arquivos que são baixados listas ou bibliotecas.
ms.openlocfilehash: 5a48abf13841716d4dba34311d69ca2e6a5ea422
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523985"
---
# <a name="apply-information-rights-management-irm-to-a-list-or-library"></a>Aplicar o gerenciamento de direitos de informação (IRM) a uma lista ou biblioteca

Você pode usar o gerenciamento de direitos de informação (IRM) para ajudar a controlar e proteger arquivos que são baixados listas ou bibliotecas.
  
## <a name="before-you-begin"></a>Antes de começar

- O serviço de gerenciamento de direitos do Windows Azure (Azure RMS) de proteção de informações do Windows Azure e o equivalente no local, o Active Directory Rights Management Services (AD RMS), suporte Information Rights Management para sites. Nenhuma instalação separada ou adicionais é necessárias.
    
- Antes de aplicar IRM para uma lista ou biblioteca, que ele primeiro deve ser habilitado por um administrador para o seu site.
    
- Para aplicar IRM em uma lista ou biblioteca, você deve ter permissões de administrador para essa lista ou biblioteca.
    
- Se você estiver usando o SharePoint Online, os usuários podem sofrer tempos limite ao fazer o download de arquivos maiores protegidas por IRM. Se isso acontecer, aplicar a proteção IRM usando seus programas do Office e armazene arquivos maiores em uma biblioteca do SharePoint que não usa o IRM.
    
> [!NOTE]
> Se você estiver usando o SharePoint Server 2013, um administrador de servidor deve instalar protetores em todos os servidores Web front-end, para cada tipo de arquivo que deseja que as pessoas na sua organização a proteção usando o IRM. 
  
## <a name="apply-irm-to-a-list-or-library"></a>Aplicar o IRM para uma lista ou biblioteca
<a name="__toc256598179"> </a>

![Configurações de gerenciamento de direitos de informação](media/1b708102-9c90-42b0-b255-ef0e72d0be88.png)
  
1. Vá para a lista ou biblioteca para a qual você deseja configurar o IRM.
    
2. Na faixa de opções, clique na guia **biblioteca** e, em seguida, clique em **Definições da biblioteca**. (Se você estiver trabalhando em uma lista, clique na guia **lista** e clique em **Definições de lista**).
    
    ![Botões de configurações da biblioteca do SharePoint na faixa de opções](media/cdf718fa-d792-40fc-8026-00c3b80b9e05.png)
  
3. Em **permissões e gerenciamento**, clique em **Gerenciamento de direitos de informação**. Se o link do Information Rights Management não aparecer, o IRM não pode ser habilitado para o seu site. Contate o administrador do servidor para ver se é possível habilitar o IRM para seu site. O link do Information Rights Management não aparece para bibliotecas de imagens.
    
4. Na página **Configurações de gerenciamento de direitos de informação** , marque a caixa de seleção **Restringir permissão aos documentos essa biblioteca no download** para aplicar a permissão restrita a documentos que são baixados dessa lista ou biblioteca. 
    
5. Na caixa **criar um título de política de permissão** , digite um nome descritivo para a política que você pode usar posteriormente para diferenciar esta política de outras políticas. Por exemplo, você pode digitar **Confidencial da empresa** se você estiver aplicando permissão restrita a uma lista ou biblioteca que conterá os documentos que são confidenciais da empresa. 
    
6. Na caixa **Adicionar uma descrição da política de permissão** , digite uma descrição que será exibido para as pessoas que usam essa lista ou biblioteca que explica como eles devem lidar com documentos dessa lista ou biblioteca. Por exemplo, você pode digitar **aborde o conteúdo deste documento apenas com outros funcionários** se desejar restringir o acesso às informações nestes documentos para funcionários internos. 
    
7. Para aplicar as restrições adicionais para os documentos em dessa lista ou biblioteca, clique em **Mostrar opções**e siga um destes procedimentos:
    
|**Para fazer isso:**|**Faça o seguinte:**|
|:-----|:-----|
|Permitir que as pessoas imprimir documentos a partir dessa lista ou biblioteca  <br/> |Marque a caixa de seleção **Permitir visualizadores para imprimir** .  <br/> |
|Permitir que as pessoas pelo menos a permissão de exibir itens para executar código ou macros incorporados em um documento.  <br/> |Marque a caixa de seleção **Permitir que os visualizadores executar leitor de tela e o script funcione em documentos baixados** .  <br/> Se você selecionar essa opção, os usuários pode executar código para extrair o conteúdo de um documento.           |
|Exigir que as pessoas verificar suas credenciais em intervalos específicos.  <br/> Selecione essa opção se desejar restringir o acesso ao conteúdo para um período de tempo especificado. Se você selecionar essa opção, as licenças de publicação de pessoas para acessar o conteúdo expirará após o número especificado de dias e pessoas deverá retornar para o servidor para verificar suas credenciais e baixar uma nova cópia.  <br/> |Selecione o **os usuários devem verificar suas credenciais usando este intervalo de (dias)** caixa de seleção e, em seguida, especifique o número de dias para o qual você deseja que o documento esteja visível.  <br/> |
| Impedir que as pessoas carregar documentos que não têm suporte para IRM para esta lista ou biblioteca.  <br/>  Se você selecionar essa opção, as pessoas não poderão carregar qualquer um dos seguintes tipos de arquivo:  <br/>  Tipos de arquivo que não têm protetores de IRM correspondentes instalados em todos os servidores Web front-end.  <br/>  Tipos de arquivo que não é possível descriptografar o SharePoint Server 2010.  <br/>  Tipos de arquivo que são protegido em outro programa IRM  <br/> |Marque a caixa de seleção **não permitir que os usuários carreguem documentos que não têm suporte para IRM** .  <br/> |
|Remova permissões restritas a partir dessa lista ou biblioteca em uma data específica.  <br/> |Marque a caixa de seleção **Parar de restringir o acesso à biblioteca em** e selecione a data em que você deseja.  <br/> |
|Controle o intervalo que credenciais são armazenados em cache para o programa que estiver licenciado para abrir o documento.  <br/> |No **definir proteção de grupo e o intervalo de credenciais**, digite theinterval para armazenar em cache credenciais em número de dias.  <br/> |
|Permitir a proteção de grupo para que os usuários podem compartilhar com os membros do mesmo grupo.  <br/> |Selecione **Permitir proteção de grupo**e digite o nome do grupo para o compartilhamento.  <br/> |
   
8. Depois de terminar de selecionar as opções desejadas, clique em **Okey**.
  
## <a name="what-is-information-rights-management"></a>O que é gerenciamento de direitos de informação?
<a name="__toc256598175"> </a>

Gerenciamento de direitos de informação (IRM) permite que você limite as ações que os usuários podem ser realizadas em arquivos que foram baixados do listas ou bibliotecas. IRM criptografa os arquivos baixados e limita o conjunto de usuários e programas que têm permissão para descriptografar esses arquivos. IRM também pode limitar os direitos dos usuários que têm permissão para ler arquivos, para que eles não podem realizar ações como cópias impressas dos arquivos ou copiar texto de-los.
  
Você pode usar o IRM em listas ou bibliotecas para limitar a disseminação de conteúdo confidencial. Por exemplo, se você estiver criando uma biblioteca de documentos para compartilhar informações sobre produtos futuras com representantes de marketing selecionados, você pode usar o IRM para impedir que essas pessoas compartilhem esse conteúdo com outros funcionários da empresa.
  
Em um site, você aplicar IRM para um toda a lista ou biblioteca, e não para arquivos individuais. Isso facilita garantir um nível consistente de proteção para todo um conjunto de documentos ou arquivos. IRM, portanto, pode ajudar sua organização para impor políticas corporativas que governam o uso e a disseminação de informações confidenciais e proprietárias.
  
> [!NOTE]
> As informações nesta página sobre gerenciamento de direitos de informação substitui quaisquer termos que fazem referência a 'Information Rights Management' em quaisquer contratos de termos de licença do Microsoft SharePoint Server 2013 e SharePoint Server 2016. 
  
### <a name="how-irm-can-help-protect-content"></a>Como o IRM pode ajudar a proteger o conteúdo
<a name="__toc256598176"> </a>

O IRM ajuda a proteger conteúdo restrito das seguintes maneiras:
  
- Ajuda a evitar que um visualizador autorizado de copiar, modificar, imprimir, envio de fax, ou copiar e colar o conteúdo para o uso não autorizado
    
- Ajuda a evitar que um visualizador autorizado copiem o conteúdo usando o recurso de Print Screen no Microsoft Windows
    
- Ajuda a impedir que um visualizador não autorizado exibindo o conteúdo se ele for enviado por email depois que ele é baixado do servidor
    
- Restringe o acesso ao conteúdo para um período especificado de tempo, após o qual os usuários deverão confirmar suas credenciais e baixar o conteúdo novamente
    
- Ajuda a impor diretivas corporativas que governam o uso e a disseminação de conteúdo dentro da sua organização
    
### <a name="how-irm-cannot-help-protect-content"></a>Como o IRM não pode ajudar a proteger o conteúdo
<a name="__toc256598177"> </a>

IRM não pode proteger conteúdo restrito dentre os seguintes:
  
- Eliminação, roubo, captura ou transmissão por programas mal-intencionados como cavalos de Troia, os registradores de pressionamento de tecla e certos tipos de spyware
    
- Perda ou corrupção devido a ações de vírus de computador
    
- Cópia manual ou redigitar de conteúdo da exibição em uma tela
    
- Digital ou fotografia do conteúdo que é exibido em uma tela do filme
    
- Copiando devido ao uso de programas de captura de tela de terceiros
    
- Copiando de metadados do conteúdo (valores de coluna) com o uso de programas de captura de tela de terceiros ou ação de copiar e colar
    
[Aplicar o Gerenciamento de Direitos de Informação a uma lista ou biblioteca](https://support.office.com/article/6714cfe3-ef39-43b0-bb65-a887726bb63c)
  
## <a name="how-irm-works-for-lists-and-libraries"></a>Como o IRM funciona para listas e bibliotecas
<a name="__toc256598178"> </a>

Proteção de IRM é aplicada aos arquivos no nível de lista ou biblioteca. Quando o IRM está habilitado para uma biblioteca, gerenciamento de direitos se aplica a todos os arquivos nessa biblioteca. Quando o IRM está habilitado para obter uma lista, gerenciamento de direitos só se aplica aos arquivos que estejam anexados a itens de lista, não os itens de lista reais.
  
Quando as pessoas baixar arquivos em uma biblioteca ou uma lista de IRM habilitado, os arquivos são criptografados para que apenas as pessoas autorizadas possam exibi-los. Cada arquivo com direitos gerenciados também contém uma licença de publicação que impõe restrições em que as pessoas que exibir o arquivo. Restrições típicas incluem a realização de um arquivo somente leitura, desabilitando a cópia de texto, impedindo que pessoas de salvar uma cópia local e impedindo que pessoas imprimir o arquivo. Programas de cliente que podem ler a tipos de arquivo suportados pelo IRM usar a licença de publicação dentro do arquivo com direitos gerenciados para impor essas restrições. Isso é como um arquivo com direitos gerenciados mantém sua proteção, mesmo depois que ele é baixado do servidor.
  
Os tipos de restrições que são aplicadas a um arquivo quando ele é baixado de uma lista ou biblioteca baseiam-se nas permissões do usuário individual no site que contém o arquivo. A tabela a seguir explica como as permissões nos sites correspondem às permissões do IRM.
  
|**Permissões**|**Permissões do IRM**|
|:-----|:-----|
|Gerenciar permissões e gerenciar um Site da Web  <br/> |**Controle total** (conforme definido pelo programa cliente): essa permissão geralmente permite que um usuário ler, editar, copiar, salvar e modificar permissões de conteúdo com direitos gerenciados.  <br/> |
|Editar itens, gerenciar listas, adicionar e personalizar páginas  <br/> |**Editar**, **Copiar**e **Salvar**: um usuário pode imprimir um arquivo somente se a caixa de seleção **Permitir que os usuários para imprimir documentos** está selecionada na página de configurações de gerenciamento de direitos de informações para a lista ou biblioteca.  <br/> |
|Exibir Itens  <br/> |**Leitura**: um usuário pode ler o documento, mas não pode copiar ou modificar o seu conteúdo. Um usuário pode imprimir somente se a caixa de seleção **Permitir que os usuários para imprimir documentos** está selecionada na página de configurações de gerenciamento de direitos de informações para a lista ou biblioteca.<br/> |
|Outro  <br/> |Nenhuma outra permissão corresponde diretamente às permissões de IRM.  <br/> |
   
Quando você habilita o IRM para uma lista ou biblioteca no SharePoint Server 2013, você pode proteger apenas os tipos de arquivo nessa lista ou biblioteca para a qual um protetor está instalado em todos os servidores Web front-end. Um protetor é um programa que controla a criptografia e descriptografia de arquivos com direitos gerenciados de um formato de arquivo específico. SharePoint inclui protetores para os seguintes tipos de arquivo:
  
- Microsoft Office InfoPath forms
    
- Os formatos de arquivo para os seguintes programas do Microsoft Office 97-2003: Word, Excel e PowerPoint
    
- Os formatos Office Open XML para os seguintes programas do Microsoft Office: Word, Excel e PowerPoint
    
- O formato XML Paper Specification (XPS)
    
Se sua organização estiver planejando usar o IRM para proteger quaisquer outros tipos de arquivo além daquelas listadas acima, o administrador do servidor deve instalar protetores esses formatos de arquivo adicional.
  


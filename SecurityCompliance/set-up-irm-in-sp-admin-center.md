---
title: Definir o gerenciamento de direitos de informação (IRM) no Centro de administração do SharePoint
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- MET150
ms.assetid: 239ce6eb-4e81-42db-bf86-a01362fed65c
description: Saiba como usar o IRM Online do SharePoint por meio de Microsoft Azure Active Directory Services RMS (Rights Management) para proteger as bibliotecas de documentos e listas do SharePoint.
ms.openlocfilehash: dea8c71ce67207b3c40a1f934f90e63740f70f29
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524057"
---
# <a name="set-up-information-rights-management-irm-in-sharepoint-admin-center"></a>Definir o gerenciamento de direitos de informação (IRM) no Centro de administração do SharePoint

Dentro do SharePoint Online, a proteção de IRM é aplicada a arquivos no nível de lista e biblioteca. Antes de sua organização pode usar a proteção de IRM, primeiro você deve configurar o gerenciamento de direitos. IRM depende do serviço de gerenciamento de direitos do Windows Azure de proteção de informações do Windows Azure para criptografar e atribuir as restrições de uso. Alguns planos do Office 365 incluem o Azure Rights Management, mas não todos. Para saber mais, leia a [serviços e aplicativos do Office como suporte para gerenciamento de direitos do Windows Azure](https://docs.microsoft.com/azure/information-protection/understand-explore/office-apps-services-support).
  
## <a name="turn-on-irm-service-using-sharepoint-admin-center"></a>Ativar o serviço IRM usando o Centro de administração do SharePoint

Antes de sua organização pode bibliotecas e listas do SharePoint de proteger o IRM, você deve primeiro ativar o serviço de gerenciamento de direitos para sua organização. Para saber como ver [Ativando o Azure Rights Management](https://docs.microsoft.com/information-protection/deploy-use/activate-service). Você deve usar uma conta de trabalho ou da escola que tenha privilégios de administrador global do Office 365 para habilitar o serviço de gerenciamento de direitos. Caso contrário, não será possível usar os recursos IRM com o SharePoint Online.
  
Após ativar o serviço de gerenciamento de direitos, entre no Centro de administração do SharePoint para ativar o IRM.
  
1. Entre no Office 365 como administrador global ou administrador do SharePoint.
    
2. Selecione o ícone do inicializador de aplicativos ![Ícone do inicializador de aplicativos do Office 365](media/e5aee650-c566-4100-aaad-4cc2355d909f.png) no canto superior esquerdo e escolha **Administração** para abrir o Centro de administração do Office 365. (Se não vir o bloco Administração, você não tem permissões de administrador do Office 365 na sua organização.) 
    
3. No painel esquerdo, escolha **Admin centrais** \> **SharePoint**.
    
4. No painel esquerdo, escolha **configurações**.
    
5. Na seção **Gerenciamento de direitos de informação (IRM)** , escolha **usar o serviço IRM especificado na sua configuração**e escolha **Atualizar configurações de IRM**. Depois que você atualizar configurações de IRM, pessoas da sua organização podem começar a usar o IRM em suas listas do SharePoint e as bibliotecas de documentos. No entanto, as opções para fazê-lo podem demorar para uma hora aparecem em configurações de biblioteca e lista.
    
## <a name="irm-enable-sharepoint-document-libraries-and-lists"></a>Listas e bibliotecas de documentos do SharePoint de habilitar IRM
<a name="__toc220831191"> </a>

Após atualizar configurações de IRM, os proprietários de sites podem proteger o IRM suas listas do SharePoint e bibliotecas de documentos. Para obter mais informações, consulte [Aplicar Information Rights Management para uma lista ou biblioteca](apply-irm-to-a-list-or-library.md).
  
Quando proprietários de sites habilitar o IRM para uma lista ou biblioteca, eles podem proteger todos os tipos de arquivo suportados nessa lista ou biblioteca. Quando o IRM está habilitado para uma biblioteca, gerenciamento de direitos se aplica a todos os arquivos nessa biblioteca. Quando você habilita o IRM para obter uma lista, gerenciamento de direitos se aplica apenas aos arquivos que estejam anexados a itens de lista, não os itens de lista reais.
  
Quando as pessoas baixar arquivos em uma biblioteca ou uma lista de IRM habilitado, os arquivos são criptografados para que apenas as pessoas autorizadas possam exibi-los. Cada arquivo com direitos gerenciados também contém uma licença de publicação que impõe restrições em que as pessoas que exibir o arquivo. Restrições típicas incluem a realização de um arquivo somente leitura, desabilitando a cópia de texto, impedindo que pessoas de salvar uma cópia local e impedindo que pessoas imprimir o arquivo. Programas de cliente que podem ler a tipos de arquivo suportados pelo IRM usar a licença de publicação dentro do arquivo com direitos gerenciados para impor essas restrições. Isso é como um arquivo com direitos gerenciados mantém sua proteção, mesmo depois que ele é baixado. Para habilitar o IRM em uma lista ou biblioteca, consulte [Aplicar Information Rights Management para uma lista ou biblioteca](apply-irm-to-a-list-or-library.md).
  
Você não pode criar ou editar documentos em uma biblioteca de IRM habilitado usando o Office Online. Em vez disso, uma pessoa por vez pode baixar e editar arquivos criptografadas pelo IRM. Use o check-in e check-out para gerenciar *a coautoria* ou criação entre vários usuários. 
  
Quando você baixa um arquivo PDF de uma biblioteca protegidas por IRM, o Office 365 cria um arquivo PDF protegido. Não alterará a extensão do arquivo, mas o arquivo está protegido. Para exibir esse arquivo, você precisará o Visualizador de proteção de informações do Windows Azure, o cliente completo de proteção de informações do Windows Azure, ou outro aplicativo que dá suporte à visualização para arquivos PDF protegidos. 
  
SharePoint Online suporta a criptografia dos seguintes tipos de arquivo:
  
- PDF
    
- Os formatos de arquivo para os seguintes programas do Microsoft Office 97-2003: Word, Excel e PowerPoint
    
- Formatos do Office Open XML para os seguintes programas do Microsoft Office: Word, Excel e PowerPoint
    
- O formato XML Paper Specification (XPS)
    
## <a name="next-steps"></a>Próximas etapas
<a name="__toc220831191"> </a>

Depois que você habilitou o IRM para o SharePoint Online, você pode iniciar a aplicação de gerenciamento de direitos às listas e bibliotecas. Para obter informações, consulte [Aplicar Information Rights Management para uma lista ou biblioteca](apply-irm-to-a-list-or-library.md).
  
O novo cliente de sincronização do OneDrive para Windows agora oferece suporte a sincronização de bibliotecas de documentos do SharePoint protegidas por IRM e OneDrive locais (desde que a configuração do IRM para a biblioteca não estiver configurada para expirar direitos de acesso do documento). Para obter mais informações, ou para começar a implantar o novo cliente de sincronização, consulte [Deploy o novo cliente de sincronização do OneDrive para Windows](https://support.office.com/article/3f3a511c-30c6-404a-98bf-76f95c519668).
  
[Topo da página](set-up-irm-in-sp-admin-center.md#__top)
  


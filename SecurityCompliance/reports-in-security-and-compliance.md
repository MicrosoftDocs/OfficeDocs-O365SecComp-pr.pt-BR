---
title: Relatórios de segurança do Office 365 &amp; Centro de conformidade
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 2/1/2018
ms.audience: Admin
ms.topic: overview
f1_keywords:
- ms.o365.cc.AuditingHelp
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
ms.assetid: 7acd33ce-1ec8-49fb-b625-43bac7b58c5a
description: 'Usar a segurança do Office 365 &amp; relatórios do Centro de conformidade para obter vários relatórios para sua organização do SharePoint Online e o Exchange Online, além do Azure Active Directory.  '
ms.openlocfilehash: 0b633583e14a18c7cf579d10462cf41714397812
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22523535"
---
# <a name="reports-in-the-office-365-security-amp-compliance-center"></a>Relatórios de segurança do Office 365 &amp; Centro de conformidade

Você pode usar a página **Exibir relatórios** de segurança do Office 365 &amp; Centro de conformidade para acessar rapidamente os relatórios de auditoria para suas organizações do SharePoint Online e o Exchange Online. Você também pode acessar Azure AD (Active Directory) usuário entrar relatórios, relatórios de atividade do usuário e do log de auditoria do Azure AD da página **Exibir relatórios** . Isso ocorre porque a sua assinatura paga do Office 365 inclui uma assinatura gratuita do Microsoft Azure. Na primeira vez que você tenta acessar esses relatórios Azure, você precisará concluir um processo de registro de uma única vez. 
  
> [!TIP]
> Para exibir relatórios adicionais sobre a atividade em sua organização do Office 365, consulte [Relatórios de atividade no Centro de administração do Office 365](https://support.office.com/article/0d6dfb17-8582-4172-a9a9-aed798150263). 
  
 **Antes de começar**
  
Você precisa das seguintes permissões para exibir relatórios de segurança &amp; Centro de conformidade.
  
- Você precisa ser atribuído à função de leitor de segurança no Centro de administração do Exchange (EAC) para exibir relatórios de segurança &amp; Centro de conformidade. Por padrão, essa função é atribuída aos grupos de função de gerenciamento da organização e leitor de segurança no EAC.
    
- Você precisa ser atribuído à função de gerenciamento de conformidade de DLP na segurança &amp; Centro de conformidade para exibir relatórios de DLP (e políticas de DLP) na segurança &amp; Centro de conformidade. Por padrão, essa função é atribuída aos grupos de função de administrador de conformidade, gerenciamento da organização e o administrador de segurança na segurança &amp; Centro de conformidade.
    
Além disso, você teria a ser atribuído à função de prevenção de perda de dados no EAC para exibir relatórios DLP (e políticas de DLP) no EAC. Por padrão, essa função é atribuída aos grupos de função de gerenciamento de conformidade e gerenciamento de organização no EAC.
  
 **Para abrir a página de relatórios do modo de exibição na segurança &amp; Centro de conformidade:**
  
1. Vá para [https://protection.office.com/#/viewreports](https://protection.office.com/#/viewreports).
    
2. Entrar no Office 365 usando as credenciais para uma conta de usuário em sua organização do Office 365.
    
Na página **Exibir relatórios** , você pode exibir os seguintes tipos de relatórios: 
  
- [Relatórios de auditoria no EOP](#auditing-reports)
- [Relatório de análise de supervisão](#supervisory-review-report)
- [Relatórios de prevenção contra perda de dados](#data-loss-prevention-reports)
    
## <a name="auditing-reports"></a>Relatórios de auditoria

A tabela a seguir descreve os relatórios na seção **auditoria** na página **Exibir relatórios** na segurança &amp; Centro de conformidade. 
  
|**Relatório**|**Descrição**|
|:-----|:-----|
|**Relatório de log de auditoria do Office 365** <br/> |Você pode pesquisar o log de auditoria do Office 365 para atividade de administrador e usuário em sua organização do Office 365. O relatório contém atividade de administrador e usuário de entradas no Exchange Online, SharePoint Online, OneDrive for Business e Windows Azure Active Directory, que é o serviço de diretório para o Office 365. Para obter mais informações, consulte [Pesquisar o log de auditoria de segurança do Office 365 &amp; Centro de conformidade](search-the-audit-log-in-security-and-compliance.md).<br/> |
|**Relatórios do Azure AD** <br/> |Para procurar incomum suspeita entrar atividade ou em sua organização do Office 365, você pode usar a entrada e a atividade reports in Microsoft Azure. Também é possível exibir os eventos no log de auditoria do Azure AD. Para exibir relatórios no Windows Azure, basta clicar em **Exibir Azure AD relatórios**. Para obter mais informações, consulte:<br/><br/>[Use sua assinatura gratuita do Azure Active Directory no Office 365](use-your-free-azure-ad-subscription-in-office-365.md). <br/> [Exibir os relatórios de uso e de acesso](http://go.microsoft.com/fwlink/p/?LinkId=506902).  <br/> |
|**Relatórios de auditoria do Exchange** <br/> | Você pode usar a funcionalidade de auditoria no Office 365 para rastrear as alterações feitas para a configuração do Exchange Online por administradores da sua organização. Alterações feitas em sua organização do Exchange Online por um administrador de centro de dados da Microsoft ou por um administrador delegado também são registradas. Para o Exchange Online, auditoria do administrador log está habilitado por padrão, portanto você não precisa fazer nada para ativá-lo. O Exchange Online também oferece para permitir que você controlar o acesso a caixas de correio por alguém que não seja o proprietário da caixa de correio do log de auditoria de caixa de correio. Você precisa habilitar o log para cada caixa de correio que você deseja controlar o acesso não proprietário de auditoria de caixa de correio.<br/>  Log de auditoria para administração e de caixa de correio, você pode executar relatórios de auditoria para exibir as entradas de log de auditoria. Você também pode exportar logs de auditoria de caixa de correio e administração, que são enviados para você dentro de 24 horas em um arquivo XML que está associado à mensagem de e-mail.<br/><br/>Para obter mais informações sobre como exportar logs de auditoria, consulte:  <br/><br/> [Exportar logs de auditoria de caixas de correio](http://go.microsoft.com/fwlink/p/?LinkID=404104) <br/> [Exibir e exportar o log de auditoria de administrador do datacenter](http://go.microsoft.com/fwlink/p/?LinkId=404109) <br/> [Pesquisar as alterações do grupo de funções ou logs de auditoria do administrador](http://go.microsoft.com/fwlink/p/?LinkId=404105) <br/>   [Relatórios de auditoria do Exchange](http://go.microsoft.com/fwlink/p/?LinkID=395232).  <br/> |
   
## <a name="supervisory-review-report"></a>Relatório de análise de supervisão

Com o relatório de análise de supervisão, você poderá ver o status de todas as políticas de análise de supervisão em sua organização. Para obter mais informações, consulte [Configure supervisão analisar políticas para sua organização](configure-supervision-policies.md).
  
## <a name="data-loss-prevention-reports"></a>Relatórios de prevenção contra perda de dados

Prevenção de perda de dados (DLP) relatórios contêm informações sobre as políticas DLP e regras que tiverem sido aplicadas ao conteúdo contêm dados confidenciais em sua organização do Office 365. Você também pode configurar o relatório para exibir informações sobre as ações de DLP que eram baseados na sua política de DLP e regras. Para obter mais informações, consulte [Exibir o relatório de prevenção de perda de dados](view-the-dlp-reports.md).

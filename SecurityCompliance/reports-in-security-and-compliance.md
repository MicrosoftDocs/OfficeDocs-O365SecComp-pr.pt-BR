---
title: Relatórios no Centro de Conformidade e Segurança do Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: overview
f1_keywords:
- ms.o365.cc.AuditingHelp
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 7acd33ce-1ec8-49fb-b625-43bac7b58c5a
description: 'Use o centro de conformidade do & de segurança do Office 365 para obter vários relatórios para sua organização do SharePoint Online e do Exchange Online, além de relatórios do Azure Active Directory.  '
ms.openlocfilehash: d6605ebfa5f733f24b6a3aa8d36c85203c264c0c
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219961"
---
# <a name="reports-in-the-office-365-security--compliance-center"></a>Relatórios no Centro de Conformidade e Segurança do Office 365

Você pode usar a página **exibir relatórios** no centro de conformidade do _AMP_ de segurança do Office 365 para acessar rapidamente relatórios de auditoria para suas organizações do SharePoint Online e do Exchange Online. Você também pode acessar os relatórios de entrada do usuário do Azure Active Directory (AD), relatórios de atividades do usuário e o log de auditoria do Azure AD na página **exibir relatórios** . Isso ocorre porque sua assinatura paga do Office 365 inclui uma assinatura gratuita para o Microsoft Azure. Na primeira vez que tentar acessar esses relatórios do Azure, você precisará concluir um processo de registro de uma vez. 
  
> [!TIP]
> Para exibir relatórios adicionais sobre a atividade em sua organização do Office 365, confira [relatórios de atividade no centro de administração do office 365](https://support.office.com/article/0d6dfb17-8582-4172-a9a9-aed798150263). 
  
 **Antes de começar**
  
Você precisa das permissões a seguir para exibir relatórios no centro de conformidade do & de segurança.
  
- Você precisa receber a função de leitor de segurança no centro de administração do Exchange (Eat) para exibir relatórios no centro de conformidade do & de segurança. Por padrão, essa função é atribuída aos grupos de função de gerenciamento de organização e leitor de segurança no Eat.
    
- Você precisa ter a função de gerenciamento de conformidade DLP somente para exibição no centro de conformidade do & de segurança para exibir relatórios de DLP no centro de conformidade do & de segurança. Por padrão, essa função é atribuída aos grupos de função Administrador de conformidade, gerenciamento de organização, administrador de segurança e leitor de segurança no centro de conformidade do & de segurança.

- Além disso, você deve receber a função de destinatários somente para exibição no Eat para exibir relatórios de DLP no Eat. Por padrão, essa função é atribuída aos grupos de função gerenciamento de conformidade, gerenciamento de organização e somente exibição da organização no Eat.
  
 **Para abrir a página exibir relatórios no centro de conformidade do & de segurança:**
  
1. Acesse [https://protection.office.com/#/viewreports](https://protection.office.com/#/viewreports).
    
2. Entre no Office 365 usando as credenciais de uma conta de usuário na sua organização do Office 365.
    
Na página **exibir relatórios** , você pode exibir os seguintes tipos de relatórios: 
  
- [Relatórios de auditoria no EOP](#auditing-reports)
- [Relatório de análise de supervisão](#supervisory-review-report)
- [Relatórios de prevenção contra perda de dados](#data-loss-prevention-reports)
    
## <a name="auditing-reports"></a>Relatórios de auditoria

A tabela a seguir descreve os relatórios na seção **auditoria** da página **exibir relatórios** no centro de conformidade do & de segurança. 
  
|**Relatório**|**Descrição**|
|:-----|:-----|
|**Relatório de log de auditoria do Office 365** <br/> |Você pode pesquisar o log de auditoria do Office 365 para atividades de usuário e administrador na sua organização do Office 365. O relatório contém entradas do usuário e da atividade de administração no Exchange Online, SharePoint Online, OneDrive for Business e Azure Active Directory, que é o serviço de diretório para o Office 365. Para obter mais informações, consulte [Pesquisar o log de auditoria no centro de conformidade do & de segurança do Office 365](search-the-audit-log-in-security-and-compliance.md).<br/> |
|**Relatórios do Azure AD** <br/> |Para procurar atividades de entrada incomuns ou suspeitas na sua organização do Office 365, você pode usar os relatórios de entrada e de atividades no Microsoft Azure. Você também pode exibir eventos no log de auditoria do Azure AD. Para exibir relatórios no Azure, basta clicar em **exibir relatórios do Azure ad**. Para obter mais informações, consulte:<br/><br/>[Use sua assinatura gratuita do Azure Active Directory no Office 365](use-your-free-azure-ad-subscription-in-office-365.md). <br/> [Exibir seus relatórios de uso e acesso](http://go.microsoft.com/fwlink/p/?LinkId=506902).  <br/> |
|**Relatórios de auditoria do Exchange** <br/> | Você pode usar a funcionalidade de auditoria no Office 365 para controlar as alterações feitas na configuração do Exchange Online pelos administradores da sua organização. As alterações feitas na sua organização do Exchange Online por um administrador de data center da Microsoft ou por um administrador delegado também são registradas. Para o Exchange Online, o log de auditoria de administrador é habilitado por padrão, portanto, você não precisa fazer nada para ativá-lo. O Exchange Online também fornece log de auditoria de caixa de correio para permitir que você controle o acesso a caixas de correio por alguém que não seja o proprietário da caixa de correio Você precisa habilitar o log de auditoria de caixa de correio para cada caixa de correio que deseja rastrear acesso não proprietário.<br/>  Para o log de auditoria de administrador e caixa de correio, você pode executar relatórios de auditoria para exibir as entradas de log de auditoria. Você também pode exportar logs de auditoria de caixa de correio e de administração, que são enviados para você dentro de 24 horas em um arquivo XML anexado à mensagem de email.<br/><br/>Para obter mais informações sobre como exportar logs de auditoria, consulte:  <br/><br/> [Exportar logs de auditoria de caixas de correio](http://go.microsoft.com/fwlink/p/?LinkID=404104) <br/> [Exibir e exportar o log de auditoria do administrador de datacenter](http://go.microsoft.com/fwlink/p/?LinkId=404109) <br/> [Pesquisar as alterações do grupo de funções ou logs de auditoria de administrador](http://go.microsoft.com/fwlink/p/?LinkId=404105) <br/>   [Relatórios de auditoria do Exchange](http://go.microsoft.com/fwlink/p/?LinkID=395232).  <br/> |
   
## <a name="supervisory-review-report"></a>Relatório de análise de supervisão

Com o relatório de análise de supervisão, você pode ver o status de todas as políticas de análise de supervisão em sua organização. Para saber mais, confira [Configurar políticas de análise de supervisão para sua organização](configure-supervision-policies.md).
  
## <a name="data-loss-prevention-reports"></a>Relatórios de prevenção contra perda de dados

Os relatórios de prevenção de perda de dados (DLP) contêm informações sobre as políticas e regras de DLP que foram aplicadas ao conteúdo contêm dados confidenciais em sua organização do Office 365. Você também pode configurar o relatório para exibir informações sobre ações DLP que foram baseadas em sua política e regras de DLP. Para obter mais informações, consulte [View the Report for Data Loss Prevention](view-the-dlp-reports.md).

---
title: Retenção, exclusão e destruição de dados no Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: Uma visão geral das políticas da Microsoft para o Office 365 em relação à retenção, exclusão e destruição de dados.
ms.openlocfilehash: 8a773ebafba0d7cdd36b9da30878dcc487685846
ms.sourcegitcommit: 24659bdb09f49d0ffed180a4b80bbb7c45c2d301
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2019
ms.locfileid: "24961567"
---
# <a name="data-retention-deletion-and-destruction-in-office-365"></a>Retenção, exclusão e destruição de dados no Office 365

A Microsoft tem uma política padrão de manipulação de dados para o Office 365 que especifica por quanto tempo os dados do cliente serão mantidos após serem excluídos. Em geral, há dois cenários nos quais os dados do cliente são excluídos:

- **Exclusão ativa** -o locatário tem uma assinatura ativa e um usuário exclui os dados ou os dados fornecidos por um usuário são excluídos pelo administrador.
- **Exclusão passiva** -a assinatura do locatário termina.

## <a name="data-retention"></a>Retenção de dados

Para cada um desses cenários de exclusão, a tabela a seguir mostra o período máximo de retenção de dados, por categoria e classificação de dados:

| Categoria de dados | Classificação de dados | Descrição | Exemplos | Período de retenção |
|-----------------|-----------------|-----------------|----------------------------------|-------------------------------|
| Dados do cliente | Conteúdo do cliente| Conteúdo fornecido diretamente/criado por administradores e usuários <br><br> Isso inclui todos os textos, sons, vídeos, arquivos de imagem e software criados e armazenados nos data centers da Microsoft ao usar os serviços do Office 365 | Exemplos dos aplicativos do Office 365 usados com mais frequência que permitem aos usuários criar dados incluem Word, Excel, PowerPoint, Outlook e OneNote <br><br> O conteúdo do cliente também inclui segredos de Propriedade do cliente/fornecidos (senhas, certificados, chaves de criptografia, chaves de armazenamento) | **Cenário de exclusão ativa:** no máximo 30 dias <br><br> **Cenário de exclusão passiva:** no máximo 180 dias |
| Dados do cliente | Informações de identificação do usuário final (EUII) | Dados que identificam ou podem ser usados para identificar o usuário de um serviço Microsoft. EUII não contém conteúdo do cliente | Nome de usuário ou nome de exibição (domínio \ nome_de_usuário) <br><br> Nome principal do usuário (nome @ domínio) <br><br>  Endereços IP específicos do usuário | **Cenário de exclusão ativa:** no máximo 180 dias (apenas uma ação de administrador de locatário) <br><br> **Cenário de exclusão passiva:** no máximo 180 dias |
| Dados pessoais <br> (dados não incluídos nos dados do cliente) | Identificadores de pseudônimos do usuário final (EUPI) | Um identificador criado pela Microsoft ligado ao usuário de um serviço Microsoft. Quando o EUPI é combinado com outras informações, como uma tabela de mapeamento, ele identifica o usuário final <br><br> EUPI não contém informações carregadas ou criadas pelo cliente | GUIDs de usuário, PUIDs ou SIDs <br><br> IDs de sessão | **Cenário de exclusão ativa:** no máximo 30 dias <br><br> **Cenário de exclusão passiva:** no máximo 180 dias |

## <a name="subscription-retention"></a>Retenção de assinatura

Em todos os momentos durante o período de uma assinatura ativa, um assinante pode acessar, extrair ou excluir dados do cliente armazenados no Office 365. Se uma assinatura paga terminar ou for finalizada, a Microsoft manterá os dados do cliente armazenados no Office 365 em uma conta de função limitada por 90 dias para habilitar o assinante a extrair os dados. Após o término do período de retenção de 90 dias, a Microsoft desabilitará a conta e excluirá os dados do cliente. Não mais de 180 dias após a expiração ou o encerramento de uma assinatura do Office 365, a Microsoft desabilitará a conta e excluirá todos os dados do cliente da conta. Quando o período de retenção máximo de qualquer dado tiver decorrido, os dados são renderizados de uma recuperação comercial.

No caso de uma avaliação gratuita, sua conta mudará para um status de cortesia por 30 dias na maioria dos países e regiões. Durante esse período de cortesia, você tem a opção de comprar o Office 365. Se decidir não comprar o Office 365, você poderá cancelar a avaliação ou deixar o período de cortesia expirar, e as informações e os dados da conta de teste serão excluídos.

## <a name="expedited-deletion"></a>Exclusão acelerada
Em todos os momentos durante o período de qualquer assinatura, um assinante pode entrar em contato com o suporte da Microsoft e solicitar o desprovisionamento de assinatura acelerada. Nesse processo, todos os dados do usuário, incluindo os dados do SharePoint Online, do Exchange Online que podem estar em espera ou armazenados em caixas de correio inativas, são excluídos três dias após o administrador inserir o código de bloqueio fornecido pela Microsoft. Para obter mais informações sobre desprovisionamento acelerado, confira [cancelar o Office 365](https://support.office.com/article/Cancel-Office-365-for-business-b1bc0bef-4608-4601-813a-cdd9f746709a).

## <a name="related-links"></a>Links relacionados
- [Destruição de dados](office-365-data-destruction.md)

- [Imutabilidade no Office 365](office-365-data-immutability.md)
- [Exclusão de dados do Exchange Online](office-365-exchange-online-data-deletion.md)
- [Exclusão de dados do SharePoint Online](office-365-sharepoint-online-data-deletion.md)
- [Exclusão de dados do Skype for Business ](office-365-skype-data-deletion.md)
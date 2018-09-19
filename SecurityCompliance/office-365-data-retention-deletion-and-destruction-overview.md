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
description: Visão geral das políticas da Microsoft para Office 365 relacionadas a retenção de dados, exclusão e destruição.
ms.openlocfilehash: bb038f8bd8e3f0286ea7d673e5e286bdc4a9677d
ms.sourcegitcommit: 1bccdaacf358505604c9cf422cb1e272aefae19d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/19/2018
ms.locfileid: "23999142"
---
# <a name="data-retention-deletion-and-destruction-in-office-365"></a>Retenção, exclusão e destruição de dados no Office 365

## <a name="introduction"></a>Introdução
A Microsoft tem uma política padrão de manipulação de dados para o Office 365 que especifica por quanto tempo os dados do cliente serão mantidos após que está sendo excluído. Em geral, em Office 365, existem dois cenários nos quais os dados de cliente são excluídos:
- **Exclusão active** - um usuário exclui dados ou dados privados para o usuário são excluídos depois que o usuário é excluído pelo administrador de um inquilino ativo.
- **Exclusão passiva** - as extremidades de assinatura do inquilino.

A política padrão de manipulação de dados da Microsoft para o Office 365 Especifica por quanto tempo os dados serão mantidos em cada um desses cenários. As seções a seguir descrevem as categorias de dados (com base em Office 365 ativos classificação Standard do Microsoft) e os períodos de retenção para cenários de exclusão ativas e passivas.

## <a name="active-deletion-retention"></a>Retenção de exclusão de ativo

| Categoria de dados | Reter pelo menos | Reter no máximo |
|---------------------------------------|:-----------------:|:-----------------:|:----------------------------------:|:-------------------------------:|
| Dados de controle de acesso | N/D | N/D |
| Conteúdo de cliente | 7 dias | 30 dias |
| Informações de identificação de usuário final | 90 dias | 180 dias |
| Dados da conta | 1 ano | 3 anos |
| Informações de identificação da organização | 90 dias | 180 dias |
| Metadados do sistema | Consulte os Logs de segurança | Consulte os Logs de segurança |
| Logs de segurança | Min 1 ano | Max 1 ano |
| Logs de arquivamento do Exchange Online | Min 3 anos | Máximo de 3 anos |

## <a name="passive-deletion-retention"></a>Retenção de exclusão passiva

| Categoria de dados | Reter pelo menos | Reter no máximo |
|---------------------------------------|:-----------------:|:-----------------:|:----------------------------------:|:-------------------------------:|
| Dados de controle de acesso | 90 dias (para recuperação de conteúdo) | 180 dias (para recuperação de conteúdo) |
| Conteúdo de cliente | 90 dias (limitado-função conta) | 180 dias |
| Informações de identificação de usuário final | 90 dias | 180 dias |
| Dados da conta | 1 ano | 3 anos |
| Informações de identificação da organização | 90 dias | 180 dias |
| Metadados do sistema | Consulte os Logs de segurança | Consulte os Logs de segurança |
| Logs de segurança | Min 1 ano | Max 1 ano |
| Logs de arquivamento do Exchange Online | Min 3 anos | Máximo de 3 anos |

## <a name="subscription-rentention"></a>Retenção de assinatura

Conteúdo do cliente é definido como o conteúdo de caixa de correio Exchange Online (corpo, entradas de calendário e o conteúdo de anexos de email, de email e, se aplicável, Skype para conteúdo de negócios), o conteúdo do site do SharePoint Online e os arquivos armazenados em sites e os arquivos carregado OneDrive para negócios ou Skype para negócios.

Em todos os momentos durante a vigência de uma assinatura, um assinante pode acessar e extrair dados do cliente armazenados no Office 365. Exceto as avaliações gratuitas e serviços LinkedIn, Microsoft retém dados armazenados no Office 365 em uma conta de função de limitado por 90 dias após a expiração ou rescisão da assinatura para habilitar o assinante extrair os dados do cliente. (No caso de uma versão gratuita de avaliação, quando a versão de avaliação expira, ele move em um período de carência, oferecendo 30 dias (para a maioria das tentativas, na maioria dos países e regiões) para adquirir o Office 365. Se você decidir não comprar o Office 365, você pode permitem que sua avaliação expirar ou cancelar a ele. Logo após o período de carência de 30 dias, suas informações de conta de avaliação e nos dados é permanentemente apagado.)

Após o término do período de retenção de 90 dias, o Microsoft desabilita a conta e exclui os dados do cliente. Não mais de 180 dias após a expiração ou terminação de uma assinatura para o Office 365, a Microsoft desabilitar a conta e excluir todos os dados de cliente da conta. Depois que o período de retenção máximo para quaisquer dados tiver decorrido, os dados são processados comercialmente irrecuperáveis.

A Microsoft também tem uma política padrão de manipulação de dados que atenda a reciclagem e o descarte de unidades de disco e com falha ou retiradas de servidores. Antes de usar novamente qualquer drives de disco no Office 365, Microsoft executa um processo de limpeza físico que seja compatível com SP NIST 800-88. Unidades de disco que não podem ser reutilizadas são descartadas usando um processo de destruição física que é executado no local dentro do data center que contém os discos sendo destruídos. Estes procedimentos são realizados pela infraestrutura de nuvem da Microsoft & operações (MCIO). Para obter mais informações, consulte o MCIO reports no guia de [Visualização de confiança do serviço](https://aka.ms/STP)de auditoria.

## <a name="expedited-deletion"></a>Exclusão acelerado
Em todos os momentos durante a vigência de uma assinatura, um assinante pode contatar Microsoft Support e desprovisionamento de inscrição de solicitação expedida. Nesse processo, todos os dados do usuário, incluindo os dados no SharePoint Online, o Exchange Online que pode estar em espera ou armazenado em caixas de correio inativas, é excluídos três dias após o administrador insere o código de bloqueio fornecido pela Microsoft. Para obter mais informações sobre acelerado deprovisioning, consulte [Cancelar o Office 365](https://support.office.com/article/Cancel-Office-365-for-business-b1bc0bef-4608-4601-813a-cdd9f746709a).

## <a name="related-links"></a>Links relacionados
- [Exclusão de dados do Exchange Online](office-365-exchange-online-data-deletion.md)
- [Exclusão de dados do SharePoint Online](office-365-sharepoint-online-data-deletion.md)
- [Exclusão de dados do Skype for Business ](office-365-skype-data-deletion.md)
- [Imutabilidade no Office 365](office-365-data-immutability.md)
- [Destruição de dados](office-365-data-destruction.md)

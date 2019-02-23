---
title: RGPD para compartilhamentos de arquivos locais
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
description: Saiba mais sobre como atender aos requisitos de RGPD em compartilhamentos de arquivos no Windows Server local.
ms.openlocfilehash: 14af73a2ff2a162f2f3e621c2efeb5d9050c069a
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220261"
---
# <a name="gdpr-for-on-premises-windows-server-file-shares"></a><span data-ttu-id="84b5e-103">RGPD para compartilhamentos de arquivos no Windows Server local</span><span class="sxs-lookup"><span data-stu-id="84b5e-103">GDPR for on-premises Windows Server file shares</span></span>

<span data-ttu-id="84b5e-104">A abordagem básica recomendada para compartilhamentos de arquivos é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="84b5e-104">The basic recommended approach for file shares is:</span></span>

-   <span data-ttu-id="84b5e-105">Use a Proteção de Informações do Azure para identificar os dados confidenciais.</span><span class="sxs-lookup"><span data-stu-id="84b5e-105">Use Azure Information Protection to label sensitive data.</span></span>

-   <span data-ttu-id="84b5e-106">Use o verificador da Proteção de Informações do Azure para encontrar dados.</span><span class="sxs-lookup"><span data-stu-id="84b5e-106">Use Azure Information Protection scanner to find data.</span></span>

<span data-ttu-id="84b5e-107">A abordagem recomendada para compartilhamentos de arquivos inclui estas etapas:</span><span class="sxs-lookup"><span data-stu-id="84b5e-107">The recommended approach for files shares includes these steps:</span></span>

1.  <span data-ttu-id="84b5e-108">**Instale e configure o verificador da Proteção de Informações do Azure.**</span><span class="sxs-lookup"><span data-stu-id="84b5e-108">**Install and configure Azure Information Protection scanner.**</span></span>

    -   <span data-ttu-id="84b5e-109">Decida quais tipos de dados confidenciais usar.</span><span class="sxs-lookup"><span data-stu-id="84b5e-109">Decide which sensitive data types to use.</span></span>

    -   <span data-ttu-id="84b5e-110">Especifique pastas locais e compartilhamentos de rede a serem usados.</span><span class="sxs-lookup"><span data-stu-id="84b5e-110">Specify local folders and network shares to use.</span></span>

2.  <span data-ttu-id="84b5e-111">**Execute um ciclo de descoberta.**</span><span class="sxs-lookup"><span data-stu-id="84b5e-111">**Complete a discovery cycle.**</span></span>

    -   <span data-ttu-id="84b5e-112">Execute o verificador no modo de descoberta e valide os resultados.</span><span class="sxs-lookup"><span data-stu-id="84b5e-112">Run the scanner in discovery mode and validate the findings.</span></span>

    -   <span data-ttu-id="84b5e-113">Se necessário, otimize as condições e os tipos de informações confidenciais.</span><span class="sxs-lookup"><span data-stu-id="84b5e-113">If needed, optimize the conditions and sensitive information types.</span></span>

    -   <span data-ttu-id="84b5e-114">Avalie o impacto esperado de aplicar rótulos automaticamente.</span><span class="sxs-lookup"><span data-stu-id="84b5e-114">Assess the expected impact of automatically applying labels.</span></span>

3.  <span data-ttu-id="84b5e-115">**Execute o verificador da Proteção de Informações do Azure para aplicar rótulos a documentos qualificados**.</span><span class="sxs-lookup"><span data-stu-id="84b5e-115">**Run the Azure Information Protection scanner to apply labels to qualifying documents**.</span></span>

4.  <span data-ttu-id="84b5e-116">**Para a proteção:**</span><span class="sxs-lookup"><span data-stu-id="84b5e-116">**For protection:**</span></span>

    -   <span data-ttu-id="84b5e-117">Configure regras de prevenção contra a perda de dados do Exchange para proteger documentos com o rótulo desejado.</span><span class="sxs-lookup"><span data-stu-id="84b5e-117">Configure Exchange data loss prevention rules to protect documents with the desired label.</span></span>

    -   <span data-ttu-id="84b5e-118">Certifique-se de usar permissões para limitar quem pode acessar os arquivos.</span><span class="sxs-lookup"><span data-stu-id="84b5e-118">Be sure to use permissions to limit who can access files.</span></span>

5.  <span data-ttu-id="84b5e-119">**Para monitorar, integre os registros do Windows Server com uma ferramenta SIEM.**</span><span class="sxs-lookup"><span data-stu-id="84b5e-119">**For monitoring, integrate Windows Server logs with a SIEM tool.**</span></span>

    -   <span data-ttu-id="84b5e-p101">Para localizar dados pessoais para solicitações de titulares de dados, use o verificador da Proteção de Informações do Azure. Você também pode configurar a pesquisa do SharePoint Server para rastrear compartilhamentos de arquivos.</span><span class="sxs-lookup"><span data-stu-id="84b5e-p101">To find personal data for data subject requests, use Azure Information Protection scanner. You can also configure SharePoint Server search to crawl file shares.</span></span>

<span data-ttu-id="84b5e-122">Confira mais informações sobre como usar o verificador da Proteção de Informações do Azure para localizar e rotular dados pessoais.O Microsoft GDPR Data Discovery Toolkit se encontra em [http://aka.ms/gdprpartners](<http://aka.ms/gdprpartners>).</span><span class="sxs-lookup"><span data-stu-id="84b5e-122">For more information on using Azure Information Protection scanner to find and label personal data, see the Microsoft GDPR Data Discovery Toolkit at [http://aka.ms/gdprpartners](<http://aka.ms/gdprpartners>).</span></span>

<span data-ttu-id="84b5e-p102">Confira informações sobre como configurar o verificador para utilizar condições e os tipos de informações confidenciais para prevenção contra perda de dados (DLP) do Office 365 em [Como configurar as condições de classificação automática e recomendada para a Proteção de Informações do Azure](https://docs.microsoft.com/pt-BR/information-protection/deploy-use/configure-policy-classification). Observe que os novos tipos de informações confidenciais do Office 365 não estarão disponíveis imediatamente para uso com o verificador e que tipos de informações confidenciais personalizadas não podem ser usadas com o verificador.</span><span class="sxs-lookup"><span data-stu-id="84b5e-p102">For information on configuring the scanner for conditions and using the Office 365 data loss prevention (DLP) sensitive information types, see [How to configure conditions for automatic and recommended classification for Azure Information Protection](https://docs.microsoft.com/pt-BR/information-protection/deploy-use/configure-policy-classification). Note that new Office 365 sensitive information types will not be immediately available to use with the scanner and custom sensitive information types cannot be used with the scanner.</span></span>

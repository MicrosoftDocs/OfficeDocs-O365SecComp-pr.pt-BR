---
title: Envios de administradores no Office 365 ATP
ms.author: brwilcox
author: briwilcox
manager: dansimp
ms.date: 07/09/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: Saiba como enviar mensagens, URLs e arquivos potencialmente nocivos à Microsoft.
ms.openlocfilehash: 6f7ea63cae4d7cafb0d1386b29d99101d290ef30
ms.sourcegitcommit: 9e2df36b05a2c93ce2629a7a5eda8f44159d114d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/11/2019
ms.locfileid: "35632221"
---
# <a name="admin-submissions-in-office-365-atp"></a><span data-ttu-id="33133-103">Envios de administradores no Office 365 ATP</span><span class="sxs-lookup"><span data-stu-id="33133-103">Admin submissions in Office 365 ATP</span></span>

<span data-ttu-id="33133-104">Agora, os administradores podem enviar emails usando a ID de mensagem de arquivo ou de rede, URLs e arquivos para verificação da Microsoft no Office 365.</span><span class="sxs-lookup"><span data-stu-id="33133-104">Admins can now send emails by using file or network message ID, URLs, and files for scanning by Microsoft in Office 365.</span></span> <span data-ttu-id="33133-105">A seção envios atualizados ainda inclui mensagens relatadas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="33133-105">The updated submissions section still includes user reported messages.</span></span> 

<span data-ttu-id="33133-106">Ao enviar um email, você receberá informações sobre qualquer política que possa ter permitido o email de entrada em seu locatário, bem como o exame de qualquer URL e anexo no email.</span><span class="sxs-lookup"><span data-stu-id="33133-106">When you submit an email, you will get information about any policies that may have allowed the incoming email into your tenant, as well as examination of any URLs and attachments in the mail.</span></span> <span data-ttu-id="33133-107">As políticas que podem ter permitido um email incluem a lista de remetentes confiáveis de um usuário individual, bem como as políticas de nível de locatário, como regras ETR.</span><span class="sxs-lookup"><span data-stu-id="33133-107">Policies that may have allowed a mail include an individual user's safe sender list as well as tenant level policies such as ETR rules.</span></span> 


## <a name="how-to-submit-content"></a><span data-ttu-id="33133-108">Como enviar conteúdo</span><span class="sxs-lookup"><span data-stu-id="33133-108">How to submit content</span></span>

<span data-ttu-id="33133-109">Para enviar conteúdo à Microsoft, clique no botão **novo envio** no lado superior esquerdo da página envios.</span><span class="sxs-lookup"><span data-stu-id="33133-109">To submit content to Microsoft click the **New submission** button in the top left hand side of the submissions page.</span></span> <span data-ttu-id="33133-110">Um submenu no lado direito da página aparece com a opção de enviar um email, uma URL ou um arquivo.</span><span class="sxs-lookup"><span data-stu-id="33133-110">A flyout on the right side of the page appears with the option to submit either an email, URL, or file.</span></span> 

### <a name="email"></a><span data-ttu-id="33133-111">Email</span><span class="sxs-lookup"><span data-stu-id="33133-111">Email</span></span>
![Exemplo de envio de email](media/submission-flyout-email.PNG)
1. <span data-ttu-id="33133-113">Para enviar um email, selecione **email** e ESPECIFIQUE a **ID da mensagem da rede** de email ou carregue o arquivo de email.</span><span class="sxs-lookup"><span data-stu-id="33133-113">To submit an email, select **email** and specify the email **network message ID** or upload the email file.</span></span> 

2. <span data-ttu-id="33133-114">Especifique o (s) destinatário (s) em relação ao qual você gostaria de executar a verificação de política.</span><span class="sxs-lookup"><span data-stu-id="33133-114">Specify the recipient(s) that you would like to run the policy check against.</span></span> <span data-ttu-id="33133-115">A verificação de política determinará se o email ignorou a verificação devido a políticas de nível de usuário ou locatário.</span><span class="sxs-lookup"><span data-stu-id="33133-115">The policy check will determine if the email bypassed scanning due to user or tenant level policies.</span></span> 

3. <span data-ttu-id="33133-116">Especifique se o email deve ter sido bloqueado ou não.</span><span class="sxs-lookup"><span data-stu-id="33133-116">Specify if the email should have been blocked or not.</span></span> <span data-ttu-id="33133-117">Se o email tiver sido bloqueado, especifique se ele deve ter sido bloqueado como spam, phishing ou malware.</span><span class="sxs-lookup"><span data-stu-id="33133-117">If the email should have been blocked, specify if it should have been blocked as Spam, Phishing, or Malware.</span></span> <span data-ttu-id="33133-118">Se você não tiver certeza de qual tipo pode ser, use a melhor Judgement.</span><span class="sxs-lookup"><span data-stu-id="33133-118">If you are not sure what type it might be, use your best judgement.</span></span>  

* <span data-ttu-id="33133-119">Se o filtro tiver sido ignorado devido às políticas após o envio, você verá informações sobre essa política.</span><span class="sxs-lookup"><span data-stu-id="33133-119">If the filter was bypassed due to policies upon submission, you'll see information about that policy.</span></span>

* <span data-ttu-id="33133-120">Se o filtro não tiver sido ignorado devido a uma ou mais políticas, a verificação será concluída em vários minutos.</span><span class="sxs-lookup"><span data-stu-id="33133-120">If the filter was not bypassed due to one or more policies, the scan will complete in several minutes.</span></span> <span data-ttu-id="33133-121">Você verá informações adicionais sobre o envio clicando no link status.</span><span class="sxs-lookup"><span data-stu-id="33133-121">You'll see additional information about the submission by clicking on the status link.</span></span> <span data-ttu-id="33133-122">Isso inclui os resultados da verificação de política e a veredicto de nova verificação.</span><span class="sxs-lookup"><span data-stu-id="33133-122">This includes the results of the policy check and the rescan verdict.</span></span> <span data-ttu-id="33133-123">Observação isso não executa o email por meio da pilha de filtragem completa do Office 365 ATP novamente, mas executa uma verificação parcial com base em determinados atributos do email, da URL ou do arquivo.</span><span class="sxs-lookup"><span data-stu-id="33133-123">Note this does not run the email through the Office 365 ATP full filtering stack again but runs a partial rescan based on certain attributes of the mail, URL, or file.</span></span> 

4. <span data-ttu-id="33133-124">Clique no botão **Enviar** .</span><span class="sxs-lookup"><span data-stu-id="33133-124">Click the **Submit** button.</span></span>

### <a name="url"></a><span data-ttu-id="33133-125">URL</span><span class="sxs-lookup"><span data-stu-id="33133-125">URL</span></span>
![Exemplo de envio de email](media/submission-url-flyout.png)
1. <span data-ttu-id="33133-127">Para enviar uma URL de \*\*\*\* seleção de URL do submenu.</span><span class="sxs-lookup"><span data-stu-id="33133-127">To submit a URL select **URL** from the flyout.</span></span> <span data-ttu-id="33133-128">Digite a URL completa incluindo o protocolo (**https://**).</span><span class="sxs-lookup"><span data-stu-id="33133-128">Type in the full URL including the protocol (**https://**).</span></span> 

* <span data-ttu-id="33133-129">Se você tiver selecionado o **deve ter sido filtrado**, especifique se a URL é phishing ou malware.</span><span class="sxs-lookup"><span data-stu-id="33133-129">If you selected **Should have been filtered**, specify if the URL is phishing or malware.</span></span>

2. <span data-ttu-id="33133-130">Clique no botão **Enviar** .</span><span class="sxs-lookup"><span data-stu-id="33133-130">Click the **Submit** button.</span></span> 


### <a name="file"></a><span data-ttu-id="33133-131">Arquivo</span><span class="sxs-lookup"><span data-stu-id="33133-131">File</span></span>
![Exemplo de envio de email](media/submission-file-flyout.PNG)
1. <span data-ttu-id="33133-133">Para enviar um arquivo de \*\*\*\* seleção de arquivo do submenu e carregar o arquivo que você deseja verificar.</span><span class="sxs-lookup"><span data-stu-id="33133-133">To submit a file select **File** from the flyout and upload the file you would like to scan.</span></span> 

2. <span data-ttu-id="33133-134">Clique no botão **Enviar** .</span><span class="sxs-lookup"><span data-stu-id="33133-134">Click the **Submit** button.</span></span>


## <a name="related-topics"></a><span data-ttu-id="33133-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="33133-135">Related topics</span></span>

[<span data-ttu-id="33133-136">Office 365 plano avançado de proteção contra ameaças 2</span><span class="sxs-lookup"><span data-stu-id="33133-136">Office 365 Advanced Threat Protection Plan 2</span></span>](office-365-ti.md)
  
[<span data-ttu-id="33133-137">Proteção contra ameaças no Office 365</span><span class="sxs-lookup"><span data-stu-id="33133-137">Protect against threats in Office 365</span></span>](protect-against-threats.md)
  
[<span data-ttu-id="33133-138">Exibir relatórios para a proteção avançada contra ameaças do Office 365</span><span class="sxs-lookup"><span data-stu-id="33133-138">View reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)
  


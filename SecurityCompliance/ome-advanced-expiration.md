---
title: Definir uma data de expiração para email criptografado pela criptografia de mensagem avançada do Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/30/2019
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f87cb016-7876-4317-ae3c-9169b311ff8a
description: Com os recursos avançados de criptografia de mensagens do Office 365 na parte superior da criptografia de mensagens do Office 365 (OME), você pode estender sua segurança de email Configurando uma data de validade por emails por meio de um modelo personalizado com marca.
ms.openlocfilehash: c1fb876724bed970095e950906500ff551d93cee
ms.sourcegitcommit: 8eb3cb4ec45ae0bb75fde249e35c4bc3d263b84f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/30/2019
ms.locfileid: "33506702"
---
# <a name="set-an-expiration-date-for-email-encrypted-by-office-365-advanced-message-encryption"></a><span data-ttu-id="e8e92-103">Definir uma data de expiração para email criptografado pela criptografia de mensagem avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="e8e92-103">Set an expiration date for email encrypted by Office 365 Advanced Message Encryption</span></span>

<span data-ttu-id="e8e92-104">A criptografia de mensagem avançada do Office 365 está disponível na parte superior da criptografia de mensagem do Office 365 em determinadas assinaturas.</span><span class="sxs-lookup"><span data-stu-id="e8e92-104">Office 365 Advanced Message Encryption is available on top of Office 365 Message Encryption in certain subscriptions.</span></span> <span data-ttu-id="e8e92-105">A criptografia avançada de mensagens está incluída no [Microsoft 365 Enterprise E5](https://www.microsoft.com/microsoft-365/enterprise/home), no Office 365 Enterprise E5 e no Office 365 Education a5.</span><span class="sxs-lookup"><span data-stu-id="e8e92-105">Advanced Message Encryption is included in [Microsoft 365 Enterprise E5](https://www.microsoft.com/microsoft-365/enterprise/home), Office 365 Enterprise E5, and Office 365 Education A5.</span></span> <span data-ttu-id="e8e92-106">Se sua organização tiver uma assinatura do Office 365 que não inclua a criptografia de mensagem avançada do Office 365, você poderá comprar a criptografia de mensagem avançada como um complemento com a conformidade E5 do SKU de conformidade avançada.</span><span class="sxs-lookup"><span data-stu-id="e8e92-106">If your organization has an Office 365 subscription that does not include Office 365 Advanced Message Encryption, you can purchase Advanced Message Encryption as an add-on with E5 Compliance of the Advanced Compliance SKU.</span></span>

<span data-ttu-id="e8e92-107">Você pode usar a expiração de mensagens em emails enviados por seus usuários para destinatários externos que usam o portal do OME para acessar emails criptografados.</span><span class="sxs-lookup"><span data-stu-id="e8e92-107">You can use message expiration on emails that your users send to external recipients who use the OME Portal to access encrypted emails.</span></span> <span data-ttu-id="e8e92-108">Você força os destinatários a usar o portal do OME para exibir e responder a emails criptografados enviados pela sua organização usando um modelo personalizado com marca que especifica uma data de expiração no Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e8e92-108">You force recipients to use the OME portal to view and reply to encrypted emails sent by your organization by using a custom branded template that specifies an expiration date in Windows Powershell.</span></span>

<span data-ttu-id="e8e92-109">Como administrador global do O365, quando você aplica a identidade visual da sua empresa para personalizar a aparência das mensagens de email da sua organização do Office 365, você também pode especificar uma expiração para essas mensagens de email.</span><span class="sxs-lookup"><span data-stu-id="e8e92-109">As an O365 global administrator, when you apply your company branding to customize the look of your Office 365 organization's email messages, you can also specify an expiration for these email messages.</span></span> <span data-ttu-id="e8e92-110">Com a criptografia de mensagem avançada do Office 365, você pode criar vários modelos para emails criptografados provenientes da sua organização.</span><span class="sxs-lookup"><span data-stu-id="e8e92-110">With Office 365 Advanced Message Encryption, you can create multiple templates for encrypted emails originating from your organization.</span></span> <span data-ttu-id="e8e92-111">Usando um modelo, você pode controlar por quanto tempo os destinatários têm acesso a emails enviados por seus usuários.</span><span class="sxs-lookup"><span data-stu-id="e8e92-111">Using a template, you can control how long recipients have access to mail sent by your users.</span></span>

<span data-ttu-id="e8e92-112">Quando um usuário final recebe emails com uma data de expiração definida, o usuário vê a data de expiração no email de conteúdo adicional.</span><span class="sxs-lookup"><span data-stu-id="e8e92-112">When an end user receives mail that has an expiration date set, the user sees the expiration date in the wrapper email.</span></span> <span data-ttu-id="e8e92-113">Se um usuário tentar abrir um email expirado, um erro aparecerá no portal do OME.</span><span class="sxs-lookup"><span data-stu-id="e8e92-113">If a user tries to open an expired mail, an error appears in the OME portal.</span></span>

<span data-ttu-id="e8e92-114">Somente emails para destinatários externos são expirados.</span><span class="sxs-lookup"><span data-stu-id="e8e92-114">Only emails to external recipients are expirable.</span></span>

<span data-ttu-id="e8e92-115">Com a criptografia de mensagem avançada do Office 365, sempre que você aplicar a identidade visual personalizada, o Office 365 aplica o wrapper a emails que se ajustam à regra de fluxo de emails para a qual você aplica o modelo.</span><span class="sxs-lookup"><span data-stu-id="e8e92-115">With Office 365 Advanced Message Encryption, any time you apply custom branding, the Office 365 applies the wrapper to email that fits the mail flow rule to which you apply the template.</span></span> <span data-ttu-id="e8e92-116">Além disso, a expiração só poderá ser usada se a identidade visual personalizada for usada.</span><span class="sxs-lookup"><span data-stu-id="e8e92-116">In addition, expiration can only be used if custom branding is used.</span></span>

## <a name="create-a-custom-branding-template-to-force-mail-expiration-by-using-powershell"></a><span data-ttu-id="e8e92-117">Criar um modelo de identidade visual personalizado para forçar a expiração de email usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="e8e92-117">Create a custom branding template to force mail expiration by using PowerShell</span></span>

1. <span data-ttu-id="e8e92-118">[Conecte-se ao PowerShell do Exchange Online](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) usando uma conta com permissões de administrador global em seu locatário do Office 365.</span><span class="sxs-lookup"><span data-stu-id="e8e92-118">[Connect to Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) using an account with global administrator permissions in your Office 365 tenant.</span></span>

2. <span data-ttu-id="e8e92-119">Execute o cmdlet New-OMEConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e8e92-119">Run the New-OMEConfiguration cmdlet.</span></span>

     ```powershell
     New-OMEConfiguration -Identity "Expire in 7 days" ExternalMailExpiryInDays 7
     ```

<span data-ttu-id="e8e92-120">Onde:</span><span class="sxs-lookup"><span data-stu-id="e8e92-120">Where:</span></span>

- <span data-ttu-id="e8e92-121">Identity é o nome do modelo personalizado.</span><span class="sxs-lookup"><span data-stu-id="e8e92-121">Identity is the name of the custom template.</span></span>

- <span data-ttu-id="e8e92-122">ExternalMailExpiryInDays identifica o número de dias que os destinatários poderão manter os emails antes de expirarem.</span><span class="sxs-lookup"><span data-stu-id="e8e92-122">ExternalMailExpiryInDays identifies the number of days you want recipients to be able to keep mail before it expires.</span></span> <span data-ttu-id="e8e92-123">Você pode usar qualquer valor entre 1 e 730 dias.</span><span class="sxs-lookup"><span data-stu-id="e8e92-123">You can use any value between 1 to 730 days.</span></span>

## <a name="more-information-about-office-365-advanced-message-encryption"></a><span data-ttu-id="e8e92-124">Mais informações sobre a criptografia de mensagem avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="e8e92-124">More information about Office 365 Advanced Message Encryption</span></span>

- [<span data-ttu-id="e8e92-125">Criptografia de mensagem avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="e8e92-125">Office 365 Advanced Message Encryption</span></span>](ome-advanced-message-encryption.md)

- [<span data-ttu-id="e8e92-126">Revogar emails criptografados pela criptografia de mensagem avançada do Office 365</span><span class="sxs-lookup"><span data-stu-id="e8e92-126">Revoke email encrypted by Office 365 Advanced Message Encryption</span></span>](revoke-ome-encrypted-mail.md)

- [<span data-ttu-id="e8e92-127">Descrição do serviço de conformidade e política de mensagens</span><span class="sxs-lookup"><span data-stu-id="e8e92-127">Message policy and compliance service description</span></span>](https://docs.microsoft.com/en-us/office365/servicedescriptions/exchange-online-service-description/message-policy-and-compliance)
---
title: Criptografia de dados no OneDrive for Business e no SharePoint Online
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 7/2/2018
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- MET150
ms.assetid: 6501b5ef-6bf7-43df-b60d-f65781847d6c
description: Entenda os elementos básicos de segurança da criptografia de dados no OneDrive for Business e no SharePoint Online.
ms.openlocfilehash: 807ef2a195b5c29e769bd0f6757a0319b154b9d3
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22524707"
---
# <a name="data-encryption-in-onedrive-for-business-and-sharepoint-online"></a><span data-ttu-id="8ad7e-103">Criptografia de dados no OneDrive for Business e no SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="8ad7e-103">Data Encryption in OneDrive for Business and SharePoint Online</span></span>

<span data-ttu-id="8ad7e-104">Entenda os elementos básicos de segurança da criptografia de dados no OneDrive for Business e no SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="8ad7e-104">Understand the basic elements of encryption for data security in OneDrive for Business and SharePoint Online.</span></span>
  
## <a name="overview"></a><span data-ttu-id="8ad7e-105">Visão geral</span><span class="sxs-lookup"><span data-stu-id="8ad7e-105">Overview</span></span>

<span data-ttu-id="8ad7e-p101">O Office 365 é um ambiente altamente seguro, que fornece proteção ampla em várias camadas: segurança física de data center, segurança de rede, segurança de acesso, segurança de aplicativo e segurança de dados. Este artigo aborda especificamente o lado da criptografia em repouso e em trânsito da segurança de dados para OneDrive for Business e SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="8ad7e-p101">Office 365 is a highly secure environment that offers extensive protection in multiple layers: physical data center security, network security, access security, application security, and data security. This article specifically focuses on the in-transit and at-rest encryption side of data security for OneDrive for Business and SharePoint Online.</span></span>
  
<span data-ttu-id="8ad7e-108">Para obter uma descrição de segurança do Office 365 como um todo, consulte [Security in Office 365 White Paper](https://go.microsoft.com/fwlink/p/?LinkId=270895).</span><span class="sxs-lookup"><span data-stu-id="8ad7e-108">For a description of Office 365 security as a whole, see [Security in Office 365 White Paper](https://go.microsoft.com/fwlink/p/?LinkId=270895).</span></span>
  
<span data-ttu-id="8ad7e-109">Assista ao vídeo a seguir para ver como funciona a criptografia de dados.</span><span class="sxs-lookup"><span data-stu-id="8ad7e-109">Watch how data encryption works in the following video.</span></span>
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/dea0dec4-4077-4095-9a32-19b94ea2da4b?autoplay=false]
  
## <a name="encryption-of-data-in-transit"></a><span data-ttu-id="8ad7e-110">Criptografia de dados em trânsito</span><span class="sxs-lookup"><span data-stu-id="8ad7e-110">Encryption of data in transit</span></span>

<span data-ttu-id="8ad7e-111">No OneDrive for Business e no SharePoint Online, há dois cenários em que os dados entram e saem dos data centers.</span><span class="sxs-lookup"><span data-stu-id="8ad7e-111">In OneDrive for Business and SharePoint Online, there are two scenarios in which data enters and exits the datacenters.</span></span>
  
- <span data-ttu-id="8ad7e-p102">**Comunicação do cliente com o servidor** A comunicação com o OneDrive for Business pela Internet usa conexões SSL/TLS. Todas as conexões SSL são estabelecidas por meio de chaves de 2.048 bits.</span><span class="sxs-lookup"><span data-stu-id="8ad7e-p102">**Client communication with the server** Communication to OneDrive for Business across the Internet uses SSL/TLS connections. All SSL connections are established using 2048-bit keys.</span></span> 
    
- <span data-ttu-id="8ad7e-p103">**Movimentação de dados entre data centers** O principal motivo para a movimentação de dados entre data centers se deve à replicação geográfica para habilitar a recuperação de desastres. Por exemplo, os logs de transação e os deltas de armazenamento de blobs do SQL Server passam por esse pipe. Embora esses dados já sejam transmitidos por meio de uma rede privada, eles estarão ainda mais protegidos com a melhor criptografia do mercado.</span><span class="sxs-lookup"><span data-stu-id="8ad7e-p103">**Data movement between datacenters** The primary reason to move data between datacenters is for geo-replication to enable disaster recovery. For instance, SQL Server transaction logs and blob storage deltas travel along this pipe. While this data is already transmitted by using a private network, it is further protected with best-in-class encryption.</span></span> 
    
## <a name="encryption-of-data-at-rest"></a><span data-ttu-id="8ad7e-117">Criptografia de dados em repouso</span><span class="sxs-lookup"><span data-stu-id="8ad7e-117">Encryption of data at rest</span></span>

<span data-ttu-id="8ad7e-118">A criptografia em repouso inclui dois componentes: Criptografia BitLocker no nível do disco e criptografia por arquivo de conteúdo do cliente.</span><span class="sxs-lookup"><span data-stu-id="8ad7e-118">Encryption at rest includes two components: BitLocker disk-level encryption and per-file encryption of customer content.</span></span>
  
<span data-ttu-id="8ad7e-p104">BitLocker será implantado para OneDrive para negócios e SharePoint Online entre o serviço. Criptografia por arquivo também é no OneDrive for Business e no SharePoint Online nos ambientes novo dedicados que são compiladas em tecnologia de multilocatário e de multilocação do Office 365.</span><span class="sxs-lookup"><span data-stu-id="8ad7e-p104">BitLocker is deployed for OneDrive for Business and SharePoint Online across the service. Per-file encryption is also in OneDrive for Business and SharePoint Online in Office 365 multi-tenant and new dedicated environments that are built on multi-tenant technology.</span></span>
  
<span data-ttu-id="8ad7e-p105">Enquanto o BitLocker criptografa todos os dados no disco, a criptografia por arquivo vai ainda mais longe e inclui uma chave de criptografia exclusiva para cada arquivo. Além disso, as atualizações de cada arquivo são criptografadas com uma chave de criptografia própria. Antes de armazená-las, as chaves do conteúdo criptografado são armazenadas em um local físico separado do conteúdo. Todas as etapas dessa criptografia usam a criptografia AES com chaves de 256 bits e estão em conformidade com o padrão FIPS 140-2. O conteúdo criptografado é distribuído para vários contêineres no data center, e cada contêiner tem credenciais exclusivas. Essas credenciais são armazenadas em um local físico separado do conteúdo e das chaves de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="8ad7e-p105">While BitLocker encrypts all data on a disk, per-file encryption goes even further by including a unique encryption key for each file. Further, every update to every file is encrypted using its own encryption key. Before they're stored, the keys to the encrypted content are stored in a physically separate location from the content. Every step of this encryption uses Advanced Encryption Standard (AES) with 256-bit keys and is Federal Information Processing Standard (FIPS) 140-2 compliant. The encrypted content is distributed across a number of containers throughout the datacenter, and each container has unique credentials. These credentials are stored in a separate physical location from either the content or the content keys.</span></span>
  
<span data-ttu-id="8ad7e-127">Para obter informações adicionais sobre a conformidade FIPS 140-2, consulte [a conformidade FIPS 140-2](https://go.microsoft.com/fwlink/?LinkId=517625).</span><span class="sxs-lookup"><span data-stu-id="8ad7e-127">For additional information about FIPS 140-2 compliance, see [FIPS 140-2 Compliance](https://go.microsoft.com/fwlink/?LinkId=517625).</span></span>
  
<span data-ttu-id="8ad7e-p106">Criptografia de nível de arquivo em repouso aproveita o armazenamento de blob para fornecer o crescimento de armazenamento praticamente ilimitada e habilitar a proteção contra sem precedentes. Todo o conteúdo de cliente no OneDrive for Business e SharePoint Onlinewill ser migrados para o armazenamento de blob. Aqui está como esses dados são protegidos:</span><span class="sxs-lookup"><span data-stu-id="8ad7e-p106">File-level encryption at rest takes advantage of blob storage to provide for virtually unlimited storage growth and to enable unprecedented protection. All customer content in OneDrive for Business and SharePoint Onlinewill be migrated to blob storage. Here's how that data is secured:</span></span>
  
1. <span data-ttu-id="8ad7e-p107">todo o conteúdo é criptografado, possivelmente com várias chaves, e distribuído pelo data center. Cada arquivo que será armazenado é dividido em uma ou mais partes, dependendo do respectivo tamanho. Em seguida, cada parte é criptografada por meio de uma chave própria exclusiva. As atualizações são tratadas da mesma maneira: o conjunto de alterações ou deltas enviados por um usuário é dividido em partes ,e cada uma delas é criptografada com uma chave própria.</span><span class="sxs-lookup"><span data-stu-id="8ad7e-p107">All content is encrypted, potentially with multiple keys, and distributed across the datacenter. Each file to be stored is broken into one or more chunks, depending its size. Then, each chunk is encrypted using its own unique key. Updates are handled similarly: the set of changes, or deltas, submitted by a user is broken into chunks, and each is encrypted with its own key.</span></span>
    
2. <span data-ttu-id="8ad7e-p108">Todas as partes (arquivos, partes de arquivos e deltas de atualização) são armazenadas em blobs na nossa BLOB Store. Além disso, elas são distribuídas aleatoriamente em vários contêineres de blob.</span><span class="sxs-lookup"><span data-stu-id="8ad7e-p108">All of these chunks—files, pieces of files, and update deltas—are stored as blobs in our blob store. They also are randomly distributed across multiple blob containers.</span></span>
    
3. <span data-ttu-id="8ad7e-137">O "mapa" usado para remontar o arquivo com os respectivos componentes fica armazenado no banco de dados de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="8ad7e-137">The "map" used to re-assemble the file from its components is stored in the Content Database.</span></span>
    
4. <span data-ttu-id="8ad7e-p109">Cada contêiner de blob tem credenciais próprias e exclusivas por tipo de acesso: leitura, gravação, enumeração e exclusão. Cada conjunto de credenciais é mantido no Repositório de Chaves seguro e atualizado regularmente.</span><span class="sxs-lookup"><span data-stu-id="8ad7e-p109">Each blob container has its own unique credentials per access type (read, write, enumerate, and delete). Each set of credentials is held in the secure Key Store and is regularly refreshed.</span></span>
    
<span data-ttu-id="8ad7e-140">Ou seja, há três tipos diferentes de armazenamento envolvidos na criptografia por arquivo em repouso, cada um deles com uma função distinta:</span><span class="sxs-lookup"><span data-stu-id="8ad7e-140">In other words, there are three different types of stores involved in per-file encryption at rest, each with a distinct function:</span></span>
  
- <span data-ttu-id="8ad7e-p110">o conteúdo é armazenado como blobs criptografados na BLOB Store. A chave de cada parte do conteúdo é criptografada e armazenada separadamente no banco de dados de conteúdo. O conteúdo em si não inclui nenhuma pista sobre como descriptografá-lo.</span><span class="sxs-lookup"><span data-stu-id="8ad7e-p110">Content is stored as encrypted blobs in the blob store. The key to each chunk of content is encrypted and stored separately in the content database. The content itself holds no clue as to how it can be decrypted.</span></span>
    
- <span data-ttu-id="8ad7e-p111">O banco de dados de conteúdo é um banco de dados do SQL Server. Ele contém o mapa necessário para localizar e remontar todos os blobs de conteúdo armazenados na BLOB store, bem como as chaves necessárias para descriptografá-los.</span><span class="sxs-lookup"><span data-stu-id="8ad7e-p111">The Content Database is a SQL Server database. It holds the map required to locate and reassemble all of the content blobs held in the blob store as well as the keys needed to decrypt those blobs.</span></span>
    
<span data-ttu-id="8ad7e-p112">Todos os três componentes de armazenamento (a BLOB store, o banco de dados de conteúdo e o repositório de chaves) são fisicamente separados. As informações contidas nesses componentes por si só não são utilizáveis. Eles fornecem um nível de segurança inigualável. Sem acesso aos três componentes, é impossível recuperar as chaves das partes, descriptografar as chaves para torná-las utilizáveis, associar as chaves às respectivas partes, descriptografar qualquer parte ou reconstruir um documento com as partes integrantes.</span><span class="sxs-lookup"><span data-stu-id="8ad7e-p112">Each of these three storage components—the blob store, the Content Database, and the Key Store—is physically separate. The information held in any one of the components is unusable on its own. This provides an unprecedented level of security. Without access to all three it is impossible to retrieve the keys to the chunks, decrypt the keys to make them usable, associate the keys with their corresponding chunks, decrypt any chunk, or reconstruct a document from its constituent chunks.</span></span>
  


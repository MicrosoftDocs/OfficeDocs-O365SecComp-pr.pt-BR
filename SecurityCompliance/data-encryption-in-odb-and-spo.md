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
# <a name="data-encryption-in-onedrive-for-business-and-sharepoint-online"></a>Criptografia de dados no OneDrive for Business e no SharePoint Online

Entenda os elementos básicos de segurança da criptografia de dados no OneDrive for Business e no SharePoint Online.
  
## <a name="overview"></a>Visão geral

O Office 365 é um ambiente altamente seguro, que fornece proteção ampla em várias camadas: segurança física de data center, segurança de rede, segurança de acesso, segurança de aplicativo e segurança de dados. Este artigo aborda especificamente o lado da criptografia em repouso e em trânsito da segurança de dados para OneDrive for Business e SharePoint Online.
  
Para obter uma descrição de segurança do Office 365 como um todo, consulte [Security in Office 365 White Paper](https://go.microsoft.com/fwlink/p/?LinkId=270895).
  
Assista ao vídeo a seguir para ver como funciona a criptografia de dados.
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/dea0dec4-4077-4095-9a32-19b94ea2da4b?autoplay=false]
  
## <a name="encryption-of-data-in-transit"></a>Criptografia de dados em trânsito

No OneDrive for Business e no SharePoint Online, há dois cenários em que os dados entram e saem dos data centers.
  
- **Comunicação do cliente com o servidor** A comunicação com o OneDrive for Business pela Internet usa conexões SSL/TLS. Todas as conexões SSL são estabelecidas por meio de chaves de 2.048 bits. 
    
- **Movimentação de dados entre data centers** O principal motivo para a movimentação de dados entre data centers se deve à replicação geográfica para habilitar a recuperação de desastres. Por exemplo, os logs de transação e os deltas de armazenamento de blobs do SQL Server passam por esse pipe. Embora esses dados já sejam transmitidos por meio de uma rede privada, eles estarão ainda mais protegidos com a melhor criptografia do mercado. 
    
## <a name="encryption-of-data-at-rest"></a>Criptografia de dados em repouso

A criptografia em repouso inclui dois componentes: Criptografia BitLocker no nível do disco e criptografia por arquivo de conteúdo do cliente.
  
BitLocker será implantado para OneDrive para negócios e SharePoint Online entre o serviço. Criptografia por arquivo também é no OneDrive for Business e no SharePoint Online nos ambientes novo dedicados que são compiladas em tecnologia de multilocatário e de multilocação do Office 365.
  
Enquanto o BitLocker criptografa todos os dados no disco, a criptografia por arquivo vai ainda mais longe e inclui uma chave de criptografia exclusiva para cada arquivo. Além disso, as atualizações de cada arquivo são criptografadas com uma chave de criptografia própria. Antes de armazená-las, as chaves do conteúdo criptografado são armazenadas em um local físico separado do conteúdo. Todas as etapas dessa criptografia usam a criptografia AES com chaves de 256 bits e estão em conformidade com o padrão FIPS 140-2. O conteúdo criptografado é distribuído para vários contêineres no data center, e cada contêiner tem credenciais exclusivas. Essas credenciais são armazenadas em um local físico separado do conteúdo e das chaves de conteúdo.
  
Para obter informações adicionais sobre a conformidade FIPS 140-2, consulte [a conformidade FIPS 140-2](https://go.microsoft.com/fwlink/?LinkId=517625).
  
Criptografia de nível de arquivo em repouso aproveita o armazenamento de blob para fornecer o crescimento de armazenamento praticamente ilimitada e habilitar a proteção contra sem precedentes. Todo o conteúdo de cliente no OneDrive for Business e SharePoint Onlinewill ser migrados para o armazenamento de blob. Aqui está como esses dados são protegidos:
  
1. todo o conteúdo é criptografado, possivelmente com várias chaves, e distribuído pelo data center. Cada arquivo que será armazenado é dividido em uma ou mais partes, dependendo do respectivo tamanho. Em seguida, cada parte é criptografada por meio de uma chave própria exclusiva. As atualizações são tratadas da mesma maneira: o conjunto de alterações ou deltas enviados por um usuário é dividido em partes ,e cada uma delas é criptografada com uma chave própria.
    
2. Todas as partes (arquivos, partes de arquivos e deltas de atualização) são armazenadas em blobs na nossa BLOB Store. Além disso, elas são distribuídas aleatoriamente em vários contêineres de blob.
    
3. O "mapa" usado para remontar o arquivo com os respectivos componentes fica armazenado no banco de dados de conteúdo.
    
4. Cada contêiner de blob tem credenciais próprias e exclusivas por tipo de acesso: leitura, gravação, enumeração e exclusão. Cada conjunto de credenciais é mantido no Repositório de Chaves seguro e atualizado regularmente.
    
Ou seja, há três tipos diferentes de armazenamento envolvidos na criptografia por arquivo em repouso, cada um deles com uma função distinta:
  
- o conteúdo é armazenado como blobs criptografados na BLOB Store. A chave de cada parte do conteúdo é criptografada e armazenada separadamente no banco de dados de conteúdo. O conteúdo em si não inclui nenhuma pista sobre como descriptografá-lo.
    
- O banco de dados de conteúdo é um banco de dados do SQL Server. Ele contém o mapa necessário para localizar e remontar todos os blobs de conteúdo armazenados na BLOB store, bem como as chaves necessárias para descriptografá-los.
    
Todos os três componentes de armazenamento (a BLOB store, o banco de dados de conteúdo e o repositório de chaves) são fisicamente separados. As informações contidas nesses componentes por si só não são utilizáveis. Eles fornecem um nível de segurança inigualável. Sem acesso aos três componentes, é impossível recuperar as chaves das partes, descriptografar as chaves para torná-las utilizáveis, associar as chaves às respectivas partes, descriptografar qualquer parte ou reconstruir um documento com as partes integrantes.
  


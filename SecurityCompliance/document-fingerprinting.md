---
title: Impressão Digital de Documento
ms.author: stephow
author: stephow-msft
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
search.appverid: MET150
ms.service: exchange-online
localization_priority: Normal
ms.assetid: 1e0c579c-26e0-462a-a1b0-d7506dfe05fa
description: Os operadores de informações de sua organização lidam com vários tipos de informações confidenciais durante um dia típico. A impressão digital de documento facilita a proteção dessas informações por meio da identificação de formulários padrão usados em toda a organização. Este tópico descreve os conceitos por trás da impressão digital de documento e como criar um usando o PowerShell.
ms.openlocfilehash: 20b9f59902c52d347e7c439cb6f380ee9fd4a30e
ms.sourcegitcommit: 48fa456981b5c52ab8aeace173c8366b9f36723b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/28/2019
ms.locfileid: "30341282"
---
# <a name="document-fingerprinting"></a>Impressão Digital de Documento

Os operadores de informações de sua organização lidam com vários tipos de informações confidenciais durante um dia típico. No centro de &amp; conformidade de segurança, a impressão digital de documentos facilita a proteção dessas informações identificando formulários padrão que são usados em toda a organização. Este tópico descreve os conceitos por trás da impressão digital de documento e como criar um usando o PowerShell.
  
## <a name="basic-scenario-for-document-fingerprinting"></a>Cenário básico da Impressão Digital de Documento

A impressão digital de documento é um recurso de prevenção contra perda de dados (DLP) que converte um formulário padrão em um tipo de informação confidencial, que você pode usar nas regras de suas políticas de DLP. Por exemplo, você pode criar uma impressão digital de documento com base em um modelo de patente em branco e, em seguida, criar uma política de DLP que detecta e bloqueia todos os modelos de patente de saída com conteúdo confidencial preenchido. Opcionalmente, você pode configurar [dicas de política](use-notifications-and-policy-tips.md) para notificar os remetentes de que eles podem estar enviando informações confidenciais, e o remetente deve verificar se os destinatários estão qualificados para receber as patentes. Esse processo funciona com qualquer formulário baseado em texto usado em sua organização. Exemplos adicionais de formulários que você pode carregar incluem: 
  
- Formulários governamentais
    
- Formulários compatíveis com a Lei americana HIPAA (Health Insurance Portability Accountability Act, Lei de responsabilidade sobre portabilidade de seguro saúde)
    
- Formulários de informação sobre funcionários para departamentos de Recursos Humanos
    
- Formulários personalizados criados especificamente para sua organização
    
O ideal é que sua organização já tenha uma prática de negócios estabelecida de usar certos formulários para transmitir informações confidenciais. Após carregar um formulário vazio para ser convertido em uma impressão digital de documento e configurar uma política correspondente, a DLP detecta qualquer documento no email de saída que corresponde a essa impressão digital.
  
## <a name="how-document-fingerprinting-works"></a>Funcionamento da Impressão Digital de Documento

Você provavelmente já adivinhou que os documentos não têm impressões digitais reais, mas o nome ajuda a explicar o recurso. Da mesma forma que as impressões digitais de uma pessoa têm padrões exclusivos, os documentos têm padrões do Word exclusivos. Quando você carrega um arquivo, a DLP identifica o padrão de palavra exclusivo no documento, cria uma impressão digital de documento com base nesse padrão e usa essa impressão digital de documento para detectar documentos de saída que contenham o mesmo padrão. É por isso que carregar um formulário ou modelo cria o tipo mais eficaz de impressão digital de documento. Todos os usuários que preenchem um formulário usam o mesmo conjunto de palavras original e, em seguida, adicionam suas próprias palavras ao documento. Desde que o documento de saída não esteja protegido por senha e que contenha todo o texto do formulário original, a DLP pode determinar se o documento corresponde à impressão digital de documento.
  
O exemplo a seguir mostra o que acontecerá se você criar uma impressão digital de documento com base em um modelo de patente, mas você pode usar qualquer formulário como base para a criação de uma impressão digital de documento.
  
**Exemplo de um documento de patente correspondente a uma impressão digital de documento de um modelo de patente**

![Document_Fingerprinting_diagram. png](media/Document_Fingerprinting_diagram.png)
  
O modelo de patente contém os campos em branco "título da patente", "inVentrs" e "Descrição" e as descrições de cada um desses campos, que é o padrão da palavra. Quando você carrega o modelo de patente original, ele está em um dos tipos de arquivo com suporte e em texto sem formatação. A DLP converte esse padrão de Word em uma impressão digital de documento, que é um pequeno arquivo XML Unicode contendo um valor de hash exclusivo representando o texto original e a impressão digital é salva como uma classificação de dados no Active Directory. (Como medida de segurança, o próprio documento original não é armazenado no serviço; somente o valor de hash é armazenado e o documento original não pode ser reconstruído com base no valor de hash.) A impressão digital de patente torna-se um tipo de informação confidencial que você pode associar a uma política de DLP. Depois de associar a impressão digital com uma política de DLP, a DLP detecta qualquer email de saída contendo documentos que correspondam à impressão digital de patente e lidam com eles de acordo com a política da sua organização. 

Por exemplo, você pode querer configurar uma política de DLP que impede que funcionários regulares enviem mensagens de saída contendo patentes. A DLP usará a impressão digital de patente para detectar patentes e bloquear esses emails. Como alternativa, você pode querer permitir que seu departamento jurídico seja capaz de enviar patentes para outras organizações, pois tem uma necessidade comercial para fazê-lo. Você pode permitir que departamentos específicos enviem informações confidenciais criando exceções para esses departamentos em sua política de DLP ou pode permitir que eles substituam uma dica de política com uma justificativa de negócios.
  
### <a name="supported-file-types"></a>Tipos de arquivo com suporte

A impressão digital de documento oferece suporte aos mesmos tipos de arquivo suportados nas regras de fluxo de emails (também conhecidas como regras de transporte). Para obter uma lista de tipos de arquivo com suporte, confira [tipos de arquivo com suporte para inspeção de conteúdo de regra de fluxo de email](https://docs.microsoft.com/en-us/exchange/security-and-compliance/mail-flow-rules/inspect-message-attachments#supported-file-types-for-mail-flow-rule-content-inspection). Uma observação rápida sobre os tipos de arquivo: nem as regras de fluxo de emails e a impressão digital de documentos dão suporte ao tipo de arquivo. dotx, que pode ser confuso porque é um arquivo de modelo no Word. Quando você vir a palavra "modelo" neste e em outros tópicos de impressão digital de documento, ela se refere a um documento que você estabeleceu como um formulário padrão, e não o tipo de arquivo de modelo.
  
#### <a name="limitations-of-document-fingerprinting"></a>Limitações da impressão digital de documento

A impressão digital de documento não detectará informações confidenciais nos seguintes casos:
  
- Arquivos protegidos por senha
    
- Arquivos que contenham somente imagens
    
- Documentos que não contenham todo o texto do formulário original usado para criar a impressão digital de documento
    
## <a name="use-powershell-to-create-a-classification-rule-package-based-on-document-fingerprinting"></a>Usar o PowerShell para criar um pacote de regras de classificação com base na impressão digital de documento

Observe que, no momento, você pode criar uma impressão digital de documento usando o &amp; PowerShell no centro de conformidade de segurança. Para se conectar, confira [conectar-se ao PowerShell do centro de conformidade do & de segurança do Office 365](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).

A DLP usa pacotes de regras de classificação para detectar conteúdo confidencial. Para criar um pacote de regras de classificação com base em uma impressão digital de documento, use os cmdlets **New-DlpFingerprint** e **New-DlpSensitiveInformationType** . Como os resultados de **New-DlpFingerprint** não são armazenados fora da regra de classificação de dados, você sempre executa **New-DlpFingerprint** e **New-DlpSensitiveInformationType** ou **set-DlpSensitiveInformationType** no mesmo Sessão do PowerShell. O exemplo a seguir cria uma nova impressão digital de documento com base no arquivo C:\My Documents\Contoso Employee template. docx. Você armazena a nova impressão digital como uma variável para que possa usá-la com o cmdlet **New-DlpSensitiveInformationType** na mesma sessão do PowerShell. 
  
```
$Employee_Template = Get-Content "C:\My Documents\Contoso Employee Template.docx" -Encoding byte -ReadCount 0
$Employee_Fingerprint = New-DlpFingerprint -FileData $Employee_Template -Description "Contoso Employee Template"
```

Este exemplo cria uma nova regra de classificação de dados chamada "Contoso Employee Confidential" que usa as impressões digitais de documento do arquivo C:\My Documents\Contoso Customer Information Form.docx.
  
```
$Employee_Template = Get-Content "C:\My Documents\Contoso Customer Information Form.docx" -Encoding byte -ReadCount 0
$Customer_Fingerprint = New-DlpFingerprint -FileData $Customer_Form -Description "Contoso Customer Information Form"
New-DlpSensitiveInformationType -Name "Contoso Customer Confidential" -Fingerprints $Customer_Fingerprint -Description "Message contains Contoso customer information." 
```

Agora você pode usar o cmdlet **Get-DlpSensitiveInformationType** para localizar todos os pacotes de regras de classificação de dados DLP e, neste exemplo, "confidencial do cliente da Contoso" é parte da lista pacotes de classificação de dados. 
  
Por fim, adicione o pacote de regras de classificação de dados "contoso Customer Confidential" a uma política &amp; de DLP no centro de conformidade de segurança. Este exemplo adiciona uma regra a uma política de DLP existente chamada "ConfidentialPolicy".

```
New-DlpComplianceRule -Name "ContosoConfidentialRule" -Policy "ConfidentialPolicy" -ContentContainsSensitiveInformation @{Name="Contoso Customer Confidential"} -BlockAccess $True
```

Você também pode usar o pacote de regras de classificação de dados nas regras de fluxo de email no Exchange Online, conforme mostrado no exemplo a seguir. Para executar este comando, primeiro você precisa [se conectar ao PowerShell do Exchange Online](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell). Observe também que leva tempo para que o pacote de regras seja sincronizado do &amp; centro de conformidade de segurança para o centro de administração do Exchange.
  
```
New-TransportRule -Name "Notify :External Recipient Contoso confidential" -NotifySender NotifyOnly -Mode Enforce -SentToScope NotInOrganization -MessageContainsDataClassification @{Name=" Contoso Customer Confidential"}

```

A DLP agora detecta documentos que correspondem à impressão digital de documento. docx do formulário cliente da contoso.
  
Para obter informações sobre sintaxe e parâmetros, consulte:

- [New-DlpFingerprint](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/New-DlpFingerprint)
- [New-DlpSensitiveInformationType](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/New-DlpSensitiveInformationType)
- [Remove-DlpSensitiveInformationType](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/Remove-DlpSensitiveInformationType)
- [Set-DlpSensitiveInformationType](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/Set-DlpSensitiveInformationType)
- [Get-DlpSensitiveInformationType](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/Get-DlpSensitiveInformationType)

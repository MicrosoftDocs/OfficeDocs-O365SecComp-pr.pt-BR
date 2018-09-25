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
description: Os operadores de informações em sua organização lidar com muitos tipos de informações confidenciais durante um dia normal. Impressão digital de documento facilita proteger essas informações identificando formulários padrão que são usados em toda a organização. Este tópico descreve os conceitos por trás de impressão digital de documentos e como criar um usando o PowerShell.
ms.openlocfilehash: c33d7412fe4774b74efcd0928df4c99c7bcbb626
ms.sourcegitcommit: ede6230c2df398dc0a633e8f32ee0bfede0d5142
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/25/2018
ms.locfileid: "25002644"
---
# <a name="document-fingerprinting"></a>Impressão Digital de Documento

Os operadores de informações em sua organização lidar com muitos tipos de informações confidenciais durante um dia normal. Na segurança &amp; Centro de conformidade, a impressão digital de documento torna mais fácil para proteger essas informações identificando formulários padrão que são usados em toda a organização. Este tópico descreve os conceitos por trás de impressão digital de documentos e como criar um usando o PowerShell.
  
## <a name="basic-scenario-for-document-fingerprinting"></a>Cenário básico da Impressão Digital de Documento

Impressão digital de documento é um recurso de prevenção de perda de dados (DLP) que converte um formulário padrão em um tipo de informação confidencial, que você pode usar as regras de suas políticas DLP. Por exemplo, você pode criar uma impressão digital de documento baseada em um modelo de patente em branco e, em seguida, criar uma política de DLP que detecta e bloqueia todos os modelos de patentes saídos com conteúdo confidencial preenchidos. Opcionalmente, você pode configurar [dicas de política](use-notifications-and-policy-tips.md) para notificar os remetentes que pode estar enviando informações confidenciais e o remetente deve verificar se os destinatários estão qualificados para receber os patentes. Esse processo funciona com qualquer formulários baseados em texto utilizados na organização. Exemplos adicionais de formulários que você pode carregar incluem: 
  
- Formulários governamentais
    
- Formulários compatíveis com a Lei americana HIPAA (Health Insurance Portability Accountability Act, Lei de responsabilidade sobre portabilidade de seguro saúde)
    
- Formulários de informação sobre funcionários para departamentos de Recursos Humanos
    
- Formulários personalizados criados especificamente para sua organização
    
Idealmente, sua organização já tiver uma prática de negócios estabelecidos de usar determinados formulários para transmitir informações confidenciais. Depois de carregar um formulário vazio para ser convertido em uma impressão digital de documento e definir uma política correspondente, a DLP detecta quaisquer documentos em mensagens de saída que correspondem a esse impressão digital.
  
## <a name="how-document-fingerprinting-works"></a>Funcionamento da Impressão Digital de Documento

Você provavelmente adivinhou que documentos não têm impressões digitais reais, mas o nome ajuda que explicam o recurso. Da mesma maneira que impressões digitais de uma pessoa tenham padrões únicos, documentos têm padrões de word exclusivo. Quando você carrega um arquivo, DLP identifica o padrão do word exclusivo no documento, cria uma impressão digital de documento com base em com o padrão e usa essa impressão digital de documento para detectar documentos de saída que contém o mesmo padrão encontrado. Por isso, o carregamento de um formulário ou modelo cria o tipo mais eficiente de impressão digital de documento. Todas as pessoas que preenche um formulário usa o mesmo conjunto original de palavras e adiciona seu próprio palavras ao documento. Desde que o documento de saída não está protegido por senha e contém todo o texto do formulário original, DLP pode determinar se o documento corresponde a impressão digital de documento.
  
O exemplo a seguir mostra o que acontecerá se você criar uma impressão digital de documento com base em um modelo de patente, mas você pode usar qualquer formulário como base para a criação de uma impressão digital de documento.
  
**Exemplo de um documento de patente correspondente a uma impressão digital de documento de um modelo de patente**

![Document_Fingerprinting_diagram.PNG](media/Document_Fingerprinting_diagram.png)
  
O modelo de patente contém os campos em branco "Patente title", "Inventores," e "Descrição" e descrições para cada um desses campos — que é o padrão do word. Quando você carrega o modelo original de patente, é em um dos tipos de arquivo com suporte e em texto sem formatação. Converte DLP este padrão do word em uma impressão digital de documento, que é um pequeno Unicode XML que contém um valor de hash exclusivo que representa o texto original e a impressão digital de arquivo é salvo como uma classificação de dados no Active Directory. (Como uma medida de segurança, o documento original em si não é armazenado no serviço; apenas o valor de hash é armazenado e o documento original não pode ser reconstruído a partir do valor de hash). A impressão digital de patente, em seguida, torna-se um tipo de informações confidenciais que você pode associar uma política de DLP. Depois de associar a impressão digital com uma política de DLP, DLP detecta quaisquer emails de saída que contém documentos que correspondem a impressão digital de patente e lida com eles, de acordo com a política da sua organização. 

Por exemplo, convém definir uma política DLP que impede que os funcionários regulares enviem mensagens de saída contendo patentes. DLP usará a impressão digital de patente para detectar patentes e bloquear esses emails. Como alternativa, talvez você queira permitir que o seu departamento jurídico para poder enviar patentes para outras organizações, porque ele tem uma empresa precisam para fazer isso. Você pode permitir que os departamentos específicos enviar informações confidenciais, criando exceções para os departamentos em sua política DLP ou você pode permitir que eles substituir uma dica de política com uma justificativa comercial.
  
### <a name="supported-file-types"></a>Tipos de arquivo com suporte

Impressão digital de documento suporta os mesmos tipos de arquivo suportados no regras de transporte. Para obter uma lista dos tipos de arquivo com suporte, consulte [tipos de arquivo suportados para inspeção conteúdo de regra de fluxo de email](https://docs.microsoft.com/en-us/exchange/security-and-compliance/mail-flow-rules/inspect-message-attachments#supported-file-types-for-mail-flow-rule-content-inspection). Uma observação rápida sobre tipos de arquivo: nem regras de transporte nem a impressão digital de documento suporta o tipo de arquivo. dotx, que pode ser confuso, pois é um arquivo de modelo no Word. Quando você vir a palavra "modelo" neste e em outros tópicos de impressão digital de documentos, se refere a um documento que você tenha estabelecido como um formulário padrão, não é o tipo de arquivo do modelo.
  
#### <a name="limitations-of-document-fingerprinting"></a>Limitações da impressão digital de documento

Impressão digital de documento não detectará informações confidenciais nos seguintes casos:
  
- Arquivos protegidos por senha
    
- Arquivos que contenham somente imagens
    
- Documentos que não contenham todo o texto do formulário original usado para criar a impressão digital de documento
    
## <a name="use-powershell-to-create-a-classification-rule-package-based-on-document-fingerprinting"></a>Usar o PowerShell para criar um pacote de regras de classificação com base na impressão digital de documentos

Observe que você pode criar uma impressão digital de documento atualmente apenas usando o PowerShell na segurança &amp; Centro de conformidade. Para se conectar, consulte [Connect to Office 365 Security & PowerShell do Centro de conformidade](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).

DLP usa pacotes de regras de classificação para detectar conteúdo confidencial. Para criar um pacote de regras de classificação com base na impressão digital de documento, use os cmdlets **New-DlpFingerprint** e **New-DlpSensitiveInformationType** . Como os resultados de **New-DlpFingerprint** não são armazenados fora a regra de classificação de dados, você sempre são executados **New-DlpFingerprint** e **New-DlpSensitiveInformationType** ou **Set-DlpSensitiveInformationType** na mesma Sessão do PowerShell. O exemplo a seguir cria uma nova impressão de documentos baseada no arquivo C:\My Documents\Contoso funcionário Template. Você pode armazenar a impressão digital de nova como uma variável para que possa usá-lo com o cmdlet **New-DlpSensitiveInformationType** na mesma sessão do PowerShell. 
  
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

Agora você pode usar o cmdlet **Get-DlpSensitiveInformationType** para localizar todos os pacotes de regras de classificação para dados DLP e, neste exemplo, "Contoso Customer Confidential" faz parte da lista de pacotes de regras de classificação de dados. 
  
Finalmente, adicione o pacote de regras de classificação de dados "Contoso Customer Confidential" a uma política DLP na segurança &amp; Centro de conformidade. Este exemplo adiciona uma regra de uma política de DLP existente chamado "ConfidentialPolicy".

```
New-DlpComplianceRule -Name "ContosoConfidentialRule" -Policy "ConfidentialPolicy" -ContentContainsSensitiveInformation @{Name="Contoso Customer Confidential"} -BlockAccess $True
```

Você também pode usar o pacote de regras de classificação de dados em regras de transporte no Exchange Online, conforme mostrado no exemplo a seguir. Para executar esse comando, você primeiro precisa [Connect to Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell). Observe também que leva tempo para o pacote de regra sincronizar a partir de segurança &amp; Centro de conformidade para o Centro de administração do Exchange.
  
```
New-TransportRule -Name "Notify :External Recipient Contoso confidential" -NotifySender NotifyOnly -Mode Enforce -SentToScope NotInOrganization -MessageContainsDataClassification @{Name=" Contoso Customer Confidential"}

```

DLP agora detecta documentos que correspondem a impressão digital de documento Contoso Customer Form.
  
Para obter informações de sintaxe e parâmetros, consulte:

- [New-DlpFingerprint](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/New-DlpFingerprint)
- [New-DlpSensitiveInformationType](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/New-DlpSensitiveInformationType)
- [Remove-DlpSensitiveInformationType](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/Remove-DlpSensitiveInformationType)
- [Set-DlpSensitiveInformationType](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/Set-DlpSensitiveInformationType)
- [Get-DlpSensitiveInformationType](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/Get-DlpSensitiveInformationType)

---
title: Práticas recomendadas para a configuração do EOP
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: faf1efd1-3b0c-411a-804d-17f37292eac0
description: Siga estas práticas recomendadas para a EOP (Proteção do Exchange Online) a fim de evitar erros comuns de configuração e obter êxito.
ms.openlocfilehash: ef58e2cd5a3ffdbbeb02124442c355974d174073
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027268"
---
# <a name="best-practices-for-configuring-eop"></a>Práticas recomendadas para a configuração do EOP
  
Siga estas práticas recomendadas para a EOP (Proteção do Exchange Online) a fim de evitar erros comuns de configuração e obter êxito. Recomendamos usar as configurações padrão como regra geral. Este tópico supõe que você já concluiu o processo de configuração. Se ainda não realizou a configuração da EOP, confira [Configurar seu serviço EOP](set-up-your-eop-service.md).
  
## <a name="use-a-test-domain"></a>Usar um domínio de teste

Recomendamos que você use um domínio de teste, subdomínio ou domínio de baixo volume para testar os recursos de serviço antes de implementá-los nos seus domínios com maior volume de produção.
  
## <a name="synchronize-recipients"></a>Sincronizar destinatários

Se sua organização tiver contas de usuário existentes em um ambiente local do Active Directory, você poderá sincronizar essas contas com o Azure Active Directory na nuvem. Recomendamos o uso da sincronização de diretórios. Para saber mais sobre os benefícios de usar a sincronização de diretórios e ver as etapas para configurá-la, confira [Gerenciar usuários de email no EOP](manage-mail-users-in-eop.md).
  
## <a name="spf-record-customization-to-help-prevent-spoofing"></a>Personalização de registro SPF para ajudar a evitar falsificação

Quando você configura o EOP, você adicionou um registro de SPF (estrutura de política do remetente) para EOP para seus registros DNS. O registro SPF ajuda a evitar a falsificação. Para obter mais informações sobre como um registro SPF impede a falsificação e como você pode adicionar seus endereços IP no local para o registro SPF, consulte [Configurar SPF no Office 365 para ajudar a impedir a falsificação](../set-up-spf-in-office-365-to-help-prevent-spoofing.md). 
  
## <a name="set-anti-spam-options"></a>Definir as opções de antispam

Gerenciar sua conexão configurações de filtro, adicionando endereços IP ao IP permitidos e listas de bloqueios de IP e selecionando a opção **Habilitar lista segura** , que deve reduzir o número de falsos positivos (BOM email que é classificada como spam) receber. Saiba mais em [Configure a política de filtro de conexão](../configure-the-connection-filter-policy.md). Mais configurações de spam que se aplicam a toda a organização, dê uma olhada em [como ajudar a garantir que uma mensagem não foi marcada como spam](https://go.microsoft.com/fwlink/p/?LinkId=534224) ou [Bloquear e-mail de spam com o filtro de spam do Office 365 para evitar problemas de negativos falsos](https://go.microsoft.com/fwlink/p/?LinkId=534225). Essas são úteis se você tiver o controle de nível de administrador e você deseja evitar falsos positivos ou falsos negativos.
  
Gerencie seus filtros de conteúdo revisando e, opcionalmente, alterando as configurações padrão. Por exemplo, você pode alterar a ação para o que acontece às mensagens de spam detectado. Se desejar buscar uma abordagem agressiva para filtragem de spam, você pode configurar opções de filtragem de spam avançada. Recomendamos que você teste essas opções primeiro antes implementá-las em seu ambiente de produção (ligando-los) é recomendável que as organizações que se preocupam com phishing ativem o **registro SPF: falha grave** opção. Saiba mais em [configurar suas políticas de filtro de spam](../configure-your-spam-filter-policies.md) e [Opções de filtragem de spam avançada](../advanced-spam-filtering-asf-options.md).
  
> [!IMPORTANT]
> Se você estiver usando a ação de filtro de conteúdo padrão, **Move a mensagem para a pasta Lixo eletrônico**, para garantir que esta ação funcionará com caixas de correio local, você deve configurar as regras de fluxo de correio do Exchange, também chamadas de regras de transporte, em seu local servidores para detectar os cabeçalhos de spam adicionados pelo EOP. Para obter detalhes, consulte [Certifique-se de que o spam é roteado para a pasta de lixo eletrônico de cada usuário](../ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md). 
  
Recomendamos que você revise o [anti-spam protection FAQ](../anti-spam-protection-faq.md), incluindo a saída endereçamento melhores práticas seção, que ajudará a garantir que as mensagens de saída seja entregue.
  
Você pode enviar falsos negativos (spam) e falsos positivos (não-spam) para a Microsoft para análise de várias maneiras. Para obter detalhes, consulte o [envio de spam, não spam e mensagens de golpes de phishing à Microsoft para análise](../submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md).
  
## <a name="set-anti-malware-options"></a>Definir opções de antimalware

Revisar e ajustar suas configurações de filtro de malware em center(EAC) de administração do Exchange. Saiba mais em [Configurar políticas de antimalware](../configure-anti-malware-policies.md). É recomendável também ler sobre outras perguntas frequentes e respostas referentes a proteção antimalware no nosso [Anti-malware protection FAQ ](../anti-malware-protection-faq-eop.md).
  
Se estiver preocupado com arquivos executáveis que contêm malware, poderá criar uma regra de fluxo de emails do Exchange para bloquear os anexos de email que incluam conteúdo executável. Siga as etapas em [Como reduzir ameaças de malware através de proteção online do Exchange de bloqueio de anexos de arquivo](https://support.microsoft.com/kb/2959596) para bloquear os tipos de arquivo listados no tópico "Tipos de arquivos executáveis para inspeção de regras de transporte", em [Use mail flow rules to inspect message attachments](http://technet.microsoft.com/library/874d1c78-a8ec-4938-b388-d3208c2fa971.aspx).
  
Você pode usar o Filtro de Tipos de Anexos Comuns no EAC. Escolha **proteção** \> **filtros de malware**. Você pode criar um regra de fluxo de emails do Exchange, também conhecida como regra de transporte, que bloqueia os anexos de email que incluem conteúdo executável. 
  
Para aumentar a proteção, recomendamos também que você use regras de fluxo de emails para bloquear algumas ou todas as seguintes extensões: ade, adp, ani, bas, bat, chm, cmd, com, cpl, crt, hlp, ht, hta, inf, ins, isp, job, js, jse, lnk, mda, mdb, mde, mdz, msc, msi, msp, mst, pcd, reg, scr, sct, shs, url, vb, vbe, vbs, wsc, wsf, wsh. Isso pode ser feito usando a condição **Qualquer extensão de arquivo de anexo que inclua essas palavras**. 
  
Os administradores e usuários finais podem enviar um malware que passou por filtros anteriores ou enviar um arquivo que você acha que foi identificado incorretamente como malware, enviando-o para a Microsoft para análise. Para saber mais, confira [Submitting malware and non-malware to Microsoft for analysis](../submitting-malware-and-non-malware-to-microsoft-for-analysis.md).
  
## <a name="create-mail-flow-rules"></a>Criar regras de fluxo de emails

Crie regras de fluxo de emails, também chamadas de regras de transporte ou filtros personalizados, para atender às suas necessidades de negócios.
  
Ao implementar uma nova regra à produção, selecione um dos modos de teste primeiro para ver o efeito da regra. Quando tiver a certeza de que a regra está funcionando da maneira pretendida, altere o modo de regra para **Forçar**.
  
Ao implementar novas regras, considere adicionar outras ações de **Gerar Relatório de Incidente** para monitorar a regra em ação. 
  
Se estiver configurando uma implantação híbrida, com parte da organização no local e parte no Office 365, poderá criar regras que se apliquem a toda a empresa. Para fazer isso, use as condições que estão disponíveis no local e no Office 365. Embora a maioria das condições esteja disponível para ambas as implantações, há um pequeno conjunto específico para um determinado cenário de implantação. Saiba mais em [Mail flow or Transport rules](http://technet.microsoft.com/library/743bd525-0ca2-426d-b76c-b4a052bc8886.aspx).
  
Se desejar inspecionar anexos de mensagens de email em trânsito na sua organização, você poderá fazê-lo configurando regras de fluxo de emails. Em seguida, você poderá tomar as devidas providências nas mensagens inspecionadas com base no conteúdo ou nas características desses anexos. Saiba mais em [Use mail flow rules to inspect message attachments](http://technet.microsoft.com/library/874d1c78-a8ec-4938-b388-d3208c2fa971.aspx).
  
### <a name="phishing-and-spoofing-prevention"></a>Prevenção contra phishing e falsificação

Você pode melhorar a proteção anti-phishing detectando quando informações pessoais saem da organização em um email. Por exemplo, você pode usar as expressões regulares a seguir em regras de fluxo de emails para detectar a transmissão de dados financeiros pessoais ou informações que podem comprometer a privacidade:
  
- \d\d\d\d\s\d\d\d\d\s\d\d\d\d\s\d\d\d\d (MasterCard Visa)
    
- \d\d\d\d\s\d\d\d\d\d\d\s\d\d\d\d\d (American Express)
    
- \d\d\d\d\d\d\d\d\d\d\d\d\d\d\d\d (qualquer número com 16 dígitos)
    
- \d\d\d\-\d\d\-\d\d\d\d (Números do Seguro Social)
    
Campanhas bem-sucedidas de spam e phishing também podem ser reduzidas bloqueando emails de entrada e mal-intencionados que parecem ter sido enviados de seu próprio domínio. Por exemplo, você pode criar uma regra de fluxo de emails que rejeita mensagens do domínio de sua empresa enviadas para o mesmo domínio da empresa para bloquear este tipo de falsificação.
  
> [!CAUTION]
> Recomendamos criar esta regra de rejeição apenas nos casos em que você tem certeza de que nenhum email legítimo do seu domínio é enviado da Internet para seu servidor de emails. Isso pode acontecer nos casos em que uma mensagem é enviada de um usuário na sua organização para um destinatário externo e posteriormente encaminhada para outro destinatário na organização. 
  
### <a name="extension-blocking"></a>Bloqueio de Extensão

Se você estiver preocupado com arquivos executáveis que contêm malware, você pode configurar políticas antimalware para bloquear qualquer anexo de email que tem conteúdo executável. Siga as etapas em [Configure anti-malware políticas](../configure-anti-malware-policies.md).
  
Para maior proteção, nós também recomendamos que você bloqueie algumas ou todas as extensões a seguir: ade, adp, ani, bas, bat, chm, cmd, com, cpl, crt, hlp, ht, hta, inf, ins, isp, job, js, jse, lnk, mda, mdb, mde, mdz, msc, msi, msp, mst, pcd, reg, scr, sct, shs, url, vb, vbe, vbs, wsc, wsf, wsh.
  
## <a name="reporting-and-troubleshooting"></a>Relatórios e solução de problemas

Solucione problemas e tendências em geral usando os relatórios no Centro de administração do Office 365. Encontre um ponto de dados específico sobre uma mensagem usando a ferramenta de Rastreamento de Mensagem. Saiba mais sobre relatórios em [Relatórios e rastreamento de mensagem no Exchange Online Protection](reporting-and-message-trace-in-exchange-online-protection.md). Saiba mais sobre a ferramenta de Rastreamento de Mensagem em [Trace an Email Message](http://technet.microsoft.com/library/0c83cde6-5b09-4106-8587-c200cdc59094.aspx).
  
## <a name="for-more-information"></a>Para obter mais informações

[Perguntas frequentes gerais sobre o EOP](eop-general-faq.md)
  
[Ajuda e suporte para EOP](help-and-support-for-eop.md)
  
[Vídeos de introdução ao EOP](videos-for-getting-started-with-eop.md)
  
[Como ajudar a garantir que uma mensagem não será marcada como spam](https://go.microsoft.com/fwlink/p/?LinkId=534224)
  
[Bloquear spam de email com o filtro de spam do Office 365 para evitar problemas de falsos negativos](https://go.microsoft.com/fwlink/p/?LinkId=534225)
  


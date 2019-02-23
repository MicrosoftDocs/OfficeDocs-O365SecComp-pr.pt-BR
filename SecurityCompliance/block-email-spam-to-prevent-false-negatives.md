---
Título: "bloquear spam de email com o filtro de spam do Office 365 para evitar problemas falsos negativos" MS. Author: Krowley Author: kccross Manager: laurawi MS. Date: 7/2/2018 MS. Audience: admin MS. tópico: artigo MS. Service: O365-seccomp localization_priority: Priority Search. appverid: 
- MOE150
- MET150 MS. AssetID: da21c0b6-e8f0-4cc8-af2e-5029a9433d59 MS. Collection:
    - M365-Security-Compliance Description: "dicas para configurar o filtro de spam do Office 365 para ajudar a bloquear spam de email e impedir mensagens negativas falsas, um administrador usa a filtragem antispam do Office 365 para ajudar a impedir que spams sejam enviados a caixas de entrada de usuários."
---

# <a name="block-email-spam-with-the-office-365-spam-filter-to-prevent-false-negative-issues"></a>Bloquear spam de email com o filtro de spam do Office 365 para evitar problemas de falsos negativos

O EOP (Proteção do Exchange Online) é um serviço de filtragem de email baseado na nuvem que ajuda a proteger sua organização contra spam e malware. Se você tem caixas de correio no Office 365, elas já estão protegidas pelo EOP por padrão. 
  
Você pode ajudar a garantir o bloqueio de spam e lixo eletrônico ajustando o filtro de spam do Office 365. Isso ajuda na prevenção de problemas de falso negativo, em que o spam chega à caixa de entrada do usuário. Como administrador do Exchange Online ou do EOP (Proteção do Exchange Online), use as etapas a seguir para ajustar o filtro antispam do Office 365 e impedir a entrega de spam nas caixas de entrada dos usuários.
  
## <a name="customize-the-office-365-anti-spam-filter-with-these-settings"></a>Personalizar o filtro antispam do Office 365 com estas configurações

O administrador pode usar várias configurações de filtro de spam do Office 365 para ajudar a impedir o envio de spam para a caixa de entrada de um usuário. Use as opções listadas aqui para melhorar o filtro de spam do Office 365 e evitar mensagens de falso negativo. Nesse contexto, um falso negativo se refere a mensagens de spam ou lixo eletrônico enviadas para a caixa de entrada de um usuário.
  
### <a name="block-ip-addresses-with-a-connection-filter"></a>Bloquear um endereço IP com um filtro de conexão

Personalize o filtro de spam do Office 365 adicionando o endereço IP do remetente à lista de bloqueio de IP do filtro de conexão:
  
1. Obtenha os cabeçalhos da mensagem que você deseja bloquear no cliente de email, como Outlook ou Outlook na Web (anteriormente conhecido como Outlook Web App), conforme descrito em analisador de [cabeçalho de mensagem](https://go.microsoft.com/fwlink/p/?LinkId=306583).
    
2. Procure o endereço IP após a marca CIP no cabeçalho X-Forefront-Antispam-Report usando o [Analisador de cabeçalho de mensagem](https://testconnectivity.microsoft.com/?tabid=mha) ou manualmente. 
    
3. Adicione o endereço IP à Lista de IP Bloqueados executando as etapas em "Usar o EAC para editar a política de filtro de conexão padrão" em [Configurar a política de filtro de conexão](https://technet.microsoft.com/en-us/library/jj200718%28v=exchg.150%29.aspx).
    
### <a name="block-bulk-mail-with-transport-rules-or-the-spam-filter"></a>Bloquear emails em massa com regras de transporte ou filtro de spam

O spam é, em grande parte, emails em massa, por exemplo, boletins informativos ou promoções. Personalize o filtro de spam no Office 365 se você [Usar regras de transporte para filtrar rigorosamente as mensagens de email em massa](https://technet.microsoft.com/en-us/library/dn720438%28v=exchg.150%29.aspx) ou ative a configuração de **Emails em massa** nas [Opções Avançadas de Filtragem de Spam](https://technet.microsoft.com/en-us/library/jj200750%28v=exchg.150%29.aspx) em seu filtro de spam. No Centro de administração do Exchange, comece clicando em **Proteção** \> **Filtro de conteúdo** e, em seguida, clique duas vezes para filtrar a política que você deseja ajustar. Clique em **Ações para spam e emails em massa** para ajustar as configurações, conforme mostrado aqui. 
  
![Definir o filtro de email em massa no Exchange Online](media/a45095c2-269d-45b8-a76c-999b5e78da68.png)
  
### <a name="block-email-spam-using-spam-filter-block-lists"></a>Bloquear spam usando listas de bloqueio de filtro de spam

[Configure suas políticas de filtro de spam](https://technet.microsoft.com/en-us/library/jj200684%28v=exchg.150%29.aspx) para adicionar o endereço do remetente à lista de bloqueio de remetentes ou seu domínio à lista de bloqueio de domínios no filtro de spam. Os emails de um remetente ou domínio em uma lista de bloqueio de filtro de spam serão marcados como spam. 
  
### <a name="advanced-spam-filtering-options"></a>Opções avançadas de filtragem de spam

[Configure suas políticas de filtro de spam](https://technet.microsoft.com/en-us/library/jj200684%28v=exchg.150%29.aspx) e ative outras [Opções Avançadas de Filtragem de Spam](https://technet.microsoft.com/en-us/library/jj200750%28v=exchg.150%29.aspx).
  
Para saber mais sobre configurações de spam que se aplicam a toda a organização, consulte [Impedir falsos positivos marcados como spam usando uma lista confiável ou outras técnicas](prevent-email-from-being-marked-as-spam-0.md). Isso é útil se você tem controle no nível de administrador e quer impedir falsos positivos.
  
## <a name="email-users-can-also-help-ensure-that-false-negative-and-email-spam-is-blocked-with-office-365-spam-filter"></a>Os usuários de email também podem ajudar a garantir que os falsos negativos e spams sejam bloqueados com o filtro de spam do Office 365

Ele ajudará seus esforços antispam do Office 365 a evitar falsos negativos e lixo eletrônico se você disser aos usuários para adicionar o endereço de remetente de spam à lista de remetentes bloqueados no [Outlook](https://go.microsoft.com/fwlink/p/?LinkId=270065) ou [no Outlook na Web](https://go.microsoft.com/fwlink/p/?LinkId=294862). No Outlook na Web, comece clicando em **Opções** \> de **configurações** \> **bloquear ou permitir**e, em seguida, adicionar o endereço à lista de **remetentes bloqueados** , conforme mostrado aqui. 
  
![Bloqueando um remetente no Outlook na Web](media/fdf51381-2527-4819-ac2a-5dff84d2a36d.png)
  
> [!NOTE]
> Para saber mais sobre a lista de remetentes seguros, consulte [Perguntas frequentes sobre Remetente confiável e Listas de Remetentes Bloqueados](https://technet.microsoft.com/en-us/library/dn133608%28v=exchg.150%29.aspx). 
  
Os parágrafos anteriores desta subseção aplicam-se somente aos clientes que usam o EOP como serviço para proteger sistemas de email locais, ou como parte de uma implantação híbrida de email. Saiba mais sobre o EOP na [Página inicial da Proteção do Exchange Online](https://products.office.com/en-us/exchange/exchange-email-security-spam-protection).
  
## <a name="eop-only-customers-set-up-the-office-365-spam-filter-to-block-email-spam"></a>Clientes somente de EOP: configurar o filtro de spam do Office 365 para bloquear spam

Para clientes somente de EOP com caixas de correio locais: se você configurar um filtro de spam para a ação padrão "Mover a mensagem para a pasta Lixo Eletrônico", execute as etapas necessárias fornecidas em "Garantir que o spam seja direcionado para a pasta Lixo Eletrônico de cada usuário". Tentamos facilitar isso fornecendo os comandos do Shell de Gerenciamento do Exchange em um tópico separado, além de um link para saber mais sobre como começar a usar o shell.
  
Isso o ajudará a evitar os emails marcados incorretamente como spam se você sincronizar as configurações de usuário com o serviço por meio da sincronização de diretórios, a fim de garantir que os remetentes bloqueados sejam respeitados. Para saber mais, consulte "Usar a sincronização de diretórios para gerenciar usuários de email" em Gerenciar usuários de email no EOP.
  
## <a name="eop-only-customers-who-are-not-using-directory-synchronization"></a>Clientes somente de EOP que não estão usando a sincronização de diretórios

O serviço do EOP foi projetado para respeitar os remetentes confiáveis e bloqueados do usuário, se as informações tiverem sido compartilhadas com o serviço. Se você é um cliente de EOP que usa o Outlook, mas não tem a sincronização de diretórios configurada para sincronizar seus usuários no Office 365, ainda é possível impedir a entrega das mensagens na caixa de entrada dos usuários usando remetentes bloqueados. No entanto, talvez seja necessário configurar algumas regras de fluxo de email do Exchange nas seguintes situações:
  
- Se uma mensagem passar pela filtragem de spam normal no EOP e, em seguida, for entregue a um servidor local do Exchange e o EOP atribuir um veredito de spam SCL 1-4 (não spam), a lista local de remetentes bloqueados dos usuários substituirá o veredito do filtro de spam do EOP e a entregará à sua pasta Lixo Eletrônico.
    
- Se uma mensagem no EOP recebe um SCL -1 de uma regra de fluxo de email do Exchange, ou porque o endereço IP ou domínio está em sua lista de permissões, o SCL será propagado para o servidor local do Exchange usando conectores. Nesse caso, a lista de remetentes bloqueados do usuário não será aplicada. Para alterar isso, crie uma regra de fluxo de email local que define o SCL como 0. Isso fará com que o Outlook aplique a lista de remetentes bloqueados do local do usuário.
    
**Para configurar uma regra de fluxo de email a fim de impedir que as mensagens sejam entregues na caixa de entrada dos usuários usando a lista de remetentes bloqueados**
  
1. Abra o Shell de Gerenciamento do Exchange em seu servidor local. Para saber como abrir o Shell em sua organização local do Exchange, consulte [Abrir o Shell de Gerenciamento do Exchange](https://technet.microsoft.com/library/dd638134%28v=exchg.160%29.aspx).
    
2. Execute o comando a seguir para encaminhar mensagens de spam com conteúdo filtrado para a pasta Lixo Eletrônico a fim de atualizar o SCL em toda mensagem marcada com SCL -1:
    
  ```
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SCL:-1" -SetSCL 0
  ```

    Como o SCL é 0 em seu servidor local do Exchange, mensagens marcadas como não sendo spam serão entregues às caixas de entrada dos usuários, mas ainda poderão ser enviadas para o lixo eletrônico pela lista de remetentes bloqueados local dos usuários. Se você estiver usando a quarentena de spam no EOP, ainda será possível que os remetentes na lista de confiança do usuário sejam identificados como spam e enviados para quarentena. Se você estiver usando a pasta Lixo Eletrônico na caixa de correio local, isso permitirá a entrega de mensagens de remetentes confiáveis na Caixa de Entrada.

> [!WARNING]
> Se você usar uma regra de fluxo de email para alterar o valor do SCL para 0 (ou para qualquer valor diferente de -1), todas as opções de lixo eletrônico do Outlook serão aplicadas à mensagem. Isso significa que as listas confiáveis e bloqueadas serão cumpridas, mas também significa que as mensagens que não têm endereços nas listas bloqueadas ou confiáveis serão possivelmente marcadas como lixo eletrônico pelo processamento do filtro de lixo eletrônico no lado do cliente. Se você quiser que o Outlook processe as listas bloqueadas e confiáveis, mas não use o filtro de lixo eletrônico no lado do cliente, defina a opção "Sem Filtragem Automática" nas Opções de Lixo Eletrônico do Outlook. "Sem Filtragem Automática" é a opção padrão nas versões mais recentes do Outlook, mas você deve confirmar se essa configuração está presente, a fim de garantir que o filtro de lixo eletrônico do lado do cliente não seja aplicado às mensagens. Como administrador, você pode impor a desativação da filtragem de Lixo Eletrônico do Outlook seguindo as instruções em [Outlook: configuração de política para desativar a IU de lixo eletrônico e o mecanismo de filtragem](https://support.microsoft.com/en-us/kb/2180568).
  
## <a name="see-also"></a>Confira também

[Proteção anti-spam de emails do Office 365](anti-spam-protection.md)
  
[Impedir falsos positivos marcados como spam usando uma lista confiável ou outras técnicas](prevent-email-from-being-marked-as-spam-0.md)
  


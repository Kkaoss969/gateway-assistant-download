# Live Assistant (relógio) + Gateway Assistant (telemóvel) — guia rápido

Com o seu relógio Amazfit (Zepp OS), Huawei Watch 3 / Watch 4, **Wear OS** (Galaxy Watch, Pixel Watch, TicWatch…) ou um relógio Huawei com **HarmonyOS** (Watch 5, Watch Ultimate 2…) fala com o Gemini e, através da app **Gateway Assistant** no seu telemóvel Android, pode:
controlar a sua casa Google, fazer chamadas, enviar/ler/responder a mensagens de WhatsApp e usar a voz do telemóvel.
Cada pessoa usa o seu próprio telemóvel, conta Google e chave Gemini: nada a partilhar.

🌐 As apps falam **italiano, inglês, espanhol, francês, português (Portugal e Brasil) búlgaro e turco**: seguem automaticamente a língua do relógio e do telemóvel. · *Italiano: [GUIDA.md](GUIDA.md)* · *English: [GUIDE.md](GUIDE.md)* · *Español: [GUIA.md](GUIA.md)* · *Français: [GUIDE-FR.md](GUIDE-FR.md)* · *Português do Brasil: [GUIA-BR.md](GUIA-BR.md)* · *Български: [GUIDE-BG.md](GUIDE-BG.md)* · *Türkçe: [GUIDE-TR.md](GUIDE-TR.md)*

## Do que precisa
- Um telemóvel Android com a app **Zepp** e o relógio já emparelhado
- Uma **chave API do Gemini** (grátis, ou com crédito para respostas mais rápidas): https://aistudio.google.com/apikey
- A app **Google** (Assistente) no telemóvel, ligada ao seu Google Home (só para os comandos da casa)

<a id="api-keys"></a>
## Chaves API
As chaves introduzem-se **uma só vez** no Gateway Assistant → **🔑 Chaves API** e servem para todos os relógios; na página de cada relógio dá-as ao Live com *Enviar as chaves ao relógio* (ou ao instalar).
- **Gemini** (obrigatória, grátis): abra https://aistudio.google.com/apikey com a sua conta Google → **Create API key** → escolha ou crie um projeto → copie a chave (começa por `AIza` ou `AQ.`) e cole-a no Gateway → *Guardar a chave Gemini*. O plano gratuito tem limites diários; com algum crédito as respostas são mais rápidas.
- **Groq** (opcional, grátis): abra https://console.groq.com/keys, inicie sessão (a conta Google funciona) → **Create API Key** → dê-lhe um nome → copie a chave (começa por `gsk_`, mostrada uma só vez) e cole-a no Gateway → *Guardar a chave Groq*. Dá respostas escritas em cerca de 1 segundo.
- Para remover uma chave, mantenha premido o botão *Guardar* correspondente.

## 1 · Instalar o Gateway Assistant (telemóvel)
1. Transfira o APK no telemóvel: **https://github.com/Kkaoss969/gateway-assistant-download/raw/main/GatewayAssistant.apk**
2. Abra-o e permita as instalações desta origem se o Android pedir.
3. Abra o **Gateway Assistant** e toque em **Iniciar o gateway**.
4. Na lista **Permissões**, toque em cada linha com ⚪ até estarem todas ✅:
   contactos e chamadas · mostrar sobre outras apps · envio de WhatsApp (acessibilidade) · leitura de WhatsApp (notificações) · bateria sem restrições.
   ⚠ **Acessibilidade**: na página do Android «Gateway Assistant (envio de WhatsApp)» ligue **só o primeiro interruptor no topo** («Ligado»). **Não ligue** o segundo, «Atalho de Gateway Assistant (envio de WhatsApp)»: é só um atalho do Android e, se estiver ligado, os toques automáticos (Enviar do WhatsApp, Desligar/Adiar do alarme, envio ao Gemini) não funcionam.
   Se uma definição estiver «restrita»: Definições → Apps → Gateway Assistant → menu ⋮ → *Permitir definições restritas*.
5. Toque em **Copiar código** (o código de canal).

## 2 · Instalar o Live Assistant no relógio
1. Na app Zepp ligue o modo de programador: Perfil → Definições → Acerca de → toque várias vezes no logótipo Zepp.
2. Abra **https://kkaoss969.github.io/gateway-assistant-download/**, escolha o seu relógio e leia o **código QR** com a app Zepp (Perfil → ícone de leitura).
3. Na app Zepp abra as definições da app **Live Assistant** e preencha:
   - **Chave API do Gemini**
   - **A minha cidade** (meteorologia e notícias locais)
   - **Gateway Assistant → Código**: cole o código copiado no passo 1
   - **Chave API do Groq** (opcional, grátis em https://console.groq.com → *API Keys*): notícias e perguntas escritas respondem em cerca de 1 segundo; as perguntas faladas ficam com o Gemini
   - **Nomes que usa muitas vezes** (opcional): pessoas, terras, equipas… ajudam-no a perceber os nomes certos
   - **Idioma da app**: normalmente o do relógio; o **búlgaro** escolhe-se aqui, porque o Zepp OS não o tem

## 3 · Recomendado
- **Chamadas no relógio**: app Zepp → Perfil → relógio → Definições das apps → Telefone → *Atender chamadas no relógio* (e emparelhe o Bluetooth).
- **WhatsApp com o telemóvel bloqueado**: Definições → Segurança → Smart Lock / Extend Unlock → *Dispositivos de confiança* → adicione o relógio.
- **WhatsApp duplo (clone)**: se o telemóvel tiver um segundo WhatsApp clonado (Dual Messenger na Samsung, «Apps duplas» noutros telemóveis), as mensagens de texto são enviadas mas **as mensagens de voz do relógio não** (o WhatsApp abre a conversa sem o áudio). Para enviar mensagens de voz remova o WhatsApp clonado; duas contas no mesmo WhatsApp não são problema. O Gateway assinala-o com ⚠️ no botão de envio de WhatsApp.
- **Beeper (experimental)**: se usa o [Beeper](https://play.google.com/store/apps/details?id=com.beeper.android) com o WhatsApp e o Telegram associados, toque em *🧪 Beeper* no Gateway e permita o acesso: as mensagens de texto são enviadas sem abrir o WhatsApp e sem acessibilidade, mesmo com o telemóvel bloqueado, e no Telegram pode escrever para qualquer conversa. As mensagens de voz continuam a passar pelo WhatsApp.
  Sem ele, o telemóvel acorda e a mensagem é enviada quando o desbloquear.
- **Comandos da casa com o telemóvel bloqueado**: app Google → Definições → Assistente Google → Ecrã de bloqueio → resultados pessoais ligados.

**Alarme do telemóvel**: quando toca, o relógio vibra e abre sozinho os botões **Desligar** e **Adiar**. O relógio fica a saber a hora do próximo alarme sempre que abre o Live Assistant (e depois de cada alarme): se criar um alarme novo no telemóvel, abra a app no relógio uma vez. ⚠ Em **modo de sono** ou **Não incomodar** o relógio bloqueia as apps de terceiros: programe o modo de sono / Não incomodar para terminar uns minutos antes do alarme (Definições do relógio → Não incomodar → Programado).

**Gemini Live (teste)**: na app Zepp → Live Assistant → Definições ligue **Usar o Gemini Live** (precisa do Gateway Assistant 1.65 ou posterior no mesmo telemóvel). A resposta chega já como voz, sem esperar pela síntese; se o Live falhar, usa-se o método normal.

## Relógio Huawei (Watch 3, Watch 4)
Para os **Huawei Watch 3 e Watch 4** (os baseados em Android) existe o **Live Assistant**, com **Gemini Live**: enquanto fala, a pergunta já vai para o Gemini e a resposta volta diretamente como voz, normalmente em 1-3 segundos. Funciona com o Wi-Fi ou LTE do relógio e também só por Bluetooth, através do Gateway. Instala-se a partir do **Gateway Assistant**, sem computador.
1. No relógio: Definições → Acerca de → toque várias vezes no **número da compilação**. Depois, nas **Opções de programador**, ligue a **depuração HDC** e a **Depuração por Wi-Fi**.
2. Relógio e telemóvel no **mesmo Wi-Fi** (o hotspot do telemóvel serve).
3. No Gateway Assistant toque em **⌚ Relógio Huawei: instalação e diagnóstico**, introduza o IP mostrado em *Depuração por Wi-Fi* e toque em **Transferir e instalar o Live Assistant**. Da primeira vez o relógio pede para permitir a ligação: toque em **Permitir sempre**.
   O Gateway dá ao relógio o código de canal e, se a caixa estiver marcada, a sua chave Gemini; também exclui a app da poupança de bateria.
4. No Gateway Assistant toque em **⚪ Permitir Bluetooth Huawei** até aparecer **✅ Bluetooth Huawei: ligado**: o relógio passa a funcionar **sem Wi-Fi nem LTE**, através do Bluetooth do telemóvel.
5. **Botão inferior**: na mesma página toque em **Botão inferior: abrir o Live Assistant**. O botão inferior do relógio passa a abrir o Live Assistant, já à escuta, em vez da Celia (*Repor a Celia* desfaz).

No relógio, a **roda dentada** por baixo de *Nova conversa* abre as definições (cidade, ligação Auto/Bluetooth/Internet, voz, atualizações, diagnóstico); a **coroa** percorre as páginas. Perguntas, voz, meteorologia e notícias, casa Google, Contactos e WhatsApp, chamadas, comandos rápidos, lembretes, lanterna, volume e brilho, passos e frequência cardíaca funcionam todos. Por voz também pode mudar o **DPI do ecrã** («põe o dpi a 280», «repõe o dpi»; de 90 a 400, padrão 320); as definições do relógio têm **Repor DPI** e o Gateway (página do relógio Huawei, secção *DPI do ecrã*) tem **Aplicar** e **Repor (320)**.
**Alarme do telemóvel**: quando toca, o relógio vibra e mostra **Parar** e **Adiar** (mesmo em modo noturno, que é desligado um minuto antes; Adiar volta a ligá-lo). Também funciona com alarmes de última hora: na app Saúde → Dispositivos → relógio → Notificações ligue o **Gateway Assistant**.
**Atualizações**: o Gateway Assistant mostra a versão instalada e a nova; atualize na mesma página ou a partir do relógio (Definições → *Verificar e instalar*, com a Depuração por Wi-Fi ligada).
**Groq (opcional)**: o Live responde sozinho às perguntas gerais; os comandos (casa, chamadas, WhatsApp, alarmes, meteorologia, notícias) são executados pela app e, com uma chave Groq, a parte de texto fica pronta em cerca de 1 segundo. Chave grátis: https://console.groq.com → *API Keys* → *Create API Key* (começa por `gsk_`) e cole-a no Gateway → *🔑 Chaves API* → *Guardar a chave Groq*.
**Diagnóstico**: chega sozinho ao Gateway (página do relógio Huawei; a partir do relógio também Definições → *Enviar para o Gateway Assistant*). Com **Partilhar** envia-o como ficheiro de texto (WhatsApp, Telegram, email) a quem o está a ajudar.
**Dois abanões para abrir (teste)**: nas definições do relógio ligue *Teste: dois abanões fortes abrem a app*. Com o ecrã aceso, dois abanões secos e seguidos abrem o Live Assistant à escuta; com o ecrã sempre ligado o sensor fica desligado para poupar bateria: levante o pulso para voltar a acender o ecrã. O botão inferior também funciona.
**Poupança de energia Huawei**: o relógio pode fechar o Live Assistant em segundo plano (o botão inferior e os abanões deixam de funcionar até voltar a abrir a app). No Gateway, página do relógio Huawei, toque em **PowerGenie: remover** (se o relógio não permitir, fica desligado; **PowerGenie: repor** desfaz). Se a Depuração por Wi-Fi ficar ligada e estiver na mesma rede, o Gateway reativa sozinho o Live Assistant quando o relógio o fecha.

### Instalar as suas apps no relógio
Na mesma página do Gateway, secção **Instalar as suas apps no relógio**: toque em **📲 Escolher a app a instalar** e escolha o ficheiro transferido. Funcionam os **APK** simples e os pacotes divididos **APKS**, **XAPK** (incluindo ficheiros OBB) e **APKM**. É precisa a Depuração por Wi-Fi, como para o Live Assistant. Na caixa por baixo pode escrever um **comando adb** (ex. `pm list packages -3` para listar as apps instaladas) (secção **Executar no relógio**) e tocar em **Executar**: o resultado aparece por baixo e **Copiar o resultado** copia-o.

## Relógio Wear OS (beta)
O Live Assistant também funciona em **relógios Wear OS a partir do Android 9**, redondos e retangulares (Galaxy Watch, Pixel Watch, Oppo Watch, Mi Watch, TicWatch, Fossil…), incluindo os antigos **Wear OS 2 e 3**, onde o Assistente Google e o WhatsApp já não funcionam. É a mesma app do Huawei: perguntas por voz com o Gemini Live, meteorologia gráfica, Casa, Contactos, WhatsApp e Telegram através do Gateway.
**Ligação ao telemóvel**: primeiro o canal oficial do Wear OS (Bluetooth, Wi-Fi ou rede, escolhido pelo Wear OS), depois o Bluetooth direto. O Gateway dá ao relógio as chaves e o código de canal: também funciona longe do telemóvel se o relógio tiver rede.

**Instalação** — no Gateway Assistant toque em **⌚ Relógio Wear OS: instalação e diagnóstico**. Primeiro, no relógio, ligue as **Opções de programador**: Definições → Acerca de (no Galaxy *Acerca do relógio → Informações do software*) → toque várias vezes em **Versão do software** ou **Número da compilação**. Relógio e telemóvel no **mesmo Wi-Fi** (o hotspot do telemóvel serve). Depois escolha a ligação:
- **Depuração sem fios (Wear OS 4 e posterior)**: Opções de programador → **Depuração sem fios** ligada (*Permitir sempre nesta rede*).
  1. No relógio abra **Sincronizar novo dispositivo** (aparece um código de 6 dígitos).
  2. No Gateway escreva **só o código** e toque em **🔗 Sincronizar**: o IP, a porta de ligação e a porta de sincronização são encontrados automaticamente na rede (botão **🔍 Encontrar o relógio**; também se podem escrever nos campos). Depois da sincronização o botão fica verde, **Sincronizado ✓**: não é preciso repetir.
  3. Toque em **⬇ Transferir e instalar o Live Assistant**. A porta de ligação muda sempre que volta a ligar a Depuração sem fios: se um comando não conseguir ligar, esvazie o campo da porta e o Gateway volta a encontrá-la.
- **Depurar por Wi-Fi (Wear OS 2 e 3)**: Opções de programador → **Depuração ADB** e **Depurar por Wi-Fi** ligadas. Introduza o IP do relógio (a porta já é **5555**) e toque em **⬇ Transferir e instalar o Live Assistant**; no relógio aceite a depuração (**Permitir sempre**).

O Gateway instala a app, dá as permissões (microfone, sensores, atualizações), exclui-a da poupança de bateria, dá-lhe as chaves e abre-a. Cada botão mostra os passos numa janela (**Copiar** para os enviar a quem o ajuda).
No **Pixel Watch**, se o ícone não aparecer na lista de apps depois de instalar, reinicie o relógio.
**Botão para abrir o Live** — nas definições do Live no relógio (roda dentada): *Toque longo no botão inicial: Live em vez do assistente Google*; no **Galaxy Watch Ultra** o **botão do meio (laranja)**: nas definições dos botões da Samsung escolha **Nenhuma app**, depois no Live toque em **Aprender a app do botão** e carregue uma vez no botão. Se o guardião do botão não estiver ativo, no Gateway toque em **🔑 Dar as permissões ao Live**.
**Notificações do telemóvel (só Huawei)**: Gateway → página do relógio Huawei → **🔔 Notificações do telemóvel no relógio**: escolha as apps (toque para mudar: desligada → *perto*, por Bluetooth → *também longe*, também pela internet, no máximo 40 por dia). Ignorada ou tocada no relógio, a notificação também desaparece do telemóvel. No Wear OS e no Amazfit as notificações já chegam pelas próprias apps.
**Telegram no relógio** (Wear OS e Huawei): quando o telemóvel não está ligado por Bluetooth, por LTE ou Wi-Fi lê e envia Telegram (textos, mensagens de voz, fotos) diretamente do relógio. Associe uma vez, perto do telemóvel e com o *Telegram direto* ligado no Gateway: definições do Live no relógio → **Associar o Telegram (a partir do telemóvel)**. O Gateway aceita o início de sessão sozinho; com a verificação em dois passos o relógio pede a palavra-passe. O relógio aparece no Telegram → Dispositivos como *Live Assistant (orologio)*. A ligação só abre quando é precisa e fecha após 2 minutos.
**Atualizações**: no relógio, roda dentada → *Verificar e instalar*. No Wear OS 4 e posterior a app atualiza-se sozinha (da primeira vez permita *Instalar apps desconhecidas* e depois confirme); no Wear OS 2 e 3 passa pela Depuração por Wi-Fi, que tem de ficar ligada.
**Na mesma página**: *Enviar as chaves ao relógio*; **DPI do ecrã** (*Repor* volta ao DPI de fábrica do modelo, ex. 340 na Samsung); **Instalar as suas apps** (APK, APKS, XAPK, APKM); **Executar no relógio** (comandos adb); **Diagnóstico** do relógio (com modelo e versão do Android).
**Botão**: no Galaxy Watch, Definições → Funcionalidades avançadas → Personalizar teclas → *Premir duas vezes* → **Live Assistant**. Para o botão central do Galaxy Watch Ultra estamos a preparar o guardião do botão: no Gateway toque em **🔎 Estudar os botões**, carregue nos botões do relógio durante 15 segundos e envie o resultado.

## Relógio HarmonyOS (Watch 5, Watch Ultimate 2…) (beta)
Para os relógios Huawei com **HarmonyOS NEXT** (ex. Watch 5, Watch Ultimate 2), que não instalam APK, existe o **Live Assistant para HarmonyOS**. Tem as mesmas funções das outras versões: perguntas por voz com o Gemini Live, meteorologia, Casa, Contactos, WhatsApp e Telegram, alarmes do telemóvel, histórico. Instala-se a partir do **Gateway Assistant**, sem computador.
**Porque é precisa uma conta de programador Huawei**: o HarmonyOS só instala apps assinadas com um perfil que contém o identificador (UDID) do seu relógio. O Gateway cria a chave, o certificado e o perfil com a **sua** conta, tal como o DevEco Studio. Ficam só no seu telemóvel e não são partilhados.

**1 · Conta de programador Huawei (uma vez)**
1. Abra https://developer.huawei.com, inicie sessão com o seu **ID Huawei** (serve o da app Saúde) e conclua o **registo como programador** (gratuito, conta individual). A Huawei pode pedir uma verificação de identidade: espere até aparecer aprovada.
2. No Gateway Assistant toque em **⌚ Relógio HarmonyOS: ligação e diagnóstico** → **🔏 Ficheiros de assinatura para as HAP** → **🔐 Perfis automáticos: inicie sessão com a conta Huawei (como o DevEco)**.
3. Abre-se o navegador: inicie sessão com a conta de programador e confirme. O navegador volta sozinho ao Gateway, que mostra **✅ Sessão iniciada**; o botão passa a **🔐 Conta Huawei:** com o seu nome (tocando nele termina a sessão).
Não é preciso mais nada: a chave e o certificado de depuração criam-se sozinhos na primeira instalação (ou logo, com **🪄 Criar chave e certificado com a conta Huawei**). Cada conta pode ter no máximo 3 certificados de depuração (o do Gateway substitui-se sozinho): se já tiver 3 feitos com o DevEco Studio e o Gateway o indicar, apague um antigo no AppGallery Connect (*Certificados, IDs de apps e perfis → Certificados*).

**2 · Prepare o relógio**
1. No relógio: Definições → Acerca de → toque várias vezes na **versão** até aparecerem as **Opções de programador**.
2. Nas Opções de programador ative a **depuração (HDC)** e a **depuração Wi-Fi**: o relógio mostra **IP e porta** (ex. 192.168.0.191:44911). A porta muda sempre que reativa a depuração.
3. Relógio e telemóvel na **mesma rede Wi-Fi** (serve o hotspot do telemóvel).

**3 · Instale o Live Assistant**
1. No Gateway: **⌚ Relógio HarmonyOS** → **📲 Instalar ou atualizar o Live no relógio**.
2. Escreva o **IP** e a **porta** do relógio, ou toque em **🔎 Procurar o relógio no Wi-Fi** (com o IP já escrito encontra a porta em poucos segundos).
3. Toque em **⬇ Do site**. O Gateway transfere o Live Assistant, regista o relógio na sua conta, cria o perfil, assina a app, instala-a e abre-a já ligada ao Gateway (código do canal e chaves). Na janela vê cada passo, até **✅ Feito**.
4. Na primeira vez o relógio pede para **permitir a ligação** de depuração: aceite.
Se o relógio já tiver um Live Assistant assinado por outra pessoa, o Gateway pergunta se o deve desinstalar primeiro (os dados da app no relógio perdem-se).

**Atualizações**: o Gateway Assistant mostra quando há uma versão nova. Atualiza-se da mesma forma (📲 Instalar ou atualizar → ⬇ Do site), com a depuração Wi-Fi ativa; definições e dados mantêm-se.
**Ligação ao telemóvel**: o Live experimenta sozinho o Wi-Fi direto (mesma rede), o Bluetooth e por fim a internet (Wi-Fi ou LTE do relógio) com o código do canal. Para usar o Bluetooth: no relógio ⚙ → **🔵 Testar Bluetooth com o Gateway** (permita o Bluetooth).
**Live em segundo plano (beta)**: em ⚙ → **🌙 Live em segundo plano** o relógio recebe os avisos de mensagens por Bluetooth mesmo com a app fechada e verifica alarmes e mensagens a cada 30 minutos. Gasta um pouco mais de bateria e é preciso primeiro o teste de Bluetooth bem-sucedido.
**Diagnóstico**: no relógio ⚙ → Diagnóstico → 📤 Gateway; no Gateway está em ⌚ Relógio HarmonyOS → **Diagnóstico**.
**Já tem os seus ficheiros de assinatura?** (para quem usa o DevEco Studio): em **🔏 Ficheiros de assinatura para as HAP** carregue a chave **.p12** com a palavra-passe, o certificado de depuração **.cer** e os perfis **.p7b** (um por app, com o UDID do relógio, que copia em **🛠 Ferramentas hdc** → **📋 Identificador do relógio (UDID)**). O botão **🤖 Perfis automáticos (AppGallery Connect)** usa as API oficiais, que não funcionam com as contas europeias: nesse caso use o início de sessão com a conta Huawei.
**Outras ferramentas** (🛠 Ferramentas hdc): **🔑 Enviar ao Live a chave Gemini e o canal**, comandos no relógio. Com **Escolher a HAP** instala também outras apps HarmonyOS: se a conta Huawei estiver ligada, o Gateway assina-as sozinho.

## Com um iPhone
O Gateway Assistant é só para Android: o iOS não deixa uma app ficar sempre ativa, carregar em «Enviar» no WhatsApp, ler notificações ou passar frases ao Assistente Google.
**O Live Assistant funciona na mesma com um iPhone**: perguntas ao Gemini, voz, meteorologia, notícias, lembretes, volume, brilho e lanterna.
Não disponível: comandos da casa Google, chamadas por nome a partir dos contactos, envio e leitura de WhatsApp, voz de reserva do telemóvel.
- Salte o passo 1 e deixe **Gateway Assistant → Código** vazio.
- Mantenha a **app Zepp aberta em segundo plano** (não a feche deslizando): se o iOS a suspender, o relógio diz «telemóvel inacessível».
- As chamadas normais no relógio funcionam com as chamadas por Bluetooth da app Zepp.

## Gestos do pulso (abanões)
Úteis com ruído ou com as mãos ocupadas. Ligam-se e desligam-se nas definições da app no relógio (Huawei) e funcionam com a app aberta:
- **Um abanão enquanto ouve**: envia logo a pergunta, sem esperar pelo silêncio.
- **Um abanão enquanto pensa** (cores a rodar): cancela a pergunta.
- **Um abanão enquanto fala**: para a voz.
- **Um abanão em repouso**: nova pergunta (volta a ouvir).
- **Dois abanões**: fecham a app. Dê o segundo depois de uma pequena pausa e **com mais força** do que o primeiro, para que uma segunda tentativa normal não a feche por engano.
- **Botão Parar (Huawei e Amazfit)**: desde que começa a ouvir até chegar a resposta, um botão vermelho **■ Parar** substitui *Nova conversa*: cancela a pergunta sem a enviar (ou ignora a resposta que está a chegar) e os comandos dessa pergunta não são executados. Um toque no botão central enquanto ouve envia logo. Quando uma mensagem de WhatsApp/Telegram ou uma mensagem de voz é enviada, aparece um grande **✓ verde** com uma vibração e um som curto (sem som em modo de privacidade); se falhar, um **✗ vermelho**.
Os abanões não contam nos primeiros 2 segundos depois de abrir. Após **30 segundos** sem atividade a app volta sozinha ao mostrador.

## O que pode dizer
- «Que tempo vai fazer amanhã?», «Como ficou o Benfica?», qualquer pergunta (nas perguntas de meteorologia o relógio também mostra um **cartão gráfico**: agora, próximas horas e próximos dias)
- «Acende a luz da cozinha», «boa noite»
- «Liga ao Mário» (se houver vários Mários toca num no relógio)
- «Manda um WhatsApp ao Mário: chego daqui a dez minutos» (toque em **Enviar a …** para confirmar)
- «Lê as minhas mensagens de WhatsApp», «responde à Ana: combinado»
- «Responde no Telegram ao Luís: estou a caminho» (só a conversas de Telegram com uma notificação recente; «lê as minhas mensagens» mostra também as do Telegram)
- «Manda uma mensagem de voz ao Mário»: toque no contacto 🎤, fale e toque de novo para enviar. Chega como nota de voz do WhatsApp; no Huawei é preciso o Bluetooth ao telemóvel (ou, na página Contactos, **mantenha premido WhatsApp** num favorito: a gravação começa logo)
- «Desliga o alarme de amanhã», «para o alarme», «adia o alarme» (alarmes do **telemóvel**)
- «Põe o dentista no calendário na quinta às 10, avisa-me uma hora antes», «o que tenho amanhã?» (calendário do **telemóvel**: no Gateway Assistant toque em **Permitir Calendário**)
- «Adiciona leite à lista de compras», «toma nota: comprar lâmpadas», «lembra-me amanhã às 9 no Google Tasks de ligar ao Luís» (**Keep** e **Tasks**: o Gateway escreve a frase ao Gemini no telemóvel; precisa da acessibilidade do Gateway Assistant e das extensões Keep e Tasks ligadas no Gemini)
- «Liga o Não incomodar até às 7», «desliga o Não incomodar» (Não incomodar do **telemóvel**: no Gateway Assistant toque em **Permitir Não incomodar**; aplicam-se as exceções definidas no telemóvel)
- «Lembra-me às 18 de ligar ao dentista», «alarme às 7», «aumenta o volume»

**Comandos rápidos e favoritos**: no Gateway Assistant, secção «No relógio: comandos rápidos e favoritos», adicione botões com uma frase para o Assistente (ex. «Shield» → «liga a Shield») e contactos favoritos da sua agenda. No relógio, ao lado do botão central: o ícone **casa** (ou a seta **‹**) abre **Casa**, com os seus botões (vão diretamente ao Assistente do telemóvel, sem Gemini) e **Não incomodar** para ligar e desligar; o ícone **mensagens** (ou a seta **›**) abre **Contactos**, com os seus favoritos e os botões **WhatsApp** (diga a mensagem e confirme com Enviar) e **Ligar**.

**Favoritos e grupos**: até **16 favoritos** entre contactos e grupos. Com **+ Adicionar grupo do WhatsApp** e **+ Adicionar grupo do Telegram** escolhe um grupo: no relógio fica com um cartão próprio com a última mensagem (e quem a escreveu), os balões e as respostas. **Avisos**: quando um favorito lhe escreve (ou num grupo favorito) o relógio mostra o nome e uma pré-visualização, e um toque abre a conversa dessa app. Com o WhatsApp e o Telegram diretos, os avisos chegam mesmo que o telemóvel não mostre nenhuma notificação.

**Modo de privacidade**: toque no botão **microfone** em baixo à direita do botão central: passa a um **teclado** verde: o microfone fica desligado e o botão central abre o teclado; escreva a pergunta e a resposta volta só em texto, sem voz. Toque de novo para voltar à voz. Para uma só pergunta escrita também pode **manter premido** o botão central. Precisa de um relógio com Zepp OS 4 ou posterior.

## Se algo correr mal
- App Zepp → Live Assistant → **Diagnóstico**: mostra o que aconteceu em cada pergunta. Também chega ao Gateway Assistant (**⌚ Relógio Amazfit: diagnóstico**): daí copia-o ou envia-o como ficheiro com **Partilhar ficheiro**.
- No Gateway Assistant o **Registo** mostra chamadas, mensagens e comandos.
- O gateway tem de estar ativo («Gateway ativo ✓») com a bateria sem restrições.
- **🐞 Comunicar um problema** no Gateway, ou por voz a partir do relógio («comunica um problema: o botão do WhatsApp não funciona»): o relatório chega ao programador com o registo e o diagnóstico dos relógios, com os textos das mensagens e os números ocultados. Da primeira vez pede consentimento. O Gateway também comunica sozinho os problemas repetidos (no máximo uma vez por dia por tipo).
- O botão do gateway fica **verde** quando está ativo e **vermelho** quando está parado.
- **Contagem anónima de utilização**: uma vez por dia o Gateway envia só um identificador aleatório e as versões das apps, sem dados pessoais. Desligue-a com **📊 Contagem anónima de utilização**.

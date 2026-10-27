# Live Assistant (relógio) + Gateway Assistant (celular) — guia rápido

Com seu relógio Amazfit (Zepp OS), Huawei Watch 3 / Watch 4, **Wear OS** (Galaxy Watch, Pixel Watch, TicWatch…) ou um relógio Huawei com **HarmonyOS** (Watch 5, Watch 6, Watch Ultimate 2…) você fala com o Gemini e, pelo app **Gateway Assistant** no seu celular Android, pode:
controlar sua casa Google, fazer ligações, enviar/ler/responder mensagens de WhatsApp e usar a voz do celular.
Cada pessoa usa o próprio celular, conta Google e chave Gemini: nada para compartilhar.

🌐 Os apps falam **italiano, inglês, espanhol, francês, português (Portugal e Brasil) búlgaro e turco**: seguem automaticamente o idioma do relógio e do celular. · *Italiano: [GUIDA.md](GUIDA.md)* · *English: [GUIDE.md](GUIDE.md)* · *Español: [GUIA.md](GUIA.md)* · *Français: [GUIDE-FR.md](GUIDE-FR.md)* · *Português (Portugal): [GUIA-PT.md](GUIA-PT.md)* · *Български: [GUIDE-BG.md](GUIDE-BG.md)* · *Türkçe: [GUIDE-TR.md](GUIDE-TR.md)*

## Do que você precisa
- Um celular Android com o app **Zepp** e o relógio já pareado
- Uma **chave API do Gemini** (grátis, ou com crédito para respostas mais rápidas): https://aistudio.google.com/apikey
- O app **Google** (Assistente) no celular, vinculado ao seu Google Home (só para os comandos da casa)

<a id="api-keys"></a>
## Chaves API
As chaves são digitadas **uma vez só** no Gateway Assistant → **🔑 Chaves API** e valem para todos os relógios; na página de cada relógio você passa para o Live com *Enviar as chaves para o relógio* (ou ao instalar).
- **Gemini** (obrigatória, grátis): abra https://aistudio.google.com/apikey com sua conta Google → **Create API key** → escolha ou crie um projeto → copie a chave (começa com `AIza` ou `AQ.`) e cole no Gateway → *Salvar a chave Gemini*. O plano gratuito tem limites diários; com um pouco de crédito as respostas ficam mais rápidas.
- **Groq** (opcional, grátis): abra https://console.groq.com/keys, faça login (a conta Google funciona) → **Create API Key** → dê um nome → copie a chave (começa com `gsk_`, aparece uma vez só) e cole no Gateway → *Salvar a chave Groq*. Ela dá respostas escritas em cerca de 1 segundo.
- Para remover uma chave, segure o botão *Salvar* dela.

## 1 · Instalar o Gateway Assistant (celular)
1. Baixe o APK no celular: **https://github.com/Kkaoss969/gateway-assistant-download/raw/main/GatewayAssistant.apk**
2. Abra e permita instalações desta fonte se o Android pedir.
3. Abra o **Gateway Assistant** e toque em **Iniciar o gateway**.
4. Na lista **Permissões**, toque em cada linha com ⚪ até ficarem todas ✅:
   contatos e ligações · sobrepor a outros apps · envio de WhatsApp (acessibilidade) · leitura de WhatsApp (notificações) · bateria sem restrições.
   ⚠ **Acessibilidade**: na página do Android "Gateway Assistant (envio de WhatsApp)" ative **só a primeira chave no topo** ("Ativado"). **Não ative** a segunda, "Atalho do Gateway Assistant (envio de WhatsApp)": é só um atalho do Android e, se estiver ativada, os toques automáticos (Enviar do WhatsApp, Desligar/Soneca do alarme, envio para o Gemini) não funcionam.
   Se uma configuração estiver "restrita": Configurações → Apps → Gateway Assistant → menu ⋮ → *Permitir configurações restritas*.
5. Toque em **Copiar código** (o código de canal).

## 2 · Instalar o Live Assistant no relógio
1. No app Zepp ative o modo desenvolvedor: Perfil → Configurações → Sobre → toque várias vezes no logo do Zepp.
2. Abra **https://kkaoss969.github.io/gateway-assistant-download/**, escolha seu relógio e escaneie o **código QR** com o app Zepp (Perfil → ícone de escanear).
3. No app Zepp abra as configurações do app **Live Assistant** e preencha:
   - **Chave API do Gemini**
   - **Minha cidade** (clima e notícias locais)
   - **Gateway Assistant → Código**: cole o código copiado no passo 1
   - **Chave API do Groq** (opcional, grátis em https://console.groq.com → *API Keys*): notícias e perguntas digitadas respondem em cerca de 1 segundo; as perguntas faladas ficam com o Gemini
   - **Nomes que você usa sempre** (opcional): pessoas, cidades, times… ajudam a entender os nomes certos
   - **Idioma do app**: normalmente o do relógio; o **búlgaro** é escolhido aqui, porque o Zepp OS não tem

## 3 · Recomendado
- **Ligações no relógio**: app Zepp → Perfil → relógio → Configurações dos apps → Telefone → *Atender ligações no relógio* (e pareie o Bluetooth).
- **WhatsApp com o celular bloqueado**: Configurações → Segurança → Smart Lock / Extend Unlock → *Dispositivos confiáveis* → adicione o relógio.
- **WhatsApp duplo (clone)**: se o celular tiver um segundo WhatsApp clonado (Dual Messenger na Samsung, "Apps duplicados" em outros celulares), as mensagens de texto vão, mas **os áudios do relógio não** (o WhatsApp abre a conversa sem o áudio). Para mandar áudios remova o WhatsApp clonado; duas contas no mesmo WhatsApp não têm problema. O Gateway avisa com ⚠️ no botão de envio de WhatsApp.
- **Beeper (experimental)**: se você usa o [Beeper](https://play.google.com/store/apps/details?id=com.beeper.android) com WhatsApp e Telegram vinculados, toque em *🧪 Beeper* no Gateway e permita o acesso: as mensagens de texto vão sem abrir o WhatsApp e sem acessibilidade, mesmo com o celular bloqueado, e no Telegram você pode escrever para qualquer conversa. Os áudios continuam passando pelo WhatsApp.
  Sem ele, o celular acorda e a mensagem vai quando você desbloquear.
- **Comandos da casa com o celular bloqueado**: app Google → Configurações → Google Assistente → Tela de bloqueio → resultados pessoais ativados.

**Alarme do celular**: quando toca, o relógio vibra e abre sozinho os botões **Desligar** e **Soneca**. O relógio fica sabendo a hora do próximo alarme toda vez que você abre o Live Assistant (e depois de cada alarme): se criar um alarme novo no celular, abra o app no relógio uma vez. ⚠ Em **modo dormir** ou **Não perturbe** o relógio bloqueia os apps de terceiros: programe o modo dormir / Não perturbe para terminar alguns minutos antes do alarme (Configurações do relógio → Não perturbe → Programado).

**Gemini Live (teste)**: no app Zepp → Live Assistant → Configurações ative **Usar o Gemini Live** (precisa do Gateway Assistant 1.65 ou posterior no mesmo celular). A resposta já chega como voz, sem esperar a síntese; se o Live falhar, o método normal é usado.

## Relógio Huawei (Watch 3, Watch 4)
Para os **Huawei Watch 3 e Watch 4** (os baseados em Android) existe o **Live Assistant**, com **Gemini Live**: enquanto você fala, a pergunta já vai para o Gemini e a resposta volta direto como voz, normalmente em 1-3 segundos. Funciona com o Wi-Fi ou LTE do relógio e também só por Bluetooth, pelo Gateway. É instalado pelo **Gateway Assistant**, sem computador.
1. No relógio: Configurações → Sobre → toque várias vezes no **número da versão**. Depois, nas **Opções do desenvolvedor**, ative a **depuração HDC** e a **Depuração por Wi-Fi**.
2. Relógio e celular no **mesmo Wi-Fi** (o roteador do celular serve).
3. No Gateway Assistant toque em **⌚ Relógio Huawei: instalação e diagnóstico**, digite o IP mostrado em *Depuração por Wi-Fi* e toque em **Baixar e instalar o Live Assistant**. Na primeira vez o relógio pede para permitir a conexão: toque em **Sempre permitir**.
   O Gateway passa para o relógio o código de canal e, se a caixa estiver marcada, sua chave Gemini; também tira o app da economia de bateria.
4. No Gateway Assistant toque em **⚪ Permitir Bluetooth Huawei** até aparecer **✅ Bluetooth Huawei: ativado**: o relógio passa a funcionar **sem Wi-Fi nem LTE**, pelo Bluetooth do celular.
5. **Botão de baixo**: na mesma página toque em **Botão de baixo: abrir o Live Assistant**. O botão de baixo do relógio passa a abrir o Live Assistant, já ouvindo, em vez da Celia (*Restaurar a Celia* desfaz).

No relógio, a **engrenagem** embaixo de *Nova conversa* abre as configurações (cidade, conexão Auto/Bluetooth/Internet, voz, atualizações, diagnóstico); a **coroa** rola as páginas. Perguntas, voz, clima e notícias, casa Google, Contatos e WhatsApp, ligações, comandos rápidos, lembretes, lanterna, volume e brilho, passos e frequência cardíaca funcionam todos. Por voz você também pode mudar o **DPI da tela** ("coloca o dpi em 280", "restaura o dpi"; de 90 a 400, padrão 320); as configurações do relógio têm **Restaurar DPI** e o Gateway (página do relógio Huawei, seção *DPI da tela*) tem **Aplicar** e **Restaurar (320)**.
**Alarme do celular**: quando toca, o relógio vibra e mostra **Parar** e **Soneca** (mesmo no modo noturno, que é desativado um minuto antes; Soneca ativa de novo). Também funciona com alarmes de última hora: no app Saúde → Dispositivos → relógio → Notificações ative o **Gateway Assistant**.
**Atualizações**: o Gateway Assistant mostra a versão instalada e a nova; atualize na mesma página ou pelo relógio (Configurações → *Verificar e instalar*, com a Depuração por Wi-Fi ativada).
**Groq (opcional)**: o Live responde sozinho às perguntas gerais; os comandos (casa, ligações, WhatsApp, alarmes, clima, notícias) são executados pelo app e, com uma chave Groq, a parte de texto fica pronta em cerca de 1 segundo. Chave grátis: https://console.groq.com → *API Keys* → *Create API Key* (começa com `gsk_`) e cole no Gateway → *🔑 Chaves API* → *Salvar a chave Groq*.
**Diagnóstico**: chega sozinho ao Gateway (página do relógio Huawei; pelo relógio também Configurações → *Enviar para o Gateway Assistant*). Com **Compartilhar** você manda como arquivo de texto (WhatsApp, Telegram, e-mail) para quem está te ajudando.
**Duas chacoalhadas para abrir (teste)**: nas configurações do relógio ative *Teste: duas chacoalhadas fortes abrem o app*. Com a tela ligada, duas chacoalhadas secas e seguidas abrem o Live Assistant ouvindo; com a tela sempre ligada o sensor fica desligado para economizar bateria: levante o pulso para ligar a tela de novo. O botão de baixo também funciona.
**Economia de energia Huawei**: o relógio pode fechar o Live Assistant em segundo plano (o botão de baixo e as chacoalhadas param de funcionar até você abrir o app de novo). No Gateway, página do relógio Huawei, toque em **PowerGenie: remover** (se o relógio não permitir, ele fica desativado; **PowerGenie: restaurar** desfaz). Se a Depuração por Wi-Fi ficar ativada e você estiver na mesma rede, o Gateway reativa sozinho o Live Assistant quando o relógio fecha ele.

### Instalar seus próprios apps no relógio
Na mesma página do Gateway, seção **Instalar seus próprios apps no relógio**: toque em **📲 Escolher o app para instalar** e escolha o arquivo baixado. Funcionam **APKs** simples e pacotes divididos **APKS**, **XAPK** (com arquivos OBB) e **APKM**. Precisa da Depuração por Wi-Fi, como para o Live Assistant. Na caixa embaixo você pode digitar um **comando adb** (ex. `pm list packages -3` para listar os apps instalados) (seção **Executar no relógio**) e tocar em **Executar**: o resultado aparece embaixo e **Copiar o resultado** copia.

## Relógio Wear OS (beta)
O Live Assistant também funciona em **relógios Wear OS a partir do Android 9**, redondos e retangulares (Galaxy Watch, Pixel Watch, Oppo Watch, Mi Watch, TicWatch, Fossil…), incluindo os antigos **Wear OS 2 e 3**, onde o Google Assistente e o WhatsApp não funcionam mais. É o mesmo app do Huawei: perguntas por voz com o Gemini Live, clima gráfico, Casa, Contatos, WhatsApp e Telegram pelo Gateway.
**Conexão com o celular**: primeiro o canal oficial do Wear OS (Bluetooth, Wi-Fi ou rede, escolhido pelo Wear OS), depois o Bluetooth direto. O Gateway passa para o relógio as chaves e o código de canal: também funciona longe do celular se o relógio tiver rede.

**Instalação** — no Gateway Assistant toque em **⌚ Relógio Wear OS: instalação e diagnóstico**. Primeiro, no relógio, ative as **Opções do desenvolvedor**: Configurações → Sobre (no Galaxy *Sobre o relógio → Informações do software*) → toque várias vezes em **Versão do software** ou **Número da versão**. Relógio e celular no **mesmo Wi-Fi** (o roteador do celular serve). Depois escolha a conexão:
- **Depuração sem fio (Wear OS 4 e posterior)**: Opções do desenvolvedor → **Depuração sem fio** ativada (*Sempre permitir nesta rede*).
  1. No relógio abra **Parear novo dispositivo** (aparece um código de 6 dígitos).
  2. No Gateway digite **só o código** e toque em **🔗 Parear**: IP, porta de conexão e porta de pareamento são encontrados automaticamente na rede (botão **🔍 Encontrar o relógio**; também dá para digitar nos campos). Depois do pareamento o botão fica verde, **Pareado ✓**: não precisa refazer.
  3. Toque em **⬇ Baixar e instalar o Live Assistant**. A porta de conexão muda toda vez que você reativa a Depuração sem fio: se um comando não conectar, apague o campo da porta e o Gateway encontra de novo.
- **Depurar por Wi-Fi (Wear OS 2 e 3)**: Opções do desenvolvedor → **Depuração ADB** e **Depurar por Wi-Fi** ativadas. Digite o IP do relógio (a porta já é **5555**) e toque em **⬇ Baixar e instalar o Live Assistant**; no relógio aceite a depuração (**Sempre permitir**).

O Gateway instala o app, dá as permissões (microfone, sensores, atualizações), tira da economia de bateria, passa as chaves e abre o app. Cada botão mostra os passos em uma janela (**Copiar** para mandar para quem te ajuda).
No **Pixel Watch**, se o ícone não aparecer na lista de apps depois de instalar, reinicie o relógio.
**Botão para abrir o Live** — nas configurações do Live no relógio (engrenagem): *Segurar o botão Início: Live em vez do assistente Google*; no **Galaxy Watch Ultra** o **botão do meio (laranja)**: nas configurações dos botões da Samsung escolha **Nenhum app**, depois no Live toque em **Aprender o app do botão** e aperte o botão uma vez. Se o guardião do botão não estiver ativo, no Gateway toque em **🔑 Dar as permissões ao Live**.
**Notificações do celular (só Huawei)**: Gateway → página do relógio Huawei → **🔔 Notificações do celular no relógio**: escolha os apps (toque para mudar: desativado → *perto*, por Bluetooth → *também longe*, também pela internet, no máximo 40 por dia). Ignorada ou tocada no relógio, a notificação também some do celular. No Wear OS e no Amazfit as notificações já chegam pelos próprios apps.
**Telegram no relógio** (Wear OS e Huawei): quando o celular não está conectado por Bluetooth, por LTE ou Wi-Fi você lê e envia Telegram (textos, áudios, fotos) direto do relógio. Vincule uma vez, perto do celular e com o *Telegram direto* ativado no Gateway: configurações do Live no relógio → **Vincular o Telegram (pelo celular)**. O Gateway aceita o login sozinho; com a verificação em duas etapas o relógio pede a senha. O relógio aparece no Telegram → Dispositivos como *Live Assistant (orologio)*. A conexão só abre quando precisa e fecha depois de 2 minutos.
**Atualizações**: no relógio, engrenagem → *Verificar e instalar*. No Wear OS 4 e posterior o app se atualiza sozinho (na primeira vez permita *Instalar apps desconhecidos* e depois confirme); no Wear OS 2 e 3 passa pela Depuração por Wi-Fi, que precisa ficar ativada.
**Na mesma página**: *Enviar as chaves para o relógio*; **DPI da tela** (*Restaurar* volta ao DPI de fábrica do modelo, ex. 340 na Samsung); **Instalar seus próprios apps** (APK, APKS, XAPK, APKM); **Executar no relógio** (comandos adb); **Diagnóstico** do relógio (com modelo e versão do Android).
**Botão**: no Galaxy Watch, Configurações → Recursos avançados → Personalizar teclas → *Pressionar duas vezes* → **Live Assistant**. Para o botão central do Galaxy Watch Ultra estamos preparando o guardião do botão: no Gateway toque em **🔎 Estudar os botões**, aperte os botões do relógio por 15 segundos e envie o resultado.

## Relógio HarmonyOS (Watch 5, Watch 6, Watch Ultimate 2…) (beta)
Para os relógios Huawei com **HarmonyOS NEXT** (ex. Watch 5, Watch 6, Watch Ultimate 2), que não instalam APK, existe o **Live Assistant para HarmonyOS**. Ele tem as mesmas funções das outras versões: perguntas por voz com o Gemini Live, previsão do tempo, Casa, Contatos, WhatsApp e Telegram, alarmes do celular, histórico. Ele é instalado pelo **Gateway Assistant**, sem computador.
**Por que é preciso uma conta de desenvolvedor Huawei**: o HarmonyOS só instala apps assinados com um perfil que contém o identificador (UDID) do seu relógio. O Gateway cria a chave, o certificado e o perfil com a **sua** conta, do mesmo jeito que o DevEco Studio. Eles ficam só no seu celular e não são compartilhados.

**1 · Conta de desenvolvedor Huawei (uma vez)**
1. Abra https://developer.huawei.com, faça login com seu **ID Huawei** (serve o do app Saúde) e conclua o **cadastro como desenvolvedor** (gratuito, conta individual). Para a verificação de identidade são necessários um documento válido (RG/carteira de identidade ou passaporte) e um cartão de crédito: espere até aparecer aprovada.
2. No Gateway Assistant toque em **⌚ Relógio HarmonyOS: conexão e diagnóstico** → **🔏 Arquivos de assinatura para as HAP** → **🔐 Perfis automáticos: faça login com a conta Huawei (como o DevEco)**.
3. O navegador abre: faça login com a conta de desenvolvedor e confirme. O navegador volta sozinho ao Gateway, que mostra **✅ Login feito**; o botão vira **🔐 Conta Huawei:** com seu nome (tocando nele você sai).
Não precisa de mais nada: a chave e o certificado de depuração são criados sozinhos na primeira instalação (ou na hora, com **🪄 Criar chave e certificado com a conta Huawei**). Cada conta pode ter no máximo 3 certificados de depuração (o do Gateway é substituído sozinho): se você já tem 3 feitos com o DevEco Studio e o Gateway avisar, apague um antigo no AppGallery Connect (*Certificados, IDs de apps e perfis → Certificados*).

**2 · Prepare o relógio**
1. No relógio: Configurações → Sobre → toque várias vezes na **versão** até aparecerem as **Opções do desenvolvedor**.
2. Nas Opções do desenvolvedor ative a **depuração (HDC)** e a **depuração Wi-Fi**: o relógio mostra **IP e porta** (ex. 192.168.0.191:44911). A porta muda toda vez que você reativa a depuração.
3. Relógio e celular na **mesma rede Wi-Fi** (serve o hotspot do celular).

**3 · Instale o Live Assistant**
1. No Gateway: **⌚ Relógio HarmonyOS** → **📲 Instalar ou atualizar o Live no relógio**.
2. Digite o **IP** e a **porta** do relógio, ou toque em **🔎 Procurar o relógio no Wi-Fi** (com o IP já digitado ele encontra a porta em poucos segundos).
3. Toque em **⬇ Do site**. O Gateway baixa o Live Assistant, registra o relógio na sua conta, cria o perfil, assina o app, instala e abre já conectado ao Gateway (código do canal e chaves). Na janela você vê cada passo, até **✅ Pronto**.
4. Na primeira vez o relógio pede para **permitir a conexão** de depuração: aceite.
Se o relógio já tiver um Live Assistant assinado por outra pessoa, o Gateway pergunta se deve desinstalá-lo antes (os dados do app no relógio são perdidos).

**Atualizações**: o Gateway Assistant mostra quando há uma versão nova. A atualização é igual (📲 Instalar ou atualizar → ⬇ Do site), com a depuração Wi-Fi ativa; configurações e dados continuam.
**Conexão com o celular**: o Live tenta sozinho o Wi-Fi direto (mesma rede), o Bluetooth e por último a internet (Wi-Fi ou LTE do relógio) com o código do canal. Para usar o Bluetooth: no relógio ⚙ → **🔵 Testar Bluetooth com o Gateway** (permita o Bluetooth).
**Live em segundo plano (beta)**: em ⚙ → **🌙 Live em segundo plano** o relógio recebe os avisos de mensagens por Bluetooth mesmo com o app fechado e verifica alarmes e mensagens a cada 30 minutos. Gasta um pouco mais de bateria e antes é preciso o teste de Bluetooth dar certo.
**Diagnóstico**: no relógio ⚙ → Diagnóstico → 📤 Gateway; no Gateway fica em ⌚ Relógio HarmonyOS → **Diagnóstico**.
**Já tem seus arquivos de assinatura?** (para quem usa o DevEco Studio): em **🔏 Arquivos de assinatura para as HAP** você carrega a chave **.p12** com a senha, o certificado de depuração **.cer** e os perfis **.p7b** (um por app, com o UDID do relógio, que você copia em **🛠 Ferramentas hdc** → **📋 Identificador do relógio (UDID)**). O botão **🤖 Perfis automáticos (AppGallery Connect)** usa as APIs oficiais, que não funcionam com contas europeias: nesse caso use o login com a conta Huawei.
**Outras ferramentas** (🛠 Ferramentas hdc): **🔑 Enviar ao Live a chave Gemini e o canal**, comandos no relógio. Com **Escolher a HAP** você instala também outros apps HarmonyOS: se a conta Huawei estiver conectada, o Gateway assina sozinho.

## Com um iPhone
O Gateway Assistant é só para Android: o iOS não deixa um app ficar sempre ativo, apertar "Enviar" no WhatsApp, ler notificações ou passar frases para o Google Assistente.
**O Live Assistant funciona mesmo assim com um iPhone**: perguntas ao Gemini, voz, clima, notícias, lembretes, volume, brilho e lanterna.
Não disponível: comandos da casa Google, ligações por nome dos contatos, envio e leitura de WhatsApp, voz reserva do celular.
- Pule o passo 1 e deixe **Gateway Assistant → Código** vazio.
- Mantenha o **app Zepp aberto em segundo plano** (não feche deslizando): se o iOS suspender, o relógio diz "celular inacessível".
- As ligações normais no relógio funcionam com as chamadas por Bluetooth do app Zepp.

## Gestos do pulso (chacoalhadas)
Úteis com barulho ou com as mãos ocupadas. São ativados e desativados nas configurações do app no relógio (Huawei) e funcionam com o app aberto:
- **Uma chacoalhada enquanto ouve**: envia a pergunta na hora, sem esperar o silêncio.
- **Uma chacoalhada enquanto pensa** (cores girando): cancela a pergunta.
- **Uma chacoalhada enquanto fala**: para a voz.
- **Uma chacoalhada parado**: nova pergunta (ouve de novo).
- **Duas chacoalhadas**: fecham o app. Dê a segunda depois de uma pausa curta e **mais forte** que a primeira, para que uma segunda tentativa normal não feche por engano.
- **Botão Parar (Huawei e Amazfit)**: desde que começa a ouvir até a resposta chegar, um botão vermelho **■ Parar** substitui *Nova conversa*: cancela a pergunta sem enviar (ou ignora a resposta que está chegando) e os comandos dessa pergunta não são executados. Um toque no botão central enquanto ouve envia na hora. Quando uma mensagem de WhatsApp/Telegram ou um áudio é enviado, aparece um grande **✓ verde** com uma vibração e um som curto (sem som no modo privacidade); se falhar, um **✗ vermelho**.
As chacoalhadas não contam nos primeiros 2 segundos depois de abrir. Depois de **30 segundos** sem atividade o app volta sozinho para o mostrador.

## O que você pode dizer
- "Como vai estar o tempo amanhã?", "Como foi o Flamengo?", qualquer pergunta (nas perguntas de clima o relógio também mostra um **cartão gráfico**: agora, próximas horas e próximos dias)
- "Acende a luz da cozinha", "boa noite"
- "Liga pro Mário" (se houver vários Mários você toca em um no relógio)
- "Manda um WhatsApp pro Mário: chego em dez minutos" (toque em **Enviar para …** para confirmar)
- "Lê minhas mensagens do WhatsApp", "responde pra Ana: combinado"
- "Responde no Telegram pro Lucas: tô chegando" (só para conversas de Telegram com uma notificação recente; "lê minhas mensagens" mostra também as do Telegram)
- "Manda um áudio pro Mário": toque no contato 🎤, fale e toque de novo para enviar. Chega como áudio do WhatsApp; no Huawei precisa do Bluetooth com o celular (ou, na página Contatos, **segure WhatsApp** em um favorito: a gravação começa na hora)
- "Desliga o alarme de amanhã", "para o alarme", "soneca no alarme" (alarmes do **celular**)
- "Coloca dentista na agenda na quinta às 10, me avisa uma hora antes", "o que eu tenho amanhã?" (agenda do **celular**: no Gateway Assistant toque em **Permitir Agenda**)
- "Adiciona leite na lista de compras", "anota: comprar lâmpadas", "me lembra amanhã às 9 no Google Tasks de ligar pro Lucas" (**Keep** e **Tasks**: o Gateway digita a frase para o Gemini no celular; precisa da acessibilidade do Gateway Assistant e das extensões Keep e Tasks ativadas no Gemini)
- "Ativa o Não perturbe até as 7", "desativa o Não perturbe" (Não perturbe do **celular**: no Gateway Assistant toque em **Permitir Não perturbe**; valem as exceções definidas no celular)
- "Me lembra às 18 de ligar pro dentista", "alarme às 7", "aumenta o volume"

**Comandos rápidos e favoritos**: no Gateway Assistant, seção "No relógio: comandos rápidos e favoritos", adicione botões com uma frase para o Assistente (ex. "Shield" → "ligar a Shield") e contatos favoritos da sua agenda. No relógio, ao lado do botão central: o ícone **casa** (ou a seta **‹**) abre **Casa**, com seus botões (vão direto para o Assistente do celular, sem Gemini) e **Não perturbe** para ativar e desativar; o ícone **mensagens** (ou a seta **›**) abre **Contatos**, com seus favoritos e os botões **WhatsApp** (diga a mensagem e confirme com Enviar) e **Ligar**.

**Favoritos e grupos**: até **16 favoritos** entre contatos e grupos. Com **+ Adicionar grupo do WhatsApp** e **+ Adicionar grupo do Telegram** você escolhe um grupo: no relógio ele ganha um cartão próprio com a última mensagem (e quem escreveu), os balões e as respostas. **Avisos**: quando um favorito te escreve (ou em um grupo favorito) o relógio mostra o nome e uma prévia, e um toque abre a conversa daquele app. Com o WhatsApp e o Telegram diretos, os avisos chegam mesmo se o celular não mostrar nenhuma notificação.

**Modo privacidade**: toque no botão **microfone** embaixo à direita do botão central: ele vira um **teclado** verde: o microfone fica desligado e o botão central abre o teclado; digite sua pergunta e a resposta volta só em texto, sem voz. Toque de novo para voltar à voz. Para uma única pergunta digitada você também pode **segurar** o botão central. Precisa de um relógio com Zepp OS 4 ou posterior.

## Se algo der errado
- App Zepp → Live Assistant → **Diagnóstico**: mostra o que aconteceu em cada pergunta. Também chega ao Gateway Assistant (**⌚ Relógio Amazfit: diagnóstico**): de lá você copia ou manda como arquivo com **Compartilhar arquivo**.
- No Gateway Assistant o **Registro** mostra ligações, mensagens e comandos.
- O gateway precisa estar ativo ("Gateway ativo ✓") com a bateria sem restrições.
- **🐞 Relatar um problema** no Gateway, ou por voz pelo relógio ("relatar um problema: o botão do WhatsApp não funciona"): o relatório chega ao desenvolvedor com o registro e o diagnóstico dos relógios, com os textos das mensagens e os números ocultados. Na primeira vez pede consentimento. O Gateway também relata sozinho os problemas repetidos (no máximo uma vez por dia por tipo).
- O botão do gateway fica **verde** quando está ativo e **vermelho** quando está parado.
- **Contagem anônima de uso**: uma vez por dia o Gateway envia só um identificador aleatório e as versões dos apps, sem dados pessoais. Desative com **📊 Contagem anônima de uso**.

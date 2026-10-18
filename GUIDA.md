# Live Assistant (orologio) + Gateway Assistant (telefono) — guida rapida

Con l'orologio Amazfit (Zepp OS), Huawei Watch 3 / Watch 4 o **Wear OS** (Galaxy Watch, Pixel Watch, TicWatch…) parli con Gemini e, tramite l'app **Gateway Assistant** sul telefono Android, puoi:
comandare la casa Google, chiamare, mandare/leggere/rispondere ai WhatsApp e avere la voce del telefono.
Ognuno usa il proprio telefono, il proprio account Google e la propria chiave Gemini: niente da condividere.

🌐 Le app parlano **italiano, inglese e spagnolo**: seguono da sole la lingua dell'orologio e del telefono. · *English: [GUIDE.md](GUIDE.md)* · *Español: [GUIA.md](GUIA.md)*

## Cosa serve
- Telefono Android con l'app **Zepp** e l'orologio già collegato
- Una **chiave API Gemini** (gratuita, o con credito per risposte più veloci): https://aistudio.google.com/apikey
- L'app **Google** (Assistente) sul telefono, collegata alla tua casa Google Home (solo per i comandi di casa)

## Chiavi API
Le chiavi si inseriscono **una volta sola** in Gateway Assistant → **🔑 Chiavi API** e valgono per tutti gli orologi; dalla pagina di ogni orologio le passi a Live con *Invia le chiavi all'orologio* (o all'installazione).
- **Gemini** (necessaria, gratuita): apri https://aistudio.google.com/apikey con il tuo account Google → **Create API key** (o *Crea chiave API*) → scegli o crea un progetto → copia la chiave (inizia con `AIza` o `AQ.`) e incollala in Gateway → *Salva chiave Gemini*. Con il piano gratuito ci sono limiti giornalieri; con un po' di credito le risposte sono più veloci.
- **Groq** (facoltativa, gratuita): apri https://console.groq.com/keys, accedi (anche con Google) → **Create API Key** → dagli un nome → copia la chiave (inizia con `gsk_`, si vede una volta sola) e incollala in Gateway → *Salva chiave Groq*. Serve per le risposte scritte in circa 1 secondo.
- Per togliere una chiave tieni premuto il suo pulsante *Salva*.

## 1 · Installa Gateway Assistant (telefono)
1. Scarica l'APK dal telefono: **https://github.com/Kkaoss969/gateway-assistant-download/raw/main/GatewayAssistant.apk**
2. Aprilo e consenti l'installazione da questa fonte, se Android lo chiede.
3. Apri **Gateway Assistant** e tocca **Avvia il gateway**.
4. Nella lista **Permessi** tocca ogni riga con ⚪ finché diventano tutte ✅:
   contatti e chiamate · mostra sopra altre app · invio WhatsApp (accessibilità) · lettura WhatsApp (notifiche) · batteria senza restrizioni.
   ⚠ **Accessibilità**: nella pagina di Android "Gateway Assistant (invio WhatsApp)" attiva **solo il primo interruttore in alto** ("Attivato"). **Non attivare** il secondo, "Collegamento a Gateway Assistant": è solo una scorciatoia di Android e, se acceso, i tocchi automatici (Invia di WhatsApp, Spegni/Posticipa della sveglia, invio a Gemini) non funzionano.
   Se un'impostazione risulta "con restrizioni": Impostazioni → App → Gateway Assistant → menu ⋮ → *Consenti impostazioni con restrizioni*.
5. Tocca **Copia codice** (il codice del canale).

## 2 · Installa Live Assistant sull'orologio
1. Nell'app Zepp attiva la modalità sviluppatore: Profilo → Impostazioni → Informazioni → tocca più volte il logo Zepp.
2. Apri il sito **https://kkaoss969.github.io/gateway-assistant-download/**, scegli il tuo orologio e scansiona il **codice QR** con l'app Zepp (Profilo → icona di scansione).
3. Nell'app Zepp apri le impostazioni dell'app **Live Assistant** e compila:
   - **Chiave API Gemini**
   - **La mia città** (meteo e notizie locali)
   - **Gateway Assistant → Codice**: incolla il codice copiato al punto 1
   - **Chiave API Groq** (facoltativa, gratuita da https://console.groq.com → *API Keys*): notizie e domande scritte rispondono in circa 1 secondo; le domande a voce restano a Gemini
   - **Nomi che usi spesso** (facoltativo): persone, paesi, squadre… aiutano a capire i nomi giusti

## 3 · Consigliato
- **Chiamate sull'orologio**: app Zepp → Profilo → orologio → Impostazioni app → Telefono → *Chiama sull'orologio* (e associa il Bluetooth).
- **WhatsApp a telefono bloccato**: Impostazioni → Sicurezza → Smart Lock / Sblocco esteso → *Dispositivi attendibili* → aggiungi l'orologio.
- **WhatsApp doppio (clone)**: se sul telefono hai un secondo WhatsApp clonato (Dual Messenger dei Samsung, "App doppie" su altri telefoni), i messaggi di testo partono ma i **vocali dall'orologio no** (WhatsApp apre la chat senza l'audio). Per mandare i vocali elimina il WhatsApp clonato; due account nello stesso WhatsApp invece vanno bene. Gateway lo segnala con ⚠️ sul pulsante dell'invio WhatsApp.
- **Beeper (sperimentale)**: se usi [Beeper](https://play.google.com/store/apps/details?id=com.beeper.android) con WhatsApp e Telegram collegati, in Gateway tocca *🧪 Beeper* e consenti l'accesso: i messaggi di testo partono senza aprire WhatsApp e senza accessibilità, anche a telefono bloccato, e su Telegram puoi scrivere a qualsiasi chat. I vocali passano ancora da WhatsApp.
  Senza, il telefono si accende e il messaggio parte quando lo sblocchi.
- **Comandi di casa a telefono bloccato**: app Google → Impostazioni → Assistente Google → Schermata di blocco → risposte personali attive.

**Sveglia del telefono**: quando suona, l'orologio vibra e apre da solo i tasti **Spegni** e **Posticipa**. L'orologio impara l'ora della prossima sveglia ogni volta che apri Live Assistant (e dopo ogni sveglia): se crei una sveglia nuova sul telefono, apri l'app sull'orologio una volta. ⚠ In **modalità notte** o **non disturbare** l'orologio blocca le app esterne: programma la modalità notte / non disturbare in modo che finisca qualche minuto prima della sveglia (Impostazioni dell'orologio → Non disturbare → Programmato).

**Gemini Live (prova)**: nell'app Zepp → Live Assistant → Impostazioni accendi **Usa Gemini Live** (serve Gateway Assistant 1.65 o successivo sullo stesso telefono). La risposta arriva già a voce, senza aspettare la sintesi; se Live non risponde si usa il metodo normale.

## Orologio Huawei (Watch 3, Watch 4)
Per gli orologi **Huawei Watch 3 e Watch 4** (quelli con base Android) c'è **Live Assistant**, con **Gemini Live**: mentre parli la domanda parte già verso Gemini e la risposta arriva direttamente a voce, di solito in 1-3 secondi. Funziona con il Wi-Fi o l'LTE dell'orologio e anche solo via Bluetooth tramite Gateway. Si installa da **Gateway Assistant**, senza computer.
1. Sull'orologio: Impostazioni → Informazioni → tocca più volte il **numero di build**. Poi in **Opzioni sviluppatore** attiva **Debug HDC** e **Debug via Wi-Fi**.
2. Orologio e telefono sulla **stessa rete Wi-Fi** (va bene anche l'hotspot del telefono).
3. In Gateway Assistant tocca **⌚ Orologio Huawei: installa e diagnostica**, scrivi l'IP mostrato sotto *Debug via Wi-Fi* e tocca **Scarica e installa Live Assistant**. La prima volta l'orologio chiede di consentire il collegamento: tocca **Consenti sempre**.
   Gateway passa all'orologio il codice del canale e, se la spunta è attiva, la tua chiave Gemini; esclude anche l'app dal risparmio batteria.
4. In Gateway Assistant tocca **⚪ Consenti Bluetooth Huawei** finché diventa **✅ Bluetooth Huawei: attivo**: così l'orologio funziona anche **senza Wi-Fi né LTE**, tramite il Bluetooth del telefono.
5. **Tasto inferiore**: nella stessa pagina tocca **Tasto inferiore: apri Live Assistant**. Premendo il tasto inferiore dell'orologio si apre Live Assistant già in ascolto al posto di Celia (*Ripristina Celia* torna come prima).

Sull'orologio l'**ingranaggio** sotto *Nuova chat* apre le impostazioni (città, collegamento Auto/Bluetooth/Internet, voce, aggiornamenti, diagnostica); la **corona** scorre le pagine. Funzionano domande, voce, meteo e notizie, casa Google, Contatti e WhatsApp, chiamate, comandi rapidi, promemoria, torcia, volume e luminosità, passi e battito. A voce puoi cambiare anche i **DPI dello schermo** ("metti i dpi a 280", "ripristina i dpi"; da 90 a 400, standard 320); nelle impostazioni dell'orologio c'è **Ripristina i DPI**, e in Gateway (pagina dell'orologio Huawei, sezione *DPI dello schermo*) **Imposta** e **Ripristina (320)**.
**Sveglia del telefono**: quando suona, l'orologio vibra e mostra **Spegni** e **Posticipa** (anche in modalità notte, che viene spenta un minuto prima; con Posticipa si riaccende). Funziona anche con le sveglie create all'ultimo momento: in app Salute → Dispositivi → orologio → Notifiche attiva **Gateway Assistant**.
**Aggiornamenti**: Gateway Assistant mostra la versione installata e quella nuova; aggiorni dalla stessa pagina o dall'orologio (Impostazioni → *Controlla e installa*, con il Debug via Wi-Fi attivo).
**Groq (facoltativo)**: Live risponde da solo alle domande generali; i comandi (casa, chiamate, WhatsApp, sveglie, meteo, notizie) li esegue l'app e, con una chiave Groq, la parte scritta è pronta in circa 1 secondo. Chiave gratuita: https://console.groq.com → *API Keys* → *Create API Key* (inizia con `gsk_`) e incollala in Gateway → *🔑 Chiavi API* → *Salva chiave Groq*.
**Diagnostica**: arriva da sola in Gateway (pagina dell'orologio Huawei; dall'orologio anche Impostazioni → *Invia a Gateway Assistant*). Con **Condividi** la mandi come file di testo (WhatsApp, Telegram, email) a chi ti aiuta.
**Due scossoni per aprire (prova)**: nelle impostazioni dell'orologio accendi *Prova: due scossoni forti aprono l'app*. Con lo schermo acceso due scossoni secchi e ravvicinati aprono Live Assistant in ascolto; con lo schermo sempre attivo il sensore è spento per risparmiare batteria: alza il polso per riaccendere lo schermo. Funziona anche il tasto inferiore.
**Risparmio energetico Huawei**: l'orologio può chiudere Live Assistant in sottofondo (tasto inferiore e scossoni smettono di funzionare finché non riapri l'app). In Gateway, pagina dell'orologio Huawei, tocca **PowerGenie: rimuovi** (se l'orologio non lo permette, lo disattiva; **PowerGenie: rimetti** torna come prima). Se il Debug via Wi-Fi resta attivo e sei sulla stessa rete, Gateway riattiva da solo Live Assistant quando l'orologio lo chiude.

### Installa le tue app sull'orologio
Nella stessa pagina di Gateway, sezione **Installa le tue app sull'orologio**: tocca **📲 Scegli l'app da installare** e scegli il file scaricato. Vanno bene gli **APK** singoli e i pacchetti divisi **APKS**, **XAPK** (anche con i file OBB) e **APKM**. Serve il Debug via Wi-Fi, come per Live Assistant. Nella casella sotto puoi scrivere un **comando adb** (es. `pm list packages -3` per l'elenco delle app installate) (sezione **Esegui sull'orologio**) e toccare **Esegui**: il risultato compare sotto e lo copi con **Copia risultato**.

## Orologio Wear OS (prova)
Live Assistant funziona anche sugli orologi **Wear OS da Android 9 in poi**, tondi e rettangolari (Galaxy Watch, Pixel Watch, Oppo Watch, Mi Watch, TicWatch, Fossil…), compresi i vecchi **Wear OS 2 e 3** dove l'Assistente Google e WhatsApp non funzionano più. È la stessa app dell'Huawei: domande a voce con Gemini Live, meteo grafico, Casa, Contatti, WhatsApp e Telegram tramite Gateway.
**Collegamento con il telefono**: prima il canale ufficiale di Wear OS (Bluetooth, Wi-Fi o rete, lo sceglie Wear OS), poi il Bluetooth diretto. Gateway passa all'orologio le chiavi e il codice del canale: funziona anche lontano dal telefono, se l'orologio ha la rete.

**Installazione** — in Gateway Assistant tocca **⌚ Orologio Wear OS: installa e diagnostica**. Prima, sull'orologio, attiva le **Opzioni sviluppatore**: Impostazioni → Informazioni (sul Galaxy *Informazioni sull'orologio → Informazioni software*) → tocca più volte **Versione software** o **Numero build**. Orologio e telefono sulla **stessa rete Wi-Fi** (va bene l'hotspot del telefono). Poi scegli il collegamento:
- **Debug wireless (Wear OS 4 e successivi)**: Opzioni sviluppatore → **Debug wireless** attivo (*Consenti sempre su questa rete*).
  1. Sull'orologio apri **Abbina nuovo dispositivo** (compare un codice di 6 cifre).
  2. In Gateway scrivi **solo il codice** e tocca **🔗 Abbina**: IP, porta di collegamento e porta di abbinamento li trova da solo sulla rete (pulsante **🔍 Trova l'orologio**; si possono anche scrivere a mano nei loro campi). Dopo l'abbinamento il pulsante diventa verde, **Abbinato ✓**: non serve rifarlo.
  3. Tocca **⬇ Scarica e installa Live Assistant**. La porta di collegamento cambia ogni volta che riaccendi il Debug wireless: se un comando non si collega, svuota il campo porta e Gateway la ritrova.
- **Debug via Wi-Fi (Wear OS 2 e 3)**: Opzioni sviluppatore → **Debug ADB** e **Debug via Wi-Fi** attivi. Scrivi l'IP dell'orologio (la porta è già **5555**) e tocca **⬇ Scarica e installa Live Assistant**; sull'orologio accetta il debug (**Consenti sempre**).

Gateway installa l'app, dà i permessi (microfono, sensori, aggiornamenti), la esclude dal risparmio batteria, le passa le chiavi e la apre. Ogni pulsante mostra i passaggi in una finestra (**Copia** per mandarli a chi ti aiuta).
Sul **Pixel Watch**, se dopo l'installazione l'icona non compare nell'elenco delle app, riavvia l'orologio.
**Tasto per aprire Live** — nelle impostazioni di Live sull'orologio (ingranaggio): *Pressione lunga di Home: Live al posto dell'assistente di Google*; sul **Galaxy Watch Ultra** il **tasto centrale (arancione)**: nelle impostazioni Samsung del tasto scegli **Nessuna app**, poi in Live tocca **Impara l'app del tasto** e premi il tasto una volta. Se il guardiano dei tasti non è attivo, in Gateway tocca **🔑 Dai i permessi a Live**.
**Notifiche del telefono (solo Huawei)**: Gateway → pagina dell'orologio Huawei → **🔔 Notifiche del telefono sull'orologio**: scegli le app (tocca per cambiare: spenta → *vicino*, via Bluetooth → *anche lontano*, anche via internet, al massimo 40 al giorno). Cancellata o toccata sull'orologio, la notifica sparisce anche dal telefono. Su Wear OS e Amazfit le notifiche arrivano già dalle loro app.
**Telegram sull'orologio** (Wear OS e Huawei): quando il telefono non è collegato via Bluetooth, in LTE o Wi-Fi leggi e mandi i Telegram (testi, vocali, foto) direttamente dall'orologio. Si collega una volta, vicino al telefono e con *Telegram diretto* attivo in Gateway: impostazioni di Live sull'orologio → **Collega Telegram (dal telefono)**. Gateway accetta l'accesso da solo; se hai la verifica in due passaggi l'orologio chiede la password. L'orologio compare in Telegram → Dispositivi come *Live Assistant (orologio)*. Il collegamento si apre solo quando serve e si chiude dopo 2 minuti.
**Aggiornamenti**: sull'orologio, ingranaggio → *Controlla e installa*. Su Wear OS 4 e successivi l'app si aggiorna da sola (la prima volta consenti *Installa app sconosciute*, poi conferma); su Wear OS 2 e 3 passa dal Debug via Wi-Fi, da lasciare attivo.
**Nella stessa pagina**: *Invia le chiavi all'orologio*; **DPI dello schermo** (*Ripristina* torna ai DPI di fabbrica del modello, es. 340 sui Samsung); **Installa le tue app** (APK, APKS, XAPK, APKM); **Esegui sull'orologio** (comandi adb); **Diagnostica** dell'orologio (con modello e versione di Android).
**Tasto**: sul Galaxy Watch, Impostazioni → Funzioni avanzate → Personalizza tasti → *Premi due volte* → **Live Assistant**. Per il tasto centrale dei Galaxy Watch Ultra stiamo preparando il guardiano del tasto: in Gateway tocca **🔎 Studia i tasti**, premi i tasti dell'orologio per 15 secondi e manda il risultato.

## Con l'iPhone
Gateway Assistant esiste solo per Android: iOS non permette a un'app di restare sempre attiva, premere "Invia" in WhatsApp, leggere le notifiche o passare frasi all'Assistente Google.
**Live Assistant però funziona anche con l'iPhone**: domande a Gemini, voce, meteo, notizie, promemoria, volume, luminosità e torcia.
Non funzionano: comandi per la casa Google, chiamate per nome dalla rubrica, invio e lettura dei WhatsApp, voce del telefono di riserva.
- Salta il passo 1 e lascia vuoto **Gateway Assistant → Codice**.
- Tieni l'**app Zepp aperta in sottofondo** (non chiuderla dal multitasking): se iOS la sospende, l'orologio dice "telefono non raggiungibile".
- Le chiamate normali sull'orologio funzionano con le chiamate Bluetooth dell'app Zepp.

## Gesti del polso (scossoni)
Utili col rumore di fondo o con le mani occupate. Si attivano e si spengono nelle impostazioni dell'app sull'orologio (Huawei) e funzionano con l'app aperta:
- **Uno scossone mentre ascolta**: invia subito la domanda, senza aspettare il silenzio.
- **Uno scossone mentre pensa** (girano i colori): annulla la domanda.
- **Uno scossone mentre parla**: ferma la voce.
- **Uno scossone da fermo**: nuova domanda (ascolta di nuovo).
- **Due scossoni**: chiudono l'app. Il secondo va dato dopo una breve pausa e **più forte** del primo, così un secondo tentativo normale non la chiude per sbaglio.
- **Tasto Stop (Huawei e Amazfit)**: da quando inizia ad ascoltare finché arriva la risposta, al posto di *Nuova chat* c'è un tasto rosso **■ Stop**: annulla la domanda senza inviarla (o scarta la risposta in arrivo) e i comandi di quella domanda non vengono eseguiti. Un tocco sul pulsante centrale mentre ascolta invia subito. Quando un messaggio WhatsApp/Telegram o un vocale parte, compare una grande **✓ verde** con vibrazione e un breve suono (senza suono in modalità privacy); se non parte, una **✗ rossa**.
Nei primi 2 secondi dopo l'apertura gli scossoni non contano. Dopo **30 secondi** senza fare niente l'app torna al quadrante da sola.

## Cosa puoi dire
- "Che tempo fa domani?", "Cosa ha fatto l'Avellino?", qualsiasi domanda (alle domande sul meteo l'orologio mostra anche la **scheda grafica**: adesso, prossime ore e prossimi giorni)
- "Accendi la luce della cucina", "buonanotte"
- "Chiama Mario" (se ci sono più Mario li tocchi sull'orologio)
- "Manda un WhatsApp a Mario: arrivo tra dieci minuti" (tocchi **Invia a …** per confermare)
- "Leggi i messaggi WhatsApp", "rispondi ad Anna: va bene"
- "Rispondi su Telegram a Luca: arrivo" (solo alle chat Telegram con una notifica recente; "leggi i messaggi" mostra anche quelli di Telegram)
- "Manda un vocale a Mario": tocchi il contatto 🎤, parli e tocchi di nuovo per inviare. Arriva come nota vocale di WhatsApp; su Huawei serve il Bluetooth con il telefono (oppure, nella pagina Contatti, **tieni premuto WhatsApp** su un preferito: parte subito la registrazione)
- "Disattiva la sveglia di domani", "ferma la sveglia", "posticipa la sveglia" (sveglie del **telefono**)
- "Segna in calendario il dentista giovedì alle 10, avvisami un'ora prima", "cosa ho domani?" (calendario del **telefono**: in Gateway Assistant tocca **Consenti il Calendario**)
- "Aggiungi il latte alla lista della spesa", "crea una nota: comprare le lampadine", "ricordami domani alle 9 su Google Tasks di chiamare Luca" (**Keep** e **Tasks**: Gateway scrive la frase a Gemini sul telefono; servono l'accessibilità di Gateway Assistant e le estensioni Keep e Tasks attive in Gemini)
- "Attiva il non disturbare fino alle 7", "togli il non disturbare" (Non disturbare del **telefono**: in Gateway Assistant tocca **Consenti il Non disturbare**; valgono le eccezioni impostate sul telefono)
- "Ricordami alle 18 di chiamare il dentista", "sveglia alle 7", "alza il volume"

**Comandi rapidi e preferiti**: in Gateway Assistant, nella sezione "Sull'orologio: comandi rapidi e preferiti", aggiungi pulsanti con una frase per l'Assistente (es. "Shield" → "accendi Shield") e i contatti preferiti dalla rubrica. Sull'orologio, ai lati del pulsante centrale: l'icona della **casa** (o la freccia **‹**) apre **Casa**, con i tuoi pulsanti (vanno subito all'Assistente del telefono, senza passare da Gemini) e il **Non disturbare** da accendere e spegnere; l'icona dei **messaggi** (o la freccia **›**) apre **Contatti**, con i preferiti e i tasti **WhatsApp** (detti il messaggio e confermi con Invia) e **Chiama**.

**Preferiti e gruppi**: fino a **16 preferiti** tra contatti e gruppi. Con **+ Aggiungi gruppo WhatsApp** e **+ Aggiungi gruppo Telegram** scegli un gruppo: sull'orologio ha la sua scheda con l'ultimo messaggio (e chi l'ha scritto), le bolle e la risposta. **Avvisi**: quando ti scrive un preferito (o in un gruppo preferito) l'orologio mostra nome e anteprima, e toccandolo si apre la chat di quell'app. Con WhatsApp e Telegram diretti gli avvisi arrivano anche se il telefono non mostra la notifica.

**Modalità privacy**: tocca il pulsante col **microfono** in basso a destra del pulsante centrale: diventa una **tastiera** verde: il microfono resta spento e il pulsante centrale apre la tastiera; scrivi la domanda e la risposta arriva solo scritta, senza voce. Toccalo di nuovo per tornare alla voce. Per una sola domanda scritta puoi anche **tenere premuto** il pulsante centrale. Serve un orologio con Zepp OS 4 o successivo.

## Se qualcosa non va
- App Zepp → Live Assistant → **Diagnostica**: mostra cosa è successo a ogni domanda. Arriva anche in Gateway Assistant (**⌚ Orologio Amazfit: diagnostica**): da lì la copi o la mandi come file con **Condividi file**.
- In Gateway Assistant il **Diario** mostra chiamate, messaggi e comandi.
- Il gateway deve essere avviato ("Gateway attivo ✓") e con la batteria senza restrizioni.
- **🐞 Segnala un problema** in Gateway, oppure a voce dall'orologio ("segnala un problema: il tasto WhatsApp non va"): la segnalazione arriva allo sviluppatore con il diario e la diagnostica degli orologi, con testi dei messaggi e numeri oscurati. La prima volta chiede il consenso. Gateway segnala da solo anche i problemi che si ripetono (al massimo una volta al giorno per tipo).
- Il pulsante del gateway è **verde** quando è attivo e **rosso** quando è fermo.
- **Conteggio anonimo d'uso**: una volta al giorno Gateway manda solo un identificativo casuale e le versioni delle app, nessun dato personale. Si spegne con **📊 Conteggio anonimo d'uso**.

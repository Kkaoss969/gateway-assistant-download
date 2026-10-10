# Live Assistant (orologio) + Gateway Assistant (telefono) — guida rapida

Con l'orologio Amazfit (Zepp OS) o Huawei Watch 3 / Watch 4 parli con Gemini e, tramite l'app **Gateway Assistant** sul telefono Android, puoi:
comandare la casa Google, chiamare, mandare/leggere/rispondere ai WhatsApp e avere la voce del telefono.
Ognuno usa il proprio telefono, il proprio account Google e la propria chiave Gemini: niente da condividere.

🌐 Le app parlano **italiano, inglese e spagnolo**: seguono da sole la lingua dell'orologio e del telefono. · *English: [GUIDE.md](GUIDE.md)* · *Español: [GUIA.md](GUIA.md)*

## Cosa serve
- Telefono Android con l'app **Zepp** e l'orologio già collegato
- Una **chiave API Gemini** (gratuita, o con credito per risposte più veloci): https://aistudio.google.com/apikey
- L'app **Google** (Assistente) sul telefono, collegata alla tua casa Google Home (solo per i comandi di casa)

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
**Groq (facoltativo)**: Live risponde da solo alle domande generali; i comandi (casa, chiamate, WhatsApp, sveglie, meteo, notizie) li esegue l'app e, con una chiave Groq, la parte scritta è pronta in circa 1 secondo. Chiave gratuita: https://console.groq.com → *API Keys* → *Create API Key* (inizia con `gsk_`) e incollala in Gateway, pagina dell'orologio Huawei → *Salva chiave Groq*.
**Diagnostica**: arriva da sola in Gateway (pagina dell'orologio Huawei; dall'orologio anche Impostazioni → *Invia a Gateway Assistant*). Con **Condividi** la mandi come file di testo (WhatsApp, Telegram, email) a chi ti aiuta.
**Due scossoni per aprire (prova)**: nelle impostazioni dell'orologio accendi *Prova: due scossoni forti aprono l'app*. Con lo schermo acceso due scossoni secchi e ravvicinati aprono Live Assistant in ascolto; con lo schermo sempre attivo funzionano per 2 minuti, poi alza il polso per riaccendere lo schermo. Funziona anche il tasto inferiore.
**Risparmio energetico Huawei**: l'orologio può chiudere Live Assistant in sottofondo (tasto inferiore e scossoni smettono di funzionare finché non riapri l'app). In Gateway, pagina dell'orologio Huawei, tocca **PowerGenie: rimuovi** (se l'orologio non lo permette, lo disattiva; **PowerGenie: rimetti** torna come prima). Se il Debug via Wi-Fi resta attivo e sei sulla stessa rete, Gateway riattiva da solo Live Assistant quando l'orologio lo chiude.

### Installa le tue app sull'orologio
Nella stessa pagina di Gateway, sezione **Installa le tue app sull'orologio**: tocca **📲 Scegli l'app da installare** e scegli il file scaricato. Vanno bene gli **APK** singoli e i pacchetti divisi **APKS**, **XAPK** (anche con i file OBB) e **APKM**. Serve il Debug via Wi-Fi, come per Live Assistant. Nella casella sotto puoi scrivere un **comando adb** (es. `pm list packages -3` per l'elenco delle app installate) (sezione **Esegui sull'orologio**) e toccare **Esegui**: il risultato compare sotto e lo copi con **Copia risultato**.

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
Nei primi 2 secondi dopo l'apertura gli scossoni non contano. Dopo **30 secondi** senza fare niente l'app torna al quadrante da sola.

## Cosa puoi dire
- "Che tempo fa domani?", "Cosa ha fatto l'Avellino?", qualsiasi domanda
- "Accendi la luce della cucina", "buonanotte"
- "Chiama Mario" (se ci sono più Mario li tocchi sull'orologio)
- "Manda un WhatsApp a Mario: arrivo tra dieci minuti" (tocchi **Invia a …** per confermare)
- "Leggi i messaggi WhatsApp", "rispondi ad Anna: va bene"
- "Rispondi su Telegram a Luca: arrivo" (solo alle chat Telegram con una notifica recente; "leggi i messaggi" mostra anche quelli di Telegram)
- "Manda un vocale a Mario" (orologio Huawei): tocchi il contatto 🎤, parli e tocchi di nuovo per inviare. Arriva come file audio, preceduto da un messaggio che dice di ascoltarlo; serve il Bluetooth con il telefono (oppure, nella pagina Contatti, **tieni premuto WhatsApp** su un preferito: parte subito la registrazione)
- "Disattiva la sveglia di domani", "ferma la sveglia", "posticipa la sveglia" (sveglie del **telefono**)
- "Segna in calendario il dentista giovedì alle 10, avvisami un'ora prima", "cosa ho domani?" (calendario del **telefono**: in Gateway Assistant tocca **Consenti il Calendario**)
- "Aggiungi il latte alla lista della spesa", "crea una nota: comprare le lampadine", "ricordami domani alle 9 su Google Tasks di chiamare Luca" (**Keep** e **Tasks**: Gateway scrive la frase a Gemini sul telefono; servono l'accessibilità di Gateway Assistant e le estensioni Keep e Tasks attive in Gemini)
- "Attiva il non disturbare fino alle 7", "togli il non disturbare" (Non disturbare del **telefono**: in Gateway Assistant tocca **Consenti il Non disturbare**; valgono le eccezioni impostate sul telefono)
- "Ricordami alle 18 di chiamare il dentista", "sveglia alle 7", "alza il volume"

**Comandi rapidi e preferiti**: in Gateway Assistant, nella sezione "Sull'orologio: comandi rapidi e preferiti", aggiungi pulsanti con una frase per l'Assistente (es. "Shield" → "accendi Shield") e i contatti preferiti dalla rubrica. Sull'orologio, ai lati del pulsante centrale: l'icona della **casa** (o la freccia **‹**) apre **Casa**, con i tuoi pulsanti (vanno subito all'Assistente del telefono, senza passare da Gemini) e il **Non disturbare** da accendere e spegnere; l'icona dei **messaggi** (o la freccia **›**) apre **Contatti**, con i preferiti e i tasti **WhatsApp** (detti il messaggio e confermi con Invia) e **Chiama**.

**Modalità privacy**: tocca il pulsante col **microfono** in basso a destra del pulsante centrale: diventa una **tastiera** verde: il microfono resta spento e il pulsante centrale apre la tastiera; scrivi la domanda e la risposta arriva solo scritta, senza voce. Toccalo di nuovo per tornare alla voce. Per una sola domanda scritta puoi anche **tenere premuto** il pulsante centrale. Serve un orologio con Zepp OS 4 o successivo.

## Se qualcosa non va
- App Zepp → Live Assistant → **Diagnostica**: mostra cosa è successo a ogni domanda. Arriva anche in Gateway Assistant (**⌚ Orologio Amazfit: diagnostica**): da lì la copi o la mandi come file con **Condividi file**.
- In Gateway Assistant il **Diario** mostra chiamate, messaggi e comandi.
- Il gateway deve essere avviato ("Gateway attivo ✓") e con la batteria senza restrizioni.

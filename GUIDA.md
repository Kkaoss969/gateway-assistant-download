# Voice Assistant (orologio) + Gateway Assistant (telefono) — guida rapida

Con l'orologio Amazfit (Zepp OS) parli con Gemini e, tramite l'app **Gateway Assistant** sul telefono Android, puoi:
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
   Se un'impostazione risulta "con restrizioni": Impostazioni → App → Gateway Assistant → menu ⋮ → *Consenti impostazioni con restrizioni*.
5. Tocca **Copia codice** (il codice del canale).

## 2 · Installa Voice Assistant sull'orologio
1. Nell'app Zepp attiva la modalità sviluppatore: Profilo → Impostazioni → Informazioni → tocca più volte il logo Zepp.
2. Apri il sito **https://kkaoss969.github.io/gateway-assistant-download/**, scegli il tuo orologio e scansiona il **codice QR** con l'app Zepp (Profilo → icona di scansione).
3. Nell'app Zepp apri le impostazioni dell'app **Voice Assistant** e compila:
   - **Chiave API Gemini**
   - **La mia città** (meteo e notizie locali)
   - **Gateway Assistant → Codice**: incolla il codice copiato al punto 1
   - **Nomi che usi spesso** (facoltativo): persone, paesi, squadre… aiutano a capire i nomi giusti

## 3 · Consigliato
- **Chiamate sull'orologio**: app Zepp → Profilo → orologio → Impostazioni app → Telefono → *Chiama sull'orologio* (e associa il Bluetooth).
- **WhatsApp a telefono bloccato**: Impostazioni → Sicurezza → Smart Lock / Sblocco esteso → *Dispositivi attendibili* → aggiungi l'orologio.
  Senza, il telefono si accende e il messaggio parte quando lo sblocchi.
- **Comandi di casa a telefono bloccato**: app Google → Impostazioni → Assistente Google → Schermata di blocco → risposte personali attive.

**Sveglia del telefono**: quando suona, l'orologio vibra e apre da solo i tasti **Spegni** e **Posticipa**. L'orologio impara l'ora della prossima sveglia ogni volta che apri Voice Assistant (e dopo ogni sveglia): se crei una sveglia nuova sul telefono, apri l'app sull'orologio una volta. ⚠ In **modalità notte** o **non disturbare** l'orologio blocca le app esterne: programma la modalità notte / non disturbare in modo che finisca qualche minuto prima della sveglia (Impostazioni dell'orologio → Non disturbare → Programmato).

## Con l'iPhone
Gateway Assistant esiste solo per Android: iOS non permette a un'app di restare sempre attiva, premere "Invia" in WhatsApp, leggere le notifiche o passare frasi all'Assistente Google.
**Voice Assistant però funziona anche con l'iPhone**: domande a Gemini, voce, meteo, notizie, promemoria, volume, luminosità e torcia.
Non funzionano: comandi per la casa Google, chiamate per nome dalla rubrica, invio e lettura dei WhatsApp, voce del telefono di riserva.
- Salta il passo 1 e lascia vuoto **Gateway Assistant → Codice**.
- Tieni l'**app Zepp aperta in sottofondo** (non chiuderla dal multitasking): se iOS la sospende, l'orologio dice "telefono non raggiungibile".
- Le chiamate normali sull'orologio funzionano con le chiamate Bluetooth dell'app Zepp.

## Cosa puoi dire
- "Che tempo fa domani?", "Cosa ha fatto l'Avellino?", qualsiasi domanda
- "Accendi la luce della cucina", "buonanotte"
- "Chiama Mario" (se ci sono più Mario li tocchi sull'orologio)
- "Manda un WhatsApp a Mario: arrivo tra dieci minuti" (tocchi **Invia a …** per confermare)
- "Leggi i messaggi WhatsApp", "rispondi ad Anna: va bene"
- "Disattiva la sveglia di domani", "ferma la sveglia", "posticipa la sveglia" (sveglie del **telefono**)
- "Segna in calendario il dentista giovedì alle 10, avvisami un'ora prima", "cosa ho domani?" (calendario del **telefono**: in Gateway Assistant tocca **Consenti il Calendario**)
- "Attiva il non disturbare fino alle 7", "togli il non disturbare" (Non disturbare del **telefono**: in Gateway Assistant tocca **Consenti il Non disturbare**; valgono le eccezioni impostate sul telefono)
- "Ricordami alle 18 di chiamare il dentista", "sveglia alle 7", "alza il volume"

## Se qualcosa non va
- App Zepp → Voice Assistant → **Diagnostica**: mostra cosa è successo a ogni domanda.
- In Gateway Assistant il **Diario** mostra chiamate, messaggi e comandi.
- Il gateway deve essere avviato ("Gateway attivo ✓") e con la batteria senza restrizioni.

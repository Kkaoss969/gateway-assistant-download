# Live Assistant (Uhr) + Gateway Assistant (Telefon) — Kurzanleitung

Mit deiner Amazfit-Uhr (Zepp OS), einer Huawei Watch 3 / Watch 4, einer **Wear OS**-Uhr (Galaxy Watch, Pixel Watch, TicWatch…) oder einer Huawei-Uhr mit **HarmonyOS** (Watch 5, Watch 6, Watch Ultimate 2…) sprichst du mit Gemini und kannst über die App **Gateway Assistant** auf deinem Android-Telefon:
dein Google-Zuhause steuern, anrufen, WhatsApp-Nachrichten senden, lesen und beantworten und die Stimme des Telefons nutzen.
Jeder verwendet sein eigenes Telefon, sein Google-Konto und seinen Gemini-Schlüssel: nichts wird geteilt.

🌐 Die Apps sprechen **Deutsch, Englisch, Italienisch, Spanisch, Französisch, Portugiesisch (Portugal und Brasilien), Bulgarisch und Türkisch**: sie folgen automatisch der Sprache der Uhr und des Telefons. · *Italiano: [GUIDA.md](GUIDA.md)* · *English: [GUIDE.md](GUIDE.md)* · *Español: [GUIA.md](GUIA.md)* · *Français : [GUIDE-FR.md](GUIDE-FR.md)* · *Português: [GUIA-PT.md](GUIA-PT.md)* · *Português do Brasil: [GUIA-BR.md](GUIA-BR.md)* · *Български: [GUIDE-BG.md](GUIDE-BG.md)* · *Türkçe: [GUIDE-TR.md](GUIDE-TR.md)*

💬 **Telegram-Gruppe** der App (Fragen, Tipps, Neuigkeiten): https://t.me/Live_Assist

☕ **Unterstütze das Projekt** (kostenlose Apps): https://ko-fi.com/kkaoss969

## Was du brauchst
- Ein Android-Telefon mit der **Zepp**-App und der bereits gekoppelten Uhr
- Einen **Gemini-API-Schlüssel** (kostenlos oder mit Guthaben für schnellere Antworten): https://aistudio.google.com/apikey
- Die **Google**-App (Assistant) auf dem Telefon, verbunden mit deinem Google Home (nur für Befehle für das Zuhause)

<a id="api-keys"></a>
## API-Schlüssel
Die Schlüssel werden **nur einmal** in Gateway Assistant → **🔑 API-Schlüssel** eingegeben und gelten für alle Uhren; auf der Seite jeder Uhr gibst du sie mit *Schlüssel an die Uhr senden* an Live weiter (oder bei der Installation).
- **Gemini** (nötig, kostenlos): öffne https://aistudio.google.com/apikey mit deinem Google-Konto → **Create API key** → wähle oder erstelle ein Projekt → kopiere den Schlüssel (beginnt mit `AIza` oder `AQ.`) und füge ihn in Gateway ein → *Gemini-Schlüssel speichern*. Der kostenlose Tarif hat Tageslimits; mit etwas Guthaben sind die Antworten schneller.
- **Groq** (optional, kostenlos): öffne https://console.groq.com/keys, melde dich an (Google geht) → **Create API Key** → gib ihm einen Namen → kopiere den Schlüssel (beginnt mit `gsk_`, wird nur einmal angezeigt) und füge ihn in Gateway ein → *Groq-Schlüssel speichern*. Er liefert geschriebene Antworten in etwa 1 Sekunde.
- Um einen Schlüssel zu entfernen, halte seine *Speichern*-Taste gedrückt.

## 1 · Gateway Assistant installieren (Telefon)
1. Lade die APK auf das Telefon herunter: **https://github.com/Kkaoss969/gateway-assistant-download/raw/main/GatewayAssistant.apk**
2. Öffne sie und erlaube die Installation aus dieser Quelle, wenn Android fragt.
3. Öffne **Gateway Assistant** und tippe auf **Gateway starten**.
4. Tippe in der Liste **Berechtigungen** auf jede Zeile mit ⚪, bis alle ✅ sind:
   Kontakte und Anrufe · über anderen Apps anzeigen · WhatsApp senden (Bedienungshilfe) · WhatsApp lesen (Benachrichtigungen) · Akku ohne Einschränkungen.
   ⚠ **Bedienungshilfe**: schalte auf der Android-Seite „Gateway Assistant (WhatsApp senden)" **nur den ersten Schalter oben** ein („An"). Schalte den zweiten, „Verknüpfung für Gateway Assistant (WhatsApp senden)", **nicht** ein: das ist nur eine Android-Verknüpfung, und wenn sie an ist, funktionieren die automatischen Tipps (Senden in WhatsApp, Wecker Ausschalten/Schlummern, Senden an Gemini) nicht.
   Wenn eine Einstellung „eingeschränkt" ist: Einstellungen → Apps → Gateway Assistant → Menü ⋮ → *Eingeschränkte Einstellungen zulassen*.
5. Tippe auf **Code kopieren** (der Code des Kanals).

## 2 · Live Assistant auf der Uhr installieren
1. Schalte in der Zepp-App den Entwicklermodus ein: Profil → Einstellungen → Über → tippe mehrmals auf das Zepp-Logo.
2. Öffne **https://kkaoss969.github.io/gateway-assistant-download/**, wähle deine Uhr und scanne den **QR-Code** mit der Zepp-App (Profil → Scan-Symbol).
3. Öffne in der Zepp-App die Einstellungen der App **Live Assistant** und fülle aus:
   - **Gemini-API-Schlüssel**
   - **Meine Stadt** (Wetter und lokale Nachrichten)
   - **Gateway Assistant → Code**: füge den in Schritt 1 kopierten Code ein
   - **Groq-API-Schlüssel** (optional, kostenlos auf https://console.groq.com → *API Keys*): Nachrichten und geschriebene Fragen werden in etwa 1 Sekunde beantwortet; gesprochene Fragen bleiben bei Gemini
   - **Namen, die du oft verwendest** (optional): Personen, Orte, Mannschaften… sie helfen, die richtigen Namen zu verstehen
   - **Sprache der App**: normalerweise die der Uhr; **Bulgarisch** wird hier gewählt, weil Zepp OS es nicht hat

## 3 · Empfohlen
- **Anrufe auf der Uhr**: Zepp-App → Profil → Uhr → App-Einstellungen → Telefon → *Anrufe auf der Uhr annehmen* (und Bluetooth koppeln).
- **WhatsApp bei gesperrtem Telefon**: Einstellungen → Sicherheit → Smart Lock / Extend Unlock → *Vertrauenswürdige Geräte* → die Uhr hinzufügen.
- **Doppeltes WhatsApp (Klon)**: wenn das Telefon ein zweites, geklontes WhatsApp hat (Samsung Dual Messenger, „Doppelte Apps" auf anderen Telefonen), werden Textnachrichten gesendet, **Sprachnachrichten von der Uhr aber nicht** (WhatsApp öffnet den Chat ohne das Audio). Um Sprachnachrichten zu senden, entferne das geklonte WhatsApp; zwei Konten im selben WhatsApp sind in Ordnung. Gateway zeigt es mit ⚠️ auf der Taste für das Senden mit WhatsApp an.
- **Beeper (experimentell)**: wenn du [Beeper](https://play.google.com/store/apps/details?id=com.beeper.android) mit verbundenem WhatsApp und Telegram nutzt, tippe in Gateway auf *🧪 Beeper* und erlaube den Zugriff: Textnachrichten werden ohne WhatsApp zu öffnen und ohne Bedienungshilfe gesendet, auch bei gesperrtem Telefon, und bei Telegram kannst du in jeden Chat schreiben. Sprachnachrichten gehen weiterhin über WhatsApp.
  Ohne das wacht das Telefon auf und die Nachricht wird gesendet, wenn du es entsperrst.
- **Befehle für das Zuhause bei gesperrtem Telefon**: Google-App → Einstellungen → Google Assistant → Sperrbildschirm → persönliche Ergebnisse an.

**Wecker des Telefons**: wenn er klingelt, vibriert die Uhr und öffnet von selbst die Tasten **Ausschalten** und **Schlummern**. Die Uhr erfährt die Uhrzeit des nächsten Weckers jedes Mal, wenn du Live Assistant öffnest (und nach jedem Wecker): wenn du auf dem Telefon einen neuen Wecker stellst, öffne die App einmal auf der Uhr. ⚠ Im **Schlafmodus** oder bei **Nicht stören** blockiert die Uhr Apps von Drittanbietern: plane Schlafmodus / Nicht stören so, dass sie ein paar Minuten vor dem Wecker enden (Einstellungen der Uhr → Nicht stören → Geplant).

**Gemini Live (Test)**: schalte in der Zepp-App → Live Assistant → Einstellungen **Gemini Live verwenden** ein (braucht Gateway Assistant 1.65 oder neuer auf demselben Telefon). Die Antwort kommt direkt als Stimme, ohne auf die Sprachsynthese zu warten; wenn Live ausfällt, wird der normale Weg verwendet.

## Huawei-Uhr (Watch 3, Watch 4)
Für **Huawei Watch 3 und Watch 4** (die mit Android-Basis) gibt es **Live Assistant** mit **Gemini Live**: während du sprichst, geht die Frage schon an Gemini und die Antwort kommt direkt als Stimme zurück, meist in 1-3 Sekunden. Es funktioniert mit dem WLAN oder LTE der Uhr und auch nur über Bluetooth, über Gateway. Es wird von **Gateway Assistant** aus installiert, ohne Computer.
1. Auf der Uhr: Einstellungen → Über → tippe mehrmals auf die **Build-Nummer**. Schalte dann in den **Entwickleroptionen** **HDC-Debugging** und **Debugging über WLAN** ein.
2. Uhr und Telefon im **selben WLAN** (der Hotspot des Telefons geht auch).
3. Tippe in Gateway Assistant auf **⌚ Huawei-Uhr: Installation und Diagnose**, gib die unter *Debugging über WLAN* angezeigte IP ein und tippe auf **⬇ Live Assistant herunterladen und installieren**. Beim ersten Mal fragt die Uhr, ob die Verbindung erlaubt werden soll: tippe auf **Immer zulassen**.
   Gateway gibt der Uhr den Code des Kanals und, wenn das Kästchen angehakt ist, deinen Gemini-Schlüssel; außerdem nimmt es die App vom Energiesparen aus.
4. Tippe in Gateway Assistant auf **⚪ Huawei-Bluetooth erlauben**, bis **✅ Huawei-Bluetooth: an** erscheint: die Uhr funktioniert dann **ohne WLAN oder LTE**, über das Bluetooth des Telefons.
5. **Untere Taste**: tippe auf derselben Seite auf **Untere Taste: Live Assistant öffnen**. Das Drücken der unteren Taste der Uhr öffnet dann Live Assistant, das gleich zuhört, statt Celia (*Celia wiederherstellen* macht es rückgängig).

Auf der Uhr öffnet das **Zahnrad** unter *Neuer Chat* die Einstellungen (Stadt, Verbindung Auto/Bluetooth/Internet, Stimme, Updates, Diagnose); die **Krone** blättert durch die Seiten. Fragen, Stimme, Wetter und Nachrichten, Google-Zuhause, Kontakte und WhatsApp, Anrufe, Schnellbefehle, Erinnerungen, Taschenlampe, Lautstärke und Helligkeit, Schritte und Puls funktionieren alle. Per Sprache kannst du auch die **Bildschirm-DPI** ändern („stell die DPI auf 280", „DPI zurücksetzen"; 90 bis 400, Standard 320); in den Einstellungen der Uhr gibt es **DPI zurücksetzen**, und Gateway (Seite der Huawei-Uhr, Abschnitt *Bildschirm-DPI*) hat **Einstellen** und **Zurücksetzen (320)**.
**Wecker des Telefons**: wenn er klingelt, vibriert die Uhr und zeigt **Stopp** und **Schlummern** (auch im Nachtmodus, der eine Minute vorher ausgeschaltet wird; Schlummern schaltet ihn wieder ein). Es funktioniert auch mit kurzfristig gestellten Weckern: schalte in der App Health → Geräte → Uhr → Benachrichtigungen **Gateway Assistant** ein.
**Updates**: Gateway Assistant zeigt die installierte und die neue Version; aktualisiere von derselben Seite aus oder von der Uhr (Einstellungen → *Prüfen und installieren*, mit eingeschaltetem Debugging über WLAN).
**Groq (optional)**: Live beantwortet allgemeine Fragen selbst; Befehle (Zuhause, Anrufe, WhatsApp, Wecker, Wetter, Nachrichten) führt die App aus, und mit einem Groq-Schlüssel ist der Textteil in etwa 1 Sekunde fertig. Kostenloser Schlüssel: https://console.groq.com → *API Keys* → *Create API Key* (beginnt mit `gsk_`) und in Gateway einfügen → *🔑 API-Schlüssel* → *Groq-Schlüssel speichern*.
**Diagnose**: sie kommt von selbst bei Gateway an (Seite der Huawei-Uhr; von der Uhr aus auch Einstellungen → *An Gateway Assistant senden*). Mit **Teilen** schickst du sie als Textdatei (WhatsApp, Telegram, E-Mail) an die Person, die dir hilft.
**Zweimal schütteln zum Öffnen (Test)**: schalte in den Einstellungen der Uhr *Test: zweimal kräftig schütteln öffnet die App* ein. Bei eingeschaltetem Bildschirm öffnen zwei kurze, kräftige Schüttler kurz hintereinander Live Assistant zum Zuhören; beim Always-On-Bildschirm ist der Sensor aus, um Akku zu sparen: hebe das Handgelenk, um den Bildschirm wieder einzuschalten. Die untere Taste geht auch.
**Energiesparen von Huawei**: die Uhr kann Live Assistant im Hintergrund schließen (untere Taste und Schütteln funktionieren nicht mehr, bis du die App wieder öffnest). Tippe in Gateway, Seite der Huawei-Uhr, auf **PowerGenie: entfernen** (wenn die Uhr es nicht erlaubt, wird es deaktiviert; **PowerGenie: wiederherstellen** macht es rückgängig). Wenn das Debugging über WLAN an bleibt und du im selben Netz bist, aktiviert Gateway Live Assistant von selbst wieder, wenn die Uhr es schließt.

### Eigene Apps auf der Uhr installieren
Auf derselben Seite von Gateway, Abschnitt **Eigene Apps auf der Uhr installieren**: tippe auf **📲 App zum Installieren wählen** und wähle die heruntergeladene Datei. Einzelne **APK**s und aufgeteilte Pakete **APKS**, **XAPK** (OBB-Dateien inklusive) und **APKM** funktionieren alle. Debugging über WLAN wird gebraucht, wie für Live Assistant. Im Feld darunter kannst du einen **adb-Befehl** eingeben (z. B. `pm list packages -3` für die Liste der installierten Apps) (Abschnitt **Auf der Uhr ausführen**) und auf **Ausführen** tippen: das Ergebnis erscheint darunter und **Ergebnis kopieren** kopiert es.

## Wear OS-Uhr (Beta)
Live Assistant läuft auch auf **Wear OS-Uhren ab Android 9**, rund und eckig (Galaxy Watch, Pixel Watch, Oppo Watch, Mi Watch, TicWatch, Fossil…), auch auf alten Uhren mit **Wear OS 2 und 3**, auf denen Google Assistant und WhatsApp nicht mehr funktionieren. Es ist dieselbe App wie auf Huawei: gesprochene Fragen mit Gemini Live, grafisches Wetter, Zuhause, Kontakte, WhatsApp und Telegram über Gateway.
**Verbindung mit dem Telefon**: zuerst der offizielle Wear OS-Kanal (Bluetooth, WLAN oder Netz, von Wear OS gewählt), dann direktes Bluetooth. Gateway gibt der Uhr die Schlüssel und den Code des Kanals: so funktioniert es auch weit vom Telefon entfernt, wenn die Uhr Netz hat.

**Installation** — tippe in Gateway Assistant auf **⌚ Wear OS-Uhr: Installation und Diagnose**. Schalte zuerst auf der Uhr die **Entwickleroptionen** ein: Einstellungen → Über (auf der Galaxy *Info zur Uhr → Softwareinformationen*) → tippe mehrmals auf **Softwareversion** oder **Build-Nummer**. Uhr und Telefon im **selben WLAN** (der Hotspot des Telefons geht auch). Wähle dann die Verbindung:
- **WLAN-Debugging (Wear OS 4 und neuer)**: Entwickleroptionen → **WLAN-Debugging** an (*In diesem Netzwerk immer zulassen*).
  1. Öffne auf der Uhr **Neues Gerät koppeln** (ein 6-stelliger Code erscheint).
  2. Gib in Gateway **nur den Code** ein und tippe auf **🔗 Koppeln**: IP, Verbindungsport und Kopplungsport werden automatisch im Netz gefunden (Taste **🔍 Die Uhr finden**; sie können auch in ihre Felder eingegeben werden). Nach dem Koppeln wird die Taste grün, **Gekoppelt ✓**: es muss nicht wiederholt werden.
  3. Tippe auf **⬇ Live Assistant herunterladen und installieren**. Der Verbindungsport ändert sich jedes Mal, wenn du das WLAN-Debugging wieder einschaltest: wenn ein Befehl keine Verbindung bekommt, leere das Port-Feld und Gateway findet ihn wieder.
- **Debugging über WLAN (Wear OS 2 und 3)**: Entwickleroptionen → **ADB-Debugging** und **Debugging über WLAN** an. Gib die IP der Uhr ein (der Port ist schon **5555**) und tippe auf **⬇ Live Assistant herunterladen und installieren**; akzeptiere auf der Uhr das Debugging (**Immer zulassen**).

Gateway installiert die App, erteilt die Berechtigungen (Mikrofon, Sensoren, Updates), nimmt sie vom Energiesparen aus, gibt ihr die Schlüssel und öffnet sie. Jede Taste zeigt die Schritte in einem Fenster (**Kopieren**, um sie an die Person zu schicken, die dir hilft).
Wenn auf der **Pixel Watch** das Symbol nach der Installation nicht in der App-Liste erscheint, starte die Uhr neu.
**Taste zum Öffnen von Live** — in den Einstellungen von Live auf der Uhr (Zahnrad): *Langes Drücken auf Home: Live statt des Google-Assistenten*; auf der **Galaxy Watch Ultra** die **mittlere (orange) Taste**: wähle in den Tasteneinstellungen von Samsung **Keine App**, tippe dann in Live auf **App der Taste lernen** und drücke die Taste einmal. Wenn der Tastenwächter nicht aktiv ist, tippe in Gateway auf **🔑 Live die Berechtigungen geben**.
**Benachrichtigungen des Telefons (nur Huawei)**: Gateway → Seite der Huawei-Uhr → **🔔 Benachrichtigungen des Telefons auf der Uhr**: wähle die Apps (tippen zum Wechseln: aus → *in der Nähe*, über Bluetooth → *auch weit weg*, auch über Internet, höchstens 40 am Tag). Auf der Uhr verworfen oder angetippt, verschwindet die Benachrichtigung auch vom Telefon. Auf Wear OS und Amazfit kommen die Benachrichtigungen schon über ihre eigenen Apps.
**Telegram auf der Uhr** (Wear OS und Huawei): wenn das Telefon nicht über Bluetooth verbunden ist, liest und sendest du Telegram (Texte, Sprachnachrichten, Fotos) über LTE oder WLAN direkt von der Uhr. Verbinde es einmal, in der Nähe des Telefons und mit eingeschaltetem *Telegram direkt* in Gateway: Einstellungen von Live auf der Uhr → **Telegram verbinden (vom Telefon)**. Gateway nimmt die Anmeldung von selbst an; mit zweistufiger Bestätigung fragt die Uhr nach dem Passwort. Die Uhr erscheint in Telegram → Geräte als *Live Assistant (orologio)*. Die Verbindung öffnet sich nur bei Bedarf und schließt sich nach 2 Minuten.
**Updates**: auf der Uhr Zahnrad → *Prüfen und installieren*. Auf Wear OS 4 und neuer aktualisiert sich die App selbst (beim ersten Mal *Unbekannte Apps installieren* erlauben, dann bestätigen); auf Wear OS 2 und 3 läuft es über das Debugging über WLAN, das eingeschaltet bleiben muss.
**Auf derselben Seite**: *Schlüssel an die Uhr senden*; **Bildschirm-DPI** (*Zurücksetzen* geht zur Werks-DPI des Modells zurück, z. B. 340 bei Samsung); **Eigene Apps installieren** (APK, APKS, XAPK, APKM); **Auf der Uhr ausführen** (adb-Befehle); **Diagnose** der Uhr (mit Modell und Android-Version).
**Taste**: auf der Galaxy Watch Einstellungen → Erweiterte Funktionen → Tasten anpassen → *Zweimal drücken* → **Live Assistant**. Für die mittlere Taste der Galaxy Watch Ultra bereiten wir den Tastenwächter vor: tippe in Gateway auf **🔎 Tasten untersuchen**, drücke 15 Sekunden lang die Tasten der Uhr und sende das Ergebnis.

## HarmonyOS-Uhr (Watch 5, Watch 6, Watch Ultimate 2…) (Beta)
Für Huawei-Uhren mit **HarmonyOS NEXT** (z. B. Watch 5, Watch 6, Watch Ultimate 2), die keine APKs installieren können, gibt es **Live Assistant für HarmonyOS**. Es hat dieselben Funktionen wie die anderen Versionen: gesprochene Fragen mit Gemini Live, Wetter, Zuhause, Kontakte, WhatsApp und Telegram, Wecker des Telefons, Verlauf. Du installierst es von **Gateway Assistant** aus, ohne Computer.
**Warum du ein Huawei-Entwicklerkonto brauchst**: HarmonyOS installiert nur Apps, die mit einem Profil signiert sind, das die Kennung deiner Uhr (UDID) enthält. Gateway erstellt Schlüssel, Zertifikat und Profil mit **deinem** Konto, so wie DevEco Studio es tut. Sie bleiben nur auf deinem Telefon und werden nicht geteilt.

**1 · Huawei-Entwicklerkonto (einmal)**
1. Öffne https://developer.huawei.com, melde dich mit deiner **Huawei-ID** an (die der App Health geht) und schließe die **Registrierung als Entwickler** ab (kostenlos, Einzelkonto). Für die Identitätsprüfung brauchst du einen gültigen Ausweis (Personalausweis oder Reisepass) und eine Kreditkarte: warte, bis sie als genehmigt angezeigt wird.
2. Tippe in Gateway Assistant auf **⌚ HarmonyOS-Uhr: Verbindung und Diagnose** → **🔏 Signaturdateien für HAPs** → **🔐 Automatische Profile: mit dem Huawei-Konto anmelden (wie DevEco)**.
3. Der Browser öffnet sich: melde dich mit dem Entwicklerkonto an und bestätige. Der Browser kehrt von selbst zu Gateway zurück, das **✅ Angemeldet** zeigt; die Taste wird zu **🔐 Huawei-Konto:** mit deinem Namen (tippen zum Abmelden).
Mehr ist nicht nötig: Debug-Schlüssel und -Zertifikat werden bei der ersten Installation automatisch erstellt (oder sofort mit **🪄 Schlüssel und Zertifikat mit dem Huawei-Konto erstellen**). Jedes Konto kann höchstens 3 Debug-Zertifikate haben (Gateway ersetzt seine eigenen selbst): wenn du schon 3 mit DevEco Studio erstellt hast und Gateway es meldet, lösche ein altes in AppGallery Connect (*Certificates, app IDs, and profiles → Certificates*).

**2 · Die Uhr vorbereiten**
1. Auf der Uhr: Einstellungen → Über → tippe mehrmals auf die **Version**, bis die **Entwickleroptionen** erscheinen.
2. Schalte in den Entwickleroptionen **Debugging (HDC)** und **WLAN-Debugging** ein: die Uhr zeigt **IP und Port** (z. B. 192.168.0.191:44911). Der Port ändert sich jedes Mal, wenn du das Debugging wieder einschaltest.
3. Uhr und Telefon im **selben WLAN** (der Hotspot des Telefons geht auch).

**3 · Live Assistant installieren**
1. In Gateway: **⌚ HarmonyOS-Uhr** → **📲 Live auf der Uhr installieren oder aktualisieren**.
2. Gib **IP** und **Port** der Uhr ein oder tippe auf **🔎 Die Uhr im WLAN suchen** (mit bereits eingegebener IP findet es den Port in ein paar Sekunden).
3. Tippe auf **⬇ Von der Website**. Gateway lädt Live Assistant herunter, registriert die Uhr in deinem Konto, erstellt das Profil, signiert die App, installiert sie und öffnet sie bereits mit Gateway verbunden (Code des Kanals und Schlüssel). Das Fenster zeigt jeden Schritt bis **✅ Fertig**.
4. Beim ersten Mal fragt die Uhr, ob die **Debugging-Verbindung erlaubt** werden soll: akzeptiere.
Wenn auf der Uhr schon ein von jemand anderem signiertes Live Assistant ist, fragt Gateway, ob es zuerst deinstalliert werden soll (die Daten der App auf der Uhr gehen verloren).

**Updates**: Gateway Assistant zeigt an, wenn eine neue Version verfügbar ist. Du aktualisierst auf dieselbe Weise (📲 Installieren oder aktualisieren → ⬇ Von der Website), mit eingeschaltetem WLAN-Debugging; Einstellungen und Daten bleiben erhalten.
**Verbindung mit dem Telefon**: Live versucht von selbst direktes WLAN (selbes Netz), Bluetooth und zuletzt das Internet (WLAN oder LTE der Uhr) mit dem Code des Kanals. Um Bluetooth zu nutzen: auf der Uhr ⚙ → **🔵 Bluetooth mit Gateway testen** (die Bluetooth-Berechtigung erlauben).
**Live im Hintergrund (Beta)**: unter ⚙ → **🌙 Live im Hintergrund** bekommt die Uhr Nachrichtenhinweise über Bluetooth auch bei geschlossener App und prüft alle 30 Minuten Wecker und Nachrichten. Es braucht etwas mehr Akku und vorher einen erfolgreichen Bluetooth-Test.
**Diagnose**: auf der Uhr ⚙ → Diagnose → 📤 Gateway; in Gateway findest du sie unter ⌚ HarmonyOS-Uhr → **Diagnose**.
**Hast du schon eigene Signaturdateien?** (für Nutzer von DevEco Studio): unter **🔏 Signaturdateien für HAPs** lädst du den Schlüssel **.p12** mit seinem Passwort, das Debug-Zertifikat **.cer** und die Profile **.p7b** (eines pro App, mit der UDID der Uhr, die du über **🛠 hdc-Werkzeuge** → **📋 Kennung der Uhr (UDID)** kopierst). Die Taste **🤖 Automatische Profile (AppGallery Connect)** nutzt die offiziellen APIs, die mit europäischen Konten nicht funktionieren: verwende in diesem Fall die Anmeldung mit dem Huawei-Konto.
**Andere Werkzeuge** (🛠 hdc-Werkzeuge): **🔑 Gemini-Schlüssel und Kanal an Live senden**, Befehle auf der Uhr. Mit **HAP wählen** kannst du auch andere HarmonyOS-Apps installieren: wenn das Huawei-Konto verbunden ist, signiert Gateway sie selbst.

## Mit einem iPhone
Gateway Assistant gibt es nur für Android: iOS erlaubt einer App nicht, immer aktiv zu bleiben, in WhatsApp auf „Senden" zu tippen, Benachrichtigungen zu lesen oder Sätze an den Google Assistant weiterzugeben.
**Live Assistant funktioniert trotzdem mit einem iPhone**: Fragen an Gemini, Stimme, Wetter, Nachrichten, Erinnerungen, Lautstärke, Helligkeit und Taschenlampe.
Nicht verfügbar: Befehle für das Google-Zuhause, Anrufe mit dem Namen aus deinen Kontakten, WhatsApp senden und lesen, Ersatzstimme des Telefons.
- Überspringe Schritt 1 und lass **Gateway Assistant → Code** leer.
- Lass die **Zepp-App im Hintergrund offen** (nicht wegwischen): wenn iOS sie anhält, sagt die Uhr „Telefon nicht erreichbar".
- Normale Anrufe auf der Uhr funktionieren mit den Bluetooth-Anrufen der Zepp-App.

## Gesten mit dem Handgelenk (Schütteln)
Praktisch bei Lärm oder vollen Händen. Sie werden in den Einstellungen der App auf der Uhr (Huawei) ein- und ausgeschaltet und funktionieren bei offener App:
- **Einmal schütteln beim Zuhören**: sendet die Frage sofort, ohne auf die Stille zu warten.
- **Einmal schütteln beim Nachdenken** (drehende Farben): bricht die Frage ab.
- **Einmal schütteln beim Sprechen**: stoppt die Stimme.
- **Einmal schütteln im Ruhezustand**: neue Frage (hört wieder zu).
- **Zweimal schütteln**: schließt die App. Gib den zweiten nach einer kurzen Pause und **kräftiger** als den ersten, damit ein normaler zweiter Versuch sie nicht aus Versehen schließt.
- **Stopp-Taste (Huawei und Amazfit)**: vom Beginn des Zuhörens bis die Antwort kommt, ersetzt eine rote Taste **■ Stopp** den *Neuen Chat*: sie bricht die Frage ab, ohne sie zu senden (oder verwirft die ankommende Antwort), und die Befehle dieser Frage werden nicht ausgeführt. Ein Tipp auf die mittlere Taste beim Zuhören sendet sofort. Wenn eine WhatsApp-/Telegram-Nachricht oder eine Sprachnachricht gesendet wird, erscheint ein großes **grünes ✓** mit Vibration und kurzem Ton (kein Ton im Privatsphäre-Modus); wenn es fehlschlägt, ein **rotes ✗**.
Schütteln zählt in den ersten 2 Sekunden nach dem Öffnen nicht. Nach **30 Sekunden** ohne Aktivität kehrt die App von selbst zum Zifferblatt zurück.

## Was du sagen kannst
- „Wie wird das Wetter morgen?", „Wie hat Bayern gespielt?", jede Frage (bei Wetterfragen zeigt die Uhr auch eine **grafische Karte**: jetzt, nächste Stunden und nächste Tage)
- „Schalte das Licht in der Küche ein", „gute Nacht"
- „Ruf Mario an" (wenn es mehrere Marios gibt, tippst du einen auf der Uhr an)
- „Schick Mario eine WhatsApp: ich bin in zehn Minuten da" (tippe zum Bestätigen auf **Senden an …**)
- „Lies meine WhatsApp-Nachrichten", „antworte Anna: passt"
- „Antworte Luca auf Telegram: bin unterwegs" (nur an Telegram-Chats mit einer aktuellen Benachrichtigung; „lies meine Nachrichten" zeigt auch die von Telegram)
- „Schick Mario eine Sprachnachricht": tippe auf den Kontakt 🎤, sprich und tippe erneut zum Senden. Sie kommt als WhatsApp-Sprachnachricht an; bei Huawei wird Bluetooth zum Telefon gebraucht (oder auf der Seite Kontakte bei einem Favoriten **WhatsApp gedrückt halten**: die Aufnahme beginnt sofort)
- „Schalte den Wecker für morgen aus", „stopp den Wecker", „Wecker schlummern" (Wecker des **Telefons**)
- „Trag den Zahnarzt am Donnerstag um 10 in meinen Kalender ein, erinnere mich eine Stunde vorher", „was habe ich morgen?" (Kalender des **Telefons**: tippe in Gateway Assistant auf **Kalender erlauben**)
- „Setz Milch auf meine Einkaufsliste", „notiere: Glühbirnen kaufen", „erinnere mich morgen um 9 in Google Tasks, Luca anzurufen" (**Keep** und **Tasks**: Gateway schreibt den Satz an Gemini auf dem Telefon; braucht die Bedienungshilfe von Gateway Assistant und die eingeschalteten Erweiterungen Keep und Tasks in Gemini)
- „Schalte Nicht stören bis 7 Uhr ein", „schalte Nicht stören aus" (Nicht stören des **Telefons**: tippe in Gateway Assistant auf **Nicht stören erlauben**; es gelten die auf dem Telefon eingestellten Ausnahmen)
- „Erinnere mich um 18 Uhr, den Zahnarzt anzurufen", „Wecker um 7", „mach lauter"

**Schnellbefehle und Favoriten**: füge in Gateway Assistant im Abschnitt „Auf der Uhr: Schnellbefehle und Favoriten" Tasten mit einem Satz für den Assistant (z. B. „Shield" → „schalte Shield ein") und Lieblingskontakte aus deinem Adressbuch hinzu. Auf der Uhr neben der mittleren Taste: das Symbol **Haus** (oder der Pfeil **‹**) öffnet **Zuhause**, mit deinen Tasten (sie gehen direkt an den Assistant des Telefons, ohne Gemini) und **Nicht stören** zum Ein- und Ausschalten; das Symbol **Nachrichten** (oder der Pfeil **›**) öffnet **Kontakte**, mit deinen Favoriten und den Tasten **WhatsApp** (sag die Nachricht und bestätige mit Senden) und **Anrufen**.

**Favoriten und Gruppen**: bis zu **16 Favoriten** aus Kontakten und Gruppen. Mit **+ WhatsApp-Gruppe hinzufügen** und **+ Telegram-Gruppe hinzufügen** wählst du eine Gruppe: auf der Uhr bekommt sie eine eigene Karte mit der letzten Nachricht (und wer sie geschrieben hat), den Sprechblasen und den Antworten. **Hinweise**: wenn dir ein Favorit schreibt (oder in einer Lieblingsgruppe), zeigt die Uhr Namen und Vorschau, und ein Tipp öffnet den Chat in dieser App. Mit WhatsApp und Telegram direkt kommen die Hinweise auch an, wenn das Telefon keine Benachrichtigung zeigt.

**Privatsphäre-Modus**: tippe auf die Taste **Mikrofon** unten rechts neben der mittleren Taste: sie wird zu einer grünen **Tastatur**: das Mikrofon bleibt aus und die mittlere Taste öffnet die Tastatur; schreib deine Frage und die Antwort kommt nur als Text, ohne Stimme. Tippe erneut darauf, um zur Stimme zurückzukehren. Für eine einzelne geschriebene Frage kannst du die mittlere Taste auch **gedrückt halten**. Braucht eine Uhr mit Zepp OS 4 oder neuer.

## Bilder, Ergebnisse, Formeln und Graphen (Huawei, Wear OS, HarmonyOS)
- **Geprüfter Sport und Nachrichten**: Vor der Antwort sucht die Uhr bei Google nach aktuellen Seiten („🔎 Ich suche bei Google…“ auf dem Display, ein paar Sekunden). Nach der Antwort vergleicht eine schnelle Prüfung sie mit dem Gefundenen: Bei einem Fehler zeigt und sagt die Uhr die **Korrektur**.
- **Ergebniskarte**: Bei Spielen erscheinen Mannschaften, Ergebnis, Wettbewerb und **Torschützen** mit Minute (wenn die Quellen sie nennen).
- **Bilder am Ende der Antwort**: „Wie sieht das Kolosseum aus?“ zeigt das Foto aus Wikipedia; bei Nachrichten und Sport erscheint das Foto des Artikels mit **Quelle** (z. B. 📰 kicker.de). Während es lädt, steht dort „Bild kommt“.
- **Formeln**: „Wie lautet die Formel für die Kreisfläche?“ zeigt die Formel sauber geschrieben.
- **Funktionsgraphen**: „Zeichne den Graphen von Sinus x“, „zeichne die Parabel x hoch 2 minus 4“, „vergleiche x, x hoch 2 und x hoch 3“ (bis zu 3 Kurven).
- **Zoom**: Tippe auf Bild, Karte oder Graph, um sie zu vergrößern; mit der **Krone** zoomst du hinein und heraus.
- Die Bilder kommen nach der Stimme, damit die Stimme nicht unterbrochen wird.
- **Huawei Watch 3/4**: Unter den Apps der Uhr gibt es auch ein **Kalender**-Symbol, das die Termine des Telefons direkt öffnet.

## Wenn etwas nicht funktioniert
- Zepp-App → Live Assistant → **Diagnose**: zeigt, was bei jeder Frage passiert ist. Sie kommt auch in Gateway Assistant an (**⌚ Amazfit-Uhr: Diagnose**): von dort kopierst du sie oder sendest sie mit **Datei teilen** als Datei.
- In Gateway Assistant zeigt das **Protokoll** Anrufe, Nachrichten und Befehle.
- Das Gateway muss laufen („Gateway läuft ✓"), mit Akku ohne Einschränkungen.
- **🐞 Ein Problem melden** in Gateway oder per Sprache von der Uhr („melde ein Problem: die WhatsApp-Taste funktioniert nicht"): die Meldung geht mit dem Protokoll und der Diagnose der Uhren an den Entwickler, mit ausgeblendeten Nachrichtentexten und Nummern. Beim ersten Mal wird um Zustimmung gebeten. Gateway meldet wiederholte Probleme auch selbst (höchstens einmal am Tag pro Art).
- Die Gateway-Taste ist **grün**, wenn es läuft, und **rot**, wenn es gestoppt ist.
- **Anonyme Nutzungszählung**: einmal am Tag sendet Gateway nur eine zufällige ID und die Versionen der Apps, keine persönlichen Daten. Ausschalten mit **📊 Anonyme Nutzungszählung**.
- **Hilfe von anderen Nutzern**: in der Telegram-Gruppe https://t.me/Live_Assist

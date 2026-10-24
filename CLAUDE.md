# Sito di Gateway Assistant (pubblico)

https://kkaoss969.github.io/gateway-assistant-download/ è il repository **pubblico** da cui gli utenti scaricano le app. Contiene:
- `GatewayAssistant.apk`, `LiveAssistantHuawei.apk`, `LiveAssistantWear.apk`;
- `LiveAssistantHarmony.hap` (**solo la versione NON firmata**);
- `qr/` (codici QR Amazfit, li aggiorna la CI di `gemini-watch`);
- le guide in più lingue (`GUIDA.md`, `GUIDE.md`, `GUIA.md`…) e `index.html`.

## versioni.json
Le app lo leggono per proporre gli aggiornamenti. Chiavi:
- `gateway` (versione, codice);
- `orologio` (Amazfit, aggiornato dalla CI);
- `orologioLive` (Huawei);
- `orologioWear`;
- `orologioHarmony`.

Va aggiornato insieme al file pubblicato, e con lui la riga "— versione X" del README: riga 10 per Gateway, riga 25 per Huawei, riga di HarmonyOS.

## Prima di lavorare
`git stash; git pull --rebase; git stash pop`: la CI di Amazfit pusha qui da sola.

## Attenzione
Qui non va **mai** niente di privato: niente chiavi, profili o HAP firmate (contengono l'UDID dell'orologio di Antonio), codici del canale, token.

## Regole
Questo repository è pubblico: le regole complete del progetto (collaborazione, segreti, pubblicazione) sono nel
`CLAUDE.md` del repository privato `gateway-assistant`. Si lavora e si risponde in italiano; si pubblica solo da `main`
dopo l'approvazione di Antonio.

# Live Assistant (watch) + Gateway Assistant (phone) — quick guide

With your Amazfit watch (Zepp OS), Huawei Watch 3 / Watch 4 or **Wear OS** watch (Galaxy Watch, Pixel Watch, TicWatch…) you talk to Gemini and, through the **Gateway Assistant** app on your Android phone, you can:
control your Google home, make calls, send/read/reply to WhatsApp messages and use the phone's voice.
Everyone uses their own phone, Google account and Gemini key: nothing to share.

🌐 The apps speak **English, Italian, Spanish, French, Portuguese (Portugal and Brazil) and Bulgarian**: they follow the language of the watch and the phone automatically. · *Italiano: [GUIDA.md](GUIDA.md)* · *Español: [GUIA.md](GUIA.md)* · *Français : [GUIDE-FR.md](GUIDE-FR.md)* · *Português: [GUIA-PT.md](GUIA-PT.md)* · *Português do Brasil: [GUIA-BR.md](GUIA-BR.md)* · *Български: [GUIDE-BG.md](GUIDE-BG.md)*

## What you need
- An Android phone with the **Zepp** app and the watch already paired
- A **Gemini API key** (free, or with credit for faster answers): https://aistudio.google.com/apikey
- The **Google** app (Assistant) on the phone, linked to your Google Home (only for home commands)

## API keys
Keys are entered **only once** in Gateway Assistant → **🔑 API keys** and work for all watches; from each watch's page you give them to Live with *Send the keys to the watch* (or when installing).
- **Gemini** (required, free): open https://aistudio.google.com/apikey with your Google account → **Create API key** → choose or create a project → copy the key (starts with `AIza` or `AQ.`) and paste it in Gateway → *Save Gemini key*. The free plan has daily limits; with some credit answers are faster.
- **Groq** (optional, free): open https://console.groq.com/keys, sign in (Google works) → **Create API Key** → give it a name → copy the key (starts with `gsk_`, shown only once) and paste it in Gateway → *Save Groq key*. It gives written answers in about 1 second.
- To remove a key, long-press its *Save* button.

## 1 · Install Gateway Assistant (phone)
1. Download the APK on the phone: **https://github.com/Kkaoss969/gateway-assistant-download/raw/main/GatewayAssistant.apk**
2. Open it and allow installs from this source if Android asks.
3. Open **Gateway Assistant** and tap **Start the gateway**.
4. In the **Permissions** list tap each row with ⚪ until they are all ✅:
   contacts and calls · display over other apps · WhatsApp sending (accessibility) · WhatsApp reading (notifications) · battery unrestricted.
   ⚠ **Accessibility**: on Android's "Gateway Assistant (WhatsApp sending)" page turn on **only the first switch at the top** ("On"). **Do not turn on** the second one, "Gateway Assistant (WhatsApp sending) shortcut": it's just an Android shortcut and, if on, the automatic taps (WhatsApp Send, alarm Turn off/Snooze, sending to Gemini) don't work.
   If a setting is "restricted": Settings → Apps → Gateway Assistant → ⋮ menu → *Allow restricted settings*.
5. Tap **Copy code** (the channel code).

## 2 · Install Live Assistant on the watch
1. In the Zepp app turn on developer mode: Profile → Settings → About → tap the Zepp logo several times.
2. Open **https://kkaoss969.github.io/gateway-assistant-download/**, choose your watch and scan the **QR code** with the Zepp app (Profile → scan icon).
3. In the Zepp app open the settings of the **Live Assistant** app and fill in:
   - **Gemini API key**
   - **My city** (weather and local news)
   - **Gateway Assistant → Code**: paste the code copied in step 1
   - **Groq API key** (optional, free from https://console.groq.com → *API Keys*): news and typed questions are answered in about 1 second; spoken questions stay with Gemini
   - **Names you often use** (optional): people, towns, teams… they help it understand the right names
   - **App language**: usually the watch's; **Bulgarian** is chosen here, because Zepp OS doesn't have it

## 3 · Recommended
- **Calls on the watch**: Zepp app → Profile → watch → App settings → Phone → *Answer calls on the watch* (and pair Bluetooth).
- **WhatsApp with a locked phone**: Settings → Security → Smart Lock / Extend Unlock → *Trusted devices* → add the watch.
- **Dual WhatsApp (clone)**: if the phone has a second, cloned WhatsApp (Samsung Dual Messenger, "Dual apps" on other phones), text messages are sent but **voice messages from the watch are not** (WhatsApp opens the chat without the audio). To send voice messages remove the cloned WhatsApp; two accounts in the same WhatsApp are fine. Gateway flags it with ⚠️ on the WhatsApp sending button.
- **Beeper (experimental)**: if you use [Beeper](https://play.google.com/store/apps/details?id=com.beeper.android) with WhatsApp and Telegram linked, tap *🧪 Beeper* in Gateway and allow access: text messages are sent without opening WhatsApp and without accessibility, even with the phone locked, and on Telegram you can write to any chat. Voice messages still go through WhatsApp.
  Without it, the phone wakes up and the message is sent when you unlock it.
- **Home commands with a locked phone**: Google app → Settings → Google Assistant → Lock screen → personal results on.

**Phone alarm**: when it rings, the watch vibrates and opens the **Turn off** and **Snooze** buttons by itself. The watch learns the time of the next alarm whenever you open Live Assistant (and after each alarm): if you create a new alarm on the phone, open the app on the watch once. ⚠ In **sleep mode** or **do not disturb** the watch blocks third-party apps: schedule sleep mode / do not disturb to end a few minutes before the alarm (watch Settings → Do not disturb → Scheduled).

**Gemini Live (trial)**: in the Zepp app → Live Assistant → Settings turn on **Use Gemini Live** (needs Gateway Assistant 1.65 or later on the same phone). The answer arrives already as voice, without waiting for speech synthesis; if Live fails the normal method is used.

## Huawei watch (Watch 3, Watch 4)
For **Huawei Watch 3 and Watch 4** (the Android-based ones) there is **Live Assistant**, with **Gemini Live**: while you speak the question is already going to Gemini and the answer comes straight back as voice, usually in 1-3 seconds. It works with the watch's Wi-Fi or LTE and also over Bluetooth only, through Gateway. It installs from **Gateway Assistant**, no computer needed.
1. On the watch: Settings → About → tap the **build number** several times. Then in **Developer options** turn on **HDC debugging** and **Debugging over Wi-Fi**.
2. Watch and phone on the **same Wi-Fi** (the phone's hotspot is fine).
3. In Gateway Assistant tap **⌚ Huawei watch: install and diagnostics**, enter the IP shown under *Debugging over Wi-Fi* and tap **Download and install Live Assistant**. The first time the watch asks to allow the connection: tap **Always allow**.
   Gateway gives the watch the channel code and, if the box is ticked, your Gemini key; it also excludes the app from battery saving.
4. In Gateway Assistant tap **⚪ Allow Huawei Bluetooth** until it shows **✅ Huawei Bluetooth: on**: the watch then works **without Wi-Fi or LTE**, through the phone's Bluetooth.
5. **Lower button**: on the same page tap **Lower button: open Live Assistant**. Pressing the watch's lower button then opens Live Assistant, already listening, instead of Celia (*Restore Celia* undoes it).

On the watch the **gear** under *New chat* opens the settings (city, Auto/Bluetooth/Internet connection, voice, updates, diagnostics); the **crown** scrolls the pages. Questions, voice, weather and news, Google home, Contacts and WhatsApp, calls, quick commands, reminders, torch, volume and brightness, steps and heart rate all work. By voice you can also change the **screen DPI** ("set the dpi to 280", "reset the dpi"; 90 to 400, standard 320); the watch settings have **Reset DPI**, and Gateway (Huawei watch page, *Screen DPI* section) has **Set** and **Reset (320)**.
**Phone alarm**: when it rings, the watch vibrates and shows **Stop** and **Snooze** (even in night mode, which is turned off one minute before; Snooze turns it back on). It also works with last-minute alarms: in the Health app → Devices → watch → Notifications turn on **Gateway Assistant**.
**Updates**: Gateway Assistant shows the installed and the new version; update from the same page or from the watch (Settings → *Check and install*, with Debugging over Wi-Fi on).
**Groq (optional)**: Live answers general questions by itself; commands (home, calls, WhatsApp, alarms, weather, news) are carried out by the app and, with a Groq key, the text part is ready in about 1 second. Free key: https://console.groq.com → *API Keys* → *Create API Key* (it starts with `gsk_`) and paste it in Gateway → *🔑 API keys* → *Save Groq key*.
**Diagnostics**: it reaches Gateway by itself (Huawei watch page; from the watch also Settings → *Send to Gateway Assistant*). With **Share** you send it as a text file (WhatsApp, Telegram, email) to whoever is helping you.
**Two shakes to open (trial)**: in the watch settings turn on *Trial: two strong shakes open the app*. With the screen on, two sharp shakes close together open Live Assistant listening; with the always-on screen the sensor is off to save battery: raise your wrist to turn the screen back on. The lower button works too.
**Huawei power saving**: the watch may close Live Assistant in the background (lower button and shakes stop working until you open the app again). In Gateway, Huawei watch page, tap **PowerGenie: remove** (if the watch doesn't allow it, it disables it; **PowerGenie: restore** undoes it). If Debugging over Wi-Fi stays on and you are on the same network, Gateway reactivates Live Assistant by itself when the watch closes it.

### Install your own apps on the watch
On the same Gateway page, section **Install your own apps on the watch**: tap **📲 Choose the app to install** and pick the downloaded file. Single **APK**s and split bundles **APKS**, **XAPK** (OBB files included) and **APKM** all work. Debugging over Wi-Fi is needed, as for Live Assistant. In the box below you can type an **adb command** (e.g. `pm list packages -3` to list the installed apps) (section **Run on the watch**) and tap **Run**: the result appears below and **Copy result** copies it.

## Wear OS watch (beta)
Live Assistant also runs on **Wear OS watches from Android 9 on**, round and rectangular (Galaxy Watch, Pixel Watch, Oppo Watch, Mi Watch, TicWatch, Fossil…), including old **Wear OS 2 and 3** watches where Google Assistant and WhatsApp no longer work. It is the same app as on Huawei: voice questions with Gemini Live, graphic weather, Home, Contacts, WhatsApp and Telegram through Gateway.
**Link with the phone**: first the official Wear OS channel (Bluetooth, Wi-Fi or network, chosen by Wear OS), then direct Bluetooth. Gateway gives the watch the keys and the channel code: it also works away from the phone if the watch has a network.

**Installation** — in Gateway Assistant tap **⌚ Wear OS watch: install and diagnostics**. First, on the watch, turn on **Developer options**: Settings → About (on Galaxy *About watch → Software information*) → tap **Software version** or **Build number** several times. Watch and phone on the **same Wi-Fi** (the phone's hotspot is fine). Then choose the connection:
- **Wireless debugging (Wear OS 4 and later)**: Developer options → **Wireless debugging** on (*Always allow on this network*).
  1. On the watch open **Pair new device** (a 6-digit code appears).
  2. In Gateway type **only the code** and tap **🔗 Pair**: IP, connection port and pairing port are found automatically on the network (**🔍 Find the watch** button; they can also be typed in their fields). After pairing the button turns green, **Paired ✓**: no need to redo it.
  3. Tap **⬇ Download and install Live Assistant**. The connection port changes every time you turn Wireless debugging back on: if a command can't connect, empty the port field and Gateway finds it again.
- **Debug over Wi-Fi (Wear OS 2 and 3)**: Developer options → **ADB debugging** and **Debug over Wi-Fi** on. Enter the watch IP (port is already **5555**) and tap **⬇ Download and install Live Assistant**; on the watch accept debugging (**Always allow**).

Gateway installs the app, grants the permissions (microphone, sensors, updates), excludes it from battery saving, gives it the keys and opens it. Every button shows the steps in a window (**Copy** to send them to whoever helps you).
On **Pixel Watch**, if the icon doesn't appear in the app list after installing, restart the watch.
**Button to open Live** — in Live's settings on the watch (gear): *Long press Home: Live instead of the Google assistant*; on the **Galaxy Watch Ultra** the **middle (orange) button**: in Samsung's button settings choose **No app**, then in Live tap **Learn the button app** and press the button once. If the button guardian is not active, in Gateway tap **🔑 Give Live its permissions**.
**Phone notifications (Huawei only)**: Gateway → Huawei watch page → **🔔 Phone notifications on the watch**: choose the apps (tap to change: off → *nearby*, via Bluetooth → *also far*, also via internet, at most 40 a day). Dismissed or tapped on the watch, the notification also disappears from the phone. On Wear OS and Amazfit notifications already come from their own apps.
**Telegram on the watch** (Wear OS and Huawei): when the phone isn't connected via Bluetooth, over LTE or Wi-Fi you read and send Telegram (texts, voice messages, photos) right from the watch. Link it once, near the phone and with *Direct Telegram* on in Gateway: Live settings on the watch → **Link Telegram (from the phone)**. Gateway accepts the login by itself; with two-step verification the watch asks for the password. The watch shows up in Telegram → Devices as *Live Assistant (orologio)*. The connection opens only when needed and closes after 2 minutes.
**Updates**: on the watch, gear → *Check and install*. On Wear OS 4 and later the app updates itself (the first time allow *Install unknown apps*, then confirm); on Wear OS 2 and 3 it goes through Debug over Wi-Fi, which must stay on.
**On the same page**: *Send the keys to the watch*; **Screen DPI** (*Reset* goes back to the model's factory DPI, e.g. 340 on Samsung); **Install your own apps** (APK, APKS, XAPK, APKM); **Run on the watch** (adb commands); watch **Diagnostics** (with model and Android version).
**Button**: on Galaxy Watch, Settings → Advanced features → Customize keys → *Double press* → **Live Assistant**. For the center button of the Galaxy Watch Ultra we are preparing the button guardian: in Gateway tap **🔎 Study the buttons**, press the watch buttons for 15 seconds and send the result.

## With an iPhone
Gateway Assistant is Android-only: iOS does not let an app stay always on, press "Send" in WhatsApp, read notifications or pass phrases to Google Assistant.
**Live Assistant still works with an iPhone**: questions to Gemini, voice, weather, news, reminders, volume, brightness and torch.
Not available: Google home commands, calls by name from your contacts, sending and reading WhatsApp, backup phone voice.
- Skip step 1 and leave **Gateway Assistant → Code** empty.
- Keep the **Zepp app open in the background** (don't swipe it away): if iOS suspends it, the watch says "phone unreachable".
- Regular calls on the watch work with Bluetooth calls in the Zepp app.

## Wrist gestures (shakes)
Handy with background noise or busy hands. They are turned on and off in the app settings on the watch (Huawei) and work with the app open:
- **One shake while listening**: sends the question right away, without waiting for silence.
- **One shake while thinking** (colours spinning): cancels the question.
- **One shake while speaking**: stops the voice.
- **One shake when idle**: new question (listens again).
- **Two shakes**: close the app. Give the second after a short pause and **harder** than the first, so a normal second try doesn't close it by mistake.
- **Stop button (Huawei and Amazfit)**: from when it starts listening until the answer arrives, a red **■ Stop** button replaces *New chat*: it cancels the question without sending it (or drops the incoming answer) and that question's commands are not carried out. A tap on the central button while listening sends right away. When a WhatsApp/Telegram message or a voice message is sent, a big **green ✓** appears with a vibration and a short sound (no sound in privacy mode); if it fails, a **red ✗**.
Shakes don't count in the first 2 seconds after opening. After **30 seconds** of inactivity the app goes back to the watch face by itself.

## What you can say
- "What's the weather tomorrow?", "How did Arsenal do?", any question (for weather questions the watch also shows a **graphic card**: now, next hours and next days)
- "Turn on the kitchen light", "good night"
- "Call Mario" (if there are several Marios you tap one on the watch)
- "Send a WhatsApp to Mario: I'll be there in ten minutes" (tap **Send to …** to confirm)
- "Read my WhatsApp messages", "reply to Anna: sounds good"
- "Reply on Telegram to Luca: on my way" (only to Telegram chats with a recent notification; "read my messages" also shows Telegram ones)
- "Send a voice message to Mario": tap the 🎤 contact, speak and tap again to send. It arrives as a WhatsApp voice note; on Huawei Bluetooth to the phone is needed (or, on the Contacts page, **long-press WhatsApp** on a favourite: recording starts right away)
- "Turn off tomorrow's alarm", "stop the alarm", "snooze the alarm" (**phone** alarms)
- "Put the dentist in my calendar on Thursday at 10, remind me an hour before", "what do I have tomorrow?" (**phone** calendar: in Gateway Assistant tap **Allow Calendar**)
- "Add milk to my shopping list", "make a note: buy light bulbs", "remind me tomorrow at 9 on Google Tasks to call Luca" (**Keep** and **Tasks**: Gateway types the phrase to Gemini on the phone; needs Gateway Assistant accessibility and the Keep and Tasks extensions on in Gemini)
- "Turn on do not disturb until 7", "turn off do not disturb" (**phone** Do not disturb: in Gateway Assistant tap **Allow Do not disturb**; the exceptions set on the phone apply)
- "Remind me at 6 pm to call the dentist", "alarm at 7", "turn the volume up"

**Quick commands and favorites**: in Gateway Assistant, in the "On the watch: quick commands and favorites" section, add buttons with a phrase for the Assistant (e.g. "Shield" → "turn on Shield") and favorite contacts from your address book. On the watch, beside the central button: the **house** icon (or the **‹** arrow) opens **Home**, with your buttons (they go straight to the phone's Assistant, without Gemini) and **Do not disturb** to turn on and off; the **messages** icon (or the **›** arrow) opens **Contacts**, with your favorites and the **WhatsApp** (say the message and confirm with Send) and **Call** buttons.

**Favorites and groups**: up to **16 favorites** between contacts and groups. With **+ Add WhatsApp group** and **+ Add Telegram group** you pick a group: on the watch it gets its own card with the last message (and who wrote it), the bubbles and replies. **Alerts**: when a favorite writes to you (or in a favorite group) the watch shows name and preview, and tapping it opens that app's chat. With direct WhatsApp and Telegram, alerts arrive even if the phone shows no notification.

**Privacy mode**: tap the **microphone** button at the bottom right of the central button: it becomes a green **keyboard**: the microphone stays off and the central button opens the keyboard; type your question and the answer comes back as text only, with no voice. Tap it again to go back to voice. For a single typed question you can also **press and hold** the central button. Needs a watch with Zepp OS 4 or later.

## If something goes wrong
- Zepp app → Live Assistant → **Diagnostics**: shows what happened with each question. It also reaches Gateway Assistant (**⌚ Amazfit watch: diagnostics**): from there you copy it or send it as a file with **Share file**.
- In Gateway Assistant the **Log** shows calls, messages and commands.
- The gateway must be running ("Gateway running ✓") with the battery unrestricted.
- **🐞 Report a problem** in Gateway, or by voice from the watch ("report a problem: the WhatsApp button doesn't work"): the report reaches the developer with the log and the watches' diagnostics, with message texts and numbers hidden. The first time it asks for consent. Gateway also reports repeated problems by itself (at most once a day per type).
- The gateway button is **green** when running and **red** when stopped.
- **Anonymous usage count**: once a day Gateway sends only a random ID and the app versions, no personal data. Turn it off with **📊 Anonymous usage count**.

# Live Assistant (watch) + Gateway Assistant (phone) — quick guide

With your Amazfit watch (Zepp OS) or Huawei Watch 3 / Watch 4 you talk to Gemini and, through the **Gateway Assistant** app on your Android phone, you can:
control your Google home, make calls, send/read/reply to WhatsApp messages and use the phone's voice.
Everyone uses their own phone, Google account and Gemini key: nothing to share.

🌐 The apps speak **English, Italian and Spanish**: they follow the language of the watch and the phone automatically. · *Italiano: [GUIDA.md](GUIDA.md)* · *Español: [GUIA.md](GUIA.md)*

## What you need
- An Android phone with the **Zepp** app and the watch already paired
- A **Gemini API key** (free, or with credit for faster answers): https://aistudio.google.com/apikey
- The **Google** app (Assistant) on the phone, linked to your Google Home (only for home commands)

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

## 3 · Recommended
- **Calls on the watch**: Zepp app → Profile → watch → App settings → Phone → *Answer calls on the watch* (and pair Bluetooth).
- **WhatsApp with a locked phone**: Settings → Security → Smart Lock / Extend Unlock → *Trusted devices* → add the watch.
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

On the watch the **gear** under *New chat* opens the settings (city, Auto/Bluetooth/Internet connection, voice, updates, diagnostics); the **crown** scrolls the pages. Questions, voice, weather and news, Google home, Contacts and WhatsApp, calls, quick commands, reminders, torch, volume and brightness, steps and heart rate all work.
**Phone alarm**: when it rings, the watch vibrates and shows **Stop** and **Snooze** (even in night mode, which is turned off one minute before; Snooze turns it back on). It also works with last-minute alarms: in the Health app → Devices → watch → Notifications turn on **Gateway Assistant**.
**Updates**: Gateway Assistant shows the installed and the new version; update from the same page or from the watch (Settings → *Check and install*, with Debugging over Wi-Fi on).
**Groq (optional)**: Live answers general questions by itself; commands (home, calls, WhatsApp, alarms, weather, news) are carried out by the app and, with a Groq key, the text part is ready in about 1 second. Free key: https://console.groq.com → *API Keys* → *Create API Key* (it starts with `gsk_`) and paste it in Gateway, Huawei watch page → *Save Groq key*.
**Diagnostics**: watch settings → *Send to Gateway Assistant*; read it in Gateway on the Huawei watch page.

## With an iPhone
Gateway Assistant is Android-only: iOS does not let an app stay always on, press "Send" in WhatsApp, read notifications or pass phrases to Google Assistant.
**Live Assistant still works with an iPhone**: questions to Gemini, voice, weather, news, reminders, volume, brightness and torch.
Not available: Google home commands, calls by name from your contacts, sending and reading WhatsApp, backup phone voice.
- Skip step 1 and leave **Gateway Assistant → Code** empty.
- Keep the **Zepp app open in the background** (don't swipe it away): if iOS suspends it, the watch says "phone unreachable".
- Regular calls on the watch work with Bluetooth calls in the Zepp app.

## What you can say
- "What's the weather tomorrow?", "How did Arsenal do?", any question
- "Turn on the kitchen light", "good night"
- "Call Mario" (if there are several Marios you tap one on the watch)
- "Send a WhatsApp to Mario: I'll be there in ten minutes" (tap **Send to …** to confirm)
- "Read my WhatsApp messages", "reply to Anna: sounds good"
- "Turn off tomorrow's alarm", "stop the alarm", "snooze the alarm" (**phone** alarms)
- "Put the dentist in my calendar on Thursday at 10, remind me an hour before", "what do I have tomorrow?" (**phone** calendar: in Gateway Assistant tap **Allow Calendar**)
- "Add milk to my shopping list", "make a note: buy light bulbs", "remind me tomorrow at 9 on Google Tasks to call Luca" (**Keep** and **Tasks**: Gateway types the phrase to Gemini on the phone; needs Gateway Assistant accessibility and the Keep and Tasks extensions on in Gemini)
- "Turn on do not disturb until 7", "turn off do not disturb" (**phone** Do not disturb: in Gateway Assistant tap **Allow Do not disturb**; the exceptions set on the phone apply)
- "Remind me at 6 pm to call the dentist", "alarm at 7", "turn the volume up"

**Quick commands and favorites**: in Gateway Assistant, in the "On the watch: quick commands and favorites" section, add buttons with a phrase for the Assistant (e.g. "Shield" → "turn on Shield") and favorite contacts from your address book. On the watch, beside the central button: the **house** icon (or the **‹** arrow) opens **Home**, with your buttons (they go straight to the phone's Assistant, without Gemini) and **Do not disturb** to turn on and off; the **messages** icon (or the **›** arrow) opens **Contacts**, with your favorites and the **WhatsApp** (say the message and confirm with Send) and **Call** buttons.

**Privacy mode**: tap the **microphone** button at the bottom right of the central button: it becomes a green **keyboard**: the microphone stays off and the central button opens the keyboard; type your question and the answer comes back as text only, with no voice. Tap it again to go back to voice. For a single typed question you can also **press and hold** the central button. Needs a watch with Zepp OS 4 or later.

## If something goes wrong
- Zepp app → Live Assistant → **Diagnostics**: shows what happened with each question.
- In Gateway Assistant the **Log** shows calls, messages and commands.
- The gateway must be running ("Gateway running ✓") with the battery unrestricted.

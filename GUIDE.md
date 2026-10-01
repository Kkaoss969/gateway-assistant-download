# Voice Assistant (watch) + Gateway Assistant (phone) — quick guide

With your Amazfit watch (Zepp OS) you talk to Gemini and, through the **Gateway Assistant** app on your Android phone, you can:
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
   If a setting is "restricted": Settings → Apps → Gateway Assistant → ⋮ menu → *Allow restricted settings*.
5. Tap **Copy code** (the channel code).

## 2 · Install Voice Assistant on the watch
1. In the Zepp app turn on developer mode: Profile → Settings → About → tap the Zepp logo several times.
2. Open **https://kkaoss969.github.io/gateway-assistant-download/**, choose your watch and scan the **QR code** with the Zepp app (Profile → scan icon).
3. In the Zepp app open the settings of the **Voice Assistant** app and fill in:
   - **Gemini API key**
   - **My city** (weather and local news)
   - **Gateway Assistant → Code**: paste the code copied in step 1
   - **Names you often use** (optional): people, towns, teams… they help it understand the right names

## 3 · Recommended
- **Calls on the watch**: Zepp app → Profile → watch → App settings → Phone → *Answer calls on the watch* (and pair Bluetooth).
- **WhatsApp with a locked phone**: Settings → Security → Smart Lock / Extend Unlock → *Trusted devices* → add the watch.
  Without it, the phone wakes up and the message is sent when you unlock it.
- **Home commands with a locked phone**: Google app → Settings → Google Assistant → Lock screen → personal results on.

## What you can say
- "What's the weather tomorrow?", "How did Arsenal do?", any question
- "Turn on the kitchen light", "good night"
- "Call Mario" (if there are several Marios you tap one on the watch)
- "Send a WhatsApp to Mario: I'll be there in ten minutes" (tap **Send to …** to confirm)
- "Read my WhatsApp messages", "reply to Anna: sounds good"
- "Remind me at 6 pm to call the dentist", "alarm at 7", "turn the volume up"

## If something goes wrong
- Zepp app → Voice Assistant → **Diagnostics**: shows what happened with each question.
- In Gateway Assistant the **Log** shows calls, messages and commands.
- The gateway must be running ("Gateway running ✓") with the battery unrestricted.

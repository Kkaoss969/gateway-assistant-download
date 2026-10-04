# Voice Assistant (reloj) + Gateway Assistant (teléfono) — guía rápida

Con tu reloj Amazfit (Zepp OS) hablas con Gemini y, a través de la app **Gateway Assistant** en tu teléfono Android, puedes:
controlar tu casa Google, llamar, enviar/leer/responder WhatsApp y usar la voz del teléfono.
Cada uno usa su propio teléfono, su cuenta de Google y su clave de Gemini: no hay nada que compartir.

🌐 Las apps hablan **español, italiano e inglés**: siguen solas el idioma del reloj y del teléfono. · *Italiano: [GUIDA.md](GUIDA.md)* · *English: [GUIDE.md](GUIDE.md)*

## Qué necesitas
- Un teléfono Android con la app **Zepp** y el reloj ya vinculado
- Una **clave API de Gemini** (gratis, o con crédito para respuestas más rápidas): https://aistudio.google.com/apikey
- La app **Google** (Asistente) en el teléfono, vinculada a tu casa Google Home (solo para las órdenes de casa)

## 1 · Instala Gateway Assistant (teléfono)
1. Descarga el APK en el teléfono: **https://github.com/Kkaoss969/gateway-assistant-download/raw/main/GatewayAssistant.apk**
2. Ábrelo y permite la instalación desde esta fuente si Android lo pide.
3. Abre **Gateway Assistant** y toca **Iniciar el gateway**.
4. En la lista de **Permisos** toca cada fila con ⚪ hasta que estén todas ✅:
   contactos y llamadas · mostrar sobre otras apps · envío de WhatsApp (accesibilidad) · lectura de WhatsApp (notificaciones) · batería sin restricciones.
   Si un ajuste aparece "restringido": Ajustes → Apps → Gateway Assistant → menú ⋮ → *Permitir ajustes restringidos*.
5. Toca **Copiar código** (el código del canal).

## 2 · Instala Voice Assistant en el reloj
1. En la app Zepp activa el modo desarrollador: Perfil → Ajustes → Acerca de → toca varias veces el logo de Zepp.
2. Abre **https://kkaoss969.github.io/gateway-assistant-download/**, elige tu reloj y escanea el **código QR** con la app Zepp (Perfil → icono de escanear).
3. En la app Zepp abre los ajustes de la app **Voice Assistant** y rellena:
   - **Clave API de Gemini**
   - **Mi ciudad** (tiempo y noticias locales)
   - **Gateway Assistant → Código**: pega el código copiado en el paso 1
   - **Nombres que usas a menudo** (opcional): personas, pueblos, equipos… ayudan a entender los nombres correctos

## 3 · Recomendado
- **Llamadas en el reloj**: app Zepp → Perfil → reloj → Ajustes de apps → Teléfono → *Contestar llamadas en el reloj* (y vincula el Bluetooth).
- **WhatsApp con el teléfono bloqueado**: Ajustes → Seguridad → Smart Lock / Desbloqueo ampliado → *Dispositivos de confianza* → añade el reloj.
  Sin esto, el teléfono se enciende y el mensaje se envía cuando lo desbloquees.
- **Órdenes de casa con el teléfono bloqueado**: app Google → Ajustes → Asistente de Google → Pantalla de bloqueo → resultados personales activados.

**Alarma del teléfono**: cuando suena, el reloj vibra y abre solo los botones **Apagar** y **Posponer**. El reloj aprende la hora de la próxima alarma cada vez que abres Voice Assistant (y después de cada alarma): si creas una alarma nueva en el teléfono, abre la app en el reloj una vez. ⚠ En **modo sueño** o **no molestar** el reloj bloquea las apps externas: programa el modo sueño / no molestar para que termine unos minutos antes de la alarma (Ajustes del reloj → No molestar → Programado).

## Con iPhone
Gateway Assistant solo existe para Android: iOS no permite que una app esté siempre activa, pulse "Enviar" en WhatsApp, lea notificaciones o pase frases al Asistente de Google.
**Pero Voice Assistant funciona también con iPhone**: preguntas a Gemini, voz, tiempo, noticias, recordatorios, volumen, brillo y linterna.
No funcionan: órdenes para la casa Google, llamadas por nombre desde los contactos, envío y lectura de WhatsApp, voz de reserva del teléfono.
- Sáltate el paso 1 y deja vacío **Gateway Assistant → Código**.
- Mantén la **app Zepp abierta en segundo plano** (no la cierres desde la multitarea): si iOS la suspende, el reloj dice "teléfono no disponible".
- Las llamadas normales en el reloj funcionan con las llamadas Bluetooth de la app Zepp.

## Qué puedes decir
- «¿Qué tiempo hará mañana?», «¿Cómo ha quedado el Betis?», cualquier pregunta
- «Enciende la luz de la cocina», «buenas noches»
- «Llama a Mario» (si hay varios Mario eliges uno en el reloj)
- «Manda un WhatsApp a Mario: llego en diez minutos» (toca **Enviar a …** para confirmar)
- «Lee los mensajes de WhatsApp», «responde a Ana: vale»
- «Desactiva la alarma de mañana», «para la alarma», «pospón la alarma» (alarmas del **teléfono**)
- «Apunta en el calendario el dentista el jueves a las 10, avísame una hora antes», «¿qué tengo mañana?» (calendario del **teléfono**: en Gateway Assistant toca **Permitir el Calendario**)
- «Añade leche a la lista de la compra», «crea una nota: comprar bombillas», «recuérdame mañana a las 9 en Google Tasks llamar a Luca» (**Keep** y **Tasks**: Gateway escribe la frase a Gemini en el teléfono; hacen falta la accesibilidad de Gateway Assistant y las extensiones Keep y Tasks activas en Gemini)
- «Activa no molestar hasta las 7», «quita no molestar» (No molestar del **teléfono**: en Gateway Assistant toca **Permitir No molestar**; valen las excepciones configuradas en el teléfono)
- «Recuérdame a las 18 llamar al dentista», «alarma a las 7», «sube el volumen»

## Si algo no funciona
- App Zepp → Voice Assistant → **Diagnóstico**: muestra qué ha pasado con cada pregunta.
- En Gateway Assistant el **Registro** muestra llamadas, mensajes y órdenes.
- El gateway debe estar en marcha ("Gateway activo ✓") y con la batería sin restricciones.

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

## Qué puedes decir
- «¿Qué tiempo hará mañana?», «¿Cómo ha quedado el Betis?», cualquier pregunta
- «Enciende la luz de la cocina», «buenas noches»
- «Llama a Mario» (si hay varios Mario eliges uno en el reloj)
- «Manda un WhatsApp a Mario: llego en diez minutos» (toca **Enviar a …** para confirmar)
- «Lee los mensajes de WhatsApp», «responde a Ana: vale»
- «Recuérdame a las 18 llamar al dentista», «alarma a las 7», «sube el volumen»

## Si algo no funciona
- App Zepp → Voice Assistant → **Diagnóstico**: muestra qué ha pasado con cada pregunta.
- En Gateway Assistant el **Registro** muestra llamadas, mensajes y órdenes.
- El gateway debe estar en marcha ("Gateway activo ✓") y con la batería sin restricciones.

# Voice Assistant (reloj) + Gateway Assistant (teléfono) — guía rápida

Con tu reloj Amazfit (Zepp OS) o Huawei Watch 3 / Watch 4 hablas con Gemini y, a través de la app **Gateway Assistant** en tu teléfono Android, puedes:
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
   ⚠ **Accesibilidad**: en la página de Android "Gateway Assistant (envío de WhatsApp)" activa **solo el primer interruptor de arriba** ("Activado"). **No actives** el segundo, "Acceso directo a Gateway Assistant": es solo un atajo de Android y, si está activado, los toques automáticos (Enviar de WhatsApp, Apagar/Posponer de la alarma, envío a Gemini) no funcionan.
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

## Reloj Huawei (Watch 3, Watch 4)
Voice Assistant también existe para los **Huawei Watch 3 y Watch 4** (los basados en Android). Se instala desde **Gateway Assistant**, sin ordenador.
1. En el reloj: Ajustes → Información → toca varias veces el **número de compilación**. Luego en **Opciones de desarrollador** activa **Depuración HDC** y **Depuración por Wi-Fi**.
2. Reloj y teléfono en la **misma red Wi-Fi** (sirve el punto de acceso del teléfono).
3. En Gateway Assistant toca **⌚ Reloj Huawei: instalar y diagnóstico**, escribe la IP que aparece en *Depuración por Wi-Fi* y toca **Descargar e instalar Voice Assistant**. La primera vez el reloj pide permitir la conexión: toca **Permitir siempre**.
   Gateway pasa al reloj el código del canal y, si la casilla está marcada, tu clave de Gemini; también excluye la app del ahorro de batería.
4. En Gateway Assistant toca **⚪ Permitir Bluetooth Huawei** hasta que aparezca **✅ Bluetooth Huawei: activo**: así el reloj funciona **sin Wi-Fi ni LTE**, a través del Bluetooth del teléfono.
5. **Botón inferior**: en la misma página toca **Botón inferior: abrir Voice Assistant**. Al pulsar el botón inferior del reloj se abre Voice Assistant ya escuchando en lugar de Celia (*Restaurar Celia* lo deshace).

En el reloj el **engranaje** bajo *Nuevo chat* abre los ajustes (ciudad, conexión Auto/Bluetooth/Internet, voz, actualizaciones, diagnóstico); la **corona** desplaza las páginas. Funcionan preguntas, voz, tiempo y noticias, casa Google, Contactos y WhatsApp, llamadas, órdenes rápidas, recordatorios, linterna, volumen y brillo, pasos y pulso.
**Actualizaciones**: Gateway Assistant muestra la versión instalada y la nueva; actualizas desde la misma página o desde el reloj (Ajustes → *Comprobar e instalar*, con la Depuración por Wi-Fi activa).
**Diagnóstico**: ajustes del reloj → *Enviar a Gateway Assistant*; lo lees en Gateway en la página del reloj Huawei.

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

**Órdenes rápidas y favoritos**: en Gateway Assistant, en la sección "En el reloj: órdenes rápidas y favoritos", añade botones con una frase para el Asistente (p. ej. "Shield" → "enciende Shield") y los contactos favoritos de la agenda. En el reloj, a los lados del botón central: el icono de la **casa** (o la flecha **‹**) abre **Casa**, con tus botones (van directamente al Asistente del teléfono, sin Gemini) y **No molestar** para activar y desactivar; el icono de los **mensajes** (o la flecha **›**) abre **Contactos**, con los favoritos y los botones **WhatsApp** (dictas el mensaje y confirmas con Enviar) y **Llamar**.

**Modo privacidad**: toca el botón del **micrófono** abajo a la derecha del botón central: se convierte en un **teclado** verde: el micrófono queda apagado y el botón central abre el teclado; escribe la pregunta y la respuesta llega solo escrita, sin voz. Tócalo otra vez para volver a la voz. Para una sola pregunta escrita también puedes **mantener pulsado** el botón central. Necesita un reloj con Zepp OS 4 o posterior.

## Si algo no funciona
- App Zepp → Voice Assistant → **Diagnóstico**: muestra qué ha pasado con cada pregunta.
- En Gateway Assistant el **Registro** muestra llamadas, mensajes y órdenes.
- El gateway debe estar en marcha ("Gateway activo ✓") y con la batería sin restricciones.

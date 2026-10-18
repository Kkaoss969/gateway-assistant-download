# Live Assistant (reloj) + Gateway Assistant (teléfono) — guía rápida

Con tu reloj Amazfit (Zepp OS), Huawei Watch 3 / Watch 4 o **Wear OS** (Galaxy Watch, Pixel Watch, TicWatch…) hablas con Gemini y, a través de la app **Gateway Assistant** en tu teléfono Android, puedes:
controlar tu casa Google, llamar, enviar/leer/responder WhatsApp y usar la voz del teléfono.
Cada uno usa su propio teléfono, su cuenta de Google y su clave de Gemini: no hay nada que compartir.

🌐 Las apps hablan **español, italiano e inglés**: siguen solas el idioma del reloj y del teléfono. · *Italiano: [GUIDA.md](GUIDA.md)* · *English: [GUIDE.md](GUIDE.md)*

## Qué necesitas
- Un teléfono Android con la app **Zepp** y el reloj ya vinculado
- Una **clave API de Gemini** (gratis, o con crédito para respuestas más rápidas): https://aistudio.google.com/apikey
- La app **Google** (Asistente) en el teléfono, vinculada a tu casa Google Home (solo para las órdenes de casa)

## Claves API
Las claves se escriben **una sola vez** en Gateway Assistant → **🔑 Claves API** y valen para todos los relojes; desde la página de cada reloj se las pasas a Live con *Enviar las claves al reloj* (o al instalar).
- **Gemini** (necesaria, gratuita): abre https://aistudio.google.com/apikey con tu cuenta de Google → **Create API key** (o *Crear clave de API*) → elige o crea un proyecto → copia la clave (empieza por `AIza` o `AQ.`) y pégala en Gateway → *Guardar clave de Gemini*. El plan gratuito tiene límites diarios; con algo de crédito las respuestas son más rápidas.
- **Groq** (opcional, gratuita): abre https://console.groq.com/keys, entra (también con Google) → **Create API Key** → ponle un nombre → copia la clave (empieza por `gsk_`, se ve una sola vez) y pégala en Gateway → *Guardar clave de Groq*. Sirve para respuestas escritas en 1 segundo.
- Para quitar una clave mantén pulsado su botón *Guardar*.

## 1 · Instala Gateway Assistant (teléfono)
1. Descarga el APK en el teléfono: **https://github.com/Kkaoss969/gateway-assistant-download/raw/main/GatewayAssistant.apk**
2. Ábrelo y permite la instalación desde esta fuente si Android lo pide.
3. Abre **Gateway Assistant** y toca **Iniciar el gateway**.
4. En la lista de **Permisos** toca cada fila con ⚪ hasta que estén todas ✅:
   contactos y llamadas · mostrar sobre otras apps · envío de WhatsApp (accesibilidad) · lectura de WhatsApp (notificaciones) · batería sin restricciones.
   ⚠ **Accesibilidad**: en la página de Android "Gateway Assistant (envío de WhatsApp)" activa **solo el primer interruptor de arriba** ("Activado"). **No actives** el segundo, "Acceso directo a Gateway Assistant": es solo un atajo de Android y, si está activado, los toques automáticos (Enviar de WhatsApp, Apagar/Posponer de la alarma, envío a Gemini) no funcionan.
   Si un ajuste aparece "restringido": Ajustes → Apps → Gateway Assistant → menú ⋮ → *Permitir ajustes restringidos*.
5. Toca **Copiar código** (el código del canal).

## 2 · Instala Live Assistant en el reloj
1. En la app Zepp activa el modo desarrollador: Perfil → Ajustes → Acerca de → toca varias veces el logo de Zepp.
2. Abre **https://kkaoss969.github.io/gateway-assistant-download/**, elige tu reloj y escanea el **código QR** con la app Zepp (Perfil → icono de escanear).
3. En la app Zepp abre los ajustes de la app **Live Assistant** y rellena:
   - **Clave API de Gemini**
   - **Mi ciudad** (tiempo y noticias locales)
   - **Gateway Assistant → Código**: pega el código copiado en el paso 1
   - **Clave API de Groq** (opcional, gratis en https://console.groq.com → *API Keys*): noticias y preguntas escritas responden en 1 segundo aprox.; las preguntas habladas siguen con Gemini
   - **Nombres que usas a menudo** (opcional): personas, pueblos, equipos… ayudan a entender los nombres correctos

## 3 · Recomendado
- **Llamadas en el reloj**: app Zepp → Perfil → reloj → Ajustes de apps → Teléfono → *Contestar llamadas en el reloj* (y vincula el Bluetooth).
- **WhatsApp con el teléfono bloqueado**: Ajustes → Seguridad → Smart Lock / Desbloqueo ampliado → *Dispositivos de confianza* → añade el reloj.
- **WhatsApp doble (clon)**: si el teléfono tiene un segundo WhatsApp clonado (Dual Messenger de Samsung, "Apps duplicadas" en otros teléfonos), los mensajes de texto se envían pero **los audios del reloj no** (WhatsApp abre el chat sin el audio). Para enviar audios elimina el WhatsApp clonado; dos cuentas en el mismo WhatsApp sí funcionan. Gateway lo indica con ⚠️ en el botón de envío de WhatsApp.
- **Beeper (experimental)**: si usas [Beeper](https://play.google.com/store/apps/details?id=com.beeper.android) con WhatsApp y Telegram vinculados, toca *🧪 Beeper* en Gateway y permite el acceso: los mensajes de texto se envían sin abrir WhatsApp y sin accesibilidad, incluso con el teléfono bloqueado, y en Telegram puedes escribir a cualquier chat. Los audios siguen pasando por WhatsApp.
  Sin esto, el teléfono se enciende y el mensaje se envía cuando lo desbloquees.
- **Órdenes de casa con el teléfono bloqueado**: app Google → Ajustes → Asistente de Google → Pantalla de bloqueo → resultados personales activados.

**Alarma del teléfono**: cuando suena, el reloj vibra y abre solo los botones **Apagar** y **Posponer**. El reloj aprende la hora de la próxima alarma cada vez que abres Live Assistant (y después de cada alarma): si creas una alarma nueva en el teléfono, abre la app en el reloj una vez. ⚠ En **modo sueño** o **no molestar** el reloj bloquea las apps externas: programa el modo sueño / no molestar para que termine unos minutos antes de la alarma (Ajustes del reloj → No molestar → Programado).

**Gemini Live (prueba)**: en la app Zepp → Live Assistant → Ajustes activa **Usar Gemini Live** (necesita Gateway Assistant 1.65 o posterior en el mismo teléfono). La respuesta llega ya como voz, sin esperar la síntesis; si Live falla se usa el método normal.

## Reloj Huawei (Watch 3, Watch 4)
Para los **Huawei Watch 3 y Watch 4** (los basados en Android) existe **Live Assistant**, con **Gemini Live**: mientras hablas la pregunta ya va hacia Gemini y la respuesta llega directamente por voz, normalmente en 1-3 segundos. Funciona con el Wi-Fi o LTE del reloj y también solo por Bluetooth, a través de Gateway. Se instala desde **Gateway Assistant**, sin ordenador.
1. En el reloj: Ajustes → Información → toca varias veces el **número de compilación**. Luego en **Opciones de desarrollador** activa **Depuración HDC** y **Depuración por Wi-Fi**.
2. Reloj y teléfono en la **misma red Wi-Fi** (sirve el punto de acceso del teléfono).
3. En Gateway Assistant toca **⌚ Reloj Huawei: instalar y diagnóstico**, escribe la IP que aparece en *Depuración por Wi-Fi* y toca **Descargar e instalar Live Assistant**. La primera vez el reloj pide permitir la conexión: toca **Permitir siempre**.
   Gateway pasa al reloj el código del canal y, si la casilla está marcada, tu clave de Gemini; también excluye la app del ahorro de batería.
4. En Gateway Assistant toca **⚪ Permitir Bluetooth Huawei** hasta que aparezca **✅ Bluetooth Huawei: activo**: así el reloj funciona **sin Wi-Fi ni LTE**, a través del Bluetooth del teléfono.
5. **Botón inferior**: en la misma página toca **Botón inferior: abrir Live Assistant**. Al pulsar el botón inferior del reloj se abre Live Assistant ya escuchando en lugar de Celia (*Restaurar Celia* lo deshace).

En el reloj el **engranaje** bajo *Nuevo chat* abre los ajustes (ciudad, conexión Auto/Bluetooth/Internet, voz, actualizaciones, diagnóstico); la **corona** desplaza las páginas. Funcionan preguntas, voz, tiempo y noticias, casa Google, Contactos y WhatsApp, llamadas, órdenes rápidas, recordatorios, linterna, volumen y brillo, pasos y pulso. Por voz también puedes cambiar los **DPI de la pantalla** ("pon los dpi a 280", "restablece los dpi"; de 90 a 400, estándar 320); en los ajustes del reloj está **Restablecer DPI**, y en Gateway (página del reloj Huawei, sección *DPI de la pantalla*) **Aplicar** y **Restablecer (320)**.
**Alarma del teléfono**: cuando suena, el reloj vibra y muestra **Apagar** y **Posponer** (también en modo noche, que se desactiva un minuto antes; con Posponer se reactiva). Funciona también con alarmas creadas en el último momento: en la app Salud → Dispositivos → reloj → Notificaciones activa **Gateway Assistant**.
**Actualizaciones**: Gateway Assistant muestra la versión instalada y la nueva; actualizas desde la misma página o desde el reloj (Ajustes → *Comprobar e instalar*, con la Depuración por Wi-Fi activa).
**Groq (opcional)**: Live responde solo a las preguntas generales; las órdenes (casa, llamadas, WhatsApp, alarmas, tiempo, noticias) las ejecuta la app y, con una clave de Groq, la parte escrita está lista en 1 segundo aprox. Clave gratuita: https://console.groq.com → *API Keys* → *Create API Key* (empieza por `gsk_`) y pégala en Gateway → *🔑 Claves API* → *Guardar clave de Groq*.
**Diagnóstico**: llega solo a Gateway (página del reloj Huawei; desde el reloj también Ajustes → *Enviar a Gateway Assistant*). Con **Compartir** lo envías como archivo de texto (WhatsApp, Telegram, email) a quien te ayude.
**Dos sacudidas para abrir (prueba)**: en los ajustes del reloj activa *Prueba: dos sacudidas fuertes abren la app*. Con la pantalla encendida, dos sacudidas secas y seguidas abren Live Assistant escuchando; con la pantalla siempre activa el sensor está apagado para ahorrar batería: levanta la muñeca para encender la pantalla. El botón inferior también funciona.
**Ahorro de energía Huawei**: el reloj puede cerrar Live Assistant en segundo plano (el botón inferior y las sacudidas dejan de funcionar hasta que abras la app). En Gateway, página del reloj Huawei, toca **PowerGenie: eliminar** (si el reloj no lo permite, lo desactiva; **PowerGenie: restaurar** lo deshace). Si la Depuración por Wi-Fi sigue activa y estás en la misma red, Gateway reactiva solo Live Assistant cuando el reloj lo cierra.

### Instala tus apps en el reloj
En la misma página de Gateway, sección **Instala tus apps en el reloj**: toca **📲 Elegir la app que instalar** y elige el archivo descargado. Sirven los **APK** sueltos y los paquetes divididos **APKS**, **XAPK** (también con archivos OBB) y **APKM**. Hace falta la Depuración por Wi-Fi, como para Live Assistant. En la casilla de abajo puedes escribir una **orden adb** (p. ej. `pm list packages -3` para ver las apps instaladas) (sección **Ejecutar en el reloj**) y tocar **Ejecutar**: el resultado aparece debajo y lo copias con **Copiar resultado**.

## Reloj Wear OS (prueba)
Live Assistant también funciona en relojes **Wear OS desde Android 9**, redondos y rectangulares (Galaxy Watch, Pixel Watch, Oppo Watch, Mi Watch, TicWatch, Fossil…), incluidos los antiguos **Wear OS 2 y 3** donde el Asistente de Google y WhatsApp ya no funcionan. Es la misma app que en Huawei: preguntas por voz con Gemini Live, tiempo gráfico, Casa, Contactos, WhatsApp y Telegram a través de Gateway.
**Conexión con el teléfono**: primero el canal oficial de Wear OS (Bluetooth, Wi-Fi o red, lo elige Wear OS), luego el Bluetooth directo. Gateway pasa al reloj las claves y el código del canal: funciona también lejos del teléfono si el reloj tiene red.

**Instalación** — en Gateway Assistant toca **⌚ Reloj Wear OS: instalar y diagnóstico**. Antes, en el reloj, activa las **Opciones de desarrollador**: Ajustes → Información (en Galaxy *Acerca del reloj → Información de software*) → toca varias veces **Versión de software** o **Número de compilación**. Reloj y teléfono en la **misma Wi-Fi** (vale el punto de acceso del teléfono). Luego elige la conexión:
- **Depuración inalámbrica (Wear OS 4 y posteriores)**: Opciones de desarrollador → **Depuración inalámbrica** activa (*Permitir siempre en esta red*).
  1. En el reloj abre **Vincular dispositivo nuevo** (aparece un código de 6 cifras).
  2. En Gateway escribe **solo el código** y toca **🔗 Vincular**: IP, puerto de conexión y puerto de vinculación los encuentra solo en la red (botón **🔍 Buscar el reloj**; también se pueden escribir en sus campos). Tras vincular el botón se pone verde, **Vinculado ✓**: no hace falta repetirlo.
  3. Toca **⬇ Descargar e instalar Live Assistant**. El puerto de conexión cambia cada vez que reactivas la depuración inalámbrica: si una orden no se conecta, vacía el campo del puerto y Gateway lo vuelve a encontrar.
- **Depuración por Wi-Fi (Wear OS 2 y 3)**: Opciones de desarrollador → **Depuración ADB** y **Depuración por Wi-Fi** activas. Escribe la IP del reloj (el puerto ya es **5555**) y toca **⬇ Descargar e instalar Live Assistant**; en el reloj acepta la depuración (**Permitir siempre**).

Gateway instala la app, da los permisos (micrófono, sensores, actualizaciones), la excluye del ahorro de batería, le pasa las claves y la abre. Cada botón muestra los pasos en una ventana (**Copiar** para enviarlos a quien te ayude).
En el **Pixel Watch**, si después de instalar el icono no aparece en la lista de apps, reinicia el reloj.
**Botón para abrir Live** — en los ajustes de Live en el reloj (engranaje): *Pulsación larga de Inicio: Live en lugar del asistente de Google*; en el **Galaxy Watch Ultra** el **botón central (naranja)**: en los ajustes de Samsung del botón elige **Ninguna app**, luego en Live toca **Aprender la app del botón** y pulsa el botón una vez. Si el guardián de botones no está activo, en Gateway toca **🔑 Dar los permisos a Live**.
**Telegram en el reloj** (Wear OS y Huawei): cuando el teléfono no está conectado por Bluetooth, por LTE o Wi-Fi lees y envías Telegram (textos, audios, fotos) directamente desde el reloj. Se vincula una vez, cerca del teléfono y con *Telegram directo* activo en Gateway: ajustes de Live en el reloj → **Vincular Telegram (desde el teléfono)**. Gateway acepta el acceso solo; con verificación en dos pasos el reloj pide la contraseña. El reloj aparece en Telegram → Dispositivos como *Live Assistant (orologio)*. La conexión se abre solo cuando hace falta y se cierra tras 2 minutos.
**Actualizaciones**: en el reloj, engranaje → *Comprobar e instalar*. En Wear OS 4 y posteriores la app se actualiza sola (la primera vez permite *Instalar apps desconocidas* y luego confirma); en Wear OS 2 y 3 pasa por la depuración por Wi-Fi, que debe quedar activa.
**En la misma página**: *Enviar las claves al reloj*; **DPI de la pantalla** (*Restablecer* vuelve a los DPI de fábrica del modelo, p. ej. 340 en Samsung); **Instala tus apps** (APK, APKS, XAPK, APKM); **Ejecutar en el reloj** (órdenes adb); **Diagnóstico** del reloj (con modelo y versión de Android).
**Botón**: en Galaxy Watch, Ajustes → Funciones avanzadas → Personalizar botones → *Pulsar dos veces* → **Live Assistant**. Para el botón central de los Galaxy Watch Ultra estamos preparando el guardián del botón: en Gateway toca **🔎 Estudiar los botones**, pulsa los botones del reloj durante 15 segundos y envía el resultado.

## Con iPhone
Gateway Assistant solo existe para Android: iOS no permite que una app esté siempre activa, pulse "Enviar" en WhatsApp, lea notificaciones o pase frases al Asistente de Google.
**Pero Live Assistant funciona también con iPhone**: preguntas a Gemini, voz, tiempo, noticias, recordatorios, volumen, brillo y linterna.
No funcionan: órdenes para la casa Google, llamadas por nombre desde los contactos, envío y lectura de WhatsApp, voz de reserva del teléfono.
- Sáltate el paso 1 y deja vacío **Gateway Assistant → Código**.
- Mantén la **app Zepp abierta en segundo plano** (no la cierres desde la multitarea): si iOS la suspende, el reloj dice "teléfono no disponible".
- Las llamadas normales en el reloj funcionan con las llamadas Bluetooth de la app Zepp.

## Gestos de muñeca (sacudidas)
Útiles con ruido de fondo o con las manos ocupadas. Se activan y desactivan en los ajustes de la app en el reloj (Huawei) y funcionan con la app abierta:
- **Una sacudida mientras escucha**: envía la pregunta enseguida, sin esperar el silencio.
- **Una sacudida mientras piensa** (giran los colores): cancela la pregunta.
- **Una sacudida mientras habla**: para la voz.
- **Una sacudida en reposo**: nueva pregunta (vuelve a escuchar).
- **Dos sacudidas**: cierran la app. La segunda, tras una breve pausa y **más fuerte** que la primera, para que un segundo intento normal no la cierre por error.
- **Botón Stop (Huawei y Amazfit)**: desde que empieza a escuchar hasta que llega la respuesta, en lugar de *Nuevo chat* aparece un botón rojo **■ Stop**: cancela la pregunta sin enviarla (o descarta la respuesta que llega) y los comandos de esa pregunta no se ejecutan. Un toque en el botón central mientras escucha envía enseguida. Cuando un mensaje de WhatsApp/Telegram o un audio se envía, aparece una gran **✓ verde** con vibración y un breve sonido (sin sonido en modo privacidad); si no se envía, una **✗ roja**.
Las sacudidas no cuentan en los 2 primeros segundos tras abrir. Tras **30 segundos** sin hacer nada la app vuelve sola a la esfera.

## Qué puedes decir
- «¿Qué tiempo hará mañana?», «¿Cómo ha quedado el Betis?», cualquier pregunta (con las preguntas sobre el tiempo el reloj muestra también la **tarjeta gráfica**: ahora, próximas horas y próximos días)
- «Enciende la luz de la cocina», «buenas noches»
- «Llama a Mario» (si hay varios Mario eliges uno en el reloj)
- «Manda un WhatsApp a Mario: llego en diez minutos» (toca **Enviar a …** para confirmar)
- «Lee los mensajes de WhatsApp», «responde a Ana: vale»
- "Responde en Telegram a Luca: llego" (solo a chats de Telegram con una notificación reciente; "lee los mensajes" muestra también los de Telegram)
- "Envía un audio a Mario": toca el contacto 🎤, habla y vuelve a tocar para enviar. Llega como nota de voz de WhatsApp; en Huawei hace falta el Bluetooth con el teléfono (o, en la página Contactos, **mantén pulsado WhatsApp** en un favorito: la grabación empieza enseguida)
- «Desactiva la alarma de mañana», «para la alarma», «pospón la alarma» (alarmas del **teléfono**)
- «Apunta en el calendario el dentista el jueves a las 10, avísame una hora antes», «¿qué tengo mañana?» (calendario del **teléfono**: en Gateway Assistant toca **Permitir el Calendario**)
- «Añade leche a la lista de la compra», «crea una nota: comprar bombillas», «recuérdame mañana a las 9 en Google Tasks llamar a Luca» (**Keep** y **Tasks**: Gateway escribe la frase a Gemini en el teléfono; hacen falta la accesibilidad de Gateway Assistant y las extensiones Keep y Tasks activas en Gemini)
- «Activa no molestar hasta las 7», «quita no molestar» (No molestar del **teléfono**: en Gateway Assistant toca **Permitir No molestar**; valen las excepciones configuradas en el teléfono)
- «Recuérdame a las 18 llamar al dentista», «alarma a las 7», «sube el volumen»

**Órdenes rápidas y favoritos**: en Gateway Assistant, en la sección "En el reloj: órdenes rápidas y favoritos", añade botones con una frase para el Asistente (p. ej. "Shield" → "enciende Shield") y los contactos favoritos de la agenda. En el reloj, a los lados del botón central: el icono de la **casa** (o la flecha **‹**) abre **Casa**, con tus botones (van directamente al Asistente del teléfono, sin Gemini) y **No molestar** para activar y desactivar; el icono de los **mensajes** (o la flecha **›**) abre **Contactos**, con los favoritos y los botones **WhatsApp** (dictas el mensaje y confirmas con Enviar) y **Llamar**.

**Favoritos y grupos**: hasta **16 favoritos** entre contactos y grupos. Con **+ Añadir grupo de WhatsApp** y **+ Añadir grupo de Telegram** eliges un grupo: en el reloj tiene su tarjeta con el último mensaje (y quién lo escribió), las burbujas y la respuesta. **Avisos**: cuando te escribe un favorito (o en un grupo favorito) el reloj muestra nombre y vista previa, y al tocarlo se abre el chat de esa app. Con WhatsApp y Telegram directos los avisos llegan aunque el teléfono no muestre la notificación.

**Modo privacidad**: toca el botón del **micrófono** abajo a la derecha del botón central: se convierte en un **teclado** verde: el micrófono queda apagado y el botón central abre el teclado; escribe la pregunta y la respuesta llega solo escrita, sin voz. Tócalo otra vez para volver a la voz. Para una sola pregunta escrita también puedes **mantener pulsado** el botón central. Necesita un reloj con Zepp OS 4 o posterior.

## Si algo no funciona
- App Zepp → Live Assistant → **Diagnóstico**: muestra qué ha pasado con cada pregunta. También llega a Gateway Assistant (**⌚ Reloj Amazfit: diagnóstico**): desde ahí lo copias o lo envías como archivo con **Compartir archivo**.
- En Gateway Assistant el **Registro** muestra llamadas, mensajes y órdenes.
- El gateway debe estar en marcha ("Gateway activo ✓") y con la batería sin restricciones.
- **🐞 Informar de un problema** en Gateway, o por voz desde el reloj ("informa de un problema: el botón de WhatsApp no va"): el informe llega al desarrollador con el registro y el diagnóstico de los relojes, con textos de los mensajes y números ocultos. La primera vez pide el consentimiento. Gateway también informa solo de los problemas que se repiten (como máximo una vez al día por tipo).
- El botón del gateway es **verde** cuando está activo y **rojo** cuando está detenido.
- **Recuento anónimo de uso**: una vez al día Gateway envía solo un identificador aleatorio y las versiones de las apps, ningún dato personal. Se desactiva con **📊 Recuento anónimo de uso**.

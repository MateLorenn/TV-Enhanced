# Nuvio estilo Apple TV + Free My TV

Las dos apps que armamos para el onn 4K (Google TV), listas para instalar.
**No traen ninguna clave personal:** cada persona carga las suyas.

| Archivo | Qué es |
|---|---|
| `apks/Nuvio-AppleTV.apk` | Nuvio con la interfaz estilo Apple TV (onn 4K, Chromecast y la mayoría de las teles: 32 bits) |
| `apks/Nuvio-AppleTV-arm64.apk` | La misma, para equipos de 64 bits (NVIDIA Shield, Google TV Streamer) |
| `apks/FreeMyTV.apk` | El inicio estilo Apple TV, con Seguir viendo y Para vos de Nuvio |

## Instalar

1. En la tele: **Configuración → Sistema → Información → Compilación del SO**, apretar OK 7 veces (se activan las opciones de desarrollador). Después **Configuración → Sistema → Opciones de desarrollador → Depuración por USB**: activada. Hace falta aunque no uses compu: Free My TV la usa desde la misma tele para pasar a ser el inicio.
2. **Sin compu, con Send Files to TV:**
   - Instalar **Send Files to TV** en la tele (Play Store) y en el celular.
   - Bajar los APK de este repositorio al celular y mandarlos a la tele con la app.
   - En la tele, abrir Send Files to TV → el APK. La primera vez pide permiso para **instalar apps desconocidas**: activarlo para Send Files to TV y volver atrás.
   - Si Google Play Protect avisa: **Más detalles → Instalar de todas formas**.
3. **O desde una compu con `adb`** (en la misma red Wi-Fi que la tele):
   ```
   adb connect IP_DE_LA_TELE:5555
   adb install -r Nuvio-AppleTV.apk
   adb install -r FreeMyTV.apk
   ```
   La tele pregunta "¿Permitir depuración por USB?": marcar "Permitir siempre" y aceptar. Si Google Play Protect avisa, **Más detalles → Instalar de todas formas**.

## Nuvio, la primera vez

1. Elegir **Avanzada** y cualquier diseño (la interfaz siempre es la estilo Apple TV).
2. Entrar con la cuenta de Nuvio propia y elegir el perfil.
3. **Configuración → TMDB → Clave de API de TMDB**: pegar una clave propia (gratis en themoviedb.org → Configuración → API). Sin ella no hay pósters, logos, descripciones ni "Para vos". Reiniciar la app después.
4. Opcional, para entrar con Simkl: **Configuración → TMDB → ID de cliente de Simkl** (se crea en simkl.com/settings/developer).

## Free My TV, la primera vez

1. Abrir **Free My TV → Ajustes de inicio → Clave de TMDB** y cargar la misma clave de TMDB (con el QR desde el celular, o escribiéndola).
2. La ciudad del clima sale sola de la zona horaria; se cambia en **Ajustes de inicio → Ciudad**.
3. **Free My TV → Home Screen → Free My TV** para que pase a ser el inicio. La tele pide permiso de depuración otra vez: aceptar.
   - Si aparece un aviso amarillo del Wi-Fi: la red se guardó durante la configuración inicial de la tele. Olvidar esa red en Configuración → Red e Internet y volver a conectarse, y probar de nuevo.
   - Para volver al inicio de siempre: **Home Screen → Original**.

Seguir viendo y Para vos del inicio salen del último perfil usado en Nuvio.

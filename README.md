# Stream Player Comunidad para Windows

Reproductor gratuito, sin vencimiento y con aportes voluntarios. No incluye canales, listas, películas, series ni suscripciones IPTV: conectá tus propias fuentes autorizadas.

## Descargar

- [Instalador oficial Comunidad 1.0.3](https://github.com/faqunditto-byte/stream-player-comunidad/releases/download/community-v1.0.3/Stream-Player-Comunidad-Setup-1.0.3.exe)
- [Archivos y notas de la versión](https://github.com/faqunditto-byte/stream-player-comunidad/releases/tag/community-v1.0.3)

Comunidad se instala aparte de IPTV Player y usa sus propios datos y cuentas. Si ya tenés Comunidad 1.0.0 o 1.0.1, instalá esta versión encima una vez, sin desinstalar, para activar el canal de actualizaciones. No reemplaza la edición paga ni necesita un código de activación.

## Actualizaciones

Desde 1.0.2 la app busca una versión nueva al abrirse. Si encuentra una, permite elegir si descargarla y abrir el instalador. Si no hay novedades o no hay conexión, sigue funcionando sin avisos. También se puede consultar desde Ajustes → Buscar actualizaciones.

El catálogo fijo es [community-updates.json](https://raw.githubusercontent.com/faqunditto-byte/stream-player-comunidad/refs/heads/main/community-updates.json). La app exige una firma RSA válida de Comunidad, comprueba tamaño y SHA-256 después de descargar y vuelve a verificar antes de ejecutar. No se instala automáticamente sin confirmación.

## Aportes voluntarios

[Apoyar el proyecto con PayPal](https://www.paypal.com/donate/?hosted_button_id=NAFPXB63KRUBL). Opciones sugeridas: USD 5, 10 y 20; PayPal también permite otros importes, incluso inferiores a USD 5. Los aportes son puntuales y opcionales; no desbloquean funciones ni crean una suscripción. La app sigue siendo gratuita aunque no aportes. PayPal muestra el nombre del titular al confirmar. No compartas tu contraseña ni códigos de seguridad con nadie.

## Integridad de la versión oficial

Desde 1.0.3, el control de integridad, el verificador de actualizaciones y la apertura de PayPal se distribuyen como módulos nativos de Windows, sin una copia Python de respaldo de esas partes. Esto dificulta extraerlas y modificarlas directamente; no impide crear otra app parecida, con o sin ayuda de una IA.

La app comprueba la firma del manifiesto y sus archivos al iniciar y vuelve a comprobar el ejecutable antes de abrir PayPal. Si detecta archivos modificados o incompletos, bloquea el inicio y pide reinstalar desde la fuente oficial.

Esto no hace imposible crear una copia modificada eliminando los controles. El instalador todavía no tiene firma Authenticode con un certificado reconocido por Windows: la firma propia no elimina avisos de SmartScreen ni identifica al editor para Windows.

En los archivos de la versión se incluyen el instalador, metadatos firmados y un verificador independiente. Para comprobar una descarga con el script, descargar `Verificar-Descarga-Comunidad.ps1` y `comunidad-release-signed.json` en la misma carpeta y ejecutar:

```powershell
./Verificar-Descarga-Comunidad.ps1 -Archivo ./Stream-Player-Comunidad-Setup-1.0.3.exe
```

Obtener siempre el script y sus metadatos desde este repositorio oficial. El verificador comprueba la firma propia y el SHA-256 y muestra aparte el estado de Authenticode.

Este repositorio distribuye solamente instaladores, documentación y comprobantes públicos. No contiene el código fuente de la app ni sus claves privadas. Los archivos automáticos «Source code» de GitHub contienen los archivos de este repositorio de distribución, no los fuentes de la aplicación. Los avisos y licencias de componentes externos están incluidos en el instalador.

Las cuentas IPTV y contraseñas permanecen en el dispositivo y no se publican ni se envían a GitHub. Las comprobaciones y descargas se realizan por HTTPS; las solicitudes a las fuentes IPTV se envían a los servidores elegidos por el usuario.

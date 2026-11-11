# Guía Conciliación - Academia AJ

PWA estática (sin servidor ni dependencias): `index.html` contiene toda la app,
`sw.js` es el service worker y `manifest.webmanifest` los datos de instalación.
Se publica en GitHub Pages (https://conciliacion.campusacademiaaj.com/) cada vez
que se fusiona algo en `main`. Más detalles en `LEEME.txt`.

## Instrucciones del propietario

- Responde siempre en castellano y con explicaciones sencillas, sin tecnicismos.
- Cuando termines un cambio y lo hayas probado, crea la pull request hacia `main`
  y **fusiónala tú** sin esperar a que te lo pida. Después confirma que se ha
  fusionado.
- Si las pruebas fallan o el cambio es dudoso, no fusiones: explica el problema
  y pregunta.
- Siempre que cambie el contenido de la app, sube la versión en `sw.js`
  (`conciliacion-aj-vN` → `vN+1`). La versión se muestra al pie del menú
  principal.
- No borres ni cambies el archivo `CNAME`.

## Pruebas

Sirve la carpeta con `python3 -m http.server` y abre `index.html` con Playwright
(Chromium ya instalado). Comprueba que no hay errores en la consola ni avisos de
la Content-Security-Policy, y que las calculadoras y el contador de descansos
siguen funcionando.

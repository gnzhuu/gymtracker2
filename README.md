# Gon — Gym Tracker v22

App móvil tipo PWA para registrar entrenamientos de fuerza con Google Sheets como base de datos central.

## Qué cambia en v22

- Google Sheets pasa a ser la fuente de verdad de datos.
- Al abrir/recargar/volver a la app, sincroniza automáticamente si hay internet.
- Si estás en medio de un ejercicio, el borrador se autoguarda y no se pisa al sincronizar.
- `Actualizar app` queda solo para actualizar código/cache.
- `Sincronizar ahora` y `Recargar datos de Sheets` actualizan datos.
- `Reset local y recargar` limpia la copia local del dispositivo y reconstruye desde Sheets.

## Qué subir a GitHub Pages

Sube a la raíz del repo:

- `index.html`
- `sw.js`
- `manifest.webmanifest`
- `icon.svg`

## Apps Script

Si ya tienes el backend v18 instalado, esta v22 no debería requerir cambiar la URL. Aun así, el ZIP incluye `appscript/Code.gs` actualizado.

Para actualizar Apps Script sin cambiar URL:

1. Pega `appscript/Code.gs` en Apps Script.
2. Guarda.
3. Implementar → Gestionar implementaciones.
4. Edita la Web App actual.
5. Versión: Nueva versión.
6. Implementar.

No uses “Nueva implementación” salvo que quieras una URL nueva.

# GymTracker v45 — Sync profesional con Sheets + Apps Script

Cambio principal frente a v44:
- Google Sheets sigue siendo la única base de datos autoritativa.
- El navegador solo conserva cola offline mínima.
- La sincronización ahora se hace con un endpoint atómico `syncBatch`.
- Apps Script usa `LockService` para evitar escrituras simultáneas.
- Las escrituras a Sheets se hacen por lotes cuando aplica.
- Se añade la hoja `BorradosDia` como registro de tombstones: si borras un día, entradas antiguas pendientes de otro dispositivo no pueden resucitarlo.
- El botón “Actualizar” primero sube cola pendiente y después recarga desde Sheets.
- Se añade cache-busting a las llamadas de API para evitar respuestas antiguas.

Archivos para GitHub Pages:
- `index.html`
- `sw.js`
- `manifest.webmanifest`
- `icon.svg`
- `icon-180.png`
- `icon-192.png`
- `icon-512.png`

Apps Script:
1. Copia `appscript/Code.gs` en tu proyecto de Apps Script.
2. Guarda.
3. Ejecuta `setup()` una vez.
4. Ve a **Implementar > Gestionar implementaciones**.
5. Edita la implementación actual.
6. Selecciona **Nueva versión**.
7. Implementa.

La primera ejecución creará/actualizará estas hojas:
- `Entrenamientos`
- `Ejercicios`
- `EntrenosDia`
- `BorradosDia`

# GymTracker v43 — Fix borrado en Sheets

Base: v42.

Corrige el problema de Histórico:
- El frontend ya NO da por borrado un día si Apps Script no confirma `deleteDay`.
- Si el backend viejo no borra en Sheets, el día queda oculto localmente y el borrado queda pendiente.
- `appscript/Code.gs` incluye `deleteDay` y responde con `deletedDate`, `deletedLogs`, `deletedDayNames`.

IMPORTANTE:
Esta vez no basta con GitHub Pages. Hay que actualizar Apps Script también.

GitHub Pages:
- index.html
- sw.js
- manifest.webmanifest
- icon.svg
- icon-180.png
- icon-192.png
- icon-512.png

Apps Script:
- Copiar appscript/Code.gs
- Guardar
- Implementar > Gestionar implementaciones > Editar la implementación actual
- Versión: Nueva versión
- Implementar

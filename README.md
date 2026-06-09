# GymTracker v44 — Sin base local, solo cola offline

Base: v43.

Cambio principal:
- Google Sheets es la única base de datos.
- Se elimina la copia local de histórico/ejercicios/nombres/borrador.
- El navegador solo guarda una cola offline mínima:
  - series pendientes
  - ejercicios pendientes
  - nombres de entrenamiento pendientes
  - borrados pendientes
- Al recuperar conexión:
  1. sube la cola a Apps Script/Sheets
  2. vacía lo subido
  3. recarga todo desde Sheets

IMPORTANTE:
Actualizar también Apps Script con appscript/Code.gs.

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
- Implementar > Gestionar implementaciones > Editar implementación actual
- Versión: Nueva versión
- Implementar

# Gym Tracker v47-json-days

Versión más rápida y estable para Google Sheets.

## Qué cambia

- Usa hojas nuevas limpias:
  - `GT_Dias_v47`
  - `GT_Ejercicios_v47`
  - `GT_Config_v47`
- El histórico ya no se guarda como una fila por serie.
- Ahora cada día se guarda como **una sola fila JSON** en `GT_Dias_v47`.
- Guardar un ejercicio actualiza la fila completa del día.
- Borrar un día marca esa fila como `deleted=true`, así no reaparece al actualizar.
- Offline mínimo: si no hay cobertura, se guarda en este dispositivo el día completo pendiente de subir.
- Al volver internet, la app sube pendientes y después carga Sheets.
- Apps Script usa `LockService` para evitar escrituras simultáneas.

## Instalación

1. Copia `appscript/Code.gs` en tu proyecto de Apps Script.
2. Ejecuta `setup()` una vez desde Apps Script.
3. Despliega una **nueva versión** del Web App.
4. Si cambia la URL del Web App, actualiza `API_URL` en `index.html`.
5. Sube `index.html`, `sw.js`, `manifest.webmanifest` e iconos a GitHub Pages.
6. En la app, ve a Ajustes → Actualizar app para limpiar caché.

## Importante

Esta versión empieza desde cero en hojas nuevas. Las hojas antiguas no se borran, pero tampoco se leen.

El modelo nuevo es:

```text
1 día = 1 fila en Sheets
```

Esto reduce llamadas, reduce filas y evita que un día borrado reaparezca por filas antiguas sueltas.

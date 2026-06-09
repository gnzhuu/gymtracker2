# Gym Tracker v46-clean-sheets

Versión simplificada para evitar errores de guardado/borrado.

## Qué cambia

- Usa hojas nuevas limpias en el mismo Spreadsheet:
  - `GT_Entrenamientos_v46`
  - `GT_Ejercicios_v46`
  - `GT_Dias_v46`
- Ignora las hojas antiguas que podían estar contaminadas por versiones anteriores.
- El navegador ya no guarda una cola offline de cambios.
- Guardar, borrar y renombrar se hacen directamente en Google Sheets.
- La pantalla solo cambia cuando Sheets confirma la operación.
- Apps Script usa `LockService` para que dos escrituras a la vez no pisen datos.

## Instalación

1. Copia `appscript/Code.gs` en tu proyecto de Apps Script.
2. Ejecuta `setup()` una vez desde Apps Script.
3. Despliega una nueva versión del Web App.
4. Sube `index.html`, `sw.js`, `manifest.webmanifest` e iconos a GitHub Pages.
5. En la app, ve a Ajustes → Actualizar app para limpiar caché.

## Importante

Esta versión empieza desde cero en hojas nuevas. Los datos viejos no se borran, pero tampoco se leen.
Si quieres migrar entrenos antiguos buenos, copia filas manualmente desde la hoja vieja a `GT_Entrenamientos_v46` respetando las cabeceras.

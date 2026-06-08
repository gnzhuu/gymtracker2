# Gym Tracker — GitHub Pages v9

App móvil para registrar entrenamientos de fuerza desde iPhone.

## Cómo se usa

- GitHub Pages sirve la app visual.
- Google Apps Script actúa como API privada.
- Google Sheets guarda los datos.
- La app puede guardar entrenamientos en local cuando no haya cobertura y sincronizar después.

## Qué subir a GitHub Pages

Sube estos archivos a la raíz del repositorio:

- `index.html`
- `manifest.webmanifest`
- `sw.js`
- `icon.svg`

No hace falta subir la carpeta `appscript` al repositorio público.

## Apps Script

1. Abre tu Google Sheet.
2. Ve a **Extensiones → Apps Script**.
3. Sustituye `Code.gs` por el archivo de `appscript/Code.gs`.
4. Ejecuta `setup()` una vez.
5. Despliega como Web App:
   - Ejecutar como: tú
   - Acceso: cualquiera con el enlace
6. Edita la implementación existente y crea una nueva versión cuando cambies el código.

## Contraseña/token

La contraseña de sincronización se define en `Code.gs` como `SECRET_TOKEN`.

La primera vez que abras la app, te pedirá esa contraseña en un popup. Se guarda localmente en el iPhone.

## iPhone

1. Abre la URL de GitHub Pages en Safari.
2. Pulsa compartir.
3. Elige **Añadir a pantalla de inicio**.
4. Abre la app desde el icono.

La primera carga necesita internet. Después la app queda cacheada y puede registrar entrenamientos aunque el gimnasio no tenga cobertura.


## Cambios v9

- Eliminada la capa superior semitransparente que aparecía al hacer scroll en iPhone.
- Rediseñados los controles de kg/reps para que cada número tenga más ancho y no se corte con dos o tres cifras.
- Kg y reps ahora se muestran apilados dentro de cada serie para mejorar ergonomía en móvil.


## v11

- Añadido botón **Actualizar app** en la pestaña Ejercicios/Offline.
- El service worker usa caché versionada `gym-tracker-v11`.
- La pantalla principal intenta cargar primero desde red y usa caché solo si no hay conexión.


## v11

- Se mantiene la barra inferior existente.
- Añadida pestaña Ajustes abajo.
- Botón visible: Ajustes → Actualizar app.
- No borra entrenamientos, ejercicios ni contraseña.

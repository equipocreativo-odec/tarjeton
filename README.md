# Consultas — Ejercicio Pedagógico ODEC

Incluye múltiples consultas y sus precandidatos conforme al anexo. Cada tarjeta muestra solo **Nombre + Primer Apellido**, pero envía a la hoja el **nombre de archivo**.

## Carpetas esperadas para imágenes
Coloque **fotos** y **logos** en estas rutas (por consulta):

- Fotos: `fotos/<id-consulta>/<NOMBRE COMPLETO>.png`
- Logos: `logos/<id-consulta>/<NOMBRE COMPLETO>-logo.png`

IDs de consulta:
- `frente-vida` → Frente por la Vida
- `gran-consulta` → La Gran Consulta por Colombia
- `soluciones` → Consulta de las Soluciones: Salud, Seguridad y Educación

> Los nombres completos de archivo se toman de `data/consultas.json`.

## Conexión con Google Sheets
1. Crea una hoja con encabezados: `timestamp`, `consulta`, `filename`.
2. Despliega tu Apps Script (Web App) que agregue filas con esos campos.
3. En `config.js`, pega la URL del Web App en `window.SHEETS_ENDPOINT`.

## Publicación
Sube todo a tu repo (root) y habilita GitHub Pages. Abre `index.html`.

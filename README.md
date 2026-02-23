# Consulta del Frente por la Vida — ODEC (Ejercicio Pedagógico)

Este paquete publica una **tarjeta de consulta** orientada al público, con diseño sobrio y profesional alineado a la imagen de ODEC.

## Contenido
- `index.html`: Tarjeta interactiva (solo **Nombre + Primer Apellido**). Usa el **nombre del archivo** para registrar el voto.
- `config.js`: Pega aquí la URL de tu **Google Apps Script (Web App)** en `window.SHEETS_ENDPOINT`.
- `X.png`: Marca de selección.
- `assets/odec-logo.svg`: Marcador de posición para el logo ODEC (reemplázalo por tu archivo oficial si lo tienes).

## Imágenes de candidatos
Coloca estas imágenes junto a `index.html` conservando **estos nombres exactos**:
- Daniel Quintero.png
- Edinson Torres.png
- Hector Pineda.png
- Roy Barreras.png
- Martha Bernal.png

## Conexión con Google Sheets
1. Crea una hoja con encabezados: `timestamp`, `filename`.
2. En Apps Script, despliega tu Web App que escriba en la hoja y copia la URL.
3. En `config.js`, asigna: `window.SHEETS_ENDPOINT = 'https://script.google.com/macros/s/TU_ID/exec'`.

## GitHub Pages
- Sube todo a tu repositorio.
- Activa **Settings → Pages → Deploy from a branch** (branch `main`, carpeta root).
- Abre `https://<usuario>.github.io/<repo>/`.

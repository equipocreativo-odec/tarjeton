INSTRUCCIONES PARA REGISTRAR VOTOS EN GOOGLE SHEETS

1) Crea una hoja en Google Sheets con encabezados en la primera fila: timestamp, filename
2) Abre https://script.google.com/ y crea un nuevo proyecto. Pega este código Apps Script:

function doPost(e){
  try {
    var payload = JSON.parse(e.postData.contents);
    var ss = SpreadsheetApp.openByUrl('PEGAR_URL_DE_TU_SHEET');
    var sh = ss.getSheets()[0];
    sh.appendRow([new Date(), payload.filename]);
    return ContentService.createTextOutput('ok').setMimeType(ContentService.MimeType.TEXT);
  } catch(err){
    return ContentService.createTextOutput('error: '+err).setMimeType(ContentService.MimeType.TEXT);
  }
}

3) En Apps Script, ve a "Deploy" > "New deployment" > Type: Web app
   - Description: Votos tarjetón
   - Execute as: Me (tu cuenta)
   - Who has access: Anyone with the link (o "Anyone")
   Copia la URL que te entrega el despliegue.

4) Abre el archivo config.js y pega esa URL en:
   window.SHEETS_ENDPOINT = 'TU_URL_AQUI';

5) Coloca tus imágenes originales en la MISMA carpeta que este HTML con estos nombres exactos:
   - Daniel Quintero.png
   - Edinson Torres.png
   - Hector Pineda.png
   - Roy Barreras.png
   - Martha Bernal.png

6) Abre tarjeton-consulta.html en tu navegador, elige una opción y haz clic en "Enviar voto". Verás los registros en tu Sheet.

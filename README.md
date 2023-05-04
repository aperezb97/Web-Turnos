# Web-Turnos
## Turnero para ingreso de camiones a planta

Este proyecto consiste en la creación de una página web utilizando servicios de Google, aprovechando su popularidad y facilidad de uso. Surgió como respuesta a la necesidad de organizar el ingreso de camiones a una planta de acopio, donde los conductores necesitan conocer su posición en la fila de espera en la playa de camiones para poder descargar su carga.

Anteriormente, el operario encargado de la descarga de camiones recibía constantes llamadas de los conductores para informarles sobre su ingreso a la planta. Con el objetivo de simplificar y agilizar este proceso, se desarrolló una página web responsive en la cual el operario puede registrar quién ingresa a la planta y en qué orden se encuentran. A su vez, los conductores que esperan en la playa de camiones pueden acceder a través de sus dispositivos móviles para conocer su posición en la fila de espera.

La idea principal fue brindar una solución sencilla y eficiente para el operario de descarga de camiones, quien necesitaba una herramienta similar a una hoja de cálculo en la que pudiera eliminar y modificar nombres de forma fácil. Para cumplir con este objetivo, se utilizó una página web con servicios de Google, aprovechando la integración con Google Sheets. De esta manera, se añadió una planilla de Google Sheets que permite al operario modificar de manera sencilla la fila de camiones, manteniendo así un proceso ágil y actualizado.

La utilización de los servicios de Google para desarrollar esta solución garantiza la familiaridad y comodidad de uso para los usuarios, además de proporcionar una plataforma segura y confiable.

En resumen, este proyecto consiste en la creación de una página web utilizando servicios de Google para organizar el ingreso de camiones a una planta de acopio. Proporciona una solución eficiente y sencilla para el operario de descarga, permitiendo el registro y seguimiento de la fila de camiones en tiempo real. Mediante la integración de una planilla de Google Sheets, se facilita la modificación y actualización de la fila de camiones de manera simple y rápida.


### Código que vincula la planilla de Google Sheets a la web.
```
function doGet() {

  var ss = SpreadsheetApp.getActiveSpreadsheet();
  var sheet = ss.getSheetByName("BD");
  var data = sheet.getDataRange().getDisplayValues();

  console.log(data);

  var template= HtmlService.createTemplateFromFile("index");
  template.data = data;
  var output = template.evaluate();
  return output;
}
```

### Planilla en la que el operario informa por nombre y estado quien debe ingresar a la planta

[![Screenshot-2023-05-04-155018.png](https://i.postimg.cc/kgJSLrc1/Screenshot-2023-05-04-155018.png)](https://postimg.cc/4m0nhSjV)

### WEB

[![screencapture-sites-google-view-hectorabertone-acopio-turnero-pagina-principal-2023-05-04-15-58-06.png](https://i.postimg.cc/vHd2gBY4/screencapture-sites-google-view-hectorabertone-acopio-turnero-pagina-principal-2023-05-04-15-58-06.png)](https://postimg.cc/8stmxTrG)

https://sites.google.com/view/hectorabertone-acopio-turnero/p%C3%A1gina-principal



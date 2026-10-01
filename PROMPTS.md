# Bitácora de Prompts - BASURA CERO
PROMT 1:
ROL: Sos un desarrollador senior de aplicaciones web móviles.
CONTEXTO: Estoy construyendo una app llamada BASURA CERO para vecinos y la unidad ambiental de la alcaldía.
El problema que resuelve es: Los días de recolección de basura cambian o no se avisan, provocando acumulación en la calle.
TAREA: Generá la primera versión funcional en un único archivo HTML/JS/CSS responsive, con estas tres funciones y nada más:
Registrar días y hora de paso del tren de aseo por zona.
Alerta o aviso visual claro el día anterior al paso del tren de aseo.
Formulario para reportar un punto con acumulación de basura fuera de horario (descripción, ubicación y foto ficticia o campo de texto).
RESTRICCIONES: En español, usando HTML5, CSS3 integrado y JavaScript puro (vanilla JS), sin librerías de pago, sin login, sin base de datos en servidor todavía. Que se vea bien en un celular. Código comentado en los puntos clave.
FORMATO DE SALIDA: El archivo index.html completo, y al final una lista de lo que NO hiciste y por qué.
CRITERIO DE ACEPTACIÓN: Abro la app, registro una zona con sus días de recolección y puedo crear un reporte de basura sin ningún error en la consola del navegador.

PROMT 2:
Ajustemos la app BASURA CERO con estas dos mejoras necesarias:
MEJORA M1 (Avisos): Asegúrate de que al seleccionar la fecha actual o al abrir la app, se verifique automáticamente si mañana pasa el tren de aseo en la zona elegida y se despliegue un aviso visual destacado en amarillo/naranja.
MEJORA M2 (Persistencia): Implementá localStorage para que los registros de zonas y los reportes comunitarios no se borren al recargar o cerrar la página. Si el localStorage está vacío, carga automáticamente datos de ejemplo (mockup) para que la app no empiece vacía.
Dame el código completo actualizado en un único archivo HTML/CSS/JS listo para reemplazar en index.html.

PROMT 3:
Ajustemos la app BASURA CERO con las siguientes mejoras de interfaz y seguridad:

1. MEJORA M3 (Diseño Celular + Estado Vacío):
   - Asegúrate de que la interfaz sea 100% responsive desde 320px de ancho y cómoda para usar con una sola mano en celular.
   - Si no hay reportes registrados en la lista, muestra un "Estado Vacío" amigable que diga: "No hay reportes de basura comunitarios. ¡Tu zona está limpia!" junto a un botón para crear el primer reporte.

2. MEJORA M4 (Validaciones y Control de Errores):
   - No permitas enviar el formulario de reporte si la ubicación o la descripción están vacías.
   - Limita el texto de la descripción a un máximo de 200 caracteres con un contador en tiempo real.
   - Desactiva el botón de guardar temporalmente mientras se procesa para evitar el doble clic.
   - Si hay un error, muéstralo en una caja de alerta roja accesible dentro de la pantalla, sin usar la función alert() nativa ni generar errores en la consola.

Entrégame el código completo actualizado en un solo archivo HTML/CSS/JS para reemplazar en index.html.

PROMT 4:
Integra la MEJORA M5 (Sello de IA con la API de Google Gemini gemini-2.5-flash) en la app BASURA CERO con estas especificaciones:

1. Cuando el usuario llene el formulario de reporte de basura, envía el texto de la ubicación y descripción a Gemini mediante un llamado fetch().
2. Pide a la API un JSON estructurado con este formato exacto:
{
  "prioridad": "Baja | Media | Alta | Crítica",
  "recomendacion": "Acción inmediata sugerida para la unidad ambiental de la alcaldía"
}
3. Renderiza en la tarjeta del reporte una etiqueta visual con el color según la prioridad (ej. Baja: verde, Media: amarillo, Alta: naranja, Crítica: rojo) y muestra la recomendación de la IA.
4. Si la API de Gemini falla o no hay API Key ingresada, la app debe clasificar el reporte como "Por clasificar (offline)" de forma elegante sin romper la interfaz.
5. Agrega un campo simple para que el usuario pueda ingresar su API Key de Gemini.

Entrégame el archivo index.html completo e integrado con todo lo anterior listo para producción.

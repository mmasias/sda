# Banco de tareas

Tareas de práctica para el seminario, ordenadas por sesión. Todas trabajan sobre la [carpeta de ejemplo](carpetaEjemplo/LEEME.md), material ficticio sin datos de personas reales, para que nadie tenga que buscar una carpeta propia "segura" antes de practicar. Una vez dominada cada tarea sobre el ejemplo, se repite sobre material propio, respetando la regla de datos de terceros.

## Criterios de diseño

1. **Solo texto plano** (`.md`, `.txt`, `.csv`). El agente los lee y escribe sin herramientas adicionales en un Windows recién instalado. Word, Excel y PDF exigen herramientas que el equipo no tiene y son la causa más probable de que una primera tarea falle.
2. **Resultado verificable sin conocimientos técnicos.** Cada tarea indica qué mirar para darla por buena. Revisar es el centro del seminario, no un paso final.
3. **Valor reconocible.** Tareas que un docente haría a mano: ordenar, renombrar, resumir, consolidar, personalizar.
4. **Bajo consumo de créditos.** Pensadas para Qwen3 Coder Next; ninguna debería superar una fracción pequeña de los 50 créditos mensuales.

## Índice

<div align=center>

|#|Sesión|Tarea|Carpeta|
|-|:-:|-|-|
|T01|1|Ordenar facturas por mes|`facturas/`|
|T02|1|Unificar nombres de archivo|`facturas/`|
|T03|1|Crear un índice de la carpeta|raíz|
|T04|2|Dar formato Markdown a unos apuntes|`apuntes/`|
|T05|2|Corregir ortografía y revisar los cambios|`apuntes/`|
|T06|3|Crear el archivo de contexto propio|raíz|
|T07|3|Generar actividades con y sin contexto|`apuntes/`|
|T08|4|Renombrado masivo: cuándo confiar|`facturas/`|
|T09|4|Pedir un borrado y no aceptarlo|`facturas/`|
|T10|5|Consolidar acuerdos y pendientes de varias actas|`actas/`|
|T11|5|Personalizar una comunicación por grupo|raíz|
|T12|5|Informe de calificaciones por grupo|raíz|
|T13|6|Exportar un documento a Word|cualquiera|

</div>

## Sesión 1: delegar y revisar

### T01. Ordenar facturas por mes

- **Petición:** "Organiza las facturas de la carpeta facturas en subcarpetas por mes, a partir de la fecha que aparece en el nombre de archivo. Las subcarpetas deben llamarse 2026-09, 2026-10 y así."
- **Qué revisar:** en el Explorador, que existan tres subcarpetas y que cada factura esté en la de su mes: septiembre 2, octubre 3, noviembre 3. Abrir dos facturas al azar y comprobar que la fecha del contenido coincide con la carpeta.
- **Fallo típico:** los nombres usan formatos de fecha distintos a propósito (`15-09-2026`, `20261002`, `oct-9-2026`, `4 nov 2026`). Si el agente ignora alguno, deja una factura sin mover o la coloca en otro mes. Es la mejor ocasión para mostrar por qué se revisa.

### T02. Unificar nombres de archivo

- **Petición:** "Renombra todas las facturas con el formato AAAA-MM-DD_proveedor.md, en minúsculas y con guiones en lugar de espacios."
- **Qué revisar:** que los 8 archivos sigan ahí (ni uno menos) y que todos sigan el formato. Ejemplo esperado: `2026-10-09_ferreteria-norte.md`.
- **Fallo típico:** confundir día y mes en `15-09-2026`, o perder un archivo al renombrar dos con el mismo nombre resultante.

### T03. Crear un índice de la carpeta

- **Petición:** "Crea un archivo indice.md con una lista de todos los archivos de esta carpeta y sus subcarpetas, con una línea que describa el contenido de cada uno."
- **Qué revisar:** que estén todos los archivos (son 15 en la carpeta original) y que las descripciones correspondan a lo que hay dentro. Abrir `indice.md` con el Bloc de notas.
- **Fallo típico:** descripciones inventadas a partir del nombre sin abrir el archivo. Se detecta comparando dos descripciones con el contenido real.

## Sesión 2: puntos de control

### T04. Dar formato Markdown a unos apuntes

- **Petición:** "Guarda un punto de control. Después, convierte apuntes/tema3-ecosistemas.txt en un archivo .md con títulos, listas y negritas para los términos clave, sin cambiar el contenido."
- **Qué revisar:** pedir "muéstrame qué cambió desde el último punto de control". El texto debe ser el mismo; solo cambian títulos, listas y marcas de formato.
- **Fallo típico:** el agente "mejora" el contenido (añade o reescribe frases) aunque se le pidió no cambiarlo. Las diferencias lo dejan a la vista, y es justo lo que se quiere enseñar.

### T05. Corregir ortografía y revisar los cambios

- **Petición:** "Corrige las tildes y faltas de ortografía de los apuntes, sin cambiar nada más. Luego guarda un punto de control."
- **Qué revisar:** los apuntes no llevan tildes y tienen al menos una falta (`aprobechada`). En las diferencias solo deben aparecer correcciones ortográficas. Después, pedir "vuelve al punto de control anterior" y comprobar que los errores reaparecen: el deshacer funciona.
- **Fallo típico:** corregir de más (cambiar palabras o la puntuación). Si ocurre, se deshace y se repite con una petición más estricta.

## Sesión 3: contexto persistente

### T06. Crear el archivo de contexto propio

- **Petición:** "Hazme preguntas para crear un archivo de contexto: quién soy, qué enseño, a qué nivel, cómo quiero que me escribas. Después guárdalo."
- **Qué revisar:** que el archivo recoja las respuestas dadas y nada inventado. Que al arrancar una conversación nueva el agente lo tenga en cuenta (preguntarle "¿qué sabes de mí?").
- **Fallo típico:** guardarlo en un sitio donde el agente no lo lee al arrancar. El mecanismo concreto de Kiro se detalla en la sesión 3.

### T07. Generar actividades con y sin contexto

- **Petición:** "A partir de los apuntes de ecosistemas, propón cinco actividades nuevas en un archivo actividades.md." Hacerlo una vez sin archivo de contexto y otra con él.
- **Qué revisar:** comparar los dos resultados. Con contexto, las actividades deben ajustarse al nivel y estilo declarados sin que haga falta repetirlos en la petición.
- **Fallo típico:** que no haya diferencia apreciable. Suele indicar que el contexto no se está cargando (volver a T06).

## Sesión 4: permisos y confianza gradual

### T08. Renombrado masivo: cuándo confiar

- **Petición:** la misma que T02, sobre una copia nueva de la carpeta.
- **Qué revisar:** el agente pide permiso para cada archivo. Tras aprobar dos o tres a mano y comprobar que lo hace bien, decidir si se usa `t` (confiar en esa acción para el resto de la sesión). La discusión importa más que el resultado: qué se gana y qué se arriesga al confiar.
- **Fallo típico:** confiar desde el primer archivo, sin haber visto ninguno.

### T09. Pedir un borrado y no aceptarlo

- **Petición:** "Borra las facturas de Copistería Rápida."
- **Qué revisar:** cuando el agente pida permiso para borrar, responder `n` y pedir en su lugar "muévelas a una carpeta llamada revisar". Comprobar que no se ha borrado nada.
- **Fallo típico:** aprobar por inercia. Esta tarea entrena justamente a leer qué se aprueba.

## Sesión 5: tareas multiarchivo

### T10. Consolidar acuerdos y pendientes de varias actas

- **Petición:** "Lee las tres actas y crea seguimiento.md con todos los acuerdos en orden cronológico y una tabla de pendientes con responsable y si siguen abiertos o se cerraron en una reunión posterior."
- **Qué revisar:** los pendientes se encadenan entre actas a propósito. Referencia: la propuesta de rúbrica (Docente B) se cierra en octubre y la incorporación de cambios, en noviembre; el presupuesto de diccionarios (Docente C) sigue abierto en octubre y se cierra en noviembre; el contacto con el museo (Docente A) se cierra en noviembre; las autorizaciones a las familias (Docente A) y la revisión de la rúbrica en enero (Coordinación) siguen abiertas; el envío del calendario a jefatura (Coordinación) no consta como cerrado en ninguna acta. Un buen resultado lo señala como dudoso en lugar de darlo por cerrado.
- **Fallo típico:** listar los pendientes de cada acta por separado sin detectar cuáles se cerraron después.

### T11. Personalizar una comunicación por grupo

- **Petición:** "Usa plantillaComunicacion.md para crear una comunicación por cada grupo que aparece en calificaciones.csv, en una carpeta comunicaciones, rellenando el campo del grupo."
- **Qué revisar:** que haya exactamente dos archivos (grupos A y B), que el campo esté relleno y que el resto del texto sea idéntico a la plantilla.
- **Fallo típico:** reescribir el texto de la plantilla, o crear un archivo por estudiante en vez de por grupo.

### T12. Informe de calificaciones por grupo

- **Petición:** "A partir de calificaciones.csv, crea informe.md con la nota media de cada grupo en cada trimestre, la media final (media de los tres trimestres) y cuántos estudiantes tienen media final inferior a 5."
- **Qué revisar:** comprobar a mano al menos un dato, por ejemplo con una calculadora. Valores de referencia:

<div align=center>

|Grupo|Trimestre 1|Trimestre 2|Trimestre 3|Media final|Media final < 5|
|:-:|:-:|:-:|:-:|:-:|:-:|
|A|5,50|5,97|6,20|5,89|4|
|B|7,32|6,64|6,87|6,94|1|

</div>

- **Fallo típico:** errores de cálculo. Un modelo de lenguaje puede equivocarse con la aritmética si calcula "de cabeza" en lugar de ejecutar un cálculo. Es la tarea que mejor muestra por qué ningún número del agente se da por bueno sin comprobarlo. Si falla, pedirle que haga el cálculo con PowerShell y repetir la comprobación.

## Sesión 6: salida a Office

### T13. Exportar un documento a Word

- **Petición:** "Convierte seguimiento.md en un documento de Word."
- **Qué revisar:** que el `.docx` se abra en Word y conserve títulos, listas y tablas.
- **Fallo típico:** el equipo no tiene herramienta de conversión. El agente puede proponer instalar Pandoc (`winget install --id JohnMacFarlane.Pandoc -e`); es una buena ocasión para decidir, con lo visto en la sesión 4, si se aprueba esa instalación. Tarea opcional.

## Tareas a evitar

- **Documentos de Word, hojas de Excel y PDF como entrada.** Su lectura depende de herramientas ausentes y el agente puede fallar o improvisar soluciones frágiles. Si hay que partir de ellos, convertirlos antes a texto.
- **PDF escaneados.** Son imágenes; no hay texto que leer.
- **Cualquier archivo con datos reales de estudiantes, familias o colegas** sin anonimizar, aunque sea material propio.
- **Tareas sin forma clara de comprobarlas** ("mejora este documento"). Si no se puede revisar, no se puede delegar.

## Estado de validación

Ninguna tarea se ha probado todavía en Kiro CLI sobre Windows 11. Antes de usarlas en una sesión, ejecutar cada una sobre una copia limpia de la carpeta de ejemplo con Qwen3 Coder Next y anotar aquí: resultado (correcto, parcial, fallido), créditos consumidos según `/usage` e incidencias.

<div align=center>

|#|Resultado|Créditos|Incidencias|
|-|-|-|-|
|T01|Sin validar|||
|T02|Sin validar|||
|T03|Sin validar|||
|T04|Sin validar|||
|T05|Sin validar|||
|T06|Sin validar|||
|T07|Sin validar|||
|T08|Sin validar|||
|T09|Sin validar|||
|T10|Sin validar|||
|T11|Sin validar|||
|T12|Sin validar|||
|T13|Sin validar|||

</div>

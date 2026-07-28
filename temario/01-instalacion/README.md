# 01. Instalación y primer contacto

## ¿Por qué?

La terminal es percibida como superficie hostil por quien nunca la ha usado: pantalla en negro, cursor parpadeante, ausencia de botones, asociación cultural con "hackear" o con errores irreversibles. Si la primera sesión de un curso de agentes empieza explicando sintaxis de comandos, la mayoría de los asistentes abandona antes de ver para qué sirve la herramienta. La barrera no es técnica: es de percepción de riesgo.

El obstáculo real no es aprender comandos sino cambiar un modelo mental. Quien ha usado un asistente conversacional espera hacer una pregunta y recibir una respuesta de texto que copia y pega donde haga falta. Un agente no funciona así: se le describe una tarea completa y es él quien decide los pasos, lee y escribe archivos reales, y entrega un resultado verificable. Pasar de "pedir una respuesta" a "delegar una tarea" es el único aprendizaje que importa en esta sesión; instalación y sintaxis son soporte para llegar ahí, no el contenido en sí.

Por eso la sesión empieza con una tarea real del propio docente (por ejemplo, reorganizar una copia de una carpeta de exámenes), no con un ejercicio de programación. Ver que el agente resuelve algo reconocible, algo que puede juzgarse sin conocimientos técnicos, es lo que neutraliza el miedo. Explicar el funcionamiento interno del agente en este punto sería prematuro: añadiría carga antes de que exista ninguna razón para quererla.

## ¿Qué?

La terminal es, a efectos de esta sesión, la ventana donde se escriben instrucciones en texto en vez de hacer clic, y donde vive el agente mientras trabaja. No hace falta memorizar comandos propios de la terminal (moverse entre carpetas, listar archivos): esas acciones se le piden al agente en lenguaje natural, y es él quien las traduce. La terminal es el sitio donde ocurre la conversación con el agente, no una asignatura previa que haya que aprobar antes de empezar.

<div align=center>

| |Asistente conversacional (chat)|Agente en terminal|
|-|-|-|
|Qué recibe|Una pregunta|Una tarea completa|
|Qué hace|Responde con texto|Decide los pasos, ejecuta, lee y escribe archivos reales|
|Qué hace el usuario con el resultado|Copia y pega donde haga falta|Revisa un resultado ya aplicado sobre sus propios archivos|
|Alcance de una interacción|Un turno de pregunta y respuesta|Una tarea de varios pasos resuelta de principio a fin|

</div>

Un agente, en un sentido de trabajo, es un programa que entiende una tarea descrita en lenguaje natural, puede leer y escribir archivos reales del ordenador donde se ejecuta, decide por sí mismo qué pasos dar y en qué orden, y muestra lo que ha hecho para que se pueda comprobar antes de darlo por bueno.

Desde esta primera sesión rigen dos reglas permanentes, no exclusivas de hoy:

1. **Se trabaja siempre sobre una copia**, nunca sobre el archivo original, hasta que la sesión 5 (control de versiones) aporte un mecanismo real de deshacer. Delegar una tarea por primera vez no debe depender de arriesgar el único ejemplar de un archivo.
2. **Antes de delegar cualquier tarea sobre un archivo, se comprueba si contiene datos personales de alumnos** (nombres, notas, cualquier dato identificable). Si los contiene, se trabaja sobre una versión anonimizada o con datos de prueba. Esta regla se establece aquí, no en el cierre del curso, porque la primera tarea de la sesión 1 ya puede tocar una carpeta de exámenes con datos reales.

## ¿Para qué?

Al cerrar la sesión, cada docente debe poder abrir la terminal sin percibirla como amenaza, describir en lenguaje natural una tarea real sobre sus propios archivos, y revisar lo que el agente hizo antes de darlo por bueno. No se espera que entiendan cómo funciona el agente por dentro ni que memoricen comandos. Se espera que hayan comprobado, sobre un caso propio, que delegar una tarea completa es distinto de usar un buscador o un chat, y que ese resultado es revisable y por tanto confiable bajo las condiciones correctas.

La tarea elegida para la práctica debe ser lo bastante simple para completarse dentro de la sesión y lo bastante real para que el docente reconozca el valor inmediato. Eso es lo que le permite, después, delegar una tarea parecida sin depender de nadie.

## ¿Cómo?

Herramienta: **Kiro CLI**. Entorno: **Windows 11**, shell **PowerShell** (dentro de Windows Terminal). Kiro CLI no soporta instalarse desde Command Prompt, y en Windows usa PowerShell por defecto para ejecutar comandos: no hay margen real para elegir cmd aquí.

### Preparación previa (antes de la sesión, no durante)

- Confirmar que el equipo corre **Windows 11**. Es un requisito de la herramienta, no una preferencia: en Windows 10 no hay instalación nativa soportada.
- Tener a mano una cuenta de Google (la mayoría ya tiene una) o, si se prefiere no usarla, estar dispuesto a crear una AWS Builder ID durante la sesión: es gratuita, sin tarjeta de crédito, solo pide correo, nombre y contraseña.
- Preparar sobre el escritorio una **copia** de la carpeta de examen que se va a usar en la práctica (copiar y pegar en el Explorador de archivos, renombrando la copia). El original no se toca en esta sesión.

### Instalación

1. Abrir el menú Inicio, escribir `Terminal` y abrir **Windows Terminal** (si no está disponible, `PowerShell` a secas sirve igual).
2. Ejecutar:
   ```
   irm 'https://cli.kiro.dev/install.ps1' | iex
   ```
3. Esperar a que termine. No hace falta entender el comando: descarga e instala Kiro CLI.

### Cuenta e inicio de sesión

1. Ejecutar `kiro-cli login`.
2. La terminal pide pulsar Intro para abrir el navegador.
3. En el navegador aparecen varias opciones de inicio de sesión. La recomendada para esta sesión es **Google**, porque no exige crear ninguna cuenta nueva. Alternativa: **Crear una AWS Builder ID** (correo, nombre, contraseña, código de verificación por correo), para quien prefiera no usar su Google.
4. Al terminar en el navegador, la propia página indica que ya se puede volver a la terminal. Ahí debe aparecer confirmación de sesión iniciada.

### Primer contacto

1. En el Explorador de archivos, entrar en la carpeta **copia** preparada de antemano.
2. Clic derecho sobre un espacio vacío de la carpeta y elegir **Abrir en Terminal**. Windows 11 abre Windows Terminal ya situado en esa carpeta: no hace falta moverse entre carpetas con comandos.
3. Ejecutar `kiro-cli` para arrancar el agente.
4. Describir la tarea en una frase, en lenguaje natural (por ejemplo: "organiza estos exámenes en subcarpetas por grupo, a partir del nombre de archivo").
5. Revisar en el propio Explorador el resultado antes de darlo por bueno. Esta revisión, no la ejecución del comando, es el punto central de la sesión.

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

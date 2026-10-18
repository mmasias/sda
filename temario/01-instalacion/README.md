# 01. Instalación y primer contacto

## ¿Por qué?

La terminal es percibida como superficie hostil por quien nunca la ha usado: pantalla en negro, cursor parpadeante, ausencia de botones, asociación cultural con "hackear" o con errores irreversibles. Si la primera sesión de un curso de agentes empieza explicando sintaxis de comandos, la mayoría de los asistentes abandona antes de ver para qué sirve la herramienta. La barrera no es técnica: es de percepción de riesgo.

El obstáculo real no es aprender comandos sino cambiar un modelo mental. Quien ha usado un asistente conversacional espera hacer una pregunta y recibir una respuesta de texto que copia y pega donde haga falta. Un agente no funciona así: se le describe una tarea completa y es él quien decide los pasos, lee y escribe archivos reales y entrega un resultado verificable. Pasar de "pedir una respuesta" a "delegar una tarea" es el único aprendizaje que importa en esta sesión; instalación y sintaxis son soporte para llegar ahí, no el contenido en sí.

Por eso la sesión empieza con una tarea real de quien participa (por ejemplo, reorganizar una copia de una carpeta de facturas), no con un ejercicio de programación. Ver que el agente resuelve algo reconocible, algo que puede juzgarse sin conocimientos técnicos, es lo que neutraliza el miedo. Explicar el funcionamiento interno del agente en este punto sería prematuro: añadiría carga antes de que exista ninguna razón para quererla.

## ¿Qué?

La terminal es, a efectos de esta sesión, la ventana donde se escriben instrucciones en texto en vez de hacer clic y donde vive el agente mientras trabaja. No hace falta memorizar comandos propios de la terminal (moverse entre carpetas, listar archivos): esas acciones se le piden al agente en lenguaje natural y es él quien las traduce. La terminal es el sitio donde ocurre la conversación con el agente, no una asignatura previa que haya que aprobar antes de empezar.

<div align=center>

| |Asistente conversacional (chat)|Agente en terminal|
|-|-|-|
|Qué recibe|Una pregunta|Una tarea completa|
|Qué hace|Responde con texto|Decide los pasos, ejecuta, lee y escribe archivos reales|
|Qué hace el usuario con el resultado|Copia y pega donde haga falta|Revisa un resultado ya aplicado sobre sus propios archivos|
|Alcance de una interacción|Un turno de pregunta y respuesta|Una tarea de varios pasos resuelta de principio a fin|

</div>

Un agente, en un sentido de trabajo, es un programa que entiende una tarea descrita en lenguaje natural, puede leer y escribir archivos reales del ordenador donde se ejecuta, decide por sí mismo qué pasos dar y en qué orden y muestra lo que ha hecho para que se pueda comprobar antes de darlo por bueno.

Desde esta primera sesión rigen dos reglas permanentes, no exclusivas de hoy:

1. **Se trabaja siempre sobre una copia**, nunca sobre el archivo original, hasta que la sesión 5 (control de versiones) aporte un mecanismo real de deshacer. Delegar una tarea por primera vez no debe depender de arriesgar el único ejemplar de un archivo.
2. **Antes de delegar cualquier tarea sobre un archivo, se comprueba si contiene datos personales de terceros** (nombres, identificadores, cualquier dato que permita reconocer a una persona). Si los contiene, se trabaja sobre una versión anonimizada o con datos de prueba. Esta regla se establece aquí, no en el cierre del curso, porque la primera tarea de la sesión 1 ya puede tocar archivos con datos reales de terceros.

## ¿Para qué?

Al cerrar la sesión, cada participante debe poder abrir la terminal sin percibirla como amenaza, describir en lenguaje natural una tarea real sobre sus propios archivos y revisar lo que el agente hizo antes de darlo por bueno. No se espera que entiendan cómo funciona el agente por dentro ni que memoricen comandos. Se espera que hayan comprobado, sobre un caso propio, que delegar una tarea completa es distinto de usar un buscador o un chat y que ese resultado es revisable y por tanto confiable bajo las condiciones correctas.

La tarea elegida para la práctica debe ser lo bastante simple para completarse dentro de la sesión y lo bastante real para que quien participa reconozca el valor inmediato. Eso es lo que le permite, después, delegar una tarea parecida sin depender de nadie.

## ¿Cómo?

Herramienta: **Kiro CLI**. Entorno: **Windows 11**, shell **PowerShell** (dentro de Windows Terminal). Kiro CLI no soporta instalarse desde Command Prompt y en Windows usa PowerShell por defecto para ejecutar comandos: no hay margen real para elegir cmd aquí.

Kiro se elige por fricción mínima: gratis sin tarjeta, login con la cuenta de Google, instalación de una línea. Su plan gratuito (50 créditos al mes) solo alcanza si se fija un modelo de bajo costo, **Qwen3 Coder Next**, en el primer arranque; el procedimiento lo incluye como paso único.

> [Alternativas](articulos/alternativas.md): comparativa de herramientas gratuitas, por qué Kiro y plan B si cambian sus condiciones.

> [Preparación previa](articulos/preparacionPrevia.md): qué comprobar y dejar listo antes de la sesión, para no gastar tiempo de contacto en soporte técnico.

> [Instalación y primer contacto: procedimiento](articulos/instalacionYPrimerContacto.md): instalación de Kiro CLI, creación de cuenta e inicio de sesión y la primera tarea delegada al agente.

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

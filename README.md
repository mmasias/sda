# Seminario de Agentes

Itinerario de 6 sesiones para introducir el uso de agentes de IA en terminal a personas sin formación informática, anclado en tareas reales del propio trabajo de quien participa (no ejercicios de programación).

## ¿Por qué?

Los agentes de IA ya permiten delegar tareas completas sobre los propios archivos (ordenar, renombrar, resumir, consolidar), no solo hacer preguntas y copiar respuestas. Pero su uso se percibe reservado a quien programa: viven en la terminal, una superficie que quien no es informático asocia a riesgo y error. El resultado es que quien más tareas repetitivas acumula en su trabajo es quien menos acceso tiene a la herramienta que podría aliviarlas.

La barrera no es técnica sino de percepción y de modelo mental: pasar de "pedir una respuesta" a "delegar una tarea y revisar el resultado". Ningún tutorial de instalación resuelve eso; hace falta un recorrido guiado sobre tareas reconocibles, con mecanismos de seguridad desde el primer día.

## ¿Qué?

Un seminario de 6 sesiones semanales que lleva a quien participa desde el primer contacto con la terminal hasta delegar con autonomía un proyecto propio. Lo sostienen tres decisiones de diseño:

1. **En terminal, no en una interfaz gráfica.** Existen agentes con interfaz que esconden la terminal. Se renuncia a ellos deliberadamente: el esfuerzo inicial es lo que da independencia. Quien participa ve y aprueba cada acción del agente, sin una interfaz que decida qué mostrar; lo aprendido se transfiere a cualquier agente de terminal, no queda atado a un producto.
2. **Markdown como formato de trabajo.** Los documentos que produce o modifica el agente se piden en `.md`, de forma transversal desde la sesión 1. Es texto plano: el agente lo maneja sin herramientas adicionales y cada cambio se puede ver línea a línea. Office pasa a ser formato de salida (exportar a `.docx` o `.pdf` cuando haya que entregar algo), no de trabajo.
3. **Control de versiones temprano, manejado por el agente.** Hasta que existe un mecanismo real de deshacer, se trabaja sobre copias y nadie trabaja sobre sus archivos de verdad. Por eso va en la sesión 2. Quien participa solo aprende a pedir "guarda un punto de control", "qué cambió desde el último punto" y "vuelve al último punto". Todo es local; publicar en GitHub queda como opcional.

## ¿Para qué?

Al terminar, cada participante debe poder:

- Abrir la terminal sin percibirla como amenaza y describir en lenguaje natural una tarea real de su trabajo.
- Revisar lo que hizo el agente antes de darlo por bueno y deshacerlo si no sirve, lo que convierte la delegación en algo confiable y no en un acto de fe.
- Darle al agente contexto persistente sobre su trabajo y otorgarle confianza de forma gradual, sabiendo qué aprueba.
- Seguir sin depender de quien facilitó el seminario ni de una herramienta concreta.

## ¿Cómo?

Cadencia semanal, 6 semanas. Instalación resuelta antes de la sesión 1 mediante guía enviada previamente, para dedicar el tiempo de contacto al primer uso, no al soporte técnico. Herramienta: Kiro CLI sobre Windows 11 (ver [alternativas](temario/01-instalacion/articulos/alternativas.md)).

1. [Instalación y primer contacto](temario/01-instalacion/README.md) (120 min)
2. Puntos de control: control de versiones manejado por el agente (90 min)
3. Contexto persistente (90 min)
4. Permisos y confianza gradual (90 min)
5. Tareas multiarchivo (90 min)
6. Cierre con proyecto propio (90 min)

Recursos:

- [Banco de tareas](recursos/bancoDeTareas.md): tareas de práctica por sesión, con qué revisar y fallos típicos.
- [Carpeta de ejemplo](recursos/carpetaEjemplo/LEEME.md): material ficticio, sin datos de personas reales, sobre el que se hacen las prácticas.

## Estado

En diseño. El itinerario detallado sesión por sesión está en discusión; el contenido de cada sesión se desarrollará a continuación.

# Instalación y primer contacto: procedimiento

Requiere haber resuelto antes la [preparación previa](preparacionPrevia.md). Las secciones de instalación, cuenta y configuración inicial se hacen una sola vez y, preferiblemente, antes de la sesión.

## Instalación

1. Abrir el menú Inicio, escribir `Terminal` y abrir **Windows Terminal** (si no está disponible, `PowerShell` a secas sirve igual).
2. Ejecutar:
   ```
   irm 'https://cli.kiro.dev/install.ps1' | iex
   ```
3. Esperar a que aparezca `Installed successfully`. No hace falta entender el comando: descarga e instala Kiro CLI. Si Windows pide permiso para que la aplicación haga cambios en el equipo, aceptar.
4. En la misma terminal, instalar también Git, que el agente usará a partir de la sesión 2 para guardar puntos de control:
   ```
   winget install --id Git.Git -e --source winget
   ```
   Si pregunta si se aceptan los términos del origen, responder `Y`. Si Windows pide permiso para hacer cambios en el equipo, aceptar.
5. **Cerrar la terminal y abrir una nueva.** La terminal en la que se instaló no reconoce todavía los comandos `kiro-cli` ni `git`; las que se abran a partir de ahora, sí. Es el tropiezo más frecuente de toda la instalación.

Si aparece `Installation failed`, casi siempre se debe a falta de permisos de administrador (equipos gestionados por la institución): pedir la instalación a soporte.

## Cuenta e inicio de sesión

1. Ejecutar `kiro-cli login`.
2. La terminal pide pulsar Intro para abrir el navegador.
3. En el navegador aparecen varias opciones de inicio de sesión. La recomendada es **Google**, porque no exige crear ninguna cuenta nueva. Alternativa: **Crear una AWS Builder ID** (correo, nombre, contraseña, código de verificación por correo), para quien prefiera no usar su Google.
4. Al terminar en el navegador, la propia página indica que ya se puede volver a la terminal. Ahí debe aparecer confirmación de sesión iniciada.

## Configuración inicial

El plan gratuito da 50 créditos al mes. Con el modelo por defecto se agotan en pocas tareas; con **Qwen3 Coder Next** rinden unas 20 veces más. Se fija una sola vez (detalle en [alternativas](alternativas.md)):

1. Ejecutar `kiro-cli` para arrancar el agente.
2. Escribir `/model` y pulsar Intro. Aparece una lista: moverse con las flechas hasta **Qwen3 Coder Next** y pulsar Intro.
3. Escribir `/model set-current-as-default` y pulsar Intro. Desde ahora, cada vez que se arranque el agente usará ese modelo.
4. Escribir `/usage` y pulsar Intro para ver los créditos disponibles. Conviene anotar la cifra: al terminar la primera tarea se vuelve a consultar y se ve cuánto ha costado.
5. Escribir `/quit` y pulsar Intro para salir.

## Primer contacto

1. En el Explorador de archivos, entrar en la carpeta **copia** preparada de antemano.
2. Clic derecho sobre un espacio vacío de la carpeta y elegir **Abrir en Terminal**. Windows 11 abre Windows Terminal ya situado en esa carpeta: no hace falta moverse entre carpetas con comandos.
3. Ejecutar `kiro-cli` para arrancar el agente.
4. Describir la tarea en una frase, en lenguaje natural y en español (por ejemplo: "organiza estas facturas en subcarpetas por mes, a partir del nombre de archivo"). Si la tarea produce un documento (un resumen, un listado, un informe), pedirlo en Markdown: "déjalo en un archivo `.md`".
5. Antes de crear, mover o modificar archivos, el agente **pide permiso** y muestra qué va a hacer. Leerlo y responder `y` (sí) o `n` (no). La opción `t` (confiar en esa acción para el resto de la sesión) no se usa todavía: otorgar confianza de forma gradual es el tema de la sesión 4. Si no se reconocen las opciones, pulsar Tab para verlas.
6. Revisar en el propio Explorador el resultado antes de darlo por bueno. Esta revisión, no la ejecución del comando, es el punto central de la sesión.
7. Consultar `/usage` y comparar con la cifra anotada.
8. Salir con `/quit`.

## Si el resultado no sirve

No hay nada que reparar: se trabaja sobre una copia. Borrar la carpeta copia, volver a copiarla desde el original y repetir la tarea con una instrucción más precisa (qué criterio usar, qué hacer con los archivos que no encajan). Reformular la petición es parte del aprendizaje, no un fracaso.

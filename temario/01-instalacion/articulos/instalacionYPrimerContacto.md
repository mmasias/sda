# Instalación y primer contacto: procedimiento

Requiere haber resuelto antes la [preparación previa](preparacionPrevia.md).

## Instalación

1. Abrir el menú Inicio, escribir `Terminal` y abrir **Windows Terminal** (si no está disponible, `PowerShell` a secas sirve igual).
2. Ejecutar:
   ```
   irm 'https://cli.kiro.dev/install.ps1' | iex
   ```
3. Esperar a que termine. No hace falta entender el comando: descarga e instala Kiro CLI.

## Cuenta e inicio de sesión

1. Ejecutar `kiro-cli login`.
2. La terminal pide pulsar Intro para abrir el navegador.
3. En el navegador aparecen varias opciones de inicio de sesión. La recomendada para esta sesión es **Google**, porque no exige crear ninguna cuenta nueva. Alternativa: **Crear una AWS Builder ID** (correo, nombre, contraseña, código de verificación por correo), para quien prefiera no usar su Google.
4. Al terminar en el navegador, la propia página indica que ya se puede volver a la terminal. Ahí debe aparecer confirmación de sesión iniciada.

## Primer contacto

1. En el Explorador de archivos, entrar en la carpeta **copia** preparada de antemano.
2. Clic derecho sobre un espacio vacío de la carpeta y elegir **Abrir en Terminal**. Windows 11 abre Windows Terminal ya situado en esa carpeta: no hace falta moverse entre carpetas con comandos.
3. Ejecutar `kiro-cli` para arrancar el agente.
4. Describir la tarea en una frase, en lenguaje natural (por ejemplo: "organiza estas facturas en subcarpetas por mes, a partir del nombre de archivo").
5. Revisar en el propio Explorador el resultado antes de darlo por bueno. Esta revisión, no la ejecución del comando, es el punto central de la sesión.

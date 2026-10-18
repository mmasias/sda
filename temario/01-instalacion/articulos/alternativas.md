# Alternativas a Kiro CLI

Verificado en octubre de 2026. Las condiciones de los planes gratuitos cambian varias veces al año: revisar esta página antes de cada edición del seminario.

## Criterios

El público no es informático: cada paso adicional de instalación o configuración es un punto de abandono. La herramienta se elige por fricción, no por potencia.

1. **Costo cero sin tarjeta de crédito.** Pedir una tarjeta, aunque no se cobre, frena a buena parte de quien participa.
2. **Inicio de sesión con una cuenta que ya se tiene** (Google), sin claves de API ni paneles de configuración.
3. **Instalación de una sola línea** en Windows 11, sin dependencias previas (Node.js, Python, Git).
4. **Cuota suficiente** para las 6 sesiones y la práctica entre sesiones, sin que se agote a mitad de una tarea.
5. **Condiciones estables y publicadas.** Una cuota que no se conoce no se puede planificar.

## Comparativa

<div align=center>

| |Gratis sin tarjeta|Login con cuenta existente|Instalación en una línea|Cuota suficiente|Condiciones publicadas|
|-|:-:|:-:|:-:|:-:|:-:|
|**Kiro CLI**|Sí|Sí (Google, GitHub)|Sí|Sí, con modelo de bajo costo|Sí|
|Antigravity CLI (Google)|Sí|Sí (Google)|Sí|Incierta|No: límites semanales sin cifras|
|Gemini CLI|No para cuentas personales|-|Requiere Node.js|-|-|
|Qwen Code|No|-|Requiere Node.js|-|-|
|OpenCode|Variable|No: exige elegir proveedor|Requiere configuración|Variable|No|
|GitHub Copilot CLI|Sí|Sí (GitHub)|No verificada|No: unas 50 solicitudes al mes|Sí|

</div>

- **Gemini CLI.** Fue la referencia gratuita hasta junio de 2026. Desde el 18 de junio de 2026 dejó de atender cuentas personales gratuitas; solo funciona con clave de API de pago o licencia empresarial. Google lo sustituye por Antigravity CLI.
- **Antigravity CLI** (comando `agy`). Gratis con cuenta personal de Google, instalación desde PowerShell. Pega: Google no publica cifras de la cuota gratuita, la ha cambiado varias veces en 2026 y hay reportes de bloqueo tras pocas peticiones. Es el plan B.
- **Qwen Code.** Su acceso gratuito con login terminó el 15 de abril de 2026; ahora exige plan de pago o clave de API.
- **OpenCode.** Programa libre, pero el modelo se contrata aparte. Sus modelos gratuitos (Zen) cambian sin aviso. Inviable para este público.
- **GitHub Copilot CLI.** El plan gratuito da para unas pocas tareas al mes: insuficiente para un seminario.

## Recomendación: Kiro CLI con modelo de bajo costo

Kiro mantiene un plan gratuito permanente de **50 créditos al mes**, sin tarjeta, con login de Google. Lo que se retiró en 2026 fue el bono de bienvenida, no el plan gratuito; de ahí la impresión extendida de que "ya no es gratis".

Con la configuración por defecto (modelo "Auto") los 50 créditos dan para pocas tareas. La clave está en el multiplicador de cada modelo:

<div align=center>

|Modelo|Multiplicador|Rendimiento de 50 créditos frente a Auto|
|-|:-:|:-:|
|Auto (por defecto)|1.0x|1x|
|Claude Sonnet|1.3x|0.8x|
|DeepSeek 3.2|0.25x|4x|
|MiniMax M2.1|0.15x|6-7x|
|**Qwen3 Coder Next**|**0.05x**|**20x**|

</div>

Con **Qwen3 Coder Next**, los 50 créditos rinden como 1.000 en Auto: margen holgado para tareas de organización de archivos, resúmenes y transformaciones de documentos. Por eso el procedimiento de la sesión 1 fija ese modelo como predeterminado en el primer arranque (`/model` y `/model set-current-as-default`) y enseña a consultar el saldo con `/usage`.

Reservas:

- Los modelos de pesos abiertos figuran como soporte "experimental" y tienen límites de uso no publicados. Si Qwen3 Coder Next desaparece o rinde mal en una tarea, el siguiente candidato es MiniMax M2.1 y después DeepSeek 3.2.
- Son menos capaces que Claude. Para las tareas del seminario bastan; para algo delicado puede cambiarse de modelo puntualmente, sabiendo que consume el saldo mucho más rápido.
- Kiro CLI requiere Windows 11 y PowerShell. En Windows 10 no hay instalación soportada; quien solo disponga de Windows 10 puede usar Antigravity CLI.
- El instalador escribe en `C:\Program Files`, por lo que necesita permisos de administrador. En equipos gestionados por la institución hay que pedir la instalación a soporte con antelación.

## Fuentes

- [Kiro: precios](https://kiro.dev/pricing/)
- [Kiro: modelos y multiplicadores](https://kiro.dev/docs/models/)
- [Kiro: requisitos de instalación](https://kiro.dev/docs/getting-started/installation/)
- [Kiro: comandos de barra](https://kiro.dev/docs/reference/slash-commands/)
- [Google: transición de Gemini CLI a Antigravity CLI](https://developers.googleblog.com/an-important-update-transitioning-gemini-cli-to-antigravity-cli/)
- [Layer3 Labs: precios de Antigravity](https://www.layer3labs.io/guides/google-antigravity-pricing)
- [DevOpsTales: comparativa de CLIs (Qwen Code)](https://devopstales.github.io/ai/ai-coding-cli-comparison/)
- [codeagentswarm: precios de OpenCode](https://www.codeagentswarm.com/en/guides/opencode-plans-and-pricing)
- [devtoolsreview: precios de GitHub Copilot](https://devtoolsreview.com/pricing/copilot-pricing/)

# GerontoLib — Guía en español

Ayuda de lectura gratuita y de código abierto para investigar el **envejecimiento y la longevidad**: letra grande, alto contraste, en español, inglés y francés, privada por diseño.
Un solo `index.html`, sin servidor ni cuenta. Los artículos llegan en vivo desde la API de [Europe PMC](https://europepmc.org).

## Cómo usarla
- **Lo más rápido:** descargue `index.html` y haga doble clic (buscar y la IA funcionan con Internet; instalarla como app no es posible de esta forma).
- **Como app instalable (computadora, Android, iPhone):** suba la carpeta a un alojamiento estático gratuito y abra la dirección.

### Publicarla gratis
**GitHub Pages:** cree un repositorio → suba todos los archivos → *Settings → Pages* → rama `main`, carpeta `/ (root)` → abra `https://<usuario>.github.io/<repositorio>/`.
**Netlify:** entre a `app.netlify.com/drop` y arrastre la carpeta completa.

### Instalar en el teléfono
- **iPhone/iPad:** abra la dirección en **Safari** → Compartir → **Añadir a pantalla de inicio**.
- **Android:** abra en **Chrome** → menú ⋮ → **Instalar app** / **Añadir a pantalla de inicio**.
- **Computadora (Chrome/Edge):** ícono de instalar en la barra de direcciones.

## Dónde se guarda la información (resumen)
- En el **`localStorage` del navegador**, en el aparato que usa. Claves: `gerontolib_v1` (notas, valoraciones, biblioteca, idioma, tamaño) y `gerontolib_ai_v1` (clave de Groq).
- **Cada aparato y cada dirección son independientes:** la versión en línea, el archivo descargado, el teléfono y la computadora **no comparten datos**. Para pasarlos: *Mis Notas → Respaldo completo* y *Restaurar respaldo*.
- Borrar los datos del navegador los elimina. **Haga respaldos.**
- Detalle completo (rutas en disco, qué sale a Internet): [PRIVACY.md](PRIVACY.md).

## Asistente de IA (opcional)
1. Cree una clave gratuita en <https://console.groq.com/keys>.
2. En la app: **Ayuda → Configurar el asistente de IA** → pegue la clave, marque la casilla y guarde.
3. Modelo por defecto: `openai/gpt-oss-120b`. Groq cambia su lista de modelos; si aparece un error de "modelo", edite el nombre.

La clave queda en su navegador, **nunca entra en los respaldos** y solo se envía a Groq. El plan gratuito tiene límites (aprox. 30 consultas por minuto y topes diarios según el modelo). **Nunca suba una clave a GitHub.** Las respuestas las genera una IA y pueden ser erróneas: verifique en los artículos.

## Traducción de títulos y resúmenes
- En cada artículo, botón **🌐 Traducir**: traduce al idioma de la pantalla y permite **Ver original** con un toque.
- **Con la clave de Groq** la calidad es mejor; además puede marcar "Traducir automáticamente los títulos de los resultados" en Ayuda.
- **Sin clave** se usa el servicio gratuito MyMemory (pide permiso la primera vez). Su cuota anónima es pequeña (unos 5.000 caracteres por día, es decir, pocos resúmenes). Si se agota, la app avisa.
- Siempre se indica "Traducción automática": puede tener errores.

## Comandos de voz
Toque **🎤 Voz** y diga una orden (en español, inglés o francés, sin importar el idioma de la pantalla):
- "Ir a biblioteca" · "Ir a mis notas" · "Ir a buscar" · "Ir a ayuda"
- "Buscar alzhéimer" · "Buscar telómeros y envejecimiento"
- "Ver en biblioteca senolíticos" (busca dentro de su biblioteca, también en títulos traducidos)
- "Letra grande" · "Letra extra grande" · "Letra normal"
- "Cambiar a inglés" · "Cambiar a francés" · "Cambiar a español"
- "Más resultados" · "Comandos" (muestra la lista)

Requisitos y límites: Chrome, Edge o Safari (no Firefox), micrófono autorizado e Internet; el audio lo procesa el proveedor del navegador (Google, Microsoft o Apple) y GerontoLib no lo guarda. Las órdenes de búsqueda se pasan a inglés si son palabras comunes. Probado solo con micrófono simulado, no en aparatos reales; en una app de iPhone instalada el reconocimiento de voz puede no estar disponible (use Safari).

## Documentos
- [PRIVACY.md](PRIVACY.md) — privacidad y almacenamiento
- [COMPLIANCE.md](COMPLIANCE.md) — autoevaluación de cumplimiento europeo
- [ORIGINALITY.md](ORIGINALITY.md) — qué tan original es
- [LICENSE](LICENSE) — MIT (reemplace `[YOUR NAME]`)

## Aviso
Herramienta informativa y educativa. No ofrece consejo médico, diagnóstico ni tratamiento.

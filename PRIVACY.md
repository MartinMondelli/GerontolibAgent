# GerontoLib — Privacy & data storage / Privacidad y almacenamiento de datos

*Español abajo · Version 2026-11-05*

## English

**GerontoLib has no server and no user accounts. The author of the software receives no data.**

### Exactly where your data is stored

Everything you create is saved in your browser's **`localStorage`**, on the device you are using, under two keys:

| Key | Contents | Included in "Full backup"? |
|---|---|---|
| `gerontolib_v1` | Language, text size, voice/translation permission flags, your ratings, your notes (with date), and a copy of the metadata (title, authors, journal, year, link, abstract excerpt) of every article you rated or annotated | **Yes** |
| `gerontolib_ai_v1` | Your Groq API key, chosen model, and your consent checkbox | **No — never** |
| `gerontolib_tr_v1` | Cache of translated titles/abstracts (max. 200) — a convenience copy | **No** |

The AI conversation is held **in memory only** and disappears when you close or reload the page.

Where the browser keeps `localStorage` on disk (internal folders — not meant to be opened by hand):

- **Chrome (Windows):** `%LOCALAPPDATA%\Google\Chrome\User Data\<Profile>\Local Storage\leveldb`
- **Chrome (macOS):** `~/Library/Application Support/Google/Chrome/<Profile>/Local Storage/leveldb`
- **Firefox:** `<profile folder>\storage\default\<site>\ls\data.sqlite`
- **Safari, iPhone/iPad, Android:** inside the app's protected storage; not reachable by the user.

To see the values: browser developer tools → *Application* (Chrome/Edge) or *Storage* (Firefox) → *Local Storage*.

**Important consequences**

- Data is tied to **browser + device + site address**. The online version, a downloaded `index.html`, your phone and your computer are **separate stores that do not sync**. Use *Full backup* / *Restore backup* to move data.
- Clearing site data, using private/incognito windows, or (on Safari) not visiting a website for about a week can erase it. Installing the app to the Home Screen helps on iOS. **Make backups regularly.**
- The key is stored **unencrypted** in `localStorage`. Anyone with access to your unlocked device/browser profile could read it. Use a free Groq key you can revoke at any time; never use a key with billing attached on a shared computer.
- The app's service worker caches only the app's own files (HTML, icons), never searches or AI traffic.

### What leaves your device

| Recipient | When | What is sent |
|---|---|---|
| **Europe PMC (EMBL-EBI)** | Every search | The search terms and, as with any web request, your IP address |
| **Groq** (only if you enable the AI assistant) | Every question; "Explain with AI"; "Translate" | Your question and recent messages of the conversation; for "Explain with AI": the article's title, journal, year and abstract excerpt; for "Translate": the title and abstract (and, if automatic title translation is on, the titles of the results); your API key as authorization |
| **MyMemory (Translated, Italy)** | Only if you press "Translate" **without** the AI assistant, after a permission prompt | The title/abstract text (up to 1,500 characters) and your IP address |
| **Your browser's speech service** (Google in Chrome, Microsoft in Edge, Apple in Safari) | Only when you press 🎤, after a permission prompt | The audio of your voice command, processed by the browser vendor under its own privacy policy. GerontoLib does not receive or store it |
| **Your hosting provider** (GitHub Pages, Netlify…) | When the page loads | Standard server logs (IP address, browser) handled by that provider |

Your notes, ratings and library are **never** sent anywhere. Translation only sends the public title/abstract of the article, never your notes.

The software contains no analytics, no advertising, no tracking, no cookies and no third-party scripts or fonts.

### Your rights

Because the author holds no data, access/erasure requests are met by you directly: export or delete your data in the app (delete a note, "Delete my key") or clear the site's data in your browser. For data held by Europe PMC, Groq or your host, see their privacy policies.

---

## Español

**GerontoLib no tiene servidor ni cuentas de usuario. El autor del programa no recibe ningún dato.**

### Dónde se guarda exactamente la información

Todo lo que usted crea se guarda en el **`localStorage` de su navegador**, en el aparato que está usando, bajo dos claves:

| Clave | Contenido | ¿Entra en el "Respaldo completo"? |
|---|---|---|
| `gerontolib_v1` | Idioma, tamaño de letra, permisos de voz/traducción, valoraciones, notas (con fecha) y copia de los datos (título, autores, revista, año, enlace, extracto del resumen) de cada artículo valorado o anotado | **Sí** |
| `gerontolib_ai_v1` | Su clave de Groq, el modelo elegido y su casilla de aceptación | **No, nunca** |
| `gerontolib_tr_v1` | Caché de títulos/resúmenes traducidos (máx. 200), una copia de comodidad | **No** |

La conversación con la IA vive **solo en la memoria** y desaparece al cerrar o recargar la página.

Dónde guarda el navegador el `localStorage` en el disco (carpetas internas, no pensadas para abrirse a mano):

- **Chrome (Windows):** `%LOCALAPPDATA%\Google\Chrome\User Data\<Perfil>\Local Storage\leveldb`
- **Chrome (macOS):** `~/Library/Application Support/Google/Chrome/<Perfil>/Local Storage/leveldb`
- **Firefox:** `<carpeta del perfil>\storage\default\<sitio>\ls\data.sqlite`
- **Safari, iPhone/iPad, Android:** dentro del almacenamiento protegido de la aplicación; no accesible para el usuario.

Para verlos: herramientas de desarrollo del navegador → *Aplicación* (Chrome/Edge) o *Almacenamiento* (Firefox) → *Local Storage*.

**Consecuencias importantes**

- Los datos están ligados a **navegador + aparato + dirección del sitio**. La versión en línea, un `index.html` descargado, el teléfono y la computadora son **almacenes separados que no se sincronizan**. Para pasar datos de uno a otro use *Respaldo completo* / *Restaurar respaldo*.
- Borrar los datos del sitio, usar ventanas privadas o (en Safari) no visitar el sitio durante aproximadamente una semana puede borrarlos. Instalar la app en la pantalla de inicio ayuda en iPhone. **Haga respaldos con regularidad.**
- La clave se guarda **sin cifrar** en `localStorage`. Quien acceda a su aparato desbloqueado o a su perfil del navegador podría leerla. Use una clave gratuita de Groq que pueda revocar cuando quiera; no use una clave con facturación en una computadora compartida.
- El service worker guarda en caché solo los archivos de la propia app (HTML, íconos), nunca búsquedas ni tráfico de IA.

### Qué sale de su aparato

| Destinatario | Cuándo | Qué se envía |
|---|---|---|
| **Europe PMC (EMBL-EBI)** | En cada búsqueda | Los términos de búsqueda y, como en cualquier petición web, su dirección IP |
| **Groq** (solo si activa el asistente de IA) | En cada pregunta; "Explicar con IA"; "Traducir" | Su pregunta y los últimos mensajes de la conversación; en "Explicar con IA": título, revista, año y extracto del resumen del artículo; en "Traducir": el título y resumen (y, si la traducción automática de títulos está activa, los títulos de los resultados); su clave como autorización |
| **MyMemory (Translated, Italia)** | Solo si pulsa "Traducir" **sin** el asistente de IA, tras un aviso de permiso | El texto del título/resumen (hasta 1.500 caracteres) y su dirección IP |
| **Servicio de voz de su navegador** (Google en Chrome, Microsoft en Edge, Apple en Safari) | Solo al pulsar 🎤, tras un aviso de permiso | El audio de su orden, procesado por el proveedor del navegador según su propia política. GerontoLib no lo recibe ni lo guarda |
| **Su proveedor de alojamiento** (GitHub Pages, Netlify…) | Al cargar la página | Registros habituales del servidor (IP, navegador), gestionados por ese proveedor |

Sus notas, valoraciones y biblioteca **nunca** se envían a ningún sitio. La traducción solo envía el título/resumen público del artículo, nunca sus notas.

El programa no incluye analítica, publicidad, rastreo, cookies ni scripts o tipografías de terceros.

### Sus derechos

Como el autor no conserva datos, usted ejerce el acceso y la supresión directamente: exporte o borre sus datos en la app (borrar una nota, "Borrar mi clave") o limpie los datos del sitio en su navegador. Para los datos que conserven Europe PMC, Groq o su proveedor de alojamiento, consulte sus políticas de privacidad.

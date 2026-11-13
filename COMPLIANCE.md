# EU compliance notes / Notas de cumplimiento europeo

*Español abajo · Reviewed 2026-11-05 · **This is a self-assessment, not legal advice.** No software can honestly be declared "100% compliant" with all European law; compliance depends on how *you* publish and operate it. Have a lawyer review it before any commercial use, and re-check dates: EU digital rules are still being adjusted (e.g. the "Digital Omnibus").*

## English

| Area | Assessment | What the project does / what you must do |
|---|---|---|
| **GDPR (Reg. 2016/679)** | Low exposure by design | No server, no accounts, no analytics. User data stays in the user's own browser (see `PRIVACY.md`). The only personal data in transit are IP addresses seen by Europe PMC, the host and (optionally) Groq. **You:** keep `PRIVACY.md` published; do not add trackers; never put real personal data (names, health data, API keys) in the repo. |
| **Transfers outside the EU (GDPR ch. V)** | Needs checking, **only if the AI assistant is used** | Questions go to Groq, a US company. The AI feature is **opt-in**: off by default, user supplies their own key and ticks an explicit consent box that names Groq. **You:** read Groq's current privacy policy / DPA and transfer mechanism before recommending the feature to others; keep the opt-in. |
| **Voice commands (browser speech services)** | Disclosed; opt-in | Speech recognition is done by the browser vendor (Google/Microsoft/Apple), not by this project, which never receives the audio. Voice can be personal data, and the vendor is responsible for that processing. The app asks permission before first use and names the providers. Not available in Firefox. **You:** keep the prompt and the disclosure in `PRIVACY.md`; adding your own audio recording or server-side speech processing would need a new assessment. |
| **Translation (Groq / MyMemory)** | Low risk, disclosed | Only public article titles/abstracts are sent (never notes or personal data), plus the IP address as with any request. MyMemory is run by Translated (Italy, EU); Groq is covered in the row above. Translations are labelled as machine translations and the original is one tap away. **You:** keep the label; do not present translations as authoritative. |
| **ePrivacy Art. 5(3) ("cookie law")** | No consent banner needed in principle | Only `localStorage` for functions the user explicitly requests (saving their notes, language, key). No tracking or advertising storage. **You:** do not add non-essential storage. |
| **EU AI Act, Art. 50 (transparency; applies since 2 Aug 2026)** | Addressed | The assistant is clearly labelled as AI in every language ("🤖 Asistente IA", a notice above the chat), and the footer says answers are AI-generated. Sources checked state Art. 50 transparency duties for AI that interacts with people apply from 2 Aug 2026. Obligations for the underlying general-purpose model sit with its provider (Groq/model developer). **You:** keep the labels; if you offer it as a hosted service to others, re-assess whether you count as "provider" or "deployer". |
| **Medical device rules (MDR 2017/745)** | Out of scope *as positioned* | Positioned as an educational reading aid, not for diagnosis, prevention, monitoring or treatment of disease. The AI system prompt forbids personal medical advice/dosing and every language carries a disclaimer. **You:** do not market it with clinical claims ("diagnose", "treat", "recommend therapy"); that could change its legal category. |
| **Europe PMC content & copyright** | OK with care | Europe PMC says its API is free, usable commercially, keyless, and that article content belongs to its publishers/authors. The app shows metadata + an abstract excerpt (max 2,500 characters, collapsed by default) and **links to the official page**; it does not copy full texts. Not all content is reusable; full-text licences vary per article. **You:** keep the attribution to Europe PMC; do not bulk-download or mirror content; respect rate limits (per IP). |
| **Accessibility (European Accessibility Act, WCAG)** | Designed for it, **not audited** | Large targets, high contrast, 3 text sizes, labels, `aria-pressed`/`aria-live`, keyboard focus outlines, `lang` switching. The EAA mainly covers specified commercial products/services, so a free personal open-source tool is probably outside it — but it is good practice. **You:** before claiming "WCAG 2.1 AA", test with a screen reader (VoiceOver/NVDA), keyboard only, and the axe or Lighthouse tools. |
| **Open-source licence** | OK | MIT. No third-party libraries or fonts are bundled, so there are no inherited licence obligations. Replace `[YOUR NAME]` in `LICENSE`. |
| **Name / trademarks** | Unchecked | Search EUIPO TMview and the web for "GerontoLib" before building a brand. Groq, Europe PMC, PubMed, GitHub, LinkedIn are trademarks of their owners; use them descriptively only. |

### Before you publish — checklist
- [ ] Replace `[YOUR NAME]` in `LICENSE`.
- [ ] Remove any personal details from the repo (no names of family members, no real notes, no API keys).
- [ ] Keep the disclaimer and the AI labels in the UI.
- [ ] Verify the Groq model name still exists (they change) and that Groq's terms permit your use.
- [ ] Run an accessibility test (screen reader + Lighthouse).
- [ ] Re-read this table in 6 months.

## Español

*Autoevaluación, **no es asesoramiento jurídico**. Ningún software puede declararse honestamente "100 % conforme" con toda la normativa europea: depende de cómo usted lo publique y opere. Pida revisión a un abogado antes de cualquier uso comercial y vuelva a verificar las fechas: las normas digitales de la UE se siguen ajustando (p. ej. el "Digital Omnibus").*

| Área | Evaluación | Qué hace el proyecto / qué debe hacer usted |
|---|---|---|
| **RGPD** | Exposición baja por diseño | Sin servidor, sin cuentas, sin analítica. Los datos del usuario quedan en su propio navegador (ver `PRIVACY.md`). Los únicos datos personales en tránsito son las IP que ven Europe PMC, el alojamiento y (opcionalmente) Groq. **Usted:** mantenga publicado `PRIVACY.md`; no añada rastreadores; no suba al repositorio datos personales reales (nombres, datos de salud, claves). |
| **Transferencias fuera de la UE** | A comprobar, **solo si se usa la IA** | Las preguntas van a Groq, empresa estadounidense. La función es **opcional**: apagada por defecto, con clave propia del usuario y casilla de consentimiento que nombra a Groq. **Usted:** lea la política de privacidad y el DPA vigentes de Groq antes de recomendar la función a terceros; mantenga el consentimiento previo. |
| **Comandos de voz (servicios de voz del navegador)** | Informado; opcional | El reconocimiento lo hace el proveedor del navegador (Google/Microsoft/Apple), no este proyecto, que nunca recibe el audio. La voz puede ser dato personal y el proveedor es responsable de ese tratamiento. La app pide permiso antes del primer uso y nombra a los proveedores. No disponible en Firefox. **Usted:** mantenga el aviso y la información en `PRIVACY.md`; grabar audio por su cuenta o procesar voz en un servidor exigiría una nueva evaluación. |
| **Traducción (Groq / MyMemory)** | Riesgo bajo, informado | Solo se envían títulos/resúmenes públicos de artículos (nunca notas ni datos personales), más la IP como en cualquier petición. MyMemory la opera Translated (Italia, UE); Groq se trata en la fila anterior. Las traducciones se etiquetan como automáticas y el original está a un toque. **Usted:** mantenga la etiqueta; no las presente como texto autorizado. |
| **ePrivacy art. 5(3)** | En principio no hace falta banner | Solo `localStorage` para funciones que el usuario pide (notas, idioma, clave). Nada de rastreo ni publicidad. **Usted:** no añada almacenamiento no esencial. |
| **Reglamento de IA (art. 50, desde el 2-ago-2026)** | Atendido | El asistente se identifica como IA en los tres idiomas (aviso sobre el chat, etiqueta "🤖 Asistente IA", pie de página). Las fuentes consultadas indican que los deberes de transparencia del art. 50 para IA que interactúa con personas rigen desde el 2 de agosto de 2026. Las obligaciones del modelo de IA de propósito general corresponden a su proveedor. **Usted:** conserve las etiquetas; si lo ofrece como servicio alojado a terceros, reevalúe si es "proveedor" o "responsable del despliegue". |
| **Productos sanitarios (MDR 2017/745)** | Fuera de alcance *según su posicionamiento* | Es una ayuda educativa de lectura, no sirve para diagnosticar, prevenir, monitorizar ni tratar enfermedades. El prompt de la IA prohíbe consejo médico personal y posologías, y hay avisos en cada idioma. **Usted:** no lo promocione con afirmaciones clínicas ("diagnostica", "trata"); podría cambiar su categoría legal. |
| **Contenido y derechos de Europe PMC** | Correcto con cuidado | Europe PMC indica que su API es gratuita, de uso comercial permitido y sin clave, y que el contenido pertenece a editoriales/autores. La app muestra metadatos + extracto del resumen (máx. 2.500 caracteres, plegado) y **enlaza a la página oficial**; no copia textos completos. No todo el contenido es reutilizable. **Usted:** mantenga la atribución a Europe PMC; no descargue en masa ni replique contenido; respete los límites por IP. |
| **Accesibilidad (Acta Europea de Accesibilidad, WCAG)** | Diseñada para ello, **sin auditar** | Botones grandes, alto contraste, 3 tamaños de letra, etiquetas, `aria-pressed`/`aria-live`, foco visible, cambio de `lang`. El Acta cubre sobre todo productos/servicios comerciales concretos, así que una herramienta personal gratuita probablemente queda fuera, pero es buena práctica. **Usted:** antes de decir "WCAG 2.1 AA", pruebe con lector de pantalla (VoiceOver/NVDA), solo teclado y Lighthouse/axe. |
| **Licencia** | Correcta | MIT. No hay librerías ni tipografías de terceros. Reemplace `[YOUR NAME]` en `LICENSE`. |
| **Nombre / marcas** | Sin comprobar | Busque "GerontoLib" en EUIPO TMview y en la web antes de crear una marca. Groq, Europe PMC, PubMed, GitHub y LinkedIn son marcas de sus dueños; úselas solo de forma descriptiva. |

### Lista previa a publicar
- [ ] Reemplazar `[YOUR NAME]` en `LICENSE`.
- [ ] Quitar datos personales del repositorio (sin nombres de familiares, sin notas reales, sin claves).
- [ ] Mantener el aviso y las etiquetas de IA en la interfaz.
- [ ] Verificar que el modelo de Groq sigue existiendo y que sus términos permiten su uso.
- [ ] Hacer una prueba de accesibilidad (lector de pantalla + Lighthouse).
- [ ] Releer esta tabla en 6 meses.

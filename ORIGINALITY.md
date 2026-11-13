# How original is GerontoLib? / ¿Qué tan original es?

*Español abajo · Based on web searches on 2026-11-05. Limited searches cannot prove that nothing identical exists.*

## English

**Short answer:** each *ingredient* already exists; the *combination and the audience* are the distinctive part. Do not present it as "the first" or "unique" — present it as a **focused, accessible, privacy-friendly take**.

### What already exists (found while researching)
- **Europe PMC / PubMed** — the literature search itself. GerontoLib is a front-end for the Europe PMC API, as are many other tools (e.g. the rOpenSci `europepmc` R client).
- **Aging/longevity AI research tools** — *Longevity Genie* (open-source RAG tools for aging biology), *Aubrey* (geroscience research copilot, Georgia Longevity Alliance), *Aubrai* (longevity research engine with citations and a public API), *LongevityLLM* (a preprint describing an agent that also uses Europe PMC), and various "longevity copilot" chatbots.
- **General reference managers and note-taking apps** (Zotero and similar) — libraries, ratings, notes.
- **"Bring your own key" LLM front-ends** — a common pattern.

### What is different here
| Aspect | GerontoLib |
|---|---|
| Target user | An older, non-technical physician-scientist: huge buttons, 3 text sizes, high contrast, plain-language everything. The tools above target researchers/developers. |
| Zero infrastructure | One HTML file; works by double-click, USB stick, or as an installable app on a free static host. No backend, no account, no database. |
| Privacy model | Notes and library never leave the device; AI is opt-in with the user's own key kept out of backups. |
| Trilingual UI (ES/EN/FR) | Live switching; Spanish/French search words mapped to English MeSH-style terms. |
| Whole workflow in one place | Search → read → rate → annotate → export notes → ask the AI about *this* article. |

### Honest limits
- The search quality is only as good as Europe PMC's; there is no semantic search or citation checking (the AI can still be wrong).
- No sync between devices (backup/restore by file).
- Not peer-reviewed or clinically validated; it is a reading aid.

### How to describe it publicly
> "A free, open-source, single-file reading aid for aging research, built for an older physician-scientist: large-print, trilingual, private by design, powered by Europe PMC, with an optional AI explainer."

Avoid: "first", "revolutionary", "medical AI", "100% compliant", "replaces your doctor". Credit Europe PMC and Groq, and say it was built with AI assistance if true (a good practice and consistent with EU transparency norms).

## Español

**Respuesta corta:** cada *ingrediente* ya existe; lo distintivo es la *combinación y el público*. No lo presente como "el primero" ni "único": preséntelo como una **propuesta enfocada, accesible y respetuosa con la privacidad**.

### Lo que ya existe (encontrado en la investigación)
- **Europe PMC / PubMed** — la búsqueda bibliográfica en sí. GerontoLib es un front-end de la API de Europe PMC, como muchas otras herramientas (p. ej. el cliente `europepmc` de rOpenSci para R).
- **Herramientas de IA para investigación del envejecimiento** — *Longevity Genie* (herramientas RAG de código abierto), *Aubrey* (copiloto de gerociencia), *Aubrai* (motor de investigación con citas y API pública), *LongevityLLM* (preprint de un agente que también usa Europe PMC) y varios chatbots "longevity copilot".
- **Gestores de referencias y notas** (Zotero y similares) — bibliotecas, valoraciones, notas.
- **Interfaces de LLM con clave propia** — un patrón muy común.

### Qué es distinto aquí
| Aspecto | GerontoLib |
|---|---|
| Usuario objetivo | Una médica-científica mayor, no técnica: botones enormes, 3 tamaños de letra, alto contraste, todo en lenguaje claro. Las otras herramientas apuntan a investigadores/desarrolladores. |
| Infraestructura cero | Un solo archivo HTML; funciona con doble clic, pendrive o como app instalable en alojamiento estático gratuito. Sin backend, cuenta ni base de datos. |
| Modelo de privacidad | Notas y biblioteca nunca salen del aparato; la IA es opcional con clave propia fuera de los respaldos. |
| Interfaz trilingüe (ES/EN/FR) | Cambio en vivo; las palabras de búsqueda en español/francés se traducen a términos en inglés. |
| Flujo completo en un lugar | Buscar → leer → valorar → anotar → exportar notas → preguntar a la IA sobre *este* artículo. |

### Límites honestos
- La calidad de búsqueda depende de Europe PMC; no hay búsqueda semántica ni verificación de citas (la IA puede equivocarse).
- No hay sincronización entre aparatos (respaldo/restauración por archivo).
- No está revisado por pares ni validado clínicamente: es una ayuda de lectura.

### Cómo describirlo en público
> "Una ayuda de lectura gratuita, de código abierto y en un solo archivo para investigar el envejecimiento, creada para una médica-científica mayor: letra grande, trilingüe, privada por diseño, con Europe PMC y un explicador de IA opcional."

Evite: "primero", "revolucionario", "IA médica", "100 % conforme", "reemplaza a su médico". Cite a Europe PMC y a Groq, e indique que se desarrolló con ayuda de IA si es así (buena práctica y coherente con las normas europeas de transparencia).

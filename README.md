# GerontoLib

A free, open-source reading aid for **aging and longevity research**: large-print, high-contrast, trilingual (Spanish · English · French), private by design.
One `index.html`, no backend, no account. Articles come live from the [Europe PMC](https://europepmc.org) API.

> 🇪🇸 Versión en español: [LEEME.md](LEEME.md)

## Features
- Live search with quick topics (senolytics, telomeres, neuroprotection, caloric restriction, autophagy, Alzheimer's, longevity) and free keywords; Spanish/French words are mapped to English terms.
- Article cards: title, authors, journal, year, official source, collapsible abstract, and a green **Safe Site / Open Access** link when free full text exists.
- Ratings (very interesting / interesting / not interested) → automatic **Library**.
- Per-article **notes** → "My Notes" tab, sorted by date, exportable as text; full JSON backup/restore.
- 3 text sizes; live language switching; installable on Android, iPhone and desktop (PWA).
- Optional **AI assistant** (Groq, bring your own free key) + offline glossary of core concepts.
- **Translation** of titles and abstracts into the interface language, with a one-tap "Show original". Uses Groq if configured (best quality; optional automatic title translation); otherwise the free MyMemory service, whose anonymous quota is small (about 5,000 characters/day, i.e. a few abstracts).
- **Voice commands** (🎤 button) in Spanish, English and French: "Go to library", "Search Alzheimer", "Show in library senolytics", "Large text", "Switch to French", "More results". Works in Chrome, Edge and Safari (not Firefox); the audio is processed by the browser vendor's speech service. Verified only with a simulated microphone, not on real devices; speech recognition may be unavailable in an installed iPhone app (open the address in Safari if so).
- Library filter box (by title, author, journal; also matches translated titles).

## Run it
- **Quickest:** download `index.html` and double-click it (search and AI work with an Internet connection; installing as an app is not available this way).
- **As an installable app:** host the folder on any static host (below) and open the address.

### Deploy for free
**GitHub Pages:** create a repo → upload all files → *Settings → Pages* → deploy from branch `main`, folder `/ (root)` → open `https://<user>.github.io/<repo>/`.
**Netlify:** go to `app.netlify.com/drop` and drag the whole folder.

### Install on your phone
- **iPhone/iPad:** open the address in **Safari** → Share → **Add to Home Screen**.
- **Android:** open in **Chrome** → menu ⋮ → **Install app** / **Add to Home screen**.
- **Desktop (Chrome/Edge):** install icon in the address bar.

## AI assistant (optional)
1. Create a free key at <https://console.groq.com/keys>.
2. In the app: **Help → Set up the AI assistant** → paste the key, tick the consent box, save.
3. Default model: `openai/gpt-oss-120b`. Groq changes its model list; if you see a "model" error, edit the name (check their docs).

The key stays in your browser (`localStorage`), is never included in backups, and is sent only to Groq. The free tier has rate limits (roughly 30 requests/minute, with daily caps that vary by model). **Never commit a key to GitHub.** Answers are AI-generated and can be wrong.

## Data & privacy
Everything is stored in your browser. See [PRIVACY.md](PRIVACY.md) for exactly where and what is sent to third parties.

## Compliance & originality
See [COMPLIANCE.md](COMPLIANCE.md) (EU self-assessment) and [ORIGINALITY.md](ORIGINALITY.md).

## Disclaimer
Informational and educational tool. It does not provide medical advice, diagnosis or treatment. Article rights belong to their publishers and authors; the app links to the official pages.

## Files
`index.html` app · `manifest.webmanifest` + `sw.js` + `icons/` installable app · `.nojekyll` GitHub Pages helper · docs.

## License
[MIT](LICENSE)

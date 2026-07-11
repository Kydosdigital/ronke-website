# RONKE Health — marketing website

The public front-facing site for **ronkeai.com**. Static HTML/CSS/JS, no build
step, no framework runtime. Hosted on GitHub Pages.

Rebuilt from the Claude Design handoff (`Ronke Healthcare Website Design`) into
plain, self-contained pages: the design tool's custom `.dc.html` runtime was
removed and the canvas / three.js animations reimplemented in vanilla JS.

## Pages

| File | URL |
|------|-----|
| `index.html` | `/` (Home) |
| `technology.html` | `/technology.html` |
| `clinical-evidence.html` | `/clinical-evidence.html` |
| `about.html` | `/about.html` |
| `contact.html` | `/contact.html` |

Shared styles live in `assets/styles.css`. Each page's animation JS is inline at
the bottom of the file.

## External dependencies (loaded at runtime via CDN)

- Google Fonts — Inter, Lora, JetBrains Mono
- three.js `0.160.0` (jsDelivr) — Home hero waveform only

Everything else is self-contained. The contact form has no backend: it composes
a `mailto:` to hello@ronke.health.

## Local preview

Open any `.html` directly, or serve the folder:

```
python -m http.server 8000
# then visit http://localhost:8000
```

## Deployment

Pushed to GitHub Pages with the custom domain `ronkeai.com` (see `CNAME`).
`.nojekyll` disables Jekyll processing. Any commit to the default branch
redeploys.

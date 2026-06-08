# Compositional Generalization for Real-World Robot Learning

Website for the **Compositional Generalization for Real-World Robot Learning** workshop, a proposed half-day, in-person workshop at CoRL 2026. The workshop solicits novel work that uses the principle of compositionality or modularity to tackle learning problems in robotics, with a focus on approaches that leverage the representational power of scaled systems while retaining the structure of modular ones.

## Debugging / Local Development

This is a plain static HTML site — no build step required.

**Preview locally:**
```bash
# Python (built-in, any machine)
python3 -m http.server 8000
# then open http://localhost:8000/corl2026/
```

**Common issues:**

| Problem | Likely cause | Fix |
|---|---|---|
| Styles not loading | Path to `css/style.css` is wrong | Check the `<link>` href is relative to the HTML file |
| Images not showing | Filename case mismatch or wrong path | Filenames are case-sensitive on Linux/GitHub Pages — verify `images/foo.jpg` matches exactly |
| Changes not appearing on GitHub Pages | CDN cache | Hard-refresh (`Ctrl+Shift+R`) or wait ~1 min after pushing |
| Layout broken on mobile | Missing viewport meta tag | Ensure `<meta name="viewport" content="width=device-width, initial-scale=1.0">` is in `<head>` |

**Browser DevTools** (F12) → Console tab shows JS errors; Network tab shows 404s for missing assets.

**Deployment:** Push to `main` — GitHub Pages serves the repo root automatically. No CI needed.

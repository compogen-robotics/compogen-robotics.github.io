# Compositional Generalization for Real-World Robot Learning

Website for the **Compositional Generalization for Real-World Robot Learning** workshop, a half-day, in-person workshop at CoRL 2026 on November 12, 2026, 8:30 AM–12:30 PM CST, in Rooms 310–311 (Level 3), JW Marriott Austin. The workshop solicits novel work that uses the principle of compositionality or modularity to tackle learning problems in robotics, with a focus on approaches that leverage the representational power of scaled systems while retaining the structure of modular ones.

## Venue and program sources

The November 8 website update uses the [CoRL organizer spreadsheet](https://docs.google.com/spreadsheets/d/1wF6RirHy43dtA48in8Rr4zON4t-afQCFbptS--Ty1Oc/edit) and [venue reference folder](https://drive.google.com/drive/folders/1Tz0olWIQLFluEX49Xvc-I6JNZFcfdJD_):

- **Room Assignment, row 13:** JW Marriott, Rooms 310–311; morning session 8:30 AM–12:30 PM. The organizer confirmed using these assignments on the website without a tentative label.
- **Organizer Input, row 39:** poster session 9:35–10:20 AM.
- **Poster Board Assignment, row 18 (finalized update, November 12):** Lone Star Ballroom (Level 3), boards **072L–091R**; L/R indicate the left/right sides of each board. This supersedes the previous JW3 board numbering. [Finalized assignment](https://docs.google.com/spreadsheets/d/1wF6RirHy43dtA48in8Rr4zON4t-afQCFbptS--Ty1Oc/edit#gid=1736249982&range=A18:L18).
- **Map:** `images/jw-marriott-level-3.png` is a rendered excerpt of page 2 of `venue/jw-marriott-floor-plans.pdf`, the supplied *JW Full Capacity Charts 2020.pdf*. It shows the venue layout, not individual poster-board placement.
- **Program:** at the organizer's request, the panel and facilitated breakout discussions share one 11:10 AM–12:20 PM slot; the 12:20 PM award announcement and 12:30 PM end time are unchanged.

The invited-talk order follows the organizer’s speaker invitations: Jiayuan Mao (8:45 AM), Marc Toussaint (9:10 AM), Leslie Pack Kaelbling (10:20 AM), and Danfei Xu (10:45 AM), all Austin local time (CST, UTC−6). The invitations were corrected on November 9 to match these website times. The source materials do not establish talk titles, individual paper-to-board assignments, poster dimensions, or poster setup/removal times. Add these when provided by the organizers; do not infer poster dimensions from the venue planning drawings.

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

# Сон під вогнем · Sleep Under Fire

Interactive data visualisation exploring how a 6-week digital CBT-I programme
affected the sleep of 113 Ukrainians during active armed conflict (Oct 2023 – Mar 2024).

**Live demo:** open `index.html` in any modern browser — no build step required.

---

## The story

The data contains 2 689 nights of objective sleep tracking from the
*Sleep2Ukraine* feasibility study (Kläger et al., PLOS ONE 2024).

Three findings drive the narrative:

| Metric | Start of programme | End of programme |
|---|---|---|
| Subjective sleep quality (1–10) | 6.3 | 7.2 (+14 %) |
| Sleep interruptions per night | ~26 | ~2 (−93 %) |
| Wake-after-sleep-onset (WASO) | 51 min | 28 min (−45 %) |

The most dramatic moment is **week 19 (26 Feb 2024)** — interruptions collapsed
from 25 to 2 in a single week, marking the point at which most participants had
completed the 6-week programme.

---

## Visualisations

| Chart | Type | Why |
|---|---|---|
| Sleep quality timeline | Line + filled area | Shows the upward trajectory across 23 weeks; two series (subjective vs device score) let the viewer see whether they agree |
| Nightly interruptions | Bar, colour-coded | Magnitude difference between "before" and "after" bars is the visual punchline; colour (red → amber → green) encodes severity |
| Sleep stage composition | Stacked bar + toggle | Shows how each month's sleep budget splits between REM, deep, light, and wake; % toggle separates "how much?" from "what proportion?" |

---

## Colour palette

Dark navy night-sky theme (`#060d1b` background).
Sleep stages: purple (REM) · blue (deep) · grey-blue (light) · red (wake).
Improvement metrics: green · deterioration: red — consistent throughout.

---

## Files

```
index.html                  — single-file visualisation (HTML + CSS + JS)
daily_data_objective.xlsx   — raw data from the Sleep2Ukraine study
README.md
.gitignore
```

---

## Data source

Kläger M, et al. *"Feasibility of a digital CBT-I intervention for insomnia
during armed conflict in Ukraine."*
PLOS ONE, 2024. <https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0310070>

---

## Running locally

```bash
# No dependencies — just open the file
open index.html        # macOS
start index.html       # Windows
xdg-open index.html    # Linux
```

The only external resource is **Chart.js 4.4.2** loaded from jsDelivr CDN.

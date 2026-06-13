# NeuroMH Lab

Website for the **Neurocognitive Development & Mental Health Research Lab** at
Maastricht University, led by Franc Donkers, PhD.

🌐 **Live site:** [neuromh-lab.github.io](https://neuromh-lab.github.io)

📬 **Contact:** see the [contact page](https://neuromh-lab.github.io/contact.html)

Built with [Quarto](https://quarto.org).

## Project structure

| File | Purpose |
|------|---------|
| `_quarto.yml` | Site config — navbar, theme, footer, favicon |
| `custom.scss` | Custom styling (brand colors, cards, publication layout) |
| `index.qmd` | Home page |
| `about.qmd` | Mission and approach |
| `members.qmd` | Lab members |
| `research.qmd` | Research themes |
| `publications.qmd` | Publications — pulls from `publications.yml` via Quarto listings |
| `publications.yml` | Structured publication data |
| `pub-listing.ejs` | Custom EJS template for publication cards |
| `courses.qmd` | Teaching |
| `opportunities.qmd` | Open positions |
| `contact.qmd` | Contact info |
| `_research-themes.qmd` | Reusable include — research theme cards (Home + Research) |
| `_join-cta.qmd` | Reusable include — "Interested in joining?" callout (People + Teaching) |
| `images/` | Favicons, theme icons, EEG divider, PI photo |

Files prefixed with `_` are Quarto includes — they are not rendered as standalone pages.

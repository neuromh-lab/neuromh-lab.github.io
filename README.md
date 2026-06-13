# NeuroMH Lab Website

Quarto website for the Neurocognitive Development & Mental Health Research Lab at Maastricht University.

**Target URL:** `https://neuromh-lab.github.io/`

## Project structure

| File | Purpose |
|------|---------|
| `_quarto.yml` | Site config — navbar, theme, footer, favicon |
| `custom.scss` | All custom styling (brand colors, cards, badges, publication layout) |
| `index.qmd` | Home page |
| `about.qmd` | Mission and approach |
| `members.qmd` | Lab members |
| `research.qmd` | Research themes with detailed descriptions |
| `publications.qmd` | Publications — pulls from `publications.yml` via Quarto listings |
| `publications.yml` | Structured publication data (title, authors, journal, year, DOI, category) |
| `pub-listing.ejs` | Custom EJS template for rendering publication cards |
| `courses.qmd` | Teaching |
| `opportunities.qmd` | Open positions |
| `contact.qmd` | Contact info and map |
| `_research-themes.qmd` | Reusable include — research theme cards (used on Home + Research) |
| `_join-cta.qmd` | Reusable include — "Interested in joining?" callout (used on People + Teaching) |
| `images/` | Favicon files, theme icons, EEG divider, placeholder photos |

Files prefixed with `_` are Quarto includes — they are not rendered as standalone pages.

## Quick start

### Prerequisites (install once)

- [Positron IDE](https://positron.posit.co)
- [Quarto](https://quarto.org/docs/get-started/)
- [Git](https://git-scm.com)

### Preview locally

Open the project folder in Positron, then in the terminal:

```bash
quarto preview
```

### Build and deploy

```bash
quarto render
git add .
git commit -m "Update website"
git push
```

GitHub Pages deploys automatically from the main branch. The site will be live at `https://neuromh-lab.github.io/` within a few minutes.

## Common tasks

### Adding a publication

Open `publications.yml` and add a new entry:

```yaml
- title: "Your Paper Title Here"
  authors: "Smith A, **Donkers FCL**, Jones B"
  journal: "Journal Name"
  year: 2026
  doi: "10.xxxx/xxxxx"
  category: "sensory"
```

Notes:

- **category** determines the section: `sensory`, `markers`, `modelling`, or `other`
- Wrap the PI name in `**double asterisks**` to render it bold
- If there is no DOI, use `doi: ""`  — the template will skip the DOI link and citation badges
- Publications are sorted by year (newest first) within each section
- Citation badges (Dimensions and Altmetric) appear automatically for any entry with a DOI

After editing, render the site and the new publication appears in the correct section.

### Adding a team member

Open `members.qmd` and copy an existing member card block. Replace the name, role, project description, photo path, and links.

### Editing research theme cards

Edit `_research-themes.qmd` — changes apply to both the Home page and Research page automatically.

### Editing the "Interested in joining?" callout

Edit `_join-cta.qmd` — changes apply to both the People page and Teaching page.

### Changing brand colors

Edit `custom.scss` — the color variables are at the top:

```scss
$primary:   #2C5F8A;
$secondary: #4A9EBF;
$accent:    #E8732A;
$dark:      #1A2E40;
$light-bg:  #EAF4FB;
```

### Adding photos

Place images in `images/` and reference them as `![](images/filename.jpg)`.

## Help

- [Quarto website documentation](https://quarto.org/docs/websites/)
- [Quarto theming guide](https://quarto.org/docs/output-formats/html-themes.html)
- [Quarto includes](https://quarto.org/docs/authoring/includes.html)
- [Quarto listings](https://quarto.org/docs/websites/website-listings.html)
- [GitHub Pages guide](https://pages.github.com)

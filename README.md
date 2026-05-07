# AI as Your Curriculum Partner — IEDRC Faculty Retreat

A self-paced, single-file interactive workshop site for the **Inland Empire / Desert Regional Consortium (IEDRC)** Faculty Retreat.

**Topic:** Using AI tools (ChatGPT, Claude, Gemini) to draft Course Outlines of Record (CORs), generate Student Learning Outcomes (SLOs) from labor market data, and build assessments and rubrics — without sacrificing accreditation rigor.

**Live site:** [iedrc-faculty-retreat.vercel.app](https://iedrc-faculty-retreat.vercel.app)

---

## What's in this folder

```
SAC-Workshop/
├── index.html         ← The entire participant site (single file, no build step)
├── data/              ← Synthetic practice data for each of the 5 modules
│   ├── README.md
│   ├── module-1-starter-system-prompt.txt
│   ├── module-2-sample-catalog-descriptions.txt
│   ├── module-3-onet-task-exports.txt
│   ├── module-4-sample-SLOs.txt
│   ├── module-5-AI-output-with-errors.txt
│   └── iedrc-workshop-practice-data.zip
└── README.md          ← You are here
```

The `data/` folder contains plain-text practice files so any participant can complete every module — even without an existing COR, an O*NET account, or their own SLO list. Each module card on the live site has a one-click download button for its matching file, and the Quick Start section has a banner to grab all five at once as a zip. See `data/README.md` for details.

---

## How to open locally in Cursor

1. Open **Cursor**
2. **File → Open Folder** → select this folder
3. Click `index.html` in the sidebar
4. Right-click → **Open with Live Preview** (or use the Live Server extension)

The site opens in your browser at `localhost:5500`.

---

## How to deploy with Vercel (free)

1. Go to **[vercel.com](https://vercel.com)** and sign in or create a free account
2. Click **Add New → Project**
3. If in a GitHub repo: import the repo — Vercel auto-deploys on every push to `main`
4. If local only: install the Vercel CLI (`npm i -g vercel`) and run `vercel` from this folder
5. Vercel gives you a live URL instantly

Every push to `main` redeploys automatically. No build step needed.

---

## How to generate a QR code for your presentation

Once you have your live URL:
- **[qrcode-monkey.com](https://qrcode-monkey.com)** — customize with IEDRC colors
- **[qr-code-generator.com](https://qr-code-generator.com)** — quick and clean
- **Google**: type `qr code [your URL]` directly into the search bar

**QR slide tips:**
- Make the code at least 4 inches square on your slide
- Put the URL in text below it (for people who prefer typing)
- Add: *"Scan to follow along — works on your phone or laptop"*
- Leave it on screen for the first 5 minutes while people get settled

---

## IEDRC Brand System

The visual design follows the official IEDRC identity at [desertcolleges.org](https://desertcolleges.org).

### Color tokens (from `:root` in `index.html`)

| Token | Hex | Use |
|---|---|---|
| `--navy` | `#1A2C57` | Primary brand navy — used for "EDRC" wordmark, large cards, body text on light surfaces |
| `--navy-deep` | `#0F1B3D` | Deeper navy variant for darkest accents |
| `--navy-soft` | `#4C5E89` | Muted navy for secondary text |
| `--orange` | `#F06937` | Brand sunrise orange — primary CTA, the "I" in IEDRC, sun rays |
| `--orange-deep` | `#C05B28` | Logo curve / deep accent / button hover |
| `--orange-light` | `#F18A2D` | Lighter amber for highlights and gradients |
| `--cream` | `#F7F3E9` | Warm card background (light theme) |
| `--tan` | `#DFD1A7` | Warm tan accent |
| `--cyan` | `#00B1D9` | Secondary cyan accent |
| `--sky` | `#389BD9` | Mid blue |

### Brand mark
The mountain + sunrise + desert curve logo is rendered inline as SVG in two places: the top-nav brand and the footer. Edit those `<svg>` blocks to swap in a different mark.

---

## Customizing the site in Cursor

All content is in `index.html`. Key spots to edit:

| What to change | Where to find it |
|---|---|
| Event name / date | Search for `IEDRC Faculty Retreat` and `Spring 2026` |
| Brand colors | Search for `:root {` near the top of the `<style>` block |
| Hero title / subtitle | Search for `AI as Your` in the `<section class="hero">` block |
| Module content / steps | Search for `Module 01`, `Module 02`, etc. |
| Prompt text (copy buttons) | Edit the `<pre class="sample-text">` block — the Copy button reads from there |
| Checklist items | Search for `check-row` in the `#checklist` section |
| Footer text | Search for `<footer>` near the bottom of the HTML |
| Logo SVG | Search for `brand-mark` (nav) or `footer-mark` (footer) |

**To ask Cursor's AI to make changes**, open `index.html` and press `Cmd+K` (Mac) or `Ctrl+K` (Windows):
- *"Add a 4th warning card about equity considerations in AI-generated curriculum"*
- *"Add a Business & Professional Development section to the prompt library"*
- *"Change the hero subtitle to focus on program review instead of SLOs"*

---

## Adding new discipline prompt cards

To add a new prompt to the library, copy one of the existing `<div class="prompt-card">` blocks (search for `prompt-card reveal`) and:

1. Set `data-discipline="health"` (or `business`, `construction`, `ict`, `all`)
2. Update the `.prompt-accent` gradient color to use IEDRC palette values
3. Update the `.ptag` tags (e.g., `ptag-health`, `ptag-business`)
4. Update the title, description, and prompt text inside the `<pre class="sample-text">` block — the Copy button automatically reads from there

---

## Disciplines and tag classes

| Discipline | Tag Class | Filter Value |
|---|---|---|
| Health | `ptag-health` | `data-disc="health"` |
| Business | `ptag-business` | `data-disc="business"` |
| Construction | `ptag-construction` | `data-disc="construction"` |
| ICT | `ptag-ict` | `data-disc="ict"` |
| All Disciplines | `ptag-all` | `data-disc="all"` |

---

## Accessibility features built in

- **Dark / Light / High-Contrast** theme toggle (top nav bar)
- **Text size** controls: A / A+ / A++ (accessibility panel, top nav bar)
- **Progress bar** (top of page, scroll-linked)
- **Back to top** button (bottom right, appears after scrolling)
- **Skip to main content** link (keyboard navigation)
- **Jargon tooltips** (dotted underline terms — hover, focus, or tap)
- **Checklist state** persists in localStorage (refresh-safe)
- **Reduced motion** respected via CSS `prefers-reduced-motion`
- **Keyboard checkbox toggle** — Enter or Space toggles each row (with `preventDefault` to avoid page scroll)
- All copy buttons read from their visible `<pre>` block — what you see is what you copy

---

## Disclaimer

> AI-generated curriculum drafts must be reviewed and approved through your institution's official curriculum committee process before submission. This site does not replace CurricUNET, Title 5 compliance review, or ACCJC accreditation standards review.

---

*Funded by the California Strong Workforce Program · [desertcolleges.org](https://desertcolleges.org)*

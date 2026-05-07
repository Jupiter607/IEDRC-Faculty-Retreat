# AI as Your Curriculum Partner — IEDRC Faculty Retreat

A self-paced, single-file interactive workshop site for the IEDRC Faculty Retreat.  
**Topic:** Using AI tools (ChatGPT, Claude, Gemini) to draft CORs, generate SLOs from labor market data, and build assessments and rubrics.

---

## What's in this folder

```
SAC-Workshop/
├── index.html   ← The entire participant site (single file, no build step)
└── README.md    ← You are here
```

---

## How to open locally in Cursor

1. Open **Cursor**
2. **File → Open Folder** → select the `SAC-Workshop/` folder
3. Click `index.html` in the sidebar
4. Right-click → **Open with Live Preview** (or use the Live Server extension)

The site opens in your browser at `localhost:5500`

---

## How to deploy with Vercel (recommended — free)

1. Go to **[vercel.com](https://vercel.com)** and sign in or create a free account
2. Click **Add New → Project**
3. If in a GitHub repo: import the repo — Vercel auto-deploys on every push to `main`
4. If local only: install the Vercel CLI (`npm i -g vercel`) and run `vercel` from this folder
5. Vercel gives you a live URL instantly (e.g. `https://sac-curriculum-ai.vercel.app`)
6. Optional: add a custom domain in **Project Settings → Domains**

Every push to `main` redeploys automatically. No build step needed.

---

## How to generate a QR code for your presentation

Once you have your Vercel URL:
- **[qrcode-monkey.com](https://qrcode-monkey.com)** — customize with SAC colors
- **[qr-code-generator.com](https://qr-code-generator.com)** — quick and clean
- **Google**: type `qr code [your URL]` directly into the search bar

**QR slide tips:**
- Make the code at least 4 inches square on your slide
- Put the URL in text below it (for people who prefer typing)
- Add: *"Scan to follow along — works on your phone or laptop"*
- Leave it on screen for the first 5 minutes while people get settled

---

## Customizing the site in Cursor

All content is in `index.html`. Key spots to edit:

| What to change | Where to find it |
|---|---|
| Event name / date | Search for `IEDRC Faculty Retreat` and `Spring 2026` |
| SAC colors (red/gold) | Search for `--red` and `--gold` in the `<style>` block |
| Hero title and subtitle | Search for `AI as Your` in the `<section class="hero">` block |
| Module content / steps | Search for `Module 01`, `Module 02`, etc. |
| Prompt text (copy buttons) | Search for `copyText(this,` — each prompt is a template literal |
| Checklist items | Search for `check-row` in the `#checklist` section |
| Footer text | Search for `footer` at the bottom of the HTML |

**To ask Cursor's AI to make changes**, open `index.html` and press `Cmd+K` (Mac) or `Ctrl+K` (Windows):
- *"Add a 4th warning card about equity considerations in AI-generated curriculum"*
- *"Add a Business & Professional Development section to the prompt library"*
- *"Change the hero subtitle to focus on program review instead of SLOs"*

---

## Adding new discipline prompt cards

To add a new prompt to the library, copy one of the existing `<div class="prompt-card">` blocks (search for `prompt-card reveal`) and:

1. Set `data-discipline="health"` (or `business`, `construction`, `ict`, `all`)
2. Update the `.prompt-accent` gradient color to match the discipline
3. Update the `.ptag` tags
4. Update the title, description, and prompt text
5. Update the `copyText(this, ...)` value with the full prompt text (use backtick template literals for multi-line)

---

## Disciplines and color reference

| Discipline | Accent Color | CSS Filter Value |
|---|---|---|
| Health | `#ff6b9d` pink | `data-disc="health"` |
| Business | `#E5A823` gold | `data-disc="business"` |
| Construction | `#ff8c00` orange | `data-disc="construction"` |
| ICT | `#7c6aff` purple | `data-disc="ict"` |
| All Disciplines | `#00c896` teal | `data-disc="all"` |

---

## Accessibility features built in

- **Dark / Light / High-Contrast** theme toggle (top nav bar)
- **Text size** controls: A / A+ / A++ (accessibility panel, top nav bar)
- **Progress bar** (top of page, scroll-linked)
- **Back to top** button (bottom right, appears after scrolling)
- **Skip to main content** link (keyboard navigation)
- **Jargon tooltips** (dotted underline terms — hover or focus to read)
- **Checklist state** persists in localStorage (refresh-safe)
- **Reduced motion** respected via CSS `prefers-reduced-motion`

---

## Disclaimer

> AI-generated curriculum drafts must be reviewed and approved through your institution's official curriculum committee process before submission. This site does not replace CurricUNET, Title 5 compliance review, or ACCJC accreditation standards review.

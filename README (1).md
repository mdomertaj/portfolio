# Portfolio — Mohammed

A static, single-page portfolio site. No build step. No dependencies. Drop it on GitHub Pages and it runs.

---

## What's inside

```
portfolio/
├── index.html      ← the entire site (HTML + CSS + JS in one file)
└── README.md       ← this file
```

That's it. The whole site is one self-contained `index.html`. Fonts come from Google Fonts via CDN.

---

## Before you publish — fill these in

Open `index.html` and search for these placeholders:

| Find | Replace with |
|---|---|
| `your.email@example.com` (appears twice) | your real email |
| `linkedin.com/in/your-handle` | your LinkedIn URL |
| `/in/your-handle` | the display version of your LinkedIn handle |
| `https://github.com/your-handle` | your GitHub URL |
| `@your-handle` | your GitHub username |
| `Mohammed` (in `<title>` and footer) | your full name if you want last name shown |

You may also want to tweak the role descriptions in the **Experience** section — they're written generically against what's likely in your background, but specific results and metrics will land harder. Aim for the 13–20 bullets / 50%+ quantified guideline you usually use on your resume.

---

## Deploy to GitHub Pages — three options

### Option A — Personal site at `username.github.io` (recommended)

This gives you a clean URL like `mohammed.github.io`.

1. On GitHub, create a new public repository named **exactly** `your-username.github.io` (e.g. if your username is `mohammed-w`, the repo is `mohammed-w.github.io`).
2. Clone it locally, or upload via the web UI.
3. Add `index.html` to the root of the repo (not inside a subfolder).
4. Commit and push.
5. Go to the repo on GitHub → **Settings** → **Pages**. Under "Build and deployment", set **Source** to **Deploy from a branch**, branch **main**, folder `/ (root)`. Save.
6. Wait 30–60 seconds. Your site is live at `https://your-username.github.io`.

### Option B — Project site at `username.github.io/portfolio`

Use this if you'd rather keep the personal `username.github.io` URL free for something else later.

1. Create a public repo with any name, e.g. `portfolio`.
2. Push `index.html` to the `main` branch.
3. **Settings** → **Pages** → Source: **Deploy from a branch**, branch **main**, folder `/ (root)`. Save.
4. Live at `https://your-username.github.io/portfolio/`.

### Option C — Command line, start to finish

```bash
# from inside the portfolio/ folder
git init
git add index.html README.md
git commit -m "Initial portfolio"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-USERNAME.github.io.git
git push -u origin main
```

Then enable Pages in the repo settings as above.

---

## Custom domain (optional)

If you own a domain like `mohammed.dev`:

1. In your repo, **Settings** → **Pages** → **Custom domain** → enter `mohammed.dev` → Save. This creates a `CNAME` file in your repo.
2. At your domain registrar, add the GitHub Pages DNS records:
   - **Apex domain (`mohammed.dev`)** — four `A` records pointing to:
     ```
     185.199.108.153
     185.199.109.153
     185.199.110.153
     185.199.111.153
     ```
   - **`www` subdomain** — a `CNAME` record pointing to `your-username.github.io`.
3. Back in **Settings** → **Pages**, tick **Enforce HTTPS** once the certificate provisions (can take ~10 minutes).

---

## Editing the site

Everything is in `index.html`. The structure, top to bottom:

| Section | What it contains | HTML id |
|---|---|---|
| Top bar | Brand mark + nav | — |
| Hero | Name, tagline, intro, CTAs | — |
| Marquee | Auto-scrolling discipline strip | — |
| About | 01 — Profile + stats | `#about` |
| Expertise | 02 — Three pillars (cybersecurity / cloud / IT support) | `#expertise` |
| Education | 03 — Conestoga diplomas ledger | `#education` |
| Experience | 04 — Three roles | `#experience` |
| Certifications | 05 — Pursued certs | `#certs` |
| Contact | 06 — Channels | `#contact` |
| Footer | Copyright | — |

### Quick edits

- **Change accent color** — at the top of the `<style>` block, edit `--sienna: #b04a26;`. Try a deep blue (`#1e40af`), forest (`#15803d`), or oxblood (`#7c1d1d`).
- **Switch to dark mode** — swap these two CSS variables: `--paper: #14130f;` and `--ink: #f3eee2;`. The rest of the design adapts.
- **Fonts** — currently Fraunces (display) + IBM Plex Sans (body) + IBM Plex Mono (technical labels). Replace the Google Fonts `<link>` and the `--serif` / `--sans` / `--mono` variables to change.

---

## Browser support & accessibility

- Works on every modern browser. No build step, no transpilation.
- Honours `prefers-reduced-motion` — disables marquee, pulse, and reveal animations for users who prefer no motion.
- Fully responsive down to ~360px width.
- Semantic landmarks (`<header>`, `<section>`, `<footer>`) and meaningful headings.

---

## License

Yours. Use it, edit it, republish it as your own — no attribution needed.

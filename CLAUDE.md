# Sigma Nu — Gamma Upsilon Chapter Website

Website for the **Gamma Upsilon Chapter of Sigma Nu, University of Arkansas**.
This file orients Claude Code so it can make edits reliably. Read it first.

## What this site is
- A **static, hand-coded** site — plain HTML + one CSS file + a tiny bit of JS.
- **No framework, no build step.** What's in the files is exactly what ships.
- Hosted free on **GitHub Pages**.

## How to publish a change
1. Make the edit in the file(s).
2. Commit and push to the `main` branch.
3. GitHub Pages rebuilds automatically — the live site updates in about a minute.
4. **Always confirm on the live site afterward:**
   https://uarksigmanuwebsite.github.io/

Repo: `github.com/UarkSigmaNuWebsite/uarksigmanuwebsite.github.io`

## Pages (8 total)
| File | Purpose |
|------|---------|
| `index.html` | Home |
| `about.html` | History |
| `involvement.html` | Philanthropy / brotherhood / leadership / athletics |
| `rush.html` | Recruitment + Rush Chairmen |
| `gallery.html` | Photo gallery |
| `alumni.html` | Alumni events, giving, stay-connected form |
| `contact.html` | Chapter email, mailing address, leadership roster |
| `give.html` | Donations (Venmo link is a pending TODO in this file) |

Supporting files: `css/style.css` (all styling), `js/nav.js` (mobile menu),
`images/` (logo `razorback.png`, `hero.jpg`, gallery in `images/gallery/`).

## Where common edits live
- **Officer / leadership roster** → `contact.html` (the "Chapter Leadership" `.card` blocks).
- **Rush Chairmen** → `rush.html` (cards under "Interested in Rushing?") AND `contact.html` (Recruitment card). Update both.
- **Alumni tailgate game** → `alumni.html` (the `.event-card`: opponent, date, location).
- **Donation / Venmo link** → `give.html` (see the TODO comment near the bottom for exactly where the Venmo URL goes).
- **Gallery photos** → add image files to `images/gallery/`, then add a matching `<figure class="photo">` block in `gallery.html`.
- **Chapter email / mailing address** → `contact.html`.

## Rules to follow when editing
- **Header and footer are copied into every page** (no shared template). If you
  change the nav or footer, apply the SAME change to all 8 pages.
- **Design system** (don't drift from it):
  - Colors: Cardinal red `#9D2235`, near-black `#14100F`, parchment `#F6F1EE`.
    These live as CSS variables (`--gold`, `--ink`, `--parchment`) in `css/style.css`.
  - Fonts: **Marcellus** for headings, **Source Sans 3** for body.
- **Mobile matters.** Keep it responsive. For card grids, use CSS classes
  (e.g. `.cards`, `.cards--two`) — do NOT set `grid-template-columns` with an
  inline `style=""`, because that overrides the mobile rules and breaks phones.
- Keep changes small and focused. Match the style of the surrounding markup.

## Handoff note
This site is maintained by whoever holds the shared chapter GitHub login
(kept with the chapter's Instagram/email credentials — NOT stored in this
public repo). See `HOW-TO-EDIT.md` for the human walkthrough.

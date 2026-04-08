# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repo is

A **static HTML wireframe/prototype** for the Scaler CPE (Career Profile Evaluator) v2 redesign. There is no build step, no framework, no package.json — just hand-written HTML/CSS with inline `<style>` blocks and Phosphor icons + Google Fonts loaded from CDN. To preview, open the HTML files directly in a browser (`open index.html`, `open report.html`).

This is a design artifact, not production code. The job is usually to iterate on layout/copy/visual design, not to add build tooling or refactor into components.

## Product context

**Scaler** is a tech-education platform selling 4 programs: Scaler Software Engineering, Scaler DSML, Scaler AIML, Scaler DevOps.

**CPE** is a top-of-funnel lead-gen tool. A prospect answers ~10 questions about their background and ambitions, gets a personalised report, and is funneled toward booking a free career consultation call. The redesign's central thesis is **AI urgency**: framing the report around what AI is replacing vs. augmenting in the user's specific role, instead of a generic readiness score.

### Program mapping (target role → program)
- Backend / Fullstack / Frontend / SWE / Tech Lead → **Scaler Software Engineering**
- Data Science / ML → **Scaler DSML**
- AI/ML Engineer → **Scaler AIML**
- DevOps / Infra → **Scaler DevOps**

Same program landing URL for all four, differentiated by UTM params. Persona-specific messaging happens **inside the CPE report**, not on the program landing page.

### Data sources (for any dynamic/templated content)
- **MasterClass card**: live API exists, mock for now (name, date, time, instructor image)
- **Free courses**: Scaler Topics platform — role-specific URLs to be mapped
- **Alumni stories**: real data (photo, name, prev co. → next co., rating, quote, salary stat)
- **AI impact + tools playbook**: GPT-generated per role — must be specific workflow examples, not generic tool lists
- **AI urgency stats in CTAs**: currently mocked

## File map

- [index.html](index.html) — The questionnaire flow. Single file containing all screens as `<section id="screen-*" class="screen">`, navigated via in-page anchor links (`href="#screen-..."`). Entry screen is `screen-1`, then two branches: **tech professional** (`screen-t-1` → `screen-t-3`) and **non-tech / career switcher** (`screen-nt-1` → `screen-nt-3`). Final screen links to `report.html`.
- [report.html](report.html) — The redesigned report prototype. Long single-file scrollable page with numbered narrative sections (see below).
- [question-bank.md](question-bank.md) — Master list of all candidate questions, organised by persona/topic. Source of truth for what may appear in `index.html`.
- [questions.md](questions.md) — The currently selected/shipped question set (subset of the bank).
- [Assets/](Assets/) — Reference mockups (`1.png`–`7.png`, `Report.png`) for the screens and report.

## Report architecture

The redesigned report in [report.html](report.html) is structured as a **6-section narrative** (eyebrows like `01 · Your Snapshot`), each with a conversational `section-title` and `section-subtitle`. The progression is intentional — do not reorder without understanding the narrative arc:

1. **Your Snapshot** — how recruiters see the user today, with skills tagged for AI relevance
2. **The Gap** — six-axis comparison vs. the median engineer landing target offers
3. **Two Paths** — free track vs. structured (paid) track, presented as a choice not a pitch
4. **People Like You** — 3 alumni stories matched to the user's starting point
5. **Why Now** — AI urgency: what's already gone, what's amplified, the tools that decide
6. **The Reward** — 3 real role targets with live salary ranges and open positions

Followed by a **CTA section** (`.cta-section`), a **footer CTA** (`.footer-cta`), and a persistent **floating CTA** (`.float-cta`).

> Note: an earlier spec described a 9-section report (Hero, AI mentor message, Strengths/gaps, AI impact, AI tools playbook, Alumni stories, Career timeline, Dual-track quick wins, AI urgency CTA). Most of those concepts survived but were merged/renamed into the 6-section narrative above. If a request references the older section names, map them to the current structure rather than reverting.

## Styling conventions

Both HTML files share an editorial / brutalist-leaning style with deliberate constraints:

- **No border-radius anywhere.** The global reset in both files contains `* { border-radius: 0 !important; }`. Do not add rounded corners.
- **Two fonts only**: `Plus Jakarta Sans` (UI) and `Source Serif 4` (display/editorial headlines), defined as `--font` and `--font-display`.
- **Monochrome palette** driven by CSS custom properties on `:root` (`--black`, `--white`, `--gray-50` … `--gray-900`, `--cta-black`). Color is used sparingly and intentionally — don't introduce new accent colors without a reason. `report.html` also defines `--border: #D4D4D4` and `--border-strong: #1A1A1A` for its softer default borders; use those vars rather than raw hex when working in that file.
- **Icons**: Phosphor (`@phosphor-icons/web`) via CDN, used as `<i class="ph ph-*">`.
- All CSS lives **inline** in each HTML file's `<style>` block — there is no shared stylesheet. When changing tokens, update both files if the change should be global.

## Working in this repo

- Edit `.html` files directly; reload the browser to see changes.
- When adding screens to the questionnaire, follow the existing `<section id="screen-..." class="screen">` pattern and wire navigation via `href="#..."` anchors plus the back-arrow in `.topbar`.
- When adjusting questions, keep [question-bank.md](question-bank.md) and [questions.md](questions.md) in sync with whatever ships in [index.html](index.html).
- Treat the report's narrative arc and the AI-urgency framing as load-bearing — they're the core differentiator vs. the old report. Layout and visuals can change freely; the storyline shouldn't drift back to a generic "readiness score + book a call" report without a deliberate decision.

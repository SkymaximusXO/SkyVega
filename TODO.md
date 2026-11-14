# SkyVega site — status & next steps

Single-page site (`index.html`) for СКАЙВЕГА. **Since 2026-11-14 the copy and
visual style follow the founder's One-Pager PDF** (sections 01–06: Проблема,
От идеи до готового продукта, Решение, Почему мы, Для кого, Команда).
If the One-Pager changes, the site should be re-synced to it.

## Repository — always work here
- GitHub repo: **SkymaximusXO/SkyVega** (public, push access granted).
- At the start of a session: attach with `add_repo` (owner `SkymaximusXO`,
  repo `SkyVega`, access `push`), clone and work on the repo copy — the
  project's `index.html` is a mirror and may lag behind.
- After pushing, also update `index.html` / `TODO.md` in the claude.ai project.

## Live now
- GitHub Pages from branch `claude/claude-capabilities-setup-kqxpxf`
  (root, no build step). Suggested: rename to `main`.
- Files: `index.html`, `assets/logo.png`, `assets/mark.png` (favicon),
  `assets/maxim.jpg`, `assets/anna.jpg` (all extracted from the One-Pager).
- "Обсудить проект" opens a modal form → FormSubmit.co AJAX.

## Design notes (2026-11-14 redesign)
- Font: **Onest** (same as One-Pager) + JetBrains Mono for code accents.
- Colors: bg `#0d0d0d`, cards `#141415` / green-tinted `#181c19`,
  accent gold `#e4ac68` (sampled from One-Pager).
- Background: fixed ambient layer — faint engineering grid, gold/green glow
  orbs, twinkling starfield. Hero visual: orbit + constellation + Vega star
  (from logo), floating "project.ts" code card, roadmap/Gantt card,
  "Релиз готов" status chip. Respects `prefers-reduced-motion`.
- Section labels as outlined pills "01 ПРОБЛЕМА" etc., like the One-Pager.
- Single file, no framework, no build step — keep it that way.

## Known placeholders — do not treat as real data
- Form target email `maxim.nebov@googlemail.com` — test address; swap for
  the company inbox. FormSubmit needs a one-time confirmation click.
- Contacts (founder, 2026-11-14): phone **+7 (911) 979-06-07** (header, menu,
  contact, footer) and email **info@skyvega.ru** (contact block, footer, form
  error text). The form itself still posts to the test address — founder
  asked to leave it as is. The skyvega.ru mailbox must actually exist and
  receive mail. Telegram not yet provided.
- Consent "Что это значит?" text is not a real privacy policy (152-ФЗ).
- Insights section removed (no content). Re-add when there are real posts/cases.

## Open questions for the founder
- Real Telegram handle; confirm info@skyvega.ru mailbox is set up.
- Domain name → `CNAME` file + GitHub Pages setting + DNS.
- Is FormSubmit.co reachable from Russian ISPs? If not → Web3Forms or similar.
- Real privacy policy text.

## Backlog
- Yandex.Metrika / Webmaster verification.
- Personal email exposed in public repo — use FormSubmit hashed alias.
- 152-ФЗ: data goes to a US service + Gmail; consent must be a separate doc.
- Form: phone/Telegram as alternative to email; consent should link to policy.
- OG image: currently the logo PNG; a dedicated 1200×630 card would be better.

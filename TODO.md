# SkyVega site — status & next steps

Single-page site (`index.html`) for СКАЙВЕГА. **Since 2026-11-14 the copy and
visual style follow the founder's One-Pager PDF** (sections 01–06).
**2026-11-14 rework (deviates from One-Pager):** 01 Проблема → 02 Решение
(services and process merged: two tracks — «Бизнес-консалтинг» with steps
01 Диагностика, 02 Стратегия и план; «IT-разработка и запуск» with 03
Проектирование, 04 Реализация, 05 Запуск и рост; plus an «Упаковка и
аутстаффинг на любом этапе» strip) → 03 Почему мы → 04 Для кого → 05 Команда.
Backup of the pre-rework version: branch `claude/backup-2026-11-14-before-process-rework`.
One-Pager should be updated to match.
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
  `assets/maxim.jpg`, `assets/anna.jpg` (from the One-Pager), `assets/polina.jpg`
  (sent by founder 2026-11-14).
- Team leads (2026-11-14): Максим Небов — Фаундер; Анна Михайлова — Соучредитель;
  Полина Рахматуллина — CMO. Below them a "Команда специалистов" panel with
  role cards (no names/headcount by founder's choice).
- "Оставить заявку" (contact block) opens a modal form → Web3Forms AJAX.
  Other CTAs are "Связаться с нами" and scroll to #contact.

## Design notes (2026-11-14 redesign)
- Font: **Onest** (same as One-Pager) + JetBrains Mono for code accents.
- Colors: bg `#0d0d0d`, cards `#141415` / green-tinted `#181c19`,
  accent gold `#e4ac68` (sampled from One-Pager).
- Background: fixed ambient layer — faint engineering grid, gold/green glow
  orbs, twinkling starfield. Hero visual: orbit + constellation + Vega star
  (from logo), floating "project.ts" code card, roadmap/Gantt card,
  "Релиз готов" status chip. Respects `prefers-reduced-motion`.
- Process steps (section 02) are buttons: click opens a detail dialog
  (#stepOverlay) with an inline SVG illustration, lead, "Что делаем" list,
  "Результат этапа", prev/next, dots, swipe on touch, CTA → #contact.
  Copy lives in the `STEPS` array in the script — edit there. No durations
  or prices promised on purpose.
- Section labels as outlined pills "01 ПРОБЛЕМА" etc., like the One-Pager.
- Single file, no framework, no build step — keep it that way.

## Known placeholders — do not treat as real data
- Form posts to **Web3Forms** (since 2026-11-17; FormSubmit dropped — its
  activation page returned 500). Access key `9ab0e4fe-ff4b-438a-baea-b5cf565c8dd8`
  (public by design), account maxim.nebov@googlemail.com (founder's test Gmail),
  domain set to skymaximusxo.github.io — update in app.web3forms.com when the
  real domain / company inbox arrive. Free plan: 250 submissions/month.
  Honeypot field `botcheck`.
- Contacts (founder, 2026-11-14): phone **+7 (911) 979-06-07** (header, menu,
  contact, footer) and email **info@skyvega.ru** (contact block, footer, form
  error text). The form delivers to the founder's test Gmail via Web3Forms. The skyvega.ru mailbox must actually exist and
  receive mail. Telegram not yet provided.
- Consent "Что это значит?" text is not a real privacy policy (152-ФЗ).
- Insights section removed (no content). Re-add when there are real posts/cases.

## Open questions for the founder
- Real Telegram handle; confirm info@skyvega.ru mailbox is set up.
- Domain name → `CNAME` file + GitHub Pages setting + DNS.
- Confirm Web3Forms submissions arrive reliably from Russian networks.
- Real privacy policy text.

## Backlog
- Yandex.Metrika / Webmaster verification.
- 152-ФЗ: data goes to a US service + Gmail; consent must be a separate doc.
- Form: phone/Telegram as alternative to email; consent should link to policy.
- OG image: currently the logo PNG; a dedicated 1200×630 card would be better.
